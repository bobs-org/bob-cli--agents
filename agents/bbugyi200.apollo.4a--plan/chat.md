# Chat History - ace-run (4a--code)

- **TIMESTAMP:** 2026-10-02 17:02:40 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** 4a--code

## Linked Chats

- 1. --plan — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-4a__plan-261002_164929.md`
- **2. --code** — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-4a__code-261002_164929.md`

## Prompt

%model:@small
#gh:gh_bobs-org__bob-cli @plan:202610/scheduled_first_for_prioritized_tasks.md

The above plan has been reviewed and approved. Implement it now.


## Response

Plan implemented. Opening `Ctrl+Shift+P` on a prioritized task now selects `scheduled` first, so `Ctrl+Enter` takes the previewed roll/decay/cancel with no navigation.

What changed:

- [main.js](sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/main.js) (bob-plugins): new pure helper `promoteScheduledRowForPrioritizedTask` plus a hook at the end of `showPropertyStage` row assembly. It stably moves the configured `schedules` row (default `scheduled`, config order for multiples) to the front only when a real target defines priority — single tasks via the existing task context, counted/link sessions via aggregate `defined` states (so a mixed batch's empty `currentValue` still counts). All other rows keep order/identity; lane, refresh, and Cancel stay where they were, just shifted down. Non-task bullets, unprioritized tasks, and missing schedule rows keep the old order. Recommendation computation and all write paths are untouched.
- Tests: 10 new ordering cases in `test-navigation-hotkeys.cjs` (present/absent schedule, priority-first config, extra defined property, lane+refresh+cancel sequence, unconfigured/closed priority, filtering, `selectPropertyName` rebuild, `^prj`, mixed vs plain counted batches, Task Link sessions) and 4 immediate-`Ctrl+Enter` regressions in `test-navigation-roll-decay.cjs` (single, `^prj`, counted batch, link) asserting `visibleItems[0]`, `selectedIndex 0`, previewed date, Schedule Log, one undo group, and closure. One existing test asserting lane-first on a prioritized task was updated to the new contract.
- Docs/version: `docs/projects.md` describes the immediate flow; README and manifest bumped to 1.51.0 consistently.

Verification: `npm test` — 1199 pass, 0 fail; `npm run validate` — 6/6 plugins valid. `bob plugins sync --no-pull --plugin bob-navigation-hotkeys` deployed 2 files with backups preserved. Reload Obsidian plugins to pick up the new `main.js`. No GUI smoke check was possible here (no Obsidian in this environment) — worth one manual open of the picker on a prioritized task to confirm `scheduled` is selected, Enter opens dates, and `Ctrl+Enter` uses the displayed action.
