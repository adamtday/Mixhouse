---
doc_type: spec
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [design_tokens, visual_identity, schema, design_system]
related:
  - 09_design_system/typography.md
  - 09_design_system/color.md
  - 09_design_system/motion.md
  - 09_design_system/components.md
  - 07_brand_world/visual_positioning.md
---

# Design Tokens

## Purpose

Define the canonical design token vocabulary for MixHouse — the atomic primitives (colour, type, spacing, radius, motion) that downstream components and pages reuse.

## Key Takeaways

- Tokens live in one place; components reference them by name, never raw values.
- Token names are semantic ("surface/elevated", "ink/primary"), not visual ("grey-90").
- Tokens are exportable to CSS variables, Tailwind config, and Figma variables.
- Token changes propagate through the system; do not hard-code values anywhere.

## Core Content

### Token Categories

| Category | Description | Owner file |
| --- | --- | --- |
| **Colour** | Surface, ink, accent, state colours. | `09_design_system/color.md` |
| **Typography** | Font families, type scale, line height, tracking. | `09_design_system/typography.md` |
| **Spacing** | Spacing scale used for padding, margin, gap. | This file. |
| **Radius** | Border radius scale. | This file. |
| **Shadow** | Elevation tokens. | This file. |
| **Motion** | Duration, easing tokens. | `09_design_system/motion.md` |
| **Z-index** | Stacking layer tokens. | This file. |
| **Breakpoint** | Responsive breakpoints. | This file. |

### Spacing Scale

Scale based on a 4px base unit (or 0.25rem):

| Token | Value (rem) | Use case |
| --- | --- | --- |
| `space-0` | 0 | reset |
| `space-1` | 0.25 | hairline gaps |
| `space-2` | 0.5 | tight |
| `space-3` | 0.75 | inline |
| `space-4` | 1 | base |
| `space-6` | 1.5 | small block |
| `space-8` | 2 | block |
| `space-12` | 3 | section interior |
| `space-16` | 4 | section gap |
| `space-24` | 6 | major section gap |
| `space-32` | 8 | page rhythm |

### Radius Scale

| Token | Value | Use case |
| --- | --- | --- |
| `radius-none` | 0 | hard edges |
| `radius-sm` | 2px | small UI |
| `radius-md` | 4px | inputs |
| `radius-lg` | 8px | cards |
| `radius-xl` | 16px | media |
| `radius-pill` | 999px | tags / pills |

The brand bias is toward minimal radius — prestige over cute.

### Shadow / Elevation

| Token | Use case |
| --- | --- |
| `shadow-none` | default |
| `shadow-sm` | subtle hover/lift |
| `shadow-md` | floating panels |
| `shadow-lg` | overlays |

Specific values defined in CSS exports. Bias is toward minimal shadow — depth via type and image, not bevel.

### Z-Index

| Token | Layer |
| --- | --- |
| `z-base` | content |
| `z-sticky` | sticky nav |
| `z-overlay` | overlay panels |
| `z-modal` | modals |
| `z-toast` | toasts |
| `z-max` | top of stack |

### Breakpoints

| Token | Min width | Use |
| --- | --- | --- |
| `bp-sm` | 480px | small phone |
| `bp-md` | 768px | tablet portrait |
| `bp-lg` | 1024px | tablet landscape / small laptop |
| `bp-xl` | 1280px | desktop |
| `bp-2xl` | 1536px | large desktop |

Mobile-first defaults; breakpoints scale up only.

### Naming Convention

- Categories: lowercase noun (`color`, `space`, `radius`, `shadow`, `motion`).
- Scale tokens: category + integer/keyword (`space-8`, `radius-lg`).
- Semantic tokens: category + role (`surface-base`, `ink-primary`, `accent-warm`).
- All tokens lowercase, hyphen-separated.

### Export Targets

- CSS custom properties (`--space-4: 1rem`).
- Tailwind config (extending defaults, not replacing).
- Figma variables (synced manually until automation set up).

### Versioning

- Tokens are versioned. Breaking changes (renames, removals) only at semver-major.
- Change Log here is the source of truth.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Design token best practices | Design Tokens W3C Community Group | 2026-05-20 | A |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Why semantic + scale tokens both?" | Components reference semantic tokens; semantic tokens reference scale tokens. This insulates components from raw value churn. |
| "Why so few radius / shadow tokens?" | Restraint is the brand. Adding more loosens the system. |

## Website Implications

- All `08_website_strategy/component_requirements.md` components consume tokens defined here.
- Theme switching (light / dark / season variants) is implemented at the semantic-token layer.

## Open Questions

- Whether to ship a fluid type scale (clamp-based) or fixed-step scale at launch.
- Dark-mode default — likely yes for prestige feel.
- Season-specific accent token overrides — implementation pattern TBD.

## Change Log

- 2026-05-20 — Initial token scaffolding drafted.
