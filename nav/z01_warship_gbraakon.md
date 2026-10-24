# Nav -- Warship Gbraakon (z01_warship_gbraakon)

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28
**research_run:** P2 (deep-research cascade), ingested 2026-09-28

**Type:** main-story zone (interior mission, Banished ship in space)
**Linear?:** yes
**Chapter:** 1. Warship Gbraakon (campaign section "Ringfall")

_source: deep-research cascade 2026-09-28 · capture: web_fetch · category: mainline unless noted · confidence per claim_

## Entry

New campaign start -- this is the graph's entry node (`architecture.md` Zone Graph). The player wakes aboard a Banished warship. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 2 languages]

## Exit

To `z02_foundation` via edge `(z01_warship_gbraakon, z02_foundation)`.
**Type:** story-gate
**Point of no return:** permanent (pre-replay) -- after this mission the warship can never be reached from the ring surface; missed collectibles come back only through Mission Replay. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language]

## Outgoing edges

- `(z01_warship_gbraakon, z02_foundation)` -- story-gate, finish the mission
- `(TacMap, z01_warship_gbraakon)` -- conditional (Mission Replay), only after completion -- see `architecture.md` Mission Replay row

## Entry tips (3 max)

1. This ship is a one-time visit: sweep it for its Skull and audio logs before leaving, or plan to come back through Mission Replay later. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high]
2. The Grappleshot is picked up early here and is the key to almost everything after -- including the Boom Skull perch on the freight lifts (see `../items/skulls.md`). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high]
3. For **Mix Things Up**, get a kill with every weapon and grenade type available on the ship (mission-scoped; Mission Replay can retry it). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · achievement: Mix Things Up · achievement-hidden: no · trigger_type: collection]

## Sequential gates

1. **Banished ship corridors** -- fight through the red-and-black Banished interior from the wake-up point. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 2 languages]
   - `point_of_no_return:` none
2. **Grappleshot pickup** -- take the first equipment piece, the Grappleshot, early in the mission. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 3 sources, 1 language]
   - `point_of_no_return:` none
3. **Stasis-beam hangar** -- reach the hangar-scale space where a Pelican is held in a tractor/stasis beam. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · Single source -- verify · class:editorial-non-en (Moyens I/O, es) · translated from: Spanish]
   - `point_of_no_return:` none
4. **Free the Pelican and leave** -- release the Pelican from the beam and escape the ship with it. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 2 languages] (who flies it is a `story` beat -- see `../sections/z01_warship_gbraakon.md`)
   - `point_of_no_return:` chapter-bound -- the ship is gone after this
5. **Mission end** -- the mission ends and Foundation begins (the ship's fate is a `story` beat -- see `../sections/z01_warship_gbraakon.md`). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-wiki]
   - `point_of_no_return:` permanent (pre-replay)

## Optional branches / shortcuts

- **Collectibles aboard:** two UNSC audio logs (one granted automatically by the story), one Banished audio log, and the Boom Skull (GamesRadar+, PC Gamer). Container detail: `../items/skulls.md`, `../items/collectibles.md`. Recoverable via Mission Replay. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · category: easter-egg · confidence: medium]

- **Where the Boom Skull room sits (web research 2026-10-24):** after the Grappleshot pickup (both guides below use the Grappleshot there) and once your objective is to reach the bridge: a long room with a floor above and three moving freight lifts on the right. GG Recon: go to the back of the room, before the slope on your left, grapple onto one of the blocks and ride it to the top. PC Gamer: grapple up through the gap in the ceiling, jump onto the middle lift, the Skull sits on a container to your right if you face the wall. No source gives a time or distance into the mission, and none places the room relative to the stasis-beam hangar. This guide has no room-by-room layout for the ship (gates only). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium (two guide articles agree on the room, differ on the exact step) · _source: WebFetch pcgamer.com/halo-infinite-skull-locations-guide + ggrecon.com 2026-10-24]
- **TacMap tallies in Mission Replay (observed 2026-10-24):** the mission panel reads skull 01/01 and logs 02/02 (one canister 00/01), while the "Area Collectibles" box beside it reads skull 01/02, logs 04/04 and canisters 02/03, so the area box counts more than this mission. The extra Skull is most likely Cowbell in Foundation (inference from the counts; the screen does not name it). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: low (inference) · _source: in-game TacMap 2026-10-24]
- **Banished log B2, Escharum's Testimony 1/9 (confirmed in play 2026-10-24):** on the bridge, to the right after you enter it, on the second level: a small orange-lit tablet standing on the floor against the wall beside a dark pillar, a rack of three Banished weapons just to its left and a low crate to its right. Guides disagree on its timing (Nightly Gaming Binge: on the bridge before the stasis-beam switch; Pro Game Guides: by a door during the escape); Halopedia's "top level of the bridge, next to the door you use to escape" matches the confirmed spot. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high (confirmed in play with a screenshot) · _source: player report and screenshot + halopedia.org/HINF:Audio_log 2026-10-24]

## Common confusions

- "I left something on the ship -- can I fly back?" -- No. After this mission the warship is unreachable from the ring; use Mission Replay from the TacMap (Winter Update 2022+). Anything you pick up in a replay saves to your current file. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language]

## Sources

- https://www.halopedia.org/Foundation_(Halo_Infinite) (EN, accessed 2026-09-28)
- https://es.moyens.net/gaming/guia-halo-infinite-desde-coleccionables-campana-hasta-consejos-multijugador-todo/ (ES, n.d.)
- https://vandal.elespanol.com/guias/guia-halo-infinite-trucos-consejos-y-secretos/historia (ES, 2025-12-26)
- https://www.theloadout.com/halo-infinite/gear-equipment-locations (EN, n.d.)
- https://support.halowaypoint.com/hc/en-us/articles/26608497528596-Equipment-in-Halo-Infinite (EN, official)
- https://kotaku.com/you-can-t-replay-campaign-missions-in-halo-infinite-1848169253 (EN, Dec 2021)
- https://support.halowaypoint.com/hc/en-us/articles/10581554050324-Halo-Infinite-Winter-Update-November-8-2022 (EN, 2022-11-10)

## Cross-system dependencies

> **Cross-system dependency** -- see `../dependencies.md` PON-003: Leaving Warship Gbraakon or Foundation makes their Skulls, logs and mission achievements reachable only through Mission Replay. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]
