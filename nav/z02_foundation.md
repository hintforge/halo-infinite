# Nav -- Foundation (z02_foundation)

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28
**research_run:** P2 (deep-research cascade), ingested 2026-09-28; P3 (Tremonius placement) ingested 2026-09-28

**Type:** main-story zone (interior mission, first Forerunner interior)
**Linear?:** yes
**Chapter:** 2. Foundation (campaign section "Ringfall")

_source: deep-research cascade 2026-09-28 · capture: web_fetch · category: mainline unless noted · confidence per claim_

## Entry

From `z01_warship_gbraakon` via edge `(z01_warship_gbraakon, z02_foundation)` -- see `architecture.md`. The mission opens beneath the ring's surface. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high]

## Exit

To `z03_outpost_tremonius` via edge `(z02_foundation, z03_outpost_tremonius)`.
**Type:** story-gate
**Point of no return:** permanent (pre-replay) -- like z01, Foundation cannot be reached from the ring surface after completion; Mission Replay only. Outpost Tremonius starts the moment this mission ends (no overworld break in between). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]

## Outgoing edges

- `(z02_foundation, z03_outpost_tremonius)` -- story-gate, automatic on mission end
- `(TacMap, z02_foundation)` -- conditional (Mission Replay), only after completion

## Entry tips (3 max)

1. Another one-time interior: the Cowbell Skull and this mission's audio logs are only here (or via Mission Replay later) -- see `../items/skulls.md`. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]
2. The Shield Core equipment is on a dead Spartan in this mission -- interact with the body; don't run past it. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language]
3. The mission ends with the Tremonius boss fight and then the elevator ride; the next mission begins immediately -- there's no chance to wander back. Keep the Skewer from earlier in the mission if you want **Stick Around**, and finish sweeping first. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]

## Sequential gates

1. **Forerunner structure** -- enter the ancient Forerunner architecture beneath the surface. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 2 languages]
   - `point_of_no_return:` none
2. **Find the AI** -- the mission objective is to locate an AI inside the structure (Vandal: "buscamos una IA que nos ayude"). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:editorial-non-en · translated from: Spanish · entity: the_weapon · entity-status: friendly · achievement: Together. Again? · achievement-hidden: yes · trigger_type: progression]
   > see npcs/the_weapon.md for full summary
3. **Shield Core** -- take the Shield Core from a dead Spartan's body. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language]
   - `lock:` none -- this is a key pickup, see `architecture.md` Locks and Keys
4. **Hologram sequence** -- a ship-AI hologram plays (a scripted scene, not a gate you solve). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-wiki] (the hologram's content is a `story` beat -- see `../sections/z02_foundation.md`)
5. **Power seed and terminal** -- place a power seed in the crucible to restore power to the elevator, then deploy the Weapon at the terminal. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language · entity: the_weapon · entity-status: friendly]
   > see npcs/the_weapon.md for full summary
6. **Tremonius boss fight** -- the elevator descends carrying Tremonius and two Major Jackals with orange (hardened) shields; kill him for **Ascension**. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: high · Confirmed: 5 sources, 1 language · entity: tremonius · entity-status: hostile · achievement: Ascension · achievement-hidden: no · trigger_type: progression]
   > see npcs/tremonius.md for full summary
7. **Elevator exit** -- ride the elevator to the surface; that ends this mission and Outpost Tremonius begins at once. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
   - `point_of_no_return:` permanent (pre-replay)

## Boss pointer

- **Tremonius** -- fought at the end of this mission (gate 6), not in Outpost Tremonius. Strategy: break his energy shield with a Pulse Carbine or overcharged Plasma Pistol, then kinetic to the head; the shield regenerates fully if you stop damaging him. For **Stick Around**, fire the Skewer only once the shield is down. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: high · Confirmed: 5 sources, 1 language · entity: tremonius · entity-status: hostile · achievement: Ascension, Stick Around · achievement-hidden: no · trigger_type: progression]
  > see npcs/tremonius.md for full summary

## Optional branches / shortcuts

- **Cowbell Skull** -- grapple-reached, after the Weapon pickup; container detail in `../items/skulls.md`. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]

## Common confusions

- "Where's the open world?" -- not yet. Foundation and Outpost Tremonius are both interior missions; the ring surface opens only after Outpost Tremonius (edge `(z03_outpost_tremonius, ow_lockdown)`). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]

## Sources

- https://www.pcgamesn.com/halo-infinite/bosses-guide-list (EN, Dec 2021; P3, Tremonius placement)
- https://www.gamerguides.com/halo-infinite/guide/bosses/main-story/how-to-defeat-tremonius (EN, 2021; P3)
- https://samurai-gamers.com/halo-infinite/tremonius-boss-guide/ (EN, 2021; P3)
- https://screenrant.com/halo-infinite-tremonius-boss-fight-disruptor-plasma-strategies/ (EN, 2021; P3)
- https://www.windowscentral.com/halo-infinite-boss-guide (EN, Dec 11, 2021; P3)
- https://www.halopedia.org/Foundation_(Halo_Infinite) (EN, accessed 2026-09-28)
- https://vandal.elespanol.com/guias/guia-halo-infinite-trucos-consejos-y-secretos/historia (ES "Cimientos", 2025-12-26)
- https://www.gamerguides.com/halo-infinite/guide/walkthrough/campaign-missions/outpost-tremonius (EN, n.d.)
- https://www.theloadout.com/halo-infinite/gear-equipment-locations (EN, n.d.)
- https://games.atrivialmindatwork.com/aanews/wikis/halo-infinite/Outpost_Tremonius (IGN wiki mirror, EN, n.d.)

## Cross-system dependencies

> **Cross-system dependency** -- see `../dependencies.md` PON-003: Leaving Warship Gbraakon or Foundation makes their Skulls, logs and mission achievements reachable only through Mission Replay. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` SEQ-001: Stick Around must use the Skewer found earlier in Foundation; after Foundation only Mission Replay works. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0]
