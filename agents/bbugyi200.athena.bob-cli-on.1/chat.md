# Chat History - ace-run (bob-cli-on.1)

- **TIMESTAMP:** 2026-11-21 12:17:04 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-on.1

## Prompt

#gh:gh_bobs-org__bob-cli
%id(bob-cli-on.1, bead=bob-cli-on.1)
%clan(bob-cli-on, tribe=epic, summary_script=sase_clan_summary_epic)
%model:@medium
%auto
Can you complete the work for bead bob-cli-on.1? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-on.1` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-on.1` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-on.1 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-on.1 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-on.1 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-on.1`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-on.1 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Phase `bob-cli-on.1` (req-contract) is done and closed.

What shipped:

- Retired the canceled `bob-cli-of` epic (closed as superseded by `bob-cli-on`).
- New recognizer `src/native/task_reqs.rs`: recursive req forest with `ReqMark`, derived `EffectiveReqState` (pending/met/moot/dropped/carried/excluded with ancestor rule and explicit-state preservation), structural row identity (`req_row_key` with path + sha), subtree ends, note ranges, `MAX_REQ_DEPTH` (16), plus `req_forest`, `owner_of_line`, `is_req_line` queries.
- `TaskChildKind::Requirement` in `classify_task_child` (checked before `Authored`, with a filter-aware variant); merge still copies req children as authored and split candidacy is unchanged.
- Shared vectors `tests/fixtures/task_reqs/vectors.json` (RQ1–RQ21) plus README, loaded by 7 passing tests covering positions, nesting, marks under open/done/cancelled owners, exclusions, depth bound, anchors, distinct keys, and token matching.
- Contract page `docs/task-requirements.md`, registered in `contracts.yml` (nav regenerated), with one-line cross-links in vault-format, tasks-and-lanes, task-split, task-dependencies §12, projects, and capture.

Verification: `cargo fmt --check` clean, `just lint` clean, full `cargo test --workspace` 12255 passed / 0 failed, `just docs-gen` clean. `just docs-check` fails only on the pre-existing `vault-format.md` budget overrun (6016 words without my edit; tracked by [bob-cli-oc](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-oc/README.md)), recorded as a `PROPOSED FOLLOW-UP` note.

Declaration submitted: commit for `main` with `bead_action: close` accepted.
