# Chat History - ace-run (bob-cli-aq.1--mon)

- **TIMESTAMP:** 2026-10-23 07:00:20 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-aq.1--mon

## Prompt

sase monitor start --command 'npm test' --reason 'Run the bob-plugins full npm test suite for phase bob-cli-aq.1'

## Response

sase tool run 98aa9f380ece318e75f53b346b738d7b

> bob-plugins@0.1.0 test
> node scripts/build-plugins.mjs --check && npm run docs:inventory:check && node --test scripts/test-project-tasks-snapshot.cjs scripts/test-bob-articles.cjs scripts/test-dependency-line-migration.cjs scripts/test-navigation-hotkeys-section-nav.cjs scripts/test-navigation-hotkeys-rename.cjs scripts/test-navigation-hotkeys-ref-pdf.cjs scripts/test-navigation-hotkeys-templater-trigger.cjs scripts/test-navigation-hotkeys-schedule-recovery.cjs scripts/test-navigation-hotkeys-schedule-properties.cjs scripts/test-navigation-hotkeys-schedule-writes.cjs scripts/test-navigation-hotkeys-runtime-schedule.cjs scripts/test-navigation-hotkeys-dependencies.cjs scripts/test-navigation-blocks-guards.cjs scripts/test-navigation-blocks-writers.cjs scripts/test-navigation-blocks-edit.cjs scripts/test-navigation-blocks-stage-view.cjs scripts/test-navigation-hotkeys-dependency-mirror.cjs scripts/test-navigation-hotkeys-task-move-plan.cjs scripts/test-navigation-hotkeys-priority-notice.cjs scripts/test-navigation-successor-picker.cjs scripts/test-navigation-image-zoom-viewer.cjs scripts/test-navigation-hotkeys-unblocked-notice.cjs scripts/test-navigation-project-blocking.cjs scripts/test-navigation-project-dependency-stage.cjs scripts/test-navigation-project-subprojects.cjs scripts/test-navigation-project-subtree-gestures.cjs scripts/test-navigation-hotkeys-priority-picker.cjs scripts/test-navigation-hotkeys-picker-lifecycle.cjs scripts/test-navigation-hotkeys-ref-picker-text.cjs scripts/test-navigation-hotkeys-pomodoro-move-pickers.cjs scripts/test-navigation-inbox-route.cjs scripts/test-navigation-inbox-route-card.cjs scripts/test-navigation-hotkeys-task-move.cjs scripts/test-navigation-open-notes-uri.cjs scripts/test-navigation-hotkeys-dash-open.cjs scripts/test-navigation-goto-task-uri.cjs scripts/test-navigation-hotkeys-open-task-jump.cjs scripts/test-navigation-hotkeys-vim-counts.cjs scripts/test-navigation-hotkeys-tab-pin.cjs scripts/test-navigation-hotkeys-schedule-log.cjs scripts/test-navigation-hotkeys-schedule-review.cjs scripts/test-navigation-hotkeys-deferred-pomodoro.cjs scripts/test-navigation-hotkeys-pomodoro-parse.cjs scripts/test-navigation-hotkeys-pomodoro-bullet-move.cjs scripts/test-navigation-hotkeys-pomodoro-split-rename.cjs scripts/test-navigation-hotkeys-pomodoro-reorder.cjs scripts/test-navigation-hotkeys-runtime-prune.cjs scripts/test-navigation-hotkeys-project-from-task.cjs scripts/test-navigation-hotkeys-project-reversal.cjs scripts/test-navigation-hotkeys-link-picker.cjs scripts/test-navigation-hotkeys-lane-toggle.cjs scripts/test-navigation-hotkeys-task-link-lane.cjs scripts/test-navigation-hotkeys-cancel-log.cjs scripts/test-navigation-hotkeys-cancel-task.cjs scripts/test-navigation-hotkeys-forward-promotion.cjs scripts/test-navigation-hotkeys-schedule-work-log.cjs scripts/test-navigation-hotkeys-task-move-history.cjs scripts/test-navigation-jump-history.cjs scripts/test-navigation-dependencies.cjs scripts/test-navigation-editor-line-diff.cjs scripts/test-navigation-quick-roll.cjs scripts/test-navigation-roll-decay.cjs scripts/test-navigation-decay-planner.cjs scripts/test-navigation-task-card-model.cjs scripts/test-navigation-task-card-view.cjs scripts/test-navigation-task-card-schedule.cjs scripts/test-navigation-task-card-review.cjs scripts/test-navigation-decision-card.cjs scripts/test-navigation-decision-card-handlers.cjs scripts/test-navigation-refresh-modal.cjs scripts/test-navigation-freshness.cjs scripts/test-navigation-stamps.cjs scripts/test-navigation-keep-counting.cjs scripts/test-navigation-checklist.cjs scripts/test-navigation-review-advance.cjs scripts/test-navigation-review-advance-gestures.cjs scripts/test-navigation-checklist-ctrl-enter.cjs scripts/test-ledger-tools-navigation.cjs scripts/test-ledger-tools-plan-budget.cjs scripts/test-ledger-tools-ready-badge.cjs scripts/test-ledger-tools-note-ready.cjs scripts/test-ledger-tools-note-ready-views.cjs scripts/test-ledger-tools-dashboard-parity.cjs scripts/test-ledger-tools-work-badge-tone.cjs scripts/test-ledger-tools-dashboard-collections.cjs scripts/test-ledger-tools-today.cjs scripts/test-ledger-tools-freshness-placement.cjs scripts/test-ledger-tools-freshness-states.cjs scripts/test-ledger-tools-freshness-namespace.cjs scripts/test-ledger-tools-freshness-review-model.cjs scripts/test-ledger-tools-freshness-queue.cjs scripts/test-ledger-tools-freshness-tracking.cjs scripts/test-ledger-tools-freshness-footer.cjs scripts/test-ledger-tools-freshness-recurring.cjs scripts/test-ledger-tools-freshness-mark.cjs scripts/test-ledger-tools-freshness-mark-surfaces.cjs scripts/test-ledger-tools-priority-marks.cjs scripts/test-ledger-tools-task-tag-marks.cjs scripts/test-ledger-tools-today-marks.cjs scripts/test-ledger-tools-today-marks-reading.cjs scripts/test-ledger-tools-unblocked-glyph.cjs scripts/test-ledger-tools-progress-marks.cjs scripts/test-ledger-tools-date-marks.cjs scripts/test-ledger-tools-recurrence-marks.cjs scripts/test-ledger-tools-date-marks-tasks.cjs scripts/test-ledger-tools-freshness-keeps.cjs scripts/test-ledger-tools-freshness-unblocked.cjs scripts/test-ledger-tools-freshness-decision-card.cjs scripts/test-ledger-tools-dependency-chips.cjs scripts/test-ledger-tools-blocks-chips.cjs scripts/test-ledger-tools-snippets.cjs scripts/test-ledger-tools-vim-mappings.cjs scripts/test-task-status-cycler-dependencies.cjs scripts/test-task-status-cycler-blocks-guards.cjs scripts/test-task-status-cycler-ctrl-enter.cjs scripts/test-task-status-cycler-reference-lifecycle.cjs scripts/test-task-status-cycler-pomodoro-completion.cjs scripts/test-task-status-cycler-pomodoro-work-log.cjs scripts/test-task-status-cycler-pomodoro-reopen.cjs scripts/test-task-status-cycler-blocked-schedule.cjs scripts/test-task-status-cycler-demotion-picker.cjs scripts/test-task-status-cycler-promotion.cjs scripts/test-task-status-cycler-counted-toggle.cjs scripts/test-task-status-cycler-successors.cjs scripts/test-task-status-cycler-successor-wiring.cjs scripts/test-task-status-cycler-successor-polish.cjs scripts/test-task-status-cycler-successor-offers.cjs scripts/test-task-status-cycler-project-pull-in.cjs scripts/test-task-status-cycler-task-links-api.cjs scripts/test-task-status-cycler-task-link-lane.cjs scripts/test-task-status-cycler-freshness.cjs scripts/test-block-id-prompt-dependencies.cjs scripts/test-block-id-prompt-blocks-guards.cjs scripts/test-block-id-prompt-ref-picker-text.cjs scripts/test-block-id-prompt-markers.cjs scripts/test-block-id-prompt-pomodoro-context.cjs scripts/test-block-id-prompt-target-update.cjs scripts/test-block-id-prompt-pomodoro-insertion.cjs scripts/test-block-id-prompt-pomodoro-targets.cjs scripts/test-block-id-prompt-pomodoro-picker-view.cjs scripts/test-block-id-prompt-pomodoro-picker-runtime.cjs scripts/test-block-id-prompt-work-log.cjs scripts/test-block-id-prompt-pomodoro-link-runtime.cjs scripts/test-block-id-prompt-pomodoro-link-picker-api.cjs scripts/test-block-id-prompt-pomodoro-unlink-runtime.cjs scripts/test-block-id-prompt-task-link-deletion.cjs scripts/test-block-id-prompt-plan-budget-and-freshness.cjs scripts/test-prompt-block-id-naming.cjs scripts/test-block-id-prompt-prefill.cjs scripts/test-vim-surround.cjs scripts/test-navigation-dependencies-stage-ranker-and-pool.cjs scripts/test-navigation-dependencies-stage-entry-and-view.cjs scripts/test-navigation-dependencies-stage-writes.cjs scripts/test-navigation-dependencies-stage-mirror-and-badge.cjs scripts/test-navigation-dependencies-stage-stale-guards.cjs scripts/test-navigation-dependencies-stage-performance.cjs scripts/test-navigation-prompt-block-id-stage.cjs scripts/test-navigation-dependencies-writer.cjs scripts/test-navigation-dependency-link-consumption.cjs scripts/test-plugin-build.cjs scripts/test-ledger-tools-stats-journal.cjs scripts/test-ledger-tools-stats-data.cjs scripts/test-ledger-tools-stats-block.cjs scripts/test-ledger-tools-stats-charts.cjs scripts/test-navigation-review-journal.cjs scripts/test-ledger-tools-stats-panels.cjs scripts/test-ledger-tools-reading-board-data.cjs scripts/test-ledger-tools-reading-board-models.cjs scripts/test-ledger-tools-reading-board-block.cjs scripts/test-ledger-tools-pomodoro-home-chips.cjs scripts/test-navigation-image-zoom-target.cjs scripts/test-navigation-image-zoom-command.cjs scripts/test-docs-inventory.mjs scripts/test-docs-check.mjs scripts/test-navigation-relation-lines.cjs scripts/test-navigation-relation-writer.cjs scripts/test-navigation-relation-links-stage.cjs scripts/test-relation-index-linked-from-stage.cjs scripts/test-ledger-tools-relations.cjs scripts/test-ledger-tools-relation-index.cjs scripts/test-ledger-tools-relation-chips.cjs scripts/test-task-status-cycler-relations.cjs scripts/test-block-id-prompt-relations.cjs

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
  duration_ms: 1.176406
  ...
# Subtest: bip BK13–BK15 malformed split mirrors the Depends-On twin
ok 2 - bip BK13–BK15 malformed split mirrors the Depends-On twin
  ---
  duration_ms: 0.368434
  ...
# Subtest: bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
ok 3 - bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
  ---
  duration_ms: 0.112294
  ...
# Subtest: bip MC1/MC2 Pomodoro scanners skip managed lines
ok 4 - bip MC1/MC2 Pomodoro scanners skip managed lines
  ---
  duration_ms: 1.098557
  ...
# Subtest: explicit task IDs exclusively own dependency lookup
ok 5 - explicit task IDs exclusively own dependency lookup
  ---
  duration_ms: 2.487689
  ...
# Subtest: legacy tasks without an id field still fall back to their block ID
ok 6 - legacy tasks without an id field still fall back to their block ID
  ---
  duration_ms: 0.295524
  ...
# Subtest: blocked-link consumption raises open prerequisites and leaves the dependent blocked
ok 7 - blocked-link consumption raises open prerequisites and leaves the dependent blocked
  ---
  duration_ms: 1.081284
  ...
# Subtest: project-blocked member consumption promotes the project's open prerequisite
ok 8 - project-blocked member consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.653488
  ...
# Subtest: project-blocked resident consumption promotes the project's open prerequisite
ok 9 - project-blocked resident consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.391317
  ...
# Subtest: a tagged inherited ^prj target is refused with its parent named
ok 10 - a tagged inherited ^prj target is refused with its parent named
  ---
  duration_ms: 0.359055
  ...
# Subtest: project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
ok 11 - project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
  ---
  duration_ms: 1.572131
  ...
# Subtest: project date refusal applies only when the date is the sole project reason
ok 12 - project date refusal applies only when the date is the sole project reason
  ---
  duration_ms: 0.259345
  ...
# Subtest: a project-blocked tag is token-bounded and ignored on lookalike tags
ok 13 - a project-blocked tag is token-bounded and ignored on lookalike tags
  ---
  duration_ms: 0.361409
  ...
# Subtest: task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
ok 14 - task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
  ---
  duration_ms: 0.63926
  ...
# Subtest: task blocked state unifies status and dependency reasons
ok 15 - task blocked state unifies status and dependency reasons
  ---
  duration_ms: 0.325582
  ...
# Subtest: task picker partition sinks blocked tasks while preserving group order
ok 16 - task picker partition sinks blocked tasks while preserving group order
  ---
  duration_ms: 0.187879
  ...
# Subtest: blocked chip labels show useful unmet dependency counts
ok 17 - blocked chip labels show useful unmet dependency counts
  ---
  duration_ms: 0.101764
  ...
# Subtest: blocked tooltips explain dependency and status-only reasons
ok 18 - blocked tooltips explain dependency and status-only reasons
  ---
  duration_ms: 0.202196
  ...
# Subtest: task status classes cover every open task status
ok 19 - task status classes cover every open task status
  ---
  duration_ms: 0.07855
  ...
# Subtest: Blocked tasks remain unmet dependency targets
ok 20 - Blocked tasks remain unmet dependency targets
  ---
  duration_ms: 0.121371
  ...
# Subtest: blocked task count covers both reasons without double-counting
ok 21 - blocked task count covers both reasons without double-counting
  ---
  duration_ms: 0.113106
  ...
# Subtest: single caret relocation preserves embedding and removes aliases
ok 22 - single caret relocation preserves embedding and removes aliases
  ---
  duration_ms: 1.470938
  ...
# Subtest: single caret relocation resets aliased block links
ok 23 - single caret relocation resets aliased block links
  ---
  duration_ms: 0.232023
  ...
# Subtest: single caret relocation strips heading and block subpaths
ok 24 - single caret relocation strips heading and block subpaths
  ---
  duration_ms: 0.249747
  ...
# Subtest: task picker normalizes every supported wiki block-link form
ok 25 - task picker normalizes every supported wiki block-link form
  ---
  duration_ms: 0.644751
  ...
# Subtest: three or more carets never trigger the task picker
ok 26 - three or more carets never trigger the task picker
  ---
  duration_ms: 0.145077
  ...
# Subtest: rapid aliased task picker completion preserves the alias
ok 27 - rapid aliased task picker completion preserves the alias
  ---
  duration_ms: 2.34172
  ...
# Subtest: task picker recognition is independent of Markdown source context
ok 28 - task picker recognition is independent of Markdown source context
  ---
  duration_ms: 0.731987
  ...
# Subtest: task picker recognition respects cursor proximity and fenced code
ok 29 - task picker recognition respects cursor proximity and fenced code
  ---
  duration_ms: 0.235069
  ...
# Subtest: plan budget suffix: link Notice appends the meter computed on post-write daily content
ok 30 - plan budget suffix: link Notice appends the meter computed on post-write daily content
  ---
  duration_ms: 7.027064
  ...
# Subtest: plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
ok 31 - plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
  ---
  duration_ms: 1.821497
  ...
# Subtest: plan budget suffix: unlink Notice marks an over-cap plan with 🔴
ok 32 - plan budget suffix: unlink Notice marks an over-cap plan with 🔴
  ---
  duration_ms: 1.827459
  ...
# Subtest: plan budget suffix: Next task without a block ID prompts for one and omits the meter
ok 33 - plan budget suffix: Next task without a block ID prompts for one and omits the meter
  ---
  duration_ms: 0.362141
  ...
# Subtest: plan budget suffix: Task Link Notice appends the meter from post-write daily content
ok 34 - plan budget suffix: Task Link Notice appends the meter from post-write daily content
  ---
  duration_ms: 2.11149
  ...
# Subtest: plan budget suffix: Task Link Notice omits the meter when no daily note takes part
ok 35 - plan budget suffix: Task Link Notice omits the meter when no daily note takes part
  ---
  duration_ms: 0.524421
  ...
# Subtest: planTargetTaskUpdate stamps the rewritten line last via injected stamper
ok 36 - planTargetTaskUpdate stamps the rewritten line last via injected stamper
  ---
  duration_ms: 0.252953
  ...
# Subtest: planTargetTaskUpdate without a stamper never stamps (identity default)
ok 37 - planTargetTaskUpdate without a stamper never stamps (identity default)
  ---
  duration_ms: 0.129597
  ...
# Subtest: planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
ok 38 - planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
  ---
  duration_ms: 0.353344
  ...
# Subtest: planTargetTaskUpdate stamps a Next task that gains a block ID
ok 39 - planTargetTaskUpdate stamps a Next task that gains a block ID
  ---
  duration_ms: 0.447033
  ...
# Subtest: planTargetTaskUpdate tolerates a throwing stamper
ok 40 - planTargetTaskUpdate tolerates a throwing stamper
  ---
  duration_ms: 0.225601
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 41 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.412658
  ...
# Subtest: dedicated-link helpers reject Depends-On lines
ok 42 - dedicated-link helpers reject Depends-On lines
  ---
  duration_ms: 0.339207
  ...
# Subtest: Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
ok 43 - Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
  ---
  duration_ms: 0.338376
  ...
# Subtest: malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
ok 44 - malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
  ---
  duration_ms: 0.106323
  ...
# Subtest: Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
ok 45 - Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
  ---
  duration_ms: 0.247783
  ...
# Subtest: Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
ok 46 - Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
  ---
  duration_ms: 0.197807
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent
ok 47 - readPlanBudgetMeter keeps per-cap over flags independent
  ---
  duration_ms: 0.196706
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent (mirror)
ok 48 - readPlanBudgetMeter keeps per-cap over flags independent (mirror)
  ---
  duration_ms: 0.09426
  ...
# Subtest: block-id-prompt freshness accessors degrade without ledger-tools
ok 49 - block-id-prompt freshness accessors degrade without ledger-tools
  ---
  duration_ms: 0.205042
  ...
# Subtest: list item body bounds trim whitespace and reject empty bullets
ok 50 - list item body bounds trim whitespace and reject empty bullets
  ---
  duration_ms: 1.302777
  ...
# Subtest: Pomodoro activation eligibility requires a sole-content sub-bullet
ok 51 - Pomodoro activation eligibility requires a sole-content sub-bullet
  ---
  duration_ms: 1.888735
  ...
# Subtest: Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
ok 52 - Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
  ---
  duration_ms: 0.527707
  ...
# Subtest: Pomodoro source context distinguishes ledger ancestry and open state
ok 53 - Pomodoro source context distinguishes ledger ancestry and open state
  ---
  duration_ms: 0.45028
  ...
# Subtest: future cleanup touches only later open Pomodoros and counts duplicates
ok 54 - future cleanup touches only later open Pomodoros and counts duplicates
  ---
  duration_ms: 2.208947
  ...
# Subtest: cleanup resolves aliases, embeds, same-note links, and alternate paths
ok 55 - cleanup resolves aliases, embeds, same-note links, and alternate paths
  ---
  duration_ms: 1.370787
  ...
# Subtest: dedicated bullet subtree cleanup preserves CRLF line endings
ok 56 - dedicated bullet subtree cleanup preserves CRLF line endings
  ---
  duration_ms: 0.358936
  ...
# Subtest: existing-ID task completion prunes future links in the source editor
ok 57 - existing-ID task completion prunes future links in the source editor
  ---
  duration_ms: 2.301674
  ...
# Subtest: new-ID same-file completion plans cleanup after the task edit
ok 58 - new-ID same-file completion plans cleanup after the task edit
  ---
  duration_ms: 1.322034
  ...
# Subtest: findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
ok 59 - findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
  ---
  duration_ms: 2.187967
  ...
# Subtest: findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
ok 60 - findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
  ---
  duration_ms: 0.185765
  ...
# Subtest: findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
ok 61 - findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
  ---
  duration_ms: 0.193579
  ...
# Subtest: todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
ok 62 - todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
  ---
  duration_ms: 0.607219
  ...
# Subtest: todayDailyPath honors a custom Daily Notes format and an empty folder
ok 63 - todayDailyPath honors a custom Daily Notes format and an empty folder
  ---
  duration_ms: 1.235098
  ...
# Subtest: formatDailyDate resolves bracketed literal text alongside date tokens
ok 64 - formatDailyDate resolves bracketed literal text alongside date tokens
  ---
  duration_ms: 0.130079
  ...
# Subtest: getDailyNotesOptions reads the daily-notes core plugin's configured options
ok 65 - getDailyNotesOptions reads the daily-notes core plugin's configured options
  ---
  duration_ms: 0.658797
  ...
# Subtest: computeFencedLineFlags marks opening and closing fence lines and everything between
ok 66 - computeFencedLineFlags marks opening and closing fence lines and everything between
  ---
  duration_ms: 0.261389
  ...
# Subtest: selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
ok 67 - selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
  ---
  duration_ms: 0.766052
  ...
# Subtest: selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
ok 68 - selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
  ---
  duration_ms: 0.459628
  ...
# Subtest: selectPomodoroInsertionTarget rejects more than one open timed entry
ok 69 - selectPomodoroInsertionTarget rejects more than one open timed entry
  ---
  duration_ms: 0.198889
  ...
# Subtest: selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
ok 70 - selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
  ---
  duration_ms: 0.18818
  ...
# Subtest: findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
ok 71 - findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
  ---
  duration_ms: 0.168872
  ...
# Subtest: planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
ok 72 - planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
  ---
  duration_ms: 1.305121
  ...
# Subtest: planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
ok 73 - planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
  ---
  duration_ms: 2.05889
  ...
# Subtest: planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
ok 74 - planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
  ---
  duration_ms: 0.309421
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
ok 75 - planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
  ---
  duration_ms: 0.701459
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
ok 76 - planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
  ---
  duration_ms: 0.631224
  ...
# Subtest: planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
ok 77 - planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
  ---
  duration_ms: 0.394513
  ...
# Subtest: planPomodoroLinkInsertion inserts before the separator preceding later content
ok 78 - planPomodoroLinkInsertion inserts before the separator preceding later content
  ---
  duration_ms: 0.340029
  ...
# Subtest: planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
ok 79 - planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
  ---
  duration_ms: 0.375798
  ...
# Subtest: planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
ok 80 - planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
  ---
  duration_ms: 0.470217
  ...
# Subtest: existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
ok 81 - existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
  ---
  duration_ms: 3.919122
  ...
# Subtest: same-note Pomodoro link runtime composes the task update with adjacent insertion
ok 82 - same-note Pomodoro link runtime composes the task update with adjacent insertion
  ---
  duration_ms: 1.22043
  ...
# Subtest: new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
ok 83 - new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
  ---
  duration_ms: 0.606808
  ...
# Subtest: planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
ok 84 - planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
  ---
  duration_ms: 0.311706
  ...
# Subtest: all-open cleanup removes current and future links while preserving history and unresolved links
ok 85 - all-open cleanup removes current and future links while preserving history and unresolved links
  ---
  duration_ms: 0.908654
  ...
# Subtest: all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
ok 86 - all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
  ---
  duration_ms: 1.127192
  ...
# Subtest: all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
ok 87 - all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
  ---
  duration_ms: 0.265296
  ...
# Subtest: all-open cleanup treats missing section, no open entries, and no matches as no-op successes
ok 88 - all-open cleanup treats missing section, no open entries, and no matches as no-op successes
  ---
  duration_ms: 0.233195
  ...
# Subtest: composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
ok 89 - composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
  ---
  duration_ms: 0.346211
  ...
# Subtest: pomodoro link picker choices normalize to existing/new or null
ok 90 - pomodoro link picker choices normalize to existing/new or null
  ---
  duration_ms: 1.180163
  ...
# Subtest: pomodoroLinkPicker api never rejects and validates choices
ok 91 - pomodoroLinkPicker api never rejects and validates choices
  ---
  duration_ms: 0.355249
  ...
# Subtest: destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
ok 92 - destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
  ---
  duration_ms: 0.699837
  ...
# Subtest: destination pick with a section releases its guards when the modal cannot open
ok 93 - destination pick with a section releases its guards when the modal cannot open
  ---
  duration_ms: 1.528198
  ...
# Subtest: plugin lifecycle installs the api and drops it on unload
ok 94 - plugin lifecycle installs the api and drops it on unload
  ---
  duration_ms: 0.294913
  ...
# Subtest: Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
ok 95 - Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
  ---
  duration_ms: 2.609431
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor requires a single cursor
ok 96 - resolvePomodoroLinkTaskFromEditor requires a single cursor
  ---
  duration_ms: 0.325602
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
ok 97 - resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
  ---
  duration_ms: 0.369806
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
ok 98 - resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
  ---
  duration_ms: 0.398571
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
ok 99 - resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
  ---
  duration_ms: 0.479666
  ...
# Subtest: blocked-link consumption reports dependency reasons before the project date
ok 100 - blocked-link consumption reports dependency reasons before the project date
  ---
  duration_ms: 2.280363
  ...
# Subtest: Pomodoro link checks do not read other notes for a non-Blocked task
ok 101 - Pomodoro link checks do not read other notes for a non-Blocked task
  ---
  duration_ms: 0.276298
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
ok 102 - resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
  ---
  duration_ms: 0.336241
  ...
# Subtest: task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
ok 103 - task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
  ---
  duration_ms: 5.587005
  ...
# Subtest: task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
ok 104 - task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
  ---
  duration_ms: 1.746444
  ...
# Subtest: task-mode toggle: linked only under a completed Pomodoro links again
ok 105 - task-mode toggle: linked only under a completed Pomodoro links again
  ---
  duration_ms: 0.774508
  ...
# Subtest: task-mode toggle: a task without a block ID is never linked and prompts for one
ok 106 - task-mode toggle: a task without a block ID is never linked and prompts for one
  ---
  duration_ms: 0.383271
  ...
# Subtest: existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
ok 107 - existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
  ---
  duration_ms: 1.017902
  ...
# Subtest: forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
ok 108 - forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
  ---
  duration_ms: 0.501638
  ...
# Subtest: new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
ok 109 - new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
  ---
  duration_ms: 0.496027
  ...
# Subtest: submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
ok 110 - submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
  ---
  duration_ms: 0.13591
  ...
# Subtest: submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
ok 111 - submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
  ---
  duration_ms: 0.180725
  ...
# Subtest: same-note Pomodoro link runtime: task and ledger edits merge into one transaction
ok 112 - same-note Pomodoro link runtime: task and ledger edits merge into one transaction
  ---
  duration_ms: 1.111583
  ...
# Subtest: linking an already-linked Ready task raises it to Next without duplicating the link
ok 113 - linking an already-linked Ready task raises it to Next without duplicating the link
  ---
  duration_ms: 0.461622
  ...
# Subtest: Next task without a block ID preflights the picker before prompting
ok 114 - Next task without a block ID preflights the picker before prompting
  ---
  duration_ms: 0.433308
  ...
# Subtest: Pomodoro link stops before any mutation when today's daily note is missing
ok 115 - Pomodoro link stops before any mutation when today's daily note is missing
  ---
  duration_ms: 0.163021
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
ok 116 - Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
  ---
  duration_ms: 0.427957
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
ok 117 - Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
  ---
  duration_ms: 0.263413
  ...
# Subtest: Pomodoro link aborts without any write when the task line changed since it was selected
ok 118 - Pomodoro link aborts without any write when the task line changed since it was selected
  ---
  duration_ms: 0.150708
  ...
# Subtest: Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
ok 119 - Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
  ---
  duration_ms: 0.574527
  ...
# Subtest: canceling the Pomodoro block-ID modal leaves the note untouched
ok 120 - canceling the Pomodoro block-ID modal leaves the note untouched
  ---
  duration_ms: 0.147612
  ...
# Subtest: review-walk: existing-ID link hands its Linked notice to continue with no separate notice
ok 121 - review-walk: existing-ID link hands its Linked notice to continue with no separate notice
  ---
  duration_ms: 0.725655
  ...
# Subtest: review-walk: prompted-ID link continues after submit
ok 122 - review-walk: prompted-ID link continues after submit
  ---
  duration_ms: 0.868077
  ...
# Subtest: review-walk: prompt cancel settles with null
ok 123 - review-walk: prompt cancel settles with null
  ---
  duration_ms: 0.13605
  ...
# Subtest: review-walk: BUSY swallows the key with no write
ok 124 - review-walk: BUSY swallows the key with no write
  ---
  duration_ms: 0.23059
  ...
# Subtest: review-walk: failed link keeps its notice and settles with null
ok 125 - review-walk: failed link keeps its notice and settles with null
  ---
  duration_ms: 0.172499
  ...
# Subtest: review-walk: partial link keeps its notice and never continues with an outcome
ok 126 - review-walk: partial link keeps its notice and never continues with an outcome
  ---
  duration_ms: 0.694355
  ...
# Subtest: inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
ok 127 - inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
  ---
  duration_ms: 0.199922
  ...
# Subtest: inbox-route: non-inbox notes and task-link mode never prompt
ok 128 - inbox-route: non-inbox notes and task-link mode never prompt
  ---
  duration_ms: 0.584296
  ...
# Subtest: inbox-route: cancel writes nothing and settles once
ok 129 - inbox-route: cancel writes nothing and settles once
  ---
  duration_ms: 0.438277
  ...
# Subtest: inbox-route: stay matches today
ok 130 - inbox-route: stay matches today
  ---
  duration_ms: 1.311744
  ...
# Subtest: inbox-route: move links, then moves, with one composed toast and a route continue
ok 131 - inbox-route: move links, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.538527
  ...
# Subtest: inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
ok 132 - inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
  ---
  duration_ms: 0.621917
  ...
# Subtest: inbox-route: a move failure gives the partial notice plus a link-today continue
ok 133 - inbox-route: a move failure gives the partial notice plus a link-today continue
  ---
  duration_ms: 0.414741
  ...
# Subtest: review-walk: no nav or nav v2 keeps today's notices
ok 134 - review-walk: no nav or nav v2 keeps today's notices
  ---
  duration_ms: 0.844552
  ...
# Subtest: inbox-route: source drift during route prompt refuses without writes
ok 135 - inbox-route: source drift during route prompt refuses without writes
  ---
  duration_ms: 0.308819
  ...
# Subtest: inbox-route: block-ID route cancel returns sentinel and settles null once
ok 136 - inbox-route: block-ID route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.302057
  ...
# Subtest: inbox-route: link no-op with move never commits
ok 137 - inbox-route: link no-op with move never commits
  ---
  duration_ms: 0.169664
  ...
# Subtest: picker opens only on the link direction, never on unlink
ok 138 - picker opens only on the link direction, never on unlink
  ---
  duration_ms: 8.726879
  ...
# Subtest: picker never opens in task-link mode
ok 139 - picker never opens in task-link mode
  ---
  duration_ms: 3.544286
  ...
# Subtest: Depends-On refusals never open the picker
ok 140 - Depends-On refusals never open the picker
  ---
  duration_ms: 0.896962
  ...
# Subtest: preflight refusals open nothing
ok 141 - preflight refusals open nothing
  ---
  duration_ms: 0.51288
  ...
# Subtest: picking a non-default entry links there
ok 142 - picking a non-default entry links there
  ---
  duration_ms: 1.108997
  ...
# Subtest: cancel writes nothing with no Notice and settles the walk null
ok 143 - cancel writes nothing with no Notice and settles the walk null
  ---
  duration_ms: 0.639681
  ...
# Subtest: a no-ID task gets picker, then the block-ID prompt with the target carried
ok 144 - a no-ID task gets picker, then the block-ID prompt with the target carried
  ---
  duration_ms: 0.842128
  ...
# Subtest: inbox order is picker, then route, then write
ok 145 - inbox order is picker, then route, then write
  ---
  duration_ms: 0.698263
  ...
# Subtest: a review-walk landing continues with link-today and the new text
ok 146 - a review-walk landing continues with link-today and the new text
  ---
  duration_ms: 0.855462
  ...
# Subtest: an all-closed ledger creates a new entry after the last completed block
ok 147 - an all-closed ledger creates a new entry after the last completed block
  ---
  duration_ms: 1.652144
  ...
# Subtest: several running entries allow an explicit pick
ok 148 - several running entries allow an explicit pick
  ---
  duration_ms: 0.698664
  ...
# Subtest: a target that changed before commit refuses with no writes
ok 149 - a target that changed before commit refuses with no writes
  ---
  duration_ms: 0.443426
  ...
# Subtest: a target that closed before commit refuses with no writes
ok 150 - a target that closed before commit refuses with no writes
  ---
  duration_ms: 0.355037
  ...
# Subtest: the task note being the daily note uses one editor transaction
ok 151 - the task note being the daily note uses one editor transaction
  ---
  duration_ms: 0.587722
  ...
# Subtest: promptOpen blocks re-entry while the picker is open
ok 152 - promptOpen blocks re-entry while the picker is open
  ---
  duration_ms: 9.636807
  ...
# Subtest: header shows title, subtitle, lane chip per status, and block-ID chip
ok 153 - header shows title, subtitle, lane chip per status, and block-ID chip
  ---
  duration_ms: 7.61598
  ...
# Subtest: rows render in document order with the default selected
ok 154 - rows render in document order with the default selected
  ---
  duration_ms: 0.954633
  ...
# Subtest: running row shows progress fraction and minutes-left meta
ok 155 - running row shows progress fraction and minutes-left meta
  ---
  duration_ms: 0.835455
  ...
# Subtest: unnamed entries render muted italic
ok 156 - unnamed entries render muted italic
  ---
  duration_ms: 0.407949
  ...
# Subtest: filtering ranks, highlights, and clearing restores the default
ok 157 - filtering ranks, highlights, and clearing restores the default
  ---
  duration_ms: 1.086063
  ...
# Subtest: create row meta, divider, and theme badge
ok 158 - create row meta, divider, and theme badge
  ---
  duration_ms: 1.444747
  ...
# Subtest: exact open names suppress the create row; prefix matches keep it
ok 159 - exact open names suppress the create row; prefix matches keep it
  ---
  duration_ms: 0.622428
  ...
# Subtest: theme badge turns red over cap; a throwing budget hides the detail
ok 160 - theme badge turns red over cap; a throwing budget hides the detail
  ---
  duration_ms: 1.761162
  ...
# Subtest: invalid rows explain the grammar and are inert on Enter
ok 161 - invalid rows explain the grammar and are inert on Enter
  ---
  duration_ms: 11.651141
  ...
# Subtest: multiple running entries show the banner, no pills, and block creation
ok 162 - multiple running entries show the banner, no pills, and block creation
  ---
  duration_ms: 1.890298
  ...
# Subtest: navigation wraps and skips non-selectable rows
ok 163 - navigation wraps and skips non-selectable rows
  ---
  duration_ms: 1.557053
  ...
# Subtest: empty state invites planning a Pomodoro
ok 164 - empty state invites planning a Pomodoro
  ---
  duration_ms: 0.339628
  ...
# Subtest: footer hints and plan meter
ok 165 - footer hints and plan meter
  ---
  duration_ms: 1.247892
  ...
# Subtest: Enter chooses the selected row; click chooses that row
ok 166 - Enter chooses the selected row; click chooses that row
  ---
  duration_ms: 0.863518
  ...
# Subtest: Shift+Enter creates; an exact open name links there instead
ok 167 - Shift+Enter creates; an exact open name links there instead
  ---
  duration_ms: 0.984099
  ...
# Subtest: Ctrl+Shift+Enter commits exactly like Enter
ok 168 - Ctrl+Shift+Enter commits exactly like Enter
  ---
  duration_ms: 2.060374
  ...
# Subtest: Escape and Ctrl+[ cancel with no choice; settle-once holds
ok 169 - Escape and Ctrl+[ cancel with no choice; settle-once holds
  ---
  duration_ms: 1.058651
  ...
# Subtest: canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
ok 170 - canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
  ---
  duration_ms: 1.709683
  ...
# Subtest: canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
ok 171 - canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
  ---
  duration_ms: 0.280986
  ...
# Subtest: pomodoroLinkSelectorSlug mirrors capture slugs
ok 172 - pomodoroLinkSelectorSlug mirrors capture slugs
  ---
  duration_ms: 0.238325
  ...
# Subtest: parsePomodoroEntryParts reads canonical and legacy entry lines
ok 173 - parsePomodoroEntryParts reads canonical and legacy entry lines
  ---
  duration_ms: 1.822619
  ...
# Subtest: collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
ok 174 - collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
  ---
  duration_ms: 1.532897
  ...
# Subtest: collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
ok 175 - collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
  ---
  duration_ms: 0.969181
  ...
# Subtest: collectPomodoroLinkEntries counts links but excludes struck references
ok 176 - collectPomodoroLinkEntries counts links but excludes struck references
  ---
  duration_ms: 0.439419
  ...
# Subtest: collectPomodoroLinkEntries falls back to range text and position titles
ok 177 - collectPomodoroLinkEntries falls back to range text and position titles
  ---
  duration_ms: 0.275717
  ...
# Subtest: pomodoroRunProgress reports fractions, overtime, and midnight wrap
ok 178 - pomodoroRunProgress reports fractions, overtime, and midnight wrap
  ---
  duration_ms: 1.315281
  ...
# Subtest: buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
ok 179 - buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
  ---
  duration_ms: 0.73862
  ...
# Subtest: buildPomodoroLinkPickerRows keeps the create row for prefix matches
ok 180 - buildPomodoroLinkPickerRows keeps the create row for prefix matches
  ---
  duration_ms: 0.276899
  ...
# Subtest: buildPomodoroLinkPickerRows marks completed-only names as again
ok 181 - buildPomodoroLinkPickerRows marks completed-only names as again
  ---
  duration_ms: 0.166928
  ...
# Subtest: buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
ok 182 - buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
  ---
  duration_ms: 0.367311
  ...
# Subtest: buildPomodoroLinkPickerRows matches times, positions, and block IDs
ok 183 - buildPomodoroLinkPickerRows matches times, positions, and block IDs
  ---
  duration_ms: 0.440632
  ...
# Subtest: resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
ok 184 - resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
  ---
  duration_ms: 0.275206
  ...
# Subtest: defaultPomodoroLinkChoice returns the default entry or null
ok 185 - defaultPomodoroLinkChoice returns the default entry or null
  ---
  duration_ms: 0.171738
  ...
# Subtest: planExplicitPomodoroLinkInsertion links under a chosen existing entry
ok 186 - planExplicitPomodoroLinkInsertion links under a chosen existing entry
  ---
  duration_ms: 0.906771
  ...
# Subtest: planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
ok 187 - planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
  ---
  duration_ms: 0.274023
  ...
# Subtest: planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
ok 188 - planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
  ---
  duration_ms: 1.064893
  ...
# Subtest: planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
ok 189 - planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
  ---
  duration_ms: 0.35607
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after the running entry
ok 190 - planExplicitPomodoroLinkInsertion creates after the running entry
  ---
  duration_ms: 0.58126
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
ok 191 - planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
  ---
  duration_ms: 0.662053
  ...
# Subtest: planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
ok 192 - planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
  ---
  duration_ms: 0.24612
  ...
# Subtest: planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
ok 193 - planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
  ---
  duration_ms: 0.270146
  ...
# Subtest: planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
ok 194 - planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
  ---
  duration_ms: 0.3771
  ...
# Subtest: buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
ok 195 - buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
  ---
  duration_ms: 0.201514
  ...
# Subtest: buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
ok 196 - buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
  ---
  duration_ms: 0.166168
  ...
# Subtest: planExplicitPomodoroLinkInsertion matches mixed-case raced open names
ok 197 - planExplicitPomodoroLinkInsertion matches mixed-case raced open names
  ---
  duration_ms: 0.185905
  ...
# Subtest: buildPomodoroLinkPickerRows bounds \#N position matches
ok 198 - buildPomodoroLinkPickerRows bounds \#N position matches
  ---
  duration_ms: 0.348866
  ...
# Subtest: planPomodoroLinkInsertion without a target keeps today's behavior and shape
ok 199 - planPomodoroLinkInsertion without a target keeps today's behavior and shape
  ---
  duration_ms: 0.404362
  ...
# Subtest: direct unlink without a daily note keeps the Next lane and reports it
ok 200 - direct unlink without a daily note keeps the Next lane and reports it
  ---
  duration_ms: 2.190401
  ...
# Subtest: In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
ok 201 - In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
  ---
  duration_ms: 0.424991
  ...
# Subtest: In Progress unlink with a summary keeps the lane and creates a Work Log
ok 202 - In Progress unlink with a summary keeps the lane and creates a Work Log
  ---
  duration_ms: 1.176185
  ...
# Subtest: In Progress unlink revalidates task text and block-ID uniqueness at confirmation
ok 203 - In Progress unlink revalidates task text and block-ID uniqueness at confirmation
  ---
  duration_ms: 0.940145
  ...
# Subtest: Next task unlink removes current and future links and keeps the Next lane
ok 204 - Next task unlink removes current and future links and keeps the Next lane
  ---
  duration_ms: 3.339475
  ...
# Subtest: In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
ok 205 - In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
  ---
  duration_ms: 0.669579
  ...
# Subtest: same-note Next unlink merges the Work Log and all-open cleanup in the active editor
ok 206 - same-note Next unlink merges the Work Log and all-open cleanup in the active editor
  ---
  duration_ms: 0.753559
  ...
# Subtest: same-note In Progress unlink merges cleanup and Work Log in the active editor
ok 207 - same-note In Progress unlink merges cleanup and Work Log in the active editor
  ---
  duration_ms: 0.513039
  ...
# Subtest: Next unlink stops before any write when daily cleanup write is stale
ok 208 - Next unlink stops before any write when daily cleanup write is stale
  ---
  duration_ms: 0.716789
  ...
# Subtest: Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
ok 209 - Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
  ---
  duration_ms: 0.879709
  ...
# Subtest: In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
ok 210 - In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
  ---
  duration_ms: 0.589566
  ...
# Subtest: review-walk: unlink settles with null and keeps its notice
ok 211 - review-walk: unlink settles with null and keeps its notice
  ---
  duration_ms: 1.109398
  ...
# Subtest: inbox-route: unlink cancel writes nothing
ok 212 - inbox-route: unlink cancel writes nothing
  ---
  duration_ms: 0.305643
  ...
# Subtest: inbox-route: unlink stay matches today and never commits
ok 213 - inbox-route: unlink stay matches today and never commits
  ---
  duration_ms: 0.489294
  ...
# Subtest: inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
ok 214 - inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.534169
  ...
# Subtest: inbox-route: In Progress unlink with a Work summary routes
ok 215 - inbox-route: In Progress unlink with a Work summary routes
  ---
  duration_ms: 0.620064
  ...
# Subtest: inbox-route: unlink move failure gives the partial notice and stays
ok 216 - inbox-route: unlink move failure gives the partial notice and stays
  ---
  duration_ms: 0.272881
  ...
# Subtest: inbox-route: non-inbox unlink never prompts
ok 217 - inbox-route: non-inbox unlink never prompts
  ---
  duration_ms: 0.274204
  ...
# Subtest: review-walk: Work-summary unlink path retains origin until submit
ok 218 - review-walk: Work-summary unlink path retains origin until submit
  ---
  duration_ms: 0.27744
  ...
# Subtest: inbox-route: unlink source drift during route prompt refuses without writes
ok 219 - inbox-route: unlink source drift during route prompt refuses without writes
  ---
  duration_ms: 0.213708
  ...
# Subtest: inbox-route: Work-summary route cancel returns sentinel and settles null once
ok 220 - inbox-route: Work-summary route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.23554
  ...
# Subtest: inbox-route: unlink no-op with move never commits
ok 221 - inbox-route: unlink no-op with move never commits
  ---
  duration_ms: 0.197968
  ...
# Subtest: same-note unlink maps a task below removed entries through Work-summary inserts
ok 222 - same-note unlink maps a task below removed entries through Work-summary inserts
  ---
  duration_ms: 0.491118
  ...
# Subtest: direct-add seeds from the task headline, not non-task blocks
ok 223 - direct-add seeds from the task headline, not non-task blocks
  ---
  duration_ms: 3.00694
  ...
# Subtest: link-task-complete seeds from the target, prefers open buffers
ok 224 - link-task-complete seeds from the target, prefers open buffers
  ---
  duration_ms: 0.88027
  ...
# Subtest: link-task-complete reports stale and unreadable targets
ok 225 - link-task-complete reports stale and unreadable targets
  ---
  duration_ms: 0.288831
  ...
# Subtest: pomodoro link seeds after the choice from the cursor task
ok 226 - pomodoro link seeds after the choice from the cursor task
  ---
  duration_ms: 0.265477
  ...
# Subtest: marker rename suggests from the unique task, never hiding ambiguity
ok 227 - marker rename suggests from the unique task, never hiding ambiguity
  ---
  duration_ms: 0.538387
  ...
# Subtest: modal seeds the value, selects once, and never overwrites typing
ok 228 - modal seeds the value, selects once, and never overwrites typing
  ---
  duration_ms: 1.152439
  ...
# Subtest: modal disables Save while loading and survives close/reopen
ok 229 - modal disables Save while loading and survives close/reopen
  ---
  duration_ms: 1.818321
  ...
# Subtest: submit revalidates: occupied IDs and stale tasks fail editable
ok 230 - submit revalidates: occupied IDs and stale tasks fail editable
  ---
  duration_ms: 0.473254
  ...
# Subtest: cancelling writes no ID and explicit renames keep the current ID
ok 231 - cancelling writes no ID and explicit renames keep the current ID
  ---
  duration_ms: 0.638789
  ...
# Subtest: the task picker drops the paired \#ref and prefixes the book
ok 232 - the task picker drops the paired \#ref and prefixes the book
  ---
  duration_ms: 2.492347
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 233 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.31945
  ...
# Subtest: block-id-prompt LK1–LK19 recognises only relation line shapes
ok 234 - block-id-prompt LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 1.763596
  ...
# Subtest: block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
ok 235 - block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
  ---
  duration_ms: 1.444888
  ...
# Subtest: block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
ok 236 - block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
  ---
  duration_ms: 1.819634
  ...
# Subtest: calendar date parsing rejects malformed width and impossible dates
ok 237 - calendar date parsing rejects malformed width and impossible dates
  ---
  duration_ms: 1.560458
  ...
# Subtest: future scheduled field detection respects the yesterday/today/tomorrow boundary
ok 238 - future scheduled field detection respects the yesterday/today/tomorrow boundary
  ---
  duration_ms: 1.241429
  ...
# Subtest: scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
ok 239 - scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
  ---
  duration_ms: 0.176958
  ...
# Subtest: planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
ok 240 - planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
  ---
  duration_ms: 0.972256
  ...
# Subtest: planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
ok 241 - planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
  ---
  duration_ms: 0.205462
  ...
# Subtest: planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
ok 242 - planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
  ---
  duration_ms: 0.16256
  ...
# Subtest: planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
ok 243 - planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
  ---
  duration_ms: 0.153503
  ...
# Subtest: planTargetTaskUpdate leaves today and past schedules untouched
ok 244 - planTargetTaskUpdate leaves today and past schedules untouched
  ---
  duration_ms: 0.263934
  ...
# Subtest: planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
ok 245 - planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
  ---
  duration_ms: 0.333587
  ...
# Subtest: two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
ok 246 - two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
  ---
  duration_ms: 0.44498
  ...
# Subtest: a malformed single scheduled field is never treated as future
ok 247 - a malformed single scheduled field is never treated as future
  ---
  duration_ms: 0.166978
  ...
# Subtest: an ambiguous scheduled field does not block the legacy Ready promotion
ok 248 - an ambiguous scheduled field does not block the legacy Ready promotion
  ---
  duration_ms: 0.164925
  ...
# Subtest: planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
ok 249 - planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
  ---
  duration_ms: 0.117654
  ...
# Subtest: Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
ok 250 - Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
  ---
  duration_ms: 0.453205
  ...
# Subtest: Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
ok 251 - Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
  ---
  duration_ms: 0.160747
  ...
# Subtest: planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
ok 252 - planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
  ---
  duration_ms: 0.253263
  ...
# Subtest: planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
ok 253 - planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
  ---
  duration_ms: 0.126542
  ...
# Subtest: planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
ok 254 - planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.108076
  ...
# Subtest: planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
ok 255 - planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
  ---
  duration_ms: 0.122223
  ...
# Subtest: planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
ok 256 - planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
  ---
  duration_ms: 0.122664
  ...
# Subtest: planTargetTaskUpdate preserves a trailing newline when one was already present
ok 257 - planTargetTaskUpdate preserves a trailing newline when one was already present
  ---
  duration_ms: 0.129688
  ...
# Subtest: planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
ok 258 - planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
  ---
  duration_ms: 0.106233
  ...
# Subtest: planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
ok 259 - planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
  ---
  duration_ms: 0.148253
  ...
# Subtest: planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
ok 260 - planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
  ---
  duration_ms: 0.106032
  ...
# Subtest: existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
ok 261 - existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
  ---
  duration_ms: 3.013633
  ...
# Subtest: new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
ok 262 - new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
  ---
  duration_ms: 0.733941
  ...
# Subtest: activation runtime aborts without any write when the target preimage goes stale
ok 263 - activation runtime aborts without any write when the target preimage goes stale
  ---
  duration_ms: 0.403931
  ...
# Subtest: same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
ok 264 - same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
  ---
  duration_ms: 2.298357
  ...
# Subtest: same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
ok 265 - same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
  ---
  duration_ms: 0.578835
  ...
# Subtest: a source marker edited after a successful existing-ID target write reports an accurate partial notice
ok 266 - a source marker edited after a successful existing-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.641515
  ...
# Subtest: a source marker edited after a successful new-ID target write reports an accurate partial notice
ok 267 - a source marker edited after a successful new-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.632537
  ...
# Subtest: planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
ok 268 - planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
  ---
  duration_ms: 0.204821
  ...
# Subtest: planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
ok 269 - planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
  ---
  duration_ms: 0.151479
  ...
# Subtest: planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
ok 270 - planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
  ---
  duration_ms: 0.161118
  ...
# Subtest: planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
ok 271 - planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.147301
  ...
# Subtest: direct Task Links raise ^prj while never pulling its date forward
ok 272 - direct Task Links raise ^prj while never pulling its date forward
  ---
  duration_ms: 0.170255
  ...
# Subtest: task-link selection: one link is selectable from any column, several are chosen by cursor
ok 273 - task-link selection: one link is selectable from any column, several are chosen by cursor
  ---
  duration_ms: 4.87743
  ...
# Subtest: task-link selection ignores picker/rename markers, plain links, and Markdown-style links
ok 274 - task-link selection ignores picker/rename markers, plain links, and Markdown-style links
  ---
  duration_ms: 0.489725
  ...
# Subtest: dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
ok 275 - dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
  ---
  duration_ms: 0.929645
  ...
# Subtest: inline Task Link deletion removes the token with its decoration and collapses whitespace
ok 276 - inline Task Link deletion removes the token with its decoration and collapses whitespace
  ---
  duration_ms: 0.859541
  ...
# Subtest: dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
ok 277 - dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
  ---
  duration_ms: 1.28899
  ...
# Subtest: mergeCoveringEdits keeps the covering edit and the earlier of identical edits
ok 278 - mergeCoveringEdits keeps the covering edit and the earlier of identical edits
  ---
  duration_ms: 0.271769
  ...
# Subtest: dependency transclusion detection needs an embedded sole-content child of a \#task line
ok 279 - dependency transclusion detection needs an embedded sole-content child of a \#task line
  ---
  duration_ms: 0.639661
  ...
# Subtest: Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
ok 280 - Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
  ---
  duration_ms: 6.542389
  ...
# Subtest: Task Link on a Next target works from an embedded aliased link outside any Pomodoro
ok 281 - Task Link on a Next target works from an embedded aliased link outside any Pomodoro
  ---
  duration_ms: 1.564287
  ...
# Subtest: same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
ok 282 - same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
  ---
  duration_ms: 1.442824
  ...
# Subtest: same-note Task Link deletion clamps the restored cursor to the shortened note
ok 283 - same-note Task Link deletion clamps the restored cursor to the shortened note
  ---
  duration_ms: 0.543327
  ...
# Subtest: a cleanup subtree that covers a nested selected link wins and links are not double counted
ok 284 - a cleanup subtree that covers a nested selected link wins and links are not double counted
  ---
  duration_ms: 0.727148
  ...
# Subtest: same-note Task Link in a closed entry deletes the closed entry it empties
ok 285 - same-note Task Link in a closed entry deletes the closed entry it empties
  ---
  duration_ms: 0.609514
  ...
# Subtest: Task Link in another day's note deletes the emptied entry there and in today's note
ok 286 - Task Link in another day's note deletes the emptied entry there and in today's note
  ---
  duration_ms: 0.554028
  ...
# Subtest: Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
ok 287 - Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
  ---
  duration_ms: 1.19982
  ...
# Subtest: Task Link on an In Progress target with a blank summary logs nothing
ok 288 - Task Link on an In Progress target with a blank summary logs nothing
  ---
  duration_ms: 0.747216
  ...
# Subtest: canceling the In Progress Task Link prompt leaves everything untouched
ok 289 - canceling the In Progress Task Link prompt leaves everything untouched
  ---
  duration_ms: 0.290394
  ...
# Subtest: canceling the In Progress unlink prompt in task mode leaves everything untouched
ok 290 - canceling the In Progress unlink prompt in task mode leaves everything untouched
  ---
  duration_ms: 0.540161
  ...
# Subtest: In Progress Task Link submit revalidates the link line and the target task
ok 291 - In Progress Task Link submit revalidates the link line and the target task
  ---
  duration_ms: 0.551132
  ...
# Subtest: Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
ok 292 - Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
  ---
  duration_ms: 0.611487
  ...
# Subtest: Task Link on a Done or Cancelled target is refused without edits
ok 293 - Task Link on a Done or Cancelled target is refused without edits
  ---
  duration_ms: 0.344267
  ...
# Subtest: Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
ok 294 - Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
  ---
  duration_ms: 0.613191
  ...
# Subtest: precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
ok 295 - precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
  ---
  duration_ms: 1.265175
  ...
# Subtest: Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
ok 296 - Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
  ---
  duration_ms: 0.347664
  ...
# Subtest: Task Link that is a sub-task dependency transclusion is refused without edits
ok 297 - Task Link that is a sub-task dependency transclusion is refused without edits
  ---
  duration_ms: 0.215912
  ...
# Subtest: Task Link partial failure after the daily write is retryable
ok 298 - Task Link partial failure after the daily write is retryable
  ---
  duration_ms: 0.877214
  ...
# Subtest: Task Link stops before any write when the target note changes after planning
ok 299 - Task Link stops before any write when the target note changes after planning
  ---
  duration_ms: 0.353915
  ...
# Subtest: Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
ok 300 - Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
  ---
  duration_ms: 0.410524
  ...
# Subtest: Task Link subtree deletion removes a nested target task without any status write
ok 301 - Task Link subtree deletion removes a nested target task without any status write
  ---
  duration_ms: 0.275255
  ...
# Subtest: whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
ok 302 - whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
  ---
  duration_ms: 0.551303
  ...
# Subtest: selected-link deletion maps a cursor inside a removed entry to its former start
ok 303 - selected-link deletion maps a cursor inside a removed entry to its former start
  ---
  duration_ms: 0.448857
  ...
# Subtest: work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
ok 304 - work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
  ---
  duration_ms: 1.466961
  ...
# Subtest: work log date helpers use local calendar components
ok 305 - work log date helpers use local calendar components
  ---
  duration_ms: 0.247092
  ...
# Subtest: planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
ok 306 - planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
  ---
  duration_ms: 0.631926
  ...
# Subtest: planWorkLogInsertion inherits an existing space-indented child prefix
ok 307 - planWorkLogInsertion inherits an existing space-indented child prefix
  ---
  duration_ms: 0.470559
  ...
# Subtest: planWorkLogInsertion inherits an existing tab-indented child prefix
ok 308 - planWorkLogInsertion inherits an existing tab-indented child prefix
  ---
  duration_ms: 0.228366
  ...
# Subtest: planWorkLogInsertion prepends newest-first entries into existing marker spellings
ok 309 - planWorkLogInsertion prepends newest-first entries into existing marker spellings
  ---
  duration_ms: 0.465638
  ...
# Subtest: planWorkLogInsertion ignores nested child-task markers and preserves CRLF
ok 310 - planWorkLogInsertion ignores nested child-task markers and preserves CRLF
  ---
  duration_ms: 0.380967
  ...
# Subtest: planWorkLogInsertion treats blank summaries as no-op structural edits
ok 311 - planWorkLogInsertion treats blank summaries as no-op structural edits
  ---
  duration_ms: 0.130249
  ...
# Subtest: the Open-reset planner is removed: unlink plans only a Work Log insertion
ok 312 - the Open-reset planner is removed: unlink plans only a Work Log insertion
  ---
  duration_ms: 0.321293
  ...
# Subtest: unlink Work Log plan keeps the In Progress checkbox and appends one entry
ok 313 - unlink Work Log plan keeps the In Progress checkbox and appends one entry
  ---
  duration_ms: 0.393892
  ...
# Subtest: article detection accepts scalar and list frontmatter values
ok 314 - article detection accepts scalar and list frontmatter values
  ---
  duration_ms: 1.296816
  ...
# Subtest: bob resolution prefers its setting, then known install paths, then PATH
ok 315 - bob resolution prefers its setting, then known install paths, then PATH
  ---
  duration_ms: 0.75429
  ...
# Subtest: plan decoder accepts v1 and rejects a foreign schema version
ok 316 - plan decoder accepts v1 and rejects a foreign schema version
  ---
  duration_ms: 0.332324
  ...
# Subtest: bob stdin spawn passes the article contract and vault environment
ok 317 - bob stdin spawn passes the article contract and vault environment
  ---
  duration_ms: 2.488501
  ...
# Subtest: bob plan stdout decodes UTF-8 split across chunks
ok 318 - bob plan stdout decodes UTF-8 split across chunks
  ---
  duration_ms: 0.934434
  ...
# Subtest: early bob exit on stdin reports EPIPE as a run failure
ok 319 - early bob exit on stdin reports EPIPE as a run failure
  ---
  duration_ms: 0.67588
  ...
# Subtest: line hunks become minimal cursor-preserving changes
ok 320 - line hunks become minimal cursor-preserving changes
  ---
  duration_ms: 0.602941
  ...
# Subtest: insert, multi-line replace, and deletion hunks reproduce the formatted note
ok 321 - insert, multi-line replace, and deletion hunks reproduce the formatted note
  ---
  duration_ms: 4.189066
  ...
# Subtest: notice shows bob's text and at most two warning findings
ok 322 - notice shows bob's text and at most two warning findings
  ---
  duration_ms: 0.415153
  ...
# Subtest: inbound changes apply only when their target line still matches the preimage
ok 323 - inbound changes apply only when their target line still matches the preimage
  ---
  duration_ms: 0.638108
  ...
# Subtest: undo guard blocks a reformat until a fresh input or delete event
ok 324 - undo guard blocks a reformat until a fresh input or delete event
  ---
  duration_ms: 0.362673
  ...
# Subtest: leave formatting observes the undo guard before saving or reading
ok 325 - leave formatting observes the undo guard before saving or reading
  ---
  duration_ms: 0.265277
  ...
# Subtest: Convert shows bob's refusal on every invocation
ok 326 - Convert shows bob's refusal on every invocation
  ---
  duration_ms: 0.240048
  ...
# Subtest: old bob's non-JSON article response gets one update notice per session
ok 327 - old bob's non-JSON article response gets one update notice per session
  ---
  duration_ms: 0.158913
  ...
# Subtest: format drops its response if the editor changed while bob was running
ok 328 - format drops its response if the editor changed while bob was running
  ---
  duration_ms: 0.291486
  ...
# Subtest: decoration ranges mark written section numbers from the outline
ok 329 - decoration ranges mark written section numbers from the outline
  ---
  duration_ms: 0.627448
  ...
# Subtest: a new outline rerenders each open Reading view once for that generation
ok 330 - a new outline rerenders each open Reading view once for that generation
  ---
  duration_ms: 0.315943
  ...
# Subtest: section at a given line uses the innermost outline range
ok 331 - section at a given line uses the innermost outline range
  ---
  duration_ms: 0.263693
  ...
# Subtest: stale-hint debounce and in-flight state machine
ok 332 - stale-hint debounce and in-flight state machine
  ---
  duration_ms: 0.281217
  ...
# Subtest: reading-view wrapping puts the leading number token in span.bob-secno
ok 333 - reading-view wrapping puts the leading number token in span.bob-secno
  ---
  duration_ms: 0.559758
  ...
# Subtest: applied plans remap outline lines onto the formatted buffer
ok 334 - applied plans remap outline lines onto the formatted buffer
  ---
  duration_ms: 0.129327
  ...
# Subtest: article styles scope the reading look under .bob-article
ok 335 - article styles scope the reading look under .bob-article
  ---
  duration_ms: 0.450941
  ...
# Subtest: look settings default to serif typeface and stale-number hints
ok 336 - look settings default to serif typeface and stale-number hints
  ---
  duration_ms: 0.102786
  ...
# Subtest: folds embed, struck, and plain legacy children into one canonical line
ok 337 - folds embed, struck, and plain legacy children into one canonical line
  ---
  duration_ms: 71.462747
  ...
# Subtest: legacy-label row links come first, then legacy children in order
ok 338 - legacy-label row links come first, then legacy children in order
  ---
  duration_ms: 1.873738
  ...
# Subtest: R2 adopts field-only open dependents; unadoptable ids stay warned
ok 339 - R2 adopts field-only open dependents; unadoptable ids stay warned
  ---
  duration_ms: 0.562204
  ...
# Subtest: closed dependents gain the line but keep the field untouched
ok 340 - closed dependents gain the line but keep the field untouched
  ---
  duration_ms: 0.924585
  ...
# Subtest: open dependents drop stale field ids and stamp targets missing [id::]
ok 341 - open dependents drop stale field ids and stamp targets missing [id::]
  ---
  duration_ms: 0.531394
  ...
# Subtest: unresolved links stay verbatim and keep field ids as breadcrumbs
ok 342 - unresolved links stay verbatim and keep field ids as breadcrumbs
  ---
  duration_ms: 0.496218
  ...
# Subtest: leaves \#^ref embeds, non-task parents, fences, and conflict children alone
ok 343 - leaves \#^ref embeds, non-task parents, fences, and conflict children alone
  ---
  duration_ms: 0.639761
  ...
# Subtest: malformed rows leave the whole dependent alone
ok 344 - malformed rows leave the whole dependent alone
  ---
  duration_ms: 0.50803
  ...
# Subtest: R9 deletes label-only rows and removes the open field
ok 345 - R9 deletes label-only rows and removes the open field
  ---
  duration_ms: 0.665781
  ...
# Subtest: cross-note links use the shortest unambiguous form
ok 346 - cross-note links use the shortest unambiguous form
  ---
  duration_ms: 0.644039
  ...
# Subtest: ambiguous basenames fall back to the full path
ok 347 - ambiguous basenames fall back to the full path
  ---
  duration_ms: 0.433968
  ...
# Subtest: duplicate ids are ambiguous and fatal for --write
ok 348 - duplicate ids are ambiguous and fatal for --write
  ---
  duration_ms: 0.221122
  ...
# Subtest: archive targets keep the done/ path and are never stamped
ok 349 - archive targets keep the done/ path and are never stamped
  ---
  duration_ms: 1.939102
  ...
# Subtest: self links stay on the line but are not projected
ok 350 - self links stay on the line but are not projected
  ---
  duration_ms: 1.029506
  ...
# Subtest: non-task targets stay on the line but are not projected
ok 351 - non-task targets stay on the line but are not projected
  ---
  duration_ms: 0.368183
  ...
# Subtest: preserves CRLF, missing final newline, and cancel-log position
ok 352 - preserves CRLF, missing final newline, and cancel-log position
  ---
  duration_ms: 0.381658
  ...
# Subtest: migration is idempotent
ok 353 - migration is idempotent
  ---
  duration_ms: 0.920969
  ...
# Subtest: parseArgs handles --vault, --write, --help, and rejects unknowns
ok 354 - parseArgs handles --vault, --write, --help, and rejects unknowns
  ---
  duration_ms: 0.580068
  ...
# Subtest: BOB_CLI_DIR wins over a sibling checkout and a cache
ok 355 - BOB_CLI_DIR wins over a sibling checkout and a cache
  ---
  duration_ms: 21.472179
  ...
# Subtest: sibling bob-cli is used when BOB_CLI_DIR is unset
ok 356 - sibling bob-cli is used when BOB_CLI_DIR is unset
  ---
  duration_ms: 12.557311
  ...
# Subtest: an invalid BOB_CLI_DIR does not fall through
ok 357 - an invalid BOB_CLI_DIR does not fall through
  ---
  duration_ms: 7.39161
  ...
# Subtest: cache clone is used when no user-owned checkout exists
ok 358 - cache clone is used when no user-owned checkout exists
  ---
  duration_ms: 28.566311
  ...
# Subtest: refreshing an existing cache keeps git chatter off stdout and forwards exact paths
ok 359 - refreshing an existing cache keeps git chatter off stdout and forwards exact paths
  ---
  duration_ms: 44.393203
  ...
# Subtest: a cache clone with a foreign origin fails before fetch or reset
ok 360 - a cache clone with a foreign origin fails before fetch or reset
  ---
  duration_ms: 19.155677
  ...
# Subtest: a justfile alone is rejected as an explicit bob-cli checkout
ok 361 - a justfile alone is rejected as an explicit bob-cli checkout
  ---
  duration_ms: 16.387913
  ...
# Subtest: just failures propagate
ok 362 - just failures propagate
  ---
  duration_ms: 14.179699
  ...
# Subtest: scans multiline, one-line, and guarded literal registrations
ok 363 - scans multiline, one-line, and guarded literal registrations
  ---
  duration_ms: 2.865941
  ...
# Subtest: scans an optional addCommand call
ok 364 - scans an optional addCommand call
  ---
  duration_ms: 0.262612
  ...
# Subtest: allows addCommand references only in a typeof guard
ok 365 - allows addCommand references only in a typeof guard
  ---
  duration_ms: 0.344958
  ...
# Subtest: rejects bind, call, and aliased addCommand references with source locations
ok 366 - rejects bind, call, and aliased addCommand references with source locations
  ---
  duration_ms: 0.566361
  ...
# Subtest: expands literal command data from a constant-array forEach across source files
ok 367 - expands literal command data from a constant-array forEach across source files
  ---
  duration_ms: 1.567772
  ...
# Subtest: balances nested callback syntax and ignores misleading comments, strings, templates, and regexes
ok 368 - balances nested callback syntax and ignores misleading comments, strings, templates, and regexes
  ---
  duration_ms: 0.525353
  ...
# Subtest: decodes escaped string metadata and literal default hotkeys
ok 369 - decodes escaped string metadata and literal default hotkeys
  ---
  duration_ms: 0.377381
  ...
# Subtest: returns no commands for a plugin without registrations
ok 370 - returns no commands for a plugin without registrations
  ---
  duration_ms: 0.173983
  ...
# Subtest: fails with source locations for dynamic metadata, hotkeys, and malformed tables
ok 371 - fails with source locations for dynamic metadata, hotkeys, and malformed tables
  ---
  duration_ms: 0.878728
  ...
# Subtest: fails duplicate command ids with both registration locations
ok 372 - fails duplicate command ids with both registration locations
  ---
  duration_ms: 0.49729
  ...
# Subtest: checks drift without writes, preserves prose, and generates deterministically
ok 373 - checks drift without writes, preserves prose, and generates deterministically
  ---
  duration_ms: 8.911101
  ...
# Subtest: code-span table cells preserve backslashes and use a safe backtick fence
ok 374 - code-span table cells preserve backslashes and use a safe backtick fence
  ---
  duration_ms: 1.581939
  ...
# Subtest: does not write any output when source validation fails
ok 375 - does not write any output when source validation fails
  ---
  duration_ms: 1.076064
  ...
# Subtest: BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
ok 376 - BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
  ---
  duration_ms: 2.991551
  ...
# Subtest: reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
ok 377 - reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
  ---
  duration_ms: 3.321952
  ...
# Subtest: stale, missing, canonical append, and frozen-owner models (BC8-BC10)
ok 378 - stale, missing, canonical append, and frozen-owner models (BC8-BC10)
  ---
  duration_ms: 0.830785
  ...
# Subtest: Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
ok 379 - Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
  ---
  duration_ms: 10.026659
  ...
# Subtest: budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
ok 380 - budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
  ---
  duration_ms: 2.138632
  ...
# Subtest: chip builder includes the 🔑 badge and has no edit controls
ok 381 - chip builder includes the 🔑 badge and has no edit controls
  ---
  duration_ms: 0.805668
  ...
# Subtest: RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
ok 382 - RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
  ---
  duration_ms: 2.470556
  ...
# Subtest: RBC2 hover × on a live chip calls removeDependent; notice is nav's
ok 383 - RBC2 hover × on a live chip calls removeDependent; notice is nav's
  ---
  duration_ms: 0.652045
  ...
# Subtest: RBC3 frozen, stale, and no api.blocks stay navigation-only
ok 384 - RBC3 frozen, stale, and no api.blocks stay navigation-only
  ---
  duration_ms: 1.269524
  ...
# Subtest: RBC4 Reading view matches Live Preview ＋ / ×
ok 385 - RBC4 Reading view matches Live Preview ＋ / ×
  ---
  duration_ms: 5.368829
  ...
# Subtest: collections namespace version is additive v1
ok 386 - collections namespace version is additive v1
  ---
  duration_ms: 1.176877
  ...
# Subtest: collection chip classes stay collection-specific through paint and refresh
ok 387 - collection chip classes stay collection-specific through paint and refresh
  ---
  duration_ms: 3.416322
  ...
# Subtest: projects: scalar resolved links count, lists never widen
ok 388 - projects: scalar resolved links count, lists never widen
  ---
  duration_ms: 0.364055
  ...
# Subtest: projects: templates, status, and containsAny edges
ok 389 - projects: templates, status, and containsAny edges
  ---
  duration_ms: 0.394904
  ...
# Subtest: references: exact prefix, md only, exact scalar status
ok 390 - references: exact prefix, md only, exact scalar status
  ---
  duration_ms: 0.33496
  ...
# Subtest: base contracts: accept current files, reject drift, tolerate presentation
ok 391 - base contracts: accept current files, reject drift, tolerate presentation
  ---
  duration_ms: 0.755753
  ...
# Subtest: entries: true zero vs unavailable with reason, failure isolation
ok 392 - entries: true zero vs unavailable with reason, failure isolation
  ---
  duration_ms: 0.300944
  ...
# Subtest: snapshot counts both collections once, true zero stays clickable
ok 393 - snapshot counts both collections once, true zero stays clickable
  ---
  duration_ms: 0.471159
  ...
# Subtest: snapshot never presents partial counts as final
ok 394 - snapshot never presents partial counts as final
  ---
  duration_ms: 0.507138
  ...
# Subtest: changed definitions fail closed per collection, never stale
ok 395 - changed definitions fail closed per collection, never stale
  ---
  duration_ms: 0.562744
  ...
# Subtest: renderChip links, labels, and cleans up per component
ok 396 - renderChip links, labels, and cleans up per component
  ---
  duration_ms: 0.660531
  ...
# Subtest: PENDING section excludes TODAY while the whole lane keeps it
ok 397 - PENDING section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 4.747724
  ...
# Subtest: NEXT section excludes TODAY while the whole lane keeps it
ok 398 - NEXT section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 0.383392
  ...
# Subtest: NEXT uses symbol *, not name matching
ok 399 - NEXT uses symbol *, not name matching
  ---
  duration_ms: 0.286557
  ...
# Subtest: READY badge and query agree on hide and path case variants
ok 400 - READY badge and query agree on hide and path case variants
  ---
  duration_ms: 0.538858
  ...
# Subtest: blocked uses the full list even outside the visible subset
ok 401 - blocked uses the full list even outside the visible subset
  ---
  duration_ms: 0.198138
  ...
# Subtest: duplicate block IDs, missing IDs, and reused objects stay per-row
ok 402 - duplicate block IDs, missing IDs, and reused objects stay per-row
  ---
  duration_ms: 0.241351
  ...
# Subtest: READY gating keeps exempt rows and drops NEW/ROTTEN
ok 403 - READY gating keeps exempt rows and drops NEW/ROTTEN
  ---
  duration_ms: 0.310543
  ...
# Subtest: throwing Today degrades to unavailable, never zero
ok 404 - throwing Today degrades to unavailable, never zero
  ---
  duration_ms: 6.960025
  ...
# Subtest: dashboard badges color the displayed section count and label whole-lane pressure
ok 405 - dashboard badges color the displayed section count and label whole-lane pressure
  ---
  duration_ms: 0.6706
  ...
# Subtest: dashboard section warning boundaries ignore TODAY-only whole-lane excess
ok 406 - dashboard section warning boundaries ignore TODAY-only whole-lane excess
  ---
  duration_ms: 0.761303
  ...
# Subtest: dashboard lane badge keeps unavailable data neutral
ok 407 - dashboard lane badge keeps unavailable data neutral
  ---
  duration_ms: 0.306295
  ...
# Subtest: dashboard lane paint and refresh keep color aligned with the visible section
ok 408 - dashboard lane paint and refresh keep color aligned with the visible section
  ---
  duration_ms: 2.775449
  ...
# Subtest: dashboard lane widgets refresh together and prune on unload
ok 409 - dashboard lane widgets refresh together and prune on unload
  ---
  duration_ms: 3.356587
  ...
# Subtest: daily paint matches dashboard section badges on screenshot fixtures
ok 410 - daily paint matches dashboard section badges on screenshot fixtures
  ---
  duration_ms: 22.12204
  ...
# Subtest: daily paint lane lint matches a red badge section count
ok 411 - daily paint lane lint matches a red badge section count
  ---
  duration_ms: 4.832316
  ...
# Subtest: daily and dashboard membership agree for exclusions and custom IN_PROGRESS
ok 412 - daily and dashboard membership agree for exclusions and custom IN_PROGRESS
  ---
  duration_ms: 3.16938
  ...
# Subtest: daily paint refreshes with dashboard when Today, lane, and cap change
ok 413 - daily paint refreshes with dashboard when Today, lane, and cap change
  ---
  duration_ms: 5.523083
  ...
# Subtest: older daily notes follow today's dashboard lanes
ok 414 - older daily notes follow today's dashboard lanes
  ---
  duration_ms: 2.91843
  ...
# Subtest: daily lane anchors keep shared navigation and reject stale paints
ok 415 - daily lane anchors keep shared navigation and reject stale paints
  ---
  duration_ms: 2.629911
  ...
# Subtest: daily paint stays unavailable until Tasks and Today are ready
ok 416 - daily paint stays unavailable until Tasks and Today are ready
  ---
  duration_ms: 1.172218
  ...
# Subtest: work tones: dashboard lane models carry section tones
ok 417 - work tones: dashboard lane models carry section tones
  ---
  duration_ms: 0.169053
  ...
# Subtest: T1 scheduled full-mode row gets a Fri mark inside the span
ok 418 - T1 scheduled full-mode row gets a Fri mark inside the span
  ---
  duration_ms: 2.776992
  ...
# Subtest: T2 done row maps to a completion Oct 5 mark
ok 419 - T2 done row maps to a completion Oct 5 mark
  ---
  duration_ms: 0.486398
  ...
# Subtest: T3 short-mode created span is left untouched by JS
ok 420 - T3 short-mode created span is left untouched by JS
  ---
  duration_ms: 0.286677
  ...
# Subtest: T4 pending row decorates once data-task appears; exhausted rows stay native
ok 421 - T4 pending row decorates once data-task appears; exhausted rows stay native
  ---
  duration_ms: 0.940465
  ...
# Subtest: T5 a second pass adds nothing
ok 422 - T5 a second pass adds nothing
  ---
  duration_ms: 0.265748
  ...
# Subtest: T6 task-due and task-start spans are untouched
ok 423 - T6 task-due and task-start spans are untouched
  ---
  duration_ms: 0.235189
  ...
# Subtest: T7 an invalid date is untouched
ok 424 - T7 an invalid date is untouched
  ---
  duration_ms: 0.250939
  ...
# Subtest: T8 nothing is scheduled with marks off or for connected non-Tasks elements
ok 425 - T8 nothing is scheduled with marks off or for connected non-Tasks elements
  ---
  duration_ms: 0.243174
  ...
# Subtest: T9 a Tasks-host Fri mark relabels to tomorrow on rollover
ok 426 - T9 a Tasks-host Fri mark relabels to tomorrow on rollover
  ---
  duration_ms: 0.673505
  ...
# Subtest: renderDateMarksIn schedules one shared frame for every row
ok 427 - renderDateMarksIn schedules one shared frame for every row
  ---
  duration_ms: 0.939674
  ...
# Subtest: the Tasks pass never throws on hostile input
ok 428 - the Tasks pass never throws on hostile input
  ---
  duration_ms: 0.391036
  ...
# Subtest: T10 real-DOM NodeList children decorate via direct and queued passes
ok 429 - T10 real-DOM NodeList children decorate via direct and queued passes
  ---
  duration_ms: 0.556743
  ...
# Subtest: T11 toggling off before a queued frame runs writes nothing
ok 430 - T11 toggling off before a queued frame runs writes nothing
  ---
  duration_ms: 0.389072
  ...
# Subtest: T12 a pending-row retry followed by disabling writes nothing
ok 431 - T12 a pending-row retry followed by disabling writes nothing
  ---
  duration_ms: 0.306355
  ...
# Subtest: T13 unloading before a callback runs writes nothing
ok 432 - T13 unloading before a callback runs writes nothing
  ---
  duration_ms: 0.909656
  ...
# Subtest: RT1 full-mode recurring result gets a daily mark and stays idempotent
ok 433 - RT1 full-mode recurring result gets a daily mark and stays idempotent
  ---
  duration_ms: 0.977576
  ...
# Subtest: RT2 recurring labels use the shared cadence grammar
ok 434 - RT2 recurring labels use the shared cadence grammar
  ---
  duration_ms: 2.107875
  ...
# Subtest: RT2a unknown inherited-name rules stay readable in Tasks results
ok 435 - RT2a unknown inherited-name rules stay readable in Tasks results
  ---
  duration_ms: 0.425803
  ...
# Subtest: RT3 short-mode recurring spans stay native to JS and use the CSS loop
ok 436 - RT3 short-mode recurring spans stay native to JS and use the CSS loop
  ---
  duration_ms: 0.887835
  ...
# Subtest: RT4 open checklist members keep recurrence pills without `when done`
ok 437 - RT4 open checklist members keep recurrence pills without `when done`
  ---
  duration_ms: 0.557274
  ...
# Subtest: RT5 invalid recurrence stays native and incomplete rows are retried
ok 438 - RT5 invalid recurrence stays native and incomplete rows are retried
  ---
  duration_ms: 0.378653
  ...
# Subtest: styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
ok 439 - styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
  ---
  duration_ms: 0.606929
  ...
# Subtest: DATE_MARK_FIELDS lists the four dates with verbs
ok 440 - DATE_MARK_FIELDS lists the four dates with verbs
  ---
  duration_ms: 1.686569
  ...
# Subtest: DM1 created today: label, tooltip, fold, quiet field
ok 441 - DM1 created today: label, tooltip, fold, quiet field
  ---
  duration_ms: 1.276667
  ...
# Subtest: DM2 created yesterday without space after the colons
ok 442 - DM2 created yesterday without space after the colons
  ---
  duration_ms: 0.37763
  ...
# Subtest: DM3-DM6 scheduled tomorrow, weekday, and month/day labels
ok 443 - DM3-DM6 scheduled tomorrow, weekday, and month/day labels
  ---
  duration_ms: 0.229197
  ...
# Subtest: DM7 scheduled today reads with emphasis timing
ok 444 - DM7 scheduled today reads with emphasis timing
  ---
  duration_ms: 0.245749
  ...
# Subtest: DM8 past scheduled uses month/day, never a weekday
ok 445 - DM8 past scheduled uses month/day, never a weekday
  ---
  duration_ms: 0.152281
  ...
# Subtest: DM9 completion on a closed task keeps the timeline grammar
ok 446 - DM9 completion on a closed task keeps the timeline grammar
  ---
  duration_ms: 0.186385
  ...
# Subtest: DM10 cancelled across years appends the year
ok 447 - DM10 cancelled across years appends the year
  ---
  duration_ms: 0.128275
  ...
# Subtest: DM11 next-year date appends the year
ok 448 - DM11 next-year date appends the year
  ---
  duration_ms: 0.295424
  ...
# Subtest: DM12 the weekday rule wins across the year boundary
ok 449 - DM12 the weekday rule wins across the year boundary
  ---
  duration_ms: 0.376348
  ...
# Subtest: DM13 two marks in order with folds 1 and 2
ok 450 - DM13 two marks in order with folds 1 and 2
  ---
  duration_ms: 0.418078
  ...
# Subtest: DM14 created and scheduled ranges stay disjoint from the fresh mark
ok 451 - DM14 created and scheduled ranges stay disjoint from the fresh mark
  ---
  duration_ms: 0.304351
  ...
# Subtest: DM15-DM16 paren and padded brackets are canonical
ok 452 - DM15-DM16 paren and padded brackets are canonical
  ---
  duration_ms: 0.163993
  ...
# Subtest: DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
ok 453 - DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
  ---
  duration_ms: 0.310463
  ...
# Subtest: DM22 code still parses pure but decorates nothing (see Live Preview)
ok 454 - DM22 code still parses pure but decorates nothing (see Live Preview)
  ---
  duration_ms: 0.111753
  ...
# Subtest: DM23 rescheduled is untouched and never a duplicate
ok 455 - DM23 rescheduled is untouched and never a duplicate
  ---
  duration_ms: 0.147191
  ...
# Subtest: DN1-DN9 non-canonical fields get no mark
ok 456 - DN1-DN9 non-canonical fields get no mark
  ---
  duration_ms: 0.2253
  ...
# Subtest: dateMarkContentStart finds content on list, quoted, and plain lines
ok 457 - dateMarkContentStart finds content on list, quoted, and plain lines
  ---
  duration_ms: 0.102185
  ...
# Subtest: dateMarkRelativePhrase covers the exact-day phrases
ok 458 - dateMarkRelativePhrase covers the exact-day phrases
  ---
  duration_ms: 0.08922
  ...
# Subtest: dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
ok 459 - dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
  ---
  duration_ms: 0.300874
  ...
# Subtest: no model output contains a double colon
ok 460 - no model output contains a double colon
  ---
  duration_ms: 2.306894
  ...
# Subtest: a new day always changes the widget key
ok 461 - a new day always changes the widget key
  ---
  duration_ms: 0.217525
  ...
# Subtest: element structure and the decorative/inheritColor/rendered options
ok 462 - element structure and the decorative/inheritColor/rendered options
  ---
  duration_ms: 0.532036
  ...
# Subtest: Live Preview emits several decorations in ascending order
ok 463 - Live Preview emits several decorations in ascending order
  ---
  duration_ms: 1.396476
  ...
# Subtest: Live Preview reveals per field, never the whole line
ok 464 - Live Preview reveals per field, never the whole line
  ---
  duration_ms: 0.270647
  ...
# Subtest: Live Preview refuses source mode, code, and disabled marks
ok 465 - Live Preview refuses source mode, code, and disabled marks
  ---
  duration_ms: 0.439809
  ...
# Subtest: widget mousedown anchors at the field start for folds 0, 1, and 2
ok 466 - widget mousedown anchors at the field start for folds 0, 1, and 2
  ---
  duration_ms: 0.92729
  ...
# Subtest: DM24 a cursor in the folded run unfolds the mark (vim cw)
ok 467 - DM24 a cursor in the folded run unfolds the mark (vim cw)
  ---
  duration_ms: 0.250317
  ...
# Subtest: DM25 a cursor in Tasks double space unfolds only that field
ok 468 - DM25 a cursor in Tasks double space unfolds only that field
  ---
  duration_ms: 0.176266
  ...
# Subtest: a selection ending inside the run unfolds; ending at its start keeps the fold
ok 469 - a selection ending inside the run unfolds; ending at its start keeps the fold
  ---
  duration_ms: 0.181075
  ...
# Subtest: no emitted decoration ever hides a cursor, and reveal still means field overlap
ok 470 - no emitted decoration ever hides a cursor, and reveal still means field overlap
  ---
  duration_ms: 10.272931
  ...
# Subtest: dateMarkSelectionFold: reveal, unfold, fold, and garbage input
ok 471 - dateMarkSelectionFold: reveal, unfold, fold, and garbage input
  ---
  duration_ms: 0.241071
  ...
# Subtest: mousedown on an unfolded (fold-0) widget anchors at the field start
ok 472 - mousedown on an unfolded (fold-0) widget anchors at the field start
  ---
  duration_ms: 0.356761
  ...
# Subtest: rendered views split several fields in one node
ok 473 - rendered views split several fields in one node
  ---
  duration_ms: 1.575668
  ...
# Subtest: rendered views skip exclusions and duplicates
ok 474 - rendered views skip exclusions and duplicates
  ---
  duration_ms: 0.481499
  ...
# Subtest: RO1 rendered marks relabel in place across midnight
ok 475 - RO1 rendered marks relabel in place across midnight
  ---
  duration_ms: 0.498
  ...
# Subtest: rollover dispatches once per day change and never touches widgets
ok 476 - rollover dispatches once per day change and never touches widgets
  ---
  duration_ms: 0.334529
  ...
# Subtest: api.dateMarks v1 is additive, sync, and never throwing
ok 477 - api.dateMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.438086
  ...
# Subtest: session toggle and onload wiring
ok 478 - session toggle and onload wiring
  ---
  duration_ms: 4.793099
  ...
# Subtest: styles.css contract: masks, tones, repair flag, resting
ok 479 - styles.css contract: masks, tones, repair flag, resting
  ---
  duration_ms: 0.893295
  ...
# Subtest: DP parse vectors
ok 480 - DP parse vectors
  ---
  duration_ms: 2.265194
  ...
# Subtest: DC chip model vectors
ok 481 - DC chip model vectors
  ---
  duration_ms: 1.727638
  ...
# Subtest: decoration builds one widget, reveals on cursor, skips code and ranges
ok 482 - decoration builds one widget, reveals on cursor, skips code and ranges
  ---
  duration_ms: 7.399714
  ...
# Subtest: decoration skips paragraphs, grandchildren, and Work Log lines
ok 483 - decoration skips paragraphs, grandchildren, and Work Log lines
  ---
  duration_ms: 0.708373
  ...
# Subtest: decoration renders chips on DP30 and still skips DP20
ok 484 - decoration renders chips on DP30 and still skips DP20
  ---
  duration_ms: 0.791481
  ...
# Subtest: ownership check reads O(depth) lines, not the whole note
ok 485 - ownership check reads O(depth) lines, not the whole note
  ---
  duration_ms: 3.111931
  ...
# Subtest: widget identity covers the line and the interactive flag
ok 486 - widget identity covers the line and the interactive flag
  ---
  duration_ms: 1.895399
  ...
# Subtest: element hides actions without nav api v1
ok 487 - element hides actions without nav api v1
  ---
  duration_ms: 1.027201
  ...
# Subtest: nav api feature detection gates actions
ok 488 - nav api feature detection gates actions
  ---
  duration_ms: 0.578554
  ...
# Subtest: reading view decorates only the Depends-On row, hides chrome, stays idempotent
ok 489 - reading view decorates only the Depends-On row, hides chrome, stays idempotent
  ---
  duration_ms: 4.103933
  ...
# Subtest: reading view collapses more than three Done targets to one chip
ok 490 - reading view collapses more than three Done targets to one chip
  ---
  duration_ms: 1.986012
  ...
# Subtest: DC chip model vectors by id: DC2, DC5, DC6, DC9
ok 491 - DC chip model vectors by id: DC2, DC5, DC6, DC9
  ---
  duration_ms: 0.422276
  ...
# Subtest: chip actions send the 0-based line index through nav api v1
ok 492 - chip actions send the 0-based line index through nav api v1
  ---
  duration_ms: 1.69725
  ...
# Subtest: chip hover passes the chip element and its row to the preview
ok 493 - chip hover passes the chip element and its row to the preview
  ---
  duration_ms: 0.27228
  ...
# Subtest: chip lookup index lives on the freshness memo
ok 494 - chip lookup index lives on the freshness memo
  ---
  duration_ms: 0.707861
  ...
# Subtest: reading view hides actions when the line cannot be derived
ok 495 - reading view hides actions when the line cannot be derived
  ---
  duration_ms: 15.547669
  ...
# Subtest: reading view actions carry the derived 0-based line
ok 496 - reading view actions carry the derived 0-based line
  ---
  duration_ms: 2.48813
  ...
# Subtest: reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
ok 497 - reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
  ---
  duration_ms: 0.56072
  ...
# Subtest: reading view renders chips on DP30 (owner is a task under a Work Log entry)
ok 498 - reading view renders chips on DP30 (owner is a task under a Work Log entry)
  ---
  duration_ms: 0.405243
  ...
# Subtest: reading view DP30 row actions send the owned Depends-On line
ok 499 - reading view DP30 row actions send the owned Depends-On line
  ---
  duration_ms: 2.02719
  ...
# Subtest: reading view second-row remove sends the second line when two tasks share a prerequisite
ok 500 - reading view second-row remove sends the second line when two tasks share a prerequisite
  ---
  duration_ms: 1.513499
  ...
# Subtest: chip lookup index builds once per freshness memo
ok 501 - chip lookup index builds once per freshness memo
  ---
  duration_ms: 0.377711
  ...
# Subtest: decoration evaluates ownership without copying the note
ok 502 - decoration evaluates ownership without copying the note
  ---
  duration_ms: 0.433207
  ...
# Subtest: toggle flips the body class and onload wires chips
ok 503 - toggle flips the body class and onload wires chips
  ---
  duration_ms: 4.540688
  ...
# Subtest: capability: nav card v2 is capable
ok 504 - capability: nav card v2 is capable
  ---
  duration_ms: 0.860373
  ...
# Subtest: capability: nav card v1 is not capable
ok 505 - capability: nav card v1 is not capable
  ---
  duration_ms: 0.196394
  ...
# Subtest: capability: absent nav, missing api, and old versions are not capable
ok 506 - capability: absent nav, missing api, and old versions are not capable
  ---
  duration_ms: 0.126201
  ...
# Subtest: capability: a throwing app never throws
ok 507 - capability: a throwing app never throws
  ---
  duration_ms: 0.178691
  ...
# Subtest: leaf: active capable due choice replaces refresh with a leaf
ok 508 - leaf: active capable due choice replaces refresh with a leaf
  ---
  duration_ms: 2.44136
  ...
# Subtest: leaf: the same row without the card keeps refresh and counting words
ok 509 - leaf: the same row without the card keeps refresh and counting words
  ---
  duration_ms: 0.405644
  ...
# Subtest: leaf: early dates still leaf when capable
ok 510 - leaf: early dates still leaf when capable
  ---
  duration_ms: 0.418589
  ...
# Subtest: leaf: decay-off rows never leaf even when capable
ok 511 - leaf: decay-off rows never leaf even when capable
  ---
  duration_ms: 0.38234
  ...
# Subtest: leaf: below-threshold rows never leaf
ok 512 - leaf: below-threshold rows never leaf
  ---
  duration_ms: 0.518079
  ...
# Subtest: leaf: threshold zero asks on every due re-confirmation when capable
ok 513 - leaf: threshold zero asks on every due re-confirmation when capable
  ---
  duration_ms: 0.478363
  ...
# Subtest: leaf: overflow renders capped dots with +N and the exact count in text
ok 514 - leaf: overflow renders capped dots with +N and the exact count in text
  ---
  duration_ms: 0.294172
  ...
# Subtest: leaf: out-of-scope and closed tasks show dots quietly, never a leaf
ok 515 - leaf: out-of-scope and closed tasks show dots quietly, never a leaf
  ---
  duration_ms: 0.678425
  ...
# Subtest: leaf: unresolved marks show dots quietly with counting-only wording
ok 516 - leaf: unresolved marks show dots quietly with counting-only wording
  ---
  duration_ms: 0.194061
  ...
# Subtest: element: leaf marks carry data-decide true and a leaf path
ok 517 - element: leaf marks carry data-decide true and a leaf path
  ---
  duration_ms: 0.602961
  ...
# Subtest: element: non-decision marks carry data-decide false
ok 518 - element: non-decision marks carry data-decide false
  ---
  duration_ms: 0.217766
  ...
# Subtest: footer groups omit every zero tier and keep walk order
ok 519 - footer groups omit every zero tier and keep walk order
  ---
  duration_ms: 1.644519
  ...
# Subtest: PRE and POST groups bracket the nine-tier queue and expose completion hints
ok 520 - PRE and POST groups bracket the nine-tier queue and expose completion hints
  ---
  duration_ms: 0.799265
  ...
# Subtest: a NEW-state project appears only in its walk tier
ok 521 - a NEW-state project appears only in its walk tier
  ---
  duration_ms: 0.207316
  ...
# Subtest: empty queue hides the footer even with upkeep or a met budget
ok 522 - empty queue hides the footer even with upkeep or a met budget
  ---
  duration_ms: 0.152501
  ...
# Subtest: unavailable or missing data never render false counts
ok 523 - unavailable or missing data never render false counts
  ---
  duration_ms: 0.356541
  ...
# Subtest: generic summary names due, commitments, and nonempty groups
ok 524 - generic summary names due, commitments, and nonempty groups
  ---
  duration_ms: 0.487931
  ...
# Subtest: current-task context uses shared ranks and compact wording
ok 525 - current-task context uses shared ranks and compact wording
  ---
  duration_ms: 0.845975
  ...
# Subtest: only ROTTEN remaining names commitments done or a met budget
ok 526 - only ROTTEN remaining names commitments done or a met budget
  ---
  duration_ms: 0.408319
  ...
# Subtest: NEW and commitments take precedence over a met budget
ok 527 - NEW and commitments take precedence over a met budget
  ---
  duration_ms: 0.571421
  ...
# Subtest: reviewEntryView compact and detail cover the original freshness tiers
ok 528 - reviewEntryView compact and detail cover the original freshness tiers
  ---
  duration_ms: 1.104038
  ...
# Subtest: cursor matching requires a unique verified identity
ok 529 - cursor matching requires a unique verified identity
  ---
  duration_ms: 0.500255
  ...
# Subtest: footer paint hides the host and keeps a stable button
ok 530 - footer paint hides the host and keeps a stable button
  ---
  duration_ms: 1.519
  ...
# Subtest: status bar 0-1-0 transitions hide without a reload
ok 531 - status bar 0-1-0 transitions hide without a reload
  ---
  duration_ms: 7.997898
  ...
# Subtest: cursor-only updates reuse a warm memo
ok 532 - cursor-only updates reuse a warm memo
  ---
  duration_ms: 1.322344
  ...
# Subtest: unload disconnects the observer and click handler
ok 533 - unload disconnects the observer and click handler
  ---
  duration_ms: 1.554899
  ...
# Subtest: queue-built ranks agree with the footer current entry
ok 534 - queue-built ranks agree with the footer current entry
  ---
  duration_ms: 0.829474
  ...
# Subtest: footer short labels map every tier
ok 535 - footer short labels map every tier
  ---
  duration_ms: 0.117645
  ...
# Subtest: current-row footer context uses short labels while entry views keep full labels
ok 536 - current-row footer context uses short labels while entry views keep full labels
  ---
  duration_ms: 0.274364
  ...
# Subtest: legend line lists only current abbreviated tiers
ok 537 - legend line lists only current abbreviated tiers
  ---
  duration_ms: 0.266419
  ...
# Subtest: K1 absent: no keeps means 0 with no lints
ok 538 - K1 absent: no keeps means 0 with no lints
  ---
  duration_ms: 2.566469
  ...
# Subtest: K8 misplaced: keeps inside the Tasks suffix reads with a lint
ok 539 - K8 misplaced: keeps inside the Tasks suffix reads with a lint
  ---
  duration_ms: 0.446192
  ...
# Subtest: K9 duplicates and invalid values: first valid wins, else 0
ok 540 - K9 duplicates and invalid values: first valid wins, else 0
  ---
  duration_ms: 0.598773
  ...
# Subtest: K10 ceiling and NEW: 999 reads, never-confirmed reads 0
ok 541 - K10 ceiling and NEW: 999 reads, never-confirmed reads 0
  ---
  duration_ms: 0.231562
  ...
# Subtest: K13 exact keys: near-miss keys are not keeps; parens read
ok 542 - K13 exact keys: near-miss keys are not keeps; parens read
  ---
  duration_ms: 0.198278
  ...
# Subtest: keeps value parser accepts only decimal 1-999
ok 543 - keeps value parser accepts only decimal 1-999
  ---
  duration_ms: 0.186176
  ...
# Subtest: K2 first valid canonical: uncounted keep preserves and repairs
ok 544 - K2 first valid canonical: uncounted keep preserves and repairs
  ---
  duration_ms: 0.752626
  ...
# Subtest: K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
ok 545 - K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
  ---
  duration_ms: 0.484605
  ...
# Subtest: K4 same-day preserve noop: canonical kept line is byte-identical
ok 546 - K4 same-day preserve noop: canonical kept line is byte-identical
  ---
  duration_ms: 0.462873
  ...
# Subtest: K5 generic stamp clears, even same-day
ok 547 - K5 generic stamp clears, even same-day
  ---
  duration_ms: 0.45021
  ...
# Subtest: K6 set-refresh clears keeps
ok 548 - K6 set-refresh clears keeps
  ---
  duration_ms: 0.288972
  ...
# Subtest: K7 stale stamp clears keeps
ok 549 - K7 stale stamp clears keeps
  ---
  duration_ms: 0.159855
  ...
# Subtest: K8b misplaced keeps repaired to canonical order by a keep
ok 550 - K8b misplaced keeps repaired to canonical order by a keep
  ---
  duration_ms: 0.188881
  ...
# Subtest: K11 refusals preserve: closed and recurring lines never write
ok 551 - K11 refusals preserve: closed and recurring lines never write
  ---
  duration_ms: 0.206244
  ...
# Subtest: counted keep increments a stale streak once in the same write
ok 552 - counted keep increments a stale streak once in the same write
  ---
  duration_ms: 0.199311
  ...
# Subtest: first counted keep on a streakless due task writes keeps 1
ok 553 - first counted keep on a streakless due task writes keeps 1
  ---
  duration_ms: 0.16204
  ...
# Subtest: counted keep saturates at 999 and never wraps
ok 554 - counted keep saturates at 999 and never wraps
  ---
  duration_ms: 0.239176
  ...
# Subtest: counted keep needs a valid prior fresh before today
ok 555 - counted keep needs a valid prior fresh before today
  ---
  duration_ms: 0.325601
  ...
# Subtest: counted keep repairs malformed and duplicate placement
ok 556 - counted keep repairs malformed and duplicate placement
  ---
  duration_ms: 0.262741
  ...
# Subtest: uncounted keep preserves the valid value while canonicalizing
ok 557 - uncounted keep preserves the valid value while canonicalizing
  ---
  duration_ms: 0.206474
  ...
# Subtest: UB13 keep on an unblock TICKLER preserves the streak and skips the card
ok 558 - UB13 keep on an unblock TICKLER preserves the streak and skips the card
  ---
  duration_ms: 1.871313
  ...
# Subtest: a scheduled tickler still counts when schedule wins an unblock tie
ok 559 - a scheduled tickler still counts when schedule wins an unblock tie
  ---
  duration_ms: 0.305924
  ...
# Subtest: decay normalization: absent, null, true, and {} enable with 3
ok 560 - decay normalization: absent, null, true, and {} enable with 3
  ---
  duration_ms: 0.670761
  ...
# Subtest: decay false counts and displays but never asks
ok 561 - decay false counts and displays but never asks
  ---
  duration_ms: 0.114729
  ...
# Subtest: decay keeps 0 and fixed entry normalize
ok 562 - decay keeps 0 and fixed entry normalize
  ---
  duration_ms: 0.129247
  ...
# Subtest: invalid decay shapes fail the freshness config contract
ok 563 - invalid decay shapes fail the freshness config contract
  ---
  duration_ms: 0.233927
  ...
# Subtest: B: at-limit Ready due rows decide on every local day
ok 564 - B: at-limit Ready due rows decide on every local day
  ---
  duration_ms: 0.441853
  ...
# Subtest: D1 early date: an at-limit Ready due row decides
ok 565 - D1 early date: an at-limit Ready due row decides
  ---
  duration_ms: 0.108347
  ...
# Subtest: D2 at limit decides; D3 below limit stamps without a card
ok 566 - D2 at limit decides; D3 below limit stamps without a card
  ---
  duration_ms: 0.119548
  ...
# Subtest: D4 tickler counts as due; D5 NEW never decides
ok 567 - D4 tickler counts as due; D5 NEW never decides
  ---
  duration_ms: 0.171107
  ...
# Subtest: D6 zero limit asks on every due Ready re-confirmation
ok 568 - D6 zero limit asks on every due Ready re-confirmation
  ---
  duration_ms: 0.086195
  ...
# Subtest: D7 off never asks; D8 lane rows never decide
ok 569 - D7 off never asks; D8 lane rows never decide
  ---
  duration_ms: 0.548177
  ...
# Subtest: evaluator, queue, and counts carry keeps and decide
ok 570 - evaluator, queue, and counts carry keeps and decide
  ---
  duration_ms: 1.096382
  ...
# Subtest: no keeps: the existing mark is unchanged
ok 571 - no keeps: the existing mark is unchanged
  ---
  duration_ms: 0.907913
  ...
# Subtest: aging with two keeps: faint pips plus a counting-only line
ok 572 - aging with two keeps: faint pips plus a counting-only line
  ---
  duration_ms: 0.265647
  ...
# Subtest: confirmed today with two keeps: check glyph, faint dots
ok 573 - confirmed today with two keeps: check glyph, faint dots
  ---
  duration_ms: 0.22023
  ...
# Subtest: due below threshold: orange capsule keeps its glyph, adds dots
ok 574 - due below threshold: orange capsule keeps its glyph, adds dots
  ---
  duration_ms: 0.236
  ...
# Subtest: resting marks show historical dots quietly and never decide
ok 575 - resting marks show historical dots quietly and never decide
  ---
  duration_ms: 0.325581
  ...
# Subtest: active decision due: data stays truthful, leaf stays gated
ok 576 - active decision due: data stays truthful, leaf stays gated
  ---
  duration_ms: 0.235821
  ...
# Subtest: dot caps follow the threshold with +N overflow
ok 577 - dot caps follow the threshold with +N overflow
  ---
  duration_ms: 0.562284
  ...
# Subtest: keeps tooltip wording: singulars, zero threshold, off state
ok 578 - keeps tooltip wording: singulars, zero threshold, off state
  ---
  duration_ms: 0.11035
  ...
# Subtest: noncanonical keeps never fold but keep their repair pill
ok 579 - noncanonical keeps never fold but keep their repair pill
  ---
  duration_ms: 0.32469
  ...
# Subtest: quoted lines fold; rendered fragments fold without task checks
ok 580 - quoted lines fold; rendered fragments fold without task checks
  ---
  duration_ms: 0.20925
  ...
# Subtest: unresolved marks show the line's own pips quietly and never decide
ok 581 - unresolved marks show the line's own pips quietly and never decide
  ---
  duration_ms: 0.178712
  ...
# Subtest: consensus sees count and decision eligibility: ambiguity stays neutral
ok 582 - consensus sees count and decision eligibility: ambiguity stays neutral
  ---
  duration_ms: 0.454307
  ...
# Subtest: pips render as one aria-hidden span with the count in the label
ok 583 - pips render as one aria-hidden span with the count in the label
  ---
  duration_ms: 1.122894
  ...
# Subtest: Live Preview decorates the folded range including space and refresh
ok 584 - Live Preview decorates the folded range including space and refresh
  ---
  duration_ms: 4.606174
  ...
# Subtest: Live Preview reveals the raw field when the cursor overlaps either edge
ok 585 - Live Preview reveals the raw field when the cursor overlaps either edge
  ---
  duration_ms: 1.148433
  ...
# Subtest: Live Preview skips codeblock and inline code spans
ok 586 - Live Preview skips codeblock and inline code spans
  ---
  duration_ms: 0.672874
  ...
# Subtest: source mode and marks-off yield no decorations
ok 587 - source mode and marks-off yield no decorations
  ---
  duration_ms: 0.167259
  ...
# Subtest: update rebuilds on the refresh effect and widget eq is stable
ok 588 - update rebuilds on the refresh effect and widget eq is stable
  ---
  duration_ms: 0.962097
  ...
# Subtest: widget click reveals the field at the folded offset
ok 589 - widget click reveals the field at the folded offset
  ---
  duration_ms: 0.674488
  ...
# Subtest: line resolver prefers exact, then consensus, then unresolved
ok 590 - line resolver prefers exact, then consensus, then unresolved
  ---
  duration_ms: 1.139054
  ...
# Subtest: decoration builds reuse the snapshot without touching the loader
ok 591 - decoration builds reuse the snapshot without touching the loader
  ---
  duration_ms: 0.386598
  ...
# Subtest: rendered views split text nodes and skip excluded ancestors
ok 592 - rendered views split text nodes and skip excluded ancestors
  ---
  duration_ms: 1.382729
  ...
# Subtest: rendered views stay idempotent
ok 593 - rendered views stay idempotent
  ---
  duration_ms: 0.744161
  ...
# Subtest: text resolver reaches consensus and degrades to neutral
ok 594 - text resolver reaches consensus and degrades to neutral
  ---
  duration_ms: 0.61777
  ...
# Subtest: session toggle flips the body class and notifies
ok 595 - session toggle flips the body class and notifies
  ---
  duration_ms: 0.834954
  ...
# Subtest: onload registers the toggle, extension, and post-processor
ok 596 - onload registers the toggle, extension, and post-processor
  ---
  duration_ms: 4.144062
  ...
# Subtest: M1 today: check glyph, today label, full ring
ok 597 - M1 today: check glyph, today label, full ring
  ---
  duration_ms: 3.70325
  ...
# Subtest: M2 aging: ring glyph, 3d label, draining lease
ok 598 - M2 aging: ring glyph, 3d label, draining lease
  ---
  duration_ms: 0.402428
  ...
# Subtest: M3 boundary: ROTTEN due capsule with Alt+F hint
ok 599 - M3 boundary: ROTTEN due capsule with Alt+F hint
  ---
  duration_ms: 0.34569
  ...
# Subtest: checklist marks replace stamp hints with their completion tier
ok 600 - checklist marks replace stamp hints with their completion tier
  ---
  duration_ms: 0.65994
  ...
# Subtest: M4 yesterday uses the yesterday relative
ok 601 - M4 yesterday uses the yesterday relative
  ---
  duration_ms: 0.253955
  ...
# Subtest: M5 folded refresh shows the /14d suffix
ok 602 - M5 folded refresh shows the /14d suffix
  ---
  duration_ms: 0.425612
  ...
# Subtest: M6 refresh today: today tone hides the interval suffix
ok 603 - M6 refresh today: today tone hides the interval suffix
  ---
  duration_ms: 0.297968
  ...
# Subtest: M7 note interval stays tooltip-only
ok 604 - M7 note interval stays tooltip-only
  ---
  duration_ms: 0.567413
  ...
# Subtest: M8 resurfaced: due tone on the scheduled return
ok 605 - M8 resurfaced: due tone on the scheduled return
  ---
  duration_ms: 0.488363
  ...
# Subtest: M9 due NEXT lane with keep/release/today keys
ok 606 - M9 due NEXT lane with keep/release/today keys
  ---
  duration_ms: 0.502219
  ...
# Subtest: M10 NEXT lane stamped today
ok 607 - M10 NEXT lane stamped today
  ---
  duration_ms: 0.291787
  ...
# Subtest: M19 disabled Next lane rests
ok 608 - M19 disabled Next lane rests
  ---
  duration_ms: 0.255368
  ...
# Subtest: M20 PENDING lane folds refresh without the suffix
ok 609 - M20 PENDING lane folds refresh without the suffix
  ---
  duration_ms: 0.237864
  ...
# Subtest: M11 closed: resting beats age 0
ok 610 - M11 closed: resting beats age 0
  ---
  duration_ms: 0.202006
  ...
# Subtest: M12 unresolved running and M13 unresolved lease over
ok 611 - M12 unresolved running and M13 unresolved lease over
  ---
  duration_ms: 0.208718
  ...
# Subtest: M14 linked today rests with its reason
ok 612 - M14 linked today rests with its reason
  ---
  duration_ms: 0.171457
  ...
# Subtest: M15 other year shows the year and the 282d age
ok 613 - M15 other year shows the year and the 282d age
  ---
  duration_ms: 0.141561
  ...
# Subtest: M16 quoted line keeps foldSpace
ok 614 - M16 quoted line keeps foldSpace
  ---
  duration_ms: 0.144776
  ...
# Subtest: M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
ok 615 - M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
  ---
  duration_ms: 0.347263
  ...
# Subtest: N1-N6 non-canonical lines get no mark
ok 616 - N1-N6 non-canonical lines get no mark
  ---
  duration_ms: 0.159244
  ...
# Subtest: C1-C3 consensus is exact or unresolved
ok 617 - C1-C3 consensus is exact or unresolved
  ---
  duration_ms: 0.53944
  ...
# Subtest: freshnessMarkResolution treats evaluator new as unresolved
ok 618 - freshnessMarkResolution treats evaluator new as unresolved
  ---
  duration_ms: 0.154976
  ...
# Subtest: freshnessMarkSourceInText covers rendered fragments
ok 619 - freshnessMarkSourceInText covers rendered fragments
  ---
  duration_ms: 0.191787
  ...
# Subtest: tone order: closed, then due, then age 0, then out of scope
ok 620 - tone order: closed, then due, then age 0, then out of scope
  ---
  duration_ms: 0.357302
  ...
# Subtest: no tooltip ever contains a double colon
ok 621 - no tooltip ever contains a double colon
  ---
  duration_ms: 0.690758
  ...
# Subtest: freshnessShortDate pins English names and the year rule
ok 622 - freshnessShortDate pins English names and the year rule
  ---
  duration_ms: 0.100432
  ...
# Subtest: DOM builder structure, attributes, and ring geometry
ok 623 - DOM builder structure, attributes, and ring geometry
  ---
  duration_ms: 0.949704
  ...
# Subtest: every mark helper is synchronous and never throws on bad input
ok 624 - every mark helper is synchronous and never throws on bad input
  ---
  duration_ms: 0.103708
  ...
# Subtest: freshness namespace v12 exposes unblock TICKLER metadata and writers
ok 625 - freshness namespace v12 exposes unblock TICKLER metadata and writers
  ---
  duration_ms: 11.320661
  ...
# Subtest: freshness state and count API expose an unblock return source
ok 626 - freshness state and count API expose an unblock return source
  ---
  duration_ms: 1.68708
  ...
# Subtest: checklist rows report tier and rank while keeping the READY bucket null
ok 627 - checklist rows report tier and rank while keeping the READY bucket null
  ---
  duration_ms: 1.236721
  ...
# Subtest: tier, isDue, and rank cover lane rows
ok 628 - tier, isDue, and rank cover lane rows
  ---
  duration_ms: 2.245055
  ...
# Subtest: memo invalidates on a new tasks array, rollover, and frontmatter
ok 629 - memo invalidates on a new tasks array, rollover, and frontmatter
  ---
  duration_ms: 2.973135
  ...
# Subtest: the reload event fires only when the due key set changes
ok 630 - the reload event fires only when the due key set changes
  ---
  duration_ms: 2.814833
  ...
# Subtest: status bar text covers every state, and a missing host stays quiet
ok 631 - status bar text covers every state, and a missing host stays quiet
  ---
  duration_ms: 1.300052
  ...
# Subtest: status bar clicks through, falling back to rotten
ok 632 - status bar clicks through, falling back to rotten
  ---
  duration_ms: 5.127439
  ...
# Subtest: every freshness api member is synchronous and never throws
ok 633 - every freshness api member is synchronous and never throws
  ---
  duration_ms: 2.369452
  ...
# Subtest: placement vectors P1-P11, P14-P16, P18 stamp canonically
ok 634 - placement vectors P1-P11, P14-P16, P18 stamp canonically
  ---
  duration_ms: 3.197002
  ...
# Subtest: P12 set and clear refresh stamps alongside
ok 635 - P12 set and clear refresh stamps alongside
  ---
  duration_ms: 0.295904
  ...
# Subtest: P13 recurring and P17 done tasks are refused unchanged
ok 636 - P13 recurring and P17 done tasks are refused unchanged
  ---
  duration_ms: 0.169734
  ...
# Subtest: U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
ok 637 - U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
  ---
  duration_ms: 0.769027
  ...
# Subtest: reader reports misplaced and duplicate fields
ok 638 - reader reports misplaced and duplicate fields
  ---
  duration_ms: 0.322015
  ...
# Subtest: Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
ok 639 - Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
  ---
  duration_ms: 5.233882
  ...
# Subtest: Q2 tier order beats path order
ok 640 - Q2 tier order beats path order
  ---
  duration_ms: 1.448294
  ...
# Subtest: L1 lane due and stamped today
ok 641 - L1 lane due and stamped today
  ---
  duration_ms: 0.479315
  ...
# Subtest: L2 lane overrides refresh
ok 642 - L2 lane overrides refresh
  ---
  duration_ms: 0.32474
  ...
# Subtest: L3 lane exclusions have no tier
ok 643 - L3 lane exclusions have no tier
  ---
  duration_ms: 0.475638
  ...
# Subtest: L4 lane off switch and null default
ok 644 - L4 lane off switch and null default
  ---
  duration_ms: 0.337795
  ...
# Subtest: L5 lane order never stamped first
ok 645 - L5 lane order never stamped first
  ---
  duration_ms: 0.533869
  ...
# Subtest: R1 TICKLER beats older ROTTEN
ok 646 - R1 TICKLER beats older ROTTEN
  ---
  duration_ms: 0.418008
  ...
# Subtest: R2 tickler orders by due date then path and line
ok 647 - R2 tickler orders by due date then path and line
  ---
  duration_ms: 0.818333
  ...
# Subtest: missing created sorts after dated peers
ok 648 - missing created sorts after dated peers
  ---
  duration_ms: 0.966325
  ...
# Subtest: B1 upkeep counts outside the lanes
ok 649 - B1 upkeep counts outside the lanes
  ---
  duration_ms: 3.080621
  ...
# Subtest: review model meter uses upkeep and exposes refreshed
ok 650 - review model meter uses upkeep and exposes refreshed
  ---
  duration_ms: 0.408219
  ...
# Subtest: RC1 arrived: past scheduled walks RECURRING with lane and null state
ok 651 - RC1 arrived: past scheduled walks RECURRING with lane and null state
  ---
  duration_ms: 3.062316
  ...
# Subtest: RC2 arrives today: due today with zero days overdue
ok 652 - RC2 arrives today: due today with zero days overdue
  ---
  duration_ms: 0.290444
  ...
# Subtest: RC3 not yet: future scheduled walks nowhere
ok 653 - RC3 not yet: future scheduled walks nowhere
  ---
  duration_ms: 0.218247
  ...
# Subtest: RC4 due only, past: the due date is the occurrence
ok 654 - RC4 due only, past: the due date is the occurrence
  ---
  duration_ms: 0.213347
  ...
# Subtest: RC5 due only, future: walks nowhere
ok 655 - RC5 due only, future: walks nowhere
  ---
  duration_ms: 0.245769
  ...
# Subtest: RC6 earliest date wins across start and due
ok 656 - RC6 earliest date wins across start and due
  ---
  duration_ms: 0.253834
  ...
# Subtest: RC7 undated: no occurrence, no tier
ok 657 - RC7 undated: no occurrence, no tier
  ---
  duration_ms: 0.286647
  ...
# Subtest: RC8 lanes: recurring lane rows keep their lane with null state
ok 658 - RC8 lanes: recurring lane rows keep their lane with null state
  ---
  duration_ms: 0.46098
  ...
# Subtest: RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
ok 659 - RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
  ---
  duration_ms: 1.520533
  ...
# Subtest: RC10 checklist wins: a recurring chore stays in its checklist tier
ok 660 - RC10 checklist wins: a recurring chore stays in its checklist tier
  ---
  duration_ms: 0.406356
  ...
# Subtest: RC11 a stray stamp is ignored: recurring with null state
ok 661 - RC11 a stray stamp is ignored: recurring with null state
  ---
  duration_ms: 0.329459
  ...
# Subtest: RC12 order and counts: due_on, then path, then line; recurring adds no due
ok 662 - RC12 order and counts: due_on, then path, then line; recurring adds no due
  ---
  duration_ms: 1.075363
  ...
# Subtest: recurring rows adapt due and start from Tasks fields and inline fallbacks
ok 663 - recurring rows adapt due and start from Tasks fields and inline fallbacks
  ---
  duration_ms: 1.171637
  ...
# Subtest: status view counts RECURRING as a due commitment tier
ok 664 - status view counts RECURRING as a due commitment tier
  ---
  duration_ms: 0.322225
  ...
# Subtest: footer groups, entry view, and legend cover RECURRING
ok 665 - footer groups, entry view, and legend cover RECURRING
  ---
  duration_ms: 0.766423
  ...
# Subtest: a stale-stamped recurring row marks due with the resolve hint
ok 666 - a stale-stamped recurring row marks due with the resolve hint
  ---
  duration_ms: 0.852637
  ...
# Subtest: freshness namespace v12 keeps recurring and removes reference capabilities
ok 667 - freshness namespace v12 keeps recurring and removes reference capabilities
  ---
  duration_ms: 3.799784
  ...
# Subtest: hidden recurring ^ref keeps ordinary visibility (Rust parity)
ok 668 - hidden recurring ^ref keeps ordinary visibility (Rust parity)
  ---
  duration_ms: 0.998667
  ...
# Subtest: bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
ok 669 - bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
  ---
  duration_ms: 3.726214
  ...
# Subtest: day numbers stay calendar-local across a DST boundary
ok 670 - day numbers stay calendar-local across a DST boundary
  ---
  duration_ms: 0.469587
  ...
# Subtest: reviewModel shares counts, meter, tooltip, and severity
ok 671 - reviewModel shares counts, meter, tooltip, and severity
  ---
  duration_ms: 0.456401
  ...
# Subtest: memo serves warm map hits and misses use the per-row evaluator
ok 672 - memo serves warm map hits and misses use the per-row evaluator
  ---
  duration_ms: 7.340352
  ...
# Subtest: config snapshot caches the parse and invalidates explicitly
ok 673 - config snapshot caches the parse and invalidates explicitly
  ---
  duration_ms: 1.350849
  ...
# Subtest: review chips share the model with severity classes
ok 674 - review chips share the model with severity classes
  ---
  duration_ms: 1.040707
  ...
# Subtest: warm lookups reuse one snapshot without re-reading config
ok 675 - warm lookups reuse one snapshot without re-reading config
  ---
  duration_ms: 1.961114
  ...
# Subtest: same-array cache updates and Today changes rebuild the memo
ok 676 - same-array cache updates and Today changes rebuild the memo
  ---
  duration_ms: 3.503027
  ...
# Subtest: duplicate block IDs keep each row's own classification
ok 677 - duplicate block IDs keep each row's own classification
  ---
  duration_ms: 3.276223
  ...
# Subtest: line identity separates same-path rows without block IDs
ok 678 - line identity separates same-path rows without block IDs
  ---
  duration_ms: 1.284772
  ...
# Subtest: interval lookup serves the cached interval with one memo acquisition
ok 679 - interval lookup serves the cached interval with one memo acquisition
  ---
  duration_ms: 1.292117
  ...
# Subtest: S1 new through S4 overdue
ok 680 - S1 new through S4 overdue
  ---
  duration_ms: 2.853266
  ...
# Subtest: S5 task beats note, S6 note beats config, S7 config
ok 681 - S5 task beats note, S6 note beats config, S7 config
  ---
  duration_ms: 0.732117
  ...
# Subtest: S8 invalid overrides fall through with lints
ok 682 - S8 invalid overrides fall through with lints
  ---
  duration_ms: 0.391818
  ...
# Subtest: S9 malformed and S10 future stamps read as new
ok 683 - S9 malformed and S10 future stamps read as new
  ---
  duration_ms: 0.220621
  ...
# Subtest: S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
ok 684 - S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
  ---
  duration_ms: 0.339318
  ...
# Subtest: S13 out-of-scope rows read null
ok 685 - S13 out-of-scope rows read null
  ---
  duration_ms: 0.31423
  ...
# Subtest: S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
ok 686 - S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
  ---
  duration_ms: 1.33532
  ...
# Subtest: S15 counts (updated): upkeep outside the lanes drives the budget
ok 687 - S15 counts (updated): upkeep outside the lanes drives the budget
  ---
  duration_ms: 1.201323
  ...
# Subtest: config coercion keeps defaults, flags invalid, ignores unknown keys
ok 688 - config coercion keeps defaults, flags invalid, ignores unknown keys
  ---
  duration_ms: 1.316573
  ...
# Subtest: loadFreshnessConfig reads the block with plan-style injectables
ok 689 - loadFreshnessConfig reads the block with plan-style injectables
  ---
  duration_ms: 0.892965
  ...
# Subtest: interval precedence is task, note, config, default
ok 690 - interval precedence is task, note, config, default
  ---
  duration_ms: 0.22537
  ...
# Subtest: intervalForLine covers every source with its Ready fallback
ok 691 - intervalForLine covers every source with its Ready fallback
  ---
  duration_ms: 0.836126
  ...
# Subtest: project tracking stays special while reference tasks use ordinary Ready freshness
ok 692 - project tracking stays special while reference tasks use ordinary Ready freshness
  ---
  duration_ms: 5.224875
  ...
# Subtest: reference tasks match ordinary interval precedence and lane behavior
ok 693 - reference tasks match ordinary interval precedence and lane behavior
  ---
  duration_ms: 2.953689
  ...
# Subtest: obsolete reference interval keys are ignored and project config still validates
ok 694 - obsolete reference interval keys are ignored and project config still validates
  ---
  duration_ms: 0.904607
  ...
# Subtest: references use ordinary keep decisions and the nine-tier queue shape
ok 695 - references use ordinary keep decisions and the nine-tier queue shape
  ---
  duration_ms: 1.884157
  ...
# Subtest: CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
ok 696 - CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
  ---
  duration_ms: 3.331849
  ...
# Subtest: CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
ok 697 - CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
  ---
  duration_ms: 2.405591
  ...
# Subtest: freshness namespace v12 retains the tracker capability contract
ok 698 - freshness namespace v12 retains the tracker capability contract
  ---
  duration_ms: 6.326888
  ...
# Subtest: UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
ok 699 - UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
  ---
  duration_ms: 2.889085
  ...
# Subtest: UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
ok 700 - UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
  ---
  duration_ms: 0.438828
  ...
# Subtest: UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
ok 701 - UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
  ---
  duration_ms: 0.295965
  ...
# Subtest: UB11 scheduled wins a tie with the unblock date
ok 702 - UB11 scheduled wins a tie with the unblock date
  ---
  duration_ms: 0.275877
  ...
# Subtest: unblocked reader takes the latest valid duplicate and reports malformed values
ok 703 - unblocked reader takes the latest valid duplicate and reports malformed values
  ---
  duration_ms: 0.261159
  ...
# Subtest: UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
ok 704 - UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
  ---
  duration_ms: 0.411075
  ...
# Subtest: UB14 TICKLERs with the same due date sort only by path and line
ok 705 - UB14 TICKLERs with the same due date sort only by path and line
  ---
  duration_ms: 1.395183
  ...
# Subtest: UB15 a scheduled ^prj resurfaces in PROJECTS
ok 706 - UB15 a scheduled ^prj resurfaces in PROJECTS
  ---
  duration_ms: 0.195863
  ...
# Subtest: an active-note Pomodoro target still jumps and centers immediately
ok 707 - an active-note Pomodoro target still jumps and centers immediately
  ---
  duration_ms: 9.950214
  ...
# Subtest: Ctrl+9 from an unpinned daily copy switches to the pinned home tab
ok 708 - Ctrl+9 from an unpinned daily copy switches to the pinned home tab
  ---
  duration_ms: 3.092492
  ...
# Subtest: Ctrl+9 on the pinned daily tab jumps in place when a copy exists
ok 709 - Ctrl+9 on the pinned daily tab jumps in place when a copy exists
  ---
  duration_ms: 1.234136
  ...
# Subtest: Ctrl+9 switches daily copies without a Pomodoros section and stays quiet
ok 710 - Ctrl+9 switches daily copies without a Pomodoros section and stays quiet
  ---
  duration_ms: 1.119567
  ...
# Subtest: Ctrl+9 keeps the active daily tab when equal-ranked copies exist
ok 711 - Ctrl+9 keeps the active daily tab when equal-ranked copies exist
  ---
  duration_ms: 1.425011
  ...
# Subtest: Ctrl+9 from a sidebar daily copy switches to a main-area home tab
ok 712 - Ctrl+9 from a sidebar daily copy switches to a main-area home tab
  ---
  duration_ms: 1.029365
  ...
# Subtest: the first fallback press only opens daily and the second press jumps
ok 713 - the first fallback press only opens daily and the second press jumps
  ---
  duration_ms: 1.454457
  ...
# Subtest: a daily note with no target defers its notice until the second press
ok 714 - a daily note with no target defers its notice until the second press
  ---
  duration_ms: 2.597629
  ...
# Subtest: an already-open daily leaf retains its live cursor and viewport
ok 715 - an already-open daily leaf retains its live cursor and viewport
  ---
  duration_ms: 1.947537
  ...
# Subtest: a second press after reused-leaf fallback performs the Pomodoro jump
ok 716 - a second press after reused-leaf fallback performs the Pomodoro jump
  ---
  duration_ms: 1.375575
  ...
# Subtest: the standalone daily-note command activates a reused daily leaf
ok 717 - the standalone daily-note command activates a reused daily leaf
  ---
  duration_ms: 0.672083
  ...
# Subtest: Ctrl+9 loads and reuses a deferred pinned daily tab before falling back
ok 718 - Ctrl+9 loads and reuses a deferred pinned daily tab before falling back
  ---
  duration_ms: 0.739622
  ...
# Subtest: pinned daily tabs win over earlier unpinned tabs
ok 719 - pinned daily tabs win over earlier unpinned tabs
  ---
  duration_ms: 0.690047
  ...
# Subtest: a deferred sidebar daily tab is reused only without a main-area match
ok 720 - a deferred sidebar daily tab is reused only without a main-area match
  ---
  duration_ms: 0.682623
  ...
# Subtest: a deferred sidebar daily tab is reused when there is no main-area match
ok 721 - a deferred sidebar daily tab is reused when there is no main-area match
  ---
  duration_ms: 0.952098
  ...
# Subtest: a deferred non-Markdown daily path is ignored and uses the daily-note fallback
ok 722 - a deferred non-Markdown daily path is ignored and uses the daily-note fallback
  ---
  duration_ms: 0.841306
  ...
# Subtest: the standalone daily-note command reuses a deferred pinned tab
ok 723 - the standalone daily-note command reuses a deferred pinned tab
  ---
  duration_ms: 0.574527
  ...
# Subtest: Ctrl+9 opens the pinned daily tab from a non-Markdown active leaf
ok 724 - Ctrl+9 opens the pinned daily tab from a non-Markdown active leaf
  ---
  duration_ms: 0.604574
  ...
# Subtest: a closed then reopened daily note restores its in-session location
ok 725 - a closed then reopened daily note restores its in-session location
  ---
  duration_ms: 1.431613
  ...
# Subtest: different-path and invalid locations do not leak into a daily note
ok 726 - different-path and invalid locations do not leak into a daily note
  ---
  duration_ms: 1.617808
  ...
# Subtest: out-of-range remembered coordinates are clamped safely
ok 727 - out-of-range remembered coordinates are clamped safely
  ---
  duration_ms: 4.97621
  ...
# Subtest: a rapid second press cancels an older fallback restore
ok 728 - a rapid second press cancels an older fallback restore
  ---
  duration_ms: 1.117955
  ...
# Subtest: navigation and unload clean up daily scroll listeners and deferred work
ok 729 - navigation and unload clean up daily scroll listeners and deferred work
  ---
  duration_ms: 0.956065
  ...
# Subtest: crowded chip: over count is red with tooltip, aria, and names
ok 730 - crowded chip: over count is red with tooltip, aria, and names
  ---
  duration_ms: 1.224057
  ...
# Subtest: crowded chip: calm zero and unavailable dash
ok 731 - crowded chip: calm zero and unavailable dash
  ---
  duration_ms: 0.218978
  ...
# Subtest: crowded chip: names at most five notes
ok 732 - crowded chip: names at most five notes
  ---
  duration_ms: 0.220571
  ...
# Subtest: crowded chip: classes, text, aria, and arrow
ok 733 - crowded chip: classes, text, aria, and arrow
  ---
  duration_ms: 1.616206
  ...
# Subtest: crowded chip: refresh in place keeps the anchor, unload drops it
ok 734 - crowded chip: refresh in place keeps the anchor, unload drops it
  ---
  duration_ms: 0.589446
  ...
# Subtest: anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
ok 735 - anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
  ---
  duration_ms: 0.502409
  ...
# Subtest: ready-notes summary: crowded, calm, and unavailable
ok 736 - ready-notes summary: crowded, calm, and unavailable
  ---
  duration_ms: 0.232884
  ...
# Subtest: ready-notes bar: cap tick and red overflow within 30 cells
ok 737 - ready-notes bar: cap tick and red overflow within 30 cells
  ---
  duration_ms: 0.207376
  ...
# Subtest: ready-notes block: model and render with grid, pills, and footer
ok 738 - ready-notes block: model and render with grid, pills, and footer
  ---
  duration_ms: 1.307577
  ...
# Subtest: ready-notes block: unavailable renders a dash line
ok 739 - ready-notes block: unavailable renders a dash line
  ---
  duration_ms: 0.410234
  ...
# Subtest: heading matcher: fences, level, case, and first-only
ok 740 - heading matcher: fences, level, case, and first-only
  ---
  duration_ms: 0.372061
  ...
# Subtest: heading chip copy: room, full, crowded, exempt, unavailable
ok 741 - heading chip copy: room, full, crowded, exempt, unavailable
  ---
  duration_ms: 0.415674
  ...
# Subtest: heading chip key is stable for equal models
ok 742 - heading chip key is stable for equal models
  ---
  duration_ms: 0.183751
  ...
# Subtest: reading view: appends the chip to the matching h2 only
ok 743 - reading view: appends the chip to the matching h2 only
  ---
  duration_ms: 1.762455
  ...
# Subtest: reading view: no chip for ineligible notes
ok 744 - reading view: no chip for ineligible notes
  ---
  duration_ms: 0.135138
  ...
# Subtest: one live-refresh fan-out reaches every family
ok 745 - one live-refresh fan-out reaches every family
  ---
  duration_ms: 0.873568
  ...
# Subtest: ledger-tools CSS is theme-safe for the new views
ok 746 - ledger-tools CSS is theme-safe for the new views
  ---
  duration_ms: 0.589054
  ...
# Subtest: maxReadyPerNote defaults to 5 and validates 1–999
ok 747 - maxReadyPerNote defaults to 5 and validates 1–999
  ---
  duration_ms: 2.929382
  ...
# Subtest: loadPlanCaps caches on a stat key and detects edits
ok 748 - loadPlanCaps caches on a stat key and detects edits
  ---
  duration_ms: 0.683825
  ...
# Subtest: loadPlanCaps handles deletion, invalid edits, and recovery
ok 749 - loadPlanCaps handles deletion, invalid edits, and recovery
  ---
  duration_ms: 0.708382
  ...
# Subtest: loadPlanCaps without statSync reads through uncached
ok 750 - loadPlanCaps without statSync reads through uncached
  ---
  duration_ms: 0.346992
  ...
# Subtest: noteFrontmatter resolves through getFileCache, not getCache
ok 751 - noteFrontmatter resolves through getFileCache, not getCache
  ---
  duration_ms: 0.77484
  ...
# Subtest: task_refresh applies through the shared reader
ok 752 - task_refresh applies through the shared reader
  ---
  duration_ms: 3.622205
  ...
# Subtest: noteReadyKindFromType covers every R11 form
ok 753 - noteReadyKindFromType covers every R11 form
  ---
  duration_ms: 0.533077
  ...
# Subtest: noteReadyStatusLabel mirrors ProjectStatus::parse
ok 754 - noteReadyStatusLabel mirrors ProjectStatus::parse
  ---
  duration_ms: 0.279664
  ...
# Subtest: noteReadyParentStem strips alias, heading, and path
ok 755 - noteReadyParentStem strips alias, heading, and path
  ---
  duration_ms: 0.316825
  ...
# Subtest: parseNoteReadyCap covers every R8 form
ok 756 - parseNoteReadyCap covers every R8 form
  ---
  duration_ms: 0.74934
  ...
# Subtest: R1: 6 tasks at the default cap are crowded with over_by 1
ok 757 - R1: 6 tasks at the default cap are crowded with over_by 1
  ---
  duration_ms: 7.581173
  ...
# Subtest: R2: 5 tasks are full with no lint
ok 758 - R2: 5 tasks are full with no lint
  ---
  duration_ms: 5.293835
  ...
# Subtest: R3: hidden, future, blocked, and non-TODO rows never count
ok 759 - R3: hidden, future, blocked, and non-TODO rows never count
  ---
  duration_ms: 2.734719
  ...
# Subtest: R4: make-up splits 1 ready + 1 new + 1 rotten
ok 760 - R4: make-up splits 1 ready + 1 new + 1 rotten
  ---
  duration_ms: 1.823952
  ...
# Subtest: R5: recurring rows are excluded but tallied
ok 761 - R5: recurring rows are excluded but tallied
  ---
  duration_ms: 1.098247
  ...
# Subtest: R6: a visible ^prj task never counts
ok 762 - R6: a visible ^prj task never counts
  ---
  duration_ms: 0.910368
  ...
# Subtest: R7: daily, untyped, template, done, and dash rows are absent
ok 763 - R7: daily, untyped, template, done, and dash rows are absent
  ---
  duration_ms: 1.525422
  ...
# Subtest: R8: ready_cap forms map to cap, exempt, or lint-then-default
ok 764 - R8: ready_cap forms map to cap, exempt, or lint-then-default
  ---
  duration_ms: 2.542734
  ...
# Subtest: R9: a parent with two children counts 3
ok 765 - R9: a parent with two children counts 3
  ---
  duration_ms: 1.21505
  ...
# Subtest: R10: terminal projects are not capped and lint once
ok 766 - R10: terminal projects are not capped and lint once
  ---
  duration_ms: 5.299435
  ...
# Subtest: R11: every type form and nested folders are eligible
ok 767 - R11: every type form and nested folders are eligible
  ---
  duration_ms: 1.740062
  ...
# Subtest: R12: stamping a NEW task keeps the count and moves the make-up
ok 768 - R12: stamping a NEW task keeps the count and moves the make-up
  ---
  duration_ms: 2.643517
  ...
# Subtest: R13: a Today-linked task still counts
ok 769 - R13: a Today-linked task still counts
  ---
  duration_ms: 0.67099
  ...
# Subtest: R14: max_ready_per_note 3 caps others while ready_cap 8 holds
ok 770 - R14: max_ready_per_note 3 caps others while ready_cap 8 holds
  ---
  duration_ms: 2.246117
  ...
# Subtest: api.noteReady is frozen at version 1 under api v3
ok 771 - api.noteReady is frozen at version 1 under api v3
  ---
  duration_ms: 0.257622
  ...
# Subtest: counted and inCrowdedNote resolve per task
ok 772 - counted and inCrowdedNote resolve per task
  ---
  duration_ms: 1.489533
  ...
# Subtest: groupLabel ranks crowded notes by excess
ok 773 - groupLabel ranks crowded notes by excess
  ---
  duration_ms: 4.409519
  ...
# Subtest: snapshot sorts crowded, full, room, empty, exempt and splits totals
ok 774 - snapshot sorts crowded, full, room, empty, exempt and splits totals
  ---
  duration_ms: 5.964094
  ...
# Subtest: missing Tasks data and a cold cache are unavailable, never zero
ok 775 - missing Tasks data and a cold cache are unavailable, never zero
  ---
  duration_ms: 1.205661
  ...
# Subtest: throwing Tasks guards never throw
ok 776 - throwing Tasks guards never throw
  ---
  duration_ms: 0.787974
  ...
# Subtest: snapshot reuses the memo without reparsing or re-walking
ok 777 - snapshot reuses the memo without reparsing or re-walking
  ---
  duration_ms: 1.066024
  ...
# Subtest: a task edit rebuilds through the cache-update handler
ok 778 - a task edit rebuilds through the cache-update handler
  ---
  duration_ms: 1.281657
  ...
# Subtest: a ready_cap edit rebuilds and fires the query-refresh trigger
ok 779 - a ready_cap edit rebuilds and fires the query-refresh trigger
  ---
  duration_ms: 0.934594
  ...
# Subtest: rename and delete move the eligibility entry
ok 780 - rename and delete move the eligibility entry
  ---
  duration_ms: 1.08951
  ...
# Subtest: day rollover rebuilds the snapshot date
ok 781 - day rollover rebuilds the snapshot date
  ---
  duration_ms: 0.891953
  ...
# Subtest: a config edit flows through the stat cache
ok 782 - a config edit flows through the stat cache
  ---
  duration_ms: 1.77056
  ...
# Subtest: untyped and non-markdown vault events are no-ops
ok 783 - untyped and non-markdown vault events are no-ops
  ---
  duration_ms: 0.662104
  ...
# Subtest: memo hits never re-walk the vault
ok 784 - memo hits never re-walk the vault
  ---
  duration_ms: 51.996568
  ...
# Subtest: the startup storm is linear
ok 785 - the startup storm is linear
  ---
  duration_ms: 22.585255
  ...
# Subtest: the first resolved event forces one rebuild and later ones do not
ok 786 - the first resolved event forces one rebuild and later ones do not
  ---
  duration_ms: 1.282939
  ...
# Subtest: noteReadyEvaluate is pure and mirrors the Rust totals
ok 787 - noteReadyEvaluate is pure and mirrors the Rust totals
  ---
  duration_ms: 0.255277
  ...
# Subtest: conformance: merged name with duplicate
ok 788 - conformance: merged name with duplicate
  ---
  duration_ms: 4.616904
  ...
# Subtest: conformance: link forms and exclusions
ok 789 - conformance: link forms and exclusions
  ---
  duration_ms: 1.068029
  ...
# Subtest: conformance: unnamed placeholders
ok 790 - conformance: unnamed placeholders
  ---
  duration_ms: 0.505666
  ...
# Subtest: conformance: subheading in the section
ok 791 - conformance: subheading in the section
  ---
  duration_ms: 0.313478
  ...
# Subtest: conformance: open inventory label
ok 792 - conformance: open inventory label
  ---
  duration_ms: 0.490065
  ...
# Subtest: conformance: over the cap
ok 793 - conformance: over the cap
  ---
  duration_ms: 0.305523
  ...
# Subtest: conformance: cancelled and completed entries
ok 794 - conformance: cancelled and completed entries
  ---
  duration_ms: 0.375026
  ...
# Subtest: exactly at the cap is fine
ok 795 - exactly at the cap is fine
  ---
  duration_ms: 0.242533
  ...
# Subtest: no Pomodoros section degrades to an empty budget
ok 796 - no Pomodoros section degrades to an empty budget
  ---
  duration_ms: 0.633208
  ...
# Subtest: fenced code never counts
ok 797 - fenced code never counts
  ---
  duration_ms: 0.781341
  ...
# Subtest: highlight is the first open non-exempt entry; running is the timed one
ok 798 - highlight is the first open non-exempt entry; running is the timed one
  ---
  duration_ms: 0.574597
  ...
# Subtest: coercePlanCaps ignores a legacy max_now instead of failing
ok 799 - coercePlanCaps ignores a legacy max_now instead of failing
  ---
  duration_ms: 0.451892
  ...
# Subtest: parsePlanCaps defaults, overrides, and invalid fallbacks
ok 800 - parsePlanCaps defaults, overrides, and invalid fallbacks
  ---
  duration_ms: 0.316915
  ...
# Subtest: loadPlanCaps falls back to defaults without fs
ok 801 - loadPlanCaps falls back to defaults without fs
  ---
  duration_ms: 0.435872
  ...
# Subtest: loadPlanCaps falls back to defaults on mobile
ok 802 - loadPlanCaps falls back to defaults on mobile
  ---
  duration_ms: 0.255006
  ...
# Subtest: loadPlanCaps reads plan: and flags invalid values
ok 803 - loadPlanCaps reads plan: and flags invalid values
  ---
  duration_ms: 0.417076
  ...
# Subtest: planBlockTargetPath prefers the containing daily note
ok 804 - planBlockTargetPath prefers the containing daily note
  ---
  duration_ms: 0.745252
  ...
# Subtest: planBlockModel degrades to placeholders, never an error
ok 805 - planBlockModel degrades to placeholders, never an error
  ---
  duration_ms: 0.891302
  ...
# Subtest: planBlockModel renders chips, themes, and lints
ok 806 - planBlockModel renders chips, themes, and lints
  ---
  duration_ms: 1.053251
  ...
# Subtest: planBlockModel adds lane cap lints when a lane is over
ok 807 - planBlockModel adds lane cap lints when a lane is over
  ---
  duration_ms: 0.730204
  ...
# Subtest: plugin exposes the versioned api and registers the bob-plan block
ok 808 - plugin exposes the versioned api and registers the bob-plan block
  ---
  duration_ms: 6.732192
  ...
# Subtest: invalid plan block falls back to full defaults
ok 809 - invalid plan block falls back to full defaults
  ---
  duration_ms: 3.514469
  ...
# Subtest: entries require column-0 dash-space with one status char
ok 810 - entries require column-0 dash-space with one status char
  ---
  duration_ms: 0.353345
  ...
# Subtest: crlf line endings split like lf
ok 811 - crlf line endings split like lf
  ---
  duration_ms: 0.261218
  ...
# Subtest: conformance: empty target means the daily note
ok 812 - conformance: empty target means the daily note
  ---
  duration_ms: 0.210932
  ...
# Subtest: lane predicate matches hide subtags, case, and non-task
ok 813 - lane predicate matches hide subtags, case, and non-task
  ---
  duration_ms: 0.259926
  ...
# Subtest: planBlockModel daily badges follow dashboard section counts
ok 814 - planBlockModel daily badges follow dashboard section counts
  ---
  duration_ms: 2.461378
  ...
# Subtest: planBlockModel keeps a supplied unavailable dashboard budget
ok 815 - planBlockModel keeps a supplied unavailable dashboard budget
  ---
  duration_ms: 0.441633
  ...
# Subtest: work tones: TODAY override and unavailable stay neutral in planBlockModel
ok 816 - work tones: TODAY override and unavailable stay neutral in planBlockModel
  ---
  duration_ms: 0.293631
  ...
# Subtest: shared vector: rollup-archive-review
ok 817 - shared vector: rollup-archive-review
  ---
  duration_ms: 5.92517
  ...
# Subtest: shared vector: review-decisions
ok 818 - shared vector: review-decisions
  ---
  duration_ms: 1.575017
  ...
# Subtest: shared vector: resolution-and-lints
ok 819 - shared vector: resolution-and-lints
  ---
  duration_ms: 1.825014
  ...
# Subtest: shared vector: chips, forecast shares, empty forecasts, and session identity
ok 820 - shared vector: chips, forecast shares, empty forecasts, and session identity
  ---
  duration_ms: 2.070533
  ...
# Subtest: shared vector: split-rounding-and-duration
ok 821 - shared vector: split-rounding-and-duration
  ---
  duration_ms: 0.640593
  ...
# Subtest: shared vector: share-rounding
ok 822 - shared vector: share-rounding
  ---
  duration_ms: 0.395906
  ...
# Subtest: shared vector: daily-review-link
ok 823 - shared vector: daily-review-link
  ---
  duration_ms: 0.339067
  ...
# Subtest: shared vector: rollup-depth-and-parent-shapes
ok 824 - shared vector: rollup-depth-and-parent-shapes
  ---
  duration_ms: 1.04289
  ...
# Subtest: shared vector: unresolved-and-closed-zero
ok 825 - shared vector: unresolved-and-closed-zero
  ---
  duration_ms: 0.861064
  ...
# Subtest: shared vector: parent-scalar-shapes
ok 826 - shared vector: parent-scalar-shapes
  ---
  duration_ms: 0.661793
  ...
# Subtest: dedicated link parser keeps embeds and one struck link, but rejects prose
ok 827 - dedicated link parser keeps embeds and one struck link, but rejects prose
  ---
  duration_ms: 0.254616
  ...
# Subtest: FNV-1a fallback for job maps to the pinned magenta slot
ok 828 - FNV-1a fallback for job maps to the pinned magenta slot
  ---
  duration_ms: 0.112124
  ...
# Subtest: rollup and area-color lints are reported once per note
ok 829 - rollup and area-color lints are reported once per note
  ---
  duration_ms: 0.380877
  ...
# Subtest: chip DOM exposes forecast, hue, accessible text, and tooltip
ok 830 - chip DOM exposes forecast, hue, accessible text, and tooltip
  ---
  duration_ms: 0.233626
  ...
# Subtest: Reading view appends a forecast chip before its Task Link list
ok 831 - Reading view appends a forecast chip before its Task Link list
  ---
  duration_ms: 4.711855
  ...
# Subtest: Live Preview places a chip widget at the end of the Pomodoro line
ok 832 - Live Preview places a chip widget at the end of the Pomodoro line
  ---
  duration_ms: 0.666993
  ...
# Subtest: Live Preview skips chips in Source mode
ok 833 - Live Preview skips chips in Source mode
  ---
  duration_ms: 0.167429
  ...
# Subtest: Reading view finds embedded Task Links via src
ok 834 - Reading view finds embedded Task Links via src
  ---
  duration_ms: 0.411676
  ...
# Subtest: Obsidian frontmatter shapes unwrap nested wikilink arrays
ok 835 - Obsidian frontmatter shapes unwrap nested wikilink arrays
  ---
  duration_ms: 0.148303
  ...
# Subtest: parser accepts the PM1-PM5 conformance vectors verbatim
ok 836 - parser accepts the PM1-PM5 conformance vectors verbatim
  ---
  duration_ms: 1.782794
  ...
# Subtest: parser rejects the PM7-PM12 conformance vectors verbatim
ok 837 - parser rejects the PM7-PM12 conformance vectors verbatim
  ---
  duration_ms: 0.275276
  ...
# Subtest: PM6 with the ladder unknown omits P-labels instead of guessing
ok 838 - PM6 with the ladder unknown omits P-labels instead of guessing
  ---
  duration_ms: 0.183841
  ...
# Subtest: PM13-PM17 ladder and line variants hold
ok 839 - PM13-PM17 ladder and line variants hold
  ---
  duration_ms: 0.316825
  ...
# Subtest: no model output contains a double colon
ok 840 - no model output contains a double colon
  ---
  duration_ms: 0.751795
  ...
# Subtest: element structure and the decorative/inheritColor options
ok 841 - element structure and the decorative/inheritColor options
  ---
  duration_ms: 0.326403
  ...
# Subtest: Live Preview decorations fold space, reveal, and refuse
ok 842 - Live Preview decorations fold space, reveal, and refuse
  ---
  duration_ms: 1.308789
  ...
# Subtest: a line with fresh and priority fields gets a disjoint decoration
ok 843 - a line with fresh and priority fields gets a disjoint decoration
  ---
  duration_ms: 0.202627
  ...
# Subtest: widget mousedown reveals the field at the folded offset
ok 844 - widget mousedown reveals the field at the folded offset
  ---
  duration_ms: 0.595467
  ...
# Subtest: rendered views split task nodes and skip exclusions
ok 845 - rendered views split task nodes and skip exclusions
  ---
  duration_ms: 1.477721
  ...
# Subtest: ladder coercion is lenient: valid, partial, and unknown
ok 846 - ladder coercion is lenient: valid, partial, and unknown
  ---
  duration_ms: 0.424541
  ...
# Subtest: ladder snapshot reads the file and reuses the cache
ok 847 - ladder snapshot reads the file and reuses the cache
  ---
  duration_ms: 1.79735
  ...
# Subtest: ladder snapshot degrades on missing files and parse errors
ok 848 - ladder snapshot degrades on missing files and parse errors
  ---
  duration_ms: 0.910478
  ...
# Subtest: ladder snapshot is unknown on mobile
ok 849 - ladder snapshot is unknown on mobile
  ---
  duration_ms: 19.226844
  ...
# Subtest: api.priorityMarks v1 is additive, sync, and never throwing
ok 850 - api.priorityMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 5.286421
  ...
# Subtest: session toggle and onload wiring
ok 851 - session toggle and onload wiring
  ---
  duration_ms: 0.81225
  ...
# Subtest: styles.css contract: masks, both hosts, repair flag, resting
ok 852 - styles.css contract: masks, both hosts, repair flag, resting
  ---
  duration_ms: 0.728561
  ...
# Subtest: P1/P3/P4: open entries mark plain and aliased links
ok 853 - P1/P3/P4: open entries mark plain and aliased links
  ---
  duration_ms: 2.201323
  ...
# Subtest: P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
ok 854 - P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
  ---
  duration_ms: 2.864247
  ...
# Subtest: P5: closed entries never mark, even with 🍅 history
ok 855 - P5: closed entries never mark, even with 🍅 history
  ---
  duration_ms: 0.807191
  ...
# Subtest: P6/P7: embedded and struck links never mark
ok 856 - P6/P7: embedded and struck links never mark
  ---
  duration_ms: 0.293931
  ...
# Subtest: P8: both trailing-\# move-only forms mark
ok 857 - P8: both trailing-\# move-only forms mark
  ---
  duration_ms: 0.282269
  ...
# Subtest: P9: nested and prose-mixed links never mark
ok 858 - P9: nested and prose-mixed links never mark
  ---
  duration_ms: 0.190103
  ...
# Subtest: P10: fenced, off-section, and off-note links never mark
ok 859 - P10: fenced, off-section, and off-note links never mark
  ---
  duration_ms: 0.441463
  ...
# Subtest: P11: unresolved targets and non-task blocks get no mark
ok 860 - P11: unresolved targets and non-task blocks get no mark
  ---
  duration_ms: 0.52343
  ...
# Subtest: P13: a same-note target reads the live doc
ok 861 - P13: a same-note target reads the live doc
  ---
  duration_ms: 0.805568
  ...
# Subtest: P14: expect() wins until the cache agrees or 4 s pass
ok 862 - P14: expect() wins until the cache agrees or 4 s pass
  ---
  duration_ms: 0.979941
  ...
# Subtest: tooltip, element structure, and eq
ok 863 - tooltip, element structure, and eq
  ---
  duration_ms: 0.304541
  ...
# Subtest: Live Preview places one widget at each In Progress link
ok 864 - Live Preview places one widget at each In Progress link
  ---
  duration_ms: 0.53998
  ...
# Subtest: widget mousedown places the cursor at the link start
ok 865 - widget mousedown places the cursor at the link start
  ---
  duration_ms: 0.414963
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
ok 866 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 0.50245
  ...
# Subtest: Reading view marks In Progress rows and dedupes
ok 867 - Reading view marks In Progress rows and dedupes
  ---
  duration_ms: 1.363493
  ...
# Subtest: Reading view refuses every non-mark row
ok 868 - Reading view refuses every non-mark row
  ---
  duration_ms: 1.208959
  ...
# Subtest: Reading view allows the 🍅 prefix and the trailing \# marker
ok 869 - Reading view allows the 🍅 prefix and the trailing \# marker
  ---
  duration_ms: 0.349357
  ...
# Subtest: api.progressMarks v1 is additive, sync, and never throwing
ok 870 - api.progressMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.779007
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 871 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 0.920968
  ...
# Subtest: changed-file and rollover refreshes
ok 872 - changed-file and rollover refreshes
  ---
  duration_ms: 2.699924
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 873 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.111272
  ...
# Subtest: styles.css contract: glyph, box, motion, toggle, calm
ok 874 - styles.css contract: glyph, box, motion, toggle, calm
  ---
  duration_ms: 0.807611
  ...
# Subtest: the board registers its code block processor and the Open Reading Board command
ok 875 - the board registers its code block processor and the Open Reading Board command
  ---
  duration_ms: 5.912506
  ...
# Subtest: four lanes render with counts, list and listitem roles, and one hint
ok 876 - four lanes render with counts, list and listitem roles, and one hint
  ---
  duration_ms: 16.96192
  ...
# Subtest: awake cards show kind, topic, added mark, counts, priority, and the pending-sync star
ok 877 - awake cards show kind, topic, added mark, counts, priority, and the pending-sync star
  ---
  duration_ms: 3.328212
  ...
# Subtest: a path-valued Bob audio field produces exactly one visible music marker
ok 878 - a path-valued Bob audio field produces exactly one visible music marker
  ---
  duration_ms: 2.041136
  ...
# Subtest: Snoozed shows Waking, date groups, and Waiting-on rows with their reasons
ok 879 - Snoozed shows Waking, date groups, and Waiting-on rows with their reasons
  ---
  duration_ms: 3.285132
  ...
# Subtest: TODAY pills float linked cards first, and never appear without a ready Today cache
ok 880 - TODAY pills float linked cards first, and never appear without a ready Today cache
  ---
  duration_ms: 5.160913
  ...
# Subtest: the PDF button needs the nav member, macOS, and a source_pdf
ok 881 - the PDF button needs the nav member, macOS, and a source_pdf
  ---
  duration_ms: 13.801926
  ...
# Subtest: click, modifier-click, middle-click, and the Task button route to openLinkText
ok 882 - click, modifier-click, middle-click, and the Task button route to openLinkText
  ---
  duration_ms: 2.109377
  ...
# Subtest: the board is one Tab stop and every key moves or acts
ok 883 - the board is one Tab stop and every key moves or acts
  ---
  duration_ms: 23.994313
  ...
# Subtest: movement targets stay inside the lanes that show cards
ok 884 - movement targets stay inside the lanes that show cards
  ---
  duration_ms: 0.638238
  ...
# Subtest: hovering a Waiting-on row outlines its prerequisite card on the board
ok 885 - hovering a Waiting-on row outlines its prerequisite card on the board
  ---
  duration_ms: 1.610675
  ...
# Subtest: the board never calls a vault write API, in the source or in any gesture
ok 886 - the board never calls a vault write API, in the source or in any gesture
  ---
  duration_ms: 10.593863
  ...
# Subtest: a repaint keeps focus by note path and each lane's scroll position
ok 887 - a repaint keeps focus by note path and each lane's scroll position
  ---
  duration_ms: 3.011889
  ...
# Subtest: a task move and topic/type update repaint handlers while preserving focus and scroll
ok 888 - a task move and topic/type update repaint handlers while preserving focus and scroll
  ---
  duration_ms: 3.021308
  ...
# Subtest: prerequisite identity changes repaint highlighting even when reason text is unchanged
ok 889 - prerequisite identity changes repaint highlighting even when reason text is unchanged
  ---
  duration_ms: 4.333894
  ...
# Subtest: an unchanged board is not repainted; only the data time updates in place
ok 890 - an unchanged board is not repainted; only the data time updates in place
  ---
  duration_ms: 6.733624
  ...
# Subtest: a Today cache change repaints boards from cached data without spawning bob
ok 891 - a Today cache change repaints boards from cached data without spawning bob
  ---
  duration_ms: 6.321036
  ...
# Subtest: first paint is a skeleton in the real grid, then the board without a layout jump
ok 892 - first paint is a skeleton in the real grid, then the board without a layout jump
  ---
  duration_ms: 7.077771
  ...
# Subtest: failures without a frame render an actionable card with Retry
ok 893 - failures without a frame render an actionable card with Retry
  ---
  duration_ms: 22.434937
  ...
# Subtest: a failed manual refresh keeps the last frame and says why with Retry
ok 894 - a failed manual refresh keeps the last frame and says why with Retry
  ---
  duration_ms: 5.833946
  ...
# Subtest: metadata revalidation delivers a silent stale-frame error and recovery updates freshness
ok 895 - metadata revalidation delivers a silent stale-frame error and recovery updates freshness
  ---
  duration_ms: 8.977839
  ...
# Subtest: stale-cache mount refresh failures reach the mounted view
ok 896 - stale-cache mount refresh failures reach the mounted view
  ---
  duration_ms: 6.384108
  ...
# Subtest: unload during a fetch prevents late repaint and queued spawns
ok 897 - unload during a fetch prevents late repaint and queued spawns
  ---
  duration_ms: 5.339652
  ...
# Subtest: in-flight edits and forced refreshes coalesce without dropping mounted fences
ok 898 - in-flight edits and forced refreshes coalesce without dropping mounted fences
  ---
  duration_ms: 12.587369
  ...
# Subtest: manual refresh shows a busy state until the result lands, then announces it
ok 899 - manual refresh shows a busy state until the result lands, then announces it
  ---
  duration_ms: 3.172947
  ...
# Subtest: an older bob without blocked_by falls back to Waiting-on with one lint line
ok 900 - an older bob without blocked_by falls back to Waiting-on with one lint line
  ---
  duration_ms: 3.588962
  ...
# Subtest: an empty queue shows bob's own phrase instead of lanes
ok 901 - an empty queue shows bob's own phrase instead of lanes
  ---
  duration_ms: 1.06344
  ...
# Subtest: fence options reach the fetch and bad options show as muted lint lines
ok 902 - fence options reach the fetch and bad options show as muted lint lines
  ---
  duration_ms: 3.682269
  ...
# Subtest: Snoozed collapses per source path, leaves the key order, and survives repaints
ok 903 - Snoozed collapses per source path, leaves the key order, and survives repaints
  ---
  duration_ms: 8.321875
  ...
# Subtest: unloading a block releases its view, and teardown clears the session state
ok 904 - unloading a block releases its view, and teardown clears the session state
  ---
  duration_ms: 1.649378
  ...
# Subtest: reading board stylesheet contract: selectors, layout, tabular-nums, motion, colors
ok 905 - reading board stylesheet contract: selectors, layout, tabular-nums, motion, colors
  ---
  duration_ms: 0.739903
  ...
# Subtest: Reading Board argv carries bob's fixed queue and optional fence filters
ok 906 - Reading Board argv carries bob's fixed queue and optional fence filters
  ---
  duration_ms: 1.547133
  ...
# Subtest: Reading Board decoder accepts the shared bob fixture and normalizes optional fields
ok 907 - Reading Board decoder accepts the shared bob fixture and normalizes optional fields
  ---
  duration_ms: 0.300123
  ...
# Subtest: Reading Board audio presence survives raw JSON decoding and model construction
ok 908 - Reading Board audio presence survives raw JSON decoding and model construction
  ---
  duration_ms: 5.102381
  ...
# Subtest: Reading Board decoder rejects malformed JSON, shapes, schema, and bob errors
ok 909 - Reading Board decoder rejects malformed JSON, shapes, schema, and bob errors
  ---
  duration_ms: 0.246841
  ...
# Subtest: shared bob spawn passes the vault environment, timeout, and buffer
ok 910 - shared bob spawn passes the vault environment, timeout, and buffer
  ---
  duration_ms: 6.020202
  ...
# Subtest: shared bob spawn maps missing binary and timeout failures
ok 911 - shared bob spawn maps missing binary and timeout failures
  ---
  duration_ms: 3.118262
  ...
# Subtest: Reading Board error cards explain not-found, timeout, schema, and bob errors
ok 912 - Reading Board error cards explain not-found, timeout, schema, and bob errors
  ---
  duration_ms: 0.449548
  ...
# Subtest: Reading Board cache returns stale data while revalidating and keeps a four-entry LRU
ok 913 - Reading Board cache returns stale data while revalidating and keeps a four-entry LRU
  ---
  duration_ms: 1.410662
  ...
# Subtest: Reading Board shares identical flights and coalesces one different follow-up
ok 914 - Reading Board shares identical flights and coalesces one different follow-up
  ---
  duration_ms: 1.176987
  ...
# Subtest: Reading Board refresh is mounted-only, debounced, and reacts to rollover and stale active leaves
ok 915 - Reading Board refresh is mounted-only, debounced, and reacts to rollover and stale active leaves
  ---
  duration_ms: 1.063581
  ...
# Subtest: the shared bob output builds the expected four lanes and preserves bob order
ok 916 - the shared bob output builds the expected four lanes and preserves bob order
  ---
  duration_ms: 4.658081
  ...
# Subtest: each status uses its awake lane and every blocked status uses Snoozed
ok 917 - each status uses its awake lane and every blocked status uses Snoozed
  ---
  duration_ms: 0.441212
  ...
# Subtest: Today floats cards by ledger rank only when the cache is ready
ok 918 - Today floats cards by ledger rank only when the cache is ready
  ---
  duration_ms: 1.189862
  ...
# Subtest: Snoozed groups show waking, schedule, dependency, project, return lane, and mark models
ok 919 - Snoozed groups show waking, schedule, dependency, project, return lane, and mark models
  ---
  duration_ms: 0.60756
  ...
# Subtest: schedule groups follow Monday-start weeks through Sunday across month and year ends
ok 920 - schedule groups follow Monday-start weeks through Sunday across month and year ends
  ---
  duration_ms: 0.273011
  ...
# Subtest: older bob output remains visible in Waiting on and explains the missing reasons
ok 921 - older bob output remains visible in Waiting on and explains the missing reasons
  ---
  duration_ms: 0.912572
  ...
# Subtest: fence options accept parent and type lists while turning bad input into lints
ok 922 - fence options accept parent and type lists while turning bad input into lints
  ---
  duration_ms: 1.279973
  ...
# Subtest: kind names, title code spans, and render signatures are deterministic
ok 923 - kind names, title code spans, and render signatures are deterministic
  ---
  duration_ms: 4.203054
  ...
# Subtest: max_ready defaults to 100 for missing, absent, and null values
ok 924 - max_ready defaults to 100 for missing, absent, and null values
  ---
  duration_ms: 8.589026
  ...
# Subtest: max_ready accepts a custom positive cap
ok 925 - max_ready accepts a custom positive cap
  ---
  duration_ms: 0.353254
  ...
# Subtest: max_ready rejects zero, negative, fractions, strings, booleans, and overflow
ok 926 - max_ready rejects zero, negative, fractions, strings, booleans, and overflow
  ---
  duration_ms: 1.328105
  ...
# Subtest: old configurations and legacy max_now still load
ok 927 - old configurations and legacy max_now still load
  ---
  duration_ms: 0.353515
  ...
# Subtest: READY boundary: only a strict excess turns red
ok 928 - READY boundary: only a strict excess turns red
  ---
  duration_ms: 2.677932
  ...
# Subtest: READY custom-cap boundary
ok 929 - READY custom-cap boundary
  ---
  duration_ms: 0.328247
  ...
# Subtest: READY over is independent of the PLAN ledger status
ok 930 - READY over is independent of the PLAN ledger status
  ---
  duration_ms: 6.69935
  ...
# Subtest: READY predicate: statuses, custom TODO symbols, and non-tasks
ok 931 - READY predicate: statuses, custom TODO symbols, and non-tasks
  ---
  duration_ms: 0.281227
  ...
# Subtest: READY predicate: blocked uses the full list, even outside the queue
ok 932 - READY predicate: blocked uses the full list, even outside the queue
  ---
  duration_ms: 0.521395
  ...
# Subtest: READY predicate: past, today, and future schedules
ok 933 - READY predicate: past, today, and future schedules
  ---
  duration_ms: 0.587441
  ...
# Subtest: READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
ok 934 - READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
  ---
  duration_ms: 0.337655
  ...
# Subtest: READY predicate: Today exclusion
ok 935 - READY predicate: Today exclusion
  ---
  duration_ms: 0.179963
  ...
# Subtest: readyTaskVisible excludes hide variants like Tasks
ok 936 - readyTaskVisible excludes hide variants like Tasks
  ---
  duration_ms: 0.170155
  ...
# Subtest: daily and dashboard share the READY element contract
ok 937 - daily and dashboard share the READY element contract
  ---
  duration_ms: 12.720111
  ...
# Subtest: READY placeholder keeps the limit in its tooltip
ok 938 - READY placeholder keeps the limit in its tooltip
  ---
  duration_ms: 0.132914
  ...
# Subtest: READY keyboard and modifier-key navigation
ok 939 - READY keyboard and modifier-key navigation
  ---
  duration_ms: 0.815938
  ...
# Subtest: READY unavailable without Tasks, on Cold/Initializing, or before Today
ok 940 - READY unavailable without Tasks, on Cold/Initializing, or before Today
  ---
  duration_ms: 1.952317
  ...
# Subtest: READY counts a valid empty queue as zero, not unavailable
ok 941 - READY counts a valid empty queue as zero, not unavailable
  ---
  duration_ms: 0.810497
  ...
# Subtest: READY stays compatible with hosts exposing only getTasks()
ok 942 - READY stays compatible with hosts exposing only getTasks()
  ---
  duration_ms: 1.886492
  ...
# Subtest: READY degrades to unavailable when the Today predicate throws
ok 943 - READY degrades to unavailable when the Today predicate throws
  ---
  duration_ms: 0.548157
  ...
# Subtest: READY renders label/value spans for every budget state
ok 944 - READY renders label/value spans for every budget state
  ---
  duration_ms: 1.127331
  ...
# Subtest: READY live refresh keeps the anchor, spans, and handlers
ok 945 - READY live refresh keeps the anchor, spans, and handlers
  ---
  duration_ms: 1.209398
  ...
# Subtest: READY refresh crosses the over-cap boundary and back
ok 946 - READY refresh crosses the over-cap boundary and back
  ---
  duration_ms: 0.589194
  ...
# Subtest: READY refresh crosses the unavailable boundary and back
ok 947 - READY refresh crosses the unavailable boundary and back
  ---
  duration_ms: 2.288849
  ...
# Subtest: READY never assigns the Obsidian text setter
ok 948 - READY never assigns the Obsidian text setter
  ---
  duration_ms: 1.164172
  ...
# Subtest: READY gating excludes review buckets and keeps the partition
ok 949 - READY gating excludes review buckets and keeps the partition
  ---
  duration_ms: 0.27746
  ...
# Subtest: gated READY tooltip carries total lane pressure
ok 950 - gated READY tooltip carries total lane pressure
  ---
  duration_ms: 0.108737
  ...
# Subtest: planBlockModel gates READY and shares the lane tooltip
ok 951 - planBlockModel gates READY and shares the lane tooltip
  ---
  duration_ms: 0.56585
  ...
# Subtest: READY lint appears only on a strict excess
ok 952 - READY lint appears only on a strict excess
  ---
  duration_ms: 2.969109
  ...
# Subtest: READY lint uses a custom cap
ok 953 - READY lint uses a custom cap
  ---
  duration_ms: 0.527156
  ...
# Subtest: lane lints appear in NEXT, PENDING, READY order
ok 954 - lane lints appear in NEXT, PENDING, READY order
  ---
  duration_ms: 1.618781
  ...
# Subtest: READY lint uses the gated count
ok 955 - READY lint uses the gated count
  ---
  duration_ms: 1.18358
  ...
# Subtest: READY lint stays silent while unavailable
ok 956 - READY lint stays silent while unavailable
  ---
  duration_ms: 0.398291
  ...
# Subtest: READY speaks each host's chip language (daily single-tone, dash two-tone)
ok 957 - READY speaks each host's chip language (daily single-tone, dash two-tone)
  ---
  duration_ms: 3.096361
  ...
# Subtest: daily paint carries lane pressure to the shared READY renderer
ok 958 - daily paint carries lane pressure to the shared READY renderer
  ---
  duration_ms: 19.539649
  ...
# Subtest: daily paint degrades to the legacy tooltip without freshness
ok 959 - daily paint degrades to the legacy tooltip without freshness
  ---
  duration_ms: 2.104728
  ...
# Subtest: work tones: READY model carries the displayed-count tone
ok 960 - work tones: READY model carries the displayed-count tone
  ---
  duration_ms: 0.186466
  ...
# Subtest: recurrence helpers are exported and frozen where shaped
ok 961 - recurrence helpers are exported and frozen where shaped
  ---
  duration_ms: 2.266317
  ...
# Subtest: RM1 daily with when done: fold, label, tooltip
ok 962 - RM1 daily with when done: fold, label, tooltip
  ---
  duration_ms: 1.125669
  ...
# Subtest: RM2 non-checklist row without when done still marks
ok 963 - RM2 non-checklist row without when done still marks
  ---
  duration_ms: 0.752857
  ...
# Subtest: RM3 weekday plurals keep the full name
ok 964 - RM3 weekday plurals keep the full name
  ---
  duration_ms: 0.646635
  ...
# Subtest: RM4 monthly ordinals use the written token
ok 965 - RM4 monthly ordinals use the written token
  ---
  duration_ms: 0.4664
  ...
# Subtest: RM5 every N days stays verbatim with its count
ok 966 - RM5 every N days stays verbatim with its count
  ---
  duration_ms: 0.166017
  ...
# Subtest: RM6 weekly, N-week, and yearly forms
ok 967 - RM6 weekly, N-week, and yearly forms
  ---
  duration_ms: 0.394202
  ...
# Subtest: RM7 week lists join with Tue, Fri and weekday alone
ok 968 - RM7 week lists join with Tue, Fri and weekday alone
  ---
  duration_ms: 0.171027
  ...
# Subtest: RM8 unknown rules stay verbatim
ok 969 - RM8 unknown rules stay verbatim
  ---
  duration_ms: 0.584636
  ...
# Subtest: RM9 parens and padded brackets are canonical
ok 970 - RM9 parens and padded brackets are canonical
  ---
  duration_ms: 0.720856
  ...
# Subtest: RM10 case is preserved in the rule and tooltip
ok 971 - RM10 case is preserved in the rule and tooltip
  ---
  duration_ms: 0.319861
  ...
# Subtest: RM11 cursor in the field reveals it, RM12 closed rows still mark
ok 972 - RM11 cursor in the field reveals it, RM12 closed rows still mark
  ---
  duration_ms: 0.309982
  ...
# Subtest: RN1 unreadable rules get no mark
ok 973 - RN1 unreadable rules get no mark
  ---
  duration_ms: 0.881092
  ...
# Subtest: RN2 the checklist guard follows membership, not the glyph slot
ok 974 - RN2 the checklist guard follows membership, not the glyph slot
  ---
  duration_ms: 0.190694
  ...
# Subtest: RN3 code still parses pure but decorates nothing
ok 975 - RN3 code still parses pure but decorates nothing
  ---
  duration_ms: 0.22556
  ...
# Subtest: element anatomy: repeat host, rule, quiet tone, no date
ok 976 - element anatomy: repeat host, rule, quiet tone, no date
  ---
  duration_ms: 0.480727
  ...
# Subtest: family dispatch keeps dates working and sorts adds
ok 977 - family dispatch keeps dates working and sorts adds
  ---
  duration_ms: 0.751465
  ...
# Subtest: Live Preview decorates repeat and respects the guard and code
ok 978 - Live Preview decorates repeat and respects the guard and code
  ---
  duration_ms: 1.05312
  ...
# Subtest: RR1 reading view honors the guard, RO2 rollover skips repeat
ok 979 - RR1 reading view honors the guard, RO2 rollover skips repeat
  ---
  duration_ms: 2.474424
  ...
# Subtest: RA1 api.dateMarks stays dates-only and tooltips never contain ::
ok 980 - RA1 api.dateMarks stays dates-only and tooltips never contain ::
  ---
  duration_ms: 0.416986
  ...
# Subtest: styles.css contract: repeat glyph, ink, resting, repair flag
ok 981 - styles.css contract: repeat glyph, ink, resting, repair flag
  ---
  duration_ms: 0.600397
  ...
# Subtest: LC1 one unlabelled open target renders links-to arrow chip
ok 982 - LC1 one unlabelled open target renders links-to arrow chip
  ---
  duration_ms: 3.008263
  ...
# Subtest: LC2 labelled target carries a pill
ok 983 - LC2 labelled target carries a pill
  ---
  duration_ms: 0.489725
  ...
# Subtest: LC3 closed and archived targets dim without strike; \#hide mutes
ok 984 - LC3 closed and archived targets dim without strike; \#hide mutes
  ---
  duration_ms: 2.457341
  ...
# Subtest: LC4 unresolvable target is a dashed missing chip
ok 985 - LC4 unresolvable target is a dashed missing chip
  ---
  duration_ms: 0.554609
  ...
# Subtest: LC5 LINKED FROM shows the builtin inverse phrase
ok 986 - LC5 LINKED FROM shows the builtin inverse phrase
  ---
  duration_ms: 0.95912
  ...
# Subtest: LC6 LINKED FROM with an unknown label reads chip, label, this
ok 987 - LC6 LINKED FROM with an unknown label reads chip, label, this
  ---
  duration_ms: 0.491498
  ...
# Subtest: LC7 live edges missing from the text append in canonical order
ok 988 - LC7 live edges missing from the text append in canonical order
  ---
  duration_ms: 0.5871
  ...
# Subtest: LC8 stored entries that are no longer live are dashed and uncounted
ok 989 - LC8 stored entries that are no longer live are dashed and uncounted
  ---
  duration_ms: 0.464987
  ...
# Subtest: LC9 three or more closed chips collapse to ✓×N and expand
ok 990 - LC9 three or more closed chips collapse to ✓×N and expand
  ---
  duration_ms: 0.900589
  ...
# Subtest: LC10 labelled rows wrap one entry per visual row
ok 991 - LC10 labelled rows wrap one entry per visual row
  ---
  duration_ms: 1.015748
  ...
# Subtest: LC11 controls need api.relations v1; linked_from_remove calls removeLink(S, T)
ok 992 - LC11 controls need api.relations v1; linked_from_remove calls removeLink(S, T)
  ---
  duration_ms: 1.771993
  ...
# Subtest: LC12 toggle-dependency-chips covers both relation rows
ok 993 - LC12 toggle-dependency-chips covers both relation rows
  ---
  duration_ms: 0.580608
  ...
# Subtest: LC13 malformed and not-a-line rows have no model
ok 994 - LC13 malformed and not-a-line rows have no model
  ---
  duration_ms: 0.194461
  ...
# Subtest: LC14 unsaved editor text refreshes the live model
ok 995 - LC14 unsaved editor text refreshes the live model
  ---
  duration_ms: 15.451186
  ...
# Subtest: Live Preview decorates relation rows from the index
ok 996 - Live Preview decorates relation rows from the index
  ---
  duration_ms: 3.711404
  ...
# Subtest: Reading view decorates stored anchors and appends live edges
ok 997 - Reading view decorates stored anchors and appends live edges
  ---
  duration_ms: 2.571569
  ...
# Subtest: Reading view with api.relations v1 shows ＋ and ×
ok 998 - Reading view with api.relations v1 shows ＋ and ×
  ---
  duration_ms: 1.569426
  ...
# Subtest: ledger parser agrees with shared LK vectors and parses source task children
ok 999 - ledger parser agrees with shared LK vectors and parses source task children
  ---
  duration_ms: 4.048558
  ...
# Subtest: relationIndex scans done sources, resolves both directions, and orders label suggestions
ok 1000 - relationIndex scans done sources, resolves both directions, and orders label suggestions
  ---
  duration_ms: 8.058864
  ...
# Subtest: relationIndex applies changed, delete, rename, and unsaved editor overlays
ok 1001 - relationIndex applies changed, delete, rename, and unsaved editor overlays
  ---
  duration_ms: 25.541507
  ...
# Subtest: relationIndex registers after layout-ready and never reads non-markdown during startup replay
ok 1002 - relationIndex registers after layout-ready and never reads non-markdown during startup replay
  ---
  duration_ms: 37.022042
  ...
# Subtest: relationIndex ignores non-markdown live events
ok 1003 - relationIndex ignores non-markdown live events
  ---
  duration_ms: 32.1222
  ...
# Subtest: relationIndex layout-ready after unload registers nothing
ok 1004 - relationIndex layout-ready after unload registers nothing
  ---
  duration_ms: 31.554184
  ...
# Subtest: parseTaskRelationFile indexes every checkbox status as a task
ok 1005 - parseTaskRelationFile indexes every checkbox status as a task
  ---
  duration_ms: 0.948751
  ...
# Subtest: relationIndex incoming and suggestions include Next and Blocked sources
ok 1006 - relationIndex incoming and suggestions include Next and Blocked sources
  ---
  duration_ms: 6.45413
  ...
# Subtest: ledger LK1–LK19 recognises relation shapes and keeps them out of plan links
ok 1007 - ledger LK1–LK19 recognises relation shapes and keeps them out of plan links
  ---
  duration_ms: 2.542473
  ...
# Subtest: parseTrigger parses D[-]<N> dated-entry triggers with offset and span
ok 1008 - parseTrigger parses D[-]<N> dated-entry triggers with offset and span
  ---
  duration_ms: 1.762254
  ...
# Subtest: computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
ok 1009 - computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
  ---
  duration_ms: 0.447114
  ...
# Subtest: expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
ok 1010 - expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
  ---
  duration_ms: 0.423148
  ...
# Subtest: findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
ok 1011 - findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
  ---
  duration_ms: 0.339538
  ...
# Subtest: compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
ok 1012 - compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
  ---
  duration_ms: 0.298019
  ...
# Subtest: parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
ok 1013 - parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
  ---
  duration_ms: 0.142843
  ...
# Subtest: computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
ok 1014 - computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
  ---
  duration_ms: 0.171608
  ...
# Subtest: findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
ok 1015 - findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
  ---
  duration_ms: 0.176147
  ...
# Subtest: findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
ok 1016 - findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
  ---
  duration_ms: 0.295404
  ...
# Subtest: expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
ok 1017 - expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
  ---
  duration_ms: 0.612529
  ...
# Subtest: regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
ok 1018 - regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
  ---
  duration_ms: 0.35105
  ...
# Subtest: expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
ok 1019 - expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
  ---
  duration_ms: 0.28824
  ...
# Subtest: stats fence body sets defaults only and ignores the rest
ok 1020 - stats fence body sets defaults only and ignores the rest
  ---
  duration_ms: 2.460747
  ...
# Subtest: stats tile models cover every unit and every quality
ok 1021 - stats tile models cover every unit and every quality
  ---
  duration_ms: 0.592401
  ...
# Subtest: stats spark bars mark null gaps, zero ticks, and hollow today
ok 1022 - stats spark bars mark null gaps, zero ticks, and hollow today
  ---
  duration_ms: 0.376228
  ...
# Subtest: stats table rows and CSV share the same points
ok 1023 - stats table rows and CSV share the same points
  ---
  duration_ms: 0.821979
  ...
# Subtest: stats overview ids prefer the fence, then config, then report order
ok 1024 - stats overview ids prefer the fence, then config, then report order
  ---
  duration_ms: 1.191535
  ...
# Subtest: stats window label always states today and tracking start
ok 1025 - stats window label always states today and tracking start
  ---
  duration_ms: 0.248865
  ...
# Subtest: stats view state is session-only and per source path
ok 1026 - stats view state is session-only and per source path
  ---
  duration_ms: 5.619376
  ...
# Subtest: stats block renders header, tiles, table, and footer from JSON
ok 1027 - stats block renders header, tiles, table, and footer from JSON
  ---
  duration_ms: 43.009913
  ...
# Subtest: stats block shows an actionable card with Retry when bob fails
ok 1028 - stats block shows an actionable card with Retry when bob fails
  ---
  duration_ms: 43.043798
  ...
# Subtest: stats block registers the processor and the Open Stats command
ok 1029 - stats block registers the processor and the Open Stats command
  ---
  duration_ms: 1.768296
  ...
# Subtest: stats stylesheet contract: selectors, tabular-nums, motion, colors
ok 1030 - stats stylesheet contract: selectors, tabular-nums, motion, colors
  ---
  duration_ms: 1.408649
  ...
# Subtest: Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
ok 1031 - Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
  ---
  duration_ms: 2.034213
  ...
# Subtest: prior buckets align by elapsed position and omit invalid and provisional points
ok 1032 - prior buckets align by elapsed position and omit invalid and provisional points
  ---
  duration_ms: 0.770161
  ...
# Subtest: chart renders SVG safely and keeps secondary focus metrics selectable
ok 1033 - chart renders SVG safely and keeps secondary focus metrics selectable
  ---
  duration_ms: 9.955575
  ...
# Subtest: grouped chart pins honest buckets, bounds daily detail, and opens validated notes
ok 1034 - grouped chart pins honest buckets, bounds daily detail, and opens validated notes
  ---
  duration_ms: 7.416728
  ...
# Subtest: local focus, table, pin, and definition changes reuse the retained report
ok 1035 - local focus, table, pin, and definition changes reuse the retained report
  ---
  duration_ms: 8.959693
  ...
# Subtest: keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
ok 1036 - keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
  ---
  duration_ms: 34.389989
  ...
# Subtest: schema-1 fallback keeps day quartiles and never invents grouped daily history
ok 1037 - schema-1 fallback keeps day quartiles and never invents grouped daily history
  ---
  duration_ms: 3.458432
  ...
# Subtest: ResizeObserver redraws cached data and disconnects across rerenders and unload
ok 1038 - ResizeObserver redraws cached data and disconnects across rerenders and unload
  ---
  duration_ms: 132.798453
  ...
# Subtest: stats resolution prefers stats.bob_path, then candidates, then PATH
ok 1039 - stats resolution prefers stats.bob_path, then candidates, then PATH
  ---
  duration_ms: 1.53995
  ...
# Subtest: stats home expansion and range/offset normalization
ok 1040 - stats home expansion and range/offset normalization
  ---
  duration_ms: 0.333607
  ...
# Subtest: stats fetch always runs show -a -f json plus the chosen flags
ok 1041 - stats fetch always runs show -a -f json plus the chosen flags
  ---
  duration_ms: 0.324429
  ...
# Subtest: stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
ok 1042 - stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
  ---
  duration_ms: 5.853313
  ...
# Subtest: stats spawn maps ENOENT, timeouts, and stderr to named errors
ok 1043 - stats spawn maps ENOENT, timeouts, and stderr to named errors
  ---
  duration_ms: 2.325909
  ...
# Subtest: stats decode accepts schema 1 and rejects the rest defensively
ok 1044 - stats decode accepts schema 1 and rejects the rest defensively
  ---
  duration_ms: 0.281788
  ...
# Subtest: stats error cards name the cause and the stats.bob_path fix
ok 1045 - stats error cards name the cause and the stats.bob_path fix
  ---
  duration_ms: 0.340751
  ...
# Subtest: stats fetch shares one flight and coalesces one follow-up
ok 1046 - stats fetch shares one flight and coalesces one follow-up
  ---
  duration_ms: 23.037068
  ...
# Subtest: stats cache is a small LRU keyed by the argument list
ok 1047 - stats cache is a small LRU keyed by the argument list
  ---
  duration_ms: 2.797189
  ...
# Subtest: stats stale entries return immediately and refresh in the background
ok 1048 - stats stale entries return immediately and refresh in the background
  ---
  duration_ms: 1.4199
  ...
# Subtest: stats api v2 keeps append and adds fetch plus bobPath
ok 1049 - stats api v2 keeps append and adds fetch plus bobPath
  ---
  duration_ms: 0.888556
  ...
# Subtest: statsHomeDir defaults to the real home and strips a trailing slash
ok 1050 - statsHomeDir defaults to the real home and strips a trailing slash
  ---
  duration_ms: 0.203739
  ...
# Subtest: stats mac regression: un-injected resolution probes the real home first
ok 1051 - stats mac regression: un-injected resolution probes the real home first
  ---
  duration_ms: 0.227715
  ...
# Subtest: stats absolute candidates are probed verbatim with no doubled slashes
ok 1052 - stats absolute candidates are probed verbatim with no doubled slashes
  ---
  duration_ms: 0.247372
  ...
# Subtest: stats with no home probes only absolute candidates
ok 1053 - stats with no home probes only absolute candidates
  ---
  duration_ms: 0.25144
  ...
# Subtest: stats tilde config expands against the real home
ok 1054 - stats tilde config expands against the real home
  ---
  duration_ms: 0.128886
  ...
# Subtest: stats candidate and tried lists share one source of truth
ok 1055 - stats candidate and tried lists share one source of truth
  ---
  duration_ms: 0.113817
  ...
# Subtest: stats spawn bob-not-found tried list uses the real home
ok 1056 - stats spawn bob-not-found tried list uses the real home
  ---
  duration_ms: 1.02164
  ...
# Subtest: stats unload clears views, timers, cache, and flights
ok 1057 - stats unload clears views, timers, cache, and flights
  ---
  duration_ms: 0.554258
  ...
# Subtest: stats namespace v1 serializes versioned review answer JSONL
ok 1058 - stats namespace v1 serializes versioned review answer JSONL
  ---
  duration_ms: 9.165326
  ...
# Subtest: stats journal rejects invalid calendar days and outcomes
ok 1059 - stats journal rejects invalid calendar days and outcomes
  ---
  duration_ms: 1.716767
  ...
# Subtest: statsReviewHost lowercases, cuts at the first dot, and never throws
ok 1060 - statsReviewHost lowercases, cuts at the first dot, and never throws
  ---
  duration_ms: 0.1989
  ...
# Subtest: stats journal plugin passthrough keeps a semver writer and falls back otherwise
ok 1061 - stats journal plugin passthrough keeps a semver writer and falls back otherwise
  ---
  duration_ms: 0.948801
  ...
# Subtest: panel dispatch covers every family, custom kinds, and the net exception
ok 1062 - panel dispatch covers every family, custom kinds, and the net exception
  ---
  duration_ms: 0.9323
  ...
# Subtest: pomodoro panel shows the supplied total, shares, hue, and safe text
ok 1063 - pomodoro panel shows the supplied total, shares, hue, and safe text
  ---
  duration_ms: 10.129115
  ...
# Subtest: home parts use the report catalog for labels, hue slots, and pinned values
ok 1064 - home parts use the report catalog for labels, hue slots, and pinned values
  ---
  duration_ms: 10.391147
  ...
# Subtest: areas panel toggles Themes, pins spans, expands projects, and opens home links
ok 1065 - areas panel toggles Themes, pins spans, expands projects, and opens home links
  ---
  duration_ms: 17.961066
  ...
# Subtest: chart pin refreshes Where the time went and Themes honor the pinned span
ok 1066 - chart pin refreshes Where the time went and Themes honor the pinned span
  ---
  duration_ms: 4.823478
  ...
# Subtest: review rows keep their area hue and a missing homes report keeps the saved view
ok 1067 - review rows keep their area hue and a missing homes report keeps the saved view
  ---
  duration_ms: 3.6875
  ...
# Subtest: task home table uses catalog labels and keeps hue dots and mini-bars
ok 1068 - task home table uses catalog labels and keeps hue dots and mini-bars
  ---
  duration_ms: 7.871285
  ...
# Subtest: task flow stacks signed values, keeps missing constituents missing, and labels series
ok 1069 - task flow stacks signed values, keeps missing constituents missing, and labels series
  ---
  duration_ms: 3.22151
  ...
# Subtest: absent companions are named, custom filters are labeled overall, and net splits breakdowns
ok 1070 - absent companions are named, custom filters are labeled overall, and net splits breakdowns
  ---
  duration_ms: 4.694663
  ...
# Subtest: journal panels pair answers with review time and a gapped keep chart under 90%
ok 1071 - journal panels pair answers with review time and a gapped keep chart under 90%
  ---
  duration_ms: 4.317982
  ...
# Subtest: checklist calendar aligns Monday weeks with states, reasons, and provisional today
ok 1072 - checklist calendar aligns Monday weeks with states, reasons, and provisional today
  ---
  duration_ms: 5.727375
  ...
# Subtest: grouped calendars reuse daily points and old schemas fall back with a label
ok 1073 - grouped calendars reuse daily points and old schemas fall back with a label
  ---
  duration_ms: 3.145044
  ...
# Subtest: ISO year boundaries stay in one Monday week and chore dots expose text
ok 1074 - ISO year boundaries stay in one Monday week and chore dots expose text
  ---
  duration_ms: 2.123764
  ...
# Subtest: panel day selection pins the shared day and never fetches
ok 1075 - panel day selection pins the shared day and never fetches
  ---
  duration_ms: 3.817336
  ...
# Subtest: field and formula metrics keep only the focus chart and table
ok 1076 - field and formula metrics keep only the focus chart and table
  ---
  duration_ms: 1.034564
  ...
# Subtest: TT vectors verbatim: task-line gate plus boundary tokens
ok 1077 - TT vectors verbatim: task-line gate plus boundary tokens
  ---
  duration_ms: 3.675678
  ...
# Subtest: TT13-TT14 cursor reveal is inclusive
ok 1078 - TT13-TT14 cursor reveal is inclusive
  ---
  duration_ms: 1.888584
  ...
# Subtest: TT16 coexistence: task tag range is disjoint from priority and date marks
ok 1079 - TT16 coexistence: task tag range is disjoint from priority and date marks
  ---
  duration_ms: 1.232152
  ...
# Subtest: tooltip is exact and never contains a double colon
ok 1080 - tooltip is exact and never contains a double colon
  ---
  duration_ms: 0.196264
  ...
# Subtest: element structure: empty widget span with tooltip attributes
ok 1081 - element structure: empty widget span with tooltip attributes
  ---
  duration_ms: 0.321294
  ...
# Subtest: Live Preview decorations cover exactly the tag and respect reveal and code
ok 1082 - Live Preview decorations cover exactly the tag and respect reveal and code
  ---
  duration_ms: 0.70204
  ...
# Subtest: widget mousedown reveals the tag start
ok 1083 - widget mousedown reveals the tag start
  ---
  duration_ms: 0.369826
  ...
# Subtest: TR vectors verbatim: rendered views annotate eligible anchors in place
ok 1084 - TR vectors verbatim: rendered views annotate eligible anchors in place
  ---
  duration_ms: 1.448916
  ...
# Subtest: TR9 toggle strips document-wide and re-annotates on enable
ok 1085 - TR9 toggle strips document-wide and re-annotates on enable
  ---
  duration_ms: 0.904938
  ...
# Subtest: annotate and strip helpers are idempotent and defensive
ok 1086 - annotate and strip helpers are idempotent and defensive
  ---
  duration_ms: 0.554499
  ...
# Subtest: session toggle and onload wiring
ok 1087 - session toggle and onload wiring
  ---
  duration_ms: 3.883284
  ...
# Subtest: styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
ok 1088 - styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
  ---
  duration_ms: 0.983337
  ...
# Subtest: TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
ok 1089 - TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
  ---
  duration_ms: 0.374374
  ...
# Subtest: Live Preview ref decorations replace the whole pair and reveal both tags at once
ok 1090 - Live Preview ref decorations replace the whole pair and reveal both tags at once
  ---
  duration_ms: 0.333717
  ...
# Subtest: ref element structure: book classes, reference label, and tooltip
ok 1091 - ref element structure: book classes, reference label, and tooltip
  ---
  duration_ms: 0.135609
  ...
# Subtest: TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
ok 1092 - TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
  ---
  duration_ms: 0.588183
  ...
# Subtest: TR11 verbatim: \#task \#references and reversed order keep the hash only
ok 1093 - TR11 verbatim: \#task \#references and reversed order keep the hash only
  ---
  duration_ms: 0.26693
  ...
# Subtest: TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
ok 1094 - TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
  ---
  duration_ms: 0.138014
  ...
# Subtest: TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
ok 1095 - TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
  ---
  duration_ms: 0.543727
  ...
# Subtest: styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
ok 1096 - styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
  ---
  duration_ms: 0.753759
  ...
# Subtest: CK vectors: canonical PRE/POST checklist runs share membership semantics
ok 1097 - CK vectors: canonical PRE/POST checklist runs share membership semantics
  ---
  duration_ms: 1.835022
  ...
# Subtest: CK live preview and widget vectors: one stable glyph replaces the full run
ok 1098 - CK live preview and widget vectors: one stable glyph replaces the full run
  ---
  duration_ms: 0.37718
  ...
# Subtest: CR vectors: rendered checklist anchors annotate in place, conflict stays native
ok 1099 - CR vectors: rendered checklist anchors annotate in place, conflict stays native
  ---
  duration_ms: 0.847417
  ...
# Subtest: CR3 toggle restores all checklist pills and re-annotates them
ok 1100 - CR3 toggle restores all checklist pills and re-annotates them
  ---
  duration_ms: 0.365287
  ...
# Subtest: CR4 Today reading-view anchor follows the second checklist tag
ok 1101 - CR4 Today reading-view anchor follows the second checklist tag
  ---
  duration_ms: 0.330251
  ...
# Subtest: checklist task mark CSS contract covers glyphs, conflict gates, Tasks rows, and resting
ok 1102 - checklist task mark CSS contract covers glyphs, conflict gates, Tasks rows, and resting
  ---
  duration_ms: 0.724092
  ...
# Subtest: section info null stays neutral (TM19)
ok 1103 - section info null stays neutral (TM19)
  ---
  duration_ms: 1.907641
  ...
# Subtest: data-line mapping stamps and marks an exact Today row
ok 1104 - data-line mapping stamps and marks an exact Today row
  ---
  duration_ms: 3.340788
  ...
# Subtest: data-line mapping rejects a status mismatch
ok 1105 - data-line mapping rejects a status mismatch
  ---
  duration_ms: 0.318608
  ...
# Subtest: row-index fallback maps when counts agree and refuses when they disagree
ok 1106 - row-index fallback maps when counts agree and refuses when they disagree
  ---
  duration_ms: 1.358212
  ...
# Subtest: Tasks result rows and code are skipped
ok 1107 - Tasks result rows and code are skipped
  ---
  duration_ms: 0.417537
  ...
# Subtest: a daily-note sourcePath is skipped
ok 1108 - a daily-note sourcePath is skipped
  ---
  duration_ms: 0.191325
  ...
# Subtest: duplicate ids stay neutral
ok 1109 - duplicate ids stay neutral
  ---
  duration_ms: 0.52358
  ...
# Subtest: insertion points: \#task anchor, \#ref pair, checkbox, whitespace split
ok 1110 - insertion points: \#task anchor, \#ref pair, checkbox, whitespace split
  ---
  duration_ms: 1.342332
  ...
# Subtest: identity-proven non-Today rows are stamped without a mark
ok 1111 - identity-proven non-Today rows are stamped without a mark
  ---
  duration_ms: 0.535322
  ...
# Subtest: sweep adds on link, removes on unlink or completion, updates tooltip, respects toggle, skips daily ancestors
ok 1112 - sweep adds on link, removes on unlink or completion, updates tooltip, respects toggle, skips daily ancestors
  ---
  duration_ms: 1.513028
  ...
# Subtest: daily-view class is set on open daily leaves and cleared on switch
ok 1113 - daily-view class is set on open daily leaves and cleared on switch
  ---
  duration_ms: 0.313689
  ...
# Subtest: delegated Mod+click jumps; plain click does not
ok 1114 - delegated Mod+click jumps; plain click does not
  ---
  duration_ms: 2.71333
  ...
# Subtest: setupTodayMarks registers the reading post-processor at order 60
ok 1115 - setupTodayMarks registers the reading post-processor at order 60
  ---
  duration_ms: 0.325922
  ...
# Subtest: styles.css daily-view suppression is present
ok 1116 - styles.css daily-view suppression is present
  ---
  duration_ms: 0.590538
  ...
# Subtest: Live Preview marks do not double-jump in Reading view
ok 1117 - Live Preview marks do not double-jump in Reading view
  ---
  duration_ms: 0.45034
  ...
# Subtest: mid-body \#task goes at the body start
ok 1118 - mid-body \#task goes at the body start
  ---
  duration_ms: 0.566191
  ...
# Subtest: \#task inside inline code stays neutral
ok 1119 - \#task inside inline code stays neutral
  ---
  duration_ms: 0.244387
  ...
# Subtest: re-render with a new path refreshes the mark key
ok 1120 - re-render with a new path refreshes the mark key
  ---
  duration_ms: 0.313238
  ...
# Subtest: one duplicate scan per render
ok 1121 - one duplicate scan per render
  ---
  duration_ms: 0.558436
  ...
# Subtest: row-index fallback uses every list item
ok 1122 - row-index fallback uses every list item
  ---
  duration_ms: 0.512148
  ...
# Subtest: open statuses are exactly space, star, slash, and question
ok 1123 - open statuses are exactly space, star, slash, and question
  ---
  duration_ms: 1.868838
  ...
# Subtest: trailing-id rules: leading space, trailing-only, valid charset
ok 1124 - trailing-id rules: leading space, trailing-only, valid charset
  ---
  duration_ms: 0.312106
  ...
# Subtest: candidate: TM9 closed stays null, TM10 open statuses pass
ok 1125 - candidate: TM9 closed stays null, TM10 open statuses pass
  ---
  duration_ms: 1.694786
  ...
# Subtest: candidate: TM11 needs an exact \#task tag and a trailing id
ok 1126 - candidate: TM11 needs an exact \#task tag and a trailing id
  ---
  duration_ms: 0.261529
  ...
# Subtest: candidate: TM21 code is left for the call-site code check
ok 1127 - candidate: TM21 code is left for the call-site code check
  ---
  duration_ms: 0.432165
  ...
# Subtest: insert offset: \#task first lands before the title
ok 1128 - insert offset: \#task first lands before the title
  ---
  duration_ms: 0.211163
  ...
# Subtest: insert offset: TM16 \#task \#ref spans the pair, \#prj sits between
ok 1129 - insert offset: TM16 \#task \#ref spans the pair, \#prj sits between
  ---
  duration_ms: 0.255117
  ...
# Subtest: insert offset: mid-body \#task falls back to the body start
ok 1130 - insert offset: mid-body \#task falls back to the body start
  ---
  duration_ms: 0.149596
  ...
# Subtest: insert offset: blockquote, spaces, numbered, empty title, emoji
ok 1131 - insert offset: blockquote, spaces, numbered, empty title, emoji
  ---
  duration_ms: 0.794155
  ...
# Subtest: duplicates: TM15 marks neither line
ok 1132 - duplicates: TM15 marks neither line
  ---
  duration_ms: 0.491087
  ...
# Subtest: session text: named, home label, range-only, unnamed
ok 1133 - session text: named, home label, range-only, unnamed
  ---
  duration_ms: 0.306004
  ...
# Subtest: tooltip: TM1 running, TM2 queued, and the platform variants
ok 1134 - tooltip: TM1 running, TM2 queued, and the platform variants
  ---
  duration_ms: 0.243525
  ...
# Subtest: tooltip: running wins as primary with a +N more suffix
ok 1135 - tooltip: running wins as primary with a +N more suffix
  ---
  duration_ms: 0.130039
  ...
# Subtest: tooltip: empty input yields Today and output never has ::
ok 1136 - tooltip: empty input yields Today and output never has ::
  ---
  duration_ms: 0.212696
  ...
# Subtest: entering window: 600 ms after join, never before or at load
ok 1137 - entering window: 600 ms after join, never before or at load
  ---
  duration_ms: 0.116543
  ...
# Subtest: modifier: primary button with meta on mac, ctrl elsewhere
ok 1138 - modifier: primary button with meta on mac, ctrl elsewhere
  ---
  duration_ms: 0.138244
  ...
# Subtest: element: empty span with tooltip attributes and no listeners
ok 1139 - element: empty span with tooltip attributes and no listeners
  ---
  duration_ms: 0.311886
  ...
# Subtest: widget: eq ignores entering and the callback
ok 1140 - widget: eq ignores entering and the callback
  ---
  duration_ms: 0.167861
  ...
# Subtest: widget: plain mousedown moves the cursor, Mod mousedown jumps
ok 1141 - widget: plain mousedown moves the cursor, Mod mousedown jumps
  ---
  duration_ms: 0.47131
  ...
# Subtest: refresh effect is lazy and stable
ok 1142 - refresh effect is lazy and stable
  ---
  duration_ms: 0.110742
  ...
# Subtest: styles.css implements the glyph anatomy contract
ok 1143 - styles.css implements the glyph anatomy contract
  ---
  duration_ms: 0.643048
  ...
# Subtest: Live Preview applies the TM1-TM22 line, cache, and refresh vectors
ok 1144 - Live Preview applies the TM1-TM22 line, cache, and refresh vectors
  ---
  duration_ms: 26.216456
  ...
# Subtest: Today mark lifecycle registers the toggle, keyboard command, and reading processor
ok 1145 - Today mark lifecycle registers the toggle, keyboard command, and reading processor
  ---
  duration_ms: 18.231644
  ...
# Subtest: keyboard jump uses the task under the cursor and reports non-membership
ok 1146 - keyboard jump uses the task under the cursor and reports non-membership
  ---
  duration_ms: 17.151941
  ...
# Subtest: Mod-click and keyboard jumps land on the current running Task Link
ok 1147 - Mod-click and keyboard jumps land on the current running Task Link
  ---
  duration_ms: 15.76272
  ...
# Subtest: reduced motion stops the entrance pop
ok 1148 - reduced motion stops the entrance pop
  ---
  duration_ms: 0.590687
  ...
# Subtest: tooltips never contain ::
ok 1149 - tooltips never contain ::
  ---
  duration_ms: 0.185224
  ...
# Subtest: todayMarkPosInInlineCode: single, double, unmatched, positions
ok 1150 - todayMarkPosInInlineCode: single, double, unmatched, positions
  ---
  duration_ms: 0.286177
  ...
# Subtest: builder gates on Today ids without touching doc lines
ok 1151 - builder gates on Today ids without touching doc lines
  ---
  duration_ms: 21.113034
  ...
# Subtest: two rebuilds on the same doc compute duplicates once
ok 1152 - two rebuilds on the same doc compute duplicates once
  ---
  duration_ms: 20.226301
  ...
# Subtest: todayMarksNow override drives readiness
ok 1153 - todayMarksNow override drives readiness
  ---
  duration_ms: 11.98557
  ...
# Subtest: refresh dispatches only to non-daily leaves and uses 16 ms
ok 1154 - refresh dispatches only to non-daily leaves and uses 16 ms
  ---
  duration_ms: 11.33661
  ...
# Subtest: keyboard command gates closed status and daily notes
ok 1155 - keyboard command gates closed status and daily notes
  ---
  duration_ms: 15.367747
  ...
# Subtest: TM14 rollover: day N+1 shows no decoration
ok 1156 - TM14 rollover: day N+1 shows no decoration
  ---
  duration_ms: 18.227725
  ...
# Subtest: TM17 widget sits at line.from + insertCh with side -1
ok 1157 - TM17 widget sits at line.from + insertCh with side -1
  ---
  duration_ms: 10.428659
  ...
# Subtest: TM18 entering: new key pops then settles
ok 1158 - TM18 entering: new key pops then settles
  ---
  duration_ms: 21.88156
  ...
# Subtest: TM20 toggle flips class, notice, and refreshes non-daily leaves
ok 1159 - TM20 toggle flips class, notice, and refreshes non-daily leaves
  ---
  duration_ms: 19.469436
  ...
# Subtest: rebuild triggers: doc, viewport, LP field, file switch rebuild; selection alone does not
ok 1160 - rebuild triggers: doc, viewport, LP field, file switch rebuild; selection alone does not
  ---
  duration_ms: 9.187829
  ...
# Subtest: jump guards in-flight, prefers cached ledgerLine over later match
ok 1161 - jump guards in-flight, prefers cached ledgerLine over later match
  ---
  duration_ms: 10.360307
  ...
# Subtest: jump with no open daily leaf attempts the daily open
ok 1162 - jump with no open daily leaf attempts the daily open
  ---
  duration_ms: 17.073782
  ...
# Subtest: home labels: unnamed timed entry uses derived label and 1-based entryLine
ok 1163 - home labels: unnamed timed entry uses derived label and 1-based entryLine
  ---
  duration_ms: 12.959648
  ...
# Subtest: T1 GTD: empty target resolves to the daily note
ok 1164 - T1 GTD: empty target resolves to the daily note
  ---
  duration_ms: 3.793723
  ...
# Subtest: T2 markers: pomodoro mark counts, struck drops, embed counts
ok 1165 - T2 markers: pomodoro mark counts, struck drops, embed counts
  ---
  duration_ms: 0.645643
  ...
# Subtest: T3 closed entries: links under completed/cancelled entries drop
ok 1166 - T3 closed entries: links under completed/cancelled entries drop
  ---
  duration_ms: 0.237313
  ...
# Subtest: T4 shapes: mixed text and deeper descendants drop
ok 1167 - T4 shapes: mixed text and deeper descendants drop
  ---
  duration_ms: 0.345991
  ...
# Subtest: T5 dedupe: same task twice keeps the first position
ok 1168 - T5 dedupe: same task twice keeps the first position
  ---
  duration_ms: 0.42426
  ...
# Subtest: T6 fenced: links inside fenced blocks drop
ok 1169 - T6 fenced: links inside fenced blocks drop
  ---
  duration_ms: 0.336593
  ...
# Subtest: T7 status: the link layer lists every dedicated link
ok 1170 - T7 status: the link layer lists every dedicated link
  ---
  duration_ms: 0.363144
  ...
# Subtest: T8 unresolved: missing notes give no key
ok 1171 - T8 unresolved: missing notes give no key
  ---
  duration_ms: 0.195844
  ...
# Subtest: T9 alias: aliased links count under their target
ok 1172 - T9 alias: aliased links count under their target
  ---
  duration_ms: 0.531284
  ...
# Subtest: laneBudgetFromTasks counts the whole Next lane, Today included
ok 1173 - laneBudgetFromTasks counts the whole Next lane, Today included
  ---
  duration_ms: 1.106822
  ...
# Subtest: laneBudgetFromTasks counts Pending by type and flags over-cap
ok 1174 - laneBudgetFromTasks counts Pending by type and flags over-cap
  ---
  duration_ms: 0.333357
  ...
# Subtest: lane caps come from max_next/max_pending; legacy max_now is ignored
ok 1175 - lane caps come from max_next/max_pending; legacy max_now is ignored
  ---
  duration_ms: 0.17317
  ...
# Subtest: reload event name matches the Tasks bundle subscription
ok 1176 - reload event name matches the Tasks bundle subscription
  ---
  duration_ms: 0.081596
  ...
# Subtest: api v2 shape: Today and lane budgets, no nowBudget
ok 1177 - api v2 shape: Today and lane budgets, no nowBudget
  ---
  duration_ms: 4.159419
  ...
# Subtest: cache rebuild answers isToday/todayRank in ledger order
ok 1178 - cache rebuild answers isToday/todayRank in ledger order
  ---
  duration_ms: 2.09994
  ...
# Subtest: refresh fires only when the key set changes
ok 1179 - refresh fires only when the key set changes
  ---
  duration_ms: 0.930707
  ...
# Subtest: unready to ready with empty TODAY still refreshes open badges
ok 1180 - unready to ready with empty TODAY still refreshes open badges
  ---
  duration_ms: 0.892725
  ...
# Subtest: cache rebuilds on the daily changed event with the event content
ok 1181 - cache rebuilds on the daily changed event with the event content
  ---
  duration_ms: 0.682282
  ...
# Subtest: cache rebuilds once on resolved and at midnight rollover
ok 1182 - cache rebuilds once on resolved and at midnight rollover
  ---
  duration_ms: 2.344516
  ...
# Subtest: computeTodayLinks records entry range and placeholder
ok 1183 - computeTodayLinks records entry range and placeholder
  ---
  duration_ms: 0.321704
  ...
# Subtest: todayOpenEntries and todayRunningEntryLine follow the unique timed rule
ok 1184 - todayOpenEntries and todayRunningEntryLine follow the unique timed rule
  ---
  duration_ms: 0.33523
  ...
# Subtest: resolveTodayLinkKeys keeps duplicates; resolveTodayKeys is first-occurrence
ok 1185 - resolveTodayLinkKeys keeps duplicates; resolveTodayKeys is first-occurrence
  ---
  duration_ms: 0.227916
  ...
# Subtest: todayLinkDetails: named running, placeholder, unnamed home, unnamed none
ok 1186 - todayLinkDetails: named running, placeholder, unnamed home, unnamed none
  ---
  duration_ms: 0.201896
  ...
# Subtest: todayLinkDetails orders running first and keeps one detail per key+entry
ok 1187 - todayLinkDetails orders running first and keeps one detail per key+entry
  ---
  duration_ms: 0.147933
  ...
# Subtest: todayKeyParts splits at the last hash; idsByPath groups block ids
ok 1188 - todayKeyParts splits at the last hash; idsByPath groups block ids
  ---
  duration_ms: 0.118757
  ...
# Subtest: todayDetailsSignature changes only when details change
ok 1189 - todayDetailsSignature changes only when details change
  ---
  duration_ms: 0.23059
  ...
# Subtest: idsByPath and details accessors follow the rebuilt cache
ok 1190 - idsByPath and details accessors follow the rebuilt cache
  ---
  duration_ms: 0.983988
  ...
# Subtest: details-only change refreshes marks without a Tasks reload
ok 1191 - details-only change refreshes marks without a Tasks reload
  ---
  duration_ms: 0.807601
  ...
# Subtest: entered stamps only when the cache was already ready, then prune
ok 1192 - entered stamps only when the cache was already ready, then prune
  ---
  duration_ms: 1.316823
  ...
# Subtest: generation guard: reverse-order async reads keep the newer
ok 1193 - generation guard: reverse-order async reads keep the newer
  ---
  duration_ms: 1.2619
  ...
# Subtest: generation guard: a sync rebuild wins over an in-flight async read
ok 1194 - generation guard: a sync rebuild wins over an in-flight async read
  ---
  duration_ms: 0.556252
  ...
# Subtest: revalidateTodayCache is throttled and refreshes when not ready
ok 1195 - revalidateTodayCache is throttled and refreshes when not ready
  ---
  duration_ms: 0.568104
  ...
# Subtest: revalidateTodayCache respects layoutReady and backwards clock steps
ok 1196 - revalidateTodayCache respects layoutReady and backwards clock steps
  ---
  duration_ms: 0.455009
  ...
# Subtest: a done-today prerequisite shows the glyph
ok 1197 - a done-today prerequisite shows the glyph
  ---
  duration_ms: 3.204757
  ...
# Subtest: done yesterday does not show the glyph
ok 1198 - done yesterday does not show the glyph
  ---
  duration_ms: 0.41408
  ...
# Subtest: a struck link does not show the glyph
ok 1199 - a struck link does not show the glyph
  ---
  duration_ms: 0.258163
  ...
# Subtest: a closed entry does not show the glyph
ok 1200 - a closed entry does not show the glyph
  ---
  duration_ms: 0.267831
  ...
# Subtest: several prerequisites give +N
ok 1201 - several prerequisites give +N
  ---
  duration_ms: 0.554428
  ...
# Subtest: the model refuses every non-glyph shape
ok 1202 - the model refuses every non-glyph shape
  ---
  duration_ms: 1.080923
  ...
# Subtest: unblockedGlyphDoneToday needs DONE plus a today done date
ok 1203 - unblockedGlyphDoneToday needs DONE plus a today done date
  ---
  duration_ms: 0.348556
  ...
# Subtest: tooltip names one prerequisite and counts several
ok 1204 - tooltip names one prerequisite and counts several
  ---
  duration_ms: 0.421675
  ...
# Subtest: Live Preview places one glyph after each unblocked link
not ok 1205 - Live Preview places one glyph after each unblocked link
  ---
  duration_ms: 2.753607
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:546:1'
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
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:553:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Live Preview draws nothing without a warm cache or a live link
ok 1206 - Live Preview draws nothing without a warm cache or a live link
  ---
  duration_ms: 1.513139
  ...
# Subtest: widget mousedown places the cursor past the link
not ok 1207 - widget mousedown places the cursor past the link
  ---
  duration_ms: 0.43982
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:612:1'
  failureType: 'testCodeFailure'
  error: "Cannot read properties of undefined (reading 'value')"
  code: 'ERR_TEST_FAILURE'
  name: 'TypeError'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:615:69)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
not ok 1208 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 0.421345
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:654:1'
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
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:662:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Reading view glyphs unblocked rows and dedupes
not ok 1209 - Reading view glyphs unblocked rows and dedupes
  ---
  duration_ms: 1.602399
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:849:1'
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
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:858:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Reading view refuses every non-glyph row
ok 1210 - Reading view refuses every non-glyph row
  ---
  duration_ms: 1.561251
  ...
# Subtest: api.unblockedGlyph v1 is additive, sync, and never throwing
ok 1211 - api.unblockedGlyph v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.636154
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 1212 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 1.149113
  ...
# Subtest: changed-file and rollover refreshes
ok 1213 - changed-file and rollover refreshes
  ---
  duration_ms: 0.297478
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 1214 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.104179
  ...
# Subtest: styles.css contract: faint glyph, Done token, toggle
ok 1215 - styles.css contract: faint glyph, Done token, toggle
  ---
  duration_ms: 0.75439
  ...
# Subtest: Ledger Vim mappings restore \\p and retain the other normal-mode actions
ok 1216 - Ledger Vim mappings restore \\p and retain the other normal-mode actions
  ---
  duration_ms: 2.537985
  ...
# Subtest: workBadgeTone boundary vectors at cap 100 use exact comparisons
ok 1217 - workBadgeTone boundary vectors at cap 100 use exact comparisons
  ---
  duration_ms: 0.954562
  ...
# Subtest: workBadgeTone at cap 15 has no percentage rounding
ok 1218 - workBadgeTone at cap 15 has no percentage rounding
  ---
  duration_ms: 0.178671
  ...
# Subtest: workBadgeTone default caps, small caps, and cap changes
ok 1219 - workBadgeTone default caps, small caps, and cap changes
  ---
  duration_ms: 0.139606
  ...
# Subtest: workBadgeTone never coerces invalid input to zero
ok 1220 - workBadgeTone never coerces invalid input to zero
  ---
  duration_ms: 0.958089
  ...
# Subtest: TODAY links bands with themes at cap 3
ok 1221 - TODAY links bands with themes at cap 3
  ---
  duration_ms: 0.306085
  ...
# Subtest: TODAY theme overflow forces red, exact cap does not
ok 1222 - TODAY theme overflow forces red, exact cap does not
  ---
  duration_ms: 0.201785
  ...
# Subtest: TODAY unavailable stays neutral, empty section is grey
ok 1223 - TODAY unavailable stays neutral, empty section is grey
  ---
  duration_ms: 1.048752
  ...
# Subtest: PENDING/NEXT models color the section, READY its gated count
ok 1224 - PENDING/NEXT models color the section, READY its gated count
  ---
  duration_ms: 0.463104
  ...
# Subtest: READY uses its gated count even when the total lane is larger
ok 1225 - READY uses its gated count even when the total lane is larger
  ---
  duration_ms: 0.341321
  ...
# Subtest: cap equality still emits no cap lint
ok 1226 - cap equality still emits no cap lint
  ---
  duration_ms: 2.617036
  ...
# Subtest: lane DOM keeps exactly one tone through transitions and unavailability
ok 1227 - lane DOM keeps exactly one tone through transitions and unavailability
  ---
  duration_ms: 6.063835
  ...
# Subtest: READY DOM keeps exactly one tone and daily/dashboard models agree
ok 1228 - READY DOM keeps exactly one tone and daily/dashboard models agree
  ---
  duration_ms: 1.020689
  ...
# SKIP dashboard integration: BOB_DASHBOARD_FILE is not set
# SKIP dashboard fallback integration: BOB_DASHBOARD_FILE is not set
# SKIP dash CSS contract: BOB_DASHBOARD_FILE is not set
# Subtest: daily TODAY chip uses the theme-overflow tone
ok 1229 - daily TODAY chip uses the theme-overflow tone
  ---
  duration_ms: 14.836632
  ...
# Subtest: dashboard integration uses Work tones, TODAY override, and keeps Work order
ok 1230 - dashboard integration uses Work tones, TODAY override, and keeps Work order
  ---
  duration_ms: 0.53434
  ...
# Subtest: dashboard fallbacks keep Work tones without plugin renderers or colors
ok 1231 - dashboard fallbacks keep Work tones without plugin renderers or colors
  ---
  duration_ms: 0.325752
  ...
# Subtest: Work tone CSS covers each tone and uses the shared magenta value
ok 1232 - Work tone CSS covers each tone and uses the shared magenta value
  ---
  duration_ms: 0.840234
  ...
# Subtest: RBW6 mergeTargetPreparations keeps one write at the strongest lane
ok 1233 - RBW6 mergeTargetPreparations keeps one write at the strongest lane
  ---
  duration_ms: 1.746013
  ...
# Subtest: §15.7 notices use curly quotes and the Ready → Blocked copy
ok 1234 - §15.7 notices use curly quotes and the Ready → Blocked copy
  ---
  duration_ms: 0.360819
  ...
# Subtest: RBP1 same-note add is one transaction and matches forward bytes
ok 1235 - RBP1 same-note add is one transaction and matches forward bytes
  ---
  duration_ms: 17.682945
  ...
# Subtest: RBP2 background-leaf T matches forward bytes
ok 1236 - RBP2 background-leaf T matches forward bytes
  ---
  duration_ms: 5.162786
  ...
# Subtest: RBP3 closed T is written through vault.process and matches forward bytes
ok 1237 - RBP3 closed T is written through vault.process and matches forward bytes
  ---
  duration_ms: 3.473322
  ...
# Subtest: RBP4 ordinary transfer; a ^prj N is never raised
ok 1238 - RBP4 ordinary transfer; a ^prj N is never raised
  ---
  duration_ms: 12.320779
  ...
# Subtest: RBP5 consumed Pomodoro link matches forward bytes
ok 1239 - RBP5 consumed Pomodoro link matches forward bytes
  ---
  duration_ms: 4.889435
  ...
# Subtest: RBP6 project T with residents and a sub-project matches forward bytes
ok 1240 - RBP6 project T with residents and a sub-project matches forward bytes
  ---
  duration_ms: 25.15532
  ...
# Subtest: RBP7 two dependents in different lanes prepare N once at [/]
ok 1241 - RBP7 two dependents in different lanes prepare N once at [/]
  ---
  duration_ms: 5.075039
  ...
# Subtest: RBP8 counted sources N1 and N2 match forward(T + N1, N2)
ok 1242 - RBP8 counted sources N1 and N2 match forward(T + N1, N2)
  ---
  duration_ms: 4.184187
  ...
# Subtest: RBP9 blocks_lines false writes no BLOCKS and still ids N
ok 1243 - RBP9 blocks_lines false writes no BLOCKS and still ids N
  ---
  duration_ms: 2.21115
  ...
# Subtest: RBP10 removing the last reason matches forward removal
ok 1244 - RBP10 removing the last reason matches forward removal
  ---
  duration_ms: 4.129223
  ...
# Subtest: RBW1 a changed source note writes nothing
ok 1245 - RBW1 a changed source note writes nothing
  ---
  duration_ms: 1.423938
  ...
# Subtest: RBW2 one changed T note still lands the others and omits it from BLOCKS
ok 1246 - RBW2 one changed T note still lands the others and omits it from BLOCKS
  ---
  duration_ms: 1.561571
  ...
# Subtest: RBW3 already-present picks write nothing
ok 1247 - RBW3 already-present picks write nothing
  ---
  duration_ms: 1.379384
  ...
# Subtest: RBW4 cleanup runs for T's that committed when N lives in today's daily note
ok 1248 - RBW4 cleanup runs for T's that committed when N lives in today's daily note
  ---
  duration_ms: 2.565507
  ...
# Subtest: RBW6 counted forward two-lane dependents prepare N once
ok 1249 - RBW6 counted forward two-lane dependents prepare N once
  ---
  duration_ms: 10.344146
  ...
# Subtest: A1 N above two T's in one note matches forward (open and closed note)
ok 1250 - A1 N above two T's in one note matches forward (open and closed note)
  ---
  duration_ms: 14.233621
  ...
# Subtest: A1 N below two T's matches forward bytes
ok 1251 - A1 N below two T's matches forward bytes
  ---
  duration_ms: 2.657002
  ...
# Subtest: A2 forward stamps the dependent when a prerequisite above gains BLOCKS
ok 1252 - A2 forward stamps the dependent when a prerequisite above gains BLOCKS
  ---
  duration_ms: 0.743589
  ...
# Subtest: A1 mixed same-note and cross-note picks keep N's lane rise (RBP7 variant)
ok 1253 - A1 mixed same-note and cross-note picks keep N's lane rise (RBP7 variant)
  ---
  duration_ms: 2.652374
  ...
# Subtest: A1 RBP1 with N truly lacking ^id is prompted an id and matches forward
ok 1254 - A1 RBP1 with N truly lacking ^id is prompted an id and matches forward
  ---
  duration_ms: 1.802221
  ...
# Subtest: A1 N lacking ^id in a closed note above T keeps its BLOCKS line under N
ok 1255 - A1 N lacking ^id in a closed note above T keeps its BLOCKS line under N
  ---
  duration_ms: 1.216092
  ...
# Subtest: A3 mirror lists the committed T's by identity (N above T1, X, T2)
ok 1256 - A3 mirror lists the committed T's by identity (N above T1, X, T2)
  ---
  duration_ms: 1.277238
  ...
# Subtest: A4 notices name T, not N (add, remove, project, counted)
ok 1257 - A4 notices name T, not N (add, remove, project, counted)
  ---
  duration_ms: 5.907597
  ...
# Subtest: A5 the writer's stale notice is returned once and never shown by the writer
ok 1258 - A5 the writer's stale notice is returned once and never shown by the writer
  ---
  duration_ms: 0.290865
  ...
# Subtest: A6 a changed T row (rawLine) is refused before any write
ok 1259 - A6 a changed T row (rawLine) is refused before any write
  ---
  duration_ms: 0.202316
  ...
# Subtest: A7 RBW2 keeps the failed T's Pomodoro link and consumes the committed one
ok 1260 - A7 RBW2 keeps the failed T's Pomodoro link and consumes the committed one
  ---
  duration_ms: 1.684145
  ...
# Subtest: A8 closed-note T guards run when the gesture is applied
ok 1261 - A8 closed-note T guards run when the gesture is applied
  ---
  duration_ms: 2.63029
  ...
# Subtest: A9 a ^prj T's residents recover with [unblocked::] when N lives in a daily note
ok 1262 - A9 a ^prj T's residents recover with [unblocked::] when N lives in a daily note
  ---
  duration_ms: 8.74747
  ...
# Subtest: A5 a preparation no write can carry fails the plan instead of being dropped
ok 1263 - A5 a preparation no write can carry fails the plan instead of being dropped
  ---
  duration_ms: 0.897063
  ...
# Subtest: applyDependencyEdit adding a first cross-note prerequisite keeps the dependent's cursor
ok 1264 - applyDependencyEdit adding a first cross-note prerequisite keeps the dependent's cursor
  ---
  duration_ms: 1.705726
  ...
# Subtest: applyBlocksEdit giving a source its first BLOCKS line keeps the source's cursor
ok 1265 - applyBlocksEdit giving a source its first BLOCKS line keeps the source's cursor
  ---
  duration_ms: 3.757893
  ...
# Subtest: nav BK1–BK2 accept canonical BLOCKS lines
ok 1266 - nav BK1–BK2 accept canonical BLOCKS lines
  ---
  duration_ms: 2.077385
  ...
# Subtest: nav BK3–BK11 canonicalise
ok 1267 - nav BK3–BK11 canonicalise
  ---
  duration_ms: 0.559157
  ...
# Subtest: nav BK12 empty, BK13–BK15 malformed
ok 1268 - nav BK12 empty, BK13–BK15 malformed
  ---
  duration_ms: 0.188008
  ...
# Subtest: nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse
ok 1269 - nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse
  ---
  duration_ms: 0.349367
  ...
# Subtest: nav BK21 code-point sort and writer format
ok 1270 - nav BK21 code-point sort and writer format
  ---
  duration_ms: 0.275516
  ...
# Subtest: nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS
ok 1271 - nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS
  ---
  duration_ms: 0.438558
  ...
# Subtest: nav BW18 conversion drops BLOCKS like Sub-projects
ok 1272 - nav BW18 conversion drops BLOCKS like Sub-projects
  ---
  duration_ms: 0.954622
  ...
# Subtest: nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner
ok 1273 - nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner
  ---
  duration_ms: 0.712119
  ...
# Subtest: nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists
ok 1274 - nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists
  ---
  duration_ms: 1.504101
  ...
# Subtest: nav MC1/MC2 deferred Pomodoro cleanup skips managed lines
ok 1275 - nav MC1/MC2 deferred Pomodoro cleanup skips managed lines
  ---
  duration_ms: 0.378362
  ...
# Subtest: showBlocksStage opens from a task with reverse CURRENT and RESULTS
ok 1276 - showBlocksStage opens from a task with reverse CURRENT and RESULTS
  ---
  duration_ms: 14.665084
  ...
# Subtest: showBlocksStage opens from a counted session
ok 1277 - showBlocksStage opens from a counted session
  ---
  duration_ms: 1.6708
  ...
# Subtest: showBlocksStage opens on a Task Link target note
ok 1278 - showBlocksStage opens on a Task Link target note
  ---
  duration_ms: 1.426492
  ...
# Subtest: RBU1 empty query uses today-first then In Progress, Next, same-note, rest
ok 1279 - RBU1 empty query uses today-first then In Progress, Next, same-note, rest
  ---
  duration_ms: 1.618058
  ...
# Subtest: RBU2 today-linked rows carry 🍅 running and strip names the entry
ok 1280 - RBU2 today-linked rows carry 🍅 running and strip names the entry
  ---
  duration_ms: 0.943241
  ...
# Subtest: RBU3 CURRENT 🔑 only when N is the last reason
ok 1281 - RBU3 CURRENT 🔑 only when N is the last reason
  ---
  duration_ms: 1.51388
  ...
# Subtest: RBU4 footer verbs are block, remove, and apply N
ok 1282 - RBU4 footer verbs are block, remove, and apply N
  ---
  duration_ms: 1.548215
  ...
# Subtest: RBU5 subtitle at rest, with marks, and names this task first
ok 1283 - RBU5 subtitle at rest, with marks, and names this task first
  ---
  duration_ms: 1.496807
  ...
# Subtest: RBG1 N itself is excluded from RESULTS
ok 1284 - RBG1 N itself is excluded from RESULTS
  ---
  duration_ms: 0.69174
  ...
# Subtest: RBG2 a cycle disables the row with path tooltip copy
ok 1285 - RBG2 a cycle disables the row with path tooltip copy
  ---
  duration_ms: 0.856525
  ...
# Subtest: RBG3 ^prj T with N inside the project is inside this project
ok 1286 - RBG3 ^prj T with N inside the project is inside this project
  ---
  duration_ms: 1.553365
  ...
# Subtest: RBG3 descendant N disables the parent project as a sub-project
ok 1287 - RBG3 descendant N disables the parent project as a sub-project
  ---
  duration_ms: 1.108857
  ...
# Subtest: RBG4 a malformed or second Depends-On line is guarded
ok 1288 - RBG4 a malformed or second Depends-On line is guarded
  ---
  duration_ms: 0.694566
  ...
# Subtest: RBG5 stale refuse reopens in the Blocks direction
ok 1289 - RBG5 stale refuse reopens in the Blocks direction
  ---
  duration_ms: 2.947247
  ...
# Subtest: RBG5 for T: a T changed after stage open refuses once and writes nothing
ok 1290 - RBG5 for T: a T changed after stage open refuses once and writes nothing
  ---
  duration_ms: 2.290052
  ...
# Subtest: today's links survive a pool refresh that lands while the daily note loads
ok 1291 - today's links survive a pool refresh that lands while the daily note loads
  ---
  duration_ms: 32.21721
  ...
# Subtest: RBG8 Esc from the stage or the block-ID prompt writes nothing
ok 1292 - RBG8 Esc from the stage or the block-ID prompt writes nothing
  ---
  duration_ms: 2.376626
  ...
# Subtest: missing source ^id opens the block-ID prompt and Esc allocates none
ok 1293 - missing source ^id opens the block-ID prompt and Esc allocates none
  ---
  duration_ms: 1.353804
  ...
# Subtest: RBP11 inbox route runs first then the Blocks write
ok 1294 - RBP11 inbox route runs first then the Blocks write
  ---
  duration_ms: 0.961175
  ...
# Subtest: RBW5 review walk stays unless the commit takes N out of today's walk
ok 1295 - RBW5 review walk stays unless the commit takes N out of today's walk
  ---
  duration_ms: 5.669273
  ...
# Subtest: marks commit add and remove together; counted uses k/n block
ok 1296 - marks commit add and remove together; counted uses k/n block
  ---
  duration_ms: 3.044892
  ...
# Subtest: strip text covers RESULTS, BLOCKED, CURRENT, disabled, marks, and ^prj
ok 1297 - strip text covers RESULTS, BLOCKED, CURRENT, disabled, marks, and ^prj
  ---
  duration_ms: 0.408781
  ...
# Subtest: counted subtitle drops the ⇥ hint because marks are off in counted sessions
ok 1298 - counted subtitle drops the ⇥ hint because marks are off in counted sessions
  ---
  duration_ms: 0.923212
  ...
# Subtest: 🔑 tooltip and 🍅 tooltip render on badges
ok 1299 - 🔑 tooltip and 🍅 tooltip render on badges
  ---
  duration_ms: 1.015168
  ...
# Subtest: Tab marks Blocks CURRENT rows and Enter removes both dependents
ok 1300 - Tab marks Blocks CURRENT rows and Enter removes both dependents
  ---
  duration_ms: 15.196781
  ...
# Subtest: SB1-SB9 dependent IDs match the successor mint vectors
ok 1301 - SB1-SB9 dependent IDs match the successor mint vectors
  ---
  duration_ms: 2.082565
  ...
# Subtest: BW1 same-note add mints and writes BLOCKS in the dependent's single transaction
ok 1302 - BW1 same-note add mints and writes BLOCKS in the dependent's single transaction
  ---
  duration_ms: 10.351971
  ...
# Subtest: BW2 cross-note add follows the dependent commit and writes the target note
ok 1303 - BW2 cross-note add follows the dependent commit and writes the target note
  ---
  duration_ms: 2.154914
  ...
# Subtest: BW4 cross-note target preparation precedes the reverse-line preimage
ok 1304 - BW4 cross-note target preparation precedes the reverse-line preimage
  ---
  duration_ms: 1.965181
  ...
# Subtest: BW3 stale cross-note preimage leaves the forward write standing and shows the suffix
ok 1305 - BW3 stale cross-note preimage leaves the forward write standing and shows the suffix
  ---
  duration_ms: 1.575076
  ...
# Subtest: BW5 removal deletes the reverse line when its last dependent leaves
ok 1306 - BW5 removal deletes the reverse line when its last dependent leaves
  ---
  duration_ms: 3.31575
  ...
# Subtest: BW6 an already mirrored edge is a byte-identical no-op
ok 1307 - BW6 an already mirrored edge is a byte-identical no-op
  ---
  duration_ms: 0.654079
  ...
# Subtest: BW7 closed owners stay frozen
ok 1308 - BW7 closed owners stay frozen
  ---
  duration_ms: 1.460127
  ...
# Subtest: BW8 malformed reverse lines stay untouched and report the failed mirror
ok 1309 - BW8 malformed reverse lines stay untouched and report the failed mirror
  ---
  duration_ms: 1.521043
  ...
# Subtest: BW15 config defaults on, honors false, and invalid values fall back on
ok 1310 - BW15 config defaults on, honors false, and invalid values fall back on
  ---
  duration_ms: 0.72279
  ...
# Subtest: BW17 planner output follows BK21 Unicode code-point ordering
ok 1311 - BW17 planner output follows BK21 Unicode code-point ordering
  ---
  duration_ms: 0.45578
  ...
# Subtest: duplicate BLOCKS children merge their known dependents and preserve CRLF
ok 1312 - duplicate BLOCKS children merge their known dependents and preserve CRLF
  ---
  duration_ms: 0.486809
  ...
# Subtest: BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270)
ok 1313 - BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270)
  ---
  duration_ms: 4.41064
  ...
# Subtest: counted remove-from-all drops every dependent from the same-note BLOCKS line (420)
ok 1314 - counted remove-from-all drops every dependent from the same-note BLOCKS line (420)
  ---
  duration_ms: 1.464546
  ...
# Subtest: vault counted add composes cross-note follow-ups for every source (420)
ok 1315 - vault counted add composes cross-note follow-ups for every source (420)
  ---
  duration_ms: 2.325219
  ...
# Subtest: marked batch add writes every same-note target onto BLOCKS in one plan (430)
ok 1316 - marked batch add writes every same-note target onto BLOCKS in one plan (430)
  ---
  duration_ms: 0.694796
  ...
# Subtest: counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600)
ok 1317 - counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600)
  ---
  duration_ms: 5.929628
  ...
# Subtest: BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves
ok 1318 - BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves
  ---
  duration_ms: 2.821346
  ...
# Subtest: BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS
ok 1319 - BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS
  ---
  duration_ms: 2.679956
  ...
# Subtest: hand-edit clear path routes through the BLOCKS seam (600)
ok 1320 - hand-edit clear path routes through the BLOCKS seam (600)
  ---
  duration_ms: 0.557665
  ...
# Subtest: BW18 conversion never copies a BLOCKS line as a user child
ok 1321 - BW18 conversion never copies a BLOCKS line as a user child
  ---
  duration_ms: 0.538348
  ...
# Subtest: BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it
ok 1322 - BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it
  ---
  duration_ms: 2.894225
  ...
# Subtest: review checklist group helpers format exact completion and close notices
ok 1323 - review checklist group helpers format exact completion and close notices
  ---
  duration_ms: 1.908413
  ...
# Subtest: claim declines without a current exact PRE/POST walk landing
ok 1324 - claim declines without a current exact PRE/POST walk landing
  ---
  duration_ms: 6.644015
  ...
# Subtest: a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
ok 1325 - a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
  ---
  duration_ms: 2.99643
  ...
# Subtest: checklist Ctrl+Enter holds its landing through the actual successor picker
ok 1326 - checklist Ctrl+Enter holds its landing through the actual successor picker
  ---
  duration_ms: 10.187146
  ...
# Subtest: seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
ok 1327 - seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
  ---
  duration_ms: 15.27034
  ...
# Subtest: a landed [?] checklist chore is claimed and completed
ok 1328 - a landed [?] checklist chore is claimed and completed
  ---
  duration_ms: 1.242301
  ...
# Subtest: ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
ok 1329 - ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
  ---
  duration_ms: 2.556721
  ...
# Subtest: live successor filtering skips a stale completed row
ok 1330 - live successor filtering skips a stale completed row
  ---
  duration_ms: 3.384501
  ...
# Subtest: live group filtering reads each cross-note path once
ok 1331 - live group filtering reads each cross-note path once
  ---
  duration_ms: 0.672765
  ...
# Subtest: Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
ok 1332 - Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
  ---
  duration_ms: 2.544507
  ...
# Subtest: POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
ok 1333 - POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
  ---
  duration_ms: 1.279813
  ...
# Subtest: ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
ok 1334 - ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
  ---
  duration_ms: 0.67037
  ...
# Subtest: completion failure preserves cursor and landing and reports the Tasks failure
ok 1335 - completion failure preserves cursor and landing and reports the Tasks failure
  ---
  duration_ms: 0.308799
  ...
# Subtest: reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
ok 1336 - reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
  ---
  duration_ms: 1.212294
  ...
# Subtest: Alt+F on PRE stays with remaining PRE count and never stamps
ok 1337 - Alt+F on PRE stays with remaining PRE count and never stamps
  ---
  duration_ms: 4.812016
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a stale cache
ok 1338 - Ctrl+Alt+F completes seven PRE rows from a stale cache
  ---
  duration_ms: 10.661052
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a refreshed cache
ok 1339 - Ctrl+Alt+F completes seven PRE rows from a refreshed cache
  ---
  duration_ms: 3.962024
  ...
# Subtest: POST stays put with the closing notice
ok 1340 - POST stays put with the closing notice
  ---
  duration_ms: 0.922411
  ...
# Subtest: manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
ok 1341 - manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
  ---
  duration_ms: 1.358212
  ...
# Subtest: manual Ctrl+Enter then ]s from a stale cache uses text-first identity
ok 1342 - manual Ctrl+Enter then ]s from a stale cache uses text-first identity
  ---
  duration_ms: 1.839631
  ...
# Subtest: counted Alt+F skips checklist rows with the skip tail
ok 1343 - counted Alt+F skips checklist rows with the skip tail
  ---
  duration_ms: 4.962924
  ...
# Subtest: missing cycler gate on a PRE row writes nothing
ok 1344 - missing cycler gate on a PRE row writes nothing
  ---
  duration_ms: 0.547976
  ...
# Subtest: missing ledger checklist gate on a tagged line writes nothing
ok 1345 - missing ledger checklist gate on a tagged line writes nothing
  ---
  duration_ms: 0.569908
  ...
# Subtest: a tagged line that is not a queue match falls through to recurring refusal
ok 1346 - a tagged line that is not a queue match falls through to recurring refusal
  ---
  duration_ms: 0.476239
  ...
# Subtest: formatFreshStampChecklistSkipTail names the skipped count
ok 1347 - formatFreshStampChecklistSkipTail names the skipped count
  ---
  duration_ms: 0.132072
  ...
# Subtest: partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
ok 1348 - partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
  ---
  duration_ms: 0.174253
  ...
# Subtest: Task Link Alt+F skips a PRE target with the skip notice
ok 1349 - Task Link Alt+F skips a PRE target with the skip notice
  ---
  duration_ms: 1.808713
  ...
# Subtest: P0 at interval 7 enters P2 with a previewed decay date and kept tail
ok 1350 - P0 at interval 7 enters P2 with a previewed decay date and kept tail
  ---
  duration_ms: 3.044993
  ...
# Subtest: P0 at interval 30 enters P3
ok 1351 - P0 at interval 30 enters P3
  ---
  duration_ms: 0.449648
  ...
# Subtest: fixed enter overrides the interval scan
ok 1352 - fixed enter overrides the interval scan
  ---
  duration_ms: 0.426033
  ...
# Subtest: unknown enter disables Not now without disabling Keep/Reword
ok 1353 - unknown enter disables Not now without disabling Keep/Reword
  ---
  duration_ms: 0.385616
  ...
# Subtest: P0 with no suitable level stays unavailable and never shortens the lease
ok 1354 - P0 with no suitable level stays unavailable and never shortens the lease
  ---
  duration_ms: 0.335871
  ...
# Subtest: custom level order resolves entry in ladder order
ok 1355 - custom level order resolves entry in ladder order
  ---
  duration_ms: 0.274975
  ...
# Subtest: unknown priority value disables Not now only
ok 1356 - unknown priority value disables Not now only
  ---
  duration_ms: 0.316164
  ...
# Subtest: prioritized P2 below its roll limit stays on the same level
ok 1357 - prioritized P2 below its roll limit stays on the same level
  ---
  duration_ms: 0.539741
  ...
# Subtest: P2 at its roll limit decays to P3
ok 1358 - P2 at its roll limit decays to P3
  ---
  duration_ms: 0.651844
  ...
# Subtest: P2 streak derives from the task Schedule Log
ok 1359 - P2 streak derives from the task Schedule Log
  ---
  duration_ms: 2.699703
  ...
# Subtest: configured decay:false keeps rolling past the limit
ok 1360 - configured decay:false keeps rolling past the limit
  ---
  duration_ms: 0.303108
  ...
# Subtest: per-level rolls:0 decays immediately
ok 1361 - per-level rolls:0 decays immediately
  ---
  duration_ms: 0.24646
  ...
# Subtest: terminal cancel substitutes a truthful same-level card roll
ok 1362 - terminal cancel substitutes a truthful same-level card roll
  ---
  duration_ms: 0.289542
  ...
# Subtest: no future date in the window refuses Not now
ok 1363 - no future date in the window refuses Not now
  ---
  duration_ms: 0.190253
  ...
# Subtest: Less often steps 7/14/30 to the next preset with a decision reason
ok 1364 - Less often steps 7/14/30 to the next preset with a decision reason
  ---
  duration_ms: 0.496047
  ...
# Subtest: Less often at 90+ opens the constrained custom picker; 365 is unavailable
ok 1365 - Less often at 90+ opens the constrained custom picker; 365 is unavailable
  ---
  duration_ms: 0.261279
  ...
# Subtest: previewed dates are stable for one random draw
ok 1366 - previewed dates are stable for one random draw
  ---
  duration_ms: 0.24069
  ...
# Subtest: Keep saturates at 999 and Drop preserves keeps history
ok 1367 - Keep saturates at 999 and Drop preserves keeps history
  ---
  duration_ms: 0.311815
  ...
# Subtest: kept tails preserve roll classification; decisions break it deliberately
ok 1368 - kept tails preserve roll classification; decisions break it deliberately
  ---
  duration_ms: 0.779168
  ...
# Subtest: invalid priority config offers no priority-changing action
ok 1369 - invalid priority config offers no priority-changing action
  ---
  duration_ms: 0.208708
  ...
# Subtest: decay off disables Not now but keeps counting
ok 1370 - decay off disables Not now but keeps counting
  ---
  duration_ms: 0.197357
  ...
# Subtest: explicit level picks cover the ladder with previewed rolls
ok 1371 - explicit level picks cover the ladder with previewed rolls
  ---
  duration_ms: 0.755132
  ...
# Subtest: card model is deeply frozen
ok 1372 - card model is deeply frozen
  ---
  duration_ms: 0.207316
  ...
# Subtest: single Alt+F on an at-limit task opens the card and writes nothing
ok 1373 - single Alt+F on an at-limit task opens the card and writes nothing
  ---
  duration_ms: 8.580821
  ...
# Subtest: dismissing the card writes nothing and does not advance
ok 1374 - dismissing the card writes nothing and does not advance
  ---
  duration_ms: 1.279061
  ...
# Subtest: early dates open the card and write nothing
ok 1375 - early dates open the card and write nothing
  ---
  duration_ms: 1.149063
  ...
# Subtest: namespace v5 with decide true stamps counted and opens no card
ok 1376 - namespace v5 with decide true stamps counted and opens no card
  ---
  duration_ms: 4.344924
  ...
# Subtest: stale task-line change writes nothing
ok 1377 - stale task-line change writes nothing
  ---
  duration_ms: 1.113697
  ...
# Subtest: stale local-day change writes nothing
ok 1378 - stale local-day change writes nothing
  ---
  duration_ms: 1.19451
  ...
# Subtest: stale decay-config change writes nothing
ok 1379 - stale decay-config change writes nothing
  ---
  duration_ms: 0.958209
  ...
# Subtest: stale priority-ladder config writes nothing
ok 1380 - stale priority-ladder config writes nothing
  ---
  duration_ms: 1.381287
  ...
# Subtest: stale child Schedule Log writes nothing
ok 1381 - stale child Schedule Log writes nothing
  ---
  duration_ms: 1.726386
  ...
# Subtest: Not now stamps, clears keeps, and advances exactly once
ok 1382 - Not now stamps, clears keeps, and advances exactly once
  ---
  duration_ms: 6.099172
  ...
# Subtest: Keep counts once and saturates at 999 without reset
not ok 1383 - Keep counts once and saturates at 999 without reset
  ---
  duration_ms: 1.868487
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-navigation-decision-card-handlers.cjs:546:1'
  failureType: 'testCodeFailure'
  error: '- [ ] #task Buy milk [fresh:: 2026-09-30] [keeps:: 3]'
  code: 'ERR_ASSERTION'
  name: 'AssertionError'
  expected:
  actual: 'Update Bob Ledger Tools to record review stats'
  operator: 'match'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-navigation-decision-card-handlers.cjs:569:12)
    async Test.run (node:internal/test_runner/test:980:9)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Reword stamps, clears, logs, and never advances
ok 1384 - Reword stamps, clears, logs, and never advances
  ---
  duration_ms: 1.369074
  ...
# Subtest: Drop cancels with the dropped-after-keeps reason and keeps history
ok 1385 - Drop cancels with the dropped-after-keeps reason and keeps history
  ---
  duration_ms: 0.711488
  ...
# Subtest: Less often at 90+ opens the picker and dismiss writes nothing
ok 1386 - Less often at 90+ opens the picker and dismiss writes nothing
  ---
  duration_ms: 0.619312
  ...
# Subtest: counted session skips at-limit and counts below-limit
ok 1387 - counted session skips at-limit and counts below-limit
  ---
  duration_ms: 0.803273
  ...
# Subtest: counted session skips at-limit on an early date
ok 1388 - counted session skips at-limit on an early date
  ---
  duration_ms: 0.667634
  ...
# Subtest: counted session with every target skipped writes nothing
ok 1389 - counted session with every target skipped writes nothing
  ---
  duration_ms: 0.589716
  ...
# Subtest: availability: decay on (or absent) may ask; decay off never asks
ok 1390 - availability: decay on (or absent) may ask; decay off never asks
  ---
  duration_ms: 1.033032
  ...
# Subtest: trigger: only an explicit decide row decides
ok 1391 - trigger: only an explicit decide row decides
  ---
  duration_ms: 0.186436
  ...
# Subtest: partition: exact at-limit rows skip, everything else stamps
ok 1392 - partition: exact at-limit rows skip, everything else stamps
  ---
  duration_ms: 0.690007
  ...
# Subtest: partition: empty and malformed input stamps nothing and skips nothing
ok 1393 - partition: empty and malformed input stamps nothing and skips nothing
  ---
  duration_ms: 0.155196
  ...
# Subtest: partition: enabled false stamps decision rows (older namespace fallback)
ok 1394 - partition: enabled false stamps decision rows (older namespace fallback)
  ---
  duration_ms: 0.158593
  ...
# Subtest: skip wording: singular, plural, and all-skipped notices
ok 1395 - skip wording: singular, plural, and all-skipped notices
  ---
  duration_ms: 0.194471
  ...
# Subtest: reword cursor: lands at the end of the task body before metadata
ok 1396 - reword cursor: lands at the end of the task body before metadata
  ---
  duration_ms: 0.384444
  ...
# Subtest: captured age: optional context ages, null when created is missing
ok 1397 - captured age: optional context ages, null when created is missing
  ---
  duration_ms: 0.454237
  ...
# Subtest: rows: P0 entry shows the recommended Not now with a clean window
ok 1398 - rows: P0 entry shows the recommended Not now with a clean window
  ---
  duration_ms: 3.198136
  ...
# Subtest: rows: invalid priority config disables Not now and levels, keeps safe rows
ok 1399 - rows: invalid priority config disables Not now and levels, keeps safe rows
  ---
  duration_ms: 0.72302
  ...
# Subtest: rows: picker-mode Less often and 365-day cap
ok 1400 - rows: picker-mode Less often and 365-day cap
  ---
  duration_ms: 1.00023
  ...
# Subtest: rows: terminal ladder keeps Enter available and never cancels
ok 1401 - rows: terminal ladder keeps Enter available and never cancels
  ---
  duration_ms: 0.624422
  ...
# Subtest: modal: Enter approves once; later keys cannot approve again
ok 1402 - modal: Enter approves once; later keys cannot approve again
  ---
  duration_ms: 0.53977
  ...
# Subtest: modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
ok 1403 - modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
  ---
  duration_ms: 0.358054
  ...
# Subtest: modal: key repeat and modified keys never approve
ok 1404 - modal: key repeat and modified keys never approve
  ---
  duration_ms: 0.234899
  ...
# Subtest: modal: Esc changes nothing — dismiss without a choice
ok 1405 - modal: Esc changes nothing — dismiss without a choice
  ---
  duration_ms: 0.153934
  ...
# Subtest: modal: unavailable actions cannot be chosen
ok 1406 - modal: unavailable actions cannot be chosen
  ---
  duration_ms: 0.236191
  ...
# Subtest: modal: a double callback applies once
ok 1407 - modal: a double callback applies once
  ---
  duration_ms: 0.126141
  ...
# Subtest: capability: the nav api exposes the card while loaded
ok 1408 - capability: the nav api exposes the card while loaded
  ---
  duration_ms: 0.421855
  ...
# Subtest: capability: unload drops the card so marks stop promising it
ok 1409 - capability: unload drops the card so marks stop promising it
  ---
  duration_ms: 0.143023
  ...
# Subtest: ladder lookup: the first priority property wins, null without one
ok 1410 - ladder lookup: the first priority property wins, null without one
  ---
  duration_ms: 0.168531
  ...
# Subtest: stage entry resolves the line itself and refuses prose
ok 1411 - stage entry resolves the line itself and refuses prose
  ---
  duration_ms: 3.962976
  ...
# Subtest: Ctrl+Shift+P on a BLOCKS line opens the owner's Blocks stage directly
ok 1412 - Ctrl+Shift+P on a BLOCKS line opens the owner's Blocks stage directly
  ---
  duration_ms: 1.360497
  ...
# Subtest: Ctrl+Shift+P hotkey path on a BLOCKS line opens the owner's Blocks stage directly
ok 1413 - Ctrl+Shift+P hotkey path on a BLOCKS line opens the owner's Blocks stage directly
  ---
  duration_ms: 0.740043
  ...
# Subtest: Ctrl+Shift+Alt+B on a BLOCKS or Depends-On line opens the owner's Blocks stage
ok 1414 - Ctrl+Shift+Alt+B on a BLOCKS or Depends-On line opens the owner's Blocks stage
  ---
  duration_ms: 0.448295
  ...
# Subtest: Ctrl+Shift+P on a Depends-On line is unchanged forward behavior
ok 1415 - Ctrl+Shift+P on a Depends-On line is unchanged forward behavior
  ---
  duration_ms: 0.428298
  ...
# Subtest: Ctrl+Shift+P on a plain child bullet and a nested Task Link are unchanged (3e359a6)
ok 1416 - Ctrl+Shift+P on a plain child bullet and a nested Task Link are unchanged (3e359a6)
  ---
  duration_ms: 7.368124
  ...
# Subtest: forward counted mixed row in BLOCKED keeps the waits-on badge (3e359a6 order)
ok 1417 - forward counted mixed row in BLOCKED keeps the waits-on badge (3e359a6 order)
  ---
  duration_ms: 2.428145
  ...
# Subtest: api.blocks opens the stage and removes only a listed dependent
ok 1418 - api.blocks opens the stage and removes only a listed dependent
  ---
  duration_ms: 1.995449
  ...
# Subtest: api.blocks removeDependent on an owner with no ^id is not-a-dependent
ok 1419 - api.blocks removeDependent on an owner with no ^id is not-a-dependent
  ---
  duration_ms: 0.453966
  ...
# Subtest: stage canonical order ranks \#hide last ahead of the lane
ok 1420 - stage canonical order ranks \#hide last ahead of the lane
  ---
  duration_ms: 0.467573
  ...
# Subtest: stage empty query shows same-note plus In Progress and Next only
ok 1421 - stage empty query shows same-note plus In Progress and Next only
  ---
  duration_ms: 2.442583
  ...
# Subtest: stage cap appends a type-to-search-more hint row
ok 1422 - stage cap appends a type-to-search-more hint row
  ---
  duration_ms: 2.591077
  ...
# Subtest: stage BLOCKED rows carry waits-on counts and short guard reasons
ok 1423 - stage BLOCKED rows carry waits-on counts and short guard reasons
  ---
  duration_ms: 1.3724
  ...
# Subtest: stage removal notices name the task description, not the block id
ok 1424 - stage removal notices name the task description, not the block id
  ---
  duration_ms: 0.49752
  ...
# Subtest: stage Task Link batches keep Depends on without refusal
ok 1425 - stage Task Link batches keep Depends on without refusal
  ---
  duration_ms: 0.386047
  ...
# Subtest: stage batch cycle check runs on the post-batch graph
ok 1426 - stage batch cycle check runs on the post-batch graph
  ---
  duration_ms: 0.435401
  ...
# Subtest: stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
ok 1427 - stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
  ---
  duration_ms: 9.959974
  ...
# Subtest: stage stale single add refuses and reopens
ok 1428 - stage stale single add refuses and reopens
  ---
  duration_ms: 1.342272
  ...
# Subtest: Task Link Depends on focuses a linked note open in a background tab
ok 1429 - Task Link Depends on focuses a linked note open in a background tab
  ---
  duration_ms: 0.48193
  ...
# Subtest: Task Link Blocks focuses the linked note and opens Blocks directly
ok 1430 - Task Link Blocks focuses the linked note and opens Blocks directly
  ---
  duration_ms: 0.491137
  ...
# Subtest: Task Link Depends on refuses clearly when the linked note cannot be focused
    # Subtest: focus reports success but the active view stays elsewhere
    ok 1 - focus reports success but the active view stays elsewhere
      ---
      duration_ms: 0.226131
      ...
    # Subtest: focus reports failure
    ok 2 - focus reports failure
      ---
      duration_ms: 0.16241
      ...
    1..2
ok 1431 - Task Link Depends on refuses clearly when the linked note cannot be focused
  ---
  duration_ms: 0.726918
  ...
# Subtest: stage mirror burst keeps the baseline owner across an insertion above
ok 1432 - stage mirror burst keeps the baseline owner across an insertion above
  ---
  duration_ms: 1003.594912
  ...
# Subtest: stage mirror burst clears on a text-only line deletion
ok 1433 - stage mirror burst clears on a text-only line deletion
  ---
  duration_ms: 1000.99006
  ...
# Subtest: stage mirror vim dd clears the deleted line's owner
ok 1434 - stage mirror vim dd clears the deleted line's owner
  ---
  duration_ms: 1000.965514
  ...
# Subtest: stage badge counts open prerequisites without a block id
ok 1435 - stage badge counts open prerequisites without a block id
  ---
  duration_ms: 3.940993
  ...
# Subtest: stage badge names the future scheduled date with no open prerequisite
ok 1436 - stage badge names the future scheduled date with no open prerequisite
  ---
  duration_ms: 1.242622
  ...
# Subtest: stage badge reads blocked with nothing waiting and no schedule
ok 1437 - stage badge reads blocked with nothing waiting and no schedule
  ---
  duration_ms: 0.773737
  ...
# Subtest: stage vault batch with a stale row refuses and reopens
ok 1438 - stage vault batch with a stale row refuses and reopens
  ---
  duration_ms: 6.053787
  ...
# Subtest: stage opening builds 200/400/1000-task notes without cubic growth
ok 1439 - stage opening builds 200/400/1000-task notes without cubic growth
  ---
  duration_ms: 38.901639
  ...
# Subtest: stage snapshots match standalone parsing across grammar vectors
ok 1440 - stage snapshots match standalone parsing across grammar vectors
  ---
  duration_ms: 4.956503
  ...
# Subtest: stage Warm-empty cache is ready without a vault fallback
ok 1441 - stage Warm-empty cache is ready without a vault fallback
  ---
  duration_ms: 0.461411
  ...
# Subtest: stage opening renders cross-note results with zero writes and cap
ok 1442 - stage opening renders cross-note results with zero writes and cap
  ---
  duration_ms: 40.627524
  ...
# Subtest: stage CURRENT covers same-note, cross-note, blocked, and counted parents
ok 1443 - stage CURRENT covers same-note, cross-note, blocked, and counted parents
  ---
  duration_ms: 2.023313
  ...
# Subtest: stage collections reuse one snapshot per parent
ok 1444 - stage collections reuse one snapshot per parent
  ---
  duration_ms: 0.455339
  ...
# Subtest: stage cold refresh yields, preserves state, and performs no search reads
ok 1445 - stage cold refresh yields, preserves state, and performs no search reads
  ---
  duration_ms: 114.080763
  ...
# Subtest: stage cold refresh abandons after dismissal or replacement
ok 1446 - stage cold refresh abandons after dismissal or replacement
  ---
  duration_ms: 54.738011
  ...
# Subtest: stage 400-task opening finishes in a child process before the parent timeout
ok 1447 - stage 400-task opening finishes in a child process before the parent timeout
  ---
  duration_ms: 99.920453
  ...
# Subtest: stage ranker passes the DK contract vectors verbatim
ok 1448 - stage ranker passes the DK contract vectors verbatim
  ---
  duration_ms: 2.7347
  ...
# Subtest: stage ranker tiers match the capture ranker tier order
ok 1449 - stage ranker tiers match the capture ranker tier order
  ---
  duration_ms: 0.325431
  ...
# Subtest: stage pool excludes daily notes, done, templates, and dot-dirs
ok 1450 - stage pool excludes daily notes, done, templates, and dot-dirs
  ---
  duration_ms: 0.381759
  ...
# Subtest: stage pool collects open vault tasks with buffers as given
ok 1451 - stage pool collects open vault tasks with buffers as given
  ---
  duration_ms: 3.336509
  ...
# Subtest: stage CURRENT resolves same-note, missing, closed, and non-task targets
ok 1452 - stage CURRENT resolves same-note, missing, closed, and non-task targets
  ---
  duration_ms: 2.222241
  ...
# Subtest: stage cycle guard reports the path back to the dependent
ok 1453 - stage cycle guard reports the path back to the dependent
  ---
  duration_ms: 0.939533
  ...
# Subtest: stage view groups CURRENT, RESULTS, and BLOCKED with guards
ok 1454 - stage view groups CURRENT, RESULTS, and BLOCKED with guards
  ---
  duration_ms: 2.410221
  ...
# Subtest: stage view disables cycles and unencodable targets, keeps +id rows
ok 1455 - stage view disables cycles and unencodable targets, keeps +id rows
  ---
  duration_ms: 0.983979
  ...
# Subtest: stage cache tasks normalize across Tasks shapes, buffers win
ok 1456 - stage cache tasks normalize across Tasks shapes, buffers win
  ---
  duration_ms: 0.760281
  ...
# Subtest: stage Task Link mode shows Depends on for one link and batches
ok 1457 - stage Task Link mode shows Depends on for one link and batches
  ---
  duration_ms: 0.816198
  ...
# Subtest: stage mark keys never collide across notes
ok 1458 - stage mark keys never collide across notes
  ---
  duration_ms: 0.195914
  ...
# Subtest: stage display-text locating matches one open task
ok 1459 - stage display-text locating matches one open task
  ---
  duration_ms: 0.23571
  ...
# Subtest: stage selection refusal spans tasks only
ok 1460 - stage selection refusal spans tasks only
  ---
  duration_ms: 0.237714
  ...
# Subtest: stage builder composes pool, current, guards, and pill title
ok 1461 - stage builder composes pool, current, guards, and pill title
  ---
  duration_ms: 1.943379
  ...
# Subtest: stage counted vault add with a stale target refuses and reopens
ok 1462 - stage counted vault add with a stale target refuses and reopens
  ---
  duration_ms: 10.267529
  ...
# Subtest: stage vault commit with a stale write notifies once and reopens
ok 1463 - stage vault commit with a stale write notifies once and reopens
  ---
  duration_ms: 7.351654
  ...
# Subtest: commitVaultRefs refuses a cycle through implicit resident edges
ok 1464 - commitVaultRefs refuses a cycle through implicit resident edges
  ---
  duration_ms: 1.917089
  ...
# Subtest: stage single remove with a stale write notifies once and reopens
ok 1465 - stage single remove with a stale write notifies once and reopens
  ---
  duration_ms: 2.614662
  ...
# Subtest: stage vault single +id guard refuses a stale target
ok 1466 - stage vault single +id guard refuses a stale target
  ---
  duration_ms: 1.250687
  ...
# Subtest: stage vault counted +id guard refuses a stale target
ok 1467 - stage vault counted +id guard refuses a stale target
  ---
  duration_ms: 0.810958
  ...
# Subtest: stage single +id guard refuses a stale target
ok 1468 - stage single +id guard refuses a stale target
  ---
  duration_ms: 0.847698
  ...
# Subtest: stage counted remove with a stale write refuses and reopens
ok 1469 - stage counted remove with a stale write refuses and reopens
  ---
  duration_ms: 2.527966
  ...
# Subtest: stage counted remove counts only changed sources
ok 1470 - stage counted remove counts only changed sources
  ---
  duration_ms: 4.230645
  ...
# Subtest: counted local add on [?] sources reads zero extra notes
ok 1471 - counted local add on [?] sources reads zero extra notes
  ---
  duration_ms: 4.752552
  ...
# Subtest: counted local toggle-off on a Pomodoro-linked [?] source recovers
ok 1472 - counted local toggle-off on a Pomodoro-linked [?] source recovers
  ---
  duration_ms: 5.17534
  ...
# Subtest: stage counted vault add counts only changed sources
ok 1473 - stage counted vault add counts only changed sources
  ---
  duration_ms: 1.829502
  ...
# Subtest: stage counted vault remove counts only changed sources
ok 1474 - stage counted vault remove counts only changed sources
  ---
  duration_ms: 1.303839
  ...
# Subtest: stage +id row prompts without writing
ok 1475 - stage +id row prompts without writing
  ---
  duration_ms: 9.720545
  ...
# Subtest: stage dismissal writes no bytes and drops the batch
ok 1476 - stage dismissal writes no bytes and drops the batch
  ---
  duration_ms: 0.968779
  ...
# Subtest: stage same-note batch commits in one undo group
ok 1477 - stage same-note batch commits in one undo group
  ---
  duration_ms: 9.281037
  ...
# Subtest: stage batch with a stale row refuses and reopens
ok 1478 - stage batch with a stale row refuses and reopens
  ---
  duration_ms: 0.930516
  ...
# Subtest: stage counted add applies to every source task
ok 1479 - stage counted add applies to every source task
  ---
  duration_ms: 34.571404
  ...
# Subtest: stage batch cycle rows stay guarded and write nothing
ok 1480 - stage batch cycle rows stay guarded and write nothing
  ---
  duration_ms: 28.384745
  ...
# Subtest: stage edit-task-dependencies registers with no default hotkey
ok 1481 - stage edit-task-dependencies registers with no default hotkey
  ---
  duration_ms: 3.620631
  ...
# Subtest: task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row
ok 1482 - task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row
  ---
  duration_ms: 1.549838
  ...
# Subtest: task-card-blocks registers Ctrl+Shift+Alt+B and opens the Blocks row
ok 1483 - task-card-blocks registers Ctrl+Shift+Alt+B and opens the Blocks row
  ---
  duration_ms: 0.949472
  ...
# Subtest: stage waits-on badge counts open prerequisites only
ok 1484 - stage waits-on badge counts open prerequisites only
  ---
  duration_ms: 2.295593
  ...
# Subtest: stage cycle tooltip shows task descriptions
ok 1485 - stage cycle tooltip shows task descriptions
  ---
  duration_ms: 1.311103
  ...
# Subtest: stage same-note single add stamps the dependent and keeps its cursor
ok 1486 - stage same-note single add stamps the dependent and keeps its cursor
  ---
  duration_ms: 6.124782
  ...
# Subtest: stage same-note marked batch stamps the dependent and keeps its cursor
ok 1487 - stage same-note marked batch stamps the dependent and keeps its cursor
  ---
  duration_ms: 4.347459
  ...
# Subtest: Tab marks a same-note CURRENT row and Enter removes it
ok 1488 - Tab marks a same-note CURRENT row and Enter removes it
  ---
  duration_ms: 30.473703
  ...
# Subtest: Tab twice unmarks a CURRENT row
ok 1489 - Tab twice unmarks a CURRENT row
  ---
  duration_ms: 27.619515
  ...
# Subtest: Tab mixed CURRENT removal and RESULTS add apply in one commit
ok 1490 - Tab mixed CURRENT removal and RESULTS add apply in one commit
  ---
  duration_ms: 29.544519
  ...
# Subtest: Tab marks a missing CURRENT target and the batch removes it
ok 1491 - Tab marks a missing CURRENT target and the batch removes it
  ---
  duration_ms: 31.290783
  ...
# Subtest: Tab same-note and cross-note CURRENT removals apply in one vault batch
ok 1492 - Tab same-note and cross-note CURRENT removals apply in one vault batch
  ---
  duration_ms: 32.026465
  ...
# Subtest: cross-note add awaits preparation before the one commit
ok 1493 - cross-note add awaits preparation before the one commit
  ---
  duration_ms: 18.106093
  ...
# Subtest: a failed async preparation leaves the dependent untouched
ok 1494 - a failed async preparation leaves the dependent untouched
  ---
  duration_ms: 6.915121
  ...
# Subtest: links to unloaded notes tolerate add, remove, and deleted targets
ok 1495 - links to unloaded notes tolerate add, remove, and deleted targets
  ---
  duration_ms: 3.261365
  ...
# Subtest: Pomodoro-linked dependents recover through the plugin vault read
ok 1496 - Pomodoro-linked dependents recover through the plugin vault read
  ---
  duration_ms: 5.110116
  ...
# Subtest: same-note batch +id stamps the target and links in one undo group
ok 1497 - same-note batch +id stamps the target and links in one undo group
  ---
  duration_ms: 8.462945
  ...
# Subtest: confirmBatchBlockId collects the id and executes the batch
ok 1498 - confirmBatchBlockId collects the id and executes the batch
  ---
  duration_ms: 2.268671
  ...
# Subtest: commitMarkedDependencies executes ready additions at once
ok 1499 - commitMarkedDependencies executes ready additions at once
  ---
  duration_ms: 3.227851
  ...
# Subtest: counted vault add links two siblings bottom-up
ok 1500 - counted vault add links two siblings bottom-up
  ---
  duration_ms: 3.835771
  ...
# Subtest: counted CURRENT rows without a line remove from every source
ok 1501 - counted CURRENT rows without a line remove from every source
  ---
  duration_ms: 6.251384
  ...
# Subtest: a stale editor between await and commit refuses
ok 1502 - a stale editor between await and commit refuses
  ---
  duration_ms: 1.211032
  ...
# Subtest: removeDependencyByRef refuses targets that are not on the line
ok 1503 - removeDependencyByRef refuses targets that are not on the line
  ---
  duration_ms: 1.077637
  ...
# Subtest: kept unloaded links resolve the field id by line position
ok 1504 - kept unloaded links resolve the field id by line position
  ---
  duration_ms: 3.028881
  ...
# Subtest: pendingTargetLine commits the same-note target id with the link
ok 1505 - pendingTargetLine commits the same-note target id with the link
  ---
  duration_ms: 2.225197
  ...
# Subtest: counted vault add commits every source in one transaction
ok 1506 - counted vault add commits every source in one transaction
  ---
  duration_ms: 3.329988
  ...
# Subtest: field-only clears snapshot the vault and recover
ok 1507 - field-only clears snapshot the vault and recover
  ---
  duration_ms: 1.470196
  ...
# Subtest: adds without recovery read zero extra vault notes
ok 1508 - adds without recovery read zero extra vault notes
  ---
  duration_ms: 0.743449
  ...
# Subtest: hand-edit clear recovers Pomodoro-linked dependents to Next
ok 1509 - hand-edit clear recovers Pomodoro-linked dependents to Next
  ---
  duration_ms: 1.00047
  ...
# Subtest: hand-edit clear on a non-Blocked parent reads zero extra notes
ok 1510 - hand-edit clear on a non-Blocked parent reads zero extra notes
  ---
  duration_ms: 0.725254
  ...
# Subtest: writer keeps the full route for duplicate basenames
ok 1511 - writer keeps the full route for duplicate basenames
  ---
  duration_ms: 2.768756
  ...
# Subtest: adds on Blocked parents and non-Blocked mirror touches read nothing
ok 1512 - adds on Blocked parents and non-Blocked mirror touches read nothing
  ---
  duration_ms: 0.993236
  ...
# Subtest: counted vault add loads each source's existing links
ok 1513 - counted vault add loads each source's existing links
  ---
  duration_ms: 3.101742
  ...
# Subtest: counted Ctrl+D on a blockquoted task refuses with the blockquote notice
ok 1514 - counted Ctrl+D on a blockquoted task refuses with the blockquote notice
  ---
  duration_ms: 0.747687
  ...
# Subtest: single Ctrl+D on a quoted task without a field refuses as a blockquote
ok 1515 - single Ctrl+D on a quoted task without a field refuses as a blockquote
  ---
  duration_ms: 0.25664
  ...
# Subtest: confirmSingleBlockId folds the target id into one transaction
ok 1516 - confirmSingleBlockId folds the target id into one transaction
  ---
  duration_ms: 2.573412
  ...
# Subtest: chooseTaskDependency folds a missing target id into one transaction
ok 1517 - chooseTaskDependency folds a missing target id into one transaction
  ---
  duration_ms: 1.784716
  ...
# Subtest: counted remove commits every source in one transaction
ok 1518 - counted remove commits every source in one transaction
  ---
  duration_ms: 2.828589
  ...
# Subtest: DP parse vectors accept, empty, malformed, and not-a-line
ok 1519 - DP parse vectors accept, empty, malformed, and not-a-line
  ---
  duration_ms: 3.341859
  ...
# Subtest: DP30 attributes a Work-Log-nested Depends-On line to the inner task
ok 1520 - DP30 attributes a Work-Log-nested Depends-On line to the inner task
  ---
  duration_ms: 2.583602
  ...
# Subtest: fenced lines never collect as Depends-On lines
ok 1521 - fenced lines never collect as Depends-On lines
  ---
  duration_ms: 0.436443
  ...
# Subtest: DW1 creates the line as the first child
ok 1522 - DW1 creates the line as the first child
  ---
  duration_ms: 5.566025
  ...
# Subtest: DW2 creates the line after a Cancel Log
ok 1523 - DW2 creates the line after a Cancel Log
  ---
  duration_ms: 1.395164
  ...
# Subtest: DW3-DW5 append, remove the middle, and delete on the last link
ok 1524 - DW3-DW5 append, remove the middle, and delete on the last link
  ---
  duration_ms: 5.19053
  ...
# Subtest: DW6-DW7 re-add moves to the end and the field mirrors the line
ok 1525 - DW6-DW7 re-add moves to the end and the field mirrors the line
  ---
  duration_ms: 0.778917
  ...
# Subtest: DW8 tab parents deepen the child by one tab
ok 1526 - DW8 tab parents deepen the child by one tab
  ---
  duration_ms: 1.34145
  ...
# Subtest: DW9 space parents reuse the existing child indent
ok 1527 - DW9 space parents reuse the existing child indent
  ---
  duration_ms: 1.034395
  ...
# Subtest: DW10-DW11 CRLF and final-newline state survive
ok 1528 - DW10-DW11 CRLF and final-newline state survive
  ---
  duration_ms: 1.142661
  ...
# Subtest: DW12-DW14 link form is the shortest unambiguous form
ok 1529 - DW12-DW14 link form is the shortest unambiguous form
  ---
  duration_ms: 0.350208
  ...
# Subtest: archive targets keep the explicit done/ path form
ok 1530 - archive targets keep the explicit done/ path form
  ---
  duration_ms: 0.243094
  ...
# Subtest: DW15 an existing id is never rewritten
ok 1531 - DW15 an existing id is never rewritten
  ---
  duration_ms: 0.428758
  ...
# Subtest: DW16 an unencodable path without an id refuses
ok 1532 - DW16 an unencodable path without an id refuses
  ---
  duration_ms: 0.33514
  ...
# Subtest: DW17 field placement follows fresh and precedes the block id
ok 1533 - DW17 field placement follows fresh and precedes the block id
  ---
  duration_ms: 0.339979
  ...
# Subtest: DW18 legacy children fold into the line
ok 1534 - DW18 legacy children fold into the line
  ---
  duration_ms: 0.921439
  ...
# Subtest: DW19 variants canonicalise to the writer form
ok 1535 - DW19 variants canonicalise to the writer form
  ---
  duration_ms: 1.627306
  ...
# Subtest: adding an open prerequisite blocks the dependent
ok 1536 - adding an open prerequisite blocks the dependent
  ---
  duration_ms: 0.432696
  ...
# Subtest: adding transfers Next and In Progress commitment to the open target
ok 1537 - adding transfers Next and In Progress commitment to the open target
  ---
  duration_ms: 0.669027
  ...
# Subtest: removing the last open prerequisite recovers immediately
ok 1538 - removing the last open prerequisite recovers immediately
  ---
  duration_ms: 0.855052
  ...
# Subtest: removal stays Blocked while another prerequisite is open
ok 1539 - removal stays Blocked while another prerequisite is open
  ---
  duration_ms: 0.388101
  ...
# Subtest: removal stays Blocked with a future schedule
ok 1540 - removal stays Blocked with a future schedule
  ---
  duration_ms: 3.033752
  ...
# Subtest: one gesture commits the dependent note in a single transaction
ok 1541 - one gesture commits the dependent note in a single transaction
  ---
  duration_ms: 2.168851
  ...
# Subtest: a failed preparation leaves the dependent untouched
ok 1542 - a failed preparation leaves the dependent untouched
  ---
  duration_ms: 0.555581
  ...
# Subtest: recovery references follow the line plus covered legacy children
ok 1543 - recovery references follow the line plus covered legacy children
  ---
  duration_ms: 0.567924
  ...
# Subtest: task-block helpers find owners, lines, and insertion points
ok 1544 - task-block helpers find owners, lines, and insertion points
  ---
  duration_ms: 0.376329
  ...
# Subtest: dependency notices follow the contract shapes
ok 1545 - dependency notices follow the contract shapes
  ---
  duration_ms: 0.182088
  ...
# Subtest: nav api v3 resolves results and never throws
ok 1546 - nav api v3 resolves results and never throws
  ---
  duration_ms: 1.406434
  ...
# Subtest: getDependencyInsertLine lands after a Cancel Log subtree
ok 1547 - getDependencyInsertLine lands after a Cancel Log subtree
  ---
  duration_ms: 0.326223
  ...
# Subtest: planner: an ordinary dependent with a block id plus an open add yields one target
ok 1548 - planner: an ordinary dependent with a block id plus an open add yields one target
  ---
  duration_ms: 7.191097
  ...
# Subtest: planner: adding only a closed target yields none
ok 1549 - planner: adding only a closed target yields none
  ---
  duration_ms: 1.099108
  ...
# Subtest: planner: no block id yields none
ok 1550 - planner: no block id yields none
  ---
  duration_ms: 0.542426
  ...
# Subtest: planner: a dependent already [?] with an open add yields a target
ok 1551 - planner: a dependent already [?] with an open add yields a target
  ---
  duration_ms: 1.92271
  ...
# Subtest: planner: a removal yields none
ok 1552 - planner: a removal yields none
  ---
  duration_ms: 1.041528
  ...
# Subtest: planner: mirrorTouch emits no ordinary consumption target
ok 1553 - planner: mirrorTouch emits no ordinary consumption target
  ---
  duration_ms: 0.440451
  ...
# Subtest: planner: ^prj keeps project targets and a deduplicated union
ok 1554 - planner: ^prj keeps project targets and a deduplicated union
  ---
  duration_ms: 2.103766
  ...
# Subtest: suffix helper names the removed count and the failed follow-up
ok 1555 - suffix helper names the removed count and the failed follow-up
  ---
  duration_ms: 0.170556
  ...
# Subtest: applyDependencyEdit cross-file consumes live links and emptied entries
ok 1556 - applyDependencyEdit cross-file consumes live links and emptied entries
  ---
  duration_ms: 7.835898
  ...
# Subtest: applyDependencyEdit removes one live link and reports it
ok 1557 - applyDependencyEdit removes one live link and reports it
  ---
  duration_ms: 2.041417
  ...
# Subtest: applyDependencyEdit keeps the dependent write when the daily preimage changes
ok 1558 - applyDependencyEdit keeps the dependent write when the daily preimage changes
  ---
  duration_ms: 1.329278
  ...
# Subtest: same-file fold lands the dependency and the cleanup in one undo group
ok 1559 - same-file fold lands the dependency and the cleanup in one undo group
  ---
  duration_ms: 2.190852
  ...
# Subtest: setLocalTaskDependencyLink stays synchronous and folds same-file cleanup
ok 1560 - setLocalTaskDependencyLink stays synchronous and folds same-file cleanup
  ---
  duration_ms: 2.914814
  ...
# Subtest: setLocalTaskDependencyLink cross-file continuation removes the live link
ok 1561 - setLocalTaskDependencyLink cross-file continuation removes the live link
  ---
  duration_ms: 12.249694
  ...
# Subtest: same-note marked batch consumes every newly Blocked source
ok 1562 - same-note marked batch consumes every newly Blocked source
  ---
  duration_ms: 10.765642
  ...
# Subtest: counted same-note writer consumes every newly Blocked source
ok 1563 - counted same-note writer consumes every newly Blocked source
  ---
  duration_ms: 4.972141
  ...
# Subtest: counted vault writer consumes every newly Blocked source
ok 1564 - counted vault writer consumes every newly Blocked source
  ---
  duration_ms: 4.747774
  ...
# Subtest: counted ^prj source consumes its project targets
ok 1565 - counted ^prj source consumes its project targets
  ---
  duration_ms: 4.390902
  ...
# Subtest: a dependent without a block id does zero cachedReads even when today's daily exists
ok 1566 - a dependent without a block id does zero cachedReads even when today's daily exists
  ---
  duration_ms: 2.240949
  ...
# Subtest: alignment key ignores fields, the block id, the status and trailing space
ok 1567 - alignment key ignores fields, the block id, the status and trailing space
  ---
  duration_ms: 1.361249
  ...
# Subtest: insertion after a modified line edits that line and inserts after it
ok 1568 - insertion after a modified line edits that line and inserts after it
  ---
  duration_ms: 1.439417
  ...
# Subtest: adjacent prerequisite and parent both change while two lines insert
ok 1569 - adjacent prerequisite and parent both change while two lines insert
  ---
  duration_ms: 0.523299
  ...
# Subtest: deletion at the end of the document
ok 1570 - deletion at the end of the document
  ---
  duration_ms: 0.480888
  ...
# Subtest: insertion at the top and at the end of the document
ok 1571 - insertion at the top and at the end of the document
  ---
  duration_ms: 0.381458
  ...
# Subtest: empty documents align and apply
ok 1572 - empty documents align and apply
  ---
  duration_ms: 0.222234
  ...
# Subtest: CRLF documents insert and delete with CRLF
ok 1573 - CRLF documents insert and delete with CRLF
  ---
  duration_ms: 0.301275
  ...
# Subtest: equal-count shifted edits take the aligned path
ok 1574 - equal-count shifted edits take the aligned path
  ---
  duration_ms: 0.60244
  ...
# Subtest: pure in-place edits keep the line-bounded change shapes
ok 1575 - pure in-place edits keep the line-bounded change shapes
  ---
  duration_ms: 0.654309
  ...
# Subtest: an unchanged document writes nothing
ok 1576 - an unchanged document writes nothing
  ---
  duration_ms: 0.356661
  ...
# Subtest: an explicit final cursor wins over the mapped cursor
ok 1577 - an explicit final cursor wins over the mapped cursor
  ---
  duration_ms: 0.242523
  ...
# Subtest: the machine-write annotation still reaches the transaction
ok 1578 - the machine-write annotation still reaches the transaction
  ---
  duration_ms: 0.163943
  ...
# Subtest: an editor without transaction falls back to bottom-up replaceRange
ok 1579 - an editor without transaction falls back to bottom-up replaceRange
  ---
  duration_ms: 0.320151
  ...
# Subtest: positions map through aligned, changed, gap and deleted lines
ok 1580 - positions map through aligned, changed, gap and deleted lines
  ---
  duration_ms: 0.38221
  ...
# Subtest: a deletion at the end of the document maps to the last line
ok 1581 - a deletion at the end of the document maps to the last line
  ---
  duration_ms: 0.107365
  ...
# Subtest: a gap with new lines maps by offset and clamps to its last line
ok 1582 - a gap with new lines maps by offset and clamps to its last line
  ---
  duration_ms: 0.14687
  ...
# Subtest: seeded property: planned changes rebuild the new text and map unchanged lines
ok 1583 - seeded property: planned changes rebuild the new text and map unchanged lines
  ---
  duration_ms: 43.895354
  ...
# Subtest: a diff past the edit cap becomes one unaligned gap
ok 1584 - a diff past the edit cap becomes one unaligned gap
  ---
  duration_ms: 72.559021
  ...
# Subtest: the CM6 double reproduces the whole-document replacement jump
ok 1585 - the CM6 double reproduces the whole-document replacement jump
  ---
  duration_ms: 0.908735
  ...
# Subtest: first cross-note prerequisite keeps the cursor and the viewport
ok 1586 - first cross-note prerequisite keeps the cursor and the viewport
  ---
  duration_ms: 6.325686
  ...
# Subtest: same-note prerequisite directly above keeps the dependent's line
ok 1587 - same-note prerequisite directly above keeps the dependent's line
  ---
  duration_ms: 3.052677
  ...
# Subtest: removing the last prerequisite keeps the dependent's line
ok 1588 - removing the last prerequisite keeps the dependent's line
  ---
  duration_ms: 3.412614
  ...
# Subtest: a Blocks source gaining its first BLOCKS line keeps its line
ok 1589 - a Blocks source gaining its first BLOCKS line keeps its line
  ---
  duration_ms: 0.38282
  ...
# Subtest: missing ledger-tools api refuses the review namespace
ok 1590 - missing ledger-tools api refuses the review namespace
  ---
  duration_ms: 1.925256
  ...
# Subtest: review jump on an empty queue
ok 1591 - review jump on an empty queue
  ---
  duration_ms: 1.249485
  ...
# Subtest: review jump from a queued task goes to the neighbor
ok 1592 - review jump from a queued task goes to the neighbor
  ---
  duration_ms: 0.873086
  ...
# Subtest: review jump wraps at the ends
ok 1593 - review jump wraps at the ends
  ---
  duration_ms: 0.327786
  ...
# Subtest: review jump from elsewhere goes to the first or last entry
ok 1594 - review jump from elsewhere goes to the first or last entry
  ---
  duration_ms: 0.258333
  ...
# Subtest: review jump matches a moved cursor task by text
ok 1595 - review jump matches a moved cursor task by text
  ---
  duration_ms: 0.210191
  ...
# Subtest: review jump from a just-stamped rank goes to the entry after it
ok 1596 - review jump from a just-stamped rank goes to the entry after it
  ---
  duration_ms: 0.347714
  ...
# Subtest: review jump skips just-stamped keys the lagging cache still shows
ok 1597 - review jump skips just-stamped keys the lagging cache still shows
  ---
  duration_ms: 0.200733
  ...
# Subtest: review jump after stamping everything reports empty or wraps
ok 1598 - review jump after stamping everything reports empty or wraps
  ---
  duration_ms: 0.671181
  ...
# Subtest: review queue line resolves at the entry line
ok 1599 - review queue line resolves at the entry line
  ---
  duration_ms: 0.729813
  ...
# Subtest: review queue line follows a moved line to its unique match
ok 1600 - review queue line follows a moved line to its unique match
  ---
  duration_ms: 0.520805
  ...
# Subtest: review queue line goes stale on duplicates or a missing line
ok 1601 - review queue line goes stale on duplicates or a missing line
  ---
  duration_ms: 0.268162
  ...
# Subtest: review jump notices name the state
ok 1602 - review jump notices name the state
  ---
  duration_ms: 0.567614
  ...
# Subtest: fresh stamp targets refuse closed and recurring tasks
ok 1603 - fresh stamp targets refuse closed and recurring tasks
  ---
  duration_ms: 0.861595
  ...
# Subtest: fresh stamp batch stamps every target and nothing else
ok 1604 - fresh stamp batch stamps every target and nothing else
  ---
  duration_ms: 0.425983
  ...
# Subtest: one refusal refuses the whole fresh stamp batch
ok 1605 - one refusal refuses the whole fresh stamp batch
  ---
  duration_ms: 0.393231
  ...
# Subtest: a throwing stamper refuses the fresh stamp batch
ok 1606 - a throwing stamper refuses the fresh stamp batch
  ---
  duration_ms: 0.244116
  ...
# Subtest: fresh stamp plus Work Log prepends only stamped Pending targets
ok 1607 - fresh stamp plus Work Log prepends only stamped Pending targets
  ---
  duration_ms: 1.646203
  ...
# Subtest: blank Work Log summary and stamp refusal never create a log marker
ok 1608 - blank Work Log summary and stamp refusal never create a log marker
  ---
  duration_ms: 0.326684
  ...
# Subtest: fresh stamp notices adjust the pre-write counts
ok 1609 - fresh stamp notices adjust the pre-write counts
  ---
  duration_ms: 0.274143
  ...
# Subtest: today detection only matches today's fresh field
ok 1610 - today detection only matches today's fresh field
  ---
  duration_ms: 0.252793
  ...
# Subtest: stamped refs match the pre-write queue by line or text
ok 1611 - stamped refs match the pre-write queue by line or text
  ---
  duration_ms: 0.499684
  ...
# Subtest: review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
ok 1612 - review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
  ---
  duration_ms: 0.339969
  ...
# Subtest: tier-aware jump notices name each tier
ok 1613 - tier-aware jump notices name each tier
  ---
  duration_ms: 0.808273
  ...
# Subtest: projects tier walks with commitment rank and empty-project notice
ok 1614 - projects tier walks with commitment rank and empty-project notice
  ---
  duration_ms: 0.27769
  ...
# Subtest: references tier walks with commitment rank and reference notice
ok 1615 - references tier walks with commitment rank and reference notice
  ---
  duration_ms: 0.648357
  ...
# Subtest: jump notices use reviewEntryView when provided and keep the fallback
ok 1616 - jump notices use reviewEntryView when provided and keep the fallback
  ---
  duration_ms: 0.40337
  ...
# Subtest: tier notices fall back without tier ranks and wrap on the last line
ok 1617 - tier notices fall back without tier ranks and wrap on the last line
  ---
  duration_ms: 0.222986
  ...
# Subtest: boundary notice names commitments done and rotten next
ok 1618 - boundary notice names commitments done and rotten next
  ---
  duration_ms: 0.159284
  ...
# Subtest: walk anchor records handled keys with their neighbors
ok 1619 - walk anchor records handled keys with their neighbors
  ---
  duration_ms: 0.708552
  ...
# Subtest: cursor on a live entry wins over a lagging anchor
ok 1620 - cursor on a live entry wins over a lagging anchor
  ---
  duration_ms: 0.40382
  ...
# Subtest: [s after a stamp goes backwards from the anchor
ok 1621 - [s after a stamp goes backwards from the anchor
  ---
  duration_ms: 0.65467
  ...
# Subtest: release-then-]s continues from the anchor successor
ok 1622 - release-then-]s continues from the anchor successor
  ---
  duration_ms: 0.306936
  ...
# Subtest: non-contiguous counted stamp advances past the last handled rank
ok 1623 - non-contiguous counted stamp advances past the last handled rank
  ---
  duration_ms: 0.389403
  ...
# Subtest: anchor wraps at both ends
ok 1624 - anchor wraps at both ends
  ---
  duration_ms: 0.475097
  ...
# Subtest: advance across NEXT to TICKLER to ROTTEN lands the boundary
ok 1625 - advance across NEXT to TICKLER to ROTTEN lands the boundary
  ---
  duration_ms: 0.487561
  ...
# Subtest: tier capability gates on the freshness namespace version
ok 1626 - tier capability gates on the freshness namespace version
  ---
  duration_ms: 0.162009
  ...
# Subtest: empty queue notice reads the upkeep meter
ok 1627 - empty queue notice reads the upkeep meter
  ---
  duration_ms: 0.153934
  ...
# Subtest: refresh row reads lane intervals from the api with the once-Ready return
ok 1628 - refresh row reads lane intervals from the api with the once-Ready return
  ---
  duration_ms: 1.475096
  ...
# Subtest: endpoint jumps select the queue ends with full rank and total
ok 1629 - endpoint jumps select the queue ends with full rank and total
  ---
  duration_ms: 0.702481
  ...
# Subtest: endpoint jumps ignore cursor, anchor, and direction
ok 1630 - endpoint jumps ignore cursor, anchor, and direction
  ---
  duration_ms: 0.264675
  ...
# Subtest: endpoint jumps on empty and one-entry queues
ok 1631 - endpoint jumps on empty and one-entry queues
  ---
  duration_ms: 0.256129
  ...
# Subtest: a visited endpoint is still due under its own anchor
ok 1632 - a visited endpoint is still due under its own anchor
  ---
  duration_ms: 0.173502
  ...
# Subtest: lowercase steps continue from an endpoint anchor
ok 1633 - lowercase steps continue from an endpoint anchor
  ---
  duration_ms: 0.309201
  ...
# Subtest: counted review jump repeat 1 matches omitted repeat
ok 1634 - counted review jump repeat 1 matches omitted repeat
  ---
  duration_ms: 1.118746
  ...
# Subtest: counted review jump from the first entry lands N steps ahead
ok 1635 - counted review jump from the first entry lands N steps ahead
  ---
  duration_ms: 0.306275
  ...
# Subtest: counted review jump from the last entry wraps past the start
ok 1636 - counted review jump from the last entry wraps past the start
  ---
  duration_ms: 0.172439
  ...
# Subtest: counted review jump larger than the queue wraps once
ok 1637 - counted review jump larger than the queue wraps once
  ---
  duration_ms: 0.203458
  ...
# Subtest: counted review jump on a one-entry queue stays there
ok 1638 - counted review jump on a one-entry queue stays there
  ---
  duration_ms: 0.185434
  ...
# Subtest: counted review jump with no origin lands on the Nth entry
ok 1639 - counted review jump with no origin lands on the Nth entry
  ---
  duration_ms: 0.193169
  ...
# Subtest: counted review jump from a shaped anchor takes N surviving successors
ok 1640 - counted review jump from a shaped anchor takes N surviving successors
  ---
  duration_ms: 0.272019
  ...
# Subtest: counted review jump does not change endpoint selection
ok 1641 - counted review jump does not change endpoint selection
  ---
  duration_ms: 0.195843
  ...
# Subtest: a stamped endpoint that moved is stale and cannot land from old text
ok 1642 - a stamped endpoint that moved is stale and cannot land from old text
  ---
  duration_ms: 0.252301
  ...
# Subtest: stale endpoint target reselects the same endpoint in the new queue
ok 1643 - stale endpoint target reselects the same endpoint in the new queue
  ---
  duration_ms: 1.936758
  ...
# Subtest: endpoint retry is bounded and failures preserve the anchor
ok 1644 - endpoint retry is bounded and failures preserve the anchor
  ---
  duration_ms: 0.514812
  ...
# Subtest: endpoint jump to ROTTEN carries no boundary preamble
ok 1645 - endpoint jump to ROTTEN carries no boundary preamble
  ---
  duration_ms: 1.918732
  ...
# Subtest: endpoint notices keep v4 tier details and legacy v3 text
ok 1646 - endpoint notices keep v4 tier details and legacy v3 text
  ---
  duration_ms: 0.142342
  ...
# Subtest: onload registers first/last commands routed to the shared jump
ok 1647 - onload registers first/last commands routed to the shared jump
  ---
  duration_ms: 1.617067
  ...
# Subtest: jumpToDueTask consumes a pending Vim prefix as N review steps
ok 1648 - jumpToDueTask consumes a pending Vim prefix as N review steps
  ---
  duration_ms: 0.907102
  ...
# Subtest: registered next-due-task callback reads the pending Vim prefix
ok 1649 - registered next-due-task callback reads the pending Vim prefix
  ---
  duration_ms: 0.877876
  ...
# Subtest: explicit jumpToDueTask repeat skips the Vim prefix
ok 1650 - explicit jumpToDueTask repeat skips the Vim prefix
  ---
  duration_ms: 0.337695
  ...
# Subtest: non-normal editor with a pending prefix still jumps one entry
ok 1651 - non-normal editor with a pending prefix still jumps one entry
  ---
  duration_ms: 0.288701
  ...
# Subtest: stale counted replan reuses the captured repeat
ok 1652 - stale counted replan reuses the captured repeat
  ---
  duration_ms: 2.154634
  ...
# Subtest: endpoint jump with a pending prefix still lands on the endpoint
ok 1653 - endpoint jump with a pending prefix still lands on the endpoint
  ---
  duration_ms: 0.343636
  ...
# Subtest: counted forward landing on ROTTEN keeps the boundary preamble
ok 1654 - counted forward landing on ROTTEN keeps the boundary preamble
  ---
  duration_ms: 0.483633
  ...
# Subtest: PRE and POST are machine tiers; PRE is a commitment
ok 1655 - PRE and POST are machine tiers; PRE is a commitment
  ---
  duration_ms: 0.224068
  ...
# Subtest: fallback notices name PRE checklist and POST closeout
ok 1656 - fallback notices name PRE checklist and POST closeout
  ---
  duration_ms: 0.231422
  ...
# Subtest: text-first cursor matching does not skip Pills after an above-insert
ok 1657 - text-first cursor matching does not skip Pills after an above-insert
  ---
  duration_ms: 0.132072
  ...
# Subtest: day-scoped anchors from another day are ignored
ok 1658 - day-scoped anchors from another day are ignored
  ---
  duration_ms: 0.19928
  ...
# Subtest: boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
ok 1659 - boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
  ---
  duration_ms: 0.191175
  ...
# Subtest: ]S reaches POST with 77 ROTTEN rows and a null budget
ok 1660 - ]S reaches POST with 77 ROTTEN rows and a null budget
  ---
  duration_ms: 0.553196
  ...
# Subtest: nav normalizes a legacy v7 returned tier to tickler
ok 1661 - nav normalizes a legacy v7 returned tier to tickler
  ---
  duration_ms: 0.12552
  ...
# Subtest: RECURRING is a machine tier, a commitment, and a v9 capability
ok 1662 - RECURRING is a machine tier, a commitment, and a v9 capability
  ---
  duration_ms: 0.155477
  ...
# Subtest: RECURRING counts in reviewWalkRemaining and gates the boundary
ok 1663 - RECURRING counts in reviewWalkRemaining and gates the boundary
  ---
  duration_ms: 0.154565
  ...
# Subtest: matchReviewRecurringCursor is text-first like the checklist matcher
ok 1664 - matchReviewRecurringCursor is text-first like the checklist matcher
  ---
  duration_ms: 0.174673
  ...
# Subtest: fallback notices name RECURRING due detail with the reschedule hint
ok 1665 - fallback notices name RECURRING due detail with the reschedule hint
  ---
  duration_ms: 0.15175
  ...
# Subtest: Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
ok 1666 - Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
  ---
  duration_ms: 0.143724
  ...
# Subtest: bobLineDigest matches the shared bob-cli vectors
ok 1667 - bobLineDigest matches the shared bob-cli vectors
  ---
  duration_ms: 4.247599
  ...
# Subtest: parseGoToTaskParams accepts a complete v1 link and ignores extra keys
ok 1668 - parseGoToTaskParams accepts a complete v1 link and ignores extra keys
  ---
  duration_ms: 0.719884
  ...
# Subtest: parseGoToTaskParams treats ref and block as optional
ok 1669 - parseGoToTaskParams treats ref and block as optional
  ---
  duration_ms: 0.13114
  ...
# Subtest: parseGoToTaskParams rejects each malformed field
ok 1670 - parseGoToTaskParams rejects each malformed field
  ---
  duration_ms: 0.232654
  ...
# Subtest: vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
ok 1671 - vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
  ---
  duration_ms: 0.257512
  ...
# Subtest: refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
ok 1672 - refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
  ---
  duration_ms: 1.25714
  ...
# Subtest: handleGoToTaskUri notices each malformed parameter
ok 1673 - handleGoToTaskUri notices each malformed parameter
  ---
  duration_ms: 1.112143
  ...
# Subtest: handleGoToTaskUri notices a path outside the vault
ok 1674 - handleGoToTaskUri notices a path outside the vault
  ---
  duration_ms: 0.392379
  ...
# Subtest: handleGoToTaskUri notices a missing file inside the vault
ok 1675 - handleGoToTaskUri notices a missing file inside the vault
  ---
  duration_ms: 0.464066
  ...
# Subtest: handleGoToTaskUri maps a trailing-slash vault base
ok 1676 - handleGoToTaskUri maps a trailing-slash vault base
  ---
  duration_ms: 1.645141
  ...
# Subtest: handleGoToTaskUri prefers the open buffer over cachedRead
ok 1677 - handleGoToTaskUri prefers the open buffer over cachedRead
  ---
  duration_ms: 0.717199
  ...
# Subtest: handleGoToTaskUri re-finds by block id after an insert above the task
ok 1678 - handleGoToTaskUri re-finds by block id after an insert above the task
  ---
  duration_ms: 0.442635
  ...
# Subtest: handleGoToTaskUri re-finds a unique digest after a shift with no block
ok 1679 - handleGoToTaskUri re-finds a unique digest after a shift with no block
  ---
  duration_ms: 0.459617
  ...
# Subtest: handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
ok 1680 - handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
  ---
  duration_ms: 0.376979
  ...
# Subtest: handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
ok 1681 - handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
  ---
  duration_ms: 0.419351
  ...
# Subtest: handleGoToTaskUri reuses a leaf that already shows the note
ok 1682 - handleGoToTaskUri reuses a leaf that already shows the note
  ---
  duration_ms: 0.583694
  ...
# Subtest: handleGoToTaskUri switches a Reading-view leaf to editing
ok 1683 - handleGoToTaskUri switches a Reading-view leaf to editing
  ---
  duration_ms: 0.552484
  ...
# Subtest: handleGoToTaskUri records a jump from the prior cursor and none without one
ok 1684 - handleGoToTaskUri records a jump from the prior cursor and none without one
  ---
  duration_ms: 0.768868
  ...
# Subtest: handleGoToTaskUri never writes the vault or advances the walk
ok 1685 - handleGoToTaskUri never writes the vault or advances the walk
  ---
  duration_ms: 0.393872
  ...
# Subtest: handleGoToTaskUri reports when the note cannot be opened
ok 1686 - handleGoToTaskUri reports when the note cannot be opened
  ---
  duration_ms: 0.282619
  ...
# Subtest: focusTaskMoveDestination still lands without switching Reading view
ok 1687 - focusTaskMoveDestination still lands without switching Reading view
  ---
  duration_ms: 0.347964
  ...
# Subtest: onload registers both read-only navigation protocols when available
ok 1688 - onload registers both read-only navigation protocols when available
  ---
  duration_ms: 1.02663
  ...
# Subtest: onload skips protocol registration when the API is missing
ok 1689 - onload skips protocol registration when the API is missing
  ---
  duration_ms: 0.31466
  ...
# Subtest: registered protocol handler forwards params to handleGoToTaskUri
ok 1690 - registered protocol handler forwards params to handleGoToTaskUri
  ---
  duration_ms: 0.306355
  ...
# Subtest: handleGoToTaskUri maps a path through realpath when prefixes differ
ok 1691 - handleGoToTaskUri maps a path through realpath when prefixes differ
  ---
  duration_ms: 2.408228
  ...
# Subtest: cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
ok 1692 - cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
  ---
  duration_ms: 1.987795
  ...
# Subtest: findCancelLogParent finds a direct child but ignores a grandchild
ok 1693 - findCancelLogParent finds a direct child but ignores a grandchild
  ---
  duration_ms: 0.600176
  ...
# Subtest: getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
ok 1694 - getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
  ---
  duration_ms: 0.19415
  ...
# Subtest: formatCancelLogEntryText renders the exact preview text
ok 1695 - formatCancelLogEntryText renders the exact preview text
  ---
  duration_ms: 0.150637
  ...
# Subtest: planCancelLogEntry inserts a first-child log with tabs or spaces
ok 1696 - planCancelLogEntry inserts a first-child log with tabs or spaces
  ---
  duration_ms: 0.862897
  ...
# Subtest: planCancelLogEntry prepends under an existing log wherever it sits
ok 1697 - planCancelLogEntry prepends under an existing log wherever it sits
  ---
  duration_ms: 0.379474
  ...
# Subtest: planCancelLogEntry uses the fallback only when a marker exists
ok 1698 - planCancelLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.460429
  ...
# Subtest: isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
ok 1699 - isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
  ---
  duration_ms: 0.386066
  ...
# Subtest: describeCancelTaskRow covers single, counted, link, recurring, and hidden
ok 1700 - describeCancelTaskRow covers single, counted, link, recurring, and hidden
  ---
  duration_ms: 2.455046
  ...
# Subtest: planTaskCancelBatch cancels a single task with a first-child log
ok 1701 - planTaskCancelBatch cancels a single task with a first-child log
  ---
  duration_ms: 1.806408
  ...
# Subtest: planTaskCancelBatch upserts cancelled before the block id and preserves fields
ok 1702 - planTaskCancelBatch upserts cancelled before the block id and preserves fields
  ---
  duration_ms: 0.559768
  ...
# Subtest: planTaskCancelBatch records id-field task identities
ok 1703 - planTaskCancelBatch records id-field task identities
  ---
  duration_ms: 0.308659
  ...
# Subtest: planTaskCancelBatch skips closed targets and stays bottom-up
ok 1704 - planTaskCancelBatch skips closed targets and stays bottom-up
  ---
  duration_ms: 0.579476
  ...
# Subtest: planTaskCancelBatch refuses recurring targets in all three syntaxes
ok 1705 - planTaskCancelBatch refuses recurring targets in all three syntaxes
  ---
  duration_ms: 0.90648
  ...
# Subtest: planTaskCancelBatch handles empty reasons and stale preimages
ok 1706 - planTaskCancelBatch handles empty reasons and stale preimages
  ---
  duration_ms: 0.525553
  ...
# Subtest: planTaskCancelBatch preserves CRLF line endings
ok 1707 - planTaskCancelBatch preserves CRLF line endings
  ---
  duration_ms: 0.34578
  ...
# Subtest: cancel project conversion carries the log and reports it
ok 1708 - cancel project conversion carries the log and reports it
  ---
  duration_ms: 4.877692
  ...
# Subtest: getCancelTaskRowTitle names single, counted, and link sessions
ok 1709 - getCancelTaskRowTitle names single, counted, and link sessions
  ---
  duration_ms: 0.977245
  ...
# Subtest: getCancelReasonHints labels Enter per state and Esc as Keep open
ok 1710 - getCancelReasonHints labels Enter per state and Esc as Keep open
  ---
  duration_ms: 0.79137
  ...
# Subtest: the Cancel property item and the card's cancel row describe an open task
ok 1711 - the Cancel property item and the card's cancel row describe an open task
  ---
  duration_ms: 11.832197
  ...
# Subtest: Cancel row hides on closed tasks, plain bullets, and all-closed sessions
ok 1712 - Cancel row hides on closed tasks, plain bullets, and all-closed sessions
  ---
  duration_ms: 6.863673
  ...
# Subtest: Cancel row reports skipped closed targets in a counted session
ok 1713 - Cancel row reports skipped closed targets in a counted session
  ---
  duration_ms: 1.651843
  ...
# Subtest: the card refuses the cancel row on a recurring task and stays on the card
ok 1714 - the card refuses the cancel row on a recurring task and stays on the card
  ---
  duration_ms: 2.223313
  ...
# Subtest: cancel reason stage previews the typed, empty, fallback, and :: cases
ok 1715 - cancel reason stage previews the typed, empty, fallback, and :: cases
  ---
  duration_ms: 3.310789
  ...
# Subtest: cancel reason footer flips between plain, log, and fallback labels
ok 1716 - cancel reason footer flips between plain, log, and fallback labels
  ---
  duration_ms: 0.996983
  ...
# Subtest: Esc from the cancel reason stage writes nothing
ok 1717 - Esc from the cancel reason stage writes nothing
  ---
  duration_ms: 4.244082
  ...
# Subtest: single cancel writes [-], stamp, and first-child log in one transaction
ok 1718 - single cancel writes [-], stamp, and first-child log in one transaction
  ---
  duration_ms: 4.423354
  ...
# Subtest: empty reason writes no log unless one already exists
ok 1719 - empty reason writes no log unless one already exists
  ---
  duration_ms: 3.833478
  ...
# Subtest: stale single preimage refuses with nothing written
ok 1720 - stale single preimage refuses with nothing written
  ---
  duration_ms: 2.857705
  ...
# Subtest: cancel writes [-] with no NOW chip
ok 1721 - cancel writes [-] with no NOW chip
  ---
  duration_ms: 1.364474
  ...
# Subtest: TSC recovery runs with cancelled identities; a missing API still succeeds
ok 1722 - TSC recovery runs with cancelled identities; a missing API still succeeds
  ---
  duration_ms: 2.51471
  ...
# Subtest: a throwing TSC API is skipped silently with no chip
ok 1723 - a throwing TSC API is skipped silently with no chip
  ---
  duration_ms: 5.193926
  ...
# Subtest: counted cancel skips closed targets and reports them
ok 1724 - counted cancel skips closed targets and reports them
  ---
  duration_ms: 2.738447
  ...
# Subtest: same-file cancel folds today's Pomodoro prune into one transaction
ok 1725 - same-file cancel folds today's Pomodoro prune into one transaction
  ---
  duration_ms: 4.595461
  ...
# Subtest: link session cancels the target and removes the invoking link bullet
ok 1726 - link session cancels the target and removes the invoking link bullet
  ---
  duration_ms: 5.776037
  ...
# Subtest: buildCancelNoticeModel text covers every chip
ok 1727 - buildCancelNoticeModel text covers every chip
  ---
  duration_ms: 0.296125
  ...
# Subtest: renderCancelNoticeFragment builds the is-cancel card
ok 1728 - renderCancelNoticeFragment builds the is-cancel card
  ---
  duration_ms: 0.636696
  ...
# Subtest: Ctrl+0 loads and focuses a deferred pinned dash tab without jumping or restoring
ok 1729 - Ctrl+0 loads and focuses a deferred pinned dash tab without jumping or restoring
  ---
  duration_ms: 2.931105
  ...
# Subtest: Ctrl+0 from an unpinned dash copy switches to the pinned home tab
ok 1730 - Ctrl+0 from an unpinned dash copy switches to the pinned home tab
  ---
  duration_ms: 0.508852
  ...
# Subtest: Ctrl+0 stays on the pinned dash tab when an unpinned copy exists
ok 1731 - Ctrl+0 stays on the pinned dash tab when an unpinned copy exists
  ---
  duration_ms: 0.260728
  ...
# Subtest: Ctrl+0 keeps the active dash tab when equal-ranked copies exist
ok 1732 - Ctrl+0 keeps the active dash tab when equal-ranked copies exist
  ---
  duration_ms: 0.299432
  ...
# Subtest: a pinned dash tab wins over an earlier unpinned tab
ok 1733 - a pinned dash tab wins over an earlier unpinned tab
  ---
  duration_ms: 0.333908
  ...
# Subtest: a main-area dash tab wins over a pinned sidebar tab
ok 1734 - a main-area dash tab wins over a pinned sidebar tab
  ---
  duration_ms: 0.220321
  ...
# Subtest: a deferred sidebar dash tab is reused when there is no main-area match
ok 1735 - a deferred sidebar dash tab is reused when there is no main-area match
  ---
  duration_ms: 1.069031
  ...
# Subtest: a markdown saved state is considered even when the leaf is not deferred
ok 1736 - a markdown saved state is considered even when the leaf is not deferred
  ---
  duration_ms: 0.232383
  ...
# Subtest: Ctrl+0 opens dash in the current tab when no matching tab exists
ok 1737 - Ctrl+0 opens dash in the current tab when no matching tab exists
  ---
  duration_ms: 0.541093
  ...
# Subtest: Ctrl+0 leaves an already active dash tab alone
ok 1738 - Ctrl+0 leaves an already active dash tab alone
  ---
  duration_ms: 0.548937
  ...
# Subtest: isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
ok 1739 - isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
  ---
  duration_ms: 1.111642
  ...
# Subtest: findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
ok 1740 - findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
  ---
  duration_ms: 1.425641
  ...
# Subtest: collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
ok 1741 - collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
  ---
  duration_ms: 0.512538
  ...
# Subtest: planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
ok 1742 - planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
  ---
  duration_ms: 0.945094
  ...
# Subtest: planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
ok 1743 - planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
  ---
  duration_ms: 0.807251
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
ok 1744 - planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
  ---
  duration_ms: 1.000149
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
ok 1745 - planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
  ---
  duration_ms: 0.569487
  ...
# Subtest: planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
ok 1746 - planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
  ---
  duration_ms: 0.208999
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
ok 1747 - planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
  ---
  duration_ms: 0.694185
  ...
# Subtest: planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
ok 1748 - planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
  ---
  duration_ms: 0.624692
  ...
# Subtest: planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
ok 1749 - planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
  ---
  duration_ms: 0.527287
  ...
# Subtest: planDeferredPomodoroLinkCleanup preserves CRLF line endings
ok 1750 - planDeferredPomodoroLinkCleanup preserves CRLF line endings
  ---
  duration_ms: 0.259506
  ...
# Subtest: deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
ok 1751 - deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
  ---
  duration_ms: 0.273843
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks\#^x]] \#
ok 1752 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks\#^x]] \#
  ---
  duration_ms: 0.269204
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks\#^x|alias]] \#
ok 1753 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks\#^x|alias]] \#
  ---
  duration_ms: 0.15698
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks\#^x]]
ok 1754 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks\#^x]]
  ---
  duration_ms: 0.191927
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks\#^x]]
ok 1755 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks\#^x]]
  ---
  duration_ms: 0.147842
  ...
# Subtest: dedicated decoration check accepts paired strikes but cleanup never removes struck links
ok 1756 - dedicated decoration check accepts paired strikes but cleanup never removes struck links
  ---
  duration_ms: 0.299492
  ...
# Subtest: cleanup deletes only touched childless entries, preserving prose, placeholders and closed history
ok 1757 - cleanup deletes only touched childless entries, preserving prose, placeholders and closed history
  ---
  duration_ms: 0.290404
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\n", final newline false)
ok 1758 - cleanup handles adjacent EOF entries ("\\n", final newline false)
  ---
  duration_ms: 0.206103
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\n", final newline true)
ok 1759 - cleanup handles adjacent EOF entries ("\\n", final newline true)
  ---
  duration_ms: 0.166508
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\r\\n", final newline false)
ok 1760 - cleanup handles adjacent EOF entries ("\\r\\n", final newline false)
  ---
  duration_ms: 0.146319
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\r\\n", final newline true)
ok 1761 - cleanup handles adjacent EOF entries ("\\r\\n", final newline true)
  ---
  duration_ms: 0.155968
  ...
# Subtest: counted dependencies converge mixed sources and maintain one link per parent
ok 1762 - counted dependencies converge mixed sources and maintain one link per parent
  ---
  duration_ms: 13.440637
  ...
# Subtest: counted and single dependency gestures refuse inside a blockquote (DP29)
ok 1763 - counted and single dependency gestures refuse inside a blockquote (DP29)
  ---
  duration_ms: 0.420844
  ...
# Subtest: counted dependency candidates exclude every source and expose mixed state
ok 1764 - counted dependency candidates exclude every source and expose mixed state
  ---
  duration_ms: 0.884118
  ...
# Subtest: counted dependency block-ID prompting is planned atomically
ok 1765 - counted dependency block-ID prompting is planned atomically
  ---
  duration_ms: 1.874829
  ...
# Subtest: counted dependency runtime applies target, parents, and navigation in one undo group
ok 1766 - counted dependency runtime applies target, parents, and navigation in one undo group
  ---
  duration_ms: 6.508064
  ...
# Subtest: counted Depends-on removal recovers residents with [unblocked::]
ok 1767 - counted Depends-on removal recovers residents with [unblocked::]
  ---
  duration_ms: 4.016807
  ...
# Subtest: counted Depends-on removal writes [unblocked::] through the wired freshness API
ok 1768 - counted Depends-on removal writes [unblocked::] through the wired freshness API
  ---
  duration_ms: 5.249461
  ...
# Subtest: cross-file toggle changes only the source link
ok 1769 - cross-file toggle changes only the source link
  ---
  duration_ms: 1.735844
  ...
# Subtest: cross-file write failure still toggles only the source link
ok 1770 - cross-file write failure still toggles only the source link
  ---
  duration_ms: 0.619273
  ...
# Subtest: line-local fallback applies bottom-up and preserves CRLF
ok 1771 - line-local fallback applies bottom-up and preserves CRLF
  ---
  duration_ms: 0.774539
  ...
# Subtest: source line-count invariant rejects embedded newline changes
ok 1772 - source line-count invariant rejects embedded newline changes
  ---
  duration_ms: 0.204831
  ...
# Subtest: pure toggle refuses when the source changed under it
ok 1773 - pure toggle refuses when the source changed under it
  ---
  duration_ms: 0.156198
  ...
# Subtest: counted transclusion toggle evaluates each line independently
ok 1774 - counted transclusion toggle evaluates each line independently
  ---
  duration_ms: 0.349558
  ...
# Subtest: transclusion toggle is refused on Depends-On lines
ok 1775 - transclusion toggle is refused on Depends-On lines
  ---
  duration_ms: 0.265217
  ...
# Subtest: legacy sole-link children toggle purely, without field or status writes
ok 1776 - legacy sole-link children toggle purely, without field or status writes
  ---
  duration_ms: 0.394593
  ...
# Subtest: Ctrl+D on the Depends on row clears the line, field, and legacy children
ok 1777 - Ctrl+D on the Depends on row clears the line, field, and legacy children
  ---
  duration_ms: 2.8599
  ...
# Subtest: Ctrl+D clears a field-only dependency without a line
ok 1778 - Ctrl+D clears a field-only dependency without a line
  ---
  duration_ms: 0.954533
  ...
# Subtest: counted Ctrl+D on the Depends on row clears every targeted task
ok 1779 - counted Ctrl+D on the Depends on row clears every targeted task
  ---
  duration_ms: 2.234847
  ...
# Subtest: findRemovedLineText reports deleted lines
ok 1780 - findRemovedLineText reports deleted lines
  ---
  duration_ms: 0.140869
  ...
# Subtest: hand-edit mirror projects an edited line into the field
ok 1781 - hand-edit mirror projects an edited line into the field
  ---
  duration_ms: 1.527866
  ...
# Subtest: hand-edit mirror canonicalises a hand-written line variant
ok 1782 - hand-edit mirror canonicalises a hand-written line variant
  ---
  duration_ms: 0.797172
  ...
# Subtest: hand-edit mirror drops a linkless line and the field
ok 1783 - hand-edit mirror drops a linkless line and the field
  ---
  duration_ms: 1.248724
  ...
# Subtest: hand-edit mirror clears the field after the line is deleted
ok 1784 - hand-edit mirror clears the field after the line is deleted
  ---
  duration_ms: 0.90137
  ...
# Subtest: hand-edit mirror leaves malformed lines alone
ok 1785 - hand-edit mirror leaves malformed lines alone
  ---
  duration_ms: 0.252181
  ...
# Subtest: hand-edit mirror leaves legacy-only children for the hooks
ok 1786 - hand-edit mirror leaves legacy-only children for the hooks
  ---
  duration_ms: 0.3143
  ...
# Subtest: hand-edit mirror blocks when an open prerequisite is added by hand
ok 1787 - hand-edit mirror blocks when an open prerequisite is added by hand
  ---
  duration_ms: 0.68599
  ...
# Subtest: hand-edit mirror never transfers commitment to the target
ok 1788 - hand-edit mirror never transfers commitment to the target
  ---
  duration_ms: 0.87482
  ...
# Subtest: hand-edit mirror recovers when the last open prerequisite is removed by hand
ok 1789 - hand-edit mirror recovers when the last open prerequisite is removed by hand
  ---
  duration_ms: 1.079861
  ...
# Subtest: hand-edit mirror leaves a half-typed link alone
ok 1790 - hand-edit mirror leaves a half-typed link alone
  ---
  duration_ms: 0.334198
  ...
# Subtest: hand-edit mirror clears the owning task when its last-child line is deleted
ok 1791 - hand-edit mirror clears the owning task when its last-child line is deleted
  ---
  duration_ms: 0.882445
  ...
# Subtest: mirror scheduler debounces at the contract interval
ok 1792 - mirror scheduler debounces at the contract interval
  ---
  duration_ms: 0.967677
  ...
# Subtest: mirror scheduler seeds the baseline from the update start state
ok 1793 - mirror scheduler seeds the baseline from the update start state
  ---
  duration_ms: 1.689045
  ...
# Subtest: mirror scheduler keeps the first baseline and maps the owner across a burst
ok 1794 - mirror scheduler keeps the first baseline and maps the owner across a burst
  ---
  duration_ms: 0.491809
  ...
# Subtest: mirror listener runs clear-field for a first-edit deletion with a following sibling
ok 1795 - mirror listener runs clear-field for a first-edit deletion with a following sibling
  ---
  duration_ms: 11.117603
  ...
# Subtest: mirror fire re-arms while the cursor stays on the edited line
ok 1796 - mirror fire re-arms while the cursor stays on the edited line
  ---
  duration_ms: 2.454376
  ...
# Subtest: mirror scheduler reads changed ranges from the CM6 update
ok 1797 - mirror scheduler reads changed ranges from the CM6 update
  ---
  duration_ms: 0.253824
  ...
# Subtest: mirror scheduler skips IME composition
ok 1798 - mirror scheduler skips IME composition
  ---
  duration_ms: 0.198408
  ...
# Subtest: mirror scheduler skips open modals
ok 1799 - mirror scheduler skips open modals
  ---
  duration_ms: 0.170465
  ...
# Subtest: counted Ctrl+D clears every targeted task in one transaction with one notice
ok 1800 - counted Ctrl+D clears every targeted task in one transaction with one notice
  ---
  duration_ms: 4.883511
  ...
# Subtest: counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
ok 1801 - counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
  ---
  duration_ms: 1.553314
  ...
# Subtest: counted N! on only a Depends-On line refuses without writing
ok 1802 - counted N! on only a Depends-On line refuses without writing
  ---
  duration_ms: 0.289863
  ...
# Subtest: promotion targets enumerate real tasks and assign stable IDs
ok 1803 - promotion targets enumerate real tasks and assign stable IDs
  ---
  duration_ms: 4.725111
  ...
# Subtest: promotion file planner expands live links and preserves history
ok 1804 - promotion file planner expands live links and preserves history
  ---
  duration_ms: 4.23295
  ...
# Subtest: promotion file planner handles forms, whitespace, and subtrees
ok 1805 - promotion file planner handles forms, whitespace, and subtrees
  ---
  duration_ms: 1.386517
  ...
# Subtest: promotion file planner keeps compatibility for non-live references
ok 1806 - promotion file planner keeps compatibility for non-live references
  ---
  duration_ms: 0.718833
  ...
# Subtest: forward promotion expands live links, persists anchors, and removes the source
ok 1807 - forward promotion expands live links, persists anchors, and removes the source
  ---
  duration_ms: 7.01926
  ...
# Subtest: forward promotion uses zero-task fallback and keeps reverse one-to-one
ok 1808 - forward promotion uses zero-task fallback and keeps reverse one-to-one
  ---
  duration_ms: 1.174081
  ...
# Subtest: forward promotion retains the source on ambiguous, stale, and write failures
ok 1809 - forward promotion retains the source on ambiguous, stale, and write failures
  ---
  duration_ms: 1.581278
  ...
# Subtest: forward promotion discovers live links without a backlink cache and uses one open-editor write
ok 1810 - forward promotion discovers live links without a backlink cache and uses one open-editor write
  ---
  duration_ms: 1.888265
  ...
# Subtest: forward conversion carries a Depends-On line and reverse restores it
not ok 1811 - forward conversion carries a Depends-On line and reverse restores it
  ---
  duration_ms: 17.416519
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-navigation-hotkeys-forward-promotion.cjs:662:1'
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
      '- [?] #task Ship it [created::2026-10-23] [id:: Areas__Work__ship] [dependsOn:: Areas__Work__prereq] ^ship\n' +
      '\t- ⛓️ **DEPENDS ON:** [[#^prereq]]\n' +
      '\t- [?] #task Follow up [created::2026-10-23] ^follow-up'
    
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
    - [?] #task Ship it [created::2026-10-23] [id:: Areas__Work__ship] [dependsOn:: Areas__Work__prereq] ^ship
    	- ⛓️ **DEPENDS ON:** [[#^prereq]]
    	- [?] #task Follow up [created::2026-10-23] ^follow-up
  operator: 'doesNotMatch'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-navigation-hotkeys-forward-promotion.cjs:734:10)
    async Test.run (node:internal/test_runner/test:980:9)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: planTaskLaneBatch commits every Ready target to Next
ok 1812 - planTaskLaneBatch commits every Ready target to Next
  ---
  duration_ms: 2.65125
  ...
# Subtest: planTaskLaneBatch releases Next and In Progress to Ready
ok 1813 - planTaskLaneBatch releases Next and In Progress to Ready
  ---
  duration_ms: 0.913984
  ...
# Subtest: planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
ok 1814 - planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
  ---
  duration_ms: 0.828431
  ...
# Subtest: planTaskLaneBatch skips Blocked and refuses stale preimages
ok 1815 - planTaskLaneBatch skips Blocked and refuses stale preimages
  ---
  duration_ms: 0.30372
  ...
# Subtest: buildLaneToggleNotice reports commit and release with and without budgets
ok 1816 - buildLaneToggleNotice reports commit and release with and without budgets
  ---
  duration_ms: 0.374465
  ...
# Subtest: describeLaneRow covers task, counted, and link sessions
ok 1817 - describeLaneRow covers task, counted, and link sessions
  ---
  duration_ms: 0.410333
  ...
# Subtest: toggleTaskLane commits Ready to Next and reports lane budgets
ok 1818 - toggleTaskLane commits Ready to Next and reports lane budgets
  ---
  duration_ms: 2.397527
  ...
# Subtest: toggleTaskLane releases to Ready without the api
ok 1819 - toggleTaskLane releases to Ready without the api
  ---
  duration_ms: 0.985511
  ...
# Subtest: toggleTaskLane release logs the summary on In Progress tasks
ok 1820 - toggleTaskLane release logs the summary on In Progress tasks
  ---
  duration_ms: 1.088808
  ...
# Subtest: toggleTaskLane skips Blocked targets
ok 1821 - toggleTaskLane skips Blocked targets
  ---
  duration_ms: 0.822109
  ...
# Subtest: counted toggleTaskLane covers the current task plus the next N tasks
ok 1822 - counted toggleTaskLane covers the current task plus the next N tasks
  ---
  duration_ms: 0.533559
  ...
# Subtest: toggleTaskLane on a Task Link writes through the open buffer
ok 1823 - toggleTaskLane on a Task Link writes through the open buffer
  ---
  duration_ms: 3.373951
  ...
# Subtest: toggleTaskLane on Task Links releases across notes
ok 1824 - toggleTaskLane on Task Links releases across notes
  ---
  duration_ms: 1.119076
  ...
# Subtest: toggleTaskLane refuses when a preimage changed
ok 1825 - toggleTaskLane refuses when a preimage changed
  ---
  duration_ms: 0.236251
  ...
# Subtest: Ctrl+Shift+P shows a pinned lane row that commits immediately
ok 1826 - Ctrl+Shift+P shows a pinned lane row that commits immediately
  ---
  duration_ms: 11.104977
  ...
# Subtest: Ctrl+Shift+P link mode shows the lane row with release detail
ok 1827 - Ctrl+Shift+P link mode shows the lane row with release detail
  ---
  duration_ms: 3.845071
  ...
# Subtest: Ctrl+Shift+P lane release with In Progress goes through the reason stage
ok 1828 - Ctrl+Shift+P lane release with In Progress goes through the reason stage
  ---
  duration_ms: 3.255635
  ...
# Subtest: getLinkPickerSessionSubtitle keeps the clamp for a single link
ok 1829 - getLinkPickerSessionSubtitle keeps the clamp for a single link
  ---
  duration_ms: 0.13135
  ...
# Subtest: link-mode priority notice keeps via Task Links visible
ok 1830 - link-mode priority notice keeps via Task Links visible
  ---
  duration_ms: 0.778757
  ...
# Subtest: already-handled Alt+N leaves Vim state alone
ok 1831 - already-handled Alt+N leaves Vim state alone
  ---
  duration_ms: 0.310302
  ...
# Subtest: Alt+N fallback still dispatches once with the Vim count
ok 1832 - Alt+N fallback still dispatches once with the Vim count
  ---
  duration_ms: 0.712129
  ...
# Subtest: lane release deletes an emptied entry (cross-file, Alt+N)
ok 1833 - lane release deletes an emptied entry (cross-file, Alt+N)
  ---
  duration_ms: 2.319698
  ...
# Subtest: lane release deletes an emptied entry (cross-file, card)
ok 1834 - lane release deletes an emptied entry (cross-file, card)
  ---
  duration_ms: 2.258231
  ...
# Subtest: lane release deletes an emptied entry (same-file, Alt+N)
ok 1835 - lane release deletes an emptied entry (same-file, Alt+N)
  ---
  duration_ms: 0.714073
  ...
# Subtest: lane release deletes an emptied entry (same-file, card)
ok 1836 - lane release deletes an emptied entry (same-file, card)
  ---
  duration_ms: 2.049633
  ...
# Subtest: Task Link release deletes its entry in one undo group (separate, Alt+N)
ok 1837 - Task Link release deletes its entry in one undo group (separate, Alt+N)
  ---
  duration_ms: 1.144104
  ...
# Subtest: Task Link release deletes its entry in one undo group (separate, card)
ok 1838 - Task Link release deletes its entry in one undo group (separate, card)
  ---
  duration_ms: 2.284812
  ...
# Subtest: Task Link release deletes its entry in one undo group (folded, Alt+N)
ok 1839 - Task Link release deletes its entry in one undo group (folded, Alt+N)
  ---
  duration_ms: 0.833862
  ...
# Subtest: Task Link release deletes its entry in one undo group (folded, card)
ok 1840 - Task Link release deletes its entry in one undo group (folded, card)
  ---
  duration_ms: 2.18467
  ...
# Subtest: parseLinkPickerTaskLink recognizes dedicated Task Link bullets
ok 1841 - parseLinkPickerTaskLink recognizes dedicated Task Link bullets
  ---
  duration_ms: 1.84976
  ...
# Subtest: discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
ok 1842 - discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
  ---
  duration_ms: 0.971243
  ...
# Subtest: discoverLinkPickerTargets leaves \#task lines to the regular picker
ok 1843 - discoverLinkPickerTargets leaves \#task lines to the regular picker
  ---
  duration_ms: 0.279093
  ...
# Subtest: findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
ok 1844 - findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
  ---
  duration_ms: 0.437626
  ...
# Subtest: createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
ok 1845 - createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
  ---
  duration_ms: 2.065604
  ...
# Subtest: getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
ok 1846 - getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
  ---
  duration_ms: 0.713292
  ...
# Subtest: bare link mode edits the task behind a Task Link through the open buffer
ok 1847 - bare link mode edits the task behind a Task Link through the open buffer
  ---
  duration_ms: 14.471536
  ...
# Subtest: counted link mode writes across notes through both the open buffer and the vault
ok 1848 - counted link mode writes across notes through both the open buffer and the vault
  ---
  duration_ms: 3.687899
  ...
# Subtest: Task Link scheduled delete recovers a Blocked task through the wired freshness API
ok 1849 - Task Link scheduled delete recovers a Blocked task through the wired freshness API
  ---
  duration_ms: 5.78301
  ...
# Subtest: link mode refuses the whole operation when a linked note changed
ok 1850 - link mode refuses the whole operation when a linked note changed
  ---
  duration_ms: 2.927379
  ...
# Subtest: link mode reports a closed target and changes nothing
ok 1851 - link mode reports a closed target and changes nothing
  ---
  duration_ms: 1.115119
  ...
# Subtest: link mode defers to a future date, blocks the task, and prunes today
ok 1852 - link mode defers to a future date, blocks the task, and prunes today
  ---
  duration_ms: 7.888128
  ...
# Subtest: bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
ok 1853 - bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
  ---
  duration_ms: 2.821106
  ...
# Subtest: Task Link scheduled write deletes its entry (separate)
ok 1854 - Task Link scheduled write deletes its entry (separate)
  ---
  duration_ms: 5.294877
  ...
# Subtest: Task Link scheduled write deletes its entry (folded)
ok 1855 - Task Link scheduled write deletes its entry (folded)
  ---
  duration_ms: 3.3265
  ...
# Subtest: folded Task Link scheduling maps the cursor past logs inserted before the emptied entry
ok 1856 - folded Task Link scheduling maps the cursor past logs inserted before the emptied entry
  ---
  duration_ms: 3.14305
  ...
# Subtest: dash restore suppresses editor notice after deliberate navigation
ok 1857 - dash restore suppresses editor notice after deliberate navigation
  ---
  duration_ms: 21.550167
  ...
# Subtest: open-task dispatch timeout is registered for plugin cleanup
ok 1858 - open-task dispatch timeout is registered for plugin cleanup
  ---
  duration_ms: 0.525584
  ...
# Subtest: jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
ok 1859 - jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
  ---
  duration_ms: 5.214495
  ...
# Subtest: jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
ok 1860 - jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
  ---
  duration_ms: 1.421674
  ...
# Subtest: jumpToOpenObsidianTask keeps current-swap transaction failures local
ok 1861 - jumpToOpenObsidianTask keeps current-swap transaction failures local
  ---
  duration_ms: 0.748669
  ...
# Subtest: jumpToOpenObsidianTask refuses current-up without jumping or mutating
ok 1862 - jumpToOpenObsidianTask refuses current-up without jumping or mutating
  ---
  duration_ms: 0.459207
  ...
# Subtest: jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
ok 1863 - jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
  ---
  duration_ms: 2.270114
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
ok 1864 - Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
  ---
  duration_ms: 0.758658
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
ok 1865 - Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
  ---
  duration_ms: 0.791862
  ...
# Subtest: counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
ok 1866 - counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
  ---
  duration_ms: 1.274843
  ...
# Subtest: an impossible counted Pomodoro move refuses without jumping or mutating
ok 1867 - an impossible counted Pomodoro move refuses without jumping or mutating
  ---
  duration_ms: 0.50819
  ...
# Subtest: counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
ok 1868 - counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
  ---
  duration_ms: 0.725715
  ...
# Subtest: counted open-task jump on a sole current target keeps the existing notice
ok 1869 - counted open-task jump on a sole current target keeps the existing notice
  ---
  duration_ms: 0.211674
  ...
# Subtest: dispatch guard allows exactly one counted Pomodoro move when the command route also fires
ok 1870 - dispatch guard allows exactly one counted Pomodoro move when the command route also fires
  ---
  duration_ms: 0.826247
  ...
# Subtest: bullet property picker reconciles duplicate bare and counted opens
ok 1871 - bullet property picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 14.819068
  ...
# Subtest: bullet property picker close lifecycle clears tracking for fresh sessions
ok 1872 - bullet property picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 7.708927
  ...
# Subtest: task move picker reconciles duplicate bare and counted opens
ok 1873 - task move picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 2.538565
  ...
# Subtest: task move picker close lifecycle clears tracking for fresh sessions
ok 1874 - task move picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 2.337091
  ...
# Subtest: Pomodoro bullet move picker opens sessions and clears the shared move picker slot
ok 1875 - Pomodoro bullet move picker opens sessions and clears the shared move picker slot
  ---
  duration_ms: 2.847025
  ...
# Subtest: Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
ok 1876 - Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
  ---
  duration_ms: 0.782153
  ...
# Subtest: move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
ok 1877 - move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
  ---
  duration_ms: 1.274633
  ...
# Subtest: commitPomodoroBulletMoveSession applies one guarded same-file transaction
ok 1878 - commitPomodoroBulletMoveSession applies one guarded same-file transaction
  ---
  duration_ms: 2.46745
  ...
# Subtest: Pomodoro bullet move picker confirms = through the actual picker callback
ok 1879 - Pomodoro bullet move picker confirms = through the actual picker callback
  ---
  duration_ms: 1.05833
  ...
# Subtest: Pomodoro bullet move picker reserves =NAME for peeling a named merged component
ok 1880 - Pomodoro bullet move picker reserves =NAME for peeling a named merged component
  ---
  duration_ms: 1.031439
  ...
# Subtest: Pomodoro bullet move picker confirms =email through the actual picker callback
ok 1881 - Pomodoro bullet move picker confirms =email through the actual picker callback
  ---
  duration_ms: 1.374323
  ...
# Subtest: Pomodoro bullet move picker confirms = review through the actual picker callback
ok 1882 - Pomodoro bullet move picker confirms = review through the actual picker callback
  ---
  duration_ms: 0.689766
  ...
# Subtest: Pomodoro bullet move picker confirms =focus by unnaming a single-name source
ok 1883 - Pomodoro bullet move picker confirms =focus by unnaming a single-name source
  ---
  duration_ms: 0.653116
  ...
# Subtest: Pomodoro bullet split stale-content guard does not write
ok 1884 - Pomodoro bullet split stale-content guard does not write
  ---
  duration_ms: 0.325801
  ...
# Subtest: Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
ok 1885 - Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
  ---
  duration_ms: 0.625274
  ...
# Subtest: native isOpen regression: pickers attach, close clears slot, reopen works
ok 1886 - native isOpen regression: pickers attach, close clears slot, reopen works
  ---
  duration_ms: 2.895107
  ...
# Subtest: stale registered pickers fail open on the next key
ok 1887 - stale registered pickers fail open on the next key
  ---
  duration_ms: 6.069437
  ...
# Subtest: planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
ok 1888 - planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
  ---
  duration_ms: 4.198334
  ...
# Subtest: planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
ok 1889 - planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
  ---
  duration_ms: 0.551593
  ...
# Subtest: planPomodoroBulletMove preserves the source when only some siblings move out
ok 1890 - planPomodoroBulletMove preserves the source when only some siblings move out
  ---
  duration_ms: 0.304261
  ...
# Subtest: planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
ok 1891 - planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
  ---
  duration_ms: 0.344387
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
ok 1892 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
  ---
  duration_ms: 0.569187
  ...
# Subtest: planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
ok 1893 - planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
  ---
  duration_ms: 0.712771
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
ok 1894 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
  ---
  duration_ms: 0.394122
  ...
# Subtest: planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
ok 1895 - planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
  ---
  duration_ms: 0.289051
  ...
# Subtest: planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
ok 1896 - planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
  ---
  duration_ms: 0.483082
  ...
# Subtest: planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
ok 1897 - planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
  ---
  duration_ms: 0.815627
  ...
# Subtest: planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
ok 1898 - planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
  ---
  duration_ms: 0.290766
  ...
# Subtest: planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
ok 1899 - planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
  ---
  duration_ms: 0.228977
  ...
# Subtest: planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
ok 1900 - planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
  ---
  duration_ms: 0.371159
  ...
# Subtest: planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
ok 1901 - planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
  ---
  duration_ms: 0.373222
  ...
# Subtest: planPomodoroBulletMove deletes both open and closed source entries the same way
ok 1902 - planPomodoroBulletMove deletes both open and closed source entries the same way
  ---
  duration_ms: 0.515965
  ...
# Subtest: planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
ok 1903 - planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
  ---
  duration_ms: 0.323888
  ...
# Subtest: planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
ok 1904 - planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
  ---
  duration_ms: 0.374996
  ...
# Subtest: planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
ok 1905 - planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
  ---
  duration_ms: 0.469716
  ...
# Subtest: planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
ok 1906 - planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
  ---
  duration_ms: 0.329449
  ...
# Subtest: planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
ok 1907 - planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
  ---
  duration_ms: 0.44034
  ...
# Subtest: planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
ok 1908 - planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
  ---
  duration_ms: 0.286708
  ...
# Subtest: planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
ok 1909 - planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
  ---
  duration_ms: 0.336913
  ...
# Subtest: planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
ok 1910 - planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
  ---
  duration_ms: 0.205482
  ...
# Subtest: planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
ok 1911 - planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
  ---
  duration_ms: 0.398581
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
ok 1912 - planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
  ---
  duration_ms: 0.213066
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
ok 1913 - planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
  ---
  duration_ms: 0.408469
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
ok 1914 - planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
  ---
  duration_ms: 2.442813
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
ok 1915 - planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
  ---
  duration_ms: 0.480157
  ...
# Subtest: Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
ok 1916 - Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
  ---
  duration_ms: 5.365442
  ...
# Subtest: commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
ok 1917 - commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
  ---
  duration_ms: 3.14272
  ...
# Subtest: commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
ok 1918 - commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
  ---
  duration_ms: 0.940085
  ...
# Subtest: commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
ok 1919 - commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
  ---
  duration_ms: 0.456932
  ...
# Subtest: commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
ok 1920 - commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
  ---
  duration_ms: 0.386709
  ...
# Subtest: Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
ok 1921 - Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
  ---
  duration_ms: 7.510096
  ...
# Subtest: Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
ok 1922 - Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
  ---
  duration_ms: 0.819043
  ...
# Subtest: Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
ok 1923 - Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
  ---
  duration_ms: 0.740824
  ...
# Subtest: Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
ok 1924 - Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
  ---
  duration_ms: 1.120149
  ...
# Subtest: task move picker closes before commit while other pickers retain delayed close
ok 1925 - task move picker closes before commit while other pickers retain delayed close
  ---
  duration_ms: 0.879519
  ...
# Subtest: parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
ok 1926 - parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
  ---
  duration_ms: 1.884608
  ...
# Subtest: normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
ok 1927 - normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
  ---
  duration_ms: 0.359506
  ...
# Subtest: formatPomodoroEntryLine emits a placeholder entry with or without a name
ok 1928 - formatPomodoroEntryLine emits a placeholder entry with or without a name
  ---
  duration_ms: 0.13075
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
ok 1929 - createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
  ---
  duration_ms: 1.941716
  ...
# Subtest: createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
ok 1930 - createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
  ---
  duration_ms: 0.749981
  ...
# Subtest: createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
ok 1931 - createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
  ---
  duration_ms: 0.615665
  ...
# Subtest: createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
ok 1932 - createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
  ---
  duration_ms: 0.625033
  ...
# Subtest: buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
ok 1933 - buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
  ---
  duration_ms: 0.208839
  ...
# Subtest: buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
ok 1934 - buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
  ---
  duration_ms: 0.352684
  ...
# Subtest: createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
ok 1935 - createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
  ---
  duration_ms: 0.583003
  ...
# Subtest: createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
ok 1936 - createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
  ---
  duration_ms: 0.317425
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
ok 1937 - createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
  ---
  duration_ms: 0.302196
  ...
# Subtest: collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
ok 1938 - collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
  ---
  duration_ms: 0.383101
  ...
# Subtest: findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
ok 1939 - findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
  ---
  duration_ms: 0.464036
  ...
# Subtest: findPomodoroBulletContext leaves plain \#task lines on the task-move route
ok 1940 - findPomodoroBulletContext leaves plain \#task lines on the task-move route
  ---
  duration_ms: 0.289844
  ...
# Subtest: discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
ok 1941 - discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
  ---
  duration_ms: 0.751625
  ...
# Subtest: findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
ok 1942 - findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
  ---
  duration_ms: 0.699045
  ...
# Subtest: discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
ok 1943 - discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
  ---
  duration_ms: 0.818613
  ...
# Subtest: isMovablePomodoroEntryContext matches open current and future Pomodoro entries
ok 1944 - isMovablePomodoroEntryContext matches open current and future Pomodoro entries
  ---
  duration_ms: 3.752654
  ...
# Subtest: planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
ok 1945 - planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
  ---
  duration_ms: 0.783495
  ...
# Subtest: planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
ok 1946 - planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
  ---
  duration_ms: 0.305183
  ...
# Subtest: planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
ok 1947 - planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
  ---
  duration_ms: 0.375247
  ...
# Subtest: planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
ok 1948 - planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
  ---
  duration_ms: 0.508341
  ...
# Subtest: planPomodoroEntryReorder handles counted current swaps and their inverses
ok 1949 - planPomodoroEntryReorder handles counted current swaps and their inverses
  ---
  duration_ms: 0.477451
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
ok 1950 - planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
  ---
  duration_ms: 0.230399
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
ok 1951 - planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
  ---
  duration_ms: 0.211013
  ...
# Subtest: planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
ok 1952 - planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
  ---
  duration_ms: 0.522367
  ...
# Subtest: planPomodoroEntryReorder round-trips a future-up swap across the current open entry
ok 1953 - planPomodoroEntryReorder round-trips a future-up swap across the current open entry
  ---
  duration_ms: 0.542595
  ...
# Subtest: planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
ok 1954 - planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
  ---
  duration_ms: 0.501026
  ...
# Subtest: planPomodoroEntryReorder refuses moving down past the last placeholder in the section
ok 1955 - planPomodoroEntryReorder refuses moving down past the last placeholder in the section
  ---
  duration_ms: 0.192978
  ...
# Subtest: planPomodoroEntryReorder refuses both directions for a lone placeholder
ok 1956 - planPomodoroEntryReorder refuses both directions for a lone placeholder
  ---
  duration_ms: 0.15704
  ...
# Subtest: planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
ok 1957 - planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
  ---
  duration_ms: 0.148593
  ...
# Subtest: planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
ok 1958 - planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
  ---
  duration_ms: 0.256569
  ...
# Subtest: planPomodoroEntryReorder refuses illegal current/future spans atomically
ok 1959 - planPomodoroEntryReorder refuses illegal current/future spans atomically
  ---
  duration_ms: 0.514952
  ...
# Subtest: planPomodoroEntryReorder rejects a stale source line
ok 1960 - planPomodoroEntryReorder rejects a stale source line
  ---
  duration_ms: 0.171317
  ...
# Subtest: planPomodoroEntryReorder round-trips CRLF content
ok 1961 - planPomodoroEntryReorder round-trips CRLF content
  ---
  duration_ms: 0.264996
  ...
# Subtest: planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
ok 1962 - planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
  ---
  duration_ms: 0.191685
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
ok 1963 - planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
  ---
  duration_ms: 0.285655
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up three positions and round-trips
ok 1964 - planPomodoroEntryReorder moves a placeholder up three positions and round-trips
  ---
  duration_ms: 0.395605
  ...
# Subtest: planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
ok 1965 - planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
  ---
  duration_ms: 0.234167
  ...
# Subtest: planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
ok 1966 - planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
  ---
  duration_ms: 0.742758
  ...
# Subtest: planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
ok 1967 - planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
  ---
  duration_ms: 2.547353
  ...
# Subtest: planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
ok 1968 - planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
  ---
  duration_ms: 0.514652
  ...
# Subtest: peelPomodoroMergedName removes every matching canonical plus component
ok 1969 - peelPomodoroMergedName removes every matching canonical plus component
  ---
  duration_ms: 1.477831
  ...
# Subtest: planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
ok 1970 - planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
  ---
  duration_ms: 3.595643
  ...
# Subtest: planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
ok 1971 - planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
  ---
  duration_ms: 0.580719
  ...
# Subtest: planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
ok 1972 - planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
  ---
  duration_ms: 0.687232
  ...
# Subtest: planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
ok 1973 - planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
  ---
  duration_ms: 0.88048
  ...
# Subtest: planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
ok 1974 - planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
  ---
  duration_ms: 1.334257
  ...
# Subtest: planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
ok 1975 - planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
  ---
  duration_ms: 0.722339
  ...
# Subtest: planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
ok 1976 - planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
  ---
  duration_ms: 1.226371
  ...
# Subtest: Pomodoro bullet move picker typing =NAME or Escape does not write
ok 1977 - Pomodoro bullet move picker typing =NAME or Escape does not write
  ---
  duration_ms: 2.193227
  ...
# Subtest: planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
ok 1978 - planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
  ---
  duration_ms: 0.465769
  ...
# Subtest: planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
ok 1979 - planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
  ---
  duration_ms: 0.260548
  ...
# Subtest: planPomodoroEntryRename reports unchanged when the normalized name matches the current name
ok 1980 - planPomodoroEntryRename reports unchanged when the normalized name matches the current name
  ---
  duration_ms: 0.123847
  ...
# Subtest: planPomodoroEntryRename rejects unsupported trailing content and a stale source line
ok 1981 - planPomodoroEntryRename rejects unsupported trailing content and a stale source line
  ---
  duration_ms: 0.135309
  ...
# Subtest: planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
ok 1982 - planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
  ---
  duration_ms: 0.142442
  ...
# Subtest: planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
ok 1983 - planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
  ---
  duration_ms: 2.538606
  ...
# Subtest: planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
ok 1984 - planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
  ---
  duration_ms: 0.95866
  ...
# Subtest: planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
ok 1985 - planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
  ---
  duration_ms: 0.472852
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: priority notice relative day helpers handle offsets ranges and icons
ok 1986 - priority notice relative day helpers handle offsets ranges and icons
  ---
  duration_ms: 1.1949
  ...
# Subtest: priority notice model summarizes single counted and project writes
ok 1987 - priority notice model summarizes single counted and project writes
  ---
  duration_ms: 2.92303
  ...
# Subtest: priority notice renderer builds an accessible fragment
ok 1988 - priority notice renderer builds an accessible fragment
  ---
  duration_ms: 1.834282
  ...
# Subtest: priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
ok 1989 - priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
  ---
  duration_ms: 7.892576
  ...
# Subtest: priority notice falls back to one plain notice without a DOM
ok 1990 - priority notice falls back to one plain notice without a DOM
  ---
  duration_ms: 0.580518
  ...
# Subtest: priority notice falls back to plain text when fragment rendering fails
ok 1991 - priority notice falls back to plain text when fragment rendering fails
  ---
  duration_ms: 0.364065
  ...
# Subtest: priority scheduling rolls inclusively and clamps a random value of one
ok 1992 - priority scheduling rolls inclusively and clamps a random value of one
  ---
  duration_ms: 0.511206
  ...
# Subtest: priority value rows preserve config order and expose labels ranges and current state
ok 1993 - priority value rows preserve config order and expose labels ranges and current state
  ---
  duration_ms: 0.762686
  ...
# Subtest: priority picker writes priority then rolled schedule in one guarded edit
ok 1994 - priority picker writes priority then rolled schedule in one guarded edit
  ---
  duration_ms: 13.641843
  ...
# Subtest: priority picker writes lowest priority with a wide rolled schedule
ok 1995 - priority picker writes lowest priority with a wide rolled schedule
  ---
  duration_ms: 2.591467
  ...
# Subtest: priority picker replaces both existing values without duplicating fields
ok 1996 - priority picker replaces both existing values without duplicating fields
  ---
  duration_ms: 2.708499
  ...
# Subtest: counted priority writes keep the rolled date right of the priority
ok 1997 - counted priority writes keep the rolled date right of the priority
  ---
  duration_ms: 5.923067
  ...
# Subtest: priority picker writes project priority and schedule inline atomically
ok 1998 - priority picker writes project priority and schedule inline atomically
  ---
  duration_ms: 4.846903
  ...
# Subtest: counted priority picker rolls an independent schedule for every task
ok 1999 - counted priority picker rolls an independent schedule for every task
  ---
  duration_ms: 2.338273
  ...
# Subtest: counted priority planning keeps project schedules inline
ok 2000 - counted priority planning keeps project schedules inline
  ---
  duration_ms: 0.893466
  ...
# Subtest: counted priority planning evaluates Blocked recovery per rolled date
ok 2001 - counted priority planning evaluates Blocked recovery per rolled date
  ---
  duration_ms: 1.16767
  ...
# Subtest: a counted priority batch writes one entry per task using each task's own previous level
ok 2002 - a counted priority batch writes one entry per task using each task's own previous level
  ---
  duration_ms: 0.955654
  ...
# Subtest: priority notice models carry the stored level value for the glyph
ok 2003 - priority notice models carry the stored level value for the glyph
  ---
  duration_ms: 0.458706
  ...
# Subtest: ledger priority mark lookup guards version and render
ok 2004 - ledger priority mark lookup guards version and render
  ---
  duration_ms: 0.18332
  ...
# Subtest: priority notice header reuses the shared mark when available
ok 2005 - priority notice header reuses the shared mark when available
  ---
  duration_ms: 0.455279
  ...
# Subtest: priority notice keeps the Lucide icon without a usable mark api
ok 2006 - priority notice keeps the Lucide icon without a usable mark api
  ---
  duration_ms: 1.362231
  ...
# Subtest: a counted priority batch skips a task whose rolled date equals its current date
ok 2007 - a counted priority batch skips a task whose rolled date equals its current date
  ---
  duration_ms: 4.029352
  ...
# Subtest: counted priority runtime aborts a stale session without rolling writes
ok 2008 - counted priority runtime aborts a stale session without rolling writes
  ---
  duration_ms: 1.90133
  ...
# Subtest: scheduled picker pins a priority roll only for configured current priorities
ok 2009 - scheduled picker pins a priority roll only for configured current priorities
  ---
  duration_ms: 21.384452
  ...
# Subtest: Ctrl+R replaces only the pinned priority roll and keeps it selected
ok 2010 - Ctrl+R replaces only the pinned priority roll and keeps it selected
  ---
  duration_ms: 7.264578
  ...
# Subtest: choosing a priority roll writes immediately with a deterministic reason instead of prompting
ok 2011 - choosing a priority roll writes immediately with a deterministic reason instead of prompting
  ---
  duration_ms: 6.00808
  ...
# Subtest: counted scheduled picker requires one shared configured priority
ok 2012 - counted scheduled picker requires one shared configured priority
  ---
  duration_ms: 7.663287
  ...
# Subtest: buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
ok 2013 - buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
  ---
  duration_ms: 2.873425
  ...
# Subtest: buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
ok 2014 - buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
  ---
  duration_ms: 0.298199
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
ok 2015 - buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
  ---
  duration_ms: 0.410634
  ...
# Subtest: buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
ok 2016 - buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
  ---
  duration_ms: 0.270747
  ...
# Subtest: buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
ok 2017 - buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
  ---
  duration_ms: 0.404041
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
ok 2018 - buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
  ---
  duration_ms: 0.16243
  ...
# Subtest: buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
ok 2019 - buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
  ---
  duration_ms: 0.224859
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
ok 2020 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
  ---
  duration_ms: 0.359897
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child work log under the project task
ok 2021 - buildProjectSeedFromChildBullets moves a direct-child work log under the project task
  ---
  duration_ms: 0.328076
  ...
# Subtest: buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
ok 2022 - buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
  ---
  duration_ms: 0.424611
  ...
# Subtest: buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
ok 2023 - buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
  ---
  duration_ms: 0.259776
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
ok 2024 - buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
  ---
  duration_ms: 0.147251
  ...
# Subtest: buildProjectSeedFromChildBullets moves an empty work log without forcing task output
ok 2025 - buildProjectSeedFromChildBullets moves an empty work log without forcing task output
  ---
  duration_ms: 0.116562
  ...
# Subtest: buildProjectSeedFromChildBullets moves both logs in source order without sorting by kind
ok 2026 - buildProjectSeedFromChildBullets moves both logs in source order without sorting by kind
  ---
  duration_ms: 0.113948
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
ok 2027 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
  ---
  duration_ms: 0.23616
  ...
# Subtest: parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
ok 2028 - parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
  ---
  duration_ms: 0.232353
  ...
# Subtest: parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
ok 2029 - parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
  ---
  duration_ms: 0.153723
  ...
# Subtest: parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
ok 2030 - parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
  ---
  duration_ms: 0.452634
  ...
# Subtest: normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
ok 2031 - normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
  ---
  duration_ms: 0.087347
  ...
# Subtest: parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
ok 2032 - parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
  ---
  duration_ms: 0.098979
  ...
# Subtest: formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
ok 2033 - formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
  ---
  duration_ms: 0.110431
  ...
# Subtest: insertProjectSectionNotes fills an empty existing section with a blank line then the notes
ok 2034 - insertProjectSectionNotes fills an empty existing section with a blank line then the notes
  ---
  duration_ms: 0.578023
  ...
# Subtest: insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
ok 2035 - insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
  ---
  duration_ms: 0.168021
  ...
# Subtest: insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
ok 2036 - insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
  ---
  duration_ms: 0.129929
  ...
# Subtest: insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
ok 2037 - insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
  ---
  duration_ms: 0.237724
  ...
# Subtest: insertProjectSectionNotes does not add a trailing newline when the original content had none
ok 2038 - insertProjectSectionNotes does not add a trailing newline when the original content had none
  ---
  duration_ms: 0.137893
  ...
# Subtest: insertProjectSectionNotes preserves CRLF line endings for an existing section
ok 2039 - insertProjectSectionNotes preserves CRLF line endings for an existing section
  ---
  duration_ms: 0.175846
  ...
# Subtest: insertProjectSectionNotes creates a new section using the document's CRLF line ending
ok 2040 - insertProjectSectionNotes creates a new section using the document's CRLF line ending
  ---
  duration_ms: 0.124869
  ...
# Subtest: buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
ok 2041 - buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
  ---
  duration_ms: 0.173742
  ...
# Subtest: buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
ok 2042 - buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
  ---
  duration_ms: 0.348084
  ...
# Subtest: buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
ok 2043 - buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
  ---
  duration_ms: 0.124829
  ...
# Subtest: buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
ok 2044 - buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
  ---
  duration_ms: 1.074271
  ...
# Subtest: project conversion accepts blocked sources and extracts their managed dependency child
ok 2045 - project conversion accepts blocked sources and extracts their managed dependency child
  ---
  duration_ms: 2.052478
  ...
# Subtest: project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
ok 2046 - project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
  ---
  duration_ms: 1.125117
  ...
# Subtest: buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
ok 2047 - buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
  ---
  duration_ms: 0.362792
  ...
# Subtest: buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
ok 2048 - buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
  ---
  duration_ms: 0.215652
  ...
# Subtest: buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
ok 2049 - buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
  ---
  duration_ms: 0.195723
  ...
# Subtest: insertProjectManagedLogLines preserves CRLF line endings
ok 2050 - insertProjectManagedLogLines preserves CRLF line endings
  ---
  duration_ms: 0.15679
  ...
# Subtest: findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
ok 2051 - findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
  ---
  duration_ms: 0.197848
  ...
# Subtest: getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
ok 2052 - getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
  ---
  duration_ms: 0.201915
  ...
# Subtest: getProjectFromTaskNoticeText reports moved log kinds in a fixed order
ok 2053 - getProjectFromTaskNoticeText reports moved log kinds in a fixed order
  ---
  duration_ms: 0.110771
  ...
# Subtest: forward conversion leaves the project Ready when only the source status was Blocked
ok 2054 - forward conversion leaves the project Ready when only the source status was Blocked
  ---
  duration_ms: 0.376218
  ...
# Subtest: buildTaskBlockFromProjectNote restores the worked example and round-trips
ok 2055 - buildTaskBlockFromProjectNote restores the worked example and round-trips
  ---
  duration_ms: 7.415265
  ...
# Subtest: project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
ok 2056 - project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
  ---
  duration_ms: 2.241539
  ...
# Subtest: buildTaskLineFromProjectNote preserves status, tags, and fields
ok 2057 - buildTaskLineFromProjectNote preserves status, tags, and fields
  ---
  duration_ms: 1.360507
  ...
# Subtest: getProjectReversalBlockId inverts the forward basename helper
ok 2058 - getProjectReversalBlockId inverts the forward basename helper
  ---
  duration_ms: 0.135529
  ...
# Subtest: formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
ok 2059 - formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
  ---
  duration_ms: 0.136561
  ...
# Subtest: splitProjectNoteForReversal treats TASKS as the task section and keeps section order
ok 2060 - splitProjectNoteForReversal treats TASKS as the task section and keeps section order
  ---
  duration_ms: 0.910227
  ...
# Subtest: indentProjectReversalLine preserves relative depth and drops blanks
ok 2061 - indentProjectReversalLine preserves relative depth and drops blanks
  ---
  duration_ms: 0.457364
  ...
# Subtest: buildTaskBlockFromProjectNote reports structure and frontmatter errors
ok 2062 - buildTaskBlockFromProjectNote reports structure and frontmatter errors
  ---
  duration_ms: 1.296826
  ...
# Subtest: buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
ok 2063 - buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
  ---
  duration_ms: 1.01689
  ...
# Subtest: rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
ok 2064 - rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
  ---
  duration_ms: 0.505244
  ...
# Subtest: collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
ok 2065 - collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
  ---
  duration_ms: 0.646604
  ...
# Subtest: getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
ok 2066 - getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
  ---
  duration_ms: 0.246631
  ...
# Subtest: convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
ok 2067 - convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
  ---
  duration_ms: 5.174888
  ...
# Subtest: project reversal recovers tagged residents when they leave a blocked project
ok 2068 - project reversal recovers tagged residents when they leave a blocked project
  ---
  duration_ms: 3.716385
  ...
# Subtest: convertProjectNoteToTask separates the restored task from a count-only parent section
ok 2069 - convertProjectNoteToTask separates the restored task from a count-only parent section
  ---
  duration_ms: 1.076676
  ...
# Subtest: createProjectNoteFromTask dispatches reverse only on a real ^prj line
ok 2070 - createProjectNoteFromTask dispatches reverse only on a real ^prj line
  ---
  duration_ms: 3.554435
  ...
# Subtest: convertProjectNoteToTask refusals leave every file untouched
ok 2071 - convertProjectNoteToTask refusals leave every file untouched
  ---
  duration_ms: 3.877792
  ...
# Subtest: planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
ok 2072 - planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
  ---
  duration_ms: 0.147452
  ...
# Subtest: convertProjectNoteToTask writes the parent first when it links to \#^prj
ok 2073 - convertProjectNoteToTask writes the parent first when it links to \#^prj
  ---
  duration_ms: 1.072537
  ...
# Subtest: convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
ok 2074 - convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
  ---
  duration_ms: 2.994877
  ...
# Subtest: convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
ok 2075 - convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
  ---
  duration_ms: 0.968169
  ...
# Subtest: convertProjectNoteToTask reports post-write failures without rolling back
ok 2076 - convertProjectNoteToTask reports post-write failures without rolling back
  ---
  duration_ms: 0.92205
  ...
# Subtest: convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
ok 2077 - convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
  ---
  duration_ms: 0.986673
  ...
# Subtest: convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
ok 2078 - convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
  ---
  duration_ms: 1.280164
  ...
# Subtest: v2 reading task opens its source_pdf in Highlights without writes
ok 2079 - v2 reading task opens its source_pdf in Highlights without writes
  ---
  duration_ms: 3.077695
  ...
# Subtest: every reading-task lane and \#REF casing opens
ok 2080 - every reading-task lane and \#REF casing opens
  ---
  duration_ms: 1.228265
  ...
# Subtest: v1 tracker resolves a PDF link or falls back to its own source_pdf
ok 2081 - v1 tracker resolves a PDF link or falls back to its own source_pdf
  ---
  duration_ms: 0.554719
  ...
# Subtest: plain, embedded, struck, and 🍅 Task Links resolve reading tasks
ok 2082 - plain, embedded, struck, and 🍅 Task Links resolve reading tasks
  ---
  duration_ms: 2.382047
  ...
# Subtest: bare managed embed in a reference note resolves its embedded task
ok 2083 - bare managed embed in a reference note resolves its embedded task
  ---
  duration_ms: 0.395755
  ...
# Subtest: ordinary lines, unresolved Task Links, fences, and outside focus delegate once
ok 2084 - ordinary lines, unresolved Task Links, fences, and outside focus delegate once
  ---
  duration_ms: 0.788355
  ...
# Subtest: identified reading tasks show notices without delegating
ok 2085 - identified reading tasks show notices without delegating
  ---
  duration_ms: 0.537777
  ...
# Subtest: unsafe source_pdf values are refused
ok 2086 - unsafe source_pdf values are refused
  ---
  duration_ms: 0.229608
  ...
# Subtest: bundle launch retries with the app name, and reports stderr on total failure
ok 2087 - bundle launch retries with the app name, and reports stderr on total failure
  ---
  duration_ms: 0.720144
  ...
# Subtest: off macOS shows the selected notice and managed ref-note prose delegates
ok 2088 - off macOS shows the selected notice and managed ref-note prose delegates
  ---
  duration_ms: 0.538006
  ...
# Subtest: pure helpers normalize and parse reference PDF paths
ok 2089 - pure helpers normalize and parse reference PDF paths
  ---
  duration_ms: 0.260618
  ...
# Subtest: command registration is custom-hotkey only
ok 2090 - command registration is custom-hotkey only
  ---
  duration_ms: 0.348175
  ...
# Subtest: nav api openReferencePdf hands a source_pdf to Highlights without version or vault writes
ok 2091 - nav api openReferencePdf hands a source_pdf to Highlights without version or vault writes
  ---
  duration_ms: 0.564347
  ...
# Subtest: nav api openReferencePdf settles to a reason instead of throwing
ok 2092 - nav api openReferencePdf settles to a reason instead of throwing
  ---
  duration_ms: 0.350289
  ...
# Subtest: reading tasks read with the book prefix, plain tasks unchanged
ok 2093 - reading tasks read with the book prefix, plain tasks unchanged
  ---
  duration_ms: 1.139586
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 2094 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.23553
  ...
# Subtest: picker rows carry the book prefix in displayText
ok 2095 - picker rows carry the book prefix in displayText
  ---
  duration_ms: 0.639441
  ...
# Subtest: managed reference rename modal and submit are refused
ok 2096 - managed reference rename modal and submit are refused
  ---
  duration_ms: 1.285404
  ...
# Subtest: legacy ref notes and non-ref notes still rename
ok 2097 - legacy ref notes and non-ref notes still rename
  ---
  duration_ms: 0.951606
  ...
# Subtest: managed reference predicate checks path and non-empty source_pdf
ok 2098 - managed reference predicate checks path and non-empty source_pdf
  ---
  duration_ms: 0.207696
  ...
# Subtest: planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
ok 2099 - planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
  ---
  duration_ms: 6.853625
  ...
# Subtest: planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
ok 2100 - planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
  ---
  duration_ms: 2.532514
  ...
# Subtest: runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
ok 2101 - runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
  ---
  duration_ms: 5.489347
  ...
# Subtest: runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
ok 2102 - runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
  ---
  duration_ms: 3.613949
  ...
# Subtest: runtime: no daily note today still writes the schedule with no Pomodoro chip
ok 2103 - runtime: no daily note today still writes the schedule with no Pomodoro chip
  ---
  duration_ms: 0.572172
  ...
# Subtest: runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
ok 2104 - runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
  ---
  duration_ms: 1.23651
  ...
# Subtest: runtime: vault.process throwing during the daily-note write is reported without throwing
ok 2105 - runtime: vault.process throwing during the daily-note write is reported without throwing
  ---
  duration_ms: 0.977466
  ...
# Subtest: runtime: the daily note open in another editor is written through that editor in its own transaction
ok 2106 - runtime: the daily note open in another editor is written through that editor in its own transaction
  ---
  duration_ms: 1.890059
  ...
# Subtest: runtime: re-running the same deferral gesture is idempotent
ok 2107 - runtime: re-running the same deferral gesture is idempotent
  ---
  duration_ms: 0.934263
  ...
# Subtest: runtime: a counted scheduled batch prunes exactly the targets that land on a future date
ok 2108 - runtime: a counted scheduled batch prunes exactly the targets that land on a future date
  ---
  duration_ms: 3.684223
  ...
# Subtest: runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
ok 2109 - runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
  ---
  duration_ms: 2.547253
  ...
# Subtest: runtime: the source note being today's daily note folds the prune into a single editor transaction
ok 2110 - runtime: the source note being today's daily note folds the prune into a single editor transaction
  ---
  duration_ms: 0.749852
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: bare future scheduled writes block only real supported open inline tasks
ok 2111 - bare future scheduled writes block only real supported open inline tasks
  ---
  duration_ms: 5.502274
  ...
# Subtest: single runtime transclusion toggle preserves viewport in one line transaction
ok 2112 - single runtime transclusion toggle preserves viewport in one line transaction
  ---
  duration_ms: 2.35734
  ...
# Subtest: same-file runtime toggle changes only markers, never fields or statuses
ok 2113 - same-file runtime toggle changes only markers, never fields or statuses
  ---
  duration_ms: 0.815156
  ...
# Subtest: pure toggle leaves a cursor moved during the toggle where it landed
ok 2114 - pure toggle leaves a cursor moved during the toggle where it landed
  ---
  duration_ms: 0.348185
  ...
# Subtest: counted runtime transclusion toggle preserves viewport and caret
ok 2115 - counted runtime transclusion toggle preserves viewport and caret
  ---
  duration_ms: 0.960894
  ...
# Subtest: counted property runtime uses one transaction and preserves caret and viewport
ok 2116 - counted property runtime uses one transaction and preserves caret and viewport
  ---
  duration_ms: 3.454455
  ...
# Subtest: bare due schedule recovery is guarded and can change only task status
ok 2117 - bare due schedule recovery is guarded and can change only task status
  ---
  duration_ms: 2.547724
  ...
# Subtest: counted due recovery applies Ready Next and In Progress in one transaction
ok 2118 - counted due recovery applies Ready Next and In Progress in one transaction
  ---
  duration_ms: 4.283777
  ...
# Subtest: scheduled recovery aborts after an asynchronous source change
ok 2119 - scheduled recovery aborts after an asynchronous source change
  ---
  duration_ms: 0.754961
  ...
# Subtest: counted property runtime aborts a stale batch without a transaction
ok 2120 - counted property runtime aborts a stale batch without a transaction
  ---
  duration_ms: 0.493923
  ...
# Subtest: counted project scheduling writes an inline date and blocks tagged residents
ok 2121 - counted project scheduling writes an inline date and blocks tagged residents
  ---
  duration_ms: 2.47302
  ...
# Subtest: future project scheduling prunes resident links and an emptied Pomodoro
ok 2122 - future project scheduling prunes resident links and an emptied Pomodoro
  ---
  duration_ms: 2.847035
  ...
# Subtest: single project scheduling recovers due residents through the gate
ok 2123 - single project scheduling recovers due residents through the gate
  ---
  duration_ms: 1.696149
  ...
# Subtest: single project schedule deletion removes propagated copies and recovers
ok 2124 - single project schedule deletion removes propagated copies and recovers
  ---
  duration_ms: 1.603191
  ...
# Subtest: formatPriorityRollScheduleReason covers all four shapes
ok 2125 - formatPriorityRollScheduleReason covers all four shapes
  ---
  duration_ms: 1.850342
  ...
# Subtest: the priority-roll picker row keeps range detail and stores the exact roll
ok 2126 - the priority-roll picker row keeps range detail and stores the exact roll
  ---
  duration_ms: 0.755362
  ...
# Subtest: buildPriorityRollScheduleLog returns null when the roll does not move the date
ok 2127 - buildPriorityRollScheduleLog returns null when the roll does not move the date
  ---
  duration_ms: 0.931759
  ...
# Subtest: getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
ok 2128 - getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
  ---
  duration_ms: 0.9849
  ...
# Subtest: a priority roll onto the current date writes the date but no log
ok 2129 - a priority roll onto the current date writes the date but no log
  ---
  duration_ms: 20.674767
  ...
# Subtest: a typed reason on an unchanged date is still written
ok 2130 - a typed reason on an unchanged date is still written
  ---
  duration_ms: 1.048912
  ...
# Subtest: schedule log bullet formatting and parsing round-trip with and without a previous value
ok 2131 - schedule log bullet formatting and parsing round-trip with and without a previous value
  ---
  duration_ms: 1.341661
  ...
# Subtest: formatScheduleLogEntryText renders entry text without indent or marker
ok 2132 - formatScheduleLogEntryText renders entry text without indent or marker
  ---
  duration_ms: 0.166899
  ...
# Subtest: schedule reason text normalization trims, collapses whitespace, and flags inline fields
ok 2133 - schedule reason text normalization trims, collapses whitespace, and flags inline fields
  ---
  duration_ms: 0.470528
  ...
# Subtest: findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
ok 2134 - findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
  ---
  duration_ms: 1.038302
  ...
# Subtest: getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
ok 2135 - getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
  ---
  duration_ms: 0.30382
  ...
# Subtest: planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
ok 2136 - planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
  ---
  duration_ms: 0.566362
  ...
# Subtest: planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
ok 2137 - planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
  ---
  duration_ms: 0.256299
  ...
# Subtest: planScheduleLogEntry uses the fallback only when a marker exists
ok 2138 - planScheduleLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.268783
  ...
# Subtest: a typed reason wins over the fallback
ok 2139 - a typed reason wins over the fallback
  ---
  duration_ms: 0.194922
  ...
# Subtest: the fallback is suppressed on an unchanged date
ok 2140 - the fallback is suppressed on an unchanged date
  ---
  duration_ms: 0.154415
  ...
# Subtest: no reason and no fallback still guards empty-reason
ok 2141 - no reason and no fallback still guards empty-reason
  ---
  duration_ms: 0.13093
  ...
# Subtest: getScheduleLogWriteOutcome maps plan outcomes for writers
ok 2142 - getScheduleLogWriteOutcome maps plan outcomes for writers
  ---
  duration_ms: 0.169543
  ...
# Subtest: hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
ok 2143 - hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
  ---
  duration_ms: 0.161458
  ...
# Subtest: counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
ok 2144 - counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
  ---
  duration_ms: 2.254072
  ...
# Subtest: empty reason through the counted planner writes no schedule log entries
ok 2145 - empty reason through the counted planner writes no schedule log entries
  ---
  duration_ms: 0.660591
  ...
# Subtest: a counted scheduled session logs only the tasks that already keep a log
ok 2146 - a counted scheduled session logs only the tasks that already keep a log
  ---
  duration_ms: 0.746244
  ...
# Subtest: the counted notice wording distinguishes a fallback batch from a typed-reason batch
ok 2147 - the counted notice wording distinguishes a fallback batch from a typed-reason batch
  ---
  duration_ms: 4.899383
  ...
# Subtest: setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
ok 2148 - setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
  ---
  duration_ms: 0.472072
  ...
# Subtest: setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
ok 2149 - setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
  ---
  duration_ms: 3.936255
  ...
# Subtest: priority bullet property config normalizes frozen levels and preserves existing shapes
ok 2150 - priority bullet property config normalizes frozen levels and preserves existing shapes
  ---
  duration_ms: 3.209587
  ...
# Subtest: priority bullet property config rejects each invalid schema category once
ok 2151 - priority bullet property config rejects each invalid schema category once
  ---
  duration_ms: 1.605134
  ...
# Subtest: project scheduling targets the inline ^prj field
ok 2152 - project scheduling targets the inline ^prj field
  ---
  duration_ms: 2.700255
  ...
# Subtest: local task properties are addable only on valid tasks but invalid metadata stays removable
ok 2153 - local task properties are addable only on valid tasks but invalid metadata stays removable
  ---
  duration_ms: 0.440371
  ...
# Subtest: dependency parent write validation rejects stale, Pomodoro, and fenced parents
ok 2154 - dependency parent write validation rejects stale, Pomodoro, and fenced parents
  ---
  duration_ms: 0.735795
  ...
# Subtest: counted property targets mean current plus N real tasks without wrapping
ok 2155 - counted property targets mean current plus N real tasks without wrapping
  ---
  duration_ms: 0.963769
  ...
# Subtest: counted property metadata distinguishes absent, common, and mixed values
ok 2156 - counted property metadata distinguishes absent, common, and mixed values
  ---
  duration_ms: 0.91687
  ...
# Subtest: counted priority metadata reports labels for common and mixed values
ok 2157 - counted priority metadata reports labels for common and mixed values
  ---
  duration_ms: 0.791651
  ...
# Subtest: counted scheduled planning updates the motivating three tasks atomically
ok 2158 - counted scheduled planning updates the motivating three tasks atomically
  ---
  duration_ms: 3.220557
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: project schedule validation accepts only real YYYY-MM-DD dates
ok 2159 - project schedule validation accepts only real YYYY-MM-DD dates
  ---
  duration_ms: 1.035828
  ...
# Subtest: source task schedule is extracted without losing task metadata
ok 2160 - source task schedule is extracted without losing task metadata
  ---
  duration_ms: 1.269324
  ...
# Subtest: source task schedule errors are focused and ambiguous fields fail
ok 2161 - source task schedule errors are focused and ambiguous fields fail
  ---
  duration_ms: 0.352122
  ...
# Subtest: project creation frontmatter never stores the task schedule
ok 2162 - project creation frontmatter never stores the task schedule
  ---
  duration_ms: 0.155838
  ...
# Subtest: future schedule labels use local date-only boundaries
ok 2163 - future schedule labels use local date-only boundaries
  ---
  duration_ms: 0.56561
  ...
# Subtest: scheduled recovery selects current and newest earlier daily across gaps
ok 2164 - scheduled recovery selects current and newest earlier daily across gaps
  ---
  duration_ms: 0.551974
  ...
# Subtest: scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
ok 2165 - scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
  ---
  duration_ms: 8.308328
  ...
# Subtest: scheduled recovery defers incompatible status settings and ambiguous identities
ok 2166 - scheduled recovery defers incompatible status settings and ambiguous identities
  ---
  duration_ms: 0.39813
  ...
# Subtest: scheduled recovery honors custom open and closed Tasks status types
ok 2167 - scheduled recovery honors custom open and closed Tasks status types
  ---
  duration_ms: 0.611408
  ...
# Subtest: scheduled recovery honors the configured Tasks global filter
ok 2168 - scheduled recovery honors the configured Tasks global filter
  ---
  duration_ms: 0.516326
  ...
# Subtest: child picker schedule metadata reads the inline ^prj date
ok 2169 - child picker schedule metadata reads the inline ^prj date
  ---
  duration_ms: 0.859722
  ...
# Subtest: task move destination schedule hydration reads cached ^prj content
ok 2170 - task move destination schedule hydration reads cached ^prj content
  ---
  duration_ms: 0.4556
  ...
# Subtest: project lifecycle task classification requires unfenced \#task with trailing ^prj
ok 2171 - project lifecycle task classification requires unfenced \#task with trailing ^prj
  ---
  duration_ms: 0.158843
  ...
# Subtest: valid Obsidian tasks require a standalone \#task checkbox in real note content
ok 2172 - valid Obsidian tasks require a standalone \#task checkbox in real note content
  ---
  duration_ms: 0.154885
  ...
# Subtest: choosing a scheduled date enters the combined review without writing anything
ok 2173 - choosing a scheduled date enters the combined review without writing anything
  ---
  duration_ms: 11.260126
  ...
# Subtest: choosing a priority level does not enter the schedule review
ok 2174 - choosing a priority level does not enter the schedule review
  ---
  duration_ms: 8.882776
  ...
# Subtest: confirming an empty reason on a task with an existing schedule log appends an unexplained entry
ok 2175 - confirming an empty reason on a task with an existing schedule log appends an unexplained entry
  ---
  duration_ms: 5.799521
  ...
# Subtest: confirming an empty reason on a task with no schedule log writes only the date
ok 2176 - confirming an empty reason on a task with no schedule log writes only the date
  ---
  duration_ms: 2.993125
  ...
# Subtest: review stage getFilteredItems always returns exactly one synthetic preview item
ok 2177 - review stage getFilteredItems always returns exactly one synthetic preview item
  ---
  duration_ms: 1.552334
  ...
# Subtest: the review preview row previews the entry it will write
ok 2178 - the review preview row previews the entry it will write
  ---
  duration_ms: 4.289938
  ...
# Subtest: the review footer flips between Skip optional logs and Apply schedule as the Reason changes
ok 2179 - the review footer flips between Skip optional logs and Apply schedule as the Reason changes
  ---
  duration_ms: 1.29395
  ...
# Subtest: closing the picker during the review clears pending schedule state and writes nothing
ok 2180 - closing the picker during the review clears pending schedule state and writes nothing
  ---
  duration_ms: 1.344065
  ...
# Subtest: scheduling Work Log eligibility requires Pending or Next \#task lines
ok 2181 - scheduling Work Log eligibility requires Pending or Next \#task lines
  ---
  duration_ms: 1.204689
  ...
# Subtest: single Pending explicit date opens one review and writes both logs
ok 2182 - single Pending explicit date opens one review and writes both logs
  ---
  duration_ms: 19.49239
  ...
# Subtest: single Next blank and whitespace summaries schedule without a Work Log
ok 2183 - single Next blank and whitespace summaries schedule without a Work Log
  ---
  duration_ms: 4.775616
  ...
# Subtest: Escape at the review writes nothing, with or without typed text
ok 2184 - Escape at the review writes nothing, with or without typed text
  ---
  duration_ms: 5.478469
  ...
# Subtest: Ready and Blocked explicit dates review the Reason with no Work summary field
ok 2185 - Ready and Blocked explicit dates review the Reason with no Work summary field
  ---
  duration_ms: 3.509709
  ...
# Subtest: future scheduling on Pending marks Blocked but still writes the Work Log
ok 2186 - future scheduling on Pending marks Blocked but still writes the Work Log
  ---
  duration_ms: 4.829649
  ...
# Subtest: today date on Pending still offers the Work Log
ok 2187 - today date on Pending still offers the Work Log
  ---
  duration_ms: 3.052337
  ...
# Subtest: priority pick on Pending freezes its roll and offers the Work Log
ok 2188 - priority pick on Pending freezes its roll and offers the Work Log
  ---
  duration_ms: 4.209075
  ...
# Subtest: counted mixed statuses share one summary only on Pending and Next
ok 2189 - counted mixed statuses share one summary only on Pending and Next
  ---
  duration_ms: 5.908569
  ...
# Subtest: counted planner composes Schedule and Work Logs bottom-up above later targets
ok 2190 - counted planner composes Schedule and Work Logs bottom-up above later targets
  ---
  duration_ms: 0.876934
  ...
# Subtest: counted planner writes a Work Log even when the date is unchanged
ok 2191 - counted planner writes a Work Log even when the date is unchanged
  ---
  duration_ms: 0.314842
  ...
# Subtest: scheduling Work Log ownership keeps nested logs and CRLF endings
ok 2192 - scheduling Work Log ownership keeps nested logs and CRLF endings
  ---
  duration_ms: 0.844863
  ...
# Subtest: scheduling Work Log warns on :: and preserves Markdown
ok 2193 - scheduling Work Log warns on :: and preserves Markdown
  ---
  duration_ms: 1.630533
  ...
# Subtest: stale task while reviewing refuses with no scheduling or log writes
ok 2194 - stale task while reviewing refuses with no scheduling or log writes
  ---
  duration_ms: 1.15763
  ...
# Subtest: scheduling prompts never leak into lane or cancel stages
ok 2195 - scheduling prompts never leak into lane or cancel stages
  ---
  duration_ms: 2.40445
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: Pomodoro-marked links are not managed dependency bullets
ok 2196 - Pomodoro-marked links are not managed dependency bullets
  ---
  duration_ms: 1.364355
  ...
# Subtest: deleting inline scheduled metadata recovers Blocked targets by snapshot rank
ok 2197 - deleting inline scheduled metadata recovers Blocked targets by snapshot rank
  ---
  duration_ms: 3.530149
  ...
# Subtest: counted future scheduling blocks only supported open inline task statuses
ok 2198 - counted future scheduling blocks only supported open inline task statuses
  ---
  duration_ms: 1.670038
  ...
# Subtest: counted property planning rejects any stale source with no partial result
ok 2199 - counted property planning rejects any stale source with no partial result
  ---
  duration_ms: 0.270767
  ...
# Subtest: counted project scheduling writes the ^prj inline date and blocks tagged residents
ok 2200 - counted project scheduling writes the ^prj inline date and blocks tagged residents
  ---
  duration_ms: 1.75485
  ...
# Subtest: moving a project schedule earlier replaces only exact old-date copies
ok 2201 - moving a project schedule earlier replaces only exact old-date copies
  ---
  duration_ms: 0.384093
  ...
# Subtest: future project schedules block every open resident and consume review status
ok 2202 - future project schedules block every open resident and consume review status
  ---
  duration_ms: 0.59194
  ...
# Subtest: due project dates recover residents through the gate and write unblocked markers
ok 2203 - due project dates recover residents through the gate and write unblocked markers
  ---
  duration_ms: 0.557263
  ...
# Subtest: schedule deletion removes only exact project-date copies and recovers residents
ok 2204 - schedule deletion removes only exact project-date copies and recovers residents
  ---
  duration_ms: 0.86427
  ...
# Subtest: dependency lines render one canonical Depends-On line per parent
ok 2205 - dependency lines render one canonical Depends-On line per parent
  ---
  duration_ms: 0.639631
  ...
# Subtest: dependency IDs encode root and nested Markdown paths deterministically
ok 2206 - dependency IDs encode root and nested Markdown paths deterministically
  ---
  duration_ms: 0.873988
  ...
# Subtest: prompted block IDs truthfully replace legacy id fields
ok 2207 - prompted block IDs truthfully replace legacy id fields
  ---
  duration_ms: 0.150748
  ...
# Subtest: dependency navigation identity includes note path and folds legacy children
ok 2208 - dependency navigation identity includes note path and folds legacy children
  ---
  duration_ms: 0.84887
  ...
# Subtest: retired dependency bullets are excluded from single and counted toggles
ok 2209 - retired dependency bullets are excluded from single and counted toggles
  ---
  duration_ms: 1.204559
  ...
# Subtest: dependsOn replacement accepts spaces around field name and separator
ok 2210 - dependsOn replacement accepts spaces around field name and separator
  ---
  duration_ms: 0.288701
  ...
# Subtest: task status helpers keep Blocked open but rankless
ok 2211 - task status helpers keep Blocked open but rankless
  ---
  duration_ms: 0.291637
  ...
# Subtest: a due project date with only closed Depends-On history strips the tag
ok 2212 - a due project date with only closed Depends-On history strips the tag
  ---
  duration_ms: 0.753859
  ...
# Subtest: Ctrl+D with only closed Depends-On history strips the tag
ok 2213 - Ctrl+D with only closed Depends-On history strips the tag
  ---
  duration_ms: 0.365999
  ...
# Subtest: Ctrl+D with an open Depends-On link remaining keeps the tag
ok 2214 - Ctrl+D with an open Depends-On link remaining keeps the tag
  ---
  duration_ms: 0.296787
  ...
# Subtest: counted ^prj schedule sessions write [unblocked::] when the writer is passed
ok 2215 - counted ^prj schedule sessions write [unblocked::] when the writer is passed
  ---
  duration_ms: 0.463815
  ...
# Subtest: a due project date keeps the tag while ^prj holds Depends-On links
ok 2216 - a due project date keeps the tag while ^prj holds Depends-On links
  ---
  duration_ms: 0.297247
  ...
# Subtest: a due project date strips the tag while a resident with its own reason stays Blocked
ok 2217 - a due project date strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.26186
  ...
# Subtest: Ctrl+D strips the tag while a resident with its own reason stays Blocked
ok 2218 - Ctrl+D strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.329348
  ...
# Subtest: counted scheduled deletes recover with [unblocked::] when the writer is passed
ok 2219 - counted scheduled deletes recover with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.210723
  ...
# Subtest: section-header navigation moves normally and cycles at boundaries
ok 2220 - section-header navigation moves normally and cycles at boundaries
  ---
  duration_ms: 1.981253
  ...
# Subtest: section-header navigation wraps from beyond document boundaries
ok 2221 - section-header navigation wraps from beyond document boundaries
  ---
  duration_ms: 0.190023
  ...
# Subtest: section-header navigation handles single-header and no-header notes
ok 2222 - section-header navigation handles single-header and no-header notes
  ---
  duration_ms: 0.21463
  ...
# Subtest: open-task navigation scan includes Ready In Progress and Next and excludes Blocked
ok 2223 - open-task navigation scan includes Ready In Progress and Next and excludes Blocked
  ---
  duration_ms: 0.53991
  ...
# Subtest: open-task navigation keeps existing Pomodoro ledger targets
ok 2224 - open-task navigation keeps existing Pomodoro ledger targets
  ---
  duration_ms: 0.570108
  ...
# Subtest: next and previous jumps skip Blocked tasks and wrap to an allowed task
ok 2225 - next and previous jumps skip Blocked tasks and wrap to an allowed task
  ---
  duration_ms: 0.318828
  ...
# Subtest: blocked-only notes and a sole current allowed task have no jump target
ok 2226 - blocked-only notes and a sole current allowed task have no jump target
  ---
  duration_ms: 0.158944
  ...
# Subtest: counted open-task jumps select the Nth eligible target and wrap modulo the list
ok 2227 - counted open-task jumps select the Nth eligible target and wrap modulo the list
  ---
  duration_ms: 0.278431
  ...
# Subtest: counted open-task jumps keep sole-target and invalid-repeat behavior
ok 2228 - counted open-task jumps keep sole-target and invalid-repeat behavior
  ---
  duration_ms: 0.432476
  ...
# Subtest: tab pin Vim action registers once and toggles only the active leaf once
ok 2229 - tab pin Vim action registers once and toggles only the active leaf once
  ---
  duration_ms: 2.342753
  ...
# Subtest: tab pin toggle fails safely without a supported active leaf
ok 2230 - tab pin toggle fails safely without a supported active leaf
  ---
  duration_ms: 0.169213
  ...
# Subtest: close tabs left preserves pinned sibling tabs and refocuses active tab
ok 2231 - close tabs left preserves pinned sibling tabs and refocuses active tab
  ---
  duration_ms: 0.678355
  ...
# Subtest: close tabs right preserves pinned siblings and ignores the left side
ok 2232 - close tabs right preserves pinned siblings and ignores the left side
  ---
  duration_ms: 0.272641
  ...
# Subtest: close other tabs preserves pinned siblings on both sides
ok 2233 - close other tabs preserves pinned siblings on both sides
  ---
  duration_ms: 0.270957
  ...
# Subtest: close sibling tabs is a silent no-op when the scoped range is all pinned
ok 2234 - close sibling tabs is a silent no-op when the scoped range is all pinned
  ---
  duration_ms: 0.231823
  ...
# Subtest: close sibling tabs honors every pinned leaf representation
ok 2235 - close sibling tabs honors every pinned leaf representation
  ---
  duration_ms: 0.311414
  ...
# Subtest: close sibling tabs treats throwing view state as unpinned
ok 2236 - close sibling tabs treats throwing view state as unpinned
  ---
  duration_ms: 0.383682
  ...
# Subtest: tab pin Vim registration retries after adapter availability
ok 2237 - tab pin Vim registration retries after adapter availability
  ---
  duration_ms: 0.782604
  ...
# Subtest: isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
ok 2238 - isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
  ---
  duration_ms: 4.046535
  ...
# Subtest: isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
ok 2239 - isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
  ---
  duration_ms: 0.725796
  ...
# Subtest: isPomodoroTaskLinkLine refuses Depends-On lines and prose links
ok 2240 - isPomodoroTaskLinkLine refuses Depends-On lines and prose links
  ---
  duration_ms: 0.213227
  ...
# Subtest: decideTaskLinkLaneMode starts when any target is Next
ok 2241 - decideTaskLinkLaneMode starts when any target is Next
  ---
  duration_ms: 0.176988
  ...
# Subtest: taskLinkLaneRefusalFor renders every D5 refusal
ok 2242 - taskLinkLaneRefusalFor renders every D5 refusal
  ---
  duration_ms: 0.147141
  ...
# Subtest: planTaskLinkLaneBatch starts Next targets and leaves the rest alone
ok 2243 - planTaskLinkLaneBatch starts Next targets and leaves the rest alone
  ---
  duration_ms: 1.178119
  ...
# Subtest: planTaskLinkLaneBatch pauses with one shared Work Log entry
ok 2244 - planTaskLinkLaneBatch pauses with one shared Work Log entry
  ---
  duration_ms: 0.742988
  ...
# Subtest: planTaskLinkLaneBatch applies the freshness stamp last
ok 2245 - planTaskLinkLaneBatch applies the freshness stamp last
  ---
  duration_ms: 0.353064
  ...
# Subtest: planTaskLinkLaneBatch dedupes lines and refuses stale preimages
ok 2246 - planTaskLinkLaneBatch dedupes lines and refuses stale preimages
  ---
  duration_ms: 0.525093
  ...
# Subtest: buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
ok 2247 - buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
  ---
  duration_ms: 0.720746
  ...
# Subtest: taskLinkLanePromptState drives the Move to Next prompt
ok 2248 - taskLinkLanePromptState drives the Move to Next prompt
  ---
  duration_ms: 0.25164
  ...
# Subtest: TaskLinkLanePromptModal submits, previews live, and cancels silently
ok 2249 - TaskLinkLanePromptModal submits, previews live, and cancels silently
  ---
  duration_ms: 1.40349
  ...
# Subtest: TaskLinkLanePromptModal renders the batch context card
ok 2250 - TaskLinkLanePromptModal renders the batch context card
  ---
  duration_ms: 0.35623
  ...
# Subtest: findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
ok 2251 - findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
  ---
  duration_ms: 0.285184
  ...
# Subtest: L1: toggle starts a Next link, stamps, hints, and notices
ok 2252 - L1: toggle starts a Next link, stamps, hints, and notices
  ---
  duration_ms: 3.283829
  ...
# Subtest: L2/L3: toggle pauses through the prompt, logging one shared entry
ok 2253 - L2/L3: toggle pauses through the prompt, logging one shared entry
  ---
  duration_ms: 11.23181
  ...
# Subtest: L4: cancelling the prompt writes nothing and shows no Notice
ok 2254 - L4: cancelling the prompt writes nothing and shows no Notice
  ---
  duration_ms: 0.911159
  ...
# Subtest: L5: both directions run the same toggle twice for a round trip
ok 2255 - L5: both directions run the same toggle twice for a round trip
  ---
  duration_ms: 1.387709
  ...
# Subtest: L6: Ready, Blocked, done, and cancelled targets are refused
ok 2256 - L6: Ready, Blocked, done, and cancelled targets are refused
  ---
  duration_ms: 1.591308
  ...
# Subtest: L6: missing targets keep the existing resolver error
ok 2257 - L6: missing targets keep the existing resolver error
  ---
  duration_ms: 0.23569
  ...
# Subtest: L7: a counted start flips every Next sibling and leaves In Progress alone
ok 2258 - L7: a counted start flips every Next sibling and leaves In Progress alone
  ---
  duration_ms: 0.505105
  ...
# Subtest: L8: a counted pause prompts once and skips Blocked with a count
ok 2259 - L8: a counted pause prompts once and skips Blocked with a count
  ---
  duration_ms: 1.474195
  ...
# Subtest: L9: an over-long count clamps at the entry end without error
ok 2260 - L9: an over-long count clamps at the entry end without error
  ---
  duration_ms: 0.627678
  ...
# Subtest: L10: a closed-entry history line toggles the task and keeps the line
ok 2261 - L10: a closed-entry history line toggles the task and keeps the line
  ---
  duration_ms: 0.317536
  ...
# Subtest: L11: a target edited while the prompt is open refuses stale
ok 2262 - L11: a target edited while the prompt is open refuses stale
  ---
  duration_ms: 1.732076
  ...
# Subtest: L12: an embedded Pomodoro link takes the two-state toggle
ok 2263 - L12: an embedded Pomodoro link takes the two-state toggle
  ---
  duration_ms: 0.525964
  ...
# Subtest: L14: the same task linked twice in a batch is written once
ok 2264 - L14: the same task linked twice in a batch is written once
  ---
  duration_ms: 1.348704
  ...
# Subtest: L15: a second toggle while one is in flight is swallowed as busy
ok 2265 - L15: a second toggle while one is in flight is swallowed as busy
  ---
  duration_ms: 0.677925
  ...
# Subtest: toggle on a non-link line refuses without writing
ok 2266 - toggle on a non-link line refuses without writing
  ---
  duration_ms: 0.237263
  ...
# Subtest: api.taskLinkLane is a frozen v1 namespace that never throws
ok 2267 - api.taskLinkLane is a frozen v1 namespace that never throws
  ---
  duration_ms: 0.884378
  ...
# Subtest: the progressMarks hint is a no-op without the ledger-tools api
ok 2268 - the progressMarks hint is a no-op without the ledger-tools api
  ---
  duration_ms: 0.295564
  ...
# Subtest: task move records one Vim jump and round-trips without extra writes
ok 2269 - task move records one Vim jump and round-trips without extra writes
  ---
  duration_ms: 9.980763
  ...
# Subtest: counted task move records a single jump to the first moved task
ok 2270 - counted task move records a single jump to the first moved task
  ---
  duration_ms: 1.490104
  ...
# Subtest: deferred task landing re-anchors and records the resolved cursor once
ok 2271 - deferred task landing re-anchors and records the resolved cursor once
  ---
  duration_ms: 4.651972
  ...
# Subtest: failed task move preserves seeded history including the forward branch
ok 2272 - failed task move preserves seeded history including the forward branch
  ---
  duration_ms: 0.554368
  ...
# Subtest: post-commit open failure keeps the move committed with no jump
ok 2273 - post-commit open failure keeps the move committed with no jump
  ---
  duration_ms: 0.931979
  ...
# Subtest: a newer move supersedes a pending landing without stale placement
ok 2274 - a newer move supersedes a pending landing without stale placement
  ---
  duration_ms: 10.360256
  ...
# Subtest: shared destination helper without a move context records no jump
ok 2275 - shared destination helper without a move context records no jump
  ---
  duration_ms: 0.506608
  ...
# Subtest: task moves carry the Depends-On line and repath stranded same-note links
ok 2276 - task moves carry the Depends-On line and repath stranded same-note links
  ---
  duration_ms: 6.636599
  ...
# Subtest: task moves keep pathless links when the target moves along
ok 2277 - task moves keep pathless links when the target moves along
  ---
  duration_ms: 1.05807
  ...
# Subtest: counted task moves discover movable tasks without wrapping or examples
ok 2278 - counted task moves discover movable tasks without wrapping or examples
  ---
  duration_ms: 1.087036
  ...
# Subtest: task move ranges preserve quoted subtrees and collapse overlapping selections
ok 2279 - task move ranges preserve quoted subtrees and collapse overlapping selections
  ---
  duration_ms: 0.60279
  ...
# Subtest: task move removal handles disjoint ranges, blank seams, and CRLF
ok 2280 - task move removal handles disjoint ranges, blank seams, and CRLF
  ---
  duration_ms: 0.390816
  ...
# Subtest: task move destinations include areas and only open projects
ok 2281 - task move destinations include areas and only open projects
  ---
  duration_ms: 0.694946
  ...
# Subtest: moves into a blocked project leave closed tagged lines alone
ok 2282 - moves into a blocked project leave closed tagged lines alone
  ---
  duration_ms: 2.414979
  ...
# Subtest: moves into a blocked project promote open prerequisites to the moved lane
ok 2283 - moves into a blocked project promote open prerequisites to the moved lane
  ---
  duration_ms: 2.221771
  ...
# Subtest: task move insertion preserves exact task and section spacing
ok 2284 - task move insertion preserves exact task and section spacing
  ---
  duration_ms: 3.25864
  ...
# Subtest: task move planning migrates identities and links across every affected note
ok 2285 - task move planning migrates identities and links across every affected note
  ---
  duration_ms: 5.334804
  ...
# Subtest: task move planning exposes a destination anchor for area destinations and counted moves
ok 2286 - task move planning exposes a destination anchor for area destinations and counted moves
  ---
  duration_ms: 0.998797
  ...
# Subtest: task move into a blocked project tags the moved task and consumes today's live Pomodoro link
ok 2287 - task move into a blocked project tags the moved task and consumes today's live Pomodoro link
  ---
  duration_ms: 4.060993
  ...
# Subtest: task move out of a blocked project recovers through the shared gate and writes the unblocked mark
ok 2288 - task move out of a blocked project recovers through the shared gate and writes the unblocked mark
  ---
  duration_ms: 4.056453
  ...
# Subtest: move promotion walks through a ^prj target without raising it
ok 2289 - move promotion walks through a ^prj target without raising it
  ---
  duration_ms: 2.14816
  ...
# Subtest: move promotion walks through a [?] ^prj to its open prerequisite
ok 2290 - move promotion walks through a [?] ^prj to its open prerequisite
  ---
  duration_ms: 0.947079
  ...
# Subtest: move promotion uses each open task's own lane, not the strongest moved lane
ok 2291 - move promotion uses each open task's own lane, not the strongest moved lane
  ---
  duration_ms: 1.196024
  ...
# Subtest: move promotion skips Depends-On lines of closed tasks
ok 2292 - move promotion skips Depends-On lines of closed tasks
  ---
  duration_ms: 0.75966
  ...
# Subtest: task move planning rejects destination collisions and malformed identities
ok 2293 - task move planning rejects destination collisions and malformed identities
  ---
  duration_ms: 0.597721
  ...
# Subtest: resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
ok 2294 - resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
  ---
  duration_ms: 0.634101
  ...
# Subtest: focusTaskMoveDestination opens the destination file and anchors the cursor
ok 2295 - focusTaskMoveDestination opens the destination file and anchors the cursor
  ---
  duration_ms: 1.056396
  ...
# Subtest: focusTaskMoveDestination returns false without moving the cursor when the open fails
ok 2296 - focusTaskMoveDestination returns false without moving the cursor when the open fails
  ---
  duration_ms: 0.232334
  ...
# Subtest: focusTaskMoveDestination re-anchors by block ID when the destination content drifted
ok 2297 - focusTaskMoveDestination re-anchors by block ID when the destination content drifted
  ---
  duration_ms: 0.229518
  ...
# Subtest: physical task move chord declines auto-repeat and consumes Vim normal input once
ok 2298 - physical task move chord declines auto-repeat and consumes Vim normal input once
  ---
  duration_ms: 0.810387
  ...
# Subtest: counted task move dispatch keeps its count through cold async destinations
ok 2299 - counted task move dispatch keeps its count through cold async destinations
  ---
  duration_ms: 14.554312
  ...
# Subtest: counted task move dispatch with warm async destinations opens one counted picker
ok 2300 - counted task move dispatch with warm async destinations opens one counted picker
  ---
  duration_ms: 5.075159
  ...
# Subtest: bare task move command ignores stale Vim count outside normal mode
ok 2301 - bare task move command ignores stale Vim count outside normal mode
  ---
  duration_ms: 0.725125
  ...
# Subtest: bare task move command opens one uncounted target in Vim normal mode
ok 2302 - bare task move command opens one uncounted target in Vim normal mode
  ---
  duration_ms: 0.436534
  ...
# Subtest: already handled task move event leaves pending Vim state alone
ok 2303 - already handled task move event leaves pending Vim state alone
  ---
  duration_ms: 0.189702
  ...
# Subtest: counted task move command dispatch counts Pomodoro sub-bullets once
ok 2304 - counted task move command dispatch counts Pomodoro sub-bullets once
  ---
  duration_ms: 2.340678
  ...
# Subtest: physical transclusion toggle owns bare and counted Vim normal input
ok 2305 - physical transclusion toggle owns bare and counted Vim normal input
  ---
  duration_ms: 1.367089
  ...
# Subtest: runtime task move writes destination before source and rolls back source failures
ok 2306 - runtime task move writes destination before source and rolls back source failures
  ---
  duration_ms: 2.264683
  ...
# Subtest: runtime task move groups open-editor source and destination changes
ok 2307 - runtime task move groups open-editor source and destination changes
  ---
  duration_ms: 1.513529
  ...
# Subtest: runtime task move guards destination, auxiliary, and rollback failures
ok 2308 - runtime task move guards destination, auxiliary, and rollback failures
  ---
  duration_ms: 2.973817
  ...
# Subtest: task move insertion separates the section's first task from preamble and placeholders
ok 2309 - task move insertion separates the section's first task from preamble and placeholders
  ---
  duration_ms: 0.36672
  ...
# Subtest: task move insertion keeps populated sections compact and second moves stable
ok 2310 - task move insertion keeps populated sections compact and second moves stable
  ---
  duration_ms: 0.199531
  ...
# Subtest: task move planning separates a counted move into a count-only section
ok 2311 - task move planning separates a counted move into a count-only section
  ---
  duration_ms: 0.39257
  ...
# Subtest: runtime counted move into a count-only section focuses the first moved task
ok 2312 - runtime counted move into a count-only section focuses the first moved task
  ---
  duration_ms: 1.388201
  ...
# Subtest: absent local key with folder template writes the trigger and one notice
ok 2313 - absent local key with folder template writes the trigger and one notice
  ---
  duration_ms: 1.669086
  ...
# Subtest: existing local object keeps other keys and only adds the trigger
ok 2314 - existing local object keeps other keys and only adds the trigger
  ---
  duration_ms: 0.262431
  ...
# Subtest: stored true is already-enabled with no write and no notice
ok 2315 - stored true is already-enabled with no write and no notice
  ---
  duration_ms: 0.237303
  ...
# Subtest: stored false is device-opt-out with no write and no notice
ok 2316 - stored false is device-opt-out with no write and no notice
  ---
  duration_ms: 0.152361
  ...
# Subtest: mode none and blank folder templates skip as no-creation-templates
ok 2317 - mode none and blank folder templates skip as no-creation-templates
  ---
  duration_ms: 0.249877
  ...
# Subtest: regex mode with a non-empty file template enables
ok 2318 - regex mode with a non-empty file template enables
  ---
  duration_ms: 0.180675
  ...
# Subtest: legacy settings without a mode key skip as legacy-templater
ok 2319 - legacy settings without a mode key skip as legacy-templater
  ---
  duration_ms: 0.179903
  ...
# Subtest: missing Templater plugin or settings skip as no-templater without throwing
ok 2320 - missing Templater plugin or settings skip as no-templater without throwing
  ---
  duration_ms: 0.259285
  ...
# Subtest: missing loadLocalStorage or saveLocalStorage returns without throwing
ok 2321 - missing loadLocalStorage or saveLocalStorage returns without throwing
  ---
  duration_ms: 0.330702
  ...
# Subtest: string or array stored local values skip as unknown-local-shape
ok 2322 - string or array stored local values skip as unknown-local-shape
  ---
  duration_ms: 0.407387
  ...
# Subtest: saveLocalStorage throw shows one failure notice and does not escape
ok 2323 - saveLocalStorage throw shows one failure notice and does not escape
  ---
  duration_ms: 0.2146
  ...
# Subtest: planTemplaterLocalTrigger covers helper cases and never adds extra keys
ok 2324 - planTemplaterLocalTrigger covers helper cases and never adds extra keys
  ---
  duration_ms: 0.192257
  ...
# Subtest: unblocked model returns null when there is nothing to show
ok 2325 - unblocked model returns null when there is nothing to show
  ---
  duration_ms: 1.392639
  ...
# Subtest: unblocked card renders a single linked row with receipt and chips
ok 2326 - unblocked card renders a single linked row with receipt and chips
  ---
  duration_ms: 1.619572
  ...
# Subtest: unblocked card renders several linked rows with one entry
ok 2327 - unblocked card renders several linked rows with one entry
  ---
  duration_ms: 0.316785
  ...
# Subtest: unblocked card renders a created continuation with next up
ok 2328 - unblocked card renders a created continuation with next up
  ---
  duration_ms: 0.381809
  ...
# Subtest: unblocked card renders recovered-only and still-blocked rows
ok 2329 - unblocked card renders recovered-only and still-blocked rows
  ---
  duration_ms: 0.709565
  ...
# Subtest: current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
ok 2330 - current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
  ---
  duration_ms: 0.898826
  ...
# Subtest: project pull-in rows label empty projects and preserve project blocking reasons
ok 2331 - project pull-in rows label empty projects and preserve project blocking reasons
  ---
  duration_ms: 1.033393
  ...
# Subtest: unblocked card caps visible rows with +N more
ok 2332 - unblocked card caps visible rows with +N more
  ---
  duration_ms: 0.341211
  ...
# Subtest: unblocked card renders the breaker variant
ok 2333 - unblocked card renders the breaker variant
  ---
  duration_ms: 0.499132
  ...
# Subtest: unblocked card renders the failure variant
ok 2334 - unblocked card renders the failure variant
  ---
  duration_ms: 0.503741
  ...
# Subtest: unblocked rows open their task without dismissing the notice
ok 2335 - unblocked rows open their task without dismissing the notice
  ---
  duration_ms: 1.160365
  ...
# Subtest: unblocked row without a block id opens the note path
ok 2336 - unblocked row without a block id opens the note path
  ---
  duration_ms: 0.274464
  ...
# Subtest: unblocked card omits the plan chip when daily content is null
ok 2337 - unblocked card omits the plan chip when daily content is null
  ---
  duration_ms: 0.232294
  ...
# Subtest: unblocked notice shows one card with duration through showNotice
ok 2338 - unblocked notice shows one card with duration through showNotice
  ---
  duration_ms: 0.359356
  ...
# Subtest: unblocked notice falls back to plain text without a DOM
ok 2339 - unblocked notice falls back to plain text without a DOM
  ---
  duration_ms: 0.160145
  ...
# Subtest: unblocked text truncates to 48 characters with an ellipsis
ok 2340 - unblocked text truncates to 48 characters with an ellipsis
  ---
  duration_ms: 0.154515
  ...
# Subtest: nav api exposes additive notice v1 and keeps version 3
ok 2341 - nav api exposes additive notice v1 and keeps version 3
  ---
  duration_ms: 0.408349
  ...
# Subtest: unblocked stylesheet scopes notice overrides and uses task tokens
ok 2342 - unblocked stylesheet scopes notice overrides and uses task tokens
  ---
  duration_ms: 0.562033
  ...
# Subtest: physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
ok 2343 - physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
  ---
  duration_ms: 2.262079
  ...
# Subtest: open-task command ids omit repeat so the shared route resolves the pending Vim count
ok 2344 - open-task command ids omit repeat so the shared route resolves the pending Vim count
  ---
  duration_ms: 1.263833
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
ok 2345 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
  ---
  duration_ms: 4.338181
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
ok 2346 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
  ---
  duration_ms: 0.599224
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
ok 2347 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
  ---
  duration_ms: 1.1003
  ...
# Subtest: dispatch guard applies a command-route Vim count when the capture route fires second
ok 2348 - dispatch guard applies a command-route Vim count when the capture route fires second
  ---
  duration_ms: 1.005659
  ...
# Subtest: dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
ok 2349 - dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
  ---
  duration_ms: 0.735383
  ...
# Subtest: command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
ok 2350 - command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
  ---
  duration_ms: 0.632017
  ...
# Subtest: command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
ok 2351 - command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
  ---
  duration_ms: 2.198186
  ...
# Subtest: command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
ok 2352 - command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
  ---
  duration_ms: 0.876613
  ...
# Subtest: explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
ok 2353 - explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
  ---
  duration_ms: 0.572213
  ...
# Subtest: getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
ok 2354 - getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
  ---
  duration_ms: 0.199821
  ...
# Subtest: physical counted property chord consumes only explicit normal-mode Vim counts
ok 2355 - physical counted property chord consumes only explicit normal-mode Vim counts
  ---
  duration_ms: 0.601619
  ...
# Subtest: physical counted relation and dependency chords route or refuse by direction
ok 2356 - physical counted relation and dependency chords route or refuse by direction
  ---
  duration_ms: 1.993085
  ...
# Subtest: onload registers the palette command without a default hotkey
ok 2357 - onload registers the palette command without a default hotkey
  ---
  duration_ms: 1.743949
  ...
# Subtest: an embed and a plain image link open the resolved vault resource
ok 2358 - an embed and a plain image link open the resolved vault resource
  ---
  duration_ms: 3.331641
  ...
# Subtest: no image, a missing image, and Reading view show notices without opening
ok 2359 - no image, a missing image, and Reading view show notices without opening
  ---
  duration_ms: 0.544509
  ...
# Subtest: a second command invocation is ignored while the viewer is open
ok 2360 - a second command invocation is ignored while the viewer is open
  ---
  duration_ms: 0.378503
  ...
# Subtest: closing restores focus and leaves an unchanged selection and scroll alone
ok 2361 - closing restores focus and leaves an unchanged selection and scroll alone
  ---
  duration_ms: 0.42948
  ...
# Subtest: closing restores moved selection and scroll only while the source view is active
ok 2362 - closing restores moved selection and scroll only while the source view is active
  ---
  duration_ms: 0.824785
  ...
# Subtest: unload closes the active viewer without restoring editor focus
ok 2363 - unload closes the active viewer without restoring editor focus
  ---
  duration_ms: 0.48185
  ...
# Subtest: parser finds vault embed with size hint
ok 2364 - parser finds vault embed with size hint
  ---
  duration_ms: 1.587029
  ...
# Subtest: parser finds plain image wikilink and blockquoted embed
ok 2365 - parser finds plain image wikilink and blockquoted embed
  ---
  duration_ms: 0.260117
  ...
# Subtest: parser ignores callout bracket and finds the embed
ok 2366 - parser ignores callout bracket and finds the embed
  ---
  duration_ms: 0.34081
  ...
# Subtest: parser ignores image links inside single and double backticks
ok 2367 - parser ignores image links inside single and double backticks
  ---
  duration_ms: 0.644981
  ...
# Subtest: non-image wiki targets are recognized but not candidates
ok 2368 - non-image wiki targets are recognized but not candidates
  ---
  duration_ms: 0.23537
  ...
# Subtest: parser finds two image refs and lines with no refs
ok 2369 - parser finds two image refs and lines with no refs
  ---
  duration_ms: 0.223246
  ...
# Subtest: parser handles Markdown angle, title, and balanced parens
ok 2370 - parser handles Markdown angle, title, and balanced parens
  ---
  duration_ms: 0.363885
  ...
# Subtest: picker uses containing, next, then previous rule
ok 2371 - picker uses containing, next, then previous rule
  ---
  duration_ms: 0.347494
  ...
# Subtest: resolution records sourcePath and resolves duplicate basenames
ok 2372 - resolution records sourcePath and resolves duplicate basenames
  ---
  duration_ms: 0.91655
  ...
# Subtest: resolution handles relative, unicode, and space names
ok 2373 - resolution handles relative, unicode, and space names
  ---
  duration_ms: 0.494133
  ...
# Subtest: missing file, non-image cursor, and fenced lines show exact notices
ok 2374 - missing file, non-image cursor, and fenced lines show exact notices
  ---
  duration_ms: 0.295824
  ...
# Subtest: vault resolution calls getResourcePath with the resolved file
ok 2375 - vault resolution calls getResourcePath with the resolved file
  ---
  duration_ms: 0.296496
  ...
# Subtest: http embed passes through and non-image urls are not candidates
ok 2376 - http embed passes through and non-image urls are not candidates
  ---
  duration_ms: 0.359516
  ...
# Subtest: remote URLs keep original bytes while titles decode once
ok 2377 - remote URLs keep original bytes while titles decode once
  ---
  duration_ms: 0.493833
  ...
# Subtest: escaped Markdown parentheses resolve to the unescaped vault file
ok 2378 - escaped Markdown parentheses resolve to the unescaped vault file
  ---
  duration_ms: 0.204651
  ...
# Subtest: vault percent escapes decode exactly once
ok 2379 - vault percent escapes decode exactly once
  ---
  duration_ms: 0.187999
  ...
# Subtest: extensionless http(s) needs Markdown image syntax
ok 2380 - extensionless http(s) needs Markdown image syntax
  ---
  duration_ms: 0.20964
  ...
# Subtest: fit never exceeds 1 and respects padding for landscape, portrait, and tiny images
ok 2381 - fit never exceeds 1 and respects padding for landscape, portrait, and tiny images
  ---
  duration_ms: 1.213156
  ...
# Subtest: min and max bounds follow fit, 1:1, and the max factor
ok 2382 - min and max bounds follow fit, 1:1, and the max factor
  ---
  duration_ms: 0.214449
  ...
# Subtest: stepping clamps at both bounds
ok 2383 - stepping clamps at both bounds
  ---
  duration_ms: 0.407468
  ...
# Subtest: zoom-at-point keeps the point fixed
ok 2384 - zoom-at-point keeps the point fixed
  ---
  duration_ms: 0.14645
  ...
# Subtest: clamp centres small axes and limits large ones
ok 2385 - clamp centres small axes and limits large ones
  ---
  duration_ms: 0.255177
  ...
# Subtest: key Escape → close
ok 2386 - key Escape → close
  ---
  duration_ms: 0.629191
  ...
# Subtest: key q → close
ok 2387 - key q → close
  ---
  duration_ms: 0.16222
  ...
# Subtest: key Q → close
ok 2388 - key Q → close
  ---
  duration_ms: 0.098308
  ...
# Subtest: key Ctrl+[ → close
ok 2389 - key Ctrl+[ → close
  ---
  duration_ms: 0.315583
  ...
# Subtest: key Z → close
ok 2390 - key Z → close
  ---
  duration_ms: 0.355218
  ...
# Subtest: key + → zoomIn
ok 2391 - key + → zoomIn
  ---
  duration_ms: 0.143093
  ...
# Subtest: key = → zoomIn
ok 2392 - key = → zoomIn
  ---
  duration_ms: 0.081616
  ...
# Subtest: key Shift+= → zoomIn
ok 2393 - key Shift+= → zoomIn
  ---
  duration_ms: 0.075765
  ...
# Subtest: key Shift++ → zoomIn
ok 2394 - key Shift++ → zoomIn
  ---
  duration_ms: 0.121783
  ...
# Subtest: key - → zoomOut
ok 2395 - key - → zoomOut
  ---
  duration_ms: 0.079993
  ...
# Subtest: key 0 → fit
ok 2396 - key 0 → fit
  ---
  duration_ms: 0.117814
  ...
# Subtest: key 1 → actual
ok 2397 - key 1 → actual
  ---
  duration_ms: 0.073059
  ...
# Subtest: key h → pan:left
ok 2398 - key h → pan:left
  ---
  duration_ms: 0.080995
  ...
# Subtest: key j → pan:down
ok 2399 - key j → pan:down
  ---
  duration_ms: 0.081406
  ...
# Subtest: key k → pan:up
ok 2400 - key k → pan:up
  ---
  duration_ms: 0.066998
  ...
# Subtest: key l → pan:right
ok 2401 - key l → pan:right
  ---
  duration_ms: 0.070294
  ...
# Subtest: key Shift+H → pan:left
ok 2402 - key Shift+H → pan:left
  ---
  duration_ms: 0.077638
  ...
# Subtest: key Shift+J → pan:down
ok 2403 - key Shift+J → pan:down
  ---
  duration_ms: 0.061878
  ...
# Subtest: key Shift+K → pan:up
ok 2404 - key Shift+K → pan:up
  ---
  duration_ms: 0.069743
  ...
# Subtest: key Shift+L → pan:right
ok 2405 - key Shift+L → pan:right
  ---
  duration_ms: 0.058341
  ...
# Subtest: key ArrowLeft → pan:left
ok 2406 - key ArrowLeft → pan:left
  ---
  duration_ms: 0.058482
  ...
# Subtest: key ArrowDown → pan:down
ok 2407 - key ArrowDown → pan:down
  ---
  duration_ms: 0.062329
  ...
# Subtest: key ArrowUp → pan:up
ok 2408 - key ArrowUp → pan:up
  ---
  duration_ms: 0.059012
  ...
# Subtest: key ArrowRight → pan:right
ok 2409 - key ArrowRight → pan:right
  ---
  duration_ms: 0.060055
  ...
# Subtest: key Shift+ArrowLeft → pan:left
ok 2410 - key Shift+ArrowLeft → pan:left
  ---
  duration_ms: 0.120871
  ...
# Subtest: key Ctrl+q → ignore
ok 2411 - key Ctrl+q → ignore
  ---
  duration_ms: 0.079432
  ...
# Subtest: key Meta+z → ignore
ok 2412 - key Meta+z → ignore
  ---
  duration_ms: 0.072809
  ...
# Subtest: key Meta+Z → ignore
ok 2413 - key Meta+Z → ignore
  ---
  duration_ms: 0.126381
  ...
# Subtest: key a composing → ignore
ok 2414 - key a composing → ignore
  ---
  duration_ms: 0.067429
  ...
# Subtest: key a keyCode 229 → ignore
ok 2415 - key a keyCode 229 → ignore
  ---
  duration_ms: 0.07333
  ...
# Subtest: key x → ignore
ok 2416 - key x → ignore
  ---
  duration_ms: 0.060405
  ...
# Subtest: keys before arming are ignored
ok 2417 - keys before arming are ignored
  ---
  duration_ms: 0.975131
  ...
# Subtest: Z closes after arming, and a repeated Z does not
ok 2418 - Z closes after arming, and a repeated Z does not
  ---
  duration_ms: 0.492741
  ...
# Subtest: load sets fit state and dimensions
ok 2419 - load sets fit state and dimensions
  ---
  duration_ms: 0.447094
  ...
# Subtest: a load error shows a notice, closes, and calls onClosed once
ok 2420 - a load error shows a notice, closes, and calls onClosed once
  ---
  duration_ms: 0.261339
  ...
# Subtest: Escape closes once, unregisters the scope handler, and aborts the signal
ok 2421 - Escape closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.21511
  ...
# Subtest: q closes once, unregisters the scope handler, and aborts the signal
ok 2422 - q closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.204341
  ...
# Subtest: Q closes once, unregisters the scope handler, and aborts the signal
ok 2423 - Q closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.157852
  ...
# Subtest: Ctrl+[ closes once, unregisters the scope handler, and aborts the signal
ok 2424 - Ctrl+[ closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.172519
  ...
# Subtest: Z closes once, unregisters the scope handler, and aborts the signal
ok 2425 - Z closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.237954
  ...
# Subtest: a stray x key changes nothing
ok 2426 - a stray x key changes nothing
  ---
  duration_ms: 0.236632
  ...
# Subtest: the app's vault stubs throw and are never called
ok 2427 - the app's vault stubs throw and are never called
  ---
  duration_ms: 0.201765
  ...
# Subtest: task-card-gate arms only on open inbox tasks
ok 2428 - task-card-gate arms only on open inbox tasks
  ---
  duration_ms: 3.451859
  ...
# Subtest: task-card-gate header shows the Inbox chip only when armed
ok 2429 - task-card-gate header shows the Inbox chip only when armed
  ---
  duration_ms: 6.405348
  ...
# Subtest: task-card-gate priority: cancel writes nothing
ok 2430 - task-card-gate priority: cancel writes nothing
  ---
  duration_ms: 1.151097
  ...
# Subtest: task-card-gate priority: stay runs today's write
ok 2431 - task-card-gate priority: stay runs today's write
  ---
  duration_ms: 0.253333
  ...
# Subtest: task-card-gate priority: move writes then moves
ok 2432 - task-card-gate priority: move writes then moves
  ---
  duration_ms: 0.575278
  ...
# Subtest: task-card-gate scheduled: cancel writes nothing
ok 2433 - task-card-gate scheduled: cancel writes nothing
  ---
  duration_ms: 0.163863
  ...
# Subtest: task-card-gate scheduled: stay runs today's write
ok 2434 - task-card-gate scheduled: stay runs today's write
  ---
  duration_ms: 0.150007
  ...
# Subtest: task-card-gate scheduled: move writes then moves
ok 2435 - task-card-gate scheduled: move writes then moves
  ---
  duration_ms: 0.173832
  ...
# Subtest: task-card-gate generic-property: cancel writes nothing
ok 2436 - task-card-gate generic-property: cancel writes nothing
  ---
  duration_ms: 0.382119
  ...
# Subtest: task-card-gate generic-property: stay runs today's write
ok 2437 - task-card-gate generic-property: stay runs today's write
  ---
  duration_ms: 0.419801
  ...
# Subtest: task-card-gate generic-property: move writes then moves
ok 2438 - task-card-gate generic-property: move writes then moves
  ---
  duration_ms: 0.306756
  ...
# Subtest: task-card-gate refresh-interval: cancel writes nothing
ok 2439 - task-card-gate refresh-interval: cancel writes nothing
  ---
  duration_ms: 0.174573
  ...
# Subtest: task-card-gate refresh-interval: stay runs today's write
ok 2440 - task-card-gate refresh-interval: stay runs today's write
  ---
  duration_ms: 0.123276
  ...
# Subtest: task-card-gate refresh-interval: move writes then moves
ok 2441 - task-card-gate refresh-interval: move writes then moves
  ---
  duration_ms: 0.152802
  ...
# Subtest: task-card-gate refresh-custom: cancel writes nothing
ok 2442 - task-card-gate refresh-custom: cancel writes nothing
  ---
  duration_ms: 0.100972
  ...
# Subtest: task-card-gate refresh-custom: stay runs today's write
ok 2443 - task-card-gate refresh-custom: stay runs today's write
  ---
  duration_ms: 0.09936
  ...
# Subtest: task-card-gate refresh-custom: move writes then moves
ok 2444 - task-card-gate refresh-custom: move writes then moves
  ---
  duration_ms: 0.34579
  ...
# Subtest: task-card-gate clear-priority: cancel writes nothing
ok 2445 - task-card-gate clear-priority: cancel writes nothing
  ---
  duration_ms: 0.133926
  ...
# Subtest: task-card-gate clear-priority: stay runs today's write
ok 2446 - task-card-gate clear-priority: stay runs today's write
  ---
  duration_ms: 0.114578
  ...
# Subtest: task-card-gate clear-priority: move writes then moves
ok 2447 - task-card-gate clear-priority: move writes then moves
  ---
  duration_ms: 0.138615
  ...
# Subtest: task-card-gate recommended-roll: cancel writes nothing
ok 2448 - task-card-gate recommended-roll: cancel writes nothing
  ---
  duration_ms: 0.093419
  ...
# Subtest: task-card-gate recommended-roll: stay runs today's write
ok 2449 - task-card-gate recommended-roll: stay runs today's write
  ---
  duration_ms: 0.097997
  ...
# Subtest: task-card-gate recommended-roll: move writes then moves
ok 2450 - task-card-gate recommended-roll: move writes then moves
  ---
  duration_ms: 0.130028
  ...
# Subtest: task-card-gate recommended-decay: cancel writes nothing
ok 2451 - task-card-gate recommended-decay: cancel writes nothing
  ---
  duration_ms: 0.096905
  ...
# Subtest: task-card-gate recommended-decay: stay runs today's write
ok 2452 - task-card-gate recommended-decay: stay runs today's write
  ---
  duration_ms: 0.090543
  ...
# Subtest: task-card-gate recommended-decay: move writes then moves
ok 2453 - task-card-gate recommended-decay: move writes then moves
  ---
  duration_ms: 0.117424
  ...
# Subtest: task-card-gate counted-roll: cancel writes nothing
ok 2454 - task-card-gate counted-roll: cancel writes nothing
  ---
  duration_ms: 0.143925
  ...
# Subtest: task-card-gate counted-roll: stay runs today's write
ok 2455 - task-card-gate counted-roll: stay runs today's write
  ---
  duration_ms: 0.101123
  ...
# Subtest: task-card-gate counted-roll: move writes then moves
ok 2456 - task-card-gate counted-roll: move writes then moves
  ---
  duration_ms: 0.20463
  ...
# Subtest: task-card-gate lane-toggle: cancel writes nothing
ok 2457 - task-card-gate lane-toggle: cancel writes nothing
  ---
  duration_ms: 0.100772
  ...
# Subtest: task-card-gate lane-toggle: stay runs today's write
ok 2458 - task-card-gate lane-toggle: stay runs today's write
  ---
  duration_ms: 0.108166
  ...
# Subtest: task-card-gate lane-toggle: move writes then moves
ok 2459 - task-card-gate lane-toggle: move writes then moves
  ---
  duration_ms: 0.168231
  ...
# Subtest: task-card-gate dependency-single: cancel writes nothing
ok 2460 - task-card-gate dependency-single: cancel writes nothing
  ---
  duration_ms: 0.090623
  ...
# Subtest: task-card-gate dependency-single: stay runs today's write
ok 2461 - task-card-gate dependency-single: stay runs today's write
  ---
  duration_ms: 0.087236
  ...
# Subtest: task-card-gate dependency-single: move writes then moves
ok 2462 - task-card-gate dependency-single: move writes then moves
  ---
  duration_ms: 0.35112
  ...
# Subtest: task-card-gate dependency-marked: cancel writes nothing
ok 2463 - task-card-gate dependency-marked: cancel writes nothing
  ---
  duration_ms: 0.089761
  ...
# Subtest: task-card-gate dependency-marked: stay runs today's write
ok 2464 - task-card-gate dependency-marked: stay runs today's write
  ---
  duration_ms: 0.088018
  ...
# Subtest: task-card-gate dependency-marked: move writes then moves
ok 2465 - task-card-gate dependency-marked: move writes then moves
  ---
  duration_ms: 0.109589
  ...
# Subtest: task-card-gate dependency-vault: cancel writes nothing
ok 2466 - task-card-gate dependency-vault: cancel writes nothing
  ---
  duration_ms: 0.085954
  ...
# Subtest: task-card-gate dependency-vault: stay runs today's write
ok 2467 - task-card-gate dependency-vault: stay runs today's write
  ---
  duration_ms: 0.08909
  ...
# Subtest: task-card-gate dependency-vault: move writes then moves
ok 2468 - task-card-gate dependency-vault: move writes then moves
  ---
  duration_ms: 0.102315
  ...
# Subtest: task-card-gate dependency-counted: cancel writes nothing
ok 2469 - task-card-gate dependency-counted: cancel writes nothing
  ---
  duration_ms: 0.08919
  ...
# Subtest: task-card-gate dependency-counted: stay runs today's write
ok 2470 - task-card-gate dependency-counted: stay runs today's write
  ---
  duration_ms: 0.090473
  ...
# Subtest: task-card-gate dependency-counted: move writes then moves
ok 2471 - task-card-gate dependency-counted: move writes then moves
  ---
  duration_ms: 0.134437
  ...
# Subtest: task-card-gate negative rows never prompt
ok 2472 - task-card-gate negative rows never prompt
  ---
  duration_ms: 0.677192
  ...
# Subtest: task-card-gate counted sessions capture N targets
ok 2473 - task-card-gate counted sessions capture N targets
  ---
  duration_ms: 0.254216
  ...
# Subtest: task-card-gate walk: move advances once with Moved first
ok 2474 - task-card-gate walk: move advances once with Moved first
  ---
  duration_ms: 1.224749
  ...
# Subtest: task-card-gate walk: move failure falls back to card with partial
ok 2475 - task-card-gate walk: move failure falls back to card with partial
  ---
  duration_ms: 0.320622
  ...
# Subtest: task-card-gate walk: exactly one settle per origin
ok 2476 - task-card-gate walk: exactly one settle per origin
  ---
  duration_ms: 20.128074
  ...
# Subtest: task-card-gate route outcome resolves like lane and link-today
ok 2477 - task-card-gate route outcome resolves like lane and link-today
  ---
  duration_ms: 0.464797
  ...
# Subtest: inbox classifier covers the inbox contract
ok 2478 - inbox classifier covers the inbox contract
  ---
  duration_ms: 1.500855
  ...
# Subtest: isInboxNotePath matches the inbox contract through the vault
ok 2479 - isInboxNotePath matches the inbox contract through the vault
  ---
  duration_ms: 1.409822
  ...
# Subtest: isInboxNotePath is false without an inbox note and never throws
ok 2480 - isInboxNotePath is false without an inbox note and never throws
  ---
  duration_ms: 0.197898
  ...
# Subtest: route destinations drop every inbox note, the source, and templates
ok 2481 - route destinations drop every inbox note, the source, and templates
  ---
  duration_ms: 0.956687
  ...
# Subtest: route preflight accepts a live area destination
ok 2482 - route preflight accepts a live area destination
  ---
  duration_ms: 4.379911
  ...
# Subtest: route preflight refuses stale and colliding destinations
ok 2483 - route preflight refuses stale and colliding destinations
  ---
  duration_ms: 1.412116
  ...
# Subtest: route picker resolves move, stay, cancel, and close exactly once
ok 2484 - route picker resolves move, stay, cancel, and close exactly once
  ---
  duration_ms: 3.054861
  ...
# Subtest: route picker footer names the move, the hatch, and the way back
ok 2485 - route picker footer names the move, the hatch, and the way back
  ---
  duration_ms: 0.616787
  ...
# Subtest: route picker preflight refusal keeps the picker open with a notice
ok 2486 - route picker preflight refusal keeps the picker open with a notice
  ---
  duration_ms: 8.000654
  ...
# Subtest: route picker honors the shared move-picker guard
ok 2487 - route picker honors the shared move-picker guard
  ---
  duration_ms: 2.055814
  ...
# Subtest: promptInboxRoute moves, stays, and cancels with suspend pairing
ok 2488 - promptInboxRoute moves, stays, and cancels with suspend pairing
  ---
  duration_ms: 2.416352
  ...
# Subtest: commitInboxRoute moves the verified task with its children
ok 2489 - commitInboxRoute moves the verified task with its children
  ---
  duration_ms: 3.396844
  ...
# Subtest: commitInboxRoute into a blocked project tags the moved task
ok 2490 - commitInboxRoute into a blocked project tags the moved task
  ---
  duration_ms: 1.857355
  ...
# Subtest: commitInboxRoute moves a counted run and refuses on identity drift
ok 2491 - commitInboxRoute moves a counted run and refuses on identity drift
  ---
  duration_ms: 1.334287
  ...
# Subtest: reviewOutcomeResolves treats route like lane and link-today
ok 2492 - reviewOutcomeResolves treats route like lane and link-today
  ---
  duration_ms: 0.231191
  ...
# Subtest: nav api inboxRoute v1 delegates, shapes, and never throws
ok 2493 - nav api inboxRoute v1 delegates, shapes, and never throws
  ---
  duration_ms: 1.144524
  ...
# Subtest: history records ordered locations with file identity and dedupes adjacent repeats
ok 2494 - history records ordered locations with file identity and dedupes adjacent repeats
  ---
  duration_ms: 1.219739
  ...
# Subtest: transition records origin then destination and truncates forward only on success
ok 2495 - transition records origin then destination and truncates forward only on success
  ---
  duration_ms: 0.738119
  ...
# Subtest: history retains at most 100 locations and refreshes the live tip
ok 2496 - history retains at most 100 locations and refreshes the live tip
  ---
  duration_ms: 0.588623
  ...
# Subtest: rename updates paths and delete prunes without corrupting the index
ok 2497 - rename updates paths and delete prunes without corrupting the index
  ---
  duration_ms: 0.217906
  ...
# Subtest: bridge wraps add once, mirrors native jumps, and preserves the original call
ok 2498 - bridge wraps add once, mirrors native jumps, and preserves the original call
  ---
  duration_ms: 1.158181
  ...
# Subtest: bridge without a jump list preserves keys and emits one compatibility diagnostic
ok 2499 - bridge without a jump list preserves keys and emits one compatibility diagnostic
  ---
  duration_ms: 0.250598
  ...
# Subtest: registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
ok 2500 - registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
  ---
  duration_ms: 0.30389
  ...
# Subtest: Enter A->B round-trips with Ctrl+O and Ctrl+I
ok 2501 - Enter A->B round-trips with Ctrl+O and Ctrl+I
  ---
  duration_ms: 22.496875
  ...
# Subtest: counted Enter returns to the original cursor, not the counted link line
ok 2502 - counted Enter returns to the original cursor, not the counted link line
  ---
  duration_ms: 22.004996
  ...
# Subtest: picker choice records one jump and cancellation records none
ok 2503 - picker choice records one jump and cancellation records none
  ---
  duration_ms: 22.509631
  ...
# Subtest: stale picker origin is rejected and failed opens record nothing
ok 2504 - stale picker origin is rejected and failed opens record nothing
  ---
  duration_ms: 21.976641
  ...
# Subtest: Backspace shares the link path and no-link lines fall through
ok 2505 - Backspace shares the link path and no-link lines fall through
  ---
  duration_ms: 20.899837
  ...
# Subtest: counted traversal honors boundaries and new jumps replace the forward branch
ok 2506 - counted traversal honors boundaries and new jumps replace the forward branch
  ---
  duration_ms: 0.823071
  ...
# Subtest: ordinary motion before back is preserved for forward restore
ok 2507 - ordinary motion before back is preserved for forward restore
  ---
  duration_ms: 0.3193
  ...
# Subtest: deleted entries are skipped and heading links settle before recording
ok 2508 - deleted entries are skipped and heading links settle before recording
  ---
  duration_ms: 20.999537
  ...
# Subtest: native fallback runs with empty history and boundaries never replay natives
ok 2509 - native fallback runs with empty history and boundaries never replay natives
  ---
  duration_ms: 0.643969
  ...
# Subtest: unload restores the native add and keeps a foreign later mapping
ok 2510 - unload restores the native add and keeps a foreign later mapping
  ---
  duration_ms: 0.415704
  ...
# Subtest: exact eligibility authorizes one due-Ready ROTTEN row
ok 2511 - exact eligibility authorizes one due-Ready ROTTEN row
  ---
  duration_ms: 1.872574
  ...
# Subtest: exact eligibility authorizes a TICKLER row
ok 2512 - exact eligibility authorizes a TICKLER row
  ---
  duration_ms: 0.270185
  ...
# Subtest: exact eligibility refuses every stale-cache shape
ok 2513 - exact eligibility refuses every stale-cache shape
  ---
  duration_ms: 0.690949
  ...
# Subtest: exact eligibility refuses non-Ready and non-due rows
ok 2514 - exact eligibility refuses non-Ready and non-due rows
  ---
  duration_ms: 0.386447
  ...
# Subtest: legacy refs still match line-only while exact refuses
ok 2515 - legacy refs still match line-only while exact refuses
  ---
  duration_ms: 0.782754
  ...
# Subtest: keeps support needs namespace v5 with keepLine
ok 2516 - keeps support needs namespace v5 with keepLine
  ---
  duration_ms: 0.209169
  ...
# Subtest: decay decisions need namespace v6 with keepLine
ok 2517 - decay decisions need namespace v6 with keepLine
  ---
  duration_ms: 0.324419
  ...
# Subtest: batch forwards per-target counted decisions to the stamper
ok 2518 - batch forwards per-target counted decisions to the stamper
  ---
  duration_ms: 1.002224
  ...
# Subtest: batch keeps legacy index targets uncounted
ok 2519 - batch keeps legacy index targets uncounted
  ---
  duration_ms: 0.512358
  ...
# Subtest: a throwing stamper refuses the batch with no partial write
ok 2520 - a throwing stamper refuses the batch with no partial write
  ---
  duration_ms: 0.653067
  ...
# Subtest: parseKeepsCount reads the first valid value only
ok 2521 - parseKeepsCount reads the first valid value only
  ---
  duration_ms: 0.42459
  ...
# Subtest: countFreshStampKept measures actual increments only
ok 2522 - countFreshStampKept measures actual increments only
  ---
  duration_ms: 0.256079
  ...
# Subtest: fresh stamp notice tails kept increments without promises
ok 2523 - fresh stamp notice tails kept increments without promises
  ---
  duration_ms: 0.300815
  ...
# Subtest: duplicate source targets dedupe to one write
ok 2524 - duplicate source targets dedupe to one write
  ---
  duration_ms: 0.250097
  ...
# Subtest: single Alt+F increments an exact due-Ready ROTTEN task
ok 2525 - single Alt+F increments an exact due-Ready ROTTEN task
  ---
  duration_ms: 7.428932
  ...
# Subtest: single Alt+F preserves NEW, lane, and early tasks without counting
ok 2526 - single Alt+F preserves NEW, lane, and early tasks without counting
  ---
  duration_ms: 2.892031
  ...
# Subtest: same-day repeat stays identical and counts nothing
ok 2527 - same-day repeat stays identical and counts nothing
  ---
  duration_ms: 0.784458
  ...
# Subtest: Pending Alt+F writes its summary with the stamp in one edit
ok 2528 - Pending Alt+F writes its summary with the stamp in one edit
  ---
  duration_ms: 1.883716
  ...
# Subtest: counted Pending refresh shares one summary only with Pending targets
ok 2529 - counted Pending refresh shares one summary only with Pending targets
  ---
  duration_ms: 1.01091
  ...
# Subtest: a refusing counted target refuses before the Pending Work Log prompt
ok 2530 - a refusing counted target refuses before the Pending Work Log prompt
  ---
  duration_ms: 0.608812
  ...
# Subtest: blank Pending refresh advances; cancelled or stale prompts write nothing
ok 2531 - blank Pending refresh advances; cancelled or stale prompts write nothing
  ---
  duration_ms: 1.662414
  ...
# Subtest: stale queue match stamps uncounted and never inflates
ok 2532 - stale queue match stamps uncounted and never inflates
  ---
  duration_ms: 0.688395
  ...
# Subtest: counted Alt+F increments every exact target once
ok 2533 - counted Alt+F increments every exact target once
  ---
  duration_ms: 0.737638
  ...
# Subtest: stale editor source refuses with no write
ok 2534 - stale editor source refuses with no write
  ---
  duration_ms: 0.242683
  ...
# Subtest: single-note write lands in one editor transaction and keeps CRLF
ok 2535 - single-note write lands in one editor transaction and keeps CRLF
  ---
  duration_ms: 0.635683
  ...
# Subtest: v5 without keepLine fails without writing
ok 2536 - v5 without keepLine fails without writing
  ---
  duration_ms: 0.19889
  ...
# Subtest: throwing v5 keepLine refuses the batch with no partial write
ok 2537 - throwing v5 keepLine refuses the batch with no partial write
  ---
  duration_ms: 0.426103
  ...
# Subtest: pre-v5 ledger stamps uncounted through the old stamper
ok 2538 - pre-v5 ledger stamps uncounted through the old stamper
  ---
  duration_ms: 0.615846
  ...
# Subtest: Task Link session skips an at-limit decide target
ok 2539 - Task Link session skips an at-limit decide target
  ---
  duration_ms: 2.564897
  ...
# Subtest: Task Link refresh counts one exact target
ok 2540 - Task Link refresh counts one exact target
  ---
  duration_ms: 1.064031
  ...
# Subtest: duplicate Task Links to one target stamp and count once
ok 2541 - duplicate Task Links to one target stamp and count once
  ---
  duration_ms: 0.610665
  ...
# Subtest: counted Task Links dedupe targets and log only the Pending target
ok 2542 - counted Task Links dedupe targets and log only the Pending target
  ---
  duration_ms: 1.090512
  ...
# Subtest: multi-note stale preimage refuses with no writes
ok 2543 - multi-note stale preimage refuses with no writes
  ---
  duration_ms: 0.878266
  ...
# Subtest: multi-note write failure rolls back the first note
ok 2544 - multi-note write failure rolls back the first note
  ---
  duration_ms: 1.033152
  ...
# Subtest: one physical key through two routes stamps once
ok 2545 - one physical key through two routes stamps once
  ---
  duration_ms: 1.337784
  ...
# Subtest: Ctrl+Alt+F capture advances once and consumes a Vim prefix
ok 2546 - Ctrl+Alt+F capture advances once and consumes a Vim prefix
  ---
  duration_ms: 0.556883
  ...
# Subtest: obsolete and extra-modifier F chords stay unconsumed
ok 2547 - obsolete and extra-modifier F chords stay unconsumed
  ---
  duration_ms: 0.292007
  ...
# Subtest: live Ctrl+Alt+F double dispatch asks once on a Pending task
ok 2548 - live Ctrl+Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.642877
  ...
# Subtest: live Alt+F double dispatch asks once on a Pending task
ok 2549 - live Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.667394
  ...
# Subtest: already-handled refresh keydown leaves Vim state alone
ok 2550 - already-handled refresh keydown leaves Vim state alone
  ---
  duration_ms: 0.299342
  ...
# Subtest: parseBobOpenNotesParams accepts indexed entries and ignores unknown keys
ok 2551 - parseBobOpenNotesParams accepts indexed entries and ignores unknown keys
  ---
  duration_ms: 1.773556
  ...
# Subtest: parseBobOpenNotesParams rejects every malformed URI field
ok 2552 - parseBobOpenNotesParams rejects every malformed URI field
  ---
  duration_ms: 0.437235
  ...
# Subtest: invalid batches show one notice and open nothing
ok 2553 - invalid batches show one notice and open nothing
  ---
  duration_ms: 1.095382
  ...
# Subtest: path mapping follows a symlink realpath into the vault
ok 2554 - path mapping follows a symlink realpath into the vault
  ---
  duration_ms: 3.144893
  ...
# Subtest: new-tab policy reuses existing tabs and the active empty tab, keeping order and primary active
ok 2555 - new-tab policy reuses existing tabs and the active empty tab, keeping order and primary active
  ---
  duration_ms: 1.326893
  ...
# Subtest: an absent or outside entry fails independently and a PDF opens without landing
ok 2556 - an absent or outside entry fails independently and a PDF opens without landing
  ---
  duration_ms: 2000.945906
  ...
# Subtest: a resolved note that is not open waits until its captured digest is cached
ok 2557 - a resolved note that is not open waits until its captured digest is cached
  ---
  duration_ms: 63.767759
  ...
# Subtest: a per-entry open failure does not prevent later notes from opening
ok 2558 - a per-entry open failure does not prevent later notes from opening
  ---
  duration_ms: 0.819134
  ...
# Subtest: waits for a newly created vault file and a late visible line digest
ok 2559 - waits for a newly created vault file and a late visible line digest
  ---
  duration_ms: 61.64179
  ...
# Subtest: re-finds a moved digest on any line, including prose and Pomodoro rows
ok 2560 - re-finds a moved digest on any line, including prose and Pomodoro rows
  ---
  duration_ms: 1.134476
  ...
# Subtest: deadline fallback opens near the planned line and reports a changed capture
ok 2561 - deadline fallback opens near the planned line and reports a changed capture
  ---
  duration_ms: 2001.022531
  ...
# Subtest: truncation reports how many of the full list opened
ok 2562 - truncation reports how many of the full list opened
  ---
  duration_ms: 0.662184
  ...
# Subtest: serializes quick URLs and leaves the later URL active
ok 2563 - serializes quick URLs and leaves the later URL active
  ---
  duration_ms: 5.144801
  ...
# Subtest: primary landing flashes briefly, secondary landings do not, and the handler is read-only
ok 2564 - primary landing flashes briefly, secondary landings do not, and the handler is read-only
  ---
  duration_ms: 17.059025
  ...
# Subtest: onload registers bob-open-notes beside bob-goto-task
ok 2565 - onload registers bob-open-notes beside bob-goto-task
  ---
  duration_ms: 1.276006
  ...
# Subtest: a non-file sidebar view is not reused as an empty tab
ok 2566 - a non-file sidebar view is not reused as an empty tab
  ---
  duration_ms: 0.505535
  ...
# Subtest: a true empty tab is reused for the first entry
ok 2567 - a true empty tab is reused for the first entry
  ---
  duration_ms: 0.244166
  ...
# Subtest: three new tabs follow entry order in the tab strip
ok 2568 - three new tabs follow entry order in the tab strip
  ---
  duration_ms: 0.459738
  ...
# Subtest: two tabs of the same note reuse the first matching leaf
ok 2569 - two tabs of the same note reuse the first matching leaf
  ---
  duration_ms: 0.230069
  ...
# Subtest: a missing file does not scan vault lists when getAbstractFileByPath exists
ok 2570 - a missing file does not scan vault lists when getAbstractFileByPath exists
  ---
  duration_ms: 2000.033183
  ...
# Subtest: new tabs append at the far right when the middle tab is active
ok 2571 - new tabs append at the far right when the middle tab is active
  ---
  duration_ms: 1.03233
  ...
# Subtest: a reused tab stays put while a new one is appended
ok 2572 - a reused tab stays put while a new one is appended
  ---
  duration_ms: 0.505294
  ...
# Subtest: a deferred tab is reused and findMarkdownLeafByPath sees it
ok 2573 - a deferred tab is reused and findMarkdownLeafByPath sees it
  ---
  duration_ms: 0.703242
  ...
# Subtest: a deferred sidebar leaf whose saved state names the note is not reused
ok 2574 - a deferred sidebar leaf whose saved state names the note is not reused
  ---
  duration_ms: 0.501968
  ...
# Subtest: a loaded main-area match beats an earlier loaded sidebar match
ok 2575 - a loaded main-area match beats an earlier loaded sidebar match
  ---
  duration_ms: 0.379364
  ...
# Subtest: a new tab goes to the end of the main group when a sidebar leaf is active
ok 2576 - a new tab goes to the end of the main group when a sidebar leaf is active
  ---
  duration_ms: 0.395716
  ...
# Subtest: falling back without createLeafInParent still opens a new tab
ok 2577 - falling back without createLeafInParent still opens a new tab
  ---
  duration_ms: 0.385476
  ...
# Subtest: falling back when createLeafInParent throws still opens a new tab
ok 2578 - falling back when createLeafInParent throws still opens a new tab
  ---
  duration_ms: 0.384464
  ...
# Subtest: collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
ok 2579 - collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
  ---
  duration_ms: 2.545479
  ...
# Subtest: getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
ok 2580 - getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
  ---
  duration_ms: 2.548114
  ...
# Subtest: getProjectBlockState reports an open external prerequisite
ok 2581 - getProjectBlockState reports an open external prerequisite
  ---
  duration_ms: 0.772855
  ...
# Subtest: getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
ok 2582 - getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
  ---
  duration_ms: 0.787283
  ...
# Subtest: getProjectBlockState scheduledValue override is the inline date, not frontmatter
ok 2583 - getProjectBlockState scheduledValue override is the inline date, not frontmatter
  ---
  duration_ms: 0.533879
  ...
# Subtest: getProjectBlockState skips internal and archive Depends-On links
ok 2584 - getProjectBlockState skips internal and archive Depends-On links
  ---
  duration_ms: 0.429389
  ...
# Subtest: getProjectBlockState is a no-op for terminal, daily, and non-project notes
ok 2585 - getProjectBlockState is a no-op for terminal, daily, and non-project notes
  ---
  duration_ms: 0.778836
  ...
# Subtest: projectLooksBlockedByPrjShortcut is the single [?] ^prj row
ok 2586 - projectLooksBlockedByPrjShortcut is the single [?] ^prj row
  ---
  duration_ms: 0.296255
  ...
# Subtest: taskHasProjectBlockedTag is token-bounded and does not match \#prj
ok 2587 - taskHasProjectBlockedTag is token-bounded and does not match \#prj
  ---
  duration_ms: 0.432967
  ...
# Subtest: setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
ok 2588 - setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
  ---
  duration_ms: 1.047039
  ...
# Subtest: reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
ok 2589 - reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
  ---
  duration_ms: 0.543928
  ...
# Subtest: reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
ok 2590 - reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
  ---
  duration_ms: 0.341672
  ...
# Subtest: reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
ok 2591 - reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
  ---
  duration_ms: 0.224849
  ...
# Subtest: ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
ok 2592 - ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
  ---
  duration_ms: 7.029808
  ...
# Subtest: recovery gate keeps a resident of a blocked project blocked after own deps close
ok 2593 - recovery gate keeps a resident of a blocked project blocked after own deps close
  ---
  duration_ms: 2.939532
  ...
# Subtest: recovery gate blocks residents on a future inline project date with no deps
ok 2594 - recovery gate blocks residents on a future inline project date with no deps
  ---
  duration_ms: 0.620575
  ...
# Subtest: planDeferredPomodoroLinkCleanup always deletes a last-child open entry
ok 2595 - planDeferredPomodoroLinkCleanup always deletes a last-child open entry
  ---
  duration_ms: 2.346179
  ...
# Subtest: TICKLER notice uses unblocked <date> when returnedBy is unblocked
ok 2596 - TICKLER notice uses unblocked <date> when returnedBy is unblocked
  ---
  duration_ms: 0.648198
  ...
# Subtest: recognition: a `^prj` parent in a project note carries its residents
ok 2597 - recognition: a `^prj` parent in a project note carries its residents
  ---
  duration_ms: 2.796429
  ...
# Subtest: recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
ok 2598 - recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
  ---
  duration_ms: 0.428538
  ...
# Subtest: add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
ok 2599 - add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
  ---
  duration_ms: 4.840319
  ...
# Subtest: add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
ok 2600 - add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
  ---
  duration_ms: 2.506734
  ...
# Subtest: guards: a same-note add to `^prj` refuses, including mixed batches
ok 2601 - guards: a same-note add to `^prj` refuses, including mixed batches
  ---
  duration_ms: 0.73845
  ...
# Subtest: guards: the stage disables same-note rows for `^prj` with `inside this project`
ok 2602 - guards: the stage disables same-note rows for `^prj` with `inside this project`
  ---
  duration_ms: 1.060484
  ...
# Subtest: guards: cycle detection includes the implicit resident edges (§13.6)
ok 2603 - guards: cycle detection includes the implicit resident edges (§13.6)
  ---
  duration_ms: 1.250608
  ...
# Subtest: removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
ok 2604 - removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
  ---
  duration_ms: 3.312865
  ...
# Subtest: removal: a resident with its own reason stays `[?]` without the tag (PDB3)
ok 2605 - removal: a resident with its own reason stays `[?]` without the tag (PDB3)
  ---
  duration_ms: 1.363483
  ...
# Subtest: removal without a registry defers to reconcile: residents keep `[?]` and the tag
ok 2606 - removal without a registry defers to reconcile: residents keep `[?]` and the tag
  ---
  duration_ms: 1.173581
  ...
# Subtest: writer: one gesture commits `^prj` and its residents in a single undo group
ok 2607 - writer: one gesture commits `^prj` and its residents in a single undo group
  ---
  duration_ms: 0.936999
  ...
# Subtest: writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
ok 2608 - writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
  ---
  duration_ms: 2.239785
  ...
# Subtest: notices: the project strings name the task, the flips, and the Pomodoro cleanup
ok 2609 - notices: the project strings name the task, the flips, and the Pomodoro cleanup
  ---
  duration_ms: 0.249967
  ...
# Subtest: mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
ok 2610 - mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
  ---
  duration_ms: 0.229798
  ...
# Subtest: api v3: removeDependencyByRef delegates removals to the single-transaction writer
ok 2611 - api v3: removeDependencyByRef delegates removals to the single-transaction writer
  ---
  duration_ms: 0.70703
  ...
# Subtest: api v3: openDependencyStageForRef opens the Depends on stage on the owning task
ok 2612 - api v3: openDependencyStageForRef opens the Depends on stage on the owning task
  ---
  duration_ms: 0.299272
  ...
# Subtest: internal links stay on the line but leave the field (PDR7)
ok 2613 - internal links stay on the line but leave the field (PDR7)
  ---
  duration_ms: 1.134837
  ...
# Subtest: removal from an unblocked ^prj never recovers own-reason residents (§13.10)
ok 2614 - removal from an unblocked ^prj never recovers own-reason residents (§13.10)
  ---
  duration_ms: 0.570399
  ...
# Subtest: resident recovery touches only tagged residents (§13.10)
ok 2615 - resident recovery touches only tagged residents (§13.10)
  ---
  duration_ms: 0.956506
  ...
# Subtest: stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
ok 2616 - stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
  ---
  duration_ms: 0.684477
  ...
# Subtest: projectDependentResidentKeys lists open residents with block ids
ok 2617 - projectDependentResidentKeys lists open residents with block ids
  ---
  duration_ms: 0.278502
  ...
# Subtest: navNoteScopeFlags marks daily notes; a missing writer stays null
ok 2618 - navNoteScopeFlags marks daily notes; a missing writer stays null
  ---
  duration_ms: 0.222775
  ...
# Subtest: reconcileBlockedScheduledTaskLine forwards scope flags to the writer
ok 2619 - reconcileBlockedScheduledTaskLine forwards scope flags to the writer
  ---
  duration_ms: 0.138395
  ...
# Subtest: parseProjectNoteFrontmatter ignores leftover scheduled keys
ok 2620 - parseProjectNoteFrontmatter ignores leftover scheduled keys
  ---
  duration_ms: 1.300352
  ...
# Subtest: formatTaskMoveProjectCountsNotice names blocked and recovered counts
ok 2621 - formatTaskMoveProjectCountsNotice names blocked and recovered counts
  ---
  duration_ms: 0.126843
  ...
# Subtest: PDS15: projectParentTarget keeps the path and drops alias and heading
ok 2622 - PDS15: projectParentTarget keeps the path and drops alias and heading
  ---
  duration_ms: 1.279763
  ...
# Subtest: PDS6: list-form, missing, and non-wikilink parents yield none
ok 2623 - PDS6: list-form, missing, and non-wikilink parents yield none
  ---
  duration_ms: 0.441412
  ...
# Subtest: PDS15: resolveProjectParentPath accepts alias, path, and heading forms
ok 2624 - PDS15: resolveProjectParentPath accepts alias, path, and heading forms
  ---
  duration_ms: 0.384103
  ...
# Subtest: PDS6: self, unresolved, and ambiguous basenames yield no parent
ok 2625 - PDS6: self, unresolved, and ambiguous basenames yield no parent
  ---
  duration_ms: 0.161598
  ...
# Subtest: buildProjectChildrenMap and descendants BFS skip cycles and cap depth
ok 2626 - buildProjectChildrenMap and descendants BFS skip cycles and cap depth
  ---
  duration_ms: 2.422785
  ...
# Subtest: PDS6: area, terminal, daily, and self-parent notes are not children
ok 2627 - PDS6: area, terminal, daily, and self-parent notes are not children
  ---
  duration_ms: 0.348064
  ...
# Subtest: PDG8: planner blocks child and grandchild ^prj and residents
ok 2628 - PDG8: planner blocks child and grandchild ^prj and residents
  ---
  duration_ms: 2.371797
  ...
# Subtest: PDG9: planner recovers tagged descendants with [unblocked::]
ok 2629 - PDG9: planner recovers tagged descendants with [unblocked::]
  ---
  duration_ms: 1.34152
  ...
# Subtest: PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
ok 2630 - PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
  ---
  duration_ms: 1.756373
  ...
# Subtest: PDG11: a tagged root re-asserts descendant tags and recovers nothing
ok 2631 - PDG11: a tagged root re-asserts descendant tags and recovers nothing
  ---
  duration_ms: 0.788035
  ...
# Subtest: tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
ok 2632 - tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
  ---
  duration_ms: 0.237163
  ...
# Subtest: tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
ok 2633 - tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
  ---
  duration_ms: 1.538236
  ...
# Subtest: tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
ok 2634 - tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
  ---
  duration_ms: 0.153523
  ...
# Subtest: tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
ok 2635 - tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
  ---
  duration_ms: 1.699645
  ...
# Subtest: PDG13: failProjectPrjInternalAdd refuses descendant targets
ok 2636 - PDG13: failProjectPrjInternalAdd refuses descendant targets
  ---
  duration_ms: 0.229668
  ...
# Subtest: PDG13: planDependencyEdit refuses a descendant add from the files map
ok 2637 - PDG13: planDependencyEdit refuses a descendant add from the files map
  ---
  duration_ms: 1.148773
  ...
# Subtest: PDG13: the stage disables descendant rows
ok 2638 - PDG13: the stage disables descendant rows
  ---
  duration_ms: 1.130628
  ...
# Subtest: reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
ok 2639 - reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
  ---
  duration_ms: 0.316494
  ...
# Subtest: tag proxy: removing the last own dep of a tagged ^prj recovers nobody
ok 2640 - tag proxy: removing the last own dep of a tagged ^prj recovers nobody
  ---
  duration_ms: 2.600935
  ...
# Subtest: PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
ok 2641 - PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
  ---
  duration_ms: 24.392524
  ...
# Subtest: PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
ok 2642 - PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
  ---
  duration_ms: 5.810521
  ...
# Subtest: PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
ok 2643 - PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
  ---
  duration_ms: 4.428013
  ...
# Subtest: PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
ok 2644 - PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
  ---
  duration_ms: 3.595824
  ...
# Subtest: PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
ok 2645 - PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
  ---
  duration_ms: 5.482827
  ...
# Subtest: PDG12: moving the project date due recovers descendants
ok 2646 - PDG12: moving the project date due recovers descendants
  ---
  duration_ms: 3.835933
  ...
# Subtest: PDG12: deleting the project date recovers descendants
ok 2647 - PDG12: deleting the project date recovers descendants
  ---
  duration_ms: 5.818085
  ...
# Subtest: PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
ok 2648 - PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
  ---
  duration_ms: 4.205417
  ...
# Subtest: PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
ok 2649 - PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
  ---
  duration_ms: 3.393308
  ...
# Subtest: Task Link Depends on writer preserves the internal-target guard on a project task
ok 2650 - Task Link Depends on writer preserves the internal-target guard on a project task
  ---
  duration_ms: 0.956496
  ...
# Subtest: api v3 removeDependencyByRef runs the recovery cascade for a linked project task
ok 2651 - api v3 removeDependencyByRef runs the recovery cascade for a linked project task
  ---
  duration_ms: 3.489671
  ...
# Subtest: counted Schedule writer cascades a future date through descendants
ok 2652 - counted Schedule writer cascades a future date through descendants
  ---
  duration_ms: 3.864837
  ...
# Subtest: counted subtree roots are ancestor-first and each descendant note is planned once
ok 2653 - counted subtree roots are ancestor-first and each descendant note is planned once
  ---
  duration_ms: 2.667984
  ...
# Subtest: Ctrl+D on the Depends on row removes the line and recovers the subtree
ok 2654 - Ctrl+D on the Depends on row removes the line and recovers the subtree
  ---
  duration_ms: 3.53642
  ...
# Subtest: a ^prj with no children reads no other note
ok 2655 - a ^prj with no children reads no other note
  ---
  duration_ms: 0.250347
  ...
# Subtest: single seeds from raw text, not display decorations
ok 2656 - single seeds from raw text, not display decorations
  ---
  duration_ms: 8.933504
  ...
# Subtest: legacy valid free wins; invalid and taken fall through
ok 2657 - legacy valid free wins; invalid and taken fall through
  ---
  duration_ms: 1.355348
  ...
# Subtest: batch reserves suffixes for two same-text tasks
ok 2658 - batch reserves suffixes for two same-text tasks
  ---
  duration_ms: 0.893125
  ...
# Subtest: counted-source, vault-single, and vault-counted seed per mode
ok 2659 - counted-source, vault-single, and vault-counted seed per mode
  ---
  duration_ms: 1.033473
  ...
# Subtest: cross-note uses the target note, never the dependent fallback
ok 2660 - cross-note uses the target note, never the dependent fallback
  ---
  duration_ms: 1.142331
  ...
# Subtest: staging writes nothing until confirmed
ok 2661 - staging writes nothing until confirmed
  ---
  duration_ms: 0.563816
  ...
# Subtest: Alt+P matches Ctrl+Enter for roll, decay, project, and counted task writes
ok 2662 - Alt+P matches Ctrl+Enter for roll, decay, project, and counted task writes
  ---
  duration_ms: 50.640659
  ...
# Subtest: Alt+P matches Ctrl+Enter for a counted Task Link batch
ok 2663 - Alt+P matches Ctrl+Enter for a counted Task Link batch
  ---
  duration_ms: 10.047159
  ...
# Subtest: Alt+P hides immediate rolls and reveals the optional Next Work summary
ok 2664 - Alt+P hides immediate rolls and reveals the optional Next Work summary
  ---
  duration_ms: 4.030745
  ...
# Subtest: a cancel recommendation waits for the visible card and the second Alt+P cancels
ok 2665 - a cancel recommendation waits for the visible card and the second Alt+P cancels
  ---
  duration_ms: 3.7247
  ...
# Subtest: no priority and unavailable recurring tasks reveal the card without writing
ok 2666 - no priority and unavailable recurring tasks reveal the card without writing
  ---
  duration_ms: 3.408657
  ...
# Subtest: inbox routing is shown before the write and a managed line redirects to its owner
ok 2667 - inbox routing is shown before the write and a managed line redirects to its owner
  ---
  duration_ms: 4.045923
  ...
# Subtest: a landed review row advances once after Alt+P writes
ok 2668 - a landed review row advances once after Alt+P writes
  ---
  duration_ms: 2.971193
  ...
# Subtest: the card alias uses the physical Alt+P code and ignores repeats
ok 2669 - the card alias uses the physical Alt+P code and ignores repeats
  ---
  duration_ms: 1.023554
  ...
# Subtest: a throwing one-shot dispatch always reveals the still-open card
ok 2670 - a throwing one-shot dispatch always reveals the still-open card
  ---
  duration_ms: 1.799766
  ...
# Subtest: the registered command owns Alt+P and a Vim count is consumed once
ok 2671 - the registered command owns Alt+P and a Vim count is consumed once
  ---
  duration_ms: 2.639399
  ...
# Subtest: quick-roll visibility CSS disables the modal entrance animation
ok 2672 - quick-roll visibility CSS disables the modal entrance animation
  ---
  duration_ms: 0.761414
  ...
# Subtest: Less often picker renders actual rows from 90 days and Escape writes nothing
ok 2673 - Less often picker renders actual rows from 90 days and Escape writes nothing
  ---
  duration_ms: 5.529776
  ...
# Subtest: Less often picker renders actual rows from 120 days and Escape writes nothing
ok 2674 - Less often picker renders actual rows from 120 days and Escape writes nothing
  ---
  duration_ms: 0.926068
  ...
# Subtest: Less often picker renders actual rows from 180 days and Escape writes nothing
ok 2675 - Less often picker renders actual rows from 180 days and Escape writes nothing
  ---
  duration_ms: 0.601448
  ...
# Subtest: renderFooter skips malformed hints and retains valid structured hints
ok 2676 - renderFooter skips malformed hints and retains valid structured hints
  ---
  duration_ms: 0.338466
  ...
# Subtest: Pending refresh modal previews the dated Work Log and confirms once
ok 2677 - Pending refresh modal previews the dated Work Log and confirms once
  ---
  duration_ms: 1.674397
  ...
# Subtest: dismissing the Pending refresh modal cancels without a summary
ok 2678 - dismissing the Pending refresh modal cancels without a summary
  ---
  duration_ms: 0.357994
  ...
# Subtest: nav LK1–LK18 parse relation grammar and reject the other relation parser
ok 2679 - nav LK1–LK18 parse relation grammar and reject the other relation parser
  ---
  duration_ms: 2.677972
  ...
# Subtest: nav LK14–LK19 context and cross-parse rules
ok 2680 - nav LK14–LK19 context and cross-parse rules
  ---
  duration_ms: 0.589284
  ...
# Subtest: nav MC5 refuses relation embeds and MC16 keeps LINKS while dropping LINKED FROM
ok 2681 - nav MC5 refuses relation embeds and MC16 keeps LINKS while dropping LINKED FROM
  ---
  duration_ms: 1.335309
  ...
# Subtest: nav MC15 hands LINKS edits to the relation mirror and notices generated lines once
ok 2682 - nav MC15 hands LINKS edits to the relation mirror and notices generated lines once
  ---
  duration_ms: 2.867935
  ...
# Subtest: LG3: typed relation labels commit their text through the relation field
    # Subtest: add writes the typed label and mirror
    ok 1 - add writes the typed label and mirror
      ---
      duration_ms: 8.269745
      ...
    # Subtest: typed text is normalized before commit
    ok 2 - typed text is normalized before commit
      ---
      duration_ms: 1.156908
      ...
    # Subtest: relabel replaces an existing label and its mirror
    ok 3 - relabel replaces an existing label and its mirror
      ---
      duration_ms: 5.051283
      ...
    # Subtest: Linked from labels the other task's LINKS line
    ok 4 - Linked from labels the other task's LINKS line
      ---
      duration_ms: 1.315943
      ...
    # Subtest: suggestion, plain, and raw-input paths remain supported
    ok 5 - suggestion, plain, and raw-input paths remain supported
      ---
      duration_ms: 2.562252
      ...
    1..5
ok 2683 - LG3: typed relation labels commit their text through the relation field
  ---
  duration_ms: 19.395115
  ...
# Subtest: links-to row follows blocks with N, first label, cut target, and +K
ok 2684 - links-to row follows blocks with N, first label, cut target, and +K
  ---
  duration_ms: 6.260581
  ...
# Subtest: links-to row stays available on closed tasks and empty LINKS lines
ok 2685 - links-to row stays available on closed tasks and empty LINKS lines
  ---
  duration_ms: 1.764659
  ...
# Subtest: links-to row refuses non-tasks and read-only notes
ok 2686 - links-to row refuses non-tasks and read-only notes
  ---
  duration_ms: 1.141529
  ...
# Subtest: card keycap l opens Links to; input focus keeps it quiet
ok 2687 - card keycap l opens Links to; input focus keeps it quiet
  ---
  duration_ms: 1.197015
  ...
# Subtest: card ⇧L shows live incoming detail and routes Ctrl+D by direction
ok 2688 - card ⇧L shows live incoming detail and routes Ctrl+D by direction
  ---
  duration_ms: 2.374452
  ...
# Subtest: index-only Linked-from rows convert 1-based edges into nav records
ok 2689 - index-only Linked-from rows convert 1-based edges into nav records
  ---
  duration_ms: 0.616827
  ...
# Subtest: card ⇧L detail cleans a raw index task line
ok 2690 - card ⇧L detail cleans a raw index task line
  ---
  duration_ms: 0.710486
  ...
# Subtest: Linked-from scans source LINKS, reverses built-in phrases, and ignores stored mirrors
ok 2691 - Linked-from scans source LINKS, reverses built-in phrases, and ignores stored mirrors
  ---
  duration_ms: 2.553143
  ...
# Subtest: LG7: reverse-stage Enter writes the source's LINKS and target mirror
ok 2692 - LG7: reverse-stage Enter writes the source's LINKS and target mirror
  ---
  duration_ms: 1.211863
  ...
# Subtest: LG12: counted Links to applies the chosen labelled target to every source
ok 2693 - LG12: counted Links to applies the chosen labelled target to every source
  ---
  duration_ms: 2.260685
  ...
# Subtest: LG8: Ctrl+Shift+P on a LINKS line resolves to the owner's stage
ok 2694 - LG8: Ctrl+Shift+P on a LINKS line resolves to the owner's stage
  ---
  duration_ms: 0.93728
  ...
# Subtest: pool keeps closed tasks and done/ archives, drops dailies and templates
ok 2695 - pool keeps closed tasks and done/ archives, drops dailies and templates
  ---
  duration_ms: 0.561431
  ...
# Subtest: stage lists CURRENT in authored order, then RESULTS, then CLOSED
ok 2696 - stage lists CURRENT in authored order, then RESULTS, then CLOSED
  ---
  duration_ms: 2.513358
  ...
# Subtest: LG4: missing CURRENT targets stay removable; malformed lines refuse
ok 2697 - LG4: missing CURRENT targets stay removable; malformed lines refuse
  ---
  duration_ms: 0.538779
  ...
# Subtest: prerequisite targets badge; id-less rows prompt
ok 2698 - prerequisite targets badge; id-less rows prompt
  ---
  duration_ms: 1.42461
  ...
# Subtest: subtitle, consequence strip, live sentence, and label refusal copy
ok 2699 - subtitle, consequence strip, live sentence, and label refusal copy
  ---
  duration_ms: 0.511818
  ...
# Subtest: LG15: marked rows plan one commit with adds and unlinks split
ok 2700 - LG15: marked rows plan one commit with adds and unlinks split
  ---
  duration_ms: 0.27775
  ...
# Subtest: LG1: stage link writes LINKS, mirror, and mint in one transaction
ok 2701 - LG1: stage link writes LINKS, mirror, and mint in one transaction
  ---
  duration_ms: 1.443966
  ...
# Subtest: LG2: cross-note mirror follows; a changed target suffixes the notice
ok 2702 - LG2: cross-note mirror follows; a changed target suffixes the notice
  ---
  duration_ms: 1.277809
  ...
# Subtest: LG4: CURRENT unlink removes the entry and its mirror entry
ok 2703 - LG4: CURRENT unlink removes the entry and its mirror entry
  ---
  duration_ms: 1.13675
  ...
# Subtest: LG6: archived targets link with the live-only suffix and no mirror
ok 2704 - LG6: archived targets link with the live-only suffix and no mirror
  ---
  duration_ms: 0.528589
  ...
# Subtest: LG13: linking never stamps, routes, or touches Depends-On lines
ok 2705 - LG13: linking never stamps, routes, or touches Depends-On lines
  ---
  duration_ms: 1.121922
  ...
# Subtest: LG15: two targets link in one gesture with one notice
ok 2706 - LG15: two targets link in one gesture with one notice
  ---
  duration_ms: 0.523229
  ...
# Subtest: LG5: id-less targets refuse at the writer, so the stage prompts first
ok 2707 - LG5: id-less targets refuse at the writer, so the stage prompts first
  ---
  duration_ms: 0.227204
  ...
# Subtest: LG7: Ctrl+Shift+P resolves LINKED FROM to its owner's reverse stage
ok 2708 - LG7: Ctrl+Shift+P resolves LINKED FROM to its owner's reverse stage
  ---
  duration_ms: 0.155307
  ...
# Subtest: api.relations openStage opens both directions at v1
ok 2709 - api.relations openStage opens both directions at v1
  ---
  duration_ms: 0.452354
  ...
# relations.linked_from_lines is invalid; treating as true
# Subtest: LW1 inserts an unlabelled LINKS line in the empty slot
ok 2710 - LW1 inserts an unlabelled LINKS line in the empty slot
  ---
  duration_ms: 2.51435
  ...
# Subtest: LW2 appends a labelled entry and LW3 is a byte-identical no-op
ok 2711 - LW2 appends a labelled entry and LW3 is a byte-identical no-op
  ---
  duration_ms: 1.388831
  ...
# Subtest: LW4 relabels in place and LW5/LW6 remove entries
ok 2712 - LW4 relabels in place and LW5/LW6 remove entries
  ---
  duration_ms: 0.803173
  ...
# Subtest: LW7 places LINKS after Sub-projects and LINKED FROM after LINKS
ok 2713 - LW7 places LINKS after Sub-projects and LINKED FROM after LINKS
  ---
  duration_ms: 1.600926
  ...
# Subtest: LW8 inserts LINKS as the first child when only user children exist
ok 2714 - LW8 inserts LINKS as the first child when only user children exist
  ---
  duration_ms: 0.374936
  ...
# Subtest: LW9 merges duplicate LINKS lines with first label winning
ok 2715 - LW9 merges duplicate LINKS lines with first label winning
  ---
  duration_ms: 0.392159
  ...
# Subtest: LW10 refuses a malformed LINKS line
ok 2716 - LW10 refuses a malformed LINKS line
  ---
  duration_ms: 0.222274
  ...
# Subtest: LW11 normalises and refuses labels
ok 2717 - LW11 normalises and refuses labels
  ---
  duration_ms: 0.59703
  ...
# Subtest: LW12 reuses a 4-space child indent
ok 2718 - LW12 reuses a 4-space child indent
  ---
  duration_ms: 0.320472
  ...
# Subtest: LW13 canonical link forms match Rust
ok 2719 - LW13 canonical link forms match Rust
  ---
  duration_ms: 0.680108
  ...
# Subtest: LW14 / LK20 LINKED FROM sort is byte-identical to Rust
ok 2720 - LW14 / LK20 LINKED FROM sort is byte-identical to Rust
  ---
  duration_ms: 0.396828
  ...
# Subtest: Rule 6 LINKED FROM planner table
ok 2721 - Rule 6 LINKED FROM planner table
  ---
  duration_ms: 1.099659
  ...
# Subtest: linkedFromDesiredAfterDelta keeps labels and sorts
ok 2722 - linkedFromDesiredAfterDelta keeps labels and sorts
  ---
  duration_ms: 0.382841
  ...
# Subtest: LG14 kill switch defaults on, honors false, and invalid values fall back on
ok 2723 - LG14 kill switch defaults on, honors false, and invalid values fall back on
  ---
  duration_ms: 0.954943
  ...
# Subtest: LG1 same-note add mints and writes LINKS plus LINKED FROM in one transaction
ok 2724 - LG1 same-note add mints and writes LINKS plus LINKED FROM in one transaction
  ---
  duration_ms: 3.886299
  ...
# Subtest: LG2 cross-note T follows the source commit; a changed target suffixes the notice
ok 2725 - LG2 cross-note T follows the source commit; a changed target suffixes the notice
  ---
  duration_ms: 1.653938
  ...
# Subtest: LG4 unlinks and relabels in place with the mirror
ok 2726 - LG4 unlinks and relabels in place with the mirror
  ---
  duration_ms: 2.292797
  ...
# Subtest: LG6 archived targets write LINKS without a mirror
ok 2727 - LG6 archived targets write LINKS without a mirror
  ---
  duration_ms: 0.613712
  ...
# Subtest: LG13 relation writes never stamp or change status
ok 2728 - LG13 relation writes never stamp or change status
  ---
  duration_ms: 0.613922
  ...
# Subtest: LG14 kill switch writes LINKS without a mirror or source mint
ok 2729 - LG14 kill switch writes LINKS without a mirror or source mint
  ---
  duration_ms: 0.352152
  ...
# Subtest: api.relations v1: removeLink works and openStage settles false without a plugin
ok 2730 - api.relations v1: removeLink works and openStage settles false without a plugin
  ---
  duration_ms: 2.145907
  ...
# Subtest: createDependencyNavApi mounts relations beside blocks
ok 2731 - createDependencyNavApi mounts relations beside blocks
  ---
  duration_ms: 0.396588
  ...
# Subtest: LG10: hand-edited LINKS mirrors to LINKED FROM and re-fires after undo
ok 2732 - LG10: hand-edited LINKS mirrors to LINKED FROM and re-fires after undo
  ---
  duration_ms: 2.515963
  ...
# Subtest: LG11: hand-editing generated LINKED FROM only shows its notice
ok 2733 - LG11: hand-editing generated LINKED FROM only shows its notice
  ---
  duration_ms: 1.521725
  ...
# Subtest: LG9: Ctrl+D's writer clears outgoing links and their generated mirrors
ok 2734 - LG9: Ctrl+D's writer clears outgoing links and their generated mirrors
  ---
  duration_ms: 1.519991
  ...
# Subtest: Alt+N release from a NEXT landing advances with one composed toast
ok 2735 - Alt+N release from a NEXT landing advances with one composed toast
  ---
  duration_ms: 21.829921
  ...
# Subtest: counted Alt+N lands past every handled key in one jump
ok 2736 - counted Alt+N lands past every handled key in one jump
  ---
  duration_ms: 10.584105
  ...
# Subtest: a cancelled Alt+N release prompt stays and frees the lock
ok 2737 - a cancelled Alt+N release prompt stays and frees the lock
  ---
  duration_ms: 10.845183
  ...
# Subtest: Alt+N on a checklist landing stays with the plain notice
ok 2738 - Alt+N on a checklist landing stays with the plain notice
  ---
  duration_ms: 10.446512
  ...
# Subtest: Alt+N off a landing behaves exactly as today
ok 2739 - Alt+N off a landing behaves exactly as today
  ---
  duration_ms: 11.322485
  ...
# Subtest: Alt+N while the gesture lock is held is swallowed
ok 2740 - Alt+N while the gesture lock is held is swallowed
  ---
  duration_ms: 10.324649
  ...
# Subtest: a Task Card priority commit on NEXT advances, landing after the rich card
ok 2741 - a Task Card priority commit on NEXT advances, landing after the rich card
  ---
  duration_ms: 28.581529
  ...
# Subtest: dismissing the Task Card stays and frees the lock
ok 2742 - dismissing the Task Card stays and frees the lock
  ---
  duration_ms: 13.023792
  ...
# Subtest: a frontmatter-only project edit from the card stays
ok 2743 - a frontmatter-only project edit from the card stays
  ---
  duration_ms: 11.573504
  ...
# Subtest: a same-day priority schedule on a checklist row stays
ok 2744 - a same-day priority schedule on a checklist row stays
  ---
  duration_ms: 12.309427
  ...
# Subtest: a future schedule on a checklist row advances
ok 2745 - a future schedule on a checklist row advances
  ---
  duration_ms: 15.812745
  ...
# Subtest: a Task Card cancel on a checklist row advances with the cancel card first
ok 2746 - a Task Card cancel on a checklist row advances with the cancel card first
  ---
  duration_ms: 12.819442
  ...
# Subtest: Ctrl+Shift+M from a landing follows the task and never advances
ok 2747 - Ctrl+Shift+M from a landing follows the task and never advances
  ---
  duration_ms: 13.665276
  ...
# Subtest: Ctrl+Shift+M from a checklist landing keeps the destination focus
ok 2748 - Ctrl+Shift+M from a checklist landing keeps the destination focus
  ---
  duration_ms: 10.372231
  ...
# Subtest: ]s after a landed move resumes at the successor despite the line shift
ok 2749 - ]s after a landed move resumes at the successor despite the line shift
  ---
  duration_ms: 30.671981
  ...
# Subtest: [s after a landed move resumes at the predecessor
ok 2750 - [s after a landed move resumes at the predecessor
  ---
  duration_ms: 10.412767
  ...
# Subtest: a counted move from a landing resumes past every moved target
ok 2751 - a counted move from a landing resumes past every moved target
  ---
  duration_ms: 10.041538
  ...
# Subtest: counted Ctrl+Shift+M command dispatch preserves a landed move count
ok 2752 - counted Ctrl+Shift+M command dispatch preserves a landed move count
  ---
  duration_ms: 19.513931
  ...
# Subtest: a stale landing is not parked
ok 2753 - a stale landing is not parked
  ---
  duration_ms: 10.38287
  ...
# Subtest: Ctrl+Shift+M while the gesture lock is held is swallowed
ok 2754 - Ctrl+Shift+M while the gesture lock is held is swallowed
  ---
  duration_ms: 0.436744
  ...
# Subtest: dismissing the move picker stays and frees the lock
ok 2755 - dismissing the move picker stays and frees the lock
  ---
  duration_ms: 8.929874
  ...
# Subtest: Ctrl+Shift+M off a landing behaves exactly as today
ok 2756 - Ctrl+Shift+M off a landing behaves exactly as today
  ---
  duration_ms: 9.776665
  ...
# Subtest: answer, move, answer stays in queue order past an accumulator alias
ok 2757 - answer, move, answer stays in queue order past an accumulator alias
  ---
  duration_ms: 3.649667
  ...
# Subtest: a move park ignores a stale accumulator alias
ok 2758 - a move park ignores a stale accumulator alias
  ---
  duration_ms: 0.455951
  ...
# Subtest: a re-indexed origin still advances from the landed row
ok 2759 - a re-indexed origin still advances from the landed row
  ---
  duration_ms: 1.961404
  ...
# Subtest: a landed move park clears the current review task
ok 2760 - a landed move park clears the current review task
  ---
  duration_ms: 0.351972
  ...
# Subtest: predicate: reviewOutcomeResolves across tiers and kinds
ok 2761 - predicate: reviewOutcomeResolves across tiers and kinds
  ---
  duration_ms: 3.025334
  ...
# Subtest: findReviewResumeIndex identifies rows by path and text
ok 2762 - findReviewResumeIndex identifies rows by path and text
  ---
  duration_ms: 0.402579
  ...
# Subtest: buildReviewMoveAnchor parks text-identified resume neighbours
ok 2763 - buildReviewMoveAnchor parks text-identified resume neighbours
  ---
  duration_ms: 0.763127
  ...
# Subtest: planReviewJump with a move anchor resumes at the walk neighbour
ok 2764 - planReviewJump with a move anchor resumes at the walk neighbour
  ---
  duration_ms: 1.428497
  ...
# Subtest: capture: null off a landing
ok 2765 - capture: null off a landing
  ---
  duration_ms: 4.438864
  ...
# Subtest: capture: frozen origin shape, BUSY while locked, expiry
ok 2766 - capture: frozen origin shape, BUSY while locked, expiry
  ---
  duration_ms: 0.698003
  ...
# Subtest: successor picker keeps a captured completion locked through selection and one walk toast
ok 2767 - successor picker keeps a captured completion locked through selection and one walk toast
  ---
  duration_ms: 17.442065
  ...
# Subtest: continue: refuses stale origins, showing the notice once
ok 2768 - continue: refuses stale origins, showing the notice once
  ---
  duration_ms: 7.231305
  ...
# Subtest: continue: stays on null and non-resolving outcomes
ok 2769 - continue: stays on null and non-resolving outcomes
  ---
  duration_ms: 1.507878
  ...
# Subtest: continue: stays for lane answers and mixed-version completes on checklist rows
ok 2770 - continue: stays for lane answers and mixed-version completes on checklist rows
  ---
  duration_ms: 2.461228
  ...
# Subtest: continue: a resolving lane answer advances exactly once with one composed toast
ok 2771 - continue: a resolving lane answer advances exactly once with one composed toast
  ---
  duration_ms: 2.739779
  ...
# Subtest: continue: counted handled refs land past every handled key in one jump
ok 2772 - continue: counted handled refs land past every handled key in one jump
  ---
  duration_ms: 1.425662
  ...
# Subtest: continue: wrap is announced and the empty queue composes the empty notice
ok 2773 - continue: wrap is announced and the empty queue composes the empty notice
  ---
  duration_ms: 3.88609
  ...
# Subtest: continue: anchor-only planning survives cursor drift and lagging queues
ok 2774 - continue: anchor-only planning survives cursor drift and lagging queues
  ---
  duration_ms: 2.131259
  ...
# Subtest: continue: POST origins never wrap
ok 2775 - continue: POST origins never wrap
  ---
  duration_ms: 2.218354
  ...
# Subtest: complete: the last lane row before POST stays with the next-step toast
ok 2776 - complete: the last lane row before POST stays with the next-step toast
  ---
  duration_ms: 1.835553
  ...
# Subtest: complete: a wrap onto a skipped PRE row stays
ok 2777 - complete: a wrap onto a skipped PRE row stays
  ---
  duration_ms: 1.962677
  ...
# Subtest: complete: a step into ROTTEN shows the boundary line
ok 2778 - complete: a step into ROTTEN shows the boundary line
  ---
  duration_ms: 2.203246
  ...
# Subtest: busy: walk keys, refresh, claim, and capture are swallowed in the settle window
ok 2779 - busy: walk keys, refresh, claim, and capture are swallowed in the settle window
  ---
  duration_ms: 2.342472
  ...
# Subtest: advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
ok 2780 - advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
  ---
  duration_ms: 3.475134
  ...
# Subtest: advance: decay choices advance except reword, with no preamble of their own
ok 2781 - advance: decay choices advance except reword, with no preamble of their own
  ---
  duration_ms: 0.580538
  ...
# Subtest: jump history: same-note and cross-note auto-advances record, and <C-o> returns
ok 2782 - jump history: same-note and cross-note auto-advances record, and <C-o> returns
  ---
  duration_ms: 7.118959
  ...
# Subtest: jump history: a manual ]s also records its landing
ok 2783 - jump history: a manual ]s also records its landing
  ---
  duration_ms: 2.76584
  ...
# Subtest: api: reviewWalk v3 is frozen with version 1, degrades null, never throws
ok 2784 - api: reviewWalk v3 is frozen with version 1, degrades null, never throws
  ---
  duration_ms: 1.901461
  ...
# Subtest: walk identity: a stale accumulator key never moves the anchor
ok 2785 - walk identity: a stale accumulator key never moves the anchor
  ---
  duration_ms: 0.280144
  ...
# Subtest: walk identity: a lagging answered row stays excluded
ok 2786 - walk identity: a lagging answered row stays excluded
  ---
  duration_ms: 0.153192
  ...
# Subtest: walk identity: a line-shifting answer lands on the true successor by text
ok 2787 - walk identity: a line-shifting answer lands on the true successor by text
  ---
  duration_ms: 0.237513
  ...
# Subtest: walk identity: legacy anchors without text resolve as before
ok 2788 - walk identity: legacy anchors without text resolve as before
  ---
  duration_ms: 0.247492
  ...
# Subtest: walk identity: matchFreshStampRefs prefers text over line
ok 2789 - walk identity: matchFreshStampRefs prefers text over line
  ---
  duration_ms: 0.133605
  ...
# Subtest: walk identity: collectReviewAnswerKeys separates position from exclusion
ok 2790 - walk identity: collectReviewAnswerKeys separates position from exclusion
  ---
  duration_ms: 0.381889
  ...
# Subtest: return: planReviewWalkReturn pure decisions
ok 2791 - return: planReviewWalkReturn pure decisions
  ---
  duration_ms: 0.285936
  ...
# Subtest: return: same-note ]s returns then steps, both directions
ok 2792 - return: same-note ]s returns then steps, both directions
  ---
  duration_ms: 0.990951
  ...
# Subtest: return: a different due row returns instead of stepping from there
ok 2793 - return: a different due row returns instead of stepping from there
  ---
  duration_ms: 0.442144
  ...
# Subtest: return: cross-note return re-arms and records <C-o>
ok 2794 - return: cross-note return re-arms and records <C-o>
  ---
  duration_ms: 3.048799
  ...
# Subtest: return: a count is consumed and ignored
ok 2795 - return: a count is consumed and ignored
  ---
  duration_ms: 0.668957
  ...
# Subtest: return: endpoints never return
ok 2796 - return: endpoints never return
  ---
  duration_ms: 0.53981
  ...
# Subtest: return: its own stamp ends it
ok 2797 - return: its own stamp ends it
  ---
  duration_ms: 0.959001
  ...
# Subtest: return: a stamp elsewhere does not end it
ok 2798 - return: a stamp elsewhere does not end it
  ---
  duration_ms: 0.635954
  ...
# Subtest: return: answers move the current task, a stopped Ctrl+Enter clears it
ok 2799 - return: answers move the current task, a stopped Ctrl+Enter clears it
  ---
  duration_ms: 3.385171
  ...
# Subtest: return: a stale landing falls through in the same press
ok 2800 - return: a stale landing falls through in the same press
  ---
  duration_ms: 0.281557
  ...
# Subtest: return: a day change never returns
ok 2801 - return: a day change never returns
  ---
  duration_ms: 0.387098
  ...
# Subtest: predicate: reviewOutcomeResolves for the RECURRING resolution table
ok 2802 - predicate: reviewOutcomeResolves for the RECURRING resolution table
  ---
  duration_ms: 0.443787
  ...
# Subtest: recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
ok 2803 - recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
  ---
  duration_ms: 0.189612
  ...
# Subtest: return: a RECURRING landing rearms the current-task return
ok 2804 - return: a RECURRING landing rearms the current-task return
  ---
  duration_ms: 0.292428
  ...
# Subtest: review answer outcome vectors map to the schema vocabulary
ok 2805 - review answer outcome vectors map to the schema vocabulary
  ---
  duration_ms: 1.282979
  ...
# Subtest: event builder uses the walk row key and its tier, once per distinct key
ok 2806 - event builder uses the walk row key and its tier, once per distinct key
  ---
  duration_ms: 0.842508
  ...
# Subtest: journal appends are queued and failures retain events without failing answers
ok 2807 - journal appends are queued and failures retain events without failing answers
  ---
  duration_ms: 5.540617
  ...
# Subtest: card after-line outcomes map done, drop, defer, sequence, and card
ok 2808 - card after-line outcomes map done, drop, defer, sequence, and card
  ---
  duration_ms: 1.056768
  ...
# Subtest: journal events carry plugin@manifest version with a 2.x fallback
ok 2809 - journal events carry plugin@manifest version with a 2.x fallback
  ---
  duration_ms: 1.041339
  ...
# Subtest: write failures show one notice per burst and a recovery notice
ok 2810 - write failures show one notice per burst and a recovery notice
  ---
  duration_ms: 0.956807
  ...
# Subtest: missing api.stats shows one session notice and later delivers retained events
ok 2811 - missing api.stats shows one session notice and later delivers retained events
  ---
  duration_ms: 1.36157
  ...
# Subtest: validation rejects drop the event and continue the drain
ok 2812 - validation rejects drop the event and continue the drain
  ---
  duration_ms: 0.868297
  ...
# Subtest: pending journal events cap at 500 and warn once per burst
ok 2813 - pending journal events cap at 500 and warn once per burst
  ---
  duration_ms: 2.474543
  ...
# Subtest: decay config defaults to enabled with one roll per level
ok 2814 - decay config defaults to enabled with one roll per level
  ---
  duration_ms: 3.312222
  ...
# Subtest: decay:false disables decay and level rolls are accepted but ignored
ok 2815 - decay:false disables decay and level rolls are accepted but ignored
  ---
  duration_ms: 0.690708
  ...
# Subtest: decay.rolls sets the limit and levels[].rolls overrides it
ok 2816 - decay.rolls sets the limit and levels[].rolls overrides it
  ---
  duration_ms: 0.271518
  ...
# Subtest: decay config rejects bad rolls, unknown keys and non-priority use
ok 2817 - decay config rejects bad rolls, unknown keys and non-priority use
  ---
  duration_ms: 0.586419
  ...
# Subtest: classifyScheduleLogRollReason sorts automatic heads from deliberate ones
ok 2818 - classifyScheduleLogRollReason sorts automatic heads from deliberate ones
  ---
  duration_ms: 0.808844
  ...
# Subtest: conformance vectors 1-10: streaks at P2 with the default limit
ok 2819 - conformance vectors 1-10: streaks at P2 with the default limit
  ---
  duration_ms: 3.356408
  ...
# Subtest: conformance vectors 11-15: custom limits, disabled decay and edges
ok 2820 - conformance vectors 11-15: custom limits, disabled decay and edges
  ---
  duration_ms: 0.990882
  ...
# Subtest: the streak reader follows log grammar: legacy labels, nesting and stops
ok 2821 - the streak reader follows log grammar: legacy labels, nesting and stops
  ---
  duration_ms: 0.520092
  ...
# Subtest: rollPriorityRecommendationDate avoids the current date when the window has room
ok 2822 - rollPriorityRecommendationDate avoids the current date when the window has room
  ---
  duration_ms: 0.6127
  ...
# Subtest: decay and cancel reason formatters use the exact ladder copy
ok 2823 - decay and cancel reason formatters use the exact ladder copy
  ---
  duration_ms: 0.483052
  ...
# Subtest: the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
ok 2824 - the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
  ---
  duration_ms: 0.316505
  ...
# Subtest: the planner returns null without a configured priority
ok 2825 - the planner returns null without a configured priority
  ---
  duration_ms: 0.159184
  ...
# Subtest: buildPriorityRollPreviewModel carries the row copy for every kind
ok 2826 - buildPriorityRollPreviewModel carries the row copy for every kind
  ---
  duration_ms: 0.474395
  ...
# Subtest: picker-single recognizes the recommended-roll keypress
ok 2827 - picker-single recognizes the recommended-roll keypress
  ---
  duration_ms: 0.128105
  ...
# Subtest: picker-single stage-two footers carry the recommended-roll hints
ok 2828 - picker-single stage-two footers carry the recommended-roll hints
  ---
  duration_ms: 0.281167
  ...
# Subtest: picker-single shares one roll between the preview and the pinned row
ok 2829 - picker-single shares one roll between the preview and the pinned row
  ---
  duration_ms: 0.32981
  ...
# Subtest: picker-single plans the next-roll hint for the notice chips
ok 2830 - picker-single plans the next-roll hint for the notice chips
  ---
  duration_ms: 0.546965
  ...
# Subtest: picker-single notice cards name the roll, decay and next press
ok 2831 - picker-single notice cards name the roll, decay and next press
  ---
  duration_ms: 1.470597
  ...
# Subtest: picker-single decay payload and preview-target comparison
ok 2832 - picker-single decay payload and preview-target comparison
  ---
  duration_ms: 0.309801
  ...
# Subtest: picker-counted plans one recommendation per target with skips
ok 2833 - picker-counted plans one recommendation per target with skips
  ---
  duration_ms: 1.736835
  ...
# Subtest: picker-counted batch preview, footer and notice copy
ok 2834 - picker-counted batch preview, footer and notice copy
  ---
  duration_ms: 1.457072
  ...
# Subtest: picker-counted composes cancel then set-priority into one postimage
ok 2835 - picker-counted composes cancel then set-priority into one postimage
  ---
  duration_ms: 3.162227
  ...
# Subtest: picker-counted refuses a recurring cancel as one batch
ok 2836 - picker-counted refuses a recurring cancel as one batch
  ---
  duration_ms: 0.397519
  ...
# Subtest: recommended roll recovers with [unblocked::] when the writer is passed
ok 2837 - recommended roll recovers with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.763277
  ...
# Subtest: picker-counted stale lines refuse and new options stay byte-identical
ok 2838 - picker-counted stale lines refuse and new options stay byte-identical
  ---
  duration_ms: 1.00068
  ...
# Subtest: picker-links aggregates one recommendation per note
ok 2839 - picker-links aggregates one recommendation per note
  ---
  duration_ms: 1.021019
  ...
# Subtest: picker-links refuses a recurring cancel as one batch
ok 2840 - picker-links refuses a recurring cancel as one batch
  ---
  duration_ms: 0.379575
  ...
# Subtest: picker-links takes a single recommended roll with Ctrl+Enter
ok 2841 - picker-links takes a single recommended roll with Ctrl+Enter
  ---
  duration_ms: 30.759739
  ...
# Subtest: picker-links shows no pinned roll row in stage two
ok 2842 - picker-links shows no pinned roll row in stage two
  ---
  duration_ms: 5.283206
  ...
# Subtest: picker-links decays and cancels a single Task Link
ok 2843 - picker-links decays and cancels a single Task Link
  ---
  duration_ms: 6.617641
  ...
# Subtest: picker-links applies a mixed batch across two notes
ok 2844 - picker-links applies a mixed batch across two notes
  ---
  duration_ms: 4.6883
  ...
# Subtest: picker-links refuses the whole batch when a linked note changed
ok 2845 - picker-links refuses the whole batch when a linked note changed
  ---
  duration_ms: 1.774177
  ...
# Subtest: picker-links prunes today's open Pomodoro links
ok 2846 - picker-links prunes today's open Pomodoro links
  ---
  duration_ms: 4.270242
  ...
# Subtest: picker-single Ctrl+Enter rolls a P2 task in one undo group
ok 2847 - picker-single Ctrl+Enter rolls a P2 task in one undo group
  ---
  duration_ms: 18.069434
  ...
# Subtest: picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
ok 2848 - picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
  ---
  duration_ms: 11.752474
  ...
# Subtest: picker-single opens a ^prj task on inline scheduled for an immediate roll
ok 2849 - picker-single opens a ^prj task on inline scheduled for an immediate roll
  ---
  duration_ms: 13.630641
  ...
# Subtest: picker-counted opens on scheduled for an immediate mixed batch
ok 2850 - picker-counted opens on scheduled for an immediate mixed batch
  ---
  duration_ms: 13.621082
  ...
# Subtest: picker-links opens on scheduled for an immediate roll
ok 2851 - picker-links opens on scheduled for an immediate roll
  ---
  duration_ms: 11.58267
  ...
# Subtest: picker-single Ctrl+Enter decays a P2 task in one undo group
ok 2852 - picker-single Ctrl+Enter decays a P2 task in one undo group
  ---
  duration_ms: 12.492488
  ...
# Subtest: picker-single Ctrl+Enter cancels a P4 task in one undo group
ok 2853 - picker-single Ctrl+Enter cancels a P4 task in one undo group
  ---
  duration_ms: 12.098304
  ...
# Subtest: picker-single Ctrl+Enter in stage two writes the recommended roll
ok 2854 - picker-single Ctrl+Enter in stage two writes the recommended roll
  ---
  duration_ms: 12.374022
  ...
# Subtest: picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
ok 2855 - picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
  ---
  duration_ms: 2.157237
  ...
# Subtest: picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
ok 2856 - picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
  ---
  duration_ms: 8.864502
  ...
# Subtest: picker-single recurring P4 past the limit refuses and keeps the picker open
ok 2857 - picker-single recurring P4 past the limit refuses and keeps the picker open
  ---
  duration_ms: 11.836614
  ...
# Subtest: picker-single stale tasks refuse and re-render the decay preview
ok 2858 - picker-single stale tasks refuse and re-render the decay preview
  ---
  duration_ms: 11.546802
  ...
# Subtest: picker-single Ctrl+R on the card re-rolls the recommendation date
ok 2859 - picker-single Ctrl+R on the card re-rolls the recommendation date
  ---
  duration_ms: 2.537113
  ...
# Subtest: picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
ok 2860 - picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
  ---
  duration_ms: 1.287729
  ...
# Subtest: picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
ok 2861 - picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
  ---
  duration_ms: 11.328093
  ...
# Subtest: picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
ok 2862 - picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
  ---
  duration_ms: 11.598591
  ...
# Subtest: picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
ok 2863 - picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
  ---
  duration_ms: 12.322834
  ...
# Subtest: picker-counted Ctrl+Enter refuses when a target line changed
ok 2864 - picker-counted Ctrl+Enter refuses when a target line changed
  ---
  duration_ms: 12.045112
  ...
# Subtest: picker-counted Ctrl+Enter refuses a recurring cancel batch
ok 2865 - picker-counted Ctrl+Enter refuses a recurring cancel batch
  ---
  duration_ms: 11.475807
  ...
# Subtest: recommended roll on Pending offers a Work Log with the frozen date
ok 2866 - recommended roll on Pending offers a Work Log with the frozen date
  ---
  duration_ms: 1018.105362
  ...
# Subtest: recommended roll blank summary skips the Work Log without a fallback
ok 2867 - recommended roll blank summary skips the Work Log without a fallback
  ---
  duration_ms: 1023.327902
  ...
# Subtest: Ctrl+Enter in the Work Log stage confirms instead of re-rolling
ok 2868 - Ctrl+Enter in the Work Log stage confirms instead of re-rolling
  ---
  duration_ms: 1033.08172
  ...
# Subtest: counted recommended mixed batch logs only eligible roll and decay targets
ok 2869 - counted recommended mixed batch logs only eligible roll and decay targets
  ---
  duration_ms: 1027.069494
  ...
# Subtest: Task Link recommended roll deletes the emptied Pomodoro in the same daily write
ok 2870 - Task Link recommended roll deletes the emptied Pomodoro in the same daily write
  ---
  duration_ms: 2.711546
  ...
# Subtest: lane commit stamps an open Ready task
ok 2871 - lane commit stamps an open Ready task
  ---
  duration_ms: 2.561691
  ...
# Subtest: lane release stamps an open Next task
ok 2872 - lane release stamps an open Next task
  ---
  duration_ms: 0.406736
  ...
# Subtest: lane without a stamper leaves lines as they were
ok 2873 - lane without a stamper leaves lines as they were
  ---
  duration_ms: 0.178371
  ...
# Subtest: counted property set stamps every rewritten open task
ok 2874 - counted property set stamps every rewritten open task
  ---
  duration_ms: 2.040014
  ...
# Subtest: counted delete-property stamps the rewritten task
ok 2875 - counted delete-property stamps the rewritten task
  ---
  duration_ms: 0.500505
  ...
# Subtest: stamp lands before the suffix after a priority edit on a stamped line
ok 2876 - stamp lands before the suffix after a priority edit on a stamped line
  ---
  duration_ms: 0.476479
  ...
# Subtest: recurring tasks are never stamped
ok 2877 - recurring tasks are never stamped
  ---
  duration_ms: 0.246701
  ...
# Subtest: cancel never stamps
ok 2878 - cancel never stamps
  ---
  duration_ms: 1.01132
  ...
# Subtest: fresh and refresh never go through the end-append writers
ok 2879 - fresh and refresh never go through the end-append writers
  ---
  duration_ms: 0.410344
  ...
# Subtest: counted dependency edit stamps the rewritten parent
ok 2880 - counted dependency edit stamps the rewritten parent
  ---
  duration_ms: 4.701264
  ...
# Subtest: moved tasks are stamped at their destination
ok 2881 - moved tasks are stamped at their destination
  ---
  duration_ms: 2.515802
  ...
# Subtest: move without a stamper leaves lines as they were
ok 2882 - move without a stamper leaves lines as they were
  ---
  duration_ms: 0.547866
  ...
# Subtest: refresh row shows the effective interval in task mode
ok 2883 - refresh row shows the effective interval in task mode
  ---
  duration_ms: 0.736877
  ...
# Subtest: refresh row hides without the api and on closed tasks
ok 2884 - refresh row hides without the api and on closed tasks
  ---
  duration_ms: 0.118857
  ...
# Subtest: refresh row covers counted and link modes, including mixed
ok 2885 - refresh row covers counted and link modes, including mixed
  ---
  duration_ms: 0.251811
  ...
# Subtest: refresh value items offer presets and use default
ok 2886 - refresh value items offer presets and use default
  ---
  duration_ms: 0.709825
  ...
# Subtest: setRefreshLine stamps and sets or clears the interval
ok 2887 - setRefreshLine stamps and sets or clears the interval
  ---
  duration_ms: 0.37691
  ...
# Subtest: 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
ok 2888 - 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
  ---
  duration_ms: 6.534074
  ...
# Subtest: Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
ok 2889 - Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
  ---
  duration_ms: 3.913752
  ...
# Subtest: filtering expands matches, collapse state survives clearing, and hidden marks still submit
ok 2890 - filtering expands matches, collapse state survives clearing, and hidden marks still submit
  ---
  duration_ms: 3.290581
  ...
# Subtest: group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
ok 2891 - group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
  ---
  duration_ms: 4.495742
  ...
# Subtest: Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
ok 2892 - Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
  ---
  duration_ms: 0.664519
  ...
# Subtest: Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
ok 2893 - Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
  ---
  duration_ms: 1.060535
  ...
# Subtest: the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
ok 2894 - the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
  ---
  duration_ms: 0.556463
  ...
# Subtest: destination override shapes normalize and label
ok 2895 - destination override shapes normalize and label
  ---
  duration_ms: 0.2253
  ...
# Subtest: destination picker detection needs block-id-prompt api v1 with pick
ok 2896 - destination picker detection needs block-id-prompt api v1 with pick
  ---
  duration_ms: 0.373724
  ...
# Subtest: Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks
ok 2897 - Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks
  ---
  duration_ms: 1.646163
  ...
# Subtest: Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked
ok 2898 - Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked
  ---
  duration_ms: 0.844111
  ...
# Subtest: a cancelled destination pick and a missing picker leave rows untouched
ok 2899 - a cancelled destination pick and a missing picker leave rows untouched
  ---
  duration_ms: 0.887033
  ...
# Subtest: unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
ok 2900 - unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
  ---
  duration_ms: 0.58697
  ...
# Subtest: card model builds stable rows, scope metadata, and an existing recommendation
ok 2901 - card model builds stable rows, scope metadata, and an existing recommendation
  ---
  duration_ms: 8.652868
  ...
# Subtest: explicit preview builder matches writer rolls and deduplicates linked targets
ok 2902 - explicit preview builder matches writer rolls and deduplicates linked targets
  ---
  duration_ms: 0.830304
  ...
# Subtest: counted and linked card models report real target counts and mixed values
ok 2903 - counted and linked card models report real target counts and mixed values
  ---
  duration_ms: 4.236959
  ...
# Subtest: priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
ok 2904 - priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
  ---
  duration_ms: 2.304048
  ...
# Subtest: Escape, bare q, and Ctrl+[ close the card; nothing else does
ok 2905 - Escape, bare q, and Ctrl+[ close the card; nothing else does
  ---
  duration_ms: 0.946757
  ...
# Subtest: close keys never fire during composition or inside a text field
ok 2906 - close keys never fire during composition or inside a text field
  ---
  duration_ms: 1.347703
  ...
# Subtest: unavailable actions, input composition, and repeats stay safe
ok 2907 - unavailable actions, input composition, and repeats stay safe
  ---
  duration_ms: 2.046467
  ...
# Subtest: Blocks row summarizes warm-cache dependents and their last open reason
ok 2908 - Blocks row summarizes warm-cache dependents and their last open reason
  ---
  duration_ms: 1.170454
  ...
# Subtest: Blocks row refuses closed tasks and unencodable paths without an id
ok 2909 - Blocks row refuses closed tasks and unencodable paths without an id
  ---
  duration_ms: 2.160084
  ...
# Subtest: key resolver table covers lane state, API availability, and modifier guards
ok 2910 - key resolver table covers lane state, API availability, and modifier guards
  ---
  duration_ms: 1.587691
  ...
# Subtest: recurring cancellation and blocked lanes expose reasons instead of writes
ok 2911 - recurring cancellation and blocked lanes expose reasons instead of writes
  ---
  duration_ms: 0.908945
  ...
# Subtest: identity keys distinguish linked notes that share a line number
ok 2912 - identity keys distinguish linked notes that share a line number
  ---
  duration_ms: 1.978518
  ...
# Subtest: planScheduleReview opens for a bare date and skips when reason is known without Work Log
ok 2913 - planScheduleReview opens for a bare date and skips when reason is known without Work Log
  ---
  duration_ms: 0.923704
  ...
# Subtest: planScheduleReview counts unique tasks when Task Links repeat a target
ok 2914 - planScheduleReview counts unique tasks when Task Links repeat a target
  ---
  duration_ms: 0.334589
  ...
# Subtest: bare date on Ready opens a reason-only review and writes nothing until Enter
ok 2915 - bare date on Ready opens a reason-only review and writes nothing until Enter
  ---
  duration_ms: 20.577151
  ...
# Subtest: typed reason and blank reason on an existing Schedule Log keep per-target rules
ok 2916 - typed reason and blank reason on an existing Schedule Log keep per-target rules
  ---
  duration_ms: 9.705255
  ...
# Subtest: Ready vs Next vs Pending: only Next/Pending show Work summary
ok 2917 - Ready vs Next vs Pending: only Next/Pending show Work summary
  ---
  duration_ms: 9.839113
  ...
# Subtest: inline reason on Ready dispatches immediately; on Next it still reviews Work summary
ok 2918 - inline reason on Ready dispatches immediately; on Next it still reviews Work summary
  ---
  duration_ms: 4.644757
  ...
# Subtest: Tab moves from Reason to Work summary and Enter commits from either field
ok 2919 - Tab moves from Reason to Work summary and Enter commits from either field
  ---
  duration_ms: 4.423385
  ...
# Subtest: Back and Escape at both review fields write nothing
ok 2920 - Back and Escape at both review fields write nothing
  ---
  duration_ms: 4.155742
  ...
# Subtest: a target changed during review refuses with no write
ok 2921 - a target changed during review refuses with no write
  ---
  duration_ms: 1.945353
  ...
# Subtest: counted mixed targets share one review and one adapter call
ok 2922 - counted mixed targets share one review and one adapter call
  ---
  duration_ms: 3.419127
  ...
# Subtest: linked notes with equal line numbers both qualify
ok 2923 - linked notes with equal line numbers both qualify
  ---
  duration_ms: 2.682511
  ...
# Subtest: project lifecycle review names propagation and still writes once
ok 2924 - project lifecycle review names propagation and still writes once
  ---
  duration_ms: 2.150605
  ...
# Subtest: priority picks still skip the combined review and keep Work Log-only prompts
ok 2925 - priority picks still skip the combined review and keep Work Log-only prompts
  ---
  duration_ms: 1.902832
  ...
# Subtest: a typed date from the card's schedule row uses the combined review
ok 2926 - a typed date from the card's schedule row uses the combined review
  ---
  duration_ms: 1.657975
  ...
# Subtest: scheduling a Pending task goes straight to the combined review, never serial prompts
ok 2927 - scheduling a Pending task goes straight to the combined review, never serial prompts
  ---
  duration_ms: 1.305001
  ...
# Subtest: classic parser keeps ISO, M/D, and signed units and ignores concise forms
ok 2928 - classic parser keeps ISO, M/D, and signed units and ignores concise forms
  ---
  duration_ms: 1.363593
  ...
# Subtest: typed schedule resolver covers bare days, units, weekdays, and inline reasons
ok 2929 - typed schedule resolver covers bare days, units, weekdays, and inline reasons
  ---
  duration_ms: 1.129185
  ...
# Subtest: weekdays resolve to the next occurrence strictly after today
ok 2930 - weekdays resolve to the next occurrence strictly after today
  ---
  duration_ms: 0.145999
  ...
# Subtest: invalid leap dates, end-of-month offsets, and December rollover
ok 2931 - invalid leap dates, end-of-month offsets, and December rollover
  ---
  duration_ms: 0.360307
  ...
# Subtest: negative, overflow, malformed, and preset-filter queries are rejected without dates
ok 2932 - negative, overflow, malformed, and preset-filter queries are rejected without dates
  ---
  duration_ms: 0.171207
  ...
# Subtest: DST local-calendar arithmetic stays on calendar days in America/New_York
ok 2933 - DST local-calendar arithmetic stays on calendar days in America/New_York
  ---
  duration_ms: 97.197634
  ...
# Subtest: Task Card date stage previews weekday, ISO, relative distance, and rollover year
ok 2934 - Task Card date stage previews weekday, ISO, relative distance, and rollover year
  ---
  duration_ms: 14.842213
  ...
# Subtest: inline reason is preserved on the preview and skips the reason stage
ok 2935 - inline reason is preserved on the preview and skips the reason stage
  ---
  duration_ms: 11.427083
  ...
# Subtest: Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
ok 2936 - Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
  ---
  duration_ms: 4.643784
  ...
# Subtest: Shift+Enter on a Ready task commits in four gestures without a Work Log
ok 2937 - Shift+Enter on a Ready task commits in four gestures without a Work Log
  ---
  duration_ms: 2.421081
  ...
# Subtest: invalid typed dates render an error preview and do not write
ok 2938 - invalid typed dates render an error preview and do not write
  ---
  duration_ms: 3.931115
  ...
# Subtest: the card's schedule stage always uses the concise resolver
ok 2939 - the card's schedule stage always uses the concise resolver
  ---
  duration_ms: 1.334097
  ...
# Subtest: tomorrow stays a preset filter and is not stolen as a typed date
ok 2940 - tomorrow stays a preset filter and is not stolen as a typed date
  ---
  duration_ms: 1.12079
  ...
# Subtest: mixed Task Links preview one date and freeze that action with the inline reason
ok 2941 - mixed Task Links preview one date and freeze that action with the inline reason
  ---
  duration_ms: 4.170911
  ...
# Subtest: Ctrl+Enter still takes the recommended roll from the Task Card date stage
ok 2942 - Ctrl+Enter still takes the recommended roll from the Task Card date stage
  ---
  duration_ms: 2.317404
  ...
# Subtest: Modal harness models Obsidian 1.14 attachment and idempotent close
ok 2943 - Modal harness models Obsidian 1.14 attachment and idempotent close
  ---
  duration_ms: 1.525021
  ...
# Subtest: styles share key-card tokens and compact Task Card dimensions
ok 2944 - styles share key-card tokens and compact Task Card dimensions
  ---
  duration_ms: 0.304832
  ...
# Subtest: card renderer paints header, banner, strip, stable rows, more, and footer from the model
ok 2945 - card renderer paints header, banner, strip, stable rows, more, and footer from the model
  ---
  duration_ms: 11.197115
  ...
# Subtest: renderer does not consume randomness or invent recommendation data
ok 2946 - renderer does not consume randomness or invent recommendation data
  ---
  duration_ms: 1.957436
  ...
# Subtest: no-recommendation, cancel, mixed, long text, missing API, and error states render
ok 2947 - no-recommendation, cancel, mixed, long text, missing API, and error states render
  ---
  duration_ms: 11.394863
  ...
# Subtest: counted and linked cards disclose mixed values and Task Link notes
ok 2948 - counted and linked cards disclose mixed values and Task Link notes
  ---
  duration_ms: 5.05515
  ...
# Subtest: Ctrl+Shift+P always opens the Task Card, never the classic property list
ok 2949 - Ctrl+Shift+P always opens the Task Card, never the classic property list
  ---
  duration_ms: 3.411283
  ...
# Subtest: the plugin carries no Task Card pilot setting, date gate, or classic preference
ok 2950 - the plugin carries no Task Card pilot setting, date gate, or classic preference
  ---
  duration_ms: 20.473802
  ...
# Subtest: a leftover persisted taskCard flag is ignored and never rewritten
ok 2951 - a leftover persisted taskCard flag is ignored and never rewritten
  ---
  duration_ms: 9.940105
  ...
# Subtest: palette command is named Task card (set properties)
ok 2952 - palette command is named Task card (set properties)
  ---
  duration_ms: 11.213115
  ...
# Subtest: Task Card opens the compact card with dialog semantics and a close control
ok 2953 - Task Card opens the compact card with dialog semantics and a close control
  ---
  duration_ms: 1.590395
  ...
# Subtest: a More row opens that property's value stage, never a filter list, and Back restores the card
ok 2954 - a More row opens that property's value stage, never a filter list, and Back restores the card
  ---
  duration_ms: 3.568682
  ...
# Subtest: after open the actions list, not the Close button, has focus
ok 2955 - after open the actions list, not the Close button, has focus
  ---
  duration_ms: 7.467085
  ...
# Subtest: clicking card text keeps the card key router active exactly once
ok 2956 - clicking card text keeps the card key router active exactly once
  ---
  duration_ms: 12.817518
  ...
# Subtest: Ready card writes close from a key, P1 click, recommendations, and Alt+N
ok 2957 - Ready card writes close from a key, P1 click, recommendations, and Alt+N
  ---
  duration_ms: 7.006957
  ...
# Subtest: Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
ok 2958 - Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
  ---
  duration_ms: 6.610557
  ...
# Subtest: Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
ok 2959 - Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
  ---
  duration_ms: 10.870121
  ...
# Subtest: Ctrl+R recomputes and repaints the card recommendation
ok 2960 - Ctrl+R recomputes and repaints the card recommendation
  ---
  duration_ms: 1.717619
  ...
# Subtest: Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
ok 2961 - Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
  ---
  duration_ms: 16.026433
  ...
# Subtest: Task Link opens focused while resolving and consumes keys without replay
ok 2962 - Task Link opens focused while resolving and consumes keys without replay
  ---
  duration_ms: 2.953188
  ...
# Subtest: Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card
ok 2963 - Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card
  ---
  duration_ms: 1.582832
  ...
# Subtest: Ctrl+Shift+Alt+B on a Task Link opens the linked Blocks stage
ok 2964 - Ctrl+Shift+Alt+B on a Task Link opens the linked Blocks stage
  ---
  duration_ms: 1.294531
  ...
# Subtest: Task Link count replacement and source edits invalidate old resolutions
ok 2965 - Task Link count replacement and source edits invalidate old resolutions
  ---
  duration_ms: 1.149895
  ...
# Subtest: Task Link resolution failure and plugin unload close their shells
ok 2966 - Task Link resolution failure and plugin unload close their shells
  ---
  duration_ms: 1.752184
  ...
# Subtest: direct Depends on entry opens the dependency stage without painting the card or the list
ok 2967 - direct Depends on entry opens the dependency stage without painting the card or the list
  ---
  duration_ms: 0.868167
  ...
# Subtest: a direct stage for an unconfigured property closes instead of leaving an empty modal
ok 2968 - a direct stage for an unconfigured property closes instead of leaving an empty modal
  ---
  duration_ms: 0.274775
  ...
# Subtest: a refused direct stage closes instead of landing on a card or a list
ok 2969 - a refused direct stage closes instead of landing on a card or a list
  ---
  duration_ms: 0.635944
  ...
# Subtest: Ctrl+Shift+B lands on the Depends on stage with the same intent as card b
ok 2970 - Ctrl+Shift+B lands on the Depends on stage with the same intent as card b
  ---
  duration_ms: 2.365416
  ...
# Subtest: Ctrl+Shift+B Back returns to the card without re-dispatching
ok 2971 - Ctrl+Shift+B Back returns to the card without re-dispatching
  ---
  duration_ms: 1.045156
  ...
# Subtest: Ctrl+Shift+B on a plain bullet notices and closes the card
ok 2972 - Ctrl+Shift+B on a plain bullet notices and closes the card
  ---
  duration_ms: 0.635604
  ...
# Subtest: Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch
ok 2973 - Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch
  ---
  duration_ms: 2.842355
  ...
# Subtest: Ctrl+Shift+Alt+B on Depends-On and BLOCKS lines opens the owner's stage directly
ok 2974 - Ctrl+Shift+Alt+B on Depends-On and BLOCKS lines opens the owner's stage directly
  ---
  duration_ms: 2.3945
  ...
# Subtest: Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not
ok 2975 - Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not
  ---
  duration_ms: 4.403376
  ...
# Subtest: priority gesture writes the frozen date and duplicate dispatch is single-flight
ok 2976 - priority gesture writes the frozen date and duplicate dispatch is single-flight
  ---
  duration_ms: 7.692533
  ...
# Subtest: pending priority action passes its card preview through the Work Log adapter
ok 2977 - pending priority action passes its card preview through the Work Log adapter
  ---
  duration_ms: 1.800557
  ...
# Subtest: Task Link priority action refuses a stale cross-note preflight before writes
ok 2978 - Task Link priority action refuses a stale cross-note preflight before writes
  ---
  duration_ms: 5.132068
  ...
# Subtest: Task Link priority action rolls back earlier note writes after a later write fails
ok 2979 - Task Link priority action rolls back earlier note writes after a later write fails
  ---
  duration_ms: 2.216582
  ...
# Subtest: Task Link transaction reports a cleanup failure without implying global undo
ok 2980 - Task Link transaction reports a cleanup failure without implying global undo
  ---
  duration_ms: 1.109809
  ...
# Subtest: selected-property deletion uses the existing writer; other card rows stay non-deletable
ok 2981 - selected-property deletion uses the existing writer; other card rows stay non-deletable
  ---
  duration_ms: 6.115674
  ...
# Subtest: failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
ok 2982 - failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
  ---
  duration_ms: 1.366869
  ...
# Subtest: a refused deletion rebuilds the card from the refreshed line
ok 2983 - a refused deletion rebuilds the card from the refreshed line
  ---
  duration_ms: 1.421033
  ...
# Subtest: 0 deletes only priority and keeps the scheduled field byte-for-byte
ok 2984 - 0 deletes only priority and keeps the scheduled field byte-for-byte
  ---
  duration_ms: 1.470929
  ...
# Subtest: card keys pressed on a priority radio or the banner reach the resolver exactly once
ok 2985 - card keys pressed on a priority radio or the banner reach the resolver exactly once
  ---
  duration_ms: 2.51398
  ...
# Subtest: held or composing Enter on a radio or the banner never writes
ok 2986 - held or composing Enter on a radio or the banner never writes
  ---
  duration_ms: 1.010309
  ...
# Subtest: Escape, q, Q, and Ctrl+[ close the card without writing
ok 2987 - Escape, q, Q, and Ctrl+[ close the card without writing
  ---
  duration_ms: 2.942056
  ...
# Subtest: Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
ok 2988 - Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
  ---
  duration_ms: 0.726707
  ...
# Subtest: repeated close keys and a second close() are harmless
ok 2989 - repeated close keys and a second close() are harmless
  ---
  duration_ms: 1.03742
  ...
# Subtest: composition never closes the card or a stage
ok 2990 - composition never closes the card or a stage
  ---
  duration_ms: 0.9691
  ...
# Subtest: q typed into a stage's text field never closes the modal
ok 2991 - q typed into a stage's text field never closes the modal
  ---
  duration_ms: 0.755853
  ...
# Subtest: Ctrl+[ closes from a focused date field without writing
ok 2992 - Ctrl+[ closes from a focused date field without writing
  ---
  duration_ms: 0.903374
  ...
# Subtest: Ctrl+[ closes the schedule review from its Reason and Work summary fields
ok 2993 - Ctrl+[ closes the schedule review from its Reason and Work summary fields
  ---
  duration_ms: 5.483629
  ...
# Subtest: Ctrl+[ closes the summary-only schedule-work-log stage without writing
ok 2994 - Ctrl+[ closes the summary-only schedule-work-log stage without writing
  ---
  duration_ms: 1.250026
  ...
# Subtest: Ctrl+[ closes the lane-release Work summary without writing
ok 2995 - Ctrl+[ closes the lane-release Work summary without writing
  ---
  duration_ms: 1.24148
  ...
# Subtest: q closes from a focused More row and from the Close button
ok 2996 - q closes from a focused More row and from the Close button
  ---
  duration_ms: 2.083657
  ...
# Subtest: Ctrl+[ closes from focused card controls, the Back button, and the modal frame
ok 2997 - Ctrl+[ closes from focused card controls, the Back button, and the modal frame
  ---
  duration_ms: 2.902271
  ...
# Subtest: a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
ok 2998 - a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
  ---
  duration_ms: 6.984273
  ...
# Subtest: a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
ok 2999 - a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
  ---
  duration_ms: 5.56258
  ...
# Subtest: a direct dependency stage closes on Ctrl+[ but keeps q as typed text
ok 3000 - a direct dependency stage closes on Ctrl+[ but keeps q as typed text
  ---
  duration_ms: 0.627128
  ...
# Subtest: q and Ctrl+[ are not global closes: other modals and the decay card ignore them
ok 3001 - q and Ctrl+[ are not global closes: other modals and the decay card ignore them
  ---
  duration_ms: 0.826548
  ...
# Subtest: missing freshness API disables Review every with an honest reason
ok 3002 - missing freshness API disables Review every with an honest reason
  ---
  duration_ms: 0.571711
  ...
# Subtest: child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
ok 3003 - child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
  ---
  duration_ms: 0.776643
  ...
# Subtest: decay card keeps its classes and shares key-card tokens
ok 3004 - decay card keeps its classes and shares key-card tokens
  ---
  duration_ms: 0.134237
  ...
# Subtest: decay card footer always names the X drop alias; the trial date is not this gate
ok 3005 - decay card footer always names the X drop alias; the trial date is not this gate
  ---
  duration_ms: 0.219869
  ...
# Subtest: task card level chips reuse the shared priority mark when available
ok 3006 - task card level chips reuse the shared priority mark when available
  ---
  duration_ms: 0.909817
  ...
# Subtest: task card labels are unchanged without the priority mark api
ok 3007 - task card labels are unchanged without the priority mark api
  ---
  duration_ms: 3.26937
  ...
# Subtest: manifest order is authoritative and fragments share one lexical scope
ok 3008 - manifest order is authoritative and fragments share one lexical scope
  ---
  duration_ms: 102.86902
  ...
# Subtest: builds are deterministic and build:check is read-only on success
ok 3009 - builds are deterministic and build:check is read-only on success
  ---
  duration_ms: 178.499465
  ...
# Subtest: read-only check rejects changed fragments and edited generated output
ok 3010 - read-only check rejects changed fragments and edited generated output
  ---
  duration_ms: 150.085203
  ...
# Subtest: check rejects a missing generated bundle without writing it
ok 3011 - check rejects a missing generated bundle without writing it
  ---
  duration_ms: 48.640412
  ...
# Subtest: fragment line limit is enforced before writing output
ok 3012 - fragment line limit is enforced before writing output
  ---
  duration_ms: 1.218656
  ...
# Subtest: fragment syntax errors are rejected before writing output
ok 3013 - fragment syntax errors are rejected before writing output
  ---
  duration_ms: 26.554752
  ...
# Subtest: malformed, empty, duplicate, and traversal manifests are rejected read-only
    # Subtest: invalid JSON
    ok 1 - invalid JSON
      ---
      duration_ms: 0.765601
      ...
    # Subtest: empty manifest
    ok 2 - empty manifest
      ---
      duration_ms: 0.615284
      ...
    # Subtest: non-array manifest
    ok 3 - non-array manifest
      ---
      duration_ms: 0.611998
      ...
    # Subtest: duplicate entries
    ok 4 - duplicate entries
      ---
      duration_ms: 23.451928
      ...
    # Subtest: traversal entry
    ok 5 - traversal entry
      ---
      duration_ms: 0.913224
      ...
    # Subtest: absolute entry
    ok 6 - absolute entry
      ---
      duration_ms: 0.831859
      ...
    1..6
ok 3014 - malformed, empty, duplicate, and traversal manifests are rejected read-only
  ---
  duration_ms: 28.178291
  ...
# Subtest: missing and omitted fragments are rejected read-only
    # Subtest: missing manifest entry
    ok 1 - missing manifest entry
      ---
      duration_ms: 0.795989
      ...
    # Subtest: unlisted JavaScript source
    ok 2 - unlisted JavaScript source
      ---
      duration_ms: 24.169638
      ...
    1..2
ok 3015 - missing and omitted fragments are rejected read-only
  ---
  duration_ms: 25.30244
  ...
# Subtest: escaping fragment symlinks are rejected read-only
ok 3016 - escaping fragment symlinks are rejected read-only
  ---
  duration_ms: 1.110299
  ...
# Subtest: parity comparator identifies changed helper and plugin methods
ok 3017 - parity comparator identifies changed helper and plugin methods
  ---
  duration_ms: 11.280425
  ...
# Subtest: parity comparator accepts a mixin-split helper class but not a changed method or superclass
ok 3018 - parity comparator accepts a mixin-split helper class but not a changed method or superclass
  ---
  duration_ms: 0.677503
  ...
# Subtest: snapshot commands are available only for active Markdown files
ok 3019 - snapshot commands are available only for active Markdown files
  ---
  duration_ms: 1.789796
  ...
# Subtest: commands run bob ref create on the active path, with -C for closed tasks
ok 3020 - commands run bob ref create on the active path, with -C for closed tasks
  ---
  duration_ms: 4.669193
  ...
# Subtest: bob spawn uses the resolved path, vault environment, timeout, and NO_COLOR
ok 3021 - bob spawn uses the resolved path, vault environment, timeout, and NO_COLOR
  ---
  duration_ms: 1.172138
  ...
# Subtest: failure notices retain bob error and hint lines verbatim
ok 3022 - failure notices retain bob error and hint lines verbatim
  ---
  duration_ms: 0.498522
  ...
# Subtest: off desktop, bob spawning is refused with the desktop-app explanation
ok 3023 - off desktop, bob spawning is refused with the desktop-app explanation
  ---
  duration_ms: 0.488963
  ...
# Subtest: both prompt copies pass the shared fixture table identically
ok 3024 - both prompt copies pass the shared fixture table identically
  ---
  duration_ms: 8.725426
  ...
# Subtest: suggestion is valid, compact, and collision-aware
ok 3025 - suggestion is valid, compact, and collision-aware
  ---
  duration_ms: 0.872866
  ...
# Subtest: rename excludes exactly one old-ID occurrence
ok 3026 - rename excludes exactly one old-ID occurrence
  ---
  duration_ms: 0.263994
  ...
# Subtest: dependency legacy [id::] reuses only valid free IDs
ok 3027 - dependency legacy [id::] reuses only valid free IDs
  ---
  duration_ms: 0.493702
  ...
# Subtest: project conversion keeps the existing suggestBlockIdFromTask
ok 3028 - project conversion keeps the existing suggestBlockIdFromTask
  ---
  duration_ms: 1.218296
  ...
# Subtest: successor SB vectors are unchanged
ok 3029 - successor SB vectors are unchanged
  ---
  duration_ms: 0.94836
  ...
# Subtest: Linked-from CURRENT lists every checkbox status from the live index
ok 3030 - Linked-from CURRENT lists every checkbox status from the live index
  ---
  duration_ms: 25.628986
  ...
# Subtest: option-bracket ring reads Blocked as a source-only slot ahead of Ready
ok 3031 - option-bracket ring reads Blocked as a source-only slot ahead of Ready
  ---
  duration_ms: 1.321713
  ...
# Subtest: isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
ok 3032 - isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
  ---
  duration_ms: 0.299501
  ...
# Subtest: option-bracket refuses to change a member while its project is Blocked
ok 3033 - option-bracket refuses to change a member while its project is Blocked
  ---
  duration_ms: 2.59369
  ...
# Subtest: tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
ok 3034 - tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
  ---
  duration_ms: 1.382439
  ...
# Subtest: project resident notice reads the inline ^prj date and ignores frontmatter scheduled
ok 3035 - project resident notice reads the inline ^prj date and ignores frontmatter scheduled
  ---
  duration_ms: 0.522307
  ...
# Subtest: findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
ok 3036 - findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
  ---
  duration_ms: 0.281096
  ...
# Subtest: field removal collapses only the exposed span and preserves the rest of the line
ok 3037 - field removal collapses only the exposed span and preserves the rest of the line
  ---
  duration_ms: 0.250649
  ...
# Subtest: vault-path retirement preserves CRLF and a missing final newline
ok 3038 - vault-path retirement preserves CRLF and a missing final newline
  ---
  duration_ms: 0.874469
  ...
# Subtest: Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
ok 3039 - Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
  ---
  duration_ms: 0.598914
  ...
# Subtest: Schedule Log discovery ignores a marker owned by a nested grandchild
ok 3040 - Schedule Log discovery ignores a marker owned by a nested grandchild
  ---
  duration_ms: 0.513019
  ...
# Subtest: Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
ok 3041 - Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
  ---
  duration_ms: 0.483212
  ...
# Subtest: a task with no Schedule Log gets its field retired without any insertion or new marker
ok 3042 - a task with no Schedule Log gets its field retired without any insertion or new marker
  ---
  duration_ms: 0.133855
  ...
# Subtest: Schedule Log entry uses the canonical arrow, dash, and lock bytes
ok 3043 - Schedule Log entry uses the canonical arrow, dash, and lock bytes
  ---
  duration_ms: 0.095783
  ...
# Subtest: retirement stays a no-op for shapes that are not proof of a blocking date
ok 3044 - retirement stays a no-op for shapes that are not proof of a blocking date
  ---
  duration_ms: 0.165205
  ...
# Subtest: cycling Blocked backward to Cancelled retires the date and logs, matching forward
ok 3045 - cycling Blocked backward to Cancelled retires the date and logs, matching forward
  ---
  duration_ms: 3.891069
  ...
# Subtest: single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
ok 3046 - single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
  ---
  duration_ms: 1.310011
  ...
# Subtest: counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
ok 3047 - counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
  ---
  duration_ms: 1.521885
  ...
# Subtest: counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
ok 3048 - counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
  ---
  duration_ms: 0.720014
  ...
# Subtest: transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
ok 3049 - transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
  ---
  duration_ms: 1.909846
  ...
# Subtest: pressing again after Blocked retirement performs an ordinary transition with no further changes
ok 3050 - pressing again after Blocked retirement performs an ordinary transition with no further changes
  ---
  duration_ms: 0.232273
  ...
# Subtest: Alt+] on a date-blocked ^prj recovers open residents in step
ok 3051 - Alt+] on a date-blocked ^prj recovers open residents in step
  ---
  duration_ms: 14.873532
  ...
# Subtest: Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
ok 3052 - Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
  ---
  duration_ms: 1.344457
  ...
# Subtest: planProjectResidentRecoveryEdits recovers when a cross-note id is not open
ok 3053 - planProjectResidentRecoveryEdits recovers when a cross-note id is not open
  ---
  duration_ms: 0.404593
  ...
# Subtest: Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
ok 3054 - Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
  ---
  duration_ms: 1.287127
  ...
# Subtest: Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
ok 3055 - Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
  ---
  duration_ms: 0.915658
  ...
# Subtest: Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
ok 3056 - Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
  ---
  duration_ms: 1.707249
  ...
# Subtest: cycling a transcluded ^prj recovers residents in the source note
ok 3057 - cycling a transcluded ^prj recovers residents in the source note
  ---
  duration_ms: 1.16255
  ...
# Subtest: cycler BK1–BK12 accept and empty
ok 3058 - cycler BK1–BK12 accept and empty
  ---
  duration_ms: 1.144935
  ...
# Subtest: cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded
ok 3059 - cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded
  ---
  duration_ms: 0.567003
  ...
# Subtest: cycler MC4 strike/restore skip BLOCKS lines
ok 3060 - cycler MC4 strike/restore skip BLOCKS lines
  ---
  duration_ms: 0.804055
  ...
# Subtest: cycler MC3 tree close skips BLOCKS embeds
ok 3061 - cycler MC3 tree close skips BLOCKS embeds
  ---
  duration_ms: 0.881814
  ...
# Subtest: cycler MC1/MC2 Pomodoro and successor scanners skip managed lines
ok 3062 - cycler MC1/MC2 Pomodoro and successor scanners skip managed lines
  ---
  duration_ms: 0.978929
  ...
# Subtest: cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS
ok 3063 - cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS
  ---
  duration_ms: 0.199611
  ...
# Subtest: range planner preserves every single-item mode without an effective count
ok 3064 - range planner preserves every single-item mode without an effective count
  ---
  duration_ms: 7.463238
  ...
# Subtest: item counts carry children, skip blank lines and loose continuations, and clamp
ok 3065 - item counts carry children, skip blank lines and loose continuations, and clamp
  ---
  duration_ms: 0.416725
  ...
# Subtest: range stops at headings, shallower lines, same-level paragraphs and fences
ok 3066 - range stops at headings, shallower lines, same-level paragraphs and fences
  ---
  duration_ms: 0.229729
  ...
# Subtest: siblings require the exact whitespace and blockquote prefix
ok 3067 - siblings require the exact whitespace and blockquote prefix
  ---
  duration_ms: 0.253504
  ...
# Subtest: counted demotion moves four complete blocks to one existing section
ok 3068 - counted demotion moves four complete blocks to one existing section
  ---
  duration_ms: 5.050812
  ...
# Subtest: counted demotion creates a typed section or one default Requirements section
ok 3069 - counted demotion creates a typed section or one default Requirements section
  ---
  duration_ms: 2.674325
  ...
# Subtest: bottom-up removal splices blank seams and maps destinations before the source
ok 3070 - bottom-up removal splices blank seams and maps destinations before the source
  ---
  duration_ms: 0.450029
  ...
# Subtest: counted promotion Enter appends tasks in order and removes an emptied source section
ok 3071 - counted promotion Enter appends tasks in order and removes an emptied source section
  ---
  duration_ms: 0.894898
  ...
# Subtest: counted promotion to existing or new non-Tasks destinations keeps all bullets plain
ok 3072 - counted promotion to existing or new non-Tasks destinations keeps all bullets plain
  ---
  duration_ms: 0.527177
  ...
# Subtest: same-source Tasks promotion rewrites all selected lines in place
ok 3073 - same-source Tasks promotion rewrites all selected lines in place
  ---
  duration_ms: 0.867667
  ...
# Subtest: counted demotion outside Tasks moves to the next section in one write
ok 3074 - counted demotion outside Tasks moves to the next section in one write
  ---
  duration_ms: 0.353124
  ...
# Subtest: in-place ranges write once without centering for nested, non-dash, and unrouted items
ok 3075 - in-place ranges write once without centering for nested, non-dash, and unrouted items
  ---
  duration_ms: 0.791461
  ...
# Subtest: mixed demotion ranges count unchanged siblings and only move top-level dash tasks
ok 3076 - mixed demotion ranges count unchanged siblings and only move top-level dash tasks
  ---
  duration_ms: 0.397058
  ...
# Subtest: mixed promotion preserves existing tasks and a nonempty source section
ok 3077 - mixed promotion preserves existing tasks and a nonempty source section
  ---
  duration_ms: 0.222715
  ...
# Subtest: Vim action consumes explicit additional-item counts and preserves bare behavior
ok 3078 - Vim action consumes explicit additional-item counts and preserves bare behavior
  ---
  duration_ms: 2.572041
  ...
# Subtest: command checking preserves pending count; execution consumes it once and resets Vim
ok 3079 - command checking preserves pending count; execution consumes it once and resets Vim
  ---
  duration_ms: 0.971795
  ...
# Subtest: command route stays single without normal-mode explicit count and supports in-place ranges
ok 3080 - command route stays single without normal-mode explicit count and supports in-place ranges
  ---
  duration_ms: 0.409482
  ...
# Subtest: picker displays at most five preview rows plus overflow; single picker is unchanged
ok 3081 - picker displays at most five preview rows plus overflow; single picker is unchanged
  ---
  duration_ms: 1.139976
  ...
# Subtest: stale counted picker and cancelled picker never write
ok 3082 - stale counted picker and cancelled picker never write
  ---
  duration_ms: 0.752406
  ...
# Subtest: counted moves round-trip CRLF and preserve the presence or absence of a final newline
ok 3083 - counted moves round-trip CRLF and preserve the presence or absence of a final newline
  ---
  duration_ms: 2.997551
  ...
# Subtest: direct open/done transitions include incomplete statuses without broadening excluded statuses
ok 3084 - direct open/done transitions include incomplete statuses without broadening excluded statuses
  ---
  duration_ms: 1.225339
  ...
# Subtest: Ctrl+Enter block-link selection recognizes live and retired forms
ok 3085 - Ctrl+Enter block-link selection recognizes live and retired forms
  ---
  duration_ms: 2.533085
  ...
# Subtest: Pomodoro child ownership is status-neutral and bounded by contiguous list structure
ok 3086 - Pomodoro child ownership is status-neutral and bounded by contiguous list structure
  ---
  duration_ms: 1.046047
  ...
# Subtest: daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
ok 3087 - daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
  ---
  duration_ms: 0.357592
  ...
# Subtest: parsePomodoroEntryLineParts reads placeholder and range names conservatively
ok 3088 - parsePomodoroEntryLineParts reads placeholder and range names conservatively
  ---
  duration_ms: 1.098757
  ...
# Subtest: formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
ok 3089 - formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
  ---
  duration_ms: 0.212777
  ...
# Subtest: Pomodoro bullet toggle accepts empty indented list items
ok 3090 - Pomodoro bullet toggle accepts empty indented list items
  ---
  duration_ms: 0.412057
  ...
# Subtest: Pomodoro bullet toggle rejects non-empty or out-of-section bullets
ok 3091 - Pomodoro bullet toggle rejects non-empty or out-of-section bullets
  ---
  duration_ms: 0.257341
  ...
# Subtest: Pomodoro bullet toggle reverses only empty open childless placeholders
ok 3092 - Pomodoro bullet toggle reverses only empty open childless placeholders
  ---
  duration_ms: 0.656604
  ...
# Subtest: Pomodoro bullet toggle reverses named empty open childless placeholders
ok 3093 - Pomodoro bullet toggle reverses named empty open childless placeholders
  ---
  duration_ms: 0.491859
  ...
# Subtest: Pomodoro bullet toggle round trips and normalizes child indentation
ok 3094 - Pomodoro bullet toggle round trips and normalizes child indentation
  ---
  duration_ms: 0.287348
  ...
# Subtest: Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
ok 3095 - Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
  ---
  duration_ms: 0.203409
  ...
# Subtest: Pomodoro toggle key gate does not shadow bare Option bracket cycling
ok 3096 - Pomodoro toggle key gate does not shadow bare Option bracket cycling
  ---
  duration_ms: 0.218607
  ...
# Subtest: Pomodoro toggle command is daily-only and places the cursor for both directions
ok 3097 - Pomodoro toggle command is daily-only and places the cursor for both directions
  ---
  duration_ms: 0.708553
  ...
# Subtest: Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
ok 3098 - Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
  ---
  duration_ms: 0.319971
  ...
# Subtest: Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
ok 3099 - Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
  ---
  duration_ms: 2.254032
  ...
# Subtest: Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
ok 3100 - Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
  ---
  duration_ms: 23.072004
  ...
# Subtest: Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
ok 3101 - Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
  ---
  duration_ms: 2.039273
  ...
# Subtest: Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
ok 3102 - Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
  ---
  duration_ms: 2.694723
  ...
# Subtest: Ctrl+Enter closing the local line over an already-closed target does not write it a second time
ok 3103 - Ctrl+Enter closing the local line over an already-closed target does not write it a second time
  ---
  duration_ms: 0.72823
  ...
# Subtest: Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
ok 3104 - Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
  ---
  duration_ms: 0.674618
  ...
# Subtest: Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
ok 3105 - Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
  ---
  duration_ms: 1.56644
  ...
# Subtest: Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
ok 3106 - Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
  ---
  duration_ms: 0.489475
  ...
# Subtest: Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
ok 3107 - Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
  ---
  duration_ms: 0.489805
  ...
# Subtest: Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
ok 3108 - Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
  ---
  duration_ms: 0.73855
  ...
# Subtest: Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
ok 3109 - Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
  ---
  duration_ms: 0.577031
  ...
# Subtest: getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
ok 3110 - getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
  ---
  duration_ms: 0.295915
  ...
# Subtest: Ctrl+Enter close continues the walk with complete after finalize ran
ok 3111 - Ctrl+Enter close continues the walk with complete after finalize ran
  ---
  duration_ms: 11.640261
  ...
# Subtest: Ctrl+Enter close continues only after transclusion propagation landed
ok 3112 - Ctrl+Enter close continues only after transclusion propagation landed
  ---
  duration_ms: 12.254743
  ...
# Subtest: Ctrl+Enter reopen settles the walk with null
ok 3113 - Ctrl+Enter reopen settles the walk with null
  ---
  duration_ms: 11.450969
  ...
# Subtest: Ctrl+Enter swallows the key with no write while the walk is busy
ok 3114 - Ctrl+Enter swallows the key with no write while the walk is busy
  ---
  duration_ms: 10.7186
  ...
# Subtest: Ctrl+Enter with a null capture behaves exactly like today
ok 3115 - Ctrl+Enter with a null capture behaves exactly like today
  ---
  duration_ms: 10.95848
  ...
# Subtest: Ctrl+Enter with nav v2 or no nav keeps today's behavior
ok 3116 - Ctrl+Enter with nav v2 or no nav keeps today's behavior
  ---
  duration_ms: 21.410611
  ...
# Subtest: Ctrl+Enter lets the checklist claim win before capturing
ok 3117 - Ctrl+Enter lets the checklist claim win before capturing
  ---
  duration_ms: 0.55551
  ...
# Subtest: Ctrl+Enter settles the walk with null when the toggle rejects
ok 3118 - Ctrl+Enter settles the walk with null when the toggle rejects
  ---
  duration_ms: 11.703842
  ...
# Subtest: Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
ok 3119 - Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
  ---
  duration_ms: 1.569756
  ...
# Subtest: eligible Tasks demotions prompt in project and non-project notes
ok 3120 - eligible Tasks demotions prompt in project and non-project notes
  ---
  duration_ms: 2.841373
  ...
# Subtest: selectable headings skip YAML, fences, empty titles, and Tasks
ok 3121 - selectable headings skip YAML, fences, empty titles, and Tasks
  ---
  duration_ms: 1.019666
  ...
# Subtest: duplicate heading identities stay distinct and route to the chosen occurrence
ok 3122 - duplicate heading identities stay distinct and route to the chosen occurrence
  ---
  duration_ms: 1.125309
  ...
# Subtest: demotion picker defaults and typed names resolve without synthetic duplicates
ok 3123 - demotion picker defaults and typed names resolve without synthetic duplicates
  ---
  duration_ms: 2.097635
  ...
# Subtest: picker keyboard state wraps, clamps, and refuses invalid Enter
ok 3124 - picker keyboard state wraps, clamps, and refuses invalid Enter
  ---
  duration_ms: 0.427886
  ...
# Subtest: new-section formatting keeps extra blanks, final newlines, and nested children
ok 3125 - new-section formatting keeps extra blanks, final newlines, and nested children
  ---
  duration_ms: 0.850734
  ...
# Subtest: existing-section insertion works before and after the source on CRLF-backed editors
ok 3126 - existing-section insertion works before and after the source on CRLF-backed editors
  ---
  duration_ms: 3.159761
  ...
# Subtest: command opens one picker, writes only on accept, and restores cursor plus center
ok 3127 - command opens one picker, writes only on accept, and restores cursor plus center
  ---
  duration_ms: 0.776332
  ...
# Subtest: pointer activation, Escape, and double-submit protection leave a consistent note
ok 3128 - pointer activation, Escape, and double-submit protection leave a consistent note
  ---
  duration_ms: 1.226912
  ...
# Subtest: stale document, changed editor, or missing heading notice without writing
ok 3129 - stale document, changed editor, or missing heading notice without writing
  ---
  duration_ms: 2.317274
  ...
# Subtest: dependency normalizer writes path-qualified IDs and is idempotent
ok 3130 - dependency normalizer writes path-qualified IDs and is idempotent
  ---
  duration_ms: 2.094769
  ...
# Subtest: Tasks-generated IDs become local block IDs when none exists
ok 3131 - Tasks-generated IDs become local block IDs when none exists
  ---
  duration_ms: 0.763888
  ...
# Subtest: note rename rewrites target IDs and yields exact propagation mappings
ok 3132 - note rename rewrites target IDs and yields exact propagation mappings
  ---
  duration_ms: 0.286417
  ...
# Subtest: note rename also rewrites same-file dependsOn references
ok 3133 - note rename also rewrites same-file dependsOn references
  ---
  duration_ms: 0.234357
  ...
# Subtest: dependency normalization skips unsupported paths and fenced examples
ok 3134 - dependency normalization skips unsupported paths and fenced examples
  ---
  duration_ms: 0.344478
  ...
# Subtest: blocked-dependent planner matches the CLI dependency truth table
ok 3135 - blocked-dependent planner matches the CLI dependency truth table
  ---
  duration_ms: 2.621555
  ...
# Subtest: blocked-dependent edits preserve EOLs and skip stale lines idempotently
ok 3136 - blocked-dependent edits preserve EOLs and skip stale lines idempotently
  ---
  duration_ms: 0.797773
  ...
# Subtest: project recovery strips resident tags and works without freshness v12
ok 3137 - project recovery strips resident tags and works without freshness v12
  ---
  duration_ms: 1.389222
  ...
# Subtest: recovery passes daily-note and Today skip flags to ledger freshness
ok 3138 - recovery passes daily-note and Today skip flags to ledger freshness
  ---
  duration_ms: 0.412307
  ...
# Subtest: normalization mappings propagate to every dependent file
ok 3139 - normalization mappings propagate to every dependent file
  ---
  duration_ms: 1.149303
  ...
# Subtest: runtime normalizer skips unsupported paths with one informative notice
ok 3140 - runtime normalizer skips unsupported paths with one informative notice
  ---
  duration_ms: 0.739652
  ...
# Subtest: rename reconciliation rewrites the target and every dependent
ok 3141 - rename reconciliation rewrites the target and every dependent
  ---
  duration_ms: 0.542145
  ...
# Subtest: editor dependency normalization abandons and reschedules stale snapshots
ok 3142 - editor dependency normalization abandons and reschedules stale snapshots
  ---
  duration_ms: 0.531885
  ...
# Subtest: rename reconciliation abandons and reschedules stale editor snapshots
ok 3143 - rename reconciliation abandons and reschedules stale editor snapshots
  ---
  duration_ms: 0.265547
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 3144 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.824554
  ...
# Subtest: close-time retirement skips Depends-On lines
ok 3145 - close-time retirement skips Depends-On lines
  ---
  duration_ms: 1.217473
  ...
# Subtest: reopen restoration skips Depends-On lines instead of re-embedding them
ok 3146 - reopen restoration skips Depends-On lines instead of re-embedding them
  ---
  duration_ms: 0.573815
  ...
# Subtest: embedded-tree close collection ignores Depends-On lines
ok 3147 - embedded-tree close collection ignores Depends-On lines
  ---
  duration_ms: 0.310683
  ...
# Subtest: Alt-bracket bullet formatting never applies to Depends-On lines
ok 3148 - Alt-bracket bullet formatting never applies to Depends-On lines
  ---
  duration_ms: 0.52884
  ...
# Subtest: Ctrl+Enter on a dependency link closes only the target and runs the recovery
ok 3149 - Ctrl+Enter on a dependency link closes only the target and runs the recovery
  ---
  duration_ms: 1.741615
  ...
# Subtest: Ctrl+Enter on a dependency link reopens only the target, root-only
ok 3150 - Ctrl+Enter on a dependency link reopens only the target, root-only
  ---
  duration_ms: 1.10542
  ...
# Subtest: single and counted Alt-bracket cycle the dependency target under the cursor
ok 3151 - single and counted Alt-bracket cycle the dependency target under the cursor
  ---
  duration_ms: 17.104511
  ...
# Subtest: single and counted Alt-bracket report when the cursor is off every dependency link
ok 3152 - single and counted Alt-bracket report when the cursor is off every dependency link
  ---
  duration_ms: 0.556583
  ...
# Subtest: Ctrl+Enter candidate resolution finds plain links on Depends-On lines
ok 3153 - Ctrl+Enter candidate resolution finds plain links on Depends-On lines
  ---
  duration_ms: 0.180986
  ...
# Subtest: dependency-id normalisation never edits Depends-On lines
ok 3154 - dependency-id normalisation never edits Depends-On lines
  ---
  duration_ms: 0.229278
  ...
# Subtest: note rename rewrites fields while leaving Depends-On lines alone
ok 3155 - note rename rewrites fields while leaving Depends-On lines alone
  ---
  duration_ms: 0.148253
  ...
# Subtest: recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
ok 3156 - recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
  ---
  duration_ms: 1.683674
  ...
# Subtest: cycler freshness: local-fallback rewrite stamps last via injected stamper
ok 3157 - cycler freshness: local-fallback rewrite stamps last via injected stamper
  ---
  duration_ms: 1.60862
  ...
# Subtest: cycler freshness: rewrites without a stamper are unchanged (identity default)
ok 3158 - cycler freshness: rewrites without a stamper are unchanged (identity default)
  ---
  duration_ms: 0.337635
  ...
# Subtest: cycler freshness: a throwing stamper leaves the rewritten line intact
ok 3159 - cycler freshness: a throwing stamper leaves the rewritten line intact
  ---
  duration_ms: 0.149275
  ...
# Subtest: cycler freshness: transcluded rewrite stamps last via injected stamper
ok 3160 - cycler freshness: transcluded rewrite stamps last via injected stamper
  ---
  duration_ms: 0.163802
  ...
# Subtest: cycler freshness: cycling a plain line stamps through the follow-up edit
ok 3161 - cycler freshness: cycling a plain line stamps through the follow-up edit
  ---
  duration_ms: 0.744171
  ...
# Subtest: cycler freshness: Tasks-command rewrite with the expected status is stamped
ok 3162 - cycler freshness: Tasks-command rewrite with the expected status is stamped
  ---
  duration_ms: 0.345119
  ...
# Subtest: cycler freshness: Tasks command that inserts a line never stamps
ok 3163 - cycler freshness: Tasks command that inserts a line never stamps
  ---
  duration_ms: 0.302176
  ...
# Subtest: cycler freshness: Tasks command that deletes the line never stamps the next task
ok 3164 - cycler freshness: Tasks command that deletes the line never stamps the next task
  ---
  duration_ms: 0.191846
  ...
# Subtest: cycler freshness: Tasks command that leaves a different status never stamps
ok 3165 - cycler freshness: Tasks command that leaves a different status never stamps
  ---
  duration_ms: 0.374114
  ...
# Subtest: cycler freshness: cycling without ledger-tools writes no stamp
ok 3166 - cycler freshness: cycling without ledger-tools writes no stamp
  ---
  duration_ms: 0.458735
  ...
# Subtest: cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
ok 3167 - cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
  ---
  duration_ms: 0.25667
  ...
# Subtest: Pomodoro marker helpers normalize every block link and preserve fences and EOLs
ok 3168 - Pomodoro marker helpers normalize every block link and preserve fences and EOLs
  ---
  duration_ms: 2.385233
  ...
# Subtest: completed Pomodoro markers are normalized per occurrence
ok 3169 - completed Pomodoro markers are normalized per occurrence
  ---
  duration_ms: 0.446723
  ...
# Subtest: move-only Pomodoro links require a strict immediate hash directive
ok 3170 - move-only Pomodoro links require a strict immediate hash directive
  ---
  duration_ms: 2.215299
  ...
# Subtest: Pomodoro move-only planner toggles links across additional physical lines
ok 3171 - Pomodoro move-only planner toggles links across additional physical lines
  ---
  duration_ms: 1.039113
  ...
# Subtest: Pomodoro move-only planner round trips exact text and rejects strict non-matches
ok 3172 - Pomodoro move-only planner round trips exact text and rejects strict non-matches
  ---
  duration_ms: 0.462693
  ...
# Subtest: bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
ok 3173 - bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
  ---
  duration_ms: 1.328015
  ...
# Subtest: Pomodoro move-only runtime removes locally and validates additions independently
ok 3174 - Pomodoro move-only runtime removes locally and validates additions independently
  ---
  duration_ms: 0.924004
  ...
# Subtest: Pomodoro move-only runtime protects live lines after asynchronous failures
ok 3175 - Pomodoro move-only runtime protects live lines after asynchronous failures
  ---
  duration_ms: 0.42462
  ...
# Subtest: Pomodoro hash Vim mapping distinguishes bare and explicit repeats
ok 3176 - Pomodoro hash Vim mapping distinguishes bare and explicit repeats
  ---
  duration_ms: 8.751324
  ...
# Subtest: Pomodoro completion marks originals and carries clean live copies
ok 3177 - Pomodoro completion marks originals and carries clean live copies
  ---
  duration_ms: 1.734672
  ...
# Subtest: Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
ok 3178 - Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
  ---
  duration_ms: 0.908394
  ...
# Subtest: Pomodoro completion carries the closed Pomodoro name onto created entries
ok 3179 - Pomodoro completion carries the closed Pomodoro name onto created entries
  ---
  duration_ms: 0.4191
  ...
# Subtest: buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
ok 3180 - buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
  ---
  duration_ms: 0.374084
  ...
# Subtest: buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
ok 3181 - buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
  ---
  duration_ms: 0.295073
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is marked
ok 3182 - buildPomodoroCompletionPlan keeps source order when every carried link is marked
  ---
  duration_ms: 0.205082
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
ok 3183 - buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
  ---
  duration_ms: 0.227935
  ...
# Subtest: Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
ok 3184 - Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
  ---
  duration_ms: 4.84067
  ...
# Subtest: deferred-only close deletes the emptied entry and carries stripped links
ok 3185 - deferred-only close deletes the emptied entry and carries stripped links
  ---
  duration_ms: 0.435582
  ...
# Subtest: deferred-only close at EOF leaves no dangling newline
ok 3186 - deferred-only close at EOF leaves no dangling newline
  ---
  duration_ms: 0.200272
  ...
# Subtest: a close with a remaining copyable link keeps the [x] entry
ok 3187 - a close with a remaining copyable link keeps the [x] entry
  ---
  duration_ms: 0.271929
  ...
# Subtest: a prose sibling keeps the closed entry on a deferred close
ok 3188 - a prose sibling keeps the closed entry on a deferred close
  ---
  duration_ms: 0.276067
  ...
# Subtest: Ctrl+Enter deferred-only close deletes the entry in one gesture
ok 3189 - Ctrl+Enter deferred-only close deletes the entry in one gesture
  ---
  duration_ms: 3.887622
  ...
# Subtest: deferred-only close keeps a separated prose child and deletes fence-only leftovers whole
ok 3190 - deferred-only close keeps a separated prose child and deletes fence-only leftovers whole
  ---
  duration_ms: 0.803544
  ...
# Subtest: deferred-only successor relocation uses the inserted placeholder
ok 3191 - deferred-only successor relocation uses the inserted placeholder
  ---
  duration_ms: 0.235639
  ...
# Subtest: selected Done Pomodoro transclusion reopens only its cross-file root
ok 3192 - selected Done Pomodoro transclusion reopens only its cross-file root
  ---
  duration_ms: 6.297442
  ...
# Subtest: selected same-file Done target reopens root-only in the live editor
ok 3193 - selected same-file Done target reopens root-only in the live editor
  ---
  duration_ms: 1.316553
  ...
# Subtest: selected retired link reopens its root and restores the historical occurrence
ok 3194 - selected retired link reopens its root and restores the historical occurrence
  ---
  duration_ms: 1.43538
  ...
# Subtest: incomplete selected Pomodoro transclusion still closes recursively
ok 3195 - incomplete selected Pomodoro transclusion still closes recursively
  ---
  duration_ms: 2.255716
  ...
# Subtest: Done Pomodoro reopens direct roots and clears only its block-link markers
ok 3196 - Done Pomodoro reopens direct roots and clears only its block-link markers
  ---
  duration_ms: 3.36283
  ...
# Subtest: Done Pomodoro reopen restores its own block reference after reopening direct roots
ok 3197 - Done Pomodoro reopen restores its own block reference after reopening direct roots
  ---
  duration_ms: 0.779558
  ...
# Subtest: Done Pomodoro markers remain when the Todo transition does not occur
ok 3198 - Done Pomodoro markers remain when the Todo transition does not occur
  ---
  duration_ms: 0.287419
  ...
# Subtest: registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
ok 3199 - registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
  ---
  duration_ms: 11.740612
  ...
# Subtest: registered Ctrl+Enter immediately recovers a same-file dependent
ok 3200 - registered Ctrl+Enter immediately recovers a same-file dependent
  ---
  duration_ms: 9.699065
  ...
# Subtest: registered Ctrl+Enter immediately recovers a cross-file dependent
ok 3201 - registered Ctrl+Enter immediately recovers a cross-file dependent
  ---
  duration_ms: 2.914555
  ...
# Subtest: child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
ok 3202 - child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
  ---
  duration_ms: 4.053216
  ...
# Subtest: Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
ok 3203 - Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
  ---
  duration_ms: 1.122994
  ...
# Subtest: selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
ok 3204 - selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
  ---
  duration_ms: 2.113324
  ...
# Subtest: selected unresolved or excluded embedded children are consumed as no-ops
ok 3205 - selected unresolved or excluded embedded children are consumed as no-ops
  ---
  duration_ms: 0.795689
  ...
# Subtest: Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
ok 3206 - Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
  ---
  duration_ms: 2.78683
  ...
# Subtest: Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
ok 3207 - Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
  ---
  duration_ms: 2.29457
  ...
# Subtest: Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
ok 3208 - Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
  ---
  duration_ms: 0.782844
  ...
# Subtest: Pomodoro Work Log note-group collection scopes to direct children and requires descendants
ok 3209 - Pomodoro Work Log note-group collection scopes to direct children and requires descendants
  ---
  duration_ms: 0.793164
  ...
# Subtest: Work Log entry body formats as *date* — summary
ok 3210 - Work Log entry body formats as *date* — summary
  ---
  duration_ms: 0.12554
  ...
# Subtest: buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
ok 3211 - buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
  ---
  duration_ms: 0.22047
  ...
# Subtest: planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
ok 3212 - planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
  ---
  duration_ms: 0.348375
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
ok 3213 - planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
  ---
  duration_ms: 0.297388
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
ok 3214 - planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
  ---
  duration_ms: 0.192988
  ...
# Subtest: planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
ok 3215 - planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
  ---
  duration_ms: 0.356029
  ...
# Subtest: planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
ok 3216 - planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
  ---
  duration_ms: 0.376198
  ...
# Subtest: full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
ok 3217 - full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
  ---
  duration_ms: 6.147816
  ...
# Subtest: full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
ok 3218 - full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
  ---
  duration_ms: 1.510865
  ...
# Subtest: full Pomodoro completion keeps two same-task Work Log note sets in source order
ok 3219 - full Pomodoro completion keeps two same-task Work Log note sets in source order
  ---
  duration_ms: 1.224238
  ...
# Subtest: full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
ok 3220 - full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
  ---
  duration_ms: 0.80115
  ...
# Subtest: full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
ok 3221 - full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
  ---
  duration_ms: 0.845444
  ...
# Subtest: full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
ok 3222 - full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
  ---
  duration_ms: 0.534039
  ...
# Subtest: PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
ok 3223 - PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
  ---
  duration_ms: 1.35698
  ...
# Subtest: PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
ok 3224 - PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
  ---
  duration_ms: 0.946867
  ...
# Subtest: PP1 links the emptied project's ^prj as Next and strips \#hide
ok 3225 - PP1 links the emptied project's ^prj as Next and strips \#hide
  ---
  duration_ms: 8.476731
  ...
# Subtest: PP29 closing a child ^prj pulls in its empty parent project
ok 3226 - PP29 closing a child ^prj pulls in its empty parent project
  ---
  duration_ms: 1.919765
  ...
# Subtest: PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
ok 3227 - PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
  ---
  duration_ms: 1.05282
  ...
# Subtest: PP30 keeps the parent untouched while another child or task remains
ok 3228 - PP30 keeps the parent untouched while another child or task remains
  ---
  duration_ms: 0.89026
  ...
# Subtest: PP31 skips missing, ambiguous, and non-project parents
ok 3229 - PP31 skips missing, ambiguous, and non-project parents
  ---
  duration_ms: 1.145136
  ...
# Subtest: PP33 cancellation surfaces the parent without linking it
ok 3230 - PP33 cancellation surfaces the parent without linking it
  ---
  duration_ms: 2.194689
  ...
# Subtest: PP2 and PP3 leave a project with remaining work alone
ok 3231 - PP2 and PP3 leave a project with remaining work alone
  ---
  duration_ms: 1.395433
  ...
# Subtest: PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
ok 3232 - PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
  ---
  duration_ms: 2.232723
  ...
# Subtest: PP6 Sub-projects marker states match display_for_wikilink
ok 3233 - PP6 Sub-projects marker states match display_for_wikilink
  ---
  duration_ms: 1.2519
  ...
# Subtest: PP7 and PP28 keep a future-scheduled ^prj byte-identical
ok 3234 - PP7 and PP28 keep a future-scheduled ^prj byte-identical
  ---
  duration_ms: 0.914125
  ...
# Subtest: PP8 still-blocks a ^prj that waits on another open prerequisite
ok 3235 - PP8 still-blocks a ^prj that waits on another open prerequisite
  ---
  duration_ms: 0.612098
  ...
# Subtest: PP9 already-planned ^prj raises to Next without a new link
ok 3236 - PP9 already-planned ^prj raises to Next without a new link
  ---
  duration_ms: 0.609874
  ...
# Subtest: PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
ok 3237 - PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
  ---
  duration_ms: 1.973257
  ...
# Subtest: PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
ok 3238 - PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
  ---
  duration_ms: 0.694826
  ...
# Subtest: PP14 an id-less last task still pulls in
ok 3239 - PP14 an id-less last task still pulls in
  ---
  duration_ms: 0.356962
  ...
# Subtest: PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
ok 3240 - PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
  ---
  duration_ms: 10.332565
  ...
# Subtest: PP17 one pull-in row wins over project_task
ok 3241 - PP17 one pull-in row wins over project_task
  ---
  duration_ms: 0.527738
  ...
# Subtest: PP18 cancel recovers only
ok 3242 - PP18 cancel recovers only
  ---
  duration_ms: 0.339418
  ...
# Subtest: PP20 unrecognised or unplannable notes never pull in
ok 3243 - PP20 unrecognised or unplannable notes never pull in
  ---
  duration_ms: 0.913714
  ...
# Subtest: PP24 closing an external prerequisite pulls in only when N is empty
ok 3244 - PP24 closing an external prerequisite pulls in only when N is empty
  ---
  duration_ms: 0.741455
  ...
# Subtest: PP25 cascades project_member recovery after a [?] pull-in
ok 3245 - PP25 cascades project_member recovery after a [?] pull-in
  ---
  duration_ms: 1.05828
  ...
# Subtest: PP26 dated recount treats a hidden leftover as remaining work
ok 3246 - PP26 dated recount treats a hidden leftover as remaining work
  ---
  duration_ms: 1.585567
  ...
# Subtest: PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
ok 3247 - PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
  ---
  duration_ms: 1.261007
  ...
# Subtest: successorNoticeText uses the §12.6 pull-in and surfaced copy
ok 3248 - successorNoticeText uses the §12.6 pull-in and surfaced copy
  ---
  duration_ms: 0.481539
  ...
# Subtest: Ctrl+Enter on the last task link inserts the ^prj and rewrites R
ok 3249 - Ctrl+Enter on the last task link inserts the ^prj and rewrites R
  ---
  duration_ms: 11.361479
  ...
# Subtest: PP29 runtime close and reopen use the parent pull-in receipt
ok 3250 - PP29 runtime close and reopen use the parent pull-in receipt
  ---
  duration_ms: 4.299428
  ...
# Subtest: PP18 Alt+[ cancel of the last task surfaces R without linking
ok 3251 - PP18 Alt+[ cancel of the last task surfaces R without linking
  ---
  duration_ms: 14.679021
  ...
# Subtest: PP19 same-day reopen restores R byte-for-byte and takes back the link
ok 3252 - PP19 same-day reopen restores R byte-for-byte and takes back the link
  ---
  duration_ms: 3.136578
  ...
# Subtest: a close in a project that still has work stays inside the gate
ok 3253 - a close in a project that still has work stays inside the gate
  ---
  duration_ms: 0.962276
  ...
# Subtest: P1 path-qualified skip keys: same ^review in another note does not suppress
ok 3254 - P1 path-qualified skip keys: same ^review in another note does not suppress
  ---
  duration_ms: 0.461421
  ...
# Subtest: P3 id-less cascade: stale [?] R recovers resident without [id::]
ok 3255 - P3 id-less cascade: stale [?] R recovers resident without [id::]
  ---
  duration_ms: 0.561251
  ...
# Subtest: P4 frontmatter scheduled validity mirrors Rust
ok 3256 - P4 frontmatter scheduled validity mirrors Rust
  ---
  duration_ms: 0.608742
  ...
# Subtest: P5 recognition mirrors Rust (status/type/prj line)
ok 3257 - P5 recognition mirrors Rust (status/type/prj line)
  ---
  duration_ms: 1.108085
  ...
# Subtest: P6 SUBOPEN blank line stops the marker scan (PP6)
ok 3258 - P6 SUBOPEN blank line stops the marker scan (PP6)
  ---
  duration_ms: 0.353184
  ...
# Subtest: promotion prompts default to Tasks in ordinary and project notes
ok 3259 - promotion prompts default to Tasks in ordinary and project notes
  ---
  duration_ms: 3.963535
  ...
# Subtest: promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
ok 3260 - promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
  ---
  duration_ms: 1.01053
  ...
# Subtest: promotion command writes only on accept and Enter selects Tasks
ok 3261 - promotion command writes only on accept and Enter selects Tasks
  ---
  duration_ms: 2.761332
  ...
# Subtest: promotion removes only genuinely empty source sections
ok 3262 - promotion removes only genuinely empty source sections
  ---
  duration_ms: 1.135889
  ...
# Subtest: promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
ok 3263 - promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
  ---
  duration_ms: 1.058281
  ...
# Subtest: Tasks-only preamble promotions prompt and blank Enter moves into Tasks
ok 3264 - Tasks-only preamble promotions prompt and blank Enter moves into Tasks
  ---
  duration_ms: 0.73817
  ...
# Subtest: plain bullets already in Tasks prompt and blank Enter promotes in place
ok 3265 - plain bullets already in Tasks prompt and blank Enter promotes in place
  ---
  duration_ms: 1.08441
  ...
# Subtest: promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
ok 3266 - promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
  ---
  duration_ms: 0.465749
  ...
# Subtest: always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
ok 3267 - always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
  ---
  duration_ms: 4.336267
  ...
# Could not restore all reopened task references [ 'Broken.md: unreadable' ]
# Could not recover all blocked dependents [
#   'BrokenRead.md: read failed',
#   'Stale.md: line 1 changed before recovery',
#   'BrokenWrite.md: write failed'
# ]
# Subtest: direct Done Tasks task reopens through the metadata-aware fallback
ok 3268 - direct Done Tasks task reopens through the metadata-aware fallback
  ---
  duration_ms: 1.883786
  ...
# Subtest: recursive completion status policy includes Next without broadening excluded statuses
ok 3269 - recursive completion status policy includes Next without broadening excluded statuses
  ---
  duration_ms: 0.243304
  ...
# Subtest: recursive completion closes a Next root and its nested Next descendant
ok 3270 - recursive completion closes a Next root and its nested Next descendant
  ---
  duration_ms: 3.411072
  ...
# Subtest: recursive completion traverses Done parents and skips excluded siblings
ok 3271 - recursive completion traverses Done parents and skips excluded siblings
  ---
  duration_ms: 1.117844
  ...
# Subtest: closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
ok 3272 - closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
  ---
  duration_ms: 1.506236
  ...
# Subtest: reopened-reference restoration is ancestry-aware, conservative, and idempotent
ok 3273 - reopened-reference restoration is ancestry-aware, conservative, and idempotent
  ---
  duration_ms: 1.448234
  ...
# Subtest: retirement preserves task-tree markers and unmarks Pomodoro embeds
ok 3274 - retirement preserves task-tree markers and unmarks Pomodoro embeds
  ---
  duration_ms: 0.396547
  ...
# Subtest: done Pomodoro retirement removes only the matching embedded marker
ok 3275 - done Pomodoro retirement removes only the matching embedded marker
  ---
  duration_ms: 0.274133
  ...
# Subtest: retirement stops at prose boundaries and pairs strikethrough spans
ok 3276 - retirement stops at prose boundaries and pairs strikethrough spans
  ---
  duration_ms: 0.42438
  ...
# Subtest: retired Pomodoro links are not copied into the next Pomodoro
ok 3277 - retired Pomodoro links are not copied into the next Pomodoro
  ---
  duration_ms: 1.519309
  ...
# Subtest: retirement coordinator rewrites active editor and vault notes together
ok 3278 - retirement coordinator rewrites active editor and vault notes together
  ---
  duration_ms: 0.996452
  ...
# Subtest: restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
ok 3279 - restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
  ---
  duration_ms: 1.22562
  ...
# Subtest: close and reopen reference mutations share one serialized queue
ok 3280 - close and reopen reference mutations share one serialized queue
  ---
  duration_ms: 0.265346
  ...
# Subtest: post-close finalizer runs one gated plan before reference retirement
ok 3281 - post-close finalizer runs one gated plan before reference retirement
  ---
  duration_ms: 0.474306
  ...
# Subtest: dependent recovery uses live editor buffers and preserves the cursor
ok 3282 - dependent recovery uses live editor buffers and preserves the cursor
  ---
  duration_ms: 2.810586
  ...
# Subtest: dependent recovery preserves successful siblings across stale and failed notes
ok 3283 - dependent recovery preserves successful siblings across stale and failed notes
  ---
  duration_ms: 1.230509
  ...
# Subtest: no-op vault transforms and irrelevant retirement files avoid process writes
ok 3284 - no-op vault transforms and irrelevant retirement files avoid process writes
  ---
  duration_ms: 0.293661
  ...
# Subtest: ambiguity scans and notices are cached while dependency identity lines stay stable
ok 3285 - ambiguity scans and notices are cached while dependency identity lines stay stable
  ---
  duration_ms: 0.501667
  ...
# Subtest: non-Vim open/done command finalizes the closed task identity
ok 3286 - non-Vim open/done command finalizes the closed task identity
  ---
  duration_ms: 0.480988
  ...
# Subtest: non-Vim open/done command restores the reopened task identity
ok 3287 - non-Vim open/done command restores the reopened task identity
  ---
  duration_ms: 0.352893
  ...
# Subtest: full Pomodoro completion retires embeds only after carry-forward planning
ok 3288 - full Pomodoro completion retires embeds only after carry-forward planning
  ---
  duration_ms: 5.132779
  ...
# Subtest: full Pomodoro completion recovers after a deduplicated multi-target batch
ok 3289 - full Pomodoro completion recovers after a deduplicated multi-target batch
  ---
  duration_ms: 6.194495
  ...
# Subtest: full Pomodoro completion moves a marked same-note link without history
ok 3290 - full Pomodoro completion moves a marked same-note link without history
  ---
  duration_ms: 0.603672
  ...
# Subtest: cycler LK1–LK19 recognises only relation line shapes
ok 3291 - cycler LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 1.365546
  ...
# Subtest: cycler MC10, MC11, MC12 and MC14 keep relations inert while allowing root-only gestures
ok 3292 - cycler MC10, MC11, MC12 and MC14 keep relations inert while allowing root-only gestures
  ---
  duration_ms: 2.039203
  ...
# Subtest: SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
ok 3293 - SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
  ---
  duration_ms: 22.715121
  ...
# Subtest: SO2–SO5 fan-outs with explicit selection (SO32 twenty)
ok 3294 - SO2–SO5 fan-outs with explicit selection (SO32 twenty)
  ---
  duration_ms: 6.512442
  ...
# Subtest: SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
ok 3295 - SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
  ---
  duration_ms: 1.008785
  ...
# Subtest: SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
ok 3296 - SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
  ---
  duration_ms: 1.177097
  ...
# Subtest: SO stable keys survive insertions/status changes; ambiguous rebinding refused
ok 3297 - SO stable keys survive insertions/status changes; ambiguous rebinding refused
  ---
  duration_ms: 2.012041
  ...
# Subtest: SO picker model, pick normalization, and API detection
ok 3298 - SO picker model, pick normalization, and API detection
  ---
  duration_ms: 0.65471
  ...
# Subtest: SO notice copy for offers (SO20, mixed, failure)
ok 3299 - SO notice copy for offers (SO20, mixed, failure)
  ---
  duration_ms: 0.516867
  ...
# Subtest: destination override to an existing entry inserts as its child
ok 3300 - destination override to an existing entry inserts as its child
  ---
  duration_ms: 2.515222
  ...
# Subtest: destination override with a stale preimage skips loudly
ok 3301 - destination override with a stale preimage skips loudly
  ---
  duration_ms: 0.820526
  ...
# Subtest: destination override with a closed entry skips loudly
ok 3302 - destination override with a closed entry skips loudly
  ---
  duration_ms: 0.900249
  ...
# Subtest: destination override with a new name creates one placeholder after the running entry
ok 3303 - destination override with a new name creates one placeholder after the running entry
  ---
  duration_ms: 0.818723
  ...
# Subtest: destination override with a new name racing an open entry joins it
ok 3304 - destination override with a new name racing an open entry joins it
  ---
  duration_ms: 0.53955
  ...
# Subtest: reopen takes back the untouched successor link and restores status
ok 3305 - reopen takes back the untouched successor link and restores status
  ---
  duration_ms: 21.662752
  ...
# Subtest: an edited successor bullet survives while its status still restores
ok 3306 - an edited successor bullet survives while its status still restores
  ---
  duration_ms: 3.180992
  ...
# Subtest: an edited successor status line survives while its link is taken back
ok 3307 - an edited successor status line survives while its link is taken back
  ---
  duration_ms: 4.003423
  ...
# Subtest: reopen on a different day leaves successor links alone
ok 3308 - reopen on a different day leaves successor links alone
  ---
  duration_ms: 2.260856
  ...
# Subtest: reopening a task closed without a pass shows no take-back
ok 3309 - reopening a task closed without a pass shows no take-back
  ---
  duration_ms: 1.320942
  ...
# Subtest: Alt+] on a planned prerequisite links its successor
ok 3310 - Alt+] on a planned prerequisite links its successor
  ---
  duration_ms: 9.128667
  ...
# Subtest: take-back deletes a pre-existing entry it empties
ok 3311 - take-back deletes a pre-existing entry it empties
  ---
  duration_ms: 2.680186
  ...
# Subtest: take-back deletes a stub-replaced entry through the vault
ok 3312 - take-back deletes a stub-replaced entry through the vault
  ---
  duration_ms: 0.372591
  ...
# Subtest: take-back keeps entries that are closed or keep another child
ok 3313 - take-back keeps entries that are closed or keep another child
  ---
  duration_ms: 0.38778
  ...
# Subtest: closing-entry relocation finds a deferred-only placeholder
ok 3314 - closing-entry relocation finds a deferred-only placeholder
  ---
  duration_ms: 0.449578
  ...
# Subtest: Alt+[ into Cancelled recovers its dependents without linking
ok 3315 - Alt+[ into Cancelled recovers its dependents without linking
  ---
  duration_ms: 2.621824
  ...
# Subtest: take-back keeps an entry whose prose survives across a blank line (both paths)
ok 3316 - take-back keeps an entry whose prose survives across a blank line (both paths)
  ---
  duration_ms: 0.512709
  ...
# Subtest: take-back deletes a whole block with continuation/fence leftovers (LF/CRLF, final newline)
ok 3317 - take-back deletes a whole block with continuation/fence leftovers (LF/CRLF, final newline)
  ---
  duration_ms: 1.013885
  ...
# Subtest: link close links the unblocked successor into the slot and shows the nav card
ok 3318 - link close links the unblocked successor into the slot and shows the nav card
  ---
  duration_ms: 19.629952
  ...
# Subtest: close with no [id::] performs zero vault reads and shows nothing
ok 3319 - close with no [id::] performs zero vault reads and shows nothing
  ---
  duration_ms: 0.96352
  ...
# Subtest: Warm finalize reads no unrelated note bodies on the real close path
ok 3320 - Warm finalize reads no unrelated note bodies on the real close path
  ---
  duration_ms: 2.926587
  ...
# Subtest: cold fallback still recovers and links without a Tasks cache
ok 3321 - cold fallback still recovers and links without a Tasks cache
  ---
  duration_ms: 3.287707
  ...
# Subtest: recovered-only close reports unblocked without linking (SO4 Esc)
ok 3322 - recovered-only close reports unblocked without linking (SO4 Esc)
  ---
  duration_ms: 1.326121
  ...
# Subtest: walk landing composes a single toast and shows no card
ok 3323 - walk landing composes a single toast and shows no card
  ---
  duration_ms: 6.983822
  ...
# Subtest: nav absent falls back to a plain Notice with no link (SO missing picker)
ok 3324 - nav absent falls back to a plain Notice with no link (SO missing picker)
  ---
  duration_ms: 1.870431
  ...
# Subtest: stale cache heals via re-plan from fresh text (SO30)
ok 3325 - stale cache heals via re-plan from fresh text (SO30)
  ---
  duration_ms: 1.751754
  ...
# Subtest: Pomodoro-line close appends the successor to the created continuation
ok 3326 - Pomodoro-line close appends the successor to the created continuation
  ---
  duration_ms: 4.853504
  ...
# Subtest: Pomodoro-line close keeps the closing anchor after the picker re-plan
ok 3327 - Pomodoro-line close keeps the closing anchor after the picker re-plan
  ---
  duration_ms: 2.670688
  ...
# Subtest: completeTaskAtCursor returns the notice and shows nothing itself
ok 3328 - completeTaskAtCursor returns the notice and shows nothing itself
  ---
  duration_ms: 1.721646
  ...
# Subtest: successor apply recovers project residents without ledger v12
ok 3329 - successor apply recovers project residents without ledger v12
  ---
  duration_ms: 11.452131
  ...
# Subtest: SB vectors pin the successor mint pipeline
ok 3330 - SB vectors pin the successor mint pipeline
  ---
  duration_ms: 2.143352
  ...
# Subtest: successor suggester ports the Rust candidate and suffix rules
ok 3331 - successor suggester ports the Rust candidate and suffix rules
  ---
  duration_ms: 0.646214
  ...
# Subtest: successor link form names unique basenames short and the day file always
ok 3332 - successor link form names unique basenames short and the day file always
  ---
  duration_ms: 0.399282
  ...
# Subtest: tasksFromDocuments normalizes vault lines to pool shape
ok 3333 - tasksFromDocuments normalizes vault lines to pool shape
  ---
  duration_ms: 1.069952
  ...
# Subtest: normalizeTasksCacheTask ports every known Tasks shape
ok 3334 - normalizeTasksCacheTask ports every known Tasks shape
  ---
  duration_ms: 0.386448
  ...
# Subtest: buildDependentsIndex keeps first task IDs and groups dependents
ok 3335 - buildDependentsIndex keeps first task IDs and groups dependents
  ---
  duration_ms: 0.195202
  ...
# Subtest: findLiveLinks counts plain, embedded, and deferred links under open entries only
ok 3336 - findLiveLinks counts plain, embedded, and deferred links under open entries only
  ---
  duration_ms: 2.407164
  ...
# Subtest: computeSuccessorAnchors implements closing, slot, inherit, and none
ok 3337 - computeSuccessorAnchors implements closing, slot, inherit, and none
  ---
  duration_ms: 0.857947
  ...
# Subtest: SL1 links the successor right after the predecessor bullet
ok 3338 - SL1 links the successor right after the predecessor bullet
  ---
  duration_ms: 5.825261
  ...
# Subtest: SL3 still-blocked rows count the open prerequisites left
ok 3339 - SL3 still-blocked rows count the open prerequisites left
  ---
  duration_ms: 0.919816
  ...
# Subtest: SL4 future-scheduled dependents stay Blocked with the date row
ok 3340 - SL4 future-scheduled dependents stay Blocked with the date row
  ---
  duration_ms: 0.600697
  ...
# Subtest: SL5 already-planned dependents recover without a duplicate link
ok 3341 - SL5 already-planned dependents recover without a duplicate link
  ---
  duration_ms: 0.963029
  ...
# Subtest: SL6 struck and closed-entry links do not count as planned
ok 3342 - SL6 struck and closed-entry links do not count as planned
  ---
  duration_ms: 1.686659
  ...
# Subtest: SL7 closing anchors create the continuation placeholder
ok 3343 - SL7 closing anchors create the continuation placeholder
  ---
  duration_ms: 0.948881
  ...
# Subtest: SL8 closing anchors append after carried lines in the continuation
ok 3344 - SL8 closing anchors append after carried lines in the continuation
  ---
  duration_ms: 0.724864
  ...
# Subtest: SL9 unplanned predecessors offer at the implicit destination (SO14)
ok 3345 - SL9 unplanned predecessors offer at the implicit destination (SO14)
  ---
  duration_ms: 1.098898
  ...
# Subtest: SL10 missing block IDs mint through the SB rule
ok 3346 - SL10 missing block IDs mint through the SB rule
  ---
  duration_ms: 0.557545
  ...
# Subtest: SL11 project and hidden tasks recover but never link
ok 3347 - SL11 project and hidden tasks recover but never link
  ---
  duration_ms: 8.484928
  ...
# Subtest: PDC1 leaves a dependency-ready resident Blocked while its project still waits
ok 3348 - PDC1 leaves a dependency-ready resident Blocked while its project still waits
  ---
  duration_ms: 1.83894
  ...
# Subtest: PDC2 residents are offered under the project group (SO1)
ok 3349 - PDC2 residents are offered under the project group (SO1)
  ---
  duration_ms: 1.692811
  ...
# Subtest: PDC3 keeps a project resident Blocked when its own prerequisite remains open
ok 3350 - PDC3 keeps a project resident Blocked when its own prerequisite remains open
  ---
  duration_ms: 1.130959
  ...
# Subtest: PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
ok 3351 - PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
  ---
  duration_ms: 2.407495
  ...
# Subtest: SL12 one gesture closing two prerequisites links once with both causes
ok 3352 - SL12 one gesture closing two prerequisites links once with both causes
  ---
  duration_ms: 0.511286
  ...
# Subtest: SL13 chains do not recurse: the dependent's own dependents wait
ok 3353 - SL13 chains do not recurse: the dependent's own dependents wait
  ---
  duration_ms: 0.285636
  ...
# Subtest: SL14 ambiguous basenames link long
ok 3354 - SL14 ambiguous basenames link long
  ---
  duration_ms: 0.291006
  ...
# Subtest: SL15 stale open dependents link and become Next
ok 3355 - SL15 stale open dependents link and become Next
  ---
  duration_ms: 0.275025
  ...
# Subtest: SL16 gates on [id::]: no identity means no lookup and empty rows
ok 3356 - SL16 gates on [id::]: no identity means no lookup and empty rows
  ---
  duration_ms: 0.18874
  ...
# Subtest: SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
ok 3357 - SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
  ---
  duration_ms: 1.403029
  ...
# Subtest: SL18 the kill switch recovers without linking or minting
ok 3358 - SL18 the kill switch recovers without linking or minting
  ---
  duration_ms: 0.375808
  ...
# Subtest: SL19 re-applied closes write nothing and report nothing
ok 3359 - SL19 re-applied closes write nothing and report nothing
  ---
  duration_ms: 0.307447
  ...
# Subtest: SL23 subtasks anchor at their root's link
ok 3360 - SL23 subtasks anchor at their root's link
  ---
  duration_ms: 0.493112
  ...
# Subtest: SL24 later same-name entries take the closing successors
ok 3361 - SL24 later same-name entries take the closing successors
  ---
  duration_ms: 0.619523
  ...
# Subtest: SL25 already-Next planned dependents produce no row
ok 3362 - SL25 already-Next planned dependents produce no row
  ---
  duration_ms: 0.453616
  ...
# Subtest: SL26 inbox successors carry the inbox flag
ok 3363 - SL26 inbox successors carry the inbox flag
  ---
  duration_ms: 0.29305
  ...
# Subtest: SL27 dropped links are never re-linked and recover to Ready
ok 3364 - SL27 dropped links are never re-linked and recover to Ready
  ---
  duration_ms: 0.362853
  ...
# Subtest: SL28 day-file successors name the note, never the bare link
ok 3365 - SL28 day-file successors name the note, never the bare link
  ---
  duration_ms: 0.288571
  ...
# Subtest: slot insertions land after the anchor subtree with its indent
ok 3366 - slot insertions land after the anchor subtree with its indent
  ---
  duration_ms: 0.240319
  ...
# Subtest: closing insertions replace a lone stub child
ok 3367 - closing insertions replace a lone stub child
  ---
  duration_ms: 0.478223
  ...
# Subtest: insertions skip placements with no valid target
ok 3368 - insertions skip placements with no valid target
  ---
  duration_ms: 0.139927
  ...
# Subtest: successorNoticeText implements the §12.6 table
ok 3369 - successorNoticeText implements the §12.6 table
  ---
  duration_ms: 0.500095
  ...
# Subtest: parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
ok 3370 - parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
  ---
  duration_ms: 0.389514
  ...
# Subtest: loadLinkUnblocked stat-caches the config read
ok 3371 - loadLinkUnblocked stat-caches the config read
  ---
  duration_ms: 0.29862
  ...
# Subtest: loadLinkUnblocked treats missing or unreadable config as true
ok 3372 - loadLinkUnblocked treats missing or unreadable config as true
  ---
  duration_ms: 1.219989
  ...
# Subtest: successorPlanConfigPath honors XDG_CONFIG_HOME
ok 3373 - successorPlanConfigPath honors XDG_CONFIG_HOME
  ---
  duration_ms: 0.18359
  ...
# Subtest: todayDailyPath mirrors the ledger daily path
ok 3374 - todayDailyPath mirrors the ledger daily path
  ---
  duration_ms: 0.511616
  ...
# Subtest: normalizeClosedTaskIdentities keeps the anchor root off the match gate
ok 3375 - normalizeClosedTaskIdentities keeps the anchor root off the match gate
  ---
  duration_ms: 0.208217
  ...
# Subtest: ID-less planned roots anchor ID-bearing children without minting IDs
ok 3376 - ID-less planned roots anchor ID-bearing children without minting IDs
  ---
  duration_ms: 0.681941
  ...
# Subtest: successor anchors never guess across roots
ok 3377 - successor anchors never guess across roots
  ---
  duration_ms: 0.360709
  ...
# Subtest: a child with its own live link keeps its own slot
ok 3378 - a child with its own live link keeps its own slot
  ---
  duration_ms: 0.401958
  ...
# Subtest: getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
ok 3379 - getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
  ---
  duration_ms: 0.252662
  ...
# Subtest: countSuccessorBasenames walks the vault set, not the task set
ok 3380 - countSuccessorBasenames walks the vault set, not the task set
  ---
  duration_ms: 0.331924
  ...
# Subtest: the pass threads a richer isInbox into unblocked rows
ok 3381 - the pass threads a richer isInbox into unblocked rows
  ---
  duration_ms: 0.330791
  ...
# Subtest: getTaskLinkLaneApi returns the lane only when version and both functions exist
ok 3382 - getTaskLinkLaneApi returns the lane only when version and both functions exist
  ---
  duration_ms: 1.009167
  ...
# Subtest: isTaskLinkLaneLine passes content, line, and path and never throws
ok 3383 - isTaskLinkLaneLine passes content, line, and path and never throws
  ---
  duration_ms: 5.210516
  ...
# Subtest: single Alt+] on a Task Link delegates with exactly { editor, view }
ok 3384 - single Alt+] on a Task Link delegates with exactly { editor, view }
  ---
  duration_ms: 0.672073
  ...
# Subtest: Alt+[ and Alt+] delegate identically; direction is ignored
ok 3385 - Alt+[ and Alt+] delegate identically; direction is ignored
  ---
  duration_ms: 0.312356
  ...
# Subtest: embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
ok 3386 - embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
  ---
  duration_ms: 0.29313
  ...
# Subtest: entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
ok 3387 - entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
  ---
  duration_ms: 2.614651
  ...
# Subtest: counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
ok 3388 - counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
  ---
  duration_ms: 0.615786
  ...
# Subtest: counted dispatch without an explicit repeat leaves the key alone
ok 3389 - counted dispatch without an explicit repeat leaves the key alone
  ---
  duration_ms: 0.20433
  ...
# Subtest: counted range starting elsewhere skips Task Link lines
ok 3390 - counted range starting elsewhere skips Task Link lines
  ---
  duration_ms: 1.97473
  ...
# Subtest: legacy fallback with no api keeps today's behavior
ok 3391 - legacy fallback with no api keeps today's behavior
  ---
  duration_ms: 0.798264
  ...
# Subtest: plain Task Link in an open Pomodoro closes the task root-only and strikes the link
ok 3392 - plain Task Link in an open Pomodoro closes the task root-only and strikes the link
  ---
  duration_ms: 14.849036
  ...
# Subtest: marked plain Task Link drops its marker when struck under Pomodoro ancestry
ok 3393 - marked plain Task Link drops its marker when struck under Pomodoro ancestry
  ---
  duration_ms: 1.542374
  ...
# Subtest: plain Pomodoro Task Link closes root-only while embedded closes recursively
ok 3394 - plain Pomodoro Task Link closes root-only while embedded closes recursively
  ---
  duration_ms: 2.339105
  ...
# Subtest: embedded Pomodoro Task Link still closes recursively and retires to struck form
ok 3395 - embedded Pomodoro Task Link still closes recursively and retires to struck form
  ---
  duration_ms: 2.339035
  ...
# Subtest: Ctrl+Enter toggles a struck plain Pomodoro link back to open
ok 3396 - Ctrl+Enter toggles a struck plain Pomodoro link back to open
  ---
  duration_ms: 1.675639
  ...
# Subtest: same-file plain Task Link closes and strikes the correct line
ok 3397 - same-file plain Task Link closes and strikes the correct line
  ---
  duration_ms: 1.061156
  ...
# Subtest: cursor selects which of several Task Links closes and strikes
ok 3398 - cursor selects which of several Task Links closes and strikes
  ---
  duration_ms: 1.290674
  ...
# Subtest: plain links to Blocked or non-task blocks still complete the Pomodoro
ok 3399 - plain links to Blocked or non-task blocks still complete the Pomodoro
  ---
  duration_ms: 3.663783
  ...
# Subtest: strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
ok 3400 - strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
  ---
  duration_ms: 0.626876
  ...
# Subtest: completeTaskAtCursor closes each open symbol through the Tasks command
ok 3401 - completeTaskAtCursor closes each open symbol through the Tasks command
  ---
  duration_ms: 1.646693
  ...
# Subtest: completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
ok 3402 - completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
  ---
  duration_ms: 0.347703
  ...
# Subtest: completeTaskAtCursor refuses closed, cancelled, and non-task lines
ok 3403 - completeTaskAtCursor refuses closed, cancelled, and non-task lines
  ---
  duration_ms: 0.317205
  ...
# Subtest: completeTaskAtCursor refuses a missing Tasks command with no write
ok 3404 - completeTaskAtCursor refuses a missing Tasks command with no write
  ---
  duration_ms: 0.160817
  ...
# Subtest: Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
ok 3405 - Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
  ---
  duration_ms: 0.608341
  ...
# Subtest: completeTaskAtCursor reports not-closed when Tasks does not write [x]
ok 3406 - completeTaskAtCursor reports not-closed when Tasks does not write [x]
  ---
  duration_ms: 0.181236
  ...
# Subtest: recovery api is frozen at version 2 and recovers without striking references
ok 3407 - recovery api is frozen at version 2 and recovers without striking references
  ---
  duration_ms: 2.615854
  ...
# Subtest: recovery api never throws and reports failures
ok 3408 - recovery api never throws and reports failures
  ---
  duration_ms: 0.278121
  ...
# Subtest: future-scheduled dependents stay Blocked on the planner, api, and close paths
ok 3409 - future-scheduled dependents stay Blocked on the planner, api, and close paths
  ---
  duration_ms: 16.702895
  ...
# Subtest: Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
ok 3410 - Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
  ---
  duration_ms: 5.089245
  ...
# Subtest: every printable non-space ASCII key resolves to a surround pair
ok 3411 - every printable non-space ASCII key resolves to a surround pair
  ---
  duration_ms: 4.299999
  ...
# Subtest: visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
ok 3412 - visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
  ---
  duration_ms: 0.684106
  ...
# Subtest: non-visible, combining, multi-character, and multi-code-unit values are rejected
ok 3413 - non-visible, combining, multi-character, and multi-code-unit values are rejected
  ---
  duration_ms: 0.245058
  ...
# Subtest: ys adds broad symmetric delimiters through pending keydown
ok 3414 - ys adds broad symmetric delimiters through pending keydown
  ---
  duration_ms: 1.200512
  ...
# Subtest: rejected keydown input never edits or leaks into a pending ys
ok 3415 - rejected keydown input never edits or leaks into a pending ys
  ---
  duration_ms: 0.371609
  ...
# Subtest: Escape cancels ys, cs, and ds pending state without editing
ok 3416 - Escape cancels ys, cs, and ds pending state without editing
  ---
  duration_ms: 0.260828
  ...
# Subtest: cs accepts broad target and replacement characters independently
ok 3417 - cs accepts broad target and replacement characters independently
  ---
  duration_ms: 1.967806
  ...
# Subtest: cs preserves structural alias and padding rules
ok 3418 - cs preserves structural alias and padding rules
  ---
  duration_ms: 0.543067
  ...
# Subtest: cs replaces repeated symmetric runs exactly once on each side
ok 3419 - cs replaces repeated symmetric runs exactly once on each side
  ---
  duration_ms: 0.499243
  ...
# Subtest: ds removes representative broad symmetric delimiters
ok 3420 - ds removes representative broad symmetric delimiters
  ---
  duration_ms: 0.714554
  ...
# Subtest: ds preserves structural alias and padding rules
ok 3421 - ds preserves structural alias and padding rules
  ---
  duration_ms: 0.301746
  ...
# Subtest: ds removes one pair from repeated runs, including the reported block link
ok 3422 - ds removes one pair from repeated runs, including the reported block link
  ---
  duration_ms: 1.111942
  ...
# Subtest: consecutive ds commands peel a triple symmetric surround
ok 3423 - consecutive ds commands peel a triple symmetric surround
  ---
  duration_ms: 0.206234
  ...
# Subtest: symmetric discovery uses deterministic sequential same-line run pairs
ok 3424 - symmetric discovery uses deterministic sequential same-line run pairs
  ---
  duration_ms: 0.165597
  ...
# Subtest: symmetric discovery includes every character in repeated boundaries
ok 3425 - symmetric discovery includes every character in repeated boundaries
  ---
  duration_ms: 0.25672
  ...
# Subtest: unpaired and unequal symmetric runs are safe no-ops
ok 3426 - unpaired and unequal symmetric runs are safe no-ops
  ---
  duration_ms: 0.198078
  ...
# Subtest: ordinary normal-mode keys remain untouched outside pending state
ok 3427 - ordinary normal-mode keys remain untouched outside pending state
  ---
  duration_ms: 0.191936
  ...
# Subtest: dot while a surround is pending is a literal delimiter, not repeat
ok 3428 - dot while a surround is pending is a literal delimiter, not repeat
  ---
  duration_ms: 0.119989
  ...
# Subtest: dot-repeat records and replays broad-character ys
ok 3429 - dot-repeat records and replays broad-character ys
  ---
  duration_ms: 0.234107
  ...
# Subtest: dot-repeat records and replays broad-character cs
ok 3430 - dot-repeat records and replays broad-character cs
  ---
  duration_ms: 0.17795
  ...
# Subtest: dot-repeat records and replays broad-character ds
ok 3431 - dot-repeat records and replays broad-character ds
  ---
  duration_ms: 0.192427
  ...
# Subtest: dot-repeat replays cs against repeated symmetric runs
ok 3432 - dot-repeat replays cs against repeated symmetric runs
  ---
  duration_ms: 0.276919
  ...
# Subtest: dot-repeat replays ds against repeated symmetric runs
ok 3433 - dot-repeat replays ds against repeated symmetric runs
  ---
  duration_ms: 0.205332
  ...
# Subtest: consecutive dot-repeats peel a triple symmetric surround
ok 3434 - consecutive dot-repeats peel a triple symmetric surround
  ---
  duration_ms: 0.203078
  ...
1..3434
# tests 3449
# suites 0
# pass 3443
# fail 6
# cancelled 0
# skipped 0
# todo 0
# duration_ms 7184.42764
failed  exit=1  duration=15380ms

