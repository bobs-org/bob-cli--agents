# Chat History - ace-run (bob-cli-df.2.1.4.3.1)

- **TIMESTAMP:** 2026-10-28 05:19:30 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-df.2.1.4.3.1

## Prompt

#gh:gh_bobs-org__bob-cli
%id(bob-cli-df.2.1.4.3.1, bead=bob-cli-df.2.1.4.3.1)
%clan(bob-cli-df.2.1.4.3, tribe=epic, summary_script=sase_clan_summary_epic)
%model:@medium
%auto
Can you complete the work for bead bob-cli-df.2.1.4.3.1? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-df.2.1.4.3.1` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything, and run `sase bead open bob-cli-df.2.1.4.3.1` only if the work
is genuinely unfinished. Read its
description and design file with `sase bead read bob-cli-df.2.1.4.3.1 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-df.2.1.4.3.1 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-df.2.1.4.3.1`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-df.2.1.4.3.1 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Done. Bead `bob-cli-df.2.1.4.3.1` is closed.

Work in `sase-core` (`f4bf6074`):
- Fixed `collision/mod.rs` to eliminate descendant occurrences, not whole digests: added `occurrence_is_eliminated`/`surviving_histories`/`best_surviving_instant`, rewrote `selection_pool`/`select_winner`/`pairwise_basis` to compare earliest surviving first-add instants, and added cross-digest same-commit instant validation.
- Added 6 regression tests in `collision/tests.rs` (main case with all 6 permutations plus root-label variations, 3-payload, interleaved duplicates, same-commit tie-break, same-commit conflict rejection, equal instants) and extended the PyO3 round-trip in `artifact_links/tests.rs` for the copy-chronology group.
- Removed collision/quarantine facades from `sase_core/src/lib.rs` and `sase_core_py/src/prelude.rs`; `artifact_links/mod.rs` now imports via `sase_core::artifact_link::*`. All binding names preserved.

Verification:
- `just test -p sase_core artifact_link`: 152 passed.
- `just test -p sase_core_py artifact_link_collision_bindings_round_trip`: 1 passed.
- `sase tool run check` fails only on 27 pre-existing clippy `disallowed std::env` errors in unrelated `bead`/`macro_catalog` files (zero overlap with changed files; tracked by `bob-cli-dh`). Recorded as `PROPOSED FOLLOW-UP` on the bead.
- `sase bead epic-symbols`: no entries.
