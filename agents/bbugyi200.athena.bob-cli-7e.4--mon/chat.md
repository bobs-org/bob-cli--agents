# Chat History - ace-run (bob-cli-7e.4--mon)

- **TIMESTAMP:** 2026-10-13 11:55:08 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-7e.4--mon

## Prompt

sase monitor start --command 'npm test' --reason 'Run the full bob-plugins verification suite for the assigned BLOCKS chips phase'

## Response

sase tool run c81d6069672d9a586ca1be582d7a9f6a

> bob-plugins@0.1.0 test
> node scripts/build-plugins.mjs --check && node --test scripts/test-dependency-line-migration.cjs scripts/test-navigation-hotkeys-section-nav.cjs scripts/test-navigation-hotkeys-schedule-recovery.cjs scripts/test-navigation-hotkeys-schedule-properties.cjs scripts/test-navigation-hotkeys-schedule-writes.cjs scripts/test-navigation-hotkeys-runtime-schedule.cjs scripts/test-navigation-hotkeys-dependencies.cjs scripts/test-navigation-hotkeys-dependency-mirror.cjs scripts/test-navigation-hotkeys-task-move-plan.cjs scripts/test-navigation-hotkeys-priority-notice.cjs scripts/test-navigation-successor-picker.cjs scripts/test-navigation-hotkeys-unblocked-notice.cjs scripts/test-navigation-project-blocking.cjs scripts/test-navigation-project-dependency-stage.cjs scripts/test-navigation-project-subprojects.cjs scripts/test-navigation-project-subtree-gestures.cjs scripts/test-navigation-hotkeys-priority-picker.cjs scripts/test-navigation-hotkeys-picker-lifecycle.cjs scripts/test-navigation-hotkeys-ref-picker-text.cjs scripts/test-navigation-hotkeys-pomodoro-move-pickers.cjs scripts/test-navigation-inbox-route.cjs scripts/test-navigation-inbox-route-card.cjs scripts/test-navigation-hotkeys-task-move.cjs scripts/test-navigation-goto-task-uri.cjs scripts/test-navigation-hotkeys-open-task-jump.cjs scripts/test-navigation-hotkeys-vim-counts.cjs scripts/test-navigation-hotkeys-tab-pin.cjs scripts/test-navigation-hotkeys-schedule-log.cjs scripts/test-navigation-hotkeys-schedule-review.cjs scripts/test-navigation-hotkeys-deferred-pomodoro.cjs scripts/test-navigation-hotkeys-pomodoro-parse.cjs scripts/test-navigation-hotkeys-pomodoro-bullet-move.cjs scripts/test-navigation-hotkeys-pomodoro-split-rename.cjs scripts/test-navigation-hotkeys-pomodoro-reorder.cjs scripts/test-navigation-hotkeys-runtime-prune.cjs scripts/test-navigation-hotkeys-project-from-task.cjs scripts/test-navigation-hotkeys-project-reversal.cjs scripts/test-navigation-hotkeys-link-picker.cjs scripts/test-navigation-hotkeys-lane-toggle.cjs scripts/test-navigation-hotkeys-task-link-lane.cjs scripts/test-navigation-hotkeys-cancel-log.cjs scripts/test-navigation-hotkeys-cancel-task.cjs scripts/test-navigation-hotkeys-forward-promotion.cjs scripts/test-navigation-hotkeys-schedule-work-log.cjs scripts/test-navigation-hotkeys-task-move-history.cjs scripts/test-navigation-jump-history.cjs scripts/test-navigation-dependencies.cjs scripts/test-navigation-roll-decay.cjs scripts/test-navigation-decay-planner.cjs scripts/test-navigation-task-card-model.cjs scripts/test-navigation-task-card-view.cjs scripts/test-navigation-task-card-schedule.cjs scripts/test-navigation-task-card-review.cjs scripts/test-navigation-decision-card.cjs scripts/test-navigation-decision-card-handlers.cjs scripts/test-navigation-refresh-modal.cjs scripts/test-navigation-freshness.cjs scripts/test-navigation-stamps.cjs scripts/test-navigation-keep-counting.cjs scripts/test-navigation-checklist.cjs scripts/test-navigation-review-advance.cjs scripts/test-navigation-review-advance-gestures.cjs scripts/test-navigation-checklist-ctrl-enter.cjs scripts/test-ledger-tools-navigation.cjs scripts/test-ledger-tools-plan-budget.cjs scripts/test-ledger-tools-ready-badge.cjs scripts/test-ledger-tools-note-ready.cjs scripts/test-ledger-tools-note-ready-views.cjs scripts/test-ledger-tools-dashboard-parity.cjs scripts/test-ledger-tools-work-badge-tone.cjs scripts/test-ledger-tools-dashboard-collections.cjs scripts/test-ledger-tools-today.cjs scripts/test-ledger-tools-freshness-placement.cjs scripts/test-ledger-tools-freshness-states.cjs scripts/test-ledger-tools-freshness-namespace.cjs scripts/test-ledger-tools-freshness-review-model.cjs scripts/test-ledger-tools-freshness-queue.cjs scripts/test-ledger-tools-freshness-tracking.cjs scripts/test-ledger-tools-freshness-footer.cjs scripts/test-ledger-tools-freshness-recurring.cjs scripts/test-ledger-tools-freshness-mark.cjs scripts/test-ledger-tools-freshness-mark-surfaces.cjs scripts/test-ledger-tools-priority-marks.cjs scripts/test-ledger-tools-task-tag-marks.cjs scripts/test-ledger-tools-unblocked-glyph.cjs scripts/test-ledger-tools-progress-marks.cjs scripts/test-ledger-tools-date-marks.cjs scripts/test-ledger-tools-date-marks-tasks.cjs scripts/test-ledger-tools-freshness-keeps.cjs scripts/test-ledger-tools-freshness-unblocked.cjs scripts/test-ledger-tools-freshness-decision-card.cjs scripts/test-ledger-tools-dependency-chips.cjs scripts/test-ledger-tools-blocks-chips.cjs scripts/test-ledger-tools-snippets.cjs scripts/test-ledger-tools-vim-mappings.cjs scripts/test-task-status-cycler-dependencies.cjs scripts/test-task-status-cycler-ctrl-enter.cjs scripts/test-task-status-cycler-reference-lifecycle.cjs scripts/test-task-status-cycler-pomodoro-completion.cjs scripts/test-task-status-cycler-pomodoro-work-log.cjs scripts/test-task-status-cycler-pomodoro-reopen.cjs scripts/test-task-status-cycler-blocked-schedule.cjs scripts/test-task-status-cycler-demotion-picker.cjs scripts/test-task-status-cycler-promotion.cjs scripts/test-task-status-cycler-successors.cjs scripts/test-task-status-cycler-successor-wiring.cjs scripts/test-task-status-cycler-successor-polish.cjs scripts/test-task-status-cycler-successor-offers.cjs scripts/test-task-status-cycler-project-pull-in.cjs scripts/test-task-status-cycler-task-links-api.cjs scripts/test-task-status-cycler-task-link-lane.cjs scripts/test-task-status-cycler-freshness.cjs scripts/test-block-id-prompt-dependencies.cjs scripts/test-block-id-prompt-ref-picker-text.cjs scripts/test-block-id-prompt-markers.cjs scripts/test-block-id-prompt-pomodoro-context.cjs scripts/test-block-id-prompt-target-update.cjs scripts/test-block-id-prompt-pomodoro-insertion.cjs scripts/test-block-id-prompt-pomodoro-targets.cjs scripts/test-block-id-prompt-pomodoro-picker-view.cjs scripts/test-block-id-prompt-pomodoro-picker-runtime.cjs scripts/test-block-id-prompt-work-log.cjs scripts/test-block-id-prompt-pomodoro-link-runtime.cjs scripts/test-block-id-prompt-pomodoro-unlink-runtime.cjs scripts/test-block-id-prompt-task-link-deletion.cjs scripts/test-block-id-prompt-plan-budget-and-freshness.cjs scripts/test-prompt-block-id-naming.cjs scripts/test-block-id-prompt-prefill.cjs scripts/test-vim-surround.cjs scripts/test-navigation-dependencies-stage-ranker-and-pool.cjs scripts/test-navigation-dependencies-stage-entry-and-view.cjs scripts/test-navigation-dependencies-stage-writes.cjs scripts/test-navigation-dependencies-stage-mirror-and-badge.cjs scripts/test-navigation-dependencies-stage-stale-guards.cjs scripts/test-navigation-dependencies-stage-performance.cjs scripts/test-navigation-prompt-block-id-stage.cjs scripts/test-navigation-dependencies-writer.cjs scripts/test-plugin-build.cjs scripts/test-ledger-tools-stats-journal.cjs scripts/test-ledger-tools-stats-data.cjs scripts/test-ledger-tools-stats-block.cjs scripts/test-ledger-tools-stats-charts.cjs scripts/test-navigation-review-journal.cjs scripts/test-ledger-tools-stats-panels.cjs

  checked   block-id-prompt
  checked   bob-ledger-tools
  checked   bob-navigation-hotkeys
  checked   task-status-cycler
TAP version 13
# Subtest: explicit task IDs exclusively own dependency lookup
ok 1 - explicit task IDs exclusively own dependency lookup
  ---
  duration_ms: 3.032749
  ...
# Subtest: legacy tasks without an id field still fall back to their block ID
ok 2 - legacy tasks without an id field still fall back to their block ID
  ---
  duration_ms: 0.304712
  ...
# Subtest: blocked-link consumption raises open prerequisites and leaves the dependent blocked
ok 3 - blocked-link consumption raises open prerequisites and leaves the dependent blocked
  ---
  duration_ms: 1.161748
  ...
# Subtest: project-blocked member consumption promotes the project's open prerequisite
ok 4 - project-blocked member consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.674728
  ...
# Subtest: project-blocked resident consumption promotes the project's open prerequisite
ok 5 - project-blocked resident consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.412377
  ...
# Subtest: a tagged inherited ^prj target is refused with its parent named
ok 6 - a tagged inherited ^prj target is refused with its parent named
  ---
  duration_ms: 0.365167
  ...
# Subtest: project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
ok 7 - project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
  ---
  duration_ms: 1.301966
  ...
# Subtest: project date refusal applies only when the date is the sole project reason
ok 8 - project date refusal applies only when the date is the sole project reason
  ---
  duration_ms: 0.321544
  ...
# Subtest: a project-blocked tag is token-bounded and ignored on lookalike tags
ok 9 - a project-blocked tag is token-bounded and ignored on lookalike tags
  ---
  duration_ms: 0.393582
  ...
# Subtest: task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
ok 10 - task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
  ---
  duration_ms: 0.693454
  ...
# Subtest: task blocked state unifies status and dependency reasons
ok 11 - task blocked state unifies status and dependency reasons
  ---
  duration_ms: 0.349427
  ...
# Subtest: task picker partition sinks blocked tasks while preserving group order
ok 12 - task picker partition sinks blocked tasks while preserving group order
  ---
  duration_ms: 0.200553
  ...
# Subtest: blocked chip labels show useful unmet dependency counts
ok 13 - blocked chip labels show useful unmet dependency counts
  ---
  duration_ms: 0.098669
  ...
# Subtest: blocked tooltips explain dependency and status-only reasons
ok 14 - blocked tooltips explain dependency and status-only reasons
  ---
  duration_ms: 0.247402
  ...
# Subtest: task status classes cover every open task status
ok 15 - task status classes cover every open task status
  ---
  duration_ms: 0.124328
  ...
# Subtest: Blocked tasks remain unmet dependency targets
ok 16 - Blocked tasks remain unmet dependency targets
  ---
  duration_ms: 0.189301
  ...
# Subtest: blocked task count covers both reasons without double-counting
ok 17 - blocked task count covers both reasons without double-counting
  ---
  duration_ms: 0.15197
  ...
# Subtest: single caret relocation preserves embedding and removes aliases
ok 18 - single caret relocation preserves embedding and removes aliases
  ---
  duration_ms: 1.706357
  ...
# Subtest: single caret relocation resets aliased block links
ok 19 - single caret relocation resets aliased block links
  ---
  duration_ms: 0.242543
  ...
# Subtest: single caret relocation strips heading and block subpaths
ok 20 - single caret relocation strips heading and block subpaths
  ---
  duration_ms: 0.260678
  ...
# Subtest: task picker normalizes every supported wiki block-link form
ok 21 - task picker normalizes every supported wiki block-link form
  ---
  duration_ms: 0.674568
  ...
# Subtest: three or more carets never trigger the task picker
ok 22 - three or more carets never trigger the task picker
  ---
  duration_ms: 0.154124
  ...
# Subtest: rapid aliased task picker completion preserves the alias
ok 23 - rapid aliased task picker completion preserves the alias
  ---
  duration_ms: 2.525651
  ...
# Subtest: task picker recognition is independent of Markdown source context
ok 24 - task picker recognition is independent of Markdown source context
  ---
  duration_ms: 0.774739
  ...
# Subtest: task picker recognition respects cursor proximity and fenced code
ok 25 - task picker recognition respects cursor proximity and fenced code
  ---
  duration_ms: 0.256018
  ...
# Subtest: plan budget suffix: link Notice appends the meter computed on post-write daily content
ok 26 - plan budget suffix: link Notice appends the meter computed on post-write daily content
  ---
  duration_ms: 6.57457
  ...
# Subtest: plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
ok 27 - plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
  ---
  duration_ms: 0.928833
  ...
# Subtest: plan budget suffix: unlink Notice marks an over-cap plan with 🔴
ok 28 - plan budget suffix: unlink Notice marks an over-cap plan with 🔴
  ---
  duration_ms: 2.369523
  ...
# Subtest: plan budget suffix: Next task without a block ID prompts for one and omits the meter
ok 29 - plan budget suffix: Next task without a block ID prompts for one and omits the meter
  ---
  duration_ms: 0.401627
  ...
# Subtest: plan budget suffix: Task Link Notice appends the meter from post-write daily content
ok 30 - plan budget suffix: Task Link Notice appends the meter from post-write daily content
  ---
  duration_ms: 2.008835
  ...
# Subtest: plan budget suffix: Task Link Notice omits the meter when no daily note takes part
ok 31 - plan budget suffix: Task Link Notice omits the meter when no daily note takes part
  ---
  duration_ms: 0.546022
  ...
# Subtest: planTargetTaskUpdate stamps the rewritten line last via injected stamper
ok 32 - planTargetTaskUpdate stamps the rewritten line last via injected stamper
  ---
  duration_ms: 0.28266
  ...
# Subtest: planTargetTaskUpdate without a stamper never stamps (identity default)
ok 33 - planTargetTaskUpdate without a stamper never stamps (identity default)
  ---
  duration_ms: 0.146319
  ...
# Subtest: planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
ok 34 - planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
  ---
  duration_ms: 0.340901
  ...
# Subtest: planTargetTaskUpdate stamps a Next task that gains a block ID
ok 35 - planTargetTaskUpdate stamps a Next task that gains a block ID
  ---
  duration_ms: 0.478283
  ...
# Subtest: planTargetTaskUpdate tolerates a throwing stamper
ok 36 - planTargetTaskUpdate tolerates a throwing stamper
  ---
  duration_ms: 0.226873
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 37 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.614814
  ...
# Subtest: dedicated-link helpers reject Depends-On lines
ok 38 - dedicated-link helpers reject Depends-On lines
  ---
  duration_ms: 0.322886
  ...
# Subtest: Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
ok 39 - Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
  ---
  duration_ms: 0.311846
  ...
# Subtest: malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
ok 40 - malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
  ---
  duration_ms: 0.126281
  ...
# Subtest: Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
ok 41 - Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
  ---
  duration_ms: 0.21499
  ...
# Subtest: Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
ok 42 - Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
  ---
  duration_ms: 0.207476
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent
ok 43 - readPlanBudgetMeter keeps per-cap over flags independent
  ---
  duration_ms: 0.191836
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent (mirror)
ok 44 - readPlanBudgetMeter keeps per-cap over flags independent (mirror)
  ---
  duration_ms: 0.096584
  ...
# Subtest: block-id-prompt freshness accessors degrade without ledger-tools
ok 45 - block-id-prompt freshness accessors degrade without ledger-tools
  ---
  duration_ms: 0.198599
  ...
# Subtest: list item body bounds trim whitespace and reject empty bullets
ok 46 - list item body bounds trim whitespace and reject empty bullets
  ---
  duration_ms: 1.412607
  ...
# Subtest: Pomodoro activation eligibility requires a sole-content sub-bullet
ok 47 - Pomodoro activation eligibility requires a sole-content sub-bullet
  ---
  duration_ms: 2.00164
  ...
# Subtest: Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
ok 48 - Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
  ---
  duration_ms: 0.279834
  ...
# Subtest: Pomodoro source context distinguishes ledger ancestry and open state
ok 49 - Pomodoro source context distinguishes ledger ancestry and open state
  ---
  duration_ms: 0.452193
  ...
# Subtest: future cleanup touches only later open Pomodoros and counts duplicates
ok 50 - future cleanup touches only later open Pomodoros and counts duplicates
  ---
  duration_ms: 1.239837
  ...
# Subtest: cleanup resolves aliases, embeds, same-note links, and alternate paths
ok 51 - cleanup resolves aliases, embeds, same-note links, and alternate paths
  ---
  duration_ms: 2.123213
  ...
# Subtest: dedicated bullet subtree cleanup preserves CRLF line endings
ok 52 - dedicated bullet subtree cleanup preserves CRLF line endings
  ---
  duration_ms: 0.364606
  ...
# Subtest: existing-ID task completion prunes future links in the source editor
ok 53 - existing-ID task completion prunes future links in the source editor
  ---
  duration_ms: 2.355587
  ...
# Subtest: new-ID same-file completion plans cleanup after the task edit
ok 54 - new-ID same-file completion plans cleanup after the task edit
  ---
  duration_ms: 1.25195
  ...
# Subtest: findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
ok 55 - findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
  ---
  duration_ms: 1.969059
  ...
# Subtest: findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
ok 56 - findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
  ---
  duration_ms: 0.170235
  ...
# Subtest: findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
ok 57 - findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
  ---
  duration_ms: 0.180455
  ...
# Subtest: todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
ok 58 - todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
  ---
  duration_ms: 0.542676
  ...
# Subtest: todayDailyPath honors a custom Daily Notes format and an empty folder
ok 59 - todayDailyPath honors a custom Daily Notes format and an empty folder
  ---
  duration_ms: 0.228145
  ...
# Subtest: formatDailyDate resolves bracketed literal text alongside date tokens
ok 60 - formatDailyDate resolves bracketed literal text alongside date tokens
  ---
  duration_ms: 0.123796
  ...
# Subtest: getDailyNotesOptions reads the daily-notes core plugin's configured options
ok 61 - getDailyNotesOptions reads the daily-notes core plugin's configured options
  ---
  duration_ms: 1.61363
  ...
# Subtest: computeFencedLineFlags marks opening and closing fence lines and everything between
ok 62 - computeFencedLineFlags marks opening and closing fence lines and everything between
  ---
  duration_ms: 0.260838
  ...
# Subtest: selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
ok 63 - selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
  ---
  duration_ms: 0.887995
  ...
# Subtest: selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
ok 64 - selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
  ---
  duration_ms: 0.463144
  ...
# Subtest: selectPomodoroInsertionTarget rejects more than one open timed entry
ok 65 - selectPomodoroInsertionTarget rejects more than one open timed entry
  ---
  duration_ms: 0.214499
  ...
# Subtest: selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
ok 66 - selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
  ---
  duration_ms: 0.193209
  ...
# Subtest: findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
ok 67 - findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
  ---
  duration_ms: 0.187117
  ...
# Subtest: planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
ok 68 - planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
  ---
  duration_ms: 1.213216
  ...
# Subtest: planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
ok 69 - planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
  ---
  duration_ms: 0.618431
  ...
# Subtest: planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
ok 70 - planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
  ---
  duration_ms: 0.223286
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
ok 71 - planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
  ---
  duration_ms: 0.47684
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
ok 72 - planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
  ---
  duration_ms: 0.464948
  ...
# Subtest: planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
ok 73 - planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
  ---
  duration_ms: 0.327996
  ...
# Subtest: planPomodoroLinkInsertion inserts before the separator preceding later content
ok 74 - planPomodoroLinkInsertion inserts before the separator preceding later content
  ---
  duration_ms: 0.254656
  ...
# Subtest: planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
ok 75 - planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
  ---
  duration_ms: 0.307517
  ...
# Subtest: planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
ok 76 - planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
  ---
  duration_ms: 0.259706
  ...
# Subtest: existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
ok 77 - existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
  ---
  duration_ms: 2.991761
  ...
# Subtest: same-note Pomodoro link runtime composes the task update with adjacent insertion
ok 78 - same-note Pomodoro link runtime composes the task update with adjacent insertion
  ---
  duration_ms: 1.143894
  ...
# Subtest: new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
ok 79 - new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
  ---
  duration_ms: 0.592411
  ...
# Subtest: planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
ok 80 - planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
  ---
  duration_ms: 0.18844
  ...
# Subtest: all-open cleanup removes current and future links while preserving history and unresolved links
ok 81 - all-open cleanup removes current and future links while preserving history and unresolved links
  ---
  duration_ms: 0.596168
  ...
# Subtest: all-open cleanup treats missing section, no open entries, and no matches as no-op successes
ok 82 - all-open cleanup treats missing section, no open entries, and no matches as no-op successes
  ---
  duration_ms: 0.18343
  ...
# Subtest: Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
ok 83 - Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
  ---
  duration_ms: 2.663475
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor requires a single cursor
ok 84 - resolvePomodoroLinkTaskFromEditor requires a single cursor
  ---
  duration_ms: 0.350339
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
ok 85 - resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
  ---
  duration_ms: 0.377701
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
ok 86 - resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
  ---
  duration_ms: 0.428999
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
ok 87 - resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
  ---
  duration_ms: 0.520123
  ...
# Subtest: blocked-link consumption reports dependency reasons before the project date
ok 88 - blocked-link consumption reports dependency reasons before the project date
  ---
  duration_ms: 2.625221
  ...
# Subtest: Pomodoro link checks do not read other notes for a non-Blocked task
ok 89 - Pomodoro link checks do not read other notes for a non-Blocked task
  ---
  duration_ms: 0.291787
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
ok 90 - resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
  ---
  duration_ms: 0.354196
  ...
# Subtest: task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
ok 91 - task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
  ---
  duration_ms: 5.115736
  ...
# Subtest: task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
ok 92 - task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
  ---
  duration_ms: 1.611897
  ...
# Subtest: task-mode toggle: linked only under a completed Pomodoro links again
ok 93 - task-mode toggle: linked only under a completed Pomodoro links again
  ---
  duration_ms: 0.732589
  ...
# Subtest: task-mode toggle: a task without a block ID is never linked and prompts for one
ok 94 - task-mode toggle: a task without a block ID is never linked and prompts for one
  ---
  duration_ms: 0.377992
  ...
# Subtest: existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
ok 95 - existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
  ---
  duration_ms: 1.070273
  ...
# Subtest: forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
ok 96 - forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
  ---
  duration_ms: 0.503451
  ...
# Subtest: new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
ok 97 - new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
  ---
  duration_ms: 0.472341
  ...
# Subtest: submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
ok 98 - submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
  ---
  duration_ms: 0.160907
  ...
# Subtest: submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
ok 99 - submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
  ---
  duration_ms: 0.176297
  ...
# Subtest: same-note Pomodoro link runtime: task and ledger edits merge into one transaction
ok 100 - same-note Pomodoro link runtime: task and ledger edits merge into one transaction
  ---
  duration_ms: 1.240177
  ...
# Subtest: linking an already-linked Ready task raises it to Next without duplicating the link
ok 101 - linking an already-linked Ready task raises it to Next without duplicating the link
  ---
  duration_ms: 0.535752
  ...
# Subtest: Next task without a block ID preflights the picker before prompting
ok 102 - Next task without a block ID preflights the picker before prompting
  ---
  duration_ms: 0.479675
  ...
# Subtest: Pomodoro link stops before any mutation when today's daily note is missing
ok 103 - Pomodoro link stops before any mutation when today's daily note is missing
  ---
  duration_ms: 0.171608
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
ok 104 - Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
  ---
  duration_ms: 0.448787
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
ok 105 - Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
  ---
  duration_ms: 0.281698
  ...
# Subtest: Pomodoro link aborts without any write when the task line changed since it was selected
ok 106 - Pomodoro link aborts without any write when the task line changed since it was selected
  ---
  duration_ms: 0.153253
  ...
# Subtest: Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
ok 107 - Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
  ---
  duration_ms: 0.626947
  ...
# Subtest: canceling the Pomodoro block-ID modal leaves the note untouched
ok 108 - canceling the Pomodoro block-ID modal leaves the note untouched
  ---
  duration_ms: 0.181737
  ...
# Subtest: review-walk: existing-ID link hands its Linked notice to continue with no separate notice
ok 109 - review-walk: existing-ID link hands its Linked notice to continue with no separate notice
  ---
  duration_ms: 0.790749
  ...
# Subtest: review-walk: prompted-ID link continues after submit
ok 110 - review-walk: prompted-ID link continues after submit
  ---
  duration_ms: 0.977356
  ...
# Subtest: review-walk: prompt cancel settles with null
ok 111 - review-walk: prompt cancel settles with null
  ---
  duration_ms: 0.138644
  ...
# Subtest: review-walk: BUSY swallows the key with no write
ok 112 - review-walk: BUSY swallows the key with no write
  ---
  duration_ms: 0.240408
  ...
# Subtest: review-walk: failed link keeps its notice and settles with null
ok 113 - review-walk: failed link keeps its notice and settles with null
  ---
  duration_ms: 0.214309
  ...
# Subtest: review-walk: partial link keeps its notice and never continues with an outcome
ok 114 - review-walk: partial link keeps its notice and never continues with an outcome
  ---
  duration_ms: 0.641124
  ...
# Subtest: inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
ok 115 - inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
  ---
  duration_ms: 0.207096
  ...
# Subtest: inbox-route: non-inbox notes and task-link mode never prompt
ok 116 - inbox-route: non-inbox notes and task-link mode never prompt
  ---
  duration_ms: 0.637617
  ...
# Subtest: inbox-route: cancel writes nothing and settles once
ok 117 - inbox-route: cancel writes nothing and settles once
  ---
  duration_ms: 0.429329
  ...
# Subtest: inbox-route: stay matches today
ok 118 - inbox-route: stay matches today
  ---
  duration_ms: 0.45587
  ...
# Subtest: inbox-route: move links, then moves, with one composed toast and a route continue
ok 119 - inbox-route: move links, then moves, with one composed toast and a route continue
  ---
  duration_ms: 1.406375
  ...
# Subtest: inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
ok 120 - inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
  ---
  duration_ms: 0.611247
  ...
# Subtest: inbox-route: a move failure gives the partial notice plus a link-today continue
ok 121 - inbox-route: a move failure gives the partial notice plus a link-today continue
  ---
  duration_ms: 0.417266
  ...
# Subtest: review-walk: no nav or nav v2 keeps today's notices
ok 122 - review-walk: no nav or nav v2 keeps today's notices
  ---
  duration_ms: 0.739261
  ...
# Subtest: inbox-route: source drift during route prompt refuses without writes
ok 123 - inbox-route: source drift during route prompt refuses without writes
  ---
  duration_ms: 0.28816
  ...
# Subtest: inbox-route: block-ID route cancel returns sentinel and settles null once
ok 124 - inbox-route: block-ID route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.292408
  ...
# Subtest: inbox-route: link no-op with move never commits
ok 125 - inbox-route: link no-op with move never commits
  ---
  duration_ms: 0.170255
  ...
# Subtest: picker opens only on the link direction, never on unlink
ok 126 - picker opens only on the link direction, never on unlink
  ---
  duration_ms: 7.635686
  ...
# Subtest: picker never opens in task-link mode
ok 127 - picker never opens in task-link mode
  ---
  duration_ms: 2.164942
  ...
# Subtest: Depends-On refusals never open the picker
ok 128 - Depends-On refusals never open the picker
  ---
  duration_ms: 1.641554
  ...
# Subtest: preflight refusals open nothing
ok 129 - preflight refusals open nothing
  ---
  duration_ms: 0.441563
  ...
# Subtest: picking a non-default entry links there
ok 130 - picking a non-default entry links there
  ---
  duration_ms: 1.099239
  ...
# Subtest: cancel writes nothing with no Notice and settles the walk null
ok 131 - cancel writes nothing with no Notice and settles the walk null
  ---
  duration_ms: 0.681351
  ...
# Subtest: a no-ID task gets picker, then the block-ID prompt with the target carried
ok 132 - a no-ID task gets picker, then the block-ID prompt with the target carried
  ---
  duration_ms: 0.90097
  ...
# Subtest: inbox order is picker, then route, then write
ok 133 - inbox order is picker, then route, then write
  ---
  duration_ms: 0.781752
  ...
# Subtest: a review-walk landing continues with link-today and the new text
ok 134 - a review-walk landing continues with link-today and the new text
  ---
  duration_ms: 0.963008
  ...
# Subtest: an all-closed ledger creates a new entry after the last completed block
ok 135 - an all-closed ledger creates a new entry after the last completed block
  ---
  duration_ms: 1.218076
  ...
# Subtest: several running entries allow an explicit pick
ok 136 - several running entries allow an explicit pick
  ---
  duration_ms: 0.676512
  ...
# Subtest: a target that changed before commit refuses with no writes
ok 137 - a target that changed before commit refuses with no writes
  ---
  duration_ms: 0.464407
  ...
# Subtest: a target that closed before commit refuses with no writes
ok 138 - a target that closed before commit refuses with no writes
  ---
  duration_ms: 0.355108
  ...
# Subtest: the task note being the daily note uses one editor transaction
ok 139 - the task note being the daily note uses one editor transaction
  ---
  duration_ms: 0.55488
  ...
# Subtest: promptOpen blocks re-entry while the picker is open
ok 140 - promptOpen blocks re-entry while the picker is open
  ---
  duration_ms: 9.069824
  ...
# Subtest: header shows title, subtitle, lane chip per status, and block-ID chip
ok 141 - header shows title, subtitle, lane chip per status, and block-ID chip
  ---
  duration_ms: 7.817463
  ...
# Subtest: rows render in document order with the default selected
ok 142 - rows render in document order with the default selected
  ---
  duration_ms: 0.912962
  ...
# Subtest: running row shows progress fraction and minutes-left meta
ok 143 - running row shows progress fraction and minutes-left meta
  ---
  duration_ms: 0.869489
  ...
# Subtest: unnamed entries render muted italic
ok 144 - unnamed entries render muted italic
  ---
  duration_ms: 0.409892
  ...
# Subtest: filtering ranks, highlights, and clearing restores the default
ok 145 - filtering ranks, highlights, and clearing restores the default
  ---
  duration_ms: 1.03731
  ...
# Subtest: create row meta, divider, and theme badge
ok 146 - create row meta, divider, and theme badge
  ---
  duration_ms: 1.47774
  ...
# Subtest: exact open names suppress the create row; prefix matches keep it
ok 147 - exact open names suppress the create row; prefix matches keep it
  ---
  duration_ms: 0.609763
  ...
# Subtest: theme badge turns red over cap; a throwing budget hides the detail
ok 148 - theme badge turns red over cap; a throwing budget hides the detail
  ---
  duration_ms: 2.012712
  ...
# Subtest: invalid rows explain the grammar and are inert on Enter
ok 149 - invalid rows explain the grammar and are inert on Enter
  ---
  duration_ms: 9.562585
  ...
# Subtest: multiple running entries show the banner, no pills, and block creation
ok 150 - multiple running entries show the banner, no pills, and block creation
  ---
  duration_ms: 1.359145
  ...
# Subtest: navigation wraps and skips non-selectable rows
ok 151 - navigation wraps and skips non-selectable rows
  ---
  duration_ms: 1.275535
  ...
# Subtest: empty state invites planning a Pomodoro
ok 152 - empty state invites planning a Pomodoro
  ---
  duration_ms: 0.246741
  ...
# Subtest: footer hints and plan meter
ok 153 - footer hints and plan meter
  ---
  duration_ms: 0.895029
  ...
# Subtest: Enter chooses the selected row; click chooses that row
ok 154 - Enter chooses the selected row; click chooses that row
  ---
  duration_ms: 0.546332
  ...
# Subtest: Shift+Enter creates; an exact open name links there instead
ok 155 - Shift+Enter creates; an exact open name links there instead
  ---
  duration_ms: 0.677623
  ...
# Subtest: Ctrl+Shift+Enter commits exactly like Enter
ok 156 - Ctrl+Shift+Enter commits exactly like Enter
  ---
  duration_ms: 1.454546
  ...
# Subtest: Escape and Ctrl+[ cancel with no choice; settle-once holds
ok 157 - Escape and Ctrl+[ cancel with no choice; settle-once holds
  ---
  duration_ms: 0.657846
  ...
# Subtest: canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
ok 158 - canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
  ---
  duration_ms: 1.890659
  ...
# Subtest: canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
ok 159 - canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
  ---
  duration_ms: 0.549369
  ...
# Subtest: pomodoroLinkSelectorSlug mirrors capture slugs
ok 160 - pomodoroLinkSelectorSlug mirrors capture slugs
  ---
  duration_ms: 0.345039
  ...
# Subtest: parsePomodoroEntryParts reads canonical and legacy entry lines
ok 161 - parsePomodoroEntryParts reads canonical and legacy entry lines
  ---
  duration_ms: 0.950695
  ...
# Subtest: collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
ok 162 - collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
  ---
  duration_ms: 2.206062
  ...
# Subtest: collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
ok 163 - collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
  ---
  duration_ms: 0.908684
  ...
# Subtest: collectPomodoroLinkEntries counts links but excludes struck references
ok 164 - collectPomodoroLinkEntries counts links but excludes struck references
  ---
  duration_ms: 0.404923
  ...
# Subtest: collectPomodoroLinkEntries falls back to range text and position titles
ok 165 - collectPomodoroLinkEntries falls back to range text and position titles
  ---
  duration_ms: 0.1785
  ...
# Subtest: pomodoroRunProgress reports fractions, overtime, and midnight wrap
ok 166 - pomodoroRunProgress reports fractions, overtime, and midnight wrap
  ---
  duration_ms: 0.598793
  ...
# Subtest: buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
ok 167 - buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
  ---
  duration_ms: 0.792723
  ...
# Subtest: buildPomodoroLinkPickerRows keeps the create row for prefix matches
ok 168 - buildPomodoroLinkPickerRows keeps the create row for prefix matches
  ---
  duration_ms: 0.344758
  ...
# Subtest: buildPomodoroLinkPickerRows marks completed-only names as again
ok 169 - buildPomodoroLinkPickerRows marks completed-only names as again
  ---
  duration_ms: 0.163422
  ...
# Subtest: buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
ok 170 - buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
  ---
  duration_ms: 0.346421
  ...
# Subtest: buildPomodoroLinkPickerRows matches times, positions, and block IDs
ok 171 - buildPomodoroLinkPickerRows matches times, positions, and block IDs
  ---
  duration_ms: 0.504513
  ...
# Subtest: resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
ok 172 - resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
  ---
  duration_ms: 0.303219
  ...
# Subtest: defaultPomodoroLinkChoice returns the default entry or null
ok 173 - defaultPomodoroLinkChoice returns the default entry or null
  ---
  duration_ms: 0.250428
  ...
# Subtest: planExplicitPomodoroLinkInsertion links under a chosen existing entry
ok 174 - planExplicitPomodoroLinkInsertion links under a chosen existing entry
  ---
  duration_ms: 1.030838
  ...
# Subtest: planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
ok 175 - planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
  ---
  duration_ms: 0.260026
  ...
# Subtest: planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
ok 176 - planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
  ---
  duration_ms: 0.689156
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after the running entry
ok 177 - planExplicitPomodoroLinkInsertion creates after the running entry
  ---
  duration_ms: 0.448336
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
ok 178 - planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
  ---
  duration_ms: 0.42994
  ...
# Subtest: planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
ok 179 - planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
  ---
  duration_ms: 0.17801
  ...
# Subtest: planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
ok 180 - planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
  ---
  duration_ms: 0.296486
  ...
# Subtest: planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
ok 181 - planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
  ---
  duration_ms: 0.282189
  ...
# Subtest: buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
ok 182 - buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
  ---
  duration_ms: 0.171457
  ...
# Subtest: buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
ok 183 - buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
  ---
  duration_ms: 0.155517
  ...
# Subtest: planExplicitPomodoroLinkInsertion matches mixed-case raced open names
ok 184 - planExplicitPomodoroLinkInsertion matches mixed-case raced open names
  ---
  duration_ms: 0.288791
  ...
# Subtest: buildPomodoroLinkPickerRows bounds \#N position matches
ok 185 - buildPomodoroLinkPickerRows bounds \#N position matches
  ---
  duration_ms: 0.329459
  ...
# Subtest: planPomodoroLinkInsertion without a target keeps today's behavior and shape
ok 186 - planPomodoroLinkInsertion without a target keeps today's behavior and shape
  ---
  duration_ms: 0.362582
  ...
# Subtest: direct unlink without a daily note keeps the Next lane and reports it
ok 187 - direct unlink without a daily note keeps the Next lane and reports it
  ---
  duration_ms: 2.230619
  ...
# Subtest: In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
ok 188 - In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
  ---
  duration_ms: 0.426575
  ...
# Subtest: In Progress unlink with a summary keeps the lane and creates a Work Log
ok 189 - In Progress unlink with a summary keeps the lane and creates a Work Log
  ---
  duration_ms: 1.190743
  ...
# Subtest: In Progress unlink revalidates task text and block-ID uniqueness at confirmation
ok 190 - In Progress unlink revalidates task text and block-ID uniqueness at confirmation
  ---
  duration_ms: 0.295133
  ...
# Subtest: Next task unlink removes current and future links and keeps the Next lane
ok 191 - Next task unlink removes current and future links and keeps the Next lane
  ---
  duration_ms: 3.238561
  ...
# Subtest: In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
ok 192 - In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
  ---
  duration_ms: 0.666522
  ...
# Subtest: same-note Next unlink merges the Work Log and all-open cleanup in the active editor
ok 193 - same-note Next unlink merges the Work Log and all-open cleanup in the active editor
  ---
  duration_ms: 0.602931
  ...
# Subtest: same-note In Progress unlink merges cleanup and Work Log in the active editor
ok 194 - same-note In Progress unlink merges cleanup and Work Log in the active editor
  ---
  duration_ms: 0.478593
  ...
# Subtest: Next unlink stops before any write when daily cleanup write is stale
ok 195 - Next unlink stops before any write when daily cleanup write is stale
  ---
  duration_ms: 0.58687
  ...
# Subtest: Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
ok 196 - Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
  ---
  duration_ms: 0.857437
  ...
# Subtest: In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
ok 197 - In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
  ---
  duration_ms: 0.572663
  ...
# Subtest: review-walk: unlink settles with null and keeps its notice
ok 198 - review-walk: unlink settles with null and keeps its notice
  ---
  duration_ms: 1.148853
  ...
# Subtest: inbox-route: unlink cancel writes nothing
ok 199 - inbox-route: unlink cancel writes nothing
  ---
  duration_ms: 0.338446
  ...
# Subtest: inbox-route: unlink stay matches today and never commits
ok 200 - inbox-route: unlink stay matches today and never commits
  ---
  duration_ms: 0.478413
  ...
# Subtest: inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
ok 201 - inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.533599
  ...
# Subtest: inbox-route: In Progress unlink with a Work summary routes
ok 202 - inbox-route: In Progress unlink with a Work summary routes
  ---
  duration_ms: 0.493092
  ...
# Subtest: inbox-route: unlink move failure gives the partial notice and stays
ok 203 - inbox-route: unlink move failure gives the partial notice and stays
  ---
  duration_ms: 0.254185
  ...
# Subtest: inbox-route: non-inbox unlink never prompts
ok 204 - inbox-route: non-inbox unlink never prompts
  ---
  duration_ms: 0.246491
  ...
# Subtest: review-walk: Work-summary unlink path retains origin until submit
ok 205 - review-walk: Work-summary unlink path retains origin until submit
  ---
  duration_ms: 0.26172
  ...
# Subtest: inbox-route: unlink source drift during route prompt refuses without writes
ok 206 - inbox-route: unlink source drift during route prompt refuses without writes
  ---
  duration_ms: 0.221022
  ...
# Subtest: inbox-route: Work-summary route cancel returns sentinel and settles null once
ok 207 - inbox-route: Work-summary route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.222375
  ...
# Subtest: inbox-route: unlink no-op with move never commits
ok 208 - inbox-route: unlink no-op with move never commits
  ---
  duration_ms: 0.197357
  ...
# Subtest: direct-add seeds from the task headline, not non-task blocks
ok 209 - direct-add seeds from the task headline, not non-task blocks
  ---
  duration_ms: 3.570817
  ...
# Subtest: link-task-complete seeds from the target, prefers open buffers
ok 210 - link-task-complete seeds from the target, prefers open buffers
  ---
  duration_ms: 0.899798
  ...
# Subtest: link-task-complete reports stale and unreadable targets
ok 211 - link-task-complete reports stale and unreadable targets
  ---
  duration_ms: 0.293199
  ...
# Subtest: pomodoro link seeds after the choice from the cursor task
ok 212 - pomodoro link seeds after the choice from the cursor task
  ---
  duration_ms: 0.262962
  ...
# Subtest: marker rename suggests from the unique task, never hiding ambiguity
ok 213 - marker rename suggests from the unique task, never hiding ambiguity
  ---
  duration_ms: 0.532056
  ...
# Subtest: modal seeds the value, selects once, and never overwrites typing
ok 214 - modal seeds the value, selects once, and never overwrites typing
  ---
  duration_ms: 1.178449
  ...
# Subtest: modal disables Save while loading and survives close/reopen
ok 215 - modal disables Save while loading and survives close/reopen
  ---
  duration_ms: 2.004045
  ...
# Subtest: submit revalidates: occupied IDs and stale tasks fail editable
ok 216 - submit revalidates: occupied IDs and stale tasks fail editable
  ---
  duration_ms: 0.50274
  ...
# Subtest: cancelling writes no ID and explicit renames keep the current ID
ok 217 - cancelling writes no ID and explicit renames keep the current ID
  ---
  duration_ms: 0.677253
  ...
# Subtest: the task picker drops the paired \#ref and prefixes the book
ok 218 - the task picker drops the paired \#ref and prefixes the book
  ---
  duration_ms: 2.548634
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 219 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.310002
  ...
# Subtest: calendar date parsing rejects malformed width and impossible dates
ok 220 - calendar date parsing rejects malformed width and impossible dates
  ---
  duration_ms: 1.585416
  ...
# Subtest: future scheduled field detection respects the yesterday/today/tomorrow boundary
ok 221 - future scheduled field detection respects the yesterday/today/tomorrow boundary
  ---
  duration_ms: 0.435171
  ...
# Subtest: scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
ok 222 - scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
  ---
  duration_ms: 0.967447
  ...
# Subtest: planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
ok 223 - planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
  ---
  duration_ms: 0.928643
  ...
# Subtest: planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
ok 224 - planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
  ---
  duration_ms: 0.203168
  ...
# Subtest: planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
ok 225 - planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
  ---
  duration_ms: 0.165606
  ...
# Subtest: planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
ok 226 - planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
  ---
  duration_ms: 0.149335
  ...
# Subtest: planTargetTaskUpdate leaves today and past schedules untouched
ok 227 - planTargetTaskUpdate leaves today and past schedules untouched
  ---
  duration_ms: 0.278542
  ...
# Subtest: planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
ok 228 - planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
  ---
  duration_ms: 0.34582
  ...
# Subtest: two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
ok 229 - two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
  ---
  duration_ms: 0.478984
  ...
# Subtest: a malformed single scheduled field is never treated as future
ok 230 - a malformed single scheduled field is never treated as future
  ---
  duration_ms: 0.177509
  ...
# Subtest: an ambiguous scheduled field does not block the legacy Ready promotion
ok 231 - an ambiguous scheduled field does not block the legacy Ready promotion
  ---
  duration_ms: 0.173722
  ...
# Subtest: planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
ok 232 - planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
  ---
  duration_ms: 0.127172
  ...
# Subtest: Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
ok 233 - Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
  ---
  duration_ms: 0.454417
  ...
# Subtest: Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
ok 234 - Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
  ---
  duration_ms: 0.156639
  ...
# Subtest: planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
ok 235 - planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
  ---
  duration_ms: 0.240369
  ...
# Subtest: planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
ok 236 - planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
  ---
  duration_ms: 0.12582
  ...
# Subtest: planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
ok 237 - planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.107015
  ...
# Subtest: planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
ok 238 - planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
  ---
  duration_ms: 0.126582
  ...
# Subtest: planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
ok 239 - planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
  ---
  duration_ms: 0.123686
  ...
# Subtest: planTargetTaskUpdate preserves a trailing newline when one was already present
ok 240 - planTargetTaskUpdate preserves a trailing newline when one was already present
  ---
  duration_ms: 0.135328
  ...
# Subtest: planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
ok 241 - planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
  ---
  duration_ms: 0.103267
  ...
# Subtest: planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
ok 242 - planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
  ---
  duration_ms: 0.164034
  ...
# Subtest: planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
ok 243 - planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
  ---
  duration_ms: 0.126241
  ...
# Subtest: existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
ok 244 - existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
  ---
  duration_ms: 3.028291
  ...
# Subtest: new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
ok 245 - new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
  ---
  duration_ms: 0.754821
  ...
# Subtest: activation runtime aborts without any write when the target preimage goes stale
ok 246 - activation runtime aborts without any write when the target preimage goes stale
  ---
  duration_ms: 0.404863
  ...
# Subtest: same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
ok 247 - same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
  ---
  duration_ms: 1.410182
  ...
# Subtest: same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
ok 248 - same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
  ---
  duration_ms: 0.557474
  ...
# Subtest: a source marker edited after a successful existing-ID target write reports an accurate partial notice
ok 249 - a source marker edited after a successful existing-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.468654
  ...
# Subtest: a source marker edited after a successful new-ID target write reports an accurate partial notice
ok 250 - a source marker edited after a successful new-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.464817
  ...
# Subtest: planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
ok 251 - planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
  ---
  duration_ms: 0.160837
  ...
# Subtest: planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
ok 252 - planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
  ---
  duration_ms: 0.10478
  ...
# Subtest: planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
ok 253 - planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
  ---
  duration_ms: 0.118336
  ...
# Subtest: planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
ok 254 - planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.10478
  ...
# Subtest: direct Task Links raise ^prj while never pulling its date forward
ok 255 - direct Task Links raise ^prj while never pulling its date forward
  ---
  duration_ms: 0.121362
  ...
# Subtest: task-link selection: one link is selectable from any column, several are chosen by cursor
ok 256 - task-link selection: one link is selectable from any column, several are chosen by cursor
  ---
  duration_ms: 2.606666
  ...
# Subtest: task-link selection ignores picker/rename markers, plain links, and Markdown-style links
ok 257 - task-link selection ignores picker/rename markers, plain links, and Markdown-style links
  ---
  duration_ms: 0.317025
  ...
# Subtest: dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
ok 258 - dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
  ---
  duration_ms: 1.478101
  ...
# Subtest: inline Task Link deletion removes the token with its decoration and collapses whitespace
ok 259 - inline Task Link deletion removes the token with its decoration and collapses whitespace
  ---
  duration_ms: 0.630724
  ...
# Subtest: dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
ok 260 - dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
  ---
  duration_ms: 0.831377
  ...
# Subtest: mergeCoveringEdits keeps the covering edit and the earlier of identical edits
ok 261 - mergeCoveringEdits keeps the covering edit and the earlier of identical edits
  ---
  duration_ms: 0.20393
  ...
# Subtest: dependency transclusion detection needs an embedded sole-content child of a \#task line
ok 262 - dependency transclusion detection needs an embedded sole-content child of a \#task line
  ---
  duration_ms: 0.431203
  ...
# Subtest: Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
ok 263 - Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
  ---
  duration_ms: 3.584263
  ...
# Subtest: Task Link on a Next target works from an embedded aliased link outside any Pomodoro
ok 264 - Task Link on a Next target works from an embedded aliased link outside any Pomodoro
  ---
  duration_ms: 0.908844
  ...
# Subtest: same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
ok 265 - same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
  ---
  duration_ms: 0.890109
  ...
# Subtest: same-note Task Link deletion clamps the restored cursor to the shortened note
ok 266 - same-note Task Link deletion clamps the restored cursor to the shortened note
  ---
  duration_ms: 0.417497
  ...
# Subtest: a cleanup subtree that covers a nested selected link wins and links are not double counted
ok 267 - a cleanup subtree that covers a nested selected link wins and links are not double counted
  ---
  duration_ms: 0.647426
  ...
# Subtest: Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
ok 268 - Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
  ---
  duration_ms: 1.375014
  ...
# Subtest: Task Link on an In Progress target with a blank summary logs nothing
ok 269 - Task Link on an In Progress target with a blank summary logs nothing
  ---
  duration_ms: 0.518009
  ...
# Subtest: canceling the In Progress Task Link prompt leaves everything untouched
ok 270 - canceling the In Progress Task Link prompt leaves everything untouched
  ---
  duration_ms: 0.274023
  ...
# Subtest: canceling the In Progress unlink prompt in task mode leaves everything untouched
ok 271 - canceling the In Progress unlink prompt in task mode leaves everything untouched
  ---
  duration_ms: 0.548076
  ...
# Subtest: In Progress Task Link submit revalidates the link line and the target task
ok 272 - In Progress Task Link submit revalidates the link line and the target task
  ---
  duration_ms: 0.763047
  ...
# Subtest: Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
ok 273 - Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
  ---
  duration_ms: 0.72274
  ...
# Subtest: Task Link on a Done or Cancelled target is refused without edits
ok 274 - Task Link on a Done or Cancelled target is refused without edits
  ---
  duration_ms: 0.353906
  ...
# Subtest: Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
ok 275 - Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
  ---
  duration_ms: 0.920076
  ...
# Subtest: precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
ok 276 - precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
  ---
  duration_ms: 1.237392
  ...
# Subtest: Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
ok 277 - Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
  ---
  duration_ms: 0.324981
  ...
# Subtest: Task Link that is a sub-task dependency transclusion is refused without edits
ok 278 - Task Link that is a sub-task dependency transclusion is refused without edits
  ---
  duration_ms: 0.23051
  ...
# Subtest: Task Link partial failure after the daily write is retryable
ok 279 - Task Link partial failure after the daily write is retryable
  ---
  duration_ms: 0.645582
  ...
# Subtest: Task Link stops before any write when the target note changes after planning
ok 280 - Task Link stops before any write when the target note changes after planning
  ---
  duration_ms: 0.626987
  ...
# Subtest: Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
ok 281 - Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
  ---
  duration_ms: 0.387209
  ...
# Subtest: Task Link subtree deletion removes a nested target task without any status write
ok 282 - Task Link subtree deletion removes a nested target task without any status write
  ---
  duration_ms: 0.265096
  ...
# Subtest: work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
ok 283 - work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
  ---
  duration_ms: 1.459546
  ...
# Subtest: work log date helpers use local calendar components
ok 284 - work log date helpers use local calendar components
  ---
  duration_ms: 0.250017
  ...
# Subtest: planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
ok 285 - planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
  ---
  duration_ms: 0.662956
  ...
# Subtest: planWorkLogInsertion inherits an existing space-indented child prefix
ok 286 - planWorkLogInsertion inherits an existing space-indented child prefix
  ---
  duration_ms: 0.488322
  ...
# Subtest: planWorkLogInsertion inherits an existing tab-indented child prefix
ok 287 - planWorkLogInsertion inherits an existing tab-indented child prefix
  ---
  duration_ms: 0.228336
  ...
# Subtest: planWorkLogInsertion prepends newest-first entries into existing marker spellings
ok 288 - planWorkLogInsertion prepends newest-first entries into existing marker spellings
  ---
  duration_ms: 0.474566
  ...
# Subtest: planWorkLogInsertion ignores nested child-task markers and preserves CRLF
ok 289 - planWorkLogInsertion ignores nested child-task markers and preserves CRLF
  ---
  duration_ms: 0.35094
  ...
# Subtest: planWorkLogInsertion treats blank summaries as no-op structural edits
ok 290 - planWorkLogInsertion treats blank summaries as no-op structural edits
  ---
  duration_ms: 0.130229
  ...
# Subtest: the Open-reset planner is removed: unlink plans only a Work Log insertion
ok 291 - the Open-reset planner is removed: unlink plans only a Work Log insertion
  ---
  duration_ms: 0.294622
  ...
# Subtest: unlink Work Log plan keeps the In Progress checkbox and appends one entry
ok 292 - unlink Work Log plan keeps the In Progress checkbox and appends one entry
  ---
  duration_ms: 0.400214
  ...
# Subtest: folds embed, struck, and plain legacy children into one canonical line
ok 293 - folds embed, struck, and plain legacy children into one canonical line
  ---
  duration_ms: 132.371892
  ...
# Subtest: legacy-label row links come first, then legacy children in order
ok 294 - legacy-label row links come first, then legacy children in order
  ---
  duration_ms: 1.877985
  ...
# Subtest: R2 adopts field-only open dependents; unadoptable ids stay warned
ok 295 - R2 adopts field-only open dependents; unadoptable ids stay warned
  ---
  duration_ms: 0.640612
  ...
# Subtest: closed dependents gain the line but keep the field untouched
ok 296 - closed dependents gain the line but keep the field untouched
  ---
  duration_ms: 1.076645
  ...
# Subtest: open dependents drop stale field ids and stamp targets missing [id::]
ok 297 - open dependents drop stale field ids and stamp targets missing [id::]
  ---
  duration_ms: 0.569708
  ...
# Subtest: unresolved links stay verbatim and keep field ids as breadcrumbs
ok 298 - unresolved links stay verbatim and keep field ids as breadcrumbs
  ---
  duration_ms: 0.51366
  ...
# Subtest: leaves \#^ref embeds, non-task parents, fences, and conflict children alone
ok 299 - leaves \#^ref embeds, non-task parents, fences, and conflict children alone
  ---
  duration_ms: 0.77554
  ...
# Subtest: malformed rows leave the whole dependent alone
ok 300 - malformed rows leave the whole dependent alone
  ---
  duration_ms: 0.527968
  ...
# Subtest: R9 deletes label-only rows and removes the open field
ok 301 - R9 deletes label-only rows and removes the open field
  ---
  duration_ms: 0.63946
  ...
# Subtest: cross-note links use the shortest unambiguous form
ok 302 - cross-note links use the shortest unambiguous form
  ---
  duration_ms: 0.985762
  ...
# Subtest: ambiguous basenames fall back to the full path
ok 303 - ambiguous basenames fall back to the full path
  ---
  duration_ms: 0.491698
  ...
# Subtest: duplicate ids are ambiguous and fatal for --write
ok 304 - duplicate ids are ambiguous and fatal for --write
  ---
  duration_ms: 0.241421
  ...
# Subtest: archive targets keep the done/ path and are never stamped
ok 305 - archive targets keep the done/ path and are never stamped
  ---
  duration_ms: 0.271198
  ...
# Subtest: self links stay on the line but are not projected
ok 306 - self links stay on the line but are not projected
  ---
  duration_ms: 0.352513
  ...
# Subtest: non-task targets stay on the line but are not projected
ok 307 - non-task targets stay on the line but are not projected
  ---
  duration_ms: 0.258914
  ...
# Subtest: preserves CRLF, missing final newline, and cancel-log position
ok 308 - preserves CRLF, missing final newline, and cancel-log position
  ---
  duration_ms: 0.678405
  ...
# Subtest: migration is idempotent
ok 309 - migration is idempotent
  ---
  duration_ms: 1.044915
  ...
# Subtest: parseArgs handles --vault, --write, --help, and rejects unknowns
ok 310 - parseArgs handles --vault, --write, --help, and rejects unknowns
  ---
  duration_ms: 0.636214
  ...
# Subtest: BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
ok 311 - BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
  ---
  duration_ms: 3.482479
  ...
# Subtest: reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
ok 312 - reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
  ---
  duration_ms: 2.888464
  ...
# Subtest: stale, missing, canonical append, and frozen-owner models (BC8-BC10)
ok 313 - stale, missing, canonical append, and frozen-owner models (BC8-BC10)
  ---
  duration_ms: 0.611788
  ...
# Subtest: Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
ok 314 - Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
  ---
  duration_ms: 7.182982
  ...
# Subtest: budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
ok 315 - budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
  ---
  duration_ms: 1.307426
  ...
# Subtest: chip builder includes the 🔑 badge and has no edit controls
ok 316 - chip builder includes the 🔑 badge and has no edit controls
  ---
  duration_ms: 0.426134
  ...
# Subtest: collections namespace version is additive v1
ok 317 - collections namespace version is additive v1
  ---
  duration_ms: 1.254516
  ...
# Subtest: collection chip classes stay collection-specific through paint and refresh
ok 318 - collection chip classes stay collection-specific through paint and refresh
  ---
  duration_ms: 3.355144
  ...
# Subtest: projects: scalar resolved links count, lists never widen
ok 319 - projects: scalar resolved links count, lists never widen
  ---
  duration_ms: 0.4351
  ...
# Subtest: projects: templates, status, and containsAny edges
ok 320 - projects: templates, status, and containsAny edges
  ---
  duration_ms: 0.390776
  ...
# Subtest: references: exact prefix, md only, exact scalar status
ok 321 - references: exact prefix, md only, exact scalar status
  ---
  duration_ms: 0.274404
  ...
# Subtest: base contracts: accept current files, reject drift, tolerate presentation
ok 322 - base contracts: accept current files, reject drift, tolerate presentation
  ---
  duration_ms: 0.674257
  ...
# Subtest: entries: true zero vs unavailable with reason, failure isolation
ok 323 - entries: true zero vs unavailable with reason, failure isolation
  ---
  duration_ms: 0.24628
  ...
# Subtest: snapshot counts both collections once, true zero stays clickable
ok 324 - snapshot counts both collections once, true zero stays clickable
  ---
  duration_ms: 0.37206
  ...
# Subtest: snapshot never presents partial counts as final
ok 325 - snapshot never presents partial counts as final
  ---
  duration_ms: 0.374314
  ...
# Subtest: changed definitions fail closed per collection, never stale
ok 326 - changed definitions fail closed per collection, never stale
  ---
  duration_ms: 0.471029
  ...
# Subtest: renderChip links, labels, and cleans up per component
ok 327 - renderChip links, labels, and cleans up per component
  ---
  duration_ms: 0.575369
  ...
# Subtest: PENDING section excludes TODAY while the whole lane keeps it
ok 328 - PENDING section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 3.351147
  ...
# Subtest: NEXT section excludes TODAY while the whole lane keeps it
ok 329 - NEXT section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 0.449408
  ...
# Subtest: NEXT uses symbol *, not name matching
ok 330 - NEXT uses symbol *, not name matching
  ---
  duration_ms: 0.28825
  ...
# Subtest: READY badge and query agree on hide and path case variants
ok 331 - READY badge and query agree on hide and path case variants
  ---
  duration_ms: 0.595005
  ...
# Subtest: blocked uses the full list even outside the visible subset
ok 332 - blocked uses the full list even outside the visible subset
  ---
  duration_ms: 0.217365
  ...
# Subtest: duplicate block IDs, missing IDs, and reused objects stay per-row
ok 333 - duplicate block IDs, missing IDs, and reused objects stay per-row
  ---
  duration_ms: 0.260868
  ...
# Subtest: READY gating keeps exempt rows and drops NEW/ROTTEN
ok 334 - READY gating keeps exempt rows and drops NEW/ROTTEN
  ---
  duration_ms: 0.304141
  ...
# Subtest: throwing Today degrades to unavailable, never zero
ok 335 - throwing Today degrades to unavailable, never zero
  ---
  duration_ms: 6.225214
  ...
# Subtest: dashboard badges color the displayed section count and label whole-lane pressure
ok 336 - dashboard badges color the displayed section count and label whole-lane pressure
  ---
  duration_ms: 0.690788
  ...
# Subtest: dashboard section warning boundaries ignore TODAY-only whole-lane excess
ok 337 - dashboard section warning boundaries ignore TODAY-only whole-lane excess
  ---
  duration_ms: 0.823602
  ...
# Subtest: dashboard lane badge keeps unavailable data neutral
ok 338 - dashboard lane badge keeps unavailable data neutral
  ---
  duration_ms: 3.060852
  ...
# Subtest: dashboard lane paint and refresh keep color aligned with the visible section
ok 339 - dashboard lane paint and refresh keep color aligned with the visible section
  ---
  duration_ms: 2.961483
  ...
# Subtest: dashboard lane widgets refresh together and prune on unload
ok 340 - dashboard lane widgets refresh together and prune on unload
  ---
  duration_ms: 3.004886
  ...
# Subtest: daily paint matches dashboard section badges on screenshot fixtures
ok 341 - daily paint matches dashboard section badges on screenshot fixtures
  ---
  duration_ms: 30.318054
  ...
# Subtest: daily and dashboard membership agree for exclusions and custom IN_PROGRESS
ok 342 - daily and dashboard membership agree for exclusions and custom IN_PROGRESS
  ---
  duration_ms: 9.065665
  ...
# Subtest: daily paint refreshes with dashboard when Today, lane, and cap change
ok 343 - daily paint refreshes with dashboard when Today, lane, and cap change
  ---
  duration_ms: 9.113897
  ...
# Subtest: older daily notes follow today's dashboard lanes
ok 344 - older daily notes follow today's dashboard lanes
  ---
  duration_ms: 3.239473
  ...
# Subtest: daily lane anchors keep shared navigation and reject stale paints
ok 345 - daily lane anchors keep shared navigation and reject stale paints
  ---
  duration_ms: 3.018001
  ...
# Subtest: daily paint stays unavailable until Tasks and Today are ready
ok 346 - daily paint stays unavailable until Tasks and Today are ready
  ---
  duration_ms: 1.286366
  ...
# Subtest: work tones: dashboard lane models carry section tones
ok 347 - work tones: dashboard lane models carry section tones
  ---
  duration_ms: 0.177759
  ...
# Subtest: T1 scheduled full-mode row gets a Fri mark inside the span
ok 348 - T1 scheduled full-mode row gets a Fri mark inside the span
  ---
  duration_ms: 5.944887
  ...
# Subtest: T2 done row maps to a completion Oct 5 mark
ok 349 - T2 done row maps to a completion Oct 5 mark
  ---
  duration_ms: 0.761845
  ...
# Subtest: T3 short-mode created span is left untouched by JS
ok 350 - T3 short-mode created span is left untouched by JS
  ---
  duration_ms: 0.441844
  ...
# Subtest: T4 pending row decorates once data-task appears; exhausted rows stay native
ok 351 - T4 pending row decorates once data-task appears; exhausted rows stay native
  ---
  duration_ms: 1.497108
  ...
# Subtest: T5 a second pass adds nothing
ok 352 - T5 a second pass adds nothing
  ---
  duration_ms: 0.481659
  ...
# Subtest: T6 task-due and task-start spans are untouched
ok 353 - T6 task-due and task-start spans are untouched
  ---
  duration_ms: 0.339909
  ...
# Subtest: T7 an invalid date is untouched
ok 354 - T7 an invalid date is untouched
  ---
  duration_ms: 0.354417
  ...
# Subtest: T8 nothing is scheduled with marks off or for connected non-Tasks elements
ok 355 - T8 nothing is scheduled with marks off or for connected non-Tasks elements
  ---
  duration_ms: 0.375968
  ...
# Subtest: T9 a Tasks-host Fri mark relabels to tomorrow on rollover
ok 356 - T9 a Tasks-host Fri mark relabels to tomorrow on rollover
  ---
  duration_ms: 0.999879
  ...
# Subtest: renderDateMarksIn schedules one shared frame for every row
ok 357 - renderDateMarksIn schedules one shared frame for every row
  ---
  duration_ms: 1.528197
  ...
# Subtest: the Tasks pass never throws on hostile input
ok 358 - the Tasks pass never throws on hostile input
  ---
  duration_ms: 0.530914
  ...
# Subtest: T10 real-DOM NodeList children decorate via direct and queued passes
ok 359 - T10 real-DOM NodeList children decorate via direct and queued passes
  ---
  duration_ms: 0.677984
  ...
# Subtest: T11 toggling off before a queued frame runs writes nothing
ok 360 - T11 toggling off before a queued frame runs writes nothing
  ---
  duration_ms: 3.056975
  ...
# Subtest: T12 a pending-row retry followed by disabling writes nothing
ok 361 - T12 a pending-row retry followed by disabling writes nothing
  ---
  duration_ms: 0.384224
  ...
# Subtest: T13 unloading before a callback runs writes nothing
ok 362 - T13 unloading before a callback runs writes nothing
  ---
  duration_ms: 0.940756
  ...
# Subtest: styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
ok 363 - styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
  ---
  duration_ms: 0.688935
  ...
# Subtest: DATE_MARK_FIELDS lists the four dates with verbs
ok 364 - DATE_MARK_FIELDS lists the four dates with verbs
  ---
  duration_ms: 2.41527
  ...
# Subtest: DM1 created today: label, tooltip, fold, quiet field
ok 365 - DM1 created today: label, tooltip, fold, quiet field
  ---
  duration_ms: 1.99563
  ...
# Subtest: DM2 created yesterday without space after the colons
ok 366 - DM2 created yesterday without space after the colons
  ---
  duration_ms: 0.598403
  ...
# Subtest: DM3-DM6 scheduled tomorrow, weekday, and month/day labels
ok 367 - DM3-DM6 scheduled tomorrow, weekday, and month/day labels
  ---
  duration_ms: 0.319149
  ...
# Subtest: DM7 scheduled today reads with emphasis timing
ok 368 - DM7 scheduled today reads with emphasis timing
  ---
  duration_ms: 0.317586
  ...
# Subtest: DM8 past scheduled uses month/day, never a weekday
ok 369 - DM8 past scheduled uses month/day, never a weekday
  ---
  duration_ms: 0.213978
  ...
# Subtest: DM9 completion on a closed task keeps the timeline grammar
ok 370 - DM9 completion on a closed task keeps the timeline grammar
  ---
  duration_ms: 0.264044
  ...
# Subtest: DM10 cancelled across years appends the year
ok 371 - DM10 cancelled across years appends the year
  ---
  duration_ms: 0.218306
  ...
# Subtest: DM11 next-year date appends the year
ok 372 - DM11 next-year date appends the year
  ---
  duration_ms: 0.387239
  ...
# Subtest: DM12 the weekday rule wins across the year boundary
ok 373 - DM12 the weekday rule wins across the year boundary
  ---
  duration_ms: 0.408009
  ...
# Subtest: DM13 two marks in order with folds 1 and 2
ok 374 - DM13 two marks in order with folds 1 and 2
  ---
  duration_ms: 0.439138
  ...
# Subtest: DM14 created and scheduled ranges stay disjoint from the fresh mark
ok 375 - DM14 created and scheduled ranges stay disjoint from the fresh mark
  ---
  duration_ms: 0.307728
  ...
# Subtest: DM15-DM16 paren and padded brackets are canonical
ok 376 - DM15-DM16 paren and padded brackets are canonical
  ---
  duration_ms: 0.181326
  ...
# Subtest: DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
ok 377 - DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
  ---
  duration_ms: 0.311916
  ...
# Subtest: DM22 code still parses pure but decorates nothing (see Live Preview)
ok 378 - DM22 code still parses pure but decorates nothing (see Live Preview)
  ---
  duration_ms: 0.106814
  ...
# Subtest: DM23 rescheduled is untouched and never a duplicate
ok 379 - DM23 rescheduled is untouched and never a duplicate
  ---
  duration_ms: 0.14161
  ...
# Subtest: DN1-DN9 non-canonical fields get no mark
ok 380 - DN1-DN9 non-canonical fields get no mark
  ---
  duration_ms: 0.241
  ...
# Subtest: dateMarkContentStart finds content on list, quoted, and plain lines
ok 381 - dateMarkContentStart finds content on list, quoted, and plain lines
  ---
  duration_ms: 0.111313
  ...
# Subtest: dateMarkRelativePhrase covers the exact-day phrases
ok 382 - dateMarkRelativePhrase covers the exact-day phrases
  ---
  duration_ms: 0.095332
  ...
# Subtest: dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
ok 383 - dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
  ---
  duration_ms: 0.542375
  ...
# Subtest: no model output contains a double colon
ok 384 - no model output contains a double colon
  ---
  duration_ms: 2.45169
  ...
# Subtest: a new day always changes the widget key
ok 385 - a new day always changes the widget key
  ---
  duration_ms: 0.248314
  ...
# Subtest: element structure and the decorative/inheritColor/rendered options
ok 386 - element structure and the decorative/inheritColor/rendered options
  ---
  duration_ms: 0.620184
  ...
# Subtest: Live Preview emits several decorations in ascending order
ok 387 - Live Preview emits several decorations in ascending order
  ---
  duration_ms: 1.609433
  ...
# Subtest: Live Preview reveals per field, never the whole line
ok 388 - Live Preview reveals per field, never the whole line
  ---
  duration_ms: 0.458866
  ...
# Subtest: Live Preview refuses source mode, code, and disabled marks
ok 389 - Live Preview refuses source mode, code, and disabled marks
  ---
  duration_ms: 0.633659
  ...
# Subtest: widget mousedown anchors at the field start for folds 0, 1, and 2
ok 390 - widget mousedown anchors at the field start for folds 0, 1, and 2
  ---
  duration_ms: 1.266037
  ...
# Subtest: DM24 a cursor in the folded run unfolds the mark (vim cw)
ok 391 - DM24 a cursor in the folded run unfolds the mark (vim cw)
  ---
  duration_ms: 0.362391
  ...
# Subtest: DM25 a cursor in Tasks double space unfolds only that field
ok 392 - DM25 a cursor in Tasks double space unfolds only that field
  ---
  duration_ms: 0.259586
  ...
# Subtest: a selection ending inside the run unfolds; ending at its start keeps the fold
ok 393 - a selection ending inside the run unfolds; ending at its start keeps the fold
  ---
  duration_ms: 0.306435
  ...
# Subtest: no emitted decoration ever hides a cursor, and reveal still means field overlap
ok 394 - no emitted decoration ever hides a cursor, and reveal still means field overlap
  ---
  duration_ms: 13.419466
  ...
# Subtest: dateMarkSelectionFold: reveal, unfold, fold, and garbage input
ok 395 - dateMarkSelectionFold: reveal, unfold, fold, and garbage input
  ---
  duration_ms: 0.260738
  ...
# Subtest: mousedown on an unfolded (fold-0) widget anchors at the field start
ok 396 - mousedown on an unfolded (fold-0) widget anchors at the field start
  ---
  duration_ms: 0.330381
  ...
# Subtest: rendered views split several fields in one node
ok 397 - rendered views split several fields in one node
  ---
  duration_ms: 1.342793
  ...
# Subtest: rendered views skip exclusions and duplicates
ok 398 - rendered views skip exclusions and duplicates
  ---
  duration_ms: 0.503151
  ...
# Subtest: RO1 rendered marks relabel in place across midnight
ok 399 - RO1 rendered marks relabel in place across midnight
  ---
  duration_ms: 0.468685
  ...
# Subtest: rollover dispatches once per day change and never touches widgets
ok 400 - rollover dispatches once per day change and never touches widgets
  ---
  duration_ms: 0.52918
  ...
# Subtest: api.dateMarks v1 is additive, sync, and never throwing
ok 401 - api.dateMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.449448
  ...
# Subtest: session toggle and onload wiring
ok 402 - session toggle and onload wiring
  ---
  duration_ms: 3.25906
  ...
# Subtest: styles.css contract: masks, tones, repair flag, resting
ok 403 - styles.css contract: masks, tones, repair flag, resting
  ---
  duration_ms: 0.786281
  ...
# Subtest: DP parse vectors
ok 404 - DP parse vectors
  ---
  duration_ms: 2.207404
  ...
# Subtest: DC chip model vectors
ok 405 - DC chip model vectors
  ---
  duration_ms: 1.652785
  ...
# Subtest: decoration builds one widget, reveals on cursor, skips code and ranges
ok 406 - decoration builds one widget, reveals on cursor, skips code and ranges
  ---
  duration_ms: 6.802045
  ...
# Subtest: decoration skips paragraphs, grandchildren, and Work Log lines
ok 407 - decoration skips paragraphs, grandchildren, and Work Log lines
  ---
  duration_ms: 2.455777
  ...
# Subtest: decoration renders chips on DP30 and still skips DP20
ok 408 - decoration renders chips on DP30 and still skips DP20
  ---
  duration_ms: 0.78587
  ...
# Subtest: ownership check reads O(depth) lines, not the whole note
ok 409 - ownership check reads O(depth) lines, not the whole note
  ---
  duration_ms: 1.095802
  ...
# Subtest: widget identity covers the line and the interactive flag
ok 410 - widget identity covers the line and the interactive flag
  ---
  duration_ms: 1.178639
  ...
# Subtest: element hides actions without nav api v1
ok 411 - element hides actions without nav api v1
  ---
  duration_ms: 0.716859
  ...
# Subtest: nav api feature detection gates actions
ok 412 - nav api feature detection gates actions
  ---
  duration_ms: 0.38228
  ...
# Subtest: reading view decorates only the Depends-On row, hides chrome, stays idempotent
ok 413 - reading view decorates only the Depends-On row, hides chrome, stays idempotent
  ---
  duration_ms: 2.826977
  ...
# Subtest: reading view collapses more than three Done targets to one chip
ok 414 - reading view collapses more than three Done targets to one chip
  ---
  duration_ms: 1.231471
  ...
# Subtest: DC chip model vectors by id: DC2, DC5, DC6, DC9
ok 415 - DC chip model vectors by id: DC2, DC5, DC6, DC9
  ---
  duration_ms: 0.257512
  ...
# Subtest: chip actions send the 0-based line index through nav api v1
ok 416 - chip actions send the 0-based line index through nav api v1
  ---
  duration_ms: 1.063519
  ...
# Subtest: chip hover passes the chip element and its row to the preview
ok 417 - chip hover passes the chip element and its row to the preview
  ---
  duration_ms: 0.166417
  ...
# Subtest: chip lookup index lives on the freshness memo
ok 418 - chip lookup index lives on the freshness memo
  ---
  duration_ms: 0.498191
  ...
# Subtest: reading view hides actions when the line cannot be derived
ok 419 - reading view hides actions when the line cannot be derived
  ---
  duration_ms: 9.43497
  ...
# Subtest: reading view actions carry the derived 0-based line
ok 420 - reading view actions carry the derived 0-based line
  ---
  duration_ms: 3.556398
  ...
# Subtest: reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
ok 421 - reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
  ---
  duration_ms: 0.527728
  ...
# Subtest: reading view renders chips on DP30 (owner is a task under a Work Log entry)
ok 422 - reading view renders chips on DP30 (owner is a task under a Work Log entry)
  ---
  duration_ms: 0.689286
  ...
# Subtest: reading view DP30 row actions send the owned Depends-On line
ok 423 - reading view DP30 row actions send the owned Depends-On line
  ---
  duration_ms: 2.429007
  ...
# Subtest: reading view second-row remove sends the second line when two tasks share a prerequisite
ok 424 - reading view second-row remove sends the second line when two tasks share a prerequisite
  ---
  duration_ms: 1.731495
  ...
# Subtest: chip lookup index builds once per freshness memo
ok 425 - chip lookup index builds once per freshness memo
  ---
  duration_ms: 0.486548
  ...
# Subtest: decoration evaluates ownership without copying the note
ok 426 - decoration evaluates ownership without copying the note
  ---
  duration_ms: 0.536614
  ...
# Subtest: toggle flips the body class and onload wires chips
ok 427 - toggle flips the body class and onload wires chips
  ---
  duration_ms: 3.445477
  ...
# Subtest: capability: nav card v2 is capable
ok 428 - capability: nav card v2 is capable
  ---
  duration_ms: 2.106121
  ...
# Subtest: capability: nav card v1 is not capable
ok 429 - capability: nav card v1 is not capable
  ---
  duration_ms: 0.250959
  ...
# Subtest: capability: absent nav, missing api, and old versions are not capable
ok 430 - capability: absent nav, missing api, and old versions are not capable
  ---
  duration_ms: 0.163071
  ...
# Subtest: capability: a throwing app never throws
ok 431 - capability: a throwing app never throws
  ---
  duration_ms: 0.263002
  ...
# Subtest: leaf: active capable due choice replaces refresh with a leaf
ok 432 - leaf: active capable due choice replaces refresh with a leaf
  ---
  duration_ms: 3.690665
  ...
# Subtest: leaf: the same row without the card keeps refresh and counting words
ok 433 - leaf: the same row without the card keeps refresh and counting words
  ---
  duration_ms: 0.472602
  ...
# Subtest: leaf: early dates still leaf when capable
ok 434 - leaf: early dates still leaf when capable
  ---
  duration_ms: 0.503782
  ...
# Subtest: leaf: decay-off rows never leaf even when capable
ok 435 - leaf: decay-off rows never leaf even when capable
  ---
  duration_ms: 0.484095
  ...
# Subtest: leaf: below-threshold rows never leaf
ok 436 - leaf: below-threshold rows never leaf
  ---
  duration_ms: 0.74929
  ...
# Subtest: leaf: threshold zero asks on every due re-confirmation when capable
ok 437 - leaf: threshold zero asks on every due re-confirmation when capable
  ---
  duration_ms: 0.632136
  ...
# Subtest: leaf: overflow renders capped dots with +N and the exact count in text
ok 438 - leaf: overflow renders capped dots with +N and the exact count in text
  ---
  duration_ms: 0.367541
  ...
# Subtest: leaf: out-of-scope and closed tasks show dots quietly, never a leaf
ok 439 - leaf: out-of-scope and closed tasks show dots quietly, never a leaf
  ---
  duration_ms: 0.894637
  ...
# Subtest: leaf: unresolved marks show dots quietly with counting-only wording
ok 440 - leaf: unresolved marks show dots quietly with counting-only wording
  ---
  duration_ms: 0.240219
  ...
# Subtest: element: leaf marks carry data-decide true and a leaf path
ok 441 - element: leaf marks carry data-decide true and a leaf path
  ---
  duration_ms: 0.819374
  ...
# Subtest: element: non-decision marks carry data-decide false
ok 442 - element: non-decision marks carry data-decide false
  ---
  duration_ms: 0.316555
  ...
# Subtest: footer groups omit every zero tier and keep walk order
ok 443 - footer groups omit every zero tier and keep walk order
  ---
  duration_ms: 1.572161
  ...
# Subtest: PRE and POST groups bracket the nine-tier queue and expose completion hints
ok 444 - PRE and POST groups bracket the nine-tier queue and expose completion hints
  ---
  duration_ms: 0.823993
  ...
# Subtest: a NEW-state project appears only in its walk tier
ok 445 - a NEW-state project appears only in its walk tier
  ---
  duration_ms: 0.207707
  ...
# Subtest: empty queue hides the footer even with upkeep or a met budget
ok 446 - empty queue hides the footer even with upkeep or a met budget
  ---
  duration_ms: 0.144986
  ...
# Subtest: unavailable or missing data never render false counts
ok 447 - unavailable or missing data never render false counts
  ---
  duration_ms: 0.250629
  ...
# Subtest: generic summary names due, commitments, and nonempty groups
ok 448 - generic summary names due, commitments, and nonempty groups
  ---
  duration_ms: 0.390064
  ...
# Subtest: current-task context uses shared ranks and compact wording
ok 449 - current-task context uses shared ranks and compact wording
  ---
  duration_ms: 0.667284
  ...
# Subtest: only ROTTEN remaining names commitments done or a met budget
ok 450 - only ROTTEN remaining names commitments done or a met budget
  ---
  duration_ms: 0.284554
  ...
# Subtest: NEW and commitments take precedence over a met budget
ok 451 - NEW and commitments take precedence over a met budget
  ---
  duration_ms: 0.389374
  ...
# Subtest: reviewEntryView compact and detail cover the original freshness tiers
ok 452 - reviewEntryView compact and detail cover the original freshness tiers
  ---
  duration_ms: 1.083448
  ...
# Subtest: cursor matching requires a unique verified identity
ok 453 - cursor matching requires a unique verified identity
  ---
  duration_ms: 0.50843
  ...
# Subtest: footer paint hides the host and keeps a stable button
ok 454 - footer paint hides the host and keeps a stable button
  ---
  duration_ms: 1.521194
  ...
# Subtest: status bar 0-1-0 transitions hide without a reload
ok 455 - status bar 0-1-0 transitions hide without a reload
  ---
  duration_ms: 11.418768
  ...
# Subtest: cursor-only updates reuse a warm memo
ok 456 - cursor-only updates reuse a warm memo
  ---
  duration_ms: 4.865777
  ...
# Subtest: unload disconnects the observer and click handler
ok 457 - unload disconnects the observer and click handler
  ---
  duration_ms: 2.034723
  ...
# Subtest: queue-built ranks agree with the footer current entry
ok 458 - queue-built ranks agree with the footer current entry
  ---
  duration_ms: 1.132542
  ...
# Subtest: footer short labels map every tier
ok 459 - footer short labels map every tier
  ---
  duration_ms: 0.163412
  ...
# Subtest: current-row footer context uses short labels while entry views keep full labels
ok 460 - current-row footer context uses short labels while entry views keep full labels
  ---
  duration_ms: 0.339478
  ...
# Subtest: legend line lists only current abbreviated tiers
ok 461 - legend line lists only current abbreviated tiers
  ---
  duration_ms: 0.356731
  ...
# Subtest: K1 absent: no keeps means 0 with no lints
ok 462 - K1 absent: no keeps means 0 with no lints
  ---
  duration_ms: 3.797599
  ...
# Subtest: K8 misplaced: keeps inside the Tasks suffix reads with a lint
ok 463 - K8 misplaced: keeps inside the Tasks suffix reads with a lint
  ---
  duration_ms: 0.663397
  ...
# Subtest: K9 duplicates and invalid values: first valid wins, else 0
ok 464 - K9 duplicates and invalid values: first valid wins, else 0
  ---
  duration_ms: 0.885371
  ...
# Subtest: K10 ceiling and NEW: 999 reads, never-confirmed reads 0
ok 465 - K10 ceiling and NEW: 999 reads, never-confirmed reads 0
  ---
  duration_ms: 0.293721
  ...
# Subtest: K13 exact keys: near-miss keys are not keeps; parens read
ok 466 - K13 exact keys: near-miss keys are not keeps; parens read
  ---
  duration_ms: 0.311575
  ...
# Subtest: keeps value parser accepts only decimal 1-999
ok 467 - keeps value parser accepts only decimal 1-999
  ---
  duration_ms: 0.264996
  ...
# Subtest: K2 first valid canonical: uncounted keep preserves and repairs
ok 468 - K2 first valid canonical: uncounted keep preserves and repairs
  ---
  duration_ms: 1.132151
  ...
# Subtest: K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
ok 469 - K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
  ---
  duration_ms: 0.730885
  ...
# Subtest: K4 same-day preserve noop: canonical kept line is byte-identical
ok 470 - K4 same-day preserve noop: canonical kept line is byte-identical
  ---
  duration_ms: 0.613591
  ...
# Subtest: K5 generic stamp clears, even same-day
ok 471 - K5 generic stamp clears, even same-day
  ---
  duration_ms: 0.685889
  ...
# Subtest: K6 set-refresh clears keeps
ok 472 - K6 set-refresh clears keeps
  ---
  duration_ms: 0.372982
  ...
# Subtest: K7 stale stamp clears keeps
ok 473 - K7 stale stamp clears keeps
  ---
  duration_ms: 0.259074
  ...
# Subtest: K8b misplaced keeps repaired to canonical order by a keep
ok 474 - K8b misplaced keeps repaired to canonical order by a keep
  ---
  duration_ms: 0.292358
  ...
# Subtest: K11 refusals preserve: closed and recurring lines never write
ok 475 - K11 refusals preserve: closed and recurring lines never write
  ---
  duration_ms: 3.433894
  ...
# Subtest: counted keep increments a stale streak once in the same write
ok 476 - counted keep increments a stale streak once in the same write
  ---
  duration_ms: 0.366059
  ...
# Subtest: first counted keep on a streakless due task writes keeps 1
ok 477 - first counted keep on a streakless due task writes keeps 1
  ---
  duration_ms: 0.258623
  ...
# Subtest: counted keep saturates at 999 and never wraps
ok 478 - counted keep saturates at 999 and never wraps
  ---
  duration_ms: 0.39262
  ...
# Subtest: counted keep needs a valid prior fresh before today
ok 479 - counted keep needs a valid prior fresh before today
  ---
  duration_ms: 0.598573
  ...
# Subtest: counted keep repairs malformed and duplicate placement
ok 480 - counted keep repairs malformed and duplicate placement
  ---
  duration_ms: 0.508431
  ...
# Subtest: uncounted keep preserves the valid value while canonicalizing
ok 481 - uncounted keep preserves the valid value while canonicalizing
  ---
  duration_ms: 0.386859
  ...
# Subtest: UB13 keep on an unblock TICKLER preserves the streak and skips the card
ok 482 - UB13 keep on an unblock TICKLER preserves the streak and skips the card
  ---
  duration_ms: 1.370045
  ...
# Subtest: a scheduled tickler still counts when schedule wins an unblock tie
ok 483 - a scheduled tickler still counts when schedule wins an unblock tie
  ---
  duration_ms: 0.485837
  ...
# Subtest: decay normalization: absent, null, true, and {} enable with 3
ok 484 - decay normalization: absent, null, true, and {} enable with 3
  ---
  duration_ms: 0.997524
  ...
# Subtest: decay false counts and displays but never asks
ok 485 - decay false counts and displays but never asks
  ---
  duration_ms: 0.181567
  ...
# Subtest: decay keeps 0 and fixed entry normalize
ok 486 - decay keeps 0 and fixed entry normalize
  ---
  duration_ms: 0.215391
  ...
# Subtest: invalid decay shapes fail the freshness config contract
ok 487 - invalid decay shapes fail the freshness config contract
  ---
  duration_ms: 0.3611
  ...
# Subtest: B: at-limit Ready due rows decide on every local day
ok 488 - B: at-limit Ready due rows decide on every local day
  ---
  duration_ms: 0.78054
  ...
# Subtest: D1 early date: an at-limit Ready due row decides
ok 489 - D1 early date: an at-limit Ready due row decides
  ---
  duration_ms: 0.236161
  ...
# Subtest: D2 at limit decides; D3 below limit stamps without a card
ok 490 - D2 at limit decides; D3 below limit stamps without a card
  ---
  duration_ms: 0.196395
  ...
# Subtest: D4 tickler counts as due; D5 NEW never decides
ok 491 - D4 tickler counts as due; D5 NEW never decides
  ---
  duration_ms: 0.284403
  ...
# Subtest: D6 zero limit asks on every due Ready re-confirmation
ok 492 - D6 zero limit asks on every due Ready re-confirmation
  ---
  duration_ms: 0.145448
  ...
# Subtest: D7 off never asks; D8 lane rows never decide
ok 493 - D7 off never asks; D8 lane rows never decide
  ---
  duration_ms: 0.144385
  ...
# Subtest: evaluator, queue, and counts carry keeps and decide
ok 494 - evaluator, queue, and counts carry keeps and decide
  ---
  duration_ms: 1.797071
  ...
# Subtest: no keeps: the existing mark is unchanged
ok 495 - no keeps: the existing mark is unchanged
  ---
  duration_ms: 1.551672
  ...
# Subtest: aging with two keeps: faint pips plus a counting-only line
ok 496 - aging with two keeps: faint pips plus a counting-only line
  ---
  duration_ms: 0.464346
  ...
# Subtest: confirmed today with two keeps: check glyph, faint dots
ok 497 - confirmed today with two keeps: check glyph, faint dots
  ---
  duration_ms: 0.353505
  ...
# Subtest: due below threshold: orange capsule keeps its glyph, adds dots
ok 498 - due below threshold: orange capsule keeps its glyph, adds dots
  ---
  duration_ms: 0.349707
  ...
# Subtest: resting marks show historical dots quietly and never decide
ok 499 - resting marks show historical dots quietly and never decide
  ---
  duration_ms: 0.514392
  ...
# Subtest: active decision due: data stays truthful, leaf stays gated
ok 500 - active decision due: data stays truthful, leaf stays gated
  ---
  duration_ms: 0.376399
  ...
# Subtest: dot caps follow the threshold with +N overflow
ok 501 - dot caps follow the threshold with +N overflow
  ---
  duration_ms: 0.961345
  ...
# Subtest: keeps tooltip wording: singulars, zero threshold, off state
ok 502 - keeps tooltip wording: singulars, zero threshold, off state
  ---
  duration_ms: 0.25671
  ...
# Subtest: noncanonical keeps never fold but keep their repair pill
ok 503 - noncanonical keeps never fold but keep their repair pill
  ---
  duration_ms: 0.595557
  ...
# Subtest: quoted lines fold; rendered fragments fold without task checks
ok 504 - quoted lines fold; rendered fragments fold without task checks
  ---
  duration_ms: 0.362562
  ...
# Subtest: unresolved marks show the line's own pips quietly and never decide
ok 505 - unresolved marks show the line's own pips quietly and never decide
  ---
  duration_ms: 0.308048
  ...
# Subtest: consensus sees count and decision eligibility: ambiguity stays neutral
ok 506 - consensus sees count and decision eligibility: ambiguity stays neutral
  ---
  duration_ms: 0.72824
  ...
# Subtest: pips render as one aria-hidden span with the count in the label
ok 507 - pips render as one aria-hidden span with the count in the label
  ---
  duration_ms: 1.491728
  ...
# Subtest: Live Preview decorates the folded range including space and refresh
ok 508 - Live Preview decorates the folded range including space and refresh
  ---
  duration_ms: 6.597875
  ...
# Subtest: Live Preview reveals the raw field when the cursor overlaps either edge
ok 509 - Live Preview reveals the raw field when the cursor overlaps either edge
  ---
  duration_ms: 1.642194
  ...
# Subtest: Live Preview skips codeblock and inline code spans
ok 510 - Live Preview skips codeblock and inline code spans
  ---
  duration_ms: 0.759881
  ...
# Subtest: source mode and marks-off yield no decorations
ok 511 - source mode and marks-off yield no decorations
  ---
  duration_ms: 0.200062
  ...
# Subtest: update rebuilds on the refresh effect and widget eq is stable
ok 512 - update rebuilds on the refresh effect and widget eq is stable
  ---
  duration_ms: 1.335419
  ...
# Subtest: widget click reveals the field at the folded offset
ok 513 - widget click reveals the field at the folded offset
  ---
  duration_ms: 1.012853
  ...
# Subtest: line resolver prefers exact, then consensus, then unresolved
ok 514 - line resolver prefers exact, then consensus, then unresolved
  ---
  duration_ms: 1.668285
  ...
# Subtest: decoration builds reuse the snapshot without touching the loader
ok 515 - decoration builds reuse the snapshot without touching the loader
  ---
  duration_ms: 0.530573
  ...
# Subtest: rendered views split text nodes and skip excluded ancestors
ok 516 - rendered views split text nodes and skip excluded ancestors
  ---
  duration_ms: 1.751324
  ...
# Subtest: rendered views stay idempotent
ok 517 - rendered views stay idempotent
  ---
  duration_ms: 0.568966
  ...
# Subtest: text resolver reaches consensus and degrades to neutral
ok 518 - text resolver reaches consensus and degrades to neutral
  ---
  duration_ms: 0.77543
  ...
# Subtest: session toggle flips the body class and notifies
ok 519 - session toggle flips the body class and notifies
  ---
  duration_ms: 0.789166
  ...
# Subtest: onload registers the toggle, extension, and post-processor
ok 520 - onload registers the toggle, extension, and post-processor
  ---
  duration_ms: 3.497196
  ...
# Subtest: M1 today: check glyph, today label, full ring
ok 521 - M1 today: check glyph, today label, full ring
  ---
  duration_ms: 4.932906
  ...
# Subtest: M2 aging: ring glyph, 3d label, draining lease
ok 522 - M2 aging: ring glyph, 3d label, draining lease
  ---
  duration_ms: 0.69156
  ...
# Subtest: M3 boundary: ROTTEN due capsule with Alt+F hint
ok 523 - M3 boundary: ROTTEN due capsule with Alt+F hint
  ---
  duration_ms: 0.484013
  ...
# Subtest: checklist marks replace stamp hints with their completion tier
ok 524 - checklist marks replace stamp hints with their completion tier
  ---
  duration_ms: 0.922711
  ...
# Subtest: M4 yesterday uses the yesterday relative
ok 525 - M4 yesterday uses the yesterday relative
  ---
  duration_ms: 0.376028
  ...
# Subtest: M5 folded refresh shows the /14d suffix
ok 526 - M5 folded refresh shows the /14d suffix
  ---
  duration_ms: 0.591278
  ...
# Subtest: M6 refresh today: today tone hides the interval suffix
ok 527 - M6 refresh today: today tone hides the interval suffix
  ---
  duration_ms: 0.412928
  ...
# Subtest: M7 note interval stays tooltip-only
ok 528 - M7 note interval stays tooltip-only
  ---
  duration_ms: 0.641304
  ...
# Subtest: M8 resurfaced: due tone on the scheduled return
ok 529 - M8 resurfaced: due tone on the scheduled return
  ---
  duration_ms: 0.663086
  ...
# Subtest: M9 due NEXT lane with keep/release/today keys
ok 530 - M9 due NEXT lane with keep/release/today keys
  ---
  duration_ms: 0.703403
  ...
# Subtest: M10 NEXT lane stamped today
ok 531 - M10 NEXT lane stamped today
  ---
  duration_ms: 0.417217
  ...
# Subtest: M19 disabled Next lane rests
ok 532 - M19 disabled Next lane rests
  ---
  duration_ms: 0.373483
  ...
# Subtest: M20 PENDING lane folds refresh without the suffix
ok 533 - M20 PENDING lane folds refresh without the suffix
  ---
  duration_ms: 0.328176
  ...
# Subtest: M11 closed: resting beats age 0
ok 534 - M11 closed: resting beats age 0
  ---
  duration_ms: 0.306545
  ...
# Subtest: M12 unresolved running and M13 unresolved lease over
ok 535 - M12 unresolved running and M13 unresolved lease over
  ---
  duration_ms: 2.473512
  ...
# Subtest: M14 linked today rests with its reason
ok 536 - M14 linked today rests with its reason
  ---
  duration_ms: 0.30403
  ...
# Subtest: M15 other year shows the year and the 282d age
ok 537 - M15 other year shows the year and the 282d age
  ---
  duration_ms: 0.20926
  ...
# Subtest: M16 quoted line keeps foldSpace
ok 538 - M16 quoted line keeps foldSpace
  ---
  duration_ms: 0.215903
  ...
# Subtest: M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
ok 539 - M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
  ---
  duration_ms: 0.608481
  ...
# Subtest: N1-N6 non-canonical lines get no mark
ok 540 - N1-N6 non-canonical lines get no mark
  ---
  duration_ms: 0.232023
  ...
# Subtest: C1-C3 consensus is exact or unresolved
ok 541 - C1-C3 consensus is exact or unresolved
  ---
  duration_ms: 0.758338
  ...
# Subtest: freshnessMarkResolution treats evaluator new as unresolved
ok 542 - freshnessMarkResolution treats evaluator new as unresolved
  ---
  duration_ms: 0.173041
  ...
# Subtest: freshnessMarkSourceInText covers rendered fragments
ok 543 - freshnessMarkSourceInText covers rendered fragments
  ---
  duration_ms: 0.274093
  ...
# Subtest: tone order: closed, then due, then age 0, then out of scope
ok 544 - tone order: closed, then due, then age 0, then out of scope
  ---
  duration_ms: 0.575769
  ...
# Subtest: no tooltip ever contains a double colon
ok 545 - no tooltip ever contains a double colon
  ---
  duration_ms: 1.161578
  ...
# Subtest: freshnessShortDate pins English names and the year rule
ok 546 - freshnessShortDate pins English names and the year rule
  ---
  duration_ms: 0.176597
  ...
# Subtest: DOM builder structure, attributes, and ring geometry
ok 547 - DOM builder structure, attributes, and ring geometry
  ---
  duration_ms: 1.680638
  ...
# Subtest: every mark helper is synchronous and never throws on bad input
ok 548 - every mark helper is synchronous and never throws on bad input
  ---
  duration_ms: 0.175154
  ...
# Subtest: freshness namespace v12 exposes unblock TICKLER metadata and writers
ok 549 - freshness namespace v12 exposes unblock TICKLER metadata and writers
  ---
  duration_ms: 18.121632
  ...
# Subtest: freshness state and count API expose an unblock return source
ok 550 - freshness state and count API expose an unblock return source
  ---
  duration_ms: 2.205329
  ...
# Subtest: checklist rows report tier and rank while keeping the READY bucket null
ok 551 - checklist rows report tier and rank while keeping the READY bucket null
  ---
  duration_ms: 1.520573
  ...
# Subtest: tier, isDue, and rank cover lane rows
ok 552 - tier, isDue, and rank cover lane rows
  ---
  duration_ms: 2.32052
  ...
# Subtest: memo invalidates on a new tasks array, rollover, and frontmatter
ok 553 - memo invalidates on a new tasks array, rollover, and frontmatter
  ---
  duration_ms: 9.506407
  ...
# Subtest: the reload event fires only when the due key set changes
ok 554 - the reload event fires only when the due key set changes
  ---
  duration_ms: 2.280804
  ...
# Subtest: status bar text covers every state, and a missing host stays quiet
ok 555 - status bar text covers every state, and a missing host stays quiet
  ---
  duration_ms: 1.242472
  ...
# Subtest: status bar clicks through, falling back to rotten
ok 556 - status bar clicks through, falling back to rotten
  ---
  duration_ms: 7.44905
  ...
# Subtest: every freshness api member is synchronous and never throws
ok 557 - every freshness api member is synchronous and never throws
  ---
  duration_ms: 1.651572
  ...
# Subtest: placement vectors P1-P11, P14-P16, P18 stamp canonically
ok 558 - placement vectors P1-P11, P14-P16, P18 stamp canonically
  ---
  duration_ms: 5.320366
  ...
# Subtest: P12 set and clear refresh stamps alongside
ok 559 - P12 set and clear refresh stamps alongside
  ---
  duration_ms: 0.474455
  ...
# Subtest: P13 recurring and P17 done tasks are refused unchanged
ok 560 - P13 recurring and P17 done tasks are refused unchanged
  ---
  duration_ms: 0.245348
  ...
# Subtest: U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
ok 561 - U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
  ---
  duration_ms: 1.038393
  ...
# Subtest: reader reports misplaced and duplicate fields
ok 562 - reader reports misplaced and duplicate fields
  ---
  duration_ms: 0.470297
  ...
# Subtest: Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
ok 563 - Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
  ---
  duration_ms: 6.654452
  ...
# Subtest: Q2 tier order beats path order
ok 564 - Q2 tier order beats path order
  ---
  duration_ms: 1.201222
  ...
# Subtest: L1 lane due and stamped today
ok 565 - L1 lane due and stamped today
  ---
  duration_ms: 0.415754
  ...
# Subtest: L2 lane overrides refresh
ok 566 - L2 lane overrides refresh
  ---
  duration_ms: 0.308529
  ...
# Subtest: L3 lane exclusions have no tier
ok 567 - L3 lane exclusions have no tier
  ---
  duration_ms: 0.453767
  ...
# Subtest: L4 lane off switch and null default
ok 568 - L4 lane off switch and null default
  ---
  duration_ms: 0.259525
  ...
# Subtest: L5 lane order never stamped first
ok 569 - L5 lane order never stamped first
  ---
  duration_ms: 0.406316
  ...
# Subtest: R1 TICKLER beats older ROTTEN
ok 570 - R1 TICKLER beats older ROTTEN
  ---
  duration_ms: 0.332024
  ...
# Subtest: R2 tickler orders by due date then path and line
ok 571 - R2 tickler orders by due date then path and line
  ---
  duration_ms: 0.600607
  ...
# Subtest: missing created sorts after dated peers
ok 572 - missing created sorts after dated peers
  ---
  duration_ms: 0.779969
  ...
# Subtest: B1 upkeep counts outside the lanes
ok 573 - B1 upkeep counts outside the lanes
  ---
  duration_ms: 5.468007
  ...
# Subtest: review model meter uses upkeep and exposes refreshed
ok 574 - review model meter uses upkeep and exposes refreshed
  ---
  duration_ms: 0.348295
  ...
# Subtest: RC1 arrived: past scheduled walks RECURRING with lane and null state
ok 575 - RC1 arrived: past scheduled walks RECURRING with lane and null state
  ---
  duration_ms: 4.583068
  ...
# Subtest: RC2 arrives today: due today with zero days overdue
ok 576 - RC2 arrives today: due today with zero days overdue
  ---
  duration_ms: 0.519602
  ...
# Subtest: RC3 not yet: future scheduled walks nowhere
ok 577 - RC3 not yet: future scheduled walks nowhere
  ---
  duration_ms: 0.287579
  ...
# Subtest: RC4 due only, past: the due date is the occurrence
ok 578 - RC4 due only, past: the due date is the occurrence
  ---
  duration_ms: 0.285154
  ...
# Subtest: RC5 due only, future: walks nowhere
ok 579 - RC5 due only, future: walks nowhere
  ---
  duration_ms: 0.313018
  ...
# Subtest: RC6 earliest date wins across start and due
ok 580 - RC6 earliest date wins across start and due
  ---
  duration_ms: 0.328026
  ...
# Subtest: RC7 undated: no occurrence, no tier
ok 581 - RC7 undated: no occurrence, no tier
  ---
  duration_ms: 0.384193
  ...
# Subtest: RC8 lanes: recurring lane rows keep their lane with null state
ok 582 - RC8 lanes: recurring lane rows keep their lane with null state
  ---
  duration_ms: 0.545732
  ...
# Subtest: RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
ok 583 - RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
  ---
  duration_ms: 2.198627
  ...
# Subtest: RC10 checklist wins: a recurring chore stays in its checklist tier
ok 584 - RC10 checklist wins: a recurring chore stays in its checklist tier
  ---
  duration_ms: 0.589716
  ...
# Subtest: RC11 a stray stamp is ignored: recurring with null state
ok 585 - RC11 a stray stamp is ignored: recurring with null state
  ---
  duration_ms: 0.60222
  ...
# Subtest: RC12 order and counts: due_on, then path, then line; recurring adds no due
ok 586 - RC12 order and counts: due_on, then path, then line; recurring adds no due
  ---
  duration_ms: 1.560529
  ...
# Subtest: recurring rows adapt due and start from Tasks fields and inline fallbacks
ok 587 - recurring rows adapt due and start from Tasks fields and inline fallbacks
  ---
  duration_ms: 1.661151
  ...
# Subtest: status view counts RECURRING as a due commitment tier
ok 588 - status view counts RECURRING as a due commitment tier
  ---
  duration_ms: 0.47148
  ...
# Subtest: footer groups, entry view, and legend cover RECURRING
ok 589 - footer groups, entry view, and legend cover RECURRING
  ---
  duration_ms: 1.201393
  ...
# Subtest: a stale-stamped recurring row marks due with the resolve hint
ok 590 - a stale-stamped recurring row marks due with the resolve hint
  ---
  duration_ms: 1.401465
  ...
# Subtest: freshness namespace v12 keeps recurring and removes reference capabilities
ok 591 - freshness namespace v12 keeps recurring and removes reference capabilities
  ---
  duration_ms: 7.377612
  ...
# Subtest: hidden recurring ^ref keeps ordinary visibility (Rust parity)
ok 592 - hidden recurring ^ref keeps ordinary visibility (Rust parity)
  ---
  duration_ms: 1.252471
  ...
# Subtest: bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
ok 593 - bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
  ---
  duration_ms: 6.279365
  ...
# Subtest: day numbers stay calendar-local across a DST boundary
ok 594 - day numbers stay calendar-local across a DST boundary
  ---
  duration_ms: 0.518239
  ...
# Subtest: reviewModel shares counts, meter, tooltip, and severity
ok 595 - reviewModel shares counts, meter, tooltip, and severity
  ---
  duration_ms: 0.544029
  ...
# Subtest: memo serves warm map hits and misses use the per-row evaluator
ok 596 - memo serves warm map hits and misses use the per-row evaluator
  ---
  duration_ms: 7.429613
  ...
# Subtest: config snapshot caches the parse and invalidates explicitly
ok 597 - config snapshot caches the parse and invalidates explicitly
  ---
  duration_ms: 1.605595
  ...
# Subtest: review chips share the model with severity classes
ok 598 - review chips share the model with severity classes
  ---
  duration_ms: 1.60827
  ...
# Subtest: warm lookups reuse one snapshot without re-reading config
ok 599 - warm lookups reuse one snapshot without re-reading config
  ---
  duration_ms: 2.559145
  ...
# Subtest: same-array cache updates and Today changes rebuild the memo
ok 600 - same-array cache updates and Today changes rebuild the memo
  ---
  duration_ms: 7.860394
  ...
# Subtest: duplicate block IDs keep each row's own classification
ok 601 - duplicate block IDs keep each row's own classification
  ---
  duration_ms: 2.887592
  ...
# Subtest: line identity separates same-path rows without block IDs
ok 602 - line identity separates same-path rows without block IDs
  ---
  duration_ms: 1.317995
  ...
# Subtest: interval lookup serves the cached interval with one memo acquisition
ok 603 - interval lookup serves the cached interval with one memo acquisition
  ---
  duration_ms: 1.332624
  ...
# Subtest: S1 new through S4 overdue
ok 604 - S1 new through S4 overdue
  ---
  duration_ms: 5.210928
  ...
# Subtest: S5 task beats note, S6 note beats config, S7 config
ok 605 - S5 task beats note, S6 note beats config, S7 config
  ---
  duration_ms: 0.92735
  ...
# Subtest: S8 invalid overrides fall through with lints
ok 606 - S8 invalid overrides fall through with lints
  ---
  duration_ms: 0.431554
  ...
# Subtest: S9 malformed and S10 future stamps read as new
ok 607 - S9 malformed and S10 future stamps read as new
  ---
  duration_ms: 0.232223
  ...
# Subtest: S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
ok 608 - S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
  ---
  duration_ms: 0.339107
  ...
# Subtest: S13 out-of-scope rows read null
ok 609 - S13 out-of-scope rows read null
  ---
  duration_ms: 0.322887
  ...
# Subtest: S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
ok 610 - S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
  ---
  duration_ms: 1.288279
  ...
# Subtest: S15 counts (updated): upkeep outside the lanes drives the budget
ok 611 - S15 counts (updated): upkeep outside the lanes drives the budget
  ---
  duration_ms: 1.179402
  ...
# Subtest: config coercion keeps defaults, flags invalid, ignores unknown keys
ok 612 - config coercion keeps defaults, flags invalid, ignores unknown keys
  ---
  duration_ms: 1.798143
  ...
# Subtest: loadFreshnessConfig reads the block with plan-style injectables
ok 613 - loadFreshnessConfig reads the block with plan-style injectables
  ---
  duration_ms: 0.975963
  ...
# Subtest: interval precedence is task, note, config, default
ok 614 - interval precedence is task, note, config, default
  ---
  duration_ms: 0.237483
  ...
# Subtest: intervalForLine covers every source with its Ready fallback
ok 615 - intervalForLine covers every source with its Ready fallback
  ---
  duration_ms: 0.782433
  ...
# Subtest: project tracking stays special while reference tasks use ordinary Ready freshness
ok 616 - project tracking stays special while reference tasks use ordinary Ready freshness
  ---
  duration_ms: 6.095235
  ...
# Subtest: reference tasks match ordinary interval precedence and lane behavior
ok 617 - reference tasks match ordinary interval precedence and lane behavior
  ---
  duration_ms: 2.627154
  ...
# Subtest: obsolete reference interval keys are ignored and project config still validates
ok 618 - obsolete reference interval keys are ignored and project config still validates
  ---
  duration_ms: 0.804065
  ...
# Subtest: references use ordinary keep decisions and the nine-tier queue shape
ok 619 - references use ordinary keep decisions and the nine-tier queue shape
  ---
  duration_ms: 1.53448
  ...
# Subtest: CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
ok 620 - CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
  ---
  duration_ms: 3.10635
  ...
# Subtest: CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
ok 621 - CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
  ---
  duration_ms: 4.116738
  ...
# Subtest: freshness namespace v12 retains the tracker capability contract
ok 622 - freshness namespace v12 retains the tracker capability contract
  ---
  duration_ms: 4.25882
  ...
# Subtest: UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
ok 623 - UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
  ---
  duration_ms: 5.66828
  ...
# Subtest: UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
ok 624 - UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
  ---
  duration_ms: 0.657625
  ...
# Subtest: UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
ok 625 - UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
  ---
  duration_ms: 0.428377
  ...
# Subtest: UB11 scheduled wins a tie with the unblock date
ok 626 - UB11 scheduled wins a tie with the unblock date
  ---
  duration_ms: 0.376699
  ...
# Subtest: unblocked reader takes the latest valid duplicate and reports malformed values
ok 627 - unblocked reader takes the latest valid duplicate and reports malformed values
  ---
  duration_ms: 0.360337
  ...
# Subtest: UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
ok 628 - UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
  ---
  duration_ms: 0.563446
  ...
# Subtest: UB14 TICKLERs with the same due date sort only by path and line
ok 629 - UB14 TICKLERs with the same due date sort only by path and line
  ---
  duration_ms: 2.093507
  ...
# Subtest: UB15 a scheduled ^prj resurfaces in PROJECTS
ok 630 - UB15 a scheduled ^prj resurfaces in PROJECTS
  ---
  duration_ms: 0.273552
  ...
# Subtest: an active-note Pomodoro target still jumps and centers immediately
ok 631 - an active-note Pomodoro target still jumps and centers immediately
  ---
  duration_ms: 11.00683
  ...
# Subtest: the first fallback press only opens daily and the second press jumps
ok 632 - the first fallback press only opens daily and the second press jumps
  ---
  duration_ms: 2.070533
  ...
# Subtest: a daily note with no target defers its notice until the second press
ok 633 - a daily note with no target defers its notice until the second press
  ---
  duration_ms: 0.922281
  ...
# Subtest: an already-open daily leaf retains its live cursor and viewport
ok 634 - an already-open daily leaf retains its live cursor and viewport
  ---
  duration_ms: 1.233254
  ...
# Subtest: a second press after reused-leaf fallback performs the Pomodoro jump
ok 635 - a second press after reused-leaf fallback performs the Pomodoro jump
  ---
  duration_ms: 1.237042
  ...
# Subtest: the standalone daily-note command activates a reused daily leaf
ok 636 - the standalone daily-note command activates a reused daily leaf
  ---
  duration_ms: 1.55598
  ...
# Subtest: a closed then reopened daily note restores its in-session location
ok 637 - a closed then reopened daily note restores its in-session location
  ---
  duration_ms: 2.914443
  ...
# Subtest: different-path and invalid locations do not leak into a daily note
ok 638 - different-path and invalid locations do not leak into a daily note
  ---
  duration_ms: 0.803804
  ...
# Subtest: out-of-range remembered coordinates are clamped safely
ok 639 - out-of-range remembered coordinates are clamped safely
  ---
  duration_ms: 1.525302
  ...
# Subtest: a rapid second press cancels an older fallback restore
ok 640 - a rapid second press cancels an older fallback restore
  ---
  duration_ms: 1.253172
  ...
# Subtest: navigation and unload clean up daily scroll listeners and deferred work
ok 641 - navigation and unload clean up daily scroll listeners and deferred work
  ---
  duration_ms: 0.711027
  ...
# Subtest: crowded chip: over count is red with tooltip, aria, and names
ok 642 - crowded chip: over count is red with tooltip, aria, and names
  ---
  duration_ms: 1.662724
  ...
# Subtest: crowded chip: calm zero and unavailable dash
ok 643 - crowded chip: calm zero and unavailable dash
  ---
  duration_ms: 4.655067
  ...
# Subtest: crowded chip: names at most five notes
ok 644 - crowded chip: names at most five notes
  ---
  duration_ms: 0.337615
  ...
# Subtest: crowded chip: classes, text, aria, and arrow
ok 645 - crowded chip: classes, text, aria, and arrow
  ---
  duration_ms: 2.018683
  ...
# Subtest: crowded chip: refresh in place keeps the anchor, unload drops it
ok 646 - crowded chip: refresh in place keeps the anchor, unload drops it
  ---
  duration_ms: 0.783916
  ...
# Subtest: anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
ok 647 - anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
  ---
  duration_ms: 1.073559
  ...
# Subtest: ready-notes summary: crowded, calm, and unavailable
ok 648 - ready-notes summary: crowded, calm, and unavailable
  ---
  duration_ms: 0.296747
  ...
# Subtest: ready-notes bar: cap tick and red overflow within 30 cells
ok 649 - ready-notes bar: cap tick and red overflow within 30 cells
  ---
  duration_ms: 0.27726
  ...
# Subtest: ready-notes block: model and render with grid, pills, and footer
ok 650 - ready-notes block: model and render with grid, pills, and footer
  ---
  duration_ms: 2.323064
  ...
# Subtest: ready-notes block: unavailable renders a dash line
ok 651 - ready-notes block: unavailable renders a dash line
  ---
  duration_ms: 0.633118
  ...
# Subtest: heading matcher: fences, level, case, and first-only
ok 652 - heading matcher: fences, level, case, and first-only
  ---
  duration_ms: 0.572182
  ...
# Subtest: heading chip copy: room, full, crowded, exempt, unavailable
ok 653 - heading chip copy: room, full, crowded, exempt, unavailable
  ---
  duration_ms: 0.525473
  ...
# Subtest: heading chip key is stable for equal models
ok 654 - heading chip key is stable for equal models
  ---
  duration_ms: 0.2044
  ...
# Subtest: reading view: appends the chip to the matching h2 only
ok 655 - reading view: appends the chip to the matching h2 only
  ---
  duration_ms: 1.864208
  ...
# Subtest: reading view: no chip for ineligible notes
ok 656 - reading view: no chip for ineligible notes
  ---
  duration_ms: 0.169905
  ...
# Subtest: one live-refresh fan-out reaches every family
ok 657 - one live-refresh fan-out reaches every family
  ---
  duration_ms: 1.182627
  ...
# Subtest: ledger-tools CSS is theme-safe for the new views
ok 658 - ledger-tools CSS is theme-safe for the new views
  ---
  duration_ms: 0.73845
  ...
# Subtest: maxReadyPerNote defaults to 5 and validates 1–999
ok 659 - maxReadyPerNote defaults to 5 and validates 1–999
  ---
  duration_ms: 2.533246
  ...
# Subtest: loadPlanCaps caches on a stat key and detects edits
ok 660 - loadPlanCaps caches on a stat key and detects edits
  ---
  duration_ms: 0.792473
  ...
# Subtest: loadPlanCaps handles deletion, invalid edits, and recovery
ok 661 - loadPlanCaps handles deletion, invalid edits, and recovery
  ---
  duration_ms: 0.55018
  ...
# Subtest: loadPlanCaps without statSync reads through uncached
ok 662 - loadPlanCaps without statSync reads through uncached
  ---
  duration_ms: 0.349257
  ...
# Subtest: noteFrontmatter resolves through getFileCache, not getCache
ok 663 - noteFrontmatter resolves through getFileCache, not getCache
  ---
  duration_ms: 0.761163
  ...
# Subtest: task_refresh applies through the shared reader
ok 664 - task_refresh applies through the shared reader
  ---
  duration_ms: 3.030014
  ...
# Subtest: noteReadyKindFromType covers every R11 form
ok 665 - noteReadyKindFromType covers every R11 form
  ---
  duration_ms: 0.470899
  ...
# Subtest: noteReadyStatusLabel mirrors ProjectStatus::parse
ok 666 - noteReadyStatusLabel mirrors ProjectStatus::parse
  ---
  duration_ms: 0.297909
  ...
# Subtest: noteReadyParentStem strips alias, heading, and path
ok 667 - noteReadyParentStem strips alias, heading, and path
  ---
  duration_ms: 0.448716
  ...
# Subtest: parseNoteReadyCap covers every R8 form
ok 668 - parseNoteReadyCap covers every R8 form
  ---
  duration_ms: 0.682082
  ...
# Subtest: R1: 6 tasks at the default cap are crowded with over_by 1
ok 669 - R1: 6 tasks at the default cap are crowded with over_by 1
  ---
  duration_ms: 8.505616
  ...
# Subtest: R2: 5 tasks are full with no lint
ok 670 - R2: 5 tasks are full with no lint
  ---
  duration_ms: 2.092986
  ...
# Subtest: R3: hidden, future, blocked, and non-TODO rows never count
ok 671 - R3: hidden, future, blocked, and non-TODO rows never count
  ---
  duration_ms: 2.227081
  ...
# Subtest: R4: make-up splits 1 ready + 1 new + 1 rotten
ok 672 - R4: make-up splits 1 ready + 1 new + 1 rotten
  ---
  duration_ms: 1.567322
  ...
# Subtest: R5: recurring rows are excluded but tallied
ok 673 - R5: recurring rows are excluded but tallied
  ---
  duration_ms: 1.125599
  ...
# Subtest: R6: a visible ^prj task never counts
ok 674 - R6: a visible ^prj task never counts
  ---
  duration_ms: 0.928943
  ...
# Subtest: R7: daily, untyped, template, done, and dash rows are absent
ok 675 - R7: daily, untyped, template, done, and dash rows are absent
  ---
  duration_ms: 2.059201
  ...
# Subtest: R8: ready_cap forms map to cap, exempt, or lint-then-default
ok 676 - R8: ready_cap forms map to cap, exempt, or lint-then-default
  ---
  duration_ms: 4.034691
  ...
# Subtest: R9: a parent with two children counts 3
ok 677 - R9: a parent with two children counts 3
  ---
  duration_ms: 1.394071
  ...
# Subtest: R10: terminal projects are not capped and lint once
ok 678 - R10: terminal projects are not capped and lint once
  ---
  duration_ms: 1.729893
  ...
# Subtest: R11: every type form and nested folders are eligible
ok 679 - R11: every type form and nested folders are eligible
  ---
  duration_ms: 1.730773
  ...
# Subtest: R12: stamping a NEW task keeps the count and moves the make-up
ok 680 - R12: stamping a NEW task keeps the count and moves the make-up
  ---
  duration_ms: 3.852243
  ...
# Subtest: R13: a Today-linked task still counts
ok 681 - R13: a Today-linked task still counts
  ---
  duration_ms: 1.512537
  ...
# Subtest: R14: max_ready_per_note 3 caps others while ready_cap 8 holds
ok 682 - R14: max_ready_per_note 3 caps others while ready_cap 8 holds
  ---
  duration_ms: 5.572919
  ...
# Subtest: api.noteReady is frozen at version 1 under api v3
ok 683 - api.noteReady is frozen at version 1 under api v3
  ---
  duration_ms: 0.602971
  ...
# Subtest: counted and inCrowdedNote resolve per task
ok 684 - counted and inCrowdedNote resolve per task
  ---
  duration_ms: 4.653413
  ...
# Subtest: groupLabel ranks crowded notes by excess
ok 685 - groupLabel ranks crowded notes by excess
  ---
  duration_ms: 6.79455
  ...
# Subtest: snapshot sorts crowded, full, room, empty, exempt and splits totals
ok 686 - snapshot sorts crowded, full, room, empty, exempt and splits totals
  ---
  duration_ms: 7.420895
  ...
# Subtest: missing Tasks data and a cold cache are unavailable, never zero
ok 687 - missing Tasks data and a cold cache are unavailable, never zero
  ---
  duration_ms: 1.396576
  ...
# Subtest: throwing Tasks guards never throw
ok 688 - throwing Tasks guards never throw
  ---
  duration_ms: 0.764389
  ...
# Subtest: snapshot reuses the memo without reparsing or re-walking
ok 689 - snapshot reuses the memo without reparsing or re-walking
  ---
  duration_ms: 1.560138
  ...
# Subtest: a task edit rebuilds through the cache-update handler
ok 690 - a task edit rebuilds through the cache-update handler
  ---
  duration_ms: 1.768366
  ...
# Subtest: a ready_cap edit rebuilds and fires the query-refresh trigger
ok 691 - a ready_cap edit rebuilds and fires the query-refresh trigger
  ---
  duration_ms: 1.342102
  ...
# Subtest: rename and delete move the eligibility entry
ok 692 - rename and delete move the eligibility entry
  ---
  duration_ms: 1.605223
  ...
# Subtest: day rollover rebuilds the snapshot date
ok 693 - day rollover rebuilds the snapshot date
  ---
  duration_ms: 1.270054
  ...
# Subtest: a config edit flows through the stat cache
ok 694 - a config edit flows through the stat cache
  ---
  duration_ms: 13.074259
  ...
# Subtest: untyped and non-markdown vault events are no-ops
ok 695 - untyped and non-markdown vault events are no-ops
  ---
  duration_ms: 1.103246
  ...
# Subtest: memo hits never re-walk the vault
ok 696 - memo hits never re-walk the vault
  ---
  duration_ms: 53.8437
  ...
# Subtest: the startup storm is linear
ok 697 - the startup storm is linear
  ---
  duration_ms: 15.203122
  ...
# Subtest: the first resolved event forces one rebuild and later ones do not
ok 698 - the first resolved event forces one rebuild and later ones do not
  ---
  duration_ms: 2.479733
  ...
# Subtest: noteReadyEvaluate is pure and mirrors the Rust totals
ok 699 - noteReadyEvaluate is pure and mirrors the Rust totals
  ---
  duration_ms: 0.454488
  ...
# Subtest: conformance: merged name with duplicate
ok 700 - conformance: merged name with duplicate
  ---
  duration_ms: 3.78754
  ...
# Subtest: conformance: link forms and exclusions
ok 701 - conformance: link forms and exclusions
  ---
  duration_ms: 0.891972
  ...
# Subtest: conformance: unnamed placeholders
ok 702 - conformance: unnamed placeholders
  ---
  duration_ms: 0.470197
  ...
# Subtest: conformance: subheading in the section
ok 703 - conformance: subheading in the section
  ---
  duration_ms: 0.245769
  ...
# Subtest: conformance: open inventory label
ok 704 - conformance: open inventory label
  ---
  duration_ms: 0.36167
  ...
# Subtest: conformance: over the cap
ok 705 - conformance: over the cap
  ---
  duration_ms: 0.274013
  ...
# Subtest: conformance: cancelled and completed entries
ok 706 - conformance: cancelled and completed entries
  ---
  duration_ms: 0.325913
  ...
# Subtest: exactly at the cap is fine
ok 707 - exactly at the cap is fine
  ---
  duration_ms: 0.228717
  ...
# Subtest: no Pomodoros section degrades to an empty budget
ok 708 - no Pomodoros section degrades to an empty budget
  ---
  duration_ms: 0.505756
  ...
# Subtest: fenced code never counts
ok 709 - fenced code never counts
  ---
  duration_ms: 0.525763
  ...
# Subtest: highlight is the first open non-exempt entry; running is the timed one
ok 710 - highlight is the first open non-exempt entry; running is the timed one
  ---
  duration_ms: 0.425823
  ...
# Subtest: coercePlanCaps ignores a legacy max_now instead of failing
ok 711 - coercePlanCaps ignores a legacy max_now instead of failing
  ---
  duration_ms: 0.350278
  ...
# Subtest: parsePlanCaps defaults, overrides, and invalid fallbacks
ok 712 - parsePlanCaps defaults, overrides, and invalid fallbacks
  ---
  duration_ms: 0.394584
  ...
# Subtest: loadPlanCaps falls back to defaults without fs
ok 713 - loadPlanCaps falls back to defaults without fs
  ---
  duration_ms: 0.514121
  ...
# Subtest: loadPlanCaps falls back to defaults on mobile
ok 714 - loadPlanCaps falls back to defaults on mobile
  ---
  duration_ms: 0.274825
  ...
# Subtest: loadPlanCaps reads plan: and flags invalid values
ok 715 - loadPlanCaps reads plan: and flags invalid values
  ---
  duration_ms: 0.458205
  ...
# Subtest: planBlockTargetPath prefers the containing daily note
ok 716 - planBlockTargetPath prefers the containing daily note
  ---
  duration_ms: 0.874059
  ...
# Subtest: planBlockModel degrades to placeholders, never an error
ok 717 - planBlockModel degrades to placeholders, never an error
  ---
  duration_ms: 0.999488
  ...
# Subtest: planBlockModel renders chips, themes, and lints
ok 718 - planBlockModel renders chips, themes, and lints
  ---
  duration_ms: 4.192943
  ...
# Subtest: planBlockModel adds lane cap lints when a lane is over
ok 719 - planBlockModel adds lane cap lints when a lane is over
  ---
  duration_ms: 0.939864
  ...
# Subtest: plugin exposes the versioned api and registers the bob-plan block
ok 720 - plugin exposes the versioned api and registers the bob-plan block
  ---
  duration_ms: 4.810463
  ...
# Subtest: invalid plan block falls back to full defaults
ok 721 - invalid plan block falls back to full defaults
  ---
  duration_ms: 0.328477
  ...
# Subtest: entries require column-0 dash-space with one status char
ok 722 - entries require column-0 dash-space with one status char
  ---
  duration_ms: 0.219049
  ...
# Subtest: crlf line endings split like lf
ok 723 - crlf line endings split like lf
  ---
  duration_ms: 0.254987
  ...
# Subtest: conformance: empty target means the daily note
ok 724 - conformance: empty target means the daily note
  ---
  duration_ms: 0.207686
  ...
# Subtest: lane predicate matches hide subtags, case, and non-task
ok 725 - lane predicate matches hide subtags, case, and non-task
  ---
  duration_ms: 0.255147
  ...
# Subtest: planBlockModel daily badges follow dashboard section counts
ok 726 - planBlockModel daily badges follow dashboard section counts
  ---
  duration_ms: 2.227031
  ...
# Subtest: planBlockModel keeps a supplied unavailable dashboard budget
ok 727 - planBlockModel keeps a supplied unavailable dashboard budget
  ---
  duration_ms: 0.341071
  ...
# Subtest: work tones: TODAY override and unavailable stay neutral in planBlockModel
ok 728 - work tones: TODAY override and unavailable stay neutral in planBlockModel
  ---
  duration_ms: 0.290574
  ...
# Subtest: parser accepts the PM1-PM5 conformance vectors verbatim
ok 729 - parser accepts the PM1-PM5 conformance vectors verbatim
  ---
  duration_ms: 1.834292
  ...
# Subtest: parser rejects the PM7-PM12 conformance vectors verbatim
ok 730 - parser rejects the PM7-PM12 conformance vectors verbatim
  ---
  duration_ms: 0.291045
  ...
# Subtest: PM6 with the ladder unknown omits P-labels instead of guessing
ok 731 - PM6 with the ladder unknown omits P-labels instead of guessing
  ---
  duration_ms: 0.196274
  ...
# Subtest: PM13-PM17 ladder and line variants hold
ok 732 - PM13-PM17 ladder and line variants hold
  ---
  duration_ms: 0.31959
  ...
# Subtest: no model output contains a double colon
ok 733 - no model output contains a double colon
  ---
  duration_ms: 0.862246
  ...
# Subtest: element structure and the decorative/inheritColor options
ok 734 - element structure and the decorative/inheritColor options
  ---
  duration_ms: 0.427717
  ...
# Subtest: Live Preview decorations fold space, reveal, and refuse
ok 735 - Live Preview decorations fold space, reveal, and refuse
  ---
  duration_ms: 1.31529
  ...
# Subtest: a line with fresh and priority fields gets a disjoint decoration
ok 736 - a line with fresh and priority fields gets a disjoint decoration
  ---
  duration_ms: 0.201274
  ...
# Subtest: widget mousedown reveals the field at the folded offset
ok 737 - widget mousedown reveals the field at the folded offset
  ---
  duration_ms: 0.610205
  ...
# Subtest: rendered views split task nodes and skip exclusions
ok 738 - rendered views split task nodes and skip exclusions
  ---
  duration_ms: 1.537445
  ...
# Subtest: ladder coercion is lenient: valid, partial, and unknown
ok 739 - ladder coercion is lenient: valid, partial, and unknown
  ---
  duration_ms: 0.418719
  ...
# Subtest: ladder snapshot reads the file and reuses the cache
ok 740 - ladder snapshot reads the file and reuses the cache
  ---
  duration_ms: 23.246887
  ...
# Subtest: ladder snapshot degrades on missing files and parse errors
ok 741 - ladder snapshot degrades on missing files and parse errors
  ---
  duration_ms: 1.334277
  ...
# Subtest: ladder snapshot is unknown on mobile
ok 742 - ladder snapshot is unknown on mobile
  ---
  duration_ms: 15.279075
  ...
# Subtest: api.priorityMarks v1 is additive, sync, and never throwing
ok 743 - api.priorityMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 5.759955
  ...
# Subtest: session toggle and onload wiring
ok 744 - session toggle and onload wiring
  ---
  duration_ms: 1.081445
  ...
# Subtest: styles.css contract: masks, both hosts, repair flag, resting
ok 745 - styles.css contract: masks, both hosts, repair flag, resting
  ---
  duration_ms: 0.830285
  ...
# Subtest: P1/P3/P4: open entries mark plain and aliased links
ok 746 - P1/P3/P4: open entries mark plain and aliased links
  ---
  duration_ms: 2.595385
  ...
# Subtest: P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
ok 747 - P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
  ---
  duration_ms: 2.633076
  ...
# Subtest: P5: closed entries never mark, even with 🍅 history
ok 748 - P5: closed entries never mark, even with 🍅 history
  ---
  duration_ms: 0.756744
  ...
# Subtest: P6/P7: embedded and struck links never mark
ok 749 - P6/P7: embedded and struck links never mark
  ---
  duration_ms: 0.274434
  ...
# Subtest: P8: both trailing-\# move-only forms mark
ok 750 - P8: both trailing-\# move-only forms mark
  ---
  duration_ms: 0.306785
  ...
# Subtest: P9: nested and prose-mixed links never mark
ok 751 - P9: nested and prose-mixed links never mark
  ---
  duration_ms: 0.221773
  ...
# Subtest: P10: fenced, off-section, and off-note links never mark
ok 752 - P10: fenced, off-section, and off-note links never mark
  ---
  duration_ms: 0.447884
  ...
# Subtest: P11: unresolved targets and non-task blocks get no mark
ok 753 - P11: unresolved targets and non-task blocks get no mark
  ---
  duration_ms: 0.584045
  ...
# Subtest: P13: a same-note target reads the live doc
ok 754 - P13: a same-note target reads the live doc
  ---
  duration_ms: 0.959271
  ...
# Subtest: P14: expect() wins until the cache agrees or 4 s pass
ok 755 - P14: expect() wins until the cache agrees or 4 s pass
  ---
  duration_ms: 1.22056
  ...
# Subtest: tooltip, element structure, and eq
ok 756 - tooltip, element structure, and eq
  ---
  duration_ms: 0.404682
  ...
# Subtest: Live Preview places one widget at each In Progress link
ok 757 - Live Preview places one widget at each In Progress link
  ---
  duration_ms: 0.667564
  ...
# Subtest: widget mousedown places the cursor at the link start
ok 758 - widget mousedown places the cursor at the link start
  ---
  duration_ms: 0.461932
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
ok 759 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 0.548087
  ...
# Subtest: Reading view marks In Progress rows and dedupes
ok 760 - Reading view marks In Progress rows and dedupes
  ---
  duration_ms: 1.505484
  ...
# Subtest: Reading view refuses every non-mark row
ok 761 - Reading view refuses every non-mark row
  ---
  duration_ms: 1.458885
  ...
# Subtest: Reading view allows the 🍅 prefix and the trailing \# marker
ok 762 - Reading view allows the 🍅 prefix and the trailing \# marker
  ---
  duration_ms: 0.414842
  ...
# Subtest: api.progressMarks v1 is additive, sync, and never throwing
ok 763 - api.progressMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.813863
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 764 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 0.818994
  ...
# Subtest: changed-file and rollover refreshes
ok 765 - changed-file and rollover refreshes
  ---
  duration_ms: 0.412567
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 766 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.09418
  ...
# Subtest: styles.css contract: glyph, box, motion, toggle, calm
ok 767 - styles.css contract: glyph, box, motion, toggle, calm
  ---
  duration_ms: 0.566311
  ...
# Subtest: max_ready defaults to 100 for missing, absent, and null values
ok 768 - max_ready defaults to 100 for missing, absent, and null values
  ---
  duration_ms: 1.607549
  ...
# Subtest: max_ready accepts a custom positive cap
ok 769 - max_ready accepts a custom positive cap
  ---
  duration_ms: 0.237613
  ...
# Subtest: max_ready rejects zero, negative, fractions, strings, booleans, and overflow
ok 770 - max_ready rejects zero, negative, fractions, strings, booleans, and overflow
  ---
  duration_ms: 1.121582
  ...
# Subtest: old configurations and legacy max_now still load
ok 771 - old configurations and legacy max_now still load
  ---
  duration_ms: 0.29854
  ...
# Subtest: READY boundary: only a strict excess turns red
ok 772 - READY boundary: only a strict excess turns red
  ---
  duration_ms: 2.465967
  ...
# Subtest: READY custom-cap boundary
ok 773 - READY custom-cap boundary
  ---
  duration_ms: 0.263863
  ...
# Subtest: READY over is independent of the PLAN ledger status
ok 774 - READY over is independent of the PLAN ledger status
  ---
  duration_ms: 7.529974
  ...
# Subtest: READY predicate: statuses, custom TODO symbols, and non-tasks
ok 775 - READY predicate: statuses, custom TODO symbols, and non-tasks
  ---
  duration_ms: 0.248334
  ...
# Subtest: READY predicate: blocked uses the full list, even outside the queue
ok 776 - READY predicate: blocked uses the full list, even outside the queue
  ---
  duration_ms: 0.449988
  ...
# Subtest: READY predicate: past, today, and future schedules
ok 777 - READY predicate: past, today, and future schedules
  ---
  duration_ms: 0.537005
  ...
# Subtest: READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
ok 778 - READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
  ---
  duration_ms: 0.2568
  ...
# Subtest: READY predicate: Today exclusion
ok 779 - READY predicate: Today exclusion
  ---
  duration_ms: 0.159845
  ...
# Subtest: readyTaskVisible excludes hide variants like Tasks
ok 780 - readyTaskVisible excludes hide variants like Tasks
  ---
  duration_ms: 0.165886
  ...
# Subtest: daily and dashboard share the READY element contract
ok 781 - daily and dashboard share the READY element contract
  ---
  duration_ms: 10.693942
  ...
# Subtest: READY placeholder keeps the limit in its tooltip
ok 782 - READY placeholder keeps the limit in its tooltip
  ---
  duration_ms: 0.226653
  ...
# Subtest: READY keyboard and modifier-key navigation
ok 783 - READY keyboard and modifier-key navigation
  ---
  duration_ms: 0.961696
  ...
# Subtest: READY unavailable without Tasks, on Cold/Initializing, or before Today
ok 784 - READY unavailable without Tasks, on Cold/Initializing, or before Today
  ---
  duration_ms: 2.174662
  ...
# Subtest: READY counts a valid empty queue as zero, not unavailable
ok 785 - READY counts a valid empty queue as zero, not unavailable
  ---
  duration_ms: 1.205151
  ...
# Subtest: READY stays compatible with hosts exposing only getTasks()
ok 786 - READY stays compatible with hosts exposing only getTasks()
  ---
  duration_ms: 2.07972
  ...
# Subtest: READY degrades to unavailable when the Today predicate throws
ok 787 - READY degrades to unavailable when the Today predicate throws
  ---
  duration_ms: 0.710636
  ...
# Subtest: READY renders label/value spans for every budget state
ok 788 - READY renders label/value spans for every budget state
  ---
  duration_ms: 1.44579
  ...
# Subtest: READY live refresh keeps the anchor, spans, and handlers
ok 789 - READY live refresh keeps the anchor, spans, and handlers
  ---
  duration_ms: 1.445931
  ...
# Subtest: READY refresh crosses the over-cap boundary and back
ok 790 - READY refresh crosses the over-cap boundary and back
  ---
  duration_ms: 0.60747
  ...
# Subtest: READY refresh crosses the unavailable boundary and back
ok 791 - READY refresh crosses the unavailable boundary and back
  ---
  duration_ms: 0.613441
  ...
# Subtest: READY never assigns the Obsidian text setter
ok 792 - READY never assigns the Obsidian text setter
  ---
  duration_ms: 1.15782
  ...
# Subtest: READY gating excludes review buckets and keeps the partition
ok 793 - READY gating excludes review buckets and keeps the partition
  ---
  duration_ms: 0.348776
  ...
# Subtest: gated READY tooltip carries total lane pressure
ok 794 - gated READY tooltip carries total lane pressure
  ---
  duration_ms: 0.150658
  ...
# Subtest: planBlockModel gates READY and shares the lane tooltip
ok 795 - planBlockModel gates READY and shares the lane tooltip
  ---
  duration_ms: 0.661101
  ...
# Subtest: READY lint appears only on a strict excess
ok 796 - READY lint appears only on a strict excess
  ---
  duration_ms: 3.976862
  ...
# Subtest: READY lint uses a custom cap
ok 797 - READY lint uses a custom cap
  ---
  duration_ms: 0.609273
  ...
# Subtest: lane lints appear in NEXT, PENDING, READY order
ok 798 - lane lints appear in NEXT, PENDING, READY order
  ---
  duration_ms: 3.349414
  ...
# Subtest: READY lint uses the gated count
ok 799 - READY lint uses the gated count
  ---
  duration_ms: 1.809884
  ...
# Subtest: READY lint stays silent while unavailable
ok 800 - READY lint stays silent while unavailable
  ---
  duration_ms: 0.461341
  ...
# Subtest: READY speaks each host's chip language (daily single-tone, dash two-tone)
ok 801 - READY speaks each host's chip language (daily single-tone, dash two-tone)
  ---
  duration_ms: 2.795025
  ...
# Subtest: daily paint carries lane pressure to the shared READY renderer
ok 802 - daily paint carries lane pressure to the shared READY renderer
  ---
  duration_ms: 19.488262
  ...
# Subtest: daily paint degrades to the legacy tooltip without freshness
ok 803 - daily paint degrades to the legacy tooltip without freshness
  ---
  duration_ms: 2.333143
  ...
# Subtest: work tones: READY model carries the displayed-count tone
ok 804 - work tones: READY model carries the displayed-count tone
  ---
  duration_ms: 0.216503
  ...
# Subtest: parseTrigger parses D[-]<N> dated-entry triggers with offset and span
ok 805 - parseTrigger parses D[-]<N> dated-entry triggers with offset and span
  ---
  duration_ms: 2.628948
  ...
# Subtest: computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
ok 806 - computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
  ---
  duration_ms: 0.453716
  ...
# Subtest: expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
ok 807 - expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
  ---
  duration_ms: 0.530302
  ...
# Subtest: findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
ok 808 - findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
  ---
  duration_ms: 0.363483
  ...
# Subtest: compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
ok 809 - compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
  ---
  duration_ms: 0.332675
  ...
# Subtest: parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
ok 810 - parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
  ---
  duration_ms: 0.154585
  ...
# Subtest: computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
ok 811 - computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
  ---
  duration_ms: 0.187849
  ...
# Subtest: findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
ok 812 - findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
  ---
  duration_ms: 0.191495
  ...
# Subtest: findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
ok 813 - findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
  ---
  duration_ms: 0.323427
  ...
# Subtest: expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
ok 814 - expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
  ---
  duration_ms: 0.844281
  ...
# Subtest: regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
ok 815 - regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
  ---
  duration_ms: 0.406386
  ...
# Subtest: expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
ok 816 - expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
  ---
  duration_ms: 0.373563
  ...
# Subtest: stats fence body sets defaults only and ignores the rest
ok 817 - stats fence body sets defaults only and ignores the rest
  ---
  duration_ms: 1.932279
  ...
# Subtest: stats tile models cover every unit and every quality
ok 818 - stats tile models cover every unit and every quality
  ---
  duration_ms: 0.58703
  ...
# Subtest: stats spark bars mark null gaps, zero ticks, and hollow today
ok 819 - stats spark bars mark null gaps, zero ticks, and hollow today
  ---
  duration_ms: 0.388882
  ...
# Subtest: stats table rows and CSV share the same points
ok 820 - stats table rows and CSV share the same points
  ---
  duration_ms: 0.800879
  ...
# Subtest: stats overview ids prefer the fence, then config, then report order
ok 821 - stats overview ids prefer the fence, then config, then report order
  ---
  duration_ms: 1.137702
  ...
# Subtest: stats window label always states today and tracking start
ok 822 - stats window label always states today and tracking start
  ---
  duration_ms: 0.264836
  ...
# Subtest: stats view state is session-only and per source path
ok 823 - stats view state is session-only and per source path
  ---
  duration_ms: 4.222551
  ...
# Subtest: stats block renders header, tiles, table, and footer from JSON
ok 824 - stats block renders header, tiles, table, and footer from JSON
  ---
  duration_ms: 43.103338
  ...
# Subtest: stats block shows an actionable card with Retry when bob fails
ok 825 - stats block shows an actionable card with Retry when bob fails
  ---
  duration_ms: 42.975234
  ...
# Subtest: stats block registers the processor and the Open Stats command
ok 826 - stats block registers the processor and the Open Stats command
  ---
  duration_ms: 1.729311
  ...
# Subtest: stats stylesheet contract: selectors, tabular-nums, motion, colors
ok 827 - stats stylesheet contract: selectors, tabular-nums, motion, colors
  ---
  duration_ms: 1.432795
  ...
# Subtest: Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
ok 828 - Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
  ---
  duration_ms: 4.027619
  ...
# Subtest: prior buckets align by elapsed position and omit invalid and provisional points
ok 829 - prior buckets align by elapsed position and omit invalid and provisional points
  ---
  duration_ms: 1.281085
  ...
# Subtest: chart renders SVG safely and keeps secondary focus metrics selectable
ok 830 - chart renders SVG safely and keeps secondary focus metrics selectable
  ---
  duration_ms: 17.2455
  ...
# Subtest: grouped chart pins honest buckets, bounds daily detail, and opens validated notes
ok 831 - grouped chart pins honest buckets, bounds daily detail, and opens validated notes
  ---
  duration_ms: 7.054697
  ...
# Subtest: local focus, table, pin, and definition changes reuse the retained report
ok 832 - local focus, table, pin, and definition changes reuse the retained report
  ---
  duration_ms: 9.646042
  ...
# Subtest: keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
ok 833 - keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
  ---
  duration_ms: 37.551672
  ...
# Subtest: schema-1 fallback keeps day quartiles and never invents grouped daily history
ok 834 - schema-1 fallback keeps day quartiles and never invents grouped daily history
  ---
  duration_ms: 4.020224
  ...
# Subtest: ResizeObserver redraws cached data and disconnects across rerenders and unload
ok 835 - ResizeObserver redraws cached data and disconnects across rerenders and unload
  ---
  duration_ms: 131.810781
  ...
# Subtest: stats resolution prefers stats.bob_path, then candidates, then PATH
ok 836 - stats resolution prefers stats.bob_path, then candidates, then PATH
  ---
  duration_ms: 3.579654
  ...
# Subtest: stats home expansion and range/offset normalization
ok 837 - stats home expansion and range/offset normalization
  ---
  duration_ms: 0.46066
  ...
# Subtest: stats fetch always runs show -a -f json plus the chosen flags
ok 838 - stats fetch always runs show -a -f json plus the chosen flags
  ---
  duration_ms: 0.430752
  ...
# Subtest: stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
ok 839 - stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
  ---
  duration_ms: 5.300658
  ...
# Subtest: stats spawn maps ENOENT, timeouts, and stderr to named errors
ok 840 - stats spawn maps ENOENT, timeouts, and stderr to named errors
  ---
  duration_ms: 2.618158
  ...
# Subtest: stats decode accepts schema 1 and rejects the rest defensively
ok 841 - stats decode accepts schema 1 and rejects the rest defensively
  ---
  duration_ms: 0.265547
  ...
# Subtest: stats error cards name the cause and the stats.bob_path fix
ok 842 - stats error cards name the cause and the stats.bob_path fix
  ---
  duration_ms: 0.42972
  ...
# Subtest: stats fetch shares one flight and coalesces one follow-up
ok 843 - stats fetch shares one flight and coalesces one follow-up
  ---
  duration_ms: 22.476955
  ...
# Subtest: stats cache is a small LRU keyed by the argument list
ok 844 - stats cache is a small LRU keyed by the argument list
  ---
  duration_ms: 2.661441
  ...
# Subtest: stats stale entries return immediately and refresh in the background
ok 845 - stats stale entries return immediately and refresh in the background
  ---
  duration_ms: 1.424349
  ...
# Subtest: stats api v2 keeps append and adds fetch plus bobPath
ok 846 - stats api v2 keeps append and adds fetch plus bobPath
  ---
  duration_ms: 0.704635
  ...
# Subtest: statsHomeDir defaults to the real home and strips a trailing slash
ok 847 - statsHomeDir defaults to the real home and strips a trailing slash
  ---
  duration_ms: 0.215472
  ...
# Subtest: stats mac regression: un-injected resolution probes the real home first
ok 848 - stats mac regression: un-injected resolution probes the real home first
  ---
  duration_ms: 0.230199
  ...
# Subtest: stats absolute candidates are probed verbatim with no doubled slashes
ok 849 - stats absolute candidates are probed verbatim with no doubled slashes
  ---
  duration_ms: 0.256189
  ...
# Subtest: stats with no home probes only absolute candidates
ok 850 - stats with no home probes only absolute candidates
  ---
  duration_ms: 0.304781
  ...
# Subtest: stats tilde config expands against the real home
ok 851 - stats tilde config expands against the real home
  ---
  duration_ms: 0.174283
  ...
# Subtest: stats candidate and tried lists share one source of truth
ok 852 - stats candidate and tried lists share one source of truth
  ---
  duration_ms: 0.172018
  ...
# Subtest: stats spawn bob-not-found tried list uses the real home
ok 853 - stats spawn bob-not-found tried list uses the real home
  ---
  duration_ms: 1.246019
  ...
# Subtest: stats unload clears views, timers, cache, and flights
ok 854 - stats unload clears views, timers, cache, and flights
  ---
  duration_ms: 0.692272
  ...
# Subtest: stats namespace v1 serializes versioned review answer JSONL
ok 855 - stats namespace v1 serializes versioned review answer JSONL
  ---
  duration_ms: 7.470821
  ...
# Subtest: stats journal rejects invalid calendar days and outcomes
ok 856 - stats journal rejects invalid calendar days and outcomes
  ---
  duration_ms: 1.016871
  ...
# Subtest: statsReviewHost lowercases, cuts at the first dot, and never throws
ok 857 - statsReviewHost lowercases, cuts at the first dot, and never throws
  ---
  duration_ms: 0.150397
  ...
# Subtest: stats journal plugin passthrough keeps a semver writer and falls back otherwise
ok 858 - stats journal plugin passthrough keeps a semver writer and falls back otherwise
  ---
  duration_ms: 0.855502
  ...
# Subtest: panel dispatch covers every family, custom kinds, and the net exception
ok 859 - panel dispatch covers every family, custom kinds, and the net exception
  ---
  duration_ms: 1.636704
  ...
# Subtest: pomodoro panel shows the supplied total, shares, hue, and safe text
ok 860 - pomodoro panel shows the supplied total, shares, hue, and safe text
  ---
  duration_ms: 9.353044
  ...
# Subtest: task flow stacks signed values, keeps missing constituents missing, and labels series
ok 861 - task flow stacks signed values, keeps missing constituents missing, and labels series
  ---
  duration_ms: 6.440444
  ...
# Subtest: absent companions are named, custom filters are labeled overall, and net splits breakdowns
ok 862 - absent companions are named, custom filters are labeled overall, and net splits breakdowns
  ---
  duration_ms: 5.498295
  ...
# Subtest: journal panels pair answers with review time and a gapped keep chart under 90%
ok 863 - journal panels pair answers with review time and a gapped keep chart under 90%
  ---
  duration_ms: 15.426026
  ...
# Subtest: checklist calendar aligns Monday weeks with states, reasons, and provisional today
ok 864 - checklist calendar aligns Monday weeks with states, reasons, and provisional today
  ---
  duration_ms: 6.334191
  ...
# Subtest: grouped calendars reuse daily points and old schemas fall back with a label
ok 865 - grouped calendars reuse daily points and old schemas fall back with a label
  ---
  duration_ms: 3.579703
  ...
# Subtest: ISO year boundaries stay in one Monday week and chore dots expose text
ok 866 - ISO year boundaries stay in one Monday week and chore dots expose text
  ---
  duration_ms: 2.595154
  ...
# Subtest: panel day selection pins the shared day and never fetches
ok 867 - panel day selection pins the shared day and never fetches
  ---
  duration_ms: 9.247914
  ...
# Subtest: field and formula metrics keep only the focus chart and table
ok 868 - field and formula metrics keep only the focus chart and table
  ---
  duration_ms: 2.86005
  ...
# Subtest: TT vectors verbatim: task-line gate plus boundary tokens
ok 869 - TT vectors verbatim: task-line gate plus boundary tokens
  ---
  duration_ms: 2.869648
  ...
# Subtest: TT13-TT14 cursor reveal is inclusive
ok 870 - TT13-TT14 cursor reveal is inclusive
  ---
  duration_ms: 1.012232
  ...
# Subtest: TT16 coexistence: task tag range is disjoint from priority and date marks
ok 871 - TT16 coexistence: task tag range is disjoint from priority and date marks
  ---
  duration_ms: 1.19961
  ...
# Subtest: tooltip is exact and never contains a double colon
ok 872 - tooltip is exact and never contains a double colon
  ---
  duration_ms: 0.189863
  ...
# Subtest: element structure: empty widget span with tooltip attributes
ok 873 - element structure: empty widget span with tooltip attributes
  ---
  duration_ms: 0.249897
  ...
# Subtest: Live Preview decorations cover exactly the tag and respect reveal and code
ok 874 - Live Preview decorations cover exactly the tag and respect reveal and code
  ---
  duration_ms: 0.547996
  ...
# Subtest: widget mousedown reveals the tag start
ok 875 - widget mousedown reveals the tag start
  ---
  duration_ms: 0.482701
  ...
# Subtest: TR vectors verbatim: rendered views annotate eligible anchors in place
ok 876 - TR vectors verbatim: rendered views annotate eligible anchors in place
  ---
  duration_ms: 1.297226
  ...
# Subtest: TR9 toggle strips document-wide and re-annotates on enable
ok 877 - TR9 toggle strips document-wide and re-annotates on enable
  ---
  duration_ms: 0.962878
  ...
# Subtest: annotate and strip helpers are idempotent and defensive
ok 878 - annotate and strip helpers are idempotent and defensive
  ---
  duration_ms: 0.520293
  ...
# Subtest: session toggle and onload wiring
ok 879 - session toggle and onload wiring
  ---
  duration_ms: 3.831964
  ...
# Subtest: styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
ok 880 - styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
  ---
  duration_ms: 0.877966
  ...
# Subtest: TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
ok 881 - TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
  ---
  duration_ms: 0.363393
  ...
# Subtest: Live Preview ref decorations replace the whole pair and reveal both tags at once
ok 882 - Live Preview ref decorations replace the whole pair and reveal both tags at once
  ---
  duration_ms: 0.367992
  ...
# Subtest: ref element structure: book classes, reference label, and tooltip
ok 883 - ref element structure: book classes, reference label, and tooltip
  ---
  duration_ms: 0.136962
  ...
# Subtest: TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
ok 884 - TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
  ---
  duration_ms: 7.111626
  ...
# Subtest: TR11 verbatim: \#task \#references and reversed order keep the hash only
ok 885 - TR11 verbatim: \#task \#references and reversed order keep the hash only
  ---
  duration_ms: 0.330942
  ...
# Subtest: TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
ok 886 - TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
  ---
  duration_ms: 0.172259
  ...
# Subtest: TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
ok 887 - TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
  ---
  duration_ms: 0.603853
  ...
# Subtest: styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
ok 888 - styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
  ---
  duration_ms: 0.80654
  ...
# Subtest: T1 GTD: empty target resolves to the daily note
ok 889 - T1 GTD: empty target resolves to the daily note
  ---
  duration_ms: 2.70801
  ...
# Subtest: T2 markers: pomodoro mark counts, struck drops, embed counts
ok 890 - T2 markers: pomodoro mark counts, struck drops, embed counts
  ---
  duration_ms: 0.50308
  ...
# Subtest: T3 closed entries: links under completed/cancelled entries drop
ok 891 - T3 closed entries: links under completed/cancelled entries drop
  ---
  duration_ms: 0.172429
  ...
# Subtest: T4 shapes: mixed text and deeper descendants drop
ok 892 - T4 shapes: mixed text and deeper descendants drop
  ---
  duration_ms: 0.265417
  ...
# Subtest: T5 dedupe: same task twice keeps the first position
ok 893 - T5 dedupe: same task twice keeps the first position
  ---
  duration_ms: 0.302117
  ...
# Subtest: T6 fenced: links inside fenced blocks drop
ok 894 - T6 fenced: links inside fenced blocks drop
  ---
  duration_ms: 0.226713
  ...
# Subtest: T7 status: the link layer lists every dedicated link
ok 895 - T7 status: the link layer lists every dedicated link
  ---
  duration_ms: 0.261078
  ...
# Subtest: T8 unresolved: missing notes give no key
ok 896 - T8 unresolved: missing notes give no key
  ---
  duration_ms: 0.156659
  ...
# Subtest: T9 alias: aliased links count under their target
ok 897 - T9 alias: aliased links count under their target
  ---
  duration_ms: 0.36145
  ...
# Subtest: laneBudgetFromTasks counts the whole Next lane, Today included
ok 898 - laneBudgetFromTasks counts the whole Next lane, Today included
  ---
  duration_ms: 0.999858
  ...
# Subtest: laneBudgetFromTasks counts Pending by type and flags over-cap
ok 899 - laneBudgetFromTasks counts Pending by type and flags over-cap
  ---
  duration_ms: 0.327956
  ...
# Subtest: lane caps come from max_next/max_pending; legacy max_now is ignored
ok 900 - lane caps come from max_next/max_pending; legacy max_now is ignored
  ---
  duration_ms: 0.150578
  ...
# Subtest: reload event name matches the Tasks bundle subscription
ok 901 - reload event name matches the Tasks bundle subscription
  ---
  duration_ms: 0.075634
  ...
# Subtest: api v2 shape: Today and lane budgets, no nowBudget
ok 902 - api v2 shape: Today and lane budgets, no nowBudget
  ---
  duration_ms: 3.090861
  ...
# Subtest: cache rebuild answers isToday/todayRank in ledger order
ok 903 - cache rebuild answers isToday/todayRank in ledger order
  ---
  duration_ms: 1.175804
  ...
# Subtest: refresh fires only when the key set changes
ok 904 - refresh fires only when the key set changes
  ---
  duration_ms: 0.731497
  ...
# Subtest: unready to ready with empty TODAY still refreshes open badges
ok 905 - unready to ready with empty TODAY still refreshes open badges
  ---
  duration_ms: 0.711919
  ...
# Subtest: cache rebuilds on the daily changed event with the event content
ok 906 - cache rebuilds on the daily changed event with the event content
  ---
  duration_ms: 3.303155
  ...
# Subtest: cache rebuilds once on resolved and at midnight rollover
ok 907 - cache rebuilds once on resolved and at midnight rollover
  ---
  duration_ms: 0.967216
  ...
# Subtest: a done-today prerequisite shows the glyph
ok 908 - a done-today prerequisite shows the glyph
  ---
  duration_ms: 3.241247
  ...
# Subtest: done yesterday does not show the glyph
ok 909 - done yesterday does not show the glyph
  ---
  duration_ms: 0.376058
  ...
# Subtest: a struck link does not show the glyph
ok 910 - a struck link does not show the glyph
  ---
  duration_ms: 0.247342
  ...
# Subtest: a closed entry does not show the glyph
ok 911 - a closed entry does not show the glyph
  ---
  duration_ms: 0.212476
  ...
# Subtest: several prerequisites give +N
ok 912 - several prerequisites give +N
  ---
  duration_ms: 0.469687
  ...
# Subtest: the model refuses every non-glyph shape
ok 913 - the model refuses every non-glyph shape
  ---
  duration_ms: 0.754541
  ...
# Subtest: unblockedGlyphDoneToday needs DONE plus a today done date
ok 914 - unblockedGlyphDoneToday needs DONE plus a today done date
  ---
  duration_ms: 0.238816
  ...
# Subtest: tooltip names one prerequisite and counts several
ok 915 - tooltip names one prerequisite and counts several
  ---
  duration_ms: 0.267921
  ...
# Subtest: Live Preview places one glyph after each unblocked link
not ok 916 - Live Preview places one glyph after each unblocked link
  ---
  duration_ms: 1.902983
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:546:1'
  failureType: 'testCodeFailure'
  error: |-
    Expected values to be strictly equal:
    
    0 !== 1
    
  code: 'ERR_ASSERTION'
  name: 'AssertionError'
  expected: 1
  actual: 0
  operator: 'strictEqual'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:553:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Live Preview draws nothing without a warm cache or a live link
ok 917 - Live Preview draws nothing without a warm cache or a live link
  ---
  duration_ms: 0.786772
  ...
# Subtest: widget mousedown places the cursor past the link
not ok 918 - widget mousedown places the cursor past the link
  ---
  duration_ms: 0.362532
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:612:1'
  failureType: 'testCodeFailure'
  error: "Cannot read properties of undefined (reading 'value')"
  code: 'ERR_TEST_FAILURE'
  name: 'TypeError'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:615:69)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
not ok 919 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 0.348205
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:654:1'
  failureType: 'testCodeFailure'
  error: |-
    Expected values to be strictly equal:
    
    0 !== 1
    
  code: 'ERR_ASSERTION'
  name: 'AssertionError'
  expected: 1
  actual: 0
  operator: 'strictEqual'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:662:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Reading view glyphs unblocked rows and dedupes
not ok 920 - Reading view glyphs unblocked rows and dedupes
  ---
  duration_ms: 1.155516
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:849:1'
  failureType: 'testCodeFailure'
  error: |-
    Expected values to be strictly equal:
    
    0 !== 1
    
  code: 'ERR_ASSERTION'
  name: 'AssertionError'
  expected: 1
  actual: 0
  operator: 'strictEqual'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:858:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Reading view refuses every non-glyph row
ok 921 - Reading view refuses every non-glyph row
  ---
  duration_ms: 4.31156
  ...
# Subtest: api.unblockedGlyph v1 is additive, sync, and never throwing
ok 922 - api.unblockedGlyph v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.67571
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 923 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 1.063871
  ...
# Subtest: changed-file and rollover refreshes
ok 924 - changed-file and rollover refreshes
  ---
  duration_ms: 0.257482
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 925 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.082388
  ...
# Subtest: styles.css contract: faint glyph, Done token, toggle
ok 926 - styles.css contract: faint glyph, Done token, toggle
  ---
  duration_ms: 0.54498
  ...
# Subtest: Ledger Vim mappings restore \\p and retain the other normal-mode actions
ok 927 - Ledger Vim mappings restore \\p and retain the other normal-mode actions
  ---
  duration_ms: 2.101882
  ...
# Subtest: workBadgeTone boundary vectors at cap 100 use exact comparisons
ok 928 - workBadgeTone boundary vectors at cap 100 use exact comparisons
  ---
  duration_ms: 1.334357
  ...
# Subtest: workBadgeTone at cap 15 has no percentage rounding
ok 929 - workBadgeTone at cap 15 has no percentage rounding
  ---
  duration_ms: 0.228206
  ...
# Subtest: workBadgeTone default caps, small caps, and cap changes
ok 930 - workBadgeTone default caps, small caps, and cap changes
  ---
  duration_ms: 0.18861
  ...
# Subtest: workBadgeTone never coerces invalid input to zero
ok 931 - workBadgeTone never coerces invalid input to zero
  ---
  duration_ms: 0.232955
  ...
# Subtest: TODAY links bands with themes at cap 3
ok 932 - TODAY links bands with themes at cap 3
  ---
  duration_ms: 0.440541
  ...
# Subtest: TODAY theme overflow forces red, exact cap does not
ok 933 - TODAY theme overflow forces red, exact cap does not
  ---
  duration_ms: 0.273181
  ...
# Subtest: TODAY unavailable stays neutral, empty section is grey
ok 934 - TODAY unavailable stays neutral, empty section is grey
  ---
  duration_ms: 1.533106
  ...
# Subtest: PENDING/NEXT models color the section, READY its gated count
ok 935 - PENDING/NEXT models color the section, READY its gated count
  ---
  duration_ms: 0.674948
  ...
# Subtest: READY uses its gated count even when the total lane is larger
ok 936 - READY uses its gated count even when the total lane is larger
  ---
  duration_ms: 0.467172
  ...
# Subtest: cap equality still emits no cap lint
ok 937 - cap equality still emits no cap lint
  ---
  duration_ms: 3.013032
  ...
# Subtest: lane DOM keeps exactly one tone through transitions and unavailability
ok 938 - lane DOM keeps exactly one tone through transitions and unavailability
  ---
  duration_ms: 7.196207
  ...
# Subtest: READY DOM keeps exactly one tone and daily/dashboard models agree
ok 939 - READY DOM keeps exactly one tone and daily/dashboard models agree
  ---
  duration_ms: 1.203898
  ...
# SKIP dashboard integration: BOB_DASHBOARD_FILE is not set
# SKIP dashboard fallback integration: BOB_DASHBOARD_FILE is not set
# Subtest: daily TODAY chip uses the theme-overflow tone
ok 940 - daily TODAY chip uses the theme-overflow tone
  ---
  duration_ms: 16.215052
  ...
# Subtest: dashboard integration uses Work tones, TODAY override, and keeps Work order
ok 941 - dashboard integration uses Work tones, TODAY override, and keeps Work order
  ---
  duration_ms: 0.521305
  ...
# Subtest: dashboard fallbacks keep Work tones without plugin renderers or colors
ok 942 - dashboard fallbacks keep Work tones without plugin renderers or colors
  ---
  duration_ms: 0.309431
  ...
# Subtest: review checklist group helpers format exact completion and close notices
ok 943 - review checklist group helpers format exact completion and close notices
  ---
  duration_ms: 1.753397
  ...
# Subtest: claim declines without a current exact PRE/POST walk landing
ok 944 - claim declines without a current exact PRE/POST walk landing
  ---
  duration_ms: 5.908981
  ...
# Subtest: a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
ok 945 - a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
  ---
  duration_ms: 2.458743
  ...
# Subtest: checklist Ctrl+Enter holds its landing through the actual successor picker
ok 946 - checklist Ctrl+Enter holds its landing through the actual successor picker
  ---
  duration_ms: 8.158463
  ...
# Subtest: seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
ok 947 - seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
  ---
  duration_ms: 13.728336
  ...
# Subtest: a landed [?] checklist chore is claimed and completed
ok 948 - a landed [?] checklist chore is claimed and completed
  ---
  duration_ms: 0.59733
  ...
# Subtest: ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
ok 949 - ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
  ---
  duration_ms: 2.257549
  ...
# Subtest: live successor filtering skips a stale completed row
ok 950 - live successor filtering skips a stale completed row
  ---
  duration_ms: 0.557084
  ...
# Subtest: live group filtering reads each cross-note path once
ok 951 - live group filtering reads each cross-note path once
  ---
  duration_ms: 0.824554
  ...
# Subtest: Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
ok 952 - Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
  ---
  duration_ms: 2.779094
  ...
# Subtest: POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
ok 953 - POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
  ---
  duration_ms: 1.669176
  ...
# Subtest: ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
ok 954 - ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
  ---
  duration_ms: 0.905128
  ...
# Subtest: completion failure preserves cursor and landing and reports the Tasks failure
ok 955 - completion failure preserves cursor and landing and reports the Tasks failure
  ---
  duration_ms: 0.336473
  ...
# Subtest: reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
ok 956 - reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
  ---
  duration_ms: 1.460307
  ...
# Subtest: Alt+F on PRE stays with remaining PRE count and never stamps
ok 957 - Alt+F on PRE stays with remaining PRE count and never stamps
  ---
  duration_ms: 5.750877
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a stale cache
ok 958 - Ctrl+Alt+F completes seven PRE rows from a stale cache
  ---
  duration_ms: 13.077424
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a refreshed cache
ok 959 - Ctrl+Alt+F completes seven PRE rows from a refreshed cache
  ---
  duration_ms: 5.621101
  ...
# Subtest: POST stays put with the closing notice
ok 960 - POST stays put with the closing notice
  ---
  duration_ms: 1.234687
  ...
# Subtest: manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
ok 961 - manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
  ---
  duration_ms: 1.38812
  ...
# Subtest: manual Ctrl+Enter then ]s from a stale cache uses text-first identity
ok 962 - manual Ctrl+Enter then ]s from a stale cache uses text-first identity
  ---
  duration_ms: 0.932489
  ...
# Subtest: counted Alt+F skips checklist rows with the skip tail
ok 963 - counted Alt+F skips checklist rows with the skip tail
  ---
  duration_ms: 3.053738
  ...
# Subtest: missing cycler gate on a PRE row writes nothing
ok 964 - missing cycler gate on a PRE row writes nothing
  ---
  duration_ms: 0.668686
  ...
# Subtest: missing ledger checklist gate on a tagged line writes nothing
ok 965 - missing ledger checklist gate on a tagged line writes nothing
  ---
  duration_ms: 0.711948
  ...
# Subtest: a tagged line that is not a queue match falls through to recurring refusal
ok 966 - a tagged line that is not a queue match falls through to recurring refusal
  ---
  duration_ms: 0.47154
  ...
# Subtest: formatFreshStampChecklistSkipTail names the skipped count
ok 967 - formatFreshStampChecklistSkipTail names the skipped count
  ---
  duration_ms: 0.155256
  ...
# Subtest: partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
ok 968 - partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
  ---
  duration_ms: 0.329399
  ...
# Subtest: Task Link Alt+F skips a PRE target with the skip notice
ok 969 - Task Link Alt+F skips a PRE target with the skip notice
  ---
  duration_ms: 2.633538
  ...
# Subtest: P0 at interval 7 enters P2 with a previewed decay date and kept tail
ok 970 - P0 at interval 7 enters P2 with a previewed decay date and kept tail
  ---
  duration_ms: 3.250435
  ...
# Subtest: P0 at interval 30 enters P3
ok 971 - P0 at interval 30 enters P3
  ---
  duration_ms: 0.470838
  ...
# Subtest: fixed enter overrides the interval scan
ok 972 - fixed enter overrides the interval scan
  ---
  duration_ms: 0.431283
  ...
# Subtest: unknown enter disables Not now without disabling Keep/Reword
ok 973 - unknown enter disables Not now without disabling Keep/Reword
  ---
  duration_ms: 0.391637
  ...
# Subtest: P0 with no suitable level stays unavailable and never shortens the lease
ok 974 - P0 with no suitable level stays unavailable and never shortens the lease
  ---
  duration_ms: 0.343717
  ...
# Subtest: custom level order resolves entry in ladder order
ok 975 - custom level order resolves entry in ladder order
  ---
  duration_ms: 0.290324
  ...
# Subtest: unknown priority value disables Not now only
ok 976 - unknown priority value disables Not now only
  ---
  duration_ms: 0.321083
  ...
# Subtest: prioritized P2 below its roll limit stays on the same level
ok 977 - prioritized P2 below its roll limit stays on the same level
  ---
  duration_ms: 0.575679
  ...
# Subtest: P2 at its roll limit decays to P3
ok 978 - P2 at its roll limit decays to P3
  ---
  duration_ms: 0.705606
  ...
# Subtest: P2 streak derives from the task Schedule Log
ok 979 - P2 streak derives from the task Schedule Log
  ---
  duration_ms: 2.731724
  ...
# Subtest: configured decay:false keeps rolling past the limit
ok 980 - configured decay:false keeps rolling past the limit
  ---
  duration_ms: 0.369986
  ...
# Subtest: per-level rolls:0 decays immediately
ok 981 - per-level rolls:0 decays immediately
  ---
  duration_ms: 0.264625
  ...
# Subtest: terminal cancel substitutes a truthful same-level card roll
ok 982 - terminal cancel substitutes a truthful same-level card roll
  ---
  duration_ms: 0.292899
  ...
# Subtest: no future date in the window refuses Not now
ok 983 - no future date in the window refuses Not now
  ---
  duration_ms: 0.226131
  ...
# Subtest: Less often steps 7/14/30 to the next preset with a decision reason
ok 984 - Less often steps 7/14/30 to the next preset with a decision reason
  ---
  duration_ms: 0.424871
  ...
# Subtest: Less often at 90+ opens the constrained custom picker; 365 is unavailable
ok 985 - Less often at 90+ opens the constrained custom picker; 365 is unavailable
  ---
  duration_ms: 0.283271
  ...
# Subtest: previewed dates are stable for one random draw
ok 986 - previewed dates are stable for one random draw
  ---
  duration_ms: 0.259395
  ...
# Subtest: Keep saturates at 999 and Drop preserves keeps history
ok 987 - Keep saturates at 999 and Drop preserves keeps history
  ---
  duration_ms: 0.276398
  ...
# Subtest: kept tails preserve roll classification; decisions break it deliberately
ok 988 - kept tails preserve roll classification; decisions break it deliberately
  ---
  duration_ms: 0.754481
  ...
# Subtest: invalid priority config offers no priority-changing action
ok 989 - invalid priority config offers no priority-changing action
  ---
  duration_ms: 0.206214
  ...
# Subtest: decay off disables Not now but keeps counting
ok 990 - decay off disables Not now but keeps counting
  ---
  duration_ms: 0.172078
  ...
# Subtest: explicit level picks cover the ladder with previewed rolls
ok 991 - explicit level picks cover the ladder with previewed rolls
  ---
  duration_ms: 0.729703
  ...
# Subtest: card model is deeply frozen
ok 992 - card model is deeply frozen
  ---
  duration_ms: 0.179793
  ...
# Subtest: single Alt+F on an at-limit task opens the card and writes nothing
ok 993 - single Alt+F on an at-limit task opens the card and writes nothing
  ---
  duration_ms: 9.444698
  ...
# Subtest: dismissing the card writes nothing and does not advance
ok 994 - dismissing the card writes nothing and does not advance
  ---
  duration_ms: 1.363974
  ...
# Subtest: early dates open the card and write nothing
ok 995 - early dates open the card and write nothing
  ---
  duration_ms: 0.991312
  ...
# Subtest: namespace v5 with decide true stamps counted and opens no card
ok 996 - namespace v5 with decide true stamps counted and opens no card
  ---
  duration_ms: 4.183978
  ...
# Subtest: stale task-line change writes nothing
ok 997 - stale task-line change writes nothing
  ---
  duration_ms: 1.186234
  ...
# Subtest: stale local-day change writes nothing
ok 998 - stale local-day change writes nothing
  ---
  duration_ms: 1.206052
  ...
# Subtest: stale decay-config change writes nothing
ok 999 - stale decay-config change writes nothing
  ---
  duration_ms: 1.137381
  ...
# Subtest: stale priority-ladder config writes nothing
ok 1000 - stale priority-ladder config writes nothing
  ---
  duration_ms: 1.49824
  ...
# Subtest: stale child Schedule Log writes nothing
ok 1001 - stale child Schedule Log writes nothing
  ---
  duration_ms: 3.531001
  ...
# Subtest: Not now stamps, clears keeps, and advances exactly once
ok 1002 - Not now stamps, clears keeps, and advances exactly once
  ---
  duration_ms: 4.988533
  ...
# Subtest: Keep counts once and saturates at 999 without reset
not ok 1003 - Keep counts once and saturates at 999 without reset
  ---
  duration_ms: 1.861994
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/scripts/test-navigation-decision-card-handlers.cjs:546:1'
  failureType: 'testCodeFailure'
  error: '- [ ] #task Buy milk [fresh:: 2026-09-30] [keeps:: 3]'
  code: 'ERR_ASSERTION'
  name: 'AssertionError'
  expected:
  actual: 'Update Bob Ledger Tools to record review stats'
  operator: 'match'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/scripts/test-navigation-decision-card-handlers.cjs:569:12)
    async Test.run (node:internal/test_runner/test:980:9)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Reword stamps, clears, logs, and never advances
ok 1004 - Reword stamps, clears, logs, and never advances
  ---
  duration_ms: 1.488531
  ...
# Subtest: Drop cancels with the dropped-after-keeps reason and keeps history
ok 1005 - Drop cancels with the dropped-after-keeps reason and keeps history
  ---
  duration_ms: 0.726015
  ...
# Subtest: Less often at 90+ opens the picker and dismiss writes nothing
ok 1006 - Less often at 90+ opens the picker and dismiss writes nothing
  ---
  duration_ms: 0.611146
  ...
# Subtest: counted session skips at-limit and counts below-limit
ok 1007 - counted session skips at-limit and counts below-limit
  ---
  duration_ms: 0.729082
  ...
# Subtest: counted session skips at-limit on an early date
ok 1008 - counted session skips at-limit on an early date
  ---
  duration_ms: 0.620995
  ...
# Subtest: counted session with every target skipped writes nothing
ok 1009 - counted session with every target skipped writes nothing
  ---
  duration_ms: 0.29892
  ...
# Subtest: availability: decay on (or absent) may ask; decay off never asks
ok 1010 - availability: decay on (or absent) may ask; decay off never asks
  ---
  duration_ms: 1.00609
  ...
# Subtest: trigger: only an explicit decide row decides
ok 1011 - trigger: only an explicit decide row decides
  ---
  duration_ms: 0.185313
  ...
# Subtest: partition: exact at-limit rows skip, everything else stamps
ok 1012 - partition: exact at-limit rows skip, everything else stamps
  ---
  duration_ms: 0.845965
  ...
# Subtest: partition: empty and malformed input stamps nothing and skips nothing
ok 1013 - partition: empty and malformed input stamps nothing and skips nothing
  ---
  duration_ms: 0.163823
  ...
# Subtest: partition: enabled false stamps decision rows (older namespace fallback)
ok 1014 - partition: enabled false stamps decision rows (older namespace fallback)
  ---
  duration_ms: 0.166458
  ...
# Subtest: skip wording: singular, plural, and all-skipped notices
ok 1015 - skip wording: singular, plural, and all-skipped notices
  ---
  duration_ms: 0.192738
  ...
# Subtest: reword cursor: lands at the end of the task body before metadata
ok 1016 - reword cursor: lands at the end of the task body before metadata
  ---
  duration_ms: 0.352744
  ...
# Subtest: captured age: optional context ages, null when created is missing
ok 1017 - captured age: optional context ages, null when created is missing
  ---
  duration_ms: 0.400204
  ...
# Subtest: rows: P0 entry shows the recommended Not now with a clean window
ok 1018 - rows: P0 entry shows the recommended Not now with a clean window
  ---
  duration_ms: 2.796127
  ...
# Subtest: rows: invalid priority config disables Not now and levels, keeps safe rows
ok 1019 - rows: invalid priority config disables Not now and levels, keeps safe rows
  ---
  duration_ms: 0.674898
  ...
# Subtest: rows: picker-mode Less often and 365-day cap
ok 1020 - rows: picker-mode Less often and 365-day cap
  ---
  duration_ms: 0.920337
  ...
# Subtest: rows: terminal ladder keeps Enter available and never cancels
ok 1021 - rows: terminal ladder keeps Enter available and never cancels
  ---
  duration_ms: 0.584426
  ...
# Subtest: modal: Enter approves once; later keys cannot approve again
ok 1022 - modal: Enter approves once; later keys cannot approve again
  ---
  duration_ms: 0.513841
  ...
# Subtest: modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
ok 1023 - modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
  ---
  duration_ms: 0.337514
  ...
# Subtest: modal: key repeat and modified keys never approve
ok 1024 - modal: key repeat and modified keys never approve
  ---
  duration_ms: 0.216904
  ...
# Subtest: modal: Esc changes nothing — dismiss without a choice
ok 1025 - modal: Esc changes nothing — dismiss without a choice
  ---
  duration_ms: 0.124297
  ...
# Subtest: modal: unavailable actions cannot be chosen
ok 1026 - modal: unavailable actions cannot be chosen
  ---
  duration_ms: 0.17302
  ...
# Subtest: modal: a double callback applies once
ok 1027 - modal: a double callback applies once
  ---
  duration_ms: 0.090002
  ...
# Subtest: capability: the nav api exposes the card while loaded
ok 1028 - capability: the nav api exposes the card while loaded
  ---
  duration_ms: 0.325141
  ...
# Subtest: capability: unload drops the card so marks stop promising it
ok 1029 - capability: unload drops the card so marks stop promising it
  ---
  duration_ms: 0.140327
  ...
# Subtest: ladder lookup: the first priority property wins, null without one
ok 1030 - ladder lookup: the first priority property wins, null without one
  ---
  duration_ms: 0.156699
  ...
# Subtest: stage entry resolves the line itself and refuses prose
ok 1031 - stage entry resolves the line itself and refuses prose
  ---
  duration_ms: 2.897672
  ...
# Subtest: stage canonical order ranks \#hide last ahead of the lane
ok 1032 - stage canonical order ranks \#hide last ahead of the lane
  ---
  duration_ms: 0.307908
  ...
# Subtest: stage empty query shows same-note plus In Progress and Next only
ok 1033 - stage empty query shows same-note plus In Progress and Next only
  ---
  duration_ms: 4.328222
  ...
# Subtest: stage cap appends a type-to-search-more hint row
ok 1034 - stage cap appends a type-to-search-more hint row
  ---
  duration_ms: 3.237188
  ...
# Subtest: stage BLOCKED rows carry waits-on counts and short guard reasons
ok 1035 - stage BLOCKED rows carry waits-on counts and short guard reasons
  ---
  duration_ms: 1.924052
  ...
# Subtest: stage removal notices name the task description, not the block id
ok 1036 - stage removal notices name the task description, not the block id
  ---
  duration_ms: 0.687703
  ...
# Subtest: stage Task Link batches keep Depends on without refusal
ok 1037 - stage Task Link batches keep Depends on without refusal
  ---
  duration_ms: 0.614093
  ...
# Subtest: stage batch cycle check runs on the post-batch graph
ok 1038 - stage batch cycle check runs on the post-batch graph
  ---
  duration_ms: 1.185583
  ...
# Subtest: stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
ok 1039 - stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
  ---
  duration_ms: 9.774879
  ...
# Subtest: stage stale single add refuses and reopens
ok 1040 - stage stale single add refuses and reopens
  ---
  duration_ms: 6.944615
  ...
# Subtest: stage mirror burst keeps the baseline owner across an insertion above
ok 1041 - stage mirror burst keeps the baseline owner across an insertion above
  ---
  duration_ms: 1003.74179
  ...
# Subtest: stage mirror burst clears on a text-only line deletion
ok 1042 - stage mirror burst clears on a text-only line deletion
  ---
  duration_ms: 1001.332111
  ...
# Subtest: stage mirror vim dd clears the deleted line's owner
ok 1043 - stage mirror vim dd clears the deleted line's owner
  ---
  duration_ms: 1001.24148
  ...
# Subtest: stage badge counts open prerequisites without a block id
ok 1044 - stage badge counts open prerequisites without a block id
  ---
  duration_ms: 6.677546
  ...
# Subtest: stage badge names the future scheduled date with no open prerequisite
ok 1045 - stage badge names the future scheduled date with no open prerequisite
  ---
  duration_ms: 2.026528
  ...
# Subtest: stage badge reads blocked with nothing waiting and no schedule
ok 1046 - stage badge reads blocked with nothing waiting and no schedule
  ---
  duration_ms: 1.27865
  ...
# Subtest: stage vault batch with a stale row refuses and reopens
ok 1047 - stage vault batch with a stale row refuses and reopens
  ---
  duration_ms: 8.412597
  ...
# Subtest: stage opening builds 200/400/1000-task notes without cubic growth
ok 1048 - stage opening builds 200/400/1000-task notes without cubic growth
  ---
  duration_ms: 36.607228
  ...
# Subtest: stage snapshots match standalone parsing across grammar vectors
ok 1049 - stage snapshots match standalone parsing across grammar vectors
  ---
  duration_ms: 4.597155
  ...
# Subtest: stage Warm-empty cache is ready without a vault fallback
ok 1050 - stage Warm-empty cache is ready without a vault fallback
  ---
  duration_ms: 0.47675
  ...
# Subtest: stage opening renders cross-note results with zero writes and cap
ok 1051 - stage opening renders cross-note results with zero writes and cap
  ---
  duration_ms: 41.224943
  ...
# Subtest: stage CURRENT covers same-note, cross-note, blocked, and counted parents
ok 1052 - stage CURRENT covers same-note, cross-note, blocked, and counted parents
  ---
  duration_ms: 1.892834
  ...
# Subtest: stage collections reuse one snapshot per parent
ok 1053 - stage collections reuse one snapshot per parent
  ---
  duration_ms: 0.478894
  ...
# Subtest: stage cold refresh yields, preserves state, and performs no search reads
ok 1054 - stage cold refresh yields, preserves state, and performs no search reads
  ---
  duration_ms: 119.765909
  ...
# Subtest: stage cold refresh abandons after dismissal or replacement
ok 1055 - stage cold refresh abandons after dismissal or replacement
  ---
  duration_ms: 51.965765
  ...
# Subtest: stage 400-task opening finishes in a child process before the parent timeout
ok 1056 - stage 400-task opening finishes in a child process before the parent timeout
  ---
  duration_ms: 104.058665
  ...
# Subtest: stage ranker passes the DK contract vectors verbatim
ok 1057 - stage ranker passes the DK contract vectors verbatim
  ---
  duration_ms: 2.983024
  ...
# Subtest: stage ranker tiers match the capture ranker tier order
ok 1058 - stage ranker tiers match the capture ranker tier order
  ---
  duration_ms: 0.409802
  ...
# Subtest: stage pool excludes daily notes, done, templates, and dot-dirs
ok 1059 - stage pool excludes daily notes, done, templates, and dot-dirs
  ---
  duration_ms: 0.387119
  ...
# Subtest: stage pool collects open vault tasks with buffers as given
ok 1060 - stage pool collects open vault tasks with buffers as given
  ---
  duration_ms: 2.815485
  ...
# Subtest: stage CURRENT resolves same-note, missing, closed, and non-task targets
ok 1061 - stage CURRENT resolves same-note, missing, closed, and non-task targets
  ---
  duration_ms: 2.656361
  ...
# Subtest: stage cycle guard reports the path back to the dependent
ok 1062 - stage cycle guard reports the path back to the dependent
  ---
  duration_ms: 0.867747
  ...
# Subtest: stage view groups CURRENT, RESULTS, and BLOCKED with guards
ok 1063 - stage view groups CURRENT, RESULTS, and BLOCKED with guards
  ---
  duration_ms: 2.917148
  ...
# Subtest: stage view disables cycles and unencodable targets, keeps +id rows
ok 1064 - stage view disables cycles and unencodable targets, keeps +id rows
  ---
  duration_ms: 1.323907
  ...
# Subtest: stage cache tasks normalize across Tasks shapes, buffers win
ok 1065 - stage cache tasks normalize across Tasks shapes, buffers win
  ---
  duration_ms: 0.94297
  ...
# Subtest: stage Task Link mode shows Depends on for one link and batches
ok 1066 - stage Task Link mode shows Depends on for one link and batches
  ---
  duration_ms: 1.087406
  ...
# Subtest: stage mark keys never collide across notes
ok 1067 - stage mark keys never collide across notes
  ---
  duration_ms: 0.243815
  ...
# Subtest: stage display-text locating matches one open task
ok 1068 - stage display-text locating matches one open task
  ---
  duration_ms: 0.324519
  ...
# Subtest: stage selection refusal spans tasks only
ok 1069 - stage selection refusal spans tasks only
  ---
  duration_ms: 0.290505
  ...
# Subtest: stage builder composes pool, current, guards, and pill title
ok 1070 - stage builder composes pool, current, guards, and pill title
  ---
  duration_ms: 2.151047
  ...
# Subtest: stage counted vault add with a stale target refuses and reopens
ok 1071 - stage counted vault add with a stale target refuses and reopens
  ---
  duration_ms: 9.286307
  ...
# Subtest: stage vault commit with a stale write notifies once and reopens
ok 1072 - stage vault commit with a stale write notifies once and reopens
  ---
  duration_ms: 5.026475
  ...
# Subtest: commitVaultRefs refuses a cycle through implicit resident edges
ok 1073 - commitVaultRefs refuses a cycle through implicit resident edges
  ---
  duration_ms: 1.721586
  ...
# Subtest: stage single remove with a stale write notifies once and reopens
ok 1074 - stage single remove with a stale write notifies once and reopens
  ---
  duration_ms: 2.190672
  ...
# Subtest: stage vault single +id guard refuses a stale target
ok 1075 - stage vault single +id guard refuses a stale target
  ---
  duration_ms: 1.170995
  ...
# Subtest: stage vault counted +id guard refuses a stale target
ok 1076 - stage vault counted +id guard refuses a stale target
  ---
  duration_ms: 0.778406
  ...
# Subtest: stage single +id guard refuses a stale target
ok 1077 - stage single +id guard refuses a stale target
  ---
  duration_ms: 0.746465
  ...
# Subtest: stage counted remove with a stale write refuses and reopens
ok 1078 - stage counted remove with a stale write refuses and reopens
  ---
  duration_ms: 2.130887
  ...
# Subtest: stage counted remove counts only changed sources
ok 1079 - stage counted remove counts only changed sources
  ---
  duration_ms: 2.542003
  ...
# Subtest: counted local add on [?] sources reads zero extra notes
ok 1080 - counted local add on [?] sources reads zero extra notes
  ---
  duration_ms: 3.363851
  ...
# Subtest: counted local toggle-off on a Pomodoro-linked [?] source recovers
ok 1081 - counted local toggle-off on a Pomodoro-linked [?] source recovers
  ---
  duration_ms: 4.486585
  ...
# Subtest: stage counted vault add counts only changed sources
ok 1082 - stage counted vault add counts only changed sources
  ---
  duration_ms: 3.57819
  ...
# Subtest: stage counted vault remove counts only changed sources
ok 1083 - stage counted vault remove counts only changed sources
  ---
  duration_ms: 1.375726
  ...
# Subtest: stage +id row prompts without writing
ok 1084 - stage +id row prompts without writing
  ---
  duration_ms: 8.720667
  ...
# Subtest: stage dismissal writes no bytes and drops the batch
ok 1085 - stage dismissal writes no bytes and drops the batch
  ---
  duration_ms: 1.240508
  ...
# Subtest: stage same-note batch commits in one undo group
ok 1086 - stage same-note batch commits in one undo group
  ---
  duration_ms: 6.908907
  ...
# Subtest: stage batch with a stale row refuses and reopens
ok 1087 - stage batch with a stale row refuses and reopens
  ---
  duration_ms: 0.955012
  ...
# Subtest: stage counted add applies to every source task
ok 1088 - stage counted add applies to every source task
  ---
  duration_ms: 32.946542
  ...
# Subtest: stage batch cycle rows stay guarded and write nothing
ok 1089 - stage batch cycle rows stay guarded and write nothing
  ---
  duration_ms: 29.591467
  ...
# Subtest: stage edit-task-dependencies registers with no default hotkey
ok 1090 - stage edit-task-dependencies registers with no default hotkey
  ---
  duration_ms: 1.873587
  ...
# Subtest: stage waits-on badge counts open prerequisites only
ok 1091 - stage waits-on badge counts open prerequisites only
  ---
  duration_ms: 2.506114
  ...
# Subtest: stage cycle tooltip shows task descriptions
ok 1092 - stage cycle tooltip shows task descriptions
  ---
  duration_ms: 2.764658
  ...
# Subtest: cross-note add awaits preparation before the one commit
ok 1093 - cross-note add awaits preparation before the one commit
  ---
  duration_ms: 14.719377
  ...
# Subtest: a failed async preparation leaves the dependent untouched
ok 1094 - a failed async preparation leaves the dependent untouched
  ---
  duration_ms: 5.95641
  ...
# Subtest: links to unloaded notes tolerate add, remove, and deleted targets
ok 1095 - links to unloaded notes tolerate add, remove, and deleted targets
  ---
  duration_ms: 3.9338
  ...
# Subtest: Pomodoro-linked dependents recover through the plugin vault read
ok 1096 - Pomodoro-linked dependents recover through the plugin vault read
  ---
  duration_ms: 4.897588
  ...
# Subtest: same-note batch +id stamps the target and links in one undo group
ok 1097 - same-note batch +id stamps the target and links in one undo group
  ---
  duration_ms: 6.571564
  ...
# Subtest: confirmBatchBlockId collects the id and executes the batch
ok 1098 - confirmBatchBlockId collects the id and executes the batch
  ---
  duration_ms: 1.565218
  ...
# Subtest: commitMarkedDependencies executes ready additions at once
ok 1099 - commitMarkedDependencies executes ready additions at once
  ---
  duration_ms: 1.441492
  ...
# Subtest: counted vault add links two siblings bottom-up
ok 1100 - counted vault add links two siblings bottom-up
  ---
  duration_ms: 2.339836
  ...
# Subtest: counted CURRENT rows without a line remove from every source
ok 1101 - counted CURRENT rows without a line remove from every source
  ---
  duration_ms: 6.835959
  ...
# Subtest: a stale editor between await and commit refuses
ok 1102 - a stale editor between await and commit refuses
  ---
  duration_ms: 1.587641
  ...
# Subtest: removeDependencyByRef refuses targets that are not on the line
ok 1103 - removeDependencyByRef refuses targets that are not on the line
  ---
  duration_ms: 1.185994
  ...
# Subtest: kept unloaded links resolve the field id by line position
ok 1104 - kept unloaded links resolve the field id by line position
  ---
  duration_ms: 2.308537
  ...
# Subtest: pendingTargetLine commits the same-note target id with the link
ok 1105 - pendingTargetLine commits the same-note target id with the link
  ---
  duration_ms: 1.676219
  ...
# Subtest: counted vault add commits every source in one transaction
ok 1106 - counted vault add commits every source in one transaction
  ---
  duration_ms: 2.20061
  ...
# Subtest: field-only clears snapshot the vault and recover
ok 1107 - field-only clears snapshot the vault and recover
  ---
  duration_ms: 3.207442
  ...
# Subtest: adds without recovery read zero extra vault notes
ok 1108 - adds without recovery read zero extra vault notes
  ---
  duration_ms: 0.644631
  ...
# Subtest: hand-edit clear recovers Pomodoro-linked dependents to Next
ok 1109 - hand-edit clear recovers Pomodoro-linked dependents to Next
  ---
  duration_ms: 1.055374
  ...
# Subtest: hand-edit clear on a non-Blocked parent reads zero extra notes
ok 1110 - hand-edit clear on a non-Blocked parent reads zero extra notes
  ---
  duration_ms: 0.442926
  ...
# Subtest: writer keeps the full route for duplicate basenames
ok 1111 - writer keeps the full route for duplicate basenames
  ---
  duration_ms: 0.518701
  ...
# Subtest: adds on Blocked parents and non-Blocked mirror touches read nothing
ok 1112 - adds on Blocked parents and non-Blocked mirror touches read nothing
  ---
  duration_ms: 0.731807
  ...
# Subtest: counted vault add loads each source's existing links
ok 1113 - counted vault add loads each source's existing links
  ---
  duration_ms: 1.853748
  ...
# Subtest: counted Ctrl+D on a blockquoted task refuses with the blockquote notice
ok 1114 - counted Ctrl+D on a blockquoted task refuses with the blockquote notice
  ---
  duration_ms: 0.520283
  ...
# Subtest: single Ctrl+D on a quoted task without a field refuses as a blockquote
ok 1115 - single Ctrl+D on a quoted task without a field refuses as a blockquote
  ---
  duration_ms: 0.190113
  ...
# Subtest: confirmSingleBlockId folds the target id into one transaction
ok 1116 - confirmSingleBlockId folds the target id into one transaction
  ---
  duration_ms: 1.348153
  ...
# Subtest: chooseTaskDependency folds a missing target id into one transaction
ok 1117 - chooseTaskDependency folds a missing target id into one transaction
  ---
  duration_ms: 1.150316
  ...
# Subtest: counted remove commits every source in one transaction
ok 1118 - counted remove commits every source in one transaction
  ---
  duration_ms: 2.226361
  ...
# Subtest: DP parse vectors accept, empty, malformed, and not-a-line
ok 1119 - DP parse vectors accept, empty, malformed, and not-a-line
  ---
  duration_ms: 3.302013
  ...
# Subtest: DP30 attributes a Work-Log-nested Depends-On line to the inner task
ok 1120 - DP30 attributes a Work-Log-nested Depends-On line to the inner task
  ---
  duration_ms: 2.623458
  ...
# Subtest: fenced lines never collect as Depends-On lines
ok 1121 - fenced lines never collect as Depends-On lines
  ---
  duration_ms: 0.399142
  ...
# Subtest: DW1 creates the line as the first child
ok 1122 - DW1 creates the line as the first child
  ---
  duration_ms: 4.469322
  ...
# Subtest: DW2 creates the line after a Cancel Log
ok 1123 - DW2 creates the line after a Cancel Log
  ---
  duration_ms: 0.989499
  ...
# Subtest: DW3-DW5 append, remove the middle, and delete on the last link
ok 1124 - DW3-DW5 append, remove the middle, and delete on the last link
  ---
  duration_ms: 3.864456
  ...
# Subtest: DW6-DW7 re-add moves to the end and the field mirrors the line
ok 1125 - DW6-DW7 re-add moves to the end and the field mirrors the line
  ---
  duration_ms: 0.720585
  ...
# Subtest: DW8 tab parents deepen the child by one tab
ok 1126 - DW8 tab parents deepen the child by one tab
  ---
  duration_ms: 0.99516
  ...
# Subtest: DW9 space parents reuse the existing child indent
ok 1127 - DW9 space parents reuse the existing child indent
  ---
  duration_ms: 0.786862
  ...
# Subtest: DW10-DW11 CRLF and final-newline state survive
ok 1128 - DW10-DW11 CRLF and final-newline state survive
  ---
  duration_ms: 0.878187
  ...
# Subtest: DW12-DW14 link form is the shortest unambiguous form
ok 1129 - DW12-DW14 link form is the shortest unambiguous form
  ---
  duration_ms: 0.273312
  ...
# Subtest: archive targets keep the explicit done/ path form
ok 1130 - archive targets keep the explicit done/ path form
  ---
  duration_ms: 0.202216
  ...
# Subtest: DW15 an existing id is never rewritten
ok 1131 - DW15 an existing id is never rewritten
  ---
  duration_ms: 0.324881
  ...
# Subtest: DW16 an unencodable path without an id refuses
ok 1132 - DW16 an unencodable path without an id refuses
  ---
  duration_ms: 0.28832
  ...
# Subtest: DW17 field placement follows fresh and precedes the block id
ok 1133 - DW17 field placement follows fresh and precedes the block id
  ---
  duration_ms: 0.259215
  ...
# Subtest: DW18 legacy children fold into the line
ok 1134 - DW18 legacy children fold into the line
  ---
  duration_ms: 0.689175
  ...
# Subtest: DW19 variants canonicalise to the writer form
ok 1135 - DW19 variants canonicalise to the writer form
  ---
  duration_ms: 1.175344
  ...
# Subtest: adding an open prerequisite blocks the dependent
ok 1136 - adding an open prerequisite blocks the dependent
  ---
  duration_ms: 0.303079
  ...
# Subtest: adding transfers Next and In Progress commitment to the open target
ok 1137 - adding transfers Next and In Progress commitment to the open target
  ---
  duration_ms: 0.712851
  ...
# Subtest: removing the last open prerequisite recovers immediately
ok 1138 - removing the last open prerequisite recovers immediately
  ---
  duration_ms: 0.656412
  ...
# Subtest: removal stays Blocked while another prerequisite is open
ok 1139 - removal stays Blocked while another prerequisite is open
  ---
  duration_ms: 0.302939
  ...
# Subtest: removal stays Blocked with a future schedule
ok 1140 - removal stays Blocked with a future schedule
  ---
  duration_ms: 0.261449
  ...
# Subtest: one gesture commits the dependent note in a single transaction
ok 1141 - one gesture commits the dependent note in a single transaction
  ---
  duration_ms: 0.735644
  ...
# Subtest: a failed preparation leaves the dependent untouched
ok 1142 - a failed preparation leaves the dependent untouched
  ---
  duration_ms: 0.329288
  ...
# Subtest: recovery references follow the line plus covered legacy children
ok 1143 - recovery references follow the line plus covered legacy children
  ---
  duration_ms: 0.414772
  ...
# Subtest: task-block helpers find owners, lines, and insertion points
ok 1144 - task-block helpers find owners, lines, and insertion points
  ---
  duration_ms: 0.307287
  ...
# Subtest: dependency notices follow the contract shapes
ok 1145 - dependency notices follow the contract shapes
  ---
  duration_ms: 0.129447
  ...
# Subtest: nav api v3 resolves results and never throws
ok 1146 - nav api v3 resolves results and never throws
  ---
  duration_ms: 0.782994
  ...
# Subtest: getDependencyInsertLine lands after a Cancel Log subtree
ok 1147 - getDependencyInsertLine lands after a Cancel Log subtree
  ---
  duration_ms: 0.216944
  ...
# Subtest: missing ledger-tools api refuses the review namespace
ok 1148 - missing ledger-tools api refuses the review namespace
  ---
  duration_ms: 1.637005
  ...
# Subtest: review jump on an empty queue
ok 1149 - review jump on an empty queue
  ---
  duration_ms: 1.025427
  ...
# Subtest: review jump from a queued task goes to the neighbor
ok 1150 - review jump from a queued task goes to the neighbor
  ---
  duration_ms: 0.662475
  ...
# Subtest: review jump wraps at the ends
ok 1151 - review jump wraps at the ends
  ---
  duration_ms: 0.281477
  ...
# Subtest: review jump from elsewhere goes to the first or last entry
ok 1152 - review jump from elsewhere goes to the first or last entry
  ---
  duration_ms: 0.187348
  ...
# Subtest: review jump matches a moved cursor task by text
ok 1153 - review jump matches a moved cursor task by text
  ---
  duration_ms: 0.153323
  ...
# Subtest: review jump from a just-stamped rank goes to the entry after it
ok 1154 - review jump from a just-stamped rank goes to the entry after it
  ---
  duration_ms: 0.273952
  ...
# Subtest: review jump skips just-stamped keys the lagging cache still shows
ok 1155 - review jump skips just-stamped keys the lagging cache still shows
  ---
  duration_ms: 0.153894
  ...
# Subtest: review jump after stamping everything reports empty or wraps
ok 1156 - review jump after stamping everything reports empty or wraps
  ---
  duration_ms: 0.50341
  ...
# Subtest: review queue line resolves at the entry line
ok 1157 - review queue line resolves at the entry line
  ---
  duration_ms: 0.588644
  ...
# Subtest: review queue line follows a moved line to its unique match
ok 1158 - review queue line follows a moved line to its unique match
  ---
  duration_ms: 0.406235
  ...
# Subtest: review queue line goes stale on duplicates or a missing line
ok 1159 - review queue line goes stale on duplicates or a missing line
  ---
  duration_ms: 0.2306
  ...
# Subtest: review jump notices name the state
ok 1160 - review jump notices name the state
  ---
  duration_ms: 0.436914
  ...
# Subtest: fresh stamp targets refuse closed and recurring tasks
ok 1161 - fresh stamp targets refuse closed and recurring tasks
  ---
  duration_ms: 0.658998
  ...
# Subtest: fresh stamp batch stamps every target and nothing else
ok 1162 - fresh stamp batch stamps every target and nothing else
  ---
  duration_ms: 0.326563
  ...
# Subtest: one refusal refuses the whole fresh stamp batch
ok 1163 - one refusal refuses the whole fresh stamp batch
  ---
  duration_ms: 0.292218
  ...
# Subtest: a throwing stamper refuses the fresh stamp batch
ok 1164 - a throwing stamper refuses the fresh stamp batch
  ---
  duration_ms: 0.149906
  ...
# Subtest: fresh stamp plus Work Log prepends only stamped Pending targets
ok 1165 - fresh stamp plus Work Log prepends only stamped Pending targets
  ---
  duration_ms: 1.09506
  ...
# Subtest: blank Work Log summary and stamp refusal never create a log marker
ok 1166 - blank Work Log summary and stamp refusal never create a log marker
  ---
  duration_ms: 0.226543
  ...
# Subtest: fresh stamp notices adjust the pre-write counts
ok 1167 - fresh stamp notices adjust the pre-write counts
  ---
  duration_ms: 0.190855
  ...
# Subtest: today detection only matches today's fresh field
ok 1168 - today detection only matches today's fresh field
  ---
  duration_ms: 0.200633
  ...
# Subtest: stamped refs match the pre-write queue by line or text
ok 1169 - stamped refs match the pre-write queue by line or text
  ---
  duration_ms: 0.342514
  ...
# Subtest: review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
ok 1170 - review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
  ---
  duration_ms: 0.259866
  ...
# Subtest: tier-aware jump notices name each tier
ok 1171 - tier-aware jump notices name each tier
  ---
  duration_ms: 0.608782
  ...
# Subtest: projects tier walks with commitment rank and empty-project notice
ok 1172 - projects tier walks with commitment rank and empty-project notice
  ---
  duration_ms: 0.22571
  ...
# Subtest: references tier walks with commitment rank and reference notice
ok 1173 - references tier walks with commitment rank and reference notice
  ---
  duration_ms: 0.457713
  ...
# Subtest: jump notices use reviewEntryView when provided and keep the fallback
ok 1174 - jump notices use reviewEntryView when provided and keep the fallback
  ---
  duration_ms: 0.265837
  ...
# Subtest: tier notices fall back without tier ranks and wrap on the last line
ok 1175 - tier notices fall back without tier ranks and wrap on the last line
  ---
  duration_ms: 0.152502
  ...
# Subtest: boundary notice names commitments done and rotten next
ok 1176 - boundary notice names commitments done and rotten next
  ---
  duration_ms: 0.123757
  ...
# Subtest: walk anchor records handled keys with their neighbors
ok 1177 - walk anchor records handled keys with their neighbors
  ---
  duration_ms: 0.478844
  ...
# Subtest: cursor on a live entry wins over a lagging anchor
ok 1178 - cursor on a live entry wins over a lagging anchor
  ---
  duration_ms: 0.270557
  ...
# Subtest: [s after a stamp goes backwards from the anchor
ok 1179 - [s after a stamp goes backwards from the anchor
  ---
  duration_ms: 0.457434
  ...
# Subtest: release-then-]s continues from the anchor successor
ok 1180 - release-then-]s continues from the anchor successor
  ---
  duration_ms: 0.202527
  ...
# Subtest: non-contiguous counted stamp advances past the last handled rank
ok 1181 - non-contiguous counted stamp advances past the last handled rank
  ---
  duration_ms: 0.296977
  ...
# Subtest: anchor wraps at both ends
ok 1182 - anchor wraps at both ends
  ---
  duration_ms: 0.315913
  ...
# Subtest: advance across NEXT to TICKLER to ROTTEN lands the boundary
ok 1183 - advance across NEXT to TICKLER to ROTTEN lands the boundary
  ---
  duration_ms: 0.388772
  ...
# Subtest: tier capability gates on the freshness namespace version
ok 1184 - tier capability gates on the freshness namespace version
  ---
  duration_ms: 0.126942
  ...
# Subtest: empty queue notice reads the upkeep meter
ok 1185 - empty queue notice reads the upkeep meter
  ---
  duration_ms: 0.126091
  ...
# Subtest: refresh row reads lane intervals from the api with the once-Ready return
ok 1186 - refresh row reads lane intervals from the api with the once-Ready return
  ---
  duration_ms: 1.127473
  ...
# Subtest: endpoint jumps select the queue ends with full rank and total
ok 1187 - endpoint jumps select the queue ends with full rank and total
  ---
  duration_ms: 0.366881
  ...
# Subtest: endpoint jumps ignore cursor, anchor, and direction
ok 1188 - endpoint jumps ignore cursor, anchor, and direction
  ---
  duration_ms: 0.269835
  ...
# Subtest: endpoint jumps on empty and one-entry queues
ok 1189 - endpoint jumps on empty and one-entry queues
  ---
  duration_ms: 0.257171
  ...
# Subtest: a visited endpoint is still due under its own anchor
ok 1190 - a visited endpoint is still due under its own anchor
  ---
  duration_ms: 0.209309
  ...
# Subtest: lowercase steps continue from an endpoint anchor
ok 1191 - lowercase steps continue from an endpoint anchor
  ---
  duration_ms: 0.297608
  ...
# Subtest: counted review jump repeat 1 matches omitted repeat
ok 1192 - counted review jump repeat 1 matches omitted repeat
  ---
  duration_ms: 0.553878
  ...
# Subtest: counted review jump from the first entry lands N steps ahead
ok 1193 - counted review jump from the first entry lands N steps ahead
  ---
  duration_ms: 0.231953
  ...
# Subtest: counted review jump from the last entry wraps past the start
ok 1194 - counted review jump from the last entry wraps past the start
  ---
  duration_ms: 0.150989
  ...
# Subtest: counted review jump larger than the queue wraps once
ok 1195 - counted review jump larger than the queue wraps once
  ---
  duration_ms: 0.138885
  ...
# Subtest: counted review jump on a one-entry queue stays there
ok 1196 - counted review jump on a one-entry queue stays there
  ---
  duration_ms: 0.139316
  ...
# Subtest: counted review jump with no origin lands on the Nth entry
ok 1197 - counted review jump with no origin lands on the Nth entry
  ---
  duration_ms: 0.140158
  ...
# Subtest: counted review jump from a shaped anchor takes N surviving successors
ok 1198 - counted review jump from a shaped anchor takes N surviving successors
  ---
  duration_ms: 0.188831
  ...
# Subtest: counted review jump does not change endpoint selection
ok 1199 - counted review jump does not change endpoint selection
  ---
  duration_ms: 0.127633
  ...
# Subtest: a stamped endpoint that moved is stale and cannot land from old text
ok 1200 - a stamped endpoint that moved is stale and cannot land from old text
  ---
  duration_ms: 0.177328
  ...
# Subtest: stale endpoint target reselects the same endpoint in the new queue
ok 1201 - stale endpoint target reselects the same endpoint in the new queue
  ---
  duration_ms: 1.443225
  ...
# Subtest: endpoint retry is bounded and failures preserve the anchor
ok 1202 - endpoint retry is bounded and failures preserve the anchor
  ---
  duration_ms: 0.522727
  ...
# Subtest: endpoint jump to ROTTEN carries no boundary preamble
ok 1203 - endpoint jump to ROTTEN carries no boundary preamble
  ---
  duration_ms: 0.732769
  ...
# Subtest: endpoint notices keep v4 tier details and legacy v3 text
ok 1204 - endpoint notices keep v4 tier details and legacy v3 text
  ---
  duration_ms: 0.175735
  ...
# Subtest: onload registers first/last commands routed to the shared jump
ok 1205 - onload registers first/last commands routed to the shared jump
  ---
  duration_ms: 1.379945
  ...
# Subtest: jumpToDueTask consumes a pending Vim prefix as N review steps
ok 1206 - jumpToDueTask consumes a pending Vim prefix as N review steps
  ---
  duration_ms: 0.850574
  ...
# Subtest: registered next-due-task callback reads the pending Vim prefix
ok 1207 - registered next-due-task callback reads the pending Vim prefix
  ---
  duration_ms: 0.735173
  ...
# Subtest: explicit jumpToDueTask repeat skips the Vim prefix
ok 1208 - explicit jumpToDueTask repeat skips the Vim prefix
  ---
  duration_ms: 0.294362
  ...
# Subtest: non-normal editor with a pending prefix still jumps one entry
ok 1209 - non-normal editor with a pending prefix still jumps one entry
  ---
  duration_ms: 0.257491
  ...
# Subtest: stale counted replan reuses the captured repeat
ok 1210 - stale counted replan reuses the captured repeat
  ---
  duration_ms: 0.305052
  ...
# Subtest: endpoint jump with a pending prefix still lands on the endpoint
ok 1211 - endpoint jump with a pending prefix still lands on the endpoint
  ---
  duration_ms: 0.242242
  ...
# Subtest: counted forward landing on ROTTEN keeps the boundary preamble
ok 1212 - counted forward landing on ROTTEN keeps the boundary preamble
  ---
  duration_ms: 0.462923
  ...
# Subtest: PRE and POST are machine tiers; PRE is a commitment
ok 1213 - PRE and POST are machine tiers; PRE is a commitment
  ---
  duration_ms: 0.213418
  ...
# Subtest: fallback notices name PRE checklist and POST closeout
ok 1214 - fallback notices name PRE checklist and POST closeout
  ---
  duration_ms: 0.245479
  ...
# Subtest: text-first cursor matching does not skip Pills after an above-insert
ok 1215 - text-first cursor matching does not skip Pills after an above-insert
  ---
  duration_ms: 0.145789
  ...
# Subtest: day-scoped anchors from another day are ignored
ok 1216 - day-scoped anchors from another day are ignored
  ---
  duration_ms: 0.227514
  ...
# Subtest: boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
ok 1217 - boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
  ---
  duration_ms: 0.200744
  ...
# Subtest: ]S reaches POST with 77 ROTTEN rows and a null budget
ok 1218 - ]S reaches POST with 77 ROTTEN rows and a null budget
  ---
  duration_ms: 0.524181
  ...
# Subtest: nav normalizes a legacy v7 returned tier to tickler
ok 1219 - nav normalizes a legacy v7 returned tier to tickler
  ---
  duration_ms: 0.108276
  ...
# Subtest: RECURRING is a machine tier, a commitment, and a v9 capability
ok 1220 - RECURRING is a machine tier, a commitment, and a v9 capability
  ---
  duration_ms: 0.14122
  ...
# Subtest: RECURRING counts in reviewWalkRemaining and gates the boundary
ok 1221 - RECURRING counts in reviewWalkRemaining and gates the boundary
  ---
  duration_ms: 0.149906
  ...
# Subtest: matchReviewRecurringCursor is text-first like the checklist matcher
ok 1222 - matchReviewRecurringCursor is text-first like the checklist matcher
  ---
  duration_ms: 0.169633
  ...
# Subtest: fallback notices name RECURRING due detail with the reschedule hint
ok 1223 - fallback notices name RECURRING due detail with the reschedule hint
  ---
  duration_ms: 0.138284
  ...
# Subtest: Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
ok 1224 - Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
  ---
  duration_ms: 0.133234
  ...
# Subtest: bobLineDigest matches the shared bob-cli vectors
ok 1225 - bobLineDigest matches the shared bob-cli vectors
  ---
  duration_ms: 4.793251
  ...
# Subtest: parseGoToTaskParams accepts a complete v1 link and ignores extra keys
ok 1226 - parseGoToTaskParams accepts a complete v1 link and ignores extra keys
  ---
  duration_ms: 0.829694
  ...
# Subtest: parseGoToTaskParams treats ref and block as optional
ok 1227 - parseGoToTaskParams treats ref and block as optional
  ---
  duration_ms: 0.138354
  ...
# Subtest: parseGoToTaskParams rejects each malformed field
ok 1228 - parseGoToTaskParams rejects each malformed field
  ---
  duration_ms: 0.237213
  ...
# Subtest: vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
ok 1229 - vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
  ---
  duration_ms: 0.280676
  ...
# Subtest: refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
ok 1230 - refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
  ---
  duration_ms: 1.29451
  ...
# Subtest: handleGoToTaskUri notices each malformed parameter
ok 1231 - handleGoToTaskUri notices each malformed parameter
  ---
  duration_ms: 1.11052
  ...
# Subtest: handleGoToTaskUri notices a path outside the vault
ok 1232 - handleGoToTaskUri notices a path outside the vault
  ---
  duration_ms: 0.420853
  ...
# Subtest: handleGoToTaskUri notices a missing file inside the vault
ok 1233 - handleGoToTaskUri notices a missing file inside the vault
  ---
  duration_ms: 0.475919
  ...
# Subtest: handleGoToTaskUri maps a trailing-slash vault base
ok 1234 - handleGoToTaskUri maps a trailing-slash vault base
  ---
  duration_ms: 1.631444
  ...
# Subtest: handleGoToTaskUri prefers the open buffer over cachedRead
ok 1235 - handleGoToTaskUri prefers the open buffer over cachedRead
  ---
  duration_ms: 0.819384
  ...
# Subtest: handleGoToTaskUri re-finds by block id after an insert above the task
ok 1236 - handleGoToTaskUri re-finds by block id after an insert above the task
  ---
  duration_ms: 0.440951
  ...
# Subtest: handleGoToTaskUri re-finds a unique digest after a shift with no block
ok 1237 - handleGoToTaskUri re-finds a unique digest after a shift with no block
  ---
  duration_ms: 0.480027
  ...
# Subtest: handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
ok 1238 - handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
  ---
  duration_ms: 0.433467
  ...
# Subtest: handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
ok 1239 - handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
  ---
  duration_ms: 0.45597
  ...
# Subtest: handleGoToTaskUri reuses a leaf that already shows the note
ok 1240 - handleGoToTaskUri reuses a leaf that already shows the note
  ---
  duration_ms: 0.596298
  ...
# Subtest: handleGoToTaskUri switches a Reading-view leaf to editing
ok 1241 - handleGoToTaskUri switches a Reading-view leaf to editing
  ---
  duration_ms: 0.91708
  ...
# Subtest: handleGoToTaskUri records a jump from the prior cursor and none without one
ok 1242 - handleGoToTaskUri records a jump from the prior cursor and none without one
  ---
  duration_ms: 1.186825
  ...
# Subtest: handleGoToTaskUri never writes the vault or advances the walk
ok 1243 - handleGoToTaskUri never writes the vault or advances the walk
  ---
  duration_ms: 0.462823
  ...
# Subtest: handleGoToTaskUri reports when the note cannot be opened
ok 1244 - handleGoToTaskUri reports when the note cannot be opened
  ---
  duration_ms: 0.313368
  ...
# Subtest: focusTaskMoveDestination still lands without switching Reading view
ok 1245 - focusTaskMoveDestination still lands without switching Reading view
  ---
  duration_ms: 0.412508
  ...
# Subtest: onload registers bob-goto-task when the protocol API exists
ok 1246 - onload registers bob-goto-task when the protocol API exists
  ---
  duration_ms: 0.994308
  ...
# Subtest: onload skips protocol registration when the API is missing
ok 1247 - onload skips protocol registration when the API is missing
  ---
  duration_ms: 0.315563
  ...
# Subtest: registered protocol handler forwards params to handleGoToTaskUri
ok 1248 - registered protocol handler forwards params to handleGoToTaskUri
  ---
  duration_ms: 0.305163
  ...
# Subtest: handleGoToTaskUri maps a path through realpath when prefixes differ
ok 1249 - handleGoToTaskUri maps a path through realpath when prefixes differ
  ---
  duration_ms: 2.378491
  ...
# Subtest: cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
ok 1250 - cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
  ---
  duration_ms: 2.846223
  ...
# Subtest: findCancelLogParent finds a direct child but ignores a grandchild
ok 1251 - findCancelLogParent finds a direct child but ignores a grandchild
  ---
  duration_ms: 0.893916
  ...
# Subtest: getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
ok 1252 - getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
  ---
  duration_ms: 0.275266
  ...
# Subtest: formatCancelLogEntryText renders the exact preview text
ok 1253 - formatCancelLogEntryText renders the exact preview text
  ---
  duration_ms: 0.210271
  ...
# Subtest: planCancelLogEntry inserts a first-child log with tabs or spaces
ok 1254 - planCancelLogEntry inserts a first-child log with tabs or spaces
  ---
  duration_ms: 0.927621
  ...
# Subtest: planCancelLogEntry prepends under an existing log wherever it sits
ok 1255 - planCancelLogEntry prepends under an existing log wherever it sits
  ---
  duration_ms: 0.389704
  ...
# Subtest: planCancelLogEntry uses the fallback only when a marker exists
ok 1256 - planCancelLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.472381
  ...
# Subtest: isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
ok 1257 - isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
  ---
  duration_ms: 0.432075
  ...
# Subtest: describeCancelTaskRow covers single, counted, link, recurring, and hidden
ok 1258 - describeCancelTaskRow covers single, counted, link, recurring, and hidden
  ---
  duration_ms: 2.605853
  ...
# Subtest: planTaskCancelBatch cancels a single task with a first-child log
ok 1259 - planTaskCancelBatch cancels a single task with a first-child log
  ---
  duration_ms: 2.021629
  ...
# Subtest: planTaskCancelBatch upserts cancelled before the block id and preserves fields
ok 1260 - planTaskCancelBatch upserts cancelled before the block id and preserves fields
  ---
  duration_ms: 0.643047
  ...
# Subtest: planTaskCancelBatch records id-field task identities
ok 1261 - planTaskCancelBatch records id-field task identities
  ---
  duration_ms: 0.317647
  ...
# Subtest: planTaskCancelBatch skips closed targets and stays bottom-up
ok 1262 - planTaskCancelBatch skips closed targets and stays bottom-up
  ---
  duration_ms: 0.535032
  ...
# Subtest: planTaskCancelBatch refuses recurring targets in all three syntaxes
ok 1263 - planTaskCancelBatch refuses recurring targets in all three syntaxes
  ---
  duration_ms: 0.592171
  ...
# Subtest: planTaskCancelBatch handles empty reasons and stale preimages
ok 1264 - planTaskCancelBatch handles empty reasons and stale preimages
  ---
  duration_ms: 0.52401
  ...
# Subtest: planTaskCancelBatch preserves CRLF line endings
ok 1265 - planTaskCancelBatch preserves CRLF line endings
  ---
  duration_ms: 0.355208
  ...
# Subtest: cancel project conversion carries the log and reports it
ok 1266 - cancel project conversion carries the log and reports it
  ---
  duration_ms: 4.126787
  ...
# Subtest: getCancelTaskRowTitle names single, counted, and link sessions
ok 1267 - getCancelTaskRowTitle names single, counted, and link sessions
  ---
  duration_ms: 1.066376
  ...
# Subtest: getCancelReasonHints labels Enter per state and Esc as Keep open
ok 1268 - getCancelReasonHints labels Enter per state and Esc as Keep open
  ---
  duration_ms: 0.825575
  ...
# Subtest: the Cancel property item and the card's cancel row describe an open task
ok 1269 - the Cancel property item and the card's cancel row describe an open task
  ---
  duration_ms: 10.153121
  ...
# Subtest: Cancel row hides on closed tasks, plain bullets, and all-closed sessions
ok 1270 - Cancel row hides on closed tasks, plain bullets, and all-closed sessions
  ---
  duration_ms: 5.407171
  ...
# Subtest: Cancel row reports skipped closed targets in a counted session
ok 1271 - Cancel row reports skipped closed targets in a counted session
  ---
  duration_ms: 1.284492
  ...
# Subtest: the card refuses the cancel row on a recurring task and stays on the card
ok 1272 - the card refuses the cancel row on a recurring task and stays on the card
  ---
  duration_ms: 1.795518
  ...
# Subtest: cancel reason stage previews the typed, empty, fallback, and :: cases
ok 1273 - cancel reason stage previews the typed, empty, fallback, and :: cases
  ---
  duration_ms: 2.57754
  ...
# Subtest: cancel reason footer flips between plain, log, and fallback labels
ok 1274 - cancel reason footer flips between plain, log, and fallback labels
  ---
  duration_ms: 0.840043
  ...
# Subtest: Esc from the cancel reason stage writes nothing
ok 1275 - Esc from the cancel reason stage writes nothing
  ---
  duration_ms: 2.237612
  ...
# Subtest: single cancel writes [-], stamp, and first-child log in one transaction
ok 1276 - single cancel writes [-], stamp, and first-child log in one transaction
  ---
  duration_ms: 4.077674
  ...
# Subtest: empty reason writes no log unless one already exists
ok 1277 - empty reason writes no log unless one already exists
  ---
  duration_ms: 3.974467
  ...
# Subtest: stale single preimage refuses with nothing written
ok 1278 - stale single preimage refuses with nothing written
  ---
  duration_ms: 1.421264
  ...
# Subtest: cancel writes [-] with no NOW chip
ok 1279 - cancel writes [-] with no NOW chip
  ---
  duration_ms: 1.235559
  ...
# Subtest: TSC recovery runs with cancelled identities; a missing API still succeeds
ok 1280 - TSC recovery runs with cancelled identities; a missing API still succeeds
  ---
  duration_ms: 4.732523
  ...
# Subtest: a throwing TSC API is skipped silently with no chip
ok 1281 - a throwing TSC API is skipped silently with no chip
  ---
  duration_ms: 1.475637
  ...
# Subtest: counted cancel skips closed targets and reports them
ok 1282 - counted cancel skips closed targets and reports them
  ---
  duration_ms: 2.055644
  ...
# Subtest: same-file cancel folds today's Pomodoro prune into one transaction
ok 1283 - same-file cancel folds today's Pomodoro prune into one transaction
  ---
  duration_ms: 3.674154
  ...
# Subtest: link session cancels the target and removes the invoking link bullet
ok 1284 - link session cancels the target and removes the invoking link bullet
  ---
  duration_ms: 7.448509
  ...
# Subtest: buildCancelNoticeModel text covers every chip
ok 1285 - buildCancelNoticeModel text covers every chip
  ---
  duration_ms: 0.34556
  ...
# Subtest: renderCancelNoticeFragment builds the is-cancel card
ok 1286 - renderCancelNoticeFragment builds the is-cancel card
  ---
  duration_ms: 0.845914
  ...
# Subtest: isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
ok 1287 - isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
  ---
  duration_ms: 1.439889
  ...
# Subtest: findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
ok 1288 - findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
  ---
  duration_ms: 1.695737
  ...
# Subtest: collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
ok 1289 - collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
  ---
  duration_ms: 0.636294
  ...
# Subtest: planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
ok 1290 - planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
  ---
  duration_ms: 1.239286
  ...
# Subtest: planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
ok 1291 - planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
  ---
  duration_ms: 0.679847
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
ok 1292 - planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
  ---
  duration_ms: 0.777474
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
ok 1293 - planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
  ---
  duration_ms: 0.706489
  ...
# Subtest: planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
ok 1294 - planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
  ---
  duration_ms: 0.297558
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
ok 1295 - planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
  ---
  duration_ms: 0.794346
  ...
# Subtest: planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
ok 1296 - planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
  ---
  duration_ms: 1.002954
  ...
# Subtest: planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
ok 1297 - planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
  ---
  duration_ms: 0.742707
  ...
# Subtest: planDeferredPomodoroLinkCleanup preserves CRLF line endings
ok 1298 - planDeferredPomodoroLinkCleanup preserves CRLF line endings
  ---
  duration_ms: 0.3563
  ...
# Subtest: deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
ok 1299 - deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
  ---
  duration_ms: 0.399993
  ...
# Subtest: counted dependencies converge mixed sources and maintain one link per parent
ok 1300 - counted dependencies converge mixed sources and maintain one link per parent
  ---
  duration_ms: 12.630069
  ...
# Subtest: counted and single dependency gestures refuse inside a blockquote (DP29)
ok 1301 - counted and single dependency gestures refuse inside a blockquote (DP29)
  ---
  duration_ms: 0.542565
  ...
# Subtest: counted dependency candidates exclude every source and expose mixed state
ok 1302 - counted dependency candidates exclude every source and expose mixed state
  ---
  duration_ms: 1.164903
  ...
# Subtest: counted dependency block-ID prompting is planned atomically
ok 1303 - counted dependency block-ID prompting is planned atomically
  ---
  duration_ms: 2.387227
  ...
# Subtest: counted dependency runtime applies target, parents, and navigation in one undo group
ok 1304 - counted dependency runtime applies target, parents, and navigation in one undo group
  ---
  duration_ms: 3.829491
  ...
# Subtest: counted Depends-on removal recovers residents with [unblocked::]
ok 1305 - counted Depends-on removal recovers residents with [unblocked::]
  ---
  duration_ms: 5.858894
  ...
# Subtest: counted Depends-on removal writes [unblocked::] through the wired freshness API
ok 1306 - counted Depends-on removal writes [unblocked::] through the wired freshness API
  ---
  duration_ms: 3.927688
  ...
# Subtest: cross-file toggle changes only the source link
ok 1307 - cross-file toggle changes only the source link
  ---
  duration_ms: 1.282197
  ...
# Subtest: cross-file write failure still toggles only the source link
ok 1308 - cross-file write failure still toggles only the source link
  ---
  duration_ms: 0.600295
  ...
# Subtest: line-local fallback applies bottom-up and preserves CRLF
ok 1309 - line-local fallback applies bottom-up and preserves CRLF
  ---
  duration_ms: 0.793545
  ...
# Subtest: source line-count invariant rejects embedded newline changes
ok 1310 - source line-count invariant rejects embedded newline changes
  ---
  duration_ms: 0.218157
  ...
# Subtest: pure toggle refuses when the source changed under it
ok 1311 - pure toggle refuses when the source changed under it
  ---
  duration_ms: 0.182789
  ...
# Subtest: counted transclusion toggle evaluates each line independently
ok 1312 - counted transclusion toggle evaluates each line independently
  ---
  duration_ms: 0.34575
  ...
# Subtest: transclusion toggle is refused on Depends-On lines
ok 1313 - transclusion toggle is refused on Depends-On lines
  ---
  duration_ms: 0.48179
  ...
# Subtest: legacy sole-link children toggle purely, without field or status writes
ok 1314 - legacy sole-link children toggle purely, without field or status writes
  ---
  duration_ms: 0.402027
  ...
# Subtest: Ctrl+D on the Depends on row clears the line, field, and legacy children
ok 1315 - Ctrl+D on the Depends on row clears the line, field, and legacy children
  ---
  duration_ms: 2.742956
  ...
# Subtest: Ctrl+D clears a field-only dependency without a line
ok 1316 - Ctrl+D clears a field-only dependency without a line
  ---
  duration_ms: 0.815687
  ...
# Subtest: counted Ctrl+D on the Depends on row clears every targeted task
ok 1317 - counted Ctrl+D on the Depends on row clears every targeted task
  ---
  duration_ms: 2.012121
  ...
# Subtest: findRemovedLineText reports deleted lines
ok 1318 - findRemovedLineText reports deleted lines
  ---
  duration_ms: 0.168171
  ...
# Subtest: hand-edit mirror projects an edited line into the field
ok 1319 - hand-edit mirror projects an edited line into the field
  ---
  duration_ms: 1.025467
  ...
# Subtest: hand-edit mirror canonicalises a hand-written line variant
ok 1320 - hand-edit mirror canonicalises a hand-written line variant
  ---
  duration_ms: 0.468915
  ...
# Subtest: hand-edit mirror drops a linkless line and the field
ok 1321 - hand-edit mirror drops a linkless line and the field
  ---
  duration_ms: 0.813713
  ...
# Subtest: hand-edit mirror clears the field after the line is deleted
ok 1322 - hand-edit mirror clears the field after the line is deleted
  ---
  duration_ms: 0.617338
  ...
# Subtest: hand-edit mirror leaves malformed lines alone
ok 1323 - hand-edit mirror leaves malformed lines alone
  ---
  duration_ms: 0.306304
  ...
# Subtest: hand-edit mirror leaves legacy-only children for the hooks
ok 1324 - hand-edit mirror leaves legacy-only children for the hooks
  ---
  duration_ms: 0.561061
  ...
# Subtest: hand-edit mirror blocks when an open prerequisite is added by hand
ok 1325 - hand-edit mirror blocks when an open prerequisite is added by hand
  ---
  duration_ms: 0.854882
  ...
# Subtest: hand-edit mirror never transfers commitment to the target
ok 1326 - hand-edit mirror never transfers commitment to the target
  ---
  duration_ms: 0.818683
  ...
# Subtest: hand-edit mirror recovers when the last open prerequisite is removed by hand
ok 1327 - hand-edit mirror recovers when the last open prerequisite is removed by hand
  ---
  duration_ms: 2.049072
  ...
# Subtest: hand-edit mirror leaves a half-typed link alone
ok 1328 - hand-edit mirror leaves a half-typed link alone
  ---
  duration_ms: 0.330892
  ...
# Subtest: hand-edit mirror clears the owning task when its last-child line is deleted
ok 1329 - hand-edit mirror clears the owning task when its last-child line is deleted
  ---
  duration_ms: 0.760452
  ...
# Subtest: mirror scheduler debounces at the contract interval
ok 1330 - mirror scheduler debounces at the contract interval
  ---
  duration_ms: 1.385785
  ...
# Subtest: mirror scheduler seeds the baseline from the update start state
ok 1331 - mirror scheduler seeds the baseline from the update start state
  ---
  duration_ms: 2.516053
  ...
# Subtest: mirror scheduler keeps the first baseline and maps the owner across a burst
ok 1332 - mirror scheduler keeps the first baseline and maps the owner across a burst
  ---
  duration_ms: 0.782513
  ...
# Subtest: mirror listener runs clear-field for a first-edit deletion with a following sibling
ok 1333 - mirror listener runs clear-field for a first-edit deletion with a following sibling
  ---
  duration_ms: 8.069434
  ...
# Subtest: mirror fire re-arms while the cursor stays on the edited line
ok 1334 - mirror fire re-arms while the cursor stays on the edited line
  ---
  duration_ms: 5.311137
  ...
# Subtest: mirror scheduler reads changed ranges from the CM6 update
ok 1335 - mirror scheduler reads changed ranges from the CM6 update
  ---
  duration_ms: 0.33527
  ...
# Subtest: mirror scheduler skips IME composition
ok 1336 - mirror scheduler skips IME composition
  ---
  duration_ms: 0.237443
  ...
# Subtest: mirror scheduler skips open modals
ok 1337 - mirror scheduler skips open modals
  ---
  duration_ms: 0.192227
  ...
# Subtest: counted Ctrl+D clears every targeted task in one transaction with one notice
ok 1338 - counted Ctrl+D clears every targeted task in one transaction with one notice
  ---
  duration_ms: 4.53652
  ...
# Subtest: counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
ok 1339 - counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
  ---
  duration_ms: 1.317315
  ...
# Subtest: counted N! on only a Depends-On line refuses without writing
ok 1340 - counted N! on only a Depends-On line refuses without writing
  ---
  duration_ms: 0.235019
  ...
# Subtest: promotion targets enumerate real tasks and assign stable IDs
ok 1341 - promotion targets enumerate real tasks and assign stable IDs
  ---
  duration_ms: 5.358239
  ...
# Subtest: promotion file planner expands live links and preserves history
ok 1342 - promotion file planner expands live links and preserves history
  ---
  duration_ms: 3.947335
  ...
# Subtest: promotion file planner handles forms, whitespace, and subtrees
ok 1343 - promotion file planner handles forms, whitespace, and subtrees
  ---
  duration_ms: 1.113015
  ...
# Subtest: promotion file planner keeps compatibility for non-live references
ok 1344 - promotion file planner keeps compatibility for non-live references
  ---
  duration_ms: 0.854582
  ...
# Subtest: forward promotion expands live links, persists anchors, and removes the source
ok 1345 - forward promotion expands live links, persists anchors, and removes the source
  ---
  duration_ms: 6.829766
  ...
# Subtest: forward promotion uses zero-task fallback and keeps reverse one-to-one
ok 1346 - forward promotion uses zero-task fallback and keeps reverse one-to-one
  ---
  duration_ms: 1.144364
  ...
# Subtest: forward promotion retains the source on ambiguous, stale, and write failures
ok 1347 - forward promotion retains the source on ambiguous, stale, and write failures
  ---
  duration_ms: 1.342884
  ...
# Subtest: forward promotion discovers live links without a backlink cache and uses one open-editor write
ok 1348 - forward promotion discovers live links without a backlink cache and uses one open-editor write
  ---
  duration_ms: 1.400253
  ...
# Subtest: forward conversion carries a Depends-On line and reverse restores it
ok 1349 - forward conversion carries a Depends-On line and reverse restores it
  ---
  duration_ms: 14.347096
  ...
# Subtest: planTaskLaneBatch commits every Ready target to Next
ok 1350 - planTaskLaneBatch commits every Ready target to Next
  ---
  duration_ms: 3.146106
  ...
# Subtest: planTaskLaneBatch releases Next and In Progress to Ready
ok 1351 - planTaskLaneBatch releases Next and In Progress to Ready
  ---
  duration_ms: 0.48733
  ...
# Subtest: planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
ok 1352 - planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
  ---
  duration_ms: 0.823502
  ...
# Subtest: planTaskLaneBatch skips Blocked and refuses stale preimages
ok 1353 - planTaskLaneBatch skips Blocked and refuses stale preimages
  ---
  duration_ms: 0.297077
  ...
# Subtest: buildLaneToggleNotice reports commit and release with and without budgets
ok 1354 - buildLaneToggleNotice reports commit and release with and without budgets
  ---
  duration_ms: 0.421745
  ...
# Subtest: describeLaneRow covers task, counted, and link sessions
ok 1355 - describeLaneRow covers task, counted, and link sessions
  ---
  duration_ms: 0.52382
  ...
# Subtest: toggleTaskLane commits Ready to Next and reports lane budgets
ok 1356 - toggleTaskLane commits Ready to Next and reports lane budgets
  ---
  duration_ms: 2.259113
  ...
# Subtest: toggleTaskLane releases to Ready without the api
ok 1357 - toggleTaskLane releases to Ready without the api
  ---
  duration_ms: 1.163341
  ...
# Subtest: toggleTaskLane release logs the summary on In Progress tasks
ok 1358 - toggleTaskLane release logs the summary on In Progress tasks
  ---
  duration_ms: 0.883306
  ...
# Subtest: toggleTaskLane skips Blocked targets
ok 1359 - toggleTaskLane skips Blocked targets
  ---
  duration_ms: 0.780881
  ...
# Subtest: counted toggleTaskLane covers the current task plus the next N tasks
ok 1360 - counted toggleTaskLane covers the current task plus the next N tasks
  ---
  duration_ms: 0.477151
  ...
# Subtest: toggleTaskLane on a Task Link writes through the open buffer
ok 1361 - toggleTaskLane on a Task Link writes through the open buffer
  ---
  duration_ms: 3.205719
  ...
# Subtest: toggleTaskLane on Task Links releases across notes
ok 1362 - toggleTaskLane on Task Links releases across notes
  ---
  duration_ms: 1.080332
  ...
# Subtest: toggleTaskLane refuses when a preimage changed
ok 1363 - toggleTaskLane refuses when a preimage changed
  ---
  duration_ms: 0.164374
  ...
# Subtest: Ctrl+Shift+P shows a pinned lane row that commits immediately
ok 1364 - Ctrl+Shift+P shows a pinned lane row that commits immediately
  ---
  duration_ms: 11.12224
  ...
# Subtest: Ctrl+Shift+P link mode shows the lane row with release detail
ok 1365 - Ctrl+Shift+P link mode shows the lane row with release detail
  ---
  duration_ms: 4.444134
  ...
# Subtest: Ctrl+Shift+P lane release with In Progress goes through the reason stage
ok 1366 - Ctrl+Shift+P lane release with In Progress goes through the reason stage
  ---
  duration_ms: 2.973356
  ...
# Subtest: getLinkPickerSessionSubtitle keeps the clamp for a single link
ok 1367 - getLinkPickerSessionSubtitle keeps the clamp for a single link
  ---
  duration_ms: 0.160066
  ...
# Subtest: link-mode priority notice keeps via Task Links visible
ok 1368 - link-mode priority notice keeps via Task Links visible
  ---
  duration_ms: 0.963149
  ...
# Subtest: already-handled Alt+N leaves Vim state alone
ok 1369 - already-handled Alt+N leaves Vim state alone
  ---
  duration_ms: 0.43962
  ...
# Subtest: Alt+N fallback still dispatches once with the Vim count
ok 1370 - Alt+N fallback still dispatches once with the Vim count
  ---
  duration_ms: 0.880701
  ...
# Subtest: parseLinkPickerTaskLink recognizes dedicated Task Link bullets
ok 1371 - parseLinkPickerTaskLink recognizes dedicated Task Link bullets
  ---
  duration_ms: 2.559286
  ...
# Subtest: discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
ok 1372 - discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
  ---
  duration_ms: 1.294611
  ...
# Subtest: discoverLinkPickerTargets leaves \#task lines to the regular picker
ok 1373 - discoverLinkPickerTargets leaves \#task lines to the regular picker
  ---
  duration_ms: 0.342193
  ...
# Subtest: findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
ok 1374 - findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
  ---
  duration_ms: 0.547204
  ...
# Subtest: createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
ok 1375 - createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
  ---
  duration_ms: 2.12141
  ...
# Subtest: getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
ok 1376 - getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
  ---
  duration_ms: 0.682072
  ...
# Subtest: bare link mode edits the task behind a Task Link through the open buffer
ok 1377 - bare link mode edits the task behind a Task Link through the open buffer
  ---
  duration_ms: 19.173019
  ...
# Subtest: counted link mode writes across notes through both the open buffer and the vault
ok 1378 - counted link mode writes across notes through both the open buffer and the vault
  ---
  duration_ms: 5.733134
  ...
# Subtest: Task Link scheduled delete recovers a Blocked task through the wired freshness API
ok 1379 - Task Link scheduled delete recovers a Blocked task through the wired freshness API
  ---
  duration_ms: 7.291349
  ...
# Subtest: link mode refuses the whole operation when a linked note changed
ok 1380 - link mode refuses the whole operation when a linked note changed
  ---
  duration_ms: 3.89761
  ...
# Subtest: link mode reports a closed target and changes nothing
ok 1381 - link mode reports a closed target and changes nothing
  ---
  duration_ms: 1.560859
  ...
# Subtest: link mode defers to a future date, blocks the task, and prunes today
ok 1382 - link mode defers to a future date, blocks the task, and prunes today
  ---
  duration_ms: 9.873267
  ...
# Subtest: bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
ok 1383 - bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
  ---
  duration_ms: 4.099565
  ...
# Subtest: dash restore suppresses editor notice after deliberate navigation
ok 1384 - dash restore suppresses editor notice after deliberate navigation
  ---
  duration_ms: 22.900353
  ...
# Subtest: open-task dispatch timeout is registered for plugin cleanup
ok 1385 - open-task dispatch timeout is registered for plugin cleanup
  ---
  duration_ms: 0.575128
  ...
# Subtest: jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
ok 1386 - jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
  ---
  duration_ms: 4.953205
  ...
# Subtest: jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
ok 1387 - jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
  ---
  duration_ms: 1.307225
  ...
# Subtest: jumpToOpenObsidianTask keeps current-swap transaction failures local
ok 1388 - jumpToOpenObsidianTask keeps current-swap transaction failures local
  ---
  duration_ms: 0.751394
  ...
# Subtest: jumpToOpenObsidianTask refuses current-up without jumping or mutating
ok 1389 - jumpToOpenObsidianTask refuses current-up without jumping or mutating
  ---
  duration_ms: 0.622959
  ...
# Subtest: jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
ok 1390 - jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
  ---
  duration_ms: 2.202234
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
ok 1391 - Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
  ---
  duration_ms: 0.752276
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
ok 1392 - Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
  ---
  duration_ms: 0.913685
  ...
# Subtest: counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
ok 1393 - counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
  ---
  duration_ms: 1.693203
  ...
# Subtest: an impossible counted Pomodoro move refuses without jumping or mutating
ok 1394 - an impossible counted Pomodoro move refuses without jumping or mutating
  ---
  duration_ms: 0.589576
  ...
# Subtest: counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
ok 1395 - counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
  ---
  duration_ms: 0.843831
  ...
# Subtest: counted open-task jump on a sole current target keeps the existing notice
ok 1396 - counted open-task jump on a sole current target keeps the existing notice
  ---
  duration_ms: 0.239017
  ...
# Subtest: dispatch guard allows exactly one counted Pomodoro move when the command route also fires
ok 1397 - dispatch guard allows exactly one counted Pomodoro move when the command route also fires
  ---
  duration_ms: 0.908424
  ...
# Subtest: bullet property picker reconciles duplicate bare and counted opens
ok 1398 - bullet property picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 14.45393
  ...
# Subtest: bullet property picker close lifecycle clears tracking for fresh sessions
ok 1399 - bullet property picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 7.415365
  ...
# Subtest: task move picker reconciles duplicate bare and counted opens
ok 1400 - task move picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 3.324596
  ...
# Subtest: task move picker close lifecycle clears tracking for fresh sessions
ok 1401 - task move picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 1.276888
  ...
# Subtest: Pomodoro bullet move picker opens sessions and clears the shared move picker slot
ok 1402 - Pomodoro bullet move picker opens sessions and clears the shared move picker slot
  ---
  duration_ms: 3.494421
  ...
# Subtest: Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
ok 1403 - Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
  ---
  duration_ms: 0.912221
  ...
# Subtest: move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
ok 1404 - move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
  ---
  duration_ms: 1.603891
  ...
# Subtest: commitPomodoroBulletMoveSession applies one guarded same-file transaction
ok 1405 - commitPomodoroBulletMoveSession applies one guarded same-file transaction
  ---
  duration_ms: 1.849171
  ...
# Subtest: Pomodoro bullet move picker confirms = through the actual picker callback
ok 1406 - Pomodoro bullet move picker confirms = through the actual picker callback
  ---
  duration_ms: 1.05301
  ...
# Subtest: Pomodoro bullet move picker reserves =NAME for peeling a named merged component
ok 1407 - Pomodoro bullet move picker reserves =NAME for peeling a named merged component
  ---
  duration_ms: 1.077036
  ...
# Subtest: Pomodoro bullet move picker confirms =email through the actual picker callback
ok 1408 - Pomodoro bullet move picker confirms =email through the actual picker callback
  ---
  duration_ms: 1.623038
  ...
# Subtest: Pomodoro bullet move picker confirms = review through the actual picker callback
ok 1409 - Pomodoro bullet move picker confirms = review through the actual picker callback
  ---
  duration_ms: 0.929784
  ...
# Subtest: Pomodoro bullet move picker confirms =focus by unnaming a single-name source
ok 1410 - Pomodoro bullet move picker confirms =focus by unnaming a single-name source
  ---
  duration_ms: 0.931117
  ...
# Subtest: Pomodoro bullet split stale-content guard does not write
ok 1411 - Pomodoro bullet split stale-content guard does not write
  ---
  duration_ms: 0.412186
  ...
# Subtest: Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
ok 1412 - Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
  ---
  duration_ms: 7.078703
  ...
# Subtest: native isOpen regression: pickers attach, close clears slot, reopen works
ok 1413 - native isOpen regression: pickers attach, close clears slot, reopen works
  ---
  duration_ms: 2.572651
  ...
# Subtest: stale registered pickers fail open on the next key
ok 1414 - stale registered pickers fail open on the next key
  ---
  duration_ms: 1.957055
  ...
# Subtest: planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
ok 1415 - planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
  ---
  duration_ms: 4.685024
  ...
# Subtest: planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
ok 1416 - planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
  ---
  duration_ms: 0.825926
  ...
# Subtest: planPomodoroBulletMove preserves the source when only some siblings move out
ok 1417 - planPomodoroBulletMove preserves the source when only some siblings move out
  ---
  duration_ms: 0.404983
  ...
# Subtest: planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
ok 1418 - planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
  ---
  duration_ms: 0.431935
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
ok 1419 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
  ---
  duration_ms: 0.711919
  ...
# Subtest: planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
ok 1420 - planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
  ---
  duration_ms: 1.121941
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
ok 1421 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
  ---
  duration_ms: 0.459667
  ...
# Subtest: planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
ok 1422 - planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
  ---
  duration_ms: 0.2986
  ...
# Subtest: planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
ok 1423 - planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
  ---
  duration_ms: 0.497359
  ...
# Subtest: planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
ok 1424 - planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
  ---
  duration_ms: 0.941497
  ...
# Subtest: planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
ok 1425 - planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
  ---
  duration_ms: 0.391878
  ...
# Subtest: planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
ok 1426 - planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
  ---
  duration_ms: 0.244687
  ...
# Subtest: planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
ok 1427 - planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
  ---
  duration_ms: 0.413039
  ...
# Subtest: planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
ok 1428 - planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
  ---
  duration_ms: 0.387289
  ...
# Subtest: planPomodoroBulletMove deletes both open and closed source entries the same way
ok 1429 - planPomodoroBulletMove deletes both open and closed source entries the same way
  ---
  duration_ms: 0.410273
  ...
# Subtest: planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
ok 1430 - planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
  ---
  duration_ms: 0.311985
  ...
# Subtest: planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
ok 1431 - planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
  ---
  duration_ms: 0.378161
  ...
# Subtest: planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
ok 1432 - planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
  ---
  duration_ms: 0.554649
  ...
# Subtest: planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
ok 1433 - planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
  ---
  duration_ms: 0.316985
  ...
# Subtest: planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
ok 1434 - planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
  ---
  duration_ms: 0.454818
  ...
# Subtest: planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
ok 1435 - planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
  ---
  duration_ms: 0.322827
  ...
# Subtest: planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
ok 1436 - planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
  ---
  duration_ms: 0.321533
  ...
# Subtest: planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
ok 1437 - planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
  ---
  duration_ms: 0.341702
  ...
# Subtest: planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
ok 1438 - planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
  ---
  duration_ms: 0.38246
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
ok 1439 - planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
  ---
  duration_ms: 0.203238
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
ok 1440 - planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
  ---
  duration_ms: 0.43983
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
ok 1441 - planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
  ---
  duration_ms: 3.240395
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
ok 1442 - planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
  ---
  duration_ms: 0.519442
  ...
# Subtest: Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
ok 1443 - Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
  ---
  duration_ms: 8.244708
  ...
# Subtest: commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
ok 1444 - commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
  ---
  duration_ms: 3.603269
  ...
# Subtest: commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
ok 1445 - commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
  ---
  duration_ms: 1.248654
  ...
# Subtest: commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
ok 1446 - commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
  ---
  duration_ms: 0.712961
  ...
# Subtest: commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
ok 1447 - commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
  ---
  duration_ms: 0.516486
  ...
# Subtest: Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
ok 1448 - Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
  ---
  duration_ms: 9.657686
  ...
# Subtest: Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
ok 1449 - Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
  ---
  duration_ms: 1.1056
  ...
# Subtest: Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
ok 1450 - Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
  ---
  duration_ms: 1.117433
  ...
# Subtest: Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
ok 1451 - Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
  ---
  duration_ms: 1.693312
  ...
# Subtest: task move picker closes before commit while other pickers retain delayed close
ok 1452 - task move picker closes before commit while other pickers retain delayed close
  ---
  duration_ms: 1.276668
  ...
# Subtest: parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
ok 1453 - parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
  ---
  duration_ms: 1.968438
  ...
# Subtest: normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
ok 1454 - normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
  ---
  duration_ms: 0.379444
  ...
# Subtest: formatPomodoroEntryLine emits a placeholder entry with or without a name
ok 1455 - formatPomodoroEntryLine emits a placeholder entry with or without a name
  ---
  duration_ms: 0.136049
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
ok 1456 - createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
  ---
  duration_ms: 2.020738
  ...
# Subtest: createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
ok 1457 - createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
  ---
  duration_ms: 0.794997
  ...
# Subtest: createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
ok 1458 - createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
  ---
  duration_ms: 0.660892
  ...
# Subtest: createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
ok 1459 - createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
  ---
  duration_ms: 0.593263
  ...
# Subtest: buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
ok 1460 - buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
  ---
  duration_ms: 0.238937
  ...
# Subtest: buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
ok 1461 - buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
  ---
  duration_ms: 0.370497
  ...
# Subtest: createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
ok 1462 - createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
  ---
  duration_ms: 0.662014
  ...
# Subtest: createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
ok 1463 - createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
  ---
  duration_ms: 0.329959
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
ok 1464 - createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
  ---
  duration_ms: 0.351631
  ...
# Subtest: collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
ok 1465 - collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
  ---
  duration_ms: 0.441122
  ...
# Subtest: findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
ok 1466 - findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
  ---
  duration_ms: 0.510094
  ...
# Subtest: findPomodoroBulletContext leaves plain \#task lines on the task-move route
ok 1467 - findPomodoroBulletContext leaves plain \#task lines on the task-move route
  ---
  duration_ms: 0.332415
  ...
# Subtest: discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
ok 1468 - discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
  ---
  duration_ms: 0.810687
  ...
# Subtest: findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
ok 1469 - findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
  ---
  duration_ms: 0.735233
  ...
# Subtest: discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
ok 1470 - discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
  ---
  duration_ms: 0.95317
  ...
# Subtest: isMovablePomodoroEntryContext matches open current and future Pomodoro entries
ok 1471 - isMovablePomodoroEntryContext matches open current and future Pomodoro entries
  ---
  duration_ms: 3.041506
  ...
# Subtest: planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
ok 1472 - planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
  ---
  duration_ms: 0.767205
  ...
# Subtest: planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
ok 1473 - planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
  ---
  duration_ms: 0.313919
  ...
# Subtest: planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
ok 1474 - planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
  ---
  duration_ms: 0.367893
  ...
# Subtest: planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
ok 1475 - planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
  ---
  duration_ms: 0.397038
  ...
# Subtest: planPomodoroEntryReorder handles counted current swaps and their inverses
ok 1476 - planPomodoroEntryReorder handles counted current swaps and their inverses
  ---
  duration_ms: 0.423819
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
ok 1477 - planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
  ---
  duration_ms: 0.213417
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
ok 1478 - planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
  ---
  duration_ms: 0.194291
  ...
# Subtest: planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
ok 1479 - planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
  ---
  duration_ms: 0.511667
  ...
# Subtest: planPomodoroEntryReorder round-trips a future-up swap across the current open entry
ok 1480 - planPomodoroEntryReorder round-trips a future-up swap across the current open entry
  ---
  duration_ms: 0.528599
  ...
# Subtest: planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
ok 1481 - planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
  ---
  duration_ms: 0.517468
  ...
# Subtest: planPomodoroEntryReorder refuses moving down past the last placeholder in the section
ok 1482 - planPomodoroEntryReorder refuses moving down past the last placeholder in the section
  ---
  duration_ms: 0.177379
  ...
# Subtest: planPomodoroEntryReorder refuses both directions for a lone placeholder
ok 1483 - planPomodoroEntryReorder refuses both directions for a lone placeholder
  ---
  duration_ms: 0.161518
  ...
# Subtest: planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
ok 1484 - planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
  ---
  duration_ms: 0.150607
  ...
# Subtest: planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
ok 1485 - planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
  ---
  duration_ms: 0.249827
  ...
# Subtest: planPomodoroEntryReorder refuses illegal current/future spans atomically
ok 1486 - planPomodoroEntryReorder refuses illegal current/future spans atomically
  ---
  duration_ms: 0.479696
  ...
# Subtest: planPomodoroEntryReorder rejects a stale source line
ok 1487 - planPomodoroEntryReorder rejects a stale source line
  ---
  duration_ms: 0.180345
  ...
# Subtest: planPomodoroEntryReorder round-trips CRLF content
ok 1488 - planPomodoroEntryReorder round-trips CRLF content
  ---
  duration_ms: 0.266078
  ...
# Subtest: planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
ok 1489 - planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
  ---
  duration_ms: 0.197828
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
ok 1490 - planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
  ---
  duration_ms: 0.28277
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up three positions and round-trips
ok 1491 - planPomodoroEntryReorder moves a placeholder up three positions and round-trips
  ---
  duration_ms: 0.611758
  ...
# Subtest: planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
ok 1492 - planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
  ---
  duration_ms: 0.206063
  ...
# Subtest: planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
ok 1493 - planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
  ---
  duration_ms: 0.546904
  ...
# Subtest: planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
ok 1494 - planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
  ---
  duration_ms: 0.723832
  ...
# Subtest: planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
ok 1495 - planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
  ---
  duration_ms: 0.308479
  ...
# Subtest: peelPomodoroMergedName removes every matching canonical plus component
ok 1496 - peelPomodoroMergedName removes every matching canonical plus component
  ---
  duration_ms: 1.6286
  ...
# Subtest: planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
ok 1497 - planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
  ---
  duration_ms: 3.537552
  ...
# Subtest: planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
ok 1498 - planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
  ---
  duration_ms: 0.543227
  ...
# Subtest: planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
ok 1499 - planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
  ---
  duration_ms: 0.656884
  ...
# Subtest: planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
ok 1500 - planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
  ---
  duration_ms: 0.767435
  ...
# Subtest: planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
ok 1501 - planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
  ---
  duration_ms: 1.158241
  ...
# Subtest: planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
ok 1502 - planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
  ---
  duration_ms: 0.713091
  ...
# Subtest: planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
ok 1503 - planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
  ---
  duration_ms: 1.222965
  ...
# Subtest: Pomodoro bullet move picker typing =NAME or Escape does not write
ok 1504 - Pomodoro bullet move picker typing =NAME or Escape does not write
  ---
  duration_ms: 2.148402
  ...
# Subtest: planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
ok 1505 - planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
  ---
  duration_ms: 0.47128
  ...
# Subtest: planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
ok 1506 - planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
  ---
  duration_ms: 0.242823
  ...
# Subtest: planPomodoroEntryRename reports unchanged when the normalized name matches the current name
ok 1507 - planPomodoroEntryRename reports unchanged when the normalized name matches the current name
  ---
  duration_ms: 0.124958
  ...
# Subtest: planPomodoroEntryRename rejects unsupported trailing content and a stale source line
ok 1508 - planPomodoroEntryRename rejects unsupported trailing content and a stale source line
  ---
  duration_ms: 0.136621
  ...
# Subtest: planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
ok 1509 - planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
  ---
  duration_ms: 0.147081
  ...
# Subtest: planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
ok 1510 - planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
  ---
  duration_ms: 1.515933
  ...
# Subtest: planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
ok 1511 - planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
  ---
  duration_ms: 1.030377
  ...
# Subtest: planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
ok 1512 - planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
  ---
  duration_ms: 0.498361
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: priority notice relative day helpers handle offsets ranges and icons
ok 1513 - priority notice relative day helpers handle offsets ranges and icons
  ---
  duration_ms: 1.519822
  ...
# Subtest: priority notice model summarizes single counted and project writes
ok 1514 - priority notice model summarizes single counted and project writes
  ---
  duration_ms: 3.608868
  ...
# Subtest: priority notice renderer builds an accessible fragment
ok 1515 - priority notice renderer builds an accessible fragment
  ---
  duration_ms: 2.192094
  ...
# Subtest: priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
ok 1516 - priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
  ---
  duration_ms: 10.614882
  ...
# Subtest: priority notice falls back to one plain notice without a DOM
ok 1517 - priority notice falls back to one plain notice without a DOM
  ---
  duration_ms: 0.626396
  ...
# Subtest: priority notice falls back to plain text when fragment rendering fails
ok 1518 - priority notice falls back to plain text when fragment rendering fails
  ---
  duration_ms: 0.419671
  ...
# Subtest: priority scheduling rolls inclusively and clamps a random value of one
ok 1519 - priority scheduling rolls inclusively and clamps a random value of one
  ---
  duration_ms: 0.617189
  ...
# Subtest: priority value rows preserve config order and expose labels ranges and current state
ok 1520 - priority value rows preserve config order and expose labels ranges and current state
  ---
  duration_ms: 0.921218
  ...
# Subtest: priority picker writes priority then rolled schedule in one guarded edit
ok 1521 - priority picker writes priority then rolled schedule in one guarded edit
  ---
  duration_ms: 14.721851
  ...
# Subtest: priority picker writes lowest priority with a wide rolled schedule
ok 1522 - priority picker writes lowest priority with a wide rolled schedule
  ---
  duration_ms: 2.665508
  ...
# Subtest: priority picker replaces both existing values without duplicating fields
ok 1523 - priority picker replaces both existing values without duplicating fields
  ---
  duration_ms: 2.90206
  ...
# Subtest: counted priority writes keep the rolled date right of the priority
ok 1524 - counted priority writes keep the rolled date right of the priority
  ---
  duration_ms: 4.8827
  ...
# Subtest: priority picker writes project priority and schedule inline atomically
ok 1525 - priority picker writes project priority and schedule inline atomically
  ---
  duration_ms: 5.134261
  ...
# Subtest: counted priority picker rolls an independent schedule for every task
ok 1526 - counted priority picker rolls an independent schedule for every task
  ---
  duration_ms: 2.770428
  ...
# Subtest: counted priority planning keeps project schedules inline
ok 1527 - counted priority planning keeps project schedules inline
  ---
  duration_ms: 1.1688
  ...
# Subtest: counted priority planning evaluates Blocked recovery per rolled date
ok 1528 - counted priority planning evaluates Blocked recovery per rolled date
  ---
  duration_ms: 1.34658
  ...
# Subtest: a counted priority batch writes one entry per task using each task's own previous level
ok 1529 - a counted priority batch writes one entry per task using each task's own previous level
  ---
  duration_ms: 0.993326
  ...
# Subtest: priority notice models carry the stored level value for the glyph
ok 1530 - priority notice models carry the stored level value for the glyph
  ---
  duration_ms: 0.467713
  ...
# Subtest: ledger priority mark lookup guards version and render
ok 1531 - ledger priority mark lookup guards version and render
  ---
  duration_ms: 0.181467
  ...
# Subtest: priority notice header reuses the shared mark when available
ok 1532 - priority notice header reuses the shared mark when available
  ---
  duration_ms: 0.404012
  ...
# Subtest: priority notice keeps the Lucide icon without a usable mark api
ok 1533 - priority notice keeps the Lucide icon without a usable mark api
  ---
  duration_ms: 1.291254
  ...
# Subtest: a counted priority batch skips a task whose rolled date equals its current date
ok 1534 - a counted priority batch skips a task whose rolled date equals its current date
  ---
  duration_ms: 5.764684
  ...
# Subtest: counted priority runtime aborts a stale session without rolling writes
ok 1535 - counted priority runtime aborts a stale session without rolling writes
  ---
  duration_ms: 2.456119
  ...
# Subtest: scheduled picker pins a priority roll only for configured current priorities
ok 1536 - scheduled picker pins a priority roll only for configured current priorities
  ---
  duration_ms: 18.673005
  ...
# Subtest: Ctrl+R replaces only the pinned priority roll and keeps it selected
ok 1537 - Ctrl+R replaces only the pinned priority roll and keeps it selected
  ---
  duration_ms: 7.096585
  ...
# Subtest: choosing a priority roll writes immediately with a deterministic reason instead of prompting
ok 1538 - choosing a priority roll writes immediately with a deterministic reason instead of prompting
  ---
  duration_ms: 6.39655
  ...
# Subtest: counted scheduled picker requires one shared configured priority
ok 1539 - counted scheduled picker requires one shared configured priority
  ---
  duration_ms: 7.767087
  ...
# Subtest: buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
ok 1540 - buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
  ---
  duration_ms: 3.184039
  ...
# Subtest: buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
ok 1541 - buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
  ---
  duration_ms: 0.315833
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
ok 1542 - buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
  ---
  duration_ms: 0.446703
  ...
# Subtest: buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
ok 1543 - buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
  ---
  duration_ms: 0.29319
  ...
# Subtest: buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
ok 1544 - buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
  ---
  duration_ms: 0.423077
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
ok 1545 - buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
  ---
  duration_ms: 0.171618
  ...
# Subtest: buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
ok 1546 - buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
  ---
  duration_ms: 0.241661
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
ok 1547 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
  ---
  duration_ms: 0.384514
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child work log under the project task
ok 1548 - buildProjectSeedFromChildBullets moves a direct-child work log under the project task
  ---
  duration_ms: 0.339779
  ...
# Subtest: buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
ok 1549 - buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
  ---
  duration_ms: 0.483834
  ...
# Subtest: buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
ok 1550 - buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
  ---
  duration_ms: 0.272009
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
ok 1551 - buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
  ---
  duration_ms: 0.155356
  ...
# Subtest: buildProjectSeedFromChildBullets moves an empty work log without forcing task output
ok 1552 - buildProjectSeedFromChildBullets moves an empty work log without forcing task output
  ---
  duration_ms: 0.116573
  ...
# Subtest: buildProjectSeedFromChildBullets moves both logs in source order without sorting by kind
ok 1553 - buildProjectSeedFromChildBullets moves both logs in source order without sorting by kind
  ---
  duration_ms: 0.129548
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
ok 1554 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
  ---
  duration_ms: 0.260106
  ...
# Subtest: parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
ok 1555 - parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
  ---
  duration_ms: 0.239898
  ...
# Subtest: parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
ok 1556 - parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
  ---
  duration_ms: 0.155858
  ...
# Subtest: parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
ok 1557 - parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
  ---
  duration_ms: 0.474897
  ...
# Subtest: normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
ok 1558 - normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
  ---
  duration_ms: 0.0998
  ...
# Subtest: parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
ok 1559 - parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
  ---
  duration_ms: 0.094129
  ...
# Subtest: formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
ok 1560 - formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
  ---
  duration_ms: 0.107836
  ...
# Subtest: insertProjectSectionNotes fills an empty existing section with a blank line then the notes
ok 1561 - insertProjectSectionNotes fills an empty existing section with a blank line then the notes
  ---
  duration_ms: 0.5708
  ...
# Subtest: insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
ok 1562 - insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
  ---
  duration_ms: 0.160847
  ...
# Subtest: insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
ok 1563 - insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
  ---
  duration_ms: 0.118686
  ...
# Subtest: insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
ok 1564 - insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
  ---
  duration_ms: 0.217425
  ...
# Subtest: insertProjectSectionNotes does not add a trailing newline when the original content had none
ok 1565 - insertProjectSectionNotes does not add a trailing newline when the original content had none
  ---
  duration_ms: 0.144826
  ...
# Subtest: insertProjectSectionNotes preserves CRLF line endings for an existing section
ok 1566 - insertProjectSectionNotes preserves CRLF line endings for an existing section
  ---
  duration_ms: 0.259836
  ...
# Subtest: insertProjectSectionNotes creates a new section using the document's CRLF line ending
ok 1567 - insertProjectSectionNotes creates a new section using the document's CRLF line ending
  ---
  duration_ms: 0.137683
  ...
# Subtest: buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
ok 1568 - buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
  ---
  duration_ms: 0.189532
  ...
# Subtest: buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
ok 1569 - buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
  ---
  duration_ms: 0.349567
  ...
# Subtest: buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
ok 1570 - buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
  ---
  duration_ms: 0.126932
  ...
# Subtest: buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
ok 1571 - buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
  ---
  duration_ms: 1.106332
  ...
# Subtest: project conversion accepts blocked sources and extracts their managed dependency child
ok 1572 - project conversion accepts blocked sources and extracts their managed dependency child
  ---
  duration_ms: 2.12185
  ...
# Subtest: project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
ok 1573 - project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
  ---
  duration_ms: 1.129506
  ...
# Subtest: buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
ok 1574 - buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
  ---
  duration_ms: 0.371198
  ...
# Subtest: buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
ok 1575 - buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
  ---
  duration_ms: 0.222414
  ...
# Subtest: buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
ok 1576 - buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
  ---
  duration_ms: 0.194642
  ...
# Subtest: insertProjectManagedLogLines preserves CRLF line endings
ok 1577 - insertProjectManagedLogLines preserves CRLF line endings
  ---
  duration_ms: 0.154044
  ...
# Subtest: findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
ok 1578 - findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
  ---
  duration_ms: 0.194752
  ...
# Subtest: getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
ok 1579 - getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
  ---
  duration_ms: 0.201044
  ...
# Subtest: getProjectFromTaskNoticeText reports moved log kinds in a fixed order
ok 1580 - getProjectFromTaskNoticeText reports moved log kinds in a fixed order
  ---
  duration_ms: 0.108527
  ...
# Subtest: forward conversion leaves the project Ready when only the source status was Blocked
ok 1581 - forward conversion leaves the project Ready when only the source status was Blocked
  ---
  duration_ms: 0.351872
  ...
# Subtest: buildTaskBlockFromProjectNote restores the worked example and round-trips
ok 1582 - buildTaskBlockFromProjectNote restores the worked example and round-trips
  ---
  duration_ms: 7.143226
  ...
# Subtest: project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
ok 1583 - project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
  ---
  duration_ms: 2.333905
  ...
# Subtest: buildTaskLineFromProjectNote preserves status, tags, and fields
ok 1584 - buildTaskLineFromProjectNote preserves status, tags, and fields
  ---
  duration_ms: 1.337053
  ...
# Subtest: getProjectReversalBlockId inverts the forward basename helper
ok 1585 - getProjectReversalBlockId inverts the forward basename helper
  ---
  duration_ms: 0.124718
  ...
# Subtest: formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
ok 1586 - formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
  ---
  duration_ms: 0.143443
  ...
# Subtest: splitProjectNoteForReversal treats TASKS as the task section and keeps section order
ok 1587 - splitProjectNoteForReversal treats TASKS as the task section and keeps section order
  ---
  duration_ms: 0.825055
  ...
# Subtest: indentProjectReversalLine preserves relative depth and drops blanks
ok 1588 - indentProjectReversalLine preserves relative depth and drops blanks
  ---
  duration_ms: 0.422958
  ...
# Subtest: buildTaskBlockFromProjectNote reports structure and frontmatter errors
ok 1589 - buildTaskBlockFromProjectNote reports structure and frontmatter errors
  ---
  duration_ms: 1.020908
  ...
# Subtest: buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
ok 1590 - buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
  ---
  duration_ms: 1.01078
  ...
# Subtest: rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
ok 1591 - rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
  ---
  duration_ms: 0.640783
  ...
# Subtest: collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
ok 1592 - collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
  ---
  duration_ms: 0.595056
  ...
# Subtest: getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
ok 1593 - getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
  ---
  duration_ms: 0.192537
  ...
# Subtest: convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
ok 1594 - convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
  ---
  duration_ms: 5.954145
  ...
# Subtest: project reversal recovers tagged residents when they leave a blocked project
ok 1595 - project reversal recovers tagged residents when they leave a blocked project
  ---
  duration_ms: 4.646389
  ...
# Subtest: convertProjectNoteToTask separates the restored task from a count-only parent section
ok 1596 - convertProjectNoteToTask separates the restored task from a count-only parent section
  ---
  duration_ms: 1.139937
  ...
# Subtest: createProjectNoteFromTask dispatches reverse only on a real ^prj line
ok 1597 - createProjectNoteFromTask dispatches reverse only on a real ^prj line
  ---
  duration_ms: 1.718501
  ...
# Subtest: convertProjectNoteToTask refusals leave every file untouched
ok 1598 - convertProjectNoteToTask refusals leave every file untouched
  ---
  duration_ms: 3.618066
  ...
# Subtest: planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
ok 1599 - planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
  ---
  duration_ms: 0.157791
  ...
# Subtest: convertProjectNoteToTask writes the parent first when it links to \#^prj
ok 1600 - convertProjectNoteToTask writes the parent first when it links to \#^prj
  ---
  duration_ms: 1.046308
  ...
# Subtest: convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
ok 1601 - convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
  ---
  duration_ms: 2.56693
  ...
# Subtest: convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
ok 1602 - convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
  ---
  duration_ms: 1.311043
  ...
# Subtest: convertProjectNoteToTask reports post-write failures without rolling back
ok 1603 - convertProjectNoteToTask reports post-write failures without rolling back
  ---
  duration_ms: 1.191835
  ...
# Subtest: convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
ok 1604 - convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
  ---
  duration_ms: 1.386436
  ...
# Subtest: convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
ok 1605 - convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
  ---
  duration_ms: 1.69205
  ...
# Subtest: reading tasks read with the book prefix, plain tasks unchanged
ok 1606 - reading tasks read with the book prefix, plain tasks unchanged
  ---
  duration_ms: 1.221552
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 1607 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.232083
  ...
# Subtest: picker rows carry the book prefix in displayText
ok 1608 - picker rows carry the book prefix in displayText
  ---
  duration_ms: 0.663797
  ...
# Subtest: planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
ok 1609 - planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
  ---
  duration_ms: 6.170027
  ...
# Subtest: planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
ok 1610 - planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
  ---
  duration_ms: 2.186124
  ...
# Subtest: runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
ok 1611 - runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
  ---
  duration_ms: 4.50575
  ...
# Subtest: runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
ok 1612 - runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
  ---
  duration_ms: 3.380503
  ...
# Subtest: runtime: no daily note today still writes the schedule with no Pomodoro chip
ok 1613 - runtime: no daily note today still writes the schedule with no Pomodoro chip
  ---
  duration_ms: 0.563566
  ...
# Subtest: runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
ok 1614 - runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
  ---
  duration_ms: 0.992274
  ...
# Subtest: runtime: vault.process throwing during the daily-note write is reported without throwing
ok 1615 - runtime: vault.process throwing during the daily-note write is reported without throwing
  ---
  duration_ms: 0.888286
  ...
# Subtest: runtime: the daily note open in another editor is written through that editor in its own transaction
ok 1616 - runtime: the daily note open in another editor is written through that editor in its own transaction
  ---
  duration_ms: 0.987315
  ...
# Subtest: runtime: re-running the same deferral gesture is idempotent
ok 1617 - runtime: re-running the same deferral gesture is idempotent
  ---
  duration_ms: 0.90152
  ...
# Subtest: runtime: a counted scheduled batch prunes exactly the targets that land on a future date
ok 1618 - runtime: a counted scheduled batch prunes exactly the targets that land on a future date
  ---
  duration_ms: 3.672139
  ...
# Subtest: runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
ok 1619 - runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
  ---
  duration_ms: 3.160834
  ...
# Subtest: runtime: the source note being today's daily note folds the prune into a single editor transaction
ok 1620 - runtime: the source note being today's daily note folds the prune into a single editor transaction
  ---
  duration_ms: 0.762997
  ...
# Subtest: bare future scheduled writes block only real supported open inline tasks
ok 1621 - bare future scheduled writes block only real supported open inline tasks
  ---
  duration_ms: 5.502593
  ...
# Subtest: single runtime transclusion toggle preserves viewport in one line transaction
ok 1622 - single runtime transclusion toggle preserves viewport in one line transaction
  ---
  duration_ms: 1.44602
  ...
# Subtest: same-file runtime toggle changes only markers, never fields or statuses
ok 1623 - same-file runtime toggle changes only markers, never fields or statuses
  ---
  duration_ms: 0.625875
  ...
# Subtest: pure toggle leaves a cursor moved during the toggle where it landed
ok 1624 - pure toggle leaves a cursor moved during the toggle where it landed
  ---
  duration_ms: 0.259245
  ...
# Subtest: counted runtime transclusion toggle preserves viewport and caret
ok 1625 - counted runtime transclusion toggle preserves viewport and caret
  ---
  duration_ms: 0.721999
  ...
# Subtest: counted property runtime uses one transaction and preserves caret and viewport
ok 1626 - counted property runtime uses one transaction and preserves caret and viewport
  ---
  duration_ms: 2.987282
  ...
# Subtest: bare due schedule recovery is guarded and can change only task status
ok 1627 - bare due schedule recovery is guarded and can change only task status
  ---
  duration_ms: 2.579804
  ...
# Subtest: counted due recovery applies Ready Next and In Progress in one transaction
ok 1628 - counted due recovery applies Ready Next and In Progress in one transaction
  ---
  duration_ms: 4.224224
  ...
# Subtest: scheduled recovery aborts after an asynchronous source change
ok 1629 - scheduled recovery aborts after an asynchronous source change
  ---
  duration_ms: 0.783506
  ...
# Subtest: counted property runtime aborts a stale batch without a transaction
ok 1630 - counted property runtime aborts a stale batch without a transaction
  ---
  duration_ms: 0.477632
  ...
# Subtest: counted project scheduling writes an inline date and blocks tagged residents
ok 1631 - counted project scheduling writes an inline date and blocks tagged residents
  ---
  duration_ms: 2.842976
  ...
# Subtest: future project scheduling prunes resident links and an emptied Pomodoro
ok 1632 - future project scheduling prunes resident links and an emptied Pomodoro
  ---
  duration_ms: 2.825693
  ...
# Subtest: single project scheduling recovers due residents through the gate
ok 1633 - single project scheduling recovers due residents through the gate
  ---
  duration_ms: 1.806048
  ...
# Subtest: single project schedule deletion removes propagated copies and recovers
ok 1634 - single project schedule deletion removes propagated copies and recovers
  ---
  duration_ms: 1.601237
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: formatPriorityRollScheduleReason covers all four shapes
ok 1635 - formatPriorityRollScheduleReason covers all four shapes
  ---
  duration_ms: 1.148723
  ...
# Subtest: the priority-roll picker row keeps range detail and stores the exact roll
ok 1636 - the priority-roll picker row keeps range detail and stores the exact roll
  ---
  duration_ms: 0.548647
  ...
# Subtest: buildPriorityRollScheduleLog returns null when the roll does not move the date
ok 1637 - buildPriorityRollScheduleLog returns null when the roll does not move the date
  ---
  duration_ms: 0.621386
  ...
# Subtest: getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
ok 1638 - getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
  ---
  duration_ms: 0.680979
  ...
# Subtest: a priority roll onto the current date writes the date but no log
ok 1639 - a priority roll onto the current date writes the date but no log
  ---
  duration_ms: 12.115227
  ...
# Subtest: a typed reason on an unchanged date is still written
ok 1640 - a typed reason on an unchanged date is still written
  ---
  duration_ms: 0.692682
  ...
# Subtest: schedule log bullet formatting and parsing round-trip with and without a previous value
ok 1641 - schedule log bullet formatting and parsing round-trip with and without a previous value
  ---
  duration_ms: 0.859731
  ...
# Subtest: formatScheduleLogEntryText renders entry text without indent or marker
ok 1642 - formatScheduleLogEntryText renders entry text without indent or marker
  ---
  duration_ms: 0.124808
  ...
# Subtest: schedule reason text normalization trims, collapses whitespace, and flags inline fields
ok 1643 - schedule reason text normalization trims, collapses whitespace, and flags inline fields
  ---
  duration_ms: 0.349236
  ...
# Subtest: findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
ok 1644 - findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
  ---
  duration_ms: 0.690307
  ...
# Subtest: getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
ok 1645 - getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
  ---
  duration_ms: 0.215782
  ...
# Subtest: planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
ok 1646 - planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
  ---
  duration_ms: 0.37157
  ...
# Subtest: planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
ok 1647 - planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
  ---
  duration_ms: 0.181446
  ...
# Subtest: planScheduleLogEntry uses the fallback only when a marker exists
ok 1648 - planScheduleLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.186356
  ...
# Subtest: a typed reason wins over the fallback
ok 1649 - a typed reason wins over the fallback
  ---
  duration_ms: 0.123135
  ...
# Subtest: the fallback is suppressed on an unchanged date
ok 1650 - the fallback is suppressed on an unchanged date
  ---
  duration_ms: 0.097587
  ...
# Subtest: no reason and no fallback still guards empty-reason
ok 1651 - no reason and no fallback still guards empty-reason
  ---
  duration_ms: 0.097857
  ...
# Subtest: getScheduleLogWriteOutcome maps plan outcomes for writers
ok 1652 - getScheduleLogWriteOutcome maps plan outcomes for writers
  ---
  duration_ms: 0.130789
  ...
# Subtest: hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
ok 1653 - hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
  ---
  duration_ms: 0.117454
  ...
# Subtest: counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
ok 1654 - counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
  ---
  duration_ms: 1.609672
  ...
# Subtest: empty reason through the counted planner writes no schedule log entries
ok 1655 - empty reason through the counted planner writes no schedule log entries
  ---
  duration_ms: 0.551914
  ...
# Subtest: a counted scheduled session logs only the tasks that already keep a log
ok 1656 - a counted scheduled session logs only the tasks that already keep a log
  ---
  duration_ms: 0.572011
  ...
# Subtest: the counted notice wording distinguishes a fallback batch from a typed-reason batch
ok 1657 - the counted notice wording distinguishes a fallback batch from a typed-reason batch
  ---
  duration_ms: 2.925174
  ...
# Subtest: setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
ok 1658 - setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
  ---
  duration_ms: 0.296025
  ...
# Subtest: setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
ok 1659 - setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
  ---
  duration_ms: 2.531163
  ...
# Subtest: priority bullet property config normalizes frozen levels and preserves existing shapes
ok 1660 - priority bullet property config normalizes frozen levels and preserves existing shapes
  ---
  duration_ms: 2.189189
  ...
# Subtest: priority bullet property config rejects each invalid schema category once
ok 1661 - priority bullet property config rejects each invalid schema category once
  ---
  duration_ms: 1.046157
  ...
# Subtest: project scheduling targets the inline ^prj field
ok 1662 - project scheduling targets the inline ^prj field
  ---
  duration_ms: 1.887723
  ...
# Subtest: local task properties are addable only on valid tasks but invalid metadata stays removable
ok 1663 - local task properties are addable only on valid tasks but invalid metadata stays removable
  ---
  duration_ms: 0.301576
  ...
# Subtest: dependency parent write validation rejects stale, Pomodoro, and fenced parents
ok 1664 - dependency parent write validation rejects stale, Pomodoro, and fenced parents
  ---
  duration_ms: 0.47713
  ...
# Subtest: counted property targets mean current plus N real tasks without wrapping
ok 1665 - counted property targets mean current plus N real tasks without wrapping
  ---
  duration_ms: 0.654479
  ...
# Subtest: counted property metadata distinguishes absent, common, and mixed values
ok 1666 - counted property metadata distinguishes absent, common, and mixed values
  ---
  duration_ms: 0.637747
  ...
# Subtest: counted priority metadata reports labels for common and mixed values
ok 1667 - counted priority metadata reports labels for common and mixed values
  ---
  duration_ms: 0.571782
  ...
# Subtest: counted scheduled planning updates the motivating three tasks atomically
ok 1668 - counted scheduled planning updates the motivating three tasks atomically
  ---
  duration_ms: 2.277598
  ...
# Subtest: project schedule validation accepts only real YYYY-MM-DD dates
ok 1669 - project schedule validation accepts only real YYYY-MM-DD dates
  ---
  duration_ms: 1.137622
  ...
# Subtest: source task schedule is extracted without losing task metadata
ok 1670 - source task schedule is extracted without losing task metadata
  ---
  duration_ms: 1.254806
  ...
# Subtest: source task schedule errors are focused and ambiguous fields fail
ok 1671 - source task schedule errors are focused and ambiguous fields fail
  ---
  duration_ms: 0.351331
  ...
# Subtest: project creation frontmatter never stores the task schedule
ok 1672 - project creation frontmatter never stores the task schedule
  ---
  duration_ms: 0.162811
  ...
# Subtest: future schedule labels use local date-only boundaries
ok 1673 - future schedule labels use local date-only boundaries
  ---
  duration_ms: 0.786281
  ...
# Subtest: scheduled recovery selects current and newest earlier daily across gaps
ok 1674 - scheduled recovery selects current and newest earlier daily across gaps
  ---
  duration_ms: 0.551263
  ...
# Subtest: scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
ok 1675 - scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
  ---
  duration_ms: 8.174024
  ...
# Subtest: scheduled recovery defers incompatible status settings and ambiguous identities
ok 1676 - scheduled recovery defers incompatible status settings and ambiguous identities
  ---
  duration_ms: 0.440681
  ...
# Subtest: scheduled recovery honors custom open and closed Tasks status types
ok 1677 - scheduled recovery honors custom open and closed Tasks status types
  ---
  duration_ms: 0.626897
  ...
# Subtest: scheduled recovery honors the configured Tasks global filter
ok 1678 - scheduled recovery honors the configured Tasks global filter
  ---
  duration_ms: 0.537936
  ...
# Subtest: child picker schedule metadata reads the inline ^prj date
ok 1679 - child picker schedule metadata reads the inline ^prj date
  ---
  duration_ms: 0.858028
  ...
# Subtest: task move destination schedule hydration reads cached ^prj content
ok 1680 - task move destination schedule hydration reads cached ^prj content
  ---
  duration_ms: 0.477572
  ...
# Subtest: project lifecycle task classification requires unfenced \#task with trailing ^prj
ok 1681 - project lifecycle task classification requires unfenced \#task with trailing ^prj
  ---
  duration_ms: 0.157641
  ...
# Subtest: valid Obsidian tasks require a standalone \#task checkbox in real note content
ok 1682 - valid Obsidian tasks require a standalone \#task checkbox in real note content
  ---
  duration_ms: 0.133485
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: choosing a scheduled date enters the combined review without writing anything
ok 1683 - choosing a scheduled date enters the combined review without writing anything
  ---
  duration_ms: 14.879192
  ...
# Subtest: choosing a priority level does not enter the schedule review
ok 1684 - choosing a priority level does not enter the schedule review
  ---
  duration_ms: 11.632836
  ...
# Subtest: confirming an empty reason on a task with an existing schedule log appends an unexplained entry
ok 1685 - confirming an empty reason on a task with an existing schedule log appends an unexplained entry
  ---
  duration_ms: 7.388874
  ...
# Subtest: confirming an empty reason on a task with no schedule log writes only the date
ok 1686 - confirming an empty reason on a task with no schedule log writes only the date
  ---
  duration_ms: 3.858225
  ...
# Subtest: review stage getFilteredItems always returns exactly one synthetic preview item
ok 1687 - review stage getFilteredItems always returns exactly one synthetic preview item
  ---
  duration_ms: 1.926718
  ...
# Subtest: the review preview row previews the entry it will write
ok 1688 - the review preview row previews the entry it will write
  ---
  duration_ms: 3.906597
  ...
# Subtest: the review footer flips between Skip optional logs and Apply schedule as the Reason changes
ok 1689 - the review footer flips between Skip optional logs and Apply schedule as the Reason changes
  ---
  duration_ms: 1.719803
  ...
# Subtest: closing the picker during the review clears pending schedule state and writes nothing
ok 1690 - closing the picker during the review clears pending schedule state and writes nothing
  ---
  duration_ms: 1.463614
  ...
# Subtest: scheduling Work Log eligibility requires Pending or Next \#task lines
ok 1691 - scheduling Work Log eligibility requires Pending or Next \#task lines
  ---
  duration_ms: 1.156758
  ...
# Subtest: single Pending explicit date opens one review and writes both logs
ok 1692 - single Pending explicit date opens one review and writes both logs
  ---
  duration_ms: 16.53874
  ...
# Subtest: single Next blank and whitespace summaries schedule without a Work Log
ok 1693 - single Next blank and whitespace summaries schedule without a Work Log
  ---
  duration_ms: 4.365253
  ...
# Subtest: Escape at the review writes nothing, with or without typed text
ok 1694 - Escape at the review writes nothing, with or without typed text
  ---
  duration_ms: 3.705875
  ...
# Subtest: Ready and Blocked explicit dates review the Reason with no Work summary field
ok 1695 - Ready and Blocked explicit dates review the Reason with no Work summary field
  ---
  duration_ms: 4.309285
  ...
# Subtest: future scheduling on Pending marks Blocked but still writes the Work Log
ok 1696 - future scheduling on Pending marks Blocked but still writes the Work Log
  ---
  duration_ms: 2.044743
  ...
# Subtest: today date on Pending still offers the Work Log
ok 1697 - today date on Pending still offers the Work Log
  ---
  duration_ms: 3.065531
  ...
# Subtest: priority pick on Pending freezes its roll and offers the Work Log
ok 1698 - priority pick on Pending freezes its roll and offers the Work Log
  ---
  duration_ms: 5.113482
  ...
# Subtest: counted mixed statuses share one summary only on Pending and Next
ok 1699 - counted mixed statuses share one summary only on Pending and Next
  ---
  duration_ms: 8.10902
  ...
# Subtest: counted planner composes Schedule and Work Logs bottom-up above later targets
ok 1700 - counted planner composes Schedule and Work Logs bottom-up above later targets
  ---
  duration_ms: 1.279663
  ...
# Subtest: counted planner writes a Work Log even when the date is unchanged
ok 1701 - counted planner writes a Work Log even when the date is unchanged
  ---
  duration_ms: 0.448245
  ...
# Subtest: scheduling Work Log ownership keeps nested logs and CRLF endings
ok 1702 - scheduling Work Log ownership keeps nested logs and CRLF endings
  ---
  duration_ms: 3.359994
  ...
# Subtest: scheduling Work Log warns on :: and preserves Markdown
ok 1703 - scheduling Work Log warns on :: and preserves Markdown
  ---
  duration_ms: 4.776247
  ...
# Subtest: stale task while reviewing refuses with no scheduling or log writes
ok 1704 - stale task while reviewing refuses with no scheduling or log writes
  ---
  duration_ms: 2.43633
  ...
# Subtest: scheduling prompts never leak into lane or cancel stages
ok 1705 - scheduling prompts never leak into lane or cancel stages
  ---
  duration_ms: 2.763335
  ...
# Subtest: Pomodoro-marked links are not managed dependency bullets
ok 1706 - Pomodoro-marked links are not managed dependency bullets
  ---
  duration_ms: 1.389563
  ...
# Subtest: deleting inline scheduled metadata recovers Blocked targets by snapshot rank
ok 1707 - deleting inline scheduled metadata recovers Blocked targets by snapshot rank
  ---
  duration_ms: 3.543464
  ...
# Subtest: counted future scheduling blocks only supported open inline task statuses
ok 1708 - counted future scheduling blocks only supported open inline task statuses
  ---
  duration_ms: 1.65015
  ...
# Subtest: counted property planning rejects any stale source with no partial result
ok 1709 - counted property planning rejects any stale source with no partial result
  ---
  duration_ms: 0.273141
  ...
# Subtest: counted project scheduling writes the ^prj inline date and blocks tagged residents
ok 1710 - counted project scheduling writes the ^prj inline date and blocks tagged residents
  ---
  duration_ms: 1.903243
  ...
# Subtest: moving a project schedule earlier replaces only exact old-date copies
ok 1711 - moving a project schedule earlier replaces only exact old-date copies
  ---
  duration_ms: 0.472712
  ...
# Subtest: future project schedules block every open resident and consume review status
ok 1712 - future project schedules block every open resident and consume review status
  ---
  duration_ms: 0.789056
  ...
# Subtest: due project dates recover residents through the gate and write unblocked markers
ok 1713 - due project dates recover residents through the gate and write unblocked markers
  ---
  duration_ms: 0.580478
  ...
# Subtest: schedule deletion removes only exact project-date copies and recovers residents
ok 1714 - schedule deletion removes only exact project-date copies and recovers residents
  ---
  duration_ms: 0.892624
  ...
# Subtest: dependency lines render one canonical Depends-On line per parent
ok 1715 - dependency lines render one canonical Depends-On line per parent
  ---
  duration_ms: 0.629472
  ...
# Subtest: dependency IDs encode root and nested Markdown paths deterministically
ok 1716 - dependency IDs encode root and nested Markdown paths deterministically
  ---
  duration_ms: 1.078549
  ...
# Subtest: prompted block IDs truthfully replace legacy id fields
ok 1717 - prompted block IDs truthfully replace legacy id fields
  ---
  duration_ms: 0.137563
  ...
# Subtest: dependency navigation identity includes note path and folds legacy children
ok 1718 - dependency navigation identity includes note path and folds legacy children
  ---
  duration_ms: 0.85412
  ...
# Subtest: retired dependency bullets are excluded from single and counted toggles
ok 1719 - retired dependency bullets are excluded from single and counted toggles
  ---
  duration_ms: 0.688254
  ...
# Subtest: dependsOn replacement accepts spaces around field name and separator
ok 1720 - dependsOn replacement accepts spaces around field name and separator
  ---
  duration_ms: 0.321824
  ...
# Subtest: task status helpers keep Blocked open but rankless
ok 1721 - task status helpers keep Blocked open but rankless
  ---
  duration_ms: 0.383182
  ...
# Subtest: a due project date with only closed Depends-On history strips the tag
ok 1722 - a due project date with only closed Depends-On history strips the tag
  ---
  duration_ms: 0.737147
  ...
# Subtest: Ctrl+D with only closed Depends-On history strips the tag
ok 1723 - Ctrl+D with only closed Depends-On history strips the tag
  ---
  duration_ms: 0.384323
  ...
# Subtest: Ctrl+D with an open Depends-On link remaining keeps the tag
ok 1724 - Ctrl+D with an open Depends-On link remaining keeps the tag
  ---
  duration_ms: 0.267942
  ...
# Subtest: counted ^prj schedule sessions write [unblocked::] when the writer is passed
ok 1725 - counted ^prj schedule sessions write [unblocked::] when the writer is passed
  ---
  duration_ms: 0.467994
  ...
# Subtest: a due project date keeps the tag while ^prj holds Depends-On links
ok 1726 - a due project date keeps the tag while ^prj holds Depends-On links
  ---
  duration_ms: 0.288892
  ...
# Subtest: a due project date strips the tag while a resident with its own reason stays Blocked
ok 1727 - a due project date strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.259535
  ...
# Subtest: Ctrl+D strips the tag while a resident with its own reason stays Blocked
ok 1728 - Ctrl+D strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.318478
  ...
# Subtest: counted scheduled deletes recover with [unblocked::] when the writer is passed
ok 1729 - counted scheduled deletes recover with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.206094
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: section-header navigation moves normally and cycles at boundaries
ok 1730 - section-header navigation moves normally and cycles at boundaries
  ---
  duration_ms: 2.351919
  ...
# Subtest: section-header navigation wraps from beyond document boundaries
ok 1731 - section-header navigation wraps from beyond document boundaries
  ---
  duration_ms: 0.235399
  ...
# Subtest: section-header navigation handles single-header and no-header notes
ok 1732 - section-header navigation handles single-header and no-header notes
  ---
  duration_ms: 0.239197
  ...
# Subtest: open-task navigation scan includes Ready In Progress and Next and excludes Blocked
ok 1733 - open-task navigation scan includes Ready In Progress and Next and excludes Blocked
  ---
  duration_ms: 0.575408
  ...
# Subtest: open-task navigation keeps existing Pomodoro ledger targets
ok 1734 - open-task navigation keeps existing Pomodoro ledger targets
  ---
  duration_ms: 0.540792
  ...
# Subtest: next and previous jumps skip Blocked tasks and wrap to an allowed task
ok 1735 - next and previous jumps skip Blocked tasks and wrap to an allowed task
  ---
  duration_ms: 0.354467
  ...
# Subtest: blocked-only notes and a sole current allowed task have no jump target
ok 1736 - blocked-only notes and a sole current allowed task have no jump target
  ---
  duration_ms: 0.164755
  ...
# Subtest: counted open-task jumps select the Nth eligible target and wrap modulo the list
ok 1737 - counted open-task jumps select the Nth eligible target and wrap modulo the list
  ---
  duration_ms: 0.284513
  ...
# Subtest: counted open-task jumps keep sole-target and invalid-repeat behavior
ok 1738 - counted open-task jumps keep sole-target and invalid-repeat behavior
  ---
  duration_ms: 0.528398
  ...
# Subtest: tab pin Vim action registers once and toggles only the active leaf once
ok 1739 - tab pin Vim action registers once and toggles only the active leaf once
  ---
  duration_ms: 2.374203
  ...
# Subtest: tab pin toggle fails safely without a supported active leaf
ok 1740 - tab pin toggle fails safely without a supported active leaf
  ---
  duration_ms: 0.165445
  ...
# Subtest: close tabs left preserves pinned sibling tabs and refocuses active tab
ok 1741 - close tabs left preserves pinned sibling tabs and refocuses active tab
  ---
  duration_ms: 0.641414
  ...
# Subtest: close tabs right preserves pinned siblings and ignores the left side
ok 1742 - close tabs right preserves pinned siblings and ignores the left side
  ---
  duration_ms: 0.281026
  ...
# Subtest: close other tabs preserves pinned siblings on both sides
ok 1743 - close other tabs preserves pinned siblings on both sides
  ---
  duration_ms: 0.221793
  ...
# Subtest: close sibling tabs is a silent no-op when the scoped range is all pinned
ok 1744 - close sibling tabs is a silent no-op when the scoped range is all pinned
  ---
  duration_ms: 0.187989
  ...
# Subtest: close sibling tabs honors every pinned leaf representation
ok 1745 - close sibling tabs honors every pinned leaf representation
  ---
  duration_ms: 0.234187
  ...
# Subtest: close sibling tabs treats throwing view state as unpinned
ok 1746 - close sibling tabs treats throwing view state as unpinned
  ---
  duration_ms: 0.336763
  ...
# Subtest: tab pin Vim registration retries after adapter availability
ok 1747 - tab pin Vim registration retries after adapter availability
  ---
  duration_ms: 0.707721
  ...
# Subtest: isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
ok 1748 - isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
  ---
  duration_ms: 5.345343
  ...
# Subtest: isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
ok 1749 - isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
  ---
  duration_ms: 1.018263
  ...
# Subtest: isPomodoroTaskLinkLine refuses Depends-On lines and prose links
ok 1750 - isPomodoroTaskLinkLine refuses Depends-On lines and prose links
  ---
  duration_ms: 0.321153
  ...
# Subtest: decideTaskLinkLaneMode starts when any target is Next
ok 1751 - decideTaskLinkLaneMode starts when any target is Next
  ---
  duration_ms: 0.274624
  ...
# Subtest: taskLinkLaneRefusalFor renders every D5 refusal
ok 1752 - taskLinkLaneRefusalFor renders every D5 refusal
  ---
  duration_ms: 0.222304
  ...
# Subtest: planTaskLinkLaneBatch starts Next targets and leaves the rest alone
ok 1753 - planTaskLinkLaneBatch starts Next targets and leaves the rest alone
  ---
  duration_ms: 1.898274
  ...
# Subtest: planTaskLinkLaneBatch pauses with one shared Work Log entry
ok 1754 - planTaskLinkLaneBatch pauses with one shared Work Log entry
  ---
  duration_ms: 1.132352
  ...
# Subtest: planTaskLinkLaneBatch applies the freshness stamp last
ok 1755 - planTaskLinkLaneBatch applies the freshness stamp last
  ---
  duration_ms: 0.414621
  ...
# Subtest: planTaskLinkLaneBatch dedupes lines and refuses stale preimages
ok 1756 - planTaskLinkLaneBatch dedupes lines and refuses stale preimages
  ---
  duration_ms: 0.709244
  ...
# Subtest: buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
ok 1757 - buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
  ---
  duration_ms: 1.0371
  ...
# Subtest: taskLinkLanePromptState drives the Move to Next prompt
ok 1758 - taskLinkLanePromptState drives the Move to Next prompt
  ---
  duration_ms: 0.378442
  ...
# Subtest: TaskLinkLanePromptModal submits, previews live, and cancels silently
ok 1759 - TaskLinkLanePromptModal submits, previews live, and cancels silently
  ---
  duration_ms: 2.114847
  ...
# Subtest: TaskLinkLanePromptModal renders the batch context card
ok 1760 - TaskLinkLanePromptModal renders the batch context card
  ---
  duration_ms: 0.50335
  ...
# Subtest: findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
ok 1761 - findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
  ---
  duration_ms: 0.452884
  ...
# Subtest: L1: toggle starts a Next link, stamps, hints, and notices
ok 1762 - L1: toggle starts a Next link, stamps, hints, and notices
  ---
  duration_ms: 5.050351
  ...
# Subtest: L2/L3: toggle pauses through the prompt, logging one shared entry
ok 1763 - L2/L3: toggle pauses through the prompt, logging one shared entry
  ---
  duration_ms: 14.809489
  ...
# Subtest: L4: cancelling the prompt writes nothing and shows no Notice
ok 1764 - L4: cancelling the prompt writes nothing and shows no Notice
  ---
  duration_ms: 1.472962
  ...
# Subtest: L5: both directions run the same toggle twice for a round trip
ok 1765 - L5: both directions run the same toggle twice for a round trip
  ---
  duration_ms: 4.315016
  ...
# Subtest: L6: Ready, Blocked, done, and cancelled targets are refused
ok 1766 - L6: Ready, Blocked, done, and cancelled targets are refused
  ---
  duration_ms: 2.354885
  ...
# Subtest: L6: missing targets keep the existing resolver error
ok 1767 - L6: missing targets keep the existing resolver error
  ---
  duration_ms: 0.359927
  ...
# Subtest: L7: a counted start flips every Next sibling and leaves In Progress alone
ok 1768 - L7: a counted start flips every Next sibling and leaves In Progress alone
  ---
  duration_ms: 0.751475
  ...
# Subtest: L8: a counted pause prompts once and skips Blocked with a count
ok 1769 - L8: a counted pause prompts once and skips Blocked with a count
  ---
  duration_ms: 5.144821
  ...
# Subtest: L9: an over-long count clamps at the entry end without error
ok 1770 - L9: an over-long count clamps at the entry end without error
  ---
  duration_ms: 1.124847
  ...
# Subtest: L10: a closed-entry history line toggles the task and keeps the line
ok 1771 - L10: a closed-entry history line toggles the task and keeps the line
  ---
  duration_ms: 0.435612
  ...
# Subtest: L11: a target edited while the prompt is open refuses stale
ok 1772 - L11: a target edited while the prompt is open refuses stale
  ---
  duration_ms: 2.121209
  ...
# Subtest: L12: an embedded Pomodoro link takes the two-state toggle
ok 1773 - L12: an embedded Pomodoro link takes the two-state toggle
  ---
  duration_ms: 0.590678
  ...
# Subtest: L14: the same task linked twice in a batch is written once
ok 1774 - L14: the same task linked twice in a batch is written once
  ---
  duration_ms: 1.873337
  ...
# Subtest: L15: a second toggle while one is in flight is swallowed as busy
ok 1775 - L15: a second toggle while one is in flight is swallowed as busy
  ---
  duration_ms: 1.071566
  ...
# Subtest: toggle on a non-link line refuses without writing
ok 1776 - toggle on a non-link line refuses without writing
  ---
  duration_ms: 0.32995
  ...
# Subtest: api.taskLinkLane is a frozen v1 namespace that never throws
ok 1777 - api.taskLinkLane is a frozen v1 namespace that never throws
  ---
  duration_ms: 1.09508
  ...
# Subtest: the progressMarks hint is a no-op without the ledger-tools api
ok 1778 - the progressMarks hint is a no-op without the ledger-tools api
  ---
  duration_ms: 0.415362
  ...
# Subtest: task move records one Vim jump and round-trips without extra writes
ok 1779 - task move records one Vim jump and round-trips without extra writes
  ---
  duration_ms: 9.231262
  ...
# Subtest: counted task move records a single jump to the first moved task
ok 1780 - counted task move records a single jump to the first moved task
  ---
  duration_ms: 1.435871
  ...
# Subtest: deferred task landing re-anchors and records the resolved cursor once
ok 1781 - deferred task landing re-anchors and records the resolved cursor once
  ---
  duration_ms: 6.211768
  ...
# Subtest: failed task move preserves seeded history including the forward branch
ok 1782 - failed task move preserves seeded history including the forward branch
  ---
  duration_ms: 1.155857
  ...
# Subtest: post-commit open failure keeps the move committed with no jump
ok 1783 - post-commit open failure keeps the move committed with no jump
  ---
  duration_ms: 2.2585
  ...
# Subtest: a newer move supersedes a pending landing without stale placement
ok 1784 - a newer move supersedes a pending landing without stale placement
  ---
  duration_ms: 11.601445
  ...
# Subtest: shared destination helper without a move context records no jump
ok 1785 - shared destination helper without a move context records no jump
  ---
  duration_ms: 0.669558
  ...
# Subtest: task moves carry the Depends-On line and repath stranded same-note links
ok 1786 - task moves carry the Depends-On line and repath stranded same-note links
  ---
  duration_ms: 5.518314
  ...
# Subtest: task moves keep pathless links when the target moves along
ok 1787 - task moves keep pathless links when the target moves along
  ---
  duration_ms: 0.928061
  ...
# Subtest: counted task moves discover movable tasks without wrapping or examples
ok 1788 - counted task moves discover movable tasks without wrapping or examples
  ---
  duration_ms: 0.845984
  ...
# Subtest: task move ranges preserve quoted subtrees and collapse overlapping selections
ok 1789 - task move ranges preserve quoted subtrees and collapse overlapping selections
  ---
  duration_ms: 0.496808
  ...
# Subtest: task move removal handles disjoint ranges, blank seams, and CRLF
ok 1790 - task move removal handles disjoint ranges, blank seams, and CRLF
  ---
  duration_ms: 0.340089
  ...
# Subtest: task move destinations include areas and only open projects
ok 1791 - task move destinations include areas and only open projects
  ---
  duration_ms: 0.482521
  ...
# Subtest: moves into a blocked project leave closed tagged lines alone
ok 1792 - moves into a blocked project leave closed tagged lines alone
  ---
  duration_ms: 1.83319
  ...
# Subtest: moves into a blocked project promote open prerequisites to the moved lane
ok 1793 - moves into a blocked project promote open prerequisites to the moved lane
  ---
  duration_ms: 2.129245
  ...
# Subtest: task move insertion preserves exact task and section spacing
ok 1794 - task move insertion preserves exact task and section spacing
  ---
  duration_ms: 3.078176
  ...
# Subtest: task move planning migrates identities and links across every affected note
ok 1795 - task move planning migrates identities and links across every affected note
  ---
  duration_ms: 4.356226
  ...
# Subtest: task move planning exposes a destination anchor for area destinations and counted moves
ok 1796 - task move planning exposes a destination anchor for area destinations and counted moves
  ---
  duration_ms: 0.882775
  ...
# Subtest: task move into a blocked project tags the moved task and consumes today's live Pomodoro link
ok 1797 - task move into a blocked project tags the moved task and consumes today's live Pomodoro link
  ---
  duration_ms: 2.821636
  ...
# Subtest: task move out of a blocked project recovers through the shared gate and writes the unblocked mark
ok 1798 - task move out of a blocked project recovers through the shared gate and writes the unblocked mark
  ---
  duration_ms: 3.401192
  ...
# Subtest: move promotion walks through a ^prj target without raising it
ok 1799 - move promotion walks through a ^prj target without raising it
  ---
  duration_ms: 2.533848
  ...
# Subtest: move promotion walks through a [?] ^prj to its open prerequisite
ok 1800 - move promotion walks through a [?] ^prj to its open prerequisite
  ---
  duration_ms: 1.044444
  ...
# Subtest: move promotion uses each open task's own lane, not the strongest moved lane
ok 1801 - move promotion uses each open task's own lane, not the strongest moved lane
  ---
  duration_ms: 1.245447
  ...
# Subtest: move promotion skips Depends-On lines of closed tasks
ok 1802 - move promotion skips Depends-On lines of closed tasks
  ---
  duration_ms: 0.786712
  ...
# Subtest: task move planning rejects destination collisions and malformed identities
ok 1803 - task move planning rejects destination collisions and malformed identities
  ---
  duration_ms: 0.574216
  ...
# Subtest: resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
ok 1804 - resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
  ---
  duration_ms: 0.632077
  ...
# Subtest: focusTaskMoveDestination opens the destination file and anchors the cursor
ok 1805 - focusTaskMoveDestination opens the destination file and anchors the cursor
  ---
  duration_ms: 1.104329
  ...
# Subtest: focusTaskMoveDestination returns false without moving the cursor when the open fails
ok 1806 - focusTaskMoveDestination returns false without moving the cursor when the open fails
  ---
  duration_ms: 0.232404
  ...
# Subtest: focusTaskMoveDestination re-anchors by block ID when the destination content drifted
ok 1807 - focusTaskMoveDestination re-anchors by block ID when the destination content drifted
  ---
  duration_ms: 0.239788
  ...
# Subtest: physical task move chord declines auto-repeat and consumes Vim normal input once
ok 1808 - physical task move chord declines auto-repeat and consumes Vim normal input once
  ---
  duration_ms: 0.782184
  ...
# Subtest: physical transclusion toggle owns bare and counted Vim normal input
ok 1809 - physical transclusion toggle owns bare and counted Vim normal input
  ---
  duration_ms: 0.963359
  ...
# Subtest: runtime task move writes destination before source and rolls back source failures
ok 1810 - runtime task move writes destination before source and rolls back source failures
  ---
  duration_ms: 2.050043
  ...
# Subtest: runtime task move groups open-editor source and destination changes
ok 1811 - runtime task move groups open-editor source and destination changes
  ---
  duration_ms: 1.18927
  ...
# Subtest: runtime task move guards destination, auxiliary, and rollback failures
ok 1812 - runtime task move guards destination, auxiliary, and rollback failures
  ---
  duration_ms: 1.768887
  ...
# Subtest: task move insertion separates the section's first task from preamble and placeholders
ok 1813 - task move insertion separates the section's first task from preamble and placeholders
  ---
  duration_ms: 0.372821
  ...
# Subtest: task move insertion keeps populated sections compact and second moves stable
ok 1814 - task move insertion keeps populated sections compact and second moves stable
  ---
  duration_ms: 0.202086
  ...
# Subtest: task move planning separates a counted move into a count-only section
ok 1815 - task move planning separates a counted move into a count-only section
  ---
  duration_ms: 0.399683
  ...
# Subtest: runtime counted move into a count-only section focuses the first moved task
ok 1816 - runtime counted move into a count-only section focuses the first moved task
  ---
  duration_ms: 0.936337
  ...
# Subtest: unblocked model returns null when there is nothing to show
ok 1817 - unblocked model returns null when there is nothing to show
  ---
  duration_ms: 1.753637
  ...
# Subtest: unblocked card renders a single linked row with receipt and chips
ok 1818 - unblocked card renders a single linked row with receipt and chips
  ---
  duration_ms: 1.845083
  ...
# Subtest: unblocked card renders several linked rows with one entry
ok 1819 - unblocked card renders several linked rows with one entry
  ---
  duration_ms: 0.354417
  ...
# Subtest: unblocked card renders a created continuation with next up
ok 1820 - unblocked card renders a created continuation with next up
  ---
  duration_ms: 0.657315
  ...
# Subtest: unblocked card renders recovered-only and still-blocked rows
ok 1821 - unblocked card renders recovered-only and still-blocked rows
  ---
  duration_ms: 1.347051
  ...
# Subtest: current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
ok 1822 - current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
  ---
  duration_ms: 1.531964
  ...
# Subtest: project pull-in rows label empty projects and preserve project blocking reasons
ok 1823 - project pull-in rows label empty projects and preserve project blocking reasons
  ---
  duration_ms: 1.526243
  ...
# Subtest: unblocked card caps visible rows with +N more
ok 1824 - unblocked card caps visible rows with +N more
  ---
  duration_ms: 0.527497
  ...
# Subtest: unblocked card renders the breaker variant
ok 1825 - unblocked card renders the breaker variant
  ---
  duration_ms: 0.666412
  ...
# Subtest: unblocked card renders the failure variant
ok 1826 - unblocked card renders the failure variant
  ---
  duration_ms: 0.621747
  ...
# Subtest: unblocked rows open their task without dismissing the notice
ok 1827 - unblocked rows open their task without dismissing the notice
  ---
  duration_ms: 1.578213
  ...
# Subtest: unblocked row without a block id opens the note path
ok 1828 - unblocked row without a block id opens the note path
  ---
  duration_ms: 0.353224
  ...
# Subtest: unblocked card omits the plan chip when daily content is null
ok 1829 - unblocked card omits the plan chip when daily content is null
  ---
  duration_ms: 0.324179
  ...
# Subtest: unblocked notice shows one card with duration through showNotice
ok 1830 - unblocked notice shows one card with duration through showNotice
  ---
  duration_ms: 0.391969
  ...
# Subtest: unblocked notice falls back to plain text without a DOM
ok 1831 - unblocked notice falls back to plain text without a DOM
  ---
  duration_ms: 0.200313
  ...
# Subtest: unblocked text truncates to 48 characters with an ellipsis
ok 1832 - unblocked text truncates to 48 characters with an ellipsis
  ---
  duration_ms: 0.196966
  ...
# Subtest: nav api exposes additive notice v1 and keeps version 3
ok 1833 - nav api exposes additive notice v1 and keeps version 3
  ---
  duration_ms: 0.45612
  ...
# Subtest: unblocked stylesheet scopes notice overrides and uses task tokens
ok 1834 - unblocked stylesheet scopes notice overrides and uses task tokens
  ---
  duration_ms: 0.70188
  ...
# Subtest: physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
ok 1835 - physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
  ---
  duration_ms: 2.392246
  ...
# Subtest: open-task command ids omit repeat so the shared route resolves the pending Vim count
ok 1836 - open-task command ids omit repeat so the shared route resolves the pending Vim count
  ---
  duration_ms: 1.219017
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
ok 1837 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
  ---
  duration_ms: 3.887402
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
ok 1838 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
  ---
  duration_ms: 0.713753
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
ok 1839 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
  ---
  duration_ms: 1.092766
  ...
# Subtest: dispatch guard applies a command-route Vim count when the capture route fires second
ok 1840 - dispatch guard applies a command-route Vim count when the capture route fires second
  ---
  duration_ms: 0.932981
  ...
# Subtest: dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
ok 1841 - dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
  ---
  duration_ms: 0.715977
  ...
# Subtest: command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
ok 1842 - command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
  ---
  duration_ms: 0.627868
  ...
# Subtest: command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
ok 1843 - command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
  ---
  duration_ms: 2.097494
  ...
# Subtest: command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
ok 1844 - command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
  ---
  duration_ms: 0.908193
  ...
# Subtest: explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
ok 1845 - explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
  ---
  duration_ms: 0.610175
  ...
# Subtest: getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
ok 1846 - getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
  ---
  duration_ms: 0.176176
  ...
# Subtest: physical counted property chord consumes only explicit normal-mode Vim counts
ok 1847 - physical counted property chord consumes only explicit normal-mode Vim counts
  ---
  duration_ms: 0.557374
  ...
# Subtest: task-card-gate arms only on open inbox tasks
ok 1848 - task-card-gate arms only on open inbox tasks
  ---
  duration_ms: 4.067183
  ...
# Subtest: task-card-gate header shows the Inbox chip only when armed
ok 1849 - task-card-gate header shows the Inbox chip only when armed
  ---
  duration_ms: 6.952442
  ...
# Subtest: task-card-gate priority: cancel writes nothing
ok 1850 - task-card-gate priority: cancel writes nothing
  ---
  duration_ms: 1.559979
  ...
# Subtest: task-card-gate priority: stay runs today's write
ok 1851 - task-card-gate priority: stay runs today's write
  ---
  duration_ms: 0.334028
  ...
# Subtest: task-card-gate priority: move writes then moves
ok 1852 - task-card-gate priority: move writes then moves
  ---
  duration_ms: 0.747867
  ...
# Subtest: task-card-gate scheduled: cancel writes nothing
ok 1853 - task-card-gate scheduled: cancel writes nothing
  ---
  duration_ms: 0.186657
  ...
# Subtest: task-card-gate scheduled: stay runs today's write
ok 1854 - task-card-gate scheduled: stay runs today's write
  ---
  duration_ms: 0.305794
  ...
# Subtest: task-card-gate scheduled: move writes then moves
ok 1855 - task-card-gate scheduled: move writes then moves
  ---
  duration_ms: 1.261307
  ...
# Subtest: task-card-gate generic-property: cancel writes nothing
ok 1856 - task-card-gate generic-property: cancel writes nothing
  ---
  duration_ms: 0.567363
  ...
# Subtest: task-card-gate generic-property: stay runs today's write
ok 1857 - task-card-gate generic-property: stay runs today's write
  ---
  duration_ms: 0.766343
  ...
# Subtest: task-card-gate generic-property: move writes then moves
ok 1858 - task-card-gate generic-property: move writes then moves
  ---
  duration_ms: 0.528939
  ...
# Subtest: task-card-gate refresh-interval: cancel writes nothing
ok 1859 - task-card-gate refresh-interval: cancel writes nothing
  ---
  duration_ms: 0.250649
  ...
# Subtest: task-card-gate refresh-interval: stay runs today's write
ok 1860 - task-card-gate refresh-interval: stay runs today's write
  ---
  duration_ms: 0.246531
  ...
# Subtest: task-card-gate refresh-interval: move writes then moves
ok 1861 - task-card-gate refresh-interval: move writes then moves
  ---
  duration_ms: 0.270176
  ...
# Subtest: task-card-gate refresh-custom: cancel writes nothing
ok 1862 - task-card-gate refresh-custom: cancel writes nothing
  ---
  duration_ms: 0.15722
  ...
# Subtest: task-card-gate refresh-custom: stay runs today's write
ok 1863 - task-card-gate refresh-custom: stay runs today's write
  ---
  duration_ms: 0.15197
  ...
# Subtest: task-card-gate refresh-custom: move writes then moves
ok 1864 - task-card-gate refresh-custom: move writes then moves
  ---
  duration_ms: 0.426384
  ...
# Subtest: task-card-gate clear-priority: cancel writes nothing
ok 1865 - task-card-gate clear-priority: cancel writes nothing
  ---
  duration_ms: 0.190393
  ...
# Subtest: task-card-gate clear-priority: stay runs today's write
ok 1866 - task-card-gate clear-priority: stay runs today's write
  ---
  duration_ms: 0.156689
  ...
# Subtest: task-card-gate clear-priority: move writes then moves
ok 1867 - task-card-gate clear-priority: move writes then moves
  ---
  duration_ms: 0.166919
  ...
# Subtest: task-card-gate recommended-roll: cancel writes nothing
ok 1868 - task-card-gate recommended-roll: cancel writes nothing
  ---
  duration_ms: 0.103297
  ...
# Subtest: task-card-gate recommended-roll: stay runs today's write
ok 1869 - task-card-gate recommended-roll: stay runs today's write
  ---
  duration_ms: 0.103508
  ...
# Subtest: task-card-gate recommended-roll: move writes then moves
ok 1870 - task-card-gate recommended-roll: move writes then moves
  ---
  duration_ms: 0.149195
  ...
# Subtest: task-card-gate recommended-decay: cancel writes nothing
ok 1871 - task-card-gate recommended-decay: cancel writes nothing
  ---
  duration_ms: 0.129077
  ...
# Subtest: task-card-gate recommended-decay: stay runs today's write
ok 1872 - task-card-gate recommended-decay: stay runs today's write
  ---
  duration_ms: 0.132583
  ...
# Subtest: task-card-gate recommended-decay: move writes then moves
ok 1873 - task-card-gate recommended-decay: move writes then moves
  ---
  duration_ms: 0.146811
  ...
# Subtest: task-card-gate counted-roll: cancel writes nothing
ok 1874 - task-card-gate counted-roll: cancel writes nothing
  ---
  duration_ms: 0.181596
  ...
# Subtest: task-card-gate counted-roll: stay runs today's write
ok 1875 - task-card-gate counted-roll: stay runs today's write
  ---
  duration_ms: 0.134106
  ...
# Subtest: task-card-gate counted-roll: move writes then moves
ok 1876 - task-card-gate counted-roll: move writes then moves
  ---
  duration_ms: 0.279203
  ...
# Subtest: task-card-gate lane-toggle: cancel writes nothing
ok 1877 - task-card-gate lane-toggle: cancel writes nothing
  ---
  duration_ms: 0.143394
  ...
# Subtest: task-card-gate lane-toggle: stay runs today's write
ok 1878 - task-card-gate lane-toggle: stay runs today's write
  ---
  duration_ms: 0.138394
  ...
# Subtest: task-card-gate lane-toggle: move writes then moves
ok 1879 - task-card-gate lane-toggle: move writes then moves
  ---
  duration_ms: 0.234137
  ...
# Subtest: task-card-gate dependency-single: cancel writes nothing
ok 1880 - task-card-gate dependency-single: cancel writes nothing
  ---
  duration_ms: 0.145348
  ...
# Subtest: task-card-gate dependency-single: stay runs today's write
ok 1881 - task-card-gate dependency-single: stay runs today's write
  ---
  duration_ms: 0.113086
  ...
# Subtest: task-card-gate dependency-single: move writes then moves
ok 1882 - task-card-gate dependency-single: move writes then moves
  ---
  duration_ms: 0.359987
  ...
# Subtest: task-card-gate dependency-marked: cancel writes nothing
ok 1883 - task-card-gate dependency-marked: cancel writes nothing
  ---
  duration_ms: 0.087938
  ...
# Subtest: task-card-gate dependency-marked: stay runs today's write
ok 1884 - task-card-gate dependency-marked: stay runs today's write
  ---
  duration_ms: 0.089551
  ...
# Subtest: task-card-gate dependency-marked: move writes then moves
ok 1885 - task-card-gate dependency-marked: move writes then moves
  ---
  duration_ms: 0.0997
  ...
# Subtest: task-card-gate dependency-vault: cancel writes nothing
ok 1886 - task-card-gate dependency-vault: cancel writes nothing
  ---
  duration_ms: 0.081525
  ...
# Subtest: task-card-gate dependency-vault: stay runs today's write
ok 1887 - task-card-gate dependency-vault: stay runs today's write
  ---
  duration_ms: 0.088068
  ...
# Subtest: task-card-gate dependency-vault: move writes then moves
ok 1888 - task-card-gate dependency-vault: move writes then moves
  ---
  duration_ms: 0.107545
  ...
# Subtest: task-card-gate dependency-counted: cancel writes nothing
ok 1889 - task-card-gate dependency-counted: cancel writes nothing
  ---
  duration_ms: 0.08894
  ...
# Subtest: task-card-gate dependency-counted: stay runs today's write
ok 1890 - task-card-gate dependency-counted: stay runs today's write
  ---
  duration_ms: 0.0894
  ...
# Subtest: task-card-gate dependency-counted: move writes then moves
ok 1891 - task-card-gate dependency-counted: move writes then moves
  ---
  duration_ms: 0.139686
  ...
# Subtest: task-card-gate negative rows never prompt
ok 1892 - task-card-gate negative rows never prompt
  ---
  duration_ms: 1.329047
  ...
# Subtest: task-card-gate counted sessions capture N targets
ok 1893 - task-card-gate counted sessions capture N targets
  ---
  duration_ms: 0.354066
  ...
# Subtest: task-card-gate walk: move advances once with Moved first
ok 1894 - task-card-gate walk: move advances once with Moved first
  ---
  duration_ms: 0.271979
  ...
# Subtest: task-card-gate walk: move failure falls back to card with partial
ok 1895 - task-card-gate walk: move failure falls back to card with partial
  ---
  duration_ms: 0.438247
  ...
# Subtest: task-card-gate walk: exactly one settle per origin
ok 1896 - task-card-gate walk: exactly one settle per origin
  ---
  duration_ms: 28.657985
  ...
# Subtest: task-card-gate route outcome resolves like lane and link-today
ok 1897 - task-card-gate route outcome resolves like lane and link-today
  ---
  duration_ms: 0.362702
  ...
# Subtest: inbox classifier covers the inbox contract
ok 1898 - inbox classifier covers the inbox contract
  ---
  duration_ms: 1.701497
  ...
# Subtest: isInboxNotePath matches the inbox contract through the vault
ok 1899 - isInboxNotePath matches the inbox contract through the vault
  ---
  duration_ms: 1.054663
  ...
# Subtest: isInboxNotePath is false without an inbox note and never throws
ok 1900 - isInboxNotePath is false without an inbox note and never throws
  ---
  duration_ms: 0.158774
  ...
# Subtest: route destinations drop every inbox note, the source, and templates
ok 1901 - route destinations drop every inbox note, the source, and templates
  ---
  duration_ms: 0.722379
  ...
# Subtest: route preflight accepts a live area destination
ok 1902 - route preflight accepts a live area destination
  ---
  duration_ms: 3.840242
  ...
# Subtest: route preflight refuses stale and colliding destinations
ok 1903 - route preflight refuses stale and colliding destinations
  ---
  duration_ms: 1.435029
  ...
# Subtest: route picker resolves move, stay, cancel, and close exactly once
ok 1904 - route picker resolves move, stay, cancel, and close exactly once
  ---
  duration_ms: 3.145705
  ...
# Subtest: route picker footer names the move, the hatch, and the way back
ok 1905 - route picker footer names the move, the hatch, and the way back
  ---
  duration_ms: 0.441563
  ...
# Subtest: route picker preflight refusal keeps the picker open with a notice
ok 1906 - route picker preflight refusal keeps the picker open with a notice
  ---
  duration_ms: 6.95144
  ...
# Subtest: route picker honors the shared move-picker guard
ok 1907 - route picker honors the shared move-picker guard
  ---
  duration_ms: 2.21081
  ...
# Subtest: promptInboxRoute moves, stays, and cancels with suspend pairing
ok 1908 - promptInboxRoute moves, stays, and cancels with suspend pairing
  ---
  duration_ms: 2.779556
  ...
# Subtest: commitInboxRoute moves the verified task with its children
ok 1909 - commitInboxRoute moves the verified task with its children
  ---
  duration_ms: 3.91311
  ...
# Subtest: commitInboxRoute into a blocked project tags the moved task
ok 1910 - commitInboxRoute into a blocked project tags the moved task
  ---
  duration_ms: 1.838579
  ...
# Subtest: commitInboxRoute moves a counted run and refuses on identity drift
ok 1911 - commitInboxRoute moves a counted run and refuses on identity drift
  ---
  duration_ms: 1.492108
  ...
# Subtest: reviewOutcomeResolves treats route like lane and link-today
ok 1912 - reviewOutcomeResolves treats route like lane and link-today
  ---
  duration_ms: 0.280907
  ...
# Subtest: nav api inboxRoute v1 delegates, shapes, and never throws
ok 1913 - nav api inboxRoute v1 delegates, shapes, and never throws
  ---
  duration_ms: 1.391947
  ...
# Subtest: history records ordered locations with file identity and dedupes adjacent repeats
ok 1914 - history records ordered locations with file identity and dedupes adjacent repeats
  ---
  duration_ms: 1.243424
  ...
# Subtest: transition records origin then destination and truncates forward only on success
ok 1915 - transition records origin then destination and truncates forward only on success
  ---
  duration_ms: 0.746815
  ...
# Subtest: history retains at most 100 locations and refreshes the live tip
ok 1916 - history retains at most 100 locations and refreshes the live tip
  ---
  duration_ms: 0.67543
  ...
# Subtest: rename updates paths and delete prunes without corrupting the index
ok 1917 - rename updates paths and delete prunes without corrupting the index
  ---
  duration_ms: 0.231913
  ...
# Subtest: bridge wraps add once, mirrors native jumps, and preserves the original call
ok 1918 - bridge wraps add once, mirrors native jumps, and preserves the original call
  ---
  duration_ms: 1.218747
  ...
# Subtest: bridge without a jump list preserves keys and emits one compatibility diagnostic
ok 1919 - bridge without a jump list preserves keys and emits one compatibility diagnostic
  ---
  duration_ms: 0.266088
  ...
# Subtest: registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
ok 1920 - registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
  ---
  duration_ms: 0.298139
  ...
# Subtest: Enter A->B round-trips with Ctrl+O and Ctrl+I
ok 1921 - Enter A->B round-trips with Ctrl+O and Ctrl+I
  ---
  duration_ms: 21.674383
  ...
# Subtest: counted Enter returns to the original cursor, not the counted link line
ok 1922 - counted Enter returns to the original cursor, not the counted link line
  ---
  duration_ms: 21.696015
  ...
# Subtest: picker choice records one jump and cancellation records none
ok 1923 - picker choice records one jump and cancellation records none
  ---
  duration_ms: 21.436681
  ...
# Subtest: stale picker origin is rejected and failed opens record nothing
ok 1924 - stale picker origin is rejected and failed opens record nothing
  ---
  duration_ms: 21.294137
  ...
# Subtest: Backspace shares the link path and no-link lines fall through
ok 1925 - Backspace shares the link path and no-link lines fall through
  ---
  duration_ms: 20.365786
  ...
# Subtest: counted traversal honors boundaries and new jumps replace the forward branch
ok 1926 - counted traversal honors boundaries and new jumps replace the forward branch
  ---
  duration_ms: 0.656703
  ...
# Subtest: ordinary motion before back is preserved for forward restore
ok 1927 - ordinary motion before back is preserved for forward restore
  ---
  duration_ms: 0.277319
  ...
# Subtest: deleted entries are skipped and heading links settle before recording
ok 1928 - deleted entries are skipped and heading links settle before recording
  ---
  duration_ms: 20.80799
  ...
# Subtest: native fallback runs with empty history and boundaries never replay natives
ok 1929 - native fallback runs with empty history and boundaries never replay natives
  ---
  duration_ms: 0.736577
  ...
# Subtest: unload restores the native add and keeps a foreign later mapping
ok 1930 - unload restores the native add and keeps a foreign later mapping
  ---
  duration_ms: 0.411415
  ...
# Subtest: exact eligibility authorizes one due-Ready ROTTEN row
ok 1931 - exact eligibility authorizes one due-Ready ROTTEN row
  ---
  duration_ms: 1.775389
  ...
# Subtest: exact eligibility authorizes a TICKLER row
ok 1932 - exact eligibility authorizes a TICKLER row
  ---
  duration_ms: 0.248654
  ...
# Subtest: exact eligibility refuses every stale-cache shape
ok 1933 - exact eligibility refuses every stale-cache shape
  ---
  duration_ms: 0.562725
  ...
# Subtest: exact eligibility refuses non-Ready and non-due rows
ok 1934 - exact eligibility refuses non-Ready and non-due rows
  ---
  duration_ms: 0.368444
  ...
# Subtest: legacy refs still match line-only while exact refuses
ok 1935 - legacy refs still match line-only while exact refuses
  ---
  duration_ms: 0.685619
  ...
# Subtest: keeps support needs namespace v5 with keepLine
ok 1936 - keeps support needs namespace v5 with keepLine
  ---
  duration_ms: 0.186927
  ...
# Subtest: decay decisions need namespace v6 with keepLine
ok 1937 - decay decisions need namespace v6 with keepLine
  ---
  duration_ms: 0.242182
  ...
# Subtest: batch forwards per-target counted decisions to the stamper
ok 1938 - batch forwards per-target counted decisions to the stamper
  ---
  duration_ms: 0.912301
  ...
# Subtest: batch keeps legacy index targets uncounted
ok 1939 - batch keeps legacy index targets uncounted
  ---
  duration_ms: 0.447194
  ...
# Subtest: a throwing stamper refuses the batch with no partial write
ok 1940 - a throwing stamper refuses the batch with no partial write
  ---
  duration_ms: 0.588794
  ...
# Subtest: parseKeepsCount reads the first valid value only
ok 1941 - parseKeepsCount reads the first valid value only
  ---
  duration_ms: 0.403089
  ...
# Subtest: countFreshStampKept measures actual increments only
ok 1942 - countFreshStampKept measures actual increments only
  ---
  duration_ms: 0.192728
  ...
# Subtest: fresh stamp notice tails kept increments without promises
ok 1943 - fresh stamp notice tails kept increments without promises
  ---
  duration_ms: 0.198399
  ...
# Subtest: duplicate source targets dedupe to one write
ok 1944 - duplicate source targets dedupe to one write
  ---
  duration_ms: 0.174212
  ...
# Subtest: single Alt+F increments an exact due-Ready ROTTEN task
ok 1945 - single Alt+F increments an exact due-Ready ROTTEN task
  ---
  duration_ms: 4.768413
  ...
# Subtest: single Alt+F preserves NEW, lane, and early tasks without counting
ok 1946 - single Alt+F preserves NEW, lane, and early tasks without counting
  ---
  duration_ms: 2.230207
  ...
# Subtest: same-day repeat stays identical and counts nothing
ok 1947 - same-day repeat stays identical and counts nothing
  ---
  duration_ms: 1.891602
  ...
# Subtest: Pending Alt+F writes its summary with the stamp in one edit
ok 1948 - Pending Alt+F writes its summary with the stamp in one edit
  ---
  duration_ms: 1.025107
  ...
# Subtest: counted Pending refresh shares one summary only with Pending targets
ok 1949 - counted Pending refresh shares one summary only with Pending targets
  ---
  duration_ms: 0.607651
  ...
# Subtest: a refusing counted target refuses before the Pending Work Log prompt
ok 1950 - a refusing counted target refuses before the Pending Work Log prompt
  ---
  duration_ms: 0.473574
  ...
# Subtest: blank Pending refresh advances; cancelled or stale prompts write nothing
ok 1951 - blank Pending refresh advances; cancelled or stale prompts write nothing
  ---
  duration_ms: 1.130337
  ...
# Subtest: stale queue match stamps uncounted and never inflates
ok 1952 - stale queue match stamps uncounted and never inflates
  ---
  duration_ms: 0.513721
  ...
# Subtest: counted Alt+F increments every exact target once
ok 1953 - counted Alt+F increments every exact target once
  ---
  duration_ms: 0.589294
  ...
# Subtest: stale editor source refuses with no write
ok 1954 - stale editor source refuses with no write
  ---
  duration_ms: 0.195904
  ...
# Subtest: single-note write lands in one editor transaction and keeps CRLF
ok 1955 - single-note write lands in one editor transaction and keeps CRLF
  ---
  duration_ms: 0.470087
  ...
# Subtest: v5 without keepLine fails without writing
ok 1956 - v5 without keepLine fails without writing
  ---
  duration_ms: 0.157781
  ...
# Subtest: throwing v5 keepLine refuses the batch with no partial write
ok 1957 - throwing v5 keepLine refuses the batch with no partial write
  ---
  duration_ms: 0.403711
  ...
# Subtest: pre-v5 ledger stamps uncounted through the old stamper
ok 1958 - pre-v5 ledger stamps uncounted through the old stamper
  ---
  duration_ms: 0.555761
  ...
# Subtest: Task Link session skips an at-limit decide target
ok 1959 - Task Link session skips an at-limit decide target
  ---
  duration_ms: 1.905376
  ...
# Subtest: Task Link refresh counts one exact target
ok 1960 - Task Link refresh counts one exact target
  ---
  duration_ms: 0.91678
  ...
# Subtest: duplicate Task Links to one target stamp and count once
ok 1961 - duplicate Task Links to one target stamp and count once
  ---
  duration_ms: 0.506437
  ...
# Subtest: counted Task Links dedupe targets and log only the Pending target
ok 1962 - counted Task Links dedupe targets and log only the Pending target
  ---
  duration_ms: 0.812771
  ...
# Subtest: multi-note stale preimage refuses with no writes
ok 1963 - multi-note stale preimage refuses with no writes
  ---
  duration_ms: 0.743339
  ...
# Subtest: multi-note write failure rolls back the first note
ok 1964 - multi-note write failure rolls back the first note
  ---
  duration_ms: 0.855333
  ...
# Subtest: one physical key through two routes stamps once
ok 1965 - one physical key through two routes stamps once
  ---
  duration_ms: 1.009537
  ...
# Subtest: Ctrl+Alt+F capture advances once and consumes a Vim prefix
ok 1966 - Ctrl+Alt+F capture advances once and consumes a Vim prefix
  ---
  duration_ms: 0.485777
  ...
# Subtest: obsolete and extra-modifier F chords stay unconsumed
ok 1967 - obsolete and extra-modifier F chords stay unconsumed
  ---
  duration_ms: 0.25668
  ...
# Subtest: live Ctrl+Alt+F double dispatch asks once on a Pending task
ok 1968 - live Ctrl+Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.545811
  ...
# Subtest: live Alt+F double dispatch asks once on a Pending task
ok 1969 - live Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.568636
  ...
# Subtest: already-handled refresh keydown leaves Vim state alone
ok 1970 - already-handled refresh keydown leaves Vim state alone
  ---
  duration_ms: 0.167299
  ...
# Subtest: collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
ok 1971 - collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
  ---
  duration_ms: 2.399481
  ...
# Subtest: getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
ok 1972 - getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
  ---
  duration_ms: 2.157077
  ...
# Subtest: getProjectBlockState reports an open external prerequisite
ok 1973 - getProjectBlockState reports an open external prerequisite
  ---
  duration_ms: 0.583494
  ...
# Subtest: getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
ok 1974 - getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
  ---
  duration_ms: 0.547826
  ...
# Subtest: getProjectBlockState scheduledValue override is the inline date, not frontmatter
ok 1975 - getProjectBlockState scheduledValue override is the inline date, not frontmatter
  ---
  duration_ms: 0.398962
  ...
# Subtest: getProjectBlockState skips internal and archive Depends-On links
ok 1976 - getProjectBlockState skips internal and archive Depends-On links
  ---
  duration_ms: 0.335269
  ...
# Subtest: getProjectBlockState is a no-op for terminal, daily, and non-project notes
ok 1977 - getProjectBlockState is a no-op for terminal, daily, and non-project notes
  ---
  duration_ms: 0.588022
  ...
# Subtest: projectLooksBlockedByPrjShortcut is the single [?] ^prj row
ok 1978 - projectLooksBlockedByPrjShortcut is the single [?] ^prj row
  ---
  duration_ms: 0.221273
  ...
# Subtest: taskHasProjectBlockedTag is token-bounded and does not match \#prj
ok 1979 - taskHasProjectBlockedTag is token-bounded and does not match \#prj
  ---
  duration_ms: 0.330361
  ...
# Subtest: setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
ok 1980 - setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
  ---
  duration_ms: 0.860412
  ...
# Subtest: reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
ok 1981 - reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
  ---
  duration_ms: 0.414341
  ...
# Subtest: reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
ok 1982 - reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
  ---
  duration_ms: 0.237534
  ...
# Subtest: reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
ok 1983 - reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
  ---
  duration_ms: 0.171848
  ...
# Subtest: ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
ok 1984 - ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
  ---
  duration_ms: 4.377025
  ...
# Subtest: recovery gate keeps a resident of a blocked project blocked after own deps close
ok 1985 - recovery gate keeps a resident of a blocked project blocked after own deps close
  ---
  duration_ms: 1.979789
  ...
# Subtest: recovery gate blocks residents on a future inline project date with no deps
ok 1986 - recovery gate blocks residents on a future inline project date with no deps
  ---
  duration_ms: 0.422616
  ...
# Subtest: planDeferredPomodoroLinkCleanup removeEmptiedEntries deletes a last-child open entry
ok 1987 - planDeferredPomodoroLinkCleanup removeEmptiedEntries deletes a last-child open entry
  ---
  duration_ms: 1.390454
  ...
# Subtest: TICKLER notice uses unblocked <date> when returnedBy is unblocked
ok 1988 - TICKLER notice uses unblocked <date> when returnedBy is unblocked
  ---
  duration_ms: 0.427686
  ...
# Subtest: recognition: a `^prj` parent in a project note carries its residents
ok 1989 - recognition: a `^prj` parent in a project note carries its residents
  ---
  duration_ms: 4.296451
  ...
# Subtest: recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
ok 1990 - recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
  ---
  duration_ms: 0.661833
  ...
# Subtest: add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
ok 1991 - add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
  ---
  duration_ms: 6.469761
  ...
# Subtest: add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
ok 1992 - add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
  ---
  duration_ms: 3.914422
  ...
# Subtest: guards: a same-note add to `^prj` refuses, including mixed batches
ok 1993 - guards: a same-note add to `^prj` refuses, including mixed batches
  ---
  duration_ms: 1.057218
  ...
# Subtest: guards: the stage disables same-note rows for `^prj` with `inside this project`
ok 1994 - guards: the stage disables same-note rows for `^prj` with `inside this project`
  ---
  duration_ms: 1.693232
  ...
# Subtest: guards: cycle detection includes the implicit resident edges (§13.6)
ok 1995 - guards: cycle detection includes the implicit resident edges (§13.6)
  ---
  duration_ms: 1.835303
  ...
# Subtest: removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
ok 1996 - removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
  ---
  duration_ms: 4.538252
  ...
# Subtest: removal: a resident with its own reason stays `[?]` without the tag (PDB3)
ok 1997 - removal: a resident with its own reason stays `[?]` without the tag (PDB3)
  ---
  duration_ms: 1.303629
  ...
# Subtest: removal without a registry defers to reconcile: residents keep `[?]` and the tag
ok 1998 - removal without a registry defers to reconcile: residents keep `[?]` and the tag
  ---
  duration_ms: 1.096784
  ...
# Subtest: writer: one gesture commits `^prj` and its residents in a single undo group
ok 1999 - writer: one gesture commits `^prj` and its residents in a single undo group
  ---
  duration_ms: 0.831077
  ...
# Subtest: writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
ok 2000 - writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
  ---
  duration_ms: 1.667713
  ...
# Subtest: notices: the project strings name the task, the flips, and the Pomodoro cleanup
ok 2001 - notices: the project strings name the task, the flips, and the Pomodoro cleanup
  ---
  duration_ms: 0.248715
  ...
# Subtest: mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
ok 2002 - mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
  ---
  duration_ms: 0.190433
  ...
# Subtest: api v3: removeDependencyByRef delegates removals to the single-transaction writer
ok 2003 - api v3: removeDependencyByRef delegates removals to the single-transaction writer
  ---
  duration_ms: 0.62358
  ...
# Subtest: api v3: openDependencyStageForRef opens the Depends on stage on the owning task
ok 2004 - api v3: openDependencyStageForRef opens the Depends on stage on the owning task
  ---
  duration_ms: 0.274053
  ...
# Subtest: internal links stay on the line but leave the field (PDR7)
ok 2005 - internal links stay on the line but leave the field (PDR7)
  ---
  duration_ms: 0.605396
  ...
# Subtest: removal from an unblocked ^prj never recovers own-reason residents (§13.10)
ok 2006 - removal from an unblocked ^prj never recovers own-reason residents (§13.10)
  ---
  duration_ms: 0.493713
  ...
# Subtest: resident recovery touches only tagged residents (§13.10)
ok 2007 - resident recovery touches only tagged residents (§13.10)
  ---
  duration_ms: 0.875822
  ...
# Subtest: stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
ok 2008 - stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
  ---
  duration_ms: 0.619051
  ...
# Subtest: projectDependentResidentKeys lists open residents with block ids
ok 2009 - projectDependentResidentKeys lists open residents with block ids
  ---
  duration_ms: 0.271157
  ...
# Subtest: navNoteScopeFlags marks daily notes; a missing writer stays null
ok 2010 - navNoteScopeFlags marks daily notes; a missing writer stays null
  ---
  duration_ms: 0.212716
  ...
# Subtest: reconcileBlockedScheduledTaskLine forwards scope flags to the writer
ok 2011 - reconcileBlockedScheduledTaskLine forwards scope flags to the writer
  ---
  duration_ms: 0.132142
  ...
# Subtest: parseProjectNoteFrontmatter ignores leftover scheduled keys
ok 2012 - parseProjectNoteFrontmatter ignores leftover scheduled keys
  ---
  duration_ms: 0.429841
  ...
# Subtest: formatTaskMoveProjectCountsNotice names blocked and recovered counts
ok 2013 - formatTaskMoveProjectCountsNotice names blocked and recovered counts
  ---
  duration_ms: 0.124648
  ...
# Subtest: PDS15: projectParentTarget keeps the path and drops alias and heading
ok 2014 - PDS15: projectParentTarget keeps the path and drops alias and heading
  ---
  duration_ms: 1.047349
  ...
# Subtest: PDS6: list-form, missing, and non-wikilink parents yield none
ok 2015 - PDS6: list-form, missing, and non-wikilink parents yield none
  ---
  duration_ms: 0.428458
  ...
# Subtest: PDS15: resolveProjectParentPath accepts alias, path, and heading forms
ok 2016 - PDS15: resolveProjectParentPath accepts alias, path, and heading forms
  ---
  duration_ms: 0.375396
  ...
# Subtest: PDS6: self, unresolved, and ambiguous basenames yield no parent
ok 2017 - PDS6: self, unresolved, and ambiguous basenames yield no parent
  ---
  duration_ms: 0.146079
  ...
# Subtest: buildProjectChildrenMap and descendants BFS skip cycles and cap depth
ok 2018 - buildProjectChildrenMap and descendants BFS skip cycles and cap depth
  ---
  duration_ms: 2.376146
  ...
# Subtest: PDS6: area, terminal, daily, and self-parent notes are not children
ok 2019 - PDS6: area, terminal, daily, and self-parent notes are not children
  ---
  duration_ms: 0.337194
  ...
# Subtest: PDG8: planner blocks child and grandchild ^prj and residents
ok 2020 - PDG8: planner blocks child and grandchild ^prj and residents
  ---
  duration_ms: 2.497267
  ...
# Subtest: PDG9: planner recovers tagged descendants with [unblocked::]
ok 2021 - PDG9: planner recovers tagged descendants with [unblocked::]
  ---
  duration_ms: 1.39837
  ...
# Subtest: PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
ok 2022 - PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
  ---
  duration_ms: 1.799977
  ...
# Subtest: PDG11: a tagged root re-asserts descendant tags and recovers nothing
ok 2023 - PDG11: a tagged root re-asserts descendant tags and recovers nothing
  ---
  duration_ms: 0.78065
  ...
# Subtest: tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
ok 2024 - tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
  ---
  duration_ms: 0.2459
  ...
# Subtest: tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
ok 2025 - tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
  ---
  duration_ms: 1.819603
  ...
# Subtest: tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
ok 2026 - tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
  ---
  duration_ms: 0.191215
  ...
# Subtest: tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
ok 2027 - tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
  ---
  duration_ms: 1.848309
  ...
# Subtest: PDG13: failProjectPrjInternalAdd refuses descendant targets
ok 2028 - PDG13: failProjectPrjInternalAdd refuses descendant targets
  ---
  duration_ms: 0.258574
  ...
# Subtest: PDG13: planDependencyEdit refuses a descendant add from the files map
ok 2029 - PDG13: planDependencyEdit refuses a descendant add from the files map
  ---
  duration_ms: 1.149955
  ...
# Subtest: PDG13: the stage disables descendant rows
ok 2030 - PDG13: the stage disables descendant rows
  ---
  duration_ms: 1.143083
  ...
# Subtest: reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
ok 2031 - reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
  ---
  duration_ms: 0.324319
  ...
# Subtest: tag proxy: removing the last own dep of a tagged ^prj recovers nobody
ok 2032 - tag proxy: removing the last own dep of a tagged ^prj recovers nobody
  ---
  duration_ms: 2.148531
  ...
# Subtest: PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
ok 2033 - PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
  ---
  duration_ms: 20.262969
  ...
# Subtest: PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
ok 2034 - PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
  ---
  duration_ms: 5.903279
  ...
# Subtest: PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
ok 2035 - PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
  ---
  duration_ms: 3.719711
  ...
# Subtest: PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
ok 2036 - PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
  ---
  duration_ms: 4.078915
  ...
# Subtest: PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
ok 2037 - PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
  ---
  duration_ms: 4.643745
  ...
# Subtest: PDG12: moving the project date due recovers descendants
ok 2038 - PDG12: moving the project date due recovers descendants
  ---
  duration_ms: 2.906087
  ...
# Subtest: PDG12: deleting the project date recovers descendants
ok 2039 - PDG12: deleting the project date recovers descendants
  ---
  duration_ms: 2.522756
  ...
# Subtest: PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
ok 2040 - PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
  ---
  duration_ms: 4.244563
  ...
# Subtest: PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
ok 2041 - PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
  ---
  duration_ms: 3.974596
  ...
# Subtest: Task Link Depends on writer preserves the internal-target guard on a project task
ok 2042 - Task Link Depends on writer preserves the internal-target guard on a project task
  ---
  duration_ms: 0.903785
  ...
# Subtest: api v3 removeDependencyByRef runs the recovery cascade for a linked project task
ok 2043 - api v3 removeDependencyByRef runs the recovery cascade for a linked project task
  ---
  duration_ms: 2.73966
  ...
# Subtest: counted Schedule writer cascades a future date through descendants
ok 2044 - counted Schedule writer cascades a future date through descendants
  ---
  duration_ms: 2.90701
  ...
# Subtest: counted subtree roots are ancestor-first and each descendant note is planned once
ok 2045 - counted subtree roots are ancestor-first and each descendant note is planned once
  ---
  duration_ms: 1.595605
  ...
# Subtest: Ctrl+D on the Depends on row removes the line and recovers the subtree
ok 2046 - Ctrl+D on the Depends on row removes the line and recovers the subtree
  ---
  duration_ms: 2.673614
  ...
# Subtest: a ^prj with no children reads no other note
ok 2047 - a ^prj with no children reads no other note
  ---
  duration_ms: 0.197907
  ...
# Subtest: single seeds from raw text, not display decorations
ok 2048 - single seeds from raw text, not display decorations
  ---
  duration_ms: 10.361458
  ...
# Subtest: legacy valid free wins; invalid and taken fall through
ok 2049 - legacy valid free wins; invalid and taken fall through
  ---
  duration_ms: 1.471609
  ...
# Subtest: batch reserves suffixes for two same-text tasks
ok 2050 - batch reserves suffixes for two same-text tasks
  ---
  duration_ms: 0.920046
  ...
# Subtest: counted-source, vault-single, and vault-counted seed per mode
ok 2051 - counted-source, vault-single, and vault-counted seed per mode
  ---
  duration_ms: 1.210069
  ...
# Subtest: cross-note uses the target note, never the dependent fallback
ok 2052 - cross-note uses the target note, never the dependent fallback
  ---
  duration_ms: 1.137451
  ...
# Subtest: staging writes nothing until confirmed
ok 2053 - staging writes nothing until confirmed
  ---
  duration_ms: 0.641124
  ...
# Subtest: Less often picker renders actual rows from 90 days and Escape writes nothing
ok 2054 - Less often picker renders actual rows from 90 days and Escape writes nothing
  ---
  duration_ms: 5.365162
  ...
# Subtest: Less often picker renders actual rows from 120 days and Escape writes nothing
ok 2055 - Less often picker renders actual rows from 120 days and Escape writes nothing
  ---
  duration_ms: 0.606016
  ...
# Subtest: Less often picker renders actual rows from 180 days and Escape writes nothing
ok 2056 - Less often picker renders actual rows from 180 days and Escape writes nothing
  ---
  duration_ms: 0.479325
  ...
# Subtest: renderFooter skips malformed hints and retains valid structured hints
ok 2057 - renderFooter skips malformed hints and retains valid structured hints
  ---
  duration_ms: 0.237985
  ...
# Subtest: Pending refresh modal previews the dated Work Log and confirms once
ok 2058 - Pending refresh modal previews the dated Work Log and confirms once
  ---
  duration_ms: 1.243444
  ...
# Subtest: dismissing the Pending refresh modal cancels without a summary
ok 2059 - dismissing the Pending refresh modal cancels without a summary
  ---
  duration_ms: 0.295384
  ...
# Subtest: Alt+N release from a NEXT landing advances with one composed toast
ok 2060 - Alt+N release from a NEXT landing advances with one composed toast
  ---
  duration_ms: 22.629046
  ...
# Subtest: counted Alt+N lands past every handled key in one jump
ok 2061 - counted Alt+N lands past every handled key in one jump
  ---
  duration_ms: 11.879707
  ...
# Subtest: a cancelled Alt+N release prompt stays and frees the lock
ok 2062 - a cancelled Alt+N release prompt stays and frees the lock
  ---
  duration_ms: 11.755701
  ...
# Subtest: Alt+N on a checklist landing stays with the plain notice
ok 2063 - Alt+N on a checklist landing stays with the plain notice
  ---
  duration_ms: 9.526334
  ...
# Subtest: Alt+N off a landing behaves exactly as today
ok 2064 - Alt+N off a landing behaves exactly as today
  ---
  duration_ms: 10.713822
  ...
# Subtest: Alt+N while the gesture lock is held is swallowed
ok 2065 - Alt+N while the gesture lock is held is swallowed
  ---
  duration_ms: 10.228143
  ...
# Subtest: a Task Card priority commit on NEXT advances, landing after the rich card
ok 2066 - a Task Card priority commit on NEXT advances, landing after the rich card
  ---
  duration_ms: 24.358638
  ...
# Subtest: dismissing the Task Card stays and frees the lock
ok 2067 - dismissing the Task Card stays and frees the lock
  ---
  duration_ms: 10.006911
  ...
# Subtest: a frontmatter-only project edit from the card stays
ok 2068 - a frontmatter-only project edit from the card stays
  ---
  duration_ms: 9.956697
  ...
# Subtest: a same-day priority schedule on a checklist row stays
ok 2069 - a same-day priority schedule on a checklist row stays
  ---
  duration_ms: 13.077683
  ...
# Subtest: a future schedule on a checklist row advances
ok 2070 - a future schedule on a checklist row advances
  ---
  duration_ms: 18.891531
  ...
# Subtest: a Task Card cancel on a checklist row advances with the cancel card first
ok 2071 - a Task Card cancel on a checklist row advances with the cancel card first
  ---
  duration_ms: 13.577729
  ...
# Subtest: Ctrl+Shift+M from a landing follows the task and never advances
ok 2072 - Ctrl+Shift+M from a landing follows the task and never advances
  ---
  duration_ms: 17.022454
  ...
# Subtest: Ctrl+Shift+M from a checklist landing keeps the destination focus
ok 2073 - Ctrl+Shift+M from a checklist landing keeps the destination focus
  ---
  duration_ms: 12.196962
  ...
# Subtest: ]s after a landed move resumes at the successor despite the line shift
ok 2074 - ]s after a landed move resumes at the successor despite the line shift
  ---
  duration_ms: 35.101374
  ...
# Subtest: [s after a landed move resumes at the predecessor
ok 2075 - [s after a landed move resumes at the predecessor
  ---
  duration_ms: 11.827447
  ...
# Subtest: a counted move from a landing resumes past every moved target
ok 2076 - a counted move from a landing resumes past every moved target
  ---
  duration_ms: 13.655266
  ...
# Subtest: a stale landing is not parked
ok 2077 - a stale landing is not parked
  ---
  duration_ms: 11.103166
  ...
# Subtest: Ctrl+Shift+M while the gesture lock is held is swallowed
ok 2078 - Ctrl+Shift+M while the gesture lock is held is swallowed
  ---
  duration_ms: 0.839873
  ...
# Subtest: dismissing the move picker stays and frees the lock
ok 2079 - dismissing the move picker stays and frees the lock
  ---
  duration_ms: 10.60335
  ...
# Subtest: Ctrl+Shift+M off a landing behaves exactly as today
ok 2080 - Ctrl+Shift+M off a landing behaves exactly as today
  ---
  duration_ms: 10.841726
  ...
# Subtest: answer, move, answer stays in queue order past an accumulator alias
ok 2081 - answer, move, answer stays in queue order past an accumulator alias
  ---
  duration_ms: 5.190349
  ...
# Subtest: a move park ignores a stale accumulator alias
ok 2082 - a move park ignores a stale accumulator alias
  ---
  duration_ms: 1.23107
  ...
# Subtest: a re-indexed origin still advances from the landed row
ok 2083 - a re-indexed origin still advances from the landed row
  ---
  duration_ms: 2.733637
  ...
# Subtest: a landed move park clears the current review task
ok 2084 - a landed move park clears the current review task
  ---
  duration_ms: 0.71772
  ...
# Subtest: predicate: reviewOutcomeResolves across tiers and kinds
ok 2085 - predicate: reviewOutcomeResolves across tiers and kinds
  ---
  duration_ms: 4.027627
  ...
# Subtest: findReviewResumeIndex identifies rows by path and text
ok 2086 - findReviewResumeIndex identifies rows by path and text
  ---
  duration_ms: 0.414491
  ...
# Subtest: buildReviewMoveAnchor parks text-identified resume neighbours
ok 2087 - buildReviewMoveAnchor parks text-identified resume neighbours
  ---
  duration_ms: 0.798244
  ...
# Subtest: planReviewJump with a move anchor resumes at the walk neighbour
ok 2088 - planReviewJump with a move anchor resumes at the walk neighbour
  ---
  duration_ms: 1.467161
  ...
# Subtest: capture: null off a landing
ok 2089 - capture: null off a landing
  ---
  duration_ms: 4.307634
  ...
# Subtest: capture: frozen origin shape, BUSY while locked, expiry
ok 2090 - capture: frozen origin shape, BUSY while locked, expiry
  ---
  duration_ms: 0.655721
  ...
# Subtest: successor picker keeps a captured completion locked through selection and one walk toast
ok 2091 - successor picker keeps a captured completion locked through selection and one walk toast
  ---
  duration_ms: 18.39319
  ...
# Subtest: continue: refuses stale origins, showing the notice once
ok 2092 - continue: refuses stale origins, showing the notice once
  ---
  duration_ms: 7.00968
  ...
# Subtest: continue: stays on null and non-resolving outcomes
ok 2093 - continue: stays on null and non-resolving outcomes
  ---
  duration_ms: 1.523469
  ...
# Subtest: continue: stays for lane answers and mixed-version completes on checklist rows
ok 2094 - continue: stays for lane answers and mixed-version completes on checklist rows
  ---
  duration_ms: 3.633996
  ...
# Subtest: continue: a resolving lane answer advances exactly once with one composed toast
ok 2095 - continue: a resolving lane answer advances exactly once with one composed toast
  ---
  duration_ms: 2.701337
  ...
# Subtest: continue: counted handled refs land past every handled key in one jump
ok 2096 - continue: counted handled refs land past every handled key in one jump
  ---
  duration_ms: 1.344417
  ...
# Subtest: continue: wrap is announced and the empty queue composes the empty notice
ok 2097 - continue: wrap is announced and the empty queue composes the empty notice
  ---
  duration_ms: 4.1597
  ...
# Subtest: continue: anchor-only planning survives cursor drift and lagging queues
ok 2098 - continue: anchor-only planning survives cursor drift and lagging queues
  ---
  duration_ms: 3.136065
  ...
# Subtest: continue: POST origins never wrap
ok 2099 - continue: POST origins never wrap
  ---
  duration_ms: 2.731104
  ...
# Subtest: complete: the last lane row before POST stays with the next-step toast
ok 2100 - complete: the last lane row before POST stays with the next-step toast
  ---
  duration_ms: 3.662561
  ...
# Subtest: complete: a wrap onto a skipped PRE row stays
ok 2101 - complete: a wrap onto a skipped PRE row stays
  ---
  duration_ms: 2.831926
  ...
# Subtest: complete: a step into ROTTEN shows the boundary line
ok 2102 - complete: a step into ROTTEN shows the boundary line
  ---
  duration_ms: 2.938018
  ...
# Subtest: busy: walk keys, refresh, claim, and capture are swallowed in the settle window
ok 2103 - busy: walk keys, refresh, claim, and capture are swallowed in the settle window
  ---
  duration_ms: 4.513445
  ...
# Subtest: advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
ok 2104 - advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
  ---
  duration_ms: 4.159019
  ...
# Subtest: advance: decay choices advance except reword, with no preamble of their own
ok 2105 - advance: decay choices advance except reword, with no preamble of their own
  ---
  duration_ms: 0.776743
  ...
# Subtest: jump history: same-note and cross-note auto-advances record, and <C-o> returns
ok 2106 - jump history: same-note and cross-note auto-advances record, and <C-o> returns
  ---
  duration_ms: 6.818285
  ...
# Subtest: jump history: a manual ]s also records its landing
ok 2107 - jump history: a manual ]s also records its landing
  ---
  duration_ms: 2.108766
  ...
# Subtest: api: reviewWalk v3 is frozen with version 1, degrades null, never throws
ok 2108 - api: reviewWalk v3 is frozen with version 1, degrades null, never throws
  ---
  duration_ms: 1.973337
  ...
# Subtest: walk identity: a stale accumulator key never moves the anchor
ok 2109 - walk identity: a stale accumulator key never moves the anchor
  ---
  duration_ms: 0.376659
  ...
# Subtest: walk identity: a lagging answered row stays excluded
ok 2110 - walk identity: a lagging answered row stays excluded
  ---
  duration_ms: 0.191866
  ...
# Subtest: walk identity: a line-shifting answer lands on the true successor by text
ok 2111 - walk identity: a line-shifting answer lands on the true successor by text
  ---
  duration_ms: 0.313749
  ...
# Subtest: walk identity: legacy anchors without text resolve as before
ok 2112 - walk identity: legacy anchors without text resolve as before
  ---
  duration_ms: 0.30367
  ...
# Subtest: walk identity: matchFreshStampRefs prefers text over line
ok 2113 - walk identity: matchFreshStampRefs prefers text over line
  ---
  duration_ms: 0.153673
  ...
# Subtest: walk identity: collectReviewAnswerKeys separates position from exclusion
ok 2114 - walk identity: collectReviewAnswerKeys separates position from exclusion
  ---
  duration_ms: 0.467121
  ...
# Subtest: return: planReviewWalkReturn pure decisions
ok 2115 - return: planReviewWalkReturn pure decisions
  ---
  duration_ms: 0.331633
  ...
# Subtest: return: same-note ]s returns then steps, both directions
ok 2116 - return: same-note ]s returns then steps, both directions
  ---
  duration_ms: 1.377109
  ...
# Subtest: return: a different due row returns instead of stepping from there
ok 2117 - return: a different due row returns instead of stepping from there
  ---
  duration_ms: 0.504443
  ...
# Subtest: return: cross-note return re-arms and records <C-o>
ok 2118 - return: cross-note return re-arms and records <C-o>
  ---
  duration_ms: 4.131336
  ...
# Subtest: return: a count is consumed and ignored
ok 2119 - return: a count is consumed and ignored
  ---
  duration_ms: 0.732858
  ...
# Subtest: return: endpoints never return
ok 2120 - return: endpoints never return
  ---
  duration_ms: 0.65998
  ...
# Subtest: return: its own stamp ends it
ok 2121 - return: its own stamp ends it
  ---
  duration_ms: 0.840655
  ...
# Subtest: return: a stamp elsewhere does not end it
ok 2122 - return: a stamp elsewhere does not end it
  ---
  duration_ms: 0.764158
  ...
# Subtest: return: answers move the current task, a stopped Ctrl+Enter clears it
ok 2123 - return: answers move the current task, a stopped Ctrl+Enter clears it
  ---
  duration_ms: 3.863805
  ...
# Subtest: return: a stale landing falls through in the same press
ok 2124 - return: a stale landing falls through in the same press
  ---
  duration_ms: 0.417838
  ...
# Subtest: return: a day change never returns
ok 2125 - return: a day change never returns
  ---
  duration_ms: 0.673145
  ...
# Subtest: predicate: reviewOutcomeResolves for the RECURRING resolution table
ok 2126 - predicate: reviewOutcomeResolves for the RECURRING resolution table
  ---
  duration_ms: 0.57088
  ...
# Subtest: recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
ok 2127 - recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
  ---
  duration_ms: 0.234318
  ...
# Subtest: return: a RECURRING landing rearms the current-task return
ok 2128 - return: a RECURRING landing rearms the current-task return
  ---
  duration_ms: 0.412758
  ...
# Subtest: review answer outcome vectors map to the schema vocabulary
ok 2129 - review answer outcome vectors map to the schema vocabulary
  ---
  duration_ms: 1.615434
  ...
# Subtest: event builder uses the walk row key and its tier, once per distinct key
ok 2130 - event builder uses the walk row key and its tier, once per distinct key
  ---
  duration_ms: 1.119438
  ...
# Subtest: journal appends are queued and failures retain events without failing answers
ok 2131 - journal appends are queued and failures retain events without failing answers
  ---
  duration_ms: 5.579601
  ...
# Subtest: card after-line outcomes map done, drop, defer, sequence, and card
ok 2132 - card after-line outcomes map done, drop, defer, sequence, and card
  ---
  duration_ms: 1.359956
  ...
# Subtest: journal events carry plugin@manifest version with a 2.x fallback
ok 2133 - journal events carry plugin@manifest version with a 2.x fallback
  ---
  duration_ms: 1.308358
  ...
# Subtest: write failures show one notice per burst and a recovery notice
ok 2134 - write failures show one notice per burst and a recovery notice
  ---
  duration_ms: 1.101192
  ...
# Subtest: missing api.stats shows one session notice and later delivers retained events
ok 2135 - missing api.stats shows one session notice and later delivers retained events
  ---
  duration_ms: 1.488361
  ...
# Subtest: validation rejects drop the event and continue the drain
ok 2136 - validation rejects drop the event and continue the drain
  ---
  duration_ms: 1.0535
  ...
# Subtest: pending journal events cap at 500 and warn once per burst
ok 2137 - pending journal events cap at 500 and warn once per burst
  ---
  duration_ms: 2.429087
  ...
# Subtest: decay config defaults to enabled with one roll per level
ok 2138 - decay config defaults to enabled with one roll per level
  ---
  duration_ms: 4.037587
  ...
# Subtest: decay:false disables decay and level rolls are accepted but ignored
ok 2139 - decay:false disables decay and level rolls are accepted but ignored
  ---
  duration_ms: 0.499864
  ...
# Subtest: decay.rolls sets the limit and levels[].rolls overrides it
ok 2140 - decay.rolls sets the limit and levels[].rolls overrides it
  ---
  duration_ms: 0.201174
  ...
# Subtest: decay config rejects bad rolls, unknown keys and non-priority use
ok 2141 - decay config rejects bad rolls, unknown keys and non-priority use
  ---
  duration_ms: 0.427086
  ...
# Subtest: classifyScheduleLogRollReason sorts automatic heads from deliberate ones
ok 2142 - classifyScheduleLogRollReason sorts automatic heads from deliberate ones
  ---
  duration_ms: 0.712951
  ...
# Subtest: conformance vectors 1-10: streaks at P2 with the default limit
ok 2143 - conformance vectors 1-10: streaks at P2 with the default limit
  ---
  duration_ms: 2.402436
  ...
# Subtest: conformance vectors 11-15: custom limits, disabled decay and edges
ok 2144 - conformance vectors 11-15: custom limits, disabled decay and edges
  ---
  duration_ms: 0.685359
  ...
# Subtest: the streak reader follows log grammar: legacy labels, nesting and stops
ok 2145 - the streak reader follows log grammar: legacy labels, nesting and stops
  ---
  duration_ms: 0.439899
  ...
# Subtest: rollPriorityRecommendationDate avoids the current date when the window has room
ok 2146 - rollPriorityRecommendationDate avoids the current date when the window has room
  ---
  duration_ms: 0.564678
  ...
# Subtest: decay and cancel reason formatters use the exact ladder copy
ok 2147 - decay and cancel reason formatters use the exact ladder copy
  ---
  duration_ms: 0.449027
  ...
# Subtest: the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
ok 2148 - the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
  ---
  duration_ms: 0.295815
  ...
# Subtest: the planner returns null without a configured priority
ok 2149 - the planner returns null without a configured priority
  ---
  duration_ms: 0.137222
  ...
# Subtest: buildPriorityRollPreviewModel carries the row copy for every kind
ok 2150 - buildPriorityRollPreviewModel carries the row copy for every kind
  ---
  duration_ms: 0.437936
  ...
# Subtest: picker-single recognizes the recommended-roll keypress
ok 2151 - picker-single recognizes the recommended-roll keypress
  ---
  duration_ms: 0.13123
  ...
# Subtest: picker-single stage-two footers carry the recommended-roll hints
ok 2152 - picker-single stage-two footers carry the recommended-roll hints
  ---
  duration_ms: 0.257451
  ...
# Subtest: picker-single shares one roll between the preview and the pinned row
ok 2153 - picker-single shares one roll between the preview and the pinned row
  ---
  duration_ms: 0.309762
  ...
# Subtest: picker-single plans the next-roll hint for the notice chips
ok 2154 - picker-single plans the next-roll hint for the notice chips
  ---
  duration_ms: 0.526124
  ...
# Subtest: picker-single notice cards name the roll, decay and next press
ok 2155 - picker-single notice cards name the roll, decay and next press
  ---
  duration_ms: 1.380465
  ...
# Subtest: picker-single decay payload and preview-target comparison
ok 2156 - picker-single decay payload and preview-target comparison
  ---
  duration_ms: 0.309491
  ...
# Subtest: picker-counted plans one recommendation per target with skips
ok 2157 - picker-counted plans one recommendation per target with skips
  ---
  duration_ms: 1.699985
  ...
# Subtest: picker-counted batch preview, footer and notice copy
ok 2158 - picker-counted batch preview, footer and notice copy
  ---
  duration_ms: 1.372129
  ...
# Subtest: picker-counted composes cancel then set-priority into one postimage
ok 2159 - picker-counted composes cancel then set-priority into one postimage
  ---
  duration_ms: 2.976912
  ...
# Subtest: picker-counted refuses a recurring cancel as one batch
ok 2160 - picker-counted refuses a recurring cancel as one batch
  ---
  duration_ms: 0.364857
  ...
# Subtest: recommended roll recovers with [unblocked::] when the writer is passed
ok 2161 - recommended roll recovers with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.748819
  ...
# Subtest: picker-counted stale lines refuse and new options stay byte-identical
ok 2162 - picker-counted stale lines refuse and new options stay byte-identical
  ---
  duration_ms: 1.000139
  ...
# Subtest: picker-links aggregates one recommendation per note
ok 2163 - picker-links aggregates one recommendation per note
  ---
  duration_ms: 1.029304
  ...
# Subtest: picker-links refuses a recurring cancel as one batch
ok 2164 - picker-links refuses a recurring cancel as one batch
  ---
  duration_ms: 0.337755
  ...
# Subtest: picker-links takes a single recommended roll with Ctrl+Enter
ok 2165 - picker-links takes a single recommended roll with Ctrl+Enter
  ---
  duration_ms: 28.563895
  ...
# Subtest: picker-links shows no pinned roll row in stage two
ok 2166 - picker-links shows no pinned roll row in stage two
  ---
  duration_ms: 4.66783
  ...
# Subtest: picker-links decays and cancels a single Task Link
ok 2167 - picker-links decays and cancels a single Task Link
  ---
  duration_ms: 4.397213
  ...
# Subtest: picker-links applies a mixed batch across two notes
ok 2168 - picker-links applies a mixed batch across two notes
  ---
  duration_ms: 3.575756
  ...
# Subtest: picker-links refuses the whole batch when a linked note changed
ok 2169 - picker-links refuses the whole batch when a linked note changed
  ---
  duration_ms: 2.806787
  ...
# Subtest: picker-links prunes today's open Pomodoro links
ok 2170 - picker-links prunes today's open Pomodoro links
  ---
  duration_ms: 3.276323
  ...
# Subtest: picker-single Ctrl+Enter rolls a P2 task in one undo group
ok 2171 - picker-single Ctrl+Enter rolls a P2 task in one undo group
  ---
  duration_ms: 13.843265
  ...
# Subtest: picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
ok 2172 - picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
  ---
  duration_ms: 11.159632
  ...
# Subtest: picker-single opens a ^prj task on inline scheduled for an immediate roll
ok 2173 - picker-single opens a ^prj task on inline scheduled for an immediate roll
  ---
  duration_ms: 13.663131
  ...
# Subtest: picker-counted opens on scheduled for an immediate mixed batch
ok 2174 - picker-counted opens on scheduled for an immediate mixed batch
  ---
  duration_ms: 12.988895
  ...
# Subtest: picker-links opens on scheduled for an immediate roll
ok 2175 - picker-links opens on scheduled for an immediate roll
  ---
  duration_ms: 13.064819
  ...
# Subtest: picker-single Ctrl+Enter decays a P2 task in one undo group
ok 2176 - picker-single Ctrl+Enter decays a P2 task in one undo group
  ---
  duration_ms: 12.874816
  ...
# Subtest: picker-single Ctrl+Enter cancels a P4 task in one undo group
ok 2177 - picker-single Ctrl+Enter cancels a P4 task in one undo group
  ---
  duration_ms: 12.073328
  ...
# Subtest: picker-single Ctrl+Enter in stage two writes the recommended roll
ok 2178 - picker-single Ctrl+Enter in stage two writes the recommended roll
  ---
  duration_ms: 12.310769
  ...
# Subtest: picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
ok 2179 - picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
  ---
  duration_ms: 3.548823
  ...
# Subtest: picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
ok 2180 - picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
  ---
  duration_ms: 6.372455
  ...
# Subtest: picker-single recurring P4 past the limit refuses and keeps the picker open
ok 2181 - picker-single recurring P4 past the limit refuses and keeps the picker open
  ---
  duration_ms: 12.373651
  ...
# Subtest: picker-single stale tasks refuse and re-render the decay preview
ok 2182 - picker-single stale tasks refuse and re-render the decay preview
  ---
  duration_ms: 12.053709
  ...
# Subtest: picker-single Ctrl+R on the card re-rolls the recommendation date
ok 2183 - picker-single Ctrl+R on the card re-rolls the recommendation date
  ---
  duration_ms: 2.931356
  ...
# Subtest: picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
ok 2184 - picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
  ---
  duration_ms: 2.131398
  ...
# Subtest: picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
ok 2185 - picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
  ---
  duration_ms: 12.476515
  ...
# Subtest: picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
ok 2186 - picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
  ---
  duration_ms: 12.035806
  ...
# Subtest: picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
ok 2187 - picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
  ---
  duration_ms: 12.554314
  ...
# Subtest: picker-counted Ctrl+Enter refuses when a target line changed
ok 2188 - picker-counted Ctrl+Enter refuses when a target line changed
  ---
  duration_ms: 11.944991
  ...
# Subtest: picker-counted Ctrl+Enter refuses a recurring cancel batch
ok 2189 - picker-counted Ctrl+Enter refuses a recurring cancel batch
  ---
  duration_ms: 11.745472
  ...
# Subtest: recommended roll on Pending offers a Work Log with the frozen date
ok 2190 - recommended roll on Pending offers a Work Log with the frozen date
  ---
  duration_ms: 1019.204177
  ...
# Subtest: recommended roll blank summary skips the Work Log without a fallback
ok 2191 - recommended roll blank summary skips the Work Log without a fallback
  ---
  duration_ms: 1031.570151
  ...
# Subtest: Ctrl+Enter in the Work Log stage confirms instead of re-rolling
ok 2192 - Ctrl+Enter in the Work Log stage confirms instead of re-rolling
  ---
  duration_ms: 1041.674642
  ...
# Subtest: counted recommended mixed batch logs only eligible roll and decay targets
ok 2193 - counted recommended mixed batch logs only eligible roll and decay targets
  ---
  duration_ms: 1033.676592
  ...
# Subtest: lane commit stamps an open Ready task
ok 2194 - lane commit stamps an open Ready task
  ---
  duration_ms: 2.62974
  ...
# Subtest: lane release stamps an open Next task
ok 2195 - lane release stamps an open Next task
  ---
  duration_ms: 0.418298
  ...
# Subtest: lane without a stamper leaves lines as they were
ok 2196 - lane without a stamper leaves lines as they were
  ---
  duration_ms: 0.17799
  ...
# Subtest: counted property set stamps every rewritten open task
ok 2197 - counted property set stamps every rewritten open task
  ---
  duration_ms: 2.092705
  ...
# Subtest: counted delete-property stamps the rewritten task
ok 2198 - counted delete-property stamps the rewritten task
  ---
  duration_ms: 0.497219
  ...
# Subtest: stamp lands before the suffix after a priority edit on a stamped line
ok 2199 - stamp lands before the suffix after a priority edit on a stamped line
  ---
  duration_ms: 0.486578
  ...
# Subtest: recurring tasks are never stamped
ok 2200 - recurring tasks are never stamped
  ---
  duration_ms: 0.258263
  ...
# Subtest: cancel never stamps
ok 2201 - cancel never stamps
  ---
  duration_ms: 1.049173
  ...
# Subtest: fresh and refresh never go through the end-append writers
ok 2202 - fresh and refresh never go through the end-append writers
  ---
  duration_ms: 0.396867
  ...
# Subtest: counted dependency edit stamps the rewritten parent
ok 2203 - counted dependency edit stamps the rewritten parent
  ---
  duration_ms: 4.441477
  ...
# Subtest: moved tasks are stamped at their destination
ok 2204 - moved tasks are stamped at their destination
  ---
  duration_ms: 2.672861
  ...
# Subtest: move without a stamper leaves lines as they were
ok 2205 - move without a stamper leaves lines as they were
  ---
  duration_ms: 0.744371
  ...
# Subtest: refresh row shows the effective interval in task mode
ok 2206 - refresh row shows the effective interval in task mode
  ---
  duration_ms: 0.730524
  ...
# Subtest: refresh row hides without the api and on closed tasks
ok 2207 - refresh row hides without the api and on closed tasks
  ---
  duration_ms: 0.118927
  ...
# Subtest: refresh row covers counted and link modes, including mixed
ok 2208 - refresh row covers counted and link modes, including mixed
  ---
  duration_ms: 0.252633
  ...
# Subtest: refresh value items offer presets and use default
ok 2209 - refresh value items offer presets and use default
  ---
  duration_ms: 0.675981
  ...
# Subtest: setRefreshLine stamps and sets or clears the interval
ok 2210 - setRefreshLine stamps and sets or clears the interval
  ---
  duration_ms: 0.390365
  ...
# Subtest: 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
ok 2211 - 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
  ---
  duration_ms: 7.156772
  ...
# Subtest: Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
ok 2212 - Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
  ---
  duration_ms: 2.744068
  ...
# Subtest: filtering expands matches, collapse state survives clearing, and hidden marks still submit
ok 2213 - filtering expands matches, collapse state survives clearing, and hidden marks still submit
  ---
  duration_ms: 3.934351
  ...
# Subtest: group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
ok 2214 - group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
  ---
  duration_ms: 1.280334
  ...
# Subtest: Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
ok 2215 - Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
  ---
  duration_ms: 0.591378
  ...
# Subtest: Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
ok 2216 - Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
  ---
  duration_ms: 1.860892
  ...
# Subtest: the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
ok 2217 - the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
  ---
  duration_ms: 0.851255
  ...
# Subtest: unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
ok 2218 - unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
  ---
  duration_ms: 0.705888
  ...
# Subtest: card model builds stable rows, scope metadata, and an existing recommendation
ok 2219 - card model builds stable rows, scope metadata, and an existing recommendation
  ---
  duration_ms: 7.66938
  ...
# Subtest: explicit preview builder matches writer rolls and deduplicates linked targets
ok 2220 - explicit preview builder matches writer rolls and deduplicates linked targets
  ---
  duration_ms: 0.767494
  ...
# Subtest: counted and linked card models report real target counts and mixed values
ok 2221 - counted and linked card models report real target counts and mixed values
  ---
  duration_ms: 4.095469
  ...
# Subtest: priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
ok 2222 - priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
  ---
  duration_ms: 1.987353
  ...
# Subtest: Escape, bare q, and Ctrl+[ close the card; nothing else does
ok 2223 - Escape, bare q, and Ctrl+[ close the card; nothing else does
  ---
  duration_ms: 0.831558
  ...
# Subtest: close keys never fire during composition or inside a text field
ok 2224 - close keys never fire during composition or inside a text field
  ---
  duration_ms: 1.055605
  ...
# Subtest: unavailable actions, input composition, and repeats stay safe
ok 2225 - unavailable actions, input composition, and repeats stay safe
  ---
  duration_ms: 1.621425
  ...
# Subtest: key resolver table covers lane state, API availability, and modifier guards
ok 2226 - key resolver table covers lane state, API availability, and modifier guards
  ---
  duration_ms: 1.159704
  ...
# Subtest: recurring cancellation and blocked lanes expose reasons instead of writes
ok 2227 - recurring cancellation and blocked lanes expose reasons instead of writes
  ---
  duration_ms: 0.68083
  ...
# Subtest: identity keys distinguish linked notes that share a line number
ok 2228 - identity keys distinguish linked notes that share a line number
  ---
  duration_ms: 1.467622
  ...
# Subtest: planScheduleReview opens for a bare date and skips when reason is known without Work Log
ok 2229 - planScheduleReview opens for a bare date and skips when reason is known without Work Log
  ---
  duration_ms: 0.831517
  ...
# Subtest: planScheduleReview counts unique tasks when Task Links repeat a target
ok 2230 - planScheduleReview counts unique tasks when Task Links repeat a target
  ---
  duration_ms: 0.289112
  ...
# Subtest: bare date on Ready opens a reason-only review and writes nothing until Enter
ok 2231 - bare date on Ready opens a reason-only review and writes nothing until Enter
  ---
  duration_ms: 19.312626
  ...
# Subtest: typed reason and blank reason on an existing Schedule Log keep per-target rules
ok 2232 - typed reason and blank reason on an existing Schedule Log keep per-target rules
  ---
  duration_ms: 7.709747
  ...
# Subtest: Ready vs Next vs Pending: only Next/Pending show Work summary
ok 2233 - Ready vs Next vs Pending: only Next/Pending show Work summary
  ---
  duration_ms: 12.547912
  ...
# Subtest: inline reason on Ready dispatches immediately; on Next it still reviews Work summary
ok 2234 - inline reason on Ready dispatches immediately; on Next it still reviews Work summary
  ---
  duration_ms: 6.954346
  ...
# Subtest: Tab moves from Reason to Work summary and Enter commits from either field
ok 2235 - Tab moves from Reason to Work summary and Enter commits from either field
  ---
  duration_ms: 2.841573
  ...
# Subtest: Back and Escape at both review fields write nothing
ok 2236 - Back and Escape at both review fields write nothing
  ---
  duration_ms: 3.271856
  ...
# Subtest: a target changed during review refuses with no write
ok 2237 - a target changed during review refuses with no write
  ---
  duration_ms: 4.918409
  ...
# Subtest: counted mixed targets share one review and one adapter call
ok 2238 - counted mixed targets share one review and one adapter call
  ---
  duration_ms: 4.335746
  ...
# Subtest: linked notes with equal line numbers both qualify
ok 2239 - linked notes with equal line numbers both qualify
  ---
  duration_ms: 4.323853
  ...
# Subtest: project lifecycle review names propagation and still writes once
ok 2240 - project lifecycle review names propagation and still writes once
  ---
  duration_ms: 3.049882
  ...
# Subtest: priority picks still skip the combined review and keep Work Log-only prompts
ok 2241 - priority picks still skip the combined review and keep Work Log-only prompts
  ---
  duration_ms: 1.987103
  ...
# Subtest: a typed date from the card's schedule row uses the combined review
ok 2242 - a typed date from the card's schedule row uses the combined review
  ---
  duration_ms: 2.077986
  ...
# Subtest: scheduling a Pending task goes straight to the combined review, never serial prompts
ok 2243 - scheduling a Pending task goes straight to the combined review, never serial prompts
  ---
  duration_ms: 1.380555
  ...
# Subtest: classic parser keeps ISO, M/D, and signed units and ignores concise forms
ok 2244 - classic parser keeps ISO, M/D, and signed units and ignores concise forms
  ---
  duration_ms: 1.820134
  ...
# Subtest: typed schedule resolver covers bare days, units, weekdays, and inline reasons
ok 2245 - typed schedule resolver covers bare days, units, weekdays, and inline reasons
  ---
  duration_ms: 1.369243
  ...
# Subtest: weekdays resolve to the next occurrence strictly after today
ok 2246 - weekdays resolve to the next occurrence strictly after today
  ---
  duration_ms: 0.157922
  ...
# Subtest: invalid leap dates, end-of-month offsets, and December rollover
ok 2247 - invalid leap dates, end-of-month offsets, and December rollover
  ---
  duration_ms: 0.360167
  ...
# Subtest: negative, overflow, malformed, and preset-filter queries are rejected without dates
ok 2248 - negative, overflow, malformed, and preset-filter queries are rejected without dates
  ---
  duration_ms: 0.197257
  ...
# Subtest: DST local-calendar arithmetic stays on calendar days in America/New_York
ok 2249 - DST local-calendar arithmetic stays on calendar days in America/New_York
  ---
  duration_ms: 84.789122
  ...
# Subtest: Task Card date stage previews weekday, ISO, relative distance, and rollover year
ok 2250 - Task Card date stage previews weekday, ISO, relative distance, and rollover year
  ---
  duration_ms: 19.499452
  ...
# Subtest: inline reason is preserved on the preview and skips the reason stage
ok 2251 - inline reason is preserved on the preview and skips the reason stage
  ---
  duration_ms: 13.667911
  ...
# Subtest: Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
ok 2252 - Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
  ---
  duration_ms: 5.312521
  ...
# Subtest: Shift+Enter on a Ready task commits in four gestures without a Work Log
ok 2253 - Shift+Enter on a Ready task commits in four gestures without a Work Log
  ---
  duration_ms: 2.878444
  ...
# Subtest: invalid typed dates render an error preview and do not write
ok 2254 - invalid typed dates render an error preview and do not write
  ---
  duration_ms: 2.224907
  ...
# Subtest: the card's schedule stage always uses the concise resolver
ok 2255 - the card's schedule stage always uses the concise resolver
  ---
  duration_ms: 1.636734
  ...
# Subtest: tomorrow stays a preset filter and is not stolen as a typed date
ok 2256 - tomorrow stays a preset filter and is not stolen as a typed date
  ---
  duration_ms: 1.470538
  ...
# Subtest: mixed Task Links preview one date and freeze that action with the inline reason
ok 2257 - mixed Task Links preview one date and freeze that action with the inline reason
  ---
  duration_ms: 7.53826
  ...
# Subtest: Ctrl+Enter still takes the recommended roll from the Task Card date stage
ok 2258 - Ctrl+Enter still takes the recommended roll from the Task Card date stage
  ---
  duration_ms: 2.738106
  ...
# Subtest: Modal harness models Obsidian 1.14 attachment and idempotent close
ok 2259 - Modal harness models Obsidian 1.14 attachment and idempotent close
  ---
  duration_ms: 2.040775
  ...
# Subtest: styles share key-card tokens and compact Task Card dimensions
ok 2260 - styles share key-card tokens and compact Task Card dimensions
  ---
  duration_ms: 0.384394
  ...
# Subtest: card renderer paints header, banner, strip, stable rows, more, and footer from the model
ok 2261 - card renderer paints header, banner, strip, stable rows, more, and footer from the model
  ---
  duration_ms: 13.263369
  ...
# Subtest: renderer does not consume randomness or invent recommendation data
ok 2262 - renderer does not consume randomness or invent recommendation data
  ---
  duration_ms: 2.830183
  ...
# Subtest: no-recommendation, cancel, mixed, long text, missing API, and error states render
ok 2263 - no-recommendation, cancel, mixed, long text, missing API, and error states render
  ---
  duration_ms: 7.090055
  ...
# Subtest: counted and linked cards disclose mixed values and Task Link notes
ok 2264 - counted and linked cards disclose mixed values and Task Link notes
  ---
  duration_ms: 6.383574
  ...
# Subtest: Ctrl+Shift+P always opens the Task Card, never the classic property list
ok 2265 - Ctrl+Shift+P always opens the Task Card, never the classic property list
  ---
  duration_ms: 6.711983
  ...
# Subtest: the plugin carries no Task Card pilot setting, date gate, or classic preference
ok 2266 - the plugin carries no Task Card pilot setting, date gate, or classic preference
  ---
  duration_ms: 19.48794
  ...
# Subtest: a leftover persisted taskCard flag is ignored and never rewritten
ok 2267 - a leftover persisted taskCard flag is ignored and never rewritten
  ---
  duration_ms: 6.038557
  ...
# Subtest: palette command is named Task card (set properties)
ok 2268 - palette command is named Task card (set properties)
  ---
  duration_ms: 10.458584
  ...
# Subtest: Task Card opens the compact card with dialog semantics and a close control
ok 2269 - Task Card opens the compact card with dialog semantics and a close control
  ---
  duration_ms: 1.333786
  ...
# Subtest: a More row opens that property's value stage, never a filter list, and Back restores the card
ok 2270 - a More row opens that property's value stage, never a filter list, and Back restores the card
  ---
  duration_ms: 3.179108
  ...
# Subtest: after open the actions list, not the Close button, has focus
ok 2271 - after open the actions list, not the Close button, has focus
  ---
  duration_ms: 4.180079
  ...
# Subtest: clicking card text keeps the card key router active exactly once
ok 2272 - clicking card text keeps the card key router active exactly once
  ---
  duration_ms: 16.874773
  ...
# Subtest: Ready card writes close from a key, P1 click, recommendations, and Alt+N
ok 2273 - Ready card writes close from a key, P1 click, recommendations, and Alt+N
  ---
  duration_ms: 7.712581
  ...
# Subtest: Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
ok 2274 - Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
  ---
  duration_ms: 4.763694
  ...
# Subtest: Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
ok 2275 - Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
  ---
  duration_ms: 3.07578
  ...
# Subtest: Ctrl+R recomputes and repaints the card recommendation
ok 2276 - Ctrl+R recomputes and repaints the card recommendation
  ---
  duration_ms: 1.370196
  ...
# Subtest: Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
ok 2277 - Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
  ---
  duration_ms: 14.428303
  ...
# Subtest: Task Link opens focused while resolving and consumes keys without replay
ok 2278 - Task Link opens focused while resolving and consumes keys without replay
  ---
  duration_ms: 5.558811
  ...
# Subtest: Task Link count replacement and source edits invalidate old resolutions
ok 2279 - Task Link count replacement and source edits invalidate old resolutions
  ---
  duration_ms: 1.477932
  ...
# Subtest: Task Link resolution failure and plugin unload close their shells
ok 2280 - Task Link resolution failure and plugin unload close their shells
  ---
  duration_ms: 1.993406
  ...
# Subtest: direct Depends on entry opens the dependency stage without painting the card or the list
ok 2281 - direct Depends on entry opens the dependency stage without painting the card or the list
  ---
  duration_ms: 1.436311
  ...
# Subtest: a direct stage for an unconfigured property closes instead of leaving an empty modal
ok 2282 - a direct stage for an unconfigured property closes instead of leaving an empty modal
  ---
  duration_ms: 0.356791
  ...
# Subtest: a refused direct stage closes instead of landing on a card or a list
ok 2283 - a refused direct stage closes instead of landing on a card or a list
  ---
  duration_ms: 0.724162
  ...
# Subtest: priority gesture writes the frozen date and duplicate dispatch is single-flight
ok 2284 - priority gesture writes the frozen date and duplicate dispatch is single-flight
  ---
  duration_ms: 4.469893
  ...
# Subtest: pending priority action passes its card preview through the Work Log adapter
ok 2285 - pending priority action passes its card preview through the Work Log adapter
  ---
  duration_ms: 1.077767
  ...
# Subtest: Task Link priority action refuses a stale cross-note preflight before writes
ok 2286 - Task Link priority action refuses a stale cross-note preflight before writes
  ---
  duration_ms: 4.384969
  ...
# Subtest: Task Link priority action rolls back earlier note writes after a later write fails
ok 2287 - Task Link priority action rolls back earlier note writes after a later write fails
  ---
  duration_ms: 1.830213
  ...
# Subtest: Task Link transaction reports a cleanup failure without implying global undo
ok 2288 - Task Link transaction reports a cleanup failure without implying global undo
  ---
  duration_ms: 0.945645
  ...
# Subtest: selected-property deletion uses the existing writer; other card rows stay non-deletable
ok 2289 - selected-property deletion uses the existing writer; other card rows stay non-deletable
  ---
  duration_ms: 2.028833
  ...
# Subtest: failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
ok 2290 - failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
  ---
  duration_ms: 1.142541
  ...
# Subtest: a refused deletion rebuilds the card from the refreshed line
ok 2291 - a refused deletion rebuilds the card from the refreshed line
  ---
  duration_ms: 1.25152
  ...
# Subtest: 0 deletes only priority and keeps the scheduled field byte-for-byte
ok 2292 - 0 deletes only priority and keeps the scheduled field byte-for-byte
  ---
  duration_ms: 1.327013
  ...
# Subtest: card keys pressed on a priority radio or the banner reach the resolver exactly once
ok 2293 - card keys pressed on a priority radio or the banner reach the resolver exactly once
  ---
  duration_ms: 2.558904
  ...
# Subtest: held or composing Enter on a radio or the banner never writes
ok 2294 - held or composing Enter on a radio or the banner never writes
  ---
  duration_ms: 3.22154
  ...
# Subtest: Escape, q, Q, and Ctrl+[ close the card without writing
ok 2295 - Escape, q, Q, and Ctrl+[ close the card without writing
  ---
  duration_ms: 3.652652
  ...
# Subtest: Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
ok 2296 - Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
  ---
  duration_ms: 0.744641
  ...
# Subtest: repeated close keys and a second close() are harmless
ok 2297 - repeated close keys and a second close() are harmless
  ---
  duration_ms: 1.082827
  ...
# Subtest: composition never closes the card or a stage
ok 2298 - composition never closes the card or a stage
  ---
  duration_ms: 1.106632
  ...
# Subtest: q typed into a stage's text field never closes the modal
ok 2299 - q typed into a stage's text field never closes the modal
  ---
  duration_ms: 1.029476
  ...
# Subtest: Ctrl+[ closes from a focused date field without writing
ok 2300 - Ctrl+[ closes from a focused date field without writing
  ---
  duration_ms: 1.036789
  ...
# Subtest: Ctrl+[ closes the schedule review from its Reason and Work summary fields
ok 2301 - Ctrl+[ closes the schedule review from its Reason and Work summary fields
  ---
  duration_ms: 10.513047
  ...
# Subtest: Ctrl+[ closes the summary-only schedule-work-log stage without writing
ok 2302 - Ctrl+[ closes the summary-only schedule-work-log stage without writing
  ---
  duration_ms: 0.977186
  ...
# Subtest: Ctrl+[ closes the lane-release Work summary without writing
ok 2303 - Ctrl+[ closes the lane-release Work summary without writing
  ---
  duration_ms: 0.983928
  ...
# Subtest: q closes from a focused More row and from the Close button
ok 2304 - q closes from a focused More row and from the Close button
  ---
  duration_ms: 1.468703
  ...
# Subtest: Ctrl+[ closes from focused card controls, the Back button, and the modal frame
ok 2305 - Ctrl+[ closes from focused card controls, the Back button, and the modal frame
  ---
  duration_ms: 2.184651
  ...
# Subtest: a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
ok 2306 - a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
  ---
  duration_ms: 5.859455
  ...
# Subtest: a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
ok 2307 - a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
  ---
  duration_ms: 2.725773
  ...
# Subtest: a direct dependency stage closes on Ctrl+[ but keeps q as typed text
ok 2308 - a direct dependency stage closes on Ctrl+[ but keeps q as typed text
  ---
  duration_ms: 0.609453
  ...
# Subtest: q and Ctrl+[ are not global closes: other modals and the decay card ignore them
ok 2309 - q and Ctrl+[ are not global closes: other modals and the decay card ignore them
  ---
  duration_ms: 0.851084
  ...
# Subtest: missing freshness API disables Review every with an honest reason
ok 2310 - missing freshness API disables Review every with an honest reason
  ---
  duration_ms: 0.631666
  ...
# Subtest: child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
ok 2311 - child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
  ---
  duration_ms: 1.017052
  ...
# Subtest: decay card keeps its classes and shares key-card tokens
ok 2312 - decay card keeps its classes and shares key-card tokens
  ---
  duration_ms: 0.161999
  ...
# Subtest: decay card footer always names the X drop alias; the trial date is not this gate
ok 2313 - decay card footer always names the X drop alias; the trial date is not this gate
  ---
  duration_ms: 0.297769
  ...
# Subtest: task card level chips reuse the shared priority mark when available
ok 2314 - task card level chips reuse the shared priority mark when available
  ---
  duration_ms: 0.94794
  ...
# Subtest: task card labels are unchanged without the priority mark api
ok 2315 - task card labels are unchanged without the priority mark api
  ---
  duration_ms: 2.932729
  ...
# Subtest: manifest order is authoritative and fragments share one lexical scope
ok 2316 - manifest order is authoritative and fragments share one lexical scope
  ---
  duration_ms: 121.031615
  ...
# Subtest: builds are deterministic and build:check is read-only on success
ok 2317 - builds are deterministic and build:check is read-only on success
  ---
  duration_ms: 168.3036
  ...
# Subtest: read-only check rejects changed fragments and edited generated output
ok 2318 - read-only check rejects changed fragments and edited generated output
  ---
  duration_ms: 163.541762
  ...
# Subtest: check rejects a missing generated bundle without writing it
ok 2319 - check rejects a missing generated bundle without writing it
  ---
  duration_ms: 51.62736
  ...
# Subtest: fragment line limit is enforced before writing output
ok 2320 - fragment line limit is enforced before writing output
  ---
  duration_ms: 1.752825
  ...
# Subtest: fragment syntax errors are rejected before writing output
ok 2321 - fragment syntax errors are rejected before writing output
  ---
  duration_ms: 26.605938
  ...
# Subtest: malformed, empty, duplicate, and traversal manifests are rejected read-only
    # Subtest: invalid JSON
    ok 1 - invalid JSON
      ---
      duration_ms: 3.488799
      ...
    # Subtest: empty manifest
    ok 2 - empty manifest
      ---
      duration_ms: 0.819243
      ...
    # Subtest: non-array manifest
    ok 3 - non-array manifest
      ---
      duration_ms: 0.631596
      ...
    # Subtest: duplicate entries
    ok 4 - duplicate entries
      ---
      duration_ms: 27.257421
      ...
    # Subtest: traversal entry
    ok 5 - traversal entry
      ---
      duration_ms: 0.632057
      ...
    # Subtest: absolute entry
    ok 6 - absolute entry
      ---
      duration_ms: 0.489605
      ...
    1..6
ok 2322 - malformed, empty, duplicate, and traversal manifests are rejected read-only
  ---
  duration_ms: 34.275578
  ...
# Subtest: missing and omitted fragments are rejected read-only
    # Subtest: missing manifest entry
    ok 1 - missing manifest entry
      ---
      duration_ms: 0.504633
      ...
    # Subtest: unlisted JavaScript source
    ok 2 - unlisted JavaScript source
      ---
      duration_ms: 25.753931
      ...
    1..2
ok 2323 - missing and omitted fragments are rejected read-only
  ---
  duration_ms: 26.480958
  ...
# Subtest: escaping fragment symlinks are rejected read-only
ok 2324 - escaping fragment symlinks are rejected read-only
  ---
  duration_ms: 0.973198
  ...
# Subtest: parity comparator identifies changed helper and plugin methods
ok 2325 - parity comparator identifies changed helper and plugin methods
  ---
  duration_ms: 7.896985
  ...
# Subtest: parity comparator accepts a mixin-split helper class but not a changed method or superclass
ok 2326 - parity comparator accepts a mixin-split helper class but not a changed method or superclass
  ---
  duration_ms: 0.428297
  ...
# Subtest: both prompt copies pass the shared fixture table identically
ok 2327 - both prompt copies pass the shared fixture table identically
  ---
  duration_ms: 9.91234
  ...
# Subtest: suggestion is valid, compact, and collision-aware
ok 2328 - suggestion is valid, compact, and collision-aware
  ---
  duration_ms: 0.934083
  ...
# Subtest: rename excludes exactly one old-ID occurrence
ok 2329 - rename excludes exactly one old-ID occurrence
  ---
  duration_ms: 0.282529
  ...
# Subtest: dependency legacy [id::] reuses only valid free IDs
ok 2330 - dependency legacy [id::] reuses only valid free IDs
  ---
  duration_ms: 0.51873
  ...
# Subtest: project conversion keeps the existing suggestBlockIdFromTask
ok 2331 - project conversion keeps the existing suggestBlockIdFromTask
  ---
  duration_ms: 1.234357
  ...
# Subtest: successor SB vectors are unchanged
ok 2332 - successor SB vectors are unchanged
  ---
  duration_ms: 1.290654
  ...
# Subtest: option-bracket ring reads Blocked as a source-only slot ahead of Ready
ok 2333 - option-bracket ring reads Blocked as a source-only slot ahead of Ready
  ---
  duration_ms: 1.130729
  ...
# Subtest: isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
ok 2334 - isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
  ---
  duration_ms: 0.284484
  ...
# Subtest: option-bracket refuses to change a member while its project is Blocked
ok 2335 - option-bracket refuses to change a member while its project is Blocked
  ---
  duration_ms: 2.3629
  ...
# Subtest: tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
ok 2336 - tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
  ---
  duration_ms: 1.239496
  ...
# Subtest: project resident notice reads the inline ^prj date and ignores frontmatter scheduled
ok 2337 - project resident notice reads the inline ^prj date and ignores frontmatter scheduled
  ---
  duration_ms: 0.468695
  ...
# Subtest: findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
ok 2338 - findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
  ---
  duration_ms: 0.279684
  ...
# Subtest: field removal collapses only the exposed span and preserves the rest of the line
ok 2339 - field removal collapses only the exposed span and preserves the rest of the line
  ---
  duration_ms: 0.234628
  ...
# Subtest: vault-path retirement preserves CRLF and a missing final newline
ok 2340 - vault-path retirement preserves CRLF and a missing final newline
  ---
  duration_ms: 0.858599
  ...
# Subtest: Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
ok 2341 - Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
  ---
  duration_ms: 0.585057
  ...
# Subtest: Schedule Log discovery ignores a marker owned by a nested grandchild
ok 2342 - Schedule Log discovery ignores a marker owned by a nested grandchild
  ---
  duration_ms: 0.389934
  ...
# Subtest: Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
ok 2343 - Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
  ---
  duration_ms: 0.427486
  ...
# Subtest: a task with no Schedule Log gets its field retired without any insertion or new marker
ok 2344 - a task with no Schedule Log gets its field retired without any insertion or new marker
  ---
  duration_ms: 0.133966
  ...
# Subtest: Schedule Log entry uses the canonical arrow, dash, and lock bytes
ok 2345 - Schedule Log entry uses the canonical arrow, dash, and lock bytes
  ---
  duration_ms: 0.090293
  ...
# Subtest: retirement stays a no-op for shapes that are not proof of a blocking date
ok 2346 - retirement stays a no-op for shapes that are not proof of a blocking date
  ---
  duration_ms: 0.163322
  ...
# Subtest: cycling Blocked backward to Cancelled retires the date and logs, matching forward
ok 2347 - cycling Blocked backward to Cancelled retires the date and logs, matching forward
  ---
  duration_ms: 3.594582
  ...
# Subtest: single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
ok 2348 - single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
  ---
  duration_ms: 0.949583
  ...
# Subtest: counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
ok 2349 - counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
  ---
  duration_ms: 1.131169
  ...
# Subtest: counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
ok 2350 - counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
  ---
  duration_ms: 0.607089
  ...
# Subtest: transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
ok 2351 - transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
  ---
  duration_ms: 1.800587
  ...
# Subtest: pressing again after Blocked retirement performs an ordinary transition with no further changes
ok 2352 - pressing again after Blocked retirement performs an ordinary transition with no further changes
  ---
  duration_ms: 0.237483
  ...
# Subtest: Alt+] on a date-blocked ^prj recovers open residents in step
ok 2353 - Alt+] on a date-blocked ^prj recovers open residents in step
  ---
  duration_ms: 14.780325
  ...
# Subtest: Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
ok 2354 - Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
  ---
  duration_ms: 1.232853
  ...
# Subtest: planProjectResidentRecoveryEdits recovers when a cross-note id is not open
ok 2355 - planProjectResidentRecoveryEdits recovers when a cross-note id is not open
  ---
  duration_ms: 0.402969
  ...
# Subtest: Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
ok 2356 - Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
  ---
  duration_ms: 1.272349
  ...
# Subtest: Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
ok 2357 - Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
  ---
  duration_ms: 0.873898
  ...
# Subtest: Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
ok 2358 - Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
  ---
  duration_ms: 1.695356
  ...
# Subtest: cycling a transcluded ^prj recovers residents in the source note
ok 2359 - cycling a transcluded ^prj recovers residents in the source note
  ---
  duration_ms: 0.871965
  ...
# Subtest: direct open/done transitions include incomplete statuses without broadening excluded statuses
ok 2360 - direct open/done transitions include incomplete statuses without broadening excluded statuses
  ---
  duration_ms: 1.280204
  ...
# Subtest: Ctrl+Enter block-link selection recognizes live and retired forms
ok 2361 - Ctrl+Enter block-link selection recognizes live and retired forms
  ---
  duration_ms: 2.033472
  ...
# Subtest: Pomodoro child ownership is status-neutral and bounded by contiguous list structure
ok 2362 - Pomodoro child ownership is status-neutral and bounded by contiguous list structure
  ---
  duration_ms: 0.778416
  ...
# Subtest: daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
ok 2363 - daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
  ---
  duration_ms: 0.277319
  ...
# Subtest: parsePomodoroEntryLineParts reads placeholder and range names conservatively
ok 2364 - parsePomodoroEntryLineParts reads placeholder and range names conservatively
  ---
  duration_ms: 0.805878
  ...
# Subtest: formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
ok 2365 - formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
  ---
  duration_ms: 0.154565
  ...
# Subtest: Pomodoro bullet toggle accepts empty indented list items
ok 2366 - Pomodoro bullet toggle accepts empty indented list items
  ---
  duration_ms: 0.280054
  ...
# Subtest: Pomodoro bullet toggle rejects non-empty or out-of-section bullets
ok 2367 - Pomodoro bullet toggle rejects non-empty or out-of-section bullets
  ---
  duration_ms: 0.374465
  ...
# Subtest: Pomodoro bullet toggle reverses only empty open childless placeholders
ok 2368 - Pomodoro bullet toggle reverses only empty open childless placeholders
  ---
  duration_ms: 0.481098
  ...
# Subtest: Pomodoro bullet toggle reverses named empty open childless placeholders
ok 2369 - Pomodoro bullet toggle reverses named empty open childless placeholders
  ---
  duration_ms: 0.380557
  ...
# Subtest: Pomodoro bullet toggle round trips and normalizes child indentation
ok 2370 - Pomodoro bullet toggle round trips and normalizes child indentation
  ---
  duration_ms: 0.208759
  ...
# Subtest: Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
ok 2371 - Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
  ---
  duration_ms: 0.148794
  ...
# Subtest: Pomodoro toggle key gate does not shadow bare Option bracket cycling
ok 2372 - Pomodoro toggle key gate does not shadow bare Option bracket cycling
  ---
  duration_ms: 0.171327
  ...
# Subtest: Pomodoro toggle command is daily-only and places the cursor for both directions
ok 2373 - Pomodoro toggle command is daily-only and places the cursor for both directions
  ---
  duration_ms: 0.525703
  ...
# Subtest: Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
ok 2374 - Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
  ---
  duration_ms: 0.31996
  ...
# Subtest: Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
ok 2375 - Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
  ---
  duration_ms: 1.970091
  ...
# Subtest: Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
ok 2376 - Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
  ---
  duration_ms: 22.923417
  ...
# Subtest: Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
ok 2377 - Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
  ---
  duration_ms: 1.780109
  ...
# Subtest: Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
ok 2378 - Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
  ---
  duration_ms: 0.717951
  ...
# Subtest: Ctrl+Enter closing the local line over an already-closed target does not write it a second time
ok 2379 - Ctrl+Enter closing the local line over an already-closed target does not write it a second time
  ---
  duration_ms: 2.757133
  ...
# Subtest: Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
ok 2380 - Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
  ---
  duration_ms: 1.006531
  ...
# Subtest: Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
ok 2381 - Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
  ---
  duration_ms: 2.367549
  ...
# Subtest: Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
ok 2382 - Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
  ---
  duration_ms: 0.666853
  ...
# Subtest: Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
ok 2383 - Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
  ---
  duration_ms: 0.834283
  ...
# Subtest: Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
ok 2384 - Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
  ---
  duration_ms: 0.919535
  ...
# Subtest: Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
ok 2385 - Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
  ---
  duration_ms: 0.910107
  ...
# Subtest: getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
ok 2386 - getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
  ---
  duration_ms: 0.520273
  ...
# Subtest: Ctrl+Enter close continues the walk with complete after finalize ran
ok 2387 - Ctrl+Enter close continues the walk with complete after finalize ran
  ---
  duration_ms: 12.010386
  ...
# Subtest: Ctrl+Enter close continues only after transclusion propagation landed
ok 2388 - Ctrl+Enter close continues only after transclusion propagation landed
  ---
  duration_ms: 13.371265
  ...
# Subtest: Ctrl+Enter reopen settles the walk with null
ok 2389 - Ctrl+Enter reopen settles the walk with null
  ---
  duration_ms: 11.450397
  ...
# Subtest: Ctrl+Enter swallows the key with no write while the walk is busy
ok 2390 - Ctrl+Enter swallows the key with no write while the walk is busy
  ---
  duration_ms: 11.146307
  ...
# Subtest: Ctrl+Enter with a null capture behaves exactly like today
ok 2391 - Ctrl+Enter with a null capture behaves exactly like today
  ---
  duration_ms: 11.424718
  ...
# Subtest: Ctrl+Enter with nav v2 or no nav keeps today's behavior
ok 2392 - Ctrl+Enter with nav v2 or no nav keeps today's behavior
  ---
  duration_ms: 22.210598
  ...
# Subtest: Ctrl+Enter lets the checklist claim win before capturing
ok 2393 - Ctrl+Enter lets the checklist claim win before capturing
  ---
  duration_ms: 0.745543
  ...
# Subtest: Ctrl+Enter settles the walk with null when the toggle rejects
ok 2394 - Ctrl+Enter settles the walk with null when the toggle rejects
  ---
  duration_ms: 11.123373
  ...
# Subtest: Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
ok 2395 - Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
  ---
  duration_ms: 4.456937
  ...
# Subtest: eligible Tasks demotions prompt in project and non-project notes
ok 2396 - eligible Tasks demotions prompt in project and non-project notes
  ---
  duration_ms: 3.3785
  ...
# Subtest: selectable headings skip YAML, fences, empty titles, and Tasks
ok 2397 - selectable headings skip YAML, fences, empty titles, and Tasks
  ---
  duration_ms: 0.928492
  ...
# Subtest: duplicate heading identities stay distinct and route to the chosen occurrence
ok 2398 - duplicate heading identities stay distinct and route to the chosen occurrence
  ---
  duration_ms: 1.044764
  ...
# Subtest: demotion picker defaults and typed names resolve without synthetic duplicates
ok 2399 - demotion picker defaults and typed names resolve without synthetic duplicates
  ---
  duration_ms: 1.900327
  ...
# Subtest: picker keyboard state wraps, clamps, and refuses invalid Enter
ok 2400 - picker keyboard state wraps, clamps, and refuses invalid Enter
  ---
  duration_ms: 0.364606
  ...
# Subtest: new-section formatting keeps extra blanks, final newlines, and nested children
ok 2401 - new-section formatting keeps extra blanks, final newlines, and nested children
  ---
  duration_ms: 0.810668
  ...
# Subtest: existing-section insertion works before and after the source on CRLF-backed editors
ok 2402 - existing-section insertion works before and after the source on CRLF-backed editors
  ---
  duration_ms: 2.925575
  ...
# Subtest: command opens one picker, writes only on accept, and restores cursor plus center
ok 2403 - command opens one picker, writes only on accept, and restores cursor plus center
  ---
  duration_ms: 0.703273
  ...
# Subtest: pointer activation, Escape, and double-submit protection leave a consistent note
ok 2404 - pointer activation, Escape, and double-submit protection leave a consistent note
  ---
  duration_ms: 1.081995
  ...
# Subtest: stale document, changed editor, or missing heading notice without writing
ok 2405 - stale document, changed editor, or missing heading notice without writing
  ---
  duration_ms: 2.131919
  ...
# Subtest: dependency normalizer writes path-qualified IDs and is idempotent
ok 2406 - dependency normalizer writes path-qualified IDs and is idempotent
  ---
  duration_ms: 1.98013
  ...
# Subtest: Tasks-generated IDs become local block IDs when none exists
ok 2407 - Tasks-generated IDs become local block IDs when none exists
  ---
  duration_ms: 0.703654
  ...
# Subtest: note rename rewrites target IDs and yields exact propagation mappings
ok 2408 - note rename rewrites target IDs and yields exact propagation mappings
  ---
  duration_ms: 0.274423
  ...
# Subtest: note rename also rewrites same-file dependsOn references
ok 2409 - note rename also rewrites same-file dependsOn references
  ---
  duration_ms: 0.227124
  ...
# Subtest: dependency normalization skips unsupported paths and fenced examples
ok 2410 - dependency normalization skips unsupported paths and fenced examples
  ---
  duration_ms: 0.325251
  ...
# Subtest: blocked-dependent planner matches the CLI dependency truth table
ok 2411 - blocked-dependent planner matches the CLI dependency truth table
  ---
  duration_ms: 2.417554
  ...
# Subtest: blocked-dependent edits preserve EOLs and skip stale lines idempotently
ok 2412 - blocked-dependent edits preserve EOLs and skip stale lines idempotently
  ---
  duration_ms: 0.889218
  ...
# Subtest: project recovery strips resident tags and works without freshness v12
ok 2413 - project recovery strips resident tags and works without freshness v12
  ---
  duration_ms: 1.50381
  ...
# Subtest: recovery passes daily-note and Today skip flags to ledger freshness
ok 2414 - recovery passes daily-note and Today skip flags to ledger freshness
  ---
  duration_ms: 0.416395
  ...
# Subtest: normalization mappings propagate to every dependent file
ok 2415 - normalization mappings propagate to every dependent file
  ---
  duration_ms: 1.113626
  ...
# Subtest: runtime normalizer skips unsupported paths with one informative notice
ok 2416 - runtime normalizer skips unsupported paths with one informative notice
  ---
  duration_ms: 0.826758
  ...
# Subtest: rename reconciliation rewrites the target and every dependent
ok 2417 - rename reconciliation rewrites the target and every dependent
  ---
  duration_ms: 0.536895
  ...
# Subtest: editor dependency normalization abandons and reschedules stale snapshots
ok 2418 - editor dependency normalization abandons and reschedules stale snapshots
  ---
  duration_ms: 0.507699
  ...
# Subtest: rename reconciliation abandons and reschedules stale editor snapshots
ok 2419 - rename reconciliation abandons and reschedules stale editor snapshots
  ---
  duration_ms: 0.261289
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 2420 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.800178
  ...
# Subtest: close-time retirement skips Depends-On lines
ok 2421 - close-time retirement skips Depends-On lines
  ---
  duration_ms: 0.961355
  ...
# Subtest: reopen restoration skips Depends-On lines instead of re-embedding them
ok 2422 - reopen restoration skips Depends-On lines instead of re-embedding them
  ---
  duration_ms: 0.500375
  ...
# Subtest: embedded-tree close collection ignores Depends-On lines
ok 2423 - embedded-tree close collection ignores Depends-On lines
  ---
  duration_ms: 0.264765
  ...
# Subtest: Alt-bracket bullet formatting never applies to Depends-On lines
ok 2424 - Alt-bracket bullet formatting never applies to Depends-On lines
  ---
  duration_ms: 0.452674
  ...
# Subtest: Ctrl+Enter on a dependency link closes only the target and runs the recovery
ok 2425 - Ctrl+Enter on a dependency link closes only the target and runs the recovery
  ---
  duration_ms: 1.528347
  ...
# Subtest: Ctrl+Enter on a dependency link reopens only the target, root-only
ok 2426 - Ctrl+Enter on a dependency link reopens only the target, root-only
  ---
  duration_ms: 1.133684
  ...
# Subtest: single and counted Alt-bracket cycle the dependency target under the cursor
ok 2427 - single and counted Alt-bracket cycle the dependency target under the cursor
  ---
  duration_ms: 16.798236
  ...
# Subtest: single and counted Alt-bracket report when the cursor is off every dependency link
ok 2428 - single and counted Alt-bracket report when the cursor is off every dependency link
  ---
  duration_ms: 0.676141
  ...
# Subtest: Ctrl+Enter candidate resolution finds plain links on Depends-On lines
ok 2429 - Ctrl+Enter candidate resolution finds plain links on Depends-On lines
  ---
  duration_ms: 0.186856
  ...
# Subtest: dependency-id normalisation never edits Depends-On lines
ok 2430 - dependency-id normalisation never edits Depends-On lines
  ---
  duration_ms: 0.286036
  ...
# Subtest: note rename rewrites fields while leaving Depends-On lines alone
ok 2431 - note rename rewrites fields while leaving Depends-On lines alone
  ---
  duration_ms: 0.181787
  ...
# Subtest: recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
ok 2432 - recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
  ---
  duration_ms: 1.798694
  ...
# Subtest: cycler freshness: local-fallback rewrite stamps last via injected stamper
ok 2433 - cycler freshness: local-fallback rewrite stamps last via injected stamper
  ---
  duration_ms: 1.58731
  ...
# Subtest: cycler freshness: rewrites without a stamper are unchanged (identity default)
ok 2434 - cycler freshness: rewrites without a stamper are unchanged (identity default)
  ---
  duration_ms: 0.367611
  ...
# Subtest: cycler freshness: a throwing stamper leaves the rewritten line intact
ok 2435 - cycler freshness: a throwing stamper leaves the rewritten line intact
  ---
  duration_ms: 0.144035
  ...
# Subtest: cycler freshness: transcluded rewrite stamps last via injected stamper
ok 2436 - cycler freshness: transcluded rewrite stamps last via injected stamper
  ---
  duration_ms: 0.179443
  ...
# Subtest: cycler freshness: cycling a plain line stamps through the follow-up edit
ok 2437 - cycler freshness: cycling a plain line stamps through the follow-up edit
  ---
  duration_ms: 0.752487
  ...
# Subtest: cycler freshness: Tasks-command rewrite with the expected status is stamped
ok 2438 - cycler freshness: Tasks-command rewrite with the expected status is stamped
  ---
  duration_ms: 0.338456
  ...
# Subtest: cycler freshness: Tasks command that inserts a line never stamps
ok 2439 - cycler freshness: Tasks command that inserts a line never stamps
  ---
  duration_ms: 0.260978
  ...
# Subtest: cycler freshness: Tasks command that deletes the line never stamps the next task
ok 2440 - cycler freshness: Tasks command that deletes the line never stamps the next task
  ---
  duration_ms: 0.231172
  ...
# Subtest: cycler freshness: Tasks command that leaves a different status never stamps
ok 2441 - cycler freshness: Tasks command that leaves a different status never stamps
  ---
  duration_ms: 0.379815
  ...
# Subtest: cycler freshness: cycling without ledger-tools writes no stamp
ok 2442 - cycler freshness: cycling without ledger-tools writes no stamp
  ---
  duration_ms: 0.441944
  ...
# Subtest: cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
ok 2443 - cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
  ---
  duration_ms: 0.187158
  ...
# Subtest: Pomodoro marker helpers normalize every block link and preserve fences and EOLs
ok 2444 - Pomodoro marker helpers normalize every block link and preserve fences and EOLs
  ---
  duration_ms: 3.657421
  ...
# Subtest: completed Pomodoro markers are normalized per occurrence
ok 2445 - completed Pomodoro markers are normalized per occurrence
  ---
  duration_ms: 0.664027
  ...
# Subtest: move-only Pomodoro links require a strict immediate hash directive
ok 2446 - move-only Pomodoro links require a strict immediate hash directive
  ---
  duration_ms: 2.287928
  ...
# Subtest: Pomodoro move-only planner toggles links across additional physical lines
ok 2447 - Pomodoro move-only planner toggles links across additional physical lines
  ---
  duration_ms: 1.626594
  ...
# Subtest: Pomodoro move-only planner round trips exact text and rejects strict non-matches
ok 2448 - Pomodoro move-only planner round trips exact text and rejects strict non-matches
  ---
  duration_ms: 0.722028
  ...
# Subtest: bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
ok 2449 - bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
  ---
  duration_ms: 2.068268
  ...
# Subtest: Pomodoro move-only runtime removes locally and validates additions independently
ok 2450 - Pomodoro move-only runtime removes locally and validates additions independently
  ---
  duration_ms: 1.373832
  ...
# Subtest: Pomodoro move-only runtime protects live lines after asynchronous failures
ok 2451 - Pomodoro move-only runtime protects live lines after asynchronous failures
  ---
  duration_ms: 0.569998
  ...
# Subtest: Pomodoro hash Vim mapping distinguishes bare and explicit repeats
ok 2452 - Pomodoro hash Vim mapping distinguishes bare and explicit repeats
  ---
  duration_ms: 11.630922
  ...
# Subtest: Pomodoro completion marks originals and carries clean live copies
ok 2453 - Pomodoro completion marks originals and carries clean live copies
  ---
  duration_ms: 1.826938
  ...
# Subtest: Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
ok 2454 - Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
  ---
  duration_ms: 1.270705
  ...
# Subtest: Pomodoro completion carries the closed Pomodoro name onto created entries
ok 2455 - Pomodoro completion carries the closed Pomodoro name onto created entries
  ---
  duration_ms: 0.531143
  ...
# Subtest: buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
ok 2456 - buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
  ---
  duration_ms: 0.553567
  ...
# Subtest: buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
ok 2457 - buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
  ---
  duration_ms: 0.284513
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is marked
ok 2458 - buildPomodoroCompletionPlan keeps source order when every carried link is marked
  ---
  duration_ms: 0.237633
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
ok 2459 - buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
  ---
  duration_ms: 0.311044
  ...
# Subtest: Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
ok 2460 - Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
  ---
  duration_ms: 6.554672
  ...
# Subtest: selected Done Pomodoro transclusion reopens only its cross-file root
ok 2461 - selected Done Pomodoro transclusion reopens only its cross-file root
  ---
  duration_ms: 7.081587
  ...
# Subtest: selected same-file Done target reopens root-only in the live editor
ok 2462 - selected same-file Done target reopens root-only in the live editor
  ---
  duration_ms: 1.711909
  ...
# Subtest: selected retired link reopens its root and restores the historical occurrence
ok 2463 - selected retired link reopens its root and restores the historical occurrence
  ---
  duration_ms: 1.342794
  ...
# Subtest: incomplete selected Pomodoro transclusion still closes recursively
ok 2464 - incomplete selected Pomodoro transclusion still closes recursively
  ---
  duration_ms: 2.873675
  ...
# Subtest: Done Pomodoro reopens direct roots and clears only its block-link markers
ok 2465 - Done Pomodoro reopens direct roots and clears only its block-link markers
  ---
  duration_ms: 5.434615
  ...
# Subtest: Done Pomodoro reopen restores its own block reference after reopening direct roots
ok 2466 - Done Pomodoro reopen restores its own block reference after reopening direct roots
  ---
  duration_ms: 1.335309
  ...
# Subtest: Done Pomodoro markers remain when the Todo transition does not occur
ok 2467 - Done Pomodoro markers remain when the Todo transition does not occur
  ---
  duration_ms: 0.440601
  ...
# Subtest: registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
ok 2468 - registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
  ---
  duration_ms: 17.761895
  ...
# Subtest: registered Ctrl+Enter immediately recovers a same-file dependent
ok 2469 - registered Ctrl+Enter immediately recovers a same-file dependent
  ---
  duration_ms: 16.254507
  ...
# Subtest: registered Ctrl+Enter immediately recovers a cross-file dependent
ok 2470 - registered Ctrl+Enter immediately recovers a cross-file dependent
  ---
  duration_ms: 3.788322
  ...
# Subtest: child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
ok 2471 - child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
  ---
  duration_ms: 3.901908
  ...
# Subtest: Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
ok 2472 - Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
  ---
  duration_ms: 1.589925
  ...
# Subtest: selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
ok 2473 - selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
  ---
  duration_ms: 3.360545
  ...
# Subtest: selected unresolved or excluded embedded children are consumed as no-ops
ok 2474 - selected unresolved or excluded embedded children are consumed as no-ops
  ---
  duration_ms: 0.930496
  ...
# Subtest: Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
ok 2475 - Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
  ---
  duration_ms: 2.674375
  ...
# Subtest: Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
ok 2476 - Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
  ---
  duration_ms: 3.288057
  ...
# Subtest: Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
ok 2477 - Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
  ---
  duration_ms: 1.18422
  ...
# Subtest: Pomodoro Work Log note-group collection scopes to direct children and requires descendants
ok 2478 - Pomodoro Work Log note-group collection scopes to direct children and requires descendants
  ---
  duration_ms: 1.147
  ...
# Subtest: Work Log entry body formats as *date* — summary
ok 2479 - Work Log entry body formats as *date* — summary
  ---
  duration_ms: 0.174323
  ...
# Subtest: buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
ok 2480 - buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
  ---
  duration_ms: 0.30888
  ...
# Subtest: planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
ok 2481 - planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
  ---
  duration_ms: 0.534921
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
ok 2482 - planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
  ---
  duration_ms: 0.397329
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
ok 2483 - planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
  ---
  duration_ms: 0.248234
  ...
# Subtest: planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
ok 2484 - planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
  ---
  duration_ms: 0.492791
  ...
# Subtest: planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
ok 2485 - planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
  ---
  duration_ms: 0.531364
  ...
# Subtest: full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
ok 2486 - full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
  ---
  duration_ms: 7.551656
  ...
# Subtest: full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
ok 2487 - full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
  ---
  duration_ms: 1.872704
  ...
# Subtest: full Pomodoro completion keeps two same-task Work Log note sets in source order
ok 2488 - full Pomodoro completion keeps two same-task Work Log note sets in source order
  ---
  duration_ms: 1.557574
  ...
# Subtest: full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
ok 2489 - full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
  ---
  duration_ms: 1.063691
  ...
# Subtest: full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
ok 2490 - full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
  ---
  duration_ms: 1.794646
  ...
# Subtest: full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
ok 2491 - full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
  ---
  duration_ms: 0.666021
  ...
# Subtest: PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
ok 2492 - PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
  ---
  duration_ms: 1.766333
  ...
# Subtest: PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
ok 2493 - PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
  ---
  duration_ms: 1.354235
  ...
# Subtest: PP1 links the emptied project's ^prj as Next and strips \#hide
ok 2494 - PP1 links the emptied project's ^prj as Next and strips \#hide
  ---
  duration_ms: 11.945903
  ...
# Subtest: PP29 closing a child ^prj pulls in its empty parent project
ok 2495 - PP29 closing a child ^prj pulls in its empty parent project
  ---
  duration_ms: 2.922448
  ...
# Subtest: PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
ok 2496 - PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
  ---
  duration_ms: 1.470257
  ...
# Subtest: PP30 keeps the parent untouched while another child or task remains
ok 2497 - PP30 keeps the parent untouched while another child or task remains
  ---
  duration_ms: 1.217344
  ...
# Subtest: PP31 skips missing, ambiguous, and non-project parents
ok 2498 - PP31 skips missing, ambiguous, and non-project parents
  ---
  duration_ms: 1.556441
  ...
# Subtest: PP33 cancellation surfaces the parent without linking it
ok 2499 - PP33 cancellation surfaces the parent without linking it
  ---
  duration_ms: 2.254403
  ...
# Subtest: PP2 and PP3 leave a project with remaining work alone
ok 2500 - PP2 and PP3 leave a project with remaining work alone
  ---
  duration_ms: 2.046637
  ...
# Subtest: PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
ok 2501 - PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
  ---
  duration_ms: 3.198737
  ...
# Subtest: PP6 Sub-projects marker states match display_for_wikilink
ok 2502 - PP6 Sub-projects marker states match display_for_wikilink
  ---
  duration_ms: 1.706557
  ...
# Subtest: PP7 and PP28 keep a future-scheduled ^prj byte-identical
ok 2503 - PP7 and PP28 keep a future-scheduled ^prj byte-identical
  ---
  duration_ms: 1.234877
  ...
# Subtest: PP8 still-blocks a ^prj that waits on another open prerequisite
ok 2504 - PP8 still-blocks a ^prj that waits on another open prerequisite
  ---
  duration_ms: 0.975532
  ...
# Subtest: PP9 already-planned ^prj raises to Next without a new link
ok 2505 - PP9 already-planned ^prj raises to Next without a new link
  ---
  duration_ms: 0.758077
  ...
# Subtest: PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
ok 2506 - PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
  ---
  duration_ms: 3.521351
  ...
# Subtest: PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
ok 2507 - PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
  ---
  duration_ms: 0.832228
  ...
# Subtest: PP14 an id-less last task still pulls in
ok 2508 - PP14 an id-less last task still pulls in
  ---
  duration_ms: 0.363344
  ...
# Subtest: PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
ok 2509 - PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
  ---
  duration_ms: 9.86393
  ...
# Subtest: PP17 one pull-in row wins over project_task
ok 2510 - PP17 one pull-in row wins over project_task
  ---
  duration_ms: 0.602771
  ...
# Subtest: PP18 cancel recovers only
ok 2511 - PP18 cancel recovers only
  ---
  duration_ms: 0.388392
  ...
# Subtest: PP20 unrecognised or unplannable notes never pull in
ok 2512 - PP20 unrecognised or unplannable notes never pull in
  ---
  duration_ms: 0.988246
  ...
# Subtest: PP24 closing an external prerequisite pulls in only when N is empty
ok 2513 - PP24 closing an external prerequisite pulls in only when N is empty
  ---
  duration_ms: 0.874539
  ...
# Subtest: PP25 cascades project_member recovery after a [?] pull-in
ok 2514 - PP25 cascades project_member recovery after a [?] pull-in
  ---
  duration_ms: 1.019847
  ...
# Subtest: PP26 dated recount treats a hidden leftover as remaining work
ok 2515 - PP26 dated recount treats a hidden leftover as remaining work
  ---
  duration_ms: 0.681411
  ...
# Subtest: PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
ok 2516 - PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
  ---
  duration_ms: 1.919244
  ...
# Subtest: successorNoticeText uses the §12.6 pull-in and surfaced copy
ok 2517 - successorNoticeText uses the §12.6 pull-in and surfaced copy
  ---
  duration_ms: 0.485347
  ...
# Subtest: Ctrl+Enter on the last task link inserts the ^prj and rewrites R
ok 2518 - Ctrl+Enter on the last task link inserts the ^prj and rewrites R
  ---
  duration_ms: 10.329436
  ...
# Subtest: PP29 runtime close and reopen use the parent pull-in receipt
ok 2519 - PP29 runtime close and reopen use the parent pull-in receipt
  ---
  duration_ms: 4.434285
  ...
# Subtest: PP18 Alt+[ cancel of the last task surfaces R without linking
ok 2520 - PP18 Alt+[ cancel of the last task surfaces R without linking
  ---
  duration_ms: 17.744011
  ...
# Subtest: PP19 same-day reopen restores R byte-for-byte and takes back the link
ok 2521 - PP19 same-day reopen restores R byte-for-byte and takes back the link
  ---
  duration_ms: 3.125155
  ...
# Subtest: a close in a project that still has work stays inside the gate
ok 2522 - a close in a project that still has work stays inside the gate
  ---
  duration_ms: 1.239967
  ...
# Subtest: P1 path-qualified skip keys: same ^review in another note does not suppress
ok 2523 - P1 path-qualified skip keys: same ^review in another note does not suppress
  ---
  duration_ms: 0.59749
  ...
# Subtest: P3 id-less cascade: stale [?] R recovers resident without [id::]
ok 2524 - P3 id-less cascade: stale [?] R recovers resident without [id::]
  ---
  duration_ms: 0.815547
  ...
# Subtest: P4 frontmatter scheduled validity mirrors Rust
ok 2525 - P4 frontmatter scheduled validity mirrors Rust
  ---
  duration_ms: 2.192506
  ...
# Subtest: P5 recognition mirrors Rust (status/type/prj line)
ok 2526 - P5 recognition mirrors Rust (status/type/prj line)
  ---
  duration_ms: 1.344797
  ...
# Subtest: P6 SUBOPEN blank line stops the marker scan (PP6)
ok 2527 - P6 SUBOPEN blank line stops the marker scan (PP6)
  ---
  duration_ms: 0.352773
  ...
# Subtest: promotion prompts default to Tasks in ordinary and project notes
ok 2528 - promotion prompts default to Tasks in ordinary and project notes
  ---
  duration_ms: 5.650957
  ...
# Subtest: promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
ok 2529 - promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
  ---
  duration_ms: 1.056155
  ...
# Subtest: promotion command writes only on accept and Enter selects Tasks
ok 2530 - promotion command writes only on accept and Enter selects Tasks
  ---
  duration_ms: 2.588671
  ...
# Subtest: promotion removes only genuinely empty source sections
ok 2531 - promotion removes only genuinely empty source sections
  ---
  duration_ms: 1.12627
  ...
# Subtest: promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
ok 2532 - promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
  ---
  duration_ms: 1.080493
  ...
# Subtest: Tasks-only preamble promotions prompt and blank Enter moves into Tasks
ok 2533 - Tasks-only preamble promotions prompt and blank Enter moves into Tasks
  ---
  duration_ms: 0.756624
  ...
# Subtest: plain bullets already in Tasks prompt and blank Enter promotes in place
ok 2534 - plain bullets already in Tasks prompt and blank Enter promotes in place
  ---
  duration_ms: 0.883055
  ...
# Subtest: promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
ok 2535 - promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
  ---
  duration_ms: 0.464837
  ...
# Subtest: always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
ok 2536 - always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
  ---
  duration_ms: 3.205469
  ...
# Could not restore all reopened task references [ 'Broken.md: unreadable' ]
# Could not recover all blocked dependents [
#   'BrokenRead.md: read failed',
#   'Stale.md: line 1 changed before recovery',
#   'BrokenWrite.md: write failed'
# ]
# Subtest: direct Done Tasks task reopens through the metadata-aware fallback
ok 2537 - direct Done Tasks task reopens through the metadata-aware fallback
  ---
  duration_ms: 2.743046
  ...
# Subtest: recursive completion status policy includes Next without broadening excluded statuses
ok 2538 - recursive completion status policy includes Next without broadening excluded statuses
  ---
  duration_ms: 0.25639
  ...
# Subtest: recursive completion closes a Next root and its nested Next descendant
ok 2539 - recursive completion closes a Next root and its nested Next descendant
  ---
  duration_ms: 3.108914
  ...
# Subtest: recursive completion traverses Done parents and skips excluded siblings
ok 2540 - recursive completion traverses Done parents and skips excluded siblings
  ---
  duration_ms: 1.021249
  ...
# Subtest: closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
ok 2541 - closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
  ---
  duration_ms: 1.44056
  ...
# Subtest: reopened-reference restoration is ancestry-aware, conservative, and idempotent
ok 2542 - reopened-reference restoration is ancestry-aware, conservative, and idempotent
  ---
  duration_ms: 1.280405
  ...
# Subtest: retirement preserves task-tree markers and unmarks Pomodoro embeds
ok 2543 - retirement preserves task-tree markers and unmarks Pomodoro embeds
  ---
  duration_ms: 0.362311
  ...
# Subtest: done Pomodoro retirement removes only the matching embedded marker
ok 2544 - done Pomodoro retirement removes only the matching embedded marker
  ---
  duration_ms: 0.292619
  ...
# Subtest: retirement stops at prose boundaries and pairs strikethrough spans
ok 2545 - retirement stops at prose boundaries and pairs strikethrough spans
  ---
  duration_ms: 0.450921
  ...
# Subtest: retired Pomodoro links are not copied into the next Pomodoro
ok 2546 - retired Pomodoro links are not copied into the next Pomodoro
  ---
  duration_ms: 1.206212
  ...
# Subtest: retirement coordinator rewrites active editor and vault notes together
ok 2547 - retirement coordinator rewrites active editor and vault notes together
  ---
  duration_ms: 0.966946
  ...
# Subtest: restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
ok 2548 - restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
  ---
  duration_ms: 1.308106
  ...
# Subtest: close and reopen reference mutations share one serialized queue
ok 2549 - close and reopen reference mutations share one serialized queue
  ---
  duration_ms: 0.262081
  ...
# Subtest: post-close finalizer runs one gated plan before reference retirement
ok 2550 - post-close finalizer runs one gated plan before reference retirement
  ---
  duration_ms: 0.493202
  ...
# Subtest: dependent recovery uses live editor buffers and preserves the cursor
ok 2551 - dependent recovery uses live editor buffers and preserves the cursor
  ---
  duration_ms: 2.824212
  ...
# Subtest: dependent recovery preserves successful siblings across stale and failed notes
ok 2552 - dependent recovery preserves successful siblings across stale and failed notes
  ---
  duration_ms: 1.272538
  ...
# Subtest: no-op vault transforms and irrelevant retirement files avoid process writes
ok 2553 - no-op vault transforms and irrelevant retirement files avoid process writes
  ---
  duration_ms: 0.295323
  ...
# Subtest: ambiguity scans and notices are cached while dependency identity lines stay stable
ok 2554 - ambiguity scans and notices are cached while dependency identity lines stay stable
  ---
  duration_ms: 0.508751
  ...
# Subtest: non-Vim open/done command finalizes the closed task identity
ok 2555 - non-Vim open/done command finalizes the closed task identity
  ---
  duration_ms: 0.394763
  ...
# Subtest: non-Vim open/done command restores the reopened task identity
ok 2556 - non-Vim open/done command restores the reopened task identity
  ---
  duration_ms: 0.333046
  ...
# Subtest: full Pomodoro completion retires embeds only after carry-forward planning
ok 2557 - full Pomodoro completion retires embeds only after carry-forward planning
  ---
  duration_ms: 6.072531
  ...
# Subtest: full Pomodoro completion recovers after a deduplicated multi-target batch
ok 2558 - full Pomodoro completion recovers after a deduplicated multi-target batch
  ---
  duration_ms: 6.950759
  ...
# Subtest: full Pomodoro completion moves a marked same-note link without history
ok 2559 - full Pomodoro completion moves a marked same-note link without history
  ---
  duration_ms: 0.677884
  ...
# Subtest: SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
ok 2560 - SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
  ---
  duration_ms: 22.10736
  ...
# Subtest: SO2–SO5 fan-outs with explicit selection (SO32 twenty)
ok 2561 - SO2–SO5 fan-outs with explicit selection (SO32 twenty)
  ---
  duration_ms: 7.461684
  ...
# Subtest: SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
ok 2562 - SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
  ---
  duration_ms: 1.621295
  ...
# Subtest: SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
ok 2563 - SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
  ---
  duration_ms: 1.333837
  ...
# Subtest: SO stable keys survive insertions/status changes; ambiguous rebinding refused
ok 2564 - SO stable keys survive insertions/status changes; ambiguous rebinding refused
  ---
  duration_ms: 2.065874
  ...
# Subtest: SO picker model, pick normalization, and API detection
ok 2565 - SO picker model, pick normalization, and API detection
  ---
  duration_ms: 0.494134
  ...
# Subtest: SO notice copy for offers (SO20, mixed, failure)
ok 2566 - SO notice copy for offers (SO20, mixed, failure)
  ---
  duration_ms: 0.574527
  ...
# Subtest: reopen takes back the untouched successor link and restores status
ok 2567 - reopen takes back the untouched successor link and restores status
  ---
  duration_ms: 19.723489
  ...
# Subtest: an edited successor bullet survives while its status still restores
ok 2568 - an edited successor bullet survives while its status still restores
  ---
  duration_ms: 3.153791
  ...
# Subtest: an edited successor status line survives while its link is taken back
ok 2569 - an edited successor status line survives while its link is taken back
  ---
  duration_ms: 3.628085
  ...
# Subtest: reopen on a different day leaves successor links alone
ok 2570 - reopen on a different day leaves successor links alone
  ---
  duration_ms: 2.223334
  ...
# Subtest: reopening a task closed without a pass shows no take-back
ok 2571 - reopening a task closed without a pass shows no take-back
  ---
  duration_ms: 1.25218
  ...
# Subtest: Alt+] on a planned prerequisite links its successor
ok 2572 - Alt+] on a planned prerequisite links its successor
  ---
  duration_ms: 8.93257
  ...
# Subtest: Alt+[ into Cancelled recovers its dependents without linking
ok 2573 - Alt+[ into Cancelled recovers its dependents without linking
  ---
  duration_ms: 2.162949
  ...
# Subtest: link close links the unblocked successor into the slot and shows the nav card
ok 2574 - link close links the unblocked successor into the slot and shows the nav card
  ---
  duration_ms: 23.299205
  ...
# Subtest: close with no [id::] performs zero vault reads and shows nothing
ok 2575 - close with no [id::] performs zero vault reads and shows nothing
  ---
  duration_ms: 1.03173
  ...
# Subtest: Warm finalize reads no unrelated note bodies on the real close path
ok 2576 - Warm finalize reads no unrelated note bodies on the real close path
  ---
  duration_ms: 3.383699
  ...
# Subtest: cold fallback still recovers and links without a Tasks cache
ok 2577 - cold fallback still recovers and links without a Tasks cache
  ---
  duration_ms: 3.786558
  ...
# Subtest: recovered-only close reports unblocked without linking (SO4 Esc)
ok 2578 - recovered-only close reports unblocked without linking (SO4 Esc)
  ---
  duration_ms: 2.462751
  ...
# Subtest: walk landing composes a single toast and shows no card
ok 2579 - walk landing composes a single toast and shows no card
  ---
  duration_ms: 8.41384
  ...
# Subtest: nav absent falls back to a plain Notice with no link (SO missing picker)
ok 2580 - nav absent falls back to a plain Notice with no link (SO missing picker)
  ---
  duration_ms: 2.640471
  ...
# Subtest: stale cache heals via re-plan from fresh text (SO30)
ok 2581 - stale cache heals via re-plan from fresh text (SO30)
  ---
  duration_ms: 2.027611
  ...
# Subtest: Pomodoro-line close appends the successor to the created continuation
not ok 2582 - Pomodoro-line close appends the successor to the created continuation
  ---
  duration_ms: 6.130223
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:490:1'
  failureType: 'testCodeFailure'
  error: |-
    Expected values to be strictly equal:
    
    false !== true
    
  code: 'ERR_ASSERTION'
  name: 'AssertionError'
  expected: true
  actual: false
  operator: 'strictEqual'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:529:10)
    async Test.run (node:internal/test_runner/test:980:9)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: completeTaskAtCursor returns the notice and shows nothing itself
ok 2583 - completeTaskAtCursor returns the notice and shows nothing itself
  ---
  duration_ms: 2.887441
  ...
# Subtest: successor apply recovers project residents without ledger v12
ok 2584 - successor apply recovers project residents without ledger v12
  ---
  duration_ms: 12.481164
  ...
# Subtest: SB vectors pin the successor mint pipeline
ok 2585 - SB vectors pin the successor mint pipeline
  ---
  duration_ms: 3.85627
  ...
# Subtest: successor suggester ports the Rust candidate and suffix rules
ok 2586 - successor suggester ports the Rust candidate and suffix rules
  ---
  duration_ms: 1.013505
  ...
# Subtest: successor link form names unique basenames short and the day file always
ok 2587 - successor link form names unique basenames short and the day file always
  ---
  duration_ms: 0.588954
  ...
# Subtest: tasksFromDocuments normalizes vault lines to pool shape
ok 2588 - tasksFromDocuments normalizes vault lines to pool shape
  ---
  duration_ms: 2.569113
  ...
# Subtest: normalizeTasksCacheTask ports every known Tasks shape
ok 2589 - normalizeTasksCacheTask ports every known Tasks shape
  ---
  duration_ms: 0.469125
  ...
# Subtest: buildDependentsIndex keeps first task IDs and groups dependents
ok 2590 - buildDependentsIndex keeps first task IDs and groups dependents
  ---
  duration_ms: 0.233336
  ...
# Subtest: findLiveLinks counts plain, embedded, and deferred links under open entries only
ok 2591 - findLiveLinks counts plain, embedded, and deferred links under open entries only
  ---
  duration_ms: 2.476768
  ...
# Subtest: computeSuccessorAnchors implements closing, slot, inherit, and none
ok 2592 - computeSuccessorAnchors implements closing, slot, inherit, and none
  ---
  duration_ms: 1.029926
  ...
# Subtest: SL1 links the successor right after the predecessor bullet
ok 2593 - SL1 links the successor right after the predecessor bullet
  ---
  duration_ms: 6.342928
  ...
# Subtest: SL3 still-blocked rows count the open prerequisites left
ok 2594 - SL3 still-blocked rows count the open prerequisites left
  ---
  duration_ms: 0.936929
  ...
# Subtest: SL4 future-scheduled dependents stay Blocked with the date row
ok 2595 - SL4 future-scheduled dependents stay Blocked with the date row
  ---
  duration_ms: 0.637316
  ...
# Subtest: SL5 already-planned dependents recover without a duplicate link
ok 2596 - SL5 already-planned dependents recover without a duplicate link
  ---
  duration_ms: 1.277609
  ...
# Subtest: SL6 struck and closed-entry links do not count as planned
ok 2597 - SL6 struck and closed-entry links do not count as planned
  ---
  duration_ms: 1.139365
  ...
# Subtest: SL7 closing anchors create the continuation placeholder
ok 2598 - SL7 closing anchors create the continuation placeholder
  ---
  duration_ms: 2.273029
  ...
# Subtest: SL8 closing anchors append after carried lines in the continuation
ok 2599 - SL8 closing anchors append after carried lines in the continuation
  ---
  duration_ms: 1.076856
  ...
# Subtest: SL9 unplanned predecessors offer at the implicit destination (SO14)
ok 2600 - SL9 unplanned predecessors offer at the implicit destination (SO14)
  ---
  duration_ms: 1.552644
  ...
# Subtest: SL10 missing block IDs mint through the SB rule
ok 2601 - SL10 missing block IDs mint through the SB rule
  ---
  duration_ms: 0.764109
  ...
# Subtest: SL11 project and hidden tasks recover but never link
ok 2602 - SL11 project and hidden tasks recover but never link
  ---
  duration_ms: 9.230089
  ...
# Subtest: PDC1 leaves a dependency-ready resident Blocked while its project still waits
ok 2603 - PDC1 leaves a dependency-ready resident Blocked while its project still waits
  ---
  duration_ms: 2.184951
  ...
# Subtest: PDC2 residents are offered under the project group (SO1)
ok 2604 - PDC2 residents are offered under the project group (SO1)
  ---
  duration_ms: 1.482239
  ...
# Subtest: PDC3 keeps a project resident Blocked when its own prerequisite remains open
ok 2605 - PDC3 keeps a project resident Blocked when its own prerequisite remains open
  ---
  duration_ms: 0.871002
  ...
# Subtest: PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
ok 2606 - PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
  ---
  duration_ms: 1.530993
  ...
# Subtest: SL12 one gesture closing two prerequisites links once with both causes
ok 2607 - SL12 one gesture closing two prerequisites links once with both causes
  ---
  duration_ms: 1.261639
  ...
# Subtest: SL13 chains do not recurse: the dependent's own dependents wait
ok 2608 - SL13 chains do not recurse: the dependent's own dependents wait
  ---
  duration_ms: 0.312957
  ...
# Subtest: SL14 ambiguous basenames link long
ok 2609 - SL14 ambiguous basenames link long
  ---
  duration_ms: 0.334388
  ...
# Subtest: SL15 stale open dependents link and become Next
ok 2610 - SL15 stale open dependents link and become Next
  ---
  duration_ms: 0.350109
  ...
# Subtest: SL16 gates on [id::]: no identity means no lookup and empty rows
ok 2611 - SL16 gates on [id::]: no identity means no lookup and empty rows
  ---
  duration_ms: 0.228937
  ...
# Subtest: SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
ok 2612 - SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
  ---
  duration_ms: 1.681871
  ...
# Subtest: SL18 the kill switch recovers without linking or minting
ok 2613 - SL18 the kill switch recovers without linking or minting
  ---
  duration_ms: 0.307176
  ...
# Subtest: SL19 re-applied closes write nothing and report nothing
ok 2614 - SL19 re-applied closes write nothing and report nothing
  ---
  duration_ms: 0.277489
  ...
# Subtest: SL23 subtasks anchor at their root's link
ok 2615 - SL23 subtasks anchor at their root's link
  ---
  duration_ms: 0.348736
  ...
# Subtest: SL24 later same-name entries take the closing successors
ok 2616 - SL24 later same-name entries take the closing successors
  ---
  duration_ms: 0.481329
  ...
# Subtest: SL25 already-Next planned dependents produce no row
ok 2617 - SL25 already-Next planned dependents produce no row
  ---
  duration_ms: 0.452934
  ...
# Subtest: SL26 inbox successors carry the inbox flag
ok 2618 - SL26 inbox successors carry the inbox flag
  ---
  duration_ms: 0.3039
  ...
# Subtest: SL27 dropped links are never re-linked and recover to Ready
ok 2619 - SL27 dropped links are never re-linked and recover to Ready
  ---
  duration_ms: 0.348044
  ...
# Subtest: SL28 day-file successors name the note, never the bare link
ok 2620 - SL28 day-file successors name the note, never the bare link
  ---
  duration_ms: 0.288541
  ...
# Subtest: slot insertions land after the anchor subtree with its indent
ok 2621 - slot insertions land after the anchor subtree with its indent
  ---
  duration_ms: 0.273632
  ...
# Subtest: closing insertions replace a lone stub child
ok 2622 - closing insertions replace a lone stub child
  ---
  duration_ms: 0.472242
  ...
# Subtest: insertions skip placements with no valid target
ok 2623 - insertions skip placements with no valid target
  ---
  duration_ms: 0.146971
  ...
# Subtest: successorNoticeText implements the §12.6 table
ok 2624 - successorNoticeText implements the §12.6 table
  ---
  duration_ms: 0.50303
  ...
# Subtest: parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
ok 2625 - parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
  ---
  duration_ms: 0.436844
  ...
# Subtest: loadLinkUnblocked stat-caches the config read
ok 2626 - loadLinkUnblocked stat-caches the config read
  ---
  duration_ms: 0.315682
  ...
# Subtest: loadLinkUnblocked treats missing or unreadable config as true
ok 2627 - loadLinkUnblocked treats missing or unreadable config as true
  ---
  duration_ms: 0.56051
  ...
# Subtest: successorPlanConfigPath honors XDG_CONFIG_HOME
ok 2628 - successorPlanConfigPath honors XDG_CONFIG_HOME
  ---
  duration_ms: 0.21999
  ...
# Subtest: todayDailyPath mirrors the ledger daily path
ok 2629 - todayDailyPath mirrors the ledger daily path
  ---
  duration_ms: 0.554979
  ...
# Subtest: normalizeClosedTaskIdentities keeps the anchor root off the match gate
ok 2630 - normalizeClosedTaskIdentities keeps the anchor root off the match gate
  ---
  duration_ms: 0.229618
  ...
# Subtest: ID-less planned roots anchor ID-bearing children without minting IDs
ok 2631 - ID-less planned roots anchor ID-bearing children without minting IDs
  ---
  duration_ms: 0.797372
  ...
# Subtest: successor anchors never guess across roots
ok 2632 - successor anchors never guess across roots
  ---
  duration_ms: 1.34128
  ...
# Subtest: a child with its own live link keeps its own slot
ok 2633 - a child with its own live link keeps its own slot
  ---
  duration_ms: 0.423799
  ...
# Subtest: getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
ok 2634 - getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
  ---
  duration_ms: 0.288421
  ...
# Subtest: countSuccessorBasenames walks the vault set, not the task set
ok 2635 - countSuccessorBasenames walks the vault set, not the task set
  ---
  duration_ms: 0.344187
  ...
# Subtest: the pass threads a richer isInbox into unblocked rows
ok 2636 - the pass threads a richer isInbox into unblocked rows
  ---
  duration_ms: 0.398
  ...
# Subtest: getTaskLinkLaneApi returns the lane only when version and both functions exist
ok 2637 - getTaskLinkLaneApi returns the lane only when version and both functions exist
  ---
  duration_ms: 1.430081
  ...
# Subtest: isTaskLinkLaneLine passes content, line, and path and never throws
ok 2638 - isTaskLinkLaneLine passes content, line, and path and never throws
  ---
  duration_ms: 1.488511
  ...
# Subtest: single Alt+] on a Task Link delegates with exactly { editor, view }
ok 2639 - single Alt+] on a Task Link delegates with exactly { editor, view }
  ---
  duration_ms: 0.628329
  ...
# Subtest: Alt+[ and Alt+] delegate identically; direction is ignored
ok 2640 - Alt+[ and Alt+] delegate identically; direction is ignored
  ---
  duration_ms: 0.402959
  ...
# Subtest: embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
ok 2641 - embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
  ---
  duration_ms: 0.336532
  ...
# Subtest: entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
ok 2642 - entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
  ---
  duration_ms: 3.450017
  ...
# Subtest: counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
ok 2643 - counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
  ---
  duration_ms: 0.867306
  ...
# Subtest: counted dispatch without an explicit repeat leaves the key alone
ok 2644 - counted dispatch without an explicit repeat leaves the key alone
  ---
  duration_ms: 0.313559
  ...
# Subtest: counted range starting elsewhere skips Task Link lines
ok 2645 - counted range starting elsewhere skips Task Link lines
  ---
  duration_ms: 2.091421
  ...
# Subtest: legacy fallback with no api keeps today's behavior
ok 2646 - legacy fallback with no api keeps today's behavior
  ---
  duration_ms: 0.794747
  ...
# Subtest: plain Task Link in an open Pomodoro closes the task root-only and strikes the link
ok 2647 - plain Task Link in an open Pomodoro closes the task root-only and strikes the link
  ---
  duration_ms: 13.649295
  ...
# Subtest: marked plain Task Link drops its marker when struck under Pomodoro ancestry
ok 2648 - marked plain Task Link drops its marker when struck under Pomodoro ancestry
  ---
  duration_ms: 1.5088
  ...
# Subtest: plain Pomodoro Task Link closes root-only while embedded closes recursively
ok 2649 - plain Pomodoro Task Link closes root-only while embedded closes recursively
  ---
  duration_ms: 2.401433
  ...
# Subtest: embedded Pomodoro Task Link still closes recursively and retires to struck form
ok 2650 - embedded Pomodoro Task Link still closes recursively and retires to struck form
  ---
  duration_ms: 2.445288
  ...
# Subtest: Ctrl+Enter toggles a struck plain Pomodoro link back to open
ok 2651 - Ctrl+Enter toggles a struck plain Pomodoro link back to open
  ---
  duration_ms: 1.756543
  ...
# Subtest: same-file plain Task Link closes and strikes the correct line
ok 2652 - same-file plain Task Link closes and strikes the correct line
  ---
  duration_ms: 1.239767
  ...
# Subtest: cursor selects which of several Task Links closes and strikes
ok 2653 - cursor selects which of several Task Links closes and strikes
  ---
  duration_ms: 1.320461
  ...
# Subtest: plain links to Blocked or non-task blocks still complete the Pomodoro
ok 2654 - plain links to Blocked or non-task blocks still complete the Pomodoro
  ---
  duration_ms: 3.586717
  ...
# Subtest: strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
ok 2655 - strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
  ---
  duration_ms: 0.520784
  ...
# Subtest: completeTaskAtCursor closes each open symbol through the Tasks command
ok 2656 - completeTaskAtCursor closes each open symbol through the Tasks command
  ---
  duration_ms: 1.691509
  ...
# Subtest: completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
ok 2657 - completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
  ---
  duration_ms: 0.348325
  ...
# Subtest: completeTaskAtCursor refuses closed, cancelled, and non-task lines
ok 2658 - completeTaskAtCursor refuses closed, cancelled, and non-task lines
  ---
  duration_ms: 0.321354
  ...
# Subtest: completeTaskAtCursor refuses a missing Tasks command with no write
ok 2659 - completeTaskAtCursor refuses a missing Tasks command with no write
  ---
  duration_ms: 0.154685
  ...
# Subtest: Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
ok 2660 - Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
  ---
  duration_ms: 0.519371
  ...
# Subtest: completeTaskAtCursor reports not-closed when Tasks does not write [x]
ok 2661 - completeTaskAtCursor reports not-closed when Tasks does not write [x]
  ---
  duration_ms: 0.170496
  ...
# Subtest: recovery api is frozen at version 2 and recovers without striking references
ok 2662 - recovery api is frozen at version 2 and recovers without striking references
  ---
  duration_ms: 2.612707
  ...
# Subtest: recovery api never throws and reports failures
ok 2663 - recovery api never throws and reports failures
  ---
  duration_ms: 0.217104
  ...
# Subtest: future-scheduled dependents stay Blocked on the planner, api, and close paths
ok 2664 - future-scheduled dependents stay Blocked on the planner, api, and close paths
  ---
  duration_ms: 15.321476
  ...
# Subtest: Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
ok 2665 - Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
  ---
  duration_ms: 4.043509
  ...
# Subtest: every printable non-space ASCII key resolves to a surround pair
ok 2666 - every printable non-space ASCII key resolves to a surround pair
  ---
  duration_ms: 3.597548
  ...
# Subtest: visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
ok 2667 - visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
  ---
  duration_ms: 0.645221
  ...
# Subtest: non-visible, combining, multi-character, and multi-code-unit values are rejected
ok 2668 - non-visible, combining, multi-character, and multi-code-unit values are rejected
  ---
  duration_ms: 0.22533
  ...
# Subtest: ys adds broad symmetric delimiters through pending keydown
ok 2669 - ys adds broad symmetric delimiters through pending keydown
  ---
  duration_ms: 1.163812
  ...
# Subtest: rejected keydown input never edits or leaks into a pending ys
ok 2670 - rejected keydown input never edits or leaks into a pending ys
  ---
  duration_ms: 0.369947
  ...
# Subtest: Escape cancels ys, cs, and ds pending state without editing
ok 2671 - Escape cancels ys, cs, and ds pending state without editing
  ---
  duration_ms: 0.277119
  ...
# Subtest: cs accepts broad target and replacement characters independently
ok 2672 - cs accepts broad target and replacement characters independently
  ---
  duration_ms: 1.013776
  ...
# Subtest: cs preserves structural alias and padding rules
ok 2673 - cs preserves structural alias and padding rules
  ---
  duration_ms: 1.446501
  ...
# Subtest: cs replaces repeated symmetric runs exactly once on each side
ok 2674 - cs replaces repeated symmetric runs exactly once on each side
  ---
  duration_ms: 0.488623
  ...
# Subtest: ds removes representative broad symmetric delimiters
ok 2675 - ds removes representative broad symmetric delimiters
  ---
  duration_ms: 0.757116
  ...
# Subtest: ds preserves structural alias and padding rules
ok 2676 - ds preserves structural alias and padding rules
  ---
  duration_ms: 0.328988
  ...
# Subtest: ds removes one pair from repeated runs, including the reported block link
ok 2677 - ds removes one pair from repeated runs, including the reported block link
  ---
  duration_ms: 1.452332
  ...
# Subtest: consecutive ds commands peel a triple symmetric surround
ok 2678 - consecutive ds commands peel a triple symmetric surround
  ---
  duration_ms: 0.310072
  ...
# Subtest: symmetric discovery uses deterministic sequential same-line run pairs
ok 2679 - symmetric discovery uses deterministic sequential same-line run pairs
  ---
  duration_ms: 0.201725
  ...
# Subtest: symmetric discovery includes every character in repeated boundaries
ok 2680 - symmetric discovery includes every character in repeated boundaries
  ---
  duration_ms: 0.380326
  ...
# Subtest: unpaired and unequal symmetric runs are safe no-ops
ok 2681 - unpaired and unequal symmetric runs are safe no-ops
  ---
  duration_ms: 0.295584
  ...
# Subtest: ordinary normal-mode keys remain untouched outside pending state
ok 2682 - ordinary normal-mode keys remain untouched outside pending state
  ---
  duration_ms: 0.274884
  ...
# Subtest: dot while a surround is pending is a literal delimiter, not repeat
ok 2683 - dot while a surround is pending is a literal delimiter, not repeat
  ---
  duration_ms: 0.177629
  ...
# Subtest: dot-repeat records and replays broad-character ys
ok 2684 - dot-repeat records and replays broad-character ys
  ---
  duration_ms: 0.355558
  ...
# Subtest: dot-repeat records and replays broad-character cs
ok 2685 - dot-repeat records and replays broad-character cs
  ---
  duration_ms: 0.249787
  ...
# Subtest: dot-repeat records and replays broad-character ds
ok 2686 - dot-repeat records and replays broad-character ds
  ---
  duration_ms: 0.246751
  ...
# Subtest: dot-repeat replays cs against repeated symmetric runs
ok 2687 - dot-repeat replays cs against repeated symmetric runs
  ---
  duration_ms: 0.249136
  ...
# Subtest: dot-repeat replays ds against repeated symmetric runs
ok 2688 - dot-repeat replays ds against repeated symmetric runs
  ---
  duration_ms: 0.247552
  ...
# Subtest: consecutive dot-repeats peel a triple symmetric surround
ok 2689 - consecutive dot-repeats peel a triple symmetric surround
  ---
  duration_ms: 0.248534
  ...
1..2689
# tests 2697
# suites 0
# pass 2691
# fail 6
# cancelled 0
# skipped 0
# todo 0
# duration_ms 5298.509369
failed  exit=1  duration=11292ms

