# Nav -- Index

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28

Sequential gate lists per zone. The persona consults files in this folder first for nav-class questions ("where do I go?", "how do I get to X?", "I'm stuck at Y", "I just entered <zone>").

For position-finding when you're unsure where the player is, see [`localization.md`](localization.md). For the cross-zone structural backbone -- zone graph, edges, support topology, locks-and-keys -- see [`architecture.md`](architecture.md). For underlying puzzle mechanics, boss strategies, and per-zone hint ladders, see the relevant content folder (e.g. `puzzles/`, `<zones>/`). For per-region missables, see `sections/`. **This folder is routing only.**

## Files in this folder

| File | Type | Linear? | Status |
|---|---|---|---|
| [`architecture.md`](architecture.md) | zone graph, support topology, locks-and-keys | n/a | research-integrated |
| [`localization.md`](localization.md) | landmark -> zone resolution, ask-the-player prompts (hybrid class) | n/a | research-integrated |
| [`z01_warship_gbraakon.md`](z01_warship_gbraakon.md) | mission (interior) | yes | research-integrated |
| [`z02_foundation.md`](z02_foundation.md) | mission (interior) | yes | research-integrated |
| [`z03_outpost_tremonius.md`](z03_outpost_tremonius.md) | mission (interior to surface) | yes | research-integrated |
| [`ow_lockdown.md`](ow_lockdown.md) | overworld hub | no | research-integrated |
| [`z04_the_tower.md`](z04_the_tower.md) | mission (stronghold) | yes | research-integrated |
| [`ow_connections.md`](ow_connections.md) | overworld hub | no | research-integrated |
| [`z05_excavation_site.md`](z05_excavation_site.md) | mission (outdoor) | yes | research-integrated |
| [`z06_conservatory.md`](z06_conservatory.md) | mission (interior) | yes | research-integrated |
| [`z07_spire.md`](z07_spire.md) | mission | yes | research-integrated |
| [`ow_graveyards.md`](ow_graveyards.md) | overworld hub (sealed island) | no | research-integrated |
| [`ow_reformation.md`](ow_reformation.md) | overworld hub -- point-of-no-return warning | no | research-integrated |
| [`z10_nexus.md`](z10_nexus.md) | mission (interior) | yes | research-integrated |
| [`z11_command_spire.md`](z11_command_spire.md) | mission (interior) | yes | research-integrated |
| [`z12_repository.md`](z12_repository.md) | mission (interior) | yes | research-integrated |
| [`z13_the_road.md`](z13_the_road.md) | mission (linear exterior) | yes | research-integrated |
| [`z14_house_of_reckoning.md`](z14_house_of_reckoning.md) | mission (locked interior) | yes | research-integrated |
| [`z15_silent_auditorium.md`](z15_silent_auditorium.md) | mission (final) | yes | research-integrated |
| [`ow_postgame.md`](ow_postgame.md) | overworld hub (postgame) | no | research-integrated |

20 files: `architecture.md`, `localization.md`, and one gate-list file per zone-id (18; there is no z08/z09 -- Pelican Down is `ow_graveyards`, The Sequence is `ow_reformation`). Per-zone files created at P2 (2026-09-28).

## Routing rules (apply to ALL nav files in this folder)

### NEVER use left/right -- anchor to features

Left and right are perspective-dependent -- they depend on which way the player is currently facing, which the persona cannot see and the player may not be holding consistently.

**The rule:**
- The **zone entrance** (loading point, first save point, first chamber) is the canonical reference. State it explicitly when giving directions.
- Describe forks by what they *contain* or *lead to*, not by left/right. Examples:
  - ✅ "From the entrance chamber, the path with the **dead-end loot stash** is worth sweeping first; then take the path toward the **first puzzle room**."
  - ✅ "The corridor with the **<distinctive feature>** is the main path; the other is a side stash."
  - ✅ "From the entrance: the **lower path** / **upper path** / **path through the broken wall**." Vertical and feature-based language is fine.
  - ❌ "Go right." (whose right?)
  - ❌ "Take the left fork." (relative to what?)
- If a fork has no distinctive feature to name, ask the player to describe what they see and route from their description -- don't guess.
- Cardinal directions (N/S/E/W) are acceptable when the in-game map shows them; otherwise prefer feature anchors.

### Flag the game's save / checkpoint mechanism on zone entry

Most games name their save / checkpoint / hub mechanism something specific (`<SAVE_POINT_TERM>`). When the player enters a zone, the routing reply must include a one-liner naming the **first `<SAVE_POINT_TERM>` location** in feature-anchored terms (entrance break room, safe room past the first encounter, etc.). If a deeper `<SAVE_POINT_TERM>` exists per the guides, mention it too without spoiling its exact location until the player reaches that section.

Save / checkpoint locations are not spoilers -- withholding them is harmful, since players who don't know one exists will skip it and lose progress on death.

If a zone's `<SAVE_POINT_TERM>` placement isn't in the source guides, say so -- don't invent.

### Hint format on zone entry

When the player arrives at a zone and asks for help, **before any puzzle solutions**, give them **2-3 short navigation/anti-backtrack tips**. Goal: keep the player moving forward on a single path without missing key collectibles or chests, and without spoiling the puzzles themselves.

**Format rules:**
- Lead with the collectible/chest order if the zone has one (e.g. Bronze → Silver → Gold, or game-equivalent).
- Call out any "tempting shortcut that skips a collectible" -- alternate doors, bypass paths, etc. Tell the player *which* path forfeits *which* loot. Do not explain how to solve the puzzle, only what choice forfeits loot.
- Call out any "non-obvious correct exit" -- hidden doors, specific drops, center holes -- when missing it would force a long backtrack.
- Keep it to **3 numbered tips max**. Spoiler discipline: route hints, not solutions. The player will ask for hint-ladder solutions room by room as they hit them -- those live in the relevant content folder.

## Scaffold-file fallback

When the player asks about a zone whose nav file is still a scaffold (no gates yet), **web-search before asking a clarifying question**. Nav-class questions default search-first.

## Localization toolkit (landmark / hybrid games only)

For games where the persona must figure out player position from in-game landmarks (rather than a map system), keep a short reference at [`localization.md`](localization.md): which landmarks resolve to which zones, what to ask the player when CHECKPOINT's `player_position` confidence is below `high`. Skip for `map-system` and `none`-class games.
