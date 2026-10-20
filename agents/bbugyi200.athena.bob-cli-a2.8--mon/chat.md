# Chat History - ace-run (bob-cli-a2.8--mon)

- **TIMESTAMP:** 2026-10-20 10:42:15 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-a2.8--mon

## Prompt

sase monitor start --command 'npm test && npm run validate && npm run docs:check && bob plugins sync --no-pull -p bob-ledger-tools --repo /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins' --reason 'Run bob-plugins test, validation, docs, and the authorized bob-ledger-tools deployment'

## Response

sase tool run 0dfa4b0742e2717ea7196841359ee52b

> bob-plugins@0.1.0 test
> node scripts/build-plugins.mjs --check && npm run docs:inventory:check && node --test scripts/test-project-tasks-snapshot.cjs scripts/test-bob-articles.cjs scripts/test-dependency-line-migration.cjs scripts/test-navigation-hotkeys-section-nav.cjs scripts/test-navigation-hotkeys-rename.cjs scripts/test-navigation-hotkeys-ref-pdf.cjs scripts/test-navigation-hotkeys-templater-trigger.cjs scripts/test-navigation-hotkeys-schedule-recovery.cjs scripts/test-navigation-hotkeys-schedule-properties.cjs scripts/test-navigation-hotkeys-schedule-writes.cjs scripts/test-navigation-hotkeys-runtime-schedule.cjs scripts/test-navigation-hotkeys-dependencies.cjs scripts/test-navigation-blocks-guards.cjs scripts/test-navigation-blocks-writers.cjs scripts/test-navigation-blocks-edit.cjs scripts/test-navigation-blocks-stage-view.cjs scripts/test-navigation-hotkeys-dependency-mirror.cjs scripts/test-navigation-hotkeys-task-move-plan.cjs scripts/test-navigation-hotkeys-priority-notice.cjs scripts/test-navigation-successor-picker.cjs scripts/test-navigation-image-zoom-viewer.cjs scripts/test-navigation-hotkeys-unblocked-notice.cjs scripts/test-navigation-project-blocking.cjs scripts/test-navigation-project-dependency-stage.cjs scripts/test-navigation-project-subprojects.cjs scripts/test-navigation-project-subtree-gestures.cjs scripts/test-navigation-hotkeys-priority-picker.cjs scripts/test-navigation-hotkeys-picker-lifecycle.cjs scripts/test-navigation-hotkeys-ref-picker-text.cjs scripts/test-navigation-hotkeys-pomodoro-move-pickers.cjs scripts/test-navigation-inbox-route.cjs scripts/test-navigation-inbox-route-card.cjs scripts/test-navigation-hotkeys-task-move.cjs scripts/test-navigation-open-notes-uri.cjs scripts/test-navigation-goto-task-uri.cjs scripts/test-navigation-hotkeys-open-task-jump.cjs scripts/test-navigation-hotkeys-vim-counts.cjs scripts/test-navigation-hotkeys-tab-pin.cjs scripts/test-navigation-hotkeys-schedule-log.cjs scripts/test-navigation-hotkeys-schedule-review.cjs scripts/test-navigation-hotkeys-deferred-pomodoro.cjs scripts/test-navigation-hotkeys-pomodoro-parse.cjs scripts/test-navigation-hotkeys-pomodoro-bullet-move.cjs scripts/test-navigation-hotkeys-pomodoro-split-rename.cjs scripts/test-navigation-hotkeys-pomodoro-reorder.cjs scripts/test-navigation-hotkeys-runtime-prune.cjs scripts/test-navigation-hotkeys-project-from-task.cjs scripts/test-navigation-hotkeys-project-reversal.cjs scripts/test-navigation-hotkeys-link-picker.cjs scripts/test-navigation-hotkeys-lane-toggle.cjs scripts/test-navigation-hotkeys-task-link-lane.cjs scripts/test-navigation-hotkeys-cancel-log.cjs scripts/test-navigation-hotkeys-cancel-task.cjs scripts/test-navigation-hotkeys-forward-promotion.cjs scripts/test-navigation-hotkeys-schedule-work-log.cjs scripts/test-navigation-hotkeys-task-move-history.cjs scripts/test-navigation-jump-history.cjs scripts/test-navigation-dependencies.cjs scripts/test-navigation-editor-line-diff.cjs scripts/test-navigation-roll-decay.cjs scripts/test-navigation-decay-planner.cjs scripts/test-navigation-task-card-model.cjs scripts/test-navigation-task-card-view.cjs scripts/test-navigation-task-card-schedule.cjs scripts/test-navigation-task-card-review.cjs scripts/test-navigation-decision-card.cjs scripts/test-navigation-decision-card-handlers.cjs scripts/test-navigation-refresh-modal.cjs scripts/test-navigation-freshness.cjs scripts/test-navigation-stamps.cjs scripts/test-navigation-keep-counting.cjs scripts/test-navigation-checklist.cjs scripts/test-navigation-review-advance.cjs scripts/test-navigation-review-advance-gestures.cjs scripts/test-navigation-checklist-ctrl-enter.cjs scripts/test-ledger-tools-navigation.cjs scripts/test-ledger-tools-plan-budget.cjs scripts/test-ledger-tools-ready-badge.cjs scripts/test-ledger-tools-note-ready.cjs scripts/test-ledger-tools-note-ready-views.cjs scripts/test-ledger-tools-dashboard-parity.cjs scripts/test-ledger-tools-work-badge-tone.cjs scripts/test-ledger-tools-dashboard-collections.cjs scripts/test-ledger-tools-today.cjs scripts/test-ledger-tools-freshness-placement.cjs scripts/test-ledger-tools-freshness-states.cjs scripts/test-ledger-tools-freshness-namespace.cjs scripts/test-ledger-tools-freshness-review-model.cjs scripts/test-ledger-tools-freshness-queue.cjs scripts/test-ledger-tools-freshness-tracking.cjs scripts/test-ledger-tools-freshness-footer.cjs scripts/test-ledger-tools-freshness-recurring.cjs scripts/test-ledger-tools-freshness-mark.cjs scripts/test-ledger-tools-freshness-mark-surfaces.cjs scripts/test-ledger-tools-priority-marks.cjs scripts/test-ledger-tools-task-tag-marks.cjs scripts/test-ledger-tools-today-marks.cjs scripts/test-ledger-tools-today-marks-reading.cjs scripts/test-ledger-tools-unblocked-glyph.cjs scripts/test-ledger-tools-progress-marks.cjs scripts/test-ledger-tools-date-marks.cjs scripts/test-ledger-tools-date-marks-tasks.cjs scripts/test-ledger-tools-freshness-keeps.cjs scripts/test-ledger-tools-freshness-unblocked.cjs scripts/test-ledger-tools-freshness-decision-card.cjs scripts/test-ledger-tools-dependency-chips.cjs scripts/test-ledger-tools-blocks-chips.cjs scripts/test-ledger-tools-snippets.cjs scripts/test-ledger-tools-vim-mappings.cjs scripts/test-task-status-cycler-dependencies.cjs scripts/test-task-status-cycler-blocks-guards.cjs scripts/test-task-status-cycler-ctrl-enter.cjs scripts/test-task-status-cycler-reference-lifecycle.cjs scripts/test-task-status-cycler-pomodoro-completion.cjs scripts/test-task-status-cycler-pomodoro-work-log.cjs scripts/test-task-status-cycler-pomodoro-reopen.cjs scripts/test-task-status-cycler-blocked-schedule.cjs scripts/test-task-status-cycler-demotion-picker.cjs scripts/test-task-status-cycler-promotion.cjs scripts/test-task-status-cycler-counted-toggle.cjs scripts/test-task-status-cycler-successors.cjs scripts/test-task-status-cycler-successor-wiring.cjs scripts/test-task-status-cycler-successor-polish.cjs scripts/test-task-status-cycler-successor-offers.cjs scripts/test-task-status-cycler-project-pull-in.cjs scripts/test-task-status-cycler-task-links-api.cjs scripts/test-task-status-cycler-task-link-lane.cjs scripts/test-task-status-cycler-freshness.cjs scripts/test-block-id-prompt-dependencies.cjs scripts/test-block-id-prompt-blocks-guards.cjs scripts/test-block-id-prompt-ref-picker-text.cjs scripts/test-block-id-prompt-markers.cjs scripts/test-block-id-prompt-pomodoro-context.cjs scripts/test-block-id-prompt-target-update.cjs scripts/test-block-id-prompt-pomodoro-insertion.cjs scripts/test-block-id-prompt-pomodoro-targets.cjs scripts/test-block-id-prompt-pomodoro-picker-view.cjs scripts/test-block-id-prompt-pomodoro-picker-runtime.cjs scripts/test-block-id-prompt-work-log.cjs scripts/test-block-id-prompt-pomodoro-link-runtime.cjs scripts/test-block-id-prompt-pomodoro-link-picker-api.cjs scripts/test-block-id-prompt-pomodoro-unlink-runtime.cjs scripts/test-block-id-prompt-task-link-deletion.cjs scripts/test-block-id-prompt-plan-budget-and-freshness.cjs scripts/test-prompt-block-id-naming.cjs scripts/test-block-id-prompt-prefill.cjs scripts/test-vim-surround.cjs scripts/test-navigation-dependencies-stage-ranker-and-pool.cjs scripts/test-navigation-dependencies-stage-entry-and-view.cjs scripts/test-navigation-dependencies-stage-writes.cjs scripts/test-navigation-dependencies-stage-mirror-and-badge.cjs scripts/test-navigation-dependencies-stage-stale-guards.cjs scripts/test-navigation-dependencies-stage-performance.cjs scripts/test-navigation-prompt-block-id-stage.cjs scripts/test-navigation-dependencies-writer.cjs scripts/test-navigation-dependency-link-consumption.cjs scripts/test-plugin-build.cjs scripts/test-ledger-tools-stats-journal.cjs scripts/test-ledger-tools-stats-data.cjs scripts/test-ledger-tools-stats-block.cjs scripts/test-ledger-tools-stats-charts.cjs scripts/test-navigation-review-journal.cjs scripts/test-ledger-tools-stats-panels.cjs scripts/test-ledger-tools-reading-board-data.cjs scripts/test-ledger-tools-reading-board-models.cjs scripts/test-ledger-tools-reading-board-block.cjs scripts/test-ledger-tools-pomodoro-home-chips.cjs scripts/test-navigation-image-zoom-target.cjs scripts/test-navigation-image-zoom-command.cjs scripts/test-docs-inventory.mjs scripts/test-docs-check.mjs scripts/test-navigation-relation-lines.cjs scripts/test-ledger-tools-relations.cjs scripts/test-ledger-tools-relation-index.cjs scripts/test-task-status-cycler-relations.cjs scripts/test-block-id-prompt-relations.cjs

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
  duration_ms: 1.088479
  ...
# Subtest: bip BK13–BK15 malformed split mirrors the Depends-On twin
ok 2 - bip BK13–BK15 malformed split mirrors the Depends-On twin
  ---
  duration_ms: 0.358094
  ...
# Subtest: bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
ok 3 - bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
  ---
  duration_ms: 0.108487
  ...
# Subtest: bip MC1/MC2 Pomodoro scanners skip managed lines
ok 4 - bip MC1/MC2 Pomodoro scanners skip managed lines
  ---
  duration_ms: 1.059823
  ...
# Subtest: explicit task IDs exclusively own dependency lookup
ok 5 - explicit task IDs exclusively own dependency lookup
  ---
  duration_ms: 2.610866
  ...
# Subtest: legacy tasks without an id field still fall back to their block ID
ok 6 - legacy tasks without an id field still fall back to their block ID
  ---
  duration_ms: 0.307587
  ...
# Subtest: blocked-link consumption raises open prerequisites and leaves the dependent blocked
ok 7 - blocked-link consumption raises open prerequisites and leaves the dependent blocked
  ---
  duration_ms: 1.158042
  ...
# Subtest: project-blocked member consumption promotes the project's open prerequisite
ok 8 - project-blocked member consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.674187
  ...
# Subtest: project-blocked resident consumption promotes the project's open prerequisite
ok 9 - project-blocked resident consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.414762
  ...
# Subtest: a tagged inherited ^prj target is refused with its parent named
ok 10 - a tagged inherited ^prj target is refused with its parent named
  ---
  duration_ms: 0.368954
  ...
# Subtest: project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
ok 11 - project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
  ---
  duration_ms: 1.527978
  ...
# Subtest: project date refusal applies only when the date is the sole project reason
ok 12 - project date refusal applies only when the date is the sole project reason
  ---
  duration_ms: 0.248565
  ...
# Subtest: a project-blocked tag is token-bounded and ignored on lookalike tags
ok 13 - a project-blocked tag is token-bounded and ignored on lookalike tags
  ---
  duration_ms: 0.39248
  ...
# Subtest: task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
ok 14 - task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
  ---
  duration_ms: 0.636826
  ...
# Subtest: task blocked state unifies status and dependency reasons
ok 15 - task blocked state unifies status and dependency reasons
  ---
  duration_ms: 0.327185
  ...
# Subtest: task picker partition sinks blocked tasks while preserving group order
ok 16 - task picker partition sinks blocked tasks while preserving group order
  ---
  duration_ms: 0.180434
  ...
# Subtest: blocked chip labels show useful unmet dependency counts
ok 17 - blocked chip labels show useful unmet dependency counts
  ---
  duration_ms: 0.09413
  ...
# Subtest: blocked tooltips explain dependency and status-only reasons
ok 18 - blocked tooltips explain dependency and status-only reasons
  ---
  duration_ms: 0.206965
  ...
# Subtest: task status classes cover every open task status
ok 19 - task status classes cover every open task status
  ---
  duration_ms: 0.082357
  ...
# Subtest: Blocked tasks remain unmet dependency targets
ok 20 - Blocked tasks remain unmet dependency targets
  ---
  duration_ms: 0.122414
  ...
# Subtest: blocked task count covers both reasons without double-counting
ok 21 - blocked task count covers both reasons without double-counting
  ---
  duration_ms: 0.115551
  ...
# Subtest: single caret relocation preserves embedding and removes aliases
ok 22 - single caret relocation preserves embedding and removes aliases
  ---
  duration_ms: 1.545391
  ...
# Subtest: single caret relocation resets aliased block links
ok 23 - single caret relocation resets aliased block links
  ---
  duration_ms: 0.24073
  ...
# Subtest: single caret relocation strips heading and block subpaths
ok 24 - single caret relocation strips heading and block subpaths
  ---
  duration_ms: 0.248334
  ...
# Subtest: task picker normalizes every supported wiki block-link form
ok 25 - task picker normalizes every supported wiki block-link form
  ---
  duration_ms: 0.660882
  ...
# Subtest: three or more carets never trigger the task picker
ok 26 - three or more carets never trigger the task picker
  ---
  duration_ms: 0.145808
  ...
# Subtest: rapid aliased task picker completion preserves the alias
ok 27 - rapid aliased task picker completion preserves the alias
  ---
  duration_ms: 2.759479
  ...
# Subtest: task picker recognition is independent of Markdown source context
ok 28 - task picker recognition is independent of Markdown source context
  ---
  duration_ms: 0.90588
  ...
# Subtest: task picker recognition respects cursor proximity and fenced code
ok 29 - task picker recognition respects cursor proximity and fenced code
  ---
  duration_ms: 0.254406
  ...
# Subtest: plan budget suffix: link Notice appends the meter computed on post-write daily content
ok 30 - plan budget suffix: link Notice appends the meter computed on post-write daily content
  ---
  duration_ms: 7.019434
  ...
# Subtest: plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
ok 31 - plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
  ---
  duration_ms: 0.991553
  ...
# Subtest: plan budget suffix: unlink Notice marks an over-cap plan with 🔴
ok 32 - plan budget suffix: unlink Notice marks an over-cap plan with 🔴
  ---
  duration_ms: 2.868728
  ...
# Subtest: plan budget suffix: Next task without a block ID prompts for one and omits the meter
ok 33 - plan budget suffix: Next task without a block ID prompts for one and omits the meter
  ---
  duration_ms: 0.37162
  ...
# Subtest: plan budget suffix: Task Link Notice appends the meter from post-write daily content
ok 34 - plan budget suffix: Task Link Notice appends the meter from post-write daily content
  ---
  duration_ms: 2.06879
  ...
# Subtest: plan budget suffix: Task Link Notice omits the meter when no daily note takes part
ok 35 - plan budget suffix: Task Link Notice omits the meter when no daily note takes part
  ---
  duration_ms: 0.526505
  ...
# Subtest: planTargetTaskUpdate stamps the rewritten line last via injected stamper
ok 36 - planTargetTaskUpdate stamps the rewritten line last via injected stamper
  ---
  duration_ms: 0.260267
  ...
# Subtest: planTargetTaskUpdate without a stamper never stamps (identity default)
ok 37 - planTargetTaskUpdate without a stamper never stamps (identity default)
  ---
  duration_ms: 0.127153
  ...
# Subtest: planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
ok 38 - planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
  ---
  duration_ms: 0.339017
  ...
# Subtest: planTargetTaskUpdate stamps a Next task that gains a block ID
ok 39 - planTargetTaskUpdate stamps a Next task that gains a block ID
  ---
  duration_ms: 0.458456
  ...
# Subtest: planTargetTaskUpdate tolerates a throwing stamper
ok 40 - planTargetTaskUpdate tolerates a throwing stamper
  ---
  duration_ms: 0.208348
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 41 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.446102
  ...
# Subtest: dedicated-link helpers reject Depends-On lines
ok 42 - dedicated-link helpers reject Depends-On lines
  ---
  duration_ms: 0.316174
  ...
# Subtest: Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
ok 43 - Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
  ---
  duration_ms: 0.340501
  ...
# Subtest: malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
ok 44 - malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
  ---
  duration_ms: 0.106894
  ...
# Subtest: Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
ok 45 - Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
  ---
  duration_ms: 0.243686
  ...
# Subtest: Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
ok 46 - Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
  ---
  duration_ms: 0.193389
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent
ok 47 - readPlanBudgetMeter keeps per-cap over flags independent
  ---
  duration_ms: 0.18855
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent (mirror)
ok 48 - readPlanBudgetMeter keeps per-cap over flags independent (mirror)
  ---
  duration_ms: 0.092847
  ...
# Subtest: block-id-prompt freshness accessors degrade without ledger-tools
ok 49 - block-id-prompt freshness accessors degrade without ledger-tools
  ---
  duration_ms: 0.203378
  ...
# Subtest: list item body bounds trim whitespace and reject empty bullets
ok 50 - list item body bounds trim whitespace and reject empty bullets
  ---
  duration_ms: 1.336292
  ...
# Subtest: Pomodoro activation eligibility requires a sole-content sub-bullet
ok 51 - Pomodoro activation eligibility requires a sole-content sub-bullet
  ---
  duration_ms: 1.941537
  ...
# Subtest: Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
ok 52 - Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
  ---
  duration_ms: 0.2721
  ...
# Subtest: Pomodoro source context distinguishes ledger ancestry and open state
ok 53 - Pomodoro source context distinguishes ledger ancestry and open state
  ---
  duration_ms: 0.457313
  ...
# Subtest: future cleanup touches only later open Pomodoros and counts duplicates
ok 54 - future cleanup touches only later open Pomodoros and counts duplicates
  ---
  duration_ms: 2.218146
  ...
# Subtest: cleanup resolves aliases, embeds, same-note links, and alternate paths
ok 55 - cleanup resolves aliases, embeds, same-note links, and alternate paths
  ---
  duration_ms: 1.526184
  ...
# Subtest: dedicated bullet subtree cleanup preserves CRLF line endings
ok 56 - dedicated bullet subtree cleanup preserves CRLF line endings
  ---
  duration_ms: 0.356952
  ...
# Subtest: existing-ID task completion prunes future links in the source editor
ok 57 - existing-ID task completion prunes future links in the source editor
  ---
  duration_ms: 2.323397
  ...
# Subtest: new-ID same-file completion plans cleanup after the task edit
ok 58 - new-ID same-file completion plans cleanup after the task edit
  ---
  duration_ms: 1.316324
  ...
# Subtest: findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
ok 59 - findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
  ---
  duration_ms: 2.006151
  ...
# Subtest: findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
ok 60 - findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
  ---
  duration_ms: 0.170736
  ...
# Subtest: findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
ok 61 - findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
  ---
  duration_ms: 0.179042
  ...
# Subtest: todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
ok 62 - todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
  ---
  duration_ms: 1.345038
  ...
# Subtest: todayDailyPath honors a custom Daily Notes format and an empty folder
ok 63 - todayDailyPath honors a custom Daily Notes format and an empty folder
  ---
  duration_ms: 0.232053
  ...
# Subtest: formatDailyDate resolves bracketed literal text alongside date tokens
ok 64 - formatDailyDate resolves bracketed literal text alongside date tokens
  ---
  duration_ms: 0.116543
  ...
# Subtest: getDailyNotesOptions reads the daily-notes core plugin's configured options
ok 65 - getDailyNotesOptions reads the daily-notes core plugin's configured options
  ---
  duration_ms: 0.613442
  ...
# Subtest: computeFencedLineFlags marks opening and closing fence lines and everything between
ok 66 - computeFencedLineFlags marks opening and closing fence lines and everything between
  ---
  duration_ms: 0.24084
  ...
# Subtest: selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
ok 67 - selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
  ---
  duration_ms: 0.740283
  ...
# Subtest: selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
ok 68 - selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
  ---
  duration_ms: 0.442745
  ...
# Subtest: selectPomodoroInsertionTarget rejects more than one open timed entry
ok 69 - selectPomodoroInsertionTarget rejects more than one open timed entry
  ---
  duration_ms: 0.212506
  ...
# Subtest: selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
ok 70 - selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
  ---
  duration_ms: 0.19411
  ...
# Subtest: findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
ok 71 - findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
  ---
  duration_ms: 0.167921
  ...
# Subtest: planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
ok 72 - planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
  ---
  duration_ms: 1.122403
  ...
# Subtest: planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
ok 73 - planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
  ---
  duration_ms: 1.432436
  ...
# Subtest: planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
ok 74 - planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
  ---
  duration_ms: 0.206945
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
ok 75 - planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
  ---
  duration_ms: 0.515133
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
ok 76 - planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
  ---
  duration_ms: 0.490446
  ...
# Subtest: planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
ok 77 - planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
  ---
  duration_ms: 0.305733
  ...
# Subtest: planPomodoroLinkInsertion inserts before the separator preceding later content
ok 78 - planPomodoroLinkInsertion inserts before the separator preceding later content
  ---
  duration_ms: 0.234047
  ...
# Subtest: planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
ok 79 - planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
  ---
  duration_ms: 0.278021
  ...
# Subtest: planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
ok 80 - planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
  ---
  duration_ms: 0.332896
  ...
# Subtest: existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
ok 81 - existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
  ---
  duration_ms: 2.954642
  ...
# Subtest: same-note Pomodoro link runtime composes the task update with adjacent insertion
ok 82 - same-note Pomodoro link runtime composes the task update with adjacent insertion
  ---
  duration_ms: 1.129136
  ...
# Subtest: new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
ok 83 - new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
  ---
  duration_ms: 0.57084
  ...
# Subtest: planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
ok 84 - planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
  ---
  duration_ms: 0.288301
  ...
# Subtest: all-open cleanup removes current and future links while preserving history and unresolved links
ok 85 - all-open cleanup removes current and future links while preserving history and unresolved links
  ---
  duration_ms: 0.935897
  ...
# Subtest: all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
ok 86 - all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
  ---
  duration_ms: 1.087456
  ...
# Subtest: all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
ok 87 - all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
  ---
  duration_ms: 0.215021
  ...
# Subtest: all-open cleanup treats missing section, no open entries, and no matches as no-op successes
ok 88 - all-open cleanup treats missing section, no open entries, and no matches as no-op successes
  ---
  duration_ms: 0.177058
  ...
# Subtest: composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
ok 89 - composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
  ---
  duration_ms: 0.259756
  ...
# Subtest: pomodoro link picker choices normalize to existing/new or null
ok 90 - pomodoro link picker choices normalize to existing/new or null
  ---
  duration_ms: 1.147902
  ...
# Subtest: pomodoroLinkPicker api never rejects and validates choices
ok 91 - pomodoroLinkPicker api never rejects and validates choices
  ---
  duration_ms: 0.355789
  ...
# Subtest: destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
ok 92 - destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
  ---
  duration_ms: 0.698113
  ...
# Subtest: destination pick with a section releases its guards when the modal cannot open
ok 93 - destination pick with a section releases its guards when the modal cannot open
  ---
  duration_ms: 1.552004
  ...
# Subtest: plugin lifecycle installs the api and drops it on unload
ok 94 - plugin lifecycle installs the api and drops it on unload
  ---
  duration_ms: 0.294432
  ...
# Subtest: Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
ok 95 - Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
  ---
  duration_ms: 2.669578
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor requires a single cursor
ok 96 - resolvePomodoroLinkTaskFromEditor requires a single cursor
  ---
  duration_ms: 0.328958
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
ok 97 - resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
  ---
  duration_ms: 0.35652
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
ok 98 - resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
  ---
  duration_ms: 0.406557
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
ok 99 - resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
  ---
  duration_ms: 0.483253
  ...
# Subtest: blocked-link consumption reports dependency reasons before the project date
ok 100 - blocked-link consumption reports dependency reasons before the project date
  ---
  duration_ms: 2.468384
  ...
# Subtest: Pomodoro link checks do not read other notes for a non-Blocked task
ok 101 - Pomodoro link checks do not read other notes for a non-Blocked task
  ---
  duration_ms: 0.264495
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
ok 102 - resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
  ---
  duration_ms: 0.339287
  ...
# Subtest: task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
ok 103 - task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
  ---
  duration_ms: 5.799515
  ...
# Subtest: task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
ok 104 - task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
  ---
  duration_ms: 1.747477
  ...
# Subtest: task-mode toggle: linked only under a completed Pomodoro links again
ok 105 - task-mode toggle: linked only under a completed Pomodoro links again
  ---
  duration_ms: 0.779138
  ...
# Subtest: task-mode toggle: a task without a block ID is never linked and prompts for one
ok 106 - task-mode toggle: a task without a block ID is never linked and prompts for one
  ---
  duration_ms: 0.391157
  ...
# Subtest: existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
ok 107 - existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
  ---
  duration_ms: 1.050886
  ...
# Subtest: forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
ok 108 - forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
  ---
  duration_ms: 0.491518
  ...
# Subtest: new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
ok 109 - new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
  ---
  duration_ms: 0.495316
  ...
# Subtest: submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
ok 110 - submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
  ---
  duration_ms: 0.136902
  ...
# Subtest: submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
ok 111 - submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
  ---
  duration_ms: 0.18331
  ...
# Subtest: same-note Pomodoro link runtime: task and ledger edits merge into one transaction
ok 112 - same-note Pomodoro link runtime: task and ledger edits merge into one transaction
  ---
  duration_ms: 1.144946
  ...
# Subtest: linking an already-linked Ready task raises it to Next without duplicating the link
ok 113 - linking an already-linked Ready task raises it to Next without duplicating the link
  ---
  duration_ms: 0.512288
  ...
# Subtest: Next task without a block ID preflights the picker before prompting
ok 114 - Next task without a block ID preflights the picker before prompting
  ---
  duration_ms: 0.4559
  ...
# Subtest: Pomodoro link stops before any mutation when today's daily note is missing
ok 115 - Pomodoro link stops before any mutation when today's daily note is missing
  ---
  duration_ms: 0.165376
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
ok 116 - Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
  ---
  duration_ms: 0.430472
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
ok 117 - Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
  ---
  duration_ms: 0.269214
  ...
# Subtest: Pomodoro link aborts without any write when the task line changed since it was selected
ok 118 - Pomodoro link aborts without any write when the task line changed since it was selected
  ---
  duration_ms: 0.149105
  ...
# Subtest: Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
ok 119 - Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
  ---
  duration_ms: 0.585889
  ...
# Subtest: canceling the Pomodoro block-ID modal leaves the note untouched
ok 120 - canceling the Pomodoro block-ID modal leaves the note untouched
  ---
  duration_ms: 0.150387
  ...
# Subtest: review-walk: existing-ID link hands its Linked notice to continue with no separate notice
ok 121 - review-walk: existing-ID link hands its Linked notice to continue with no separate notice
  ---
  duration_ms: 0.825757
  ...
# Subtest: review-walk: prompted-ID link continues after submit
ok 122 - review-walk: prompted-ID link continues after submit
  ---
  duration_ms: 1.092276
  ...
# Subtest: review-walk: prompt cancel settles with null
ok 123 - review-walk: prompt cancel settles with null
  ---
  duration_ms: 0.164544
  ...
# Subtest: review-walk: BUSY swallows the key with no write
ok 124 - review-walk: BUSY swallows the key with no write
  ---
  duration_ms: 0.308209
  ...
# Subtest: review-walk: failed link keeps its notice and settles with null
ok 125 - review-walk: failed link keeps its notice and settles with null
  ---
  duration_ms: 0.242613
  ...
# Subtest: review-walk: partial link keeps its notice and never continues with an outcome
ok 126 - review-walk: partial link keeps its notice and never continues with an outcome
  ---
  duration_ms: 0.724815
  ...
# Subtest: inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
ok 127 - inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
  ---
  duration_ms: 0.199992
  ...
# Subtest: inbox-route: non-inbox notes and task-link mode never prompt
ok 128 - inbox-route: non-inbox notes and task-link mode never prompt
  ---
  duration_ms: 0.63337
  ...
# Subtest: inbox-route: cancel writes nothing and settles once
ok 129 - inbox-route: cancel writes nothing and settles once
  ---
  duration_ms: 0.457584
  ...
# Subtest: inbox-route: stay matches today
ok 130 - inbox-route: stay matches today
  ---
  duration_ms: 1.391978
  ...
# Subtest: inbox-route: move links, then moves, with one composed toast and a route continue
ok 131 - inbox-route: move links, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.655091
  ...
# Subtest: inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
ok 132 - inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
  ---
  duration_ms: 0.724764
  ...
# Subtest: inbox-route: a move failure gives the partial notice plus a link-today continue
ok 133 - inbox-route: a move failure gives the partial notice plus a link-today continue
  ---
  duration_ms: 0.506006
  ...
# Subtest: review-walk: no nav or nav v2 keeps today's notices
ok 134 - review-walk: no nav or nav v2 keeps today's notices
  ---
  duration_ms: 0.916771
  ...
# Subtest: inbox-route: source drift during route prompt refuses without writes
ok 135 - inbox-route: source drift during route prompt refuses without writes
  ---
  duration_ms: 0.321614
  ...
# Subtest: inbox-route: block-ID route cancel returns sentinel and settles null once
ok 136 - inbox-route: block-ID route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.318368
  ...
# Subtest: inbox-route: link no-op with move never commits
ok 137 - inbox-route: link no-op with move never commits
  ---
  duration_ms: 0.175785
  ...
# Subtest: picker opens only on the link direction, never on unlink
ok 138 - picker opens only on the link direction, never on unlink
  ---
  duration_ms: 9.158779
  ...
# Subtest: picker never opens in task-link mode
ok 139 - picker never opens in task-link mode
  ---
  duration_ms: 3.381878
  ...
# Subtest: Depends-On refusals never open the picker
ok 140 - Depends-On refusals never open the picker
  ---
  duration_ms: 0.897323
  ...
# Subtest: preflight refusals open nothing
ok 141 - preflight refusals open nothing
  ---
  duration_ms: 0.463956
  ...
# Subtest: picking a non-default entry links there
ok 142 - picking a non-default entry links there
  ---
  duration_ms: 1.166938
  ...
# Subtest: cancel writes nothing with no Notice and settles the walk null
ok 143 - cancel writes nothing with no Notice and settles the walk null
  ---
  duration_ms: 0.603112
  ...
# Subtest: a no-ID task gets picker, then the block-ID prompt with the target carried
ok 144 - a no-ID task gets picker, then the block-ID prompt with the target carried
  ---
  duration_ms: 0.80645
  ...
# Subtest: inbox order is picker, then route, then write
ok 145 - inbox order is picker, then route, then write
  ---
  duration_ms: 0.675039
  ...
# Subtest: a review-walk landing continues with link-today and the new text
ok 146 - a review-walk landing continues with link-today and the new text
  ---
  duration_ms: 0.889609
  ...
# Subtest: an all-closed ledger creates a new entry after the last completed block
ok 147 - an all-closed ledger creates a new entry after the last completed block
  ---
  duration_ms: 1.575068
  ...
# Subtest: several running entries allow an explicit pick
ok 148 - several running entries allow an explicit pick
  ---
  duration_ms: 0.675821
  ...
# Subtest: a target that changed before commit refuses with no writes
ok 149 - a target that changed before commit refuses with no writes
  ---
  duration_ms: 0.442845
  ...
# Subtest: a target that closed before commit refuses with no writes
ok 150 - a target that closed before commit refuses with no writes
  ---
  duration_ms: 0.347343
  ...
# Subtest: the task note being the daily note uses one editor transaction
ok 151 - the task note being the daily note uses one editor transaction
  ---
  duration_ms: 0.585257
  ...
# Subtest: promptOpen blocks re-entry while the picker is open
ok 152 - promptOpen blocks re-entry while the picker is open
  ---
  duration_ms: 12.543062
  ...
# Subtest: header shows title, subtitle, lane chip per status, and block-ID chip
ok 153 - header shows title, subtitle, lane chip per status, and block-ID chip
  ---
  duration_ms: 7.688932
  ...
# Subtest: rows render in document order with the default selected
ok 154 - rows render in document order with the default selected
  ---
  duration_ms: 0.950405
  ...
# Subtest: running row shows progress fraction and minutes-left meta
ok 155 - running row shows progress fraction and minutes-left meta
  ---
  duration_ms: 0.823903
  ...
# Subtest: unnamed entries render muted italic
ok 156 - unnamed entries render muted italic
  ---
  duration_ms: 0.409563
  ...
# Subtest: filtering ranks, highlights, and clearing restores the default
ok 157 - filtering ranks, highlights, and clearing restores the default
  ---
  duration_ms: 0.965344
  ...
# Subtest: create row meta, divider, and theme badge
ok 158 - create row meta, divider, and theme badge
  ---
  duration_ms: 1.469246
  ...
# Subtest: exact open names suppress the create row; prefix matches keep it
ok 159 - exact open names suppress the create row; prefix matches keep it
  ---
  duration_ms: 1.757887
  ...
# Subtest: theme badge turns red over cap; a throwing budget hides the detail
ok 160 - theme badge turns red over cap; a throwing budget hides the detail
  ---
  duration_ms: 0.8277
  ...
# Subtest: invalid rows explain the grammar and are inert on Enter
ok 161 - invalid rows explain the grammar and are inert on Enter
  ---
  duration_ms: 9.026496
  ...
# Subtest: multiple running entries show the banner, no pills, and block creation
ok 162 - multiple running entries show the banner, no pills, and block creation
  ---
  duration_ms: 1.268933
  ...
# Subtest: navigation wraps and skips non-selectable rows
ok 163 - navigation wraps and skips non-selectable rows
  ---
  duration_ms: 1.017182
  ...
# Subtest: empty state invites planning a Pomodoro
ok 164 - empty state invites planning a Pomodoro
  ---
  duration_ms: 0.257833
  ...
# Subtest: footer hints and plan meter
ok 165 - footer hints and plan meter
  ---
  duration_ms: 0.891662
  ...
# Subtest: Enter chooses the selected row; click chooses that row
ok 166 - Enter chooses the selected row; click chooses that row
  ---
  duration_ms: 0.557525
  ...
# Subtest: Shift+Enter creates; an exact open name links there instead
ok 167 - Shift+Enter creates; an exact open name links there instead
  ---
  duration_ms: 0.788777
  ...
# Subtest: Ctrl+Shift+Enter commits exactly like Enter
ok 168 - Ctrl+Shift+Enter commits exactly like Enter
  ---
  duration_ms: 1.433787
  ...
# Subtest: Escape and Ctrl+[ cancel with no choice; settle-once holds
ok 169 - Escape and Ctrl+[ cancel with no choice; settle-once holds
  ---
  duration_ms: 0.750282
  ...
# Subtest: canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
ok 170 - canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
  ---
  duration_ms: 1.648598
  ...
# Subtest: canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
ok 171 - canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
  ---
  duration_ms: 0.278512
  ...
# Subtest: pomodoroLinkSelectorSlug mirrors capture slugs
ok 172 - pomodoroLinkSelectorSlug mirrors capture slugs
  ---
  duration_ms: 0.241441
  ...
# Subtest: parsePomodoroEntryParts reads canonical and legacy entry lines
ok 173 - parsePomodoroEntryParts reads canonical and legacy entry lines
  ---
  duration_ms: 1.744982
  ...
# Subtest: collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
ok 174 - collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
  ---
  duration_ms: 1.511756
  ...
# Subtest: collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
ok 175 - collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
  ---
  duration_ms: 0.957379
  ...
# Subtest: collectPomodoroLinkEntries counts links but excludes struck references
ok 176 - collectPomodoroLinkEntries counts links but excludes struck references
  ---
  duration_ms: 0.456772
  ...
# Subtest: collectPomodoroLinkEntries falls back to range text and position titles
ok 177 - collectPomodoroLinkEntries falls back to range text and position titles
  ---
  duration_ms: 0.270336
  ...
# Subtest: pomodoroRunProgress reports fractions, overtime, and midnight wrap
ok 178 - pomodoroRunProgress reports fractions, overtime, and midnight wrap
  ---
  duration_ms: 0.626687
  ...
# Subtest: buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
ok 179 - buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
  ---
  duration_ms: 1.007213
  ...
# Subtest: buildPomodoroLinkPickerRows keeps the create row for prefix matches
ok 180 - buildPomodoroLinkPickerRows keeps the create row for prefix matches
  ---
  duration_ms: 0.305082
  ...
# Subtest: buildPomodoroLinkPickerRows marks completed-only names as again
ok 181 - buildPomodoroLinkPickerRows marks completed-only names as again
  ---
  duration_ms: 0.195834
  ...
# Subtest: buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
ok 182 - buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
  ---
  duration_ms: 0.427226
  ...
# Subtest: buildPomodoroLinkPickerRows matches times, positions, and block IDs
ok 183 - buildPomodoroLinkPickerRows matches times, positions, and block IDs
  ---
  duration_ms: 0.478744
  ...
# Subtest: resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
ok 184 - resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
  ---
  duration_ms: 0.316744
  ...
# Subtest: defaultPomodoroLinkChoice returns the default entry or null
ok 185 - defaultPomodoroLinkChoice returns the default entry or null
  ---
  duration_ms: 0.180725
  ...
# Subtest: planExplicitPomodoroLinkInsertion links under a chosen existing entry
ok 186 - planExplicitPomodoroLinkInsertion links under a chosen existing entry
  ---
  duration_ms: 0.964682
  ...
# Subtest: planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
ok 187 - planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
  ---
  duration_ms: 0.262331
  ...
# Subtest: planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
ok 188 - planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
  ---
  duration_ms: 1.118806
  ...
# Subtest: planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
ok 189 - planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
  ---
  duration_ms: 0.369927
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after the running entry
ok 190 - planExplicitPomodoroLinkInsertion creates after the running entry
  ---
  duration_ms: 0.598823
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
ok 191 - planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
  ---
  duration_ms: 0.704345
  ...
# Subtest: planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
ok 192 - planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
  ---
  duration_ms: 0.257572
  ...
# Subtest: planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
ok 193 - planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
  ---
  duration_ms: 0.28281
  ...
# Subtest: planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
ok 194 - planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
  ---
  duration_ms: 0.38203
  ...
# Subtest: buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
ok 195 - buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
  ---
  duration_ms: 0.189692
  ...
# Subtest: buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
ok 196 - buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
  ---
  duration_ms: 0.163322
  ...
# Subtest: planExplicitPomodoroLinkInsertion matches mixed-case raced open names
ok 197 - planExplicitPomodoroLinkInsertion matches mixed-case raced open names
  ---
  duration_ms: 0.194502
  ...
# Subtest: buildPomodoroLinkPickerRows bounds \#N position matches
ok 198 - buildPomodoroLinkPickerRows bounds \#N position matches
  ---
  duration_ms: 0.348725
  ...
# Subtest: planPomodoroLinkInsertion without a target keeps today's behavior and shape
ok 199 - planPomodoroLinkInsertion without a target keeps today's behavior and shape
  ---
  duration_ms: 0.427607
  ...
# Subtest: direct unlink without a daily note keeps the Next lane and reports it
ok 200 - direct unlink without a daily note keeps the Next lane and reports it
  ---
  duration_ms: 2.228224
  ...
# Subtest: In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
ok 201 - In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
  ---
  duration_ms: 0.430803
  ...
# Subtest: In Progress unlink with a summary keeps the lane and creates a Work Log
ok 202 - In Progress unlink with a summary keeps the lane and creates a Work Log
  ---
  duration_ms: 1.155386
  ...
# Subtest: In Progress unlink revalidates task text and block-ID uniqueness at confirmation
ok 203 - In Progress unlink revalidates task text and block-ID uniqueness at confirmation
  ---
  duration_ms: 0.904467
  ...
# Subtest: Next task unlink removes current and future links and keeps the Next lane
ok 204 - Next task unlink removes current and future links and keeps the Next lane
  ---
  duration_ms: 3.362792
  ...
# Subtest: In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
ok 205 - In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
  ---
  duration_ms: 0.7962
  ...
# Subtest: same-note Next unlink merges the Work Log and all-open cleanup in the active editor
ok 206 - same-note Next unlink merges the Work Log and all-open cleanup in the active editor
  ---
  duration_ms: 0.753108
  ...
# Subtest: same-note In Progress unlink merges cleanup and Work Log in the active editor
ok 207 - same-note In Progress unlink merges cleanup and Work Log in the active editor
  ---
  duration_ms: 0.517699
  ...
# Subtest: Next unlink stops before any write when daily cleanup write is stale
ok 208 - Next unlink stops before any write when daily cleanup write is stale
  ---
  duration_ms: 0.720215
  ...
# Subtest: Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
ok 209 - Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
  ---
  duration_ms: 0.872606
  ...
# Subtest: In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
ok 210 - In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
  ---
  duration_ms: 0.68084
  ...
# Subtest: review-walk: unlink settles with null and keeps its notice
ok 211 - review-walk: unlink settles with null and keeps its notice
  ---
  duration_ms: 1.144646
  ...
# Subtest: inbox-route: unlink cancel writes nothing
ok 212 - inbox-route: unlink cancel writes nothing
  ---
  duration_ms: 0.310463
  ...
# Subtest: inbox-route: unlink stay matches today and never commits
ok 213 - inbox-route: unlink stay matches today and never commits
  ---
  duration_ms: 0.509984
  ...
# Subtest: inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
ok 214 - inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.539751
  ...
# Subtest: inbox-route: In Progress unlink with a Work summary routes
ok 215 - inbox-route: In Progress unlink with a Work summary routes
  ---
  duration_ms: 0.543858
  ...
# Subtest: inbox-route: unlink move failure gives the partial notice and stays
ok 216 - inbox-route: unlink move failure gives the partial notice and stays
  ---
  duration_ms: 0.264175
  ...
# Subtest: inbox-route: non-inbox unlink never prompts
ok 217 - inbox-route: non-inbox unlink never prompts
  ---
  duration_ms: 0.293972
  ...
# Subtest: review-walk: Work-summary unlink path retains origin until submit
ok 218 - review-walk: Work-summary unlink path retains origin until submit
  ---
  duration_ms: 0.280706
  ...
# Subtest: inbox-route: unlink source drift during route prompt refuses without writes
ok 219 - inbox-route: unlink source drift during route prompt refuses without writes
  ---
  duration_ms: 0.223557
  ...
# Subtest: inbox-route: Work-summary route cancel returns sentinel and settles null once
ok 220 - inbox-route: Work-summary route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.238555
  ...
# Subtest: inbox-route: unlink no-op with move never commits
ok 221 - inbox-route: unlink no-op with move never commits
  ---
  duration_ms: 0.199441
  ...
# Subtest: same-note unlink maps a task below removed entries through Work-summary inserts
ok 222 - same-note unlink maps a task below removed entries through Work-summary inserts
  ---
  duration_ms: 0.550551
  ...
# Subtest: direct-add seeds from the task headline, not non-task blocks
ok 223 - direct-add seeds from the task headline, not non-task blocks
  ---
  duration_ms: 2.930145
  ...
# Subtest: link-task-complete seeds from the target, prefers open buffers
ok 224 - link-task-complete seeds from the target, prefers open buffers
  ---
  duration_ms: 0.929164
  ...
# Subtest: link-task-complete reports stale and unreadable targets
ok 225 - link-task-complete reports stale and unreadable targets
  ---
  duration_ms: 0.30881
  ...
# Subtest: pomodoro link seeds after the choice from the cursor task
ok 226 - pomodoro link seeds after the choice from the cursor task
  ---
  duration_ms: 0.27736
  ...
# Subtest: marker rename suggests from the unique task, never hiding ambiguity
ok 227 - marker rename suggests from the unique task, never hiding ambiguity
  ---
  duration_ms: 0.545401
  ...
# Subtest: modal seeds the value, selects once, and never overwrites typing
ok 228 - modal seeds the value, selects once, and never overwrites typing
  ---
  duration_ms: 1.233706
  ...
# Subtest: modal disables Save while loading and survives close/reopen
ok 229 - modal disables Save while loading and survives close/reopen
  ---
  duration_ms: 2.005179
  ...
# Subtest: submit revalidates: occupied IDs and stale tasks fail editable
ok 230 - submit revalidates: occupied IDs and stale tasks fail editable
  ---
  duration_ms: 0.514092
  ...
# Subtest: cancelling writes no ID and explicit renames keep the current ID
ok 231 - cancelling writes no ID and explicit renames keep the current ID
  ---
  duration_ms: 0.642197
  ...
# Subtest: the task picker drops the paired \#ref and prefixes the book
ok 232 - the task picker drops the paired \#ref and prefixes the book
  ---
  duration_ms: 2.467742
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 233 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.32487
  ...
# Subtest: block-id-prompt LK1–LK19 recognises only relation line shapes
ok 234 - block-id-prompt LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 1.319871
  ...
# Subtest: block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
ok 235 - block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
  ---
  duration_ms: 0.983498
  ...
# Subtest: block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
ok 236 - block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
  ---
  duration_ms: 1.285475
  ...
# Subtest: calendar date parsing rejects malformed width and impossible dates
ok 237 - calendar date parsing rejects malformed width and impossible dates
  ---
  duration_ms: 1.723761
  ...
# Subtest: future scheduled field detection respects the yesterday/today/tomorrow boundary
ok 238 - future scheduled field detection respects the yesterday/today/tomorrow boundary
  ---
  duration_ms: 0.493682
  ...
# Subtest: scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
ok 239 - scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
  ---
  duration_ms: 0.218317
  ...
# Subtest: planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
ok 240 - planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
  ---
  duration_ms: 1.010941
  ...
# Subtest: planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
ok 241 - planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
  ---
  duration_ms: 0.194662
  ...
# Subtest: planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
ok 242 - planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
  ---
  duration_ms: 0.15232
  ...
# Subtest: planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
ok 243 - planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
  ---
  duration_ms: 0.146029
  ...
# Subtest: planTargetTaskUpdate leaves today and past schedules untouched
ok 244 - planTargetTaskUpdate leaves today and past schedules untouched
  ---
  duration_ms: 0.281818
  ...
# Subtest: planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
ok 245 - planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
  ---
  duration_ms: 0.347964
  ...
# Subtest: two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
ok 246 - two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
  ---
  duration_ms: 0.459457
  ...
# Subtest: a malformed single scheduled field is never treated as future
ok 247 - a malformed single scheduled field is never treated as future
  ---
  duration_ms: 0.194711
  ...
# Subtest: an ambiguous scheduled field does not block the legacy Ready promotion
ok 248 - an ambiguous scheduled field does not block the legacy Ready promotion
  ---
  duration_ms: 0.190394
  ...
# Subtest: planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
ok 249 - planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
  ---
  duration_ms: 0.141189
  ...
# Subtest: Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
ok 250 - Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
  ---
  duration_ms: 0.50824
  ...
# Subtest: Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
ok 251 - Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
  ---
  duration_ms: 0.159524
  ...
# Subtest: planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
ok 252 - planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
  ---
  duration_ms: 0.328697
  ...
# Subtest: planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
ok 253 - planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
  ---
  duration_ms: 0.130609
  ...
# Subtest: planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
ok 254 - planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.128015
  ...
# Subtest: planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
ok 255 - planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
  ---
  duration_ms: 0.130109
  ...
# Subtest: planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
ok 256 - planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
  ---
  duration_ms: 0.134207
  ...
# Subtest: planTargetTaskUpdate preserves a trailing newline when one was already present
ok 257 - planTargetTaskUpdate preserves a trailing newline when one was already present
  ---
  duration_ms: 0.125801
  ...
# Subtest: planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
ok 258 - planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
  ---
  duration_ms: 0.099069
  ...
# Subtest: planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
ok 259 - planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
  ---
  duration_ms: 0.200913
  ...
# Subtest: planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
ok 260 - planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
  ---
  duration_ms: 0.117795
  ...
# Subtest: existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
ok 261 - existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
  ---
  duration_ms: 3.360507
  ...
# Subtest: new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
ok 262 - new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
  ---
  duration_ms: 0.831428
  ...
# Subtest: activation runtime aborts without any write when the target preimage goes stale
ok 263 - activation runtime aborts without any write when the target preimage goes stale
  ---
  duration_ms: 0.459677
  ...
# Subtest: same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
ok 264 - same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
  ---
  duration_ms: 2.532877
  ...
# Subtest: same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
ok 265 - same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
  ---
  duration_ms: 0.71731
  ...
# Subtest: a source marker edited after a successful existing-ID target write reports an accurate partial notice
ok 266 - a source marker edited after a successful existing-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.529
  ...
# Subtest: a source marker edited after a successful new-ID target write reports an accurate partial notice
ok 267 - a source marker edited after a successful new-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.526375
  ...
# Subtest: planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
ok 268 - planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
  ---
  duration_ms: 0.170866
  ...
# Subtest: planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
ok 269 - planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
  ---
  duration_ms: 0.113396
  ...
# Subtest: planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
ok 270 - planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
  ---
  duration_ms: 0.133394
  ...
# Subtest: planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
ok 271 - planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.114399
  ...
# Subtest: direct Task Links raise ^prj while never pulling its date forward
ok 272 - direct Task Links raise ^prj while never pulling its date forward
  ---
  duration_ms: 0.130669
  ...
# Subtest: task-link selection: one link is selectable from any column, several are chosen by cursor
ok 273 - task-link selection: one link is selectable from any column, several are chosen by cursor
  ---
  duration_ms: 3.562053
  ...
# Subtest: task-link selection ignores picker/rename markers, plain links, and Markdown-style links
ok 274 - task-link selection ignores picker/rename markers, plain links, and Markdown-style links
  ---
  duration_ms: 0.310123
  ...
# Subtest: dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
ok 275 - dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
  ---
  duration_ms: 0.645012
  ...
# Subtest: inline Task Link deletion removes the token with its decoration and collapses whitespace
ok 276 - inline Task Link deletion removes the token with its decoration and collapses whitespace
  ---
  duration_ms: 0.660201
  ...
# Subtest: dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
ok 277 - dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
  ---
  duration_ms: 0.891854
  ...
# Subtest: mergeCoveringEdits keeps the covering edit and the earlier of identical edits
ok 278 - mergeCoveringEdits keeps the covering edit and the earlier of identical edits
  ---
  duration_ms: 0.196645
  ...
# Subtest: dependency transclusion detection needs an embedded sole-content child of a \#task line
ok 279 - dependency transclusion detection needs an embedded sole-content child of a \#task line
  ---
  duration_ms: 0.447504
  ...
# Subtest: Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
ok 280 - Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
  ---
  duration_ms: 4.800137
  ...
# Subtest: Task Link on a Next target works from an embedded aliased link outside any Pomodoro
ok 281 - Task Link on a Next target works from an embedded aliased link outside any Pomodoro
  ---
  duration_ms: 1.127212
  ...
# Subtest: same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
ok 282 - same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
  ---
  duration_ms: 1.117974
  ...
# Subtest: same-note Task Link deletion clamps the restored cursor to the shortened note
ok 283 - same-note Task Link deletion clamps the restored cursor to the shortened note
  ---
  duration_ms: 0.557756
  ...
# Subtest: a cleanup subtree that covers a nested selected link wins and links are not double counted
ok 284 - a cleanup subtree that covers a nested selected link wins and links are not double counted
  ---
  duration_ms: 0.778867
  ...
# Subtest: same-note Task Link in a closed entry deletes the closed entry it empties
ok 285 - same-note Task Link in a closed entry deletes the closed entry it empties
  ---
  duration_ms: 0.598693
  ...
# Subtest: Task Link in another day's note deletes the emptied entry there and in today's note
ok 286 - Task Link in another day's note deletes the emptied entry there and in today's note
  ---
  duration_ms: 0.555541
  ...
# Subtest: Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
ok 287 - Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
  ---
  duration_ms: 1.271058
  ...
# Subtest: Task Link on an In Progress target with a blank summary logs nothing
ok 288 - Task Link on an In Progress target with a blank summary logs nothing
  ---
  duration_ms: 0.750102
  ...
# Subtest: canceling the In Progress Task Link prompt leaves everything untouched
ok 289 - canceling the In Progress Task Link prompt leaves everything untouched
  ---
  duration_ms: 0.286527
  ...
# Subtest: canceling the In Progress unlink prompt in task mode leaves everything untouched
ok 290 - canceling the In Progress unlink prompt in task mode leaves everything untouched
  ---
  duration_ms: 0.523219
  ...
# Subtest: In Progress Task Link submit revalidates the link line and the target task
ok 291 - In Progress Task Link submit revalidates the link line and the target task
  ---
  duration_ms: 0.551944
  ...
# Subtest: Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
ok 292 - Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
  ---
  duration_ms: 0.602741
  ...
# Subtest: Task Link on a Done or Cancelled target is refused without edits
ok 293 - Task Link on a Done or Cancelled target is refused without edits
  ---
  duration_ms: 0.380216
  ...
# Subtest: Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
ok 294 - Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
  ---
  duration_ms: 0.593774
  ...
# Subtest: precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
ok 295 - precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
  ---
  duration_ms: 1.20473
  ...
# Subtest: Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
ok 296 - Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
  ---
  duration_ms: 0.331242
  ...
# Subtest: Task Link that is a sub-task dependency transclusion is refused without edits
ok 297 - Task Link that is a sub-task dependency transclusion is refused without edits
  ---
  duration_ms: 0.211914
  ...
# Subtest: Task Link partial failure after the daily write is retryable
ok 298 - Task Link partial failure after the daily write is retryable
  ---
  duration_ms: 0.969351
  ...
# Subtest: Task Link stops before any write when the target note changes after planning
ok 299 - Task Link stops before any write when the target note changes after planning
  ---
  duration_ms: 0.429861
  ...
# Subtest: Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
ok 300 - Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
  ---
  duration_ms: 0.391437
  ...
# Subtest: Task Link subtree deletion removes a nested target task without any status write
ok 301 - Task Link subtree deletion removes a nested target task without any status write
  ---
  duration_ms: 0.254777
  ...
# Subtest: whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
ok 302 - whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
  ---
  duration_ms: 0.601107
  ...
# Subtest: selected-link deletion maps a cursor inside a removed entry to its former start
ok 303 - selected-link deletion maps a cursor inside a removed entry to its former start
  ---
  duration_ms: 0.504884
  ...
# Subtest: work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
ok 304 - work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
  ---
  duration_ms: 1.482803
  ...
# Subtest: work log date helpers use local calendar components
ok 305 - work log date helpers use local calendar components
  ---
  duration_ms: 0.254677
  ...
# Subtest: planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
ok 306 - planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
  ---
  duration_ms: 0.657506
  ...
# Subtest: planWorkLogInsertion inherits an existing space-indented child prefix
ok 307 - planWorkLogInsertion inherits an existing space-indented child prefix
  ---
  duration_ms: 0.48714
  ...
# Subtest: planWorkLogInsertion inherits an existing tab-indented child prefix
ok 308 - planWorkLogInsertion inherits an existing tab-indented child prefix
  ---
  duration_ms: 0.234908
  ...
# Subtest: planWorkLogInsertion prepends newest-first entries into existing marker spellings
ok 309 - planWorkLogInsertion prepends newest-first entries into existing marker spellings
  ---
  duration_ms: 0.482682
  ...
# Subtest: planWorkLogInsertion ignores nested child-task markers and preserves CRLF
ok 310 - planWorkLogInsertion ignores nested child-task markers and preserves CRLF
  ---
  duration_ms: 0.389063
  ...
# Subtest: planWorkLogInsertion treats blank summaries as no-op structural edits
ok 311 - planWorkLogInsertion treats blank summaries as no-op structural edits
  ---
  duration_ms: 0.133755
  ...
# Subtest: the Open-reset planner is removed: unlink plans only a Work Log insertion
ok 312 - the Open-reset planner is removed: unlink plans only a Work Log insertion
  ---
  duration_ms: 0.342594
  ...
# Subtest: unlink Work Log plan keeps the In Progress checkbox and appends one entry
ok 313 - unlink Work Log plan keeps the In Progress checkbox and appends one entry
  ---
  duration_ms: 0.415303
  ...
# Subtest: article detection accepts scalar and list frontmatter values
ok 314 - article detection accepts scalar and list frontmatter values
  ---
  duration_ms: 1.331503
  ...
# Subtest: bob resolution prefers its setting, then known install paths, then PATH
ok 315 - bob resolution prefers its setting, then known install paths, then PATH
  ---
  duration_ms: 0.80621
  ...
# Subtest: plan decoder accepts v1 and rejects a foreign schema version
ok 316 - plan decoder accepts v1 and rejects a foreign schema version
  ---
  duration_ms: 0.27735
  ...
# Subtest: bob stdin spawn passes the article contract and vault environment
ok 317 - bob stdin spawn passes the article contract and vault environment
  ---
  duration_ms: 2.082167
  ...
# Subtest: bob plan stdout decodes UTF-8 split across chunks
ok 318 - bob plan stdout decodes UTF-8 split across chunks
  ---
  duration_ms: 0.758679
  ...
# Subtest: early bob exit on stdin reports EPIPE as a run failure
ok 319 - early bob exit on stdin reports EPIPE as a run failure
  ---
  duration_ms: 0.655652
  ...
# Subtest: line hunks become minimal cursor-preserving changes
ok 320 - line hunks become minimal cursor-preserving changes
  ---
  duration_ms: 0.578445
  ...
# Subtest: insert, multi-line replace, and deletion hunks reproduce the formatted note
ok 321 - insert, multi-line replace, and deletion hunks reproduce the formatted note
  ---
  duration_ms: 2.782795
  ...
# Subtest: notice shows bob's text and at most two warning findings
ok 322 - notice shows bob's text and at most two warning findings
  ---
  duration_ms: 0.383592
  ...
# Subtest: inbound changes apply only when their target line still matches the preimage
ok 323 - inbound changes apply only when their target line still matches the preimage
  ---
  duration_ms: 0.625214
  ...
# Subtest: undo guard blocks a reformat until a fresh input or delete event
ok 324 - undo guard blocks a reformat until a fresh input or delete event
  ---
  duration_ms: 0.369005
  ...
# Subtest: leave formatting observes the undo guard before saving or reading
ok 325 - leave formatting observes the undo guard before saving or reading
  ---
  duration_ms: 0.257552
  ...
# Subtest: Convert shows bob's refusal on every invocation
ok 326 - Convert shows bob's refusal on every invocation
  ---
  duration_ms: 0.259596
  ...
# Subtest: old bob's non-JSON article response gets one update notice per session
ok 327 - old bob's non-JSON article response gets one update notice per session
  ---
  duration_ms: 0.15164
  ...
# Subtest: format drops its response if the editor changed while bob was running
ok 328 - format drops its response if the editor changed while bob was running
  ---
  duration_ms: 0.281628
  ...
# Subtest: decoration ranges mark written section numbers from the outline
ok 329 - decoration ranges mark written section numbers from the outline
  ---
  duration_ms: 0.64419
  ...
# Subtest: a new outline rerenders each open Reading view once for that generation
ok 330 - a new outline rerenders each open Reading view once for that generation
  ---
  duration_ms: 0.304501
  ...
# Subtest: section at a given line uses the innermost outline range
ok 331 - section at a given line uses the innermost outline range
  ---
  duration_ms: 0.276057
  ...
# Subtest: stale-hint debounce and in-flight state machine
ok 332 - stale-hint debounce and in-flight state machine
  ---
  duration_ms: 0.270487
  ...
# Subtest: reading-view wrapping puts the leading number token in span.bob-secno
ok 333 - reading-view wrapping puts the leading number token in span.bob-secno
  ---
  duration_ms: 0.620154
  ...
# Subtest: applied plans remap outline lines onto the formatted buffer
ok 334 - applied plans remap outline lines onto the formatted buffer
  ---
  duration_ms: 0.129708
  ...
# Subtest: article styles scope the reading look under .bob-article
ok 335 - article styles scope the reading look under .bob-article
  ---
  duration_ms: 0.384054
  ...
# Subtest: look settings default to serif typeface and stale-number hints
ok 336 - look settings default to serif typeface and stale-number hints
  ---
  duration_ms: 0.099419
  ...
# Subtest: folds embed, struck, and plain legacy children into one canonical line
ok 337 - folds embed, struck, and plain legacy children into one canonical line
  ---
  duration_ms: 63.303364
  ...
# Subtest: legacy-label row links come first, then legacy children in order
ok 338 - legacy-label row links come first, then legacy children in order
  ---
  duration_ms: 1.722509
  ...
# Subtest: R2 adopts field-only open dependents; unadoptable ids stay warned
ok 339 - R2 adopts field-only open dependents; unadoptable ids stay warned
  ---
  duration_ms: 0.56055
  ...
# Subtest: closed dependents gain the line but keep the field untouched
ok 340 - closed dependents gain the line but keep the field untouched
  ---
  duration_ms: 0.904818
  ...
# Subtest: open dependents drop stale field ids and stamp targets missing [id::]
ok 341 - open dependents drop stale field ids and stamp targets missing [id::]
  ---
  duration_ms: 0.56037
  ...
# Subtest: unresolved links stay verbatim and keep field ids as breadcrumbs
ok 342 - unresolved links stay verbatim and keep field ids as breadcrumbs
  ---
  duration_ms: 0.491879
  ...
# Subtest: leaves \#^ref embeds, non-task parents, fences, and conflict children alone
ok 343 - leaves \#^ref embeds, non-task parents, fences, and conflict children alone
  ---
  duration_ms: 0.669228
  ...
# Subtest: malformed rows leave the whole dependent alone
ok 344 - malformed rows leave the whole dependent alone
  ---
  duration_ms: 0.488103
  ...
# Subtest: R9 deletes label-only rows and removes the open field
ok 345 - R9 deletes label-only rows and removes the open field
  ---
  duration_ms: 0.615506
  ...
# Subtest: cross-note links use the shortest unambiguous form
ok 346 - cross-note links use the shortest unambiguous form
  ---
  duration_ms: 0.620445
  ...
# Subtest: ambiguous basenames fall back to the full path
ok 347 - ambiguous basenames fall back to the full path
  ---
  duration_ms: 0.45037
  ...
# Subtest: duplicate ids are ambiguous and fatal for --write
ok 348 - duplicate ids are ambiguous and fatal for --write
  ---
  duration_ms: 0.215221
  ...
# Subtest: archive targets keep the done/ path and are never stamped
ok 349 - archive targets keep the done/ path and are never stamped
  ---
  duration_ms: 0.258844
  ...
# Subtest: self links stay on the line but are not projected
ok 350 - self links stay on the line but are not projected
  ---
  duration_ms: 0.291476
  ...
# Subtest: non-task targets stay on the line but are not projected
ok 351 - non-task targets stay on the line but are not projected
  ---
  duration_ms: 0.245569
  ...
# Subtest: preserves CRLF, missing final newline, and cancel-log position
ok 352 - preserves CRLF, missing final newline, and cancel-log position
  ---
  duration_ms: 0.34019
  ...
# Subtest: migration is idempotent
ok 353 - migration is idempotent
  ---
  duration_ms: 1.014086
  ...
# Subtest: parseArgs handles --vault, --write, --help, and rejects unknowns
ok 354 - parseArgs handles --vault, --write, --help, and rejects unknowns
  ---
  duration_ms: 0.590267
  ...
# Subtest: BOB_CLI_DIR wins over a sibling checkout and a cache
ok 355 - BOB_CLI_DIR wins over a sibling checkout and a cache
  ---
  duration_ms: 18.535257
  ...
# Subtest: sibling bob-cli is used when BOB_CLI_DIR is unset
ok 356 - sibling bob-cli is used when BOB_CLI_DIR is unset
  ---
  duration_ms: 13.75167
  ...
# Subtest: an invalid BOB_CLI_DIR does not fall through
ok 357 - an invalid BOB_CLI_DIR does not fall through
  ---
  duration_ms: 9.292615
  ...
# Subtest: cache clone is used when no user-owned checkout exists
ok 358 - cache clone is used when no user-owned checkout exists
  ---
  duration_ms: 20.357354
  ...
# Subtest: refreshing an existing cache keeps git chatter off stdout and forwards exact paths
ok 359 - refreshing an existing cache keeps git chatter off stdout and forwards exact paths
  ---
  duration_ms: 33.791018
  ...
# Subtest: a cache clone with a foreign origin fails before fetch or reset
ok 360 - a cache clone with a foreign origin fails before fetch or reset
  ---
  duration_ms: 15.766029
  ...
# Subtest: a justfile alone is rejected as an explicit bob-cli checkout
ok 361 - a justfile alone is rejected as an explicit bob-cli checkout
  ---
  duration_ms: 10.975539
  ...
# Subtest: just failures propagate
ok 362 - just failures propagate
  ---
  duration_ms: 13.214674
  ...
# Subtest: scans multiline, one-line, and guarded literal registrations
ok 363 - scans multiline, one-line, and guarded literal registrations
  ---
  duration_ms: 2.870672
  ...
# Subtest: scans an optional addCommand call
ok 364 - scans an optional addCommand call
  ---
  duration_ms: 0.26211
  ...
# Subtest: allows addCommand references only in a typeof guard
ok 365 - allows addCommand references only in a typeof guard
  ---
  duration_ms: 0.35086
  ...
# Subtest: rejects bind, call, and aliased addCommand references with source locations
ok 366 - rejects bind, call, and aliased addCommand references with source locations
  ---
  duration_ms: 0.54981
  ...
# Subtest: expands literal command data from a constant-array forEach across source files
ok 367 - expands literal command data from a constant-array forEach across source files
  ---
  duration_ms: 1.741706
  ...
# Subtest: balances nested callback syntax and ignores misleading comments, strings, templates, and regexes
ok 368 - balances nested callback syntax and ignores misleading comments, strings, templates, and regexes
  ---
  duration_ms: 0.541654
  ...
# Subtest: decodes escaped string metadata and literal default hotkeys
ok 369 - decodes escaped string metadata and literal default hotkeys
  ---
  duration_ms: 0.407578
  ...
# Subtest: returns no commands for a plugin without registrations
ok 370 - returns no commands for a plugin without registrations
  ---
  duration_ms: 0.190874
  ...
# Subtest: fails with source locations for dynamic metadata, hotkeys, and malformed tables
ok 371 - fails with source locations for dynamic metadata, hotkeys, and malformed tables
  ---
  duration_ms: 0.834193
  ...
# Subtest: fails duplicate command ids with both registration locations
ok 372 - fails duplicate command ids with both registration locations
  ---
  duration_ms: 0.557254
  ...
# Subtest: checks drift without writes, preserves prose, and generates deterministically
ok 373 - checks drift without writes, preserves prose, and generates deterministically
  ---
  duration_ms: 9.630881
  ...
# Subtest: code-span table cells preserve backslashes and use a safe backtick fence
ok 374 - code-span table cells preserve backslashes and use a safe backtick fence
  ---
  duration_ms: 1.777815
  ...
# Subtest: does not write any output when source validation fails
ok 375 - does not write any output when source validation fails
  ---
  duration_ms: 1.196525
  ...
# Subtest: BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
ok 376 - BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
  ---
  duration_ms: 2.996292
  ...
# Subtest: reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
ok 377 - reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
  ---
  duration_ms: 2.872745
  ...
# Subtest: stale, missing, canonical append, and frozen-owner models (BC8-BC10)
ok 378 - stale, missing, canonical append, and frozen-owner models (BC8-BC10)
  ---
  duration_ms: 0.623851
  ...
# Subtest: Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
ok 379 - Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
  ---
  duration_ms: 7.489171
  ...
# Subtest: budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
ok 380 - budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
  ---
  duration_ms: 1.469085
  ...
# Subtest: chip builder includes the 🔑 badge and has no edit controls
ok 381 - chip builder includes the 🔑 badge and has no edit controls
  ---
  duration_ms: 0.507309
  ...
# Subtest: RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
ok 382 - RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
  ---
  duration_ms: 1.563797
  ...
# Subtest: RBC2 hover × on a live chip calls removeDependent; notice is nav's
ok 383 - RBC2 hover × on a live chip calls removeDependent; notice is nav's
  ---
  duration_ms: 0.442014
  ...
# Subtest: RBC3 frozen, stale, and no api.blocks stay navigation-only
ok 384 - RBC3 frozen, stale, and no api.blocks stay navigation-only
  ---
  duration_ms: 0.917502
  ...
# Subtest: RBC4 Reading view matches Live Preview ＋ / ×
ok 385 - RBC4 Reading view matches Live Preview ＋ / ×
  ---
  duration_ms: 2.52976
  ...
# Subtest: collections namespace version is additive v1
ok 386 - collections namespace version is additive v1
  ---
  duration_ms: 0.844883
  ...
# Subtest: collection chip classes stay collection-specific through paint and refresh
ok 387 - collection chip classes stay collection-specific through paint and refresh
  ---
  duration_ms: 2.491839
  ...
# Subtest: projects: scalar resolved links count, lists never widen
ok 388 - projects: scalar resolved links count, lists never widen
  ---
  duration_ms: 0.281257
  ...
# Subtest: projects: templates, status, and containsAny edges
ok 389 - projects: templates, status, and containsAny edges
  ---
  duration_ms: 0.299412
  ...
# Subtest: references: exact prefix, md only, exact scalar status
ok 390 - references: exact prefix, md only, exact scalar status
  ---
  duration_ms: 0.244276
  ...
# Subtest: base contracts: accept current files, reject drift, tolerate presentation
ok 391 - base contracts: accept current files, reject drift, tolerate presentation
  ---
  duration_ms: 0.571641
  ...
# Subtest: entries: true zero vs unavailable with reason, failure isolation
ok 392 - entries: true zero vs unavailable with reason, failure isolation
  ---
  duration_ms: 0.215842
  ...
# Subtest: snapshot counts both collections once, true zero stays clickable
ok 393 - snapshot counts both collections once, true zero stays clickable
  ---
  duration_ms: 0.332414
  ...
# Subtest: snapshot never presents partial counts as final
ok 394 - snapshot never presents partial counts as final
  ---
  duration_ms: 0.354076
  ...
# Subtest: changed definitions fail closed per collection, never stale
ok 395 - changed definitions fail closed per collection, never stale
  ---
  duration_ms: 0.428699
  ...
# Subtest: renderChip links, labels, and cleans up per component
ok 396 - renderChip links, labels, and cleans up per component
  ---
  duration_ms: 0.52332
  ...
# Subtest: PENDING section excludes TODAY while the whole lane keeps it
ok 397 - PENDING section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 2.875311
  ...
# Subtest: NEXT section excludes TODAY while the whole lane keeps it
ok 398 - NEXT section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 0.373423
  ...
# Subtest: NEXT uses symbol *, not name matching
ok 399 - NEXT uses symbol *, not name matching
  ---
  duration_ms: 0.262942
  ...
# Subtest: READY badge and query agree on hide and path case variants
ok 400 - READY badge and query agree on hide and path case variants
  ---
  duration_ms: 0.529832
  ...
# Subtest: blocked uses the full list even outside the visible subset
ok 401 - blocked uses the full list even outside the visible subset
  ---
  duration_ms: 0.264415
  ...
# Subtest: duplicate block IDs, missing IDs, and reused objects stay per-row
ok 402 - duplicate block IDs, missing IDs, and reused objects stay per-row
  ---
  duration_ms: 0.225831
  ...
# Subtest: READY gating keeps exempt rows and drops NEW/ROTTEN
ok 403 - READY gating keeps exempt rows and drops NEW/ROTTEN
  ---
  duration_ms: 0.267702
  ...
# Subtest: throwing Today degrades to unavailable, never zero
ok 404 - throwing Today degrades to unavailable, never zero
  ---
  duration_ms: 6.710223
  ...
# Subtest: dashboard badges color the displayed section count and label whole-lane pressure
ok 405 - dashboard badges color the displayed section count and label whole-lane pressure
  ---
  duration_ms: 0.613572
  ...
# Subtest: dashboard section warning boundaries ignore TODAY-only whole-lane excess
ok 406 - dashboard section warning boundaries ignore TODAY-only whole-lane excess
  ---
  duration_ms: 0.736607
  ...
# Subtest: dashboard lane badge keeps unavailable data neutral
ok 407 - dashboard lane badge keeps unavailable data neutral
  ---
  duration_ms: 0.311144
  ...
# Subtest: dashboard lane paint and refresh keep color aligned with the visible section
ok 408 - dashboard lane paint and refresh keep color aligned with the visible section
  ---
  duration_ms: 2.704705
  ...
# Subtest: dashboard lane widgets refresh together and prune on unload
ok 409 - dashboard lane widgets refresh together and prune on unload
  ---
  duration_ms: 1.888186
  ...
# Subtest: daily paint matches dashboard section badges on screenshot fixtures
ok 410 - daily paint matches dashboard section badges on screenshot fixtures
  ---
  duration_ms: 18.090215
  ...
# Subtest: daily and dashboard membership agree for exclusions and custom IN_PROGRESS
ok 411 - daily and dashboard membership agree for exclusions and custom IN_PROGRESS
  ---
  duration_ms: 4.087376
  ...
# Subtest: daily paint refreshes with dashboard when Today, lane, and cap change
ok 412 - daily paint refreshes with dashboard when Today, lane, and cap change
  ---
  duration_ms: 7.270584
  ...
# Subtest: older daily notes follow today's dashboard lanes
ok 413 - older daily notes follow today's dashboard lanes
  ---
  duration_ms: 2.491969
  ...
# Subtest: daily lane anchors keep shared navigation and reject stale paints
ok 414 - daily lane anchors keep shared navigation and reject stale paints
  ---
  duration_ms: 2.440542
  ...
# Subtest: daily paint stays unavailable until Tasks and Today are ready
ok 415 - daily paint stays unavailable until Tasks and Today are ready
  ---
  duration_ms: 1.292339
  ...
# Subtest: work tones: dashboard lane models carry section tones
ok 416 - work tones: dashboard lane models carry section tones
  ---
  duration_ms: 0.156239
  ...
# Subtest: T1 scheduled full-mode row gets a Fri mark inside the span
ok 417 - T1 scheduled full-mode row gets a Fri mark inside the span
  ---
  duration_ms: 2.790919
  ...
# Subtest: T2 done row maps to a completion Oct 5 mark
ok 418 - T2 done row maps to a completion Oct 5 mark
  ---
  duration_ms: 0.4715
  ...
# Subtest: T3 short-mode created span is left untouched by JS
ok 419 - T3 short-mode created span is left untouched by JS
  ---
  duration_ms: 0.291417
  ...
# Subtest: T4 pending row decorates once data-task appears; exhausted rows stay native
ok 420 - T4 pending row decorates once data-task appears; exhausted rows stay native
  ---
  duration_ms: 0.975543
  ...
# Subtest: T5 a second pass adds nothing
ok 421 - T5 a second pass adds nothing
  ---
  duration_ms: 0.26135
  ...
# Subtest: T6 task-due and task-start spans are untouched
ok 422 - T6 task-due and task-start spans are untouched
  ---
  duration_ms: 0.233937
  ...
# Subtest: T7 an invalid date is untouched
ok 423 - T7 an invalid date is untouched
  ---
  duration_ms: 0.253754
  ...
# Subtest: T8 nothing is scheduled with marks off or for connected non-Tasks elements
ok 424 - T8 nothing is scheduled with marks off or for connected non-Tasks elements
  ---
  duration_ms: 0.243405
  ...
# Subtest: T9 a Tasks-host Fri mark relabels to tomorrow on rollover
ok 425 - T9 a Tasks-host Fri mark relabels to tomorrow on rollover
  ---
  duration_ms: 0.760181
  ...
# Subtest: renderDateMarksIn schedules one shared frame for every row
ok 426 - renderDateMarksIn schedules one shared frame for every row
  ---
  duration_ms: 0.912292
  ...
# Subtest: the Tasks pass never throws on hostile input
ok 427 - the Tasks pass never throws on hostile input
  ---
  duration_ms: 0.438697
  ...
# Subtest: T10 real-DOM NodeList children decorate via direct and queued passes
ok 428 - T10 real-DOM NodeList children decorate via direct and queued passes
  ---
  duration_ms: 0.568446
  ...
# Subtest: T11 toggling off before a queued frame runs writes nothing
ok 429 - T11 toggling off before a queued frame runs writes nothing
  ---
  duration_ms: 0.404332
  ...
# Subtest: T12 a pending-row retry followed by disabling writes nothing
ok 430 - T12 a pending-row retry followed by disabling writes nothing
  ---
  duration_ms: 0.29885
  ...
# Subtest: T13 unloading before a callback runs writes nothing
not ok 431 - T13 unloading before a callback runs writes nothing
  ---
  duration_ms: 0.425973
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-date-marks-tasks.cjs:759:1'
  failureType: 'testCodeFailure'
  error: "Cannot read properties of undefined (reading 'clear')"
  code: 'ERR_TEST_FAILURE'
  name: 'TypeError'
  stack: |-
    BobLedgerToolsPlugin.teardownRelationIndex (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/main.js:17098:33)
    BobLedgerToolsPlugin.onunload (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/main.js:16364:10)
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-date-marks-tasks.cjs:766:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
ok 432 - styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
  ---
  duration_ms: 0.615466
  ...
# Subtest: DATE_MARK_FIELDS lists the four dates with verbs
ok 433 - DATE_MARK_FIELDS lists the four dates with verbs
  ---
  duration_ms: 1.534691
  ...
# Subtest: DM1 created today: label, tooltip, fold, quiet field
ok 434 - DM1 created today: label, tooltip, fold, quiet field
  ---
  duration_ms: 1.323617
  ...
# Subtest: DM2 created yesterday without space after the colons
ok 435 - DM2 created yesterday without space after the colons
  ---
  duration_ms: 0.483514
  ...
# Subtest: DM3-DM6 scheduled tomorrow, weekday, and month/day labels
ok 436 - DM3-DM6 scheduled tomorrow, weekday, and month/day labels
  ---
  duration_ms: 0.296687
  ...
# Subtest: DM7 scheduled today reads with emphasis timing
ok 437 - DM7 scheduled today reads with emphasis timing
  ---
  duration_ms: 0.258153
  ...
# Subtest: DM8 past scheduled uses month/day, never a weekday
ok 438 - DM8 past scheduled uses month/day, never a weekday
  ---
  duration_ms: 0.150127
  ...
# Subtest: DM9 completion on a closed task keeps the timeline grammar
ok 439 - DM9 completion on a closed task keeps the timeline grammar
  ---
  duration_ms: 0.186396
  ...
# Subtest: DM10 cancelled across years appends the year
ok 440 - DM10 cancelled across years appends the year
  ---
  duration_ms: 0.141269
  ...
# Subtest: DM11 next-year date appends the year
ok 441 - DM11 next-year date appends the year
  ---
  duration_ms: 0.301045
  ...
# Subtest: DM12 the weekday rule wins across the year boundary
ok 442 - DM12 the weekday rule wins across the year boundary
  ---
  duration_ms: 0.375397
  ...
# Subtest: DM13 two marks in order with folds 1 and 2
ok 443 - DM13 two marks in order with folds 1 and 2
  ---
  duration_ms: 0.463295
  ...
# Subtest: DM14 created and scheduled ranges stay disjoint from the fresh mark
ok 444 - DM14 created and scheduled ranges stay disjoint from the fresh mark
  ---
  duration_ms: 0.292899
  ...
# Subtest: DM15-DM16 paren and padded brackets are canonical
ok 445 - DM15-DM16 paren and padded brackets are canonical
  ---
  duration_ms: 0.170406
  ...
# Subtest: DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
ok 446 - DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
  ---
  duration_ms: 0.312417
  ...
# Subtest: DM22 code still parses pure but decorates nothing (see Live Preview)
ok 447 - DM22 code still parses pure but decorates nothing (see Live Preview)
  ---
  duration_ms: 0.103738
  ...
# Subtest: DM23 rescheduled is untouched and never a duplicate
ok 448 - DM23 rescheduled is untouched and never a duplicate
  ---
  duration_ms: 0.139125
  ...
# Subtest: DN1-DN9 non-canonical fields get no mark
ok 449 - DN1-DN9 non-canonical fields get no mark
  ---
  duration_ms: 0.246621
  ...
# Subtest: dateMarkContentStart finds content on list, quoted, and plain lines
ok 450 - dateMarkContentStart finds content on list, quoted, and plain lines
  ---
  duration_ms: 0.111012
  ...
# Subtest: dateMarkRelativePhrase covers the exact-day phrases
ok 451 - dateMarkRelativePhrase covers the exact-day phrases
  ---
  duration_ms: 0.081004
  ...
# Subtest: dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
ok 452 - dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
  ---
  duration_ms: 0.284303
  ...
# Subtest: no model output contains a double colon
ok 453 - no model output contains a double colon
  ---
  duration_ms: 1.433657
  ...
# Subtest: a new day always changes the widget key
ok 454 - a new day always changes the widget key
  ---
  duration_ms: 0.14708
  ...
# Subtest: element structure and the decorative/inheritColor/rendered options
ok 455 - element structure and the decorative/inheritColor/rendered options
  ---
  duration_ms: 0.411075
  ...
# Subtest: Live Preview emits several decorations in ascending order
ok 456 - Live Preview emits several decorations in ascending order
  ---
  duration_ms: 1.055045
  ...
# Subtest: Live Preview reveals per field, never the whole line
ok 457 - Live Preview reveals per field, never the whole line
  ---
  duration_ms: 0.258674
  ...
# Subtest: Live Preview refuses source mode, code, and disabled marks
ok 458 - Live Preview refuses source mode, code, and disabled marks
  ---
  duration_ms: 0.428048
  ...
# Subtest: widget mousedown anchors at the field start for folds 0, 1, and 2
ok 459 - widget mousedown anchors at the field start for folds 0, 1, and 2
  ---
  duration_ms: 2.208097
  ...
# Subtest: DM24 a cursor in the folded run unfolds the mark (vim cw)
ok 460 - DM24 a cursor in the folded run unfolds the mark (vim cw)
  ---
  duration_ms: 0.274424
  ...
# Subtest: DM25 a cursor in Tasks double space unfolds only that field
ok 461 - DM25 a cursor in Tasks double space unfolds only that field
  ---
  duration_ms: 0.18306
  ...
# Subtest: a selection ending inside the run unfolds; ending at its start keeps the fold
ok 462 - a selection ending inside the run unfolds; ending at its start keeps the fold
  ---
  duration_ms: 0.189733
  ...
# Subtest: no emitted decoration ever hides a cursor, and reveal still means field overlap
ok 463 - no emitted decoration ever hides a cursor, and reveal still means field overlap
  ---
  duration_ms: 12.424405
  ...
# Subtest: dateMarkSelectionFold: reveal, unfold, fold, and garbage input
ok 464 - dateMarkSelectionFold: reveal, unfold, fold, and garbage input
  ---
  duration_ms: 0.318037
  ...
# Subtest: mousedown on an unfolded (fold-0) widget anchors at the field start
ok 465 - mousedown on an unfolded (fold-0) widget anchors at the field start
  ---
  duration_ms: 0.496788
  ...
# Subtest: rendered views split several fields in one node
ok 466 - rendered views split several fields in one node
  ---
  duration_ms: 2.027872
  ...
# Subtest: rendered views skip exclusions and duplicates
ok 467 - rendered views skip exclusions and duplicates
  ---
  duration_ms: 0.682994
  ...
# Subtest: RO1 rendered marks relabel in place across midnight
ok 468 - RO1 rendered marks relabel in place across midnight
  ---
  duration_ms: 0.670481
  ...
# Subtest: rollover dispatches once per day change and never touches widgets
ok 469 - rollover dispatches once per day change and never touches widgets
  ---
  duration_ms: 0.500486
  ...
# Subtest: api.dateMarks v1 is additive, sync, and never throwing
ok 470 - api.dateMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.699446
  ...
# Subtest: session toggle and onload wiring
ok 471 - session toggle and onload wiring
  ---
  duration_ms: 6.471127
  ...
# Subtest: styles.css contract: masks, tones, repair flag, resting
ok 472 - styles.css contract: masks, tones, repair flag, resting
  ---
  duration_ms: 1.045206
  ...
# Subtest: DP parse vectors
ok 473 - DP parse vectors
  ---
  duration_ms: 2.130368
  ...
# Subtest: DC chip model vectors
ok 474 - DC chip model vectors
  ---
  duration_ms: 1.621617
  ...
# Subtest: decoration builds one widget, reveals on cursor, skips code and ranges
ok 475 - decoration builds one widget, reveals on cursor, skips code and ranges
  ---
  duration_ms: 7.158219
  ...
# Subtest: decoration skips paragraphs, grandchildren, and Work Log lines
ok 476 - decoration skips paragraphs, grandchildren, and Work Log lines
  ---
  duration_ms: 0.741406
  ...
# Subtest: decoration renders chips on DP30 and still skips DP20
ok 477 - decoration renders chips on DP30 and still skips DP20
  ---
  duration_ms: 0.809446
  ...
# Subtest: ownership check reads O(depth) lines, not the whole note
ok 478 - ownership check reads O(depth) lines, not the whole note
  ---
  duration_ms: 3.081825
  ...
# Subtest: widget identity covers the line and the interactive flag
ok 479 - widget identity covers the line and the interactive flag
  ---
  duration_ms: 1.583705
  ...
# Subtest: element hides actions without nav api v1
ok 480 - element hides actions without nav api v1
  ---
  duration_ms: 0.722379
  ...
# Subtest: nav api feature detection gates actions
ok 481 - nav api feature detection gates actions
  ---
  duration_ms: 0.395115
  ...
# Subtest: reading view decorates only the Depends-On row, hides chrome, stays idempotent
ok 482 - reading view decorates only the Depends-On row, hides chrome, stays idempotent
  ---
  duration_ms: 3.119186
  ...
# Subtest: reading view collapses more than three Done targets to one chip
ok 483 - reading view collapses more than three Done targets to one chip
  ---
  duration_ms: 1.344187
  ...
# Subtest: DC chip model vectors by id: DC2, DC5, DC6, DC9
ok 484 - DC chip model vectors by id: DC2, DC5, DC6, DC9
  ---
  duration_ms: 0.287168
  ...
# Subtest: chip actions send the 0-based line index through nav api v1
ok 485 - chip actions send the 0-based line index through nav api v1
  ---
  duration_ms: 1.155135
  ...
# Subtest: chip hover passes the chip element and its row to the preview
ok 486 - chip hover passes the chip element and its row to the preview
  ---
  duration_ms: 0.248565
  ...
# Subtest: chip lookup index lives on the freshness memo
ok 487 - chip lookup index lives on the freshness memo
  ---
  duration_ms: 0.478103
  ...
# Subtest: reading view hides actions when the line cannot be derived
ok 488 - reading view hides actions when the line cannot be derived
  ---
  duration_ms: 10.737103
  ...
# Subtest: reading view actions carry the derived 0-based line
ok 489 - reading view actions carry the derived 0-based line
  ---
  duration_ms: 2.140477
  ...
# Subtest: reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
ok 490 - reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
  ---
  duration_ms: 0.516977
  ...
# Subtest: reading view renders chips on DP30 (owner is a task under a Work Log entry)
ok 491 - reading view renders chips on DP30 (owner is a task under a Work Log entry)
  ---
  duration_ms: 0.503251
  ...
# Subtest: reading view DP30 row actions send the owned Depends-On line
ok 492 - reading view DP30 row actions send the owned Depends-On line
  ---
  duration_ms: 2.105741
  ...
# Subtest: reading view second-row remove sends the second line when two tasks share a prerequisite
ok 493 - reading view second-row remove sends the second line when two tasks share a prerequisite
  ---
  duration_ms: 1.524251
  ...
# Subtest: chip lookup index builds once per freshness memo
ok 494 - chip lookup index builds once per freshness memo
  ---
  duration_ms: 0.403931
  ...
# Subtest: decoration evaluates ownership without copying the note
ok 495 - decoration evaluates ownership without copying the note
  ---
  duration_ms: 0.458906
  ...
# Subtest: toggle flips the body class and onload wires chips
ok 496 - toggle flips the body class and onload wires chips
  ---
  duration_ms: 4.615075
  ...
# Subtest: capability: nav card v2 is capable
ok 497 - capability: nav card v2 is capable
  ---
  duration_ms: 1.283832
  ...
# Subtest: capability: nav card v1 is not capable
ok 498 - capability: nav card v1 is not capable
  ---
  duration_ms: 0.245659
  ...
# Subtest: capability: absent nav, missing api, and old versions are not capable
ok 499 - capability: absent nav, missing api, and old versions are not capable
  ---
  duration_ms: 0.181616
  ...
# Subtest: capability: a throwing app never throws
ok 500 - capability: a throwing app never throws
  ---
  duration_ms: 0.276559
  ...
# Subtest: leaf: active capable due choice replaces refresh with a leaf
ok 501 - leaf: active capable due choice replaces refresh with a leaf
  ---
  duration_ms: 3.8014
  ...
# Subtest: leaf: the same row without the card keeps refresh and counting words
ok 502 - leaf: the same row without the card keeps refresh and counting words
  ---
  duration_ms: 0.623821
  ...
# Subtest: leaf: early dates still leaf when capable
ok 503 - leaf: early dates still leaf when capable
  ---
  duration_ms: 0.569718
  ...
# Subtest: leaf: decay-off rows never leaf even when capable
ok 504 - leaf: decay-off rows never leaf even when capable
  ---
  duration_ms: 0.524
  ...
# Subtest: leaf: below-threshold rows never leaf
ok 505 - leaf: below-threshold rows never leaf
  ---
  duration_ms: 0.749512
  ...
# Subtest: leaf: threshold zero asks on every due re-confirmation when capable
ok 506 - leaf: threshold zero asks on every due re-confirmation when capable
  ---
  duration_ms: 0.68597
  ...
# Subtest: leaf: overflow renders capped dots with +N and the exact count in text
ok 507 - leaf: overflow renders capped dots with +N and the exact count in text
  ---
  duration_ms: 0.393732
  ...
# Subtest: leaf: out-of-scope and closed tasks show dots quietly, never a leaf
ok 508 - leaf: out-of-scope and closed tasks show dots quietly, never a leaf
  ---
  duration_ms: 0.964031
  ...
# Subtest: leaf: unresolved marks show dots quietly with counting-only wording
ok 509 - leaf: unresolved marks show dots quietly with counting-only wording
  ---
  duration_ms: 0.259095
  ...
# Subtest: element: leaf marks carry data-decide true and a leaf path
ok 510 - element: leaf marks carry data-decide true and a leaf path
  ---
  duration_ms: 0.889649
  ...
# Subtest: element: non-decision marks carry data-decide false
ok 511 - element: non-decision marks carry data-decide false
  ---
  duration_ms: 0.313799
  ...
# Subtest: footer groups omit every zero tier and keep walk order
ok 512 - footer groups omit every zero tier and keep walk order
  ---
  duration_ms: 1.676351
  ...
# Subtest: PRE and POST groups bracket the nine-tier queue and expose completion hints
ok 513 - PRE and POST groups bracket the nine-tier queue and expose completion hints
  ---
  duration_ms: 0.801851
  ...
# Subtest: a NEW-state project appears only in its walk tier
ok 514 - a NEW-state project appears only in its walk tier
  ---
  duration_ms: 0.20936
  ...
# Subtest: empty queue hides the footer even with upkeep or a met budget
ok 515 - empty queue hides the footer even with upkeep or a met budget
  ---
  duration_ms: 0.166368
  ...
# Subtest: unavailable or missing data never render false counts
ok 516 - unavailable or missing data never render false counts
  ---
  duration_ms: 0.139026
  ...
# Subtest: generic summary names due, commitments, and nonempty groups
ok 517 - generic summary names due, commitments, and nonempty groups
  ---
  duration_ms: 0.301696
  ...
# Subtest: current-task context uses shared ranks and compact wording
ok 518 - current-task context uses shared ranks and compact wording
  ---
  duration_ms: 0.844934
  ...
# Subtest: only ROTTEN remaining names commitments done or a met budget
ok 519 - only ROTTEN remaining names commitments done or a met budget
  ---
  duration_ms: 0.293671
  ...
# Subtest: NEW and commitments take precedence over a met budget
ok 520 - NEW and commitments take precedence over a met budget
  ---
  duration_ms: 0.355739
  ...
# Subtest: reviewEntryView compact and detail cover the original freshness tiers
ok 521 - reviewEntryView compact and detail cover the original freshness tiers
  ---
  duration_ms: 0.77516
  ...
# Subtest: cursor matching requires a unique verified identity
ok 522 - cursor matching requires a unique verified identity
  ---
  duration_ms: 0.417488
  ...
# Subtest: footer paint hides the host and keeps a stable button
ok 523 - footer paint hides the host and keeps a stable button
  ---
  duration_ms: 1.157851
  ...
# Subtest: status bar 0-1-0 transitions hide without a reload
ok 524 - status bar 0-1-0 transitions hide without a reload
  ---
  duration_ms: 9.369812
  ...
# Subtest: cursor-only updates reuse a warm memo
ok 525 - cursor-only updates reuse a warm memo
  ---
  duration_ms: 1.740654
  ...
# Subtest: unload disconnects the observer and click handler
ok 526 - unload disconnects the observer and click handler
  ---
  duration_ms: 1.90113
  ...
# Subtest: queue-built ranks agree with the footer current entry
ok 527 - queue-built ranks agree with the footer current entry
  ---
  duration_ms: 1.130468
  ...
# Subtest: footer short labels map every tier
ok 528 - footer short labels map every tier
  ---
  duration_ms: 0.163542
  ...
# Subtest: current-row footer context uses short labels while entry views keep full labels
ok 529 - current-row footer context uses short labels while entry views keep full labels
  ---
  duration_ms: 0.354757
  ...
# Subtest: legend line lists only current abbreviated tiers
ok 530 - legend line lists only current abbreviated tiers
  ---
  duration_ms: 0.384805
  ...
# Subtest: K1 absent: no keeps means 0 with no lints
ok 531 - K1 absent: no keeps means 0 with no lints
  ---
  duration_ms: 2.501997
  ...
# Subtest: K8 misplaced: keeps inside the Tasks suffix reads with a lint
ok 532 - K8 misplaced: keeps inside the Tasks suffix reads with a lint
  ---
  duration_ms: 0.431514
  ...
# Subtest: K9 duplicates and invalid values: first valid wins, else 0
ok 533 - K9 duplicates and invalid values: first valid wins, else 0
  ---
  duration_ms: 0.626576
  ...
# Subtest: K10 ceiling and NEW: 999 reads, never-confirmed reads 0
ok 534 - K10 ceiling and NEW: 999 reads, never-confirmed reads 0
  ---
  duration_ms: 0.200623
  ...
# Subtest: K13 exact keys: near-miss keys are not keeps; parens read
ok 535 - K13 exact keys: near-miss keys are not keeps; parens read
  ---
  duration_ms: 0.196556
  ...
# Subtest: keeps value parser accepts only decimal 1-999
ok 536 - keeps value parser accepts only decimal 1-999
  ---
  duration_ms: 0.176006
  ...
# Subtest: K2 first valid canonical: uncounted keep preserves and repairs
ok 537 - K2 first valid canonical: uncounted keep preserves and repairs
  ---
  duration_ms: 0.760042
  ...
# Subtest: K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
ok 538 - K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
  ---
  duration_ms: 0.501638
  ...
# Subtest: K4 same-day preserve noop: canonical kept line is byte-identical
ok 539 - K4 same-day preserve noop: canonical kept line is byte-identical
  ---
  duration_ms: 0.516697
  ...
# Subtest: K5 generic stamp clears, even same-day
ok 540 - K5 generic stamp clears, even same-day
  ---
  duration_ms: 0.459347
  ...
# Subtest: K6 set-refresh clears keeps
ok 541 - K6 set-refresh clears keeps
  ---
  duration_ms: 0.27255
  ...
# Subtest: K7 stale stamp clears keeps
ok 542 - K7 stale stamp clears keeps
  ---
  duration_ms: 0.179132
  ...
# Subtest: K8b misplaced keeps repaired to canonical order by a keep
ok 543 - K8b misplaced keeps repaired to canonical order by a keep
  ---
  duration_ms: 0.196095
  ...
# Subtest: K11 refusals preserve: closed and recurring lines never write
ok 544 - K11 refusals preserve: closed and recurring lines never write
  ---
  duration_ms: 0.203629
  ...
# Subtest: counted keep increments a stale streak once in the same write
ok 545 - counted keep increments a stale streak once in the same write
  ---
  duration_ms: 0.188039
  ...
# Subtest: first counted keep on a streakless due task writes keeps 1
ok 546 - first counted keep on a streakless due task writes keeps 1
  ---
  duration_ms: 0.160867
  ...
# Subtest: counted keep saturates at 999 and never wraps
ok 547 - counted keep saturates at 999 and never wraps
  ---
  duration_ms: 0.243224
  ...
# Subtest: counted keep needs a valid prior fresh before today
ok 548 - counted keep needs a valid prior fresh before today
  ---
  duration_ms: 0.326152
  ...
# Subtest: counted keep repairs malformed and duplicate placement
ok 549 - counted keep repairs malformed and duplicate placement
  ---
  duration_ms: 0.290545
  ...
# Subtest: uncounted keep preserves the valid value while canonicalizing
ok 550 - uncounted keep preserves the valid value while canonicalizing
  ---
  duration_ms: 0.237444
  ...
# Subtest: UB13 keep on an unblock TICKLER preserves the streak and skips the card
ok 551 - UB13 keep on an unblock TICKLER preserves the streak and skips the card
  ---
  duration_ms: 1.02612
  ...
# Subtest: a scheduled tickler still counts when schedule wins an unblock tie
ok 552 - a scheduled tickler still counts when schedule wins an unblock tie
  ---
  duration_ms: 0.328447
  ...
# Subtest: decay normalization: absent, null, true, and {} enable with 3
ok 553 - decay normalization: absent, null, true, and {} enable with 3
  ---
  duration_ms: 0.643439
  ...
# Subtest: decay false counts and displays but never asks
ok 554 - decay false counts and displays but never asks
  ---
  duration_ms: 0.12063
  ...
# Subtest: decay keeps 0 and fixed entry normalize
ok 555 - decay keeps 0 and fixed entry normalize
  ---
  duration_ms: 0.128004
  ...
# Subtest: invalid decay shapes fail the freshness config contract
ok 556 - invalid decay shapes fail the freshness config contract
  ---
  duration_ms: 0.226422
  ...
# Subtest: B: at-limit Ready due rows decide on every local day
ok 557 - B: at-limit Ready due rows decide on every local day
  ---
  duration_ms: 0.470027
  ...
# Subtest: D1 early date: an at-limit Ready due row decides
ok 558 - D1 early date: an at-limit Ready due row decides
  ---
  duration_ms: 0.109529
  ...
# Subtest: D2 at limit decides; D3 below limit stamps without a card
ok 559 - D2 at limit decides; D3 below limit stamps without a card
  ---
  duration_ms: 0.124538
  ...
# Subtest: D4 tickler counts as due; D5 NEW never decides
ok 560 - D4 tickler counts as due; D5 NEW never decides
  ---
  duration_ms: 0.189392
  ...
# Subtest: D6 zero limit asks on every due Ready re-confirmation
ok 561 - D6 zero limit asks on every due Ready re-confirmation
  ---
  duration_ms: 0.119628
  ...
# Subtest: D7 off never asks; D8 lane rows never decide
ok 562 - D7 off never asks; D8 lane rows never decide
  ---
  duration_ms: 0.080253
  ...
# Subtest: evaluator, queue, and counts carry keeps and decide
ok 563 - evaluator, queue, and counts carry keeps and decide
  ---
  duration_ms: 1.115731
  ...
# Subtest: no keeps: the existing mark is unchanged
ok 564 - no keeps: the existing mark is unchanged
  ---
  duration_ms: 0.885661
  ...
# Subtest: aging with two keeps: faint pips plus a counting-only line
ok 565 - aging with two keeps: faint pips plus a counting-only line
  ---
  duration_ms: 0.27721
  ...
# Subtest: confirmed today with two keeps: check glyph, faint dots
ok 566 - confirmed today with two keeps: check glyph, faint dots
  ---
  duration_ms: 0.212516
  ...
# Subtest: due below threshold: orange capsule keeps its glyph, adds dots
ok 567 - due below threshold: orange capsule keeps its glyph, adds dots
  ---
  duration_ms: 0.223587
  ...
# Subtest: resting marks show historical dots quietly and never decide
ok 568 - resting marks show historical dots quietly and never decide
  ---
  duration_ms: 0.326744
  ...
# Subtest: active decision due: data stays truthful, leaf stays gated
ok 569 - active decision due: data stays truthful, leaf stays gated
  ---
  duration_ms: 0.301486
  ...
# Subtest: dot caps follow the threshold with +N overflow
ok 570 - dot caps follow the threshold with +N overflow
  ---
  duration_ms: 0.712841
  ...
# Subtest: keeps tooltip wording: singulars, zero threshold, off state
ok 571 - keeps tooltip wording: singulars, zero threshold, off state
  ---
  duration_ms: 0.115711
  ...
# Subtest: noncanonical keeps never fold but keep their repair pill
ok 572 - noncanonical keeps never fold but keep their repair pill
  ---
  duration_ms: 0.333797
  ...
# Subtest: quoted lines fold; rendered fragments fold without task checks
ok 573 - quoted lines fold; rendered fragments fold without task checks
  ---
  duration_ms: 0.220131
  ...
# Subtest: unresolved marks show the line's own pips quietly and never decide
ok 574 - unresolved marks show the line's own pips quietly and never decide
  ---
  duration_ms: 0.208157
  ...
# Subtest: consensus sees count and decision eligibility: ambiguity stays neutral
ok 575 - consensus sees count and decision eligibility: ambiguity stays neutral
  ---
  duration_ms: 0.473104
  ...
# Subtest: pips render as one aria-hidden span with the count in the label
ok 576 - pips render as one aria-hidden span with the count in the label
  ---
  duration_ms: 1.017553
  ...
# Subtest: Live Preview decorates the folded range including space and refresh
ok 577 - Live Preview decorates the folded range including space and refresh
  ---
  duration_ms: 4.925996
  ...
# Subtest: Live Preview reveals the raw field when the cursor overlaps either edge
ok 578 - Live Preview reveals the raw field when the cursor overlaps either edge
  ---
  duration_ms: 1.249295
  ...
# Subtest: Live Preview skips codeblock and inline code spans
ok 579 - Live Preview skips codeblock and inline code spans
  ---
  duration_ms: 0.690989
  ...
# Subtest: source mode and marks-off yield no decorations
ok 580 - source mode and marks-off yield no decorations
  ---
  duration_ms: 0.173071
  ...
# Subtest: update rebuilds on the refresh effect and widget eq is stable
ok 581 - update rebuilds on the refresh effect and widget eq is stable
  ---
  duration_ms: 0.983458
  ...
# Subtest: widget click reveals the field at the folded offset
ok 582 - widget click reveals the field at the folded offset
  ---
  duration_ms: 0.73838
  ...
# Subtest: line resolver prefers exact, then consensus, then unresolved
ok 583 - line resolver prefers exact, then consensus, then unresolved
  ---
  duration_ms: 1.210501
  ...
# Subtest: decoration builds reuse the snapshot without touching the loader
ok 584 - decoration builds reuse the snapshot without touching the loader
  ---
  duration_ms: 0.426985
  ...
# Subtest: rendered views split text nodes and skip excluded ancestors
ok 585 - rendered views split text nodes and skip excluded ancestors
  ---
  duration_ms: 1.448256
  ...
# Subtest: rendered views stay idempotent
ok 586 - rendered views stay idempotent
  ---
  duration_ms: 0.580769
  ...
# Subtest: text resolver reaches consensus and degrades to neutral
ok 587 - text resolver reaches consensus and degrades to neutral
  ---
  duration_ms: 0.610115
  ...
# Subtest: session toggle flips the body class and notifies
ok 588 - session toggle flips the body class and notifies
  ---
  duration_ms: 0.813083
  ...
# Subtest: onload registers the toggle, extension, and post-processor
ok 589 - onload registers the toggle, extension, and post-processor
  ---
  duration_ms: 3.941907
  ...
# Subtest: M1 today: check glyph, today label, full ring
ok 590 - M1 today: check glyph, today label, full ring
  ---
  duration_ms: 3.635482
  ...
# Subtest: M2 aging: ring glyph, 3d label, draining lease
ok 591 - M2 aging: ring glyph, 3d label, draining lease
  ---
  duration_ms: 0.415333
  ...
# Subtest: M3 boundary: ROTTEN due capsule with Alt+F hint
ok 592 - M3 boundary: ROTTEN due capsule with Alt+F hint
  ---
  duration_ms: 0.364386
  ...
# Subtest: checklist marks replace stamp hints with their completion tier
ok 593 - checklist marks replace stamp hints with their completion tier
  ---
  duration_ms: 0.697242
  ...
# Subtest: M4 yesterday uses the yesterday relative
ok 594 - M4 yesterday uses the yesterday relative
  ---
  duration_ms: 0.266579
  ...
# Subtest: M5 folded refresh shows the /14d suffix
ok 595 - M5 folded refresh shows the /14d suffix
  ---
  duration_ms: 0.446222
  ...
# Subtest: M6 refresh today: today tone hides the interval suffix
ok 596 - M6 refresh today: today tone hides the interval suffix
  ---
  duration_ms: 0.307718
  ...
# Subtest: M7 note interval stays tooltip-only
ok 597 - M7 note interval stays tooltip-only
  ---
  duration_ms: 0.466981
  ...
# Subtest: M8 resurfaced: due tone on the scheduled return
ok 598 - M8 resurfaced: due tone on the scheduled return
  ---
  duration_ms: 0.487541
  ...
# Subtest: M9 due NEXT lane with keep/release/today keys
ok 599 - M9 due NEXT lane with keep/release/today keys
  ---
  duration_ms: 0.518369
  ...
# Subtest: M10 NEXT lane stamped today
ok 600 - M10 NEXT lane stamped today
  ---
  duration_ms: 0.297959
  ...
# Subtest: M19 disabled Next lane rests
ok 601 - M19 disabled Next lane rests
  ---
  duration_ms: 0.260979
  ...
# Subtest: M20 PENDING lane folds refresh without the suffix
ok 602 - M20 PENDING lane folds refresh without the suffix
  ---
  duration_ms: 0.246701
  ...
# Subtest: M11 closed: resting beats age 0
ok 603 - M11 closed: resting beats age 0
  ---
  duration_ms: 0.203489
  ...
# Subtest: M12 unresolved running and M13 unresolved lease over
ok 604 - M12 unresolved running and M13 unresolved lease over
  ---
  duration_ms: 0.218226
  ...
# Subtest: M14 linked today rests with its reason
ok 605 - M14 linked today rests with its reason
  ---
  duration_ms: 0.175114
  ...
# Subtest: M15 other year shows the year and the 282d age
ok 606 - M15 other year shows the year and the 282d age
  ---
  duration_ms: 0.143504
  ...
# Subtest: M16 quoted line keeps foldSpace
ok 607 - M16 quoted line keeps foldSpace
  ---
  duration_ms: 0.152442
  ...
# Subtest: M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
ok 608 - M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
  ---
  duration_ms: 0.379124
  ...
# Subtest: N1-N6 non-canonical lines get no mark
ok 609 - N1-N6 non-canonical lines get no mark
  ---
  duration_ms: 0.172991
  ...
# Subtest: C1-C3 consensus is exact or unresolved
ok 610 - C1-C3 consensus is exact or unresolved
  ---
  duration_ms: 0.544319
  ...
# Subtest: freshnessMarkResolution treats evaluator new as unresolved
ok 611 - freshnessMarkResolution treats evaluator new as unresolved
  ---
  duration_ms: 0.123826
  ...
# Subtest: freshnessMarkSourceInText covers rendered fragments
ok 612 - freshnessMarkSourceInText covers rendered fragments
  ---
  duration_ms: 0.197236
  ...
# Subtest: tone order: closed, then due, then age 0, then out of scope
ok 613 - tone order: closed, then due, then age 0, then out of scope
  ---
  duration_ms: 0.349518
  ...
# Subtest: no tooltip ever contains a double colon
ok 614 - no tooltip ever contains a double colon
  ---
  duration_ms: 0.651564
  ...
# Subtest: freshnessShortDate pins English names and the year rule
ok 615 - freshnessShortDate pins English names and the year rule
  ---
  duration_ms: 0.107214
  ...
# Subtest: DOM builder structure, attributes, and ring geometry
ok 616 - DOM builder structure, attributes, and ring geometry
  ---
  duration_ms: 2.235048
  ...
# Subtest: every mark helper is synchronous and never throws on bad input
ok 617 - every mark helper is synchronous and never throws on bad input
  ---
  duration_ms: 0.118316
  ...
# Subtest: freshness namespace v12 exposes unblock TICKLER metadata and writers
ok 618 - freshness namespace v12 exposes unblock TICKLER metadata and writers
  ---
  duration_ms: 11.12278
  ...
# Subtest: freshness state and count API expose an unblock return source
ok 619 - freshness state and count API expose an unblock return source
  ---
  duration_ms: 1.68099
  ...
# Subtest: checklist rows report tier and rank while keeping the READY bucket null
ok 620 - checklist rows report tier and rank while keeping the READY bucket null
  ---
  duration_ms: 1.271157
  ...
# Subtest: tier, isDue, and rank cover lane rows
ok 621 - tier, isDue, and rank cover lane rows
  ---
  duration_ms: 2.286146
  ...
# Subtest: memo invalidates on a new tasks array, rollover, and frontmatter
ok 622 - memo invalidates on a new tasks array, rollover, and frontmatter
  ---
  duration_ms: 2.210882
  ...
# Subtest: the reload event fires only when the due key set changes
ok 623 - the reload event fires only when the due key set changes
  ---
  duration_ms: 1.540252
  ...
# Subtest: status bar text covers every state, and a missing host stays quiet
ok 624 - status bar text covers every state, and a missing host stays quiet
  ---
  duration_ms: 1.468885
  ...
# Subtest: status bar clicks through, falling back to rotten
ok 625 - status bar clicks through, falling back to rotten
  ---
  duration_ms: 5.899866
  ...
# Subtest: every freshness api member is synchronous and never throws
ok 626 - every freshness api member is synchronous and never throws
  ---
  duration_ms: 3.66454
  ...
# Subtest: placement vectors P1-P11, P14-P16, P18 stamp canonically
ok 627 - placement vectors P1-P11, P14-P16, P18 stamp canonically
  ---
  duration_ms: 3.050014
  ...
# Subtest: P12 set and clear refresh stamps alongside
ok 628 - P12 set and clear refresh stamps alongside
  ---
  duration_ms: 0.279444
  ...
# Subtest: P13 recurring and P17 done tasks are refused unchanged
ok 629 - P13 recurring and P17 done tasks are refused unchanged
  ---
  duration_ms: 0.183871
  ...
# Subtest: U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
ok 630 - U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
  ---
  duration_ms: 0.736336
  ...
# Subtest: reader reports misplaced and duplicate fields
ok 631 - reader reports misplaced and duplicate fields
  ---
  duration_ms: 0.337785
  ...
# Subtest: Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
ok 632 - Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
  ---
  duration_ms: 3.65496
  ...
# Subtest: Q2 tier order beats path order
ok 633 - Q2 tier order beats path order
  ---
  duration_ms: 0.976875
  ...
# Subtest: L1 lane due and stamped today
ok 634 - L1 lane due and stamped today
  ---
  duration_ms: 0.344077
  ...
# Subtest: L2 lane overrides refresh
ok 635 - L2 lane overrides refresh
  ---
  duration_ms: 0.226733
  ...
# Subtest: L3 lane exclusions have no tier
ok 636 - L3 lane exclusions have no tier
  ---
  duration_ms: 0.34538
  ...
# Subtest: L4 lane off switch and null default
ok 637 - L4 lane off switch and null default
  ---
  duration_ms: 0.245429
  ...
# Subtest: L5 lane order never stamped first
ok 638 - L5 lane order never stamped first
  ---
  duration_ms: 0.358725
  ...
# Subtest: R1 TICKLER beats older ROTTEN
ok 639 - R1 TICKLER beats older ROTTEN
  ---
  duration_ms: 0.285676
  ...
# Subtest: R2 tickler orders by due date then path and line
ok 640 - R2 tickler orders by due date then path and line
  ---
  duration_ms: 0.521746
  ...
# Subtest: missing created sorts after dated peers
ok 641 - missing created sorts after dated peers
  ---
  duration_ms: 0.667595
  ...
# Subtest: B1 upkeep counts outside the lanes
ok 642 - B1 upkeep counts outside the lanes
  ---
  duration_ms: 2.049714
  ...
# Subtest: review model meter uses upkeep and exposes refreshed
ok 643 - review model meter uses upkeep and exposes refreshed
  ---
  duration_ms: 0.267681
  ...
# Subtest: RC1 arrived: past scheduled walks RECURRING with lane and null state
ok 644 - RC1 arrived: past scheduled walks RECURRING with lane and null state
  ---
  duration_ms: 3.71249
  ...
# Subtest: RC2 arrives today: due today with zero days overdue
ok 645 - RC2 arrives today: due today with zero days overdue
  ---
  duration_ms: 0.378593
  ...
# Subtest: RC3 not yet: future scheduled walks nowhere
ok 646 - RC3 not yet: future scheduled walks nowhere
  ---
  duration_ms: 0.300194
  ...
# Subtest: RC4 due only, past: the due date is the occurrence
ok 647 - RC4 due only, past: the due date is the occurrence
  ---
  duration_ms: 0.302478
  ...
# Subtest: RC5 due only, future: walks nowhere
ok 648 - RC5 due only, future: walks nowhere
  ---
  duration_ms: 0.330792
  ...
# Subtest: RC6 earliest date wins across start and due
ok 649 - RC6 earliest date wins across start and due
  ---
  duration_ms: 0.359828
  ...
# Subtest: RC7 undated: no occurrence, no tier
ok 650 - RC7 undated: no occurrence, no tier
  ---
  duration_ms: 0.416144
  ...
# Subtest: RC8 lanes: recurring lane rows keep their lane with null state
ok 651 - RC8 lanes: recurring lane rows keep their lane with null state
  ---
  duration_ms: 0.637177
  ...
# Subtest: RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
ok 652 - RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
  ---
  duration_ms: 2.202836
  ...
# Subtest: RC10 checklist wins: a recurring chore stays in its checklist tier
ok 653 - RC10 checklist wins: a recurring chore stays in its checklist tier
  ---
  duration_ms: 0.577803
  ...
# Subtest: RC11 a stray stamp is ignored: recurring with null state
ok 654 - RC11 a stray stamp is ignored: recurring with null state
  ---
  duration_ms: 0.463334
  ...
# Subtest: RC12 order and counts: due_on, then path, then line; recurring adds no due
ok 655 - RC12 order and counts: due_on, then path, then line; recurring adds no due
  ---
  duration_ms: 1.561993
  ...
# Subtest: recurring rows adapt due and start from Tasks fields and inline fallbacks
ok 656 - recurring rows adapt due and start from Tasks fields and inline fallbacks
  ---
  duration_ms: 1.789677
  ...
# Subtest: status view counts RECURRING as a due commitment tier
ok 657 - status view counts RECURRING as a due commitment tier
  ---
  duration_ms: 0.464356
  ...
# Subtest: footer groups, entry view, and legend cover RECURRING
ok 658 - footer groups, entry view, and legend cover RECURRING
  ---
  duration_ms: 1.140027
  ...
# Subtest: a stale-stamped recurring row marks due with the resolve hint
ok 659 - a stale-stamped recurring row marks due with the resolve hint
  ---
  duration_ms: 1.311394
  ...
# Subtest: freshness namespace v12 keeps recurring and removes reference capabilities
ok 660 - freshness namespace v12 keeps recurring and removes reference capabilities
  ---
  duration_ms: 5.40409
  ...
# Subtest: hidden recurring ^ref keeps ordinary visibility (Rust parity)
ok 661 - hidden recurring ^ref keeps ordinary visibility (Rust parity)
  ---
  duration_ms: 1.241931
  ...
# Subtest: bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
ok 662 - bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
  ---
  duration_ms: 3.877764
  ...
# Subtest: day numbers stay calendar-local across a DST boundary
ok 663 - day numbers stay calendar-local across a DST boundary
  ---
  duration_ms: 0.491108
  ...
# Subtest: reviewModel shares counts, meter, tooltip, and severity
ok 664 - reviewModel shares counts, meter, tooltip, and severity
  ---
  duration_ms: 0.458054
  ...
# Subtest: memo serves warm map hits and misses use the per-row evaluator
ok 665 - memo serves warm map hits and misses use the per-row evaluator
  ---
  duration_ms: 7.264272
  ...
# Subtest: config snapshot caches the parse and invalidates explicitly
ok 666 - config snapshot caches the parse and invalidates explicitly
  ---
  duration_ms: 1.290314
  ...
# Subtest: review chips share the model with severity classes
ok 667 - review chips share the model with severity classes
  ---
  duration_ms: 0.977857
  ...
# Subtest: warm lookups reuse one snapshot without re-reading config
ok 668 - warm lookups reuse one snapshot without re-reading config
  ---
  duration_ms: 1.704705
  ...
# Subtest: same-array cache updates and Today changes rebuild the memo
ok 669 - same-array cache updates and Today changes rebuild the memo
  ---
  duration_ms: 2.745763
  ...
# Subtest: duplicate block IDs keep each row's own classification
ok 670 - duplicate block IDs keep each row's own classification
  ---
  duration_ms: 1.916059
  ...
# Subtest: line identity separates same-path rows without block IDs
ok 671 - line identity separates same-path rows without block IDs
  ---
  duration_ms: 1.05255
  ...
# Subtest: interval lookup serves the cached interval with one memo acquisition
ok 672 - interval lookup serves the cached interval with one memo acquisition
  ---
  duration_ms: 1.126983
  ...
# Subtest: S1 new through S4 overdue
ok 673 - S1 new through S4 overdue
  ---
  duration_ms: 3.1579
  ...
# Subtest: S5 task beats note, S6 note beats config, S7 config
ok 674 - S5 task beats note, S6 note beats config, S7 config
  ---
  duration_ms: 0.716549
  ...
# Subtest: S8 invalid overrides fall through with lints
ok 675 - S8 invalid overrides fall through with lints
  ---
  duration_ms: 0.495697
  ...
# Subtest: S9 malformed and S10 future stamps read as new
ok 676 - S9 malformed and S10 future stamps read as new
  ---
  duration_ms: 0.296225
  ...
# Subtest: S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
ok 677 - S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
  ---
  duration_ms: 0.426184
  ...
# Subtest: S13 out-of-scope rows read null
ok 678 - S13 out-of-scope rows read null
  ---
  duration_ms: 0.418129
  ...
# Subtest: S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
ok 679 - S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
  ---
  duration_ms: 1.69144
  ...
# Subtest: S15 counts (updated): upkeep outside the lanes drives the budget
ok 680 - S15 counts (updated): upkeep outside the lanes drives the budget
  ---
  duration_ms: 1.470668
  ...
# Subtest: config coercion keeps defaults, flags invalid, ignores unknown keys
ok 681 - config coercion keeps defaults, flags invalid, ignores unknown keys
  ---
  duration_ms: 1.302077
  ...
# Subtest: loadFreshnessConfig reads the block with plan-style injectables
ok 682 - loadFreshnessConfig reads the block with plan-style injectables
  ---
  duration_ms: 0.907373
  ...
# Subtest: interval precedence is task, note, config, default
ok 683 - interval precedence is task, note, config, default
  ---
  duration_ms: 0.212266
  ...
# Subtest: intervalForLine covers every source with its Ready fallback
ok 684 - intervalForLine covers every source with its Ready fallback
  ---
  duration_ms: 0.722289
  ...
# Subtest: project tracking stays special while reference tasks use ordinary Ready freshness
ok 685 - project tracking stays special while reference tasks use ordinary Ready freshness
  ---
  duration_ms: 3.712399
  ...
# Subtest: reference tasks match ordinary interval precedence and lane behavior
ok 686 - reference tasks match ordinary interval precedence and lane behavior
  ---
  duration_ms: 2.150787
  ...
# Subtest: obsolete reference interval keys are ignored and project config still validates
ok 687 - obsolete reference interval keys are ignored and project config still validates
  ---
  duration_ms: 0.69115
  ...
# Subtest: references use ordinary keep decisions and the nine-tier queue shape
ok 688 - references use ordinary keep decisions and the nine-tier queue shape
  ---
  duration_ms: 1.177659
  ...
# Subtest: CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
ok 689 - CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
  ---
  duration_ms: 2.489894
  ...
# Subtest: CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
ok 690 - CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
  ---
  duration_ms: 1.635092
  ...
# Subtest: freshness namespace v12 retains the tracker capability contract
ok 691 - freshness namespace v12 retains the tracker capability contract
  ---
  duration_ms: 4.389522
  ...
# Subtest: UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
ok 692 - UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
  ---
  duration_ms: 3.406935
  ...
# Subtest: UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
ok 693 - UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
  ---
  duration_ms: 0.452484
  ...
# Subtest: UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
ok 694 - UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
  ---
  duration_ms: 0.297598
  ...
# Subtest: UB11 scheduled wins a tie with the unblock date
ok 695 - UB11 scheduled wins a tie with the unblock date
  ---
  duration_ms: 0.285836
  ...
# Subtest: unblocked reader takes the latest valid duplicate and reports malformed values
ok 696 - unblocked reader takes the latest valid duplicate and reports malformed values
  ---
  duration_ms: 0.260517
  ...
# Subtest: UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
ok 697 - UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
  ---
  duration_ms: 0.404572
  ...
# Subtest: UB14 TICKLERs with the same due date sort only by path and line
ok 698 - UB14 TICKLERs with the same due date sort only by path and line
  ---
  duration_ms: 1.437846
  ...
# Subtest: UB15 a scheduled ^prj resurfaces in PROJECTS
ok 699 - UB15 a scheduled ^prj resurfaces in PROJECTS
  ---
  duration_ms: 0.20414
  ...
# Subtest: an active-note Pomodoro target still jumps and centers immediately
ok 700 - an active-note Pomodoro target still jumps and centers immediately
  ---
  duration_ms: 10.185861
  ...
# Subtest: the first fallback press only opens daily and the second press jumps
ok 701 - the first fallback press only opens daily and the second press jumps
  ---
  duration_ms: 2.356931
  ...
# Subtest: a daily note with no target defers its notice until the second press
ok 702 - a daily note with no target defers its notice until the second press
  ---
  duration_ms: 1.03166
  ...
# Subtest: an already-open daily leaf retains its live cursor and viewport
ok 703 - an already-open daily leaf retains its live cursor and viewport
  ---
  duration_ms: 1.309601
  ...
# Subtest: a second press after reused-leaf fallback performs the Pomodoro jump
ok 704 - a second press after reused-leaf fallback performs the Pomodoro jump
  ---
  duration_ms: 1.205041
  ...
# Subtest: the standalone daily-note command activates a reused daily leaf
ok 705 - the standalone daily-note command activates a reused daily leaf
  ---
  duration_ms: 0.937991
  ...
# Subtest: a closed then reopened daily note restores its in-session location
ok 706 - a closed then reopened daily note restores its in-session location
  ---
  duration_ms: 1.444879
  ...
# Subtest: different-path and invalid locations do not leak into a daily note
ok 707 - different-path and invalid locations do not leak into a daily note
  ---
  duration_ms: 0.808083
  ...
# Subtest: out-of-range remembered coordinates are clamped safely
ok 708 - out-of-range remembered coordinates are clamped safely
  ---
  duration_ms: 1.91106
  ...
# Subtest: a rapid second press cancels an older fallback restore
ok 709 - a rapid second press cancels an older fallback restore
  ---
  duration_ms: 1.257491
  ...
# Subtest: navigation and unload clean up daily scroll listeners and deferred work
ok 710 - navigation and unload clean up daily scroll listeners and deferred work
  ---
  duration_ms: 0.638489
  ...
# Subtest: crowded chip: over count is red with tooltip, aria, and names
ok 711 - crowded chip: over count is red with tooltip, aria, and names
  ---
  duration_ms: 1.598121
  ...
# Subtest: crowded chip: calm zero and unavailable dash
ok 712 - crowded chip: calm zero and unavailable dash
  ---
  duration_ms: 0.400495
  ...
# Subtest: crowded chip: names at most five notes
ok 713 - crowded chip: names at most five notes
  ---
  duration_ms: 0.306265
  ...
# Subtest: crowded chip: classes, text, aria, and arrow
ok 714 - crowded chip: classes, text, aria, and arrow
  ---
  duration_ms: 1.925487
  ...
# Subtest: crowded chip: refresh in place keeps the anchor, unload drops it
ok 715 - crowded chip: refresh in place keeps the anchor, unload drops it
  ---
  duration_ms: 0.727089
  ...
# Subtest: anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
ok 716 - anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
  ---
  duration_ms: 0.60714
  ...
# Subtest: ready-notes summary: crowded, calm, and unavailable
ok 717 - ready-notes summary: crowded, calm, and unavailable
  ---
  duration_ms: 0.289903
  ...
# Subtest: ready-notes bar: cap tick and red overflow within 30 cells
ok 718 - ready-notes bar: cap tick and red overflow within 30 cells
  ---
  duration_ms: 0.233155
  ...
# Subtest: ready-notes block: model and render with grid, pills, and footer
ok 719 - ready-notes block: model and render with grid, pills, and footer
  ---
  duration_ms: 1.728992
  ...
# Subtest: ready-notes block: unavailable renders a dash line
ok 720 - ready-notes block: unavailable renders a dash line
  ---
  duration_ms: 0.538909
  ...
# Subtest: heading matcher: fences, level, case, and first-only
ok 721 - heading matcher: fences, level, case, and first-only
  ---
  duration_ms: 0.472673
  ...
# Subtest: heading chip copy: room, full, crowded, exempt, unavailable
ok 722 - heading chip copy: room, full, crowded, exempt, unavailable
  ---
  duration_ms: 0.428177
  ...
# Subtest: heading chip key is stable for equal models
ok 723 - heading chip key is stable for equal models
  ---
  duration_ms: 0.181337
  ...
# Subtest: reading view: appends the chip to the matching h2 only
ok 724 - reading view: appends the chip to the matching h2 only
  ---
  duration_ms: 1.704304
  ...
# Subtest: reading view: no chip for ineligible notes
ok 725 - reading view: no chip for ineligible notes
  ---
  duration_ms: 0.135138
  ...
# Subtest: one live-refresh fan-out reaches every family
ok 726 - one live-refresh fan-out reaches every family
  ---
  duration_ms: 0.998617
  ...
# Subtest: ledger-tools CSS is theme-safe for the new views
ok 727 - ledger-tools CSS is theme-safe for the new views
  ---
  duration_ms: 0.79056
  ...
# Subtest: maxReadyPerNote defaults to 5 and validates 1–999
ok 728 - maxReadyPerNote defaults to 5 and validates 1–999
  ---
  duration_ms: 2.328016
  ...
# Subtest: loadPlanCaps caches on a stat key and detects edits
ok 729 - loadPlanCaps caches on a stat key and detects edits
  ---
  duration_ms: 0.527427
  ...
# Subtest: loadPlanCaps handles deletion, invalid edits, and recovery
ok 730 - loadPlanCaps handles deletion, invalid edits, and recovery
  ---
  duration_ms: 0.547044
  ...
# Subtest: loadPlanCaps without statSync reads through uncached
ok 731 - loadPlanCaps without statSync reads through uncached
  ---
  duration_ms: 0.318528
  ...
# Subtest: noteFrontmatter resolves through getFileCache, not getCache
ok 732 - noteFrontmatter resolves through getFileCache, not getCache
  ---
  duration_ms: 0.699205
  ...
# Subtest: task_refresh applies through the shared reader
ok 733 - task_refresh applies through the shared reader
  ---
  duration_ms: 3.554958
  ...
# Subtest: noteReadyKindFromType covers every R11 form
ok 734 - noteReadyKindFromType covers every R11 form
  ---
  duration_ms: 0.448947
  ...
# Subtest: noteReadyStatusLabel mirrors ProjectStatus::parse
ok 735 - noteReadyStatusLabel mirrors ProjectStatus::parse
  ---
  duration_ms: 0.259736
  ...
# Subtest: noteReadyParentStem strips alias, heading, and path
ok 736 - noteReadyParentStem strips alias, heading, and path
  ---
  duration_ms: 0.318458
  ...
# Subtest: parseNoteReadyCap covers every R8 form
ok 737 - parseNoteReadyCap covers every R8 form
  ---
  duration_ms: 0.632828
  ...
# Subtest: R1: 6 tasks at the default cap are crowded with over_by 1
ok 738 - R1: 6 tasks at the default cap are crowded with over_by 1
  ---
  duration_ms: 7.217883
  ...
# Subtest: R2: 5 tasks are full with no lint
ok 739 - R2: 5 tasks are full with no lint
  ---
  duration_ms: 1.724273
  ...
# Subtest: R3: hidden, future, blocked, and non-TODO rows never count
ok 740 - R3: hidden, future, blocked, and non-TODO rows never count
  ---
  duration_ms: 3.332073
  ...
# Subtest: R4: make-up splits 1 ready + 1 new + 1 rotten
ok 741 - R4: make-up splits 1 ready + 1 new + 1 rotten
  ---
  duration_ms: 1.67606
  ...
# Subtest: R5: recurring rows are excluded but tallied
ok 742 - R5: recurring rows are excluded but tallied
  ---
  duration_ms: 1.227083
  ...
# Subtest: R6: a visible ^prj task never counts
ok 743 - R6: a visible ^prj task never counts
  ---
  duration_ms: 1.062659
  ...
# Subtest: R7: daily, untyped, template, done, and dash rows are absent
ok 744 - R7: daily, untyped, template, done, and dash rows are absent
  ---
  duration_ms: 1.710606
  ...
# Subtest: R8: ready_cap forms map to cap, exempt, or lint-then-default
ok 745 - R8: ready_cap forms map to cap, exempt, or lint-then-default
  ---
  duration_ms: 2.582351
  ...
# Subtest: R9: a parent with two children counts 3
ok 746 - R9: a parent with two children counts 3
  ---
  duration_ms: 1.198439
  ...
# Subtest: R10: terminal projects are not capped and lint once
ok 747 - R10: terminal projects are not capped and lint once
  ---
  duration_ms: 1.298018
  ...
# Subtest: R11: every type form and nested folders are eligible
ok 748 - R11: every type form and nested folders are eligible
  ---
  duration_ms: 1.272159
  ...
# Subtest: R12: stamping a NEW task keeps the count and moves the make-up
ok 749 - R12: stamping a NEW task keeps the count and moves the make-up
  ---
  duration_ms: 4.225899
  ...
# Subtest: R13: a Today-linked task still counts
ok 750 - R13: a Today-linked task still counts
  ---
  duration_ms: 0.934936
  ...
# Subtest: R14: max_ready_per_note 3 caps others while ready_cap 8 holds
ok 751 - R14: max_ready_per_note 3 caps others while ready_cap 8 holds
  ---
  duration_ms: 3.077397
  ...
# Subtest: api.noteReady is frozen at version 1 under api v3
ok 752 - api.noteReady is frozen at version 1 under api v3
  ---
  duration_ms: 0.411225
  ...
# Subtest: counted and inCrowdedNote resolve per task
ok 753 - counted and inCrowdedNote resolve per task
  ---
  duration_ms: 2.40279
  ...
# Subtest: groupLabel ranks crowded notes by excess
ok 754 - groupLabel ranks crowded notes by excess
  ---
  duration_ms: 7.951926
  ...
# Subtest: snapshot sorts crowded, full, room, empty, exempt and splits totals
ok 755 - snapshot sorts crowded, full, room, empty, exempt and splits totals
  ---
  duration_ms: 11.016597
  ...
# Subtest: missing Tasks data and a cold cache are unavailable, never zero
ok 756 - missing Tasks data and a cold cache are unavailable, never zero
  ---
  duration_ms: 1.975503
  ...
# Subtest: throwing Tasks guards never throw
ok 757 - throwing Tasks guards never throw
  ---
  duration_ms: 1.087697
  ...
# Subtest: snapshot reuses the memo without reparsing or re-walking
ok 758 - snapshot reuses the memo without reparsing or re-walking
  ---
  duration_ms: 1.631756
  ...
# Subtest: a task edit rebuilds through the cache-update handler
ok 759 - a task edit rebuilds through the cache-update handler
  ---
  duration_ms: 1.702351
  ...
# Subtest: a ready_cap edit rebuilds and fires the query-refresh trigger
ok 760 - a ready_cap edit rebuilds and fires the query-refresh trigger
  ---
  duration_ms: 1.158342
  ...
# Subtest: rename and delete move the eligibility entry
ok 761 - rename and delete move the eligibility entry
  ---
  duration_ms: 1.464216
  ...
# Subtest: day rollover rebuilds the snapshot date
ok 762 - day rollover rebuilds the snapshot date
  ---
  duration_ms: 1.327515
  ...
# Subtest: a config edit flows through the stat cache
ok 763 - a config edit flows through the stat cache
  ---
  duration_ms: 2.384744
  ...
# Subtest: untyped and non-markdown vault events are no-ops
ok 764 - untyped and non-markdown vault events are no-ops
  ---
  duration_ms: 0.784348
  ...
# Subtest: memo hits never re-walk the vault
ok 765 - memo hits never re-walk the vault
  ---
  duration_ms: 66.878413
  ...
# Subtest: the startup storm is linear
not ok 766 - the startup storm is linear
  ---
  duration_ms: 33.259732
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-note-ready.cjs:1141:1'
  failureType: 'testCodeFailure'
  error: |-
    Expected values to be strictly equal:
    
    2 !== 1
    
  code: 'ERR_ASSERTION'
  name: 'AssertionError'
  expected: 1
  actual: 2
  operator: 'strictEqual'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-note-ready.cjs:1176:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: the first resolved event forces one rebuild and later ones do not
ok 767 - the first resolved event forces one rebuild and later ones do not
  ---
  duration_ms: 1.91674
  ...
# Subtest: noteReadyEvaluate is pure and mirrors the Rust totals
ok 768 - noteReadyEvaluate is pure and mirrors the Rust totals
  ---
  duration_ms: 0.34034
  ...
# Subtest: conformance: merged name with duplicate
ok 769 - conformance: merged name with duplicate
  ---
  duration_ms: 5.659878
  ...
# Subtest: conformance: link forms and exclusions
ok 770 - conformance: link forms and exclusions
  ---
  duration_ms: 1.063811
  ...
# Subtest: conformance: unnamed placeholders
ok 771 - conformance: unnamed placeholders
  ---
  duration_ms: 0.482201
  ...
# Subtest: conformance: subheading in the section
ok 772 - conformance: subheading in the section
  ---
  duration_ms: 0.300434
  ...
# Subtest: conformance: open inventory label
ok 773 - conformance: open inventory label
  ---
  duration_ms: 0.422216
  ...
# Subtest: conformance: over the cap
ok 774 - conformance: over the cap
  ---
  duration_ms: 0.269004
  ...
# Subtest: conformance: cancelled and completed entries
ok 775 - conformance: cancelled and completed entries
  ---
  duration_ms: 0.327876
  ...
# Subtest: exactly at the cap is fine
ok 776 - exactly at the cap is fine
  ---
  duration_ms: 0.242143
  ...
# Subtest: no Pomodoros section degrades to an empty budget
ok 777 - no Pomodoros section degrades to an empty budget
  ---
  duration_ms: 0.558356
  ...
# Subtest: fenced code never counts
ok 778 - fenced code never counts
  ---
  duration_ms: 0.694447
  ...
# Subtest: highlight is the first open non-exempt entry; running is the timed one
ok 779 - highlight is the first open non-exempt entry; running is the timed one
  ---
  duration_ms: 0.543588
  ...
# Subtest: coercePlanCaps ignores a legacy max_now instead of failing
ok 780 - coercePlanCaps ignores a legacy max_now instead of failing
  ---
  duration_ms: 0.406026
  ...
# Subtest: parsePlanCaps defaults, overrides, and invalid fallbacks
ok 781 - parsePlanCaps defaults, overrides, and invalid fallbacks
  ---
  duration_ms: 0.416976
  ...
# Subtest: loadPlanCaps falls back to defaults without fs
ok 782 - loadPlanCaps falls back to defaults without fs
  ---
  duration_ms: 0.596369
  ...
# Subtest: loadPlanCaps falls back to defaults on mobile
ok 783 - loadPlanCaps falls back to defaults on mobile
  ---
  duration_ms: 0.364907
  ...
# Subtest: loadPlanCaps reads plan: and flags invalid values
ok 784 - loadPlanCaps reads plan: and flags invalid values
  ---
  duration_ms: 0.572824
  ...
# Subtest: planBlockTargetPath prefers the containing daily note
ok 785 - planBlockTargetPath prefers the containing daily note
  ---
  duration_ms: 0.961426
  ...
# Subtest: planBlockModel degrades to placeholders, never an error
ok 786 - planBlockModel degrades to placeholders, never an error
  ---
  duration_ms: 1.169362
  ...
# Subtest: planBlockModel renders chips, themes, and lints
ok 787 - planBlockModel renders chips, themes, and lints
  ---
  duration_ms: 1.386377
  ...
# Subtest: planBlockModel adds lane cap lints when a lane is over
ok 788 - planBlockModel adds lane cap lints when a lane is over
  ---
  duration_ms: 0.934474
  ...
# Subtest: plugin exposes the versioned api and registers the bob-plan block
ok 789 - plugin exposes the versioned api and registers the bob-plan block
  ---
  duration_ms: 6.674876
  ...
# Subtest: invalid plan block falls back to full defaults
ok 790 - invalid plan block falls back to full defaults
  ---
  duration_ms: 0.383372
  ...
# Subtest: entries require column-0 dash-space with one status char
ok 791 - entries require column-0 dash-space with one status char
  ---
  duration_ms: 0.214189
  ...
# Subtest: crlf line endings split like lf
ok 792 - crlf line endings split like lf
  ---
  duration_ms: 0.280706
  ...
# Subtest: conformance: empty target means the daily note
ok 793 - conformance: empty target means the daily note
  ---
  duration_ms: 0.234728
  ...
# Subtest: lane predicate matches hide subtags, case, and non-task
ok 794 - lane predicate matches hide subtags, case, and non-task
  ---
  duration_ms: 0.292188
  ...
# Subtest: planBlockModel daily badges follow dashboard section counts
ok 795 - planBlockModel daily badges follow dashboard section counts
  ---
  duration_ms: 4.438647
  ...
# Subtest: planBlockModel keeps a supplied unavailable dashboard budget
ok 796 - planBlockModel keeps a supplied unavailable dashboard budget
  ---
  duration_ms: 0.423038
  ...
# Subtest: work tones: TODAY override and unavailable stay neutral in planBlockModel
ok 797 - work tones: TODAY override and unavailable stay neutral in planBlockModel
  ---
  duration_ms: 0.342244
  ...
# Subtest: shared vector: rollup-archive-review
ok 798 - shared vector: rollup-archive-review
  ---
  duration_ms: 7.007872
  ...
# Subtest: shared vector: review-decisions
ok 799 - shared vector: review-decisions
  ---
  duration_ms: 1.699405
  ...
# Subtest: shared vector: resolution-and-lints
ok 800 - shared vector: resolution-and-lints
  ---
  duration_ms: 2.070394
  ...
# Subtest: shared vector: chips, forecast shares, empty forecasts, and session identity
ok 801 - shared vector: chips, forecast shares, empty forecasts, and session identity
  ---
  duration_ms: 1.160125
  ...
# Subtest: shared vector: split-rounding-and-duration
ok 802 - shared vector: split-rounding-and-duration
  ---
  duration_ms: 0.639802
  ...
# Subtest: shared vector: share-rounding
ok 803 - shared vector: share-rounding
  ---
  duration_ms: 0.381108
  ...
# Subtest: shared vector: daily-review-link
ok 804 - shared vector: daily-review-link
  ---
  duration_ms: 0.353214
  ...
# Subtest: shared vector: rollup-depth-and-parent-shapes
ok 805 - shared vector: rollup-depth-and-parent-shapes
  ---
  duration_ms: 1.659108
  ...
# Subtest: shared vector: unresolved-and-closed-zero
ok 806 - shared vector: unresolved-and-closed-zero
  ---
  duration_ms: 0.860994
  ...
# Subtest: shared vector: parent-scalar-shapes
ok 807 - shared vector: parent-scalar-shapes
  ---
  duration_ms: 0.678115
  ...
# Subtest: dedicated link parser keeps embeds and one struck link, but rejects prose
ok 808 - dedicated link parser keeps embeds and one struck link, but rejects prose
  ---
  duration_ms: 0.21428
  ...
# Subtest: FNV-1a fallback for job maps to the pinned magenta slot
ok 809 - FNV-1a fallback for job maps to the pinned magenta slot
  ---
  duration_ms: 0.115481
  ...
# Subtest: rollup and area-color lints are reported once per note
ok 810 - rollup and area-color lints are reported once per note
  ---
  duration_ms: 0.36127
  ...
# Subtest: chip DOM exposes forecast, hue, accessible text, and tooltip
ok 811 - chip DOM exposes forecast, hue, accessible text, and tooltip
  ---
  duration_ms: 0.232334
  ...
# Subtest: Reading view appends a forecast chip before its Task Link list
ok 812 - Reading view appends a forecast chip before its Task Link list
  ---
  duration_ms: 4.594354
  ...
# Subtest: Live Preview places a chip widget at the end of the Pomodoro line
ok 813 - Live Preview places a chip widget at the end of the Pomodoro line
  ---
  duration_ms: 0.649951
  ...
# Subtest: Live Preview skips chips in Source mode
ok 814 - Live Preview skips chips in Source mode
  ---
  duration_ms: 0.171217
  ...
# Subtest: Reading view finds embedded Task Links via src
ok 815 - Reading view finds embedded Task Links via src
  ---
  duration_ms: 0.407047
  ...
# Subtest: Obsidian frontmatter shapes unwrap nested wikilink arrays
ok 816 - Obsidian frontmatter shapes unwrap nested wikilink arrays
  ---
  duration_ms: 0.154054
  ...
# Subtest: parser accepts the PM1-PM5 conformance vectors verbatim
ok 817 - parser accepts the PM1-PM5 conformance vectors verbatim
  ---
  duration_ms: 1.947018
  ...
# Subtest: parser rejects the PM7-PM12 conformance vectors verbatim
ok 818 - parser rejects the PM7-PM12 conformance vectors verbatim
  ---
  duration_ms: 0.376469
  ...
# Subtest: PM6 with the ladder unknown omits P-labels instead of guessing
ok 819 - PM6 with the ladder unknown omits P-labels instead of guessing
  ---
  duration_ms: 0.193078
  ...
# Subtest: PM13-PM17 ladder and line variants hold
ok 820 - PM13-PM17 ladder and line variants hold
  ---
  duration_ms: 0.3144
  ...
# Subtest: no model output contains a double colon
ok 821 - no model output contains a double colon
  ---
  duration_ms: 0.756154
  ...
# Subtest: element structure and the decorative/inheritColor options
ok 822 - element structure and the decorative/inheritColor options
  ---
  duration_ms: 0.330141
  ...
# Subtest: Live Preview decorations fold space, reveal, and refuse
ok 823 - Live Preview decorations fold space, reveal, and refuse
  ---
  duration_ms: 1.263533
  ...
# Subtest: a line with fresh and priority fields gets a disjoint decoration
ok 824 - a line with fresh and priority fields gets a disjoint decoration
  ---
  duration_ms: 0.199762
  ...
# Subtest: widget mousedown reveals the field at the folded offset
ok 825 - widget mousedown reveals the field at the folded offset
  ---
  duration_ms: 0.652506
  ...
# Subtest: rendered views split task nodes and skip exclusions
ok 826 - rendered views split task nodes and skip exclusions
  ---
  duration_ms: 1.457584
  ...
# Subtest: ladder coercion is lenient: valid, partial, and unknown
ok 827 - ladder coercion is lenient: valid, partial, and unknown
  ---
  duration_ms: 0.394283
  ...
# Subtest: ladder snapshot reads the file and reuses the cache
ok 828 - ladder snapshot reads the file and reuses the cache
  ---
  duration_ms: 2.134997
  ...
# Subtest: ladder snapshot degrades on missing files and parse errors
ok 829 - ladder snapshot degrades on missing files and parse errors
  ---
  duration_ms: 0.88491
  ...
# Subtest: ladder snapshot is unknown on mobile
ok 830 - ladder snapshot is unknown on mobile
  ---
  duration_ms: 13.5895
  ...
# Subtest: api.priorityMarks v1 is additive, sync, and never throwing
ok 831 - api.priorityMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 4.642134
  ...
# Subtest: session toggle and onload wiring
ok 832 - session toggle and onload wiring
  ---
  duration_ms: 0.752878
  ...
# Subtest: styles.css contract: masks, both hosts, repair flag, resting
ok 833 - styles.css contract: masks, both hosts, repair flag, resting
  ---
  duration_ms: 0.673276
  ...
# Subtest: P1/P3/P4: open entries mark plain and aliased links
ok 834 - P1/P3/P4: open entries mark plain and aliased links
  ---
  duration_ms: 2.501146
  ...
# Subtest: P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
ok 835 - P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
  ---
  duration_ms: 2.29333
  ...
# Subtest: P5: closed entries never mark, even with 🍅 history
ok 836 - P5: closed entries never mark, even with 🍅 history
  ---
  duration_ms: 0.641555
  ...
# Subtest: P6/P7: embedded and struck links never mark
ok 837 - P6/P7: embedded and struck links never mark
  ---
  duration_ms: 0.266659
  ...
# Subtest: P8: both trailing-\# move-only forms mark
ok 838 - P8: both trailing-\# move-only forms mark
  ---
  duration_ms: 0.268783
  ...
# Subtest: P9: nested and prose-mixed links never mark
ok 839 - P9: nested and prose-mixed links never mark
  ---
  duration_ms: 0.179393
  ...
# Subtest: P10: fenced, off-section, and off-note links never mark
ok 840 - P10: fenced, off-section, and off-note links never mark
  ---
  duration_ms: 0.367192
  ...
# Subtest: P11: unresolved targets and non-task blocks get no mark
ok 841 - P11: unresolved targets and non-task blocks get no mark
  ---
  duration_ms: 0.455419
  ...
# Subtest: P13: a same-note target reads the live doc
ok 842 - P13: a same-note target reads the live doc
  ---
  duration_ms: 0.761083
  ...
# Subtest: P14: expect() wins until the cache agrees or 4 s pass
ok 843 - P14: expect() wins until the cache agrees or 4 s pass
  ---
  duration_ms: 0.919846
  ...
# Subtest: tooltip, element structure, and eq
ok 844 - tooltip, element structure, and eq
  ---
  duration_ms: 0.294813
  ...
# Subtest: Live Preview places one widget at each In Progress link
ok 845 - Live Preview places one widget at each In Progress link
  ---
  duration_ms: 0.488673
  ...
# Subtest: widget mousedown places the cursor at the link start
ok 846 - widget mousedown places the cursor at the link start
  ---
  duration_ms: 0.355228
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
ok 847 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 0.422286
  ...
# Subtest: Reading view marks In Progress rows and dedupes
ok 848 - Reading view marks In Progress rows and dedupes
  ---
  duration_ms: 1.113336
  ...
# Subtest: Reading view refuses every non-mark row
ok 849 - Reading view refuses every non-mark row
  ---
  duration_ms: 1.035758
  ...
# Subtest: Reading view allows the 🍅 prefix and the trailing \# marker
ok 850 - Reading view allows the 🍅 prefix and the trailing \# marker
  ---
  duration_ms: 0.327435
  ...
# Subtest: api.progressMarks v1 is additive, sync, and never throwing
ok 851 - api.progressMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.614784
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 852 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 0.84807
  ...
# Subtest: changed-file and rollover refreshes
ok 853 - changed-file and rollover refreshes
  ---
  duration_ms: 0.362753
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 854 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.097396
  ...
# Subtest: styles.css contract: glyph, box, motion, toggle, calm
ok 855 - styles.css contract: glyph, box, motion, toggle, calm
  ---
  duration_ms: 0.600697
  ...
# Subtest: the board registers its code block processor and the Open Reading Board command
ok 856 - the board registers its code block processor and the Open Reading Board command
  ---
  duration_ms: 5.238142
  ...
# Subtest: four lanes render with counts, list and listitem roles, and one hint
ok 857 - four lanes render with counts, list and listitem roles, and one hint
  ---
  duration_ms: 12.004945
  ...
# Subtest: awake cards show kind, topic, added mark, counts, priority, and the pending-sync star
ok 858 - awake cards show kind, topic, added mark, counts, priority, and the pending-sync star
  ---
  duration_ms: 6.0632
  ...
# Subtest: a path-valued Bob audio field produces exactly one visible music marker
ok 859 - a path-valued Bob audio field produces exactly one visible music marker
  ---
  duration_ms: 2.044234
  ...
# Subtest: Snoozed shows Waking, date groups, and Waiting-on rows with their reasons
ok 860 - Snoozed shows Waking, date groups, and Waiting-on rows with their reasons
  ---
  duration_ms: 2.446623
  ...
# Subtest: TODAY pills float linked cards first, and never appear without a ready Today cache
ok 861 - TODAY pills float linked cards first, and never appear without a ready Today cache
  ---
  duration_ms: 5.197125
  ...
# Subtest: the PDF button needs the nav member, macOS, and a source_pdf
ok 862 - the PDF button needs the nav member, macOS, and a source_pdf
  ---
  duration_ms: 11.07572
  ...
# Subtest: click, modifier-click, middle-click, and the Task button route to openLinkText
ok 863 - click, modifier-click, middle-click, and the Task button route to openLinkText
  ---
  duration_ms: 2.026309
  ...
# Subtest: the board is one Tab stop and every key moves or acts
ok 864 - the board is one Tab stop and every key moves or acts
  ---
  duration_ms: 16.024981
  ...
# Subtest: movement targets stay inside the lanes that show cards
ok 865 - movement targets stay inside the lanes that show cards
  ---
  duration_ms: 0.715917
  ...
# Subtest: hovering a Waiting-on row outlines its prerequisite card on the board
ok 866 - hovering a Waiting-on row outlines its prerequisite card on the board
  ---
  duration_ms: 1.746845
  ...
# Subtest: the board never calls a vault write API, in the source or in any gesture
ok 867 - the board never calls a vault write API, in the source or in any gesture
  ---
  duration_ms: 10.194227
  ...
# Subtest: a repaint keeps focus by note path and each lane's scroll position
ok 868 - a repaint keeps focus by note path and each lane's scroll position
  ---
  duration_ms: 2.78574
  ...
# Subtest: a task move and topic/type update repaint handlers while preserving focus and scroll
ok 869 - a task move and topic/type update repaint handlers while preserving focus and scroll
  ---
  duration_ms: 2.859531
  ...
# Subtest: prerequisite identity changes repaint highlighting even when reason text is unchanged
ok 870 - prerequisite identity changes repaint highlighting even when reason text is unchanged
  ---
  duration_ms: 3.37227
  ...
# Subtest: an unchanged board is not repainted; only the data time updates in place
ok 871 - an unchanged board is not repainted; only the data time updates in place
  ---
  duration_ms: 3.214689
  ...
# Subtest: a Today cache change repaints boards from cached data without spawning bob
ok 872 - a Today cache change repaints boards from cached data without spawning bob
  ---
  duration_ms: 4.976953
  ...
# Subtest: first paint is a skeleton in the real grid, then the board without a layout jump
ok 873 - first paint is a skeleton in the real grid, then the board without a layout jump
  ---
  duration_ms: 4.501136
  ...
# Subtest: failures without a frame render an actionable card with Retry
ok 874 - failures without a frame render an actionable card with Retry
  ---
  duration_ms: 18.998039
  ...
# Subtest: a failed manual refresh keeps the last frame and says why with Retry
ok 875 - a failed manual refresh keeps the last frame and says why with Retry
  ---
  duration_ms: 5.510174
  ...
# Subtest: metadata revalidation delivers a silent stale-frame error and recovery updates freshness
ok 876 - metadata revalidation delivers a silent stale-frame error and recovery updates freshness
  ---
  duration_ms: 10.323524
  ...
# Subtest: stale-cache mount refresh failures reach the mounted view
ok 877 - stale-cache mount refresh failures reach the mounted view
  ---
  duration_ms: 7.031206
  ...
# Subtest: unload during a fetch prevents late repaint and queued spawns
ok 878 - unload during a fetch prevents late repaint and queued spawns
  ---
  duration_ms: 4.717408
  ...
# Subtest: in-flight edits and forced refreshes coalesce without dropping mounted fences
ok 879 - in-flight edits and forced refreshes coalesce without dropping mounted fences
  ---
  duration_ms: 15.297151
  ...
# Subtest: manual refresh shows a busy state until the result lands, then announces it
ok 880 - manual refresh shows a busy state until the result lands, then announces it
  ---
  duration_ms: 7.4313
  ...
# Subtest: an older bob without blocked_by falls back to Waiting-on with one lint line
ok 881 - an older bob without blocked_by falls back to Waiting-on with one lint line
  ---
  duration_ms: 4.057758
  ...
# Subtest: an empty queue shows bob's own phrase instead of lanes
ok 882 - an empty queue shows bob's own phrase instead of lanes
  ---
  duration_ms: 1.661613
  ...
# Subtest: fence options reach the fetch and bad options show as muted lint lines
ok 883 - fence options reach the fetch and bad options show as muted lint lines
  ---
  duration_ms: 8.67221
  ...
# Subtest: Snoozed collapses per source path, leaves the key order, and survives repaints
ok 884 - Snoozed collapses per source path, leaves the key order, and survives repaints
  ---
  duration_ms: 8.41561
  ...
# Subtest: unloading a block releases its view, and teardown clears the session state
ok 885 - unloading a block releases its view, and teardown clears the session state
  ---
  duration_ms: 1.707571
  ...
# Subtest: reading board stylesheet contract: selectors, layout, tabular-nums, motion, colors
ok 886 - reading board stylesheet contract: selectors, layout, tabular-nums, motion, colors
  ---
  duration_ms: 0.704576
  ...
# Subtest: Reading Board argv carries bob's fixed queue and optional fence filters
ok 887 - Reading Board argv carries bob's fixed queue and optional fence filters
  ---
  duration_ms: 2.118695
  ...
# Subtest: Reading Board decoder accepts the shared bob fixture and normalizes optional fields
ok 888 - Reading Board decoder accepts the shared bob fixture and normalizes optional fields
  ---
  duration_ms: 0.36682
  ...
# Subtest: Reading Board audio presence survives raw JSON decoding and model construction
ok 889 - Reading Board audio presence survives raw JSON decoding and model construction
  ---
  duration_ms: 7.327422
  ...
# Subtest: Reading Board decoder rejects malformed JSON, shapes, schema, and bob errors
ok 890 - Reading Board decoder rejects malformed JSON, shapes, schema, and bob errors
  ---
  duration_ms: 0.349087
  ...
# Subtest: shared bob spawn passes the vault environment, timeout, and buffer
ok 891 - shared bob spawn passes the vault environment, timeout, and buffer
  ---
  duration_ms: 7.727369
  ...
# Subtest: shared bob spawn maps missing binary and timeout failures
ok 892 - shared bob spawn maps missing binary and timeout failures
  ---
  duration_ms: 2.728541
  ...
# Subtest: Reading Board error cards explain not-found, timeout, schema, and bob errors
ok 893 - Reading Board error cards explain not-found, timeout, schema, and bob errors
  ---
  duration_ms: 0.626636
  ...
# Subtest: Reading Board cache returns stale data while revalidating and keeps a four-entry LRU
ok 894 - Reading Board cache returns stale data while revalidating and keeps a four-entry LRU
  ---
  duration_ms: 3.101192
  ...
# Subtest: Reading Board shares identical flights and coalesces one different follow-up
ok 895 - Reading Board shares identical flights and coalesces one different follow-up
  ---
  duration_ms: 1.580077
  ...
# Subtest: Reading Board refresh is mounted-only, debounced, and reacts to rollover and stale active leaves
ok 896 - Reading Board refresh is mounted-only, debounced, and reacts to rollover and stale active leaves
  ---
  duration_ms: 0.941789
  ...
# Subtest: the shared bob output builds the expected four lanes and preserves bob order
ok 897 - the shared bob output builds the expected four lanes and preserves bob order
  ---
  duration_ms: 4.371357
  ...
# Subtest: each status uses its awake lane and every blocked status uses Snoozed
ok 898 - each status uses its awake lane and every blocked status uses Snoozed
  ---
  duration_ms: 0.458586
  ...
# Subtest: Today floats cards by ledger rank only when the cache is ready
ok 899 - Today floats cards by ledger rank only when the cache is ready
  ---
  duration_ms: 1.218758
  ...
# Subtest: Snoozed groups show waking, schedule, dependency, project, return lane, and mark models
ok 900 - Snoozed groups show waking, schedule, dependency, project, return lane, and mark models
  ---
  duration_ms: 0.631586
  ...
# Subtest: schedule groups follow Monday-start weeks through Sunday across month and year ends
ok 901 - schedule groups follow Monday-start weeks through Sunday across month and year ends
  ---
  duration_ms: 0.256509
  ...
# Subtest: older bob output remains visible in Waiting on and explains the missing reasons
ok 902 - older bob output remains visible in Waiting on and explains the missing reasons
  ---
  duration_ms: 1.022323
  ...
# Subtest: fence options accept parent and type lists while turning bad input into lints
ok 903 - fence options accept parent and type lists while turning bad input into lints
  ---
  duration_ms: 1.426725
  ...
# Subtest: kind names, title code spans, and render signatures are deterministic
ok 904 - kind names, title code spans, and render signatures are deterministic
  ---
  duration_ms: 4.81815
  ...
# Subtest: max_ready defaults to 100 for missing, absent, and null values
ok 905 - max_ready defaults to 100 for missing, absent, and null values
  ---
  duration_ms: 2.107364
  ...
# Subtest: max_ready accepts a custom positive cap
ok 906 - max_ready accepts a custom positive cap
  ---
  duration_ms: 0.294903
  ...
# Subtest: max_ready rejects zero, negative, fractions, strings, booleans, and overflow
ok 907 - max_ready rejects zero, negative, fractions, strings, booleans, and overflow
  ---
  duration_ms: 1.242513
  ...
# Subtest: old configurations and legacy max_now still load
ok 908 - old configurations and legacy max_now still load
  ---
  duration_ms: 0.343115
  ...
# Subtest: READY boundary: only a strict excess turns red
ok 909 - READY boundary: only a strict excess turns red
  ---
  duration_ms: 2.858879
  ...
# Subtest: READY custom-cap boundary
ok 910 - READY custom-cap boundary
  ---
  duration_ms: 0.359496
  ...
# Subtest: READY over is independent of the PLAN ledger status
ok 911 - READY over is independent of the PLAN ledger status
  ---
  duration_ms: 6.231301
  ...
# Subtest: READY predicate: statuses, custom TODO symbols, and non-tasks
ok 912 - READY predicate: statuses, custom TODO symbols, and non-tasks
  ---
  duration_ms: 0.2723
  ...
# Subtest: READY predicate: blocked uses the full list, even outside the queue
ok 913 - READY predicate: blocked uses the full list, even outside the queue
  ---
  duration_ms: 0.552405
  ...
# Subtest: READY predicate: past, today, and future schedules
ok 914 - READY predicate: past, today, and future schedules
  ---
  duration_ms: 0.570069
  ...
# Subtest: READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
ok 915 - READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
  ---
  duration_ms: 0.380797
  ...
# Subtest: READY predicate: Today exclusion
ok 916 - READY predicate: Today exclusion
  ---
  duration_ms: 0.175815
  ...
# Subtest: readyTaskVisible excludes hide variants like Tasks
ok 917 - readyTaskVisible excludes hide variants like Tasks
  ---
  duration_ms: 0.171828
  ...
# Subtest: daily and dashboard share the READY element contract
ok 918 - daily and dashboard share the READY element contract
  ---
  duration_ms: 16.67376
  ...
# Subtest: READY placeholder keeps the limit in its tooltip
ok 919 - READY placeholder keeps the limit in its tooltip
  ---
  duration_ms: 0.259615
  ...
# Subtest: READY keyboard and modifier-key navigation
ok 920 - READY keyboard and modifier-key navigation
  ---
  duration_ms: 0.930277
  ...
# Subtest: READY unavailable without Tasks, on Cold/Initializing, or before Today
ok 921 - READY unavailable without Tasks, on Cold/Initializing, or before Today
  ---
  duration_ms: 2.082627
  ...
# Subtest: READY counts a valid empty queue as zero, not unavailable
ok 922 - READY counts a valid empty queue as zero, not unavailable
  ---
  duration_ms: 0.804466
  ...
# Subtest: READY stays compatible with hosts exposing only getTasks()
ok 923 - READY stays compatible with hosts exposing only getTasks()
  ---
  duration_ms: 1.927551
  ...
# Subtest: READY degrades to unavailable when the Today predicate throws
ok 924 - READY degrades to unavailable when the Today predicate throws
  ---
  duration_ms: 0.506517
  ...
# Subtest: READY renders label/value spans for every budget state
ok 925 - READY renders label/value spans for every budget state
  ---
  duration_ms: 1.375708
  ...
# Subtest: READY live refresh keeps the anchor, spans, and handlers
ok 926 - READY live refresh keeps the anchor, spans, and handlers
  ---
  duration_ms: 1.404842
  ...
# Subtest: READY refresh crosses the over-cap boundary and back
ok 927 - READY refresh crosses the over-cap boundary and back
  ---
  duration_ms: 0.603562
  ...
# Subtest: READY refresh crosses the unavailable boundary and back
ok 928 - READY refresh crosses the unavailable boundary and back
  ---
  duration_ms: 0.577623
  ...
# Subtest: READY never assigns the Obsidian text setter
ok 929 - READY never assigns the Obsidian text setter
  ---
  duration_ms: 1.060324
  ...
# Subtest: READY gating excludes review buckets and keeps the partition
ok 930 - READY gating excludes review buckets and keeps the partition
  ---
  duration_ms: 0.301856
  ...
# Subtest: gated READY tooltip carries total lane pressure
ok 931 - gated READY tooltip carries total lane pressure
  ---
  duration_ms: 0.138705
  ...
# Subtest: planBlockModel gates READY and shares the lane tooltip
ok 932 - planBlockModel gates READY and shares the lane tooltip
  ---
  duration_ms: 0.592432
  ...
# Subtest: READY lint appears only on a strict excess
ok 933 - READY lint appears only on a strict excess
  ---
  duration_ms: 3.790789
  ...
# Subtest: READY lint uses a custom cap
ok 934 - READY lint uses a custom cap
  ---
  duration_ms: 0.417767
  ...
# Subtest: lane lints appear in NEXT, PENDING, READY order
ok 935 - lane lints appear in NEXT, PENDING, READY order
  ---
  duration_ms: 1.641174
  ...
# Subtest: READY lint uses the gated count
ok 936 - READY lint uses the gated count
  ---
  duration_ms: 1.191505
  ...
# Subtest: READY lint stays silent while unavailable
ok 937 - READY lint stays silent while unavailable
  ---
  duration_ms: 0.352974
  ...
# Subtest: READY speaks each host's chip language (daily single-tone, dash two-tone)
ok 938 - READY speaks each host's chip language (daily single-tone, dash two-tone)
  ---
  duration_ms: 2.596658
  ...
# Subtest: daily paint carries lane pressure to the shared READY renderer
ok 939 - daily paint carries lane pressure to the shared READY renderer
  ---
  duration_ms: 20.360249
  ...
# Subtest: daily paint degrades to the legacy tooltip without freshness
ok 940 - daily paint degrades to the legacy tooltip without freshness
  ---
  duration_ms: 2.126881
  ...
# Subtest: work tones: READY model carries the displayed-count tone
ok 941 - work tones: READY model carries the displayed-count tone
  ---
  duration_ms: 0.158834
  ...
# Subtest: ledger parser agrees with shared LK vectors and parses source task children
ok 942 - ledger parser agrees with shared LK vectors and parses source task children
  ---
  duration_ms: 3.637839
  ...
# Subtest: relationIndex scans done sources, resolves both directions, and orders label suggestions
ok 943 - relationIndex scans done sources, resolves both directions, and orders label suggestions
  ---
  duration_ms: 6.860511
  ...
# Subtest: relationIndex applies changed, delete, rename, and unsaved editor overlays
ok 944 - relationIndex applies changed, delete, rename, and unsaved editor overlays
  ---
  duration_ms: 21.46578
  ...
# Subtest: ledger LK1–LK19 recognises relation shapes and keeps them out of plan links
ok 945 - ledger LK1–LK19 recognises relation shapes and keeps them out of plan links
  ---
  duration_ms: 2.637897
  ...
# Subtest: parseTrigger parses D[-]<N> dated-entry triggers with offset and span
ok 946 - parseTrigger parses D[-]<N> dated-entry triggers with offset and span
  ---
  duration_ms: 1.713041
  ...
# Subtest: computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
ok 947 - computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
  ---
  duration_ms: 0.398421
  ...
# Subtest: expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
ok 948 - expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
  ---
  duration_ms: 0.464026
  ...
# Subtest: findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
ok 949 - findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
  ---
  duration_ms: 0.350228
  ...
# Subtest: compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
ok 950 - compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
  ---
  duration_ms: 0.306445
  ...
# Subtest: parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
ok 951 - parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
  ---
  duration_ms: 0.165246
  ...
# Subtest: computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
ok 952 - computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
  ---
  duration_ms: 0.182228
  ...
# Subtest: findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
ok 953 - findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
  ---
  duration_ms: 0.189402
  ...
# Subtest: findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
ok 954 - findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
  ---
  duration_ms: 0.307738
  ...
# Subtest: expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
ok 955 - expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
  ---
  duration_ms: 0.600186
  ...
# Subtest: regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
ok 956 - regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
  ---
  duration_ms: 0.371198
  ...
# Subtest: expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
ok 957 - expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
  ---
  duration_ms: 0.286047
  ...
# Subtest: stats fence body sets defaults only and ignores the rest
ok 958 - stats fence body sets defaults only and ignores the rest
  ---
  duration_ms: 1.556042
  ...
# Subtest: stats tile models cover every unit and every quality
ok 959 - stats tile models cover every unit and every quality
  ---
  duration_ms: 0.447745
  ...
# Subtest: stats spark bars mark null gaps, zero ticks, and hollow today
ok 960 - stats spark bars mark null gaps, zero ticks, and hollow today
  ---
  duration_ms: 0.283822
  ...
# Subtest: stats table rows and CSV share the same points
ok 961 - stats table rows and CSV share the same points
  ---
  duration_ms: 0.644762
  ...
# Subtest: stats overview ids prefer the fence, then config, then report order
ok 962 - stats overview ids prefer the fence, then config, then report order
  ---
  duration_ms: 0.91628
  ...
# Subtest: stats window label always states today and tracking start
ok 963 - stats window label always states today and tracking start
  ---
  duration_ms: 0.213808
  ...
# Subtest: stats view state is session-only and per source path
ok 964 - stats view state is session-only and per source path
  ---
  duration_ms: 4.3614
  ...
# Subtest: stats block renders header, tiles, table, and footer from JSON
ok 965 - stats block renders header, tiles, table, and footer from JSON
  ---
  duration_ms: 42.945478
  ...
# Subtest: stats block shows an actionable card with Retry when bob fails
ok 966 - stats block shows an actionable card with Retry when bob fails
  ---
  duration_ms: 42.163144
  ...
# Subtest: stats block registers the processor and the Open Stats command
ok 967 - stats block registers the processor and the Open Stats command
  ---
  duration_ms: 1.847539
  ...
# Subtest: stats stylesheet contract: selectors, tabular-nums, motion, colors
ok 968 - stats stylesheet contract: selectors, tabular-nums, motion, colors
  ---
  duration_ms: 1.764521
  ...
# Subtest: Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
ok 969 - Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
  ---
  duration_ms: 2.059744
  ...
# Subtest: prior buckets align by elapsed position and omit invalid and provisional points
ok 970 - prior buckets align by elapsed position and omit invalid and provisional points
  ---
  duration_ms: 0.782124
  ...
# Subtest: chart renders SVG safely and keeps secondary focus metrics selectable
ok 971 - chart renders SVG safely and keeps secondary focus metrics selectable
  ---
  duration_ms: 11.911266
  ...
# Subtest: grouped chart pins honest buckets, bounds daily detail, and opens validated notes
ok 972 - grouped chart pins honest buckets, bounds daily detail, and opens validated notes
  ---
  duration_ms: 8.537583
  ...
# Subtest: local focus, table, pin, and definition changes reuse the retained report
ok 973 - local focus, table, pin, and definition changes reuse the retained report
  ---
  duration_ms: 6.564966
  ...
# Subtest: keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
ok 974 - keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
  ---
  duration_ms: 36.052845
  ...
# Subtest: schema-1 fallback keeps day quartiles and never invents grouped daily history
ok 975 - schema-1 fallback keeps day quartiles and never invents grouped daily history
  ---
  duration_ms: 4.220419
  ...
# Subtest: ResizeObserver redraws cached data and disconnects across rerenders and unload
ok 976 - ResizeObserver redraws cached data and disconnects across rerenders and unload
  ---
  duration_ms: 132.96817
  ...
# Subtest: stats resolution prefers stats.bob_path, then candidates, then PATH
ok 977 - stats resolution prefers stats.bob_path, then candidates, then PATH
  ---
  duration_ms: 1.556312
  ...
# Subtest: stats home expansion and range/offset normalization
ok 978 - stats home expansion and range/offset normalization
  ---
  duration_ms: 0.391988
  ...
# Subtest: stats fetch always runs show -a -f json plus the chosen flags
ok 979 - stats fetch always runs show -a -f json plus the chosen flags
  ---
  duration_ms: 0.322275
  ...
# Subtest: stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
ok 980 - stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
  ---
  duration_ms: 4.979589
  ...
# Subtest: stats spawn maps ENOENT, timeouts, and stderr to named errors
ok 981 - stats spawn maps ENOENT, timeouts, and stderr to named errors
  ---
  duration_ms: 1.94832
  ...
# Subtest: stats decode accepts schema 1 and rejects the rest defensively
ok 982 - stats decode accepts schema 1 and rejects the rest defensively
  ---
  duration_ms: 0.208538
  ...
# Subtest: stats error cards name the cause and the stats.bob_path fix
ok 983 - stats error cards name the cause and the stats.bob_path fix
  ---
  duration_ms: 0.320982
  ...
# Subtest: stats fetch shares one flight and coalesces one follow-up
ok 984 - stats fetch shares one flight and coalesces one follow-up
  ---
  duration_ms: 22.570109
  ...
# Subtest: stats cache is a small LRU keyed by the argument list
ok 985 - stats cache is a small LRU keyed by the argument list
  ---
  duration_ms: 1.966555
  ...
# Subtest: stats stale entries return immediately and refresh in the background
ok 986 - stats stale entries return immediately and refresh in the background
  ---
  duration_ms: 0.964041
  ...
# Subtest: stats api v2 keeps append and adds fetch plus bobPath
ok 987 - stats api v2 keeps append and adds fetch plus bobPath
  ---
  duration_ms: 0.56551
  ...
# Subtest: statsHomeDir defaults to the real home and strips a trailing slash
ok 988 - statsHomeDir defaults to the real home and strips a trailing slash
  ---
  duration_ms: 0.144065
  ...
# Subtest: stats mac regression: un-injected resolution probes the real home first
ok 989 - stats mac regression: un-injected resolution probes the real home first
  ---
  duration_ms: 0.158372
  ...
# Subtest: stats absolute candidates are probed verbatim with no doubled slashes
ok 990 - stats absolute candidates are probed verbatim with no doubled slashes
  ---
  duration_ms: 0.175565
  ...
# Subtest: stats with no home probes only absolute candidates
ok 991 - stats with no home probes only absolute candidates
  ---
  duration_ms: 0.206635
  ...
# Subtest: stats tilde config expands against the real home
ok 992 - stats tilde config expands against the real home
  ---
  duration_ms: 0.117946
  ...
# Subtest: stats candidate and tried lists share one source of truth
ok 993 - stats candidate and tried lists share one source of truth
  ---
  duration_ms: 0.119318
  ...
# Subtest: stats spawn bob-not-found tried list uses the real home
ok 994 - stats spawn bob-not-found tried list uses the real home
  ---
  duration_ms: 0.940596
  ...
# Subtest: stats unload clears views, timers, cache, and flights
ok 995 - stats unload clears views, timers, cache, and flights
  ---
  duration_ms: 0.551393
  ...
# Subtest: stats namespace v1 serializes versioned review answer JSONL
ok 996 - stats namespace v1 serializes versioned review answer JSONL
  ---
  duration_ms: 6.356758
  ...
# Subtest: stats journal rejects invalid calendar days and outcomes
ok 997 - stats journal rejects invalid calendar days and outcomes
  ---
  duration_ms: 1.109839
  ...
# Subtest: statsReviewHost lowercases, cuts at the first dot, and never throws
ok 998 - statsReviewHost lowercases, cuts at the first dot, and never throws
  ---
  duration_ms: 0.149134
  ...
# Subtest: stats journal plugin passthrough keeps a semver writer and falls back otherwise
ok 999 - stats journal plugin passthrough keeps a semver writer and falls back otherwise
  ---
  duration_ms: 0.822752
  ...
# Subtest: panel dispatch covers every family, custom kinds, and the net exception
ok 1000 - panel dispatch covers every family, custom kinds, and the net exception
  ---
  duration_ms: 0.979119
  ...
# Subtest: pomodoro panel shows the supplied total, shares, hue, and safe text
ok 1001 - pomodoro panel shows the supplied total, shares, hue, and safe text
  ---
  duration_ms: 11.181542
  ...
# Subtest: home parts use the report catalog for labels, hue slots, and pinned values
ok 1002 - home parts use the report catalog for labels, hue slots, and pinned values
  ---
  duration_ms: 12.734878
  ...
# Subtest: areas panel toggles Themes, pins spans, expands projects, and opens home links
ok 1003 - areas panel toggles Themes, pins spans, expands projects, and opens home links
  ---
  duration_ms: 18.372493
  ...
# Subtest: chart pin refreshes Where the time went and Themes honor the pinned span
ok 1004 - chart pin refreshes Where the time went and Themes honor the pinned span
  ---
  duration_ms: 4.30477
  ...
# Subtest: review rows keep their area hue and a missing homes report keeps the saved view
ok 1005 - review rows keep their area hue and a missing homes report keeps the saved view
  ---
  duration_ms: 3.875962
  ...
# Subtest: task home table uses catalog labels and keeps hue dots and mini-bars
ok 1006 - task home table uses catalog labels and keeps hue dots and mini-bars
  ---
  duration_ms: 3.9954
  ...
# Subtest: task flow stacks signed values, keeps missing constituents missing, and labels series
ok 1007 - task flow stacks signed values, keeps missing constituents missing, and labels series
  ---
  duration_ms: 2.792753
  ...
# Subtest: absent companions are named, custom filters are labeled overall, and net splits breakdowns
ok 1008 - absent companions are named, custom filters are labeled overall, and net splits breakdowns
  ---
  duration_ms: 3.158311
  ...
# Subtest: journal panels pair answers with review time and a gapped keep chart under 90%
ok 1009 - journal panels pair answers with review time and a gapped keep chart under 90%
  ---
  duration_ms: 3.665209
  ...
# Subtest: checklist calendar aligns Monday weeks with states, reasons, and provisional today
ok 1010 - checklist calendar aligns Monday weeks with states, reasons, and provisional today
  ---
  duration_ms: 4.564246
  ...
# Subtest: grouped calendars reuse daily points and old schemas fall back with a label
ok 1011 - grouped calendars reuse daily points and old schemas fall back with a label
  ---
  duration_ms: 2.221493
  ...
# Subtest: ISO year boundaries stay in one Monday week and chore dots expose text
ok 1012 - ISO year boundaries stay in one Monday week and chore dots expose text
  ---
  duration_ms: 1.666213
  ...
# Subtest: panel day selection pins the shared day and never fetches
ok 1013 - panel day selection pins the shared day and never fetches
  ---
  duration_ms: 6.244918
  ...
# Subtest: field and formula metrics keep only the focus chart and table
ok 1014 - field and formula metrics keep only the focus chart and table
  ---
  duration_ms: 0.958611
  ...
# Subtest: TT vectors verbatim: task-line gate plus boundary tokens
ok 1015 - TT vectors verbatim: task-line gate plus boundary tokens
  ---
  duration_ms: 2.612108
  ...
# Subtest: TT13-TT14 cursor reveal is inclusive
ok 1016 - TT13-TT14 cursor reveal is inclusive
  ---
  duration_ms: 1.183941
  ...
# Subtest: TT16 coexistence: task tag range is disjoint from priority and date marks
ok 1017 - TT16 coexistence: task tag range is disjoint from priority and date marks
  ---
  duration_ms: 1.269283
  ...
# Subtest: tooltip is exact and never contains a double colon
ok 1018 - tooltip is exact and never contains a double colon
  ---
  duration_ms: 0.226273
  ...
# Subtest: element structure: empty widget span with tooltip attributes
ok 1019 - element structure: empty widget span with tooltip attributes
  ---
  duration_ms: 0.283381
  ...
# Subtest: Live Preview decorations cover exactly the tag and respect reveal and code
ok 1020 - Live Preview decorations cover exactly the tag and respect reveal and code
  ---
  duration_ms: 0.60257
  ...
# Subtest: widget mousedown reveals the tag start
ok 1021 - widget mousedown reveals the tag start
  ---
  duration_ms: 0.442104
  ...
# Subtest: TR vectors verbatim: rendered views annotate eligible anchors in place
ok 1022 - TR vectors verbatim: rendered views annotate eligible anchors in place
  ---
  duration_ms: 1.280054
  ...
# Subtest: TR9 toggle strips document-wide and re-annotates on enable
ok 1023 - TR9 toggle strips document-wide and re-annotates on enable
  ---
  duration_ms: 0.852498
  ...
# Subtest: annotate and strip helpers are idempotent and defensive
ok 1024 - annotate and strip helpers are idempotent and defensive
  ---
  duration_ms: 0.391568
  ...
# Subtest: session toggle and onload wiring
ok 1025 - session toggle and onload wiring
  ---
  duration_ms: 3.8437
  ...
# Subtest: styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
ok 1026 - styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
  ---
  duration_ms: 0.832831
  ...
# Subtest: TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
ok 1027 - TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
  ---
  duration_ms: 0.333838
  ...
# Subtest: Live Preview ref decorations replace the whole pair and reveal both tags at once
ok 1028 - Live Preview ref decorations replace the whole pair and reveal both tags at once
  ---
  duration_ms: 0.334699
  ...
# Subtest: ref element structure: book classes, reference label, and tooltip
ok 1029 - ref element structure: book classes, reference label, and tooltip
  ---
  duration_ms: 0.130469
  ...
# Subtest: TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
ok 1030 - TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
  ---
  duration_ms: 0.652095
  ...
# Subtest: TR11 verbatim: \#task \#references and reversed order keep the hash only
ok 1031 - TR11 verbatim: \#task \#references and reversed order keep the hash only
  ---
  duration_ms: 0.247583
  ...
# Subtest: TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
ok 1032 - TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
  ---
  duration_ms: 0.147151
  ...
# Subtest: TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
ok 1033 - TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
  ---
  duration_ms: 0.490266
  ...
# Subtest: styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
ok 1034 - styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
  ---
  duration_ms: 0.640123
  ...
# Subtest: section info null stays neutral (TM19)
ok 1035 - section info null stays neutral (TM19)
  ---
  duration_ms: 1.941838
  ...
# Subtest: data-line mapping stamps and marks an exact Today row
ok 1036 - data-line mapping stamps and marks an exact Today row
  ---
  duration_ms: 2.778366
  ...
# Subtest: data-line mapping rejects a status mismatch
ok 1037 - data-line mapping rejects a status mismatch
  ---
  duration_ms: 0.318077
  ...
# Subtest: row-index fallback maps when counts agree and refuses when they disagree
ok 1038 - row-index fallback maps when counts agree and refuses when they disagree
  ---
  duration_ms: 1.335039
  ...
# Subtest: Tasks result rows and code are skipped
ok 1039 - Tasks result rows and code are skipped
  ---
  duration_ms: 0.401045
  ...
# Subtest: a daily-note sourcePath is skipped
ok 1040 - a daily-note sourcePath is skipped
  ---
  duration_ms: 0.224128
  ...
# Subtest: duplicate ids stay neutral
ok 1041 - duplicate ids stay neutral
  ---
  duration_ms: 0.616477
  ...
# Subtest: insertion points: \#task anchor, \#ref pair, checkbox, whitespace split
ok 1042 - insertion points: \#task anchor, \#ref pair, checkbox, whitespace split
  ---
  duration_ms: 1.336041
  ...
# Subtest: identity-proven non-Today rows are stamped without a mark
ok 1043 - identity-proven non-Today rows are stamped without a mark
  ---
  duration_ms: 0.642707
  ...
# Subtest: sweep adds on link, removes on unlink or completion, updates tooltip, respects toggle, skips daily ancestors
ok 1044 - sweep adds on link, removes on unlink or completion, updates tooltip, respects toggle, skips daily ancestors
  ---
  duration_ms: 1.863589
  ...
# Subtest: daily-view class is set on open daily leaves and cleared on switch
ok 1045 - daily-view class is set on open daily leaves and cleared on switch
  ---
  duration_ms: 0.410043
  ...
# Subtest: delegated Mod+click jumps; plain click does not
ok 1046 - delegated Mod+click jumps; plain click does not
  ---
  duration_ms: 1.336081
  ...
# Subtest: setupTodayMarks registers the reading post-processor at order 60
ok 1047 - setupTodayMarks registers the reading post-processor at order 60
  ---
  duration_ms: 0.390035
  ...
# Subtest: styles.css daily-view suppression is present
ok 1048 - styles.css daily-view suppression is present
  ---
  duration_ms: 0.716508
  ...
# Subtest: Live Preview marks do not double-jump in Reading view
ok 1049 - Live Preview marks do not double-jump in Reading view
  ---
  duration_ms: 0.436002
  ...
# Subtest: mid-body \#task goes at the body start
ok 1050 - mid-body \#task goes at the body start
  ---
  duration_ms: 0.555892
  ...
# Subtest: \#task inside inline code stays neutral
ok 1051 - \#task inside inline code stays neutral
  ---
  duration_ms: 0.279985
  ...
# Subtest: re-render with a new path refreshes the mark key
ok 1052 - re-render with a new path refreshes the mark key
  ---
  duration_ms: 0.371981
  ...
# Subtest: one duplicate scan per render
ok 1053 - one duplicate scan per render
  ---
  duration_ms: 1.799396
  ...
# Subtest: row-index fallback uses every list item
ok 1054 - row-index fallback uses every list item
  ---
  duration_ms: 0.603673
  ...
# Subtest: open statuses are exactly space, star, slash, and question
ok 1055 - open statuses are exactly space, star, slash, and question
  ---
  duration_ms: 1.563896
  ...
# Subtest: trailing-id rules: leading space, trailing-only, valid charset
ok 1056 - trailing-id rules: leading space, trailing-only, valid charset
  ---
  duration_ms: 0.345029
  ...
# Subtest: candidate: TM9 closed stays null, TM10 open statuses pass
ok 1057 - candidate: TM9 closed stays null, TM10 open statuses pass
  ---
  duration_ms: 1.252182
  ...
# Subtest: candidate: TM11 needs an exact \#task tag and a trailing id
ok 1058 - candidate: TM11 needs an exact \#task tag and a trailing id
  ---
  duration_ms: 0.211303
  ...
# Subtest: candidate: TM21 code is left for the call-site code check
ok 1059 - candidate: TM21 code is left for the call-site code check
  ---
  duration_ms: 0.250348
  ...
# Subtest: insert offset: \#task first lands before the title
ok 1060 - insert offset: \#task first lands before the title
  ---
  duration_ms: 0.194641
  ...
# Subtest: insert offset: TM16 \#task \#ref spans the pair, \#prj sits between
ok 1061 - insert offset: TM16 \#task \#ref spans the pair, \#prj sits between
  ---
  duration_ms: 0.240299
  ...
# Subtest: insert offset: mid-body \#task falls back to the body start
ok 1062 - insert offset: mid-body \#task falls back to the body start
  ---
  duration_ms: 0.134196
  ...
# Subtest: insert offset: blockquote, spaces, numbered, empty title, emoji
ok 1063 - insert offset: blockquote, spaces, numbered, empty title, emoji
  ---
  duration_ms: 0.461181
  ...
# Subtest: duplicates: TM15 marks neither line
ok 1064 - duplicates: TM15 marks neither line
  ---
  duration_ms: 0.49769
  ...
# Subtest: session text: named, home label, range-only, unnamed
ok 1065 - session text: named, home label, range-only, unnamed
  ---
  duration_ms: 0.295574
  ...
# Subtest: tooltip: TM1 running, TM2 queued, and the platform variants
ok 1066 - tooltip: TM1 running, TM2 queued, and the platform variants
  ---
  duration_ms: 0.242664
  ...
# Subtest: tooltip: running wins as primary with a +N more suffix
ok 1067 - tooltip: running wins as primary with a +N more suffix
  ---
  duration_ms: 0.130268
  ...
# Subtest: tooltip: empty input yields Today and output never has ::
ok 1068 - tooltip: empty input yields Today and output never has ::
  ---
  duration_ms: 0.211033
  ...
# Subtest: entering window: 600 ms after join, never before or at load
ok 1069 - entering window: 600 ms after join, never before or at load
  ---
  duration_ms: 0.117564
  ...
# Subtest: modifier: primary button with meta on mac, ctrl elsewhere
ok 1070 - modifier: primary button with meta on mac, ctrl elsewhere
  ---
  duration_ms: 0.133916
  ...
# Subtest: element: empty span with tooltip attributes and no listeners
ok 1071 - element: empty span with tooltip attributes and no listeners
  ---
  duration_ms: 0.279343
  ...
# Subtest: widget: eq ignores entering and the callback
ok 1072 - widget: eq ignores entering and the callback
  ---
  duration_ms: 0.169704
  ...
# Subtest: widget: plain mousedown moves the cursor, Mod mousedown jumps
ok 1073 - widget: plain mousedown moves the cursor, Mod mousedown jumps
  ---
  duration_ms: 0.467964
  ...
# Subtest: refresh effect is lazy and stable
ok 1074 - refresh effect is lazy and stable
  ---
  duration_ms: 0.104539
  ...
# Subtest: styles.css implements the glyph anatomy contract
ok 1075 - styles.css implements the glyph anatomy contract
  ---
  duration_ms: 0.559058
  ...
# Subtest: Live Preview applies the TM1-TM22 line, cache, and refresh vectors
ok 1076 - Live Preview applies the TM1-TM22 line, cache, and refresh vectors
  ---
  duration_ms: 19.75843
  ...
# Subtest: Today mark lifecycle registers the toggle, keyboard command, and reading processor
ok 1077 - Today mark lifecycle registers the toggle, keyboard command, and reading processor
  ---
  duration_ms: 13.828156
  ...
# Subtest: keyboard jump uses the task under the cursor and reports non-membership
ok 1078 - keyboard jump uses the task under the cursor and reports non-membership
  ---
  duration_ms: 15.64243
  ...
# Subtest: Mod-click and keyboard jumps land on the current running Task Link
ok 1079 - Mod-click and keyboard jumps land on the current running Task Link
  ---
  duration_ms: 12.74539
  ...
# Subtest: reduced motion stops the entrance pop
ok 1080 - reduced motion stops the entrance pop
  ---
  duration_ms: 0.593324
  ...
# Subtest: tooltips never contain ::
ok 1081 - tooltips never contain ::
  ---
  duration_ms: 0.159084
  ...
# Subtest: todayMarkPosInInlineCode: single, double, unmatched, positions
ok 1082 - todayMarkPosInInlineCode: single, double, unmatched, positions
  ---
  duration_ms: 0.313278
  ...
# Subtest: builder gates on Today ids without touching doc lines
ok 1083 - builder gates on Today ids without touching doc lines
  ---
  duration_ms: 11.581686
  ...
# Subtest: two rebuilds on the same doc compute duplicates once
ok 1084 - two rebuilds on the same doc compute duplicates once
  ---
  duration_ms: 17.008058
  ...
# Subtest: todayMarksNow override drives readiness
ok 1085 - todayMarksNow override drives readiness
  ---
  duration_ms: 16.02467
  ...
# Subtest: refresh dispatches only to non-daily leaves and uses 16 ms
ok 1086 - refresh dispatches only to non-daily leaves and uses 16 ms
  ---
  duration_ms: 10.411252
  ...
# Subtest: keyboard command gates closed status and daily notes
ok 1087 - keyboard command gates closed status and daily notes
  ---
  duration_ms: 16.245722
  ...
# Subtest: TM14 rollover: day N+1 shows no decoration
ok 1088 - TM14 rollover: day N+1 shows no decoration
  ---
  duration_ms: 9.287515
  ...
# Subtest: TM17 widget sits at line.from + insertCh with side -1
ok 1089 - TM17 widget sits at line.from + insertCh with side -1
  ---
  duration_ms: 17.528193
  ...
# Subtest: TM18 entering: new key pops then settles
ok 1090 - TM18 entering: new key pops then settles
  ---
  duration_ms: 13.22766
  ...
# Subtest: TM20 toggle flips class, notice, and refreshes non-daily leaves
ok 1091 - TM20 toggle flips class, notice, and refreshes non-daily leaves
  ---
  duration_ms: 19.454019
  ...
# Subtest: rebuild triggers: doc, viewport, LP field, file switch rebuild; selection alone does not
ok 1092 - rebuild triggers: doc, viewport, LP field, file switch rebuild; selection alone does not
  ---
  duration_ms: 17.38615
  ...
# Subtest: jump guards in-flight, prefers cached ledgerLine over later match
ok 1093 - jump guards in-flight, prefers cached ledgerLine over later match
  ---
  duration_ms: 10.285771
  ...
# Subtest: jump with no open daily leaf attempts the daily open
ok 1094 - jump with no open daily leaf attempts the daily open
  ---
  duration_ms: 9.126297
  ...
# Subtest: home labels: unnamed timed entry uses derived label and 1-based entryLine
ok 1095 - home labels: unnamed timed entry uses derived label and 1-based entryLine
  ---
  duration_ms: 17.451485
  ...
# Subtest: T1 GTD: empty target resolves to the daily note
ok 1096 - T1 GTD: empty target resolves to the daily note
  ---
  duration_ms: 2.748989
  ...
# Subtest: T2 markers: pomodoro mark counts, struck drops, embed counts
ok 1097 - T2 markers: pomodoro mark counts, struck drops, embed counts
  ---
  duration_ms: 0.583094
  ...
# Subtest: T3 closed entries: links under completed/cancelled entries drop
ok 1098 - T3 closed entries: links under completed/cancelled entries drop
  ---
  duration_ms: 0.190704
  ...
# Subtest: T4 shapes: mixed text and deeper descendants drop
ok 1099 - T4 shapes: mixed text and deeper descendants drop
  ---
  duration_ms: 0.296777
  ...
# Subtest: T5 dedupe: same task twice keeps the first position
ok 1100 - T5 dedupe: same task twice keeps the first position
  ---
  duration_ms: 0.310393
  ...
# Subtest: T6 fenced: links inside fenced blocks drop
ok 1101 - T6 fenced: links inside fenced blocks drop
  ---
  duration_ms: 0.256339
  ...
# Subtest: T7 status: the link layer lists every dedicated link
ok 1102 - T7 status: the link layer lists every dedicated link
  ---
  duration_ms: 0.276939
  ...
# Subtest: T8 unresolved: missing notes give no key
ok 1103 - T8 unresolved: missing notes give no key
  ---
  duration_ms: 0.156158
  ...
# Subtest: T9 alias: aliased links count under their target
ok 1104 - T9 alias: aliased links count under their target
  ---
  duration_ms: 0.365669
  ...
# Subtest: laneBudgetFromTasks counts the whole Next lane, Today included
ok 1105 - laneBudgetFromTasks counts the whole Next lane, Today included
  ---
  duration_ms: 1.111543
  ...
# Subtest: laneBudgetFromTasks counts Pending by type and flags over-cap
ok 1106 - laneBudgetFromTasks counts Pending by type and flags over-cap
  ---
  duration_ms: 0.343677
  ...
# Subtest: lane caps come from max_next/max_pending; legacy max_now is ignored
ok 1107 - lane caps come from max_next/max_pending; legacy max_now is ignored
  ---
  duration_ms: 0.16255
  ...
# Subtest: reload event name matches the Tasks bundle subscription
ok 1108 - reload event name matches the Tasks bundle subscription
  ---
  duration_ms: 0.086335
  ...
# Subtest: api v2 shape: Today and lane budgets, no nowBudget
ok 1109 - api v2 shape: Today and lane budgets, no nowBudget
  ---
  duration_ms: 4.165144
  ...
# Subtest: cache rebuild answers isToday/todayRank in ledger order
ok 1110 - cache rebuild answers isToday/todayRank in ledger order
  ---
  duration_ms: 2.12017
  ...
# Subtest: refresh fires only when the key set changes
ok 1111 - refresh fires only when the key set changes
  ---
  duration_ms: 0.912001
  ...
# Subtest: unready to ready with empty TODAY still refreshes open badges
ok 1112 - unready to ready with empty TODAY still refreshes open badges
  ---
  duration_ms: 0.919666
  ...
# Subtest: cache rebuilds on the daily changed event with the event content
ok 1113 - cache rebuilds on the daily changed event with the event content
  ---
  duration_ms: 0.680831
  ...
# Subtest: cache rebuilds once on resolved and at midnight rollover
ok 1114 - cache rebuilds once on resolved and at midnight rollover
  ---
  duration_ms: 1.110431
  ...
# Subtest: computeTodayLinks records entry range and placeholder
ok 1115 - computeTodayLinks records entry range and placeholder
  ---
  duration_ms: 0.322436
  ...
# Subtest: todayOpenEntries and todayRunningEntryLine follow the unique timed rule
ok 1116 - todayOpenEntries and todayRunningEntryLine follow the unique timed rule
  ---
  duration_ms: 0.34047
  ...
# Subtest: resolveTodayLinkKeys keeps duplicates; resolveTodayKeys is first-occurrence
ok 1117 - resolveTodayLinkKeys keeps duplicates; resolveTodayKeys is first-occurrence
  ---
  duration_ms: 0.184632
  ...
# Subtest: todayLinkDetails: named running, placeholder, unnamed home, unnamed none
ok 1118 - todayLinkDetails: named running, placeholder, unnamed home, unnamed none
  ---
  duration_ms: 0.205532
  ...
# Subtest: todayLinkDetails orders running first and keeps one detail per key+entry
ok 1119 - todayLinkDetails orders running first and keeps one detail per key+entry
  ---
  duration_ms: 0.178341
  ...
# Subtest: todayKeyParts splits at the last hash; idsByPath groups block ids
ok 1120 - todayKeyParts splits at the last hash; idsByPath groups block ids
  ---
  duration_ms: 0.139606
  ...
# Subtest: todayDetailsSignature changes only when details change
ok 1121 - todayDetailsSignature changes only when details change
  ---
  duration_ms: 0.203038
  ...
# Subtest: idsByPath and details accessors follow the rebuilt cache
ok 1122 - idsByPath and details accessors follow the rebuilt cache
  ---
  duration_ms: 2.049985
  ...
# Subtest: details-only change refreshes marks without a Tasks reload
ok 1123 - details-only change refreshes marks without a Tasks reload
  ---
  duration_ms: 0.892334
  ...
# Subtest: entered stamps only when the cache was already ready, then prune
ok 1124 - entered stamps only when the cache was already ready, then prune
  ---
  duration_ms: 1.255558
  ...
# Subtest: generation guard: reverse-order async reads keep the newer
ok 1125 - generation guard: reverse-order async reads keep the newer
  ---
  duration_ms: 0.878277
  ...
# Subtest: generation guard: a sync rebuild wins over an in-flight async read
ok 1126 - generation guard: a sync rebuild wins over an in-flight async read
  ---
  duration_ms: 0.524282
  ...
# Subtest: revalidateTodayCache is throttled and refreshes when not ready
ok 1127 - revalidateTodayCache is throttled and refreshes when not ready
  ---
  duration_ms: 0.581991
  ...
# Subtest: revalidateTodayCache respects layoutReady and backwards clock steps
ok 1128 - revalidateTodayCache respects layoutReady and backwards clock steps
  ---
  duration_ms: 0.44005
  ...
# Subtest: a done-today prerequisite shows the glyph
ok 1129 - a done-today prerequisite shows the glyph
  ---
  duration_ms: 3.426805
  ...
# Subtest: done yesterday does not show the glyph
ok 1130 - done yesterday does not show the glyph
  ---
  duration_ms: 0.405715
  ...
# Subtest: a struck link does not show the glyph
ok 1131 - a struck link does not show the glyph
  ---
  duration_ms: 0.249036
  ...
# Subtest: a closed entry does not show the glyph
ok 1132 - a closed entry does not show the glyph
  ---
  duration_ms: 0.238035
  ...
# Subtest: several prerequisites give +N
ok 1133 - several prerequisites give +N
  ---
  duration_ms: 0.470158
  ...
# Subtest: the model refuses every non-glyph shape
ok 1134 - the model refuses every non-glyph shape
  ---
  duration_ms: 0.78013
  ...
# Subtest: unblockedGlyphDoneToday needs DONE plus a today done date
ok 1135 - unblockedGlyphDoneToday needs DONE plus a today done date
  ---
  duration_ms: 0.245409
  ...
# Subtest: tooltip names one prerequisite and counts several
ok 1136 - tooltip names one prerequisite and counts several
  ---
  duration_ms: 0.284875
  ...
# Subtest: Live Preview places one glyph after each unblocked link
not ok 1137 - Live Preview places one glyph after each unblocked link
  ---
  duration_ms: 2.11558
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:546:1'
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
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:553:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Live Preview draws nothing without a warm cache or a live link
ok 1138 - Live Preview draws nothing without a warm cache or a live link
  ---
  duration_ms: 0.744321
  ...
# Subtest: widget mousedown places the cursor past the link
not ok 1139 - widget mousedown places the cursor past the link
  ---
  duration_ms: 0.371369
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:612:1'
  failureType: 'testCodeFailure'
  error: "Cannot read properties of undefined (reading 'value')"
  code: 'ERR_TEST_FAILURE'
  name: 'TypeError'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:615:69)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
not ok 1140 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 0.372271
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:654:1'
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
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:662:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Reading view glyphs unblocked rows and dedupes
not ok 1141 - Reading view glyphs unblocked rows and dedupes
  ---
  duration_ms: 1.257711
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:849:1'
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
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:858:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Reading view refuses every non-glyph row
ok 1142 - Reading view refuses every non-glyph row
  ---
  duration_ms: 1.315492
  ...
# Subtest: api.unblockedGlyph v1 is additive, sync, and never throwing
ok 1143 - api.unblockedGlyph v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.488162
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 1144 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 0.919566
  ...
# Subtest: changed-file and rollover refreshes
ok 1145 - changed-file and rollover refreshes
  ---
  duration_ms: 0.259285
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 1146 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.090563
  ...
# Subtest: styles.css contract: faint glyph, Done token, toggle
ok 1147 - styles.css contract: faint glyph, Done token, toggle
  ---
  duration_ms: 0.691992
  ...
# Subtest: Ledger Vim mappings restore \\p and retain the other normal-mode actions
ok 1148 - Ledger Vim mappings restore \\p and retain the other normal-mode actions
  ---
  duration_ms: 2.124116
  ...
# Subtest: workBadgeTone boundary vectors at cap 100 use exact comparisons
ok 1149 - workBadgeTone boundary vectors at cap 100 use exact comparisons
  ---
  duration_ms: 0.945045
  ...
# Subtest: workBadgeTone at cap 15 has no percentage rounding
ok 1150 - workBadgeTone at cap 15 has no percentage rounding
  ---
  duration_ms: 0.218407
  ...
# Subtest: workBadgeTone default caps, small caps, and cap changes
ok 1151 - workBadgeTone default caps, small caps, and cap changes
  ---
  duration_ms: 0.198719
  ...
# Subtest: workBadgeTone never coerces invalid input to zero
ok 1152 - workBadgeTone never coerces invalid input to zero
  ---
  duration_ms: 1.187117
  ...
# Subtest: TODAY links bands with themes at cap 3
ok 1153 - TODAY links bands with themes at cap 3
  ---
  duration_ms: 0.408199
  ...
# Subtest: TODAY theme overflow forces red, exact cap does not
ok 1154 - TODAY theme overflow forces red, exact cap does not
  ---
  duration_ms: 0.270997
  ...
# Subtest: TODAY unavailable stays neutral, empty section is grey
ok 1155 - TODAY unavailable stays neutral, empty section is grey
  ---
  duration_ms: 1.445621
  ...
# Subtest: PENDING/NEXT models color the section, READY its gated count
ok 1156 - PENDING/NEXT models color the section, READY its gated count
  ---
  duration_ms: 0.68109
  ...
# Subtest: READY uses its gated count even when the total lane is larger
ok 1157 - READY uses its gated count even when the total lane is larger
  ---
  duration_ms: 0.397348
  ...
# Subtest: cap equality still emits no cap lint
ok 1158 - cap equality still emits no cap lint
  ---
  duration_ms: 3.096323
  ...
# Subtest: lane DOM keeps exactly one tone through transitions and unavailability
ok 1159 - lane DOM keeps exactly one tone through transitions and unavailability
  ---
  duration_ms: 8.156235
  ...
# Subtest: READY DOM keeps exactly one tone and daily/dashboard models agree
ok 1160 - READY DOM keeps exactly one tone and daily/dashboard models agree
  ---
  duration_ms: 1.355128
  ...
# SKIP dashboard integration: BOB_DASHBOARD_FILE is not set
# SKIP dashboard fallback integration: BOB_DASHBOARD_FILE is not set
# SKIP dash CSS contract: BOB_DASHBOARD_FILE is not set
# Subtest: daily TODAY chip uses the theme-overflow tone
ok 1161 - daily TODAY chip uses the theme-overflow tone
  ---
  duration_ms: 18.761767
  ...
# Subtest: dashboard integration uses Work tones, TODAY override, and keeps Work order
ok 1162 - dashboard integration uses Work tones, TODAY override, and keeps Work order
  ---
  duration_ms: 0.77479
  ...
# Subtest: dashboard fallbacks keep Work tones without plugin renderers or colors
ok 1163 - dashboard fallbacks keep Work tones without plugin renderers or colors
  ---
  duration_ms: 0.393331
  ...
# Subtest: Work tone CSS covers each tone and uses the shared magenta value
ok 1164 - Work tone CSS covers each tone and uses the shared magenta value
  ---
  duration_ms: 1.053632
  ...
# Subtest: RBW6 mergeTargetPreparations keeps one write at the strongest lane
ok 1165 - RBW6 mergeTargetPreparations keeps one write at the strongest lane
  ---
  duration_ms: 2.53961
  ...
# Subtest: §15.7 notices use curly quotes and the Ready → Blocked copy
ok 1166 - §15.7 notices use curly quotes and the Ready → Blocked copy
  ---
  duration_ms: 0.573996
  ...
# Subtest: RBP1 same-note add is one transaction and matches forward bytes
ok 1167 - RBP1 same-note add is one transaction and matches forward bytes
  ---
  duration_ms: 23.317737
  ...
# Subtest: RBP2 background-leaf T matches forward bytes
ok 1168 - RBP2 background-leaf T matches forward bytes
  ---
  duration_ms: 6.159163
  ...
# Subtest: RBP3 closed T is written through vault.process and matches forward bytes
ok 1169 - RBP3 closed T is written through vault.process and matches forward bytes
  ---
  duration_ms: 4.807622
  ...
# Subtest: RBP4 ordinary transfer; a ^prj N is never raised
ok 1170 - RBP4 ordinary transfer; a ^prj N is never raised
  ---
  duration_ms: 18.591903
  ...
# Subtest: RBP5 consumed Pomodoro link matches forward bytes
ok 1171 - RBP5 consumed Pomodoro link matches forward bytes
  ---
  duration_ms: 7.660699
  ...
# Subtest: RBP6 project T with residents and a sub-project matches forward bytes
ok 1172 - RBP6 project T with residents and a sub-project matches forward bytes
  ---
  duration_ms: 23.370859
  ...
# Subtest: RBP7 two dependents in different lanes prepare N once at [/]
ok 1173 - RBP7 two dependents in different lanes prepare N once at [/]
  ---
  duration_ms: 10.308685
  ...
# Subtest: RBP8 counted sources N1 and N2 match forward(T + N1, N2)
ok 1174 - RBP8 counted sources N1 and N2 match forward(T + N1, N2)
  ---
  duration_ms: 5.049933
  ...
# Subtest: RBP9 blocks_lines false writes no BLOCKS and still ids N
ok 1175 - RBP9 blocks_lines false writes no BLOCKS and still ids N
  ---
  duration_ms: 2.406666
  ...
# Subtest: RBP10 removing the last reason matches forward removal
ok 1176 - RBP10 removing the last reason matches forward removal
  ---
  duration_ms: 4.90211
  ...
# Subtest: RBW1 a changed source note writes nothing
ok 1177 - RBW1 a changed source note writes nothing
  ---
  duration_ms: 2.486488
  ...
# Subtest: RBW2 one changed T note still lands the others and omits it from BLOCKS
ok 1178 - RBW2 one changed T note still lands the others and omits it from BLOCKS
  ---
  duration_ms: 2.342393
  ...
# Subtest: RBW3 already-present picks write nothing
ok 1179 - RBW3 already-present picks write nothing
  ---
  duration_ms: 1.911059
  ...
# Subtest: RBW4 cleanup runs for T's that committed when N lives in today's daily note
ok 1180 - RBW4 cleanup runs for T's that committed when N lives in today's daily note
  ---
  duration_ms: 3.382008
  ...
# Subtest: RBW6 counted forward two-lane dependents prepare N once
ok 1181 - RBW6 counted forward two-lane dependents prepare N once
  ---
  duration_ms: 10.899354
  ...
# Subtest: A1 N above two T's in one note matches forward (open and closed note)
ok 1182 - A1 N above two T's in one note matches forward (open and closed note)
  ---
  duration_ms: 22.308111
  ...
# Subtest: A1 N below two T's matches forward bytes
ok 1183 - A1 N below two T's matches forward bytes
  ---
  duration_ms: 4.054232
  ...
# Subtest: A2 forward stamps the dependent when a prerequisite above gains BLOCKS
ok 1184 - A2 forward stamps the dependent when a prerequisite above gains BLOCKS
  ---
  duration_ms: 3.365908
  ...
# Subtest: A1 mixed same-note and cross-note picks keep N's lane rise (RBP7 variant)
ok 1185 - A1 mixed same-note and cross-note picks keep N's lane rise (RBP7 variant)
  ---
  duration_ms: 3.756724
  ...
# Subtest: A1 RBP1 with N truly lacking ^id is prompted an id and matches forward
ok 1186 - A1 RBP1 with N truly lacking ^id is prompted an id and matches forward
  ---
  duration_ms: 2.391076
  ...
# Subtest: A1 N lacking ^id in a closed note above T keeps its BLOCKS line under N
ok 1187 - A1 N lacking ^id in a closed note above T keeps its BLOCKS line under N
  ---
  duration_ms: 1.684076
  ...
# Subtest: A3 mirror lists the committed T's by identity (N above T1, X, T2)
ok 1188 - A3 mirror lists the committed T's by identity (N above T1, X, T2)
  ---
  duration_ms: 2.097666
  ...
# Subtest: A4 notices name T, not N (add, remove, project, counted)
ok 1189 - A4 notices name T, not N (add, remove, project, counted)
  ---
  duration_ms: 7.853186
  ...
# Subtest: A5 the writer's stale notice is returned once and never shown by the writer
ok 1190 - A5 the writer's stale notice is returned once and never shown by the writer
  ---
  duration_ms: 0.444428
  ...
# Subtest: A6 a changed T row (rawLine) is refused before any write
ok 1191 - A6 a changed T row (rawLine) is refused before any write
  ---
  duration_ms: 1.211994
  ...
# Subtest: A7 RBW2 keeps the failed T's Pomodoro link and consumes the committed one
ok 1192 - A7 RBW2 keeps the failed T's Pomodoro link and consumes the committed one
  ---
  duration_ms: 2.945235
  ...
# Subtest: A8 closed-note T guards run when the gesture is applied
ok 1193 - A8 closed-note T guards run when the gesture is applied
  ---
  duration_ms: 3.752286
  ...
# Subtest: A9 a ^prj T's residents recover with [unblocked::] when N lives in a daily note
ok 1194 - A9 a ^prj T's residents recover with [unblocked::] when N lives in a daily note
  ---
  duration_ms: 20.950677
  ...
# Subtest: A5 a preparation no write can carry fails the plan instead of being dropped
ok 1195 - A5 a preparation no write can carry fails the plan instead of being dropped
  ---
  duration_ms: 0.89518
  ...
# Subtest: applyDependencyEdit adding a first cross-note prerequisite keeps the dependent's cursor
ok 1196 - applyDependencyEdit adding a first cross-note prerequisite keeps the dependent's cursor
  ---
  duration_ms: 2.00047
  ...
# Subtest: applyBlocksEdit giving a source its first BLOCKS line keeps the source's cursor
ok 1197 - applyBlocksEdit giving a source its first BLOCKS line keeps the source's cursor
  ---
  duration_ms: 6.554206
  ...
# Subtest: nav BK1–BK2 accept canonical BLOCKS lines
ok 1198 - nav BK1–BK2 accept canonical BLOCKS lines
  ---
  duration_ms: 2.243855
  ...
# Subtest: nav BK3–BK11 canonicalise
ok 1199 - nav BK3–BK11 canonicalise
  ---
  duration_ms: 0.554048
  ...
# Subtest: nav BK12 empty, BK13–BK15 malformed
ok 1200 - nav BK12 empty, BK13–BK15 malformed
  ---
  duration_ms: 0.210853
  ...
# Subtest: nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse
ok 1201 - nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse
  ---
  duration_ms: 0.337695
  ...
# Subtest: nav BK21 code-point sort and writer format
ok 1202 - nav BK21 code-point sort and writer format
  ---
  duration_ms: 0.276317
  ...
# Subtest: nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS
ok 1203 - nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS
  ---
  duration_ms: 0.435231
  ...
# Subtest: nav BW18 conversion drops BLOCKS like Sub-projects
ok 1204 - nav BW18 conversion drops BLOCKS like Sub-projects
  ---
  duration_ms: 0.939615
  ...
# Subtest: nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner
ok 1205 - nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner
  ---
  duration_ms: 0.74921
  ...
# Subtest: nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists
ok 1206 - nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists
  ---
  duration_ms: 1.553607
  ...
# Subtest: nav MC1/MC2 deferred Pomodoro cleanup skips managed lines
ok 1207 - nav MC1/MC2 deferred Pomodoro cleanup skips managed lines
  ---
  duration_ms: 0.400806
  ...
# Subtest: showBlocksStage opens from a task with reverse CURRENT and RESULTS
ok 1208 - showBlocksStage opens from a task with reverse CURRENT and RESULTS
  ---
  duration_ms: 19.455331
  ...
# Subtest: showBlocksStage opens from a counted session
ok 1209 - showBlocksStage opens from a counted session
  ---
  duration_ms: 2.174302
  ...
# Subtest: showBlocksStage opens on a Task Link target note
ok 1210 - showBlocksStage opens on a Task Link target note
  ---
  duration_ms: 1.783275
  ...
# Subtest: RBU1 empty query uses today-first then In Progress, Next, same-note, rest
ok 1211 - RBU1 empty query uses today-first then In Progress, Next, same-note, rest
  ---
  duration_ms: 2.517077
  ...
# Subtest: RBU2 today-linked rows carry 🍅 running and strip names the entry
ok 1212 - RBU2 today-linked rows carry 🍅 running and strip names the entry
  ---
  duration_ms: 1.62887
  ...
# Subtest: RBU3 CURRENT 🔑 only when N is the last reason
ok 1213 - RBU3 CURRENT 🔑 only when N is the last reason
  ---
  duration_ms: 2.052499
  ...
# Subtest: RBU4 footer verbs are block, remove, and apply N
ok 1214 - RBU4 footer verbs are block, remove, and apply N
  ---
  duration_ms: 1.863269
  ...
# Subtest: RBU5 subtitle at rest, with marks, and names this task first
ok 1215 - RBU5 subtitle at rest, with marks, and names this task first
  ---
  duration_ms: 2.083981
  ...
# Subtest: RBG1 N itself is excluded from RESULTS
ok 1216 - RBG1 N itself is excluded from RESULTS
  ---
  duration_ms: 0.809937
  ...
# Subtest: RBG2 a cycle disables the row with path tooltip copy
ok 1217 - RBG2 a cycle disables the row with path tooltip copy
  ---
  duration_ms: 1.108267
  ...
# Subtest: RBG3 ^prj T with N inside the project is inside this project
ok 1218 - RBG3 ^prj T with N inside the project is inside this project
  ---
  duration_ms: 1.980343
  ...
# Subtest: RBG3 descendant N disables the parent project as a sub-project
ok 1219 - RBG3 descendant N disables the parent project as a sub-project
  ---
  duration_ms: 1.156809
  ...
# Subtest: RBG4 a malformed or second Depends-On line is guarded
ok 1220 - RBG4 a malformed or second Depends-On line is guarded
  ---
  duration_ms: 0.938612
  ...
# Subtest: RBG5 stale refuse reopens in the Blocks direction
ok 1221 - RBG5 stale refuse reopens in the Blocks direction
  ---
  duration_ms: 2.207185
  ...
# Subtest: RBG5 for T: a T changed after stage open refuses once and writes nothing
ok 1222 - RBG5 for T: a T changed after stage open refuses once and writes nothing
  ---
  duration_ms: 2.595577
  ...
# Subtest: today's links survive a pool refresh that lands while the daily note loads
ok 1223 - today's links survive a pool refresh that lands while the daily note loads
  ---
  duration_ms: 32.557311
  ...
# Subtest: RBG8 Esc from the stage or the block-ID prompt writes nothing
ok 1224 - RBG8 Esc from the stage or the block-ID prompt writes nothing
  ---
  duration_ms: 2.083739
  ...
# Subtest: missing source ^id opens the block-ID prompt and Esc allocates none
ok 1225 - missing source ^id opens the block-ID prompt and Esc allocates none
  ---
  duration_ms: 1.080053
  ...
# Subtest: RBP11 inbox route runs first then the Blocks write
ok 1226 - RBP11 inbox route runs first then the Blocks write
  ---
  duration_ms: 0.766634
  ...
# Subtest: RBW5 review walk stays unless the commit takes N out of today's walk
ok 1227 - RBW5 review walk stays unless the commit takes N out of today's walk
  ---
  duration_ms: 6.345647
  ...
# Subtest: marks commit add and remove together; counted uses k/n block
ok 1228 - marks commit add and remove together; counted uses k/n block
  ---
  duration_ms: 2.90623
  ...
# Subtest: strip text covers RESULTS, BLOCKED, CURRENT, disabled, marks, and ^prj
ok 1229 - strip text covers RESULTS, BLOCKED, CURRENT, disabled, marks, and ^prj
  ---
  duration_ms: 0.344728
  ...
# Subtest: counted subtitle drops the ⇥ hint because marks are off in counted sessions
ok 1230 - counted subtitle drops the ⇥ hint because marks are off in counted sessions
  ---
  duration_ms: 0.71767
  ...
# Subtest: 🔑 tooltip and 🍅 tooltip render on badges
ok 1231 - 🔑 tooltip and 🍅 tooltip render on badges
  ---
  duration_ms: 0.844533
  ...
# Subtest: Tab marks Blocks CURRENT rows and Enter removes both dependents
ok 1232 - Tab marks Blocks CURRENT rows and Enter removes both dependents
  ---
  duration_ms: 11.516131
  ...
# Subtest: SB1-SB9 dependent IDs match the successor mint vectors
ok 1233 - SB1-SB9 dependent IDs match the successor mint vectors
  ---
  duration_ms: 2.310622
  ...
# Subtest: BW1 same-note add mints and writes BLOCKS in the dependent's single transaction
ok 1234 - BW1 same-note add mints and writes BLOCKS in the dependent's single transaction
  ---
  duration_ms: 10.511804
  ...
# Subtest: BW2 cross-note add follows the dependent commit and writes the target note
ok 1235 - BW2 cross-note add follows the dependent commit and writes the target note
  ---
  duration_ms: 2.774227
  ...
# Subtest: BW4 cross-note target preparation precedes the reverse-line preimage
ok 1236 - BW4 cross-note target preparation precedes the reverse-line preimage
  ---
  duration_ms: 1.786191
  ...
# Subtest: BW3 stale cross-note preimage leaves the forward write standing and shows the suffix
ok 1237 - BW3 stale cross-note preimage leaves the forward write standing and shows the suffix
  ---
  duration_ms: 1.258653
  ...
# Subtest: BW5 removal deletes the reverse line when its last dependent leaves
ok 1238 - BW5 removal deletes the reverse line when its last dependent leaves
  ---
  duration_ms: 3.179822
  ...
# Subtest: BW6 an already mirrored edge is a byte-identical no-op
ok 1239 - BW6 an already mirrored edge is a byte-identical no-op
  ---
  duration_ms: 0.746726
  ...
# Subtest: BW7 closed owners stay frozen
ok 1240 - BW7 closed owners stay frozen
  ---
  duration_ms: 1.47652
  ...
# Subtest: BW8 malformed reverse lines stay untouched and report the failed mirror
ok 1241 - BW8 malformed reverse lines stay untouched and report the failed mirror
  ---
  duration_ms: 1.399813
  ...
# Subtest: BW15 config defaults on, honors false, and invalid values fall back on
ok 1242 - BW15 config defaults on, honors false, and invalid values fall back on
  ---
  duration_ms: 0.62314
  ...
# Subtest: BW17 planner output follows BK21 Unicode code-point ordering
ok 1243 - BW17 planner output follows BK21 Unicode code-point ordering
  ---
  duration_ms: 0.364396
  ...
# Subtest: duplicate BLOCKS children merge their known dependents and preserve CRLF
ok 1244 - duplicate BLOCKS children merge their known dependents and preserve CRLF
  ---
  duration_ms: 0.4081
  ...
# Subtest: BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270)
ok 1245 - BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270)
  ---
  duration_ms: 3.153732
  ...
# Subtest: counted remove-from-all drops every dependent from the same-note BLOCKS line (420)
ok 1246 - counted remove-from-all drops every dependent from the same-note BLOCKS line (420)
  ---
  duration_ms: 1.055726
  ...
# Subtest: vault counted add composes cross-note follow-ups for every source (420)
ok 1247 - vault counted add composes cross-note follow-ups for every source (420)
  ---
  duration_ms: 0.673456
  ...
# Subtest: marked batch add writes every same-note target onto BLOCKS in one plan (430)
ok 1248 - marked batch add writes every same-note target onto BLOCKS in one plan (430)
  ---
  duration_ms: 0.462433
  ...
# Subtest: counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600)
ok 1249 - counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600)
  ---
  duration_ms: 7.20047
  ...
# Subtest: BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves
ok 1250 - BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves
  ---
  duration_ms: 2.316684
  ...
# Subtest: BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS
ok 1251 - BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS
  ---
  duration_ms: 2.459076
  ...
# Subtest: hand-edit clear path routes through the BLOCKS seam (600)
ok 1252 - hand-edit clear path routes through the BLOCKS seam (600)
  ---
  duration_ms: 0.659049
  ...
# Subtest: BW18 conversion never copies a BLOCKS line as a user child
ok 1253 - BW18 conversion never copies a BLOCKS line as a user child
  ---
  duration_ms: 0.694967
  ...
# Subtest: BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it
ok 1254 - BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it
  ---
  duration_ms: 3.533609
  ...
# Subtest: review checklist group helpers format exact completion and close notices
ok 1255 - review checklist group helpers format exact completion and close notices
  ---
  duration_ms: 2.718852
  ...
# Subtest: claim declines without a current exact PRE/POST walk landing
ok 1256 - claim declines without a current exact PRE/POST walk landing
  ---
  duration_ms: 8.862404
  ...
# Subtest: a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
ok 1257 - a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
  ---
  duration_ms: 3.572552
  ...
# Subtest: checklist Ctrl+Enter holds its landing through the actual successor picker
ok 1258 - checklist Ctrl+Enter holds its landing through the actual successor picker
  ---
  duration_ms: 11.983827
  ...
# Subtest: seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
ok 1259 - seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
  ---
  duration_ms: 18.700721
  ...
# Subtest: a landed [?] checklist chore is claimed and completed
ok 1260 - a landed [?] checklist chore is claimed and completed
  ---
  duration_ms: 0.807422
  ...
# Subtest: ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
ok 1261 - ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
  ---
  duration_ms: 2.266778
  ...
# Subtest: live successor filtering skips a stale completed row
ok 1262 - live successor filtering skips a stale completed row
  ---
  duration_ms: 0.809325
  ...
# Subtest: live group filtering reads each cross-note path once
ok 1263 - live group filtering reads each cross-note path once
  ---
  duration_ms: 0.703784
  ...
# Subtest: Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
ok 1264 - Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
  ---
  duration_ms: 3.139335
  ...
# Subtest: POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
ok 1265 - POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
  ---
  duration_ms: 1.642857
  ...
# Subtest: ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
ok 1266 - ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
  ---
  duration_ms: 0.837279
  ...
# Subtest: completion failure preserves cursor and landing and reports the Tasks failure
ok 1267 - completion failure preserves cursor and landing and reports the Tasks failure
  ---
  duration_ms: 0.423208
  ...
# Subtest: reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
ok 1268 - reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
  ---
  duration_ms: 1.275025
  ...
# Subtest: Alt+F on PRE stays with remaining PRE count and never stamps
ok 1269 - Alt+F on PRE stays with remaining PRE count and never stamps
  ---
  duration_ms: 5.027551
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a stale cache
ok 1270 - Ctrl+Alt+F completes seven PRE rows from a stale cache
  ---
  duration_ms: 10.753865
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a refreshed cache
ok 1271 - Ctrl+Alt+F completes seven PRE rows from a refreshed cache
  ---
  duration_ms: 4.061576
  ...
# Subtest: POST stays put with the closing notice
ok 1272 - POST stays put with the closing notice
  ---
  duration_ms: 0.749391
  ...
# Subtest: manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
ok 1273 - manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
  ---
  duration_ms: 1.008466
  ...
# Subtest: manual Ctrl+Enter then ]s from a stale cache uses text-first identity
ok 1274 - manual Ctrl+Enter then ]s from a stale cache uses text-first identity
  ---
  duration_ms: 0.759129
  ...
# Subtest: counted Alt+F skips checklist rows with the skip tail
ok 1275 - counted Alt+F skips checklist rows with the skip tail
  ---
  duration_ms: 2.492951
  ...
# Subtest: missing cycler gate on a PRE row writes nothing
ok 1276 - missing cycler gate on a PRE row writes nothing
  ---
  duration_ms: 0.512819
  ...
# Subtest: missing ledger checklist gate on a tagged line writes nothing
ok 1277 - missing ledger checklist gate on a tagged line writes nothing
  ---
  duration_ms: 0.52365
  ...
# Subtest: a tagged line that is not a queue match falls through to recurring refusal
ok 1278 - a tagged line that is not a queue match falls through to recurring refusal
  ---
  duration_ms: 0.341682
  ...
# Subtest: formatFreshStampChecklistSkipTail names the skipped count
ok 1279 - formatFreshStampChecklistSkipTail names the skipped count
  ---
  duration_ms: 0.112796
  ...
# Subtest: partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
ok 1280 - partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
  ---
  duration_ms: 0.237704
  ...
# Subtest: Task Link Alt+F skips a PRE target with the skip notice
ok 1281 - Task Link Alt+F skips a PRE target with the skip notice
  ---
  duration_ms: 1.863979
  ...
# Subtest: P0 at interval 7 enters P2 with a previewed decay date and kept tail
ok 1282 - P0 at interval 7 enters P2 with a previewed decay date and kept tail
  ---
  duration_ms: 3.694004
  ...
# Subtest: P0 at interval 30 enters P3
ok 1283 - P0 at interval 30 enters P3
  ---
  duration_ms: 0.487811
  ...
# Subtest: fixed enter overrides the interval scan
ok 1284 - fixed enter overrides the interval scan
  ---
  duration_ms: 0.451311
  ...
# Subtest: unknown enter disables Not now without disabling Keep/Reword
ok 1285 - unknown enter disables Not now without disabling Keep/Reword
  ---
  duration_ms: 0.415744
  ...
# Subtest: P0 with no suitable level stays unavailable and never shortens the lease
ok 1286 - P0 with no suitable level stays unavailable and never shortens the lease
  ---
  duration_ms: 0.354237
  ...
# Subtest: custom level order resolves entry in ladder order
ok 1287 - custom level order resolves entry in ladder order
  ---
  duration_ms: 0.297629
  ...
# Subtest: unknown priority value disables Not now only
ok 1288 - unknown priority value disables Not now only
  ---
  duration_ms: 0.336022
  ...
# Subtest: prioritized P2 below its roll limit stays on the same level
ok 1289 - prioritized P2 below its roll limit stays on the same level
  ---
  duration_ms: 0.584065
  ...
# Subtest: P2 at its roll limit decays to P3
ok 1290 - P2 at its roll limit decays to P3
  ---
  duration_ms: 0.689606
  ...
# Subtest: P2 streak derives from the task Schedule Log
ok 1291 - P2 streak derives from the task Schedule Log
  ---
  duration_ms: 2.837799
  ...
# Subtest: configured decay:false keeps rolling past the limit
ok 1292 - configured decay:false keeps rolling past the limit
  ---
  duration_ms: 0.337064
  ...
# Subtest: per-level rolls:0 decays immediately
ok 1293 - per-level rolls:0 decays immediately
  ---
  duration_ms: 0.254857
  ...
# Subtest: terminal cancel substitutes a truthful same-level card roll
ok 1294 - terminal cancel substitutes a truthful same-level card roll
  ---
  duration_ms: 0.298971
  ...
# Subtest: no future date in the window refuses Not now
ok 1295 - no future date in the window refuses Not now
  ---
  duration_ms: 0.198068
  ...
# Subtest: Less often steps 7/14/30 to the next preset with a decision reason
ok 1296 - Less often steps 7/14/30 to the next preset with a decision reason
  ---
  duration_ms: 0.474696
  ...
# Subtest: Less often at 90+ opens the constrained custom picker; 365 is unavailable
ok 1297 - Less often at 90+ opens the constrained custom picker; 365 is unavailable
  ---
  duration_ms: 0.341522
  ...
# Subtest: previewed dates are stable for one random draw
ok 1298 - previewed dates are stable for one random draw
  ---
  duration_ms: 0.321744
  ...
# Subtest: Keep saturates at 999 and Drop preserves keeps history
ok 1299 - Keep saturates at 999 and Drop preserves keeps history
  ---
  duration_ms: 0.378202
  ...
# Subtest: kept tails preserve roll classification; decisions break it deliberately
ok 1300 - kept tails preserve roll classification; decisions break it deliberately
  ---
  duration_ms: 0.84804
  ...
# Subtest: invalid priority config offers no priority-changing action
ok 1301 - invalid priority config offers no priority-changing action
  ---
  duration_ms: 0.285064
  ...
# Subtest: decay off disables Not now but keeps counting
ok 1302 - decay off disables Not now but keeps counting
  ---
  duration_ms: 0.212496
  ...
# Subtest: explicit level picks cover the ladder with previewed rolls
ok 1303 - explicit level picks cover the ladder with previewed rolls
  ---
  duration_ms: 0.74361
  ...
# Subtest: card model is deeply frozen
ok 1304 - card model is deeply frozen
  ---
  duration_ms: 0.17307
  ...
# Subtest: single Alt+F on an at-limit task opens the card and writes nothing
ok 1305 - single Alt+F on an at-limit task opens the card and writes nothing
  ---
  duration_ms: 11.759276
  ...
# Subtest: dismissing the card writes nothing and does not advance
ok 1306 - dismissing the card writes nothing and does not advance
  ---
  duration_ms: 1.894888
  ...
# Subtest: early dates open the card and write nothing
ok 1307 - early dates open the card and write nothing
  ---
  duration_ms: 1.528168
  ...
# Subtest: namespace v5 with decide true stamps counted and opens no card
ok 1308 - namespace v5 with decide true stamps counted and opens no card
  ---
  duration_ms: 5.537454
  ...
# Subtest: stale task-line change writes nothing
ok 1309 - stale task-line change writes nothing
  ---
  duration_ms: 1.328266
  ...
# Subtest: stale local-day change writes nothing
ok 1310 - stale local-day change writes nothing
  ---
  duration_ms: 1.290043
  ...
# Subtest: stale decay-config change writes nothing
ok 1311 - stale decay-config change writes nothing
  ---
  duration_ms: 1.380447
  ...
# Subtest: stale priority-ladder config writes nothing
ok 1312 - stale priority-ladder config writes nothing
  ---
  duration_ms: 2.076655
  ...
# Subtest: stale child Schedule Log writes nothing
ok 1313 - stale child Schedule Log writes nothing
  ---
  duration_ms: 2.28328
  ...
# Subtest: Not now stamps, clears keeps, and advances exactly once
ok 1314 - Not now stamps, clears keeps, and advances exactly once
  ---
  duration_ms: 6.051295
  ...
# Subtest: Keep counts once and saturates at 999 without reset
not ok 1315 - Keep counts once and saturates at 999 without reset
  ---
  duration_ms: 1.663456
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-navigation-decision-card-handlers.cjs:546:1'
  failureType: 'testCodeFailure'
  error: '- [ ] #task Buy milk [fresh:: 2026-09-30] [keeps:: 3]'
  code: 'ERR_ASSERTION'
  name: 'AssertionError'
  expected:
  actual: 'Update Bob Ledger Tools to record review stats'
  operator: 'match'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-navigation-decision-card-handlers.cjs:569:12)
    async Test.run (node:internal/test_runner/test:980:9)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Reword stamps, clears, logs, and never advances
ok 1316 - Reword stamps, clears, logs, and never advances
  ---
  duration_ms: 1.363264
  ...
# Subtest: Drop cancels with the dropped-after-keeps reason and keeps history
ok 1317 - Drop cancels with the dropped-after-keeps reason and keeps history
  ---
  duration_ms: 0.688204
  ...
# Subtest: Less often at 90+ opens the picker and dismiss writes nothing
ok 1318 - Less often at 90+ opens the picker and dismiss writes nothing
  ---
  duration_ms: 0.783506
  ...
# Subtest: counted session skips at-limit and counts below-limit
ok 1319 - counted session skips at-limit and counts below-limit
  ---
  duration_ms: 0.896852
  ...
# Subtest: counted session skips at-limit on an early date
ok 1320 - counted session skips at-limit on an early date
  ---
  duration_ms: 0.692953
  ...
# Subtest: counted session with every target skipped writes nothing
ok 1321 - counted session with every target skipped writes nothing
  ---
  duration_ms: 0.300043
  ...
# Subtest: availability: decay on (or absent) may ask; decay off never asks
ok 1322 - availability: decay on (or absent) may ask; decay off never asks
  ---
  duration_ms: 1.295463
  ...
# Subtest: trigger: only an explicit decide row decides
ok 1323 - trigger: only an explicit decide row decides
  ---
  duration_ms: 0.250728
  ...
# Subtest: partition: exact at-limit rows skip, everything else stamps
ok 1324 - partition: exact at-limit rows skip, everything else stamps
  ---
  duration_ms: 0.965874
  ...
# Subtest: partition: empty and malformed input stamps nothing and skips nothing
ok 1325 - partition: empty and malformed input stamps nothing and skips nothing
  ---
  duration_ms: 0.204381
  ...
# Subtest: partition: enabled false stamps decision rows (older namespace fallback)
ok 1326 - partition: enabled false stamps decision rows (older namespace fallback)
  ---
  duration_ms: 0.19916
  ...
# Subtest: skip wording: singular, plural, and all-skipped notices
ok 1327 - skip wording: singular, plural, and all-skipped notices
  ---
  duration_ms: 0.238285
  ...
# Subtest: reword cursor: lands at the end of the task body before metadata
ok 1328 - reword cursor: lands at the end of the task body before metadata
  ---
  duration_ms: 0.467964
  ...
# Subtest: captured age: optional context ages, null when created is missing
ok 1329 - captured age: optional context ages, null when created is missing
  ---
  duration_ms: 0.512309
  ...
# Subtest: rows: P0 entry shows the recommended Not now with a clean window
ok 1330 - rows: P0 entry shows the recommended Not now with a clean window
  ---
  duration_ms: 3.931107
  ...
# Subtest: rows: invalid priority config disables Not now and levels, keeps safe rows
ok 1331 - rows: invalid priority config disables Not now and levels, keeps safe rows
  ---
  duration_ms: 0.803665
  ...
# Subtest: rows: picker-mode Less often and 365-day cap
ok 1332 - rows: picker-mode Less often and 365-day cap
  ---
  duration_ms: 1.219609
  ...
# Subtest: rows: terminal ladder keeps Enter available and never cancels
ok 1333 - rows: terminal ladder keeps Enter available and never cancels
  ---
  duration_ms: 0.73323
  ...
# Subtest: modal: Enter approves once; later keys cannot approve again
ok 1334 - modal: Enter approves once; later keys cannot approve again
  ---
  duration_ms: 0.751264
  ...
# Subtest: modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
ok 1335 - modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
  ---
  duration_ms: 0.450741
  ...
# Subtest: modal: key repeat and modified keys never approve
ok 1336 - modal: key repeat and modified keys never approve
  ---
  duration_ms: 0.308639
  ...
# Subtest: modal: Esc changes nothing — dismiss without a choice
ok 1337 - modal: Esc changes nothing — dismiss without a choice
  ---
  duration_ms: 0.178521
  ...
# Subtest: modal: unavailable actions cannot be chosen
ok 1338 - modal: unavailable actions cannot be chosen
  ---
  duration_ms: 0.239317
  ...
# Subtest: modal: a double callback applies once
ok 1339 - modal: a double callback applies once
  ---
  duration_ms: 0.127233
  ...
# Subtest: capability: the nav api exposes the card while loaded
ok 1340 - capability: the nav api exposes the card while loaded
  ---
  duration_ms: 0.50831
  ...
# Subtest: capability: unload drops the card so marks stop promising it
ok 1341 - capability: unload drops the card so marks stop promising it
  ---
  duration_ms: 0.241602
  ...
# Subtest: ladder lookup: the first priority property wins, null without one
ok 1342 - ladder lookup: the first priority property wins, null without one
  ---
  duration_ms: 0.195403
  ...
# Subtest: stage entry resolves the line itself and refuses prose
ok 1343 - stage entry resolves the line itself and refuses prose
  ---
  duration_ms: 4.150366
  ...
# Subtest: Ctrl+Shift+P on a BLOCKS line opens the owner's Blocks stage directly
ok 1344 - Ctrl+Shift+P on a BLOCKS line opens the owner's Blocks stage directly
  ---
  duration_ms: 1.823872
  ...
# Subtest: Ctrl+Shift+P hotkey path on a BLOCKS line opens the owner's Blocks stage directly
ok 1345 - Ctrl+Shift+P hotkey path on a BLOCKS line opens the owner's Blocks stage directly
  ---
  duration_ms: 0.890129
  ...
# Subtest: Ctrl+Shift+Alt+B on a BLOCKS or Depends-On line opens the owner's Blocks stage
ok 1346 - Ctrl+Shift+Alt+B on a BLOCKS or Depends-On line opens the owner's Blocks stage
  ---
  duration_ms: 0.593353
  ...
# Subtest: Ctrl+Shift+P on a Depends-On line is unchanged forward behavior
ok 1347 - Ctrl+Shift+P on a Depends-On line is unchanged forward behavior
  ---
  duration_ms: 0.487952
  ...
# Subtest: Ctrl+Shift+P on a plain child bullet and a nested Task Link are unchanged (3e359a6)
ok 1348 - Ctrl+Shift+P on a plain child bullet and a nested Task Link are unchanged (3e359a6)
  ---
  duration_ms: 8.689165
  ...
# Subtest: forward counted mixed row in BLOCKED keeps the waits-on badge (3e359a6 order)
ok 1349 - forward counted mixed row in BLOCKED keeps the waits-on badge (3e359a6 order)
  ---
  duration_ms: 3.142792
  ...
# Subtest: api.blocks opens the stage and removes only a listed dependent
ok 1350 - api.blocks opens the stage and removes only a listed dependent
  ---
  duration_ms: 1.926819
  ...
# Subtest: api.blocks removeDependent on an owner with no ^id is not-a-dependent
ok 1351 - api.blocks removeDependent on an owner with no ^id is not-a-dependent
  ---
  duration_ms: 0.632128
  ...
# Subtest: stage canonical order ranks \#hide last ahead of the lane
ok 1352 - stage canonical order ranks \#hide last ahead of the lane
  ---
  duration_ms: 0.580518
  ...
# Subtest: stage empty query shows same-note plus In Progress and Next only
ok 1353 - stage empty query shows same-note plus In Progress and Next only
  ---
  duration_ms: 2.527867
  ...
# Subtest: stage cap appends a type-to-search-more hint row
ok 1354 - stage cap appends a type-to-search-more hint row
  ---
  duration_ms: 2.89113
  ...
# Subtest: stage BLOCKED rows carry waits-on counts and short guard reasons
ok 1355 - stage BLOCKED rows carry waits-on counts and short guard reasons
  ---
  duration_ms: 1.506536
  ...
# Subtest: stage removal notices name the task description, not the block id
ok 1356 - stage removal notices name the task description, not the block id
  ---
  duration_ms: 0.520674
  ...
# Subtest: stage Task Link batches keep Depends on without refusal
ok 1357 - stage Task Link batches keep Depends on without refusal
  ---
  duration_ms: 0.42912
  ...
# Subtest: stage batch cycle check runs on the post-batch graph
ok 1358 - stage batch cycle check runs on the post-batch graph
  ---
  duration_ms: 0.483473
  ...
# Subtest: stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
ok 1359 - stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
  ---
  duration_ms: 10.848516
  ...
# Subtest: stage stale single add refuses and reopens
ok 1360 - stage stale single add refuses and reopens
  ---
  duration_ms: 1.229348
  ...
# Subtest: Task Link Depends on focuses a linked note open in a background tab
ok 1361 - Task Link Depends on focuses a linked note open in a background tab
  ---
  duration_ms: 0.358655
  ...
# Subtest: Task Link Blocks focuses the linked note and opens Blocks directly
ok 1362 - Task Link Blocks focuses the linked note and opens Blocks directly
  ---
  duration_ms: 0.341231
  ...
# Subtest: Task Link Depends on refuses clearly when the linked note cannot be focused
    # Subtest: focus reports success but the active view stays elsewhere
    ok 1 - focus reports success but the active view stays elsewhere
      ---
      duration_ms: 0.234708
      ...
    # Subtest: focus reports failure
    ok 2 - focus reports failure
      ---
      duration_ms: 0.147421
      ...
    1..2
ok 1363 - Task Link Depends on refuses clearly when the linked note cannot be focused
  ---
  duration_ms: 0.710968
  ...
# Subtest: stage mirror burst keeps the baseline owner across an insertion above
ok 1364 - stage mirror burst keeps the baseline owner across an insertion above
  ---
  duration_ms: 1003.594643
  ...
# Subtest: stage mirror burst clears on a text-only line deletion
ok 1365 - stage mirror burst clears on a text-only line deletion
  ---
  duration_ms: 1001.192957
  ...
# Subtest: stage mirror vim dd clears the deleted line's owner
ok 1366 - stage mirror vim dd clears the deleted line's owner
  ---
  duration_ms: 1001.671808
  ...
# Subtest: stage badge counts open prerequisites without a block id
ok 1367 - stage badge counts open prerequisites without a block id
  ---
  duration_ms: 7.511153
  ...
# Subtest: stage badge names the future scheduled date with no open prerequisite
ok 1368 - stage badge names the future scheduled date with no open prerequisite
  ---
  duration_ms: 2.410533
  ...
# Subtest: stage badge reads blocked with nothing waiting and no schedule
ok 1369 - stage badge reads blocked with nothing waiting and no schedule
  ---
  duration_ms: 1.523159
  ...
# Subtest: stage vault batch with a stale row refuses and reopens
ok 1370 - stage vault batch with a stale row refuses and reopens
  ---
  duration_ms: 11.013171
  ...
# Subtest: stage opening builds 200/400/1000-task notes without cubic growth
ok 1371 - stage opening builds 200/400/1000-task notes without cubic growth
  ---
  duration_ms: 35.879456
  ...
# Subtest: stage snapshots match standalone parsing across grammar vectors
ok 1372 - stage snapshots match standalone parsing across grammar vectors
  ---
  duration_ms: 4.704463
  ...
# Subtest: stage Warm-empty cache is ready without a vault fallback
ok 1373 - stage Warm-empty cache is ready without a vault fallback
  ---
  duration_ms: 0.504794
  ...
# Subtest: stage opening renders cross-note results with zero writes and cap
ok 1374 - stage opening renders cross-note results with zero writes and cap
  ---
  duration_ms: 39.51165
  ...
# Subtest: stage CURRENT covers same-note, cross-note, blocked, and counted parents
ok 1375 - stage CURRENT covers same-note, cross-note, blocked, and counted parents
  ---
  duration_ms: 1.564348
  ...
# Subtest: stage collections reuse one snapshot per parent
ok 1376 - stage collections reuse one snapshot per parent
  ---
  duration_ms: 0.353565
  ...
# Subtest: stage cold refresh yields, preserves state, and performs no search reads
ok 1377 - stage cold refresh yields, preserves state, and performs no search reads
  ---
  duration_ms: 114.99581
  ...
# Subtest: stage cold refresh abandons after dismissal or replacement
ok 1378 - stage cold refresh abandons after dismissal or replacement
  ---
  duration_ms: 53.335609
  ...
# Subtest: stage 400-task opening finishes in a child process before the parent timeout
ok 1379 - stage 400-task opening finishes in a child process before the parent timeout
  ---
  duration_ms: 86.091531
  ...
# Subtest: stage ranker passes the DK contract vectors verbatim
ok 1380 - stage ranker passes the DK contract vectors verbatim
  ---
  duration_ms: 3.35685
  ...
# Subtest: stage ranker tiers match the capture ranker tier order
ok 1381 - stage ranker tiers match the capture ranker tier order
  ---
  duration_ms: 0.483444
  ...
# Subtest: stage pool excludes daily notes, done, templates, and dot-dirs
ok 1382 - stage pool excludes daily notes, done, templates, and dot-dirs
  ---
  duration_ms: 0.443947
  ...
# Subtest: stage pool collects open vault tasks with buffers as given
ok 1383 - stage pool collects open vault tasks with buffers as given
  ---
  duration_ms: 3.063101
  ...
# Subtest: stage CURRENT resolves same-note, missing, closed, and non-task targets
ok 1384 - stage CURRENT resolves same-note, missing, closed, and non-task targets
  ---
  duration_ms: 2.820517
  ...
# Subtest: stage cycle guard reports the path back to the dependent
ok 1385 - stage cycle guard reports the path back to the dependent
  ---
  duration_ms: 0.993177
  ...
# Subtest: stage view groups CURRENT, RESULTS, and BLOCKED with guards
ok 1386 - stage view groups CURRENT, RESULTS, and BLOCKED with guards
  ---
  duration_ms: 2.812731
  ...
# Subtest: stage view disables cycles and unencodable targets, keeps +id rows
ok 1387 - stage view disables cycles and unencodable targets, keeps +id rows
  ---
  duration_ms: 1.04733
  ...
# Subtest: stage cache tasks normalize across Tasks shapes, buffers win
ok 1388 - stage cache tasks normalize across Tasks shapes, buffers win
  ---
  duration_ms: 0.740855
  ...
# Subtest: stage Task Link mode shows Depends on for one link and batches
ok 1389 - stage Task Link mode shows Depends on for one link and batches
  ---
  duration_ms: 0.869811
  ...
# Subtest: stage mark keys never collide across notes
ok 1390 - stage mark keys never collide across notes
  ---
  duration_ms: 0.260918
  ...
# Subtest: stage display-text locating matches one open task
ok 1391 - stage display-text locating matches one open task
  ---
  duration_ms: 0.348305
  ...
# Subtest: stage selection refusal spans tasks only
ok 1392 - stage selection refusal spans tasks only
  ---
  duration_ms: 0.411045
  ...
# Subtest: stage builder composes pool, current, guards, and pill title
ok 1393 - stage builder composes pool, current, guards, and pill title
  ---
  duration_ms: 2.437795
  ...
# Subtest: stage counted vault add with a stale target refuses and reopens
ok 1394 - stage counted vault add with a stale target refuses and reopens
  ---
  duration_ms: 9.025035
  ...
# Subtest: stage vault commit with a stale write notifies once and reopens
ok 1395 - stage vault commit with a stale write notifies once and reopens
  ---
  duration_ms: 7.32464
  ...
# Subtest: commitVaultRefs refuses a cycle through implicit resident edges
ok 1396 - commitVaultRefs refuses a cycle through implicit resident edges
  ---
  duration_ms: 1.608502
  ...
# Subtest: stage single remove with a stale write notifies once and reopens
ok 1397 - stage single remove with a stale write notifies once and reopens
  ---
  duration_ms: 2.644209
  ...
# Subtest: stage vault single +id guard refuses a stale target
ok 1398 - stage vault single +id guard refuses a stale target
  ---
  duration_ms: 1.241331
  ...
# Subtest: stage vault counted +id guard refuses a stale target
ok 1399 - stage vault counted +id guard refuses a stale target
  ---
  duration_ms: 0.934655
  ...
# Subtest: stage single +id guard refuses a stale target
ok 1400 - stage single +id guard refuses a stale target
  ---
  duration_ms: 1.124928
  ...
# Subtest: stage counted remove with a stale write refuses and reopens
ok 1401 - stage counted remove with a stale write refuses and reopens
  ---
  duration_ms: 3.218015
  ...
# Subtest: stage counted remove counts only changed sources
ok 1402 - stage counted remove counts only changed sources
  ---
  duration_ms: 4.090401
  ...
# Subtest: counted local add on [?] sources reads zero extra notes
ok 1403 - counted local add on [?] sources reads zero extra notes
  ---
  duration_ms: 5.265235
  ...
# Subtest: counted local toggle-off on a Pomodoro-linked [?] source recovers
ok 1404 - counted local toggle-off on a Pomodoro-linked [?] source recovers
  ---
  duration_ms: 4.490595
  ...
# Subtest: stage counted vault add counts only changed sources
ok 1405 - stage counted vault add counts only changed sources
  ---
  duration_ms: 1.834884
  ...
# Subtest: stage counted vault remove counts only changed sources
ok 1406 - stage counted vault remove counts only changed sources
  ---
  duration_ms: 1.273411
  ...
# Subtest: stage +id row prompts without writing
ok 1407 - stage +id row prompts without writing
  ---
  duration_ms: 11.096339
  ...
# Subtest: stage dismissal writes no bytes and drops the batch
ok 1408 - stage dismissal writes no bytes and drops the batch
  ---
  duration_ms: 1.490867
  ...
# Subtest: stage same-note batch commits in one undo group
ok 1409 - stage same-note batch commits in one undo group
  ---
  duration_ms: 11.862201
  ...
# Subtest: stage batch with a stale row refuses and reopens
ok 1410 - stage batch with a stale row refuses and reopens
  ---
  duration_ms: 0.925086
  ...
# Subtest: stage counted add applies to every source task
ok 1411 - stage counted add applies to every source task
  ---
  duration_ms: 35.246866
  ...
# Subtest: stage batch cycle rows stay guarded and write nothing
ok 1412 - stage batch cycle rows stay guarded and write nothing
  ---
  duration_ms: 28.73741
  ...
# Subtest: stage edit-task-dependencies registers with no default hotkey
ok 1413 - stage edit-task-dependencies registers with no default hotkey
  ---
  duration_ms: 1.554128
  ...
# Subtest: task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row
ok 1414 - task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row
  ---
  duration_ms: 0.938612
  ...
# Subtest: task-card-blocks registers Ctrl+Shift+Alt+B and opens the Blocks row
ok 1415 - task-card-blocks registers Ctrl+Shift+Alt+B and opens the Blocks row
  ---
  duration_ms: 0.715837
  ...
# Subtest: stage waits-on badge counts open prerequisites only
ok 1416 - stage waits-on badge counts open prerequisites only
  ---
  duration_ms: 2.379294
  ...
# Subtest: stage cycle tooltip shows task descriptions
ok 1417 - stage cycle tooltip shows task descriptions
  ---
  duration_ms: 1.540592
  ...
# Subtest: stage same-note single add stamps the dependent and keeps its cursor
ok 1418 - stage same-note single add stamps the dependent and keeps its cursor
  ---
  duration_ms: 7.16924
  ...
# Subtest: stage same-note marked batch stamps the dependent and keeps its cursor
ok 1419 - stage same-note marked batch stamps the dependent and keeps its cursor
  ---
  duration_ms: 5.191213
  ...
# Subtest: Tab marks a same-note CURRENT row and Enter removes it
ok 1420 - Tab marks a same-note CURRENT row and Enter removes it
  ---
  duration_ms: 31.883614
  ...
# Subtest: Tab twice unmarks a CURRENT row
ok 1421 - Tab twice unmarks a CURRENT row
  ---
  duration_ms: 26.810167
  ...
# Subtest: Tab mixed CURRENT removal and RESULTS add apply in one commit
ok 1422 - Tab mixed CURRENT removal and RESULTS add apply in one commit
  ---
  duration_ms: 30.04775
  ...
# Subtest: Tab marks a missing CURRENT target and the batch removes it
ok 1423 - Tab marks a missing CURRENT target and the batch removes it
  ---
  duration_ms: 30.431992
  ...
# Subtest: Tab same-note and cross-note CURRENT removals apply in one vault batch
ok 1424 - Tab same-note and cross-note CURRENT removals apply in one vault batch
  ---
  duration_ms: 30.931927
  ...
# Subtest: cross-note add awaits preparation before the one commit
ok 1425 - cross-note add awaits preparation before the one commit
  ---
  duration_ms: 23.841047
  ...
# Subtest: a failed async preparation leaves the dependent untouched
ok 1426 - a failed async preparation leaves the dependent untouched
  ---
  duration_ms: 7.541431
  ...
# Subtest: links to unloaded notes tolerate add, remove, and deleted targets
ok 1427 - links to unloaded notes tolerate add, remove, and deleted targets
  ---
  duration_ms: 5.073789
  ...
# Subtest: Pomodoro-linked dependents recover through the plugin vault read
ok 1428 - Pomodoro-linked dependents recover through the plugin vault read
  ---
  duration_ms: 6.889165
  ...
# Subtest: same-note batch +id stamps the target and links in one undo group
ok 1429 - same-note batch +id stamps the target and links in one undo group
  ---
  duration_ms: 8.115136
  ...
# Subtest: confirmBatchBlockId collects the id and executes the batch
ok 1430 - confirmBatchBlockId collects the id and executes the batch
  ---
  duration_ms: 2.476619
  ...
# Subtest: commitMarkedDependencies executes ready additions at once
ok 1431 - commitMarkedDependencies executes ready additions at once
  ---
  duration_ms: 2.404552
  ...
# Subtest: counted vault add links two siblings bottom-up
ok 1432 - counted vault add links two siblings bottom-up
  ---
  duration_ms: 4.245196
  ...
# Subtest: counted CURRENT rows without a line remove from every source
ok 1433 - counted CURRENT rows without a line remove from every source
  ---
  duration_ms: 6.863617
  ...
# Subtest: a stale editor between await and commit refuses
ok 1434 - a stale editor between await and commit refuses
  ---
  duration_ms: 1.257331
  ...
# Subtest: removeDependencyByRef refuses targets that are not on the line
ok 1435 - removeDependencyByRef refuses targets that are not on the line
  ---
  duration_ms: 1.20987
  ...
# Subtest: kept unloaded links resolve the field id by line position
ok 1436 - kept unloaded links resolve the field id by line position
  ---
  duration_ms: 2.197467
  ...
# Subtest: pendingTargetLine commits the same-note target id with the link
ok 1437 - pendingTargetLine commits the same-note target id with the link
  ---
  duration_ms: 2.444108
  ...
# Subtest: counted vault add commits every source in one transaction
ok 1438 - counted vault add commits every source in one transaction
  ---
  duration_ms: 2.656254
  ...
# Subtest: field-only clears snapshot the vault and recover
ok 1439 - field-only clears snapshot the vault and recover
  ---
  duration_ms: 1.444759
  ...
# Subtest: adds without recovery read zero extra vault notes
ok 1440 - adds without recovery read zero extra vault notes
  ---
  duration_ms: 0.711709
  ...
# Subtest: hand-edit clear recovers Pomodoro-linked dependents to Next
ok 1441 - hand-edit clear recovers Pomodoro-linked dependents to Next
  ---
  duration_ms: 0.961806
  ...
# Subtest: hand-edit clear on a non-Blocked parent reads zero extra notes
ok 1442 - hand-edit clear on a non-Blocked parent reads zero extra notes
  ---
  duration_ms: 0.42448
  ...
# Subtest: writer keeps the full route for duplicate basenames
ok 1443 - writer keeps the full route for duplicate basenames
  ---
  duration_ms: 0.741145
  ...
# Subtest: adds on Blocked parents and non-Blocked mirror touches read nothing
ok 1444 - adds on Blocked parents and non-Blocked mirror touches read nothing
  ---
  duration_ms: 0.930156
  ...
# Subtest: counted vault add loads each source's existing links
ok 1445 - counted vault add loads each source's existing links
  ---
  duration_ms: 2.989208
  ...
# Subtest: counted Ctrl+D on a blockquoted task refuses with the blockquote notice
ok 1446 - counted Ctrl+D on a blockquoted task refuses with the blockquote notice
  ---
  duration_ms: 0.601208
  ...
# Subtest: single Ctrl+D on a quoted task without a field refuses as a blockquote
ok 1447 - single Ctrl+D on a quoted task without a field refuses as a blockquote
  ---
  duration_ms: 0.195403
  ...
# Subtest: confirmSingleBlockId folds the target id into one transaction
ok 1448 - confirmSingleBlockId folds the target id into one transaction
  ---
  duration_ms: 2.700506
  ...
# Subtest: chooseTaskDependency folds a missing target id into one transaction
ok 1449 - chooseTaskDependency folds a missing target id into one transaction
  ---
  duration_ms: 1.618711
  ...
# Subtest: counted remove commits every source in one transaction
ok 1450 - counted remove commits every source in one transaction
  ---
  duration_ms: 3.061245
  ...
# Subtest: DP parse vectors accept, empty, malformed, and not-a-line
ok 1451 - DP parse vectors accept, empty, malformed, and not-a-line
  ---
  duration_ms: 2.602421
  ...
# Subtest: DP30 attributes a Work-Log-nested Depends-On line to the inner task
ok 1452 - DP30 attributes a Work-Log-nested Depends-On line to the inner task
  ---
  duration_ms: 2.037211
  ...
# Subtest: fenced lines never collect as Depends-On lines
ok 1453 - fenced lines never collect as Depends-On lines
  ---
  duration_ms: 0.340921
  ...
# Subtest: DW1 creates the line as the first child
ok 1454 - DW1 creates the line as the first child
  ---
  duration_ms: 4.451019
  ...
# Subtest: DW2 creates the line after a Cancel Log
ok 1455 - DW2 creates the line after a Cancel Log
  ---
  duration_ms: 1.049174
  ...
# Subtest: DW3-DW5 append, remove the middle, and delete on the last link
ok 1456 - DW3-DW5 append, remove the middle, and delete on the last link
  ---
  duration_ms: 4.32591
  ...
# Subtest: DW6-DW7 re-add moves to the end and the field mirrors the line
ok 1457 - DW6-DW7 re-add moves to the end and the field mirrors the line
  ---
  duration_ms: 0.589145
  ...
# Subtest: DW8 tab parents deepen the child by one tab
ok 1458 - DW8 tab parents deepen the child by one tab
  ---
  duration_ms: 1.092797
  ...
# Subtest: DW9 space parents reuse the existing child indent
ok 1459 - DW9 space parents reuse the existing child indent
  ---
  duration_ms: 0.821789
  ...
# Subtest: DW10-DW11 CRLF and final-newline state survive
ok 1460 - DW10-DW11 CRLF and final-newline state survive
  ---
  duration_ms: 0.917532
  ...
# Subtest: DW12-DW14 link form is the shortest unambiguous form
ok 1461 - DW12-DW14 link form is the shortest unambiguous form
  ---
  duration_ms: 0.276147
  ...
# Subtest: archive targets keep the explicit done/ path form
ok 1462 - archive targets keep the explicit done/ path form
  ---
  duration_ms: 0.190985
  ...
# Subtest: DW15 an existing id is never rewritten
ok 1463 - DW15 an existing id is never rewritten
  ---
  duration_ms: 0.341713
  ...
# Subtest: DW16 an unencodable path without an id refuses
ok 1464 - DW16 an unencodable path without an id refuses
  ---
  duration_ms: 0.250148
  ...
# Subtest: DW17 field placement follows fresh and precedes the block id
ok 1465 - DW17 field placement follows fresh and precedes the block id
  ---
  duration_ms: 0.2879
  ...
# Subtest: DW18 legacy children fold into the line
ok 1466 - DW18 legacy children fold into the line
  ---
  duration_ms: 0.705467
  ...
# Subtest: DW19 variants canonicalise to the writer form
ok 1467 - DW19 variants canonicalise to the writer form
  ---
  duration_ms: 1.236291
  ...
# Subtest: adding an open prerequisite blocks the dependent
ok 1468 - adding an open prerequisite blocks the dependent
  ---
  duration_ms: 0.308339
  ...
# Subtest: adding transfers Next and In Progress commitment to the open target
ok 1469 - adding transfers Next and In Progress commitment to the open target
  ---
  duration_ms: 0.498652
  ...
# Subtest: removing the last open prerequisite recovers immediately
ok 1470 - removing the last open prerequisite recovers immediately
  ---
  duration_ms: 0.642597
  ...
# Subtest: removal stays Blocked while another prerequisite is open
ok 1471 - removal stays Blocked while another prerequisite is open
  ---
  duration_ms: 0.309982
  ...
# Subtest: removal stays Blocked with a future schedule
ok 1472 - removal stays Blocked with a future schedule
  ---
  duration_ms: 0.379234
  ...
# Subtest: one gesture commits the dependent note in a single transaction
ok 1473 - one gesture commits the dependent note in a single transaction
  ---
  duration_ms: 1.495756
  ...
# Subtest: a failed preparation leaves the dependent untouched
ok 1474 - a failed preparation leaves the dependent untouched
  ---
  duration_ms: 0.370317
  ...
# Subtest: recovery references follow the line plus covered legacy children
ok 1475 - recovery references follow the line plus covered legacy children
  ---
  duration_ms: 0.424781
  ...
# Subtest: task-block helpers find owners, lines, and insertion points
ok 1476 - task-block helpers find owners, lines, and insertion points
  ---
  duration_ms: 0.311696
  ...
# Subtest: dependency notices follow the contract shapes
ok 1477 - dependency notices follow the contract shapes
  ---
  duration_ms: 0.133174
  ...
# Subtest: nav api v3 resolves results and never throws
ok 1478 - nav api v3 resolves results and never throws
  ---
  duration_ms: 1.08934
  ...
# Subtest: getDependencyInsertLine lands after a Cancel Log subtree
ok 1479 - getDependencyInsertLine lands after a Cancel Log subtree
  ---
  duration_ms: 0.221664
  ...
# Subtest: planner: an ordinary dependent with a block id plus an open add yields one target
ok 1480 - planner: an ordinary dependent with a block id plus an open add yields one target
  ---
  duration_ms: 6.747915
  ...
# Subtest: planner: adding only a closed target yields none
ok 1481 - planner: adding only a closed target yields none
  ---
  duration_ms: 0.76981
  ...
# Subtest: planner: no block id yields none
ok 1482 - planner: no block id yields none
  ---
  duration_ms: 0.454347
  ...
# Subtest: planner: a dependent already [?] with an open add yields a target
ok 1483 - planner: a dependent already [?] with an open add yields a target
  ---
  duration_ms: 1.604935
  ...
# Subtest: planner: a removal yields none
ok 1484 - planner: a removal yields none
  ---
  duration_ms: 1.02634
  ...
# Subtest: planner: mirrorTouch emits no ordinary consumption target
ok 1485 - planner: mirrorTouch emits no ordinary consumption target
  ---
  duration_ms: 0.429921
  ...
# Subtest: planner: ^prj keeps project targets and a deduplicated union
ok 1486 - planner: ^prj keeps project targets and a deduplicated union
  ---
  duration_ms: 2.522898
  ...
# Subtest: suffix helper names the removed count and the failed follow-up
ok 1487 - suffix helper names the removed count and the failed follow-up
  ---
  duration_ms: 0.21424
  ...
# Subtest: applyDependencyEdit cross-file consumes live links and emptied entries
ok 1488 - applyDependencyEdit cross-file consumes live links and emptied entries
  ---
  duration_ms: 9.775457
  ...
# Subtest: applyDependencyEdit removes one live link and reports it
ok 1489 - applyDependencyEdit removes one live link and reports it
  ---
  duration_ms: 2.475738
  ...
# Subtest: applyDependencyEdit keeps the dependent write when the daily preimage changes
ok 1490 - applyDependencyEdit keeps the dependent write when the daily preimage changes
  ---
  duration_ms: 1.71773
  ...
# Subtest: same-file fold lands the dependency and the cleanup in one undo group
ok 1491 - same-file fold lands the dependency and the cleanup in one undo group
  ---
  duration_ms: 2.208608
  ...
# Subtest: setLocalTaskDependencyLink stays synchronous and folds same-file cleanup
ok 1492 - setLocalTaskDependencyLink stays synchronous and folds same-file cleanup
  ---
  duration_ms: 2.85899
  ...
# Subtest: setLocalTaskDependencyLink cross-file continuation removes the live link
ok 1493 - setLocalTaskDependencyLink cross-file continuation removes the live link
  ---
  duration_ms: 12.93461
  ...
# Subtest: same-note marked batch consumes every newly Blocked source
ok 1494 - same-note marked batch consumes every newly Blocked source
  ---
  duration_ms: 7.649147
  ...
# Subtest: counted same-note writer consumes every newly Blocked source
ok 1495 - counted same-note writer consumes every newly Blocked source
  ---
  duration_ms: 4.074591
  ...
# Subtest: counted vault writer consumes every newly Blocked source
ok 1496 - counted vault writer consumes every newly Blocked source
  ---
  duration_ms: 3.281146
  ...
# Subtest: counted ^prj source consumes its project targets
ok 1497 - counted ^prj source consumes its project targets
  ---
  duration_ms: 3.384693
  ...
# Subtest: a dependent without a block id does zero cachedReads even when today's daily exists
ok 1498 - a dependent without a block id does zero cachedReads even when today's daily exists
  ---
  duration_ms: 1.428808
  ...
# Subtest: alignment key ignores fields, the block id, the status and trailing space
ok 1499 - alignment key ignores fields, the block id, the status and trailing space
  ---
  duration_ms: 1.643869
  ...
# Subtest: insertion after a modified line edits that line and inserts after it
ok 1500 - insertion after a modified line edits that line and inserts after it
  ---
  duration_ms: 1.903434
  ...
# Subtest: adjacent prerequisite and parent both change while two lines insert
ok 1501 - adjacent prerequisite and parent both change while two lines insert
  ---
  duration_ms: 0.72312
  ...
# Subtest: deletion at the end of the document
ok 1502 - deletion at the end of the document
  ---
  duration_ms: 0.602069
  ...
# Subtest: insertion at the top and at the end of the document
ok 1503 - insertion at the top and at the end of the document
  ---
  duration_ms: 0.591309
  ...
# Subtest: empty documents align and apply
ok 1504 - empty documents align and apply
  ---
  duration_ms: 0.32498
  ...
# Subtest: CRLF documents insert and delete with CRLF
ok 1505 - CRLF documents insert and delete with CRLF
  ---
  duration_ms: 0.377241
  ...
# Subtest: equal-count shifted edits take the aligned path
ok 1506 - equal-count shifted edits take the aligned path
  ---
  duration_ms: 0.791622
  ...
# Subtest: pure in-place edits keep the line-bounded change shapes
ok 1507 - pure in-place edits keep the line-bounded change shapes
  ---
  duration_ms: 0.978669
  ...
# Subtest: an unchanged document writes nothing
ok 1508 - an unchanged document writes nothing
  ---
  duration_ms: 0.488403
  ...
# Subtest: an explicit final cursor wins over the mapped cursor
ok 1509 - an explicit final cursor wins over the mapped cursor
  ---
  duration_ms: 0.36673
  ...
# Subtest: the machine-write annotation still reaches the transaction
ok 1510 - the machine-write annotation still reaches the transaction
  ---
  duration_ms: 0.235801
  ...
# Subtest: an editor without transaction falls back to bottom-up replaceRange
ok 1511 - an editor without transaction falls back to bottom-up replaceRange
  ---
  duration_ms: 0.336844
  ...
# Subtest: positions map through aligned, changed, gap and deleted lines
ok 1512 - positions map through aligned, changed, gap and deleted lines
  ---
  duration_ms: 0.435552
  ...
# Subtest: a deletion at the end of the document maps to the last line
ok 1513 - a deletion at the end of the document maps to the last line
  ---
  duration_ms: 0.13084
  ...
# Subtest: a gap with new lines maps by offset and clamps to its last line
ok 1514 - a gap with new lines maps by offset and clamps to its last line
  ---
  duration_ms: 0.193379
  ...
# Subtest: seeded property: planned changes rebuild the new text and map unchanged lines
ok 1515 - seeded property: planned changes rebuild the new text and map unchanged lines
  ---
  duration_ms: 43.905962
  ...
# Subtest: a diff past the edit cap becomes one unaligned gap
ok 1516 - a diff past the edit cap becomes one unaligned gap
  ---
  duration_ms: 80.213277
  ...
# Subtest: the CM6 double reproduces the whole-document replacement jump
ok 1517 - the CM6 double reproduces the whole-document replacement jump
  ---
  duration_ms: 0.590017
  ...
# Subtest: first cross-note prerequisite keeps the cursor and the viewport
ok 1518 - first cross-note prerequisite keeps the cursor and the viewport
  ---
  duration_ms: 5.341921
  ...
# Subtest: same-note prerequisite directly above keeps the dependent's line
ok 1519 - same-note prerequisite directly above keeps the dependent's line
  ---
  duration_ms: 4.109949
  ...
# Subtest: removing the last prerequisite keeps the dependent's line
ok 1520 - removing the last prerequisite keeps the dependent's line
  ---
  duration_ms: 4.941456
  ...
# Subtest: a Blocks source gaining its first BLOCKS line keeps its line
ok 1521 - a Blocks source gaining its first BLOCKS line keeps its line
  ---
  duration_ms: 0.427887
  ...
# Subtest: missing ledger-tools api refuses the review namespace
ok 1522 - missing ledger-tools api refuses the review namespace
  ---
  duration_ms: 1.388211
  ...
# Subtest: review jump on an empty queue
ok 1523 - review jump on an empty queue
  ---
  duration_ms: 0.810759
  ...
# Subtest: review jump from a queued task goes to the neighbor
ok 1524 - review jump from a queued task goes to the neighbor
  ---
  duration_ms: 0.608652
  ...
# Subtest: review jump wraps at the ends
ok 1525 - review jump wraps at the ends
  ---
  duration_ms: 0.245509
  ...
# Subtest: review jump from elsewhere goes to the first or last entry
ok 1526 - review jump from elsewhere goes to the first or last entry
  ---
  duration_ms: 0.181116
  ...
# Subtest: review jump matches a moved cursor task by text
ok 1527 - review jump matches a moved cursor task by text
  ---
  duration_ms: 0.141981
  ...
# Subtest: review jump from a just-stamped rank goes to the entry after it
ok 1528 - review jump from a just-stamped rank goes to the entry after it
  ---
  duration_ms: 0.277891
  ...
# Subtest: review jump skips just-stamped keys the lagging cache still shows
ok 1529 - review jump skips just-stamped keys the lagging cache still shows
  ---
  duration_ms: 0.188941
  ...
# Subtest: review jump after stamping everything reports empty or wraps
ok 1530 - review jump after stamping everything reports empty or wraps
  ---
  duration_ms: 0.631436
  ...
# Subtest: review queue line resolves at the entry line
ok 1531 - review queue line resolves at the entry line
  ---
  duration_ms: 0.547966
  ...
# Subtest: review queue line follows a moved line to its unique match
ok 1532 - review queue line follows a moved line to its unique match
  ---
  duration_ms: 0.378152
  ...
# Subtest: review queue line goes stale on duplicates or a missing line
ok 1533 - review queue line goes stale on duplicates or a missing line
  ---
  duration_ms: 0.203178
  ...
# Subtest: review jump notices name the state
ok 1534 - review jump notices name the state
  ---
  duration_ms: 0.395606
  ...
# Subtest: fresh stamp targets refuse closed and recurring tasks
ok 1535 - fresh stamp targets refuse closed and recurring tasks
  ---
  duration_ms: 0.70687
  ...
# Subtest: fresh stamp batch stamps every target and nothing else
ok 1536 - fresh stamp batch stamps every target and nothing else
  ---
  duration_ms: 0.305343
  ...
# Subtest: one refusal refuses the whole fresh stamp batch
ok 1537 - one refusal refuses the whole fresh stamp batch
  ---
  duration_ms: 0.270747
  ...
# Subtest: a throwing stamper refuses the fresh stamp batch
ok 1538 - a throwing stamper refuses the fresh stamp batch
  ---
  duration_ms: 0.140819
  ...
# Subtest: fresh stamp plus Work Log prepends only stamped Pending targets
ok 1539 - fresh stamp plus Work Log prepends only stamped Pending targets
  ---
  duration_ms: 1.222885
  ...
# Subtest: blank Work Log summary and stamp refusal never create a log marker
ok 1540 - blank Work Log summary and stamp refusal never create a log marker
  ---
  duration_ms: 0.302307
  ...
# Subtest: fresh stamp notices adjust the pre-write counts
ok 1541 - fresh stamp notices adjust the pre-write counts
  ---
  duration_ms: 0.271459
  ...
# Subtest: today detection only matches today's fresh field
ok 1542 - today detection only matches today's fresh field
  ---
  duration_ms: 0.22505
  ...
# Subtest: stamped refs match the pre-write queue by line or text
ok 1543 - stamped refs match the pre-write queue by line or text
  ---
  duration_ms: 0.352804
  ...
# Subtest: review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
ok 1544 - review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
  ---
  duration_ms: 0.23049
  ...
# Subtest: tier-aware jump notices name each tier
ok 1545 - tier-aware jump notices name each tier
  ---
  duration_ms: 0.533057
  ...
# Subtest: projects tier walks with commitment rank and empty-project notice
ok 1546 - projects tier walks with commitment rank and empty-project notice
  ---
  duration_ms: 0.191396
  ...
# Subtest: references tier walks with commitment rank and reference notice
ok 1547 - references tier walks with commitment rank and reference notice
  ---
  duration_ms: 0.431564
  ...
# Subtest: jump notices use reviewEntryView when provided and keep the fallback
ok 1548 - jump notices use reviewEntryView when provided and keep the fallback
  ---
  duration_ms: 0.25673
  ...
# Subtest: tier notices fall back without tier ranks and wrap on the last line
ok 1549 - tier notices fall back without tier ranks and wrap on the last line
  ---
  duration_ms: 0.13614
  ...
# Subtest: boundary notice names commitments done and rotten next
ok 1550 - boundary notice names commitments done and rotten next
  ---
  duration_ms: 0.150387
  ...
# Subtest: walk anchor records handled keys with their neighbors
ok 1551 - walk anchor records handled keys with their neighbors
  ---
  duration_ms: 0.527217
  ...
# Subtest: cursor on a live entry wins over a lagging anchor
ok 1552 - cursor on a live entry wins over a lagging anchor
  ---
  duration_ms: 0.268863
  ...
# Subtest: [s after a stamp goes backwards from the anchor
ok 1553 - [s after a stamp goes backwards from the anchor
  ---
  duration_ms: 0.446874
  ...
# Subtest: release-then-]s continues from the anchor successor
ok 1554 - release-then-]s continues from the anchor successor
  ---
  duration_ms: 0.204771
  ...
# Subtest: non-contiguous counted stamp advances past the last handled rank
ok 1555 - non-contiguous counted stamp advances past the last handled rank
  ---
  duration_ms: 0.239728
  ...
# Subtest: anchor wraps at both ends
ok 1556 - anchor wraps at both ends
  ---
  duration_ms: 0.308449
  ...
# Subtest: advance across NEXT to TICKLER to ROTTEN lands the boundary
ok 1557 - advance across NEXT to TICKLER to ROTTEN lands the boundary
  ---
  duration_ms: 0.349086
  ...
# Subtest: tier capability gates on the freshness namespace version
ok 1558 - tier capability gates on the freshness namespace version
  ---
  duration_ms: 0.11021
  ...
# Subtest: empty queue notice reads the upkeep meter
ok 1559 - empty queue notice reads the upkeep meter
  ---
  duration_ms: 0.092888
  ...
# Subtest: refresh row reads lane intervals from the api with the once-Ready return
ok 1560 - refresh row reads lane intervals from the api with the once-Ready return
  ---
  duration_ms: 0.995832
  ...
# Subtest: endpoint jumps select the queue ends with full rank and total
ok 1561 - endpoint jumps select the queue ends with full rank and total
  ---
  duration_ms: 0.323938
  ...
# Subtest: endpoint jumps ignore cursor, anchor, and direction
ok 1562 - endpoint jumps ignore cursor, anchor, and direction
  ---
  duration_ms: 0.209801
  ...
# Subtest: endpoint jumps on empty and one-entry queues
ok 1563 - endpoint jumps on empty and one-entry queues
  ---
  duration_ms: 0.178611
  ...
# Subtest: a visited endpoint is still due under its own anchor
ok 1564 - a visited endpoint is still due under its own anchor
  ---
  duration_ms: 0.177469
  ...
# Subtest: lowercase steps continue from an endpoint anchor
ok 1565 - lowercase steps continue from an endpoint anchor
  ---
  duration_ms: 0.280185
  ...
# Subtest: counted review jump repeat 1 matches omitted repeat
ok 1566 - counted review jump repeat 1 matches omitted repeat
  ---
  duration_ms: 0.544971
  ...
# Subtest: counted review jump from the first entry lands N steps ahead
ok 1567 - counted review jump from the first entry lands N steps ahead
  ---
  duration_ms: 0.230561
  ...
# Subtest: counted review jump from the last entry wraps past the start
ok 1568 - counted review jump from the last entry wraps past the start
  ---
  duration_ms: 0.116452
  ...
# Subtest: counted review jump larger than the queue wraps once
ok 1569 - counted review jump larger than the queue wraps once
  ---
  duration_ms: 0.140849
  ...
# Subtest: counted review jump on a one-entry queue stays there
ok 1570 - counted review jump on a one-entry queue stays there
  ---
  duration_ms: 0.170847
  ...
# Subtest: counted review jump with no origin lands on the Nth entry
ok 1571 - counted review jump with no origin lands on the Nth entry
  ---
  duration_ms: 0.176668
  ...
# Subtest: counted review jump from a shaped anchor takes N surviving successors
ok 1572 - counted review jump from a shaped anchor takes N surviving successors
  ---
  duration_ms: 0.233055
  ...
# Subtest: counted review jump does not change endpoint selection
ok 1573 - counted review jump does not change endpoint selection
  ---
  duration_ms: 0.164434
  ...
# Subtest: a stamped endpoint that moved is stale and cannot land from old text
ok 1574 - a stamped endpoint that moved is stale and cannot land from old text
  ---
  duration_ms: 0.217826
  ...
# Subtest: stale endpoint target reselects the same endpoint in the new queue
ok 1575 - stale endpoint target reselects the same endpoint in the new queue
  ---
  duration_ms: 1.762776
  ...
# Subtest: endpoint retry is bounded and failures preserve the anchor
ok 1576 - endpoint retry is bounded and failures preserve the anchor
  ---
  duration_ms: 0.481469
  ...
# Subtest: endpoint jump to ROTTEN carries no boundary preamble
ok 1577 - endpoint jump to ROTTEN carries no boundary preamble
  ---
  duration_ms: 0.625755
  ...
# Subtest: endpoint notices keep v4 tier details and legacy v3 text
ok 1578 - endpoint notices keep v4 tier details and legacy v3 text
  ---
  duration_ms: 0.122333
  ...
# Subtest: onload registers first/last commands routed to the shared jump
ok 1579 - onload registers first/last commands routed to the shared jump
  ---
  duration_ms: 1.295504
  ...
# Subtest: jumpToDueTask consumes a pending Vim prefix as N review steps
ok 1580 - jumpToDueTask consumes a pending Vim prefix as N review steps
  ---
  duration_ms: 0.802052
  ...
# Subtest: registered next-due-task callback reads the pending Vim prefix
ok 1581 - registered next-due-task callback reads the pending Vim prefix
  ---
  duration_ms: 0.726508
  ...
# Subtest: explicit jumpToDueTask repeat skips the Vim prefix
ok 1582 - explicit jumpToDueTask repeat skips the Vim prefix
  ---
  duration_ms: 0.310794
  ...
# Subtest: non-normal editor with a pending prefix still jumps one entry
ok 1583 - non-normal editor with a pending prefix still jumps one entry
  ---
  duration_ms: 0.2773
  ...
# Subtest: stale counted replan reuses the captured repeat
ok 1584 - stale counted replan reuses the captured repeat
  ---
  duration_ms: 0.277861
  ...
# Subtest: endpoint jump with a pending prefix still lands on the endpoint
ok 1585 - endpoint jump with a pending prefix still lands on the endpoint
  ---
  duration_ms: 0.254095
  ...
# Subtest: counted forward landing on ROTTEN keeps the boundary preamble
ok 1586 - counted forward landing on ROTTEN keeps the boundary preamble
  ---
  duration_ms: 0.431885
  ...
# Subtest: PRE and POST are machine tiers; PRE is a commitment
ok 1587 - PRE and POST are machine tiers; PRE is a commitment
  ---
  duration_ms: 0.207135
  ...
# Subtest: fallback notices name PRE checklist and POST closeout
ok 1588 - fallback notices name PRE checklist and POST closeout
  ---
  duration_ms: 0.22019
  ...
# Subtest: text-first cursor matching does not skip Pills after an above-insert
ok 1589 - text-first cursor matching does not skip Pills after an above-insert
  ---
  duration_ms: 0.158372
  ...
# Subtest: day-scoped anchors from another day are ignored
ok 1590 - day-scoped anchors from another day are ignored
  ---
  duration_ms: 0.220541
  ...
# Subtest: boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
ok 1591 - boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
  ---
  duration_ms: 0.216564
  ...
# Subtest: ]S reaches POST with 77 ROTTEN rows and a null budget
ok 1592 - ]S reaches POST with 77 ROTTEN rows and a null budget
  ---
  duration_ms: 0.533979
  ...
# Subtest: nav normalizes a legacy v7 returned tier to tickler
ok 1593 - nav normalizes a legacy v7 returned tier to tickler
  ---
  duration_ms: 0.119708
  ...
# Subtest: RECURRING is a machine tier, a commitment, and a v9 capability
ok 1594 - RECURRING is a machine tier, a commitment, and a v9 capability
  ---
  duration_ms: 0.144076
  ...
# Subtest: RECURRING counts in reviewWalkRemaining and gates the boundary
ok 1595 - RECURRING counts in reviewWalkRemaining and gates the boundary
  ---
  duration_ms: 0.147622
  ...
# Subtest: matchReviewRecurringCursor is text-first like the checklist matcher
ok 1596 - matchReviewRecurringCursor is text-first like the checklist matcher
  ---
  duration_ms: 0.184102
  ...
# Subtest: fallback notices name RECURRING due detail with the reschedule hint
ok 1597 - fallback notices name RECURRING due detail with the reschedule hint
  ---
  duration_ms: 0.152682
  ...
# Subtest: Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
ok 1598 - Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
  ---
  duration_ms: 0.110832
  ...
# Subtest: bobLineDigest matches the shared bob-cli vectors
ok 1599 - bobLineDigest matches the shared bob-cli vectors
  ---
  duration_ms: 4.764398
  ...
# Subtest: parseGoToTaskParams accepts a complete v1 link and ignores extra keys
ok 1600 - parseGoToTaskParams accepts a complete v1 link and ignores extra keys
  ---
  duration_ms: 0.686461
  ...
# Subtest: parseGoToTaskParams treats ref and block as optional
ok 1601 - parseGoToTaskParams treats ref and block as optional
  ---
  duration_ms: 0.134968
  ...
# Subtest: parseGoToTaskParams rejects each malformed field
ok 1602 - parseGoToTaskParams rejects each malformed field
  ---
  duration_ms: 0.234467
  ...
# Subtest: vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
ok 1603 - vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
  ---
  duration_ms: 0.247493
  ...
# Subtest: refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
ok 1604 - refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
  ---
  duration_ms: 1.310863
  ...
# Subtest: handleGoToTaskUri notices each malformed parameter
ok 1605 - handleGoToTaskUri notices each malformed parameter
  ---
  duration_ms: 1.098548
  ...
# Subtest: handleGoToTaskUri notices a path outside the vault
ok 1606 - handleGoToTaskUri notices a path outside the vault
  ---
  duration_ms: 0.401637
  ...
# Subtest: handleGoToTaskUri notices a missing file inside the vault
ok 1607 - handleGoToTaskUri notices a missing file inside the vault
  ---
  duration_ms: 0.459558
  ...
# Subtest: handleGoToTaskUri maps a trailing-slash vault base
ok 1608 - handleGoToTaskUri maps a trailing-slash vault base
  ---
  duration_ms: 1.886773
  ...
# Subtest: handleGoToTaskUri prefers the open buffer over cachedRead
ok 1609 - handleGoToTaskUri prefers the open buffer over cachedRead
  ---
  duration_ms: 0.717981
  ...
# Subtest: handleGoToTaskUri re-finds by block id after an insert above the task
ok 1610 - handleGoToTaskUri re-finds by block id after an insert above the task
  ---
  duration_ms: 0.465248
  ...
# Subtest: handleGoToTaskUri re-finds a unique digest after a shift with no block
ok 1611 - handleGoToTaskUri re-finds a unique digest after a shift with no block
  ---
  duration_ms: 0.469607
  ...
# Subtest: handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
ok 1612 - handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
  ---
  duration_ms: 0.363975
  ...
# Subtest: handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
ok 1613 - handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
  ---
  duration_ms: 0.414131
  ...
# Subtest: handleGoToTaskUri reuses a leaf that already shows the note
ok 1614 - handleGoToTaskUri reuses a leaf that already shows the note
  ---
  duration_ms: 0.547084
  ...
# Subtest: handleGoToTaskUri switches a Reading-view leaf to editing
ok 1615 - handleGoToTaskUri switches a Reading-view leaf to editing
  ---
  duration_ms: 0.588063
  ...
# Subtest: handleGoToTaskUri records a jump from the prior cursor and none without one
ok 1616 - handleGoToTaskUri records a jump from the prior cursor and none without one
  ---
  duration_ms: 0.762696
  ...
# Subtest: handleGoToTaskUri never writes the vault or advances the walk
ok 1617 - handleGoToTaskUri never writes the vault or advances the walk
  ---
  duration_ms: 0.359987
  ...
# Subtest: handleGoToTaskUri reports when the note cannot be opened
ok 1618 - handleGoToTaskUri reports when the note cannot be opened
  ---
  duration_ms: 0.316034
  ...
# Subtest: focusTaskMoveDestination still lands without switching Reading view
ok 1619 - focusTaskMoveDestination still lands without switching Reading view
  ---
  duration_ms: 0.470118
  ...
# Subtest: onload registers both read-only navigation protocols when available
ok 1620 - onload registers both read-only navigation protocols when available
  ---
  duration_ms: 1.449278
  ...
# Subtest: onload skips protocol registration when the API is missing
ok 1621 - onload skips protocol registration when the API is missing
  ---
  duration_ms: 0.49771
  ...
# Subtest: registered protocol handler forwards params to handleGoToTaskUri
ok 1622 - registered protocol handler forwards params to handleGoToTaskUri
  ---
  duration_ms: 0.303309
  ...
# Subtest: handleGoToTaskUri maps a path through realpath when prefixes differ
ok 1623 - handleGoToTaskUri maps a path through realpath when prefixes differ
  ---
  duration_ms: 2.496517
  ...
# Subtest: cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
ok 1624 - cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
  ---
  duration_ms: 1.993257
  ...
# Subtest: findCancelLogParent finds a direct child but ignores a grandchild
ok 1625 - findCancelLogParent finds a direct child but ignores a grandchild
  ---
  duration_ms: 0.606208
  ...
# Subtest: getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
ok 1626 - getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
  ---
  duration_ms: 0.195874
  ...
# Subtest: formatCancelLogEntryText renders the exact preview text
ok 1627 - formatCancelLogEntryText renders the exact preview text
  ---
  duration_ms: 0.153893
  ...
# Subtest: planCancelLogEntry inserts a first-child log with tabs or spaces
ok 1628 - planCancelLogEntry inserts a first-child log with tabs or spaces
  ---
  duration_ms: 0.642357
  ...
# Subtest: planCancelLogEntry prepends under an existing log wherever it sits
ok 1629 - planCancelLogEntry prepends under an existing log wherever it sits
  ---
  duration_ms: 0.27254
  ...
# Subtest: planCancelLogEntry uses the fallback only when a marker exists
ok 1630 - planCancelLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.31909
  ...
# Subtest: isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
ok 1631 - isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
  ---
  duration_ms: 0.287008
  ...
# Subtest: describeCancelTaskRow covers single, counted, link, recurring, and hidden
ok 1632 - describeCancelTaskRow covers single, counted, link, recurring, and hidden
  ---
  duration_ms: 1.736616
  ...
# Subtest: planTaskCancelBatch cancels a single task with a first-child log
ok 1633 - planTaskCancelBatch cancels a single task with a first-child log
  ---
  duration_ms: 1.29318
  ...
# Subtest: planTaskCancelBatch upserts cancelled before the block id and preserves fields
ok 1634 - planTaskCancelBatch upserts cancelled before the block id and preserves fields
  ---
  duration_ms: 0.431604
  ...
# Subtest: planTaskCancelBatch records id-field task identities
ok 1635 - planTaskCancelBatch records id-field task identities
  ---
  duration_ms: 0.238145
  ...
# Subtest: planTaskCancelBatch skips closed targets and stays bottom-up
ok 1636 - planTaskCancelBatch skips closed targets and stays bottom-up
  ---
  duration_ms: 0.431654
  ...
# Subtest: planTaskCancelBatch refuses recurring targets in all three syntaxes
ok 1637 - planTaskCancelBatch refuses recurring targets in all three syntaxes
  ---
  duration_ms: 0.430242
  ...
# Subtest: planTaskCancelBatch handles empty reasons and stale preimages
ok 1638 - planTaskCancelBatch handles empty reasons and stale preimages
  ---
  duration_ms: 0.373774
  ...
# Subtest: planTaskCancelBatch preserves CRLF line endings
ok 1639 - planTaskCancelBatch preserves CRLF line endings
  ---
  duration_ms: 0.250809
  ...
# Subtest: cancel project conversion carries the log and reports it
ok 1640 - cancel project conversion carries the log and reports it
  ---
  duration_ms: 3.349145
  ...
# Subtest: getCancelTaskRowTitle names single, counted, and link sessions
ok 1641 - getCancelTaskRowTitle names single, counted, and link sessions
  ---
  duration_ms: 0.997846
  ...
# Subtest: getCancelReasonHints labels Enter per state and Esc as Keep open
ok 1642 - getCancelReasonHints labels Enter per state and Esc as Keep open
  ---
  duration_ms: 1.034185
  ...
# Subtest: the Cancel property item and the card's cancel row describe an open task
ok 1643 - the Cancel property item and the card's cancel row describe an open task
  ---
  duration_ms: 10.912458
  ...
# Subtest: Cancel row hides on closed tasks, plain bullets, and all-closed sessions
ok 1644 - Cancel row hides on closed tasks, plain bullets, and all-closed sessions
  ---
  duration_ms: 5.327844
  ...
# Subtest: Cancel row reports skipped closed targets in a counted session
ok 1645 - Cancel row reports skipped closed targets in a counted session
  ---
  duration_ms: 1.352423
  ...
# Subtest: the card refuses the cancel row on a recurring task and stays on the card
ok 1646 - the card refuses the cancel row on a recurring task and stays on the card
  ---
  duration_ms: 2.357462
  ...
# Subtest: cancel reason stage previews the typed, empty, fallback, and :: cases
ok 1647 - cancel reason stage previews the typed, empty, fallback, and :: cases
  ---
  duration_ms: 2.909897
  ...
# Subtest: cancel reason footer flips between plain, log, and fallback labels
ok 1648 - cancel reason footer flips between plain, log, and fallback labels
  ---
  duration_ms: 1.079582
  ...
# Subtest: Esc from the cancel reason stage writes nothing
ok 1649 - Esc from the cancel reason stage writes nothing
  ---
  duration_ms: 2.663436
  ...
# Subtest: single cancel writes [-], stamp, and first-child log in one transaction
ok 1650 - single cancel writes [-], stamp, and first-child log in one transaction
  ---
  duration_ms: 4.758326
  ...
# Subtest: empty reason writes no log unless one already exists
ok 1651 - empty reason writes no log unless one already exists
  ---
  duration_ms: 4.596357
  ...
# Subtest: stale single preimage refuses with nothing written
ok 1652 - stale single preimage refuses with nothing written
  ---
  duration_ms: 0.856786
  ...
# Subtest: cancel writes [-] with no NOW chip
ok 1653 - cancel writes [-] with no NOW chip
  ---
  duration_ms: 1.079611
  ...
# Subtest: TSC recovery runs with cancelled identities; a missing API still succeeds
ok 1654 - TSC recovery runs with cancelled identities; a missing API still succeeds
  ---
  duration_ms: 2.119337
  ...
# Subtest: a throwing TSC API is skipped silently with no chip
ok 1655 - a throwing TSC API is skipped silently with no chip
  ---
  duration_ms: 1.176036
  ...
# Subtest: counted cancel skips closed targets and reports them
ok 1656 - counted cancel skips closed targets and reports them
  ---
  duration_ms: 1.901761
  ...
# Subtest: same-file cancel folds today's Pomodoro prune into one transaction
ok 1657 - same-file cancel folds today's Pomodoro prune into one transaction
  ---
  duration_ms: 3.188278
  ...
# Subtest: link session cancels the target and removes the invoking link bullet
ok 1658 - link session cancels the target and removes the invoking link bullet
  ---
  duration_ms: 7.407766
  ...
# Subtest: buildCancelNoticeModel text covers every chip
ok 1659 - buildCancelNoticeModel text covers every chip
  ---
  duration_ms: 0.27785
  ...
# Subtest: renderCancelNoticeFragment builds the is-cancel card
ok 1660 - renderCancelNoticeFragment builds the is-cancel card
  ---
  duration_ms: 0.687603
  ...
# Subtest: isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
ok 1661 - isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
  ---
  duration_ms: 1.605385
  ...
# Subtest: findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
ok 1662 - findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
  ---
  duration_ms: 1.780029
  ...
# Subtest: collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
ok 1663 - collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
  ---
  duration_ms: 0.666002
  ...
# Subtest: planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
ok 1664 - planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
  ---
  duration_ms: 1.274915
  ...
# Subtest: planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
ok 1665 - planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
  ---
  duration_ms: 1.097145
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
ok 1666 - planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
  ---
  duration_ms: 1.131541
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
ok 1667 - planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
  ---
  duration_ms: 0.770642
  ...
# Subtest: planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
ok 1668 - planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
  ---
  duration_ms: 0.300093
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
ok 1669 - planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
  ---
  duration_ms: 0.891864
  ...
# Subtest: planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
ok 1670 - planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
  ---
  duration_ms: 0.805718
  ...
# Subtest: planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
ok 1671 - planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
  ---
  duration_ms: 0.537216
  ...
# Subtest: planDeferredPomodoroLinkCleanup preserves CRLF line endings
ok 1672 - planDeferredPomodoroLinkCleanup preserves CRLF line endings
  ---
  duration_ms: 0.276959
  ...
# Subtest: deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
ok 1673 - deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
  ---
  duration_ms: 0.293551
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks\#^x]] \#
ok 1674 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks\#^x]] \#
  ---
  duration_ms: 0.299372
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks\#^x|alias]] \#
ok 1675 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks\#^x|alias]] \#
  ---
  duration_ms: 0.178872
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks\#^x]]
ok 1676 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks\#^x]]
  ---
  duration_ms: 0.189111
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks\#^x]]
ok 1677 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks\#^x]]
  ---
  duration_ms: 0.158763
  ...
# Subtest: dedicated decoration check accepts paired strikes but cleanup never removes struck links
ok 1678 - dedicated decoration check accepts paired strikes but cleanup never removes struck links
  ---
  duration_ms: 0.299171
  ...
# Subtest: cleanup deletes only touched childless entries, preserving prose, placeholders and closed history
ok 1679 - cleanup deletes only touched childless entries, preserving prose, placeholders and closed history
  ---
  duration_ms: 0.293911
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\n", final newline false)
ok 1680 - cleanup handles adjacent EOF entries ("\\n", final newline false)
  ---
  duration_ms: 0.205362
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\n", final newline true)
ok 1681 - cleanup handles adjacent EOF entries ("\\n", final newline true)
  ---
  duration_ms: 0.171638
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\r\\n", final newline false)
ok 1682 - cleanup handles adjacent EOF entries ("\\r\\n", final newline false)
  ---
  duration_ms: 0.148604
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\r\\n", final newline true)
ok 1683 - cleanup handles adjacent EOF entries ("\\r\\n", final newline true)
  ---
  duration_ms: 0.156108
  ...
# Subtest: counted dependencies converge mixed sources and maintain one link per parent
ok 1684 - counted dependencies converge mixed sources and maintain one link per parent
  ---
  duration_ms: 22.5651
  ...
# Subtest: counted and single dependency gestures refuse inside a blockquote (DP29)
ok 1685 - counted and single dependency gestures refuse inside a blockquote (DP29)
  ---
  duration_ms: 0.496829
  ...
# Subtest: counted dependency candidates exclude every source and expose mixed state
ok 1686 - counted dependency candidates exclude every source and expose mixed state
  ---
  duration_ms: 1.059904
  ...
# Subtest: counted dependency block-ID prompting is planned atomically
ok 1687 - counted dependency block-ID prompting is planned atomically
  ---
  duration_ms: 2.315572
  ...
# Subtest: counted dependency runtime applies target, parents, and navigation in one undo group
ok 1688 - counted dependency runtime applies target, parents, and navigation in one undo group
  ---
  duration_ms: 7.489402
  ...
# Subtest: counted Depends-on removal recovers residents with [unblocked::]
ok 1689 - counted Depends-on removal recovers residents with [unblocked::]
  ---
  duration_ms: 4.840584
  ...
# Subtest: counted Depends-on removal writes [unblocked::] through the wired freshness API
ok 1690 - counted Depends-on removal writes [unblocked::] through the wired freshness API
  ---
  duration_ms: 5.180395
  ...
# Subtest: cross-file toggle changes only the source link
ok 1691 - cross-file toggle changes only the source link
  ---
  duration_ms: 1.955745
  ...
# Subtest: cross-file write failure still toggles only the source link
ok 1692 - cross-file write failure still toggles only the source link
  ---
  duration_ms: 0.666953
  ...
# Subtest: line-local fallback applies bottom-up and preserves CRLF
ok 1693 - line-local fallback applies bottom-up and preserves CRLF
  ---
  duration_ms: 0.787925
  ...
# Subtest: source line-count invariant rejects embedded newline changes
ok 1694 - source line-count invariant rejects embedded newline changes
  ---
  duration_ms: 0.233095
  ...
# Subtest: pure toggle refuses when the source changed under it
ok 1695 - pure toggle refuses when the source changed under it
  ---
  duration_ms: 0.210061
  ...
# Subtest: counted transclusion toggle evaluates each line independently
ok 1696 - counted transclusion toggle evaluates each line independently
  ---
  duration_ms: 0.41946
  ...
# Subtest: transclusion toggle is refused on Depends-On lines
ok 1697 - transclusion toggle is refused on Depends-On lines
  ---
  duration_ms: 0.297508
  ...
# Subtest: legacy sole-link children toggle purely, without field or status writes
ok 1698 - legacy sole-link children toggle purely, without field or status writes
  ---
  duration_ms: 0.475027
  ...
# Subtest: Ctrl+D on the Depends on row clears the line, field, and legacy children
ok 1699 - Ctrl+D on the Depends on row clears the line, field, and legacy children
  ---
  duration_ms: 3.304029
  ...
# Subtest: Ctrl+D clears a field-only dependency without a line
ok 1700 - Ctrl+D clears a field-only dependency without a line
  ---
  duration_ms: 2.39841
  ...
# Subtest: counted Ctrl+D on the Depends on row clears every targeted task
ok 1701 - counted Ctrl+D on the Depends on row clears every targeted task
  ---
  duration_ms: 2.758428
  ...
# Subtest: findRemovedLineText reports deleted lines
ok 1702 - findRemovedLineText reports deleted lines
  ---
  duration_ms: 0.19893
  ...
# Subtest: hand-edit mirror projects an edited line into the field
ok 1703 - hand-edit mirror projects an edited line into the field
  ---
  duration_ms: 2.094008
  ...
# Subtest: hand-edit mirror canonicalises a hand-written line variant
ok 1704 - hand-edit mirror canonicalises a hand-written line variant
  ---
  duration_ms: 1.016371
  ...
# Subtest: hand-edit mirror drops a linkless line and the field
ok 1705 - hand-edit mirror drops a linkless line and the field
  ---
  duration_ms: 1.091103
  ...
# Subtest: hand-edit mirror clears the field after the line is deleted
ok 1706 - hand-edit mirror clears the field after the line is deleted
  ---
  duration_ms: 1.234457
  ...
# Subtest: hand-edit mirror leaves malformed lines alone
ok 1707 - hand-edit mirror leaves malformed lines alone
  ---
  duration_ms: 0.278172
  ...
# Subtest: hand-edit mirror leaves legacy-only children for the hooks
ok 1708 - hand-edit mirror leaves legacy-only children for the hooks
  ---
  duration_ms: 0.459428
  ...
# Subtest: hand-edit mirror blocks when an open prerequisite is added by hand
ok 1709 - hand-edit mirror blocks when an open prerequisite is added by hand
  ---
  duration_ms: 1.065335
  ...
# Subtest: hand-edit mirror never transfers commitment to the target
ok 1710 - hand-edit mirror never transfers commitment to the target
  ---
  duration_ms: 1.066377
  ...
# Subtest: hand-edit mirror recovers when the last open prerequisite is removed by hand
ok 1711 - hand-edit mirror recovers when the last open prerequisite is removed by hand
  ---
  duration_ms: 1.397669
  ...
# Subtest: hand-edit mirror leaves a half-typed link alone
ok 1712 - hand-edit mirror leaves a half-typed link alone
  ---
  duration_ms: 0.369205
  ...
# Subtest: hand-edit mirror clears the owning task when its last-child line is deleted
ok 1713 - hand-edit mirror clears the owning task when its last-child line is deleted
  ---
  duration_ms: 1.10475
  ...
# Subtest: mirror scheduler debounces at the contract interval
ok 1714 - mirror scheduler debounces at the contract interval
  ---
  duration_ms: 0.947018
  ...
# Subtest: mirror scheduler seeds the baseline from the update start state
ok 1715 - mirror scheduler seeds the baseline from the update start state
  ---
  duration_ms: 1.750903
  ...
# Subtest: mirror scheduler keeps the first baseline and maps the owner across a burst
ok 1716 - mirror scheduler keeps the first baseline and maps the owner across a burst
  ---
  duration_ms: 0.505074
  ...
# Subtest: mirror listener runs clear-field for a first-edit deletion with a following sibling
ok 1717 - mirror listener runs clear-field for a first-edit deletion with a following sibling
  ---
  duration_ms: 11.697366
  ...
# Subtest: mirror fire re-arms while the cursor stays on the edited line
ok 1718 - mirror fire re-arms while the cursor stays on the edited line
  ---
  duration_ms: 2.656593
  ...
# Subtest: mirror scheduler reads changed ranges from the CM6 update
ok 1719 - mirror scheduler reads changed ranges from the CM6 update
  ---
  duration_ms: 0.304021
  ...
# Subtest: mirror scheduler skips IME composition
ok 1720 - mirror scheduler skips IME composition
  ---
  duration_ms: 0.239598
  ...
# Subtest: mirror scheduler skips open modals
ok 1721 - mirror scheduler skips open modals
  ---
  duration_ms: 0.192868
  ...
# Subtest: counted Ctrl+D clears every targeted task in one transaction with one notice
ok 1722 - counted Ctrl+D clears every targeted task in one transaction with one notice
  ---
  duration_ms: 5.921277
  ...
# Subtest: counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
ok 1723 - counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
  ---
  duration_ms: 1.626075
  ...
# Subtest: counted N! on only a Depends-On line refuses without writing
ok 1724 - counted N! on only a Depends-On line refuses without writing
  ---
  duration_ms: 0.278322
  ...
# Subtest: promotion targets enumerate real tasks and assign stable IDs
ok 1725 - promotion targets enumerate real tasks and assign stable IDs
  ---
  duration_ms: 3.76005
  ...
# Subtest: promotion file planner expands live links and preserves history
ok 1726 - promotion file planner expands live links and preserves history
  ---
  duration_ms: 4.399161
  ...
# Subtest: promotion file planner handles forms, whitespace, and subtrees
ok 1727 - promotion file planner handles forms, whitespace, and subtrees
  ---
  duration_ms: 1.059393
  ...
# Subtest: promotion file planner keeps compatibility for non-live references
ok 1728 - promotion file planner keeps compatibility for non-live references
  ---
  duration_ms: 0.736206
  ...
# Subtest: forward promotion expands live links, persists anchors, and removes the source
ok 1729 - forward promotion expands live links, persists anchors, and removes the source
  ---
  duration_ms: 7.286925
  ...
# Subtest: forward promotion uses zero-task fallback and keeps reverse one-to-one
ok 1730 - forward promotion uses zero-task fallback and keeps reverse one-to-one
  ---
  duration_ms: 1.096143
  ...
# Subtest: forward promotion retains the source on ambiguous, stale, and write failures
ok 1731 - forward promotion retains the source on ambiguous, stale, and write failures
  ---
  duration_ms: 1.168011
  ...
# Subtest: forward promotion discovers live links without a backlink cache and uses one open-editor write
ok 1732 - forward promotion discovers live links without a backlink cache and uses one open-editor write
  ---
  duration_ms: 1.80109
  ...
# Subtest: forward conversion carries a Depends-On line and reverse restores it
not ok 1733 - forward conversion carries a Depends-On line and reverse restores it
  ---
  duration_ms: 17.52114
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-navigation-hotkeys-forward-promotion.cjs:662:1'
  failureType: 'testCodeFailure'
  error: |-
    The input was expected to not match the regular expression /Work_ship#\^prj/. Input:
    
    '---\n' +
      'type: "[[area]]"\n' +
      '---\n' +
      '\n' +
      '## Tasks\n' +
      '\n' +
      '- [ ] #task Prereq [id:: Areas__Work__prereq] ^prereq\n' +
      '\t- 🧱 **BLOCKS:** [[Work_ship#^prj]]\n' +
      '- [?] #task Ship it [created::2026-10-20] [id:: Areas__Work__ship] [dependsOn:: Areas__Work__prereq] ^ship\n' +
      '\t- ⛓️ **DEPENDS ON:** [[#^prereq]]\n' +
      '\t- [?] #task Follow up [created::2026-10-20] ^follow-up'
    
  code: 'ERR_ASSERTION'
  name: 'AssertionError'
  expected:
  actual: |-
    ---
    type: "[[area]]"
    ---
    
    ## Tasks
    
    - [ ] #task Prereq [id:: Areas__Work__prereq] ^prereq
    	- 🧱 **BLOCKS:** [[Work_ship#^prj]]
    - [?] #task Ship it [created::2026-10-20] [id:: Areas__Work__ship] [dependsOn:: Areas__Work__prereq] ^ship
    	- ⛓️ **DEPENDS ON:** [[#^prereq]]
    	- [?] #task Follow up [created::2026-10-20] ^follow-up
  operator: 'doesNotMatch'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-navigation-hotkeys-forward-promotion.cjs:734:10)
    async Test.run (node:internal/test_runner/test:980:9)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: planTaskLaneBatch commits every Ready target to Next
ok 1734 - planTaskLaneBatch commits every Ready target to Next
  ---
  duration_ms: 3.035206
  ...
# Subtest: planTaskLaneBatch releases Next and In Progress to Ready
ok 1735 - planTaskLaneBatch releases Next and In Progress to Ready
  ---
  duration_ms: 0.52849
  ...
# Subtest: planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
ok 1736 - planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
  ---
  duration_ms: 1.008115
  ...
# Subtest: planTaskLaneBatch skips Blocked and refuses stale preimages
ok 1737 - planTaskLaneBatch skips Blocked and refuses stale preimages
  ---
  duration_ms: 0.330361
  ...
# Subtest: buildLaneToggleNotice reports commit and release with and without budgets
ok 1738 - buildLaneToggleNotice reports commit and release with and without budgets
  ---
  duration_ms: 0.37166
  ...
# Subtest: describeLaneRow covers task, counted, and link sessions
ok 1739 - describeLaneRow covers task, counted, and link sessions
  ---
  duration_ms: 0.432005
  ...
# Subtest: toggleTaskLane commits Ready to Next and reports lane budgets
ok 1740 - toggleTaskLane commits Ready to Next and reports lane budgets
  ---
  duration_ms: 2.488281
  ...
# Subtest: toggleTaskLane releases to Ready without the api
ok 1741 - toggleTaskLane releases to Ready without the api
  ---
  duration_ms: 1.181116
  ...
# Subtest: toggleTaskLane release logs the summary on In Progress tasks
ok 1742 - toggleTaskLane release logs the summary on In Progress tasks
  ---
  duration_ms: 1.170756
  ...
# Subtest: toggleTaskLane skips Blocked targets
ok 1743 - toggleTaskLane skips Blocked targets
  ---
  duration_ms: 0.829303
  ...
# Subtest: counted toggleTaskLane covers the current task plus the next N tasks
ok 1744 - counted toggleTaskLane covers the current task plus the next N tasks
  ---
  duration_ms: 0.597851
  ...
# Subtest: toggleTaskLane on a Task Link writes through the open buffer
ok 1745 - toggleTaskLane on a Task Link writes through the open buffer
  ---
  duration_ms: 3.134104
  ...
# Subtest: toggleTaskLane on Task Links releases across notes
ok 1746 - toggleTaskLane on Task Links releases across notes
  ---
  duration_ms: 1.146579
  ...
# Subtest: toggleTaskLane refuses when a preimage changed
ok 1747 - toggleTaskLane refuses when a preimage changed
  ---
  duration_ms: 0.197557
  ...
# Subtest: Ctrl+Shift+P shows a pinned lane row that commits immediately
ok 1748 - Ctrl+Shift+P shows a pinned lane row that commits immediately
  ---
  duration_ms: 10.831878
  ...
# Subtest: Ctrl+Shift+P link mode shows the lane row with release detail
ok 1749 - Ctrl+Shift+P link mode shows the lane row with release detail
  ---
  duration_ms: 4.507829
  ...
# Subtest: Ctrl+Shift+P lane release with In Progress goes through the reason stage
ok 1750 - Ctrl+Shift+P lane release with In Progress goes through the reason stage
  ---
  duration_ms: 2.573004
  ...
# Subtest: getLinkPickerSessionSubtitle keeps the clamp for a single link
ok 1751 - getLinkPickerSessionSubtitle keeps the clamp for a single link
  ---
  duration_ms: 0.163803
  ...
# Subtest: link-mode priority notice keeps via Task Links visible
ok 1752 - link-mode priority notice keeps via Task Links visible
  ---
  duration_ms: 0.714916
  ...
# Subtest: already-handled Alt+N leaves Vim state alone
ok 1753 - already-handled Alt+N leaves Vim state alone
  ---
  duration_ms: 0.399182
  ...
# Subtest: Alt+N fallback still dispatches once with the Vim count
ok 1754 - Alt+N fallback still dispatches once with the Vim count
  ---
  duration_ms: 0.712812
  ...
# Subtest: lane release deletes an emptied entry (cross-file, Alt+N)
ok 1755 - lane release deletes an emptied entry (cross-file, Alt+N)
  ---
  duration_ms: 2.420222
  ...
# Subtest: lane release deletes an emptied entry (cross-file, card)
ok 1756 - lane release deletes an emptied entry (cross-file, card)
  ---
  duration_ms: 2.432114
  ...
# Subtest: lane release deletes an emptied entry (same-file, Alt+N)
ok 1757 - lane release deletes an emptied entry (same-file, Alt+N)
  ---
  duration_ms: 2.835424
  ...
# Subtest: lane release deletes an emptied entry (same-file, card)
ok 1758 - lane release deletes an emptied entry (same-file, card)
  ---
  duration_ms: 3.090381
  ...
# Subtest: Task Link release deletes its entry in one undo group (separate, Alt+N)
ok 1759 - Task Link release deletes its entry in one undo group (separate, Alt+N)
  ---
  duration_ms: 1.500946
  ...
# Subtest: Task Link release deletes its entry in one undo group (separate, card)
ok 1760 - Task Link release deletes its entry in one undo group (separate, card)
  ---
  duration_ms: 3.07412
  ...
# Subtest: Task Link release deletes its entry in one undo group (folded, Alt+N)
ok 1761 - Task Link release deletes its entry in one undo group (folded, Alt+N)
  ---
  duration_ms: 0.933623
  ...
# Subtest: Task Link release deletes its entry in one undo group (folded, card)
ok 1762 - Task Link release deletes its entry in one undo group (folded, card)
  ---
  duration_ms: 2.872685
  ...
# Subtest: parseLinkPickerTaskLink recognizes dedicated Task Link bullets
ok 1763 - parseLinkPickerTaskLink recognizes dedicated Task Link bullets
  ---
  duration_ms: 2.074201
  ...
# Subtest: discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
ok 1764 - discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
  ---
  duration_ms: 1.097386
  ...
# Subtest: discoverLinkPickerTargets leaves \#task lines to the regular picker
ok 1765 - discoverLinkPickerTargets leaves \#task lines to the regular picker
  ---
  duration_ms: 0.300293
  ...
# Subtest: findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
ok 1766 - findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
  ---
  duration_ms: 0.43466
  ...
# Subtest: createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
ok 1767 - createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
  ---
  duration_ms: 1.591509
  ...
# Subtest: getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
ok 1768 - getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
  ---
  duration_ms: 0.588945
  ...
# Subtest: bare link mode edits the task behind a Task Link through the open buffer
ok 1769 - bare link mode edits the task behind a Task Link through the open buffer
  ---
  duration_ms: 14.457017
  ...
# Subtest: counted link mode writes across notes through both the open buffer and the vault
ok 1770 - counted link mode writes across notes through both the open buffer and the vault
  ---
  duration_ms: 3.987114
  ...
# Subtest: Task Link scheduled delete recovers a Blocked task through the wired freshness API
ok 1771 - Task Link scheduled delete recovers a Blocked task through the wired freshness API
  ---
  duration_ms: 5.23663
  ...
# Subtest: link mode refuses the whole operation when a linked note changed
ok 1772 - link mode refuses the whole operation when a linked note changed
  ---
  duration_ms: 2.951657
  ...
# Subtest: link mode reports a closed target and changes nothing
ok 1773 - link mode reports a closed target and changes nothing
  ---
  duration_ms: 1.426394
  ...
# Subtest: link mode defers to a future date, blocks the task, and prunes today
ok 1774 - link mode defers to a future date, blocks the task, and prunes today
  ---
  duration_ms: 10.592781
  ...
# Subtest: bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
ok 1775 - bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
  ---
  duration_ms: 2.120209
  ...
# Subtest: Task Link scheduled write deletes its entry (separate)
ok 1776 - Task Link scheduled write deletes its entry (separate)
  ---
  duration_ms: 3.217965
  ...
# Subtest: Task Link scheduled write deletes its entry (folded)
ok 1777 - Task Link scheduled write deletes its entry (folded)
  ---
  duration_ms: 3.08439
  ...
# Subtest: folded Task Link scheduling maps the cursor past logs inserted before the emptied entry
ok 1778 - folded Task Link scheduling maps the cursor past logs inserted before the emptied entry
  ---
  duration_ms: 4.187887
  ...
# Subtest: dash restore suppresses editor notice after deliberate navigation
ok 1779 - dash restore suppresses editor notice after deliberate navigation
  ---
  duration_ms: 22.058444
  ...
# Subtest: open-task dispatch timeout is registered for plugin cleanup
ok 1780 - open-task dispatch timeout is registered for plugin cleanup
  ---
  duration_ms: 0.501458
  ...
# Subtest: jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
ok 1781 - jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
  ---
  duration_ms: 4.1473
  ...
# Subtest: jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
ok 1782 - jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
  ---
  duration_ms: 1.112254
  ...
# Subtest: jumpToOpenObsidianTask keeps current-swap transaction failures local
ok 1783 - jumpToOpenObsidianTask keeps current-swap transaction failures local
  ---
  duration_ms: 0.643258
  ...
# Subtest: jumpToOpenObsidianTask refuses current-up without jumping or mutating
ok 1784 - jumpToOpenObsidianTask refuses current-up without jumping or mutating
  ---
  duration_ms: 0.382961
  ...
# Subtest: jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
ok 1785 - jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
  ---
  duration_ms: 1.647396
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
ok 1786 - Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
  ---
  duration_ms: 0.57585
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
ok 1787 - Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
  ---
  duration_ms: 0.637558
  ...
# Subtest: counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
ok 1788 - counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
  ---
  duration_ms: 0.970754
  ...
# Subtest: an impossible counted Pomodoro move refuses without jumping or mutating
ok 1789 - an impossible counted Pomodoro move refuses without jumping or mutating
  ---
  duration_ms: 0.420102
  ...
# Subtest: counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
ok 1790 - counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
  ---
  duration_ms: 0.545912
  ...
# Subtest: counted open-task jump on a sole current target keeps the existing notice
ok 1791 - counted open-task jump on a sole current target keeps the existing notice
  ---
  duration_ms: 0.164374
  ...
# Subtest: dispatch guard allows exactly one counted Pomodoro move when the command route also fires
ok 1792 - dispatch guard allows exactly one counted Pomodoro move when the command route also fires
  ---
  duration_ms: 0.63894
  ...
# Subtest: bullet property picker reconciles duplicate bare and counted opens
ok 1793 - bullet property picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 12.926825
  ...
# Subtest: bullet property picker close lifecycle clears tracking for fresh sessions
ok 1794 - bullet property picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 7.737495
  ...
# Subtest: task move picker reconciles duplicate bare and counted opens
ok 1795 - task move picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 2.495746
  ...
# Subtest: task move picker close lifecycle clears tracking for fresh sessions
ok 1796 - task move picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 1.0055
  ...
# Subtest: Pomodoro bullet move picker opens sessions and clears the shared move picker slot
ok 1797 - Pomodoro bullet move picker opens sessions and clears the shared move picker slot
  ---
  duration_ms: 2.913463
  ...
# Subtest: Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
ok 1798 - Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
  ---
  duration_ms: 0.784228
  ...
# Subtest: move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
ok 1799 - move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
  ---
  duration_ms: 1.275997
  ...
# Subtest: commitPomodoroBulletMoveSession applies one guarded same-file transaction
ok 1800 - commitPomodoroBulletMoveSession applies one guarded same-file transaction
  ---
  duration_ms: 2.406456
  ...
# Subtest: Pomodoro bullet move picker confirms = through the actual picker callback
ok 1801 - Pomodoro bullet move picker confirms = through the actual picker callback
  ---
  duration_ms: 2.244366
  ...
# Subtest: Pomodoro bullet move picker reserves =NAME for peeling a named merged component
ok 1802 - Pomodoro bullet move picker reserves =NAME for peeling a named merged component
  ---
  duration_ms: 1.079662
  ...
# Subtest: Pomodoro bullet move picker confirms =email through the actual picker callback
ok 1803 - Pomodoro bullet move picker confirms =email through the actual picker callback
  ---
  duration_ms: 1.370567
  ...
# Subtest: Pomodoro bullet move picker confirms = review through the actual picker callback
ok 1804 - Pomodoro bullet move picker confirms = review through the actual picker callback
  ---
  duration_ms: 0.70199
  ...
# Subtest: Pomodoro bullet move picker confirms =focus by unnaming a single-name source
ok 1805 - Pomodoro bullet move picker confirms =focus by unnaming a single-name source
  ---
  duration_ms: 0.72245
  ...
# Subtest: Pomodoro bullet split stale-content guard does not write
ok 1806 - Pomodoro bullet split stale-content guard does not write
  ---
  duration_ms: 0.307207
  ...
# Subtest: Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
ok 1807 - Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
  ---
  duration_ms: 0.604925
  ...
# Subtest: native isOpen regression: pickers attach, close clears slot, reopen works
ok 1808 - native isOpen regression: pickers attach, close clears slot, reopen works
  ---
  duration_ms: 2.700698
  ...
# Subtest: stale registered pickers fail open on the next key
ok 1809 - stale registered pickers fail open on the next key
  ---
  duration_ms: 2.278271
  ...
# Subtest: planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
ok 1810 - planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
  ---
  duration_ms: 4.705916
  ...
# Subtest: planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
ok 1811 - planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
  ---
  duration_ms: 0.546644
  ...
# Subtest: planPomodoroBulletMove preserves the source when only some siblings move out
ok 1812 - planPomodoroBulletMove preserves the source when only some siblings move out
  ---
  duration_ms: 0.326674
  ...
# Subtest: planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
ok 1813 - planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
  ---
  duration_ms: 0.37133
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
ok 1814 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
  ---
  duration_ms: 0.594034
  ...
# Subtest: planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
ok 1815 - planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
  ---
  duration_ms: 0.738951
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
ok 1816 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
  ---
  duration_ms: 0.413369
  ...
# Subtest: planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
ok 1817 - planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
  ---
  duration_ms: 0.304462
  ...
# Subtest: planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
ok 1818 - planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
  ---
  duration_ms: 0.505235
  ...
# Subtest: planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
ok 1819 - planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
  ---
  duration_ms: 0.838421
  ...
# Subtest: planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
ok 1820 - planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
  ---
  duration_ms: 0.297599
  ...
# Subtest: planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
ok 1821 - planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
  ---
  duration_ms: 0.231472
  ...
# Subtest: planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
ok 1822 - planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
  ---
  duration_ms: 0.394774
  ...
# Subtest: planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
ok 1823 - planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
  ---
  duration_ms: 0.414011
  ...
# Subtest: planPomodoroBulletMove deletes both open and closed source entries the same way
ok 1824 - planPomodoroBulletMove deletes both open and closed source entries the same way
  ---
  duration_ms: 0.40861
  ...
# Subtest: planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
ok 1825 - planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
  ---
  duration_ms: 0.315813
  ...
# Subtest: planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
ok 1826 - planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
  ---
  duration_ms: 0.377791
  ...
# Subtest: planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
ok 1827 - planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
  ---
  duration_ms: 0.475719
  ...
# Subtest: planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
ok 1828 - planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
  ---
  duration_ms: 0.303991
  ...
# Subtest: planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
ok 1829 - planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
  ---
  duration_ms: 0.43468
  ...
# Subtest: planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
ok 1830 - planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
  ---
  duration_ms: 0.289293
  ...
# Subtest: planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
ok 1831 - planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
  ---
  duration_ms: 0.311475
  ...
# Subtest: planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
ok 1832 - planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
  ---
  duration_ms: 0.212687
  ...
# Subtest: planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
ok 1833 - planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
  ---
  duration_ms: 0.37665
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
ok 1834 - planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
  ---
  duration_ms: 0.248304
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
ok 1835 - planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
  ---
  duration_ms: 0.451312
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
ok 1836 - planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
  ---
  duration_ms: 3.330961
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
ok 1837 - planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
  ---
  duration_ms: 0.440351
  ...
# Subtest: Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
ok 1838 - Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
  ---
  duration_ms: 5.475886
  ...
# Subtest: commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
ok 1839 - commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
  ---
  duration_ms: 3.075713
  ...
# Subtest: commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
ok 1840 - commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
  ---
  duration_ms: 1.044695
  ...
# Subtest: commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
ok 1841 - commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
  ---
  duration_ms: 0.478964
  ...
# Subtest: commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
ok 1842 - commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
  ---
  duration_ms: 0.400916
  ...
# Subtest: Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
ok 1843 - Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
  ---
  duration_ms: 6.606105
  ...
# Subtest: Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
ok 1844 - Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
  ---
  duration_ms: 0.826839
  ...
# Subtest: Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
ok 1845 - Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
  ---
  duration_ms: 0.768057
  ...
# Subtest: Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
ok 1846 - Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
  ---
  duration_ms: 1.364275
  ...
# Subtest: task move picker closes before commit while other pickers retain delayed close
ok 1847 - task move picker closes before commit while other pickers retain delayed close
  ---
  duration_ms: 0.91602
  ...
# Subtest: parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
ok 1848 - parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
  ---
  duration_ms: 2.169654
  ...
# Subtest: normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
ok 1849 - normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
  ---
  duration_ms: 0.525724
  ...
# Subtest: formatPomodoroEntryLine emits a placeholder entry with or without a name
ok 1850 - formatPomodoroEntryLine emits a placeholder entry with or without a name
  ---
  duration_ms: 0.191455
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
ok 1851 - createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
  ---
  duration_ms: 3.039725
  ...
# Subtest: createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
ok 1852 - createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
  ---
  duration_ms: 0.991844
  ...
# Subtest: createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
ok 1853 - createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
  ---
  duration_ms: 0.805868
  ...
# Subtest: createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
ok 1854 - createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
  ---
  duration_ms: 0.817832
  ...
# Subtest: buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
ok 1855 - buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
  ---
  duration_ms: 0.303099
  ...
# Subtest: buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
ok 1856 - buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
  ---
  duration_ms: 0.480778
  ...
# Subtest: createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
ok 1857 - createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
  ---
  duration_ms: 0.791682
  ...
# Subtest: createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
ok 1858 - createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
  ---
  duration_ms: 0.409913
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
ok 1859 - createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
  ---
  duration_ms: 0.385106
  ...
# Subtest: collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
ok 1860 - collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
  ---
  duration_ms: 0.50301
  ...
# Subtest: findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
ok 1861 - findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
  ---
  duration_ms: 0.600055
  ...
# Subtest: findPomodoroBulletContext leaves plain \#task lines on the task-move route
ok 1862 - findPomodoroBulletContext leaves plain \#task lines on the task-move route
  ---
  duration_ms: 0.37155
  ...
# Subtest: discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
ok 1863 - discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
  ---
  duration_ms: 1.019838
  ...
# Subtest: findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
ok 1864 - findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
  ---
  duration_ms: 1.017253
  ...
# Subtest: discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
ok 1865 - discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
  ---
  duration_ms: 1.280275
  ...
# Subtest: isMovablePomodoroEntryContext matches open current and future Pomodoro entries
ok 1866 - isMovablePomodoroEntryContext matches open current and future Pomodoro entries
  ---
  duration_ms: 4.345768
  ...
# Subtest: planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
ok 1867 - planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
  ---
  duration_ms: 1.166438
  ...
# Subtest: planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
ok 1868 - planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
  ---
  duration_ms: 0.441342
  ...
# Subtest: planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
ok 1869 - planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
  ---
  duration_ms: 0.538448
  ...
# Subtest: planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
ok 1870 - planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
  ---
  duration_ms: 0.59179
  ...
# Subtest: planPomodoroEntryReorder handles counted current swaps and their inverses
ok 1871 - planPomodoroEntryReorder handles counted current swaps and their inverses
  ---
  duration_ms: 0.719274
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
ok 1872 - planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
  ---
  duration_ms: 0.338557
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
ok 1873 - planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
  ---
  duration_ms: 0.304542
  ...
# Subtest: planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
ok 1874 - planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
  ---
  duration_ms: 0.667705
  ...
# Subtest: planPomodoroEntryReorder round-trips a future-up swap across the current open entry
ok 1875 - planPomodoroEntryReorder round-trips a future-up swap across the current open entry
  ---
  duration_ms: 0.742508
  ...
# Subtest: planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
ok 1876 - planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
  ---
  duration_ms: 0.686241
  ...
# Subtest: planPomodoroEntryReorder refuses moving down past the last placeholder in the section
ok 1877 - planPomodoroEntryReorder refuses moving down past the last placeholder in the section
  ---
  duration_ms: 0.290014
  ...
# Subtest: planPomodoroEntryReorder refuses both directions for a lone placeholder
ok 1878 - planPomodoroEntryReorder refuses both directions for a lone placeholder
  ---
  duration_ms: 0.233045
  ...
# Subtest: planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
ok 1879 - planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
  ---
  duration_ms: 0.277961
  ...
# Subtest: planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
ok 1880 - planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
  ---
  duration_ms: 0.343587
  ...
# Subtest: planPomodoroEntryReorder refuses illegal current/future spans atomically
ok 1881 - planPomodoroEntryReorder refuses illegal current/future spans atomically
  ---
  duration_ms: 0.747949
  ...
# Subtest: planPomodoroEntryReorder rejects a stale source line
ok 1882 - planPomodoroEntryReorder rejects a stale source line
  ---
  duration_ms: 0.228847
  ...
# Subtest: planPomodoroEntryReorder round-trips CRLF content
ok 1883 - planPomodoroEntryReorder round-trips CRLF content
  ---
  duration_ms: 0.357262
  ...
# Subtest: planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
ok 1884 - planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
  ---
  duration_ms: 0.258123
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
ok 1885 - planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
  ---
  duration_ms: 0.4086
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up three positions and round-trips
ok 1886 - planPomodoroEntryReorder moves a placeholder up three positions and round-trips
  ---
  duration_ms: 0.567804
  ...
# Subtest: planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
ok 1887 - planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
  ---
  duration_ms: 0.271097
  ...
# Subtest: planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
ok 1888 - planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
  ---
  duration_ms: 0.762727
  ...
# Subtest: planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
ok 1889 - planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
  ---
  duration_ms: 0.96865
  ...
# Subtest: planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
ok 1890 - planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
  ---
  duration_ms: 0.419782
  ...
# Subtest: peelPomodoroMergedName removes every matching canonical plus component
ok 1891 - peelPomodoroMergedName removes every matching canonical plus component
  ---
  duration_ms: 2.003165
  ...
# Subtest: planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
ok 1892 - planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
  ---
  duration_ms: 4.899276
  ...
# Subtest: planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
ok 1893 - planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
  ---
  duration_ms: 0.803855
  ...
# Subtest: planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
ok 1894 - planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
  ---
  duration_ms: 0.913074
  ...
# Subtest: planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
ok 1895 - planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
  ---
  duration_ms: 1.169123
  ...
# Subtest: planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
ok 1896 - planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
  ---
  duration_ms: 1.710496
  ...
# Subtest: planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
ok 1897 - planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
  ---
  duration_ms: 0.943582
  ...
# Subtest: planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
ok 1898 - planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
  ---
  duration_ms: 1.568024
  ...
# Subtest: Pomodoro bullet move picker typing =NAME or Escape does not write
ok 1899 - Pomodoro bullet move picker typing =NAME or Escape does not write
  ---
  duration_ms: 3.121862
  ...
# Subtest: planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
ok 1900 - planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
  ---
  duration_ms: 0.689497
  ...
# Subtest: planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
ok 1901 - planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
  ---
  duration_ms: 0.339658
  ...
# Subtest: planPomodoroEntryRename reports unchanged when the normalized name matches the current name
ok 1902 - planPomodoroEntryRename reports unchanged when the normalized name matches the current name
  ---
  duration_ms: 0.163402
  ...
# Subtest: planPomodoroEntryRename rejects unsupported trailing content and a stale source line
ok 1903 - planPomodoroEntryRename rejects unsupported trailing content and a stale source line
  ---
  duration_ms: 0.180615
  ...
# Subtest: planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
ok 1904 - planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
  ---
  duration_ms: 0.192538
  ...
# Subtest: planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
ok 1905 - planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
  ---
  duration_ms: 2.111381
  ...
# Subtest: planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
ok 1906 - planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
  ---
  duration_ms: 2.520362
  ...
# Subtest: planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
ok 1907 - planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
  ---
  duration_ms: 0.698954
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: priority notice relative day helpers handle offsets ranges and icons
ok 1908 - priority notice relative day helpers handle offsets ranges and icons
  ---
  duration_ms: 1.311134
  ...
# Subtest: priority notice model summarizes single counted and project writes
ok 1909 - priority notice model summarizes single counted and project writes
  ---
  duration_ms: 3.202095
  ...
# Subtest: priority notice renderer builds an accessible fragment
ok 1910 - priority notice renderer builds an accessible fragment
  ---
  duration_ms: 1.852738
  ...
# Subtest: priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
ok 1911 - priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
  ---
  duration_ms: 7.928921
  ...
# Subtest: priority notice falls back to one plain notice without a DOM
ok 1912 - priority notice falls back to one plain notice without a DOM
  ---
  duration_ms: 0.625505
  ...
# Subtest: priority notice falls back to plain text when fragment rendering fails
ok 1913 - priority notice falls back to plain text when fragment rendering fails
  ---
  duration_ms: 0.373383
  ...
# Subtest: priority scheduling rolls inclusively and clamps a random value of one
ok 1914 - priority scheduling rolls inclusively and clamps a random value of one
  ---
  duration_ms: 0.513711
  ...
# Subtest: priority value rows preserve config order and expose labels ranges and current state
ok 1915 - priority value rows preserve config order and expose labels ranges and current state
  ---
  duration_ms: 0.785169
  ...
# Subtest: priority picker writes priority then rolled schedule in one guarded edit
ok 1916 - priority picker writes priority then rolled schedule in one guarded edit
  ---
  duration_ms: 12.97131
  ...
# Subtest: priority picker writes lowest priority with a wide rolled schedule
ok 1917 - priority picker writes lowest priority with a wide rolled schedule
  ---
  duration_ms: 2.401085
  ...
# Subtest: priority picker replaces both existing values without duplicating fields
ok 1918 - priority picker replaces both existing values without duplicating fields
  ---
  duration_ms: 2.39813
  ...
# Subtest: counted priority writes keep the rolled date right of the priority
ok 1919 - counted priority writes keep the rolled date right of the priority
  ---
  duration_ms: 5.522866
  ...
# Subtest: priority picker writes project priority and schedule inline atomically
ok 1920 - priority picker writes project priority and schedule inline atomically
  ---
  duration_ms: 5.438575
  ...
# Subtest: counted priority picker rolls an independent schedule for every task
ok 1921 - counted priority picker rolls an independent schedule for every task
  ---
  duration_ms: 4.491757
  ...
# Subtest: counted priority planning keeps project schedules inline
ok 1922 - counted priority planning keeps project schedules inline
  ---
  duration_ms: 0.953842
  ...
# Subtest: counted priority planning evaluates Blocked recovery per rolled date
ok 1923 - counted priority planning evaluates Blocked recovery per rolled date
  ---
  duration_ms: 1.013244
  ...
# Subtest: a counted priority batch writes one entry per task using each task's own previous level
ok 1924 - a counted priority batch writes one entry per task using each task's own previous level
  ---
  duration_ms: 0.825326
  ...
# Subtest: priority notice models carry the stored level value for the glyph
ok 1925 - priority notice models carry the stored level value for the glyph
  ---
  duration_ms: 0.424741
  ...
# Subtest: ledger priority mark lookup guards version and render
ok 1926 - ledger priority mark lookup guards version and render
  ---
  duration_ms: 0.154195
  ...
# Subtest: priority notice header reuses the shared mark when available
ok 1927 - priority notice header reuses the shared mark when available
  ---
  duration_ms: 0.361661
  ...
# Subtest: priority notice keeps the Lucide icon without a usable mark api
ok 1928 - priority notice keeps the Lucide icon without a usable mark api
  ---
  duration_ms: 1.165666
  ...
# Subtest: a counted priority batch skips a task whose rolled date equals its current date
ok 1929 - a counted priority batch skips a task whose rolled date equals its current date
  ---
  duration_ms: 4.352792
  ...
# Subtest: counted priority runtime aborts a stale session without rolling writes
ok 1930 - counted priority runtime aborts a stale session without rolling writes
  ---
  duration_ms: 1.859781
  ...
# Subtest: scheduled picker pins a priority roll only for configured current priorities
ok 1931 - scheduled picker pins a priority roll only for configured current priorities
  ---
  duration_ms: 14.729317
  ...
# Subtest: Ctrl+R replaces only the pinned priority roll and keeps it selected
ok 1932 - Ctrl+R replaces only the pinned priority roll and keeps it selected
  ---
  duration_ms: 6.117212
  ...
# Subtest: choosing a priority roll writes immediately with a deterministic reason instead of prompting
ok 1933 - choosing a priority roll writes immediately with a deterministic reason instead of prompting
  ---
  duration_ms: 7.71374
  ...
# Subtest: counted scheduled picker requires one shared configured priority
ok 1934 - counted scheduled picker requires one shared configured priority
  ---
  duration_ms: 5.999116
  ...
# Subtest: buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
ok 1935 - buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
  ---
  duration_ms: 2.896671
  ...
# Subtest: buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
ok 1936 - buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
  ---
  duration_ms: 0.287329
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
ok 1937 - buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
  ---
  duration_ms: 0.420132
  ...
# Subtest: buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
ok 1938 - buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
  ---
  duration_ms: 0.295975
  ...
# Subtest: buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
ok 1939 - buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
  ---
  duration_ms: 0.422587
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
ok 1940 - buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
  ---
  duration_ms: 0.174163
  ...
# Subtest: buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
ok 1941 - buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
  ---
  duration_ms: 0.226352
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
ok 1942 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
  ---
  duration_ms: 0.368344
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child work log under the project task
ok 1943 - buildProjectSeedFromChildBullets moves a direct-child work log under the project task
  ---
  duration_ms: 0.352523
  ...
# Subtest: buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
ok 1944 - buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
  ---
  duration_ms: 0.437585
  ...
# Subtest: buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
ok 1945 - buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
  ---
  duration_ms: 0.270988
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
ok 1946 - buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
  ---
  duration_ms: 0.185324
  ...
# Subtest: buildProjectSeedFromChildBullets moves an empty work log without forcing task output
ok 1947 - buildProjectSeedFromChildBullets moves an empty work log without forcing task output
  ---
  duration_ms: 0.145938
  ...
# Subtest: buildProjectSeedFromChildBullets moves both logs in source order without sorting by kind
ok 1948 - buildProjectSeedFromChildBullets moves both logs in source order without sorting by kind
  ---
  duration_ms: 0.139416
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
ok 1949 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
  ---
  duration_ms: 0.279895
  ...
# Subtest: parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
ok 1950 - parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
  ---
  duration_ms: 0.305474
  ...
# Subtest: parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
ok 1951 - parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
  ---
  duration_ms: 0.175705
  ...
# Subtest: parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
ok 1952 - parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
  ---
  duration_ms: 0.541855
  ...
# Subtest: normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
ok 1953 - normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
  ---
  duration_ms: 0.104269
  ...
# Subtest: parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
ok 1954 - parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
  ---
  duration_ms: 0.130699
  ...
# Subtest: formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
ok 1955 - formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
  ---
  duration_ms: 0.155256
  ...
# Subtest: insertProjectSectionNotes fills an empty existing section with a blank line then the notes
ok 1956 - insertProjectSectionNotes fills an empty existing section with a blank line then the notes
  ---
  duration_ms: 0.752016
  ...
# Subtest: insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
ok 1957 - insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
  ---
  duration_ms: 0.213879
  ...
# Subtest: insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
ok 1958 - insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
  ---
  duration_ms: 0.159214
  ...
# Subtest: insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
ok 1959 - insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
  ---
  duration_ms: 0.268242
  ...
# Subtest: insertProjectSectionNotes does not add a trailing newline when the original content had none
ok 1960 - insertProjectSectionNotes does not add a trailing newline when the original content had none
  ---
  duration_ms: 0.169875
  ...
# Subtest: insertProjectSectionNotes preserves CRLF line endings for an existing section
ok 1961 - insertProjectSectionNotes preserves CRLF line endings for an existing section
  ---
  duration_ms: 0.230159
  ...
# Subtest: insertProjectSectionNotes creates a new section using the document's CRLF line ending
ok 1962 - insertProjectSectionNotes creates a new section using the document's CRLF line ending
  ---
  duration_ms: 0.153654
  ...
# Subtest: buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
ok 1963 - buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
  ---
  duration_ms: 0.201194
  ...
# Subtest: buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
ok 1964 - buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
  ---
  duration_ms: 0.4454
  ...
# Subtest: buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
ok 1965 - buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
  ---
  duration_ms: 0.160406
  ...
# Subtest: buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
ok 1966 - buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
  ---
  duration_ms: 1.396396
  ...
# Subtest: project conversion accepts blocked sources and extracts their managed dependency child
ok 1967 - project conversion accepts blocked sources and extracts their managed dependency child
  ---
  duration_ms: 2.53976
  ...
# Subtest: project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
ok 1968 - project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
  ---
  duration_ms: 1.34616
  ...
# Subtest: buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
ok 1969 - buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
  ---
  duration_ms: 0.462443
  ...
# Subtest: buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
ok 1970 - buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
  ---
  duration_ms: 0.281948
  ...
# Subtest: buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
ok 1971 - buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
  ---
  duration_ms: 0.255628
  ...
# Subtest: insertProjectManagedLogLines preserves CRLF line endings
ok 1972 - insertProjectManagedLogLines preserves CRLF line endings
  ---
  duration_ms: 0.200392
  ...
# Subtest: findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
ok 1973 - findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
  ---
  duration_ms: 0.253775
  ...
# Subtest: getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
ok 1974 - getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
  ---
  duration_ms: 0.2568
  ...
# Subtest: getProjectFromTaskNoticeText reports moved log kinds in a fixed order
ok 1975 - getProjectFromTaskNoticeText reports moved log kinds in a fixed order
  ---
  duration_ms: 0.141941
  ...
# Subtest: forward conversion leaves the project Ready when only the source status was Blocked
ok 1976 - forward conversion leaves the project Ready when only the source status was Blocked
  ---
  duration_ms: 0.526916
  ...
# Subtest: buildTaskBlockFromProjectNote restores the worked example and round-trips
ok 1977 - buildTaskBlockFromProjectNote restores the worked example and round-trips
  ---
  duration_ms: 6.981672
  ...
# Subtest: project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
ok 1978 - project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
  ---
  duration_ms: 2.214198
  ...
# Subtest: buildTaskLineFromProjectNote preserves status, tags, and fields
ok 1979 - buildTaskLineFromProjectNote preserves status, tags, and fields
  ---
  duration_ms: 1.416274
  ...
# Subtest: getProjectReversalBlockId inverts the forward basename helper
ok 1980 - getProjectReversalBlockId inverts the forward basename helper
  ---
  duration_ms: 0.160577
  ...
# Subtest: formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
ok 1981 - formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
  ---
  duration_ms: 0.207245
  ...
# Subtest: splitProjectNoteForReversal treats TASKS as the task section and keeps section order
ok 1982 - splitProjectNoteForReversal treats TASKS as the task section and keeps section order
  ---
  duration_ms: 1.123355
  ...
# Subtest: indentProjectReversalLine preserves relative depth and drops blanks
ok 1983 - indentProjectReversalLine preserves relative depth and drops blanks
  ---
  duration_ms: 0.468425
  ...
# Subtest: buildTaskBlockFromProjectNote reports structure and frontmatter errors
ok 1984 - buildTaskBlockFromProjectNote reports structure and frontmatter errors
  ---
  duration_ms: 1.282299
  ...
# Subtest: buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
ok 1985 - buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
  ---
  duration_ms: 1.074702
  ...
# Subtest: rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
ok 1986 - rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
  ---
  duration_ms: 0.528198
  ...
# Subtest: collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
ok 1987 - collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
  ---
  duration_ms: 0.727739
  ...
# Subtest: getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
ok 1988 - getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
  ---
  duration_ms: 0.269294
  ...
# Subtest: convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
ok 1989 - convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
  ---
  duration_ms: 5.668946
  ...
# Subtest: project reversal recovers tagged residents when they leave a blocked project
ok 1990 - project reversal recovers tagged residents when they leave a blocked project
  ---
  duration_ms: 4.539068
  ...
# Subtest: convertProjectNoteToTask separates the restored task from a count-only parent section
ok 1991 - convertProjectNoteToTask separates the restored task from a count-only parent section
  ---
  duration_ms: 1.786321
  ...
# Subtest: createProjectNoteFromTask dispatches reverse only on a real ^prj line
ok 1992 - createProjectNoteFromTask dispatches reverse only on a real ^prj line
  ---
  duration_ms: 2.477712
  ...
# Subtest: convertProjectNoteToTask refusals leave every file untouched
ok 1993 - convertProjectNoteToTask refusals leave every file untouched
  ---
  duration_ms: 5.320811
  ...
# Subtest: planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
ok 1994 - planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
  ---
  duration_ms: 0.205853
  ...
# Subtest: convertProjectNoteToTask writes the parent first when it links to \#^prj
ok 1995 - convertProjectNoteToTask writes the parent first when it links to \#^prj
  ---
  duration_ms: 1.166368
  ...
# Subtest: convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
ok 1996 - convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
  ---
  duration_ms: 2.980181
  ...
# Subtest: convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
ok 1997 - convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
  ---
  duration_ms: 1.107444
  ...
# Subtest: convertProjectNoteToTask reports post-write failures without rolling back
ok 1998 - convertProjectNoteToTask reports post-write failures without rolling back
  ---
  duration_ms: 1.19904
  ...
# Subtest: convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
ok 1999 - convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
  ---
  duration_ms: 1.327195
  ...
# Subtest: convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
ok 2000 - convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
  ---
  duration_ms: 1.423939
  ...
# Subtest: v2 reading task opens its source_pdf in Highlights without writes
ok 2001 - v2 reading task opens its source_pdf in Highlights without writes
  ---
  duration_ms: 3.289101
  ...
# Subtest: every reading-task lane and \#REF casing opens
ok 2002 - every reading-task lane and \#REF casing opens
  ---
  duration_ms: 1.308178
  ...
# Subtest: v1 tracker resolves a PDF link or falls back to its own source_pdf
ok 2003 - v1 tracker resolves a PDF link or falls back to its own source_pdf
  ---
  duration_ms: 0.551443
  ...
# Subtest: plain, embedded, struck, and 🍅 Task Links resolve reading tasks
ok 2004 - plain, embedded, struck, and 🍅 Task Links resolve reading tasks
  ---
  duration_ms: 1.957097
  ...
# Subtest: bare managed embed in a reference note resolves its embedded task
ok 2005 - bare managed embed in a reference note resolves its embedded task
  ---
  duration_ms: 0.42978
  ...
# Subtest: ordinary lines, unresolved Task Links, fences, and outside focus delegate once
ok 2006 - ordinary lines, unresolved Task Links, fences, and outside focus delegate once
  ---
  duration_ms: 0.839844
  ...
# Subtest: identified reading tasks show notices without delegating
ok 2007 - identified reading tasks show notices without delegating
  ---
  duration_ms: 0.814175
  ...
# Subtest: unsafe source_pdf values are refused
ok 2008 - unsafe source_pdf values are refused
  ---
  duration_ms: 0.245229
  ...
# Subtest: bundle launch retries with the app name, and reports stderr on total failure
ok 2009 - bundle launch retries with the app name, and reports stderr on total failure
  ---
  duration_ms: 0.768057
  ...
# Subtest: off macOS shows the selected notice and managed ref-note prose delegates
ok 2010 - off macOS shows the selected notice and managed ref-note prose delegates
  ---
  duration_ms: 0.566832
  ...
# Subtest: pure helpers normalize and parse reference PDF paths
ok 2011 - pure helpers normalize and parse reference PDF paths
  ---
  duration_ms: 0.27275
  ...
# Subtest: command registration is custom-hotkey only
ok 2012 - command registration is custom-hotkey only
  ---
  duration_ms: 0.320542
  ...
# Subtest: nav api openReferencePdf hands a source_pdf to Highlights without version or vault writes
ok 2013 - nav api openReferencePdf hands a source_pdf to Highlights without version or vault writes
  ---
  duration_ms: 0.538208
  ...
# Subtest: nav api openReferencePdf settles to a reason instead of throwing
ok 2014 - nav api openReferencePdf settles to a reason instead of throwing
  ---
  duration_ms: 0.346943
  ...
# Subtest: reading tasks read with the book prefix, plain tasks unchanged
ok 2015 - reading tasks read with the book prefix, plain tasks unchanged
  ---
  duration_ms: 1.321684
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 2016 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.245669
  ...
# Subtest: picker rows carry the book prefix in displayText
ok 2017 - picker rows carry the book prefix in displayText
  ---
  duration_ms: 0.667695
  ...
# Subtest: managed reference rename modal and submit are refused
ok 2018 - managed reference rename modal and submit are refused
  ---
  duration_ms: 1.638058
  ...
# Subtest: legacy ref notes and non-ref notes still rename
ok 2019 - legacy ref notes and non-ref notes still rename
  ---
  duration_ms: 1.263523
  ...
# Subtest: managed reference predicate checks path and non-empty source_pdf
ok 2020 - managed reference predicate checks path and non-empty source_pdf
  ---
  duration_ms: 0.287129
  ...
# Subtest: planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
ok 2021 - planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
  ---
  duration_ms: 5.045845
  ...
# Subtest: planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
ok 2022 - planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
  ---
  duration_ms: 1.753218
  ...
# Subtest: runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
ok 2023 - runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
  ---
  duration_ms: 4.562082
  ...
# Subtest: runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
ok 2024 - runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
  ---
  duration_ms: 3.282999
  ...
# Subtest: runtime: no daily note today still writes the schedule with no Pomodoro chip
ok 2025 - runtime: no daily note today still writes the schedule with no Pomodoro chip
  ---
  duration_ms: 0.671161
  ...
# Subtest: runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
ok 2026 - runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
  ---
  duration_ms: 1.326594
  ...
# Subtest: runtime: vault.process throwing during the daily-note write is reported without throwing
ok 2027 - runtime: vault.process throwing during the daily-note write is reported without throwing
  ---
  duration_ms: 0.952178
  ...
# Subtest: runtime: the daily note open in another editor is written through that editor in its own transaction
ok 2028 - runtime: the daily note open in another editor is written through that editor in its own transaction
  ---
  duration_ms: 1.482491
  ...
# Subtest: runtime: re-running the same deferral gesture is idempotent
ok 2029 - runtime: re-running the same deferral gesture is idempotent
  ---
  duration_ms: 0.771734
  ...
# Subtest: runtime: a counted scheduled batch prunes exactly the targets that land on a future date
ok 2030 - runtime: a counted scheduled batch prunes exactly the targets that land on a future date
  ---
  duration_ms: 2.935766
  ...
# Subtest: runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
ok 2031 - runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
  ---
  duration_ms: 2.48741
  ...
# Subtest: runtime: the source note being today's daily note folds the prune into a single editor transaction
ok 2032 - runtime: the source note being today's daily note folds the prune into a single editor transaction
  ---
  duration_ms: 0.725385
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: bare future scheduled writes block only real supported open inline tasks
ok 2033 - bare future scheduled writes block only real supported open inline tasks
  ---
  duration_ms: 5.845412
  ...
# Subtest: single runtime transclusion toggle preserves viewport in one line transaction
ok 2034 - single runtime transclusion toggle preserves viewport in one line transaction
  ---
  duration_ms: 2.145787
  ...
# Subtest: same-file runtime toggle changes only markers, never fields or statuses
ok 2035 - same-file runtime toggle changes only markers, never fields or statuses
  ---
  duration_ms: 0.731848
  ...
# Subtest: pure toggle leaves a cursor moved during the toggle where it landed
ok 2036 - pure toggle leaves a cursor moved during the toggle where it landed
  ---
  duration_ms: 0.301946
  ...
# Subtest: counted runtime transclusion toggle preserves viewport and caret
ok 2037 - counted runtime transclusion toggle preserves viewport and caret
  ---
  duration_ms: 0.831447
  ...
# Subtest: counted property runtime uses one transaction and preserves caret and viewport
ok 2038 - counted property runtime uses one transaction and preserves caret and viewport
  ---
  duration_ms: 3.567453
  ...
# Subtest: bare due schedule recovery is guarded and can change only task status
ok 2039 - bare due schedule recovery is guarded and can change only task status
  ---
  duration_ms: 2.370267
  ...
# Subtest: counted due recovery applies Ready Next and In Progress in one transaction
ok 2040 - counted due recovery applies Ready Next and In Progress in one transaction
  ---
  duration_ms: 4.439067
  ...
# Subtest: scheduled recovery aborts after an asynchronous source change
ok 2041 - scheduled recovery aborts after an asynchronous source change
  ---
  duration_ms: 0.826088
  ...
# Subtest: counted property runtime aborts a stale batch without a transaction
ok 2042 - counted property runtime aborts a stale batch without a transaction
  ---
  duration_ms: 0.48659
  ...
# Subtest: counted project scheduling writes an inline date and blocks tagged residents
ok 2043 - counted project scheduling writes an inline date and blocks tagged residents
  ---
  duration_ms: 2.596899
  ...
# Subtest: future project scheduling prunes resident links and an emptied Pomodoro
ok 2044 - future project scheduling prunes resident links and an emptied Pomodoro
  ---
  duration_ms: 2.885169
  ...
# Subtest: single project scheduling recovers due residents through the gate
ok 2045 - single project scheduling recovers due residents through the gate
  ---
  duration_ms: 1.837579
  ...
# Subtest: single project schedule deletion removes propagated copies and recovers
ok 2046 - single project schedule deletion removes propagated copies and recovers
  ---
  duration_ms: 1.562624
  ...
# Subtest: formatPriorityRollScheduleReason covers all four shapes
ok 2047 - formatPriorityRollScheduleReason covers all four shapes
  ---
  duration_ms: 1.268162
  ...
# Subtest: the priority-roll picker row keeps range detail and stores the exact roll
ok 2048 - the priority-roll picker row keeps range detail and stores the exact roll
  ---
  duration_ms: 0.584466
  ...
# Subtest: buildPriorityRollScheduleLog returns null when the roll does not move the date
ok 2049 - buildPriorityRollScheduleLog returns null when the roll does not move the date
  ---
  duration_ms: 0.680419
  ...
# Subtest: getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
ok 2050 - getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
  ---
  duration_ms: 0.755703
  ...
# Subtest: a priority roll onto the current date writes the date but no log
ok 2051 - a priority roll onto the current date writes the date but no log
  ---
  duration_ms: 14.581073
  ...
# Subtest: a typed reason on an unchanged date is still written
ok 2052 - a typed reason on an unchanged date is still written
  ---
  duration_ms: 0.774169
  ...
# Subtest: schedule log bullet formatting and parsing round-trip with and without a previous value
ok 2053 - schedule log bullet formatting and parsing round-trip with and without a previous value
  ---
  duration_ms: 0.940866
  ...
# Subtest: formatScheduleLogEntryText renders entry text without indent or marker
ok 2054 - formatScheduleLogEntryText renders entry text without indent or marker
  ---
  duration_ms: 0.127273
  ...
# Subtest: schedule reason text normalization trims, collapses whitespace, and flags inline fields
ok 2055 - schedule reason text normalization trims, collapses whitespace, and flags inline fields
  ---
  duration_ms: 0.351631
  ...
# Subtest: findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
ok 2056 - findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
  ---
  duration_ms: 0.720305
  ...
# Subtest: getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
ok 2057 - getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
  ---
  duration_ms: 0.231051
  ...
# Subtest: planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
ok 2058 - planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
  ---
  duration_ms: 0.419801
  ...
# Subtest: planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
ok 2059 - planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
  ---
  duration_ms: 0.206965
  ...
# Subtest: planScheduleLogEntry uses the fallback only when a marker exists
ok 2060 - planScheduleLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.201976
  ...
# Subtest: a typed reason wins over the fallback
ok 2061 - a typed reason wins over the fallback
  ---
  duration_ms: 0.153383
  ...
# Subtest: the fallback is suppressed on an unchanged date
ok 2062 - the fallback is suppressed on an unchanged date
  ---
  duration_ms: 0.114469
  ...
# Subtest: no reason and no fallback still guards empty-reason
ok 2063 - no reason and no fallback still guards empty-reason
  ---
  duration_ms: 0.096314
  ...
# Subtest: getScheduleLogWriteOutcome maps plan outcomes for writers
ok 2064 - getScheduleLogWriteOutcome maps plan outcomes for writers
  ---
  duration_ms: 0.132903
  ...
# Subtest: hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
ok 2065 - hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
  ---
  duration_ms: 0.112464
  ...
# Subtest: counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
ok 2066 - counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
  ---
  duration_ms: 1.724443
  ...
# Subtest: empty reason through the counted planner writes no schedule log entries
ok 2067 - empty reason through the counted planner writes no schedule log entries
  ---
  duration_ms: 0.539651
  ...
# Subtest: a counted scheduled session logs only the tasks that already keep a log
ok 2068 - a counted scheduled session logs only the tasks that already keep a log
  ---
  duration_ms: 0.584576
  ...
# Subtest: the counted notice wording distinguishes a fallback batch from a typed-reason batch
ok 2069 - the counted notice wording distinguishes a fallback batch from a typed-reason batch
  ---
  duration_ms: 3.725614
  ...
# Subtest: setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
ok 2070 - setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
  ---
  duration_ms: 0.326173
  ...
# Subtest: setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
ok 2071 - setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
  ---
  duration_ms: 2.763427
  ...
# Subtest: priority bullet property config normalizes frozen levels and preserves existing shapes
ok 2072 - priority bullet property config normalizes frozen levels and preserves existing shapes
  ---
  duration_ms: 2.129636
  ...
# Subtest: priority bullet property config rejects each invalid schema category once
ok 2073 - priority bullet property config rejects each invalid schema category once
  ---
  duration_ms: 0.961527
  ...
# Subtest: project scheduling targets the inline ^prj field
ok 2074 - project scheduling targets the inline ^prj field
  ---
  duration_ms: 1.808714
  ...
# Subtest: local task properties are addable only on valid tasks but invalid metadata stays removable
ok 2075 - local task properties are addable only on valid tasks but invalid metadata stays removable
  ---
  duration_ms: 0.299071
  ...
# Subtest: dependency parent write validation rejects stale, Pomodoro, and fenced parents
ok 2076 - dependency parent write validation rejects stale, Pomodoro, and fenced parents
  ---
  duration_ms: 0.545041
  ...
# Subtest: counted property targets mean current plus N real tasks without wrapping
ok 2077 - counted property targets mean current plus N real tasks without wrapping
  ---
  duration_ms: 0.735455
  ...
# Subtest: counted property metadata distinguishes absent, common, and mixed values
ok 2078 - counted property metadata distinguishes absent, common, and mixed values
  ---
  duration_ms: 0.658057
  ...
# Subtest: counted priority metadata reports labels for common and mixed values
ok 2079 - counted priority metadata reports labels for common and mixed values
  ---
  duration_ms: 0.532026
  ...
# Subtest: counted scheduled planning updates the motivating three tasks atomically
ok 2080 - counted scheduled planning updates the motivating three tasks atomically
  ---
  duration_ms: 2.337844
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: project schedule validation accepts only real YYYY-MM-DD dates
ok 2081 - project schedule validation accepts only real YYYY-MM-DD dates
  ---
  duration_ms: 1.098498
  ...
# Subtest: source task schedule is extracted without losing task metadata
ok 2082 - source task schedule is extracted without losing task metadata
  ---
  duration_ms: 1.545531
  ...
# Subtest: source task schedule errors are focused and ambiguous fields fail
ok 2083 - source task schedule errors are focused and ambiguous fields fail
  ---
  duration_ms: 0.407148
  ...
# Subtest: project creation frontmatter never stores the task schedule
ok 2084 - project creation frontmatter never stores the task schedule
  ---
  duration_ms: 0.184282
  ...
# Subtest: future schedule labels use local date-only boundaries
ok 2085 - future schedule labels use local date-only boundaries
  ---
  duration_ms: 0.70156
  ...
# Subtest: scheduled recovery selects current and newest earlier daily across gaps
ok 2086 - scheduled recovery selects current and newest earlier daily across gaps
  ---
  duration_ms: 0.681873
  ...
# Subtest: scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
ok 2087 - scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
  ---
  duration_ms: 8.881119
  ...
# Subtest: scheduled recovery defers incompatible status settings and ambiguous identities
ok 2088 - scheduled recovery defers incompatible status settings and ambiguous identities
  ---
  duration_ms: 0.442565
  ...
# Subtest: scheduled recovery honors custom open and closed Tasks status types
ok 2089 - scheduled recovery honors custom open and closed Tasks status types
  ---
  duration_ms: 0.622579
  ...
# Subtest: scheduled recovery honors the configured Tasks global filter
ok 2090 - scheduled recovery honors the configured Tasks global filter
  ---
  duration_ms: 0.533559
  ...
# Subtest: child picker schedule metadata reads the inline ^prj date
ok 2091 - child picker schedule metadata reads the inline ^prj date
  ---
  duration_ms: 0.909617
  ...
# Subtest: task move destination schedule hydration reads cached ^prj content
ok 2092 - task move destination schedule hydration reads cached ^prj content
  ---
  duration_ms: 0.480798
  ...
# Subtest: project lifecycle task classification requires unfenced \#task with trailing ^prj
ok 2093 - project lifecycle task classification requires unfenced \#task with trailing ^prj
  ---
  duration_ms: 0.171287
  ...
# Subtest: valid Obsidian tasks require a standalone \#task checkbox in real note content
ok 2094 - valid Obsidian tasks require a standalone \#task checkbox in real note content
  ---
  duration_ms: 0.145939
  ...
# Subtest: choosing a scheduled date enters the combined review without writing anything
ok 2095 - choosing a scheduled date enters the combined review without writing anything
  ---
  duration_ms: 11.485623
  ...
# Subtest: choosing a priority level does not enter the schedule review
ok 2096 - choosing a priority level does not enter the schedule review
  ---
  duration_ms: 9.006852
  ...
# Subtest: confirming an empty reason on a task with an existing schedule log appends an unexplained entry
ok 2097 - confirming an empty reason on a task with an existing schedule log appends an unexplained entry
  ---
  duration_ms: 7.26299
  ...
# Subtest: confirming an empty reason on a task with no schedule log writes only the date
ok 2098 - confirming an empty reason on a task with no schedule log writes only the date
  ---
  duration_ms: 3.50364
  ...
# Subtest: review stage getFilteredItems always returns exactly one synthetic preview item
ok 2099 - review stage getFilteredItems always returns exactly one synthetic preview item
  ---
  duration_ms: 1.866124
  ...
# Subtest: the review preview row previews the entry it will write
ok 2100 - the review preview row previews the entry it will write
  ---
  duration_ms: 3.56608
  ...
# Subtest: the review footer flips between Skip optional logs and Apply schedule as the Reason changes
ok 2101 - the review footer flips between Skip optional logs and Apply schedule as the Reason changes
  ---
  duration_ms: 2.270025
  ...
# Subtest: closing the picker during the review clears pending schedule state and writes nothing
ok 2102 - closing the picker during the review clears pending schedule state and writes nothing
  ---
  duration_ms: 1.431985
  ...
# Subtest: scheduling Work Log eligibility requires Pending or Next \#task lines
ok 2103 - scheduling Work Log eligibility requires Pending or Next \#task lines
  ---
  duration_ms: 1.661764
  ...
# Subtest: single Pending explicit date opens one review and writes both logs
ok 2104 - single Pending explicit date opens one review and writes both logs
  ---
  duration_ms: 18.518495
  ...
# Subtest: single Next blank and whitespace summaries schedule without a Work Log
ok 2105 - single Next blank and whitespace summaries schedule without a Work Log
  ---
  duration_ms: 6.37308
  ...
# Subtest: Escape at the review writes nothing, with or without typed text
ok 2106 - Escape at the review writes nothing, with or without typed text
  ---
  duration_ms: 5.484844
  ...
# Subtest: Ready and Blocked explicit dates review the Reason with no Work summary field
ok 2107 - Ready and Blocked explicit dates review the Reason with no Work summary field
  ---
  duration_ms: 3.912291
  ...
# Subtest: future scheduling on Pending marks Blocked but still writes the Work Log
ok 2108 - future scheduling on Pending marks Blocked but still writes the Work Log
  ---
  duration_ms: 2.230129
  ...
# Subtest: today date on Pending still offers the Work Log
ok 2109 - today date on Pending still offers the Work Log
  ---
  duration_ms: 3.867785
  ...
# Subtest: priority pick on Pending freezes its roll and offers the Work Log
ok 2110 - priority pick on Pending freezes its roll and offers the Work Log
  ---
  duration_ms: 6.445158
  ...
# Subtest: counted mixed statuses share one summary only on Pending and Next
ok 2111 - counted mixed statuses share one summary only on Pending and Next
  ---
  duration_ms: 11.423043
  ...
# Subtest: counted planner composes Schedule and Work Logs bottom-up above later targets
ok 2112 - counted planner composes Schedule and Work Logs bottom-up above later targets
  ---
  duration_ms: 1.377992
  ...
# Subtest: counted planner writes a Work Log even when the date is unchanged
ok 2113 - counted planner writes a Work Log even when the date is unchanged
  ---
  duration_ms: 0.467172
  ...
# Subtest: scheduling Work Log ownership keeps nested logs and CRLF endings
ok 2114 - scheduling Work Log ownership keeps nested logs and CRLF endings
  ---
  duration_ms: 1.106233
  ...
# Subtest: scheduling Work Log warns on :: and preserves Markdown
ok 2115 - scheduling Work Log warns on :: and preserves Markdown
  ---
  duration_ms: 3.184942
  ...
# Subtest: stale task while reviewing refuses with no scheduling or log writes
ok 2116 - stale task while reviewing refuses with no scheduling or log writes
  ---
  duration_ms: 2.278511
  ...
# Subtest: scheduling prompts never leak into lane or cancel stages
ok 2117 - scheduling prompts never leak into lane or cancel stages
  ---
  duration_ms: 2.754921
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: Pomodoro-marked links are not managed dependency bullets
ok 2118 - Pomodoro-marked links are not managed dependency bullets
  ---
  duration_ms: 1.329469
  ...
# Subtest: deleting inline scheduled metadata recovers Blocked targets by snapshot rank
ok 2119 - deleting inline scheduled metadata recovers Blocked targets by snapshot rank
  ---
  duration_ms: 3.464837
  ...
# Subtest: counted future scheduling blocks only supported open inline task statuses
ok 2120 - counted future scheduling blocks only supported open inline task statuses
  ---
  duration_ms: 1.616637
  ...
# Subtest: counted property planning rejects any stale source with no partial result
ok 2121 - counted property planning rejects any stale source with no partial result
  ---
  duration_ms: 0.264225
  ...
# Subtest: counted project scheduling writes the ^prj inline date and blocks tagged residents
ok 2122 - counted project scheduling writes the ^prj inline date and blocks tagged residents
  ---
  duration_ms: 1.721237
  ...
# Subtest: moving a project schedule earlier replaces only exact old-date copies
ok 2123 - moving a project schedule earlier replaces only exact old-date copies
  ---
  duration_ms: 0.375377
  ...
# Subtest: future project schedules block every open resident and consume review status
ok 2124 - future project schedules block every open resident and consume review status
  ---
  duration_ms: 0.579035
  ...
# Subtest: due project dates recover residents through the gate and write unblocked markers
ok 2125 - due project dates recover residents through the gate and write unblocked markers
  ---
  duration_ms: 0.669879
  ...
# Subtest: schedule deletion removes only exact project-date copies and recovers residents
ok 2126 - schedule deletion removes only exact project-date copies and recovers residents
  ---
  duration_ms: 0.952048
  ...
# Subtest: dependency lines render one canonical Depends-On line per parent
ok 2127 - dependency lines render one canonical Depends-On line per parent
  ---
  duration_ms: 0.644741
  ...
# Subtest: dependency IDs encode root and nested Markdown paths deterministically
ok 2128 - dependency IDs encode root and nested Markdown paths deterministically
  ---
  duration_ms: 0.951648
  ...
# Subtest: prompted block IDs truthfully replace legacy id fields
ok 2129 - prompted block IDs truthfully replace legacy id fields
  ---
  duration_ms: 0.162089
  ...
# Subtest: dependency navigation identity includes note path and folds legacy children
ok 2130 - dependency navigation identity includes note path and folds legacy children
  ---
  duration_ms: 0.829845
  ...
# Subtest: retired dependency bullets are excluded from single and counted toggles
ok 2131 - retired dependency bullets are excluded from single and counted toggles
  ---
  duration_ms: 1.143203
  ...
# Subtest: dependsOn replacement accepts spaces around field name and separator
ok 2132 - dependsOn replacement accepts spaces around field name and separator
  ---
  duration_ms: 0.262641
  ...
# Subtest: task status helpers keep Blocked open but rankless
ok 2133 - task status helpers keep Blocked open but rankless
  ---
  duration_ms: 0.279003
  ...
# Subtest: a due project date with only closed Depends-On history strips the tag
ok 2134 - a due project date with only closed Depends-On history strips the tag
  ---
  duration_ms: 0.729202
  ...
# Subtest: Ctrl+D with only closed Depends-On history strips the tag
ok 2135 - Ctrl+D with only closed Depends-On history strips the tag
  ---
  duration_ms: 0.368935
  ...
# Subtest: Ctrl+D with an open Depends-On link remaining keeps the tag
ok 2136 - Ctrl+D with an open Depends-On link remaining keeps the tag
  ---
  duration_ms: 0.280696
  ...
# Subtest: counted ^prj schedule sessions write [unblocked::] when the writer is passed
ok 2137 - counted ^prj schedule sessions write [unblocked::] when the writer is passed
  ---
  duration_ms: 0.464597
  ...
# Subtest: a due project date keeps the tag while ^prj holds Depends-On links
ok 2138 - a due project date keeps the tag while ^prj holds Depends-On links
  ---
  duration_ms: 0.317407
  ...
# Subtest: a due project date strips the tag while a resident with its own reason stays Blocked
ok 2139 - a due project date strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.320683
  ...
# Subtest: Ctrl+D strips the tag while a resident with its own reason stays Blocked
ok 2140 - Ctrl+D strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.410534
  ...
# Subtest: counted scheduled deletes recover with [unblocked::] when the writer is passed
ok 2141 - counted scheduled deletes recover with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.257211
  ...
# Subtest: section-header navigation moves normally and cycles at boundaries
ok 2142 - section-header navigation moves normally and cycles at boundaries
  ---
  duration_ms: 1.777294
  ...
# Subtest: section-header navigation wraps from beyond document boundaries
ok 2143 - section-header navigation wraps from beyond document boundaries
  ---
  duration_ms: 0.175855
  ...
# Subtest: section-header navigation handles single-header and no-header notes
ok 2144 - section-header navigation handles single-header and no-header notes
  ---
  duration_ms: 0.197717
  ...
# Subtest: open-task navigation scan includes Ready In Progress and Next and excludes Blocked
ok 2145 - open-task navigation scan includes Ready In Progress and Next and excludes Blocked
  ---
  duration_ms: 0.514042
  ...
# Subtest: open-task navigation keeps existing Pomodoro ledger targets
ok 2146 - open-task navigation keeps existing Pomodoro ledger targets
  ---
  duration_ms: 0.501758
  ...
# Subtest: next and previous jumps skip Blocked tasks and wrap to an allowed task
ok 2147 - next and previous jumps skip Blocked tasks and wrap to an allowed task
  ---
  duration_ms: 0.305343
  ...
# Subtest: blocked-only notes and a sole current allowed task have no jump target
ok 2148 - blocked-only notes and a sole current allowed task have no jump target
  ---
  duration_ms: 0.166057
  ...
# Subtest: counted open-task jumps select the Nth eligible target and wrap modulo the list
ok 2149 - counted open-task jumps select the Nth eligible target and wrap modulo the list
  ---
  duration_ms: 0.270998
  ...
# Subtest: counted open-task jumps keep sole-target and invalid-repeat behavior
ok 2150 - counted open-task jumps keep sole-target and invalid-repeat behavior
  ---
  duration_ms: 0.421395
  ...
# Subtest: tab pin Vim action registers once and toggles only the active leaf once
ok 2151 - tab pin Vim action registers once and toggles only the active leaf once
  ---
  duration_ms: 3.263622
  ...
# Subtest: tab pin toggle fails safely without a supported active leaf
ok 2152 - tab pin toggle fails safely without a supported active leaf
  ---
  duration_ms: 0.23045
  ...
# Subtest: close tabs left preserves pinned sibling tabs and refocuses active tab
ok 2153 - close tabs left preserves pinned sibling tabs and refocuses active tab
  ---
  duration_ms: 0.858209
  ...
# Subtest: close tabs right preserves pinned siblings and ignores the left side
ok 2154 - close tabs right preserves pinned siblings and ignores the left side
  ---
  duration_ms: 0.376639
  ...
# Subtest: close other tabs preserves pinned siblings on both sides
ok 2155 - close other tabs preserves pinned siblings on both sides
  ---
  duration_ms: 0.266759
  ...
# Subtest: close sibling tabs is a silent no-op when the scoped range is all pinned
ok 2156 - close sibling tabs is a silent no-op when the scoped range is all pinned
  ---
  duration_ms: 0.171588
  ...
# Subtest: close sibling tabs honors every pinned leaf representation
ok 2157 - close sibling tabs honors every pinned leaf representation
  ---
  duration_ms: 0.239337
  ...
# Subtest: close sibling tabs treats throwing view state as unpinned
ok 2158 - close sibling tabs treats throwing view state as unpinned
  ---
  duration_ms: 0.34032
  ...
# Subtest: tab pin Vim registration retries after adapter availability
ok 2159 - tab pin Vim registration retries after adapter availability
  ---
  duration_ms: 0.812702
  ...
# Subtest: isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
ok 2160 - isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
  ---
  duration_ms: 4.233695
  ...
# Subtest: isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
ok 2161 - isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
  ---
  duration_ms: 0.65467
  ...
# Subtest: isPomodoroTaskLinkLine refuses Depends-On lines and prose links
ok 2162 - isPomodoroTaskLinkLine refuses Depends-On lines and prose links
  ---
  duration_ms: 0.223848
  ...
# Subtest: decideTaskLinkLaneMode starts when any target is Next
ok 2163 - decideTaskLinkLaneMode starts when any target is Next
  ---
  duration_ms: 0.180765
  ...
# Subtest: taskLinkLaneRefusalFor renders every D5 refusal
ok 2164 - taskLinkLaneRefusalFor renders every D5 refusal
  ---
  duration_ms: 0.156539
  ...
# Subtest: planTaskLinkLaneBatch starts Next targets and leaves the rest alone
ok 2165 - planTaskLinkLaneBatch starts Next targets and leaves the rest alone
  ---
  duration_ms: 1.234368
  ...
# Subtest: planTaskLinkLaneBatch pauses with one shared Work Log entry
ok 2166 - planTaskLinkLaneBatch pauses with one shared Work Log entry
  ---
  duration_ms: 0.75432
  ...
# Subtest: planTaskLinkLaneBatch applies the freshness stamp last
ok 2167 - planTaskLinkLaneBatch applies the freshness stamp last
  ---
  duration_ms: 0.301306
  ...
# Subtest: planTaskLinkLaneBatch dedupes lines and refuses stale preimages
ok 2168 - planTaskLinkLaneBatch dedupes lines and refuses stale preimages
  ---
  duration_ms: 0.487311
  ...
# Subtest: buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
ok 2169 - buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
  ---
  duration_ms: 0.672324
  ...
# Subtest: taskLinkLanePromptState drives the Move to Next prompt
ok 2170 - taskLinkLanePromptState drives the Move to Next prompt
  ---
  duration_ms: 0.255718
  ...
# Subtest: TaskLinkLanePromptModal submits, previews live, and cancels silently
ok 2171 - TaskLinkLanePromptModal submits, previews live, and cancels silently
  ---
  duration_ms: 1.507228
  ...
# Subtest: TaskLinkLanePromptModal renders the batch context card
ok 2172 - TaskLinkLanePromptModal renders the batch context card
  ---
  duration_ms: 0.356661
  ...
# Subtest: findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
ok 2173 - findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
  ---
  duration_ms: 0.2984
  ...
# Subtest: L1: toggle starts a Next link, stamps, hints, and notices
ok 2174 - L1: toggle starts a Next link, stamps, hints, and notices
  ---
  duration_ms: 3.364935
  ...
# Subtest: L2/L3: toggle pauses through the prompt, logging one shared entry
ok 2175 - L2/L3: toggle pauses through the prompt, logging one shared entry
  ---
  duration_ms: 12.254802
  ...
# Subtest: L4: cancelling the prompt writes nothing and shows no Notice
ok 2176 - L4: cancelling the prompt writes nothing and shows no Notice
  ---
  duration_ms: 1.040136
  ...
# Subtest: L5: both directions run the same toggle twice for a round trip
ok 2177 - L5: both directions run the same toggle twice for a round trip
  ---
  duration_ms: 1.772886
  ...
# Subtest: L6: Ready, Blocked, done, and cancelled targets are refused
ok 2178 - L6: Ready, Blocked, done, and cancelled targets are refused
  ---
  duration_ms: 1.802542
  ...
# Subtest: L6: missing targets keep the existing resolver error
ok 2179 - L6: missing targets keep the existing resolver error
  ---
  duration_ms: 0.258634
  ...
# Subtest: L7: a counted start flips every Next sibling and leaves In Progress alone
ok 2180 - L7: a counted start flips every Next sibling and leaves In Progress alone
  ---
  duration_ms: 0.565419
  ...
# Subtest: L8: a counted pause prompts once and skips Blocked with a count
ok 2181 - L8: a counted pause prompts once and skips Blocked with a count
  ---
  duration_ms: 2.055225
  ...
# Subtest: L9: an over-long count clamps at the entry end without error
ok 2182 - L9: an over-long count clamps at the entry end without error
  ---
  duration_ms: 0.637527
  ...
# Subtest: L10: a closed-entry history line toggles the task and keeps the line
ok 2183 - L10: a closed-entry history line toggles the task and keeps the line
  ---
  duration_ms: 0.320021
  ...
# Subtest: L11: a target edited while the prompt is open refuses stale
ok 2184 - L11: a target edited while the prompt is open refuses stale
  ---
  duration_ms: 1.378542
  ...
# Subtest: L12: an embedded Pomodoro link takes the two-state toggle
ok 2185 - L12: an embedded Pomodoro link takes the two-state toggle
  ---
  duration_ms: 0.411886
  ...
# Subtest: L14: the same task linked twice in a batch is written once
ok 2186 - L14: the same task linked twice in a batch is written once
  ---
  duration_ms: 1.144746
  ...
# Subtest: L15: a second toggle while one is in flight is swallowed as busy
ok 2187 - L15: a second toggle while one is in flight is swallowed as busy
  ---
  duration_ms: 0.675981
  ...
# Subtest: toggle on a non-link line refuses without writing
ok 2188 - toggle on a non-link line refuses without writing
  ---
  duration_ms: 0.274154
  ...
# Subtest: api.taskLinkLane is a frozen v1 namespace that never throws
ok 2189 - api.taskLinkLane is a frozen v1 namespace that never throws
  ---
  duration_ms: 0.924415
  ...
# Subtest: the progressMarks hint is a no-op without the ledger-tools api
ok 2190 - the progressMarks hint is a no-op without the ledger-tools api
  ---
  duration_ms: 0.311985
  ...
# Subtest: task move records one Vim jump and round-trips without extra writes
ok 2191 - task move records one Vim jump and round-trips without extra writes
  ---
  duration_ms: 9.515721
  ...
# Subtest: counted task move records a single jump to the first moved task
ok 2192 - counted task move records a single jump to the first moved task
  ---
  duration_ms: 1.484645
  ...
# Subtest: deferred task landing re-anchors and records the resolved cursor once
ok 2193 - deferred task landing re-anchors and records the resolved cursor once
  ---
  duration_ms: 6.279972
  ...
# Subtest: failed task move preserves seeded history including the forward branch
ok 2194 - failed task move preserves seeded history including the forward branch
  ---
  duration_ms: 0.538067
  ...
# Subtest: post-commit open failure keeps the move committed with no jump
ok 2195 - post-commit open failure keeps the move committed with no jump
  ---
  duration_ms: 1.129497
  ...
# Subtest: a newer move supersedes a pending landing without stale placement
ok 2196 - a newer move supersedes a pending landing without stale placement
  ---
  duration_ms: 10.863415
  ...
# Subtest: shared destination helper without a move context records no jump
ok 2197 - shared destination helper without a move context records no jump
  ---
  duration_ms: 0.813563
  ...
# Subtest: task moves carry the Depends-On line and repath stranded same-note links
ok 2198 - task moves carry the Depends-On line and repath stranded same-note links
  ---
  duration_ms: 5.420511
  ...
# Subtest: task moves keep pathless links when the target moves along
ok 2199 - task moves keep pathless links when the target moves along
  ---
  duration_ms: 0.907112
  ...
# Subtest: counted task moves discover movable tasks without wrapping or examples
ok 2200 - counted task moves discover movable tasks without wrapping or examples
  ---
  duration_ms: 0.896742
  ...
# Subtest: task move ranges preserve quoted subtrees and collapse overlapping selections
ok 2201 - task move ranges preserve quoted subtrees and collapse overlapping selections
  ---
  duration_ms: 0.509843
  ...
# Subtest: task move removal handles disjoint ranges, blank seams, and CRLF
ok 2202 - task move removal handles disjoint ranges, blank seams, and CRLF
  ---
  duration_ms: 0.363163
  ...
# Subtest: task move destinations include areas and only open projects
ok 2203 - task move destinations include areas and only open projects
  ---
  duration_ms: 0.6076
  ...
# Subtest: moves into a blocked project leave closed tagged lines alone
ok 2204 - moves into a blocked project leave closed tagged lines alone
  ---
  duration_ms: 2.34081
  ...
# Subtest: moves into a blocked project promote open prerequisites to the moved lane
ok 2205 - moves into a blocked project promote open prerequisites to the moved lane
  ---
  duration_ms: 2.093127
  ...
# Subtest: task move insertion preserves exact task and section spacing
ok 2206 - task move insertion preserves exact task and section spacing
  ---
  duration_ms: 3.951686
  ...
# Subtest: task move planning migrates identities and links across every affected note
ok 2207 - task move planning migrates identities and links across every affected note
  ---
  duration_ms: 6.057858
  ...
# Subtest: task move planning exposes a destination anchor for area destinations and counted moves
ok 2208 - task move planning exposes a destination anchor for area destinations and counted moves
  ---
  duration_ms: 1.132373
  ...
# Subtest: task move into a blocked project tags the moved task and consumes today's live Pomodoro link
ok 2209 - task move into a blocked project tags the moved task and consumes today's live Pomodoro link
  ---
  duration_ms: 4.543477
  ...
# Subtest: task move out of a blocked project recovers through the shared gate and writes the unblocked mark
ok 2210 - task move out of a blocked project recovers through the shared gate and writes the unblocked mark
  ---
  duration_ms: 4.737386
  ...
# Subtest: move promotion walks through a ^prj target without raising it
ok 2211 - move promotion walks through a ^prj target without raising it
  ---
  duration_ms: 2.370447
  ...
# Subtest: move promotion walks through a [?] ^prj to its open prerequisite
ok 2212 - move promotion walks through a [?] ^prj to its open prerequisite
  ---
  duration_ms: 1.039204
  ...
# Subtest: move promotion uses each open task's own lane, not the strongest moved lane
ok 2213 - move promotion uses each open task's own lane, not the strongest moved lane
  ---
  duration_ms: 1.188008
  ...
# Subtest: move promotion skips Depends-On lines of closed tasks
ok 2214 - move promotion skips Depends-On lines of closed tasks
  ---
  duration_ms: 0.774098
  ...
# Subtest: task move planning rejects destination collisions and malformed identities
ok 2215 - task move planning rejects destination collisions and malformed identities
  ---
  duration_ms: 0.564838
  ...
# Subtest: resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
ok 2216 - resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
  ---
  duration_ms: 0.755162
  ...
# Subtest: focusTaskMoveDestination opens the destination file and anchors the cursor
ok 2217 - focusTaskMoveDestination opens the destination file and anchors the cursor
  ---
  duration_ms: 1.222264
  ...
# Subtest: focusTaskMoveDestination returns false without moving the cursor when the open fails
ok 2218 - focusTaskMoveDestination returns false without moving the cursor when the open fails
  ---
  duration_ms: 0.271398
  ...
# Subtest: focusTaskMoveDestination re-anchors by block ID when the destination content drifted
ok 2219 - focusTaskMoveDestination re-anchors by block ID when the destination content drifted
  ---
  duration_ms: 0.276889
  ...
# Subtest: physical task move chord declines auto-repeat and consumes Vim normal input once
ok 2220 - physical task move chord declines auto-repeat and consumes Vim normal input once
  ---
  duration_ms: 0.985542
  ...
# Subtest: counted task move dispatch keeps its count through cold async destinations
ok 2221 - counted task move dispatch keeps its count through cold async destinations
  ---
  duration_ms: 13.846641
  ...
# Subtest: counted task move dispatch with warm async destinations opens one counted picker
ok 2222 - counted task move dispatch with warm async destinations opens one counted picker
  ---
  duration_ms: 5.216041
  ...
# Subtest: bare task move command ignores stale Vim count outside normal mode
ok 2223 - bare task move command ignores stale Vim count outside normal mode
  ---
  duration_ms: 1.114418
  ...
# Subtest: bare task move command opens one uncounted target in Vim normal mode
ok 2224 - bare task move command opens one uncounted target in Vim normal mode
  ---
  duration_ms: 0.642116
  ...
# Subtest: already handled task move event leaves pending Vim state alone
ok 2225 - already handled task move event leaves pending Vim state alone
  ---
  duration_ms: 0.228727
  ...
# Subtest: counted task move command dispatch counts Pomodoro sub-bullets once
ok 2226 - counted task move command dispatch counts Pomodoro sub-bullets once
  ---
  duration_ms: 3.219939
  ...
# Subtest: physical transclusion toggle owns bare and counted Vim normal input
ok 2227 - physical transclusion toggle owns bare and counted Vim normal input
  ---
  duration_ms: 2.079391
  ...
# Subtest: runtime task move writes destination before source and rolls back source failures
ok 2228 - runtime task move writes destination before source and rolls back source failures
  ---
  duration_ms: 3.044685
  ...
# Subtest: runtime task move groups open-editor source and destination changes
ok 2229 - runtime task move groups open-editor source and destination changes
  ---
  duration_ms: 1.533299
  ...
# Subtest: runtime task move guards destination, auxiliary, and rollback failures
ok 2230 - runtime task move guards destination, auxiliary, and rollback failures
  ---
  duration_ms: 1.751235
  ...
# Subtest: task move insertion separates the section's first task from preamble and placeholders
ok 2231 - task move insertion separates the section's first task from preamble and placeholders
  ---
  duration_ms: 0.365919
  ...
# Subtest: task move insertion keeps populated sections compact and second moves stable
ok 2232 - task move insertion keeps populated sections compact and second moves stable
  ---
  duration_ms: 0.195534
  ...
# Subtest: task move planning separates a counted move into a count-only section
ok 2233 - task move planning separates a counted move into a count-only section
  ---
  duration_ms: 0.371229
  ...
# Subtest: runtime counted move into a count-only section focuses the first moved task
ok 2234 - runtime counted move into a count-only section focuses the first moved task
  ---
  duration_ms: 0.933393
  ...
# Subtest: absent local key with folder template writes the trigger and one notice
ok 2235 - absent local key with folder template writes the trigger and one notice
  ---
  duration_ms: 1.712751
  ...
# Subtest: existing local object keeps other keys and only adds the trigger
ok 2236 - existing local object keeps other keys and only adds the trigger
  ---
  duration_ms: 0.279053
  ...
# Subtest: stored true is already-enabled with no write and no notice
ok 2237 - stored true is already-enabled with no write and no notice
  ---
  duration_ms: 0.255879
  ...
# Subtest: stored false is device-opt-out with no write and no notice
ok 2238 - stored false is device-opt-out with no write and no notice
  ---
  duration_ms: 0.164594
  ...
# Subtest: mode none and blank folder templates skip as no-creation-templates
ok 2239 - mode none and blank folder templates skip as no-creation-templates
  ---
  duration_ms: 0.252613
  ...
# Subtest: regex mode with a non-empty file template enables
ok 2240 - regex mode with a non-empty file template enables
  ---
  duration_ms: 0.190334
  ...
# Subtest: legacy settings without a mode key skip as legacy-templater
ok 2241 - legacy settings without a mode key skip as legacy-templater
  ---
  duration_ms: 0.191957
  ...
# Subtest: missing Templater plugin or settings skip as no-templater without throwing
ok 2242 - missing Templater plugin or settings skip as no-templater without throwing
  ---
  duration_ms: 0.270186
  ...
# Subtest: missing loadLocalStorage or saveLocalStorage returns without throwing
ok 2243 - missing loadLocalStorage or saveLocalStorage returns without throwing
  ---
  duration_ms: 0.406857
  ...
# Subtest: string or array stored local values skip as unknown-local-shape
ok 2244 - string or array stored local values skip as unknown-local-shape
  ---
  duration_ms: 0.510245
  ...
# Subtest: saveLocalStorage throw shows one failure notice and does not escape
ok 2245 - saveLocalStorage throw shows one failure notice and does not escape
  ---
  duration_ms: 0.228426
  ...
# Subtest: planTemplaterLocalTrigger covers helper cases and never adds extra keys
ok 2246 - planTemplaterLocalTrigger covers helper cases and never adds extra keys
  ---
  duration_ms: 0.216002
  ...
# Subtest: unblocked model returns null when there is nothing to show
ok 2247 - unblocked model returns null when there is nothing to show
  ---
  duration_ms: 1.357402
  ...
# Subtest: unblocked card renders a single linked row with receipt and chips
ok 2248 - unblocked card renders a single linked row with receipt and chips
  ---
  duration_ms: 1.753689
  ...
# Subtest: unblocked card renders several linked rows with one entry
ok 2249 - unblocked card renders several linked rows with one entry
  ---
  duration_ms: 0.376038
  ...
# Subtest: unblocked card renders a created continuation with next up
ok 2250 - unblocked card renders a created continuation with next up
  ---
  duration_ms: 0.432746
  ...
# Subtest: unblocked card renders recovered-only and still-blocked rows
ok 2251 - unblocked card renders recovered-only and still-blocked rows
  ---
  duration_ms: 0.700557
  ...
# Subtest: current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
ok 2252 - current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
  ---
  duration_ms: 0.915217
  ...
# Subtest: project pull-in rows label empty projects and preserve project blocking reasons
ok 2253 - project pull-in rows label empty projects and preserve project blocking reasons
  ---
  duration_ms: 0.979189
  ...
# Subtest: unblocked card caps visible rows with +N more
ok 2254 - unblocked card caps visible rows with +N more
  ---
  duration_ms: 0.338256
  ...
# Subtest: unblocked card renders the breaker variant
ok 2255 - unblocked card renders the breaker variant
  ---
  duration_ms: 0.532457
  ...
# Subtest: unblocked card renders the failure variant
ok 2256 - unblocked card renders the failure variant
  ---
  duration_ms: 0.489655
  ...
# Subtest: unblocked rows open their task without dismissing the notice
ok 2257 - unblocked rows open their task without dismissing the notice
  ---
  duration_ms: 1.096985
  ...
# Subtest: unblocked row without a block id opens the note path
ok 2258 - unblocked row without a block id opens the note path
  ---
  duration_ms: 0.27715
  ...
# Subtest: unblocked card omits the plan chip when daily content is null
ok 2259 - unblocked card omits the plan chip when daily content is null
  ---
  duration_ms: 0.23047
  ...
# Subtest: unblocked notice shows one card with duration through showNotice
ok 2260 - unblocked notice shows one card with duration through showNotice
  ---
  duration_ms: 0.309401
  ...
# Subtest: unblocked notice falls back to plain text without a DOM
ok 2261 - unblocked notice falls back to plain text without a DOM
  ---
  duration_ms: 0.161128
  ...
# Subtest: unblocked text truncates to 48 characters with an ellipsis
ok 2262 - unblocked text truncates to 48 characters with an ellipsis
  ---
  duration_ms: 0.136661
  ...
# Subtest: nav api exposes additive notice v1 and keeps version 3
ok 2263 - nav api exposes additive notice v1 and keeps version 3
  ---
  duration_ms: 0.396117
  ...
# Subtest: unblocked stylesheet scopes notice overrides and uses task tokens
ok 2264 - unblocked stylesheet scopes notice overrides and uses task tokens
  ---
  duration_ms: 0.569438
  ...
# Subtest: physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
ok 2265 - physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
  ---
  duration_ms: 2.319349
  ...
# Subtest: open-task command ids omit repeat so the shared route resolves the pending Vim count
ok 2266 - open-task command ids omit repeat so the shared route resolves the pending Vim count
  ---
  duration_ms: 1.319199
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
ok 2267 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
  ---
  duration_ms: 4.628711
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
ok 2268 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
  ---
  duration_ms: 0.825958
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
ok 2269 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
  ---
  duration_ms: 1.526976
  ...
# Subtest: dispatch guard applies a command-route Vim count when the capture route fires second
ok 2270 - dispatch guard applies a command-route Vim count when the capture route fires second
  ---
  duration_ms: 1.406445
  ...
# Subtest: dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
ok 2271 - dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
  ---
  duration_ms: 0.986174
  ...
# Subtest: command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
ok 2272 - command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
  ---
  duration_ms: 0.865964
  ...
# Subtest: command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
ok 2273 - command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
  ---
  duration_ms: 2.422616
  ...
# Subtest: command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
ok 2274 - command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
  ---
  duration_ms: 0.926339
  ...
# Subtest: explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
ok 2275 - explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
  ---
  duration_ms: 0.591369
  ...
# Subtest: getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
ok 2276 - getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
  ---
  duration_ms: 0.201604
  ...
# Subtest: physical counted property chord consumes only explicit normal-mode Vim counts
ok 2277 - physical counted property chord consumes only explicit normal-mode Vim counts
  ---
  duration_ms: 0.563315
  ...
# Subtest: physical counted Ctrl+Shift+B and Ctrl+Shift+Alt+B route to their Task Card rows
ok 2278 - physical counted Ctrl+Shift+B and Ctrl+Shift+Alt+B route to their Task Card rows
  ---
  duration_ms: 0.480177
  ...
# Subtest: onload registers the palette command without a default hotkey
ok 2279 - onload registers the palette command without a default hotkey
  ---
  duration_ms: 1.72751
  ...
# Subtest: an embed and a plain image link open the resolved vault resource
ok 2280 - an embed and a plain image link open the resolved vault resource
  ---
  duration_ms: 3.169804
  ...
# Subtest: no image, a missing image, and Reading view show notices without opening
ok 2281 - no image, a missing image, and Reading view show notices without opening
  ---
  duration_ms: 0.544741
  ...
# Subtest: a second command invocation is ignored while the viewer is open
ok 2282 - a second command invocation is ignored while the viewer is open
  ---
  duration_ms: 0.356441
  ...
# Subtest: closing restores focus and leaves an unchanged selection and scroll alone
ok 2283 - closing restores focus and leaves an unchanged selection and scroll alone
  ---
  duration_ms: 0.420222
  ...
# Subtest: closing restores moved selection and scroll only while the source view is active
ok 2284 - closing restores moved selection and scroll only while the source view is active
  ---
  duration_ms: 0.752718
  ...
# Subtest: unload closes the active viewer without restoring editor focus
ok 2285 - unload closes the active viewer without restoring editor focus
  ---
  duration_ms: 0.512018
  ...
# Subtest: parser finds vault embed with size hint
ok 2286 - parser finds vault embed with size hint
  ---
  duration_ms: 1.482762
  ...
# Subtest: parser finds plain image wikilink and blockquoted embed
ok 2287 - parser finds plain image wikilink and blockquoted embed
  ---
  duration_ms: 0.234577
  ...
# Subtest: parser ignores callout bracket and finds the embed
ok 2288 - parser ignores callout bracket and finds the embed
  ---
  duration_ms: 0.329068
  ...
# Subtest: parser ignores image links inside single and double backticks
ok 2289 - parser ignores image links inside single and double backticks
  ---
  duration_ms: 0.749621
  ...
# Subtest: non-image wiki targets are recognized but not candidates
ok 2290 - non-image wiki targets are recognized but not candidates
  ---
  duration_ms: 0.239657
  ...
# Subtest: parser finds two image refs and lines with no refs
ok 2291 - parser finds two image refs and lines with no refs
  ---
  duration_ms: 0.168162
  ...
# Subtest: parser handles Markdown angle, title, and balanced parens
ok 2292 - parser handles Markdown angle, title, and balanced parens
  ---
  duration_ms: 0.404131
  ...
# Subtest: picker uses containing, next, then previous rule
ok 2293 - picker uses containing, next, then previous rule
  ---
  duration_ms: 0.362713
  ...
# Subtest: resolution records sourcePath and resolves duplicate basenames
ok 2294 - resolution records sourcePath and resolves duplicate basenames
  ---
  duration_ms: 1.031891
  ...
# Subtest: resolution handles relative, unicode, and space names
ok 2295 - resolution handles relative, unicode, and space names
  ---
  duration_ms: 0.521836
  ...
# Subtest: missing file, non-image cursor, and fenced lines show exact notices
ok 2296 - missing file, non-image cursor, and fenced lines show exact notices
  ---
  duration_ms: 0.33519
  ...
# Subtest: vault resolution calls getResourcePath with the resolved file
ok 2297 - vault resolution calls getResourcePath with the resolved file
  ---
  duration_ms: 0.304221
  ...
# Subtest: http embed passes through and non-image urls are not candidates
ok 2298 - http embed passes through and non-image urls are not candidates
  ---
  duration_ms: 0.364767
  ...
# Subtest: fit never exceeds 1 and respects padding for landscape, portrait, and tiny images
ok 2299 - fit never exceeds 1 and respects padding for landscape, portrait, and tiny images
  ---
  duration_ms: 1.224909
  ...
# Subtest: min and max bounds follow fit, 1:1, and the max factor
ok 2300 - min and max bounds follow fit, 1:1, and the max factor
  ---
  duration_ms: 0.216143
  ...
# Subtest: stepping clamps at both bounds
ok 2301 - stepping clamps at both bounds
  ---
  duration_ms: 0.428549
  ...
# Subtest: zoom-at-point keeps the point fixed
ok 2302 - zoom-at-point keeps the point fixed
  ---
  duration_ms: 0.15199
  ...
# Subtest: clamp centres small axes and limits large ones
ok 2303 - clamp centres small axes and limits large ones
  ---
  duration_ms: 0.287599
  ...
# Subtest: key Escape → close
ok 2304 - key Escape → close
  ---
  duration_ms: 0.657987
  ...
# Subtest: key q → close
ok 2305 - key q → close
  ---
  duration_ms: 0.157661
  ...
# Subtest: key Q → close
ok 2306 - key Q → close
  ---
  duration_ms: 0.102265
  ...
# Subtest: key Ctrl+[ → close
ok 2307 - key Ctrl+[ → close
  ---
  duration_ms: 0.316084
  ...
# Subtest: key Z → close
ok 2308 - key Z → close
  ---
  duration_ms: 0.363343
  ...
# Subtest: key + → zoomIn
ok 2309 - key + → zoomIn
  ---
  duration_ms: 0.143414
  ...
# Subtest: key = → zoomIn
ok 2310 - key = → zoomIn
  ---
  duration_ms: 0.085263
  ...
# Subtest: key Shift+= → zoomIn
ok 2311 - key Shift+= → zoomIn
  ---
  duration_ms: 0.07855
  ...
# Subtest: key Shift++ → zoomIn
ok 2312 - key Shift++ → zoomIn
  ---
  duration_ms: 0.13653
  ...
# Subtest: key - → zoomOut
ok 2313 - key - → zoomOut
  ---
  duration_ms: 0.077478
  ...
# Subtest: key 0 → fit
ok 2314 - key 0 → fit
  ---
  duration_ms: 0.123366
  ...
# Subtest: key 1 → actual
ok 2315 - key 1 → actual
  ---
  duration_ms: 0.07336
  ...
# Subtest: key h → pan:left
ok 2316 - key h → pan:left
  ---
  duration_ms: 0.085473
  ...
# Subtest: key j → pan:down
ok 2317 - key j → pan:down
  ---
  duration_ms: 0.067068
  ...
# Subtest: key k → pan:up
ok 2318 - key k → pan:up
  ---
  duration_ms: 0.07292
  ...
# Subtest: key l → pan:right
ok 2319 - key l → pan:right
  ---
  duration_ms: 0.07353
  ...
# Subtest: key Shift+H → pan:left
ok 2320 - key Shift+H → pan:left
  ---
  duration_ms: 0.083079
  ...
# Subtest: key Shift+J → pan:down
ok 2321 - key Shift+J → pan:down
  ---
  duration_ms: 0.066968
  ...
# Subtest: key Shift+K → pan:up
ok 2322 - key Shift+K → pan:up
  ---
  duration_ms: 0.070865
  ...
# Subtest: key Shift+L → pan:right
ok 2323 - key Shift+L → pan:right
  ---
  duration_ms: 0.066337
  ...
# Subtest: key ArrowLeft → pan:left
ok 2324 - key ArrowLeft → pan:left
  ---
  duration_ms: 0.066317
  ...
# Subtest: key ArrowDown → pan:down
ok 2325 - key ArrowDown → pan:down
  ---
  duration_ms: 0.064633
  ...
# Subtest: key ArrowUp → pan:up
ok 2326 - key ArrowUp → pan:up
  ---
  duration_ms: 0.06273
  ...
# Subtest: key ArrowRight → pan:right
ok 2327 - key ArrowRight → pan:right
  ---
  duration_ms: 0.060064
  ...
# Subtest: key Shift+ArrowLeft → pan:left
ok 2328 - key Shift+ArrowLeft → pan:left
  ---
  duration_ms: 0.123997
  ...
# Subtest: key Ctrl+q → ignore
ok 2329 - key Ctrl+q → ignore
  ---
  duration_ms: 0.080654
  ...
# Subtest: key Meta+z → ignore
ok 2330 - key Meta+z → ignore
  ---
  duration_ms: 0.075805
  ...
# Subtest: key Meta+Z → ignore
ok 2331 - key Meta+Z → ignore
  ---
  duration_ms: 0.13617
  ...
# Subtest: key a composing → ignore
ok 2332 - key a composing → ignore
  ---
  duration_ms: 0.070465
  ...
# Subtest: key a keyCode 229 → ignore
ok 2333 - key a keyCode 229 → ignore
  ---
  duration_ms: 0.072719
  ...
# Subtest: key x → ignore
ok 2334 - key x → ignore
  ---
  duration_ms: 0.059994
  ...
# Subtest: keys before arming are ignored
ok 2335 - keys before arming are ignored
  ---
  duration_ms: 1.036589
  ...
# Subtest: Z closes after arming, and a repeated Z does not
ok 2336 - Z closes after arming, and a repeated Z does not
  ---
  duration_ms: 0.495777
  ...
# Subtest: load sets fit state and dimensions
ok 2337 - load sets fit state and dimensions
  ---
  duration_ms: 0.47675
  ...
# Subtest: a load error shows a notice, closes, and calls onClosed once
ok 2338 - a load error shows a notice, closes, and calls onClosed once
  ---
  duration_ms: 0.274744
  ...
# Subtest: Escape closes once, unregisters the scope handler, and aborts the signal
ok 2339 - Escape closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.219279
  ...
# Subtest: q closes once, unregisters the scope handler, and aborts the signal
ok 2340 - q closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.208558
  ...
# Subtest: Q closes once, unregisters the scope handler, and aborts the signal
ok 2341 - Q closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.16221
  ...
# Subtest: Ctrl+[ closes once, unregisters the scope handler, and aborts the signal
ok 2342 - Ctrl+[ closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.201545
  ...
# Subtest: Z closes once, unregisters the scope handler, and aborts the signal
ok 2343 - Z closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.256841
  ...
# Subtest: a stray x key changes nothing
ok 2344 - a stray x key changes nothing
  ---
  duration_ms: 0.237944
  ...
# Subtest: the app's vault stubs throw and are never called
ok 2345 - the app's vault stubs throw and are never called
  ---
  duration_ms: 0.205793
  ...
# Subtest: task-card-gate arms only on open inbox tasks
ok 2346 - task-card-gate arms only on open inbox tasks
  ---
  duration_ms: 3.518318
  ...
# Subtest: task-card-gate header shows the Inbox chip only when armed
ok 2347 - task-card-gate header shows the Inbox chip only when armed
  ---
  duration_ms: 5.941426
  ...
# Subtest: task-card-gate priority: cancel writes nothing
ok 2348 - task-card-gate priority: cancel writes nothing
  ---
  duration_ms: 1.080183
  ...
# Subtest: task-card-gate priority: stay runs today's write
ok 2349 - task-card-gate priority: stay runs today's write
  ---
  duration_ms: 0.265497
  ...
# Subtest: task-card-gate priority: move writes then moves
ok 2350 - task-card-gate priority: move writes then moves
  ---
  duration_ms: 0.530673
  ...
# Subtest: task-card-gate scheduled: cancel writes nothing
ok 2351 - task-card-gate scheduled: cancel writes nothing
  ---
  duration_ms: 0.15749
  ...
# Subtest: task-card-gate scheduled: stay runs today's write
ok 2352 - task-card-gate scheduled: stay runs today's write
  ---
  duration_ms: 0.276367
  ...
# Subtest: task-card-gate scheduled: move writes then moves
ok 2353 - task-card-gate scheduled: move writes then moves
  ---
  duration_ms: 0.185354
  ...
# Subtest: task-card-gate generic-property: cancel writes nothing
ok 2354 - task-card-gate generic-property: cancel writes nothing
  ---
  duration_ms: 0.39274
  ...
# Subtest: task-card-gate generic-property: stay runs today's write
ok 2355 - task-card-gate generic-property: stay runs today's write
  ---
  duration_ms: 0.431083
  ...
# Subtest: task-card-gate generic-property: move writes then moves
ok 2356 - task-card-gate generic-property: move writes then moves
  ---
  duration_ms: 0.307307
  ...
# Subtest: task-card-gate refresh-interval: cancel writes nothing
ok 2357 - task-card-gate refresh-interval: cancel writes nothing
  ---
  duration_ms: 0.171467
  ...
# Subtest: task-card-gate refresh-interval: stay runs today's write
ok 2358 - task-card-gate refresh-interval: stay runs today's write
  ---
  duration_ms: 0.13119
  ...
# Subtest: task-card-gate refresh-interval: move writes then moves
ok 2359 - task-card-gate refresh-interval: move writes then moves
  ---
  duration_ms: 0.141741
  ...
# Subtest: task-card-gate refresh-custom: cancel writes nothing
ok 2360 - task-card-gate refresh-custom: cancel writes nothing
  ---
  duration_ms: 0.12048
  ...
# Subtest: task-card-gate refresh-custom: stay runs today's write
ok 2361 - task-card-gate refresh-custom: stay runs today's write
  ---
  duration_ms: 0.133054
  ...
# Subtest: task-card-gate refresh-custom: move writes then moves
ok 2362 - task-card-gate refresh-custom: move writes then moves
  ---
  duration_ms: 0.353245
  ...
# Subtest: task-card-gate clear-priority: cancel writes nothing
ok 2363 - task-card-gate clear-priority: cancel writes nothing
  ---
  duration_ms: 0.145438
  ...
# Subtest: task-card-gate clear-priority: stay runs today's write
ok 2364 - task-card-gate clear-priority: stay runs today's write
  ---
  duration_ms: 0.115881
  ...
# Subtest: task-card-gate clear-priority: move writes then moves
ok 2365 - task-card-gate clear-priority: move writes then moves
  ---
  duration_ms: 0.150878
  ...
# Subtest: task-card-gate recommended-roll: cancel writes nothing
ok 2366 - task-card-gate recommended-roll: cancel writes nothing
  ---
  duration_ms: 0.102866
  ...
# Subtest: task-card-gate recommended-roll: stay runs today's write
ok 2367 - task-card-gate recommended-roll: stay runs today's write
  ---
  duration_ms: 0.101363
  ...
# Subtest: task-card-gate recommended-roll: move writes then moves
ok 2368 - task-card-gate recommended-roll: move writes then moves
  ---
  duration_ms: 0.123776
  ...
# Subtest: task-card-gate recommended-decay: cancel writes nothing
ok 2369 - task-card-gate recommended-decay: cancel writes nothing
  ---
  duration_ms: 0.0942
  ...
# Subtest: task-card-gate recommended-decay: stay runs today's write
ok 2370 - task-card-gate recommended-decay: stay runs today's write
  ---
  duration_ms: 0.116442
  ...
# Subtest: task-card-gate recommended-decay: move writes then moves
ok 2371 - task-card-gate recommended-decay: move writes then moves
  ---
  duration_ms: 0.114138
  ...
# Subtest: task-card-gate counted-roll: cancel writes nothing
ok 2372 - task-card-gate counted-roll: cancel writes nothing
  ---
  duration_ms: 0.141881
  ...
# Subtest: task-card-gate counted-roll: stay runs today's write
ok 2373 - task-card-gate counted-roll: stay runs today's write
  ---
  duration_ms: 0.100081
  ...
# Subtest: task-card-gate counted-roll: move writes then moves
ok 2374 - task-card-gate counted-roll: move writes then moves
  ---
  duration_ms: 0.211383
  ...
# Subtest: task-card-gate lane-toggle: cancel writes nothing
ok 2375 - task-card-gate lane-toggle: cancel writes nothing
  ---
  duration_ms: 0.100081
  ...
# Subtest: task-card-gate lane-toggle: stay runs today's write
ok 2376 - task-card-gate lane-toggle: stay runs today's write
  ---
  duration_ms: 0.10437
  ...
# Subtest: task-card-gate lane-toggle: move writes then moves
ok 2377 - task-card-gate lane-toggle: move writes then moves
  ---
  duration_ms: 0.165165
  ...
# Subtest: task-card-gate dependency-single: cancel writes nothing
ok 2378 - task-card-gate dependency-single: cancel writes nothing
  ---
  duration_ms: 0.092757
  ...
# Subtest: task-card-gate dependency-single: stay runs today's write
ok 2379 - task-card-gate dependency-single: stay runs today's write
  ---
  duration_ms: 0.091645
  ...
# Subtest: task-card-gate dependency-single: move writes then moves
ok 2380 - task-card-gate dependency-single: move writes then moves
  ---
  duration_ms: 0.373132
  ...
# Subtest: task-card-gate dependency-marked: cancel writes nothing
ok 2381 - task-card-gate dependency-marked: cancel writes nothing
  ---
  duration_ms: 0.092236
  ...
# Subtest: task-card-gate dependency-marked: stay runs today's write
ok 2382 - task-card-gate dependency-marked: stay runs today's write
  ---
  duration_ms: 0.092948
  ...
# Subtest: task-card-gate dependency-marked: move writes then moves
ok 2383 - task-card-gate dependency-marked: move writes then moves
  ---
  duration_ms: 0.112935
  ...
# Subtest: task-card-gate dependency-vault: cancel writes nothing
ok 2384 - task-card-gate dependency-vault: cancel writes nothing
  ---
  duration_ms: 0.095302
  ...
# Subtest: task-card-gate dependency-vault: stay runs today's write
ok 2385 - task-card-gate dependency-vault: stay runs today's write
  ---
  duration_ms: 0.093438
  ...
# Subtest: task-card-gate dependency-vault: move writes then moves
ok 2386 - task-card-gate dependency-vault: move writes then moves
  ---
  duration_ms: 0.139016
  ...
# Subtest: task-card-gate dependency-counted: cancel writes nothing
ok 2387 - task-card-gate dependency-counted: cancel writes nothing
  ---
  duration_ms: 0.090052
  ...
# Subtest: task-card-gate dependency-counted: stay runs today's write
ok 2388 - task-card-gate dependency-counted: stay runs today's write
  ---
  duration_ms: 0.090072
  ...
# Subtest: task-card-gate dependency-counted: move writes then moves
ok 2389 - task-card-gate dependency-counted: move writes then moves
  ---
  duration_ms: 0.114669
  ...
# Subtest: task-card-gate negative rows never prompt
ok 2390 - task-card-gate negative rows never prompt
  ---
  duration_ms: 0.782815
  ...
# Subtest: task-card-gate counted sessions capture N targets
ok 2391 - task-card-gate counted sessions capture N targets
  ---
  duration_ms: 0.373614
  ...
# Subtest: task-card-gate walk: move advances once with Moved first
ok 2392 - task-card-gate walk: move advances once with Moved first
  ---
  duration_ms: 0.223526
  ...
# Subtest: task-card-gate walk: move failure falls back to card with partial
ok 2393 - task-card-gate walk: move failure falls back to card with partial
  ---
  duration_ms: 0.327345
  ...
# Subtest: task-card-gate walk: exactly one settle per origin
ok 2394 - task-card-gate walk: exactly one settle per origin
  ---
  duration_ms: 26.182778
  ...
# Subtest: task-card-gate route outcome resolves like lane and link-today
ok 2395 - task-card-gate route outcome resolves like lane and link-today
  ---
  duration_ms: 0.609063
  ...
# Subtest: inbox classifier covers the inbox contract
ok 2396 - inbox classifier covers the inbox contract
  ---
  duration_ms: 2.238144
  ...
# Subtest: isInboxNotePath matches the inbox contract through the vault
ok 2397 - isInboxNotePath matches the inbox contract through the vault
  ---
  duration_ms: 1.581229
  ...
# Subtest: isInboxNotePath is false without an inbox note and never throws
ok 2398 - isInboxNotePath is false without an inbox note and never throws
  ---
  duration_ms: 0.208649
  ...
# Subtest: route destinations drop every inbox note, the source, and templates
ok 2399 - route destinations drop every inbox note, the source, and templates
  ---
  duration_ms: 0.954603
  ...
# Subtest: route preflight accepts a live area destination
ok 2400 - route preflight accepts a live area destination
  ---
  duration_ms: 5.160183
  ...
# Subtest: route preflight refuses stale and colliding destinations
ok 2401 - route preflight refuses stale and colliding destinations
  ---
  duration_ms: 1.812401
  ...
# Subtest: route picker resolves move, stay, cancel, and close exactly once
ok 2402 - route picker resolves move, stay, cancel, and close exactly once
  ---
  duration_ms: 4.055755
  ...
# Subtest: route picker footer names the move, the hatch, and the way back
ok 2403 - route picker footer names the move, the hatch, and the way back
  ---
  duration_ms: 0.564007
  ...
# Subtest: route picker preflight refusal keeps the picker open with a notice
ok 2404 - route picker preflight refusal keeps the picker open with a notice
  ---
  duration_ms: 7.107773
  ...
# Subtest: route picker honors the shared move-picker guard
ok 2405 - route picker honors the shared move-picker guard
  ---
  duration_ms: 2.165265
  ...
# Subtest: promptInboxRoute moves, stays, and cancels with suspend pairing
ok 2406 - promptInboxRoute moves, stays, and cancels with suspend pairing
  ---
  duration_ms: 2.422436
  ...
# Subtest: commitInboxRoute moves the verified task with its children
ok 2407 - commitInboxRoute moves the verified task with its children
  ---
  duration_ms: 3.430811
  ...
# Subtest: commitInboxRoute into a blocked project tags the moved task
ok 2408 - commitInboxRoute into a blocked project tags the moved task
  ---
  duration_ms: 1.90619
  ...
# Subtest: commitInboxRoute moves a counted run and refuses on identity drift
ok 2409 - commitInboxRoute moves a counted run and refuses on identity drift
  ---
  duration_ms: 2.973038
  ...
# Subtest: reviewOutcomeResolves treats route like lane and link-today
ok 2410 - reviewOutcomeResolves treats route like lane and link-today
  ---
  duration_ms: 0.244957
  ...
# Subtest: nav api inboxRoute v1 delegates, shapes, and never throws
ok 2411 - nav api inboxRoute v1 delegates, shapes, and never throws
  ---
  duration_ms: 1.179743
  ...
# Subtest: history records ordered locations with file identity and dedupes adjacent repeats
ok 2412 - history records ordered locations with file identity and dedupes adjacent repeats
  ---
  duration_ms: 1.287288
  ...
# Subtest: transition records origin then destination and truncates forward only on success
ok 2413 - transition records origin then destination and truncates forward only on success
  ---
  duration_ms: 0.775
  ...
# Subtest: history retains at most 100 locations and refreshes the live tip
ok 2414 - history retains at most 100 locations and refreshes the live tip
  ---
  duration_ms: 0.571151
  ...
# Subtest: rename updates paths and delete prunes without corrupting the index
ok 2415 - rename updates paths and delete prunes without corrupting the index
  ---
  duration_ms: 0.233246
  ...
# Subtest: bridge wraps add once, mirrors native jumps, and preserves the original call
ok 2416 - bridge wraps add once, mirrors native jumps, and preserves the original call
  ---
  duration_ms: 1.224768
  ...
# Subtest: bridge without a jump list preserves keys and emits one compatibility diagnostic
ok 2417 - bridge without a jump list preserves keys and emits one compatibility diagnostic
  ---
  duration_ms: 0.26699
  ...
# Subtest: registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
ok 2418 - registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
  ---
  duration_ms: 0.322747
  ...
# Subtest: Enter A->B round-trips with Ctrl+O and Ctrl+I
ok 2419 - Enter A->B round-trips with Ctrl+O and Ctrl+I
  ---
  duration_ms: 22.127083
  ...
# Subtest: counted Enter returns to the original cursor, not the counted link line
ok 2420 - counted Enter returns to the original cursor, not the counted link line
  ---
  duration_ms: 21.157191
  ...
# Subtest: picker choice records one jump and cancellation records none
ok 2421 - picker choice records one jump and cancellation records none
  ---
  duration_ms: 22.8039
  ...
# Subtest: stale picker origin is rejected and failed opens record nothing
ok 2422 - stale picker origin is rejected and failed opens record nothing
  ---
  duration_ms: 22.065225
  ...
# Subtest: Backspace shares the link path and no-link lines fall through
ok 2423 - Backspace shares the link path and no-link lines fall through
  ---
  duration_ms: 21.048013
  ...
# Subtest: counted traversal honors boundaries and new jumps replace the forward branch
ok 2424 - counted traversal honors boundaries and new jumps replace the forward branch
  ---
  duration_ms: 1.006842
  ...
# Subtest: ordinary motion before back is preserved for forward restore
ok 2425 - ordinary motion before back is preserved for forward restore
  ---
  duration_ms: 0.406246
  ...
# Subtest: deleted entries are skipped and heading links settle before recording
ok 2426 - deleted entries are skipped and heading links settle before recording
  ---
  duration_ms: 23.538799
  ...
# Subtest: native fallback runs with empty history and boundaries never replay natives
ok 2427 - native fallback runs with empty history and boundaries never replay natives
  ---
  duration_ms: 0.846587
  ...
# Subtest: unload restores the native add and keeps a foreign later mapping
ok 2428 - unload restores the native add and keeps a foreign later mapping
  ---
  duration_ms: 0.556232
  ...
# Subtest: exact eligibility authorizes one due-Ready ROTTEN row
ok 2429 - exact eligibility authorizes one due-Ready ROTTEN row
  ---
  duration_ms: 1.834954
  ...
# Subtest: exact eligibility authorizes a TICKLER row
ok 2430 - exact eligibility authorizes a TICKLER row
  ---
  duration_ms: 0.281999
  ...
# Subtest: exact eligibility refuses every stale-cache shape
ok 2431 - exact eligibility refuses every stale-cache shape
  ---
  duration_ms: 0.738871
  ...
# Subtest: exact eligibility refuses non-Ready and non-due rows
ok 2432 - exact eligibility refuses non-Ready and non-due rows
  ---
  duration_ms: 0.364085
  ...
# Subtest: legacy refs still match line-only while exact refuses
ok 2433 - legacy refs still match line-only while exact refuses
  ---
  duration_ms: 0.758608
  ...
# Subtest: keeps support needs namespace v5 with keepLine
ok 2434 - keeps support needs namespace v5 with keepLine
  ---
  duration_ms: 0.203859
  ...
# Subtest: decay decisions need namespace v6 with keepLine
ok 2435 - decay decisions need namespace v6 with keepLine
  ---
  duration_ms: 0.254136
  ...
# Subtest: batch forwards per-target counted decisions to the stamper
ok 2436 - batch forwards per-target counted decisions to the stamper
  ---
  duration_ms: 0.861455
  ...
# Subtest: batch keeps legacy index targets uncounted
ok 2437 - batch keeps legacy index targets uncounted
  ---
  duration_ms: 0.433017
  ...
# Subtest: a throwing stamper refuses the batch with no partial write
ok 2438 - a throwing stamper refuses the batch with no partial write
  ---
  duration_ms: 0.610245
  ...
# Subtest: parseKeepsCount reads the first valid value only
ok 2439 - parseKeepsCount reads the first valid value only
  ---
  duration_ms: 0.438237
  ...
# Subtest: countFreshStampKept measures actual increments only
ok 2440 - countFreshStampKept measures actual increments only
  ---
  duration_ms: 0.243204
  ...
# Subtest: fresh stamp notice tails kept increments without promises
ok 2441 - fresh stamp notice tails kept increments without promises
  ---
  duration_ms: 0.293872
  ...
# Subtest: duplicate source targets dedupe to one write
ok 2442 - duplicate source targets dedupe to one write
  ---
  duration_ms: 0.221874
  ...
# Subtest: single Alt+F increments an exact due-Ready ROTTEN task
ok 2443 - single Alt+F increments an exact due-Ready ROTTEN task
  ---
  duration_ms: 6.105509
  ...
# Subtest: single Alt+F preserves NEW, lane, and early tasks without counting
ok 2444 - single Alt+F preserves NEW, lane, and early tasks without counting
  ---
  duration_ms: 2.187207
  ...
# Subtest: same-day repeat stays identical and counts nothing
ok 2445 - same-day repeat stays identical and counts nothing
  ---
  duration_ms: 0.599204
  ...
# Subtest: Pending Alt+F writes its summary with the stamp in one edit
ok 2446 - Pending Alt+F writes its summary with the stamp in one edit
  ---
  duration_ms: 1.353425
  ...
# Subtest: counted Pending refresh shares one summary only with Pending targets
ok 2447 - counted Pending refresh shares one summary only with Pending targets
  ---
  duration_ms: 0.809596
  ...
# Subtest: a refusing counted target refuses before the Pending Work Log prompt
ok 2448 - a refusing counted target refuses before the Pending Work Log prompt
  ---
  duration_ms: 0.465379
  ...
# Subtest: blank Pending refresh advances; cancelled or stale prompts write nothing
ok 2449 - blank Pending refresh advances; cancelled or stale prompts write nothing
  ---
  duration_ms: 1.207596
  ...
# Subtest: stale queue match stamps uncounted and never inflates
ok 2450 - stale queue match stamps uncounted and never inflates
  ---
  duration_ms: 0.577283
  ...
# Subtest: counted Alt+F increments every exact target once
ok 2451 - counted Alt+F increments every exact target once
  ---
  duration_ms: 0.576822
  ...
# Subtest: stale editor source refuses with no write
ok 2452 - stale editor source refuses with no write
  ---
  duration_ms: 0.229579
  ...
# Subtest: single-note write lands in one editor transaction and keeps CRLF
ok 2453 - single-note write lands in one editor transaction and keeps CRLF
  ---
  duration_ms: 0.500937
  ...
# Subtest: v5 without keepLine fails without writing
ok 2454 - v5 without keepLine fails without writing
  ---
  duration_ms: 0.153914
  ...
# Subtest: throwing v5 keepLine refuses the batch with no partial write
ok 2455 - throwing v5 keepLine refuses the batch with no partial write
  ---
  duration_ms: 0.328568
  ...
# Subtest: pre-v5 ledger stamps uncounted through the old stamper
ok 2456 - pre-v5 ledger stamps uncounted through the old stamper
  ---
  duration_ms: 0.427636
  ...
# Subtest: Task Link session skips an at-limit decide target
ok 2457 - Task Link session skips an at-limit decide target
  ---
  duration_ms: 1.932861
  ...
# Subtest: Task Link refresh counts one exact target
ok 2458 - Task Link refresh counts one exact target
  ---
  duration_ms: 1.21505
  ...
# Subtest: duplicate Task Links to one target stamp and count once
ok 2459 - duplicate Task Links to one target stamp and count once
  ---
  duration_ms: 0.605907
  ...
# Subtest: counted Task Links dedupe targets and log only the Pending target
ok 2460 - counted Task Links dedupe targets and log only the Pending target
  ---
  duration_ms: 0.840134
  ...
# Subtest: multi-note stale preimage refuses with no writes
ok 2461 - multi-note stale preimage refuses with no writes
  ---
  duration_ms: 0.740714
  ...
# Subtest: multi-note write failure rolls back the first note
ok 2462 - multi-note write failure rolls back the first note
  ---
  duration_ms: 0.883347
  ...
# Subtest: one physical key through two routes stamps once
ok 2463 - one physical key through two routes stamps once
  ---
  duration_ms: 1.283441
  ...
# Subtest: Ctrl+Alt+F capture advances once and consumes a Vim prefix
ok 2464 - Ctrl+Alt+F capture advances once and consumes a Vim prefix
  ---
  duration_ms: 0.609954
  ...
# Subtest: obsolete and extra-modifier F chords stay unconsumed
ok 2465 - obsolete and extra-modifier F chords stay unconsumed
  ---
  duration_ms: 0.258353
  ...
# Subtest: live Ctrl+Alt+F double dispatch asks once on a Pending task
ok 2466 - live Ctrl+Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.701299
  ...
# Subtest: live Alt+F double dispatch asks once on a Pending task
ok 2467 - live Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.732779
  ...
# Subtest: already-handled refresh keydown leaves Vim state alone
ok 2468 - already-handled refresh keydown leaves Vim state alone
  ---
  duration_ms: 0.277611
  ...
# Subtest: parseBobOpenNotesParams accepts indexed entries and ignores unknown keys
ok 2469 - parseBobOpenNotesParams accepts indexed entries and ignores unknown keys
  ---
  duration_ms: 2.764148
  ...
# Subtest: parseBobOpenNotesParams rejects every malformed URI field
ok 2470 - parseBobOpenNotesParams rejects every malformed URI field
  ---
  duration_ms: 0.671873
  ...
# Subtest: invalid batches show one notice and open nothing
ok 2471 - invalid batches show one notice and open nothing
  ---
  duration_ms: 1.726607
  ...
# Subtest: path mapping follows a symlink realpath into the vault
ok 2472 - path mapping follows a symlink realpath into the vault
  ---
  duration_ms: 4.667723
  ...
# Subtest: new-tab policy reuses existing tabs and the active empty tab, keeping order and primary active
ok 2473 - new-tab policy reuses existing tabs and the active empty tab, keeping order and primary active
  ---
  duration_ms: 2.150506
  ...
# Subtest: an absent or outside entry fails independently and a PDF opens without landing
ok 2474 - an absent or outside entry fails independently and a PDF opens without landing
  ---
  duration_ms: 2000.558301
  ...
# Subtest: a resolved note that is not open waits until its captured digest is cached
ok 2475 - a resolved note that is not open waits until its captured digest is cached
  ---
  duration_ms: 65.313826
  ...
# Subtest: a per-entry open failure does not prevent later notes from opening
ok 2476 - a per-entry open failure does not prevent later notes from opening
  ---
  duration_ms: 1.160586
  ...
# Subtest: waits for a newly created vault file and a late visible line digest
ok 2477 - waits for a newly created vault file and a late visible line digest
  ---
  duration_ms: 61.352307
  ...
# Subtest: re-finds a moved digest on any line, including prose and Pomodoro rows
ok 2478 - re-finds a moved digest on any line, including prose and Pomodoro rows
  ---
  duration_ms: 1.559798
  ...
# Subtest: deadline fallback opens near the planned line and reports a changed capture
ok 2479 - deadline fallback opens near the planned line and reports a changed capture
  ---
  duration_ms: 2000.934769
  ...
# Subtest: truncation reports how many of the full list opened
ok 2480 - truncation reports how many of the full list opened
  ---
  duration_ms: 0.604725
  ...
# Subtest: serializes quick URLs and leaves the later URL active
ok 2481 - serializes quick URLs and leaves the later URL active
  ---
  duration_ms: 1.290745
  ...
# Subtest: primary landing flashes briefly, secondary landings do not, and the handler is read-only
ok 2482 - primary landing flashes briefly, secondary landings do not, and the handler is read-only
  ---
  duration_ms: 15.655287
  ...
# Subtest: onload registers bob-open-notes beside bob-goto-task
ok 2483 - onload registers bob-open-notes beside bob-goto-task
  ---
  duration_ms: 1.13611
  ...
# Subtest: a non-file sidebar view is not reused as an empty tab
ok 2484 - a non-file sidebar view is not reused as an empty tab
  ---
  duration_ms: 0.459718
  ...
# Subtest: a true empty tab is reused for the first entry
ok 2485 - a true empty tab is reused for the first entry
  ---
  duration_ms: 0.239468
  ...
# Subtest: three new tabs follow entry order in the tab strip
ok 2486 - three new tabs follow entry order in the tab strip
  ---
  duration_ms: 0.45539
  ...
# Subtest: two tabs of the same note reuse the first matching leaf
ok 2487 - two tabs of the same note reuse the first matching leaf
  ---
  duration_ms: 0.236682
  ...
# Subtest: a missing file does not scan vault lists when getAbstractFileByPath exists
ok 2488 - a missing file does not scan vault lists when getAbstractFileByPath exists
  ---
  duration_ms: 1999.822034
  ...
# Subtest: new tabs append at the far right when the middle tab is active
ok 2489 - new tabs append at the far right when the middle tab is active
  ---
  duration_ms: 1.037691
  ...
# Subtest: a reused tab stays put while a new one is appended
ok 2490 - a reused tab stays put while a new one is appended
  ---
  duration_ms: 0.509954
  ...
# Subtest: a deferred tab is reused and findMarkdownLeafByPath sees it
ok 2491 - a deferred tab is reused and findMarkdownLeafByPath sees it
  ---
  duration_ms: 0.674478
  ...
# Subtest: a deferred sidebar leaf whose saved state names the note is not reused
ok 2492 - a deferred sidebar leaf whose saved state names the note is not reused
  ---
  duration_ms: 0.489786
  ...
# Subtest: a loaded main-area match beats an earlier loaded sidebar match
ok 2493 - a loaded main-area match beats an earlier loaded sidebar match
  ---
  duration_ms: 0.394183
  ...
# Subtest: a new tab goes to the end of the main group when a sidebar leaf is active
ok 2494 - a new tab goes to the end of the main group when a sidebar leaf is active
  ---
  duration_ms: 0.447234
  ...
# Subtest: falling back without createLeafInParent still opens a new tab
ok 2495 - falling back without createLeafInParent still opens a new tab
  ---
  duration_ms: 0.394623
  ...
# Subtest: falling back when createLeafInParent throws still opens a new tab
ok 2496 - falling back when createLeafInParent throws still opens a new tab
  ---
  duration_ms: 0.389835
  ...
# Subtest: collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
ok 2497 - collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
  ---
  duration_ms: 3.253944
  ...
# Subtest: getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
ok 2498 - getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
  ---
  duration_ms: 2.715395
  ...
# Subtest: getProjectBlockState reports an open external prerequisite
ok 2499 - getProjectBlockState reports an open external prerequisite
  ---
  duration_ms: 0.736677
  ...
# Subtest: getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
ok 2500 - getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
  ---
  duration_ms: 0.763688
  ...
# Subtest: getProjectBlockState scheduledValue override is the inline date, not frontmatter
ok 2501 - getProjectBlockState scheduledValue override is the inline date, not frontmatter
  ---
  duration_ms: 0.516176
  ...
# Subtest: getProjectBlockState skips internal and archive Depends-On links
ok 2502 - getProjectBlockState skips internal and archive Depends-On links
  ---
  duration_ms: 0.408961
  ...
# Subtest: getProjectBlockState is a no-op for terminal, daily, and non-project notes
ok 2503 - getProjectBlockState is a no-op for terminal, daily, and non-project notes
  ---
  duration_ms: 0.734683
  ...
# Subtest: projectLooksBlockedByPrjShortcut is the single [?] ^prj row
ok 2504 - projectLooksBlockedByPrjShortcut is the single [?] ^prj row
  ---
  duration_ms: 0.27242
  ...
# Subtest: taskHasProjectBlockedTag is token-bounded and does not match \#prj
ok 2505 - taskHasProjectBlockedTag is token-bounded and does not match \#prj
  ---
  duration_ms: 0.383783
  ...
# Subtest: setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
ok 2506 - setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
  ---
  duration_ms: 0.993097
  ...
# Subtest: reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
ok 2507 - reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
  ---
  duration_ms: 0.527468
  ...
# Subtest: reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
ok 2508 - reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
  ---
  duration_ms: 0.316795
  ...
# Subtest: reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
ok 2509 - reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
  ---
  duration_ms: 0.203939
  ...
# Subtest: ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
ok 2510 - ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
  ---
  duration_ms: 5.877294
  ...
# Subtest: recovery gate keeps a resident of a blocked project blocked after own deps close
ok 2511 - recovery gate keeps a resident of a blocked project blocked after own deps close
  ---
  duration_ms: 1.972336
  ...
# Subtest: recovery gate blocks residents on a future inline project date with no deps
ok 2512 - recovery gate blocks residents on a future inline project date with no deps
  ---
  duration_ms: 0.503872
  ...
# Subtest: planDeferredPomodoroLinkCleanup always deletes a last-child open entry
ok 2513 - planDeferredPomodoroLinkCleanup always deletes a last-child open entry
  ---
  duration_ms: 2.061998
  ...
# Subtest: TICKLER notice uses unblocked <date> when returnedBy is unblocked
ok 2514 - TICKLER notice uses unblocked <date> when returnedBy is unblocked
  ---
  duration_ms: 0.591069
  ...
# Subtest: recognition: a `^prj` parent in a project note carries its residents
ok 2515 - recognition: a `^prj` parent in a project note carries its residents
  ---
  duration_ms: 2.980662
  ...
# Subtest: recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
ok 2516 - recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
  ---
  duration_ms: 0.449899
  ...
# Subtest: add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
ok 2517 - add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
  ---
  duration_ms: 5.591066
  ...
# Subtest: add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
ok 2518 - add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
  ---
  duration_ms: 3.451812
  ...
# Subtest: guards: a same-note add to `^prj` refuses, including mixed batches
ok 2519 - guards: a same-note add to `^prj` refuses, including mixed batches
  ---
  duration_ms: 0.828472
  ...
# Subtest: guards: the stage disables same-note rows for `^prj` with `inside this project`
ok 2520 - guards: the stage disables same-note rows for `^prj` with `inside this project`
  ---
  duration_ms: 1.162099
  ...
# Subtest: guards: cycle detection includes the implicit resident edges (§13.6)
ok 2521 - guards: cycle detection includes the implicit resident edges (§13.6)
  ---
  duration_ms: 1.434329
  ...
# Subtest: removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
ok 2522 - removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
  ---
  duration_ms: 4.039444
  ...
# Subtest: removal: a resident with its own reason stays `[?]` without the tag (PDB3)
ok 2523 - removal: a resident with its own reason stays `[?]` without the tag (PDB3)
  ---
  duration_ms: 1.543147
  ...
# Subtest: removal without a registry defers to reconcile: residents keep `[?]` and the tag
ok 2524 - removal without a registry defers to reconcile: residents keep `[?]` and the tag
  ---
  duration_ms: 1.189903
  ...
# Subtest: writer: one gesture commits `^prj` and its residents in a single undo group
ok 2525 - writer: one gesture commits `^prj` and its residents in a single undo group
  ---
  duration_ms: 0.980843
  ...
# Subtest: writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
ok 2526 - writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
  ---
  duration_ms: 2.24121
  ...
# Subtest: notices: the project strings name the task, the flips, and the Pomodoro cleanup
ok 2527 - notices: the project strings name the task, the flips, and the Pomodoro cleanup
  ---
  duration_ms: 0.253393
  ...
# Subtest: mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
ok 2528 - mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
  ---
  duration_ms: 0.201165
  ...
# Subtest: api v3: removeDependencyByRef delegates removals to the single-transaction writer
ok 2529 - api v3: removeDependencyByRef delegates removals to the single-transaction writer
  ---
  duration_ms: 0.688696
  ...
# Subtest: api v3: openDependencyStageForRef opens the Depends on stage on the owning task
ok 2530 - api v3: openDependencyStageForRef opens the Depends on stage on the owning task
  ---
  duration_ms: 0.283361
  ...
# Subtest: internal links stay on the line but leave the field (PDR7)
ok 2531 - internal links stay on the line but leave the field (PDR7)
  ---
  duration_ms: 0.611939
  ...
# Subtest: removal from an unblocked ^prj never recovers own-reason residents (§13.10)
ok 2532 - removal from an unblocked ^prj never recovers own-reason residents (§13.10)
  ---
  duration_ms: 0.424991
  ...
# Subtest: resident recovery touches only tagged residents (§13.10)
ok 2533 - resident recovery touches only tagged residents (§13.10)
  ---
  duration_ms: 0.936919
  ...
# Subtest: stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
ok 2534 - stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
  ---
  duration_ms: 0.740865
  ...
# Subtest: projectDependentResidentKeys lists open residents with block ids
ok 2535 - projectDependentResidentKeys lists open residents with block ids
  ---
  duration_ms: 0.28303
  ...
# Subtest: navNoteScopeFlags marks daily notes; a missing writer stays null
ok 2536 - navNoteScopeFlags marks daily notes; a missing writer stays null
  ---
  duration_ms: 0.269424
  ...
# Subtest: reconcileBlockedScheduledTaskLine forwards scope flags to the writer
ok 2537 - reconcileBlockedScheduledTaskLine forwards scope flags to the writer
  ---
  duration_ms: 0.13084
  ...
# Subtest: parseProjectNoteFrontmatter ignores leftover scheduled keys
ok 2538 - parseProjectNoteFrontmatter ignores leftover scheduled keys
  ---
  duration_ms: 0.475448
  ...
# Subtest: formatTaskMoveProjectCountsNotice names blocked and recovered counts
ok 2539 - formatTaskMoveProjectCountsNotice names blocked and recovered counts
  ---
  duration_ms: 0.14667
  ...
# Subtest: PDS15: projectParentTarget keeps the path and drops alias and heading
ok 2540 - PDS15: projectParentTarget keeps the path and drops alias and heading
  ---
  duration_ms: 1.270587
  ...
# Subtest: PDS6: list-form, missing, and non-wikilink parents yield none
ok 2541 - PDS6: list-form, missing, and non-wikilink parents yield none
  ---
  duration_ms: 0.468595
  ...
# Subtest: PDS15: resolveProjectParentPath accepts alias, path, and heading forms
ok 2542 - PDS15: resolveProjectParentPath accepts alias, path, and heading forms
  ---
  duration_ms: 0.395906
  ...
# Subtest: PDS6: self, unresolved, and ambiguous basenames yield no parent
ok 2543 - PDS6: self, unresolved, and ambiguous basenames yield no parent
  ---
  duration_ms: 0.182428
  ...
# Subtest: buildProjectChildrenMap and descendants BFS skip cycles and cap depth
ok 2544 - buildProjectChildrenMap and descendants BFS skip cycles and cap depth
  ---
  duration_ms: 2.686961
  ...
# Subtest: PDS6: area, terminal, daily, and self-parent notes are not children
ok 2545 - PDS6: area, terminal, daily, and self-parent notes are not children
  ---
  duration_ms: 0.443738
  ...
# Subtest: PDG8: planner blocks child and grandchild ^prj and residents
ok 2546 - PDG8: planner blocks child and grandchild ^prj and residents
  ---
  duration_ms: 3.202436
  ...
# Subtest: PDG9: planner recovers tagged descendants with [unblocked::]
ok 2547 - PDG9: planner recovers tagged descendants with [unblocked::]
  ---
  duration_ms: 1.37742
  ...
# Subtest: PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
ok 2548 - PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
  ---
  duration_ms: 1.786872
  ...
# Subtest: PDG11: a tagged root re-asserts descendant tags and recovers nothing
ok 2549 - PDG11: a tagged root re-asserts descendant tags and recovers nothing
  ---
  duration_ms: 0.888757
  ...
# Subtest: tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
ok 2550 - tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
  ---
  duration_ms: 0.25133
  ...
# Subtest: tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
ok 2551 - tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
  ---
  duration_ms: 1.535382
  ...
# Subtest: tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
ok 2552 - tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
  ---
  duration_ms: 0.162039
  ...
# Subtest: tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
ok 2553 - tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
  ---
  duration_ms: 1.760341
  ...
# Subtest: PDG13: failProjectPrjInternalAdd refuses descendant targets
ok 2554 - PDG13: failProjectPrjInternalAdd refuses descendant targets
  ---
  duration_ms: 0.255688
  ...
# Subtest: PDG13: planDependencyEdit refuses a descendant add from the files map
ok 2555 - PDG13: planDependencyEdit refuses a descendant add from the files map
  ---
  duration_ms: 1.292297
  ...
# Subtest: PDG13: the stage disables descendant rows
ok 2556 - PDG13: the stage disables descendant rows
  ---
  duration_ms: 1.172529
  ...
# Subtest: reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
ok 2557 - reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
  ---
  duration_ms: 0.316484
  ...
# Subtest: tag proxy: removing the last own dep of a tagged ^prj recovers nobody
ok 2558 - tag proxy: removing the last own dep of a tagged ^prj recovers nobody
  ---
  duration_ms: 2.590787
  ...
# Subtest: PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
ok 2559 - PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
  ---
  duration_ms: 23.165496
  ...
# Subtest: PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
ok 2560 - PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
  ---
  duration_ms: 5.926327
  ...
# Subtest: PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
ok 2561 - PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
  ---
  duration_ms: 5.619251
  ...
# Subtest: PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
ok 2562 - PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
  ---
  duration_ms: 4.322675
  ...
# Subtest: PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
ok 2563 - PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
  ---
  duration_ms: 6.139164
  ...
# Subtest: PDG12: moving the project date due recovers descendants
ok 2564 - PDG12: moving the project date due recovers descendants
  ---
  duration_ms: 3.669569
  ...
# Subtest: PDG12: deleting the project date recovers descendants
ok 2565 - PDG12: deleting the project date recovers descendants
  ---
  duration_ms: 3.508821
  ...
# Subtest: PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
ok 2566 - PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
  ---
  duration_ms: 6.916648
  ...
# Subtest: PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
ok 2567 - PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
  ---
  duration_ms: 4.429418
  ...
# Subtest: Task Link Depends on writer preserves the internal-target guard on a project task
ok 2568 - Task Link Depends on writer preserves the internal-target guard on a project task
  ---
  duration_ms: 0.902914
  ...
# Subtest: api v3 removeDependencyByRef runs the recovery cascade for a linked project task
ok 2569 - api v3 removeDependencyByRef runs the recovery cascade for a linked project task
  ---
  duration_ms: 3.685849
  ...
# Subtest: counted Schedule writer cascades a future date through descendants
ok 2570 - counted Schedule writer cascades a future date through descendants
  ---
  duration_ms: 3.469004
  ...
# Subtest: counted subtree roots are ancestor-first and each descendant note is planned once
ok 2571 - counted subtree roots are ancestor-first and each descendant note is planned once
  ---
  duration_ms: 1.947639
  ...
# Subtest: Ctrl+D on the Depends on row removes the line and recovers the subtree
ok 2572 - Ctrl+D on the Depends on row removes the line and recovers the subtree
  ---
  duration_ms: 4.700696
  ...
# Subtest: a ^prj with no children reads no other note
ok 2573 - a ^prj with no children reads no other note
  ---
  duration_ms: 0.242843
  ...
# Subtest: single seeds from raw text, not display decorations
ok 2574 - single seeds from raw text, not display decorations
  ---
  duration_ms: 8.542522
  ...
# Subtest: legacy valid free wins; invalid and taken fall through
ok 2575 - legacy valid free wins; invalid and taken fall through
  ---
  duration_ms: 1.262661
  ...
# Subtest: batch reserves suffixes for two same-text tasks
ok 2576 - batch reserves suffixes for two same-text tasks
  ---
  duration_ms: 0.825036
  ...
# Subtest: counted-source, vault-single, and vault-counted seed per mode
ok 2577 - counted-source, vault-single, and vault-counted seed per mode
  ---
  duration_ms: 1.004198
  ...
# Subtest: cross-note uses the target note, never the dependent fallback
ok 2578 - cross-note uses the target note, never the dependent fallback
  ---
  duration_ms: 1.001823
  ...
# Subtest: staging writes nothing until confirmed
ok 2579 - staging writes nothing until confirmed
  ---
  duration_ms: 0.54458
  ...
# Subtest: Less often picker renders actual rows from 90 days and Escape writes nothing
ok 2580 - Less often picker renders actual rows from 90 days and Escape writes nothing
  ---
  duration_ms: 5.567913
  ...
# Subtest: Less often picker renders actual rows from 120 days and Escape writes nothing
ok 2581 - Less often picker renders actual rows from 120 days and Escape writes nothing
  ---
  duration_ms: 0.594195
  ...
# Subtest: Less often picker renders actual rows from 180 days and Escape writes nothing
ok 2582 - Less often picker renders actual rows from 180 days and Escape writes nothing
  ---
  duration_ms: 0.499734
  ...
# Subtest: renderFooter skips malformed hints and retains valid structured hints
ok 2583 - renderFooter skips malformed hints and retains valid structured hints
  ---
  duration_ms: 0.260247
  ...
# Subtest: Pending refresh modal previews the dated Work Log and confirms once
ok 2584 - Pending refresh modal previews the dated Work Log and confirms once
  ---
  duration_ms: 1.248744
  ...
# Subtest: dismissing the Pending refresh modal cancels without a summary
ok 2585 - dismissing the Pending refresh modal cancels without a summary
  ---
  duration_ms: 0.375798
  ...
# Subtest: nav LK1–LK18 parse relation grammar and reject the other relation parser
ok 2586 - nav LK1–LK18 parse relation grammar and reject the other relation parser
  ---
  duration_ms: 2.646103
  ...
# Subtest: nav LK14–LK19 context and cross-parse rules
ok 2587 - nav LK14–LK19 context and cross-parse rules
  ---
  duration_ms: 0.568606
  ...
# Subtest: nav MC5 refuses relation embeds and MC16 keeps LINKS while dropping LINKED FROM
ok 2588 - nav MC5 refuses relation embeds and MC16 keeps LINKS while dropping LINKED FROM
  ---
  duration_ms: 1.343586
  ...
# Subtest: nav MC15 hand-edit mirror ignores relation-only bursts and notices LINKED FROM once
ok 2589 - nav MC15 hand-edit mirror ignores relation-only bursts and notices LINKED FROM once
  ---
  duration_ms: 2.940054
  ...
# Subtest: Alt+N release from a NEXT landing advances with one composed toast
ok 2590 - Alt+N release from a NEXT landing advances with one composed toast
  ---
  duration_ms: 23.461655
  ...
# Subtest: counted Alt+N lands past every handled key in one jump
ok 2591 - counted Alt+N lands past every handled key in one jump
  ---
  duration_ms: 10.118623
  ...
# Subtest: a cancelled Alt+N release prompt stays and frees the lock
ok 2592 - a cancelled Alt+N release prompt stays and frees the lock
  ---
  duration_ms: 10.336899
  ...
# Subtest: Alt+N on a checklist landing stays with the plain notice
ok 2593 - Alt+N on a checklist landing stays with the plain notice
  ---
  duration_ms: 10.779425
  ...
# Subtest: Alt+N off a landing behaves exactly as today
ok 2594 - Alt+N off a landing behaves exactly as today
  ---
  duration_ms: 9.673633
  ...
# Subtest: Alt+N while the gesture lock is held is swallowed
ok 2595 - Alt+N while the gesture lock is held is swallowed
  ---
  duration_ms: 10.213393
  ...
# Subtest: a Task Card priority commit on NEXT advances, landing after the rich card
ok 2596 - a Task Card priority commit on NEXT advances, landing after the rich card
  ---
  duration_ms: 34.948026
  ...
# Subtest: dismissing the Task Card stays and frees the lock
ok 2597 - dismissing the Task Card stays and frees the lock
  ---
  duration_ms: 14.727066
  ...
# Subtest: a frontmatter-only project edit from the card stays
ok 2598 - a frontmatter-only project edit from the card stays
  ---
  duration_ms: 11.970869
  ...
# Subtest: a same-day priority schedule on a checklist row stays
ok 2599 - a same-day priority schedule on a checklist row stays
  ---
  duration_ms: 12.216538
  ...
# Subtest: a future schedule on a checklist row advances
ok 2600 - a future schedule on a checklist row advances
  ---
  duration_ms: 19.049657
  ...
# Subtest: a Task Card cancel on a checklist row advances with the cancel card first
ok 2601 - a Task Card cancel on a checklist row advances with the cancel card first
  ---
  duration_ms: 14.198152
  ...
# Subtest: Ctrl+Shift+M from a landing follows the task and never advances
ok 2602 - Ctrl+Shift+M from a landing follows the task and never advances
  ---
  duration_ms: 14.375921
  ...
# Subtest: Ctrl+Shift+M from a checklist landing keeps the destination focus
ok 2603 - Ctrl+Shift+M from a checklist landing keeps the destination focus
  ---
  duration_ms: 11.406561
  ...
# Subtest: ]s after a landed move resumes at the successor despite the line shift
ok 2604 - ]s after a landed move resumes at the successor despite the line shift
  ---
  duration_ms: 31.030188
  ...
# Subtest: [s after a landed move resumes at the predecessor
ok 2605 - [s after a landed move resumes at the predecessor
  ---
  duration_ms: 10.351286
  ...
# Subtest: a counted move from a landing resumes past every moved target
ok 2606 - a counted move from a landing resumes past every moved target
  ---
  duration_ms: 10.16461
  ...
# Subtest: counted Ctrl+Shift+M command dispatch preserves a landed move count
ok 2607 - counted Ctrl+Shift+M command dispatch preserves a landed move count
  ---
  duration_ms: 19.022084
  ...
# Subtest: a stale landing is not parked
ok 2608 - a stale landing is not parked
  ---
  duration_ms: 10.418144
  ...
# Subtest: Ctrl+Shift+M while the gesture lock is held is swallowed
ok 2609 - Ctrl+Shift+M while the gesture lock is held is swallowed
  ---
  duration_ms: 0.420784
  ...
# Subtest: dismissing the move picker stays and frees the lock
ok 2610 - dismissing the move picker stays and frees the lock
  ---
  duration_ms: 8.956273
  ...
# Subtest: Ctrl+Shift+M off a landing behaves exactly as today
ok 2611 - Ctrl+Shift+M off a landing behaves exactly as today
  ---
  duration_ms: 9.940432
  ...
# Subtest: answer, move, answer stays in queue order past an accumulator alias
ok 2612 - answer, move, answer stays in queue order past an accumulator alias
  ---
  duration_ms: 4.067569
  ...
# Subtest: a move park ignores a stale accumulator alias
ok 2613 - a move park ignores a stale accumulator alias
  ---
  duration_ms: 0.538739
  ...
# Subtest: a re-indexed origin still advances from the landed row
ok 2614 - a re-indexed origin still advances from the landed row
  ---
  duration_ms: 2.881463
  ...
# Subtest: a landed move park clears the current review task
ok 2615 - a landed move park clears the current review task
  ---
  duration_ms: 0.457493
  ...
# Subtest: predicate: reviewOutcomeResolves across tiers and kinds
ok 2616 - predicate: reviewOutcomeResolves across tiers and kinds
  ---
  duration_ms: 2.076385
  ...
# Subtest: findReviewResumeIndex identifies rows by path and text
ok 2617 - findReviewResumeIndex identifies rows by path and text
  ---
  duration_ms: 0.449328
  ...
# Subtest: buildReviewMoveAnchor parks text-identified resume neighbours
ok 2618 - buildReviewMoveAnchor parks text-identified resume neighbours
  ---
  duration_ms: 0.774569
  ...
# Subtest: planReviewJump with a move anchor resumes at the walk neighbour
ok 2619 - planReviewJump with a move anchor resumes at the walk neighbour
  ---
  duration_ms: 1.465418
  ...
# Subtest: capture: null off a landing
ok 2620 - capture: null off a landing
  ---
  duration_ms: 4.745421
  ...
# Subtest: capture: frozen origin shape, BUSY while locked, expiry
ok 2621 - capture: frozen origin shape, BUSY while locked, expiry
  ---
  duration_ms: 0.701339
  ...
# Subtest: successor picker keeps a captured completion locked through selection and one walk toast
ok 2622 - successor picker keeps a captured completion locked through selection and one walk toast
  ---
  duration_ms: 17.701616
  ...
# Subtest: continue: refuses stale origins, showing the notice once
ok 2623 - continue: refuses stale origins, showing the notice once
  ---
  duration_ms: 7.601295
  ...
# Subtest: continue: stays on null and non-resolving outcomes
ok 2624 - continue: stays on null and non-resolving outcomes
  ---
  duration_ms: 1.157059
  ...
# Subtest: continue: stays for lane answers and mixed-version completes on checklist rows
ok 2625 - continue: stays for lane answers and mixed-version completes on checklist rows
  ---
  duration_ms: 3.329688
  ...
# Subtest: continue: a resolving lane answer advances exactly once with one composed toast
ok 2626 - continue: a resolving lane answer advances exactly once with one composed toast
  ---
  duration_ms: 3.531053
  ...
# Subtest: continue: counted handled refs land past every handled key in one jump
ok 2627 - continue: counted handled refs land past every handled key in one jump
  ---
  duration_ms: 2.473454
  ...
# Subtest: continue: wrap is announced and the empty queue composes the empty notice
ok 2628 - continue: wrap is announced and the empty queue composes the empty notice
  ---
  duration_ms: 2.731686
  ...
# Subtest: continue: anchor-only planning survives cursor drift and lagging queues
ok 2629 - continue: anchor-only planning survives cursor drift and lagging queues
  ---
  duration_ms: 2.257691
  ...
# Subtest: continue: POST origins never wrap
ok 2630 - continue: POST origins never wrap
  ---
  duration_ms: 1.135258
  ...
# Subtest: complete: the last lane row before POST stays with the next-step toast
ok 2631 - complete: the last lane row before POST stays with the next-step toast
  ---
  duration_ms: 0.883296
  ...
# Subtest: complete: a wrap onto a skipped PRE row stays
ok 2632 - complete: a wrap onto a skipped PRE row stays
  ---
  duration_ms: 2.026319
  ...
# Subtest: complete: a step into ROTTEN shows the boundary line
ok 2633 - complete: a step into ROTTEN shows the boundary line
  ---
  duration_ms: 2.185464
  ...
# Subtest: busy: walk keys, refresh, claim, and capture are swallowed in the settle window
ok 2634 - busy: walk keys, refresh, claim, and capture are swallowed in the settle window
  ---
  duration_ms: 3.641654
  ...
# Subtest: advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
ok 2635 - advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
  ---
  duration_ms: 3.528608
  ...
# Subtest: advance: decay choices advance except reword, with no preamble of their own
ok 2636 - advance: decay choices advance except reword, with no preamble of their own
  ---
  duration_ms: 0.609464
  ...
# Subtest: jump history: same-note and cross-note auto-advances record, and <C-o> returns
ok 2637 - jump history: same-note and cross-note auto-advances record, and <C-o> returns
  ---
  duration_ms: 6.591988
  ...
# Subtest: jump history: a manual ]s also records its landing
ok 2638 - jump history: a manual ]s also records its landing
  ---
  duration_ms: 0.922692
  ...
# Subtest: api: reviewWalk v3 is frozen with version 1, degrades null, never throws
ok 2639 - api: reviewWalk v3 is frozen with version 1, degrades null, never throws
  ---
  duration_ms: 1.804456
  ...
# Subtest: walk identity: a stale accumulator key never moves the anchor
ok 2640 - walk identity: a stale accumulator key never moves the anchor
  ---
  duration_ms: 0.354186
  ...
# Subtest: walk identity: a lagging answered row stays excluded
ok 2641 - walk identity: a lagging answered row stays excluded
  ---
  duration_ms: 0.187228
  ...
# Subtest: walk identity: a line-shifting answer lands on the true successor by text
ok 2642 - walk identity: a line-shifting answer lands on the true successor by text
  ---
  duration_ms: 0.336682
  ...
# Subtest: walk identity: legacy anchors without text resolve as before
ok 2643 - walk identity: legacy anchors without text resolve as before
  ---
  duration_ms: 0.307557
  ...
# Subtest: walk identity: matchFreshStampRefs prefers text over line
ok 2644 - walk identity: matchFreshStampRefs prefers text over line
  ---
  duration_ms: 0.168532
  ...
# Subtest: walk identity: collectReviewAnswerKeys separates position from exclusion
ok 2645 - walk identity: collectReviewAnswerKeys separates position from exclusion
  ---
  duration_ms: 0.448727
  ...
# Subtest: return: planReviewWalkReturn pure decisions
ok 2646 - return: planReviewWalkReturn pure decisions
  ---
  duration_ms: 0.330732
  ...
# Subtest: return: same-note ]s returns then steps, both directions
ok 2647 - return: same-note ]s returns then steps, both directions
  ---
  duration_ms: 1.396076
  ...
# Subtest: return: a different due row returns instead of stepping from there
ok 2648 - return: a different due row returns instead of stepping from there
  ---
  duration_ms: 0.494585
  ...
# Subtest: return: cross-note return re-arms and records <C-o>
ok 2649 - return: cross-note return re-arms and records <C-o>
  ---
  duration_ms: 5.42512
  ...
# Subtest: return: a count is consumed and ignored
ok 2650 - return: a count is consumed and ignored
  ---
  duration_ms: 0.589135
  ...
# Subtest: return: endpoints never return
ok 2651 - return: endpoints never return
  ---
  duration_ms: 0.558106
  ...
# Subtest: return: its own stamp ends it
ok 2652 - return: its own stamp ends it
  ---
  duration_ms: 0.747527
  ...
# Subtest: return: a stamp elsewhere does not end it
ok 2653 - return: a stamp elsewhere does not end it
  ---
  duration_ms: 0.58143
  ...
# Subtest: return: answers move the current task, a stopped Ctrl+Enter clears it
ok 2654 - return: answers move the current task, a stopped Ctrl+Enter clears it
  ---
  duration_ms: 3.14214
  ...
# Subtest: return: a stale landing falls through in the same press
ok 2655 - return: a stale landing falls through in the same press
  ---
  duration_ms: 0.297408
  ...
# Subtest: return: a day change never returns
ok 2656 - return: a day change never returns
  ---
  duration_ms: 0.386789
  ...
# Subtest: predicate: reviewOutcomeResolves for the RECURRING resolution table
ok 2657 - predicate: reviewOutcomeResolves for the RECURRING resolution table
  ---
  duration_ms: 0.422166
  ...
# Subtest: recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
ok 2658 - recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
  ---
  duration_ms: 0.189582
  ...
# Subtest: return: a RECURRING landing rearms the current-task return
ok 2659 - return: a RECURRING landing rearms the current-task return
  ---
  duration_ms: 0.256339
  ...
# Subtest: review answer outcome vectors map to the schema vocabulary
ok 2660 - review answer outcome vectors map to the schema vocabulary
  ---
  duration_ms: 1.240679
  ...
# Subtest: event builder uses the walk row key and its tier, once per distinct key
ok 2661 - event builder uses the walk row key and its tier, once per distinct key
  ---
  duration_ms: 1.144736
  ...
# Subtest: journal appends are queued and failures retain events without failing answers
ok 2662 - journal appends are queued and failures retain events without failing answers
  ---
  duration_ms: 5.790148
  ...
# Subtest: card after-line outcomes map done, drop, defer, sequence, and card
ok 2663 - card after-line outcomes map done, drop, defer, sequence, and card
  ---
  duration_ms: 1.302939
  ...
# Subtest: journal events carry plugin@manifest version with a 2.x fallback
ok 2664 - journal events carry plugin@manifest version with a 2.x fallback
  ---
  duration_ms: 1.652817
  ...
# Subtest: write failures show one notice per burst and a recovery notice
ok 2665 - write failures show one notice per burst and a recovery notice
  ---
  duration_ms: 1.331783
  ...
# Subtest: missing api.stats shows one session notice and later delivers retained events
ok 2666 - missing api.stats shows one session notice and later delivers retained events
  ---
  duration_ms: 1.660181
  ...
# Subtest: validation rejects drop the event and continue the drain
ok 2667 - validation rejects drop the event and continue the drain
  ---
  duration_ms: 1.128414
  ...
# Subtest: pending journal events cap at 500 and warn once per burst
ok 2668 - pending journal events cap at 500 and warn once per burst
  ---
  duration_ms: 3.415793
  ...
# Subtest: decay config defaults to enabled with one roll per level
ok 2669 - decay config defaults to enabled with one roll per level
  ---
  duration_ms: 2.448706
  ...
# Subtest: decay:false disables decay and level rolls are accepted but ignored
ok 2670 - decay:false disables decay and level rolls are accepted but ignored
  ---
  duration_ms: 0.589756
  ...
# Subtest: decay.rolls sets the limit and levels[].rolls overrides it
ok 2671 - decay.rolls sets the limit and levels[].rolls overrides it
  ---
  duration_ms: 0.226914
  ...
# Subtest: decay config rejects bad rolls, unknown keys and non-priority use
ok 2672 - decay config rejects bad rolls, unknown keys and non-priority use
  ---
  duration_ms: 0.4559
  ...
# Subtest: classifyScheduleLogRollReason sorts automatic heads from deliberate ones
ok 2673 - classifyScheduleLogRollReason sorts automatic heads from deliberate ones
  ---
  duration_ms: 0.644852
  ...
# Subtest: conformance vectors 1-10: streaks at P2 with the default limit
ok 2674 - conformance vectors 1-10: streaks at P2 with the default limit
  ---
  duration_ms: 2.423608
  ...
# Subtest: conformance vectors 11-15: custom limits, disabled decay and edges
ok 2675 - conformance vectors 11-15: custom limits, disabled decay and edges
  ---
  duration_ms: 0.713844
  ...
# Subtest: the streak reader follows log grammar: legacy labels, nesting and stops
ok 2676 - the streak reader follows log grammar: legacy labels, nesting and stops
  ---
  duration_ms: 0.448717
  ...
# Subtest: rollPriorityRecommendationDate avoids the current date when the window has room
ok 2677 - rollPriorityRecommendationDate avoids the current date when the window has room
  ---
  duration_ms: 0.601469
  ...
# Subtest: decay and cancel reason formatters use the exact ladder copy
ok 2678 - decay and cancel reason formatters use the exact ladder copy
  ---
  duration_ms: 0.464386
  ...
# Subtest: the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
ok 2679 - the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
  ---
  duration_ms: 0.357913
  ...
# Subtest: the planner returns null without a configured priority
ok 2680 - the planner returns null without a configured priority
  ---
  duration_ms: 0.16219
  ...
# Subtest: buildPriorityRollPreviewModel carries the row copy for every kind
ok 2681 - buildPriorityRollPreviewModel carries the row copy for every kind
  ---
  duration_ms: 0.508561
  ...
# Subtest: picker-single recognizes the recommended-roll keypress
ok 2682 - picker-single recognizes the recommended-roll keypress
  ---
  duration_ms: 0.138575
  ...
# Subtest: picker-single stage-two footers carry the recommended-roll hints
ok 2683 - picker-single stage-two footers carry the recommended-roll hints
  ---
  duration_ms: 0.315232
  ...
# Subtest: picker-single shares one roll between the preview and the pinned row
ok 2684 - picker-single shares one roll between the preview and the pinned row
  ---
  duration_ms: 0.341612
  ...
# Subtest: picker-single plans the next-roll hint for the notice chips
ok 2685 - picker-single plans the next-roll hint for the notice chips
  ---
  duration_ms: 0.57624
  ...
# Subtest: picker-single notice cards name the roll, decay and next press
ok 2686 - picker-single notice cards name the roll, decay and next press
  ---
  duration_ms: 1.567173
  ...
# Subtest: picker-single decay payload and preview-target comparison
ok 2687 - picker-single decay payload and preview-target comparison
  ---
  duration_ms: 0.333126
  ...
# Subtest: picker-counted plans one recommendation per target with skips
ok 2688 - picker-counted plans one recommendation per target with skips
  ---
  duration_ms: 1.876022
  ...
# Subtest: picker-counted batch preview, footer and notice copy
ok 2689 - picker-counted batch preview, footer and notice copy
  ---
  duration_ms: 1.473694
  ...
# Subtest: picker-counted composes cancel then set-priority into one postimage
ok 2690 - picker-counted composes cancel then set-priority into one postimage
  ---
  duration_ms: 3.315672
  ...
# Subtest: picker-counted refuses a recurring cancel as one batch
ok 2691 - picker-counted refuses a recurring cancel as one batch
  ---
  duration_ms: 0.488483
  ...
# Subtest: recommended roll recovers with [unblocked::] when the writer is passed
ok 2692 - recommended roll recovers with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.82192
  ...
# Subtest: picker-counted stale lines refuse and new options stay byte-identical
ok 2693 - picker-counted stale lines refuse and new options stay byte-identical
  ---
  duration_ms: 1.132983
  ...
# Subtest: picker-links aggregates one recommendation per note
ok 2694 - picker-links aggregates one recommendation per note
  ---
  duration_ms: 1.138524
  ...
# Subtest: picker-links refuses a recurring cancel as one batch
ok 2695 - picker-links refuses a recurring cancel as one batch
  ---
  duration_ms: 0.365378
  ...
# Subtest: picker-links takes a single recommended roll with Ctrl+Enter
ok 2696 - picker-links takes a single recommended roll with Ctrl+Enter
  ---
  duration_ms: 33.669464
  ...
# Subtest: picker-links shows no pinned roll row in stage two
ok 2697 - picker-links shows no pinned roll row in stage two
  ---
  duration_ms: 6.553535
  ...
# Subtest: picker-links decays and cancels a single Task Link
ok 2698 - picker-links decays and cancels a single Task Link
  ---
  duration_ms: 8.419859
  ...
# Subtest: picker-links applies a mixed batch across two notes
ok 2699 - picker-links applies a mixed batch across two notes
  ---
  duration_ms: 5.462832
  ...
# Subtest: picker-links refuses the whole batch when a linked note changed
ok 2700 - picker-links refuses the whole batch when a linked note changed
  ---
  duration_ms: 2.1368
  ...
# Subtest: picker-links prunes today's open Pomodoro links
ok 2701 - picker-links prunes today's open Pomodoro links
  ---
  duration_ms: 5.107753
  ...
# Subtest: picker-single Ctrl+Enter rolls a P2 task in one undo group
ok 2702 - picker-single Ctrl+Enter rolls a P2 task in one undo group
  ---
  duration_ms: 18.369
  ...
# Subtest: picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
ok 2703 - picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
  ---
  duration_ms: 13.158868
  ...
# Subtest: picker-single opens a ^prj task on inline scheduled for an immediate roll
ok 2704 - picker-single opens a ^prj task on inline scheduled for an immediate roll
  ---
  duration_ms: 15.043106
  ...
# Subtest: picker-counted opens on scheduled for an immediate mixed batch
ok 2705 - picker-counted opens on scheduled for an immediate mixed batch
  ---
  duration_ms: 15.247366
  ...
# Subtest: picker-links opens on scheduled for an immediate roll
ok 2706 - picker-links opens on scheduled for an immediate roll
  ---
  duration_ms: 12.535407
  ...
# Subtest: picker-single Ctrl+Enter decays a P2 task in one undo group
ok 2707 - picker-single Ctrl+Enter decays a P2 task in one undo group
  ---
  duration_ms: 11.810964
  ...
# Subtest: picker-single Ctrl+Enter cancels a P4 task in one undo group
ok 2708 - picker-single Ctrl+Enter cancels a P4 task in one undo group
  ---
  duration_ms: 11.728827
  ...
# Subtest: picker-single Ctrl+Enter in stage two writes the recommended roll
ok 2709 - picker-single Ctrl+Enter in stage two writes the recommended roll
  ---
  duration_ms: 12.00604
  ...
# Subtest: picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
ok 2710 - picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
  ---
  duration_ms: 3.520873
  ...
# Subtest: picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
ok 2711 - picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
  ---
  duration_ms: 4.61923
  ...
# Subtest: picker-single recurring P4 past the limit refuses and keeps the picker open
ok 2712 - picker-single recurring P4 past the limit refuses and keeps the picker open
  ---
  duration_ms: 11.46884
  ...
# Subtest: picker-single stale tasks refuse and re-render the decay preview
ok 2713 - picker-single stale tasks refuse and re-render the decay preview
  ---
  duration_ms: 11.922947
  ...
# Subtest: picker-single Ctrl+R on the card re-rolls the recommendation date
ok 2714 - picker-single Ctrl+R on the card re-rolls the recommendation date
  ---
  duration_ms: 4.077907
  ...
# Subtest: picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
ok 2715 - picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
  ---
  duration_ms: 1.175444
  ...
# Subtest: picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
ok 2716 - picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
  ---
  duration_ms: 10.73002
  ...
# Subtest: picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
ok 2717 - picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
  ---
  duration_ms: 11.566587
  ...
# Subtest: picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
ok 2718 - picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
  ---
  duration_ms: 11.911606
  ...
# Subtest: picker-counted Ctrl+Enter refuses when a target line changed
ok 2719 - picker-counted Ctrl+Enter refuses when a target line changed
  ---
  duration_ms: 10.5416
  ...
# Subtest: picker-counted Ctrl+Enter refuses a recurring cancel batch
ok 2720 - picker-counted Ctrl+Enter refuses a recurring cancel batch
  ---
  duration_ms: 11.385974
  ...
# Subtest: recommended roll on Pending offers a Work Log with the frozen date
ok 2721 - recommended roll on Pending offers a Work Log with the frozen date
  ---
  duration_ms: 1019.022925
  ...
# Subtest: recommended roll blank summary skips the Work Log without a fallback
ok 2722 - recommended roll blank summary skips the Work Log without a fallback
  ---
  duration_ms: 1017.18874
  ...
# Subtest: Ctrl+Enter in the Work Log stage confirms instead of re-rolling
ok 2723 - Ctrl+Enter in the Work Log stage confirms instead of re-rolling
  ---
  duration_ms: 1031.521692
  ...
# Subtest: counted recommended mixed batch logs only eligible roll and decay targets
ok 2724 - counted recommended mixed batch logs only eligible roll and decay targets
  ---
  duration_ms: 1022.584725
  ...
# Subtest: Task Link recommended roll deletes the emptied Pomodoro in the same daily write
ok 2725 - Task Link recommended roll deletes the emptied Pomodoro in the same daily write
  ---
  duration_ms: 3.90112
  ...
# Subtest: lane commit stamps an open Ready task
ok 2726 - lane commit stamps an open Ready task
  ---
  duration_ms: 2.866735
  ...
# Subtest: lane release stamps an open Next task
ok 2727 - lane release stamps an open Next task
  ---
  duration_ms: 0.46116
  ...
# Subtest: lane without a stamper leaves lines as they were
ok 2728 - lane without a stamper leaves lines as they were
  ---
  duration_ms: 0.192057
  ...
# Subtest: counted property set stamps every rewritten open task
ok 2729 - counted property set stamps every rewritten open task
  ---
  duration_ms: 2.208116
  ...
# Subtest: counted delete-property stamps the rewritten task
ok 2730 - counted delete-property stamps the rewritten task
  ---
  duration_ms: 0.524612
  ...
# Subtest: stamp lands before the suffix after a priority edit on a stamped line
ok 2731 - stamp lands before the suffix after a priority edit on a stamped line
  ---
  duration_ms: 0.515444
  ...
# Subtest: recurring tasks are never stamped
ok 2732 - recurring tasks are never stamped
  ---
  duration_ms: 0.271288
  ...
# Subtest: cancel never stamps
ok 2733 - cancel never stamps
  ---
  duration_ms: 1.05791
  ...
# Subtest: fresh and refresh never go through the end-append writers
ok 2734 - fresh and refresh never go through the end-append writers
  ---
  duration_ms: 0.41882
  ...
# Subtest: counted dependency edit stamps the rewritten parent
ok 2735 - counted dependency edit stamps the rewritten parent
  ---
  duration_ms: 5.78172
  ...
# Subtest: moved tasks are stamped at their destination
ok 2736 - moved tasks are stamped at their destination
  ---
  duration_ms: 2.609173
  ...
# Subtest: move without a stamper leaves lines as they were
ok 2737 - move without a stamper leaves lines as they were
  ---
  duration_ms: 0.622268
  ...
# Subtest: refresh row shows the effective interval in task mode
ok 2738 - refresh row shows the effective interval in task mode
  ---
  duration_ms: 0.762807
  ...
# Subtest: refresh row hides without the api and on closed tasks
ok 2739 - refresh row hides without the api and on closed tasks
  ---
  duration_ms: 0.131691
  ...
# Subtest: refresh row covers counted and link modes, including mixed
ok 2740 - refresh row covers counted and link modes, including mixed
  ---
  duration_ms: 0.275305
  ...
# Subtest: refresh value items offer presets and use default
ok 2741 - refresh value items offer presets and use default
  ---
  duration_ms: 0.725856
  ...
# Subtest: setRefreshLine stamps and sets or clears the interval
ok 2742 - setRefreshLine stamps and sets or clears the interval
  ---
  duration_ms: 0.393772
  ...
# Subtest: 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
ok 2743 - 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
  ---
  duration_ms: 6.950352
  ...
# Subtest: Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
ok 2744 - Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
  ---
  duration_ms: 2.89586
  ...
# Subtest: filtering expands matches, collapse state survives clearing, and hidden marks still submit
ok 2745 - filtering expands matches, collapse state survives clearing, and hidden marks still submit
  ---
  duration_ms: 4.480686
  ...
# Subtest: group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
ok 2746 - group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
  ---
  duration_ms: 1.28852
  ...
# Subtest: Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
ok 2747 - Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
  ---
  duration_ms: 0.665701
  ...
# Subtest: Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
ok 2748 - Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
  ---
  duration_ms: 3.259234
  ...
# Subtest: the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
ok 2749 - the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
  ---
  duration_ms: 0.843931
  ...
# Subtest: destination override shapes normalize and label
ok 2750 - destination override shapes normalize and label
  ---
  duration_ms: 0.272821
  ...
# Subtest: destination picker detection needs block-id-prompt api v1 with pick
ok 2751 - destination picker detection needs block-id-prompt api v1 with pick
  ---
  duration_ms: 0.488833
  ...
# Subtest: Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks
ok 2752 - Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks
  ---
  duration_ms: 2.349798
  ...
# Subtest: Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked
ok 2753 - Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked
  ---
  duration_ms: 1.066096
  ...
# Subtest: a cancelled destination pick and a missing picker leave rows untouched
ok 2754 - a cancelled destination pick and a missing picker leave rows untouched
  ---
  duration_ms: 1.382259
  ...
# Subtest: unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
ok 2755 - unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
  ---
  duration_ms: 1.039225
  ...
# Subtest: card model builds stable rows, scope metadata, and an existing recommendation
ok 2756 - card model builds stable rows, scope metadata, and an existing recommendation
  ---
  duration_ms: 8.465357
  ...
# Subtest: explicit preview builder matches writer rolls and deduplicates linked targets
ok 2757 - explicit preview builder matches writer rolls and deduplicates linked targets
  ---
  duration_ms: 0.855013
  ...
# Subtest: counted and linked card models report real target counts and mixed values
ok 2758 - counted and linked card models report real target counts and mixed values
  ---
  duration_ms: 4.047248
  ...
# Subtest: priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
ok 2759 - priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
  ---
  duration_ms: 2.196564
  ...
# Subtest: Escape, bare q, and Ctrl+[ close the card; nothing else does
ok 2760 - Escape, bare q, and Ctrl+[ close the card; nothing else does
  ---
  duration_ms: 0.895891
  ...
# Subtest: close keys never fire during composition or inside a text field
ok 2761 - close keys never fire during composition or inside a text field
  ---
  duration_ms: 1.331953
  ...
# Subtest: unavailable actions, input composition, and repeats stay safe
ok 2762 - unavailable actions, input composition, and repeats stay safe
  ---
  duration_ms: 1.910759
  ...
# Subtest: Blocks row summarizes warm-cache dependents and their last open reason
ok 2763 - Blocks row summarizes warm-cache dependents and their last open reason
  ---
  duration_ms: 1.045807
  ...
# Subtest: Blocks row refuses closed tasks and unencodable paths without an id
ok 2764 - Blocks row refuses closed tasks and unencodable paths without an id
  ---
  duration_ms: 1.943722
  ...
# Subtest: key resolver table covers lane state, API availability, and modifier guards
ok 2765 - key resolver table covers lane state, API availability, and modifier guards
  ---
  duration_ms: 1.438587
  ...
# Subtest: recurring cancellation and blocked lanes expose reasons instead of writes
ok 2766 - recurring cancellation and blocked lanes expose reasons instead of writes
  ---
  duration_ms: 0.605957
  ...
# Subtest: identity keys distinguish linked notes that share a line number
ok 2767 - identity keys distinguish linked notes that share a line number
  ---
  duration_ms: 1.474566
  ...
# Subtest: planScheduleReview opens for a bare date and skips when reason is known without Work Log
ok 2768 - planScheduleReview opens for a bare date and skips when reason is known without Work Log
  ---
  duration_ms: 0.85352
  ...
# Subtest: planScheduleReview counts unique tasks when Task Links repeat a target
ok 2769 - planScheduleReview counts unique tasks when Task Links repeat a target
  ---
  duration_ms: 0.31395
  ...
# Subtest: bare date on Ready opens a reason-only review and writes nothing until Enter
ok 2770 - bare date on Ready opens a reason-only review and writes nothing until Enter
  ---
  duration_ms: 19.207838
  ...
# Subtest: typed reason and blank reason on an existing Schedule Log keep per-target rules
ok 2771 - typed reason and blank reason on an existing Schedule Log keep per-target rules
  ---
  duration_ms: 8.323404
  ...
# Subtest: Ready vs Next vs Pending: only Next/Pending show Work summary
ok 2772 - Ready vs Next vs Pending: only Next/Pending show Work summary
  ---
  duration_ms: 9.866581
  ...
# Subtest: inline reason on Ready dispatches immediately; on Next it still reviews Work summary
ok 2773 - inline reason on Ready dispatches immediately; on Next it still reviews Work summary
  ---
  duration_ms: 4.729602
  ...
# Subtest: Tab moves from Reason to Work summary and Enter commits from either field
ok 2774 - Tab moves from Reason to Work summary and Enter commits from either field
  ---
  duration_ms: 2.127042
  ...
# Subtest: Back and Escape at both review fields write nothing
ok 2775 - Back and Escape at both review fields write nothing
  ---
  duration_ms: 6.940023
  ...
# Subtest: a target changed during review refuses with no write
ok 2776 - a target changed during review refuses with no write
  ---
  duration_ms: 2.737066
  ...
# Subtest: counted mixed targets share one review and one adapter call
ok 2777 - counted mixed targets share one review and one adapter call
  ---
  duration_ms: 3.996642
  ...
# Subtest: linked notes with equal line numbers both qualify
ok 2778 - linked notes with equal line numbers both qualify
  ---
  duration_ms: 2.757626
  ...
# Subtest: project lifecycle review names propagation and still writes once
ok 2779 - project lifecycle review names propagation and still writes once
  ---
  duration_ms: 2.203037
  ...
# Subtest: priority picks still skip the combined review and keep Work Log-only prompts
ok 2780 - priority picks still skip the combined review and keep Work Log-only prompts
  ---
  duration_ms: 1.810738
  ...
# Subtest: a typed date from the card's schedule row uses the combined review
ok 2781 - a typed date from the card's schedule row uses the combined review
  ---
  duration_ms: 1.640192
  ...
# Subtest: scheduling a Pending task goes straight to the combined review, never serial prompts
ok 2782 - scheduling a Pending task goes straight to the combined review, never serial prompts
  ---
  duration_ms: 1.30937
  ...
# Subtest: classic parser keeps ISO, M/D, and signed units and ignores concise forms
ok 2783 - classic parser keeps ISO, M/D, and signed units and ignores concise forms
  ---
  duration_ms: 1.2989
  ...
# Subtest: typed schedule resolver covers bare days, units, weekdays, and inline reasons
ok 2784 - typed schedule resolver covers bare days, units, weekdays, and inline reasons
  ---
  duration_ms: 1.12601
  ...
# Subtest: weekdays resolve to the next occurrence strictly after today
ok 2785 - weekdays resolve to the next occurrence strictly after today
  ---
  duration_ms: 0.189993
  ...
# Subtest: invalid leap dates, end-of-month offsets, and December rollover
ok 2786 - invalid leap dates, end-of-month offsets, and December rollover
  ---
  duration_ms: 0.359025
  ...
# Subtest: negative, overflow, malformed, and preset-filter queries are rejected without dates
ok 2787 - negative, overflow, malformed, and preset-filter queries are rejected without dates
  ---
  duration_ms: 0.169744
  ...
# Subtest: DST local-calendar arithmetic stays on calendar days in America/New_York
ok 2788 - DST local-calendar arithmetic stays on calendar days in America/New_York
  ---
  duration_ms: 88.000738
  ...
# Subtest: Task Card date stage previews weekday, ISO, relative distance, and rollover year
ok 2789 - Task Card date stage previews weekday, ISO, relative distance, and rollover year
  ---
  duration_ms: 14.18126
  ...
# Subtest: inline reason is preserved on the preview and skips the reason stage
ok 2790 - inline reason is preserved on the preview and skips the reason stage
  ---
  duration_ms: 11.96092
  ...
# Subtest: Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
ok 2791 - Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
  ---
  duration_ms: 4.459787
  ...
# Subtest: Shift+Enter on a Ready task commits in four gestures without a Work Log
ok 2792 - Shift+Enter on a Ready task commits in four gestures without a Work Log
  ---
  duration_ms: 2.959011
  ...
# Subtest: invalid typed dates render an error preview and do not write
ok 2793 - invalid typed dates render an error preview and do not write
  ---
  duration_ms: 2.659659
  ...
# Subtest: the card's schedule stage always uses the concise resolver
ok 2794 - the card's schedule stage always uses the concise resolver
  ---
  duration_ms: 1.90113
  ...
# Subtest: tomorrow stays a preset filter and is not stolen as a typed date
ok 2795 - tomorrow stays a preset filter and is not stolen as a typed date
  ---
  duration_ms: 1.496819
  ...
# Subtest: mixed Task Links preview one date and freeze that action with the inline reason
ok 2796 - mixed Task Links preview one date and freeze that action with the inline reason
  ---
  duration_ms: 7.497958
  ...
# Subtest: Ctrl+Enter still takes the recommended roll from the Task Card date stage
ok 2797 - Ctrl+Enter still takes the recommended roll from the Task Card date stage
  ---
  duration_ms: 3.11049
  ...
# Subtest: Modal harness models Obsidian 1.14 attachment and idempotent close
ok 2798 - Modal harness models Obsidian 1.14 attachment and idempotent close
  ---
  duration_ms: 1.508711
  ...
# Subtest: styles share key-card tokens and compact Task Card dimensions
ok 2799 - styles share key-card tokens and compact Task Card dimensions
  ---
  duration_ms: 0.285656
  ...
# Subtest: card renderer paints header, banner, strip, stable rows, more, and footer from the model
ok 2800 - card renderer paints header, banner, strip, stable rows, more, and footer from the model
  ---
  duration_ms: 11.896227
  ...
# Subtest: renderer does not consume randomness or invent recommendation data
ok 2801 - renderer does not consume randomness or invent recommendation data
  ---
  duration_ms: 2.128264
  ...
# Subtest: no-recommendation, cancel, mixed, long text, missing API, and error states render
ok 2802 - no-recommendation, cancel, mixed, long text, missing API, and error states render
  ---
  duration_ms: 5.531052
  ...
# Subtest: counted and linked cards disclose mixed values and Task Link notes
ok 2803 - counted and linked cards disclose mixed values and Task Link notes
  ---
  duration_ms: 8.359132
  ...
# Subtest: Ctrl+Shift+P always opens the Task Card, never the classic property list
ok 2804 - Ctrl+Shift+P always opens the Task Card, never the classic property list
  ---
  duration_ms: 4.945133
  ...
# Subtest: the plugin carries no Task Card pilot setting, date gate, or classic preference
ok 2805 - the plugin carries no Task Card pilot setting, date gate, or classic preference
  ---
  duration_ms: 19.469548
  ...
# Subtest: a leftover persisted taskCard flag is ignored and never rewritten
ok 2806 - a leftover persisted taskCard flag is ignored and never rewritten
  ---
  duration_ms: 6.702509
  ...
# Subtest: palette command is named Task card (set properties)
ok 2807 - palette command is named Task card (set properties)
  ---
  duration_ms: 11.315849
  ...
# Subtest: Task Card opens the compact card with dialog semantics and a close control
ok 2808 - Task Card opens the compact card with dialog semantics and a close control
  ---
  duration_ms: 1.695838
  ...
# Subtest: a More row opens that property's value stage, never a filter list, and Back restores the card
ok 2809 - a More row opens that property's value stage, never a filter list, and Back restores the card
  ---
  duration_ms: 3.320372
  ...
# Subtest: after open the actions list, not the Close button, has focus
ok 2810 - after open the actions list, not the Close button, has focus
  ---
  duration_ms: 4.612018
  ...
# Subtest: clicking card text keeps the card key router active exactly once
ok 2811 - clicking card text keeps the card key router active exactly once
  ---
  duration_ms: 16.148256
  ...
# Subtest: Ready card writes close from a key, P1 click, recommendations, and Alt+N
ok 2812 - Ready card writes close from a key, P1 click, recommendations, and Alt+N
  ---
  duration_ms: 6.719822
  ...
# Subtest: Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
ok 2813 - Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
  ---
  duration_ms: 4.423708
  ...
# Subtest: Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
ok 2814 - Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
  ---
  duration_ms: 4.247602
  ...
# Subtest: Ctrl+R recomputes and repaints the card recommendation
ok 2815 - Ctrl+R recomputes and repaints the card recommendation
  ---
  duration_ms: 1.637036
  ...
# Subtest: Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
ok 2816 - Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
  ---
  duration_ms: 22.412358
  ...
# Subtest: Task Link opens focused while resolving and consumes keys without replay
ok 2817 - Task Link opens focused while resolving and consumes keys without replay
  ---
  duration_ms: 3.151569
  ...
# Subtest: Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card
ok 2818 - Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card
  ---
  duration_ms: 1.556422
  ...
# Subtest: Ctrl+Shift+Alt+B on a Task Link opens the linked Blocks stage
ok 2819 - Ctrl+Shift+Alt+B on a Task Link opens the linked Blocks stage
  ---
  duration_ms: 0.973329
  ...
# Subtest: Task Link count replacement and source edits invalidate old resolutions
ok 2820 - Task Link count replacement and source edits invalidate old resolutions
  ---
  duration_ms: 0.988547
  ...
# Subtest: Task Link resolution failure and plugin unload close their shells
ok 2821 - Task Link resolution failure and plugin unload close their shells
  ---
  duration_ms: 1.367522
  ...
# Subtest: direct Depends on entry opens the dependency stage without painting the card or the list
ok 2822 - direct Depends on entry opens the dependency stage without painting the card or the list
  ---
  duration_ms: 0.815657
  ...
# Subtest: a direct stage for an unconfigured property closes instead of leaving an empty modal
ok 2823 - a direct stage for an unconfigured property closes instead of leaving an empty modal
  ---
  duration_ms: 0.288852
  ...
# Subtest: a refused direct stage closes instead of landing on a card or a list
ok 2824 - a refused direct stage closes instead of landing on a card or a list
  ---
  duration_ms: 0.708473
  ...
# Subtest: Ctrl+Shift+B lands on the Depends on stage with the same intent as card b
ok 2825 - Ctrl+Shift+B lands on the Depends on stage with the same intent as card b
  ---
  duration_ms: 2.391887
  ...
# Subtest: Ctrl+Shift+B Back returns to the card without re-dispatching
ok 2826 - Ctrl+Shift+B Back returns to the card without re-dispatching
  ---
  duration_ms: 1.11554
  ...
# Subtest: Ctrl+Shift+B on a plain bullet notices and closes the card
ok 2827 - Ctrl+Shift+B on a plain bullet notices and closes the card
  ---
  duration_ms: 0.686351
  ...
# Subtest: Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch
ok 2828 - Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch
  ---
  duration_ms: 2.875942
  ...
# Subtest: Ctrl+Shift+Alt+B on Depends-On and BLOCKS lines opens the owner's stage directly
ok 2829 - Ctrl+Shift+Alt+B on Depends-On and BLOCKS lines opens the owner's stage directly
  ---
  duration_ms: 2.038503
  ...
# Subtest: Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not
ok 2830 - Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not
  ---
  duration_ms: 2.229106
  ...
# Subtest: priority gesture writes the frozen date and duplicate dispatch is single-flight
ok 2831 - priority gesture writes the frozen date and duplicate dispatch is single-flight
  ---
  duration_ms: 9.927727
  ...
# Subtest: pending priority action passes its card preview through the Work Log adapter
ok 2832 - pending priority action passes its card preview through the Work Log adapter
  ---
  duration_ms: 1.154615
  ...
# Subtest: Task Link priority action refuses a stale cross-note preflight before writes
ok 2833 - Task Link priority action refuses a stale cross-note preflight before writes
  ---
  duration_ms: 4.403861
  ...
# Subtest: Task Link priority action rolls back earlier note writes after a later write fails
ok 2834 - Task Link priority action rolls back earlier note writes after a later write fails
  ---
  duration_ms: 2.583674
  ...
# Subtest: Task Link transaction reports a cleanup failure without implying global undo
ok 2835 - Task Link transaction reports a cleanup failure without implying global undo
  ---
  duration_ms: 1.375025
  ...
# Subtest: selected-property deletion uses the existing writer; other card rows stay non-deletable
ok 2836 - selected-property deletion uses the existing writer; other card rows stay non-deletable
  ---
  duration_ms: 2.938481
  ...
# Subtest: failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
ok 2837 - failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
  ---
  duration_ms: 1.871785
  ...
# Subtest: a refused deletion rebuilds the card from the refreshed line
ok 2838 - a refused deletion rebuilds the card from the refreshed line
  ---
  duration_ms: 5.812379
  ...
# Subtest: 0 deletes only priority and keeps the scheduled field byte-for-byte
ok 2839 - 0 deletes only priority and keeps the scheduled field byte-for-byte
  ---
  duration_ms: 2.030978
  ...
# Subtest: card keys pressed on a priority radio or the banner reach the resolver exactly once
ok 2840 - card keys pressed on a priority radio or the banner reach the resolver exactly once
  ---
  duration_ms: 2.855944
  ...
# Subtest: held or composing Enter on a radio or the banner never writes
ok 2841 - held or composing Enter on a radio or the banner never writes
  ---
  duration_ms: 1.122273
  ...
# Subtest: Escape, q, Q, and Ctrl+[ close the card without writing
ok 2842 - Escape, q, Q, and Ctrl+[ close the card without writing
  ---
  duration_ms: 2.888506
  ...
# Subtest: Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
ok 2843 - Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
  ---
  duration_ms: 0.757446
  ...
# Subtest: repeated close keys and a second close() are harmless
ok 2844 - repeated close keys and a second close() are harmless
  ---
  duration_ms: 1.080803
  ...
# Subtest: composition never closes the card or a stage
ok 2845 - composition never closes the card or a stage
  ---
  duration_ms: 0.973709
  ...
# Subtest: q typed into a stage's text field never closes the modal
ok 2846 - q typed into a stage's text field never closes the modal
  ---
  duration_ms: 0.716899
  ...
# Subtest: Ctrl+[ closes from a focused date field without writing
ok 2847 - Ctrl+[ closes from a focused date field without writing
  ---
  duration_ms: 0.741246
  ...
# Subtest: Ctrl+[ closes the schedule review from its Reason and Work summary fields
ok 2848 - Ctrl+[ closes the schedule review from its Reason and Work summary fields
  ---
  duration_ms: 5.465947
  ...
# Subtest: Ctrl+[ closes the summary-only schedule-work-log stage without writing
ok 2849 - Ctrl+[ closes the summary-only schedule-work-log stage without writing
  ---
  duration_ms: 1.260447
  ...
# Subtest: Ctrl+[ closes the lane-release Work summary without writing
ok 2850 - Ctrl+[ closes the lane-release Work summary without writing
  ---
  duration_ms: 1.103256
  ...
# Subtest: q closes from a focused More row and from the Close button
ok 2851 - q closes from a focused More row and from the Close button
  ---
  duration_ms: 2.101663
  ...
# Subtest: Ctrl+[ closes from focused card controls, the Back button, and the modal frame
ok 2852 - Ctrl+[ closes from focused card controls, the Back button, and the modal frame
  ---
  duration_ms: 3.174963
  ...
# Subtest: a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
ok 2853 - a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
  ---
  duration_ms: 7.566538
  ...
# Subtest: a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
ok 2854 - a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
  ---
  duration_ms: 3.222503
  ...
# Subtest: a direct dependency stage closes on Ctrl+[ but keeps q as typed text
ok 2855 - a direct dependency stage closes on Ctrl+[ but keeps q as typed text
  ---
  duration_ms: 0.772746
  ...
# Subtest: q and Ctrl+[ are not global closes: other modals and the decay card ignore them
ok 2856 - q and Ctrl+[ are not global closes: other modals and the decay card ignore them
  ---
  duration_ms: 0.893857
  ...
# Subtest: missing freshness API disables Review every with an honest reason
ok 2857 - missing freshness API disables Review every with an honest reason
  ---
  duration_ms: 0.779358
  ...
# Subtest: child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
ok 2858 - child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
  ---
  duration_ms: 0.938001
  ...
# Subtest: decay card keeps its classes and shares key-card tokens
ok 2859 - decay card keeps its classes and shares key-card tokens
  ---
  duration_ms: 0.180855
  ...
# Subtest: decay card footer always names the X drop alias; the trial date is not this gate
ok 2860 - decay card footer always names the X drop alias; the trial date is not this gate
  ---
  duration_ms: 0.302067
  ...
# Subtest: task card level chips reuse the shared priority mark when available
ok 2861 - task card level chips reuse the shared priority mark when available
  ---
  duration_ms: 5.235016
  ...
# Subtest: task card labels are unchanged without the priority mark api
ok 2862 - task card labels are unchanged without the priority mark api
  ---
  duration_ms: 2.878226
  ...
# Subtest: manifest order is authoritative and fragments share one lexical scope
ok 2863 - manifest order is authoritative and fragments share one lexical scope
  ---
  duration_ms: 108.05382
  ...
# Subtest: builds are deterministic and build:check is read-only on success
ok 2864 - builds are deterministic and build:check is read-only on success
  ---
  duration_ms: 161.065553
  ...
# Subtest: read-only check rejects changed fragments and edited generated output
ok 2865 - read-only check rejects changed fragments and edited generated output
  ---
  duration_ms: 156.952668
  ...
# Subtest: check rejects a missing generated bundle without writing it
ok 2866 - check rejects a missing generated bundle without writing it
  ---
  duration_ms: 50.23439
  ...
# Subtest: fragment line limit is enforced before writing output
ok 2867 - fragment line limit is enforced before writing output
  ---
  duration_ms: 1.505735
  ...
# Subtest: fragment syntax errors are rejected before writing output
ok 2868 - fragment syntax errors are rejected before writing output
  ---
  duration_ms: 27.256589
  ...
# Subtest: malformed, empty, duplicate, and traversal manifests are rejected read-only
    # Subtest: invalid JSON
    ok 1 - invalid JSON
      ---
      duration_ms: 1.264464
      ...
    # Subtest: empty manifest
    ok 2 - empty manifest
      ---
      duration_ms: 1.149145
      ...
    # Subtest: non-array manifest
    ok 3 - non-array manifest
      ---
      duration_ms: 1.176316
      ...
    # Subtest: duplicate entries
    ok 4 - duplicate entries
      ---
      duration_ms: 32.323123
      ...
    # Subtest: traversal entry
    ok 5 - traversal entry
      ---
      duration_ms: 0.921349
      ...
    # Subtest: absolute entry
    ok 6 - absolute entry
      ---
      duration_ms: 0.826489
      ...
    1..6
ok 2869 - malformed, empty, duplicate, and traversal manifests are rejected read-only
  ---
  duration_ms: 39.250411
  ...
# Subtest: missing and omitted fragments are rejected read-only
    # Subtest: missing manifest entry
    ok 1 - missing manifest entry
      ---
      duration_ms: 1.000621
      ...
    # Subtest: unlisted JavaScript source
    ok 2 - unlisted JavaScript source
      ---
      duration_ms: 27.654049
      ...
    1..2
ok 2870 - missing and omitted fragments are rejected read-only
  ---
  duration_ms: 29.023494
  ...
# Subtest: escaping fragment symlinks are rejected read-only
ok 2871 - escaping fragment symlinks are rejected read-only
  ---
  duration_ms: 1.438076
  ...
# Subtest: parity comparator identifies changed helper and plugin methods
ok 2872 - parity comparator identifies changed helper and plugin methods
  ---
  duration_ms: 14.790704
  ...
# Subtest: parity comparator accepts a mixin-split helper class but not a changed method or superclass
ok 2873 - parity comparator accepts a mixin-split helper class but not a changed method or superclass
  ---
  duration_ms: 0.82714
  ...
# Subtest: snapshot commands are available only for active Markdown files
ok 2874 - snapshot commands are available only for active Markdown files
  ---
  duration_ms: 1.615916
  ...
# Subtest: commands run bob ref create on the active path, with -C for closed tasks
ok 2875 - commands run bob ref create on the active path, with -C for closed tasks
  ---
  duration_ms: 4.658376
  ...
# Subtest: bob spawn uses the resolved path, vault environment, timeout, and NO_COLOR
ok 2876 - bob spawn uses the resolved path, vault environment, timeout, and NO_COLOR
  ---
  duration_ms: 1.239527
  ...
# Subtest: failure notices retain bob error and hint lines verbatim
ok 2877 - failure notices retain bob error and hint lines verbatim
  ---
  duration_ms: 0.542476
  ...
# Subtest: off desktop, bob spawning is refused with the desktop-app explanation
ok 2878 - off desktop, bob spawning is refused with the desktop-app explanation
  ---
  duration_ms: 0.488924
  ...
# Subtest: both prompt copies pass the shared fixture table identically
ok 2879 - both prompt copies pass the shared fixture table identically
  ---
  duration_ms: 9.840892
  ...
# Subtest: suggestion is valid, compact, and collision-aware
ok 2880 - suggestion is valid, compact, and collision-aware
  ---
  duration_ms: 0.858349
  ...
# Subtest: rename excludes exactly one old-ID occurrence
ok 2881 - rename excludes exactly one old-ID occurrence
  ---
  duration_ms: 0.246922
  ...
# Subtest: dependency legacy [id::] reuses only valid free IDs
ok 2882 - dependency legacy [id::] reuses only valid free IDs
  ---
  duration_ms: 0.436534
  ...
# Subtest: project conversion keeps the existing suggestBlockIdFromTask
ok 2883 - project conversion keeps the existing suggestBlockIdFromTask
  ---
  duration_ms: 0.833772
  ...
# Subtest: successor SB vectors are unchanged
ok 2884 - successor SB vectors are unchanged
  ---
  duration_ms: 1.028955
  ...
# Subtest: option-bracket ring reads Blocked as a source-only slot ahead of Ready
ok 2885 - option-bracket ring reads Blocked as a source-only slot ahead of Ready
  ---
  duration_ms: 1.323397
  ...
# Subtest: isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
ok 2886 - isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
  ---
  duration_ms: 0.319511
  ...
# Subtest: option-bracket refuses to change a member while its project is Blocked
ok 2887 - option-bracket refuses to change a member while its project is Blocked
  ---
  duration_ms: 2.348555
  ...
# Subtest: tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
ok 2888 - tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
  ---
  duration_ms: 1.233446
  ...
# Subtest: project resident notice reads the inline ^prj date and ignores frontmatter scheduled
ok 2889 - project resident notice reads the inline ^prj date and ignores frontmatter scheduled
  ---
  duration_ms: 0.463004
  ...
# Subtest: findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
ok 2890 - findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
  ---
  duration_ms: 0.27803
  ...
# Subtest: field removal collapses only the exposed span and preserves the rest of the line
ok 2891 - field removal collapses only the exposed span and preserves the rest of the line
  ---
  duration_ms: 0.238024
  ...
# Subtest: vault-path retirement preserves CRLF and a missing final newline
ok 2892 - vault-path retirement preserves CRLF and a missing final newline
  ---
  duration_ms: 0.854963
  ...
# Subtest: Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
ok 2893 - Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
  ---
  duration_ms: 0.568386
  ...
# Subtest: Schedule Log discovery ignores a marker owned by a nested grandchild
ok 2894 - Schedule Log discovery ignores a marker owned by a nested grandchild
  ---
  duration_ms: 0.394563
  ...
# Subtest: Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
ok 2895 - Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
  ---
  duration_ms: 0.451983
  ...
# Subtest: a task with no Schedule Log gets its field retired without any insertion or new marker
ok 2896 - a task with no Schedule Log gets its field retired without any insertion or new marker
  ---
  duration_ms: 0.133314
  ...
# Subtest: Schedule Log entry uses the canonical arrow, dash, and lock bytes
ok 2897 - Schedule Log entry uses the canonical arrow, dash, and lock bytes
  ---
  duration_ms: 0.095282
  ...
# Subtest: retirement stays a no-op for shapes that are not proof of a blocking date
ok 2898 - retirement stays a no-op for shapes that are not proof of a blocking date
  ---
  duration_ms: 0.164755
  ...
# Subtest: cycling Blocked backward to Cancelled retires the date and logs, matching forward
ok 2899 - cycling Blocked backward to Cancelled retires the date and logs, matching forward
  ---
  duration_ms: 3.921819
  ...
# Subtest: single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
ok 2900 - single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
  ---
  duration_ms: 0.999879
  ...
# Subtest: counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
ok 2901 - counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
  ---
  duration_ms: 1.436323
  ...
# Subtest: counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
ok 2902 - counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
  ---
  duration_ms: 0.752827
  ...
# Subtest: transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
ok 2903 - transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
  ---
  duration_ms: 1.788946
  ...
# Subtest: pressing again after Blocked retirement performs an ordinary transition with no further changes
ok 2904 - pressing again after Blocked retirement performs an ordinary transition with no further changes
  ---
  duration_ms: 0.215071
  ...
# Subtest: Alt+] on a date-blocked ^prj recovers open residents in step
ok 2905 - Alt+] on a date-blocked ^prj recovers open residents in step
  ---
  duration_ms: 14.100406
  ...
# Subtest: Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
ok 2906 - Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
  ---
  duration_ms: 1.060345
  ...
# Subtest: planProjectResidentRecoveryEdits recovers when a cross-note id is not open
ok 2907 - planProjectResidentRecoveryEdits recovers when a cross-note id is not open
  ---
  duration_ms: 0.347925
  ...
# Subtest: Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
ok 2908 - Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
  ---
  duration_ms: 1.456171
  ...
# Subtest: Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
ok 2909 - Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
  ---
  duration_ms: 0.907402
  ...
# Subtest: Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
ok 2910 - Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
  ---
  duration_ms: 2.049123
  ...
# Subtest: cycling a transcluded ^prj recovers residents in the source note
ok 2911 - cycling a transcluded ^prj recovers residents in the source note
  ---
  duration_ms: 1.282509
  ...
# Subtest: cycler BK1–BK12 accept and empty
ok 2912 - cycler BK1–BK12 accept and empty
  ---
  duration_ms: 1.10493
  ...
# Subtest: cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded
ok 2913 - cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded
  ---
  duration_ms: 0.571
  ...
# Subtest: cycler MC4 strike/restore skip BLOCKS lines
ok 2914 - cycler MC4 strike/restore skip BLOCKS lines
  ---
  duration_ms: 0.945666
  ...
# Subtest: cycler MC3 tree close skips BLOCKS embeds
ok 2915 - cycler MC3 tree close skips BLOCKS embeds
  ---
  duration_ms: 0.73311
  ...
# Subtest: cycler MC1/MC2 Pomodoro and successor scanners skip managed lines
ok 2916 - cycler MC1/MC2 Pomodoro and successor scanners skip managed lines
  ---
  duration_ms: 1.033884
  ...
# Subtest: cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS
ok 2917 - cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS
  ---
  duration_ms: 0.210442
  ...
# Subtest: range planner preserves every single-item mode without an effective count
ok 2918 - range planner preserves every single-item mode without an effective count
  ---
  duration_ms: 7.369182
  ...
# Subtest: item counts carry children, skip blank lines and loose continuations, and clamp
ok 2919 - item counts carry children, skip blank lines and loose continuations, and clamp
  ---
  duration_ms: 0.326123
  ...
# Subtest: range stops at headings, shallower lines, same-level paragraphs and fences
ok 2920 - range stops at headings, shallower lines, same-level paragraphs and fences
  ---
  duration_ms: 0.180795
  ...
# Subtest: siblings require the exact whitespace and blockquote prefix
ok 2921 - siblings require the exact whitespace and blockquote prefix
  ---
  duration_ms: 0.199441
  ...
# Subtest: counted demotion moves four complete blocks to one existing section
ok 2922 - counted demotion moves four complete blocks to one existing section
  ---
  duration_ms: 5.469535
  ...
# Subtest: counted demotion creates a typed section or one default Requirements section
ok 2923 - counted demotion creates a typed section or one default Requirements section
  ---
  duration_ms: 2.766362
  ...
# Subtest: bottom-up removal splices blank seams and maps destinations before the source
ok 2924 - bottom-up removal splices blank seams and maps destinations before the source
  ---
  duration_ms: 0.505185
  ...
# Subtest: counted promotion Enter appends tasks in order and removes an emptied source section
ok 2925 - counted promotion Enter appends tasks in order and removes an emptied source section
  ---
  duration_ms: 1.437385
  ...
# Subtest: counted promotion to existing or new non-Tasks destinations keeps all bullets plain
ok 2926 - counted promotion to existing or new non-Tasks destinations keeps all bullets plain
  ---
  duration_ms: 0.643158
  ...
# Subtest: same-source Tasks promotion rewrites all selected lines in place
ok 2927 - same-source Tasks promotion rewrites all selected lines in place
  ---
  duration_ms: 1.171126
  ...
# Subtest: counted demotion outside Tasks moves to the next section in one write
ok 2928 - counted demotion outside Tasks moves to the next section in one write
  ---
  duration_ms: 0.451562
  ...
# Subtest: in-place ranges write once without centering for nested, non-dash, and unrouted items
ok 2929 - in-place ranges write once without centering for nested, non-dash, and unrouted items
  ---
  duration_ms: 1.016811
  ...
# Subtest: mixed demotion ranges count unchanged siblings and only move top-level dash tasks
ok 2930 - mixed demotion ranges count unchanged siblings and only move top-level dash tasks
  ---
  duration_ms: 0.500566
  ...
# Subtest: mixed promotion preserves existing tasks and a nonempty source section
ok 2931 - mixed promotion preserves existing tasks and a nonempty source section
  ---
  duration_ms: 0.277349
  ...
# Subtest: Vim action consumes explicit additional-item counts and preserves bare behavior
ok 2932 - Vim action consumes explicit additional-item counts and preserves bare behavior
  ---
  duration_ms: 4.427585
  ...
# Subtest: command checking preserves pending count; execution consumes it once and resets Vim
ok 2933 - command checking preserves pending count; execution consumes it once and resets Vim
  ---
  duration_ms: 1.747086
  ...
# Subtest: command route stays single without normal-mode explicit count and supports in-place ranges
ok 2934 - command route stays single without normal-mode explicit count and supports in-place ranges
  ---
  duration_ms: 0.595498
  ...
# Subtest: picker displays at most five preview rows plus overflow; single picker is unchanged
ok 2935 - picker displays at most five preview rows plus overflow; single picker is unchanged
  ---
  duration_ms: 2.045155
  ...
# Subtest: stale counted picker and cancelled picker never write
ok 2936 - stale counted picker and cancelled picker never write
  ---
  duration_ms: 1.132633
  ...
# Subtest: counted moves round-trip CRLF and preserve the presence or absence of a final newline
ok 2937 - counted moves round-trip CRLF and preserve the presence or absence of a final newline
  ---
  duration_ms: 4.10027
  ...
# Subtest: direct open/done transitions include incomplete statuses without broadening excluded statuses
ok 2938 - direct open/done transitions include incomplete statuses without broadening excluded statuses
  ---
  duration_ms: 1.257621
  ...
# Subtest: Ctrl+Enter block-link selection recognizes live and retired forms
ok 2939 - Ctrl+Enter block-link selection recognizes live and retired forms
  ---
  duration_ms: 2.009697
  ...
# Subtest: Pomodoro child ownership is status-neutral and bounded by contiguous list structure
ok 2940 - Pomodoro child ownership is status-neutral and bounded by contiguous list structure
  ---
  duration_ms: 0.796761
  ...
# Subtest: daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
ok 2941 - daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
  ---
  duration_ms: 0.325883
  ...
# Subtest: parsePomodoroEntryLineParts reads placeholder and range names conservatively
ok 2942 - parsePomodoroEntryLineParts reads placeholder and range names conservatively
  ---
  duration_ms: 0.838641
  ...
# Subtest: formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
ok 2943 - formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
  ---
  duration_ms: 0.154224
  ...
# Subtest: Pomodoro bullet toggle accepts empty indented list items
ok 2944 - Pomodoro bullet toggle accepts empty indented list items
  ---
  duration_ms: 0.299933
  ...
# Subtest: Pomodoro bullet toggle rejects non-empty or out-of-section bullets
ok 2945 - Pomodoro bullet toggle rejects non-empty or out-of-section bullets
  ---
  duration_ms: 0.265217
  ...
# Subtest: Pomodoro bullet toggle reverses only empty open childless placeholders
ok 2946 - Pomodoro bullet toggle reverses only empty open childless placeholders
  ---
  duration_ms: 0.62291
  ...
# Subtest: Pomodoro bullet toggle reverses named empty open childless placeholders
ok 2947 - Pomodoro bullet toggle reverses named empty open childless placeholders
  ---
  duration_ms: 0.483803
  ...
# Subtest: Pomodoro bullet toggle round trips and normalizes child indentation
ok 2948 - Pomodoro bullet toggle round trips and normalizes child indentation
  ---
  duration_ms: 0.276639
  ...
# Subtest: Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
ok 2949 - Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
  ---
  duration_ms: 0.194241
  ...
# Subtest: Pomodoro toggle key gate does not shadow bare Option bracket cycling
ok 2950 - Pomodoro toggle key gate does not shadow bare Option bracket cycling
  ---
  duration_ms: 0.221563
  ...
# Subtest: Pomodoro toggle command is daily-only and places the cursor for both directions
ok 2951 - Pomodoro toggle command is daily-only and places the cursor for both directions
  ---
  duration_ms: 0.657506
  ...
# Subtest: Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
ok 2952 - Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
  ---
  duration_ms: 0.435652
  ...
# Subtest: Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
ok 2953 - Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
  ---
  duration_ms: 2.459256
  ...
# Subtest: Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
ok 2954 - Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
  ---
  duration_ms: 26.408389
  ...
# Subtest: Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
ok 2955 - Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
  ---
  duration_ms: 1.945475
  ...
# Subtest: Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
ok 2956 - Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
  ---
  duration_ms: 2.18392
  ...
# Subtest: Ctrl+Enter closing the local line over an already-closed target does not write it a second time
ok 2957 - Ctrl+Enter closing the local line over an already-closed target does not write it a second time
  ---
  duration_ms: 0.758359
  ...
# Subtest: Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
ok 2958 - Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
  ---
  duration_ms: 0.688354
  ...
# Subtest: Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
ok 2959 - Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
  ---
  duration_ms: 1.734352
  ...
# Subtest: Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
ok 2960 - Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
  ---
  duration_ms: 0.55015
  ...
# Subtest: Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
ok 2961 - Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
  ---
  duration_ms: 0.579837
  ...
# Subtest: Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
ok 2962 - Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
  ---
  duration_ms: 0.67028
  ...
# Subtest: Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
ok 2963 - Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
  ---
  duration_ms: 0.620275
  ...
# Subtest: getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
ok 2964 - getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
  ---
  duration_ms: 0.310302
  ...
# Subtest: Ctrl+Enter close continues the walk with complete after finalize ran
ok 2965 - Ctrl+Enter close continues the walk with complete after finalize ran
  ---
  duration_ms: 11.869716
  ...
# Subtest: Ctrl+Enter close continues only after transclusion propagation landed
ok 2966 - Ctrl+Enter close continues only after transclusion propagation landed
  ---
  duration_ms: 12.88268
  ...
# Subtest: Ctrl+Enter reopen settles the walk with null
ok 2967 - Ctrl+Enter reopen settles the walk with null
  ---
  duration_ms: 11.252982
  ...
# Subtest: Ctrl+Enter swallows the key with no write while the walk is busy
ok 2968 - Ctrl+Enter swallows the key with no write while the walk is busy
  ---
  duration_ms: 10.917869
  ...
# Subtest: Ctrl+Enter with a null capture behaves exactly like today
ok 2969 - Ctrl+Enter with a null capture behaves exactly like today
  ---
  duration_ms: 11.441599
  ...
# Subtest: Ctrl+Enter with nav v2 or no nav keeps today's behavior
ok 2970 - Ctrl+Enter with nav v2 or no nav keeps today's behavior
  ---
  duration_ms: 22.105342
  ...
# Subtest: Ctrl+Enter lets the checklist claim win before capturing
ok 2971 - Ctrl+Enter lets the checklist claim win before capturing
  ---
  duration_ms: 0.765311
  ...
# Subtest: Ctrl+Enter settles the walk with null when the toggle rejects
ok 2972 - Ctrl+Enter settles the walk with null when the toggle rejects
  ---
  duration_ms: 11.941333
  ...
# Subtest: Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
ok 2973 - Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
  ---
  duration_ms: 1.601217
  ...
# Subtest: eligible Tasks demotions prompt in project and non-project notes
ok 2974 - eligible Tasks demotions prompt in project and non-project notes
  ---
  duration_ms: 2.96419
  ...
# Subtest: selectable headings skip YAML, fences, empty titles, and Tasks
ok 2975 - selectable headings skip YAML, fences, empty titles, and Tasks
  ---
  duration_ms: 0.950716
  ...
# Subtest: duplicate heading identities stay distinct and route to the chosen occurrence
ok 2976 - duplicate heading identities stay distinct and route to the chosen occurrence
  ---
  duration_ms: 1.086134
  ...
# Subtest: demotion picker defaults and typed names resolve without synthetic duplicates
ok 2977 - demotion picker defaults and typed names resolve without synthetic duplicates
  ---
  duration_ms: 2.01059
  ...
# Subtest: picker keyboard state wraps, clamps, and refuses invalid Enter
ok 2978 - picker keyboard state wraps, clamps, and refuses invalid Enter
  ---
  duration_ms: 0.374325
  ...
# Subtest: new-section formatting keeps extra blanks, final newlines, and nested children
ok 2979 - new-section formatting keeps extra blanks, final newlines, and nested children
  ---
  duration_ms: 0.884649
  ...
# Subtest: existing-section insertion works before and after the source on CRLF-backed editors
ok 2980 - existing-section insertion works before and after the source on CRLF-backed editors
  ---
  duration_ms: 3.379804
  ...
# Subtest: command opens one picker, writes only on accept, and restores cursor plus center
ok 2981 - command opens one picker, writes only on accept, and restores cursor plus center
  ---
  duration_ms: 0.860012
  ...
# Subtest: pointer activation, Escape, and double-submit protection leave a consistent note
ok 2982 - pointer activation, Escape, and double-submit protection leave a consistent note
  ---
  duration_ms: 2.072187
  ...
# Subtest: stale document, changed editor, or missing heading notice without writing
ok 2983 - stale document, changed editor, or missing heading notice without writing
  ---
  duration_ms: 2.15215
  ...
# Subtest: dependency normalizer writes path-qualified IDs and is idempotent
ok 2984 - dependency normalizer writes path-qualified IDs and is idempotent
  ---
  duration_ms: 2.081875
  ...
# Subtest: Tasks-generated IDs become local block IDs when none exists
ok 2985 - Tasks-generated IDs become local block IDs when none exists
  ---
  duration_ms: 0.763629
  ...
# Subtest: note rename rewrites target IDs and yields exact propagation mappings
ok 2986 - note rename rewrites target IDs and yields exact propagation mappings
  ---
  duration_ms: 0.288201
  ...
# Subtest: note rename also rewrites same-file dependsOn references
ok 2987 - note rename also rewrites same-file dependsOn references
  ---
  duration_ms: 0.228406
  ...
# Subtest: dependency normalization skips unsupported paths and fenced examples
ok 2988 - dependency normalization skips unsupported paths and fenced examples
  ---
  duration_ms: 0.339388
  ...
# Subtest: blocked-dependent planner matches the CLI dependency truth table
ok 2989 - blocked-dependent planner matches the CLI dependency truth table
  ---
  duration_ms: 3.067016
  ...
# Subtest: blocked-dependent edits preserve EOLs and skip stale lines idempotently
ok 2990 - blocked-dependent edits preserve EOLs and skip stale lines idempotently
  ---
  duration_ms: 0.986013
  ...
# Subtest: project recovery strips resident tags and works without freshness v12
ok 2991 - project recovery strips resident tags and works without freshness v12
  ---
  duration_ms: 1.620694
  ...
# Subtest: recovery passes daily-note and Today skip flags to ledger freshness
ok 2992 - recovery passes daily-note and Today skip flags to ledger freshness
  ---
  duration_ms: 0.431334
  ...
# Subtest: normalization mappings propagate to every dependent file
ok 2993 - normalization mappings propagate to every dependent file
  ---
  duration_ms: 1.132202
  ...
# Subtest: runtime normalizer skips unsupported paths with one informative notice
ok 2994 - runtime normalizer skips unsupported paths with one informative notice
  ---
  duration_ms: 0.697241
  ...
# Subtest: rename reconciliation rewrites the target and every dependent
ok 2995 - rename reconciliation rewrites the target and every dependent
  ---
  duration_ms: 0.56544
  ...
# Subtest: editor dependency normalization abandons and reschedules stale snapshots
ok 2996 - editor dependency normalization abandons and reschedules stale snapshots
  ---
  duration_ms: 0.560189
  ...
# Subtest: rename reconciliation abandons and reschedules stale editor snapshots
ok 2997 - rename reconciliation abandons and reschedules stale editor snapshots
  ---
  duration_ms: 0.268853
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 2998 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 1.079261
  ...
# Subtest: close-time retirement skips Depends-On lines
ok 2999 - close-time retirement skips Depends-On lines
  ---
  duration_ms: 1.504263
  ...
# Subtest: reopen restoration skips Depends-On lines instead of re-embedding them
ok 3000 - reopen restoration skips Depends-On lines instead of re-embedding them
  ---
  duration_ms: 0.609023
  ...
# Subtest: embedded-tree close collection ignores Depends-On lines
ok 3001 - embedded-tree close collection ignores Depends-On lines
  ---
  duration_ms: 0.3038
  ...
# Subtest: Alt-bracket bullet formatting never applies to Depends-On lines
ok 3002 - Alt-bracket bullet formatting never applies to Depends-On lines
  ---
  duration_ms: 0.511757
  ...
# Subtest: Ctrl+Enter on a dependency link closes only the target and runs the recovery
ok 3003 - Ctrl+Enter on a dependency link closes only the target and runs the recovery
  ---
  duration_ms: 1.577172
  ...
# Subtest: Ctrl+Enter on a dependency link reopens only the target, root-only
ok 3004 - Ctrl+Enter on a dependency link reopens only the target, root-only
  ---
  duration_ms: 1.121522
  ...
# Subtest: single and counted Alt-bracket cycle the dependency target under the cursor
ok 3005 - single and counted Alt-bracket cycle the dependency target under the cursor
  ---
  duration_ms: 17.837562
  ...
# Subtest: single and counted Alt-bracket report when the cursor is off every dependency link
ok 3006 - single and counted Alt-bracket report when the cursor is off every dependency link
  ---
  duration_ms: 0.555971
  ...
# Subtest: Ctrl+Enter candidate resolution finds plain links on Depends-On lines
ok 3007 - Ctrl+Enter candidate resolution finds plain links on Depends-On lines
  ---
  duration_ms: 0.190033
  ...
# Subtest: dependency-id normalisation never edits Depends-On lines
ok 3008 - dependency-id normalisation never edits Depends-On lines
  ---
  duration_ms: 0.262571
  ...
# Subtest: note rename rewrites fields while leaving Depends-On lines alone
ok 3009 - note rename rewrites fields while leaving Depends-On lines alone
  ---
  duration_ms: 0.154776
  ...
# Subtest: recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
ok 3010 - recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
  ---
  duration_ms: 1.781031
  ...
# Subtest: cycler freshness: local-fallback rewrite stamps last via injected stamper
ok 3011 - cycler freshness: local-fallback rewrite stamps last via injected stamper
  ---
  duration_ms: 1.754931
  ...
# Subtest: cycler freshness: rewrites without a stamper are unchanged (identity default)
ok 3012 - cycler freshness: rewrites without a stamper are unchanged (identity default)
  ---
  duration_ms: 0.467052
  ...
# Subtest: cycler freshness: a throwing stamper leaves the rewritten line intact
ok 3013 - cycler freshness: a throwing stamper leaves the rewritten line intact
  ---
  duration_ms: 0.202346
  ...
# Subtest: cycler freshness: transcluded rewrite stamps last via injected stamper
ok 3014 - cycler freshness: transcluded rewrite stamps last via injected stamper
  ---
  duration_ms: 0.238325
  ...
# Subtest: cycler freshness: cycling a plain line stamps through the follow-up edit
ok 3015 - cycler freshness: cycling a plain line stamps through the follow-up edit
  ---
  duration_ms: 1.029607
  ...
# Subtest: cycler freshness: Tasks-command rewrite with the expected status is stamped
ok 3016 - cycler freshness: Tasks-command rewrite with the expected status is stamped
  ---
  duration_ms: 0.412127
  ...
# Subtest: cycler freshness: Tasks command that inserts a line never stamps
ok 3017 - cycler freshness: Tasks command that inserts a line never stamps
  ---
  duration_ms: 0.393982
  ...
# Subtest: cycler freshness: Tasks command that deletes the line never stamps the next task
ok 3018 - cycler freshness: Tasks command that deletes the line never stamps the next task
  ---
  duration_ms: 0.242323
  ...
# Subtest: cycler freshness: Tasks command that leaves a different status never stamps
ok 3019 - cycler freshness: Tasks command that leaves a different status never stamps
  ---
  duration_ms: 0.421896
  ...
# Subtest: cycler freshness: cycling without ledger-tools writes no stamp
ok 3020 - cycler freshness: cycling without ledger-tools writes no stamp
  ---
  duration_ms: 0.465038
  ...
# Subtest: cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
ok 3021 - cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
  ---
  duration_ms: 0.190954
  ...
# Subtest: Pomodoro marker helpers normalize every block link and preserve fences and EOLs
ok 3022 - Pomodoro marker helpers normalize every block link and preserve fences and EOLs
  ---
  duration_ms: 2.552324
  ...
# Subtest: completed Pomodoro markers are normalized per occurrence
ok 3023 - completed Pomodoro markers are normalized per occurrence
  ---
  duration_ms: 0.456592
  ...
# Subtest: move-only Pomodoro links require a strict immediate hash directive
ok 3024 - move-only Pomodoro links require a strict immediate hash directive
  ---
  duration_ms: 2.294482
  ...
# Subtest: Pomodoro move-only planner toggles links across additional physical lines
ok 3025 - Pomodoro move-only planner toggles links across additional physical lines
  ---
  duration_ms: 1.04701
  ...
# Subtest: Pomodoro move-only planner round trips exact text and rejects strict non-matches
ok 3026 - Pomodoro move-only planner round trips exact text and rejects strict non-matches
  ---
  duration_ms: 0.500325
  ...
# Subtest: bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
ok 3027 - bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
  ---
  duration_ms: 1.45076
  ...
# Subtest: Pomodoro move-only runtime removes locally and validates additions independently
ok 3028 - Pomodoro move-only runtime removes locally and validates additions independently
  ---
  duration_ms: 1.169113
  ...
# Subtest: Pomodoro move-only runtime protects live lines after asynchronous failures
ok 3029 - Pomodoro move-only runtime protects live lines after asynchronous failures
  ---
  duration_ms: 0.391076
  ...
# Subtest: Pomodoro hash Vim mapping distinguishes bare and explicit repeats
ok 3030 - Pomodoro hash Vim mapping distinguishes bare and explicit repeats
  ---
  duration_ms: 9.065962
  ...
# Subtest: Pomodoro completion marks originals and carries clean live copies
ok 3031 - Pomodoro completion marks originals and carries clean live copies
  ---
  duration_ms: 1.71218
  ...
# Subtest: Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
ok 3032 - Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
  ---
  duration_ms: 0.880451
  ...
# Subtest: Pomodoro completion carries the closed Pomodoro name onto created entries
ok 3033 - Pomodoro completion carries the closed Pomodoro name onto created entries
  ---
  duration_ms: 0.419301
  ...
# Subtest: buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
ok 3034 - buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
  ---
  duration_ms: 0.484285
  ...
# Subtest: buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
ok 3035 - buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
  ---
  duration_ms: 0.311625
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is marked
ok 3036 - buildPomodoroCompletionPlan keeps source order when every carried link is marked
  ---
  duration_ms: 0.217215
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
ok 3037 - buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
  ---
  duration_ms: 0.306284
  ...
# Subtest: Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
ok 3038 - Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
  ---
  duration_ms: 4.936347
  ...
# Subtest: deferred-only close deletes the emptied entry and carries stripped links
ok 3039 - deferred-only close deletes the emptied entry and carries stripped links
  ---
  duration_ms: 0.489755
  ...
# Subtest: deferred-only close at EOF leaves no dangling newline
ok 3040 - deferred-only close at EOF leaves no dangling newline
  ---
  duration_ms: 0.207667
  ...
# Subtest: a close with a remaining copyable link keeps the [x] entry
ok 3041 - a close with a remaining copyable link keeps the [x] entry
  ---
  duration_ms: 0.242092
  ...
# Subtest: a prose sibling keeps the closed entry on a deferred close
ok 3042 - a prose sibling keeps the closed entry on a deferred close
  ---
  duration_ms: 0.286147
  ...
# Subtest: Ctrl+Enter deferred-only close deletes the entry in one gesture
ok 3043 - Ctrl+Enter deferred-only close deletes the entry in one gesture
  ---
  duration_ms: 3.837179
  ...
# Subtest: deferred-only close keeps a separated prose child and deletes fence-only leftovers whole
ok 3044 - deferred-only close keeps a separated prose child and deletes fence-only leftovers whole
  ---
  duration_ms: 1.04735
  ...
# Subtest: deferred-only successor relocation uses the inserted placeholder
ok 3045 - deferred-only successor relocation uses the inserted placeholder
  ---
  duration_ms: 0.302328
  ...
# Subtest: selected Done Pomodoro transclusion reopens only its cross-file root
ok 3046 - selected Done Pomodoro transclusion reopens only its cross-file root
  ---
  duration_ms: 6.855771
  ...
# Subtest: selected same-file Done target reopens root-only in the live editor
ok 3047 - selected same-file Done target reopens root-only in the live editor
  ---
  duration_ms: 1.775731
  ...
# Subtest: selected retired link reopens its root and restores the historical occurrence
ok 3048 - selected retired link reopens its root and restores the historical occurrence
  ---
  duration_ms: 1.547245
  ...
# Subtest: incomplete selected Pomodoro transclusion still closes recursively
ok 3049 - incomplete selected Pomodoro transclusion still closes recursively
  ---
  duration_ms: 2.455821
  ...
# Subtest: Done Pomodoro reopens direct roots and clears only its block-link markers
ok 3050 - Done Pomodoro reopens direct roots and clears only its block-link markers
  ---
  duration_ms: 4.075234
  ...
# Subtest: Done Pomodoro reopen restores its own block reference after reopening direct roots
ok 3051 - Done Pomodoro reopen restores its own block reference after reopening direct roots
  ---
  duration_ms: 1.286457
  ...
# Subtest: Done Pomodoro markers remain when the Todo transition does not occur
ok 3052 - Done Pomodoro markers remain when the Todo transition does not occur
  ---
  duration_ms: 0.427256
  ...
# Subtest: registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
ok 3053 - registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
  ---
  duration_ms: 12.829249
  ...
# Subtest: registered Ctrl+Enter immediately recovers a same-file dependent
ok 3054 - registered Ctrl+Enter immediately recovers a same-file dependent
  ---
  duration_ms: 9.743185
  ...
# Subtest: registered Ctrl+Enter immediately recovers a cross-file dependent
ok 3055 - registered Ctrl+Enter immediately recovers a cross-file dependent
  ---
  duration_ms: 2.719593
  ...
# Subtest: child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
ok 3056 - child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
  ---
  duration_ms: 3.682893
  ...
# Subtest: Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
ok 3057 - Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
  ---
  duration_ms: 1.378994
  ...
# Subtest: selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
ok 3058 - selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
  ---
  duration_ms: 2.519561
  ...
# Subtest: selected unresolved or excluded embedded children are consumed as no-ops
ok 3059 - selected unresolved or excluded embedded children are consumed as no-ops
  ---
  duration_ms: 1.379555
  ...
# Subtest: Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
ok 3060 - Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
  ---
  duration_ms: 3.08453
  ...
# Subtest: Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
ok 3061 - Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
  ---
  duration_ms: 2.385676
  ...
# Subtest: Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
ok 3062 - Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
  ---
  duration_ms: 0.868027
  ...
# Subtest: Pomodoro Work Log note-group collection scopes to direct children and requires descendants
ok 3063 - Pomodoro Work Log note-group collection scopes to direct children and requires descendants
  ---
  duration_ms: 0.800419
  ...
# Subtest: Work Log entry body formats as *date* — summary
ok 3064 - Work Log entry body formats as *date* — summary
  ---
  duration_ms: 0.140549
  ...
# Subtest: buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
ok 3065 - buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
  ---
  duration_ms: 0.222255
  ...
# Subtest: planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
ok 3066 - planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
  ---
  duration_ms: 0.341723
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
ok 3067 - planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
  ---
  duration_ms: 0.297007
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
ok 3068 - planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
  ---
  duration_ms: 0.185774
  ...
# Subtest: planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
ok 3069 - planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
  ---
  duration_ms: 0.361179
  ...
# Subtest: planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
ok 3070 - planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
  ---
  duration_ms: 0.378913
  ...
# Subtest: full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
ok 3071 - full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
  ---
  duration_ms: 6.306614
  ...
# Subtest: full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
ok 3072 - full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
  ---
  duration_ms: 1.448276
  ...
# Subtest: full Pomodoro completion keeps two same-task Work Log note sets in source order
ok 3073 - full Pomodoro completion keeps two same-task Work Log note sets in source order
  ---
  duration_ms: 1.113326
  ...
# Subtest: full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
ok 3074 - full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
  ---
  duration_ms: 0.814806
  ...
# Subtest: full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
ok 3075 - full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
  ---
  duration_ms: 0.833822
  ...
# Subtest: full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
ok 3076 - full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
  ---
  duration_ms: 0.542877
  ...
# Subtest: PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
ok 3077 - PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
  ---
  duration_ms: 1.442484
  ...
# Subtest: PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
ok 3078 - PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
  ---
  duration_ms: 0.948191
  ...
# Subtest: PP1 links the emptied project's ^prj as Next and strips \#hide
ok 3079 - PP1 links the emptied project's ^prj as Next and strips \#hide
  ---
  duration_ms: 8.953299
  ...
# Subtest: PP29 closing a child ^prj pulls in its empty parent project
ok 3080 - PP29 closing a child ^prj pulls in its empty parent project
  ---
  duration_ms: 2.055296
  ...
# Subtest: PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
ok 3081 - PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
  ---
  duration_ms: 1.232864
  ...
# Subtest: PP30 keeps the parent untouched while another child or task remains
ok 3082 - PP30 keeps the parent untouched while another child or task remains
  ---
  duration_ms: 0.919196
  ...
# Subtest: PP31 skips missing, ambiguous, and non-project parents
ok 3083 - PP31 skips missing, ambiguous, and non-project parents
  ---
  duration_ms: 1.155005
  ...
# Subtest: PP33 cancellation surfaces the parent without linking it
ok 3084 - PP33 cancellation surfaces the parent without linking it
  ---
  duration_ms: 2.426574
  ...
# Subtest: PP2 and PP3 leave a project with remaining work alone
ok 3085 - PP2 and PP3 leave a project with remaining work alone
  ---
  duration_ms: 1.460569
  ...
# Subtest: PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
ok 3086 - PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
  ---
  duration_ms: 2.485166
  ...
# Subtest: PP6 Sub-projects marker states match display_for_wikilink
ok 3087 - PP6 Sub-projects marker states match display_for_wikilink
  ---
  duration_ms: 1.273451
  ...
# Subtest: PP7 and PP28 keep a future-scheduled ^prj byte-identical
ok 3088 - PP7 and PP28 keep a future-scheduled ^prj byte-identical
  ---
  duration_ms: 0.944714
  ...
# Subtest: PP8 still-blocks a ^prj that waits on another open prerequisite
ok 3089 - PP8 still-blocks a ^prj that waits on another open prerequisite
  ---
  duration_ms: 0.624793
  ...
# Subtest: PP9 already-planned ^prj raises to Next without a new link
ok 3090 - PP9 already-planned ^prj raises to Next without a new link
  ---
  duration_ms: 0.5764
  ...
# Subtest: PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
ok 3091 - PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
  ---
  duration_ms: 2.034084
  ...
# Subtest: PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
ok 3092 - PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
  ---
  duration_ms: 0.859662
  ...
# Subtest: PP14 an id-less last task still pulls in
ok 3093 - PP14 an id-less last task still pulls in
  ---
  duration_ms: 0.407719
  ...
# Subtest: PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
ok 3094 - PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
  ---
  duration_ms: 9.870388
  ...
# Subtest: PP17 one pull-in row wins over project_task
ok 3095 - PP17 one pull-in row wins over project_task
  ---
  duration_ms: 0.679818
  ...
# Subtest: PP18 cancel recovers only
ok 3096 - PP18 cancel recovers only
  ---
  duration_ms: 0.441373
  ...
# Subtest: PP20 unrecognised or unplannable notes never pull in
ok 3097 - PP20 unrecognised or unplannable notes never pull in
  ---
  duration_ms: 1.212536
  ...
# Subtest: PP24 closing an external prerequisite pulls in only when N is empty
ok 3098 - PP24 closing an external prerequisite pulls in only when N is empty
  ---
  duration_ms: 0.952328
  ...
# Subtest: PP25 cascades project_member recovery after a [?] pull-in
ok 3099 - PP25 cascades project_member recovery after a [?] pull-in
  ---
  duration_ms: 1.107665
  ...
# Subtest: PP26 dated recount treats a hidden leftover as remaining work
ok 3100 - PP26 dated recount treats a hidden leftover as remaining work
  ---
  duration_ms: 1.482741
  ...
# Subtest: PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
ok 3101 - PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
  ---
  duration_ms: 1.233235
  ...
# Subtest: successorNoticeText uses the §12.6 pull-in and surfaced copy
ok 3102 - successorNoticeText uses the §12.6 pull-in and surfaced copy
  ---
  duration_ms: 0.504413
  ...
# Subtest: Ctrl+Enter on the last task link inserts the ^prj and rewrites R
ok 3103 - Ctrl+Enter on the last task link inserts the ^prj and rewrites R
  ---
  duration_ms: 10.299879
  ...
# Subtest: PP29 runtime close and reopen use the parent pull-in receipt
ok 3104 - PP29 runtime close and reopen use the parent pull-in receipt
  ---
  duration_ms: 5.150515
  ...
# Subtest: PP18 Alt+[ cancel of the last task surfaces R without linking
ok 3105 - PP18 Alt+[ cancel of the last task surfaces R without linking
  ---
  duration_ms: 18.843533
  ...
# Subtest: PP19 same-day reopen restores R byte-for-byte and takes back the link
ok 3106 - PP19 same-day reopen restores R byte-for-byte and takes back the link
  ---
  duration_ms: 3.082717
  ...
# Subtest: a close in a project that still has work stays inside the gate
ok 3107 - a close in a project that still has work stays inside the gate
  ---
  duration_ms: 1.021641
  ...
# Subtest: P1 path-qualified skip keys: same ^review in another note does not suppress
ok 3108 - P1 path-qualified skip keys: same ^review in another note does not suppress
  ---
  duration_ms: 0.478103
  ...
# Subtest: P3 id-less cascade: stale [?] R recovers resident without [id::]
ok 3109 - P3 id-less cascade: stale [?] R recovers resident without [id::]
  ---
  duration_ms: 0.413871
  ...
# Subtest: P4 frontmatter scheduled validity mirrors Rust
ok 3110 - P4 frontmatter scheduled validity mirrors Rust
  ---
  duration_ms: 0.501728
  ...
# Subtest: P5 recognition mirrors Rust (status/type/prj line)
ok 3111 - P5 recognition mirrors Rust (status/type/prj line)
  ---
  duration_ms: 1.188349
  ...
# Subtest: P6 SUBOPEN blank line stops the marker scan (PP6)
ok 3112 - P6 SUBOPEN blank line stops the marker scan (PP6)
  ---
  duration_ms: 0.462012
  ...
# Subtest: promotion prompts default to Tasks in ordinary and project notes
ok 3113 - promotion prompts default to Tasks in ordinary and project notes
  ---
  duration_ms: 4.161078
  ...
# Subtest: promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
ok 3114 - promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
  ---
  duration_ms: 1.248825
  ...
# Subtest: promotion command writes only on accept and Enter selects Tasks
ok 3115 - promotion command writes only on accept and Enter selects Tasks
  ---
  duration_ms: 3.560881
  ...
# Subtest: promotion removes only genuinely empty source sections
ok 3116 - promotion removes only genuinely empty source sections
  ---
  duration_ms: 1.266308
  ...
# Subtest: promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
ok 3117 - promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
  ---
  duration_ms: 1.166638
  ...
# Subtest: Tasks-only preamble promotions prompt and blank Enter moves into Tasks
ok 3118 - Tasks-only preamble promotions prompt and blank Enter moves into Tasks
  ---
  duration_ms: 0.829353
  ...
# Subtest: plain bullets already in Tasks prompt and blank Enter promotes in place
ok 3119 - plain bullets already in Tasks prompt and blank Enter promotes in place
  ---
  duration_ms: 0.983608
  ...
# Subtest: promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
ok 3120 - promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
  ---
  duration_ms: 0.494183
  ...
# Subtest: always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
ok 3121 - always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
  ---
  duration_ms: 3.547374
  ...
# Could not restore all reopened task references [ 'Broken.md: unreadable' ]
# Could not recover all blocked dependents [
#   'BrokenRead.md: read failed',
#   'Stale.md: line 1 changed before recovery',
#   'BrokenWrite.md: write failed'
# ]
# Subtest: direct Done Tasks task reopens through the metadata-aware fallback
ok 3122 - direct Done Tasks task reopens through the metadata-aware fallback
  ---
  duration_ms: 2.534129
  ...
# Subtest: recursive completion status policy includes Next without broadening excluded statuses
ok 3123 - recursive completion status policy includes Next without broadening excluded statuses
  ---
  duration_ms: 0.307197
  ...
# Subtest: recursive completion closes a Next root and its nested Next descendant
ok 3124 - recursive completion closes a Next root and its nested Next descendant
  ---
  duration_ms: 3.490165
  ...
# Subtest: recursive completion traverses Done parents and skips excluded siblings
ok 3125 - recursive completion traverses Done parents and skips excluded siblings
  ---
  duration_ms: 1.108096
  ...
# Subtest: closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
ok 3126 - closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
  ---
  duration_ms: 1.503532
  ...
# Subtest: reopened-reference restoration is ancestry-aware, conservative, and idempotent
ok 3127 - reopened-reference restoration is ancestry-aware, conservative, and idempotent
  ---
  duration_ms: 1.407147
  ...
# Subtest: retirement preserves task-tree markers and unmarks Pomodoro embeds
ok 3128 - retirement preserves task-tree markers and unmarks Pomodoro embeds
  ---
  duration_ms: 0.399563
  ...
# Subtest: done Pomodoro retirement removes only the matching embedded marker
ok 3129 - done Pomodoro retirement removes only the matching embedded marker
  ---
  duration_ms: 0.305544
  ...
# Subtest: retirement stops at prose boundaries and pairs strikethrough spans
ok 3130 - retirement stops at prose boundaries and pairs strikethrough spans
  ---
  duration_ms: 0.432025
  ...
# Subtest: retired Pomodoro links are not copied into the next Pomodoro
ok 3131 - retired Pomodoro links are not copied into the next Pomodoro
  ---
  duration_ms: 1.305914
  ...
# Subtest: retirement coordinator rewrites active editor and vault notes together
ok 3132 - retirement coordinator rewrites active editor and vault notes together
  ---
  duration_ms: 1.00583
  ...
# Subtest: restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
ok 3133 - restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
  ---
  duration_ms: 1.306064
  ...
# Subtest: close and reopen reference mutations share one serialized queue
ok 3134 - close and reopen reference mutations share one serialized queue
  ---
  duration_ms: 0.273733
  ...
# Subtest: post-close finalizer runs one gated plan before reference retirement
ok 3135 - post-close finalizer runs one gated plan before reference retirement
  ---
  duration_ms: 0.490246
  ...
# Subtest: dependent recovery uses live editor buffers and preserves the cursor
ok 3136 - dependent recovery uses live editor buffers and preserves the cursor
  ---
  duration_ms: 2.927881
  ...
# Subtest: dependent recovery preserves successful siblings across stale and failed notes
ok 3137 - dependent recovery preserves successful siblings across stale and failed notes
  ---
  duration_ms: 1.357903
  ...
# Subtest: no-op vault transforms and irrelevant retirement files avoid process writes
ok 3138 - no-op vault transforms and irrelevant retirement files avoid process writes
  ---
  duration_ms: 0.328147
  ...
# Subtest: ambiguity scans and notices are cached while dependency identity lines stay stable
ok 3139 - ambiguity scans and notices are cached while dependency identity lines stay stable
  ---
  duration_ms: 0.536023
  ...
# Subtest: non-Vim open/done command finalizes the closed task identity
ok 3140 - non-Vim open/done command finalizes the closed task identity
  ---
  duration_ms: 0.399543
  ...
# Subtest: non-Vim open/done command restores the reopened task identity
ok 3141 - non-Vim open/done command restores the reopened task identity
  ---
  duration_ms: 0.339409
  ...
# Subtest: full Pomodoro completion retires embeds only after carry-forward planning
ok 3142 - full Pomodoro completion retires embeds only after carry-forward planning
  ---
  duration_ms: 6.280373
  ...
# Subtest: full Pomodoro completion recovers after a deduplicated multi-target batch
ok 3143 - full Pomodoro completion recovers after a deduplicated multi-target batch
  ---
  duration_ms: 7.080511
  ...
# Subtest: full Pomodoro completion moves a marked same-note link without history
ok 3144 - full Pomodoro completion moves a marked same-note link without history
  ---
  duration_ms: 0.746606
  ...
# Subtest: cycler LK1–LK19 recognises only relation line shapes
ok 3145 - cycler LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 1.478653
  ...
# Subtest: cycler MC10, MC11, MC12 and MC14 keep relations inert while allowing root-only gestures
ok 3146 - cycler MC10, MC11, MC12 and MC14 keep relations inert while allowing root-only gestures
  ---
  duration_ms: 2.0578
  ...
# Subtest: SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
ok 3147 - SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
  ---
  duration_ms: 23.522659
  ...
# Subtest: SO2–SO5 fan-outs with explicit selection (SO32 twenty)
ok 3148 - SO2–SO5 fan-outs with explicit selection (SO32 twenty)
  ---
  duration_ms: 9.110297
  ...
# Subtest: SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
ok 3149 - SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
  ---
  duration_ms: 1.285114
  ...
# Subtest: SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
ok 3150 - SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
  ---
  duration_ms: 1.418058
  ...
# Subtest: SO stable keys survive insertions/status changes; ambiguous rebinding refused
ok 3151 - SO stable keys survive insertions/status changes; ambiguous rebinding refused
  ---
  duration_ms: 2.233124
  ...
# Subtest: SO picker model, pick normalization, and API detection
ok 3152 - SO picker model, pick normalization, and API detection
  ---
  duration_ms: 0.690969
  ...
# Subtest: SO notice copy for offers (SO20, mixed, failure)
ok 3153 - SO notice copy for offers (SO20, mixed, failure)
  ---
  duration_ms: 0.589185
  ...
# Subtest: destination override to an existing entry inserts as its child
ok 3154 - destination override to an existing entry inserts as its child
  ---
  duration_ms: 2.61283
  ...
# Subtest: destination override with a stale preimage skips loudly
ok 3155 - destination override with a stale preimage skips loudly
  ---
  duration_ms: 0.927401
  ...
# Subtest: destination override with a closed entry skips loudly
ok 3156 - destination override with a closed entry skips loudly
  ---
  duration_ms: 0.998477
  ...
# Subtest: destination override with a new name creates one placeholder after the running entry
ok 3157 - destination override with a new name creates one placeholder after the running entry
  ---
  duration_ms: 0.838491
  ...
# Subtest: destination override with a new name racing an open entry joins it
ok 3158 - destination override with a new name racing an open entry joins it
  ---
  duration_ms: 0.677373
  ...
# Subtest: reopen takes back the untouched successor link and restores status
ok 3159 - reopen takes back the untouched successor link and restores status
  ---
  duration_ms: 21.542978
  ...
# Subtest: an edited successor bullet survives while its status still restores
ok 3160 - an edited successor bullet survives while its status still restores
  ---
  duration_ms: 3.242342
  ...
# Subtest: an edited successor status line survives while its link is taken back
ok 3161 - an edited successor status line survives while its link is taken back
  ---
  duration_ms: 3.847837
  ...
# Subtest: reopen on a different day leaves successor links alone
ok 3162 - reopen on a different day leaves successor links alone
  ---
  duration_ms: 2.591679
  ...
# Subtest: reopening a task closed without a pass shows no take-back
ok 3163 - reopening a task closed without a pass shows no take-back
  ---
  duration_ms: 1.452955
  ...
# Subtest: Alt+] on a planned prerequisite links its successor
ok 3164 - Alt+] on a planned prerequisite links its successor
  ---
  duration_ms: 9.444094
  ...
# Subtest: take-back deletes a pre-existing entry it empties
ok 3165 - take-back deletes a pre-existing entry it empties
  ---
  duration_ms: 2.730034
  ...
# Subtest: take-back deletes a stub-replaced entry through the vault
ok 3166 - take-back deletes a stub-replaced entry through the vault
  ---
  duration_ms: 0.396116
  ...
# Subtest: take-back keeps entries that are closed or keep another child
ok 3167 - take-back keeps entries that are closed or keep another child
  ---
  duration_ms: 0.420302
  ...
# Subtest: closing-entry relocation finds a deferred-only placeholder
ok 3168 - closing-entry relocation finds a deferred-only placeholder
  ---
  duration_ms: 0.467503
  ...
# Subtest: Alt+[ into Cancelled recovers its dependents without linking
ok 3169 - Alt+[ into Cancelled recovers its dependents without linking
  ---
  duration_ms: 2.577793
  ...
# Subtest: take-back keeps an entry whose prose survives across a blank line (both paths)
ok 3170 - take-back keeps an entry whose prose survives across a blank line (both paths)
  ---
  duration_ms: 0.500325
  ...
# Subtest: take-back deletes a whole block with continuation/fence leftovers (LF/CRLF, final newline)
ok 3171 - take-back deletes a whole block with continuation/fence leftovers (LF/CRLF, final newline)
  ---
  duration_ms: 0.826829
  ...
# Subtest: link close links the unblocked successor into the slot and shows the nav card
ok 3172 - link close links the unblocked successor into the slot and shows the nav card
  ---
  duration_ms: 20.511969
  ...
# Subtest: close with no [id::] performs zero vault reads and shows nothing
ok 3173 - close with no [id::] performs zero vault reads and shows nothing
  ---
  duration_ms: 1.163792
  ...
# Subtest: Warm finalize reads no unrelated note bodies on the real close path
ok 3174 - Warm finalize reads no unrelated note bodies on the real close path
  ---
  duration_ms: 3.365487
  ...
# Subtest: cold fallback still recovers and links without a Tasks cache
ok 3175 - cold fallback still recovers and links without a Tasks cache
  ---
  duration_ms: 4.029014
  ...
# Subtest: recovered-only close reports unblocked without linking (SO4 Esc)
ok 3176 - recovered-only close reports unblocked without linking (SO4 Esc)
  ---
  duration_ms: 2.056918
  ...
# Subtest: walk landing composes a single toast and shows no card
ok 3177 - walk landing composes a single toast and shows no card
  ---
  duration_ms: 8.228222
  ...
# Subtest: nav absent falls back to a plain Notice with no link (SO missing picker)
ok 3178 - nav absent falls back to a plain Notice with no link (SO missing picker)
  ---
  duration_ms: 2.408279
  ...
# Subtest: stale cache heals via re-plan from fresh text (SO30)
ok 3179 - stale cache heals via re-plan from fresh text (SO30)
  ---
  duration_ms: 2.101633
  ...
# Subtest: Pomodoro-line close appends the successor to the created continuation
ok 3180 - Pomodoro-line close appends the successor to the created continuation
  ---
  duration_ms: 6.204237
  ...
# Subtest: Pomodoro-line close keeps the closing anchor after the picker re-plan
ok 3181 - Pomodoro-line close keeps the closing anchor after the picker re-plan
  ---
  duration_ms: 3.466851
  ...
# Subtest: completeTaskAtCursor returns the notice and shows nothing itself
ok 3182 - completeTaskAtCursor returns the notice and shows nothing itself
  ---
  duration_ms: 1.948671
  ...
# Subtest: successor apply recovers project residents without ledger v12
ok 3183 - successor apply recovers project residents without ledger v12
  ---
  duration_ms: 11.894513
  ...
# Subtest: SB vectors pin the successor mint pipeline
ok 3184 - SB vectors pin the successor mint pipeline
  ---
  duration_ms: 2.232273
  ...
# Subtest: successor suggester ports the Rust candidate and suffix rules
ok 3185 - successor suggester ports the Rust candidate and suffix rules
  ---
  duration_ms: 0.634351
  ...
# Subtest: successor link form names unique basenames short and the day file always
ok 3186 - successor link form names unique basenames short and the day file always
  ---
  duration_ms: 0.399172
  ...
# Subtest: tasksFromDocuments normalizes vault lines to pool shape
ok 3187 - tasksFromDocuments normalizes vault lines to pool shape
  ---
  duration_ms: 1.091144
  ...
# Subtest: normalizeTasksCacheTask ports every known Tasks shape
ok 3188 - normalizeTasksCacheTask ports every known Tasks shape
  ---
  duration_ms: 0.387439
  ...
# Subtest: buildDependentsIndex keeps first task IDs and groups dependents
ok 3189 - buildDependentsIndex keeps first task IDs and groups dependents
  ---
  duration_ms: 0.199571
  ...
# Subtest: findLiveLinks counts plain, embedded, and deferred links under open entries only
ok 3190 - findLiveLinks counts plain, embedded, and deferred links under open entries only
  ---
  duration_ms: 2.395956
  ...
# Subtest: computeSuccessorAnchors implements closing, slot, inherit, and none
ok 3191 - computeSuccessorAnchors implements closing, slot, inherit, and none
  ---
  duration_ms: 0.866494
  ...
# Subtest: SL1 links the successor right after the predecessor bullet
ok 3192 - SL1 links the successor right after the predecessor bullet
  ---
  duration_ms: 5.49345
  ...
# Subtest: SL3 still-blocked rows count the open prerequisites left
ok 3193 - SL3 still-blocked rows count the open prerequisites left
  ---
  duration_ms: 0.868368
  ...
# Subtest: SL4 future-scheduled dependents stay Blocked with the date row
ok 3194 - SL4 future-scheduled dependents stay Blocked with the date row
  ---
  duration_ms: 0.60781
  ...
# Subtest: SL5 already-planned dependents recover without a duplicate link
ok 3195 - SL5 already-planned dependents recover without a duplicate link
  ---
  duration_ms: 0.977507
  ...
# Subtest: SL6 struck and closed-entry links do not count as planned
ok 3196 - SL6 struck and closed-entry links do not count as planned
  ---
  duration_ms: 2.038382
  ...
# Subtest: SL7 closing anchors create the continuation placeholder
ok 3197 - SL7 closing anchors create the continuation placeholder
  ---
  duration_ms: 1.164924
  ...
# Subtest: SL8 closing anchors append after carried lines in the continuation
ok 3198 - SL8 closing anchors append after carried lines in the continuation
  ---
  duration_ms: 0.776452
  ...
# Subtest: SL9 unplanned predecessors offer at the implicit destination (SO14)
ok 3199 - SL9 unplanned predecessors offer at the implicit destination (SO14)
  ---
  duration_ms: 1.217294
  ...
# Subtest: SL10 missing block IDs mint through the SB rule
ok 3200 - SL10 missing block IDs mint through the SB rule
  ---
  duration_ms: 0.557044
  ...
# Subtest: SL11 project and hidden tasks recover but never link
ok 3201 - SL11 project and hidden tasks recover but never link
  ---
  duration_ms: 9.041245
  ...
# Subtest: PDC1 leaves a dependency-ready resident Blocked while its project still waits
ok 3202 - PDC1 leaves a dependency-ready resident Blocked while its project still waits
  ---
  duration_ms: 1.910098
  ...
# Subtest: PDC2 residents are offered under the project group (SO1)
ok 3203 - PDC2 residents are offered under the project group (SO1)
  ---
  duration_ms: 1.431233
  ...
# Subtest: PDC3 keeps a project resident Blocked when its own prerequisite remains open
ok 3204 - PDC3 keeps a project resident Blocked when its own prerequisite remains open
  ---
  duration_ms: 0.84849
  ...
# Subtest: PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
ok 3205 - PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
  ---
  duration_ms: 2.077898
  ...
# Subtest: SL12 one gesture closing two prerequisites links once with both causes
ok 3206 - SL12 one gesture closing two prerequisites links once with both causes
  ---
  duration_ms: 0.452915
  ...
# Subtest: SL13 chains do not recurse: the dependent's own dependents wait
ok 3207 - SL13 chains do not recurse: the dependent's own dependents wait
  ---
  duration_ms: 0.386849
  ...
# Subtest: SL14 ambiguous basenames link long
ok 3208 - SL14 ambiguous basenames link long
  ---
  duration_ms: 0.449889
  ...
# Subtest: SL15 stale open dependents link and become Next
ok 3209 - SL15 stale open dependents link and become Next
  ---
  duration_ms: 0.437756
  ...
# Subtest: SL16 gates on [id::]: no identity means no lookup and empty rows
ok 3210 - SL16 gates on [id::]: no identity means no lookup and empty rows
  ---
  duration_ms: 0.309791
  ...
# Subtest: SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
ok 3211 - SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
  ---
  duration_ms: 1.47152
  ...
# Subtest: SL18 the kill switch recovers without linking or minting
ok 3212 - SL18 the kill switch recovers without linking or minting
  ---
  duration_ms: 0.344107
  ...
# Subtest: SL19 re-applied closes write nothing and report nothing
ok 3213 - SL19 re-applied closes write nothing and report nothing
  ---
  duration_ms: 0.269575
  ...
# Subtest: SL23 subtasks anchor at their root's link
ok 3214 - SL23 subtasks anchor at their root's link
  ---
  duration_ms: 0.405465
  ...
# Subtest: SL24 later same-name entries take the closing successors
ok 3215 - SL24 later same-name entries take the closing successors
  ---
  duration_ms: 0.480908
  ...
# Subtest: SL25 already-Next planned dependents produce no row
ok 3216 - SL25 already-Next planned dependents produce no row
  ---
  duration_ms: 0.405805
  ...
# Subtest: SL26 inbox successors carry the inbox flag
ok 3217 - SL26 inbox successors carry the inbox flag
  ---
  duration_ms: 0.289873
  ...
# Subtest: SL27 dropped links are never re-linked and recover to Ready
ok 3218 - SL27 dropped links are never re-linked and recover to Ready
  ---
  duration_ms: 0.370267
  ...
# Subtest: SL28 day-file successors name the note, never the bare link
ok 3219 - SL28 day-file successors name the note, never the bare link
  ---
  duration_ms: 0.326012
  ...
# Subtest: slot insertions land after the anchor subtree with its indent
ok 3220 - slot insertions land after the anchor subtree with its indent
  ---
  duration_ms: 0.236331
  ...
# Subtest: closing insertions replace a lone stub child
ok 3221 - closing insertions replace a lone stub child
  ---
  duration_ms: 0.501177
  ...
# Subtest: insertions skip placements with no valid target
ok 3222 - insertions skip placements with no valid target
  ---
  duration_ms: 0.142873
  ...
# Subtest: successorNoticeText implements the §12.6 table
ok 3223 - successorNoticeText implements the §12.6 table
  ---
  duration_ms: 0.521596
  ...
# Subtest: parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
ok 3224 - parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
  ---
  duration_ms: 0.402078
  ...
# Subtest: loadLinkUnblocked stat-caches the config read
ok 3225 - loadLinkUnblocked stat-caches the config read
  ---
  duration_ms: 0.297598
  ...
# Subtest: loadLinkUnblocked treats missing or unreadable config as true
ok 3226 - loadLinkUnblocked treats missing or unreadable config as true
  ---
  duration_ms: 1.127754
  ...
# Subtest: successorPlanConfigPath honors XDG_CONFIG_HOME
ok 3227 - successorPlanConfigPath honors XDG_CONFIG_HOME
  ---
  duration_ms: 0.165677
  ...
# Subtest: todayDailyPath mirrors the ledger daily path
ok 3228 - todayDailyPath mirrors the ledger daily path
  ---
  duration_ms: 0.512238
  ...
# Subtest: normalizeClosedTaskIdentities keeps the anchor root off the match gate
ok 3229 - normalizeClosedTaskIdentities keeps the anchor root off the match gate
  ---
  duration_ms: 0.19886
  ...
# Subtest: ID-less planned roots anchor ID-bearing children without minting IDs
ok 3230 - ID-less planned roots anchor ID-bearing children without minting IDs
  ---
  duration_ms: 0.609724
  ...
# Subtest: successor anchors never guess across roots
ok 3231 - successor anchors never guess across roots
  ---
  duration_ms: 0.41861
  ...
# Subtest: a child with its own live link keeps its own slot
ok 3232 - a child with its own live link keeps its own slot
  ---
  duration_ms: 0.389294
  ...
# Subtest: getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
ok 3233 - getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
  ---
  duration_ms: 0.229378
  ...
# Subtest: countSuccessorBasenames walks the vault set, not the task set
ok 3234 - countSuccessorBasenames walks the vault set, not the task set
  ---
  duration_ms: 0.322596
  ...
# Subtest: the pass threads a richer isInbox into unblocked rows
ok 3235 - the pass threads a richer isInbox into unblocked rows
  ---
  duration_ms: 0.353245
  ...
# Subtest: getTaskLinkLaneApi returns the lane only when version and both functions exist
ok 3236 - getTaskLinkLaneApi returns the lane only when version and both functions exist
  ---
  duration_ms: 1.004548
  ...
# Subtest: isTaskLinkLaneLine passes content, line, and path and never throws
ok 3237 - isTaskLinkLaneLine passes content, line, and path and never throws
  ---
  duration_ms: 1.05815
  ...
# Subtest: single Alt+] on a Task Link delegates with exactly { editor, view }
ok 3238 - single Alt+] on a Task Link delegates with exactly { editor, view }
  ---
  duration_ms: 0.517167
  ...
# Subtest: Alt+[ and Alt+] delegate identically; direction is ignored
ok 3239 - Alt+[ and Alt+] delegate identically; direction is ignored
  ---
  duration_ms: 0.306686
  ...
# Subtest: embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
ok 3240 - embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
  ---
  duration_ms: 0.295845
  ...
# Subtest: entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
ok 3241 - entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
  ---
  duration_ms: 2.669047
  ...
# Subtest: counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
ok 3242 - counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
  ---
  duration_ms: 0.611488
  ...
# Subtest: counted dispatch without an explicit repeat leaves the key alone
ok 3243 - counted dispatch without an explicit repeat leaves the key alone
  ---
  duration_ms: 0.204561
  ...
# Subtest: counted range starting elsewhere skips Task Link lines
ok 3244 - counted range starting elsewhere skips Task Link lines
  ---
  duration_ms: 1.726096
  ...
# Subtest: legacy fallback with no api keeps today's behavior
ok 3245 - legacy fallback with no api keeps today's behavior
  ---
  duration_ms: 0.682643
  ...
# Subtest: plain Task Link in an open Pomodoro closes the task root-only and strikes the link
ok 3246 - plain Task Link in an open Pomodoro closes the task root-only and strikes the link
  ---
  duration_ms: 14.645156
  ...
# Subtest: marked plain Task Link drops its marker when struck under Pomodoro ancestry
ok 3247 - marked plain Task Link drops its marker when struck under Pomodoro ancestry
  ---
  duration_ms: 1.552334
  ...
# Subtest: plain Pomodoro Task Link closes root-only while embedded closes recursively
ok 3248 - plain Pomodoro Task Link closes root-only while embedded closes recursively
  ---
  duration_ms: 2.174472
  ...
# Subtest: embedded Pomodoro Task Link still closes recursively and retires to struck form
ok 3249 - embedded Pomodoro Task Link still closes recursively and retires to struck form
  ---
  duration_ms: 2.497599
  ...
# Subtest: Ctrl+Enter toggles a struck plain Pomodoro link back to open
ok 3250 - Ctrl+Enter toggles a struck plain Pomodoro link back to open
  ---
  duration_ms: 1.86969
  ...
# Subtest: same-file plain Task Link closes and strikes the correct line
ok 3251 - same-file plain Task Link closes and strikes the correct line
  ---
  duration_ms: 1.057589
  ...
# Subtest: cursor selects which of several Task Links closes and strikes
ok 3252 - cursor selects which of several Task Links closes and strikes
  ---
  duration_ms: 1.290725
  ...
# Subtest: plain links to Blocked or non-task blocks still complete the Pomodoro
ok 3253 - plain links to Blocked or non-task blocks still complete the Pomodoro
  ---
  duration_ms: 3.690046
  ...
# Subtest: strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
ok 3254 - strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
  ---
  duration_ms: 0.514592
  ...
# Subtest: completeTaskAtCursor closes each open symbol through the Tasks command
ok 3255 - completeTaskAtCursor closes each open symbol through the Tasks command
  ---
  duration_ms: 1.711508
  ...
# Subtest: completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
ok 3256 - completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
  ---
  duration_ms: 0.352202
  ...
# Subtest: completeTaskAtCursor refuses closed, cancelled, and non-task lines
ok 3257 - completeTaskAtCursor refuses closed, cancelled, and non-task lines
  ---
  duration_ms: 0.316595
  ...
# Subtest: completeTaskAtCursor refuses a missing Tasks command with no write
ok 3258 - completeTaskAtCursor refuses a missing Tasks command with no write
  ---
  duration_ms: 0.153853
  ...
# Subtest: Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
ok 3259 - Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
  ---
  duration_ms: 0.509543
  ...
# Subtest: completeTaskAtCursor reports not-closed when Tasks does not write [x]
ok 3260 - completeTaskAtCursor reports not-closed when Tasks does not write [x]
  ---
  duration_ms: 0.171357
  ...
# Subtest: recovery api is frozen at version 2 and recovers without striking references
ok 3261 - recovery api is frozen at version 2 and recovers without striking references
  ---
  duration_ms: 2.622227
  ...
# Subtest: recovery api never throws and reports failures
ok 3262 - recovery api never throws and reports failures
  ---
  duration_ms: 0.221874
  ...
# Subtest: future-scheduled dependents stay Blocked on the planner, api, and close paths
ok 3263 - future-scheduled dependents stay Blocked on the planner, api, and close paths
  ---
  duration_ms: 14.619287
  ...
# Subtest: Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
ok 3264 - Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
  ---
  duration_ms: 3.630745
  ...
# Subtest: every printable non-space ASCII key resolves to a surround pair
ok 3265 - every printable non-space ASCII key resolves to a surround pair
  ---
  duration_ms: 3.679717
  ...
# Subtest: visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
ok 3266 - visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
  ---
  duration_ms: 0.593844
  ...
# Subtest: non-visible, combining, multi-character, and multi-code-unit values are rejected
ok 3267 - non-visible, combining, multi-character, and multi-code-unit values are rejected
  ---
  duration_ms: 0.231703
  ...
# Subtest: ys adds broad symmetric delimiters through pending keydown
ok 3268 - ys adds broad symmetric delimiters through pending keydown
  ---
  duration_ms: 1.149234
  ...
# Subtest: rejected keydown input never edits or leaks into a pending ys
ok 3269 - rejected keydown input never edits or leaks into a pending ys
  ---
  duration_ms: 0.363965
  ...
# Subtest: Escape cancels ys, cs, and ds pending state without editing
ok 3270 - Escape cancels ys, cs, and ds pending state without editing
  ---
  duration_ms: 0.25687
  ...
# Subtest: cs accepts broad target and replacement characters independently
ok 3271 - cs accepts broad target and replacement characters independently
  ---
  duration_ms: 1.014998
  ...
# Subtest: cs preserves structural alias and padding rules
ok 3272 - cs preserves structural alias and padding rules
  ---
  duration_ms: 0.54468
  ...
# Subtest: cs replaces repeated symmetric runs exactly once on each side
ok 3273 - cs replaces repeated symmetric runs exactly once on each side
  ---
  duration_ms: 0.509213
  ...
# Subtest: ds removes representative broad symmetric delimiters
ok 3274 - ds removes representative broad symmetric delimiters
  ---
  duration_ms: 0.744572
  ...
# Subtest: ds preserves structural alias and padding rules
ok 3275 - ds preserves structural alias and padding rules
  ---
  duration_ms: 0.315592
  ...
# Subtest: ds removes one pair from repeated runs, including the reported block link
ok 3276 - ds removes one pair from repeated runs, including the reported block link
  ---
  duration_ms: 1.074292
  ...
# Subtest: consecutive ds commands peel a triple symmetric surround
ok 3277 - consecutive ds commands peel a triple symmetric surround
  ---
  duration_ms: 0.208218
  ...
# Subtest: symmetric discovery uses deterministic sequential same-line run pairs
ok 3278 - symmetric discovery uses deterministic sequential same-line run pairs
  ---
  duration_ms: 0.151148
  ...
# Subtest: symmetric discovery includes every character in repeated boundaries
ok 3279 - symmetric discovery includes every character in repeated boundaries
  ---
  duration_ms: 0.289143
  ...
# Subtest: unpaired and unequal symmetric runs are safe no-ops
ok 3280 - unpaired and unequal symmetric runs are safe no-ops
  ---
  duration_ms: 0.231131
  ...
# Subtest: ordinary normal-mode keys remain untouched outside pending state
ok 3281 - ordinary normal-mode keys remain untouched outside pending state
  ---
  duration_ms: 0.187859
  ...
# Subtest: dot while a surround is pending is a literal delimiter, not repeat
ok 3282 - dot while a surround is pending is a literal delimiter, not repeat
  ---
  duration_ms: 0.131511
  ...
# Subtest: dot-repeat records and replays broad-character ys
ok 3283 - dot-repeat records and replays broad-character ys
  ---
  duration_ms: 0.248334
  ...
# Subtest: dot-repeat records and replays broad-character cs
ok 3284 - dot-repeat records and replays broad-character cs
  ---
  duration_ms: 0.190013
  ...
# Subtest: dot-repeat records and replays broad-character ds
ok 3285 - dot-repeat records and replays broad-character ds
  ---
  duration_ms: 0.17827
  ...
# Subtest: dot-repeat replays cs against repeated symmetric runs
ok 3286 - dot-repeat replays cs against repeated symmetric runs
  ---
  duration_ms: 0.201835
  ...
# Subtest: dot-repeat replays ds against repeated symmetric runs
ok 3287 - dot-repeat replays ds against repeated symmetric runs
  ---
  duration_ms: 0.206694
  ...
# Subtest: consecutive dot-repeats peel a triple symmetric surround
ok 3288 - consecutive dot-repeats peel a triple symmetric surround
  ---
  duration_ms: 0.236221
  ...
1..3288
# tests 3298
# suites 0
# pass 3290
# fail 8
# cancelled 0
# skipped 0
# todo 0
# duration_ms 7170.929681
failed  exit=1  duration=15002ms

