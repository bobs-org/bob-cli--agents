# Chat History - ace-run (bob-cli-qp.8)

- **TIMESTAMP:** 2026-11-27 00:36:47 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-qp.8

## Prompt

%auto
#gh:gh_bobs-org__bob-cli
%id(8, clan=bob-cli-qp, bead=bob-cli-qp.8)
%model:@medium
%w(bob-cli-qp.7, for_epic=false)
%w(bead=bob-cli-qp.7)
Can you complete the work for bead bob-cli-qp.8? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-qp.8` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-qp.8` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-qp.8 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-qp.8 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-qp.8 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-qp.8`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-qp.8 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Ref go-live is half landed, half gated. The plan gate (`bob-cli-qm.7` closed) is unmet — it is still in progress behind `bob-cli-qj.4` — so I shipped everything ref-owned and left the shared pieces for after `qm.7`.

Landed uncommitted in this workspace, all verified:

- **Gate deleted (bob-plugins):** removed the `240u` preview fragment, its `fragments.json` line, the gate checks in the `249s` ref host, the `374i` preview exports, and the preview-gate unit test plus its `package.json` entry. Manifest bumped to 1.172.2, bundle rebuilt.
- **Tests:** e2e runner no longer writes the key into its disposable vault, the closed-gate flow is removed, and the meta-test updated. Passive suite extended with ref paint/fold/drawer coverage (≥24 repaints, zero writes/spawns). 163 focused tests pass; `build`, `build:check`, and docs inventory checks are green. Cabinets guarded hunks untouched.
- **Docs:** `ref-card.md` admonition and gate text removed; `ref.md` points to the Ref Card page; vault-format documents `summary:` with net-zero word change; sync doc covers note-side edits and protected keys.
- **Memory:** new `glossary:ref-card` strand (the one authorized decision I could apply cleanly); roster and shims regenerated.

One check fails identically on the clean base: `vault-format.md` is 30 words over budget (6030/6000), unchanged by my edits — recorded as a proposed follow-up diet for the land agent.

Deferred until `qm.7` closes: the `property-card` strand edit, shared docs (`architecture.md`, `property-editor.md`, ledger tools, Reading Board), vault sync with smoke test, and bead close. All four notes (gate, landed files, verification, remainder) are on `bob-cli-qp.8`, which stays open.

Declaration accepted — both repos committed with `keep` on `bob-cli-qp.8` pending `qm.7`.
