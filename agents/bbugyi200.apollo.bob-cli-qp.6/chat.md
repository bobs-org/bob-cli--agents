# Chat History - ace-run (bob-cli-qp.6)

- **TIMESTAMP:** 2026-11-26 16:57:59 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-qp.6

## Prompt

%auto
#gh:gh_bobs-org__bob-cli
%id(6, clan=bob-cli-qp, bead=bob-cli-qp.6)
%model:@medium
%w(bob-cli-qp.1,bob-cli-qp.4, for_epic=false)
%w(bead=bob-cli-qp.1)
%w(bead=bob-cli-qp.4)
Can you complete the work for bead bob-cli-qp.6? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-qp.6` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-qp.6` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-qp.6 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-qp.6 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-qp.6 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-qp.6`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-qp.6 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Done. `bob-cli-qp.6` (Reference editor behind `==`) is implemented, verified, deployed, and closed.

What shipped (all in `bob-plugins`, Bob Ledger Tools 1.170.0):

- **`==` routing with capability probe** ([249v editor routing](absolute-path-placeholder)) — opens the shared Property Editor in settings mode on the `REFERENCE` contract when the per-path cache confirms `props_ref_contract_v1`, else qm.1 focus-or-add on `title`. The 249s `==` registration now delegates to this decider.
- **Capability evidence** (`298v`) — the catalog probe settles a new `refContract` slot independently beside the generic contract (confirmed/absent/unconfirmed each), plus typed-show confirmation; `==` treats anything but confirmed as fallback.
- **Settings rows** (`298w/298x/298y/298z`) — nine reference settings validate and render as `REFERENCE SETTINGS` plus `OWNED ELSEWHERE`; owned rows are `reference-route` entries whose Enter opens the reading task (or a legacy notice) and whose File name opens Command Mode while copying `bob ref rename <stem> <NEW>`. Title/Source are set-only; `=` focuses settings in place; badge kind `reference`.
- **Tests/docs** — 14 new editor tests; existing capability/settings suites extended. Full `npm test`: 10084 unit + 26 perf, 0 fail. `build:check` and `docs:check` green. Deployed via `bob plugins sync -p bob-ledger-tools` after merging origin/master (which had landed qp.5 readouts mid-turn) and resolving the one `package.json` test-list conflict.

Two notes: File name can't truly prefill Command Mode — `api.commandMode` exposes no opener — so it opens the sheet and copies; recorded as a `PROPOSED FOLLOW-UP` on the bead. The authorized glossary edits (`ref-card`, `property-card`) were left untouched; they belong to `qp.8` go-live per the plan.
