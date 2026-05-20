---
doc_type: brief
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [fan_participation, audience, format_engine, franchise]
related:
  - 02_show_bible/elimination_logic.md
  - 02_show_bible/format_engine.md
  - 05_business_model/platform_extensions.md
  - 08_website_strategy/component_requirements.md
---

# Fan Participation

## Purpose

Define the channels through which audiences interact with MixHouse outside the linear/streamer cut — and the rules governing how that participation influences the show without breaking format integrity.

## Key Takeaways

- Fan participation drives discovery and discussion, not direct elimination votes.
- Three official channels: streaming behaviour, short-form engagement, and the official MixHouse app/site experience.
- Every channel is designed to compound the music-release strategy.
- Anti-brigading defaults are baked in. No phone-vote drama, no "save my favourite" coercion.

## Core Content

### The Three Official Channels

| Channel | What fans do | How it affects the show |
| --- | --- | --- |
| **Streaming** | Listen, save, add to playlists across DSPs. | Feeds the streaming input of the `Audience Index`. |
| **Short-form** | Watch, share, and remix in-show clips on TikTok/Reels. | Feeds the short-form virality input. |
| **App / Site** | Follow contestants, build personal playlists, attend `Drop Night` virtual viewings, RSVP to alumni events. | Drives CRM, ticketing, and ongoing engagement — outside elimination math. |

### Why No Direct Vote

A direct phone/SMS vote would:
- Be brigaded.
- Reward audience reach, not music.
- Strip judges of credibility.
- Tilt the show toward `American Idol` mechanics it deliberately leaves behind.

Streaming and short-form act as participation proxies that are harder to manipulate and align fan behaviour with the music-release economy.

### Anti-Brigading Defaults

- Streaming inputs are normalised against cohort medians, blunting coordinated boosts.
- Short-form is filtered for qualifying engagement (watch-through, sound use, save) over raw views.
- Anomaly detection triggers an audit window for any single contestant exceeding a 3x cohort standard deviation.

### The App / Site Experience

The MixHouse app/site (post-pilot) gives fans:

- Watch + listen in one place.
- Contestant follow + push notifications for releases / `Drop Nights`.
- Curated weekly playlists of all released tracks.
- Virtual `Drop Night` viewing for non-attendees.
- Alumni tour ticket-priority for early adopters.
- Lightweight ranking/polls that surface fan favourites — for visibility, not voting.

This is the surface where the franchise compounds beyond the season. See `05_business_model/platform_extensions.md`.

### Talent-Side Participation

Contestants themselves participate in the fan loop:

- Real social handles, real release announcements, real DJ bookings.
- No simulated / production-controlled accounts.
- Production provides editorial support but does not ghostwrite or run accounts.

### Press and Scene Press

Scene press (Resident Advisor, DJ Mag, Mixmag, etc.) is treated as fan-participation amplification, not a separate funnel. Coverage cadence is owned by `06_production_strategy/music_release_pipeline.md`.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Eurovision split-vote brigading patterns | Public reporting (BBC, AP) | — | B (target) |
| 2 | Short-form virality as a leading indicator of streaming uplift | MIDiA / Chartmetric data | — | B (target) |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Fans want to vote." | Fans want their favourites to win. The streaming + short-form proxy lets them help in the way that actually compounds the music — which is the show's product. |
| "No vote means no engagement spike." | The release cadence + virtual `Drop Night` + alumni tour priority gives multiple engagement spikes per week. |

## Website Implications

- Live site needs a `Follow contestant` + `Save to playlist` flow per profile.
- "How fans participate" component on `the_show.md` lists the three channels.
- Newsletter capture flows feed the franchise CRM (see `05_business_model/platform_extensions.md`).

## Open Questions

- App vs website-first product strategy — owner: `08_website_strategy/site_objectives.md`.
- Whether virtual `Drop Night` is free or paid (or tiered).
- DSP partner relationships and exclusivity windows.

## Change Log

- 2026-05-20 — Initial fan-participation framework drafted.
