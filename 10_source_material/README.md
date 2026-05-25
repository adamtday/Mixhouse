---
doc_type: source
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-25
retrieval_tags: [raw_notes, transcript, reference, screenshot, quote, stat, article, source_index, capture_workflow]
related:
  - 00_system/naming_conventions.md
  - 00_system/source_reliability_rules.md
  - 03_market_research/research_source_registry.md
  - 10_source_material/reference_capture_workflow.md
  - 04_competitive_landscape/reference_taxonomy.md
  - 04_competitive_landscape/reference_analysis_template.md
---

# Source Material

## Purpose

Hold the raw, undigested inputs that fuel the analytical and creative work elsewhere in the KB, transcripts, notes, pitch deck exports, reference images, and screenshots. Nothing in here is canonical; everything in here is the trace evidence behind canonical files.

## Key Takeaways

- All files in this folder follow the date-prefixed naming convention in `00_system/naming_conventions.md`.
- Files here are *referenced* from analytical docs; they are not duplicated.
- Each subfolder has a focused purpose.
- Frontmatter is still mandatory even for raw notes.

## Core Content

### Subfolders

| Subfolder | Contents | Folder README |
| --- | --- | --- |
| `raw_notes/` | Plain-text observations, workshop notes, brainstorm dumps. Anonymous and off-record material lives here. | (none yet) |
| `transcripts/` | Full transcripts from calls, interviews, advisor conversations, meetings, panels, podcast recordings. Parent home for all interview and recorded-exchange content. | `transcripts/README.md` |
| `pitch_decks/` | Versioned pitch deck exports (PDF / Keynote / PPT). | (none yet) |
| `references/` | External reference documents: primary-source reports (IFPI, MIDiA, Pollstar), format documents, visual references (cinematography, brand, fashion, design), legal templates. Parent home for visual references. | `references/README.md` |
| `screenshots/` | Raw frame captures of websites, show pages, UIs, moodboard sources, social-media posts. Promote into `references/visual_references/` after editorial review. | `screenshots/README.md` |
| `quotes/` | Attributable quotes from named contributors, advisors, partners, press, panel discussions. Excerpted from `transcripts/` or captured from press / public talks. | `quotes/README.md` |
| `stats/` | Quantitative source artefacts (CSVs, dashboard screenshots, PDF table extracts) that underwrite numerical claims. | `stats/README.md` |
| `articles/` | Archival copies of press articles, trade-publication coverage, scene editorial, substack journalism. | `articles/README.md` |

Per-folder READMEs detail what belongs there, naming conventions, frontmatter schema, source-quality expectations, ingestion rules, archival rules, and how files connect back into canonical analytical docs.

### Top-Level Workflow

`reference_capture_workflow.md` codifies the end-to-end five-stage workflow (capture, attribute, classify, link, review) that every reference passes through before it informs canonical analysis. Any agent ingesting visual, cinematic, editorial, or interaction reference material into this folder must follow that workflow. Taxonomy classification is defined in `04_competitive_landscape/reference_taxonomy.md`; per-reference analysis is defined in `04_competitive_landscape/reference_analysis_template.md`.

### Naming Convention

`YYYYMMDD_short_topic.ext`: example: `20260412_advisor_call_p_gou.md`.

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
- LLM output dumps, those should be digested into the right analytical folder.
- Confidential documents not appropriate for the team-shared repo (those live in restricted-access storage).

## Evidence / Sources

Not applicable. This is an index file.

## Objections Answered

| Objection | Response |
| --- | --- |
| "Why frontmatter on raw notes?" | Because retrieval needs to work even for informal content. |
| "Will this folder bloat?" | Yes, deliberately. Bloat is OK if it's queryable. |

## Website Implications

Indirect, references here feed `Evidence / Sources` rows on every analytical file the site eventually surfaces.

## Open Questions

- Storage strategy for large binary references (PDFs, images), possibly LFS or external storage with a pointer.

## Change Log

- 2026-05-20, Initial source-material folder index created.
- 2026-05-24, Phase 2 source-material directory hygiene. Added three new subfolders (`quotes/`, `stats/`, `articles/`) with per-folder READMEs. Added per-folder READMEs to `transcripts/`, `references/`, `screenshots/` reusing existing folders rather than creating parallel `interview_transcripts/` or `visual_references/` directories. Cross-link to `03_market_research/research_source_registry.md` added.
- 2026-05-25, Phase 2.5 reference-ingestion expansion. Added `reference_capture_workflow.md` top-level workflow file. Added Top-Level Workflow section pointing to the five-stage workflow plus taxonomy and analysis-template anchors in `04_competitive_landscape/`.
