---
doc_type: template
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [template, research, prompts, anti_generic, citations]
related:
  - 00_system/kb_rules.md
  - 00_system/source_reliability_rules.md
  - 00_system/document_template.md
---

# Research Prompt Template

## Purpose

Provide the canonical prompt scaffold used when instructing an AI agent (Claude, Perplexity, GPT, internal research subagent) to produce or extend a research file in this KB. Following this template keeps research outputs citation-honest, formatting-consistent, and free of generic startup prose.

## Key Takeaways

- Always specify destination file, audience, and reliability tier requirements.
- Force the agent to use the section structure from `00_system/document_template.md`.
- Ban the generic phrase list. Demand numbers, dates, and named sources.
- Require explicit `Open Questions` whenever evidence is thin.

## Core Content

### Standard Prompt Skeleton

Use this as the system / instruction block when delegating research:

```
You are a research analyst contributing to the MixHouse knowledge base.

PROJECT CONTEXT
MixHouse is a cinematic electronic-music reality format and franchise. The
KB is a markdown repository optimised for AI retrieval. Read these files
before writing anything:

- 00_system/kb_rules.md
- 00_system/source_reliability_rules.md
- 00_system/document_template.md
- 01_master_context/mixhouse_master_thesis.md
- 01_master_context/one_sentence_positioning.md
- Any related files listed under `related:` in the destination file.

TASK
Populate (or extend) the file at: {destination_path}.
Topic scope: {one-sentence scope statement}.
Audience for downstream artifacts: {investor | broadcaster | advisor |
production | internal team | public site visitor}.
Minimum reliability tier for cited numbers: {A | B | A_or_B}.

OUTPUT FORMAT
- Strict markdown. Use the section structure from 00_system/document_template.md
  exactly: Purpose, Key Takeaways, Core Content, Evidence / Sources,
  Objections Answered, Website Implications, Open Questions, Change Log.
- Include YAML frontmatter with all required fields.
- Use tables for any enumerable comparison.
- Every numeric or factual claim has an inline footnote referencing a row
  in the Evidence / Sources table.

CITATION RULES
- Use the reliability tiers from 00_system/source_reliability_rules.md.
- A-tier: primary, audited, official.
- B-tier: reputable trade press citing primary data.
- C-tier: unverified secondary.
- assumption: internal estimate. Flag in frontmatter `assumption: true`.
- Never cite Wikipedia or LLM output as evidence.

ANTI-GENERIC RULES
Do not use any of the banned phrases listed in this file's "Banned Phrase
List". Replace with concrete, dated, or sourced claims.

PUNCTUATION RULES
No em dashes (`—`) anywhere in the output. Use periods, commas, colons,
or parentheses instead. This is binding.

CLAIM CLASSIFICATION
For every load-bearing claim, classify it as one of:
  - established fact (cited at A or B tier)
  - strategic hypothesis (team position, no citation yet)
  - proposed show / business mechanic (working design to test)
Use these labels in prose where the distinction matters. Do not let a
hypothesis or proposal pass as established fact.

UNCERTAINTY
If you cannot find an A or B source for a claim required by the task,
move that claim to `Open Questions` and continue. Do not fabricate.

DELIVERABLE
A single markdown file at {destination_path}, ready to commit. Add a
Change Log entry dated YYYY-MM-DD with your agent identifier.
```

### Banned Phrase List

Avoid these phrases entirely. They signal generic AI output and dilute investor confidence.

- "In today's fast-paced world"
- "Revolutionary"
- "Game-changing" / "Game changer"
- "Disruptive"
- "Cutting-edge"
- "Synergy" / "Synergies"
- "Leverage" (as a verb, except in the technical financial sense)
- "Best-in-class"
- "World-class" (unless attributable to a named third party)
- "Engaging" / "Engagement-driven"
- "Unleash" / "Unlock the power of"
- "At the intersection of"
- "Where X meets Y" (as a tagline)
- "Empower" / "Empowering"
- "Authentic" used about ourselves (let others say it)
- "Passion" / "Passionate" as a brand claim
- "Journey" (as in "the user's journey")
- "Solutions" (as a generic noun)
- "Ecosystem" used loosely
- "Curate" / "Curated" used loosely (acceptable when literal)
- "Premium" without a defined premium feature
- "Next-generation"
- "Bridging the gap"
- "Future of [X]" headlines

Note: this list governs public-facing prose and analytical writing. The phrases may still appear inside *quoted* internal vocabulary (e.g. when a strategy doc references "multi-format franchise IP" as a working term), provided the quote is clearly internal-shorthand and not export to the public site.

If a phrase is genuinely the right word, justify it in a comment in the file. Otherwise replace it.

### Required Specificity

Every assertion should answer at least one of:
- **Who?** (named person, brand, broadcaster)
- **How many?** (number with unit)
- **When?** (date or window)
- **Where?** (geography or platform)
- **How do we know?** (cited source)

Sentences that fail all five are removed.

### Tables Over Prose

When comparing options, scenarios, audiences, competitors, or numbers, use a markdown table. Prose comparisons rot fast.

### Linking Discipline

When the research touches a concept defined elsewhere in the KB, link to that file inline (`[contestant archetypes](../02_show_bible/contestant_archetypes.md)`). The agent should also propose 1–3 inbound links: existing files that should reference this new one.

### Research Provenance

Include in frontmatter:

```yaml
research_agent: {claude-3.5 | claude-opus-4.7 | perplexity | manual | other}
research_completed: YYYY-MM-DD
generated_from: [list of upstream files]
```

## Evidence / Sources

Not applicable. Template.

## Objections Answered

| Objection | Response |
| --- | --- |
| "The banned list is too restrictive." | Most banned phrases are placeholders for missing thought. Replacing them forces specificity. |
| "Cite-or-flag slows research." | The alternative is investors finding our errors. |

## Website Implications

Every research file feeding the website's `business_model`, `the_world`, or `the_show` pages must pass these rules before its content is lifted into `11_outputs/website_copy/`.

## Open Questions

- Should we maintain a separate "preferred sources" allowlist (e.g. MIDiA, IFPI, Parrot Analytics) to seed research subagents?
- Do we want an automated linter to flag banned phrases at commit time?

## Change Log

- 2026-05-20, Initial template and banned-phrase list written.
- 2026-05-20, Added Punctuation Rules (no em dashes), Claim Classification (fact / hypothesis / proposal), and clarified that the banned-phrase list applies to public and analytical prose, not internal vocabulary quoted as such.
