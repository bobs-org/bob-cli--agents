# Chat History - ace-run (01m--plan)

- **TIMESTAMP:** 2026-08-14 13:46:04 EDT
- **MODEL:** codex/gpt-5.6-sol
- **AGENT:** 01m--plan

**Plan:** /home/bryan/.sase/plans/202608/skip_blocked_task_jumps.md


## Prompt

#gh:gh_bobs-org__bob-cli Can you help me start having the `<ctrl+shift+j>` and `<ctrl+shift+k>` Obsidian keymaps only jump to tasks that have either an open, in-progress, or next status? I'm pretty sure we currently include blocked tasks, but we should stop doing that. Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.


## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202608/skip_blocked_task_jumps.md`

> # Skip Blocked Tasks During Ctrl+Shift+J/K Navigation
> ## Goal
> Change Bob Navigation Hotkeys so both `Ctrl+Shift+J` (next) and `Ctrl+Shift+K`
> (previous) navigate only among real `#task` lines whose checkbox status is Ready/open
> (`[ ]`), In Progress (`[/]`), or Next (`[*]`). Blocked tasks (`[?]`) must no longer be
> jump targets in either direction, including when navigation wraps around the beginning
> or end of a note.
> The source of truth is the linked `bob-plugins` repository. The command hotkeys and the
> Vim-normal-mode physical-key fallback already converge on `jumpToOpenObsidianTask` and
> `getOpenTaskNavigationLines`; the change should be made in that shared target-selection

*See full plan file for details.*

