# Halo Infinite -- Achievements

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28
**stub_source:** Steam <!-- Which platform's canonical list was fetched. Cite the URL in Sources at end of file. -->
**stub_fetched:** 2026-09-27
**stub_count:** 144
**live_recount:** 2026-09-28 (re-fetched at P3 ingestion) -- https://steamcommunity.com/stats/1240440/achievements: 144 names, name set identical to the stub list fetched 2026-09-27.
**coverage:** verified against the live Steam list 2026-09-28 (re-run at P3 ingestion): 144 names = 94 campaign entries below / 49 deferred (multiplayer) / 1 unreachable, with every live name present in exactly one of the three and no extra names. P3 moved Gatecrasher from unreachable to a Mastery entry (93 -> 94 campaign, 2 -> 1 unreachable). (P1's header said "51 deferred" and its self-check missed 3 names -- Visionary, Grab Some Cover, Evasive Maneuvers -- both corrected at P2.)

## Why this file exists

This file is the corpus's single source of truth for "what achievements does this game have, and what do I need to do for each one." The reader consults it when the player asks any achievement-class question -- by name, by category, or by "what am I about to miss." The aggregator (future) uses it as the completeness skeleton: developer-authored achievement lists are exhaustive, so they double as the minimum claim count for a complete guide.

The reader treats this file as authoritative for **trigger conditions**, **point-of-no-return windows**, and **missability**. It does NOT re-derive these from per-zone files at read-time; ingestion is the moment of aggregation, and this file carries the synthesized result.

## Structure

The file is organized by `trigger_type`. One H2 per type, with achievement entries as H3s under each:

- `## Progression` -- story beats, chapter completes, level milestones
- `## Branch` -- mutually-exclusive choices, endings, faction picks
- `## Mastery` -- skill-bound and restriction-bound challenges
- `## Collection` -- finite, enumerable sets the player completes in full
- `## Threshold` -- cumulative counts without a finite-set ceiling
- `## Discovery` -- non-obvious mechanics or specific-action triggers (often hidden)

A trigger type with no achievements in this game is omitted from the file (not left as an empty section). If the game has zero achievements of a type, the absence is the answer.

## How to classify an achievement into a trigger type

Ask these questions in order; the first "yes" wins. The order matters because some achievements plausibly fit two categories, and the primary classification is what the player has to do *first* to unlock the achievement.

1. **Progression.** Does every player who reaches a certain point in the game get this? If yes, `progression`. (Reaches a story beat, completes a chapter, hits a level milestone, unlocks the default tier of a class.)
2. **Branch.** Does getting this exclude another achievement, or require a non-default choice no other player has to make? If yes, `branch`. (Side with one faction over its mutually-exclusive rival; pick one romance partner over others; pursue one ending that locks out the others.)
3. **Mastery.** Did the player demonstrate skill or accept a restriction beyond normal play? If yes, `mastery`. (Complete without dying; complete on the hardest difficulty; finish under a time limit; complete with a self-imposed loadout restriction.)
4. **Collection.** Is there a finite, enumerable set the player must complete in full? If yes, `collection`. (Find all collectible items of a named type; record every creature in a journal; donate every required item to a museum.)
5. **Threshold.** Is the trigger a cumulative count of any kind of action or state, without a finite-set ceiling? If yes, `threshold`. (Kill N enemies of a class; catch N fish total; read N books in one playthrough; ship N units of a single crop.)
6. **Discovery.** Was the player likely to find this only by deliberate exploration of a non-obvious mechanic, or by following an obscure hint? If yes, `discovery`. Often carries the platform's hidden flag.

Discovery comes last because it's the residual bucket. If any earlier category fits, the achievement isn't really about discovery; it's about whatever the earlier category named.

### Disambiguation rules at the boundaries

Three boundaries carry the highest mislabel risk. These rules resolve them.

**Mastery vs discovery.** Both can apply to "weird-thing-with-the-game-system" achievements. The distinction: `discovery` is when *the fact that the trigger exists* is the achievement (hidden mechanic, easter-egg interaction, weird emergent system). `mastery` is when *executing the trigger well* is the achievement (skill, restriction, time-bound). Shape examples:

- "Kill N enemies of a type within S seconds" -> mastery. The mechanic is obvious; the skill is the trigger.
- "Use a specific enemy's ability against itself" -> discovery. The interaction isn't obvious; finding it is the trigger.
- "Use one enemy as an improvised weapon against another" -> discovery. The interaction is non-obvious.
- "Complete the game without acquiring any of class X's powers" -> mastery. The restriction is the achievement; the mechanics are known.

**Threshold vs collection.** Both can apply to "count-up-to-N" achievements. The distinction: `collection` is when the *set members* are finite, named, and discoverable in advance (the corpus must enumerate them). `threshold` is when the *count* is the achievement; any unit satisfying the action class counts. Shape examples:

- "Catch every distinct species of fish" -> collection. There is a finite known list; the corpus enumerates them.
- "Catch 100 fish" -> threshold. Any fish counts toward the count; the set isn't bounded.
- "Donate every accepted item to the museum" -> collection. The accepted-items list is a finite set.
- "Kill 666 enemies of a class" -> threshold. Any enemy of that class counts.

**Progression vs branch.** Both can apply to "completed-a-chapter" achievements. The distinction: `progression` is the *default path* every player takes; `branch` is when the player had to *choose* this path over another mutually-exclusive one. Shape examples:

- "Complete chapter 5" -> progression. Every player who reaches the end of chapter 5 gets it.
- "Complete chapter 5 the empathetic way" -> branch. Required a non-default choice; excludes the unempathetic-way achievement.
- "Reach level 20" -> progression. Every player who plays long enough hits it.
- "Multiclass into every class in one playthrough without using the in-game respec NPC" -> branch. Required a non-default constraint that excludes the usual play pattern.

When a boundary call is non-obvious, record the reasoning in the entry's `notes:` field so future maintainers and the aggregator have the audit trail.

Within each H2, entries are ordered by the game's natural sequence: chapter order for progression, story-beat order for branch, difficulty order for mastery (easier first), platform-list order for collection and threshold, and platform-list order for discovery. This is convention, not contract -- a corpus may reorder within a section when a different order serves the reader better, and document the choice in the entry-level `notes:` field.

> **Design note (zipper, 2026-09-29):** each achievement's trigger is also stated in the zone, item and entity files it belongs to (its `vector-binding`). This file is the aggregation and the completeness check; the zone and entity files are the primary homes. Not a duplicate to merge.

## Per-achievement entry format

Each achievement gets one entry under the H2 for its `trigger_type`. Format:

```markdown
### [Achievement name -- verbatim from platform list]

- **id:** [API name from platform if known; else display name slugified]
- **hidden:** [yes | no -- from platform's hidden flag]
- **trigger_type:** [progression | branch | mastery | collection | threshold | discovery -- see "How to classify an achievement into a trigger type" above]
- **genre:** [optional, repeatable. Conventional vocabulary: social | roguelike | mission | multiplayer | meta | class. See Genre vocabulary section below; corpora may add their own values with a one-line definition.]
- **trigger:** [paraphrased trigger condition in maintainer's own words -- never reproduce the platform's description verbatim]
- **missable:** [yes | no | only-on-difficulty | scenario-locked]
- **ponr-window:** [the latest gate / chapter / scenario beat where the trigger is still reachable; "n/a" if not missable]
- **prereqs:** [other achievements, items, story flags, or build states that must be in place first]
- **vector-binding:** [the corpus location where the trigger condition is documented in detail -- e.g. `nav/theatre.md` gate 4, `items/weapons.md` "Lord of War" claim, `paths/order.md` golden-path constraint]
- **enemy-tier:** [0-5]
- **puzzle-tier:** [0-3]
- **spoiler:** [none | progression | late-game | story | dlc:<name>]
- **notes:** [maintainer notes -- common gotchas, contested triggers, boundary calls between trigger types, version-specific bugs. Optional.]
```

**On hidden achievements.** A hidden achievement's *name* may itself be a spoiler. Treat the entry's `enemy-tier` and `puzzle-tier` as gating the entire entry (heading included) for hidden achievements, not just the trigger description. The reader hides the heading entirely at read-time when the player's dials are below the threshold.

**On the developer's description.** Steam, PSN, and Xbox achievement descriptions are publisher IP. Cite the achievement *name* verbatim (it's the lookup key the player types when they see the popup). Paraphrase the trigger condition in your own words. Never reproduce the full developer-authored description text. This is the same posture the framework takes toward all third-party-authored source material: names, identifiers, and short factual labels travel verbatim; descriptive prose is paraphrased.

**On `trigger_type` and the boundary cases.** The six trigger types are universal across the genres the framework has tested against. Most achievements classify cleanly; some sit at the boundary between two types (most often mastery <-> discovery, threshold <-> collection, or progression <-> branch). The "How to classify" section above covers the three disambiguation rules. When a boundary call is non-obvious even after applying those rules, record the reasoning in the entry's `notes:` field so future maintainers and the aggregator have the audit trail.

## Genre vocabulary

The `genre:` field is an optional overlay that tags genre-specific structural patterns the universal `trigger_type` doesn't capture. Conventional values shared across corpora:

- **social** -- NPC relationship, romance, friendship, companion-bond. Strong in RPGs, sims, life-games.
- **roguelike** -- character/ship-bound, run-condition, meta-progression. The roguelike-specific "what unit owns this achievement" structure.
- **mission** -- per-level mastery; achievements bind to individual missions or levels rather than to story beats. Common in stealth-action and arcade-racing games where the level is the unit.
- **multiplayer** -- online, co-op, PvP, server-social interaction. Live-service tag.
- **meta** -- fourth-wall, filesystem-poking, easter-egg, ARG. Used when the achievement's trigger reaches outside the game's diegetic world.
- **class** -- class/subclass-acquisition patterns; achievements bind to the player's class or build identity rather than to story progression.

Corpora may add their own values when none of the conventional values fit. New values get a one-line definition in this section. The reader treats unknown `genre:` values as opaque tags rather than as errors.

[Add corpus-specific genre values here as they're declared.]

## Progression

### First Contact
- **id:** First Contact
- **hidden:** yes
- **trigger_type:** progression
- **trigger:** Reach the opening story beat of Warship Gbraakon (the very start of the campaign).
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/z01_warship_gbraakon.md`
- **enemy-tier:** 3
- **puzzle-tier:** 3
- **spoiler:** story
- **notes:** Hidden because it's tied to the opening cutscene; the trigger itself (start the campaign) is trivial, but the name/context is gated story-tier.

### Together. Again?
- **id:** Together. Again?
- **hidden:** yes
- **trigger_type:** progression
- **trigger:** Retrieve the Weapon AI during Foundation.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `npcs/the_weapon.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression
- **notes:** Do not confuse with "Together. Again." (no question mark) -- a different achievement tied to Echo 216 in House of Reckoning.

### Ascension
- **id:** Ascension
- **hidden:** no
- **trigger_type:** progression
- **trigger:** Defeat Tremonius at the elevator at the end of Foundation (z02); it fires on his death, before you ride the elevator up.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `npcs/tremonius.md`, `nav/z02_foundation.md` gate 6
- **enemy-tier:** 1
- **puzzle-tier:** 0
- **spoiler:** progression

### Zeta
- **id:** Zeta
- **hidden:** no
- **trigger_type:** progression
- **trigger:** Step out of the surface door in Outpost Tremonius (z03) once its terminal opens it -- it fires when the overview cutscene ends, a few minutes after Ascension, not at mission end.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** Ascension (comes first in the mission order)
- **vector-binding:** `nav/z03_outpost_tremonius.md` gate 4, `sections/z03_outpost_tremonius.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### Fallen
- **id:** Fallen
- **hidden:** no
- **trigger_type:** progression
- **trigger:** Finish The Tower.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/z04_the_tower.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### Unearthed
- **id:** Unearthed
- **hidden:** no
- **trigger_type:** progression
- **trigger:** Shut down the Banished mining laser at Excavation Site.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/z05_excavation_site.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### Visionary / Grab Some Cover / Evasive Maneuvers
- **id:** Visionary, Grab Some Cover, Evasive Maneuvers
- **hidden:** no (Visionary, Grab Some Cover: Steam shows their descriptions); Evasive Maneuvers: Steam page shows no description text -- treated as not hidden, unverified
- **trigger_type:** progression, progression, progression
- **trigger:** Pick up a story equipment piece: the Threat Sensor in The Tower (Visionary), the Drop Wall on the first dead Spartan in the Conservatory (Grab Some Cover), the Thruster on the second dead Spartan in the Conservatory (Evasive Maneuvers).
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `items/abilities.md`, `nav/z04_the_tower.md`, `nav/z06_conservatory.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression
- **notes:** Added at P2 ingestion (2026-09-28): these three campaign names were tagged on P1 claims (`items/abilities.md`, `sections/z04_the_tower.md`, `sections/z06_conservatory.md`) but had no entry here, so P1's "every stub name is in one of the three sections" self-check was wrong by 3. Visionary -> Threat Sensor and Grab Some Cover -> Drop Wall are confirmed by Steam's own descriptions (fetched 2026-09-28); Evasive Maneuvers -> Thruster is by elimination plus P1 tagging. Drop Wall/Thruster location per P2 (Conservatory, not Excavation Site -- see `items/abilities.md` conflict note).

### Hunter. Killer.
- **id:** Hunter. Killer.
- **hidden:** no
- **trigger_type:** progression
- **trigger:** Defeat the Hunter pair at the base of Spire.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/z07_spire.md`
- **enemy-tier:** 1
- **puzzle-tier:** 0
- **spoiler:** progression

### Pelican Down
- **id:** Pelican Down
- **hidden:** no
- **trigger_type:** progression
- **trigger:** Unlocks at the start of the AA-gun arc (shutting down the first Spire), not at the arc's end.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/ow_graveyards.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression
- **notes:** Name-collides with the "Spire" mission (z07) and the "Spire Stalker" achievement -- these are three different things.

### One Down…
- **id:** One Down…
- **hidden:** no
- **trigger_type:** progression
- **trigger:** Destroy one of the three Banished AA guns.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/ow_graveyards.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### Brothers Grim
- **id:** Brothers Grim
- **hidden:** yes
- **trigger_type:** progression
- **trigger:** Defeat Hyperius and Tovarus during the Pelican Down arc.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/ow_graveyards.md`, `mechanics.md`
- **enemy-tier:** 1
- **puzzle-tier:** 0
- **spoiler:** progression
- **notes:** The bare trigger is progression-tier; the hidden NAME implies the two bosses are siblings, a relationship reveal gated `story` (see `sections/story_notes.md`).

### Light the Way
- **id:** Light the Way
- **hidden:** no
- **trigger_type:** progression
- **trigger:** Reach the Beacons and assemble the Sequence.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/ow_reformation.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### What Will It Take?
- **id:** What Will It Take?
- **hidden:** yes
- **trigger_type:** progression
- **trigger:** Reach Nexus.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/z10_nexus.md`
- **enemy-tier:** 0
- **puzzle-tier:** 2
- **spoiler:** late-game
- **notes:** The Steam flavor line ("Trust is a fragile thing, isn't it?") is a story-tier hint, gated separately in `sections/story_notes.md`; the bare mission-reached trigger is late-game (post-point-of-divergence).

### Hear These Words!
- **id:** Hear These Words!
- **hidden:** no
- **trigger_type:** progression
- **trigger:** Reach The Command Spire.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/z11_command_spire.md`
- **enemy-tier:** 0
- **puzzle-tier:** 2
- **spoiler:** late-game

### Together. Again.
- **id:** Together. Again.
- **hidden:** yes
- **trigger_type:** progression
- **trigger:** Rescue Echo 216 during the House of Reckoning arc.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `npcs/echo_216.md`
- **enemy-tier:** 3
- **puzzle-tier:** 3
- **spoiler:** story
- **notes:** No question mark -- distinct from "Together. Again?" (Foundation, the Weapon).

### Reckoning
- **id:** Reckoning
- **hidden:** no
- **trigger_type:** progression
- **trigger:** Enter House of Reckoning.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/z14_house_of_reckoning.md`
- **enemy-tier:** 0
- **puzzle-tier:** 2
- **spoiler:** late-game

### Legends
- **id:** Legends
- **hidden:** yes
- **trigger_type:** progression
- **trigger:** Escharum's death at the end of his House of Reckoning boss fight.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `npcs/escharum.md`
- **enemy-tier:** 3
- **puzzle-tier:** 3
- **spoiler:** story

### Too Many Goodbyes
- **id:** Too Many Goodbyes
- **hidden:** yes
- **trigger_type:** progression
- **trigger:** Defeat the Harbinger, the campaign's final boss.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `npcs/harbinger.md`
- **enemy-tier:** 3
- **puzzle-tier:** 3
- **spoiler:** story

### Set a Fire in Your Heart
- **id:** Set a Fire in Your Heart
- **hidden:** no
- **trigger_type:** progression
- **trigger:** Finish the campaign on any difficulty.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `nav/architecture.md`
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none

## Mastery

### Bare Your Fangs
- **id:** Bare Your Fangs
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Complete the campaign on Normal or higher without ever lowering the difficulty mid-run.
- **missable:** only-on-difficulty
- **ponr-window:** n/a (a difficulty-lowering mid-run permanently fails the run for this achievement)
- **prereqs:** none
- **vector-binding:** `settings.md`
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none

### Fight Hard, Die Well
- **id:** Fight Hard, Die Well
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Complete every mission on Heroic.
- **missable:** only-on-difficulty
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `settings.md`
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none

### A True Test of Legends
- **id:** A True Test of Legends
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Complete every mission on Legendary.
- **missable:** only-on-difficulty
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `settings.md`
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **notes:** Steam-forum consensus calls the two red Hunters in Silent Auditorium the hardest Legendary encounter -- see `sections/z15_silent_auditorium.md`. [Single source, verify · class:forum]

### Headmaster
- **id:** Headmaster
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Complete every main mission on Legendary with all 12 Skulls turned on.
- **missable:** only-on-difficulty
- **ponr-window:** n/a
- **prereqs:** All 12 Skulls collected (see `items/skulls.md`); A True Test of Legends implied
- **vector-binding:** `items/skulls.md`, `items/builds.md`
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **notes:** Winter Update patch notes say it "will now unlock consistently"; players whose unlock failed on an earlier game version must meet the conditions again. An older Steam-forum report said choosing "Continue" from the main menu turns Skulls off; the same Winter Update notes say previously enabled Skulls no longer randomly disable when you resume via Continue, so that should not apply on the current build (whether the report predates the fix is unverified). [Single source, verify · class:forum / class:official-pr]

### Forza Veloce
- **id:** Forza Veloce
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Complete all 14 (per the achievement's own text) main missions in under 8 hours total. In practice: finish every main mission on one save within 8 hours of in-game save time.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `nav/architecture.md` (mission list -- note the 14/15/16 mission-count discrepancy documented there)
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **notes:** ~2.5 hours is reportedly achievable on Easy by grappling past fights rather than fighting them; TrueAchievements commenters report 2 to 3.5 hours on Easy with the Bandana Skull, and the HaloRuns full-game records are 52:33 on Easy and 55:14 on Legendary. [Confirmed: 3 sources, 1 language] **The "14" is an official string only:** its verbatim wording appears on Steam, Xbox, GameFAQs and Halopedia, and none of them lists the 14; guide counts are 15 (most guides; Recovery and The Tower as one) and 16 (Halopedia, Gamepressure). The list is [Hypothesis -- unverified]; the number does not change what you have to do. **Timer:** Gamepressure says it keeps running through deaths, TrueAchievements commenters say time lost to reloads does not count and pausing is fine [Contradicted across sources]. Use a fresh save in a fresh slot: before the Winter Update, gameplay time could carry over between saves in the same slot, and the update fixed that. The timer cannot be restarted on the same save. Only FOB Foxtrot is mandatory for it (gives a Mongoose for the drive to The Tower). [Single source -- verify · class:community-wiki]

### Gun Runner
- **id:** Gun Runner
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Destroy all 3 Banished AA guns in the Pelican Down arc within 20 minutes.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** One Down… (implied, destroying one gun is a subset of destroying all three)
- **vector-binding:** `sections/ow_graveyards.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression
- **notes:** The Steam description shows no time limit, but TrueAchievements, Halopedia and a video walkthrough all state a 20-minute window -- assume the timer applies. [Contradicted across sources]

### Conservation of Momentum
- **id:** Conservation of Momentum
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Finish Conservatory in under 15 minutes.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/z06_conservatory.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### Gatecrasher
- **id:** Gatecrasher
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Breach the Auditorium (Silent Auditorium, z15) in under three minutes.
- **missable:** no
- **ponr-window:** n/a (Mission Replay of z15)
- **prereqs:** none
- **vector-binding:** `nav/z15_silent_auditorium.md`
- **enemy-tier:** 2
- **puzzle-tier:** 2
- **spoiler:** late-game
- **notes:** Reclassified at P3 from "unreachable" (P1 could not retrieve its description). Steam's own list gives the description and a 0.9% global unlock rate, which is a primary source; it is one of the Winter Update's achievements (not in the 24 announced, reportedly added before release). Three TrueAchievements guides and comments report it unlocking; their method is to clear the opening area and walk through the opened door within 3 minutes of spawning, ideally on Easy with the Bandana Skull and a rocket launcher carried in. [Confirmed: 2 sources (Steam list + TrueAchievements guides), 1 language · the TrueAchievements pages themselves were unreachable (HTTP 403) at ingestion, so their method text is via the P3 research result; confidence: medium]

### Stick Around
- **id:** Stick Around
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Defeat Tremonius (end of Foundation, z02) specifically with the Skewer.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `npcs/tremonius.md`, `nav/z02_foundation.md`
- **enemy-tier:** 1
- **puzzle-tier:** 0
- **spoiler:** progression
- **notes:** Keep the Skewer found earlier in Foundation and fire it only once his energy shield is down. After the first run it needs a Mission Replay of Foundation.

### Rapid Unscheduled Disassembly
- **id:** Rapid Unscheduled Disassembly
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Destroy both Phantoms before they leave Outpost Tremonius (z03 exterior clear -- not the Tremonius boss fight, which is in Foundation).
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `nav/z03_outpost_tremonius.md` gate 5, `sections/z03_outpost_tremonius.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression
- **notes:** Single official source (the Winter Update notes), so `confidence: medium`.

### Out with a Bang
- **id:** Out with a Bang
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Kill Chak 'Lok (the Tower commander) with a Plasma grenade.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `mechanics.md`, `sections/z04_the_tower.md`
- **enemy-tier:** 1
- **puzzle-tier:** 0
- **spoiler:** progression

### Vintage Fisticuffs
- **id:** Vintage Fisticuffs
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Kill the Nexus Hunter pair using only melee finishing blows.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/z10_nexus.md`
- **enemy-tier:** 2
- **puzzle-tier:** 0
- **spoiler:** late-game

### Turnabout is Fair Play
- **id:** Turnabout is Fair Play
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Kill one Chieftain in Repository, then use his dropped turret to kill the other.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/z12_repository.md`
- **enemy-tier:** 2
- **puzzle-tier:** 0
- **spoiler:** late-game

### More Than He Bargained For
- **id:** More Than He Bargained For
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Defeat Escharum without ever fully losing your shields.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `npcs/escharum.md`
- **enemy-tier:** 2
- **puzzle-tier:** 0
- **spoiler:** late-game

### Spire Stalker
- **id:** Spire Stalker
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Get 40 kills with the Stalker Rifle during The Command Spire mission.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/z11_command_spire.md`
- **enemy-tier:** 0
- **puzzle-tier:** 2
- **spoiler:** late-game
- **notes:** Boundary call: mission-scoped weapon-restriction count. Classified mastery (restricted-method execution) rather than threshold, since the constraint (one specific weapon, one specific mission) is the point, not an open-ended count.

### It Really Does Beat Everything
- **id:** It Really Does Beat Everything
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Clear the South Beacon using a Scorpion tank specifically.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/ow_reformation.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### Bring Shiela Home Safely
- **id:** Bring Shiela Home Safely
- **hidden:** no
- **trigger_type:** mastery
- **trigger:** Escort the Scorpion "Shiela" to House of Reckoning intact (don't lose the tank).
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `sections/z13_the_road.md`
- **enemy-tier:** 0
- **puzzle-tier:** 2
- **spoiler:** late-game
- **notes:** The tank despawning or relocating can break the trigger (TrueAchievements comment). One XboxAchievements comment incorrectly attributes this achievement to House of Reckoning instead of The Road -- it belongs to The Road.

### Whip-Riding the Ghost / Takes One to Make One
- **id:** Whip-Riding the Ghost, Takes One to Make One
- **hidden:** no
- **trigger_type:** mastery
- **genre:** (none -- campaign-wide, not co-op-scoped)
- **trigger:** Grapple-board a Banished Ghost, then splatter its driver.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** Grappleshot
- **vector-binding:** `mechanics.md` (Banished-vehicle-theft exception)
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **notes:** Combined entry -- both names describe the same two-step interaction (board, then splatter). Boundary call: could read as discovery (non-obvious combo), classified mastery since grapple-boarding is an advertised, taught mechanic and the achievement is about executing the follow-through.

### Inseparable / You, Me, Same Page / Controlled Demolition / Wolves at the Doors
- **id:** Inseparable, You, Me, Same Page, Controlled Demolition, Wolves at the Doors
- **hidden:** no
- **trigger_type:** mastery
- **genre:** multiplayer
- **trigger:** Co-op timing feats: kill the Nexus Hunter pair within 3 seconds of each other (Inseparable); destroy all Excavation-Site cooling towers within 60 seconds (You, Me, Same Page); destroy 4 Fuel Silos within 5 seconds at Ransom Keep or Forge of Teash (Controlled Demolition); lower all 3 Riven Gate gates within 15 seconds (Wolves at the Doors).
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** campaign co-op session
- **vector-binding:** `sections/z10_nexus.md`, `sections/z05_excavation_site.md`, `sections/ow_lockdown.md`, `sections/ow_reformation.md`
- **enemy-tier:** 1
- **puzzle-tier:** 1
- **spoiler:** progression
- **notes:** Combined entry -- 4 distinct co-op timing achievements sharing one shape (simultaneous multi-player action within a time window). All four descriptions match the official Winter Update notes word for word, and each is corroborated by the Waypoint achievements blog, Insider Gaming, XboxAchievements and Sportskeeda [Confirmed: 5 sources, 1 language]. Deepened at P3:
  - **Inseparable** (20G) -- the Nexus pair (z10) or the Spire-base pair (z07) are the easiest, most controlled setups; split the pair and burst both down together within the 3 seconds. [Single source -- verify · class:editorial-en for the "easiest pair" advice]
  - **You, Me, Same Page** (20G) -- at the Excavation Site dig (z05), as placed at P2. TrueAchievements groups it with the main-story achievements and notes it is the only one there that cannot be done solo; the Waypoint co-op preview calls the Banished dig site the largest single objective the tether lets a team split across. [Confirmed: 2 sources, 1 language]
  - **Controlled Demolition** (20G) -- Ransom Keep or the Forge of Teash. The developer anecdote shows the design: one player hits the plunger switch that raises the silos while another in a Wasp destroys them.
  - **Wolves at the Doors** (20G) -- Riven Gate. Three players is the reliable setup. The two-player method: one player hits the middle switch and takes a Banshee to the near switch while the partner triggers the far switch about 5 seconds later; it "may not unlock for you this way". [Single source -- verify · class:community-wiki]
  - **Missability of the four:** none; outposts and the Nexus/Spire mission replay through Mission Replay, and the two outpost achievements need a co-op session, so plan them for a replay with three players.

## Collection

### Mix Things Up
- **id:** Mix Things Up
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Get a kill with every weapon and grenade type available aboard Warship Gbraakon.
- **missable:** no
- **ponr-window:** z01_warship_gbraakon (mission-scoped)
- **prereqs:** none
- **vector-binding:** `sections/z01_warship_gbraakon.md`
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none

### Outpost Discovery / Bunker Buster
- **id:** Outpost Discovery, Bunker Buster
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Discover 1 / all 7 Banished outposts (Ransom Keep, Redoubt of Sundering, Forge of Teash, Armory of Reckoning, Horn of Abolition, Riven Gate, Annex Ridge).
- **missable:** no
- **ponr-window:** n/a (all recoverable via Mission Replay / postgame)
- **prereqs:** none
- **vector-binding:** `nav/architecture.md` (Optional Content registry)
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### Reclaimer / Resurgency
- **id:** Reclaimer, Resurgency
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Capture 1 / all 12 FOBs.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `nav/architecture.md`, `mechanics.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### We're On Our Way / No One Left Behind
- **id:** We're On Our Way, No One Left Behind
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Answer 1 / all UNSC distress calls (Marine rescues).
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `nav/architecture.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression
- **notes:** Total distress-call count is [unlock-chain incomplete -- official count not retrieved by P1; P3 did not address it].

### Headhunter / Bloodstars' Bane
- **id:** Headhunter, Bloodstars' Bane
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Kill 1 / all 15 High Value Targets.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `items/weapons.md`
- **enemy-tier:** 1
- **puzzle-tier:** 1
- **spoiler:** progression

### Who is Max Valor?
- **id:** Who is Max Valor?
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Complete every Valor-earning activity type (HVTs, FOBs, distress calls, main missions, outposts, collectibles).
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** implies most other collection achievements
- **vector-binding:** `mechanics.md`, `items/upgrades.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### Dispatches From the Front / Canon Collector
- **id:** Dispatches From the Front, Canon Collector
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Collect 1 / all UNSC audio logs.
- **missable:** yes (pre-replay) / no (post-replay)
- **ponr-window:** per-mission, see `items/collectibles.md`; Mission Replay recovers all
- **prereqs:** none
- **vector-binding:** `items/collectibles.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression
- **notes:** Total-count contradicted across sources (37 vs. 38) -- see `items/collectibles.md`.

### Two Sides to Every Story / Know Your Enemy
- **id:** Two Sides to Every Story, Know Your Enemy
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Collect 1 / all Banished audio logs.
- **missable:** yes (pre-replay) / no (post-replay)
- **ponr-window:** per-mission, see `items/collectibles.md`; Mission Replay recovers all
- **prereqs:** none
- **vector-binding:** `items/collectibles.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression
- **notes:** Total-count contradicted across sources (28 vs. 29).

### Infinity Down / Rubicon Protocol
- **id:** Infinity Down, Rubicon Protocol
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Collect 1 / all Spartan audio logs.
- **missable:** yes (pre-replay) / no (post-replay)
- **ponr-window:** per-mission, see `items/collectibles.md`; Mission Replay recovers all
- **prereqs:** none
- **vector-binding:** `items/collectibles.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression
- **notes:** Total-count contradicted across sources (39 vs. 40).

### Hidden Experience / Mjolnir Master
- **id:** Hidden Experience, Mjolnir Master
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Collect 1 / all 45 Spartan Cores.
- **missable:** yes (3 mission-bound in Outpost Tremonius, pre-replay) / no (post-replay)
- **ponr-window:** z03_outpost_tremonius for the 3 mission-bound cores; Mission Replay recovers
- **prereqs:** none
- **vector-binding:** `items/upgrades.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### Money in the Bank / Armory Amore
- **id:** Money in the Bank, Armory Amore
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Open 1 / all 34 Mjolnir Armor Lockers.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `items/collectibles.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### Eld Aficionado / Haruspis
- **id:** Eld Aficionado, Haruspis
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Scan 1 / all 7 Forerunner Artifacts.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `items/collectibles.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### Headstrong / Catacomb
- **id:** Headstrong, Catacomb
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Collect 1 / all 12 Skulls.
- **missable:** yes (5 mission-bound, pre-replay) / no (post-replay)
- **ponr-window:** per-Skull, see `items/skulls.md`; Mission Replay recovers all
- **prereqs:** none
- **vector-binding:** `items/skulls.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### Please Shut Up / Off the Air
- **id:** Please Shut Up, Off the Air
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Destroy 1 / all ~40 Propaganda Towers.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `nav/architecture.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### Thrusters On Full / Impervious / Big Brother / Getting Defensive / Reaching Out
- **id:** Thrusters On Full, Impervious, Big Brother, Getting Defensive, Reaching Out
- **hidden:** no
- **trigger_type:** collection
- **trigger:** Fully upgrade (all 4 ranks, 9 cores) one specific piece of equipment each: Thrusters On Full = Thruster; Impervious = Drop Wall; Big Brother = Threat Sensor; Getting Defensive = Shield Core; Reaching Out = Grappleshot.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** 9 Spartan Cores per achievement (45 in total, so all five are earnable on one save)
- **vector-binding:** `items/abilities.md` "Max-equipment achievements"
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **notes:** Mapping resolved at P3: Impervious [Confirmed: 4 sources, 1 language], Big Brother [Confirmed: 4 sources, 1 language], Reaching Out [Confirmed: 4 sources, 1 language], Getting Defensive [Confirmed: 2 sources, 1 language]; Thrusters On Full has three sources for the description, but its name-to-description pairing is by elimination (the Steam profile pages show the description with the name clipped), so treat that one row as medium confidence. Gamepressure independently re-states "9 cores to buy all 4 upgrades" per piece. In co-op each player needs their own 9 per piece, and a core picked up by a teammate credits you only if you had not already collected it.

### What's Rightfully Ours / Wardens of Zeta / First Responders / Hunting Party
- **id:** What's Rightfully Ours, Wardens of Zeta, First Responders, Hunting Party
- **hidden:** no
- **trigger_type:** collection
- **genre:** multiplayer
- **trigger:** Co-op: capture all FOBs / clear all outposts / answer all distress calls / kill all HVTs, on any difficulty.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** campaign co-op session
- **vector-binding:** `nav/architecture.md`, `items/weapons.md`
- **enemy-tier:** 1
- **puzzle-tier:** 1
- **spoiler:** progression
- **notes:** Combined entry for 4 co-op completionist achievements mirroring their solo counterparts (Bunker Buster, Resurgency, No One Left Behind, Bloodstars' Bane). Deepened at P3 (10G / 10G / 10G / 20G in that order: What's Rightfully Ours = all FOBs, Wardens of Zeta = all seven outposts, First Responders = all distress calls, Hunting Party = all HVTs): a session marks an activity complete only if every member completed it, so the way to finish all four in one pass is for the whole group to start fresh saves and play the open world together once. Outposts, HVTs and distress calls can be replayed in co-op via Mission Replay; FOB captures are not in the replayable list ("Outposts, Targets, and Marine Events" only), so at least one member needs a fresh save for What's Rightfully Ours. [Confirmed: 3 sources, 1 language for the replay list · Hypothesis -- unverified for the FOB-on-a-fresh-save route]

## Threshold

### Those Wonderful Toys / All-Seeing I / Aegis Fate / Run Rabbit, Run
- **id:** Those Wonderful Toys, All-Seeing I, Aegis Fate, Run Rabbit, Run
- **hidden:** no
- **trigger_type:** threshold
- **trigger:** Use the Grappleshot / Threat Sensor / Drop Wall / Thruster 50 times each (one achievement per piece of equipment).
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `items/abilities.md`
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **notes:** Combined entry -- 4 achievements, one per equipment piece, sharing the identical "use N times" shape. Shield Core has no matching achievement (it's passive, no "use" action).

### Wait, I Can Throw Those?
- **id:** Wait, I Can Throw Those?
- **hidden:** no
- **trigger_type:** threshold
- **trigger:** Throw 50 fusion coils.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `mechanics.md`
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none

### Wanna Have a Catch?
- **id:** Wanna Have a Catch?
- **hidden:** no
- **trigger_type:** threshold
- **trigger:** Stick 50 enemies with a grenade.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `items/consumables.md`
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **notes:** Staggered, unshielded targets are reportedly the easiest to stick.

### Air Raid / Cow Catcher / Gruesome Twosome
- **id:** Air Raid, Cow Catcher, Gruesome Twosome
- **hidden:** no
- **trigger_type:** threshold
- **genre:** multiplayer
- **trigger:** Co-op: 100 kills with all players in air vehicles (Air Raid) / 50 splatters with another player aboard your vehicle (Cow Catcher) / 50 kills on a shared Mongoose (Gruesome Twosome).
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** campaign co-op session
- **vector-binding:** `mechanics.md`
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **notes:** 10G each (P3). [Confirmed: 2 sources, 1 language]

### Keep It Steady / Rolling Thunder
- **id:** Keep It Steady, Rolling Thunder
- **hidden:** no
- **trigger_type:** threshold
- **genre:** multiplayer
- **trigger:** Co-op: get 5 Sniper Rifle or Gravity Hammer kills from a vehicle; everyone aboard shares progress toward the count.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** campaign co-op session
- **vector-binding:** `items/weapons.md`
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **notes:** 10G each (P3). Progress is shared across everyone aboard the vehicle, and both can also be done solo. [Confirmed: 2 sources, 1 language]

## Discovery

### Workplace Safety Violation
- **id:** Workplace Safety Violation
- **hidden:** no
- **trigger_type:** discovery
- **trigger:** Kill an enemy using the Excavation Site mining laser (an environmental object, not a carried weapon).
- **missable:** no
- **ponr-window:** z05_excavation_site (mission-scoped)
- **prereqs:** none
- **vector-binding:** `sections/z05_excavation_site.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression

### Passing the Gas
- **id:** Passing the Gas
- **hidden:** no
- **trigger_type:** discovery
- **trigger:** Kill a Grunt while it's still airborne after being thrown by a Brute.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** none
- **vector-binding:** `mechanics.md`
- **enemy-tier:** 0
- **puzzle-tier:** 0
- **spoiler:** none
- **notes:** Described by sources as luck-dependent (requires a Brute to throw a Grunt near you).

### Nosebleed
- **id:** Nosebleed
- **hidden:** yes
- **trigger_type:** discovery
- **trigger:** Reach the highest reachable point on the ring -- the summit of the mountain where Foxhound Squad is (per Halopedia), northeast of FOB Delta (per Screen Rant); Gamepressure's "north-west" conflicts with this.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** A Wasp (available at 2,600 Valor) reportedly makes the climb easy.
- **vector-binding:** `nav/architecture.md`, `items/upgrades.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression
- **notes:** [Contradicted across sources] on the exact cardinal direction. "Foxhound Squad" is treated here as a landmark reference; if it turns out to be a lore-bearing audio-log squad name, split this note to `story` tier -- worth rechecking.

### Wars with Friends
- **id:** Wars with Friends
- **hidden:** no
- **trigger_type:** discovery
- **trigger:** Bring Marines rescued from a distress call into the next main mission.
- **missable:** no
- **ponr-window:** n/a
- **prereqs:** We're On Our Way (a distress call answered)
- **vector-binding:** `sections/ow_lockdown.md`
- **enemy-tier:** 0
- **puzzle-tier:** 1
- **spoiler:** progression
- **notes:** The Steam 100% guide notes that the first FOB capture, first distress call, and this achievement can all be completed together in one pass through ow_lockdown.

## Deferred (multiplayer, out of single-player scope)

The following 49 names are multiplayer-only per Halo Waypoint's co-op achievement list and the Gamepressure 69-entry campaign list; none appear in either. `deferred-to: limitations` is not needed for these -- they are cleanly out of scope, not a research gap.

Clocking In; We Have a Job For You; Humble Beginnings; I'm Ready, How 'Bout You?; Peak Performance; Passion for Fashion; Which One of Us is the Machine?; Reporting for Duty; "Need a Weapon?"; Brutality; Slaying with Style; Limited Addition; You're Up, Rook'; Peeker's Disadvantage; Customary; Running Laps; Just the Two of Us; Kebab; That Thing on the Left is the Brake; They See Me Rollin'; Sharpshooter; Doing Your Part; All About the Grind; Bomb Returned; Working Remote; Getting Strong Now; Control Freak; Zone Ranger; Back to the Chopper; Multi-class Racer; A Fellow of Infinite Jest; Natural Formation Location Sensation; Sick Burn; Deadeye; New Kid on the Block; Enemies Everywhere!; Get the Popcorn; Sparring Partners; Watt Say You?; Battle Tested; One Shot, Top Mid; Skyhook Shot; Do You Even Gift?; Augmented; Secret Stash; MEDIC!; Straight to the Bank; Make a Little More Noise; Party Bus.

Doing Your Part, Make a Little More Noise, Getting Strong Now and Sparring Partners specifically come from the multiplayer tutorial and Training Mode, not competitive multiplayer proper, per the deep-research result -- still out of campaign scope.

## Unreachable

**Greased Lightning** -- its description was not retrieved by P1 research and Steam's list page shows none; it appears in neither the Halo Waypoint co-op achievement list nor Gamepressure's 69-entry campaign list, so it is presumed multiplayer-only. Recorded in `limitations.md`. (Gatecrasher was moved out of this section at P3 -- see the Mastery entry.)

## Genre vocabulary (corpus-specific)

- **multiplayer** -- applied to campaign **co-op** achievements in this corpus (Halo Infinite's campaign co-op counts as in-scope per the P1 brief, but the achievement still requires a second player, matching the conventional `multiplayer` definition of "online, co-op, PvP").

## Completeness self-check

144 total names (live Steam list, re-fetched 2026-09-28 at P2 and again at P3) = 94 resolved above + 49 deferred (multiplayer) + 1 unreachable (Greased Lightning). Per-section id counts, recomputed by script at P3 ingestion: Progression 19 entry-headings / 21 ids; Mastery 19 / 23; Collection 16 / 35; Threshold 5 / 11; Discovery 4 / 4 = 94 ids (94 unique, no id written twice). Set check: every live name matched exactly one of resolved / deferred / unreachable; no corpus name absent from the live list. P1's earlier breakdown (17/24/24/10/5, summing to 80 not 93) and its 'verified by inspection' claim were wrong -- three campaign names (Visionary, Grab Some Cover, Evasive Maneuvers) had no entry; added under Progression at P2.

## Sources

- https://steamcommunity.com/stats/1240440/achievements (fetched 2026-09-27)
- Full per-achievement trigger detail: the P1 deep-research cascade result (2026-09-27).

## Cross-system dependencies

> **Cross-system dependency** -- see `dependencies.md` PON-003: Leaving Warship Gbraakon or Foundation makes their Skulls, logs and mission achievements reachable only through Mission Replay. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `dependencies.md` DEP-001: The Threat Sensor from The Tower is the practical tool against both cloaking bosses, and maxing it is Big Brother. [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 1]

> **Cross-system dependency** -- see `dependencies.md` DEP-003: 45 cores exactly cover the five max-equipment achievements; co-op needs each player's own 9 per piece. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

> **Cross-system dependency** -- see `dependencies.md` DEP-004: Co-op progress is the intersection of members' saves, which shapes collectible sharing and the fresh-save plan for the completionist achievements. [spoiler: none · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `dependencies.md` DEP-005: Achievement methods that use the Bandana Skull can only use it after collecting it in the last mission (second run or Replay). [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 2]

> **Cross-system dependency** -- see `dependencies.md` DEP-009: Mission Replay carries loadout, equipment and upgrades into any completed mission, making timed and per-mission achievements replay plans. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

> **Cross-system dependency** -- see `dependencies.md` DEP-010: The Black Eye Skull needs Pelican Down done and the Grappleshot, is not mission-bound, and counts toward Catacomb and Headmaster. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `dependencies.md` DEP-011: Headmaster needs all twelve Skulls on, five of them mission-bound (Replay recovers them); the Continue-versus-Load warning is superseded. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `dependencies.md` DEP-013: Spire Stalker's 40 kills must happen in the second Adjutant mission, so bank them on the adds before the fight. [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 2]

> **Cross-system dependency** -- see `dependencies.md` DEP-014: The co-op timing achievements at the dig and outposts are closed from Nexus until the credits; plan them before Nexus, postgame or by Replay. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1]

> **Cross-system dependency** -- see `dependencies.md` SEQ-001: Stick Around must use the Skewer found earlier in Foundation; after Foundation only Mission Replay works. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0]

> **Cross-system dependency** -- see `dependencies.md` SEQ-002: Zeta fires at the surface door; destroy both Phantoms during the exterior clear before calling the Pelican. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `dependencies.md` SEQ-003: Forza Veloce needs a fresh save in a fresh slot; the timer cannot be restarted on the same save. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

> **Cross-system dependency** -- see `dependencies.md` SEQ-004: Gun Runner's three AA guns must all fall within 20 minutes (stated by three sources). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `dependencies.md` SEQ-005: Rescue the first Marines, capture the first FOB and bring the Marines into the next mission in one Lockdown pass. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]
