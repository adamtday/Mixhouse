---
doc_type: source
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [raw_notes, transcript, reference, screenshot, source_index]
related:
  - 00_system/naming_conventions.md
  - 00_system/source_reliability_rules.md
---

# Source Material

## Purpose

Hold the raw, undigested inputs that fuel the analytical and creative work elsewhere in the KB — transcripts, notes, pitch deck exports, reference images, and screenshots. Nothing in here is canonical; everything in here is the trace evidence behind canonical files.

## Key Takeaways

- All files in this folder follow the date-prefixed naming convention in `00_system/naming_conventions.md`.
- Files here are *referenced* from analytical docs; they are not duplicated.
- Each subfolder has a focused purpose.
- Frontmatter is still mandatory even for raw notes.

## Core Content

### Subfolders

| Subfolder | Contents |
| --- | --- |
| `raw_notes/` | Plain-text observations, workshop notes, brainstorm dumps. |
| `transcripts/` | Full transcripts from calls, interviews, advisor conversations. |
| `pitch_decks/` | Versioned pitch deck exports (PDF / Keynote / PPT). |
| `references/` | External references (PDFs of reports, screenshots of articles, photographs). |
| `screenshots/` | Frame grabs and competitor-product screenshots. |

### Naming Convention

`YYYYMMDD_short_topic.ext` — example: `20260412_advisor_call_p_gou.md`.

### Frontmatter for Source Files

Even raw notes use frontmatter:

```yaml
---
doc_type: source
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: YYYY-MM-DD
retrieval_tags: [raw_notes, ...]
source_type: raw_notes | transcript | reference | screenshot
related: [paths to analytical files that cite this]
---
```

### How Source Files Get Used

1. A source file is captured here (e.g. a transcript of an advisor call).
2. An analytical file in `01–09_*` cites it under Evidence / Sources.
3. The source file's frontmatter `related:` lists the analytical files referencing it.
4. When superseded or no longer relevant, move to `99_archive/` (do not delete).

### What Doesn't Go Here

- Final, polished assets used on the public site (those live in the web project's `public/media/`).
- LLM output dumps — those should be digested into the right analytical folder.
- Confidential documents not appropriate for the team-shared repo (those live in restricted-access storage).

## Evidence / Sources

Not applicable — this is an index file.

## Objections Answered

| Objection | Response |
| --- | --- |
| "Why frontmatter on raw notes?" | Because retrieval needs to work even for informal content. |
| "Will this folder bloat?" | Yes, deliberately. Bloat is OK if it's queryable. |

## Website Implications

Indirect — references here feed `Evidence / Sources` rows on every analytical file the site eventually surfaces.

## Open Questions

- Storage strategy for large binary references (PDFs, images) — possibly LFS or external storage with a pointer.

## Change Log

- 2026-05-20 — Initial source-material folder index created.
