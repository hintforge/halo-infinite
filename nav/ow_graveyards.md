# Nav -- Graveyards / Pelican Down (ow_graveyards)

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-10-13
**research_run:** P2 (deep-research cascade), ingested 2026-09-28

**Type:** hub (overworld island -- sealed for the length of one mission)
**Linear?:** no (three AA guns in any order), then a fixed finale
**Chapter:** 8. Pelican Down arc (campaign section "Graveyards")

_source: deep-research cascade 2026-09-28 · capture: web_fetch · category: mainline unless noted · confidence per claim_

## Entry

From `z07_spire` via edge `(z07_spire, ow_graveyards)` -- see `architecture.md`. Arrival: you wake beside a downed Pelican in a ship-graveyard marsh. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]

## Exit

To `ow_reformation` via edge `(ow_graveyards, ow_reformation)` -- after the island's boss encounter, interact with the Pelican; a cutscene carries you to the Command Spire island. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
**Type:** story-gate
**Point of no return:** chapter-bound -- whether the island can be walked or flown back to after the credits is disputed (see Common confusions); Mission Replay covers it either way.

## Outgoing edges

- `(ow_graveyards, ow_reformation)` -- story-gate, board the Pelican after the boss encounter
- `(TacMap, ow_graveyards)` -- conditional (Mission Replay), only after Pelican Down is completed; the guaranteed route back to the island's 5 Spartan Cores (P3)
- **No fast-travel edge** -- you cannot fast travel off the island during Pelican Down, and the island has no FOBs.

## Entry tips (3 max)

1. **You're sealed in.** Pelican Down relocks Lockdown and Connections until it's complete, there are no FOBs here, and fast travel off the island doesn't work -- you have only the weapons you carry, enemy drops, and what you find. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
2. Open the map at the downed Pelican to orient -- the three AA guns can be done in any order, and each one you destroy stays destroyed even if you quit. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
3. The island holds five Spartan Cores plus audio logs and a Propaganda Tower -- sweep the wrecks northeast of the Pelican on your way. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]

## Sequential gates

1. **Downed Pelican** -- wake in the crashed Pelican among ship-graveyard wrecks; open the map to orient. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
2. **(Optional) Propaganda Tower and wrecks** -- a Propaganda Tower sits south of the Pelican; the destroyed ships northeast hold audio logs and a Spartan Core. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · category: easter-egg · confidence: medium · Single source -- verify · class:editorial-en]
3. **West AA gun** -- the Banished fortification under the western Gorespike: hack, expose and destroy the generator. (Your first gun destroyed, whichever it is, gives **One Down…**.) [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language · achievement: One Down… · achievement-hidden: no · trigger_type: progression]
4. **East AA gun** -- the eastern Gorespike: use the gravity-lift controls, then destroy the core. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language · achievement: One Down… · achievement-hidden: no · trigger_type: progression]
   - Detail (web research 2026-10-11, Samurai Gamers Pelican Down walkthrough): grapple to the overlook up the slope; grapple above the cave entrance for a UNSC audio log, then take the tunnel -- a Spartan Core is at its end; the gravity lift to the gun deck starts off, so enter the small cave just past the lift to switch it on; ride up, use the console to expose the core (cutscene), destroy the core, jump back down. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-guide · achievement: One Down…]
5. **North AA gun** -- the northern Gorespike. Gates 3-5 can be done in any order; destroying all three (P1: within a 20-minute window) gives **Gun Runner** (see `../sections/ow_graveyards.md`). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language · achievement: One Down… · achievement-hidden: no · trigger_type: progression]
   - North gun detail (same source): use the terminal on the right to start the lift, ride it up, take the gravity lift directly under the gun to the deck, use the console to expose the core, destroy it, jump down. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-guide]
   - West gun detail (same source): a Propaganda Tower sits by the lake near the start of the west route (the page does not describe its size); terminal on the right starts the lift; grapple up the cliff wall below the gun; ride the gravity lift up, use the terminal, destroy the core. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-guide]
6. **Head back toward the Pelican** -- after the guns, return toward the crash site. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
   - Boss pointer: **Tovarus and Hyperius** wait in the marshy ship graveyard beneath the guns; this is the only boss fight with no intro cutscene. Full strategy and the kill-order disagreement: `../npcs/tovarus_hyperius.md`. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: high · Confirmed: 3 sources, 1 language · entity: tovarus_hyperius · entity-status: hostile · achievement: Brothers Grim · achievement-hidden: yes · trigger_type: progression]
   > see npcs/tovarus_hyperius.md for full summary
   - Tactic: Hyperius fights from a Chopper. Leaving the arena resets the damage on the brothers but not the damage on the Chopper. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: medium · Single source -- verify · class:editorial-en (arena reset) · entity: tovarus_hyperius · entity-status: hostile]
   > see npcs/tovarus_hyperius.md for full summary
7. **Board the Pelican** -- interact with the Pelican; the cutscene carries you to the Command Spire island (`ow_reformation`). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
   - `point_of_no_return:` chapter-bound

## Optional branches / shortcuts

- **Island collectibles (P1):** 5 Spartan Cores, 1 locker, 3 Banished logs, 5 Spartan logs, 4 Propaganda Towers -- see `../sections/ow_graveyards.md`. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]

## Common confusions

- **"Go to one of your captured FOBs before the bosses"** (GamePressure) -- wrong for this island: it has no FOBs and no fast travel out. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Contradicted across sources -- see notes · conflicts: GamePressure Pelican Down walkthrough]
- **"FAST TRAVEL ONLINE" banner on the TacMap (seen in play 2026-10-11):** the TacMap corner can show "FAST TRAVEL ONLINE" on this island while no FOB marker is visible; the sources above say there is no fast travel off the island. Samurai Gamers' Pelican Down overview lists the mission's FOBs as "–" (none) and says nothing about fast travel; no source found says fast travel works here. Not resolved: the banner may mean something narrower than leaving the island. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: low · Single source -- verify · class:live-observation]
- **Boss-fight checkpoint:** during the marsh boss fight, retreating to the ship graveyard near the water forces a checkpoint; going too far away forces a reset (Samurai Gamers). [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: medium · Single source -- verify · class:editorial-en]
- **"Can I come back here later?"** -- [Contradicted across sources] (P3). Neoseeker, Gamerpillar and Halopedia treat the region as mission-only; Gamepressure, Digital Trends and a Microsoft statement relayed by Kotaku point to free roaming after the campaign, and the Winter Update removed an erroneous kill volume near the eastern AA gun. A Steam user reports flying a Banshee off the island toward Reformation after the mission; no first-hand postgame walk-in was found and two Steam users report kill barriers. Safe answer: Mission Replay of Pelican Down always works (TacMap -> Pelican Down -> Replay Mission); free-roam re-entry is likely but unverified. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Contradicted across sources -- see notes]
- **"Pelican Down" the achievement** unlocks at the *start* of this arc (P1) -- it is not the end-of-arc trigger. See `../sections/ow_graveyards.md`.

## Sources

- https://www.halopedia.org/Pelican_Down_(Halo_Infinite_level) (EN, accessed 2026-09-28)
- https://www.neoseeker.com/halo-infinite/walkthrough/Pelican_Down (EN)
- https://www.gamerguides.com/halo-infinite/guide/walkthrough/campaign-missions/pelican-down (EN)
- https://www.gamepressure.com/halo-infinite/pelican-down-walkthrough/z2f2ee (EN, 2022)
- https://samurai-gamers.com/halo-infinite/tovarus-and-hyperius-boss-guide/ (EN)
- https://guides.gamepressure.com/halo-infinite/guide.asp?ID=62139 (EN)
- https://steamcommunity.com/app/1240440/discussions/0/3195864334798010848/ (EN, forum)
- https://www.trueachievements.com/forum/viewthread.aspx?tid=1344523 (EN, forum -- AA-gun progress persists across quits)
- https://vandal.elespanol.com/guias/guia-halo-infinite-trucos-consejos-y-secretos/historia (ES "Pelican abatido", 2025-12-26)

## Cross-system dependencies

> **Cross-system dependency** -- see `../dependencies.md` PON-002: Finishing the Spire mission relocks Lockdown and Connections and disables fast travel until the island arc is complete. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` DEP-012: Mission Replay of Pelican Down is the guaranteed way to collect the island's five cores, part of the 45 the equipment achievements need. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` SEQ-004: Gun Runner's three AA guns must all fall within 20 minutes (stated by three sources). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

## Island ledger by item code

The codes (type letter plus number) and cells below are the ones in `../optional_zones/ow_graveyards_collectibles.md`; the grid is the A-H by 1-9 cells defined in `../optional_zones/spartan_cores_plot.md` (map-site coordinates; the in-game TacMap prints no grid). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium]

| Code | Cell | What |
|---|---|---|
| C30 | D7 | Spartan Core, just west of the west-gun elevator |
| C21 | D6 | Spartan Core, on top of the small hill |
| C22 | E6 | Spartan Core, Banished building ground floor |
| C23 | E6 | Spartan Core, wing of the crashed starship |
| C24 | E6 | Spartan Core, cave by the east gun |
| L21 | D7 | Warmaster's Prize Battle Rifle Coating (the island's one locker) |
| B20 | D7 | Banished log, table in the building south of the guns (Reformation 5/9) |
| B16 | E6 | Banished log, sloped building (Home 6/9) |
| B17 | E6 | Banished log, armory southwest of the east gun (Loyalties 7/9) |
| U17 | E6 | UNSC log, wrecked frigate, hydra room next door |
| U16 | D6 | UNSC log, mountain over the wreckage |
| W5 | D6 | S7 Flexfire Sniper, same spot as U16 |
| U18 | E6 | UNSC log, downed Pelican above the cave |
| U22, U23 | E7 | UNSC logs, frigate with the Warthog and wreckage base |
| T21 | D6 | Propaganda Tower, northwest |
| T23 | E6 | Propaganda Tower, east gun |
| T28 | D7 | Propaganda Tower, south edge |

Rows the map site lists on the island that are not in the table above: C20 (C6, far-west cliff pillar core), C31 (D7, core inside the starship wreckage), T22 (D6) and T26 (C7) towers, W6 (E6, Pursuit Hydra, tree island), W7 (F6, Volatile Skewer), L20 (D7, Infinity Armor Emblem) and F5 (C7, Artifact VI). The game counts 5 cores and 4 towers on the island against 7 and 5 on the map site, so some of those rows probably belong to a neighbouring zone. With the table rows, the island's in-game counters read cores 5/5, UNSC logs 5/5, Banished logs 3/3, locker 1/1, towers 4/4. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · model analysis -- 2026-10-13]

**Boss arena location (inference):** the map site's data puts the Pelican Down mission marker at about (-0.689, 0.510) and the Tovarus and Hyperius spawn points at about (-0.693, 0.507) and (-0.689, 0.505), the same spot as the island's middle objective marker, so the arena sits in grid E6 at the wrecked frigate (single third-party source). The boss guides place a rocket launcher and a Hydra in a room Tovarus enters; that is probably the frigate room next to the UNSC log U17 (inference, not confirmed). [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · confidence: medium · class:live-observation]

**Optional loose gear (single sources):** a Mongoose, a Warthog and UNSC weapons including an assault rifle have been reported near the east AA gun (E6); one guide puts a Mongoose by UNSC equipment near cliffs on the north gun route and an assault rifle beside a core on the west gun route; no source names a Warthog on this island. A cave beneath the east-gun area holds a rocket launcher behind two Hunters and a gravity hammer (reported from play 2026-10-13, grid E6 approximate). [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · confidence: low · Single source each -- verify · class:community-guide · sources: gamerguides.com/halo-infinite/guide/collectibles/campaign-missions/pelican-down-collectibles, the map site catalog `extract_tools/collectible_catalog.json`]


