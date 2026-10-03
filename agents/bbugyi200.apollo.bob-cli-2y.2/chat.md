# Chat History - ace-run (bob-cli-2y.2)

- **TIMESTAMP:** 2026-09-30 17:11:34 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-2y.2

## Prompt

#gh:gh_bobs-org__bob-cli
%id(2, clan=bob-cli-2y, bead=bob-cli-2y.2)
%model:@medium
%auto
Can you complete the work for bead bob-cli-2y.2? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-2y.2 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-2y.2 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-2y.2`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-2y.2 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Bead bob-cli-2y.2 (hooks-sticky) is done and closed.

What changed: `task_transition` now takes `is_daily_note` — an unlinked Next outside daily notes stays Next (never counted as `kept_next`), while a daily-note Next still clears unless directly recent. The area/project In Progress rollback is deleted (`Transition::ClearInProgress` gone; `cleared_in_progress` stays as an always-empty JSON compatibility list). Promotion, derived Blocked, and recovery ranks are untouched.

Verified: full `cargo test` green (2125 passed, 0 failed), `cargo fmt --check` clean. Simulated next-day dry run on the real vault: installed bob cleared 25 / cleared_in_progress 48 (matching the report), new build clears 0 / `[]` with identical marked_next 0, marked_blocked 0, unblocked 24. A scratch-vault demo confirmed the carve-out: only the daily-note stale clears, promotion unchanged. Docs (`docs/task-status-hooks.md`, `README.md`) updated; new decision records `task-lanes-are-sticky` and `today-is-read-from-the-ledger` added, `now-tag-is-user-owned` superseded, `task-status-is-derived` superseded-in-part; `sase memory init --check` clean; no epic-symbols.

One finding: `cargo clippy --all-targets` fails on a pre-existing deny-error (`|| true` in untouched `tests/cli/capture/pomodoro_name.rs:808`, identical in HEAD). Recorded as a `PROPOSED FOLLOW-UP` on the bead; it does not affect this phase. Changes are uncommitted in the working tree for the epic land agent; no vault writes were made (dry-run only).

Declaration accepted. Bead bob-cli-2y.2 closed with commit; host will preserve the work after this turn.
