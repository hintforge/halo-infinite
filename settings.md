# Halo Infinite -- Settings

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28

Settings that affect difficulty or comfort. _source: deep-research cascade 2026-09-28 · capture: web_fetch_

## Difficulty (Easy / Normal / Heroic / Legendary) and Skulls

Four difficulty tiers: Easy, Normal, Heroic, Legendary. Skulls (see `items/skulls.md`) are set per session or per Mission Replay run, independent of difficulty; turning Skulls on does not disable achievement progress. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 5 sources]

### Lowering difficulty mid-campaign (web research 2026-09-29)

_source: web research 2026-09-29 (search summary of PCGamesN, GameRant, Twinfinite, TrueAchievements pages; none fetched)_

- Difficulty can be changed during the campaign and the save is rewritten with the new level; progress is kept. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · Single source (search summary) -- verify · class:editorial-en]
- Cost: lowering it fails Bare Your Fangs (Normal or higher, never lowered) for that run, and missions finished on the lower setting do not count toward Fight Hard, Die Well (every mission on Heroic). Difficulty achievements can be earned later by replaying missions on the higher setting (`nav/ow_postgame.md`). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · Single source (search summary) plus this corpus's `achievements.md` -- verify · class:editorial-en]
- The menu path for changing it was not captured; look under the campaign's difficulty setting.

## Launching into the Campaign menu (web research 2026-10-09)

_source: web research 2026-10-09 (search summaries of the Halo Waypoint "Guide to Halo Infinite Menus" support page and a community startup-video guide; Waypoint page fetch returned 403, so nothing was read first-hand)_

- The game opens on the Play menu; Campaign is reached from there, with a loading screen before the Campaign menu. Since Season 4 the Campaign menu runs independently of the Multiplayer experience, which is why that load exists. No setting or Steam launch option that makes Campaign the default landing screen was found in either search. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: low · Single source (search summary) -- verify · class:official-support]
- Closest workaround found: the logo video can be skipped by replacing or removing `intro.mp4` in the game's `videos` folder (Steam > Browse Local Files). This skips the intro only, not the menu after it. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: low · Single source (community guide, gamepretty.com) -- verify · class:community-guide]

## FOV and motion blur

- **FOV:** uses a horizontal FOV scale. Change this first if motion-sick (Shacknews). A higher FOV shrinks distant targets, which interacts with controller aim assist. Most guides suggest **~90-110** (closer to 110 on mouse and keyboard). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 4 sources]
- **Motion blur:** a slider under Sensory Effects. No measured performance impact (Digital Trends); most guides recommend disabling it for clarity. [confidence: high · Confirmed: 3 sources]

## Controller deadzones / aim assist / sensitivity curves

See `controls.md` "Controller" for the recommended deadzone/vibration/crouch/clamber settings.

## HUD, subtitles, colorblind options

Not covered by P1 research, nor by P2 (the navigation pass), nor by P3 (not reached). [The cascade is finished; fill from live observation.]

## Network co-op and mission replay options

- **Screen calibration:** access during the campaign was restored by the Winter Update. [Confirmed: 1 official source]
- **Co-op setup (P3):** the Fireteam Leader (crown icon) picks a save and sets difficulty and Skulls, then presses Start Co-Op; each other member picks their own save; the leader presses Start Game. Exact menu tab names were not confirmed. Which Skulls the leader can enable is [Contradicted across sources] (union vs. intersection of members' unlocks) -- see `mechanics.md` "Campaign co-op". [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · Single source -- verify · class:official-pr (setup) · Contradicted across sources -- see notes (Skulls)]
- **Known co-op issue:** in co-op Mission Replay, skipping the cutscene after the Spire mission's final terminal can soft-lock players. [Confirmed: 1 official source · spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]
- Mission Replay itself is documented in `nav/architecture.md` "Fast-travel network," not here (it's a navigation mechanic, not a settings-menu item).
