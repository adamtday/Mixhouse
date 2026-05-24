---
doc_type: output
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [outputs, generated, artifact_index]
related:
  - 00_system/agent_workflow.md
  - 00_system/naming_conventions.md
---

# Outputs

## Purpose

Hold every generated artifact derived from the analytical KB, website copy, design prompts, dev task lists, investor decks. These are derivative files; they are not canonical content.

## Key Takeaways

- Every file here lists `generated_from:` in frontmatter pointing to upstream source files.
- When upstream changes, downstream outputs become stale and are marked `status: deprecated` until refreshed.
- Outputs in this folder are the working artifacts; the final deliverables (e.g. a built website, a PDF deck) live outside the repo.

## Core Content

### Subfolders

| Subfolder | Contents |
| --- | --- |
| `website_copy/` | Page-by-page final copy ready for the build. |
| `page_specs/` | Per-page production specifications (component-level, content slots). |
| `claude_design_prompts/` | Prompts crafted for Claude to generate designs / mockups / hero treatments. |
| `cursor_tasks/` | Cursor-friendly task lists for engineering work. |
| `investor_materials/` | Investor-facing artifacts: one-pagers, deck outlines, FAQ packs. |

### Naming Convention

`{audience}_{artifact}_{YYYYMMDD}.md`: example: `investor_one_pager_20260520.md`.

### Required Frontmatter Additions for Outputs

```yaml
---
doc_type: output
status: draft
confidentiality: investor | internal | public
owners: [...]
last_reviewed: YYYY-MM-DD
retrieval_tags: [...]
generated_from: [list of upstream files]
generation_agent: {claude | manual | other}
generation_date: YYYY-MM-DD
---
```

### Workflow

1. Identify the upstream files (3–7 typically).
2. Run the appropriate prompt (see `00_system/research_prompt_template.md` for research; design prompts here for design).
3. Place output in the right subfolder with full frontmatter.
4. Cite numbers via the upstream evidence rows.
5. Re-generate when upstream changes; mark old version `deprecated` and move to `99_archive/`.

## Evidence / Sources

Not applicable. Index file.

## Objections Answered

| Objection | Response |
| --- | --- |
| "Why separate generated content from canonical?" | Because canonical content should not be polluted by its own derivatives. |

## Website Implications

The website's final copy is the output of this folder, with `08_website_strategy/page_briefs/` as its primary upstream.

## Open Questions

- Pre-commit linter to flag stale `generated_from:` references.
- Whether to commit pdf/png exports here or only markdown working files.

## Change Log

- 2026-05-20, Initial outputs folder index created.
