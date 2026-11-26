# Chat History - ace-run (bob-cli-qp.2)

- **TIMESTAMP:** 2026-11-26 14:54:52 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-qp.2

## Prompt

#gh:gh_bobs-org__bob-cli
%id(2, clan=bob-cli-qp, bead=bob-cli-qp.2)
%model:@medium
%auto
Can you complete the work for bead bob-cli-qp.2? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-qp.2` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-qp.2` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-qp.2 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-qp.2 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-qp.2 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-qp.2`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-qp.2 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Done. Bead `bob-cli-qp.2` (ref-kit) is complete and closed.

What landed in `bob-plugins` (manifest `1.168.0`→`1.169.0`):

- `240f`: ref species (`Ref`, `ribbon` tile, `bookmark` icon, open by default) in the registry.
- `240g`: per-card icon override for the title block (ref vocabulary icon).
- `styles.css`: `ribbon` tile form (notched bookmark) plus an empty Ref Card region; holds in forced-colors via shape.
- `240m`: silent missing `created` for ref.
- `240q`: `data-ref-source` mount attribute, ref in the coordinator kind list, props_v1-only gate.
- `240t`: exact-`[[ref]]` predicate, library-coverage predicate (`ref/`, excluding hidden/`*.assets`/`_generated`/`_templates`/`_conflicts`/`ref_history`/conflict copies), precedence slotted after prose.
- `240u` (new): ref-owned preview gate (`refCardPreview`), never touches qm's gate.
- `240v` (new): shared kind vocabulary; `242` board map derives from it, byte-identical for its 7 kinds.
- Stubs: `249q`–`249v` card fragments, `241a` report service, `374i` test exports, all wired in `fragments.json`.
- Docs: new `docs/ref-card.md` with preview admonition, registered in `nav.yml` + inventory.
- Fixtures: `scripts/fixtures/ref-cards/` (19 notes + trimmed `ref-list.json` + README).
- Tests: 3 new suites (kit, preview gate, vocabulary); existing registry/badge tests updated for the 12th species.

Verification: `npm run build` + `build:check` green, focused suites green, full `test:unit` 9969 pass / 0 fail / 5 skipped, `test:perf` 26 pass, `bob plugins sync` clean (12 synced, 0 drift), `bob plugins list` shows no drift. Closed gate keeps rendering unchanged. `COORDINATION:` notes left on `bob-cli-qp.6`/`bob-cli-qm.7` (named `bob-cli-qm.6`/`bob-cli-qm.7` in the note command). One pre-existing item recorded on the bead: `docs-check.sh` drift in the cached bob-cli clone, untouched by this change.

Conflict repaired in `bob-plugins`, rebase continued, and `sase stitch create --resume` accepted (background publication enqueued).

What conflicted: `package.json` `test:unit` — the onto commit added `test-ledger-tools-notebook-card-readouts.cjs` while the rebased Ref Card commit dropped it and added its three new test files. Both additions were legitimate, so I resolved as the union (584 entries, no duplicates), preserving each entry's original position.

Checks run in the `bob-plugins` checkout, all passing:
- `node --test` on the four affected files (readouts + 3 ref-card suites): 23 pass, 0 fail.
- `node scripts/build-plugins.mjs --check`: exit 0.
- `npm run docs:inventory:check`: up to date.
- No unmerged paths and no conflict markers remain.

No finalizer declaration was required (`submission_required: false`, no obligations, no unscanned writes), and the tree is clean at `b021aff5` over `f6458cb0`.
