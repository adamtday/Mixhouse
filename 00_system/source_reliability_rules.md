---
doc_type: system_rules
status: stable
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [reliability, citations, evidence, research_quality]
related:
  - 00_system/kb_rules.md
  - 00_system/research_prompt_template.md
---

# Source Reliability Rules

## Purpose

Standardise how we tier external evidence so that every claim in the KB carries an explicit confidence signal — and so that investor-grade artifacts can be assembled from `A`-tier sources only when required.

## Key Takeaways

- Every cited claim is tagged with a tier: `A`, `B`, `C`, or `assumption`.
- `A`-tier evidence is required for any number that appears in investor or broadcaster materials.
- Industry trade press is `B`-tier; LinkedIn posts and unverified Reddit threads are `C`-tier.
- An unverified internal estimate is `assumption` and must appear in `Open Questions`.
- When tiers conflict (e.g. Nielsen vs Parrot Analytics), record both and explain the chosen primary in the relevant doc.

## Core Content

### Tier Definitions

| Tier | Description | Examples |
| --- | --- | --- |
| **A** | Primary source data, peer-reviewed, audited, or first-party from a named institution. | IFPI annual report, RIAA shipment data, Nielsen ratings, audited broadcaster filings, MIDiA Research reports, official platform investor decks. |
| **B** | Reputable secondary reporting that cites primary data. | Variety, Hollywood Reporter, Music Business Worldwide, Pitchfork, The Verge, FT, Bloomberg, NYT. |
| **C** | Unverified secondary or tertiary sources, social posts, blog speculation, Reddit threads, generic SEO articles. | LinkedIn posts, Medium articles by non-experts, marketing blog round-ups, AI-generated SEO content. |
| **assumption** | Internal estimate or judgement call without external backing. | "We expect a 25% completion rate based on comparable formats." |

### Usage Rules

1. **Cite the highest tier you have.** If both an `A` and a `B` source exist, use `A`.
2. **Don't laundering-cite.** A `B` source citing an `A` source is still `B` unless you actually access the underlying `A` source.
3. **Always include date accessed.** Music and media data ages quickly.
4. **Pair conflicting sources.** If Nielsen and Parrot give different totals, include both and explain.
5. **Assumptions must be flagged.** In frontmatter set `assumption: true` for any file that materially rests on assumptions, even if other claims are well-cited.

### Investor and Broadcaster Materials

Any number that appears in:
- `11_outputs/investor_materials/`
- `08_website_strategy/page_briefs/business_model.md` rendered copy
- `05_business_model/investor_case.md`

must be backed by an `A` or `B` source. `C` and `assumption` numbers may appear in internal docs but must be explicitly relabeled or replaced before external use.

### Recording a Source

In `Evidence / Sources` tables, use:

```markdown
| 1 | "Global recorded music revenue reached $X bn in 2025" | https://ifpi.org/.../report-2026.pdf | 2026-05-20 | A |
```

When the source is a file in this repo:

```markdown
| 2 | "Pilot budget assumption of £2.4m" | ../10_source_material/raw_notes/20260418_budget_workshop.md | 2026-04-18 | assumption |
```

### Forbidden Sources

Do not cite:
- AI-generated SEO content farms.
- Wikipedia as a primary source (Wikipedia's underlying citations are fine if accessed directly).
- ChatGPT/Claude/Gemini outputs as evidence for factual claims. LLMs are tools, not sources.

## Evidence / Sources

Not applicable — internal rules.

## Objections Answered

| Objection | Response |
| --- | --- |
| "This is overkill for a pitch." | Investors and broadcasters will sanity-check our numbers. A single bad citation undermines the entire deck. |
| "It slows research down." | Marginally — and saves days of re-verification work when the deck goes out. |

## Website Implications

- Public-facing copy may only quote `A` or `B` sources. `C` and `assumption` content stays internal.
- Footnote references on `08_website_strategy/page_briefs/business_model.md` should auto-resolve from the Evidence tables.

## Open Questions

- Should we add a `D` tier for adversarial / competitor-published claims that we want to track but not rely on?
- Where do we keep PDF copies of primary sources to guard against link rot? (Proposal: `10_source_material/references/primary_sources/`.)

## Change Log

- 2026-05-20 — Initial tier definitions written.
