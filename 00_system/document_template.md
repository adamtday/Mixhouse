---
doc_type: template
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [template, kb_rules, schema]
related:
  - 00_system/kb_rules.md
  - 00_system/research_prompt_template.md
assumption: false
---

<!--
HOW TO USE THIS TEMPLATE

1. Copy this file to its destination path.
2. Replace every section body. Keep the section headings exactly as written.
3. Fill in the frontmatter fully. Do not leave `status` as `template`.
4. Allowed `status` values: seed | draft | validated | stable | deprecated
5. Allowed `confidentiality` values: public | investor | internal | restricted
6. `retrieval_tags` should include 4–10 lowercase, snake_case tags.
7. Add at least one entry to the change log, even on initial creation.
-->

# {Title in Title Case}

## Purpose

State in 1–3 sentences what this document is for and what decision or artifact it should enable. Begin with a verb. Do not describe the topic — describe the document's job.

## Key Takeaways

- 3–7 bullets, each a complete sentence.
- Each bullet should be quotable on its own without surrounding context.
- Order by importance, not chronology.
- Avoid hedging language ("might", "could possibly").

## Core Content

The main body of the document. Use H3 (`###`) subheadings for sections, H4 (`####`) for sub-sections. Keep paragraphs short (2–4 sentences). Prefer tables and bullet lists for any enumerable content.

### {Subsection A}

### {Subsection B}

## Evidence / Sources

| # | Claim referenced | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | {short claim} | {URL or `10_source_material/path`} | YYYY-MM-DD | A / B / C / assumption |

See `00_system/source_reliability_rules.md` for reliability tiers.

## Objections Answered

| Objection (as a stakeholder would say it) | Response (one paragraph max) |
| --- | --- |
| | |

## Website Implications

How does the content of this document affect what appears on the public site? Reference page briefs in `08_website_strategy/page_briefs/` where relevant.

- Affects pages: {list of page brief files}
- Suggested copy or component changes: {short list}

## Open Questions

- {Question 1 — phrased as a question, with the file or person who can answer it.}
- {Question 2}

## Change Log

- YYYY-MM-DD — {author or agent name} — {summary of change}
