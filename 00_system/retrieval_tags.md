---
doc_type: system_rules
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [retrieval, tags, taxonomy, agent_index]
related:
  - 00_system/kb_rules.md
  - 00_system/agent_workflow.md
---

# Retrieval Tags

## Purpose

Define the controlled vocabulary of `retrieval_tags:` used in every file's frontmatter so that semantic search, manual lookup, and agent retrieval converge on the same surface area.

## Tag Count Guidance

- Analytical files (folders `01_` through `09_`): 3–8 tags. Add more only when each adds retrieval value.
- System / template / index files (folder `00_`, folder READMEs, archive): 1–5 tags.
- Source files (`10_source_material/`): 2–5 tags.
- Output files (`11_outputs/`): inherit source file tags plus an `output` marker.

Force-padding a file to 4+ tags when fewer suffice is anti-pattern; it dilutes retrieval signal.

## Key Takeaways

- Tags are `lower_snake_case`. Count varies by file type per the Tag Count Guidance above (typically 3–8 for analytical files, 1–5 for system / index files).
- Use tags from the canonical list below. Adding a new tag requires editing this file.
- Tags describe the *content's role*, not the topic alone (e.g. `objection_handling`, not just `objections`).
- When in doubt, prefer fewer, more specific tags.

## Core Content

### Canonical Tag List

#### Identity & Positioning
- `positioning`: one-line summaries, master thesis-level claims
- `audience`: viewer / fan / talent personas
- `glossary`: definitional content
- `objection_handling`: counter-arguments to known pushbacks
- `franchise`: anything multi-season, multi-region, multi-format

#### Format & Show
- `show_premise`: logline, hook, format-defining content
- `format_engine`: how an episode self-perpetuates
- `episode_anatomy`: per-episode structural breakdown
- `season_arc`: multi-episode narrative
- `contestants`: characters, archetypes, casting
- `judges`: judging philosophy and panel design
- `elimination_logic`: competition mechanics
- `fan_participation`: audience interaction loops

#### Market & Competition
- `market_size`: TAM/SAM/SOM data
- `why_now`: timing rationale
- `audience_behaviour`: viewing, listening, discovery data
- `creator_economy`: DJ/producer/independent artist data
- `competitive`: direct comparison material
- `white_space`: where MixHouse uniquely sits

#### Commercial
- `revenue_model`: monetisation breakdown
- `sponsorship`: brand integration inventory
- `music_rights`: publishing, master, sync strategy
- `live_events`: touring, festivals, residencies
- `investor`: material aimed at investors
- `unit_economics`: per-episode, per-season financial model

#### Production
- `production_model`: studio, format owner, financing structure
- `pilot`: pilot-specific planning
- `location`: geography of the shoot
- `casting`: talent pipeline
- `music_pipeline`: release process for in-show music
- `risk`: production and commercial risks
- `use_of_funds`: capital allocation

#### Brand & Design
- `brand_voice`: tone and writing
- `visual_identity`: look and feel
- `cultural_authenticity`: respect for the electronic music scene
- `moodboard`: visual references
- `anti_patterns`: what we will not do
- `design_tokens`: colour, type, spacing, motion primitives
- `motion`: animation and interaction
- `accessibility`: a11y standards
- `media_behaviour`: how video, audio, image components behave

#### Website
- `site_objectives`: KPI / goal of the site
- `sitemap`: IA
- `progressive_disclosure`: staged revelation pattern
- `component_requirements`: UI building blocks
- `page_brief`: single-page brief

#### System & Workflow
- `kb_rules`: governance
- `template`: reusable scaffolding
- `schema`: frontmatter or data shape
- `agent_workflow`: how agents act on the repo
- `retrieval`: index and lookup mechanics
- `naming`: naming conventions
- `conventions`: formatting and process rules
- `reliability`: source-tier rules

#### Source Material
- `transcript`: raw conversation
- `raw_notes`: informal notes
- `reference`: external inspiration material
- `screenshot`: captured visual

### Adding a New Tag

1. Justify the addition in this file's Change Log.
2. Add it to the canonical list above under the right category.
3. If creating a new category, place it where it best fits the existing taxonomy.
4. Backfill any older files that should now carry the tag.

### Tag-to-Folder Heuristic

| Folder | Most common tags |
| --- | --- |
| `00_system/` | `kb_rules`, `template`, `schema`, `agent_workflow`, `naming`, `retrieval`, `reliability` |
| `01_master_context/` | `positioning`, `audience`, `glossary`, `objection_handling` |
| `02_show_bible/` | `show_premise`, `format_engine`, `episode_anatomy`, `season_arc`, `contestants`, `judges`, `elimination_logic`, `fan_participation` |
| `03_market_research/` | `market_size`, `why_now`, `audience_behaviour`, `creator_economy` |
| `04_competitive_landscape/` | `competitive`, `white_space` |
| `05_business_model/` | `revenue_model`, `sponsorship`, `music_rights`, `live_events`, `investor`, `unit_economics`, `franchise` |
| `06_production_strategy/` | `production_model`, `pilot`, `location`, `casting`, `music_pipeline`, `risk`, `use_of_funds` |
| `07_brand_world/` | `brand_voice`, `visual_identity`, `cultural_authenticity`, `moodboard`, `anti_patterns` |
| `08_website_strategy/` | `site_objectives`, `sitemap`, `progressive_disclosure`, `component_requirements`, `page_brief` |
| `09_design_system/` | `design_tokens`, `motion`, `accessibility`, `media_behaviour`, `visual_identity` |
| `10_source_material/` | `transcript`, `raw_notes`, `reference`, `screenshot` |
| `11_outputs/` | tag with the source folder's tags plus `output` |

## Evidence / Sources

Not applicable. Internal taxonomy.

## Objections Answered

| Objection | Response |
| --- | --- |
| "Why not free-form tags?" | Free-form tags fragment instantly. A controlled vocabulary keeps retrieval deterministic. |
| "This list will get stale." | Editing this file forces a deliberate review, which is the feature, not the bug. |

## Website Implications

The website's content surface (especially `08_website_strategy/page_briefs/`) is assembled by querying retrieval tags. Stale tags = stale generated pages.

## Open Questions

- Do we need synonyms / aliases (e.g. `audience` ↔ `viewers`)?
- Should retrieval tags propagate into the design system file format (e.g. Figma tokens)?

## Change Log

- 2026-05-20, Initial canonical tag list.
