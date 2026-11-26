# Chat History - ace-run (bob-cli-qp.5)

- **TIMESTAMP:** 2026-11-26 16:17:13 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-qp.5

## Prompt

%auto
#gh:gh_bobs-org__bob-cli
%id(5, clan=bob-cli-qp, bead=bob-cli-qp.5)
%model:@medium
%w(bob-cli-qp.3,bob-cli-qp.4, for_epic=false)
%w(bead=bob-cli-qp.3)
%w(bead=bob-cli-qp.4)
Can you complete the work for bead bob-cli-qp.5? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-qp.5` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-qp.5` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-qp.5 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-qp.5 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-qp.5 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-qp.5`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-qp.5 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Done — bead `bob-cli-qp.5` is closed.

Ref Card reading-state readouts are implemented in the bob-plugins repo: [249u-plugin-ref-note-card-readouts.js](sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/249u-plugin-ref-note-card-readouts.js) now subscribes each mounted card to the shared `bob ref list` snapshot and patches the lane chip (every status, snoozed wording reused from the Reading Board, `⚠ Status conflict` with bob's message), priority glyph and TODAY pill on open lanes, vN chip with `earlier[]` tooltip, arXiv/DOI copy chips, annotation counts with a Highlights jump, foot lint lines, and a missing-PDF chip drop. The host ([249s](sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/249s-plugin-ref-note-card-host.js)) paints readouts after every build, folds the readout digest into the rebuild signature, and subscribes per mounted path so the last unmount releases the shared snapshot. New [16-test suite](sase/repos/linked/bob-plugins/scripts/test-ledger-tools-ref-note-card-readouts.cjs) proves the chips, jumps, single-subscription lifecycle, and zero spawns; the stale `ref-list.json` fixture was refreshed to the real envelope and is decoded in-test.

Verified: `npm run build`, `build:check`, focused ref/board suites (101 pass), `docs:check`, inventory check, and `test:perf` all green. Full `test:unit` had one unrelated failure — the frees-marks 25 ms CPU-budget assertion, which passes isolated on both this tree and the clean base; recorded as a follow-up on the bead. No memory notes edited (only go-live may). `bob plugins sync` was refused by another checkout's in-progress vault deploy, so no `-F`; the deploy stays pending for the land/go-live agents.

Declaration accepted — `sibling:bob-plugins` work committed (bead left as-is, already closed).
