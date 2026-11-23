# Chat History - ace-run (bob-cli-pj.2.1.3)

- **TIMESTAMP:** 2026-11-22 21:00:51 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-pj.2.1.3

## Prompt

%auto
#gh:gh_bobs-org__bob-cli
%id(3, clan=bob-cli-pj.2.1, bead=bob-cli-pj.2.1.3)
%model:@medium
%w(bob-cli-pj.2.1.2, for_epic=false)
%w(bead=bob-cli-pj.2.1.2)
Can you complete the work for bead bob-cli-pj.2.1.3? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-pj.2.1.3` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-pj.2.1.3` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-pj.2.1.3 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-pj.2.1.3 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-pj.2.1.3 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-pj.2.1.3`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-pj.2.1.3 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Done — bead `bob-cli-pj.2.1.3` is closed.

**What landed** (4 files, uncommitted for review):

- [`scan_apply.rs`](src/native/highlights_ref/scan_apply.rs) — the lock-window stale branch now classifies with the typed `ScanChange` while holding both locks, drops the locks before any refresh/rebuild, then reacquires in maintenance/scan order and revalidates. Refreshes consume the shared 4-pass allowance one per lock cycle; recovery and fresh-intake arrivals consume the one-rebuild allowance instead of minting a fresh budget; destination-asset staleness still fails closed with a locked `scan_failed`; hard errors after the drop stay prelock with no receipt. The obsolete budget-resetting `rebuild_prepared` is gone.
- [`scan_plan.rs`](src/native/highlights_ref/scan_plan.rs) — `refresh_prepared_once` and `full_rebuild_prepared` are now `pub(super)` for the lock path; stale doc comments updated. Also fixed a one-token `clippy::op_ref` nit from phase 1 that was failing `just lint`.
- [`scan_interleave.rs`](tests/cli/highlights/scan_interleave.rs) — two new lock-window tests (sidecar edit between prepare/lock refreshes exactly its PDF with `locked=0 count=1`; daily edit finalizes with zero reparses) and the churn test rewritten to drive all four refreshes plus the rebuild (6 plan lines, `inputs_changed`, no receipt).
- [`highlights-ref-sync.md`](docs/highlights-ref-sync.md) — new "Coherence contract" section under the writer-lock docs.

**Verified:** `cargo fmt --check` clean, `just lint` exit 0, full workspace suite 12,798 passed / 0 failed, `epic-symbols` clean. One exception: `just docs-check` fails on word-budget overruns in four untouched pages (mac-capture ×3, plugin-apis) — pre-existing on base, recorded as a `PROPOSED FOLLOW-UP` on the bead.

Declaration accepted. Bead `bob-cli-pj.2.1.3` work committed with `bead_action: close`; host completes the commit and close after this turn.
