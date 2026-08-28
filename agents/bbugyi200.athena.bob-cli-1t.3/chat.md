# Chat History - ace-run (bob-cli-1t.3)

- **TIMESTAMP:** 2026-08-28 13:17:27 EDT
- **MODEL:** grok/grok-4.6
- **AGENT:** bob-cli-1t.3

## Prompt

#gh:gh_bobs-org__bob-cli
%id(3, clan=bob-cli-1t, bead=bob-cli-1t.3)
%model:@medium
%auto
%w:bob-cli-1t.1
%w(bead=bob-cli-1t.1)
Can you complete the work for bead bob-cli-1t.3? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file, do the work, and close only this bead with
`sase bead close bob-cli-1t.3 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-1t.3`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-1t.3 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads.

## Response

I'll start by reading the bead, its design, and the SASE bead/memory rules so the work matches the phase contract.

The bead is the pomodoro-name write command. Next I’ll read the plan, glossary, and the prior phase so the implementation stays on contract.

The plan was truncated before Phase 3. I’ll pull that section and the existing capture-pomodoro code next.

Phase 3 is the `bob capture-pomodoro-name` write command. I’ll model it on `capture-task-id` and inspect the existing scanner, CLI wiring, and tests.

I have the contract: a `capture-task-id`-shaped write that canonicalizes the name and atomically appends it. Next I’ll add the command, wire it in, and cover it with tests.

The CRLF unit test raced on `BOB_DAY_FILE` with a parallel test. I’ll inject the daily-note path in tests so they no longer share that environment variable.

Closed **bob-cli-1t.3**. `bob capture-pomodoro-name` is in place as the picker-facing write that names one open Pomodoro.

The command takes required `-p/--pomodoro-ref` and `-n/--name`, canonicalizes the name (trim, collapse whitespace, ASCII-uppercase, same title grammar as task sections), and appends ` — NAME` to the resolved physical line through one same-directory temp file plus rename. An untypeable existing name is repaired by replacing that em-dash tail instead of stacking a second one. `--dry-run` returns the same success shape without writing. Stale, ambiguous, completed, already-named, missing-note, and missing-section cases fail with `{"ok": false, "error": "..."}` and do not touch the file.

Docs, README, top-level help, and `justfile` `install-smoke` all include the new command.

Verified:
- `cargo fmt --check`
- `cargo clippy --all-targets --all-features`
- `cargo test`
- Scratch daily note: exactly one placeholder line changed; `bob capture-pomodoros -f json` then reported `DEEP WORK` / `deep-work`

No leftover `--epic-symbol` entries. The parent epic was not closed.
