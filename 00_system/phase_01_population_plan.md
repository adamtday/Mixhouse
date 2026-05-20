---
doc_type: system_rules
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [phase_plan, sequencing, agent_assignment, retrieval, master_thesis]
related:
  - 00_system/kb_rules.md
  - 00_system/agent_workflow.md
  - 00_system/research_prompt_template.md
  - 01_master_context/mixhouse_master_thesis.md
  - 01_master_context/one_sentence_positioning.md
  - 01_master_context/glossary.md
  - 02_show_bible/show_premise.md
  - 02_show_bible/format_engine.md
  - 04_competitive_landscape/mixhouse_white_space.md
  - 05_business_model/franchise_flywheel.md
  - 05_business_model/revenue_model.md
  - 07_brand_world/cultural_authenticity.md
  - 07_brand_world/tone_of_voice.md
---

# Phase 01 — Canonical Content Population Plan

## Purpose

Define the first content-population sprint: which 10 files must be raised from scaffold to canonical, in what order, by which agents, and with what acceptance criteria — so that all subsequent research, website-strategy, design-prompt, and investor-storytelling work can derive from validated upstream truth instead of placeholder content.

## Key Takeaways

- Ten files form the **load-bearing spine** of the KB. They are upstream of every other analytical file, every page brief, every output artifact.
- Phase 1 deliberately ignores external-validation gaps (named advisors, label partners, legal templates). Those are Phase 3+ — they do not block internal reasoning.
- The plan partitions the 10 files into three execution waves: one strictly sequential, two highly parallel.
- Phase 1 is complete when all 10 files are `status: validated`, cross-links verified, and an owner Change Log sign-off is in place.

## Core Content

### Phase 1 Objective

Move the **internal-reasoning system** of the KB from "scaffolded with sound assumptions" to "canonical and validated." Once the spine is canonical, every downstream effort — market research, page briefs, investor case, design prompts — has a stable, citable substrate to derive from.

We are explicitly *not* trying to fill external-validation gaps in Phase 1. We are filling the gaps that block the KB from generating accurate, consistent outputs.

### Sequencing Logic

Three principles drive the ordering:

1. **Upstream first.** A file ranks higher if it is referenced by more downstream files via `related:` frontmatter or section citation. Master thesis sits at the top because every analytical file ultimately reduces to claims it makes.
2. **Concept-defining before concept-applying.** Files that introduce vocabulary (`glossary`), formulas (`format_engine`), or mechanisms (`franchise_flywheel`) come before files that use them.
3. **Parallelism unlocks pace.** Where two files have no mutual dependency, they're assigned to independent agents and worked simultaneously.

External-validation gaps (advisors, judges, label partners, legal templates) are deliberately excluded — they are downstream commitments, not inputs to internal consistency.

### The Next 10 Canonical Files (Ranked)

| Rank | File | Why it matters | What it unlocks |
| --- | --- | --- | --- |
| 1 | `01_master_context/mixhouse_master_thesis.md` | Every analytical file reduces to a claim in this document. Currently `assumption: true` with four target Evidence rows. | Unlocks #2, #4, #6, #8 directly; indirectly every page brief and every output. |
| 2 | `01_master_context/one_sentence_positioning.md` | The canonical fan / investor / talent / broadcaster lines. Locks the words every external asset will quote. | Unlocks all copy work, especially `08_website_strategy/page_briefs/home.md` and all `11_outputs/website_copy/`. |
| 3 | `01_master_context/glossary.md` | The vocabulary contract. Resolves "what do we call X" before contributors disagree. | Unlocks consistent language across show bible, business model, brand world, and page briefs. |
| 4 | `02_show_bible/show_premise.md` | The format's source-of-truth statement. The file every external collaborator reads first about the show. | Unlocks #5, #8; unlocks `08_website_strategy/page_briefs/the_show.md`. |
| 5 | `02_show_bible/format_engine.md` | Defines `Drop Night`, the weekly loop, the `Audience Index` composite. Most-referenced concept file in the show bible. | Unlocks `episode_anatomy`, `season_arc`, `elimination_logic`, `fan_participation`, and the show-page interactive components. |
| 6 | `05_business_model/franchise_flywheel.md` | The central commercial mechanism: seven compounding assets that turn one-off production into a franchise. | Unlocks `investor_case`, `revenue_model` detail, and the centrepiece component on `business_model.md` page brief. |
| 7 | `05_business_model/revenue_model.md` | Five-line revenue stack. The skeleton all commercial conversations attach to. | Unlocks `sponsorship_inventory`, `live_event_extensions`, `platform_extensions`, `investor_case`, `use_of_funds`. |
| 8 | `04_competitive_landscape/mixhouse_white_space.md` | The defensible "why us, why now, why no one else" statement. | Unlocks investor / broadcaster / press positioning copy on every public surface. |
| 9 | `07_brand_world/cultural_authenticity.md` | The hard-constraint set that governs casting, judging, music rights, design, copy, and anti-patterns. | Unlocks `anti_patterns`, `music_scene_language`, all visual / motion / copy decisions. |
| 10 | `07_brand_world/tone_of_voice.md` | The copy gate. Every word on every surface either passes this file or doesn't ship. | Unlocks all `11_outputs/website_copy/`, all investor and broadcaster materials, all social/short-form captions. |

### Why These Ten — Not Others

Files that look like they should be on this list, and why they aren't:

- **`audience_matrix.md`** — important, but largely a routing tool. Once the master thesis and white-space are canonical, audience routing is mechanical.
- **`objection_matrix.md`** — derivative of master thesis and white-space. Phase 2.
- **`anti_patterns.md`** — derives directly from `cultural_authenticity` + `tone_of_voice`. Populating #9 and #10 cascades the right constraints.
- **`music_rights_strategy.md`** / **`casting_pipeline.md`** — high impact, but blocked by external decisions (label partners, legal templates) the user explicitly excluded.
- **`contestant_archetypes.md`** / **`judging_framework.md`** — depend on `format_engine` being canonical. Phase 2.
- **`investor_case.md`** — derives from #6 + #7 + financial model. Phase 2 once the model lands.
- **All `03_market_research/*`** — explicitly blocked on #1 (which claims need backing) and #5 (which audience signals matter). Phase 2 work.
- **All `08_website_strategy/page_briefs/*`** — every page brief depends on multiple files in this top-ten list. Phase 2.

### Parallelization Map

Three waves. Within a wave, work proceeds in parallel; between waves, sequential.

```
Wave 1 — Foundational Spine (sequential / owner-led)
  1. master_thesis             ─┐
  2. one_sentence_positioning   │  must follow (1)
  3. glossary                   │  can run alongside (2)
                              ─┘

Wave 2 — Concept Definition (parallel across three agents)
  ┌─ Editorial agent ─────────────────────────────────┐
  │   4. show_premise → 5. format_engine               │
  │   8. mixhouse_white_space (after 1, 4)             │
  └────────────────────────────────────────────────────┘
  ┌─ Commercial agent ────────────────────────────────┐
  │   6. franchise_flywheel ‖ 7. revenue_model         │
  └────────────────────────────────────────────────────┘
  ┌─ Brand agent ─────────────────────────────────────┐
  │   9. cultural_authenticity ‖ 10. tone_of_voice     │
  └────────────────────────────────────────────────────┘

Wave 3 — Cross-Validation (single reviewer)
  - Verify cross-links resolve.
  - Confirm Evidence tables for #1, #6, #7 cite A/B sources or remain explicitly flagged.
  - Owner Change Log sign-off across all 10.
```

#### Inter-Wave Dependencies

| File | Hard prerequisites |
| --- | --- |
| 2. one_sentence_positioning | 1. master_thesis |
| 4. show_premise | 1. master_thesis |
| 5. format_engine | 4. show_premise |
| 6. franchise_flywheel | 1. master_thesis |
| 7. revenue_model | 1. master_thesis |
| 8. mixhouse_white_space | 1. master_thesis, 4. show_premise |
| 9. cultural_authenticity | 1. master_thesis |
| 10. tone_of_voice | 1. master_thesis |
| 3. glossary | none (terminology can be seeded from existing scaffold) |

### Agent Assignment Recommendations

| Role | Files | Notes |
| --- | --- | --- |
| **Founder / owner** | 1, 2 | Canonical positioning requires human sign-off; this is not delegable. |
| **Editorial research agent** | 3, 4, 5, 8 | Claude or equivalent, briefed via `00_system/research_prompt_template.md`. Editorial voice, scene literacy, cite-or-flag discipline. |
| **Commercial agent** | 6, 7 | Claude or equivalent with explicit "no fabricated numbers" briefing; A/B-tier sources only. |
| **Brand agent** | 9, 10 | Claude or equivalent operating against `00_system/research_prompt_template.md` banned-phrase list. |
| **Cross-validator** | All 10 (Wave 3) | One reviewer (human or agent) walks every cross-link, verifies Evidence tier discipline, and signs off in Change Log. |

Each delegated agent should receive:
- The destination file path.
- The Boot Sequence files from `00_system/agent_workflow.md`.
- The acceptance criteria for that specific file (below).
- A reminder to keep `status: validated` only if cite-or-flag is honest.

### Acceptance Criteria (Per File)

For every file to be considered Phase 1 complete:

| # | File | Acceptance criteria |
| - | --- | --- |
| 1 | `mixhouse_master_thesis.md` | Founder sign-off on thesis claims. Four "Why Now" Evidence rows either cited at A/B tier or replaced with explicitly-scoped assumptions. `assumption: true` flag removed if all four rows are cited. `status: validated`. |
| 2 | `one_sentence_positioning.md` | Canonical line frozen. All five audience variants present and approved. Banned-phrase audit complete. `status: validated`. |
| 3 | `glossary.md` | Every internal term used anywhere in the KB is listed. Cross-link check: every analytical file links to glossary on first-use of a defined term. `status: validated`. |
| 4 | `show_premise.md` | Logline locked. Pitch paragraph approved. World, stakes, characters, conflict, payoff sections each free of placeholder language. `status: validated`. |
| 5 | `format_engine.md` | Weekly loop table locked. `Audience Index` four-input weighting recorded as a working proposal with explicit pilot-calibration flag. Compounding releases mechanic clearly stated. `status: validated`. |
| 6 | `franchise_flywheel.md` | Seven compounding assets named, defined, and tied to specific operational files. Mechanism stated as a literal feedback loop, not a metaphor. Steady-state condition specified. `status: validated`. |
| 7 | `revenue_model.md` | Five revenue lines named, defined, owner-file linked. Stack shape table reviewed. Dependencies between lines explicitly enumerated. `status: validated`. |
| 8 | `mixhouse_white_space.md` | Three-category intersection diagram (verbal or visual) locked. White-space statement frozen as the canonical parent of all positioning copy. Adjacent-category failure reasons documented. `status: validated`. |
| 9 | `cultural_authenticity.md` | Ten hard constraints reviewed and confirmed. Governance mechanisms enumerated. Cross-territory considerations stated. `status: validated`. |
| 10 | `tone_of_voice.md` | Voice attributes + anti-attributes both populated. At least three good and three bad sample passages. Banned-phrase reference confirmed. `status: validated`. |

### Phase 1 Definition of Done

Phase 1 is complete when **all of** the following are true:

1. All ten files carry `status: validated` (or `status: stable` for those receiving owner sign-off).
2. No file in the ten still carries `assumption: true` in its frontmatter unless the assumption is explicitly bounded and traceable to an Open Question.
3. Every cross-link in the ten files resolves to an existing file in the repository.
4. Every Evidence / Sources row in the ten files is either cited at A or B tier or explicitly labelled `assumption` with the missing source named in Open Questions.
5. Each of the ten files has at least one dated Change Log entry written during this phase by the owner or assigned agent.
6. A short summary commit titled `phase_01: complete canonical spine` is pushed, listing the ten files moved to validated.

When (1)–(6) hold, Phase 2 may open:
- Market research evidence sourcing (`03_market_research/*`).
- Competitive deep-dives finalised (`04_competitive_landscape/*` per-comp files).
- Page-brief refinement → `11_outputs/website_copy/` generation.
- Investor case modelling and `06_production_strategy/use_of_funds.md` numerification.

### Phase 1 Anti-Goals (Out of Scope)

To keep the sprint focused, the following are explicitly **not** Phase 1 work:

- Confirming named advisors, judges, or mentors.
- Selecting a label partner or DSP partner.
- Locking pilot location or festival anchor.
- Finalising the financial model spreadsheet.
- Producing the trademark / legal entity registration.
- Building the website.
- Generating any `11_outputs/*` artifact.

If a Phase 1 agent encounters one of these as a blocker, the answer is "log it in the relevant file's Open Questions and move on." None of the ten files require these external commitments to reach `validated`.

## Evidence / Sources

Not applicable — this is a planning file. Its authority derives from the existing dependency graph documented across the KB.

## Objections Answered

| Objection | Response |
| --- | --- |
| "Ten files is too many for one sprint." | Three of them are owner-led (1, 2) plus a low-effort vocabulary file (3). The remaining seven split cleanly across three parallel agents in Wave 2. Realistic single-sprint scope. |
| "Why is the master thesis at #1 if it's already drafted?" | Drafted is not validated. The current file is flagged `assumption: true`. Moving it to `validated` cascades trust into every downstream file. |
| "Why not start with page briefs to drive build velocity?" | Page briefs are derivative. Building a website from un-validated upstream content guarantees rework. Validate the spine; the build is then mechanical. |
| "Brand-world files feel late for a brand-led franchise." | Cultural authenticity and tone are in the same wave as commercial concept definition (Wave 2), exactly when they are needed to gate downstream outputs. |

## Website Implications

Phase 1 has no direct website surface. It is the prerequisite for Phase 2's page-brief refinement and `11_outputs/website_copy/` generation. Without validated upstream files, any copy generated now will need to be re-generated.

## Open Questions

- Should the cross-validator role (Wave 3) be a separate agent or the founder? Recommended: separate agent + founder co-sign.
- Should we require A-tier sources for the four Master Thesis Evidence rows, or accept B-tier with notes? Recommended: B-tier minimum, A-tier where reachable, explicit `assumption` flag otherwise.
- Should Phase 1 also lock the `00_system/document_template.md` schema as immutable for the rest of the project? Recommended: yes, with a Change Log entry once the ten files are validated against it.

## Change Log

- 2026-05-20 — Initial Phase 1 population plan drafted. Ranked the ten canonical files, partitioned into three waves, assigned agents, and defined acceptance and completion criteria.
