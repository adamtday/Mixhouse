---
doc_type: competitive
status: draft
confidentiality: investor
owners: [adamtday]
last_reviewed: 2026-05-25
retrieval_tags: [reference_taxonomy, visual_intelligence, retrieval_vocabulary, brand_world, cinematography, interaction_design]
related:
  - 04_competitive_landscape/visual_reference_analysis.md
  - 04_competitive_landscape/cinematography_language.md
  - 04_competitive_landscape/reference_analysis_template.md
  - 07_brand_world/visual_principles.md
  - 07_brand_world/visual_positioning.md
  - 07_brand_world/moodboard_references.md
  - 10_source_material/references/README.md
  - 10_source_material/screenshots/README.md
  - 10_source_material/reference_capture_workflow.md
  - 00_system/retrieval_tags.md
assumption: true
---

# Reference Taxonomy

## Purpose

Provide a single, structured vocabulary for categorising every visual, cinematic, editorial, and interaction reference the MixHouse KB ingests. The taxonomy is the controlled vocabulary the rest of the visual-intelligence layer leans on: capture workflows tag against it, analysis templates classify against it, brand-world principles audit against it, and future Fumadocs retrieval queries filter against it.

`04_competitive_landscape/visual_reference_analysis.md` analyses a curated set of cinematic source references through five reference classes. This file generalises that vocabulary into the broader taxonomy the KB needs as references grow beyond cinematic source material into editorial systems, interaction patterns, and brand identity systems. Visual reference analysis is a subset of the taxonomy; the taxonomy is the parent set.

## Key Takeaways

- A reference without a category is unindexed and effectively lost. Every reference ingested into the KB carries at least one category tag from this taxonomy.
- The taxonomy is deliberately broad. Visual intelligence is not just cinematography; it spans editorial typography, interaction pacing, fan-participation systems, executive-persuasion grammar, and audio-reactive interface behaviour.
- Each category has explicit qualifying and disqualifying criteria. The qualifying criteria prevent noise; the disqualifying criteria prevent category drift.
- Retrieval implications are stated per category so future Fumadocs portal and website-strategy work can query the right slice of the reference set.
- The taxonomy is versioned. New categories require a Change Log entry and a one-line justification; collapsing or renaming categories is a separate review pass.

## Core Content

### Taxonomy Overview

| Category | Slug | Owner surface | Retrieval anchor it feeds |
| --- | --- | --- | --- |
| Cinematic Storytelling | `cinematic_storytelling` | Show cinematography | `04_competitive_landscape/cinematography_language.md` |
| Editorial Systems | `editorial_systems` | Website, press kit, deck | `07_brand_world/visual_positioning.md` |
| Premium Typography | `premium_typography` | Brand identity, website | `07_brand_world/visual_principles.md` |
| Interaction Pacing | `interaction_pacing` | Website, future Fumadocs, app surfaces | `07_brand_world/visual_principles.md` |
| Prestige Unscripted | `prestige_unscripted` | Show grammar, category positioning | `04_competitive_landscape/prestige_unscripted_breakdown.md` |
| Artist Identity Systems | `artist_identity` | Cast portrait, music-press surfaces | `07_brand_world/cultural_authenticity.md` |
| Festival Visual Language | `festival_visual` | Final-set cinematography, partner identity | `03_market_research/festival_live_experience_market.md` |
| Music-World Authenticity | `music_authenticity` | Scene-credibility audit, casting on-ramp | `07_brand_world/cultural_authenticity.md` |
| Fan Participation | `fan_participation` | Audience strategy, social surfaces | `03_market_research/creator_economy_signals.md` |
| Luxury Restraint | `luxury_restraint` | Brand identity, sponsorship | `07_brand_world/visual_principles.md` |
| Progressive Disclosure | `progressive_disclosure` | Website information architecture, deck | `07_brand_world/visual_principles.md` |
| Executive Persuasion | `executive_persuasion` | Investor materials, partner deck | `11_outputs/` (future) |
| Emotional Escalation | `emotional_escalation` | Episode arc, trailer, finale | `04_competitive_landscape/cinematography_language.md` |
| Immersive Transitions | `immersive_transitions` | Show open/close, page-level transitions | `04_competitive_landscape/cinematography_language.md` |
| Audio-Reactive Systems | `audio_reactive` | Live activations, web hero, DSP visualisers | `07_brand_world/visual_principles.md` |

### Per-Category Definition

#### Cinematic Storytelling

- **What qualifies.** Long-form film and series cinematography that uses lens, light, blocking, and sound to advance narrative; demonstrable use of scripted-grade DP work in documentary or unscripted contexts; episode-level emotional arc construction visible in the cut.
- **What disqualifies.** Reality-confessional grammar; broadcast multi-camera light-entertainment cutting; promo-style music-video cinematography masquerading as narrative.
- **Why it matters to MixHouse.** Cinematic storytelling is the editorial spine; references in this category teach how to build narrative through cinematography rather than through voiceover or confession.
- **Example sources.** `Drive to Survive`, `Cheer`, `Beckham`, `The Last Dance`, `Welcome to Wrexham`, `Renaissance`, `Avicii: True Stories`.
- **Retrieval implications.** Feeds cinematography decisions, DP shortlist conversations, and trailer-language briefs. Surfaces in queries about "how does the show look", "what is the editorial spine", "which references inform residency cinematography".

#### Editorial Systems

- **What qualifies.** Print, digital, and brand publishing systems with explicit grid, hierarchy, and rhythm. Independent magazines, prestige newspaper digital design, fashion publication architecture, and brand-led editorial channels.
- **What disqualifies.** Marketing landing pages styled to look editorial without underlying system; brand blogs without typographic discipline; content farms with editorial veneer.
- **Why it matters to MixHouse.** The website and press kit read as editorial publications, not as marketing collateral. Editorial systems supply the grammar.
- **Example sources.** The Gentlewoman, The Travel Almanac, Apartamento, Resident Advisor long-form, FT Weekend digital, NYT cooking section architecture, Apple Newsroom, A24 publication channels.
- **Retrieval implications.** Feeds `08_website_strategy/page_briefs/` architecture decisions, press-kit format, deck-template design. Surfaces in queries about "how should the website read", "what does an editorial page look like", "what is our reading rhythm".

#### Premium Typography

- **What qualifies.** Type families and typographic systems with editorial restraint, considered weight progression, and clear hierarchy logic. References that demonstrate type as a brand-voice carrier, not as decoration.
- **What disqualifies.** Display fonts used for personality without system; condensed sans used as a default; trend-driven type choices without underlying brand logic; type-as-graphic-effect.
- **Why it matters to MixHouse.** Type is the most economical brand-voice carrier across every surface. Premium typography decisions outlive any single campaign.
- **Example sources.** GT Sectra in editorial use, Söhne by Klim, Migra by Pangram, MASS-Driver releases, Commercial Type catalogue, Dinamo Typefaces, Bottega Veneta brand typography, Apple corporate typography.
- **Retrieval implications.** Feeds `09_design_system/typography.md`, brand-identity decisions, and website-strategy hierarchy. Surfaces in queries about "what does our type system carry", "what fonts read as premium without reading as luxury-stereotype".

#### Interaction Pacing

- **What qualifies.** Digital products and web experiences where the rhythm of interaction (scroll behaviour, transition timing, response latency, focus shifts) is itself an editorial choice. References that demonstrate restraint and confidence in pacing.
- **What disqualifies.** Auto-play motion that overrides user pace; scroll-jacking without payoff; transition timings designed to demonstrate technical capability rather than serve content.
- **Why it matters to MixHouse.** The future website and Fumadocs portal will inherit pacing decisions. Audiences read interaction pacing as a brand signal before they read copy.
- **Example sources.** Apple product pages (specific releases), Vercel marketing site interaction rhythm, Linear app marketing pages, Stripe documentation pacing, Are.na browsing rhythm, A24 film pages, Criterion Collection film pages.
- **Retrieval implications.** Feeds `08_website_strategy/page_briefs/` interaction decisions, future Fumadocs portal pacing, and component-system motion baselines. Surfaces in queries about "how should the site feel to scroll", "what is our pacing language".

#### Prestige Unscripted

- **What qualifies.** Unscripted series and films commissioned, produced, and marketed at scripted-prestige tier; named DPs, cinematic grading, music supervision at scripted level, multi-episode emotional architecture.
- **What disqualifies.** Reality competition formats; talk-show grammar; broadcast docu-series at TV-tier production value.
- **Why it matters to MixHouse.** The category MixHouse competes inside. Every commissioning conversation and brand-positioning conversation routes through this category.
- **Example sources.** `Drive to Survive`, `The Last Dance`, `Cheer`, `Welcome to Wrexham`, `Quarterback`, `Beckham`, `Tiger`, `OJ: Made in America`, `Senna` (Netflix series).
- **Retrieval implications.** Feeds commissioning narrative, investor positioning, and category-defence arguments. Surfaces in queries about "what category are we in", "what is the commissioning benchmark".

#### Artist Identity Systems

- **What qualifies.** Visual systems built around an artist's brand world: tour identity, album-cycle visual systems, residency identity, named-producer brand identity. References that treat artist visual identity as a sustained system rather than per-release art direction.
- **What disqualifies.** Single-album art treated as system; tour merchandise without underlying identity logic; AI-generated artist visuals without curatorial authorship.
- **Why it matters to MixHouse.** The format produces named producers whose post-show identity carries the show's cultural authority. Identity systems inform cast-portrait direction, press positioning, and brand-partner introductions.
- **Example sources.** Daft Punk identity across album cycles, Aphex Twin / Warp visual identity, Fred again.. visual system, Charlotte de Witte KNTXT identity, Bicep Chroma identity, Floating Points tour identity, Nicolas Jaar / Other People label identity.
- **Retrieval implications.** Feeds casting funnel, cast-portrait sessions, press-kit direction, and post-show brand-partner introductions. Surfaces in queries about "how do we present cast", "what identity systems do producers carry into the show".

#### Festival Visual Language

- **What qualifies.** Festival and large-event visual systems including stage design, brand identity, livestream cinematography, and audience-facing wayfinding. References that demonstrate visual system across pre-event, on-site, and post-event surfaces.
- **What disqualifies.** Single-poster festival art without system; sponsor-led festival visuals; reality-TV music-festival staging (large flat LED walls without spatial logic).
- **Why it matters to MixHouse.** Finale takes place at a partner festival; the show's cinematography must integrate with the festival's existing visual language. Future Mixhouse-branded festival or activation also needs reference grounding.
- **Example sources.** Tomorrowland stage and brand identity, Awakenings stage and brand identity, Sónar visual identity, DGTL festival identity, Dekmantel festival identity, Time Warp visual language, MUTEK festival identity, Coachella stage cinematography.
- **Retrieval implications.** Feeds finale cinematography, partner-festival shortlist research, and future activation design. Surfaces in queries about "what does the finale look like", "what festival visual languages do we integrate with".

#### Music-World Authenticity

- **What qualifies.** Visual references that scene insiders recognise as their own: independent label visuals, scene press, club identity, residency identity, fanzine and zine culture, scene-photography traditions.
- **What disqualifies.** Industry-marketing visuals styled to look scene-credible; major-label attempts at scene aesthetic without scene authorship; AI-generated scene visuals.
- **Why it matters to MixHouse.** Scene credibility is structural to the format. The visual system has to pass the scene-recognition test before it passes the prestige-cinematic test.
- **Example sources.** Resident Advisor editorial visual identity, DJ Mag identity through its history, Mixmag identity, label identities (Hyperdub, Hessle Audio, Drumcode, KNTXT, XL Recordings, Warp), club identities (Berghain, fabric, Output legacy, Robert Johnson, De School legacy), scene-photographer archives (Vinca Petersen, Molly Macindoe, Wolfgang Tillmans music work).
- **Retrieval implications.** Feeds scene-credibility audit on every brand decision, music-supervision direction, and cast-introduction copy. Surfaces in queries about "does this read as scene-credible", "what scene references inform brand world".

#### Fan Participation

- **What qualifies.** Visual and interaction systems that invite audience participation as a brand choice: official fan-art systems, audience-vote interfaces, second-screen formats, user-generated-content frames with editorial discipline.
- **What disqualifies.** Open social-media free-for-alls without curation; comment-section participation without visual identity; participation framed as marketing rather than as cultural commitment.
- **Why it matters to MixHouse.** Audience verdict at `Drop Night` is a format primitive. The visual systems that frame audience participation are brand decisions, not afterthoughts.
- **Example sources.** Eurovision official fan-voting visual systems, Wrexham fan participation in club identity, Korean idol-format fan-vote systems, A24 letterboxd-style audience-letterbox participation, Criterion Channel community lists, Genius lyric annotation system.
- **Retrieval implications.** Feeds `08_website_strategy/page_briefs/audience.md`, second-screen and companion-app decisions, and audience-vote interface design. Surfaces in queries about "how do audiences participate", "what does our second-screen look like".

#### Luxury Restraint

- **What qualifies.** Brand visual systems where what is not shown carries as much weight as what is. References that demonstrate confident restraint across product, campaign, and digital surfaces. Restraint as the message rather than restraint as the absence of message.
- **What disqualifies.** Minimalism as default without intent; brand identity confused with minimal-aesthetic trend; restraint that reads as under-investment rather than as confidence.
- **Why it matters to MixHouse.** The brand world is restrained by deliberate choice. Luxury restraint references demonstrate how to communicate confidence and seriousness without volume.
- **Example sources.** Bottega Veneta (Daniel Lee era and after), Loewe under Jonathan Anderson, Phoebe Philo Celine and post-Celine work, Apple product launch grammar, Acne Studios brand world, A24 brand presence, The Row, Issey Miyake legacy.
- **Retrieval implications.** Feeds brand-identity audit, sponsorship-partner shortlist (alignment check), and editorial-restraint discipline on every surface. Surfaces in queries about "what restraint references inform brand world", "what does premium look like without luxury-stereotype".

#### Progressive Disclosure

- **What qualifies.** Information architecture and editorial systems that reveal complexity in layers, by user intent. References that demonstrate the discipline of showing the right amount of information at the right depth, with clear pathways for audiences to go deeper.
- **What disqualifies.** Hiding important information for engagement metrics; click-to-reveal patterns without underlying logic; documentation systems that confuse depth-of-access with depth-of-content.
- **Why it matters to MixHouse.** The website and Fumadocs portal both have public, investor, and internal surfaces. Progressive disclosure is the editorial discipline for surface-by-surface depth.
- **Example sources.** Stripe documentation, Linear product pages, Apple developer documentation, Notion product pages, Vercel documentation, Mozilla MDN reference depth, Criterion Channel film page depth, Wikipedia article-and-talk-page architecture.
- **Retrieval implications.** Feeds `08_website_strategy/page_briefs/` information architecture, future Fumadocs portal depth decisions, and investor-vs-public surface decisions. Surfaces in queries about "what should be public vs investor-only", "how do we layer the website".

#### Executive Persuasion

- **What qualifies.** Materials whose primary job is to convince a decision-maker (investor, commissioner, partner) at the level of strategic argument and visual seriousness. References that demonstrate persuasion through editorial restraint and structural argument rather than through pitch-deck volume.
- **What disqualifies.** High-volume slide decks; pitch decks with novelty visuals that distract from the argument; investor-letter formats with no visual discipline; PowerPoint stock-template aesthetics.
- **Why it matters to MixHouse.** Investor materials, broadcaster pitches, and sponsor decks (`11_outputs/`) carry the strategic argument. The visual register of these materials is itself part of the argument.
- **Example sources.** Berkshire Hathaway annual letter visual register, Stripe annual letter visual register, Apple investor-day decks, Netflix culture deck, prestige-investor-letter formats (Howard Marks memos, Bezos shareholder letters), boutique-bank deal-memo formats.
- **Retrieval implications.** Feeds `11_outputs/` investor-materials direction, broadcaster pitch design, and sponsor-deck structure. Surfaces in queries about "what should the investor deck look like", "what register convinces commissioners".

#### Emotional Escalation

- **What qualifies.** Visual and editorial systems that build emotional intensity across time: episode arcs, trailer architecture, multi-page editorial spreads, scroll-driven web experiences. References that demonstrate intentional pacing of emotional payload.
- **What disqualifies.** Surprise-and-shock pacing without structural underpinning; emotional manipulation without subject support; trailer cuts that exhaust emotional payload in the first ten seconds.
- **Why it matters to MixHouse.** The episode arc, the season arc, the trailer arc, and the finale all depend on emotional escalation discipline. Visual escalation references inform editorial pacing.
- **Example sources.** Apple TV+ trailer architecture, A24 trailer architecture, prestige-streamer season-finale grammar, Olympic ceremony pacing, concert-film escalation (`Stop Making Sense`, `Renaissance`), opening-sequence grammar (HBO prestige openers).
- **Retrieval implications.** Feeds episode anatomy, trailer language, and season-arc cinematography. Surfaces in queries about "how does the season escalate", "what trailer architecture do we follow".

#### Immersive Transitions

- **What qualifies.** Transition systems (between scenes, between pages, between contexts) that produce a sense of continuous world rather than discrete cuts. References that demonstrate transitions as editorial choice, not as technical demonstration.
- **What disqualifies.** Transition libraries used decoratively; transitions designed to hide loading time without editorial purpose; cinematic transitions in product UI where utility should dominate.
- **Why it matters to MixHouse.** The show transitions across residency, studio, Drop Night, and finale within a single episode. The web experience transitions across show, world, audience, and business-model surfaces. Both require deliberate transition grammar.
- **Example sources.** Apple Vision Pro environment transitions, Apple TV+ chapter transitions, theatrical-cinema chapter transitions (`Children of Men` long takes, `Birdman` continuous-camera grammar), high-end web transition systems (Active Theory work, Lusion work, Tendril work), prestige-game cinematic transitions.
- **Retrieval implications.** Feeds show-open and chapter-marker decisions, web-experience transition direction, and Drop-Night-to-residency-life transition grammar. Surfaces in queries about "how do we transition between surfaces", "what does a chapter break feel like".

#### Audio-Reactive Systems

- **What qualifies.** Visual systems that respond to audio input in editorially meaningful ways: live visual systems at venues, web visualisers tied to source audio, DSP visualisers (Spotify Canvas, Apple Music vertical video), generative-art systems with audio-reactive grammar.
- **What disqualifies.** Generic spectrum-analyser visualisers; equaliser-bar decoration; audio-reactivity as effect without editorial purpose; generative visuals that fight the music.
- **Why it matters to MixHouse.** Electronic music carries inherent audio-reactivity expectations. The format must engage with audio-reactive visual systems on its own editorial terms or risk visual generic-ness.
- **Example sources.** Cercle visual systems integrated with location, United Visual Artists installations, Daito Manabe / Rhizomatiks work, Active Theory audio-reactive web work, Spotify Canvas best-in-class examples, Apple Music vertical-video formats, generative-art venues (teamLab, Refik Anadol), Aphex Twin / Weirdcore live visuals, Squarepusher live visual systems.
- **Retrieval implications.** Feeds web-hero audio-reactive decisions, DSP visualiser direction, and live-venue visual integration. Surfaces in queries about "what audio-reactive references inform brand world", "what does our hero visualiser look like".

### Multi-Category Tagging

A single reference may legitimately carry multiple category tags. Bottega Veneta carries `luxury_restraint` and `editorial_systems`; Apple product pages carry `interaction_pacing`, `progressive_disclosure`, `premium_typography`, and `luxury_restraint`. The reference capture workflow in `10_source_material/reference_capture_workflow.md` documents multi-tagging conventions and tag-precedence rules for retrieval.

### Categories That Do Not Exist Yet

The taxonomy deliberately omits some categories that future work may require. Categories currently out of scope:

- Show-bible motion specs (deferred until post-pilot production model lands).
- Component-library reference set (deferred until website design partner engaged).
- Cast-portrait photography direction (covered under `artist_identity_systems` until cast-direction file exists).
- DSP partnership UI references (deferred until DSP partnership conversations open).

When a deferred category becomes active, add it here with a Change Log entry and a one-line justification.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Cinematic-storytelling category mapping to prestige unscripted references | `04_competitive_landscape/visual_reference_analysis.md`, `04_competitive_landscape/cinematography_language.md`, `04_competitive_landscape/prestige_unscripted_breakdown.md` | 2026-05-25 | A (internal anchor) |
| 2 | Premium-typography reference set | Type foundry catalogues (Klim, Pangram, Dinamo, MASS-Driver, Commercial Type) | 2026-05-25 | B |
| 3 | Editorial-systems reference set | Publication archives (The Gentlewoman, Apartamento, Resident Advisor, FT Weekend) | 2026-05-25 | B |
| 4 | Interaction-pacing reference set | Product marketing archives (Apple, Linear, Stripe, Vercel) | 2026-05-25 | B |
| 5 | Music-world authenticity reference set | Scene-press archives (RA, DJ Mag, Mixmag) and label visual identities | 2026-05-25 | B |
| 6 | Audio-reactive-systems reference set | Public installation and live-visual work (UVA, Rhizomatiks, teamLab, Refik Anadol) | 2026-05-25 | B |

Source registry with access status: `03_market_research/research_source_registry.md`.

## Objections Answered

| Objection | Response |
| --- | --- |
| "Fifteen categories is too many." | Each category has a distinct retrieval role. Collapsing them produces ambiguity at retrieval time. The taxonomy is the working vocabulary; pruning is a separate review pass with a Change Log entry. |
| "Some categories overlap." | Yes, deliberately. Multi-category tagging is supported. The taxonomy is not mutually exclusive; it is a controlled vocabulary for filtering retrieval queries. |
| "Why include `executive_persuasion` alongside cinematography categories?" | Because investor materials are part of the visual intelligence layer. Treating them as separate from brand visual decisions produces register drift. The same restraint discipline that governs the show governs the investor deck. |
| "This pre-empts the design partner's vocabulary." | No. The taxonomy is for retrieval and reference indexing, not for design-system naming. The design partner inherits the reference set and may introduce design-system vocabulary independently. |
| "Categories will date." | Yes. The taxonomy is reviewed quarterly alongside the reference set. Categories that no longer carry retrieval weight are deprecated with a Change Log entry. |

## Website Implications

- The taxonomy is internal-only; do not surface category names on public surfaces.
- Future Fumadocs portal uses category slugs as filter facets on the reference browser.
- `08_website_strategy/page_briefs/` may reference category names when justifying a reference set inheritance.
- `07_brand_world/moodboard_references.md` re-tags its existing reference rows against this taxonomy in a future review pass.

## Open Questions

- Which categories warrant a dedicated analysis file in `04_competitive_landscape/`, and which stay as reference clusters indexed only by the taxonomy? Recommended: dedicated files for `cinematic_storytelling`, `prestige_unscripted`, and `music_authenticity`; cluster-only for the remainder until depth is needed.
- Should `audio_reactive` references be physically separated in `10_source_material/references/` from static visual references? Recommended: yes, with a sub-folder when the set passes ten references.
- How are deferred categories surfaced to future agents working in the KB? Recommended: a "Deferred Categories" section in this file and a corresponding entry in `00_system/canonical_dependency_map.md`.
- Reconciliation with founder thesis: which categories will Sam want to add, remove, or rename when the founder thesis lands? Park as a reconciliation-pass agenda item.

## Change Log

- 2026-05-25, Initial reference taxonomy created as part of Phase 2.5 reference-ingestion layer. Fifteen categories defined with qualifying criteria, disqualifying criteria, MixHouse relevance, example sources, and retrieval implications. Multi-category tagging convention introduced. Generalises and extends the five reference classes in `visual_reference_analysis.md`.
