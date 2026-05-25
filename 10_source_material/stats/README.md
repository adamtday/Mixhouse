---
doc_type: source
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-24
retrieval_tags: [stats, statistics, evidence, source_index, raw_inputs]
related:
  - 10_source_material/README.md
  - 00_system/naming_conventions.md
  - 00_system/source_reliability_rules.md
  - 03_market_research/research_source_registry.md
---

# `10_source_material/stats/`

## Purpose

Hold quantitative source artefacts (CSVs, screenshots of dashboards, downloaded PDF tables, raw extracts) that underwrite numerical claims in analytical files. Stats captured here are the audit trail behind every cited figure in the KB.

## What Belongs Here

- CSV / XLSX extracts from named sources (IFPI, MIDiA, Luminate, Pollstar, Parrot, Spotify Loud and Clear, Chartmetric).
- Screenshots of analyst-platform dashboards (Parrot demand index, Chartmetric track performance, Spotify for Artists).
- Annotated PDF tables extracted from larger reports (per `00_system/source_reliability_rules.md`, full PDFs may live in `references/primary_sources/` when archival storage decision lands).
- Computed-from-source workings (e.g., a CSV that combines two raw extracts into a derived figure), with the derivation method documented.

## What Does Not Belong Here

- Final-form chart graphics for decks and the website (those live in `11_outputs/` or the web project's assets).
- LLM-generated estimates or projections (LLMs are tools, not sources, per `00_system/source_reliability_rules.md`).
- Marketing-blog roundups citing other sources (cite the underlying source directly; do not laundering-cite).
- Personal estimates without external backing (those are assumptions, flagged in analytical-file frontmatter).

## Naming Convention

`YYYYMMDD_source_short_topic.{csv|xlsx|png|pdf|md}`

Examples:
- `20260424_ifpi_global_music_2026_recorded_revenue.csv`
- `20260512_chartmetric_fred_again_top_tracks_72h.png`
- `20260601_pollstar_year_end_top_100_festivals.xlsx`
- `20260615_midia_genre_by_demo_under_30.pdf`

If the stat is a derivation, prefix with `derived_`:
- `derived_20260620_electronic_share_of_live_method_a.md`

## Frontmatter Schema (For Companion `.md` Files Describing The Stat)

Binary files (CSV, XLSX, PNG, PDF) sit alongside a companion `.md` file that carries the frontmatter and documents the source. The companion file shares the binary's name with `.md` extension.

```yaml
---
doc_type: source
status: draft
confidentiality: internal | restricted
owners: [adamtday]
last_reviewed: YYYY-MM-DD
retrieval_tags: [stat, source_short_name, topic_tag]
source_type: stat
related:
  - {analytical files that cite this stat}
attribution:
  source: {named institution; per 03_market_research/research_source_registry.md}
  source_tier: A | B | C
  date_accessed: YYYY-MM-DD
  date_of_data: YYYY-MM-DD or YYYY range
  access_method: {download URL / dashboard screenshot / report extract / subscription portal}
  license_constraints: {any redistribution or quote constraints}
---
```

## Source-Quality Expectations

Stats inherit the tier of the underlying source per `00_system/source_reliability_rules.md`:

- **A-tier**: IFPI, RIAA, Nielsen, BARB, Pollstar Year-End, Luminate, MIDiA, Spotify Loud and Clear, platform-published investor disclosures.
- **B-tier**: Variety, Bloomberg, THR, MBW, IQ Magazine, Chartmetric (cross-DSP analytics), Resident Advisor data.
- **C-tier**: Aggregator data (Festicket, Songkick), social-media impression dashboards, marketing-blog roundups (avoided; cite underlying source directly when possible).

If a stat exists only at C-tier, capture it with an explicit note that an A or B tier upgrade is needed before the figure leaves internal files.

## Ingestion Rules

1. Capture both the binary file and a companion `.md` frontmatter file.
2. Date-accessed is mandatory. Music and media data ages quickly per `00_system/source_reliability_rules.md`.
3. Note license constraints. Some subscription data (MIDiA, Luminate, Parrot) carries redistribution constraints; document those at ingestion.
4. Cross-link to `03_market_research/research_source_registry.md` for the parent source row.
5. Cross-link to the analytical file the stat will be cited from. If no analytical file exists yet, document the intended use in the companion `.md`.

## Archival Rules

- When a stat is superseded by a newer source extract (e.g., 2027 IFPI report replaces 2026), move the older file to `99_archive/stats/` with a Change Log entry. Do not delete; the audit trail matters.
- Subscription-licensed data files: do not duplicate beyond the KB; if a contributor's access expires, ingest only their downloaded extract, not their license.

## How These Connect Back

Stats here are cited from analytical files via Evidence rows:

```markdown
| 1 | "Global recorded music revenue reached $X bn in 2025" | `../10_source_material/stats/20260424_ifpi_global_music_2026_recorded_revenue.csv` | 2026-04-24 | A |
```

The companion `.md` file's `related:` frontmatter lists the analytical files that cite the stat.

## Change Log

- 2026-05-24, Initial stats folder README created as part of Phase 2 source-material directory hygiene.
