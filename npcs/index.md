# Halo Infinite -- NPCs

**status:** research-integrated <!-- scaffold | research-integrated | live-observed | reconciled -->
**last_reconciled:** 2026-09-28
**class:** npcs

## Why this file exists

This file is the corpus's roster for the named entities in this class -- the player-facing index of "who / what is in this class, and where do I read about each one." For `npcs/`, the class covers any named individual NPC regardless of `entity-status` (hostile, friendly, convertible, party, neutral); hostility is a state, not a class identity. For `factions/`, the class covers group entities the player has a relationship with. For `crew/`, role-aggregated entities in run-bound or party-bound contexts. For `reputation/`, reputation tracks or alignment surfaces that warrant their own aggregation.

The reader consults this file when the player asks roster-shaped questions ("who can I recruit," "what factions are there"); per-entity detail lives in `<class>/<entity-id>.md`.

## Roster

One row per entity. Columns: `entity-id` (the slug used by the `entity:` overlay), `display name`, `entity-status` (for `npcs/` only -- `unspecified` otherwise), `status` (scaffold | research-integrated), `first-encounter zone`, `missable` (yes | no | scenario-locked). The roster reflects the corpus's current entity coverage; new entries get appended at ingestion-time.

| entity-id | display name | entity-status | status | first-encounter zone | missable |
|---|---|---|---|---|---|
| [tremonius](tremonius.md) | Tremonius | hostile | research-integrated | z02_foundation | no |
| [jega_rdomnai](jega_rdomnai.md) | Jega 'Rdomnai | hostile | research-integrated | z14_house_of_reckoning | no |
| [escharum](escharum.md) | Escharum | hostile | research-integrated | z14_house_of_reckoning | no |
| [harbinger](harbinger.md) | the Harbinger | hostile (entity-hidden: yes) | research-integrated | z15_silent_auditorium | no |
| [despondent_pyre](despondent_pyre.md) | Despondent Pyre | friendly | research-integrated | z06_conservatory | no |
| [echo_216](echo_216.md) | Echo 216 | friendly | research-integrated | z01_warship_gbraakon | no |
| [the_weapon](the_weapon.md) | the Weapon | friendly | research-integrated | z02_foundation | no |
| [adjutant_resolution](adjutant_resolution.md) | Adjutant Resolution | hostile | research-integrated | z07_spire | no |
| [chak_lok](chak_lok.md) | Chak 'Lok | hostile | research-integrated | z04_the_tower | no |
| [bassus](bassus.md) | Bassus | hostile | research-integrated | z05_excavation_site | no |
| [tovarus_hyperius](tovarus_hyperius.md) | Tovarus and Hyperius (one combined entity) | hostile | research-integrated | ow_graveyards | no |

## No entity overlay (deliberate; P1, re-checked P2 and P3 2026-09-28)

Named hostiles that appear in research but do **not** get a per-entity file, because the research surfaced only a one-line mention or a single registry row, not the paragraph of strategy/relationship depth the named-individual rule requires (see the claim-format template in the Hintforge builder repo, "When entity: applies"). They stay on the generic `enemy` vector in `../mechanics.md`. Promote any of these to a per-entity file if later research surfaces real strategy or narrative depth. The research cascade is complete; P3 settled the boss candidates (below).

- All 15 named High Value Targets (Inka 'Saham, Thav 'Sebarim, Okro 'Vagaduun, Bipbap, Briglard, Barroth, Zeretus, Balkarus, En'Geddon, Ik'Novus the Devourer, Arthoc, Writh Kul, Skimmer Patrol/Alpha, Myriad, Ordo 'Mal) -- each has only a location/variant/behaviour table row. See `../items/weapons.md`.
- **Promoted at P3 (model analysis -- 2026-09-28):** Chak 'Lok, Bassus, and Hyperius/Tovarus. P3 gave each a full paragraph of strategy (two sources for Chak 'Lok, four for Bassus, six-plus dedicated guides for the pair), which is the named-individual rule's "paragraph of strategy detail" test. The P3 result itself recommended only the pair; extending the same test to Chak 'Lok and Bassus is this session's call. Hyperius and Tovarus share one file, `tovarus_hyperius`, because they are fought as a unit. See [chak_lok](chak_lok.md), [bassus](bassus.md), [tovarus_hyperius](tovarus_hyperius.md).
- **Promoted at P2:** Adjutant Resolution -- still almost no strategy detail, but P2 shows him recurring across three missions (Spire, The Command Spire, Silent Auditorium) with a changing relationship, which is the rule's "recurring named antagonist" case. See [adjutant_resolution](adjutant_resolution.md). (model analysis -- 2026-09-28)

> **Design note (zipper, 2026-09-29):** per-entity files repeat, in summary, claims that also live in `../sections/` and `../nav/` zone files. That is the entity-overlay design (primary home plus an aggregated summary with a cross-ref); do not merge them.

## Pointer rules

- Per-entity detail lives in `<class>/<entity-id>.md`. The reader opens those files for entity-shaped questions; this file is the index, not the answer surface.
- Claims about an entity continue to route to their primary-vector destination (per step 4 of the Hintforge builder's ingestion procedure). The entity overlay aggregates the claim into the per-entity file in parallel.
- Hidden entities (`entity-hidden: yes`) keep their full content in the per-entity file; read-time tier gating handles concealment.

## Sources

- [Per-entity source citations live in the per-entity files, not here.]
