# Halo Infinite -- Mechanics

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28

Core game-system rules. `_source: deep-research cascade 2026-09-28 · capture: web_fetch_` applies to every claim below unless a line overrides it (P1 base; P2 additions marked "(P2)").

## Saving and checkpoints (P2)

No manual save; autosave only. A "Saving checkpoint" is only a death-reload point; "Saving progress" survives quitting. Checkpoints fire only when you're out of immediate danger with full shields; fast travel, collectibles, HVT kills and outpost clears force a save. Full table: `nav/architecture.md` "Save stations / checkpoints". [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 3 sources, 1 language]

## Shields, health, and melee

[unlock-chain incomplete -- no source described shield/health regen numbers or melee damage. P1 did not cover it, P2 was the navigation pass, and P3 did not reach it (search budget exhausted). This cascade is finished, so it stays a gap; fill it from live observation.] [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

What P3 does record: the Tremonius, Bassus, Jega and Tovarus/Hyperius tactics all strip a shield with plasma weapons (or a Pulse Carbine) and then switch to kinetic damage, and the Tremonius and Tovarus/Hyperius shields regenerate if you stop damaging them -- see the boss files under `npcs/`. The Black Eye Skull's effect is that your shields only recharge when you melee enemies (`items/skulls.md`). [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: medium · per-boss sourcing in the boss files]

## Ammo refills (web research 2026-10-11)

_source: search summaries of Twinfinite "how to get more ammo" (twinfinite.net/guides/halo-infinite-how-to-get-more-ammo/) and Halopedia Ammo_printer (not opened); samurai-gamers.com Conservatory walkthrough and gamerguides.com Conservatory walkthrough, opened 2026-10-11 · capture: web_fetch_

- Ammo Crates are scattered through the game (a holographic logo sticks up from the top); hold the interact button to refill the ammo type matching the weapon you hold; walking over the same weapon on the ground also refills it; ammo printers in the Armory of Reckoning side mission each hold a kinetic ammo crate. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: low · search-summary only, pages not opened]
- "Hardlight regenerator" ammo top-off stations in the Conservatory: three searches (2026-10-11, 2026-10-13 twice) and the two Conservatory walkthroughs found no page that names such a station in that mission; that is a gap in what the search found, not proof there is none. No source found for a "hardlight regenerator" or any Forerunner ammo-regenerator station by that name; the two walkthroughs mention only guns lying along the path, weapon racks near a door before a bridge, a Shock Rifle after a Skimmer wave, and "plenty of other weapons scattered about" after the Drop Wall. Whether such stations exist in game data was not established. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: low · negative result, incomplete search]
- Reported from play 2026-10-13 (grid G8, the cave under the hexagonal pillars near FOB Lima that holds Spartan Core C44): a fixed station there refills every ammo type (kinetic, plasma, shock and the rest, including a sniper rifle), and the same cave holds a spread of weapons including Hard Light weapons, energy swords and gravity hammers. Matches the "refill the ammo type of the weapon you hold" behaviour above. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · class:live-observation · play report, cell G8 from the C44 catalog row]

## Damage types and enemy matchups (web research 2026-10-09)

_source: web research 2026-10-09: Halopedia Weapon_types (https://www.halopedia.org/Weapon_types), Kig-Yar/Gameplay, Jiralhanae/Gameplay, Sangheili/Gameplay, Unggoy/Gameplay, Mgalekgolo/Gameplay, Shock_Rifle, Disruptor, Skewer, Sentinel_beam/Gameplay; samurai-gamers.com/halo-infinite/weapon-damage-types; gfinityesports.com/article/best-weapons-campaign; Twinfinite, Windows Central, Gamer Guides and Halopedia Regulator_Sentinel / Sentinel_launcher via search summary only (pages 403 or not fetched) · capture: web_fetch. Halopedia mixes campaign and multiplayer; mechanism only, no numbers._

**Damage types** [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · class:community-wiki + editorial-en]
- Kinetic: strong on unshielded health and headshots; weak on energy shields; an enemy's hand-held shield is almost impervious to it.
- Plasma: strong on energy shields; reduced damage to bare health; sustained plasma wears a hand shield down and an overcharged Plasma Pistol shot knocks it away. The base Plasma Pistol charge does not stall vehicles in this game.
- Shock: arcs between nearby targets; repeated hits temporarily disable drivable vehicles (Shock Rifle about two hits; Disruptor needs sustained hits); stuns unarmed charging enemies; Shock Rifle headshot bonus applies through shields; low damage per hit.
- Hardlight (Heatwave, Sentinel Beam): works on shields and health, ricochets, pierces, disintegrates kills; can kill vehicle occupants without destroying the vehicle.
- Explosive (SPNKr, Hydra, Cindershot): groups, vehicles, large targets; ammo scarce.
- Melee power weapons: one-hit kills up close; sword energy and hammer charge run out after several uses.
- Headshots: possible with kinetic, plasma, hardlight and shock weapons; helmets on some enemies must be shot off first. No source lists weapons that cannot headshot.

**Enemy matchups** (names gated at enemy-tier 1) [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: medium (Halopedia gameplay pages) / low (search-summary guides, marked) · class:community-wiki + editorial-en]
- Grunts: weak, rush; heavy-weapon carriers and drivers are priorities; melee kills; tracking plasma (Pulse Carbine) for fast packs (Gfinity); Ghost drivers easy to hijack.
- Jackals: hand shield beats kinetic; plasma or an overcharged Plasma Pistol drops it; a precise shot to the exposed hand or feet makes them flinch and expose the head; grenades behind; melee can knock the shield aside. Jackal snipers: laser sight, three-shot volleys, no shield, no longer flee.
- Skimmers: most die in one or two hits from anything (Gamer Guides, search summary only).
- Brutes: plating falls off under fire; higher ranks add shields (varies); shielded ones can't be assassinated until shields drop; helmet must be shot off before headshots; Berserkers charge unarmed: stun with shock or Grappleshot away. Ravager and Sentinel Beam rated against heavily armored foes (Gamer Guides, search summary only).
- Elites: shields raise on alert; with shields down higher ranks use active camo, sword users leap. No Halopedia weapon advice; plasma-then-kinetic is the inferred pattern (matches the boss tactics above).
- Hunters: Infinite Halopedia section is a stub. Guide summaries (Twinfinite, Windows Central; pages 403): orange weak spots and back, Grappleshot behind, plasma grenades on the back, rockets/frags via splash, fight around pillars; the partner enrages when one dies. Kotaku keeps the Volatile Skewer for Hunter pairs.
- Sentinels: Regulators weak to electricity, eye weak spot glints before firing; launchers vulnerable when their cover opens, to overcharged Plasma Pistol shots, plasma explosions and melee (search summary of Halopedia pages).
- Vehicles: Skewer kills light and air vehicles in one or two shots and shoves heavy ones; shock disables; Hydra and M41 Tracker lock on; hammer effective (Halopedia general). Per-vehicle and turret detail not found.
- Banished in general move slowly and bunch up, favouring precision weapons and splash/chain weapons (Gfinity).
- Not found: Chieftain specifics, Protector Sentinels, per-vehicle weak points, campaign ammo availability for most weapons.

## Equipment (Grappleshot, Shield Core, Threat Sensor, Drop Wall, Thruster)

See `items/abilities.md` for acquisition points and per-tier upgrade effects. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

- **Why Quick Shot (Grappleshot rank 3) matters:** several collectibles and HVTs (e.g. the Fog and Thunderstorm Skull perches) sit on sheer hexagonal pillars that are hard to reach without Quick Shot's 40%-shorter cooldown, which lets you chain grapples up walls. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 5 sources, 2 languages]
- **Build guidance for equipment order** lives in `items/builds.md`, not here (advice, not a verifiable claim).

## Spartan Cores and equipment upgrades

See `items/abilities.md` (per-piece upgrade tiers) and `items/upgrades.md` (core math). Corrects the Stage-0 prior of 49 cores: **the confirmed total is 45** (every source checked agrees, and 45 = exactly what fully upgrading all 5 equipment pieces costs at 1/2/3/3 = 9 cores/piece). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 6 sources, 2 languages]

- The disputed alternate totals and the one wrong per-rank cost are recorded where the numbers live: `items/upgrades.md` (totals) and `items/abilities.md` (per-rank costs).

## Valor and FOB armory unlocks (weapons, vehicles, Marines)

See `items/upgrades.md` for the full Valor unlock table. Valor is cumulative and never spent -- requisitioning a FOB-armory item, vehicle, or Marine squad costs nothing once the Valor threshold is reached. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 5 sources]

- Valor sources: completing main story missions gives "usually several hundred" points; 100 per Banished outpost cleared, 30 per Marine-squad rescue, 10 per propaganda tower. FOB captures and HVT kills also award Valor. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 5 sources · achievement: Who is Max Valor?]
- **Exception:** Banished vehicles cannot be requisitioned at a FOB -- they must be stolen in the field (e.g. grapple-boarding a Ghost). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium (single source) · achievement: Whip-Riding the Ghost]
- Marine squads (Assault, Breacher, Scout, Heavy Assault, Sniper, Demolition) and vehicles are Valor-tier FOB unlocks, not a separate progression system.
- Marine types and their weapons (Halopedia Forward_Operating_Base, fetched 2026-10-14): Assault 450 Valor (MA40), Breacher 650 (CQS48 Bulldog shotgun), Scout 1,000 (VK78 Commando), Heavy Assault 1,200 (BR75), Sniper 1,600 (S7 Sniper), Demolition 1,800 (M41 SPNKr). They spawn at controlled FOBs and can fill empty vehicle seats. No source found says you can choose which type spawns or exclude one. Swapping a Marine's weapon for one from a FOB crate by asking a nearby Marine works and is easy (reported from play 2026-10-14; the search summary that mentioned it was not opened). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · _source: web research halopedia.org + play report 2026-10-14]

## FOB capture and map reveal

A captured FOB grants: a fast-travel point, 4 weapon spawners, 1 vehicle spawner, Marines who follow you and crew vehicles, and map markers for nearby collectibles. FOB capture = clear the enemies present, then hack the central terminal. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 5 sources]

## Propaganda Towers: how to destroy one (web research 2026-10-11)

A Propaganda Tower is a small optional Banished broadcast tower; its glowing yellow middle is the weak point and acts like a power source. Melee it, or hit it with explosives or a vehicle, and it blows up: Gfinity says melee leaves you slightly damaged by the blast. Each destroyed tower gives 10 Valor; the first gives Please Shut Up, all ~40 give Off the Air. Not to be confused with the three much larger Banished anti-air guns on the Pelican Down island, which cannot be shot down from the ground: you ride the gravity lift, use the console to expose the core, then destroy the core (`nav/ow_graveyards.md`).

**Propaganda Totems (a separate, bigger structure; observed in play 2026-10-12, Pelican Down island):** a tall red Banished totem with a group of guards gathered around it and no glowing center. Halopedia: totems are Banished-built and broadcast pre-recorded speeches from Atriox; eight stand in the open world, one of them west of the north anti-air gun on Pelican Down (the other seven are southeast of Ransom Keep, southeast of Indiana Squad near a Mjolnir Armory, east of FOB Delta, southwest of the eastern beacon, south of FOB Hotel, west of Repository, plus one the page does not list); a lighting artist who worked on them says some are guarded by Brutes. No source found says whether a totem can be destroyed or what it gives; players report meeting them in the earlier areas too, with no obvious way to blow one up, and a Brute shouting out of each one (Halopedia names Atriox as the speaker; Atriox is the Brute warlord who leads the Banished, so the Brute heard is that speaker -- no conflict). Not the ~40 Propaganda Towers above. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Confirmed: 2 sources, 1 language · _source: web research 2026-10-12, halopedia.org/Propaganda_totem and Tyler Klimek ArtStation project (artstation.com/projects/5BeoAO)_] [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-guide · _source: GGRecon snippet (page itself returned 410), Gfinity, Halopedia propaganda tower page_]

## High Value Targets (HVTs) and variant weapons

15 named HVTs, each hostile (`enemy` vector -- none currently warrant a per-entity `npcs/` file; see `npcs/index.md`). Kill the target **and its whole escort** to permanently unlock its variant weapon in FOB weapon racks; in co-op, the unlock is per-save, so a teammate who hasn't earned it yet still can't use it on your file. Full per-target location/variant table: `items/weapons.md`. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · confidence: high · Confirmed: 6 sources · achievement: Headhunter, Bloodstars' Bane]

- Per-target locations, disputes, variant behavior (including the Calcine Disruptor) and the one still-open source question live in `items/weapons.md`; this section keeps only the unlock rule.

## Campaign co-op and the Winter Update (P3)

Network co-op arrived with the Winter Update (Nov 8, 2022), alongside Mission Replay and 25 new achievements. It adds no zones or edges (`nav/architecture.md`); it changes how progress and collectibles are shared. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 4 sources, 1 language]

- **Who and how:** 1 to 4 players, online only, on dedicated servers, crossplay across PC, Xbox One, Series X/S and Cloud; everyone plays as Chief. Local split-screen was cancelled (343's Sept 1, 2022 update video; a menu glitch reportedly enables it unofficially -- single source). Setup: the Fireteam Leader (crown icon) picks a save and sets difficulty and Skulls and presses Start Co-Op; each other member picks their own save; the leader presses Start Game. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high (cancellation, crossplay) / medium (setup and glitch, single source · class:official-pr / editorial-en) · Confirmed: 4 sources, 1 language]
- **Progress is an intersection, not host-owned.** It is aggregated across every member's chosen save; a mission is marked complete only if all members completed it, and all progress then writes to every member's own save. A collectible (Data Pad, Skull, audio log) appears if any member lacks it and credits every member who lacked it; if all already have it, it does not appear. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 3 sources, 1 language]
- **Per player, never shared:** Spartan Cores (collecting one credits every member who had not collected it, but cores and upgrade choices are spent per player), unlocked equipment, upgrades and HVT variant weapons. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language]
- **Area-of-operations tether:** warning at 800 ft, kill at 1000 ft (roughly 240 m and 300 m); past it you die "for going AWOL" and respawn on your nearest teammate (one forum paraphrase says the fireteam leader; official wording wins). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 4 sources, 1 language]
- **Skull selection in co-op is [Contradicted across sources]:** the June 2022 preview says you can activate Skulls "you (or your teammates) have collected" (union); GameSpot's September 2022 report says only Skulls every player has unlocked (intersection); the retail notes say only that the Fireteam Leader can pick which Skulls are on. Treat the union as design intent and test in-session before a Legendary co-op attempt. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · Contradicted across sources -- see notes]
- **Enemies:** scaling adjusts enemy behavior to fireteam size (single source · class:editorial-en). Friendly fire was on in the July 2022 Insider flight; unconfirmed for retail. [spoiler: none · enemy-tier: 1 · puzzle-tier: 0 · confidence: medium · Single source -- verify · class:editorial-en]
- **Known issue:** in a co-op replay of Spire, skipping the cutscene after the boss and terminal can soft-lock players on a loading screen; do not skip it there (`sections/z07_spire.md`). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Single source -- verify · class:official-pr]
- **Winter Update fixes that matter to runs (official notes, single source):** the Threat Sensor unlock sequence can no longer halt progression; long loads after fast travel or replay fixed; previously enabled Skulls no longer randomly disable when you resume via Continue; completing missions now consistently records the right difficulty and unlocks the full-campaign completion achievements; gameplay time no longer carries over between new save files in the same slot (relevant to Forza Veloce); kill volumes adjusted so enemies launched by the Boom/Cowbell Skulls no longer block objectives. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Single source -- verify · class:official-pr]
- **Contested:** whether 100%-completion-on-one-save unlocks (Requiem Revengeance stance, Act of Genesis stance, Infinity weapon charm) shipped in the Winter Update -- TheSixthAxis's copy of the notes lists them, but the official notes were amended to say they "will be included in an upcoming release"; the official amendment wins, and which release delivered them was not found. [Contradicted across sources -- see notes · spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium]
- **Later updates:** cutscenes became pausable in the campaign (Season 3, Mar 7, 2023); Disruptor sandbox balance changed in the May 10, 2023 update (damage-over-time removed, later reported returned) -- whether the campaign Disruptor and Calcine Disruptor inherit it is [Hypothesis -- unverified]. Achievements stopped showing progress bars in Dec 2021/Feb 2022 but still unlock. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high (pause, progress bars) / low (Disruptor inheritance) · Single source -- verify · class:official-pr]
- **Co-op achievements:** the four completionist achievements and four timing achievements are documented in `achievements.md`.

## Vehicles

[unlock-chain incomplete -- P1 did not research vehicle handling/stats. The Valor unlock table (`items/upgrades.md`) covers acquisition; per-vehicle mechanics were not covered by P2 or P3 either -- fill from live observation.] The Banished-vehicle exception is stated once, under "Valor and FOB armory unlocks" above. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

## Skulls and difficulty modifiers

Full per-Skull location/effect table: `items/skulls.md`. Difficulty tiers: Easy, Normal, Heroic, Legendary; Skulls are toggled per session or per Mission Replay run, independent of difficulty. Turning Skulls on does not disable achievement progress. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 5 sources]

- **Continue vs. Load (older builds):** a Steam-forum LASO report said choosing "Continue" from the main menu turns Skulls off, so load the save directly. The Winter Update (Nov 2022) notes say previously enabled Skulls no longer randomly disable when you resume via Continue, so on the current build that caveat should no longer apply -- whether the forum report predates the fix is [Hypothesis -- unverified]. [Single source, verify · class:forum (report) / class:official-pr (fix) · spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · achievement: Headmaster]

## Generic enemy behavior (enemy vector)

Named bosses/commanders that do **not** carry a per-entity `npcs/` file (one-line mentions, no strategy paragraph -- see `npcs/index.md` "No entity overlay" note). Chak 'Lok, Bassus and Hyperius/Tovarus were promoted at P3 and now have files; the entries below are what remains generic:

- **Chak 'Lok, Bassus, Hyperius and Tovarus** -- promoted to per-entity files at P3 (see `npcs/chak_lok.md`, `npcs/bassus.md`, `npcs/tovarus_hyperius.md`). [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0]
- **Hunter pair at Spire's base** (z07_spire) -- guards the gravity lift ("Hunter. Killer."). The Spire's mission boss, Adjutant Resolution, was promoted to a per-entity file at P2 -- see `npcs/adjutant_resolution.md`. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · achievement: Hunter. Killer.]
- **Okro 'Vagaduun** -- also an HVT (see `items/weapons.md`); commonly the first HVT found, south of ow_lockdown's starting zone. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · achievement: Headhunter]
- **Barroth** -- HVT, sits high on hexagonal pillars during The Sequence (ow_reformation). [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1]
- **Hunter pairs** -- recur at Spire's base and at Nexus (Vintage Fisticuffs: defeat the Nexus pair using only melee finishing blows). [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 0 · achievement: Vintage Fisticuffs] (Nexus pair is late-game per its post-point-of-divergence location; the Spire pair is progression)
- **Chieftain pair** -- Repository (z12_repository); kill one and use its dropped turret to kill the other ("Turnabout is Fair Play"). [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 0 · achievement: Turnabout is Fair Play]
- **Stealth Elites (x4)** -- guard the Grunt Birthday Party Skull in Repository; see `puzzles/` for the full puzzle. [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 2]
- **Red Hunter pair, Silent Auditorium** -- Steam-forum consensus calls this the hardest Legendary encounter in the campaign. [Single source, verify · class:forum · spoiler: late-game · enemy-tier: 2 · puzzle-tier: 0 · achievement: A True Test of Legends]

- **Other P2 encounter notes (generic):** Berserkers deploy when the Tower's lockdown lifts (z04); cloaked golden-armored Elites on the Conservatory's lower level (z06); Aggressor Sentinels and a Sangheili Ultra in The Command Spire (z11); a Hunter pair on The Road (z13). [spoiler: progression (z04, z06) / late-game (z11, z13) · enemy-tier: 1-2 · puzzle-tier: 0 · confidence: medium]

### Enemy reinforcements at Banished outposts (web research 2026-10-09)

_source: web research 2026-10-09 (Gamerguides outpost pages, Halopedia Banished outpost and Forward Operating Base pages; six searches and six fetches found no source on the question below; only playing it settles it)_
- Tip from a search summary (Twinfinite, not fetched): the plasma cannons on enemy reinforcement dropships can be shot off and picked up to use. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: low · Single source (search summary) -- verify · class:community-guide]

- **Do destroyed dropships stop more reinforcements?** No source found says so, and none says the opposite. [Unconfirmed -- no source] [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: low]
- What the guides do say: reinforcements are tied to outpost progress and arrive "dropped in from ships" (Forge of Teash: as you move from silo to silo, mostly elite Brutes; Riven Gate: each gate lowered triggers a wave; Horn of Abolition: a wave at one point, same enemy types as before). Inference, not stated by any source: waves are scripted to objective steps, so killing the ships probably does not cancel the next trigger. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: low · Single source per outpost (Gamerguides) -- verify · class:community-guide]
- Phantoms (Halopedia): heavily modified gunship/dropship Type-44 and Type-52 variants; a Phantom is also something the Banished build at their own outposts. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · Halopedia, single source]

For named individuals WITH per-entity files (major recurring bosses and companions), see `npcs/index.md` and the linked `npcs/<id>.md` files: Tremonius, Jega 'Rdomnai, Escharum, the Harbinger, Despondent Pyre, Echo 216, the Weapon, Adjutant Resolution (P2), Chak 'Lok, Bassus and Tovarus/Hyperius (P3).

## Cross-system dependencies

> **Cross-system dependency** -- see `dependencies.md` DEP-002: Grappleshot rank 3 (Quick Shot) is the practical key to the Skull and HVT perches on hexagonal pillars. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `dependencies.md` DEP-003: 45 cores exactly cover the five max-equipment achievements; co-op needs each player's own 9 per piece. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

> **Cross-system dependency** -- see `dependencies.md` DEP-004: Co-op progress is the intersection of members' saves, which shapes collectible sharing and the fresh-save plan for the completionist achievements. [spoiler: none · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `dependencies.md` DEP-011: Headmaster needs all twelve Skulls on, five of them mission-bound (Replay recovers them); the Continue-versus-Load warning is superseded. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `dependencies.md` SEQ-003: Forza Veloce needs a fresh save in a fresh slot; the timer cannot be restarted on the same save. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]
