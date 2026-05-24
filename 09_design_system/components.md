---
doc_type: spec
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [components, design_system, component_requirements, schema]
related:
  - 09_design_system/tokens.md
  - 09_design_system/typography.md
  - 09_design_system/color.md
  - 09_design_system/motion.md
  - 09_design_system/media_behavior.md
  - 08_website_strategy/component_requirements.md
---

# Components

## Purpose

Specify the behaviour, states, and token consumption of the component library used by MixHouse's website. This file is the bridge between design tokens and shipped components.

## Key Takeaways

- All components live in a single library; each component declares its tokens.
- Every component documents: API, states, accessibility, motion, content slots.
- No bespoke per-page components, variants exist instead.
- The component list mirrors `08_website_strategy/component_requirements.md`; this file fills in the behavioural detail.

## Core Content

### Component API Convention

Each component declares:

| Field | Description |
| --- | --- |
| `name` | Component name (e.g. `CinematicHero`). |
| `purpose` | One-line purpose statement. |
| `props` | Public API. |
| `slots` | Content insertion points. |
| `tokens_used` | Which tokens it consumes. |
| `states` | Default, hover, focus, active, disabled, loading. |
| `motion` | Which motion tokens it consumes. |
| `accessibility` | Required ARIA / keyboard support. |

### Reference Specifications

#### CinematicHero

- **Purpose**: hero with looping video / image backdrop + editorial type + CTA.
- **Props**: `backdrop` (video / image / poster), `headline`, `subline`, `cta`.
- **Slots**: backdrop, headline, subline, cta.
- **Tokens used**: `type-display-xl`, `surface-base`, `ink-primary`, `motion-duration-cinematic`, `motion-ease-cinematic`.
- **States**: paused (reduced-motion), playing (default), CTA hover/focus.
- **Motion**: slow zoom on backdrop; fade-and-rise on type.
- **Accessibility**: hero copy in semantic heading; CTA is a real link/button; reduced-motion swaps to poster.

#### EditorialSpread

- **Purpose**: image-left/right with editorial copy.
- **Props**: `image`, `imagePosition`, `headline`, `body`, `caption`.
- **Slots**: image, copy, optional citation.
- **Tokens used**: `type-display-md`, `type-body-lg`, generous `space-16`.
- **States**: default; image lazy-loaded.
- **Motion**: fade-and-rise on intersection.
- **Accessibility**: image alt text mandatory; caption uses `<figcaption>`.

#### FlywheelDiagram

- **Purpose**: interactive franchise flywheel diagram.
- **Props**: `assets` (array of 7 asset descriptors).
- **Slots**: none; data-driven.
- **Tokens used**: `motion-duration-base`, semantic accents from `color`.
- **States**: default, hover (per node), focus (keyboard).
- **Motion**: slow rotational pace; respects reduced-motion (static fallback).
- **Accessibility**: full content available as a text equivalent; keyboard navigable; ARIA roles for diagram parts.

#### CompetitiveMatrix

- **Purpose**: comparison table of formats across capability columns.
- **Props**: `rows`, `columns`.
- **Slots**: cell renderer (icon / text).
- **Tokens used**: `type-body`, `border-subtle`, `border-strong`.
- **States**: default, future: filter / sort.
- **Motion**: none.
- **Accessibility**: semantic `<table>` with proper headers.

#### TimelineRail

- **Purpose**: horizontal scrolling timeline (season arc / milestones).
- **Props**: `items` (array of dated entries).
- **Slots**: item renderer.
- **Tokens used**: `space-*`, `type-body-sm`, `type-micro`.
- **States**: default, hover, focused item.
- **Motion**: scroll-tied; respects reduced-motion (static stacked layout).
- **Accessibility**: scroll region accessible via keyboard; landmarks for each item.

#### VideoPlayer / VideoTeaser

- **Purpose**: video playback.
- **Props**: `src`, `poster`, `captions`, `autoplay`, `loop`, `muted`.
- **Slots**: none.
- **Tokens used**: `radius-xl`, `motion-duration-base`.
- **States**: loading, playing, paused, error, captions-on/off.
- **Motion**: none beyond playback.
- **Accessibility**: captions required; controls visible; respects reduced-motion (autoplay disabled by default).

#### AudioPlayer

- **Purpose**: track preview with DSP links.
- **Props**: `track`, `previewSrc`, `dspLinks`.
- **Slots**: artwork, metadata, controls.
- **Tokens used**: `type-body-sm`, `radius-md`, motion tokens.
- **States**: playing, paused, loading, error.
- **Accessibility**: controls labelled; transcript available where applicable.

#### Forms (NewsletterForm, CastingForm, MaterialsGate, ContactForm)

- **Common props**: fields, submit handler, success / error states.
- **Tokens used**: typography body + microcopy, radius-md, border tokens.
- **States**: empty, valid, invalid, submitting, submitted, errored.
- **Accessibility**: labels associated with inputs; error messages linked via aria-describedby; focus rings visible.

#### Tiles (AdvisorTile, ContestantTile, ReleaseCard, EventCard)

- **Common props**: image, title, supporting metadata, links.
- **Tokens used**: `radius-lg`, `space-8`, `type-body-sm`.
- **States**: default, hover (subtle elevation), focus.
- **Accessibility**: entire tile is one focusable link; image has alt.

### Variants vs New Components

- Prefer adding a variant to an existing component.
- New components require a justification entry in this file's Change Log.

### Storybook / Component Documentation

- Each component shipped with its own Storybook story (or equivalent).
- Stories must cover all states and the reduced-motion variant.
- Story descriptions reference this file.

### Code Hygiene

- Components are typed (TypeScript) when shipping in code.
- No inline styles, tokens only.
- No raw colour / size values in component code.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Accessibility requirements per component type | W3C WAI-ARIA / WCAG 2.2 | 2026-05-20 | A |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Spec is verbose." | Components are the unit of reuse. Specs save 10x their cost in build and review. |
| "Storybook is overhead." | It's the documentation surface; reduces cross-team friction. |

## Website Implications

- The build follows this file's specs verbatim.
- Outputs in `11_outputs/claude_design_prompts/` use these specs as canonical input.

## Open Questions

- Final framework / library choice (component framework dependency).
- Storybook vs lightweight alternative.
- Test coverage requirements per component.

## Change Log

- 2026-05-20, Initial component specs drafted.
