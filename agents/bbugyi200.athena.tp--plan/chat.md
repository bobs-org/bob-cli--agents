# Chat History - ace-run (tp--plan)

- **TIMESTAMP:** 2026-08-05 20:44:41 EDT
- **MODEL:** claude/opus
- **AGENT:** tp--plan

**Plan:** /home/bryan/.sase/plans/202608/focus_task_move_destination.md


## Prompt

#gh:gh_bobs-org__bob-cli Can you help me focus the target obsidian note file when the `<ctrl+shift+m>` keymap is used? We currently just stay in the note file we are in (i.e. the source note file). Also, we should jump to the line that we moved the task to once we focus that note file. Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %model:opus

## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202608/focus_task_move_destination.md`

> # Plan: Focus the destination note after a `Ctrl+Shift+M` task move
> ## Problem
> `Ctrl+Shift+M` (bare) and `N<Ctrl+Shift+M>` (counted) move the task under the cursor — plus any requested follow-on
> tasks — from the current note into an area or open-project note chosen from a picker. When the move succeeds, the editor
> stays in the **source** note: the plugin deliberately restores the source editor's scroll position and focus, and the
> only feedback about the destination is a `Moved N tasks to <name>` toast.
> Bryan wants the opposite: after a successful move, Obsidian should **focus the destination note** and put the cursor on
> **the line the task was moved to**, so the moved task can be edited immediately without navigating there by hand.
> ## Repository
> All code changes are in the **`bob-plugins`** linked repo (plugin `bob-navigation-hotkeys`). Open it with the

*See full plan file for details.*

