---
doc_type: competitive
status: draft
confidentiality: investor
owners: [adamtday]
last_reviewed: 2026-05-25
retrieval_tags: [reference_template, analysis_standard, visual_intelligence, retrieval_consistency]
related:
  - 04_competitive_landscape/reference_taxonomy.md
  - 04_competitive_landscape/visual_reference_analysis.md
  - 04_competitive_landscape/cinematography_language.md
  - 07_brand_world/visual_principles.md
  - 10_source_material/reference_capture_workflow.md
  - 10_source_material/references/README.md
  - 10_source_material/screenshots/README.md
  - 00_system/document_template.md
assumption: false
---

# Reference Analysis Template

## Purpose

Standardise how visual, cinematic, editorial, and interaction references are analysed once ingested. The template ensures every reference analysis carries the same field set so that retrieval across references is comparable, and so that future analysts (human or agent) cannot quietly skip the parts that matter most (what should NOT translate; relationship to canonical thesis).

The template is a structural contract, not a creative constraint. Analysts may add fields; they cannot remove the required field set.

## Key Takeaways

- A reference without analysis is a screenshot. Analysis is what converts captured material into a brand-world or cinematography decision.
- The required field set covers source attribution, taxonomy classification, observational dimensions, and translation discipline (adopt vs refuse vs reinterpret).
- The hardest fields are the last three: "what should NOT translate to MixHouse", "relationship to canonical thesis", and "why audiences trust it". These are where most reference analyses fail.
- Every analysis links to one or more canonical anchors so retrieval can route from analysis back to the strategic file the reference informs.
- Templates without examples drift. Three worked examples accompany the template; agents writing new analyses should pattern-match against them.

## Core Content

### Required Field Set

The following fields are mandatory for every reference analysis. Fields marked `optional` are recommended but not required.

#### 1. Identification

| Field | Description | Format |
| --- | --- | --- |
| `source_name` | Canonical name of the reference (film, show, brand, product, artist, publication, installation). | String. |
| `source_creator` | Primary creator credit (director, brand owner, designer, studio, artist). | String. |
| `source_year` | Year the reference is from. For ongoing systems, use start year. | Integer. |
| `source_type` | One of: `film`, `series`, `episode`, `livestream`, `concert_film`, `brand_campaign`, `product_page`, `editorial_piece`, `publication`, `installation`, `live_visual_system`, `interaction_pattern`, `type_specimen`, `other`. | Enum. |
| `url` | Original source URL where applicable. | String. |
| `access_date` | Date the reference was accessed for this analysis. | YYYY-MM-DD. |

#### 2. Capture Linkage

| Field | Description | Format |
| --- | --- | --- |
| `screenshot_paths` | Relative paths to companion screenshots in `10_source_material/screenshots/`. List form even if single. | List of strings. |
| `reference_asset_paths` | Relative paths to companion reference assets in `10_source_material/references/`. Optional when screenshots are sufficient. | List of strings, optional. |

#### 3. Taxonomy Classification

| Field | Description | Format |
| --- | --- | --- |
| `primary_category` | One category slug from `04_competitive_landscape/reference_taxonomy.md`. The dominant category for this reference. | Enum slug. |
| `secondary_categories` | Additional category slugs. Multi-category tagging is encouraged. | List of enum slugs, optional. |
| `reference_class` | If the reference also maps to one of the five reference classes in `visual_reference_analysis.md`, name it: `prestige_unscripted`, `scene_credible_electronic`, `residency_life`, `music_doc`, `crossover_aesthetic`. | Enum, optional. |

#### 4. What Works

Free-form analytical prose. Required structure:

- **Visual motif.** What is the dominant visual or interaction motif? Describe at the level of mechanism (lens choice, light source, blocking, timing, hierarchy) rather than impression ("it looks good").
- **What works.** Why does it work for its intended audience? Tie the observation back to the mechanism, not to the brand surface.
- **Emotional effect.** What feeling does it produce in the viewer or user? Describe the specific affective state, not the generic "premium" or "cinematic".

#### 5. What Fails

Free-form analytical prose. Required structure:

- **What fails.** Where does the reference miscarry, over-rely on a single mechanism, or signal something it does not deliver? Honest analysis here is more useful than uncritical praise.
- **Risk of imitation.** If MixHouse copied this directly, what would go wrong? Surface the specific failure mode.

#### 6. Pacing Observations

Free-form analytical prose. Required structure:

- **Pacing rhythm.** How does the reference move through time? Long takes, fast cuts, restraint, escalation, repetition. Describe the temporal grammar.
- **Pacing failure modes.** Where does the pacing fight its content, or where would it fail if extended beyond its current duration?

#### 7. Interaction Observations

Required for `interaction_pacing`, `progressive_disclosure`, `audio_reactive`, `fan_participation` categories. Optional for cinematic references.

- **Interaction grammar.** What does the user or audience do? What is the input-to-response relationship? What is the response latency and timing?
- **Interaction failure modes.** Where does the interaction over-rely on novelty or under-deliver on user intent?

#### 8. Typography Observations

Required for `premium_typography`, `editorial_systems`, `executive_persuasion` categories. Optional elsewhere when type is incidental.

- **Type family and weight.** Identified families if known; otherwise descriptive. Include weight progression, hierarchy logic, and pairing logic.
- **Type-as-voice.** What does the typographic system signal about brand voice? Editorial confidence, technical precision, scene credibility, luxury restraint.

#### 9. Motion Observations

Required for `cinematic_storytelling`, `immersive_transitions`, `emotional_escalation`, `interaction_pacing`, `audio_reactive` categories. Optional elsewhere.

- **Motion grammar.** Camera movement, edit pace, transition language, easing curves, animation density.
- **Motion failure modes.** Where motion exists for technical demonstration rather than narrative purpose.

#### 10. Audience Trust Mechanism

Free-form analytical prose. This is the field most reference analyses underweight.

- **Why audiences trust it.** What specific mechanism makes the audience believe the reference is authentic, serious, or worthy of their attention? Trust is built through specific decisions, not through aspirational positioning.
- **What undermines that trust.** What specific decisions would erode the trust signal if changed?

#### 11. Translation Discipline

Free-form analytical prose. Required structure:

- **What should translate to MixHouse.** Specific mechanisms, decisions, or grammars that MixHouse should adopt. Phrase as commitments, not aspirations.
- **What should NOT translate to MixHouse.** Specific decisions, signatures, or surface treatments that MixHouse should refuse. This is harder to write and more important than the adoption list.
- **What should be reinterpreted.** Mechanisms whose intent transfers but whose surface execution must be reworked for MixHouse's context.

#### 12. Relationship to Canonical Thesis

Required. Name the canonical anchor file(s) this reference informs. Reference must connect back to at least one canonical or near-canonical file:

- `01_master_context/mixhouse_master_thesis.md`
- `01_master_context/audience_matrix.md`
- `02_show_bible/format_engine.md`
- `04_competitive_landscape/mixhouse_white_space.md`
- `04_competitive_landscape/cinematography_language.md`
- `04_competitive_landscape/visual_reference_analysis.md`
- `04_competitive_landscape/prestige_unscripted_breakdown.md`
- `07_brand_world/visual_principles.md`
- `07_brand_world/visual_positioning.md`
- `07_brand_world/cultural_authenticity.md`
- `08_website_strategy/page_briefs/*.md` (when website-bound)

State the relationship in one or two sentences. "Informs cinematography commitment X." "Supports brand-world principle Y." "Argues against pattern Z."

### Worked Examples

The three examples below pattern-match the template against real references in the existing analysis (`04_competitive_landscape/visual_reference_analysis.md`) and are provided so future analyses do not drift.

#### Worked Example 1: Cinematic Reference (`Drive to Survive`)

```yaml
source_name: Drive to Survive
source_creator: Box to Box Films / Netflix
source_year: 2019
source_type: series
url: https://www.netflix.com/title/80204890
access_date: 2026-05-25
screenshot_paths:
  - 10_source_material/screenshots/20260518_netflix_drive_to_survive_show_page_p1.png
  - 10_source_material/screenshots/20260518_netflix_drive_to_survive_paddock_long_lens_p2.png
reference_asset_paths: []
primary_category: prestige_unscripted
secondary_categories: [cinematic_storytelling, emotional_escalation]
reference_class: prestige_unscripted
```

- **Visual motif.** Embedded crews; scripted-grade DPs; close-quarters cinematography in motorhomes, paddocks, and team headquarters; long-lens compression at pit-lane distance; slow-motion archival treatment for race moments.
- **What works.** The cinematography earns access. Audiences read scripted-grade craft as evidence of subject importance. The grammar is documentary, but the production value is cinematic.
- **Emotional effect.** Importance. The viewer feels the subject is consequential before any narrative claim has been made.
- **What fails.** When the editorial reaches for villain-narrative grammar (driver vs driver conflict edited at promo-trailer pace), the cinematography loses its observational authority and becomes a vehicle for engineered drama.
- **Risk of imitation.** Copying the talking-head-in-windowless-interview-room grammar would import the cliché without the access; MixHouse uses environmental interviews tied to the residency space.
- **Pacing rhythm.** Documentary pacing with race-weekend escalation per episode; multi-episode arcs tracking season escalation; slow-motion deceleration at high-emotion moments.
- **Pacing failure modes.** When music supervision overreaches on tension moments, pacing reads as engineered rather than observed.
- **Motion grammar.** Long-lens at distance; jib for paddock masters; tracked vehicle shots; archival cinematic treatment of race footage.
- **Motion failure modes.** Quick-cut crash-aftermath sequences sometimes fight the observational grammar.
- **Why audiences trust it.** Cinematic prestige operates as a trust signal for subject seriousness. The grammar respects the room and the work; the audience reads that respect as authenticity.
- **What undermines that trust.** Editorial drift toward broadcast-promo cutting; visible production interventions; talking-head set-ups that break the observational frame.
- **What should translate to MixHouse.** Scripted-grade DPs; embedded crews; close-quarters residency and studio cinematography; long-lens compression at `Drop Night` venues; observational pacing as default.
- **What should NOT translate to MixHouse.** The talking-head-in-windowless-interview-room grammar; promo-trailer cutting of conflict moments; the celebrity-team-principal framing (MixHouse does not have team principals).
- **What should be reinterpreted.** The season-finale escalation grammar transfers to the finale festival cinematography but reworks for cohort dynamics rather than single-driver climax.
- **Relationship to canonical thesis.** Informs cinematography commitments for residency life and studio process in `04_competitive_landscape/cinematography_language.md`. Supports the prestige-unscripted positioning in `04_competitive_landscape/mixhouse_white_space.md`. Anchors the prestige-unscripted reference class in `04_competitive_landscape/visual_reference_analysis.md`.

#### Worked Example 2: Editorial Reference (The Gentlewoman)

```yaml
source_name: The Gentlewoman
source_creator: Penny Martin (editor) / Fantastic Woman
source_year: 2010
source_type: publication
url: https://thegentlewoman.co.uk/
access_date: 2026-05-25
screenshot_paths:
  - 10_source_material/screenshots/20260520_the_gentlewoman_cover_archive_p1.png
  - 10_source_material/screenshots/20260520_the_gentlewoman_interview_spread_p2.png
reference_asset_paths: []
primary_category: editorial_systems
secondary_categories: [premium_typography, luxury_restraint]
reference_class: crossover_aesthetic
```

- **Visual motif.** Long-form interview architecture with generous whitespace; restrained type system anchored on a single serif display and a single sans working face; cover photography as portraiture, never as celebrity bait.
- **What works.** The publication treats its subjects with the dignity of a portrait sitting and treats its readers with the assumption of patience. Both decisions compound across an issue.
- **Emotional effect.** Considered attention. Readers feel they are being trusted with a long-form encounter rather than served a marketable headline.
- **What fails.** The system can read as exclusionary; the editorial register requires reader-side investment that not every brand-world surface can demand.
- **Risk of imitation.** Adopting the typographic restraint without the editorial depth produces empty space, not generosity.
- **Pacing rhythm.** Slow. Spread-by-spread; image-text-image rhythm; long-form text passages with no visual escape valve.
- **Pacing failure modes.** Fails on mobile-first scrolling unless the digital adaptation rebuilds the pacing grammar.
- **Typography observations.** Single serif display family used at multiple weights and sizes; clear hierarchy through scale and weight alone, not through colour or treatment; supporting sans for captions and metadata; no decorative type ever.
- **Type-as-voice.** Editorial confidence; the type itself signals that the publication trusts its content to carry.
- **Motion observations.** Print is static; digital edition retains print pacing without adding digital-native motion.
- **Why audiences trust it.** The publication respects reading time as a finite resource; every page earns its space. Readers detect the discipline and extend trust to the editorial selection.
- **What undermines that trust.** Sponsored-content insertions without typographic differentiation; covers chosen for celebrity over editorial fit; rushed digital adaptation that breaks print pacing.
- **What should translate to MixHouse.** Single-display-family type discipline; long-form spread architecture in press kit and deck; reader-as-respected discipline across website page briefs.
- **What should NOT translate to MixHouse.** The exclusionary register; the small-audience editorial bet (MixHouse is mass-prestige, not niche-prestige); the print-first pacing on digital surfaces.
- **What should be reinterpreted.** The interview architecture transfers to mentor and judge profile content but reworks for digital-native reading.
- **Relationship to canonical thesis.** Informs `07_brand_world/visual_positioning.md` editorial type discipline; supports the editorial-cinema principle in `07_brand_world/visual_principles.md`; anchors `08_website_strategy/page_briefs/the_world.md` reading-rhythm decisions.

#### Worked Example 3: Interaction Reference (Apple Vision Pro Marketing Page)

```yaml
source_name: Apple Vision Pro marketing page
source_creator: Apple Marketing Communications
source_year: 2024
source_type: product_page
url: https://www.apple.com/apple-vision-pro/
access_date: 2026-05-25
screenshot_paths:
  - 10_source_material/screenshots/20260522_apple_vision_pro_hero_p1.png
  - 10_source_material/screenshots/20260522_apple_vision_pro_scroll_sequence_p2.png
  - 10_source_material/screenshots/20260522_apple_vision_pro_scroll_sequence_p3.png
reference_asset_paths: []
primary_category: interaction_pacing
secondary_categories: [progressive_disclosure, immersive_transitions, luxury_restraint]
reference_class: crossover_aesthetic
```

- **Visual motif.** Scroll-driven sequential reveal of product through environmental contexts; held moments at each scroll milestone; cinematic transitions between contexts; type system anchored in left-aligned editorial display with generous space.
- **What works.** Scroll-as-narrative pacing matches the patience-as-confidence brand register. The user is invited to pace themselves; the page does not chase them.
- **Emotional effect.** Considered consequence. The user feels they are being shown a deliberate sequence rather than scrolling through a marketing wall.
- **What fails.** On low-end devices or constrained bandwidth, the scroll grammar degrades; the fallback experience is materially less persuasive.
- **Risk of imitation.** Adopting the scroll-driven grammar without Apple-scale visual asset budget produces emptier, slower marketing pages without the payoff.
- **Pacing rhythm.** Held-then-reveal-then-held; scroll-driven escalation across product features; chapter-marker structure with breathing room between chapters.
- **Pacing failure modes.** Fails when the visual asset density does not earn the pacing; pacing without payoff reads as pretension.
- **Interaction grammar.** Scroll as primary input; click only at conversion points; hover and focus states refined for the click moments that matter; no auto-play that overrides user pace.
- **Interaction failure modes.** Some chapter-marker transitions can feel scroll-jacked on shorter pages where the held-frame logic does not have room to breathe.
- **Motion observations.** Cinematic transitions between contexts; held frames between transitions; easing curves that match camera-motion intuition rather than mechanical interpolation.
- **Motion failure modes.** Motion sometimes outpaces the user's reading speed on dense feature pages.
- **Why audiences trust it.** Pacing restraint signals confidence. The page does not chase the user; the user is trusted to engage at their own pace.
- **What undermines that trust.** Auto-play that overrides user pace; cookie-banner intrusion at scroll moments; transition timings that fight rather than serve content.
- **What should translate to MixHouse.** Scroll-as-narrative pacing on `08_website_strategy/page_briefs/the_world.md` and the home page; held-then-reveal rhythm for `Drop Night` storytelling on the show page; chapter-marker structure for season-arc storytelling.
- **What should NOT translate to MixHouse.** Apple's product-feature-list architecture; the product-as-hero framing (MixHouse leads with character and place, not product); the marketing-pages-as-spec-sheet posture.
- **What should be reinterpreted.** The scroll-driven sequential reveal transfers to season-arc storytelling but reworks for narrative arc rather than feature progression.
- **Relationship to canonical thesis.** Informs interaction-pacing decisions in `07_brand_world/visual_principles.md`; supports website-strategy page brief pacing in `08_website_strategy/`; anchors progressive-disclosure discipline for public-vs-investor surface decisions.

### Authoring Workflow

1. Capture the reference per `10_source_material/reference_capture_workflow.md` (screenshots stored, frontmatter applied, taxonomy tags assigned).
2. Open a new analysis file at `04_competitive_landscape/references/{source_slug}.md` if the reference warrants standalone analysis. Otherwise, add a row to the relevant cluster file (for example `04_competitive_landscape/visual_reference_analysis.md` for cinematic references).
3. Fill the required field set in order; do not skip later fields by rushing earlier ones.
4. Cross-link to canonical anchors via the `related:` frontmatter and the relationship-to-canonical-thesis field.
5. Submit for editorial review (founder, EP, brand-world lead). Analyses without review carry `status: seed`; reviewed analyses carry `status: draft` until canonical reconciliation closes.

### Anti-Patterns In Reference Analysis

Common failure modes to refuse:

- **Adoration without mechanism.** Praising a reference without naming the specific mechanism that makes it work. "It's beautiful" is not analysis.
- **Adoption-only thinking.** Documenting what to copy without documenting what to refuse. Refusal is half the analysis.
- **Disconnection from canon.** Analyses that do not name a canonical anchor are decoration. Every reference must connect back.
- **Trend-chasing.** References chosen because they are currently celebrated rather than because they demonstrate a durable mechanism. Test: would this reference still be useful in five years?
- **Inflation of category.** Tagging every reference with every category dilutes retrieval. Primary category is one; secondary categories are conservative.
- **Citation without access.** Naming a reference whose source URL is dead or whose screenshots are missing. References must be retrievable to be useful.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Required-field-set design pattern | `00_system/document_template.md`; existing analysis structures in `04_competitive_landscape/visual_reference_analysis.md` | 2026-05-25 | A (internal anchor) |
| 2 | `Drive to Survive` worked example fields | `04_competitive_landscape/visual_reference_analysis.md`, `04_competitive_landscape/cinematography_language.md` | 2026-05-25 | A (internal anchor) |
| 3 | The Gentlewoman worked example fields | Publication archive; editorial-analysis tradition | 2026-05-25 | B |
| 4 | Apple Vision Pro page worked example fields | Public marketing page; interaction-design analysis tradition | 2026-05-25 | B |
| 5 | Anti-patterns drawn from existing-analysis review pass | `04_competitive_landscape/visual_reference_analysis.md` quality review | 2026-05-25 | A (internal anchor) |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Twelve required fields is too many." | Each field corresponds to a retrieval question the KB will be asked. Skipping a field means the question cannot be answered from the analysis. The template is the minimum; better analyses add fields. |
| "The worked examples are too long." | The examples set the floor for analytical depth. Shorter examples produce shallower analyses; the template defends against that drift. |
| "What if the reference does not have meaningful typography or motion?" | The field is conditional on category. References tagged `cinematic_storytelling` require motion analysis; `premium_typography` requires type analysis. Other fields stay optional when their category is not in scope. |
| "Why is `what should NOT translate` mandatory?" | Because refusal is what gives the brand world coherence. Without it, every reference becomes a copy candidate, and the brand world becomes a pastiche of references. |
| "Can agents fill this template?" | Yes, with editorial review. The template is structured precisely so that an agent's output is comparable to a human analyst's output and can be reviewed against the same standard. |

## Website Implications

- The template is internal-only; do not surface field names on public surfaces.
- Future Fumadocs portal renders reference analyses as structured records with field-level filtering and search.
- `08_website_strategy/page_briefs/` references this template when justifying a reference-set inheritance for a page.
- Worked examples are the floor for any agent-generated analysis ingested into the KB.

## Open Questions

- Should reference analyses live in a dedicated `04_competitive_landscape/references/` subfolder, or remain within cluster files like `visual_reference_analysis.md`? Recommended: standalone files for high-depth analyses (10+ paragraphs of analytical prose) and cluster-file rows for shorter analyses.
- Editorial review SLA for new analyses: how long can a `status: seed` analysis sit before it is either promoted or archived? Recommended: 30 days.
- Tooling: should the template be enforced by a CI lint check on frontmatter fields? Defer until Fumadocs portal lands.
- Multi-author analyses: how is authorship attribution recorded across founders, advisors, and agents? Recommended: `owners:` frontmatter field is mandatory and lists all contributors.

## Change Log

- 2026-05-25, Initial reference analysis template created as part of Phase 2.5 reference-ingestion layer. Twelve required fields defined across identification, capture linkage, taxonomy classification, observational dimensions, and translation discipline. Three worked examples included (`Drive to Survive`, The Gentlewoman, Apple Vision Pro page). Anti-patterns codified.
