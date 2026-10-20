# Halo Infinite -- Architecture

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-10-13
**research_run:** P1 (deep-research cascade), ingested 2026-09-28; P2 (navigation pass), ingested 2026-09-28; P3 (gap-fill + co-op), ingested 2026-09-28

Cross-zone structural primitives. The persona reads this file for all cross-zone reasoning -- lookahead warnings (Rule 2), backtrack queries (Rule 3), reachability checks (Rule 4), locks-and-keys notifications (Rule 5). Per-zone gate lists live in `nav/<zone>.md` (18 files, one per zone-id below, created at P2) and reference this file's graph by edge ID. Position-finding prompts live in `localization.md`. Drift between this file and per-zone files is a bug; run a consistency pass after each ingestion.

_source: deep-research cascade 2026-09-28 · capture: web_fetch · confidence: high unless noted per-row_

## Hintforge manifest

<!-- Read by the reader at session start (see docs/corpus-format.md §3). Bump corpus-core-version only when a change to docs/corpus-format.md would break an older reader; see the Versioning subsection in that doc. game-version-* fields describe the game build the corpus was authored against (player-supplied at setup; required as of v3); they are orthogonal to corpus-core-version (which is the schema axis). -->

```
corpus-core-version: 6
game-version: "latest patch (Steam build 22709428)"
game-version-platform: "PC / Steam"
game-version-as-of: 2026-09-27
vector-extensions: [nav, puzzles, npcs, optional_zones]
```

## Vector extensions

- `puzzles/` -- discrete puzzle files with hint ladders, indexed by `puzzles/index.md`
- `npcs/` -- named individual NPCs (any `entity-status`: hostile, friendly, convertible, party, neutral), indexed by `npcs/index.md`. At `corpus-core-version: 5` and later this replaces the legacy `enemies/` folder; hostility is a state via `entity-status: hostile`, not a class identity. Generic-mob combat content continues to route via the `enemy` vector to `mechanics.md` (no folder needed for that).
- `optional_zones/` -- side content keyed to parent zone IDs: Banished outposts, FOBs, HVT sites, propaganda towers, Spartan Core and armor-locker sites. P2 populated `optional_zones/index.md` with the per-region roster (FOBs, outposts); per-region collectible-site files `optional_zones/<zone>_collectibles.md` added from MapGenie map data (2026-10-06); outpost and HVT-arena walkthroughs are still not covered (only HVT and outpost rows in `../items/weapons.md` and `../achievements.md` carry that detail).

## Zone Graph

**Game-type label:** open-world-with-distinct-dungeons (P1 confirmed the Stage-0 prior) [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]
**Localization-mechanism class:** hybrid (P1 confirmed) -- the overworld TacMap (Tab / View) shows FOBs, outposts, HVTs and FOB-revealed collectibles; interior missions have no map and resolve by landmark + objective waypoint. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]
**Entry node:** z01_warship_gbraakon
**Hub nodes:** ow_lockdown, ow_connections, ow_graveyards, ow_reformation -- overworld regions that host FOB fast-travel points and hub-spoke access to their interior missions
**Source-language set:** English (dev); Spanish, Portuguese (BR), German, French community/editorial (P1 confirmed -- Vandal/3DJuegos/Eurogamer.es/BanWoh (es), GIGA/GamePro.de/Gameswelt (de), jeuxvideo.com/Xboxygen (fr), Critical Hits (pt-BR)) [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

**Nodes:**

| Zone-id | Canonical name | Kind |
|---|---|---|
| z01_warship_gbraakon | Warship Gbraakon | Interior, linear, space |
| z02_foundation | Foundation | Interior, linear |
| z03_outpost_tremonius | Outpost Tremonius | Interior leading to surface |
| ow_lockdown | Lockdown (Recovery overworld) | Overworld |
| z04_the_tower | The Tower | Interior + overworld exterior |
| ow_connections | Connections | Overworld |
| z05_excavation_site | Excavation Site | Overworld mission area |
| z06_conservatory | Conservatory | Interior |
| z07_spire | Spire | Interior (arena at base is exterior) |
| ow_graveyards | Graveyards (Pelican Down arc) | Overworld |
| ow_reformation | Reformation (The Sequence) | Overworld |
| z10_nexus | Nexus | Interior; point of no return |
| z11_command_spire | The Command Spire | Interior |
| z12_repository | Repository | Interior |
| z13_the_road | The Road | Linear exterior |
| z14_house_of_reckoning | House of Reckoning | Interior |
| z15_silent_auditorium | Silent Auditorium | Interior, final |
| ow_postgame | Zeta Halo (postgame) | Overworld -- whole ring reopens |

**Name disambiguation (P1):** "Spire" (z07) is not "The Command Spire" (z11), and neither is one of the ~40 Banished Propaganda Towers. "Pelican Down", "Reckoning" and "Spire Stalker" are achievement names, not the places. "Armory of Reckoning" is a Banished outpost in Connections, unrelated to House of Reckoning (z14). The Tower (z04) is a single Banished stronghold, not one of the Propaganda Towers. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · _source: deep-research cascade 2026-09-28 · capture: web_fetch · confidence: high] P2 adds a physical tell: the z07 Spire has a light bridge inside; The Command Spire has none (you grapple across) -- see `localization.md`. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high · Confirmed: 2 sources, 1 language]

**Edges:**

| From | To | Type | Direction | Condition | Point of no return | Notes | Tags |
|---|---|---|---|---|---|---|---|
| z01_warship_gbraakon | z02_foundation | story-gate | one-way | Finish mission 1 | permanent (pre-replay); cleared by Mission Replay | Cannot return to the warship from the ring | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0] |
| z02_foundation | z03_outpost_tremonius | story-gate | one-way | Finish mission 2: power seed, Weapon at the terminal, defeat Tremonius (Ascension), ride the elevator | permanent (pre-replay); cleared by Mission Replay | The Tremonius boss fight is the last encounter of Foundation; Outpost Tremonius begins at once after the elevator ride (P3) | [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · confidence: high · Confirmed: 5 sources, 1 language · entity: tremonius · entity-status: hostile · achievement: Ascension] |
| z03_outpost_tremonius | ow_lockdown | story-gate | one-way | Call the Pelican from the landing-pad terminal and board it (P2); dropped on an outcrop above FOB Golf | chapter-bound | First FOB capture follows. Zeta fires earlier in this mission, at the surface door (P3) | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · achievement: Zeta] |
| ow_lockdown | z04_the_tower | hub-spoke | two-way until mission end | Recovery chain | chapter-bound | The Tower's roof/exterior stays reachable later | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1] |
| z04_the_tower | ow_connections | story-gate | one-way unlock | Finish The Tower | none | On foot, north across the chasm drawbridge past a Banished blockade (P2 resolved P1's gating hypothesis: the gate is the chasm bridge, not the Tower's own security lockdown) | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language] |
| ow_lockdown | ow_connections | story-gate | two-way once open | The Tower complete | none | Same chasm bridge; relocked while Pelican Down is in progress | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language] |
| ow_connections | z05_excavation_site | hub-spoke | two-way | Story | none | Area stays in the open world afterward | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1] |
| z05_excavation_site | z06_conservatory | story-gate | one-way | Shut down the mining laser (Unearthed) | chapter-bound | Interior locks you in until done | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · achievement: Unearthed] |
| z06_conservatory | ow_connections | story-gate (return to hub) | one-way | Finish Conservatory | chapter-bound | Walk back out into the dig (P2; supersedes P1's direct z06 -> z07 edge) | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:editorial-en] |
| ow_connections | z07_spire | hub-spoke | one-way into the mission | Conservatory complete | chapter-bound | Spire is reached across Connections | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| z07_spire | ow_graveyards | story-gate | one-way | Finish Spire | chapter-bound | Pelican Down arc begins: Lockdown and Connections are relocked and fast travel is disabled until it's complete (no FOBs on the island) | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language] |
| ow_graveyards | ow_reformation | story-gate | one-way unlock | Pelican Down arc (AA guns, Hyperius/Tovarus) | none | After the boss pair, interact with the Pelican; a cutscene carries you to the Command Spire island (P2 resolved P1's trigger hypothesis). Fast travel returns once The Sequence begins. Whether the island can be walked or flown to postgame is [Contradicted across sources] (P3) -- Mission Replay of Pelican Down is the guaranteed way back | [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1] |
| ow_reformation | ow_lockdown | overworld travel | two-way | Pelican Down complete (The Sequence begun) | none | Pelican Down's relock lifts once it is complete; fast travel works again from the Spire-base terminal | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language] |
| ow_reformation | ow_connections | overworld travel | two-way | Pelican Down complete (The Sequence begun) | none | Same as above | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language] |
| ow_reformation | z10_nexus | story-gate | one-way | Four beacon data sets + the extended bridge, then enter the Command Spire door (Light the Way at the beacons) | **point-of-divergence**: open world closed until credits | "Once you start the mission Nexus, you will be on a one-way track" (Gamepur); remaining story takes ~3 hours | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · achievement: Light the Way] -- **warn the player before this edge, not after** |
| z10_nexus | z11_command_spire | story-gate | one-way | Story | chapter-bound | | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2] |
| z11_command_spire | z12_repository | story-gate | one-way | Story | chapter-bound | | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2] |
| z12_repository | z13_the_road | story-gate | one-way | Story | chapter-bound | | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2] |
| z13_the_road | z14_house_of_reckoning | story-gate | one-way | Story | chapter-bound | Bring Shiela Home Safely ends here | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · achievement: Bring Shiela Home Safely] |
| z14_house_of_reckoning | z15_silent_auditorium | story-gate | one-way | Story | chapter-bound | "No way back until you face the challenges" (GameInfinitus) | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2] |
| z15_silent_auditorium | ow_postgame | story-gate | one-way | Credits | none | All overworld content returns; you respawn at Outpost Tremonius | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2] |
| any FOB | any captured FOB | fast-travel | two-way | FOB captured | none | Fast-travelling while dead can cause an endless load (Halo Support known issue). Unavailable during Pelican Down and from Nexus until the credits (P2) | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0] |
| TacMap | any completed mission/objective | conditional (Mission Replay) | two-way | Winter Update 2022+, mission already completed | none | When the replay ends or you quit it, your save's current mission resumes at its latest checkpoint; unlocked equipment/upgrades carry over | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0] |
| TacMap (any open-world zone) | z01_warship_gbraakon | replay-teleport | one-way in; return by finishing or quitting | Winter Update installed; z01 completed on this save | none | At launch a Microsoft spokesperson said the first two missions (before you are on the ring) could not be replayed from the same save, only their leftover FOBs, targets and audio logs; the Winter Update notes then made main story missions replayable, and Mix Things Up is scored on the Banished ship (P3) | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 3 sources, 1 language] |
| TacMap (any open-world zone) | z02_foundation | replay-teleport | one-way in; return by finishing or quitting | Winter Update installed; z02 completed on this save | none | Needed for Stick Around (Skewer on Tremonius) once the first run is past (P3) | [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language] |
| TacMap | ow_graveyards (Pelican Down arena) | replay-teleport | one-way in | Pelican Down completed | none | The guaranteed route to the island's 5 Spartan Cores; whether you can walk or fly back freely is disputed (P3) | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| Co-op session start | Furthest point common to all members' saves | session-spawn | n/a | Every member picks a save slot | none | Does not create edges, but can put a player who is further ahead back into an earlier world state (P3) | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 3 sources, 1 language] |

**Lockout summary:** Every interior mission (z01, z02, z03, z06, z07, z10-z15) keeps you inside until completed. Nexus through Silent Auditorium (z10-z15) form one continuous locked chain -- once you enter Nexus, the overworld is closed until the credits roll. Separately, Pelican Down (ow_graveyards) temporarily relocks Lockdown and Connections and disables fast travel until it's complete (P2; progression-tier). No overworld content is permanently lost after the finale: full open-world access, including previously-missed audio logs and HVTs, returns once the story ends. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · _source: deep-research cascade 2026-09-28 · capture: web_fetch · confidence: high · Confirmed: 5 sources]

**How Mission Replay restores access (post-Winter-Update, current build):** Open the TacMap (Tab / View) -> place cursor on a completed mission or event -> Mission Options -> Replay Mission -> set difficulty and Skulls. Your equipped loadout (including late-game HVT variant weapons), unlocked equipment and upgrades carry into earlier missions, even ones set before that equipment is normally found. Anything collected during a replay (Skulls, audio logs) carries over to the current save permanently, and higher-difficulty replay completions count toward achievements. Because of this, **nothing in this corpus is treated as permanently missable** -- see `../sections/missables.md`. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · _source: deep-research cascade 2026-09-28 · capture: web_fetch · confidence: high · Confirmed: 5 sources]

### DLC

None. Halo Infinite shipped no paid campaign DLC. (TrueAchievements groups the 69 launch campaign achievements under a "Campaign DLC pack" label, but that is platform bookkeeping for the separately-sold campaign, not an expansion.) [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high]

**Post-launch campaign additions (P3):** the only one of substance is the Winter Update (Nov 8, 2022): network co-op, Mission Replay and 25 new achievements (24 announced plus Gatecrasher). No later update added campaign content; Season 3 (Mar 2023) and the May 2023 update carry only quality-of-life and sandbox changes, and the last major update planned (Operation: Infinite, Nov 2025) is multiplayer progression. Co-op adds no zones and no edges -- see `../mechanics.md` "Campaign co-op (P3)". Mission Replay's reopening of z01 and z02 is the only access change (edge table above). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 4 sources, 1 language]

## Chapter <-> Zone Mapping

_Mission/region context. Full gate lists: `nav/<zone-id>.md` (P2)._

| Chapter | Zones | Notes |
|---|---|---|
| 1. Warship Gbraakon | z01_warship_gbraakon | Opening mission. [spoiler: none] |
| 2. Foundation | z02_foundation | Ends with the first boss, Tremonius, then the elevator ride (P3). [spoiler: progression · entity: tremonius] |
| 3. Outpost Tremonius | z03_outpost_tremonius | Opens indoors, then the surface door (Zeta) and the outpost clear; ends with the Pelican drop that opens the overworld. Also the first fast-travel hub once liberated (not a lettered FOB). [spoiler: progression] |
| Recovery (overworld chain) | ow_lockdown | First FOB capture + first outpost + first HVT all available here immediately after Tremonius. [spoiler: progression] |
| 4. The Tower | z04_the_tower | Interior + reachable exterior/roof (stays reachable after the mission). Threat Sensor equipment picked up here. [spoiler: progression] |
| (overworld) Connections | ow_connections | Hosts Excavation Site's entrance, FOB Alpha, Redoubt of Sundering, Forge of Teash, Armory of Reckoning, Horn of Abolition. [spoiler: progression] |
| 5. Excavation Site | z05_excavation_site | Leads into Conservatory once the mining laser is shut down (Unearthed). [spoiler: progression] |
| 6. Conservatory | z06_conservatory | Drop Wall + Thruster equipment picked up here. [spoiler: progression · entity: despondent_pyre] |
| 7. Spire | z07_spire | Hunter pair at the base; mission boss Adjutant Resolution (entity file from P2 -- `../npcs/adjutant_resolution.md`). [spoiler: progression · entity: adjutant_resolution] |
| 8. Pelican Down arc | ow_graveyards | Sealed island: three Banished AA guns (any order); Hyperius/Tovarus boss pair; no FOBs, no fast travel out. [spoiler: progression] |
| 9. The Sequence | ow_reformation | Four beacons (East, South, North, West, any order) + extend the bridge; **last safe point to clear outposts/HVTs/FOBs before Nexus locks the world.** [spoiler: progression] |
| 10. Nexus | z10_nexus | **Point of divergence -- entering this mission closes the overworld until the credits.** [spoiler: late-game] |
| 11. The Command Spire | z11_command_spire | Mythic Skull; Stalker Rifle-focused mission (Spire Stalker achievement). [spoiler: late-game] |
| 12. Repository | z12_repository | Grunt Birthday Party power-seed puzzle -- see `../puzzles/`. [spoiler: late-game] |
| 13. The Road | z13_the_road | Escort the Scorpion "Shiela" to House of Reckoning. [spoiler: late-game] |
| 14. House of Reckoning | z14_house_of_reckoning | Jega 'Rdomnai and Escharum boss fights; Echo 216 present. [spoiler: story · entity: jega_rdomnai, escharum, echo_216] |
| 15. Silent Auditorium | z15_silent_auditorium | Final mission; Harbinger boss. Bandana Skull requires a no-damage Sentinel run. [spoiler: story · entity: harbinger] |
| Postgame | ow_postgame | Full ring reopens; catch up on anything, including previously-story-gated collectibles. [spoiler: late-game] |

> **Design note (zipper, 2026-09-29):** the co-op rows in Locks and Keys and the Optional Content counts summarize facts whose full statement lives in `../mechanics.md`, `../items/` and `../optional_zones/index.md`. This file is the cross-zone index by design; keep the rows short and point to the owner.

## Optional Content

_Source registry-level counts and access windows. Per-item detail (exact Skull locations, HVT locations/variants, achievement triggers) lives in `../items/`, `../npcs/`, and `../achievements.md`; this table is the cross-reference index._

| Name | Count | Unlock condition | Access window | Parent zones | Recommended chapter | Failure mode | Tags |
|---|---|---|---|---|---|---|---|
| FOBs | 12: Golf, Foxtrot (ow_lockdown); Alpha, Bravo, Charlie, Delta, Echo (ow_connections); Hotel, Juliet, Kilo, Lima, November (ow_reformation); none on ow_graveyards (P2) | Clear enemies, hack the central terminal | From ow_lockdown on; closed Nexus-to-credits, all return postgame | ow_lockdown, ow_connections, ow_reformation | Continuous | always-available (Mission Replay + postgame) | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1] |
| Banished outposts | 7: Ransom Keep (ow_lockdown); Redoubt of Sundering, Forge of Teash, Armory of Reckoning, Horn of Abolition (ow_connections); Riven Gate, Annex Ridge (ow_reformation) | Complete listed sub-objectives (open gates, destroy fuel silos, etc.) | Overworld; closed Nexus-to-credits, returns postgame | ow_lockdown, ow_connections, ow_reformation | Continuous | always-available | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1] |
| High Value Targets | 15 | Revealed by FOB capture or found directly | Overworld; closed Nexus-to-credits, returns postgame | All `ow_*` | Continuous | always-available | [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1] -- see `../npcs/index.md` "No entity files" note |
| Propaganda Towers | ~40 | Destroy the tower | Overworld; closed Nexus-to-credits, returns postgame | All `ow_*` | Continuous | always-available | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1] |
| UNSC distress calls (Marine rescues) | count unverified [unlock-chain incomplete] | Revealed by FOBs | Overworld | All `ow_*` | Continuous | always-available | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1] |
| Spartan Cores | 45 | UNSC crate; revealed by FOBs or proximity | Mostly overworld; 3 mission-bound in z03_outpost_tremonius (MapGenie shows 4 around the outpost, none marked mission-only -- contradicted, see `../items/upgrades.md`); per-site list in `../optional_zones/<zone>_collectibles.md` | Everywhere | Continuous | mission-bound trio recoverable via Mission Replay | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1] |
| Mjolnir Armor Lockers | 34 | Proximity / FOB reveal | Mostly overworld | Everywhere | Continuous | none -- multiplayer cosmetic reward only, no campaign effect | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1] |
| Audio logs | 104: 37 UNSC / 28 Banished / 39 Spartan (breakdown and the Halopedia disagreement: `../items/collectibles.md`) | Pickup | Some mission-bound | Everywhere | Continuous | missable pre-replay; Mission Replay recovers all | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high (total) · Confirmed: 3 sources, 1 language] |
| Forerunner Artifacts | 7 | Scan | Overworld | `ow_*` | Continuous | always-available | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1] |
| Skulls | 12 (5 mission-bound) | Pickup; some puzzle-gated | See `../items/skulls.md` | Mixed | Continuous | 5 mission-bound, all recoverable via Mission Replay | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1] |

_source: deep-research cascade 2026-09-28 · capture: web_fetch · confidence: high (FOB/outpost/HVT/tower/core counts); medium (audio-log counts -- contradicted across Gamerpillar vs. Halopedia)_

## Support Topology

_P1 baseline extended at P2 (2026-09-28). source: deep-research cascade 2026-09-28 · capture: web_fetch_

### Save stations / checkpoints

Halo Infinite's campaign has no manual save and no save-station objects -- it autosaves only. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 3 sources, 1 language]

| Behavior | Detail | Tags |
|---|---|---|
| "Saving checkpoint" vs "Saving progress" | A checkpoint is only a death-reload point; "Saving progress" is the save that survives quitting | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language (forum-class)] |
| Safe-state requirement | Checkpoints fire only when you're out of immediate danger with full shields | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language] |
| Open-world forced saves | Fast travel, collectible pickups, HVT kills and outpost clears trigger saves | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language] |
| Quit in the open world | You resume at a FOB with progress kept | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · Single source -- verify · class:forum] |
| Quit mid-interior | Often resumes at the mission start or the last major objective | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · Confirmed: 2 sources, 1 language (both forum-class)] |
| Pelican Down (ow_graveyards) | Each destroyed AA gun stays destroyed across quits | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:forum] |
| Tovarus/Hyperius fight | Retreat to the ship graveyard near the water to force a checkpoint; straying too far forces a reset | [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: medium · Single source -- verify · class:editorial-en] |

Mission Replay's per-mission checkpoint restore is covered below; it's not a save station.

### Fast-travel network

Two independent fast-travel mechanisms, both opened from the TacMap (Tab on keyboard, View on controller):
1. **FOB network** -- any captured FOB to any other captured FOB, two-way, no cost. Fast-travelling while dead can trigger an endless load screen (known Halo Support issue).
2. **Mission Replay** -- any completed mission or major objective (see below).

[spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high]

**FOB capture:** defeat the Banished and access the terminal. A capture reveals nearby Banished and UNSC activity; it does **not** reveal Spartan logs, Propaganda Towers or Forerunner Artifacts. Every FOB holds one "Infinity's Approach" UNSC audio log. Besides the 12 FOBs, **Outpost Tremonius** is a fast-travel node -- "the very first fast travel hub" once liberated -- but it is not a lettered FOB, and you must capture at least one FOB before fast travel works at all (P3; the FOB count stays 12). One editorial source (Cultured Vultures) also lists any completed outpost and completed main missions after The Tower as destinations; that wider list is uncorroborated. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high (FOBs, Outpost Tremonius) / medium (wider list, single source · class:editorial-en) · Confirmed: 3 sources, 1 language]

| FOB | Region (zone) | Location anchor | Notes | Tags |
|---|---|---|---|---|
| Golf | ow_lockdown | Below the Recovery drop-off outcrop | Story-required first FOB | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language · achievement: Reclaimer · achievement-hidden: no · trigger_type: collection] |
| Foxtrot | ow_lockdown | Lockdown region; audio log against a container on the landing pad | Optional | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| Alpha | ow_connections | Northwest of the Excavation Site | Grunts, Brutes, Jackals | [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| Bravo | ow_connections | Adjacent to the Excavation Site | Optional | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| Charlie | ow_connections | Adjacent to the Excavation Site | Optional | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| Delta | ow_connections | Connections | Optional | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| Echo | ow_connections | Connections; waterfall to its northwest | Optional | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| Hotel | ow_reformation | River to its northwest with a crashed ship | Optional | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| Juliet | ow_reformation | South of the map; near Riven Gate and the Myriad HVT | Optional | [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| Kilo | ow_reformation | Swamp to its north; hexagonal structures to its south | Optional | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| Lima | ow_reformation | Southeast of the map | Optional | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| November | ow_reformation | Far east; water to its south | Optional | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |

Grid cell (A-H by 1-9) for every FOB, outpost and Forerunner site: `../optional_zones/index.md` "Landmarks by grid cell"; item codes for every collectible: `../items/collectibles.md` "Item codes and map grid". [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · model analysis -- 2026-10-13]

**What each capture reveals** (map markers that appear once the FOB is yours). Neoseeker lists nothing for Juliet, Kilo, Hotel or November. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:editorial-en]

| FOB | Marine squads revealed | Banished outposts revealed |
|---|---|---|
| Golf | Boxer, Carrera, Starlight | Ransom Keep |
| Foxtrot | Cayman | -- |
| Echo | Courier, Bluebell, Pyramid, Indiana | Redoubt of Sundering |
| Delta | Pronto, Foxhound | -- |
| Charlie | Titan, Lancer, Harpoon | Forge of Teash |
| Alpha | Paladin, Barracuda, Cobra | Armory of Reckoning |
| Bravo | Thunder, Bengal, Jester | Horn of Abolition |
| Lima | -- | Riven Gate |

**High Value Targets revealed and FOB defenders:** ("revealed by" is not "located at": a capture marks targets in a radius, and several of these sit nearer a different FOB. For where to find each one, `../items/weapons.md` is authoritative.) Golf reveals Okro 'Vagaduun; Foxtrot, Briglard; Echo, Ik 'Novus; Charlie, Balkarus; Alpha, Inka 'Saham; Bravo, Thav 'Sebarim and Bipbap; Lima, Barroth. Heaviest defences: Delta has two cloaked sword Elites; Lima has a cloaked sword Elite Captain with Banshees overhead; Charlie, Bravo and November have Brute Captains or Brute Snipers. Alpha and Hotel have Ghosts nearby, and Bravo has one just west to use. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:editorial-en]

_source: Neoseeker FOB guide (sokkus, 2021-12-30), page text saved by hand 2026-09-28 · capture: saved by hand (blocked to automated fetching)_

Region split 2 / 5 / 0 / 5 (Lockdown / Connections / Graveyards / Reformation), per Neoseeker's FOB guide headings; 12 in total (Halopedia, GamesRadar). Capturing all 12 is Resurgency. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · achievement: Resurgency · achievement-hidden: no · trigger_type: collection]

**Fast travel is unavailable** during Pelican Down [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high] and from Nexus until the credits [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high].

### Mission Replay (Winter Update, November 8, 2022)

Open the TacMap, put the cursor on a completed mission or event, open Mission Options, choose Replay Mission, then pick difficulty and Skulls. Your currently equipped weapon loadout is used, and unlocked equipment and upgrades carry over even into missions set before you found them. When you finish or leave a replay early, your save's current mission resumes at its latest checkpoint, and unlocks such as Skulls and audio logs carry over to your save permanently. Main story missions and side objectives (outposts, HVTs, Marine events) can all be replayed. Prima Games and Steam users agree replay doesn't disturb current progress. Mission Replay did not exist at launch (Dec 2021; GamePro.de, Kotaku). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high (P1: 5 sources; P2 detail single official source + reprints, class:official-pr) · translated from: German (GamePro.de)]

The same Winter Update fixed "extended loading screens or being booted to the main menu" after fast travel and replays. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · Single source -- verify · class:official-pr]

### Hub access / returning to the overworld

The overworld regions (ow_lockdown, ow_connections, ow_graveyards, ow_reformation) are the hubs.

| Transition | Mechanism | Tags |
|---|---|---|
| z01, z02 | One-way into z03; never reachable from the ring again except by Mission Replay | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language] |
| z03 -> ow_lockdown | Board Echo 216's Pelican at the landing pad | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language · entity: echo_216 · entity-status: friendly] |
| z04 -> ow_connections | On foot after The Tower | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| z06 -> ow_connections | Walk out of the Conservatory into the dig | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:editorial-en] |
| z07 -> ow_graveyards | Scripted Pelican crash | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| ow_graveyards -> ow_reformation | Board the Pelican after the boss pair | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| z10 through z15 | Chained back to back; no return until the credits | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high · Confirmed: 2 sources, 1 language] |
| after the credits | Respawn at Outpost Tremonius (ow_postgame) | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high · Confirmed: 2 sources, 1 language] |

> see npcs/echo_216.md for full summary

## Locks and Keys

| Lock location | Key required | Key source | Visible before key? | Notes |
|---|---|---|---|---|
| z12_repository -- high window in the symmetrical gold-walled room (Grunt Birthday Party Skull) | Power Seed slotted into the back-right receptacle | Right-hand door off the console room (reached via hardlight bridge) in the same zone | yes (window visibly closed; seed puzzle is visible once you're in the room) | Guarded by 4 stealth Elites once through; see `../puzzles/` for the full hint ladder. P2 re-confirms. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · category: easter-egg · confidence: high] |
| Various HVT/Skull perches on hexagonal pillars (e.g. Fog, Thunderstorm Skulls; several HVTs) | Grappleshot rank-3 upgrade "Quick Shot" (40% shorter cooldown) | Spend a Spartan Core on Grappleshot rank 3, any time after Warship Gbraakon | yes (perches are visible; only the reliable access method is upgrade-gated) | Not a hard lock -- other traversal (vehicles, patience) can substitute, but guides converge on Quick Shot as the practical unlock. P2 re-confirms. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| ow_lockdown -- chasm bridge to Connections | Story: complete The Tower | z04_the_tower | yes (chasm and blockade visible) | The region lock -- not the Tower's own lockdown. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language] |
| z04_the_tower -- Tower lockdown | Story: reach the separate security building | z04_the_tower | yes | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| z05_excavation_site -- cave in the dig cliff / Conservatory entrance | Story: sabotage the mining laser | z05_excavation_site | yes (blocked by a giant machine) | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language · achievement: Unearthed · achievement-hidden: no · trigger_type: progression] |
| z06_conservatory -- crucible-room consoles | Power seeds (pointer) | z06_conservatory | yes | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language] |
| ow_graveyards -- island exit; Lockdown and Connections relocked; fast travel off | Story: finish Pelican Down | ow_graveyards | yes | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language] |
| ow_reformation -- the whole region (5 FOBs, Annex Ridge, Riven Gate) | Story: finish Pelican Down | ow_graveyards | partly (appears on the map later) | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] |
| ow_reformation -- Command Spire door | Story: all four beacon data sets | ow_reformation | yes (the base terminal fails) | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language · achievement: Light the Way · achievement-hidden: no · trigger_type: progression] |
| ow_reformation -- Command Spire bridge (retracted) | Bridge controls; or bypass with a Banshee/Wasp or fast travel | ow_reformation | yes | A bypass reportedly broke beacon triggers until the bridge was crossed. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:forum] |
| The entire overworld, Nexus to credits | Story: finish Silent Auditorium | z15_silent_auditorium | n/a | Point of no return. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high · Confirmed: 2 sources, 1 language] |
| z10_nexus -- crucibles and a UNSC weapon cache | Power seeds | z10_nexus | yes | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high · Confirmed: 2 sources, 1 language] |
| z11_command_spire -- floor seal | Power seed into the Crucible | z11_command_spire | yes | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium · Single source -- verify · class:community-wiki] |
| z11_command_spire -- chasm to the elevator platform | Grappleshot (hard key, but always owned) | z01_warship_gbraakon | yes | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high · Confirmed: 2 sources, 1 language] |
| z01 / z02 areas after completion | Mission Replay (post-Nov 2022) | TacMap | n/a | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language] |
| Cloaked boss Chak 'Lok (z04) | Threat Sensor -- practical, not a hard gate | z04_the_tower | n/a | [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language] |
| Cloaked boss Jega 'Rdomnai (z14) | Threat Sensor -- practical, not a hard gate | z04_the_tower | n/a | [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language · entity: jega_rdomnai · entity-status: hostile] |
| Drop Wall / Thruster pickups | Story progress | z06_conservatory (not z05) | n/a | The Loadout's "Excavation Site" placement is the losing side. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Contradicted across sources -- see notes (2 of 3 agree)] |
| Tremonius elevator (z02) -- the boss arrival | Power seed in the crucible, then the Weapon deployed at the terminal | z02_foundation | yes | The fight is the last encounter of Foundation (P3). [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language · entity: tremonius · entity-status: hostile] |
| Mission Replay for z01 / z02 | Winter Update (Nov 8, 2022) plus the mission completed on the save | z01, z02 | n/a | P3. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 3 sources, 1 language] |
| Co-op Area-Of-Operations tether | Stay within 1000 ft of a teammate (warning at 800 ft); past that you are killed and respawn on your nearest teammate | all open-world zones | n/a | P3. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 4 sources, 1 language] |
| Co-op collectible visibility | At least one member has not collected the item on their own save | all | n/a | P3. Official text; single source. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Single source -- verify · class:official-pr (ground truth per rubric)] |
| Co-op mission completion state | A mission counts as complete only if all members completed it | all | n/a | P3. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language] |
| Kill volume near the eastern AA Gun Battery | Removed in the Winter Update | ow_graveyards | n/a | P3. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Single source -- verify · class:official-pr] |

> see npcs/tremonius.md for full summary

> see npcs/jega_rdomnai.md for full summary

**Equipment is never a hard region gate** -- what's ahead is fixed by story keys (Grappleshot, Threat Sensor, Drop Wall, Thruster are practical keys only). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high]

_source: deep-research cascade 2026-09-28 (P1 rows 1-2; P2 rows 3+) · capture: web_fetch_

## Cross-system dependencies

> **Cross-system dependency** -- see `../dependencies.md` PON-001: Entering the Command Spire door closes the whole open world (and fast travel) until the credits -- clear overworld content first. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` PON-002: Finishing the Spire mission relocks Lockdown and Connections and disables fast travel until the island arc is complete. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` PON-003: Leaving Warship Gbraakon or Foundation makes their Skulls, logs and mission achievements reachable only through Mission Replay. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` DEP-002: Grappleshot rank 3 (Quick Shot) is the practical key to the Skull and HVT perches on hexagonal pillars. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` DEP-004: Co-op progress is the intersection of members' saves, which shapes collectible sharing and the fresh-save plan for the completionist achievements. [spoiler: none · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` DEP-008: Fast travel needs at least one captured FOB; Outpost Tremonius is a node but not a FOB; it is off during Pelican Down and from Nexus. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` DEP-009: Mission Replay carries loadout, equipment and upgrades into any completed mission, making timed and per-mission achievements replay plans. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

> **Cross-system dependency** -- see `../dependencies.md` DEP-014: The co-op timing achievements at the dig and outposts are closed from Nexus until the credits; plan them before Nexus, postgame or by Replay. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` SEQ-001: Stick Around must use the Skewer found earlier in Foundation; after Foundation only Mission Replay works. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0]
