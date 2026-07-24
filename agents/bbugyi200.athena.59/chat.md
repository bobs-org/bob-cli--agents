# Chat History - ace-run (59--plan)

- **TIMESTAMP:** 2026-07-11 07:50:16 EDT
- **MODEL:** codex/gpt-5.6-sol
- **AGENT:** 59--plan

## Linked Chats

- **1. --plan** — `~/.sase/chats/202607/gh_bobs_org__bob_cli-ace_run-59__plan-260711_074812.md`
- 2. --code — `~/.sase/chats/202607/gh_bobs_org__bob_cli-ace_run-260711_074812.md`

**Plan:** /home/bryan/.sase/plans/202607/preserve_prj_hide_on_schedule.md


## Prompt

#gh:gh_bobs-org__bob-cli Yesterday we added support to the `bob projects` command for a new property named `scheduled` that can be added to the frontmatter of a project note file. If the scheduled date is on today or before today, we remove the `#hide` tag from all Obsidian tasks in that project note file. This is correct but we made one mistake. Namely, we shouldn't remove the `#hide` tag from the `^prj` note file (that represents the definition of done for the project) unless it is the only Obsidian task in that project note file. Can you help me fix this? Think this through thoroughly and create a plan using your `/sase_plan` skill. Submit your plan with the
`sase plan propose` command (as the skill instructs) before making any file changes.
 %a:tale

## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202607/preserve_prj_hide_on_schedule.md`

> # Preserve `^prj` Visibility During Scheduled Project Sync
> ## Goal
> Correct `bob projects sync` so reaching a project's `scheduled` date reveals the project's ordinary Obsidian tasks
> without prematurely revealing its definition-of-done task. The `^prj` task should have `#hide` removed by the
> scheduled-visibility rule only when it is the sole real Obsidian task in the project note.
> For this rule, a "real Obsidian task" should retain the command's existing meaning: any parsed Markdown checkbox task
> outside frontmatter and fenced code, including open, in-progress, completed, canceled, nested, quoted, and ordered
> tasks. Checkbox-like prose and fenced examples do not count.
> ## Behavioral Design
> - Preserve the future-schedule behavior: every real task, including `^prj`, receives exactly one whole-token `#hide`

*See full plan file for details.*

