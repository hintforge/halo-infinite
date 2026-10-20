# Nav -- Connections overworld (ow_connections)

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-10-13
**research_run:** P2 (deep-research cascade), ingested 2026-09-28

**Type:** hub (overworld region)
**Linear?:** no (open region; its story chain z05 -> z06 -> z07 is linear)
**Chapter:** (overworld) Connections -> 5. Excavation Site, 6. Conservatory, 7. Spire (campaign section "Connections")

_source: deep-research cascade 2026-09-28 · capture: web_fetch · category: mainline unless noted · confidence per claim_

## Entry

From `ow_lockdown` via edge `(ow_lockdown, ow_connections)`, or on foot straight out of the Tower via `(z04_the_tower, ow_connections)` -- see `architecture.md`. The two landmasses are separated by a chasm; you cross on a drawbridge past a Banished blockade. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]

## Exit

To `ow_graveyards` via the Spire: `(ow_connections, z07_spire)` then `(z07_spire, ow_graveyards)`.
**Type:** story-gate
**Point of no return:** none permanent -- but finishing Spire starts Pelican Down, which relocks Lockdown and Connections until Pelican Down is complete (see `ow_graveyards.md`).

## Outgoing edges

- `(ow_connections, z05_excavation_site)` -- hub-spoke, story
- `(ow_connections, z07_spire)` -- hub-spoke, story (after Conservatory)
- `(ow_lockdown, ow_connections)` -- same edge, walked in reverse: the chasm bridge is two-way once open (relocked during Pelican Down)
- `(any FOB, any captured FOB)` -- fast-travel

## Entry tips (3 max)

1. The Excavation Site sits in the middle of FOBs Charlie, Bravo and Alpha -- capturing those three first gives you fast-travel points right around the next story objective. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:editorial-en]
2. This region's side content (FOBs Alpha-Echo, its four Banished outposts, HVTs) stays available; do it whenever -- but note Pelican Down will lock you out of this region for a while after the Spire. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]
3. The story order here is fixed: Excavation Site, then Conservatory, then Spire. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]

## Sequential gates

1. **Chasm drawbridge** -- cross the drawbridge over the chasm past the Banished blockade. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
   - `lock:` story -- The Tower complete (see `architecture.md` Locks and Keys)
2. **Head north to the Excavation Site** -- it sits between FOBs Charlie, Bravo and Alpha. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:editorial-en]
3. **(Optional) Capture FOBs Alpha, Bravo, Charlie, Delta, Echo** -- UNSC platforms (Alpha is northwest of the Excavation Site); each holds one "Infinity's Approach" audio log. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
4. **Story chain** -- complete `z05_excavation_site`, then `z06_conservatory`, then `z07_spire`, in that order. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
5. **After Spire** -- Echo 216 picks you up and the region transitions to Graveyards (the next mission is Pelican Down). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language · entity: echo_216 · entity-status: friendly]
   > see npcs/echo_216.md for full summary

## Optional branches / shortcuts

- **Banished outposts in this region:** Horn of Abolition, Redoubt of Sundering, Armory of Reckoning, and Forge of Teash (Halopedia lists Forge of Teash as the fourth; P1's outpost table already carried it). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high (P1 + P2 agree) · Single source (P2) -- verify · class:community-wiki]
- **Every collectible site in this region** -- `../optional_zones/ow_connections_collectibles.md` (MapGenie, 2026-10-06): each row carries its item code and grid cell (A-H by 1-9), and most items with map-site screenshots have an approach note at the end of that file. FOB and outpost cells: `../optional_zones/index.md` "Landmarks by grid cell". [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · _source: MapGenie 2026-10-06 · capture: web_fetch_]

## Common confusions

- **Armory of Reckoning** is a Banished outpost in this region -- not House of Reckoning (z14). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]
- "I can't get back to Lockdown / Connections" right after the Spire -- expected: Pelican Down relocks both regions until it's finished. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]

## Sources

- https://guides.gamepressure.com/halo-infinite/guide.asp?ID=62157 (EN)
- https://www.halopedia.org/HINF:Overworld (EN, accessed 2026-09-28)
- https://www.neoseeker.com/halo-infinite/walkthrough/Excavation_Site (EN, snippet)
- https://www.gamerguides.com/halo-infinite/guide/fobs-forward-operating-bases/fob-alpha/how-to-complete-fob-alpha (EN)
- https://www.digitaltrends.com/gaming/halo-infinite-audio-log-locations/ (EN)
- https://www.shacknews.com/article/128137/unsc-banished-spartan-audio-log-locations-halo-infinite (EN)
