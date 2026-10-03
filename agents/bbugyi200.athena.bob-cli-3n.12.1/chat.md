# Chat History - ace-run (bob-cli-3n.12.1)

- **TIMESTAMP:** 2026-10-02 23:47:17 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-3n.12.1

## Prompt

#gh:gh_bobs-org__bob-cli
%id(bob-cli-3n.12.1, bead=bob-cli-3n.12.1)
%clan(bob-cli-3n.12, tribe=epic, summary_script=sase_clan_summary_epic)
%model:@medium
%auto
Can you complete the work for bead bob-cli-3n.12.1? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-3n.12.1 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-3n.12.1 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-3n.12.1`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-3n.12.1 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Bead `bob-cli-3n.12.1` (hooks-correctness) is complete and closed.

**What was fixed** (all in `src/native/task_status_hooks/reconcile.rs` plus `compose.rs`):
- Same-index edits now apply Replace/Remove before Insert — ends the task-line duplication / lost-adoption bug.
- Every task-line rewrite starts from the pending rewrite, so A→B→C chains settle in one run.
- Daily notes with no status change now write their reconciled contents (adoptions/stamps were reported but dropped).
- Previous-daily targets are never stamped; unencodable targets never project — both keep the link verbatim with new named warnings.
- `set_task_fields` rebuilt on the shared `projects::edits` helpers (promoted to `pub(crate)`), so `[id::]`/`[dependsOn::]` anywhere among trailing tags is replaced, never duplicated.
- `done/` legacy children follow §4.3; R1 drops emit `dependency_field_ids_dropped`.
- Contract `docs/task-dependencies.md` updated first with the three new warning kinds.

**Verification:** 3 new unit tests + 12 new CLI regression tests (each asserting a clean second run); the 3 key tests confirmed to fail on pre-fix sources. `just all` passes (25/25 in `dependency_lines`). Real-vault dry-run: 4632 files scanned, zero projections/adoptions/heals/warnings — expected, since the vault has no Depends-On usage yet. No epic-symbol leftovers; only this bead closed.

Declaration accepted. Bead bob-cli-3n.12.1 declared complete (bead_action: close) with hooks-correctness fix committed.
