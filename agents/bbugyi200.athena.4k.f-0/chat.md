# Chat History - ace-run (4k.f-0--plan)

- **TIMESTAMP:** 2026-07-10 13:34:18 EDT
- **MODEL:** codex/gpt-5.6-sol
- **AGENT:** 4k.f-0--plan

## Linked Chats

- **1. --plan** — `~/.sase/chats/202607/gh_bobs_org__bob_cli-ace_run-4k_f_0__plan-260710_133044.md`
- 2. --code — `~/.sase/chats/202607/gh_bobs_org__bob_cli-ace_run-260710_133044.md`

**Plan:** /home/bryan/.sase/plans/202607/future_scheduled_subproject_icon.md


## Prompt

#gh:gh_bobs-org__bob-cli #fork:4k Did we make sure to give these projects a special icon / emoji to use in the "Sub-projects:" bullet in the parent project note file (which will include a link to the scheduled project if it is a child of that project)? If not, use your /sase_plan skill to plan the appropriate changes.


## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202607/future_scheduled_subproject_icon.md`

> # Future-Scheduled Sub-project Calendar Marker
> ## Goal
> Make future-scheduled child projects immediately recognizable in the machine-owned `Sub-projects:` line beneath a parent
> project's `^prj` task, matching the future-only visual treatment already used by the Obsidian child-note picker without
> changing project lifecycle, ledger retention, or ordering behavior.
> ## Current gap
> The scheduled-project implementation carries schedule metadata into project frontmatter, reconciles task visibility, and
> shows a `calendar-clock` chip in the `<ctrl+=>` picker. The CLI's generated parent ledger does not carry schedule
> metadata into its sub-project model, however, so it still renders scheduled open children as ordinary bare wikilinks,
> for example `- 🧩 **Sub-projects:** [[roadmap]]`.

*See full plan file for details.*

