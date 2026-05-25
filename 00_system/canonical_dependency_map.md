---
doc_type: system_rules
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-24
retrieval_tags: [canonical_dependency, retrieval_hierarchy, system_rules, anti_canonisation, founder_thesis]
related:
  - 00_system/kb_rules.md
  - 00_system/agent_workflow.md
  - 00_system/retrieval_tags.md
  - 00_system/source_reliability_rules.md
  - 01_master_context/founder_thesis.md
  - 01_master_context/mixhouse_master_thesis.md
  - 01_master_context/audience_matrix.md
  - 01_master_context/objection_matrix.md
  - 01_master_context/README.md
  - 04_competitive_landscape/mixhouse_white_space.md
  - 02_show_bible/format_engine.md
---

# Canonical Dependency Map

## Purpose

Codify which documents in the KB are canonical anchors for retrieval and authorship, which are derivative, which are deferred (intentionally incomplete pending upstream input), which should never become retrieval anchors, and how reconciliation should proceed when a deferred input lands.

This file exists because the KB now has a deferred canonical input (the founder thesis, owned by Sam Salony) and downstream work continues around it. Without an explicit map, agents and human contributors risk treating derivative files as canonical, or accidentally canonising material that should remain provisional.

## Key Takeaways

- **Canonical anchors are few and high-leverage.** They are the spine the rest of the KB reduces back to. Every claim downstream should be traceable to a claim in a canonical anchor.
- **Derivative files inherit their status from their upstream.** A page brief that depends on the audience matrix cannot stabilise faster than the audience matrix does.
- **Deferred canonical inputs are explicit, not hidden.** The founder thesis is currently deferred; downstream work proceeds with a documented reconciliation strategy in place.
- **Some files should never become retrieval anchors.** Source material, raw transcripts, draft outputs, and archive content are supporting evidence, not anchors. Agents that retrieve from them as if they were anchors degrade the KB.
- **Anti-canonisation rule.** Prefer expanding existing owner files over creating new near-duplicate files. Create new files only when the concept has a distinct retrieval role.

## Core Content

### Retrieval Hierarchy

When an agent or human contributor loads context to answer a question or generate an artefact, files should be pulled in this priority order. Higher tiers carry more weight; lower tiers are supporting evidence.

| Tier | Role | Examples |
| --- | --- | --- |
| **0. System rules** | Bind authorship and retrieval behaviour. Override anything else when in conflict. | `00_system/kb_rules.md`, `00_system/source_reliability_rules.md`, `00_system/retrieval_tags.md`, `00_system/agent_workflow.md`, this file. |
| **1. Canonical anchors** | The strategic spine. Every downstream claim ladders back here. | Listed in the Canonical Anchors table below. |
| **2. Derivative spine** | Substantive documents that derive from canonical anchors and inform downstream operational and creative work. | Per-comp competitive files, business-model files, brand-world files, format-extension files. |
| **3. Operational derivatives** | Production, casting, location, rights, sponsorship, and other operational-execution files. | `06_production_strategy/*`, `05_business_model/*`, `09_design_system/*`. |
| **4. Public-facing derivatives** | Page briefs, output copy, design specs, marketing artefacts. Should never contradict canonical anchors. | `08_website_strategy/page_briefs/*`, `11_outputs/*`. |
| **5. Supporting evidence** | Source material that underwrites canonical and derivative files. Cited from Evidence tables; not retrieved as if they were canonical. | `10_source_material/*`, `03_market_research/research_source_registry.md`. |
| **6. Archive** | Superseded content kept for audit trail. Never an anchor; not retrieved in normal context-load. | `99_archive/*`. |

### Canonical Anchors

The following files are the canonical anchors. They are the highest-priority retrieval targets and the load-bearing references for the rest of the KB.

| File | Canonical role | Current status | Deferred? |
| --- | --- | --- | --- |
| `01_master_context/founder_thesis.md` | Originating worldview, conviction, taste, cultural insight. Sam Salony's voice. | Template; `status: draft`; `assumption: true`. | **Yes**: deferred canonical input. Sam fills. |
| `01_master_context/mixhouse_master_thesis.md` | Strategic master argument: what it is, why now, why it wins, why franchise IP. | `status: draft`; `assumption: true` until Evidence rows source. | No, but reconciliation against founder thesis pending. |
| `01_master_context/audience_matrix.md` | The nine audiences, what each wants, fears, doubts, requires as proof. | `status: draft`; `assumption: true`. | No. |
| `01_master_context/objection_matrix.md` | The ten Universal Objections plus per-audience objection tables with response, proof, site routing. | `status: draft`; `assumption: true`. | No. |
| `04_competitive_landscape/mixhouse_white_space.md` | The primary investor-persuasion artefact: three adjacent categories, four-legs framing, defensibility moats. | `status: draft`; `assumption: true`. | No. |
| `02_show_bible/format_engine.md` | The recurring mechanic that makes MixHouse a format, not a show. | `status: draft`; `assumption: true`. | No. |

Six canonical anchors total. The white-space file and the format engine sit in their topical folders rather than `01_master_context/` for routing reasons; they remain canonical regardless of folder.

### Dependency Map

Per-file: what each canonical anchor depends on upstream, and what depends on it downstream. Diagram-as-table.

| Canonical anchor | Depends on upstream | Depended on downstream by |
| --- | --- | --- |
| `founder_thesis.md` | Sam's worldview, conviction, taste, lived experience. No KB upstream dependencies. | Eventually: every other canonical anchor and most derivative files, once filled. Currently: nothing, while deferred. |
| `mixhouse_master_thesis.md` | Future reconciliation against `founder_thesis.md`. Currently independent; carries the strategic argument standalone. | `audience_matrix.md`, `objection_matrix.md`, `mixhouse_white_space.md`, `format_engine.md`, all page briefs, all investor materials. |
| `audience_matrix.md` | `mixhouse_master_thesis.md`; future reconciliation against `founder_thesis.md`. | `objection_matrix.md`, every page brief, sponsorship inventory, casting outreach, press strategy. |
| `objection_matrix.md` | `mixhouse_master_thesis.md`, `audience_matrix.md`; future reconciliation against `founder_thesis.md`. | Every page brief (the website is the objection-neutralisation engine), investor decks, press kits, FAQ surfaces. |
| `mixhouse_white_space.md` | `mixhouse_master_thesis.md`, per-comp files in `04_competitive_landscape/`; future reconciliation against `founder_thesis.md`. | `business_model.md` page brief, investor decks, press kits, partner pitch documents. |
| `format_engine.md` | `mixhouse_master_thesis.md`, `02_show_bible/show_premise.md`; future reconciliation against `founder_thesis.md`. | `episode_anatomy.md`, `elimination_logic.md`, `season_arc.md`, `the_show.md` page brief, production-strategy files, music-rights strategy. |

### Derivative Spine

The following derivative files are substantive but are not canonical anchors. They derive from canonical anchors and inform downstream operational and creative work.

| Folder | Role | Notes |
| --- | --- | --- |
| `04_competitive_landscape/` (per-comp files) | Per-show, per-platform competitive analysis. | Inform `mixhouse_white_space.md` but do not override it. |
| `04_competitive_landscape/visual_reference_analysis.md` | Reference-class analysis for cinematography and brand world. | Phase 2 derivative; informs `07_brand_world/`. |
| `04_competitive_landscape/cinematography_language.md` | Per-surface syntactic commitments for cinematography. | Phase 2 derivative; informs `07_brand_world/` and `06_production_strategy/`. |
| `04_competitive_landscape/prestige_unscripted_breakdown.md` | Category-evolution analysis. | Phase 2 derivative; informs `mixhouse_white_space.md` and `03_market_research/reality_tv_landscape.md`. |
| `03_market_research/*` | Sized market context per segment. | Inform `mixhouse_master_thesis.md` but Evidence rows must source before lifting `assumption: true`. |
| `05_business_model/*` | Revenue, franchise, rights, sponsorship modelling. | Informed by canonical anchors; inform investor decks and `business_model.md` page brief. |
| `07_brand_world/*` | Visual, tone, cultural posture. | Informed by `founder_thesis.md` (when filled) and `mixhouse_master_thesis.md`. |
| `02_show_bible/*` (non-format-engine files) | Show-craft execution detail. | Informed by `format_engine.md`. |

### Deferred Canonical Inputs

| Deferred file | Why deferred | Acceptable downstream behaviour | What requires reconciliation when input lands |
| --- | --- | --- | --- |
| `01_master_context/founder_thesis.md` | Sam Salony owns this and her completion timeline is approximately three days out. The KB does not invent founder worldview content. | Continue developing canonical and derivative files using the existing strategic spine. Mark the founder thesis as the upstream-input dependency in `related:` frontmatter. Do not paraphrase or synthesise Sam's worldview into derivative files. | Re-read every canonical anchor against `founder_thesis.md`; flag contradictions; update or supersede affected sections; lift `assumption: true` on `founder_thesis.md` only when Sam confirms. |

### Anti-Canonisation Rule

This rule prevents accidental canonisation of speculative content and prevents proliferation of near-duplicate files.

**Prefer expanding existing owner files over creating new near-duplicate files. Create new files only when the concept has a distinct retrieval role.**

Application:

- When a new concept arises (e.g., "we need to document market sizing"), first check whether an existing owner file already covers the concept. If yes, expand that file. If no, create a new file with explicit retrieval-role justification in its Purpose section.
- Per `00_system/kb_rules.md` rule 8, "No duplicate docs. If a concept already has a home, extend that file."
- Phase 2 example: the intended `market_sizing.md`, `electronic_music_demographics.md`, `streamer_unscripted_trends.md`, `festival_economics.md`, `producer_as_celebrity.md`, `short_form_discovery.md` files were merged into existing owner files (`electronic_music_market.md`, `reality_tv_landscape.md`, `festival_live_experience_market.md`, `creator_economy_signals.md`, `music_discovery_behavior.md`) rather than created as new files.

### Files That Should Never Become Retrieval Anchors

These files are supporting evidence or operational records; agents and human contributors should not treat them as canonical when constructing arguments or generating artefacts.

| Category | Examples | Why not anchors |
| --- | --- | --- |
| Source material | All of `10_source_material/*` (raw notes, transcripts, references, screenshots, quotes, stats, articles, pitch decks). | These are inputs to canonical and derivative analysis, not analyses in themselves. Citing them as anchors flattens the KB. |
| Source registry | `03_market_research/research_source_registry.md`. | Catalogues sources; does not assert claims about the world. |
| Archive | All of `99_archive/*`. | Superseded by definition. |
| System rules | `00_system/*` (other than as Tier 0 for behaviour, not as content). | Govern how the KB works; do not assert claims about the franchise. |
| Drafts in progress | Any file with `status: seed`. | Not yet substantive enough to anchor downstream work. |
| Phase plans and indexes | `00_system/phase_01_population_plan.md`, this file, folder READMEs. | Coordinate work; do not anchor it. |

### Reconciliation Strategy

When a deferred canonical input lands (currently: `founder_thesis.md`), the reconciliation pass proceeds:

1. **Read the deferred input in full.** Capture key claims, convictions, tone commitments, refusal positions, and taste references.
2. **Audit canonical anchors against the input.** For each canonical anchor, identify:
   - **Alignments** (claims that the deferred input supports).
   - **Gaps** (claims in canonical anchors that the deferred input does not address).
   - **Contradictions** (claims that the deferred input revises or refuses).
3. **Resolve contradictions explicitly.** Where the deferred input revises a canonical anchor, the canonical anchor is updated, not the deferred input. Sam's worldview takes precedence over derivative strategic argument.
4. **Update derivative files.** Once canonical anchors are aligned with the deferred input, derivative files (page briefs, business-model files, brand-world files) are re-audited against the updated canonical anchors.
5. **Lift `assumption: true` only after confirmation.** The deferred input file moves from `assumption: true` to `status: validated` only when Sam confirms the file represents her worldview accurately.
6. **Document the reconciliation pass.** Add Change Log entries to every file touched, dated to the reconciliation pass.

This strategy should run as a single coordinated branch (proposed name: `founder-reconciliation-pass`), not as scattered edits across multiple branches.

### Worked Example: Phase 2 Evidence Layer Adheres To These Rules

The Phase 2 evidence layer (introduced in `phase-2-evidence-collation` branch, 2026-05-24) demonstrates the anti-canonisation rule and the deferred-input handling:

- Six target market-research filenames were merged into existing owner files rather than created as new files.
- The founder thesis was treated as deferred canonical input; Phase 2 evidence work proceeded without paraphrasing or synthesising Sam's worldview.
- New files were created only where a concept had a distinct retrieval role: `research_source_registry.md` (catalogue function), `visual_reference_analysis.md` (per-reference editorial analysis), `cinematography_language.md` (syntactic editorial bible), `prestige_unscripted_breakdown.md` (category-evolution analysis), and this file (system-rules canonical dependency map).
- Three new source-material subfolders (`quotes/`, `stats/`, `articles/`) were created; two intended subfolders (`interview_transcripts/`, `visual_references/`) were collapsed into existing folders (`transcripts/`, `references/`) rather than created as parallel directories.

## Evidence / Sources

Not applicable. Internal system rules.

## Objections Answered

| Objection | Response |
| --- | --- |
| "Why a dependency map separate from `agent_workflow.md`?" | Workflow describes how an agent should operate; this file describes the structure agents operate against. Both are needed. |
| "Why not just declare every file canonical and let retrieval rank?" | Because retrieval that treats every file as equally canonical degrades when the KB grows. The hierarchy is a concession to scale, not a power grab. |
| "Doesn't the deferred founder thesis weaken the canonical spine?" | It would, if the spine were waiting on the founder thesis to make claims. The spine carries the strategic argument standalone; the founder thesis adds worldview and conviction depth. Reconciliation pass strengthens the spine; it does not unblock it. |
| "What if Sam's founder thesis contradicts something major in the master thesis?" | Then the master thesis revises. The founder is the originating vision holder; canonical anchors revise to align with founder worldview when conflicts arise. |
| "How do we prevent agents from accidentally treating supporting evidence as anchors?" | Per `00_system/agent_workflow.md` and this file: agents are explicitly directed to retrieve canonical anchors first, derivative spine second, supporting evidence only when traceable evidence is needed for a specific claim. |

## Website Implications

- Internal-only file. Do not surface the dependency map on public surfaces.
- Page briefs and output files should declare their canonical-anchor dependencies in frontmatter `related:` lists, per `00_system/agent_workflow.md`.
- When canonical anchors update, derivative files including page briefs must be re-audited. This is an editorial responsibility, not an automated process.

## Open Questions

- When does this file itself need updating? Proposed cadence: every phase transition (Phase 2 close, Phase 3 open) and at any reconciliation pass for a deferred input.
- Should derivative files carry an explicit `derives_from:` frontmatter field, separate from `related:`, to make the dependency machine-readable? Recommended yes; defer to Phase 3.
- Should the canonical anchors set expand beyond the current six? Proposed criterion: a file is canonical if revising it forces revision of three or more downstream files. Apply this criterion at each phase review.
- Reconciliation pass for the founder thesis: pre-schedule against Sam's expected completion date plus 24-hour read-in. Owner: founder and KB operator.

## Change Log

- 2026-05-24, Initial canonical dependency map created as part of Phase 2 evidence layer. Establishes the retrieval hierarchy, canonical anchor set, dependency map, deferred-input handling, anti-canonisation rule, files that should never become retrieval anchors, and reconciliation strategy. Documents the Phase 2 evidence layer as the first worked example of these rules in operation.
