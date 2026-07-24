# Chat History - ace-run (4k--plan)

- **TIMESTAMP:** 2026-07-10 13:10:15 EDT
- **MODEL:** codex/gpt-5.6-sol
- **AGENT:** 4k--plan

## Linked Chats

- **1. --plan** — `~/.sase/chats/202607/gh_bobs_org__bob_cli-ace_run-4k__plan-260710_130528.md`
- 2. --code — `~/.sase/chats/202607/gh_bobs_org__bob_cli-ace_run-260710_130528.md`

**Plan:** /home/bryan/.sase/plans/202607/scheduled_projects.md


## Prompt

#gh:gh_bobs-org__bob-cli Can you help me improve the `bob projects` command?

- We should start checking for a new `scheduled` frontmatter property on project note files.
- If set, this property should use a date value of the form YYYY-mm-dd.
- When found, what the `bob projects` command does should depend on whether the date is in the future (i.e. tomorrow or later) or not. If so, we should add the `#hide` tag to every Obsidian task in that project file. Otherwise, we should remove the `#hide` tag from every Obsidian task in that file.
- When the `<ctrl+shift+opt+n>` keymap is used to create a new project note file from the currently selected Obsidian task, if the task has a `scheduled` dataview property, we should remove it from the ^prj note we create and instead use this value for the new project note file's `scheduled` frontmatter property.
- When the `<ctrl+=>` Obsidian keymap is used, we should start showing which project note files are scheduled for the future somehow using a visual indicator. I want you to lead the design on this one. Just make sure it looks beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Submit your plan with the
`sase plan propose` command (as the skill instructs) before making any file changes.
 %a:tale

## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202607/scheduled_projects.md`

> # Scheduled Project Visibility
> ## Goal
> Make a project note's optional `scheduled` frontmatter date control the visibility of every Obsidian task in that note,
> carry a source task's schedule into newly-created project frontmatter, and make future-scheduled child projects
> instantly recognizable in the `<ctrl+=>` picker without disturbing the existing project lifecycle and sub-project
> workflows.
> ## Product decisions
> - `scheduled` is optional project frontmatter. When present, its scalar value must be an actual calendar date written as
>   `YYYY-MM-DD`; quoted and unquoted YAML scalars are accepted, but empty, malformed, and impossible dates are errors.
> - "Future" means strictly later than the machine's local current date. Today and all past dates are due. The CLI will

*See full plan file for details.*

