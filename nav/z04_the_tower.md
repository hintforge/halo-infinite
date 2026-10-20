# Nav -- The Tower (z04_the_tower)

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28
**research_run:** P2 (deep-research cascade), ingested 2026-09-28

**Type:** main-story zone (Banished stronghold: exterior + interior)
**Linear?:** yes (main or side entrance)
**Chapter:** 4. The Tower (campaign section "Lockdown")

_source: deep-research cascade 2026-09-28 · capture: web_fetch · category: mainline unless noted · confidence per claim_

## Entry

From `ow_lockdown` via edge `(ow_lockdown, z04_the_tower)` -- see `architecture.md`. The Tower is a single tall Banished stronghold -- not a Propaganda Tower. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]

## Exit

To `ow_connections` via edge `(z04_the_tower, ow_connections)` -- on foot, north across the chasm bridge. Excavation Site begins right after The Tower. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
**Type:** story-gate
**Point of no return:** none -- the Tower's roof and exterior stay reachable afterward.

## Outgoing edges

- `(z04_the_tower, ow_connections)` -- story-gate, on foot after the mission
- (the hub edge back to `ow_lockdown` is implicit: the exterior is part of the Lockdown region)

## Entry tips (3 max)

1. The Tower's security lockdown is controlled from a separate security building, not the Tower itself -- go there first. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
2. The Threat Sensor is inside; once you have it, make sure it's actually equipped (see Common confusions). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]
3. The IWHBYD Skull is on top of the Tower -- it stays reachable after the mission, so no rush. See `../items/skulls.md`. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · category: easter-egg · confidence: medium]

## Sequential gates

1. **Approach** -- reach the Tower's main entrance or a side entrance. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-wiki]
2. **Security building** -- reach the separate security building where the lockdown is controlled. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
   - `lock:` story -- Tower lockdown (see `architecture.md` Locks and Keys)
3. **Lockdown lifted** -- the Weapon lifts the lockdown. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-wiki · entity: the_weapon · entity-status: friendly]
   > see npcs/the_weapon.md for full summary
   - When it lifts, Berserkers deploy. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: medium · Single source -- verify · class:community-wiki]
4. **Gravity lift** -- enter the Tower via the gravity lift. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Single source -- verify · class:community-wiki]
5. **Threat Sensor** -- pick up the Threat Sensor inside. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language · achievement: Visionary · achievement-hidden: no · trigger_type: progression]
6. **Boss arena** -- the Tower's commander, Chak 'Lok, is fought here. Full strategy: `../npcs/chak_lok.md`. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language · entity: chak_lok · entity-status: hostile · achievement: Out with a Bang · achievement-hidden: no · trigger_type: mastery]
   > see npcs/chak_lok.md for full summary
   - Tactic: Chak 'Lok is cloaked -- the Threat Sensor (just picked up) is the relevant tool: stick it on him to keep him revealed, dodge his sword lunge with a jump, and throw the arena's shock coils to stun him. [spoiler: progression · enemy-tier: 1 · puzzle-tier: 0 · confidence: high · Confirmed: 2 sources, 1 language · entity: chak_lok · entity-status: hostile]
   > see npcs/chak_lok.md for full summary
7. **Mission end** -- the mission ends; the next objective (Excavation Site) begins right away. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language · achievement: Fallen · achievement-hidden: no · trigger_type: progression] (the retrieval scene itself is a `story` beat -- see `../sections/z04_the_tower.md`)

## Optional branches / shortcuts

- **Collectibles:** IWHBYD Skull on top of the Tower; two audio logs and one Mjolnir locker (Halopedia); one audio log on the second floor (The Loadout). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · category: easter-egg · confidence: medium]

## Common confusions

- **Threat Sensor won't equip / progression stalls (historic bug):** the official Winter Update notes (Nov 8, 2022, updated Nov 10) say the patch "Improved the Threat Sensor's unlock sequence so that it can now be equipped consistently and no longer has a chance to halt player progression." Fixed on current patch; on a very old save, check that the Threat Sensor is actually equipped. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Single source -- verify · class:official-pr (repeated verbatim by Liquipedia, TheSixthAxis, MP1st)]
- "Which tower?" -- The Tower (z04) is one Banished stronghold; Propaganda Towers are small destructible optional objectives across the overworld. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]

## Sources

- https://www.halopedia.org/The_Tower_(Halo_Infinite_level) (EN, accessed 2026-09-28)
- https://www.halopedia.org/Tower (EN)
- https://www.gamerguides.com/halo-infinite/guide/walkthrough/campaign-missions/recovery (EN)
- https://support.halowaypoint.com/hc/en-us/articles/10581554050324-Halo-Infinite-Winter-Update-November-8-2022 (EN, 2022-11-10)
- https://www.theloadout.com/halo-infinite/gear-equipment-locations (EN)
- https://theloadout.com/halo-infinite/audio-log-locations (EN)
- https://guides.gamepressure.com/halo-infinite/guide.asp?ID=62157 (EN)
- https://gamerant.com/halo-infinite-change-equipment-switch-grappleshot-threat-sensor-thruster-drop-wall/ (EN)
- https://www.sportskeeda.com/esports/all-halo-infinite-tower-collectibles-get (EN)
