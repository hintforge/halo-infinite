# Halo Infinite -- Limitations & Blocked Sources

Sources I found that look useful but couldn't fully fetch -- paywalls, Cloudflare, age gates, video-only content, etc. URLs preserved so the player (or another contributor) can open them in a real browser.

## How to read this file
- Each entry: topic, URL, block type, what I could glean, best alternative I did get to.
- Each per-topic file (in `puzzles/`, `[areas]/`, `items/`, `sections/`) also lists its own blocked sources at the bottom -- the player rarely needs to come hunting here.
- This file is the catch-all for sources that didn't fit a specific topic.

## Block types
- **paywall** -- content gated behind a subscription or article limit
- **cloudflare** -- Cloudflare bot challenge / 403 / 503 to automated fetching
- **video-only** -- YouTube or other video where the answer is shown visually; no readable text equivalent
- **age-gate** -- content blocked behind age verification
- **cookie-wall** -- popup or consent flow that broke the fetch
- **search-snippet-only** -- search engine returned a snippet but the page itself wasn't reachable
- **dead-link** -- URL was in another source but no longer resolves

## Entries (P1, 2026-09-28)

### FOB total count -- official list (resolved at P2, 2026-09-28)
- P1 had only an unconfirmed 12-name list. P2 confirmed all 12 names and their region split (Lockdown: Golf, Foxtrot; Connections: Alpha, Bravo, Charlie, Delta, Echo; Graveyards: none; Reformation: Hotel, Juliet, Kilo, Lima, November), each name backed by 2+ guide sources (Neoseeker's FOB guide region headings, The Loadout, Pure Xbox, Digital Trends, GamerGuides; total of 12 per Halopedia + GamesRadar). Still no developer-published list -- the spelling/set is guide-consensus, not official. Full table: `nav/architecture.md` "Fast-travel network". [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

### Shield Core acquisition container (resolved at P2, 2026-09-28)
- P1 had "early story" only. P2: taken from a dead Spartan during Foundation (z02) -- The Loadout + GamerGuides agree. See `items/abilities.md` and `nav/z02_foundation.md`. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

### Black Eye Skull container (resolved at P3, 2026-09-28)
- P1 had the effect only. P3 located it: a waterfall cave in the southern part of Reformation, reached by Grappleshot after The Sequence opens the region (PC Gamer, Gamepressure, Gamepur, GameRant, EarlyGame, Sportskeeda, Shacknews). One landmark slip remains recorded in `items/skulls.md` (GameRant's "Raven Gate"). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

### HVT variant weapon behaviour (Bipbap) (resolved at P3, 2026-09-28)
- P3: delayed-detonation rounds, more damage and an electrical area splash (five sources agree on the direction); the magazine 10 -> 7 and one-shot vehicle disable are Halopedia only (class:community-wiki, kept provisionally). Whether the May 2023 sandbox Disruptor change reaches the campaign weapon is untested. See `items/weapons.md`. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1]

### Datamined HVT spawn / Skull effect exact values
- Topic: precise numeric values for HVT spawn conditions and Skull effect magnitudes.
- Block type: search-snippet-only -- no datamining source was found by P1.
- Best alternative: guide-level qualitative descriptions only, in `items/skulls.md` and `items/weapons.md`.

### "Gatecrasher" and "Greased Lightning" achievements
- **Gatecrasher (resolved at P3, 2026-09-28):** Steam's own list gives "Breach the Auditorium in under three minutes" (0.9% global unlock); it is a Winter Update campaign achievement and now has a Mastery entry in `achievements.md`. TrueAchievements' pages (a376267 and two comment threads) returned HTTP 403 at ingestion, so the unlock method is via the P3 research result, not read directly. [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 2]
- **Greased Lightning (still open):** Steam's list page shows no description; it appears in neither the Halo Waypoint co-op list nor Gamepressure's campaign list, so it stays presumed multiplayer-only in `achievements.md` "Unreachable". [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

## Entries (P2, 2026-09-28)

### Neoseeker FOB guide -- Valor thresholds per FOB requisition (resolved 2026-09-28: page read in full by a contributor; thresholds are account-wide, see `items/upgrades.md`; per-FOB reveals now in `nav/architecture.md`)
- Topic: which Valor tier unlocks which requisition at each FOB.
- Block type: search-snippet-only (Neoseeker's table blocked from fetching; its region headings were readable).
- URL: https://www.neoseeker.com/halo-infinite/walkthrough/Forward_Operating_Bases
- Best alternative: `items/upgrades.md` Valor unlock table (P1, region-agnostic).

### Video walkthroughs -- not transcribed
- Topic: per-zone gate confirmation from video.
- Block type: video-only; no segments transcribed within the P2 research budget.
- Best alternative: text walkthroughs (Halopedia, GamerGuides, GamePressure, Neoseeker) -- 3+ sources for most zones.

### Repository (z12), The Road (z13), Silent Auditorium (z15) step-level routing
- Topic: room-by-room gate order.
- Block type: none (not blocked) -- simply thin coverage: every gate in these three zones is single-source (Halopedia or GamerGuides or Gameranx). Treat their gate lists in `nav/` as `confidence: medium` until corroborated. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

### Tremonius boss-fight placement (resolved at P3, 2026-09-28)
- Settled: the fight is the last encounter of Foundation (z02), five sources (GamerGuides, PCGamesN, Samurai Gamers, ScreenRant, Windows Central); Ascension fires on his death, Zeta at the z03 surface door a few minutes later. P1's z03 placement and one low-quality site's z03 / Gravity Hammer version were dropped. Corpus files updated: `npcs/tremonius.md`, `nav/z02_foundation.md`, `nav/z03_outpost_tremonius.md`, `nav/architecture.md`, `achievements.md`. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

### Graveyards island (ow_graveyards) postgame reachability (still contradicted after P3)
- P3 found sources on both sides: Neoseeker, Gamerpillar and Halopedia treat it as mission-only; Gamepressure, Digital Trends and a Microsoft statement relayed by Kotaku point to free roaming, and the Winter Update removed an erroneous kill volume there. No first-hand postgame walk-in report exists; a Steam user flew a Banshee off the island after the mission, and two report kill barriers. The corpus says: Mission Replay of Pelican Down is guaranteed; free-roam re-entry is likely but unverified. Test it live and record the result. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2]

### TacMap region-name display
- Topic: whether the TacMap itself prints "Lockdown" / "Connections" / "Reformation", or those are guide/section labels only.
- Block type: none -- not confirmed by any source. `nav/localization.md` treats them as section titles, not map labels.

### Outpost Tremonius as a fast-travel point (resolved at P3, 2026-09-28)
- Yes, it is a fast-travel node once liberated, but it is not a lettered FOB (SVG, Sirus Gaming, Cultured Vultures); the FOB count stays 12, and at least one FOB must be captured before fast travel works at all. `items/weapons.md` reworded. One editorial source also lists completed outposts and post-Tower missions as destinations; uncorroborated (`nav/architecture.md`). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

### Non-English gate-level coverage (P2)
- Only list-level Spanish (Vandal mission names) and German (Spieleboom, playcentral.de) sources were found; no per-gate non-English walkthrough. Reddit: no canonical thread identified, so Reddit was not fetched. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

## Entries (P3, 2026-09-28)

### Still unresolved or not reached by P3
- **Purging Shock Rifle source** (Skimmer cave north of FOB Juliet vs. the "between FOB Kilo and Juliet" wording that may describe Myriad): the P3 search budget ran out first. See `items/weapons.md`. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1]
- **Fog and Blind Skull locations** (west vs. southwest of FOB Alpha; west of FOB Hotel vs. DBLTAP's "Island 1"): not reached. See `items/skulls.md`. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]
- **Second sources for Repository (z12), The Road (z13) and Silent Auditorium (z15) gates:** not reached, and no video was transcribed; their gate lists stay `confidence: medium`. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]
- **Per-mission collectible counts** for The Command Spire, The Road and Silent Auditorium: no source found. See `items/collectibles.md`. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2]
- **Shield/health regeneration and melee numbers; whether the TacMap prints region names:** not reached. `mechanics.md` and `nav/localization.md` keep the gap. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]
- **Legendary / all-Skulls run strategy and speedrun movement tech:** only the HaloRuns record times were gathered (52:33 Easy, 55:14 Legendary, cited in `achievements.md` Forza Veloce); no route or tech breakdown. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]
- **Which release delivered the 100%-completion stances and charm:** not found; the official notes were amended to "an upcoming release". See `mechanics.md` co-op section. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

### Cross-source conflicts P3 left open (recorded in the corpus)
- **Forza Veloce's "14" missions:** no source names the 14; the number is an official string only (`achievements.md`). The most likely reading (15 menu entries with Recovery and The Tower merged, plus one more merge such as Spire folding into Pelican Down) is [Hypothesis -- unverified]. The operational answer -- every main mission on one save within 8 hours, fresh save in a fresh slot -- does not depend on it. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]
- **Escharum relay count:** four (PCGamesN, Cronica de Gipuzkoa) vs. three (Windows Central; the P1 pass). See `npcs/escharum.md`. [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 0]
- **Tovarus / Hyperius kill order:** five guides say Hyperius first, PCGamesN alone says Tovarus first. See `npcs/tovarus_hyperius.md`. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0]
- **Co-op Skull selection:** union (June 2022 preview) vs. intersection (GameSpot, Sept 2022); the retail notes do not settle it. See `mechanics.md`. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

### Blocked source at ingestion
- **TrueAchievements** (a376267 Gatecrasher and comment threads): HTTP 403 to automated fetching on 2026-09-28. The Gatecrasher unlock method rests on the P3 result's reading of those guides; Steam's own list text was read directly. [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 2]

### Coverage of P3 itself
- Sources were almost all English: one independent Spanish guide (Escharum), a Spanish translation of Windows Central (not independent), a Dutch news item and a French forum question. No PT-BR or DE source was reached. Reddit was not fetched. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

## Entries (MapGenie gap-fill, 2026-10-06)

### MapGenie map data -- single source, derived regions
- Source: https://mapgenie.io/halo-infinite/maps/zeta-halo -- the page itself blocked the normal fetch, but its public map-data endpoint returned every marker (the pull was made on 2026-10-06; the shipped copy of that data is `extract_tools/collectible_catalog.json`).
- What it gave: a location line and coordinates for every overworld collectible -> `optional_zones/<zone>_collectibles.md`. Totals agree with the corpus (45 cores, 12 skulls, 34 lockers, 7 artifacts, 37/28/39 logs).
- Limits: (1) one third-party source, so every site row is `confidence: medium`; (2) the map has no region borders, so each item's region is its nearest named FOB/outpost/landmark -- items near a border may sit in the neighbouring region (Graveyards gets 7 core markers by this rule where the corpus says 5); (3) mission interiors are barely covered -- it adds nothing for Command Spire logs, The Road or Silent Auditorium logs, which stay open above; (4) 40 Propaganda Tower markers carry no location text; (5) location text is MapGenie's wording, cleared for publication as-is (2026-10-06); (6) the grid cell and item code on every row (added 2026-10-13) are in the map site's coordinates, not something the game prints, and the "Approach notes" at the end of the four region files and in `items/collectibles.md` (185 items) read the map site's player screenshots (third-party images, not stored in the repo; one viewer's shot per item, so medium to low confidence; 170 were written in one pass, 40 of those were re-checked against the images and 7 corrected, the rest were not re-checked; 14 items had screenshots too dark or distant to add anything). [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2]
- **Keep (2026-10-06):** the MapGenie pull was a one-off, and the data stays as the guide's location layer. For the record: MapGenie is owned by Ziff Davis (since April 2022); refresh the data by hand if the map updates.

## Always-blocked categories

- **Non-English coverage was uneven:** achieved for Skulls, Spartan Cores, Foundation and Repository only; the remaining missions have no non-English source in P1, and no video segments were transcribed (only titles/descriptions were used). Not a hard block, just an acknowledged P1 gap -- P2/P3 should target non-English sources for the un-covered missions. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]
- **Reddit was not needed for P1** -- Steam forums supplied equivalent community evidence, so Reddit was not fetched this phase. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]
