# Nav -- Conservatory (z06_conservatory)

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28
**research_run:** P2 (deep-research cascade), ingested 2026-09-28

**Type:** main-story zone (Forerunner interior, separate load)
**Linear?:** yes (one hatch-drop detour that returns to the central terminal)
**Chapter:** 6. Conservatory (campaign section "Connections")

_source: deep-research cascade 2026-09-28 · capture: web_fetch · category: mainline unless noted · confidence per claim_

## Entry

From `z05_excavation_site` via edge `(z05_excavation_site, z06_conservatory)` -- see `architecture.md`. Arrival: through the hole the mining laser bored, along a passage to a Forerunner structure; an elevator panel there loads a separate location. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]

## Exit

To `ow_connections` via edge `(z06_conservatory, ow_connections)` -- you walk back out into the dig, then continue across Connections to the Spire via `(ow_connections, z07_spire)`. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:editorial-en]
**Type:** story-gate (return to hub)
**Point of no return:** chapter-bound -- once inside, you stay until the mission is done; anything inside is recoverable afterward only through Mission Replay (P1 found no collectibles in this mission).

## Outgoing edges

- `(z06_conservatory, ow_connections)` -- story-gate, return to the hub on completion
- `(TacMap, z06_conservatory)` -- conditional (Mission Replay), only after completion

## Entry tips (3 max)

1. Two equipment pieces are here, each on a dead Spartan: Drop Wall comes first (right after the opening terminal), Thruster later (after the hatch-drop section). Don't skip either body. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language · achievement: Grab Some Cover, Evasive Maneuvers · achievement-hidden: no, no · trigger_type: progression, progression]
2. The crucible rooms look almost identical -- if it feels like you're looping, follow the objective marker and watch the power-seed count, not the room shape. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:editorial-en]
3. **Conservation of Momentum** wants the whole mission done in under 15 minutes -- a speed run on a replay is the easy way. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:official-pr · achievement: Conservation of Momentum · achievement-hidden: no · trigger_type: mastery]

## Sequential gates

1. **Elevator panel** -- through the laser-bored hole, follow the passage to the Forerunner structure and use the elevator panel (a new location loads). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
2. **Terminal -> Drop Wall** -- interact with the terminal; the doors open; the first dead Spartan gives Drop Wall. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
3. **Crucible rooms** -- descend the ramps into the large, near-identical U-shaped crucible rooms with overhead bridges; activate consoles with power seeds (pointer only -- not solved here). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
   - `lock:` power seeds (see `architecture.md` Locks and Keys)
4. **Central room** -- a room with three hallways and a terminal; a cutscene plays at a window looking into the main chamber. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language · entity: despondent_pyre · entity-status: friendly] (who appears there, and what happens, is a `story` beat -- see `../sections/z06_conservatory.md`)
   > see npcs/despondent_pyre.md for full summary
5. **Hatch drop** -- through the door on the far side of the central room, use the hatch console and drop to the lower level. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
   - Cloaked golden-armored Elites wait on the lower level. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language]
6. **Back to the terminal -> Thruster** -- return to the central terminal, continue, and take Thruster from the second dead Spartan. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
7. **Bottom of the central chamber** -- reach the chamber floor; a scripted scene plays, then the objective becomes finding a way out (the scene's content is a `story` beat -- see `../sections/z06_conservatory.md`). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-wiki]
   - Skimmers attack here. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: medium · Single source -- verify · class:community-wiki]
   - `point_of_no_return:` chapter-bound

## Optional branches / shortcuts

- none -- P1 found no collectibles in this mission.

## Common confusions

- "Am I going in circles?" -- the crucible rooms are "almost identical" (Neoseeker). Follow the objective marker and the power-seed count. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:editorial-en]
- "The Loadout says Drop Wall/Thruster are in the Excavation Site" -- they're here, per GamerGuides and GamePressure. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Contradicted across sources -- see notes]

## Sources

- https://www.halopedia.org/Conservatory (EN, accessed 2026-09-28)
- https://www.gamepressure.com/halo-infinite/conservatory/z0f2ce (EN, 2022)
- https://www.gamerguides.com/halo-infinite/guide/walkthrough/campaign-missions/conservatory (EN)
- https://www.neoseeker.com/halo-infinite/walkthrough/Conservatory (EN)
- https://vandal.elespanol.com/guias/guia-halo-infinite-trucos-consejos-y-secretos/historia (ES "Invernadero", 2025-12-26)
- https://www.techradar.com/news/halo-infinite-campaign-missions-arent-replayable-but-its-being-worked-on (EN)
- https://support.halowaypoint.com/hc/en-us/articles/10581554050324-Halo-Infinite-Winter-Update-November-8-2022 (EN, 2022-11-10)
