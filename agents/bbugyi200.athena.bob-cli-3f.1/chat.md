# Chat History - ace-run (bob-cli-3f.1)

- **TIMESTAMP:** 2026-10-01 18:17:47 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-3f.1

## Prompt

#gh:gh_bobs-org__bob-cli
%id(bob-cli-3f.1, bead=bob-cli-3f.1)
%clan(bob-cli-3f, tribe=epic, summary_script=sase_clan_summary_epic)
%model:@medium
%auto
Can you complete the work for bead bob-cli-3f.1? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-3f.1 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-3f.1 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-3f.1`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-3f.1 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Bead bob-cli-3f.1 core is complete and closed.

What landed:
- `plan.max_ready_per_note` (1–999, default 5) with validation, getter, and unit tests in [plan.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/src/native/config/plan.rs).
- Area/project classifier now accepts quoted, bare, flow-list, and block-list `type` forms, plus `walk_typed_notes` in [scan.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/src/native/projects/scan.rs).
- New `src/native/note_ready/` pure evaluator + freshness-snapshot scan with R1–R14 tests (17 pass).
- `docs/plan.md` "Ready cap per note" contract, vectors, lints, and config.
- Decision `note-ready-cap-counts-the-lane` with `ready-is-freshness-gated` marked superseded-in-part; `sase memory init` regenerated shims.

Verified: `cargo fmt --check` clean, full `cargo test` green, `cargo clippy --all-targets --all-features` exit 0 (warnings only). No `--epic-symbol` leftovers.
