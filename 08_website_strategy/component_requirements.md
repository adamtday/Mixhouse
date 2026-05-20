---
doc_type: brief
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [component_requirements, sitemap, design_system, media_behavior]
related:
  - 08_website_strategy/sitemap.md
  - 08_website_strategy/page_briefs/home.md
  - 09_design_system/components.md
  - 09_design_system/media_behavior.md
  - 09_design_system/motion.md
---

# Component Requirements

## Purpose

List every UI component the MixHouse website depends on, the behaviour it must implement, and where it's used across pages — so design and engineering can build a reusable component library rather than per-page bespoke work.

## Key Takeaways

- The site is built from ~20 reusable components, no more.
- Each component is media-aware (image, video, audio behave consistently across breakpoints).
- All components conform to `09_design_system/tokens.md` and `09_design_system/accessibility.md`.
- Motion is opt-in by prefers-reduced-motion.

## Core Content

### Component Inventory

#### Layout

- **Container** — width-aware horizontal wrapper.
- **Section** — vertical-rhythm block with optional bleed.
- **Grid** — responsive grid primitive.

#### Hero / Editorial

- **CinematicHero** — looping video / image backdrop with type and CTA.
- **EditorialSpread** — image left / right with editorial copy.
- **Pullquote** — single large quote or stat.
- **Manifesto** — paragraph-length editorial block.

#### Media

- **VideoPlayer** — autoplay-muted by default, accessible controls, captions.
- **VideoTeaser** — looping muted clip with play-to-full handoff.
- **AudioPlayer** — track preview, waveform optional, DSP-link CTAs.
- **MediaCarousel** — sequenced image/video container.

#### Navigation

- **GlobalNav** — top navigation; sticky on scroll; collapses on mobile.
- **Footer** — links + legal + social.
- **CTABanner** — full-width call-to-action band.

#### Data / Argument

- **FlywheelDiagram** — interactive franchise flywheel (Business page).
- **CompetitiveMatrix** — multi-row capability comparison table.
- **TimelineRail** — horizontal scrolling timeline (season arc, milestones).
- **EvidenceCard** — citation block with reliability tier.

#### Forms / Conversion

- **NewsletterForm** — email capture.
- **CastingForm** — multi-step talent application (only on casting CTA flow).
- **MaterialsGate** — gated request form for investor / broadcaster / sponsor.
- **ContactForm** — segmented inbound routing.

#### Content

- **AdvisorTile** — advisor portrait + name + bio.
- **ContestantTile** — contestant portrait + name + city + sub-genre.
- **ReleaseCard** — track artwork + DSP links + metadata.
- **EventCard** — date / venue / city / ticket link.

#### Microcopy

- **InlineCitation** — superscript or marker linking to evidence row.
- **TermTooltip** — definition surface for terms from `01_master_context/glossary.md`.

### Cross-Component Behaviour

- All media respects `prefers-reduced-motion`.
- All forms are keyboard-navigable.
- All cards support a "minimal" variant for season-mode density.
- All grids collapse to single column at the smallest breakpoint.
- All hover states have a touch equivalent.

### State Management

- No global store required at launch.
- CMS-driven content for season-mode components (contestants, releases, events).
- Form state held locally; submission via CRM partner.

### Loading and Performance

- Lazy-load all below-the-fold media.
- Use AVIF / WebP with JPG fallback.
- Limit hero looping video to 4–8s, ≤ 2MB encoded.
- Use `srcset` and `sizes` correctly across breakpoints.

### Accessibility

- WCAG 2.2 AA target.
- Captions on all video.
- Reduced-motion variants for all motion-heavy components.
- See `09_design_system/accessibility.md`.

### Internationalisation

- All components accept locale-aware copy.
- Date / time formatting locale-aware.
- Track titles and producer names are never translated.

### Page-to-Component Map

| Page | Primary components |
| --- | --- |
| Home | CinematicHero, Manifesto, FlywheelDiagram (teaser), EvidenceCard, NewsletterForm. |
| The Show | CinematicHero, EditorialSpread, TimelineRail, ContestantTile (mock), CastingForm. |
| The World | CinematicHero, MediaCarousel, AdvisorTile (preview), EditorialSpread. |
| Business | EditorialSpread, FlywheelDiagram, CompetitiveMatrix, EvidenceCard, MaterialsGate. |
| Advisors | AdvisorTile grid, EditorialSpread, ContactForm. |
| Materials | MaterialsGate, EditorialSpread. |
| Contact | ContactForm. |

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Core Web Vitals thresholds | Google web.dev | 2026-05-20 | A |
| 2 | WCAG 2.2 AA spec | W3C WCAG | 2026-05-20 | A |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Why no design system before content?" | The design system grows with the components in this list; we don't pre-design abstractions. |
| "20 components is small." | The site is intentionally narrow. Custom one-off blocks are anti-pattern — see `07_brand_world/anti_patterns.md`. |

## Website Implications

- This file is the source for the Cursor task list in `11_outputs/cursor_tasks/` once build kicks off.
- Each component spec eventually gets a Claude design prompt in `11_outputs/claude_design_prompts/`.

## Open Questions

- Framework choice (Next.js vs Astro vs custom).
- CMS choice (Sanity / Contentful / custom).
- CRM and form-submission stack.

## Change Log

- 2026-05-20 — Initial component inventory drafted.
