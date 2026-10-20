# Sections -- Index

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28

Area/mission-by-mission notes (lore, boss fights, per-mission achievements, collectibles). For zone-graph structure and navigation, see `../nav/architecture.md` (and, from P2 onward, `../nav/<zone>.md`). Aggregation targets: [`missables.md`](missables.md), [`story_notes.md`](story_notes.md).

> **Design note (zipper, 2026-09-29):** each mission has a `sections/` file (what is in it: bosses, achievements, collectibles, story beats) and a `../nav/` file (the gate order through it). Boss and companion claims are also aggregated into `../npcs/`, story-tier claims into `story_notes.md`, and missable items into `missables.md`. Those overlaps are the entity/aggregation design, not redundancy to merge.

## Files in this folder

| File | Zone-id | Type |
|---|---|---|
| [`z01_warship_gbraakon.md`](z01_warship_gbraakon.md) | z01_warship_gbraakon | Mission |
| [`z02_foundation.md`](z02_foundation.md) | z02_foundation | Mission |
| [`z03_outpost_tremonius.md`](z03_outpost_tremonius.md) | z03_outpost_tremonius | Mission |
| [`ow_lockdown.md`](ow_lockdown.md) | ow_lockdown | Overworld region |
| [`z04_the_tower.md`](z04_the_tower.md) | z04_the_tower | Mission |
| [`z05_excavation_site.md`](z05_excavation_site.md) | z05_excavation_site | Mission |
| [`z06_conservatory.md`](z06_conservatory.md) | z06_conservatory | Mission |
| [`z07_spire.md`](z07_spire.md) | z07_spire | Mission |
| [`ow_graveyards.md`](ow_graveyards.md) | ow_graveyards | Overworld region |
| [`ow_reformation.md`](ow_reformation.md) | ow_reformation | Overworld region |
| [`z10_nexus.md`](z10_nexus.md) | z10_nexus | Mission |
| [`z11_command_spire.md`](z11_command_spire.md) | z11_command_spire | Mission |
| [`z12_repository.md`](z12_repository.md) | z12_repository | Mission |
| [`z13_the_road.md`](z13_the_road.md) | z13_the_road | Mission |
| [`z14_house_of_reckoning.md`](z14_house_of_reckoning.md) | z14_house_of_reckoning | Mission |
| [`z15_silent_auditorium.md`](z15_silent_auditorium.md) | z15_silent_auditorium | Mission |
| [`missables.md`](missables.md) | -- | Aggregation (cross-cutting) |
| [`story_notes.md`](story_notes.md) | -- | Aggregation (cross-cutting) |

`ow_postgame` and `ow_connections` have no dedicated section file -- their content is folded into the missions/regions that key off them (`ow_connections` context lives in `z04_the_tower.md` and `z05_excavation_site.md`; `ow_postgame` is documented in `../nav/architecture.md` only, since it has no unique story/boss content of its own).
