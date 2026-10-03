# Chat History - ace-run (bob-cli-31.1)

- **TIMESTAMP:** 2026-09-30 19:57:35 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-31.1

## Prompt

#gh:gh_bobs-org__bob-cli
%id(bob-cli-31.1, bead=bob-cli-31.1)
%clan(bob-cli-31, tribe=epic, summary_script=sase_clan_summary_epic)
%model:@medium
%auto
Can you complete the work for bead bob-cli-31.1? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-31.1 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-31.1 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-31.1`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-31.1 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Bead **bob-cli-31.1 (fresh-core) is closed**.

What landed:

- [docs/freshness.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/docs/freshness.md) — the contract both implementations cite: definition, fields/overrides/config, placement rules 1–6, evaluation, who-stamps table, review ritual, `bob freshness` placeholder, Surfaces table, and the P1–P17 / S1–S15 conformance vectors. Indexed in `docs/README.md`; short paragraph + docs-table row in `README.md` (command-table row left for fresh-cli per the plan).
- `src/native/freshness/placement.rs` — `stamp_fresh` / `set_refresh` / `read_freshness` / `tasks_suffix_start`, built on `task_fields::inline_fields` (no third lexer), with `NotTask`/`Recurring`/`Closed` refusals.
- `src/native/freshness/state.rs` — pure evaluator (NEW/RESURFACED/STALE/FRESH, RESURFACED beats STALE), task→note→config→default interval precedence, `queue` (NEW by path/line, DUE by due_on/path/line) and `counts` with the budget meter.
- `src/native/config/freshness.rs` — `FreshnessConfig` modeled on `plan.rs` (mistyped block stays isolated from other loaders), wired into `RawConfig`; registered in `src/native.rs`.
- Tests: one per P vector (17) and S vector (15), parse-invariance across all vectors through both `parse_details` (Dataview) and `task_metadata` (hooks), plus a hooks test (Blocked signals survive stamping; checkbox swap preserves `fresh`). Minimal `pub(crate)` visibility bumps only.

Verification observed: 45 freshness + 7 config tests pass; full `cargo test` green (1394 lib + all integration suites, 0 failures); `cargo fmt --check` clean; lib clippy clean. `cargo clippy --all-targets` fails on a **pre-existing** deny error in untouched `tests/cli/capture/pomodoro_name.rs:808` (`|| true`) that reproduces identically on the clean base tree — recorded as a `PROPOSED FOLLOW-UP` on the bead per the phase instructions. `sase bead epic-symbols` showed no leftovers.

Declaration accepted for bead bob-cli-31.1 (commit with bead_action close). Ending turn for host commit.
