# Chat History - ace-run (bob-cli-pl.9.1.1)

- **TIMESTAMP:** 2026-11-25 20:20:40 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-pl.9.1.1

## Prompt

#gh:gh_bobs-org__bob-cli
%id(bob-cli-pl.9.1.1, bead=bob-cli-pl.9.1.1)
%clan(bob-cli-pl.9.1, tribe=epic, summary_script=sase_clan_summary_epic)
%model:@medium
%auto
Can you complete the work for bead bob-cli-pl.9.1.1? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-pl.9.1.1` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-pl.9.1.1` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-pl.9.1.1 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-pl.9.1.1 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-pl.9.1.1 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-pl.9.1.1`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-pl.9.1.1 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Phase `bob-cli-pl.9.1.1` is done and closed.

**What landed** (all in `bob-plugins`, synced to the vault: 1 copied):

- **Contract evidence** (`298v`): per-bob-path `props_contract_v1` tracking beside the generic `props_v1` cache. A lifecycle `bob __catalog --protocol 1` probe confirms it (or records old-binary absence); a typed-note `props show` also confirms it, while ordinary-note reports can never establish absence or downgrade a confirmed contract. Deduplicated, bounded retries, stale/path-change/teardown discards — and it never spawns from paint.
- **Shared gate** (`240q`): `area`/`project` mounts join the eligibility allowlist with `data-home-source` paths and a species-specific contract requirement; album/record/bank keep working on `props_v1` alone. Coordinator confirmation now also refreshes home mounts.
- **Home ownership** (new `249da` + `249d` wiring): connected card+foot mounts acquire whole-frontmatter ownership in Live, Reading, and widget-fallback paths with generation-bound release on any loss (fail open, native restored). Row fallback claims only card-represented keys (chips, summary, created). `249d` stays under the 1000-line cap via the split.
- **Entry routing** (`241d`): owned-scope summary focus now opens `openPropertyEditor({ setting: "summary" })`; bare `+`/`-`/`==` and the Add wrapper ride the existing actual-ownership route.

**Verification:** `build`, `build:check`, docs-inventory, manifest validate, and smoke self-test pass; 329 focused tests green (capability, ownership, home host/DOM/model/live, catalog, entrypoints, bank, offline e2e wrappers); full `test:unit` 9712/9719 with 2 date-boundary failures that reproduce identically on the clean tree (recorded as `PROPOSED FOLLOW-UP`); `test:perf` 26/26. Live `bob __catalog` output corroborates the `props_contract_v1` feature the probe relies on. No `--epic-symbol` entries remain.

**Not verified here:** the real-Obsidian matrix (no `xvfb`/Obsidian in this environment) — that is phase `9.1.2`/`9.1.3` territory, with evidence recorded on the bead for the acceptance run.

Declaration accepted — `sibling:bob-plugins` work committed with `bead_action: keep` (phase already closed; no re-close attempted).
