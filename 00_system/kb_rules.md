---
doc_type: system_rules
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [kb_rules, formatting, conventions, agent_behaviour]
related:
  - 00_system/document_template.md
  - 00_system/naming_conventions.md
  - 00_system/agent_workflow.md
---

# Knowledge Base Rules

## Purpose

Define the binding rules every contributor, human or agent, must follow when reading, creating, or modifying files in this repository. These rules optimise the KB for semantic retrieval, downstream artifact generation, and long-term auditability.

## Key Takeaways

- Every analytical file uses the YAML frontmatter and section structure from `00_system/document_template.md`. Folder index files (`README.md` at a folder root, `.gitkeep` placeholders) follow a lighter convention documented below.
- Files are atomic: one concept per file. If a file covers two concepts, split it.
- Every quantitative claim cites a source or is flagged as an assumption.
- Cross-link aggressively. Relative markdown links are the primary connective tissue.
- Outputs in `11_outputs/` are derivatives, never edit them directly when the upstream source is wrong; fix the source.
- Anti-generic writing is enforced. See banned-phrase list in `00_system/research_prompt_template.md`.

## Core Content

### Required File Structure

Every markdown document must contain, in this order:

1. YAML frontmatter (see schema below)
2. `# Title`
3. `## Purpose`
4. `## Key Takeaways`
5. `## Core Content`
6. `## Evidence / Sources`
7. `## Objections Answered`
8. `## Website Implications`
9. `## Open Questions`
10. `## Change Log`

Documents that have nothing meaningful to say in a section must still include the heading, with a single line stating "Not applicable" and a reason. This keeps the schema machine-parseable.

### Frontmatter Schema

```yaml
doc_type: {one of: thesis | brief | research | competitive | model | spec | page_brief | system_rules | template | output | source}
status: {seed | draft | validated | stable | deprecated}
confidentiality: {public | investor | internal | restricted}
owners: [list of github handles or names]
last_reviewed: YYYY-MM-DD
retrieval_tags: [4-10 snake_case tags]
related: [optional list of relative paths to related files]
assumption: {true | false}  # true if the doc rests on unverified claims
supersedes: {optional relative path to the file this replaces}
```

### Writing Style

- **Active voice. Concrete nouns. Specific verbs.**
- Numbers > adjectives. "Reaches 18–34 viewers at 2.3x the index of broadcast reality" beats "engages younger viewers".
- One claim per sentence where possible.
- Define jargon on first use, or link to `01_master_context/glossary.md`.
- Avoid filler openings ("In recent years…", "It is well known that…").
- Avoid the banned list in `00_system/research_prompt_template.md`.
- **No em dashes (`—`).** Anywhere in the KB or in any artifact derived from it. Use periods, commas, colons, or parentheses. Binding rule; checked on review.

### Distinguishing Fact, Hypothesis, and Proposal

Any analytical document must classify load-bearing claims into one of three categories. Failing to classify is treated as overreach.

- **Established fact**: verifiable, cited at A or B tier, dated.
- **Strategic hypothesis**: a position the team holds with stated reasoning but no external citation yet. Flag in prose ("we expect…", "hypothesis:").
- **Proposed show / business mechanic**: a working design intended to be tested in pilot or financing. Flag in prose ("proposed:", "working assumption:") and surface in Open Questions.

The scaffold is not gospel. Anything in `status: draft` that survives without explicit re-classification at `status: validated` time is treated as a proposal, not a fact.

### Section Conventions

- **Purpose**: what this doc enables. Not what the topic is.
- **Key Takeaways**: extractable bullets; will be lifted into briefs.
- **Core Content**: the substance.
- **Evidence / Sources**: every external claim, with a reliability tier.
- **Objections Answered**: the toughest investor / broadcaster / fan pushbacks and our responses.
- **Website Implications**: how this doc shows up on the live site.
- **Open Questions**: gaps the next contributor should close.
- **Change Log**: dated entries; append-only.

### Linking Rules

- Use relative paths: `[show premise](../02_show_bible/show_premise.md)`.
- When a concept exists, link rather than redefine.
- Inbound links matter. When you create a file, find at least one upstream file that should link to it and add the link.

### Atomicity & Splitting

If a single file accumulates more than ~800 lines or covers more than one decision domain, split it. Example: `business_model.md` was correctly split into `revenue_model.md`, `sponsorship_inventory.md`, `franchise_flywheel.md`, etc.

### Source Material vs Digest

- `10_source_material/` contains raw inputs: transcripts, screenshots, decks, notes. These files may be informal but still need frontmatter.
- All digested, analytical content lives in `01_–09_*` folders.
- Never inline a long transcript into an analytical doc, link to the source file instead.

### Outputs

- `11_outputs/` is for generated artifacts (website copy, design prompts, cursor task lists).
- Every output file's frontmatter must list `generated_from:` with the upstream files used.
- When upstream changes, the output is stale until regenerated; mark it `status: deprecated` until refreshed.

### Archive

- Never delete a file that has been referenced externally. Move it to `99_archive/` and update frontmatter with `status: deprecated` and `supersedes:` pointing to the replacement.

## Evidence / Sources

Not applicable. This is a system rules file. Its authority derives from project owners, not external sources.

## Objections Answered

| Objection | Response |
| --- | --- |
| "This is too much structure for an early project." | Structure is the cheapest insurance against context loss. Adding it later is 10x more expensive than enforcing it now. |
| "Agents won't follow these rules." | Agents are explicitly briefed on `00_system/` first. Violations are caught at PR review. |
| "Frontmatter slows me down." | Use `00_system/document_template.md`. It's a 10-second copy. |

## Website Implications

Indirect: a well-structured KB is what allows the website to be generated from a single source of truth instead of hand-maintained. The site copy in `11_outputs/website_copy/` depends on these rules being followed upstream.

## Open Questions

- Should we enforce frontmatter validity with a pre-commit hook? (Owner: adamtday)
- Do we want a `language:` field for multi-territory rollout? (Likely yes once we hit international.)
- Should `Evidence / Sources` reliability tiers be standardised across the KB or per-folder? (See `00_system/source_reliability_rules.md`.)

## Change Log

- 2026-05-20, Initial rules drafted at repository creation.
- 2026-05-20, Added binding "no em dashes" rule. Added "Distinguishing Fact, Hypothesis, and Proposal" section. Softened the "no exceptions" frontmatter rule to acknowledge folder-index README and `.gitkeep` files.
