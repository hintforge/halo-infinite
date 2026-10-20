# Localization toolkit -- Halo Infinite (campaign)

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28
**research_run:** P2 (deep-research cascade), ingested 2026-09-28

The persona reads this file when CHECKPOINT.md's `player_position.confidence < high`. It tells the persona how to ask the player where they are, and how to map their answer to a `current_zone` in `architecture.md`.

Localization class: **hybrid** -- the overworld TacMap shows FOBs and objectives; interior missions have no map and resolve by landmark + objective waypoint.

_source: deep-research cascade 2026-09-28 · capture: web_fetch · category: mainline unless noted · confidence per row_

## Landmark → zone resolution

| Landmark / feature | Resolves to zone-id | Notes | Tags |
|---|---|---|---|
| Banished ship corridors; hangar with a Pelican held in a stasis beam | z01_warship_gbraakon | The only Banished ship interior in the game | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium] |
| First Forerunner interior; dead Spartan with the Shield Core | z02_foundation | Forerunner halls repeat in z06/z10/z11 -- this is the one before any open world | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium] |
| Elevator exit with a Spartan Core box; storage tunnel; open Cylix; crashed frigate; landing pad | z03_outpost_tremonius | | [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium] |
| Outpost Tremonius outdoors *after* the credits | ow_postgame | The same outpost is the postgame spawn point | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium] |
| Outcrop above FOB Golf; FOB Foxtrot; the Tower on the horizon; chasm bridge to the north | ow_lockdown | "Tower" here is the Banished stronghold, not a Propaganda Tower | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high] |
| Separate security building; gravity lift into the Tower; the Tower's roof | z04_the_tower | Propaganda Towers are small destructible optional objectives everywhere | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high] |
| Drawbridge over the chasm; Excavation Site between FOBs Alpha/Bravo/Charlie; waterfall northwest of FOB Echo; Armory of Reckoning outpost | ow_connections | Armory of Reckoning is not House of Reckoning (z14) | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high] |
| Cooling towers; mining laser drilling into a cliff; the laser-bored cave | z05_excavation_site | The only dig site with a laser | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high] |
| Near-identical U-shaped crucible rooms; a window into the main chamber; hatch drop; two dead Spartans | z06_conservatory | Power-seed consoles also appear in z10/z11 -- z06 is the one entered from a dig cave | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high · entity: despondent_pyre · entity-status: friendly] |
| Hunter pair at the base gravity lift; light bridge; observation platform | z07_spire | The light bridge distinguishes it from The Command Spire (z11) | [spoiler: progression · enemy-tier: 1 · puzzle-tier: 1 · confidence: high] |
| Downed Pelican; ship-graveyard marsh; three Gorespike AA guns; no FOB icons | ow_graveyards | The only region with no FOBs | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high] |
| Huge tower on a southeast island with its bridge pulled back; four objective-marked beacon towers; FOBs Hotel/Juliet/Kilo/Lima/November | ow_reformation | Beacons look like Forerunner pylons elsewhere -- only here are they objective-marked | [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high] |
| Descent below a gravity lift; gondola ride; central chamber with three crucibles | z10_nexus | Below the ring, not inside the Spire | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium] |
| Beam-shaft lift; window onto hexagonal columns being manufactured; floor portal; grapple chasm; Observation Platform with Phantoms | z11_command_spire | No light bridge (vs. z07) | [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 2 · confidence: medium] |
| Cavernous archive rooms; a distant structure on the horizon (the Silent Auditorium) | z12_repository | | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium] |
| Long fortified road with Wraiths; gate + terminal at the end | z13_the_road | | [spoiler: late-game · enemy-tier: 2 · puzzle-tier: 2 · confidence: medium] |
| Training halls with balconies; a room with a ship and a holo disc by sandbags | z14_house_of_reckoning | Not the Armory of Reckoning outpost | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high] |
| Statue halls; chamber of glowing orange portals and floating metal shapes | z15_silent_auditorium | | [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium] |

Story-tier landmark notes (lore; show only at story tier or on opt-in): z02 has an Infinity hologram sequence; z14's final room is a prisoner's cell; z15 opens in a specific ally's Pelican troop bay. See the matching `../sections/<zone>.md`. [spoiler: story · enemy-tier: 3 · puzzle-tier: 3 · category: lore · confidence: medium]

## Ask-the-player prompts

When `confidence < high` and the player asks a nav-class question, ask one of these before answering. Pick the prompt that fits what the player has volunteered.

- **"What was the last mission name shown on screen?"** -- maps straight to a zone-id via `architecture.md`'s Chapter <-> Zone table. Spanish-language names (Vandal): Buque de guerra Gbraakon (z01), Cimientos (z02), Puesto avanzado Tremonius (z03). [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium · translated from: Spanish]
  - Recuperación / La Torre (ow_lockdown / z04), Excavación (z05), Invernadero (z06), Torre (z07), Pelican abatido (ow_graveyards), La secuencia (ow_reformation). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · translated from: Spanish]
  - Nexo (z10), La torre de mando (z11); German "Haus der Abrechnung" = z14 (Spieleboom). [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium · translated from: Spanish, German]
- **"Which FOB did you capture last?"** -- Golf or Foxtrot = Lockdown; Alpha through Echo = Connections; Hotel through November = Reformation. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]
- **"Can you fast travel right now?"** -- No, and you're near a crashed Pelican: `ow_graveyards` (Pelican Down). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]
  - No, and you're indoors after the beacons: somewhere in z10-z15. [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: high]
- **"Are you outside on the ring surface or inside a structure? If inside, is it Banished (metal, red lights) or Forerunner (grey panels, glowing lines)?"** [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: medium]
- **"Do you have the Threat Sensor / Drop Wall / Thruster yet?"** -- no Threat Sensor = before or inside z04; no Drop Wall = before z06. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]
- **"What campaign section title did the game show?"** -- Ringfall (z01-z03), Lockdown, Connections, Graveyards, Reformation (The Sequence through The Command Spire), per Halopedia. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium]
  - Reckoning (z12-z14). [spoiler: late-game · enemy-tier: 0 · puzzle-tier: 2 · confidence: medium]
  - The final mission's section title names the final antagonist faction -- don't say it below story tier. It is "Endless" (z15). [spoiler: story · enemy-tier: 3 · puzzle-tier: 3 · category: lore · confidence: medium · entity: harbinger · entity-status: hostile · entity-hidden: yes]
  > see npcs/harbinger.md for full summary
- **"Can you see a huge tower on an island with its bridge pulled back?"** -- that's `ow_reformation` at the Command Spire. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]
- Fallback: "Roughly which area are you in? If you're not sure, what was the last cutscene or objective name?"

Match the player's response against the table above to resolve `current_zone`. If multiple landmarks could match, ask one disambiguating follow-up -- don't guess.

## Map-element prompts (`hybrid` games only)

For the overworld zones (TacMap: Tab on keyboard, View on controller):

- "How many FOB icons does your TacMap show, and which ones are captured?" -- 12 FOB icons total across the ring; the Graveyards island shows none. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]
- "Is there a big objective in the southeast?" -- the Command Spire sits in the southeast. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]
- "Do you see beacons marked East / South / North / West?" -- that's The Sequence (`ow_reformation`). [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: high]
- Region names: whether the TacMap itself prints "Lockdown" / "Connections" / "Reformation" is **not confirmed** -- guides use them as region labels. Don't ask the player to read a region name off the map; ask about FOBs and objectives instead. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: low · Hypothesis -- unverified]

## Sources

- https://vandal.elespanol.com/guias/guia-halo-infinite-trucos-consejos-y-secretos/historia (ES, 2025-12-26)
- https://spieleboom.com/halo-infinite-haus-der-abrechnung-komplettloesungtipps/ (DE, n.d.)
- https://www.halopedia.org/HINF:Overworld (EN, accessed 2026-09-28)
- https://www.neoseeker.com/halo-infinite/walkthrough/Forward_Operating_Bases (EN)
- Per-zone landmark sources: see each `nav/<zone>.md` Sources section.
