---
doc_type: page_brief
status: draft
confidentiality: public
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [page_brief, home, atmosphere, progressive_disclosure]
related:
  - 08_website_strategy/site_objectives.md
  - 08_website_strategy/progressive_disclosure_model.md
  - 08_website_strategy/component_requirements.md
  - 07_brand_world/visual_positioning.md
  - 07_brand_world/tone_of_voice.md
  - 01_master_context/one_sentence_positioning.md
---

# Home Page Brief

## Purpose

Define the structure, content, and atmosphere of the MixHouse home page, the surface that decides, in five seconds, whether a visitor stays.

## Key Takeaways

- Home is L1 (Atmosphere) per the progressive disclosure model.
- One looping cinematic moment, one editorial line, one CTA above the fold.
- Below the fold: light glimpses of show, world, business, and casting. No deep dives.
- The page must feel like a film opening, not a brochure.

## Core Content

### Disclosure Layer

L1 (Atmosphere). Light L2 signal as you scroll.

### Audience Priority

| Order | Audience | What they get |
| --- | --- | --- |
| 1 | Fan / scene | Cinematic atmosphere; the show is real and beautiful. |
| 2 | Talent | One signal that this is for real producers; clear path to casting. |
| 3 | Investor / broadcaster / sponsor | Visual ambition that signals premium; clear path to Materials. |

### Above-the-Fold

- **Backdrop:** single looping cinematic video. Drawn from `07_brand_world/moodboard_references.md`.
- **Headline:** one editorial line (likely: `Live in. Create together. Headline the world.`).
- **Sub-line:** the public-facing variant from `01_master_context/one_sentence_positioning.md`.
- **CTA primary:** Watch the trailer (when available) / Get on the list (pre-launch).
- **Navigation:** minimal global nav; visible but unobtrusive.

### Below-the-Fold Structure

1. **The Premise (light)**: one paragraph synopsis + a still or short clip. Links to The Show.
2. **The World (light)**: a media carousel, residency, venue, faces. Links to The World.
3. **The Numbers (quiet)**: three single-stat lines about the scene (e.g. "[X] festivals sold out in 2026", "[Y] producers active globally", "[Z] tracks streamed daily"). Each cites an A/B source. Links to Business.
4. **The Voices (advisor strip)**: small tile row, advisor portraits + names + scene affiliations. Links to Advisors.
5. **For Producers**: one short line + casting CTA.
6. **For Partners**: one short line + Materials gate link.
7. **Newsletter capture**: quiet, editorial, no hype.

### Tone

- Editorial, declarative, quiet. See `07_brand_world/tone_of_voice.md`.
- No exclamation marks, no hype, no marketing emojis.

### Components Used

See `08_website_strategy/component_requirements.md`. Specifically:

- CinematicHero
- Manifesto
- MediaCarousel
- EvidenceCard (x3 for The Numbers)
- AdvisorTile (preview row)
- NewsletterForm

### Copy Sources

| Section | Source file |
| --- | --- |
| Hero line | `01_master_context/one_sentence_positioning.md` (fan variant) |
| Premise | `02_show_bible/show_premise.md` |
| World imagery | `07_brand_world/moodboard_references.md` |
| Numbers | `03_market_research/*.md` (cite-able rows only) |
| Advisors | `08_website_strategy/page_briefs/advisors.md` (preview) |
| Newsletter | Microcopy per `07_brand_world/tone_of_voice.md` |

### Performance and Media Targets

- LCP < 2.5s.
- Hero video ≤ 2MB encoded, 4–8s loop, autoplay-muted, lazy-decoded.
- All decorative motion respects `prefers-reduced-motion`.

### Open Questions Specific to This Page

- Final hero line, to lock with copy review.
- Initial advisor strip, depends on advisor confirmation.
- Pre-launch CTA, newsletter vs trailer placeholder vs casting depending on phase.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Above-the-fold attention thresholds | Nielsen Norman Group (target) | n/a | B (target) |
| 2 | Core Web Vitals targets | Google web.dev | 2026-05-20 | A |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Home should explain the show on first scroll." | Home should magnetise, not explain. Explanation lives on The Show. |
| "We need pricing or business info on home." | No, confidentially gated. Substance is L3 / L4. |

## Website Implications

- This brief generates `11_outputs/website_copy/home_page_copy_*.md` once finalised.
- The home page's CinematicHero is the most expensive asset; capture moodboard inputs are required before build.

## Open Questions

- Final hero treatment per launch phase.
- Initial advisor strip composition.
- Newsletter capture incentive (early access? track drops?).

## Change Log

- 2026-05-20, Initial home page brief drafted.
