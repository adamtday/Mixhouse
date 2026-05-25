---
doc_type: source
status: draft
confidentiality: internal
owners: [adamtday]
last_reviewed: 2026-05-25
retrieval_tags: [manual_capture, screenshots, working_guide, founder_action]
related:
  - 10_source_material/screenshots/manual_capture_checklist.md
  - 10_source_material/reference_capture_workflow.md
  - 10_source_material/screenshots/README.md
---

# Capture Packet for Adam

## What This Is

The working guide for your manual screenshot capture session against the twenty Phase 2.6 references. Keep this file open in one window while you capture in another. The exhaustive per-reference detail lives in `manual_capture_checklist.md`; this file is the field guide.

## What You Need Before Starting

- Desktop browser (Chrome, Safari, or Firefox).
- Hi-DPI display preferred (Retina or equivalent).
- A clean window: no extensions visible, no bookmarks bar (or hide it), no developer tools open.
- Filesystem access to `10_source_material/references/visual_references/{class}/` and `10_source_material/screenshots/`.

## Step-By-Step

1. **Open the URL** in your browser. Wait for the page to fully load including any hero video or animation cycle.
2. **Crop browser chrome before capture.** Capture the page content only, not the address bar or tabs. On Mac: `Cmd-Shift-4` for region select.
3. **Capture in reading order** (top to bottom). Frame 1 is the hero; subsequent frames are mid-page sections; last frame is the footer.
4. **For multi-frame sequences** (carousels, scroll-driven reveals, drawer interactions): capture the beginning, middle, and end of the interaction.
5. **Name the file** exactly as the companion `.md` specifies. The binary stem must match the companion stem; suffix `_p1`, `_p2`, etc. per frame.
6. **Save into the correct subfolder.** Each companion file lives in `10_source_material/references/visual_references/{class}/`; save the binary next to its companion `.md`.
7. **Verify the asset pair** by listing the folder: `companion.md` and `companion_p1.png` (etc.) should sit alongside each other.

## Naming Convention (Non-Negotiable)

Pattern: `YYYYMMDD_source_short_topic_p{n}.{ext}`

Examples:
- `20260525_apple_vision_pro_marketing_page_p1.png`
- `20260525_resident_advisor_homepage_p2.png`
- `20260525_cercle_homepage_p3.png`

Rules:
- Date prefix is `20260525` (matches the companion `.md` date; this is the analysis date, not necessarily the photographic-capture date).
- Source short topic must match the companion `.md` stem exactly.
- Multi-frame suffix is `_p1`, `_p2`, `_p3`, etc. in reading order.
- Extension is `.png` for hard-edged UI and editorial spreads; `.jpg` only when file-size constraint outweighs fidelity (rare); `.webp` if your tool defaults to it and the downstream supports it.

## What To Avoid

- **No aggregator captures.** Capture the original source, not Pinterest, We Heart It, or screenshots-of-screenshots.
- **No browser chrome in frame.** Crop or use region-select.
- **No downsampling.** Native resolution or higher; if your tool defaults to compressed output, override.
- **No bulk-capturing the whole page.** Capture the specific frames named in the per-reference brief.
- **No renaming after upload.** Get the filename right before saving.
- **No filename guessing.** If the expected filename is unclear, consult `manual_capture_checklist.md` first.
- **No AI-generated or stock-image substitution** when a capture is blocked. Mark the source blocked; do not fabricate.

## What Makes A Screenshot Useful

A useful capture demonstrates the mechanism, not just the existence of the page. For each frame, ask:

- Does this frame show the specific mechanism the companion `.md` Mechanism Analysis section names?
- Is the frame at the size and crop a future analyst would want?
- Does the frame include enough context (surrounding type, layout, footer or header) that the mechanism is legible without external reference?

For multi-frame sequences, ask:

- Do frames 1 through N tell the interaction's story start-to-finish?
- Is there a frame between frames where the mechanism still happens (a held state, a transition mid-state)?

## How To Mark Blocked Sources

If a source still cannot be captured manually (CDN block, login wall, paywall, geographic restriction):

1. Edit the companion `.md` file.
2. In the `## Screenshot Links` section, replace the expected filename with: `blocked: {reason}`. Example: `blocked: source requires Pitchfork login; founder capture from authenticated session deferred`.
3. Keep `screenshot_binaries_pending: true` in frontmatter.
4. Keep `analysis_pending: true` in frontmatter if the analysis depends on screenshot capture.
5. Note the block reason in a new Change Log entry on the companion file.
6. Do not commit fake or placeholder image files.

## How To Update Companion Reference Files After Screenshots Are Added

After successful capture:

1. Open the companion `.md` file (in `10_source_material/references/visual_references/{class}/`).
2. Verify the `## Screenshot Links` section lists the expected filenames; if so, you are done in this section (the filenames map to the captured binaries automatically because they share the path).
3. If you captured fewer or more frames than expected, update the `## Screenshot Links` section to reflect actual filenames.
4. Update the `attribution.date_captured:` field from `2026-05-25` (or `pending`) to the actual photographic-capture date if it differs.
5. Remove `screenshot_binaries_pending: true` from frontmatter (or change to `screenshot_binaries_pending: false`).
6. If the file was a P0 blocked source (Cercle Odyssey, Pitchfork): write the full analysis now, replacing the founder-capture-brief content. Remove `analysis_pending: true`. Change `status: seed` to `status: draft`.
7. Add a Change Log entry: `2026-MM-DD, Screenshots captured; companion file updated.`

## Compact Capture Table

Twenty references; capture priority and frame target only. Full detail in `manual_capture_checklist.md`.

| Pri | Reference | Frames | Class | Companion stem |
| --- | --- | --- | --- | --- |
| P0 | Cercle Odyssey | 4-6 | scene_credible_electronic | `20260525_cercle_odyssey_pending_capture` |
| P0 | Pitchfork | 4-6 | scene_credible_electronic | `20260525_pitchfork_pending_capture` |
| P1 | Apple Vision Pro | 4-5 | crossover_aesthetic | `20260525_apple_vision_pro_marketing_page` |
| P1 | Apple TV+ | 3-4 | crossover_aesthetic | `20260525_apple_tv_plus_marketing_page` |
| P1 | RA homepage | 3-5 | scene_credible_electronic | `20260525_resident_advisor_homepage` |
| P1 | Cercle homepage | 3-4 | scene_credible_electronic | `20260525_cercle_homepage` |
| P1 | F1 homepage | 4-5 | prestige_unscripted | `20260525_formula1_homepage` |
| P2 | Apple AirPods Max | 4-5 | crossover_aesthetic | `20260525_apple_airpods_max_marketing_page` |
| P2 | Apple MacBook Pro | 4-5 | crossover_aesthetic | `20260525_apple_macbook_pro_marketing_page` |
| P2 | RA Magazine | 3 | scene_credible_electronic | `20260525_ra_magazine` |
| P2 | RA Reviews | 3 | scene_credible_electronic | `20260525_ra_reviews` |
| P2 | RA Podcast | 3 | scene_credible_electronic | `20260525_ra_podcast` |
| P2 | Boiler Room | 3-4 | scene_credible_electronic | `20260525_boiler_room_homepage` |
| P2 | F1 Drivers | 3 | prestige_unscripted | `20260525_formula1_drivers_page` |
| P2 | Box to Box Films | 2-3 | prestige_unscripted | `20260525_box_to_box_films_homepage` |
| P2 | Teenage Engineering home | 3-4 | crossover_aesthetic | `20260525_teenage_engineering_homepage` |
| P3 | Teenage Engineering EP-133 | 4-5 | crossover_aesthetic | `20260525_teenage_engineering_ep133` |
| P3 | Cirque du Soleil home | 3 | crossover_aesthetic | `20260525_cirque_du_soleil_homepage` |
| P3 | Cirque du Soleil O | 3 | crossover_aesthetic | `20260525_cirque_du_soleil_o` |
| P4 | Netflix Tudum | 3-4 | crossover_aesthetic | `20260525_netflix_tudum_homepage` |

Required total: 16 references. Recommended / optional total: 4 references. Grand total: 20 references; 64 to 79 individual frames.

## Session Pacing Recommendation

- **Session 1 (45-60 min, P0 + P1).** Cercle Odyssey, Pitchfork, Apple Vision Pro, Apple TV+, RA homepage, Cercle homepage, F1 homepage. Seven references; roughly 25 to 35 frames. Minimum viable pass.
- **Session 2 (45-60 min, P2).** Apple AirPods Max, Apple MacBook Pro, RA Magazine, RA Reviews, RA Podcast, Boiler Room, F1 Drivers, Box to Box, Teenage Engineering home. Nine references; roughly 28 to 35 frames. Completes the cluster sets.
- **Session 3 (30 min, P3 + P4).** Teenage Engineering EP-133, Cirque homepage, Cirque O, Netflix Tudum. Four references; roughly 13 to 17 frames.

If your time is constrained, Session 1 is the strategic minimum. Sessions 2 and 3 can wait but each subsequent session compounds the curated reference set's value for design-partner conversations.

## After All Sessions Complete

1. Verify each `_p1.png` (etc.) sits next to its companion `.md` file.
2. For P0 sources (Cercle Odyssey, Pitchfork): write the analysis content in the companion `.md` to replace the founder-capture brief, then update frontmatter (`status: draft`, remove `analysis_pending`).
3. Re-run em-dash sweep on any companion files you edited.
4. Open a new branch and commit: `phase_2_8: founder visual capture pass complete`.
5. Open a draft PR linking to this packet and listing the captured count and any blocked sources.

## Quick Reference: Folder Paths

- crossover_aesthetic captures: `10_source_material/references/visual_references/crossover_aesthetic/`
- scene_credible_electronic captures: `10_source_material/references/visual_references/scene_credible_electronic/`
- prestige_unscripted captures: `10_source_material/references/visual_references/prestige_unscripted/`

## If Something Goes Wrong

- **Wrong filename.** Rename the binary to match the companion stem; do not commit the misnamed file.
- **Wrong folder.** Move the binary; do not duplicate.
- **Lost track of which frames belong to which reference.** Recapture the affected reference rather than guess; misattributed captures degrade the asset pair beyond repair.
- **Source's design changed since the analysis.** This is expected and useful. Note the visible change in the companion `.md` body, capture the current state, and add a Change Log entry noting the page change.
- **You disagree with the priority assignment.** Capture in the order that makes sense given your time; the priorities are recommendations grounded in cluster-analysis strategic value, not fixed requirements.

## Change Log

- 2026-05-25, Initial capture packet created as part of Phase 2.7 manual visual capture packet. Paired with `10_source_material/screenshots/manual_capture_checklist.md`. Provides the field-guide working format that complements the exhaustive checklist.
