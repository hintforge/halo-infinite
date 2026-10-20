# Nav -- Lockdown overworld / Recovery (ow_lockdown)

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-10-13
**research_run:** P2 (deep-research cascade), ingested 2026-09-28

**Type:** hub (overworld region)
**Linear?:** no (open region; the story chain inside it is linear)
**Chapter:** Recovery (overworld chain) -> 4. The Tower (campaign section "Lockdown")

_source: deep-research cascade 2026-09-28 · capture: web_fetch · category: mainline unless noted · confidence per claim_

## Entry

From `z03_outpost_tremonius` via edge `(z03_outpost_tremonius, ow_lockdown)` -- see `architecture.md`. Arrival: Echo 216 drops you on an outcrop directly above FOB Golf, with the Tower looming on the horizon. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language · entity: echo_216 · entity-status: friendly]
> see npcs/echo_216.md for full summary

## Exit

To `ow_connections` via edge `(ow_lockdown, ow_connections)` -- the chasm bridge north toward the dig site opens once The Tower (z04) is complete.
**Type:** story-gate (region unlock; two-way afterward, except while Pelican Down has the region relocked)
**Point of no return:** none

## Outgoing edges

- `(ow_lockdown, z04_the_tower)` -- hub-spoke, Recovery story chain
- `(ow_lockdown, ow_connections)` -- story-gate, opens after The Tower is complete; cross the chasm bridge past the Banished blockade
- `(any FOB, any captured FOB)` -- fast-travel, once FOB Golf (or Foxtrot) is captured

## Entry tips (3 max)

1. Capture FOB Golf first -- it's directly below the drop-off outcrop, it's the story-required first FOB, and it switches on fast travel. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
2. The region's side content (FOB Foxtrot, Ransom Keep, the region's HVTs) can be done now or later -- nothing here is lost when you move on, and postgame reopens it all. See `architecture.md` Optional Content. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]
3. The tallest structure on the horizon is The Tower -- the next story objective. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]

## Sequential gates

1. **Drop-off outcrop** -- land on the outcrop above FOB Golf. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
2. **Capture FOB Golf** -- clear the Banished at FOB Golf and use its terminal; first FOB capture and first fast-travel node. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language · achievement: Reclaimer · achievement-hidden: no · trigger_type: collection]
3. **(Optional) FOB Foxtrot** -- the region's second UNSC FOB platform; an audio log leans against a container on its landing pad. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
4. **Travel to The Tower** -- head for the tallest landmark in the region; the mission hands over to `z04_the_tower`. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
5. **Chasm bridge (after The Tower)** -- cross north toward the dig site past a Banished blockade guarding a recently established bridge. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 2 sources, 1 language]
   - `lock:` story -- The Tower must be complete (see `architecture.md` Locks and Keys)

## Optional branches / shortcuts

- **Ransom Keep and the region's HVTs** -- available through this whole window; per-site detail is in `architecture.md` Optional Content and `../items/weapons.md`, not re-derived at P2; every collectible site in this region is in `../optional_zones/ow_lockdown_collectibles.md` (MapGenie, 2026-10-06; each row carries its item code and grid cell, and most items with map-site screenshots have an approach note at the end of that file); FOB and outpost cells are in `../optional_zones/index.md` "Landmarks by grid cell". [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · confidence: high]

## Common confusions

- "Lockdown" means three different things: the campaign section title, the Tower's security lockdown (a separate lock on the Tower building only), and neither of those is what keeps you out of Connections -- the chasm bridge is. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · Confirmed: 3 sources, 1 language]
- "The Tower" here is one Banished stronghold (z04), not one of the ~40 small destructible Propaganda Towers. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]

## Sources

- https://www.halopedia.org/Recovery (EN, rev. 2026)
- https://www.gamerguides.com/halo-infinite/guide/walkthrough/campaign-missions/recovery (EN, n.d.)
- https://guides.gamepressure.com/halo-infinite/guide.asp?ID=62154 (EN, 2022)
- https://www.halopedia.org/Excavation_Site (EN, accessed 2026-09-28)
- https://www.halopedia.org/HINF:Overworld (EN, accessed 2026-09-28)
- https://theloadout.com/halo-infinite/audio-log-locations (EN, n.d.)
