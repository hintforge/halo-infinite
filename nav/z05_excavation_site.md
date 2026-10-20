# Nav -- Excavation Site (z05_excavation_site)

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28
**research_run:** P2 (deep-research cascade), ingested 2026-09-28

**Type:** main-story zone (outdoor Banished dig inside the Connections overworld)
**Linear?:** yes
**Chapter:** 5. Excavation Site (campaign section "Connections")

_source: deep-research cascade 2026-09-28 · capture: web_fetch · category: mainline unless noted · confidence per claim_

## Entry

From `ow_connections` via edge `(ow_connections, z05_excavation_site)` -- see `architecture.md`. The mission begins right after The Tower. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]

## Exit

To `z06_conservatory` via edge `(z05_excavation_site, z06_conservatory)` -- through the cave the mining laser was boring into.
**Type:** story-gate
**Point of no return:** chapter-bound -- entering the Conservatory keeps you inside until it's finished. The dig area itself stays part of the open world afterward.

## Outgoing edges

- `(z05_excavation_site, z06_conservatory)` -- story-gate, after the mining laser is sabotaged
- (back into `ow_connections` -- the dig is outdoors within the region)

## Entry tips (3 max)

1. The mining laser is the mission's centerpiece and its lock: it's what's blocking the cave you need to enter next. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]
2. Drop Wall and Thruster are **not** here despite one guide (The Loadout) saying so -- they're in the Conservatory next door. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Contradicted across sources -- see notes]
3. **Workplace Safety Violation** asks for a kill with the mining laser -- keep it in mind while the laser is still running (P1; see `../sections/z05_excavation_site.md`). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · achievement: Workplace Safety Violation · achievement-hidden: no · trigger_type: discovery]

## Sequential gates

1. **Start point** -- the mission starts from the room with the Spartan, after The Tower (GamePressure). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:editorial-en]
2. **Dig site with cooling towers** -- reach the Banished dig site; its cooling towers are the target of the co-op achievement **You, Me, Same Page** (destroy all cooling towers at the Dig Site within 60 seconds of each other). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:official-pr · achievement: You, Me, Same Page · achievement-hidden: no · trigger_type: mastery]
3. **Mining laser** -- deal with the Banished mining laser boring into the cliff wall. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language · achievement: Unearthed · achievement-hidden: no · trigger_type: progression]
   - Boss pointer: the named Banished boss **Bassus** (a Brute Chieftain with a Gravity Hammer) is tied to this encounter; name confirmed at P3 by four sources. Full strategy: `../npcs/bassus.md`. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: high · Confirmed: 4 sources, 1 language · entity: bassus · entity-status: hostile]
   > see npcs/bassus.md for full summary
4. **Laser sabotaged, cave opens** -- sabotaging the drill opens the cave it was boring into (earlier blocked by a giant machine). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language · achievement: Unearthed · achievement-hidden: no · trigger_type: progression]
   - `lock:` story -- mining laser (see `architecture.md` Locks and Keys)
5. **Mission end** -- the Conservatory entrance is available from the dig, highlighted by an AI Scan. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
   - `point_of_no_return:` chapter-bound (next step enters an interior)

## Optional branches / shortcuts

- none documented at P2 beyond the collectible counts in `../sections/z05_excavation_site.md`.

## Common confusions

- "Where do I get Drop Wall / Thruster?" -- The Loadout lists both under Excavation Site; GamerGuides and GamePressure put both on dead Spartans inside the Conservatory. The corpus follows the Conservatory placement. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Contradicted across sources -- see notes]
- "I can't find the way in" -- after the laser, use AI Scan: it highlights the Conservatory entrance in the cliff. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]

## Sources

- https://www.gamepressure.com/halo-infinite/conservatory/z0f2ce (EN, 2022)
- https://guides.gamepressure.com/halo-infinite/guide.asp?ID=62157 (EN, 2022)
- https://www.gamerguides.com/halo-infinite/guide/walkthrough/campaign-missions/conservatory (EN)
- https://selphie1999gaming.com/game-guides/halo-infinite-mission-conservatory-walkthrough-guide/ (EN)
- https://support.halowaypoint.com/hc/en-us/articles/10581554050324-Halo-Infinite-Winter-Update-November-8-2022 (EN, 2022-11-10)
- https://samurai-gamers.com/halo-infinite/mission-6-conservatory-wakthrough/ (EN; boss list naming Bassus)
- https://www.theloadout.com/halo-infinite/gear-equipment-locations (EN)
- https://www.halopedia.org/Excavation_Site (EN)
