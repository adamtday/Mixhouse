---
doc_type: system_rules
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [phase_plan, sequencing, agent_assignment, master_thesis]
related:
  - 00_system/kb_rules.md
  - 00_system/agent_workflow.md
  - 00_system/research_prompt_template.md
  - 01_master_context/mixhouse_master_thesis.md
  - 01_master_context/one_sentence_positioning.md
  - 01_master_context/audience_matrix.md
  - 01_master_context/objection_matrix.md
  - 02_show_bible/show_premise.md
  - 02_show_bible/format_engine.md
  - 02_show_bible/episode_anatomy.md
  - 04_competitive_landscape/mixhouse_white_space.md
  - 05_business_model/franchise_flywheel.md
  - 07_brand_world/cultural_authenticity.md
---

# Phase 01: Canonical Content Population Plan

## Purpose

Define the first content-population sprint: which 10 files must be raised from scaffold to canonical, in what order, by which agents, and with what acceptance criteria, so that all subsequent research, website-strategy, design-prompt, and investor-storytelling work can derive from validated upstream truth instead of placeholder content.

## Key Takeaways

- Ten files form the **load-bearing spine** of the KB. They are upstream of every other analytical file, every page brief, every output artifact.
- Phase 1 deliberately ignores external-validation gaps (named advisors, label partners, legal templates). Those are Phase 3+, they do not block internal reasoning.
- The plan partitions the 10 files into three execution waves: one strictly sequential, two highly parallel.
- Phase 1 is complete when all 10 files are `status: validated`, cross-links verified, and an owner Change Log sign-off is in place.

## Core Content

### Phase 1 Objective

Generate the **argument architecture for the MixHouse pitch site and franchise**. The KB exists to sell the show, attract funding, attract advisors, attract partners, and preempt objections. Phase 1 closes the gap between "we have a scaffold" and "we can argue the case to a specific audience and answer the questions they will ask."

Once the spine is canonical, every downstream effort (market research, page briefs, investor case, design prompts) has a stable, citable substrate to derive from.

We are explicitly *not* trying to fill external-validation gaps in Phase 1 (named advisors, label partners, legal templates). We are filling the gaps that block the KB from generating accurate, audience-aware, objection-handling outputs.

### Sequencing Logic

Four principles drive the ordering:

1. **Upstream first.** A file ranks higher if it is referenced by more downstream files via `related:` frontmatter or section citation. Master thesis sits at the top because every analytical file ultimately reduces to claims it makes.
2. **Audience and objection logic is upstream, not derivative.** The site exists to communicate the idea to specific audiences and to preempt their objections. Audience and objection architecture belongs in the spine, not in late-phase polish.
3. **Concept-defining before concept-applying.** Files that introduce mechanisms (`format_engine`, `franchise_flywheel`) come before files that apply them.
4. **Parallelism unlocks pace.** Where two files have no mutual dependency, they're assigned to independent agents and worked simultaneously.

External-validation gaps (advisors, judges, label partners, legal templates) are deliberately excluded; they are downstream commitments, not inputs to internal consistency.

### The Next 10 Canonical Files (Ranked, Revised)

| Rank | File | Why it matters | What it unlocks |
| --- | --- | --- | --- |
| 1 | `01_master_context/mixhouse_master_thesis.md` | Every analytical file reduces to a claim in this document. Currently `assumption: true`. | Unlocks #2 through #10 directly; indirectly every page brief and every output. |
| 2 | `01_master_context/one_sentence_positioning.md` | The canonical fan / investor / talent / broadcaster lines. Locks the words every external asset will quote. | Unlocks all copy work, especially `08_website_strategy/page_briefs/home.md` and all `11_outputs/website_copy/`. |
| 3 | `01_master_context/audience_matrix.md` | The site's purpose is to communicate the idea to specific audiences. Without a validated audience matrix, the pitch site cannot route content correctly. | Unlocks every page brief (which audience does each page serve and at what depth?), sponsorship targeting, and progressive disclosure design. |
| 4 | `01_master_context/objection_matrix.md` | The site must preempt the strongest pushbacks from investor, broadcaster, talent, sponsor, advisor, fan. Without validated objections, no page brief can be honest. | Unlocks home / business / advisors / press copy; unlocks FAQ surfaces; unlocks the deck's objection sections. |
| 5 | `02_show_bible/show_premise.md` | The format's source-of-truth statement. The file every external collaborator reads first about the show. | Unlocks #6, #7, #9; unlocks `08_website_strategy/page_briefs/the_show.md`. |
| 6 | `02_show_bible/format_engine.md` | Defines `Drop Night`, the weekly loop, the `Audience Index` composite. Most-referenced concept file in the show bible. | Unlocks `episode_anatomy`, `season_arc`, `elimination_logic`, `fan_participation`, and the show-page interactive components. |
| 7 | `02_show_bible/episode_anatomy.md` | Defines the visible structure of a single hour: how the show pays off on screen. Without it, the pitch describes a format but not an episode. | Unlocks broadcaster-pitch language ("here's what an hour looks like"), the show-page interactive ("how an episode works"), and the cinematic capture brief. |
| 8 | `05_business_model/franchise_flywheel.md` | The central commercial mechanism: seven compounding assets that turn one-off production into a franchise. | Unlocks `investor_case`, `revenue_model` detail, and the centrepiece component on `business_model.md` page brief. |
| 9 | `04_competitive_landscape/mixhouse_white_space.md` | The defensible "why us, why now, why no one else" statement. | Unlocks investor / broadcaster / press positioning copy on every public surface. |
| 10 | `07_brand_world/cultural_authenticity.md` | The hard-constraint set that governs casting, judging, music rights, design, copy, and anti-patterns. Necessary for any talent or scene outreach. | Unlocks `anti_patterns`, `music_scene_language`, all visual / motion / copy decisions. |

### Why These Ten (and What Moved)

The revised list prioritises **argument architecture** (audience + objections) and **on-screen substance** (episode anatomy) over **vocabulary discipline** (glossary) and **copy gate** (tone of voice). The site is not failing because of vocabulary. It is failing because it does not yet argue the case to specific audiences and preempt their objections.

Phase 1.5 / early Phase 2 picks up:

- **`01_master_context/glossary.md`**: useful when multiple agents are writing in parallel, but the spine works at Phase 1 without it. Defer.
- **`07_brand_world/tone_of_voice.md`**: the copy gate. It governs `11_outputs/website_copy/`, which is downstream of the argument architecture. Defer.
- **`05_business_model/revenue_model.md`**: important, but the flywheel (#8) carries the commercial story for the spine.
- **`02_show_bible/season_arc.md`**: derives from `format_engine` and `episode_anatomy`. Early Phase 2.

Out of Phase 1 entirely (Phase 2+):

- **`anti_patterns.md`**: derives from `cultural_authenticity` + `tone_of_voice`. Populating #10 cascades the right constraints.
- **`music_rights_strategy.md`** / **`casting_pipeline.md`**: high impact, blocked by external decisions (label partners, legal templates) explicitly excluded from Phase 1.
- **`contestant_archetypes.md`** / **`judging_framework.md`**: depend on `format_engine` being canonical.
- **`investor_case.md`**: derives from #8 plus a financial model.
- **All `03_market_research/*`**: blocked on #1 (which claims need backing) and #6 (which audience signals matter).
- **All `08_website_strategy/page_briefs/*`**: every page brief depends on multiple files in this top-ten list.

### Parallelization Map

Three waves. Within a wave, work proceeds in parallel; between waves, sequential.

```
Wave 1, Foundational Spine (sequential / owner-led)
  1. master_thesis
  2. one_sentence_positioning  (must follow 1)

Wave 2, Argument Architecture (parallel across three agents)
  Audience agent
    3. audience_matrix          (after 1)
    4. objection_matrix         (after 1, 3)
  Editorial agent
    5. show_premise             (after 1)
    6. format_engine            (after 5)
    7. episode_anatomy          (after 6)
    9. mixhouse_white_space     (after 1, 5)
  Commercial / brand agent
    8. franchise_flywheel       (after 1)
    10. cultural_authenticity   (after 1)

Wave 3, Cross-Validation (single reviewer)
  - Verify cross-links resolve.
  - Confirm Evidence tables for #1, #8, #9 cite A/B sources or remain explicitly flagged.
  - Audit audience_matrix against objection_matrix for consistency.
  - Owner Change Log sign-off across all 10.
```

#### Inter-Wave Dependencies

| File | Hard prerequisites |
| --- | --- |
| 2. one_sentence_positioning | 1. master_thesis |
| 3. audience_matrix | 1. master_thesis |
| 4. objection_matrix | 1. master_thesis, 3. audience_matrix |
| 5. show_premise | 1. master_thesis |
| 6. format_engine | 5. show_premise |
| 7. episode_anatomy | 6. format_engine |
| 8. franchise_flywheel | 1. master_thesis |
| 9. mixhouse_white_space | 1. master_thesis, 5. show_premise |
| 10. cultural_authenticity | 1. master_thesis |

### Agent Assignment Recommendations

| Role | Files | Notes |
| --- | --- | --- |
| **Founder / owner** | 1, 2 | Canonical thesis and positioning require human sign-off; not delegable. |
| **Audience agent** | 3, 4 | Builds the audience and objection matrices. Needs comfort with multi-audience messaging; will pressure-test against `04_competitive_landscape/` and `01_master_context/objection_matrix.md` (existing scaffold). |
| **Editorial research agent** | 5, 6, 7, 9 | Claude or equivalent, briefed via `00_system/research_prompt_template.md`. Editorial voice, scene literacy, cite-or-flag discipline. |
| **Commercial / brand agent** | 8, 10 | Two related but separable files: the commercial mechanism and the cultural-authenticity constraint set. Both gate downstream design and brand decisions. |
| **Cross-validator** | All 10 (Wave 3) | One reviewer (human or agent) walks every cross-link, verifies Evidence tier discipline, audits audience-objection consistency, and signs off in Change Log. |

Each delegated agent should receive:
- The destination file path.
- The Boot Sequence files from `00_system/agent_workflow.md`.
- The acceptance criteria for that specific file (below).
- A reminder to keep `status: validated` only if cite-or-flag is honest.

### Acceptance Criteria (Per File)

For every file to be considered Phase 1 complete:

| # | File | Acceptance criteria |
| - | --- | --- |
| 1 | `mixhouse_master_thesis.md` | Founder sign-off on thesis claims. Each Key Takeaway explicitly classified as established fact, strategic hypothesis, or proposed mechanic. Numeric thresholds moved to owner files. `assumption: true` flag removed only when no remaining claim depends on unsourced assertions. `status: validated`. |
| 2 | `one_sentence_positioning.md` | Canonical line frozen (or explicitly retained as draft with documented rework path). All audience variants present and approved. Banned-phrase audit complete. `status: validated` only when the founder signs off on the words themselves. |
| 3 | `audience_matrix.md` | All primary audiences enumerated with: profile, must-believe claim, must-do action, key proof points. Owner-file pointers in place. Sponsorship and progressive-disclosure consumers verify the matrix is usable. `status: validated`. |
| 4 | `objection_matrix.md` | The strongest objection from each audience captured with a canonical response and a linked proof file. Valid concessions listed honestly. Cross-checked against `audience_matrix.md`. `status: validated`. |
| 5 | `show_premise.md` | Logline locked (or explicitly held as the working draft). Pitch paragraph approved. World, stakes, characters, conflict, payoff sections each free of placeholder language and labelled by claim type where relevant. `status: validated`. |
| 6 | `format_engine.md` | Weekly loop table locked. `Audience Index` weighting recorded as a working proposal with explicit pilot-calibration flag. Compounding releases mechanic stated. `status: validated`. |
| 7 | `episode_anatomy.md` | Act structure locked at proposal level. Scene types, contestant surface-area table, cinematic signature requirements all populated. Runtimes labelled as targets, not commitments. `status: validated`. |
| 8 | `franchise_flywheel.md` | Seven compounding assets named, defined, tied to operational files. Mechanism stated as a literal feedback loop. Steady-state assumptions clearly labelled as illustrative. `status: validated`. |
| 9 | `mixhouse_white_space.md` | Three-category intersection locked. White-space statement frozen as the canonical parent of all positioning copy. Adjacent-category failure reasons documented. `status: validated`. |
| 10 | `cultural_authenticity.md` | Hard constraints reviewed and confirmed. Governance mechanisms enumerated. Cross-territory considerations stated. `status: validated`. |

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

Not applicable. This is a planning file. Its authority derives from the existing dependency graph documented across the KB.

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
- Should we require A-tier sources for the Master Thesis Evidence rows, or accept B-tier with notes? Recommended: B-tier minimum, A-tier where reachable, explicit `assumption` flag otherwise.
- Should Phase 1 also lock the `00_system/document_template.md` schema as immutable for the rest of the project? Recommended: yes, with a Change Log entry once the ten files are validated against it.
- Phase 1.5 sequencing: in which order do `glossary.md`, `tone_of_voice.md`, and `revenue_model.md` get picked up? Recommended: tone_of_voice first (it gates copy work), then revenue_model (it gates investor case detail), then glossary (it gates multi-agent vocabulary).

## Change Log

- 2026-05-20, Initial Phase 1 population plan drafted. Ranked the ten canonical files, partitioned into three waves, assigned agents, and defined acceptance and completion criteria.
- 2026-05-20, Revised Phase 1 top-10 per owner review: added `audience_matrix.md` and `objection_matrix.md` as load-bearing argument-architecture files; added `episode_anatomy.md` as the on-screen substance file; demoted `glossary.md`, `tone_of_voice.md`, and `revenue_model.md` to Phase 1.5 / early Phase 2. Reframed Phase 1 objective from "internal-reasoning system stability" to "argument architecture for the pitch site and franchise."
