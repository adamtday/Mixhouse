---
doc_type: system_rules
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [agent_workflow, claude, cursor, github_agent, retrieval]
related:
  - 00_system/kb_rules.md
  - 00_system/retrieval_tags.md
  - 00_system/research_prompt_template.md
---

# Agent Workflow

## Purpose

Define the canonical operating protocol for Claude, Cursor, and GitHub coding agents working inside this repository so that their reads, edits, and outputs remain consistent across sessions and contributors.

## Key Takeaways

- Always load `00_system/` and `01_master_context/` before touching anything else.
- Prefer editing existing files over creating new ones; new files require a clear concept-to-file mapping.
- Every agent action that changes a file must update that file's `Change Log`.
- Outputs in `11_outputs/` reference their upstream files in frontmatter (`generated_from:`).
- When an agent lacks evidence for a claim, the claim goes to `Open Questions`, not into prose.

## Core Content

### Boot Sequence (every new agent session)

1. Read `README.md`.
2. Read `00_system/kb_rules.md`.
3. Read `00_system/naming_conventions.md`.
4. Read `00_system/source_reliability_rules.md`.
5. Read `00_system/retrieval_tags.md`.
6. Read `01_master_context/mixhouse_master_thesis.md`.
7. Read `01_master_context/one_sentence_positioning.md`.
8. Read `01_master_context/glossary.md`.
9. Then read the folder most relevant to the task.

### Task Classification

Agents should classify the user request into one of these task types before acting:

| Task type | Primary folders | Typical output |
| --- | --- | --- |
| Format / show question | `02_show_bible/`, `01_master_context/` | Updated show bible file or talking points. |
| Market / competitive question | `03_market_research/`, `04_competitive_landscape/` | Updated research doc, evidence table, or competitive matrix row. |
| Commercial question | `05_business_model/` | Updated model doc, investor case, or scenario. |
| Production question | `06_production_strategy/` | Updated production doc, risk register, or pipeline. |
| Brand / design question | `07_brand_world/`, `09_design_system/` | Updated brand or token doc. |
| Website question | `08_website_strategy/`, `09_design_system/` | Updated page brief, sitemap, or component requirement. |
| Generate artifact | `11_outputs/` | New or updated output file with `generated_from:` frontmatter. |
| Maintain repo | `00_system/`, `99_archive/` | Updated rule, template, or archived file. |

### Editing Rules

- Use the relevant tool (Edit for surgical changes; Write only for new files or full rewrites).
- Preserve all existing section headings unless explicitly told to restructure.
- Always update `last_reviewed:` and add a Change Log entry.
- If the change invalidates downstream outputs in `11_outputs/`, mark those outputs `status: deprecated`.

### Creating New Files

Only create a new file when:
- The concept does not already have a home in the existing folder map.
- Splitting an oversized file improves retrieval.
- An output artifact is being generated.

Procedure:
1. Copy `00_system/document_template.md`.
2. Fill frontmatter — including 4–10 valid `retrieval_tags`.
3. Add at least one inbound link from an existing file (so the new file is discoverable).
4. Add an entry to the relevant parent index (e.g. add to the README quick-start list if foundational).

### Generating Outputs

When asked to produce website copy, an investor one-pager, a design prompt, etc.:

1. Identify the source files (typically 3–7 upstream KB files).
2. Place result in the correct `11_outputs/` subfolder.
3. List sources in frontmatter under `generated_from:`.
4. Cite numbers using their tier from `00_system/source_reliability_rules.md`.
5. Never invent quotes, names, or partnerships.

### Confidentiality & Public Surface

Before writing copy destined for the public site:
- Confirm every cited file is `confidentiality: public` or has explicit approval.
- Strip any internal-only language (use the banned-phrase rules but in reverse for marketing voice).
- Run a final pass against `07_brand_world/tone_of_voice.md`.

### Handling Uncertainty

- Never fabricate ratings, deal sizes, or partner names.
- If asked for a number that isn't yet in the KB, route it to `Open Questions` and tell the user.
- Use `assumption: true` and the `assumption` reliability tier where appropriate.

### Multi-Agent / Subagent Use

When a task requires broad exploration (e.g. "summarise everything we know about Cercle"), spawn a subagent with a scoped read-only prompt and digest the result into the relevant analytical file. Do not paste raw subagent output into the KB.

### Commit Discipline

- One logical change per commit. Multiple files in one commit are fine if they form a single semantic update.
- Commit messages: `<area>: <imperative-verb> <object>` — e.g. `show_bible: add elimination logic v1`.
- Never commit raw model thinking or transcript dumps; those go in `10_source_material/` as their own files.

## Evidence / Sources

Not applicable — internal protocol.

## Objections Answered

| Objection | Response |
| --- | --- |
| "Loading 9 files before any task is wasteful." | The boot files are short (~300 lines combined). The cost of *not* reading them is generic, off-brand output. |
| "Why force outputs into `11_outputs/`?" | Separating sources from derivatives prevents the KB from poisoning itself when an output is wrong. |

## Website Implications

This document defines how the website itself is generated: page copy is an `11_outputs/website_copy/` artifact derived from `08_website_strategy/page_briefs/` plus brand and business model upstream files.

## Open Questions

- Should we formalise a Claude Skill in `.claude/skills/` that encodes this workflow?
- How do we keep `generated_from:` frontmatter in sync when upstream files move? (Possible answer: pre-commit linter.)

## Change Log

- 2026-05-20 — Initial workflow defined.
