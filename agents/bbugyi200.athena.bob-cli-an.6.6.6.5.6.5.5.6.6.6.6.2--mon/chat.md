# Chat History - ace-run (bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2--mon)

- **TIMESTAMP:** 2026-10-26 08:42:05 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2--mon

## Prompt

sase monitor start --command 'npm test' --reason 'Run bob-plugins test and validation suites, then deploy the BLOCKS notice change'

## Response

sase tool run 1ee0d3944f5d2b13a6e48ea5f65b3a3b

> bob-plugins@0.1.0 test
> node scripts/build-plugins.mjs --check && npm run docs:inventory:check && node --test scripts/test-project-tasks-snapshot.cjs scripts/test-bob-articles.cjs scripts/test-dependency-line-migration.cjs scripts/test-navigation-hotkeys-section-nav.cjs scripts/test-navigation-hotkeys-rename.cjs scripts/test-navigation-hotkeys-ref-pdf.cjs scripts/test-navigation-hotkeys-templater-trigger.cjs scripts/test-navigation-hotkeys-schedule-recovery.cjs scripts/test-navigation-hotkeys-schedule-properties.cjs scripts/test-navigation-hotkeys-schedule-writes.cjs scripts/test-navigation-hotkeys-runtime-schedule.cjs scripts/test-navigation-hotkeys-dependencies.cjs scripts/test-navigation-blocks-guards.cjs scripts/test-navigation-blocks-writers.cjs scripts/test-navigation-blocks-edit.cjs scripts/test-navigation-blocks-stage-view.cjs scripts/test-navigation-hotkeys-dependency-mirror.cjs scripts/test-navigation-hotkeys-task-move-plan.cjs scripts/test-navigation-hotkeys-priority-notice.cjs scripts/test-navigation-successor-picker.cjs scripts/test-navigation-image-zoom-viewer.cjs scripts/test-navigation-hotkeys-unblocked-notice.cjs scripts/test-navigation-project-blocking.cjs scripts/test-navigation-project-dependency-stage.cjs scripts/test-navigation-project-subprojects.cjs scripts/test-navigation-project-subtree-gestures.cjs scripts/test-navigation-hotkeys-priority-picker.cjs scripts/test-navigation-hotkeys-picker-lifecycle.cjs scripts/test-navigation-hotkeys-ref-picker-text.cjs scripts/test-navigation-hotkeys-pomodoro-move-pickers.cjs scripts/test-navigation-inbox-route.cjs scripts/test-navigation-inbox-route-card.cjs scripts/test-navigation-hotkeys-task-move.cjs scripts/test-navigation-open-notes-uri.cjs scripts/test-navigation-hotkeys-dash-open.cjs scripts/test-navigation-goto-task-uri.cjs scripts/test-navigation-hotkeys-open-task-jump.cjs scripts/test-navigation-hotkeys-vim-counts.cjs scripts/test-navigation-hotkeys-tab-pin.cjs scripts/test-navigation-hotkeys-schedule-log.cjs scripts/test-navigation-hotkeys-schedule-review.cjs scripts/test-navigation-hotkeys-deferred-pomodoro.cjs scripts/test-navigation-hotkeys-pomodoro-parse.cjs scripts/test-navigation-hotkeys-pomodoro-bullet-move.cjs scripts/test-navigation-hotkeys-pomodoro-split-rename.cjs scripts/test-navigation-hotkeys-pomodoro-themes-manager.cjs scripts/test-navigation-hotkeys-pomodoro-reorder.cjs scripts/test-navigation-hotkeys-runtime-prune.cjs scripts/test-navigation-hotkeys-project-from-task.cjs scripts/test-navigation-hotkeys-project-reversal.cjs scripts/test-navigation-hotkeys-link-picker.cjs scripts/test-navigation-hotkeys-lane-toggle.cjs scripts/test-navigation-hotkeys-task-link-lane.cjs scripts/test-navigation-hotkeys-cancel-log.cjs scripts/test-navigation-hotkeys-cancel-task.cjs scripts/test-navigation-hotkeys-forward-promotion.cjs scripts/test-navigation-hotkeys-schedule-work-log.cjs scripts/test-navigation-hotkeys-task-move-history.cjs scripts/test-navigation-jump-history.cjs scripts/test-navigation-dependencies.cjs scripts/test-navigation-editor-line-diff.cjs scripts/test-navigation-quick-roll.cjs scripts/test-navigation-quick-roll-preview.cjs scripts/test-navigation-roll-decay.cjs scripts/test-navigation-decay-planner.cjs scripts/test-navigation-task-card-model.cjs scripts/test-navigation-task-card-view.cjs scripts/test-navigation-task-card-schedule.cjs scripts/test-navigation-task-card-review.cjs scripts/test-navigation-decision-card.cjs scripts/test-navigation-decision-card-handlers.cjs scripts/test-navigation-decision-card-keep.cjs scripts/test-navigation-refresh-modal.cjs scripts/test-navigation-freshness.cjs scripts/test-navigation-stamps.cjs scripts/test-navigation-keep-counting.cjs scripts/test-navigation-rotten-keep.cjs scripts/test-navigation-rotten-log.cjs scripts/test-navigation-checklist.cjs scripts/test-navigation-review-advance.cjs scripts/test-navigation-review-advance-gestures.cjs scripts/test-navigation-checklist-ctrl-enter.cjs scripts/test-ledger-tools-navigation.cjs scripts/test-ledger-tools-plan-budget.cjs scripts/test-ledger-tools-ready-badge.cjs scripts/test-ledger-tools-note-ready.cjs scripts/test-ledger-tools-note-ready-views.cjs scripts/test-ledger-tools-dashboard-parity.cjs scripts/test-ledger-tools-work-badge-tone.cjs scripts/test-ledger-tools-dashboard-collections.cjs scripts/test-ledger-tools-today.cjs scripts/test-ledger-tools-freshness-placement.cjs scripts/test-ledger-tools-freshness-states.cjs scripts/test-ledger-tools-freshness-namespace.cjs scripts/test-ledger-tools-freshness-review-model.cjs scripts/test-ledger-tools-freshness-queue.cjs scripts/test-ledger-tools-freshness-tracking.cjs scripts/test-ledger-tools-freshness-footer.cjs scripts/test-ledger-tools-freshness-recurring.cjs scripts/test-ledger-tools-freshness-mark.cjs scripts/test-ledger-tools-freshness-mark-surfaces.cjs scripts/test-ledger-tools-priority-marks.cjs scripts/test-ledger-tools-task-tag-marks.cjs scripts/test-ledger-tools-today-marks.cjs scripts/test-ledger-tools-today-marks-reading.cjs scripts/test-ledger-tools-unblocked-glyph.cjs scripts/test-ledger-tools-progress-marks.cjs scripts/test-ledger-tools-date-marks.cjs scripts/test-ledger-tools-recurrence-marks.cjs scripts/test-ledger-tools-date-marks-tasks.cjs scripts/test-ledger-tools-freshness-keeps.cjs scripts/test-ledger-tools-freshness-unblocked.cjs scripts/test-ledger-tools-freshness-decision-card.cjs scripts/test-ledger-tools-dependency-chips.cjs scripts/test-ledger-tools-blocks-chips.cjs scripts/test-ledger-tools-snippets.cjs scripts/test-ledger-tools-vim-mappings.cjs scripts/test-task-status-cycler-dependencies.cjs scripts/test-task-status-cycler-blocks-guards.cjs scripts/test-task-status-cycler-ctrl-enter.cjs scripts/test-task-status-cycler-reference-lifecycle.cjs scripts/test-task-status-cycler-pomodoro-completion.cjs scripts/test-task-status-cycler-pomodoro-work-log.cjs scripts/test-task-status-cycler-pomodoro-reopen.cjs scripts/test-task-status-cycler-blocked-schedule.cjs scripts/test-task-status-cycler-demotion-picker.cjs scripts/test-task-status-cycler-promotion.cjs scripts/test-task-status-cycler-counted-toggle.cjs scripts/test-task-status-cycler-successors.cjs scripts/test-task-status-cycler-successor-wiring.cjs scripts/test-task-status-cycler-successor-polish.cjs scripts/test-task-status-cycler-successor-offers.cjs scripts/test-task-status-cycler-project-pull-in.cjs scripts/test-task-status-cycler-task-links-api.cjs scripts/test-task-status-cycler-task-link-lane.cjs scripts/test-task-status-cycler-freshness.cjs scripts/test-block-id-prompt-dependencies.cjs scripts/test-block-id-prompt-blocks-guards.cjs scripts/test-block-id-prompt-ref-picker-text.cjs scripts/test-block-id-prompt-markers.cjs scripts/test-block-id-prompt-pomodoro-context.cjs scripts/test-block-id-prompt-target-update.cjs scripts/test-block-id-prompt-pomodoro-insertion.cjs scripts/test-block-id-prompt-pomodoro-targets.cjs scripts/test-block-id-prompt-pomodoro-picker-view.cjs scripts/test-block-id-prompt-pomodoro-picker-runtime.cjs scripts/test-block-id-prompt-work-log.cjs scripts/test-block-id-prompt-pomodoro-link-runtime.cjs scripts/test-block-id-prompt-pomodoro-link-picker-api.cjs scripts/test-block-id-prompt-pomodoro-unlink-runtime.cjs scripts/test-block-id-prompt-task-link-deletion.cjs scripts/test-block-id-prompt-plan-budget-and-freshness.cjs scripts/test-prompt-block-id-naming.cjs scripts/test-block-id-prompt-prefill.cjs scripts/test-vim-surround.cjs scripts/test-navigation-dependencies-stage-ranker-and-pool.cjs scripts/test-navigation-dependencies-stage-entry-and-view.cjs scripts/test-navigation-dependencies-stage-writes.cjs scripts/test-navigation-dependencies-stage-mirror-and-badge.cjs scripts/test-navigation-dependencies-stage-stale-guards.cjs scripts/test-navigation-dependencies-stage-performance.cjs scripts/test-navigation-prompt-block-id-stage.cjs scripts/test-navigation-dependencies-writer.cjs scripts/test-navigation-dependency-link-consumption.cjs scripts/test-plugin-build.cjs scripts/test-ledger-tools-stats-journal.cjs scripts/test-ledger-tools-stats-data.cjs scripts/test-ledger-tools-stats-block.cjs scripts/test-ledger-tools-stats-charts.cjs scripts/test-navigation-review-journal.cjs scripts/test-ledger-tools-stats-panels.cjs scripts/test-ledger-tools-reading-board-data.cjs scripts/test-ledger-tools-reading-board-models.cjs scripts/test-ledger-tools-reading-board-block.cjs scripts/test-ledger-tools-pomodoro-home-chips.cjs scripts/test-ledger-tools-pomodoro-themes.cjs scripts/test-navigation-image-zoom-target.cjs scripts/test-navigation-image-zoom-command.cjs scripts/test-docs-inventory.mjs scripts/test-docs-check.mjs scripts/test-navigation-relation-lines.cjs scripts/test-navigation-relation-writer.cjs scripts/test-navigation-relation-links-stage.cjs scripts/test-relation-index-linked-from-stage.cjs scripts/test-ledger-tools-relations.cjs scripts/test-ledger-tools-relation-index.cjs scripts/test-ledger-tools-relation-chips.cjs scripts/test-task-status-cycler-relations.cjs scripts/test-block-id-prompt-relations.cjs scripts/test-ledger-tools-day-strip.cjs scripts/test-ledger-tools-day-strip-plan-host.cjs scripts/test-ledger-tools-day-strip-hosts.cjs

  checked   block-id-prompt
  checked   bob-articles
  checked   bob-ledger-tools
  checked   bob-navigation-hotkeys
  checked   task-status-cycler

> bob-plugins@0.1.0 docs:inventory:check
> node scripts/docs-inventory.mjs --check

Plugin documentation inventory is up to date.
TAP version 13
# Subtest: bip BK1–BK12 accept and empty
ok 1 - bip BK1–BK12 accept and empty
  ---
  duration_ms: 2.330578
  ...
# Subtest: bip BK13–BK15 malformed split mirrors the Depends-On twin
ok 2 - bip BK13–BK15 malformed split mirrors the Depends-On twin
  ---
  duration_ms: 0.529922
  ...
# Subtest: bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
ok 3 - bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
  ---
  duration_ms: 0.177419
  ...
# Subtest: bip MC1/MC2 Pomodoro scanners skip managed lines
ok 4 - bip MC1/MC2 Pomodoro scanners skip managed lines
  ---
  duration_ms: 2.077065
  ...
# Subtest: explicit task IDs exclusively own dependency lookup
ok 5 - explicit task IDs exclusively own dependency lookup
  ---
  duration_ms: 5.743164
  ...
# Subtest: legacy tasks without an id field still fall back to their block ID
ok 6 - legacy tasks without an id field still fall back to their block ID
  ---
  duration_ms: 0.401216
  ...
# Subtest: blocked-link consumption raises open prerequisites and leaves the dependent blocked
ok 7 - blocked-link consumption raises open prerequisites and leaves the dependent blocked
  ---
  duration_ms: 2.443363
  ...
# Subtest: project-blocked member consumption promotes the project's open prerequisite
ok 8 - project-blocked member consumption promotes the project's open prerequisite
  ---
  duration_ms: 1.213586
  ...
# Subtest: project-blocked resident consumption promotes the project's open prerequisite
ok 9 - project-blocked resident consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.699745
  ...
# Subtest: a tagged inherited ^prj target is refused with its parent named
ok 10 - a tagged inherited ^prj target is refused with its parent named
  ---
  duration_ms: 0.56058
  ...
# Subtest: project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
ok 11 - project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
  ---
  duration_ms: 1.096302
  ...
# Subtest: project date refusal applies only when the date is the sole project reason
ok 12 - project date refusal applies only when the date is the sole project reason
  ---
  duration_ms: 0.604965
  ...
# Subtest: a project-blocked tag is token-bounded and ignored on lookalike tags
ok 13 - a project-blocked tag is token-bounded and ignored on lookalike tags
  ---
  duration_ms: 0.57589
  ...
# Subtest: task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
ok 14 - task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
  ---
  duration_ms: 2.859558
  ...
# Subtest: task blocked state unifies status and dependency reasons
ok 15 - task blocked state unifies status and dependency reasons
  ---
  duration_ms: 0.597601
  ...
# Subtest: task picker partition sinks blocked tasks while preserving group order
ok 16 - task picker partition sinks blocked tasks while preserving group order
  ---
  duration_ms: 0.418439
  ...
# Subtest: blocked chip labels show useful unmet dependency counts
ok 17 - blocked chip labels show useful unmet dependency counts
  ---
  duration_ms: 0.243996
  ...
# Subtest: blocked tooltips explain dependency and status-only reasons
ok 18 - blocked tooltips explain dependency and status-only reasons
  ---
  duration_ms: 0.574396
  ...
# Subtest: task status classes cover every open task status
ok 19 - task status classes cover every open task status
  ---
  duration_ms: 0.232594
  ...
# Subtest: Blocked tasks remain unmet dependency targets
ok 20 - Blocked tasks remain unmet dependency targets
  ---
  duration_ms: 0.395675
  ...
# Subtest: blocked task count covers both reasons without double-counting
ok 21 - blocked task count covers both reasons without double-counting
  ---
  duration_ms: 0.258523
  ...
# Subtest: single caret relocation preserves embedding and removes aliases
ok 22 - single caret relocation preserves embedding and removes aliases
  ---
  duration_ms: 4.650947
  ...
# Subtest: single caret relocation resets aliased block links
ok 23 - single caret relocation resets aliased block links
  ---
  duration_ms: 0.561451
  ...
# Subtest: single caret relocation strips heading and block subpaths
ok 24 - single caret relocation strips heading and block subpaths
  ---
  duration_ms: 0.491618
  ...
# Subtest: task picker normalizes every supported wiki block-link form
ok 25 - task picker normalizes every supported wiki block-link form
  ---
  duration_ms: 1.478563
  ...
# Subtest: three or more carets never trigger the task picker
ok 26 - three or more carets never trigger the task picker
  ---
  duration_ms: 0.307968
  ...
# Subtest: rapid aliased task picker completion preserves the alias
ok 27 - rapid aliased task picker completion preserves the alias
  ---
  duration_ms: 5.162575
  ...
# Subtest: task picker recognition is independent of Markdown source context
ok 28 - task picker recognition is independent of Markdown source context
  ---
  duration_ms: 1.762203
  ...
# Subtest: task picker recognition respects cursor proximity and fenced code
ok 29 - task picker recognition respects cursor proximity and fenced code
  ---
  duration_ms: 0.535432
  ...
# Subtest: plan budget suffix: link Notice appends the meter computed on post-write daily content
ok 30 - plan budget suffix: link Notice appends the meter computed on post-write daily content
  ---
  duration_ms: 21.002018
  ...
# Subtest: plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
ok 31 - plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
  ---
  duration_ms: 1.813131
  ...
# Subtest: plan budget suffix: unlink Notice marks an over-cap plan with 🔴
ok 32 - plan budget suffix: unlink Notice marks an over-cap plan with 🔴
  ---
  duration_ms: 4.52589
  ...
# Subtest: plan budget suffix: Next task without a block ID prompts for one and omits the meter
ok 33 - plan budget suffix: Next task without a block ID prompts for one and omits the meter
  ---
  duration_ms: 0.955383
  ...
# Subtest: plan budget suffix: Task Link Notice appends the meter from post-write daily content
ok 34 - plan budget suffix: Task Link Notice appends the meter from post-write daily content
  ---
  duration_ms: 7.766754
  ...
# Subtest: plan budget suffix: Task Link Notice omits the meter when no daily note takes part
ok 35 - plan budget suffix: Task Link Notice omits the meter when no daily note takes part
  ---
  duration_ms: 1.285774
  ...
# Subtest: planTargetTaskUpdate stamps the rewritten line last via injected stamper
ok 36 - planTargetTaskUpdate stamps the rewritten line last via injected stamper
  ---
  duration_ms: 0.477712
  ...
# Subtest: planTargetTaskUpdate without a stamper never stamps (identity default)
ok 37 - planTargetTaskUpdate without a stamper never stamps (identity default)
  ---
  duration_ms: 0.279453
  ...
# Subtest: planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
ok 38 - planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
  ---
  duration_ms: 0.514272
  ...
# Subtest: planTargetTaskUpdate stamps a Next task that gains a block ID
ok 39 - planTargetTaskUpdate stamps a Next task that gains a block ID
  ---
  duration_ms: 0.646815
  ...
# Subtest: planTargetTaskUpdate tolerates a throwing stamper
ok 40 - planTargetTaskUpdate tolerates a throwing stamper
  ---
  duration_ms: 0.368513
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 41 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.835765
  ...
# Subtest: dedicated-link helpers reject Depends-On lines
ok 42 - dedicated-link helpers reject Depends-On lines
  ---
  duration_ms: 0.918534
  ...
# Subtest: Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
ok 43 - Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
  ---
  duration_ms: 0.795729
  ...
# Subtest: malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
ok 44 - malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
  ---
  duration_ms: 0.318147
  ...
# Subtest: Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
ok 45 - Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
  ---
  duration_ms: 0.687903
  ...
# Subtest: Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
ok 46 - Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
  ---
  duration_ms: 0.502409
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent
ok 47 - readPlanBudgetMeter keeps per-cap over flags independent
  ---
  duration_ms: 0.523048
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent (mirror)
ok 48 - readPlanBudgetMeter keeps per-cap over flags independent (mirror)
  ---
  duration_ms: 0.300243
  ...
# Subtest: block-id-prompt freshness accessors degrade without ledger-tools
ok 49 - block-id-prompt freshness accessors degrade without ledger-tools
  ---
  duration_ms: 0.676401
  ...
# Subtest: list item body bounds trim whitespace and reject empty bullets
ok 50 - list item body bounds trim whitespace and reject empty bullets
  ---
  duration_ms: 4.530458
  ...
# Subtest: Pomodoro activation eligibility requires a sole-content sub-bullet
ok 51 - Pomodoro activation eligibility requires a sole-content sub-bullet
  ---
  duration_ms: 3.961842
  ...
# Subtest: Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
ok 52 - Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
  ---
  duration_ms: 0.482411
  ...
# Subtest: Pomodoro source context distinguishes ledger ancestry and open state
ok 53 - Pomodoro source context distinguishes ledger ancestry and open state
  ---
  duration_ms: 0.608311
  ...
# Subtest: future cleanup touches only later open Pomodoros and counts duplicates
ok 54 - future cleanup touches only later open Pomodoros and counts duplicates
  ---
  duration_ms: 4.001327
  ...
# Subtest: cleanup resolves aliases, embeds, same-note links, and alternate paths
ok 55 - cleanup resolves aliases, embeds, same-note links, and alternate paths
  ---
  duration_ms: 1.671159
  ...
# Subtest: dedicated bullet subtree cleanup preserves CRLF line endings
ok 56 - dedicated bullet subtree cleanup preserves CRLF line endings
  ---
  duration_ms: 4.519918
  ...
# Subtest: existing-ID task completion prunes future links in the source editor
ok 57 - existing-ID task completion prunes future links in the source editor
  ---
  duration_ms: 4.194005
  ...
# Subtest: new-ID same-file completion plans cleanup after the task edit
ok 58 - new-ID same-file completion plans cleanup after the task edit
  ---
  duration_ms: 2.051025
  ...
# Subtest: findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
ok 59 - findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
  ---
  duration_ms: 4.6673
  ...
# Subtest: findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
ok 60 - findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
  ---
  duration_ms: 0.312146
  ...
# Subtest: findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
ok 61 - findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
  ---
  duration_ms: 0.369205
  ...
# Subtest: todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
ok 62 - todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
  ---
  duration_ms: 1.307796
  ...
# Subtest: todayDailyPath honors a custom Daily Notes format and an empty folder
ok 63 - todayDailyPath honors a custom Daily Notes format and an empty folder
  ---
  duration_ms: 0.334118
  ...
# Subtest: formatDailyDate resolves bracketed literal text alongside date tokens
ok 64 - formatDailyDate resolves bracketed literal text alongside date tokens
  ---
  duration_ms: 0.241351
  ...
# Subtest: getDailyNotesOptions reads the daily-notes core plugin's configured options
ok 65 - getDailyNotesOptions reads the daily-notes core plugin's configured options
  ---
  duration_ms: 1.976252
  ...
# Subtest: computeFencedLineFlags marks opening and closing fence lines and everything between
ok 66 - computeFencedLineFlags marks opening and closing fence lines and everything between
  ---
  duration_ms: 0.433066
  ...
# Subtest: selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
ok 67 - selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
  ---
  duration_ms: 1.331411
  ...
# Subtest: selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
ok 68 - selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
  ---
  duration_ms: 2.663775
  ...
# Subtest: selectPomodoroInsertionTarget rejects more than one open timed entry
ok 69 - selectPomodoroInsertionTarget rejects more than one open timed entry
  ---
  duration_ms: 0.566862
  ...
# Subtest: selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
ok 70 - selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
  ---
  duration_ms: 0.29851
  ...
# Subtest: findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
ok 71 - findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
  ---
  duration_ms: 0.860653
  ...
# Subtest: planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
ok 72 - planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
  ---
  duration_ms: 2.96527
  ...
# Subtest: planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
ok 73 - planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
  ---
  duration_ms: 4.350144
  ...
# Subtest: planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
ok 74 - planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
  ---
  duration_ms: 0.614362
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
ok 75 - planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
  ---
  duration_ms: 1.785208
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
ok 76 - planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
  ---
  duration_ms: 1.295282
  ...
# Subtest: planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
ok 77 - planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
  ---
  duration_ms: 1.075994
  ...
# Subtest: planPomodoroLinkInsertion inserts before the separator preceding later content
ok 78 - planPomodoroLinkInsertion inserts before the separator preceding later content
  ---
  duration_ms: 0.950585
  ...
# Subtest: planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
ok 79 - planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
  ---
  duration_ms: 0.800408
  ...
# Subtest: planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
ok 80 - planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
  ---
  duration_ms: 0.873718
  ...
# Subtest: existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
ok 81 - existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
  ---
  duration_ms: 7.210132
  ...
# Subtest: same-note Pomodoro link runtime composes the task update with adjacent insertion
ok 82 - same-note Pomodoro link runtime composes the task update with adjacent insertion
  ---
  duration_ms: 2.616454
  ...
# Subtest: new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
ok 83 - new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
  ---
  duration_ms: 1.420662
  ...
# Subtest: planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
ok 84 - planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
  ---
  duration_ms: 0.498782
  ...
# Subtest: all-open cleanup removes current and future links while preserving history and unresolved links
ok 85 - all-open cleanup removes current and future links while preserving history and unresolved links
  ---
  duration_ms: 3.796778
  ...
# Subtest: all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
ok 86 - all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
  ---
  duration_ms: 3.628136
  ...
# Subtest: all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
ok 87 - all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
  ---
  duration_ms: 0.57155
  ...
# Subtest: all-open cleanup treats missing section, no open entries, and no matches as no-op successes
ok 88 - all-open cleanup treats missing section, no open entries, and no matches as no-op successes
  ---
  duration_ms: 0.505044
  ...
# Subtest: composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
ok 89 - composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
  ---
  duration_ms: 2.898212
  ...
# Subtest: pomodoro link picker choices normalize to existing/new or null
ok 90 - pomodoro link picker choices normalize to existing/new or null
  ---
  duration_ms: 2.940282
  ...
# Subtest: pomodoroLinkPicker api never rejects and validates choices
ok 91 - pomodoroLinkPicker api never rejects and validates choices
  ---
  duration_ms: 0.70748
  ...
# Subtest: destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
ok 92 - destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
  ---
  duration_ms: 1.146148
  ...
# Subtest: destination pick with a section releases its guards when the modal cannot open
ok 93 - destination pick with a section releases its guards when the modal cannot open
  ---
  duration_ms: 2.515913
  ...
# Subtest: plugin lifecycle installs the api and drops it on unload
ok 94 - plugin lifecycle installs the api and drops it on unload
  ---
  duration_ms: 0.633058
  ...
# Subtest: Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
ok 95 - Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
  ---
  duration_ms: 3.958635
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor requires a single cursor
ok 96 - resolvePomodoroLinkTaskFromEditor requires a single cursor
  ---
  duration_ms: 0.540832
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
ok 97 - resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
  ---
  duration_ms: 0.710336
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
ok 98 - resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
  ---
  duration_ms: 0.823993
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
ok 99 - resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
  ---
  duration_ms: 0.867806
  ...
# Subtest: blocked-link consumption reports dependency reasons before the project date
ok 100 - blocked-link consumption reports dependency reasons before the project date
  ---
  duration_ms: 10.007403
  ...
# Subtest: Pomodoro link checks do not read other notes for a non-Blocked task
ok 101 - Pomodoro link checks do not read other notes for a non-Blocked task
  ---
  duration_ms: 0.64411
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
ok 102 - resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
  ---
  duration_ms: 0.705547
  ...
# Subtest: task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
ok 103 - task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
  ---
  duration_ms: 12.533475
  ...
# Subtest: task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
ok 104 - task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
  ---
  duration_ms: 3.837395
  ...
# Subtest: task-mode toggle: linked only under a completed Pomodoro links again
ok 105 - task-mode toggle: linked only under a completed Pomodoro links again
  ---
  duration_ms: 1.689865
  ...
# Subtest: task-mode toggle: a task without a block ID is never linked and prompts for one
ok 106 - task-mode toggle: a task without a block ID is never linked and prompts for one
  ---
  duration_ms: 0.891632
  ...
# Subtest: existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
ok 107 - existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
  ---
  duration_ms: 2.386906
  ...
# Subtest: forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
ok 108 - forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
  ---
  duration_ms: 1.344457
  ...
# Subtest: new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
ok 109 - new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
  ---
  duration_ms: 1.250998
  ...
# Subtest: submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
ok 110 - submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
  ---
  duration_ms: 0.43521
  ...
# Subtest: submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
ok 111 - submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
  ---
  duration_ms: 0.364756
  ...
# Subtest: same-note Pomodoro link runtime: task and ledger edits merge into one transaction
ok 112 - same-note Pomodoro link runtime: task and ledger edits merge into one transaction
  ---
  duration_ms: 2.516493
  ...
# Subtest: linking an already-linked Ready task raises it to Next without duplicating the link
ok 113 - linking an already-linked Ready task raises it to Next without duplicating the link
  ---
  duration_ms: 1.155586
  ...
# Subtest: Next task without a block ID preflights the picker before prompting
ok 114 - Next task without a block ID preflights the picker before prompting
  ---
  duration_ms: 1.051226
  ...
# Subtest: Pomodoro link stops before any mutation when today's daily note is missing
ok 115 - Pomodoro link stops before any mutation when today's daily note is missing
  ---
  duration_ms: 0.396767
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
ok 116 - Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
  ---
  duration_ms: 0.732849
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
ok 117 - Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
  ---
  duration_ms: 0.664017
  ...
# Subtest: Pomodoro link aborts without any write when the task line changed since it was selected
ok 118 - Pomodoro link aborts without any write when the task line changed since it was selected
  ---
  duration_ms: 0.316574
  ...
# Subtest: Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
ok 119 - Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
  ---
  duration_ms: 1.630983
  ...
# Subtest: canceling the Pomodoro block-ID modal leaves the note untouched
ok 120 - canceling the Pomodoro block-ID modal leaves the note untouched
  ---
  duration_ms: 0.364536
  ...
# Subtest: review-walk: existing-ID link hands its Linked notice to continue with no separate notice
ok 121 - review-walk: existing-ID link hands its Linked notice to continue with no separate notice
  ---
  duration_ms: 8.195916
  ...
# Subtest: review-walk: prompted-ID link continues after submit
ok 122 - review-walk: prompted-ID link continues after submit
  ---
  duration_ms: 9.524409
  ...
# Subtest: review-walk: prompt cancel settles with null
ok 123 - review-walk: prompt cancel settles with null
  ---
  duration_ms: 0.350138
  ...
# Subtest: review-walk: BUSY swallows the key with no write
ok 124 - review-walk: BUSY swallows the key with no write
  ---
  duration_ms: 0.374394
  ...
# Subtest: review-walk: failed link keeps its notice and settles with null
ok 125 - review-walk: failed link keeps its notice and settles with null
  ---
  duration_ms: 0.406186
  ...
# Subtest: review-walk: partial link keeps its notice and never continues with an outcome
ok 126 - review-walk: partial link keeps its notice and never continues with an outcome
  ---
  duration_ms: 6.251412
  ...
# Subtest: inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
ok 127 - inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
  ---
  duration_ms: 0.707912
  ...
# Subtest: inbox-route: non-inbox notes and task-link mode never prompt
ok 128 - inbox-route: non-inbox notes and task-link mode never prompt
  ---
  duration_ms: 1.596888
  ...
# Subtest: inbox-route: cancel writes nothing and settles once
ok 129 - inbox-route: cancel writes nothing and settles once
  ---
  duration_ms: 2.952516
  ...
# Subtest: inbox-route: stay matches today
ok 130 - inbox-route: stay matches today
  ---
  duration_ms: 1.133733
  ...
# Subtest: inbox-route: move links, then moves, with one composed toast and a route continue
ok 131 - inbox-route: move links, then moves, with one composed toast and a route continue
  ---
  duration_ms: 1.467
  ...
# Subtest: inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
ok 132 - inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
  ---
  duration_ms: 1.792562
  ...
# Subtest: inbox-route: a move failure gives the partial notice plus a link-today continue
ok 133 - inbox-route: a move failure gives the partial notice plus a link-today continue
  ---
  duration_ms: 1.019627
  ...
# Subtest: review-walk: no nav or nav v2 keeps today's notices
ok 134 - review-walk: no nav or nav v2 keeps today's notices
  ---
  duration_ms: 10.810836
  ...
# Subtest: inbox-route: source drift during route prompt refuses without writes
ok 135 - inbox-route: source drift during route prompt refuses without writes
  ---
  duration_ms: 0.715626
  ...
# Subtest: inbox-route: block-ID route cancel returns sentinel and settles null once
ok 136 - inbox-route: block-ID route cancel returns sentinel and settles null once
  ---
  duration_ms: 1.685337
  ...
# Subtest: inbox-route: link no-op with move never commits
ok 137 - inbox-route: link no-op with move never commits
  ---
  duration_ms: 0.376288
  ...
# Subtest: picker opens only on the link direction, never on unlink
ok 138 - picker opens only on the link direction, never on unlink
  ---
  duration_ms: 19.958557
  ...
# Subtest: picker never opens in task-link mode
ok 139 - picker never opens in task-link mode
  ---
  duration_ms: 5.271754
  ...
# Subtest: Depends-On refusals never open the picker
ok 140 - Depends-On refusals never open the picker
  ---
  duration_ms: 2.376256
  ...
# Subtest: preflight refusals open nothing
ok 141 - preflight refusals open nothing
  ---
  duration_ms: 5.420506
  ...
# Subtest: picking a non-default entry links there
ok 142 - picking a non-default entry links there
  ---
  duration_ms: 4.583269
  ...
# Subtest: cancel writes nothing with no Notice and settles the walk null
ok 143 - cancel writes nothing with no Notice and settles the walk null
  ---
  duration_ms: 1.679286
  ...
# Subtest: a no-ID task gets picker, then the block-ID prompt with the target carried
ok 144 - a no-ID task gets picker, then the block-ID prompt with the target carried
  ---
  duration_ms: 4.649464
  ...
# Subtest: inbox order is picker, then route, then write
ok 145 - inbox order is picker, then route, then write
  ---
  duration_ms: 2.021478
  ...
# Subtest: a review-walk landing continues with link-today and the new text
ok 146 - a review-walk landing continues with link-today and the new text
  ---
  duration_ms: 3.107181
  ...
# Subtest: an all-closed ledger creates a new entry after the last completed block
ok 147 - an all-closed ledger creates a new entry after the last completed block
  ---
  duration_ms: 3.488529
  ...
# Subtest: several running entries allow an explicit pick
ok 148 - several running entries allow an explicit pick
  ---
  duration_ms: 1.156839
  ...
# Subtest: a target that changed before commit refuses with no writes
ok 149 - a target that changed before commit refuses with no writes
  ---
  duration_ms: 0.83844
  ...
# Subtest: a target that closed before commit refuses with no writes
ok 150 - a target that closed before commit refuses with no writes
  ---
  duration_ms: 0.841677
  ...
# Subtest: the task note being the daily note uses one editor transaction
ok 151 - the task note being the daily note uses one editor transaction
  ---
  duration_ms: 1.170454
  ...
# Subtest: promptOpen blocks re-entry while the picker is open
ok 152 - promptOpen blocks re-entry while the picker is open
  ---
  duration_ms: 21.425887
  ...
# Subtest: header shows title, subtitle, lane chip per status, and block-ID chip
ok 153 - header shows title, subtitle, lane chip per status, and block-ID chip
  ---
  duration_ms: 17.950594
  ...
# Subtest: rows render in document order with the default selected
ok 154 - rows render in document order with the default selected
  ---
  duration_ms: 2.263711
  ...
# Subtest: recent theme rows follow today's rows and render component swatches
ok 155 - recent theme rows follow today's rows and render component swatches
  ---
  duration_ms: 30.26972
  ...
# Subtest: exact recent themes suppress generic creation and preserve catalog spelling
ok 156 - exact recent themes suppress generic creation and preserve catalog spelling
  ---
  duration_ms: 4.743766
  ...
# Subtest: Ctrl+D hides a Recent suggestion as an undoable ghost and leaves Today unchanged
ok 157 - Ctrl+D hides a Recent suggestion as an undoable ghost and leaves Today unchanged
  ---
  duration_ms: 21.849736
  ...
# Subtest: new-name rows show near-duplicate and hidden-theme hints
ok 158 - new-name rows show near-duplicate and hidden-theme hints
  ---
  duration_ms: 5.532601
  ...
# Subtest: running row shows progress fraction and minutes-left meta
ok 159 - running row shows progress fraction and minutes-left meta
  ---
  duration_ms: 2.25796
  ...
# Subtest: unnamed entries render muted italic
ok 160 - unnamed entries render muted italic
  ---
  duration_ms: 0.882735
  ...
# Subtest: filtering ranks, highlights, and clearing restores the default
ok 161 - filtering ranks, highlights, and clearing restores the default
  ---
  duration_ms: 1.474665
  ...
# Subtest: create row meta, divider, and theme badge
ok 162 - create row meta, divider, and theme badge
  ---
  duration_ms: 3.05443
  ...
# Subtest: exact open names suppress the create row; prefix matches keep it
ok 163 - exact open names suppress the create row; prefix matches keep it
  ---
  duration_ms: 1.606096
  ...
# Subtest: theme badge turns red over cap; a throwing budget hides the detail
ok 164 - theme badge turns red over cap; a throwing budget hides the detail
  ---
  duration_ms: 1.871873
  ...
# Subtest: invalid rows explain the grammar and are inert on Enter
ok 165 - invalid rows explain the grammar and are inert on Enter
  ---
  duration_ms: 11.499701
  ...
# Subtest: multiple running entries show the banner, no pills, and block creation
ok 166 - multiple running entries show the banner, no pills, and block creation
  ---
  duration_ms: 2.376035
  ...
# Subtest: navigation wraps and skips non-selectable rows
ok 167 - navigation wraps and skips non-selectable rows
  ---
  duration_ms: 2.407185
  ...
# Subtest: empty state invites planning a Pomodoro
ok 168 - empty state invites planning a Pomodoro
  ---
  duration_ms: 1.71288
  ...
# Subtest: footer hints and plan meter
ok 169 - footer hints and plan meter
  ---
  duration_ms: 2.103226
  ...
# Subtest: Enter chooses the selected row; click chooses that row
ok 170 - Enter chooses the selected row; click chooses that row
  ---
  duration_ms: 1.792092
  ...
# Subtest: Shift+Enter creates; an exact open name links there instead
ok 171 - Shift+Enter creates; an exact open name links there instead
  ---
  duration_ms: 1.59301
  ...
# Subtest: Ctrl+Shift+Enter commits exactly like Enter
ok 172 - Ctrl+Shift+Enter commits exactly like Enter
  ---
  duration_ms: 0.879679
  ...
# Subtest: Escape and Ctrl+[ cancel with no choice; settle-once holds
ok 173 - Escape and Ctrl+[ cancel with no choice; settle-once holds
  ---
  duration_ms: 6.671054
  ...
# Subtest: canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
ok 174 - canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
  ---
  duration_ms: 3.812046
  ...
# Subtest: canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
ok 175 - canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
  ---
  duration_ms: 0.407308
  ...
# Subtest: pomodoroLinkSelectorSlug mirrors capture slugs
ok 176 - pomodoroLinkSelectorSlug mirrors capture slugs
  ---
  duration_ms: 0.569126
  ...
# Subtest: parsePomodoroEntryParts reads canonical and legacy entry lines
ok 177 - parsePomodoroEntryParts reads canonical and legacy entry lines
  ---
  duration_ms: 1.71344
  ...
# Subtest: collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
ok 178 - collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
  ---
  duration_ms: 3.977592
  ...
# Subtest: collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
ok 179 - collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
  ---
  duration_ms: 4.351287
  ...
# Subtest: collectPomodoroLinkEntries counts links but excludes struck references
ok 180 - collectPomodoroLinkEntries counts links but excludes struck references
  ---
  duration_ms: 0.999838
  ...
# Subtest: collectPomodoroLinkEntries falls back to range text and position titles
ok 181 - collectPomodoroLinkEntries falls back to range text and position titles
  ---
  duration_ms: 1.444227
  ...
# Subtest: pomodoroRunProgress reports fractions, overtime, and midnight wrap
ok 182 - pomodoroRunProgress reports fractions, overtime, and midnight wrap
  ---
  duration_ms: 0.960142
  ...
# Subtest: buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
ok 183 - buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
  ---
  duration_ms: 1.988635
  ...
# Subtest: buildPomodoroLinkPickerRows keeps the create row for prefix matches
ok 184 - buildPomodoroLinkPickerRows keeps the create row for prefix matches
  ---
  duration_ms: 1.096122
  ...
# Subtest: buildPomodoroLinkPickerRows marks completed-only names as again
ok 185 - buildPomodoroLinkPickerRows marks completed-only names as again
  ---
  duration_ms: 0.8328
  ...
# Subtest: buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
ok 186 - buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
  ---
  duration_ms: 0.921098
  ...
# Subtest: buildPomodoroLinkPickerRows matches times, positions, and block IDs
ok 187 - buildPomodoroLinkPickerRows matches times, positions, and block IDs
  ---
  duration_ms: 1.15218
  ...
# Subtest: resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
ok 188 - resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
  ---
  duration_ms: 1.072668
  ...
# Subtest: defaultPomodoroLinkChoice returns the default entry or null
ok 189 - defaultPomodoroLinkChoice returns the default entry or null
  ---
  duration_ms: 0.572864
  ...
# Subtest: planExplicitPomodoroLinkInsertion links under a chosen existing entry
ok 190 - planExplicitPomodoroLinkInsertion links under a chosen existing entry
  ---
  duration_ms: 2.632936
  ...
# Subtest: planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
ok 191 - planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
  ---
  duration_ms: 0.935696
  ...
# Subtest: planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
ok 192 - planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
  ---
  duration_ms: 2.700083
  ...
# Subtest: planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
ok 193 - planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
  ---
  duration_ms: 0.905778
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after the running entry
ok 194 - planExplicitPomodoroLinkInsertion creates after the running entry
  ---
  duration_ms: 1.312235
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
ok 195 - planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
  ---
  duration_ms: 1.149294
  ...
# Subtest: planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
ok 196 - planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
  ---
  duration_ms: 0.381969
  ...
# Subtest: planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
ok 197 - planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
  ---
  duration_ms: 0.559608
  ...
# Subtest: planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
ok 198 - planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
  ---
  duration_ms: 2.680267
  ...
# Subtest: buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
ok 199 - buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
  ---
  duration_ms: 0.40338
  ...
# Subtest: buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
ok 200 - buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
  ---
  duration_ms: 0.513671
  ...
# Subtest: planExplicitPomodoroLinkInsertion matches mixed-case raced open names
ok 201 - planExplicitPomodoroLinkInsertion matches mixed-case raced open names
  ---
  duration_ms: 0.685308
  ...
# Subtest: buildPomodoroLinkPickerRows bounds \#N position matches
ok 202 - buildPomodoroLinkPickerRows bounds \#N position matches
  ---
  duration_ms: 0.990761
  ...
# Subtest: planPomodoroLinkInsertion without a target keeps today's behavior and shape
ok 203 - planPomodoroLinkInsertion without a target keeps today's behavior and shape
  ---
  duration_ms: 0.811149
  ...
# Subtest: direct unlink without a daily note keeps the Next lane and reports it
ok 204 - direct unlink without a daily note keeps the Next lane and reports it
  ---
  duration_ms: 4.229614
  ...
# Subtest: In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
ok 205 - In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
  ---
  duration_ms: 0.629301
  ...
# Subtest: In Progress unlink with a summary keeps the lane and creates a Work Log
ok 206 - In Progress unlink with a summary keeps the lane and creates a Work Log
  ---
  duration_ms: 1.878947
  ...
# Subtest: In Progress unlink revalidates task text and block-ID uniqueness at confirmation
ok 207 - In Progress unlink revalidates task text and block-ID uniqueness at confirmation
  ---
  duration_ms: 0.43464
  ...
# Subtest: Next task unlink removes current and future links and keeps the Next lane
ok 208 - Next task unlink removes current and future links and keeps the Next lane
  ---
  duration_ms: 5.963893
  ...
# Subtest: In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
ok 209 - In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
  ---
  duration_ms: 1.500263
  ...
# Subtest: same-note Next unlink merges the Work Log and all-open cleanup in the active editor
ok 210 - same-note Next unlink merges the Work Log and all-open cleanup in the active editor
  ---
  duration_ms: 1.346801
  ...
# Subtest: same-note In Progress unlink merges cleanup and Work Log in the active editor
ok 211 - same-note In Progress unlink merges cleanup and Work Log in the active editor
  ---
  duration_ms: 0.999889
  ...
# Subtest: Next unlink stops before any write when daily cleanup write is stale
ok 212 - Next unlink stops before any write when daily cleanup write is stale
  ---
  duration_ms: 0.905268
  ...
# Subtest: Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
ok 213 - Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
  ---
  duration_ms: 1.012663
  ...
# Subtest: In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
ok 214 - In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
  ---
  duration_ms: 0.894859
  ...
# Subtest: review-walk: unlink settles with null and keeps its notice
ok 215 - review-walk: unlink settles with null and keeps its notice
  ---
  duration_ms: 2.233663
  ...
# Subtest: inbox-route: unlink cancel writes nothing
ok 216 - inbox-route: unlink cancel writes nothing
  ---
  duration_ms: 0.592381
  ...
# Subtest: inbox-route: unlink stay matches today and never commits
ok 217 - inbox-route: unlink stay matches today and never commits
  ---
  duration_ms: 0.889909
  ...
# Subtest: inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
ok 218 - inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
  ---
  duration_ms: 1.002814
  ...
# Subtest: inbox-route: In Progress unlink with a Work summary routes
ok 219 - inbox-route: In Progress unlink with a Work summary routes
  ---
  duration_ms: 0.901481
  ...
# Subtest: inbox-route: unlink move failure gives the partial notice and stays
ok 220 - inbox-route: unlink move failure gives the partial notice and stays
  ---
  duration_ms: 0.587562
  ...
# Subtest: inbox-route: non-inbox unlink never prompts
ok 221 - inbox-route: non-inbox unlink never prompts
  ---
  duration_ms: 0.609293
  ...
# Subtest: review-walk: Work-summary unlink path retains origin until submit
ok 222 - review-walk: Work-summary unlink path retains origin until submit
  ---
  duration_ms: 0.600726
  ...
# Subtest: inbox-route: unlink source drift during route prompt refuses without writes
ok 223 - inbox-route: unlink source drift during route prompt refuses without writes
  ---
  duration_ms: 0.465769
  ...
# Subtest: inbox-route: Work-summary route cancel returns sentinel and settles null once
ok 224 - inbox-route: Work-summary route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.557303
  ...
# Subtest: inbox-route: unlink no-op with move never commits
ok 225 - inbox-route: unlink no-op with move never commits
  ---
  duration_ms: 0.366299
  ...
# Subtest: same-note unlink maps a task below removed entries through Work-summary inserts
ok 226 - same-note unlink maps a task below removed entries through Work-summary inserts
  ---
  duration_ms: 1.180413
  ...
# Subtest: direct-add seeds from the task headline, not non-task blocks
ok 227 - direct-add seeds from the task headline, not non-task blocks
  ---
  duration_ms: 6.196619
  ...
# Subtest: link-task-complete seeds from the target, prefers open buffers
ok 228 - link-task-complete seeds from the target, prefers open buffers
  ---
  duration_ms: 2.043641
  ...
# Subtest: link-task-complete reports stale and unreadable targets
ok 229 - link-task-complete reports stale and unreadable targets
  ---
  duration_ms: 0.617669
  ...
# Subtest: pomodoro link seeds after the choice from the cursor task
ok 230 - pomodoro link seeds after the choice from the cursor task
  ---
  duration_ms: 0.48198
  ...
# Subtest: marker rename suggests from the unique task, never hiding ambiguity
ok 231 - marker rename suggests from the unique task, never hiding ambiguity
  ---
  duration_ms: 1.090882
  ...
# Subtest: modal seeds the value, selects once, and never overwrites typing
ok 232 - modal seeds the value, selects once, and never overwrites typing
  ---
  duration_ms: 2.419108
  ...
# Subtest: modal disables Save while loading and survives close/reopen
ok 233 - modal disables Save while loading and survives close/reopen
  ---
  duration_ms: 1.883927
  ...
# Subtest: submit revalidates: occupied IDs and stale tasks fail editable
ok 234 - submit revalidates: occupied IDs and stale tasks fail editable
  ---
  duration_ms: 0.993527
  ...
# Subtest: cancelling writes no ID and explicit renames keep the current ID
ok 235 - cancelling writes no ID and explicit renames keep the current ID
  ---
  duration_ms: 1.073429
  ...
# Subtest: the task picker drops the paired \#ref and prefixes the book
ok 236 - the task picker drops the paired \#ref and prefixes the book
  ---
  duration_ms: 4.855899
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 237 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.60755
  ...
# Subtest: block-id-prompt LK1–LK19 recognises only relation line shapes
ok 238 - block-id-prompt LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 3.304238
  ...
# Subtest: block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
ok 239 - block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
  ---
  duration_ms: 2.207904
  ...
# Subtest: block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
ok 240 - block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
  ---
  duration_ms: 2.475665
  ...
# Subtest: calendar date parsing rejects malformed width and impossible dates
ok 241 - calendar date parsing rejects malformed width and impossible dates
  ---
  duration_ms: 3.02332
  ...
# Subtest: future scheduled field detection respects the yesterday/today/tomorrow boundary
ok 242 - future scheduled field detection respects the yesterday/today/tomorrow boundary
  ---
  duration_ms: 0.692151
  ...
# Subtest: scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
ok 243 - scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
  ---
  duration_ms: 0.23091
  ...
# Subtest: planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
ok 244 - planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
  ---
  duration_ms: 1.921758
  ...
# Subtest: planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
ok 245 - planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
  ---
  duration_ms: 0.410062
  ...
# Subtest: planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
ok 246 - planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
  ---
  duration_ms: 0.322416
  ...
# Subtest: planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
ok 247 - planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
  ---
  duration_ms: 0.284212
  ...
# Subtest: planTargetTaskUpdate leaves today and past schedules untouched
ok 248 - planTargetTaskUpdate leaves today and past schedules untouched
  ---
  duration_ms: 0.313268
  ...
# Subtest: planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
ok 249 - planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
  ---
  duration_ms: 3.885367
  ...
# Subtest: two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
ok 250 - two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
  ---
  duration_ms: 0.817741
  ...
# Subtest: a malformed single scheduled field is never treated as future
ok 251 - a malformed single scheduled field is never treated as future
  ---
  duration_ms: 0.300463
  ...
# Subtest: an ambiguous scheduled field does not block the legacy Ready promotion
ok 252 - an ambiguous scheduled field does not block the legacy Ready promotion
  ---
  duration_ms: 0.552094
  ...
# Subtest: planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
ok 253 - planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
  ---
  duration_ms: 0.38243
  ...
# Subtest: Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
ok 254 - Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
  ---
  duration_ms: 0.965963
  ...
# Subtest: Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
ok 255 - Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
  ---
  duration_ms: 0.375367
  ...
# Subtest: planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
ok 256 - planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
  ---
  duration_ms: 0.742117
  ...
# Subtest: planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
ok 257 - planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
  ---
  duration_ms: 0.325912
  ...
# Subtest: planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
ok 258 - planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.519331
  ...
# Subtest: planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
ok 259 - planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
  ---
  duration_ms: 0.397228
  ...
# Subtest: planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
ok 260 - planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
  ---
  duration_ms: 0.414732
  ...
# Subtest: planTargetTaskUpdate preserves a trailing newline when one was already present
ok 261 - planTargetTaskUpdate preserves a trailing newline when one was already present
  ---
  duration_ms: 0.308499
  ...
# Subtest: planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
ok 262 - planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
  ---
  duration_ms: 0.227815
  ...
# Subtest: planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
ok 263 - planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
  ---
  duration_ms: 0.289603
  ...
# Subtest: planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
ok 264 - planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
  ---
  duration_ms: 0.26685
  ...
# Subtest: existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
ok 265 - existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
  ---
  duration_ms: 6.409586
  ...
# Subtest: new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
ok 266 - new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
  ---
  duration_ms: 1.696959
  ...
# Subtest: activation runtime aborts without any write when the target preimage goes stale
ok 267 - activation runtime aborts without any write when the target preimage goes stale
  ---
  duration_ms: 0.818823
  ...
# Subtest: same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
ok 268 - same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
  ---
  duration_ms: 4.353018
  ...
# Subtest: same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
ok 269 - same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
  ---
  duration_ms: 1.068439
  ...
# Subtest: a source marker edited after a successful existing-ID target write reports an accurate partial notice
ok 270 - a source marker edited after a successful existing-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.99525
  ...
# Subtest: a source marker edited after a successful new-ID target write reports an accurate partial notice
ok 271 - a source marker edited after a successful new-ID target write reports an accurate partial notice
  ---
  duration_ms: 1.38814
  ...
# Subtest: planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
ok 272 - planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
  ---
  duration_ms: 0.809585
  ...
# Subtest: planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
ok 273 - planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
  ---
  duration_ms: 0.331884
  ...
# Subtest: planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
ok 274 - planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
  ---
  duration_ms: 0.321764
  ...
# Subtest: planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
ok 275 - planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.247492
  ...
# Subtest: direct Task Links raise ^prj while never pulling its date forward
ok 276 - direct Task Links raise ^prj while never pulling its date forward
  ---
  duration_ms: 0.271027
  ...
# Subtest: task-link selection: one link is selectable from any column, several are chosen by cursor
ok 277 - task-link selection: one link is selectable from any column, several are chosen by cursor
  ---
  duration_ms: 6.078033
  ...
# Subtest: task-link selection ignores picker/rename markers, plain links, and Markdown-style links
ok 278 - task-link selection ignores picker/rename markers, plain links, and Markdown-style links
  ---
  duration_ms: 0.71786
  ...
# Subtest: dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
ok 279 - dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
  ---
  duration_ms: 1.109778
  ...
# Subtest: inline Task Link deletion removes the token with its decoration and collapses whitespace
ok 280 - inline Task Link deletion removes the token with its decoration and collapses whitespace
  ---
  duration_ms: 4.8359
  ...
# Subtest: dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
ok 281 - dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
  ---
  duration_ms: 1.971594
  ...
# Subtest: mergeCoveringEdits keeps the covering edit and the earlier of identical edits
ok 282 - mergeCoveringEdits keeps the covering edit and the earlier of identical edits
  ---
  duration_ms: 0.533489
  ...
# Subtest: dependency transclusion detection needs an embedded sole-content child of a \#task line
ok 283 - dependency transclusion detection needs an embedded sole-content child of a \#task line
  ---
  duration_ms: 0.833842
  ...
# Subtest: Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
ok 284 - Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
  ---
  duration_ms: 9.132992
  ...
# Subtest: Task Link on a Next target works from an embedded aliased link outside any Pomodoro
ok 285 - Task Link on a Next target works from an embedded aliased link outside any Pomodoro
  ---
  duration_ms: 2.276045
  ...
# Subtest: same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
ok 286 - same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
  ---
  duration_ms: 1.804355
  ...
# Subtest: same-note Task Link deletion clamps the restored cursor to the shortened note
ok 287 - same-note Task Link deletion clamps the restored cursor to the shortened note
  ---
  duration_ms: 0.946487
  ...
# Subtest: a cleanup subtree that covers a nested selected link wins and links are not double counted
ok 288 - a cleanup subtree that covers a nested selected link wins and links are not double counted
  ---
  duration_ms: 1.282779
  ...
# Subtest: same-note Task Link in a closed entry deletes the closed entry it empties
ok 289 - same-note Task Link in a closed entry deletes the closed entry it empties
  ---
  duration_ms: 0.930075
  ...
# Subtest: Task Link in another day's note deletes the emptied entry there and in today's note
ok 290 - Task Link in another day's note deletes the emptied entry there and in today's note
  ---
  duration_ms: 1.379423
  ...
# Subtest: Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
ok 291 - Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
  ---
  duration_ms: 2.973967
  ...
# Subtest: Task Link on an In Progress target with a blank summary logs nothing
ok 292 - Task Link on an In Progress target with a blank summary logs nothing
  ---
  duration_ms: 1.687541
  ...
# Subtest: canceling the In Progress Task Link prompt leaves everything untouched
ok 293 - canceling the In Progress Task Link prompt leaves everything untouched
  ---
  duration_ms: 0.711598
  ...
# Subtest: canceling the In Progress unlink prompt in task mode leaves everything untouched
ok 294 - canceling the In Progress unlink prompt in task mode leaves everything untouched
  ---
  duration_ms: 1.525793
  ...
# Subtest: In Progress Task Link submit revalidates the link line and the target task
ok 295 - In Progress Task Link submit revalidates the link line and the target task
  ---
  duration_ms: 5.659434
  ...
# Subtest: Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
ok 296 - Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
  ---
  duration_ms: 2.146597
  ...
# Subtest: Task Link on a Done or Cancelled target is refused without edits
ok 297 - Task Link on a Done or Cancelled target is refused without edits
  ---
  duration_ms: 0.94334
  ...
# Subtest: Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
ok 298 - Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
  ---
  duration_ms: 6.676092
  ...
# Subtest: precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
ok 299 - precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
  ---
  duration_ms: 2.804654
  ...
# Subtest: Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
ok 300 - Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
  ---
  duration_ms: 0.799125
  ...
# Subtest: Task Link that is a sub-task dependency transclusion is refused without edits
ok 301 - Task Link that is a sub-task dependency transclusion is refused without edits
  ---
  duration_ms: 0.334919
  ...
# Subtest: Task Link partial failure after the daily write is retryable
ok 302 - Task Link partial failure after the daily write is retryable
  ---
  duration_ms: 1.741525
  ...
# Subtest: Task Link stops before any write when the target note changes after planning
ok 303 - Task Link stops before any write when the target note changes after planning
  ---
  duration_ms: 1.035166
  ...
# Subtest: Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
ok 304 - Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
  ---
  duration_ms: 0.971765
  ...
# Subtest: Task Link subtree deletion removes a nested target task without any status write
ok 305 - Task Link subtree deletion removes a nested target task without any status write
  ---
  duration_ms: 0.624001
  ...
# Subtest: whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
ok 306 - whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
  ---
  duration_ms: 1.209679
  ...
# Subtest: selected-link deletion maps a cursor inside a removed entry to its former start
ok 307 - selected-link deletion maps a cursor inside a removed entry to its former start
  ---
  duration_ms: 3.238321
  ...
# Subtest: work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
ok 308 - work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
  ---
  duration_ms: 3.865408
  ...
# Subtest: work log date helpers use local calendar components
ok 309 - work log date helpers use local calendar components
  ---
  duration_ms: 0.442856
  ...
# Subtest: planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
ok 310 - planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
  ---
  duration_ms: 1.217945
  ...
# Subtest: planWorkLogInsertion inherits an existing space-indented child prefix
ok 311 - planWorkLogInsertion inherits an existing space-indented child prefix
  ---
  duration_ms: 0.876914
  ...
# Subtest: planWorkLogInsertion inherits an existing tab-indented child prefix
ok 312 - planWorkLogInsertion inherits an existing tab-indented child prefix
  ---
  duration_ms: 0.368964
  ...
# Subtest: planWorkLogInsertion prepends newest-first entries into existing marker spellings
ok 313 - planWorkLogInsertion prepends newest-first entries into existing marker spellings
  ---
  duration_ms: 0.801219
  ...
# Subtest: planWorkLogInsertion ignores nested child-task markers and preserves CRLF
ok 314 - planWorkLogInsertion ignores nested child-task markers and preserves CRLF
  ---
  duration_ms: 0.541654
  ...
# Subtest: planWorkLogInsertion treats blank summaries as no-op structural edits
ok 315 - planWorkLogInsertion treats blank summaries as no-op structural edits
  ---
  duration_ms: 0.434239
  ...
# Subtest: the Open-reset planner is removed: unlink plans only a Work Log insertion
ok 316 - the Open-reset planner is removed: unlink plans only a Work Log insertion
  ---
  duration_ms: 0.357172
  ...
# Subtest: unlink Work Log plan keeps the In Progress checkbox and appends one entry
ok 317 - unlink Work Log plan keeps the In Progress checkbox and appends one entry
  ---
  duration_ms: 0.561182
  ...
# Subtest: article detection accepts scalar and list frontmatter values
ok 318 - article detection accepts scalar and list frontmatter values
  ---
  duration_ms: 2.820584
  ...
# Subtest: bob resolution prefers its setting, then known install paths, then PATH
ok 319 - bob resolution prefers its setting, then known install paths, then PATH
  ---
  duration_ms: 2.055403
  ...
# Subtest: plan decoder accepts v1 and rejects a foreign schema version
ok 320 - plan decoder accepts v1 and rejects a foreign schema version
  ---
  duration_ms: 0.578775
  ...
# Subtest: bob stdin spawn passes the article contract and vault environment
ok 321 - bob stdin spawn passes the article contract and vault environment
  ---
  duration_ms: 3.921725
  ...
# Subtest: bob plan stdout decodes UTF-8 split across chunks
ok 322 - bob plan stdout decodes UTF-8 split across chunks
  ---
  duration_ms: 1.993285
  ...
# Subtest: early bob exit on stdin reports EPIPE as a run failure
ok 323 - early bob exit on stdin reports EPIPE as a run failure
  ---
  duration_ms: 4.708388
  ...
# Subtest: line hunks become minimal cursor-preserving changes
ok 324 - line hunks become minimal cursor-preserving changes
  ---
  duration_ms: 1.402357
  ...
# Subtest: insert, multi-line replace, and deletion hunks reproduce the formatted note
ok 325 - insert, multi-line replace, and deletion hunks reproduce the formatted note
  ---
  duration_ms: 4.756349
  ...
# Subtest: notice shows bob's text and at most two warning findings
ok 326 - notice shows bob's text and at most two warning findings
  ---
  duration_ms: 0.61313
  ...
# Subtest: inbound changes apply only when their target line still matches the preimage
ok 327 - inbound changes apply only when their target line still matches the preimage
  ---
  duration_ms: 0.993437
  ...
# Subtest: undo guard blocks a reformat until a fresh input or delete event
ok 328 - undo guard blocks a reformat until a fresh input or delete event
  ---
  duration_ms: 0.736647
  ...
# Subtest: leave formatting observes the undo guard before saving or reading
ok 329 - leave formatting observes the undo guard before saving or reading
  ---
  duration_ms: 0.584115
  ...
# Subtest: Convert shows bob's refusal on every invocation
ok 330 - Convert shows bob's refusal on every invocation
  ---
  duration_ms: 0.617038
  ...
# Subtest: old bob's non-JSON article response gets one update notice per session
ok 331 - old bob's non-JSON article response gets one update notice per session
  ---
  duration_ms: 0.476049
  ...
# Subtest: format drops its response if the editor changed while bob was running
ok 332 - format drops its response if the editor changed while bob was running
  ---
  duration_ms: 0.679657
  ...
# Subtest: decoration ranges mark written section numbers from the outline
ok 333 - decoration ranges mark written section numbers from the outline
  ---
  duration_ms: 1.438386
  ...
# Subtest: a new outline rerenders each open Reading view once for that generation
ok 334 - a new outline rerenders each open Reading view once for that generation
  ---
  duration_ms: 0.719023
  ...
# Subtest: section at a given line uses the innermost outline range
ok 335 - section at a given line uses the innermost outline range
  ---
  duration_ms: 0.859601
  ...
# Subtest: stale-hint debounce and in-flight state machine
ok 336 - stale-hint debounce and in-flight state machine
  ---
  duration_ms: 0.662925
  ...
# Subtest: reading-view wrapping puts the leading number token in span.bob-secno
ok 337 - reading-view wrapping puts the leading number token in span.bob-secno
  ---
  duration_ms: 1.445779
  ...
# Subtest: applied plans remap outline lines onto the formatted buffer
ok 338 - applied plans remap outline lines onto the formatted buffer
  ---
  duration_ms: 0.417988
  ...
# Subtest: article styles scope the reading look under .bob-article
ok 339 - article styles scope the reading look under .bob-article
  ---
  duration_ms: 0.85944
  ...
# Subtest: look settings default to serif typeface and stale-number hints
ok 340 - look settings default to serif typeface and stale-number hints
  ---
  duration_ms: 0.234447
  ...
# Subtest: folds embed, struck, and plain legacy children into one canonical line
ok 341 - folds embed, struck, and plain legacy children into one canonical line
  ---
  duration_ms: 227.448135
  ...
# Subtest: legacy-label row links come first, then legacy children in order
ok 342 - legacy-label row links come first, then legacy children in order
  ---
  duration_ms: 3.819902
  ...
# Subtest: R2 adopts field-only open dependents; unadoptable ids stay warned
ok 343 - R2 adopts field-only open dependents; unadoptable ids stay warned
  ---
  duration_ms: 5.534203
  ...
# Subtest: closed dependents gain the line but keep the field untouched
ok 344 - closed dependents gain the line but keep the field untouched
  ---
  duration_ms: 2.388359
  ...
# Subtest: open dependents drop stale field ids and stamp targets missing [id::]
ok 345 - open dependents drop stale field ids and stamp targets missing [id::]
  ---
  duration_ms: 2.769326
  ...
# Subtest: unresolved links stay verbatim and keep field ids as breadcrumbs
ok 346 - unresolved links stay verbatim and keep field ids as breadcrumbs
  ---
  duration_ms: 1.212495
  ...
# Subtest: leaves \#^ref embeds, non-task parents, fences, and conflict children alone
ok 347 - leaves \#^ref embeds, non-task parents, fences, and conflict children alone
  ---
  duration_ms: 1.376227
  ...
# Subtest: malformed rows leave the whole dependent alone
ok 348 - malformed rows leave the whole dependent alone
  ---
  duration_ms: 0.926959
  ...
# Subtest: R9 deletes label-only rows and removes the open field
ok 349 - R9 deletes label-only rows and removes the open field
  ---
  duration_ms: 1.33602
  ...
# Subtest: cross-note links use the shortest unambiguous form
ok 350 - cross-note links use the shortest unambiguous form
  ---
  duration_ms: 1.240318
  ...
# Subtest: ambiguous basenames fall back to the full path
ok 351 - ambiguous basenames fall back to the full path
  ---
  duration_ms: 0.700587
  ...
# Subtest: duplicate ids are ambiguous and fatal for --write
ok 352 - duplicate ids are ambiguous and fatal for --write
  ---
  duration_ms: 0.611968
  ...
# Subtest: archive targets keep the done/ path and are never stamped
ok 353 - archive targets keep the done/ path and are never stamped
  ---
  duration_ms: 0.726436
  ...
# Subtest: self links stay on the line but are not projected
ok 354 - self links stay on the line but are not projected
  ---
  duration_ms: 0.833591
  ...
# Subtest: non-task targets stay on the line but are not projected
ok 355 - non-task targets stay on the line but are not projected
  ---
  duration_ms: 1.207525
  ...
# Subtest: preserves CRLF, missing final newline, and cancel-log position
ok 356 - preserves CRLF, missing final newline, and cancel-log position
  ---
  duration_ms: 0.998636
  ...
# Subtest: migration is idempotent
ok 357 - migration is idempotent
  ---
  duration_ms: 1.93348
  ...
# Subtest: parseArgs handles --vault, --write, --help, and rejects unknowns
ok 358 - parseArgs handles --vault, --write, --help, and rejects unknowns
  ---
  duration_ms: 1.342041
  ...
# Subtest: BOB_CLI_DIR wins over a sibling checkout and a cache
ok 359 - BOB_CLI_DIR wins over a sibling checkout and a cache
  ---
  duration_ms: 47.512943
  ...
# Subtest: sibling bob-cli is used when BOB_CLI_DIR is unset
ok 360 - sibling bob-cli is used when BOB_CLI_DIR is unset
  ---
  duration_ms: 27.164292
  ...
# Subtest: an invalid BOB_CLI_DIR does not fall through
ok 361 - an invalid BOB_CLI_DIR does not fall through
  ---
  duration_ms: 21.712116
  ...
# Subtest: cache clone is used when no user-owned checkout exists
ok 362 - cache clone is used when no user-owned checkout exists
  ---
  duration_ms: 41.435522
  ...
# Subtest: refreshing an existing cache keeps git chatter off stdout and forwards exact paths
ok 363 - refreshing an existing cache keeps git chatter off stdout and forwards exact paths
  ---
  duration_ms: 46.327271
  ...
# Subtest: a cache clone with a foreign origin fails before fetch or reset
ok 364 - a cache clone with a foreign origin fails before fetch or reset
  ---
  duration_ms: 25.790888
  ...
# Subtest: a justfile alone is rejected as an explicit bob-cli checkout
ok 365 - a justfile alone is rejected as an explicit bob-cli checkout
  ---
  duration_ms: 18.397008
  ...
# Subtest: just failures propagate
ok 366 - just failures propagate
  ---
  duration_ms: 24.095784
  ...
# Subtest: scans multiline, one-line, and guarded literal registrations
ok 367 - scans multiline, one-line, and guarded literal registrations
  ---
  duration_ms: 5.435445
  ...
# Subtest: scans an optional addCommand call
ok 368 - scans an optional addCommand call
  ---
  duration_ms: 0.396056
  ...
# Subtest: allows addCommand references only in a typeof guard
ok 369 - allows addCommand references only in a typeof guard
  ---
  duration_ms: 0.56025
  ...
# Subtest: rejects bind, call, and aliased addCommand references with source locations
ok 370 - rejects bind, call, and aliased addCommand references with source locations
  ---
  duration_ms: 0.862255
  ...
# Subtest: expands literal command data from a constant-array forEach across source files
ok 371 - expands literal command data from a constant-array forEach across source files
  ---
  duration_ms: 0.768787
  ...
# Subtest: balances nested callback syntax and ignores misleading comments, strings, templates, and regexes
ok 372 - balances nested callback syntax and ignores misleading comments, strings, templates, and regexes
  ---
  duration_ms: 1.196374
  ...
# Subtest: decodes escaped string metadata and literal default hotkeys
ok 373 - decodes escaped string metadata and literal default hotkeys
  ---
  duration_ms: 0.666552
  ...
# Subtest: returns no commands for a plugin without registrations
ok 374 - returns no commands for a plugin without registrations
  ---
  duration_ms: 0.204942
  ...
# Subtest: fails with source locations for dynamic metadata, hotkeys, and malformed tables
ok 375 - fails with source locations for dynamic metadata, hotkeys, and malformed tables
  ---
  duration_ms: 3.068357
  ...
# Subtest: fails duplicate command ids with both registration locations
ok 376 - fails duplicate command ids with both registration locations
  ---
  duration_ms: 0.668476
  ...
# Subtest: checks drift without writes, preserves prose, and generates deterministically
ok 377 - checks drift without writes, preserves prose, and generates deterministically
  ---
  duration_ms: 19.975088
  ...
# Subtest: code-span table cells preserve backslashes and use a safe backtick fence
ok 378 - code-span table cells preserve backslashes and use a safe backtick fence
  ---
  duration_ms: 4.559422
  ...
# Subtest: does not write any output when source validation fails
ok 379 - does not write any output when source validation fails
  ---
  duration_ms: 3.1798
  ...
# Subtest: BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
ok 380 - BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
  ---
  duration_ms: 11.436771
  ...
# Subtest: reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
ok 381 - reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
  ---
  duration_ms: 11.308507
  ...
# Subtest: stale, missing, canonical append, and frozen-owner models (BC8-BC10)
ok 382 - stale, missing, canonical append, and frozen-owner models (BC8-BC10)
  ---
  duration_ms: 1.622096
  ...
# Subtest: Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
ok 383 - Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
  ---
  duration_ms: 27.237101
  ...
# Subtest: budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
ok 384 - budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
  ---
  duration_ms: 3.241748
  ...
# Subtest: chip builder includes the 🔑 badge and has no edit controls
ok 385 - chip builder includes the 🔑 badge and has no edit controls
  ---
  duration_ms: 2.119065
  ...
# Subtest: RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
ok 386 - RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
  ---
  duration_ms: 3.813198
  ...
# Subtest: RBC2 hover × on a live chip calls removeDependent; notice is nav's
ok 387 - RBC2 hover × on a live chip calls removeDependent; notice is nav's
  ---
  duration_ms: 1.197195
  ...
# Subtest: RBC3 frozen, stale, and no api.blocks stay navigation-only
ok 388 - RBC3 frozen, stale, and no api.blocks stay navigation-only
  ---
  duration_ms: 1.38804
  ...
# Subtest: RBC4 Reading view matches Live Preview ＋ / ×
ok 389 - RBC4 Reading view matches Live Preview ＋ / ×
  ---
  duration_ms: 4.663863
  ...
# Subtest: collections namespace version is additive v1
ok 390 - collections namespace version is additive v1
  ---
  duration_ms: 2.243803
  ...
# Subtest: collection chip classes stay collection-specific through paint and refresh
ok 391 - collection chip classes stay collection-specific through paint and refresh
  ---
  duration_ms: 11.541741
  ...
# Subtest: projects: scalar resolved links count, lists never widen
ok 392 - projects: scalar resolved links count, lists never widen
  ---
  duration_ms: 0.599444
  ...
# Subtest: projects: templates, status, and containsAny edges
ok 393 - projects: templates, status, and containsAny edges
  ---
  duration_ms: 0.634912
  ...
# Subtest: references: exact prefix, md only, exact scalar status
ok 394 - references: exact prefix, md only, exact scalar status
  ---
  duration_ms: 0.469737
  ...
# Subtest: base contracts: accept current files, reject drift, tolerate presentation
ok 395 - base contracts: accept current files, reject drift, tolerate presentation
  ---
  duration_ms: 1.536382
  ...
# Subtest: entries: true zero vs unavailable with reason, failure isolation
ok 396 - entries: true zero vs unavailable with reason, failure isolation
  ---
  duration_ms: 0.557634
  ...
# Subtest: snapshot counts both collections once, true zero stays clickable
ok 397 - snapshot counts both collections once, true zero stays clickable
  ---
  duration_ms: 0.61313
  ...
# Subtest: snapshot never presents partial counts as final
ok 398 - snapshot never presents partial counts as final
  ---
  duration_ms: 0.542586
  ...
# Subtest: changed definitions fail closed per collection, never stale
ok 399 - changed definitions fail closed per collection, never stale
  ---
  duration_ms: 0.531004
  ...
# Subtest: renderChip links, labels, and cleans up per component
ok 400 - renderChip links, labels, and cleans up per component
  ---
  duration_ms: 1.265536
  ...
# Subtest: PENDING section excludes TODAY while the whole lane keeps it
ok 401 - PENDING section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 5.087372
  ...
# Subtest: NEXT section excludes TODAY while the whole lane keeps it
ok 402 - NEXT section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 0.751324
  ...
# Subtest: NEXT uses symbol *, not name matching
ok 403 - NEXT uses symbol *, not name matching
  ---
  duration_ms: 0.505244
  ...
# Subtest: READY badge and query agree on hide and path case variants
ok 404 - READY badge and query agree on hide and path case variants
  ---
  duration_ms: 1.075323
  ...
# Subtest: blocked uses the full list even outside the visible subset
ok 405 - blocked uses the full list even outside the visible subset
  ---
  duration_ms: 0.404312
  ...
# Subtest: duplicate block IDs, missing IDs, and reused objects stay per-row
ok 406 - duplicate block IDs, missing IDs, and reused objects stay per-row
  ---
  duration_ms: 0.584415
  ...
# Subtest: READY gating keeps exempt rows and drops NEW/ROTTEN
ok 407 - READY gating keeps exempt rows and drops NEW/ROTTEN
  ---
  duration_ms: 0.539239
  ...
# Subtest: throwing Today degrades to unavailable, never zero
ok 408 - throwing Today degrades to unavailable, never zero
  ---
  duration_ms: 15.594196
  ...
# Subtest: dashboard badges color the displayed section count and label whole-lane pressure
ok 409 - dashboard badges color the displayed section count and label whole-lane pressure
  ---
  duration_ms: 0.801239
  ...
# Subtest: dashboard section warning boundaries ignore TODAY-only whole-lane excess
ok 410 - dashboard section warning boundaries ignore TODAY-only whole-lane excess
  ---
  duration_ms: 1.260767
  ...
# Subtest: dashboard lane badge keeps unavailable data neutral
ok 411 - dashboard lane badge keeps unavailable data neutral
  ---
  duration_ms: 0.447785
  ...
# Subtest: dashboard lane paint and refresh keep color aligned with the visible section
ok 412 - dashboard lane paint and refresh keep color aligned with the visible section
  ---
  duration_ms: 5.762541
  ...
# Subtest: dashboard lane widgets refresh together and prune on unload
ok 413 - dashboard lane widgets refresh together and prune on unload
  ---
  duration_ms: 3.744057
  ...
# Subtest: daily paint matches dashboard section badges on screenshot fixtures
ok 414 - daily paint matches dashboard section badges on screenshot fixtures
  ---
  duration_ms: 46.664363
  ...
# Subtest: daily paint lane lint matches a red badge section count
ok 415 - daily paint lane lint matches a red badge section count
  ---
  duration_ms: 11.140185
  ...
# Subtest: daily and dashboard membership agree for exclusions and custom IN_PROGRESS
ok 416 - daily and dashboard membership agree for exclusions and custom IN_PROGRESS
  ---
  duration_ms: 6.78996
  ...
# Subtest: daily paint refreshes with dashboard when Today, lane, and cap change
ok 417 - daily paint refreshes with dashboard when Today, lane, and cap change
  ---
  duration_ms: 12.98725
  ...
# Subtest: older daily notes follow today's dashboard lanes
ok 418 - older daily notes follow today's dashboard lanes
  ---
  duration_ms: 6.038246
  ...
# Subtest: daily lane anchors keep shared navigation and reject stale paints
ok 419 - daily lane anchors keep shared navigation and reject stale paints
  ---
  duration_ms: 6.688407
  ...
# Subtest: daily paint stays unavailable until Tasks and Today are ready
ok 420 - daily paint stays unavailable until Tasks and Today are ready
  ---
  duration_ms: 3.346217
  ...
# Subtest: work tones: dashboard lane models carry section tones
ok 421 - work tones: dashboard lane models carry section tones
  ---
  duration_ms: 0.404563
  ...
# Subtest: T1 scheduled full-mode row gets a Fri mark inside the span
ok 422 - T1 scheduled full-mode row gets a Fri mark inside the span
  ---
  duration_ms: 4.922566
  ...
# Subtest: T2 done row maps to a completion Oct 5 mark
ok 423 - T2 done row maps to a completion Oct 5 mark
  ---
  duration_ms: 1.12691
  ...
# Subtest: T3 short-mode created span is left untouched by JS
ok 424 - T3 short-mode created span is left untouched by JS
  ---
  duration_ms: 0.483362
  ...
# Subtest: T4 pending row decorates once data-task appears; exhausted rows stay native
ok 425 - T4 pending row decorates once data-task appears; exhausted rows stay native
  ---
  duration_ms: 2.36296
  ...
# Subtest: T5 a second pass adds nothing
ok 426 - T5 a second pass adds nothing
  ---
  duration_ms: 0.726537
  ...
# Subtest: T6 task-due and task-start spans are untouched
ok 427 - T6 task-due and task-start spans are untouched
  ---
  duration_ms: 0.461511
  ...
# Subtest: T7 an invalid date is untouched
ok 428 - T7 an invalid date is untouched
  ---
  duration_ms: 0.377651
  ...
# Subtest: T8 nothing is scheduled with marks off or for connected non-Tasks elements
ok 429 - T8 nothing is scheduled with marks off or for connected non-Tasks elements
  ---
  duration_ms: 0.49741
  ...
# Subtest: T9 a Tasks-host Fri mark relabels to tomorrow on rollover
ok 430 - T9 a Tasks-host Fri mark relabels to tomorrow on rollover
  ---
  duration_ms: 1.038763
  ...
# Subtest: renderDateMarksIn schedules one shared frame for every row
ok 431 - renderDateMarksIn schedules one shared frame for every row
  ---
  duration_ms: 2.33129
  ...
# Subtest: the Tasks pass never throws on hostile input
ok 432 - the Tasks pass never throws on hostile input
  ---
  duration_ms: 0.652425
  ...
# Subtest: T10 real-DOM NodeList children decorate via direct and queued passes
ok 433 - T10 real-DOM NodeList children decorate via direct and queued passes
  ---
  duration_ms: 1.056266
  ...
# Subtest: T11 toggling off before a queued frame runs writes nothing
ok 434 - T11 toggling off before a queued frame runs writes nothing
  ---
  duration_ms: 1.171867
  ...
# Subtest: T12 a pending-row retry followed by disabling writes nothing
ok 435 - T12 a pending-row retry followed by disabling writes nothing
  ---
  duration_ms: 0.719012
  ...
# Subtest: T13 unloading before a callback runs writes nothing
ok 436 - T13 unloading before a callback runs writes nothing
  ---
  duration_ms: 2.516063
  ...
# Subtest: RT1 full-mode recurring result gets a daily mark and stays idempotent
ok 437 - RT1 full-mode recurring result gets a daily mark and stays idempotent
  ---
  duration_ms: 2.073208
  ...
# Subtest: RT2 recurring labels use the shared cadence grammar
ok 438 - RT2 recurring labels use the shared cadence grammar
  ---
  duration_ms: 1.887293
  ...
# Subtest: RT2a unknown inherited-name rules stay readable in Tasks results
ok 439 - RT2a unknown inherited-name rules stay readable in Tasks results
  ---
  duration_ms: 1.129977
  ...
# Subtest: RT3 short-mode recurring spans stay native to JS and use the CSS loop
ok 440 - RT3 short-mode recurring spans stay native to JS and use the CSS loop
  ---
  duration_ms: 1.505172
  ...
# Subtest: RT4 open checklist members keep recurrence pills without `when done`
ok 441 - RT4 open checklist members keep recurrence pills without `when done`
  ---
  duration_ms: 0.838099
  ...
# Subtest: RT5 invalid recurrence stays native and incomplete rows are retried
ok 442 - RT5 invalid recurrence stays native and incomplete rows are retried
  ---
  duration_ms: 1.005099
  ...
# Subtest: styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
ok 443 - styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
  ---
  duration_ms: 1.200752
  ...
# Subtest: DATE_MARK_FIELDS lists the four dates with verbs
ok 444 - DATE_MARK_FIELDS lists the four dates with verbs
  ---
  duration_ms: 3.730822
  ...
# Subtest: DM1 created today: label, tooltip, fold, quiet field
ok 445 - DM1 created today: label, tooltip, fold, quiet field
  ---
  duration_ms: 2.396324
  ...
# Subtest: DM2 created yesterday without space after the colons
ok 446 - DM2 created yesterday without space after the colons
  ---
  duration_ms: 0.716548
  ...
# Subtest: DM3-DM6 scheduled tomorrow, weekday, and month/day labels
ok 447 - DM3-DM6 scheduled tomorrow, weekday, and month/day labels
  ---
  duration_ms: 0.441072
  ...
# Subtest: DM7 scheduled today reads with emphasis timing
ok 448 - DM7 scheduled today reads with emphasis timing
  ---
  duration_ms: 0.338246
  ...
# Subtest: DM8 past scheduled uses month/day, never a weekday
ok 449 - DM8 past scheduled uses month/day, never a weekday
  ---
  duration_ms: 0.265777
  ...
# Subtest: DM9 completion on a closed task keeps the timeline grammar
ok 450 - DM9 completion on a closed task keeps the timeline grammar
  ---
  duration_ms: 0.342423
  ...
# Subtest: DM10 cancelled across years appends the year
ok 451 - DM10 cancelled across years appends the year
  ---
  duration_ms: 0.280645
  ...
# Subtest: DM11 next-year date appends the year
ok 452 - DM11 next-year date appends the year
  ---
  duration_ms: 0.470257
  ...
# Subtest: DM12 the weekday rule wins across the year boundary
ok 453 - DM12 the weekday rule wins across the year boundary
  ---
  duration_ms: 0.415584
  ...
# Subtest: DM13 two marks in order with folds 1 and 2
ok 454 - DM13 two marks in order with folds 1 and 2
  ---
  duration_ms: 0.564277
  ...
# Subtest: DM14 created and scheduled ranges stay disjoint from the fresh mark
ok 455 - DM14 created and scheduled ranges stay disjoint from the fresh mark
  ---
  duration_ms: 0.662434
  ...
# Subtest: DM15-DM16 paren and padded brackets are canonical
ok 456 - DM15-DM16 paren and padded brackets are canonical
  ---
  duration_ms: 0.450279
  ...
# Subtest: DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
ok 457 - DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
  ---
  duration_ms: 0.750763
  ...
# Subtest: DM22 code still parses pure but decorates nothing (see Live Preview)
ok 458 - DM22 code still parses pure but decorates nothing (see Live Preview)
  ---
  duration_ms: 0.2516
  ...
# Subtest: DM23 rescheduled is untouched and never a duplicate
ok 459 - DM23 rescheduled is untouched and never a duplicate
  ---
  duration_ms: 0.383693
  ...
# Subtest: DN1-DN9 non-canonical fields get no mark
ok 460 - DN1-DN9 non-canonical fields get no mark
  ---
  duration_ms: 0.623901
  ...
# Subtest: dateMarkContentStart finds content on list, quoted, and plain lines
ok 461 - dateMarkContentStart finds content on list, quoted, and plain lines
  ---
  duration_ms: 0.56064
  ...
# Subtest: dateMarkRelativePhrase covers the exact-day phrases
ok 462 - dateMarkRelativePhrase covers the exact-day phrases
  ---
  duration_ms: 0.237163
  ...
# Subtest: dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
ok 463 - dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
  ---
  duration_ms: 0.752878
  ...
# Subtest: no model output contains a double colon
ok 464 - no model output contains a double colon
  ---
  duration_ms: 3.001138
  ...
# Subtest: a new day always changes the widget key
ok 465 - a new day always changes the widget key
  ---
  duration_ms: 0.385166
  ...
# Subtest: element structure and the decorative/inheritColor/rendered options
ok 466 - element structure and the decorative/inheritColor/rendered options
  ---
  duration_ms: 1.026129
  ...
# Subtest: Live Preview emits several decorations in ascending order
ok 467 - Live Preview emits several decorations in ascending order
  ---
  duration_ms: 3.145364
  ...
# Subtest: Live Preview reveals per field, never the whole line
ok 468 - Live Preview reveals per field, never the whole line
  ---
  duration_ms: 0.51848
  ...
# Subtest: Live Preview refuses source mode, code, and disabled marks
ok 469 - Live Preview refuses source mode, code, and disabled marks
  ---
  duration_ms: 0.830916
  ...
# Subtest: widget mousedown anchors at the field start for folds 0, 1, and 2
ok 470 - widget mousedown anchors at the field start for folds 0, 1, and 2
  ---
  duration_ms: 1.918201
  ...
# Subtest: DM24 a cursor in the folded run unfolds the mark (vim cw)
ok 471 - DM24 a cursor in the folded run unfolds the mark (vim cw)
  ---
  duration_ms: 0.758778
  ...
# Subtest: DM25 a cursor in Tasks double space unfolds only that field
ok 472 - DM25 a cursor in Tasks double space unfolds only that field
  ---
  duration_ms: 0.370277
  ...
# Subtest: a selection ending inside the run unfolds; ending at its start keeps the fold
ok 473 - a selection ending inside the run unfolds; ending at its start keeps the fold
  ---
  duration_ms: 0.46104
  ...
# Subtest: no emitted decoration ever hides a cursor, and reveal still means field overlap
ok 474 - no emitted decoration ever hides a cursor, and reveal still means field overlap
  ---
  duration_ms: 17.468534
  ...
# Subtest: dateMarkSelectionFold: reveal, unfold, fold, and garbage input
ok 475 - dateMarkSelectionFold: reveal, unfold, fold, and garbage input
  ---
  duration_ms: 0.45564
  ...
# Subtest: mousedown on an unfolded (fold-0) widget anchors at the field start
ok 476 - mousedown on an unfolded (fold-0) widget anchors at the field start
  ---
  duration_ms: 1.121881
  ...
# Subtest: rendered views split several fields in one node
ok 477 - rendered views split several fields in one node
  ---
  duration_ms: 3.093997
  ...
# Subtest: rendered views skip exclusions and duplicates
ok 478 - rendered views skip exclusions and duplicates
  ---
  duration_ms: 0.70746
  ...
# Subtest: RO1 rendered marks relabel in place across midnight
ok 479 - RO1 rendered marks relabel in place across midnight
  ---
  duration_ms: 0.941016
  ...
# Subtest: rollover dispatches once per day change and never touches widgets
ok 480 - rollover dispatches once per day change and never touches widgets
  ---
  duration_ms: 0.78046
  ...
# Subtest: api.dateMarks v1 is additive, sync, and never throwing
ok 481 - api.dateMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 1.054853
  ...
# Subtest: session toggle and onload wiring
ok 482 - session toggle and onload wiring
  ---
  duration_ms: 17.409391
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 483 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 0.734512
  ...
# Subtest: styles.css contract: masks, tones, repair flag, resting
ok 484 - styles.css contract: masks, tones, repair flag, resting
  ---
  duration_ms: 1.220219
  ...
# Subtest: day identity follows the canonical path, never the tab or mtime
ok 485 - day identity follows the canonical path, never the tab or mtime
  ---
  duration_ms: 2.878073
  ...
# Subtest: fence day parsing accepts YAML mappings and plain lines, nothing else
ok 486 - fence day parsing accepts YAML mappings and plain lines, nothing else
  ---
  duration_ms: 0.967777
  ...
# Subtest: report selection reads the default entry, an 8-day range, or nothing
ok 487 - report selection reads the default entry, an 8-day range, or nothing
  ---
  duration_ms: 16.331764
  ...
# Subtest: report window checks keep the page window only when it shows D
ok 488 - report window checks keep the page window only when it shows D
  ---
  duration_ms: 2.809133
  ...
# Subtest: paint from cache costs one frame and zero spawns
ok 489 - paint from cache costs one frame and zero spawns
  ---
  duration_ms: 44.801357
  ...
# Subtest: off-screen and hidden-tab strips spawn nothing
ok 490 - off-screen and hidden-tab strips spawn nothing
  ---
  duration_ms: 142.875962
  ...
# Subtest: clean fresh entries never refetch, whatever changes
ok 491 - clean fresh entries never refetch, whatever changes
  ---
  duration_ms: 102.025057
  ...
# Subtest: visible changing strips spawn at most once per 30 s
ok 492 - visible changing strips spawn at most once per 30 s
  ---
  duration_ms: 199.229231
  ...
# Subtest: the 10-minute age rule refetches today without any change
ok 493 - the 10-minute age rule refetches today without any change
  ---
  duration_ms: 67.583754
  ...
# Subtest: past days wait out the 10-minute gate
ok 494 - past days wait out the 10-minute gate
  ---
  duration_ms: 89.284337
  ...
# Subtest: several strips and the page share one spawn per key
ok 495 - several strips and the page share one spawn per key
  ---
  duration_ms: 70.233763
  ...
# Subtest: strips repaint for free when the page refreshes the shared key
ok 496 - strips repaint for free when the page refreshes the shared key
  ---
  duration_ms: 107.313571
  ...
# Subtest: rollover re-keys today to a past day and refetches
ok 497 - rollover re-keys today to a past day and refetches
  ---
  duration_ms: 102.554257
  ...
# Subtest: a stale-across-midnight report is never shown as so far
ok 498 - a stale-across-midnight report is never shown as so far
  ---
  duration_ms: 69.321551
  ...
# Subtest: window-edge days fetch the 8-day range
ok 499 - window-edge days fetch the 8-day range
  ---
  duration_ms: 71.333322
  ...
# Subtest: future days render nothing and spawn nothing
ok 500 - future days render nothing and spawn nothing
  ---
  duration_ms: 22.755857
  ...
# Subtest: a failed refresh keeps the frame and shows the stale dot
ok 501 - a failed refresh keeps the frame and shows the stale dot
  ---
  duration_ms: 96.363769
  ...
# Subtest: a failure with nothing cached shows the one-line error and Retry
ok 502 - a failure with nothing cached shows the one-line error and Retry
  ---
  duration_ms: 138.713046
  ...
# Subtest: bob-not-found with nothing cached names stats.bob_path
ok 503 - bob-not-found with nothing cached names stats.bob_path
  ---
  duration_ms: 65.740397
  ...
# Subtest: the fence parses day:, falls back to the note date, or explains itself
ok 504 - the fence parses day:, falls back to the note date, or explains itself
  ---
  duration_ms: 91.510996
  ...
# Subtest: the fence skips hover popovers and embeds, and unregisters on unload
ok 505 - the fence skips hover popovers and embeds, and unregisters on unload
  ---
  duration_ms: 4.759885
  ...
# Subtest: openStatsForDay pins the day, focuses the metric, and opens a new tab
ok 506 - openStatsForDay pins the day, focuses the metric, and opens a new tab
  ---
  duration_ms: 2.46752
  ...
# Subtest: openStatsForDay keeps the page window when it already shows D
ok 507 - openStatsForDay keeps the page window when it already shows D
  ---
  duration_ms: 66.48595
  ...
# Subtest: openStatsForDay Notices when Stats cannot open
ok 508 - openStatsForDay Notices when Stats cannot open
  ---
  duration_ms: 6.178183
  ...
# Subtest: the page honours a pinned day on its first paint
ok 509 - the page honours a pinned day on its first paint
  ---
  duration_ms: 63.288397
  ...
# Subtest: renderStatsResult consumes the one-shot revealPanel
ok 510 - renderStatsResult consumes the one-shot revealPanel
  ---
  duration_ms: 8.628068
  ...
# Subtest: every strip paints facts and links with no buttons and no vault writes
ok 511 - every strip paints facts and links with no buttons and no vault writes
  ---
  duration_ms: 67.26614
  ...
# Subtest: change bursts coalesce behind one trailing quiet window
ok 512 - change bursts coalesce behind one trailing quiet window
  ---
  duration_ms: 116.553097
  ...
# Subtest: mobile and spawn-less hosts render nothing and spawn nothing
ok 513 - mobile and spawn-less hosts render nothing and spawn nothing
  ---
  duration_ms: 35.250166
  ...
# Subtest: rollover synchronously skeletons visible and offscreen fences; visible refetch resolves as past
ok 514 - rollover synchronously skeletons visible and offscreen fences; visible refetch resolves as past
  ---
  duration_ms: 185.054073
  ...
# Subtest: require time adds no eager StateEffect.define()
ok 515 - require time adds no eager StateEffect.define()
  ---
  duration_ms: 2.02212
  ...
# Subtest: renderPlanBlock puts exactly one host first with .bob-plan after it on canonical days
ok 516 - renderPlanBlock puts exactly one host first with .bob-plan after it on canonical days
  ---
  duration_ms: 95.549155
  ...
# Subtest: non-daily, future, dashboard, mobile, spawn-less, and excluded blocks get no host
ok 517 - non-daily, future, dashboard, mobile, spawn-less, and excluded blocks get no host
  ---
  duration_ms: 224.043236
  ...
# Subtest: paintPlanBlock keeps the same host node first with .bob-plan after it and no strip repaint or spawn
ok 518 - paintPlanBlock keeps the same host node first with .bob-plan after it and no strip repaint or spawn
  ---
  duration_ms: 254.151568
  ...
# Subtest: toggle and stats.day_strip remove the host and class, re-enabling restores them
ok 519 - toggle and stats.day_strip remove the host and class, re-enabling restores them
  ---
  duration_ms: 117.30905
  ...
# Subtest: unload releases the record and its observer
ok 520 - unload releases the record and its observer
  ---
  duration_ms: 34.344969
  ...
# Subtest: rollover attaches future blocks and repaints today as a past day
ok 521 - rollover attaches future blocks and repaints today as a past day
  ---
  duration_ms: 106.983742
  ...
# Subtest: rollover skeletons a visible automatic today host synchronously; it resolves as past
ok 522 - rollover skeletons a visible automatic today host synchronously; it resolves as past
  ---
  duration_ms: 229.218874
  ...
# Subtest: plan hosts never write the vault or journals
ok 523 - plan hosts never write the vault or journals
  ---
  duration_ms: 131.458019
  ...
# Subtest: cold plan host waits for visibility: no spawn before callback, false stays zero, true fetches once
ok 524 - cold plan host waits for visibility: no spawn before callback, false stays zero, true fetches once
  ---
  duration_ms: 166.217658
  ...
# Subtest: plan host paints synchronously from cache with zero spawn before visibility
ok 525 - plan host paints synchronously from cache with zero spawn before visibility
  ---
  duration_ms: 38.663271
  ...
# Subtest: detached excluded blocks get no host; detached ordinary blocks attach synchronously
ok 526 - detached excluded blocks get no host; detached ordinary blocks attach synchronously
  ---
  duration_ms: 204.798011
  ...
# Subtest: no-observer fallback attaches detached, fetches on check after connect, releases excluded
ok 527 - no-observer fallback attaches detached, fetches on check after connect, releases excluded
  ---
  duration_ms: 276.076307
  ...
# Subtest: excluded after attach releases on the first observer callback
ok 528 - excluded after attach releases on the first observer callback
  ---
  duration_ms: 194.666021
  ...
# Subtest: excluded processor container gets no host
ok 529 - excluded processor container gets no host
  ---
  duration_ms: 41.187881
  ...
# Subtest: reading-view order attaches detached, virtualized stays quiet until attach
ok 530 - reading-view order attaches detached, virtualized stays quiet until attach
  ---
  duration_ms: 165.376613
  ...
# Subtest: today host shows so far HH:MM from the fetch stamp
ok 531 - today host shows so far HH:MM from the fetch stamp
  ---
  duration_ms: 117.01511
  ...
# Subtest: failed refresh over a cached report names the HH:MM it shows
ok 532 - failed refresh over a cached report names the HH:MM it shows
  ---
  duration_ms: 176.30942
  ...
# Subtest: placeholder finds .bob-plan by class and toggle-off restores it first
ok 533 - placeholder finds .bob-plan by class and toggle-off restores it first
  ---
  duration_ms: 64.332008
  ...
# Subtest: date words and day shifts use calendar integers, including leap day
ok 534 - date words and day shifts use calendar integers, including leap day
  ---
  duration_ms: 2.003885
  ...
# Subtest: fact displays are selected from the exact day point, even with null headline and grouped input
ok 535 - fact displays are selected from the exact day point, even with null headline and grouped input
  ---
  duration_ms: 4.518054
  ...
# Subtest: honest states carry meta text for today, past, stale today, and stale past
ok 536 - honest states carry meta text for today, past, stale today, and stale past
  ---
  duration_ms: 2.254814
  ...
# Subtest: time mix reuses Stats area ordering and hues, with buckets last and a tooltip title
ok 537 - time mix reuses Stats area ordering and hues, with buckets last and a tooltip title
  ---
  duration_ms: 16.317437
  ...
# Subtest: root_parent is preferred with an honest area fallback
ok 538 - root_parent is preferred with an honest area fallback
  ---
  duration_ms: 0.959041
  ...
# Subtest: zero worked renders no Pomodoros and redefined worked omits its mix
ok 539 - zero worked renders no Pomodoros and redefined worked omits its mix
  ---
  duration_ms: 1.237492
  ...
# Subtest: aria label carries the date, values, provisional state, and area names
ok 540 - aria label carries the date, values, provisional state, and area names
  ---
  duration_ms: 0.463184
  ...
# Subtest: skeleton carries placeholder text per fact and the same tag and class sequence
ok 541 - skeleton carries placeholder text per fact and the same tag and class sequence
  ---
  duration_ms: 1.961485
  ...
# Subtest: painter repaints in place, emits no buttons, and shows unavailable controls
ok 542 - painter repaints in place, emits no buttons, and shows unavailable controls
  ---
  duration_ms: 1.524681
  ...
# Subtest: facts, mix, and Retry preserve day, focus, and new-leaf modifiers
ok 543 - facts, mix, and Retry preserve day, focus, and new-leaf modifiers
  ---
  duration_ms: 1.958098
  ...
# Subtest: future and hidden models paint no children
ok 544 - future and hidden models paint no children
  ---
  duration_ms: 0.39791
  ...
# Subtest: strip paints facts, legend row, then full-width bar with no buttons
ok 545 - strip paints facts, legend row, then full-width bar with no buttons
  ---
  duration_ms: 0.722229
  ...
# Subtest: bar click opens Stats homes with day and new-leaf modifiers
ok 546 - bar click opens Stats homes with day and new-leaf modifiers
  ---
  duration_ms: 0.821858
  ...
# Subtest: same-area roots get distinct hues and legend dots match their segments
ok 547 - same-area roots get distinct hues and legend dots match their segments
  ---
  duration_ms: 1.49327
  ...
# Subtest: dayStripValueRuns splits numerals from units and keeps words whole
ok 548 - dayStripValueRuns splits numerals from units and keeps words whole
  ---
  duration_ms: 1.192607
  ...
# Subtest: facts stack a label head over a faithful value with warnings in the head
ok 549 - facts stack a label head over a faithful value with warnings in the head
  ---
  duration_ms: 21.270723
  ...
# Subtest: DP parse vectors
ok 550 - DP parse vectors
  ---
  duration_ms: 4.454782
  ...
# Subtest: DC chip model vectors
ok 551 - DC chip model vectors
  ---
  duration_ms: 3.204857
  ...
# Subtest: decoration builds one widget, reveals on cursor, skips code and ranges
ok 552 - decoration builds one widget, reveals on cursor, skips code and ranges
  ---
  duration_ms: 12.987281
  ...
# Subtest: decoration skips paragraphs, grandchildren, and Work Log lines
ok 553 - decoration skips paragraphs, grandchildren, and Work Log lines
  ---
  duration_ms: 2.243392
  ...
# Subtest: decoration renders chips on DP30 and still skips DP20
ok 554 - decoration renders chips on DP30 and still skips DP20
  ---
  duration_ms: 1.599414
  ...
# Subtest: ownership check reads O(depth) lines, not the whole note
ok 555 - ownership check reads O(depth) lines, not the whole note
  ---
  duration_ms: 2.178639
  ...
# Subtest: widget identity covers the line and the interactive flag
ok 556 - widget identity covers the line and the interactive flag
  ---
  duration_ms: 2.674465
  ...
# Subtest: element hides actions without nav api v1
ok 557 - element hides actions without nav api v1
  ---
  duration_ms: 3.784434
  ...
# Subtest: nav api feature detection gates actions
ok 558 - nav api feature detection gates actions
  ---
  duration_ms: 0.680238
  ...
# Subtest: reading view decorates only the Depends-On row, hides chrome, stays idempotent
ok 559 - reading view decorates only the Depends-On row, hides chrome, stays idempotent
  ---
  duration_ms: 6.052002
  ...
# Subtest: reading view collapses more than three Done targets to one chip
ok 560 - reading view collapses more than three Done targets to one chip
  ---
  duration_ms: 3.360014
  ...
# Subtest: DC chip model vectors by id: DC2, DC5, DC6, DC9
ok 561 - DC chip model vectors by id: DC2, DC5, DC6, DC9
  ---
  duration_ms: 0.652335
  ...
# Subtest: chip actions send the 0-based line index through nav api v1
ok 562 - chip actions send the 0-based line index through nav api v1
  ---
  duration_ms: 3.379911
  ...
# Subtest: chip hover passes the chip element and its row to the preview
ok 563 - chip hover passes the chip element and its row to the preview
  ---
  duration_ms: 0.602349
  ...
# Subtest: chip lookup index lives on the freshness memo
ok 564 - chip lookup index lives on the freshness memo
  ---
  duration_ms: 1.314228
  ...
# Subtest: reading view hides actions when the line cannot be derived
ok 565 - reading view hides actions when the line cannot be derived
  ---
  duration_ms: 30.633774
  ...
# Subtest: reading view actions carry the derived 0-based line
ok 566 - reading view actions carry the derived 0-based line
  ---
  duration_ms: 9.141941
  ...
# Subtest: reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
ok 567 - reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
  ---
  duration_ms: 1.590345
  ...
# Subtest: reading view renders chips on DP30 (owner is a task under a Work Log entry)
ok 568 - reading view renders chips on DP30 (owner is a task under a Work Log entry)
  ---
  duration_ms: 7.612741
  ...
# Subtest: reading view DP30 row actions send the owned Depends-On line
ok 569 - reading view DP30 row actions send the owned Depends-On line
  ---
  duration_ms: 5.81429
  ...
# Subtest: reading view second-row remove sends the second line when two tasks share a prerequisite
ok 570 - reading view second-row remove sends the second line when two tasks share a prerequisite
  ---
  duration_ms: 8.323948
  ...
# Subtest: chip lookup index builds once per freshness memo
ok 571 - chip lookup index builds once per freshness memo
  ---
  duration_ms: 1.128715
  ...
# Subtest: decoration evaluates ownership without copying the note
ok 572 - decoration evaluates ownership without copying the note
  ---
  duration_ms: 0.868718
  ...
# Subtest: toggle flips the body class and onload wires chips
ok 573 - toggle flips the body class and onload wires chips
  ---
  duration_ms: 10.028362
  ...
# Subtest: capability: nav card v2 is capable
ok 574 - capability: nav card v2 is capable
  ---
  duration_ms: 2.517366
  ...
# Subtest: capability: nav card v1 is not capable
ok 575 - capability: nav card v1 is not capable
  ---
  duration_ms: 0.218657
  ...
# Subtest: capability: absent nav, missing api, and old versions are not capable
ok 576 - capability: absent nav, missing api, and old versions are not capable
  ---
  duration_ms: 0.288391
  ...
# Subtest: capability: a throwing app never throws
ok 577 - capability: a throwing app never throws
  ---
  duration_ms: 0.28289
  ...
# Subtest: leaf: active capable due choice replaces refresh with a leaf
ok 578 - leaf: active capable due choice replaces refresh with a leaf
  ---
  duration_ms: 5.637289
  ...
# Subtest: leaf: the same row without the card keeps refresh and counting words
ok 579 - leaf: the same row without the card keeps refresh and counting words
  ---
  duration_ms: 0.763948
  ...
# Subtest: leaf: early dates still leaf when capable
ok 580 - leaf: early dates still leaf when capable
  ---
  duration_ms: 0.756684
  ...
# Subtest: leaf: decay-off rows never leaf even when capable
ok 581 - leaf: decay-off rows never leaf even when capable
  ---
  duration_ms: 0.799135
  ...
# Subtest: leaf: below-threshold rows never leaf
ok 582 - leaf: below-threshold rows never leaf
  ---
  duration_ms: 0.86955
  ...
# Subtest: leaf: threshold zero asks on every due re-confirmation when capable
ok 583 - leaf: threshold zero asks on every due re-confirmation when capable
  ---
  duration_ms: 0.728971
  ...
# Subtest: leaf: overflow renders capped dots with +N and the exact count in text
ok 584 - leaf: overflow renders capped dots with +N and the exact count in text
  ---
  duration_ms: 0.654679
  ...
# Subtest: leaf: out-of-scope and closed tasks show dots quietly, never a leaf
ok 585 - leaf: out-of-scope and closed tasks show dots quietly, never a leaf
  ---
  duration_ms: 1.376788
  ...
# Subtest: leaf: unresolved marks show dots quietly with counting-only wording
ok 586 - leaf: unresolved marks show dots quietly with counting-only wording
  ---
  duration_ms: 0.400815
  ...
# Subtest: element: leaf marks carry data-decide true and a leaf path
ok 587 - element: leaf marks carry data-decide true and a leaf path
  ---
  duration_ms: 1.258712
  ...
# Subtest: element: non-decision marks carry data-decide false
ok 588 - element: non-decision marks carry data-decide false
  ---
  duration_ms: 0.618821
  ...
# Subtest: footer groups omit every zero tier and keep walk order
ok 589 - footer groups omit every zero tier and keep walk order
  ---
  duration_ms: 4.634256
  ...
# Subtest: PRE and POST groups bracket the nine-tier queue and expose completion hints
ok 590 - PRE and POST groups bracket the nine-tier queue and expose completion hints
  ---
  duration_ms: 1.69715
  ...
# Subtest: a NEW-state project appears only in its walk tier
ok 591 - a NEW-state project appears only in its walk tier
  ---
  duration_ms: 0.342234
  ...
# Subtest: empty queue hides the footer even with upkeep or a met budget
ok 592 - empty queue hides the footer even with upkeep or a met budget
  ---
  duration_ms: 0.316794
  ...
# Subtest: unavailable or missing data never render false counts
ok 593 - unavailable or missing data never render false counts
  ---
  duration_ms: 0.451553
  ...
# Subtest: generic summary names due, commitments, and nonempty groups
ok 594 - generic summary names due, commitments, and nonempty groups
  ---
  duration_ms: 0.709124
  ...
# Subtest: current-task context uses shared ranks and compact wording
ok 595 - current-task context uses shared ranks and compact wording
  ---
  duration_ms: 1.322825
  ...
# Subtest: only ROTTEN remaining names commitments done or a met budget
ok 596 - only ROTTEN remaining names commitments done or a met budget
  ---
  duration_ms: 0.477501
  ...
# Subtest: NEW and commitments take precedence over a met budget
ok 597 - NEW and commitments take precedence over a met budget
  ---
  duration_ms: 0.477842
  ...
# Subtest: reviewEntryView compact and detail cover the original freshness tiers
ok 598 - reviewEntryView compact and detail cover the original freshness tiers
  ---
  duration_ms: 1.143934
  ...
# Subtest: cursor matching requires a unique verified identity
ok 599 - cursor matching requires a unique verified identity
  ---
  duration_ms: 0.66569
  ...
# Subtest: footer paint hides the host and keeps a stable button
ok 600 - footer paint hides the host and keeps a stable button
  ---
  duration_ms: 2.262258
  ...
# Subtest: status bar 0-1-0 transitions hide without a reload
ok 601 - status bar 0-1-0 transitions hide without a reload
  ---
  duration_ms: 25.064373
  ...
# Subtest: cursor-only updates reuse a warm memo
ok 602 - cursor-only updates reuse a warm memo
  ---
  duration_ms: 3.233802
  ...
# Subtest: unload disconnects the observer and click handler
ok 603 - unload disconnects the observer and click handler
  ---
  duration_ms: 2.904193
  ...
# Subtest: queue-built ranks agree with the footer current entry
ok 604 - queue-built ranks agree with the footer current entry
  ---
  duration_ms: 1.80755
  ...
# Subtest: footer short labels map every tier
ok 605 - footer short labels map every tier
  ---
  duration_ms: 0.295063
  ...
# Subtest: current-row footer context uses short labels while entry views keep full labels
ok 606 - current-row footer context uses short labels while entry views keep full labels
  ---
  duration_ms: 1.012864
  ...
# Subtest: legend line lists only current abbreviated tiers
ok 607 - legend line lists only current abbreviated tiers
  ---
  duration_ms: 0.767815
  ...
# Subtest: queue-row quickRoll preview takes the hint slot, tooltip, and aria
ok 608 - queue-row quickRoll preview takes the hint slot, tooltip, and aria
  ---
  duration_ms: 0.781722
  ...
# Subtest: quickRoll detail sits next to the action hint on lane rows
ok 609 - quickRoll detail sits next to the action hint on lane rows
  ---
  duration_ms: 0.600496
  ...
# Subtest: missing, failed, or off-row quickRoll leaves the footer byte-identical
ok 610 - missing, failed, or off-row quickRoll leaves the footer byte-identical
  ---
  duration_ms: 2.212182
  ...
# Subtest: PRE rows stay unchanged under the nav checklist-tier contract
ok 611 - PRE rows stay unchanged under the nav checklist-tier contract
  ---
  duration_ms: 0.535171
  ...
# Subtest: status bar wires nav api.quickRoll into the hint slot
ok 612 - status bar wires nav api.quickRoll into the hint slot
  ---
  duration_ms: 3.968995
  ...
# Subtest: status bar ignores missing, v0, or throwing quickRoll namespaces
ok 613 - status bar ignores missing, v0, or throwing quickRoll namespaces
  ---
  duration_ms: 8.661464
  ...
# Subtest: K1 absent: no keeps means 0 with no lints
ok 614 - K1 absent: no keeps means 0 with no lints
  ---
  duration_ms: 5.633122
  ...
# Subtest: K8 misplaced: keeps inside the Tasks suffix reads with a lint
ok 615 - K8 misplaced: keeps inside the Tasks suffix reads with a lint
  ---
  duration_ms: 0.945745
  ...
# Subtest: K9 duplicates and invalid values: first valid wins, else 0
ok 616 - K9 duplicates and invalid values: first valid wins, else 0
  ---
  duration_ms: 1.081865
  ...
# Subtest: K10 ceiling and NEW: 999 reads, never-confirmed reads 0
ok 617 - K10 ceiling and NEW: 999 reads, never-confirmed reads 0
  ---
  duration_ms: 0.516105
  ...
# Subtest: K13 exact keys: near-miss keys are not keeps; parens read
ok 618 - K13 exact keys: near-miss keys are not keeps; parens read
  ---
  duration_ms: 0.379775
  ...
# Subtest: keeps value parser accepts only decimal 1-999
ok 619 - keeps value parser accepts only decimal 1-999
  ---
  duration_ms: 0.374726
  ...
# Subtest: K2 first valid canonical: uncounted keep preserves and repairs
ok 620 - K2 first valid canonical: uncounted keep preserves and repairs
  ---
  duration_ms: 1.73904
  ...
# Subtest: K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
ok 621 - K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
  ---
  duration_ms: 0.883026
  ...
# Subtest: K4 same-day preserve noop: canonical kept line is byte-identical
ok 622 - K4 same-day preserve noop: canonical kept line is byte-identical
  ---
  duration_ms: 0.563736
  ...
# Subtest: K5 generic stamp clears, even same-day
ok 623 - K5 generic stamp clears, even same-day
  ---
  duration_ms: 0.692412
  ...
# Subtest: K6 set-refresh clears keeps
ok 624 - K6 set-refresh clears keeps
  ---
  duration_ms: 0.587731
  ...
# Subtest: K7 stale stamp clears keeps
ok 625 - K7 stale stamp clears keeps
  ---
  duration_ms: 0.364947
  ...
# Subtest: K8b misplaced keeps repaired to canonical order by a keep
ok 626 - K8b misplaced keeps repaired to canonical order by a keep
  ---
  duration_ms: 0.52927
  ...
# Subtest: K11 refusals preserve: closed and recurring lines never write
ok 627 - K11 refusals preserve: closed and recurring lines never write
  ---
  duration_ms: 0.610365
  ...
# Subtest: counted keep increments a stale streak once in the same write
ok 628 - counted keep increments a stale streak once in the same write
  ---
  duration_ms: 0.424551
  ...
# Subtest: first counted keep on a streakless due task writes keeps 1
ok 629 - first counted keep on a streakless due task writes keeps 1
  ---
  duration_ms: 0.561933
  ...
# Subtest: counted keep saturates at 999 and never wraps
ok 630 - counted keep saturates at 999 and never wraps
  ---
  duration_ms: 0.509383
  ...
# Subtest: counted keep needs a valid prior fresh before today
ok 631 - counted keep needs a valid prior fresh before today
  ---
  duration_ms: 0.999027
  ...
# Subtest: counted keep repairs malformed and duplicate placement
ok 632 - counted keep repairs malformed and duplicate placement
  ---
  duration_ms: 0.605957
  ...
# Subtest: uncounted keep preserves the valid value while canonicalizing
ok 633 - uncounted keep preserves the valid value while canonicalizing
  ---
  duration_ms: 0.897062
  ...
# Subtest: UB13 keep on an unblock TICKLER preserves the streak and skips the card
ok 634 - UB13 keep on an unblock TICKLER preserves the streak and skips the card
  ---
  duration_ms: 2.083236
  ...
# Subtest: a scheduled tickler still counts when schedule wins an unblock tie
ok 635 - a scheduled tickler still counts when schedule wins an unblock tie
  ---
  duration_ms: 0.641795
  ...
# Subtest: decay normalization: absent, null, true, and {} enable with 3
ok 636 - decay normalization: absent, null, true, and {} enable with 3
  ---
  duration_ms: 1.250687
  ...
# Subtest: decay false counts and displays but never asks
ok 637 - decay false counts and displays but never asks
  ---
  duration_ms: 0.245008
  ...
# Subtest: decay keeps 0 and fixed entry normalize
ok 638 - decay keeps 0 and fixed entry normalize
  ---
  duration_ms: 0.316784
  ...
# Subtest: invalid decay shapes fail the freshness config contract
ok 639 - invalid decay shapes fail the freshness config contract
  ---
  duration_ms: 0.594214
  ...
# Subtest: B: at-limit Ready due rows decide on every local day
ok 640 - B: at-limit Ready due rows decide on every local day
  ---
  duration_ms: 0.883697
  ...
# Subtest: D1 early date: an at-limit Ready due row decides
ok 641 - D1 early date: an at-limit Ready due row decides
  ---
  duration_ms: 0.253243
  ...
# Subtest: D2 at limit decides; D3 below limit stamps without a card
ok 642 - D2 at limit decides; D3 below limit stamps without a card
  ---
  duration_ms: 0.281528
  ...
# Subtest: D4 tickler counts as due; D5 NEW never decides
ok 643 - D4 tickler counts as due; D5 NEW never decides
  ---
  duration_ms: 0.227114
  ...
# Subtest: D6 zero limit asks on every due Ready re-confirmation
ok 644 - D6 zero limit asks on every due Ready re-confirmation
  ---
  duration_ms: 0.554418
  ...
# Subtest: D7 off never asks; D8 lane rows never decide
ok 645 - D7 off never asks; D8 lane rows never decide
  ---
  duration_ms: 0.373563
  ...
# Subtest: evaluator, queue, and counts carry keeps and decide
ok 646 - evaluator, queue, and counts carry keeps and decide
  ---
  duration_ms: 2.622285
  ...
# Subtest: no keeps: the existing mark is unchanged
ok 647 - no keeps: the existing mark is unchanged
  ---
  duration_ms: 2.276515
  ...
# Subtest: aging with two keeps: faint pips plus a counting-only line
ok 648 - aging with two keeps: faint pips plus a counting-only line
  ---
  duration_ms: 0.607409
  ...
# Subtest: confirmed today with two keeps: check glyph, faint dots
ok 649 - confirmed today with two keeps: check glyph, faint dots
  ---
  duration_ms: 0.800408
  ...
# Subtest: due below threshold: orange capsule keeps its glyph, adds dots
ok 650 - due below threshold: orange capsule keeps its glyph, adds dots
  ---
  duration_ms: 0.500365
  ...
# Subtest: resting marks show historical dots quietly and never decide
ok 651 - resting marks show historical dots quietly and never decide
  ---
  duration_ms: 0.565039
  ...
# Subtest: active decision due: data stays truthful, leaf stays gated
ok 652 - active decision due: data stays truthful, leaf stays gated
  ---
  duration_ms: 0.582
  ...
# Subtest: dot caps follow the threshold with +N overflow
ok 653 - dot caps follow the threshold with +N overflow
  ---
  duration_ms: 0.883316
  ...
# Subtest: keeps tooltip wording: singulars, zero threshold, off state
ok 654 - keeps tooltip wording: singulars, zero threshold, off state
  ---
  duration_ms: 0.251279
  ...
# Subtest: noncanonical keeps never fold but keep their repair pill
ok 655 - noncanonical keeps never fold but keep their repair pill
  ---
  duration_ms: 0.619613
  ...
# Subtest: quoted lines fold; rendered fragments fold without task checks
ok 656 - quoted lines fold; rendered fragments fold without task checks
  ---
  duration_ms: 5.476305
  ...
# Subtest: unresolved marks show the line's own pips quietly and never decide
ok 657 - unresolved marks show the line's own pips quietly and never decide
  ---
  duration_ms: 0.933712
  ...
# Subtest: consensus sees count and decision eligibility: ambiguity stays neutral
ok 658 - consensus sees count and decision eligibility: ambiguity stays neutral
  ---
  duration_ms: 1.327103
  ...
# Subtest: pips render as one aria-hidden span with the count in the label
ok 659 - pips render as one aria-hidden span with the count in the label
  ---
  duration_ms: 2.380194
  ...
# Subtest: Live Preview decorates the folded range including space and refresh
ok 660 - Live Preview decorates the folded range including space and refresh
  ---
  duration_ms: 9.220351
  ...
# Subtest: Live Preview reveals the raw field when the cursor overlaps either edge
ok 661 - Live Preview reveals the raw field when the cursor overlaps either edge
  ---
  duration_ms: 2.12182
  ...
# Subtest: Live Preview skips codeblock and inline code spans
ok 662 - Live Preview skips codeblock and inline code spans
  ---
  duration_ms: 1.176555
  ...
# Subtest: source mode and marks-off yield no decorations
ok 663 - source mode and marks-off yield no decorations
  ---
  duration_ms: 0.252592
  ...
# Subtest: update rebuilds on the refresh effect and widget eq is stable
ok 664 - update rebuilds on the refresh effect and widget eq is stable
  ---
  duration_ms: 1.985049
  ...
# Subtest: widget click reveals the field at the folded offset
ok 665 - widget click reveals the field at the folded offset
  ---
  duration_ms: 1.469355
  ...
# Subtest: line resolver prefers exact, then consensus, then unresolved
ok 666 - line resolver prefers exact, then consensus, then unresolved
  ---
  duration_ms: 2.30479
  ...
# Subtest: decoration builds reuse the snapshot without touching the loader
ok 667 - decoration builds reuse the snapshot without touching the loader
  ---
  duration_ms: 0.835275
  ...
# Subtest: rendered views split text nodes and skip excluded ancestors
ok 668 - rendered views split text nodes and skip excluded ancestors
  ---
  duration_ms: 3.657362
  ...
# Subtest: rendered views stay idempotent
ok 669 - rendered views stay idempotent
  ---
  duration_ms: 0.755121
  ...
# Subtest: text resolver reaches consensus and degrades to neutral
ok 670 - text resolver reaches consensus and degrades to neutral
  ---
  duration_ms: 1.105199
  ...
# Subtest: session toggle flips the body class and notifies
ok 671 - session toggle flips the body class and notifies
  ---
  duration_ms: 2.080982
  ...
# Subtest: Live Preview reads only the child block and never calls doc.toString
ok 672 - Live Preview reads only the child block and never calls doc.toString
  ---
  duration_ms: 2.77708
  ...
# Subtest: Live Preview stops at the first nonblank line at or above the task
ok 673 - Live Preview stops at the first nonblank line at or above the task
  ---
  duration_ms: 0.795157
  ...
# Subtest: Live Preview performance stays bounded on a large child block
ok 674 - Live Preview performance stays bounded on a large child block
  ---
  duration_ms: 1620.126616
  ...
# Subtest: reading view shows the rotten line and excludes Tasks and Dataview rows
ok 675 - reading view shows the rotten line and excludes Tasks and Dataview rows
  ---
  duration_ms: 1.373512
  ...
# Subtest: query-row consensus stays byte-identical with and without a Rotten Log
ok 676 - query-row consensus stays byte-identical with and without a Rotten Log
  ---
  duration_ms: 0.793014
  ...
# Subtest: onload registers the toggle, extension, and post-processor
ok 677 - onload registers the toggle, extension, and post-processor
  ---
  duration_ms: 13.575824
  ...
# Subtest: M1 today: check glyph, today label, full ring
ok 678 - M1 today: check glyph, today label, full ring
  ---
  duration_ms: 9.826157
  ...
# Subtest: M2 aging: ring glyph, 3d label, draining lease
ok 679 - M2 aging: ring glyph, 3d label, draining lease
  ---
  duration_ms: 0.9901
  ...
# Subtest: M3 boundary: ROTTEN due capsule with Alt+F hint
ok 680 - M3 boundary: ROTTEN due capsule with Alt+F hint
  ---
  duration_ms: 0.841606
  ...
# Subtest: checklist marks replace stamp hints with their completion tier
ok 681 - checklist marks replace stamp hints with their completion tier
  ---
  duration_ms: 1.430831
  ...
# Subtest: M4 yesterday uses the yesterday relative
ok 682 - M4 yesterday uses the yesterday relative
  ---
  duration_ms: 0.691921
  ...
# Subtest: M5 folded refresh shows the /14d suffix
ok 683 - M5 folded refresh shows the /14d suffix
  ---
  duration_ms: 1.185092
  ...
# Subtest: M6 refresh today: today tone hides the interval suffix
ok 684 - M6 refresh today: today tone hides the interval suffix
  ---
  duration_ms: 0.502289
  ...
# Subtest: M7 note interval stays tooltip-only
ok 685 - M7 note interval stays tooltip-only
  ---
  duration_ms: 0.613231
  ...
# Subtest: M8 resurfaced: due tone on the scheduled return
ok 686 - M8 resurfaced: due tone on the scheduled return
  ---
  duration_ms: 0.677924
  ...
# Subtest: M9 due NEXT lane with keep/release/today keys
ok 687 - M9 due NEXT lane with keep/release/today keys
  ---
  duration_ms: 0.638008
  ...
# Subtest: M10 NEXT lane stamped today
ok 688 - M10 NEXT lane stamped today
  ---
  duration_ms: 0.42914
  ...
# Subtest: M19 disabled Next lane rests
ok 689 - M19 disabled Next lane rests
  ---
  duration_ms: 0.5762
  ...
# Subtest: M20 PENDING lane folds refresh without the suffix
ok 690 - M20 PENDING lane folds refresh without the suffix
  ---
  duration_ms: 0.753228
  ...
# Subtest: M11 closed: resting beats age 0
ok 691 - M11 closed: resting beats age 0
  ---
  duration_ms: 0.639481
  ...
# Subtest: M12 unresolved running and M13 unresolved lease over
ok 692 - M12 unresolved running and M13 unresolved lease over
  ---
  duration_ms: 0.515794
  ...
# Subtest: M14 linked today rests with its reason
ok 693 - M14 linked today rests with its reason
  ---
  duration_ms: 0.495445
  ...
# Subtest: M15 other year shows the year and the 282d age
ok 694 - M15 other year shows the year and the 282d age
  ---
  duration_ms: 0.351341
  ...
# Subtest: M16 quoted line keeps foldSpace
ok 695 - M16 quoted line keeps foldSpace
  ---
  duration_ms: 0.624371
  ...
# Subtest: M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
ok 696 - M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
  ---
  duration_ms: 0.90631
  ...
# Subtest: N1-N6 non-canonical lines get no mark
ok 697 - N1-N6 non-canonical lines get no mark
  ---
  duration_ms: 0.568706
  ...
# Subtest: C1-C3 consensus is exact or unresolved
ok 698 - C1-C3 consensus is exact or unresolved
  ---
  duration_ms: 1.439217
  ...
# Subtest: freshnessMarkResolution treats evaluator new as unresolved
ok 699 - freshnessMarkResolution treats evaluator new as unresolved
  ---
  duration_ms: 0.310794
  ...
# Subtest: freshnessMarkSourceInText covers rendered fragments
ok 700 - freshnessMarkSourceInText covers rendered fragments
  ---
  duration_ms: 0.481349
  ...
# Subtest: tone order: closed, then due, then age 0, then out of scope
ok 701 - tone order: closed, then due, then age 0, then out of scope
  ---
  duration_ms: 0.819444
  ...
# Subtest: no tooltip ever contains a double colon
ok 702 - no tooltip ever contains a double colon
  ---
  duration_ms: 1.545741
  ...
# Subtest: freshnessShortDate pins English names and the year rule
ok 703 - freshnessShortDate pins English names and the year rule
  ---
  duration_ms: 0.308619
  ...
# Subtest: DOM builder structure, attributes, and ring geometry
ok 704 - DOM builder structure, attributes, and ring geometry
  ---
  duration_ms: 6.807946
  ...
# Subtest: every mark helper is synchronous and never throws on bad input
ok 705 - every mark helper is synchronous and never throws on bad input
  ---
  duration_ms: 0.366259
  ...
# Subtest: rotten line wording covers 0, 1, and many entries
ok 706 - rotten line wording covers 0, 1, and many entries
  ---
  duration_ms: 0.768056
  ...
# Subtest: rotten line date format includes the year only when it differs
ok 707 - rotten line date format includes the year only when it differs
  ---
  duration_ms: 0.290174
  ...
# Subtest: rotten line truncates the reason to 48 code points without splitting emoji
ok 708 - rotten line truncates the reason to 48 code points without splitting emoji
  ---
  duration_ms: 0.33493
  ...
# Subtest: rotten history rejects ambiguous, invalid, and nested entries
ok 709 - rotten history rejects ambiguous, invalid, and nested entries
  ---
  duration_ms: 2.119656
  ...
# Subtest: rotten marker vectors reject mismatched emoji and missing spaces
ok 710 - rotten marker vectors reject mismatched emoji and missing spaces
  ---
  duration_ms: 0.861594
  ...
# Subtest: rotten line splices before the action line and reaches aria-label
ok 711 - rotten line splices before the action line and reaches aria-label
  ---
  duration_ms: 0.967898
  ...
# Subtest: freshness namespace v12 exposes unblock TICKLER metadata and writers
ok 712 - freshness namespace v12 exposes unblock TICKLER metadata and writers
  ---
  duration_ms: 28.168087
  ...
# Subtest: freshness state and count API expose an unblock return source
ok 713 - freshness state and count API expose an unblock return source
  ---
  duration_ms: 3.532072
  ...
# Subtest: checklist rows report tier and rank while keeping the READY bucket null
ok 714 - checklist rows report tier and rank while keeping the READY bucket null
  ---
  duration_ms: 3.251357
  ...
# Subtest: tier, isDue, and rank cover lane rows
ok 715 - tier, isDue, and rank cover lane rows
  ---
  duration_ms: 4.214825
  ...
# Subtest: memo invalidates on a new tasks array, rollover, and frontmatter
ok 716 - memo invalidates on a new tasks array, rollover, and frontmatter
  ---
  duration_ms: 4.550455
  ...
# Subtest: the reload event fires only when the due key set changes
ok 717 - the reload event fires only when the due key set changes
  ---
  duration_ms: 2.805555
  ...
# Subtest: status bar text covers every state, and a missing host stays quiet
ok 718 - status bar text covers every state, and a missing host stays quiet
  ---
  duration_ms: 2.077525
  ...
# Subtest: status bar clicks through, falling back to rotten
ok 719 - status bar clicks through, falling back to rotten
  ---
  duration_ms: 8.366311
  ...
# Subtest: every freshness api member is synchronous and never throws
ok 720 - every freshness api member is synchronous and never throws
  ---
  duration_ms: 2.772532
  ...
# Subtest: placement vectors P1-P11, P14-P16, P18 stamp canonically
ok 721 - placement vectors P1-P11, P14-P16, P18 stamp canonically
  ---
  duration_ms: 14.51158
  ...
# Subtest: P12 set and clear refresh stamps alongside
ok 722 - P12 set and clear refresh stamps alongside
  ---
  duration_ms: 0.651393
  ...
# Subtest: P13 recurring and P17 done tasks are refused unchanged
ok 723 - P13 recurring and P17 done tasks are refused unchanged
  ---
  duration_ms: 0.343185
  ...
# Subtest: U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
ok 724 - U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
  ---
  duration_ms: 1.512387
  ...
# Subtest: reader reports misplaced and duplicate fields
ok 725 - reader reports misplaced and duplicate fields
  ---
  duration_ms: 0.659248
  ...
# Subtest: Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
ok 726 - Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
  ---
  duration_ms: 7.224028
  ...
# Subtest: Q2 tier order beats path order
ok 727 - Q2 tier order beats path order
  ---
  duration_ms: 1.487369
  ...
# Subtest: L1 lane due and stamped today
ok 728 - L1 lane due and stamped today
  ---
  duration_ms: 0.53964
  ...
# Subtest: L2 lane overrides refresh
ok 729 - L2 lane overrides refresh
  ---
  duration_ms: 0.45536
  ...
# Subtest: L3 lane exclusions have no tier
ok 730 - L3 lane exclusions have no tier
  ---
  duration_ms: 0.918504
  ...
# Subtest: L4 lane off switch and null default
ok 731 - L4 lane off switch and null default
  ---
  duration_ms: 0.341832
  ...
# Subtest: L5 lane order never stamped first
ok 732 - L5 lane order never stamped first
  ---
  duration_ms: 1.196233
  ...
# Subtest: R1 TICKLER beats older ROTTEN
ok 733 - R1 TICKLER beats older ROTTEN
  ---
  duration_ms: 0.505526
  ...
# Subtest: R2 tickler orders by due date then path and line
ok 734 - R2 tickler orders by due date then path and line
  ---
  duration_ms: 0.727459
  ...
# Subtest: missing created sorts after dated peers
ok 735 - missing created sorts after dated peers
  ---
  duration_ms: 0.772955
  ...
# Subtest: B1 upkeep counts outside the lanes
ok 736 - B1 upkeep counts outside the lanes
  ---
  duration_ms: 3.791658
  ...
# Subtest: review model meter uses upkeep and exposes refreshed
ok 737 - review model meter uses upkeep and exposes refreshed
  ---
  duration_ms: 0.729022
  ...
# Subtest: RC1 arrived: past scheduled walks RECURRING with lane and null state
ok 738 - RC1 arrived: past scheduled walks RECURRING with lane and null state
  ---
  duration_ms: 4.166462
  ...
# Subtest: RC2 arrives today: due today with zero days overdue
ok 739 - RC2 arrives today: due today with zero days overdue
  ---
  duration_ms: 0.366911
  ...
# Subtest: RC3 not yet: future scheduled walks nowhere
ok 740 - RC3 not yet: future scheduled walks nowhere
  ---
  duration_ms: 0.253504
  ...
# Subtest: RC4 due only, past: the due date is the occurrence
ok 741 - RC4 due only, past: the due date is the occurrence
  ---
  duration_ms: 0.425433
  ...
# Subtest: RC5 due only, future: walks nowhere
ok 742 - RC5 due only, future: walks nowhere
  ---
  duration_ms: 0.274935
  ...
# Subtest: RC6 earliest date wins across start and due
ok 743 - RC6 earliest date wins across start and due
  ---
  duration_ms: 0.300433
  ...
# Subtest: RC7 undated: no occurrence, no tier
ok 744 - RC7 undated: no occurrence, no tier
  ---
  duration_ms: 0.28278
  ...
# Subtest: RC8 lanes: recurring lane rows keep their lane with null state
ok 745 - RC8 lanes: recurring lane rows keep their lane with null state
  ---
  duration_ms: 0.651304
  ...
# Subtest: RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
ok 746 - RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
  ---
  duration_ms: 2.874216
  ...
# Subtest: RC10 checklist wins: a recurring chore stays in its checklist tier
ok 747 - RC10 checklist wins: a recurring chore stays in its checklist tier
  ---
  duration_ms: 0.406896
  ...
# Subtest: RC11 a stray stamp is ignored: recurring with null state
ok 748 - RC11 a stray stamp is ignored: recurring with null state
  ---
  duration_ms: 0.467142
  ...
# Subtest: RC12 order and counts: due_on, then path, then line; recurring adds no due
ok 749 - RC12 order and counts: due_on, then path, then line; recurring adds no due
  ---
  duration_ms: 1.759318
  ...
# Subtest: recurring rows adapt due and start from Tasks fields and inline fallbacks
ok 750 - recurring rows adapt due and start from Tasks fields and inline fallbacks
  ---
  duration_ms: 1.932568
  ...
# Subtest: status view counts RECURRING as a due commitment tier
ok 751 - status view counts RECURRING as a due commitment tier
  ---
  duration_ms: 0.730294
  ...
# Subtest: footer groups, entry view, and legend cover RECURRING
ok 752 - footer groups, entry view, and legend cover RECURRING
  ---
  duration_ms: 1.247972
  ...
# Subtest: a stale-stamped recurring row marks due with the resolve hint
ok 753 - a stale-stamped recurring row marks due with the resolve hint
  ---
  duration_ms: 1.474304
  ...
# Subtest: freshness namespace v12 keeps recurring and removes reference capabilities
ok 754 - freshness namespace v12 keeps recurring and removes reference capabilities
  ---
  duration_ms: 8.688665
  ...
# Subtest: hidden recurring ^ref keeps ordinary visibility (Rust parity)
ok 755 - hidden recurring ^ref keeps ordinary visibility (Rust parity)
  ---
  duration_ms: 1.483191
  ...
# Subtest: bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
ok 756 - bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
  ---
  duration_ms: 5.367665
  ...
# Subtest: day numbers stay calendar-local across a DST boundary
ok 757 - day numbers stay calendar-local across a DST boundary
  ---
  duration_ms: 0.575919
  ...
# Subtest: reviewModel shares counts, meter, tooltip, and severity
ok 758 - reviewModel shares counts, meter, tooltip, and severity
  ---
  duration_ms: 0.647917
  ...
# Subtest: memo serves warm map hits and misses use the per-row evaluator
ok 759 - memo serves warm map hits and misses use the per-row evaluator
  ---
  duration_ms: 14.122818
  ...
# Subtest: config snapshot caches the parse and invalidates explicitly
ok 760 - config snapshot caches the parse and invalidates explicitly
  ---
  duration_ms: 2.786008
  ...
# Subtest: review chips share the model with severity classes
ok 761 - review chips share the model with severity classes
  ---
  duration_ms: 1.560218
  ...
# Subtest: warm lookups reuse one snapshot without re-reading config
ok 762 - warm lookups reuse one snapshot without re-reading config
  ---
  duration_ms: 2.707779
  ...
# Subtest: same-array cache updates and Today changes rebuild the memo
ok 763 - same-array cache updates and Today changes rebuild the memo
  ---
  duration_ms: 4.289657
  ...
# Subtest: duplicate block IDs keep each row's own classification
ok 764 - duplicate block IDs keep each row's own classification
  ---
  duration_ms: 3.443292
  ...
# Subtest: line identity separates same-path rows without block IDs
ok 765 - line identity separates same-path rows without block IDs
  ---
  duration_ms: 1.923942
  ...
# Subtest: interval lookup serves the cached interval with one memo acquisition
ok 766 - interval lookup serves the cached interval with one memo acquisition
  ---
  duration_ms: 2.244906
  ...
# Subtest: S1 new through S4 overdue
ok 767 - S1 new through S4 overdue
  ---
  duration_ms: 8.269897
  ...
# Subtest: S5 task beats note, S6 note beats config, S7 config
ok 768 - S5 task beats note, S6 note beats config, S7 config
  ---
  duration_ms: 1.17355
  ...
# Subtest: S8 invalid overrides fall through with lints
ok 769 - S8 invalid overrides fall through with lints
  ---
  duration_ms: 0.906931
  ...
# Subtest: S9 malformed and S10 future stamps read as new
ok 770 - S9 malformed and S10 future stamps read as new
  ---
  duration_ms: 0.546263
  ...
# Subtest: S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
ok 771 - S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
  ---
  duration_ms: 0.510865
  ...
# Subtest: S13 out-of-scope rows read null
ok 772 - S13 out-of-scope rows read null
  ---
  duration_ms: 1.146228
  ...
# Subtest: S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
ok 773 - S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
  ---
  duration_ms: 3.491043
  ...
# Subtest: S15 counts (updated): upkeep outside the lanes drives the budget
ok 774 - S15 counts (updated): upkeep outside the lanes drives the budget
  ---
  duration_ms: 2.478071
  ...
# Subtest: config coercion keeps defaults, flags invalid, ignores unknown keys
ok 775 - config coercion keeps defaults, flags invalid, ignores unknown keys
  ---
  duration_ms: 2.610302
  ...
# Subtest: loadFreshnessConfig reads the block with plan-style injectables
ok 776 - loadFreshnessConfig reads the block with plan-style injectables
  ---
  duration_ms: 1.248513
  ...
# Subtest: interval precedence is task, note, config, default
ok 777 - interval precedence is task, note, config, default
  ---
  duration_ms: 0.372872
  ...
# Subtest: intervalForLine covers every source with its Ready fallback
ok 778 - intervalForLine covers every source with its Ready fallback
  ---
  duration_ms: 2.066133
  ...
# Subtest: project tracking stays special while reference tasks use ordinary Ready freshness
ok 779 - project tracking stays special while reference tasks use ordinary Ready freshness
  ---
  duration_ms: 13.443742
  ...
# Subtest: reference tasks match ordinary interval precedence and lane behavior
ok 780 - reference tasks match ordinary interval precedence and lane behavior
  ---
  duration_ms: 5.948665
  ...
# Subtest: obsolete reference interval keys are ignored and project config still validates
ok 781 - obsolete reference interval keys are ignored and project config still validates
  ---
  duration_ms: 1.569496
  ...
# Subtest: references use ordinary keep decisions and the nine-tier queue shape
ok 782 - references use ordinary keep decisions and the nine-tier queue shape
  ---
  duration_ms: 2.391395
  ...
# Subtest: CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
ok 783 - CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
  ---
  duration_ms: 5.49542
  ...
# Subtest: CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
ok 784 - CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
  ---
  duration_ms: 3.265374
  ...
# Subtest: freshness namespace v12 retains the tracker capability contract
ok 785 - freshness namespace v12 retains the tracker capability contract
  ---
  duration_ms: 11.664323
  ...
# Subtest: UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
ok 786 - UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
  ---
  duration_ms: 6.747779
  ...
# Subtest: UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
ok 787 - UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
  ---
  duration_ms: 0.992394
  ...
# Subtest: UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
ok 788 - UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
  ---
  duration_ms: 0.697551
  ...
# Subtest: UB11 scheduled wins a tie with the unblock date
ok 789 - UB11 scheduled wins a tie with the unblock date
  ---
  duration_ms: 0.415924
  ...
# Subtest: unblocked reader takes the latest valid duplicate and reports malformed values
ok 790 - unblocked reader takes the latest valid duplicate and reports malformed values
  ---
  duration_ms: 0.608432
  ...
# Subtest: UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
ok 791 - UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
  ---
  duration_ms: 0.737919
  ...
# Subtest: UB14 TICKLERs with the same due date sort only by path and line
ok 792 - UB14 TICKLERs with the same due date sort only by path and line
  ---
  duration_ms: 3.725331
  ...
# Subtest: UB15 a scheduled ^prj resurfaces in PROJECTS
ok 793 - UB15 a scheduled ^prj resurfaces in PROJECTS
  ---
  duration_ms: 0.495275
  ...
# Subtest: an active-note Pomodoro target still jumps and centers immediately
ok 794 - an active-note Pomodoro target still jumps and centers immediately
  ---
  duration_ms: 21.832062
  ...
# Subtest: Ctrl+9 from an unpinned daily copy switches to the pinned home tab
ok 795 - Ctrl+9 from an unpinned daily copy switches to the pinned home tab
  ---
  duration_ms: 6.456986
  ...
# Subtest: Ctrl+9 on the pinned daily tab jumps in place when a copy exists
ok 796 - Ctrl+9 on the pinned daily tab jumps in place when a copy exists
  ---
  duration_ms: 2.30491
  ...
# Subtest: Ctrl+9 switches daily copies without a Pomodoros section and stays quiet
ok 797 - Ctrl+9 switches daily copies without a Pomodoros section and stays quiet
  ---
  duration_ms: 2.561829
  ...
# Subtest: Ctrl+9 keeps the active daily tab when equal-ranked copies exist
ok 798 - Ctrl+9 keeps the active daily tab when equal-ranked copies exist
  ---
  duration_ms: 2.280703
  ...
# Subtest: Ctrl+9 from a sidebar daily copy switches to a main-area home tab
ok 799 - Ctrl+9 from a sidebar daily copy switches to a main-area home tab
  ---
  duration_ms: 2.427413
  ...
# Subtest: the first fallback press only opens daily and the second press jumps
ok 800 - the first fallback press only opens daily and the second press jumps
  ---
  duration_ms: 2.885839
  ...
# Subtest: a daily note with no target defers its notice until the second press
ok 801 - a daily note with no target defers its notice until the second press
  ---
  duration_ms: 2.212795
  ...
# Subtest: an already-open daily leaf retains its live cursor and viewport
ok 802 - an already-open daily leaf retains its live cursor and viewport
  ---
  duration_ms: 2.252049
  ...
# Subtest: a second press after reused-leaf fallback performs the Pomodoro jump
ok 803 - a second press after reused-leaf fallback performs the Pomodoro jump
  ---
  duration_ms: 2.61422
  ...
# Subtest: the standalone daily-note command activates a reused daily leaf
ok 804 - the standalone daily-note command activates a reused daily leaf
  ---
  duration_ms: 1.850923
  ...
# Subtest: Ctrl+9 loads and reuses a deferred pinned daily tab before falling back
ok 805 - Ctrl+9 loads and reuses a deferred pinned daily tab before falling back
  ---
  duration_ms: 1.969228
  ...
# Subtest: pinned daily tabs win over earlier unpinned tabs
ok 806 - pinned daily tabs win over earlier unpinned tabs
  ---
  duration_ms: 2.019867
  ...
# Subtest: a deferred sidebar daily tab is reused only without a main-area match
ok 807 - a deferred sidebar daily tab is reused only without a main-area match
  ---
  duration_ms: 1.468083
  ...
# Subtest: a deferred sidebar daily tab is reused when there is no main-area match
ok 808 - a deferred sidebar daily tab is reused when there is no main-area match
  ---
  duration_ms: 2.173068
  ...
# Subtest: a deferred non-Markdown daily path is ignored and uses the daily-note fallback
ok 809 - a deferred non-Markdown daily path is ignored and uses the daily-note fallback
  ---
  duration_ms: 5.965276
  ...
# Subtest: the standalone daily-note command reuses a deferred pinned tab
ok 810 - the standalone daily-note command reuses a deferred pinned tab
  ---
  duration_ms: 2.06434
  ...
# Subtest: Ctrl+9 opens the pinned daily tab from a non-Markdown active leaf
ok 811 - Ctrl+9 opens the pinned daily tab from a non-Markdown active leaf
  ---
  duration_ms: 1.538677
  ...
# Subtest: a closed then reopened daily note restores its in-session location
ok 812 - a closed then reopened daily note restores its in-session location
  ---
  duration_ms: 2.253101
  ...
# Subtest: different-path and invalid locations do not leak into a daily note
ok 813 - different-path and invalid locations do not leak into a daily note
  ---
  duration_ms: 1.103006
  ...
# Subtest: out-of-range remembered coordinates are clamped safely
ok 814 - out-of-range remembered coordinates are clamped safely
  ---
  duration_ms: 1.403509
  ...
# Subtest: a rapid second press cancels an older fallback restore
ok 815 - a rapid second press cancels an older fallback restore
  ---
  duration_ms: 5.265911
  ...
# Subtest: navigation and unload clean up daily scroll listeners and deferred work
ok 816 - navigation and unload clean up daily scroll listeners and deferred work
  ---
  duration_ms: 2.053008
  ...
# Subtest: crowded chip: over count is red with tooltip, aria, and names
ok 817 - crowded chip: over count is red with tooltip, aria, and names
  ---
  duration_ms: 2.101853
  ...
# Subtest: crowded chip: calm zero and unavailable dash
ok 818 - crowded chip: calm zero and unavailable dash
  ---
  duration_ms: 0.21983
  ...
# Subtest: crowded chip: names at most five notes
ok 819 - crowded chip: names at most five notes
  ---
  duration_ms: 0.328287
  ...
# Subtest: crowded chip: classes, text, aria, and arrow
ok 820 - crowded chip: classes, text, aria, and arrow
  ---
  duration_ms: 2.46777
  ...
# Subtest: crowded chip: refresh in place keeps the anchor, unload drops it
ok 821 - crowded chip: refresh in place keeps the anchor, unload drops it
  ---
  duration_ms: 1.114477
  ...
# Subtest: anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
ok 822 - anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
  ---
  duration_ms: 0.81214
  ...
# Subtest: ready-notes summary: crowded, calm, and unavailable
ok 823 - ready-notes summary: crowded, calm, and unavailable
  ---
  duration_ms: 0.35663
  ...
# Subtest: ready-notes bar: cap tick and red overflow within 30 cells
ok 824 - ready-notes bar: cap tick and red overflow within 30 cells
  ---
  duration_ms: 0.342053
  ...
# Subtest: ready-notes block: model and render with grid, pills, and footer
ok 825 - ready-notes block: model and render with grid, pills, and footer
  ---
  duration_ms: 2.387497
  ...
# Subtest: ready-notes block: unavailable renders a dash line
ok 826 - ready-notes block: unavailable renders a dash line
  ---
  duration_ms: 0.579667
  ...
# Subtest: heading matcher: fences, level, case, and first-only
ok 827 - heading matcher: fences, level, case, and first-only
  ---
  duration_ms: 0.572252
  ...
# Subtest: heading chip copy: room, full, crowded, exempt, unavailable
ok 828 - heading chip copy: room, full, crowded, exempt, unavailable
  ---
  duration_ms: 0.760112
  ...
# Subtest: heading chip key is stable for equal models
ok 829 - heading chip key is stable for equal models
  ---
  duration_ms: 0.333246
  ...
# Subtest: reading view: appends the chip to the matching h2 only
ok 830 - reading view: appends the chip to the matching h2 only
  ---
  duration_ms: 3.219526
  ...
# Subtest: reading view: no chip for ineligible notes
ok 831 - reading view: no chip for ineligible notes
  ---
  duration_ms: 0.390816
  ...
# Subtest: one live-refresh fan-out reaches every family
ok 832 - one live-refresh fan-out reaches every family
  ---
  duration_ms: 2.780427
  ...
# Subtest: ledger-tools CSS is theme-safe for the new views
ok 833 - ledger-tools CSS is theme-safe for the new views
  ---
  duration_ms: 0.965733
  ...
# Subtest: maxReadyPerNote defaults to 5 and validates 1–999
ok 834 - maxReadyPerNote defaults to 5 and validates 1–999
  ---
  duration_ms: 4.61481
  ...
# Subtest: loadPlanCaps caches on a stat key and detects edits
ok 835 - loadPlanCaps caches on a stat key and detects edits
  ---
  duration_ms: 1.261708
  ...
# Subtest: loadPlanCaps handles deletion, invalid edits, and recovery
ok 836 - loadPlanCaps handles deletion, invalid edits, and recovery
  ---
  duration_ms: 0.834283
  ...
# Subtest: loadPlanCaps without statSync reads through uncached
ok 837 - loadPlanCaps without statSync reads through uncached
  ---
  duration_ms: 0.50262
  ...
# Subtest: noteFrontmatter resolves through getFileCache, not getCache
ok 838 - noteFrontmatter resolves through getFileCache, not getCache
  ---
  duration_ms: 1.222413
  ...
# Subtest: task_refresh applies through the shared reader
ok 839 - task_refresh applies through the shared reader
  ---
  duration_ms: 9.0373
  ...
# Subtest: noteReadyKindFromType covers every R11 form
ok 840 - noteReadyKindFromType covers every R11 form
  ---
  duration_ms: 0.882465
  ...
# Subtest: noteReadyStatusLabel mirrors ProjectStatus::parse
ok 841 - noteReadyStatusLabel mirrors ProjectStatus::parse
  ---
  duration_ms: 0.606207
  ...
# Subtest: noteReadyParentStem strips alias, heading, and path
ok 842 - noteReadyParentStem strips alias, heading, and path
  ---
  duration_ms: 0.822641
  ...
# Subtest: parseNoteReadyCap covers every R8 form
ok 843 - parseNoteReadyCap covers every R8 form
  ---
  duration_ms: 1.254113
  ...
# Subtest: R1: 6 tasks at the default cap are crowded with over_by 1
ok 844 - R1: 6 tasks at the default cap are crowded with over_by 1
  ---
  duration_ms: 13.439252
  ...
# Subtest: R2: 5 tasks are full with no lint
ok 845 - R2: 5 tasks are full with no lint
  ---
  duration_ms: 3.878493
  ...
# Subtest: R3: hidden, future, blocked, and non-TODO rows never count
ok 846 - R3: hidden, future, blocked, and non-TODO rows never count
  ---
  duration_ms: 5.623483
  ...
# Subtest: R4: make-up splits 1 ready + 1 new + 1 rotten
ok 847 - R4: make-up splits 1 ready + 1 new + 1 rotten
  ---
  duration_ms: 3.770627
  ...
# Subtest: R5: recurring rows are excluded but tallied
ok 848 - R5: recurring rows are excluded but tallied
  ---
  duration_ms: 2.756523
  ...
# Subtest: R6: a visible ^prj task never counts
ok 849 - R6: a visible ^prj task never counts
  ---
  duration_ms: 2.043801
  ...
# Subtest: R7: daily, untyped, template, done, and dash rows are absent
ok 850 - R7: daily, untyped, template, done, and dash rows are absent
  ---
  duration_ms: 3.68823
  ...
# Subtest: R8: ready_cap forms map to cap, exempt, or lint-then-default
ok 851 - R8: ready_cap forms map to cap, exempt, or lint-then-default
  ---
  duration_ms: 11.370295
  ...
# Subtest: R9: a parent with two children counts 3
ok 852 - R9: a parent with two children counts 3
  ---
  duration_ms: 3.57827
  ...
# Subtest: R10: terminal projects are not capped and lint once
ok 853 - R10: terminal projects are not capped and lint once
  ---
  duration_ms: 9.409261
  ...
# Subtest: R11: every type form and nested folders are eligible
ok 854 - R11: every type form and nested folders are eligible
  ---
  duration_ms: 3.14884
  ...
# Subtest: R12: stamping a NEW task keeps the count and moves the make-up
ok 855 - R12: stamping a NEW task keeps the count and moves the make-up
  ---
  duration_ms: 3.854797
  ...
# Subtest: R13: a Today-linked task still counts
ok 856 - R13: a Today-linked task still counts
  ---
  duration_ms: 2.108705
  ...
# Subtest: R14: max_ready_per_note 3 caps others while ready_cap 8 holds
ok 857 - R14: max_ready_per_note 3 caps others while ready_cap 8 holds
  ---
  duration_ms: 6.958012
  ...
# Subtest: api.noteReady is frozen at version 1 under api v3
ok 858 - api.noteReady is frozen at version 1 under api v3
  ---
  duration_ms: 1.434999
  ...
# Subtest: counted and inCrowdedNote resolve per task
ok 859 - counted and inCrowdedNote resolve per task
  ---
  duration_ms: 3.704791
  ...
# Subtest: groupLabel ranks crowded notes by excess
ok 860 - groupLabel ranks crowded notes by excess
  ---
  duration_ms: 9.219248
  ...
# Subtest: snapshot sorts crowded, full, room, empty, exempt and splits totals
ok 861 - snapshot sorts crowded, full, room, empty, exempt and splits totals
  ---
  duration_ms: 15.806482
  ...
# Subtest: missing Tasks data and a cold cache are unavailable, never zero
ok 862 - missing Tasks data and a cold cache are unavailable, never zero
  ---
  duration_ms: 2.67174
  ...
# Subtest: throwing Tasks guards never throw
ok 863 - throwing Tasks guards never throw
  ---
  duration_ms: 2.511074
  ...
# Subtest: snapshot reuses the memo without reparsing or re-walking
ok 864 - snapshot reuses the memo without reparsing or re-walking
  ---
  duration_ms: 2.838738
  ...
# Subtest: a task edit rebuilds through the cache-update handler
ok 865 - a task edit rebuilds through the cache-update handler
  ---
  duration_ms: 2.988555
  ...
# Subtest: a ready_cap edit rebuilds and fires the query-refresh trigger
ok 866 - a ready_cap edit rebuilds and fires the query-refresh trigger
  ---
  duration_ms: 2.105699
  ...
# Subtest: rename and delete move the eligibility entry
ok 867 - rename and delete move the eligibility entry
  ---
  duration_ms: 3.656229
  ...
# Subtest: day rollover rebuilds the snapshot date
ok 868 - day rollover rebuilds the snapshot date
  ---
  duration_ms: 2.177637
  ...
# Subtest: a config edit flows through the stat cache
ok 869 - a config edit flows through the stat cache
  ---
  duration_ms: 4.620801
  ...
# Subtest: untyped and non-markdown vault events are no-ops
ok 870 - untyped and non-markdown vault events are no-ops
  ---
  duration_ms: 1.932409
  ...
# Subtest: memo hits never re-walk the vault
ok 871 - memo hits never re-walk the vault
  ---
  duration_ms: 117.9527
  ...
# Subtest: the startup storm is linear
ok 872 - the startup storm is linear
  ---
  duration_ms: 91.487782
  ...
# Subtest: the first resolved event forces one rebuild and later ones do not
ok 873 - the first resolved event forces one rebuild and later ones do not
  ---
  duration_ms: 2.842706
  ...
# Subtest: noteReadyEvaluate is pure and mirrors the Rust totals
ok 874 - noteReadyEvaluate is pure and mirrors the Rust totals
  ---
  duration_ms: 0.585387
  ...
# Subtest: conformance: merged name with duplicate
ok 875 - conformance: merged name with duplicate
  ---
  duration_ms: 9.043382
  ...
# Subtest: conformance: link forms and exclusions
ok 876 - conformance: link forms and exclusions
  ---
  duration_ms: 1.227753
  ...
# Subtest: conformance: unnamed placeholders
ok 877 - conformance: unnamed placeholders
  ---
  duration_ms: 0.516546
  ...
# Subtest: conformance: subheading in the section
ok 878 - conformance: subheading in the section
  ---
  duration_ms: 0.842388
  ...
# Subtest: conformance: open inventory label
ok 879 - conformance: open inventory label
  ---
  duration_ms: 0.628049
  ...
# Subtest: conformance: over the cap
ok 880 - conformance: over the cap
  ---
  duration_ms: 0.874419
  ...
# Subtest: conformance: cancelled and completed entries
ok 881 - conformance: cancelled and completed entries
  ---
  duration_ms: 0.507037
  ...
# Subtest: exactly at the cap is fine
ok 882 - exactly at the cap is fine
  ---
  duration_ms: 0.476188
  ...
# Subtest: no Pomodoros section degrades to an empty budget
ok 883 - no Pomodoros section degrades to an empty budget
  ---
  duration_ms: 0.74863
  ...
# Subtest: fenced code never counts
ok 884 - fenced code never counts
  ---
  duration_ms: 0.644551
  ...
# Subtest: highlight is the first open non-exempt entry; running is the timed one
ok 885 - highlight is the first open non-exempt entry; running is the timed one
  ---
  duration_ms: 0.723431
  ...
# Subtest: coercePlanCaps ignores a legacy max_now instead of failing
ok 886 - coercePlanCaps ignores a legacy max_now instead of failing
  ---
  duration_ms: 0.711178
  ...
# Subtest: parsePlanCaps defaults, overrides, and invalid fallbacks
ok 887 - parsePlanCaps defaults, overrides, and invalid fallbacks
  ---
  duration_ms: 0.760572
  ...
# Subtest: loadPlanCaps falls back to defaults without fs
ok 888 - loadPlanCaps falls back to defaults without fs
  ---
  duration_ms: 1.272729
  ...
# Subtest: loadPlanCaps falls back to defaults on mobile
ok 889 - loadPlanCaps falls back to defaults on mobile
  ---
  duration_ms: 0.426123
  ...
# Subtest: loadPlanCaps reads plan: and flags invalid values
ok 890 - loadPlanCaps reads plan: and flags invalid values
  ---
  duration_ms: 1.275455
  ...
# Subtest: planBlockTargetPath prefers the containing daily note
ok 891 - planBlockTargetPath prefers the containing daily note
  ---
  duration_ms: 1.600976
  ...
# Subtest: planBlockModel degrades to placeholders, never an error
ok 892 - planBlockModel degrades to placeholders, never an error
  ---
  duration_ms: 2.4886
  ...
# Subtest: planBlockModel renders chips, themes, and lints
ok 893 - planBlockModel renders chips, themes, and lints
  ---
  duration_ms: 2.256557
  ...
# Subtest: planBlockModel adds lane cap lints when a lane is over
ok 894 - planBlockModel adds lane cap lints when a lane is over
  ---
  duration_ms: 1.699093
  ...
# Subtest: plugin exposes the versioned api and registers the bob-plan block
ok 895 - plugin exposes the versioned api and registers the bob-plan block
  ---
  duration_ms: 15.001225
  ...
# Subtest: invalid plan block falls back to full defaults
ok 896 - invalid plan block falls back to full defaults
  ---
  duration_ms: 0.894167
  ...
# Subtest: entries require column-0 dash-space with one status char
ok 897 - entries require column-0 dash-space with one status char
  ---
  duration_ms: 0.406376
  ...
# Subtest: crlf line endings split like lf
ok 898 - crlf line endings split like lf
  ---
  duration_ms: 0.503901
  ...
# Subtest: conformance: empty target means the daily note
ok 899 - conformance: empty target means the daily note
  ---
  duration_ms: 0.363274
  ...
# Subtest: lane predicate matches hide subtags, case, and non-task
ok 900 - lane predicate matches hide subtags, case, and non-task
  ---
  duration_ms: 0.507709
  ...
# Subtest: planBlockModel daily badges follow dashboard section counts
ok 901 - planBlockModel daily badges follow dashboard section counts
  ---
  duration_ms: 4.46832
  ...
# Subtest: planBlockModel keeps a supplied unavailable dashboard budget
ok 902 - planBlockModel keeps a supplied unavailable dashboard budget
  ---
  duration_ms: 0.879519
  ...
# Subtest: work tones: TODAY override and unavailable stay neutral in planBlockModel
ok 903 - work tones: TODAY override and unavailable stay neutral in planBlockModel
  ---
  duration_ms: 0.65497
  ...
# Subtest: shared vector: subproject-archive-review
ok 904 - shared vector: subproject-archive-review
  ---
  duration_ms: 10.361589
  ...
# Subtest: shared vector: review-decisions
ok 905 - shared vector: review-decisions
  ---
  duration_ms: 2.732295
  ...
# Subtest: shared vector: resolution-and-lints
ok 906 - shared vector: resolution-and-lints
  ---
  duration_ms: 3.651882
  ...
# Subtest: shared vector: chips, forecast shares, empty forecasts, and session identity
ok 907 - shared vector: chips, forecast shares, empty forecasts, and session identity
  ---
  duration_ms: 2.854759
  ...
# Subtest: shared vector: split-rounding-and-duration
ok 908 - shared vector: split-rounding-and-duration
  ---
  duration_ms: 1.88107
  ...
# Subtest: shared vector: share-rounding
ok 909 - shared vector: share-rounding
  ---
  duration_ms: 0.709143
  ...
# Subtest: shared vector: daily-review-link
ok 910 - shared vector: daily-review-link
  ---
  duration_ms: 0.79106
  ...
# Subtest: shared vector: depth-and-parent-shapes
ok 911 - shared vector: depth-and-parent-shapes
  ---
  duration_ms: 1.654749
  ...
# Subtest: shared vector: unresolved-and-closed-zero
ok 912 - shared vector: unresolved-and-closed-zero
  ---
  duration_ms: 1.439968
  ...
# Subtest: shared vector: parent-scalar-shapes
ok 913 - shared vector: parent-scalar-shapes
  ---
  duration_ms: 0.888807
  ...
# Subtest: dedicated link parser keeps embeds and one struck link, but rejects prose
ok 914 - dedicated link parser keeps embeds and one struck link, but rejects prose
  ---
  duration_ms: 0.365197
  ...
# Subtest: FNV-1a fallback for job maps to the pinned magenta slot
ok 915 - FNV-1a fallback for job maps to the pinned magenta slot
  ---
  duration_ms: 0.237804
  ...
# Subtest: area-color lints are reported once per note
ok 916 - area-color lints are reported once per note
  ---
  duration_ms: 0.816338
  ...
# Subtest: a leftover rollup key neither regroups nor warns
ok 917 - a leftover rollup key neither regroups nor warns
  ---
  duration_ms: 0.69133
  ...
# Subtest: chip DOM exposes forecast, hue, accessible text, and tooltip
ok 918 - chip DOM exposes forecast, hue, accessible text, and tooltip
  ---
  duration_ms: 0.630213
  ...
# Subtest: Reading view appends a forecast chip before its Task Link list
ok 919 - Reading view appends a forecast chip before its Task Link list
  ---
  duration_ms: 8.672766
  ...
# Subtest: Live Preview places a chip widget at the end of the Pomodoro line
ok 920 - Live Preview places a chip widget at the end of the Pomodoro line
  ---
  duration_ms: 1.805576
  ...
# Subtest: Live Preview skips chips in Source mode
ok 921 - Live Preview skips chips in Source mode
  ---
  duration_ms: 0.645322
  ...
# Subtest: Reading view finds embedded Task Links via src
ok 922 - Reading view finds embedded Task Links via src
  ---
  duration_ms: 0.963379
  ...
# Subtest: Obsidian frontmatter shapes unwrap nested wikilink arrays
ok 923 - Obsidian frontmatter shapes unwrap nested wikilink arrays
  ---
  duration_ms: 0.4979
  ...
# Subtest: theme vectors: components split and key like bob
ok 924 - theme vectors: components split and key like bob
  ---
  duration_ms: 3.821015
  ...
# Subtest: theme vectors: hue rule resolves pin, exempt, area, then hash
ok 925 - theme vectors: hue rule resolves pin, exempt, area, then hash
  ---
  duration_ms: 0.64416
  ...
# Subtest: theme vectors: journal fold is last writer wins with rename moves
ok 926 - theme vectors: journal fold is last writer wins with rename moves
  ---
  duration_ms: 1.369023
  ...
# Subtest: theme vectors: history rank is exact, prefix, then substring
ok 927 - theme vectors: history rank is exact, prefix, then substring
  ---
  duration_ms: 0.973639
  ...
# Subtest: theme hash hues match the known collisions
ok 928 - theme hash hues match the known collisions
  ---
  duration_ms: 0.330681
  ...
# Subtest: theme similar keys follow the near-duplicate rule
ok 929 - theme similar keys follow the near-duplicate rule
  ---
  duration_ms: 0.948721
  ...
# Subtest: theme decode accepts a schema 1 report and rejects the rest
ok 930 - theme decode accepts a schema 1 report and rejects the rest
  ---
  duration_ms: 0.888456
  ...
# Subtest: theme write decode maps refusals and pre-writer bob output
ok 931 - theme write decode maps refusals and pre-writer bob output
  ---
  duration_ms: 0.582672
  ...
# Subtest: theme components carry byte offsets excluding quotes and plus
ok 932 - theme components carry byte offsets excluding quotes and plus
  ---
  duration_ms: 0.617338
  ...
# Subtest: theme pill models mark exempt components muted
ok 933 - theme pill models mark exempt components muted
  ---
  duration_ms: 0.6918
  ...
# Subtest: theme name offsets anchor at the em dash of a ledger line
ok 934 - theme name offsets anchor at the em dash of a ledger line
  ---
  duration_ms: 0.976023
  ...
# Subtest: parser accepts the PM1-PM5 conformance vectors verbatim
ok 935 - parser accepts the PM1-PM5 conformance vectors verbatim
  ---
  duration_ms: 3.206121
  ...
# Subtest: parser rejects the PM7-PM12 conformance vectors verbatim
ok 936 - parser rejects the PM7-PM12 conformance vectors verbatim
  ---
  duration_ms: 0.399393
  ...
# Subtest: PM6 with the ladder unknown omits P-labels instead of guessing
ok 937 - PM6 with the ladder unknown omits P-labels instead of guessing
  ---
  duration_ms: 0.42413
  ...
# Subtest: PM13-PM17 ladder and line variants hold
ok 938 - PM13-PM17 ladder and line variants hold
  ---
  duration_ms: 4.923247
  ...
# Subtest: no model output contains a double colon
ok 939 - no model output contains a double colon
  ---
  duration_ms: 2.447522
  ...
# Subtest: element structure and the decorative/inheritColor options
ok 940 - element structure and the decorative/inheritColor options
  ---
  duration_ms: 0.747036
  ...
# Subtest: Live Preview decorations fold space, reveal, and refuse
ok 941 - Live Preview decorations fold space, reveal, and refuse
  ---
  duration_ms: 2.476868
  ...
# Subtest: a line with fresh and priority fields gets a disjoint decoration
ok 942 - a line with fresh and priority fields gets a disjoint decoration
  ---
  duration_ms: 0.394323
  ...
# Subtest: widget mousedown reveals the field at the folded offset
ok 943 - widget mousedown reveals the field at the folded offset
  ---
  duration_ms: 1.026079
  ...
# Subtest: rendered views split task nodes and skip exclusions
ok 944 - rendered views split task nodes and skip exclusions
  ---
  duration_ms: 2.558755
  ...
# Subtest: ladder coercion is lenient: valid, partial, and unknown
ok 945 - ladder coercion is lenient: valid, partial, and unknown
  ---
  duration_ms: 0.688855
  ...
# Subtest: ladder snapshot reads the file and reuses the cache
ok 946 - ladder snapshot reads the file and reuses the cache
  ---
  duration_ms: 5.266111
  ...
# Subtest: ladder snapshot degrades on missing files and parse errors
ok 947 - ladder snapshot degrades on missing files and parse errors
  ---
  duration_ms: 1.694314
  ...
# Subtest: ladder snapshot is unknown on mobile
ok 948 - ladder snapshot is unknown on mobile
  ---
  duration_ms: 64.671658
  ...
# Subtest: api.priorityMarks v1 is additive, sync, and never throwing
ok 949 - api.priorityMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 14.141944
  ...
# Subtest: session toggle and onload wiring
ok 950 - session toggle and onload wiring
  ---
  duration_ms: 2.568043
  ...
# Subtest: styles.css contract: masks, both hosts, repair flag, resting
ok 951 - styles.css contract: masks, both hosts, repair flag, resting
  ---
  duration_ms: 1.402677
  ...
# Subtest: P1/P3/P4: open entries mark plain and aliased links
ok 952 - P1/P3/P4: open entries mark plain and aliased links
  ---
  duration_ms: 5.112228
  ...
# Subtest: P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
ok 953 - P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
  ---
  duration_ms: 4.724598
  ...
# Subtest: P5: closed entries never mark, even with 🍅 history
ok 954 - P5: closed entries never mark, even with 🍅 history
  ---
  duration_ms: 1.83352
  ...
# Subtest: P6/P7: embedded and struck links never mark
ok 955 - P6/P7: embedded and struck links never mark
  ---
  duration_ms: 0.811099
  ...
# Subtest: P8: both trailing-\# move-only forms mark
ok 956 - P8: both trailing-\# move-only forms mark
  ---
  duration_ms: 0.547255
  ...
# Subtest: P9: nested and prose-mixed links never mark
ok 957 - P9: nested and prose-mixed links never mark
  ---
  duration_ms: 0.304111
  ...
# Subtest: P10: fenced, off-section, and off-note links never mark
ok 958 - P10: fenced, off-section, and off-note links never mark
  ---
  duration_ms: 0.682694
  ...
# Subtest: P11: unresolved targets and non-task blocks get no mark
ok 959 - P11: unresolved targets and non-task blocks get no mark
  ---
  duration_ms: 0.810638
  ...
# Subtest: P13: a same-note target reads the live doc
ok 960 - P13: a same-note target reads the live doc
  ---
  duration_ms: 1.325209
  ...
# Subtest: P14: expect() wins until the cache agrees or 4 s pass
ok 961 - P14: expect() wins until the cache agrees or 4 s pass
  ---
  duration_ms: 1.715144
  ...
# Subtest: tooltip, element structure, and eq
ok 962 - tooltip, element structure, and eq
  ---
  duration_ms: 0.635734
  ...
# Subtest: Live Preview places one widget at each In Progress link
ok 963 - Live Preview places one widget at each In Progress link
  ---
  duration_ms: 1.530061
  ...
# Subtest: widget mousedown places the cursor at the link start
ok 964 - widget mousedown places the cursor at the link start
  ---
  duration_ms: 0.842067
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
ok 965 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 1.195442
  ...
# Subtest: Reading view marks In Progress rows and dedupes
ok 966 - Reading view marks In Progress rows and dedupes
  ---
  duration_ms: 2.64039
  ...
# Subtest: Reading view refuses every non-mark row
ok 967 - Reading view refuses every non-mark row
  ---
  duration_ms: 2.42019
  ...
# Subtest: Reading view allows the 🍅 prefix and the trailing \# marker
ok 968 - Reading view allows the 🍅 prefix and the trailing \# marker
  ---
  duration_ms: 0.78049
  ...
# Subtest: api.progressMarks v1 is additive, sync, and never throwing
ok 969 - api.progressMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 2.281375
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 970 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 2.335778
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 971 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 1.235598
  ...
# Subtest: changed-file and rollover refreshes
ok 972 - changed-file and rollover refreshes
  ---
  duration_ms: 1.246729
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 973 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.300323
  ...
# Subtest: styles.css contract: glyph, box, motion, toggle, calm
ok 974 - styles.css contract: glyph, box, motion, toggle, calm
  ---
  duration_ms: 1.096573
  ...
# Subtest: the board registers its code block processor and the Open Reading Board command
ok 975 - the board registers its code block processor and the Open Reading Board command
  ---
  duration_ms: 18.922701
  ...
# Subtest: four lanes render with counts, list and listitem roles, and one hint
ok 976 - four lanes render with counts, list and listitem roles, and one hint
  ---
  duration_ms: 25.212555
  ...
# Subtest: awake cards show kind, topic, added mark, counts, priority, and the pending-sync star
ok 977 - awake cards show kind, topic, added mark, counts, priority, and the pending-sync star
  ---
  duration_ms: 7.313752
  ...
# Subtest: a path-valued Bob audio field produces exactly one visible music marker
ok 978 - a path-valued Bob audio field produces exactly one visible music marker
  ---
  duration_ms: 6.482202
  ...
# Subtest: Snoozed shows Waking, date groups, and Waiting-on rows with their reasons
ok 979 - Snoozed shows Waking, date groups, and Waiting-on rows with their reasons
  ---
  duration_ms: 12.859707
  ...
# Subtest: TODAY pills float linked cards first, and never appear without a ready Today cache
ok 980 - TODAY pills float linked cards first, and never appear without a ready Today cache
  ---
  duration_ms: 13.64729
  ...
# Subtest: the PDF button needs the nav member, macOS, and a source_pdf
ok 981 - the PDF button needs the nav member, macOS, and a source_pdf
  ---
  duration_ms: 19.779776
  ...
# Subtest: click, modifier-click, middle-click, and the Task button route to openLinkText
ok 982 - click, modifier-click, middle-click, and the Task button route to openLinkText
  ---
  duration_ms: 12.140454
  ...
# Subtest: the board is one Tab stop and every key moves or acts
ok 983 - the board is one Tab stop and every key moves or acts
  ---
  duration_ms: 32.31338
  ...
# Subtest: movement targets stay inside the lanes that show cards
ok 984 - movement targets stay inside the lanes that show cards
  ---
  duration_ms: 0.689205
  ...
# Subtest: hovering a Waiting-on row outlines its prerequisite card on the board
ok 985 - hovering a Waiting-on row outlines its prerequisite card on the board
  ---
  duration_ms: 3.654356
  ...
# Subtest: the board never calls a vault write API, in the source or in any gesture
ok 986 - the board never calls a vault write API, in the source or in any gesture
  ---
  duration_ms: 18.951464
  ...
# Subtest: a repaint keeps focus by note path and each lane's scroll position
ok 987 - a repaint keeps focus by note path and each lane's scroll position
  ---
  duration_ms: 8.077189
  ...
# Subtest: a task move and topic/type update repaint handlers while preserving focus and scroll
ok 988 - a task move and topic/type update repaint handlers while preserving focus and scroll
  ---
  duration_ms: 7.817892
  ...
# Subtest: prerequisite identity changes repaint highlighting even when reason text is unchanged
ok 989 - prerequisite identity changes repaint highlighting even when reason text is unchanged
  ---
  duration_ms: 6.430195
  ...
# Subtest: an unchanged board is not repainted; only the data time updates in place
ok 990 - an unchanged board is not repainted; only the data time updates in place
  ---
  duration_ms: 4.966059
  ...
# Subtest: a Today cache change repaints boards from cached data without spawning bob
ok 991 - a Today cache change repaints boards from cached data without spawning bob
  ---
  duration_ms: 14.56366
  ...
# Subtest: first paint is a skeleton in the real grid, then the board without a layout jump
ok 992 - first paint is a skeleton in the real grid, then the board without a layout jump
  ---
  duration_ms: 9.314198
  ...
# Subtest: failures without a frame render an actionable card with Retry
ok 993 - failures without a frame render an actionable card with Retry
  ---
  duration_ms: 29.978354
  ...
# Subtest: a failed manual refresh keeps the last frame and says why with Retry
ok 994 - a failed manual refresh keeps the last frame and says why with Retry
  ---
  duration_ms: 11.428915
  ...
# Subtest: metadata revalidation delivers a silent stale-frame error and recovery updates freshness
ok 995 - metadata revalidation delivers a silent stale-frame error and recovery updates freshness
  ---
  duration_ms: 34.197969
  ...
# Subtest: stale-cache mount refresh failures reach the mounted view
ok 996 - stale-cache mount refresh failures reach the mounted view
  ---
  duration_ms: 11.257898
  ...
# Subtest: unload during a fetch prevents late repaint and queued spawns
ok 997 - unload during a fetch prevents late repaint and queued spawns
  ---
  duration_ms: 7.71105
  ...
# Subtest: in-flight edits and forced refreshes coalesce without dropping mounted fences
ok 998 - in-flight edits and forced refreshes coalesce without dropping mounted fences
  ---
  duration_ms: 19.218514
  ...
# Subtest: manual refresh shows a busy state until the result lands, then announces it
ok 999 - manual refresh shows a busy state until the result lands, then announces it
  ---
  duration_ms: 7.996554
  ...
# Subtest: an older bob without blocked_by falls back to Waiting-on with one lint line
ok 1000 - an older bob without blocked_by falls back to Waiting-on with one lint line
  ---
  duration_ms: 7.991534
  ...
# Subtest: an empty queue shows bob's own phrase instead of lanes
ok 1001 - an empty queue shows bob's own phrase instead of lanes
  ---
  duration_ms: 6.557077
  ...
# Subtest: fence options reach the fetch and bad options show as muted lint lines
ok 1002 - fence options reach the fetch and bad options show as muted lint lines
  ---
  duration_ms: 21.575603
  ...
# Subtest: Snoozed collapses per source path, leaves the key order, and survives repaints
ok 1003 - Snoozed collapses per source path, leaves the key order, and survives repaints
  ---
  duration_ms: 13.324134
  ...
# Subtest: unloading a block releases its view, and teardown clears the session state
ok 1004 - unloading a block releases its view, and teardown clears the session state
  ---
  duration_ms: 3.320087
  ...
# Subtest: reading board stylesheet contract: selectors, layout, tabular-nums, motion, colors
ok 1005 - reading board stylesheet contract: selectors, layout, tabular-nums, motion, colors
  ---
  duration_ms: 1.346621
  ...
# Subtest: Reading Board argv carries bob's fixed queue and optional fence filters
ok 1006 - Reading Board argv carries bob's fixed queue and optional fence filters
  ---
  duration_ms: 4.610811
  ...
# Subtest: Reading Board decoder accepts the shared bob fixture and normalizes optional fields
ok 1007 - Reading Board decoder accepts the shared bob fixture and normalizes optional fields
  ---
  duration_ms: 0.555982
  ...
# Subtest: Reading Board audio presence survives raw JSON decoding and model construction
ok 1008 - Reading Board audio presence survives raw JSON decoding and model construction
  ---
  duration_ms: 11.19536
  ...
# Subtest: Reading Board decoder rejects malformed JSON, shapes, schema, and bob errors
ok 1009 - Reading Board decoder rejects malformed JSON, shapes, schema, and bob errors
  ---
  duration_ms: 0.635293
  ...
# Subtest: shared bob spawn passes the vault environment, timeout, and buffer
ok 1010 - shared bob spawn passes the vault environment, timeout, and buffer
  ---
  duration_ms: 16.621216
  ...
# Subtest: shared bob spawn maps missing binary and timeout failures
ok 1011 - shared bob spawn maps missing binary and timeout failures
  ---
  duration_ms: 5.24859
  ...
# Subtest: Reading Board error cards explain not-found, timeout, schema, and bob errors
ok 1012 - Reading Board error cards explain not-found, timeout, schema, and bob errors
  ---
  duration_ms: 0.953941
  ...
# Subtest: Reading Board cache returns stale data while revalidating and keeps a four-entry LRU
ok 1013 - Reading Board cache returns stale data while revalidating and keeps a four-entry LRU
  ---
  duration_ms: 4.255292
  ...
# Subtest: Reading Board shares identical flights and coalesces one different follow-up
ok 1014 - Reading Board shares identical flights and coalesces one different follow-up
  ---
  duration_ms: 2.848617
  ...
# Subtest: Reading Board refresh is mounted-only, debounced, and reacts to rollover and stale active leaves
ok 1015 - Reading Board refresh is mounted-only, debounced, and reacts to rollover and stale active leaves
  ---
  duration_ms: 1.298088
  ...
# Subtest: the shared bob output builds the expected four lanes and preserves bob order
ok 1016 - the shared bob output builds the expected four lanes and preserves bob order
  ---
  duration_ms: 9.330159
  ...
# Subtest: each status uses its awake lane and every blocked status uses Snoozed
ok 1017 - each status uses its awake lane and every blocked status uses Snoozed
  ---
  duration_ms: 0.956246
  ...
# Subtest: Today floats cards by ledger rank only when the cache is ready
ok 1018 - Today floats cards by ledger rank only when the cache is ready
  ---
  duration_ms: 2.512287
  ...
# Subtest: Snoozed groups show waking, schedule, dependency, project, return lane, and mark models
ok 1019 - Snoozed groups show waking, schedule, dependency, project, return lane, and mark models
  ---
  duration_ms: 1.264594
  ...
# Subtest: schedule groups follow Monday-start weeks through Sunday across month and year ends
ok 1020 - schedule groups follow Monday-start weeks through Sunday across month and year ends
  ---
  duration_ms: 0.449247
  ...
# Subtest: older bob output remains visible in Waiting on and explains the missing reasons
ok 1021 - older bob output remains visible in Waiting on and explains the missing reasons
  ---
  duration_ms: 1.144044
  ...
# Subtest: fence options accept parent and type lists while turning bad input into lints
ok 1022 - fence options accept parent and type lists while turning bad input into lints
  ---
  duration_ms: 2.150625
  ...
# Subtest: kind names, title code spans, and render signatures are deterministic
ok 1023 - kind names, title code spans, and render signatures are deterministic
  ---
  duration_ms: 5.120664
  ...
# Subtest: max_ready defaults to 100 for missing, absent, and null values
ok 1024 - max_ready defaults to 100 for missing, absent, and null values
  ---
  duration_ms: 3.706915
  ...
# Subtest: max_ready accepts a custom positive cap
ok 1025 - max_ready accepts a custom positive cap
  ---
  duration_ms: 0.439128
  ...
# Subtest: max_ready rejects zero, negative, fractions, strings, booleans, and overflow
ok 1026 - max_ready rejects zero, negative, fractions, strings, booleans, and overflow
  ---
  duration_ms: 3.465915
  ...
# Subtest: old configurations and legacy max_now still load
ok 1027 - old configurations and legacy max_now still load
  ---
  duration_ms: 0.357853
  ...
# Subtest: READY boundary: only a strict excess turns red
ok 1028 - READY boundary: only a strict excess turns red
  ---
  duration_ms: 3.611064
  ...
# Subtest: READY custom-cap boundary
ok 1029 - READY custom-cap boundary
  ---
  duration_ms: 0.457744
  ...
# Subtest: READY over is independent of the PLAN ledger status
ok 1030 - READY over is independent of the PLAN ledger status
  ---
  duration_ms: 7.151731
  ...
# Subtest: READY predicate: statuses, custom TODO symbols, and non-tasks
ok 1031 - READY predicate: statuses, custom TODO symbols, and non-tasks
  ---
  duration_ms: 0.339077
  ...
# Subtest: READY predicate: blocked uses the full list, even outside the queue
ok 1032 - READY predicate: blocked uses the full list, even outside the queue
  ---
  duration_ms: 0.525262
  ...
# Subtest: READY predicate: past, today, and future schedules
ok 1033 - READY predicate: past, today, and future schedules
  ---
  duration_ms: 0.387069
  ...
# Subtest: READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
ok 1034 - READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
  ---
  duration_ms: 0.301516
  ...
# Subtest: READY predicate: Today exclusion
ok 1035 - READY predicate: Today exclusion
  ---
  duration_ms: 0.227284
  ...
# Subtest: readyTaskVisible excludes hide variants like Tasks
ok 1036 - readyTaskVisible excludes hide variants like Tasks
  ---
  duration_ms: 0.205332
  ...
# Subtest: daily and dashboard share the READY element contract
ok 1037 - daily and dashboard share the READY element contract
  ---
  duration_ms: 17.931999
  ...
# Subtest: READY placeholder keeps the limit in its tooltip
ok 1038 - READY placeholder keeps the limit in its tooltip
  ---
  duration_ms: 0.355638
  ...
# Subtest: READY keyboard and modifier-key navigation
ok 1039 - READY keyboard and modifier-key navigation
  ---
  duration_ms: 2.838189
  ...
# Subtest: READY unavailable without Tasks, on Cold/Initializing, or before Today
ok 1040 - READY unavailable without Tasks, on Cold/Initializing, or before Today
  ---
  duration_ms: 4.983562
  ...
# Subtest: READY counts a valid empty queue as zero, not unavailable
ok 1041 - READY counts a valid empty queue as zero, not unavailable
  ---
  duration_ms: 2.003374
  ...
# Subtest: READY stays compatible with hosts exposing only getTasks()
ok 1042 - READY stays compatible with hosts exposing only getTasks()
  ---
  duration_ms: 2.062236
  ...
# Subtest: READY degrades to unavailable when the Today predicate throws
ok 1043 - READY degrades to unavailable when the Today predicate throws
  ---
  duration_ms: 0.94288
  ...
# Subtest: READY renders label/value spans for every budget state
ok 1044 - READY renders label/value spans for every budget state
  ---
  duration_ms: 1.504181
  ...
# Subtest: READY live refresh keeps the anchor, spans, and handlers
ok 1045 - READY live refresh keeps the anchor, spans, and handlers
  ---
  duration_ms: 2.039753
  ...
# Subtest: READY refresh crosses the over-cap boundary and back
ok 1046 - READY refresh crosses the over-cap boundary and back
  ---
  duration_ms: 1.493421
  ...
# Subtest: READY refresh crosses the unavailable boundary and back
ok 1047 - READY refresh crosses the unavailable boundary and back
  ---
  duration_ms: 1.157039
  ...
# Subtest: READY never assigns the Obsidian text setter
ok 1048 - READY never assigns the Obsidian text setter
  ---
  duration_ms: 3.655107
  ...
# Subtest: READY gating excludes review buckets and keeps the partition
ok 1049 - READY gating excludes review buckets and keeps the partition
  ---
  duration_ms: 0.867586
  ...
# Subtest: gated READY tooltip carries total lane pressure
ok 1050 - gated READY tooltip carries total lane pressure
  ---
  duration_ms: 0.32997
  ...
# Subtest: planBlockModel gates READY and shares the lane tooltip
ok 1051 - planBlockModel gates READY and shares the lane tooltip
  ---
  duration_ms: 1.082977
  ...
# Subtest: READY lint appears only on a strict excess
ok 1052 - READY lint appears only on a strict excess
  ---
  duration_ms: 10.240758
  ...
# Subtest: READY lint uses a custom cap
ok 1053 - READY lint uses a custom cap
  ---
  duration_ms: 1.287678
  ...
# Subtest: lane lints appear in NEXT, PENDING, READY order
ok 1054 - lane lints appear in NEXT, PENDING, READY order
  ---
  duration_ms: 3.051544
  ...
# Subtest: READY lint uses the gated count
ok 1055 - READY lint uses the gated count
  ---
  duration_ms: 2.764497
  ...
# Subtest: READY lint stays silent while unavailable
ok 1056 - READY lint stays silent while unavailable
  ---
  duration_ms: 1.654589
  ...
# Subtest: READY speaks each host's chip language (daily single-tone, dash two-tone)
ok 1057 - READY speaks each host's chip language (daily single-tone, dash two-tone)
  ---
  duration_ms: 5.610109
  ...
# Subtest: daily paint carries lane pressure to the shared READY renderer
ok 1058 - daily paint carries lane pressure to the shared READY renderer
  ---
  duration_ms: 49.202398
  ...
# Subtest: daily paint degrades to the legacy tooltip without freshness
ok 1059 - daily paint degrades to the legacy tooltip without freshness
  ---
  duration_ms: 4.873062
  ...
# Subtest: work tones: READY model carries the displayed-count tone
ok 1060 - work tones: READY model carries the displayed-count tone
  ---
  duration_ms: 0.257291
  ...
# Subtest: recurrence helpers are exported and frozen where shaped
ok 1061 - recurrence helpers are exported and frozen where shaped
  ---
  duration_ms: 4.42129
  ...
# Subtest: RM1 daily with when done: fold, label, tooltip
ok 1062 - RM1 daily with when done: fold, label, tooltip
  ---
  duration_ms: 2.204087
  ...
# Subtest: RM2 non-checklist row without when done still marks
ok 1063 - RM2 non-checklist row without when done still marks
  ---
  duration_ms: 1.392688
  ...
# Subtest: RM3 weekday plurals keep the full name
ok 1064 - RM3 weekday plurals keep the full name
  ---
  duration_ms: 1.10554
  ...
# Subtest: RM4 monthly ordinals use the written token
ok 1065 - RM4 monthly ordinals use the written token
  ---
  duration_ms: 0.847227
  ...
# Subtest: RM5 every N days stays verbatim with its count
ok 1066 - RM5 every N days stays verbatim with its count
  ---
  duration_ms: 0.254596
  ...
# Subtest: RM6 weekly, N-week, and yearly forms
ok 1067 - RM6 weekly, N-week, and yearly forms
  ---
  duration_ms: 0.585487
  ...
# Subtest: RM7 week lists join with Tue, Fri and weekday alone
ok 1068 - RM7 week lists join with Tue, Fri and weekday alone
  ---
  duration_ms: 0.341391
  ...
# Subtest: RM8 unknown rules stay verbatim
ok 1069 - RM8 unknown rules stay verbatim
  ---
  duration_ms: 1.063751
  ...
# Subtest: RM9 parens and padded brackets are canonical
ok 1070 - RM9 parens and padded brackets are canonical
  ---
  duration_ms: 0.74921
  ...
# Subtest: RM10 case is preserved in the rule and tooltip
ok 1071 - RM10 case is preserved in the rule and tooltip
  ---
  duration_ms: 0.484054
  ...
# Subtest: RM11 cursor in the field reveals it, RM12 closed rows still mark
ok 1072 - RM11 cursor in the field reveals it, RM12 closed rows still mark
  ---
  duration_ms: 0.653908
  ...
# Subtest: RN1 unreadable rules get no mark
ok 1073 - RN1 unreadable rules get no mark
  ---
  duration_ms: 3.522925
  ...
# Subtest: RN2 the checklist guard follows membership, not the glyph slot
ok 1074 - RN2 the checklist guard follows membership, not the glyph slot
  ---
  duration_ms: 0.65012
  ...
# Subtest: RN3 code still parses pure but decorates nothing
ok 1075 - RN3 code still parses pure but decorates nothing
  ---
  duration_ms: 0.777675
  ...
# Subtest: element anatomy: repeat host, rule, quiet tone, no date
ok 1076 - element anatomy: repeat host, rule, quiet tone, no date
  ---
  duration_ms: 1.106212
  ...
# Subtest: family dispatch keeps dates working and sorts adds
ok 1077 - family dispatch keeps dates working and sorts adds
  ---
  duration_ms: 1.31511
  ...
# Subtest: Live Preview decorates repeat and respects the guard and code
ok 1078 - Live Preview decorates repeat and respects the guard and code
  ---
  duration_ms: 3.04923
  ...
# Subtest: RR1 reading view honors the guard, RO2 rollover skips repeat
ok 1079 - RR1 reading view honors the guard, RO2 rollover skips repeat
  ---
  duration_ms: 5.251896
  ...
# Subtest: RA1 api.dateMarks stays dates-only and tooltips never contain ::
ok 1080 - RA1 api.dateMarks stays dates-only and tooltips never contain ::
  ---
  duration_ms: 1.003766
  ...
# Subtest: styles.css contract: repeat glyph, ink, resting, repair flag
ok 1081 - styles.css contract: repeat glyph, ink, resting, repair flag
  ---
  duration_ms: 1.396005
  ...
# Subtest: LC1 one unlabelled open target renders links-to arrow chip
ok 1082 - LC1 one unlabelled open target renders links-to arrow chip
  ---
  duration_ms: 5.734448
  ...
# Subtest: LC2 labelled target carries a pill
ok 1083 - LC2 labelled target carries a pill
  ---
  duration_ms: 0.909666
  ...
# Subtest: LC3 closed and archived targets dim without strike; \#hide mutes
ok 1084 - LC3 closed and archived targets dim without strike; \#hide mutes
  ---
  duration_ms: 2.559345
  ...
# Subtest: LC4 unresolvable target is a dashed missing chip
ok 1085 - LC4 unresolvable target is a dashed missing chip
  ---
  duration_ms: 0.603933
  ...
# Subtest: LC5 LINKED FROM shows the builtin inverse phrase
ok 1086 - LC5 LINKED FROM shows the builtin inverse phrase
  ---
  duration_ms: 2.187746
  ...
# Subtest: LC6 LINKED FROM with an unknown label reads chip, label, this
ok 1087 - LC6 LINKED FROM with an unknown label reads chip, label, this
  ---
  duration_ms: 0.934574
  ...
# Subtest: LC7 live edges missing from the text append in canonical order
ok 1088 - LC7 live edges missing from the text append in canonical order
  ---
  duration_ms: 0.795579
  ...
# Subtest: LC8 stored entries that are no longer live are dashed and uncounted
ok 1089 - LC8 stored entries that are no longer live are dashed and uncounted
  ---
  duration_ms: 1.096092
  ...
# Subtest: LC9 three or more closed chips collapse to ✓×N and expand
ok 1090 - LC9 three or more closed chips collapse to ✓×N and expand
  ---
  duration_ms: 1.978026
  ...
# Subtest: LC10 labelled rows wrap one entry per visual row
ok 1091 - LC10 labelled rows wrap one entry per visual row
  ---
  duration_ms: 0.999679
  ...
# Subtest: LC11 controls need api.relations v1; linked_from_remove calls removeLink(S, T)
ok 1092 - LC11 controls need api.relations v1; linked_from_remove calls removeLink(S, T)
  ---
  duration_ms: 2.708962
  ...
# Subtest: LC12 toggle-dependency-chips covers both relation rows
ok 1093 - LC12 toggle-dependency-chips covers both relation rows
  ---
  duration_ms: 1.221582
  ...
# Subtest: LC13 malformed and not-a-line rows have no model
ok 1094 - LC13 malformed and not-a-line rows have no model
  ---
  duration_ms: 0.593012
  ...
# Subtest: LC14 unsaved editor text refreshes the live model
ok 1095 - LC14 unsaved editor text refreshes the live model
  ---
  duration_ms: 29.949117
  ...
# Subtest: Live Preview decorates relation rows from the index
ok 1096 - Live Preview decorates relation rows from the index
  ---
  duration_ms: 11.042569
  ...
# Subtest: Reading view decorates stored anchors and appends live edges
ok 1097 - Reading view decorates stored anchors and appends live edges
  ---
  duration_ms: 5.072603
  ...
# Subtest: Reading view with api.relations v1 shows ＋ and ×
ok 1098 - Reading view with api.relations v1 shows ＋ and ×
  ---
  duration_ms: 3.018852
  ...
# Subtest: ledger parser agrees with shared LK vectors and parses source task children
ok 1099 - ledger parser agrees with shared LK vectors and parses source task children
  ---
  duration_ms: 8.310103
  ...
# Subtest: relationIndex scans done sources, resolves both directions, and orders label suggestions
ok 1100 - relationIndex scans done sources, resolves both directions, and orders label suggestions
  ---
  duration_ms: 15.929967
  ...
# Subtest: relationIndex applies changed, delete, rename, and unsaved editor overlays
ok 1101 - relationIndex applies changed, delete, rename, and unsaved editor overlays
  ---
  duration_ms: 27.350157
  ...
# Subtest: relationIndex registers after layout-ready and never reads non-markdown during startup replay
ok 1102 - relationIndex registers after layout-ready and never reads non-markdown during startup replay
  ---
  duration_ms: 43.722939
  ...
# Subtest: relationIndex ignores non-markdown live events
ok 1103 - relationIndex ignores non-markdown live events
  ---
  duration_ms: 32.410465
  ...
# Subtest: relationIndex layout-ready after unload registers nothing
ok 1104 - relationIndex layout-ready after unload registers nothing
  ---
  duration_ms: 31.701662
  ...
# Subtest: parseTaskRelationFile indexes every checkbox status as a task
ok 1105 - parseTaskRelationFile indexes every checkbox status as a task
  ---
  duration_ms: 1.213907
  ...
# Subtest: relationIndex incoming and suggestions include Next and Blocked sources
ok 1106 - relationIndex incoming and suggestions include Next and Blocked sources
  ---
  duration_ms: 6.760045
  ...
# Subtest: relation-label JS mirrors match the shared bob-cli vectors
ok 1107 - relation-label JS mirrors match the shared bob-cli vectors
  ---
  duration_ms: 3.873062
  ...
# Subtest: api.relationLabels reads folded preferences and delegates desktop writes to bob
ok 1108 - api.relationLabels reads folded preferences and delegates desktop writes to bob
  ---
  duration_ms: 6.256012
  ...
# Subtest: ledger LK1–LK19 recognises relation shapes and keeps them out of plan links
ok 1109 - ledger LK1–LK19 recognises relation shapes and keeps them out of plan links
  ---
  duration_ms: 6.036382
  ...
# Subtest: parseTrigger parses D[-]<N> dated-entry triggers with offset and span
ok 1110 - parseTrigger parses D[-]<N> dated-entry triggers with offset and span
  ---
  duration_ms: 4.54233
  ...
# Subtest: computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
ok 1111 - computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
  ---
  duration_ms: 0.792633
  ...
# Subtest: expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
ok 1112 - expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
  ---
  duration_ms: 0.812852
  ...
# Subtest: findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
ok 1113 - findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
  ---
  duration_ms: 0.529351
  ...
# Subtest: compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
ok 1114 - compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
  ---
  duration_ms: 0.44021
  ...
# Subtest: parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
ok 1115 - parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
  ---
  duration_ms: 0.227003
  ...
# Subtest: computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
ok 1116 - computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
  ---
  duration_ms: 0.197307
  ...
# Subtest: findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
ok 1117 - findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
  ---
  duration_ms: 0.365488
  ...
# Subtest: findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
ok 1118 - findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
  ---
  duration_ms: 0.304181
  ...
# Subtest: expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
ok 1119 - expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
  ---
  duration_ms: 0.753929
  ...
# Subtest: regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
ok 1120 - regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
  ---
  duration_ms: 0.622328
  ...
# Subtest: expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
ok 1121 - expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
  ---
  duration_ms: 0.635554
  ...
# Subtest: stats fence body sets defaults only and ignores the rest
ok 1122 - stats fence body sets defaults only and ignores the rest
  ---
  duration_ms: 3.919421
  ...
# Subtest: stats tile models cover every unit and every quality
ok 1123 - stats tile models cover every unit and every quality
  ---
  duration_ms: 0.82776
  ...
# Subtest: stats spark bars mark null gaps, zero ticks, and hollow today
ok 1124 - stats spark bars mark null gaps, zero ticks, and hollow today
  ---
  duration_ms: 0.569717
  ...
# Subtest: stats table rows and CSV share the same points
ok 1125 - stats table rows and CSV share the same points
  ---
  duration_ms: 1.206593
  ...
# Subtest: stats overview ids prefer the fence, then config, then report order
ok 1126 - stats overview ids prefer the fence, then config, then report order
  ---
  duration_ms: 1.459676
  ...
# Subtest: stats window label always states today and tracking start
ok 1127 - stats window label always states today and tracking start
  ---
  duration_ms: 1.806518
  ...
# Subtest: stats view state is session-only and per source path
ok 1128 - stats view state is session-only and per source path
  ---
  duration_ms: 10.247822
  ...
# Subtest: stats block renders header, tiles, table, and footer from JSON
ok 1129 - stats block renders header, tiles, table, and footer from JSON
  ---
  duration_ms: 46.417191
  ...
# Subtest: stats block shows an actionable card with Retry when bob fails
ok 1130 - stats block shows an actionable card with Retry when bob fails
  ---
  duration_ms: 44.108765
  ...
# Subtest: stats block registers the processor and the Open Stats command
ok 1131 - stats block registers the processor and the Open Stats command
  ---
  duration_ms: 2.439637
  ...
# Subtest: stats revalidation gates on visibility: hidden views never spawn
ok 1132 - stats revalidation gates on visibility: hidden views never spawn
  ---
  duration_ms: 96.516954
  ...
# Subtest: stats background tabs never spawn until the tab is visible again
ok 1133 - stats background tabs never spawn until the tab is visible again
  ---
  duration_ms: 75.38197
  ...
# Subtest: stats cache subscriber repaints only shown views reading the key
ok 1134 - stats cache subscriber repaints only shown views reading the key
  ---
  duration_ms: 23.571362
  ...
# Subtest: stats local-date rollover bumps the change generation once per day
ok 1135 - stats local-date rollover bumps the change generation once per day
  ---
  duration_ms: 2.38867
  ...
# Subtest: stats stylesheet contract: selectors, tabular-nums, motion, colors
ok 1136 - stats stylesheet contract: selectors, tabular-nums, motion, colors
  ---
  duration_ms: 2.61407
  ...
# Subtest: Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
ok 1137 - Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
  ---
  duration_ms: 4.533243
  ...
# Subtest: prior buckets align by elapsed position and omit invalid and provisional points
ok 1138 - prior buckets align by elapsed position and omit invalid and provisional points
  ---
  duration_ms: 1.162268
  ...
# Subtest: chart renders SVG safely and keeps secondary focus metrics selectable
ok 1139 - chart renders SVG safely and keeps secondary focus metrics selectable
  ---
  duration_ms: 17.657455
  ...
# Subtest: grouped chart pins honest buckets, bounds daily detail, and opens validated notes
ok 1140 - grouped chart pins honest buckets, bounds daily detail, and opens validated notes
  ---
  duration_ms: 10.291505
  ...
# Subtest: local focus, table, pin, and definition changes reuse the retained report
ok 1141 - local focus, table, pin, and definition changes reuse the retained report
  ---
  duration_ms: 11.084768
  ...
# Subtest: keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
ok 1142 - keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
  ---
  duration_ms: 39.247467
  ...
# Subtest: schema-1 fallback keeps day quartiles and never invents grouped daily history
ok 1143 - schema-1 fallback keeps day quartiles and never invents grouped daily history
  ---
  duration_ms: 4.482075
  ...
# Subtest: ResizeObserver redraws cached data and disconnects across rerenders and unload
ok 1144 - ResizeObserver redraws cached data and disconnects across rerenders and unload
  ---
  duration_ms: 135.442415
  ...
# Subtest: stats resolution prefers stats.bob_path, then candidates, then PATH
ok 1145 - stats resolution prefers stats.bob_path, then candidates, then PATH
  ---
  duration_ms: 4.208223
  ...
# Subtest: stats home expansion and range/offset normalization
ok 1146 - stats home expansion and range/offset normalization
  ---
  duration_ms: 0.631035
  ...
# Subtest: stats fetch always runs show -a -f json plus the chosen flags
ok 1147 - stats fetch always runs show -a -f json plus the chosen flags
  ---
  duration_ms: 0.639241
  ...
# Subtest: stats group emits -g before metric ids and rejects the rest
ok 1148 - stats group emits -g before metric ids and rejects the rest
  ---
  duration_ms: 0.463655
  ...
# Subtest: stats request resolves one shared key for the page and strip defaults
ok 1149 - stats request resolves one shared key for the page and strip defaults
  ---
  duration_ms: 1.706337
  ...
# Subtest: stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
ok 1150 - stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
  ---
  duration_ms: 14.565974
  ...
# Subtest: stats spawn maps ENOENT, timeouts, and stderr to named errors
ok 1151 - stats spawn maps ENOENT, timeouts, and stderr to named errors
  ---
  duration_ms: 4.354071
  ...
# Subtest: stats decode accepts schema 1 and rejects the rest defensively
ok 1152 - stats decode accepts schema 1 and rejects the rest defensively
  ---
  duration_ms: 0.443046
  ...
# Subtest: stats error cards name the cause and the stats.bob_path fix
ok 1153 - stats error cards name the cause and the stats.bob_path fix
  ---
  duration_ms: 0.795388
  ...
# Subtest: stats fetch shares one flight per key and queues distinct keys FIFO
ok 1154 - stats fetch shares one flight per key and queues distinct keys FIFO
  ---
  duration_ms: 25.891162
  ...
# Subtest: stats fetch never loses waiters: A in flight, B then C settle with own reports
ok 1155 - stats fetch never loses waiters: A in flight, B then C settle with own reports
  ---
  duration_ms: 2.715593
  ...
# Subtest: stats queue caps at 8 distinct pending keys with explicit cancellation
ok 1156 - stats queue caps at 8 distinct pending keys with explicit cancellation
  ---
  duration_ms: 5.592616
  ...
# Subtest: stats cache is a 16-entry LRU keyed by the argument list
ok 1157 - stats cache is a 16-entry LRU keyed by the argument list
  ---
  duration_ms: 5.659603
  ...
# Subtest: stats warm remount with a clean fresh entry spawns nothing
ok 1158 - stats warm remount with a clean fresh entry spawns nothing
  ---
  duration_ms: 2.629189
  ...
# Subtest: stats change bump makes the next hit spawn exactly once
ok 1159 - stats change bump makes the next hit spawn exactly once
  ---
  duration_ms: 2.105088
  ...
# Subtest: stats change during a flight leaves the stored entry dirty
ok 1160 - stats change during a flight leaves the stored entry dirty
  ---
  duration_ms: 2.780869
  ...
# Subtest: stats entries older than the max clean age read dirty
ok 1161 - stats entries older than the max clean age read dirty
  ---
  duration_ms: 1.674116
  ...
# Subtest: stats revalidate never skips a miss but skips dirty hits
ok 1162 - stats revalidate never skips a miss but skips dirty hits
  ---
  duration_ms: 1.700776
  ...
# Subtest: stats peek reads synchronously and listeners fire per store
ok 1163 - stats peek reads synchronously and listeners fire per store
  ---
  duration_ms: 2.955561
  ...
# Subtest: stats unload settles every waiter with cancellation
ok 1164 - stats unload settles every waiter with cancellation
  ---
  duration_ms: 2.144714
  ...
# Subtest: stats spawn counters record each spawn
ok 1165 - stats spawn counters record each spawn
  ---
  duration_ms: 1.988475
  ...
# Subtest: stats block views count as shown without a visibility host
ok 1166 - stats block views count as shown without a visibility host
  ---
  duration_ms: 0.346792
  ...
# Subtest: stats api v2 keeps append and adds fetch plus bobPath
ok 1167 - stats api v2 keeps append and adds fetch plus bobPath
  ---
  duration_ms: 2.121329
  ...
# Subtest: statsHomeDir defaults to the real home and strips a trailing slash
ok 1168 - statsHomeDir defaults to the real home and strips a trailing slash
  ---
  duration_ms: 0.266739
  ...
# Subtest: stats mac regression: un-injected resolution probes the real home first
ok 1169 - stats mac regression: un-injected resolution probes the real home first
  ---
  duration_ms: 0.35623
  ...
# Subtest: stats absolute candidates are probed verbatim with no doubled slashes
ok 1170 - stats absolute candidates are probed verbatim with no doubled slashes
  ---
  duration_ms: 0.317867
  ...
# Subtest: stats with no home probes only absolute candidates
ok 1171 - stats with no home probes only absolute candidates
  ---
  duration_ms: 0.320291
  ...
# Subtest: stats tilde config expands against the real home
ok 1172 - stats tilde config expands against the real home
  ---
  duration_ms: 0.206284
  ...
# Subtest: stats candidate and tried lists share one source of truth
ok 1173 - stats candidate and tried lists share one source of truth
  ---
  duration_ms: 0.25142
  ...
# Subtest: stats spawn bob-not-found tried list uses the real home
ok 1174 - stats spawn bob-not-found tried list uses the real home
  ---
  duration_ms: 2.935734
  ...
# Subtest: stats unload clears views, timers, cache, flights, and queues
ok 1175 - stats unload clears views, timers, cache, flights, and queues
  ---
  duration_ms: 1.662974
  ...
# Subtest: stats queue outcomes carry fetchedAt
ok 1176 - stats queue outcomes carry fetchedAt
  ---
  duration_ms: 2.251548
  ...
# Subtest: stats namespace v1 serializes versioned review answer JSONL
ok 1177 - stats namespace v1 serializes versioned review answer JSONL
  ---
  duration_ms: 18.58167
  ...
# Subtest: stats journal rejects invalid calendar days and outcomes
ok 1178 - stats journal rejects invalid calendar days and outcomes
  ---
  duration_ms: 2.960631
  ...
# Subtest: statsReviewHost lowercases, cuts at the first dot, and never throws
ok 1179 - statsReviewHost lowercases, cuts at the first dot, and never throws
  ---
  duration_ms: 0.315803
  ...
# Subtest: stats journal plugin passthrough keeps a semver writer and falls back otherwise
ok 1180 - stats journal plugin passthrough keeps a semver writer and falls back otherwise
  ---
  duration_ms: 2.156987
  ...
# Subtest: panel dispatch covers every family, custom kinds, and the net exception
ok 1181 - panel dispatch covers every family, custom kinds, and the net exception
  ---
  duration_ms: 2.033662
  ...
# Subtest: pomodoro panel shows the supplied total, shares, hue, and safe text
ok 1182 - pomodoro panel shows the supplied total, shares, hue, and safe text
  ---
  duration_ms: 21.662039
  ...
# Subtest: home parts use the report catalog for labels, hue slots, and pinned values
ok 1183 - home parts use the report catalog for labels, hue slots, and pinned values
  ---
  duration_ms: 14.475721
  ...
# Subtest: roots panel toggles Themes, pins spans, discloses sub-projects, and opens home links
ok 1184 - roots panel toggles Themes, pins spans, discloses sub-projects, and opens home links
  ---
  duration_ms: 28.969848
  ...
# Subtest: a stale areas view maps to Root parents, and old bob falls back with copy
ok 1185 - a stale areas view maps to Root parents, and old bob falls back with copy
  ---
  duration_ms: 12.063567
  ...
# Subtest: chart pin refreshes Where the time went and Themes honor the pinned span
ok 1186 - chart pin refreshes Where the time went and Themes honor the pinned span
  ---
  duration_ms: 12.941832
  ...
# Subtest: review rows keep their area hue and a missing homes report keeps the saved view
ok 1187 - review rows keep their area hue and a missing homes report keeps the saved view
  ---
  duration_ms: 6.491422
  ...
# Subtest: task home table uses catalog labels and keeps hue dots and mini-bars
ok 1188 - task home table uses catalog labels and keeps hue dots and mini-bars
  ---
  duration_ms: 19.306632
  ...
# Subtest: task flow stacks signed values, keeps missing constituents missing, and labels series
ok 1189 - task flow stacks signed values, keeps missing constituents missing, and labels series
  ---
  duration_ms: 6.740737
  ...
# Subtest: absent companions are named, custom filters are labeled overall, and net splits breakdowns
ok 1190 - absent companions are named, custom filters are labeled overall, and net splits breakdowns
  ---
  duration_ms: 8.05269
  ...
# Subtest: journal panels pair answers with review time and a gapped keep chart under 90%
ok 1191 - journal panels pair answers with review time and a gapped keep chart under 90%
  ---
  duration_ms: 9.145057
  ...
# Subtest: checklist calendar aligns Monday weeks with states, reasons, and provisional today
ok 1192 - checklist calendar aligns Monday weeks with states, reasons, and provisional today
  ---
  duration_ms: 19.32113
  ...
# Subtest: grouped calendars reuse daily points and old schemas fall back with a label
ok 1193 - grouped calendars reuse daily points and old schemas fall back with a label
  ---
  duration_ms: 8.810648
  ...
# Subtest: ISO year boundaries stay in one Monday week and chore dots expose text
ok 1194 - ISO year boundaries stay in one Monday week and chore dots expose text
  ---
  duration_ms: 4.603927
  ...
# Subtest: panel day selection pins the shared day and never fetches
ok 1195 - panel day selection pins the shared day and never fetches
  ---
  duration_ms: 7.064294
  ...
# Subtest: field and formula metrics keep only the focus chart and table
ok 1196 - field and formula metrics keep only the focus chart and table
  ---
  duration_ms: 2.443965
  ...
# Subtest: statsPanelDistinctHues gives every root its own colour
ok 1197 - statsPanelDistinctHues gives every root its own colour
  ---
  duration_ms: 0.429951
  ...
# Subtest: statsPanelDistinctHues does not depend on input order
ok 1198 - statsPanelDistinctHues does not depend on input order
  ---
  duration_ms: 0.533368
  ...
# Subtest: statsPanelDistinctHues keeps different area hues and greys buckets
ok 1199 - statsPanelDistinctHues keeps different area hues and greys buckets
  ---
  duration_ms: 0.307317
  ...
# Subtest: statsPanelDistinctHues never throws past eight coloured roots
ok 1200 - statsPanelDistinctHues never throws past eight coloured roots
  ---
  duration_ms: 0.505335
  ...
# Subtest: root bar gives same-area roots distinct hues and GTD review stays coloured
ok 1201 - root bar gives same-area roots distinct hues and GTD review stays coloured
  ---
  duration_ms: 3.811165
  ...
# Subtest: root rows and their sub-project leaves share the mapped hue
ok 1202 - root rows and their sub-project leaves share the mapped hue
  ---
  duration_ms: 5.588648
  ...
# Subtest: TT vectors verbatim: task-line gate plus boundary tokens
ok 1203 - TT vectors verbatim: task-line gate plus boundary tokens
  ---
  duration_ms: 5.627942
  ...
# Subtest: TT13-TT14 cursor reveal is inclusive
ok 1204 - TT13-TT14 cursor reveal is inclusive
  ---
  duration_ms: 1.45109
  ...
# Subtest: TT16 coexistence: task tag range is disjoint from priority and date marks
ok 1205 - TT16 coexistence: task tag range is disjoint from priority and date marks
  ---
  duration_ms: 1.585897
  ...
# Subtest: tooltip is exact and never contains a double colon
ok 1206 - tooltip is exact and never contains a double colon
  ---
  duration_ms: 0.211975
  ...
# Subtest: element structure: empty widget span with tooltip attributes
ok 1207 - element structure: empty widget span with tooltip attributes
  ---
  duration_ms: 0.423058
  ...
# Subtest: Live Preview decorations cover exactly the tag and respect reveal and code
ok 1208 - Live Preview decorations cover exactly the tag and respect reveal and code
  ---
  duration_ms: 1.180062
  ...
# Subtest: widget mousedown reveals the tag start
ok 1209 - widget mousedown reveals the tag start
  ---
  duration_ms: 0.914245
  ...
# Subtest: TR vectors verbatim: rendered views annotate eligible anchors in place
ok 1210 - TR vectors verbatim: rendered views annotate eligible anchors in place
  ---
  duration_ms: 2.610424
  ...
# Subtest: TR9 toggle strips document-wide and re-annotates on enable
ok 1211 - TR9 toggle strips document-wide and re-annotates on enable
  ---
  duration_ms: 1.378702
  ...
# Subtest: annotate and strip helpers are idempotent and defensive
ok 1212 - annotate and strip helpers are idempotent and defensive
  ---
  duration_ms: 0.428719
  ...
# Subtest: session toggle and onload wiring
ok 1213 - session toggle and onload wiring
  ---
  duration_ms: 9.085361
  ...
# Subtest: styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
ok 1214 - styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
  ---
  duration_ms: 1.234877
  ...
# Subtest: TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
ok 1215 - TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
  ---
  duration_ms: 1.007172
  ...
# Subtest: Live Preview ref decorations replace the whole pair and reveal both tags at once
ok 1216 - Live Preview ref decorations replace the whole pair and reveal both tags at once
  ---
  duration_ms: 0.697943
  ...
# Subtest: ref element structure: book classes, reference label, and tooltip
ok 1217 - ref element structure: book classes, reference label, and tooltip
  ---
  duration_ms: 0.318879
  ...
# Subtest: TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
ok 1218 - TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
  ---
  duration_ms: 0.992444
  ...
# Subtest: TR11 verbatim: \#task \#references and reversed order keep the hash only
ok 1219 - TR11 verbatim: \#task \#references and reversed order keep the hash only
  ---
  duration_ms: 0.442365
  ...
# Subtest: TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
ok 1220 - TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
  ---
  duration_ms: 0.449257
  ...
# Subtest: TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
ok 1221 - TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
  ---
  duration_ms: 0.915919
  ...
# Subtest: styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
ok 1222 - styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
  ---
  duration_ms: 1.135827
  ...
# Subtest: CK vectors: canonical PRE/POST checklist runs share membership semantics
ok 1223 - CK vectors: canonical PRE/POST checklist runs share membership semantics
  ---
  duration_ms: 1.097154
  ...
# Subtest: CK live preview and widget vectors: one stable glyph replaces the full run
ok 1224 - CK live preview and widget vectors: one stable glyph replaces the full run
  ---
  duration_ms: 0.593503
  ...
# Subtest: CR vectors: rendered checklist anchors annotate in place, conflict stays native
ok 1225 - CR vectors: rendered checklist anchors annotate in place, conflict stays native
  ---
  duration_ms: 1.376126
  ...
# Subtest: CR3 toggle restores all checklist pills and re-annotates them
ok 1226 - CR3 toggle restores all checklist pills and re-annotates them
  ---
  duration_ms: 0.415694
  ...
# Subtest: CR4 Today reading-view anchor follows the second checklist tag
ok 1227 - CR4 Today reading-view anchor follows the second checklist tag
  ---
  duration_ms: 0.500515
  ...
# Subtest: checklist task mark CSS contract covers glyphs, conflict gates, Tasks rows, and resting
ok 1228 - checklist task mark CSS contract covers glyphs, conflict gates, Tasks rows, and resting
  ---
  duration_ms: 0.939202
  ...
# Subtest: section info null stays neutral (TM19)
ok 1229 - section info null stays neutral (TM19)
  ---
  duration_ms: 4.4476
  ...
# Subtest: data-line mapping stamps and marks an exact Today row
ok 1230 - data-line mapping stamps and marks an exact Today row
  ---
  duration_ms: 7.752418
  ...
# Subtest: data-line mapping rejects a status mismatch
ok 1231 - data-line mapping rejects a status mismatch
  ---
  duration_ms: 0.881662
  ...
# Subtest: row-index fallback maps when counts agree and refuses when they disagree
ok 1232 - row-index fallback maps when counts agree and refuses when they disagree
  ---
  duration_ms: 2.669916
  ...
# Subtest: Tasks result rows and code are skipped
ok 1233 - Tasks result rows and code are skipped
  ---
  duration_ms: 0.752927
  ...
# Subtest: a daily-note sourcePath is skipped
ok 1234 - a daily-note sourcePath is skipped
  ---
  duration_ms: 0.358664
  ...
# Subtest: duplicate ids stay neutral
ok 1235 - duplicate ids stay neutral
  ---
  duration_ms: 0.997053
  ...
# Subtest: insertion points: \#task anchor, \#ref pair, checkbox, whitespace split
ok 1236 - insertion points: \#task anchor, \#ref pair, checkbox, whitespace split
  ---
  duration_ms: 2.847716
  ...
# Subtest: identity-proven non-Today rows are stamped without a mark
ok 1237 - identity-proven non-Today rows are stamped without a mark
  ---
  duration_ms: 1.00077
  ...
# Subtest: sweep adds on link, removes on unlink or completion, updates tooltip, respects toggle, skips daily ancestors
ok 1238 - sweep adds on link, removes on unlink or completion, updates tooltip, respects toggle, skips daily ancestors
  ---
  duration_ms: 2.846203
  ...
# Subtest: daily-view class is set on open daily leaves and cleared on switch
ok 1239 - daily-view class is set on open daily leaves and cleared on switch
  ---
  duration_ms: 0.635463
  ...
# Subtest: delegated Mod+click jumps; plain click does not
ok 1240 - delegated Mod+click jumps; plain click does not
  ---
  duration_ms: 3.212151
  ...
# Subtest: setupTodayMarks registers the reading post-processor at order 60
ok 1241 - setupTodayMarks registers the reading post-processor at order 60
  ---
  duration_ms: 0.747767
  ...
# Subtest: styles.css daily-view suppression is present
ok 1242 - styles.css daily-view suppression is present
  ---
  duration_ms: 1.338976
  ...
# Subtest: Live Preview marks do not double-jump in Reading view
ok 1243 - Live Preview marks do not double-jump in Reading view
  ---
  duration_ms: 1.153953
  ...
# Subtest: mid-body \#task goes at the body start
ok 1244 - mid-body \#task goes at the body start
  ---
  duration_ms: 1.374524
  ...
# Subtest: \#task inside inline code stays neutral
ok 1245 - \#task inside inline code stays neutral
  ---
  duration_ms: 0.591218
  ...
# Subtest: re-render with a new path refreshes the mark key
ok 1246 - re-render with a new path refreshes the mark key
  ---
  duration_ms: 0.989378
  ...
# Subtest: one duplicate scan per render
ok 1247 - one duplicate scan per render
  ---
  duration_ms: 1.303568
  ...
# Subtest: row-index fallback uses every list item
ok 1248 - row-index fallback uses every list item
  ---
  duration_ms: 1.22078
  ...
# Subtest: open statuses are exactly space, star, slash, and question
ok 1249 - open statuses are exactly space, star, slash, and question
  ---
  duration_ms: 4.038849
  ...
# Subtest: trailing-id rules: leading space, trailing-only, valid charset
ok 1250 - trailing-id rules: leading space, trailing-only, valid charset
  ---
  duration_ms: 4.275122
  ...
# Subtest: candidate: TM9 closed stays null, TM10 open statuses pass
ok 1251 - candidate: TM9 closed stays null, TM10 open statuses pass
  ---
  duration_ms: 4.393376
  ...
# Subtest: candidate: TM11 needs an exact \#task tag and a trailing id
ok 1252 - candidate: TM11 needs an exact \#task tag and a trailing id
  ---
  duration_ms: 0.479726
  ...
# Subtest: candidate: TM21 code is left for the call-site code check
ok 1253 - candidate: TM21 code is left for the call-site code check
  ---
  duration_ms: 0.936487
  ...
# Subtest: insert offset: \#task first lands before the title
ok 1254 - insert offset: \#task first lands before the title
  ---
  duration_ms: 0.273272
  ...
# Subtest: insert offset: TM16 \#task \#ref spans the pair, \#prj sits between
ok 1255 - insert offset: TM16 \#task \#ref spans the pair, \#prj sits between
  ---
  duration_ms: 0.540351
  ...
# Subtest: insert offset: mid-body \#task falls back to the body start
ok 1256 - insert offset: mid-body \#task falls back to the body start
  ---
  duration_ms: 0.386718
  ...
# Subtest: insert offset: blockquote, spaces, numbered, empty title, emoji
ok 1257 - insert offset: blockquote, spaces, numbered, empty title, emoji
  ---
  duration_ms: 1.149314
  ...
# Subtest: duplicates: TM15 marks neither line
ok 1258 - duplicates: TM15 marks neither line
  ---
  duration_ms: 0.567654
  ...
# Subtest: session text: named, home label, range-only, unnamed
ok 1259 - session text: named, home label, range-only, unnamed
  ---
  duration_ms: 0.479164
  ...
# Subtest: tooltip: TM1 running, TM2 queued, and the platform variants
ok 1260 - tooltip: TM1 running, TM2 queued, and the platform variants
  ---
  duration_ms: 0.462974
  ...
# Subtest: tooltip: running wins as primary with a +N more suffix
ok 1261 - tooltip: running wins as primary with a +N more suffix
  ---
  duration_ms: 0.397879
  ...
# Subtest: tooltip: empty input yields Today and output never has ::
ok 1262 - tooltip: empty input yields Today and output never has ::
  ---
  duration_ms: 0.459026
  ...
# Subtest: entering window: 600 ms after join, never before or at load
ok 1263 - entering window: 600 ms after join, never before or at load
  ---
  duration_ms: 0.28298
  ...
# Subtest: modifier: primary button with meta on mac, ctrl elsewhere
ok 1264 - modifier: primary button with meta on mac, ctrl elsewhere
  ---
  duration_ms: 0.388301
  ...
# Subtest: element: empty span with tooltip attributes and no listeners
ok 1265 - element: empty span with tooltip attributes and no listeners
  ---
  duration_ms: 0.65967
  ...
# Subtest: widget: eq ignores entering and the callback
ok 1266 - widget: eq ignores entering and the callback
  ---
  duration_ms: 0.949593
  ...
# Subtest: widget: plain mousedown moves the cursor, Mod mousedown jumps
ok 1267 - widget: plain mousedown moves the cursor, Mod mousedown jumps
  ---
  duration_ms: 1.106653
  ...
# Subtest: refresh effect is lazy and stable
ok 1268 - refresh effect is lazy and stable
  ---
  duration_ms: 0.495416
  ...
# Subtest: styles.css implements the glyph anatomy contract
ok 1269 - styles.css implements the glyph anatomy contract
  ---
  duration_ms: 1.319007
  ...
# Subtest: Live Preview applies the TM1-TM22 line, cache, and refresh vectors
ok 1270 - Live Preview applies the TM1-TM22 line, cache, and refresh vectors
  ---
  duration_ms: 82.198321
  ...
# Subtest: Today mark lifecycle registers the toggle, keyboard command, and reading processor
ok 1271 - Today mark lifecycle registers the toggle, keyboard command, and reading processor
  ---
  duration_ms: 72.891165
  ...
# Subtest: keyboard jump uses the task under the cursor and reports non-membership
ok 1272 - keyboard jump uses the task under the cursor and reports non-membership
  ---
  duration_ms: 86.335358
  ...
# Subtest: Mod-click and keyboard jumps land on the current running Task Link
ok 1273 - Mod-click and keyboard jumps land on the current running Task Link
  ---
  duration_ms: 145.554917
  ...
# Subtest: reduced motion stops the entrance pop
ok 1274 - reduced motion stops the entrance pop
  ---
  duration_ms: 1.039113
  ...
# Subtest: tooltips never contain ::
ok 1275 - tooltips never contain ::
  ---
  duration_ms: 0.412818
  ...
# Subtest: todayMarkPosInInlineCode: single, double, unmatched, positions
ok 1276 - todayMarkPosInInlineCode: single, double, unmatched, positions
  ---
  duration_ms: 0.648368
  ...
# Subtest: builder gates on Today ids without touching doc lines
ok 1277 - builder gates on Today ids without touching doc lines
  ---
  duration_ms: 67.148533
  ...
# Subtest: two rebuilds on the same doc compute duplicates once
ok 1278 - two rebuilds on the same doc compute duplicates once
  ---
  duration_ms: 66.072972
  ...
# Subtest: todayMarksNow override drives readiness
ok 1279 - todayMarksNow override drives readiness
  ---
  duration_ms: 62.109335
  ...
# Subtest: refresh dispatches only to non-daily leaves and uses 16 ms
ok 1280 - refresh dispatches only to non-daily leaves and uses 16 ms
  ---
  duration_ms: 48.979773
  ...
# Subtest: keyboard command gates closed status and daily notes
ok 1281 - keyboard command gates closed status and daily notes
  ---
  duration_ms: 62.954949
  ...
# Subtest: TM14 rollover: day N+1 shows no decoration
ok 1282 - TM14 rollover: day N+1 shows no decoration
  ---
  duration_ms: 73.596172
  ...
# Subtest: TM17 widget sits at line.from + insertCh with side -1
ok 1283 - TM17 widget sits at line.from + insertCh with side -1
  ---
  duration_ms: 65.078894
  ...
# Subtest: TM18 entering: new key pops then settles
ok 1284 - TM18 entering: new key pops then settles
  ---
  duration_ms: 63.337921
  ...
# Subtest: TM20 toggle flips class, notice, and refreshes non-daily leaves
ok 1285 - TM20 toggle flips class, notice, and refreshes non-daily leaves
  ---
  duration_ms: 68.934713
  ...
# Subtest: rebuild triggers: doc, viewport, LP field, file switch rebuild; selection alone does not
ok 1286 - rebuild triggers: doc, viewport, LP field, file switch rebuild; selection alone does not
  ---
  duration_ms: 63.111969
  ...
# Subtest: jump guards in-flight, prefers cached ledgerLine over later match
ok 1287 - jump guards in-flight, prefers cached ledgerLine over later match
  ---
  duration_ms: 60.190973
  ...
# Subtest: jump with no open daily leaf attempts the daily open
ok 1288 - jump with no open daily leaf attempts the daily open
  ---
  duration_ms: 88.075139
  ...
# Subtest: home labels: unnamed timed entry uses derived label and 1-based entryLine
ok 1289 - home labels: unnamed timed entry uses derived label and 1-based entryLine
  ---
  duration_ms: 68.677041
  ...
# Subtest: T1 GTD: empty target resolves to the daily note
ok 1290 - T1 GTD: empty target resolves to the daily note
  ---
  duration_ms: 8.581129
  ...
# Subtest: T2 markers: pomodoro mark counts, struck drops, embed counts
ok 1291 - T2 markers: pomodoro mark counts, struck drops, embed counts
  ---
  duration_ms: 0.847518
  ...
# Subtest: T3 closed entries: links under completed/cancelled entries drop
ok 1292 - T3 closed entries: links under completed/cancelled entries drop
  ---
  duration_ms: 0.526084
  ...
# Subtest: T4 shapes: mixed text and deeper descendants drop
ok 1293 - T4 shapes: mixed text and deeper descendants drop
  ---
  duration_ms: 0.574186
  ...
# Subtest: T5 dedupe: same task twice keeps the first position
ok 1294 - T5 dedupe: same task twice keeps the first position
  ---
  duration_ms: 0.695037
  ...
# Subtest: T6 fenced: links inside fenced blocks drop
ok 1295 - T6 fenced: links inside fenced blocks drop
  ---
  duration_ms: 0.380747
  ...
# Subtest: T7 status: the link layer lists every dedicated link
ok 1296 - T7 status: the link layer lists every dedicated link
  ---
  duration_ms: 0.425332
  ...
# Subtest: T8 unresolved: missing notes give no key
ok 1297 - T8 unresolved: missing notes give no key
  ---
  duration_ms: 0.281357
  ...
# Subtest: T9 alias: aliased links count under their target
ok 1298 - T9 alias: aliased links count under their target
  ---
  duration_ms: 0.575659
  ...
# Subtest: laneBudgetFromTasks counts the whole Next lane, Today included
ok 1299 - laneBudgetFromTasks counts the whole Next lane, Today included
  ---
  duration_ms: 1.867574
  ...
# Subtest: laneBudgetFromTasks counts Pending by type and flags over-cap
ok 1300 - laneBudgetFromTasks counts Pending by type and flags over-cap
  ---
  duration_ms: 0.584285
  ...
# Subtest: lane caps come from max_next/max_pending; legacy max_now is ignored
ok 1301 - lane caps come from max_next/max_pending; legacy max_now is ignored
  ---
  duration_ms: 0.331002
  ...
# Subtest: reload event name matches the Tasks bundle subscription
ok 1302 - reload event name matches the Tasks bundle subscription
  ---
  duration_ms: 0.191345
  ...
# Subtest: api v2 shape: Today and lane budgets, no nowBudget
ok 1303 - api v2 shape: Today and lane budgets, no nowBudget
  ---
  duration_ms: 12.557721
  ...
# Subtest: cache rebuild answers isToday/todayRank in ledger order
ok 1304 - cache rebuild answers isToday/todayRank in ledger order
  ---
  duration_ms: 8.049193
  ...
# Subtest: refresh fires only when the key set changes
ok 1305 - refresh fires only when the key set changes
  ---
  duration_ms: 3.101692
  ...
# Subtest: unready to ready with empty TODAY still refreshes open badges
ok 1306 - unready to ready with empty TODAY still refreshes open badges
  ---
  duration_ms: 1.582131
  ...
# Subtest: cache rebuilds on the daily changed event with the event content
ok 1307 - cache rebuilds on the daily changed event with the event content
  ---
  duration_ms: 1.55612
  ...
# Subtest: cache rebuilds once on resolved and at midnight rollover
ok 1308 - cache rebuilds once on resolved and at midnight rollover
  ---
  duration_ms: 1.934583
  ...
# Subtest: computeTodayLinks records entry range and placeholder
ok 1309 - computeTodayLinks records entry range and placeholder
  ---
  duration_ms: 0.693834
  ...
# Subtest: todayOpenEntries and todayRunningEntryLine follow the unique timed rule
ok 1310 - todayOpenEntries and todayRunningEntryLine follow the unique timed rule
  ---
  duration_ms: 0.578725
  ...
# Subtest: resolveTodayLinkKeys keeps duplicates; resolveTodayKeys is first-occurrence
ok 1311 - resolveTodayLinkKeys keeps duplicates; resolveTodayKeys is first-occurrence
  ---
  duration_ms: 0.341262
  ...
# Subtest: todayLinkDetails: named running, placeholder, unnamed home, unnamed none
ok 1312 - todayLinkDetails: named running, placeholder, unnamed home, unnamed none
  ---
  duration_ms: 0.525372
  ...
# Subtest: todayLinkDetails orders running first and keeps one detail per key+entry
ok 1313 - todayLinkDetails orders running first and keeps one detail per key+entry
  ---
  duration_ms: 0.350219
  ...
# Subtest: todayKeyParts splits at the last hash; idsByPath groups block ids
ok 1314 - todayKeyParts splits at the last hash; idsByPath groups block ids
  ---
  duration_ms: 0.357021
  ...
# Subtest: todayDetailsSignature changes only when details change
ok 1315 - todayDetailsSignature changes only when details change
  ---
  duration_ms: 0.442815
  ...
# Subtest: idsByPath and details accessors follow the rebuilt cache
ok 1316 - idsByPath and details accessors follow the rebuilt cache
  ---
  duration_ms: 1.535091
  ...
# Subtest: details-only change refreshes marks without a Tasks reload
ok 1317 - details-only change refreshes marks without a Tasks reload
  ---
  duration_ms: 1.648207
  ...
# Subtest: entered stamps only when the cache was already ready, then prune
ok 1318 - entered stamps only when the cache was already ready, then prune
  ---
  duration_ms: 1.945985
  ...
# Subtest: generation guard: reverse-order async reads keep the newer
ok 1319 - generation guard: reverse-order async reads keep the newer
  ---
  duration_ms: 1.308107
  ...
# Subtest: generation guard: a sync rebuild wins over an in-flight async read
ok 1320 - generation guard: a sync rebuild wins over an in-flight async read
  ---
  duration_ms: 0.978428
  ...
# Subtest: revalidateTodayCache is throttled and refreshes when not ready
ok 1321 - revalidateTodayCache is throttled and refreshes when not ready
  ---
  duration_ms: 1.171426
  ...
# Subtest: revalidateTodayCache respects layoutReady and backwards clock steps
ok 1322 - revalidateTodayCache respects layoutReady and backwards clock steps
  ---
  duration_ms: 0.978738
  ...
# Subtest: a done-today prerequisite shows the glyph
ok 1323 - a done-today prerequisite shows the glyph
  ---
  duration_ms: 8.693315
  ...
# Subtest: done yesterday does not show the glyph
ok 1324 - done yesterday does not show the glyph
  ---
  duration_ms: 0.673375
  ...
# Subtest: a struck link does not show the glyph
ok 1325 - a struck link does not show the glyph
  ---
  duration_ms: 0.243184
  ...
# Subtest: a closed entry does not show the glyph
ok 1326 - a closed entry does not show the glyph
  ---
  duration_ms: 0.243054
  ...
# Subtest: several prerequisites give +N
ok 1327 - several prerequisites give +N
  ---
  duration_ms: 0.778156
  ...
# Subtest: the model refuses every non-glyph shape
ok 1328 - the model refuses every non-glyph shape
  ---
  duration_ms: 1.142891
  ...
# Subtest: unblockedGlyphDoneToday needs DONE plus a today done date
ok 1329 - unblockedGlyphDoneToday needs DONE plus a today done date
  ---
  duration_ms: 0.284282
  ...
# Subtest: tooltip names one prerequisite and counts several
ok 1330 - tooltip names one prerequisite and counts several
  ---
  duration_ms: 0.468033
  ...
# Subtest: Live Preview places one glyph after each unblocked link
ok 1331 - Live Preview places one glyph after each unblocked link
  ---
  duration_ms: 3.54682
  ...
# Subtest: Live Preview draws nothing without a warm cache or a live link
ok 1332 - Live Preview draws nothing without a warm cache or a live link
  ---
  duration_ms: 0.985651
  ...
# Subtest: widget mousedown places the cursor past the link
ok 1333 - widget mousedown places the cursor past the link
  ---
  duration_ms: 0.918253
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
ok 1334 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 1.182608
  ...
# Subtest: Reading view glyphs unblocked rows and dedupes
ok 1335 - Reading view glyphs unblocked rows and dedupes
  ---
  duration_ms: 2.114447
  ...
# Subtest: Reading view refuses every non-glyph row
ok 1336 - Reading view refuses every non-glyph row
  ---
  duration_ms: 2.002261
  ...
# Subtest: api.unblockedGlyph v1 is additive, sync, and never throwing
ok 1337 - api.unblockedGlyph v1 is additive, sync, and never throwing
  ---
  duration_ms: 1.167668
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 1338 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 2.337602
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 1339 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 1.101853
  ...
# Subtest: changed-file and rollover refreshes
ok 1340 - changed-file and rollover refreshes
  ---
  duration_ms: 0.734833
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 1341 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.248464
  ...
# Subtest: styles.css contract: faint glyph, Done token, toggle
ok 1342 - styles.css contract: faint glyph, Done token, toggle
  ---
  duration_ms: 1.078419
  ...
# Subtest: Ledger Vim mappings restore \\p and retain the other normal-mode actions
ok 1343 - Ledger Vim mappings restore \\p and retain the other normal-mode actions
  ---
  duration_ms: 4.822717
  ...
# Subtest: workBadgeTone boundary vectors at cap 100 use exact comparisons
ok 1344 - workBadgeTone boundary vectors at cap 100 use exact comparisons
  ---
  duration_ms: 2.150234
  ...
# Subtest: workBadgeTone at cap 15 has no percentage rounding
ok 1345 - workBadgeTone at cap 15 has no percentage rounding
  ---
  duration_ms: 0.289973
  ...
# Subtest: workBadgeTone default caps, small caps, and cap changes
ok 1346 - workBadgeTone default caps, small caps, and cap changes
  ---
  duration_ms: 0.337464
  ...
# Subtest: workBadgeTone never coerces invalid input to zero
ok 1347 - workBadgeTone never coerces invalid input to zero
  ---
  duration_ms: 2.471217
  ...
# Subtest: TODAY links bands with themes at cap 3
ok 1348 - TODAY links bands with themes at cap 3
  ---
  duration_ms: 0.507479
  ...
# Subtest: TODAY theme overflow forces red, exact cap does not
ok 1349 - TODAY theme overflow forces red, exact cap does not
  ---
  duration_ms: 0.416084
  ...
# Subtest: TODAY unavailable stays neutral, empty section is grey
ok 1350 - TODAY unavailable stays neutral, empty section is grey
  ---
  duration_ms: 2.007713
  ...
# Subtest: PENDING/NEXT models color the section, READY its gated count
ok 1351 - PENDING/NEXT models color the section, READY its gated count
  ---
  duration_ms: 0.890781
  ...
# Subtest: READY uses its gated count even when the total lane is larger
ok 1352 - READY uses its gated count even when the total lane is larger
  ---
  duration_ms: 0.412988
  ...
# Subtest: cap equality still emits no cap lint
ok 1353 - cap equality still emits no cap lint
  ---
  duration_ms: 4.346237
  ...
# Subtest: lane DOM keeps exactly one tone through transitions and unavailability
ok 1354 - lane DOM keeps exactly one tone through transitions and unavailability
  ---
  duration_ms: 13.411
  ...
# Subtest: READY DOM keeps exactly one tone and daily/dashboard models agree
ok 1355 - READY DOM keeps exactly one tone and daily/dashboard models agree
  ---
  duration_ms: 2.136478
  ...
# SKIP dashboard integration: BOB_DASHBOARD_FILE is not set
# SKIP dashboard fallback integration: BOB_DASHBOARD_FILE is not set
# SKIP dash CSS contract: BOB_DASHBOARD_FILE is not set
# Subtest: daily TODAY chip uses the theme-overflow tone
ok 1356 - daily TODAY chip uses the theme-overflow tone
  ---
  duration_ms: 28.175001
  ...
# Subtest: dashboard integration uses Work tones, TODAY override, and keeps Work order
ok 1357 - dashboard integration uses Work tones, TODAY override, and keeps Work order
  ---
  duration_ms: 2.121579
  ...
# Subtest: dashboard fallbacks keep Work tones without plugin renderers or colors
ok 1358 - dashboard fallbacks keep Work tones without plugin renderers or colors
  ---
  duration_ms: 0.666141
  ...
# Subtest: Work tone CSS covers each tone and uses the shared magenta value
ok 1359 - Work tone CSS covers each tone and uses the shared magenta value
  ---
  duration_ms: 1.344106
  ...
# Subtest: RBW6 mergeTargetPreparations keeps one write at the strongest lane
ok 1360 - RBW6 mergeTargetPreparations keeps one write at the strongest lane
  ---
  duration_ms: 3.794171
  ...
# Subtest: §15.7 notices use curly quotes and the Ready → Blocked copy
ok 1361 - §15.7 notices use curly quotes and the Ready → Blocked copy
  ---
  duration_ms: 0.725605
  ...
# Subtest: RBP1 same-note add is one transaction and matches forward bytes
ok 1362 - RBP1 same-note add is one transaction and matches forward bytes
  ---
  duration_ms: 40.654612
  ...
# Subtest: RBP2 background-leaf T matches forward bytes
ok 1363 - RBP2 background-leaf T matches forward bytes
  ---
  duration_ms: 8.900609
  ...
# Subtest: RBP3 closed T is written through vault.process and matches forward bytes
ok 1364 - RBP3 closed T is written through vault.process and matches forward bytes
  ---
  duration_ms: 6.251494
  ...
# Subtest: RBP4 ordinary transfer; a ^prj N is never raised
ok 1365 - RBP4 ordinary transfer; a ^prj N is never raised
  ---
  duration_ms: 20.225607
  ...
# Subtest: RBP5 consumed Pomodoro link matches forward bytes
ok 1366 - RBP5 consumed Pomodoro link matches forward bytes
  ---
  duration_ms: 8.025319
  ...
# Subtest: RBP6 project T with residents and a sub-project matches forward bytes
ok 1367 - RBP6 project T with residents and a sub-project matches forward bytes
  ---
  duration_ms: 25.158764
  ...
# Subtest: RBP7 two dependents in different lanes prepare N once at [/]
ok 1368 - RBP7 two dependents in different lanes prepare N once at [/]
  ---
  duration_ms: 15.271941
  ...
# Subtest: RBP8 counted sources N1 and N2 match forward(T + N1, N2)
ok 1369 - RBP8 counted sources N1 and N2 match forward(T + N1, N2)
  ---
  duration_ms: 12.066051
  ...
# Subtest: RBP9 blocks_lines false writes no BLOCKS and still ids N
ok 1370 - RBP9 blocks_lines false writes no BLOCKS and still ids N
  ---
  duration_ms: 7.605558
  ...
# Subtest: RBP10 removing the last reason matches forward removal
ok 1371 - RBP10 removing the last reason matches forward removal
  ---
  duration_ms: 10.485363
  ...
# Subtest: RBW1 a changed source note writes nothing
ok 1372 - RBW1 a changed source note writes nothing
  ---
  duration_ms: 3.167397
  ...
# Subtest: RBW2 one changed T note still lands the others and omits it from BLOCKS
ok 1373 - RBW2 one changed T note still lands the others and omits it from BLOCKS
  ---
  duration_ms: 4.546417
  ...
# Subtest: RBW3 already-present picks write nothing
ok 1374 - RBW3 already-present picks write nothing
  ---
  duration_ms: 2.86079
  ...
# Subtest: RBW4 cleanup runs for T's that committed when N lives in today's daily note
ok 1375 - RBW4 cleanup runs for T's that committed when N lives in today's daily note
  ---
  duration_ms: 21.152908
  ...
# Subtest: RBW6 counted forward two-lane dependents prepare N once
ok 1376 - RBW6 counted forward two-lane dependents prepare N once
  ---
  duration_ms: 16.991614
  ...
# Subtest: A1 N above two T's in one note matches forward (open and closed note)
ok 1377 - A1 N above two T's in one note matches forward (open and closed note)
  ---
  duration_ms: 29.686836
  ...
# Subtest: A1 N below two T's matches forward bytes
ok 1378 - A1 N below two T's matches forward bytes
  ---
  duration_ms: 6.838793
  ...
# Subtest: A2 forward stamps the dependent when a prerequisite above gains BLOCKS
ok 1379 - A2 forward stamps the dependent when a prerequisite above gains BLOCKS
  ---
  duration_ms: 1.856754
  ...
# Subtest: A1 mixed same-note and cross-note picks keep N's lane rise (RBP7 variant)
ok 1380 - A1 mixed same-note and cross-note picks keep N's lane rise (RBP7 variant)
  ---
  duration_ms: 8.509935
  ...
# Subtest: A1 RBP1 with N truly lacking ^id is prompted an id and matches forward
ok 1381 - A1 RBP1 with N truly lacking ^id is prompted an id and matches forward
  ---
  duration_ms: 2.589322
  ...
# Subtest: A1 N lacking ^id in a closed note above T keeps its BLOCKS line under N
ok 1382 - A1 N lacking ^id in a closed note above T keeps its BLOCKS line under N
  ---
  duration_ms: 1.816588
  ...
# Subtest: A3 mirror lists the committed T's by identity (N above T1, X, T2)
ok 1383 - A3 mirror lists the committed T's by identity (N above T1, X, T2)
  ---
  duration_ms: 4.738155
  ...
# Subtest: A4 notices name T, not N (add, remove, project, counted)
ok 1384 - A4 notices name T, not N (add, remove, project, counted)
  ---
  duration_ms: 8.850223
  ...
# Subtest: A5 the writer's stale notice is returned once and never shown by the writer
ok 1385 - A5 the writer's stale notice is returned once and never shown by the writer
  ---
  duration_ms: 0.499965
  ...
# Subtest: A6 a changed T row (rawLine) is refused before any write
ok 1386 - A6 a changed T row (rawLine) is refused before any write
  ---
  duration_ms: 0.372862
  ...
# Subtest: A7 RBW2 keeps the failed T's Pomodoro link and consumes the committed one
ok 1387 - A7 RBW2 keeps the failed T's Pomodoro link and consumes the committed one
  ---
  duration_ms: 5.274879
  ...
# Subtest: A8 closed-note T guards run when the gesture is applied
ok 1388 - A8 closed-note T guards run when the gesture is applied
  ---
  duration_ms: 4.697256
  ...
# Subtest: A9 a ^prj T's residents recover with [unblocked::] when N lives in a daily note
ok 1389 - A9 a ^prj T's residents recover with [unblocked::] when N lives in a daily note
  ---
  duration_ms: 20.696214
  ...
# Subtest: A5 a preparation no write can carry fails the plan instead of being dropped
ok 1390 - A5 a preparation no write can carry fails the plan instead of being dropped
  ---
  duration_ms: 1.122593
  ...
# Subtest: applyDependencyEdit adding a first cross-note prerequisite keeps the dependent's cursor
ok 1391 - applyDependencyEdit adding a first cross-note prerequisite keeps the dependent's cursor
  ---
  duration_ms: 5.599639
  ...
# Subtest: applyBlocksEdit giving a source its first BLOCKS line keeps the source's cursor
ok 1392 - applyBlocksEdit giving a source its first BLOCKS line keeps the source's cursor
  ---
  duration_ms: 11.63085
  ...
# Subtest: nav BK1–BK2 accept canonical BLOCKS lines
ok 1393 - nav BK1–BK2 accept canonical BLOCKS lines
  ---
  duration_ms: 5.13923
  ...
# Subtest: nav BK3–BK11 canonicalise
ok 1394 - nav BK3–BK11 canonicalise
  ---
  duration_ms: 0.915448
  ...
# Subtest: nav BK12 empty, BK13–BK15 malformed
ok 1395 - nav BK12 empty, BK13–BK15 malformed
  ---
  duration_ms: 0.544389
  ...
# Subtest: nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse
ok 1396 - nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse
  ---
  duration_ms: 0.639611
  ...
# Subtest: nav BK21 code-point sort and writer format
ok 1397 - nav BK21 code-point sort and writer format
  ---
  duration_ms: 0.391538
  ...
# Subtest: nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS
ok 1398 - nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS
  ---
  duration_ms: 0.832408
  ...
# Subtest: nav BW18 conversion drops BLOCKS like Sub-projects
ok 1399 - nav BW18 conversion drops BLOCKS like Sub-projects
  ---
  duration_ms: 1.630412
  ...
# Subtest: nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner
ok 1400 - nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner
  ---
  duration_ms: 1.344476
  ...
# Subtest: nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists
ok 1401 - nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists
  ---
  duration_ms: 4.286613
  ...
# Subtest: nav MC1/MC2 deferred Pomodoro cleanup skips managed lines
ok 1402 - nav MC1/MC2 deferred Pomodoro cleanup skips managed lines
  ---
  duration_ms: 0.469897
  ...
# Subtest: showBlocksStage opens from a task with reverse CURRENT and RESULTS
ok 1403 - showBlocksStage opens from a task with reverse CURRENT and RESULTS
  ---
  duration_ms: 31.091358
  ...
# Subtest: showBlocksStage opens from a counted session
ok 1404 - showBlocksStage opens from a counted session
  ---
  duration_ms: 5.790664
  ...
# Subtest: showBlocksStage opens on a Task Link target note
ok 1405 - showBlocksStage opens on a Task Link target note
  ---
  duration_ms: 3.09112
  ...
# Subtest: RBU1 empty query uses today-first then In Progress, Next, same-note, rest
ok 1406 - RBU1 empty query uses today-first then In Progress, Next, same-note, rest
  ---
  duration_ms: 15.368896
  ...
# Subtest: RBU2 today-linked rows carry 🍅 running and strip names the entry
ok 1407 - RBU2 today-linked rows carry 🍅 running and strip names the entry
  ---
  duration_ms: 1.427815
  ...
# Subtest: RBU3 CURRENT 🔑 only when N is the last reason
ok 1408 - RBU3 CURRENT 🔑 only when N is the last reason
  ---
  duration_ms: 1.853708
  ...
# Subtest: RBU4 footer verbs are block, remove, and apply N
ok 1409 - RBU4 footer verbs are block, remove, and apply N
  ---
  duration_ms: 2.908802
  ...
# Subtest: RBU5 subtitle at rest, with marks, and names this task first
ok 1410 - RBU5 subtitle at rest, with marks, and names this task first
  ---
  duration_ms: 3.474813
  ...
# Subtest: RBG1 N itself is excluded from RESULTS
ok 1411 - RBG1 N itself is excluded from RESULTS
  ---
  duration_ms: 2.061085
  ...
# Subtest: RBG2 a cycle disables the row with path tooltip copy
ok 1412 - RBG2 a cycle disables the row with path tooltip copy
  ---
  duration_ms: 2.600654
  ...
# Subtest: RBG3 ^prj T with N inside the project is inside this project
ok 1413 - RBG3 ^prj T with N inside the project is inside this project
  ---
  duration_ms: 3.786407
  ...
# Subtest: RBG3 descendant N disables the parent project as a sub-project
ok 1414 - RBG3 descendant N disables the parent project as a sub-project
  ---
  duration_ms: 2.140866
  ...
# Subtest: RBG4 a malformed or second Depends-On line is guarded
ok 1415 - RBG4 a malformed or second Depends-On line is guarded
  ---
  duration_ms: 1.773165
  ...
# Subtest: RBG5 stale refuse reopens in the Blocks direction
ok 1416 - RBG5 stale refuse reopens in the Blocks direction
  ---
  duration_ms: 5.863512
  ...
# Subtest: RBG5 for T: a T changed after stage open refuses once and writes nothing
ok 1417 - RBG5 for T: a T changed after stage open refuses once and writes nothing
  ---
  duration_ms: 13.349241
  ...
# Subtest: today's links survive a pool refresh that lands while the daily note loads
ok 1418 - today's links survive a pool refresh that lands while the daily note loads
  ---
  duration_ms: 41.96828
  ...
# Subtest: RBG8 Esc from the stage or the block-ID prompt writes nothing
ok 1419 - RBG8 Esc from the stage or the block-ID prompt writes nothing
  ---
  duration_ms: 3.545227
  ...
# Subtest: missing source ^id opens the block-ID prompt and Esc allocates none
ok 1420 - missing source ^id opens the block-ID prompt and Esc allocates none
  ---
  duration_ms: 2.604842
  ...
# Subtest: RBP11 inbox route runs first then the Blocks write
ok 1421 - RBP11 inbox route runs first then the Blocks write
  ---
  duration_ms: 2.387106
  ...
# Subtest: RBW5 review walk stays unless the commit takes N out of today's walk
ok 1422 - RBW5 review walk stays unless the commit takes N out of today's walk
  ---
  duration_ms: 8.608222
  ...
# Subtest: marks commit add and remove together; counted uses k/n block
ok 1423 - marks commit add and remove together; counted uses k/n block
  ---
  duration_ms: 3.924411
  ...
# Subtest: strip text covers RESULTS, BLOCKED, CURRENT, disabled, marks, and ^prj
ok 1424 - strip text covers RESULTS, BLOCKED, CURRENT, disabled, marks, and ^prj
  ---
  duration_ms: 0.431022
  ...
# Subtest: counted subtitle drops the ⇥ hint because marks are off in counted sessions
ok 1425 - counted subtitle drops the ⇥ hint because marks are off in counted sessions
  ---
  duration_ms: 1.46703
  ...
# Subtest: 🔑 tooltip and 🍅 tooltip render on badges
ok 1426 - 🔑 tooltip and 🍅 tooltip render on badges
  ---
  duration_ms: 1.592029
  ...
# Subtest: Tab marks Blocks CURRENT rows and Enter removes both dependents
ok 1427 - Tab marks Blocks CURRENT rows and Enter removes both dependents
  ---
  duration_ms: 26.823963
  ...
# Subtest: SB1-SB9 dependent IDs match the successor mint vectors
ok 1428 - SB1-SB9 dependent IDs match the successor mint vectors
  ---
  duration_ms: 4.204927
  ...
# Subtest: BW1 same-note add mints and writes BLOCKS in the dependent's single transaction
ok 1429 - BW1 same-note add mints and writes BLOCKS in the dependent's single transaction
  ---
  duration_ms: 16.646956
  ...
# Subtest: BW2 cross-note add follows the dependent commit and writes the target note
ok 1430 - BW2 cross-note add follows the dependent commit and writes the target note
  ---
  duration_ms: 8.617508
  ...
# Subtest: BW4 cross-note target preparation precedes the reverse-line preimage
ok 1431 - BW4 cross-note target preparation precedes the reverse-line preimage
  ---
  duration_ms: 3.091182
  ...
# Subtest: BW3 stale cross-note preimage leaves the forward write standing and shows the suffix
ok 1432 - BW3 stale cross-note preimage leaves the forward write standing and shows the suffix
  ---
  duration_ms: 1.916077
  ...
# Subtest: BW5 removal deletes the reverse line when its last dependent leaves
ok 1433 - BW5 removal deletes the reverse line when its last dependent leaves
  ---
  duration_ms: 6.566323
  ...
# Subtest: BW6 an already mirrored edge is a byte-identical no-op
ok 1434 - BW6 an already mirrored edge is a byte-identical no-op
  ---
  duration_ms: 1.592329
  ...
# Subtest: BW7 closed owners stay frozen
ok 1435 - BW7 closed owners stay frozen
  ---
  duration_ms: 2.029894
  ...
# Subtest: BW8 malformed reverse lines stay untouched and report the failed mirror
ok 1436 - BW8 malformed reverse lines stay untouched and report the failed mirror
  ---
  duration_ms: 2.736435
  ...
# Subtest: BW15 config defaults on, honors false, and invalid values fall back on
ok 1437 - BW15 config defaults on, honors false, and invalid values fall back on
  ---
  duration_ms: 1.08923
  ...
# Subtest: BW17 planner output follows BK21 Unicode code-point ordering
ok 1438 - BW17 planner output follows BK21 Unicode code-point ordering
  ---
  duration_ms: 0.919826
  ...
# Subtest: duplicate BLOCKS children merge their known dependents and preserve CRLF
ok 1439 - duplicate BLOCKS children merge their known dependents and preserve CRLF
  ---
  duration_ms: 0.639361
  ...
# Subtest: BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270)
ok 1440 - BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270)
  ---
  duration_ms: 12.738605
  ...
# Subtest: counted remove-from-all drops every dependent from the same-note BLOCKS line (420)
ok 1441 - counted remove-from-all drops every dependent from the same-note BLOCKS line (420)
  ---
  duration_ms: 3.12745
  ...
# Subtest: vault counted add composes cross-note follow-ups for every source (420)
ok 1442 - vault counted add composes cross-note follow-ups for every source (420)
  ---
  duration_ms: 2.82954
  ...
# Subtest: marked batch add writes every same-note target onto BLOCKS in one plan (430)
ok 1443 - marked batch add writes every same-note target onto BLOCKS in one plan (430)
  ---
  duration_ms: 2.78712
  ...
# Subtest: counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600)
ok 1444 - counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600)
  ---
  duration_ms: 11.479111
  ...
# Subtest: BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves
ok 1445 - BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves
  ---
  duration_ms: 5.122057
  ...
# Subtest: BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS
ok 1446 - BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS
  ---
  duration_ms: 6.39123
  ...
# Subtest: hand-edit clear path routes through the BLOCKS seam (600)
ok 1447 - hand-edit clear path routes through the BLOCKS seam (600)
  ---
  duration_ms: 3.256906
  ...
# Subtest: BW18 conversion never copies a BLOCKS line as a user child
ok 1448 - BW18 conversion never copies a BLOCKS line as a user child
  ---
  duration_ms: 1.404821
  ...
# Subtest: BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it
ok 1449 - BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it
  ---
  duration_ms: 6.647359
  ...
# Subtest: review checklist group helpers format exact completion and close notices
ok 1450 - review checklist group helpers format exact completion and close notices
  ---
  duration_ms: 9.983377
  ...
# Subtest: claim declines without a current exact PRE/POST walk landing
ok 1451 - claim declines without a current exact PRE/POST walk landing
  ---
  duration_ms: 25.735243
  ...
# Subtest: a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
ok 1452 - a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
  ---
  duration_ms: 7.427078
  ...
# Subtest: checklist Ctrl+Enter holds its landing through the actual successor picker
ok 1453 - checklist Ctrl+Enter holds its landing through the actual successor picker
  ---
  duration_ms: 25.304782
  ...
# Subtest: seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
ok 1454 - seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
  ---
  duration_ms: 70.053788
  ...
# Subtest: a landed [?] checklist chore is claimed and completed
ok 1455 - a landed [?] checklist chore is claimed and completed
  ---
  duration_ms: 0.883396
  ...
# Subtest: ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
ok 1456 - ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
  ---
  duration_ms: 2.446601
  ...
# Subtest: live successor filtering skips a stale completed row
ok 1457 - live successor filtering skips a stale completed row
  ---
  duration_ms: 0.827811
  ...
# Subtest: live group filtering reads each cross-note path once
ok 1458 - live group filtering reads each cross-note path once
  ---
  duration_ms: 0.606999
  ...
# Subtest: Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
ok 1459 - Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
  ---
  duration_ms: 3.377116
  ...
# Subtest: POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
ok 1460 - POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
  ---
  duration_ms: 8.22598
  ...
# Subtest: ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
ok 1461 - ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
  ---
  duration_ms: 2.041937
  ...
# Subtest: completion failure preserves cursor and landing and reports the Tasks failure
ok 1462 - completion failure preserves cursor and landing and reports the Tasks failure
  ---
  duration_ms: 0.671542
  ...
# Subtest: reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
ok 1463 - reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
  ---
  duration_ms: 2.962295
  ...
# Subtest: Alt+F on PRE stays with remaining PRE count and never stamps
ok 1464 - Alt+F on PRE stays with remaining PRE count and never stamps
  ---
  duration_ms: 10.046386
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a stale cache
ok 1465 - Ctrl+Alt+F completes seven PRE rows from a stale cache
  ---
  duration_ms: 24.2245
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a refreshed cache
ok 1466 - Ctrl+Alt+F completes seven PRE rows from a refreshed cache
  ---
  duration_ms: 9.603111
  ...
# Subtest: POST stays put with the closing notice
ok 1467 - POST stays put with the closing notice
  ---
  duration_ms: 1.758306
  ...
# Subtest: manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
ok 1468 - manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
  ---
  duration_ms: 2.946805
  ...
# Subtest: manual Ctrl+Enter then ]s from a stale cache uses text-first identity
ok 1469 - manual Ctrl+Enter then ]s from a stale cache uses text-first identity
  ---
  duration_ms: 0.801911
  ...
# Subtest: counted Alt+F skips checklist rows with the skip tail
ok 1470 - counted Alt+F skips checklist rows with the skip tail
  ---
  duration_ms: 9.945044
  ...
# Subtest: missing cycler gate on a PRE row writes nothing
ok 1471 - missing cycler gate on a PRE row writes nothing
  ---
  duration_ms: 1.090672
  ...
# Subtest: missing ledger checklist gate on a tagged line writes nothing
ok 1472 - missing ledger checklist gate on a tagged line writes nothing
  ---
  duration_ms: 0.679317
  ...
# Subtest: a tagged line that is not a queue match falls through to recurring refusal
ok 1473 - a tagged line that is not a queue match falls through to recurring refusal
  ---
  duration_ms: 0.57679
  ...
# Subtest: formatFreshStampChecklistSkipTail names the skipped count
ok 1474 - formatFreshStampChecklistSkipTail names the skipped count
  ---
  duration_ms: 0.247953
  ...
# Subtest: partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
ok 1475 - partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
  ---
  duration_ms: 0.394493
  ...
# Subtest: Task Link Alt+F skips a PRE target with the skip notice
ok 1476 - Task Link Alt+F skips a PRE target with the skip notice
  ---
  duration_ms: 4.521532
  ...
# Subtest: P0 at interval 7 enters P2 with a previewed decay date and kept tail
ok 1477 - P0 at interval 7 enters P2 with a previewed decay date and kept tail
  ---
  duration_ms: 6.765453
  ...
# Subtest: P0 at interval 30 enters P3
ok 1478 - P0 at interval 30 enters P3
  ---
  duration_ms: 0.995981
  ...
# Subtest: fixed enter overrides the interval scan
ok 1479 - fixed enter overrides the interval scan
  ---
  duration_ms: 0.763067
  ...
# Subtest: unknown enter disables Not now without disabling Keep/Reword
ok 1480 - unknown enter disables Not now without disabling Keep/Reword
  ---
  duration_ms: 0.900298
  ...
# Subtest: P0 with no suitable level stays unavailable and never shortens the lease
ok 1481 - P0 with no suitable level stays unavailable and never shortens the lease
  ---
  duration_ms: 0.528198
  ...
# Subtest: custom level order resolves entry in ladder order
ok 1482 - custom level order resolves entry in ladder order
  ---
  duration_ms: 0.745433
  ...
# Subtest: unknown priority value disables Not now only
ok 1483 - unknown priority value disables Not now only
  ---
  duration_ms: 0.657415
  ...
# Subtest: prioritized P2 below its roll limit stays on the same level
ok 1484 - prioritized P2 below its roll limit stays on the same level
  ---
  duration_ms: 1.279632
  ...
# Subtest: P2 at its roll limit decays to P3
ok 1485 - P2 at its roll limit decays to P3
  ---
  duration_ms: 2.421993
  ...
# Subtest: P2 streak derives from the task Schedule Log
ok 1486 - P2 streak derives from the task Schedule Log
  ---
  duration_ms: 11.183739
  ...
# Subtest: configured decay:false keeps rolling past the limit
ok 1487 - configured decay:false keeps rolling past the limit
  ---
  duration_ms: 0.730093
  ...
# Subtest: per-level rolls:0 decays immediately
ok 1488 - per-level rolls:0 decays immediately
  ---
  duration_ms: 0.591078
  ...
# Subtest: terminal cancel substitutes a truthful same-level card roll
ok 1489 - terminal cancel substitutes a truthful same-level card roll
  ---
  duration_ms: 0.792082
  ...
# Subtest: no future date in the window refuses Not now
ok 1490 - no future date in the window refuses Not now
  ---
  duration_ms: 0.571822
  ...
# Subtest: Less often steps 7/14/30 to the next preset with a decision reason
ok 1491 - Less often steps 7/14/30 to the next preset with a decision reason
  ---
  duration_ms: 1.337333
  ...
# Subtest: Less often at 90+ opens the constrained custom picker; 365 is unavailable
ok 1492 - Less often at 90+ opens the constrained custom picker; 365 is unavailable
  ---
  duration_ms: 0.876924
  ...
# Subtest: previewed dates are stable for one random draw
ok 1493 - previewed dates are stable for one random draw
  ---
  duration_ms: 0.595557
  ...
# Subtest: Keep saturates at 999 and Drop preserves keeps history
ok 1494 - Keep saturates at 999 and Drop preserves keeps history
  ---
  duration_ms: 1.055876
  ...
# Subtest: kept tails preserve roll classification; decisions break it deliberately
ok 1495 - kept tails preserve roll classification; decisions break it deliberately
  ---
  duration_ms: 4.632894
  ...
# Subtest: invalid priority config offers no priority-changing action
ok 1496 - invalid priority config offers no priority-changing action
  ---
  duration_ms: 1.015458
  ...
# Subtest: decay off disables Not now but keeps counting
ok 1497 - decay off disables Not now but keeps counting
  ---
  duration_ms: 0.388401
  ...
# Subtest: explicit level picks cover the ladder with previewed rolls
ok 1498 - explicit level picks cover the ladder with previewed rolls
  ---
  duration_ms: 2.187475
  ...
# Subtest: card model is deeply frozen
ok 1499 - card model is deeply frozen
  ---
  duration_ms: 0.373032
  ...
# Subtest: single Alt+F on an at-limit task opens the card and writes nothing
ok 1500 - single Alt+F on an at-limit task opens the card and writes nothing
  ---
  duration_ms: 21.77202
  ...
# Subtest: dismissing the card writes nothing and does not advance
ok 1501 - dismissing the card writes nothing and does not advance
  ---
  duration_ms: 3.386674
  ...
# Subtest: early dates open the card and write nothing
ok 1502 - early dates open the card and write nothing
  ---
  duration_ms: 1.664988
  ...
# Subtest: namespace v5 with decide true stamps counted and opens no card
ok 1503 - namespace v5 with decide true stamps counted and opens no card
  ---
  duration_ms: 7.293272
  ...
# Subtest: stale task-line change writes nothing
ok 1504 - stale task-line change writes nothing
  ---
  duration_ms: 2.938608
  ...
# Subtest: stale local-day change writes nothing
ok 1505 - stale local-day change writes nothing
  ---
  duration_ms: 3.348501
  ...
# Subtest: stale decay-config change writes nothing
ok 1506 - stale decay-config change writes nothing
  ---
  duration_ms: 2.475575
  ...
# Subtest: stale priority-ladder config writes nothing
ok 1507 - stale priority-ladder config writes nothing
  ---
  duration_ms: 3.043601
  ...
# Subtest: stale child Schedule Log writes nothing
ok 1508 - stale child Schedule Log writes nothing
  ---
  duration_ms: 11.140685
  ...
# Subtest: Not now stamps, clears keeps, and advances exactly once
ok 1509 - Not now stamps, clears keeps, and advances exactly once
  ---
  duration_ms: 10.143924
  ...
# Subtest: Keep counts once and saturates at 999 without reset
ok 1510 - Keep counts once and saturates at 999 without reset
  ---
  duration_ms: 4.517041
  ...
# Subtest: Keep with a reason logs that reason in the Rotten Log entry
ok 1511 - Keep with a reason logs that reason in the Rotten Log entry
  ---
  duration_ms: 2.297486
  ...
# Subtest: Keep carries the logged history and preview keeps in its context
ok 1512 - Keep carries the logged history and preview keeps in its context
  ---
  duration_ms: 2.69282
  ...
# Subtest: Keep with a stale child log during the stage refuses and rebuilds
ok 1513 - Keep with a stale child log during the stage refuses and rebuilds
  ---
  duration_ms: 2.221621
  ...
# Subtest: Keep with advance commits once and advances exactly once
ok 1514 - Keep with advance commits once and advances exactly once
  ---
  duration_ms: 2.087474
  ...
# Subtest: Reword stamps, clears, logs, and never advances
ok 1515 - Reword stamps, clears, logs, and never advances
  ---
  duration_ms: 2.922137
  ...
# Subtest: Drop cancels with the dropped-after-keeps reason and keeps history
ok 1516 - Drop cancels with the dropped-after-keeps reason and keeps history
  ---
  duration_ms: 1.813973
  ...
# Subtest: Less often at 90+ opens the picker and dismiss writes nothing
ok 1517 - Less often at 90+ opens the picker and dismiss writes nothing
  ---
  duration_ms: 1.577071
  ...
# Subtest: counted session skips at-limit and counts below-limit
ok 1518 - counted session skips at-limit and counts below-limit
  ---
  duration_ms: 2.408949
  ...
# Subtest: counted session skips at-limit on an early date
ok 1519 - counted session skips at-limit on an early date
  ---
  duration_ms: 33.284173
  ...
# Subtest: counted session with every target skipped writes nothing
ok 1520 - counted session with every target skipped writes nothing
  ---
  duration_ms: 1.478412
  ...
# Subtest: opening the card writes nothing and shows the Keep row detail
ok 1521 - opening the card writes nothing and shows the Keep row detail
  ---
  duration_ms: 19.182455
  ...
# Subtest: Esc on the rows closes the card and writes nothing
ok 1522 - Esc on the rows closes the card and writes nothing
  ---
  duration_ms: 3.322594
  ...
# Subtest: Keep swaps the rows for the reason stage without closing
ok 1523 - Keep swaps the rows for the reason stage without closing
  ---
  duration_ms: 3.628786
  ...
# Subtest: repeat Alt+F never enters or submits the stage
ok 1524 - repeat Alt+F never enters or submits the stage
  ---
  duration_ms: 2.15304
  ...
# Subtest: Esc in the stage returns to the rows; a second Esc writes nothing
ok 1525 - Esc in the stage returns to the rows; a second Esc writes nothing
  ---
  duration_ms: 8.093759
  ...
# Subtest: Keep stage Enter logs the reason with one transaction; one undo restores
ok 1526 - Keep stage Enter logs the reason with one transaction; one undo restores
  ---
  duration_ms: 20.628686
  ...
# Subtest: blank Keep stage Enter logs no reason given
ok 1527 - blank Keep stage Enter logs no reason given
  ---
  duration_ms: 15.354058
  ...
# Subtest: a double Enter submits once
ok 1528 - a double Enter submits once
  ---
  duration_ms: 17.150216
  ...
# Subtest: IME Enter never submits the stage
ok 1529 - IME Enter never submits the stage
  ---
  duration_ms: 8.391278
  ...
# Subtest: the card header shows the logged count and last reason
ok 1530 - the card header shows the logged count and last reason
  ---
  duration_ms: 13.661206
  ...
# Subtest: an unreadable log shows the header even with no countable entries
ok 1531 - an unreadable log shows the header even with no countable entries
  ---
  duration_ms: 0.364696
  ...
# Subtest: the decay card Keep stage uses the reviews streak copy
ok 1532 - the decay card Keep stage uses the reviews streak copy
  ---
  duration_ms: 0.473414
  ...
# Subtest: ambiguous Rotten Logs refuse the Keep write
ok 1533 - ambiguous Rotten Logs refuse the Keep write
  ---
  duration_ms: 7.965705
  ...
# Subtest: availability: decay on (or absent) may ask; decay off never asks
ok 1534 - availability: decay on (or absent) may ask; decay off never asks
  ---
  duration_ms: 2.46761
  ...
# Subtest: trigger: only an explicit decide row decides
ok 1535 - trigger: only an explicit decide row decides
  ---
  duration_ms: 0.460509
  ...
# Subtest: partition: exact at-limit rows skip, everything else stamps
ok 1536 - partition: exact at-limit rows skip, everything else stamps
  ---
  duration_ms: 2.22693
  ...
# Subtest: partition: empty and malformed input stamps nothing and skips nothing
ok 1537 - partition: empty and malformed input stamps nothing and skips nothing
  ---
  duration_ms: 0.355799
  ...
# Subtest: partition: enabled false stamps decision rows (older namespace fallback)
ok 1538 - partition: enabled false stamps decision rows (older namespace fallback)
  ---
  duration_ms: 0.350539
  ...
# Subtest: skip wording: singular, plural, and all-skipped notices
ok 1539 - skip wording: singular, plural, and all-skipped notices
  ---
  duration_ms: 0.498101
  ...
# Subtest: reword cursor: lands at the end of the task body before metadata
ok 1540 - reword cursor: lands at the end of the task body before metadata
  ---
  duration_ms: 0.586009
  ...
# Subtest: captured age: optional context ages, null when created is missing
ok 1541 - captured age: optional context ages, null when created is missing
  ---
  duration_ms: 0.770862
  ...
# Subtest: rows: P0 entry shows the recommended Not now with a clean window
ok 1542 - rows: P0 entry shows the recommended Not now with a clean window
  ---
  duration_ms: 6.269267
  ...
# Subtest: rows: invalid priority config disables Not now and levels, keeps safe rows
ok 1543 - rows: invalid priority config disables Not now and levels, keeps safe rows
  ---
  duration_ms: 0.918443
  ...
# Subtest: rows: picker-mode Less often and 365-day cap
ok 1544 - rows: picker-mode Less often and 365-day cap
  ---
  duration_ms: 1.248082
  ...
# Subtest: rows: terminal ladder keeps Enter available and never cancels
ok 1545 - rows: terminal ladder keeps Enter available and never cancels
  ---
  duration_ms: 1.322003
  ...
# Subtest: modal: Enter approves once; later keys cannot approve again
ok 1546 - modal: Enter approves once; later keys cannot approve again
  ---
  duration_ms: 1.234536
  ...
# Subtest: modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
ok 1547 - modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
  ---
  duration_ms: 0.890409
  ...
# Subtest: modal: key repeat and modified keys never approve
ok 1548 - modal: key repeat and modified keys never approve
  ---
  duration_ms: 0.528929
  ...
# Subtest: modal: Esc changes nothing — dismiss without a choice
ok 1549 - modal: Esc changes nothing — dismiss without a choice
  ---
  duration_ms: 0.454707
  ...
# Subtest: modal: unavailable actions cannot be chosen
ok 1550 - modal: unavailable actions cannot be chosen
  ---
  duration_ms: 0.38779
  ...
# Subtest: modal: a double callback applies once
ok 1551 - modal: a double callback applies once
  ---
  duration_ms: 0.552845
  ...
# Subtest: capability: the nav api exposes the card while loaded
ok 1552 - capability: the nav api exposes the card while loaded
  ---
  duration_ms: 1.069622
  ...
# Subtest: capability: unload drops the card so marks stop promising it
ok 1553 - capability: unload drops the card so marks stop promising it
  ---
  duration_ms: 0.49271
  ...
# Subtest: ladder lookup: the first priority property wins, null without one
ok 1554 - ladder lookup: the first priority property wins, null without one
  ---
  duration_ms: 0.553266
  ...
# Subtest: stage entry resolves the line itself and refuses prose
ok 1555 - stage entry resolves the line itself and refuses prose
  ---
  duration_ms: 6.176751
  ...
# Subtest: Ctrl+Shift+P on a BLOCKS line opens the owner's Blocks stage directly
ok 1556 - Ctrl+Shift+P on a BLOCKS line opens the owner's Blocks stage directly
  ---
  duration_ms: 3.090218
  ...
# Subtest: Ctrl+Shift+P hotkey path on a BLOCKS line opens the owner's Blocks stage directly
ok 1557 - Ctrl+Shift+P hotkey path on a BLOCKS line opens the owner's Blocks stage directly
  ---
  duration_ms: 3.756181
  ...
# Subtest: Ctrl+Shift+Alt+B on a BLOCKS or Depends-On line opens the owner's Blocks stage
ok 1558 - Ctrl+Shift+Alt+B on a BLOCKS or Depends-On line opens the owner's Blocks stage
  ---
  duration_ms: 0.736727
  ...
# Subtest: Ctrl+Shift+P on a Depends-On line is unchanged forward behavior
ok 1559 - Ctrl+Shift+P on a Depends-On line is unchanged forward behavior
  ---
  duration_ms: 0.467813
  ...
# Subtest: Ctrl+Shift+P on a plain child bullet and a nested Task Link are unchanged (3e359a6)
ok 1560 - Ctrl+Shift+P on a plain child bullet and a nested Task Link are unchanged (3e359a6)
  ---
  duration_ms: 13.243679
  ...
# Subtest: forward counted mixed row in BLOCKED keeps the waits-on badge (3e359a6 order)
ok 1561 - forward counted mixed row in BLOCKED keeps the waits-on badge (3e359a6 order)
  ---
  duration_ms: 4.233732
  ...
# Subtest: api.blocks opens the stage and removes only a listed dependent
ok 1562 - api.blocks opens the stage and removes only a listed dependent
  ---
  duration_ms: 3.90881
  ...
# Subtest: api.blocks removeDependent on an owner with no ^id is not-a-dependent
ok 1563 - api.blocks removeDependent on an owner with no ^id is not-a-dependent
  ---
  duration_ms: 0.606988
  ...
# Subtest: stage canonical order ranks \#hide last ahead of the lane
ok 1564 - stage canonical order ranks \#hide last ahead of the lane
  ---
  duration_ms: 0.508099
  ...
# Subtest: stage empty query shows same-note plus In Progress and Next only
ok 1565 - stage empty query shows same-note plus In Progress and Next only
  ---
  duration_ms: 4.723365
  ...
# Subtest: stage cap appends a type-to-search-more hint row
ok 1566 - stage cap appends a type-to-search-more hint row
  ---
  duration_ms: 8.251782
  ...
# Subtest: stage BLOCKED rows carry waits-on counts and short guard reasons
ok 1567 - stage BLOCKED rows carry waits-on counts and short guard reasons
  ---
  duration_ms: 2.756191
  ...
# Subtest: stage removal notices name the task description, not the block id
ok 1568 - stage removal notices name the task description, not the block id
  ---
  duration_ms: 1.46158
  ...
# Subtest: stage Task Link batches keep Depends on without refusal
ok 1569 - stage Task Link batches keep Depends on without refusal
  ---
  duration_ms: 0.955123
  ...
# Subtest: stage batch cycle check runs on the post-batch graph
ok 1570 - stage batch cycle check runs on the post-batch graph
  ---
  duration_ms: 1.009416
  ...
# Subtest: stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
ok 1571 - stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
  ---
  duration_ms: 80.62574
  ...
# Subtest: stage stale single add refuses and reopens
ok 1572 - stage stale single add refuses and reopens
  ---
  duration_ms: 2.725332
  ...
# Subtest: Task Link Depends on focuses a linked note open in a background tab
ok 1573 - Task Link Depends on focuses a linked note open in a background tab
  ---
  duration_ms: 0.972496
  ...
# Subtest: Task Link Blocks focuses the linked note and opens Blocks directly
ok 1574 - Task Link Blocks focuses the linked note and opens Blocks directly
  ---
  duration_ms: 0.787022
  ...
# Subtest: Task Link Depends on refuses clearly when the linked note cannot be focused
    # Subtest: focus reports success but the active view stays elsewhere
    ok 1 - focus reports success but the active view stays elsewhere
      ---
      duration_ms: 0.422767
      ...
    # Subtest: focus reports failure
    ok 2 - focus reports failure
      ---
      duration_ms: 0.315702
      ...
    1..2
ok 1575 - Task Link Depends on refuses clearly when the linked note cannot be focused
  ---
  duration_ms: 1.371378
  ...
# Subtest: stage mirror burst keeps the baseline owner across an insertion above
ok 1576 - stage mirror burst keeps the baseline owner across an insertion above
  ---
  duration_ms: 1010.752274
  ...
# Subtest: stage mirror burst clears on a text-only line deletion
ok 1577 - stage mirror burst clears on a text-only line deletion
  ---
  duration_ms: 1001.840474
  ...
# Subtest: stage mirror vim dd clears the deleted line's owner
ok 1578 - stage mirror vim dd clears the deleted line's owner
  ---
  duration_ms: 1003.827498
  ...
# Subtest: stage badge counts open prerequisites without a block id
ok 1579 - stage badge counts open prerequisites without a block id
  ---
  duration_ms: 7.318249
  ...
# Subtest: stage badge names the future scheduled date with no open prerequisite
ok 1580 - stage badge names the future scheduled date with no open prerequisite
  ---
  duration_ms: 1.848008
  ...
# Subtest: stage badge reads blocked with nothing waiting and no schedule
ok 1581 - stage badge reads blocked with nothing waiting and no schedule
  ---
  duration_ms: 0.673706
  ...
# Subtest: stage vault batch with a stale row refuses and reopens
ok 1582 - stage vault batch with a stale row refuses and reopens
  ---
  duration_ms: 9.118155
  ...
# Subtest: stage opening builds 200/400/1000-task notes without cubic growth
ok 1583 - stage opening builds 200/400/1000-task notes without cubic growth
  ---
  duration_ms: 62.893051
  ...
# Subtest: stage snapshots match standalone parsing across grammar vectors
ok 1584 - stage snapshots match standalone parsing across grammar vectors
  ---
  duration_ms: 7.923034
  ...
# Subtest: stage Warm-empty cache is ready without a vault fallback
ok 1585 - stage Warm-empty cache is ready without a vault fallback
  ---
  duration_ms: 0.700678
  ...
# Subtest: stage opening renders cross-note results with zero writes and cap
ok 1586 - stage opening renders cross-note results with zero writes and cap
  ---
  duration_ms: 50.292127
  ...
# Subtest: stage CURRENT covers same-note, cross-note, blocked, and counted parents
ok 1587 - stage CURRENT covers same-note, cross-note, blocked, and counted parents
  ---
  duration_ms: 2.857975
  ...
# Subtest: stage collections reuse one snapshot per parent
ok 1588 - stage collections reuse one snapshot per parent
  ---
  duration_ms: 0.834102
  ...
# Subtest: stage cold refresh yields, preserves state, and performs no search reads
ok 1589 - stage cold refresh yields, preserves state, and performs no search reads
  ---
  duration_ms: 148.762219
  ...
# Subtest: stage cold refresh abandons after dismissal or replacement
ok 1590 - stage cold refresh abandons after dismissal or replacement
  ---
  duration_ms: 75.695378
  ...
# Subtest: stage 400-task opening finishes in a child process before the parent timeout
ok 1591 - stage 400-task opening finishes in a child process before the parent timeout
  ---
  duration_ms: 285.855775
  ...
# Subtest: stage ranker passes the DK contract vectors verbatim
ok 1592 - stage ranker passes the DK contract vectors verbatim
  ---
  duration_ms: 4.925972
  ...
# Subtest: stage ranker tiers match the capture ranker tier order
ok 1593 - stage ranker tiers match the capture ranker tier order
  ---
  duration_ms: 0.451662
  ...
# Subtest: stage pool excludes daily notes, done, templates, and dot-dirs
ok 1594 - stage pool excludes daily notes, done, templates, and dot-dirs
  ---
  duration_ms: 0.661633
  ...
# Subtest: stage pool collects open vault tasks with buffers as given
ok 1595 - stage pool collects open vault tasks with buffers as given
  ---
  duration_ms: 3.553943
  ...
# Subtest: stage CURRENT resolves same-note, missing, closed, and non-task targets
ok 1596 - stage CURRENT resolves same-note, missing, closed, and non-task targets
  ---
  duration_ms: 3.925023
  ...
# Subtest: stage cycle guard reports the path back to the dependent
ok 1597 - stage cycle guard reports the path back to the dependent
  ---
  duration_ms: 1.945814
  ...
# Subtest: stage view groups CURRENT, RESULTS, and BLOCKED with guards
ok 1598 - stage view groups CURRENT, RESULTS, and BLOCKED with guards
  ---
  duration_ms: 5.105956
  ...
# Subtest: stage view disables cycles and unencodable targets, keeps +id rows
ok 1599 - stage view disables cycles and unencodable targets, keeps +id rows
  ---
  duration_ms: 3.049871
  ...
# Subtest: stage cache tasks normalize across Tasks shapes, buffers win
ok 1600 - stage cache tasks normalize across Tasks shapes, buffers win
  ---
  duration_ms: 1.619551
  ...
# Subtest: stage Task Link mode shows Depends on for one link and batches
ok 1601 - stage Task Link mode shows Depends on for one link and batches
  ---
  duration_ms: 1.900257
  ...
# Subtest: stage mark keys never collide across notes
ok 1602 - stage mark keys never collide across notes
  ---
  duration_ms: 0.516226
  ...
# Subtest: stage display-text locating matches one open task
ok 1603 - stage display-text locating matches one open task
  ---
  duration_ms: 0.616176
  ...
# Subtest: stage selection refusal spans tasks only
ok 1604 - stage selection refusal spans tasks only
  ---
  duration_ms: 0.608272
  ...
# Subtest: stage builder composes pool, current, guards, and pill title
ok 1605 - stage builder composes pool, current, guards, and pill title
  ---
  duration_ms: 5.484879
  ...
# Subtest: stage counted vault add with a stale target refuses and reopens
ok 1606 - stage counted vault add with a stale target refuses and reopens
  ---
  duration_ms: 20.449613
  ...
# Subtest: stage vault commit with a stale write notifies once and reopens
ok 1607 - stage vault commit with a stale write notifies once and reopens
  ---
  duration_ms: 14.308352
  ...
# Subtest: commitVaultRefs refuses a cycle through implicit resident edges
ok 1608 - commitVaultRefs refuses a cycle through implicit resident edges
  ---
  duration_ms: 4.138129
  ...
# Subtest: stage single remove with a stale write notifies once and reopens
ok 1609 - stage single remove with a stale write notifies once and reopens
  ---
  duration_ms: 5.036814
  ...
# Subtest: stage vault single +id guard refuses a stale target
ok 1610 - stage vault single +id guard refuses a stale target
  ---
  duration_ms: 9.468643
  ...
# Subtest: stage vault counted +id guard refuses a stale target
ok 1611 - stage vault counted +id guard refuses a stale target
  ---
  duration_ms: 2.002914
  ...
# Subtest: stage single +id guard refuses a stale target
ok 1612 - stage single +id guard refuses a stale target
  ---
  duration_ms: 1.58195
  ...
# Subtest: stage counted remove with a stale write refuses and reopens
ok 1613 - stage counted remove with a stale write refuses and reopens
  ---
  duration_ms: 4.896947
  ...
# Subtest: stage counted remove counts only changed sources
ok 1614 - stage counted remove counts only changed sources
  ---
  duration_ms: 7.552888
  ...
# Subtest: counted local add on [?] sources reads zero extra notes
ok 1615 - counted local add on [?] sources reads zero extra notes
  ---
  duration_ms: 9.428466
  ...
# Subtest: counted local toggle-off on a Pomodoro-linked [?] source recovers
ok 1616 - counted local toggle-off on a Pomodoro-linked [?] source recovers
  ---
  duration_ms: 9.689286
  ...
# Subtest: stage counted vault add counts only changed sources
ok 1617 - stage counted vault add counts only changed sources
  ---
  duration_ms: 10.202173
  ...
# Subtest: stage counted vault remove counts only changed sources
ok 1618 - stage counted vault remove counts only changed sources
  ---
  duration_ms: 4.061583
  ...
# Subtest: vault counted same-note add follows BLOCKS shifts with post-plan stamps
ok 1619 - vault counted same-note add follows BLOCKS shifts with post-plan stamps
  ---
  duration_ms: 3.93981
  ...
# Subtest: vault counted same-note remove follows BLOCKS deletions
ok 1620 - vault counted same-note remove follows BLOCKS deletions
  ---
  duration_ms: 7.458348
  ...
# Subtest: vault counted cross-note add keeps follow-up behavior
ok 1621 - vault counted cross-note add keeps follow-up behavior
  ---
  duration_ms: 5.494958
  ...
# Subtest: stage +id row prompts without writing
ok 1622 - stage +id row prompts without writing
  ---
  duration_ms: 17.166147
  ...
# Subtest: stage dismissal writes no bytes and drops the batch
ok 1623 - stage dismissal writes no bytes and drops the batch
  ---
  duration_ms: 2.458654
  ...
# Subtest: stage same-note batch commits in one undo group
ok 1624 - stage same-note batch commits in one undo group
  ---
  duration_ms: 20.906285
  ...
# Subtest: stage batch with a stale row refuses and reopens
ok 1625 - stage batch with a stale row refuses and reopens
  ---
  duration_ms: 1.822408
  ...
# Subtest: stage counted add applies to every source task
ok 1626 - stage counted add applies to every source task
  ---
  duration_ms: 42.819054
  ...
# Subtest: stage batch cycle rows stay guarded and write nothing
ok 1627 - stage batch cycle rows stay guarded and write nothing
  ---
  duration_ms: 30.996667
  ...
# Subtest: stage edit-task-dependencies registers with no default hotkey
ok 1628 - stage edit-task-dependencies registers with no default hotkey
  ---
  duration_ms: 3.424207
  ...
# Subtest: task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row
ok 1629 - task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row
  ---
  duration_ms: 3.063228
  ...
# Subtest: task-card-blocks registers Ctrl+Shift+Alt+B and opens the Blocks row
ok 1630 - task-card-blocks registers Ctrl+Shift+Alt+B and opens the Blocks row
  ---
  duration_ms: 0.863167
  ...
# Subtest: stage waits-on badge counts open prerequisites only
ok 1631 - stage waits-on badge counts open prerequisites only
  ---
  duration_ms: 2.711115
  ...
# Subtest: stage cycle tooltip shows task descriptions
ok 1632 - stage cycle tooltip shows task descriptions
  ---
  duration_ms: 2.578912
  ...
# Subtest: stage same-note single add stamps the dependent and keeps its cursor
ok 1633 - stage same-note single add stamps the dependent and keeps its cursor
  ---
  duration_ms: 10.211403
  ...
# Subtest: stage same-note marked batch stamps the dependent and keeps its cursor
ok 1634 - stage same-note marked batch stamps the dependent and keeps its cursor
  ---
  duration_ms: 7.858078
  ...
# Subtest: Tab marks a same-note CURRENT row and Enter removes it
ok 1635 - Tab marks a same-note CURRENT row and Enter removes it
  ---
  duration_ms: 44.012642
  ...
# Subtest: Tab twice unmarks a CURRENT row
ok 1636 - Tab twice unmarks a CURRENT row
  ---
  duration_ms: 33.216284
  ...
# Subtest: Tab mixed CURRENT removal and RESULTS add apply in one commit
ok 1637 - Tab mixed CURRENT removal and RESULTS add apply in one commit
  ---
  duration_ms: 38.875786
  ...
# Subtest: Tab marks a missing CURRENT target and the batch removes it
ok 1638 - Tab marks a missing CURRENT target and the batch removes it
  ---
  duration_ms: 46.912807
  ...
# Subtest: Tab same-note and cross-note CURRENT removals apply in one vault batch
ok 1639 - Tab same-note and cross-note CURRENT removals apply in one vault batch
  ---
  duration_ms: 46.727745
  ...
# Subtest: cross-note add awaits preparation before the one commit
ok 1640 - cross-note add awaits preparation before the one commit
  ---
  duration_ms: 51.793723
  ...
# Subtest: a failed async preparation leaves the dependent untouched
ok 1641 - a failed async preparation leaves the dependent untouched
  ---
  duration_ms: 8.268594
  ...
# Subtest: links to unloaded notes tolerate add, remove, and deleted targets
ok 1642 - links to unloaded notes tolerate add, remove, and deleted targets
  ---
  duration_ms: 8.017493
  ...
# Subtest: Pomodoro-linked dependents recover through the plugin vault read
ok 1643 - Pomodoro-linked dependents recover through the plugin vault read
  ---
  duration_ms: 10.476258
  ...
# Subtest: same-note batch +id stamps the target and links in one undo group
ok 1644 - same-note batch +id stamps the target and links in one undo group
  ---
  duration_ms: 17.624061
  ...
# Subtest: confirmBatchBlockId collects the id and executes the batch
ok 1645 - confirmBatchBlockId collects the id and executes the batch
  ---
  duration_ms: 11.942727
  ...
# Subtest: commitMarkedDependencies executes ready additions at once
ok 1646 - commitMarkedDependencies executes ready additions at once
  ---
  duration_ms: 4.610972
  ...
# Subtest: counted vault add links two siblings bottom-up
ok 1647 - counted vault add links two siblings bottom-up
  ---
  duration_ms: 9.206855
  ...
# Subtest: counted CURRENT rows without a line remove from every source
ok 1648 - counted CURRENT rows without a line remove from every source
  ---
  duration_ms: 12.242829
  ...
# Subtest: a stale editor between await and commit refuses
ok 1649 - a stale editor between await and commit refuses
  ---
  duration_ms: 2.643576
  ...
# Subtest: removeDependencyByRef refuses targets that are not on the line
ok 1650 - removeDependencyByRef refuses targets that are not on the line
  ---
  duration_ms: 8.747127
  ...
# Subtest: kept unloaded links resolve the field id by line position
ok 1651 - kept unloaded links resolve the field id by line position
  ---
  duration_ms: 6.031332
  ...
# Subtest: pendingTargetLine commits the same-note target id with the link
ok 1652 - pendingTargetLine commits the same-note target id with the link
  ---
  duration_ms: 6.350793
  ...
# Subtest: counted vault add commits every source in one transaction
ok 1653 - counted vault add commits every source in one transaction
  ---
  duration_ms: 11.430407
  ...
# Subtest: field-only clears snapshot the vault and recover
ok 1654 - field-only clears snapshot the vault and recover
  ---
  duration_ms: 4.276935
  ...
# Subtest: adds without recovery read zero extra vault notes
ok 1655 - adds without recovery read zero extra vault notes
  ---
  duration_ms: 4.753804
  ...
# Subtest: hand-edit clear recovers Pomodoro-linked dependents to Next
ok 1656 - hand-edit clear recovers Pomodoro-linked dependents to Next
  ---
  duration_ms: 3.24325
  ...
# Subtest: hand-edit clear on a non-Blocked parent reads zero extra notes
ok 1657 - hand-edit clear on a non-Blocked parent reads zero extra notes
  ---
  duration_ms: 1.285724
  ...
# Subtest: writer keeps the full route for duplicate basenames
ok 1658 - writer keeps the full route for duplicate basenames
  ---
  duration_ms: 4.178386
  ...
# Subtest: adds on Blocked parents and non-Blocked mirror touches read nothing
ok 1659 - adds on Blocked parents and non-Blocked mirror touches read nothing
  ---
  duration_ms: 3.160724
  ...
# Subtest: counted vault add loads each source's existing links
ok 1660 - counted vault add loads each source's existing links
  ---
  duration_ms: 7.488253
  ...
# Subtest: counted Ctrl+D on a blockquoted task refuses with the blockquote notice
ok 1661 - counted Ctrl+D on a blockquoted task refuses with the blockquote notice
  ---
  duration_ms: 1.479935
  ...
# Subtest: single Ctrl+D on a quoted task without a field refuses as a blockquote
ok 1662 - single Ctrl+D on a quoted task without a field refuses as a blockquote
  ---
  duration_ms: 0.505846
  ...
# Subtest: confirmSingleBlockId folds the target id into one transaction
ok 1663 - confirmSingleBlockId folds the target id into one transaction
  ---
  duration_ms: 14.44859
  ...
# Subtest: chooseTaskDependency folds a missing target id into one transaction
ok 1664 - chooseTaskDependency folds a missing target id into one transaction
  ---
  duration_ms: 6.276822
  ...
# Subtest: counted remove commits every source in one transaction
ok 1665 - counted remove commits every source in one transaction
  ---
  duration_ms: 10.264453
  ...
# Subtest: DP parse vectors accept, empty, malformed, and not-a-line
ok 1666 - DP parse vectors accept, empty, malformed, and not-a-line
  ---
  duration_ms: 5.619065
  ...
# Subtest: DP30 attributes a Work-Log-nested Depends-On line to the inner task
ok 1667 - DP30 attributes a Work-Log-nested Depends-On line to the inner task
  ---
  duration_ms: 5.449823
  ...
# Subtest: fenced lines never collect as Depends-On lines
ok 1668 - fenced lines never collect as Depends-On lines
  ---
  duration_ms: 0.563866
  ...
# Subtest: DW1 creates the line as the first child
ok 1669 - DW1 creates the line as the first child
  ---
  duration_ms: 9.999949
  ...
# Subtest: DW2 creates the line after a Cancel Log
ok 1670 - DW2 creates the line after a Cancel Log
  ---
  duration_ms: 1.955843
  ...
# Subtest: DW3-DW5 append, remove the middle, and delete on the last link
ok 1671 - DW3-DW5 append, remove the middle, and delete on the last link
  ---
  duration_ms: 7.803836
  ...
# Subtest: DW6-DW7 re-add moves to the end and the field mirrors the line
ok 1672 - DW6-DW7 re-add moves to the end and the field mirrors the line
  ---
  duration_ms: 1.004468
  ...
# Subtest: DW8 tab parents deepen the child by one tab
ok 1673 - DW8 tab parents deepen the child by one tab
  ---
  duration_ms: 5.426629
  ...
# Subtest: DW9 space parents reuse the existing child indent
ok 1674 - DW9 space parents reuse the existing child indent
  ---
  duration_ms: 2.364103
  ...
# Subtest: DW10-DW11 CRLF and final-newline state survive
ok 1675 - DW10-DW11 CRLF and final-newline state survive
  ---
  duration_ms: 1.863457
  ...
# Subtest: DW12-DW14 link form is the shortest unambiguous form
ok 1676 - DW12-DW14 link form is the shortest unambiguous form
  ---
  duration_ms: 0.659939
  ...
# Subtest: archive targets keep the explicit done/ path form
ok 1677 - archive targets keep the explicit done/ path form
  ---
  duration_ms: 0.279684
  ...
# Subtest: DW15 an existing id is never rewritten
ok 1678 - DW15 an existing id is never rewritten
  ---
  duration_ms: 0.811799
  ...
# Subtest: DW16 an unencodable path without an id refuses
ok 1679 - DW16 an unencodable path without an id refuses
  ---
  duration_ms: 0.672042
  ...
# Subtest: DW17 field placement follows fresh and precedes the block id
ok 1680 - DW17 field placement follows fresh and precedes the block id
  ---
  duration_ms: 0.802712
  ...
# Subtest: DW18 legacy children fold into the line
ok 1681 - DW18 legacy children fold into the line
  ---
  duration_ms: 1.725083
  ...
# Subtest: DW19 variants canonicalise to the writer form
ok 1682 - DW19 variants canonicalise to the writer form
  ---
  duration_ms: 3.951042
  ...
# Subtest: adding an open prerequisite blocks the dependent
ok 1683 - adding an open prerequisite blocks the dependent
  ---
  duration_ms: 1.253853
  ...
# Subtest: adding transfers Next and In Progress commitment to the open target
ok 1684 - adding transfers Next and In Progress commitment to the open target
  ---
  duration_ms: 1.192145
  ...
# Subtest: removing the last open prerequisite recovers immediately
ok 1685 - removing the last open prerequisite recovers immediately
  ---
  duration_ms: 1.788633
  ...
# Subtest: removal stays Blocked while another prerequisite is open
ok 1686 - removal stays Blocked while another prerequisite is open
  ---
  duration_ms: 1.419009
  ...
# Subtest: removal stays Blocked with a future schedule
ok 1687 - removal stays Blocked with a future schedule
  ---
  duration_ms: 0.828852
  ...
# Subtest: one gesture commits the dependent note in a single transaction
ok 1688 - one gesture commits the dependent note in a single transaction
  ---
  duration_ms: 3.78198
  ...
# Subtest: a failed preparation leaves the dependent untouched
ok 1689 - a failed preparation leaves the dependent untouched
  ---
  duration_ms: 1.900618
  ...
# Subtest: recovery references follow the line plus covered legacy children
ok 1690 - recovery references follow the line plus covered legacy children
  ---
  duration_ms: 1.541703
  ...
# Subtest: task-block helpers find owners, lines, and insertion points
ok 1691 - task-block helpers find owners, lines, and insertion points
  ---
  duration_ms: 0.719383
  ...
# Subtest: dependency notices follow the contract shapes
ok 1692 - dependency notices follow the contract shapes
  ---
  duration_ms: 0.331694
  ...
# Subtest: nav api v3 resolves results and never throws
ok 1693 - nav api v3 resolves results and never throws
  ---
  duration_ms: 7.119569
  ...
# Subtest: getDependencyInsertLine lands after a Cancel Log subtree
ok 1694 - getDependencyInsertLine lands after a Cancel Log subtree
  ---
  duration_ms: 0.791421
  ...
# Subtest: planner: an ordinary dependent with a block id plus an open add yields one target
ok 1695 - planner: an ordinary dependent with a block id plus an open add yields one target
  ---
  duration_ms: 13.653252
  ...
# Subtest: planner: adding only a closed target yields none
ok 1696 - planner: adding only a closed target yields none
  ---
  duration_ms: 1.652954
  ...
# Subtest: planner: no block id yields none
ok 1697 - planner: no block id yields none
  ---
  duration_ms: 0.847638
  ...
# Subtest: planner: a dependent already [?] with an open add yields a target
ok 1698 - planner: a dependent already [?] with an open add yields a target
  ---
  duration_ms: 3.399979
  ...
# Subtest: planner: a removal yields none
ok 1699 - planner: a removal yields none
  ---
  duration_ms: 1.900909
  ...
# Subtest: planner: mirrorTouch emits no ordinary consumption target
ok 1700 - planner: mirrorTouch emits no ordinary consumption target
  ---
  duration_ms: 0.653156
  ...
# Subtest: planner: ^prj keeps project targets and a deduplicated union
ok 1701 - planner: ^prj keeps project targets and a deduplicated union
  ---
  duration_ms: 3.300129
  ...
# Subtest: suffix helper names the removed count and the failed follow-up
ok 1702 - suffix helper names the removed count and the failed follow-up
  ---
  duration_ms: 0.268593
  ...
# Subtest: applyDependencyEdit cross-file consumes live links and emptied entries
ok 1703 - applyDependencyEdit cross-file consumes live links and emptied entries
  ---
  duration_ms: 22.49547
  ...
# Subtest: applyDependencyEdit removes one live link and reports it
ok 1704 - applyDependencyEdit removes one live link and reports it
  ---
  duration_ms: 4.911685
  ...
# Subtest: applyDependencyEdit keeps the dependent write when the daily preimage changes
ok 1705 - applyDependencyEdit keeps the dependent write when the daily preimage changes
  ---
  duration_ms: 12.706563
  ...
# Subtest: same-file fold lands the dependency and the cleanup in one undo group
ok 1706 - same-file fold lands the dependency and the cleanup in one undo group
  ---
  duration_ms: 3.528746
  ...
# Subtest: setLocalTaskDependencyLink stays synchronous and folds same-file cleanup
ok 1707 - setLocalTaskDependencyLink stays synchronous and folds same-file cleanup
  ---
  duration_ms: 4.957823
  ...
# Subtest: setLocalTaskDependencyLink cross-file continuation removes the live link
ok 1708 - setLocalTaskDependencyLink cross-file continuation removes the live link
  ---
  duration_ms: 27.686088
  ...
# Subtest: same-note marked batch consumes every newly Blocked source
ok 1709 - same-note marked batch consumes every newly Blocked source
  ---
  duration_ms: 18.645341
  ...
# Subtest: counted same-note writer consumes every newly Blocked source
ok 1710 - counted same-note writer consumes every newly Blocked source
  ---
  duration_ms: 11.038141
  ...
# Subtest: counted vault writer consumes every newly Blocked source
ok 1711 - counted vault writer consumes every newly Blocked source
  ---
  duration_ms: 8.636204
  ...
# Subtest: counted ^prj source consumes its project targets
ok 1712 - counted ^prj source consumes its project targets
  ---
  duration_ms: 12.78264
  ...
# Subtest: a dependent without a block id does zero cachedReads even when today's daily exists
ok 1713 - a dependent without a block id does zero cachedReads even when today's daily exists
  ---
  duration_ms: 8.0048
  ...
# Subtest: alignment key ignores fields, the block id, the status and trailing space
ok 1714 - alignment key ignores fields, the block id, the status and trailing space
  ---
  duration_ms: 3.493239
  ...
# Subtest: insertion after a modified line edits that line and inserts after it
ok 1715 - insertion after a modified line edits that line and inserts after it
  ---
  duration_ms: 4.041585
  ...
# Subtest: adjacent prerequisite and parent both change while two lines insert
ok 1716 - adjacent prerequisite and parent both change while two lines insert
  ---
  duration_ms: 0.734882
  ...
# Subtest: deletion at the end of the document
ok 1717 - deletion at the end of the document
  ---
  duration_ms: 0.829123
  ...
# Subtest: insertion at the top and at the end of the document
ok 1718 - insertion at the top and at the end of the document
  ---
  duration_ms: 0.939273
  ...
# Subtest: empty documents align and apply
ok 1719 - empty documents align and apply
  ---
  duration_ms: 0.631496
  ...
# Subtest: CRLF documents insert and delete with CRLF
ok 1720 - CRLF documents insert and delete with CRLF
  ---
  duration_ms: 0.486388
  ...
# Subtest: equal-count shifted edits take the aligned path
ok 1721 - equal-count shifted edits take the aligned path
  ---
  duration_ms: 1.196263
  ...
# Subtest: pure in-place edits keep the line-bounded change shapes
ok 1722 - pure in-place edits keep the line-bounded change shapes
  ---
  duration_ms: 1.187968
  ...
# Subtest: an unchanged document writes nothing
ok 1723 - an unchanged document writes nothing
  ---
  duration_ms: 0.410523
  ...
# Subtest: an explicit final cursor wins over the mapped cursor
ok 1724 - an explicit final cursor wins over the mapped cursor
  ---
  duration_ms: 0.420853
  ...
# Subtest: the machine-write annotation still reaches the transaction
ok 1725 - the machine-write annotation still reaches the transaction
  ---
  duration_ms: 0.348224
  ...
# Subtest: an editor without transaction falls back to bottom-up replaceRange
ok 1726 - an editor without transaction falls back to bottom-up replaceRange
  ---
  duration_ms: 0.856695
  ...
# Subtest: positions map through aligned, changed, gap and deleted lines
ok 1727 - positions map through aligned, changed, gap and deleted lines
  ---
  duration_ms: 0.595978
  ...
# Subtest: a deletion at the end of the document maps to the last line
ok 1728 - a deletion at the end of the document maps to the last line
  ---
  duration_ms: 0.27235
  ...
# Subtest: a gap with new lines maps by offset and clamps to its last line
ok 1729 - a gap with new lines maps by offset and clamps to its last line
  ---
  duration_ms: 0.579546
  ...
# Subtest: seeded property: planned changes rebuild the new text and map unchanged lines
ok 1730 - seeded property: planned changes rebuild the new text and map unchanged lines
  ---
  duration_ms: 97.518445
  ...
# Subtest: a diff past the edit cap becomes one unaligned gap
ok 1731 - a diff past the edit cap becomes one unaligned gap
  ---
  duration_ms: 145.535329
  ...
# Subtest: the CM6 double reproduces the whole-document replacement jump
ok 1732 - the CM6 double reproduces the whole-document replacement jump
  ---
  duration_ms: 0.999548
  ...
# Subtest: first cross-note prerequisite keeps the cursor and the viewport
ok 1733 - first cross-note prerequisite keeps the cursor and the viewport
  ---
  duration_ms: 16.084793
  ...
# Subtest: same-note prerequisite directly above keeps the dependent's line
ok 1734 - same-note prerequisite directly above keeps the dependent's line
  ---
  duration_ms: 6.67453
  ...
# Subtest: removing the last prerequisite keeps the dependent's line
ok 1735 - removing the last prerequisite keeps the dependent's line
  ---
  duration_ms: 7.312739
  ...
# Subtest: a Blocks source gaining its first BLOCKS line keeps its line
ok 1736 - a Blocks source gaining its first BLOCKS line keeps its line
  ---
  duration_ms: 0.641945
  ...
# Subtest: missing ledger-tools api refuses the review namespace
ok 1737 - missing ledger-tools api refuses the review namespace
  ---
  duration_ms: 2.662662
  ...
# Subtest: review jump on an empty queue
ok 1738 - review jump on an empty queue
  ---
  duration_ms: 3.763375
  ...
# Subtest: review jump from a queued task goes to the neighbor
ok 1739 - review jump from a queued task goes to the neighbor
  ---
  duration_ms: 2.211101
  ...
# Subtest: review jump wraps at the ends
ok 1740 - review jump wraps at the ends
  ---
  duration_ms: 2.614981
  ...
# Subtest: review jump from elsewhere goes to the first or last entry
ok 1741 - review jump from elsewhere goes to the first or last entry
  ---
  duration_ms: 0.384594
  ...
# Subtest: review jump matches a moved cursor task by text
ok 1742 - review jump matches a moved cursor task by text
  ---
  duration_ms: 0.279944
  ...
# Subtest: review jump from a just-stamped rank goes to the entry after it
ok 1743 - review jump from a just-stamped rank goes to the entry after it
  ---
  duration_ms: 0.345139
  ...
# Subtest: review jump skips just-stamped keys the lagging cache still shows
ok 1744 - review jump skips just-stamped keys the lagging cache still shows
  ---
  duration_ms: 0.344939
  ...
# Subtest: review jump after stamping everything reports empty or wraps
ok 1745 - review jump after stamping everything reports empty or wraps
  ---
  duration_ms: 0.437706
  ...
# Subtest: review queue line resolves at the entry line
ok 1746 - review queue line resolves at the entry line
  ---
  duration_ms: 0.767414
  ...
# Subtest: review queue line follows a moved line to its unique match
ok 1747 - review queue line follows a moved line to its unique match
  ---
  duration_ms: 0.624682
  ...
# Subtest: review queue line goes stale on duplicates or a missing line
ok 1748 - review queue line goes stale on duplicates or a missing line
  ---
  duration_ms: 0.360979
  ...
# Subtest: review jump notices name the state
ok 1749 - review jump notices name the state
  ---
  duration_ms: 0.954391
  ...
# Subtest: fresh stamp targets refuse closed and recurring tasks
ok 1750 - fresh stamp targets refuse closed and recurring tasks
  ---
  duration_ms: 1.119627
  ...
# Subtest: fresh stamp batch stamps every target and nothing else
ok 1751 - fresh stamp batch stamps every target and nothing else
  ---
  duration_ms: 0.66516
  ...
# Subtest: one refusal refuses the whole fresh stamp batch
ok 1752 - one refusal refuses the whole fresh stamp batch
  ---
  duration_ms: 0.665661
  ...
# Subtest: a throwing stamper refuses the fresh stamp batch
ok 1753 - a throwing stamper refuses the fresh stamp batch
  ---
  duration_ms: 0.337444
  ...
# Subtest: fresh stamp plus Work Log prepends only stamped Pending targets
ok 1754 - fresh stamp plus Work Log prepends only stamped Pending targets
  ---
  duration_ms: 2.423897
  ...
# Subtest: blank Work Log summary and stamp refusal never create a log marker
ok 1755 - blank Work Log summary and stamp refusal never create a log marker
  ---
  duration_ms: 0.41933
  ...
# Subtest: fresh stamp notices adjust the pre-write counts
ok 1756 - fresh stamp notices adjust the pre-write counts
  ---
  duration_ms: 0.545521
  ...
# Subtest: today detection only matches today's fresh field
ok 1757 - today detection only matches today's fresh field
  ---
  duration_ms: 0.395575
  ...
# Subtest: stamped refs match the pre-write queue by line or text
ok 1758 - stamped refs match the pre-write queue by line or text
  ---
  duration_ms: 0.692982
  ...
# Subtest: review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
ok 1759 - review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
  ---
  duration_ms: 0.462884
  ...
# Subtest: tier-aware jump notices name each tier
ok 1760 - tier-aware jump notices name each tier
  ---
  duration_ms: 0.814846
  ...
# Subtest: projects tier walks with commitment rank and empty-project notice
ok 1761 - projects tier walks with commitment rank and empty-project notice
  ---
  duration_ms: 0.376829
  ...
# Subtest: references tier walks with commitment rank and reference notice
ok 1762 - references tier walks with commitment rank and reference notice
  ---
  duration_ms: 0.956055
  ...
# Subtest: jump notices use reviewEntryView when provided and keep the fallback
ok 1763 - jump notices use reviewEntryView when provided and keep the fallback
  ---
  duration_ms: 0.514973
  ...
# Subtest: tier notices fall back without tier ranks and wrap on the last line
ok 1764 - tier notices fall back without tier ranks and wrap on the last line
  ---
  duration_ms: 0.253453
  ...
# Subtest: boundary notice names commitments done and rotten next
ok 1765 - boundary notice names commitments done and rotten next
  ---
  duration_ms: 0.236812
  ...
# Subtest: walk anchor records handled keys with their neighbors
ok 1766 - walk anchor records handled keys with their neighbors
  ---
  duration_ms: 0.867226
  ...
# Subtest: cursor on a live entry wins over a lagging anchor
ok 1767 - cursor on a live entry wins over a lagging anchor
  ---
  duration_ms: 0.376759
  ...
# Subtest: [s after a stamp goes backwards from the anchor
ok 1768 - [s after a stamp goes backwards from the anchor
  ---
  duration_ms: 0.953971
  ...
# Subtest: release-then-]s continues from the anchor successor
ok 1769 - release-then-]s continues from the anchor successor
  ---
  duration_ms: 0.559969
  ...
# Subtest: non-contiguous counted stamp advances past the last handled rank
ok 1770 - non-contiguous counted stamp advances past the last handled rank
  ---
  duration_ms: 0.401406
  ...
# Subtest: anchor wraps at both ends
ok 1771 - anchor wraps at both ends
  ---
  duration_ms: 0.421144
  ...
# Subtest: advance across NEXT to TICKLER to ROTTEN lands the boundary
ok 1772 - advance across NEXT to TICKLER to ROTTEN lands the boundary
  ---
  duration_ms: 4.80863
  ...
# Subtest: tier capability gates on the freshness namespace version
ok 1773 - tier capability gates on the freshness namespace version
  ---
  duration_ms: 0.57642
  ...
# Subtest: empty queue notice reads the upkeep meter
ok 1774 - empty queue notice reads the upkeep meter
  ---
  duration_ms: 0.355097
  ...
# Subtest: refresh row reads lane intervals from the api with the once-Ready return
ok 1775 - refresh row reads lane intervals from the api with the once-Ready return
  ---
  duration_ms: 1.496847
  ...
# Subtest: endpoint jumps select the queue ends with full rank and total
ok 1776 - endpoint jumps select the queue ends with full rank and total
  ---
  duration_ms: 0.643238
  ...
# Subtest: endpoint jumps ignore cursor, anchor, and direction
ok 1777 - endpoint jumps ignore cursor, anchor, and direction
  ---
  duration_ms: 0.391467
  ...
# Subtest: endpoint jumps on empty and one-entry queues
ok 1778 - endpoint jumps on empty and one-entry queues
  ---
  duration_ms: 0.544449
  ...
# Subtest: a visited endpoint is still due under its own anchor
ok 1779 - a visited endpoint is still due under its own anchor
  ---
  duration_ms: 0.289874
  ...
# Subtest: lowercase steps continue from an endpoint anchor
ok 1780 - lowercase steps continue from an endpoint anchor
  ---
  duration_ms: 0.396127
  ...
# Subtest: counted review jump repeat 1 matches omitted repeat
ok 1781 - counted review jump repeat 1 matches omitted repeat
  ---
  duration_ms: 3.693871
  ...
# Subtest: counted review jump from the first entry lands N steps ahead
ok 1782 - counted review jump from the first entry lands N steps ahead
  ---
  duration_ms: 0.479836
  ...
# Subtest: counted review jump from the last entry wraps past the start
ok 1783 - counted review jump from the last entry wraps past the start
  ---
  duration_ms: 3.960811
  ...
# Subtest: counted review jump larger than the queue wraps once
ok 1784 - counted review jump larger than the queue wraps once
  ---
  duration_ms: 0.322817
  ...
# Subtest: counted review jump on a one-entry queue stays there
ok 1785 - counted review jump on a one-entry queue stays there
  ---
  duration_ms: 0.242012
  ...
# Subtest: counted review jump with no origin lands on the Nth entry
ok 1786 - counted review jump with no origin lands on the Nth entry
  ---
  duration_ms: 0.240889
  ...
# Subtest: counted review jump from a shaped anchor takes N surviving successors
ok 1787 - counted review jump from a shaped anchor takes N surviving successors
  ---
  duration_ms: 0.327125
  ...
# Subtest: counted review jump does not change endpoint selection
ok 1788 - counted review jump does not change endpoint selection
  ---
  duration_ms: 0.233776
  ...
# Subtest: a stamped endpoint that moved is stale and cannot land from old text
ok 1789 - a stamped endpoint that moved is stale and cannot land from old text
  ---
  duration_ms: 0.296316
  ...
# Subtest: stale endpoint target reselects the same endpoint in the new queue
ok 1790 - stale endpoint target reselects the same endpoint in the new queue
  ---
  duration_ms: 2.749808
  ...
# Subtest: endpoint retry is bounded and failures preserve the anchor
ok 1791 - endpoint retry is bounded and failures preserve the anchor
  ---
  duration_ms: 0.680198
  ...
# Subtest: endpoint jump to ROTTEN carries no boundary preamble
ok 1792 - endpoint jump to ROTTEN carries no boundary preamble
  ---
  duration_ms: 1.286075
  ...
# Subtest: endpoint notices keep v4 tier details and legacy v3 text
ok 1793 - endpoint notices keep v4 tier details and legacy v3 text
  ---
  duration_ms: 0.213849
  ...
# Subtest: onload registers first/last commands routed to the shared jump
ok 1794 - onload registers first/last commands routed to the shared jump
  ---
  duration_ms: 2.241278
  ...
# Subtest: jumpToDueTask consumes a pending Vim prefix as N review steps
ok 1795 - jumpToDueTask consumes a pending Vim prefix as N review steps
  ---
  duration_ms: 1.618198
  ...
# Subtest: registered next-due-task callback reads the pending Vim prefix
ok 1796 - registered next-due-task callback reads the pending Vim prefix
  ---
  duration_ms: 4.900505
  ...
# Subtest: explicit jumpToDueTask repeat skips the Vim prefix
ok 1797 - explicit jumpToDueTask repeat skips the Vim prefix
  ---
  duration_ms: 0.52918
  ...
# Subtest: non-normal editor with a pending prefix still jumps one entry
ok 1798 - non-normal editor with a pending prefix still jumps one entry
  ---
  duration_ms: 0.40871
  ...
# Subtest: stale counted replan reuses the captured repeat
ok 1799 - stale counted replan reuses the captured repeat
  ---
  duration_ms: 0.519311
  ...
# Subtest: endpoint jump with a pending prefix still lands on the endpoint
ok 1800 - endpoint jump with a pending prefix still lands on the endpoint
  ---
  duration_ms: 0.398411
  ...
# Subtest: counted forward landing on ROTTEN keeps the boundary preamble
ok 1801 - counted forward landing on ROTTEN keeps the boundary preamble
  ---
  duration_ms: 0.823221
  ...
# Subtest: PRE and POST are machine tiers; PRE is a commitment
ok 1802 - PRE and POST are machine tiers; PRE is a commitment
  ---
  duration_ms: 0.374394
  ...
# Subtest: fallback notices name PRE checklist and POST closeout
ok 1803 - fallback notices name PRE checklist and POST closeout
  ---
  duration_ms: 0.442474
  ...
# Subtest: text-first cursor matching does not skip Pills after an above-insert
ok 1804 - text-first cursor matching does not skip Pills after an above-insert
  ---
  duration_ms: 0.215141
  ...
# Subtest: day-scoped anchors from another day are ignored
ok 1805 - day-scoped anchors from another day are ignored
  ---
  duration_ms: 0.321984
  ...
# Subtest: boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
ok 1806 - boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
  ---
  duration_ms: 0.356501
  ...
# Subtest: ]S reaches POST with 77 ROTTEN rows and a null budget
ok 1807 - ]S reaches POST with 77 ROTTEN rows and a null budget
  ---
  duration_ms: 0.808523
  ...
# Subtest: nav normalizes a legacy v7 returned tier to tickler
ok 1808 - nav normalizes a legacy v7 returned tier to tickler
  ---
  duration_ms: 0.16252
  ...
# Subtest: RECURRING is a machine tier, a commitment, and a v9 capability
ok 1809 - RECURRING is a machine tier, a commitment, and a v9 capability
  ---
  duration_ms: 0.218197
  ...
# Subtest: RECURRING counts in reviewWalkRemaining and gates the boundary
ok 1810 - RECURRING counts in reviewWalkRemaining and gates the boundary
  ---
  duration_ms: 0.202647
  ...
# Subtest: matchReviewRecurringCursor is text-first like the checklist matcher
ok 1811 - matchReviewRecurringCursor is text-first like the checklist matcher
  ---
  duration_ms: 0.304131
  ...
# Subtest: fallback notices name RECURRING due detail with the reschedule hint
ok 1812 - fallback notices name RECURRING due detail with the reschedule hint
  ---
  duration_ms: 0.246721
  ...
# Subtest: Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
ok 1813 - Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
  ---
  duration_ms: 0.168642
  ...
# Subtest: bobLineDigest matches the shared bob-cli vectors
ok 1814 - bobLineDigest matches the shared bob-cli vectors
  ---
  duration_ms: 12.760978
  ...
# Subtest: parseGoToTaskParams accepts a complete v1 link and ignores extra keys
ok 1815 - parseGoToTaskParams accepts a complete v1 link and ignores extra keys
  ---
  duration_ms: 1.940845
  ...
# Subtest: parseGoToTaskParams treats ref and block as optional
ok 1816 - parseGoToTaskParams treats ref and block as optional
  ---
  duration_ms: 0.228286
  ...
# Subtest: parseGoToTaskParams rejects each malformed field
ok 1817 - parseGoToTaskParams rejects each malformed field
  ---
  duration_ms: 0.560019
  ...
# Subtest: vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
ok 1818 - vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
  ---
  duration_ms: 0.467181
  ...
# Subtest: refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
ok 1819 - refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
  ---
  duration_ms: 2.450448
  ...
# Subtest: handleGoToTaskUri notices each malformed parameter
ok 1820 - handleGoToTaskUri notices each malformed parameter
  ---
  duration_ms: 1.947959
  ...
# Subtest: handleGoToTaskUri notices a path outside the vault
ok 1821 - handleGoToTaskUri notices a path outside the vault
  ---
  duration_ms: 0.705978
  ...
# Subtest: handleGoToTaskUri notices a missing file inside the vault
ok 1822 - handleGoToTaskUri notices a missing file inside the vault
  ---
  duration_ms: 0.773948
  ...
# Subtest: handleGoToTaskUri maps a trailing-slash vault base
ok 1823 - handleGoToTaskUri maps a trailing-slash vault base
  ---
  duration_ms: 4.619519
  ...
# Subtest: handleGoToTaskUri prefers the open buffer over cachedRead
ok 1824 - handleGoToTaskUri prefers the open buffer over cachedRead
  ---
  duration_ms: 5.919519
  ...
# Subtest: handleGoToTaskUri re-finds by block id after an insert above the task
ok 1825 - handleGoToTaskUri re-finds by block id after an insert above the task
  ---
  duration_ms: 1.3937
  ...
# Subtest: handleGoToTaskUri re-finds a unique digest after a shift with no block
ok 1826 - handleGoToTaskUri re-finds a unique digest after a shift with no block
  ---
  duration_ms: 0.732398
  ...
# Subtest: handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
ok 1827 - handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
  ---
  duration_ms: 0.962057
  ...
# Subtest: handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
ok 1828 - handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
  ---
  duration_ms: 0.737518
  ...
# Subtest: handleGoToTaskUri reuses a leaf that already shows the note
ok 1829 - handleGoToTaskUri reuses a leaf that already shows the note
  ---
  duration_ms: 1.154434
  ...
# Subtest: handleGoToTaskUri switches a Reading-view leaf to editing
ok 1830 - handleGoToTaskUri switches a Reading-view leaf to editing
  ---
  duration_ms: 1.003907
  ...
# Subtest: handleGoToTaskUri records a jump from the prior cursor and none without one
ok 1831 - handleGoToTaskUri records a jump from the prior cursor and none without one
  ---
  duration_ms: 1.638748
  ...
# Subtest: handleGoToTaskUri never writes the vault or advances the walk
ok 1832 - handleGoToTaskUri never writes the vault or advances the walk
  ---
  duration_ms: 0.819164
  ...
# Subtest: handleGoToTaskUri reports when the note cannot be opened
ok 1833 - handleGoToTaskUri reports when the note cannot be opened
  ---
  duration_ms: 0.750292
  ...
# Subtest: focusTaskMoveDestination still lands without switching Reading view
ok 1834 - focusTaskMoveDestination still lands without switching Reading view
  ---
  duration_ms: 0.741125
  ...
# Subtest: onload registers both read-only navigation protocols when available
ok 1835 - onload registers both read-only navigation protocols when available
  ---
  duration_ms: 6.954243
  ...
# Subtest: onload skips protocol registration when the API is missing
ok 1836 - onload skips protocol registration when the API is missing
  ---
  duration_ms: 0.802622
  ...
# Subtest: registered protocol handler forwards params to handleGoToTaskUri
ok 1837 - registered protocol handler forwards params to handleGoToTaskUri
  ---
  duration_ms: 2.405331
  ...
# Subtest: handleGoToTaskUri maps a path through realpath when prefixes differ
ok 1838 - handleGoToTaskUri maps a path through realpath when prefixes differ
  ---
  duration_ms: 7.631848
  ...
# Subtest: cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
ok 1839 - cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
  ---
  duration_ms: 4.910302
  ...
# Subtest: findCancelLogParent finds a direct child but ignores a grandchild
ok 1840 - findCancelLogParent finds a direct child but ignores a grandchild
  ---
  duration_ms: 1.051276
  ...
# Subtest: getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
ok 1841 - getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
  ---
  duration_ms: 0.376419
  ...
# Subtest: formatCancelLogEntryText renders the exact preview text
ok 1842 - formatCancelLogEntryText renders the exact preview text
  ---
  duration_ms: 0.294322
  ...
# Subtest: planCancelLogEntry inserts a first-child log with tabs or spaces
ok 1843 - planCancelLogEntry inserts a first-child log with tabs or spaces
  ---
  duration_ms: 1.482821
  ...
# Subtest: planCancelLogEntry prepends under an existing log wherever it sits
ok 1844 - planCancelLogEntry prepends under an existing log wherever it sits
  ---
  duration_ms: 0.370107
  ...
# Subtest: planCancelLogEntry uses the fallback only when a marker exists
ok 1845 - planCancelLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.552305
  ...
# Subtest: isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
ok 1846 - isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
  ---
  duration_ms: 0.629712
  ...
# Subtest: describeCancelTaskRow covers single, counted, link, recurring, and hidden
ok 1847 - describeCancelTaskRow covers single, counted, link, recurring, and hidden
  ---
  duration_ms: 3.414497
  ...
# Subtest: planTaskCancelBatch cancels a single task with a first-child log
ok 1848 - planTaskCancelBatch cancels a single task with a first-child log
  ---
  duration_ms: 2.405972
  ...
# Subtest: planTaskCancelBatch upserts cancelled before the block id and preserves fields
ok 1849 - planTaskCancelBatch upserts cancelled before the block id and preserves fields
  ---
  duration_ms: 0.823582
  ...
# Subtest: planTaskCancelBatch records id-field task identities
ok 1850 - planTaskCancelBatch records id-field task identities
  ---
  duration_ms: 0.868348
  ...
# Subtest: planTaskCancelBatch skips closed targets and stays bottom-up
ok 1851 - planTaskCancelBatch skips closed targets and stays bottom-up
  ---
  duration_ms: 0.836407
  ...
# Subtest: planTaskCancelBatch refuses recurring targets in all three syntaxes
ok 1852 - planTaskCancelBatch refuses recurring targets in all three syntaxes
  ---
  duration_ms: 4.0441
  ...
# Subtest: planTaskCancelBatch handles empty reasons and stale preimages
ok 1853 - planTaskCancelBatch handles empty reasons and stale preimages
  ---
  duration_ms: 1.172047
  ...
# Subtest: planTaskCancelBatch preserves CRLF line endings
ok 1854 - planTaskCancelBatch preserves CRLF line endings
  ---
  duration_ms: 1.659127
  ...
# Subtest: cancel project conversion carries the log and reports it
ok 1855 - cancel project conversion carries the log and reports it
  ---
  duration_ms: 8.887554
  ...
# Subtest: getCancelTaskRowTitle names single, counted, and link sessions
ok 1856 - getCancelTaskRowTitle names single, counted, and link sessions
  ---
  duration_ms: 3.046444
  ...
# Subtest: getCancelReasonHints labels Enter per state and Esc as Keep open
ok 1857 - getCancelReasonHints labels Enter per state and Esc as Keep open
  ---
  duration_ms: 2.195701
  ...
# Subtest: the Cancel property item and the card's cancel row describe an open task
ok 1858 - the Cancel property item and the card's cancel row describe an open task
  ---
  duration_ms: 29.622986
  ...
# Subtest: Cancel row hides on closed tasks, plain bullets, and all-closed sessions
ok 1859 - Cancel row hides on closed tasks, plain bullets, and all-closed sessions
  ---
  duration_ms: 17.602841
  ...
# Subtest: Cancel row reports skipped closed targets in a counted session
ok 1860 - Cancel row reports skipped closed targets in a counted session
  ---
  duration_ms: 4.006227
  ...
# Subtest: the card refuses the cancel row on a recurring task and stays on the card
ok 1861 - the card refuses the cancel row on a recurring task and stays on the card
  ---
  duration_ms: 6.322678
  ...
# Subtest: cancel reason stage previews the typed, empty, fallback, and :: cases
ok 1862 - cancel reason stage previews the typed, empty, fallback, and :: cases
  ---
  duration_ms: 5.804841
  ...
# Subtest: cancel reason footer flips between plain, log, and fallback labels
ok 1863 - cancel reason footer flips between plain, log, and fallback labels
  ---
  duration_ms: 17.44031
  ...
# Subtest: Esc from the cancel reason stage writes nothing
ok 1864 - Esc from the cancel reason stage writes nothing
  ---
  duration_ms: 5.205887
  ...
# Subtest: single cancel writes [-], stamp, and first-child log in one transaction
ok 1865 - single cancel writes [-], stamp, and first-child log in one transaction
  ---
  duration_ms: 10.458413
  ...
# Subtest: empty reason writes no log unless one already exists
ok 1866 - empty reason writes no log unless one already exists
  ---
  duration_ms: 12.466938
  ...
# Subtest: stale single preimage refuses with nothing written
ok 1867 - stale single preimage refuses with nothing written
  ---
  duration_ms: 4.201429
  ...
# Subtest: cancel writes [-] with no NOW chip
ok 1868 - cancel writes [-] with no NOW chip
  ---
  duration_ms: 4.984654
  ...
# Subtest: TSC recovery runs with cancelled identities; a missing API still succeeds
ok 1869 - TSC recovery runs with cancelled identities; a missing API still succeeds
  ---
  duration_ms: 12.417372
  ...
# Subtest: a throwing TSC API is skipped silently with no chip
ok 1870 - a throwing TSC API is skipped silently with no chip
  ---
  duration_ms: 6.355112
  ...
# Subtest: counted cancel skips closed targets and reports them
ok 1871 - counted cancel skips closed targets and reports them
  ---
  duration_ms: 5.999431
  ...
# Subtest: same-file cancel folds today's Pomodoro prune into one transaction
ok 1872 - same-file cancel folds today's Pomodoro prune into one transaction
  ---
  duration_ms: 9.93819
  ...
# Subtest: link session cancels the target and removes the invoking link bullet
ok 1873 - link session cancels the target and removes the invoking link bullet
  ---
  duration_ms: 35.609411
  ...
# Subtest: buildCancelNoticeModel text covers every chip
ok 1874 - buildCancelNoticeModel text covers every chip
  ---
  duration_ms: 0.819554
  ...
# Subtest: renderCancelNoticeFragment builds the is-cancel card
ok 1875 - renderCancelNoticeFragment builds the is-cancel card
  ---
  duration_ms: 1.750993
  ...
# Subtest: Ctrl+0 loads and focuses a deferred pinned dash tab without jumping or restoring
ok 1876 - Ctrl+0 loads and focuses a deferred pinned dash tab without jumping or restoring
  ---
  duration_ms: 4.640739
  ...
# Subtest: Ctrl+0 from an unpinned dash copy switches to the pinned home tab
ok 1877 - Ctrl+0 from an unpinned dash copy switches to the pinned home tab
  ---
  duration_ms: 0.429039
  ...
# Subtest: Ctrl+0 stays on the pinned dash tab when an unpinned copy exists
ok 1878 - Ctrl+0 stays on the pinned dash tab when an unpinned copy exists
  ---
  duration_ms: 0.358505
  ...
# Subtest: Ctrl+0 keeps the active dash tab when equal-ranked copies exist
ok 1879 - Ctrl+0 keeps the active dash tab when equal-ranked copies exist
  ---
  duration_ms: 0.373453
  ...
# Subtest: a pinned dash tab wins over an earlier unpinned tab
ok 1880 - a pinned dash tab wins over an earlier unpinned tab
  ---
  duration_ms: 0.395615
  ...
# Subtest: a main-area dash tab wins over a pinned sidebar tab
ok 1881 - a main-area dash tab wins over a pinned sidebar tab
  ---
  duration_ms: 0.375447
  ...
# Subtest: a deferred sidebar dash tab is reused when there is no main-area match
ok 1882 - a deferred sidebar dash tab is reused when there is no main-area match
  ---
  duration_ms: 0.292448
  ...
# Subtest: a markdown saved state is considered even when the leaf is not deferred
ok 1883 - a markdown saved state is considered even when the leaf is not deferred
  ---
  duration_ms: 0.379374
  ...
# Subtest: Ctrl+0 opens dash in the current tab when no matching tab exists
ok 1884 - Ctrl+0 opens dash in the current tab when no matching tab exists
  ---
  duration_ms: 0.640202
  ...
# Subtest: Ctrl+0 leaves an already active dash tab alone
ok 1885 - Ctrl+0 leaves an already active dash tab alone
  ---
  duration_ms: 0.484094
  ...
# Subtest: isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
ok 1886 - isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
  ---
  duration_ms: 2.875098
  ...
# Subtest: findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
ok 1887 - findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
  ---
  duration_ms: 3.515911
  ...
# Subtest: collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
ok 1888 - collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
  ---
  duration_ms: 0.982295
  ...
# Subtest: planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
ok 1889 - planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
  ---
  duration_ms: 2.162157
  ...
# Subtest: planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
ok 1890 - planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
  ---
  duration_ms: 1.542104
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
ok 1891 - planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
  ---
  duration_ms: 1.851203
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
ok 1892 - planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
  ---
  duration_ms: 1.078419
  ...
# Subtest: planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
ok 1893 - planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
  ---
  duration_ms: 0.493862
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
ok 1894 - planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
  ---
  duration_ms: 0.835375
  ...
# Subtest: planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
ok 1895 - planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
  ---
  duration_ms: 0.784888
  ...
# Subtest: planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
ok 1896 - planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
  ---
  duration_ms: 1.289862
  ...
# Subtest: planDeferredPomodoroLinkCleanup preserves CRLF line endings
ok 1897 - planDeferredPomodoroLinkCleanup preserves CRLF line endings
  ---
  duration_ms: 0.471359
  ...
# Subtest: deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
ok 1898 - deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
  ---
  duration_ms: 0.764249
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks\#^x]] \#
ok 1899 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks\#^x]] \#
  ---
  duration_ms: 0.638038
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks\#^x|alias]] \#
ok 1900 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks\#^x|alias]] \#
  ---
  duration_ms: 6.227116
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks\#^x]]
ok 1901 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks\#^x]]
  ---
  duration_ms: 1.387578
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks\#^x]]
ok 1902 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks\#^x]]
  ---
  duration_ms: 0.580818
  ...
# Subtest: dedicated decoration check accepts paired strikes but cleanup never removes struck links
ok 1903 - dedicated decoration check accepts paired strikes but cleanup never removes struck links
  ---
  duration_ms: 0.914275
  ...
# Subtest: cleanup deletes only touched childless entries, preserving prose, placeholders and closed history
ok 1904 - cleanup deletes only touched childless entries, preserving prose, placeholders and closed history
  ---
  duration_ms: 0.672464
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\n", final newline false)
ok 1905 - cleanup handles adjacent EOF entries ("\\n", final newline false)
  ---
  duration_ms: 0.699245
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\n", final newline true)
ok 1906 - cleanup handles adjacent EOF entries ("\\n", final newline true)
  ---
  duration_ms: 0.255488
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\r\\n", final newline false)
ok 1907 - cleanup handles adjacent EOF entries ("\\r\\n", final newline false)
  ---
  duration_ms: 0.263433
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\r\\n", final newline true)
ok 1908 - cleanup handles adjacent EOF entries ("\\r\\n", final newline true)
  ---
  duration_ms: 0.235801
  ...
# Subtest: counted dependencies converge mixed sources and maintain one link per parent
ok 1909 - counted dependencies converge mixed sources and maintain one link per parent
  ---
  duration_ms: 20.538443
  ...
# Subtest: counted and single dependency gestures refuse inside a blockquote (DP29)
ok 1910 - counted and single dependency gestures refuse inside a blockquote (DP29)
  ---
  duration_ms: 0.694666
  ...
# Subtest: counted dependency candidates exclude every source and expose mixed state
ok 1911 - counted dependency candidates exclude every source and expose mixed state
  ---
  duration_ms: 1.981152
  ...
# Subtest: counted dependency block-ID prompting is planned atomically
ok 1912 - counted dependency block-ID prompting is planned atomically
  ---
  duration_ms: 6.207369
  ...
# Subtest: counted dependency runtime applies target, parents, and navigation in one undo group
ok 1913 - counted dependency runtime applies target, parents, and navigation in one undo group
  ---
  duration_ms: 12.453612
  ...
# Subtest: counted Depends-on removal recovers residents with [unblocked::]
ok 1914 - counted Depends-on removal recovers residents with [unblocked::]
  ---
  duration_ms: 7.300414
  ...
# Subtest: counted Depends-on removal writes [unblocked::] through the wired freshness API
ok 1915 - counted Depends-on removal writes [unblocked::] through the wired freshness API
  ---
  duration_ms: 7.171189
  ...
# Subtest: cross-file toggle changes only the source link
ok 1916 - cross-file toggle changes only the source link
  ---
  duration_ms: 3.216559
  ...
# Subtest: cross-file write failure still toggles only the source link
ok 1917 - cross-file write failure still toggles only the source link
  ---
  duration_ms: 0.798624
  ...
# Subtest: line-local fallback applies bottom-up and preserves CRLF
ok 1918 - line-local fallback applies bottom-up and preserves CRLF
  ---
  duration_ms: 0.998045
  ...
# Subtest: source line-count invariant rejects embedded newline changes
ok 1919 - source line-count invariant rejects embedded newline changes
  ---
  duration_ms: 0.678706
  ...
# Subtest: pure toggle refuses when the source changed under it
ok 1920 - pure toggle refuses when the source changed under it
  ---
  duration_ms: 0.348665
  ...
# Subtest: counted transclusion toggle evaluates each line independently
ok 1921 - counted transclusion toggle evaluates each line independently
  ---
  duration_ms: 0.988036
  ...
# Subtest: transclusion toggle is refused on Depends-On lines
ok 1922 - transclusion toggle is refused on Depends-On lines
  ---
  duration_ms: 0.686571
  ...
# Subtest: transclusion toggles refuse generated BLOCKS lines with their notice
ok 1923 - transclusion toggles refuse generated BLOCKS lines with their notice
  ---
  duration_ms: 1.32528
  ...
# Subtest: legacy sole-link children toggle purely, without field or status writes
ok 1924 - legacy sole-link children toggle purely, without field or status writes
  ---
  duration_ms: 1.275825
  ...
# Subtest: Ctrl+D on the Depends on row clears the line, field, and legacy children
ok 1925 - Ctrl+D on the Depends on row clears the line, field, and legacy children
  ---
  duration_ms: 11.137579
  ...
# Subtest: Ctrl+D clears a field-only dependency without a line
ok 1926 - Ctrl+D clears a field-only dependency without a line
  ---
  duration_ms: 4.240134
  ...
# Subtest: counted Ctrl+D on the Depends on row clears every targeted task
ok 1927 - counted Ctrl+D on the Depends on row clears every targeted task
  ---
  duration_ms: 5.937503
  ...
# Subtest: findRemovedLineText reports deleted lines
ok 1928 - findRemovedLineText reports deleted lines
  ---
  duration_ms: 0.638268
  ...
# Subtest: hand-edit mirror projects an edited line into the field
ok 1929 - hand-edit mirror projects an edited line into the field
  ---
  duration_ms: 3.512326
  ...
# Subtest: hand-edit mirror canonicalises a hand-written line variant
ok 1930 - hand-edit mirror canonicalises a hand-written line variant
  ---
  duration_ms: 1.763696
  ...
# Subtest: hand-edit mirror drops a linkless line and the field
ok 1931 - hand-edit mirror drops a linkless line and the field
  ---
  duration_ms: 2.238572
  ...
# Subtest: hand-edit mirror clears the field after the line is deleted
ok 1932 - hand-edit mirror clears the field after the line is deleted
  ---
  duration_ms: 2.151927
  ...
# Subtest: hand-edit mirror leaves malformed lines alone
ok 1933 - hand-edit mirror leaves malformed lines alone
  ---
  duration_ms: 0.628219
  ...
# Subtest: hand-edit mirror leaves legacy-only children for the hooks
ok 1934 - hand-edit mirror leaves legacy-only children for the hooks
  ---
  duration_ms: 0.924755
  ...
# Subtest: hand-edit mirror blocks when an open prerequisite is added by hand
ok 1935 - hand-edit mirror blocks when an open prerequisite is added by hand
  ---
  duration_ms: 1.771591
  ...
# Subtest: hand-edit mirror never transfers commitment to the target
ok 1936 - hand-edit mirror never transfers commitment to the target
  ---
  duration_ms: 1.414379
  ...
# Subtest: hand-edit mirror recovers when the last open prerequisite is removed by hand
ok 1937 - hand-edit mirror recovers when the last open prerequisite is removed by hand
  ---
  duration_ms: 2.141448
  ...
# Subtest: hand-edit mirror leaves a half-typed link alone
ok 1938 - hand-edit mirror leaves a half-typed link alone
  ---
  duration_ms: 0.647636
  ...
# Subtest: hand-edit mirror clears the owning task when its last-child line is deleted
ok 1939 - hand-edit mirror clears the owning task when its last-child line is deleted
  ---
  duration_ms: 2.995969
  ...
# Subtest: counted add below a prerequisite follows BLOCKS shifts (bob-cli-95)
ok 1940 - counted add below a prerequisite follows BLOCKS shifts (bob-cli-95)
  ---
  duration_ms: 5.026885
  ...
# Subtest: counted remove follows BLOCKS deletions above the sources
ok 1941 - counted remove follows BLOCKS deletions above the sources
  ---
  duration_ms: 4.298344
  ...
# Subtest: counted runtime commits once with the mapped first-source cursor
ok 1942 - counted runtime commits once with the mapped first-source cursor
  ---
  duration_ms: 3.314437
  ...
# Subtest: mirror scheduler debounces at the contract interval
ok 1943 - mirror scheduler debounces at the contract interval
  ---
  duration_ms: 2.682421
  ...
# Subtest: mirror scheduler seeds the baseline from the update start state
ok 1944 - mirror scheduler seeds the baseline from the update start state
  ---
  duration_ms: 4.423924
  ...
# Subtest: mirror scheduler keeps the first baseline and maps the owner across a burst
ok 1945 - mirror scheduler keeps the first baseline and maps the owner across a burst
  ---
  duration_ms: 1.104017
  ...
# Subtest: mirror listener runs clear-field for a first-edit deletion with a following sibling
ok 1946 - mirror listener runs clear-field for a first-edit deletion with a following sibling
  ---
  duration_ms: 26.601567
  ...
# Subtest: mirror fire re-arms while the cursor stays on the edited line
ok 1947 - mirror fire re-arms while the cursor stays on the edited line
  ---
  duration_ms: 5.371733
  ...
# Subtest: mirror scheduler reads changed ranges from the CM6 update
ok 1948 - mirror scheduler reads changed ranges from the CM6 update
  ---
  duration_ms: 0.642206
  ...
# Subtest: mirror scheduler skips IME composition
ok 1949 - mirror scheduler skips IME composition
  ---
  duration_ms: 0.437535
  ...
# Subtest: mirror scheduler skips open modals
ok 1950 - mirror scheduler skips open modals
  ---
  duration_ms: 0.341833
  ...
# Subtest: counted Ctrl+D clears every targeted task in one transaction with one notice
ok 1951 - counted Ctrl+D clears every targeted task in one transaction with one notice
  ---
  duration_ms: 8.132945
  ...
# Subtest: counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
ok 1952 - counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
  ---
  duration_ms: 2.64089
  ...
# Subtest: counted N! on only a Depends-On line refuses without writing
ok 1953 - counted N! on only a Depends-On line refuses without writing
  ---
  duration_ms: 0.705196
  ...
# Subtest: promotion targets enumerate real tasks and assign stable IDs
ok 1954 - promotion targets enumerate real tasks and assign stable IDs
  ---
  duration_ms: 8.237004
  ...
# Subtest: promotion file planner expands live links and preserves history
ok 1955 - promotion file planner expands live links and preserves history
  ---
  duration_ms: 11.891459
  ...
# Subtest: promotion file planner handles forms, whitespace, and subtrees
ok 1956 - promotion file planner handles forms, whitespace, and subtrees
  ---
  duration_ms: 2.766471
  ...
# Subtest: promotion file planner keeps compatibility for non-live references
ok 1957 - promotion file planner keeps compatibility for non-live references
  ---
  duration_ms: 1.5666
  ...
# Subtest: forward promotion expands live links, persists anchors, and removes the source
ok 1958 - forward promotion expands live links, persists anchors, and removes the source
  ---
  duration_ms: 20.62555
  ...
# Subtest: forward promotion preserves a concurrent frontmatter write before anchoring
ok 1959 - forward promotion preserves a concurrent frontmatter write before anchoring
  ---
  duration_ms: 2.486146
  ...
# Subtest: forward promotion rebases anchors in an open project editor
ok 1960 - forward promotion rebases anchors in an open project editor
  ---
  duration_ms: 3.317693
  ...
# Subtest: forward promotion refuses a concurrent edit to a task line being anchored
ok 1961 - forward promotion refuses a concurrent edit to a task line being anchored
  ---
  duration_ms: 1.871582
  ...
# Subtest: forward promotion uses zero-task fallback and keeps reverse one-to-one
ok 1962 - forward promotion uses zero-task fallback and keeps reverse one-to-one
  ---
  duration_ms: 1.62973
  ...
# Subtest: forward promotion retains the source on ambiguous, stale, and write failures
ok 1963 - forward promotion retains the source on ambiguous, stale, and write failures
  ---
  duration_ms: 2.16876
  ...
# Subtest: forward promotion discovers live links without a backlink cache and uses one open-editor write
ok 1964 - forward promotion discovers live links without a backlink cache and uses one open-editor write
  ---
  duration_ms: 2.01647
  ...
# Subtest: forward conversion carries a Depends-On line and reverse restores it
ok 1965 - forward conversion carries a Depends-On line and reverse restores it
  ---
  duration_ms: 53.518436
  ...
# Subtest: reverse conversion re-keys a cross-note prerequisite BLOCKS link
ok 1966 - reverse conversion re-keys a cross-note prerequisite BLOCKS link
  ---
  duration_ms: 16.694546
  ...
# Subtest: planTaskLaneBatch commits every Ready target to Next
ok 1967 - planTaskLaneBatch commits every Ready target to Next
  ---
  duration_ms: 6.204754
  ...
# Subtest: planTaskLaneBatch releases Next and In Progress to Ready
ok 1968 - planTaskLaneBatch releases Next and In Progress to Ready
  ---
  duration_ms: 1.198919
  ...
# Subtest: planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
ok 1969 - planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
  ---
  duration_ms: 1.715935
  ...
# Subtest: planTaskLaneBatch skips Blocked and refuses stale preimages
ok 1970 - planTaskLaneBatch skips Blocked and refuses stale preimages
  ---
  duration_ms: 0.881232
  ...
# Subtest: buildLaneToggleNotice reports commit and release with and without budgets
ok 1971 - buildLaneToggleNotice reports commit and release with and without budgets
  ---
  duration_ms: 0.874479
  ...
# Subtest: describeLaneRow covers task, counted, and link sessions
ok 1972 - describeLaneRow covers task, counted, and link sessions
  ---
  duration_ms: 1.119197
  ...
# Subtest: toggleTaskLane commits Ready to Next and reports lane budgets
ok 1973 - toggleTaskLane commits Ready to Next and reports lane budgets
  ---
  duration_ms: 6.07707
  ...
# Subtest: toggleTaskLane releases to Ready without the api
ok 1974 - toggleTaskLane releases to Ready without the api
  ---
  duration_ms: 2.087125
  ...
# Subtest: toggleTaskLane release logs the summary on In Progress tasks
ok 1975 - toggleTaskLane release logs the summary on In Progress tasks
  ---
  duration_ms: 2.416021
  ...
# Subtest: toggleTaskLane skips Blocked targets
ok 1976 - toggleTaskLane skips Blocked targets
  ---
  duration_ms: 1.407737
  ...
# Subtest: counted toggleTaskLane covers the current task plus the next N tasks
ok 1977 - counted toggleTaskLane covers the current task plus the next N tasks
  ---
  duration_ms: 0.847838
  ...
# Subtest: toggleTaskLane on a Task Link writes through the open buffer
ok 1978 - toggleTaskLane on a Task Link writes through the open buffer
  ---
  duration_ms: 12.101129
  ...
# Subtest: toggleTaskLane on Task Links releases across notes
ok 1979 - toggleTaskLane on Task Links releases across notes
  ---
  duration_ms: 2.668484
  ...
# Subtest: toggleTaskLane refuses when a preimage changed
ok 1980 - toggleTaskLane refuses when a preimage changed
  ---
  duration_ms: 0.677463
  ...
# Subtest: Ctrl+Shift+P shows a pinned lane row that commits immediately
ok 1981 - Ctrl+Shift+P shows a pinned lane row that commits immediately
  ---
  duration_ms: 25.4189
  ...
# Subtest: Ctrl+Shift+P link mode shows the lane row with release detail
ok 1982 - Ctrl+Shift+P link mode shows the lane row with release detail
  ---
  duration_ms: 10.724531
  ...
# Subtest: Ctrl+Shift+P lane release with In Progress goes through the reason stage
ok 1983 - Ctrl+Shift+P lane release with In Progress goes through the reason stage
  ---
  duration_ms: 6.029599
  ...
# Subtest: getLinkPickerSessionSubtitle keeps the clamp for a single link
ok 1984 - getLinkPickerSessionSubtitle keeps the clamp for a single link
  ---
  duration_ms: 0.758778
  ...
# Subtest: link-mode priority notice keeps via Task Links visible
ok 1985 - link-mode priority notice keeps via Task Links visible
  ---
  duration_ms: 10.360737
  ...
# Subtest: already-handled Alt+N leaves Vim state alone
ok 1986 - already-handled Alt+N leaves Vim state alone
  ---
  duration_ms: 1.236631
  ...
# Subtest: Alt+N fallback still dispatches once with the Vim count
ok 1987 - Alt+N fallback still dispatches once with the Vim count
  ---
  duration_ms: 2.235166
  ...
# Subtest: lane release deletes an emptied entry (cross-file, Alt+N)
ok 1988 - lane release deletes an emptied entry (cross-file, Alt+N)
  ---
  duration_ms: 6.165048
  ...
# Subtest: lane release deletes an emptied entry (cross-file, card)
ok 1989 - lane release deletes an emptied entry (cross-file, card)
  ---
  duration_ms: 5.077362
  ...
# Subtest: lane release deletes an emptied entry (same-file, Alt+N)
ok 1990 - lane release deletes an emptied entry (same-file, Alt+N)
  ---
  duration_ms: 1.671912
  ...
# Subtest: lane release deletes an emptied entry (same-file, card)
ok 1991 - lane release deletes an emptied entry (same-file, card)
  ---
  duration_ms: 6.225813
  ...
# Subtest: Task Link release deletes its entry in one undo group (separate, Alt+N)
ok 1992 - Task Link release deletes its entry in one undo group (separate, Alt+N)
  ---
  duration_ms: 3.346588
  ...
# Subtest: Task Link release deletes its entry in one undo group (separate, card)
ok 1993 - Task Link release deletes its entry in one undo group (separate, card)
  ---
  duration_ms: 7.200315
  ...
# Subtest: Task Link release deletes its entry in one undo group (folded, Alt+N)
ok 1994 - Task Link release deletes its entry in one undo group (folded, Alt+N)
  ---
  duration_ms: 2.408357
  ...
# Subtest: Task Link release deletes its entry in one undo group (folded, card)
ok 1995 - Task Link release deletes its entry in one undo group (folded, card)
  ---
  duration_ms: 5.576083
  ...
# Subtest: parseLinkPickerTaskLink recognizes dedicated Task Link bullets
ok 1996 - parseLinkPickerTaskLink recognizes dedicated Task Link bullets
  ---
  duration_ms: 4.447449
  ...
# Subtest: discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
ok 1997 - discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
  ---
  duration_ms: 1.789215
  ...
# Subtest: discoverLinkPickerTargets leaves \#task lines to the regular picker
ok 1998 - discoverLinkPickerTargets leaves \#task lines to the regular picker
  ---
  duration_ms: 0.503231
  ...
# Subtest: findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
ok 1999 - findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
  ---
  duration_ms: 1.040877
  ...
# Subtest: createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
ok 2000 - createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
  ---
  duration_ms: 2.929902
  ...
# Subtest: getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
ok 2001 - getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
  ---
  duration_ms: 1.112634
  ...
# Subtest: bare link mode edits the task behind a Task Link through the open buffer
ok 2002 - bare link mode edits the task behind a Task Link through the open buffer
  ---
  duration_ms: 31.596904
  ...
# Subtest: counted link mode writes across notes through both the open buffer and the vault
ok 2003 - counted link mode writes across notes through both the open buffer and the vault
  ---
  duration_ms: 15.047773
  ...
# Subtest: Task Link scheduled delete recovers a Blocked task through the wired freshness API
ok 2004 - Task Link scheduled delete recovers a Blocked task through the wired freshness API
  ---
  duration_ms: 8.335801
  ...
# Subtest: link mode refuses the whole operation when a linked note changed
ok 2005 - link mode refuses the whole operation when a linked note changed
  ---
  duration_ms: 13.114403
  ...
# Subtest: link mode reports a closed target and changes nothing
ok 2006 - link mode reports a closed target and changes nothing
  ---
  duration_ms: 1.90187
  ...
# Subtest: link mode defers to a future date, blocks the task, and prunes today
ok 2007 - link mode defers to a future date, blocks the task, and prunes today
  ---
  duration_ms: 14.826411
  ...
# Subtest: bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
ok 2008 - bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
  ---
  duration_ms: 7.090505
  ...
# Subtest: Task Link scheduled write deletes its entry (separate)
ok 2009 - Task Link scheduled write deletes its entry (separate)
  ---
  duration_ms: 7.969601
  ...
# Subtest: Task Link scheduled write deletes its entry (folded)
ok 2010 - Task Link scheduled write deletes its entry (folded)
  ---
  duration_ms: 7.227887
  ...
# Subtest: folded Task Link scheduling maps the cursor past logs inserted before the emptied entry
ok 2011 - folded Task Link scheduling maps the cursor past logs inserted before the emptied entry
  ---
  duration_ms: 6.540364
  ...
# Subtest: dash restore suppresses editor notice after deliberate navigation
ok 2012 - dash restore suppresses editor notice after deliberate navigation
  ---
  duration_ms: 26.504953
  ...
# Subtest: open-task dispatch timeout is registered for plugin cleanup
ok 2013 - open-task dispatch timeout is registered for plugin cleanup
  ---
  duration_ms: 1.083087
  ...
# Subtest: jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
ok 2014 - jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
  ---
  duration_ms: 7.23007
  ...
# Subtest: jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
ok 2015 - jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
  ---
  duration_ms: 1.953218
  ...
# Subtest: jumpToOpenObsidianTask keeps current-swap transaction failures local
ok 2016 - jumpToOpenObsidianTask keeps current-swap transaction failures local
  ---
  duration_ms: 1.076034
  ...
# Subtest: jumpToOpenObsidianTask refuses current-up without jumping or mutating
ok 2017 - jumpToOpenObsidianTask refuses current-up without jumping or mutating
  ---
  duration_ms: 0.611197
  ...
# Subtest: jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
ok 2018 - jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
  ---
  duration_ms: 2.838719
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
ok 2019 - Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
  ---
  duration_ms: 0.834373
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
ok 2020 - Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
  ---
  duration_ms: 1.083278
  ...
# Subtest: counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
ok 2021 - counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
  ---
  duration_ms: 1.549268
  ...
# Subtest: an impossible counted Pomodoro move refuses without jumping or mutating
ok 2022 - an impossible counted Pomodoro move refuses without jumping or mutating
  ---
  duration_ms: 0.631495
  ...
# Subtest: counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
ok 2023 - counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
  ---
  duration_ms: 6.092709
  ...
# Subtest: counted open-task jump on a sole current target keeps the existing notice
ok 2024 - counted open-task jump on a sole current target keeps the existing notice
  ---
  duration_ms: 0.705507
  ...
# Subtest: dispatch guard allows exactly one counted Pomodoro move when the command route also fires
ok 2025 - dispatch guard allows exactly one counted Pomodoro move when the command route also fires
  ---
  duration_ms: 1.727979
  ...
# Subtest: bullet property picker reconciles duplicate bare and counted opens
ok 2026 - bullet property picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 26.459436
  ...
# Subtest: bullet property picker close lifecycle clears tracking for fresh sessions
ok 2027 - bullet property picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 14.415848
  ...
# Subtest: task move picker reconciles duplicate bare and counted opens
ok 2028 - task move picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 4.747702
  ...
# Subtest: task move picker close lifecycle clears tracking for fresh sessions
ok 2029 - task move picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 6.351052
  ...
# Subtest: Pomodoro bullet move picker opens sessions and clears the shared move picker slot
ok 2030 - Pomodoro bullet move picker opens sessions and clears the shared move picker slot
  ---
  duration_ms: 6.888308
  ...
# Subtest: Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
ok 2031 - Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
  ---
  duration_ms: 1.850201
  ...
# Subtest: move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
ok 2032 - move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
  ---
  duration_ms: 2.706727
  ...
# Subtest: commitPomodoroBulletMoveSession applies one guarded same-file transaction
ok 2033 - commitPomodoroBulletMoveSession applies one guarded same-file transaction
  ---
  duration_ms: 4.675916
  ...
# Subtest: Pomodoro bullet move picker confirms = through the actual picker callback
ok 2034 - Pomodoro bullet move picker confirms = through the actual picker callback
  ---
  duration_ms: 2.161326
  ...
# Subtest: Pomodoro bullet move picker reserves =NAME for peeling a named merged component
ok 2035 - Pomodoro bullet move picker reserves =NAME for peeling a named merged component
  ---
  duration_ms: 2.078728
  ...
# Subtest: Pomodoro bullet move picker confirms =email through the actual picker callback
ok 2036 - Pomodoro bullet move picker confirms =email through the actual picker callback
  ---
  duration_ms: 2.723929
  ...
# Subtest: Pomodoro bullet move picker confirms = review through the actual picker callback
ok 2037 - Pomodoro bullet move picker confirms = review through the actual picker callback
  ---
  duration_ms: 1.601407
  ...
# Subtest: Pomodoro bullet move picker confirms =focus by unnaming a single-name source
ok 2038 - Pomodoro bullet move picker confirms =focus by unnaming a single-name source
  ---
  duration_ms: 2.331861
  ...
# Subtest: Pomodoro bullet split stale-content guard does not write
ok 2039 - Pomodoro bullet split stale-content guard does not write
  ---
  duration_ms: 0.96409
  ...
# Subtest: Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
ok 2040 - Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
  ---
  duration_ms: 1.604993
  ...
# Subtest: native isOpen regression: pickers attach, close clears slot, reopen works
ok 2041 - native isOpen regression: pickers attach, close clears slot, reopen works
  ---
  duration_ms: 5.732143
  ...
# Subtest: stale registered pickers fail open on the next key
ok 2042 - stale registered pickers fail open on the next key
  ---
  duration_ms: 8.958571
  ...
# Subtest: Task Card onClose clears card classes and resolving flags
ok 2043 - Task Card onClose clears card classes and resolving flags
  ---
  duration_ms: 2.439928
  ...
# Subtest: planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
ok 2044 - planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
  ---
  duration_ms: 8.710907
  ...
# Subtest: planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
ok 2045 - planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
  ---
  duration_ms: 1.181075
  ...
# Subtest: planPomodoroBulletMove preserves the source when only some siblings move out
ok 2046 - planPomodoroBulletMove preserves the source when only some siblings move out
  ---
  duration_ms: 0.453256
  ...
# Subtest: planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
ok 2047 - planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
  ---
  duration_ms: 0.537146
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
ok 2048 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
  ---
  duration_ms: 1.059723
  ...
# Subtest: planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
ok 2049 - planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
  ---
  duration_ms: 1.340178
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
ok 2050 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
  ---
  duration_ms: 0.592391
  ...
# Subtest: planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
ok 2051 - planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
  ---
  duration_ms: 0.448577
  ...
# Subtest: planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
ok 2052 - planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
  ---
  duration_ms: 0.643198
  ...
# Subtest: planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
ok 2053 - planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
  ---
  duration_ms: 7.494055
  ...
# Subtest: planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
ok 2054 - planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
  ---
  duration_ms: 0.699755
  ...
# Subtest: planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
ok 2055 - planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
  ---
  duration_ms: 0.42464
  ...
# Subtest: planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
ok 2056 - planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
  ---
  duration_ms: 1.040947
  ...
# Subtest: planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
ok 2057 - planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
  ---
  duration_ms: 0.769368
  ...
# Subtest: planPomodoroBulletMove deletes both open and closed source entries the same way
ok 2058 - planPomodoroBulletMove deletes both open and closed source entries the same way
  ---
  duration_ms: 0.696199
  ...
# Subtest: planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
ok 2059 - planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
  ---
  duration_ms: 0.776141
  ...
# Subtest: planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
ok 2060 - planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
  ---
  duration_ms: 0.718221
  ...
# Subtest: planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
ok 2061 - planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
  ---
  duration_ms: 1.160094
  ...
# Subtest: planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
ok 2062 - planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
  ---
  duration_ms: 0.52885
  ...
# Subtest: planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
ok 2063 - planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
  ---
  duration_ms: 0.698153
  ...
# Subtest: planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
ok 2064 - planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
  ---
  duration_ms: 0.619893
  ...
# Subtest: planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
ok 2065 - planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
  ---
  duration_ms: 0.412196
  ...
# Subtest: planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
ok 2066 - planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
  ---
  duration_ms: 0.352393
  ...
# Subtest: planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
ok 2067 - planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
  ---
  duration_ms: 0.594545
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
ok 2068 - planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
  ---
  duration_ms: 0.391577
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
ok 2069 - planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
  ---
  duration_ms: 8.707562
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
ok 2070 - planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
  ---
  duration_ms: 7.30849
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
ok 2071 - planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
  ---
  duration_ms: 0.985891
  ...
# Subtest: navigation Pomodoro picker renders theme accents and Ctrl+D only changes Recent suggestions
ok 2072 - navigation Pomodoro picker renders theme accents and Ctrl+D only changes Recent suggestions
  ---
  duration_ms: 55.839657
  ...
# Subtest: Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
ok 2073 - Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
  ---
  duration_ms: 3.624438
  ...
# Subtest: commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
ok 2074 - commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
  ---
  duration_ms: 5.729007
  ...
# Subtest: commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
ok 2075 - commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
  ---
  duration_ms: 1.620753
  ...
# Subtest: commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
ok 2076 - commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
  ---
  duration_ms: 0.998395
  ...
# Subtest: commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
ok 2077 - commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
  ---
  duration_ms: 0.650832
  ...
# Subtest: Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
ok 2078 - Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
  ---
  duration_ms: 19.77666
  ...
# Subtest: Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
ok 2079 - Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
  ---
  duration_ms: 2.313666
  ...
# Subtest: Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
ok 2080 - Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
  ---
  duration_ms: 6.680924
  ...
# Subtest: Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
ok 2081 - Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
  ---
  duration_ms: 3.207121
  ...
# Subtest: task move picker closes before commit while other pickers retain delayed close
ok 2082 - task move picker closes before commit while other pickers retain delayed close
  ---
  duration_ms: 1.738769
  ...
# Subtest: parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
ok 2083 - parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
  ---
  duration_ms: 4.524266
  ...
# Subtest: normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
ok 2084 - normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
  ---
  duration_ms: 0.655311
  ...
# Subtest: formatPomodoroEntryLine emits a placeholder entry with or without a name
ok 2085 - formatPomodoroEntryLine emits a placeholder entry with or without a name
  ---
  duration_ms: 0.24131
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
ok 2086 - createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
  ---
  duration_ms: 4.930712
  ...
# Subtest: Pomodoro move pickers place recent themes around typed names and exclude today's themes
ok 2087 - Pomodoro move pickers place recent themes around typed names and exclude today's themes
  ---
  duration_ms: 25.752848
  ...
# Subtest: createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
ok 2088 - createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
  ---
  duration_ms: 2.459164
  ...
# Subtest: createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
ok 2089 - createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
  ---
  duration_ms: 1.435089
  ...
# Subtest: createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
ok 2090 - createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
  ---
  duration_ms: 1.558264
  ...
# Subtest: buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
ok 2091 - buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
  ---
  duration_ms: 0.690879
  ...
# Subtest: buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
ok 2092 - buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
  ---
  duration_ms: 0.532517
  ...
# Subtest: createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
ok 2093 - createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
  ---
  duration_ms: 0.804175
  ...
# Subtest: createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
ok 2094 - createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
  ---
  duration_ms: 0.516777
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
ok 2095 - createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
  ---
  duration_ms: 1.027591
  ...
# Subtest: collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
ok 2096 - collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
  ---
  duration_ms: 1.106221
  ...
# Subtest: findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
ok 2097 - findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
  ---
  duration_ms: 4.787778
  ...
# Subtest: findPomodoroBulletContext leaves plain \#task lines on the task-move route
ok 2098 - findPomodoroBulletContext leaves plain \#task lines on the task-move route
  ---
  duration_ms: 0.872896
  ...
# Subtest: discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
ok 2099 - discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
  ---
  duration_ms: 2.040435
  ...
# Subtest: findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
ok 2100 - findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
  ---
  duration_ms: 1.345498
  ...
# Subtest: discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
ok 2101 - discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
  ---
  duration_ms: 1.784687
  ...
# Subtest: isMovablePomodoroEntryContext matches open current and future Pomodoro entries
ok 2102 - isMovablePomodoroEntryContext matches open current and future Pomodoro entries
  ---
  duration_ms: 5.616552
  ...
# Subtest: planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
ok 2103 - planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
  ---
  duration_ms: 1.255577
  ...
# Subtest: planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
ok 2104 - planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
  ---
  duration_ms: 0.419761
  ...
# Subtest: planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
ok 2105 - planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
  ---
  duration_ms: 0.660481
  ...
# Subtest: planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
ok 2106 - planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
  ---
  duration_ms: 0.557343
  ...
# Subtest: planPomodoroEntryReorder handles counted current swaps and their inverses
ok 2107 - planPomodoroEntryReorder handles counted current swaps and their inverses
  ---
  duration_ms: 1.020378
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
ok 2108 - planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
  ---
  duration_ms: 0.527366
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
ok 2109 - planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
  ---
  duration_ms: 0.40342
  ...
# Subtest: planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
ok 2110 - planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
  ---
  duration_ms: 0.764539
  ...
# Subtest: planPomodoroEntryReorder round-trips a future-up swap across the current open entry
ok 2111 - planPomodoroEntryReorder round-trips a future-up swap across the current open entry
  ---
  duration_ms: 0.774669
  ...
# Subtest: planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
ok 2112 - planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
  ---
  duration_ms: 1.202937
  ...
# Subtest: planPomodoroEntryReorder refuses moving down past the last placeholder in the section
ok 2113 - planPomodoroEntryReorder refuses moving down past the last placeholder in the section
  ---
  duration_ms: 0.39307
  ...
# Subtest: planPomodoroEntryReorder refuses both directions for a lone placeholder
ok 2114 - planPomodoroEntryReorder refuses both directions for a lone placeholder
  ---
  duration_ms: 0.43481
  ...
# Subtest: planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
ok 2115 - planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
  ---
  duration_ms: 2.018053
  ...
# Subtest: planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
ok 2116 - planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
  ---
  duration_ms: 0.503722
  ...
# Subtest: planPomodoroEntryReorder refuses illegal current/future spans atomically
ok 2117 - planPomodoroEntryReorder refuses illegal current/future spans atomically
  ---
  duration_ms: 1.211683
  ...
# Subtest: planPomodoroEntryReorder rejects a stale source line
ok 2118 - planPomodoroEntryReorder rejects a stale source line
  ---
  duration_ms: 0.38216
  ...
# Subtest: planPomodoroEntryReorder round-trips CRLF content
ok 2119 - planPomodoroEntryReorder round-trips CRLF content
  ---
  duration_ms: 0.778887
  ...
# Subtest: planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
ok 2120 - planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
  ---
  duration_ms: 0.43982
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
ok 2121 - planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
  ---
  duration_ms: 0.638659
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up three positions and round-trips
ok 2122 - planPomodoroEntryReorder moves a placeholder up three positions and round-trips
  ---
  duration_ms: 0.903444
  ...
# Subtest: planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
ok 2123 - planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
  ---
  duration_ms: 0.391728
  ...
# Subtest: planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
ok 2124 - planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
  ---
  duration_ms: 1.018644
  ...
# Subtest: planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
ok 2125 - planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
  ---
  duration_ms: 1.376908
  ...
# Subtest: planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
ok 2126 - planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
  ---
  duration_ms: 0.602991
  ...
# Subtest: peelPomodoroMergedName removes every matching canonical plus component
ok 2127 - peelPomodoroMergedName removes every matching canonical plus component
  ---
  duration_ms: 2.479563
  ...
# Subtest: planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
ok 2128 - planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
  ---
  duration_ms: 5.450613
  ...
# Subtest: planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
ok 2129 - planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
  ---
  duration_ms: 0.805387
  ...
# Subtest: planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
ok 2130 - planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
  ---
  duration_ms: 0.814374
  ...
# Subtest: planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
ok 2131 - planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
  ---
  duration_ms: 1.286546
  ...
# Subtest: planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
ok 2132 - planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
  ---
  duration_ms: 4.101901
  ...
# Subtest: planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
ok 2133 - planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
  ---
  duration_ms: 1.160575
  ...
# Subtest: planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
ok 2134 - planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
  ---
  duration_ms: 1.897021
  ...
# Subtest: Pomodoro bullet move picker typing =NAME or Escape does not write
ok 2135 - Pomodoro bullet move picker typing =NAME or Escape does not write
  ---
  duration_ms: 4.450525
  ...
# Subtest: planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
ok 2136 - planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
  ---
  duration_ms: 0.725815
  ...
# Subtest: planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
ok 2137 - planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
  ---
  duration_ms: 0.383792
  ...
# Subtest: planPomodoroEntryRename reports unchanged when the normalized name matches the current name
ok 2138 - planPomodoroEntryRename reports unchanged when the normalized name matches the current name
  ---
  duration_ms: 0.234448
  ...
# Subtest: planPomodoroEntryRename rejects unsupported trailing content and a stale source line
ok 2139 - planPomodoroEntryRename rejects unsupported trailing content and a stale source line
  ---
  duration_ms: 0.337414
  ...
# Subtest: planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
ok 2140 - planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
  ---
  duration_ms: 0.385506
  ...
# Subtest: planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
ok 2141 - planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
  ---
  duration_ms: 5.768631
  ...
# Subtest: planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
ok 2142 - planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
  ---
  duration_ms: 2.594963
  ...
# Subtest: planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
ok 2143 - planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
  ---
  duration_ms: 1.001662
  ...
# Subtest: manager relative dates label today, yesterday, and older days
ok 2144 - manager relative dates label today, yesterday, and older days
  ---
  duration_ms: 3.048188
  ...
# Subtest: manager duplicate pairs follow the near-duplicate rule
ok 2145 - manager duplicate pairs follow the near-duplicate rule
  ---
  duration_ms: 1.270545
  ...
# Subtest: manager rows separate views, hints, and reappeared flags
ok 2146 - manager rows separate views, hints, and reappeared flags
  ---
  duration_ms: 3.196091
  ...
# Subtest: manager rename input rejects empty names and composites
ok 2147 - manager rename input rejects empty names and composites
  ---
  duration_ms: 0.652836
  ...
# Subtest: manager rename preview formats files, entries, and state notes
ok 2148 - manager rename preview formats files, entries, and state notes
  ---
  duration_ms: 0.918945
  ...
# Subtest: manager occurrences scan skips fences and non-Pomodoro bullets
ok 2149 - manager occurrences scan skips fences and non-Pomodoro bullets
  ---
  duration_ms: 1.096874
  ...
# Subtest: manager opens, cycles views, filters, and hides through the stubbed api
ok 2150 - manager opens, cycles views, filters, and hides through the stubbed api
  ---
  duration_ms: 31.830198
  ...
# Subtest: manager refuses without the desktop api
ok 2151 - manager refuses without the desktop api
  ---
  duration_ms: 0.592992
  ...
# Subtest: color modal pins hues and Auto through the stubbed api
ok 2152 - color modal pins hues and Auto through the stubbed api
  ---
  duration_ms: 10.125888
  ...
# Subtest: action modal jumps to actions with single keys when the filter is empty
ok 2153 - action modal jumps to actions with single keys when the filter is empty
  ---
  duration_ms: 2.879947
  ...
# Subtest: rename modal previews the dry run and applies one merge commit
ok 2154 - rename modal previews the dry run and applies one merge commit
  ---
  duration_ms: 2.447422
  ...
# Subtest: rename apply saves touched notes and refuses on a failed save
ok 2155 - rename apply saves touched notes and refuses on a failed save
  ---
  duration_ms: 1.32568
  ...
# Subtest: occurrences modal lists daily notes and opens the entry
ok 2156 - occurrences modal lists daily notes and opens the entry
  ---
  duration_ms: 15.209242
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: priority notice relative day helpers handle offsets ranges and icons
ok 2157 - priority notice relative day helpers handle offsets ranges and icons
  ---
  duration_ms: 2.955441
  ...
# Subtest: priority notice model summarizes single counted and project writes
ok 2158 - priority notice model summarizes single counted and project writes
  ---
  duration_ms: 7.401739
  ...
# Subtest: priority notice renderer builds an accessible fragment
ok 2159 - priority notice renderer builds an accessible fragment
  ---
  duration_ms: 4.013791
  ...
# Subtest: priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
ok 2160 - priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
  ---
  duration_ms: 12.584231
  ...
# Subtest: priority notice falls back to one plain notice without a DOM
ok 2161 - priority notice falls back to one plain notice without a DOM
  ---
  duration_ms: 0.985251
  ...
# Subtest: priority notice falls back to plain text when fragment rendering fails
ok 2162 - priority notice falls back to plain text when fragment rendering fails
  ---
  duration_ms: 0.944292
  ...
# Subtest: priority scheduling rolls inclusively and clamps a random value of one
ok 2163 - priority scheduling rolls inclusively and clamps a random value of one
  ---
  duration_ms: 1.322985
  ...
# Subtest: priority value rows preserve config order and expose labels ranges and current state
ok 2164 - priority value rows preserve config order and expose labels ranges and current state
  ---
  duration_ms: 1.712659
  ...
# Subtest: priority picker writes priority then rolled schedule in one guarded edit
ok 2165 - priority picker writes priority then rolled schedule in one guarded edit
  ---
  duration_ms: 32.248305
  ...
# Subtest: priority picker writes lowest priority with a wide rolled schedule
ok 2166 - priority picker writes lowest priority with a wide rolled schedule
  ---
  duration_ms: 4.345686
  ...
# Subtest: priority picker replaces both existing values without duplicating fields
ok 2167 - priority picker replaces both existing values without duplicating fields
  ---
  duration_ms: 5.931462
  ...
# Subtest: counted priority writes keep the rolled date right of the priority
ok 2168 - counted priority writes keep the rolled date right of the priority
  ---
  duration_ms: 10.395173
  ...
# Subtest: priority picker writes project priority and schedule inline atomically
ok 2169 - priority picker writes project priority and schedule inline atomically
  ---
  duration_ms: 21.986377
  ...
# Subtest: counted priority picker rolls an independent schedule for every task
ok 2170 - counted priority picker rolls an independent schedule for every task
  ---
  duration_ms: 9.944153
  ...
# Subtest: counted priority planning keeps project schedules inline
ok 2171 - counted priority planning keeps project schedules inline
  ---
  duration_ms: 2.007241
  ...
# Subtest: counted priority planning evaluates Blocked recovery per rolled date
ok 2172 - counted priority planning evaluates Blocked recovery per rolled date
  ---
  duration_ms: 3.079789
  ...
# Subtest: a counted priority batch writes one entry per task using each task's own previous level
ok 2173 - a counted priority batch writes one entry per task using each task's own previous level
  ---
  duration_ms: 1.038121
  ...
# Subtest: priority notice models carry the stored level value for the glyph
ok 2174 - priority notice models carry the stored level value for the glyph
  ---
  duration_ms: 1.451711
  ...
# Subtest: ledger priority mark lookup guards version and render
ok 2175 - ledger priority mark lookup guards version and render
  ---
  duration_ms: 0.409592
  ...
# Subtest: priority notice header reuses the shared mark when available
ok 2176 - priority notice header reuses the shared mark when available
  ---
  duration_ms: 1.038162
  ...
# Subtest: priority notice keeps the Lucide icon without a usable mark api
ok 2177 - priority notice keeps the Lucide icon without a usable mark api
  ---
  duration_ms: 2.43056
  ...
# Subtest: a counted priority batch skips a task whose rolled date equals its current date
ok 2178 - a counted priority batch skips a task whose rolled date equals its current date
  ---
  duration_ms: 17.480437
  ...
# Subtest: counted priority runtime aborts a stale session without rolling writes
ok 2179 - counted priority runtime aborts a stale session without rolling writes
  ---
  duration_ms: 4.846421
  ...
# Subtest: scheduled picker pins a priority roll only for configured current priorities
ok 2180 - scheduled picker pins a priority roll only for configured current priorities
  ---
  duration_ms: 41.000803
  ...
# Subtest: Ctrl+R replaces only the pinned priority roll and keeps it selected
ok 2181 - Ctrl+R replaces only the pinned priority roll and keeps it selected
  ---
  duration_ms: 21.439124
  ...
# Subtest: choosing a priority roll writes immediately with a deterministic reason instead of prompting
ok 2182 - choosing a priority roll writes immediately with a deterministic reason instead of prompting
  ---
  duration_ms: 16.457715
  ...
# Subtest: counted scheduled picker requires one shared configured priority
ok 2183 - counted scheduled picker requires one shared configured priority
  ---
  duration_ms: 9.427785
  ...
# Subtest: buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
ok 2184 - buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
  ---
  duration_ms: 7.42939
  ...
# Subtest: buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
ok 2185 - buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
  ---
  duration_ms: 0.522147
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
ok 2186 - buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
  ---
  duration_ms: 1.187287
  ...
# Subtest: buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
ok 2187 - buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
  ---
  duration_ms: 0.515534
  ...
# Subtest: buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
ok 2188 - buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
  ---
  duration_ms: 0.734062
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
ok 2189 - buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
  ---
  duration_ms: 0.300734
  ...
# Subtest: buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
ok 2190 - buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
  ---
  duration_ms: 0.654049
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
ok 2191 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
  ---
  duration_ms: 0.690518
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child work log under the project task
ok 2192 - buildProjectSeedFromChildBullets moves a direct-child work log under the project task
  ---
  duration_ms: 0.543658
  ...
# Subtest: buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
ok 2193 - buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
  ---
  duration_ms: 0.435181
  ...
# Subtest: buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
ok 2194 - buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
  ---
  duration_ms: 0.437656
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
ok 2195 - buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
  ---
  duration_ms: 0.290134
  ...
# Subtest: buildProjectSeedFromChildBullets moves an empty work log without forcing task output
ok 2196 - buildProjectSeedFromChildBullets moves an empty work log without forcing task output
  ---
  duration_ms: 1.051617
  ...
# Subtest: buildProjectSeedFromChildBullets moves managed logs in source order without sorting by kind
ok 2197 - buildProjectSeedFromChildBullets moves managed logs in source order without sorting by kind
  ---
  duration_ms: 1.075343
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
ok 2198 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
  ---
  duration_ms: 0.69717
  ...
# Subtest: parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
ok 2199 - parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
  ---
  duration_ms: 0.671932
  ...
# Subtest: Rotten Log markers, history reading, formatting, and generic insertion
ok 2200 - Rotten Log markers, history reading, formatting, and generic insertion
  ---
  duration_ms: 3.081131
  ...
# Subtest: parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
ok 2201 - parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
  ---
  duration_ms: 0.769138
  ...
# Subtest: parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
ok 2202 - parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
  ---
  duration_ms: 0.488593
  ...
# Subtest: normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
ok 2203 - normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
  ---
  duration_ms: 0.325692
  ...
# Subtest: parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
ok 2204 - parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
  ---
  duration_ms: 0.270477
  ...
# Subtest: formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
ok 2205 - formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
  ---
  duration_ms: 0.275857
  ...
# Subtest: insertProjectSectionNotes fills an empty existing section with a blank line then the notes
ok 2206 - insertProjectSectionNotes fills an empty existing section with a blank line then the notes
  ---
  duration_ms: 1.328777
  ...
# Subtest: insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
ok 2207 - insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
  ---
  duration_ms: 0.352904
  ...
# Subtest: insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
ok 2208 - insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
  ---
  duration_ms: 0.332895
  ...
# Subtest: insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
ok 2209 - insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
  ---
  duration_ms: 0.32481
  ...
# Subtest: insertProjectSectionNotes does not add a trailing newline when the original content had none
ok 2210 - insertProjectSectionNotes does not add a trailing newline when the original content had none
  ---
  duration_ms: 0.277169
  ...
# Subtest: insertProjectSectionNotes preserves CRLF line endings for an existing section
ok 2211 - insertProjectSectionNotes preserves CRLF line endings for an existing section
  ---
  duration_ms: 0.259105
  ...
# Subtest: insertProjectSectionNotes creates a new section using the document's CRLF line ending
ok 2212 - insertProjectSectionNotes creates a new section using the document's CRLF line ending
  ---
  duration_ms: 0.252832
  ...
# Subtest: buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
ok 2213 - buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
  ---
  duration_ms: 0.427977
  ...
# Subtest: buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
ok 2214 - buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
  ---
  duration_ms: 0.784468
  ...
# Subtest: buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
ok 2215 - buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
  ---
  duration_ms: 0.384735
  ...
# Subtest: buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
ok 2216 - buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
  ---
  duration_ms: 2.71865
  ...
# Subtest: project conversion accepts blocked sources and extracts their managed dependency child
ok 2217 - project conversion accepts blocked sources and extracts their managed dependency child
  ---
  duration_ms: 4.825341
  ...
# Subtest: project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
ok 2218 - project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
  ---
  duration_ms: 2.647383
  ...
# Subtest: buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
ok 2219 - buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
  ---
  duration_ms: 0.897022
  ...
# Subtest: buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
ok 2220 - buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
  ---
  duration_ms: 0.443717
  ...
# Subtest: buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
ok 2221 - buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
  ---
  duration_ms: 0.441202
  ...
# Subtest: insertProjectManagedLogLines preserves CRLF line endings
ok 2222 - insertProjectManagedLogLines preserves CRLF line endings
  ---
  duration_ms: 0.435552
  ...
# Subtest: findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
ok 2223 - findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
  ---
  duration_ms: 0.438878
  ...
# Subtest: getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
ok 2224 - getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
  ---
  duration_ms: 0.478624
  ...
# Subtest: getProjectFromTaskNoticeText reports moved log kinds in a fixed order
ok 2225 - getProjectFromTaskNoticeText reports moved log kinds in a fixed order
  ---
  duration_ms: 0.256079
  ...
# Subtest: forward conversion leaves the project Ready when only the source status was Blocked
ok 2226 - forward conversion leaves the project Ready when only the source status was Blocked
  ---
  duration_ms: 1.152861
  ...
# Subtest: buildTaskBlockFromProjectNote restores the worked example and round-trips
ok 2227 - buildTaskBlockFromProjectNote restores the worked example and round-trips
  ---
  duration_ms: 15.667468
  ...
# Subtest: project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
ok 2228 - project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
  ---
  duration_ms: 4.359671
  ...
# Subtest: buildTaskLineFromProjectNote preserves status, tags, and fields
ok 2229 - buildTaskLineFromProjectNote preserves status, tags, and fields
  ---
  duration_ms: 2.992852
  ...
# Subtest: getProjectReversalBlockId inverts the forward basename helper
ok 2230 - getProjectReversalBlockId inverts the forward basename helper
  ---
  duration_ms: 4.518023
  ...
# Subtest: formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
ok 2231 - formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
  ---
  duration_ms: 0.502479
  ...
# Subtest: splitProjectNoteForReversal treats TASKS as the task section and keeps section order
ok 2232 - splitProjectNoteForReversal treats TASKS as the task section and keeps section order
  ---
  duration_ms: 1.884317
  ...
# Subtest: indentProjectReversalLine preserves relative depth and drops blanks
ok 2233 - indentProjectReversalLine preserves relative depth and drops blanks
  ---
  duration_ms: 1.313748
  ...
# Subtest: buildTaskBlockFromProjectNote reports structure and frontmatter errors
ok 2234 - buildTaskBlockFromProjectNote reports structure and frontmatter errors
  ---
  duration_ms: 2.636692
  ...
# Subtest: buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
ok 2235 - buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
  ---
  duration_ms: 2.114747
  ...
# Subtest: rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
ok 2236 - rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
  ---
  duration_ms: 0.729152
  ...
# Subtest: collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
ok 2237 - collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
  ---
  duration_ms: 1.242431
  ...
# Subtest: getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
ok 2238 - getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
  ---
  duration_ms: 0.468865
  ...
# Subtest: convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
ok 2239 - convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
  ---
  duration_ms: 12.528425
  ...
# Subtest: project reversal recovers tagged residents when they leave a blocked project
ok 2240 - project reversal recovers tagged residents when they leave a blocked project
  ---
  duration_ms: 8.108649
  ...
# Subtest: convertProjectNoteToTask separates the restored task from a count-only parent section
ok 2241 - convertProjectNoteToTask separates the restored task from a count-only parent section
  ---
  duration_ms: 6.919256
  ...
# Subtest: createProjectNoteFromTask dispatches reverse only on a real ^prj line
ok 2242 - createProjectNoteFromTask dispatches reverse only on a real ^prj line
  ---
  duration_ms: 4.179588
  ...
# Subtest: convertProjectNoteToTask refusals leave every file untouched
ok 2243 - convertProjectNoteToTask refusals leave every file untouched
  ---
  duration_ms: 7.052011
  ...
# Subtest: planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
ok 2244 - planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
  ---
  duration_ms: 0.962958
  ...
# Subtest: convertProjectNoteToTask writes the parent first when it links to \#^prj
ok 2245 - convertProjectNoteToTask writes the parent first when it links to \#^prj
  ---
  duration_ms: 2.276134
  ...
# Subtest: convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
ok 2246 - convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
  ---
  duration_ms: 6.268445
  ...
# Subtest: convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
ok 2247 - convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
  ---
  duration_ms: 2.423257
  ...
# Subtest: convertProjectNoteToTask reports post-write failures without rolling back
ok 2248 - convertProjectNoteToTask reports post-write failures without rolling back
  ---
  duration_ms: 3.395832
  ...
# Subtest: convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
ok 2249 - convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
  ---
  duration_ms: 3.976199
  ...
# Subtest: convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
ok 2250 - convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
  ---
  duration_ms: 5.841471
  ...
# Subtest: v2 reading task opens its source_pdf in Highlights without writes
ok 2251 - v2 reading task opens its source_pdf in Highlights without writes
  ---
  duration_ms: 7.747627
  ...
# Subtest: every reading-task lane and \#REF casing opens
ok 2252 - every reading-task lane and \#REF casing opens
  ---
  duration_ms: 2.969128
  ...
# Subtest: v1 tracker resolves a PDF link or falls back to its own source_pdf
ok 2253 - v1 tracker resolves a PDF link or falls back to its own source_pdf
  ---
  duration_ms: 0.99017
  ...
# Subtest: plain, embedded, struck, and 🍅 Task Links resolve reading tasks
ok 2254 - plain, embedded, struck, and 🍅 Task Links resolve reading tasks
  ---
  duration_ms: 5.508675
  ...
# Subtest: bare managed embed in a reference note resolves its embedded task
ok 2255 - bare managed embed in a reference note resolves its embedded task
  ---
  duration_ms: 0.878717
  ...
# Subtest: ordinary lines, unresolved Task Links, fences, and outside focus delegate once
ok 2256 - ordinary lines, unresolved Task Links, fences, and outside focus delegate once
  ---
  duration_ms: 1.499161
  ...
# Subtest: identified reading tasks show notices without delegating
ok 2257 - identified reading tasks show notices without delegating
  ---
  duration_ms: 1.05816
  ...
# Subtest: unsafe source_pdf values are refused
ok 2258 - unsafe source_pdf values are refused
  ---
  duration_ms: 1.0006
  ...
# Subtest: bundle launch retries with the app name, and reports stderr on total failure
ok 2259 - bundle launch retries with the app name, and reports stderr on total failure
  ---
  duration_ms: 1.23124
  ...
# Subtest: off macOS shows the selected notice and managed ref-note prose delegates
ok 2260 - off macOS shows the selected notice and managed ref-note prose delegates
  ---
  duration_ms: 0.807792
  ...
# Subtest: pure helpers normalize and parse reference PDF paths
ok 2261 - pure helpers normalize and parse reference PDF paths
  ---
  duration_ms: 0.438868
  ...
# Subtest: command registration is custom-hotkey only
ok 2262 - command registration is custom-hotkey only
  ---
  duration_ms: 0.733911
  ...
# Subtest: nav api openReferencePdf hands a source_pdf to Highlights without version or vault writes
ok 2263 - nav api openReferencePdf hands a source_pdf to Highlights without version or vault writes
  ---
  duration_ms: 1.193899
  ...
# Subtest: nav api openReferencePdf settles to a reason instead of throwing
ok 2264 - nav api openReferencePdf settles to a reason instead of throwing
  ---
  duration_ms: 1.057889
  ...
# Subtest: reading tasks read with the book prefix, plain tasks unchanged
ok 2265 - reading tasks read with the book prefix, plain tasks unchanged
  ---
  duration_ms: 5.50581
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 2266 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.495165
  ...
# Subtest: picker rows carry the book prefix in displayText
ok 2267 - picker rows carry the book prefix in displayText
  ---
  duration_ms: 2.159262
  ...
# Subtest: managed reference rename modal and submit are refused
ok 2268 - managed reference rename modal and submit are refused
  ---
  duration_ms: 3.794132
  ...
# Subtest: legacy ref notes and non-ref notes still rename
ok 2269 - legacy ref notes and non-ref notes still rename
  ---
  duration_ms: 2.154282
  ...
# Subtest: managed reference predicate checks path and non-empty source_pdf
ok 2270 - managed reference predicate checks path and non-empty source_pdf
  ---
  duration_ms: 0.322386
  ...
# Subtest: planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
ok 2271 - planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
  ---
  duration_ms: 12.06004
  ...
# Subtest: planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
ok 2272 - planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
  ---
  duration_ms: 3.642494
  ...
# Subtest: runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
ok 2273 - runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
  ---
  duration_ms: 6.2448
  ...
# Subtest: runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
ok 2274 - runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
  ---
  duration_ms: 16.822381
  ...
# Subtest: runtime: no daily note today still writes the schedule with no Pomodoro chip
ok 2275 - runtime: no daily note today still writes the schedule with no Pomodoro chip
  ---
  duration_ms: 0.782504
  ...
# Subtest: runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
ok 2276 - runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
  ---
  duration_ms: 2.001791
  ...
# Subtest: runtime: vault.process throwing during the daily-note write is reported without throwing
ok 2277 - runtime: vault.process throwing during the daily-note write is reported without throwing
  ---
  duration_ms: 0.991523
  ...
# Subtest: runtime: the daily note open in another editor is written through that editor in its own transaction
ok 2278 - runtime: the daily note open in another editor is written through that editor in its own transaction
  ---
  duration_ms: 2.386165
  ...
# Subtest: runtime: re-running the same deferral gesture is idempotent
ok 2279 - runtime: re-running the same deferral gesture is idempotent
  ---
  duration_ms: 0.907172
  ...
# Subtest: runtime: a counted scheduled batch prunes exactly the targets that land on a future date
ok 2280 - runtime: a counted scheduled batch prunes exactly the targets that land on a future date
  ---
  duration_ms: 3.734397
  ...
# Subtest: runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
ok 2281 - runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
  ---
  duration_ms: 3.694832
  ...
# Subtest: runtime: the source note being today's daily note folds the prune into a single editor transaction
ok 2282 - runtime: the source note being today's daily note folds the prune into a single editor transaction
  ---
  duration_ms: 0.975461
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: bare future scheduled writes block only real supported open inline tasks
ok 2283 - bare future scheduled writes block only real supported open inline tasks
  ---
  duration_ms: 9.912841
  ...
# Subtest: single runtime transclusion toggle preserves viewport in one line transaction
ok 2284 - single runtime transclusion toggle preserves viewport in one line transaction
  ---
  duration_ms: 3.57276
  ...
# Subtest: same-file runtime toggle changes only markers, never fields or statuses
ok 2285 - same-file runtime toggle changes only markers, never fields or statuses
  ---
  duration_ms: 1.378571
  ...
# Subtest: pure toggle leaves a cursor moved during the toggle where it landed
ok 2286 - pure toggle leaves a cursor moved during the toggle where it landed
  ---
  duration_ms: 0.630133
  ...
# Subtest: counted runtime transclusion toggle preserves viewport and caret
ok 2287 - counted runtime transclusion toggle preserves viewport and caret
  ---
  duration_ms: 1.40434
  ...
# Subtest: counted property runtime uses one transaction and preserves caret and viewport
ok 2288 - counted property runtime uses one transaction and preserves caret and viewport
  ---
  duration_ms: 5.831591
  ...
# Subtest: bare due schedule recovery is guarded and can change only task status
ok 2289 - bare due schedule recovery is guarded and can change only task status
  ---
  duration_ms: 3.811407
  ...
# Subtest: counted due recovery applies Ready Next and In Progress in one transaction
ok 2290 - counted due recovery applies Ready Next and In Progress in one transaction
  ---
  duration_ms: 16.119399
  ...
# Subtest: scheduled recovery aborts after an asynchronous source change
ok 2291 - scheduled recovery aborts after an asynchronous source change
  ---
  duration_ms: 1.5506
  ...
# Subtest: counted property runtime aborts a stale batch without a transaction
ok 2292 - counted property runtime aborts a stale batch without a transaction
  ---
  duration_ms: 0.606828
  ...
# Subtest: counted project scheduling writes an inline date and blocks tagged residents
ok 2293 - counted project scheduling writes an inline date and blocks tagged residents
  ---
  duration_ms: 4.783149
  ...
# Subtest: future project scheduling prunes resident links and an emptied Pomodoro
ok 2294 - future project scheduling prunes resident links and an emptied Pomodoro
  ---
  duration_ms: 6.038618
  ...
# Subtest: single project scheduling recovers due residents through the gate
ok 2295 - single project scheduling recovers due residents through the gate
  ---
  duration_ms: 3.539316
  ...
# Subtest: single project schedule deletion removes propagated copies and recovers
ok 2296 - single project schedule deletion removes propagated copies and recovers
  ---
  duration_ms: 3.402405
  ...
# Subtest: formatPriorityRollScheduleReason covers all four shapes
ok 2297 - formatPriorityRollScheduleReason covers all four shapes
  ---
  duration_ms: 2.160955
  ...
# Subtest: the priority-roll picker row keeps range detail and stores the exact roll
ok 2298 - the priority-roll picker row keeps range detail and stores the exact roll
  ---
  duration_ms: 0.975823
  ...
# Subtest: buildPriorityRollScheduleLog returns null when the roll does not move the date
ok 2299 - buildPriorityRollScheduleLog returns null when the roll does not move the date
  ---
  duration_ms: 1.448826
  ...
# Subtest: getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
ok 2300 - getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
  ---
  duration_ms: 1.1158
  ...
# Subtest: a priority roll onto the current date writes the date but no log
ok 2301 - a priority roll onto the current date writes the date but no log
  ---
  duration_ms: 24.758378
  ...
# Subtest: a typed reason on an unchanged date is still written
ok 2302 - a typed reason on an unchanged date is still written
  ---
  duration_ms: 1.258602
  ...
# Subtest: schedule log bullet formatting and parsing round-trip with and without a previous value
ok 2303 - schedule log bullet formatting and parsing round-trip with and without a previous value
  ---
  duration_ms: 4.083565
  ...
# Subtest: formatScheduleLogEntryText renders entry text without indent or marker
ok 2304 - formatScheduleLogEntryText renders entry text without indent or marker
  ---
  duration_ms: 0.276688
  ...
# Subtest: schedule reason text normalization trims, collapses whitespace, and flags inline fields
ok 2305 - schedule reason text normalization trims, collapses whitespace, and flags inline fields
  ---
  duration_ms: 0.462724
  ...
# Subtest: findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
ok 2306 - findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
  ---
  duration_ms: 0.763748
  ...
# Subtest: getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
ok 2307 - getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
  ---
  duration_ms: 0.467082
  ...
# Subtest: planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
ok 2308 - planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
  ---
  duration_ms: 0.661362
  ...
# Subtest: planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
ok 2309 - planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
  ---
  duration_ms: 0.318588
  ...
# Subtest: planScheduleLogEntry uses the fallback only when a marker exists
ok 2310 - planScheduleLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.423999
  ...
# Subtest: a typed reason wins over the fallback
ok 2311 - a typed reason wins over the fallback
  ---
  duration_ms: 0.27221
  ...
# Subtest: the fallback is suppressed on an unchanged date
ok 2312 - the fallback is suppressed on an unchanged date
  ---
  duration_ms: 0.333677
  ...
# Subtest: no reason and no fallback still guards empty-reason
ok 2313 - no reason and no fallback still guards empty-reason
  ---
  duration_ms: 0.216323
  ...
# Subtest: getScheduleLogWriteOutcome maps plan outcomes for writers
ok 2314 - getScheduleLogWriteOutcome maps plan outcomes for writers
  ---
  duration_ms: 0.41391
  ...
# Subtest: hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
ok 2315 - hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
  ---
  duration_ms: 0.219489
  ...
# Subtest: counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
ok 2316 - counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
  ---
  duration_ms: 2.953027
  ...
# Subtest: empty reason through the counted planner writes no schedule log entries
ok 2317 - empty reason through the counted planner writes no schedule log entries
  ---
  duration_ms: 1.012022
  ...
# Subtest: a counted scheduled session logs only the tasks that already keep a log
ok 2318 - a counted scheduled session logs only the tasks that already keep a log
  ---
  duration_ms: 0.69123
  ...
# Subtest: the counted notice wording distinguishes a fallback batch from a typed-reason batch
ok 2319 - the counted notice wording distinguishes a fallback batch from a typed-reason batch
  ---
  duration_ms: 6.568499
  ...
# Subtest: setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
ok 2320 - setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
  ---
  duration_ms: 0.547004
  ...
# Subtest: setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
ok 2321 - setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
  ---
  duration_ms: 6.817663
  ...
# Subtest: priority bullet property config normalizes frozen levels and preserves existing shapes
ok 2322 - priority bullet property config normalizes frozen levels and preserves existing shapes
  ---
  duration_ms: 7.510838
  ...
# Subtest: priority bullet property config rejects each invalid schema category once
ok 2323 - priority bullet property config rejects each invalid schema category once
  ---
  duration_ms: 2.131839
  ...
# Subtest: project scheduling targets the inline ^prj field
ok 2324 - project scheduling targets the inline ^prj field
  ---
  duration_ms: 4.263879
  ...
# Subtest: local task properties are addable only on valid tasks but invalid metadata stays removable
ok 2325 - local task properties are addable only on valid tasks but invalid metadata stays removable
  ---
  duration_ms: 0.697942
  ...
# Subtest: dependency parent write validation rejects stale, Pomodoro, and fenced parents
ok 2326 - dependency parent write validation rejects stale, Pomodoro, and fenced parents
  ---
  duration_ms: 1.179592
  ...
# Subtest: counted property targets mean current plus N real tasks without wrapping
ok 2327 - counted property targets mean current plus N real tasks without wrapping
  ---
  duration_ms: 1.902933
  ...
# Subtest: counted property metadata distinguishes absent, common, and mixed values
ok 2328 - counted property metadata distinguishes absent, common, and mixed values
  ---
  duration_ms: 2.225017
  ...
# Subtest: counted priority metadata reports labels for common and mixed values
ok 2329 - counted priority metadata reports labels for common and mixed values
  ---
  duration_ms: 1.37797
  ...
# Subtest: counted scheduled planning updates the motivating three tasks atomically
ok 2330 - counted scheduled planning updates the motivating three tasks atomically
  ---
  duration_ms: 4.76244
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: project schedule validation accepts only real YYYY-MM-DD dates
ok 2331 - project schedule validation accepts only real YYYY-MM-DD dates
  ---
  duration_ms: 2.896659
  ...
# Subtest: source task schedule is extracted without losing task metadata
ok 2332 - source task schedule is extracted without losing task metadata
  ---
  duration_ms: 5.353849
  ...
# Subtest: source task schedule errors are focused and ambiguous fields fail
ok 2333 - source task schedule errors are focused and ambiguous fields fail
  ---
  duration_ms: 1.102113
  ...
# Subtest: project creation frontmatter never stores the task schedule
ok 2334 - project creation frontmatter never stores the task schedule
  ---
  duration_ms: 0.327014
  ...
# Subtest: future schedule labels use local date-only boundaries
ok 2335 - future schedule labels use local date-only boundaries
  ---
  duration_ms: 1.256698
  ...
# Subtest: scheduled recovery selects current and newest earlier daily across gaps
ok 2336 - scheduled recovery selects current and newest earlier daily across gaps
  ---
  duration_ms: 4.874125
  ...
# Subtest: scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
ok 2337 - scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
  ---
  duration_ms: 71.66233
  ...
# Subtest: scheduled recovery defers incompatible status settings and ambiguous identities
ok 2338 - scheduled recovery defers incompatible status settings and ambiguous identities
  ---
  duration_ms: 11.550597
  ...
# Subtest: scheduled recovery honors custom open and closed Tasks status types
ok 2339 - scheduled recovery honors custom open and closed Tasks status types
  ---
  duration_ms: 2.021098
  ...
# Subtest: scheduled recovery honors the configured Tasks global filter
ok 2340 - scheduled recovery honors the configured Tasks global filter
  ---
  duration_ms: 5.786745
  ...
# Subtest: child picker schedule metadata reads the inline ^prj date
ok 2341 - child picker schedule metadata reads the inline ^prj date
  ---
  duration_ms: 2.188157
  ...
# Subtest: task move destination schedule hydration reads cached ^prj content
ok 2342 - task move destination schedule hydration reads cached ^prj content
  ---
  duration_ms: 5.108563
  ...
# Subtest: project lifecycle task classification requires unfenced \#task with trailing ^prj
ok 2343 - project lifecycle task classification requires unfenced \#task with trailing ^prj
  ---
  duration_ms: 0.542015
  ...
# Subtest: valid Obsidian tasks require a standalone \#task checkbox in real note content
ok 2344 - valid Obsidian tasks require a standalone \#task checkbox in real note content
  ---
  duration_ms: 0.696109
  ...
# Subtest: choosing a scheduled date enters the combined review without writing anything
ok 2345 - choosing a scheduled date enters the combined review without writing anything
  ---
  duration_ms: 27.948959
  ...
# Subtest: choosing a priority level does not enter the schedule review
ok 2346 - choosing a priority level does not enter the schedule review
  ---
  duration_ms: 23.588505
  ...
# Subtest: confirming an empty reason on a task with an existing schedule log appends an unexplained entry
ok 2347 - confirming an empty reason on a task with an existing schedule log appends an unexplained entry
  ---
  duration_ms: 16.283262
  ...
# Subtest: confirming an empty reason on a task with no schedule log writes only the date
ok 2348 - confirming an empty reason on a task with no schedule log writes only the date
  ---
  duration_ms: 9.693724
  ...
# Subtest: review stage getFilteredItems always returns exactly one synthetic preview item
ok 2349 - review stage getFilteredItems always returns exactly one synthetic preview item
  ---
  duration_ms: 2.76613
  ...
# Subtest: the review preview row previews the entry it will write
ok 2350 - the review preview row previews the entry it will write
  ---
  duration_ms: 13.744386
  ...
# Subtest: the review footer flips between Skip optional logs and Apply schedule as the Reason changes
ok 2351 - the review footer flips between Skip optional logs and Apply schedule as the Reason changes
  ---
  duration_ms: 3.765839
  ...
# Subtest: closing the picker during the review clears pending schedule state and writes nothing
ok 2352 - closing the picker during the review clears pending schedule state and writes nothing
  ---
  duration_ms: 3.836383
  ...
# Subtest: scheduling Work Log eligibility requires Pending or Next \#task lines
ok 2353 - scheduling Work Log eligibility requires Pending or Next \#task lines
  ---
  duration_ms: 2.160925
  ...
# Subtest: single Pending explicit date opens one review and writes both logs
ok 2354 - single Pending explicit date opens one review and writes both logs
  ---
  duration_ms: 40.911483
  ...
# Subtest: single Next blank and whitespace summaries schedule without a Work Log
ok 2355 - single Next blank and whitespace summaries schedule without a Work Log
  ---
  duration_ms: 10.132642
  ...
# Subtest: Escape at the review writes nothing, with or without typed text
ok 2356 - Escape at the review writes nothing, with or without typed text
  ---
  duration_ms: 21.201278
  ...
# Subtest: Ready and Blocked explicit dates review the Reason with no Work summary field
ok 2357 - Ready and Blocked explicit dates review the Reason with no Work summary field
  ---
  duration_ms: 13.018951
  ...
# Subtest: future scheduling on Pending marks Blocked but still writes the Work Log
ok 2358 - future scheduling on Pending marks Blocked but still writes the Work Log
  ---
  duration_ms: 5.396541
  ...
# Subtest: today date on Pending still offers the Work Log
ok 2359 - today date on Pending still offers the Work Log
  ---
  duration_ms: 4.76674
  ...
# Subtest: priority pick on Pending freezes its roll and offers the Work Log
ok 2360 - priority pick on Pending freezes its roll and offers the Work Log
  ---
  duration_ms: 7.474277
  ...
# Subtest: counted mixed statuses share one summary only on Pending and Next
ok 2361 - counted mixed statuses share one summary only on Pending and Next
  ---
  duration_ms: 14.438189
  ...
# Subtest: counted planner composes Schedule and Work Logs bottom-up above later targets
ok 2362 - counted planner composes Schedule and Work Logs bottom-up above later targets
  ---
  duration_ms: 1.647905
  ...
# Subtest: counted planner writes a Work Log even when the date is unchanged
ok 2363 - counted planner writes a Work Log even when the date is unchanged
  ---
  duration_ms: 0.443477
  ...
# Subtest: scheduling Work Log ownership keeps nested logs and CRLF endings
ok 2364 - scheduling Work Log ownership keeps nested logs and CRLF endings
  ---
  duration_ms: 0.83831
  ...
# Subtest: scheduling Work Log warns on :: and preserves Markdown
ok 2365 - scheduling Work Log warns on :: and preserves Markdown
  ---
  duration_ms: 3.455166
  ...
# Subtest: stale task while reviewing refuses with no scheduling or log writes
ok 2366 - stale task while reviewing refuses with no scheduling or log writes
  ---
  duration_ms: 4.305778
  ...
# Subtest: scheduling prompts never leak into lane or cancel stages
ok 2367 - scheduling prompts never leak into lane or cancel stages
  ---
  duration_ms: 6.593655
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: Pomodoro-marked links are not managed dependency bullets
ok 2368 - Pomodoro-marked links are not managed dependency bullets
  ---
  duration_ms: 2.813992
  ...
# Subtest: deleting inline scheduled metadata recovers Blocked targets by snapshot rank
ok 2369 - deleting inline scheduled metadata recovers Blocked targets by snapshot rank
  ---
  duration_ms: 7.535133
  ...
# Subtest: counted future scheduling blocks only supported open inline task statuses
ok 2370 - counted future scheduling blocks only supported open inline task statuses
  ---
  duration_ms: 3.082685
  ...
# Subtest: counted property planning rejects any stale source with no partial result
ok 2371 - counted property planning rejects any stale source with no partial result
  ---
  duration_ms: 0.392209
  ...
# Subtest: counted project scheduling writes the ^prj inline date and blocks tagged residents
ok 2372 - counted project scheduling writes the ^prj inline date and blocks tagged residents
  ---
  duration_ms: 3.171134
  ...
# Subtest: moving a project schedule earlier replaces only exact old-date copies
ok 2373 - moving a project schedule earlier replaces only exact old-date copies
  ---
  duration_ms: 0.550881
  ...
# Subtest: future project schedules block every open resident and consume review status
ok 2374 - future project schedules block every open resident and consume review status
  ---
  duration_ms: 1.084941
  ...
# Subtest: due project dates recover residents through the gate and write unblocked markers
ok 2375 - due project dates recover residents through the gate and write unblocked markers
  ---
  duration_ms: 0.845073
  ...
# Subtest: schedule deletion removes only exact project-date copies and recovers residents
ok 2376 - schedule deletion removes only exact project-date copies and recovers residents
  ---
  duration_ms: 1.189691
  ...
# Subtest: dependency lines render one canonical Depends-On line per parent
ok 2377 - dependency lines render one canonical Depends-On line per parent
  ---
  duration_ms: 0.902292
  ...
# Subtest: dependency IDs encode root and nested Markdown paths deterministically
ok 2378 - dependency IDs encode root and nested Markdown paths deterministically
  ---
  duration_ms: 1.573674
  ...
# Subtest: prompted block IDs truthfully replace legacy id fields
ok 2379 - prompted block IDs truthfully replace legacy id fields
  ---
  duration_ms: 0.343536
  ...
# Subtest: dependency navigation identity includes note path and folds legacy children
ok 2380 - dependency navigation identity includes note path and folds legacy children
  ---
  duration_ms: 1.762665
  ...
# Subtest: retired dependency bullets are excluded from single and counted toggles
ok 2381 - retired dependency bullets are excluded from single and counted toggles
  ---
  duration_ms: 2.363451
  ...
# Subtest: dependsOn replacement accepts spaces around field name and separator
ok 2382 - dependsOn replacement accepts spaces around field name and separator
  ---
  duration_ms: 0.550721
  ...
# Subtest: task status helpers keep Blocked open but rankless
ok 2383 - task status helpers keep Blocked open but rankless
  ---
  duration_ms: 0.882916
  ...
# Subtest: a due project date with only closed Depends-On history strips the tag
ok 2384 - a due project date with only closed Depends-On history strips the tag
  ---
  duration_ms: 1.437114
  ...
# Subtest: Ctrl+D with only closed Depends-On history strips the tag
ok 2385 - Ctrl+D with only closed Depends-On history strips the tag
  ---
  duration_ms: 4.326719
  ...
# Subtest: Ctrl+D with an open Depends-On link remaining keeps the tag
ok 2386 - Ctrl+D with an open Depends-On link remaining keeps the tag
  ---
  duration_ms: 0.671402
  ...
# Subtest: counted ^prj schedule sessions write [unblocked::] when the writer is passed
ok 2387 - counted ^prj schedule sessions write [unblocked::] when the writer is passed
  ---
  duration_ms: 1.174842
  ...
# Subtest: a due project date keeps the tag while ^prj holds Depends-On links
ok 2388 - a due project date keeps the tag while ^prj holds Depends-On links
  ---
  duration_ms: 1.297868
  ...
# Subtest: a due project date strips the tag while a resident with its own reason stays Blocked
ok 2389 - a due project date strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.536213
  ...
# Subtest: Ctrl+D strips the tag while a resident with its own reason stays Blocked
ok 2390 - Ctrl+D strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.514542
  ...
# Subtest: counted scheduled deletes recover with [unblocked::] when the writer is passed
ok 2391 - counted scheduled deletes recover with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.555289
  ...
# Subtest: section-header navigation moves normally and cycles at boundaries
ok 2392 - section-header navigation moves normally and cycles at boundaries
  ---
  duration_ms: 5.27064
  ...
# Subtest: section-header navigation wraps from beyond document boundaries
ok 2393 - section-header navigation wraps from beyond document boundaries
  ---
  duration_ms: 0.423949
  ...
# Subtest: section-header navigation handles single-header and no-header notes
ok 2394 - section-header navigation handles single-header and no-header notes
  ---
  duration_ms: 0.448206
  ...
# Subtest: open-task navigation scan includes Ready In Progress and Next and excludes Blocked
ok 2395 - open-task navigation scan includes Ready In Progress and Next and excludes Blocked
  ---
  duration_ms: 0.950845
  ...
# Subtest: open-task navigation keeps existing Pomodoro ledger targets
ok 2396 - open-task navigation keeps existing Pomodoro ledger targets
  ---
  duration_ms: 0.98519
  ...
# Subtest: next and previous jumps skip Blocked tasks and wrap to an allowed task
ok 2397 - next and previous jumps skip Blocked tasks and wrap to an allowed task
  ---
  duration_ms: 0.499814
  ...
# Subtest: blocked-only notes and a sole current allowed task have no jump target
ok 2398 - blocked-only notes and a sole current allowed task have no jump target
  ---
  duration_ms: 0.291687
  ...
# Subtest: counted open-task jumps select the Nth eligible target and wrap modulo the list
ok 2399 - counted open-task jumps select the Nth eligible target and wrap modulo the list
  ---
  duration_ms: 0.605115
  ...
# Subtest: counted open-task jumps keep sole-target and invalid-repeat behavior
ok 2400 - counted open-task jumps keep sole-target and invalid-repeat behavior
  ---
  duration_ms: 0.578094
  ...
# Subtest: tab pin Vim action registers once and toggles only the active leaf once
ok 2401 - tab pin Vim action registers once and toggles only the active leaf once
  ---
  duration_ms: 6.132225
  ...
# Subtest: tab pin toggle fails safely without a supported active leaf
ok 2402 - tab pin toggle fails safely without a supported active leaf
  ---
  duration_ms: 0.396928
  ...
# Subtest: close tabs left preserves pinned sibling tabs and refocuses active tab
ok 2403 - close tabs left preserves pinned sibling tabs and refocuses active tab
  ---
  duration_ms: 1.246519
  ...
# Subtest: close tabs right preserves pinned siblings and ignores the left side
ok 2404 - close tabs right preserves pinned siblings and ignores the left side
  ---
  duration_ms: 0.510455
  ...
# Subtest: close other tabs preserves pinned siblings on both sides
ok 2405 - close other tabs preserves pinned siblings on both sides
  ---
  duration_ms: 0.562935
  ...
# Subtest: close sibling tabs is a silent no-op when the scoped range is all pinned
ok 2406 - close sibling tabs is a silent no-op when the scoped range is all pinned
  ---
  duration_ms: 0.40352
  ...
# Subtest: close sibling tabs honors every pinned leaf representation
ok 2407 - close sibling tabs honors every pinned leaf representation
  ---
  duration_ms: 6.06708
  ...
# Subtest: close sibling tabs treats throwing view state as unpinned
ok 2408 - close sibling tabs treats throwing view state as unpinned
  ---
  duration_ms: 0.489465
  ...
# Subtest: tab pin Vim registration retries after adapter availability
ok 2409 - tab pin Vim registration retries after adapter availability
  ---
  duration_ms: 1.27266
  ...
# Subtest: isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
ok 2410 - isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
  ---
  duration_ms: 13.731841
  ...
# Subtest: isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
ok 2411 - isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
  ---
  duration_ms: 1.882514
  ...
# Subtest: isPomodoroTaskLinkLine refuses Depends-On lines and prose links
ok 2412 - isPomodoroTaskLinkLine refuses Depends-On lines and prose links
  ---
  duration_ms: 0.430582
  ...
# Subtest: decideTaskLinkLaneMode starts when any target is Next
ok 2413 - decideTaskLinkLaneMode starts when any target is Next
  ---
  duration_ms: 0.328557
  ...
# Subtest: taskLinkLaneRefusalFor renders every D5 refusal
ok 2414 - taskLinkLaneRefusalFor renders every D5 refusal
  ---
  duration_ms: 0.292538
  ...
# Subtest: planTaskLinkLaneBatch starts Next targets and leaves the rest alone
ok 2415 - planTaskLinkLaneBatch starts Next targets and leaves the rest alone
  ---
  duration_ms: 2.816686
  ...
# Subtest: planTaskLinkLaneBatch pauses with one shared Work Log entry
ok 2416 - planTaskLinkLaneBatch pauses with one shared Work Log entry
  ---
  duration_ms: 1.500854
  ...
# Subtest: planTaskLinkLaneBatch applies the freshness stamp last
ok 2417 - planTaskLinkLaneBatch applies the freshness stamp last
  ---
  duration_ms: 0.388601
  ...
# Subtest: planTaskLinkLaneBatch dedupes lines and refuses stale preimages
ok 2418 - planTaskLinkLaneBatch dedupes lines and refuses stale preimages
  ---
  duration_ms: 0.773417
  ...
# Subtest: buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
ok 2419 - buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
  ---
  duration_ms: 1.950643
  ...
# Subtest: taskLinkLanePromptState drives the Move to Next prompt
ok 2420 - taskLinkLanePromptState drives the Move to Next prompt
  ---
  duration_ms: 0.488643
  ...
# Subtest: TaskLinkLanePromptModal submits, previews live, and cancels silently
ok 2421 - TaskLinkLanePromptModal submits, previews live, and cancels silently
  ---
  duration_ms: 3.523225
  ...
# Subtest: TaskLinkLanePromptModal renders the batch context card
ok 2422 - TaskLinkLanePromptModal renders the batch context card
  ---
  duration_ms: 0.745082
  ...
# Subtest: findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
ok 2423 - findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
  ---
  duration_ms: 0.821157
  ...
# Subtest: L1: toggle starts a Next link, stamps, hints, and notices
ok 2424 - L1: toggle starts a Next link, stamps, hints, and notices
  ---
  duration_ms: 7.54892
  ...
# Subtest: L2/L3: toggle pauses through the prompt, logging one shared entry
ok 2425 - L2/L3: toggle pauses through the prompt, logging one shared entry
  ---
  duration_ms: 34.785689
  ...
# Subtest: L4: cancelling the prompt writes nothing and shows no Notice
ok 2426 - L4: cancelling the prompt writes nothing and shows no Notice
  ---
  duration_ms: 2.177997
  ...
# Subtest: L5: both directions run the same toggle twice for a round trip
ok 2427 - L5: both directions run the same toggle twice for a round trip
  ---
  duration_ms: 2.555037
  ...
# Subtest: L6: Ready, Blocked, done, and cancelled targets are refused
ok 2428 - L6: Ready, Blocked, done, and cancelled targets are refused
  ---
  duration_ms: 2.371097
  ...
# Subtest: L6: missing targets keep the existing resolver error
ok 2429 - L6: missing targets keep the existing resolver error
  ---
  duration_ms: 0.774288
  ...
# Subtest: L7: a counted start flips every Next sibling and leaves In Progress alone
ok 2430 - L7: a counted start flips every Next sibling and leaves In Progress alone
  ---
  duration_ms: 1.394322
  ...
# Subtest: L8: a counted pause prompts once and skips Blocked with a count
ok 2431 - L8: a counted pause prompts once and skips Blocked with a count
  ---
  duration_ms: 3.30602
  ...
# Subtest: L9: an over-long count clamps at the entry end without error
ok 2432 - L9: an over-long count clamps at the entry end without error
  ---
  duration_ms: 1.997492
  ...
# Subtest: L10: a closed-entry history line toggles the task and keeps the line
ok 2433 - L10: a closed-entry history line toggles the task and keeps the line
  ---
  duration_ms: 0.841456
  ...
# Subtest: L11: a target edited while the prompt is open refuses stale
ok 2434 - L11: a target edited while the prompt is open refuses stale
  ---
  duration_ms: 3.681867
  ...
# Subtest: L12: an embedded Pomodoro link takes the two-state toggle
ok 2435 - L12: an embedded Pomodoro link takes the two-state toggle
  ---
  duration_ms: 1.60295
  ...
# Subtest: L14: the same task linked twice in a batch is written once
ok 2436 - L14: the same task linked twice in a batch is written once
  ---
  duration_ms: 8.791241
  ...
# Subtest: L15: a second toggle while one is in flight is swallowed as busy
ok 2437 - L15: a second toggle while one is in flight is swallowed as busy
  ---
  duration_ms: 1.938901
  ...
# Subtest: toggle on a non-link line refuses without writing
ok 2438 - toggle on a non-link line refuses without writing
  ---
  duration_ms: 3.357059
  ...
# Subtest: api.taskLinkLane is a frozen v1 namespace that never throws
ok 2439 - api.taskLinkLane is a frozen v1 namespace that never throws
  ---
  duration_ms: 2.141788
  ...
# Subtest: the progressMarks hint is a no-op without the ledger-tools api
ok 2440 - the progressMarks hint is a no-op without the ledger-tools api
  ---
  duration_ms: 0.592761
  ...
# Subtest: task move records one Vim jump and round-trips without extra writes
ok 2441 - task move records one Vim jump and round-trips without extra writes
  ---
  duration_ms: 24.125221
  ...
# Subtest: counted task move records a single jump to the first moved task
ok 2442 - counted task move records a single jump to the first moved task
  ---
  duration_ms: 3.443162
  ...
# Subtest: deferred task landing re-anchors and records the resolved cursor once
ok 2443 - deferred task landing re-anchors and records the resolved cursor once
  ---
  duration_ms: 15.021193
  ...
# Subtest: failed task move preserves seeded history including the forward branch
ok 2444 - failed task move preserves seeded history including the forward branch
  ---
  duration_ms: 1.066175
  ...
# Subtest: post-commit open failure keeps the move committed with no jump
ok 2445 - post-commit open failure keeps the move committed with no jump
  ---
  duration_ms: 2.175002
  ...
# Subtest: a newer move supersedes a pending landing without stale placement
ok 2446 - a newer move supersedes a pending landing without stale placement
  ---
  duration_ms: 11.343922
  ...
# Subtest: shared destination helper without a move context records no jump
ok 2447 - shared destination helper without a move context records no jump
  ---
  duration_ms: 1.342994
  ...
# Subtest: task moves carry the Depends-On line and repath stranded same-note links
ok 2448 - task moves carry the Depends-On line and repath stranded same-note links
  ---
  duration_ms: 12.050251
  ...
# Subtest: task moves keep pathless links when the target moves along
ok 2449 - task moves keep pathless links when the target moves along
  ---
  duration_ms: 1.784646
  ...
# Subtest: counted task moves discover movable tasks without wrapping or examples
ok 2450 - counted task moves discover movable tasks without wrapping or examples
  ---
  duration_ms: 2.287697
  ...
# Subtest: task move ranges preserve quoted subtrees and collapse overlapping selections
ok 2451 - task move ranges preserve quoted subtrees and collapse overlapping selections
  ---
  duration_ms: 0.988166
  ...
# Subtest: task move removal handles disjoint ranges, blank seams, and CRLF
ok 2452 - task move removal handles disjoint ranges, blank seams, and CRLF
  ---
  duration_ms: 0.616056
  ...
# Subtest: task move destinations include areas and only open projects
ok 2453 - task move destinations include areas and only open projects
  ---
  duration_ms: 1.013966
  ...
# Subtest: moves into a blocked project leave closed tagged lines alone
ok 2454 - moves into a blocked project leave closed tagged lines alone
  ---
  duration_ms: 4.075208
  ...
# Subtest: moves into a blocked project promote open prerequisites to the moved lane
ok 2455 - moves into a blocked project promote open prerequisites to the moved lane
  ---
  duration_ms: 4.000506
  ...
# Subtest: task move insertion preserves exact task and section spacing
ok 2456 - task move insertion preserves exact task and section spacing
  ---
  duration_ms: 5.232397
  ...
# Subtest: task move planning migrates identities and links across every affected note
ok 2457 - task move planning migrates identities and links across every affected note
  ---
  duration_ms: 6.188854
  ...
# Subtest: task move planning exposes a destination anchor for area destinations and counted moves
ok 2458 - task move planning exposes a destination anchor for area destinations and counted moves
  ---
  duration_ms: 0.95855
  ...
# Subtest: task move into a blocked project tags the moved task and consumes today's live Pomodoro link
ok 2459 - task move into a blocked project tags the moved task and consumes today's live Pomodoro link
  ---
  duration_ms: 6.251301
  ...
# Subtest: task move out of a blocked project recovers through the shared gate and writes the unblocked mark
ok 2460 - task move out of a blocked project recovers through the shared gate and writes the unblocked mark
  ---
  duration_ms: 7.086778
  ...
# Subtest: move promotion walks through a ^prj target without raising it
ok 2461 - move promotion walks through a ^prj target without raising it
  ---
  duration_ms: 11.688621
  ...
# Subtest: move promotion walks through a [?] ^prj to its open prerequisite
ok 2462 - move promotion walks through a [?] ^prj to its open prerequisite
  ---
  duration_ms: 1.333015
  ...
# Subtest: move promotion uses each open task's own lane, not the strongest moved lane
ok 2463 - move promotion uses each open task's own lane, not the strongest moved lane
  ---
  duration_ms: 1.795157
  ...
# Subtest: move promotion skips Depends-On lines of closed tasks
ok 2464 - move promotion skips Depends-On lines of closed tasks
  ---
  duration_ms: 1.302225
  ...
# Subtest: task move planning rejects destination collisions and malformed identities
ok 2465 - task move planning rejects destination collisions and malformed identities
  ---
  duration_ms: 0.858589
  ...
# Subtest: resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
ok 2466 - resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
  ---
  duration_ms: 0.794125
  ...
# Subtest: focusTaskMoveDestination opens the destination file and anchors the cursor
ok 2467 - focusTaskMoveDestination opens the destination file and anchors the cursor
  ---
  duration_ms: 2.165253
  ...
# Subtest: focusTaskMoveDestination returns false without moving the cursor when the open fails
ok 2468 - focusTaskMoveDestination returns false without moving the cursor when the open fails
  ---
  duration_ms: 0.323608
  ...
# Subtest: focusTaskMoveDestination re-anchors by block ID when the destination content drifted
ok 2469 - focusTaskMoveDestination re-anchors by block ID when the destination content drifted
  ---
  duration_ms: 0.483984
  ...
# Subtest: physical task move chord declines auto-repeat and consumes Vim normal input once
ok 2470 - physical task move chord declines auto-repeat and consumes Vim normal input once
  ---
  duration_ms: 1.474133
  ...
# Subtest: counted task move dispatch keeps its count through cold async destinations
ok 2471 - counted task move dispatch keeps its count through cold async destinations
  ---
  duration_ms: 35.049914
  ...
# Subtest: counted task move dispatch with warm async destinations opens one counted picker
ok 2472 - counted task move dispatch with warm async destinations opens one counted picker
  ---
  duration_ms: 8.493953
  ...
# Subtest: bare task move command ignores stale Vim count outside normal mode
ok 2473 - bare task move command ignores stale Vim count outside normal mode
  ---
  duration_ms: 2.019375
  ...
# Subtest: bare task move command opens one uncounted target in Vim normal mode
ok 2474 - bare task move command opens one uncounted target in Vim normal mode
  ---
  duration_ms: 1.363744
  ...
# Subtest: already handled task move event leaves pending Vim state alone
ok 2475 - already handled task move event leaves pending Vim state alone
  ---
  duration_ms: 0.456541
  ...
# Subtest: counted task move command dispatch counts Pomodoro sub-bullets once
ok 2476 - counted task move command dispatch counts Pomodoro sub-bullets once
  ---
  duration_ms: 6.781914
  ...
# Subtest: physical transclusion toggle owns bare and counted Vim normal input
ok 2477 - physical transclusion toggle owns bare and counted Vim normal input
  ---
  duration_ms: 3.503557
  ...
# Subtest: runtime task move writes destination before source and rolls back source failures
ok 2478 - runtime task move writes destination before source and rolls back source failures
  ---
  duration_ms: 5.722194
  ...
# Subtest: runtime task move groups open-editor source and destination changes
ok 2479 - runtime task move groups open-editor source and destination changes
  ---
  duration_ms: 4.095256
  ...
# Subtest: runtime task move guards destination, auxiliary, and rollback failures
ok 2480 - runtime task move guards destination, auxiliary, and rollback failures
  ---
  duration_ms: 3.382656
  ...
# Subtest: task move insertion separates the section's first task from preamble and placeholders
ok 2481 - task move insertion separates the section's first task from preamble and placeholders
  ---
  duration_ms: 0.66023
  ...
# Subtest: task move insertion keeps populated sections compact and second moves stable
ok 2482 - task move insertion keeps populated sections compact and second moves stable
  ---
  duration_ms: 0.320963
  ...
# Subtest: task move planning separates a counted move into a count-only section
ok 2483 - task move planning separates a counted move into a count-only section
  ---
  duration_ms: 0.903725
  ...
# Subtest: runtime counted move into a count-only section focuses the first moved task
ok 2484 - runtime counted move into a count-only section focuses the first moved task
  ---
  duration_ms: 1.71333
  ...
# Subtest: absent local key with folder template writes the trigger and one notice
ok 2485 - absent local key with folder template writes the trigger and one notice
  ---
  duration_ms: 4.045032
  ...
# Subtest: existing local object keeps other keys and only adds the trigger
ok 2486 - existing local object keeps other keys and only adds the trigger
  ---
  duration_ms: 0.274183
  ...
# Subtest: stored true is already-enabled with no write and no notice
ok 2487 - stored true is already-enabled with no write and no notice
  ---
  duration_ms: 0.239166
  ...
# Subtest: stored false is device-opt-out with no write and no notice
ok 2488 - stored false is device-opt-out with no write and no notice
  ---
  duration_ms: 0.343916
  ...
# Subtest: mode none and blank folder templates skip as no-creation-templates
ok 2489 - mode none and blank folder templates skip as no-creation-templates
  ---
  duration_ms: 0.287368
  ...
# Subtest: regex mode with a non-empty file template enables
ok 2490 - regex mode with a non-empty file template enables
  ---
  duration_ms: 0.258243
  ...
# Subtest: legacy settings without a mode key skip as legacy-templater
ok 2491 - legacy settings without a mode key skip as legacy-templater
  ---
  duration_ms: 0.332304
  ...
# Subtest: missing Templater plugin or settings skip as no-templater without throwing
ok 2492 - missing Templater plugin or settings skip as no-templater without throwing
  ---
  duration_ms: 0.423629
  ...
# Subtest: missing loadLocalStorage or saveLocalStorage returns without throwing
ok 2493 - missing loadLocalStorage or saveLocalStorage returns without throwing
  ---
  duration_ms: 0.378312
  ...
# Subtest: string or array stored local values skip as unknown-local-shape
ok 2494 - string or array stored local values skip as unknown-local-shape
  ---
  duration_ms: 0.451812
  ...
# Subtest: saveLocalStorage throw shows one failure notice and does not escape
ok 2495 - saveLocalStorage throw shows one failure notice and does not escape
  ---
  duration_ms: 0.396306
  ...
# Subtest: planTemplaterLocalTrigger covers helper cases and never adds extra keys
ok 2496 - planTemplaterLocalTrigger covers helper cases and never adds extra keys
  ---
  duration_ms: 0.302728
  ...
# Subtest: unblocked model returns null when there is nothing to show
ok 2497 - unblocked model returns null when there is nothing to show
  ---
  duration_ms: 3.167987
  ...
# Subtest: unblocked card renders a single linked row with receipt and chips
ok 2498 - unblocked card renders a single linked row with receipt and chips
  ---
  duration_ms: 3.247089
  ...
# Subtest: unblocked card renders several linked rows with one entry
ok 2499 - unblocked card renders several linked rows with one entry
  ---
  duration_ms: 0.65476
  ...
# Subtest: unblocked card renders a created continuation with next up
ok 2500 - unblocked card renders a created continuation with next up
  ---
  duration_ms: 0.685138
  ...
# Subtest: unblocked card renders recovered-only and still-blocked rows
ok 2501 - unblocked card renders recovered-only and still-blocked rows
  ---
  duration_ms: 4.558021
  ...
# Subtest: current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
ok 2502 - current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
  ---
  duration_ms: 1.40396
  ...
# Subtest: project pull-in rows label empty projects and preserve project blocking reasons
ok 2503 - project pull-in rows label empty projects and preserve project blocking reasons
  ---
  duration_ms: 1.813511
  ...
# Subtest: unblocked card caps visible rows with +N more
ok 2504 - unblocked card caps visible rows with +N more
  ---
  duration_ms: 0.557754
  ...
# Subtest: unblocked card renders the breaker variant
ok 2505 - unblocked card renders the breaker variant
  ---
  duration_ms: 0.795749
  ...
# Subtest: unblocked card renders the failure variant
ok 2506 - unblocked card renders the failure variant
  ---
  duration_ms: 0.525974
  ...
# Subtest: unblocked rows open their task without dismissing the notice
ok 2507 - unblocked rows open their task without dismissing the notice
  ---
  duration_ms: 2.413947
  ...
# Subtest: unblocked row without a block id opens the note path
ok 2508 - unblocked row without a block id opens the note path
  ---
  duration_ms: 0.641104
  ...
# Subtest: unblocked card omits the plan chip when daily content is null
ok 2509 - unblocked card omits the plan chip when daily content is null
  ---
  duration_ms: 0.446332
  ...
# Subtest: unblocked notice shows one card with duration through showNotice
ok 2510 - unblocked notice shows one card with duration through showNotice
  ---
  duration_ms: 0.644741
  ...
# Subtest: unblocked notice falls back to plain text without a DOM
ok 2511 - unblocked notice falls back to plain text without a DOM
  ---
  duration_ms: 0.314941
  ...
# Subtest: unblocked text truncates to 48 characters with an ellipsis
ok 2512 - unblocked text truncates to 48 characters with an ellipsis
  ---
  duration_ms: 0.355188
  ...
# Subtest: nav api exposes additive notice v1 and keeps version 3
ok 2513 - nav api exposes additive notice v1 and keeps version 3
  ---
  duration_ms: 0.762355
  ...
# Subtest: unblocked stylesheet scopes notice overrides and uses task tokens
ok 2514 - unblocked stylesheet scopes notice overrides and uses task tokens
  ---
  duration_ms: 5.02436
  ...
# Subtest: physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
ok 2515 - physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
  ---
  duration_ms: 5.65276
  ...
# Subtest: open-task command ids omit repeat so the shared route resolves the pending Vim count
ok 2516 - open-task command ids omit repeat so the shared route resolves the pending Vim count
  ---
  duration_ms: 3.349555
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
ok 2517 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
  ---
  duration_ms: 10.049513
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
ok 2518 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
  ---
  duration_ms: 1.432244
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
ok 2519 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
  ---
  duration_ms: 2.313807
  ...
# Subtest: dispatch guard applies a command-route Vim count when the capture route fires second
ok 2520 - dispatch guard applies a command-route Vim count when the capture route fires second
  ---
  duration_ms: 7.269507
  ...
# Subtest: dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
ok 2521 - dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
  ---
  duration_ms: 1.907941
  ...
# Subtest: command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
ok 2522 - command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
  ---
  duration_ms: 1.05314
  ...
# Subtest: command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
ok 2523 - command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
  ---
  duration_ms: 3.931494
  ...
# Subtest: command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
ok 2524 - command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
  ---
  duration_ms: 1.741484
  ...
# Subtest: explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
ok 2525 - explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
  ---
  duration_ms: 1.133434
  ...
# Subtest: getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
ok 2526 - getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
  ---
  duration_ms: 0.520414
  ...
# Subtest: physical counted property chord consumes only explicit normal-mode Vim counts
ok 2527 - physical counted property chord consumes only explicit normal-mode Vim counts
  ---
  duration_ms: 1.258642
  ...
# Subtest: physical counted relation and dependency chords route or refuse by direction
ok 2528 - physical counted relation and dependency chords route or refuse by direction
  ---
  duration_ms: 1.438145
  ...
# Subtest: onload registers the palette command without a default hotkey
ok 2529 - onload registers the palette command without a default hotkey
  ---
  duration_ms: 4.025594
  ...
# Subtest: an embed and a plain image link open the resolved vault resource
ok 2530 - an embed and a plain image link open the resolved vault resource
  ---
  duration_ms: 6.683747
  ...
# Subtest: no image, a missing image, and Reading view show notices without opening
ok 2531 - no image, a missing image, and Reading view show notices without opening
  ---
  duration_ms: 0.808293
  ...
# Subtest: a second command invocation is ignored while the viewer is open
ok 2532 - a second command invocation is ignored while the viewer is open
  ---
  duration_ms: 0.425773
  ...
# Subtest: closing restores focus and leaves an unchanged selection and scroll alone
ok 2533 - closing restores focus and leaves an unchanged selection and scroll alone
  ---
  duration_ms: 0.503892
  ...
# Subtest: closing restores moved selection and scroll only while the source view is active
ok 2534 - closing restores moved selection and scroll only while the source view is active
  ---
  duration_ms: 1.062418
  ...
# Subtest: unload closes the active viewer without restoring editor focus
ok 2535 - unload closes the active viewer without restoring editor focus
  ---
  duration_ms: 0.901411
  ...
# Subtest: parser finds vault embed with size hint
ok 2536 - parser finds vault embed with size hint
  ---
  duration_ms: 3.601956
  ...
# Subtest: parser finds plain image wikilink and blockquoted embed
ok 2537 - parser finds plain image wikilink and blockquoted embed
  ---
  duration_ms: 0.449999
  ...
# Subtest: parser ignores callout bracket and finds the embed
ok 2538 - parser ignores callout bracket and finds the embed
  ---
  duration_ms: 0.683865
  ...
# Subtest: parser ignores image links inside single and double backticks
ok 2539 - parser ignores image links inside single and double backticks
  ---
  duration_ms: 1.836095
  ...
# Subtest: non-image wiki targets are recognized but not candidates
ok 2540 - non-image wiki targets are recognized but not candidates
  ---
  duration_ms: 0.438217
  ...
# Subtest: parser finds two image refs and lines with no refs
ok 2541 - parser finds two image refs and lines with no refs
  ---
  duration_ms: 0.279443
  ...
# Subtest: parser handles Markdown angle, title, and balanced parens
ok 2542 - parser handles Markdown angle, title, and balanced parens
  ---
  duration_ms: 0.643819
  ...
# Subtest: picker uses containing, next, then previous rule
ok 2543 - picker uses containing, next, then previous rule
  ---
  duration_ms: 0.509873
  ...
# Subtest: resolution records sourcePath and resolves duplicate basenames
ok 2544 - resolution records sourcePath and resolves duplicate basenames
  ---
  duration_ms: 1.583262
  ...
# Subtest: resolution handles relative, unicode, and space names
ok 2545 - resolution handles relative, unicode, and space names
  ---
  duration_ms: 0.647286
  ...
# Subtest: missing file, non-image cursor, and fenced lines show exact notices
ok 2546 - missing file, non-image cursor, and fenced lines show exact notices
  ---
  duration_ms: 0.505354
  ...
# Subtest: vault resolution calls getResourcePath with the resolved file
ok 2547 - vault resolution calls getResourcePath with the resolved file
  ---
  duration_ms: 0.284533
  ...
# Subtest: http embed passes through and non-image urls are not candidates
ok 2548 - http embed passes through and non-image urls are not candidates
  ---
  duration_ms: 0.917271
  ...
# Subtest: remote URLs keep original bytes while titles decode once
ok 2549 - remote URLs keep original bytes while titles decode once
  ---
  duration_ms: 1.05296
  ...
# Subtest: escaped Markdown parentheses resolve to the unescaped vault file
ok 2550 - escaped Markdown parentheses resolve to the unescaped vault file
  ---
  duration_ms: 0.640262
  ...
# Subtest: vault percent escapes decode exactly once
ok 2551 - vault percent escapes decode exactly once
  ---
  duration_ms: 0.614573
  ...
# Subtest: extensionless http(s) needs Markdown image syntax
ok 2552 - extensionless http(s) needs Markdown image syntax
  ---
  duration_ms: 0.475106
  ...
# Subtest: fit never exceeds 1 and respects padding for landscape, portrait, and tiny images
ok 2553 - fit never exceeds 1 and respects padding for landscape, portrait, and tiny images
  ---
  duration_ms: 2.27357
  ...
# Subtest: min and max bounds follow fit, 1:1, and the max factor
ok 2554 - min and max bounds follow fit, 1:1, and the max factor
  ---
  duration_ms: 0.314821
  ...
# Subtest: stepping clamps at both bounds
ok 2555 - stepping clamps at both bounds
  ---
  duration_ms: 0.833
  ...
# Subtest: zoom-at-point keeps the point fixed
ok 2556 - zoom-at-point keeps the point fixed
  ---
  duration_ms: 0.258163
  ...
# Subtest: clamp centres small axes and limits large ones
ok 2557 - clamp centres small axes and limits large ones
  ---
  duration_ms: 0.367471
  ...
# Subtest: key Escape → close
ok 2558 - key Escape → close
  ---
  duration_ms: 1.640291
  ...
# Subtest: key q → close
ok 2559 - key q → close
  ---
  duration_ms: 0.177679
  ...
# Subtest: key Q → close
ok 2560 - key Q → close
  ---
  duration_ms: 0.155697
  ...
# Subtest: key Ctrl+[ → close
ok 2561 - key Ctrl+[ → close
  ---
  duration_ms: 0.342904
  ...
# Subtest: key Z → close
ok 2562 - key Z → close
  ---
  duration_ms: 0.312617
  ...
# Subtest: key + → zoomIn
ok 2563 - key + → zoomIn
  ---
  duration_ms: 0.583795
  ...
# Subtest: key = → zoomIn
ok 2564 - key = → zoomIn
  ---
  duration_ms: 0.172198
  ...
# Subtest: key Shift+= → zoomIn
ok 2565 - key Shift+= → zoomIn
  ---
  duration_ms: 0.160646
  ...
# Subtest: key Shift++ → zoomIn
ok 2566 - key Shift++ → zoomIn
  ---
  duration_ms: 0.259616
  ...
# Subtest: key - → zoomOut
ok 2567 - key - → zoomOut
  ---
  duration_ms: 0.2517
  ...
# Subtest: key 0 → fit
ok 2568 - key 0 → fit
  ---
  duration_ms: 0.307246
  ...
# Subtest: key 1 → actual
ok 2569 - key 1 → actual
  ---
  duration_ms: 0.82766
  ...
# Subtest: key h → pan:left
ok 2570 - key h → pan:left
  ---
  duration_ms: 0.762786
  ...
# Subtest: key j → pan:down
ok 2571 - key j → pan:down
  ---
  duration_ms: 0.232664
  ...
# Subtest: key k → pan:up
ok 2572 - key k → pan:up
  ---
  duration_ms: 0.563295
  ...
# Subtest: key l → pan:right
ok 2573 - key l → pan:right
  ---
  duration_ms: 0.16726
  ...
# Subtest: key Shift+H → pan:left
ok 2574 - key Shift+H → pan:left
  ---
  duration_ms: 0.167129
  ...
# Subtest: key Shift+J → pan:down
ok 2575 - key Shift+J → pan:down
  ---
  duration_ms: 0.245328
  ...
# Subtest: key Shift+K → pan:up
ok 2576 - key Shift+K → pan:up
  ---
  duration_ms: 0.142011
  ...
# Subtest: key Shift+L → pan:right
ok 2577 - key Shift+L → pan:right
  ---
  duration_ms: 0.128796
  ...
# Subtest: key ArrowLeft → pan:left
ok 2578 - key ArrowLeft → pan:left
  ---
  duration_ms: 0.122604
  ...
# Subtest: key ArrowDown → pan:down
ok 2579 - key ArrowDown → pan:down
  ---
  duration_ms: 0.138725
  ...
# Subtest: key ArrowUp → pan:up
ok 2580 - key ArrowUp → pan:up
  ---
  duration_ms: 0.290295
  ...
# Subtest: key ArrowRight → pan:right
ok 2581 - key ArrowRight → pan:right
  ---
  duration_ms: 0.147261
  ...
# Subtest: key Shift+ArrowLeft → pan:left
ok 2582 - key Shift+ArrowLeft → pan:left
  ---
  duration_ms: 0.300744
  ...
# Subtest: key Ctrl+q → ignore
ok 2583 - key Ctrl+q → ignore
  ---
  duration_ms: 0.143253
  ...
# Subtest: key Meta+z → ignore
ok 2584 - key Meta+z → ignore
  ---
  duration_ms: 0.472292
  ...
# Subtest: key Meta+Z → ignore
ok 2585 - key Meta+Z → ignore
  ---
  duration_ms: 0.227805
  ...
# Subtest: key a composing → ignore
ok 2586 - key a composing → ignore
  ---
  duration_ms: 0.15216
  ...
# Subtest: key a keyCode 229 → ignore
ok 2587 - key a keyCode 229 → ignore
  ---
  duration_ms: 0.128155
  ...
# Subtest: key x → ignore
ok 2588 - key x → ignore
  ---
  duration_ms: 0.127764
  ...
# Subtest: keys before arming are ignored
ok 2589 - keys before arming are ignored
  ---
  duration_ms: 2.442623
  ...
# Subtest: Z closes after arming, and a repeated Z does not
ok 2590 - Z closes after arming, and a repeated Z does not
  ---
  duration_ms: 0.925237
  ...
# Subtest: load sets fit state and dimensions
ok 2591 - load sets fit state and dimensions
  ---
  duration_ms: 1.112534
  ...
# Subtest: a load error shows a notice, closes, and calls onClosed once
ok 2592 - a load error shows a notice, closes, and calls onClosed once
  ---
  duration_ms: 0.538007
  ...
# Subtest: Escape closes once, unregisters the scope handler, and aborts the signal
ok 2593 - Escape closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.376188
  ...
# Subtest: q closes once, unregisters the scope handler, and aborts the signal
ok 2594 - q closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.779498
  ...
# Subtest: Q closes once, unregisters the scope handler, and aborts the signal
ok 2595 - Q closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.534069
  ...
# Subtest: Ctrl+[ closes once, unregisters the scope handler, and aborts the signal
ok 2596 - Ctrl+[ closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.568144
  ...
# Subtest: Z closes once, unregisters the scope handler, and aborts the signal
ok 2597 - Z closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.54985
  ...
# Subtest: a stray x key changes nothing
ok 2598 - a stray x key changes nothing
  ---
  duration_ms: 0.681291
  ...
# Subtest: the app's vault stubs throw and are never called
ok 2599 - the app's vault stubs throw and are never called
  ---
  duration_ms: 0.415784
  ...
# Subtest: task-card-gate arms only on open inbox tasks
ok 2600 - task-card-gate arms only on open inbox tasks
  ---
  duration_ms: 8.058252
  ...
# Subtest: task-card-gate header shows the Inbox chip only when armed
ok 2601 - task-card-gate header shows the Inbox chip only when armed
  ---
  duration_ms: 13.268837
  ...
# Subtest: task-card-gate priority: cancel writes nothing
ok 2602 - task-card-gate priority: cancel writes nothing
  ---
  duration_ms: 2.872985
  ...
# Subtest: task-card-gate priority: stay runs today's write
ok 2603 - task-card-gate priority: stay runs today's write
  ---
  duration_ms: 0.504283
  ...
# Subtest: task-card-gate priority: move writes then moves
ok 2604 - task-card-gate priority: move writes then moves
  ---
  duration_ms: 1.040527
  ...
# Subtest: task-card-gate scheduled: cancel writes nothing
ok 2605 - task-card-gate scheduled: cancel writes nothing
  ---
  duration_ms: 0.287198
  ...
# Subtest: task-card-gate scheduled: stay runs today's write
ok 2606 - task-card-gate scheduled: stay runs today's write
  ---
  duration_ms: 0.458506
  ...
# Subtest: task-card-gate scheduled: move writes then moves
ok 2607 - task-card-gate scheduled: move writes then moves
  ---
  duration_ms: 0.307366
  ...
# Subtest: task-card-gate generic-property: cancel writes nothing
ok 2608 - task-card-gate generic-property: cancel writes nothing
  ---
  duration_ms: 0.520394
  ...
# Subtest: task-card-gate generic-property: stay runs today's write
ok 2609 - task-card-gate generic-property: stay runs today's write
  ---
  duration_ms: 0.44526
  ...
# Subtest: task-card-gate generic-property: move writes then moves
ok 2610 - task-card-gate generic-property: move writes then moves
  ---
  duration_ms: 0.531715
  ...
# Subtest: task-card-gate refresh-interval: cancel writes nothing
ok 2611 - task-card-gate refresh-interval: cancel writes nothing
  ---
  duration_ms: 0.383542
  ...
# Subtest: task-card-gate refresh-interval: stay runs today's write
ok 2612 - task-card-gate refresh-interval: stay runs today's write
  ---
  duration_ms: 0.376859
  ...
# Subtest: task-card-gate refresh-interval: move writes then moves
ok 2613 - task-card-gate refresh-interval: move writes then moves
  ---
  duration_ms: 0.390455
  ...
# Subtest: task-card-gate refresh-custom: cancel writes nothing
ok 2614 - task-card-gate refresh-custom: cancel writes nothing
  ---
  duration_ms: 0.23065
  ...
# Subtest: task-card-gate refresh-custom: stay runs today's write
ok 2615 - task-card-gate refresh-custom: stay runs today's write
  ---
  duration_ms: 0.354667
  ...
# Subtest: task-card-gate refresh-custom: move writes then moves
ok 2616 - task-card-gate refresh-custom: move writes then moves
  ---
  duration_ms: 0.727268
  ...
# Subtest: task-card-gate clear-priority: cancel writes nothing
ok 2617 - task-card-gate clear-priority: cancel writes nothing
  ---
  duration_ms: 0.528319
  ...
# Subtest: task-card-gate clear-priority: stay runs today's write
ok 2618 - task-card-gate clear-priority: stay runs today's write
  ---
  duration_ms: 0.263633
  ...
# Subtest: task-card-gate clear-priority: move writes then moves
ok 2619 - task-card-gate clear-priority: move writes then moves
  ---
  duration_ms: 0.362381
  ...
# Subtest: task-card-gate recommended-roll: cancel writes nothing
ok 2620 - task-card-gate recommended-roll: cancel writes nothing
  ---
  duration_ms: 0.203678
  ...
# Subtest: task-card-gate recommended-roll: stay runs today's write
ok 2621 - task-card-gate recommended-roll: stay runs today's write
  ---
  duration_ms: 0.231982
  ...
# Subtest: task-card-gate recommended-roll: move writes then moves
ok 2622 - task-card-gate recommended-roll: move writes then moves
  ---
  duration_ms: 0.201906
  ...
# Subtest: task-card-gate recommended-decay: cancel writes nothing
ok 2623 - task-card-gate recommended-decay: cancel writes nothing
  ---
  duration_ms: 0.14694
  ...
# Subtest: task-card-gate recommended-decay: stay runs today's write
ok 2624 - task-card-gate recommended-decay: stay runs today's write
  ---
  duration_ms: 0.153262
  ...
# Subtest: task-card-gate recommended-decay: move writes then moves
ok 2625 - task-card-gate recommended-decay: move writes then moves
  ---
  duration_ms: 0.384404
  ...
# Subtest: task-card-gate counted-roll: cancel writes nothing
ok 2626 - task-card-gate counted-roll: cancel writes nothing
  ---
  duration_ms: 0.231211
  ...
# Subtest: task-card-gate counted-roll: stay runs today's write
ok 2627 - task-card-gate counted-roll: stay runs today's write
  ---
  duration_ms: 0.294472
  ...
# Subtest: task-card-gate counted-roll: move writes then moves
ok 2628 - task-card-gate counted-roll: move writes then moves
  ---
  duration_ms: 0.256099
  ...
# Subtest: task-card-gate lane-toggle: cancel writes nothing
ok 2629 - task-card-gate lane-toggle: cancel writes nothing
  ---
  duration_ms: 0.197257
  ...
# Subtest: task-card-gate lane-toggle: stay runs today's write
ok 2630 - task-card-gate lane-toggle: stay runs today's write
  ---
  duration_ms: 2.346921
  ...
# Subtest: task-card-gate lane-toggle: move writes then moves
ok 2631 - task-card-gate lane-toggle: move writes then moves
  ---
  duration_ms: 0.672223
  ...
# Subtest: task-card-gate dependency-single: cancel writes nothing
ok 2632 - task-card-gate dependency-single: cancel writes nothing
  ---
  duration_ms: 0.322525
  ...
# Subtest: task-card-gate dependency-single: stay runs today's write
ok 2633 - task-card-gate dependency-single: stay runs today's write
  ---
  duration_ms: 0.197096
  ...
# Subtest: task-card-gate dependency-single: move writes then moves
ok 2634 - task-card-gate dependency-single: move writes then moves
  ---
  duration_ms: 0.221092
  ...
# Subtest: task-card-gate dependency-marked: cancel writes nothing
ok 2635 - task-card-gate dependency-marked: cancel writes nothing
  ---
  duration_ms: 0.177318
  ...
# Subtest: task-card-gate dependency-marked: stay runs today's write
ok 2636 - task-card-gate dependency-marked: stay runs today's write
  ---
  duration_ms: 0.472331
  ...
# Subtest: task-card-gate dependency-marked: move writes then moves
ok 2637 - task-card-gate dependency-marked: move writes then moves
  ---
  duration_ms: 0.265847
  ...
# Subtest: task-card-gate dependency-vault: cancel writes nothing
ok 2638 - task-card-gate dependency-vault: cancel writes nothing
  ---
  duration_ms: 0.176707
  ...
# Subtest: task-card-gate dependency-vault: stay runs today's write
ok 2639 - task-card-gate dependency-vault: stay runs today's write
  ---
  duration_ms: 1.293589
  ...
# Subtest: task-card-gate dependency-vault: move writes then moves
ok 2640 - task-card-gate dependency-vault: move writes then moves
  ---
  duration_ms: 0.478974
  ...
# Subtest: task-card-gate dependency-counted: cancel writes nothing
ok 2641 - task-card-gate dependency-counted: cancel writes nothing
  ---
  duration_ms: 0.218376
  ...
# Subtest: task-card-gate dependency-counted: stay runs today's write
ok 2642 - task-card-gate dependency-counted: stay runs today's write
  ---
  duration_ms: 0.306765
  ...
# Subtest: task-card-gate dependency-counted: move writes then moves
ok 2643 - task-card-gate dependency-counted: move writes then moves
  ---
  duration_ms: 0.261699
  ...
# Subtest: task-card-gate negative rows never prompt
ok 2644 - task-card-gate negative rows never prompt
  ---
  duration_ms: 1.700957
  ...
# Subtest: task-card-gate counted sessions capture N targets
ok 2645 - task-card-gate counted sessions capture N targets
  ---
  duration_ms: 0.612489
  ...
# Subtest: task-card-gate walk: move advances once with Moved first
ok 2646 - task-card-gate walk: move advances once with Moved first
  ---
  duration_ms: 0.522778
  ...
# Subtest: task-card-gate walk: move failure falls back to card with partial
ok 2647 - task-card-gate walk: move failure falls back to card with partial
  ---
  duration_ms: 0.948952
  ...
# Subtest: task-card-gate walk: exactly one settle per origin
ok 2648 - task-card-gate walk: exactly one settle per origin
  ---
  duration_ms: 49.697744
  ...
# Subtest: task-card-gate route outcome resolves like lane and link-today
ok 2649 - task-card-gate route outcome resolves like lane and link-today
  ---
  duration_ms: 0.65452
  ...
# Subtest: inbox classifier covers the inbox contract
ok 2650 - inbox classifier covers the inbox contract
  ---
  duration_ms: 3.807908
  ...
# Subtest: isInboxNotePath matches the inbox contract through the vault
ok 2651 - isInboxNotePath matches the inbox contract through the vault
  ---
  duration_ms: 2.339586
  ...
# Subtest: isInboxNotePath is false without an inbox note and never throws
ok 2652 - isInboxNotePath is false without an inbox note and never throws
  ---
  duration_ms: 0.378743
  ...
# Subtest: route destinations drop every inbox note, the source, and templates
ok 2653 - route destinations drop every inbox note, the source, and templates
  ---
  duration_ms: 1.835022
  ...
# Subtest: route preflight accepts a live area destination
ok 2654 - route preflight accepts a live area destination
  ---
  duration_ms: 7.506038
  ...
# Subtest: route preflight refuses stale and colliding destinations
ok 2655 - route preflight refuses stale and colliding destinations
  ---
  duration_ms: 2.704833
  ...
# Subtest: route picker resolves move, stay, cancel, and close exactly once
ok 2656 - route picker resolves move, stay, cancel, and close exactly once
  ---
  duration_ms: 6.515377
  ...
# Subtest: route picker footer names the move, the hatch, and the way back
ok 2657 - route picker footer names the move, the hatch, and the way back
  ---
  duration_ms: 1.14211
  ...
# Subtest: route picker preflight refusal keeps the picker open with a notice
ok 2658 - route picker preflight refusal keeps the picker open with a notice
  ---
  duration_ms: 17.969179
  ...
# Subtest: route picker honors the shared move-picker guard
ok 2659 - route picker honors the shared move-picker guard
  ---
  duration_ms: 4.174728
  ...
# Subtest: promptInboxRoute moves, stays, and cancels with suspend pairing
ok 2660 - promptInboxRoute moves, stays, and cancels with suspend pairing
  ---
  duration_ms: 5.60044
  ...
# Subtest: commitInboxRoute moves the verified task with its children
ok 2661 - commitInboxRoute moves the verified task with its children
  ---
  duration_ms: 6.944305
  ...
# Subtest: commitInboxRoute into a blocked project tags the moved task
ok 2662 - commitInboxRoute into a blocked project tags the moved task
  ---
  duration_ms: 13.237839
  ...
# Subtest: commitInboxRoute moves a counted run and refuses on identity drift
ok 2663 - commitInboxRoute moves a counted run and refuses on identity drift
  ---
  duration_ms: 4.714739
  ...
# Subtest: reviewOutcomeResolves treats route like lane and link-today
ok 2664 - reviewOutcomeResolves treats route like lane and link-today
  ---
  duration_ms: 0.699235
  ...
# Subtest: nav api inboxRoute v1 delegates, shapes, and never throws
ok 2665 - nav api inboxRoute v1 delegates, shapes, and never throws
  ---
  duration_ms: 3.045594
  ...
# Subtest: history records ordered locations with file identity and dedupes adjacent repeats
ok 2666 - history records ordered locations with file identity and dedupes adjacent repeats
  ---
  duration_ms: 2.493822
  ...
# Subtest: transition records origin then destination and truncates forward only on success
ok 2667 - transition records origin then destination and truncates forward only on success
  ---
  duration_ms: 2.088166
  ...
# Subtest: history retains at most 100 locations and refreshes the live tip
ok 2668 - history retains at most 100 locations and refreshes the live tip
  ---
  duration_ms: 1.064802
  ...
# Subtest: rename updates paths and delete prunes without corrupting the index
ok 2669 - rename updates paths and delete prunes without corrupting the index
  ---
  duration_ms: 0.416695
  ...
# Subtest: bridge wraps add once, mirrors native jumps, and preserves the original call
ok 2670 - bridge wraps add once, mirrors native jumps, and preserves the original call
  ---
  duration_ms: 2.320449
  ...
# Subtest: bridge without a jump list preserves keys and emits one compatibility diagnostic
ok 2671 - bridge without a jump list preserves keys and emits one compatibility diagnostic
  ---
  duration_ms: 0.516175
  ...
# Subtest: registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
ok 2672 - registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
  ---
  duration_ms: 0.679798
  ...
# Subtest: Enter A->B round-trips with Ctrl+O and Ctrl+I
ok 2673 - Enter A->B round-trips with Ctrl+O and Ctrl+I
  ---
  duration_ms: 24.320764
  ...
# Subtest: counted Enter returns to the original cursor, not the counted link line
ok 2674 - counted Enter returns to the original cursor, not the counted link line
  ---
  duration_ms: 26.323997
  ...
# Subtest: picker choice records one jump and cancellation records none
ok 2675 - picker choice records one jump and cancellation records none
  ---
  duration_ms: 32.597743
  ...
# Subtest: stale picker origin is rejected and failed opens record nothing
ok 2676 - stale picker origin is rejected and failed opens record nothing
  ---
  duration_ms: 26.039624
  ...
# Subtest: Backspace shares the link path and no-link lines fall through
ok 2677 - Backspace shares the link path and no-link lines fall through
  ---
  duration_ms: 22.517412
  ...
# Subtest: counted traversal honors boundaries and new jumps replace the forward branch
ok 2678 - counted traversal honors boundaries and new jumps replace the forward branch
  ---
  duration_ms: 1.574896
  ...
# Subtest: ordinary motion before back is preserved for forward restore
ok 2679 - ordinary motion before back is preserved for forward restore
  ---
  duration_ms: 0.694375
  ...
# Subtest: deleted entries are skipped and heading links settle before recording
ok 2680 - deleted entries are skipped and heading links settle before recording
  ---
  duration_ms: 22.650366
  ...
# Subtest: native fallback runs with empty history and boundaries never replay natives
ok 2681 - native fallback runs with empty history and boundaries never replay natives
  ---
  duration_ms: 1.486638
  ...
# Subtest: unload restores the native add and keeps a foreign later mapping
ok 2682 - unload restores the native add and keeps a foreign later mapping
  ---
  duration_ms: 0.688434
  ...
# Subtest: exact eligibility authorizes one due-Ready ROTTEN row
ok 2683 - exact eligibility authorizes one due-Ready ROTTEN row
  ---
  duration_ms: 2.469013
  ...
# Subtest: exact eligibility authorizes a TICKLER row
ok 2684 - exact eligibility authorizes a TICKLER row
  ---
  duration_ms: 0.341662
  ...
# Subtest: exact eligibility refuses every stale-cache shape
ok 2685 - exact eligibility refuses every stale-cache shape
  ---
  duration_ms: 1.459687
  ...
# Subtest: exact eligibility refuses non-Ready and non-due rows
ok 2686 - exact eligibility refuses non-Ready and non-due rows
  ---
  duration_ms: 0.578364
  ...
# Subtest: legacy refs still match line-only while exact refuses
ok 2687 - legacy refs still match line-only while exact refuses
  ---
  duration_ms: 1.107264
  ...
# Subtest: keeps support needs namespace v5 with keepLine
ok 2688 - keeps support needs namespace v5 with keepLine
  ---
  duration_ms: 0.324089
  ...
# Subtest: decay decisions need namespace v6 with keepLine
ok 2689 - decay decisions need namespace v6 with keepLine
  ---
  duration_ms: 0.285435
  ...
# Subtest: batch forwards per-target counted decisions to the stamper
ok 2690 - batch forwards per-target counted decisions to the stamper
  ---
  duration_ms: 1.591037
  ...
# Subtest: batch keeps legacy index targets uncounted
ok 2691 - batch keeps legacy index targets uncounted
  ---
  duration_ms: 0.466301
  ...
# Subtest: a throwing stamper refuses the batch with no partial write
ok 2692 - a throwing stamper refuses the batch with no partial write
  ---
  duration_ms: 0.601408
  ...
# Subtest: parseKeepsCount reads the first valid value only
ok 2693 - parseKeepsCount reads the first valid value only
  ---
  duration_ms: 0.509984
  ...
# Subtest: countFreshStampKept measures actual increments only
ok 2694 - countFreshStampKept measures actual increments only
  ---
  duration_ms: 0.401627
  ...
# Subtest: fresh stamp notice tails kept increments without promises
ok 2695 - fresh stamp notice tails kept increments without promises
  ---
  duration_ms: 0.616176
  ...
# Subtest: duplicate source targets dedupe to one write
ok 2696 - duplicate source targets dedupe to one write
  ---
  duration_ms: 0.493552
  ...
# Subtest: single Alt+F increments an exact due-Ready ROTTEN task
ok 2697 - single Alt+F increments an exact due-Ready ROTTEN task
  ---
  duration_ms: 15.053304
  ...
# Subtest: single Alt+F preserves NEW, lane, and early tasks without counting
ok 2698 - single Alt+F preserves NEW, lane, and early tasks without counting
  ---
  duration_ms: 4.49432
  ...
# Subtest: same-day repeat stays identical and counts nothing
ok 2699 - same-day repeat stays identical and counts nothing
  ---
  duration_ms: 1.388249
  ...
# Subtest: Pending Alt+F writes its summary with the stamp in one edit
ok 2700 - Pending Alt+F writes its summary with the stamp in one edit
  ---
  duration_ms: 2.104427
  ...
# Subtest: counted Pending refresh shares one summary only with Pending targets
ok 2701 - counted Pending refresh shares one summary only with Pending targets
  ---
  duration_ms: 8.657034
  ...
# Subtest: a refusing counted target refuses before the Pending Work Log prompt
ok 2702 - a refusing counted target refuses before the Pending Work Log prompt
  ---
  duration_ms: 1.380215
  ...
# Subtest: blank Pending refresh advances; cancelled or stale prompts write nothing
ok 2703 - blank Pending refresh advances; cancelled or stale prompts write nothing
  ---
  duration_ms: 3.149512
  ...
# Subtest: stale queue match stamps uncounted and never inflates
ok 2704 - stale queue match stamps uncounted and never inflates
  ---
  duration_ms: 1.532404
  ...
# Subtest: counted Alt+F increments every exact target once
ok 2705 - counted Alt+F increments every exact target once
  ---
  duration_ms: 3.523846
  ...
# Subtest: stale editor source refuses with no write
ok 2706 - stale editor source refuses with no write
  ---
  duration_ms: 0.852838
  ...
# Subtest: single-note write lands in one editor transaction and keeps CRLF
ok 2707 - single-note write lands in one editor transaction and keeps CRLF
  ---
  duration_ms: 1.700125
  ...
# Subtest: v5 without keepLine fails without writing
ok 2708 - v5 without keepLine fails without writing
  ---
  duration_ms: 0.482671
  ...
# Subtest: throwing v5 keepLine refuses the batch with no partial write
ok 2709 - throwing v5 keepLine refuses the batch with no partial write
  ---
  duration_ms: 0.802452
  ...
# Subtest: pre-v5 ledger stamps uncounted through the old stamper
ok 2710 - pre-v5 ledger stamps uncounted through the old stamper
  ---
  duration_ms: 0.905759
  ...
# Subtest: Task Link session skips an at-limit decide target
ok 2711 - Task Link session skips an at-limit decide target
  ---
  duration_ms: 4.205569
  ...
# Subtest: Task Link refresh counts one exact target
ok 2712 - Task Link refresh counts one exact target
  ---
  duration_ms: 4.20674
  ...
# Subtest: duplicate Task Links to one target stamp and count once
ok 2713 - duplicate Task Links to one target stamp and count once
  ---
  duration_ms: 1.866483
  ...
# Subtest: counted Task Link sessions combine Pending work and Rotten keep logs
ok 2714 - counted Task Link sessions combine Pending work and Rotten keep logs
  ---
  duration_ms: 1.678354
  ...
# Subtest: counted Task Links dedupe targets and log only the Pending target
ok 2715 - counted Task Links dedupe targets and log only the Pending target
  ---
  duration_ms: 1.516816
  ...
# Subtest: multi-note stale preimage refuses with no writes
ok 2716 - multi-note stale preimage refuses with no writes
  ---
  duration_ms: 1.2049
  ...
# Subtest: a linked note changed during the Keep prompt refuses before any write
ok 2717 - a linked note changed during the Keep prompt refuses before any write
  ---
  duration_ms: 0.677614
  ...
# Subtest: multi-note write failure rolls back the first note
ok 2718 - multi-note write failure rolls back the first note
  ---
  duration_ms: 1.787883
  ...
# Subtest: partial rollback is reported and a same-day retry does not duplicate the logged keep
ok 2719 - partial rollback is reported and a same-day retry does not duplicate the logged keep
  ---
  duration_ms: 3.458742
  ...
# Subtest: one physical key through two routes stamps once
ok 2720 - one physical key through two routes stamps once
  ---
  duration_ms: 1.957696
  ...
# Subtest: Ctrl+Alt+F capture advances once and consumes a Vim prefix
ok 2721 - Ctrl+Alt+F capture advances once and consumes a Vim prefix
  ---
  duration_ms: 1.51432
  ...
# Subtest: obsolete and extra-modifier F chords stay unconsumed
ok 2722 - obsolete and extra-modifier F chords stay unconsumed
  ---
  duration_ms: 0.491548
  ...
# Subtest: live Ctrl+Alt+F double dispatch asks once on a Pending task
ok 2723 - live Ctrl+Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 1.053171
  ...
# Subtest: live Alt+F double dispatch asks once on a Pending task
ok 2724 - live Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.716247
  ...
# Subtest: already-handled refresh keydown leaves Vim state alone
ok 2725 - already-handled refresh keydown leaves Vim state alone
  ---
  duration_ms: 0.334689
  ...
# Subtest: parseBobOpenNotesParams accepts indexed entries and ignores unknown keys
ok 2726 - parseBobOpenNotesParams accepts indexed entries and ignores unknown keys
  ---
  duration_ms: 4.108802
  ...
# Subtest: parseBobOpenNotesParams rejects every malformed URI field
ok 2727 - parseBobOpenNotesParams rejects every malformed URI field
  ---
  duration_ms: 0.770942
  ...
# Subtest: invalid batches show one notice and open nothing
ok 2728 - invalid batches show one notice and open nothing
  ---
  duration_ms: 2.138983
  ...
# Subtest: path mapping follows a symlink realpath into the vault
ok 2729 - path mapping follows a symlink realpath into the vault
  ---
  duration_ms: 8.426756
  ...
# Subtest: new-tab policy reuses existing tabs and the active empty tab, keeping order and primary active
ok 2730 - new-tab policy reuses existing tabs and the active empty tab, keeping order and primary active
  ---
  duration_ms: 3.910293
  ...
# Subtest: an absent or outside entry fails independently and a PDF opens without landing
ok 2731 - an absent or outside entry fails independently and a PDF opens without landing
  ---
  duration_ms: 2001.275567
  ...
# Subtest: a resolved note that is not open waits until its captured digest is cached
ok 2732 - a resolved note that is not open waits until its captured digest is cached
  ---
  duration_ms: 71.366746
  ...
# Subtest: a per-entry open failure does not prevent later notes from opening
ok 2733 - a per-entry open failure does not prevent later notes from opening
  ---
  duration_ms: 1.433536
  ...
# Subtest: waits for a newly created vault file and a late visible line digest
ok 2734 - waits for a newly created vault file and a late visible line digest
  ---
  duration_ms: 61.409449
  ...
# Subtest: re-finds a moved digest on any line, including prose and Pomodoro rows
ok 2735 - re-finds a moved digest on any line, including prose and Pomodoro rows
  ---
  duration_ms: 1.189671
  ...
# Subtest: deadline fallback opens near the planned line and reports a changed capture
ok 2736 - deadline fallback opens near the planned line and reports a changed capture
  ---
  duration_ms: 2001.202289
  ...
# Subtest: truncation reports how many of the full list opened
ok 2737 - truncation reports how many of the full list opened
  ---
  duration_ms: 0.800719
  ...
# Subtest: serializes quick URLs and leaves the later URL active
ok 2738 - serializes quick URLs and leaves the later URL active
  ---
  duration_ms: 1.872685
  ...
# Subtest: primary landing flashes briefly, secondary landings do not, and the handler is read-only
ok 2739 - primary landing flashes briefly, secondary landings do not, and the handler is read-only
  ---
  duration_ms: 16.180195
  ...
# Subtest: onload registers bob-open-notes beside bob-goto-task
ok 2740 - onload registers bob-open-notes beside bob-goto-task
  ---
  duration_ms: 1.745882
  ...
# Subtest: a non-file sidebar view is not reused as an empty tab
ok 2741 - a non-file sidebar view is not reused as an empty tab
  ---
  duration_ms: 0.669908
  ...
# Subtest: a true empty tab is reused for the first entry
ok 2742 - a true empty tab is reused for the first entry
  ---
  duration_ms: 0.420613
  ...
# Subtest: three new tabs follow entry order in the tab strip
ok 2743 - three new tabs follow entry order in the tab strip
  ---
  duration_ms: 0.752276
  ...
# Subtest: two tabs of the same note reuse the first matching leaf
ok 2744 - two tabs of the same note reuse the first matching leaf
  ---
  duration_ms: 0.40858
  ...
# Subtest: a missing file does not scan vault lists when getAbstractFileByPath exists
ok 2745 - a missing file does not scan vault lists when getAbstractFileByPath exists
  ---
  duration_ms: 2000.520025
  ...
# Subtest: new tabs append at the far right when the middle tab is active
ok 2746 - new tabs append at the far right when the middle tab is active
  ---
  duration_ms: 0.918023
  ...
# Subtest: a reused tab stays put while a new one is appended
ok 2747 - a reused tab stays put while a new one is appended
  ---
  duration_ms: 0.496879
  ...
# Subtest: a deferred tab is reused and findMarkdownLeafByPath sees it
ok 2748 - a deferred tab is reused and findMarkdownLeafByPath sees it
  ---
  duration_ms: 0.682453
  ...
# Subtest: a deferred sidebar leaf whose saved state names the note is not reused
ok 2749 - a deferred sidebar leaf whose saved state names the note is not reused
  ---
  duration_ms: 0.43485
  ...
# Subtest: a loaded main-area match beats an earlier loaded sidebar match
ok 2750 - a loaded main-area match beats an earlier loaded sidebar match
  ---
  duration_ms: 0.380196
  ...
# Subtest: a new tab goes to the end of the main group when a sidebar leaf is active
ok 2751 - a new tab goes to the end of the main group when a sidebar leaf is active
  ---
  duration_ms: 0.420884
  ...
# Subtest: falling back without createLeafInParent still opens a new tab
ok 2752 - falling back without createLeafInParent still opens a new tab
  ---
  duration_ms: 0.404502
  ...
# Subtest: falling back when createLeafInParent throws still opens a new tab
ok 2753 - falling back when createLeafInParent throws still opens a new tab
  ---
  duration_ms: 0.526786
  ...
# Subtest: collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
ok 2754 - collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
  ---
  duration_ms: 5.43219
  ...
# Subtest: getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
ok 2755 - getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
  ---
  duration_ms: 4.413403
  ...
# Subtest: getProjectBlockState reports an open external prerequisite
ok 2756 - getProjectBlockState reports an open external prerequisite
  ---
  duration_ms: 1.148973
  ...
# Subtest: getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
ok 2757 - getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
  ---
  duration_ms: 1.271376
  ...
# Subtest: getProjectBlockState scheduledValue override is the inline date, not frontmatter
ok 2758 - getProjectBlockState scheduledValue override is the inline date, not frontmatter
  ---
  duration_ms: 0.630744
  ...
# Subtest: getProjectBlockState skips internal and archive Depends-On links
ok 2759 - getProjectBlockState skips internal and archive Depends-On links
  ---
  duration_ms: 5.040061
  ...
# Subtest: getProjectBlockState is a no-op for terminal, daily, and non-project notes
ok 2760 - getProjectBlockState is a no-op for terminal, daily, and non-project notes
  ---
  duration_ms: 1.337985
  ...
# Subtest: projectLooksBlockedByPrjShortcut is the single [?] ^prj row
ok 2761 - projectLooksBlockedByPrjShortcut is the single [?] ^prj row
  ---
  duration_ms: 0.416445
  ...
# Subtest: taskHasProjectBlockedTag is token-bounded and does not match \#prj
ok 2762 - taskHasProjectBlockedTag is token-bounded and does not match \#prj
  ---
  duration_ms: 0.445691
  ...
# Subtest: setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
ok 2763 - setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
  ---
  duration_ms: 1.160155
  ...
# Subtest: reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
ok 2764 - reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
  ---
  duration_ms: 0.766102
  ...
# Subtest: reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
ok 2765 - reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
  ---
  duration_ms: 0.507679
  ...
# Subtest: reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
ok 2766 - reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
  ---
  duration_ms: 0.598523
  ...
# Subtest: ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
ok 2767 - ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
  ---
  duration_ms: 11.113544
  ...
# Subtest: recovery gate keeps a resident of a blocked project blocked after own deps close
ok 2768 - recovery gate keeps a resident of a blocked project blocked after own deps close
  ---
  duration_ms: 4.468629
  ...
# Subtest: recovery gate blocks residents on a future inline project date with no deps
ok 2769 - recovery gate blocks residents on a future inline project date with no deps
  ---
  duration_ms: 1.080763
  ...
# Subtest: planDeferredPomodoroLinkCleanup always deletes a last-child open entry
ok 2770 - planDeferredPomodoroLinkCleanup always deletes a last-child open entry
  ---
  duration_ms: 4.114915
  ...
# Subtest: TICKLER notice uses unblocked <date> when returnedBy is unblocked
ok 2771 - TICKLER notice uses unblocked <date> when returnedBy is unblocked
  ---
  duration_ms: 1.373011
  ...
# Subtest: recognition: a `^prj` parent in a project note carries its residents
ok 2772 - recognition: a `^prj` parent in a project note carries its residents
  ---
  duration_ms: 6.616901
  ...
# Subtest: recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
ok 2773 - recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
  ---
  duration_ms: 0.956375
  ...
# Subtest: add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
ok 2774 - add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
  ---
  duration_ms: 10.659846
  ...
# Subtest: add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
ok 2775 - add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
  ---
  duration_ms: 6.536528
  ...
# Subtest: guards: a same-note add to `^prj` refuses, including mixed batches
ok 2776 - guards: a same-note add to `^prj` refuses, including mixed batches
  ---
  duration_ms: 1.300231
  ...
# Subtest: guards: the stage disables same-note rows for `^prj` with `inside this project`
ok 2777 - guards: the stage disables same-note rows for `^prj` with `inside this project`
  ---
  duration_ms: 2.209507
  ...
# Subtest: guards: cycle detection includes the implicit resident edges (§13.6)
ok 2778 - guards: cycle detection includes the implicit resident edges (§13.6)
  ---
  duration_ms: 2.75571
  ...
# Subtest: removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
ok 2779 - removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
  ---
  duration_ms: 11.071674
  ...
# Subtest: removal: a resident with its own reason stays `[?]` without the tag (PDB3)
ok 2780 - removal: a resident with its own reason stays `[?]` without the tag (PDB3)
  ---
  duration_ms: 2.373791
  ...
# Subtest: removal without a registry defers to reconcile: residents keep `[?]` and the tag
ok 2781 - removal without a registry defers to reconcile: residents keep `[?]` and the tag
  ---
  duration_ms: 1.374073
  ...
# Subtest: writer: one gesture commits `^prj` and its residents in a single undo group
ok 2782 - writer: one gesture commits `^prj` and its residents in a single undo group
  ---
  duration_ms: 1.518008
  ...
# Subtest: writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
ok 2783 - writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
  ---
  duration_ms: 4.623917
  ...
# Subtest: notices: the project strings name the task, the flips, and the Pomodoro cleanup
ok 2784 - notices: the project strings name the task, the flips, and the Pomodoro cleanup
  ---
  duration_ms: 0.432154
  ...
# Subtest: mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
ok 2785 - mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
  ---
  duration_ms: 0.511016
  ...
# Subtest: api v3: removeDependencyByRef delegates removals to the single-transaction writer
ok 2786 - api v3: removeDependencyByRef delegates removals to the single-transaction writer
  ---
  duration_ms: 1.45151
  ...
# Subtest: api v3: openDependencyStageForRef opens the Depends on stage on the owning task
ok 2787 - api v3: openDependencyStageForRef opens the Depends on stage on the owning task
  ---
  duration_ms: 0.707751
  ...
# Subtest: internal links stay on the line but leave the field (PDR7)
ok 2788 - internal links stay on the line but leave the field (PDR7)
  ---
  duration_ms: 1.550079
  ...
# Subtest: removal from an unblocked ^prj never recovers own-reason residents (§13.10)
ok 2789 - removal from an unblocked ^prj never recovers own-reason residents (§13.10)
  ---
  duration_ms: 1.489793
  ...
# Subtest: resident recovery touches only tagged residents (§13.10)
ok 2790 - resident recovery touches only tagged residents (§13.10)
  ---
  duration_ms: 2.00649
  ...
# Subtest: stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
ok 2791 - stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
  ---
  duration_ms: 1.510444
  ...
# Subtest: projectDependentResidentKeys lists open residents with block ids
ok 2792 - projectDependentResidentKeys lists open residents with block ids
  ---
  duration_ms: 0.551433
  ...
# Subtest: navNoteScopeFlags marks daily notes; a missing writer stays null
ok 2793 - navNoteScopeFlags marks daily notes; a missing writer stays null
  ---
  duration_ms: 0.482491
  ...
# Subtest: reconcileBlockedScheduledTaskLine forwards scope flags to the writer
ok 2794 - reconcileBlockedScheduledTaskLine forwards scope flags to the writer
  ---
  duration_ms: 0.292118
  ...
# Subtest: parseProjectNoteFrontmatter ignores leftover scheduled keys
ok 2795 - parseProjectNoteFrontmatter ignores leftover scheduled keys
  ---
  duration_ms: 0.957297
  ...
# Subtest: formatTaskMoveProjectCountsNotice names blocked and recovered counts
ok 2796 - formatTaskMoveProjectCountsNotice names blocked and recovered counts
  ---
  duration_ms: 0.283472
  ...
# Subtest: PDS15: projectParentTarget keeps the path and drops alias and heading
ok 2797 - PDS15: projectParentTarget keeps the path and drops alias and heading
  ---
  duration_ms: 2.379673
  ...
# Subtest: PDS6: list-form, missing, and non-wikilink parents yield none
ok 2798 - PDS6: list-form, missing, and non-wikilink parents yield none
  ---
  duration_ms: 0.635883
  ...
# Subtest: PDS15: resolveProjectParentPath accepts alias, path, and heading forms
ok 2799 - PDS15: resolveProjectParentPath accepts alias, path, and heading forms
  ---
  duration_ms: 0.658146
  ...
# Subtest: PDS6: self, unresolved, and ambiguous basenames yield no parent
ok 2800 - PDS6: self, unresolved, and ambiguous basenames yield no parent
  ---
  duration_ms: 0.261409
  ...
# Subtest: buildProjectChildrenMap and descendants BFS skip cycles and cap depth
ok 2801 - buildProjectChildrenMap and descendants BFS skip cycles and cap depth
  ---
  duration_ms: 4.991938
  ...
# Subtest: PDS6: area, terminal, daily, and self-parent notes are not children
ok 2802 - PDS6: area, terminal, daily, and self-parent notes are not children
  ---
  duration_ms: 0.631816
  ...
# Subtest: PDG8: planner blocks child and grandchild ^prj and residents
ok 2803 - PDG8: planner blocks child and grandchild ^prj and residents
  ---
  duration_ms: 4.255353
  ...
# Subtest: PDG9: planner recovers tagged descendants with [unblocked::]
ok 2804 - PDG9: planner recovers tagged descendants with [unblocked::]
  ---
  duration_ms: 2.102273
  ...
# Subtest: PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
ok 2805 - PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
  ---
  duration_ms: 7.110331
  ...
# Subtest: PDG11: a tagged root re-asserts descendant tags and recovers nothing
ok 2806 - PDG11: a tagged root re-asserts descendant tags and recovers nothing
  ---
  duration_ms: 0.861915
  ...
# Subtest: tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
ok 2807 - tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
  ---
  duration_ms: 0.349106
  ...
# Subtest: tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
ok 2808 - tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
  ---
  duration_ms: 2.84011
  ...
# Subtest: tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
ok 2809 - tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
  ---
  duration_ms: 0.321274
  ...
# Subtest: tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
ok 2810 - tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
  ---
  duration_ms: 3.049652
  ...
# Subtest: PDG13: failProjectPrjInternalAdd refuses descendant targets
ok 2811 - PDG13: failProjectPrjInternalAdd refuses descendant targets
  ---
  duration_ms: 0.575038
  ...
# Subtest: PDG13: planDependencyEdit refuses a descendant add from the files map
ok 2812 - PDG13: planDependencyEdit refuses a descendant add from the files map
  ---
  duration_ms: 2.60903
  ...
# Subtest: PDG13: the stage disables descendant rows
ok 2813 - PDG13: the stage disables descendant rows
  ---
  duration_ms: 2.124705
  ...
# Subtest: reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
ok 2814 - reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
  ---
  duration_ms: 0.781391
  ...
# Subtest: tag proxy: removing the last own dep of a tagged ^prj recovers nobody
ok 2815 - tag proxy: removing the last own dep of a tagged ^prj recovers nobody
  ---
  duration_ms: 4.381434
  ...
# Subtest: PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
ok 2816 - PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
  ---
  duration_ms: 58.008106
  ...
# Subtest: PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
ok 2817 - PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
  ---
  duration_ms: 11.155783
  ...
# Subtest: PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
ok 2818 - PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
  ---
  duration_ms: 27.544848
  ...
# Subtest: PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
ok 2819 - PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
  ---
  duration_ms: 17.588232
  ...
# Subtest: PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
ok 2820 - PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
  ---
  duration_ms: 17.632899
  ...
# Subtest: PDG12: moving the project date due recovers descendants
ok 2821 - PDG12: moving the project date due recovers descendants
  ---
  duration_ms: 6.609236
  ...
# Subtest: PDG12: deleting the project date recovers descendants
ok 2822 - PDG12: deleting the project date recovers descendants
  ---
  duration_ms: 5.873781
  ...
# Subtest: PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
ok 2823 - PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
  ---
  duration_ms: 21.75138
  ...
# Subtest: PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
ok 2824 - PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
  ---
  duration_ms: 8.745814
  ...
# Subtest: Task Link Depends on writer preserves the internal-target guard on a project task
ok 2825 - Task Link Depends on writer preserves the internal-target guard on a project task
  ---
  duration_ms: 1.839723
  ...
# Subtest: api v3 removeDependencyByRef runs the recovery cascade for a linked project task
ok 2826 - api v3 removeDependencyByRef runs the recovery cascade for a linked project task
  ---
  duration_ms: 19.03314
  ...
# Subtest: counted Schedule writer cascades a future date through descendants
ok 2827 - counted Schedule writer cascades a future date through descendants
  ---
  duration_ms: 7.123597
  ...
# Subtest: counted subtree roots are ancestor-first and each descendant note is planned once
ok 2828 - counted subtree roots are ancestor-first and each descendant note is planned once
  ---
  duration_ms: 5.046543
  ...
# Subtest: Ctrl+D on the Depends on row removes the line and recovers the subtree
ok 2829 - Ctrl+D on the Depends on row removes the line and recovers the subtree
  ---
  duration_ms: 14.90979
  ...
# Subtest: a ^prj with no children reads no other note
ok 2830 - a ^prj with no children reads no other note
  ---
  duration_ms: 0.804365
  ...
# Subtest: single seeds from raw text, not display decorations
ok 2831 - single seeds from raw text, not display decorations
  ---
  duration_ms: 19.854309
  ...
# Subtest: legacy valid free wins; invalid and taken fall through
ok 2832 - legacy valid free wins; invalid and taken fall through
  ---
  duration_ms: 3.639497
  ...
# Subtest: batch reserves suffixes for two same-text tasks
ok 2833 - batch reserves suffixes for two same-text tasks
  ---
  duration_ms: 1.911218
  ...
# Subtest: counted-source, vault-single, and vault-counted seed per mode
ok 2834 - counted-source, vault-single, and vault-counted seed per mode
  ---
  duration_ms: 2.124726
  ...
# Subtest: cross-note uses the target note, never the dependent fallback
ok 2835 - cross-note uses the target note, never the dependent fallback
  ---
  duration_ms: 1.912951
  ...
# Subtest: staging writes nothing until confirmed
ok 2836 - staging writes nothing until confirmed
  ---
  duration_ms: 1.113365
  ...
# Subtest: the shared planner matches the Task Card recommendation
ok 2837 - the shared planner matches the Task Card recommendation
  ---
  duration_ms: 62.695073
  ...
# Subtest: the preview table strings are exact
ok 2838 - the preview table strings are exact
  ---
  duration_ms: 1.892253
  ...
# Subtest: checklist tiers and unpreviewable rows report ok:false
ok 2839 - checklist tiers and unpreviewable rows report ok:false
  ---
  duration_ms: 0.529481
  ...
# Subtest: a silent config failure reports ok:false with no Notice
ok 2840 - a silent config failure reports ok:false with no Notice
  ---
  duration_ms: 0.211213
  ...
# Subtest: landing toasts append the preview after tails
ok 2841 - landing toasts append the preview after tails
  ---
  duration_ms: 1.353033
  ...
# Subtest: api.quickRoll has the v1 shape and never throws
ok 2842 - api.quickRoll has the v1 shape and never throws
  ---
  duration_ms: 2.628467
  ...
# Subtest: the preview matches what Alt+P then writes
ok 2843 - the preview matches what Alt+P then writes
  ---
  duration_ms: 24.81623
  ...
# Subtest: Alt+P matches Ctrl+Enter for roll, decay, project, and counted task writes
ok 2844 - Alt+P matches Ctrl+Enter for roll, decay, project, and counted task writes
  ---
  duration_ms: 110.120288
  ...
# Subtest: Alt+P matches Ctrl+Enter for a counted Task Link batch
ok 2845 - Alt+P matches Ctrl+Enter for a counted Task Link batch
  ---
  duration_ms: 30.242437
  ...
# Subtest: Task Link resolution keeps the outer modal hidden until its targets are ready
ok 2846 - Task Link resolution keeps the outer modal hidden until its targets are ready
  ---
  duration_ms: 9.242472
  ...
# Subtest: Alt+P hides immediate rolls and reveals the optional Next Work summary
ok 2847 - Alt+P hides immediate rolls and reveals the optional Next Work summary
  ---
  duration_ms: 10.878345
  ...
# Subtest: a cancel recommendation waits for the visible card and the second Alt+P cancels
ok 2848 - a cancel recommendation waits for the visible card and the second Alt+P cancels
  ---
  duration_ms: 8.658026
  ...
# Subtest: no priority and unavailable recurring tasks reveal the card without writing
ok 2849 - no priority and unavailable recurring tasks reveal the card without writing
  ---
  duration_ms: 3.019353
  ...
# Subtest: inbox routing is shown before the write and a managed line redirects to its owner
ok 2850 - inbox routing is shown before the write and a managed line redirects to its owner
  ---
  duration_ms: 12.875918
  ...
# Subtest: a landed review row advances once after Alt+P writes
ok 2851 - a landed review row advances once after Alt+P writes
  ---
  duration_ms: 14.81045
  ...
# Subtest: the card alias uses the physical Alt+P code and ignores repeats
ok 2852 - the card alias uses the physical Alt+P code and ignores repeats
  ---
  duration_ms: 3.539175
  ...
# Subtest: a throwing one-shot dispatch always reveals the still-open card
ok 2853 - a throwing one-shot dispatch always reveals the still-open card
  ---
  duration_ms: 3.559114
  ...
# Subtest: the registered command owns Alt+P and a Vim count is consumed once
ok 2854 - the registered command owns Alt+P and a Vim count is consumed once
  ---
  duration_ms: 8.967628
  ...
# Subtest: quick-roll visibility CSS disables the modal entrance animation
ok 2855 - quick-roll visibility CSS disables the modal entrance animation
  ---
  duration_ms: 1.412807
  ...
# Subtest: Less often picker renders actual rows from 90 days and Escape writes nothing
ok 2856 - Less often picker renders actual rows from 90 days and Escape writes nothing
  ---
  duration_ms: 11.196843
  ...
# Subtest: Less often picker renders actual rows from 120 days and Escape writes nothing
ok 2857 - Less often picker renders actual rows from 120 days and Escape writes nothing
  ---
  duration_ms: 1.311694
  ...
# Subtest: Less often picker renders actual rows from 180 days and Escape writes nothing
ok 2858 - Less often picker renders actual rows from 180 days and Escape writes nothing
  ---
  duration_ms: 0.645071
  ...
# Subtest: renderFooter skips malformed hints and retains valid structured hints
ok 2859 - renderFooter skips malformed hints and retains valid structured hints
  ---
  duration_ms: 0.358123
  ...
# Subtest: Pending refresh modal previews the dated Work Log and confirms once
ok 2860 - Pending refresh modal previews the dated Work Log and confirms once
  ---
  duration_ms: 3.197553
  ...
# Subtest: dismissing the Pending refresh modal cancels without a summary
ok 2861 - dismissing the Pending refresh modal cancels without a summary
  ---
  duration_ms: 0.613721
  ...
# Subtest: nav LK1–LK18 parse relation grammar and reject the other relation parser
ok 2862 - nav LK1–LK18 parse relation grammar and reject the other relation parser
  ---
  duration_ms: 5.792026
  ...
# Subtest: nav LK14–LK19 context and cross-parse rules
ok 2863 - nav LK14–LK19 context and cross-parse rules
  ---
  duration_ms: 0.915628
  ...
# Subtest: nav MC5 refuses relation embeds and MC16 keeps LINKS while dropping LINKED FROM
ok 2864 - nav MC5 refuses relation embeds and MC16 keeps LINKS while dropping LINKED FROM
  ---
  duration_ms: 2.785466
  ...
# Subtest: nav MC15 hands LINKS edits to the relation mirror and notices generated lines once
ok 2865 - nav MC15 hands LINKS edits to the relation mirror and notices generated lines once
  ---
  duration_ms: 4.336106
  ...
# Subtest: LG3: typed relation labels commit their text through the relation field
    # Subtest: add writes the typed label and mirror
    ok 1 - add writes the typed label and mirror
      ---
      duration_ms: 19.817928
      ...
    # Subtest: typed text is normalized before commit
    ok 2 - typed text is normalized before commit
      ---
      duration_ms: 2.566909
      ...
    # Subtest: relabel replaces an existing label and its mirror
    ok 3 - relabel replaces an existing label and its mirror
      ---
      duration_ms: 13.338872
      ...
    # Subtest: Linked from labels the other task's LINKS line
    ok 4 - Linked from labels the other task's LINKS line
      ---
      duration_ms: 2.382919
      ...
    # Subtest: suggestion, plain, and raw-input paths remain supported
    ok 5 - suggestion, plain, and raw-input paths remain supported
      ---
      duration_ms: 4.520409
      ...
    1..5
ok 2866 - LG3: typed relation labels commit their text through the relation field
  ---
  duration_ms: 48.505638
  ...
# Subtest: Linked from Shift+Enter goes through the relation field and labels the source
ok 2867 - Linked from Shift+Enter goes through the relation field and labels the source
  ---
  duration_ms: 3.290901
  ...
# Subtest: Linked from Shift+Enter relabels a CURRENT source
ok 2868 - Linked from Shift+Enter relabels a CURRENT source
  ---
  duration_ms: 8.41849
  ...
# Subtest: Linked from prompts for the owner's id then links
    # Subtest: plain Enter writes the owner id and the reverse link
    ok 1 - plain Enter writes the owner id and the reverse link
      ---
      duration_ms: 5.709127
      ...
    # Subtest: Shift+Enter labels the source after the owner id prompt
    ok 2 - Shift+Enter labels the source after the owner id prompt
      ---
      duration_ms: 2.568662
      ...
    1..2
ok 2869 - Linked from prompts for the owner's id then links
  ---
  duration_ms: 9.330288
  ...
# Subtest: Links to prompts for the selected task's id then links
ok 2870 - Links to prompts for the selected task's id then links
  ---
  duration_ms: 3.42629
  ...
# Subtest: Linked-from toasts name the source task
ok 2871 - Linked-from toasts name the source task
  ---
  duration_ms: 7.317428
  ...
# Subtest: links-to row follows blocks with N, first label, cut target, and +K
ok 2872 - links-to row follows blocks with N, first label, cut target, and +K
  ---
  duration_ms: 12.286553
  ...
# Subtest: links-to row stays available on closed tasks and empty LINKS lines
ok 2873 - links-to row stays available on closed tasks and empty LINKS lines
  ---
  duration_ms: 4.066531
  ...
# Subtest: links-to row refuses non-tasks and read-only notes
ok 2874 - links-to row refuses non-tasks and read-only notes
  ---
  duration_ms: 2.962425
  ...
# Subtest: card keycap l opens Links to; input focus keeps it quiet
ok 2875 - card keycap l opens Links to; input focus keeps it quiet
  ---
  duration_ms: 2.188999
  ...
# Subtest: card ⇧L shows live incoming detail and routes Ctrl+D by direction
ok 2876 - card ⇧L shows live incoming detail and routes Ctrl+D by direction
  ---
  duration_ms: 9.144054
  ...
# Subtest: index-only Linked-from rows convert 1-based edges into nav records
ok 2877 - index-only Linked-from rows convert 1-based edges into nav records
  ---
  duration_ms: 1.104908
  ...
# Subtest: card ⇧L detail cleans a raw index task line
ok 2878 - card ⇧L detail cleans a raw index task line
  ---
  duration_ms: 1.617768
  ...
# Subtest: Linked-from scans source LINKS, reverses built-in phrases, and ignores stored mirrors
ok 2879 - Linked-from scans source LINKS, reverses built-in phrases, and ignores stored mirrors
  ---
  duration_ms: 2.441651
  ...
# Subtest: LG7: reverse-stage Enter writes the source's LINKS and target mirror
ok 2880 - LG7: reverse-stage Enter writes the source's LINKS and target mirror
  ---
  duration_ms: 1.551142
  ...
# Subtest: LG12: counted Links to applies the chosen labelled target to every source
ok 2881 - LG12: counted Links to applies the chosen labelled target to every source
  ---
  duration_ms: 4.953736
  ...
# Subtest: LG8: Ctrl+Shift+P on a LINKS line resolves to the owner's stage
ok 2882 - LG8: Ctrl+Shift+P on a LINKS line resolves to the owner's stage
  ---
  duration_ms: 1.49324
  ...
# Subtest: pool keeps closed tasks and done/ archives, drops dailies and templates
ok 2883 - pool keeps closed tasks and done/ archives, drops dailies and templates
  ---
  duration_ms: 0.934013
  ...
# Subtest: stage lists CURRENT in authored order, then RESULTS, then CLOSED
ok 2884 - stage lists CURRENT in authored order, then RESULTS, then CLOSED
  ---
  duration_ms: 3.88759
  ...
# Subtest: LG4: missing CURRENT targets stay removable; malformed lines refuse
ok 2885 - LG4: missing CURRENT targets stay removable; malformed lines refuse
  ---
  duration_ms: 1.68189
  ...
# Subtest: prerequisite targets badge; id-less rows prompt
ok 2886 - prerequisite targets badge; id-less rows prompt
  ---
  duration_ms: 2.899635
  ...
# Subtest: subtitle, consequence strip, live sentence, and label refusal copy
ok 2887 - subtitle, consequence strip, live sentence, and label refusal copy
  ---
  duration_ms: 1.129085
  ...
# Subtest: LG15: marked rows plan one commit with adds and unlinks split
ok 2888 - LG15: marked rows plan one commit with adds and unlinks split
  ---
  duration_ms: 0.445179
  ...
# Subtest: LG1: stage link writes LINKS, mirror, and mint in one transaction
ok 2889 - LG1: stage link writes LINKS, mirror, and mint in one transaction
  ---
  duration_ms: 2.337411
  ...
# Subtest: LG2: cross-note mirror follows; a changed target suffixes the notice
ok 2890 - LG2: cross-note mirror follows; a changed target suffixes the notice
  ---
  duration_ms: 2.385884
  ...
# Subtest: LG4: CURRENT unlink removes the entry and its mirror entry
ok 2891 - LG4: CURRENT unlink removes the entry and its mirror entry
  ---
  duration_ms: 1.659207
  ...
# Subtest: LG6: archived targets link with the live-only suffix and no mirror
ok 2892 - LG6: archived targets link with the live-only suffix and no mirror
  ---
  duration_ms: 0.740413
  ...
# Subtest: LG13: linking never stamps, routes, or touches Depends-On lines
ok 2893 - LG13: linking never stamps, routes, or touches Depends-On lines
  ---
  duration_ms: 1.873767
  ...
# Subtest: LG15: two targets link in one gesture with one notice
ok 2894 - LG15: two targets link in one gesture with one notice
  ---
  duration_ms: 1.06345
  ...
# Subtest: LG5: id-less targets refuse at the writer, so the stage prompts first
ok 2895 - LG5: id-less targets refuse at the writer, so the stage prompts first
  ---
  duration_ms: 0.634371
  ...
# Subtest: LG7: Ctrl+Shift+P resolves LINKED FROM to its owner's reverse stage
ok 2896 - LG7: Ctrl+Shift+P resolves LINKED FROM to its owner's reverse stage
  ---
  duration_ms: 0.353696
  ...
# Subtest: api.relations openStage opens both directions at v1
ok 2897 - api.relations openStage opens both directions at v1
  ---
  duration_ms: 0.740263
  ...
# Subtest: relation-label stage Tab, Ctrl+D, pipe, and Ctrl+H mirror the card
ok 2898 - relation-label stage Tab, Ctrl+D, pipe, and Ctrl+H mirror the card
  ---
  duration_ms: 80.659824
  ...
# Subtest: relation-label rename preview reports done/ impact and checks affected editors
ok 2899 - relation-label rename preview reports done/ impact and checks affected editors
  ---
  duration_ms: 1.592149
  ...
# Subtest: relation-label rename modal re-previews, saves the active note, and confirms merges
ok 2900 - relation-label rename modal re-previews, saves the active note, and confirms merges
  ---
  duration_ms: 2.313255
  ...
# Subtest: Bob: Relation labels manager keeps hidden labels visible and delegates hide and unhide
ok 2901 - Bob: Relation labels manager keeps hidden labels visible and delegates hide and unhide
  ---
  duration_ms: 2.753386
  ...
# Subtest: one-off labels hide through bob only after the relation commit succeeds
ok 2902 - one-off labels hide through bob only after the relation commit succeeds
  ---
  duration_ms: 1.909325
  ...
# relations.linked_from_lines is invalid; treating as true
# Subtest: LW1 inserts an unlabelled LINKS line in the empty slot
ok 2903 - LW1 inserts an unlabelled LINKS line in the empty slot
  ---
  duration_ms: 7.71672
  ...
# Subtest: LW2 appends a labelled entry and LW3 is a byte-identical no-op
ok 2904 - LW2 appends a labelled entry and LW3 is a byte-identical no-op
  ---
  duration_ms: 3.522653
  ...
# Subtest: LW4 relabels in place and LW5/LW6 remove entries
ok 2905 - LW4 relabels in place and LW5/LW6 remove entries
  ---
  duration_ms: 2.230868
  ...
# Subtest: LW7 places LINKS after Sub-projects and LINKED FROM after LINKS
ok 2906 - LW7 places LINKS after Sub-projects and LINKED FROM after LINKS
  ---
  duration_ms: 4.101388
  ...
# Subtest: LW8 inserts LINKS as the first child when only user children exist
ok 2907 - LW8 inserts LINKS as the first child when only user children exist
  ---
  duration_ms: 1.290053
  ...
# Subtest: LW9 merges duplicate LINKS lines with first label winning
ok 2908 - LW9 merges duplicate LINKS lines with first label winning
  ---
  duration_ms: 1.377931
  ...
# Subtest: LW10 refuses a malformed LINKS line
ok 2909 - LW10 refuses a malformed LINKS line
  ---
  duration_ms: 0.559919
  ...
# Subtest: LW11 normalises and refuses labels
ok 2910 - LW11 normalises and refuses labels
  ---
  duration_ms: 1.025367
  ...
# Subtest: LW12 reuses a 4-space child indent
ok 2911 - LW12 reuses a 4-space child indent
  ---
  duration_ms: 0.654509
  ...
# Subtest: LW13 canonical link forms match Rust
ok 2912 - LW13 canonical link forms match Rust
  ---
  duration_ms: 1.195722
  ...
# Subtest: LW14 / LK20 LINKED FROM sort is byte-identical to Rust
ok 2913 - LW14 / LK20 LINKED FROM sort is byte-identical to Rust
  ---
  duration_ms: 0.977666
  ...
# Subtest: Rule 6 LINKED FROM planner table
ok 2914 - Rule 6 LINKED FROM planner table
  ---
  duration_ms: 3.130725
  ...
# Subtest: linkedFromDesiredAfterDelta keeps labels and sorts
ok 2915 - linkedFromDesiredAfterDelta keeps labels and sorts
  ---
  duration_ms: 0.976454
  ...
# Subtest: LG14 kill switch defaults on, honors false, and invalid values fall back on
ok 2916 - LG14 kill switch defaults on, honors false, and invalid values fall back on
  ---
  duration_ms: 3.115226
  ...
# Subtest: LG1 same-note add mints and writes LINKS plus LINKED FROM in one transaction
ok 2917 - LG1 same-note add mints and writes LINKS plus LINKED FROM in one transaction
  ---
  duration_ms: 10.060364
  ...
# Subtest: LG2 cross-note T follows the source commit; a changed target suffixes the notice
ok 2918 - LG2 cross-note T follows the source commit; a changed target suffixes the notice
  ---
  duration_ms: 8.877776
  ...
# Subtest: LG4 unlinks and relabels in place with the mirror
ok 2919 - LG4 unlinks and relabels in place with the mirror
  ---
  duration_ms: 5.467826
  ...
# Subtest: LG6 archived targets write LINKS without a mirror
ok 2920 - LG6 archived targets write LINKS without a mirror
  ---
  duration_ms: 2.1429
  ...
# Subtest: LG13 relation writes never stamp or change status
ok 2921 - LG13 relation writes never stamp or change status
  ---
  duration_ms: 2.024916
  ...
# Subtest: LG14 kill switch writes LINKS without a mirror or source mint
ok 2922 - LG14 kill switch writes LINKS without a mirror or source mint
  ---
  duration_ms: 1.47177
  ...
# Subtest: api.relations v1: removeLink works and openStage settles false without a plugin
ok 2923 - api.relations v1: removeLink works and openStage settles false without a plugin
  ---
  duration_ms: 5.417702
  ...
# Subtest: createDependencyNavApi mounts relations beside blocks
ok 2924 - createDependencyNavApi mounts relations beside blocks
  ---
  duration_ms: 1.221412
  ...
# Subtest: LG10: hand-edited LINKS mirrors to LINKED FROM and re-fires after undo
ok 2925 - LG10: hand-edited LINKS mirrors to LINKED FROM and re-fires after undo
  ---
  duration_ms: 6.866055
  ...
# Subtest: LG11: hand-editing generated LINKED FROM only shows its notice
ok 2926 - LG11: hand-editing generated LINKED FROM only shows its notice
  ---
  duration_ms: 0.958299
  ...
# Subtest: LG9: Ctrl+D's writer clears outgoing links and their generated mirrors
ok 2927 - LG9: Ctrl+D's writer clears outgoing links and their generated mirrors
  ---
  duration_ms: 3.897831
  ...
# Subtest: Alt+N release from a NEXT landing advances with one composed toast
ok 2928 - Alt+N release from a NEXT landing advances with one composed toast
  ---
  duration_ms: 48.871697
  ...
# Subtest: counted Alt+N lands past every handled key in one jump
ok 2929 - counted Alt+N lands past every handled key in one jump
  ---
  duration_ms: 26.004287
  ...
# Subtest: a cancelled Alt+N release prompt stays and frees the lock
ok 2930 - a cancelled Alt+N release prompt stays and frees the lock
  ---
  duration_ms: 14.139098
  ...
# Subtest: Alt+N on a checklist landing stays with the plain notice
ok 2931 - Alt+N on a checklist landing stays with the plain notice
  ---
  duration_ms: 12.22737
  ...
# Subtest: Alt+N off a landing behaves exactly as today
ok 2932 - Alt+N off a landing behaves exactly as today
  ---
  duration_ms: 12.347128
  ...
# Subtest: Alt+N while the gesture lock is held is swallowed
ok 2933 - Alt+N while the gesture lock is held is swallowed
  ---
  duration_ms: 10.172217
  ...
# Subtest: a Task Card priority commit on NEXT advances, landing after the rich card
ok 2934 - a Task Card priority commit on NEXT advances, landing after the rich card
  ---
  duration_ms: 57.626087
  ...
# Subtest: dismissing the Task Card stays and frees the lock
ok 2935 - dismissing the Task Card stays and frees the lock
  ---
  duration_ms: 15.115633
  ...
# Subtest: a frontmatter-only project edit from the card stays
ok 2936 - a frontmatter-only project edit from the card stays
  ---
  duration_ms: 13.042955
  ...
# Subtest: a same-day priority schedule on a checklist row stays
ok 2937 - a same-day priority schedule on a checklist row stays
  ---
  duration_ms: 23.008098
  ...
# Subtest: a future schedule on a checklist row advances
ok 2938 - a future schedule on a checklist row advances
  ---
  duration_ms: 29.726682
  ...
# Subtest: a Task Card cancel on a checklist row advances with the cancel card first
ok 2939 - a Task Card cancel on a checklist row advances with the cancel card first
  ---
  duration_ms: 19.071795
  ...
# Subtest: Ctrl+Shift+M from a landing follows the task and never advances
ok 2940 - Ctrl+Shift+M from a landing follows the task and never advances
  ---
  duration_ms: 20.489992
  ...
# Subtest: Ctrl+Shift+M from a checklist landing keeps the destination focus
ok 2941 - Ctrl+Shift+M from a checklist landing keeps the destination focus
  ---
  duration_ms: 12.002961
  ...
# Subtest: ]s after a landed move resumes at the successor despite the line shift
ok 2942 - ]s after a landed move resumes at the successor despite the line shift
  ---
  duration_ms: 37.755067
  ...
# Subtest: [s after a landed move resumes at the predecessor
ok 2943 - [s after a landed move resumes at the predecessor
  ---
  duration_ms: 14.641207
  ...
# Subtest: a counted move from a landing resumes past every moved target
ok 2944 - a counted move from a landing resumes past every moved target
  ---
  duration_ms: 18.050324
  ...
# Subtest: counted Ctrl+Shift+M command dispatch preserves a landed move count
ok 2945 - counted Ctrl+Shift+M command dispatch preserves a landed move count
  ---
  duration_ms: 22.293194
  ...
# Subtest: a stale landing is not parked
ok 2946 - a stale landing is not parked
  ---
  duration_ms: 12.606253
  ...
# Subtest: Ctrl+Shift+M while the gesture lock is held is swallowed
ok 2947 - Ctrl+Shift+M while the gesture lock is held is swallowed
  ---
  duration_ms: 1.173179
  ...
# Subtest: dismissing the move picker stays and frees the lock
ok 2948 - dismissing the move picker stays and frees the lock
  ---
  duration_ms: 9.296354
  ...
# Subtest: Ctrl+Shift+M off a landing behaves exactly as today
ok 2949 - Ctrl+Shift+M off a landing behaves exactly as today
  ---
  duration_ms: 11.19515
  ...
# Subtest: answer, move, answer stays in queue order past an accumulator alias
ok 2950 - answer, move, answer stays in queue order past an accumulator alias
  ---
  duration_ms: 5.01858
  ...
# Subtest: a move park ignores a stale accumulator alias
ok 2951 - a move park ignores a stale accumulator alias
  ---
  duration_ms: 0.922912
  ...
# Subtest: a re-indexed origin still advances from the landed row
ok 2952 - a re-indexed origin still advances from the landed row
  ---
  duration_ms: 2.801928
  ...
# Subtest: a landed move park clears the current review task
ok 2953 - a landed move park clears the current review task
  ---
  duration_ms: 0.695107
  ...
# Subtest: review settle follows the task through a BLOCKS insertion above (bob-cli-94)
ok 2954 - review settle follows the task through a BLOCKS insertion above (bob-cli-94)
  ---
  duration_ms: 21.037386
  ...
# Subtest: review settle follows a BLOCKS deletion above without advancing on a non-resolving edit
ok 2955 - review settle follows a BLOCKS deletion above without advancing on a non-resolving edit
  ---
  duration_ms: 13.009543
  ...
# Subtest: review settle never substitutes the cursor line and shares the inbox fallback reader
ok 2956 - review settle never substitutes the cursor line and shares the inbox fallback reader
  ---
  duration_ms: 3.234544
  ...
# Subtest: predicate: reviewOutcomeResolves across tiers and kinds
ok 2957 - predicate: reviewOutcomeResolves across tiers and kinds
  ---
  duration_ms: 4.227889
  ...
# Subtest: findReviewResumeIndex identifies rows by path and text
ok 2958 - findReviewResumeIndex identifies rows by path and text
  ---
  duration_ms: 0.902573
  ...
# Subtest: buildReviewMoveAnchor parks text-identified resume neighbours
ok 2959 - buildReviewMoveAnchor parks text-identified resume neighbours
  ---
  duration_ms: 1.667523
  ...
# Subtest: planReviewJump with a move anchor resumes at the walk neighbour
ok 2960 - planReviewJump with a move anchor resumes at the walk neighbour
  ---
  duration_ms: 3.070991
  ...
# Subtest: capture: null off a landing
ok 2961 - capture: null off a landing
  ---
  duration_ms: 13.04953
  ...
# Subtest: capture: frozen origin shape, BUSY while locked, expiry
ok 2962 - capture: frozen origin shape, BUSY while locked, expiry
  ---
  duration_ms: 1.736445
  ...
# Subtest: successor picker keeps a captured completion locked through selection and one walk toast
ok 2963 - successor picker keeps a captured completion locked through selection and one walk toast
  ---
  duration_ms: 41.75941
  ...
# Subtest: continue: refuses stale origins, showing the notice once
ok 2964 - continue: refuses stale origins, showing the notice once
  ---
  duration_ms: 18.383571
  ...
# Subtest: continue: stays on null and non-resolving outcomes
ok 2965 - continue: stays on null and non-resolving outcomes
  ---
  duration_ms: 3.179048
  ...
# Subtest: continue: stays for lane answers and mixed-version completes on checklist rows
ok 2966 - continue: stays for lane answers and mixed-version completes on checklist rows
  ---
  duration_ms: 9.289601
  ...
# Subtest: continue: a resolving lane answer advances exactly once with one composed toast
ok 2967 - continue: a resolving lane answer advances exactly once with one composed toast
  ---
  duration_ms: 4.006709
  ...
# Subtest: continue: counted handled refs land past every handled key in one jump
ok 2968 - continue: counted handled refs land past every handled key in one jump
  ---
  duration_ms: 3.467859
  ...
# Subtest: continue: wrap is announced and the empty queue composes the empty notice
ok 2969 - continue: wrap is announced and the empty queue composes the empty notice
  ---
  duration_ms: 4.131796
  ...
# Subtest: continue: anchor-only planning survives cursor drift and lagging queues
ok 2970 - continue: anchor-only planning survives cursor drift and lagging queues
  ---
  duration_ms: 7.628622
  ...
# Subtest: continue: POST origins never wrap
ok 2971 - continue: POST origins never wrap
  ---
  duration_ms: 14.920861
  ...
# Subtest: complete: the last lane row before POST stays with the next-step toast
ok 2972 - complete: the last lane row before POST stays with the next-step toast
  ---
  duration_ms: 3.99169
  ...
# Subtest: complete: a wrap onto a skipped PRE row stays
ok 2973 - complete: a wrap onto a skipped PRE row stays
  ---
  duration_ms: 3.188095
  ...
# Subtest: complete: a step into ROTTEN shows the boundary line
ok 2974 - complete: a step into ROTTEN shows the boundary line
  ---
  duration_ms: 4.603508
  ...
# Subtest: busy: walk keys, refresh, claim, and capture are swallowed in the settle window
ok 2975 - busy: walk keys, refresh, claim, and capture are swallowed in the settle window
  ---
  duration_ms: 7.255329
  ...
# Subtest: advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
ok 2976 - advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
  ---
  duration_ms: 12.52075
  ...
# Subtest: advance: decay choices advance except reword, with no preamble of their own
ok 2977 - advance: decay choices advance except reword, with no preamble of their own
  ---
  duration_ms: 1.235088
  ...
# Subtest: jump history: same-note and cross-note auto-advances record, and <C-o> returns
ok 2978 - jump history: same-note and cross-note auto-advances record, and <C-o> returns
  ---
  duration_ms: 15.943994
  ...
# Subtest: jump history: a manual ]s also records its landing
ok 2979 - jump history: a manual ]s also records its landing
  ---
  duration_ms: 3.466938
  ...
# Subtest: api: reviewWalk v3 is frozen with version 1, degrades null, never throws
ok 2980 - api: reviewWalk v3 is frozen with version 1, degrades null, never throws
  ---
  duration_ms: 2.976151
  ...
# Subtest: walk identity: a stale accumulator key never moves the anchor
ok 2981 - walk identity: a stale accumulator key never moves the anchor
  ---
  duration_ms: 0.652245
  ...
# Subtest: walk identity: a lagging answered row stays excluded
ok 2982 - walk identity: a lagging answered row stays excluded
  ---
  duration_ms: 0.433338
  ...
# Subtest: walk identity: a line-shifting answer lands on the true successor by text
ok 2983 - walk identity: a line-shifting answer lands on the true successor by text
  ---
  duration_ms: 0.437706
  ...
# Subtest: walk identity: legacy anchors without text resolve as before
ok 2984 - walk identity: legacy anchors without text resolve as before
  ---
  duration_ms: 0.505334
  ...
# Subtest: walk identity: matchFreshStampRefs prefers text over line
ok 2985 - walk identity: matchFreshStampRefs prefers text over line
  ---
  duration_ms: 0.313548
  ...
# Subtest: walk identity: collectReviewAnswerKeys separates position from exclusion
ok 2986 - walk identity: collectReviewAnswerKeys separates position from exclusion
  ---
  duration_ms: 0.71756
  ...
# Subtest: return: planReviewWalkReturn pure decisions
ok 2987 - return: planReviewWalkReturn pure decisions
  ---
  duration_ms: 0.677253
  ...
# Subtest: return: same-note ]s returns then steps, both directions
ok 2988 - return: same-note ]s returns then steps, both directions
  ---
  duration_ms: 3.001439
  ...
# Subtest: return: a different due row returns instead of stepping from there
ok 2989 - return: a different due row returns instead of stepping from there
  ---
  duration_ms: 1.245658
  ...
# Subtest: return: cross-note return re-arms and records <C-o>
ok 2990 - return: cross-note return re-arms and records <C-o>
  ---
  duration_ms: 10.238364
  ...
# Subtest: return: a count is consumed and ignored
ok 2991 - return: a count is consumed and ignored
  ---
  duration_ms: 1.626474
  ...
# Subtest: return: endpoints never return
ok 2992 - return: endpoints never return
  ---
  duration_ms: 0.984549
  ...
# Subtest: return: its own stamp ends it
ok 2993 - return: its own stamp ends it
  ---
  duration_ms: 1.808522
  ...
# Subtest: return: a stamp elsewhere does not end it
ok 2994 - return: a stamp elsewhere does not end it
  ---
  duration_ms: 1.388159
  ...
# Subtest: return: answers move the current task, a stopped Ctrl+Enter clears it
ok 2995 - return: answers move the current task, a stopped Ctrl+Enter clears it
  ---
  duration_ms: 7.469328
  ...
# Subtest: return: a stale landing falls through in the same press
ok 2996 - return: a stale landing falls through in the same press
  ---
  duration_ms: 1.772103
  ...
# Subtest: return: a day change never returns
ok 2997 - return: a day change never returns
  ---
  duration_ms: 1.023013
  ...
# Subtest: predicate: reviewOutcomeResolves for the RECURRING resolution table
ok 2998 - predicate: reviewOutcomeResolves for the RECURRING resolution table
  ---
  duration_ms: 1.072898
  ...
# Subtest: recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
ok 2999 - recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
  ---
  duration_ms: 0.412066
  ...
# Subtest: return: a RECURRING landing rearms the current-task return
ok 3000 - return: a RECURRING landing rearms the current-task return
  ---
  duration_ms: 0.748178
  ...
# Subtest: Ctrl+Alt+F after a Rotten Log insertion lands on the shifted successor exactly once
ok 3001 - Ctrl+Alt+F after a Rotten Log insertion lands on the shifted successor exactly once
  ---
  duration_ms: 5.612954
  ...
# Subtest: review answer outcome vectors map to the schema vocabulary
ok 3002 - review answer outcome vectors map to the schema vocabulary
  ---
  duration_ms: 2.549637
  ...
# Subtest: event builder uses the walk row key and its tier, once per distinct key
ok 3003 - event builder uses the walk row key and its tier, once per distinct key
  ---
  duration_ms: 2.473982
  ...
# Subtest: journal appends are queued and failures retain events without failing answers
ok 3004 - journal appends are queued and failures retain events without failing answers
  ---
  duration_ms: 14.424634
  ...
# Subtest: card after-line outcomes map done, drop, defer, sequence, and card
ok 3005 - card after-line outcomes map done, drop, defer, sequence, and card
  ---
  duration_ms: 2.389511
  ...
# Subtest: journal events carry plugin@manifest version with a 2.x fallback
ok 3006 - journal events carry plugin@manifest version with a 2.x fallback
  ---
  duration_ms: 1.93256
  ...
# Subtest: write failures show one notice per burst and a recovery notice
ok 3007 - write failures show one notice per burst and a recovery notice
  ---
  duration_ms: 1.495174
  ...
# Subtest: missing api.stats shows one session notice and later delivers retained events
ok 3008 - missing api.stats shows one session notice and later delivers retained events
  ---
  duration_ms: 1.512376
  ...
# Subtest: validation rejects drop the event and continue the drain
ok 3009 - validation rejects drop the event and continue the drain
  ---
  duration_ms: 1.689465
  ...
# Subtest: pending journal events cap at 500 and warn once per burst
ok 3010 - pending journal events cap at 500 and warn once per burst
  ---
  duration_ms: 3.739398
  ...
# Subtest: decay config defaults to enabled with one roll per level
ok 3011 - decay config defaults to enabled with one roll per level
  ---
  duration_ms: 5.450926
  ...
# Subtest: decay:false disables decay and level rolls are accepted but ignored
ok 3012 - decay:false disables decay and level rolls are accepted but ignored
  ---
  duration_ms: 0.846065
  ...
# Subtest: decay.rolls sets the limit and levels[].rolls overrides it
ok 3013 - decay.rolls sets the limit and levels[].rolls overrides it
  ---
  duration_ms: 0.655311
  ...
# Subtest: decay config rejects bad rolls, unknown keys and non-priority use
ok 3014 - decay config rejects bad rolls, unknown keys and non-priority use
  ---
  duration_ms: 1.187015
  ...
# Subtest: classifyScheduleLogRollReason sorts automatic heads from deliberate ones
ok 3015 - classifyScheduleLogRollReason sorts automatic heads from deliberate ones
  ---
  duration_ms: 1.1316
  ...
# Subtest: conformance vectors 1-10: streaks at P2 with the default limit
ok 3016 - conformance vectors 1-10: streaks at P2 with the default limit
  ---
  duration_ms: 6.015001
  ...
# Subtest: conformance vectors 11-15: custom limits, disabled decay and edges
ok 3017 - conformance vectors 11-15: custom limits, disabled decay and edges
  ---
  duration_ms: 1.352321
  ...
# Subtest: the streak reader follows log grammar: legacy labels, nesting and stops
ok 3018 - the streak reader follows log grammar: legacy labels, nesting and stops
  ---
  duration_ms: 1.409862
  ...
# Subtest: rollPriorityRecommendationDate avoids the current date when the window has room
ok 3019 - rollPriorityRecommendationDate avoids the current date when the window has room
  ---
  duration_ms: 1.133354
  ...
# Subtest: decay and cancel reason formatters use the exact ladder copy
ok 3020 - decay and cancel reason formatters use the exact ladder copy
  ---
  duration_ms: 0.548678
  ...
# Subtest: the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
ok 3021 - the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
  ---
  duration_ms: 0.888847
  ...
# Subtest: the planner returns null without a configured priority
ok 3022 - the planner returns null without a configured priority
  ---
  duration_ms: 0.389333
  ...
# Subtest: buildPriorityRollPreviewModel carries the row copy for every kind
ok 3023 - buildPriorityRollPreviewModel carries the row copy for every kind
  ---
  duration_ms: 1.239716
  ...
# Subtest: picker-single recognizes the recommended-roll keypress
ok 3024 - picker-single recognizes the recommended-roll keypress
  ---
  duration_ms: 0.522878
  ...
# Subtest: picker-single stage-two footers carry the recommended-roll hints
ok 3025 - picker-single stage-two footers carry the recommended-roll hints
  ---
  duration_ms: 1.130057
  ...
# Subtest: picker-single shares one roll between the preview and the pinned row
ok 3026 - picker-single shares one roll between the preview and the pinned row
  ---
  duration_ms: 1.258932
  ...
# Subtest: picker-single plans the next-roll hint for the notice chips
ok 3027 - picker-single plans the next-roll hint for the notice chips
  ---
  duration_ms: 1.492799
  ...
# Subtest: picker-single notice cards name the roll, decay and next press
ok 3028 - picker-single notice cards name the roll, decay and next press
  ---
  duration_ms: 3.545799
  ...
# Subtest: picker-single decay payload and preview-target comparison
ok 3029 - picker-single decay payload and preview-target comparison
  ---
  duration_ms: 0.888416
  ...
# Subtest: picker-counted plans one recommendation per target with skips
ok 3030 - picker-counted plans one recommendation per target with skips
  ---
  duration_ms: 4.346717
  ...
# Subtest: picker-counted batch preview, footer and notice copy
ok 3031 - picker-counted batch preview, footer and notice copy
  ---
  duration_ms: 3.224124
  ...
# Subtest: picker-counted composes cancel then set-priority into one postimage
ok 3032 - picker-counted composes cancel then set-priority into one postimage
  ---
  duration_ms: 8.213268
  ...
# Subtest: picker-counted refuses a recurring cancel as one batch
ok 3033 - picker-counted refuses a recurring cancel as one batch
  ---
  duration_ms: 7.196487
  ...
# Subtest: recommended roll recovers with [unblocked::] when the writer is passed
ok 3034 - recommended roll recovers with [unblocked::] when the writer is passed
  ---
  duration_ms: 2.925123
  ...
# Subtest: picker-counted stale lines refuse and new options stay byte-identical
ok 3035 - picker-counted stale lines refuse and new options stay byte-identical
  ---
  duration_ms: 3.364762
  ...
# Subtest: picker-links aggregates one recommendation per note
ok 3036 - picker-links aggregates one recommendation per note
  ---
  duration_ms: 4.178016
  ...
# Subtest: picker-links refuses a recurring cancel as one batch
ok 3037 - picker-links refuses a recurring cancel as one batch
  ---
  duration_ms: 0.854782
  ...
# Subtest: picker-links takes a single recommended roll with Ctrl+Enter
ok 3038 - picker-links takes a single recommended roll with Ctrl+Enter
  ---
  duration_ms: 100.179794
  ...
# Subtest: picker-links shows no pinned roll row in stage two
ok 3039 - picker-links shows no pinned roll row in stage two
  ---
  duration_ms: 12.837353
  ...
# Subtest: picker-links decays and cancels a single Task Link
ok 3040 - picker-links decays and cancels a single Task Link
  ---
  duration_ms: 12.715081
  ...
# Subtest: picker-links applies a mixed batch across two notes
ok 3041 - picker-links applies a mixed batch across two notes
  ---
  duration_ms: 15.786123
  ...
# Subtest: picker-links refuses the whole batch when a linked note changed
ok 3042 - picker-links refuses the whole batch when a linked note changed
  ---
  duration_ms: 5.651469
  ...
# Subtest: picker-links prunes today's open Pomodoro links
ok 3043 - picker-links prunes today's open Pomodoro links
  ---
  duration_ms: 11.447501
  ...
# Subtest: picker-single Ctrl+Enter rolls a P2 task in one undo group
ok 3044 - picker-single Ctrl+Enter rolls a P2 task in one undo group
  ---
  duration_ms: 19.299741
  ...
# Subtest: picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
ok 3045 - picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
  ---
  duration_ms: 13.782408
  ...
# Subtest: picker-single opens a ^prj task on inline scheduled for an immediate roll
ok 3046 - picker-single opens a ^prj task on inline scheduled for an immediate roll
  ---
  duration_ms: 15.843693
  ...
# Subtest: picker-counted opens on scheduled for an immediate mixed batch
ok 3047 - picker-counted opens on scheduled for an immediate mixed batch
  ---
  duration_ms: 16.895561
  ...
# Subtest: picker-links opens on scheduled for an immediate roll
ok 3048 - picker-links opens on scheduled for an immediate roll
  ---
  duration_ms: 14.077952
  ...
# Subtest: picker-single Ctrl+Enter decays a P2 task in one undo group
ok 3049 - picker-single Ctrl+Enter decays a P2 task in one undo group
  ---
  duration_ms: 16.284284
  ...
# Subtest: picker-single Ctrl+Enter cancels a P4 task in one undo group
ok 3050 - picker-single Ctrl+Enter cancels a P4 task in one undo group
  ---
  duration_ms: 13.988581
  ...
# Subtest: picker-single Ctrl+Enter in stage two writes the recommended roll
ok 3051 - picker-single Ctrl+Enter in stage two writes the recommended roll
  ---
  duration_ms: 19.425299
  ...
# Subtest: picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
ok 3052 - picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
  ---
  duration_ms: 5.777268
  ...
# Subtest: picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
ok 3053 - picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
  ---
  duration_ms: 8.351982
  ...
# Subtest: picker-single recurring P4 past the limit refuses and keeps the picker open
ok 3054 - picker-single recurring P4 past the limit refuses and keeps the picker open
  ---
  duration_ms: 12.616332
  ...
# Subtest: picker-single stale tasks refuse and re-render the decay preview
ok 3055 - picker-single stale tasks refuse and re-render the decay preview
  ---
  duration_ms: 13.27508
  ...
# Subtest: picker-single Ctrl+R on the card re-rolls the recommendation date
ok 3056 - picker-single Ctrl+R on the card re-rolls the recommendation date
  ---
  duration_ms: 4.129763
  ...
# Subtest: picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
ok 3057 - picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
  ---
  duration_ms: 2.67174
  ...
# Subtest: picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
ok 3058 - picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
  ---
  duration_ms: 11.758565
  ...
# Subtest: picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
ok 3059 - picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
  ---
  duration_ms: 12.892139
  ...
# Subtest: picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
ok 3060 - picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
  ---
  duration_ms: 13.909751
  ...
# Subtest: picker-counted Ctrl+Enter refuses when a target line changed
ok 3061 - picker-counted Ctrl+Enter refuses when a target line changed
  ---
  duration_ms: 13.175911
  ...
# Subtest: picker-counted Ctrl+Enter refuses a recurring cancel batch
ok 3062 - picker-counted Ctrl+Enter refuses a recurring cancel batch
  ---
  duration_ms: 12.758433
  ...
# Subtest: recommended roll on Pending offers a Work Log with the frozen date
ok 3063 - recommended roll on Pending offers a Work Log with the frozen date
  ---
  duration_ms: 1029.659365
  ...
# Subtest: recommended roll blank summary skips the Work Log without a fallback
ok 3064 - recommended roll blank summary skips the Work Log without a fallback
  ---
  duration_ms: 1023.907696
  ...
# Subtest: Ctrl+Enter in the Work Log stage confirms instead of re-rolling
ok 3065 - Ctrl+Enter in the Work Log stage confirms instead of re-rolling
  ---
  duration_ms: 1031.099844
  ...
# Subtest: counted recommended mixed batch logs only eligible roll and decay targets
ok 3066 - counted recommended mixed batch logs only eligible roll and decay targets
  ---
  duration_ms: 1021.699912
  ...
# Subtest: Task Link recommended roll deletes the emptied Pomodoro in the same daily write
ok 3067 - Task Link recommended roll deletes the emptied Pomodoro in the same daily write
  ---
  duration_ms: 3.818759
  ...
# Subtest: single keep logs still the primer with stamp in one undo
ok 3068 - single keep logs still the primer with stamp in one undo
  ---
  duration_ms: 24.00975
  ...
# Subtest: single keep logs blank with stamp in one undo
ok 3069 - single keep logs blank with stamp in one undo
  ---
  duration_ms: 2.962544
  ...
# Subtest: Esc retains the document and walk anchor; repeat command cannot open another prompt
ok 3070 - Esc retains the document and walk anchor; repeat command cannot open another prompt
  ---
  duration_ms: 1.306163
  ...
# Subtest: same-day repeat never prompts or appends, including saturated 999
ok 3071 - same-day repeat never prompts or appends, including saturated 999
  ---
  duration_ms: 4.26915
  ...
# Subtest: counted predicate: scheduled tickler
ok 3072 - counted predicate: scheduled tickler
  ---
  duration_ms: 0.567794
  ...
# Subtest: counted predicate: unblock tickler
ok 3073 - counted predicate: unblock tickler
  ---
  duration_ms: 0.18857
  ...
# Subtest: counted predicate: new
ok 3074 - counted predicate: new
  ---
  duration_ms: 0.175976
  ...
# Subtest: counted predicate: Pending
ok 3075 - counted predicate: Pending
  ---
  duration_ms: 0.264775
  ...
# Subtest: counted predicate: Next
ok 3076 - counted predicate: Next
  ---
  duration_ms: 0.427496
  ...
# Subtest: counted predicate: PROJECTS
ok 3077 - counted predicate: PROJECTS
  ---
  duration_ms: 0.37179
  ...
# Subtest: counted predicate: recurring
ok 3078 - counted predicate: recurring
  ---
  duration_ms: 0.301786
  ...
# Subtest: counted predicate: checklist
ok 3079 - counted predicate: checklist
  ---
  duration_ms: 0.238275
  ...
# Subtest: counted predicate: closed
ok 3080 - counted predicate: closed
  ---
  duration_ms: 0.748418
  ...
# Subtest: counted predicate: early
ok 3081 - counted predicate: early
  ---
  duration_ms: 0.395425
  ...
# Subtest: scheduled tickler logs; unblocked and legacy keeps never prompt
ok 3082 - scheduled tickler logs; unblocked and legacy keeps never prompt
  ---
  duration_ms: 4.391102
  ...
# Subtest: Pending retains its Work summary prompt
ok 3083 - Pending retains its Work summary prompt
  ---
  duration_ms: 3.110728
  ...
# Subtest: counted mixed sessions use one Work-first prompt and route each answer to its log
ok 3084 - counted mixed sessions use one Work-first prompt and route each answer to its log
  ---
  duration_ms: 5.356514
  ...
# Subtest: counted at-limit Rotten targets skip without opening a prompt or logging
ok 3085 - counted at-limit Rotten targets skip without opening a prompt or logging
  ---
  duration_ms: 1.782993
  ...
# Subtest: unavailable decay card falls through the reason planner
ok 3086 - unavailable decay card falls through the reason planner
  ---
  duration_ms: 7.022926
  ...
# Subtest: document changes while prompt is open refuse the entire keep
ok 3087 - document changes while prompt is open refuse the entire keep
  ---
  duration_ms: 1.730773
  ...
# Subtest: day changes while prompt is open refuse the entire keep
ok 3088 - day changes while prompt is open refuse the entire keep
  ---
  duration_ms: 1.419479
  ...
# Subtest: prediction changes while prompt is open refuse the entire keep
ok 3089 - prediction changes while prompt is open refuse the entire keep
  ---
  duration_ms: 4.758994
  ...
# Subtest: guard changes while prompt is open refuse the entire keep
ok 3090 - guard changes while prompt is open refuse the entire keep
  ---
  duration_ms: 1.072909
  ...
# Subtest: ambiguous Rotten markers disable the prompt and refuse even a bypass
ok 3091 - ambiguous Rotten markers disable the prompt and refuse even a bypass
  ---
  duration_ms: 2.128543
  ...
# Subtest: combined planner inserts nested targets bottom-up and preserves CRLF
ok 3092 - combined planner inserts nested targets bottom-up and preserves CRLF
  ---
  duration_ms: 1.12635
  ...
# Subtest: prompt copy separates streak from history and previews exact formatter output
ok 3093 - prompt copy separates streak from history and previews exact formatter output
  ---
  duration_ms: 0.694866
  ...
# Subtest: keep stage warns for inline fields, ignores IME Enter, and swallows both keep chords
ok 3094 - keep stage warns for inline fields, ignores IME Enter, and swallows both keep chords
  ---
  duration_ms: 2.312594
  ...
# Subtest: marker vectors match the Rust Rotten cases
ok 3095 - marker vectors match the Rust Rotten cases
  ---
  duration_ms: 3.706614
  ...
# Subtest: entry parsing accepts valid entries and rejects bad counts
ok 3096 - entry parsing accepts valid entries and rejects bad counts
  ---
  duration_ms: 0.795098
  ...
# Subtest: readRottenLog statuses cover missing, empty, ok, and unknown
ok 3097 - readRottenLog statuses cover missing, empty, ok, and unknown
  ---
  duration_ms: 1.651493
  ...
# Subtest: planManagedTaskLogEntry creates the log last and prepends entries
ok 3098 - planManagedTaskLogEntry creates the log last and prepends entries
  ---
  duration_ms: 1.822119
  ...
# Subtest: Work Log writes never file under the Rotten marker
ok 3099 - Work Log writes never file under the Rotten marker
  ---
  duration_ms: 1.22088
  ...
# Subtest: lane commit stamps an open Ready task
ok 3100 - lane commit stamps an open Ready task
  ---
  duration_ms: 6.183974
  ...
# Subtest: lane release stamps an open Next task
ok 3101 - lane release stamps an open Next task
  ---
  duration_ms: 0.563956
  ...
# Subtest: lane without a stamper leaves lines as they were
ok 3102 - lane without a stamper leaves lines as they were
  ---
  duration_ms: 0.273863
  ...
# Subtest: counted property set stamps every rewritten open task
ok 3103 - counted property set stamps every rewritten open task
  ---
  duration_ms: 3.287295
  ...
# Subtest: counted delete-property stamps the rewritten task
ok 3104 - counted delete-property stamps the rewritten task
  ---
  duration_ms: 0.93778
  ...
# Subtest: stamp lands before the suffix after a priority edit on a stamped line
ok 3105 - stamp lands before the suffix after a priority edit on a stamped line
  ---
  duration_ms: 0.90137
  ...
# Subtest: recurring tasks are never stamped
ok 3106 - recurring tasks are never stamped
  ---
  duration_ms: 0.383682
  ...
# Subtest: cancel never stamps
ok 3107 - cancel never stamps
  ---
  duration_ms: 2.170503
  ...
# Subtest: fresh and refresh never go through the end-append writers
ok 3108 - fresh and refresh never go through the end-append writers
  ---
  duration_ms: 0.55517
  ...
# Subtest: counted dependency edit stamps the rewritten parent
ok 3109 - counted dependency edit stamps the rewritten parent
  ---
  duration_ms: 11.380452
  ...
# Subtest: moved tasks are stamped at their destination
ok 3110 - moved tasks are stamped at their destination
  ---
  duration_ms: 7.019851
  ...
# Subtest: move without a stamper leaves lines as they were
ok 3111 - move without a stamper leaves lines as they were
  ---
  duration_ms: 1.18418
  ...
# Subtest: refresh row shows the effective interval in task mode
ok 3112 - refresh row shows the effective interval in task mode
  ---
  duration_ms: 1.641002
  ...
# Subtest: refresh row hides without the api and on closed tasks
ok 3113 - refresh row hides without the api and on closed tasks
  ---
  duration_ms: 0.527717
  ...
# Subtest: refresh row covers counted and link modes, including mixed
ok 3114 - refresh row covers counted and link modes, including mixed
  ---
  duration_ms: 0.749761
  ...
# Subtest: refresh value items offer presets and use default
ok 3115 - refresh value items offer presets and use default
  ---
  duration_ms: 2.297987
  ...
# Subtest: setRefreshLine stamps and sets or clears the interval
ok 3116 - setRefreshLine stamps and sets or clears the interval
  ---
  duration_ms: 0.870883
  ...
# Subtest: 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
ok 3117 - 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
  ---
  duration_ms: 22.803107
  ...
# Subtest: Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
ok 3118 - Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
  ---
  duration_ms: 14.404826
  ...
# Subtest: filtering expands matches, collapse state survives clearing, and hidden marks still submit
ok 3119 - filtering expands matches, collapse state survives clearing, and hidden marks still submit
  ---
  duration_ms: 22.175199
  ...
# Subtest: group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
ok 3120 - group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
  ---
  duration_ms: 12.223823
  ...
# Subtest: Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
ok 3121 - Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
  ---
  duration_ms: 2.542934
  ...
# Subtest: Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
ok 3122 - Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
  ---
  duration_ms: 9.791541
  ...
# Subtest: the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
ok 3123 - the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
  ---
  duration_ms: 1.819383
  ...
# Subtest: destination override shapes normalize and label
ok 3124 - destination override shapes normalize and label
  ---
  duration_ms: 0.721517
  ...
# Subtest: destination picker detection needs block-id-prompt api v1 with pick
ok 3125 - destination picker detection needs block-id-prompt api v1 with pick
  ---
  duration_ms: 0.452193
  ...
# Subtest: Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks
ok 3126 - Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks
  ---
  duration_ms: 9.501377
  ...
# Subtest: Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked
ok 3127 - Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked
  ---
  duration_ms: 1.480888
  ...
# Subtest: a cancelled destination pick and a missing picker leave rows untouched
ok 3128 - a cancelled destination pick and a missing picker leave rows untouched
  ---
  duration_ms: 2.161325
  ...
# Subtest: unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
ok 3129 - unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
  ---
  duration_ms: 1.603802
  ...
# Subtest: card model builds stable rows, scope metadata, and an existing recommendation
ok 3130 - card model builds stable rows, scope metadata, and an existing recommendation
  ---
  duration_ms: 18.157871
  ...
# Subtest: explicit preview builder matches writer rolls and deduplicates linked targets
ok 3131 - explicit preview builder matches writer rolls and deduplicates linked targets
  ---
  duration_ms: 1.44049
  ...
# Subtest: counted and linked card models report real target counts and mixed values
ok 3132 - counted and linked card models report real target counts and mixed values
  ---
  duration_ms: 7.667936
  ...
# Subtest: priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
ok 3133 - priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
  ---
  duration_ms: 4.31646
  ...
# Subtest: Escape, bare q, and Ctrl+[ close the card; nothing else does
ok 3134 - Escape, bare q, and Ctrl+[ close the card; nothing else does
  ---
  duration_ms: 1.933891
  ...
# Subtest: close keys never fire during composition or inside a text field
ok 3135 - close keys never fire during composition or inside a text field
  ---
  duration_ms: 2.422935
  ...
# Subtest: unavailable actions, input composition, and repeats stay safe
ok 3136 - unavailable actions, input composition, and repeats stay safe
  ---
  duration_ms: 4.122449
  ...
# Subtest: Blocks row summarizes warm-cache dependents and their last open reason
ok 3137 - Blocks row summarizes warm-cache dependents and their last open reason
  ---
  duration_ms: 4.816014
  ...
# Subtest: Blocks row refuses closed tasks and unencodable paths without an id
ok 3138 - Blocks row refuses closed tasks and unencodable paths without an id
  ---
  duration_ms: 4.586544
  ...
# Subtest: key resolver table covers lane state, API availability, and modifier guards
ok 3139 - key resolver table covers lane state, API availability, and modifier guards
  ---
  duration_ms: 2.952215
  ...
# Subtest: recurring cancellation and blocked lanes expose reasons instead of writes
ok 3140 - recurring cancellation and blocked lanes expose reasons instead of writes
  ---
  duration_ms: 1.332062
  ...
# Subtest: identity keys distinguish linked notes that share a line number
ok 3141 - identity keys distinguish linked notes that share a line number
  ---
  duration_ms: 3.479602
  ...
# Subtest: planScheduleReview opens for a bare date and skips when reason is known without Work Log
ok 3142 - planScheduleReview opens for a bare date and skips when reason is known without Work Log
  ---
  duration_ms: 1.537043
  ...
# Subtest: planScheduleReview counts unique tasks when Task Links repeat a target
ok 3143 - planScheduleReview counts unique tasks when Task Links repeat a target
  ---
  duration_ms: 0.644129
  ...
# Subtest: bare date on Ready opens a reason-only review and writes nothing until Enter
ok 3144 - bare date on Ready opens a reason-only review and writes nothing until Enter
  ---
  duration_ms: 61.926115
  ...
# Subtest: typed reason and blank reason on an existing Schedule Log keep per-target rules
ok 3145 - typed reason and blank reason on an existing Schedule Log keep per-target rules
  ---
  duration_ms: 19.240548
  ...
# Subtest: Ready vs Next vs Pending: only Next/Pending show Work summary
ok 3146 - Ready vs Next vs Pending: only Next/Pending show Work summary
  ---
  duration_ms: 30.121095
  ...
# Subtest: inline reason on Ready dispatches immediately; on Next it still reviews Work summary
ok 3147 - inline reason on Ready dispatches immediately; on Next it still reviews Work summary
  ---
  duration_ms: 10.895387
  ...
# Subtest: Tab moves from Reason to Work summary and Enter commits from either field
ok 3148 - Tab moves from Reason to Work summary and Enter commits from either field
  ---
  duration_ms: 7.26584
  ...
# Subtest: Back and Escape at both review fields write nothing
ok 3149 - Back and Escape at both review fields write nothing
  ---
  duration_ms: 11.659667
  ...
# Subtest: a target changed during review refuses with no write
ok 3150 - a target changed during review refuses with no write
  ---
  duration_ms: 4.91419
  ...
# Subtest: counted mixed targets share one review and one adapter call
ok 3151 - counted mixed targets share one review and one adapter call
  ---
  duration_ms: 6.7479
  ...
# Subtest: linked notes with equal line numbers both qualify
ok 3152 - linked notes with equal line numbers both qualify
  ---
  duration_ms: 5.06004
  ...
# Subtest: project lifecycle review names propagation and still writes once
ok 3153 - project lifecycle review names propagation and still writes once
  ---
  duration_ms: 10.836624
  ...
# Subtest: priority picks still skip the combined review and keep Work Log-only prompts
ok 3154 - priority picks still skip the combined review and keep Work Log-only prompts
  ---
  duration_ms: 5.045763
  ...
# Subtest: a typed date from the card's schedule row uses the combined review
ok 3155 - a typed date from the card's schedule row uses the combined review
  ---
  duration_ms: 4.581054
  ...
# Subtest: scheduling a Pending task goes straight to the combined review, never serial prompts
ok 3156 - scheduling a Pending task goes straight to the combined review, never serial prompts
  ---
  duration_ms: 3.003243
  ...
# Subtest: classic parser keeps ISO, M/D, and signed units and ignores concise forms
ok 3157 - classic parser keeps ISO, M/D, and signed units and ignores concise forms
  ---
  duration_ms: 7.282139
  ...
# Subtest: typed schedule resolver covers bare days, units, weekdays, and inline reasons
ok 3158 - typed schedule resolver covers bare days, units, weekdays, and inline reasons
  ---
  duration_ms: 2.523747
  ...
# Subtest: weekdays resolve to the next occurrence strictly after today
ok 3159 - weekdays resolve to the next occurrence strictly after today
  ---
  duration_ms: 0.503562
  ...
# Subtest: invalid leap dates, end-of-month offsets, and December rollover
ok 3160 - invalid leap dates, end-of-month offsets, and December rollover
  ---
  duration_ms: 0.693894
  ...
# Subtest: negative, overflow, malformed, and preset-filter queries are rejected without dates
ok 3161 - negative, overflow, malformed, and preset-filter queries are rejected without dates
  ---
  duration_ms: 0.447314
  ...
# Subtest: DST local-calendar arithmetic stays on calendar days in America/New_York
ok 3162 - DST local-calendar arithmetic stays on calendar days in America/New_York
  ---
  duration_ms: 274.423823
  ...
# Subtest: Task Card date stage previews weekday, ISO, relative distance, and rollover year
ok 3163 - Task Card date stage previews weekday, ISO, relative distance, and rollover year
  ---
  duration_ms: 31.943654
  ...
# Subtest: inline reason is preserved on the preview and skips the reason stage
ok 3164 - inline reason is preserved on the preview and skips the reason stage
  ---
  duration_ms: 27.627275
  ...
# Subtest: Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
ok 3165 - Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
  ---
  duration_ms: 8.474326
  ...
# Subtest: Shift+Enter on a Ready task commits in four gestures without a Work Log
ok 3166 - Shift+Enter on a Ready task commits in four gestures without a Work Log
  ---
  duration_ms: 5.681997
  ...
# Subtest: invalid typed dates render an error preview and do not write
ok 3167 - invalid typed dates render an error preview and do not write
  ---
  duration_ms: 6.24474
  ...
# Subtest: the card's schedule stage always uses the concise resolver
ok 3168 - the card's schedule stage always uses the concise resolver
  ---
  duration_ms: 4.70964
  ...
# Subtest: tomorrow stays a preset filter and is not stolen as a typed date
ok 3169 - tomorrow stays a preset filter and is not stolen as a typed date
  ---
  duration_ms: 7.552456
  ...
# Subtest: mixed Task Links preview one date and freeze that action with the inline reason
ok 3170 - mixed Task Links preview one date and freeze that action with the inline reason
  ---
  duration_ms: 9.285475
  ...
# Subtest: Ctrl+Enter still takes the recommended roll from the Task Card date stage
ok 3171 - Ctrl+Enter still takes the recommended roll from the Task Card date stage
  ---
  duration_ms: 3.743565
  ...
# Subtest: Modal harness models Obsidian 1.14 attachment and idempotent close
ok 3172 - Modal harness models Obsidian 1.14 attachment and idempotent close
  ---
  duration_ms: 4.410478
  ...
# Subtest: styles share key-card tokens and compact Task Card dimensions
ok 3173 - styles share key-card tokens and compact Task Card dimensions
  ---
  duration_ms: 0.45597
  ...
# Subtest: card renderer paints header, banner, strip, stable rows, more, and footer from the model
ok 3174 - card renderer paints header, banner, strip, stable rows, more, and footer from the model
  ---
  duration_ms: 26.208999
  ...
# Subtest: renderer does not consume randomness or invent recommendation data
ok 3175 - renderer does not consume randomness or invent recommendation data
  ---
  duration_ms: 4.423254
  ...
# Subtest: no-recommendation, cancel, mixed, long text, missing API, and error states render
ok 3176 - no-recommendation, cancel, mixed, long text, missing API, and error states render
  ---
  duration_ms: 19.101541
  ...
# Subtest: counted and linked cards disclose mixed values and Task Link notes
ok 3177 - counted and linked cards disclose mixed values and Task Link notes
  ---
  duration_ms: 13.113802
  ...
# Subtest: Ctrl+Shift+P always opens the Task Card, never the classic property list
ok 3178 - Ctrl+Shift+P always opens the Task Card, never the classic property list
  ---
  duration_ms: 6.945076
  ...
# Subtest: the plugin carries no Task Card pilot setting, date gate, or classic preference
ok 3179 - the plugin carries no Task Card pilot setting, date gate, or classic preference
  ---
  duration_ms: 24.175737
  ...
# Subtest: a leftover persisted taskCard flag is ignored and never rewritten
ok 3180 - a leftover persisted taskCard flag is ignored and never rewritten
  ---
  duration_ms: 10.55622
  ...
# Subtest: palette command is named Task card (set properties)
ok 3181 - palette command is named Task card (set properties)
  ---
  duration_ms: 17.334388
  ...
# Subtest: Task Card opens the compact card with dialog semantics and a close control
ok 3182 - Task Card opens the compact card with dialog semantics and a close control
  ---
  duration_ms: 3.498137
  ...
# Subtest: a More row opens that property's value stage, never a filter list, and Back restores the card
ok 3183 - a More row opens that property's value stage, never a filter list, and Back restores the card
  ---
  duration_ms: 7.329562
  ...
# Subtest: after open the actions list, not the Close button, has focus
ok 3184 - after open the actions list, not the Close button, has focus
  ---
  duration_ms: 10.394219
  ...
# Subtest: clicking card text keeps the card key router active exactly once
ok 3185 - clicking card text keeps the card key router active exactly once
  ---
  duration_ms: 30.395349
  ...
# Subtest: Ready card writes close from a key, P1 click, recommendations, and Alt+N
ok 3186 - Ready card writes close from a key, P1 click, recommendations, and Alt+N
  ---
  duration_ms: 12.272537
  ...
# Subtest: Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
ok 3187 - Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
  ---
  duration_ms: 12.765818
  ...
# Subtest: Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
ok 3188 - Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
  ---
  duration_ms: 6.535836
  ...
# Subtest: Ctrl+R recomputes and repaints the card recommendation
ok 3189 - Ctrl+R recomputes and repaints the card recommendation
  ---
  duration_ms: 2.820724
  ...
# Subtest: Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
ok 3190 - Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
  ---
  duration_ms: 27.653845
  ...
# Subtest: Task Link opens focused while resolving and consumes keys without replay
ok 3191 - Task Link opens focused while resolving and consumes keys without replay
  ---
  duration_ms: 6.081509
  ...
# Subtest: Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card
ok 3192 - Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card
  ---
  duration_ms: 3.397274
  ...
# Subtest: Ctrl+Shift+Alt+B on a Task Link opens the linked Blocks stage
ok 3193 - Ctrl+Shift+Alt+B on a Task Link opens the linked Blocks stage
  ---
  duration_ms: 2.169521
  ...
# Subtest: Task Link count replacement and source edits invalidate old resolutions
ok 3194 - Task Link count replacement and source edits invalidate old resolutions
  ---
  duration_ms: 1.840334
  ...
# Subtest: Task Link resolution failure and plugin unload close their shells
ok 3195 - Task Link resolution failure and plugin unload close their shells
  ---
  duration_ms: 2.413327
  ...
# Subtest: direct Depends on entry opens the dependency stage without painting the card or the list
ok 3196 - direct Depends on entry opens the dependency stage without painting the card or the list
  ---
  duration_ms: 1.58742
  ...
# Subtest: a direct stage for an unconfigured property closes instead of leaving an empty modal
ok 3197 - a direct stage for an unconfigured property closes instead of leaving an empty modal
  ---
  duration_ms: 0.506006
  ...
# Subtest: a refused direct stage closes instead of landing on a card or a list
ok 3198 - a refused direct stage closes instead of landing on a card or a list
  ---
  duration_ms: 0.898845
  ...
# Subtest: Ctrl+Shift+B lands on the Depends on stage with the same intent as card b
ok 3199 - Ctrl+Shift+B lands on the Depends on stage with the same intent as card b
  ---
  duration_ms: 4.590853
  ...
# Subtest: Ctrl+Shift+B Back returns to the card without re-dispatching
ok 3200 - Ctrl+Shift+B Back returns to the card without re-dispatching
  ---
  duration_ms: 2.637854
  ...
# Subtest: Ctrl+Shift+B on a plain bullet notices and closes the card
ok 3201 - Ctrl+Shift+B on a plain bullet notices and closes the card
  ---
  duration_ms: 1.507337
  ...
# Subtest: Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch
ok 3202 - Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch
  ---
  duration_ms: 5.424966
  ...
# Subtest: Ctrl+Shift+Alt+B on Depends-On and BLOCKS lines opens the owner's stage directly
ok 3203 - Ctrl+Shift+Alt+B on Depends-On and BLOCKS lines opens the owner's stage directly
  ---
  duration_ms: 9.030286
  ...
# Subtest: Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not
ok 3204 - Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not
  ---
  duration_ms: 12.553022
  ...
# Subtest: priority gesture writes the frozen date and duplicate dispatch is single-flight
ok 3205 - priority gesture writes the frozen date and duplicate dispatch is single-flight
  ---
  duration_ms: 11.8707
  ...
# Subtest: pending priority action passes its card preview through the Work Log adapter
ok 3206 - pending priority action passes its card preview through the Work Log adapter
  ---
  duration_ms: 1.710996
  ...
# Subtest: Task Link priority action refuses a stale cross-note preflight before writes
ok 3207 - Task Link priority action refuses a stale cross-note preflight before writes
  ---
  duration_ms: 7.010322
  ...
# Subtest: Task Link priority action rolls back earlier note writes after a later write fails
ok 3208 - Task Link priority action rolls back earlier note writes after a later write fails
  ---
  duration_ms: 4.328141
  ...
# Subtest: Task Link transaction reports a cleanup failure without implying global undo
ok 3209 - Task Link transaction reports a cleanup failure without implying global undo
  ---
  duration_ms: 1.798763
  ...
# Subtest: selected-property deletion uses the existing writer; other card rows stay non-deletable
ok 3210 - selected-property deletion uses the existing writer; other card rows stay non-deletable
  ---
  duration_ms: 3.615591
  ...
# Subtest: failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
ok 3211 - failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
  ---
  duration_ms: 2.05876
  ...
# Subtest: a refused deletion rebuilds the card from the refreshed line
ok 3212 - a refused deletion rebuilds the card from the refreshed line
  ---
  duration_ms: 2.129806
  ...
# Subtest: 0 deletes only priority and keeps the scheduled field byte-for-byte
ok 3213 - 0 deletes only priority and keeps the scheduled field byte-for-byte
  ---
  duration_ms: 2.239695
  ...
# Subtest: card keys pressed on a priority radio or the banner reach the resolver exactly once
ok 3214 - card keys pressed on a priority radio or the banner reach the resolver exactly once
  ---
  duration_ms: 4.922967
  ...
# Subtest: held or composing Enter on a radio or the banner never writes
ok 3215 - held or composing Enter on a radio or the banner never writes
  ---
  duration_ms: 2.435629
  ...
# Subtest: Escape, q, Q, and Ctrl+[ close the card without writing
ok 3216 - Escape, q, Q, and Ctrl+[ close the card without writing
  ---
  duration_ms: 5.541709
  ...
# Subtest: Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
ok 3217 - Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
  ---
  duration_ms: 1.654959
  ...
# Subtest: repeated close keys and a second close() are harmless
ok 3218 - repeated close keys and a second close() are harmless
  ---
  duration_ms: 1.871713
  ...
# Subtest: composition never closes the card or a stage
ok 3219 - composition never closes the card or a stage
  ---
  duration_ms: 1.756502
  ...
# Subtest: q typed into a stage's text field never closes the modal
ok 3220 - q typed into a stage's text field never closes the modal
  ---
  duration_ms: 1.552593
  ...
# Subtest: Ctrl+[ closes from a focused date field without writing
ok 3221 - Ctrl+[ closes from a focused date field without writing
  ---
  duration_ms: 1.342532
  ...
# Subtest: Ctrl+[ closes the schedule review from its Reason and Work summary fields
ok 3222 - Ctrl+[ closes the schedule review from its Reason and Work summary fields
  ---
  duration_ms: 15.357153
  ...
# Subtest: Ctrl+[ closes the summary-only schedule-work-log stage without writing
ok 3223 - Ctrl+[ closes the summary-only schedule-work-log stage without writing
  ---
  duration_ms: 3.414127
  ...
# Subtest: Ctrl+[ closes the lane-release Work summary without writing
ok 3224 - Ctrl+[ closes the lane-release Work summary without writing
  ---
  duration_ms: 2.559536
  ...
# Subtest: q closes from a focused More row and from the Close button
ok 3225 - q closes from a focused More row and from the Close button
  ---
  duration_ms: 4.59476
  ...
# Subtest: Ctrl+[ closes from focused card controls, the Back button, and the modal frame
ok 3226 - Ctrl+[ closes from focused card controls, the Back button, and the modal frame
  ---
  duration_ms: 5.905101
  ...
# Subtest: a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
ok 3227 - a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
  ---
  duration_ms: 14.215595
  ...
# Subtest: a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
ok 3228 - a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
  ---
  duration_ms: 4.467809
  ...
# Subtest: a direct dependency stage closes on Ctrl+[ but keeps q as typed text
ok 3229 - a direct dependency stage closes on Ctrl+[ but keeps q as typed text
  ---
  duration_ms: 1.116962
  ...
# Subtest: q and Ctrl+[ are not global closes: other modals and the decay card ignore them
ok 3230 - q and Ctrl+[ are not global closes: other modals and the decay card ignore them
  ---
  duration_ms: 1.493261
  ...
# Subtest: missing freshness API disables Review every with an honest reason
ok 3231 - missing freshness API disables Review every with an honest reason
  ---
  duration_ms: 1.100771
  ...
# Subtest: child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
ok 3232 - child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
  ---
  duration_ms: 2.04303
  ...
# Subtest: decay card keeps its classes and shares key-card tokens
ok 3233 - decay card keeps its classes and shares key-card tokens
  ---
  duration_ms: 0.260978
  ...
# Subtest: decay card footer always names the X drop alias; the trial date is not this gate
ok 3234 - decay card footer always names the X drop alias; the trial date is not this gate
  ---
  duration_ms: 0.462032
  ...
# Subtest: task card level chips reuse the shared priority mark when available
ok 3235 - task card level chips reuse the shared priority mark when available
  ---
  duration_ms: 1.602439
  ...
# Subtest: task card labels are unchanged without the priority mark api
ok 3236 - task card labels are unchanged without the priority mark api
  ---
  duration_ms: 5.635308
  ...
# Subtest: manifest order is authoritative and fragments share one lexical scope
ok 3237 - manifest order is authoritative and fragments share one lexical scope
  ---
  duration_ms: 517.202572
  ...
# Subtest: builds are deterministic and build:check is read-only on success
ok 3238 - builds are deterministic and build:check is read-only on success
  ---
  duration_ms: 704.398074
  ...
# Subtest: read-only check rejects changed fragments and edited generated output
ok 3239 - read-only check rejects changed fragments and edited generated output
  ---
  duration_ms: 696.123827
  ...
# Subtest: check rejects a missing generated bundle without writing it
ok 3240 - check rejects a missing generated bundle without writing it
  ---
  duration_ms: 227.187688
  ...
# Subtest: fragment line limit is enforced before writing output
ok 3241 - fragment line limit is enforced before writing output
  ---
  duration_ms: 1.506276
  ...
# Subtest: fragment syntax errors are rejected before writing output
ok 3242 - fragment syntax errors are rejected before writing output
  ---
  duration_ms: 114.667899
  ...
# Subtest: malformed, empty, duplicate, and traversal manifests are rejected read-only
    # Subtest: invalid JSON
    ok 1 - invalid JSON
      ---
      duration_ms: 0.920828
      ...
    # Subtest: empty manifest
    ok 2 - empty manifest
      ---
      duration_ms: 0.639961
      ...
    # Subtest: non-array manifest
    ok 3 - non-array manifest
      ---
      duration_ms: 1.779506
      ...
    # Subtest: duplicate entries
    ok 4 - duplicate entries
      ---
      duration_ms: 127.026771
      ...
    # Subtest: traversal entry
    ok 5 - traversal entry
      ---
      duration_ms: 1.12156
      ...
    # Subtest: absolute entry
    ok 6 - absolute entry
      ---
      duration_ms: 0.83275
      ...
    1..6
ok 3243 - malformed, empty, duplicate, and traversal manifests are rejected read-only
  ---
  duration_ms: 134.397119
  ...
# Subtest: missing and omitted fragments are rejected read-only
    # Subtest: missing manifest entry
    ok 1 - missing manifest entry
      ---
      duration_ms: 1.135988
      ...
    # Subtest: unlisted JavaScript source
    ok 2 - unlisted JavaScript source
      ---
      duration_ms: 124.028949
      ...
    1..2
ok 3244 - missing and omitted fragments are rejected read-only
  ---
  duration_ms: 125.96783
  ...
# Subtest: escaping fragment symlinks are rejected read-only
ok 3245 - escaping fragment symlinks are rejected read-only
  ---
  duration_ms: 2.267879
  ...
# Subtest: parity comparator identifies changed helper and plugin methods
ok 3246 - parity comparator identifies changed helper and plugin methods
  ---
  duration_ms: 16.866104
  ...
# Subtest: parity comparator accepts a mixin-split helper class but not a changed method or superclass
ok 3247 - parity comparator accepts a mixin-split helper class but not a changed method or superclass
  ---
  duration_ms: 1.022121
  ...
# Subtest: snapshot commands are available only for active Markdown files
ok 3248 - snapshot commands are available only for active Markdown files
  ---
  duration_ms: 4.837214
  ...
# Subtest: commands run bob ref create on the active path, with -C for closed tasks
ok 3249 - commands run bob ref create on the active path, with -C for closed tasks
  ---
  duration_ms: 6.157574
  ...
# Subtest: bob spawn uses the resolved path, vault environment, timeout, and NO_COLOR
ok 3250 - bob spawn uses the resolved path, vault environment, timeout, and NO_COLOR
  ---
  duration_ms: 2.453394
  ...
# Subtest: failure notices retain bob error and hint lines verbatim
ok 3251 - failure notices retain bob error and hint lines verbatim
  ---
  duration_ms: 0.601639
  ...
# Subtest: off desktop, bob spawning is refused with the desktop-app explanation
ok 3252 - off desktop, bob spawning is refused with the desktop-app explanation
  ---
  duration_ms: 0.549819
  ...
# Subtest: both prompt copies pass the shared fixture table identically
ok 3253 - both prompt copies pass the shared fixture table identically
  ---
  duration_ms: 16.860143
  ...
# Subtest: suggestion is valid, compact, and collision-aware
ok 3254 - suggestion is valid, compact, and collision-aware
  ---
  duration_ms: 1.336612
  ...
# Subtest: rename excludes exactly one old-ID occurrence
ok 3255 - rename excludes exactly one old-ID occurrence
  ---
  duration_ms: 0.380596
  ...
# Subtest: dependency legacy [id::] reuses only valid free IDs
ok 3256 - dependency legacy [id::] reuses only valid free IDs
  ---
  duration_ms: 0.634261
  ...
# Subtest: project conversion keeps the existing suggestBlockIdFromTask
ok 3257 - project conversion keeps the existing suggestBlockIdFromTask
  ---
  duration_ms: 1.28365
  ...
# Subtest: successor SB vectors are unchanged
ok 3258 - successor SB vectors are unchanged
  ---
  duration_ms: 1.916698
  ...
# Subtest: Linked-from CURRENT lists every checkbox status from the live index
ok 3259 - Linked-from CURRENT lists every checkbox status from the live index
  ---
  duration_ms: 45.778412
  ...
# Subtest: option-bracket ring reads Blocked as a source-only slot ahead of Ready
ok 3260 - option-bracket ring reads Blocked as a source-only slot ahead of Ready
  ---
  duration_ms: 2.945672
  ...
# Subtest: isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
ok 3261 - isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
  ---
  duration_ms: 0.667955
  ...
# Subtest: option-bracket refuses to change a member while its project is Blocked
ok 3262 - option-bracket refuses to change a member while its project is Blocked
  ---
  duration_ms: 4.948456
  ...
# Subtest: tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
ok 3263 - tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
  ---
  duration_ms: 3.230857
  ...
# Subtest: project resident notice reads the inline ^prj date and ignores frontmatter scheduled
ok 3264 - project resident notice reads the inline ^prj date and ignores frontmatter scheduled
  ---
  duration_ms: 0.814685
  ...
# Subtest: findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
ok 3265 - findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
  ---
  duration_ms: 0.574125
  ...
# Subtest: field removal collapses only the exposed span and preserves the rest of the line
ok 3266 - field removal collapses only the exposed span and preserves the rest of the line
  ---
  duration_ms: 0.496628
  ...
# Subtest: vault-path retirement preserves CRLF and a missing final newline
ok 3267 - vault-path retirement preserves CRLF and a missing final newline
  ---
  duration_ms: 1.893064
  ...
# Subtest: Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
ok 3268 - Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
  ---
  duration_ms: 0.965032
  ...
# Subtest: Schedule Log discovery ignores a marker owned by a nested grandchild
ok 3269 - Schedule Log discovery ignores a marker owned by a nested grandchild
  ---
  duration_ms: 0.463866
  ...
# Subtest: Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
ok 3270 - Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
  ---
  duration_ms: 0.738159
  ...
# Subtest: a task with no Schedule Log gets its field retired without any insertion or new marker
ok 3271 - a task with no Schedule Log gets its field retired without any insertion or new marker
  ---
  duration_ms: 4.736971
  ...
# Subtest: Schedule Log entry uses the canonical arrow, dash, and lock bytes
ok 3272 - Schedule Log entry uses the canonical arrow, dash, and lock bytes
  ---
  duration_ms: 0.288671
  ...
# Subtest: retirement stays a no-op for shapes that are not proof of a blocking date
ok 3273 - retirement stays a no-op for shapes that are not proof of a blocking date
  ---
  duration_ms: 0.681731
  ...
# Subtest: cycling Blocked backward to Cancelled retires the date and logs, matching forward
ok 3274 - cycling Blocked backward to Cancelled retires the date and logs, matching forward
  ---
  duration_ms: 15.950456
  ...
# Subtest: single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
ok 3275 - single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
  ---
  duration_ms: 3.087303
  ...
# Subtest: counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
ok 3276 - counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
  ---
  duration_ms: 3.003333
  ...
# Subtest: counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
ok 3277 - counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
  ---
  duration_ms: 1.546894
  ...
# Subtest: transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
ok 3278 - transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
  ---
  duration_ms: 6.192249
  ...
# Subtest: pressing again after Blocked retirement performs an ordinary transition with no further changes
ok 3279 - pressing again after Blocked retirement performs an ordinary transition with no further changes
  ---
  duration_ms: 0.695678
  ...
# Subtest: Alt+] on a date-blocked ^prj recovers open residents in step
ok 3280 - Alt+] on a date-blocked ^prj recovers open residents in step
  ---
  duration_ms: 33.017424
  ...
# Subtest: Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
ok 3281 - Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
  ---
  duration_ms: 1.623419
  ...
# Subtest: planProjectResidentRecoveryEdits recovers when a cross-note id is not open
ok 3282 - planProjectResidentRecoveryEdits recovers when a cross-note id is not open
  ---
  duration_ms: 0.636936
  ...
# Subtest: Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
ok 3283 - Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
  ---
  duration_ms: 2.242101
  ...
# Subtest: Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
ok 3284 - Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
  ---
  duration_ms: 4.910322
  ...
# Subtest: Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
ok 3285 - Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
  ---
  duration_ms: 3.705803
  ...
# Subtest: cycling a transcluded ^prj recovers residents in the source note
ok 3286 - cycling a transcluded ^prj recovers residents in the source note
  ---
  duration_ms: 1.566249
  ...
# Subtest: cycler BK1–BK12 accept and empty
ok 3287 - cycler BK1–BK12 accept and empty
  ---
  duration_ms: 2.774026
  ...
# Subtest: cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded
ok 3288 - cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded
  ---
  duration_ms: 1.204068
  ...
# Subtest: cycler MC4 strike/restore skip BLOCKS lines
ok 3289 - cycler MC4 strike/restore skip BLOCKS lines
  ---
  duration_ms: 1.576229
  ...
# Subtest: cycler MC3 tree close skips BLOCKS embeds
ok 3290 - cycler MC3 tree close skips BLOCKS embeds
  ---
  duration_ms: 1.914384
  ...
# Subtest: cycler MC1/MC2 Pomodoro and successor scanners skip managed lines
ok 3291 - cycler MC1/MC2 Pomodoro and successor scanners skip managed lines
  ---
  duration_ms: 1.913802
  ...
# Subtest: cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS
ok 3292 - cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS
  ---
  duration_ms: 0.398401
  ...
# Subtest: range planner preserves every single-item mode without an effective count
ok 3293 - range planner preserves every single-item mode without an effective count
  ---
  duration_ms: 18.295222
  ...
# Subtest: item counts carry children, skip blank lines and loose continuations, and clamp
ok 3294 - item counts carry children, skip blank lines and loose continuations, and clamp
  ---
  duration_ms: 0.730615
  ...
# Subtest: range stops at headings, shallower lines, same-level paragraphs and fences
ok 3295 - range stops at headings, shallower lines, same-level paragraphs and fences
  ---
  duration_ms: 0.309401
  ...
# Subtest: siblings require the exact whitespace and blockquote prefix
ok 3296 - siblings require the exact whitespace and blockquote prefix
  ---
  duration_ms: 0.239778
  ...
# Subtest: counted demotion moves four complete blocks to one existing section
ok 3297 - counted demotion moves four complete blocks to one existing section
  ---
  duration_ms: 8.772053
  ...
# Subtest: counted demotion creates a typed section or one default Requirements section
ok 3298 - counted demotion creates a typed section or one default Requirements section
  ---
  duration_ms: 4.197694
  ...
# Subtest: bottom-up removal splices blank seams and maps destinations before the source
ok 3299 - bottom-up removal splices blank seams and maps destinations before the source
  ---
  duration_ms: 0.813693
  ...
# Subtest: counted promotion Enter appends tasks in order and removes an emptied source section
ok 3300 - counted promotion Enter appends tasks in order and removes an emptied source section
  ---
  duration_ms: 1.749841
  ...
# Subtest: counted promotion to existing or new non-Tasks destinations keeps all bullets plain
ok 3301 - counted promotion to existing or new non-Tasks destinations keeps all bullets plain
  ---
  duration_ms: 1.663355
  ...
# Subtest: same-source Tasks promotion rewrites all selected lines in place
ok 3302 - same-source Tasks promotion rewrites all selected lines in place
  ---
  duration_ms: 1.447102
  ...
# Subtest: counted demotion outside Tasks moves to the next section in one write
ok 3303 - counted demotion outside Tasks moves to the next section in one write
  ---
  duration_ms: 0.882825
  ...
# Subtest: in-place ranges write once without centering for nested, non-dash, and unrouted items
ok 3304 - in-place ranges write once without centering for nested, non-dash, and unrouted items
  ---
  duration_ms: 1.513218
  ...
# Subtest: mixed demotion ranges count unchanged siblings and only move top-level dash tasks
ok 3305 - mixed demotion ranges count unchanged siblings and only move top-level dash tasks
  ---
  duration_ms: 0.74412
  ...
# Subtest: mixed promotion preserves existing tasks and a nonempty source section
ok 3306 - mixed promotion preserves existing tasks and a nonempty source section
  ---
  duration_ms: 0.545922
  ...
# Subtest: Vim action consumes explicit additional-item counts and preserves bare behavior
ok 3307 - Vim action consumes explicit additional-item counts and preserves bare behavior
  ---
  duration_ms: 3.084879
  ...
# Subtest: command checking preserves pending count; execution consumes it once and resets Vim
ok 3308 - command checking preserves pending count; execution consumes it once and resets Vim
  ---
  duration_ms: 2.051135
  ...
# Subtest: command route stays single without normal-mode explicit count and supports in-place ranges
ok 3309 - command route stays single without normal-mode explicit count and supports in-place ranges
  ---
  duration_ms: 0.793325
  ...
# Subtest: picker displays at most five preview rows plus overflow; single picker is unchanged
ok 3310 - picker displays at most five preview rows plus overflow; single picker is unchanged
  ---
  duration_ms: 2.87655
  ...
# Subtest: stale counted picker and cancelled picker never write
ok 3311 - stale counted picker and cancelled picker never write
  ---
  duration_ms: 1.611826
  ...
# Subtest: counted moves round-trip CRLF and preserve the presence or absence of a final newline
ok 3312 - counted moves round-trip CRLF and preserve the presence or absence of a final newline
  ---
  duration_ms: 8.351442
  ...
# Subtest: direct open/done transitions include incomplete statuses without broadening excluded statuses
ok 3313 - direct open/done transitions include incomplete statuses without broadening excluded statuses
  ---
  duration_ms: 3.25908
  ...
# Subtest: Ctrl+Enter block-link selection recognizes live and retired forms
ok 3314 - Ctrl+Enter block-link selection recognizes live and retired forms
  ---
  duration_ms: 5.237938
  ...
# Subtest: Pomodoro child ownership is status-neutral and bounded by contiguous list structure
ok 3315 - Pomodoro child ownership is status-neutral and bounded by contiguous list structure
  ---
  duration_ms: 1.768897
  ...
# Subtest: daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
ok 3316 - daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
  ---
  duration_ms: 0.73322
  ...
# Subtest: parsePomodoroEntryLineParts reads placeholder and range names conservatively
ok 3317 - parsePomodoroEntryLineParts reads placeholder and range names conservatively
  ---
  duration_ms: 1.449937
  ...
# Subtest: formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
ok 3318 - formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
  ---
  duration_ms: 0.37718
  ...
# Subtest: Pomodoro bullet toggle accepts empty indented list items
ok 3319 - Pomodoro bullet toggle accepts empty indented list items
  ---
  duration_ms: 0.825906
  ...
# Subtest: Pomodoro bullet toggle rejects non-empty or out-of-section bullets
ok 3320 - Pomodoro bullet toggle rejects non-empty or out-of-section bullets
  ---
  duration_ms: 0.29847
  ...
# Subtest: Pomodoro bullet toggle reverses only empty open childless placeholders
ok 3321 - Pomodoro bullet toggle reverses only empty open childless placeholders
  ---
  duration_ms: 1.088598
  ...
# Subtest: Pomodoro bullet toggle reverses named empty open childless placeholders
ok 3322 - Pomodoro bullet toggle reverses named empty open childless placeholders
  ---
  duration_ms: 3.341087
  ...
# Subtest: Pomodoro bullet toggle round trips and normalizes child indentation
ok 3323 - Pomodoro bullet toggle round trips and normalizes child indentation
  ---
  duration_ms: 0.617289
  ...
# Subtest: Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
ok 3324 - Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
  ---
  duration_ms: 0.509403
  ...
# Subtest: Pomodoro toggle key gate does not shadow bare Option bracket cycling
ok 3325 - Pomodoro toggle key gate does not shadow bare Option bracket cycling
  ---
  duration_ms: 0.397339
  ...
# Subtest: Pomodoro toggle command is daily-only and places the cursor for both directions
ok 3326 - Pomodoro toggle command is daily-only and places the cursor for both directions
  ---
  duration_ms: 1.325029
  ...
# Subtest: Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
ok 3327 - Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
  ---
  duration_ms: 1.081074
  ...
# Subtest: Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
ok 3328 - Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
  ---
  duration_ms: 4.399299
  ...
# Subtest: Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
ok 3329 - Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
  ---
  duration_ms: 64.294536
  ...
# Subtest: Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
ok 3330 - Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
  ---
  duration_ms: 2.410321
  ...
# Subtest: Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
ok 3331 - Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
  ---
  duration_ms: 0.930717
  ...
# Subtest: Ctrl+Enter closing the local line over an already-closed target does not write it a second time
ok 3332 - Ctrl+Enter closing the local line over an already-closed target does not write it a second time
  ---
  duration_ms: 0.889308
  ...
# Subtest: Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
ok 3333 - Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
  ---
  duration_ms: 0.988727
  ...
# Subtest: Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
ok 3334 - Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
  ---
  duration_ms: 2.881541
  ...
# Subtest: Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
ok 3335 - Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
  ---
  duration_ms: 1.073108
  ...
# Subtest: Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
ok 3336 - Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
  ---
  duration_ms: 0.95391
  ...
# Subtest: Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
ok 3337 - Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
  ---
  duration_ms: 0.921018
  ...
# Subtest: Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
ok 3338 - Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
  ---
  duration_ms: 1.106773
  ...
# Subtest: getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
ok 3339 - getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
  ---
  duration_ms: 5.001787
  ...
# Subtest: Ctrl+Enter close continues the walk with complete after finalize ran
ok 3340 - Ctrl+Enter close continues the walk with complete after finalize ran
  ---
  duration_ms: 14.476463
  ...
# Subtest: Ctrl+Enter close continues only after transclusion propagation landed
ok 3341 - Ctrl+Enter close continues only after transclusion propagation landed
  ---
  duration_ms: 12.829539
  ...
# Subtest: Ctrl+Enter reopen settles the walk with null
ok 3342 - Ctrl+Enter reopen settles the walk with null
  ---
  duration_ms: 12.587708
  ...
# Subtest: Ctrl+Enter swallows the key with no write while the walk is busy
ok 3343 - Ctrl+Enter swallows the key with no write while the walk is busy
  ---
  duration_ms: 12.072104
  ...
# Subtest: Ctrl+Enter with a null capture behaves exactly like today
ok 3344 - Ctrl+Enter with a null capture behaves exactly like today
  ---
  duration_ms: 12.833707
  ...
# Subtest: Ctrl+Enter with nav v2 or no nav keeps today's behavior
ok 3345 - Ctrl+Enter with nav v2 or no nav keeps today's behavior
  ---
  duration_ms: 24.179303
  ...
# Subtest: Ctrl+Enter lets the checklist claim win before capturing
ok 3346 - Ctrl+Enter lets the checklist claim win before capturing
  ---
  duration_ms: 1.558685
  ...
# Subtest: Ctrl+Enter settles the walk with null when the toggle rejects
ok 3347 - Ctrl+Enter settles the walk with null when the toggle rejects
  ---
  duration_ms: 12.361657
  ...
# Subtest: Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
ok 3348 - Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
  ---
  duration_ms: 3.594121
  ...
# Subtest: eligible Tasks demotions prompt in project and non-project notes
ok 3349 - eligible Tasks demotions prompt in project and non-project notes
  ---
  duration_ms: 6.607022
  ...
# Subtest: selectable headings skip YAML, fences, empty titles, and Tasks
ok 3350 - selectable headings skip YAML, fences, empty titles, and Tasks
  ---
  duration_ms: 2.23212
  ...
# Subtest: duplicate heading identities stay distinct and route to the chosen occurrence
ok 3351 - duplicate heading identities stay distinct and route to the chosen occurrence
  ---
  duration_ms: 1.864929
  ...
# Subtest: demotion picker defaults and typed names resolve without synthetic duplicates
ok 3352 - demotion picker defaults and typed names resolve without synthetic duplicates
  ---
  duration_ms: 3.335406
  ...
# Subtest: picker keyboard state wraps, clamps, and refuses invalid Enter
ok 3353 - picker keyboard state wraps, clamps, and refuses invalid Enter
  ---
  duration_ms: 0.76514
  ...
# Subtest: new-section formatting keeps extra blanks, final newlines, and nested children
ok 3354 - new-section formatting keeps extra blanks, final newlines, and nested children
  ---
  duration_ms: 1.351229
  ...
# Subtest: existing-section insertion works before and after the source on CRLF-backed editors
ok 3355 - existing-section insertion works before and after the source on CRLF-backed editors
  ---
  duration_ms: 12.336328
  ...
# Subtest: command opens one picker, writes only on accept, and restores cursor plus center
ok 3356 - command opens one picker, writes only on accept, and restores cursor plus center
  ---
  duration_ms: 2.171395
  ...
# Subtest: pointer activation, Escape, and double-submit protection leave a consistent note
ok 3357 - pointer activation, Escape, and double-submit protection leave a consistent note
  ---
  duration_ms: 2.265235
  ...
# Subtest: stale document, changed editor, or missing heading notice without writing
ok 3358 - stale document, changed editor, or missing heading notice without writing
  ---
  duration_ms: 2.89203
  ...
# Subtest: dependency normalizer writes path-qualified IDs and is idempotent
ok 3359 - dependency normalizer writes path-qualified IDs and is idempotent
  ---
  duration_ms: 4.220175
  ...
# Subtest: Tasks-generated IDs become local block IDs when none exists
ok 3360 - Tasks-generated IDs become local block IDs when none exists
  ---
  duration_ms: 1.921427
  ...
# Subtest: note rename rewrites target IDs and yields exact propagation mappings
ok 3361 - note rename rewrites target IDs and yields exact propagation mappings
  ---
  duration_ms: 0.542365
  ...
# Subtest: note rename also rewrites same-file dependsOn references
ok 3362 - note rename also rewrites same-file dependsOn references
  ---
  duration_ms: 0.308659
  ...
# Subtest: dependency normalization skips unsupported paths and fenced examples
ok 3363 - dependency normalization skips unsupported paths and fenced examples
  ---
  duration_ms: 0.802582
  ...
# Subtest: blocked-dependent planner matches the CLI dependency truth table
ok 3364 - blocked-dependent planner matches the CLI dependency truth table
  ---
  duration_ms: 4.5993
  ...
# Subtest: blocked-dependent edits preserve EOLs and skip stale lines idempotently
ok 3365 - blocked-dependent edits preserve EOLs and skip stale lines idempotently
  ---
  duration_ms: 1.423847
  ...
# Subtest: project recovery strips resident tags and works without freshness v12
ok 3366 - project recovery strips resident tags and works without freshness v12
  ---
  duration_ms: 5.819448
  ...
# Subtest: recovery passes daily-note and Today skip flags to ledger freshness
ok 3367 - recovery passes daily-note and Today skip flags to ledger freshness
  ---
  duration_ms: 0.700387
  ...
# Subtest: normalization mappings propagate to every dependent file
ok 3368 - normalization mappings propagate to every dependent file
  ---
  duration_ms: 1.530712
  ...
# Subtest: runtime normalizer skips unsupported paths with one informative notice
ok 3369 - runtime normalizer skips unsupported paths with one informative notice
  ---
  duration_ms: 1.049443
  ...
# Subtest: rename reconciliation rewrites the target and every dependent
ok 3370 - rename reconciliation rewrites the target and every dependent
  ---
  duration_ms: 0.870712
  ...
# Subtest: editor dependency normalization abandons and reschedules stale snapshots
ok 3371 - editor dependency normalization abandons and reschedules stale snapshots
  ---
  duration_ms: 0.802572
  ...
# Subtest: rename reconciliation abandons and reschedules stale editor snapshots
ok 3372 - rename reconciliation abandons and reschedules stale editor snapshots
  ---
  duration_ms: 0.555791
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 3373 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 1.18918
  ...
# Subtest: close-time retirement skips Depends-On lines
ok 3374 - close-time retirement skips Depends-On lines
  ---
  duration_ms: 1.804755
  ...
# Subtest: reopen restoration skips Depends-On lines instead of re-embedding them
ok 3375 - reopen restoration skips Depends-On lines instead of re-embedding them
  ---
  duration_ms: 0.90126
  ...
# Subtest: embedded-tree close collection ignores Depends-On lines
ok 3376 - embedded-tree close collection ignores Depends-On lines
  ---
  duration_ms: 0.622317
  ...
# Subtest: Alt-bracket bullet formatting never applies to Depends-On lines
ok 3377 - Alt-bracket bullet formatting never applies to Depends-On lines
  ---
  duration_ms: 0.829313
  ...
# Subtest: Ctrl+Enter on a dependency link closes only the target and runs the recovery
ok 3378 - Ctrl+Enter on a dependency link closes only the target and runs the recovery
  ---
  duration_ms: 2.556039
  ...
# Subtest: Ctrl+Enter on a dependency link reopens only the target, root-only
ok 3379 - Ctrl+Enter on a dependency link reopens only the target, root-only
  ---
  duration_ms: 1.63425
  ...
# Subtest: single and counted Alt-bracket cycle the dependency target under the cursor
ok 3380 - single and counted Alt-bracket cycle the dependency target under the cursor
  ---
  duration_ms: 27.844359
  ...
# Subtest: single and counted Alt-bracket report when the cursor is off every dependency link
ok 3381 - single and counted Alt-bracket report when the cursor is off every dependency link
  ---
  duration_ms: 0.944252
  ...
# Subtest: Ctrl+Enter candidate resolution finds plain links on Depends-On lines
ok 3382 - Ctrl+Enter candidate resolution finds plain links on Depends-On lines
  ---
  duration_ms: 0.4192
  ...
# Subtest: dependency-id normalisation never edits Depends-On lines
ok 3383 - dependency-id normalisation never edits Depends-On lines
  ---
  duration_ms: 0.521876
  ...
# Subtest: note rename rewrites fields while leaving Depends-On lines alone
ok 3384 - note rename rewrites fields while leaving Depends-On lines alone
  ---
  duration_ms: 0.302036
  ...
# Subtest: recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
ok 3385 - recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
  ---
  duration_ms: 3.022139
  ...
# Subtest: cycler freshness: local-fallback rewrite stamps last via injected stamper
ok 3386 - cycler freshness: local-fallback rewrite stamps last via injected stamper
  ---
  duration_ms: 3.215218
  ...
# Subtest: cycler freshness: rewrites without a stamper are unchanged (identity default)
ok 3387 - cycler freshness: rewrites without a stamper are unchanged (identity default)
  ---
  duration_ms: 0.510014
  ...
# Subtest: cycler freshness: a throwing stamper leaves the rewritten line intact
ok 3388 - cycler freshness: a throwing stamper leaves the rewritten line intact
  ---
  duration_ms: 0.223626
  ...
# Subtest: cycler freshness: transcluded rewrite stamps last via injected stamper
ok 3389 - cycler freshness: transcluded rewrite stamps last via injected stamper
  ---
  duration_ms: 0.276928
  ...
# Subtest: cycler freshness: cycling a plain line stamps through the follow-up edit
ok 3390 - cycler freshness: cycling a plain line stamps through the follow-up edit
  ---
  duration_ms: 1.342062
  ...
# Subtest: cycler freshness: Tasks-command rewrite with the expected status is stamped
ok 3391 - cycler freshness: Tasks-command rewrite with the expected status is stamped
  ---
  duration_ms: 0.441954
  ...
# Subtest: cycler freshness: Tasks command that inserts a line never stamps
ok 3392 - cycler freshness: Tasks command that inserts a line never stamps
  ---
  duration_ms: 0.391357
  ...
# Subtest: cycler freshness: Tasks command that deletes the line never stamps the next task
ok 3393 - cycler freshness: Tasks command that deletes the line never stamps the next task
  ---
  duration_ms: 0.392028
  ...
# Subtest: cycler freshness: Tasks command that leaves a different status never stamps
ok 3394 - cycler freshness: Tasks command that leaves a different status never stamps
  ---
  duration_ms: 0.494775
  ...
# Subtest: cycler freshness: cycling without ledger-tools writes no stamp
ok 3395 - cycler freshness: cycling without ledger-tools writes no stamp
  ---
  duration_ms: 0.448917
  ...
# Subtest: cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
ok 3396 - cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
  ---
  duration_ms: 0.264525
  ...
# Subtest: Pomodoro marker helpers normalize every block link and preserve fences and EOLs
ok 3397 - Pomodoro marker helpers normalize every block link and preserve fences and EOLs
  ---
  duration_ms: 5.718175
  ...
# Subtest: completed Pomodoro markers are normalized per occurrence
ok 3398 - completed Pomodoro markers are normalized per occurrence
  ---
  duration_ms: 1.274232
  ...
# Subtest: move-only Pomodoro links require a strict immediate hash directive
ok 3399 - move-only Pomodoro links require a strict immediate hash directive
  ---
  duration_ms: 5.50681
  ...
# Subtest: Pomodoro move-only planner toggles links across additional physical lines
ok 3400 - Pomodoro move-only planner toggles links across additional physical lines
  ---
  duration_ms: 4.518897
  ...
# Subtest: Pomodoro move-only planner round trips exact text and rejects strict non-matches
ok 3401 - Pomodoro move-only planner round trips exact text and rejects strict non-matches
  ---
  duration_ms: 1.166096
  ...
# Subtest: bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
ok 3402 - bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
  ---
  duration_ms: 6.903897
  ...
# Subtest: Pomodoro move-only runtime removes locally and validates additions independently
ok 3403 - Pomodoro move-only runtime removes locally and validates additions independently
  ---
  duration_ms: 2.200951
  ...
# Subtest: Pomodoro move-only runtime protects live lines after asynchronous failures
ok 3404 - Pomodoro move-only runtime protects live lines after asynchronous failures
  ---
  duration_ms: 0.769258
  ...
# Subtest: Pomodoro hash Vim mapping distinguishes bare and explicit repeats
ok 3405 - Pomodoro hash Vim mapping distinguishes bare and explicit repeats
  ---
  duration_ms: 15.818855
  ...
# Subtest: Pomodoro completion marks originals and carries clean live copies
ok 3406 - Pomodoro completion marks originals and carries clean live copies
  ---
  duration_ms: 12.019712
  ...
# Subtest: Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
ok 3407 - Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
  ---
  duration_ms: 2.539258
  ...
# Subtest: Pomodoro completion carries the closed Pomodoro name onto created entries
ok 3408 - Pomodoro completion carries the closed Pomodoro name onto created entries
  ---
  duration_ms: 0.914857
  ...
# Subtest: buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
ok 3409 - buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
  ---
  duration_ms: 1.10535
  ...
# Subtest: buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
ok 3410 - buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
  ---
  duration_ms: 0.568305
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is marked
ok 3411 - buildPomodoroCompletionPlan keeps source order when every carried link is marked
  ---
  duration_ms: 0.436654
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
ok 3412 - buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
  ---
  duration_ms: 0.663917
  ...
# Subtest: Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
ok 3413 - Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
  ---
  duration_ms: 12.000046
  ...
# Subtest: deferred-only close deletes the emptied entry and carries stripped links
ok 3414 - deferred-only close deletes the emptied entry and carries stripped links
  ---
  duration_ms: 1.840163
  ...
# Subtest: deferred-only close at EOF leaves no dangling newline
ok 3415 - deferred-only close at EOF leaves no dangling newline
  ---
  duration_ms: 0.533158
  ...
# Subtest: a close with a remaining copyable link keeps the [x] entry
ok 3416 - a close with a remaining copyable link keeps the [x] entry
  ---
  duration_ms: 0.820195
  ...
# Subtest: a prose sibling keeps the closed entry on a deferred close
ok 3417 - a prose sibling keeps the closed entry on a deferred close
  ---
  duration_ms: 0.656674
  ...
# Subtest: Ctrl+Enter deferred-only close deletes the entry in one gesture
ok 3418 - Ctrl+Enter deferred-only close deletes the entry in one gesture
  ---
  duration_ms: 4.529896
  ...
# Subtest: deferred-only close keeps a separated prose child and deletes fence-only leftovers whole
ok 3419 - deferred-only close keeps a separated prose child and deletes fence-only leftovers whole
  ---
  duration_ms: 4.352399
  ...
# Subtest: deferred-only successor relocation uses the inserted placeholder
ok 3420 - deferred-only successor relocation uses the inserted placeholder
  ---
  duration_ms: 0.516956
  ...
# Subtest: selected Done Pomodoro transclusion reopens only its cross-file root
ok 3421 - selected Done Pomodoro transclusion reopens only its cross-file root
  ---
  duration_ms: 12.758342
  ...
# Subtest: selected same-file Done target reopens root-only in the live editor
ok 3422 - selected same-file Done target reopens root-only in the live editor
  ---
  duration_ms: 2.30989
  ...
# Subtest: selected retired link reopens its root and restores the historical occurrence
ok 3423 - selected retired link reopens its root and restores the historical occurrence
  ---
  duration_ms: 2.150374
  ...
# Subtest: incomplete selected Pomodoro transclusion still closes recursively
ok 3424 - incomplete selected Pomodoro transclusion still closes recursively
  ---
  duration_ms: 3.850309
  ...
# Subtest: Done Pomodoro reopens direct roots and clears only its block-link markers
ok 3425 - Done Pomodoro reopens direct roots and clears only its block-link markers
  ---
  duration_ms: 9.340129
  ...
# Subtest: Done Pomodoro reopen restores its own block reference after reopening direct roots
ok 3426 - Done Pomodoro reopen restores its own block reference after reopening direct roots
  ---
  duration_ms: 1.589164
  ...
# Subtest: Done Pomodoro markers remain when the Todo transition does not occur
ok 3427 - Done Pomodoro markers remain when the Todo transition does not occur
  ---
  duration_ms: 0.550762
  ...
# Subtest: registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
ok 3428 - registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
  ---
  duration_ms: 21.807626
  ...
# Subtest: registered Ctrl+Enter immediately recovers a same-file dependent
ok 3429 - registered Ctrl+Enter immediately recovers a same-file dependent
  ---
  duration_ms: 17.054524
  ...
# Subtest: registered Ctrl+Enter immediately recovers a cross-file dependent
ok 3430 - registered Ctrl+Enter immediately recovers a cross-file dependent
  ---
  duration_ms: 4.10702
  ...
# Subtest: child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
ok 3431 - child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
  ---
  duration_ms: 4.147907
  ...
# Subtest: Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
ok 3432 - Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
  ---
  duration_ms: 2.71393
  ...
# Subtest: selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
ok 3433 - selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
  ---
  duration_ms: 4.935441
  ...
# Subtest: selected unresolved or excluded embedded children are consumed as no-ops
ok 3434 - selected unresolved or excluded embedded children are consumed as no-ops
  ---
  duration_ms: 1.943119
  ...
# Subtest: Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
ok 3435 - Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
  ---
  duration_ms: 3.719179
  ...
# Subtest: Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
ok 3436 - Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
  ---
  duration_ms: 5.617103
  ...
# Subtest: Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
ok 3437 - Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
  ---
  duration_ms: 2.421151
  ...
# Subtest: Pomodoro Work Log note-group collection scopes to direct children and requires descendants
ok 3438 - Pomodoro Work Log note-group collection scopes to direct children and requires descendants
  ---
  duration_ms: 1.800677
  ...
# Subtest: Work Log entry body formats as *date* — summary
ok 3439 - Work Log entry body formats as *date* — summary
  ---
  duration_ms: 0.271678
  ...
# Subtest: buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
ok 3440 - buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
  ---
  duration_ms: 0.464186
  ...
# Subtest: planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
ok 3441 - planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
  ---
  duration_ms: 0.682473
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
ok 3442 - planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
  ---
  duration_ms: 0.753879
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
ok 3443 - planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
  ---
  duration_ms: 0.38266
  ...
# Subtest: planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
ok 3444 - planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
  ---
  duration_ms: 0.500806
  ...
# Subtest: planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
ok 3445 - planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
  ---
  duration_ms: 0.487049
  ...
# Subtest: full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
ok 3446 - full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
  ---
  duration_ms: 16.440372
  ...
# Subtest: full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
ok 3447 - full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
  ---
  duration_ms: 3.427383
  ...
# Subtest: full Pomodoro completion keeps two same-task Work Log note sets in source order
ok 3448 - full Pomodoro completion keeps two same-task Work Log note sets in source order
  ---
  duration_ms: 2.836725
  ...
# Subtest: full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
ok 3449 - full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
  ---
  duration_ms: 2.344905
  ...
# Subtest: full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
ok 3450 - full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
  ---
  duration_ms: 2.002532
  ...
# Subtest: full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
ok 3451 - full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
  ---
  duration_ms: 1.511155
  ...
# Subtest: PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
ok 3452 - PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
  ---
  duration_ms: 2.57702
  ...
# Subtest: PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
ok 3453 - PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
  ---
  duration_ms: 1.449617
  ...
# Subtest: PP1 links the emptied project's ^prj as Next and strips \#hide
ok 3454 - PP1 links the emptied project's ^prj as Next and strips \#hide
  ---
  duration_ms: 16.83242
  ...
# Subtest: PP29 closing a child ^prj pulls in its empty parent project
ok 3455 - PP29 closing a child ^prj pulls in its empty parent project
  ---
  duration_ms: 4.776507
  ...
# Subtest: PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
ok 3456 - PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
  ---
  duration_ms: 1.623919
  ...
# Subtest: PP30 keeps the parent untouched while another child or task remains
ok 3457 - PP30 keeps the parent untouched while another child or task remains
  ---
  duration_ms: 1.690677
  ...
# Subtest: PP31 skips missing, ambiguous, and non-project parents
ok 3458 - PP31 skips missing, ambiguous, and non-project parents
  ---
  duration_ms: 2.110188
  ...
# Subtest: PP33 cancellation surfaces the parent without linking it
ok 3459 - PP33 cancellation surfaces the parent without linking it
  ---
  duration_ms: 3.182174
  ...
# Subtest: PP2 and PP3 leave a project with remaining work alone
ok 3460 - PP2 and PP3 leave a project with remaining work alone
  ---
  duration_ms: 1.835574
  ...
# Subtest: PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
ok 3461 - PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
  ---
  duration_ms: 3.276564
  ...
# Subtest: PP6 Sub-projects marker states match display_for_wikilink
ok 3462 - PP6 Sub-projects marker states match display_for_wikilink
  ---
  duration_ms: 2.676791
  ...
# Subtest: PP7 and PP28 keep a future-scheduled ^prj byte-identical
ok 3463 - PP7 and PP28 keep a future-scheduled ^prj byte-identical
  ---
  duration_ms: 2.049552
  ...
# Subtest: PP8 still-blocks a ^prj that waits on another open prerequisite
ok 3464 - PP8 still-blocks a ^prj that waits on another open prerequisite
  ---
  duration_ms: 1.089159
  ...
# Subtest: PP9 already-planned ^prj raises to Next without a new link
ok 3465 - PP9 already-planned ^prj raises to Next without a new link
  ---
  duration_ms: 1.125608
  ...
# Subtest: PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
ok 3466 - PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
  ---
  duration_ms: 3.271414
  ...
# Subtest: PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
ok 3467 - PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
  ---
  duration_ms: 2.000188
  ...
# Subtest: PP14 an id-less last task still pulls in
ok 3468 - PP14 an id-less last task still pulls in
  ---
  duration_ms: 1.166907
  ...
# Subtest: PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
ok 3469 - PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
  ---
  duration_ms: 13.342518
  ...
# Subtest: PP17 one pull-in row wins over project_task
ok 3470 - PP17 one pull-in row wins over project_task
  ---
  duration_ms: 1.272469
  ...
# Subtest: PP18 cancel recovers only
ok 3471 - PP18 cancel recovers only
  ---
  duration_ms: 0.698784
  ...
# Subtest: PP20 unrecognised or unplannable notes never pull in
ok 3472 - PP20 unrecognised or unplannable notes never pull in
  ---
  duration_ms: 2.566198
  ...
# Subtest: PP24 closing an external prerequisite pulls in only when N is empty
ok 3473 - PP24 closing an external prerequisite pulls in only when N is empty
  ---
  duration_ms: 1.347222
  ...
# Subtest: PP25 cascades project_member recovery after a [?] pull-in
ok 3474 - PP25 cascades project_member recovery after a [?] pull-in
  ---
  duration_ms: 1.90681
  ...
# Subtest: PP26 dated recount treats a hidden leftover as remaining work
ok 3475 - PP26 dated recount treats a hidden leftover as remaining work
  ---
  duration_ms: 1.138434
  ...
# Subtest: PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
ok 3476 - PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
  ---
  duration_ms: 2.043841
  ...
# Subtest: successorNoticeText uses the §12.6 pull-in and surfaced copy
ok 3477 - successorNoticeText uses the §12.6 pull-in and surfaced copy
  ---
  duration_ms: 0.909335
  ...
# Subtest: Ctrl+Enter on the last task link inserts the ^prj and rewrites R
ok 3478 - Ctrl+Enter on the last task link inserts the ^prj and rewrites R
  ---
  duration_ms: 20.90385
  ...
# Subtest: PP29 runtime close and reopen use the parent pull-in receipt
ok 3479 - PP29 runtime close and reopen use the parent pull-in receipt
  ---
  duration_ms: 8.663929
  ...
# Subtest: PP18 Alt+[ cancel of the last task surfaces R without linking
ok 3480 - PP18 Alt+[ cancel of the last task surfaces R without linking
  ---
  duration_ms: 39.709167
  ...
# Subtest: PP19 same-day reopen restores R byte-for-byte and takes back the link
ok 3481 - PP19 same-day reopen restores R byte-for-byte and takes back the link
  ---
  duration_ms: 5.965668
  ...
# Subtest: a close in a project that still has work stays inside the gate
ok 3482 - a close in a project that still has work stays inside the gate
  ---
  duration_ms: 1.778425
  ...
# Subtest: P1 path-qualified skip keys: same ^review in another note does not suppress
ok 3483 - P1 path-qualified skip keys: same ^review in another note does not suppress
  ---
  duration_ms: 1.095221
  ...
# Subtest: P3 id-less cascade: stale [?] R recovers resident without [id::]
ok 3484 - P3 id-less cascade: stale [?] R recovers resident without [id::]
  ---
  duration_ms: 1.003876
  ...
# Subtest: P4 frontmatter scheduled validity mirrors Rust
ok 3485 - P4 frontmatter scheduled validity mirrors Rust
  ---
  duration_ms: 1.151107
  ...
# Subtest: P5 recognition mirrors Rust (status/type/prj line)
ok 3486 - P5 recognition mirrors Rust (status/type/prj line)
  ---
  duration_ms: 2.922028
  ...
# Subtest: P6 SUBOPEN blank line stops the marker scan (PP6)
ok 3487 - P6 SUBOPEN blank line stops the marker scan (PP6)
  ---
  duration_ms: 0.98434
  ...
# Subtest: promotion prompts default to Tasks in ordinary and project notes
ok 3488 - promotion prompts default to Tasks in ordinary and project notes
  ---
  duration_ms: 8.059755
  ...
# Subtest: promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
ok 3489 - promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
  ---
  duration_ms: 1.751413
  ...
# Subtest: promotion command writes only on accept and Enter selects Tasks
ok 3490 - promotion command writes only on accept and Enter selects Tasks
  ---
  duration_ms: 5.316758
  ...
# Subtest: promotion removes only genuinely empty source sections
ok 3491 - promotion removes only genuinely empty source sections
  ---
  duration_ms: 2.027039
  ...
# Subtest: promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
ok 3492 - promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
  ---
  duration_ms: 1.636104
  ...
# Subtest: Tasks-only preamble promotions prompt and blank Enter moves into Tasks
ok 3493 - Tasks-only preamble promotions prompt and blank Enter moves into Tasks
  ---
  duration_ms: 3.798831
  ...
# Subtest: plain bullets already in Tasks prompt and blank Enter promotes in place
ok 3494 - plain bullets already in Tasks prompt and blank Enter promotes in place
  ---
  duration_ms: 3.806716
  ...
# Subtest: promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
ok 3495 - promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
  ---
  duration_ms: 1.250617
  ...
# Subtest: always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
ok 3496 - always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
  ---
  duration_ms: 5.801695
  ...
# Could not restore all reopened task references [ 'Broken.md: unreadable' ]
# Could not recover all blocked dependents [
#   'BrokenRead.md: read failed',
#   'Stale.md: line 1 changed before recovery',
#   'BrokenWrite.md: write failed'
# ]
# Subtest: direct Done Tasks task reopens through the metadata-aware fallback
ok 3497 - direct Done Tasks task reopens through the metadata-aware fallback
  ---
  duration_ms: 4.266834
  ...
# Subtest: recursive completion status policy includes Next without broadening excluded statuses
ok 3498 - recursive completion status policy includes Next without broadening excluded statuses
  ---
  duration_ms: 0.414361
  ...
# Subtest: recursive completion closes a Next root and its nested Next descendant
ok 3499 - recursive completion closes a Next root and its nested Next descendant
  ---
  duration_ms: 6.430245
  ...
# Subtest: recursive completion traverses Done parents and skips excluded siblings
ok 3500 - recursive completion traverses Done parents and skips excluded siblings
  ---
  duration_ms: 1.595075
  ...
# Subtest: closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
ok 3501 - closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
  ---
  duration_ms: 2.70322
  ...
# Subtest: reopened-reference restoration is ancestry-aware, conservative, and idempotent
ok 3502 - reopened-reference restoration is ancestry-aware, conservative, and idempotent
  ---
  duration_ms: 2.676268
  ...
# Subtest: retirement preserves task-tree markers and unmarks Pomodoro embeds
ok 3503 - retirement preserves task-tree markers and unmarks Pomodoro embeds
  ---
  duration_ms: 4.814911
  ...
# Subtest: done Pomodoro retirement removes only the matching embedded marker
ok 3504 - done Pomodoro retirement removes only the matching embedded marker
  ---
  duration_ms: 0.629361
  ...
# Subtest: retirement stops at prose boundaries and pairs strikethrough spans
ok 3505 - retirement stops at prose boundaries and pairs strikethrough spans
  ---
  duration_ms: 0.83822
  ...
# Subtest: retired Pomodoro links are not copied into the next Pomodoro
ok 3506 - retired Pomodoro links are not copied into the next Pomodoro
  ---
  duration_ms: 2.901168
  ...
# Subtest: retirement coordinator rewrites active editor and vault notes together
ok 3507 - retirement coordinator rewrites active editor and vault notes together
  ---
  duration_ms: 3.19076
  ...
# Subtest: restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
ok 3508 - restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
  ---
  duration_ms: 5.55886
  ...
# Subtest: close and reopen reference mutations share one serialized queue
ok 3509 - close and reopen reference mutations share one serialized queue
  ---
  duration_ms: 0.85902
  ...
# Subtest: post-close finalizer runs one gated plan before reference retirement
ok 3510 - post-close finalizer runs one gated plan before reference retirement
  ---
  duration_ms: 1.252551
  ...
# Subtest: dependent recovery uses live editor buffers and preserves the cursor
ok 3511 - dependent recovery uses live editor buffers and preserves the cursor
  ---
  duration_ms: 5.77323
  ...
# Subtest: dependent recovery preserves successful siblings across stale and failed notes
ok 3512 - dependent recovery preserves successful siblings across stale and failed notes
  ---
  duration_ms: 3.204487
  ...
# Subtest: no-op vault transforms and irrelevant retirement files avoid process writes
ok 3513 - no-op vault transforms and irrelevant retirement files avoid process writes
  ---
  duration_ms: 0.68658
  ...
# Subtest: ambiguity scans and notices are cached while dependency identity lines stay stable
ok 3514 - ambiguity scans and notices are cached while dependency identity lines stay stable
  ---
  duration_ms: 1.481638
  ...
# Subtest: non-Vim open/done command finalizes the closed task identity
ok 3515 - non-Vim open/done command finalizes the closed task identity
  ---
  duration_ms: 1.111011
  ...
# Subtest: non-Vim open/done command restores the reopened task identity
ok 3516 - non-Vim open/done command restores the reopened task identity
  ---
  duration_ms: 0.993326
  ...
# Subtest: full Pomodoro completion retires embeds only after carry-forward planning
ok 3517 - full Pomodoro completion retires embeds only after carry-forward planning
  ---
  duration_ms: 11.249975
  ...
# Subtest: full Pomodoro completion recovers after a deduplicated multi-target batch
ok 3518 - full Pomodoro completion recovers after a deduplicated multi-target batch
  ---
  duration_ms: 15.179986
  ...
# Subtest: full Pomodoro completion moves a marked same-note link without history
ok 3519 - full Pomodoro completion moves a marked same-note link without history
  ---
  duration_ms: 2.281956
  ...
# Subtest: closed-reference retirement never duplicates a daily Task Link into the completed fallback (bob-cli-2l)
ok 3520 - closed-reference retirement never duplicates a daily Task Link into the completed fallback (bob-cli-2l)
  ---
  duration_ms: 1.433387
  ...
# Subtest: cycler LK1–LK19 recognises only relation line shapes
ok 3521 - cycler LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 3.815542
  ...
# Subtest: cycler MC10, MC11, MC12 and MC14 keep relations inert while allowing root-only gestures
ok 3522 - cycler MC10, MC11, MC12 and MC14 keep relations inert while allowing root-only gestures
  ---
  duration_ms: 4.825401
  ...
# Subtest: SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
ok 3523 - SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
  ---
  duration_ms: 27.523107
  ...
# Subtest: SO2–SO5 fan-outs with explicit selection (SO32 twenty)
ok 3524 - SO2–SO5 fan-outs with explicit selection (SO32 twenty)
  ---
  duration_ms: 13.269969
  ...
# Subtest: SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
ok 3525 - SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
  ---
  duration_ms: 2.360507
  ...
# Subtest: SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
ok 3526 - SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
  ---
  duration_ms: 2.610903
  ...
# Subtest: SO stable keys survive insertions/status changes; ambiguous rebinding refused
ok 3527 - SO stable keys survive insertions/status changes; ambiguous rebinding refused
  ---
  duration_ms: 4.538072
  ...
# Subtest: SO picker model, pick normalization, and API detection
ok 3528 - SO picker model, pick normalization, and API detection
  ---
  duration_ms: 1.097185
  ...
# Subtest: SO notice copy for offers (SO20, mixed, failure)
ok 3529 - SO notice copy for offers (SO20, mixed, failure)
  ---
  duration_ms: 0.972246
  ...
# Subtest: destination override to an existing entry inserts as its child
ok 3530 - destination override to an existing entry inserts as its child
  ---
  duration_ms: 3.244763
  ...
# Subtest: destination override with a stale preimage skips loudly
ok 3531 - destination override with a stale preimage skips loudly
  ---
  duration_ms: 1.294721
  ...
# Subtest: destination override with a closed entry skips loudly
ok 3532 - destination override with a closed entry skips loudly
  ---
  duration_ms: 1.067588
  ...
# Subtest: destination override with a new name creates one placeholder after the running entry
ok 3533 - destination override with a new name creates one placeholder after the running entry
  ---
  duration_ms: 1.289551
  ...
# Subtest: destination override with a new name racing an open entry joins it
ok 3534 - destination override with a new name racing an open entry joins it
  ---
  duration_ms: 1.02164
  ...
# Subtest: reopen takes back the untouched successor link and restores status
ok 3535 - reopen takes back the untouched successor link and restores status
  ---
  duration_ms: 49.791703
  ...
# Subtest: an edited successor bullet survives while its status still restores
ok 3536 - an edited successor bullet survives while its status still restores
  ---
  duration_ms: 5.835069
  ...
# Subtest: an edited successor status line survives while its link is taken back
ok 3537 - an edited successor status line survives while its link is taken back
  ---
  duration_ms: 5.621119
  ...
# Subtest: reopen on a different day leaves successor links alone
ok 3538 - reopen on a different day leaves successor links alone
  ---
  duration_ms: 4.271924
  ...
# Subtest: reopening a task closed without a pass shows no take-back
ok 3539 - reopening a task closed without a pass shows no take-back
  ---
  duration_ms: 2.140697
  ...
# Subtest: Alt+] on a planned prerequisite links its successor
ok 3540 - Alt+] on a planned prerequisite links its successor
  ---
  duration_ms: 16.033575
  ...
# Subtest: take-back deletes a pre-existing entry it empties
ok 3541 - take-back deletes a pre-existing entry it empties
  ---
  duration_ms: 4.737122
  ...
# Subtest: take-back deletes a stub-replaced entry through the vault
ok 3542 - take-back deletes a stub-replaced entry through the vault
  ---
  duration_ms: 0.855954
  ...
# Subtest: take-back keeps entries that are closed or keep another child
ok 3543 - take-back keeps entries that are closed or keep another child
  ---
  duration_ms: 0.408049
  ...
# Subtest: closing-entry relocation finds a deferred-only placeholder
ok 3544 - closing-entry relocation finds a deferred-only placeholder
  ---
  duration_ms: 0.512939
  ...
# Subtest: Alt+[ into Cancelled recovers its dependents without linking
ok 3545 - Alt+[ into Cancelled recovers its dependents without linking
  ---
  duration_ms: 7.062793
  ...
# Subtest: take-back keeps an entry whose prose survives across a blank line (both paths)
ok 3546 - take-back keeps an entry whose prose survives across a blank line (both paths)
  ---
  duration_ms: 2.24263
  ...
# Subtest: take-back deletes a whole block with continuation/fence leftovers (LF/CRLF, final newline)
ok 3547 - take-back deletes a whole block with continuation/fence leftovers (LF/CRLF, final newline)
  ---
  duration_ms: 1.972906
  ...
# Subtest: link close links the unblocked successor into the slot and shows the nav card
ok 3548 - link close links the unblocked successor into the slot and shows the nav card
  ---
  duration_ms: 34.355948
  ...
# Subtest: close with no [id::] performs zero vault reads and shows nothing
ok 3549 - close with no [id::] performs zero vault reads and shows nothing
  ---
  duration_ms: 1.654037
  ...
# Subtest: Warm finalize reads no unrelated note bodies on the real close path
ok 3550 - Warm finalize reads no unrelated note bodies on the real close path
  ---
  duration_ms: 8.417848
  ...
# Subtest: cold fallback still recovers and links without a Tasks cache
ok 3551 - cold fallback still recovers and links without a Tasks cache
  ---
  duration_ms: 4.272045
  ...
# Subtest: recovered-only close reports unblocked without linking (SO4 Esc)
ok 3552 - recovered-only close reports unblocked without linking (SO4 Esc)
  ---
  duration_ms: 3.120246
  ...
# Subtest: walk landing composes a single toast and shows no card
ok 3553 - walk landing composes a single toast and shows no card
  ---
  duration_ms: 16.467123
  ...
# Subtest: nav absent falls back to a plain Notice with no link (SO missing picker)
ok 3554 - nav absent falls back to a plain Notice with no link (SO missing picker)
  ---
  duration_ms: 3.36836
  ...
# Subtest: stale cache heals via re-plan from fresh text (SO30)
ok 3555 - stale cache heals via re-plan from fresh text (SO30)
  ---
  duration_ms: 3.812708
  ...
# Subtest: Pomodoro-line close appends the successor to the created continuation
ok 3556 - Pomodoro-line close appends the successor to the created continuation
  ---
  duration_ms: 8.327664
  ...
# Subtest: Pomodoro-line close keeps the closing anchor after the picker re-plan
ok 3557 - Pomodoro-line close keeps the closing anchor after the picker re-plan
  ---
  duration_ms: 6.718375
  ...
# Subtest: completeTaskAtCursor returns the notice and shows nothing itself
ok 3558 - completeTaskAtCursor returns the notice and shows nothing itself
  ---
  duration_ms: 4.182554
  ...
# Subtest: successor apply recovers project residents without ledger v12
ok 3559 - successor apply recovers project residents without ledger v12
  ---
  duration_ms: 14.612532
  ...
# Subtest: SB vectors pin the successor mint pipeline
ok 3560 - SB vectors pin the successor mint pipeline
  ---
  duration_ms: 4.535899
  ...
# Subtest: successor suggester ports the Rust candidate and suffix rules
ok 3561 - successor suggester ports the Rust candidate and suffix rules
  ---
  duration_ms: 2.017952
  ...
# Subtest: successor link form names unique basenames short and the day file always
ok 3562 - successor link form names unique basenames short and the day file always
  ---
  duration_ms: 0.805567
  ...
# Subtest: tasksFromDocuments normalizes vault lines to pool shape
ok 3563 - tasksFromDocuments normalizes vault lines to pool shape
  ---
  duration_ms: 4.97189
  ...
# Subtest: normalizeTasksCacheTask ports every known Tasks shape
ok 3564 - normalizeTasksCacheTask ports every known Tasks shape
  ---
  duration_ms: 0.899768
  ...
# Subtest: buildDependentsIndex keeps first task IDs and groups dependents
ok 3565 - buildDependentsIndex keeps first task IDs and groups dependents
  ---
  duration_ms: 0.378423
  ...
# Subtest: findLiveLinks counts plain, embedded, and deferred links under open entries only
ok 3566 - findLiveLinks counts plain, embedded, and deferred links under open entries only
  ---
  duration_ms: 4.423745
  ...
# Subtest: computeSuccessorAnchors implements closing, slot, inherit, and none
ok 3567 - computeSuccessorAnchors implements closing, slot, inherit, and none
  ---
  duration_ms: 1.749269
  ...
# Subtest: SL1 links the successor right after the predecessor bullet
ok 3568 - SL1 links the successor right after the predecessor bullet
  ---
  duration_ms: 13.168255
  ...
# Subtest: SL3 still-blocked rows count the open prerequisites left
ok 3569 - SL3 still-blocked rows count the open prerequisites left
  ---
  duration_ms: 1.647675
  ...
# Subtest: SL4 future-scheduled dependents stay Blocked with the date row
ok 3570 - SL4 future-scheduled dependents stay Blocked with the date row
  ---
  duration_ms: 1.165404
  ...
# Subtest: SL5 already-planned dependents recover without a duplicate link
ok 3571 - SL5 already-planned dependents recover without a duplicate link
  ---
  duration_ms: 2.224607
  ...
# Subtest: SL6 struck and closed-entry links do not count as planned
ok 3572 - SL6 struck and closed-entry links do not count as planned
  ---
  duration_ms: 1.862735
  ...
# Subtest: SL7 closing anchors create the continuation placeholder
ok 3573 - SL7 closing anchors create the continuation placeholder
  ---
  duration_ms: 2.0901
  ...
# Subtest: SL8 closing anchors append after carried lines in the continuation
ok 3574 - SL8 closing anchors append after carried lines in the continuation
  ---
  duration_ms: 1.845273
  ...
# Subtest: SL9 unplanned predecessors offer at the implicit destination (SO14)
ok 3575 - SL9 unplanned predecessors offer at the implicit destination (SO14)
  ---
  duration_ms: 2.620451
  ...
# Subtest: SL10 missing block IDs mint through the SB rule
ok 3576 - SL10 missing block IDs mint through the SB rule
  ---
  duration_ms: 1.404591
  ...
# Subtest: SL11 project and hidden tasks recover but never link
ok 3577 - SL11 project and hidden tasks recover but never link
  ---
  duration_ms: 10.693032
  ...
# Subtest: PDC1 leaves a dependency-ready resident Blocked while its project still waits
ok 3578 - PDC1 leaves a dependency-ready resident Blocked while its project still waits
  ---
  duration_ms: 3.248371
  ...
# Subtest: PDC2 residents are offered under the project group (SO1)
ok 3579 - PDC2 residents are offered under the project group (SO1)
  ---
  duration_ms: 2.109857
  ...
# Subtest: PDC3 keeps a project resident Blocked when its own prerequisite remains open
ok 3580 - PDC3 keeps a project resident Blocked when its own prerequisite remains open
  ---
  duration_ms: 1.816457
  ...
# Subtest: PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
ok 3581 - PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
  ---
  duration_ms: 2.504911
  ...
# Subtest: SL12 one gesture closing two prerequisites links once with both causes
ok 3582 - SL12 one gesture closing two prerequisites links once with both causes
  ---
  duration_ms: 0.914756
  ...
# Subtest: SL13 chains do not recurse: the dependent's own dependents wait
ok 3583 - SL13 chains do not recurse: the dependent's own dependents wait
  ---
  duration_ms: 0.87477
  ...
# Subtest: SL14 ambiguous basenames link long
ok 3584 - SL14 ambiguous basenames link long
  ---
  duration_ms: 0.614122
  ...
# Subtest: SL15 stale open dependents link and become Next
ok 3585 - SL15 stale open dependents link and become Next
  ---
  duration_ms: 0.824213
  ...
# Subtest: SL16 gates on [id::]: no identity means no lookup and empty rows
ok 3586 - SL16 gates on [id::]: no identity means no lookup and empty rows
  ---
  duration_ms: 0.343316
  ...
# Subtest: SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
ok 3587 - SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
  ---
  duration_ms: 2.12101
  ...
# Subtest: SL18 the kill switch recovers without linking or minting
ok 3588 - SL18 the kill switch recovers without linking or minting
  ---
  duration_ms: 0.513881
  ...
# Subtest: SL19 re-applied closes write nothing and report nothing
ok 3589 - SL19 re-applied closes write nothing and report nothing
  ---
  duration_ms: 0.364105
  ...
# Subtest: SL23 subtasks anchor at their root's link
ok 3590 - SL23 subtasks anchor at their root's link
  ---
  duration_ms: 0.636715
  ...
# Subtest: SL24 later same-name entries take the closing successors
ok 3591 - SL24 later same-name entries take the closing successors
  ---
  duration_ms: 0.945785
  ...
# Subtest: SL25 already-Next planned dependents produce no row
ok 3592 - SL25 already-Next planned dependents produce no row
  ---
  duration_ms: 3.918569
  ...
# Subtest: SL26 inbox successors carry the inbox flag
ok 3593 - SL26 inbox successors carry the inbox flag
  ---
  duration_ms: 1.010729
  ...
# Subtest: SL27 dropped links are never re-linked and recover to Ready
ok 3594 - SL27 dropped links are never re-linked and recover to Ready
  ---
  duration_ms: 1.081374
  ...
# Subtest: SL28 day-file successors name the note, never the bare link
ok 3595 - SL28 day-file successors name the note, never the bare link
  ---
  duration_ms: 0.779077
  ...
# Subtest: slot insertions land after the anchor subtree with its indent
ok 3596 - slot insertions land after the anchor subtree with its indent
  ---
  duration_ms: 0.776162
  ...
# Subtest: closing insertions replace a lone stub child
ok 3597 - closing insertions replace a lone stub child
  ---
  duration_ms: 0.664489
  ...
# Subtest: insertions skip placements with no valid target
ok 3598 - insertions skip placements with no valid target
  ---
  duration_ms: 0.309662
  ...
# Subtest: successorNoticeText implements the §12.6 table
ok 3599 - successorNoticeText implements the §12.6 table
  ---
  duration_ms: 1.680127
  ...
# Subtest: parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
ok 3600 - parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
  ---
  duration_ms: 1.39887
  ...
# Subtest: loadLinkUnblocked stat-caches the config read
ok 3601 - loadLinkUnblocked stat-caches the config read
  ---
  duration_ms: 0.800418
  ...
# Subtest: loadLinkUnblocked treats missing or unreadable config as true
ok 3602 - loadLinkUnblocked treats missing or unreadable config as true
  ---
  duration_ms: 1.65531
  ...
# Subtest: successorPlanConfigPath honors XDG_CONFIG_HOME
ok 3603 - successorPlanConfigPath honors XDG_CONFIG_HOME
  ---
  duration_ms: 0.416415
  ...
# Subtest: todayDailyPath mirrors the ledger daily path
ok 3604 - todayDailyPath mirrors the ledger daily path
  ---
  duration_ms: 1.090352
  ...
# Subtest: normalizeClosedTaskIdentities keeps the anchor root off the match gate
ok 3605 - normalizeClosedTaskIdentities keeps the anchor root off the match gate
  ---
  duration_ms: 0.479335
  ...
# Subtest: ID-less planned roots anchor ID-bearing children without minting IDs
ok 3606 - ID-less planned roots anchor ID-bearing children without minting IDs
  ---
  duration_ms: 1.15798
  ...
# Subtest: successor anchors never guess across roots
ok 3607 - successor anchors never guess across roots
  ---
  duration_ms: 1.018584
  ...
# Subtest: a child with its own live link keeps its own slot
ok 3608 - a child with its own live link keeps its own slot
  ---
  duration_ms: 0.973348
  ...
# Subtest: getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
ok 3609 - getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
  ---
  duration_ms: 0.818182
  ...
# Subtest: countSuccessorBasenames walks the vault set, not the task set
ok 3610 - countSuccessorBasenames walks the vault set, not the task set
  ---
  duration_ms: 0.808322
  ...
# Subtest: the pass threads a richer isInbox into unblocked rows
ok 3611 - the pass threads a richer isInbox into unblocked rows
  ---
  duration_ms: 0.782023
  ...
# Subtest: getTaskLinkLaneApi returns the lane only when version and both functions exist
ok 3612 - getTaskLinkLaneApi returns the lane only when version and both functions exist
  ---
  duration_ms: 2.600044
  ...
# Subtest: isTaskLinkLaneLine passes content, line, and path and never throws
ok 3613 - isTaskLinkLaneLine passes content, line, and path and never throws
  ---
  duration_ms: 2.982442
  ...
# Subtest: single Alt+] on a Task Link delegates with exactly { editor, view }
ok 3614 - single Alt+] on a Task Link delegates with exactly { editor, view }
  ---
  duration_ms: 1.371237
  ...
# Subtest: Alt+[ and Alt+] delegate identically; direction is ignored
ok 3615 - Alt+[ and Alt+] delegate identically; direction is ignored
  ---
  duration_ms: 0.520944
  ...
# Subtest: embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
ok 3616 - embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
  ---
  duration_ms: 0.350449
  ...
# Subtest: entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
ok 3617 - entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
  ---
  duration_ms: 5.339732
  ...
# Subtest: counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
ok 3618 - counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
  ---
  duration_ms: 1.358263
  ...
# Subtest: counted dispatch without an explicit repeat leaves the key alone
ok 3619 - counted dispatch without an explicit repeat leaves the key alone
  ---
  duration_ms: 0.373904
  ...
# Subtest: counted range starting elsewhere skips Task Link lines
ok 3620 - counted range starting elsewhere skips Task Link lines
  ---
  duration_ms: 3.325068
  ...
# Subtest: legacy fallback with no api keeps today's behavior
ok 3621 - legacy fallback with no api keeps today's behavior
  ---
  duration_ms: 1.173861
  ...
# Subtest: plain Task Link in an open Pomodoro closes the task root-only and strikes the link
ok 3622 - plain Task Link in an open Pomodoro closes the task root-only and strikes the link
  ---
  duration_ms: 29.005797
  ...
# Subtest: marked plain Task Link drops its marker when struck under Pomodoro ancestry
ok 3623 - marked plain Task Link drops its marker when struck under Pomodoro ancestry
  ---
  duration_ms: 2.837075
  ...
# Subtest: plain Pomodoro Task Link closes root-only while embedded closes recursively
ok 3624 - plain Pomodoro Task Link closes root-only while embedded closes recursively
  ---
  duration_ms: 1.872114
  ...
# Subtest: embedded Pomodoro Task Link still closes recursively and retires to struck form
ok 3625 - embedded Pomodoro Task Link still closes recursively and retires to struck form
  ---
  duration_ms: 4.567028
  ...
# Subtest: Ctrl+Enter toggles a struck plain Pomodoro link back to open
ok 3626 - Ctrl+Enter toggles a struck plain Pomodoro link back to open
  ---
  duration_ms: 3.883232
  ...
# Subtest: same-file plain Task Link closes and strikes the correct line
ok 3627 - same-file plain Task Link closes and strikes the correct line
  ---
  duration_ms: 3.978836
  ...
# Subtest: cursor selects which of several Task Links closes and strikes
ok 3628 - cursor selects which of several Task Links closes and strikes
  ---
  duration_ms: 3.448873
  ...
# Subtest: plain links to Blocked or non-task blocks still complete the Pomodoro
ok 3629 - plain links to Blocked or non-task blocks still complete the Pomodoro
  ---
  duration_ms: 10.136768
  ...
# Subtest: strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
ok 3630 - strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
  ---
  duration_ms: 1.568665
  ...
# Subtest: completeTaskAtCursor closes each open symbol through the Tasks command
ok 3631 - completeTaskAtCursor closes each open symbol through the Tasks command
  ---
  duration_ms: 3.526571
  ...
# Subtest: completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
ok 3632 - completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
  ---
  duration_ms: 0.596308
  ...
# Subtest: completeTaskAtCursor refuses closed, cancelled, and non-task lines
ok 3633 - completeTaskAtCursor refuses closed, cancelled, and non-task lines
  ---
  duration_ms: 0.637296
  ...
# Subtest: completeTaskAtCursor refuses a missing Tasks command with no write
ok 3634 - completeTaskAtCursor refuses a missing Tasks command with no write
  ---
  duration_ms: 0.405825
  ...
# Subtest: Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
ok 3635 - Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
  ---
  duration_ms: 0.797783
  ...
# Subtest: completeTaskAtCursor reports not-closed when Tasks does not write [x]
ok 3636 - completeTaskAtCursor reports not-closed when Tasks does not write [x]
  ---
  duration_ms: 0.3039
  ...
# Subtest: recovery api is frozen at version 2 and recovers without striking references
ok 3637 - recovery api is frozen at version 2 and recovers without striking references
  ---
  duration_ms: 4.782358
  ...
# Subtest: recovery api never throws and reports failures
ok 3638 - recovery api never throws and reports failures
  ---
  duration_ms: 0.668035
  ...
# Subtest: future-scheduled dependents stay Blocked on the planner, api, and close paths
ok 3639 - future-scheduled dependents stay Blocked on the planner, api, and close paths
  ---
  duration_ms: 21.719029
  ...
# Subtest: Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
ok 3640 - Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
  ---
  duration_ms: 5.179166
  ...
# Subtest: every printable non-space ASCII key resolves to a surround pair
ok 3641 - every printable non-space ASCII key resolves to a surround pair
  ---
  duration_ms: 5.034961
  ...
# Subtest: visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
ok 3642 - visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
  ---
  duration_ms: 0.726246
  ...
# Subtest: non-visible, combining, multi-character, and multi-code-unit values are rejected
ok 3643 - non-visible, combining, multi-character, and multi-code-unit values are rejected
  ---
  duration_ms: 0.23568
  ...
# Subtest: ys adds broad symmetric delimiters through pending keydown
ok 3644 - ys adds broad symmetric delimiters through pending keydown
  ---
  duration_ms: 1.730654
  ...
# Subtest: rejected keydown input never edits or leaks into a pending ys
ok 3645 - rejected keydown input never edits or leaks into a pending ys
  ---
  duration_ms: 0.545912
  ...
# Subtest: Escape cancels ys, cs, and ds pending state without editing
ok 3646 - Escape cancels ys, cs, and ds pending state without editing
  ---
  duration_ms: 0.384234
  ...
# Subtest: cs accepts broad target and replacement characters independently
ok 3647 - cs accepts broad target and replacement characters independently
  ---
  duration_ms: 1.427554
  ...
# Subtest: cs preserves structural alias and padding rules
ok 3648 - cs preserves structural alias and padding rules
  ---
  duration_ms: 0.768426
  ...
# Subtest: cs replaces repeated symmetric runs exactly once on each side
ok 3649 - cs replaces repeated symmetric runs exactly once on each side
  ---
  duration_ms: 0.605496
  ...
# Subtest: ds removes representative broad symmetric delimiters
ok 3650 - ds removes representative broad symmetric delimiters
  ---
  duration_ms: 0.824063
  ...
# Subtest: ds preserves structural alias and padding rules
ok 3651 - ds preserves structural alias and padding rules
  ---
  duration_ms: 2.382788
  ...
# Subtest: ds removes one pair from repeated runs, including the reported block link
ok 3652 - ds removes one pair from repeated runs, including the reported block link
  ---
  duration_ms: 1.722058
  ...
# Subtest: consecutive ds commands peel a triple symmetric surround
ok 3653 - consecutive ds commands peel a triple symmetric surround
  ---
  duration_ms: 0.35643
  ...
# Subtest: symmetric discovery uses deterministic sequential same-line run pairs
ok 3654 - symmetric discovery uses deterministic sequential same-line run pairs
  ---
  duration_ms: 0.336753
  ...
# Subtest: symmetric discovery includes every character in repeated boundaries
ok 3655 - symmetric discovery includes every character in repeated boundaries
  ---
  duration_ms: 0.419711
  ...
# Subtest: unpaired and unequal symmetric runs are safe no-ops
ok 3656 - unpaired and unequal symmetric runs are safe no-ops
  ---
  duration_ms: 0.469607
  ...
# Subtest: ordinary normal-mode keys remain untouched outside pending state
ok 3657 - ordinary normal-mode keys remain untouched outside pending state
  ---
  duration_ms: 0.342464
  ...
# Subtest: dot while a surround is pending is a literal delimiter, not repeat
ok 3658 - dot while a surround is pending is a literal delimiter, not repeat
  ---
  duration_ms: 0.511907
  ...
# Subtest: dot-repeat records and replays broad-character ys
ok 3659 - dot-repeat records and replays broad-character ys
  ---
  duration_ms: 0.430081
  ...
# Subtest: dot-repeat records and replays broad-character cs
ok 3660 - dot-repeat records and replays broad-character cs
  ---
  duration_ms: 0.385315
  ...
# Subtest: dot-repeat records and replays broad-character ds
ok 3661 - dot-repeat records and replays broad-character ds
  ---
  duration_ms: 0.301746
  ...
# Subtest: dot-repeat replays cs against repeated symmetric runs
ok 3662 - dot-repeat replays cs against repeated symmetric runs
  ---
  duration_ms: 0.336402
  ...
# Subtest: dot-repeat replays ds against repeated symmetric runs
ok 3663 - dot-repeat replays ds against repeated symmetric runs
  ---
  duration_ms: 0.295684
  ...
# Subtest: consecutive dot-repeats peel a triple symmetric surround
ok 3664 - consecutive dot-repeats peel a triple symmetric surround
  ---
  duration_ms: 0.342183
  ...
1..3664
# tests 3681
# suites 0
# pass 3681
# fail 0
# cancelled 0
# skipped 0
# todo 0
# duration_ms 8362.615163
succeeded  exit=0  duration=42982ms

