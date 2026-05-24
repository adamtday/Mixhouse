---
doc_type: page_brief
status: draft
confidentiality: public
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [page_brief, advisors, credibility, story]
related:
  - 08_website_strategy/site_objectives.md
  - 07_brand_world/cultural_authenticity.md
  - 06_production_strategy/production_model.md
---

# Advisors Page Brief

## Purpose

Define the page that lists MixHouse's named advisors, judges, and mentors, the page that earns trust from talent, scene press, broadcasters, and investors at a glance.

## Key Takeaways

- L2 (Story).
- Names matter more than copy here. One sentence per advisor + scene affiliation + photo.
- Pre-pilot: the page exists with placeholder treatment until first names are confirmed.
- The page is also the inbound surface for new advisor inquiries.

## Core Content

### Disclosure Layer

L2 (Story).

### Page Outline

1. **Hero, Why advisors.**
   - One-paragraph editorial: scene-credible governance is built in. Source: `07_brand_world/cultural_authenticity.md`.
2. **The advisor board.**
   - AdvisorTile grid: portrait + name + scene affiliation + one-sentence role.
3. **Resident judges.**
   - Separate strip; same treatment. Source: `02_show_bible/judging_framework.md`.
4. **Mentor drops (season-mode).**
   - Per-season list of confirmed mentors. Pre-pilot: hidden.
5. **What advisors do.**
   - Defined scopes: judging, talent intros, A&R consult, public credit. Source: `06_production_strategy/production_model.md`.
6. **Become an advisor.**
   - Soft CTA, contact form. Source: `08_website_strategy/page_briefs/contact.md`.

### Audience Priority

| Order | Audience | What they get |
| --- | --- | --- |
| 1 | Talent / scene | Credibility signal that decides whether to apply. |
| 2 | Broadcaster / investor | Visible governance proof. |
| 3 | Press | Quotable names. |

### Tone

- Editorial. Names lead; copy follows.
- No effusive endorsements; let the names speak.

### Components Used

- CinematicHero (small)
- EditorialSpread (intro paragraph)
- AdvisorTile (grid)
- ContactForm (advisor inquiry routing)

### Copy Sources

| Section | Source |
| --- | --- |
| Hero | `07_brand_world/cultural_authenticity.md` |
| Advisor list | This file's data block (TBD) |
| Judge list | `02_show_bible/judging_framework.md` |
| Mentor list | Per-season config |
| What advisors do | `06_production_strategy/production_model.md` |
| Inquiry CTA | `08_website_strategy/page_briefs/contact.md` |

### Pre-Pilot State

Before advisors are publicly confirmed, the page:
- Shows the editorial framing (Hero + What advisors do).
- Shows placeholder language: "Names will appear here as advisors confirm publicly."
- Includes a contact CTA for inquiries.

Avoid "coming soon" or "stay tuned", write the placeholder as confidently as the final state.

### Data Structure

Each advisor record:

```yaml
- name: "Advisor Name"
  scene_affiliation: "Resident at X | Founder of Y | Producer"
  role: "Judging, house and tech house"
  bio_short: "One sentence."
  portrait: "/media/advisors/advisor-slug.jpg"
  links:
    - { label: "Resident Advisor profile", url: "..." }
```

### Performance and Media Targets

- Portraits served as AVIF / WebP, 800x800 minimum.
- LCP < 2.5s.
- Grid lazy-loads beyond 12 tiles.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Cultural authenticity framework | `07_brand_world/cultural_authenticity.md` | 2026-05-20 | B |

## Objections Answered

| Objection | Response |
| --- | --- |
| "What if no advisors are confirmed yet?" | Then the page is empty of names but full of intent. The framing alone is differentiating. |
| "Why not include all judges and mentors here?" | Separation keeps the cognitive load down; judges and mentors get their own strip with different scope. |

## Website Implications

- High-priority page from the moment the first advisor signs.
- Updates per advisor confirmation; ensure CRM tagging on inquiries.

## Open Questions

- First confirmed advisors, owner: founder.
- Whether to show advisor scope (judging vs talent intros vs A&R) on the public page.

## Change Log

- 2026-05-20, Initial Advisors page brief drafted.
