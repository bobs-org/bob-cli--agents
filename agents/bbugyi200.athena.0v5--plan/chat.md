# Chat History - ace-run (0v5--plan)

- **TIMESTAMP:** 2026-10-01 17:55:43 EDT
- **MODEL:** claude/opus
- **AGENT:** 0v5--plan

**Plan:** /home/bryan/.sase/plans/202610/per_note_ready_cap.md


## Prompt

#gh:gh_bobs-org__bob-cli One of my goals while reviewing my Obsidian tasks during my morning GTD is to
make sure that no area/project note file contains more than N ready tasks (this number
should be configurable, but should default to 5).

- The idea is that if I have more than N ready tasks in a area/project, then I should
  probably look into creating a new project from some of those tasks and/or
  de-prioritizing (using the `<ctrl+shift+p>` keymap, for example) some tasks in that
  area/project note file.
- I would like to make it clearer which project files have more ready tasks than they
  should.
- We should show some kind of notification / toast in Obsidian anytime we use any one of
  the Obsidian keymaps that would cause this constraint to be violated (for example,
  when moving a task to a project note file that already has >=N ready tasks).
- We should show a badge and/or diagnostics in the ~/bob/dash.md file and/or in project
  note files that makes it clear how many area/projects violate this contraint currently
  (and which ones).
- I should also have the ability to view this information from the command-line. Namely,
  I should have the ability to review the number of ready tasks in each area/project
  note file from the command-line and should be able to see (in some visually appealing
  way) when this constraint is being violated (and in which area/project note files).
- Review the per_note_ready_cap.md file in the research sidecar repo for context and
  inspiration before planning. I agree with all of the recommendations made by that
  research file.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you help me implement this? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %auto

## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202610/per_note_ready_cap.md`

> # Per-note Ready cap: crowded notes in the CLI, dash, and notes
> ## Outcome and scope
> During the morning GTD review, Bryan wants no area/project note to hold more than N
> ready tasks, with N configurable and defaulting to 5. When a note goes over, the fix is
> to split the work into a new project or to de-prioritize some of it. Bryan accepted
> every recommendation in `research:202610/per_note_ready_cap/per_note_ready_cap.md`. Read
> it with `sase artifact read` before starting any phase. This epic implements that
> report's design, with the refinements called out under "Design decisions beyond the
> report".
> The phases deliver these surfaces:

*See full plan file for details.*

