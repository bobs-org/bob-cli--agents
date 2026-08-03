# Chat History - ace-run (m3--plan)

- **TIMESTAMP:** 2026-07-27 08:16:06 EDT
- **MODEL:** claude/opus
- **AGENT:** m3--plan

## Linked Chats

- **1. --plan** — `~/.sase/chats/202607/gh_bobs_org__bob_cli-ace_run-m3__plan-260727_074546.md`
- 2. --code — `~/.sase/chats/202607/gh_bobs_org__bob_cli-ace_run-m3__code-260727_074546.md`

**Plan:** /home/bryan/.sase/plans/202607/project_schedule_task_properties.md


## Prompt

#gh:gh_bobs-org__bob-cli The Obsidian `<ctrl+shift+p>` keymap and the `bob task-status-hooks` commands already add/remove the `#hide` tag to open tasks in an Obsidian project note file when we add/find a `scheduled` property in the project note file's frontmatter. Can you help me stop using the `#hide` tag and instead add a `scheduled` data view property to each open task in the project note file, assuming that the task does not already have a scheduled property that specifies a date equal to or further in the future than the date the project note file specifies? We should also mark/unmark each task as blocked (i.e. change the task checkbox to `[?]`).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %model:opus

## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202607/project_schedule_task_properties.md`

> # Replace project `#hide` visibility with task-level scheduled properties
> ## Goal
> Stop using the `#hide` tag as the mechanism that suppresses ordinary tasks in a scheduled project note. When a project
> note's frontmatter declares a valid `scheduled: YYYY-MM-DD`, every **open** ordinary task in that note should instead
> carry a task-level Dataview schedule `[scheduled:: YYYY-MM-DD]` equal to the project's date, unless the task already
> declares a valid schedule on the same day or later. Those tasks should then be Blocked (`[?]`) while the date is in the
> future and recover to their normal rank once the date is due, removed, or superseded.
> The user-visible outcome is unchanged (tasks in a future-scheduled project stay off `dash.md`), but the reason becomes a
> real, inspectable task property instead of an opaque tag, and those tasks become first-class Blocked tasks that appear
> in `blocked.md` alongside dependency-blocked tasks.

*See full plan file for details.*

