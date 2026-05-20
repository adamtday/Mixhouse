---
doc_type: spec
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [media_behavior, design_system, performance, accessibility]
related:
  - 09_design_system/components.md
  - 09_design_system/motion.md
  - 09_design_system/accessibility.md
  - 08_website_strategy/component_requirements.md
---

# Media Behaviour

## Purpose

Define how images, video, and audio behave across MixHouse surfaces — formats, sizes, lazy-loading, autoplay rules, accessibility, and performance budgets.

## Key Takeaways

- Visual ambition is enforced by media quality; performance discipline keeps it from breaking the experience.
- Default formats: AVIF / WebP with JPG fallback for images; H.265 / VP9 for video where supported.
- Autoplay only when muted and below set encoded weight.
- All video has captions; all audio respects user-initiated playback.

## Core Content

### Image Behaviour

- **Formats:** AVIF preferred, WebP fallback, JPG only as final fallback.
- **Sizing:** `srcset` and `sizes` correctly defined per breakpoint.
- **Lazy-loading:** `loading="lazy"` for all below-the-fold images.
- **Decoding:** `decoding="async"`.
- **Alt text:** mandatory; descriptive, not decorative ("Aerial shot of the residency at dusk" — not "image").
- **Hero images:** preloaded; LCP candidate clearly defined.

### Video Behaviour

| Surface | Treatment |
| --- | --- |
| Hero loops | Autoplay muted; encoded ≤ 2MB; 4–8s loop; poster image. |
| Inline video | User-initiated; encoded reasonably; captions on. |
| Editorial spreads | Looping muted; encoded ≤ 1MB; optional play-to-full handoff. |
| Trailer (full) | User-initiated; captions on; controls visible. |
| Vertical short-form | Embedded as native player from short-form platforms when needed. |

- **Captions:** required on all video carrying spoken or musical content.
- **Audio:** muted by default; user-initiated for sound.
- **Reduced motion:** hero video swaps to poster image.

### Audio Behaviour

- Always user-initiated.
- Transcript or descriptive label available where music is the content (e.g. a curated mix preview).
- Visible controls (play / pause, scrubber, volume).

### Performance Budgets

| Surface | Initial payload target |
| --- | --- |
| Home above-the-fold | < 1.2MB total |
| Section below-the-fold | lazy-loaded; no impact on LCP |
| Hero looping video | ≤ 2MB encoded |
| Inline video clip | ≤ 1MB encoded |
| Audio preview | ≤ 200KB initial |

### LCP / Core Web Vitals

- LCP < 2.5s on primary pages.
- CLS < 0.1.
- INP < 200ms.

Concrete steps:
- Pre-define image dimensions to prevent layout shift.
- Pre-load critical fonts and LCP images.
- Avoid render-blocking scripts.

### CMS / Content Delivery

- Use an image CDN (e.g. Cloudflare Images, imgix) for on-demand resizing.
- Static export friendly: avoid client-side image processing dependencies.
- Cache aggressively; bust by content hash.

### Accessibility

- Decorative images use `alt=""` and `role="presentation"`.
- Hero loops include `aria-hidden="true"` if purely decorative.
- Captions standards: WebVTT files committed alongside video assets.

### File Naming

- Per `00_system/naming_conventions.md`:
  - `YYYYMMDD_subject_descriptor.ext`
  - Stored under `10_source_material/screenshots/` or `10_source_material/references/` until promoted to production assets.
  - Production assets live in the web project's `public/media/` (out of repo).

### Anti-Patterns

- Autoplay audio.
- Carousels that auto-rotate.
- Lazy-loading the hero LCP image (defeats LCP).
- Inline base64 images larger than 4KB.
- Background-image videos.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Core Web Vitals thresholds | Google web.dev | 2026-05-20 | A |
| 2 | Image format support across browsers | MDN / Can I Use | 2026-05-20 | A |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Performance budget is restrictive on cinematic ambition." | Restriction forces craft. A 2MB hero loop with good encoding looks excellent. |
| "Why captions on muted video?" | When users unmute, captions are already there. Default-on aligns with accessibility. |

## Website Implications

- All component implementations honour these rules.
- Pre-launch QA checklist includes Core Web Vitals against each primary page.

## Open Questions

- CDN choice (Cloudflare Images vs imgix vs custom).
- Captioning workflow (manual vs auto + review).
- Video hosting and delivery pipeline.

## Change Log

- 2026-05-20 — Initial media behaviour spec drafted.
