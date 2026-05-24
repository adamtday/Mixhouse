---
doc_type: brief
status: draft
confidentiality: investor
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [sitemap, ia, site_objectives, progressive_disclosure]
related:
  - 08_website_strategy/site_objectives.md
  - 08_website_strategy/progressive_disclosure_model.md
  - 08_website_strategy/page_briefs/home.md
  - 08_website_strategy/page_briefs/the_show.md
  - 08_website_strategy/page_briefs/the_world.md
  - 08_website_strategy/page_briefs/business_model.md
  - 08_website_strategy/page_briefs/advisors.md
  - 08_website_strategy/page_briefs/materials.md
  - 08_website_strategy/page_briefs/contact.md
---

# Sitemap

## Purpose

Lay out the information architecture of the MixHouse public website: pages, their hierarchy, primary content blocks, and navigation across audiences.

## Key Takeaways

- The pre-pilot site has seven primary pages, each with a dedicated page brief.
- Navigation is intentionally narrow, depth lives inside pages, not in nav.
- Investor / broadcaster / sponsor depth lives behind a single "Materials" gate.
- Season mode adds dynamic surfaces (season hub, contestants, releases, tickets) without changing the top-level structure.

## Core Content

### Primary Sitemap (Pre-Pilot / Launch Mode)

```
/                            Home                       (08_website_strategy/page_briefs/home.md)
/the-show                    The Show                   (the_show.md)
/the-world                   The World (brand/look)     (the_world.md)
/business                    Business Model             (business_model.md)
/advisors                    Advisors                   (advisors.md)
/materials                   Materials (gated)          (materials.md)
/contact                     Contact                    (contact.md)
```

Plus utility:

```
/legal                       Legal / privacy / cookies
/sitemap.xml                 Sitemap (search engines)
/robots.txt                  Robots
```

### Season Mode Additions

```
/season/[n]                  Season hub
/season/[n]/episode/[e]      Episode pages
/contestants/[slug]          Contestant profile pages
/music                       Releases hub (links to DSPs)
/live                        Live events + tickets
```

### Navigation

Primary navigation (top-level, always visible):

- The Show
- The World
- Business
- Advisors
- Contact

Materials gate appears as a CTA, not a primary nav item.

Footer navigation:

- Legal / privacy
- Casting CTA
- Materials gate
- Social links
- Press inquiries

### Cross-Page Links

| From | Links to | Reason |
| --- | --- | --- |
| Home | The Show, The World, Business, Materials, Contact | Primary funnel branches. |
| The Show | The World, Casting CTA | Brand depth + talent funnel. |
| The World | The Show, Advisors | Brand context + credibility. |
| Business | Materials, Contact | Investor / broadcaster / sponsor depth. |
| Advisors | The World, Contact | Credibility + outreach. |
| Materials | Contact | Form completion. |
| Contact | (form variants) | Audience-specific routing. |

### Anchors and In-Page Sections

Each page brief lists its in-page sections. Major sections get URL anchors so investors and broadcasters can link to specific arguments (e.g. `/business#franchise-flywheel`).

### Localisation

Pre-launch site is English-only. Future territory adaptations get sub-paths:

```
/de/                         Germany
/es-mx/                      Mexico
/pt-br/                      Brazil
```

### Search Engine Strategy

- Public site is SEO-discoverable but does not target generic "music" or "reality TV" queries.
- Targets brand queries (MixHouse) and selected long-tail (casting, advisors, format).
- Gated materials are noindexed.

### Performance Targets

- LCP < 2.5s, CLS < 0.1, INP < 200ms on every primary page.
- See `09_design_system/media_behavior.md` for media optimisation rules.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Core Web Vitals thresholds | Google web.dev | 2026-05-20 | A |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Seven pages is too few." | Depth lives inside the pages, not as nav width. Narrow nav is a confidence signal. |
| "Investors need their own hub." | They have one: `/materials`. The gate filters; the page brief delivers. |

## Website Implications

- Every page in `08_website_strategy/page_briefs/` aligns with a slug above.
- Routing rules and CMS structure derive from this sitemap.

## Open Questions

- Final URL pattern for season / episode hubs.
- Whether `/live` is a top-level page or a sub-section of season hub.
- Domain strategy and country-code preferences.

## Change Log

- 2026-05-20, Initial sitemap drafted.
