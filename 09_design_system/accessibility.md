---
doc_type: spec
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [accessibility, design_system, motion, media_behavior]
related:
  - 09_design_system/tokens.md
  - 09_design_system/color.md
  - 09_design_system/motion.md
  - 09_design_system/media_behavior.md
  - 09_design_system/components.md
---

# Accessibility

## Purpose

Define the accessibility standards MixHouse meets, across visual, motion, keyboard, screen-reader, and content dimensions, so the site is inclusive by default, not retrofitted.

## Key Takeaways

- WCAG 2.2 Level AA is the binding standard.
- Accessibility is enforced at component level via the design system, not added page-by-page.
- All motion respects `prefers-reduced-motion`; all colour passes contrast minimums; all interactive elements are keyboard navigable.
- Accessibility QA is part of the launch checklist, not a post-launch follow-up.

## Core Content

### Standard

- **WCAG 2.2 Level AA** as the binding target across all primary surfaces.
- Selected AAA criteria adopted where reasonable (contrast 7:1 on body type, link colour contrast 3:1).

### Colour and Contrast

- Body text contrast ≥ 4.5:1 against background.
- Large text (≥ 24px) contrast ≥ 3:1.
- Interactive elements contrast ≥ 3:1 against adjacent colours.
- Focus indicators ≥ 3:1 against the focused element's background.
- Colour is never the only signal (state, link, etc., also use icon, weight, or underline).

### Typography

- Minimum body type 16px equivalent.
- Line lengths 60–80 characters.
- Line-height 1.5+ for body.
- Text can be resized 200% without loss of functionality.

### Motion

- All motion respects `prefers-reduced-motion`.
- Auto-rotating content (carousels, parallax, hero loops) freezes when reduced motion is requested.
- Vestibular triggers (large screen-shake, parallax exceeding 24px) avoided entirely.

### Media

- All video has captions and a transcript.
- All audio has visible controls and a descriptive label.
- All images have meaningful alt text or are marked decorative.
- No autoplay audio.

### Keyboard

- Every interactive element is reachable via Tab.
- Focus order matches reading order.
- Focus indicators visible on every focusable element.
- Skip-to-content link at the top of each page.
- Custom components (carousels, accordions, dialogs) follow ARIA Authoring Practices.

### Screen Reader

- Semantic HTML used by default (`<nav>`, `<main>`, `<article>`, `<section>`, `<button>`, `<a>`).
- ARIA only when semantic HTML can't express the intent.
- Live regions used judiciously for dynamic updates (form errors, async results).
- Decorative SVG marked `aria-hidden`; meaningful SVG carries `<title>` and `<desc>`.

### Forms

- Every input has a visible label.
- Errors are announced and linked via `aria-describedby`.
- Required fields are marked accessibly.
- Submission state announced (loading, submitted, errored).

### Internationalisation

- `lang` attribute set on the HTML root.
- Locale-specific number, date, and currency formatting.
- Direction support (LTR / RTL) considered for future Arabic / Hebrew localisation.

### Cognitive Accessibility

- Plain-language summaries on long pages (Business Model).
- Glossary tooltips for industry terms (using `TermTooltip` component).
- Consistent navigation across pages.

### Testing

- Automated checks: axe, Lighthouse accessibility audit, ESLint a11y rules.
- Manual checks: keyboard traversal, screen-reader pass (VoiceOver + NVDA).
- Reduced-motion testing on every component.
- Pre-launch full audit by an external accessibility partner where budget permits.

### Anti-Patterns

- Placeholder text as a substitute for labels.
- "Click here" link text.
- Focus styles removed via `outline: none` without a replacement.
- Hover-only interactions without touch / keyboard equivalents.
- Auto-playing audio.
- Carousels that rotate too fast for cognitive processing.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | WCAG 2.2 standard | W3C WCAG | 2026-05-20 | A |
| 2 | ARIA Authoring Practices | W3C WAI ARIA APG | 2026-05-20 | A |

## Objections Answered

| Objection | Response |
| --- | --- |
| "AA is enough, AAA is over-investment." | Mostly true; we adopt AAA only where the additional discipline aligns with the brand (contrast, readability). |
| "Accessibility slows down cinematic ambition." | False. Cinematic ambition that breaks accessibility breaks the brand's audience expansion. |

## Website Implications

- Every component spec in `09_design_system/components.md` lists its accessibility requirements.
- Launch checklist includes a full accessibility audit.

## Open Questions

- External accessibility partner choice.
- Captions workflow for short-form clips (auto vs reviewed).
- Whether to commit to WCAG 2.2 conformance public statement.

## Change Log

- 2026-05-20, Initial accessibility spec drafted.
