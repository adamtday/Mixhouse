---
doc_type: research
status: draft
confidentiality: investor
owners: [adamtday]
last_reviewed: 2026-05-24
retrieval_tags: [research_registry, sources, citations, evidence, research_quality]
related:
  - 00_system/source_reliability_rules.md
  - 03_market_research/electronic_music_market.md
  - 03_market_research/festival_live_experience_market.md
  - 03_market_research/reality_tv_landscape.md
  - 03_market_research/creator_economy_signals.md
  - 03_market_research/music_discovery_behavior.md
  - 03_market_research/why_now.md
assumption: false
---

# Research Source Registry

## Purpose

Maintain a single index of every external source the KB plans to or already cites, with access status and the files that depend on each source, so research operators can plan acquisition, avoid duplicated effort, and surface broken or paywalled dependencies before they block downstream artefacts.

This file is `assumption: false` because it is a registry of intent and access status, not a claim about the world. The sources it tracks may themselves be A, B, or C tier per `00_system/source_reliability_rules.md`.

## Key Takeaways

- Every quantitative claim in the KB should trace to a row in this registry. If a citation is added to a Phase 1 or Phase 2 file, the source belongs here.
- Access status (`have`, `paywalled`, `outreach needed`, `open`, `partner-gated`) tells research operators where to focus acquisition effort.
- The registry distinguishes **named institutional sources** (IFPI, MIDiA, Pollstar, Nielsen) from **trade press** (Variety, Bloomberg, MBW) from **platform-published reports** (Spotify Loud and Clear, TikTok What's Next) from **scene press** (Resident Advisor, DJ Mag, Mixmag).
- Sourcing is the Phase 2 critical path. The `(target)` rows across `03_market_research/` Evidence tables and the canonical spine cannot lift `assumption: true` until rows here move from `outreach needed` to `have`.
- Source acquisition is owned by a designated research operator. Founder time should not be the bottleneck for sources beyond direct industry-relationship-gated data.

## Core Content

### Registry

Tier follows `00_system/source_reliability_rules.md`: A (primary, audited, named institution), B (reputable secondary), C (unverified secondary). Access status: `have` (in repo or downloaded), `paywalled` (subscription required), `outreach needed` (request access from publisher or contact), `open` (publicly accessible without cost or login), `partner-gated` (only accessible through a partner relationship MixHouse needs to establish).

| Source | Tier | Reliability | Access status | Used in | Notes |
| --- | --- | --- | --- | --- | --- |
| IFPI Global Music Report | A | Primary; audited industry body | Open (annual report); paywalled (full dataset) | `electronic_music_market.md`, `festival_live_experience_market.md`, `why_now.md` | Top-line recorded music revenue and regional cuts; cited by every credible music investor pack. |
| IFPI Engaging With Music | A | Primary consumer survey | Open (summary); paywalled (full report) | `music_discovery_behavior.md`, `electronic_music_market.md` | Consumer-behaviour cuts; live attendance and streaming engagement. |
| MIDiA Research | A | Primary research; subscription | Paywalled | `electronic_music_market.md`, `music_discovery_behavior.md`, `creator_economy_signals.md` | Genre-by-demo cuts; indie artist income reports; consumer surveys; subscription costs material. |
| Luminate (formerly MRC Data / Nielsen Music) | A | Primary streaming and sales data | Paywalled | `electronic_music_market.md`, `music_discovery_behavior.md` | Year-End Report; genre-by-demo cuts. |
| Nielsen | A | Primary ratings; audited | Paywalled | `reality_tv_landscape.md` | TV ratings data; singing-competition decline evidence. |
| Parrot Analytics | A | Demand-side TV analytics | Paywalled | `reality_tv_landscape.md` | Demand-volume cuts; prestige unscripted subscriber-attribution evidence. |
| BARB (UK) | A | UK broadcast ratings; audited | Open (summary); partner-gated (full data) | `reality_tv_landscape.md` | UK ratings for singing-competition decline. |
| Pollstar Year-End Worldwide Concert Industry | A | Primary touring industry data | Paywalled (full report); open (top-line headlines) | `festival_live_experience_market.md`, `creator_economy_signals.md` | Top-100 festival attendance; producer-as-celebrity touring evidence. |
| Pollstar Boxscore | A | Audited touring revenue | Paywalled | `creator_economy_signals.md` | Named-producer touring economics evidence (Fred again.., Charlotte de Witte, John Summit, Bicep). |
| Billboard | B | Trade-press; charts (A-tier) | Open | `creator_economy_signals.md`, `electronic_music_market.md` | Billboard charts at A-tier; editorial coverage at B-tier. |
| Billboard Boxscore | A | Audited touring data | Paywalled | `creator_economy_signals.md` | Named-producer touring sourcing. |
| PwC Global Entertainment and Media Outlook | A | Primary forecast and sizing | Paywalled (full); open (summary) | `electronic_music_market.md`, `festival_live_experience_market.md` | Global media and music sizing; 5-year forecasts. |
| Deloitte Tech Media Telecoms Predictions | A | Primary analyst forecast | Open | `reality_tv_landscape.md`, `music_discovery_behavior.md` | Annual TMT predictions; streaming and short-form. |
| IQ Magazine European Festival Report | B | Trade-press primary survey | Paywalled (full); open (summary) | `festival_live_experience_market.md` | European festival market sizing and sponsorship benchmarks. |
| IEG Sponsorship Report | B | Trade-press sponsorship data | Paywalled | `festival_live_experience_market.md`, `05_business_model/sponsorship_inventory.md` | Sponsorship category mix; multi-year-contract benchmarks. |
| IAB | A/B | Industry body sponsorship data | Open | `05_business_model/sponsorship_inventory.md` | Sponsorship category and digital advertising data. |
| WARC | A/B | Industry body advertising research | Paywalled | `05_business_model/sponsorship_inventory.md` | Brand-spend and category benchmarks. |
| Spotify Loud and Clear | A | Platform-published artist economics data | Open | `creator_economy_signals.md`, `music_discovery_behavior.md` | Per-artist streaming economics. |
| Spotify Equity Reports | A | Platform-published demographic and equity data | Open | `electronic_music_market.md`, `music_discovery_behavior.md` | Regional and demographic cuts. |
| Apple Music public reports | A/B | Platform-published partial data | Open | `music_discovery_behavior.md` | Editorial and discovery framing; less comprehensive than Spotify. |
| Amazon Music public reports | B | Platform-published partial data | Open | `music_discovery_behavior.md` | Limited primary data; trade-press round-ups. |
| YouTube Culture and Trends Report | A | Platform-published primary data | Open | `music_discovery_behavior.md`, `creator_economy_signals.md` | Annual trends; music and creator behaviour. |
| TikTok For Business / What's Next | A | Platform-published primary data | Open | `music_discovery_behavior.md`, `creator_economy_signals.md` | Music-discovery behaviour; trend velocity. |
| Live Nation Annual Report and Investor Presentations | A | Primary; SEC-filed | Open | `festival_live_experience_market.md` | Live music industry economics; venue and festival operations. |
| AEG Presents disclosures | A/B | Primary plus trade-press | Partner-gated for full data | `festival_live_experience_market.md` | Live music industry economics. |
| Tomorrowland operator filings | A | Primary; Belgian filings | Outreach needed | `festival_live_experience_market.md` | Headline festival economics. |
| Festicket and Songkick public data | B/C | Aggregator data | Open | `festival_live_experience_market.md` | Festival attendance estimates; quality varies by region. |
| Variety | B | Trade press | Open (most coverage); paywalled (some) | `reality_tv_landscape.md`, `creator_economy_signals.md` | Streamer commissioning, CPH, prestige unscripted coverage. |
| Hollywood Reporter | B | Trade press | Open (most); paywalled (some) | `reality_tv_landscape.md` | Streamer commissioning and slate analysis. |
| Bloomberg | B | Trade press / financial | Paywalled (most) | `reality_tv_landscape.md`, `creator_economy_signals.md` | Streaming economics; subscriber attribution. |
| Music Business Worldwide | B | Trade press; music industry | Open (most); paywalled (some) | `creator_economy_signals.md`, `electronic_music_market.md` | Rights, deal economics, industry restructuring. |
| Music Ally | B | Trade press; music tech | Open (newsletter); paywalled (premium) | `music_discovery_behavior.md` | Music tech and DSP behaviour. |
| Resident Advisor | B | Scene press; editorial | Open | `creator_economy_signals.md`, `04_competitive_landscape/cercle.md`, `04_competitive_landscape/boiler_room.md` | Scene credibility; sub-genre coverage; producer profiles. |
| DJ Mag | B | Scene press; editorial | Open | `creator_economy_signals.md`, `04_competitive_landscape/visual_reference_analysis.md` | Producer rankings (Top 100); scene coverage. |
| Mixmag | B | Scene press; editorial | Open | `creator_economy_signals.md`, `04_competitive_landscape/visual_reference_analysis.md` | Scene coverage; mix release context. |
| Chartmetric | A/B | Cross-DSP analytics | Subscription | `music_discovery_behavior.md`, `creator_economy_signals.md` | Cross-platform tracking; clip-to-stream attribution. |
| Splice corporate disclosures | B | Platform data | Open (limited); outreach needed (full) | `creator_economy_signals.md` | Producer population proxy. |
| Native Instruments user data | B | Platform data | Outreach needed | `creator_economy_signals.md` | Producer population proxy. |
| DistroKid annual reports | B | Platform-published indie release data | Open | `creator_economy_signals.md` | Independent release volume. |
| Beatport public data | B | Platform-published genre charts | Open | `electronic_music_market.md`, `creator_economy_signals.md` | Sub-genre share; active label count. |
| Traxsource public data | B | Platform-published genre charts | Open | `electronic_music_market.md` | House and soulful electronic sub-genre data. |
| Vogue | B | Mainstream press; fashion | Open | `creator_economy_signals.md` | Brand-deal precedent (Peggy Gou Bottega, Honey Dijon collaborations). |
| Hypebeast | B | Trade-press; lifestyle | Open | `creator_economy_signals.md` | Brand-deal precedent; producer-fashion crossover. |
| The New York Times culture desk | B | Mainstream press | Paywalled (most); open (some) | `creator_economy_signals.md` | Cultural-context coverage of named producers. |
| The Guardian | B | Mainstream press | Open (most) | `creator_economy_signals.md` | UK / EU coverage of named producers and scene. |
| The Verge | B | Tech press | Open | `music_discovery_behavior.md` | Music-tech and DSP behaviour coverage. |
| FT (Financial Times) | B | Mainstream press; financial | Paywalled | `reality_tv_landscape.md`, `festival_live_experience_market.md` | Streaming and live-music industry coverage. |
| RIAA | A | US industry body | Open | `electronic_music_market.md` | US-specific recorded music data. |
| Soundscan | A | US sales and streaming data | Paywalled | `electronic_music_market.md` | US streaming and sales detail. |
| 1001Tracklists | B | Community-curated DJ set data | Open | `music_discovery_behavior.md` | DJ set catalogue revival evidence. |
| BBC Sounds and Radio 1 Essential Mix | A | UK public-service broadcaster | Open | `04_competitive_landscape/visual_reference_analysis.md` | UK scene legitimacy signal. |

### Access Status Summary

| Access status | Count (approx) | Implication |
| --- | --- | --- |
| Open | 18 | Immediate research operator can ingest. |
| Paywalled (subscription) | 12 | Budget decision required; many are critical for A-tier sourcing. |
| Outreach needed | 5 | Direct relationship or research request required. |
| Partner-gated | 3 | Requires MixHouse to first establish a partner relationship before access. |

### Subscription Stack To Consider

For Phase 2 to lift `assumption: true` on the canonical files, the following subscription stack is likely required. Costs are illustrative pending vendor quotes; decisions are budget-owner judgement.

| Subscription | Why critical | Substitutes |
| --- | --- | --- |
| MIDiA Research | Genre-by-demo cuts; indie artist income; consumer surveys. | None at equivalent granularity. |
| Luminate (formerly MRC Data) | Streaming and sales authoritative source for US, UK, and most major markets. | Nielsen / Soundscan partial coverage. |
| Pollstar Year-End plus Boxscore | Festival attendance and named-producer touring economics. | IQ Magazine partial; trade-press estimates. |
| Parrot Analytics | Subscriber-attribution and demand-volume evidence for prestige unscripted. | Nielsen partial; trade-press estimates. |
| Chartmetric | Cross-DSP analytics for clip-to-stream attribution and DJ set catalogue revival. | DSP-partner-specific data when relationships land. |

### Notes On Source Hygiene

- Apply tier rules from `00_system/source_reliability_rules.md`. Do not laundering-cite: a `B` source citing an `A` source remains `B` unless the underlying `A` source is accessed directly.
- Date-accessed is mandatory for every citation. Music and media data ages quickly.
- When tiers conflict (e.g. Nielsen vs Parrot), record both sources in the Evidence row and explain the chosen primary in the parent file.
- Public-facing copy (per `00_system/source_reliability_rules.md`) only quotes A or B tier. C and assumption content stays internal.

## Evidence / Sources

Not applicable. This is a registry of sources, not a claim about the world.

## Objections Answered

| Objection | Response |
| --- | --- |
| "Why duplicate the source list across this file and the Evidence tables?" | The Evidence tables are claim-specific; this registry is source-specific. The registry tracks access status and acquisition effort across the whole KB; the Evidence tables track per-claim citations. Both are needed. |
| "MIDiA and Luminate subscriptions are expensive." | Yes. The cost is small relative to the cost of being wrong in an investor or commissioning conversation. The subscription decision is a budget-owner call, not an operator default. |
| "Trade press is B-tier; isn't that not good enough for investor copy?" | Trade press is acceptable for investor copy when no A-tier source exists, per `00_system/source_reliability_rules.md`. Several MixHouse claims will land at B-tier and that is fine, provided the limitation is noted alongside the figure. |

## Website Implications

- This file is internal-only. Do not surface the source registry on the public site.
- Public-facing copy on `08_website_strategy/page_briefs/business_model.md` and the press kit derives citations from this registry indirectly via the parent file's Evidence table.

## Open Questions

- Designate a named research operator with explicit ownership for source acquisition. Owner: founder.
- Budget approval for MIDiA, Luminate, Pollstar Year-End, Parrot, and Chartmetric subscriptions. Owner: founder.
- Identify which partner-gated sources (Tomorrowland, AEG, BARB full data) can be unlocked via existing advisor or investor relationships rather than cold outreach.
- Decide whether to maintain primary-source PDFs in `10_source_material/references/primary_sources/` for archival purposes (proposed in `00_system/source_reliability_rules.md` Open Questions).
- Should the registry expand to track competitor-published claims at C-tier for adversarial tracking?
- Quarterly review cadence: who is responsible for keeping access-status accurate as subscriptions are added or expired?

## Change Log

- 2026-05-24, Initial research source registry created as part of Phase 2 evidence layer. Catalogues every source the KB plans to or already cites, with access status and dependent files per source. Subscription stack to consider section identifies the critical paid sources for Phase 2 sourcing to land at A or B tier.
