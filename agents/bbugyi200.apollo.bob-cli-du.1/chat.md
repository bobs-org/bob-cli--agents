# Chat History - ace-run (bob-cli-du.1)

- **TIMESTAMP:** 2026-10-28 15:15:25 EDT
- **MODEL:** grok/grok-4.6
- **AGENT:** bob-cli-du.1

## Prompt

#gh:gh_bobs-org__bob-cli
%id(bob-cli-du.1, bead=bob-cli-du.1)
%clan(bob-cli-du, tribe=epic, summary_script=sase_clan_summary_epic)
%model:@medium
%auto
Can you complete the work for bead bob-cli-du.1? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-du.1` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything, and run `sase bead open bob-cli-du.1` only if the work
is genuinely unfinished. Read its
description and design file with `sase bead read bob-cli-du.1 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-du.1 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-du.1`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-du.1 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

I'll start by reading the phase bead, SASE bead conventions, and any leftover notes so I can see what already landed before planning the rest.

The phase is in progress and scoped to the complete-label contract. Next I’ll read the epic plan, phase notes, and the docs/memory those changes touch.

The phase is docs, inverse pairs, and shared vectors. I’ll read the rest of the plan plus the cancel-label contract so the new sections match that shape.

I’ll use §17 as the template and open the cancel vectors plus the inverse-pair code next.

I’ll generate the cycler Done bytes first, then write the contract docs and tests around those postimages.

Cycler bytes look right, including the two-space `[completion::]` field. Next I’ll land the vectors, inverse pairs, and the §18 contract.

Vectors are in place. Next I’ll amend `task-relations.md` and the other contract docs.

Closed **bob-cli-du.1** (`complete-contract`). The complete-label contract, reverse-rename contract, inverse pairs, and shared vectors are in the tree.

**Contract.** `docs/task-relations.md` now has **§18 Complete labels** (CP1–CP8, planned per later phase) and **RV10** (planned for `reverse-rename`). §§1, 2, 6/LR7, 8, 10, 13, 14, 15 (LR26), and 17 CL2 (both-lists) are amended. Capture, config, JSON, dependency, and project docs follow, with `offer_successors = yes`.

**Rust.** `inverse_phrase` now includes `implemented by` ⇄ `implements` and `verified by` ⇄ `verifies`, with catalog cases in `tests/fixtures/relation_labels/vectors.json`.

**Vectors.** `tests/fixtures/relation_complete/vectors.json` has:
- `done` — generated from bob-plugins `e395721` via `rewriteTaskLineForLocalFallback` + `addOrReplaceCompletionField` (two-space `[completion::]` before `^id`, matching `!`)
- `rule` / `key` / `config` — hand-authored from §18

**Verified.** `just docs-check` passed. `complete_task_tree` matches every non-refused `done` case. Inverse-phrase and catalog tests passed.

**Follow-up on the bead.** `docs/reference/glossary.md` is generated from the glossary memory web, so **Complete label** waits for rollout’s authorized `glossary:task-relation` edit.
