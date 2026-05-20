---
doc_type: spec
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [design_tokens, typography, visual_identity, brand_voice]
related:
  - 09_design_system/tokens.md
  - 07_brand_world/visual_positioning.md
  - 07_brand_world/tone_of_voice.md
---

# Typography

## Purpose

Define the type system for MixHouse — families, scale, leading, tracking, and usage rules — so every surface reads as a single editorial voice.

## Key Takeaways

- Two families: one editorial display (heads, hero, pull quotes); one working sans (body, UI).
- Scale follows a deliberate, irregular step (not a uniform multiplier) to encourage editorial pacing.
- Tight tracking on display, generous tracking on small caps and microcopy.
- Type does the heavy lifting visually — colour and motion follow.

## Core Content

### Families (working choices, subject to design partner review)

| Role | Family direction | Notes |
| --- | --- | --- |
| **Display** | A modern editorial serif *or* a precise technical sans. | Final choice TBD. References: Söhne, Editorial New, Reckless, GT Sectra. |
| **Working** | A neutral, technical sans. | References: Söhne, Inter, IBM Plex Sans. |
| **Mono (sparingly)** | Technical mono for data, captions, timestamps. | References: IBM Plex Mono, JetBrains Mono. |

### Scale

| Token | Use | Approx size |
| --- | --- | --- |
| `type-display-xl` | Hero / cover | 88–128px responsive |
| `type-display-lg` | Section heads / quotes | 56–80px |
| `type-display-md` | Subsection heads | 40–56px |
| `type-h1` | Page H1 | 32–40px |
| `type-h2` | Page H2 | 24–32px |
| `type-h3` | Page H3 | 20–24px |
| `type-body-lg` | Lead paragraph | 18–20px |
| `type-body` | Body | 16–17px |
| `type-body-sm` | Captions / small body | 14–15px |
| `type-micro` | Microcopy / metadata | 12–13px |

Fluid sizing via `clamp()` recommended.

### Leading (line-height)

| Use | Line-height |
| --- | --- |
| Display | 1.0–1.05 |
| Heading | 1.15–1.2 |
| Lead paragraph | 1.4 |
| Body | 1.55–1.6 |
| Microcopy | 1.4 |

### Tracking (letter-spacing)

| Use | Tracking |
| --- | --- |
| Display | -1% to -2% |
| Heading | -0.5% to -1% |
| Body | 0 |
| Microcopy / UI labels | +1% to +2% (especially uppercase) |
| All-caps small | +6% to +8% |

### Usage Rules

- Display family is reserved for hero, section heads, and pull quotes.
- Headings use the working sans by default; display family used only when the page calls for editorial gravity.
- Body always working sans.
- No mixing more than two families per page.
- No script faces. No condensed sans. No outlined or stroked variations.

### Hierarchy Examples

- **Hero:** `type-display-xl`, display family, tight tracking.
- **Manifesto:** `type-display-md`, display family.
- **Section head:** `type-h1`, working sans, modest weight.
- **Body:** `type-body`, working sans, regular.
- **Caption / metadata:** `type-micro`, mono.

### Accessibility

- Body minimum 16px equivalent.
- Contrast ratios meet WCAG 2.2 AA at all sizes.
- Line lengths 60–80 characters for sustained reading.

### Internationalisation

- Display and working families must support extended Latin (territory adaptation).
- Cyrillic / Greek / CJK support is a future requirement.

### Tools and Files

- Font files stored under license per family; not committed to repo.
- Webfont delivery via self-hosted or licensed CDN.
- Font preloading on critical pages (hero).

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | WCAG type contrast and size rules | W3C WCAG 2.2 | 2026-05-20 | A |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Why two families?" | One does display; one does work. Single-family systems lose editorial gravity. |
| "Mono is dated." | Used sparingly, mono signals craft and data — exactly the show's voice. |

## Website Implications

- All components in `09_design_system/components.md` cite type tokens, not raw sizes.
- Trailers and key art use the same display family for cross-surface consistency.

## Open Questions

- Final display family choice — design partner.
- Final working sans choice.
- Licensing scope (web only vs print, social, on-screen).

## Change Log

- 2026-05-20 — Initial type system scaffolded.
