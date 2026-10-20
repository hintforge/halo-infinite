# Optional zones -- Index

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-10-13
**research_run:** P2 (deep-research cascade), ingested 2026-09-28; P3 reviewed 2026-09-28 (no per-site data); MapGenie map-data gap-fill ingested 2026-10-06 (per-region collectible sites)

Side content keyed to parent zone IDs in `../nav/architecture.md`. P2 supplies a per-region **roster** (which FOBs and outposts sit in which overworld zone). **Collectible sites per region** (every core, Skull, locker, log, artifact, tower, unique weapon and HVT marker, grouped by nearest FOB/outpost) are in the four `<zone>_collectibles.md` files below (MapGenie, 2026-10-06). Outpost objectives and HVT arena walkthroughs are still not covered. HVT locations and variant weapons live in `../items/weapons.md`; Skull sites in `../items/skulls.md`.

_source: deep-research cascade 2026-09-28 · capture: web_fetch_

## Roster by parent zone

| Parent zone | FOBs (fast-travel nodes) | Banished outposts | Tags |
|---|---|---|---|
| `ow_lockdown` | Golf (story-required first FOB, below the drop-off outcrop), Foxtrot | Ransom Keep | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high] |
| `ow_connections` | Alpha (northwest of the Excavation Site), Bravo, Charlie, Delta, Echo (waterfall to its northwest) | Horn of Abolition, Redoubt of Sundering, Armory of Reckoning, Forge of Teash | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high] |
| `ow_graveyards` | none -- no FOBs on the island | none recorded | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high] |
| `ow_reformation` | Hotel, Juliet, Kilo, Lima, November | Annex Ridge, Riven Gate | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high] |
| `ow_postgame` | all 12 reachable again | all 7 reachable again | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high] |

Location anchors for every FOB: `../nav/architecture.md` "Fast-travel network". Every FOB holds one "Infinity's Approach" UNSC audio log. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 3 sources, 1 language]

> **Design note (zipper, 2026-09-29):** this roster (which FOB and outpost sits in which region) and `../nav/architecture.md`'s Fast-travel and Optional Content tables list some of the same names on purpose: this file answers "what is in region X", the architecture tables answer "where exactly is it and what does it need". Not a duplicate to merge.

## Landmarks by grid cell

Where every FOB, Banished facility and Forerunner facility the map site marks sits on the A-H by 1-9 grid (defined in `spartan_cores_plot.md`; the in-game TacMap prints no grid). Use it to turn "what is near FOB Lima" into a cell and then into the item rows with that cell in the region files. Within each kind the rows run in map reading order (north to south, then west to east). The three "Gun Battery" rows are the island's AA guns; the data does not say which is which. Added 2026-10-13 from the map site's landmark data (positions in MapGenie's coordinates, pulled 2026-10-06); positions are map-site coordinates, medium confidence. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · _source: MapGenie interactive map 2026-10-06 · capture: web_fetch_]

| Landmark | Kind | Cell | Tags |
|---|---|---|---|
| FOB Alpha | FOB | B3 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| FOB Charlie | FOB | C4 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| FOB Bravo | FOB | C4 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| FOB Echo | FOB | B5 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| FOB Delta | FOB | D5 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| FOB Foxtrot | FOB | B7 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| FOB Golf | FOB | B7 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| FOB November | FOB | H7 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| FOB Hotel | FOB | D8 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| FOB Juliet | FOB | E8 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| FOB Kilo | FOB | E8 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| FOB Lima | FOB | H8 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Outpost Tremonius | Banished facility | A2 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Armory of Reckoning | Banished facility | B3 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Excavation Site | Banished facility | C4 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Horn of Abolition | Banished facility | D4 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Forge of Teash | Banished facility | B5 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| The Tower | Banished facility | A6 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Redoubt of Sundering | Banished facility | B6 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Gun Battery (island AA gun) | Banished facility | E6 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Gun Battery (island AA gun) | Banished facility | E6 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Ransom Keep | Banished facility | B7 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Gun Battery (island AA gun) | Banished facility | D7 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Annex Ridge | Banished facility | E8 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Riven Gate | Banished facility | F8 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Conservatory | Forerunner facility | B4 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Spire | Forerunner facility | C6 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Beacon | Forerunner facility | E7 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Beacon | Forerunner facility | east of H7 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Beacon | Forerunner facility | F8 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |
| Nexus | Forerunner facility | H8 | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium] |
| The Command Spire | Forerunner facility | H8 | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium] |
| Beacon | Forerunner facility | D9 | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium] |

FOB Foxtrot and FOB Golf share cell B7, FOB Bravo and FOB Charlie share C4 and FOB Juliet and FOB Kilo share E8, so a cell alone does not name a FOB; use the "Near ..." headings in the region files to tell them apart. The Tower, Excavation Site, Outpost Tremonius, Conservatory, Spire, Nexus and The Command Spire are also missions (`../nav/`); the map site draws them as facilities, so they appear here as well. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium · model analysis -- 2026-10-13]

## Files in this folder

| File | Contents | Status |
|---|---|---|
| `index.md` | This roster | research-integrated |
| `ow_lockdown_collectibles.md` | 55 collectible sites, Lockdown | research-integrated |
| `ow_connections_collectibles.md` | 89 collectible sites, Connections | research-integrated |
| `ow_graveyards_collectibles.md` | 26 collectible sites, Pelican Down island | research-integrated |
| `ow_reformation_collectibles.md` | 95 collectible sites, Reformation | research-integrated |
| `spartan_cores_plot.md` | All 45 Spartan Cores by zone, grid cell and item code | research-integrated |

Region placement in those files is derived from map coordinates (nearest named anchor), so a site near a border may belong to the neighbouring region -- see `../limitations.md` "MapGenie map data". Per-site walkthroughs (outpost objectives, HVT arenas) remain uncovered; that would need a new research brief. What P3 did add at site level lives elsewhere: Briglard and Bipbap HVT detail in `../items/weapons.md`, the Black Eye Skull in `../items/skulls.md`, and the co-op timing achievements for Ransom Keep, the Forge of Teash and Riven Gate in `../achievements.md`.
