---
doc_type: spec
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [design_tokens, color, visual_identity, accessibility]
related:
  - 09_design_system/tokens.md
  - 07_brand_world/visual_positioning.md
  - 09_design_system/accessibility.md
---

# Color

## Purpose

Define the colour system for MixHouse, neutrals, accents, semantic states, and the rules that keep it disciplined across surfaces and seasons.

## Key Takeaways

- The base palette is neutral and high-contrast. Accents are seasonal.
- Dark mode is the design default; light mode is a parallel variant.
- Every colour token is checked for WCAG 2.2 AA contrast against its intended surface.
- No EDM-stereotype neon palette anywhere in the system.

## Core Content

### Palette Structure

Two layers:

1. **Foundation**: fixed across seasons. Neutrals, ink, signal states.
2. **Season Accent**: limited palette swapped per season to reflect the residency location.

### Foundation Tokens

| Token | Role | Approximate value (dark mode) |
| --- | --- | --- |
| `surface-base` | Default page background | Near-black, low-saturation. |
| `surface-elevated` | Cards, panels | One step lighter than base. |
| `surface-inverse` | Light surface inside dark page | Off-white. |
| `ink-primary` | Default text on dark surface | Near-white. |
| `ink-secondary` | Secondary text | ~70% opacity of primary. |
| `ink-tertiary` | Metadata, captions | ~50% opacity. |
| `ink-on-inverse` | Text on light surface | Near-black. |
| `border-subtle` | Subtle dividers | Low-contrast line. |
| `border-strong` | Strong dividers | Mid-contrast. |
| `state-success` | Confirmation | Single restrained green. |
| `state-warning` | Caution | Single restrained amber. |
| `state-error` | Errors | Single restrained red. |
| `state-info` | Information | Single restrained blue. |

### Season Accent

Each season chooses a small accent set (typically 2 hues) tied to the residency location's character. Examples (illustrative):

| Season concept | Accent direction |
| --- | --- |
| Ibiza summer | Sun-orange + Mediterranean blue. |
| Berlin year-round | Cool grey + signal magenta. |
| Mexico City coast | Bone + jungle green. |
| Athens / Aegean | Marble + cobalt. |

Accents are used sparingly: hero accents, CTA highlights, link emphasis. They are never the dominant brand colour.

### Light Mode

A parallel surface / ink palette inverted from dark. Light mode is supported (accessibility, print) but the brand default is dark.

### Contrast Rules

- Text on background: 4.5:1 minimum for body, 3:1 minimum for large display.
- Interactive elements (links, buttons): contrast at default state and focus state.
- Focus indicators are visible against any surface (3:1 minimum).
- See `09_design_system/accessibility.md`.

### Anti-Patterns

- Acid greens, hot pinks, oranges-on-black neon stack.
- Multi-accent gradients.
- Glowing text effects.
- Pure black (`#000`) and pure white (`#fff`) as default ink, use near-black / near-white for warmth and reading comfort.

### Usage Patterns

- Body type uses `ink-primary` on `surface-base`.
- Section divisions use `border-subtle`, not heavy colour changes.
- CTAs use foundation ink against an accent fill, not the reverse.
- Hover and focus states are subtle elevation + outline; not colour shifts.

### Implementation

- Tokens defined as CSS custom properties.
- Theme switching at the CSS root level (`[data-theme="dark"]`, `[data-theme="light"]`).
- Season accent swapped via a season class on the root.

### Photography Treatment

- Photography should breathe. Avoid heavy colour overlays.
- Where overlay is needed for legibility, use a subtle gradient from foundation tokens.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | WCAG contrast minimums | W3C WCAG 2.2 | 2026-05-20 | A |
| 2 | Dark-mode editorial precedent | Apple TV+, A24 web | 2026-05-20 | B |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Dark mode default reads moody." | Dark default is cinematic. Light mode exists for accessibility and print contexts. |
| "Accent should be fixed across seasons for brand recognition." | Brand recognition lives in type, layout, and tone, not accent. Variable accent connects the brand to the season's place. |

## Website Implications

- Tokens implemented as CSS variables; components reference semantic names only.
- Season transitions implemented via root-level class swap with motion-safe transition.

## Open Questions

- Pilot season accent, depends on location lock.
- Print palette equivalence (for press kit).
- Brand wordmark lockup colour usage rules.

## Change Log

- 2026-05-20, Initial colour system scaffolded.
