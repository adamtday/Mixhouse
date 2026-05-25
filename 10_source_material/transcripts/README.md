---
doc_type: source
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-24
retrieval_tags: [transcripts, interviews, source_index, raw_inputs]
related:
  - 10_source_material/README.md
  - 10_source_material/quotes/README.md
  - 00_system/naming_conventions.md
  - 00_system/source_reliability_rules.md
---

# `10_source_material/transcripts/`

## Purpose

Hold full transcripts from interviews, advisor calls, partner conversations, panel discussions, podcast recordings, and any recorded exchange that benefits from a complete searchable record. This folder is the parent home for interview, call, meeting, and recorded-transcript content; do not create a parallel `interview_transcripts/` folder.

## What Belongs Here

- Founder interviews with advisors, judges, mentors, and partners.
- Investor and commissioning-conversation transcripts (with consent).
- Panel discussion transcripts from industry events (ADE, Miami Music Week, IMS Ibiza, SXSW).
- Podcast episode transcripts where the founder or advisors participate.
- Internal team meeting transcripts when the meeting carries decision weight (e.g., format-bible review, music-rights deal structure decisions).
- Casting interview transcripts (post-consent).

## What Does Not Belong Here

- Quotes extracted from these transcripts for analytical-file use (those live in `quotes/` with a `related:` link to the parent transcript here).
- Raw audio files (those live in restricted-access storage; only the transcript belongs in the git repository).
- Off-record or anonymous exchanges (those live in `raw_notes/` with internal-only confidentiality flagging).
- Edited or excerpted versions of transcripts intended for publication (those live in `11_outputs/`).

## Naming Convention

`YYYYMMDD_type_short_topic.md`

Examples:
- `20260418_advisor_call_p_gou.md`
- `20260512_panel_ade_format_economics.md`
- `20260601_investor_meeting_acme_capital.md`
- `20260615_podcast_decoder_format_strategy.md`
- `20260701_internal_format_bible_review.md`

Type prefix establishes context:
- `advisor_call`, `partner_call`, `investor_meeting`, `casting_interview`, `panel`, `podcast`, `internal_meeting`, `press_interview`.

## Frontmatter Schema

```yaml
---
doc_type: source
status: draft
confidentiality: internal | restricted
owners: [adamtday]
last_reviewed: YYYY-MM-DD
retrieval_tags: [transcript, type_short_name, topic_tag]
source_type: transcript
related:
  - {analytical files that cite this transcript}
  - {quotes/ files that excerpt from this transcript}
participants:
  - name: {full name}
    role: {advisor / judge / mentor / partner / investor / founder / other}
    affiliation: {organisation or scene context}
    consent_status: {on-record / off-record / pending}
date_recorded: YYYY-MM-DD
duration_minutes: {integer}
recording_method: {in-person / video call / phone / panel recording}
transcription_method: {human / AI plus human review / AI only}
---
```

## Source-Quality Expectations

Transcripts inherit tier from participant context and consent:

- **A-tier**: Named participants on-the-record, transcript verified by participant or against recording.
- **B-tier**: Named participants on-the-record, transcript AI-generated with light human review.
- **C-tier**: AI-only transcription without human review; off-record or anonymous content (which should not be here in the first place).

Verified transcripts can be quoted directly. Unverified transcripts should be paraphrased in analytical files; direct quotes from unverified transcripts require participant confirmation first.

## Ingestion Rules

1. Capture the transcript as a markdown file with timestamps where the recording supports.
2. Frontmatter participant list with consent status is mandatory.
3. Long transcripts (over 5,000 words) include a Table of Contents at the top of the file (auto-generated from H2 headings).
4. For investor and commissioning conversations, consent status is critical: pending-consent transcripts are `restricted` confidentiality until consent confirms.
5. When extracting a quote for analytical use, create the quote file in `quotes/` with `related:` pointing back to this transcript.

## Archival Rules

- Transcripts are time-stamped records; do not delete superseded transcripts. When a transcript is no longer reference-worthy, move to `99_archive/transcripts/` with a Change Log entry.
- If a participant withdraws consent post-recording, remove the transcript from active retrieval and move to `99_archive/restricted/` (or delete if the participant requires).
- AI-transcribed material that has not been human-reviewed expires for direct-quote purposes after 6 months; either review the transcript or downgrade direct-quote citations to paraphrase.

## How These Connect Back

Transcripts here are cited from analytical files via Evidence rows or referenced in quotes:

```markdown
| 4 | "Scene credibility as relationship decision" (full transcript) | `../10_source_material/transcripts/20260418_advisor_call_p_gou.md` | 2026-04-18 | A |
```

When a specific quote is used, the citation points to `quotes/`, which in turn references this transcript via `related:`.

## Change Log

- 2026-05-24, Initial transcripts folder README created as part of Phase 2 source-material directory hygiene. Folder serves as parent home for interviews, calls, meetings, and recorded-transcript content; replaces the previously-considered separate `interview_transcripts/` folder.
