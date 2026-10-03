# Chat History - ace-run (bob-cli-2c.1)

- **TIMESTAMP:** 2026-09-28 12:42:05 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-2c.1

## Prompt

#gh:gh_bobs-org__bob-cli
%id(bob-cli-2c.1, bead=bob-cli-2c.1)
%clan(bob-cli-2c, tribe=epic, summary_script=sase_clan_summary_epic)
%model:@medium
%auto
Can you complete the work for bead bob-cli-2c.1? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-2c.1 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-2c.1 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-2c.1`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-2c.1 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Done. Bead `bob-cli-2c.1` (start_core) is implemented, verified, and closed.

Result: whole-item `=`/`=<X>` capture items now start today's next future Pomodoro with `se<X>` timing, atomically through the staged batch planner.

- [capture_language.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/src/native/capture_language.rs): shared `session_equals_token` lexer; `parse_pomodoro_close_item` reworked into the `=`-family parser emitting `CaptureKind::PomodoroClose` (unchanged) or new `CaptureKind::PomodoroStart`; token-echoing shape error; `POMODORO_START_FORCED_ERROR`; deleted `POMODORO_CLOSE_INCOMPLETE_ERROR`; `EditorMode::PomodoroStart` variant plus label for parity (editor recognition left to `editor_contract`).
- [capture_pomodoros.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/src/native/capture_pomodoros.rs): `next_future_pomodoro` helper, adopted in the link-start path and the close "next up" lookup.
- [capture.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/src/native/capture.rs): dispatch arm, `plan_pomodoro_start_item` with the five ordered guards and exact error copy, `Placement::Started`, `pomodoro_start` JSON/human output (`tasks` omitted until `start_lineup`), and `(start it with `=`)` hints on the `=x`/`+`/`++` nothing-running errors.
- [tests/cli.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/tests/cli.rs): 5 new tests (suffix table, selection/move/CRLF, all guards, shape/forced/prose/argv/hints, batch composition and rollback); updated the stale `=3`-is-a-task and `=`-incomplete assertions.

Verified: full `cargo test` green (1029 lib + 511 cli), `cargo clippy` shows only pre-existing warnings, `cargo fmt --check` clean. One transient failure of `missing_note_and_missing_section_are_warning_successes` appeared once and passed on two reruns; recorded as a `PROPOSED FOLLOW-UP` on the bead (likely `with_env` race under parallel test threads).
