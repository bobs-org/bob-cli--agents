# Chat History - ace-run (research.36.linker.w0--plan)

- **TIMESTAMP:** 2026-11-03 16:00:26 EST
- **MODEL:** claude/opus
- **AGENT:** research.36.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/task_move_merge_split.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/task_move_merge_split.md`

> # Plan: Move, merge, and split tasks
> ## Why
> Bob already moves whole tasks between notes (`bob task move`, Ctrl+Shift+M, capture move
> bullets). It cannot do the other two outline refactorings Bryan reaches for:
> - **folding** one or more tasks into another task, or into a "Future Work" section, when
>   they turn out to be part of it;
> - **promoting** bullets that grew into real work (meeting notes, a task's notes, a
>   Future Work entry) into tasks of their own.
> This epic adds both. The design follows the research report
> `research:202611/task_move_merge_split_design/task_move_merge_split_design.md`, which

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to add better support for moving tasks from one note file to
another and add excellent (new) support for merging tasks to / creating new tasks from
bullets of other tasks. Can you help me implement this?

- We should add support for a new `@a+aid @b+bid > @c` capture syntax where any number
  of notes can be on the left-hand side of the `>` character and `@c` can have a
  `#drawer` suffix to specify that the tasks should be converted to notes and moved to
  that drawer (this drawer should be created if it does not already exist).
- We should also be able to use a target of the form `@c+cid` after the `>`, in which
  case we should merge the source tasks into the `^cid` task in the ~/bob/c.md file. We
  should also be able to use the `@c+cid#drawer` syntax to target a specific drawer in
  the `^cid` task (this drawer should be created if it does not already exist).
- When merging one task into another, we should not delete the source tasks. Instead, we
  should add a new "merged into" task relation that points from the source tasks to the
  destination task (and auto-cancels the source task). This "merged into" task relation
  should be able to be used on its own (in Obsidian via the `<ctrl+shift+l>` keymap, for
  example) to perform the same operation (see how we associate other task relations with
  specific operations for inspiration--this "merged into" relation should be
  configurable if possible/desirable).
- We should add a new `<ctrl+shift+t>` keymap to Obsidian that makes it easy to split
  out one or more top-level bullets from a task into new tasks. When this is done, the
  bullets (and their child bullets) should be replaced by some concise and useful text
  containing inline links to the new tasks that were created from the old bullets (the
  old tasks should wind up being given "linked from" mentions which are triggered by
  these inline links).
- Make sure that we have good command-line support for all of this new functionality.
- FYI: I already am in the process of adding support for the `@file+id` capture syntax
  multiple times on the same line (see the capture_multi_target.md file in the plans
  sidecar repo for context).
- Review the task_move_merge_split_design.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.36.linker

## Response

Reading the research and multi-target plan artifacts before exploring the code.

Read both context docs; now checking the multi-target epic's status and the codebase.

Explorations are back; checking a few remaining facts (grammar revision, existing beads, docs) before designing.

Checking the move-bullets plan's Mac phases so a `>` Mac phase can align with them.

Design is taking shape. Loading the memory-write procedure, since the plan will record decisions and glossary strands.

Memory routing is clear. Now checking the epic plan schema before writing the plan.

I have the full design picture. Checking the exact glossary sentence that the merge-label work will make false, for the plan's memory decision.

I have what I need. Writing the epic plan now.

Existing strands in one web collide across decisions; I'll drop the optional successor-offer addition rather than fold an unrequested addition into the correction.

Validation passes. One wording fix (a reference to "the research survey" that should point to grep), then revalidate and propose.

Staged. Finishing through `/sase_final`.

I've written the plan as a 13-phase epic, staged it with `sase plan propose`, and it's waiting for your approval. No code has changed. It passed `sase plan validate` with no warnings.

**The design rule:** the destination decides the shape. `>` to a bare note moves the tasks and keeps their IDs. `>` to a task, a task's drawer, or a note section merges them in. Split is the reverse: it turns bullets back into tasks. Each of the three operations gets one Rust engine that capture, the CLI and Obsidian all call.

- **Move:** `@a+x @b+y > @c` reuses the existing move engine. The CLI gains `bob task move -t NOTE TASK…` for many tasks into one note.
- **Merge** (`> @c+id`, `> @c+id#drawer`, `> @c#section`, `bob task merge`):
  - Your notes now land in the target. The source's notes are moved under a plain title bullet there, not copied, and links to them are repaired.
  - The source isn't deleted. It stays as a cancelled task carrying `merged into [[T]]`, and the target shows "merged from".
  - Tasks that were waiting on the source now wait on the target, so a merge never unblocks unfinished work.
  - The source's links in today's open Pomodoros are removed and the target is offered in its place. Bob never adds the link without your pick.
  - Running the same merge again changes nothing.
- **The `merged into` label:** this is a new `relations.merge_labels` setting, empty by default. I'll turn it on in your chezmoi config. Using the label through capture `~`/`~~` or Ctrl+Shift+L runs the same merge.
- **Split:** Ctrl+Shift+T works on the bullet under the cursor, a count, a visual selection, or a picker. Each bullet becomes a new task right below its parent and is replaced in place by a `[[#^id|Title]]` link. The parent turns into a live checklist.
  - **Mentions point the other way from what you asked:** the "linked from" mention lands on each new task, pointing back at the parent, because mentions are one-directional (the research's adjustment, which you accepted).
  - **Placement:** bullets in meeting notes (daily-note tasks) become tasks in the meeting's root note.
- **CLI:** `bob task move -t`, `bob task merge -i … [-D|-s] [-p]`, and `bob task split … [-n|-m|-s]`. They share `bob task move`'s lock, sync, dry-run and single commit. Running `bob task split` with nothing selected lists the numbered bullets you can pick.

**How the work is split:** the contract docs and the shared Rust plumbing go first. Then split and the merge engine run in parallel. After the merge engine come its CLI, the merge label and the Obsidian merge. Capture `>` comes after those, then completion help, the Mac app, and a final check pass.

**Before you approve:**
- **Waits on your multi-target work:** the `>` capture phase can only start after the multi-target epic (`bob-cli-gm`) and the move-bullet lexer (`bob-cli-gl.2`) have landed. The plan has no way to express that as a dependency, so that phase is told to stop and report if either is still open.
- **Ctrl+Shift+T collides on Linux:** it's Obsidian's built-in "Undo close tab" there. The plan moves Undo close tab in your vault's `hotkeys.json` to Ctrl+Shift+Alt+T and keeps Cmd+Shift+T on the Mac.
- **Memory decisions:** there are three.
  - Updating `glossary:task-relation` is on by default, because merge labels make its list of status exceptions wrong.
  - New Task Merge / Task Split glossary entries and three new decision records are off by default; turn them on if you want them recorded.
  - I dropped a sentence for the successor-offer glossary entry because validation wouldn't allow it alongside the task-relation update.

The plan file is `sase_plan_task_move_merge_split.md`.
