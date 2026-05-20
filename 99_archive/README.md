---
doc_type: system_rules
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [archive, deprecated, audit_trail]
related:
  - 00_system/kb_rules.md
  - 00_system/naming_conventions.md
---

# Archive

## Purpose

Hold superseded files so the project preserves an auditable history of how decisions and positioning evolved. Nothing here is canonical; everything here is a trace.

## Key Takeaways

- Files move here when they're superseded; they are not deleted.
- Every archived file has `status: deprecated` and either `supersedes` or `superseded_by` in frontmatter.
- The archive is searchable but does not appear in any retrieval boot sequence.

## Core Content

### When to Archive

- A file is split into two and the original becomes redundant.
- A file's content is replaced by a structurally different new file.
- An artifact is regenerated and the old version is no longer current.
- A position is updated and the prior position should be preserved for audit.

### How to Archive

1. In the source file's frontmatter, set `status: deprecated` and add `superseded_by: <relative path>`.
2. Move the file to `99_archive/` preserving its original folder structure where relevant (`99_archive/02_show_bible/old_premise.md`, etc.).
3. In the replacing file, add `supersedes: <archive path>` to frontmatter.
4. Add a Change Log entry in both files.

### Browsing the Archive

- Sub-organised by original folder structure where helpful.
- All files retain frontmatter and section structure.

### What Doesn't Belong Here

- Raw source material (that's `10_source_material/`).
- Active outputs (those stay in `11_outputs/` until superseded).
- Files that were never canonical, those are deleted, not archived.

## Evidence / Sources

Not applicable.

## Objections Answered

| Objection | Response |
| --- | --- |
| "Why not just use git history?" | Git history doesn't preserve cross-link integrity. The archive does. |

## Website Implications

None directly. The archive is internal.

## Open Questions

- Annual archive review, should we remove files past a certain age?

## Change Log

- 2026-05-20, Archive folder index created.
