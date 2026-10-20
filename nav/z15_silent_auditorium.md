# Nav -- Silent Auditorium (z15_silent_auditorium)

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28
**research_run:** P2 (deep-research cascade), ingested 2026-09-28

**Type:** main-story zone (Forerunner interior, final mission)
**Linear?:** yes
**Chapter:** 15. Silent Auditorium (the campaign-section title for this mission is itself a `story` reveal -- see `localization.md`)

_source: deep-research cascade 2026-09-28 · capture: web_fetch · category: mainline unless noted · confidence per claim · **coverage note:** most gates below are single-source; treat as medium confidence -- see `../limitations.md`_

## Entry

From `z14_house_of_reckoning` via edge `(z14_house_of_reckoning, z15_silent_auditorium)` -- see `architecture.md`. You start in a Pelican troop bay en route (whose Pelican is a `story` beat -- see `../sections/z15_silent_auditorium.md`). [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium · Single source -- verify · class:community-wiki]

## Exit

To `ow_postgame` via edge `(z15_silent_auditorium, ow_postgame)` -- the credits roll and you respawn in the reopened overworld.
**Type:** story-gate
**Point of no return:** none -- the whole overworld reopens after the credits.

## Outgoing edges

- `(z15_silent_auditorium, ow_postgame)` -- story-gate, credits
- `(TacMap, z15_silent_auditorium)` -- conditional (Mission Replay), only after completion

## Entry tips (3 max)

1. **Bandana Skull:** it's earned by reaching the final lift without destroying any Sentinels -- decide before you start shooting. See `../items/skulls.md`. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium · Single source -- verify · class:editorial-en]
2. The red Hunter pair here is widely called the hardest Legendary encounter (P1, Steam forum). [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 2 · confidence: medium · Single source -- verify · class:forum]
3. This is the last mission -- anything you missed in the overworld comes back after the credits. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high]

## Sequential gates

1. **Troop bay start** -- begin in a Pelican troop bay en route. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium · Single source -- verify · class:community-wiki]
2. **Halls of statues** -- pass through the statue halls. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium · Single source -- verify · class:community-wiki]
3. **Orange-portal chamber** -- a chamber with glowing orange portals and floating metal shapes (Mythic-Skull-style set piece; pointer only). [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium · Single source -- verify · class:editorial-en]
4. **Red Hunter pair** -- two red Hunters. [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 0 · confidence: medium · Single source -- verify · class:forum]
5. **Sub-monitor meeting** -- Adjutant Resolution makes amends in a scripted scene. [spoiler: story · enemy-tier: 3 · puzzle-tier: 3 · category: lore · confidence: medium · Single source -- verify · class:community-wiki · entity: adjutant_resolution · entity-status: hostile]
   > see npcs/adjutant_resolution.md for full summary
6. **Final boss (pointer)** -- the campaign's final boss arena. [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language]
   - Identity: the final boss is the Harbinger. [spoiler: story · enemy-tier: 3 · puzzle-tier: 3 · confidence: high · Confirmed: 2 sources, 1 language · entity: harbinger · entity-status: hostile · entity-hidden: yes · achievement: Too Many Goodbyes · achievement-hidden: yes · trigger_type: progression]
   > see npcs/harbinger.md for full summary
7. **Credits -> Outpost Tremonius** -- after the credits you're back at Outpost Tremonius. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium · Single source -- verify · class:community-wiki · achievement: Set a Fire in Your Heart · achievement-hidden: no · trigger_type: progression]
   - `point_of_no_return:` none

## Optional branches / shortcuts

- **Bandana Skull** -- no-Sentinel-kill condition; see entry tip 1 and `../items/skulls.md`. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high · category: easter-egg]

- **Gatecrasher (P3)** -- timed run: breach the Auditorium in under three minutes (Steam's wording). Reported method: clear the opening area and walk through the opened door within 3 minutes of spawning, ideally on Easy with the Bandana Skull and a rocket launcher carried in; replay the mission via Mission Replay. [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 2 · confidence: medium · Confirmed: 2 sources, 1 language · achievement: Gatecrasher · achievement-hidden: no · trigger_type: mastery]

## Common confusions

- "Did I lose everything I didn't finish?" -- no; the postgame overworld reopens all side content (see `ow_postgame.md`). [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high · Confirmed: 3 sources, 2 languages]

## Sources

- https://www.halopedia.org/Silent_Auditorium (EN, accessed 2026-09-28)
- https://www.halopedia.org/The_Auditorium (EN)
- https://gameranx.com/features/id/282338/article/halo-infinite-how-to-find-all-collectibles-command-spire-nexus-repository-house-of-reckoning-silent-auditorium/ (EN)
- https://steamcommunity.com/app/1240440/discussions/0/3195866872026079939 (EN, forum)
- GamePressure Harbinger boss page (EN, 2022)
- https://www.halopedia.org/Adjutant_Resolution (EN)

## Cross-system dependencies

> **Cross-system dependency** -- see `../dependencies.md` DEP-005: Achievement methods that use the Bandana Skull can only use it after collecting it in the last mission (second run or Replay). [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 2]
