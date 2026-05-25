---
doc_type: source
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-24
retrieval_tags: [references, primary_sources, reports, visual_references, source_index, raw_inputs]
related:
  - 10_source_material/README.md
  - 10_source_material/articles/README.md
  - 10_source_material/screenshots/README.md
  - 00_system/naming_conventions.md
  - 00_system/source_reliability_rules.md
  - 03_market_research/research_source_registry.md
---

# `10_source_material/references/`

## Purpose

Hold external reference documents that underwrite analytical files: primary-source reports (IFPI, MIDiA, Pollstar, Parrot, Spotify Loud and Clear), industry-body publications, format bibles or production documents from comparable shows, and visual references that inform the brand world and cinematography decisions.

This folder is the parent home for `references/` and `visual_references/` content; do not create a parallel `visual_references/` folder. Visual references are organised under a `visual_references/` subsection of this folder.

## What Belongs Here

### Primary-source reports (`references/primary_sources/`)

- IFPI Global Music Report, IFPI Engaging With Music.
- MIDiA Research reports (when license permits archival).
- Pollstar Year-End Worldwide.
- PwC Global Entertainment and Media Outlook.
- Parrot Analytics demand reports.
- Spotify Loud and Clear, Equity Reports.
- Platform-published reports (YouTube Culture and Trends, TikTok For Business What's Next).
- Live Nation, AEG annual reports.

### Format and production documents (`references/formats/`)

- Format bibles (where publicly available; e.g., `Idol` format-sale public summaries).
- Production-process documentation from comparable shows (DP interviews compiled, behind-the-scenes books).
- Reality-format format-rule guides.

### Visual references (`references/visual_references/`)

- Cinematography references (frame grabs and frame-grab compilations from prestige unscripted, scene-credible electronic, music documentary).
- Brand and fashion references (campaign images, look-books).
- Design references (Bottega Veneta campaigns, Apple product films, Cercle visual identity).
- Editorial cinema references (concert films, music documentary screenshots).

### Other reference documents

- Sponsorship category data (IEG, IAB, WARC excerpts).
- Legal and rights templates from comparable industries (where publicly available).
- Academic research on music discovery, audience behaviour, prestige unscripted economics.

## What Does Not Belong Here

- Journalistic articles (those live in `articles/`).
- Screenshots of competitor websites or product UIs (those live in `screenshots/`).
- Quantitative data extracts (CSV, XLSX); those live in `stats/`.
- Original photography or assets created for MixHouse (those live in the web project's assets or `11_outputs/`).

## Naming Convention

`YYYYMMDD_source_short_topic.{pdf|md|jpg|png}`

Subdirectory:
- `references/primary_sources/` for institutional and industry-body reports.
- `references/formats/` for format bibles and production-process documents.
- `references/visual_references/` for cinematography, brand, fashion, and design references.
- `references/legal/` for legal and rights templates.

Examples:
- `references/primary_sources/20260415_ifpi_global_music_report_2026.pdf`
- `references/formats/20260420_idol_format_overview_public.md`
- `references/visual_references/20260512_cercle_pyramids_frame_grabs.zip`
- `references/visual_references/20260518_bottega_veneta_ss26_campaign.jpg`
- `references/legal/20260601_uk_unscripted_talent_contract_template.pdf`

## Frontmatter Schema (For Companion `.md` Files Describing The Reference)

Binary files (PDF, JPG, PNG, ZIP) sit alongside a companion `.md` file that carries the frontmatter. The companion file shares the binary's name with `.md` extension.

```yaml
---
doc_type: source
status: draft
confidentiality: internal | restricted
owners: [adamtday]
last_reviewed: YYYY-MM-DD
retrieval_tags: [reference, source_short_name, topic_tag]
source_type: reference
reference_category: primary_source | format_document | visual_reference | legal_template | other
related:
  - {analytical files that cite this reference}
attribution:
  source: {named institution or publication}
  source_tier: A | B | C
  date_published: YYYY-MM-DD
  date_accessed: YYYY-MM-DD
  url: {original URL if applicable}
  license_constraints: {redistribution, archival, or use constraints}
---
```

## Source-Quality Expectations

References inherit tier from their source per `00_system/source_reliability_rules.md`:

- **A-tier**: IFPI, MIDiA, Luminate, Pollstar Year-End, Nielsen, BARB, Parrot Analytics, Spotify Loud and Clear, Live Nation annual report.
- **B-tier**: Trade-press analysis reports, IQ Magazine European Festival Report, format-sale public summaries.
- **C-tier**: Aggregator content, marketing-blog reports, unverified competitor materials.
- Visual references are tier-neutral; their value is editorial-decision support, not factual claim support.

## Ingestion Rules

1. Capture both the binary file and a companion `.md` frontmatter file.
2. License constraints are critical for primary-source reports. Many institutional reports (MIDiA, Parrot, Luminate) carry redistribution constraints; document those at ingestion to avoid downstream license violations.
3. Cross-link to `03_market_research/research_source_registry.md` for the parent source row.
4. For visual references, organise within `visual_references/` by reference class per `04_competitive_landscape/visual_reference_analysis.md`.
5. Per `00_system/source_reliability_rules.md`, primary-source PDFs are preferred to trade-press summaries when available.

## Visual References Subsection

The `visual_references/` subdirectory is structured to mirror the reference classes in `04_competitive_landscape/visual_reference_analysis.md`:

- `visual_references/prestige_unscripted/` (frame grabs, BTS images, DP interview compilations).
- `visual_references/scene_credible_electronic/` (Cercle, Boiler Room, RA sessions, festival livestreams).
- `visual_references/residency_life/` (Love Island, Real World retrospective).
- `visual_references/music_doc/` (Avicii, Daft Punk, Renaissance, concert-film grammar).
- `visual_references/crossover_aesthetic/` (Bottega Veneta, Apple, Pirelli, Aphex Twin / Warp).

Each subdirectory contains the binary references plus companion `.md` files.

## Archival Rules

- Primary-source reports are time-stamped; do not delete superseded reports when a new annual edition replaces them. Move to `99_archive/references/primary_sources/` with a Change Log entry.
- Visual references inform brand-world decisions over time. When a reference is no longer informing the brand world, mark `status: deprecated` and move to `99_archive/references/visual_references/` rather than delete.
- For very large binary collections (e.g., complete frame-grab compilations), consider whether to move to external storage to keep the git repository performant.

## How These Connect Back

References here are cited from analytical files via Evidence rows or directly referenced in the relevant brand-world / cinematography file:

```markdown
| 1 | "Global recorded music revenue 2025" | `../10_source_material/references/primary_sources/20260415_ifpi_global_music_report_2026.pdf` | 2026-04-15 | A |
```

Visual references are typically cited from `07_brand_world/moodboard_references.md` and `04_competitive_landscape/visual_reference_analysis.md` rather than from Evidence rows.

## Change Log

- 2026-05-24, Initial references folder README created as part of Phase 2 source-material directory hygiene. Folder absorbs the previously-considered separate `visual_references/` folder as a subdirectory; includes structure for primary-source reports, format documents, visual references, and legal templates.
