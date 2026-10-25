# Chat History - ace-run (bob-cli-an.6.6.6.5.6.5.5.6.5)

- **TIMESTAMP:** 2026-10-25 08:59:22 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-an.6.6.6.5.6.5.5.6.5

## Prompt

#gh:gh_bobs-org__bob-cli
%id(5, clan=bob-cli-an.6.6.6.5.6.5.5.6, bead=bob-cli-an.6.6.6.5.6.5.5.6.5)
%model:@small
%auto
Can you complete the work for bead bob-cli-an.6.6.6.5.6.5.5.6.5? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Check
whether the earlier work landed before redoing anything, and run `sase bead open bob-cli-an.6.6.6.5.6.5.5.6.5` only if the work
is genuinely unfinished. Read its
description and design file with `sase bead read bob-cli-an.6.6.6.5.6.5.5.6.5 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-an.6.6.6.5.6.5.5.6.5 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-an.6.6.6.5.6.5.5.6.5`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-an.6.6.6.5.6.5.5.6.5 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Done. Bead `bob-cli-an.6.6.6.5.6.5.5.6.5` (migrate-snapshot-prune, `bob-cli-c2`) is closed.

What changed: all `ref_library` snapshot walkers now prune `.git` during traversal instead of reading it and filtering afterwards. `migrate_tasks.rs` had the reported walk-then-filter race; `show.rs`, `list.rs`, `find.rs`, and `today.rs` got the same one-line guard for consistency (`rename.rs` and `mod.rs` already had it). Also replaced `migrate_zorg.rs`'s silent read-error skip — a macOS portability band-aid from `1d1b8fec` — with `expect`, since swallowing `NotFound` on work-tree files would mask real writes. No test compared raw `.git` bytes, so no `rev-parse` substitution was needed. No `support.rs` changes; the six edited files stay disjoint from the parallel phases.

Verification: `cargo test --test cli ref_library` green 4 times including 3 runs at `--test-threads=64` (132 passed each), then full `just check` exit 0. No `--epic-symbol` leftovers.

Declaration submitted: commit of the six `ref_library` test files with bead close.
