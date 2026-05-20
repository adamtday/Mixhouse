---
doc_type: spec
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [motion, design_tokens, visual_identity, accessibility]
related:
  - 09_design_system/tokens.md
  - 09_design_system/components.md
  - 09_design_system/accessibility.md
  - 07_brand_world/visual_positioning.md
---

# Motion

## Purpose

Define how MixHouse moves, durations, easings, intent, so motion serves cinematic atmosphere rather than decorating it.

## Key Takeaways

- Motion is slow, considered, and content-led.
- All motion respects `prefers-reduced-motion`.
- Easings favour custom curves over default `ease`: closer to film than UI.
- No bouncing, no parallax-for-parallax's-sake, no kinetic typography flourish.

## Core Content

### Duration Tokens

| Token | Value | Use |
| --- | --- | --- |
| `motion-duration-instant` | 80ms | UI feedback (button press) |
| `motion-duration-fast` | 180ms | Subtle UI transitions |
| `motion-duration-base` | 320ms | Default transitions |
| `motion-duration-slow` | 560ms | Section reveals |
| `motion-duration-cinematic` | 1200ms | Hero / location reveals |
| `motion-duration-loop-long` | 4000–8000ms | Background loops |

### Easing Tokens

| Token | Curve | Use |
| --- | --- | --- |
| `motion-ease-out` | cubic-bezier(0.22, 1, 0.36, 1) | Default reveal |
| `motion-ease-in-out` | cubic-bezier(0.65, 0, 0.35, 1) | Symmetric transitions |
| `motion-ease-cinematic` | cubic-bezier(0.16, 1, 0.3, 1) | Slow hero entries |
| `motion-ease-linear` | linear | Background loops, scroll-tied motion |

### Motion Patterns

- **Fade and rise.** New content fades in while rising 8–16px. Default for most reveals.
- **Slow zoom.** Hero background images zoom 1.0 → 1.02 across 10s+ for life.
- **Single-take cuts.** Video components avoid cut transitions; let frames hold.
- **Scroll-tied parallax.** Subtle (8–16px) and only on hero or section anchors. Never multi-layer.

### Reduced Motion

When `prefers-reduced-motion: reduce`:

- Fade-only reveals; no rise / scale / parallax.
- Loops freeze on first frame.
- Hero motion replaced with a static image.

This is enforced at component level; not a global override that breaks UI feedback.

### Anti-Patterns

- Flashy transitions between sections.
- Bouncing buttons or cards.
- Kinetic typography stunts unrelated to content.
- Confetti / particle effects.
- Triggering motion on hover for primary content.
- Auto-rotating carousels (carousels rotate only on user interaction).

### Cinematic Mode

For hero and editorial components:

- Hold durations long (≥ 560ms).
- Use `motion-ease-cinematic`.
- Pair motion with sound where appropriate (subtle).
- Treat the screen like a frame, not a UI canvas.

### Performance

- All motion respects 60fps target on low-end devices.
- Heavy motion is opt-in (intersection observer triggers; not always-on).
- Video loops compressed to ≤ 2MB for hero, ≤ 500KB for inline.

### Sound and Motion

- Hero loops are muted by default.
- Audio components have visible controls.
- Motion + sound combination requires explicit user start.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Cinematic easing curve references | Industry motion design references (target) | n/a | B (target) |
| 2 | `prefers-reduced-motion` spec | MDN | 2026-05-20 | A |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Slow motion feels sluggish on mobile." | At mobile sizes, durations scale down via media queries. Cinematic on desktop, responsive on mobile. |
| "Why no parallax?" | Heavy parallax breaks the cinematic illusion. Subtle yes; layered no. |

## Website Implications

- All components in `09_design_system/components.md` import motion tokens, not raw durations.
- Hero treatments per `08_website_strategy/page_briefs/home.md` and `the_world.md` rely on cinematic easings.

## Open Questions

- Cinematic easing values, final tuning with design partner.
- Sound + motion editorial moments, owner: trailer / brand team.

## Change Log

- 2026-05-20, Initial motion system scaffolded.
