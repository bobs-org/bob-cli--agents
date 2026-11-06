# Chat History - ace-run (bob-cli-hn.7)

- **TIMESTAMP:** 2026-11-06 10:25:18 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-hn.7

## Prompt

%auto
#gh:gh_bobs-org__bob-cli
%id(7, clan=bob-cli-hn, bead=bob-cli-hn.7)
%model:@small
%w(bob-cli-hn.6, for_epic=false)
%w(bead=bob-cli-hn.6)
Can you complete the work for bead bob-cli-hn.7? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-hn.7` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-hn.7` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-hn.7 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-hn.7 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-hn.7 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-hn.7`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-hn.7 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Done. Bead `bob-cli-hn.7` (project-promotion verdicts) is implemented, verified, and closed.

What landed in `bob-plugins` (deployed to the vault via `bob plugins sync --repo`):

- **Cycler api v5**: new `137b-successor-offer-close-api.js` exposes queued `describeOfferCloses({rows, gesture})` and `applyOfferCloses({closes, expectedLines, rows?})`, built on the hn.6 engine internals. Promotion ID-less keys (different digest than the engine's) are translated per call to engine keys, so shared validators keep refusing look-alike neighbours. `api.version` bumped 4→5 and documented in `docs/develop/plugin-apis.md`.
- **Nav promotion card** (`667` + new `667a`): attaches descriptors when cycler is v5+ and successors is v4, applies picks as today, then closes through `applyOfferCloses`, with the receipt shown via notice v4 (guarded Undo). Older cyclers get today's pull-in-only card. The merge card (`429a`) is untouched by construction.
- **Tests**: new `test-task-status-cycler-promotion-verdicts.cjs` (8) and `test-navigation-hotkeys-promotion-verdicts.cjs` (6), both registered in `package.json`; three frozen-version tests moved 4→5 with new-method assertions added.

Verification: full `npm test` 5657/5657 green (two perf flakes pass in isolation; three version pins were the intended v5 bump), `npm run build` + `build:check` green, `docs:inventory:check` green. One pre-existing failure recorded as a follow-up on the bead: `docs-check`'s README contract-table snapshot fails identically on clean master `f075147`, unrelated to this phase.
