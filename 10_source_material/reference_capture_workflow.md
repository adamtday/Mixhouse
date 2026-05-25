---
doc_type: source
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-25
retrieval_tags: [reference_capture, ingestion_workflow, source_material, screenshots, references, retrieval_consistency]
related:
  - 10_source_material/README.md
  - 10_source_material/references/README.md
  - 10_source_material/screenshots/README.md
  - 10_source_material/articles/README.md
  - 10_source_material/quotes/README.md
  - 10_source_material/stats/README.md
  - 04_competitive_landscape/reference_taxonomy.md
  - 04_competitive_landscape/reference_analysis_template.md
  - 00_system/naming_conventions.md
  - 00_system/source_reliability_rules.md
  - 00_system/canonical_dependency_map.md
---

# Reference Capture Workflow

## Purpose

Codify the end-to-end workflow for capturing visual, cinematic, editorial, and interaction references into the MixHouse KB. The workflow turns "I saw something useful" into a retrievable, attributed, taxonomy-tagged asset that downstream analysis (`04_competitive_landscape/reference_analysis_template.md`) and downstream brand-world work (`07_brand_world/visual_principles.md`, `07_brand_world/visual_positioning.md`) can build on.

Without a workflow, reference capture becomes inbox sprawl: screenshots without context, references without attribution, assets without retrievability. The workflow is the discipline that prevents that drift.

## Key Takeaways

- Capture is a workflow, not an instinct. The discipline is in attribution, taxonomy tagging, and canonical linkage, not in the screenshot itself.
- Every captured reference passes through five stages: capture, attribute, classify, link, review. Skipping any stage produces unindexed material.
- The workflow distinguishes raw capture (the screenshot or asset) from curated reference (the asset plus frontmatter, taxonomy tags, and canonical linkage). Both belong in the KB; they live in different places.
- "Good vs bad reference capture" is a learned skill. The examples in this file set the standard.
- The workflow defends against three failure modes: capture without attribution, attribution without taxonomy, and taxonomy without canonical linkage.

## Core Content

### The Five-Stage Workflow

#### Stage 1: Capture

Capture the asset itself. Two pathways:

- **Screenshot pathway.** Frame capture of a website, show, film, livestream, or product page. Lands in `10_source_material/screenshots/`.
- **Reference pathway.** External binary file (PDF, JPG, PNG, ZIP) or curated visual reference. Lands in `10_source_material/references/`.

Capture standards:

- Resolution at native or higher. For screenshots, capture at native screen resolution; do not downsample.
- For animated or video references, capture both a still frame and a short clip (when copyright permits). The clip lives in restricted storage; the still and the citation live in the KB.
- For interaction references, capture a sequence of three or more screenshots showing the interaction's beginning, middle, and end. Single-frame interaction captures are insufficient.
- For type specimens, capture the type at the size it appears in context plus a detail crop showing letterform construction.

#### Stage 2: Attribute

Attribute the source. This is where most reference capture fails.

Every captured asset carries attribution metadata, either inline in the filename (date prefix, source slug) or in a companion `.md` file (full frontmatter).

Filename attribution (mandatory):

```
YYYYMMDD_source_short_topic.{ext}
```

Examples:
- `20260520_apple_vision_pro_marketing_hero_p1.png`
- `20260520_the_gentlewoman_interview_spread_p2.png`
- `20260520_cercle_pyramids_drone_master_p3.png`

Companion `.md` attribution (required when the reference will be analysed):

```yaml
---
doc_type: source
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: YYYY-MM-DD
retrieval_tags: [reference, source_short_name, topic_tag]
source_type: screenshot | reference
attribution:
  source: {website / show / publication / brand}
  creator: {director / brand owner / designer / studio}
  url: {original URL if applicable}
  date_captured: YYYY-MM-DD
  capture_context: {brief note on why this was captured}
  license_considerations: {note copyright / trademark constraints for any downstream use}
---
```

Attribution must include:

- Source identifier (named institution, publication, brand, or work).
- Creator credit where applicable (director, designer, brand owner).
- URL for digital sources.
- Date captured.
- License considerations for any downstream use.

#### Stage 3: Classify

Classify against `04_competitive_landscape/reference_taxonomy.md`.

Add taxonomy tags to the companion `.md` frontmatter:

```yaml
taxonomy:
  primary_category: {category_slug}
  secondary_categories: [{category_slug}, {category_slug}]
  reference_class: {reference_class_slug, optional}
```

Tagging discipline:

- Primary category is exactly one. If the reference fits two categories equally, choose the one that aligns with the dominant retrieval use.
- Secondary categories are conservative. Two to four is typical; more than five suggests the reference is being inflated.
- Reference class (the five-class scheme in `04_competitive_landscape/visual_reference_analysis.md`) is optional and applies only to cinematic references.

#### Stage 4: Link

Link to canonical anchors.

Add the canonical files the reference informs to the companion `.md` `related:` frontmatter:

```yaml
related:
  - 04_competitive_landscape/cinematography_language.md
  - 07_brand_world/visual_principles.md
  - 08_website_strategy/page_briefs/the_world.md
```

Linkage rules:

- Every reference must link to at least one canonical or near-canonical file. References without linkage are decoration; they get downgraded to `status: deprecated` after 30 days.
- Linkage is bidirectional: when a canonical file cites a reference, the canonical file's Evidence table or References section names the asset path. When a reference informs a canonical file, the reference's `related:` lists that file.

#### Stage 5: Review

Editorial review before promotion to `status: draft`.

Review checklist:

- Capture standards met (resolution, completeness, sequence for interactions).
- Attribution complete (source, creator, URL, date, license).
- Taxonomy tags assigned and defensible.
- Canonical linkage present and reciprocated.
- Filename follows the date-prefix convention.
- No em dashes in any companion `.md` content.

Reviewer is the founder for high-impact references (brand-world informing), the EP for production references, or any designated owner for cluster contributions. Reviewed references promote from `status: seed` to `status: draft`.

### Folder Examples

#### Screenshots

```
10_source_material/screenshots/
  20260520_apple_vision_pro_marketing_hero_p1.png
  20260520_apple_vision_pro_marketing_hero_p1.md  (companion)
  20260520_apple_vision_pro_scroll_sequence_p2.png
  20260520_apple_vision_pro_scroll_sequence_p3.png
  20260520_apple_vision_pro_scroll_sequence_p4.png
  20260520_apple_vision_pro_scroll_sequence_p2.md  (companion, covers p2-p4)
  20260518_cercle_pyramids_drone_master_p1.png
  20260518_cercle_pyramids_drone_master_p1.md
  20260518_the_gentlewoman_interview_spread_p1.png
  20260518_the_gentlewoman_interview_spread_p1.md
```

Notes:

- A multi-frame sequence shares one companion `.md` file, named for the first frame in the sequence.
- Companion `.md` filename matches the binary's stem.

#### References

```
10_source_material/references/
  primary_sources/
    20260415_ifpi_global_music_report_2026.pdf
    20260415_ifpi_global_music_report_2026.md  (companion)
  visual_references/
    prestige_unscripted/
      20260512_drive_to_survive_paddock_frame_grabs.zip
      20260512_drive_to_survive_paddock_frame_grabs.md
    scene_credible_electronic/
      20260512_cercle_pyramids_frame_grabs.zip
      20260512_cercle_pyramids_frame_grabs.md
    crossover_aesthetic/
      20260518_bottega_veneta_ss26_campaign.jpg
      20260518_bottega_veneta_ss26_campaign.md
  formats/
    20260420_idol_format_overview_public.md
  legal/
    20260601_uk_unscripted_talent_contract_template.pdf
    20260601_uk_unscripted_talent_contract_template.md
```

Notes:

- `references/visual_references/` is subdivided by reference class per `04_competitive_landscape/visual_reference_analysis.md`.
- `references/primary_sources/`, `references/formats/`, `references/legal/` follow the same `binary + companion .md` pattern.

### Naming Examples

| Asset | Filename |
| --- | --- |
| Netflix `Drive to Survive` Season 6 episode 1 paddock scene frame grab | `20260518_drive_to_survive_s6e1_paddock_frame_p1.png` |
| Cercle Pyramids livestream drone master | `20260518_cercle_pyramids_drone_master_p1.png` |
| The Gentlewoman interview spread (page 1 of 4) | `20260518_the_gentlewoman_interview_spread_p1.png` |
| Apple Vision Pro marketing page scroll sequence (4 frames) | `20260518_apple_vision_pro_scroll_sequence_p1.png` through `_p4.png` |
| Tomorrowland 2025 mainstage hero shot | `20260518_tomorrowland_2025_mainstage_hero_p1.png` |
| Resident Advisor long-form article PDF archive | `20260518_resident_advisor_long_form_article_archive.pdf` |
| IFPI Global Music Report 2026 (primary source) | `20260415_ifpi_global_music_report_2026.pdf` |
| Daft Punk Unchained frame grab archive | `20260512_daft_punk_unchained_frame_grabs.zip` |

### Metadata Examples

#### Screenshot Companion `.md` (Cinematic Reference)

```yaml
---
doc_type: source
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-25
retrieval_tags: [screenshot, drive_to_survive, prestige_unscripted, paddock_cinematography]
source_type: screenshot
attribution:
  source: Drive to Survive (Netflix)
  creator: Box to Box Films / Netflix
  url: https://www.netflix.com/title/80204890
  date_captured: 2026-05-18
  capture_context: Season 6 episode 1 paddock long-lens compression frame, used for cinematography-language analysis of long-lens-at-distance grammar.
  license_considerations: Frame grab for internal reference use; fair-use considerations apply for any downstream public use.
taxonomy:
  primary_category: prestige_unscripted
  secondary_categories: [cinematic_storytelling]
  reference_class: prestige_unscripted
related:
  - 04_competitive_landscape/cinematography_language.md
  - 04_competitive_landscape/visual_reference_analysis.md
  - 04_competitive_landscape/prestige_unscripted_breakdown.md
---

# Drive to Survive S6E1 Paddock Frame

Captured for cinematography-language analysis of long-lens compression at pit-lane distance. The frame demonstrates the embedded-crew grammar that earns access without breaking the observational frame.
```

#### Reference Companion `.md` (Editorial Reference)

```yaml
---
doc_type: source
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-25
retrieval_tags: [reference, the_gentlewoman, editorial_systems, premium_typography, luxury_restraint]
source_type: reference
reference_category: visual_reference
attribution:
  source: The Gentlewoman magazine
  creator: Penny Martin (editor) / Fantastic Woman
  url: https://thegentlewoman.co.uk/
  date_captured: 2026-05-20
  capture_context: Interview spread architecture for editorial-systems analysis. Captured to inform website-strategy reading-rhythm decisions and press-kit format direction.
  license_considerations: Editorial reference for internal use; any reproduction of magazine spreads requires publisher clearance.
taxonomy:
  primary_category: editorial_systems
  secondary_categories: [premium_typography, luxury_restraint]
  reference_class: crossover_aesthetic
related:
  - 07_brand_world/visual_principles.md
  - 07_brand_world/visual_positioning.md
  - 08_website_strategy/page_briefs/the_world.md
  - 04_competitive_landscape/reference_analysis_template.md
---

# The Gentlewoman Interview Spread

Captured for editorial-systems analysis. Demonstrates spread architecture that respects reader time, anchored typography, and image-text-image rhythm that translates to digital editorial pacing.
```

### Annotation Examples

Annotations are optional but recommended for references that will inform analysis. Annotations live in the companion `.md` file's body (below the frontmatter).

#### Good Annotation

```markdown
# Drive to Survive S6E1 Paddock Frame

## Observation

Long-lens compression at approximately 135mm equivalent, subject at 8-10 metres distance. Subject is unaware or has acclimated to the camera presence; framing is observational, not directed.

## Mechanism

The long lens at distance produces three things simultaneously:
1. Subject isolation (background goes soft, subject reads three-dimensional).
2. Compression of paddock depth (the world feels close, even at scale).
3. Implicit access claim (the audience knows you cannot fake this).

## Relevance

Informs `04_competitive_landscape/cinematography_language.md` long-lens commitment for `Drop Night` venues. Specifically supports the "long-lens for crowd reaction at distance" syntactic decision.

## Refusal

What this frame does NOT teach MixHouse: the paddock-cinematography composition is heavily F1-specific (pit-lane geometry, team-uniform colour blocks). MixHouse does not import the composition; it imports the lens-and-distance mechanism.
```

#### Bad Annotation

```markdown
# Drive to Survive Frame

Looks cool. Use for reference.
```

The bad annotation fails on every dimension: no mechanism, no relevance, no refusal, no actionable detail. Future agents and analysts cannot use it.

### Good vs Bad Reference Capture Examples

#### Good Capture: Apple Vision Pro Scroll Sequence

- Four-frame sequence captured at native resolution.
- Filename pattern: `20260520_apple_vision_pro_scroll_sequence_p1.png` through `_p4.png`.
- Companion `.md` with full frontmatter, taxonomy tags (`interaction_pacing`, `progressive_disclosure`, `immersive_transitions`, `luxury_restraint`), and `related:` linkage to `07_brand_world/visual_principles.md` and `08_website_strategy/page_briefs/`.
- Annotation explains scroll-as-narrative mechanism and identifies what to adopt vs refuse.

Why it is good: the sequence captures the interaction (not just a frame), attribution is complete, taxonomy is conservative and defensible, canonical linkage routes to specific files.

#### Bad Capture: "Apple Page"

- Single frame captured at half-resolution.
- Filename: `apple.png`.
- No companion `.md` file.
- No attribution, no taxonomy, no linkage.

Why it is bad: the frame does not show the interaction, the filename loses the source identity, and the lack of metadata means the asset cannot be retrieved by future queries.

#### Good Capture: Cercle Pyramids Drone Master

- Single hero frame plus three supporting frames showing crowd, performer, and venue.
- Filename pattern: `20260518_cercle_pyramids_drone_master_p1.png` through `_p4.png`.
- Lives in `10_source_material/references/visual_references/scene_credible_electronic/`.
- Companion `.md` with taxonomy tags (`festival_visual`, `music_authenticity`, `cinematic_storytelling`, `immersive_transitions`), `related:` linkage to `04_competitive_landscape/cinematography_language.md` and `04_competitive_landscape/cercle.md`.
- Annotation explains the location-as-subject mechanism and identifies what to adopt vs refuse for `Drop Night` cinematography.

Why it is good: captured for cinematography analysis with full attribution and taxonomy, placed in the correct sub-folder for retrieval.

#### Bad Capture: Pinterest Moodboard Dump

- Twenty unrelated images saved from Pinterest with no source attribution.
- Filenames retain Pinterest hash IDs.
- No companion `.md` files.
- No taxonomy, no linkage.

Why it is bad: the captures lose source attribution at point of capture (Pinterest is not the source; the underlying creator is). Without attribution, the assets cannot be licensed, cannot be cited, and cannot be defended in editorial review. They become noise.

### Anti-Noise Rules

Refuse the following capture patterns:

- **Bulk-capturing entire websites or albums.** Capture only the frames that inform a specific decision.
- **Decontextualised image saves.** If the source attribution cannot be reconstructed at point of capture, do not capture.
- **Trend-chasing captures without retrieval intent.** If the capture does not connect to a canonical file, do not capture.
- **Aggregator screenshots (Pinterest, We Heart It).** These obscure the actual source. Capture the original source instead.
- **Duplicate captures.** Before capturing, search `10_source_material/screenshots/` and `10_source_material/references/` for an existing capture of the same source-and-context. Promote existing captures rather than recapture.
- **AI-generated reference imagery presented as captured.** Do not capture AI-generated material into the reference set; if AI-generated material is referenced, it must be tagged as such with attribution to the generative system.

### Promotion Workflow: Screenshot to Curated Reference

Screenshots in `10_source_material/screenshots/` are raw captures. When a screenshot warrants editorial analysis and curation, it is promoted into `10_source_material/references/visual_references/` with the analysis template applied.

Promotion criteria:

- The screenshot has been cited in two or more canonical or near-canonical files.
- The screenshot has been analysed in `04_competitive_landscape/visual_reference_analysis.md` or `04_competitive_landscape/cinematography_language.md` or a standalone reference analysis.
- The screenshot informs ongoing brand-world or cinematography work, not a single decision.

Promotion process:

1. Copy the binary into the appropriate `references/visual_references/{reference_class}/` sub-folder.
2. Expand the companion `.md` to a full reference analysis using `04_competitive_landscape/reference_analysis_template.md`.
3. Update the original screenshot's companion `.md` `related:` to point to the curated reference.
4. Do not delete the original screenshot; the raw capture stays as evidence.

### Connection Back to Canonical Docs

Every reference, once captured and curated, routes back to one or more canonical anchors. Routing patterns:

| Reference type | Routes to |
| --- | --- |
| Cinematography reference | `04_competitive_landscape/cinematography_language.md`, `04_competitive_landscape/visual_reference_analysis.md` |
| Editorial-systems reference | `07_brand_world/visual_positioning.md`, `07_brand_world/visual_principles.md`, `08_website_strategy/page_briefs/` |
| Premium-typography reference | `07_brand_world/visual_principles.md`, `09_design_system/typography.md` |
| Interaction-pacing reference | `07_brand_world/visual_principles.md`, `08_website_strategy/page_briefs/` |
| Festival-visual reference | `04_competitive_landscape/cinematography_language.md`, `03_market_research/festival_live_experience_market.md` |
| Music-authenticity reference | `07_brand_world/cultural_authenticity.md`, `04_competitive_landscape/visual_reference_analysis.md` |
| Audio-reactive reference | `07_brand_world/visual_principles.md`, future design-system motion |
| Executive-persuasion reference | `11_outputs/` (future), investor-deck direction |

When a canonical file cites a reference, the citation lives in the file's Evidence / Sources table or in a Reference section, with the file path to the asset and the date accessed. Reciprocally, the reference's companion `.md` lists the canonical file in its `related:` frontmatter.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Capture-attribute-classify-link-review workflow design | Synthesis of `10_source_material/README.md` ingestion patterns and `00_system/source_reliability_rules.md` discipline | 2026-05-25 | A (internal anchor) |
| 2 | Filename convention pattern | `00_system/naming_conventions.md` | 2026-05-25 | A (internal anchor) |
| 3 | Frontmatter schema pattern | `00_system/kb_rules.md`; existing companion `.md` patterns in `10_source_material/references/` and `10_source_material/screenshots/` | 2026-05-25 | A (internal anchor) |
| 4 | Taxonomy classification scheme | `04_competitive_landscape/reference_taxonomy.md` | 2026-05-25 | A (internal anchor) |
| 5 | Reference analysis template | `04_competitive_landscape/reference_analysis_template.md` | 2026-05-25 | A (internal anchor) |
| 6 | Promotion criteria for screenshot to curated reference | `10_source_material/screenshots/README.md` archival rules | 2026-05-25 | A (internal anchor) |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Five stages is too much friction for casual capture." | The friction is the discipline. Capture without attribution, taxonomy, or linkage produces unindexed material; the workflow is what prevents that drift. Casual capture lives in personal notes; KB capture lives in this workflow. |
| "Annotations take time we do not have." | Bad annotations take time and produce nothing. Good annotations take slightly more time and produce a retrievable, defensible asset. The workflow is calibrated for asset reuse over multiple analyses. |
| "Why not just dump screenshots and tag them later?" | Because tagging later does not happen. The workflow front-loads attribution and taxonomy at capture time; deferred tagging produces inbox sprawl. |
| "What about quick captures for in-flight conversations?" | Quick captures live in `10_source_material/raw_notes/` with a date-prefixed filename. They do not enter the reference workflow until they warrant analysis. The workflow gates the reference set, not the raw inbox. |
| "Subscribing to Pinterest is faster than building this workflow." | Pinterest obscures attribution and loses retrievability. Speed at point of capture trades against speed at point of retrieval. The workflow optimises the latter. |

## Website Implications

- The workflow is internal-only; do not surface workflow stages on public surfaces.
- Future Fumadocs portal renders reference assets with full frontmatter visible to internal users and filtered taxonomy facets visible to investor users.
- `08_website_strategy/page_briefs/` may inherit reference sets via taxonomy queries against the curated reference base.
- Cinematography decisions on public surfaces (trailer, hero, atmosphere modules) trace back through curated references to source captures with full attribution chain.

## Open Questions

- Tooling: should capture be supported by a browser extension that pre-fills the companion `.md` frontmatter from page metadata? Defer until Fumadocs portal lands and capture volume justifies tooling.
- Bulk import: when migrating existing Pinterest boards or Are.na collections into the KB, what is the attribution-recovery process? Recommended: do not migrate; recapture from source with full attribution.
- Video clip storage: where do short video clips live when the still frame is in `screenshots/` and the clip itself exceeds repository performance budget? Recommended: external storage with a pointer in the companion `.md`.
- Multi-language references: how are non-English source references attributed and tagged? Recommended: attribution in source language, retrieval tags in English, with a translation note in the companion `.md` body.
- License management: at what volume of references does centralised licence tracking become necessary? Recommended: when curated reference count exceeds 200, introduce a licence-tracking sheet in `99_archive/admin/`.

## Change Log

- 2026-05-25, Initial reference capture workflow created as part of Phase 2.5 reference-ingestion layer. Five-stage workflow (capture, attribute, classify, link, review) codified with folder examples, naming examples, metadata examples, annotation examples, good-vs-bad capture examples, anti-noise rules, and promotion workflow from screenshot to curated reference.
