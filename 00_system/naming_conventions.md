---
doc_type: system_rules
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [naming, conventions, file_paths, slug]
related:
  - 00_system/kb_rules.md
---

# Naming Conventions

## Purpose

Eliminate ambiguity in file, folder, and asset naming so that retrieval, cross-linking, and downstream tooling behave deterministically.

## Key Takeaways

- All file and folder names are `lower_snake_case`. No spaces, no camelCase, no kebab-case.
- Numeric prefixes on top-level folders define retrieval priority and reading order.
- One concept per filename. Filenames must be self-describing without the parent folder.
- No `v2`, `final`, `new`, `old`, `copy_of_*`. Use the change log instead.
- Asset filenames include a date prefix `YYYYMMDD_` for temporal sortability.

## Core Content

### Folders

Top-level folders use a `NN_name/` pattern, where `NN` indicates retrieval priority (lower = read earlier by agents).

```
00_system/                 # rules and templates (read first)
01_master_context/         # who/what/why
02_show_bible/             # the format itself
03_market_research/        # external evidence
04_competitive_landscape/  # comp set and white space
05_business_model/         # commercials
06_production_strategy/    # how it gets made
07_brand_world/            # voice, look, feel
08_website_strategy/       # web product brief
09_design_system/          # design primitives
10_source_material/        # raw inputs
11_outputs/                # generated artifacts
99_archive/                # superseded files
```

Subfolders use `lower_snake_case` with no numeric prefix unless ordering matters within that subfolder.

### Files

- `lower_snake_case.md`
- Self-describing: `revenue_model.md`, not `model.md`.
- Avoid adjectives in names ("strong", "final", "v2"). The status comes from the frontmatter.
- Match the concept's canonical name from `01_master_context/glossary.md`.

### Templates and System Files

Prefixed with their function: `document_template.md`, `research_prompt_template.md`, `kb_rules.md`.

### Source Material

Files in `10_source_material/` follow:

```
YYYYMMDD_short_topic.md
YYYYMMDD_speaker_or_source_topic.md
```

Examples:
- `20260418_market_size_notes.md`
- `20260512_broadcaster_call_amazon_mgm.md`
- `20260403_pitch_deck_v1_export.pdf` (binary in `pitch_decks/`)

### Outputs

Files in `11_outputs/` follow:

```
{audience}_{artifact}_{YYYYMMDD}.md
```

Examples:
- `investor_one_pager_20260520.md`
- `broadcaster_deck_outline_20260520.md`
- `home_page_copy_20260520.md`

### Images and Binaries

Stored in `10_source_material/screenshots/` or `10_source_material/references/`:

```
YYYYMMDD_subject_descriptor.{ext}
```

Examples:
- `20260512_cercle_drone_shot_pyramids.jpg`
- `20260514_drive_to_survive_thumbnail_grid.png`

### Branches and Pull Requests

- Branches: `claude/{slug}` for agent work, `feature/{slug}` for human work, `fix/{slug}` for corrections.
- Slugs are `lower-kebab-case` for git branch names only (git convention), they are the one exception to the snake_case rule.

### IDs and Slugs

When a document needs a stable identifier for cross-system reference (e.g. CMS), use the file path relative to repo root without `.md`. Example: `02_show_bible/episode_anatomy`.

## Evidence / Sources

Not applicable. Internal convention.

## Objections Answered

| Objection | Response |
| --- | --- |
| "Why snake_case instead of kebab-case?" | Snake_case is friendlier to Python tooling, agent prompts, and JSON keys. Kebab-case is reserved for URL slugs and git branches. |
| "Numbered folders look bureaucratic." | They double as a retrieval order signal for agents. The cost (visual) is dwarfed by the benefit (determinism). |

## Website Implications

- Page slugs on the live site mirror the page brief filenames in `08_website_strategy/page_briefs/` but converted to kebab-case (e.g. `the_show.md` → `/the-show`).

## Open Questions

- Do we need a separate naming convention for multilingual assets once we expand internationally?

## Change Log

- 2026-05-20, Initial conventions written at repo creation.
