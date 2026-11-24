# Chat History - ace-run (bob-cli-pl.5)

- **TIMESTAMP:** 2026-11-24 16:32:09 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-pl.5

## Prompt

%auto
#gh:gh_bobs-org__bob-cli
%id(5, clan=bob-cli-pl, bead=bob-cli-pl.5)
%model:@medium
%w(bob-cli-pl.3,bob-cli-pl.4, for_epic=false)
%w(bead=bob-cli-pl.3)
%w(bead=bob-cli-pl.4)
Can you complete the work for bead bob-cli-pl.5? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-pl.5` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-pl.5` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-pl.5 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-pl.5 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-pl.5 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-pl.5`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-pl.5 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Done. `bob-cli-pl.5` (card-live) is closed.

What landed in `bob-plugins` (`plugins/bob-ledger-tools`):

- **Live patch** — new `249f-plugin-home-card-live.js`: pure merge of the already-cached areas/projects snapshots into the card. Dependency-blocked projects get `waits on [[a]], [[b]] +N` links (max 2, same-note targets stay text); inherited-blocked projects name the nearest blocked ancestor via a bounded, cycle-safe walk of the report's `parent` rows; DONE/CANCELED without a line date gains the report `closed_on` (line dates always win, terminal cards included); projects show `N open`/`N today`, areas direct `N today` only, absent snapshots render nothing (never zero), terminal cards keep no readout row. Stale/unavailable snapshots hide only the report parts.
- **Foot lint** — kit `propertyCardFootLint` counts the row's `contract_issues` in the chip count and tooltip (feature-detected, old callers byte-identical); with a known first affected setting (mapped per bob-cli's contract setting ids) the chip becomes a button opening `=+` on that setting, never the drawer.
- **^prj goal line** — a lazily computed CodeMirror line decoration in Live Preview plus a `bob-home-card-goal` class on the recognized row in Reading, applied only while a project card is mounted and stripped on unmount/Source mode; no document change, so cursor and IME are untouched.
- **Tests** — 19 new unit tests (patch merging, absent-not-zero, ancestor walk incl. cycles, contract filing, goal locators) plus 2 foot chip-button tests; e2e fixtures for dependency-blocked, sub-project-blocked, and undated-done notes, probe fields (`goalDecorated`, reason links, readouts, lint chip), and goal/cursor checks; docs section in `area-and-project-cards.md`.

Verification: `build:check` clean, `docs:check` 447 passed, 147/147 tests across all touched suites pass, full `test:unit` 9358/9365 with only 2 perf-budget flakes that fail identically on the clean tree (recorded as a follow-up note). `bob plugins sync` deployed after following the landed-commit overwrite recipe for a sibling checkout's stamp — no `-F`. No memory edits were needed.

Declaration accepted for `commit` (sibling:bob-plugins, bead_action keep). No further work this turn.
