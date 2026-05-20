---
doc_type: brief
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-20
retrieval_tags: [elimination_logic, format_engine, judging, audience_index]
related:
  - 02_show_bible/format_engine.md
  - 02_show_bible/judging_framework.md
  - 02_show_bible/fan_participation.md
---

# Elimination Logic

## Purpose

Specify exactly how a contestant is eliminated each week — the inputs, the weighting, the safeguards, and how the mechanic is filmed.

## Key Takeaways

- Eliminations are decided by a composite `Audience Index` with four inputs: judges, live crowd, streams, short-form.
- The composite is transparent: each input is shown numerically on-screen at reveal.
- No twist eliminations. Mechanics are stable across the season.
- Safeguards exist for unfair circumstances (technical failure, illness, partner recusal).
- The fan-participation channel never overrides the index but can shift one input's data.

## Core Content

### Inputs to the `Audience Index`

| Input | Source | Available by | Initial weight |
| --- | --- | --- | --- |
| **Resident Judge Score** | Filmed panel debate after `Drop Night` | Same evening | 40% |
| **`Drop Night` Crowd Reaction** | Audience-reaction sensors (applause + dance-floor density + dedicated reaction zones) | Real-time | 20% |
| **Streaming Performance** | DSP first-72-hour streams normalised per release window | Day 3 | 25% |
| **Short-Form Virality** | TikTok/Reels velocity + qualifying engagement | Day 3 | 15% |

Weights to be calibrated in pilot. Total always sums to 100.

### The Algorithm

```
For each contestant in the active cohort:
  judge_score      = panel_average / 10            # normalised 0-1
  crowd_score      = crowd_sensor_avg / max        # normalised 0-1
  streaming_score  = streams_72h / cohort_max      # normalised 0-1
  shortform_score  = velocity_index / cohort_max   # normalised 0-1

  audience_index =
      0.40 * judge_score
    + 0.20 * crowd_score
    + 0.25 * streaming_score
    + 0.15 * shortform_score

The lowest audience_index in the cohort is eliminated.
Ties broken by judge_score, then by streaming_score.
```

The math is deliberately legible on screen — viewers must be able to follow it.

### Reveal Mechanic

- The reveal is the cold, designed Act 5 (`02_show_bible/episode_anatomy.md`).
- Each input is revealed one at a time on the venue's screens.
- The eliminated contestant is named only after all four bars are shown.
- No live audience boos. Reveal energy is reverent, not gladiatorial.

### Safeguards

| Scenario | Safeguard |
| --- | --- |
| Technical failure during `Drop Night` | The contestant's crowd score is excluded; weight redistributed proportionally across remaining inputs. |
| Illness / withdrawal | Contestant is paused, not eliminated. Returns at producer discretion within 1 episode. |
| Conflict-of-interest recusal | A "Floating Judge" replaces the recused score. |
| Suspected manipulated streaming numbers | Audit window of 24h; if anomalies confirmed, that contestant's streaming score is excluded for the week. |

### Variance and Volatility

- Composite design ensures no single input can dominate.
- Streaming compounds: contestants with strong early tracks accumulate baseline streams that survive a weak `Drop Night`.
- Late-season variance is deliberately higher; finalists must perform across all four dimensions.

### What This Mechanic Avoids

- Hidden judges' votes.
- Surprise immunity twists.
- Algorithmically opaque "the producers chose" reveals.
- Crowd boos / audience-shaming framing.

### Fan Participation Interaction

Fan participation (`02_show_bible/fan_participation.md`) does not directly enter the Index. Instead, official fan polls and curated playlists *influence* the short-form input organically — they don't get a separate vote.

## Evidence / Sources

| # | Claim | Source | Date accessed | Reliability |
| - | --- | --- | --- | --- |
| 1 | Composite-index precedent in reality formats | `Eurovision` jury+televote split as a reference | — | B |
| 2 | Audience-reaction sensor technology | To populate from venue tech partners | — | B (target) |

## Objections Answered

| Objection | Response |
| --- | --- |
| "Streaming windows favour early releases — unfair." | Normalised per release window. Late-week tracks aren't penalised for shorter exposure. |
| "Algorithmic eliminations are cold." | They're filmed warm — reverent, ceremonial, with full context. The math is honest; the moment is human. |
| "Crowd manipulation risk." | Sensors are not show-of-hands. Manipulation requires coordinated physical movement, not online brigading. |

## Website Implications

- "How elimination works" component on `the_show.md` shows the four inputs visually.
- Press kit explains the algorithm — investors and journalists love this kind of transparency.

## Open Questions

- Final weighting balance (pilot calibration).
- Whether short-form virality should be from a single platform or aggregated.
- Public visibility of running index between episodes (yes, with delay, vs no).

## Change Log

- 2026-05-20 — Initial composite-index logic drafted.
