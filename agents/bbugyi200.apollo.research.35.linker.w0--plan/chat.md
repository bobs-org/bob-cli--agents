# Chat History - ace-run (research.35.linker.w0--plan)

- **TIMESTAMP:** 2026-11-03 13:36:42 EST
- **MODEL:** claude/opus
- **AGENT:** research.35.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/capture_move_bullets.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/capture_move_bullets.md`

> # Plan: Move parent tasks into a new project note with capture move bullets
> Research: `research:202611/parent_task_move_bullets/parent_task_move_bullets.md`. Bryan
> accepted every requirement it recommends. This plan turns that report into a contract
> and splits the work into phases. Where this plan departs from the report, §2.2 says why.
> ## 1. The experience
> You are splitting `cash` into a project for leaving Google. In Bob Mac Capture you type:
> ```text
> Finish the Google exit packet @cash^goog-exit@#admin
> - Draft the resignation memo :draft-memo
> - ^

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to make it so that, when the `@foo[:^]bar@` capture syntax is used
to create a new project note, child tasks can be easily pulled in from the parent
project (the ~/bob/foo.md file in our example). Can you help me implement this?

- I think we can achieve this by usig a `^some-id` reference on a bullet line by itself
  (i.e. with no other text) to specify that we should move the `^some-id` task from the
  parent project file into the new project note that we create with this capture.
- Make sure that pressing `^` in this case (i.e. after a `- ` when the `@foo[:^]bar@`
  syntax has been used somewhere in this capture) triggers good completion from the
  bob-mac-capture app.
- Review the parent_task_move_bullets.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.35.linker

## Response

Reading the research report on move bullets, then I'll explore the capture code and Mac app.

The research is thorough and recommends building it as move bullets. Now checking the bob-cli capture code it cites against current master.

The Mac survey is back: no shared picker protocol, so the move picker needs its own source and Add-ID purpose. Now reading bob-cli's project-note planner, move engine and batch commit order.

Confirmed the move engine only appends at the end of `## Tasks`, so draft-order placement needs a new engine option. Next: the inbox-routing move, batch write order, and the project-note renderer.

Renderer understood: moved bullets will need recorded slots. Now checking the sub-bullet model and how both parsers run the project-task pass.

Reading the scoped `@route+` parent picker rows and `capture-task-id`, the pieces the move picker reuses.

Probing today's `capture-parse` and `capture-complete` on `- ^` / `- ^id` to confirm the research's baseline.

Checking what the docs contract tests verify, since that affects whether docs can land ahead of code.

Building a throwaway sandbox vault to see today's project-note dry-run output, so the new move lines fit its style.

Key finding: project-note items already refuse `&` prerequisites, so a future `s:N` date is the only way a new project starts Blocked. Now checking how memory updates must be planned.

Checking what the grammar revision number promises, since the in-flight note-pull epic is also bumping it.

Measuring the vault size, since a move's link repair reads every note and the Mac live preview would pay that cost on each settle.

Confirming whether capture already has a Ready-cap warning to reuse for moved tasks.

Checking how freshness stamping treats recurring tasks, so moved recurring roots follow Ctrl+Shift+M exactly.

I have what I need. Writing the epic plan now.

Validation passed. The file was modified on disk after my write (likely a formatter), so I'm re-reading it to confirm content and phase descriptions.

Content is intact. Applying the validator's guidance that each phase description starts with its id and doesn't point back at the plan file.

Verifying the gate commands the phases cite actually exist in both justfiles.

All cited recipes and files exist. Submitting the validated plan.

I've written the plan and proposed it for review. It is an epic with seven phases, and nothing starts until you approve it.

**The design.** Inside an item sealed with `@foo^bar@` or `@foo:bar@`, a first-level bullet holding only `^<id>` moves that open task, with its whole block, from `foo.md` into the new `foo_bar.md`. It lands at that bullet's position. `- :<id>` does the same, then makes the task Next and links it, as `@foo_bar:<id>` would. The rule to teach is: **a leading `^` or `:` points at an existing task; a trailing one names a new task.** That form is refused today ("names a task but has no task text"), so no draft that captures today changes.

**What you'll see:**
- **Picker.** Typing `^` after `- ` opens "Move into foo_bar.md · from foo.md · N open". It lists the parent's open tasks in document order, grouped by heading, including the 54% without a block ID (those go through the existing Add block ID step). ⇧↵ means "move & add another"; ⎋ leaves the `^` and blocks submit until you pick or delete it.
- **Ghost titles.** A dimmed task title is drawn after each `- ^id` line, so the bare ID is never opaque. It is never written into the draft.
- **Preview band.** "↪ Moves N tasks from foo.md" lists each moved task, with notes like "WORK link follows" or "becomes Next · links under ADMIN", plus a count of repaired links.
- **Hint.** A project-note draft with no moves gets one quiet line telling you `- ^` can move one of the parent's open tasks.

**Reliability:**
- One atomic batch, using the `bob task move` engine that inbox routing already runs inside capture.
- The batch replaces the parent note last. As capture writes files today, a crash mid-write could have deleted the task from `foo.md` before `foo_bar.md` existed. With the new order, an interrupted write can leave a duplicate but never lose a task. The fix also covers inbox routing.
- Moved tasks are stamped fresh, the same as Ctrl+Shift+M.
- Every refusal is a teaching error that writes nothing.

**Phases:**
1. `contract`: docs-first contract, error-message table and test cases.
2. `cli-grammar` and `cli-engine`, in parallel. Until `cli-execution` lands, `bob capture` refuses move bullets with a "not available in this build yet" message.
3. `cli-complete` and `cli-execution`, in parallel. `cli-execution` is sized large, so its agent plans before implementing.
4. `mac-picker`, then `mac-preview`.

**Where I went beyond the research:**
- **No new `move_replacement` field** on `capture-task-id`. The Mac splices the bare block ID it already gets back, as the `@route+` picker does today. bob supplies the ⇧↵ continuation text instead.
- **Separate highlight kinds for `^` and `:`**, so the Mac colours them without inspecting characters.
- **Ghost titles are in this epic**, not deferred.
- **No prerequisite guard needed.** Project-note items already refuse `&` prerequisites, so a future `s:N` date is the only way a new project starts Blocked; moving a non-Blocked task into such a project is refused.

**Your decisions at review:**
- **Grammar revision:** the research said keep it with no breaking marker. I defaulted to bumping it with `feat(capture)!:`, because list bullets and note pull did the same when a refused draft gained meaning.
- **Memory:** a new decision record for the leading/trailing rule and a Project Note glossary update. Both default off because you didn't request them.

**Deferred:** notes nested under a move bullet, converting tasks into a project that starts Blocked, cross-note `- ^route:id`, and the note-to-be outline. The first three are refused with teaching errors.

The note-pull epic (`bob-cli-gj`) is still in progress and touches the same files and the grammar number, so the phases are told to rebase onto it.
