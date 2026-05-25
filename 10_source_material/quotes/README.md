---
doc_type: source
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-24
retrieval_tags: [quotes, source_index, raw_inputs]
related:
  - 10_source_material/README.md
  - 00_system/naming_conventions.md
  - 00_system/source_reliability_rules.md
---

# `10_source_material/quotes/`

## Purpose

Hold quotable, attributable statements gathered from interviews, public talks, press articles, podcasts, advisor conversations, and on-the-record exchanges. Quotes captured here are referenced from analytical files when a claim benefits from a named voice rather than a paraphrase.

## What Belongs Here

- Direct quotes from named contributors, advisors, judges, partners, press contacts, and credible industry voices.
- Excerpts from podcasts, interviews, or panel discussions where the speaker is on-the-record.
- Press-article excerpts where the journalist or named source is the quote's attribution.
- Investor or commissioning-conversation quotes captured live (with consent) for later use in case studies, decks, and downstream artefacts.

## What Does Not Belong Here

- Anonymous or unattributed material (those go to `raw_notes/` with an internal-only flag).
- Paraphrases (paraphrase the source in the analytical file; do not store the paraphrase here).
- Quotes from contributors who have not consented to internal capture; route those to founder for clearance first.
- Full transcripts (those live in `transcripts/`; quotes are excerpts).

## Naming Convention

`YYYYMMDD_speaker_short_topic.md`

Examples:
- `20260418_advisor_p_gou_culture.md`
- `20260512_press_resident_advisor_credibility.md`
- `20260601_panel_ade_format_economics.md`

If the quote came from a longer transcript that lives in `transcripts/`, the filename should reference the parent transcript and the timestamp:
- `20260418_advisor_p_gou_culture_from_20260418_advisor_call_p_gou.md` (full filename optional; the `related:` frontmatter must reference the parent).

## Frontmatter Schema

```yaml
---
doc_type: source
status: draft
confidentiality: internal | restricted
owners: [adamtday]
last_reviewed: YYYY-MM-DD
retrieval_tags: [quote, speaker_short_name, topic_tag]
source_type: quote
related:
  - {analytical files that cite this quote}
  - {parent transcript if this quote excerpts from one}
attribution:
  speaker: {full name}
  affiliation: {organisation or role}
  date: YYYY-MM-DD
  source_context: {interview / podcast / press article / panel / conversation}
  consent_status: {on-record / off-record / pending}
---
```

## Source-Quality Expectations

Quotes inherit the tier of the speaker and the source context:

- A named industry contributor (advisor, judge, partner) speaking on-the-record: A or B tier depending on context.
- A press journalist or named publication source: B tier.
- A podcast or panel quote: B tier, with the specific episode and timestamp cited.
- Anonymous or off-the-record material: belongs in `raw_notes/`, not here.

Per `00_system/source_reliability_rules.md`: never laundering-cite. A quote from a journalist quoting an industry figure remains tier-B unless the underlying industry figure's source is captured directly.

## Ingestion Rules

1. Capture the quote verbatim. Do not edit for clarity in the source file; clarity edits happen in the analytical file with `[sic]` or `[edited for length]` notation.
2. Capture the source context (interview, podcast, panel, press article) and timestamp or location.
3. Capture consent status. If consent is unclear or off-record, route to founder before publication.
4. Add `related:` links to analytical files that will use this quote.

## Archival Rules

- When a quote is no longer relevant (subject no longer associated, claim superseded), move to `99_archive/quotes/` with a Change Log entry, do not delete.
- If the speaker withdraws consent, remove the quote from analytical files and move the source file to `99_archive/restricted/` (or delete if the speaker requires).

## How These Connect Back

Quotes here are cited from analytical files via Evidence rows:

```markdown
| 3 | "Scene credibility is not a marketing decision; it is a relationship decision." | `../10_source_material/quotes/20260418_advisor_p_gou_culture.md` | 2026-04-18 | A |
```

The source file's `related:` frontmatter lists the analytical files that cite it.

## Change Log

- 2026-05-24, Initial quotes folder README created as part of Phase 2 source-material directory hygiene.
