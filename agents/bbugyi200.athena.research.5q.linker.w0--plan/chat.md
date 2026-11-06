# Chat History - ace-run (research.5q.linker.w0--plan)

- **TIMESTAMP:** 2026-11-05 10:19:41 EST
- **MODEL:** claude/opus
- **AGENT:** research.5q.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/pomodoro_names_follow_task_types.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/pomodoro_names_follow_task_types.md`

> # Plan: Open Pomodoro names follow their tasks' types
> ## Why
> Bryan wants every Obsidian task (typed explicitly or by inheritance) to have a type that
> matches one of the types of the Pomodoro holding its Task Link. `bob task reconcile`
> should be the fallback that adds or removes types on Pomodoro lines. The keymaps that
> break the rule should be fixed so the fallback rarely fires. Custom Pomodoro names may
> be an exception, but they must not drive the design or break.
> This plan implements the recommended solution of the research report
> `research:202611/pomodoro_names_follow_task_types/pomodoro_names_follow_task_types.md`
> (read it with `sase artifact read` for evidence and line references). Bryan accepted all

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Obsidian tasks should always have a type (either implicitly or explicitly) that
matches one of the task types of a pomodoro that contains a task link pointing to that
task, but we don't seem to do a good job of enforcing this currently. I would like to
change that. Can you help me implement this?

- The `bob task reconcile` command should be used as a fallback mechanism to ensure this
  is always the case (by removing or adding types to pomodoro lines as necessary).
- With that said, we should try to make sure that any keymaps that can currently break
  this constraint are fixed, so the `bob task reconcile` command is rarely needed to
  perform this cleanup.
- I think that the exception to this rule should maybe be custom pomodoro names, but I
  don't use these much so don't let them constrain the design too much (but don't break
  anything).
- Review the pomodoro_names_follow_task_types.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.5q.linker

## Response

Reading the research report first; the research sidecar isn't cloned in this workspace yet, so I'm opening it.

I've read the research report; now I'm checking the current Rust code (routing, merged-name helpers, reconcile) to anchor the plan.

Opened bob-plugins; now checking the JS mirror and the two writer bugs the report flagged.

Confirmed `bob task reconcile` is the task-status-hooks sync. Next I'm reading the close-naming code and the decision records the plan would supersede.

Both plugin bugs from the report are still present at the current bob-plugins HEAD. I'm now mapping where plugin link-removal paths funnel through, so the plan can fix them at shared choke points.

Memory routing is clear: the plan will change two glossary strands and add one decision record. Now I'm reading an existing decision record to match the format.

I have enough to plan. One last format check: I'm looking at a recent epic plan in the plans sidecar so this one matches the expected schema.

I've finished exploring, and both writer bugs are confirmed at the current bob-plugins HEAD. Writing the epic plan now: 9 phases across bob-cli and bob-plugins.

Two glossary decisions collided (both strands live in one glossary note), so I'm merging them into a single memory decision.

Validation passes. I'm re-reading the file once to check that the edits left it coherent; the on-disk-change notice may mean a formatter touched it.

Validation passes. Proposing the plan now.

I've written and submitted a plan to enforce the type rule. It passed validation and is waiting for your approval; nothing has been changed in either repo yet. It's a 9-phase epic across bob-cli and bob-plugins.

**Both writer bugs from the research report are still present.** I checked them against the current bob-plugins code:
- Renaming a Pomodoro with Ctrl+Shift+M no longer retypes its tasks.
- The Task Card type edit skips moving the link for any task that already had a session today, because the closed entry's 🍅 link also matches.

**The rule.** The task's type is the source of truth. Only the type part of the name changes on today's open Pomodoros; no automatic repair ever writes a `[type::]` field or moves a link.
- **Adding:** a type that a linked task has but the name lacks is added.
- **Removing:** a type that no link carries (struck links count) is removed, but only when every child bullet is a resolved task link. A prose bullet keeps any planned type you want to protect.
- **Never touched:** custom names with no types in them (your existing "container" rule, so no new mechanism), MEET entries, and closed entries.
- **At close:** a session's closed name becomes exactly the types worked, so `— FIX` that only worked a BUILD task closes as `— BUILD`.
- **New entries:** typing a type name for a brand-new entry changes the tasks' type instead of producing `FIX + BUILD`. Ctrl+Shift+M into a new named entry does the same, because otherwise `bob task reconcile` would strip the typed name 15 minutes later.

**Phases:**
1. **Plugin bugs:** fix the two bugs above.
2. **The rule in Rust:** the rule and the close naming, a shared test-case file, and one shared function that applies the rule to a daily note. Reconcile and every bob command that writes to the Pomodoro list use it.
3. **Reconcile:** `bob task reconcile` applies the rule to today's open Pomodoros. Its JSON gains `type_agreement` and `type_agreement_unrepaired` lists, its human output shows renames, and `bob plan`'s `type_mismatch` warning narrows to what reconcile won't fix. This phase waits for phase 1.
4. **Ledger Tools:** the JavaScript copy of the rule, plus one shared async helper for the other plugins. The type mark now also covers inherited types.
5. **bob commands:** capture, `bob task cancel`/`complete`, and type-change moves apply the rule to the Pomodoros they touch.
6. **Close and capture naming in bob:** the close naming, plus the capture change for new `#NAME` entries. That commit is marked breaking (`!`), because documented capture behavior changes.
7. **Navigation hotkeys:** every link-removal keymap applies the rule through the shared plugin write path, rather than being patched one by one.
8. **Block ID Prompt and the task-status-cycler close.**
9. **Audit:** a docs consistency pass, a read-only reconcile dry run on your vault, and new task beads for any leak it finds.

**Decisions waiting for you in the review:**
- **Reconcile rollout:** the default is to apply repairs right away after a dry-run check on your vault. The alternative is a report-only period first, with a follow-up bead to switch it on.
- **Event Task links under work Pomodoros:** the default adds MEET to the name (`— BUILD + MEET`), matching what Enter already does. This was the one open question in the report without a recommendation.
- **Memory:** a new decision record (`open-pomodoro-names-follow-task-links`), and updates to the Task Type and Merged Pomodoro glossary entries, whose current text the plan makes false.

What the rule costs you:
- A Pomodoro name you change by hand to disagree with its tasks reverts within about 15 minutes. The fixed Ctrl+Shift+M rename is the supported way.
- A running session can be renamed while you watch.
