---
doc_type: source
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-25
retrieval_tags: [manual_capture, screenshots, checklist, ingestion_workflow, founder_action]
related:
  - 10_source_material/screenshots/capture_packet_for_adam.md
  - 10_source_material/reference_capture_workflow.md
  - 10_source_material/screenshots/README.md
  - 10_source_material/references/README.md
  - 04_competitive_landscape/visual_reference_analysis.md
  - 04_competitive_landscape/reference_taxonomy.md
  - 04_competitive_landscape/reference_analysis_template.md
---

# Manual Capture Checklist

## Purpose

Exhaustive per-reference checklist for the manual screenshot capture pass that follows the Phase 2.6 ingestion sprint. The checklist enumerates every reference, what to capture, recommended frame counts, capture priority, the exact filename pattern, and the companion `.md` file each capture links back to.

This file is the reference. The day-of working guide is `10_source_material/screenshots/capture_packet_for_adam.md`. Use the packet while capturing; consult this file for any per-reference detail the packet abbreviates.

## Key Takeaways

- Twenty references are pending capture across three reference classes.
- Capture priorities are ordered P0 to P4. P0 is the blocked-source pass (Cercle Odyssey, Pitchfork) that also requires re-analysis. P1 anchors the four cluster analyses; capture these next. P2 to P4 complete the set in declining strategic urgency.
- Filename pattern is non-negotiable: each binary's stem must match the companion `.md` file's stem so the asset pair stays unified at retrieval time.
- The companion `.md` file's `## Screenshot Links` section lists the expected filenames; the capture should match those names exactly.
- Multi-frame sequences use `_p1`, `_p2`, etc. suffixes; the companion `.md` covers the whole sequence.
- Blocked-source captures (P0) unlock pending analyses. Once the binaries are captured, the founder also re-analyses the page content (the existing stub is a placeholder, not an analysis).

## Core Content

### Capture priority order

| Priority | Reasoning | References |
| --- | --- | --- |
| P0 | Blocked at fetch; capture also unblocks pending analysis. Highest founder ROI. | Cercle Odyssey, Pitchfork |
| P1 | Anchors one of the four cluster analyses. Strategic core. | Apple Vision Pro, Apple TV+, Resident Advisor homepage, Cercle homepage, F1 homepage |
| P2 | Supporting member of a cluster analysis or scene-credibility anchor. | Apple AirPods Max, Apple MacBook Pro, RA Magazine, RA Reviews, RA Podcast, Boiler Room homepage, F1 Drivers, Box to Box Films, Teenage Engineering homepage |
| P3 | Depth or contrast reference; useful but not anchoring. | Teenage Engineering EP-133, Cirque du Soleil homepage, Cirque du Soleil O |
| P4 | Lower direct relevance to MixHouse public surfaces; capture when convenient. | Netflix Tudum |

### Per-reference checklist

#### P0: Blocked sources requiring capture and re-analysis

| Source | URL | Frames | Visual moments | Filename pattern | Companion `.md` | Status |
| --- | --- | --- | --- | --- | --- | --- |
| Cercle Odyssey | https://cercleodyssey.com/ | 4 to 6 | Hero / immersive experience pitch, navigation, location-and-date presentation, audio-reactive or motion elements, footer | `20260525_cercle_odyssey_pending_capture_p1.png` through `_p6.png` (after capture, rename stub to `20260525_cercle_odyssey_homepage` and update both `.md` and `.png` filenames) | `10_source_material/references/visual_references/scene_credible_electronic/20260525_cercle_odyssey_pending_capture.md` | required; blocks pending analysis |
| Pitchfork | https://pitchfork.com/ | 4 to 6 | Hero / lead article, review-score system in context, Best New Music or feature series, footer / parent-publisher integration | `20260525_pitchfork_pending_capture_p1.png` through `_p6.png` (after capture, rename stub to `20260525_pitchfork_homepage`) | `10_source_material/references/visual_references/scene_credible_electronic/20260525_pitchfork_pending_capture.md` | required; blocks pending analysis |

#### P1: Cluster-analysis anchors

| Source | URL | Frames | Visual moments | Filename pattern | Companion `.md` | Status |
| --- | --- | --- | --- | --- | --- | --- |
| Apple Vision Pro | https://www.apple.com/apple-vision-pro/ | 4 to 5 | Hero with headline, mid-page section transition, drawer-expansion interaction, footer | `20260525_apple_vision_pro_marketing_page_p1.png` through `_p5.png` | `10_source_material/references/visual_references/crossover_aesthetic/20260525_apple_vision_pro_marketing_page.md` | required |
| Apple TV+ | https://www.apple.com/apple-tv-plus/ | 3 to 4 | Hero with partnership imagery (F1 if visible), subscription block, partnership logos (F1, MLS, MLB) in context, footer | `20260525_apple_tv_plus_marketing_page_p1.png` through `_p4.png` | `10_source_material/references/visual_references/crossover_aesthetic/20260525_apple_tv_plus_marketing_page.md` | required |
| Resident Advisor homepage | https://ra.co/ | 3 to 5 | Hero / Latest News, city-specific event listings, magazine card grid, footer with regional selector | `20260525_resident_advisor_homepage_p1.png` through `_p5.png` | `10_source_material/references/visual_references/scene_credible_electronic/20260525_resident_advisor_homepage.md` | required |
| Cercle homepage | https://cercle.io/ | 3 to 4 | Hero performer-at-screen image, six-card navigation grid (ODYSSEY, Festival, MOMENT, RECORDS, SHOP, Newsletter), brand-positioning sentence in context, footer | `20260525_cercle_homepage_p1.png` through `_p4.png` | `10_source_material/references/visual_references/scene_credible_electronic/20260525_cercle_homepage.md` | required |
| F1 homepage | https://www.formula1.com/ | 4 to 5 | Result-as-hero (latest race), schedule carousel, standings table, video gallery, footer with partner logos | `20260525_formula1_homepage_p1.png` through `_p5.png` | `10_source_material/references/visual_references/prestige_unscripted/20260525_formula1_homepage.md` | required |

#### P2: Cluster supporting members and scene-credibility anchors

| Source | URL | Frames | Visual moments | Filename pattern | Companion `.md` | Status |
| --- | --- | --- | --- | --- | --- | --- |
| Apple AirPods Max | https://www.apple.com/airpods-max/ | 4 to 5 | Hero with colorway carousel, "Take a closer look" interactive color selector, tabbed audio-specification section, footer | `20260525_apple_airpods_max_marketing_page_p1.png` through `_p5.png` | `10_source_material/references/visual_references/crossover_aesthetic/20260525_apple_airpods_max_marketing_page.md` | required |
| Apple MacBook Pro | https://www.apple.com/macbook-pro/ | 4 to 5 | Hero with M5 V-shape product visualisation, feature breakdown section, M5 / M4 / M1 comparison table, footer | `20260525_apple_macbook_pro_marketing_page_p1.png` through `_p5.png` | `10_source_material/references/visual_references/crossover_aesthetic/20260525_apple_macbook_pro_marketing_page.md` | required |
| RA Magazine | https://ra.co/magazine | 3 | Magazine hub with Latest News and Popular News, Latest Features section, Feature Series cards | `20260525_ra_magazine_p1.png` through `_p3.png` | `10_source_material/references/visual_references/scene_credible_electronic/20260525_ra_magazine.md` | required |
| RA Reviews | https://ra.co/reviews | 3 | Reviews hub with RA Recommends tabs, Albums tab content, Singles tab content with byline visibility | `20260525_ra_reviews_p1.png` through `_p3.png` | `10_source_material/references/visual_references/scene_credible_electronic/20260525_ra_reviews.md` | required |
| RA Podcast | https://ra.co/podcast | 3 | Featured weekly episode hero, archive grid for current year, year navigation (Previous / Next) | `20260525_ra_podcast_p1.png` through `_p3.png` | `10_source_material/references/visual_references/scene_credible_electronic/20260525_ra_podcast.md` | required |
| Boiler Room homepage | https://boilerroom.tv/ | 3 to 4 | Upcoming Events carousel, archive with genre tags, Cities hub navigation, footer | `20260525_boiler_room_homepage_p1.png` through `_p4.png` | `10_source_material/references/visual_references/scene_credible_electronic/20260525_boiler_room_homepage.md` | required |
| F1 Drivers page | https://www.formula1.com/en/drivers | 3 | 20-driver grid hero, team-colour-background portraits in context, news cards in context | `20260525_formula1_drivers_page_p1.png` through `_p3.png` | `10_source_material/references/visual_references/prestige_unscripted/20260525_formula1_drivers_page.md` | required |
| Box to Box Films homepage | https://www.boxtoboxfilms.com/ | 2 to 3 | Sparse navigation header, production list, footer with contact email | `20260525_box_to_box_films_homepage_p1.png` through `_p3.png` | `10_source_material/references/visual_references/prestige_unscripted/20260525_box_to_box_films_homepage.md` | required |
| Teenage Engineering homepage | https://teenage.engineering/ | 3 to 4 | Hero with restrained product grid, navigation revealing collections, all-lowercase headings in context, footer | `20260525_teenage_engineering_homepage_p1.png` through `_p4.png` | `10_source_material/references/visual_references/crossover_aesthetic/20260525_teenage_engineering_homepage.md` | required |

#### P3: Depth and contrast references

| Source | URL | Frames | Visual moments | Filename pattern | Companion `.md` | Status |
| --- | --- | --- | --- | --- | --- | --- |
| Teenage Engineering EP-133 | https://teenage.engineering/products/ep-133 | 4 to 5 | Hero with Muhammad Ali imagery and repeated CTA, feature breakdowns, "no. 1 champion" headline section, footer | `20260525_teenage_engineering_ep133_p1.png` through `_p5.png` | `10_source_material/references/visual_references/crossover_aesthetic/20260525_teenage_engineering_ep133.md` | recommended |
| Cirque du Soleil homepage | https://www.cirquedusoleil.com/ | 3 | Hero with character illustration and mission statement, brand-philosophy lead section, footer with affiliated brands | `20260525_cirque_du_soleil_homepage_p1.png` through `_p3.png` | `10_source_material/references/visual_references/crossover_aesthetic/20260525_cirque_du_soleil_homepage.md` | recommended |
| Cirque du Soleil O show page | https://www.cirquedusoleil.com/o | 3 | Hero quote and blog introduction, FAQ section with specific scale numbers, footer | `20260525_cirque_du_soleil_o_p1.png` through `_p3.png` | `10_source_material/references/visual_references/crossover_aesthetic/20260525_cirque_du_soleil_o.md` | recommended |

#### P4: Lower direct relevance

| Source | URL | Frames | Visual moments | Filename pattern | Companion `.md` | Status |
| --- | --- | --- | --- | --- | --- | --- |
| Netflix Tudum homepage | https://www.netflix.com/tudum/ | 3 to 4 | Hero imagery, content cards / topic clusters, footer | `20260525_netflix_tudum_homepage_p1.png` through `_p4.png` | `10_source_material/references/visual_references/crossover_aesthetic/20260525_netflix_tudum_homepage.md` | optional |

### Capture requirements summary

| Reference class | Required captures | Optional / recommended captures | Total |
| --- | --- | --- | --- |
| crossover_aesthetic | Apple Vision Pro, Apple TV+, Apple AirPods Max, Apple MacBook Pro, Teenage Engineering homepage | Teenage Engineering EP-133, Cirque du Soleil homepage, Cirque du Soleil O, Netflix Tudum | 9 |
| scene_credible_electronic | Cercle Odyssey, Pitchfork, RA homepage, Cercle homepage, RA Magazine, RA Reviews, RA Podcast, Boiler Room homepage | (none) | 8 |
| prestige_unscripted | F1 homepage, F1 Drivers, Box to Box Films | (none) | 3 |
| Total | 16 required | 4 recommended / optional | 20 |

### Per-reference details: visual moments to prioritise

Many companion `.md` files identify a specific mechanism that the screenshot should evidence. The capture brief below names that mechanism per reference so the screenshot does analytical work, not just documentation work.

#### crossover_aesthetic

- **Apple Vision Pro page.** Capture the held-then-reveal scroll pacing. Frame 1: hero with the spatial-computing headline. Frames 2-4: section transitions showing how each thematic block resets the frame. Frame 5: footer information density (this is a counter-reference, evidence of what MixHouse refuses).
- **Apple AirPods Max page.** Capture the colorway carousel as identity statement (Frame 1), the tabbed audio-spec interaction (Frame 2-3), and an example of a two-word headline doing brand work (Frame 4-5).
- **Apple MacBook Pro page.** Capture the spec-tables-compartmented-from-narrative discipline. Frame 1: hero. Frame 2-3: a feature section that runs narrative and adjacent spec content separately. Frame 4: the M5 / M4 / M1 comparison table. Frame 5: lifestyle photography example.
- **Apple TV+ page.** Capture the partnership-as-credibility mechanism. Frame 1: hero with partnership imagery. Frame 2-3: partnership logos (F1, MLS, MLB) doing credibility work in context. Frame 4: footer.
- **Netflix Tudum.** Capture the editorial-property branding. Frame 1: hero with Tudum wordmark and editorial register. Frame 2-3: content cards with on-set photography. Frame 4: footer Netflix integration.
- **Teenage Engineering homepage.** Capture the all-lowercase-minimal-headings discipline. Frame 1: hero with restrained product display. Frame 2: navigation revealing collections. Frame 3: example of playful-and-technical voice pairing in context. Frame 4: footer with Stockholm address.
- **Teenage Engineering EP-133.** Capture the cultural-reference-as-brand-collaboration mechanism. Frame 1: hero with Ali imagery and "ONLY $329 BUY NOW!" CTA. Frame 2-3: feature breakdowns extending the boxing metaphor. Frame 4: spec section. Frame 5: footer.
- **Cirque du Soleil homepage.** Capture the brand-philosophy-precedes-inventory choice. Frame 1: hero with character illustration and mission statement. Frame 2: navigation showing corporate-and-entertainment separation. Frame 3: footer with affiliated brands.
- **Cirque du Soleil O show page.** Capture the spectacle-by-numbers FAQ pattern. Frame 1: hero quote. Frame 2: FAQ section showing specific scale numbers (1.5 million gallons, 75 artists, etc.). Frame 3: footer.

#### scene_credible_electronic

- **Resident Advisor homepage.** Capture the assumed-knowledge editorial voice and location-as-first-class-entity discipline. Frame 1: Latest News hero. Frame 2: city-specific event listings (note the regional selector). Frame 3: magazine card grid. Frame 4-5: footer including B-Corp badge (refused pattern) and social-platform listing.
- **RA Magazine.** Capture the no-hero-image editorial density discipline. Frame 1: top of magazine hub showing density-led layout. Frame 2: Latest Features section. Frame 3: Feature Series cards with headline craft examples.
- **RA Reviews.** Capture the reviewer-byline-visibility discipline. Frame 1: RA Recommends tab with byline-visible cards. Frame 2: Albums tab. Frame 3: Singles tab showing scene-specific genre tagging.
- **RA Podcast.** Capture the archive-as-asset chronological discipline. Frame 1: featured weekly episode hero. Frame 2: archive grid for current year. Frame 3: year navigation showing depth.
- **Cercle homepage.** Capture the experience-type-taxonomy navigation and brand-positioning sentence. Frame 1: hero with performer image. Frame 2: six-card navigation grid. Frame 3: brand-positioning sentence in context. Frame 4: footer.
- **Boiler Room homepage.** Capture the multi-identity (event, archive, lifestyle) framing. Frame 1: Upcoming Events carousel. Frame 2: archive with genre-tag vocabulary visible. Frame 3: Cities hub. Frame 4: footer with project links.
- **Cercle Odyssey.** Capture the immersive-experience positioning. Frame 1: hero. Frame 2-4: immersive-experience presentation, location-and-date, audio-reactive or motion elements visible. Frame 5-6: footer and any positioning copy. Note: after capture, also write a full analysis in the companion `.md` (the current file is a stub).
- **Pitchfork.** Capture the editorial-publication architecture. Frame 1: homepage hero / lead article. Frame 2: review-score system in context with the iconic 0-to-10 score visible. Frame 3: Best New Music or feature series. Frame 4: footer with Condé Nast integration. Frame 5-6: a specific review page if useful. Note: after capture, also write a full analysis in the companion `.md`.

#### prestige_unscripted

- **F1 homepage.** Capture the result-as-hero mechanism. Frame 1: race-result hero (this resets each weekend; capture during or shortly after a race weekend if possible). Frame 2: schedule carousel. Frame 3: standings table with visual hierarchy. Frame 4: video gallery. Frame 5: footer with partner logos (counter-reference; evidence of what MixHouse refuses).
- **F1 Drivers page.** Capture the roster-as-permanent-page discipline. Frame 1: 20-driver grid hero. Frame 2: detail of driver-card treatment showing team colour and national flag. Frame 3: news section in context.
- **Box to Box Films.** Capture the work-as-credential discipline. Frame 1: sparse navigation header. Frame 2: production list with five recent titles. Frame 3: footer with contact email.

### Capture sequencing recommendation

Recommended order across a single capture session (estimated 60 to 90 minutes):

1. P0 first (Cercle Odyssey, Pitchfork): unblock pending analyses; founder also re-writes the analysis content in each companion file after capture.
2. P1 second (Apple Vision Pro, Apple TV+, RA homepage, Cercle homepage, F1 homepage): anchors the cluster analyses; high strategic ROI.
3. P2 next (the remaining cluster supporting members): completes the cluster sets.
4. P3 / P4 last (Teenage Engineering EP-133, Cirque pages, Tudum): depth and contrast.

If session time is limited, P0 + P1 is the minimum viable capture pass. P2 should follow in a second session. P3 / P4 can wait for a third pass.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Twenty references requiring capture | `10_source_material/references/visual_references/` (all subfolders) per Phase 2.6 ingestion sprint commit | 2026-05-25 | A (internal anchor) |
| 2 | Per-reference visual moments to prioritise | Companion `.md` files in `10_source_material/references/visual_references/` (Mechanism Analysis sections per reference) | 2026-05-25 | A (internal anchor) |
| 3 | Cluster-analysis anchors | `04_competitive_landscape/references/apple_marketing_pages.md`, `resident_advisor.md`, `cercle_platform.md`, `formula1_editorial.md` | 2026-05-25 | A (internal anchor) |
| 4 | Filename pattern conventions | `10_source_material/reference_capture_workflow.md` Naming Examples section | 2026-05-25 | A (internal anchor) |
| 5 | Blocked-source pending-capture discipline | `10_source_material/references/visual_references/scene_credible_electronic/20260525_cercle_odyssey_pending_capture.md`, `20260525_pitchfork_pending_capture.md` | 2026-05-25 | A (internal anchor) |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Twenty captures is a lot for one session." | The priority ordering supports a partial pass. P0 plus P1 (seven references) is a minimum viable capture and unblocks the most strategic depth. P2, P3, P4 can follow in subsequent sessions. |
| "Why does the filename matter so precisely?" | Because retrieval depends on the binary stem matching the companion `.md` stem. Mismatched filenames break the asset-pair link and require manual reconciliation later. The discipline at capture is the cheapest possible defence. |
| "What if I miss a frame or capture in the wrong order?" | The companion `.md` covers the whole sequence; frames are numbered `_p1` through `_pN`. Order is by reading order on the page (top to bottom), not by capture order. Recapture if needed; do not renumber after the fact. |
| "Cercle Odyssey is the highest priority? Even ahead of Apple?" | Yes. Cercle Odyssey is blocked at the network layer and capturing it also unlocks pending analysis. Apple references are already analysed from WebFetch; the screenshots are evidence, not analysis-enabling. |
| "Can I capture at lower resolution to save time?" | No. Capture at native screen resolution. Hi-DPI displays produce the highest-fidelity assets and should be preferred. Resolution choice is locked in `10_source_material/screenshots/README.md` capture standards. |

## Website Implications

- The captured assets become the visual-evidence base for future website-strategy decisions in `08_website_strategy/page_briefs/`.
- Captured Apple, Cercle, and F1 screenshots are direct inputs to the cluster analyses in `04_competitive_landscape/references/`; the cluster analyses currently reference expected filenames that the captures will populate.
- The `## Screenshot Links` section in each companion `.md` will populate with actual binary references once captures are uploaded.

## Open Questions

- Cercle Odyssey re-analysis: after capture, who writes the full analysis (founder, agent in a follow-up session, both)? Recommended: agent drafts based on captured screenshots; founder reviews.
- Pitchfork re-analysis: same question. Recommended: same answer.
- Capture-session pairing: should the founder capture solo or pair with a designer or producer who can flag interaction details the founder might miss? Recommended: solo first pass; pair second pass for any reference where interaction depth matters (Apple Vision Pro, Cercle Odyssey, F1 home).
- Screenshot retention: as the reference set grows, what is the per-source retention policy? Recommended: keep all captures from each ingestion sprint; deprecate per the archival rules in `10_source_material/screenshots/README.md` only when the source has been re-captured or the reference is removed.

## Change Log

- 2026-05-25, Initial manual capture checklist created as part of Phase 2.7 manual visual capture packet. Enumerates twenty references across three reference classes; assigns capture priority (P0 to P4); names per-reference visual moments to prioritise; names exact filename patterns; lists companion `.md` files for back-linking. Paired with `10_source_material/screenshots/capture_packet_for_adam.md` as the day-of working guide.
