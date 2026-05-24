---
doc_type: model
status: draft
confidentiality: investor
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [music_pipeline, music_rights, format_engine, audience_behaviour]
related:
  - 05_business_model/music_rights_strategy.md
  - 02_show_bible/format_engine.md
  - 02_show_bible/episode_anatomy.md
  - 03_market_research/music_discovery_behavior.md
---

# Music Release Pipeline

## Purpose

Operationalise how MixHouse turns each episode's in-show tracks into real, commercially released music, week after week, season after season, across multiple territories.

## Key Takeaways

- The pipeline is the franchise's moat. Building it once is hard; replicating it from outside is harder.
- End-to-end: brief → studio → master → distribution → release → reaction → re-input.
- Average target: 1 track per active contestant per week, mastered and released within 24–48 hours of `Drop Night`.
- Pipeline is owned centrally (Music Supervision), executed via label partner, governed by the rights deal in `05_business_model/music_rights_strategy.md`.

## Core Content

### End-to-End Flow

```
Mon  Brief released + Crate drop
Tue  Studio sessions begin
Wed  Mentor Drop checkpoint
Thu  Mix + master + metadata locked
Fri  Drop Night (live performance)
Fri  Distribution push to DSPs
Sat  Release goes live; short-form clips deploy
Sun  72h streaming + short-form data fed back into Audience Index
```

### Operational Roles

| Role | Responsibility |
| --- | --- |
| **Music Supervisor (Format Co.)** | End-to-end quality, rights, label coordination, episode integration. |
| **Mentor Drops** | Per-episode creative steering. |
| **Supervising Engineer** | Mix / master quality control. |
| **A&R Liaison** | Editorial / DSP relationships. |
| **Label Partner** | Distribution, release schedule, royalty accounting. |
| **Short-form Lead** | Clip generation, captioning, platform-native distribution. |

### Tooling and Infrastructure

- Residency studios: scene-credible gear (controllers, synths, monitors).
- Cloud collaboration: secure DAW project storage; revision control.
- Distribution: DSP-native partner (or major-label-grade distribution).
- Pre-save and link tooling: Linkfire / Feature.fm equivalent.
- Short-form: native pipelines per platform.

### Quality Floor

The pipeline does not ship under-finished work. Quality gates:

- Mentor sign-off on creative direction (Wed).
- Supervising engineer sign-off on mix / master (Thu).
- Music Supervisor final approval (Thu).
- Rights and metadata audit (Thu).

A track that fails any gate is held back. Contestant's `Drop Night` is filled with prior-week material; the elimination index for that contestant excludes the unreleased track.

### Metadata Discipline

Every release carries:
- Producer credit(s).
- Co-writer credit(s), including mentors if applicable.
- Label imprint.
- ISRC / ISWC codes.
- Release territory list (default: all available).
- Pre-save flow URLs.

Bad metadata is fatal to long-tail royalties. The pipeline enforces it.

### Compounding Releases

Each release accumulates streams over weeks; the cohort streaming data feeds back into elimination math (see `02_show_bible/elimination_logic.md`). The catalogue compounds across:
- DSP editorial pickups.
- Sync placements (post-release).
- Tour set placements.
- Year-end soundtrack album.

### Territory Adaptation

In each territory, the same pipeline runs with a local Music Supervisor reporting to central Music Supervision. Label partner may be local; rights structure stays centralised.

### Risks

| Risk | Mitigation |
| --- | --- |
| Track fails QC by Thu | Use prior-week B-side; contestant's index excludes the missed release that week. |
| DSP partner outage | Distribute via secondary partner; pre-tested fallback. |
| Mastering bottleneck | Two engineers on rotation. |
| Metadata error | Pre-release metadata audit Step 4 of pipeline. |
| Contestant retracts a release | Contract terms require completion or alternative release; rare. |

### Why This Cannot Be Bolted On Later

- Building a music supervision team takes 6–12 months.
- Label partner relationships take months to negotiate.
- DSP relationships compound on prior release history.
- Rights deal templates require iteration with talent and legal.

This is the structural moat MixHouse builds early.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | DSP release timing best practice (Friday window) | Music Business Worldwide / DSP partner guidance (target) | n/a | B (target) |
| 2 | Metadata-quality impact on long-tail royalties | Music Reports / IFPI (target) | n/a | A/B (target) |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Releasing real music inside a reality show is unprecedented." | That's the point. The unprecedented operational difficulty is also the competitive moat. |
| "Quality will be uneven." | Quality floor is enforced by gates. Uneven is fine, we're not releasing pop hits, we're releasing scene-credible music with real character. |

## Website Implications

- Public site shows release cadence on the season hub.
- "How the music gets made" interactive on `the_show.md` maps the pipeline.

## Open Questions

- DSP partner choice and exclusivity windows.
- Label partner for pilot vs S1 vs S2+.
- Mentor compensation and credit policy.

## Change Log

- 2026-05-20, Initial pipeline drafted.
