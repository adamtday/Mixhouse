---
doc_type: thesis
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [glossary, definitions, taxonomy, jargon]
related:
  - 01_master_context/mixhouse_master_thesis.md
  - 00_system/retrieval_tags.md
---

# MixHouse Glossary

## Purpose

Canonical definitions for every internal-jargon term used across the KB so that contributors and agents converge on a single meaning. When a term in this list appears in any other file, link to this glossary on first use.

## Key Takeaways

- All capitalised internal terms are defined here exactly once.
- If a term has a public-facing variant, both are listed.
- Music scene language is documented separately in `07_brand_world/music_scene_language.md`.

## Core Content

### Format Terms

- **MixHouse** — the franchise. Always one word, capital M and H. The plural form ("MixHouses") is not used.
- **Residency** — the principal location where contestants live and create for the duration of the season. Borrowed from the dance-music meaning of an extended booking at a venue/city.
- **Drop Night** — the recurring episode-end event at which the week's tracks are debuted to a curated live audience. Source for audience-reaction data feeding elimination.
- **Final Set** — the season finale headline performance at a tentpole festival or branded MixHouse event.
- **Crate** — the in-show music library curated by judges, mentors, and supervising A&R for sample/reference access during episodes.
- **Mentor Drop** — a one-off appearance by a scene-credible established artist who works with contestants on a specific challenge.
- **Audience Index** — composite signal from `Drop Night` reaction, streaming performance, and short-form virality used in elimination logic. Defined in `02_show_bible/elimination_logic.md`.

### Business Terms

- **Franchise Flywheel** — the multi-format revenue compounding model. See `05_business_model/franchise_flywheel.md`.
- **Format Engine** — the structural mechanic that makes each episode produce a finished, releasable track. See `02_show_bible/format_engine.md`.
- **Release Pipeline** — the operational and legal scaffolding that ships in-show music as a real commercial release. See `06_production_strategy/music_release_pipeline.md`.
- **Pilot Block** — the first production unit; not necessarily the broadcast pilot. Includes test-of-format scenes and full episode template.
- **Format Sale** — international licensing of the MixHouse format to local broadcasters / producers, on the `Idol` / `Voice` template.

### Audience and Scene Terms

- **Scene** — used to mean the global electronic-music community of producers, DJs, fans, labels, and venues. Not a substitute for "industry".
- **Producer** (in MixHouse context) — a person who makes electronic music tracks. Distinct from a TV producer; disambiguate in any doc that uses both meanings.
- **DJ** — a performer who plays electronic music live or recorded sets. May or may not also produce.
- **Promoter** — operator of clubs / festivals / event series.
- **A&R** — Artists and Repertoire; the label function responsible for talent and creative direction.
- **Sync** — synchronisation, the licensing of music for use in screen content.

### KB and Workflow Terms

- **KB** — this knowledge base.
- **Boot Sequence** — the canonical set of files an agent must read at session start. See `00_system/agent_workflow.md`.
- **Frontmatter** — the YAML block at the top of every markdown file. Schema in `00_system/kb_rules.md`.
- **Reliability Tier** — `A`, `B`, `C`, or `assumption` rating for evidence. See `00_system/source_reliability_rules.md`.
- **Progressive Disclosure** — the website pattern that reveals depth based on user signal. See `08_website_strategy/progressive_disclosure_model.md`.
- **Page Brief** — a single-page specification in `08_website_strategy/page_briefs/`.

### Design and Brand Terms

- **Design Token** — atomic styling primitive (colour, type scale, spacing) defined in `09_design_system/tokens.md`.
- **Motion Token** — atomic motion primitive (easing, duration). See `09_design_system/motion.md`.
- **Cinematic Mode** — the high-density, motion-heavy presentation style applied to hero and editorial components. See `09_design_system/motion.md`.
- **Anti-Pattern** — a thing MixHouse must not be or do. Cultural authenticity safeguard. See `07_brand_world/anti_patterns.md`.

## Evidence / Sources

Not applicable — definitional file.

## Objections Answered

| Objection | Response |
| --- | --- |
| "Some of these aren't really jargon." | If two contributors could plausibly disagree on the meaning, it belongs here. |
| "The glossary will go stale." | Linking from first-use anchors content to this file. When a term drifts, this is the first place to update. |

## Website Implications

- Public site uses public-facing variants only (e.g. "Drop Night" rather than internal abbreviations).
- Tooltips and footer glossary on `08_website_strategy/page_briefs/the_show.md` derive from this file's "Format Terms" section.

## Open Questions

- Are there scene-specific terms (e.g. "B2B set", "back-to-back", "live set" vs "DJ set") that should be split into a separate scene language doc? Tentatively yes — owner: `07_brand_world/music_scene_language.md`.
- Do we want trademark designations on any of these terms?

## Change Log

- 2026-05-20 — Initial glossary drafted.
