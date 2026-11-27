# Chat History - ace-run (bob-cli-q5.5.1.land--mon-4)

- **TIMESTAMP:** 2026-11-27 00:34:31 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-q5.5.1.land--mon-4

## Prompt

sase monitor start --command 'env TZ=UTC TMPDIR=/home/bryan/.cache/bob-cli-snooze-clock-render-fix/tmp DISPLAY=:999 OBSIDIAN_BIN=/home/bryan/.cache/bob-cli-snooze-clock-render-fix/obsidian-ozone-sized-debug node --require /home/bryan/.cache/bob-cli-snooze-clock-render-fix/retain-snooze-e2e-fixture.cjs scripts/obsidian-snooze-marks-e2e.cjs --out /home/bryan/.cache/bob-cli-snooze-clock-render-fix/screenshots-headless-final --report /home/bryan/.cache/bob-cli-snooze-clock-render-fix/report-headless-final.json' --reason 'Rerun real Obsidian snooze display acceptance after correcting the headless viewport and blocked-clock assertion'

## Response

sase tool run 6c59439a79a21af5aaa0e604ee0f2a83
PASS plugin-loaded (bob-ledger-tools)
PASS toggle-commands-registered (snooze=true today=true)
DEFKEYS [{"key":"job.md#sz-asleep","tone":"asleep","time":"08:03","visible":true,"surface":"live"},{"key":"job.md#sz-due","tone":"due","time":"04:48","visible":true,"surface":"live"},{"key":"job.md#sz-blocked","tone":"blocked","time":"04:48","visible":true,"surface":"live"}]
CACHE {"wakeDisabled":true,"ready":true,"date":"2026-11-27","nowMinutes":333,"nextWakeAt":"2026-11-27T04:48:00+00:00","planned":["job.md#^sz-asleep","job.md#^sz-blocked","job.md#^sz-due"],"blocked":["job.md#^sz-blocked"],"rows":[{"blockId":"sz-asleep","state":"asleep","line":19,"hhmm":"0803","target":"job","wokeAt":null,"history":false},{"blockId":"sz-due","state":"due","line":20,"hhmm":"0448","target":"job","wokeAt":null,"history":false},{"blockId":"sz-blocked","state":"blocked","line":21,"hhmm":"0448","target":"job","wokeAt":null,"history":false},{"blockId":"sz-ready","state":"ready","line":22,"hhmm":"0803","target":"job","wokeAt":null,"history":false},{"blockId":"sz-gone","state":"missing","line":23,"hhmm":"0803","target":"nope","wokeAt":null,"history":false},{"blockId":"sz-dup","state":"ambiguous","line":24,"hhmm":"0803","target":"job","wokeAt":null,"history":false},{"blockId":"sz-done","state":"done","line":25,"hhmm":"0803","target":"job","wokeAt":null,"history":false},{"blockId":"sz-woken","state":"woken","line":26,"hhmm":"0448","target":"job","wokeAt":"05:08","history":true},{"blockId":"sz-woken2","state":"woken","line":27,"hhmm":"0448","target":"job","wokeAt":"04:18","history":true}],"todayRank":["job.md#sz-woken","job.md#sz-woken2","job.md#sz-plain","2026/20261127.md#evt-running"]}
PASS wake-stubbed (wakeDisabled=true)
PASS lp-asleep-clock ({"key":"job.md#sz-asleep","time":"08:03","label":"08:03","tone":"asleep","aria":"Snoozed until 08:03 · in 2h 30m\nCtrl-click to open the Snoozed row","text":"","title":"","width":55.125,"height":16.3125,"fontSize":13.6,"rowLineHeight":24,"afterContent":"\"08:03\"","color":"color(srgb 0.49005 0.360796 0.791644)","beforeMask":"url(\"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBo)
PASS lp-due-clock ({"key":"job.md#sz-due","time":"04:48","label":"04:48 · due","tone":"due","aria":"Snoozed until 04:48 · due — waking\nCtrl-click to open the Snoozed row","text":"","title":"","width":90.265625,"height":16.3125,"fontSize":13.6,"rowLineHeight":24,"afterContent":"\"04:48 · due\"","color":"rgb(236, 117, 0)","beforeMask":"url(\"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24)
PASS lp-blocked-clock ({"key":"job.md#sz-blocked","time":"04:48","label":"04:48","tone":"blocked","aria":"Snoozed until 04:48 · waits on prerequisites\nCtrl-click to open the Snoozed row","text":"","title":"","width":55.125,"height":16.3125,"fontSize":13.6,"rowLineHeight":24,"afterContent":"\"04:48\"","color":"rgb(92, 92, 92)","beforeMask":"url(\"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 )
PASS lp-clock-single-line-width ([{"key":"job.md#sz-asleep","width":55.125,"height":16.3125,"rowLineHeight":24,"fontSize":13.6},{"key":"job.md#sz-due","width":90.265625,"height":16.3125,"rowLineHeight":24,"fontSize":13.6},{"key":"job.md#sz-blocked","width":55.125,"height":16.3125,"rowLineHeight":24,"fontSize":13.6}])
PASS lp-clock-state-colors (["color(srgb 0.49005 0.360796 0.791644)","rgb(236, 117, 0)","rgb(92, 92, 92)"])
PASS lp-clock-visible-labels ({"dueContent":"\"04:48 · due\"","asleepContent":"\"08:03\"","blockedContent":"\"04:48\""})
PASS lp-clock-masked-glyphs (["url(\"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='black' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Ccircle cx='12' cy='13' r='8'/%3E%3Cpath d='M12 9v4l2 2'/%3E%3Cpath d='M5 3 2 6'/%3E%3Cpath d='m22 6-3-3'/%3E%3Cpath d='M6.38 18.7 4 21')
PASS lp-neutral-sz-ready (null)
PASS lp-neutral-sz-dup (null)
PASS lp-neutral-sz-done (null)
PASS lp-neutral-missing (null)
PASS lp-tomato-regression (tomatoes=3)
PASS lp-no-tomato-on-snoozed (asleep keeps its clock, never both marks)
PASS theme-dark-repaints (marks=3)
PASS reading-asleep-clock ({"key":"job.md#sz-asleep","time":"08:03","label":"08:03","tone":"asleep","aria":"Snoozed until 08:03 · in 2h 30m\nCtrl-click to open the Snoozed row","text":"","title":"","width":55.125,"height":16.3125,"fontSize":13.6,"rowLineHeight":24,"afterContent":"\"08:03\"","color":"color(srgb 0.49005 0.360796 0.791644)","beforeMask":"url(\"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBo)
PASS reading-live-mark-hosts-match ([{"key":"job.md#sz-asleep","live":{"key":"job.md#sz-asleep","time":"08:03","label":"08:03","tone":"asleep","aria":"Snoozed until 08:03 · in 2h 30m\nCtrl-click to open the Snoozed row","text":"","title":"","width":55.125,"height":16.3125,"fontSize":13.6,"rowLineHeight":24,"afterContent":"\"08:03\"","color":"color(srgb 0.49005 0.360796 0.791644)","beforeMask":"url(\"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='black' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Ccircle cx='12' cy='13' r='8'/%3E%3Cpath d='M12 9v4l2 2'/%3E%3Cpath d='M5 3 2 6'/%3E%3Cpath d='m22 6-3-3'/%3E%3Cpath d='M6.38 18.7 4 21'/%3E%3Cpath d='M17.64 18.67 20 21'/%3E%3C/svg%3E\")","beforeBackground":"color(srgb 0.49005 0.360796 0.791644)","beforeFo)
PASS reading-clock-single-line-width ([{"key":"job.md#sz-asleep","width":55.125,"height":16.3125,"rowLineHeight":24,"fontSize":13.6},{"key":"job.md#sz-due","width":90.265625,"height":16.3125,"rowLineHeight":24,"fontSize":13.6},{"key":"job.md#sz-blocked","width":55.125,"height":16.3125,"rowLineHeight":24,"fontSize":13.6}])
PASS reading-tomato-stamps ({"stamped":7,"marks":[{"aria":"Today · queued in WRITE\nCtrl-click to open in today's note","visible":false,"context":""},{"aria":"Today · queued in WRITE\nCtrl-click to open in today's note","visible":false,"context":""},{"aria":"Today · queued in WRITE\nCtrl-click to open in today's note","visible":false,"context":""}]})
FAIL reading-tomato-regression: tomatoes=0
CHIPS [{"paint":"asleep","time":"08:03","status":"in 2h 30m","visible":true,"surface":"live","context":"- 0803 job#^sz-asleep"},{"paint":"due","time":"04:48","status":"due · waking","visible":true,"surface":"live","context":"- 0448 job#^sz-due"},{"paint":"blocked","time":"04:48","status":"waits on prerequisites","visible":true,"surface":"live","context":"- 0448 job#^sz-blocked"},{"paint":"ignored","time":"","status":"Ready — won't wake","visible":true,"surface":"live","context":"- 0803 job#^sz-ready"},{"paint":"ignored","time":"","status":"Missing — won't wake","visible":true,"surface":"live","context":"- 0803 nope#^sz-gone"},{"paint":"ignored","time":"","status":"Ambiguous — won't wake","visible":true,"surface":"live","context":"- 0803 job#^sz-dup"},{"paint":"ignored","time":"","status":"Done — won't wake","visible":true,"surface":"live","context":"- 0803 job#^sz-done"},{"paint":"history","time":"","status":"woke 05:08","visible":true,"surface":"live","context":"- 0448 job#^sz-woken · woke 05:08"},{"paint":"history","time":"","status":"woke 04:18","visible":true,"surface":"live","context":"- 0448 job#^sz-woken2 · woke 04:18"}]
PASS lp-woken-masked-glyphs (["url(\"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='black' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Ccircle cx='12' cy='13' r='8'/%3E%3Cpath d='M12 9v4l2 2'/%3E%3Cpath d='M5 3 2 6'/%3E%3Cpath d='m22 6-3-3'/%3E%3Cpath d='M6.38 18.7 4 21')
PASS lp-woken-fresh ({"pill":"fresh","text":"","aria":"Woke 05:08 (snoozed until 04:48, 20m late)\nCtrl-click to open the struck row","title":"","time":"05:08","line":"26","beforeMask":"url(\"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='black' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Ccircle cx='12' cy='13' r='8'/%3E%3Cpath d='M12 9v4l2)
PASS lp-woken-settled ({"pill":"settled","text":"","aria":"Woke 04:18 (snoozed until 04:48, 30m early)\nCtrl-click to open the struck row","title":"","time":"04:18","line":"27","beforeMask":"url(\"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='black' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Ccircle cx='12' cy='13' r='8'/%3E%3Cpath d='M12 9v)
PASS lp-row-asleep ([{"text":"","paint":"asleep","time":"08:03","status":"in 2h 30m","aria":"in 2h 30m","title":"","visible":true,"surface":"live","context":"- 0803 job#^sz-asleep"}])
PASS lp-row-due ([{"text":"","paint":"due","time":"04:48","status":"due · waking","aria":"due · waking","title":"","visible":true,"surface":"live","context":"- 0448 job#^sz-due"}])
PASS lp-row-blocked ([{"text":"","paint":"blocked","time":"04:48","status":"waits on prerequisites","aria":"waits on prerequisites","title":"","visible":true,"surface":"live","context":"- 0448 job#^sz-blocked"}])
PASS lp-row-ready (["Ready — won't wake","Missing — won't wake","Ambiguous — won't wake","Done — won't wake"])
PASS lp-row-missing (["Ready — won't wake","Missing — won't wake","Ambiguous — won't wake","Done — won't wake"])
PASS lp-row-ambiguous (["Ready — won't wake","Missing — won't wake","Ambiguous — won't wake","Done — won't wake"])
PASS lp-row-done (["Ready — won't wake","Missing — won't wake","Ambiguous — won't wake","Done — won't wake"])
PASS lp-row-history ([{"text":"","paint":"history","time":"","status":"woke 05:08","aria":"woke 05:08","title":"","visible":true,"surface":"live","context":"- 0448 job#^sz-woken · woke 05:08"},{"text":"","paint":"history","time":"","status":"woke 04:18","aria":"woke 04:18","title":"","visible":true,"surface":"live","context":"- 0448 job#^sz-woken2 · woke 04:18"}])
PASS lp-heading-summary (["1 asleep · 1 due · 1 blocked · next 04:48"])
PASS live-classify-state ({"file":"2026/20261127.md","err":null,"summary":"1 asleep · 1 due · 1 blocked · next 04:48","headerNumber":17,"rows":[[19,"asleep","0803"],[20,"due","0448"],[21,"blocked","0448"],[22,"ready","0803"],[23,"missing","0803"],[24,"ambiguous","0803"],[25,"done","0803"]]})
PASS live-heading-bisect ({"all":[{"aria":"1 asleep · 1 due · 1 blocked · next 04:48","summary":"1 asleep · 1 due · 1 blocked · next 04:48","visible":true,"surface":"live"}],"scoped":1})
PASS lp-event-time-regression (event-chips=1)
PASS lp-pill-marks-linked-task (["- job#^sz-woken","- job#^sz-woken2"])
PASS lp-pill-before-link ({"ok":true,"position":4})
PASS reading-dom-shape ({"ok":true,"parent":"DIV.el-h2","sibling":null,"lists":5})
PASS reading-woken-fresh ({"pill":"fresh","text":"","aria":"Woke 05:08 (snoozed until 04:48, 20m late)\nCtrl-click to open the struck row","title":"","time":"05:08","line":"26","beforeMask":"url(\"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='black' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Ccircle cx='12' cy='13' r='8'/%3E%3Cpath d='M12 9v4l2)
PASS reading-row-classes (["bob-snooze-row bob-snooze-row--asleep :: ","bob-snooze-row bob-snooze-row--due :: ","bob-snooze-row bob-snooze-row--blocked :: ","bob-snooze-row bob-snooze-row--ignored :: ","bob-snooze-row bob-snooze-row--ignored :: ","bob-snooze-row bob-snooze-row--ignored :: ","bob-snooze-row bob-snooze-row--ignored :: ","bob-snooze-row bob-snooze-row--history :: ","bob-snooze-row bob-snooze-row--history :: ")
PASS reading-row-history ([{"text":"","paint":"history","time":"","status":"woke 05:08","aria":"woke 05:08","title":"","visible":true,"surface":"reading","context":"0448 job > ^sz-woken · woke 05:08"},{"text":"","paint":"history","time":"","status":"woke 04:18","aria":"woke 04:18","title":"","visible":true,"surface":"reading)
PASS reading-heading-summary (["1 asleep · 1 due · 1 blocked · next 04:48"])
PASS lp-plan-chip ({"text":"3 · 04:48","aria":"3 snoozed · 1 due · 1 blocked · next wakes 04:48 · not counted in TODAY · 4/6 when all wake","title":"3 snoozed · 1 due · 1 blocked · next wakes 04:48 · not counted in TODAY · 4/6 when all wake","due":true,"glyphMask":"url(\"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='black' stroke-width='2' stroke-linecap='round')
PASS lp-plan-chip-masked-glyph ({"mask":"url(\"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='black' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Ccircle cx='12' cy='13' r='8'/%3E%3Cpath d='M12 9v4l2 2'/%3E%3Cpath d='M5 3 2 6'/%3E%3Cpath d='m22 6-3-3'/%3E%3Cpath d='M6.38 18.7 4 21'/%3E%3Cpath d='M17.64 18.67 20 21'/%3E%3C/svg%3E\")","background":"rgb(34, 34, 34)"})
PASS past-quiet-pill ([{"pill":"quiet","text":"","aria":"Woke 05:08 (snoozed until 05:08, on time)\nCtrl-click to open the struck row","title":"","time":"05:08","line":"11","beforeMask":"url(\"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='black' stroke-width='2' stroke-linecap='round' s)
PASS past-no-countdown (["",""])
PASS past-no-today-summary ([])
PASS hover-def-tooltip ({"tip":"Snoozed until 08:03 · in 2h 29m Ctrl-click to open the Snoozed row","aria":"Snoozed until 08:03 · in 2h 29m\nCtrl-click to open the Snoozed row"})
PASS hover-woken-tooltip ({"tip":"Woke 05:08 (snoozed until 04:48, 20m late) Ctrl-click to open the struck row","aria":"Woke 05:08 (snoozed until 04:48, 20m late)\nCtrl-click to open the struck row"})
PASS passive-render-no-write (4adca4a153e09f9d 20f91c1ceb6dba07 91836d14e3a6f87b 80ed715192c5ad6b)
PASS line-height-baseline (snoozed=50.375 plain=26.375 (content differs; see toggle pair))
PASS narrow-no-hscroll ({"overflowX":0,"clientWidth":124})
PASS reduced-motion-keeps-marks (marks=3)
PASS forced-colors-keeps-definition-glyphs ([{"background":"rgb(0, 0, 0)","adjust":"none"},{"background":"rgb(0, 0, 0)","adjust":"none"},{"background":"rgb(0, 0, 0)","adjust":"none"}])
PASS forced-colors-keeps-pills (pills=2)
PASS forced-colors-keeps-woken-glyphs ([{"background":"rgb(0, 0, 0)","adjust":"none"},{"background":"rgb(0, 0, 0)","adjust":"none"}])
PASS forced-colors-keeps-plan-glyph ({"mask":"url(\"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='black' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Ccircle cx='12' cy='13' r='8'/%3E%3Cpath d='M12 9v4l2 2'/%3E%3Cpath d='M5 3 2 6'/%3E%3Cpath d='m22 6-3-3'/%3E%3Cpath d='M6.38 18.7 4 21'/%3E%3Cpath d='M17.64 18.67 20 21'/%3E%3C/svg%3E\")","background":"rgb(0, 0, 0)","adjust":"none"})
PASS toggle-off-command ({"ok":true})
PASS toggle-hides-clocks (marks=0)
PASS toggle-hides-pills (pills=0)
PASS toggle-hides-rows (chips=0)
PASS toggle-keeps-meter (chips=1 text=3 · 04:48)
PASS toggle-row-height-unchanged (on=50.375 off=50.375)
PASS toggle-restores-marks (marks=3)
PASS today-toggle-hides-clocks (marks=0)
PASS today-toggle-restores (marks=3)
PASS plain-click-no-write (4adca4a153e09f9d 20f91c1ceb6dba07 91836d14e3a6f87b 80ed715192c5ad6b vs 4adca4a153e09f9d 20f91c1ceb6dba07 91836d14e3a6f87b 80ed715192c5ad6b)
PASS plain-click-keeps-editor ({"ok":true,"line":2,"ch":12,"text":"- [*] #task Asleep alpha with a deliberately long title that keeps going past an","focused":true})
PASS mod-click-opens-daily ({"active":"2026/20261127.md","cursor":{"line":18,"ch":17}})
PASS mod-click-lands-on-row (cursor={"line":18,"ch":17})
PASS woken-mod-click-lands-on-history (cursor={"line":25,"ch":0})
PASS plan-chip-reaches-heading ({"active":"2026/20261127.md","cursor":{"line":16,"ch":0}})
PASS live-retime-edit-applied ({"ok":true})
PASS live-retime-to-due (["due:due · waking","due:due · waking","blocked:waits on prerequisites","ignored:Ready — won't wake","ignored:Missing — won't wake","ignored:Ambiguous — won't wake","ignored:Done — won't wake","history:woke 05:08","history:woke 04:18"])
PASS live-link-edit-applied ({"ok":true})
PASS live-link-wins-over-clock (["job.md#sz-due","job.md#sz-blocked"])
PASS wake-to-tomato (tomatoes=1)
PASS live-delete-edit-applied ({"ok":true})
PASS live-delete-removes-paint (["","","","","","","",""])
PASS no-renderer-errors ([])
PASS no-duplicate-hosts ([])
{
  "pass": false,
  "failed": [
    "reading-tomato-regression"
  ],
  "skipped": [],
  "screenshots": [
    "/home/bryan/.cache/bob-cli-snooze-clock-render-fix/screenshots-headless-final/e2e-snooze-marks-live-light.png",
    "/home/bryan/.cache/bob-cli-snooze-clock-render-fix/screenshots-headless-final/e2e-snooze-marks-live-dark.png",
    "/home/bryan/.cache/bob-cli-snooze-clock-render-fix/screenshots-headless-final/e2e-snooze-marks-daily-light.png",
    "/home/bryan/.cache/bob-cli-snooze-clock-render-fix/screenshots-headless-final/e2e-snooze-marks-daily-dark.png",
    "/home/bryan/.cache/bob-cli-snooze-clock-render-fix/screenshots-headless-final/e2e-snooze-marks-rows.png",
    "/home/bryan/.cache/bob-cli-snooze-clock-render-fix/screenshots-headless-final/e2e-snooze-marks-rows-dark.png",
    "/home/bryan/.cache/bob-cli-snooze-clock-render-fix/screenshots-headless-final/e2e-snooze-marks-reading-light.png",
    "/home/bryan/.cache/bob-cli-snooze-clock-render-fix/screenshots-headless-final/e2e-snooze-marks-reading-dark.png",
    "/home/bryan/.cache/bob-cli-snooze-clock-render-fix/screenshots-headless-final/e2e-snooze-marks-plan.png",
    "/home/bryan/.cache/bob-cli-snooze-clock-render-fix/screenshots-headless-final/e2e-snooze-marks-hover.png",
    "/home/bryan/.cache/bob-cli-snooze-clock-render-fix/screenshots-headless-final/e2e-snooze-marks-narrow.png",
    "/home/bryan/.cache/bob-cli-snooze-clock-render-fix/screenshots-headless-final/e2e-snooze-marks-a11y.png"
  ],
  "out": "/home/bryan/.cache/bob-cli-snooze-clock-render-fix/screenshots-headless-final"
}
Preserved E2E fixture at /home/bryan/.cache/bob-cli-snooze-clock-render-fix/tmp/snooze-e2e-retained-3170619
Error: e2e failed: reading-tomato-regression
    at fail (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/obsidian-snooze-marks-e2e.cjs:88:17)
    at runE2e (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/obsidian-snooze-marks-e2e.cjs:1713:23)
    at async main (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/obsidian-snooze-marks-e2e.cjs:1754:3)
failed  exit=1  duration=67051ms

