# Chat History - ace-run (bob-cli-on.6--plan)

- **TIMESTAMP:** 2026-11-21 13:50:25 EST
- **MODEL:** claude/opus
- **AGENT:** bob-cli-on.6--plan

**Plan:** /home/bryan/.sase/plans/202611/capture_req_bullets.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/capture_req_bullets.md`

> - **PARENT:** [202611/task_requirements.md](202611/task_requirements.md)
> # Requirement bullets in capture (grammar 29)
> ## Scope and authority
> This child epic implements phase **`bob-cli-on.6`** (`capture-reqs`) of epic
> `bob-cli-on` (Task requirements). Its land agent verifies the complete phase and closes
> `bob-cli-on.6`. Child phase workers close only their own assigned beads. Nobody here
> closes `bob-cli-on` or any other ancestor.
> Read before implementing any phase:
> - `sase bead read bob-cli-on.6 -r "<why>"` and its epic plan
>   `plan:202611/task_requirements.md` (read it with `sase artifact read`). Its **§1, §3,

*See full plan file for details.*

## Prompt

%auto
#gh:gh_bobs-org__bob-cli
%id(6, clan=bob-cli-on, bead=bob-cli-on.6)
%model:@large
%w(bob-cli-on.3, for_epic=false)
%w(bead=bob-cli-on.3)
Can you complete the work for bead bob-cli-on.6? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-on.6` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-on.6` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-on.6 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-on.6 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-on.6 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-on.6`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-on.6 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.
Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.


## Response

I'm reading the phase scope (capture grammar for requirements, a large phase) and will explore the capture code before writing the plan.

Still exploring: now reading how capture models bullet depth (`AuthoredDepth`) and classifies authored lines.

Still mapping the capture write paths (multi-note notes, sub-bullet placement) before deciding how to split the work.

Next I'm checking how the `capture-parse` resolver (`editor_parse.rs`) handles bullet lines, so both resolvers can be planned in sync.

Reading the rewrite engine (`rewrite.rs`) next to see how a new typing rule like `expand_req_marker` would hook in.

Exploration is mostly done. I'm leaning toward a child epic (grammar → writes → rewrite). Now checking how child epic plans are structured in this repo.

Validation passed. Tightening three details before proposing: `--section` isn't a drawer host, depth-preserving renders belong in `depth-model`, and deeper marker-only rows should be placeholders.

The plan is staged. Finishing the turn through `/sase_final`.

I've proposed a child epic plan for `bob-cli-on.6` (capture-reqs) and it's waiting for your review. No code has been written yet, and the bead stays in progress. Nothing needed committing this turn.

The bead had no notes from an earlier attempt, so this is a fresh start. The phase is too big for one agent: it touches the depth model, both capture parsers, refusals, spans, writes, the typing rewrite and the grammar bump. So the plan splits it into five phases:

1. **depth-model** (medium): bullet depth becomes a number instead of first/nested, and the bullet classifier learns deeper levels. Notebook, record, close-log, Pomodoro and drawer handling keep refusing anything past level 2, exactly as today. The write paths learn to keep deeper bullets at their depth, but output for levels 1–2 doesn't change.
2. **req-positions** (medium): one shared module decides where a checkbox bullet is a requirement, for both `bob capture` and `capture-parse`, so the two can't disagree.
   - Bullets past level 2 are allowed only beneath a requirement chain.
   - It adds the `req_in_drawer`, `req_parent`, `req_state` and `req_depth` refusals.
   - `capture-parse` gets the `req_marker` span with a `depth` field.
   - Grammar revision goes from 28 to 29, committed with `!`.
   - A test feeds the same drafts to both parsers and checks they report the same refusals and depths.
3. **new-block-writes** (medium): new tasks and project-note rows put requirements first and file notes into `NOTES` (created only when a note lands in it). Tasks with no requirements stay byte-identical. Adds a `requirements` summary to JSON and human output.
4. **existing-target-writes** (medium): `@route+id` bullets and the same-line `[ ] text @route+id` form go through `insert_reqs`, which moves the task's loose notes into `NOTES` on its first requirement. Adds `req_link` for Pomodoro links whose anchor is a requirement line.
5. **req-rewrite** (medium, runs alongside 3–4): typing `- [` then space expands to `- [ ] `. The docs also describe what the Mac and Obsidian do on their side: absorbing a following `]` and space, and deleting the whole marker with one Backspace.

Two behaviour changes you should know about before approving:
- A checkbox bullet under a plain note, which capture writes literally today, will now be refused with `req_parent`. This follows the epic's design.
- `req_link` is checked only when the capture runs (including dry run), not in `capture-parse`, because it needs to read the vault. The Mac would see it as a dry-run preview error.

The child epic's land agent closes `bob-cli-on.6`. No memory notes are edited here; the epic's `memory` phase handles the capture-bullets decision update.
