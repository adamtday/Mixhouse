---
doc_type: source
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-25
retrieval_tags: [screenshots, visual_references, source_index, raw_inputs, capture_workflow, taxonomy_tagging]
related:
  - 10_source_material/README.md
  - 10_source_material/references/README.md
  - 10_source_material/reference_capture_workflow.md
  - 04_competitive_landscape/reference_taxonomy.md
  - 04_competitive_landscape/reference_analysis_template.md
  - 00_system/naming_conventions.md
  - 00_system/source_reliability_rules.md
---

# `10_source_material/screenshots/`

## Purpose

Hold screen captures of websites, visual references, moodboards, deck captures, UI examples, and any frame-level visual content that informs design, brand-world, format, or competitive analysis. This folder is the home for screen-captured visual material that does not belong in `references/visual_references/` (which holds cinematography and curated visual reference compilations).

The distinction between `screenshots/` and `references/visual_references/`: `screenshots/` is the raw-capture inbox; `references/visual_references/` is the curated and analysed reference set. Screenshots may be promoted into `references/visual_references/` after editorial review.

## What Belongs Here

- Competitor and reference website screenshots (Cercle YouTube, Boiler Room, Drive to Survive landing page, Apple Music editorial pages).
- Show landing-page screenshots (Netflix show pages, broadcaster show pages).
- Investor-deck and partner-deck pages captured from external sources (with consent).
- UI examples for digital products that inform interactive surfaces (DSP interfaces, livestream platforms, ticketing flows).
- Moodboard screenshots from temporary external sources (Pinterest, Are.na boards, mood collections) when they inform a design decision.
- Frame grabs from films, shows, or music videos that inform brand-world or cinematography analysis.
- Social-media screenshots when the post itself is the reference (e.g., a producer's announcement post that becomes a creator-economy evidence row).

## What Does Not Belong Here

- Curated visual reference compilations with editorial analysis (those live in `references/visual_references/`).
- Internal product screenshots for MixHouse itself (those live in the web project's assets or `11_outputs/`).
- Personal photographs without attribution context (treat as raw notes or omit entirely).
- Article screenshots when the source is a journalistic article (capture the article in `articles/` instead).

## Naming Convention

`YYYYMMDD_source_short_topic.{png|jpg|webp}`

Examples:
- `20260415_cercle_youtube_pyramids_landing.png`
- `20260518_netflix_drive_to_survive_show_page.png`
- `20260601_apple_music_editorial_electronic_homepage.png`
- `20260615_bottega_veneta_campaign_ss26_lookbook_p3.jpg`
- `20260701_boiler_room_livestream_berlin_2025_frame.png`

If the screenshot is part of a series, suffix with `_p{n}`:
- `20260518_netflix_drive_to_survive_show_page_p1.png`, `_p2.png`, etc.

## Frontmatter Schema (Optional Companion `.md` File)

Most screenshots do not require a companion `.md` file. When a screenshot carries editorial significance (will be referenced from an analytical file, or analysed in `04_competitive_landscape/visual_reference_analysis.md`), create a companion `.md` with frontmatter:

```yaml
---
doc_type: source
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: YYYY-MM-DD
retrieval_tags: [screenshot, source_short_name, topic_tag]
source_type: screenshot
related:
  - {analytical files that reference this screenshot}
attribution:
  source: {website / show / publication / brand}
  url: {original URL if applicable}
  date_captured: YYYY-MM-DD
  capture_context: {brief note on why this was captured}
  license_considerations: {note copyright / trademark constraints for any downstream use}
---
```

## Capture Standards

Resolution and completeness are non-negotiable:

- **Resolution at native or higher.** Capture at native screen resolution; do not downsample. Hi-DPI displays produce the highest-fidelity captures and should be preferred when available.
- **Format selection.** PNG for hard-edged UI, type specimens, and editorial spreads where pixel-level fidelity matters; JPG only when file-size constraint outweighs fidelity (rare); WEBP when both fidelity and compression matter and the downstream consumer supports it.
- **No browser chrome.** Capture the page content only; crop out browser address bar, tabs, and OS chrome unless the chrome itself is the subject of the capture (rare).
- **Sequence captures for interactions.** Multi-frame sequences when capturing an interaction, scroll behaviour, or transition. Three frames minimum (beginning, middle, end); five to seven for complex interactions.
- **Video reference handling.** For frames pulled from video sources, capture at native video resolution. For reference clips themselves, store the clip in restricted-access storage and keep only the still frames in the KB with citation pointing to the clip location.
- **Type specimen captures.** Capture type both at the size it appears in context and at a detail crop showing letterform construction.

## Tagging Conventions

Every screenshot that carries editorial significance is tagged against `04_competitive_landscape/reference_taxonomy.md` in its companion `.md` frontmatter. Tagging is the discipline that lets retrieval queries find the right slice of the reference set.

Tagging schema (in companion `.md`):

```yaml
taxonomy:
  primary_category: {category_slug}
  secondary_categories: [{category_slug}, {category_slug}]
  reference_class: {prestige_unscripted | scene_credible_electronic | residency_life | music_doc | crossover_aesthetic}
```

Tagging discipline:

- Primary category is exactly one. The dominant retrieval use determines the primary.
- Secondary categories are conservative; two to four is typical.
- `reference_class` applies only to cinematic references (the five-class scheme in `04_competitive_landscape/visual_reference_analysis.md`).
- `retrieval_tags` frontmatter list includes the source short name plus topic tags; primary and secondary taxonomy slugs are mirrored into `retrieval_tags` for compatibility with the wider tag vocabulary in `00_system/retrieval_tags.md`.

## Annotation Guidance

Companion `.md` body content (below frontmatter) carries annotation when the screenshot will inform analysis. Annotation discipline:

- **Lead with observation, not impression.** Describe the mechanism (lens choice, light, blocking, hierarchy, timing) before any aesthetic judgement.
- **Connect to canonical work.** State which canonical file the screenshot informs and what specific decision it supports or argues against.
- **Identify the refusal.** Name what should NOT translate from the captured material to MixHouse. This is the highest-value annotation field.
- **Keep it short and load-bearing.** Three to six paragraphs for a meaningful annotation; longer is rarely better.
- **No em dashes.** Repository-wide rule applies in companion files.

Worked annotation examples live in `10_source_material/reference_capture_workflow.md`.

## Anti-Noise Rules

Refuse the following capture patterns:

- **Bulk-capturing entire websites or albums.** Capture only the frames that inform a specific decision. If the decision is not yet known, do not capture.
- **Decontextualised image saves.** If the source attribution cannot be reconstructed at point of capture, do not capture. The source identity must survive into the filename.
- **Aggregator screenshots.** Captures from Pinterest, We Heart It, or similar aggregators obscure the original creator and lose attribution. Capture the original source instead.
- **Duplicate captures.** Before capturing, search existing screenshots for the same source-and-context. Promote existing captures via the workflow in `reference_capture_workflow.md` rather than recapture.
- **AI-generated reference imagery presented as captured.** Do not capture AI-generated material into the reference set. If AI-generated material must be referenced, it carries explicit attribution to the generative system.
- **Trend-chasing captures without retrieval intent.** A capture that does not connect to a canonical file becomes inbox sprawl. The intent question ("which canonical file will this inform?") is asked at point of capture, not later.
- **Single-frame captures of multi-frame interactions.** A scroll grammar or transition is not a single frame; capturing it as one degrades the asset.

## Folder Taxonomy

Top-level structure of `10_source_material/screenshots/`:

```
10_source_material/screenshots/
  {YYYYMMDD_source_topic.{ext}}              # binary captures
  {YYYYMMDD_source_topic.md}                 # companion annotations
```

Sub-folders are used sparingly. When the screenshot set within a single source reaches ten or more captures, create a source-named sub-folder:

```
10_source_material/screenshots/
  cercle_catalogue/
    20260518_cercle_pyramids_drone_master_p1.png
    20260518_cercle_pyramids_drone_master_p1.md
    20260601_cercle_versailles_opera_house_p1.png
    20260601_cercle_versailles_opera_house_p1.md
```

Screenshots that have been promoted to curated references move into `10_source_material/references/visual_references/{reference_class}/` per the promotion workflow in `reference_capture_workflow.md`. The raw screenshot stays in `screenshots/` as evidence; the curated reference is the analysed artefact.

## Source-Quality Expectations

Screenshots are reference material, not factual evidence. They inform editorial and design decisions but typically do not appear in Evidence tables of analytical files. When they do appear (e.g., a screenshot of a Netflix subscriber-attribution callout in earnings commentary), they are cited at the tier of the underlying source:

- Earnings-call slide screenshot: A-tier (with the call as parent source).
- Streamer show-page screenshot: B-tier (informational, not authoritative).
- Brand campaign screenshot: B-tier (reference, not authoritative claim).

## Ingestion Rules

1. Date-captured in the filename is mandatory.
2. Source identifier in the filename is mandatory.
3. For screenshots that will be analysed editorially, create a companion `.md` with frontmatter, taxonomy tags, and `related:` links.
4. Respect copyright constraints. Screenshots for internal-reference use are typically protected under fair use; downstream use (decks, public-facing copy) requires per-image clearance.
5. Avoid bulk-capturing entire websites; capture the specific frame or page that informs a decision.
6. Follow the full five-stage workflow in `10_source_material/reference_capture_workflow.md` for any screenshot intended to inform analysis. Screenshots captured without taxonomy classification and canonical linkage are downgraded to `status: deprecated` after 30 days.

## Archival Rules

- Screenshots age fast (websites redesign, show pages update). When a screenshot's reference value lapses (the redesigned page no longer matches the captured frame), mark `status: deprecated` and move to `99_archive/screenshots/` with a Change Log entry.
- For screenshots that have been promoted into `references/visual_references/` with editorial analysis, the original screenshot can stay here (raw) or move to the archive depending on retention judgement.
- Subscription-platform screenshots (paywalled article slides, gated dashboards) carry license constraints; respect them at archival time.

## How These Connect Back

Screenshots here are typically referenced from:

- `04_competitive_landscape/visual_reference_analysis.md` (when the screenshot informs a reference-class analysis).
- `04_competitive_landscape/cinematography_language.md` (when the screenshot illustrates a syntactic point).
- `07_brand_world/moodboard_references.md` (when the screenshot informs the brand-world moodboard).
- `07_brand_world/visual_positioning.md` (when the screenshot informs visual positioning).
- `08_website_strategy/page_briefs/*.md` (when the screenshot informs page-brief design decisions).

Screenshots referenced from `04_competitive_landscape/visual_reference_analysis.md` or `07_brand_world/moodboard_references.md` should be considered for promotion into `references/visual_references/` with full editorial analysis.

## Change Log

- 2026-05-24, Initial screenshots folder README created as part of Phase 2 source-material directory hygiene.
- 2026-05-25, Phase 2.5 reference-ingestion expansion. Added Capture Standards, Tagging Conventions, Annotation Guidance, Anti-Noise Rules, and Folder Taxonomy sections. Added cross-links to `04_competitive_landscape/reference_taxonomy.md`, `04_competitive_landscape/reference_analysis_template.md`, and `10_source_material/reference_capture_workflow.md`.
