---
doc_type: source
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-25
retrieval_tags: [references, primary_sources, reports, visual_references, source_index, raw_inputs, capture_workflow, taxonomy_tagging]
related:
  - 10_source_material/README.md
  - 10_source_material/articles/README.md
  - 10_source_material/screenshots/README.md
  - 10_source_material/reference_capture_workflow.md
  - 04_competitive_landscape/reference_taxonomy.md
  - 04_competitive_landscape/reference_analysis_template.md
  - 04_competitive_landscape/visual_reference_analysis.md
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

## Capture Standards

Reference capture standards inherit the screenshot capture standards in `10_source_material/screenshots/README.md` and extend them for binary assets:

- **Native fidelity for binary assets.** PDFs are captured as published (no re-rendering, no compression). ZIP archives preserve original file structure. Image references preserve original resolution and bit depth.
- **Companion `.md` is mandatory for binary assets.** Unlike screenshots (where the companion `.md` is conditional on editorial significance), references always carry a companion `.md` with full frontmatter, attribution, and taxonomy tags.
- **Sequence references.** When a reference is part of a published series (annual reports, campaign sequences, format-bible versions), preserve sequence numbering in the filename and cross-link companion `.md` files.
- **Type specimen captures.** When ingesting type-specimen PDFs or images, capture both the foundry-published specimen and a context-of-use capture showing the type in real editorial use.
- **Visual-reference frame grabs.** Frame-grab compilations are preferred as ZIP archives with a manifest in the companion `.md`. Individual high-impact frames may also live as standalone images.

## Tagging Conventions

Every reference is tagged against `04_competitive_landscape/reference_taxonomy.md` in its companion `.md` frontmatter. Tagging discipline matches the screenshots README pattern:

```yaml
taxonomy:
  primary_category: {category_slug}
  secondary_categories: [{category_slug}, {category_slug}]
  reference_class: {prestige_unscripted | scene_credible_electronic | residency_life | music_doc | crossover_aesthetic, optional}
```

References that map to one of the five reference classes in `04_competitive_landscape/visual_reference_analysis.md` live in the corresponding sub-folder under `visual_references/` (see Folder Taxonomy below) and carry the matching `reference_class` tag. References that do not map to a reference class still carry primary and secondary category tags from the taxonomy.

Primary-source reports (`references/primary_sources/`) typically carry `primary_category: prestige_unscripted` for category-relevant reports or `executive_persuasion` for investor-grade research; secondary categories surface the topic ("market_sizing", "audience_demographics", "festival_economics").

## Annotation Guidance

Companion `.md` body content (below frontmatter) carries annotation when the reference will inform analysis. Annotation discipline matches the screenshots README:

- Lead with observation and mechanism, not impression.
- Connect to canonical work; name the canonical file the reference informs.
- Identify the refusal (what should NOT translate to MixHouse).
- Keep annotations load-bearing; three to six paragraphs for a meaningful reference, longer for primary-source reports with multiple analytical extracts.
- No em dashes.
- For primary-source reports, the annotation includes a Key Extracts section listing the specific figures, charts, or claims that downstream analytical files will cite.

Worked annotation examples for visual references live in `10_source_material/reference_capture_workflow.md`. Worked annotation patterns for primary-source reports live in `03_market_research/research_source_registry.md`.

## Anti-Noise Rules

Refuse the following ingestion patterns:

- **Aggregator-sourced reference assets.** Pinterest boards, Are.na collections, and similar aggregators obscure attribution and lose creator context. Capture from the original source with full attribution.
- **AI-generated reference assets without disclosure.** Generative output may be cited as a reference only with explicit attribution to the generative system and a note on what the output demonstrates (typically: an anti-pattern or a category exploration).
- **Sub-publication-quality scans.** Low-resolution scans of published material degrade reference fidelity. Source the publication-quality PDF or capture from the original at native resolution.
- **Trade-press summaries when the primary source is available.** Per `00_system/source_reliability_rules.md`, primary-source PDFs are preferred to trade-press summaries when available. Trade-press is captured into `10_source_material/articles/`, not into `references/primary_sources/`.
- **Visual-reference dumps without curation.** Bulk frame-grab archives without companion `.md` files become unindexed material. Every ZIP archive carries a companion `.md` with a manifest and tagged extracts.
- **Duplicate ingestion of the same primary source across multiple annual cycles without supersession.** When IFPI 2027 lands, mark IFPI 2026 as `status: deprecated`, move to `99_archive/references/primary_sources/`, and cross-link the new edition in the deprecated companion `.md`.

## Folder Taxonomy

Top-level structure of `10_source_material/references/`:

```
10_source_material/references/
  primary_sources/
    {YYYYMMDD_source_topic.pdf}            # institutional/industry-body reports
    {YYYYMMDD_source_topic.md}             # companion annotations and Key Extracts
  formats/
    {YYYYMMDD_source_topic.md|pdf}         # format bibles and production documents
  legal/
    {YYYYMMDD_source_topic.pdf|md}         # legal and rights templates
  visual_references/
    prestige_unscripted/
      {YYYYMMDD_source_topic.{ext}}
      {YYYYMMDD_source_topic.md}
    scene_credible_electronic/
      {YYYYMMDD_source_topic.{ext}}
      {YYYYMMDD_source_topic.md}
    residency_life/
      ...
    music_doc/
      ...
    crossover_aesthetic/
      ...
```

The `visual_references/` sub-structure mirrors the five reference classes in `04_competitive_landscape/visual_reference_analysis.md`. References that map to multiple reference classes live under their primary class with cross-links in the companion `.md` `related:` frontmatter.

`primary_sources/`, `formats/`, and `legal/` do not subdivide by category; the source short name carries the categorisation in the filename, and the companion `.md` carries the taxonomy tags. Sub-folders within these may be added when a source family exceeds twenty references (for example, an IFPI sub-folder once multiple IFPI publications across multiple years are ingested).

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
6. Follow the full five-stage workflow in `10_source_material/reference_capture_workflow.md` (capture, attribute, classify, link, review). References without taxonomy tags or canonical linkage are downgraded to `status: deprecated` after 30 days.
7. For visual references promoted from `screenshots/`, retain the original screenshot in place and cross-link the curated reference via the companion `.md` `related:` frontmatter on both sides.

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
- 2026-05-25, Phase 2.5 reference-ingestion expansion. Added Capture Standards, Tagging Conventions, Annotation Guidance, Anti-Noise Rules, and Folder Taxonomy sections. Added cross-links to `04_competitive_landscape/reference_taxonomy.md`, `04_competitive_landscape/reference_analysis_template.md`, and `10_source_material/reference_capture_workflow.md`. Extended ingestion rules with the five-stage workflow gate and the screenshots-to-curated-reference promotion linkage.
