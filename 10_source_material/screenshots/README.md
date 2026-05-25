---
doc_type: source
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-24
retrieval_tags: [screenshots, visual_references, source_index, raw_inputs]
related:
  - 10_source_material/README.md
  - 10_source_material/references/README.md
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

## Source-Quality Expectations

Screenshots are reference material, not factual evidence. They inform editorial and design decisions but typically do not appear in Evidence tables of analytical files. When they do appear (e.g., a screenshot of a Netflix subscriber-attribution callout in earnings commentary), they are cited at the tier of the underlying source:

- Earnings-call slide screenshot: A-tier (with the call as parent source).
- Streamer show-page screenshot: B-tier (informational, not authoritative).
- Brand campaign screenshot: B-tier (reference, not authoritative claim).

## Ingestion Rules

1. Date-captured in the filename is mandatory.
2. Source identifier in the filename is mandatory.
3. For screenshots that will be analysed editorially, create a companion `.md` with frontmatter and `related:` links.
4. Respect copyright constraints. Screenshots for internal-reference use are typically protected under fair use; downstream use (decks, public-facing copy) requires per-image clearance.
5. Avoid bulk-capturing entire websites; capture the specific frame or page that informs a decision.

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
