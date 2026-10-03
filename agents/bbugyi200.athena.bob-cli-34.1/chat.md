# Chat History - ace-run (bob-cli-34.1)

- **TIMESTAMP:** 2026-10-01 00:08:30 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-34.1

## Prompt

#gh:gh_bobs-org__bob-cli
%id(bob-cli-34.1, bead=bob-cli-34.1)
%clan(bob-cli-34, tribe=epic, summary_script=sase_clan_summary_epic)
%model:@medium
%auto
Can you complete the work for bead bob-cli-34.1? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-34.1 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-34.1 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-34.1`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-34.1 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Bead bob-cli-34.1 (decay-core) is done and closed.

What landed in the linked `bob-plugins` repo (no UI changes, per phase scope):

- Config grammar: `decay`/`rolls` on priority properties with `normalizePriorityDecayConfig` and `getPriorityLevelRollLimit`. Absent/`true`/`{}` → enabled with 1 roll; `false` → disabled; unknown `decay` keys and bad `rolls` values invalidate the config with a named notice; `decay`/`rolls` on non-priority properties is rejected. Levels gain frozen `rolls` (`null` when unset), properties gain frozen `decay`.
- Streak reader: `classifyScheduleLogRollReason` (roll/randomize/decay/other) plus `countPriorityRollStreak` and `getPriorityRollStreak`, which walks direct Schedule Log children newest-first, skips `randomize`, and stops on decays, re-picks, typed reasons, or unparseable bullets.
- `rollPriorityRecommendationDate`: uniform roll from the window minus the current date's offset, only when the offset is inside a multi-day window; otherwise identical to the existing roll.
- Planner and formatters: `planPriorityRollRecommendation` (roll/decay/cancel/unavailable, with derived streak/value/recurring from content when passed), `formatPriorityDecayScheduleReason` (`🎲 P2 → P3 decay · …`), `formatPriorityDecayCancelReason` (`🍂 decayed past P4 [after N rolls]`), and `buildPriorityRollPreviewModel` with the exact icon/tone/action/date/meta/footer/aria copy for all five kinds.
- Tests: new `scripts/test-navigation-roll-decay.cjs` covers all 15 conformance vectors verbatim plus grammar, nesting/legacy-label edge cases, and preview copy; registered in `package.json`'s `test` script. Updated one existing config-shape expectation in `test-navigation-hotkeys.cjs` for the new `decay`/`rolls` fields.

Verified: new file 13/13 pass; full `npm test` 958 pass, 0 fail; `bob plugins sync` deployed (9 copied); `sase bead epic-symbols` shows no leftovers. The bob-cli checkout itself is untouched.

Declaration accepted. Bead bob-cli-34.1 work (priority decay core in `bob-plugins`) committed via `keep` (bead already closed; host is the closer).
