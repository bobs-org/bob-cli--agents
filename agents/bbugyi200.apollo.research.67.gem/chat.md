# Chat History - ace-run (research.67.gem)

- **TIMESTAMP:** 2026-11-25 08:04:50 EST
- **MODEL:** agy/gemini-4-neon-xhigh
- **AGENT:** research.67.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261125_074451.md`

## Prompt

%id(gem, clan=research.67)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.67.cdx`, `research.67.cld`, `research.67.grk`, `research.67.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I want to complete the work associated with the ^snoozed-tasks task in the ~/bob/bob.md
file.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
First run `sase repo open research -r "Write this research report"` and use the path it prints as `<research checkout>`. Write this research to a new markdown file under `<research checkout>/202611/`.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path under the opened research checkout and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

Completed the independent research report for `^snoozed-tasks`.

- **Report:** [snoozed_task_links_design__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_21/sase/repos/research/202611/snoozed_task_links_design__gem.md)
- **Registered Artifact:** `file:explicit:d0720a5fc050f8fa4d790621` (label `research:202611/snoozed_task_links_design__gem.md`, snapshot at [snoozed_task_links_design__gem-00d32a997e76.md](file:///home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261125074457/snoozed_task_links_design__gem-00d32a997e76.md))

### Verdict & Core Critique

**Yes—daily-note `## Snoozed` Task Links are a strong architectural fit for Bob**, specifically because they preserve sticky lanes (`[*]` Next / `[/]` WIP per `decisions:task-lanes-are-sticky`), keep Obsidian Tasks' `YYYY-MM-DD` `[scheduled::]` format intact (unlike using `^task-props-use-time` for same-day deferrals, which would force tasks to `[?]` Blocked), isolate cleanly from existing `## Pomodoros` parsers, inherit free vault-wide wikilink repair (`repair_links_in_note_with`), and degrade losslessly across midnight.

However, the raw task notes need **six justified adjustments** before implementation:

1. **Decouple Event Tasks from v1 (`A1`):** Treating Event Tasks as the v1 driver collides with four accepted decisions (`synced-meetings-link-by-phase`, `meet-filing-follows-google-until-edited`, `ended-off-clock-events-settle`, `past-day-sync-closes-bob-filed-meetings`), breaks early `=meet` starts, and duplicates what `## Events`, Mac Capture's `EventTimeRail`/`start_hint`, off-clock `max_links` exemption, and clock-aware timed closes already handle. Ship v1 strictly for **non-Event time-gated tasks** (e.g., emailing Dan after 3:30 PM; home tasks at 7:00 PM) and evaluate display-only far-future `MEET` folding or opt-in lead-time snoozing in v2.
2. **Dedicated 5m `bob snooze wake` child step in `bob tick` (`A2`):** `bob tick` is an orchestrator, not a vault mutator, and `tasks` reconcile runs every 15m (too slow). Register a daily-note-only `snooze` step at **5m cadence** ordered `gcal → snooze → tasks` that exits lock-free when nothing is due and otherwise writes via `task_status_hooks_write`; pair with instant manual wake gestures and Mac Capture `refresh_at` cues to cover the 0–5m cron window and MacBook sleep.
3. **Include `## Snoozed` in `Today` and daily on-clock `plan.max_links` (`A3`):** Keeping snoozed links inside `Today` removes them from `dash.md` `NEXT`/`READY` and the `]s` morning walk, protects R9 daily-note tasks, and prevents snoozing from becoming a budget-evasion loophole—while keeping them completely out of `## Pomodoros` lineups and `x`/`=` numbering.
4. **Use `z:<when>` in `bob capture`—never `s:<time>` (`A4`):** `parse_schedule_token` in `capture_language/markers.rs` already parses `s:1530` as **+1,530 days**. Use `z:1530`, `z:3:30pm`, `z:+2h`, and `config.yml` `snooze.presets` (`z:home`), plus `capture-complete` suggestions pulled from today's `## Events` end times (e.g., `15:30 (after Yogi interview)`).
5. **Full lifecycle parity & running-Pomodoro wake safety (`A5`):** Clean up `## Snoozed` on complete/cancel/block/release (`Alt+N`)/unlink (with safety pruning in `bob snooze wake` and `reconcile`), forbid simultaneous active + snoozed links, and **tail-append** woken links into an already-running target Pomodoro so existing `x` lineup indices never shift mid-session.
6. **Terminology clarity (`A6`):** Distinguish same-day **Snoozed Task Links** (`## Snoozed`) from the Reading Board's existing future-date `Snoozed` lane in `bob-ledger-tools`.

### Recommended Solution Summary

- **Vault format:** On-demand `## Snoozed` section placed **after** `## Pomodoros` (removed when emptied), sorted by bold 24-hour wake time with optional `— NAME` target override and preserved child notes: `- **1530** [[job#^email-dan-eod]]`.
- **CLI & `bob tick`:** Top-level `bob snooze wake` / `bob snooze list`, 5m `snooze` tick step, D7 typed placement via `routing::place`, and additive `snoozed[]` + `refresh_at` in `capture-pomodoros --tasks`.
- **Clients:** Extend `bob-ledger-tools` (`050-plan-budget.js`, `060-today.js`, `143-today-marks.js`), `block-id-prompt`/`task-status-cycler`/`bob-navigation-hotkeys` (cleanup + snooze/wake gestures), and `bob-mac-capture` (foldable `Snoozed` strip below `Later` with exact-minute `refresh_at` wake visibility).
- **Rollout:** Four incremental phases (Core CLI + `bob tick` → Capture grammar & presets → Obsidian plugins → Mac Capture), followed by an optional Phase 5 reassessment of Event Tasks and event-relative triggers after real-world usage.
