# Nav -- Reformation overworld / The Sequence (ow_reformation)

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-10-13
**research_run:** P2 (deep-research cascade), ingested 2026-09-28

**Type:** hub (overworld region)
**Linear?:** no (four beacons in any order), then a fixed finale
**Chapter:** 9. The Sequence (campaign section "Reformation")

_source: deep-research cascade 2026-09-28 · capture: web_fetch · category: mainline unless noted · confidence per claim_

## Entry

From `ow_graveyards` via edge `(ow_graveyards, ow_reformation)` -- see `architecture.md`. Arrival: the Pelican cutscene sets you down at the base of the Command Spire in the southeast corner of the map; the bridge west off the island is retracted. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]

## Exit

Into the Command Spire via edge `(ow_reformation, z10_nexus)` -- cross the extended bridge, use the panel, enter.
**Type:** story-gate
**Point of no return:** point-of-divergence. **Entering the Command Spire closes the open world until the credits -- finish side content first.** Nothing is permanently lost (postgame reopens everything), but outposts, HVTs, FOBs and overworld collectibles wait until after the ending. Warn the player before this edge, not after. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
- Halopedia: "Upon entering the Command Spire to start the mission Nexus, players pass through the campaign's point of no return." [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high · Confirmed: 2 sources, 1 language]
- No overworld content is permanently lost, because postgame reopens it (P1). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high]

## Outgoing edges

- `(ow_reformation, z10_nexus)` -- story-gate, one-way until the credits (point-of-divergence) [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2]
- `(ow_reformation, ow_lockdown)`, `(ow_reformation, ow_connections)` -- the relock from Pelican Down ends once The Sequence begins; travel between regions works again
- `(any FOB, any captured FOB)` -- fast-travel works again from the moment the island's Spire-base terminal fails (gate 2)

## Entry tips (3 max)

1. **This is the last stop before the point of no return.** Clear any outposts, HVTs, FOBs and collectibles you want before entering the Command Spire -- after that, the open world is closed until the credits. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
2. Fast travel works again here (after the first terminal fails), and Lockdown and Connections are open again. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
3. There are **four** beacons (East, South, North, West), visitable in any order -- ignore the one guide line that says three. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]

## Sequential gates

1. **Command Spire island** -- arrive at the base of the Command Spire in the southeast; the bridge west is retracted. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
2. **Spire-base terminal fails** -- clear the island; the terminal at the Spire's base doesn't open it; fast travel works again from here. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
   - `lock:` Command Spire door -- needs data from all four beacons (see `architecture.md` Locks and Keys)
3. **Four beacons** -- visit the East, South, North and West beacons (tall Forerunner towers with interiors) in any order and collect each one's sequence data. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language · achievement: Light the Way · achievement-hidden: no · trigger_type: progression]
4. **(Optional) Reformation FOBs and outposts** -- capture FOBs Hotel, Juliet, Kilo, Lima and November; outposts Annex Ridge and Riven Gate. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
5. **Extend the bridge** -- return to the Spire, kill the refortified Banished, find the bridge controls and extend the bridge. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
   - `lock:` retracted bridge -- bridge controls (or a flying bypass; see Optional branches)
6. **Enter the Command Spire -- POINT OF NO RETURN** -- cross, use the panel, and enter. Entering closes the open world until the credits. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
   - `point_of_no_return:` point-of-divergence
   - Nexus begins. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high · Confirmed: 3 sources, 1 language · achievement: What Will It Take? · achievement-hidden: yes · trigger_type: progression]

## Optional branches / shortcuts

- **Retaliation 05 audio log** -- near FOB Lima during The Sequence (Shacknews). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · category: easter-egg · confidence: medium]
- **Archaeological Findings audio logs** -- The Sequence has four of them (Halopedia); P1 counts 4 Banished logs here. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · category: easter-egg · confidence: medium]
- **Black Eye Skull (P3)** -- in the southern part of the region, a small cave behind a tall waterfall (pool at the top, wrecked vehicle in front, opening on the right about halfway up); grapple to the rock shelf and crouch through. Not tied to a mission, so it is collectable now or postgame. Full detail: `../items/skulls.md`. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · category: easter-egg · confidence: high · Confirmed: 4 sources, 1 language]
- **Bridge bypass** -- Halopedia says you can skip extending the bridge by flying a Banshee or Wasp across, or by fast travel. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-wiki]
- **Every collectible site in this region** -- `../optional_zones/ow_reformation_collectibles.md` (MapGenie, 2026-10-06): each row carries its item code and grid cell (A-H by 1-9; the Black Eye Skull is K11 in F8), and most items with map-site screenshots have an approach note at the end of that file. FOB and outpost cells: `../optional_zones/index.md` "Landmarks by grid cell". [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · _source: MapGenie 2026-10-06 · capture: web_fetch_]

## Common confusions

- **"Three beacons or four?"** -- one Neoseeker line says "three Beacons" while the same guide names four. Four is correct. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Contradicted across sources -- see notes · conflicts: Neoseeker The Sequence snippet]
- **Beacons won't trigger after a flying shortcut:** a Steam user reports that skipping ahead by Banshee broke the beacon triggers until they crossed the bridge. If beacons aren't registering, cross the bridge normally. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:forum]
- **Beacon towers vs. other Forerunner pylons:** Forerunner towers repeat across the ring; only these four are objective-marked during The Sequence. See `localization.md`. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]

## Sources

- https://www.halopedia.org/The_Sequence (EN, accessed 2026-09-28)
- https://www.halopedia.org/HINF:Overworld (EN, accessed 2026-09-28)
- https://www.neoseeker.com/halo-infinite/walkthrough/The_Sequence (EN)
- https://www.gamepressure.com/halo-infinite/the-sequence/z8f39f (EN, 2022-01-10)
- https://www.gamerguides.com/halo-infinite/guide/walkthrough/campaign-missions/the-sequence (EN)
- https://www.halopedia.org/Command_Spire_(location) (EN)
- https://steamcommunity.com/app/1240440/discussions/0/3833170517026704885 (EN, forum)
- https://www.neoseeker.com/halo-infinite/walkthrough/Forward_Operating_Bases (EN)
- https://www.shacknews.com/article/128137/unsc-banished-spartan-audio-log-locations-halo-infinite (EN)
- https://vandal.elespanol.com/guias/guia-halo-infinite-trucos-consejos-y-secretos/historia (ES "La secuencia", 2025-12-26)

## Cross-system dependencies

> **Cross-system dependency** -- see `../dependencies.md` PON-001: Entering the Command Spire door closes the whole open world (and fast travel) until the credits -- clear overworld content first. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` DEP-010: The Black Eye Skull needs Pelican Down done and the Grappleshot, is not mission-bound, and counts toward Catacomb and Headmaster. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]
