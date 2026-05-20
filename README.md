---
doc_type: repository_readme
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [readme, repo_overview, agent_onboarding, workflow]
---

# MixHouse Knowledge Base & Memory Harness

This repository is the **single source of truth** for the MixHouse franchise: a cinematic electronic-music reality format, its accompanying business model, and the public-facing materials (website, pitch decks, investor docs) that sell it.

It is engineered as a **retrieval-optimized markdown knowledge base** that humans, Claude agents, Cursor, and GitHub coding agents can all read, extend, and build from. The repository is not a wiki; it is a long-term memory harness.

## 1. Purpose

The repository must, at all times, be able to:

1. Brief a new collaborator (human, agent, or LLM) quickly and consistently via `01_master_context/`.
2. Answer the question "what is MixHouse?" with consistent positioning across investors, broadcasters, advisors, talent, and audience.
3. Generate downstream artifacts deterministically: website copy, pitch decks, design prompts, dev tasks, sponsor decks, casting briefs.
4. Survive personnel changes. Every claim, number, and design decision must be traceable to a source or labeled as an assumption.
5. Compound. Each new piece of research, transcript, or screenshot should make the next output cheaper and better.

## 2. Workflow Rules

- **Develop on branches.** Never push speculative content directly to `main`. Use `claude/*` or `feature/*` branches.
- **One concept per file.** If a file's purpose can't be stated in one sentence, split it.
- **Frontmatter is mandatory.** Every markdown file uses the YAML schema in `00_system/document_template.md`.
- **Cite or label.** Any quantitative or market claim must include a source in the `Evidence / Sources` section, or be flagged `assumption: true` in frontmatter.
- **Cross-link.** When you reference a concept defined elsewhere, link to that file using a relative path.
- **No lorem ipsum.** Empty scaffolding files must still contain a real `Purpose` and `Open Questions` block so future agents know what is missing.
- **Update the change log.** When you change a file, add a dated entry at the bottom.
- **Promote, don't pile.** When raw research in `10_source_material/` is digested into `03_market_research/`, summarise and link, do not duplicate.

## 3. Retrieval Priorities

When a Claude or Cursor agent loads context to answer a question or generate an artifact, it should pull files in this priority order (highest first):

1. `00_system/kb_rules.md`: formatting and behaviour rules
2. `01_master_context/*`: positioning, audience, glossary
3. The folder most topical to the task (e.g. `02_show_bible/` for format questions, `08_website_strategy/` for web copy)
4. `04_competitive_landscape/`: for any "why us / why now" framing
5. `00_system/retrieval_tags.md`: tag-to-file map
6. `10_source_material/`: only when traceable evidence is needed
7. `99_archive/`: only when reconstructing prior decisions

See `00_system/agent_workflow.md` for the full retrieval protocol.

## 4. Confidentiality Levels

Every file declares a `confidentiality:` field in frontmatter. Allowed values:

| Level | Meaning | Examples |
| --- | --- | --- |
| `public` | Safe for the live website, press, and social. | Logline, audience hooks, public bios. |
| `investor` | Shown under NDA to investors, broadcasters, partners. | Revenue model, use of funds, ratings benchmarks. |
| `internal` | Team-only working documents. | Production risks, casting pipeline, raw notes. |
| `restricted` | Sensitive, named individuals only. | Personal financial info, contracts, unredacted talent lists. |

Default is `internal`. Anything moving to `public` requires explicit approval in the change log.

## 5. File Status Conventions

The `status:` field in frontmatter takes one of:

- `seed`: scaffold; structure only, almost no content yet.
- `draft`: meaningful content; not yet validated against sources.
- `validated`: content reviewed against `Evidence / Sources` and cross-checked.
- `stable`: locked for use in external materials; changes require a change-log entry and review.
- `deprecated`: superseded; kept for audit trail. Should link to its replacement.

Agents should treat anything below `validated` as provisional and surface that uncertainty in generated artifacts.

## 6. Contribution Rules for AI Agents

When extending this repository as an agent (Claude, Cursor, GitHub Copilot, etc.):

1. **Read `00_system/kb_rules.md` and `00_system/agent_workflow.md` first.** They are short and binding.
2. **Use `00_system/document_template.md`** when creating new files.
3. **Never invent numbers.** If a market size, ratings figure, or revenue benchmark is unknown, add it to `Open Questions` instead of fabricating.
4. **Prefer editing over creating.** If a concept already has a home, extend that file rather than spawning a near-duplicate.
5. **Preserve modularity.** Don't merge `show_bible/` content into `business_model/`, even if related, cross-link instead.
6. **Use explicit filenames.** No `notes.md`, `misc.md`, `final_v2.md`.
7. **Anti-generic writing.** Avoid "in today's fast-paced world", "revolutionary", "game-changing". See `00_system/research_prompt_template.md` for the banned-phrase list.
8. **Leave the repo more legible than you found it.**

## 7. Top-Level Map

```
00_system/                 Rules, templates, retrieval index, agent workflow
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

## 8. Quick Start for New Agents

For coding and research agents, read `AGENTS.md` at the repository root first. Then:

1. Read `01_master_context/mixhouse_master_thesis.md`.
2. Read `01_master_context/one_sentence_positioning.md`.
3. Read `02_show_bible/show_premise.md`.
4. Read `04_competitive_landscape/mixhouse_white_space.md`.
5. Scan `00_system/retrieval_tags.md` to learn the tag vocabulary.
6. Only then start the task.

## Change Log

- 2026-05-20, Initial repository scaffold created on branch `claude/init-mixhouse-kb-cp80H`.
- 2026-05-20, Removed "under 10 minutes" operational claim (not yet load-tested). Added pointer to root `AGENTS.md` quick-card. Repo-wide em-dash sweep applied; binding rule documented in `00_system/kb_rules.md` and `07_brand_world/tone_of_voice.md`.
