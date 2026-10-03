# Chat History - ace-run (bob-cli-28.3)

- **TIMESTAMP:** 2026-09-27 12:21:27 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-28.3

## Prompt

#gh:gh_bobs-org__bob-cli
%id(3, clan=bob-cli-28, bead=bob-cli-28.3)
%model:@medium
%auto
%w:bob-cli-28.2
%w(bead=bob-cli-28.2)
Can you complete the work for bead bob-cli-28.3? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-28.3 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-28.3 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-28.3`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-28.3 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Bead bob-cli-28.3 is closed.

Implemented the editor contract for solo `@route:id` / `^route:id` Pomodoro links:

- [capture_language.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/src/native/capture_language.rs): `pomodoro_link` mode for complete solo items of either spelling, new `active_task_route` / `active_task_block_id` spans, `active_task` need, `invalid_pomodoro_link` diagnostics for near misses and conflicts, `active_task` completion context with suffix-preserving replacement ranges, solo-`@` parse/capture agreement fix.
- [capture_complete.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/src/native/capture_complete.rs): `active_task` candidates backed by the discovery module (queued-first ordering, prefix ranking, `pomodoro: null` when unqueued), human rows, `#name` completion after `^`, empty success inside `=<X>`.
- Rewrite needed no code change: `pomodoro_link` was already non-absorbable; verified both spellings emit the specified notice and `^` items are never rewritten.
- Help (`capture`, `capture-complete`, `capture-parse`) and docs (`docs/capture.md` grammar table, new "Linking and starting existing tasks" section, kind list, editor-marker/parse/complete/rewrite sections; `README.md` summary) updated.

Verification observed: `cargo fmt --check` clean, `cargo clippy --all-targets --all-features` exit 0 with no new warnings, full `cargo test` green (921 lib + 485 cli), `sase bead epic-symbols` reports no leftovers. New tests: 6 parse unit tests, 4 completion unit tests (plus a `BOB_DAY_FILE` race guard shared with the 2 pre-existing users), 2 rewrite notice rows; one pre-existing expectation (`@dev:id` → `pomodoro_link`) updated for the intended behavior change.

Declaration accepted for bead bob-cli-28.3 (commit, close).
