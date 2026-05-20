---
doc_type: brief
status: draft
confidentiality: investor
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [site_objectives, audience, kpi, progressive_disclosure]
related:
  - 08_website_strategy/sitemap.md
  - 08_website_strategy/progressive_disclosure_model.md
  - 01_master_context/audience_matrix.md
  - 05_business_model/platform_extensions.md
---

# Site Objectives

## Purpose

State exactly what the MixHouse public website is for, what it must achieve for each audience, and the measurable success criteria for the launch and ongoing operations.

## Key Takeaways

- The site is a brand-defining surface, not a brochure. It signals quality and ambition before content does.
- It serves six audiences via progressive disclosure (see `08_website_strategy/progressive_disclosure_model.md`).
- It captures direct audience (email, follows, pre-saves), the asset that compounds.
- Pre-pilot, it carries no commercial pricing or detailed financials. Investor/broadcaster materials are gated.

## Core Content

### Primary Objectives (by audience)

| Audience | Objective | Primary KPI |
| --- | --- | --- |
| Viewer / fan | Magnetise; build anticipation; collect email; drive pre-save when music exists. | Email captures, pre-save count, return visits. |
| Talent / producer | Convert to casting applications. | Casting applications, qualified-applicant rate. |
| Advisor / industry | Reassure tone and credibility; surface advisor list. | Inbound advisor / referral inquiries. |
| Broadcaster / streamer | Surface format + creative + casting evidence; route to gated materials. | Gated-materials access requests. |
| Investor | Surface thesis + business model framing; route to gated materials. | Investor inbound inquiries. |
| Sponsor | Surface partnership philosophy; route to gated materials. | Sponsor inbound inquiries. |

### Secondary Objectives

- Anchor brand visual identity across every external surface (LinkedIn, press, email, deck links).
- Provide a stable home for the trailer, sizzle, and press kit.
- Operate as a CRM front-door for the franchise platform.
- Reduce cost-per-qualified-applicant in casting.

### Non-Objectives

- The site is not an editorial publication.
- The site is not a video service.
- The site is not a community forum.
- The site does not display detailed financial figures.
- The site does not display unconfirmed partners or advisors.

### Pre-Launch vs Launch vs Season Modes

| Mode | What the site shows |
| --- | --- |
| **Pre-launch (pre-pilot)** | Brand world, premise teaser, advisor list (placeholder), casting CTA, gated materials. |
| **Launch (pilot ready)** | Trailer, premise, advisor list, gated press / investor materials, casting open. |
| **Season mode (S1 in-flight)** | Live season hub, episode schedule, contestant profiles, release links, live event tickets. |
| **Off-season** | Catalogue, alumni, next-season tease, casting open. |

### Success Criteria (Launch: provisional thresholds)

- Email captures: target threshold per week.
- Casting applications: target per week.
- Gated-materials requests: by audience (investor / broadcaster / sponsor) per month.
- Time-on-page benchmarks for hero + show + business model pages.
- Site performance: LCP < 2.5s, CLS < 0.1, INP < 200ms.
- Accessibility: WCAG 2.2 AA conformance.

Concrete numbers to be calibrated post-launch and stored in `11_outputs/website_copy/` reporting docs.

### Stack and Architecture Direction (separate from content strategy)

- Static-first / framework-light; high cinematic media weight.
- Direct CMS surface for season hub (light CMS, not Wordpress-heavy).
- CRM integration (Klaviyo / Customer.io class).
- DSP-link integration (Linkfire / Feature.fm).
- Analytics: privacy-first first-party + DSP attribution.

Detailed in `08_website_strategy/component_requirements.md`.

### Confidentiality Surfaces

The public site is `confidentiality: public`. Investor and broadcaster materials live behind gated forms with NDA-on-access; sponsor materials likewise. See `08_website_strategy/page_briefs/materials.md`.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Email capture benchmarks for music IP launches | MailerLite / Klaviyo benchmarks (target) | n/a | B (target) |
| 2 | Core Web Vitals thresholds | Google web.dev | 2026-05-20 | A |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Why launch a site before there's a show?" | Because the site is a credibility surface for every other workstream. Casting, investors, advisors all look here first. |
| "Why no detailed numbers publicly?" | They belong in gated investor materials. Public numbers age badly and can mis-anchor coverage. |

## Website Implications

- This file is the parent for every other file in `08_website_strategy/`.
- Page briefs in `08_website_strategy/page_briefs/` each reference an objective from this file.

## Open Questions

- Lock concrete KPI thresholds (Q+1).
- Site stack final choice (Next.js / Astro / custom, owner: tech lead).
- Domain strategy (mixhouse.com vs alternates).

## Change Log

- 2026-05-20, Initial objectives drafted.
