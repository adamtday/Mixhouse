---
doc_type: source
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-24
retrieval_tags: [articles, press, source_index, raw_inputs]
related:
  - 10_source_material/README.md
  - 10_source_material/references/README.md
  - 00_system/naming_conventions.md
  - 00_system/source_reliability_rules.md
  - 03_market_research/research_source_registry.md
---

# `10_source_material/articles/`

## Purpose

Hold archival copies (PDF, markdown, screenshot) of press articles, editorial pieces, and trade-publication coverage that inform analytical files. Articles captured here exist as a hedge against link rot and as a citation audit trail.

The distinction between `articles/` and `references/`: `articles/` holds journalistic content (trade and mainstream press, scene editorial); `references/` holds source documents (reports, datasets, primary-source PDFs) and external references that are not journalistic articles.

## What Belongs Here

- PDF or markdown archives of press articles (Variety, Hollywood Reporter, Bloomberg, MBW, NYT, FT, The Guardian, Vogue, Hypebeast, etc.).
- Scene-press editorial (Resident Advisor, DJ Mag, Mixmag, Pitchfork, The Fader, Crack).
- Trade-press analysis pieces with named bylines (THR streamer-strategy pieces, Variety prestige-unscripted analyses).
- Podcast episode summaries or transcripts when the podcast carries journalistic weight (Decoder, MBW podcast, Switched on Pop).
- Substack newsletter posts that carry journalistic weight (Puck, The Town, Hot Pod).

## What Does Not Belong Here

- Reports and datasets (those live in `references/`).
- Screenshots of social-media posts (those live in `references/social/` or `screenshots/`).
- Direct quotes excerpted from articles for analytical-file use (those live in `quotes/` with the article cited as source).
- Aggregator content (LinkedIn shares of articles, Reddit links): cite the original article, do not archive the aggregator.

## Naming Convention

`YYYYMMDD_publication_short_topic.{pdf|md|html}`

Examples:
- `20260408_variety_netflix_prestige_unscripted_slate.pdf`
- `20260515_resident_advisor_fred_again_scene_relationship.md`
- `20260620_bloomberg_streamer_subscriber_attribution.pdf`
- `20260701_mbw_electronic_market_share_2025.md`

If the article exists only as a paywalled URL and cannot be archived, capture the citation as a markdown stub with the URL, publication, byline, date, and a 2-3 sentence excerpt:
- `20260408_variety_netflix_prestige_unscripted_slate.md`

## Frontmatter Schema

```yaml
---
doc_type: source
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: YYYY-MM-DD
retrieval_tags: [article, publication_short_name, topic_tag]
source_type: article
related:
  - {analytical files that cite this article}
attribution:
  publication: {publication name}
  byline: {author name(s)}
  date_published: YYYY-MM-DD
  url: {original article URL}
  paywall_status: {open / soft paywall / hard paywall}
  archive_method: {full PDF / markdown extract / citation-stub only}
---
```

## Source-Quality Expectations

Articles inherit publication tier per `00_system/source_reliability_rules.md`:

- **B-tier (default)**: Variety, Hollywood Reporter, Bloomberg, Music Business Worldwide, NYT, FT, The Guardian, Pitchfork, The Verge, Vogue, Hypebeast.
- **B-tier (scene)**: Resident Advisor, DJ Mag, Mixmag, The Fader, Crack, Truants.
- **A-tier**: When the article is the primary source for a claim (e.g., an earnings-call quote, a direct interview with a named source).
- **C-tier**: Aggregator round-ups, marketing blogs, unverified industry-rumour pieces. Avoid; cite the underlying primary source instead.

## Ingestion Rules

1. Capture both the article (PDF, markdown, or citation stub) and frontmatter.
2. Date-published is mandatory; date-accessed is mandatory if different.
3. Note paywall status. If hard-paywalled, the archive is a citation stub with excerpt rather than a full copy (respect publisher copyright).
4. Cross-link to the analytical file the article supports.
5. Per `00_system/source_reliability_rules.md`, do not laundering-cite. If the article cites primary-source data, capture the primary source separately in `stats/` or `references/`.

## Archival Rules

- Articles are time-stamped; do not delete superseded articles even when newer coverage replaces them. Move to `99_archive/articles/` with a Change Log entry.
- If an article is retracted by the publication, note the retraction in the source file's Change Log and update analytical files that cite it.
- For long-archive purposes (Phase 3+), consider whether to move article archives to external storage to keep the git repository performant.

## How These Connect Back

Articles here are cited from analytical files via Evidence rows:

```markdown
| 5 | "Netflix subscriber-attribution language for prestige unscripted" | `../10_source_material/articles/20260620_bloomberg_streamer_subscriber_attribution.pdf` | 2026-06-20 | B |
```

The source file's `related:` frontmatter lists the analytical files that cite the article.

## Change Log

- 2026-05-24, Initial articles folder README created as part of Phase 2 source-material directory hygiene.
