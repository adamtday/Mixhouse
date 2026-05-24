# AGENTS.md

Quick-card for coding and research agents (Claude Code, Cursor, GitHub agents, subagents). Read this first.

## What this repository is

The MixHouse knowledge base and memory harness. A retrieval-optimised markdown KB that holds the franchise's thesis, format, business model, brand world, website strategy, and design system. It is engineered for AI retrieval. Everything in it is meant to be queryable, citable, and composable into downstream artifacts.

## Read these before writing anything

1. `README.md`
2. `00_system/kb_rules.md`
3. `00_system/naming_conventions.md`
4. `00_system/source_reliability_rules.md`
5. `00_system/retrieval_tags.md`
6. `00_system/agent_workflow.md`
7. `01_master_context/mixhouse_master_thesis.md`
8. `01_master_context/one_sentence_positioning.md`
9. `01_master_context/glossary.md`

Then read the folder most relevant to the task.

## Binding rules (short version)

1. **Source vs output discipline.** Analytical content lives in `01_–09_*`. Raw inputs live in `10_source_material/`. Generated artifacts live in `11_outputs/`. Never edit a derivative when the source is wrong; fix the source.
2. **Frontmatter is mandatory** on every analytical file. Schema in `00_system/kb_rules.md`. Folder index READMEs and `.gitkeep` files follow a lighter convention.
3. **Cite or flag.** Every quantitative or factual claim cites a source at A or B tier, or is marked `assumption` with the gap noted in Open Questions.
4. **Classify claims.** Distinguish established fact, strategic hypothesis, and proposed mechanic. Do not let a hypothesis or a proposal pass as fact.
5. **No invented facts.** Do not fabricate ratings, deal sizes, partner names, or quotes. Route unknowns to Open Questions.
6. **No em dashes (`—`).** Anywhere. Use periods, commas, colons, or parentheses. Enforced at review.
7. **Anti-generic writing.** Avoid the banned-phrase list in `00_system/research_prompt_template.md`.
8. **No duplicate docs.** If a concept already has a home, extend that file. Filenames are explicit and self-describing.
9. **Update the Change Log** on every file you edit, with date and a short note.
10. **Cross-link.** Use relative paths whenever you reference a concept that already has a file.

## Commit and PR discipline

- Branches: `claude/{slug}`, `feature/{slug}`, `fix/{slug}`. Never push directly to `main`.
- Commit messages: `<area>: <imperative-verb> <object>`. One logical change per commit.
- Never skip hooks or bypass review.

## When in doubt

Ask the user. Don't silently invent. Don't expand scope.

## Repository map

```
00_system/                 Rules, templates, retrieval, agent workflow
01_master_context/         Thesis, positioning, audience, glossary
02_show_bible/             Format, episode anatomy, season arc, characters
03_market_research/        Why now, market data, audience behaviour
04_competitive_landscape/  Comp set, white space
05_business_model/         Revenue, franchise flywheel, investor case
06_production_strategy/    Pilot scope, location, casting, music pipeline
07_brand_world/            Visual identity, voice, cultural authenticity
08_website_strategy/       Site objectives, sitemap, page briefs
09_design_system/          Tokens, typography, motion, components
10_source_material/        Raw inputs: notes, transcripts, decks, refs
11_outputs/                Generated artifacts: copy, specs, prompts, tasks
99_archive/                Superseded files, kept for audit
```

## Change Log

- 2026-05-20, Initial AGENTS.md quick-card created.
