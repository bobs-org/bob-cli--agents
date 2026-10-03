# Chat History - ace-run (bob-cli-2k.2)

- **TIMESTAMP:** 2026-09-29 14:16:20 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-2k.2

## Prompt

#gh:gh_bobs-org__bob-cli
%id(2, clan=bob-cli-2k, bead=bob-cli-2k.2)
%model:@medium
%auto
Can you complete the work for bead bob-cli-2k.2? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-2k.2 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-2k.2 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-2k.2`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-2k.2 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Bead bob-cli-2k.2 closed.

What was built (selection-grammar phase):

- New shared lexer `src/native/capture_language/close_selection.rs` (`lex_close_selection`), used by both execution and editor parsers so `bob capture` and `capture-parse` agree on every message and byte range.
- `PomodoroCloseSpec` now carries sorted `in_progress` (`None` when `<N>` omitted, `[]` for `=x0`) and `complete`; plain `=x` serializes as `in_progress: null, complete: []`.
- New `pomodoro_close_in_progress` / `pomodoro_close_complete` spans (`=x1,3!2` → `[0,2) [2,5) [5,7)`) and the `pomodoro_close_task` need.
- Precise `invalid_pomodoro_close` diagnostics for every contract row (duplicates, overlap, misplaced `0`, `0`-in-`!`, empty elements, double `!`, bad characters, overflow, no-spaces hint, shape errors), and `incomplete` + partial spec + placeholder span for dangling `,`/`!`.
- Wired into whole-item closes and `@`/`^`/body-bearing `=x` suffixes; `@@` still skips closes; completion returns empty success inside selections; rewrite never touches them.
- Executor refuses selection-bearing closes (`task numbers after `=x` are not supported by this build yet`) until selection-capture wires them in; capture-parse/complete/rewrite help updated. Untouched per scope: `bob capture --help`, `docs/capture.md`, `README.md` (selection-docs' job).

Verification: `cargo fmt --check` clean; full `cargo test` green (1147 lib + 523 CLI, including new lexer unit tests and the `capture_parse_pomodoro_close_selection_protocol` suite); clippy has zero new warnings versus base (base fails identically — recorded as a `PROPOSED FOLLOW-UP` note). `sase bead epic-symbols` showed no leftover entries.

Declaration submitted: commit for bead bob-cli-2k.2 with `bead_action: close`.
