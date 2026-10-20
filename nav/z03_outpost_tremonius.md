# Nav -- Outpost Tremonius (z03_outpost_tremonius)

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28
**research_run:** P2 (deep-research cascade), ingested 2026-09-28; P3 (Zeta trigger, fast travel) ingested 2026-09-28

**Type:** main-story zone (interior leading to the surface)
**Linear?:** yes (with optional side chambers)
**Chapter:** 3. Outpost Tremonius (campaign section "Ringfall")

_source: deep-research cascade 2026-09-28 · capture: web_fetch · category: mainline unless noted · confidence per claim_

## Entry

From `z02_foundation` via edge `(z02_foundation, z03_outpost_tremonius)` -- see `architecture.md`. Arrival: you step out of the elevator. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]

## Exit

To `ow_lockdown` via edge `(z03_outpost_tremonius, ow_lockdown)` -- board the Pelican at the landing pad; you are dropped on an outcrop directly above FOB Golf. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
**Type:** story-gate
**Point of no return:** chapter-bound -- the interior half of the mission is replay-only afterward; the outpost area itself becomes the postgame spawn point (see `ow_postgame.md`).

## Outgoing edges

- `(z03_outpost_tremonius, ow_lockdown)` -- story-gate, board the Pelican at the landing pad
- `(TacMap, z03_outpost_tremonius)` -- conditional (Mission Replay), only after completion

## Entry tips (3 max)

1. The first of this mission's three Spartan Cores is the flashing green UNSC box directly in front of the elevator exit -- grab it before moving on. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language]
2. This mission holds three Spartan Cores, one Banished audio log and a Mjolnir locker (GamerGuides); the cores are mission-bound (Mission Replay recovers them). See `../sections/z03_outpost_tremonius.md`. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · category: easter-egg · confidence: medium]
3. The mission is over when you call the Pelican from the landing-pad terminal -- sweep the outpost before using that terminal. If you want Rapid Unscheduled Disassembly, destroy both Phantoms before they leave the outpost. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:official-pr]

## Sequential gates

1. **Elevator exit** -- step off the elevator; Spartan Core ahead in a flashing green UNSC box. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language]
2. **Storage tunnel** -- pass through a Banished storage-tunnel facility with sleeping Grunts. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language]
3. **Open Cylix** -- pass an open Cylix, a distinctive route landmark (what's unusual about it is a `story` beat -- see `../sections/z03_outpost_tremonius.md`). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-wiki]
4. **Terminal and surface door** -- the interior opens with a group of Grunts, then a terminal opens the door to the surface. **Zeta** fires as you step out of that door, when the overview cutscene ends -- not at mission end and not at the Pelican. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language · achievement: Zeta · achievement-hidden: no · trigger_type: progression] (the order of this terminal relative to the storage tunnel and open Cylix above is not pinned by the sources)
5. **Cliffside above the outpost** -- emerge above the outpost among crashed-frigate wreckage and clear the Banished garrison, including the two Phantoms (destroy both before they leave for **Rapid Unscheduled Disassembly**). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language · achievement: Rapid Unscheduled Disassembly · achievement-hidden: no · trigger_type: mastery]
6. **Hack the outpost** -- remove the outpost from the Banished network (the Weapon performs the hack). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-wiki · entity: the_weapon · entity-status: friendly]
   > see npcs/the_weapon.md for full summary
7. **Landing-pad terminal** -- reach the landing-pad terminal and call for pickup. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language · entity: echo_216 · entity-status: friendly]
   > see npcs/echo_216.md for full summary
8. **Board the Pelican** -- ride out; the Recovery overworld chain starts. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
   - `point_of_no_return:` chapter-bound

## Fast travel

Outpost Tremonius is a fast-travel destination once you have liberated it, but it is not a lettered FOB. To use fast travel at all you must capture at least one FOB first. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]

## Boss pointer

- **Tremonius** is not fought here -- he is the last encounter of Foundation (`z02_foundation.md` gate 6). This mission starts after the elevator ride that follows his death. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: high · Confirmed: 5 sources, 1 language · entity: tremonius · entity-status: hostile]
  > see npcs/tremonius.md for full summary

## Optional branches / shortcuts

- **Frigate-wreckage control switches** -- three red Banished control switches sit in the crashed-frigate wreckage (pointer only). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · Single source -- verify · class:community-wiki · category: easter-egg]
- **Hidden Forerunner chamber** -- in the cliffs north of the outpost, a hidden chamber holds a Heatwave. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · Single source -- verify · class:community-wiki · category: easter-egg]
  - Revisiting after a later mission, the same chamber holds a Game Zone arcade. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-wiki · category: easter-egg]

## Common confusions

- "Is this the open world yet?" -- not until the Pelican drop. The outpost clearing is part of an interior mission; the overworld begins at the outcrop above FOB Golf. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]

## Sources

- https://www.svg.com/931691/halo-infinite-how-to-unlock-fast-travel/ (EN; P3, fast travel)
- https://sirusgaming.com/halo-infinite-how-to-unlock-fast-travel/ (EN; P3)
- https://culturedvultures.com/halo-infinite-how-to-fast-travel/ (EN; P3)
- https://www.halopedia.org/Outpost_Tremonius (EN, accessed 2026-09-28)
- https://www.gamerguides.com/halo-infinite/guide/walkthrough/campaign-missions/outpost-tremonius (EN, n.d.)
- https://www.neoseeker.com/halo-infinite/walkthrough/Outpost_Tremonius (EN, 2021-12-17)
- https://games.atrivialmindatwork.com/aanews/wikis/halo-infinite/Outpost_Tremonius (IGN wiki mirror, EN, n.d.)
- https://guides.gamepressure.com/halo-infinite/guide.asp?ID=62154 (GamePressure Recovery, EN, 2022)

## Cross-system dependencies

> **Cross-system dependency** -- see `../dependencies.md` DEP-008: Fast travel needs at least one captured FOB; Outpost Tremonius is a node but not a FOB; it is off during Pelican Down and from Nexus. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` SEQ-002: Zeta fires at the surface door; destroy both Phantoms during the exterior clear before calling the Pelican. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]
