# Sections -- Missables

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-10-06

_source: deep-research cascade 2026-09-28 · capture: web_fetch_

## The short answer: nothing is permanently missable

Since the November 2022 Winter Update added **Mission Replay** (TacMap -> completed mission -> Mission Options -> Replay Mission), every campaign collectible and achievement can be recovered by replaying the mission that contains it -- your current loadout, upgrades, and equipment carry into the replay, and anything collected there saves permanently to your current file. See `../nav/architecture.md` "How Mission Replay restores access." [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Confirmed: 5 sources]

The list below is the **pre-replay missable window** -- useful for a first playthrough that wants to avoid backtracking, even though nothing here is a permanent loss.

## Skulls (5 of 12 are mission-bound)

| Skull | Latest safe mission | Zone-id |
|---|---|---|
| Boom | Warship Gbraakon | z01_warship_gbraakon |
| Cowbell | Foundation | z02_foundation |
| Mythic | The Command Spire | z11_command_spire |
| Grunt Birthday Party | Repository | z12_repository |
| Bandana | Silent Auditorium | z15_silent_auditorium |

Full location detail: `../items/skulls.md`. [spoiler: progression/late-game · confidence: high]

## Spartan Cores

3 of the 45 total are mission-bound, in Outpost Tremonius (z03_outpost_tremonius). MapGenie (2026-10-06) instead shows four cores in and around the outpost with none marked mission-only [Contradicted across sources -- see `../items/upgrades.md`]. [spoiler: progression · confidence: medium (contradicted)]

(P2) The Graveyards island (Pelican Down, `ow_graveyards`) holds 5 more. Whether the island can be walked or flown back to after the credits is [Contradicted across sources] (P3) -- the 5 are recoverable through Mission Replay of Pelican Down whatever the answer, so never permanently lost. See `../nav/ow_graveyards.md`. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1 · confidence: medium · Contradicted across sources -- see notes]

(P3) FOB captures are not in Mission Replay's replayable list (it names only outposts, targets and Marine events), and the Forza Veloce timer cannot be restarted on the same save -- those two are the only things Replay does not give back. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0 · confidence: high · Single source -- verify · class:official-pr]

## Audio logs

Per-mission UNSC/Banished/Spartan log counts are mission-bound where noted -- see `../items/collectibles.md` for the full per-mission table. Overall total is 104 (37 UNSC / 28 Banished / 39 Spartan); the breakdown, the Halopedia disagreement and the UNSC-vs-Spartan menu quirk are in `../items/collectibles.md`. [confidence: high]

## Achievements with a point-of-no-return window

- **Headmaster** (all 12 Skulls + Legendary difficulty across the whole campaign) -- effectively requires planning collection before a Legendary run, though Mission Replay lets you retrofit it. An older Steam-forum report warned that choosing "Continue" from the main menu turns Skulls off; the Winter Update notes say that is fixed, so it should not apply on the current build (report date unverified). [Single source, verify · class:forum / class:official-pr]
- **Forza Veloce** (14 main missions in under 8 hours) -- a timing achievement, not a collectible-loss risk; ~2.5 hours is achievable on Easy by grappling past fights. The timer cannot be restarted on the same save, so start it on a fresh save in a fresh slot (P3; see `../achievements.md` for the mission-count and timer caveats).

No achievement in P1-P3 research was found to be truly unrecoverable post-Winter-Update, other than restarting the Forza Veloce timer on the same save.

## Cross-system dependencies

> **Cross-system dependency** -- see `../dependencies.md` PON-001: Entering the Command Spire door closes the whole open world (and fast travel) until the credits -- clear overworld content first. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` DEP-009: Mission Replay carries loadout, equipment and upgrades into any completed mission, making timed and per-mission achievements replay plans. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]

> **Cross-system dependency** -- see `../dependencies.md` DEP-011: Headmaster needs all twelve Skulls on, five of them mission-bound (Replay recovers them); the Continue-versus-Load warning is superseded. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` DEP-012: Mission Replay of Pelican Down is the guaranteed way to collect the island's five cores, part of the 45 the equipment achievements need. [spoiler: progression · enemy-tier: 0 · puzzle-tier: 1]

> **Cross-system dependency** -- see `../dependencies.md` SEQ-003: Forza Veloce needs a fresh save in a fresh slot; the timer cannot be restarted on the same save. [spoiler: none · enemy-tier: 0 · puzzle-tier: 0]
