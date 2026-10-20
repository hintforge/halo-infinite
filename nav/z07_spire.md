# Nav -- Spire (z07_spire)

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28
**research_run:** P2 (deep-research cascade), ingested 2026-09-28

**Type:** main-story zone (exterior arena at the base, Forerunner interior above)
**Linear?:** yes
**Chapter:** 7. Spire (campaign section "Connections") -- not "The Command Spire" (z11)

_source: deep-research cascade 2026-09-28 · capture: web_fetch · category: mainline unless noted · confidence per claim_

## Entry

From `ow_connections` via edge `(ow_connections, z07_spire)` -- see `architecture.md`. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]

## Exit

To `ow_graveyards` via edge `(z07_spire, ow_graveyards)` -- a scripted exit from the Spire leads straight into Pelican Down. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
**Type:** story-gate
**Point of no return:** chapter-bound -- Pelican Down follows immediately and relocks Lockdown and Connections until it's done.

## Outgoing edges

- `(z07_spire, ow_graveyards)` -- story-gate, automatic on mission end
- `(TacMap, z07_spire)` -- conditional (Mission Replay), only after completion

## Entry tips (3 max)

1. Before you commit: finishing the Spire starts Pelican Down, which relocks Lockdown and Connections and has no FOBs -- restock at a FOB and wrap up any Connections side content you want first. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
2. The base of the Spire is an exterior fight with Ghost patrols and a Hunter pair guarding the gravity lift -- vehicles and cover help. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language · achievement: Hunter. Killer. · achievement-hidden: no · trigger_type: progression]
3. This Spire has a light bridge inside; The Command Spire (z11) does not -- a quick way to tell the two apart. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high · Confirmed: 2 sources, 1 language]

## Sequential gates

1. **Spire base** -- reach the area beneath the Spire; Banished patrol in Ghosts. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:editorial-en]
2. **Hunter pair at the gravity lift** -- defeat the two Hunters guarding the base gravity lift. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
3. **Gravity lift + light bridge** -- ride the lift in, cross the light bridge, pass platforms and a viewscreen. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-wiki]
4. **Escort to the elevator** -- follow your escort to the elevator and up to an observation platform. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language] (who the escort is, is a `story` beat -- see `../sections/z07_spire.md`)
5. **Release terminal** -- use the Weapon's release terminal. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language · entity: the_weapon · entity-status: friendly]
   > see npcs/the_weapon.md for full summary
   - Boss pointer: **Adjutant Resolution** (first of two fights). [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: high · Confirmed: 3 sources, 1 language · entity: adjutant_resolution · entity-status: hostile]
   > see npcs/adjutant_resolution.md for full summary
   - Tactic: the area transforms and pillars rise -- use them as cover. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: high · Confirmed: 3 sources, 1 language · entity: adjutant_resolution · entity-status: hostile]
6. **Jump off the Spire** -- the mission exits with a free-fall jump; Pelican Down begins (what happens next is a `story` beat -- see `../sections/z07_spire.md`). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-wiki]
   - `point_of_no_return:` chapter-bound

## Optional branches / shortcuts

- **Collectibles:** 2, both in the open world at the base, outside the interior: 1 UNSC audio log and 1 Spartan Core; none found inside the interior (web research 2026-10-11, `../sections/z07_spire.md`). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Confirmed: 3 sources, 1 language]

## Common confusions

- "Spire" (z07, in Connections, with a light bridge inside) is **not** "The Command Spire" (z11, in Reformation, reached by gravity lift). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
  - The Command Spire has no light bridge -- you grapple across instead. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high · Confirmed: 2 sources, 1 language]
- **Co-op replay soft-lock (P1):** skipping the cutscene after the final terminal in co-op Mission Replay can soft-lock players -- don't skip it. See `../sections/z07_spire.md`. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium]

## Sources

- https://www.halopedia.org/Spire_(Halo_Infinite_level) (EN, accessed 2026-09-28)
- https://www.gamerguides.com/halo-infinite/guide/walkthrough/campaign-missions/spire (EN)
- https://www.gamepressure.com/halo-infinite/spire/z1f2ed (EN, 2022)
- https://www.halopedia.org/The_Command_Spire (EN)
- https://vandal.elespanol.com/guias/guia-halo-infinite-trucos-consejos-y-secretos/historia (ES "Torre", 2025-12-26)
