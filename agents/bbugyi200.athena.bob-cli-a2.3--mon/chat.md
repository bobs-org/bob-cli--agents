# Chat History - ace-run (bob-cli-a2.3--mon)

- **TIMESTAMP:** 2026-10-20 09:48:27 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-a2.3--mon

## Prompt

sase monitor start --command 'npm test' --reason 'Run the full bob-plugins suite and complete the assigned task-relations guard phase'

## Response

sase tool run 71d6c9add058c773a2aeb75931cd661e

> bob-plugins@0.1.0 test
> node scripts/build-plugins.mjs --check && npm run docs:inventory:check && node --test scripts/test-project-tasks-snapshot.cjs scripts/test-bob-articles.cjs scripts/test-dependency-line-migration.cjs scripts/test-navigation-hotkeys-section-nav.cjs scripts/test-navigation-hotkeys-rename.cjs scripts/test-navigation-hotkeys-ref-pdf.cjs scripts/test-navigation-hotkeys-templater-trigger.cjs scripts/test-navigation-hotkeys-schedule-recovery.cjs scripts/test-navigation-hotkeys-schedule-properties.cjs scripts/test-navigation-hotkeys-schedule-writes.cjs scripts/test-navigation-hotkeys-runtime-schedule.cjs scripts/test-navigation-hotkeys-dependencies.cjs scripts/test-navigation-blocks-guards.cjs scripts/test-navigation-relation-lines.cjs scripts/test-navigation-blocks-writers.cjs scripts/test-navigation-blocks-edit.cjs scripts/test-navigation-blocks-stage-view.cjs scripts/test-navigation-hotkeys-dependency-mirror.cjs scripts/test-navigation-hotkeys-task-move-plan.cjs scripts/test-navigation-hotkeys-priority-notice.cjs scripts/test-navigation-successor-picker.cjs scripts/test-navigation-image-zoom-viewer.cjs scripts/test-navigation-hotkeys-unblocked-notice.cjs scripts/test-navigation-project-blocking.cjs scripts/test-navigation-project-dependency-stage.cjs scripts/test-navigation-project-subprojects.cjs scripts/test-navigation-project-subtree-gestures.cjs scripts/test-navigation-hotkeys-priority-picker.cjs scripts/test-navigation-hotkeys-picker-lifecycle.cjs scripts/test-navigation-hotkeys-ref-picker-text.cjs scripts/test-navigation-hotkeys-pomodoro-move-pickers.cjs scripts/test-navigation-inbox-route.cjs scripts/test-navigation-inbox-route-card.cjs scripts/test-navigation-hotkeys-task-move.cjs scripts/test-navigation-open-notes-uri.cjs scripts/test-navigation-goto-task-uri.cjs scripts/test-navigation-hotkeys-open-task-jump.cjs scripts/test-navigation-hotkeys-vim-counts.cjs scripts/test-navigation-hotkeys-tab-pin.cjs scripts/test-navigation-hotkeys-schedule-log.cjs scripts/test-navigation-hotkeys-schedule-review.cjs scripts/test-navigation-hotkeys-deferred-pomodoro.cjs scripts/test-navigation-hotkeys-pomodoro-parse.cjs scripts/test-navigation-hotkeys-pomodoro-bullet-move.cjs scripts/test-navigation-hotkeys-pomodoro-split-rename.cjs scripts/test-navigation-hotkeys-pomodoro-reorder.cjs scripts/test-navigation-hotkeys-runtime-prune.cjs scripts/test-navigation-hotkeys-project-from-task.cjs scripts/test-navigation-hotkeys-project-reversal.cjs scripts/test-navigation-hotkeys-link-picker.cjs scripts/test-navigation-hotkeys-lane-toggle.cjs scripts/test-navigation-hotkeys-task-link-lane.cjs scripts/test-navigation-hotkeys-cancel-log.cjs scripts/test-navigation-hotkeys-cancel-task.cjs scripts/test-navigation-hotkeys-forward-promotion.cjs scripts/test-navigation-hotkeys-schedule-work-log.cjs scripts/test-navigation-hotkeys-task-move-history.cjs scripts/test-navigation-jump-history.cjs scripts/test-navigation-dependencies.cjs scripts/test-navigation-editor-line-diff.cjs scripts/test-navigation-roll-decay.cjs scripts/test-navigation-decay-planner.cjs scripts/test-navigation-task-card-model.cjs scripts/test-navigation-task-card-view.cjs scripts/test-navigation-task-card-schedule.cjs scripts/test-navigation-task-card-review.cjs scripts/test-navigation-decision-card.cjs scripts/test-navigation-decision-card-handlers.cjs scripts/test-navigation-refresh-modal.cjs scripts/test-navigation-freshness.cjs scripts/test-navigation-stamps.cjs scripts/test-navigation-keep-counting.cjs scripts/test-navigation-checklist.cjs scripts/test-navigation-review-advance.cjs scripts/test-navigation-review-advance-gestures.cjs scripts/test-navigation-checklist-ctrl-enter.cjs scripts/test-ledger-tools-navigation.cjs scripts/test-ledger-tools-plan-budget.cjs scripts/test-ledger-tools-relations.cjs scripts/test-ledger-tools-ready-badge.cjs scripts/test-ledger-tools-note-ready.cjs scripts/test-ledger-tools-note-ready-views.cjs scripts/test-ledger-tools-dashboard-parity.cjs scripts/test-ledger-tools-work-badge-tone.cjs scripts/test-ledger-tools-dashboard-collections.cjs scripts/test-ledger-tools-today.cjs scripts/test-ledger-tools-freshness-placement.cjs scripts/test-ledger-tools-freshness-states.cjs scripts/test-ledger-tools-freshness-namespace.cjs scripts/test-ledger-tools-freshness-review-model.cjs scripts/test-ledger-tools-freshness-queue.cjs scripts/test-ledger-tools-freshness-tracking.cjs scripts/test-ledger-tools-freshness-footer.cjs scripts/test-ledger-tools-freshness-recurring.cjs scripts/test-ledger-tools-freshness-mark.cjs scripts/test-ledger-tools-freshness-mark-surfaces.cjs scripts/test-ledger-tools-priority-marks.cjs scripts/test-ledger-tools-task-tag-marks.cjs scripts/test-ledger-tools-today-marks.cjs scripts/test-ledger-tools-today-marks-reading.cjs scripts/test-ledger-tools-unblocked-glyph.cjs scripts/test-ledger-tools-progress-marks.cjs scripts/test-ledger-tools-date-marks.cjs scripts/test-ledger-tools-date-marks-tasks.cjs scripts/test-ledger-tools-freshness-keeps.cjs scripts/test-ledger-tools-freshness-unblocked.cjs scripts/test-ledger-tools-freshness-decision-card.cjs scripts/test-ledger-tools-dependency-chips.cjs scripts/test-ledger-tools-blocks-chips.cjs scripts/test-ledger-tools-snippets.cjs scripts/test-ledger-tools-vim-mappings.cjs scripts/test-task-status-cycler-dependencies.cjs scripts/test-task-status-cycler-blocks-guards.cjs scripts/test-task-status-cycler-relations.cjs scripts/test-task-status-cycler-ctrl-enter.cjs scripts/test-task-status-cycler-reference-lifecycle.cjs scripts/test-task-status-cycler-pomodoro-completion.cjs scripts/test-task-status-cycler-pomodoro-work-log.cjs scripts/test-task-status-cycler-pomodoro-reopen.cjs scripts/test-task-status-cycler-blocked-schedule.cjs scripts/test-task-status-cycler-demotion-picker.cjs scripts/test-task-status-cycler-promotion.cjs scripts/test-task-status-cycler-counted-toggle.cjs scripts/test-task-status-cycler-successors.cjs scripts/test-task-status-cycler-successor-wiring.cjs scripts/test-task-status-cycler-successor-polish.cjs scripts/test-task-status-cycler-successor-offers.cjs scripts/test-task-status-cycler-project-pull-in.cjs scripts/test-task-status-cycler-task-links-api.cjs scripts/test-task-status-cycler-task-link-lane.cjs scripts/test-task-status-cycler-freshness.cjs scripts/test-block-id-prompt-dependencies.cjs scripts/test-block-id-prompt-blocks-guards.cjs scripts/test-block-id-prompt-relations.cjs scripts/test-block-id-prompt-ref-picker-text.cjs scripts/test-block-id-prompt-markers.cjs scripts/test-block-id-prompt-pomodoro-context.cjs scripts/test-block-id-prompt-target-update.cjs scripts/test-block-id-prompt-pomodoro-insertion.cjs scripts/test-block-id-prompt-pomodoro-targets.cjs scripts/test-block-id-prompt-pomodoro-picker-view.cjs scripts/test-block-id-prompt-pomodoro-picker-runtime.cjs scripts/test-block-id-prompt-work-log.cjs scripts/test-block-id-prompt-pomodoro-link-runtime.cjs scripts/test-block-id-prompt-pomodoro-link-picker-api.cjs scripts/test-block-id-prompt-pomodoro-unlink-runtime.cjs scripts/test-block-id-prompt-task-link-deletion.cjs scripts/test-block-id-prompt-plan-budget-and-freshness.cjs scripts/test-prompt-block-id-naming.cjs scripts/test-block-id-prompt-prefill.cjs scripts/test-vim-surround.cjs scripts/test-navigation-dependencies-stage-ranker-and-pool.cjs scripts/test-navigation-dependencies-stage-entry-and-view.cjs scripts/test-navigation-dependencies-stage-writes.cjs scripts/test-navigation-dependencies-stage-mirror-and-badge.cjs scripts/test-navigation-dependencies-stage-stale-guards.cjs scripts/test-navigation-dependencies-stage-performance.cjs scripts/test-navigation-prompt-block-id-stage.cjs scripts/test-navigation-dependencies-writer.cjs scripts/test-navigation-dependency-link-consumption.cjs scripts/test-plugin-build.cjs scripts/test-ledger-tools-stats-journal.cjs scripts/test-ledger-tools-stats-data.cjs scripts/test-ledger-tools-stats-block.cjs scripts/test-ledger-tools-stats-charts.cjs scripts/test-navigation-review-journal.cjs scripts/test-ledger-tools-stats-panels.cjs scripts/test-ledger-tools-reading-board-data.cjs scripts/test-ledger-tools-reading-board-models.cjs scripts/test-ledger-tools-reading-board-block.cjs scripts/test-ledger-tools-pomodoro-home-chips.cjs scripts/test-navigation-image-zoom-target.cjs scripts/test-docs-inventory.mjs scripts/test-docs-check.mjs

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
  duration_ms: 1.119949
  ...
# Subtest: bip BK13–BK15 malformed split mirrors the Depends-On twin
ok 2 - bip BK13–BK15 malformed split mirrors the Depends-On twin
  ---
  duration_ms: 0.382381
  ...
# Subtest: bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
ok 3 - bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
  ---
  duration_ms: 0.107335
  ...
# Subtest: bip MC1/MC2 Pomodoro scanners skip managed lines
ok 4 - bip MC1/MC2 Pomodoro scanners skip managed lines
  ---
  duration_ms: 1.05756
  ...
# Subtest: explicit task IDs exclusively own dependency lookup
ok 5 - explicit task IDs exclusively own dependency lookup
  ---
  duration_ms: 2.626515
  ...
# Subtest: legacy tasks without an id field still fall back to their block ID
ok 6 - legacy tasks without an id field still fall back to their block ID
  ---
  duration_ms: 0.30343
  ...
# Subtest: blocked-link consumption raises open prerequisites and leaves the dependent blocked
ok 7 - blocked-link consumption raises open prerequisites and leaves the dependent blocked
  ---
  duration_ms: 1.15235
  ...
# Subtest: project-blocked member consumption promotes the project's open prerequisite
ok 8 - project-blocked member consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.672615
  ...
# Subtest: project-blocked resident consumption promotes the project's open prerequisite
ok 9 - project-blocked resident consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.412278
  ...
# Subtest: a tagged inherited ^prj target is refused with its parent named
ok 10 - a tagged inherited ^prj target is refused with its parent named
  ---
  duration_ms: 0.363995
  ...
# Subtest: project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
ok 11 - project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
  ---
  duration_ms: 1.461872
  ...
# Subtest: project date refusal applies only when the date is the sole project reason
ok 12 - project date refusal applies only when the date is the sole project reason
  ---
  duration_ms: 0.234928
  ...
# Subtest: a project-blocked tag is token-bounded and ignored on lookalike tags
ok 13 - a project-blocked tag is token-bounded and ignored on lookalike tags
  ---
  duration_ms: 0.375507
  ...
# Subtest: task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
ok 14 - task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
  ---
  duration_ms: 0.786722
  ...
# Subtest: task blocked state unifies status and dependency reasons
ok 15 - task blocked state unifies status and dependency reasons
  ---
  duration_ms: 0.339569
  ...
# Subtest: task picker partition sinks blocked tasks while preserving group order
ok 16 - task picker partition sinks blocked tasks while preserving group order
  ---
  duration_ms: 0.186877
  ...
# Subtest: blocked chip labels show useful unmet dependency counts
ok 17 - blocked chip labels show useful unmet dependency counts
  ---
  duration_ms: 0.103217
  ...
# Subtest: blocked tooltips explain dependency and status-only reasons
ok 18 - blocked tooltips explain dependency and status-only reasons
  ---
  duration_ms: 0.222465
  ...
# Subtest: task status classes cover every open task status
ok 19 - task status classes cover every open task status
  ---
  duration_ms: 0.090052
  ...
# Subtest: Blocked tasks remain unmet dependency targets
ok 20 - Blocked tasks remain unmet dependency targets
  ---
  duration_ms: 0.137312
  ...
# Subtest: blocked task count covers both reasons without double-counting
ok 21 - blocked task count covers both reasons without double-counting
  ---
  duration_ms: 0.11486
  ...
# Subtest: single caret relocation preserves embedding and removes aliases
ok 22 - single caret relocation preserves embedding and removes aliases
  ---
  duration_ms: 1.566081
  ...
# Subtest: single caret relocation resets aliased block links
ok 23 - single caret relocation resets aliased block links
  ---
  duration_ms: 0.238015
  ...
# Subtest: single caret relocation strips heading and block subpaths
ok 24 - single caret relocation strips heading and block subpaths
  ---
  duration_ms: 0.247994
  ...
# Subtest: task picker normalizes every supported wiki block-link form
ok 25 - task picker normalizes every supported wiki block-link form
  ---
  duration_ms: 0.655112
  ...
# Subtest: three or more carets never trigger the task picker
ok 26 - three or more carets never trigger the task picker
  ---
  duration_ms: 0.175335
  ...
# Subtest: rapid aliased task picker completion preserves the alias
ok 27 - rapid aliased task picker completion preserves the alias
  ---
  duration_ms: 2.444559
  ...
# Subtest: task picker recognition is independent of Markdown source context
ok 28 - task picker recognition is independent of Markdown source context
  ---
  duration_ms: 0.764601
  ...
# Subtest: task picker recognition respects cursor proximity and fenced code
ok 29 - task picker recognition respects cursor proximity and fenced code
  ---
  duration_ms: 0.255087
  ...
# Subtest: plan budget suffix: link Notice appends the meter computed on post-write daily content
ok 30 - plan budget suffix: link Notice appends the meter computed on post-write daily content
  ---
  duration_ms: 7.217385
  ...
# Subtest: plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
ok 31 - plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
  ---
  duration_ms: 0.917994
  ...
# Subtest: plan budget suffix: unlink Notice marks an over-cap plan with 🔴
ok 32 - plan budget suffix: unlink Notice marks an over-cap plan with 🔴
  ---
  duration_ms: 3.002655
  ...
# Subtest: plan budget suffix: Next task without a block ID prompts for one and omits the meter
ok 33 - plan budget suffix: Next task without a block ID prompts for one and omits the meter
  ---
  duration_ms: 0.447053
  ...
# Subtest: plan budget suffix: Task Link Notice appends the meter from post-write daily content
ok 34 - plan budget suffix: Task Link Notice appends the meter from post-write daily content
  ---
  duration_ms: 2.234848
  ...
# Subtest: plan budget suffix: Task Link Notice omits the meter when no daily note takes part
ok 35 - plan budget suffix: Task Link Notice omits the meter when no daily note takes part
  ---
  duration_ms: 0.557325
  ...
# Subtest: planTargetTaskUpdate stamps the rewritten line last via injected stamper
ok 36 - planTargetTaskUpdate stamps the rewritten line last via injected stamper
  ---
  duration_ms: 0.279423
  ...
# Subtest: planTargetTaskUpdate without a stamper never stamps (identity default)
ok 37 - planTargetTaskUpdate without a stamper never stamps (identity default)
  ---
  duration_ms: 0.153353
  ...
# Subtest: planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
ok 38 - planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
  ---
  duration_ms: 0.441403
  ...
# Subtest: planTargetTaskUpdate stamps a Next task that gains a block ID
ok 39 - planTargetTaskUpdate stamps a Next task that gains a block ID
  ---
  duration_ms: 0.471952
  ...
# Subtest: planTargetTaskUpdate tolerates a throwing stamper
ok 40 - planTargetTaskUpdate tolerates a throwing stamper
  ---
  duration_ms: 0.21467
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 41 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.431814
  ...
# Subtest: dedicated-link helpers reject Depends-On lines
ok 42 - dedicated-link helpers reject Depends-On lines
  ---
  duration_ms: 0.320913
  ...
# Subtest: Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
ok 43 - Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
  ---
  duration_ms: 0.350349
  ...
# Subtest: malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
ok 44 - malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
  ---
  duration_ms: 0.114759
  ...
# Subtest: Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
ok 45 - Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
  ---
  duration_ms: 0.302197
  ...
# Subtest: Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
ok 46 - Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
  ---
  duration_ms: 0.263283
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent
ok 47 - readPlanBudgetMeter keeps per-cap over flags independent
  ---
  duration_ms: 0.239968
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent (mirror)
ok 48 - readPlanBudgetMeter keeps per-cap over flags independent (mirror)
  ---
  duration_ms: 0.130278
  ...
# Subtest: block-id-prompt freshness accessors degrade without ledger-tools
ok 49 - block-id-prompt freshness accessors degrade without ledger-tools
  ---
  duration_ms: 0.271799
  ...
# Subtest: list item body bounds trim whitespace and reject empty bullets
ok 50 - list item body bounds trim whitespace and reject empty bullets
  ---
  duration_ms: 1.350479
  ...
# Subtest: Pomodoro activation eligibility requires a sole-content sub-bullet
ok 51 - Pomodoro activation eligibility requires a sole-content sub-bullet
  ---
  duration_ms: 1.962038
  ...
# Subtest: Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
ok 52 - Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
  ---
  duration_ms: 0.273763
  ...
# Subtest: Pomodoro source context distinguishes ledger ancestry and open state
ok 53 - Pomodoro source context distinguishes ledger ancestry and open state
  ---
  duration_ms: 0.45538
  ...
# Subtest: future cleanup touches only later open Pomodoros and counts duplicates
ok 54 - future cleanup touches only later open Pomodoros and counts duplicates
  ---
  duration_ms: 2.277059
  ...
# Subtest: cleanup resolves aliases, embeds, same-note links, and alternate paths
ok 55 - cleanup resolves aliases, embeds, same-note links, and alternate paths
  ---
  duration_ms: 1.618822
  ...
# Subtest: dedicated bullet subtree cleanup preserves CRLF line endings
ok 56 - dedicated bullet subtree cleanup preserves CRLF line endings
  ---
  duration_ms: 0.38745
  ...
# Subtest: existing-ID task completion prunes future links in the source editor
ok 57 - existing-ID task completion prunes future links in the source editor
  ---
  duration_ms: 2.426505
  ...
# Subtest: new-ID same-file completion plans cleanup after the task edit
ok 58 - new-ID same-file completion plans cleanup after the task edit
  ---
  duration_ms: 1.355409
  ...
# Subtest: findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
ok 59 - findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
  ---
  duration_ms: 2.093299
  ...
# Subtest: findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
ok 60 - findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
  ---
  duration_ms: 0.178791
  ...
# Subtest: findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
ok 61 - findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
  ---
  duration_ms: 0.18835
  ...
# Subtest: todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
ok 62 - todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
  ---
  duration_ms: 1.523811
  ...
# Subtest: todayDailyPath honors a custom Daily Notes format and an empty folder
ok 63 - todayDailyPath honors a custom Daily Notes format and an empty folder
  ---
  duration_ms: 0.242593
  ...
# Subtest: formatDailyDate resolves bracketed literal text alongside date tokens
ok 64 - formatDailyDate resolves bracketed literal text alongside date tokens
  ---
  duration_ms: 0.123276
  ...
# Subtest: getDailyNotesOptions reads the daily-notes core plugin's configured options
ok 65 - getDailyNotesOptions reads the daily-notes core plugin's configured options
  ---
  duration_ms: 0.658648
  ...
# Subtest: computeFencedLineFlags marks opening and closing fence lines and everything between
ok 66 - computeFencedLineFlags marks opening and closing fence lines and everything between
  ---
  duration_ms: 0.248174
  ...
# Subtest: selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
ok 67 - selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
  ---
  duration_ms: 0.748209
  ...
# Subtest: selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
ok 68 - selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
  ---
  duration_ms: 0.454908
  ...
# Subtest: selectPomodoroInsertionTarget rejects more than one open timed entry
ok 69 - selectPomodoroInsertionTarget rejects more than one open timed entry
  ---
  duration_ms: 0.231002
  ...
# Subtest: selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
ok 70 - selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
  ---
  duration_ms: 0.201134
  ...
# Subtest: findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
ok 71 - findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
  ---
  duration_ms: 0.173992
  ...
# Subtest: planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
ok 72 - planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
  ---
  duration_ms: 1.160867
  ...
# Subtest: planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
ok 73 - planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
  ---
  duration_ms: 1.468555
  ...
# Subtest: planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
ok 74 - planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
  ---
  duration_ms: 0.216754
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
ok 75 - planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
  ---
  duration_ms: 0.534441
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
ok 76 - planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
  ---
  duration_ms: 0.490167
  ...
# Subtest: planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
ok 77 - planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
  ---
  duration_ms: 0.36661
  ...
# Subtest: planPomodoroLinkInsertion inserts before the separator preceding later content
ok 78 - planPomodoroLinkInsertion inserts before the separator preceding later content
  ---
  duration_ms: 0.275717
  ...
# Subtest: planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
ok 79 - planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
  ---
  duration_ms: 0.322936
  ...
# Subtest: planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
ok 80 - planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
  ---
  duration_ms: 0.381549
  ...
# Subtest: existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
ok 81 - existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
  ---
  duration_ms: 3.030588
  ...
# Subtest: same-note Pomodoro link runtime composes the task update with adjacent insertion
ok 82 - same-note Pomodoro link runtime composes the task update with adjacent insertion
  ---
  duration_ms: 1.149856
  ...
# Subtest: new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
ok 83 - new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
  ---
  duration_ms: 0.585839
  ...
# Subtest: planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
ok 84 - planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
  ---
  duration_ms: 0.315824
  ...
# Subtest: all-open cleanup removes current and future links while preserving history and unresolved links
ok 85 - all-open cleanup removes current and future links while preserving history and unresolved links
  ---
  duration_ms: 0.871555
  ...
# Subtest: all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
ok 86 - all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
  ---
  duration_ms: 1.250559
  ...
# Subtest: all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
ok 87 - all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
  ---
  duration_ms: 0.218938
  ...
# Subtest: all-open cleanup treats missing section, no open entries, and no matches as no-op successes
ok 88 - all-open cleanup treats missing section, no open entries, and no matches as no-op successes
  ---
  duration_ms: 0.192247
  ...
# Subtest: composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
ok 89 - composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
  ---
  duration_ms: 0.268422
  ...
# Subtest: pomodoro link picker choices normalize to existing/new or null
ok 90 - pomodoro link picker choices normalize to existing/new or null
  ---
  duration_ms: 1.353385
  ...
# Subtest: pomodoroLinkPicker api never rejects and validates choices
ok 91 - pomodoroLinkPicker api never rejects and validates choices
  ---
  duration_ms: 0.363765
  ...
# Subtest: destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
ok 92 - destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
  ---
  duration_ms: 0.750734
  ...
# Subtest: destination pick with a section releases its guards when the modal cannot open
ok 93 - destination pick with a section releases its guards when the modal cannot open
  ---
  duration_ms: 1.628991
  ...
# Subtest: plugin lifecycle installs the api and drops it on unload
ok 94 - plugin lifecycle installs the api and drops it on unload
  ---
  duration_ms: 0.300093
  ...
# Subtest: Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
ok 95 - Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
  ---
  duration_ms: 2.458465
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor requires a single cursor
ok 96 - resolvePomodoroLinkTaskFromEditor requires a single cursor
  ---
  duration_ms: 0.339599
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
ok 97 - resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
  ---
  duration_ms: 0.397609
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
ok 98 - resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
  ---
  duration_ms: 0.420653
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
ok 99 - resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
  ---
  duration_ms: 0.49752
  ...
# Subtest: blocked-link consumption reports dependency reasons before the project date
ok 100 - blocked-link consumption reports dependency reasons before the project date
  ---
  duration_ms: 2.364236
  ...
# Subtest: Pomodoro link checks do not read other notes for a non-Blocked task
ok 101 - Pomodoro link checks do not read other notes for a non-Blocked task
  ---
  duration_ms: 0.284573
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
ok 102 - resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
  ---
  duration_ms: 0.363544
  ...
# Subtest: task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
ok 103 - task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
  ---
  duration_ms: 5.875643
  ...
# Subtest: task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
ok 104 - task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
  ---
  duration_ms: 1.723983
  ...
# Subtest: task-mode toggle: linked only under a completed Pomodoro links again
ok 105 - task-mode toggle: linked only under a completed Pomodoro links again
  ---
  duration_ms: 0.817541
  ...
# Subtest: task-mode toggle: a task without a block ID is never linked and prompts for one
ok 106 - task-mode toggle: a task without a block ID is never linked and prompts for one
  ---
  duration_ms: 0.417938
  ...
# Subtest: existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
ok 107 - existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
  ---
  duration_ms: 1.067989
  ...
# Subtest: forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
ok 108 - forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
  ---
  duration_ms: 0.512358
  ...
# Subtest: new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
ok 109 - new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
  ---
  duration_ms: 0.505055
  ...
# Subtest: submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
ok 110 - submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
  ---
  duration_ms: 0.137041
  ...
# Subtest: submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
ok 111 - submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
  ---
  duration_ms: 0.182639
  ...
# Subtest: same-note Pomodoro link runtime: task and ledger edits merge into one transaction
ok 112 - same-note Pomodoro link runtime: task and ledger edits merge into one transaction
  ---
  duration_ms: 1.128997
  ...
# Subtest: linking an already-linked Ready task raises it to Next without duplicating the link
ok 113 - linking an already-linked Ready task raises it to Next without duplicating the link
  ---
  duration_ms: 0.485788
  ...
# Subtest: Next task without a block ID preflights the picker before prompting
ok 114 - Next task without a block ID preflights the picker before prompting
  ---
  duration_ms: 0.435111
  ...
# Subtest: Pomodoro link stops before any mutation when today's daily note is missing
ok 115 - Pomodoro link stops before any mutation when today's daily note is missing
  ---
  duration_ms: 0.167159
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
ok 116 - Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
  ---
  duration_ms: 0.432556
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
ok 117 - Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
  ---
  duration_ms: 0.273493
  ...
# Subtest: Pomodoro link aborts without any write when the task line changed since it was selected
ok 118 - Pomodoro link aborts without any write when the task line changed since it was selected
  ---
  duration_ms: 0.155337
  ...
# Subtest: Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
ok 119 - Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
  ---
  duration_ms: 0.587462
  ...
# Subtest: canceling the Pomodoro block-ID modal leaves the note untouched
ok 120 - canceling the Pomodoro block-ID modal leaves the note untouched
  ---
  duration_ms: 0.157451
  ...
# Subtest: review-walk: existing-ID link hands its Linked notice to continue with no separate notice
ok 121 - review-walk: existing-ID link hands its Linked notice to continue with no separate notice
  ---
  duration_ms: 0.972958
  ...
# Subtest: review-walk: prompted-ID link continues after submit
ok 122 - review-walk: prompted-ID link continues after submit
  ---
  duration_ms: 1.265758
  ...
# Subtest: review-walk: prompt cancel settles with null
ok 123 - review-walk: prompt cancel settles with null
  ---
  duration_ms: 0.198278
  ...
# Subtest: review-walk: BUSY swallows the key with no write
ok 124 - review-walk: BUSY swallows the key with no write
  ---
  duration_ms: 0.381108
  ...
# Subtest: review-walk: failed link keeps its notice and settles with null
ok 125 - review-walk: failed link keeps its notice and settles with null
  ---
  duration_ms: 0.254065
  ...
# Subtest: review-walk: partial link keeps its notice and never continues with an outcome
ok 126 - review-walk: partial link keeps its notice and never continues with an outcome
  ---
  duration_ms: 1.004339
  ...
# Subtest: inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
ok 127 - inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
  ---
  duration_ms: 0.280265
  ...
# Subtest: inbox-route: non-inbox notes and task-link mode never prompt
ok 128 - inbox-route: non-inbox notes and task-link mode never prompt
  ---
  duration_ms: 0.86954
  ...
# Subtest: inbox-route: cancel writes nothing and settles once
ok 129 - inbox-route: cancel writes nothing and settles once
  ---
  duration_ms: 0.648689
  ...
# Subtest: inbox-route: stay matches today
ok 130 - inbox-route: stay matches today
  ---
  duration_ms: 1.838081
  ...
# Subtest: inbox-route: move links, then moves, with one composed toast and a route continue
ok 131 - inbox-route: move links, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.698214
  ...
# Subtest: inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
ok 132 - inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
  ---
  duration_ms: 0.666433
  ...
# Subtest: inbox-route: a move failure gives the partial notice plus a link-today continue
ok 133 - inbox-route: a move failure gives the partial notice plus a link-today continue
  ---
  duration_ms: 0.426715
  ...
# Subtest: review-walk: no nav or nav v2 keeps today's notices
ok 134 - review-walk: no nav or nav v2 keeps today's notices
  ---
  duration_ms: 0.889639
  ...
# Subtest: inbox-route: source drift during route prompt refuses without writes
ok 135 - inbox-route: source drift during route prompt refuses without writes
  ---
  duration_ms: 0.30386
  ...
# Subtest: inbox-route: block-ID route cancel returns sentinel and settles null once
ok 136 - inbox-route: block-ID route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.314721
  ...
# Subtest: inbox-route: link no-op with move never commits
ok 137 - inbox-route: link no-op with move never commits
  ---
  duration_ms: 0.179542
  ...
# Subtest: picker opens only on the link direction, never on unlink
ok 138 - picker opens only on the link direction, never on unlink
  ---
  duration_ms: 8.589856
  ...
# Subtest: picker never opens in task-link mode
ok 139 - picker never opens in task-link mode
  ---
  duration_ms: 2.90072
  ...
# Subtest: Depends-On refusals never open the picker
ok 140 - Depends-On refusals never open the picker
  ---
  duration_ms: 0.853009
  ...
# Subtest: preflight refusals open nothing
ok 141 - preflight refusals open nothing
  ---
  duration_ms: 0.483022
  ...
# Subtest: picking a non-default entry links there
ok 142 - picking a non-default entry links there
  ---
  duration_ms: 1.079301
  ...
# Subtest: cancel writes nothing with no Notice and settles the walk null
ok 143 - cancel writes nothing with no Notice and settles the walk null
  ---
  duration_ms: 0.594325
  ...
# Subtest: a no-ID task gets picker, then the block-ID prompt with the target carried
ok 144 - a no-ID task gets picker, then the block-ID prompt with the target carried
  ---
  duration_ms: 0.889789
  ...
# Subtest: inbox order is picker, then route, then write
ok 145 - inbox order is picker, then route, then write
  ---
  duration_ms: 0.737659
  ...
# Subtest: a review-walk landing continues with link-today and the new text
ok 146 - a review-walk landing continues with link-today and the new text
  ---
  duration_ms: 0.87999
  ...
# Subtest: an all-closed ledger creates a new entry after the last completed block
ok 147 - an all-closed ledger creates a new entry after the last completed block
  ---
  duration_ms: 1.584226
  ...
# Subtest: several running entries allow an explicit pick
ok 148 - several running entries allow an explicit pick
  ---
  duration_ms: 0.715828
  ...
# Subtest: a target that changed before commit refuses with no writes
ok 149 - a target that changed before commit refuses with no writes
  ---
  duration_ms: 0.478845
  ...
# Subtest: a target that closed before commit refuses with no writes
ok 150 - a target that closed before commit refuses with no writes
  ---
  duration_ms: 0.353615
  ...
# Subtest: the task note being the daily note uses one editor transaction
ok 151 - the task note being the daily note uses one editor transaction
  ---
  duration_ms: 0.600026
  ...
# Subtest: promptOpen blocks re-entry while the picker is open
ok 152 - promptOpen blocks re-entry while the picker is open
  ---
  duration_ms: 9.707873
  ...
# Subtest: header shows title, subtitle, lane chip per status, and block-ID chip
ok 153 - header shows title, subtitle, lane chip per status, and block-ID chip
  ---
  duration_ms: 8.571001
  ...
# Subtest: rows render in document order with the default selected
ok 154 - rows render in document order with the default selected
  ---
  duration_ms: 1.092577
  ...
# Subtest: running row shows progress fraction and minutes-left meta
ok 155 - running row shows progress fraction and minutes-left meta
  ---
  duration_ms: 0.968459
  ...
# Subtest: unnamed entries render muted italic
ok 156 - unnamed entries render muted italic
  ---
  duration_ms: 0.44023
  ...
# Subtest: filtering ranks, highlights, and clearing restores the default
ok 157 - filtering ranks, highlights, and clearing restores the default
  ---
  duration_ms: 1.073751
  ...
# Subtest: create row meta, divider, and theme badge
ok 158 - create row meta, divider, and theme badge
  ---
  duration_ms: 1.526456
  ...
# Subtest: exact open names suppress the create row; prefix matches keep it
ok 159 - exact open names suppress the create row; prefix matches keep it
  ---
  duration_ms: 0.644361
  ...
# Subtest: theme badge turns red over cap; a throwing budget hides the detail
ok 160 - theme badge turns red over cap; a throwing budget hides the detail
  ---
  duration_ms: 1.999069
  ...
# Subtest: invalid rows explain the grammar and are inert on Enter
ok 161 - invalid rows explain the grammar and are inert on Enter
  ---
  duration_ms: 10.396537
  ...
# Subtest: multiple running entries show the banner, no pills, and block creation
ok 162 - multiple running entries show the banner, no pills, and block creation
  ---
  duration_ms: 1.620775
  ...
# Subtest: navigation wraps and skips non-selectable rows
ok 163 - navigation wraps and skips non-selectable rows
  ---
  duration_ms: 1.259315
  ...
# Subtest: empty state invites planning a Pomodoro
ok 164 - empty state invites planning a Pomodoro
  ---
  duration_ms: 0.254175
  ...
# Subtest: footer hints and plan meter
ok 165 - footer hints and plan meter
  ---
  duration_ms: 1.198218
  ...
# Subtest: Enter chooses the selected row; click chooses that row
ok 166 - Enter chooses the selected row; click chooses that row
  ---
  duration_ms: 0.689407
  ...
# Subtest: Shift+Enter creates; an exact open name links there instead
ok 167 - Shift+Enter creates; an exact open name links there instead
  ---
  duration_ms: 0.900309
  ...
# Subtest: Ctrl+Shift+Enter commits exactly like Enter
ok 168 - Ctrl+Shift+Enter commits exactly like Enter
  ---
  duration_ms: 2.018044
  ...
# Subtest: Escape and Ctrl+[ cancel with no choice; settle-once holds
ok 169 - Escape and Ctrl+[ cancel with no choice; settle-once holds
  ---
  duration_ms: 0.861986
  ...
# Subtest: canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
ok 170 - canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
  ---
  duration_ms: 1.65973
  ...
# Subtest: canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
ok 171 - canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
  ---
  duration_ms: 0.283401
  ...
# Subtest: pomodoroLinkSelectorSlug mirrors capture slugs
ok 172 - pomodoroLinkSelectorSlug mirrors capture slugs
  ---
  duration_ms: 1.150688
  ...
# Subtest: parsePomodoroEntryParts reads canonical and legacy entry lines
ok 173 - parsePomodoroEntryParts reads canonical and legacy entry lines
  ---
  duration_ms: 0.980733
  ...
# Subtest: collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
ok 174 - collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
  ---
  duration_ms: 1.583685
  ...
# Subtest: collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
ok 175 - collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
  ---
  duration_ms: 0.98953
  ...
# Subtest: collectPomodoroLinkEntries counts links but excludes struck references
ok 176 - collectPomodoroLinkEntries counts links but excludes struck references
  ---
  duration_ms: 0.451432
  ...
# Subtest: collectPomodoroLinkEntries falls back to range text and position titles
ok 177 - collectPomodoroLinkEntries falls back to range text and position titles
  ---
  duration_ms: 0.283311
  ...
# Subtest: pomodoroRunProgress reports fractions, overtime, and midnight wrap
ok 178 - pomodoroRunProgress reports fractions, overtime, and midnight wrap
  ---
  duration_ms: 0.537897
  ...
# Subtest: buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
ok 179 - buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
  ---
  duration_ms: 0.797693
  ...
# Subtest: buildPomodoroLinkPickerRows keeps the create row for prefix matches
ok 180 - buildPomodoroLinkPickerRows keeps the create row for prefix matches
  ---
  duration_ms: 0.309552
  ...
# Subtest: buildPomodoroLinkPickerRows marks completed-only names as again
ok 181 - buildPomodoroLinkPickerRows marks completed-only names as again
  ---
  duration_ms: 0.189261
  ...
# Subtest: buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
ok 182 - buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
  ---
  duration_ms: 0.378823
  ...
# Subtest: buildPomodoroLinkPickerRows matches times, positions, and block IDs
ok 183 - buildPomodoroLinkPickerRows matches times, positions, and block IDs
  ---
  duration_ms: 0.462563
  ...
# Subtest: resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
ok 184 - resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
  ---
  duration_ms: 0.338486
  ...
# Subtest: defaultPomodoroLinkChoice returns the default entry or null
ok 185 - defaultPomodoroLinkChoice returns the default entry or null
  ---
  duration_ms: 0.195032
  ...
# Subtest: planExplicitPomodoroLinkInsertion links under a chosen existing entry
ok 186 - planExplicitPomodoroLinkInsertion links under a chosen existing entry
  ---
  duration_ms: 0.97405
  ...
# Subtest: planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
ok 187 - planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
  ---
  duration_ms: 0.272671
  ...
# Subtest: planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
ok 188 - planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
  ---
  duration_ms: 1.094581
  ...
# Subtest: planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
ok 189 - planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
  ---
  duration_ms: 0.373954
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after the running entry
ok 190 - planExplicitPomodoroLinkInsertion creates after the running entry
  ---
  duration_ms: 0.657345
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
ok 191 - planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
  ---
  duration_ms: 0.728842
  ...
# Subtest: planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
ok 192 - planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
  ---
  duration_ms: 0.384805
  ...
# Subtest: planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
ok 193 - planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
  ---
  duration_ms: 0.415514
  ...
# Subtest: planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
ok 194 - planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
  ---
  duration_ms: 0.581941
  ...
# Subtest: buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
ok 195 - buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
  ---
  duration_ms: 0.231863
  ...
# Subtest: buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
ok 196 - buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
  ---
  duration_ms: 0.234538
  ...
# Subtest: planExplicitPomodoroLinkInsertion matches mixed-case raced open names
ok 197 - planExplicitPomodoroLinkInsertion matches mixed-case raced open names
  ---
  duration_ms: 0.291236
  ...
# Subtest: buildPomodoroLinkPickerRows bounds \#N position matches
ok 198 - buildPomodoroLinkPickerRows bounds \#N position matches
  ---
  duration_ms: 0.519653
  ...
# Subtest: planPomodoroLinkInsertion without a target keeps today's behavior and shape
ok 199 - planPomodoroLinkInsertion without a target keeps today's behavior and shape
  ---
  duration_ms: 0.623511
  ...
# Subtest: direct unlink without a daily note keeps the Next lane and reports it
ok 200 - direct unlink without a daily note keeps the Next lane and reports it
  ---
  duration_ms: 2.285054
  ...
# Subtest: In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
ok 201 - In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
  ---
  duration_ms: 0.434039
  ...
# Subtest: In Progress unlink with a summary keeps the lane and creates a Work Log
ok 202 - In Progress unlink with a summary keeps the lane and creates a Work Log
  ---
  duration_ms: 1.266319
  ...
# Subtest: In Progress unlink revalidates task text and block-ID uniqueness at confirmation
ok 203 - In Progress unlink revalidates task text and block-ID uniqueness at confirmation
  ---
  duration_ms: 1.316293
  ...
# Subtest: Next task unlink removes current and future links and keeps the Next lane
ok 204 - Next task unlink removes current and future links and keeps the Next lane
  ---
  duration_ms: 3.918463
  ...
# Subtest: In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
ok 205 - In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
  ---
  duration_ms: 0.791712
  ...
# Subtest: same-note Next unlink merges the Work Log and all-open cleanup in the active editor
ok 206 - same-note Next unlink merges the Work Log and all-open cleanup in the active editor
  ---
  duration_ms: 0.798455
  ...
# Subtest: same-note In Progress unlink merges cleanup and Work Log in the active editor
ok 207 - same-note In Progress unlink merges cleanup and Work Log in the active editor
  ---
  duration_ms: 0.579176
  ...
# Subtest: Next unlink stops before any write when daily cleanup write is stale
ok 208 - Next unlink stops before any write when daily cleanup write is stale
  ---
  duration_ms: 0.773859
  ...
# Subtest: Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
ok 209 - Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
  ---
  duration_ms: 1.018185
  ...
# Subtest: In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
ok 210 - In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
  ---
  duration_ms: 0.658037
  ...
# Subtest: review-walk: unlink settles with null and keeps its notice
ok 211 - review-walk: unlink settles with null and keeps its notice
  ---
  duration_ms: 1.230039
  ...
# Subtest: inbox-route: unlink cancel writes nothing
ok 212 - inbox-route: unlink cancel writes nothing
  ---
  duration_ms: 0.352283
  ...
# Subtest: inbox-route: unlink stay matches today and never commits
ok 213 - inbox-route: unlink stay matches today and never commits
  ---
  duration_ms: 0.545381
  ...
# Subtest: inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
ok 214 - inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.653158
  ...
# Subtest: inbox-route: In Progress unlink with a Work summary routes
ok 215 - inbox-route: In Progress unlink with a Work summary routes
  ---
  duration_ms: 0.794197
  ...
# Subtest: inbox-route: unlink move failure gives the partial notice and stays
ok 216 - inbox-route: unlink move failure gives the partial notice and stays
  ---
  duration_ms: 0.38739
  ...
# Subtest: inbox-route: non-inbox unlink never prompts
ok 217 - inbox-route: non-inbox unlink never prompts
  ---
  duration_ms: 0.376139
  ...
# Subtest: review-walk: Work-summary unlink path retains origin until submit
ok 218 - review-walk: Work-summary unlink path retains origin until submit
  ---
  duration_ms: 0.395856
  ...
# Subtest: inbox-route: unlink source drift during route prompt refuses without writes
ok 219 - inbox-route: unlink source drift during route prompt refuses without writes
  ---
  duration_ms: 0.29296
  ...
# Subtest: inbox-route: Work-summary route cancel returns sentinel and settles null once
ok 220 - inbox-route: Work-summary route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.285055
  ...
# Subtest: inbox-route: unlink no-op with move never commits
ok 221 - inbox-route: unlink no-op with move never commits
  ---
  duration_ms: 0.220691
  ...
# Subtest: same-note unlink maps a task below removed entries through Work-summary inserts
ok 222 - same-note unlink maps a task below removed entries through Work-summary inserts
  ---
  duration_ms: 0.580679
  ...
# Subtest: direct-add seeds from the task headline, not non-task blocks
ok 223 - direct-add seeds from the task headline, not non-task blocks
  ---
  duration_ms: 3.443117
  ...
# Subtest: link-task-complete seeds from the target, prefers open buffers
ok 224 - link-task-complete seeds from the target, prefers open buffers
  ---
  duration_ms: 0.941818
  ...
# Subtest: link-task-complete reports stale and unreadable targets
ok 225 - link-task-complete reports stale and unreadable targets
  ---
  duration_ms: 0.309691
  ...
# Subtest: pomodoro link seeds after the choice from the cursor task
ok 226 - pomodoro link seeds after the choice from the cursor task
  ---
  duration_ms: 0.271469
  ...
# Subtest: marker rename suggests from the unique task, never hiding ambiguity
ok 227 - marker rename suggests from the unique task, never hiding ambiguity
  ---
  duration_ms: 0.53377
  ...
# Subtest: modal seeds the value, selects once, and never overwrites typing
ok 228 - modal seeds the value, selects once, and never overwrites typing
  ---
  duration_ms: 1.284063
  ...
# Subtest: modal disables Save while loading and survives close/reopen
ok 229 - modal disables Save while loading and survives close/reopen
  ---
  duration_ms: 2.17274
  ...
# Subtest: submit revalidates: occupied IDs and stale tasks fail editable
ok 230 - submit revalidates: occupied IDs and stale tasks fail editable
  ---
  duration_ms: 0.528159
  ...
# Subtest: cancelling writes no ID and explicit renames keep the current ID
ok 231 - cancelling writes no ID and explicit renames keep the current ID
  ---
  duration_ms: 0.819215
  ...
# Subtest: the task picker drops the paired \#ref and prefixes the book
ok 232 - the task picker drops the paired \#ref and prefixes the book
  ---
  duration_ms: 2.506738
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 233 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.320823
  ...
# Subtest: block-id-prompt LK1–LK19 recognises only relation line shapes
ok 234 - block-id-prompt LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 1.420263
  ...
# Subtest: block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
ok 235 - block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
  ---
  duration_ms: 1.087086
  ...
# Subtest: block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
ok 236 - block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
  ---
  duration_ms: 1.297058
  ...
# Subtest: calendar date parsing rejects malformed width and impossible dates
ok 237 - calendar date parsing rejects malformed width and impossible dates
  ---
  duration_ms: 2.061608
  ...
# Subtest: future scheduled field detection respects the yesterday/today/tomorrow boundary
ok 238 - future scheduled field detection respects the yesterday/today/tomorrow boundary
  ---
  duration_ms: 1.464357
  ...
# Subtest: scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
ok 239 - scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
  ---
  duration_ms: 0.208137
  ...
# Subtest: planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
ok 240 - planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
  ---
  duration_ms: 1.045907
  ...
# Subtest: planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
ok 241 - planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
  ---
  duration_ms: 0.217766
  ...
# Subtest: planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
ok 242 - planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
  ---
  duration_ms: 0.168381
  ...
# Subtest: planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
ok 243 - planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
  ---
  duration_ms: 0.1678
  ...
# Subtest: planTargetTaskUpdate leaves today and past schedules untouched
ok 244 - planTargetTaskUpdate leaves today and past schedules untouched
  ---
  duration_ms: 0.298069
  ...
# Subtest: planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
ok 245 - planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
  ---
  duration_ms: 0.368323
  ...
# Subtest: two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
ok 246 - two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
  ---
  duration_ms: 0.456873
  ...
# Subtest: a malformed single scheduled field is never treated as future
ok 247 - a malformed single scheduled field is never treated as future
  ---
  duration_ms: 0.186556
  ...
# Subtest: an ambiguous scheduled field does not block the legacy Ready promotion
ok 248 - an ambiguous scheduled field does not block the legacy Ready promotion
  ---
  duration_ms: 0.189743
  ...
# Subtest: planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
ok 249 - planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
  ---
  duration_ms: 0.13072
  ...
# Subtest: Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
ok 250 - Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
  ---
  duration_ms: 0.481339
  ...
# Subtest: Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
ok 251 - Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
  ---
  duration_ms: 0.169003
  ...
# Subtest: planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
ok 252 - planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
  ---
  duration_ms: 0.260738
  ...
# Subtest: planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
ok 253 - planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
  ---
  duration_ms: 0.141981
  ...
# Subtest: planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
ok 254 - planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.123796
  ...
# Subtest: planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
ok 255 - planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
  ---
  duration_ms: 0.152591
  ...
# Subtest: planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
ok 256 - planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
  ---
  duration_ms: 0.141
  ...
# Subtest: planTargetTaskUpdate preserves a trailing newline when one was already present
ok 257 - planTargetTaskUpdate preserves a trailing newline when one was already present
  ---
  duration_ms: 0.137222
  ...
# Subtest: planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
ok 258 - planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
  ---
  duration_ms: 0.110161
  ...
# Subtest: planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
ok 259 - planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
  ---
  duration_ms: 0.170716
  ...
# Subtest: planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
ok 260 - planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
  ---
  duration_ms: 0.128445
  ...
# Subtest: existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
ok 261 - existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
  ---
  duration_ms: 3.264064
  ...
# Subtest: new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
ok 262 - new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
  ---
  duration_ms: 0.972116
  ...
# Subtest: activation runtime aborts without any write when the target preimage goes stale
ok 263 - activation runtime aborts without any write when the target preimage goes stale
  ---
  duration_ms: 0.552575
  ...
# Subtest: same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
ok 264 - same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
  ---
  duration_ms: 2.880671
  ...
# Subtest: same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
ok 265 - same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
  ---
  duration_ms: 0.656103
  ...
# Subtest: a source marker edited after a successful existing-ID target write reports an accurate partial notice
ok 266 - a source marker edited after a successful existing-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.516286
  ...
# Subtest: a source marker edited after a successful new-ID target write reports an accurate partial notice
ok 267 - a source marker edited after a successful new-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.558246
  ...
# Subtest: planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
ok 268 - planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
  ---
  duration_ms: 0.169984
  ...
# Subtest: planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
ok 269 - planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
  ---
  duration_ms: 0.116032
  ...
# Subtest: planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
ok 270 - planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
  ---
  duration_ms: 0.128285
  ...
# Subtest: planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
ok 271 - planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.121081
  ...
# Subtest: direct Task Links raise ^prj while never pulling its date forward
ok 272 - direct Task Links raise ^prj while never pulling its date forward
  ---
  duration_ms: 0.129056
  ...
# Subtest: task-link selection: one link is selectable from any column, several are chosen by cursor
ok 273 - task-link selection: one link is selectable from any column, several are chosen by cursor
  ---
  duration_ms: 5.262361
  ...
# Subtest: task-link selection ignores picker/rename markers, plain links, and Markdown-style links
ok 274 - task-link selection ignores picker/rename markers, plain links, and Markdown-style links
  ---
  duration_ms: 0.435472
  ...
# Subtest: dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
ok 275 - dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
  ---
  duration_ms: 0.901783
  ...
# Subtest: inline Task Link deletion removes the token with its decoration and collapses whitespace
ok 276 - inline Task Link deletion removes the token with its decoration and collapses whitespace
  ---
  duration_ms: 0.897013
  ...
# Subtest: dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
ok 277 - dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
  ---
  duration_ms: 1.21979
  ...
# Subtest: mergeCoveringEdits keeps the covering edit and the earlier of identical edits
ok 278 - mergeCoveringEdits keeps the covering edit and the earlier of identical edits
  ---
  duration_ms: 0.285736
  ...
# Subtest: dependency transclusion detection needs an embedded sole-content child of a \#task line
ok 279 - dependency transclusion detection needs an embedded sole-content child of a \#task line
  ---
  duration_ms: 0.616267
  ...
# Subtest: Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
ok 280 - Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
  ---
  duration_ms: 6.289671
  ...
# Subtest: Task Link on a Next target works from an embedded aliased link outside any Pomodoro
ok 281 - Task Link on a Next target works from an embedded aliased link outside any Pomodoro
  ---
  duration_ms: 1.457995
  ...
# Subtest: same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
ok 282 - same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
  ---
  duration_ms: 1.142432
  ...
# Subtest: same-note Task Link deletion clamps the restored cursor to the shortened note
ok 283 - same-note Task Link deletion clamps the restored cursor to the shortened note
  ---
  duration_ms: 0.547356
  ...
# Subtest: a cleanup subtree that covers a nested selected link wins and links are not double counted
ok 284 - a cleanup subtree that covers a nested selected link wins and links are not double counted
  ---
  duration_ms: 0.928764
  ...
# Subtest: same-note Task Link in a closed entry deletes the closed entry it empties
ok 285 - same-note Task Link in a closed entry deletes the closed entry it empties
  ---
  duration_ms: 0.612831
  ...
# Subtest: Task Link in another day's note deletes the emptied entry there and in today's note
ok 286 - Task Link in another day's note deletes the emptied entry there and in today's note
  ---
  duration_ms: 0.580298
  ...
# Subtest: Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
ok 287 - Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
  ---
  duration_ms: 1.498041
  ...
# Subtest: Task Link on an In Progress target with a blank summary logs nothing
ok 288 - Task Link on an In Progress target with a blank summary logs nothing
  ---
  duration_ms: 0.935247
  ...
# Subtest: canceling the In Progress Task Link prompt leaves everything untouched
ok 289 - canceling the In Progress Task Link prompt leaves everything untouched
  ---
  duration_ms: 0.384164
  ...
# Subtest: canceling the In Progress unlink prompt in task mode leaves everything untouched
ok 290 - canceling the In Progress unlink prompt in task mode leaves everything untouched
  ---
  duration_ms: 0.828202
  ...
# Subtest: In Progress Task Link submit revalidates the link line and the target task
ok 291 - In Progress Task Link submit revalidates the link line and the target task
  ---
  duration_ms: 0.666513
  ...
# Subtest: Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
ok 292 - Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
  ---
  duration_ms: 0.690509
  ...
# Subtest: Task Link on a Done or Cancelled target is refused without edits
ok 293 - Task Link on a Done or Cancelled target is refused without edits
  ---
  duration_ms: 0.377942
  ...
# Subtest: Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
ok 294 - Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
  ---
  duration_ms: 0.672464
  ...
# Subtest: precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
ok 295 - precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
  ---
  duration_ms: 1.334468
  ...
# Subtest: Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
ok 296 - Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
  ---
  duration_ms: 0.485518
  ...
# Subtest: Task Link that is a sub-task dependency transclusion is refused without edits
ok 297 - Task Link that is a sub-task dependency transclusion is refused without edits
  ---
  duration_ms: 0.239447
  ...
# Subtest: Task Link partial failure after the daily write is retryable
ok 298 - Task Link partial failure after the daily write is retryable
  ---
  duration_ms: 2.85855
  ...
# Subtest: Task Link stops before any write when the target note changes after planning
ok 299 - Task Link stops before any write when the target note changes after planning
  ---
  duration_ms: 0.66479
  ...
# Subtest: Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
ok 300 - Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
  ---
  duration_ms: 0.590878
  ...
# Subtest: Task Link subtree deletion removes a nested target task without any status write
ok 301 - Task Link subtree deletion removes a nested target task without any status write
  ---
  duration_ms: 0.416576
  ...
# Subtest: whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
ok 302 - whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
  ---
  duration_ms: 0.906601
  ...
# Subtest: selected-link deletion maps a cursor inside a removed entry to its former start
ok 303 - selected-link deletion maps a cursor inside a removed entry to its former start
  ---
  duration_ms: 0.584536
  ...
# Subtest: work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
ok 304 - work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
  ---
  duration_ms: 1.550551
  ...
# Subtest: work log date helpers use local calendar components
ok 305 - work log date helpers use local calendar components
  ---
  duration_ms: 0.267491
  ...
# Subtest: planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
ok 306 - planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
  ---
  duration_ms: 0.679508
  ...
# Subtest: planWorkLogInsertion inherits an existing space-indented child prefix
ok 307 - planWorkLogInsertion inherits an existing space-indented child prefix
  ---
  duration_ms: 0.486519
  ...
# Subtest: planWorkLogInsertion inherits an existing tab-indented child prefix
ok 308 - planWorkLogInsertion inherits an existing tab-indented child prefix
  ---
  duration_ms: 0.229768
  ...
# Subtest: planWorkLogInsertion prepends newest-first entries into existing marker spellings
ok 309 - planWorkLogInsertion prepends newest-first entries into existing marker spellings
  ---
  duration_ms: 0.500316
  ...
# Subtest: planWorkLogInsertion ignores nested child-task markers and preserves CRLF
ok 310 - planWorkLogInsertion ignores nested child-task markers and preserves CRLF
  ---
  duration_ms: 0.378242
  ...
# Subtest: planWorkLogInsertion treats blank summaries as no-op structural edits
ok 311 - planWorkLogInsertion treats blank summaries as no-op structural edits
  ---
  duration_ms: 0.138103
  ...
# Subtest: the Open-reset planner is removed: unlink plans only a Work Log insertion
ok 312 - the Open-reset planner is removed: unlink plans only a Work Log insertion
  ---
  duration_ms: 0.32433
  ...
# Subtest: unlink Work Log plan keeps the In Progress checkbox and appends one entry
ok 313 - unlink Work Log plan keeps the In Progress checkbox and appends one entry
  ---
  duration_ms: 0.415384
  ...
# Subtest: article detection accepts scalar and list frontmatter values
ok 314 - article detection accepts scalar and list frontmatter values
  ---
  duration_ms: 1.64397
  ...
# Subtest: bob resolution prefers its setting, then known install paths, then PATH
ok 315 - bob resolution prefers its setting, then known install paths, then PATH
  ---
  duration_ms: 0.756174
  ...
# Subtest: plan decoder accepts v1 and rejects a foreign schema version
ok 316 - plan decoder accepts v1 and rejects a foreign schema version
  ---
  duration_ms: 0.278342
  ...
# Subtest: bob stdin spawn passes the article contract and vault environment
ok 317 - bob stdin spawn passes the article contract and vault environment
  ---
  duration_ms: 2.415704
  ...
# Subtest: bob plan stdout decodes UTF-8 split across chunks
ok 318 - bob plan stdout decodes UTF-8 split across chunks
  ---
  duration_ms: 0.780471
  ...
# Subtest: early bob exit on stdin reports EPIPE as a run failure
ok 319 - early bob exit on stdin reports EPIPE as a run failure
  ---
  duration_ms: 0.673035
  ...
# Subtest: line hunks become minimal cursor-preserving changes
ok 320 - line hunks become minimal cursor-preserving changes
  ---
  duration_ms: 0.672965
  ...
# Subtest: insert, multi-line replace, and deletion hunks reproduce the formatted note
ok 321 - insert, multi-line replace, and deletion hunks reproduce the formatted note
  ---
  duration_ms: 2.833812
  ...
# Subtest: notice shows bob's text and at most two warning findings
ok 322 - notice shows bob's text and at most two warning findings
  ---
  duration_ms: 0.390716
  ...
# Subtest: inbound changes apply only when their target line still matches the preimage
ok 323 - inbound changes apply only when their target line still matches the preimage
  ---
  duration_ms: 0.679157
  ...
# Subtest: undo guard blocks a reformat until a fresh input or delete event
ok 324 - undo guard blocks a reformat until a fresh input or delete event
  ---
  duration_ms: 0.378333
  ...
# Subtest: leave formatting observes the undo guard before saving or reading
ok 325 - leave formatting observes the undo guard before saving or reading
  ---
  duration_ms: 0.285996
  ...
# Subtest: Convert shows bob's refusal on every invocation
ok 326 - Convert shows bob's refusal on every invocation
  ---
  duration_ms: 0.305233
  ...
# Subtest: old bob's non-JSON article response gets one update notice per session
ok 327 - old bob's non-JSON article response gets one update notice per session
  ---
  duration_ms: 0.154806
  ...
# Subtest: format drops its response if the editor changed while bob was running
ok 328 - format drops its response if the editor changed while bob was running
  ---
  duration_ms: 0.304151
  ...
# Subtest: decoration ranges mark written section numbers from the outline
ok 329 - decoration ranges mark written section numbers from the outline
  ---
  duration_ms: 0.776673
  ...
# Subtest: a new outline rerenders each open Reading view once for that generation
ok 330 - a new outline rerenders each open Reading view once for that generation
  ---
  duration_ms: 0.423269
  ...
# Subtest: section at a given line uses the innermost outline range
ok 331 - section at a given line uses the innermost outline range
  ---
  duration_ms: 0.365649
  ...
# Subtest: stale-hint debounce and in-flight state machine
ok 332 - stale-hint debounce and in-flight state machine
  ---
  duration_ms: 0.404312
  ...
# Subtest: reading-view wrapping puts the leading number token in span.bob-secno
ok 333 - reading-view wrapping puts the leading number token in span.bob-secno
  ---
  duration_ms: 0.809505
  ...
# Subtest: applied plans remap outline lines onto the formatted buffer
ok 334 - applied plans remap outline lines onto the formatted buffer
  ---
  duration_ms: 0.192337
  ...
# Subtest: article styles scope the reading look under .bob-article
ok 335 - article styles scope the reading look under .bob-article
  ---
  duration_ms: 1.554558
  ...
# Subtest: look settings default to serif typeface and stale-number hints
ok 336 - look settings default to serif typeface and stale-number hints
  ---
  duration_ms: 0.111172
  ...
# Subtest: folds embed, struck, and plain legacy children into one canonical line
ok 337 - folds embed, struck, and plain legacy children into one canonical line
  ---
  duration_ms: 63.169027
  ...
# Subtest: legacy-label row links come first, then legacy children in order
ok 338 - legacy-label row links come first, then legacy children in order
  ---
  duration_ms: 1.74311
  ...
# Subtest: R2 adopts field-only open dependents; unadoptable ids stay warned
ok 339 - R2 adopts field-only open dependents; unadoptable ids stay warned
  ---
  duration_ms: 0.569608
  ...
# Subtest: closed dependents gain the line but keep the field untouched
ok 340 - closed dependents gain the line but keep the field untouched
  ---
  duration_ms: 0.92184
  ...
# Subtest: open dependents drop stale field ids and stamp targets missing [id::]
ok 341 - open dependents drop stale field ids and stamp targets missing [id::]
  ---
  duration_ms: 0.589205
  ...
# Subtest: unresolved links stay verbatim and keep field ids as breadcrumbs
ok 342 - unresolved links stay verbatim and keep field ids as breadcrumbs
  ---
  duration_ms: 0.510986
  ...
# Subtest: leaves \#^ref embeds, non-task parents, fences, and conflict children alone
ok 343 - leaves \#^ref embeds, non-task parents, fences, and conflict children alone
  ---
  duration_ms: 0.683445
  ...
# Subtest: malformed rows leave the whole dependent alone
ok 344 - malformed rows leave the whole dependent alone
  ---
  duration_ms: 0.507329
  ...
# Subtest: R9 deletes label-only rows and removes the open field
ok 345 - R9 deletes label-only rows and removes the open field
  ---
  duration_ms: 0.627448
  ...
# Subtest: cross-note links use the shortest unambiguous form
ok 346 - cross-note links use the shortest unambiguous form
  ---
  duration_ms: 0.666843
  ...
# Subtest: ambiguous basenames fall back to the full path
ok 347 - ambiguous basenames fall back to the full path
  ---
  duration_ms: 0.537516
  ...
# Subtest: duplicate ids are ambiguous and fatal for --write
ok 348 - duplicate ids are ambiguous and fatal for --write
  ---
  duration_ms: 0.230079
  ...
# Subtest: archive targets keep the done/ path and are never stamped
ok 349 - archive targets keep the done/ path and are never stamped
  ---
  duration_ms: 0.276458
  ...
# Subtest: self links stay on the line but are not projected
ok 350 - self links stay on the line but are not projected
  ---
  duration_ms: 0.300984
  ...
# Subtest: non-task targets stay on the line but are not projected
ok 351 - non-task targets stay on the line but are not projected
  ---
  duration_ms: 0.252683
  ...
# Subtest: preserves CRLF, missing final newline, and cancel-log position
ok 352 - preserves CRLF, missing final newline, and cancel-log position
  ---
  duration_ms: 0.359367
  ...
# Subtest: migration is idempotent
ok 353 - migration is idempotent
  ---
  duration_ms: 1.008296
  ...
# Subtest: parseArgs handles --vault, --write, --help, and rejects unknowns
ok 354 - parseArgs handles --vault, --write, --help, and rejects unknowns
  ---
  duration_ms: 0.587342
  ...
# Subtest: BOB_CLI_DIR wins over a sibling checkout and a cache
ok 355 - BOB_CLI_DIR wins over a sibling checkout and a cache
  ---
  duration_ms: 19.204658
  ...
# Subtest: sibling bob-cli is used when BOB_CLI_DIR is unset
ok 356 - sibling bob-cli is used when BOB_CLI_DIR is unset
  ---
  duration_ms: 14.217385
  ...
# Subtest: an invalid BOB_CLI_DIR does not fall through
ok 357 - an invalid BOB_CLI_DIR does not fall through
  ---
  duration_ms: 9.669856
  ...
# Subtest: cache clone is used when no user-owned checkout exists
ok 358 - cache clone is used when no user-owned checkout exists
  ---
  duration_ms: 23.484204
  ...
# Subtest: refreshing an existing cache keeps git chatter off stdout and forwards exact paths
ok 359 - refreshing an existing cache keeps git chatter off stdout and forwards exact paths
  ---
  duration_ms: 36.267668
  ...
# Subtest: a cache clone with a foreign origin fails before fetch or reset
ok 360 - a cache clone with a foreign origin fails before fetch or reset
  ---
  duration_ms: 16.817287
  ...
# Subtest: a justfile alone is rejected as an explicit bob-cli checkout
ok 361 - a justfile alone is rejected as an explicit bob-cli checkout
  ---
  duration_ms: 10.736096
  ...
# Subtest: just failures propagate
ok 362 - just failures propagate
  ---
  duration_ms: 14.148764
  ...
# Subtest: scans multiline, one-line, and guarded literal registrations
ok 363 - scans multiline, one-line, and guarded literal registrations
  ---
  duration_ms: 2.984108
  ...
# Subtest: scans an optional addCommand call
ok 364 - scans an optional addCommand call
  ---
  duration_ms: 0.274264
  ...
# Subtest: allows addCommand references only in a typeof guard
ok 365 - allows addCommand references only in a typeof guard
  ---
  duration_ms: 0.355138
  ...
# Subtest: rejects bind, call, and aliased addCommand references with source locations
ok 366 - rejects bind, call, and aliased addCommand references with source locations
  ---
  duration_ms: 0.579847
  ...
# Subtest: expands literal command data from a constant-array forEach across source files
ok 367 - expands literal command data from a constant-array forEach across source files
  ---
  duration_ms: 1.86889
  ...
# Subtest: balances nested callback syntax and ignores misleading comments, strings, templates, and regexes
ok 368 - balances nested callback syntax and ignores misleading comments, strings, templates, and regexes
  ---
  duration_ms: 0.55007
  ...
# Subtest: decodes escaped string metadata and literal default hotkeys
ok 369 - decodes escaped string metadata and literal default hotkeys
  ---
  duration_ms: 0.371099
  ...
# Subtest: returns no commands for a plugin without registrations
ok 370 - returns no commands for a plugin without registrations
  ---
  duration_ms: 0.195874
  ...
# Subtest: fails with source locations for dynamic metadata, hotkeys, and malformed tables
ok 371 - fails with source locations for dynamic metadata, hotkeys, and malformed tables
  ---
  duration_ms: 0.963269
  ...
# Subtest: fails duplicate command ids with both registration locations
ok 372 - fails duplicate command ids with both registration locations
  ---
  duration_ms: 0.545091
  ...
# Subtest: checks drift without writes, preserves prose, and generates deterministically
ok 373 - checks drift without writes, preserves prose, and generates deterministically
  ---
  duration_ms: 9.564328
  ...
# Subtest: code-span table cells preserve backslashes and use a safe backtick fence
ok 374 - code-span table cells preserve backslashes and use a safe backtick fence
  ---
  duration_ms: 1.794277
  ...
# Subtest: does not write any output when source validation fails
ok 375 - does not write any output when source validation fails
  ---
  duration_ms: 1.196085
  ...
# Subtest: BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
ok 376 - BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
  ---
  duration_ms: 3.049253
  ...
# Subtest: reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
ok 377 - reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
  ---
  duration_ms: 3.022972
  ...
# Subtest: stale, missing, canonical append, and frozen-owner models (BC8-BC10)
ok 378 - stale, missing, canonical append, and frozen-owner models (BC8-BC10)
  ---
  duration_ms: 0.655311
  ...
# Subtest: Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
ok 379 - Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
  ---
  duration_ms: 7.907683
  ...
# Subtest: budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
ok 380 - budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
  ---
  duration_ms: 1.495717
  ...
# Subtest: chip builder includes the 🔑 badge and has no edit controls
ok 381 - chip builder includes the 🔑 badge and has no edit controls
  ---
  duration_ms: 0.532667
  ...
# Subtest: RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
ok 382 - RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
  ---
  duration_ms: 1.611879
  ...
# Subtest: RBC2 hover × on a live chip calls removeDependent; notice is nav's
ok 383 - RBC2 hover × on a live chip calls removeDependent; notice is nav's
  ---
  duration_ms: 0.638058
  ...
# Subtest: RBC3 frozen, stale, and no api.blocks stay navigation-only
ok 384 - RBC3 frozen, stale, and no api.blocks stay navigation-only
  ---
  duration_ms: 1.097547
  ...
# Subtest: RBC4 Reading view matches Live Preview ＋ / ×
ok 385 - RBC4 Reading view matches Live Preview ＋ / ×
  ---
  duration_ms: 2.954644
  ...
# Subtest: collections namespace version is additive v1
ok 386 - collections namespace version is additive v1
  ---
  duration_ms: 0.849622
  ...
# Subtest: collection chip classes stay collection-specific through paint and refresh
ok 387 - collection chip classes stay collection-specific through paint and refresh
  ---
  duration_ms: 2.567964
  ...
# Subtest: projects: scalar resolved links count, lists never widen
ok 388 - projects: scalar resolved links count, lists never widen
  ---
  duration_ms: 0.287448
  ...
# Subtest: projects: templates, status, and containsAny edges
ok 389 - projects: templates, status, and containsAny edges
  ---
  duration_ms: 0.303459
  ...
# Subtest: references: exact prefix, md only, exact scalar status
ok 390 - references: exact prefix, md only, exact scalar status
  ---
  duration_ms: 0.243555
  ...
# Subtest: base contracts: accept current files, reject drift, tolerate presentation
ok 391 - base contracts: accept current files, reject drift, tolerate presentation
  ---
  duration_ms: 0.574347
  ...
# Subtest: entries: true zero vs unavailable with reason, failure isolation
ok 392 - entries: true zero vs unavailable with reason, failure isolation
  ---
  duration_ms: 0.222004
  ...
# Subtest: snapshot counts both collections once, true zero stays clickable
ok 393 - snapshot counts both collections once, true zero stays clickable
  ---
  duration_ms: 0.33549
  ...
# Subtest: snapshot never presents partial counts as final
ok 394 - snapshot never presents partial counts as final
  ---
  duration_ms: 0.350569
  ...
# Subtest: changed definitions fail closed per collection, never stale
ok 395 - changed definitions fail closed per collection, never stale
  ---
  duration_ms: 0.430201
  ...
# Subtest: renderChip links, labels, and cleans up per component
ok 396 - renderChip links, labels, and cleans up per component
  ---
  duration_ms: 0.579447
  ...
# Subtest: PENDING section excludes TODAY while the whole lane keeps it
ok 397 - PENDING section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 2.408248
  ...
# Subtest: NEXT section excludes TODAY while the whole lane keeps it
ok 398 - NEXT section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 0.378052
  ...
# Subtest: NEXT uses symbol *, not name matching
ok 399 - NEXT uses symbol *, not name matching
  ---
  duration_ms: 0.26217
  ...
# Subtest: READY badge and query agree on hide and path case variants
ok 400 - READY badge and query agree on hide and path case variants
  ---
  duration_ms: 0.57593
  ...
# Subtest: blocked uses the full list even outside the visible subset
ok 401 - blocked uses the full list even outside the visible subset
  ---
  duration_ms: 0.20374
  ...
# Subtest: duplicate block IDs, missing IDs, and reused objects stay per-row
ok 402 - duplicate block IDs, missing IDs, and reused objects stay per-row
  ---
  duration_ms: 0.239046
  ...
# Subtest: READY gating keeps exempt rows and drops NEW/ROTTEN
ok 403 - READY gating keeps exempt rows and drops NEW/ROTTEN
  ---
  duration_ms: 0.284734
  ...
# Subtest: throwing Today degrades to unavailable, never zero
ok 404 - throwing Today degrades to unavailable, never zero
  ---
  duration_ms: 6.553386
  ...
# Subtest: dashboard badges color the displayed section count and label whole-lane pressure
ok 405 - dashboard badges color the displayed section count and label whole-lane pressure
  ---
  duration_ms: 0.643589
  ...
# Subtest: dashboard section warning boundaries ignore TODAY-only whole-lane excess
ok 406 - dashboard section warning boundaries ignore TODAY-only whole-lane excess
  ---
  duration_ms: 0.758819
  ...
# Subtest: dashboard lane badge keeps unavailable data neutral
ok 407 - dashboard lane badge keeps unavailable data neutral
  ---
  duration_ms: 0.313919
  ...
# Subtest: dashboard lane paint and refresh keep color aligned with the visible section
ok 408 - dashboard lane paint and refresh keep color aligned with the visible section
  ---
  duration_ms: 2.582172
  ...
# Subtest: dashboard lane widgets refresh together and prune on unload
ok 409 - dashboard lane widgets refresh together and prune on unload
  ---
  duration_ms: 1.907263
  ...
# Subtest: daily paint matches dashboard section badges on screenshot fixtures
ok 410 - daily paint matches dashboard section badges on screenshot fixtures
  ---
  duration_ms: 19.572903
  ...
# Subtest: daily and dashboard membership agree for exclusions and custom IN_PROGRESS
ok 411 - daily and dashboard membership agree for exclusions and custom IN_PROGRESS
  ---
  duration_ms: 4.604994
  ...
# Subtest: daily paint refreshes with dashboard when Today, lane, and cap change
ok 412 - daily paint refreshes with dashboard when Today, lane, and cap change
  ---
  duration_ms: 7.719354
  ...
# Subtest: older daily notes follow today's dashboard lanes
ok 413 - older daily notes follow today's dashboard lanes
  ---
  duration_ms: 3.094561
  ...
# Subtest: daily lane anchors keep shared navigation and reject stale paints
ok 414 - daily lane anchors keep shared navigation and reject stale paints
  ---
  duration_ms: 2.584767
  ...
# Subtest: daily paint stays unavailable until Tasks and Today are ready
ok 415 - daily paint stays unavailable until Tasks and Today are ready
  ---
  duration_ms: 1.294863
  ...
# Subtest: work tones: dashboard lane models carry section tones
ok 416 - work tones: dashboard lane models carry section tones
  ---
  duration_ms: 0.17258
  ...
# Subtest: T1 scheduled full-mode row gets a Fri mark inside the span
ok 417 - T1 scheduled full-mode row gets a Fri mark inside the span
  ---
  duration_ms: 2.756825
  ...
# Subtest: T2 done row maps to a completion Oct 5 mark
ok 418 - T2 done row maps to a completion Oct 5 mark
  ---
  duration_ms: 0.468384
  ...
# Subtest: T3 short-mode created span is left untouched by JS
ok 419 - T3 short-mode created span is left untouched by JS
  ---
  duration_ms: 0.326153
  ...
# Subtest: T4 pending row decorates once data-task appears; exhausted rows stay native
ok 420 - T4 pending row decorates once data-task appears; exhausted rows stay native
  ---
  duration_ms: 0.97894
  ...
# Subtest: T5 a second pass adds nothing
ok 421 - T5 a second pass adds nothing
  ---
  duration_ms: 0.26685
  ...
# Subtest: T6 task-due and task-start spans are untouched
ok 422 - T6 task-due and task-start spans are untouched
  ---
  duration_ms: 0.242143
  ...
# Subtest: T7 an invalid date is untouched
ok 423 - T7 an invalid date is untouched
  ---
  duration_ms: 0.256861
  ...
# Subtest: T8 nothing is scheduled with marks off or for connected non-Tasks elements
ok 424 - T8 nothing is scheduled with marks off or for connected non-Tasks elements
  ---
  duration_ms: 0.255317
  ...
# Subtest: T9 a Tasks-host Fri mark relabels to tomorrow on rollover
ok 425 - T9 a Tasks-host Fri mark relabels to tomorrow on rollover
  ---
  duration_ms: 0.702281
  ...
# Subtest: renderDateMarksIn schedules one shared frame for every row
ok 426 - renderDateMarksIn schedules one shared frame for every row
  ---
  duration_ms: 0.976956
  ...
# Subtest: the Tasks pass never throws on hostile input
ok 427 - the Tasks pass never throws on hostile input
  ---
  duration_ms: 0.394103
  ...
# Subtest: T10 real-DOM NodeList children decorate via direct and queued passes
ok 428 - T10 real-DOM NodeList children decorate via direct and queued passes
  ---
  duration_ms: 0.568466
  ...
# Subtest: T11 toggling off before a queued frame runs writes nothing
ok 429 - T11 toggling off before a queued frame runs writes nothing
  ---
  duration_ms: 0.441052
  ...
# Subtest: T12 a pending-row retry followed by disabling writes nothing
ok 430 - T12 a pending-row retry followed by disabling writes nothing
  ---
  duration_ms: 0.320402
  ...
# Subtest: T13 unloading before a callback runs writes nothing
ok 431 - T13 unloading before a callback runs writes nothing
  ---
  duration_ms: 0.914607
  ...
# Subtest: styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
ok 432 - styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
  ---
  duration_ms: 1.059734
  ...
# Subtest: DATE_MARK_FIELDS lists the four dates with verbs
ok 433 - DATE_MARK_FIELDS lists the four dates with verbs
  ---
  duration_ms: 1.547285
  ...
# Subtest: DM1 created today: label, tooltip, fold, quiet field
ok 434 - DM1 created today: label, tooltip, fold, quiet field
  ---
  duration_ms: 1.323428
  ...
# Subtest: DM2 created yesterday without space after the colons
ok 435 - DM2 created yesterday without space after the colons
  ---
  duration_ms: 0.374224
  ...
# Subtest: DM3-DM6 scheduled tomorrow, weekday, and month/day labels
ok 436 - DM3-DM6 scheduled tomorrow, weekday, and month/day labels
  ---
  duration_ms: 0.220982
  ...
# Subtest: DM7 scheduled today reads with emphasis timing
ok 437 - DM7 scheduled today reads with emphasis timing
  ---
  duration_ms: 0.211173
  ...
# Subtest: DM8 past scheduled uses month/day, never a weekday
ok 438 - DM8 past scheduled uses month/day, never a weekday
  ---
  duration_ms: 0.150057
  ...
# Subtest: DM9 completion on a closed task keeps the timeline grammar
ok 439 - DM9 completion on a closed task keeps the timeline grammar
  ---
  duration_ms: 0.185294
  ...
# Subtest: DM10 cancelled across years appends the year
ok 440 - DM10 cancelled across years appends the year
  ---
  duration_ms: 0.130869
  ...
# Subtest: DM11 next-year date appends the year
ok 441 - DM11 next-year date appends the year
  ---
  duration_ms: 0.302137
  ...
# Subtest: DM12 the weekday rule wins across the year boundary
ok 442 - DM12 the weekday rule wins across the year boundary
  ---
  duration_ms: 0.377291
  ...
# Subtest: DM13 two marks in order with folds 1 and 2
ok 443 - DM13 two marks in order with folds 1 and 2
  ---
  duration_ms: 0.41855
  ...
# Subtest: DM14 created and scheduled ranges stay disjoint from the fresh mark
ok 444 - DM14 created and scheduled ranges stay disjoint from the fresh mark
  ---
  duration_ms: 0.301706
  ...
# Subtest: DM15-DM16 paren and padded brackets are canonical
ok 445 - DM15-DM16 paren and padded brackets are canonical
  ---
  duration_ms: 0.164334
  ...
# Subtest: DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
ok 446 - DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
  ---
  duration_ms: 0.310002
  ...
# Subtest: DM22 code still parses pure but decorates nothing (see Live Preview)
ok 447 - DM22 code still parses pure but decorates nothing (see Live Preview)
  ---
  duration_ms: 0.109339
  ...
# Subtest: DM23 rescheduled is untouched and never a duplicate
ok 448 - DM23 rescheduled is untouched and never a duplicate
  ---
  duration_ms: 0.148974
  ...
# Subtest: DN1-DN9 non-canonical fields get no mark
ok 449 - DN1-DN9 non-canonical fields get no mark
  ---
  duration_ms: 0.229568
  ...
# Subtest: dateMarkContentStart finds content on list, quoted, and plain lines
ok 450 - dateMarkContentStart finds content on list, quoted, and plain lines
  ---
  duration_ms: 0.10478
  ...
# Subtest: dateMarkRelativePhrase covers the exact-day phrases
ok 451 - dateMarkRelativePhrase covers the exact-day phrases
  ---
  duration_ms: 0.085664
  ...
# Subtest: dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
ok 452 - dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
  ---
  duration_ms: 0.309311
  ...
# Subtest: no model output contains a double colon
ok 453 - no model output contains a double colon
  ---
  duration_ms: 1.377962
  ...
# Subtest: a new day always changes the widget key
ok 454 - a new day always changes the widget key
  ---
  duration_ms: 0.150457
  ...
# Subtest: element structure and the decorative/inheritColor/rendered options
ok 455 - element structure and the decorative/inheritColor/rendered options
  ---
  duration_ms: 0.436203
  ...
# Subtest: Live Preview emits several decorations in ascending order
ok 456 - Live Preview emits several decorations in ascending order
  ---
  duration_ms: 1.499514
  ...
# Subtest: Live Preview reveals per field, never the whole line
ok 457 - Live Preview reveals per field, never the whole line
  ---
  duration_ms: 0.267391
  ...
# Subtest: Live Preview refuses source mode, code, and disabled marks
ok 458 - Live Preview refuses source mode, code, and disabled marks
  ---
  duration_ms: 0.449819
  ...
# Subtest: widget mousedown anchors at the field start for folds 0, 1, and 2
ok 459 - widget mousedown anchors at the field start for folds 0, 1, and 2
  ---
  duration_ms: 0.920568
  ...
# Subtest: DM24 a cursor in the folded run unfolds the mark (vim cw)
ok 460 - DM24 a cursor in the folded run unfolds the mark (vim cw)
  ---
  duration_ms: 0.241501
  ...
# Subtest: DM25 a cursor in Tasks double space unfolds only that field
ok 461 - DM25 a cursor in Tasks double space unfolds only that field
  ---
  duration_ms: 0.177058
  ...
# Subtest: a selection ending inside the run unfolds; ending at its start keeps the fold
ok 462 - a selection ending inside the run unfolds; ending at its start keeps the fold
  ---
  duration_ms: 0.18333
  ...
# Subtest: no emitted decoration ever hides a cursor, and reveal still means field overlap
ok 463 - no emitted decoration ever hides a cursor, and reveal still means field overlap
  ---
  duration_ms: 11.929376
  ...
# Subtest: dateMarkSelectionFold: reveal, unfold, fold, and garbage input
ok 464 - dateMarkSelectionFold: reveal, unfold, fold, and garbage input
  ---
  duration_ms: 0.19932
  ...
# Subtest: mousedown on an unfolded (fold-0) widget anchors at the field start
ok 465 - mousedown on an unfolded (fold-0) widget anchors at the field start
  ---
  duration_ms: 0.306936
  ...
# Subtest: rendered views split several fields in one node
ok 466 - rendered views split several fields in one node
  ---
  duration_ms: 1.427306
  ...
# Subtest: rendered views skip exclusions and duplicates
ok 467 - rendered views skip exclusions and duplicates
  ---
  duration_ms: 0.495867
  ...
# Subtest: RO1 rendered marks relabel in place across midnight
ok 468 - RO1 rendered marks relabel in place across midnight
  ---
  duration_ms: 0.470358
  ...
# Subtest: rollover dispatches once per day change and never touches widgets
ok 469 - rollover dispatches once per day change and never touches widgets
  ---
  duration_ms: 0.359105
  ...
# Subtest: api.dateMarks v1 is additive, sync, and never throwing
ok 470 - api.dateMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.432085
  ...
# Subtest: session toggle and onload wiring
ok 471 - session toggle and onload wiring
  ---
  duration_ms: 3.75501
  ...
# Subtest: styles.css contract: masks, tones, repair flag, resting
ok 472 - styles.css contract: masks, tones, repair flag, resting
  ---
  duration_ms: 0.803754
  ...
# Subtest: DP parse vectors
ok 473 - DP parse vectors
  ---
  duration_ms: 2.217425
  ...
# Subtest: DC chip model vectors
ok 474 - DC chip model vectors
  ---
  duration_ms: 1.653247
  ...
# Subtest: decoration builds one widget, reveals on cursor, skips code and ranges
ok 475 - decoration builds one widget, reveals on cursor, skips code and ranges
  ---
  duration_ms: 7.845555
  ...
# Subtest: decoration skips paragraphs, grandchildren, and Work Log lines
ok 476 - decoration skips paragraphs, grandchildren, and Work Log lines
  ---
  duration_ms: 0.746466
  ...
# Subtest: decoration renders chips on DP30 and still skips DP20
ok 477 - decoration renders chips on DP30 and still skips DP20
  ---
  duration_ms: 0.855314
  ...
# Subtest: ownership check reads O(depth) lines, not the whole note
ok 478 - ownership check reads O(depth) lines, not the whole note
  ---
  duration_ms: 1.606278
  ...
# Subtest: widget identity covers the line and the interactive flag
ok 479 - widget identity covers the line and the interactive flag
  ---
  duration_ms: 2.388552
  ...
# Subtest: element hides actions without nav api v1
ok 480 - element hides actions without nav api v1
  ---
  duration_ms: 0.758719
  ...
# Subtest: nav api feature detection gates actions
ok 481 - nav api feature detection gates actions
  ---
  duration_ms: 0.407208
  ...
# Subtest: reading view decorates only the Depends-On row, hides chrome, stays idempotent
ok 482 - reading view decorates only the Depends-On row, hides chrome, stays idempotent
  ---
  duration_ms: 3.316795
  ...
# Subtest: reading view collapses more than three Done targets to one chip
ok 483 - reading view collapses more than three Done targets to one chip
  ---
  duration_ms: 1.344728
  ...
# Subtest: DC chip model vectors by id: DC2, DC5, DC6, DC9
ok 484 - DC chip model vectors by id: DC2, DC5, DC6, DC9
  ---
  duration_ms: 0.292168
  ...
# Subtest: chip actions send the 0-based line index through nav api v1
ok 485 - chip actions send the 0-based line index through nav api v1
  ---
  duration_ms: 1.276638
  ...
# Subtest: chip hover passes the chip element and its row to the preview
ok 486 - chip hover passes the chip element and its row to the preview
  ---
  duration_ms: 0.184652
  ...
# Subtest: chip lookup index lives on the freshness memo
ok 487 - chip lookup index lives on the freshness memo
  ---
  duration_ms: 0.540041
  ...
# Subtest: reading view hides actions when the line cannot be derived
ok 488 - reading view hides actions when the line cannot be derived
  ---
  duration_ms: 11.319608
  ...
# Subtest: reading view actions carry the derived 0-based line
ok 489 - reading view actions carry the derived 0-based line
  ---
  duration_ms: 2.447775
  ...
# Subtest: reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
ok 490 - reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
  ---
  duration_ms: 0.521987
  ...
# Subtest: reading view renders chips on DP30 (owner is a task under a Work Log entry)
ok 491 - reading view renders chips on DP30 (owner is a task under a Work Log entry)
  ---
  duration_ms: 0.558066
  ...
# Subtest: reading view DP30 row actions send the owned Depends-On line
ok 492 - reading view DP30 row actions send the owned Depends-On line
  ---
  duration_ms: 2.034697
  ...
# Subtest: reading view second-row remove sends the second line when two tasks share a prerequisite
ok 493 - reading view second-row remove sends the second line when two tasks share a prerequisite
  ---
  duration_ms: 1.53962
  ...
# Subtest: chip lookup index builds once per freshness memo
ok 494 - chip lookup index builds once per freshness memo
  ---
  duration_ms: 0.37714
  ...
# Subtest: decoration evaluates ownership without copying the note
ok 495 - decoration evaluates ownership without copying the note
  ---
  duration_ms: 0.469637
  ...
# Subtest: toggle flips the body class and onload wires chips
ok 496 - toggle flips the body class and onload wires chips
  ---
  duration_ms: 3.898937
  ...
# Subtest: capability: nav card v2 is capable
ok 497 - capability: nav card v2 is capable
  ---
  duration_ms: 0.905469
  ...
# Subtest: capability: nav card v1 is not capable
ok 498 - capability: nav card v1 is not capable
  ---
  duration_ms: 0.179994
  ...
# Subtest: capability: absent nav, missing api, and old versions are not capable
ok 499 - capability: absent nav, missing api, and old versions are not capable
  ---
  duration_ms: 0.134777
  ...
# Subtest: capability: a throwing app never throws
ok 500 - capability: a throwing app never throws
  ---
  duration_ms: 0.186837
  ...
# Subtest: leaf: active capable due choice replaces refresh with a leaf
ok 501 - leaf: active capable due choice replaces refresh with a leaf
  ---
  duration_ms: 2.642638
  ...
# Subtest: leaf: the same row without the card keeps refresh and counting words
ok 502 - leaf: the same row without the card keeps refresh and counting words
  ---
  duration_ms: 0.411977
  ...
# Subtest: leaf: early dates still leaf when capable
ok 503 - leaf: early dates still leaf when capable
  ---
  duration_ms: 0.420673
  ...
# Subtest: leaf: decay-off rows never leaf even when capable
ok 504 - leaf: decay-off rows never leaf even when capable
  ---
  duration_ms: 0.387951
  ...
# Subtest: leaf: below-threshold rows never leaf
ok 505 - leaf: below-threshold rows never leaf
  ---
  duration_ms: 0.544089
  ...
# Subtest: leaf: threshold zero asks on every due re-confirmation when capable
ok 506 - leaf: threshold zero asks on every due re-confirmation when capable
  ---
  duration_ms: 0.48662
  ...
# Subtest: leaf: overflow renders capped dots with +N and the exact count in text
ok 507 - leaf: overflow renders capped dots with +N and the exact count in text
  ---
  duration_ms: 0.284403
  ...
# Subtest: leaf: out-of-scope and closed tasks show dots quietly, never a leaf
ok 508 - leaf: out-of-scope and closed tasks show dots quietly, never a leaf
  ---
  duration_ms: 0.668957
  ...
# Subtest: leaf: unresolved marks show dots quietly with counting-only wording
ok 509 - leaf: unresolved marks show dots quietly with counting-only wording
  ---
  duration_ms: 0.200072
  ...
# Subtest: element: leaf marks carry data-decide true and a leaf path
ok 510 - element: leaf marks carry data-decide true and a leaf path
  ---
  duration_ms: 0.655642
  ...
# Subtest: element: non-decision marks carry data-decide false
ok 511 - element: non-decision marks carry data-decide false
  ---
  duration_ms: 0.228145
  ...
# Subtest: footer groups omit every zero tier and keep walk order
ok 512 - footer groups omit every zero tier and keep walk order
  ---
  duration_ms: 1.634422
  ...
# Subtest: PRE and POST groups bracket the nine-tier queue and expose completion hints
ok 513 - PRE and POST groups bracket the nine-tier queue and expose completion hints
  ---
  duration_ms: 0.789868
  ...
# Subtest: a NEW-state project appears only in its walk tier
ok 514 - a NEW-state project appears only in its walk tier
  ---
  duration_ms: 0.207627
  ...
# Subtest: empty queue hides the footer even with upkeep or a met budget
ok 515 - empty queue hides the footer even with upkeep or a met budget
  ---
  duration_ms: 0.158933
  ...
# Subtest: unavailable or missing data never render false counts
ok 516 - unavailable or missing data never render false counts
  ---
  duration_ms: 0.135659
  ...
# Subtest: generic summary names due, commitments, and nonempty groups
ok 517 - generic summary names due, commitments, and nonempty groups
  ---
  duration_ms: 0.300253
  ...
# Subtest: current-task context uses shared ranks and compact wording
ok 518 - current-task context uses shared ranks and compact wording
  ---
  duration_ms: 0.636336
  ...
# Subtest: only ROTTEN remaining names commitments done or a met budget
ok 519 - only ROTTEN remaining names commitments done or a met budget
  ---
  duration_ms: 0.262883
  ...
# Subtest: NEW and commitments take precedence over a met budget
ok 520 - NEW and commitments take precedence over a met budget
  ---
  duration_ms: 0.358385
  ...
# Subtest: reviewEntryView compact and detail cover the original freshness tiers
ok 521 - reviewEntryView compact and detail cover the original freshness tiers
  ---
  duration_ms: 0.768477
  ...
# Subtest: cursor matching requires a unique verified identity
ok 522 - cursor matching requires a unique verified identity
  ---
  duration_ms: 0.367011
  ...
# Subtest: footer paint hides the host and keeps a stable button
ok 523 - footer paint hides the host and keeps a stable button
  ---
  duration_ms: 1.01595
  ...
# Subtest: status bar 0-1-0 transitions hide without a reload
ok 524 - status bar 0-1-0 transitions hide without a reload
  ---
  duration_ms: 8.233125
  ...
# Subtest: cursor-only updates reuse a warm memo
ok 525 - cursor-only updates reuse a warm memo
  ---
  duration_ms: 1.275576
  ...
# Subtest: unload disconnects the observer and click handler
ok 526 - unload disconnects the observer and click handler
  ---
  duration_ms: 1.316835
  ...
# Subtest: queue-built ranks agree with the footer current entry
ok 527 - queue-built ranks agree with the footer current entry
  ---
  duration_ms: 0.912864
  ...
# Subtest: footer short labels map every tier
ok 528 - footer short labels map every tier
  ---
  duration_ms: 0.117475
  ...
# Subtest: current-row footer context uses short labels while entry views keep full labels
ok 529 - current-row footer context uses short labels while entry views keep full labels
  ---
  duration_ms: 0.234187
  ...
# Subtest: legend line lists only current abbreviated tiers
ok 530 - legend line lists only current abbreviated tiers
  ---
  duration_ms: 0.264075
  ...
# Subtest: K1 absent: no keeps means 0 with no lints
ok 531 - K1 absent: no keeps means 0 with no lints
  ---
  duration_ms: 2.59727
  ...
# Subtest: K8 misplaced: keeps inside the Tasks suffix reads with a lint
ok 532 - K8 misplaced: keeps inside the Tasks suffix reads with a lint
  ---
  duration_ms: 0.50237
  ...
# Subtest: K9 duplicates and invalid values: first valid wins, else 0
ok 533 - K9 duplicates and invalid values: first valid wins, else 0
  ---
  duration_ms: 0.608032
  ...
# Subtest: K10 ceiling and NEW: 999 reads, never-confirmed reads 0
ok 534 - K10 ceiling and NEW: 999 reads, never-confirmed reads 0
  ---
  duration_ms: 0.200664
  ...
# Subtest: K13 exact keys: near-miss keys are not keeps; parens read
ok 535 - K13 exact keys: near-miss keys are not keeps; parens read
  ---
  duration_ms: 0.189282
  ...
# Subtest: keeps value parser accepts only decimal 1-999
ok 536 - keeps value parser accepts only decimal 1-999
  ---
  duration_ms: 0.184092
  ...
# Subtest: K2 first valid canonical: uncounted keep preserves and repairs
ok 537 - K2 first valid canonical: uncounted keep preserves and repairs
  ---
  duration_ms: 0.814215
  ...
# Subtest: K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
ok 538 - K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
  ---
  duration_ms: 0.64392
  ...
# Subtest: K4 same-day preserve noop: canonical kept line is byte-identical
ok 539 - K4 same-day preserve noop: canonical kept line is byte-identical
  ---
  duration_ms: 0.487901
  ...
# Subtest: K5 generic stamp clears, even same-day
ok 540 - K5 generic stamp clears, even same-day
  ---
  duration_ms: 0.469227
  ...
# Subtest: K6 set-refresh clears keeps
ok 541 - K6 set-refresh clears keeps
  ---
  duration_ms: 0.27222
  ...
# Subtest: K7 stale stamp clears keeps
ok 542 - K7 stale stamp clears keeps
  ---
  duration_ms: 0.164524
  ...
# Subtest: K8b misplaced keeps repaired to canonical order by a keep
ok 543 - K8b misplaced keeps repaired to canonical order by a keep
  ---
  duration_ms: 0.189412
  ...
# Subtest: K11 refusals preserve: closed and recurring lines never write
ok 544 - K11 refusals preserve: closed and recurring lines never write
  ---
  duration_ms: 0.219991
  ...
# Subtest: counted keep increments a stale streak once in the same write
ok 545 - counted keep increments a stale streak once in the same write
  ---
  duration_ms: 0.192568
  ...
# Subtest: first counted keep on a streakless due task writes keeps 1
ok 546 - first counted keep on a streakless due task writes keeps 1
  ---
  duration_ms: 0.201665
  ...
# Subtest: counted keep saturates at 999 and never wraps
ok 547 - counted keep saturates at 999 and never wraps
  ---
  duration_ms: 0.244617
  ...
# Subtest: counted keep needs a valid prior fresh before today
ok 548 - counted keep needs a valid prior fresh before today
  ---
  duration_ms: 0.332325
  ...
# Subtest: counted keep repairs malformed and duplicate placement
ok 549 - counted keep repairs malformed and duplicate placement
  ---
  duration_ms: 0.32985
  ...
# Subtest: uncounted keep preserves the valid value while canonicalizing
ok 550 - uncounted keep preserves the valid value while canonicalizing
  ---
  duration_ms: 0.217916
  ...
# Subtest: UB13 keep on an unblock TICKLER preserves the streak and skips the card
ok 551 - UB13 keep on an unblock TICKLER preserves the streak and skips the card
  ---
  duration_ms: 0.875984
  ...
# Subtest: a scheduled tickler still counts when schedule wins an unblock tie
ok 552 - a scheduled tickler still counts when schedule wins an unblock tie
  ---
  duration_ms: 0.334118
  ...
# Subtest: decay normalization: absent, null, true, and {} enable with 3
ok 553 - decay normalization: absent, null, true, and {} enable with 3
  ---
  duration_ms: 0.657395
  ...
# Subtest: decay false counts and displays but never asks
ok 554 - decay false counts and displays but never asks
  ---
  duration_ms: 0.114769
  ...
# Subtest: decay keeps 0 and fixed entry normalize
ok 555 - decay keeps 0 and fixed entry normalize
  ---
  duration_ms: 0.137462
  ...
# Subtest: invalid decay shapes fail the freshness config contract
ok 556 - invalid decay shapes fail the freshness config contract
  ---
  duration_ms: 0.231493
  ...
# Subtest: B: at-limit Ready due rows decide on every local day
ok 557 - B: at-limit Ready due rows decide on every local day
  ---
  duration_ms: 0.468495
  ...
# Subtest: D1 early date: an at-limit Ready due row decides
ok 558 - D1 early date: an at-limit Ready due row decides
  ---
  duration_ms: 0.110942
  ...
# Subtest: D2 at limit decides; D3 below limit stamps without a card
ok 559 - D2 at limit decides; D3 below limit stamps without a card
  ---
  duration_ms: 0.122484
  ...
# Subtest: D4 tickler counts as due; D5 NEW never decides
ok 560 - D4 tickler counts as due; D5 NEW never decides
  ---
  duration_ms: 0.214139
  ...
# Subtest: D6 zero limit asks on every due Ready re-confirmation
ok 561 - D6 zero limit asks on every due Ready re-confirmation
  ---
  duration_ms: 0.130249
  ...
# Subtest: D7 off never asks; D8 lane rows never decide
ok 562 - D7 off never asks; D8 lane rows never decide
  ---
  duration_ms: 0.100652
  ...
# Subtest: evaluator, queue, and counts carry keeps and decide
ok 563 - evaluator, queue, and counts carry keeps and decide
  ---
  duration_ms: 1.148804
  ...
# Subtest: no keeps: the existing mark is unchanged
ok 564 - no keeps: the existing mark is unchanged
  ---
  duration_ms: 0.941568
  ...
# Subtest: aging with two keeps: faint pips plus a counting-only line
ok 565 - aging with two keeps: faint pips plus a counting-only line
  ---
  duration_ms: 0.279214
  ...
# Subtest: confirmed today with two keeps: check glyph, faint dots
ok 566 - confirmed today with two keeps: check glyph, faint dots
  ---
  duration_ms: 0.213097
  ...
# Subtest: due below threshold: orange capsule keeps its glyph, adds dots
ok 567 - due below threshold: orange capsule keeps its glyph, adds dots
  ---
  duration_ms: 0.229298
  ...
# Subtest: resting marks show historical dots quietly and never decide
ok 568 - resting marks show historical dots quietly and never decide
  ---
  duration_ms: 0.331683
  ...
# Subtest: active decision due: data stays truthful, leaf stays gated
ok 569 - active decision due: data stays truthful, leaf stays gated
  ---
  duration_ms: 0.243005
  ...
# Subtest: dot caps follow the threshold with +N overflow
ok 570 - dot caps follow the threshold with +N overflow
  ---
  duration_ms: 2.0006
  ...
# Subtest: keeps tooltip wording: singulars, zero threshold, off state
ok 571 - keeps tooltip wording: singulars, zero threshold, off state
  ---
  duration_ms: 0.121772
  ...
# Subtest: noncanonical keeps never fold but keep their repair pill
ok 572 - noncanonical keeps never fold but keep their repair pill
  ---
  duration_ms: 0.357432
  ...
# Subtest: quoted lines fold; rendered fragments fold without task checks
ok 573 - quoted lines fold; rendered fragments fold without task checks
  ---
  duration_ms: 0.24066
  ...
# Subtest: unresolved marks show the line's own pips quietly and never decide
ok 574 - unresolved marks show the line's own pips quietly and never decide
  ---
  duration_ms: 0.215171
  ...
# Subtest: consensus sees count and decision eligibility: ambiguity stays neutral
ok 575 - consensus sees count and decision eligibility: ambiguity stays neutral
  ---
  duration_ms: 0.531285
  ...
# Subtest: pips render as one aria-hidden span with the count in the label
ok 576 - pips render as one aria-hidden span with the count in the label
  ---
  duration_ms: 1.039324
  ...
# Subtest: Live Preview decorates the folded range including space and refresh
ok 577 - Live Preview decorates the folded range including space and refresh
  ---
  duration_ms: 5.046309
  ...
# Subtest: Live Preview reveals the raw field when the cursor overlaps either edge
ok 578 - Live Preview reveals the raw field when the cursor overlaps either edge
  ---
  duration_ms: 1.131441
  ...
# Subtest: Live Preview skips codeblock and inline code spans
ok 579 - Live Preview skips codeblock and inline code spans
  ---
  duration_ms: 0.693715
  ...
# Subtest: source mode and marks-off yield no decorations
ok 580 - source mode and marks-off yield no decorations
  ---
  duration_ms: 0.199922
  ...
# Subtest: update rebuilds on the refresh effect and widget eq is stable
ok 581 - update rebuilds on the refresh effect and widget eq is stable
  ---
  duration_ms: 0.965694
  ...
# Subtest: widget click reveals the field at the folded offset
ok 582 - widget click reveals the field at the folded offset
  ---
  duration_ms: 0.701059
  ...
# Subtest: line resolver prefers exact, then consensus, then unresolved
ok 583 - line resolver prefers exact, then consensus, then unresolved
  ---
  duration_ms: 1.224649
  ...
# Subtest: decoration builds reuse the snapshot without touching the loader
ok 584 - decoration builds reuse the snapshot without touching the loader
  ---
  duration_ms: 0.401296
  ...
# Subtest: rendered views split text nodes and skip excluded ancestors
ok 585 - rendered views split text nodes and skip excluded ancestors
  ---
  duration_ms: 1.447525
  ...
# Subtest: rendered views stay idempotent
ok 586 - rendered views stay idempotent
  ---
  duration_ms: 0.549249
  ...
# Subtest: text resolver reaches consensus and degrades to neutral
ok 587 - text resolver reaches consensus and degrades to neutral
  ---
  duration_ms: 0.576902
  ...
# Subtest: session toggle flips the body class and notifies
ok 588 - session toggle flips the body class and notifies
  ---
  duration_ms: 0.779319
  ...
# Subtest: onload registers the toggle, extension, and post-processor
ok 589 - onload registers the toggle, extension, and post-processor
  ---
  duration_ms: 3.98521
  ...
# Subtest: M1 today: check glyph, today label, full ring
ok 590 - M1 today: check glyph, today label, full ring
  ---
  duration_ms: 8.446011
  ...
# Subtest: M2 aging: ring glyph, 3d label, draining lease
ok 591 - M2 aging: ring glyph, 3d label, draining lease
  ---
  duration_ms: 4.778385
  ...
# Subtest: M3 boundary: ROTTEN due capsule with Alt+F hint
ok 592 - M3 boundary: ROTTEN due capsule with Alt+F hint
  ---
  duration_ms: 0.475669
  ...
# Subtest: checklist marks replace stamp hints with their completion tier
ok 593 - checklist marks replace stamp hints with their completion tier
  ---
  duration_ms: 0.866796
  ...
# Subtest: M4 yesterday uses the yesterday relative
ok 594 - M4 yesterday uses the yesterday relative
  ---
  duration_ms: 0.309822
  ...
# Subtest: M5 folded refresh shows the /14d suffix
ok 595 - M5 folded refresh shows the /14d suffix
  ---
  duration_ms: 0.568706
  ...
# Subtest: M6 refresh today: today tone hides the interval suffix
ok 596 - M6 refresh today: today tone hides the interval suffix
  ---
  duration_ms: 0.365668
  ...
# Subtest: M7 note interval stays tooltip-only
ok 597 - M7 note interval stays tooltip-only
  ---
  duration_ms: 0.611508
  ...
# Subtest: M8 resurfaced: due tone on the scheduled return
ok 598 - M8 resurfaced: due tone on the scheduled return
  ---
  duration_ms: 0.584626
  ...
# Subtest: M9 due NEXT lane with keep/release/today keys
ok 599 - M9 due NEXT lane with keep/release/today keys
  ---
  duration_ms: 0.606749
  ...
# Subtest: M10 NEXT lane stamped today
ok 600 - M10 NEXT lane stamped today
  ---
  duration_ms: 0.30901
  ...
# Subtest: M19 disabled Next lane rests
ok 601 - M19 disabled Next lane rests
  ---
  duration_ms: 0.302398
  ...
# Subtest: M20 PENDING lane folds refresh without the suffix
ok 602 - M20 PENDING lane folds refresh without the suffix
  ---
  duration_ms: 0.264555
  ...
# Subtest: M11 closed: resting beats age 0
ok 603 - M11 closed: resting beats age 0
  ---
  duration_ms: 0.208849
  ...
# Subtest: M12 unresolved running and M13 unresolved lease over
ok 604 - M12 unresolved running and M13 unresolved lease over
  ---
  duration_ms: 0.221984
  ...
# Subtest: M14 linked today rests with its reason
ok 605 - M14 linked today rests with its reason
  ---
  duration_ms: 0.182138
  ...
# Subtest: M15 other year shows the year and the 282d age
ok 606 - M15 other year shows the year and the 282d age
  ---
  duration_ms: 0.147051
  ...
# Subtest: M16 quoted line keeps foldSpace
ok 607 - M16 quoted line keeps foldSpace
  ---
  duration_ms: 0.15696
  ...
# Subtest: M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
ok 608 - M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
  ---
  duration_ms: 0.357884
  ...
# Subtest: N1-N6 non-canonical lines get no mark
ok 609 - N1-N6 non-canonical lines get no mark
  ---
  duration_ms: 0.222776
  ...
# Subtest: C1-C3 consensus is exact or unresolved
ok 610 - C1-C3 consensus is exact or unresolved
  ---
  duration_ms: 0.566211
  ...
# Subtest: freshnessMarkResolution treats evaluator new as unresolved
ok 611 - freshnessMarkResolution treats evaluator new as unresolved
  ---
  duration_ms: 0.142762
  ...
# Subtest: freshnessMarkSourceInText covers rendered fragments
ok 612 - freshnessMarkSourceInText covers rendered fragments
  ---
  duration_ms: 0.210892
  ...
# Subtest: tone order: closed, then due, then age 0, then out of scope
ok 613 - tone order: closed, then due, then age 0, then out of scope
  ---
  duration_ms: 0.370468
  ...
# Subtest: no tooltip ever contains a double colon
ok 614 - no tooltip ever contains a double colon
  ---
  duration_ms: 0.694486
  ...
# Subtest: freshnessShortDate pins English names and the year rule
ok 615 - freshnessShortDate pins English names and the year rule
  ---
  duration_ms: 0.107947
  ...
# Subtest: DOM builder structure, attributes, and ring geometry
ok 616 - DOM builder structure, attributes, and ring geometry
  ---
  duration_ms: 1.025789
  ...
# Subtest: every mark helper is synchronous and never throws on bad input
ok 617 - every mark helper is synchronous and never throws on bad input
  ---
  duration_ms: 0.117985
  ...
# Subtest: freshness namespace v12 exposes unblock TICKLER metadata and writers
ok 618 - freshness namespace v12 exposes unblock TICKLER metadata and writers
  ---
  duration_ms: 11.713048
  ...
# Subtest: freshness state and count API expose an unblock return source
ok 619 - freshness state and count API expose an unblock return source
  ---
  duration_ms: 1.560801
  ...
# Subtest: checklist rows report tier and rank while keeping the READY bucket null
ok 620 - checklist rows report tier and rank while keeping the READY bucket null
  ---
  duration_ms: 1.300183
  ...
# Subtest: tier, isDue, and rank cover lane rows
ok 621 - tier, isDue, and rank cover lane rows
  ---
  duration_ms: 2.519522
  ...
# Subtest: memo invalidates on a new tasks array, rollover, and frontmatter
ok 622 - memo invalidates on a new tasks array, rollover, and frontmatter
  ---
  duration_ms: 2.174333
  ...
# Subtest: the reload event fires only when the due key set changes
ok 623 - the reload event fires only when the due key set changes
  ---
  duration_ms: 1.279344
  ...
# Subtest: status bar text covers every state, and a missing host stays quiet
ok 624 - status bar text covers every state, and a missing host stays quiet
  ---
  duration_ms: 1.100562
  ...
# Subtest: status bar clicks through, falling back to rotten
ok 625 - status bar clicks through, falling back to rotten
  ---
  duration_ms: 3.961827
  ...
# Subtest: every freshness api member is synchronous and never throws
ok 626 - every freshness api member is synchronous and never throws
  ---
  duration_ms: 2.069974
  ...
# Subtest: placement vectors P1-P11, P14-P16, P18 stamp canonically
ok 627 - placement vectors P1-P11, P14-P16, P18 stamp canonically
  ---
  duration_ms: 3.380676
  ...
# Subtest: P12 set and clear refresh stamps alongside
ok 628 - P12 set and clear refresh stamps alongside
  ---
  duration_ms: 0.285555
  ...
# Subtest: P13 recurring and P17 done tasks are refused unchanged
ok 629 - P13 recurring and P17 done tasks are refused unchanged
  ---
  duration_ms: 0.182669
  ...
# Subtest: U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
ok 630 - U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
  ---
  duration_ms: 0.747448
  ...
# Subtest: reader reports misplaced and duplicate fields
ok 631 - reader reports misplaced and duplicate fields
  ---
  duration_ms: 0.340661
  ...
# Subtest: Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
ok 632 - Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
  ---
  duration_ms: 4.169334
  ...
# Subtest: Q2 tier order beats path order
ok 633 - Q2 tier order beats path order
  ---
  duration_ms: 1.094821
  ...
# Subtest: L1 lane due and stamped today
ok 634 - L1 lane due and stamped today
  ---
  duration_ms: 0.375236
  ...
# Subtest: L2 lane overrides refresh
ok 635 - L2 lane overrides refresh
  ---
  duration_ms: 0.243074
  ...
# Subtest: L3 lane exclusions have no tier
ok 636 - L3 lane exclusions have no tier
  ---
  duration_ms: 0.431885
  ...
# Subtest: L4 lane off switch and null default
ok 637 - L4 lane off switch and null default
  ---
  duration_ms: 0.258493
  ...
# Subtest: L5 lane order never stamped first
ok 638 - L5 lane order never stamped first
  ---
  duration_ms: 0.366781
  ...
# Subtest: R1 TICKLER beats older ROTTEN
ok 639 - R1 TICKLER beats older ROTTEN
  ---
  duration_ms: 0.339969
  ...
# Subtest: R2 tickler orders by due date then path and line
ok 640 - R2 tickler orders by due date then path and line
  ---
  duration_ms: 0.631516
  ...
# Subtest: missing created sorts after dated peers
ok 641 - missing created sorts after dated peers
  ---
  duration_ms: 0.719124
  ...
# Subtest: B1 upkeep counts outside the lanes
ok 642 - B1 upkeep counts outside the lanes
  ---
  duration_ms: 2.108908
  ...
# Subtest: review model meter uses upkeep and exposes refreshed
ok 643 - review model meter uses upkeep and exposes refreshed
  ---
  duration_ms: 0.311655
  ...
# Subtest: RC1 arrived: past scheduled walks RECURRING with lane and null state
ok 644 - RC1 arrived: past scheduled walks RECURRING with lane and null state
  ---
  duration_ms: 2.58618
  ...
# Subtest: RC2 arrives today: due today with zero days overdue
ok 645 - RC2 arrives today: due today with zero days overdue
  ---
  duration_ms: 0.268152
  ...
# Subtest: RC3 not yet: future scheduled walks nowhere
ok 646 - RC3 not yet: future scheduled walks nowhere
  ---
  duration_ms: 0.216464
  ...
# Subtest: RC4 due only, past: the due date is the occurrence
ok 647 - RC4 due only, past: the due date is the occurrence
  ---
  duration_ms: 0.21456
  ...
# Subtest: RC5 due only, future: walks nowhere
ok 648 - RC5 due only, future: walks nowhere
  ---
  duration_ms: 0.242683
  ...
# Subtest: RC6 earliest date wins across start and due
ok 649 - RC6 earliest date wins across start and due
  ---
  duration_ms: 0.267641
  ...
# Subtest: RC7 undated: no occurrence, no tier
ok 650 - RC7 undated: no occurrence, no tier
  ---
  duration_ms: 0.292429
  ...
# Subtest: RC8 lanes: recurring lane rows keep their lane with null state
ok 651 - RC8 lanes: recurring lane rows keep their lane with null state
  ---
  duration_ms: 0.451151
  ...
# Subtest: RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
ok 652 - RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
  ---
  duration_ms: 1.537657
  ...
# Subtest: RC10 checklist wins: a recurring chore stays in its checklist tier
ok 653 - RC10 checklist wins: a recurring chore stays in its checklist tier
  ---
  duration_ms: 0.434159
  ...
# Subtest: RC11 a stray stamp is ignored: recurring with null state
ok 654 - RC11 a stray stamp is ignored: recurring with null state
  ---
  duration_ms: 0.346973
  ...
# Subtest: RC12 order and counts: due_on, then path, then line; recurring adds no due
ok 655 - RC12 order and counts: due_on, then path, then line; recurring adds no due
  ---
  duration_ms: 1.100031
  ...
# Subtest: recurring rows adapt due and start from Tasks fields and inline fallbacks
ok 656 - recurring rows adapt due and start from Tasks fields and inline fallbacks
  ---
  duration_ms: 1.219109
  ...
# Subtest: status view counts RECURRING as a due commitment tier
ok 657 - status view counts RECURRING as a due commitment tier
  ---
  duration_ms: 0.346542
  ...
# Subtest: footer groups, entry view, and legend cover RECURRING
ok 658 - footer groups, entry view, and legend cover RECURRING
  ---
  duration_ms: 0.856035
  ...
# Subtest: a stale-stamped recurring row marks due with the resolve hint
ok 659 - a stale-stamped recurring row marks due with the resolve hint
  ---
  duration_ms: 0.963019
  ...
# Subtest: freshness namespace v12 keeps recurring and removes reference capabilities
ok 660 - freshness namespace v12 keeps recurring and removes reference capabilities
  ---
  duration_ms: 3.544891
  ...
# Subtest: hidden recurring ^ref keeps ordinary visibility (Rust parity)
ok 661 - hidden recurring ^ref keeps ordinary visibility (Rust parity)
  ---
  duration_ms: 0.805389
  ...
# Subtest: bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
ok 662 - bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
  ---
  duration_ms: 4.984461
  ...
# Subtest: day numbers stay calendar-local across a DST boundary
ok 663 - day numbers stay calendar-local across a DST boundary
  ---
  duration_ms: 0.468746
  ...
# Subtest: reviewModel shares counts, meter, tooltip, and severity
ok 664 - reviewModel shares counts, meter, tooltip, and severity
  ---
  duration_ms: 0.466631
  ...
# Subtest: memo serves warm map hits and misses use the per-row evaluator
ok 665 - memo serves warm map hits and misses use the per-row evaluator
  ---
  duration_ms: 6.790969
  ...
# Subtest: config snapshot caches the parse and invalidates explicitly
ok 666 - config snapshot caches the parse and invalidates explicitly
  ---
  duration_ms: 1.493011
  ...
# Subtest: review chips share the model with severity classes
ok 667 - review chips share the model with severity classes
  ---
  duration_ms: 1.066096
  ...
# Subtest: warm lookups reuse one snapshot without re-reading config
ok 668 - warm lookups reuse one snapshot without re-reading config
  ---
  duration_ms: 1.956116
  ...
# Subtest: same-array cache updates and Today changes rebuild the memo
ok 669 - same-array cache updates and Today changes rebuild the memo
  ---
  duration_ms: 2.806962
  ...
# Subtest: duplicate block IDs keep each row's own classification
ok 670 - duplicate block IDs keep each row's own classification
  ---
  duration_ms: 1.853561
  ...
# Subtest: line identity separates same-path rows without block IDs
ok 671 - line identity separates same-path rows without block IDs
  ---
  duration_ms: 0.99985
  ...
# Subtest: interval lookup serves the cached interval with one memo acquisition
ok 672 - interval lookup serves the cached interval with one memo acquisition
  ---
  duration_ms: 1.094921
  ...
# Subtest: S1 new through S4 overdue
ok 673 - S1 new through S4 overdue
  ---
  duration_ms: 3.114008
  ...
# Subtest: S5 task beats note, S6 note beats config, S7 config
ok 674 - S5 task beats note, S6 note beats config, S7 config
  ---
  duration_ms: 0.680941
  ...
# Subtest: S8 invalid overrides fall through with lints
ok 675 - S8 invalid overrides fall through with lints
  ---
  duration_ms: 0.414812
  ...
# Subtest: S9 malformed and S10 future stamps read as new
ok 676 - S9 malformed and S10 future stamps read as new
  ---
  duration_ms: 0.224278
  ...
# Subtest: S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
ok 677 - S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
  ---
  duration_ms: 0.321364
  ...
# Subtest: S13 out-of-scope rows read null
ok 678 - S13 out-of-scope rows read null
  ---
  duration_ms: 0.31386
  ...
# Subtest: S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
ok 679 - S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
  ---
  duration_ms: 1.241702
  ...
# Subtest: S15 counts (updated): upkeep outside the lanes drives the budget
ok 680 - S15 counts (updated): upkeep outside the lanes drives the budget
  ---
  duration_ms: 1.112615
  ...
# Subtest: config coercion keeps defaults, flags invalid, ignores unknown keys
ok 681 - config coercion keeps defaults, flags invalid, ignores unknown keys
  ---
  duration_ms: 1.337425
  ...
# Subtest: loadFreshnessConfig reads the block with plan-style injectables
ok 682 - loadFreshnessConfig reads the block with plan-style injectables
  ---
  duration_ms: 0.880391
  ...
# Subtest: interval precedence is task, note, config, default
ok 683 - interval precedence is task, note, config, default
  ---
  duration_ms: 0.215001
  ...
# Subtest: intervalForLine covers every source with its Ready fallback
ok 684 - intervalForLine covers every source with its Ready fallback
  ---
  duration_ms: 0.782885
  ...
# Subtest: project tracking stays special while reference tasks use ordinary Ready freshness
ok 685 - project tracking stays special while reference tasks use ordinary Ready freshness
  ---
  duration_ms: 4.589927
  ...
# Subtest: reference tasks match ordinary interval precedence and lane behavior
ok 686 - reference tasks match ordinary interval precedence and lane behavior
  ---
  duration_ms: 2.555631
  ...
# Subtest: obsolete reference interval keys are ignored and project config still validates
ok 687 - obsolete reference interval keys are ignored and project config still validates
  ---
  duration_ms: 0.752096
  ...
# Subtest: references use ordinary keep decisions and the nine-tier queue shape
ok 688 - references use ordinary keep decisions and the nine-tier queue shape
  ---
  duration_ms: 1.830666
  ...
# Subtest: CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
ok 689 - CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
  ---
  duration_ms: 2.923994
  ...
# Subtest: CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
ok 690 - CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
  ---
  duration_ms: 1.851405
  ...
# Subtest: freshness namespace v12 retains the tracker capability contract
ok 691 - freshness namespace v12 retains the tracker capability contract
  ---
  duration_ms: 4.762375
  ...
# Subtest: UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
ok 692 - UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
  ---
  duration_ms: 2.943391
  ...
# Subtest: UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
ok 693 - UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
  ---
  duration_ms: 0.453697
  ...
# Subtest: UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
ok 694 - UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
  ---
  duration_ms: 0.302248
  ...
# Subtest: UB11 scheduled wins a tie with the unblock date
ok 695 - UB11 scheduled wins a tie with the unblock date
  ---
  duration_ms: 0.307067
  ...
# Subtest: unblocked reader takes the latest valid duplicate and reports malformed values
ok 696 - unblocked reader takes the latest valid duplicate and reports malformed values
  ---
  duration_ms: 0.274865
  ...
# Subtest: UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
ok 697 - UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
  ---
  duration_ms: 0.41879
  ...
# Subtest: UB14 TICKLERs with the same due date sort only by path and line
ok 698 - UB14 TICKLERs with the same due date sort only by path and line
  ---
  duration_ms: 1.450922
  ...
# Subtest: UB15 a scheduled ^prj resurfaces in PROJECTS
ok 699 - UB15 a scheduled ^prj resurfaces in PROJECTS
  ---
  duration_ms: 0.190143
  ...
# Subtest: an active-note Pomodoro target still jumps and centers immediately
ok 700 - an active-note Pomodoro target still jumps and centers immediately
  ---
  duration_ms: 9.445431
  ...
# Subtest: the first fallback press only opens daily and the second press jumps
ok 701 - the first fallback press only opens daily and the second press jumps
  ---
  duration_ms: 2.49255
  ...
# Subtest: a daily note with no target defers its notice until the second press
ok 702 - a daily note with no target defers its notice until the second press
  ---
  duration_ms: 1.112334
  ...
# Subtest: an already-open daily leaf retains its live cursor and viewport
ok 703 - an already-open daily leaf retains its live cursor and viewport
  ---
  duration_ms: 1.421755
  ...
# Subtest: a second press after reused-leaf fallback performs the Pomodoro jump
ok 704 - a second press after reused-leaf fallback performs the Pomodoro jump
  ---
  duration_ms: 1.247362
  ...
# Subtest: the standalone daily-note command activates a reused daily leaf
ok 705 - the standalone daily-note command activates a reused daily leaf
  ---
  duration_ms: 0.893086
  ...
# Subtest: a closed then reopened daily note restores its in-session location
ok 706 - a closed then reopened daily note restores its in-session location
  ---
  duration_ms: 1.521366
  ...
# Subtest: different-path and invalid locations do not leak into a daily note
ok 707 - different-path and invalid locations do not leak into a daily note
  ---
  duration_ms: 0.768367
  ...
# Subtest: out-of-range remembered coordinates are clamped safely
ok 708 - out-of-range remembered coordinates are clamped safely
  ---
  duration_ms: 1.825998
  ...
# Subtest: a rapid second press cancels an older fallback restore
ok 709 - a rapid second press cancels an older fallback restore
  ---
  duration_ms: 1.36667
  ...
# Subtest: navigation and unload clean up daily scroll listeners and deferred work
ok 710 - navigation and unload clean up daily scroll listeners and deferred work
  ---
  duration_ms: 0.640704
  ...
# Subtest: crowded chip: over count is red with tooltip, aria, and names
ok 711 - crowded chip: over count is red with tooltip, aria, and names
  ---
  duration_ms: 1.209691
  ...
# Subtest: crowded chip: calm zero and unavailable dash
ok 712 - crowded chip: calm zero and unavailable dash
  ---
  duration_ms: 0.218056
  ...
# Subtest: crowded chip: names at most five notes
ok 713 - crowded chip: names at most five notes
  ---
  duration_ms: 0.27265
  ...
# Subtest: crowded chip: classes, text, aria, and arrow
ok 714 - crowded chip: classes, text, aria, and arrow
  ---
  duration_ms: 1.511346
  ...
# Subtest: crowded chip: refresh in place keeps the anchor, unload drops it
ok 715 - crowded chip: refresh in place keeps the anchor, unload drops it
  ---
  duration_ms: 0.615295
  ...
# Subtest: anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
ok 716 - anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
  ---
  duration_ms: 0.609805
  ...
# Subtest: ready-notes summary: crowded, calm, and unavailable
ok 717 - ready-notes summary: crowded, calm, and unavailable
  ---
  duration_ms: 0.247162
  ...
# Subtest: ready-notes bar: cap tick and red overflow within 30 cells
ok 718 - ready-notes bar: cap tick and red overflow within 30 cells
  ---
  duration_ms: 0.204761
  ...
# Subtest: ready-notes block: model and render with grid, pills, and footer
ok 719 - ready-notes block: model and render with grid, pills, and footer
  ---
  duration_ms: 1.329308
  ...
# Subtest: ready-notes block: unavailable renders a dash line
ok 720 - ready-notes block: unavailable renders a dash line
  ---
  duration_ms: 0.42927
  ...
# Subtest: heading matcher: fences, level, case, and first-only
ok 721 - heading matcher: fences, level, case, and first-only
  ---
  duration_ms: 0.385997
  ...
# Subtest: heading chip copy: room, full, crowded, exempt, unavailable
ok 722 - heading chip copy: room, full, crowded, exempt, unavailable
  ---
  duration_ms: 0.336643
  ...
# Subtest: heading chip key is stable for equal models
ok 723 - heading chip key is stable for equal models
  ---
  duration_ms: 0.144366
  ...
# Subtest: reading view: appends the chip to the matching h2 only
ok 724 - reading view: appends the chip to the matching h2 only
  ---
  duration_ms: 1.305052
  ...
# Subtest: reading view: no chip for ineligible notes
ok 725 - reading view: no chip for ineligible notes
  ---
  duration_ms: 0.117033
  ...
# Subtest: one live-refresh fan-out reaches every family
ok 726 - one live-refresh fan-out reaches every family
  ---
  duration_ms: 0.891202
  ...
# Subtest: ledger-tools CSS is theme-safe for the new views
ok 727 - ledger-tools CSS is theme-safe for the new views
  ---
  duration_ms: 0.524091
  ...
# Subtest: maxReadyPerNote defaults to 5 and validates 1–999
ok 728 - maxReadyPerNote defaults to 5 and validates 1–999
  ---
  duration_ms: 2.316785
  ...
# Subtest: loadPlanCaps caches on a stat key and detects edits
ok 729 - loadPlanCaps caches on a stat key and detects edits
  ---
  duration_ms: 0.615666
  ...
# Subtest: loadPlanCaps handles deletion, invalid edits, and recovery
ok 730 - loadPlanCaps handles deletion, invalid edits, and recovery
  ---
  duration_ms: 0.689978
  ...
# Subtest: loadPlanCaps without statSync reads through uncached
ok 731 - loadPlanCaps without statSync reads through uncached
  ---
  duration_ms: 0.420383
  ...
# Subtest: noteFrontmatter resolves through getFileCache, not getCache
ok 732 - noteFrontmatter resolves through getFileCache, not getCache
  ---
  duration_ms: 0.946137
  ...
# Subtest: task_refresh applies through the shared reader
ok 733 - task_refresh applies through the shared reader
  ---
  duration_ms: 3.5864
  ...
# Subtest: noteReadyKindFromType covers every R11 form
ok 734 - noteReadyKindFromType covers every R11 form
  ---
  duration_ms: 0.461832
  ...
# Subtest: noteReadyStatusLabel mirrors ProjectStatus::parse
ok 735 - noteReadyStatusLabel mirrors ProjectStatus::parse
  ---
  duration_ms: 0.317586
  ...
# Subtest: noteReadyParentStem strips alias, heading, and path
ok 736 - noteReadyParentStem strips alias, heading, and path
  ---
  duration_ms: 0.34029
  ...
# Subtest: parseNoteReadyCap covers every R8 form
ok 737 - parseNoteReadyCap covers every R8 form
  ---
  duration_ms: 0.850344
  ...
# Subtest: R1: 6 tasks at the default cap are crowded with over_by 1
ok 738 - R1: 6 tasks at the default cap are crowded with over_by 1
  ---
  duration_ms: 9.000451
  ...
# Subtest: R2: 5 tasks are full with no lint
ok 739 - R2: 5 tasks are full with no lint
  ---
  duration_ms: 2.475128
  ...
# Subtest: R3: hidden, future, blocked, and non-TODO rows never count
ok 740 - R3: hidden, future, blocked, and non-TODO rows never count
  ---
  duration_ms: 2.7067
  ...
# Subtest: R4: make-up splits 1 ready + 1 new + 1 rotten
ok 741 - R4: make-up splits 1 ready + 1 new + 1 rotten
  ---
  duration_ms: 2.14675
  ...
# Subtest: R5: recurring rows are excluded but tallied
ok 742 - R5: recurring rows are excluded but tallied
  ---
  duration_ms: 2.325651
  ...
# Subtest: R6: a visible ^prj task never counts
ok 743 - R6: a visible ^prj task never counts
  ---
  duration_ms: 1.153062
  ...
# Subtest: R7: daily, untyped, template, done, and dash rows are absent
ok 744 - R7: daily, untyped, template, done, and dash rows are absent
  ---
  duration_ms: 1.588894
  ...
# Subtest: R8: ready_cap forms map to cap, exempt, or lint-then-default
ok 745 - R8: ready_cap forms map to cap, exempt, or lint-then-default
  ---
  duration_ms: 2.53958
  ...
# Subtest: R9: a parent with two children counts 3
ok 746 - R9: a parent with two children counts 3
  ---
  duration_ms: 0.89496
  ...
# Subtest: R10: terminal projects are not capped and lint once
ok 747 - R10: terminal projects are not capped and lint once
  ---
  duration_ms: 1.196866
  ...
# Subtest: R11: every type form and nested folders are eligible
ok 748 - R11: every type form and nested folders are eligible
  ---
  duration_ms: 1.135929
  ...
# Subtest: R12: stamping a NEW task keeps the count and moves the make-up
ok 749 - R12: stamping a NEW task keeps the count and moves the make-up
  ---
  duration_ms: 2.011462
  ...
# Subtest: R13: a Today-linked task still counts
ok 750 - R13: a Today-linked task still counts
  ---
  duration_ms: 0.597972
  ...
# Subtest: R14: max_ready_per_note 3 caps others while ready_cap 8 holds
ok 751 - R14: max_ready_per_note 3 caps others while ready_cap 8 holds
  ---
  duration_ms: 2.53928
  ...
# Subtest: api.noteReady is frozen at version 1 under api v3
ok 752 - api.noteReady is frozen at version 1 under api v3
  ---
  duration_ms: 0.296296
  ...
# Subtest: counted and inCrowdedNote resolve per task
ok 753 - counted and inCrowdedNote resolve per task
  ---
  duration_ms: 3.169153
  ...
# Subtest: groupLabel ranks crowded notes by excess
ok 754 - groupLabel ranks crowded notes by excess
  ---
  duration_ms: 6.00492
  ...
# Subtest: snapshot sorts crowded, full, room, empty, exempt and splits totals
ok 755 - snapshot sorts crowded, full, room, empty, exempt and splits totals
  ---
  duration_ms: 7.052109
  ...
# Subtest: missing Tasks data and a cold cache are unavailable, never zero
ok 756 - missing Tasks data and a cold cache are unavailable, never zero
  ---
  duration_ms: 1.368984
  ...
# Subtest: throwing Tasks guards never throw
ok 757 - throwing Tasks guards never throw
  ---
  duration_ms: 0.845435
  ...
# Subtest: snapshot reuses the memo without reparsing or re-walking
ok 758 - snapshot reuses the memo without reparsing or re-walking
  ---
  duration_ms: 1.041178
  ...
# Subtest: a task edit rebuilds through the cache-update handler
ok 759 - a task edit rebuilds through the cache-update handler
  ---
  duration_ms: 1.166378
  ...
# Subtest: a ready_cap edit rebuilds and fires the query-refresh trigger
ok 760 - a ready_cap edit rebuilds and fires the query-refresh trigger
  ---
  duration_ms: 0.878508
  ...
# Subtest: rename and delete move the eligibility entry
ok 761 - rename and delete move the eligibility entry
  ---
  duration_ms: 1.047521
  ...
# Subtest: day rollover rebuilds the snapshot date
ok 762 - day rollover rebuilds the snapshot date
  ---
  duration_ms: 0.881895
  ...
# Subtest: a config edit flows through the stat cache
ok 763 - a config edit flows through the stat cache
  ---
  duration_ms: 1.896012
  ...
# Subtest: untyped and non-markdown vault events are no-ops
ok 764 - untyped and non-markdown vault events are no-ops
  ---
  duration_ms: 0.761034
  ...
# Subtest: memo hits never re-walk the vault
ok 765 - memo hits never re-walk the vault
  ---
  duration_ms: 55.110595
  ...
# Subtest: the startup storm is linear
ok 766 - the startup storm is linear
  ---
  duration_ms: 16.425072
  ...
# Subtest: the first resolved event forces one rebuild and later ones do not
ok 767 - the first resolved event forces one rebuild and later ones do not
  ---
  duration_ms: 1.279774
  ...
# Subtest: noteReadyEvaluate is pure and mirrors the Rust totals
ok 768 - noteReadyEvaluate is pure and mirrors the Rust totals
  ---
  duration_ms: 0.249817
  ...
# Subtest: conformance: merged name with duplicate
ok 769 - conformance: merged name with duplicate
  ---
  duration_ms: 4.097316
  ...
# Subtest: conformance: link forms and exclusions
ok 770 - conformance: link forms and exclusions
  ---
  duration_ms: 0.797623
  ...
# Subtest: conformance: unnamed placeholders
ok 771 - conformance: unnamed placeholders
  ---
  duration_ms: 0.355139
  ...
# Subtest: conformance: subheading in the section
ok 772 - conformance: subheading in the section
  ---
  duration_ms: 0.23027
  ...
# Subtest: conformance: open inventory label
ok 773 - conformance: open inventory label
  ---
  duration_ms: 0.331704
  ...
# Subtest: conformance: over the cap
ok 774 - conformance: over the cap
  ---
  duration_ms: 0.213267
  ...
# Subtest: conformance: cancelled and completed entries
ok 775 - conformance: cancelled and completed entries
  ---
  duration_ms: 0.264395
  ...
# Subtest: exactly at the cap is fine
ok 776 - exactly at the cap is fine
  ---
  duration_ms: 0.175916
  ...
# Subtest: no Pomodoros section degrades to an empty budget
ok 777 - no Pomodoros section degrades to an empty budget
  ---
  duration_ms: 0.435371
  ...
# Subtest: fenced code never counts
ok 778 - fenced code never counts
  ---
  duration_ms: 0.547716
  ...
# Subtest: highlight is the first open non-exempt entry; running is the timed one
ok 779 - highlight is the first open non-exempt entry; running is the timed one
  ---
  duration_ms: 0.462884
  ...
# Subtest: coercePlanCaps ignores a legacy max_now instead of failing
ok 780 - coercePlanCaps ignores a legacy max_now instead of failing
  ---
  duration_ms: 0.30879
  ...
# Subtest: parsePlanCaps defaults, overrides, and invalid fallbacks
ok 781 - parsePlanCaps defaults, overrides, and invalid fallbacks
  ---
  duration_ms: 0.335821
  ...
# Subtest: loadPlanCaps falls back to defaults without fs
ok 782 - loadPlanCaps falls back to defaults without fs
  ---
  duration_ms: 0.498512
  ...
# Subtest: loadPlanCaps falls back to defaults on mobile
ok 783 - loadPlanCaps falls back to defaults on mobile
  ---
  duration_ms: 0.255829
  ...
# Subtest: loadPlanCaps reads plan: and flags invalid values
ok 784 - loadPlanCaps reads plan: and flags invalid values
  ---
  duration_ms: 0.441974
  ...
# Subtest: planBlockTargetPath prefers the containing daily note
ok 785 - planBlockTargetPath prefers the containing daily note
  ---
  duration_ms: 0.740675
  ...
# Subtest: planBlockModel degrades to placeholders, never an error
ok 786 - planBlockModel degrades to placeholders, never an error
  ---
  duration_ms: 0.874621
  ...
# Subtest: planBlockModel renders chips, themes, and lints
ok 787 - planBlockModel renders chips, themes, and lints
  ---
  duration_ms: 1.144386
  ...
# Subtest: planBlockModel adds lane cap lints when a lane is over
ok 788 - planBlockModel adds lane cap lints when a lane is over
  ---
  duration_ms: 0.719774
  ...
# Subtest: plugin exposes the versioned api and registers the bob-plan block
ok 789 - plugin exposes the versioned api and registers the bob-plan block
  ---
  duration_ms: 4.496128
  ...
# Subtest: invalid plan block falls back to full defaults
ok 790 - invalid plan block falls back to full defaults
  ---
  duration_ms: 0.262912
  ...
# Subtest: entries require column-0 dash-space with one status char
ok 791 - entries require column-0 dash-space with one status char
  ---
  duration_ms: 0.171167
  ...
# Subtest: crlf line endings split like lf
ok 792 - crlf line endings split like lf
  ---
  duration_ms: 0.206905
  ...
# Subtest: conformance: empty target means the daily note
ok 793 - conformance: empty target means the daily note
  ---
  duration_ms: 0.182228
  ...
# Subtest: lane predicate matches hide subtags, case, and non-task
ok 794 - lane predicate matches hide subtags, case, and non-task
  ---
  duration_ms: 0.216363
  ...
# Subtest: planBlockModel daily badges follow dashboard section counts
ok 795 - planBlockModel daily badges follow dashboard section counts
  ---
  duration_ms: 1.920438
  ...
# Subtest: planBlockModel keeps a supplied unavailable dashboard budget
ok 796 - planBlockModel keeps a supplied unavailable dashboard budget
  ---
  duration_ms: 0.298099
  ...
# Subtest: work tones: TODAY override and unavailable stay neutral in planBlockModel
ok 797 - work tones: TODAY override and unavailable stay neutral in planBlockModel
  ---
  duration_ms: 0.246561
  ...
# Subtest: shared vector: rollup-archive-review
ok 798 - shared vector: rollup-archive-review
  ---
  duration_ms: 7.597532
  ...
# Subtest: shared vector: review-decisions
ok 799 - shared vector: review-decisions
  ---
  duration_ms: 2.258103
  ...
# Subtest: shared vector: resolution-and-lints
ok 800 - shared vector: resolution-and-lints
  ---
  duration_ms: 2.874891
  ...
# Subtest: shared vector: chips, forecast shares, empty forecasts, and session identity
ok 801 - shared vector: chips, forecast shares, empty forecasts, and session identity
  ---
  duration_ms: 1.447635
  ...
# Subtest: shared vector: split-rounding-and-duration
ok 802 - shared vector: split-rounding-and-duration
  ---
  duration_ms: 0.694376
  ...
# Subtest: shared vector: share-rounding
ok 803 - shared vector: share-rounding
  ---
  duration_ms: 0.382361
  ...
# Subtest: shared vector: daily-review-link
ok 804 - shared vector: daily-review-link
  ---
  duration_ms: 0.368744
  ...
# Subtest: shared vector: rollup-depth-and-parent-shapes
ok 805 - shared vector: rollup-depth-and-parent-shapes
  ---
  duration_ms: 1.095442
  ...
# Subtest: shared vector: unresolved-and-closed-zero
ok 806 - shared vector: unresolved-and-closed-zero
  ---
  duration_ms: 0.856957
  ...
# Subtest: shared vector: parent-scalar-shapes
ok 807 - shared vector: parent-scalar-shapes
  ---
  duration_ms: 1.767195
  ...
# Subtest: dedicated link parser keeps embeds and one struck link, but rejects prose
ok 808 - dedicated link parser keeps embeds and one struck link, but rejects prose
  ---
  duration_ms: 0.28242
  ...
# Subtest: FNV-1a fallback for job maps to the pinned magenta slot
ok 809 - FNV-1a fallback for job maps to the pinned magenta slot
  ---
  duration_ms: 0.133826
  ...
# Subtest: rollup and area-color lints are reported once per note
ok 810 - rollup and area-color lints are reported once per note
  ---
  duration_ms: 0.386618
  ...
# Subtest: chip DOM exposes forecast, hue, accessible text, and tooltip
ok 811 - chip DOM exposes forecast, hue, accessible text, and tooltip
  ---
  duration_ms: 0.248915
  ...
# Subtest: Reading view appends a forecast chip before its Task Link list
ok 812 - Reading view appends a forecast chip before its Task Link list
  ---
  duration_ms: 4.566281
  ...
# Subtest: Live Preview places a chip widget at the end of the Pomodoro line
ok 813 - Live Preview places a chip widget at the end of the Pomodoro line
  ---
  duration_ms: 0.745203
  ...
# Subtest: Live Preview skips chips in Source mode
ok 814 - Live Preview skips chips in Source mode
  ---
  duration_ms: 0.216884
  ...
# Subtest: Reading view finds embedded Task Links via src
ok 815 - Reading view finds embedded Task Links via src
  ---
  duration_ms: 0.476731
  ...
# Subtest: Obsidian frontmatter shapes unwrap nested wikilink arrays
ok 816 - Obsidian frontmatter shapes unwrap nested wikilink arrays
  ---
  duration_ms: 0.161268
  ...
# Subtest: parser accepts the PM1-PM5 conformance vectors verbatim
ok 817 - parser accepts the PM1-PM5 conformance vectors verbatim
  ---
  duration_ms: 1.83239
  ...
# Subtest: parser rejects the PM7-PM12 conformance vectors verbatim
ok 818 - parser rejects the PM7-PM12 conformance vectors verbatim
  ---
  duration_ms: 0.288431
  ...
# Subtest: PM6 with the ladder unknown omits P-labels instead of guessing
ok 819 - PM6 with the ladder unknown omits P-labels instead of guessing
  ---
  duration_ms: 0.193459
  ...
# Subtest: PM13-PM17 ladder and line variants hold
ok 820 - PM13-PM17 ladder and line variants hold
  ---
  duration_ms: 0.3247
  ...
# Subtest: no model output contains a double colon
ok 821 - no model output contains a double colon
  ---
  duration_ms: 0.794237
  ...
# Subtest: element structure and the decorative/inheritColor options
ok 822 - element structure and the decorative/inheritColor options
  ---
  duration_ms: 0.352914
  ...
# Subtest: Live Preview decorations fold space, reveal, and refuse
ok 823 - Live Preview decorations fold space, reveal, and refuse
  ---
  duration_ms: 1.40845
  ...
# Subtest: a line with fresh and priority fields gets a disjoint decoration
ok 824 - a line with fresh and priority fields gets a disjoint decoration
  ---
  duration_ms: 0.216694
  ...
# Subtest: widget mousedown reveals the field at the folded offset
ok 825 - widget mousedown reveals the field at the folded offset
  ---
  duration_ms: 0.622078
  ...
# Subtest: rendered views split task nodes and skip exclusions
ok 826 - rendered views split task nodes and skip exclusions
  ---
  duration_ms: 1.651164
  ...
# Subtest: ladder coercion is lenient: valid, partial, and unknown
ok 827 - ladder coercion is lenient: valid, partial, and unknown
  ---
  duration_ms: 0.527678
  ...
# Subtest: ladder snapshot reads the file and reuses the cache
ok 828 - ladder snapshot reads the file and reuses the cache
  ---
  duration_ms: 2.000732
  ...
# Subtest: ladder snapshot degrades on missing files and parse errors
ok 829 - ladder snapshot degrades on missing files and parse errors
  ---
  duration_ms: 0.888547
  ...
# Subtest: ladder snapshot is unknown on mobile
ok 830 - ladder snapshot is unknown on mobile
  ---
  duration_ms: 15.129407
  ...
# Subtest: api.priorityMarks v1 is additive, sync, and never throwing
ok 831 - api.priorityMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 4.502598
  ...
# Subtest: session toggle and onload wiring
ok 832 - session toggle and onload wiring
  ---
  duration_ms: 0.79105
  ...
# Subtest: styles.css contract: masks, both hosts, repair flag, resting
ok 833 - styles.css contract: masks, both hosts, repair flag, resting
  ---
  duration_ms: 0.80138
  ...
# Subtest: P1/P3/P4: open entries mark plain and aliased links
ok 834 - P1/P3/P4: open entries mark plain and aliased links
  ---
  duration_ms: 2.115481
  ...
# Subtest: P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
ok 835 - P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
  ---
  duration_ms: 2.305513
  ...
# Subtest: P5: closed entries never mark, even with 🍅 history
ok 836 - P5: closed entries never mark, even with 🍅 history
  ---
  duration_ms: 0.721748
  ...
# Subtest: P6/P7: embedded and struck links never mark
ok 837 - P6/P7: embedded and struck links never mark
  ---
  duration_ms: 0.248154
  ...
# Subtest: P8: both trailing-\# move-only forms mark
ok 838 - P8: both trailing-\# move-only forms mark
  ---
  duration_ms: 0.25688
  ...
# Subtest: P9: nested and prose-mixed links never mark
ok 839 - P9: nested and prose-mixed links never mark
  ---
  duration_ms: 0.156088
  ...
# Subtest: P10: fenced, off-section, and off-note links never mark
ok 840 - P10: fenced, off-section, and off-note links never mark
  ---
  duration_ms: 0.383272
  ...
# Subtest: P11: unresolved targets and non-task blocks get no mark
ok 841 - P11: unresolved targets and non-task blocks get no mark
  ---
  duration_ms: 0.456773
  ...
# Subtest: P13: a same-note target reads the live doc
ok 842 - P13: a same-note target reads the live doc
  ---
  duration_ms: 0.754421
  ...
# Subtest: P14: expect() wins until the cache agrees or 4 s pass
ok 843 - P14: expect() wins until the cache agrees or 4 s pass
  ---
  duration_ms: 0.926801
  ...
# Subtest: tooltip, element structure, and eq
ok 844 - tooltip, element structure, and eq
  ---
  duration_ms: 0.289143
  ...
# Subtest: Live Preview places one widget at each In Progress link
ok 845 - Live Preview places one widget at each In Progress link
  ---
  duration_ms: 0.479215
  ...
# Subtest: widget mousedown places the cursor at the link start
ok 846 - widget mousedown places the cursor at the link start
  ---
  duration_ms: 0.397579
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
ok 847 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 0.432807
  ...
# Subtest: Reading view marks In Progress rows and dedupes
ok 848 - Reading view marks In Progress rows and dedupes
  ---
  duration_ms: 1.110641
  ...
# Subtest: Reading view refuses every non-mark row
ok 849 - Reading view refuses every non-mark row
  ---
  duration_ms: 1.033735
  ...
# Subtest: Reading view allows the 🍅 prefix and the trailing \# marker
ok 850 - Reading view allows the 🍅 prefix and the trailing \# marker
  ---
  duration_ms: 0.320612
  ...
# Subtest: api.progressMarks v1 is additive, sync, and never throwing
ok 851 - api.progressMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.625134
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 852 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 0.848751
  ...
# Subtest: changed-file and rollover refreshes
ok 853 - changed-file and rollover refreshes
  ---
  duration_ms: 0.371108
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 854 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.093469
  ...
# Subtest: styles.css contract: glyph, box, motion, toggle, calm
ok 855 - styles.css contract: glyph, box, motion, toggle, calm
  ---
  duration_ms: 0.639371
  ...
# Subtest: the board registers its code block processor and the Open Reading Board command
ok 856 - the board registers its code block processor and the Open Reading Board command
  ---
  duration_ms: 5.097856
  ...
# Subtest: four lanes render with counts, list and listitem roles, and one hint
ok 857 - four lanes render with counts, list and listitem roles, and one hint
  ---
  duration_ms: 12.804153
  ...
# Subtest: awake cards show kind, topic, added mark, counts, priority, and the pending-sync star
ok 858 - awake cards show kind, topic, added mark, counts, priority, and the pending-sync star
  ---
  duration_ms: 4.253144
  ...
# Subtest: a path-valued Bob audio field produces exactly one visible music marker
ok 859 - a path-valued Bob audio field produces exactly one visible music marker
  ---
  duration_ms: 3.657456
  ...
# Subtest: Snoozed shows Waking, date groups, and Waiting-on rows with their reasons
ok 860 - Snoozed shows Waking, date groups, and Waiting-on rows with their reasons
  ---
  duration_ms: 2.6025
  ...
# Subtest: TODAY pills float linked cards first, and never appear without a ready Today cache
ok 861 - TODAY pills float linked cards first, and never appear without a ready Today cache
  ---
  duration_ms: 6.372742
  ...
# Subtest: the PDF button needs the nav member, macOS, and a source_pdf
ok 862 - the PDF button needs the nav member, macOS, and a source_pdf
  ---
  duration_ms: 9.168681
  ...
# Subtest: click, modifier-click, middle-click, and the Task button route to openLinkText
ok 863 - click, modifier-click, middle-click, and the Task button route to openLinkText
  ---
  duration_ms: 2.071767
  ...
# Subtest: the board is one Tab stop and every key moves or acts
ok 864 - the board is one Tab stop and every key moves or acts
  ---
  duration_ms: 16.977083
  ...
# Subtest: movement targets stay inside the lanes that show cards
ok 865 - movement targets stay inside the lanes that show cards
  ---
  duration_ms: 0.518571
  ...
# Subtest: hovering a Waiting-on row outlines its prerequisite card on the board
ok 866 - hovering a Waiting-on row outlines its prerequisite card on the board
  ---
  duration_ms: 2.135298
  ...
# Subtest: the board never calls a vault write API, in the source or in any gesture
ok 867 - the board never calls a vault write API, in the source or in any gesture
  ---
  duration_ms: 10.701149
  ...
# Subtest: a repaint keeps focus by note path and each lane's scroll position
ok 868 - a repaint keeps focus by note path and each lane's scroll position
  ---
  duration_ms: 3.181868
  ...
# Subtest: a task move and topic/type update repaint handlers while preserving focus and scroll
ok 869 - a task move and topic/type update repaint handlers while preserving focus and scroll
  ---
  duration_ms: 5.614213
  ...
# Subtest: prerequisite identity changes repaint highlighting even when reason text is unchanged
ok 870 - prerequisite identity changes repaint highlighting even when reason text is unchanged
  ---
  duration_ms: 2.953571
  ...
# Subtest: an unchanged board is not repainted; only the data time updates in place
ok 871 - an unchanged board is not repainted; only the data time updates in place
  ---
  duration_ms: 3.306595
  ...
# Subtest: a Today cache change repaints boards from cached data without spawning bob
ok 872 - a Today cache change repaints boards from cached data without spawning bob
  ---
  duration_ms: 4.192806
  ...
# Subtest: first paint is a skeleton in the real grid, then the board without a layout jump
ok 873 - first paint is a skeleton in the real grid, then the board without a layout jump
  ---
  duration_ms: 6.184401
  ...
# Subtest: failures without a frame render an actionable card with Retry
ok 874 - failures without a frame render an actionable card with Retry
  ---
  duration_ms: 15.457324
  ...
# Subtest: a failed manual refresh keeps the last frame and says why with Retry
ok 875 - a failed manual refresh keeps the last frame and says why with Retry
  ---
  duration_ms: 5.04165
  ...
# Subtest: metadata revalidation delivers a silent stale-frame error and recovery updates freshness
ok 876 - metadata revalidation delivers a silent stale-frame error and recovery updates freshness
  ---
  duration_ms: 9.482479
  ...
# Subtest: stale-cache mount refresh failures reach the mounted view
ok 877 - stale-cache mount refresh failures reach the mounted view
  ---
  duration_ms: 7.642106
  ...
# Subtest: unload during a fetch prevents late repaint and queued spawns
ok 878 - unload during a fetch prevents late repaint and queued spawns
  ---
  duration_ms: 3.952339
  ...
# Subtest: in-flight edits and forced refreshes coalesce without dropping mounted fences
ok 879 - in-flight edits and forced refreshes coalesce without dropping mounted fences
  ---
  duration_ms: 15.037312
  ...
# Subtest: manual refresh shows a busy state until the result lands, then announces it
ok 880 - manual refresh shows a busy state until the result lands, then announces it
  ---
  duration_ms: 5.278742
  ...
# Subtest: an older bob without blocked_by falls back to Waiting-on with one lint line
ok 881 - an older bob without blocked_by falls back to Waiting-on with one lint line
  ---
  duration_ms: 4.584936
  ...
# Subtest: an empty queue shows bob's own phrase instead of lanes
ok 882 - an empty queue shows bob's own phrase instead of lanes
  ---
  duration_ms: 1.186075
  ...
# Subtest: fence options reach the fetch and bad options show as muted lint lines
ok 883 - fence options reach the fetch and bad options show as muted lint lines
  ---
  duration_ms: 4.989369
  ...
# Subtest: Snoozed collapses per source path, leaves the key order, and survives repaints
ok 884 - Snoozed collapses per source path, leaves the key order, and survives repaints
  ---
  duration_ms: 9.95789
  ...
# Subtest: unloading a block releases its view, and teardown clears the session state
ok 885 - unloading a block releases its view, and teardown clears the session state
  ---
  duration_ms: 7.719454
  ...
# Subtest: reading board stylesheet contract: selectors, layout, tabular-nums, motion, colors
ok 886 - reading board stylesheet contract: selectors, layout, tabular-nums, motion, colors
  ---
  duration_ms: 0.963991
  ...
# Subtest: Reading Board argv carries bob's fixed queue and optional fence filters
ok 887 - Reading Board argv carries bob's fixed queue and optional fence filters
  ---
  duration_ms: 1.731137
  ...
# Subtest: Reading Board decoder accepts the shared bob fixture and normalizes optional fields
ok 888 - Reading Board decoder accepts the shared bob fixture and normalizes optional fields
  ---
  duration_ms: 0.265036
  ...
# Subtest: Reading Board audio presence survives raw JSON decoding and model construction
ok 889 - Reading Board audio presence survives raw JSON decoding and model construction
  ---
  duration_ms: 5.244307
  ...
# Subtest: Reading Board decoder rejects malformed JSON, shapes, schema, and bob errors
ok 890 - Reading Board decoder rejects malformed JSON, shapes, schema, and bob errors
  ---
  duration_ms: 0.273212
  ...
# Subtest: shared bob spawn passes the vault environment, timeout, and buffer
ok 891 - shared bob spawn passes the vault environment, timeout, and buffer
  ---
  duration_ms: 4.951447
  ...
# Subtest: shared bob spawn maps missing binary and timeout failures
ok 892 - shared bob spawn maps missing binary and timeout failures
  ---
  duration_ms: 1.807322
  ...
# Subtest: Reading Board error cards explain not-found, timeout, schema, and bob errors
ok 893 - Reading Board error cards explain not-found, timeout, schema, and bob errors
  ---
  duration_ms: 0.457243
  ...
# Subtest: Reading Board cache returns stale data while revalidating and keeps a four-entry LRU
ok 894 - Reading Board cache returns stale data while revalidating and keeps a four-entry LRU
  ---
  duration_ms: 1.266729
  ...
# Subtest: Reading Board shares identical flights and coalesces one different follow-up
ok 895 - Reading Board shares identical flights and coalesces one different follow-up
  ---
  duration_ms: 0.981865
  ...
# Subtest: Reading Board refresh is mounted-only, debounced, and reacts to rollover and stale active leaves
ok 896 - Reading Board refresh is mounted-only, debounced, and reacts to rollover and stale active leaves
  ---
  duration_ms: 0.716228
  ...
# Subtest: the shared bob output builds the expected four lanes and preserves bob order
ok 897 - the shared bob output builds the expected four lanes and preserves bob order
  ---
  duration_ms: 4.877737
  ...
# Subtest: each status uses its awake lane and every blocked status uses Snoozed
ok 898 - each status uses its awake lane and every blocked status uses Snoozed
  ---
  duration_ms: 0.480528
  ...
# Subtest: Today floats cards by ledger rank only when the cache is ready
ok 899 - Today floats cards by ledger rank only when the cache is ready
  ---
  duration_ms: 1.222615
  ...
# Subtest: Snoozed groups show waking, schedule, dependency, project, return lane, and mark models
ok 900 - Snoozed groups show waking, schedule, dependency, project, return lane, and mark models
  ---
  duration_ms: 0.64916
  ...
# Subtest: schedule groups follow Monday-start weeks through Sunday across month and year ends
ok 901 - schedule groups follow Monday-start weeks through Sunday across month and year ends
  ---
  duration_ms: 0.258393
  ...
# Subtest: older bob output remains visible in Waiting on and explains the missing reasons
ok 902 - older bob output remains visible in Waiting on and explains the missing reasons
  ---
  duration_ms: 0.888357
  ...
# Subtest: fence options accept parent and type lists while turning bad input into lints
ok 903 - fence options accept parent and type lists while turning bad input into lints
  ---
  duration_ms: 1.244998
  ...
# Subtest: kind names, title code spans, and render signatures are deterministic
ok 904 - kind names, title code spans, and render signatures are deterministic
  ---
  duration_ms: 4.116792
  ...
# Subtest: max_ready defaults to 100 for missing, absent, and null values
ok 905 - max_ready defaults to 100 for missing, absent, and null values
  ---
  duration_ms: 1.436304
  ...
# Subtest: max_ready accepts a custom positive cap
ok 906 - max_ready accepts a custom positive cap
  ---
  duration_ms: 0.233176
  ...
# Subtest: max_ready rejects zero, negative, fractions, strings, booleans, and overflow
ok 907 - max_ready rejects zero, negative, fractions, strings, booleans, and overflow
  ---
  duration_ms: 0.882806
  ...
# Subtest: old configurations and legacy max_now still load
ok 908 - old configurations and legacy max_now still load
  ---
  duration_ms: 0.274094
  ...
# Subtest: READY boundary: only a strict excess turns red
ok 909 - READY boundary: only a strict excess turns red
  ---
  duration_ms: 1.93181
  ...
# Subtest: READY custom-cap boundary
ok 910 - READY custom-cap boundary
  ---
  duration_ms: 0.231552
  ...
# Subtest: READY over is independent of the PLAN ledger status
ok 911 - READY over is independent of the PLAN ledger status
  ---
  duration_ms: 4.275837
  ...
# Subtest: READY predicate: statuses, custom TODO symbols, and non-tasks
ok 912 - READY predicate: statuses, custom TODO symbols, and non-tasks
  ---
  duration_ms: 0.184422
  ...
# Subtest: READY predicate: blocked uses the full list, even outside the queue
ok 913 - READY predicate: blocked uses the full list, even outside the queue
  ---
  duration_ms: 0.379174
  ...
# Subtest: READY predicate: past, today, and future schedules
ok 914 - READY predicate: past, today, and future schedules
  ---
  duration_ms: 0.41351
  ...
# Subtest: READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
ok 915 - READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
  ---
  duration_ms: 0.281037
  ...
# Subtest: READY predicate: Today exclusion
ok 916 - READY predicate: Today exclusion
  ---
  duration_ms: 0.131892
  ...
# Subtest: readyTaskVisible excludes hide variants like Tasks
ok 917 - readyTaskVisible excludes hide variants like Tasks
  ---
  duration_ms: 0.126762
  ...
# Subtest: daily and dashboard share the READY element contract
ok 918 - daily and dashboard share the READY element contract
  ---
  duration_ms: 10.745311
  ...
# Subtest: READY placeholder keeps the limit in its tooltip
ok 919 - READY placeholder keeps the limit in its tooltip
  ---
  duration_ms: 0.145137
  ...
# Subtest: READY keyboard and modifier-key navigation
ok 920 - READY keyboard and modifier-key navigation
  ---
  duration_ms: 0.883978
  ...
# Subtest: READY unavailable without Tasks, on Cold/Initializing, or before Today
ok 921 - READY unavailable without Tasks, on Cold/Initializing, or before Today
  ---
  duration_ms: 3.095292
  ...
# Subtest: READY counts a valid empty queue as zero, not unavailable
ok 922 - READY counts a valid empty queue as zero, not unavailable
  ---
  duration_ms: 0.877216
  ...
# Subtest: READY stays compatible with hosts exposing only getTasks()
ok 923 - READY stays compatible with hosts exposing only getTasks()
  ---
  duration_ms: 1.824936
  ...
# Subtest: READY degrades to unavailable when the Today predicate throws
ok 924 - READY degrades to unavailable when the Today predicate throws
  ---
  duration_ms: 0.50787
  ...
# Subtest: READY renders label/value spans for every budget state
ok 925 - READY renders label/value spans for every budget state
  ---
  duration_ms: 1.211724
  ...
# Subtest: READY live refresh keeps the anchor, spans, and handlers
ok 926 - READY live refresh keeps the anchor, spans, and handlers
  ---
  duration_ms: 1.367723
  ...
# Subtest: READY refresh crosses the over-cap boundary and back
ok 927 - READY refresh crosses the over-cap boundary and back
  ---
  duration_ms: 0.801751
  ...
# Subtest: READY refresh crosses the unavailable boundary and back
ok 928 - READY refresh crosses the unavailable boundary and back
  ---
  duration_ms: 0.568275
  ...
# Subtest: READY never assigns the Obsidian text setter
ok 929 - READY never assigns the Obsidian text setter
  ---
  duration_ms: 1.124608
  ...
# Subtest: READY gating excludes review buckets and keeps the partition
ok 930 - READY gating excludes review buckets and keeps the partition
  ---
  duration_ms: 0.308419
  ...
# Subtest: gated READY tooltip carries total lane pressure
ok 931 - gated READY tooltip carries total lane pressure
  ---
  duration_ms: 0.124538
  ...
# Subtest: planBlockModel gates READY and shares the lane tooltip
ok 932 - planBlockModel gates READY and shares the lane tooltip
  ---
  duration_ms: 0.682023
  ...
# Subtest: READY lint appears only on a strict excess
ok 933 - READY lint appears only on a strict excess
  ---
  duration_ms: 3.463145
  ...
# Subtest: READY lint uses a custom cap
ok 934 - READY lint uses a custom cap
  ---
  duration_ms: 0.574077
  ...
# Subtest: lane lints appear in NEXT, PENDING, READY order
ok 935 - lane lints appear in NEXT, PENDING, READY order
  ---
  duration_ms: 2.788064
  ...
# Subtest: READY lint uses the gated count
ok 936 - READY lint uses the gated count
  ---
  duration_ms: 1.237924
  ...
# Subtest: READY lint stays silent while unavailable
ok 937 - READY lint stays silent while unavailable
  ---
  duration_ms: 0.396498
  ...
# Subtest: READY speaks each host's chip language (daily single-tone, dash two-tone)
ok 938 - READY speaks each host's chip language (daily single-tone, dash two-tone)
  ---
  duration_ms: 2.746706
  ...
# Subtest: daily paint carries lane pressure to the shared READY renderer
ok 939 - daily paint carries lane pressure to the shared READY renderer
  ---
  duration_ms: 20.888925
  ...
# Subtest: daily paint degrades to the legacy tooltip without freshness
ok 940 - daily paint degrades to the legacy tooltip without freshness
  ---
  duration_ms: 2.357172
  ...
# Subtest: work tones: READY model carries the displayed-count tone
ok 941 - work tones: READY model carries the displayed-count tone
  ---
  duration_ms: 0.212536
  ...
# Subtest: ledger LK1–LK19 recognises relation shapes and keeps them out of plan links
ok 942 - ledger LK1–LK19 recognises relation shapes and keeps them out of plan links
  ---
  duration_ms: 2.703512
  ...
# Subtest: parseTrigger parses D[-]<N> dated-entry triggers with offset and span
ok 943 - parseTrigger parses D[-]<N> dated-entry triggers with offset and span
  ---
  duration_ms: 1.713232
  ...
# Subtest: computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
ok 944 - computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
  ---
  duration_ms: 0.40315
  ...
# Subtest: expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
ok 945 - expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
  ---
  duration_ms: 0.44501
  ...
# Subtest: findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
ok 946 - findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
  ---
  duration_ms: 0.356421
  ...
# Subtest: compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
ok 947 - compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
  ---
  duration_ms: 0.319901
  ...
# Subtest: parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
ok 948 - parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
  ---
  duration_ms: 0.149686
  ...
# Subtest: computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
ok 949 - computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
  ---
  duration_ms: 0.182448
  ...
# Subtest: findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
ok 950 - findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
  ---
  duration_ms: 0.189352
  ...
# Subtest: findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
ok 951 - findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
  ---
  duration_ms: 0.301205
  ...
# Subtest: expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
ok 952 - expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
  ---
  duration_ms: 0.601229
  ...
# Subtest: regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
ok 953 - regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
  ---
  duration_ms: 0.392199
  ...
# Subtest: expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
ok 954 - expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
  ---
  duration_ms: 0.291176
  ...
# Subtest: stats fence body sets defaults only and ignores the rest
ok 955 - stats fence body sets defaults only and ignores the rest
  ---
  duration_ms: 1.950866
  ...
# Subtest: stats tile models cover every unit and every quality
ok 956 - stats tile models cover every unit and every quality
  ---
  duration_ms: 0.4659
  ...
# Subtest: stats spark bars mark null gaps, zero ticks, and hollow today
ok 957 - stats spark bars mark null gaps, zero ticks, and hollow today
  ---
  duration_ms: 0.283631
  ...
# Subtest: stats table rows and CSV share the same points
ok 958 - stats table rows and CSV share the same points
  ---
  duration_ms: 0.646084
  ...
# Subtest: stats overview ids prefer the fence, then config, then report order
ok 959 - stats overview ids prefer the fence, then config, then report order
  ---
  duration_ms: 1.0633
  ...
# Subtest: stats window label always states today and tracking start
ok 960 - stats window label always states today and tracking start
  ---
  duration_ms: 0.235169
  ...
# Subtest: stats view state is session-only and per source path
ok 961 - stats view state is session-only and per source path
  ---
  duration_ms: 3.65044
  ...
# Subtest: stats block renders header, tiles, table, and footer from JSON
ok 962 - stats block renders header, tiles, table, and footer from JSON
  ---
  duration_ms: 43.083027
  ...
# Subtest: stats block shows an actionable card with Retry when bob fails
ok 963 - stats block shows an actionable card with Retry when bob fails
  ---
  duration_ms: 42.728255
  ...
# Subtest: stats block registers the processor and the Open Stats command
ok 964 - stats block registers the processor and the Open Stats command
  ---
  duration_ms: 1.391287
  ...
# Subtest: stats stylesheet contract: selectors, tabular-nums, motion, colors
ok 965 - stats stylesheet contract: selectors, tabular-nums, motion, colors
  ---
  duration_ms: 1.394213
  ...
# Subtest: Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
ok 966 - Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
  ---
  duration_ms: 2.933262
  ...
# Subtest: prior buckets align by elapsed position and omit invalid and provisional points
ok 967 - prior buckets align by elapsed position and omit invalid and provisional points
  ---
  duration_ms: 1.13626
  ...
# Subtest: chart renders SVG safely and keeps secondary focus metrics selectable
ok 968 - chart renders SVG safely and keeps secondary focus metrics selectable
  ---
  duration_ms: 11.219057
  ...
# Subtest: grouped chart pins honest buckets, bounds daily detail, and opens validated notes
ok 969 - grouped chart pins honest buckets, bounds daily detail, and opens validated notes
  ---
  duration_ms: 6.512529
  ...
# Subtest: local focus, table, pin, and definition changes reuse the retained report
ok 970 - local focus, table, pin, and definition changes reuse the retained report
  ---
  duration_ms: 6.268052
  ...
# Subtest: keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
ok 971 - keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
  ---
  duration_ms: 36.167898
  ...
# Subtest: schema-1 fallback keeps day quartiles and never invents grouped daily history
ok 972 - schema-1 fallback keeps day quartiles and never invents grouped daily history
  ---
  duration_ms: 3.248845
  ...
# Subtest: ResizeObserver redraws cached data and disconnects across rerenders and unload
ok 973 - ResizeObserver redraws cached data and disconnects across rerenders and unload
  ---
  duration_ms: 132.698341
  ...
# Subtest: stats resolution prefers stats.bob_path, then candidates, then PATH
ok 974 - stats resolution prefers stats.bob_path, then candidates, then PATH
  ---
  duration_ms: 1.947269
  ...
# Subtest: stats home expansion and range/offset normalization
ok 975 - stats home expansion and range/offset normalization
  ---
  duration_ms: 0.452835
  ...
# Subtest: stats fetch always runs show -a -f json plus the chosen flags
ok 976 - stats fetch always runs show -a -f json plus the chosen flags
  ---
  duration_ms: 0.369576
  ...
# Subtest: stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
ok 977 - stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
  ---
  duration_ms: 5.823994
  ...
# Subtest: stats spawn maps ENOENT, timeouts, and stderr to named errors
ok 978 - stats spawn maps ENOENT, timeouts, and stderr to named errors
  ---
  duration_ms: 2.312706
  ...
# Subtest: stats decode accepts schema 1 and rejects the rest defensively
ok 979 - stats decode accepts schema 1 and rejects the rest defensively
  ---
  duration_ms: 0.237674
  ...
# Subtest: stats error cards name the cause and the stats.bob_path fix
ok 980 - stats error cards name the cause and the stats.bob_path fix
  ---
  duration_ms: 0.27249
  ...
# Subtest: stats fetch shares one flight and coalesces one follow-up
ok 981 - stats fetch shares one flight and coalesces one follow-up
  ---
  duration_ms: 22.103846
  ...
# Subtest: stats cache is a small LRU keyed by the argument list
ok 982 - stats cache is a small LRU keyed by the argument list
  ---
  duration_ms: 1.861455
  ...
# Subtest: stats stale entries return immediately and refresh in the background
ok 983 - stats stale entries return immediately and refresh in the background
  ---
  duration_ms: 0.915338
  ...
# Subtest: stats api v2 keeps append and adds fetch plus bobPath
ok 984 - stats api v2 keeps append and adds fetch plus bobPath
  ---
  duration_ms: 0.752898
  ...
# Subtest: statsHomeDir defaults to the real home and strips a trailing slash
ok 985 - statsHomeDir defaults to the real home and strips a trailing slash
  ---
  duration_ms: 0.201585
  ...
# Subtest: stats mac regression: un-injected resolution probes the real home first
ok 986 - stats mac regression: un-injected resolution probes the real home first
  ---
  duration_ms: 0.231041
  ...
# Subtest: stats absolute candidates are probed verbatim with no doubled slashes
ok 987 - stats absolute candidates are probed verbatim with no doubled slashes
  ---
  duration_ms: 0.234978
  ...
# Subtest: stats with no home probes only absolute candidates
ok 988 - stats with no home probes only absolute candidates
  ---
  duration_ms: 0.231973
  ...
# Subtest: stats tilde config expands against the real home
ok 989 - stats tilde config expands against the real home
  ---
  duration_ms: 0.132754
  ...
# Subtest: stats candidate and tried lists share one source of truth
ok 990 - stats candidate and tried lists share one source of truth
  ---
  duration_ms: 0.121562
  ...
# Subtest: stats spawn bob-not-found tried list uses the real home
ok 991 - stats spawn bob-not-found tried list uses the real home
  ---
  duration_ms: 0.932551
  ...
# Subtest: stats unload clears views, timers, cache, and flights
ok 992 - stats unload clears views, timers, cache, and flights
  ---
  duration_ms: 0.539651
  ...
# Subtest: stats namespace v1 serializes versioned review answer JSONL
ok 993 - stats namespace v1 serializes versioned review answer JSONL
  ---
  duration_ms: 6.990142
  ...
# Subtest: stats journal rejects invalid calendar days and outcomes
ok 994 - stats journal rejects invalid calendar days and outcomes
  ---
  duration_ms: 1.190333
  ...
# Subtest: statsReviewHost lowercases, cuts at the first dot, and never throws
ok 995 - statsReviewHost lowercases, cuts at the first dot, and never throws
  ---
  duration_ms: 0.155457
  ...
# Subtest: stats journal plugin passthrough keeps a semver writer and falls back otherwise
ok 996 - stats journal plugin passthrough keeps a semver writer and falls back otherwise
  ---
  duration_ms: 0.859502
  ...
# Subtest: panel dispatch covers every family, custom kinds, and the net exception
ok 997 - panel dispatch covers every family, custom kinds, and the net exception
  ---
  duration_ms: 0.946798
  ...
# Subtest: pomodoro panel shows the supplied total, shares, hue, and safe text
ok 998 - pomodoro panel shows the supplied total, shares, hue, and safe text
  ---
  duration_ms: 10.742277
  ...
# Subtest: home parts use the report catalog for labels, hue slots, and pinned values
ok 999 - home parts use the report catalog for labels, hue slots, and pinned values
  ---
  duration_ms: 9.895399
  ...
# Subtest: areas panel toggles Themes, pins spans, expands projects, and opens home links
ok 1000 - areas panel toggles Themes, pins spans, expands projects, and opens home links
  ---
  duration_ms: 16.580798
  ...
# Subtest: chart pin refreshes Where the time went and Themes honor the pinned span
ok 1001 - chart pin refreshes Where the time went and Themes honor the pinned span
  ---
  duration_ms: 3.50344
  ...
# Subtest: review rows keep their area hue and a missing homes report keeps the saved view
ok 1002 - review rows keep their area hue and a missing homes report keeps the saved view
  ---
  duration_ms: 2.084341
  ...
# Subtest: task home table uses catalog labels and keeps hue dots and mini-bars
ok 1003 - task home table uses catalog labels and keeps hue dots and mini-bars
  ---
  duration_ms: 5.707601
  ...
# Subtest: task flow stacks signed values, keeps missing constituents missing, and labels series
ok 1004 - task flow stacks signed values, keeps missing constituents missing, and labels series
  ---
  duration_ms: 3.088409
  ...
# Subtest: absent companions are named, custom filters are labeled overall, and net splits breakdowns
ok 1005 - absent companions are named, custom filters are labeled overall, and net splits breakdowns
  ---
  duration_ms: 3.877937
  ...
# Subtest: journal panels pair answers with review time and a gapped keep chart under 90%
ok 1006 - journal panels pair answers with review time and a gapped keep chart under 90%
  ---
  duration_ms: 4.917963
  ...
# Subtest: checklist calendar aligns Monday weeks with states, reasons, and provisional today
ok 1007 - checklist calendar aligns Monday weeks with states, reasons, and provisional today
  ---
  duration_ms: 4.815287
  ...
# Subtest: grouped calendars reuse daily points and old schemas fall back with a label
ok 1008 - grouped calendars reuse daily points and old schemas fall back with a label
  ---
  duration_ms: 2.772485
  ...
# Subtest: ISO year boundaries stay in one Monday week and chore dots expose text
ok 1009 - ISO year boundaries stay in one Monday week and chore dots expose text
  ---
  duration_ms: 1.745343
  ...
# Subtest: panel day selection pins the shared day and never fetches
ok 1010 - panel day selection pins the shared day and never fetches
  ---
  duration_ms: 6.303126
  ...
# Subtest: field and formula metrics keep only the focus chart and table
ok 1011 - field and formula metrics keep only the focus chart and table
  ---
  duration_ms: 0.878016
  ...
# Subtest: TT vectors verbatim: task-line gate plus boundary tokens
ok 1012 - TT vectors verbatim: task-line gate plus boundary tokens
  ---
  duration_ms: 2.781623
  ...
# Subtest: TT13-TT14 cursor reveal is inclusive
ok 1013 - TT13-TT14 cursor reveal is inclusive
  ---
  duration_ms: 1.051108
  ...
# Subtest: TT16 coexistence: task tag range is disjoint from priority and date marks
ok 1014 - TT16 coexistence: task tag range is disjoint from priority and date marks
  ---
  duration_ms: 1.097907
  ...
# Subtest: tooltip is exact and never contains a double colon
ok 1015 - tooltip is exact and never contains a double colon
  ---
  duration_ms: 0.203809
  ...
# Subtest: element structure: empty widget span with tooltip attributes
ok 1016 - element structure: empty widget span with tooltip attributes
  ---
  duration_ms: 0.321834
  ...
# Subtest: Live Preview decorations cover exactly the tag and respect reveal and code
ok 1017 - Live Preview decorations cover exactly the tag and respect reveal and code
  ---
  duration_ms: 0.560721
  ...
# Subtest: widget mousedown reveals the tag start
ok 1018 - widget mousedown reveals the tag start
  ---
  duration_ms: 0.432857
  ...
# Subtest: TR vectors verbatim: rendered views annotate eligible anchors in place
ok 1019 - TR vectors verbatim: rendered views annotate eligible anchors in place
  ---
  duration_ms: 1.292448
  ...
# Subtest: TR9 toggle strips document-wide and re-annotates on enable
ok 1020 - TR9 toggle strips document-wide and re-annotates on enable
  ---
  duration_ms: 0.918413
  ...
# Subtest: annotate and strip helpers are idempotent and defensive
ok 1021 - annotate and strip helpers are idempotent and defensive
  ---
  duration_ms: 0.399793
  ...
# Subtest: session toggle and onload wiring
ok 1022 - session toggle and onload wiring
  ---
  duration_ms: 3.735645
  ...
# Subtest: styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
ok 1023 - styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
  ---
  duration_ms: 0.826258
  ...
# Subtest: TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
ok 1024 - TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
  ---
  duration_ms: 0.341572
  ...
# Subtest: Live Preview ref decorations replace the whole pair and reveal both tags at once
ok 1025 - Live Preview ref decorations replace the whole pair and reveal both tags at once
  ---
  duration_ms: 0.334539
  ...
# Subtest: ref element structure: book classes, reference label, and tooltip
ok 1026 - ref element structure: book classes, reference label, and tooltip
  ---
  duration_ms: 0.125349
  ...
# Subtest: TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
ok 1027 - TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
  ---
  duration_ms: 0.567213
  ...
# Subtest: TR11 verbatim: \#task \#references and reversed order keep the hash only
ok 1028 - TR11 verbatim: \#task \#references and reversed order keep the hash only
  ---
  duration_ms: 0.290325
  ...
# Subtest: TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
ok 1029 - TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
  ---
  duration_ms: 0.148724
  ...
# Subtest: TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
ok 1030 - TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
  ---
  duration_ms: 0.496228
  ...
# Subtest: styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
ok 1031 - styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
  ---
  duration_ms: 0.654501
  ...
# Subtest: section info null stays neutral (TM19)
ok 1032 - section info null stays neutral (TM19)
  ---
  duration_ms: 2.040628
  ...
# Subtest: data-line mapping stamps and marks an exact Today row
ok 1033 - data-line mapping stamps and marks an exact Today row
  ---
  duration_ms: 2.731207
  ...
# Subtest: data-line mapping rejects a status mismatch
ok 1034 - data-line mapping rejects a status mismatch
  ---
  duration_ms: 0.308319
  ...
# Subtest: row-index fallback maps when counts agree and refuses when they disagree
ok 1035 - row-index fallback maps when counts agree and refuses when they disagree
  ---
  duration_ms: 1.269043
  ...
# Subtest: Tasks result rows and code are skipped
ok 1036 - Tasks result rows and code are skipped
  ---
  duration_ms: 0.417237
  ...
# Subtest: a daily-note sourcePath is skipped
ok 1037 - a daily-note sourcePath is skipped
  ---
  duration_ms: 0.191666
  ...
# Subtest: duplicate ids stay neutral
ok 1038 - duplicate ids stay neutral
  ---
  duration_ms: 0.46603
  ...
# Subtest: insertion points: \#task anchor, \#ref pair, checkbox, whitespace split
ok 1039 - insertion points: \#task anchor, \#ref pair, checkbox, whitespace split
  ---
  duration_ms: 1.189572
  ...
# Subtest: identity-proven non-Today rows are stamped without a mark
ok 1040 - identity-proven non-Today rows are stamped without a mark
  ---
  duration_ms: 0.519893
  ...
# Subtest: sweep adds on link, removes on unlink or completion, updates tooltip, respects toggle, skips daily ancestors
ok 1041 - sweep adds on link, removes on unlink or completion, updates tooltip, respects toggle, skips daily ancestors
  ---
  duration_ms: 1.435922
  ...
# Subtest: daily-view class is set on open daily leaves and cleared on switch
ok 1042 - daily-view class is set on open daily leaves and cleared on switch
  ---
  duration_ms: 0.320492
  ...
# Subtest: delegated Mod+click jumps; plain click does not
ok 1043 - delegated Mod+click jumps; plain click does not
  ---
  duration_ms: 1.081065
  ...
# Subtest: setupTodayMarks registers the reading post-processor at order 60
ok 1044 - setupTodayMarks registers the reading post-processor at order 60
  ---
  duration_ms: 0.304281
  ...
# Subtest: styles.css daily-view suppression is present
ok 1045 - styles.css daily-view suppression is present
  ---
  duration_ms: 0.524241
  ...
# Subtest: Live Preview marks do not double-jump in Reading view
ok 1046 - Live Preview marks do not double-jump in Reading view
  ---
  duration_ms: 0.350549
  ...
# Subtest: mid-body \#task goes at the body start
ok 1047 - mid-body \#task goes at the body start
  ---
  duration_ms: 0.457654
  ...
# Subtest: \#task inside inline code stays neutral
ok 1048 - \#task inside inline code stays neutral
  ---
  duration_ms: 0.221493
  ...
# Subtest: re-render with a new path refreshes the mark key
ok 1049 - re-render with a new path refreshes the mark key
  ---
  duration_ms: 0.298189
  ...
# Subtest: one duplicate scan per render
ok 1050 - one duplicate scan per render
  ---
  duration_ms: 0.51835
  ...
# Subtest: row-index fallback uses every list item
ok 1051 - row-index fallback uses every list item
  ---
  duration_ms: 0.449499
  ...
# Subtest: open statuses are exactly space, star, slash, and question
ok 1052 - open statuses are exactly space, star, slash, and question
  ---
  duration_ms: 1.525434
  ...
# Subtest: trailing-id rules: leading space, trailing-only, valid charset
ok 1053 - trailing-id rules: leading space, trailing-only, valid charset
  ---
  duration_ms: 0.31401
  ...
# Subtest: candidate: TM9 closed stays null, TM10 open statuses pass
ok 1054 - candidate: TM9 closed stays null, TM10 open statuses pass
  ---
  duration_ms: 1.111383
  ...
# Subtest: candidate: TM11 needs an exact \#task tag and a trailing id
ok 1055 - candidate: TM11 needs an exact \#task tag and a trailing id
  ---
  duration_ms: 0.232154
  ...
# Subtest: candidate: TM21 code is left for the call-site code check
ok 1056 - candidate: TM21 code is left for the call-site code check
  ---
  duration_ms: 0.243154
  ...
# Subtest: insert offset: \#task first lands before the title
ok 1057 - insert offset: \#task first lands before the title
  ---
  duration_ms: 0.194933
  ...
# Subtest: insert offset: TM16 \#task \#ref spans the pair, \#prj sits between
ok 1058 - insert offset: TM16 \#task \#ref spans the pair, \#prj sits between
  ---
  duration_ms: 0.238445
  ...
# Subtest: insert offset: mid-body \#task falls back to the body start
ok 1059 - insert offset: mid-body \#task falls back to the body start
  ---
  duration_ms: 0.132693
  ...
# Subtest: insert offset: blockquote, spaces, numbered, empty title, emoji
ok 1060 - insert offset: blockquote, spaces, numbered, empty title, emoji
  ---
  duration_ms: 0.454167
  ...
# Subtest: duplicates: TM15 marks neither line
ok 1061 - duplicates: TM15 marks neither line
  ---
  duration_ms: 0.551483
  ...
# Subtest: session text: named, home label, range-only, unnamed
ok 1062 - session text: named, home label, range-only, unnamed
  ---
  duration_ms: 0.344879
  ...
# Subtest: tooltip: TM1 running, TM2 queued, and the platform variants
ok 1063 - tooltip: TM1 running, TM2 queued, and the platform variants
  ---
  duration_ms: 0.246821
  ...
# Subtest: tooltip: running wins as primary with a +N more suffix
ok 1064 - tooltip: running wins as primary with a +N more suffix
  ---
  duration_ms: 0.150106
  ...
# Subtest: tooltip: empty input yields Today and output never has ::
ok 1065 - tooltip: empty input yields Today and output never has ::
  ---
  duration_ms: 0.20958
  ...
# Subtest: entering window: 600 ms after join, never before or at load
ok 1066 - entering window: 600 ms after join, never before or at load
  ---
  duration_ms: 0.113647
  ...
# Subtest: modifier: primary button with meta on mac, ctrl elsewhere
ok 1067 - modifier: primary button with meta on mac, ctrl elsewhere
  ---
  duration_ms: 0.13574
  ...
# Subtest: element: empty span with tooltip attributes and no listeners
ok 1068 - element: empty span with tooltip attributes and no listeners
  ---
  duration_ms: 0.273332
  ...
# Subtest: widget: eq ignores entering and the callback
ok 1069 - widget: eq ignores entering and the callback
  ---
  duration_ms: 0.212886
  ...
# Subtest: widget: plain mousedown moves the cursor, Mod mousedown jumps
ok 1070 - widget: plain mousedown moves the cursor, Mod mousedown jumps
  ---
  duration_ms: 0.473595
  ...
# Subtest: refresh effect is lazy and stable
ok 1071 - refresh effect is lazy and stable
  ---
  duration_ms: 0.113617
  ...
# Subtest: styles.css implements the glyph anatomy contract
ok 1072 - styles.css implements the glyph anatomy contract
  ---
  duration_ms: 0.578505
  ...
# Subtest: Live Preview applies the TM1-TM22 line, cache, and refresh vectors
ok 1073 - Live Preview applies the TM1-TM22 line, cache, and refresh vectors
  ---
  duration_ms: 20.200751
  ...
# Subtest: Today mark lifecycle registers the toggle, keyboard command, and reading processor
ok 1074 - Today mark lifecycle registers the toggle, keyboard command, and reading processor
  ---
  duration_ms: 10.948731
  ...
# Subtest: keyboard jump uses the task under the cursor and reports non-membership
ok 1075 - keyboard jump uses the task under the cursor and reports non-membership
  ---
  duration_ms: 18.492151
  ...
# Subtest: Mod-click and keyboard jumps land on the current running Task Link
ok 1076 - Mod-click and keyboard jumps land on the current running Task Link
  ---
  duration_ms: 12.318885
  ...
# Subtest: reduced motion stops the entrance pop
ok 1077 - reduced motion stops the entrance pop
  ---
  duration_ms: 0.68046
  ...
# Subtest: tooltips never contain ::
ok 1078 - tooltips never contain ::
  ---
  duration_ms: 0.142271
  ...
# Subtest: todayMarkPosInInlineCode: single, double, unmatched, positions
ok 1079 - todayMarkPosInInlineCode: single, double, unmatched, positions
  ---
  duration_ms: 0.271038
  ...
# Subtest: builder gates on Today ids without touching doc lines
ok 1080 - builder gates on Today ids without touching doc lines
  ---
  duration_ms: 10.166618
  ...
# Subtest: two rebuilds on the same doc compute duplicates once
ok 1081 - two rebuilds on the same doc compute duplicates once
  ---
  duration_ms: 17.470177
  ...
# Subtest: todayMarksNow override drives readiness
ok 1082 - todayMarksNow override drives readiness
  ---
  duration_ms: 11.768165
  ...
# Subtest: refresh dispatches only to non-daily leaves and uses 16 ms
ok 1083 - refresh dispatches only to non-daily leaves and uses 16 ms
  ---
  duration_ms: 17.004989
  ...
# Subtest: keyboard command gates closed status and daily notes
ok 1084 - keyboard command gates closed status and daily notes
  ---
  duration_ms: 10.05421
  ...
# Subtest: TM14 rollover: day N+1 shows no decoration
ok 1085 - TM14 rollover: day N+1 shows no decoration
  ---
  duration_ms: 10.111473
  ...
# Subtest: TM17 widget sits at line.from + insertCh with side -1
ok 1086 - TM17 widget sits at line.from + insertCh with side -1
  ---
  duration_ms: 17.789889
  ...
# Subtest: TM18 entering: new key pops then settles
ok 1087 - TM18 entering: new key pops then settles
  ---
  duration_ms: 18.653756
  ...
# Subtest: TM20 toggle flips class, notice, and refreshes non-daily leaves
ok 1088 - TM20 toggle flips class, notice, and refreshes non-daily leaves
  ---
  duration_ms: 16.132213
  ...
# Subtest: rebuild triggers: doc, viewport, LP field, file switch rebuild; selection alone does not
ok 1089 - rebuild triggers: doc, viewport, LP field, file switch rebuild; selection alone does not
  ---
  duration_ms: 9.416102
  ...
# Subtest: jump guards in-flight, prefers cached ledgerLine over later match
ok 1090 - jump guards in-flight, prefers cached ledgerLine over later match
  ---
  duration_ms: 9.642557
  ...
# Subtest: jump with no open daily leaf attempts the daily open
ok 1091 - jump with no open daily leaf attempts the daily open
  ---
  duration_ms: 13.867256
  ...
# Subtest: home labels: unnamed timed entry uses derived label and 1-based entryLine
ok 1092 - home labels: unnamed timed entry uses derived label and 1-based entryLine
  ---
  duration_ms: 16.937497
  ...
# Subtest: T1 GTD: empty target resolves to the daily note
ok 1093 - T1 GTD: empty target resolves to the daily note
  ---
  duration_ms: 2.661183
  ...
# Subtest: T2 markers: pomodoro mark counts, struck drops, embed counts
ok 1094 - T2 markers: pomodoro mark counts, struck drops, embed counts
  ---
  duration_ms: 0.555301
  ...
# Subtest: T3 closed entries: links under completed/cancelled entries drop
ok 1095 - T3 closed entries: links under completed/cancelled entries drop
  ---
  duration_ms: 0.181567
  ...
# Subtest: T4 shapes: mixed text and deeper descendants drop
ok 1096 - T4 shapes: mixed text and deeper descendants drop
  ---
  duration_ms: 0.263774
  ...
# Subtest: T5 dedupe: same task twice keeps the first position
ok 1097 - T5 dedupe: same task twice keeps the first position
  ---
  duration_ms: 0.311235
  ...
# Subtest: T6 fenced: links inside fenced blocks drop
ok 1098 - T6 fenced: links inside fenced blocks drop
  ---
  duration_ms: 0.24634
  ...
# Subtest: T7 status: the link layer lists every dedicated link
ok 1099 - T7 status: the link layer lists every dedicated link
  ---
  duration_ms: 0.470288
  ...
# Subtest: T8 unresolved: missing notes give no key
ok 1100 - T8 unresolved: missing notes give no key
  ---
  duration_ms: 0.309041
  ...
# Subtest: T9 alias: aliased links count under their target
ok 1101 - T9 alias: aliased links count under their target
  ---
  duration_ms: 0.409963
  ...
# Subtest: laneBudgetFromTasks counts the whole Next lane, Today included
ok 1102 - laneBudgetFromTasks counts the whole Next lane, Today included
  ---
  duration_ms: 1.151609
  ...
# Subtest: laneBudgetFromTasks counts Pending by type and flags over-cap
ok 1103 - laneBudgetFromTasks counts Pending by type and flags over-cap
  ---
  duration_ms: 0.334739
  ...
# Subtest: lane caps come from max_next/max_pending; legacy max_now is ignored
ok 1104 - lane caps come from max_next/max_pending; legacy max_now is ignored
  ---
  duration_ms: 0.158462
  ...
# Subtest: reload event name matches the Tasks bundle subscription
ok 1105 - reload event name matches the Tasks bundle subscription
  ---
  duration_ms: 0.126571
  ...
# Subtest: api v2 shape: Today and lane budgets, no nowBudget
ok 1106 - api v2 shape: Today and lane budgets, no nowBudget
  ---
  duration_ms: 4.008587
  ...
# Subtest: cache rebuild answers isToday/todayRank in ledger order
ok 1107 - cache rebuild answers isToday/todayRank in ledger order
  ---
  duration_ms: 1.974791
  ...
# Subtest: refresh fires only when the key set changes
ok 1108 - refresh fires only when the key set changes
  ---
  duration_ms: 0.948141
  ...
# Subtest: unready to ready with empty TODAY still refreshes open badges
ok 1109 - unready to ready with empty TODAY still refreshes open badges
  ---
  duration_ms: 0.886442
  ...
# Subtest: cache rebuilds on the daily changed event with the event content
ok 1110 - cache rebuilds on the daily changed event with the event content
  ---
  duration_ms: 0.699826
  ...
# Subtest: cache rebuilds once on resolved and at midnight rollover
ok 1111 - cache rebuilds once on resolved and at midnight rollover
  ---
  duration_ms: 1.049224
  ...
# Subtest: computeTodayLinks records entry range and placeholder
ok 1112 - computeTodayLinks records entry range and placeholder
  ---
  duration_ms: 0.292348
  ...
# Subtest: todayOpenEntries and todayRunningEntryLine follow the unique timed rule
ok 1113 - todayOpenEntries and todayRunningEntryLine follow the unique timed rule
  ---
  duration_ms: 0.34076
  ...
# Subtest: resolveTodayLinkKeys keeps duplicates; resolveTodayKeys is first-occurrence
ok 1114 - resolveTodayLinkKeys keeps duplicates; resolveTodayKeys is first-occurrence
  ---
  duration_ms: 0.181036
  ...
# Subtest: todayLinkDetails: named running, placeholder, unnamed home, unnamed none
ok 1115 - todayLinkDetails: named running, placeholder, unnamed home, unnamed none
  ---
  duration_ms: 0.206093
  ...
# Subtest: todayLinkDetails orders running first and keeps one detail per key+entry
ok 1116 - todayLinkDetails orders running first and keeps one detail per key+entry
  ---
  duration_ms: 0.190624
  ...
# Subtest: todayKeyParts splits at the last hash; idsByPath groups block ids
ok 1117 - todayKeyParts splits at the last hash; idsByPath groups block ids
  ---
  duration_ms: 0.15666
  ...
# Subtest: todayDetailsSignature changes only when details change
ok 1118 - todayDetailsSignature changes only when details change
  ---
  duration_ms: 0.235941
  ...
# Subtest: idsByPath and details accessors follow the rebuilt cache
ok 1119 - idsByPath and details accessors follow the rebuilt cache
  ---
  duration_ms: 0.956126
  ...
# Subtest: details-only change refreshes marks without a Tasks reload
ok 1120 - details-only change refreshes marks without a Tasks reload
  ---
  duration_ms: 0.761594
  ...
# Subtest: entered stamps only when the cache was already ready, then prune
ok 1121 - entered stamps only when the cache was already ready, then prune
  ---
  duration_ms: 1.330982
  ...
# Subtest: generation guard: reverse-order async reads keep the newer
ok 1122 - generation guard: reverse-order async reads keep the newer
  ---
  duration_ms: 0.804336
  ...
# Subtest: generation guard: a sync rebuild wins over an in-flight async read
ok 1123 - generation guard: a sync rebuild wins over an in-flight async read
  ---
  duration_ms: 0.545092
  ...
# Subtest: revalidateTodayCache is throttled and refreshes when not ready
ok 1124 - revalidateTodayCache is throttled and refreshes when not ready
  ---
  duration_ms: 0.546544
  ...
# Subtest: revalidateTodayCache respects layoutReady and backwards clock steps
ok 1125 - revalidateTodayCache respects layoutReady and backwards clock steps
  ---
  duration_ms: 0.415293
  ...
# Subtest: a done-today prerequisite shows the glyph
ok 1126 - a done-today prerequisite shows the glyph
  ---
  duration_ms: 3.926039
  ...
# Subtest: done yesterday does not show the glyph
ok 1127 - done yesterday does not show the glyph
  ---
  duration_ms: 0.398661
  ...
# Subtest: a struck link does not show the glyph
ok 1128 - a struck link does not show the glyph
  ---
  duration_ms: 0.294873
  ...
# Subtest: a closed entry does not show the glyph
ok 1129 - a closed entry does not show the glyph
  ---
  duration_ms: 0.277039
  ...
# Subtest: several prerequisites give +N
ok 1130 - several prerequisites give +N
  ---
  duration_ms: 0.477852
  ...
# Subtest: the model refuses every non-glyph shape
ok 1131 - the model refuses every non-glyph shape
  ---
  duration_ms: 0.786813
  ...
# Subtest: unblockedGlyphDoneToday needs DONE plus a today done date
ok 1132 - unblockedGlyphDoneToday needs DONE plus a today done date
  ---
  duration_ms: 0.26179
  ...
# Subtest: tooltip names one prerequisite and counts several
ok 1133 - tooltip names one prerequisite and counts several
  ---
  duration_ms: 0.309761
  ...
# Subtest: Live Preview places one glyph after each unblocked link
not ok 1134 - Live Preview places one glyph after each unblocked link
  ---
  duration_ms: 1.92658
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
ok 1135 - Live Preview draws nothing without a warm cache or a live link
  ---
  duration_ms: 0.95288
  ...
# Subtest: widget mousedown places the cursor past the link
not ok 1136 - widget mousedown places the cursor past the link
  ---
  duration_ms: 0.473655
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
not ok 1137 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 0.518901
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
not ok 1138 - Reading view glyphs unblocked rows and dedupes
  ---
  duration_ms: 1.667515
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
ok 1139 - Reading view refuses every non-glyph row
  ---
  duration_ms: 1.477662
  ...
# Subtest: api.unblockedGlyph v1 is additive, sync, and never throwing
ok 1140 - api.unblockedGlyph v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.516277
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 1141 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 0.915429
  ...
# Subtest: changed-file and rollover refreshes
ok 1142 - changed-file and rollover refreshes
  ---
  duration_ms: 0.270957
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 1143 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.090653
  ...
# Subtest: styles.css contract: faint glyph, Done token, toggle
ok 1144 - styles.css contract: faint glyph, Done token, toggle
  ---
  duration_ms: 0.563747
  ...
# Subtest: Ledger Vim mappings restore \\p and retain the other normal-mode actions
ok 1145 - Ledger Vim mappings restore \\p and retain the other normal-mode actions
  ---
  duration_ms: 2.388442
  ...
# Subtest: workBadgeTone boundary vectors at cap 100 use exact comparisons
ok 1146 - workBadgeTone boundary vectors at cap 100 use exact comparisons
  ---
  duration_ms: 1.03695
  ...
# Subtest: workBadgeTone at cap 15 has no percentage rounding
ok 1147 - workBadgeTone at cap 15 has no percentage rounding
  ---
  duration_ms: 0.17847
  ...
# Subtest: workBadgeTone default caps, small caps, and cap changes
ok 1148 - workBadgeTone default caps, small caps, and cap changes
  ---
  duration_ms: 0.152301
  ...
# Subtest: workBadgeTone never coerces invalid input to zero
ok 1149 - workBadgeTone never coerces invalid input to zero
  ---
  duration_ms: 0.982115
  ...
# Subtest: TODAY links bands with themes at cap 3
ok 1150 - TODAY links bands with themes at cap 3
  ---
  duration_ms: 0.301035
  ...
# Subtest: TODAY theme overflow forces red, exact cap does not
ok 1151 - TODAY theme overflow forces red, exact cap does not
  ---
  duration_ms: 0.196866
  ...
# Subtest: TODAY unavailable stays neutral, empty section is grey
ok 1152 - TODAY unavailable stays neutral, empty section is grey
  ---
  duration_ms: 1.097487
  ...
# Subtest: PENDING/NEXT models color the section, READY its gated count
ok 1153 - PENDING/NEXT models color the section, READY its gated count
  ---
  duration_ms: 0.503201
  ...
# Subtest: READY uses its gated count even when the total lane is larger
ok 1154 - READY uses its gated count even when the total lane is larger
  ---
  duration_ms: 0.358184
  ...
# Subtest: cap equality still emits no cap lint
ok 1155 - cap equality still emits no cap lint
  ---
  duration_ms: 2.478173
  ...
# Subtest: lane DOM keeps exactly one tone through transitions and unavailability
ok 1156 - lane DOM keeps exactly one tone through transitions and unavailability
  ---
  duration_ms: 7.447832
  ...
# Subtest: READY DOM keeps exactly one tone and daily/dashboard models agree
ok 1157 - READY DOM keeps exactly one tone and daily/dashboard models agree
  ---
  duration_ms: 1.148053
  ...
# SKIP dashboard integration: BOB_DASHBOARD_FILE is not set
# SKIP dashboard fallback integration: BOB_DASHBOARD_FILE is not set
# SKIP dash CSS contract: BOB_DASHBOARD_FILE is not set
# Subtest: daily TODAY chip uses the theme-overflow tone
ok 1158 - daily TODAY chip uses the theme-overflow tone
  ---
  duration_ms: 17.925528
  ...
# Subtest: dashboard integration uses Work tones, TODAY override, and keeps Work order
ok 1159 - dashboard integration uses Work tones, TODAY override, and keeps Work order
  ---
  duration_ms: 0.730325
  ...
# Subtest: dashboard fallbacks keep Work tones without plugin renderers or colors
ok 1160 - dashboard fallbacks keep Work tones without plugin renderers or colors
  ---
  duration_ms: 0.32937
  ...
# Subtest: Work tone CSS covers each tone and uses the shared magenta value
ok 1161 - Work tone CSS covers each tone and uses the shared magenta value
  ---
  duration_ms: 0.765953
  ...
# Subtest: RBW6 mergeTargetPreparations keeps one write at the strongest lane
ok 1162 - RBW6 mergeTargetPreparations keeps one write at the strongest lane
  ---
  duration_ms: 1.714655
  ...
# Subtest: §15.7 notices use curly quotes and the Ready → Blocked copy
ok 1163 - §15.7 notices use curly quotes and the Ready → Blocked copy
  ---
  duration_ms: 0.369035
  ...
# Subtest: RBP1 same-note add is one transaction and matches forward bytes
ok 1164 - RBP1 same-note add is one transaction and matches forward bytes
  ---
  duration_ms: 16.992222
  ...
# Subtest: RBP2 background-leaf T matches forward bytes
ok 1165 - RBP2 background-leaf T matches forward bytes
  ---
  duration_ms: 5.334999
  ...
# Subtest: RBP3 closed T is written through vault.process and matches forward bytes
ok 1166 - RBP3 closed T is written through vault.process and matches forward bytes
  ---
  duration_ms: 4.226603
  ...
# Subtest: RBP4 ordinary transfer; a ^prj N is never raised
ok 1167 - RBP4 ordinary transfer; a ^prj N is never raised
  ---
  duration_ms: 13.084191
  ...
# Subtest: RBP5 consumed Pomodoro link matches forward bytes
ok 1168 - RBP5 consumed Pomodoro link matches forward bytes
  ---
  duration_ms: 5.303911
  ...
# Subtest: RBP6 project T with residents and a sub-project matches forward bytes
ok 1169 - RBP6 project T with residents and a sub-project matches forward bytes
  ---
  duration_ms: 16.097132
  ...
# Subtest: RBP7 two dependents in different lanes prepare N once at [/]
ok 1170 - RBP7 two dependents in different lanes prepare N once at [/]
  ---
  duration_ms: 8.581931
  ...
# Subtest: RBP8 counted sources N1 and N2 match forward(T + N1, N2)
ok 1171 - RBP8 counted sources N1 and N2 match forward(T + N1, N2)
  ---
  duration_ms: 4.409182
  ...
# Subtest: RBP9 blocks_lines false writes no BLOCKS and still ids N
ok 1172 - RBP9 blocks_lines false writes no BLOCKS and still ids N
  ---
  duration_ms: 1.781784
  ...
# Subtest: RBP10 removing the last reason matches forward removal
ok 1173 - RBP10 removing the last reason matches forward removal
  ---
  duration_ms: 3.699506
  ...
# Subtest: RBW1 a changed source note writes nothing
ok 1174 - RBW1 a changed source note writes nothing
  ---
  duration_ms: 1.55496
  ...
# Subtest: RBW2 one changed T note still lands the others and omits it from BLOCKS
ok 1175 - RBW2 one changed T note still lands the others and omits it from BLOCKS
  ---
  duration_ms: 1.596178
  ...
# Subtest: RBW3 already-present picks write nothing
ok 1176 - RBW3 already-present picks write nothing
  ---
  duration_ms: 1.34049
  ...
# Subtest: RBW4 cleanup runs for T's that committed when N lives in today's daily note
ok 1177 - RBW4 cleanup runs for T's that committed when N lives in today's daily note
  ---
  duration_ms: 2.358273
  ...
# Subtest: RBW6 counted forward two-lane dependents prepare N once
ok 1178 - RBW6 counted forward two-lane dependents prepare N once
  ---
  duration_ms: 7.482641
  ...
# Subtest: A1 N above two T's in one note matches forward (open and closed note)
ok 1179 - A1 N above two T's in one note matches forward (open and closed note)
  ---
  duration_ms: 17.114459
  ...
# Subtest: A1 N below two T's matches forward bytes
ok 1180 - A1 N below two T's matches forward bytes
  ---
  duration_ms: 5.078731
  ...
# Subtest: A2 forward stamps the dependent when a prerequisite above gains BLOCKS
ok 1181 - A2 forward stamps the dependent when a prerequisite above gains BLOCKS
  ---
  duration_ms: 0.872977
  ...
# Subtest: A1 mixed same-note and cross-note picks keep N's lane rise (RBP7 variant)
ok 1182 - A1 mixed same-note and cross-note picks keep N's lane rise (RBP7 variant)
  ---
  duration_ms: 2.447644
  ...
# Subtest: A1 RBP1 with N truly lacking ^id is prompted an id and matches forward
ok 1183 - A1 RBP1 with N truly lacking ^id is prompted an id and matches forward
  ---
  duration_ms: 1.716318
  ...
# Subtest: A1 N lacking ^id in a closed note above T keeps its BLOCKS line under N
ok 1184 - A1 N lacking ^id in a closed note above T keeps its BLOCKS line under N
  ---
  duration_ms: 1.309651
  ...
# Subtest: A3 mirror lists the committed T's by identity (N above T1, X, T2)
ok 1185 - A3 mirror lists the committed T's by identity (N above T1, X, T2)
  ---
  duration_ms: 1.46636
  ...
# Subtest: A4 notices name T, not N (add, remove, project, counted)
ok 1186 - A4 notices name T, not N (add, remove, project, counted)
  ---
  duration_ms: 5.206745
  ...
# Subtest: A5 the writer's stale notice is returned once and never shown by the writer
ok 1187 - A5 the writer's stale notice is returned once and never shown by the writer
  ---
  duration_ms: 0.28819
  ...
# Subtest: A6 a changed T row (rawLine) is refused before any write
ok 1188 - A6 a changed T row (rawLine) is refused before any write
  ---
  duration_ms: 0.22024
  ...
# Subtest: A7 RBW2 keeps the failed T's Pomodoro link and consumes the committed one
ok 1189 - A7 RBW2 keeps the failed T's Pomodoro link and consumes the committed one
  ---
  duration_ms: 1.739382
  ...
# Subtest: A8 closed-note T guards run when the gesture is applied
ok 1190 - A8 closed-note T guards run when the gesture is applied
  ---
  duration_ms: 3.226943
  ...
# Subtest: A9 a ^prj T's residents recover with [unblocked::] when N lives in a daily note
ok 1191 - A9 a ^prj T's residents recover with [unblocked::] when N lives in a daily note
  ---
  duration_ms: 12.664819
  ...
# Subtest: A5 a preparation no write can carry fails the plan instead of being dropped
ok 1192 - A5 a preparation no write can carry fails the plan instead of being dropped
  ---
  duration_ms: 0.992486
  ...
# Subtest: applyDependencyEdit adding a first cross-note prerequisite keeps the dependent's cursor
ok 1193 - applyDependencyEdit adding a first cross-note prerequisite keeps the dependent's cursor
  ---
  duration_ms: 1.736576
  ...
# Subtest: applyBlocksEdit giving a source its first BLOCKS line keeps the source's cursor
ok 1194 - applyBlocksEdit giving a source its first BLOCKS line keeps the source's cursor
  ---
  duration_ms: 4.751384
  ...
# Subtest: nav BK1–BK2 accept canonical BLOCKS lines
ok 1195 - nav BK1–BK2 accept canonical BLOCKS lines
  ---
  duration_ms: 2.815187
  ...
# Subtest: nav BK3–BK11 canonicalise
ok 1196 - nav BK3–BK11 canonicalise
  ---
  duration_ms: 0.698183
  ...
# Subtest: nav BK12 empty, BK13–BK15 malformed
ok 1197 - nav BK12 empty, BK13–BK15 malformed
  ---
  duration_ms: 0.239548
  ...
# Subtest: nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse
ok 1198 - nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse
  ---
  duration_ms: 0.41355
  ...
# Subtest: nav BK21 code-point sort and writer format
ok 1199 - nav BK21 code-point sort and writer format
  ---
  duration_ms: 0.342174
  ...
# Subtest: nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS
ok 1200 - nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS
  ---
  duration_ms: 0.553748
  ...
# Subtest: nav BW18 conversion drops BLOCKS like Sub-projects
ok 1201 - nav BW18 conversion drops BLOCKS like Sub-projects
  ---
  duration_ms: 1.174975
  ...
# Subtest: nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner
ok 1202 - nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner
  ---
  duration_ms: 0.885
  ...
# Subtest: nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists
ok 1203 - nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists
  ---
  duration_ms: 1.970544
  ...
# Subtest: nav MC1/MC2 deferred Pomodoro cleanup skips managed lines
ok 1204 - nav MC1/MC2 deferred Pomodoro cleanup skips managed lines
  ---
  duration_ms: 0.532697
  ...
# Subtest: showBlocksStage opens from a task with reverse CURRENT and RESULTS
ok 1205 - showBlocksStage opens from a task with reverse CURRENT and RESULTS
  ---
  duration_ms: 13.632038
  ...
# Subtest: showBlocksStage opens from a counted session
ok 1206 - showBlocksStage opens from a counted session
  ---
  duration_ms: 1.913694
  ...
# Subtest: showBlocksStage opens on a Task Link target note
ok 1207 - showBlocksStage opens on a Task Link target note
  ---
  duration_ms: 1.284142
  ...
# Subtest: RBU1 empty query uses today-first then In Progress, Next, same-note, rest
ok 1208 - RBU1 empty query uses today-first then In Progress, Next, same-note, rest
  ---
  duration_ms: 1.578144
  ...
# Subtest: RBU2 today-linked rows carry 🍅 running and strip names the entry
ok 1209 - RBU2 today-linked rows carry 🍅 running and strip names the entry
  ---
  duration_ms: 0.975573
  ...
# Subtest: RBU3 CURRENT 🔑 only when N is the last reason
ok 1210 - RBU3 CURRENT 🔑 only when N is the last reason
  ---
  duration_ms: 1.856736
  ...
# Subtest: RBU4 footer verbs are block, remove, and apply N
ok 1211 - RBU4 footer verbs are block, remove, and apply N
  ---
  duration_ms: 1.590779
  ...
# Subtest: RBU5 subtitle at rest, with marks, and names this task first
ok 1212 - RBU5 subtitle at rest, with marks, and names this task first
  ---
  duration_ms: 1.446483
  ...
# Subtest: RBG1 N itself is excluded from RESULTS
ok 1213 - RBG1 N itself is excluded from RESULTS
  ---
  duration_ms: 0.918594
  ...
# Subtest: RBG2 a cycle disables the row with path tooltip copy
ok 1214 - RBG2 a cycle disables the row with path tooltip copy
  ---
  duration_ms: 0.948211
  ...
# Subtest: RBG3 ^prj T with N inside the project is inside this project
ok 1215 - RBG3 ^prj T with N inside the project is inside this project
  ---
  duration_ms: 1.902413
  ...
# Subtest: RBG3 descendant N disables the parent project as a sub-project
ok 1216 - RBG3 descendant N disables the parent project as a sub-project
  ---
  duration_ms: 1.542496
  ...
# Subtest: RBG4 a malformed or second Depends-On line is guarded
ok 1217 - RBG4 a malformed or second Depends-On line is guarded
  ---
  duration_ms: 0.928543
  ...
# Subtest: RBG5 stale refuse reopens in the Blocks direction
ok 1218 - RBG5 stale refuse reopens in the Blocks direction
  ---
  duration_ms: 2.068922
  ...
# Subtest: RBG5 for T: a T changed after stage open refuses once and writes nothing
ok 1219 - RBG5 for T: a T changed after stage open refuses once and writes nothing
  ---
  duration_ms: 2.322586
  ...
# Subtest: today's links survive a pool refresh that lands while the daily note loads
ok 1220 - today's links survive a pool refresh that lands while the daily note loads
  ---
  duration_ms: 32.596756
  ...
# Subtest: RBG8 Esc from the stage or the block-ID prompt writes nothing
ok 1221 - RBG8 Esc from the stage or the block-ID prompt writes nothing
  ---
  duration_ms: 2.149375
  ...
# Subtest: missing source ^id opens the block-ID prompt and Esc allocates none
ok 1222 - missing source ^id opens the block-ID prompt and Esc allocates none
  ---
  duration_ms: 1.023695
  ...
# Subtest: RBP11 inbox route runs first then the Blocks write
ok 1223 - RBP11 inbox route runs first then the Blocks write
  ---
  duration_ms: 0.745033
  ...
# Subtest: RBW5 review walk stays unless the commit takes N out of today's walk
ok 1224 - RBW5 review walk stays unless the commit takes N out of today's walk
  ---
  duration_ms: 6.773157
  ...
# Subtest: marks commit add and remove together; counted uses k/n block
ok 1225 - marks commit add and remove together; counted uses k/n block
  ---
  duration_ms: 2.580809
  ...
# Subtest: strip text covers RESULTS, BLOCKED, CURRENT, disabled, marks, and ^prj
ok 1226 - strip text covers RESULTS, BLOCKED, CURRENT, disabled, marks, and ^prj
  ---
  duration_ms: 0.390536
  ...
# Subtest: counted subtitle drops the ⇥ hint because marks are off in counted sessions
ok 1227 - counted subtitle drops the ⇥ hint because marks are off in counted sessions
  ---
  duration_ms: 0.89491
  ...
# Subtest: 🔑 tooltip and 🍅 tooltip render on badges
ok 1228 - 🔑 tooltip and 🍅 tooltip render on badges
  ---
  duration_ms: 1.00536
  ...
# Subtest: Tab marks Blocks CURRENT rows and Enter removes both dependents
ok 1229 - Tab marks Blocks CURRENT rows and Enter removes both dependents
  ---
  duration_ms: 14.296564
  ...
# Subtest: SB1-SB9 dependent IDs match the successor mint vectors
ok 1230 - SB1-SB9 dependent IDs match the successor mint vectors
  ---
  duration_ms: 2.390986
  ...
# Subtest: BW1 same-note add mints and writes BLOCKS in the dependent's single transaction
ok 1231 - BW1 same-note add mints and writes BLOCKS in the dependent's single transaction
  ---
  duration_ms: 12.051739
  ...
# Subtest: BW2 cross-note add follows the dependent commit and writes the target note
ok 1232 - BW2 cross-note add follows the dependent commit and writes the target note
  ---
  duration_ms: 3.682473
  ...
# Subtest: BW4 cross-note target preparation precedes the reverse-line preimage
ok 1233 - BW4 cross-note target preparation precedes the reverse-line preimage
  ---
  duration_ms: 2.858469
  ...
# Subtest: BW3 stale cross-note preimage leaves the forward write standing and shows the suffix
ok 1234 - BW3 stale cross-note preimage leaves the forward write standing and shows the suffix
  ---
  duration_ms: 1.584276
  ...
# Subtest: BW5 removal deletes the reverse line when its last dependent leaves
ok 1235 - BW5 removal deletes the reverse line when its last dependent leaves
  ---
  duration_ms: 3.231071
  ...
# Subtest: BW6 an already mirrored edge is a byte-identical no-op
ok 1236 - BW6 an already mirrored edge is a byte-identical no-op
  ---
  duration_ms: 0.695508
  ...
# Subtest: BW7 closed owners stay frozen
ok 1237 - BW7 closed owners stay frozen
  ---
  duration_ms: 1.64415
  ...
# Subtest: BW8 malformed reverse lines stay untouched and report the failed mirror
ok 1238 - BW8 malformed reverse lines stay untouched and report the failed mirror
  ---
  duration_ms: 1.382881
  ...
# Subtest: BW15 config defaults on, honors false, and invalid values fall back on
ok 1239 - BW15 config defaults on, honors false, and invalid values fall back on
  ---
  duration_ms: 0.614373
  ...
# Subtest: BW17 planner output follows BK21 Unicode code-point ordering
ok 1240 - BW17 planner output follows BK21 Unicode code-point ordering
  ---
  duration_ms: 0.388211
  ...
# Subtest: duplicate BLOCKS children merge their known dependents and preserve CRLF
ok 1241 - duplicate BLOCKS children merge their known dependents and preserve CRLF
  ---
  duration_ms: 0.46087
  ...
# Subtest: BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270)
ok 1242 - BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270)
  ---
  duration_ms: 2.827138
  ...
# Subtest: counted remove-from-all drops every dependent from the same-note BLOCKS line (420)
ok 1243 - counted remove-from-all drops every dependent from the same-note BLOCKS line (420)
  ---
  duration_ms: 1.138774
  ...
# Subtest: vault counted add composes cross-note follow-ups for every source (420)
ok 1244 - vault counted add composes cross-note follow-ups for every source (420)
  ---
  duration_ms: 0.689587
  ...
# Subtest: marked batch add writes every same-note target onto BLOCKS in one plan (430)
ok 1245 - marked batch add writes every same-note target onto BLOCKS in one plan (430)
  ---
  duration_ms: 0.47621
  ...
# Subtest: counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600)
ok 1246 - counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600)
  ---
  duration_ms: 6.510334
  ...
# Subtest: BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves
ok 1247 - BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves
  ---
  duration_ms: 2.990903
  ...
# Subtest: BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS
ok 1248 - BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS
  ---
  duration_ms: 2.856456
  ...
# Subtest: hand-edit clear path routes through the BLOCKS seam (600)
ok 1249 - hand-edit clear path routes through the BLOCKS seam (600)
  ---
  duration_ms: 0.695568
  ...
# Subtest: BW18 conversion never copies a BLOCKS line as a user child
ok 1250 - BW18 conversion never copies a BLOCKS line as a user child
  ---
  duration_ms: 0.732078
  ...
# Subtest: BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it
ok 1251 - BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it
  ---
  duration_ms: 4.159575
  ...
# Subtest: review checklist group helpers format exact completion and close notices
ok 1252 - review checklist group helpers format exact completion and close notices
  ---
  duration_ms: 2.47622
  ...
# Subtest: claim declines without a current exact PRE/POST walk landing
ok 1253 - claim declines without a current exact PRE/POST walk landing
  ---
  duration_ms: 7.061387
  ...
# Subtest: a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
ok 1254 - a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
  ---
  duration_ms: 2.800979
  ...
# Subtest: checklist Ctrl+Enter holds its landing through the actual successor picker
ok 1255 - checklist Ctrl+Enter holds its landing through the actual successor picker
  ---
  duration_ms: 10.976673
  ...
# Subtest: seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
ok 1256 - seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
  ---
  duration_ms: 18.172109
  ...
# Subtest: a landed [?] checklist chore is claimed and completed
ok 1257 - a landed [?] checklist chore is claimed and completed
  ---
  duration_ms: 1.162881
  ...
# Subtest: ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
ok 1258 - ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
  ---
  duration_ms: 2.684637
  ...
# Subtest: live successor filtering skips a stale completed row
ok 1259 - live successor filtering skips a stale completed row
  ---
  duration_ms: 0.73303
  ...
# Subtest: live group filtering reads each cross-note path once
ok 1260 - live group filtering reads each cross-note path once
  ---
  duration_ms: 0.710176
  ...
# Subtest: Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
ok 1261 - Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
  ---
  duration_ms: 3.5452
  ...
# Subtest: POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
ok 1262 - POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
  ---
  duration_ms: 2.202996
  ...
# Subtest: ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
ok 1263 - ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
  ---
  duration_ms: 0.890921
  ...
# Subtest: completion failure preserves cursor and landing and reports the Tasks failure
ok 1264 - completion failure preserves cursor and landing and reports the Tasks failure
  ---
  duration_ms: 0.409923
  ...
# Subtest: reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
ok 1265 - reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
  ---
  duration_ms: 1.495586
  ...
# Subtest: Alt+F on PRE stays with remaining PRE count and never stamps
ok 1266 - Alt+F on PRE stays with remaining PRE count and never stamps
  ---
  duration_ms: 5.567142
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a stale cache
ok 1267 - Ctrl+Alt+F completes seven PRE rows from a stale cache
  ---
  duration_ms: 11.966283
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a refreshed cache
ok 1268 - Ctrl+Alt+F completes seven PRE rows from a refreshed cache
  ---
  duration_ms: 5.924045
  ...
# Subtest: POST stays put with the closing notice
ok 1269 - POST stays put with the closing notice
  ---
  duration_ms: 1.371499
  ...
# Subtest: manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
ok 1270 - manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
  ---
  duration_ms: 1.417027
  ...
# Subtest: manual Ctrl+Enter then ]s from a stale cache uses text-first identity
ok 1271 - manual Ctrl+Enter then ]s from a stale cache uses text-first identity
  ---
  duration_ms: 0.907533
  ...
# Subtest: counted Alt+F skips checklist rows with the skip tail
ok 1272 - counted Alt+F skips checklist rows with the skip tail
  ---
  duration_ms: 3.500266
  ...
# Subtest: missing cycler gate on a PRE row writes nothing
ok 1273 - missing cycler gate on a PRE row writes nothing
  ---
  duration_ms: 0.647026
  ...
# Subtest: missing ledger checklist gate on a tagged line writes nothing
ok 1274 - missing ledger checklist gate on a tagged line writes nothing
  ---
  duration_ms: 0.691301
  ...
# Subtest: a tagged line that is not a queue match falls through to recurring refusal
ok 1275 - a tagged line that is not a queue match falls through to recurring refusal
  ---
  duration_ms: 0.466792
  ...
# Subtest: formatFreshStampChecklistSkipTail names the skipped count
ok 1276 - formatFreshStampChecklistSkipTail names the skipped count
  ---
  duration_ms: 0.155867
  ...
# Subtest: partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
ok 1277 - partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
  ---
  duration_ms: 0.342544
  ...
# Subtest: Task Link Alt+F skips a PRE target with the skip notice
ok 1278 - Task Link Alt+F skips a PRE target with the skip notice
  ---
  duration_ms: 2.548898
  ...
# Subtest: P0 at interval 7 enters P2 with a previewed decay date and kept tail
ok 1279 - P0 at interval 7 enters P2 with a previewed decay date and kept tail
  ---
  duration_ms: 4.110842
  ...
# Subtest: P0 at interval 30 enters P3
ok 1280 - P0 at interval 30 enters P3
  ---
  duration_ms: 0.492952
  ...
# Subtest: fixed enter overrides the interval scan
ok 1281 - fixed enter overrides the interval scan
  ---
  duration_ms: 0.496849
  ...
# Subtest: unknown enter disables Not now without disabling Keep/Reword
ok 1282 - unknown enter disables Not now without disabling Keep/Reword
  ---
  duration_ms: 0.48156
  ...
# Subtest: P0 with no suitable level stays unavailable and never shortens the lease
ok 1283 - P0 with no suitable level stays unavailable and never shortens the lease
  ---
  duration_ms: 0.364396
  ...
# Subtest: custom level order resolves entry in ladder order
ok 1284 - custom level order resolves entry in ladder order
  ---
  duration_ms: 0.304592
  ...
# Subtest: unknown priority value disables Not now only
ok 1285 - unknown priority value disables Not now only
  ---
  duration_ms: 0.37134
  ...
# Subtest: prioritized P2 below its roll limit stays on the same level
ok 1286 - prioritized P2 below its roll limit stays on the same level
  ---
  duration_ms: 0.672825
  ...
# Subtest: P2 at its roll limit decays to P3
ok 1287 - P2 at its roll limit decays to P3
  ---
  duration_ms: 0.800749
  ...
# Subtest: P2 streak derives from the task Schedule Log
ok 1288 - P2 streak derives from the task Schedule Log
  ---
  duration_ms: 2.801611
  ...
# Subtest: configured decay:false keeps rolling past the limit
ok 1289 - configured decay:false keeps rolling past the limit
  ---
  duration_ms: 0.343936
  ...
# Subtest: per-level rolls:0 decays immediately
ok 1290 - per-level rolls:0 decays immediately
  ---
  duration_ms: 0.263964
  ...
# Subtest: terminal cancel substitutes a truthful same-level card roll
ok 1291 - terminal cancel substitutes a truthful same-level card roll
  ---
  duration_ms: 0.315011
  ...
# Subtest: no future date in the window refuses Not now
ok 1292 - no future date in the window refuses Not now
  ---
  duration_ms: 0.195023
  ...
# Subtest: Less often steps 7/14/30 to the next preset with a decision reason
ok 1293 - Less often steps 7/14/30 to the next preset with a decision reason
  ---
  duration_ms: 0.45011
  ...
# Subtest: Less often at 90+ opens the constrained custom picker; 365 is unavailable
ok 1294 - Less often at 90+ opens the constrained custom picker; 365 is unavailable
  ---
  duration_ms: 0.281508
  ...
# Subtest: previewed dates are stable for one random draw
ok 1295 - previewed dates are stable for one random draw
  ---
  duration_ms: 0.260027
  ...
# Subtest: Keep saturates at 999 and Drop preserves keeps history
ok 1296 - Keep saturates at 999 and Drop preserves keeps history
  ---
  duration_ms: 0.317296
  ...
# Subtest: kept tails preserve roll classification; decisions break it deliberately
ok 1297 - kept tails preserve roll classification; decisions break it deliberately
  ---
  duration_ms: 0.859681
  ...
# Subtest: invalid priority config offers no priority-changing action
ok 1298 - invalid priority config offers no priority-changing action
  ---
  duration_ms: 0.201615
  ...
# Subtest: decay off disables Not now but keeps counting
ok 1299 - decay off disables Not now but keeps counting
  ---
  duration_ms: 0.198088
  ...
# Subtest: explicit level picks cover the ladder with previewed rolls
ok 1300 - explicit level picks cover the ladder with previewed rolls
  ---
  duration_ms: 0.735374
  ...
# Subtest: card model is deeply frozen
ok 1301 - card model is deeply frozen
  ---
  duration_ms: 0.181506
  ...
# Subtest: single Alt+F on an at-limit task opens the card and writes nothing
ok 1302 - single Alt+F on an at-limit task opens the card and writes nothing
  ---
  duration_ms: 8.601405
  ...
# Subtest: dismissing the card writes nothing and does not advance
ok 1303 - dismissing the card writes nothing and does not advance
  ---
  duration_ms: 1.123646
  ...
# Subtest: early dates open the card and write nothing
ok 1304 - early dates open the card and write nothing
  ---
  duration_ms: 0.877506
  ...
# Subtest: namespace v5 with decide true stamps counted and opens no card
ok 1305 - namespace v5 with decide true stamps counted and opens no card
  ---
  duration_ms: 4.271749
  ...
# Subtest: stale task-line change writes nothing
ok 1306 - stale task-line change writes nothing
  ---
  duration_ms: 1.41353
  ...
# Subtest: stale local-day change writes nothing
ok 1307 - stale local-day change writes nothing
  ---
  duration_ms: 1.268042
  ...
# Subtest: stale decay-config change writes nothing
ok 1308 - stale decay-config change writes nothing
  ---
  duration_ms: 1.201686
  ...
# Subtest: stale priority-ladder config writes nothing
ok 1309 - stale priority-ladder config writes nothing
  ---
  duration_ms: 1.468745
  ...
# Subtest: stale child Schedule Log writes nothing
ok 1310 - stale child Schedule Log writes nothing
  ---
  duration_ms: 1.898135
  ...
# Subtest: Not now stamps, clears keeps, and advances exactly once
ok 1311 - Not now stamps, clears keeps, and advances exactly once
  ---
  duration_ms: 5.914467
  ...
# Subtest: Keep counts once and saturates at 999 without reset
not ok 1312 - Keep counts once and saturates at 999 without reset
  ---
  duration_ms: 1.90032
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
ok 1313 - Reword stamps, clears, logs, and never advances
  ---
  duration_ms: 1.541834
  ...
# Subtest: Drop cancels with the dropped-after-keeps reason and keeps history
ok 1314 - Drop cancels with the dropped-after-keeps reason and keeps history
  ---
  duration_ms: 0.743811
  ...
# Subtest: Less often at 90+ opens the picker and dismiss writes nothing
ok 1315 - Less often at 90+ opens the picker and dismiss writes nothing
  ---
  duration_ms: 0.684638
  ...
# Subtest: counted session skips at-limit and counts below-limit
ok 1316 - counted session skips at-limit and counts below-limit
  ---
  duration_ms: 0.81162
  ...
# Subtest: counted session skips at-limit on an early date
ok 1317 - counted session skips at-limit on an early date
  ---
  duration_ms: 0.792243
  ...
# Subtest: counted session with every target skipped writes nothing
ok 1318 - counted session with every target skipped writes nothing
  ---
  duration_ms: 0.308078
  ...
# Subtest: availability: decay on (or absent) may ask; decay off never asks
ok 1319 - availability: decay on (or absent) may ask; decay off never asks
  ---
  duration_ms: 1.017994
  ...
# Subtest: trigger: only an explicit decide row decides
ok 1320 - trigger: only an explicit decide row decides
  ---
  duration_ms: 0.196154
  ...
# Subtest: partition: exact at-limit rows skip, everything else stamps
ok 1321 - partition: exact at-limit rows skip, everything else stamps
  ---
  duration_ms: 0.712672
  ...
# Subtest: partition: empty and malformed input stamps nothing and skips nothing
ok 1322 - partition: empty and malformed input stamps nothing and skips nothing
  ---
  duration_ms: 0.150487
  ...
# Subtest: partition: enabled false stamps decision rows (older namespace fallback)
ok 1323 - partition: enabled false stamps decision rows (older namespace fallback)
  ---
  duration_ms: 0.170796
  ...
# Subtest: skip wording: singular, plural, and all-skipped notices
ok 1324 - skip wording: singular, plural, and all-skipped notices
  ---
  duration_ms: 0.196967
  ...
# Subtest: reword cursor: lands at the end of the task body before metadata
ok 1325 - reword cursor: lands at the end of the task body before metadata
  ---
  duration_ms: 0.351771
  ...
# Subtest: captured age: optional context ages, null when created is missing
ok 1326 - captured age: optional context ages, null when created is missing
  ---
  duration_ms: 0.440291
  ...
# Subtest: rows: P0 entry shows the recommended Not now with a clean window
ok 1327 - rows: P0 entry shows the recommended Not now with a clean window
  ---
  duration_ms: 2.878397
  ...
# Subtest: rows: invalid priority config disables Not now and levels, keeps safe rows
ok 1328 - rows: invalid priority config disables Not now and levels, keeps safe rows
  ---
  duration_ms: 0.697923
  ...
# Subtest: rows: picker-mode Less often and 365-day cap
ok 1329 - rows: picker-mode Less often and 365-day cap
  ---
  duration_ms: 1.044384
  ...
# Subtest: rows: terminal ladder keeps Enter available and never cancels
ok 1330 - rows: terminal ladder keeps Enter available and never cancels
  ---
  duration_ms: 0.692843
  ...
# Subtest: modal: Enter approves once; later keys cannot approve again
ok 1331 - modal: Enter approves once; later keys cannot approve again
  ---
  duration_ms: 0.568827
  ...
# Subtest: modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
ok 1332 - modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
  ---
  duration_ms: 0.370217
  ...
# Subtest: modal: key repeat and modified keys never approve
ok 1333 - modal: key repeat and modified keys never approve
  ---
  duration_ms: 0.250308
  ...
# Subtest: modal: Esc changes nothing — dismiss without a choice
ok 1334 - modal: Esc changes nothing — dismiss without a choice
  ---
  duration_ms: 0.133295
  ...
# Subtest: modal: unavailable actions cannot be chosen
ok 1335 - modal: unavailable actions cannot be chosen
  ---
  duration_ms: 0.19388
  ...
# Subtest: modal: a double callback applies once
ok 1336 - modal: a double callback applies once
  ---
  duration_ms: 0.115461
  ...
# Subtest: capability: the nav api exposes the card while loaded
ok 1337 - capability: the nav api exposes the card while loaded
  ---
  duration_ms: 0.431324
  ...
# Subtest: capability: unload drops the card so marks stop promising it
ok 1338 - capability: unload drops the card so marks stop promising it
  ---
  duration_ms: 0.149636
  ...
# Subtest: ladder lookup: the first priority property wins, null without one
ok 1339 - ladder lookup: the first priority property wins, null without one
  ---
  duration_ms: 0.166999
  ...
# Subtest: stage entry resolves the line itself and refuses prose
ok 1340 - stage entry resolves the line itself and refuses prose
  ---
  duration_ms: 3.715577
  ...
# Subtest: Ctrl+Shift+P on a BLOCKS line opens the owner's Blocks stage directly
ok 1341 - Ctrl+Shift+P on a BLOCKS line opens the owner's Blocks stage directly
  ---
  duration_ms: 1.779619
  ...
# Subtest: Ctrl+Shift+P hotkey path on a BLOCKS line opens the owner's Blocks stage directly
ok 1342 - Ctrl+Shift+P hotkey path on a BLOCKS line opens the owner's Blocks stage directly
  ---
  duration_ms: 1.142903
  ...
# Subtest: Ctrl+Shift+Alt+B on a BLOCKS or Depends-On line opens the owner's Blocks stage
ok 1343 - Ctrl+Shift+Alt+B on a BLOCKS or Depends-On line opens the owner's Blocks stage
  ---
  duration_ms: 0.562534
  ...
# Subtest: Ctrl+Shift+P on a Depends-On line is unchanged forward behavior
ok 1344 - Ctrl+Shift+P on a Depends-On line is unchanged forward behavior
  ---
  duration_ms: 0.420012
  ...
# Subtest: Ctrl+Shift+P on a plain child bullet and a nested Task Link are unchanged (3e359a6)
ok 1345 - Ctrl+Shift+P on a plain child bullet and a nested Task Link are unchanged (3e359a6)
  ---
  duration_ms: 7.142411
  ...
# Subtest: forward counted mixed row in BLOCKED keeps the waits-on badge (3e359a6 order)
ok 1346 - forward counted mixed row in BLOCKED keeps the waits-on badge (3e359a6 order)
  ---
  duration_ms: 2.609864
  ...
# Subtest: api.blocks opens the stage and removes only a listed dependent
ok 1347 - api.blocks opens the stage and removes only a listed dependent
  ---
  duration_ms: 2.051948
  ...
# Subtest: api.blocks removeDependent on an owner with no ^id is not-a-dependent
ok 1348 - api.blocks removeDependent on an owner with no ^id is not-a-dependent
  ---
  duration_ms: 0.631326
  ...
# Subtest: stage canonical order ranks \#hide last ahead of the lane
ok 1349 - stage canonical order ranks \#hide last ahead of the lane
  ---
  duration_ms: 0.524181
  ...
# Subtest: stage empty query shows same-note plus In Progress and Next only
ok 1350 - stage empty query shows same-note plus In Progress and Next only
  ---
  duration_ms: 2.840575
  ...
# Subtest: stage cap appends a type-to-search-more hint row
ok 1351 - stage cap appends a type-to-search-more hint row
  ---
  duration_ms: 2.823954
  ...
# Subtest: stage BLOCKED rows carry waits-on counts and short guard reasons
ok 1352 - stage BLOCKED rows carry waits-on counts and short guard reasons
  ---
  duration_ms: 1.160096
  ...
# Subtest: stage removal notices name the task description, not the block id
ok 1353 - stage removal notices name the task description, not the block id
  ---
  duration_ms: 0.436043
  ...
# Subtest: stage Task Link batches keep Depends on without refusal
ok 1354 - stage Task Link batches keep Depends on without refusal
  ---
  duration_ms: 0.478935
  ...
# Subtest: stage batch cycle check runs on the post-batch graph
ok 1355 - stage batch cycle check runs on the post-batch graph
  ---
  duration_ms: 0.487091
  ...
# Subtest: stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
ok 1356 - stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
  ---
  duration_ms: 11.60227
  ...
# Subtest: stage stale single add refuses and reopens
ok 1357 - stage stale single add refuses and reopens
  ---
  duration_ms: 1.517859
  ...
# Subtest: Task Link Depends on focuses a linked note open in a background tab
ok 1358 - Task Link Depends on focuses a linked note open in a background tab
  ---
  duration_ms: 0.383954
  ...
# Subtest: Task Link Blocks focuses the linked note and opens Blocks directly
ok 1359 - Task Link Blocks focuses the linked note and opens Blocks directly
  ---
  duration_ms: 0.348215
  ...
# Subtest: Task Link Depends on refuses clearly when the linked note cannot be focused
    # Subtest: focus reports success but the active view stays elsewhere
    ok 1 - focus reports success but the active view stays elsewhere
      ---
      duration_ms: 0.209841
      ...
    # Subtest: focus reports failure
    ok 2 - focus reports failure
      ---
      duration_ms: 0.150808
      ...
    1..2
ok 1360 - Task Link Depends on refuses clearly when the linked note cannot be focused
  ---
  duration_ms: 0.655893
  ...
# Subtest: stage mirror burst keeps the baseline owner across an insertion above
ok 1361 - stage mirror burst keeps the baseline owner across an insertion above
  ---
  duration_ms: 1003.833234
  ...
# Subtest: stage mirror burst clears on a text-only line deletion
ok 1362 - stage mirror burst clears on a text-only line deletion
  ---
  duration_ms: 1001.236387
  ...
# Subtest: stage mirror vim dd clears the deleted line's owner
ok 1363 - stage mirror vim dd clears the deleted line's owner
  ---
  duration_ms: 1001.814589
  ...
# Subtest: stage badge counts open prerequisites without a block id
ok 1364 - stage badge counts open prerequisites without a block id
  ---
  duration_ms: 4.883977
  ...
# Subtest: stage badge names the future scheduled date with no open prerequisite
ok 1365 - stage badge names the future scheduled date with no open prerequisite
  ---
  duration_ms: 1.430442
  ...
# Subtest: stage badge reads blocked with nothing waiting and no schedule
ok 1366 - stage badge reads blocked with nothing waiting and no schedule
  ---
  duration_ms: 0.872506
  ...
# Subtest: stage vault batch with a stale row refuses and reopens
ok 1367 - stage vault batch with a stale row refuses and reopens
  ---
  duration_ms: 6.574808
  ...
# Subtest: stage opening builds 200/400/1000-task notes without cubic growth
ok 1368 - stage opening builds 200/400/1000-task notes without cubic growth
  ---
  duration_ms: 59.506513
  ...
# Subtest: stage snapshots match standalone parsing across grammar vectors
ok 1369 - stage snapshots match standalone parsing across grammar vectors
  ---
  duration_ms: 5.868777
  ...
# Subtest: stage Warm-empty cache is ready without a vault fallback
ok 1370 - stage Warm-empty cache is ready without a vault fallback
  ---
  duration_ms: 0.469657
  ...
# Subtest: stage opening renders cross-note results with zero writes and cap
ok 1371 - stage opening renders cross-note results with zero writes and cap
  ---
  duration_ms: 39.584746
  ...
# Subtest: stage CURRENT covers same-note, cross-note, blocked, and counted parents
ok 1372 - stage CURRENT covers same-note, cross-note, blocked, and counted parents
  ---
  duration_ms: 1.854732
  ...
# Subtest: stage collections reuse one snapshot per parent
ok 1373 - stage collections reuse one snapshot per parent
  ---
  duration_ms: 0.438458
  ...
# Subtest: stage cold refresh yields, preserves state, and performs no search reads
ok 1374 - stage cold refresh yields, preserves state, and performs no search reads
  ---
  duration_ms: 116.565929
  ...
# Subtest: stage cold refresh abandons after dismissal or replacement
ok 1375 - stage cold refresh abandons after dismissal or replacement
  ---
  duration_ms: 55.781089
  ...
# Subtest: stage 400-task opening finishes in a child process before the parent timeout
ok 1376 - stage 400-task opening finishes in a child process before the parent timeout
  ---
  duration_ms: 93.099572
  ...
# Subtest: stage ranker passes the DK contract vectors verbatim
ok 1377 - stage ranker passes the DK contract vectors verbatim
  ---
  duration_ms: 2.807412
  ...
# Subtest: stage ranker tiers match the capture ranker tier order
ok 1378 - stage ranker tiers match the capture ranker tier order
  ---
  duration_ms: 0.434339
  ...
# Subtest: stage pool excludes daily notes, done, templates, and dot-dirs
ok 1379 - stage pool excludes daily notes, done, templates, and dot-dirs
  ---
  duration_ms: 0.441653
  ...
# Subtest: stage pool collects open vault tasks with buffers as given
ok 1380 - stage pool collects open vault tasks with buffers as given
  ---
  duration_ms: 2.658828
  ...
# Subtest: stage CURRENT resolves same-note, missing, closed, and non-task targets
ok 1381 - stage CURRENT resolves same-note, missing, closed, and non-task targets
  ---
  duration_ms: 2.766344
  ...
# Subtest: stage cycle guard reports the path back to the dependent
ok 1382 - stage cycle guard reports the path back to the dependent
  ---
  duration_ms: 1.337795
  ...
# Subtest: stage view groups CURRENT, RESULTS, and BLOCKED with guards
ok 1383 - stage view groups CURRENT, RESULTS, and BLOCKED with guards
  ---
  duration_ms: 2.778778
  ...
# Subtest: stage view disables cycles and unencodable targets, keeps +id rows
ok 1384 - stage view disables cycles and unencodable targets, keeps +id rows
  ---
  duration_ms: 1.344538
  ...
# Subtest: stage cache tasks normalize across Tasks shapes, buffers win
ok 1385 - stage cache tasks normalize across Tasks shapes, buffers win
  ---
  duration_ms: 0.855634
  ...
# Subtest: stage Task Link mode shows Depends on for one link and batches
ok 1386 - stage Task Link mode shows Depends on for one link and batches
  ---
  duration_ms: 0.880562
  ...
# Subtest: stage mark keys never collide across notes
ok 1387 - stage mark keys never collide across notes
  ---
  duration_ms: 0.201545
  ...
# Subtest: stage display-text locating matches one open task
ok 1388 - stage display-text locating matches one open task
  ---
  duration_ms: 0.244087
  ...
# Subtest: stage selection refusal spans tasks only
ok 1389 - stage selection refusal spans tasks only
  ---
  duration_ms: 0.248054
  ...
# Subtest: stage builder composes pool, current, guards, and pill title
ok 1390 - stage builder composes pool, current, guards, and pill title
  ---
  duration_ms: 1.930446
  ...
# Subtest: stage counted vault add with a stale target refuses and reopens
ok 1391 - stage counted vault add with a stale target refuses and reopens
  ---
  duration_ms: 10.004849
  ...
# Subtest: stage vault commit with a stale write notifies once and reopens
ok 1392 - stage vault commit with a stale write notifies once and reopens
  ---
  duration_ms: 7.79205
  ...
# Subtest: commitVaultRefs refuses a cycle through implicit resident edges
ok 1393 - commitVaultRefs refuses a cycle through implicit resident edges
  ---
  duration_ms: 1.889989
  ...
# Subtest: stage single remove with a stale write notifies once and reopens
ok 1394 - stage single remove with a stale write notifies once and reopens
  ---
  duration_ms: 2.974091
  ...
# Subtest: stage vault single +id guard refuses a stale target
ok 1395 - stage vault single +id guard refuses a stale target
  ---
  duration_ms: 1.458305
  ...
# Subtest: stage vault counted +id guard refuses a stale target
ok 1396 - stage vault counted +id guard refuses a stale target
  ---
  duration_ms: 0.857989
  ...
# Subtest: stage single +id guard refuses a stale target
ok 1397 - stage single +id guard refuses a stale target
  ---
  duration_ms: 0.95304
  ...
# Subtest: stage counted remove with a stale write refuses and reopens
ok 1398 - stage counted remove with a stale write refuses and reopens
  ---
  duration_ms: 3.354427
  ...
# Subtest: stage counted remove counts only changed sources
ok 1399 - stage counted remove counts only changed sources
  ---
  duration_ms: 5.323588
  ...
# Subtest: counted local add on [?] sources reads zero extra notes
ok 1400 - counted local add on [?] sources reads zero extra notes
  ---
  duration_ms: 6.211915
  ...
# Subtest: counted local toggle-off on a Pomodoro-linked [?] source recovers
ok 1401 - counted local toggle-off on a Pomodoro-linked [?] source recovers
  ---
  duration_ms: 6.295143
  ...
# Subtest: stage counted vault add counts only changed sources
ok 1402 - stage counted vault add counts only changed sources
  ---
  duration_ms: 2.245658
  ...
# Subtest: stage counted vault remove counts only changed sources
ok 1403 - stage counted vault remove counts only changed sources
  ---
  duration_ms: 1.92707
  ...
# Subtest: stage +id row prompts without writing
ok 1404 - stage +id row prompts without writing
  ---
  duration_ms: 8.043793
  ...
# Subtest: stage dismissal writes no bytes and drops the batch
ok 1405 - stage dismissal writes no bytes and drops the batch
  ---
  duration_ms: 1.148473
  ...
# Subtest: stage same-note batch commits in one undo group
ok 1406 - stage same-note batch commits in one undo group
  ---
  duration_ms: 10.856223
  ...
# Subtest: stage batch with a stale row refuses and reopens
ok 1407 - stage batch with a stale row refuses and reopens
  ---
  duration_ms: 0.970373
  ...
# Subtest: stage counted add applies to every source task
ok 1408 - stage counted add applies to every source task
  ---
  duration_ms: 34.698161
  ...
# Subtest: stage batch cycle rows stay guarded and write nothing
ok 1409 - stage batch cycle rows stay guarded and write nothing
  ---
  duration_ms: 27.767755
  ...
# Subtest: stage edit-task-dependencies registers with no default hotkey
ok 1410 - stage edit-task-dependencies registers with no default hotkey
  ---
  duration_ms: 1.613071
  ...
# Subtest: task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row
ok 1411 - task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row
  ---
  duration_ms: 1.038714
  ...
# Subtest: task-card-blocks registers Ctrl+Shift+Alt+B and opens the Blocks row
ok 1412 - task-card-blocks registers Ctrl+Shift+Alt+B and opens the Blocks row
  ---
  duration_ms: 0.786813
  ...
# Subtest: stage waits-on badge counts open prerequisites only
ok 1413 - stage waits-on badge counts open prerequisites only
  ---
  duration_ms: 2.388342
  ...
# Subtest: stage cycle tooltip shows task descriptions
ok 1414 - stage cycle tooltip shows task descriptions
  ---
  duration_ms: 1.703524
  ...
# Subtest: stage same-note single add stamps the dependent and keeps its cursor
ok 1415 - stage same-note single add stamps the dependent and keeps its cursor
  ---
  duration_ms: 7.709393
  ...
# Subtest: stage same-note marked batch stamps the dependent and keeps its cursor
ok 1416 - stage same-note marked batch stamps the dependent and keeps its cursor
  ---
  duration_ms: 5.002604
  ...
# Subtest: Tab marks a same-note CURRENT row and Enter removes it
ok 1417 - Tab marks a same-note CURRENT row and Enter removes it
  ---
  duration_ms: 31.078849
  ...
# Subtest: Tab twice unmarks a CURRENT row
ok 1418 - Tab twice unmarks a CURRENT row
  ---
  duration_ms: 26.237263
  ...
# Subtest: Tab mixed CURRENT removal and RESULTS add apply in one commit
ok 1419 - Tab mixed CURRENT removal and RESULTS add apply in one commit
  ---
  duration_ms: 29.741213
  ...
# Subtest: Tab marks a missing CURRENT target and the batch removes it
ok 1420 - Tab marks a missing CURRENT target and the batch removes it
  ---
  duration_ms: 30.5987
  ...
# Subtest: Tab same-note and cross-note CURRENT removals apply in one vault batch
ok 1421 - Tab same-note and cross-note CURRENT removals apply in one vault batch
  ---
  duration_ms: 30.811426
  ...
# Subtest: cross-note add awaits preparation before the one commit
ok 1422 - cross-note add awaits preparation before the one commit
  ---
  duration_ms: 19.45717
  ...
# Subtest: a failed async preparation leaves the dependent untouched
ok 1423 - a failed async preparation leaves the dependent untouched
  ---
  duration_ms: 7.15685
  ...
# Subtest: links to unloaded notes tolerate add, remove, and deleted targets
ok 1424 - links to unloaded notes tolerate add, remove, and deleted targets
  ---
  duration_ms: 5.067258
  ...
# Subtest: Pomodoro-linked dependents recover through the plugin vault read
ok 1425 - Pomodoro-linked dependents recover through the plugin vault read
  ---
  duration_ms: 7.236471
  ...
# Subtest: same-note batch +id stamps the target and links in one undo group
ok 1426 - same-note batch +id stamps the target and links in one undo group
  ---
  duration_ms: 10.736925
  ...
# Subtest: confirmBatchBlockId collects the id and executes the batch
ok 1427 - confirmBatchBlockId collects the id and executes the batch
  ---
  duration_ms: 3.141769
  ...
# Subtest: commitMarkedDependencies executes ready additions at once
ok 1428 - commitMarkedDependencies executes ready additions at once
  ---
  duration_ms: 2.841608
  ...
# Subtest: counted vault add links two siblings bottom-up
ok 1429 - counted vault add links two siblings bottom-up
  ---
  duration_ms: 5.349848
  ...
# Subtest: counted CURRENT rows without a line remove from every source
ok 1430 - counted CURRENT rows without a line remove from every source
  ---
  duration_ms: 9.839544
  ...
# Subtest: a stale editor between await and commit refuses
ok 1431 - a stale editor between await and commit refuses
  ---
  duration_ms: 1.610856
  ...
# Subtest: removeDependencyByRef refuses targets that are not on the line
ok 1432 - removeDependencyByRef refuses targets that are not on the line
  ---
  duration_ms: 1.557886
  ...
# Subtest: kept unloaded links resolve the field id by line position
ok 1433 - kept unloaded links resolve the field id by line position
  ---
  duration_ms: 3.030087
  ...
# Subtest: pendingTargetLine commits the same-note target id with the link
ok 1434 - pendingTargetLine commits the same-note target id with the link
  ---
  duration_ms: 2.970652
  ...
# Subtest: counted vault add commits every source in one transaction
ok 1435 - counted vault add commits every source in one transaction
  ---
  duration_ms: 2.878047
  ...
# Subtest: field-only clears snapshot the vault and recover
ok 1436 - field-only clears snapshot the vault and recover
  ---
  duration_ms: 1.574227
  ...
# Subtest: adds without recovery read zero extra vault notes
ok 1437 - adds without recovery read zero extra vault notes
  ---
  duration_ms: 0.766304
  ...
# Subtest: hand-edit clear recovers Pomodoro-linked dependents to Next
ok 1438 - hand-edit clear recovers Pomodoro-linked dependents to Next
  ---
  duration_ms: 1.296757
  ...
# Subtest: hand-edit clear on a non-Blocked parent reads zero extra notes
ok 1439 - hand-edit clear on a non-Blocked parent reads zero extra notes
  ---
  duration_ms: 0.469466
  ...
# Subtest: writer keeps the full route for duplicate basenames
ok 1440 - writer keeps the full route for duplicate basenames
  ---
  duration_ms: 0.872487
  ...
# Subtest: adds on Blocked parents and non-Blocked mirror touches read nothing
ok 1441 - adds on Blocked parents and non-Blocked mirror touches read nothing
  ---
  duration_ms: 0.993177
  ...
# Subtest: counted vault add loads each source's existing links
ok 1442 - counted vault add loads each source's existing links
  ---
  duration_ms: 2.893577
  ...
# Subtest: counted Ctrl+D on a blockquoted task refuses with the blockquote notice
ok 1443 - counted Ctrl+D on a blockquoted task refuses with the blockquote notice
  ---
  duration_ms: 0.7173
  ...
# Subtest: single Ctrl+D on a quoted task without a field refuses as a blockquote
ok 1444 - single Ctrl+D on a quoted task without a field refuses as a blockquote
  ---
  duration_ms: 0.244457
  ...
# Subtest: confirmSingleBlockId folds the target id into one transaction
ok 1445 - confirmSingleBlockId folds the target id into one transaction
  ---
  duration_ms: 2.432897
  ...
# Subtest: chooseTaskDependency folds a missing target id into one transaction
ok 1446 - chooseTaskDependency folds a missing target id into one transaction
  ---
  duration_ms: 3.835384
  ...
# Subtest: counted remove commits every source in one transaction
ok 1447 - counted remove commits every source in one transaction
  ---
  duration_ms: 3.935996
  ...
# Subtest: DP parse vectors accept, empty, malformed, and not-a-line
ok 1448 - DP parse vectors accept, empty, malformed, and not-a-line
  ---
  duration_ms: 3.922241
  ...
# Subtest: DP30 attributes a Work-Log-nested Depends-On line to the inner task
ok 1449 - DP30 attributes a Work-Log-nested Depends-On line to the inner task
  ---
  duration_ms: 2.882887
  ...
# Subtest: fenced lines never collect as Depends-On lines
ok 1450 - fenced lines never collect as Depends-On lines
  ---
  duration_ms: 0.50803
  ...
# Subtest: DW1 creates the line as the first child
ok 1451 - DW1 creates the line as the first child
  ---
  duration_ms: 5.730696
  ...
# Subtest: DW2 creates the line after a Cancel Log
ok 1452 - DW2 creates the line after a Cancel Log
  ---
  duration_ms: 1.363715
  ...
# Subtest: DW3-DW5 append, remove the middle, and delete on the last link
ok 1453 - DW3-DW5 append, remove the middle, and delete on the last link
  ---
  duration_ms: 4.966626
  ...
# Subtest: DW6-DW7 re-add moves to the end and the field mirrors the line
ok 1454 - DW6-DW7 re-add moves to the end and the field mirrors the line
  ---
  duration_ms: 0.844422
  ...
# Subtest: DW8 tab parents deepen the child by one tab
ok 1455 - DW8 tab parents deepen the child by one tab
  ---
  duration_ms: 1.47114
  ...
# Subtest: DW9 space parents reuse the existing child indent
ok 1456 - DW9 space parents reuse the existing child indent
  ---
  duration_ms: 0.926931
  ...
# Subtest: DW10-DW11 CRLF and final-newline state survive
ok 1457 - DW10-DW11 CRLF and final-newline state survive
  ---
  duration_ms: 0.92174
  ...
# Subtest: DW12-DW14 link form is the shortest unambiguous form
ok 1458 - DW12-DW14 link form is the shortest unambiguous form
  ---
  duration_ms: 0.28274
  ...
# Subtest: archive targets keep the explicit done/ path form
ok 1459 - archive targets keep the explicit done/ path form
  ---
  duration_ms: 0.194322
  ...
# Subtest: DW15 an existing id is never rewritten
ok 1460 - DW15 an existing id is never rewritten
  ---
  duration_ms: 0.347043
  ...
# Subtest: DW16 an unencodable path without an id refuses
ok 1461 - DW16 an unencodable path without an id refuses
  ---
  duration_ms: 0.254686
  ...
# Subtest: DW17 field placement follows fresh and precedes the block id
ok 1462 - DW17 field placement follows fresh and precedes the block id
  ---
  duration_ms: 0.898256
  ...
# Subtest: DW18 legacy children fold into the line
ok 1463 - DW18 legacy children fold into the line
  ---
  duration_ms: 0.926539
  ...
# Subtest: DW19 variants canonicalise to the writer form
ok 1464 - DW19 variants canonicalise to the writer form
  ---
  duration_ms: 1.34566
  ...
# Subtest: adding an open prerequisite blocks the dependent
ok 1465 - adding an open prerequisite blocks the dependent
  ---
  duration_ms: 0.377481
  ...
# Subtest: adding transfers Next and In Progress commitment to the open target
ok 1466 - adding transfers Next and In Progress commitment to the open target
  ---
  duration_ms: 0.610105
  ...
# Subtest: removing the last open prerequisite recovers immediately
ok 1467 - removing the last open prerequisite recovers immediately
  ---
  duration_ms: 0.890701
  ...
# Subtest: removal stays Blocked while another prerequisite is open
ok 1468 - removal stays Blocked while another prerequisite is open
  ---
  duration_ms: 0.423399
  ...
# Subtest: removal stays Blocked with a future schedule
ok 1469 - removal stays Blocked with a future schedule
  ---
  duration_ms: 0.410244
  ...
# Subtest: one gesture commits the dependent note in a single transaction
ok 1470 - one gesture commits the dependent note in a single transaction
  ---
  duration_ms: 2.242262
  ...
# Subtest: a failed preparation leaves the dependent untouched
ok 1471 - a failed preparation leaves the dependent untouched
  ---
  duration_ms: 0.61272
  ...
# Subtest: recovery references follow the line plus covered legacy children
ok 1472 - recovery references follow the line plus covered legacy children
  ---
  duration_ms: 0.677704
  ...
# Subtest: task-block helpers find owners, lines, and insertion points
ok 1473 - task-block helpers find owners, lines, and insertion points
  ---
  duration_ms: 0.48222
  ...
# Subtest: dependency notices follow the contract shapes
ok 1474 - dependency notices follow the contract shapes
  ---
  duration_ms: 0.196004
  ...
# Subtest: nav api v3 resolves results and never throws
ok 1475 - nav api v3 resolves results and never throws
  ---
  duration_ms: 1.604764
  ...
# Subtest: getDependencyInsertLine lands after a Cancel Log subtree
ok 1476 - getDependencyInsertLine lands after a Cancel Log subtree
  ---
  duration_ms: 0.433929
  ...
# Subtest: planner: an ordinary dependent with a block id plus an open add yields one target
ok 1477 - planner: an ordinary dependent with a block id plus an open add yields one target
  ---
  duration_ms: 9.331503
  ...
# Subtest: planner: adding only a closed target yields none
ok 1478 - planner: adding only a closed target yields none
  ---
  duration_ms: 1.171788
  ...
# Subtest: planner: no block id yields none
ok 1479 - planner: no block id yields none
  ---
  duration_ms: 0.656614
  ...
# Subtest: planner: a dependent already [?] with an open add yields a target
ok 1480 - planner: a dependent already [?] with an open add yields a target
  ---
  duration_ms: 2.234458
  ...
# Subtest: planner: a removal yields none
ok 1481 - planner: a removal yields none
  ---
  duration_ms: 1.39837
  ...
# Subtest: planner: mirrorTouch emits no ordinary consumption target
ok 1482 - planner: mirrorTouch emits no ordinary consumption target
  ---
  duration_ms: 0.593704
  ...
# Subtest: planner: ^prj keeps project targets and a deduplicated union
ok 1483 - planner: ^prj keeps project targets and a deduplicated union
  ---
  duration_ms: 3.130228
  ...
# Subtest: suffix helper names the removed count and the failed follow-up
ok 1484 - suffix helper names the removed count and the failed follow-up
  ---
  duration_ms: 0.18827
  ...
# Subtest: applyDependencyEdit cross-file consumes live links and emptied entries
ok 1485 - applyDependencyEdit cross-file consumes live links and emptied entries
  ---
  duration_ms: 12.068399
  ...
# Subtest: applyDependencyEdit removes one live link and reports it
ok 1486 - applyDependencyEdit removes one live link and reports it
  ---
  duration_ms: 3.380507
  ...
# Subtest: applyDependencyEdit keeps the dependent write when the daily preimage changes
ok 1487 - applyDependencyEdit keeps the dependent write when the daily preimage changes
  ---
  duration_ms: 2.087066
  ...
# Subtest: same-file fold lands the dependency and the cleanup in one undo group
ok 1488 - same-file fold lands the dependency and the cleanup in one undo group
  ---
  duration_ms: 2.452084
  ...
# Subtest: setLocalTaskDependencyLink stays synchronous and folds same-file cleanup
ok 1489 - setLocalTaskDependencyLink stays synchronous and folds same-file cleanup
  ---
  duration_ms: 2.845685
  ...
# Subtest: setLocalTaskDependencyLink cross-file continuation removes the live link
ok 1490 - setLocalTaskDependencyLink cross-file continuation removes the live link
  ---
  duration_ms: 14.153041
  ...
# Subtest: same-note marked batch consumes every newly Blocked source
ok 1491 - same-note marked batch consumes every newly Blocked source
  ---
  duration_ms: 10.902523
  ...
# Subtest: counted same-note writer consumes every newly Blocked source
ok 1492 - counted same-note writer consumes every newly Blocked source
  ---
  duration_ms: 6.912009
  ...
# Subtest: counted vault writer consumes every newly Blocked source
ok 1493 - counted vault writer consumes every newly Blocked source
  ---
  duration_ms: 3.648619
  ...
# Subtest: counted ^prj source consumes its project targets
ok 1494 - counted ^prj source consumes its project targets
  ---
  duration_ms: 2.95311
  ...
# Subtest: a dependent without a block id does zero cachedReads even when today's daily exists
ok 1495 - a dependent without a block id does zero cachedReads even when today's daily exists
  ---
  duration_ms: 1.35106
  ...
# Subtest: alignment key ignores fields, the block id, the status and trailing space
ok 1496 - alignment key ignores fields, the block id, the status and trailing space
  ---
  duration_ms: 1.831108
  ...
# Subtest: insertion after a modified line edits that line and inserts after it
ok 1497 - insertion after a modified line edits that line and inserts after it
  ---
  duration_ms: 2.008416
  ...
# Subtest: adjacent prerequisite and parent both change while two lines insert
ok 1498 - adjacent prerequisite and parent both change while two lines insert
  ---
  duration_ms: 0.743009
  ...
# Subtest: deletion at the end of the document
ok 1499 - deletion at the end of the document
  ---
  duration_ms: 0.635344
  ...
# Subtest: insertion at the top and at the end of the document
ok 1500 - insertion at the top and at the end of the document
  ---
  duration_ms: 0.5286
  ...
# Subtest: empty documents align and apply
ok 1501 - empty documents align and apply
  ---
  duration_ms: 0.336744
  ...
# Subtest: CRLF documents insert and delete with CRLF
ok 1502 - CRLF documents insert and delete with CRLF
  ---
  duration_ms: 0.431034
  ...
# Subtest: equal-count shifted edits take the aligned path
ok 1503 - equal-count shifted edits take the aligned path
  ---
  duration_ms: 0.839544
  ...
# Subtest: pure in-place edits keep the line-bounded change shapes
ok 1504 - pure in-place edits keep the line-bounded change shapes
  ---
  duration_ms: 1.011111
  ...
# Subtest: an unchanged document writes nothing
ok 1505 - an unchanged document writes nothing
  ---
  duration_ms: 0.401507
  ...
# Subtest: an explicit final cursor wins over the mapped cursor
ok 1506 - an explicit final cursor wins over the mapped cursor
  ---
  duration_ms: 0.26691
  ...
# Subtest: the machine-write annotation still reaches the transaction
ok 1507 - the machine-write annotation still reaches the transaction
  ---
  duration_ms: 0.166328
  ...
# Subtest: an editor without transaction falls back to bottom-up replaceRange
ok 1508 - an editor without transaction falls back to bottom-up replaceRange
  ---
  duration_ms: 0.307768
  ...
# Subtest: positions map through aligned, changed, gap and deleted lines
ok 1509 - positions map through aligned, changed, gap and deleted lines
  ---
  duration_ms: 0.382049
  ...
# Subtest: a deletion at the end of the document maps to the last line
ok 1510 - a deletion at the end of the document maps to the last line
  ---
  duration_ms: 0.10988
  ...
# Subtest: a gap with new lines maps by offset and clamps to its last line
ok 1511 - a gap with new lines maps by offset and clamps to its last line
  ---
  duration_ms: 0.153283
  ...
# Subtest: seeded property: planned changes rebuild the new text and map unchanged lines
ok 1512 - seeded property: planned changes rebuild the new text and map unchanged lines
  ---
  duration_ms: 55.106619
  ...
# Subtest: a diff past the edit cap becomes one unaligned gap
ok 1513 - a diff past the edit cap becomes one unaligned gap
  ---
  duration_ms: 86.925489
  ...
# Subtest: the CM6 double reproduces the whole-document replacement jump
ok 1514 - the CM6 double reproduces the whole-document replacement jump
  ---
  duration_ms: 0.860183
  ...
# Subtest: first cross-note prerequisite keeps the cursor and the viewport
ok 1515 - first cross-note prerequisite keeps the cursor and the viewport
  ---
  duration_ms: 8.083449
  ...
# Subtest: same-note prerequisite directly above keeps the dependent's line
ok 1516 - same-note prerequisite directly above keeps the dependent's line
  ---
  duration_ms: 5.289553
  ...
# Subtest: removing the last prerequisite keeps the dependent's line
ok 1517 - removing the last prerequisite keeps the dependent's line
  ---
  duration_ms: 6.26658
  ...
# Subtest: a Blocks source gaining its first BLOCKS line keeps its line
ok 1518 - a Blocks source gaining its first BLOCKS line keeps its line
  ---
  duration_ms: 0.657847
  ...
# Subtest: missing ledger-tools api refuses the review namespace
ok 1519 - missing ledger-tools api refuses the review namespace
  ---
  duration_ms: 2.168321
  ...
# Subtest: review jump on an empty queue
ok 1520 - review jump on an empty queue
  ---
  duration_ms: 1.208778
  ...
# Subtest: review jump from a queued task goes to the neighbor
ok 1521 - review jump from a queued task goes to the neighbor
  ---
  duration_ms: 0.89032
  ...
# Subtest: review jump wraps at the ends
ok 1522 - review jump wraps at the ends
  ---
  duration_ms: 0.364686
  ...
# Subtest: review jump from elsewhere goes to the first or last entry
ok 1523 - review jump from elsewhere goes to the first or last entry
  ---
  duration_ms: 0.279453
  ...
# Subtest: review jump matches a moved cursor task by text
ok 1524 - review jump matches a moved cursor task by text
  ---
  duration_ms: 0.21997
  ...
# Subtest: review jump from a just-stamped rank goes to the entry after it
ok 1525 - review jump from a just-stamped rank goes to the entry after it
  ---
  duration_ms: 0.364586
  ...
# Subtest: review jump skips just-stamped keys the lagging cache still shows
ok 1526 - review jump skips just-stamped keys the lagging cache still shows
  ---
  duration_ms: 0.23002
  ...
# Subtest: review jump after stamping everything reports empty or wraps
ok 1527 - review jump after stamping everything reports empty or wraps
  ---
  duration_ms: 0.661823
  ...
# Subtest: review queue line resolves at the entry line
ok 1528 - review queue line resolves at the entry line
  ---
  duration_ms: 0.7385
  ...
# Subtest: review queue line follows a moved line to its unique match
ok 1529 - review queue line follows a moved line to its unique match
  ---
  duration_ms: 0.497641
  ...
# Subtest: review queue line goes stale on duplicates or a missing line
ok 1530 - review queue line goes stale on duplicates or a missing line
  ---
  duration_ms: 0.283501
  ...
# Subtest: review jump notices name the state
ok 1531 - review jump notices name the state
  ---
  duration_ms: 0.585498
  ...
# Subtest: fresh stamp targets refuse closed and recurring tasks
ok 1532 - fresh stamp targets refuse closed and recurring tasks
  ---
  duration_ms: 0.910128
  ...
# Subtest: fresh stamp batch stamps every target and nothing else
ok 1533 - fresh stamp batch stamps every target and nothing else
  ---
  duration_ms: 0.425613
  ...
# Subtest: one refusal refuses the whole fresh stamp batch
ok 1534 - one refusal refuses the whole fresh stamp batch
  ---
  duration_ms: 0.417176
  ...
# Subtest: a throwing stamper refuses the fresh stamp batch
ok 1535 - a throwing stamper refuses the fresh stamp batch
  ---
  duration_ms: 0.229077
  ...
# Subtest: fresh stamp plus Work Log prepends only stamped Pending targets
ok 1536 - fresh stamp plus Work Log prepends only stamped Pending targets
  ---
  duration_ms: 1.563857
  ...
# Subtest: blank Work Log summary and stamp refusal never create a log marker
ok 1537 - blank Work Log summary and stamp refusal never create a log marker
  ---
  duration_ms: 0.31961
  ...
# Subtest: fresh stamp notices adjust the pre-write counts
ok 1538 - fresh stamp notices adjust the pre-write counts
  ---
  duration_ms: 0.297458
  ...
# Subtest: today detection only matches today's fresh field
ok 1539 - today detection only matches today's fresh field
  ---
  duration_ms: 0.274755
  ...
# Subtest: stamped refs match the pre-write queue by line or text
ok 1540 - stamped refs match the pre-write queue by line or text
  ---
  duration_ms: 0.515104
  ...
# Subtest: review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
ok 1541 - review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
  ---
  duration_ms: 0.346452
  ...
# Subtest: tier-aware jump notices name each tier
ok 1542 - tier-aware jump notices name each tier
  ---
  duration_ms: 0.762376
  ...
# Subtest: projects tier walks with commitment rank and empty-project notice
ok 1543 - projects tier walks with commitment rank and empty-project notice
  ---
  duration_ms: 0.283582
  ...
# Subtest: references tier walks with commitment rank and reference notice
ok 1544 - references tier walks with commitment rank and reference notice
  ---
  duration_ms: 0.654921
  ...
# Subtest: jump notices use reviewEntryView when provided and keep the fallback
ok 1545 - jump notices use reviewEntryView when provided and keep the fallback
  ---
  duration_ms: 0.435612
  ...
# Subtest: tier notices fall back without tier ranks and wrap on the last line
ok 1546 - tier notices fall back without tier ranks and wrap on the last line
  ---
  duration_ms: 0.20442
  ...
# Subtest: boundary notice names commitments done and rotten next
ok 1547 - boundary notice names commitments done and rotten next
  ---
  duration_ms: 0.173872
  ...
# Subtest: walk anchor records handled keys with their neighbors
ok 1548 - walk anchor records handled keys with their neighbors
  ---
  duration_ms: 0.652826
  ...
# Subtest: cursor on a live entry wins over a lagging anchor
ok 1549 - cursor on a live entry wins over a lagging anchor
  ---
  duration_ms: 0.37183
  ...
# Subtest: [s after a stamp goes backwards from the anchor
ok 1550 - [s after a stamp goes backwards from the anchor
  ---
  duration_ms: 0.636736
  ...
# Subtest: release-then-]s continues from the anchor successor
ok 1551 - release-then-]s continues from the anchor successor
  ---
  duration_ms: 0.265287
  ...
# Subtest: non-contiguous counted stamp advances past the last handled rank
ok 1552 - non-contiguous counted stamp advances past the last handled rank
  ---
  duration_ms: 0.413279
  ...
# Subtest: anchor wraps at both ends
ok 1553 - anchor wraps at both ends
  ---
  duration_ms: 0.429701
  ...
# Subtest: advance across NEXT to TICKLER to ROTTEN lands the boundary
ok 1554 - advance across NEXT to TICKLER to ROTTEN lands the boundary
  ---
  duration_ms: 0.486419
  ...
# Subtest: tier capability gates on the freshness namespace version
ok 1555 - tier capability gates on the freshness namespace version
  ---
  duration_ms: 0.161539
  ...
# Subtest: empty queue notice reads the upkeep meter
ok 1556 - empty queue notice reads the upkeep meter
  ---
  duration_ms: 0.137152
  ...
# Subtest: refresh row reads lane intervals from the api with the once-Ready return
ok 1557 - refresh row reads lane intervals from the api with the once-Ready return
  ---
  duration_ms: 1.468906
  ...
# Subtest: endpoint jumps select the queue ends with full rank and total
ok 1558 - endpoint jumps select the queue ends with full rank and total
  ---
  duration_ms: 0.43426
  ...
# Subtest: endpoint jumps ignore cursor, anchor, and direction
ok 1559 - endpoint jumps ignore cursor, anchor, and direction
  ---
  duration_ms: 0.325121
  ...
# Subtest: endpoint jumps on empty and one-entry queues
ok 1560 - endpoint jumps on empty and one-entry queues
  ---
  duration_ms: 0.27247
  ...
# Subtest: a visited endpoint is still due under its own anchor
ok 1561 - a visited endpoint is still due under its own anchor
  ---
  duration_ms: 0.222095
  ...
# Subtest: lowercase steps continue from an endpoint anchor
ok 1562 - lowercase steps continue from an endpoint anchor
  ---
  duration_ms: 0.376669
  ...
# Subtest: counted review jump repeat 1 matches omitted repeat
ok 1563 - counted review jump repeat 1 matches omitted repeat
  ---
  duration_ms: 0.78517
  ...
# Subtest: counted review jump from the first entry lands N steps ahead
ok 1564 - counted review jump from the first entry lands N steps ahead
  ---
  duration_ms: 0.310163
  ...
# Subtest: counted review jump from the last entry wraps past the start
ok 1565 - counted review jump from the last entry wraps past the start
  ---
  duration_ms: 0.17801
  ...
# Subtest: counted review jump larger than the queue wraps once
ok 1566 - counted review jump larger than the queue wraps once
  ---
  duration_ms: 0.203379
  ...
# Subtest: counted review jump on a one-entry queue stays there
ok 1567 - counted review jump on a one-entry queue stays there
  ---
  duration_ms: 0.18873
  ...
# Subtest: counted review jump with no origin lands on the Nth entry
ok 1568 - counted review jump with no origin lands on the Nth entry
  ---
  duration_ms: 0.188911
  ...
# Subtest: counted review jump from a shaped anchor takes N surviving successors
ok 1569 - counted review jump from a shaped anchor takes N surviving successors
  ---
  duration_ms: 0.249496
  ...
# Subtest: counted review jump does not change endpoint selection
ok 1570 - counted review jump does not change endpoint selection
  ---
  duration_ms: 0.194021
  ...
# Subtest: a stamped endpoint that moved is stale and cannot land from old text
ok 1571 - a stamped endpoint that moved is stale and cannot land from old text
  ---
  duration_ms: 0.247612
  ...
# Subtest: stale endpoint target reselects the same endpoint in the new queue
ok 1572 - stale endpoint target reselects the same endpoint in the new queue
  ---
  duration_ms: 1.957109
  ...
# Subtest: endpoint retry is bounded and failures preserve the anchor
ok 1573 - endpoint retry is bounded and failures preserve the anchor
  ---
  duration_ms: 0.639682
  ...
# Subtest: endpoint jump to ROTTEN carries no boundary preamble
ok 1574 - endpoint jump to ROTTEN carries no boundary preamble
  ---
  duration_ms: 0.88973
  ...
# Subtest: endpoint notices keep v4 tier details and legacy v3 text
ok 1575 - endpoint notices keep v4 tier details and legacy v3 text
  ---
  duration_ms: 0.160176
  ...
# Subtest: onload registers first/last commands routed to the shared jump
ok 1576 - onload registers first/last commands routed to the shared jump
  ---
  duration_ms: 1.920719
  ...
# Subtest: jumpToDueTask consumes a pending Vim prefix as N review steps
ok 1577 - jumpToDueTask consumes a pending Vim prefix as N review steps
  ---
  duration_ms: 1.140298
  ...
# Subtest: registered next-due-task callback reads the pending Vim prefix
ok 1578 - registered next-due-task callback reads the pending Vim prefix
  ---
  duration_ms: 1.007915
  ...
# Subtest: explicit jumpToDueTask repeat skips the Vim prefix
ok 1579 - explicit jumpToDueTask repeat skips the Vim prefix
  ---
  duration_ms: 0.407518
  ...
# Subtest: non-normal editor with a pending prefix still jumps one entry
ok 1580 - non-normal editor with a pending prefix still jumps one entry
  ---
  duration_ms: 0.363053
  ...
# Subtest: stale counted replan reuses the captured repeat
ok 1581 - stale counted replan reuses the captured repeat
  ---
  duration_ms: 0.398641
  ...
# Subtest: endpoint jump with a pending prefix still lands on the endpoint
ok 1582 - endpoint jump with a pending prefix still lands on the endpoint
  ---
  duration_ms: 0.330391
  ...
# Subtest: counted forward landing on ROTTEN keeps the boundary preamble
ok 1583 - counted forward landing on ROTTEN keeps the boundary preamble
  ---
  duration_ms: 0.604264
  ...
# Subtest: PRE and POST are machine tiers; PRE is a commitment
ok 1584 - PRE and POST are machine tiers; PRE is a commitment
  ---
  duration_ms: 0.282319
  ...
# Subtest: fallback notices name PRE checklist and POST closeout
ok 1585 - fallback notices name PRE checklist and POST closeout
  ---
  duration_ms: 0.314581
  ...
# Subtest: text-first cursor matching does not skip Pills after an above-insert
ok 1586 - text-first cursor matching does not skip Pills after an above-insert
  ---
  duration_ms: 0.176246
  ...
# Subtest: day-scoped anchors from another day are ignored
ok 1587 - day-scoped anchors from another day are ignored
  ---
  duration_ms: 0.301155
  ...
# Subtest: boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
ok 1588 - boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
  ---
  duration_ms: 0.283842
  ...
# Subtest: ]S reaches POST with 77 ROTTEN rows and a null budget
ok 1589 - ]S reaches POST with 77 ROTTEN rows and a null budget
  ---
  duration_ms: 0.701961
  ...
# Subtest: nav normalizes a legacy v7 returned tier to tickler
ok 1590 - nav normalizes a legacy v7 returned tier to tickler
  ---
  duration_ms: 0.144837
  ...
# Subtest: RECURRING is a machine tier, a commitment, and a v9 capability
ok 1591 - RECURRING is a machine tier, a commitment, and a v9 capability
  ---
  duration_ms: 0.196906
  ...
# Subtest: RECURRING counts in reviewWalkRemaining and gates the boundary
ok 1592 - RECURRING counts in reviewWalkRemaining and gates the boundary
  ---
  duration_ms: 0.195364
  ...
# Subtest: matchReviewRecurringCursor is text-first like the checklist matcher
ok 1593 - matchReviewRecurringCursor is text-first like the checklist matcher
  ---
  duration_ms: 0.237854
  ...
# Subtest: fallback notices name RECURRING due detail with the reschedule hint
ok 1594 - fallback notices name RECURRING due detail with the reschedule hint
  ---
  duration_ms: 0.179012
  ...
# Subtest: Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
ok 1595 - Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
  ---
  duration_ms: 0.164284
  ...
# Subtest: bobLineDigest matches the shared bob-cli vectors
ok 1596 - bobLineDigest matches the shared bob-cli vectors
  ---
  duration_ms: 4.015089
  ...
# Subtest: parseGoToTaskParams accepts a complete v1 link and ignores extra keys
ok 1597 - parseGoToTaskParams accepts a complete v1 link and ignores extra keys
  ---
  duration_ms: 0.750704
  ...
# Subtest: parseGoToTaskParams treats ref and block as optional
ok 1598 - parseGoToTaskParams treats ref and block as optional
  ---
  duration_ms: 0.139236
  ...
# Subtest: parseGoToTaskParams rejects each malformed field
ok 1599 - parseGoToTaskParams rejects each malformed field
  ---
  duration_ms: 0.251861
  ...
# Subtest: vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
ok 1600 - vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
  ---
  duration_ms: 0.34033
  ...
# Subtest: refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
ok 1601 - refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
  ---
  duration_ms: 1.600497
  ...
# Subtest: handleGoToTaskUri notices each malformed parameter
ok 1602 - handleGoToTaskUri notices each malformed parameter
  ---
  duration_ms: 1.184152
  ...
# Subtest: handleGoToTaskUri notices a path outside the vault
ok 1603 - handleGoToTaskUri notices a path outside the vault
  ---
  duration_ms: 0.426916
  ...
# Subtest: handleGoToTaskUri notices a missing file inside the vault
ok 1604 - handleGoToTaskUri notices a missing file inside the vault
  ---
  duration_ms: 0.486008
  ...
# Subtest: handleGoToTaskUri maps a trailing-slash vault base
ok 1605 - handleGoToTaskUri maps a trailing-slash vault base
  ---
  duration_ms: 1.75386
  ...
# Subtest: handleGoToTaskUri prefers the open buffer over cachedRead
ok 1606 - handleGoToTaskUri prefers the open buffer over cachedRead
  ---
  duration_ms: 0.71762
  ...
# Subtest: handleGoToTaskUri re-finds by block id after an insert above the task
ok 1607 - handleGoToTaskUri re-finds by block id after an insert above the task
  ---
  duration_ms: 0.463736
  ...
# Subtest: handleGoToTaskUri re-finds a unique digest after a shift with no block
ok 1608 - handleGoToTaskUri re-finds a unique digest after a shift with no block
  ---
  duration_ms: 0.485407
  ...
# Subtest: handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
ok 1609 - handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
  ---
  duration_ms: 0.381098
  ...
# Subtest: handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
ok 1610 - handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
  ---
  duration_ms: 0.446042
  ...
# Subtest: handleGoToTaskUri reuses a leaf that already shows the note
ok 1611 - handleGoToTaskUri reuses a leaf that already shows the note
  ---
  duration_ms: 0.574948
  ...
# Subtest: handleGoToTaskUri switches a Reading-view leaf to editing
ok 1612 - handleGoToTaskUri switches a Reading-view leaf to editing
  ---
  duration_ms: 0.662786
  ...
# Subtest: handleGoToTaskUri records a jump from the prior cursor and none without one
ok 1613 - handleGoToTaskUri records a jump from the prior cursor and none without one
  ---
  duration_ms: 0.775391
  ...
# Subtest: handleGoToTaskUri never writes the vault or advances the walk
ok 1614 - handleGoToTaskUri never writes the vault or advances the walk
  ---
  duration_ms: 0.372391
  ...
# Subtest: handleGoToTaskUri reports when the note cannot be opened
ok 1615 - handleGoToTaskUri reports when the note cannot be opened
  ---
  duration_ms: 0.308429
  ...
# Subtest: focusTaskMoveDestination still lands without switching Reading view
ok 1616 - focusTaskMoveDestination still lands without switching Reading view
  ---
  duration_ms: 0.360078
  ...
# Subtest: onload registers both read-only navigation protocols when available
ok 1617 - onload registers both read-only navigation protocols when available
  ---
  duration_ms: 1.076837
  ...
# Subtest: onload skips protocol registration when the API is missing
ok 1618 - onload skips protocol registration when the API is missing
  ---
  duration_ms: 0.324069
  ...
# Subtest: registered protocol handler forwards params to handleGoToTaskUri
ok 1619 - registered protocol handler forwards params to handleGoToTaskUri
  ---
  duration_ms: 0.345941
  ...
# Subtest: handleGoToTaskUri maps a path through realpath when prefixes differ
ok 1620 - handleGoToTaskUri maps a path through realpath when prefixes differ
  ---
  duration_ms: 2.300132
  ...
# Subtest: cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
ok 1621 - cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
  ---
  duration_ms: 2.932902
  ...
# Subtest: findCancelLogParent finds a direct child but ignores a grandchild
ok 1622 - findCancelLogParent finds a direct child but ignores a grandchild
  ---
  duration_ms: 0.841827
  ...
# Subtest: getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
ok 1623 - getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
  ---
  duration_ms: 0.306185
  ...
# Subtest: formatCancelLogEntryText renders the exact preview text
ok 1624 - formatCancelLogEntryText renders the exact preview text
  ---
  duration_ms: 0.19932
  ...
# Subtest: planCancelLogEntry inserts a first-child log with tabs or spaces
ok 1625 - planCancelLogEntry inserts a first-child log with tabs or spaces
  ---
  duration_ms: 0.841126
  ...
# Subtest: planCancelLogEntry prepends under an existing log wherever it sits
ok 1626 - planCancelLogEntry prepends under an existing log wherever it sits
  ---
  duration_ms: 0.360278
  ...
# Subtest: planCancelLogEntry uses the fallback only when a marker exists
ok 1627 - planCancelLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.438668
  ...
# Subtest: isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
ok 1628 - isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
  ---
  duration_ms: 0.3929
  ...
# Subtest: describeCancelTaskRow covers single, counted, link, recurring, and hidden
ok 1629 - describeCancelTaskRow covers single, counted, link, recurring, and hidden
  ---
  duration_ms: 2.089029
  ...
# Subtest: planTaskCancelBatch cancels a single task with a first-child log
ok 1630 - planTaskCancelBatch cancels a single task with a first-child log
  ---
  duration_ms: 1.362833
  ...
# Subtest: planTaskCancelBatch upserts cancelled before the block id and preserves fields
ok 1631 - planTaskCancelBatch upserts cancelled before the block id and preserves fields
  ---
  duration_ms: 0.422237
  ...
# Subtest: planTaskCancelBatch records id-field task identities
ok 1632 - planTaskCancelBatch records id-field task identities
  ---
  duration_ms: 0.236441
  ...
# Subtest: planTaskCancelBatch skips closed targets and stays bottom-up
ok 1633 - planTaskCancelBatch skips closed targets and stays bottom-up
  ---
  duration_ms: 0.414732
  ...
# Subtest: planTaskCancelBatch refuses recurring targets in all three syntaxes
ok 1634 - planTaskCancelBatch refuses recurring targets in all three syntaxes
  ---
  duration_ms: 0.493443
  ...
# Subtest: planTaskCancelBatch handles empty reasons and stale preimages
ok 1635 - planTaskCancelBatch handles empty reasons and stale preimages
  ---
  duration_ms: 0.451071
  ...
# Subtest: planTaskCancelBatch preserves CRLF line endings
ok 1636 - planTaskCancelBatch preserves CRLF line endings
  ---
  duration_ms: 0.262401
  ...
# Subtest: cancel project conversion carries the log and reports it
ok 1637 - cancel project conversion carries the log and reports it
  ---
  duration_ms: 3.538308
  ...
# Subtest: getCancelTaskRowTitle names single, counted, and link sessions
ok 1638 - getCancelTaskRowTitle names single, counted, and link sessions
  ---
  duration_ms: 0.97382
  ...
# Subtest: getCancelReasonHints labels Enter per state and Esc as Keep open
ok 1639 - getCancelReasonHints labels Enter per state and Esc as Keep open
  ---
  duration_ms: 0.813193
  ...
# Subtest: the Cancel property item and the card's cancel row describe an open task
ok 1640 - the Cancel property item and the card's cancel row describe an open task
  ---
  duration_ms: 11.487148
  ...
# Subtest: Cancel row hides on closed tasks, plain bullets, and all-closed sessions
ok 1641 - Cancel row hides on closed tasks, plain bullets, and all-closed sessions
  ---
  duration_ms: 5.493663
  ...
# Subtest: Cancel row reports skipped closed targets in a counted session
ok 1642 - Cancel row reports skipped closed targets in a counted session
  ---
  duration_ms: 1.34017
  ...
# Subtest: the card refuses the cancel row on a recurring task and stays on the card
ok 1643 - the card refuses the cancel row on a recurring task and stays on the card
  ---
  duration_ms: 1.886312
  ...
# Subtest: cancel reason stage previews the typed, empty, fallback, and :: cases
ok 1644 - cancel reason stage previews the typed, empty, fallback, and :: cases
  ---
  duration_ms: 3.034395
  ...
# Subtest: cancel reason footer flips between plain, log, and fallback labels
ok 1645 - cancel reason footer flips between plain, log, and fallback labels
  ---
  duration_ms: 1.006934
  ...
# Subtest: Esc from the cancel reason stage writes nothing
ok 1646 - Esc from the cancel reason stage writes nothing
  ---
  duration_ms: 2.516416
  ...
# Subtest: single cancel writes [-], stamp, and first-child log in one transaction
ok 1647 - single cancel writes [-], stamp, and first-child log in one transaction
  ---
  duration_ms: 4.537706
  ...
# Subtest: empty reason writes no log unless one already exists
ok 1648 - empty reason writes no log unless one already exists
  ---
  duration_ms: 5.239888
  ...
# Subtest: stale single preimage refuses with nothing written
ok 1649 - stale single preimage refuses with nothing written
  ---
  duration_ms: 0.898696
  ...
# Subtest: cancel writes [-] with no NOW chip
ok 1650 - cancel writes [-] with no NOW chip
  ---
  duration_ms: 1.05783
  ...
# Subtest: TSC recovery runs with cancelled identities; a missing API still succeeds
ok 1651 - TSC recovery runs with cancelled identities; a missing API still succeeds
  ---
  duration_ms: 2.220601
  ...
# Subtest: a throwing TSC API is skipped silently with no chip
ok 1652 - a throwing TSC API is skipped silently with no chip
  ---
  duration_ms: 1.31392
  ...
# Subtest: counted cancel skips closed targets and reports them
ok 1653 - counted cancel skips closed targets and reports them
  ---
  duration_ms: 2.002745
  ...
# Subtest: same-file cancel folds today's Pomodoro prune into one transaction
ok 1654 - same-file cancel folds today's Pomodoro prune into one transaction
  ---
  duration_ms: 3.094871
  ...
# Subtest: link session cancels the target and removes the invoking link bullet
ok 1655 - link session cancels the target and removes the invoking link bullet
  ---
  duration_ms: 7.609972
  ...
# Subtest: buildCancelNoticeModel text covers every chip
ok 1656 - buildCancelNoticeModel text covers every chip
  ---
  duration_ms: 0.362131
  ...
# Subtest: renderCancelNoticeFragment builds the is-cancel card
ok 1657 - renderCancelNoticeFragment builds the is-cancel card
  ---
  duration_ms: 0.898737
  ...
# Subtest: isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
ok 1658 - isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
  ---
  duration_ms: 1.419411
  ...
# Subtest: findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
ok 1659 - findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
  ---
  duration_ms: 1.222716
  ...
# Subtest: collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
ok 1660 - collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
  ---
  duration_ms: 0.470208
  ...
# Subtest: planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
ok 1661 - planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
  ---
  duration_ms: 0.890301
  ...
# Subtest: planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
ok 1662 - planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
  ---
  duration_ms: 0.829674
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
ok 1663 - planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
  ---
  duration_ms: 0.803585
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
ok 1664 - planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
  ---
  duration_ms: 0.556102
  ...
# Subtest: planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
ok 1665 - planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
  ---
  duration_ms: 0.219149
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
ok 1666 - planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
  ---
  duration_ms: 0.801591
  ...
# Subtest: planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
ok 1667 - planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
  ---
  duration_ms: 0.626687
  ...
# Subtest: planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
ok 1668 - planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
  ---
  duration_ms: 0.563536
  ...
# Subtest: planDeferredPomodoroLinkCleanup preserves CRLF line endings
ok 1669 - planDeferredPomodoroLinkCleanup preserves CRLF line endings
  ---
  duration_ms: 0.276748
  ...
# Subtest: deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
ok 1670 - deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
  ---
  duration_ms: 0.30401
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks\#^x]] \#
ok 1671 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks\#^x]] \#
  ---
  duration_ms: 0.271649
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks\#^x|alias]] \#
ok 1672 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks\#^x|alias]] \#
  ---
  duration_ms: 0.168632
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks\#^x]]
ok 1673 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks\#^x]]
  ---
  duration_ms: 0.200282
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks\#^x]]
ok 1674 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks\#^x]]
  ---
  duration_ms: 0.153343
  ...
# Subtest: dedicated decoration check accepts paired strikes but cleanup never removes struck links
ok 1675 - dedicated decoration check accepts paired strikes but cleanup never removes struck links
  ---
  duration_ms: 0.299462
  ...
# Subtest: cleanup deletes only touched childless entries, preserving prose, placeholders and closed history
ok 1676 - cleanup deletes only touched childless entries, preserving prose, placeholders and closed history
  ---
  duration_ms: 0.337625
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\n", final newline false)
ok 1677 - cleanup handles adjacent EOF entries ("\\n", final newline false)
  ---
  duration_ms: 0.202928
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\n", final newline true)
ok 1678 - cleanup handles adjacent EOF entries ("\\n", final newline true)
  ---
  duration_ms: 0.185644
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\r\\n", final newline false)
ok 1679 - cleanup handles adjacent EOF entries ("\\r\\n", final newline false)
  ---
  duration_ms: 0.149355
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\r\\n", final newline true)
ok 1680 - cleanup handles adjacent EOF entries ("\\r\\n", final newline true)
  ---
  duration_ms: 0.147232
  ...
# Subtest: counted dependencies converge mixed sources and maintain one link per parent
ok 1681 - counted dependencies converge mixed sources and maintain one link per parent
  ---
  duration_ms: 10.951608
  ...
# Subtest: counted and single dependency gestures refuse inside a blockquote (DP29)
ok 1682 - counted and single dependency gestures refuse inside a blockquote (DP29)
  ---
  duration_ms: 0.427987
  ...
# Subtest: counted dependency candidates exclude every source and expose mixed state
ok 1683 - counted dependency candidates exclude every source and expose mixed state
  ---
  duration_ms: 0.877085
  ...
# Subtest: counted dependency block-ID prompting is planned atomically
ok 1684 - counted dependency block-ID prompting is planned atomically
  ---
  duration_ms: 1.757265
  ...
# Subtest: counted dependency runtime applies target, parents, and navigation in one undo group
ok 1685 - counted dependency runtime applies target, parents, and navigation in one undo group
  ---
  duration_ms: 6.117244
  ...
# Subtest: counted Depends-on removal recovers residents with [unblocked::]
ok 1686 - counted Depends-on removal recovers residents with [unblocked::]
  ---
  duration_ms: 4.016993
  ...
# Subtest: counted Depends-on removal writes [unblocked::] through the wired freshness API
ok 1687 - counted Depends-on removal writes [unblocked::] through the wired freshness API
  ---
  duration_ms: 4.092987
  ...
# Subtest: cross-file toggle changes only the source link
ok 1688 - cross-file toggle changes only the source link
  ---
  duration_ms: 1.669449
  ...
# Subtest: cross-file write failure still toggles only the source link
ok 1689 - cross-file write failure still toggles only the source link
  ---
  duration_ms: 0.608773
  ...
# Subtest: line-local fallback applies bottom-up and preserves CRLF
ok 1690 - line-local fallback applies bottom-up and preserves CRLF
  ---
  duration_ms: 0.810508
  ...
# Subtest: source line-count invariant rejects embedded newline changes
ok 1691 - source line-count invariant rejects embedded newline changes
  ---
  duration_ms: 0.211234
  ...
# Subtest: pure toggle refuses when the source changed under it
ok 1692 - pure toggle refuses when the source changed under it
  ---
  duration_ms: 0.15681
  ...
# Subtest: counted transclusion toggle evaluates each line independently
ok 1693 - counted transclusion toggle evaluates each line independently
  ---
  duration_ms: 0.377601
  ...
# Subtest: transclusion toggle is refused on Depends-On lines
ok 1694 - transclusion toggle is refused on Depends-On lines
  ---
  duration_ms: 0.289292
  ...
# Subtest: legacy sole-link children toggle purely, without field or status writes
ok 1695 - legacy sole-link children toggle purely, without field or status writes
  ---
  duration_ms: 0.42398
  ...
# Subtest: Ctrl+D on the Depends on row clears the line, field, and legacy children
ok 1696 - Ctrl+D on the Depends on row clears the line, field, and legacy children
  ---
  duration_ms: 2.804966
  ...
# Subtest: Ctrl+D clears a field-only dependency without a line
ok 1697 - Ctrl+D clears a field-only dependency without a line
  ---
  duration_ms: 1.979861
  ...
# Subtest: counted Ctrl+D on the Depends on row clears every targeted task
ok 1698 - counted Ctrl+D on the Depends on row clears every targeted task
  ---
  duration_ms: 2.40874
  ...
# Subtest: findRemovedLineText reports deleted lines
ok 1699 - findRemovedLineText reports deleted lines
  ---
  duration_ms: 0.147331
  ...
# Subtest: hand-edit mirror projects an edited line into the field
ok 1700 - hand-edit mirror projects an edited line into the field
  ---
  duration_ms: 1.61235
  ...
# Subtest: hand-edit mirror canonicalises a hand-written line variant
ok 1701 - hand-edit mirror canonicalises a hand-written line variant
  ---
  duration_ms: 0.869922
  ...
# Subtest: hand-edit mirror drops a linkless line and the field
ok 1702 - hand-edit mirror drops a linkless line and the field
  ---
  duration_ms: 1.381108
  ...
# Subtest: hand-edit mirror clears the field after the line is deleted
ok 1703 - hand-edit mirror clears the field after the line is deleted
  ---
  duration_ms: 1.260878
  ...
# Subtest: hand-edit mirror leaves malformed lines alone
ok 1704 - hand-edit mirror leaves malformed lines alone
  ---
  duration_ms: 0.32413
  ...
# Subtest: hand-edit mirror leaves legacy-only children for the hooks
ok 1705 - hand-edit mirror leaves legacy-only children for the hooks
  ---
  duration_ms: 0.421154
  ...
# Subtest: hand-edit mirror blocks when an open prerequisite is added by hand
ok 1706 - hand-edit mirror blocks when an open prerequisite is added by hand
  ---
  duration_ms: 0.942811
  ...
# Subtest: hand-edit mirror never transfers commitment to the target
ok 1707 - hand-edit mirror never transfers commitment to the target
  ---
  duration_ms: 0.917092
  ...
# Subtest: hand-edit mirror recovers when the last open prerequisite is removed by hand
ok 1708 - hand-edit mirror recovers when the last open prerequisite is removed by hand
  ---
  duration_ms: 1.084101
  ...
# Subtest: hand-edit mirror leaves a half-typed link alone
ok 1709 - hand-edit mirror leaves a half-typed link alone
  ---
  duration_ms: 0.301827
  ...
# Subtest: hand-edit mirror clears the owning task when its last-child line is deleted
ok 1710 - hand-edit mirror clears the owning task when its last-child line is deleted
  ---
  duration_ms: 1.043002
  ...
# Subtest: mirror scheduler debounces at the contract interval
ok 1711 - mirror scheduler debounces at the contract interval
  ---
  duration_ms: 0.900039
  ...
# Subtest: mirror scheduler seeds the baseline from the update start state
ok 1712 - mirror scheduler seeds the baseline from the update start state
  ---
  duration_ms: 1.639702
  ...
# Subtest: mirror scheduler keeps the first baseline and maps the owner across a burst
ok 1713 - mirror scheduler keeps the first baseline and maps the owner across a burst
  ---
  duration_ms: 0.594676
  ...
# Subtest: mirror listener runs clear-field for a first-edit deletion with a following sibling
ok 1714 - mirror listener runs clear-field for a first-edit deletion with a following sibling
  ---
  duration_ms: 10.809514
  ...
# Subtest: mirror fire re-arms while the cursor stays on the edited line
ok 1715 - mirror fire re-arms while the cursor stays on the edited line
  ---
  duration_ms: 2.239808
  ...
# Subtest: mirror scheduler reads changed ranges from the CM6 update
ok 1716 - mirror scheduler reads changed ranges from the CM6 update
  ---
  duration_ms: 0.249636
  ...
# Subtest: mirror scheduler skips IME composition
ok 1717 - mirror scheduler skips IME composition
  ---
  duration_ms: 0.197938
  ...
# Subtest: mirror scheduler skips open modals
ok 1718 - mirror scheduler skips open modals
  ---
  duration_ms: 0.177309
  ...
# Subtest: counted Ctrl+D clears every targeted task in one transaction with one notice
ok 1719 - counted Ctrl+D clears every targeted task in one transaction with one notice
  ---
  duration_ms: 4.190864
  ...
# Subtest: counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
ok 1720 - counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
  ---
  duration_ms: 1.530713
  ...
# Subtest: counted N! on only a Depends-On line refuses without writing
ok 1721 - counted N! on only a Depends-On line refuses without writing
  ---
  duration_ms: 0.244447
  ...
# Subtest: promotion targets enumerate real tasks and assign stable IDs
ok 1722 - promotion targets enumerate real tasks and assign stable IDs
  ---
  duration_ms: 5.699586
  ...
# Subtest: promotion file planner expands live links and preserves history
ok 1723 - promotion file planner expands live links and preserves history
  ---
  duration_ms: 5.442675
  ...
# Subtest: promotion file planner handles forms, whitespace, and subtrees
ok 1724 - promotion file planner handles forms, whitespace, and subtrees
  ---
  duration_ms: 1.532848
  ...
# Subtest: promotion file planner keeps compatibility for non-live references
ok 1725 - promotion file planner keeps compatibility for non-live references
  ---
  duration_ms: 0.952459
  ...
# Subtest: forward promotion expands live links, persists anchors, and removes the source
ok 1726 - forward promotion expands live links, persists anchors, and removes the source
  ---
  duration_ms: 8.977865
  ...
# Subtest: forward promotion uses zero-task fallback and keeps reverse one-to-one
ok 1727 - forward promotion uses zero-task fallback and keeps reverse one-to-one
  ---
  duration_ms: 1.100381
  ...
# Subtest: forward promotion retains the source on ambiguous, stale, and write failures
ok 1728 - forward promotion retains the source on ambiguous, stale, and write failures
  ---
  duration_ms: 1.134366
  ...
# Subtest: forward promotion discovers live links without a backlink cache and uses one open-editor write
ok 1729 - forward promotion discovers live links without a backlink cache and uses one open-editor write
  ---
  duration_ms: 2.147993
  ...
# Subtest: forward conversion carries a Depends-On line and reverse restores it
not ok 1730 - forward conversion carries a Depends-On line and reverse restores it
  ---
  duration_ms: 18.140999
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
ok 1731 - planTaskLaneBatch commits every Ready target to Next
  ---
  duration_ms: 3.155387
  ...
# Subtest: planTaskLaneBatch releases Next and In Progress to Ready
ok 1732 - planTaskLaneBatch releases Next and In Progress to Ready
  ---
  duration_ms: 0.52348
  ...
# Subtest: planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
ok 1733 - planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
  ---
  duration_ms: 0.819615
  ...
# Subtest: planTaskLaneBatch skips Blocked and refuses stale preimages
ok 1734 - planTaskLaneBatch skips Blocked and refuses stale preimages
  ---
  duration_ms: 0.298991
  ...
# Subtest: buildLaneToggleNotice reports commit and release with and without budgets
ok 1735 - buildLaneToggleNotice reports commit and release with and without budgets
  ---
  duration_ms: 0.358966
  ...
# Subtest: describeLaneRow covers task, counted, and link sessions
ok 1736 - describeLaneRow covers task, counted, and link sessions
  ---
  duration_ms: 0.507839
  ...
# Subtest: toggleTaskLane commits Ready to Next and reports lane budgets
ok 1737 - toggleTaskLane commits Ready to Next and reports lane budgets
  ---
  duration_ms: 3.114418
  ...
# Subtest: toggleTaskLane releases to Ready without the api
ok 1738 - toggleTaskLane releases to Ready without the api
  ---
  duration_ms: 1.360218
  ...
# Subtest: toggleTaskLane release logs the summary on In Progress tasks
ok 1739 - toggleTaskLane release logs the summary on In Progress tasks
  ---
  duration_ms: 1.282589
  ...
# Subtest: toggleTaskLane skips Blocked targets
ok 1740 - toggleTaskLane skips Blocked targets
  ---
  duration_ms: 0.825898
  ...
# Subtest: counted toggleTaskLane covers the current task plus the next N tasks
ok 1741 - counted toggleTaskLane covers the current task plus the next N tasks
  ---
  duration_ms: 0.548057
  ...
# Subtest: toggleTaskLane on a Task Link writes through the open buffer
ok 1742 - toggleTaskLane on a Task Link writes through the open buffer
  ---
  duration_ms: 4.070415
  ...
# Subtest: toggleTaskLane on Task Links releases across notes
ok 1743 - toggleTaskLane on Task Links releases across notes
  ---
  duration_ms: 1.347243
  ...
# Subtest: toggleTaskLane refuses when a preimage changed
ok 1744 - toggleTaskLane refuses when a preimage changed
  ---
  duration_ms: 0.210091
  ...
# Subtest: Ctrl+Shift+P shows a pinned lane row that commits immediately
ok 1745 - Ctrl+Shift+P shows a pinned lane row that commits immediately
  ---
  duration_ms: 12.233673
  ...
# Subtest: Ctrl+Shift+P link mode shows the lane row with release detail
ok 1746 - Ctrl+Shift+P link mode shows the lane row with release detail
  ---
  duration_ms: 4.82732
  ...
# Subtest: Ctrl+Shift+P lane release with In Progress goes through the reason stage
ok 1747 - Ctrl+Shift+P lane release with In Progress goes through the reason stage
  ---
  duration_ms: 2.465499
  ...
# Subtest: getLinkPickerSessionSubtitle keeps the clamp for a single link
ok 1748 - getLinkPickerSessionSubtitle keeps the clamp for a single link
  ---
  duration_ms: 0.14169
  ...
# Subtest: link-mode priority notice keeps via Task Links visible
ok 1749 - link-mode priority notice keeps via Task Links visible
  ---
  duration_ms: 0.685319
  ...
# Subtest: already-handled Alt+N leaves Vim state alone
ok 1750 - already-handled Alt+N leaves Vim state alone
  ---
  duration_ms: 0.318067
  ...
# Subtest: Alt+N fallback still dispatches once with the Vim count
ok 1751 - Alt+N fallback still dispatches once with the Vim count
  ---
  duration_ms: 0.706579
  ...
# Subtest: lane release deletes an emptied entry (cross-file, Alt+N)
ok 1752 - lane release deletes an emptied entry (cross-file, Alt+N)
  ---
  duration_ms: 2.49208
  ...
# Subtest: lane release deletes an emptied entry (cross-file, card)
ok 1753 - lane release deletes an emptied entry (cross-file, card)
  ---
  duration_ms: 2.311365
  ...
# Subtest: lane release deletes an emptied entry (same-file, Alt+N)
ok 1754 - lane release deletes an emptied entry (same-file, Alt+N)
  ---
  duration_ms: 2.343496
  ...
# Subtest: lane release deletes an emptied entry (same-file, card)
ok 1755 - lane release deletes an emptied entry (same-file, card)
  ---
  duration_ms: 3.136671
  ...
# Subtest: Task Link release deletes its entry in one undo group (separate, Alt+N)
ok 1756 - Task Link release deletes its entry in one undo group (separate, Alt+N)
  ---
  duration_ms: 1.582422
  ...
# Subtest: Task Link release deletes its entry in one undo group (separate, card)
ok 1757 - Task Link release deletes its entry in one undo group (separate, card)
  ---
  duration_ms: 3.882145
  ...
# Subtest: Task Link release deletes its entry in one undo group (folded, Alt+N)
ok 1758 - Task Link release deletes its entry in one undo group (folded, Alt+N)
  ---
  duration_ms: 1.237774
  ...
# Subtest: Task Link release deletes its entry in one undo group (folded, card)
ok 1759 - Task Link release deletes its entry in one undo group (folded, card)
  ---
  duration_ms: 3.04213
  ...
# Subtest: parseLinkPickerTaskLink recognizes dedicated Task Link bullets
ok 1760 - parseLinkPickerTaskLink recognizes dedicated Task Link bullets
  ---
  duration_ms: 2.302417
  ...
# Subtest: discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
ok 1761 - discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
  ---
  duration_ms: 1.400024
  ...
# Subtest: discoverLinkPickerTargets leaves \#task lines to the regular picker
ok 1762 - discoverLinkPickerTargets leaves \#task lines to the regular picker
  ---
  duration_ms: 0.294713
  ...
# Subtest: findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
ok 1763 - findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
  ---
  duration_ms: 0.459268
  ...
# Subtest: createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
ok 1764 - createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
  ---
  duration_ms: 1.669248
  ...
# Subtest: getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
ok 1765 - getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
  ---
  duration_ms: 0.587963
  ...
# Subtest: bare link mode edits the task behind a Task Link through the open buffer
ok 1766 - bare link mode edits the task behind a Task Link through the open buffer
  ---
  duration_ms: 15.809687
  ...
# Subtest: counted link mode writes across notes through both the open buffer and the vault
ok 1767 - counted link mode writes across notes through both the open buffer and the vault
  ---
  duration_ms: 4.33514
  ...
# Subtest: Task Link scheduled delete recovers a Blocked task through the wired freshness API
ok 1768 - Task Link scheduled delete recovers a Blocked task through the wired freshness API
  ---
  duration_ms: 6.473542
  ...
# Subtest: link mode refuses the whole operation when a linked note changed
ok 1769 - link mode refuses the whole operation when a linked note changed
  ---
  duration_ms: 3.606908
  ...
# Subtest: link mode reports a closed target and changes nothing
ok 1770 - link mode reports a closed target and changes nothing
  ---
  duration_ms: 1.244828
  ...
# Subtest: link mode defers to a future date, blocks the task, and prunes today
ok 1771 - link mode defers to a future date, blocks the task, and prunes today
  ---
  duration_ms: 10.394954
  ...
# Subtest: bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
ok 1772 - bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
  ---
  duration_ms: 2.561843
  ...
# Subtest: Task Link scheduled write deletes its entry (separate)
ok 1773 - Task Link scheduled write deletes its entry (separate)
  ---
  duration_ms: 3.986855
  ...
# Subtest: Task Link scheduled write deletes its entry (folded)
ok 1774 - Task Link scheduled write deletes its entry (folded)
  ---
  duration_ms: 3.931008
  ...
# Subtest: folded Task Link scheduling maps the cursor past logs inserted before the emptied entry
ok 1775 - folded Task Link scheduling maps the cursor past logs inserted before the emptied entry
  ---
  duration_ms: 7.211253
  ...
# Subtest: dash restore suppresses editor notice after deliberate navigation
ok 1776 - dash restore suppresses editor notice after deliberate navigation
  ---
  duration_ms: 22.255935
  ...
# Subtest: open-task dispatch timeout is registered for plugin cleanup
ok 1777 - open-task dispatch timeout is registered for plugin cleanup
  ---
  duration_ms: 0.591921
  ...
# Subtest: jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
ok 1778 - jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
  ---
  duration_ms: 5.27221
  ...
# Subtest: jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
ok 1779 - jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
  ---
  duration_ms: 1.393952
  ...
# Subtest: jumpToOpenObsidianTask keeps current-swap transaction failures local
ok 1780 - jumpToOpenObsidianTask keeps current-swap transaction failures local
  ---
  duration_ms: 0.842168
  ...
# Subtest: jumpToOpenObsidianTask refuses current-up without jumping or mutating
ok 1781 - jumpToOpenObsidianTask refuses current-up without jumping or mutating
  ---
  duration_ms: 0.537236
  ...
# Subtest: jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
ok 1782 - jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
  ---
  duration_ms: 2.220711
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
ok 1783 - Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
  ---
  duration_ms: 0.784298
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
ok 1784 - Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
  ---
  duration_ms: 0.87934
  ...
# Subtest: counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
ok 1785 - counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
  ---
  duration_ms: 1.325261
  ...
# Subtest: an impossible counted Pomodoro move refuses without jumping or mutating
ok 1786 - an impossible counted Pomodoro move refuses without jumping or mutating
  ---
  duration_ms: 0.540583
  ...
# Subtest: counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
ok 1787 - counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
  ---
  duration_ms: 1.033344
  ...
# Subtest: counted open-task jump on a sole current target keeps the existing notice
ok 1788 - counted open-task jump on a sole current target keeps the existing notice
  ---
  duration_ms: 0.224498
  ...
# Subtest: dispatch guard allows exactly one counted Pomodoro move when the command route also fires
ok 1789 - dispatch guard allows exactly one counted Pomodoro move when the command route also fires
  ---
  duration_ms: 0.863509
  ...
# Subtest: bullet property picker reconciles duplicate bare and counted opens
ok 1790 - bullet property picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 13.100492
  ...
# Subtest: bullet property picker close lifecycle clears tracking for fresh sessions
ok 1791 - bullet property picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 8.407936
  ...
# Subtest: task move picker reconciles duplicate bare and counted opens
ok 1792 - task move picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 2.909868
  ...
# Subtest: task move picker close lifecycle clears tracking for fresh sessions
ok 1793 - task move picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 1.122434
  ...
# Subtest: Pomodoro bullet move picker opens sessions and clears the shared move picker slot
ok 1794 - Pomodoro bullet move picker opens sessions and clears the shared move picker slot
  ---
  duration_ms: 2.775291
  ...
# Subtest: Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
ok 1795 - Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
  ---
  duration_ms: 0.773407
  ...
# Subtest: move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
ok 1796 - move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
  ---
  duration_ms: 1.295284
  ...
# Subtest: commitPomodoroBulletMoveSession applies one guarded same-file transaction
ok 1797 - commitPomodoroBulletMoveSession applies one guarded same-file transaction
  ---
  duration_ms: 2.238976
  ...
# Subtest: Pomodoro bullet move picker confirms = through the actual picker callback
ok 1798 - Pomodoro bullet move picker confirms = through the actual picker callback
  ---
  duration_ms: 2.295815
  ...
# Subtest: Pomodoro bullet move picker reserves =NAME for peeling a named merged component
ok 1799 - Pomodoro bullet move picker reserves =NAME for peeling a named merged component
  ---
  duration_ms: 1.029948
  ...
# Subtest: Pomodoro bullet move picker confirms =email through the actual picker callback
ok 1800 - Pomodoro bullet move picker confirms =email through the actual picker callback
  ---
  duration_ms: 1.468325
  ...
# Subtest: Pomodoro bullet move picker confirms = review through the actual picker callback
ok 1801 - Pomodoro bullet move picker confirms = review through the actual picker callback
  ---
  duration_ms: 0.753219
  ...
# Subtest: Pomodoro bullet move picker confirms =focus by unnaming a single-name source
ok 1802 - Pomodoro bullet move picker confirms =focus by unnaming a single-name source
  ---
  duration_ms: 0.703243
  ...
# Subtest: Pomodoro bullet split stale-content guard does not write
ok 1803 - Pomodoro bullet split stale-content guard does not write
  ---
  duration_ms: 0.304912
  ...
# Subtest: Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
ok 1804 - Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
  ---
  duration_ms: 0.619643
  ...
# Subtest: native isOpen regression: pickers attach, close clears slot, reopen works
ok 1805 - native isOpen regression: pickers attach, close clears slot, reopen works
  ---
  duration_ms: 2.737118
  ...
# Subtest: stale registered pickers fail open on the next key
ok 1806 - stale registered pickers fail open on the next key
  ---
  duration_ms: 2.211074
  ...
# Subtest: planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
ok 1807 - planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
  ---
  duration_ms: 4.348095
  ...
# Subtest: planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
ok 1808 - planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
  ---
  duration_ms: 0.61298
  ...
# Subtest: planPomodoroBulletMove preserves the source when only some siblings move out
ok 1809 - planPomodoroBulletMove preserves the source when only some siblings move out
  ---
  duration_ms: 0.315653
  ...
# Subtest: planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
ok 1810 - planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
  ---
  duration_ms: 0.395295
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
ok 1811 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
  ---
  duration_ms: 0.728521
  ...
# Subtest: planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
ok 1812 - planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
  ---
  duration_ms: 1.029316
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
ok 1813 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
  ---
  duration_ms: 0.591049
  ...
# Subtest: planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
ok 1814 - planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
  ---
  duration_ms: 0.410244
  ...
# Subtest: planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
ok 1815 - planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
  ---
  duration_ms: 0.691691
  ...
# Subtest: planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
ok 1816 - planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
  ---
  duration_ms: 1.117835
  ...
# Subtest: planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
ok 1817 - planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
  ---
  duration_ms: 0.368604
  ...
# Subtest: planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
ok 1818 - planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
  ---
  duration_ms: 0.284423
  ...
# Subtest: planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
ok 1819 - planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
  ---
  duration_ms: 0.480247
  ...
# Subtest: planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
ok 1820 - planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
  ---
  duration_ms: 0.471581
  ...
# Subtest: planPomodoroBulletMove deletes both open and closed source entries the same way
ok 1821 - planPomodoroBulletMove deletes both open and closed source entries the same way
  ---
  duration_ms: 0.503752
  ...
# Subtest: planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
ok 1822 - planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
  ---
  duration_ms: 0.395595
  ...
# Subtest: planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
ok 1823 - planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
  ---
  duration_ms: 0.446483
  ...
# Subtest: planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
ok 1824 - planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
  ---
  duration_ms: 0.642057
  ...
# Subtest: planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
ok 1825 - planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
  ---
  duration_ms: 0.37169
  ...
# Subtest: planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
ok 1826 - planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
  ---
  duration_ms: 0.590378
  ...
# Subtest: planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
ok 1827 - planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
  ---
  duration_ms: 0.389003
  ...
# Subtest: planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
ok 1828 - planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
  ---
  duration_ms: 0.40835
  ...
# Subtest: planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
ok 1829 - planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
  ---
  duration_ms: 0.280435
  ...
# Subtest: planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
ok 1830 - planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
  ---
  duration_ms: 0.396267
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
ok 1831 - planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
  ---
  duration_ms: 0.210051
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
ok 1832 - planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
  ---
  duration_ms: 0.440852
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
ok 1833 - planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
  ---
  duration_ms: 3.301035
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
ok 1834 - planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
  ---
  duration_ms: 0.546053
  ...
# Subtest: Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
ok 1835 - Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
  ---
  duration_ms: 7.39984
  ...
# Subtest: commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
ok 1836 - commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
  ---
  duration_ms: 3.58112
  ...
# Subtest: commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
ok 1837 - commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
  ---
  duration_ms: 1.151569
  ...
# Subtest: commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
ok 1838 - commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
  ---
  duration_ms: 0.478494
  ...
# Subtest: commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
ok 1839 - commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
  ---
  duration_ms: 0.393571
  ...
# Subtest: Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
ok 1840 - Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
  ---
  duration_ms: 6.333737
  ...
# Subtest: Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
ok 1841 - Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
  ---
  duration_ms: 0.80074
  ...
# Subtest: Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
ok 1842 - Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
  ---
  duration_ms: 0.742949
  ...
# Subtest: Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
ok 1843 - Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
  ---
  duration_ms: 1.144225
  ...
# Subtest: task move picker closes before commit while other pickers retain delayed close
ok 1844 - task move picker closes before commit while other pickers retain delayed close
  ---
  duration_ms: 0.872497
  ...
# Subtest: parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
ok 1845 - parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
  ---
  duration_ms: 2.111622
  ...
# Subtest: normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
ok 1846 - normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
  ---
  duration_ms: 0.384093
  ...
# Subtest: formatPomodoroEntryLine emits a placeholder entry with or without a name
ok 1847 - formatPomodoroEntryLine emits a placeholder entry with or without a name
  ---
  duration_ms: 0.123146
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
ok 1848 - createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
  ---
  duration_ms: 2.040548
  ...
# Subtest: createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
ok 1849 - createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
  ---
  duration_ms: 0.818784
  ...
# Subtest: createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
ok 1850 - createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
  ---
  duration_ms: 0.627399
  ...
# Subtest: createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
ok 1851 - createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
  ---
  duration_ms: 0.648408
  ...
# Subtest: buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
ok 1852 - buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
  ---
  duration_ms: 0.243795
  ...
# Subtest: buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
ok 1853 - buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
  ---
  duration_ms: 0.42945
  ...
# Subtest: createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
ok 1854 - createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
  ---
  duration_ms: 0.632347
  ...
# Subtest: createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
ok 1855 - createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
  ---
  duration_ms: 0.330451
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
ok 1856 - createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
  ---
  duration_ms: 0.343927
  ...
# Subtest: collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
ok 1857 - collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
  ---
  duration_ms: 0.426905
  ...
# Subtest: findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
ok 1858 - findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
  ---
  duration_ms: 0.497009
  ...
# Subtest: findPomodoroBulletContext leaves plain \#task lines on the task-move route
ok 1859 - findPomodoroBulletContext leaves plain \#task lines on the task-move route
  ---
  duration_ms: 0.310784
  ...
# Subtest: discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
ok 1860 - discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
  ---
  duration_ms: 0.767085
  ...
# Subtest: findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
ok 1861 - findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
  ---
  duration_ms: 0.713463
  ...
# Subtest: discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
ok 1862 - discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
  ---
  duration_ms: 0.850915
  ...
# Subtest: isMovablePomodoroEntryContext matches open current and future Pomodoro entries
ok 1863 - isMovablePomodoroEntryContext matches open current and future Pomodoro entries
  ---
  duration_ms: 3.192017
  ...
# Subtest: planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
ok 1864 - planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
  ---
  duration_ms: 0.813133
  ...
# Subtest: planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
ok 1865 - planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
  ---
  duration_ms: 0.333888
  ...
# Subtest: planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
ok 1866 - planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
  ---
  duration_ms: 0.405715
  ...
# Subtest: planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
ok 1867 - planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
  ---
  duration_ms: 0.435271
  ...
# Subtest: planPomodoroEntryReorder handles counted current swaps and their inverses
ok 1868 - planPomodoroEntryReorder handles counted current swaps and their inverses
  ---
  duration_ms: 0.551684
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
ok 1869 - planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
  ---
  duration_ms: 0.322465
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
ok 1870 - planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
  ---
  duration_ms: 0.305343
  ...
# Subtest: planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
ok 1871 - planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
  ---
  duration_ms: 0.690198
  ...
# Subtest: planPomodoroEntryReorder round-trips a future-up swap across the current open entry
ok 1872 - planPomodoroEntryReorder round-trips a future-up swap across the current open entry
  ---
  duration_ms: 0.788035
  ...
# Subtest: planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
ok 1873 - planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
  ---
  duration_ms: 0.738741
  ...
# Subtest: planPomodoroEntryReorder refuses moving down past the last placeholder in the section
ok 1874 - planPomodoroEntryReorder refuses moving down past the last placeholder in the section
  ---
  duration_ms: 0.286918
  ...
# Subtest: planPomodoroEntryReorder refuses both directions for a lone placeholder
ok 1875 - planPomodoroEntryReorder refuses both directions for a lone placeholder
  ---
  duration_ms: 0.238566
  ...
# Subtest: planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
ok 1876 - planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
  ---
  duration_ms: 0.191055
  ...
# Subtest: planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
ok 1877 - planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
  ---
  duration_ms: 0.317016
  ...
# Subtest: planPomodoroEntryReorder refuses illegal current/future spans atomically
ok 1878 - planPomodoroEntryReorder refuses illegal current/future spans atomically
  ---
  duration_ms: 1.373874
  ...
# Subtest: planPomodoroEntryReorder rejects a stale source line
ok 1879 - planPomodoroEntryReorder rejects a stale source line
  ---
  duration_ms: 0.21455
  ...
# Subtest: planPomodoroEntryReorder round-trips CRLF content
ok 1880 - planPomodoroEntryReorder round-trips CRLF content
  ---
  duration_ms: 0.334368
  ...
# Subtest: planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
ok 1881 - planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
  ---
  duration_ms: 0.247904
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
ok 1882 - planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
  ---
  duration_ms: 0.378012
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up three positions and round-trips
ok 1883 - planPomodoroEntryReorder moves a placeholder up three positions and round-trips
  ---
  duration_ms: 0.5235
  ...
# Subtest: planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
ok 1884 - planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
  ---
  duration_ms: 0.261329
  ...
# Subtest: planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
ok 1885 - planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
  ---
  duration_ms: 0.728832
  ...
# Subtest: planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
ok 1886 - planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
  ---
  duration_ms: 1.004098
  ...
# Subtest: planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
ok 1887 - planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
  ---
  duration_ms: 0.493883
  ...
# Subtest: peelPomodoroMergedName removes every matching canonical plus component
ok 1888 - peelPomodoroMergedName removes every matching canonical plus component
  ---
  duration_ms: 1.711919
  ...
# Subtest: planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
ok 1889 - planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
  ---
  duration_ms: 3.928432
  ...
# Subtest: planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
ok 1890 - planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
  ---
  duration_ms: 0.710216
  ...
# Subtest: planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
ok 1891 - planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
  ---
  duration_ms: 0.746085
  ...
# Subtest: planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
ok 1892 - planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
  ---
  duration_ms: 0.98453
  ...
# Subtest: planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
ok 1893 - planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
  ---
  duration_ms: 1.343326
  ...
# Subtest: planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
ok 1894 - planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
  ---
  duration_ms: 0.758178
  ...
# Subtest: planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
ok 1895 - planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
  ---
  duration_ms: 1.364627
  ...
# Subtest: Pomodoro bullet move picker typing =NAME or Escape does not write
ok 1896 - Pomodoro bullet move picker typing =NAME or Escape does not write
  ---
  duration_ms: 2.494745
  ...
# Subtest: planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
ok 1897 - planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
  ---
  duration_ms: 0.566582
  ...
# Subtest: planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
ok 1898 - planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
  ---
  duration_ms: 0.325943
  ...
# Subtest: planPomodoroEntryRename reports unchanged when the normalized name matches the current name
ok 1899 - planPomodoroEntryRename reports unchanged when the normalized name matches the current name
  ---
  duration_ms: 0.177559
  ...
# Subtest: planPomodoroEntryRename rejects unsupported trailing content and a stale source line
ok 1900 - planPomodoroEntryRename rejects unsupported trailing content and a stale source line
  ---
  duration_ms: 0.199521
  ...
# Subtest: planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
ok 1901 - planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
  ---
  duration_ms: 0.171076
  ...
# Subtest: planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
ok 1902 - planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
  ---
  duration_ms: 1.848551
  ...
# Subtest: planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
ok 1903 - planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
  ---
  duration_ms: 1.191205
  ...
# Subtest: planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
ok 1904 - planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
  ---
  duration_ms: 0.678977
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: priority notice relative day helpers handle offsets ranges and icons
ok 1905 - priority notice relative day helpers handle offsets ranges and icons
  ---
  duration_ms: 1.620394
  ...
# Subtest: priority notice model summarizes single counted and project writes
ok 1906 - priority notice model summarizes single counted and project writes
  ---
  duration_ms: 3.966686
  ...
# Subtest: priority notice renderer builds an accessible fragment
ok 1907 - priority notice renderer builds an accessible fragment
  ---
  duration_ms: 2.599856
  ...
# Subtest: priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
ok 1908 - priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
  ---
  duration_ms: 11.053973
  ...
# Subtest: priority notice falls back to one plain notice without a DOM
ok 1909 - priority notice falls back to one plain notice without a DOM
  ---
  duration_ms: 0.723993
  ...
# Subtest: priority notice falls back to plain text when fragment rendering fails
ok 1910 - priority notice falls back to plain text when fragment rendering fails
  ---
  duration_ms: 0.454307
  ...
# Subtest: priority scheduling rolls inclusively and clamps a random value of one
ok 1911 - priority scheduling rolls inclusively and clamps a random value of one
  ---
  duration_ms: 0.662004
  ...
# Subtest: priority value rows preserve config order and expose labels ranges and current state
ok 1912 - priority value rows preserve config order and expose labels ranges and current state
  ---
  duration_ms: 1.048403
  ...
# Subtest: priority picker writes priority then rolled schedule in one guarded edit
ok 1913 - priority picker writes priority then rolled schedule in one guarded edit
  ---
  duration_ms: 17.116129
  ...
# Subtest: priority picker writes lowest priority with a wide rolled schedule
ok 1914 - priority picker writes lowest priority with a wide rolled schedule
  ---
  duration_ms: 3.341352
  ...
# Subtest: priority picker replaces both existing values without duplicating fields
ok 1915 - priority picker replaces both existing values without duplicating fields
  ---
  duration_ms: 3.84303
  ...
# Subtest: counted priority writes keep the rolled date right of the priority
ok 1916 - counted priority writes keep the rolled date right of the priority
  ---
  duration_ms: 6.873338
  ...
# Subtest: priority picker writes project priority and schedule inline atomically
ok 1917 - priority picker writes project priority and schedule inline atomically
  ---
  duration_ms: 6.550932
  ...
# Subtest: counted priority picker rolls an independent schedule for every task
ok 1918 - counted priority picker rolls an independent schedule for every task
  ---
  duration_ms: 5.638088
  ...
# Subtest: counted priority planning keeps project schedules inline
ok 1919 - counted priority planning keeps project schedules inline
  ---
  duration_ms: 1.312176
  ...
# Subtest: counted priority planning evaluates Blocked recovery per rolled date
ok 1920 - counted priority planning evaluates Blocked recovery per rolled date
  ---
  duration_ms: 1.305332
  ...
# Subtest: a counted priority batch writes one entry per task using each task's own previous level
ok 1921 - a counted priority batch writes one entry per task using each task's own previous level
  ---
  duration_ms: 5.529259
  ...
# Subtest: priority notice models carry the stored level value for the glyph
ok 1922 - priority notice models carry the stored level value for the glyph
  ---
  duration_ms: 0.82709
  ...
# Subtest: ledger priority mark lookup guards version and render
ok 1923 - ledger priority mark lookup guards version and render
  ---
  duration_ms: 0.176597
  ...
# Subtest: priority notice header reuses the shared mark when available
ok 1924 - priority notice header reuses the shared mark when available
  ---
  duration_ms: 0.437345
  ...
# Subtest: priority notice keeps the Lucide icon without a usable mark api
ok 1925 - priority notice keeps the Lucide icon without a usable mark api
  ---
  duration_ms: 1.127434
  ...
# Subtest: a counted priority batch skips a task whose rolled date equals its current date
ok 1926 - a counted priority batch skips a task whose rolled date equals its current date
  ---
  duration_ms: 5.851446
  ...
# Subtest: counted priority runtime aborts a stale session without rolling writes
ok 1927 - counted priority runtime aborts a stale session without rolling writes
  ---
  duration_ms: 2.285305
  ...
# Subtest: scheduled picker pins a priority roll only for configured current priorities
ok 1928 - scheduled picker pins a priority roll only for configured current priorities
  ---
  duration_ms: 15.788917
  ...
# Subtest: Ctrl+R replaces only the pinned priority roll and keeps it selected
ok 1929 - Ctrl+R replaces only the pinned priority roll and keeps it selected
  ---
  duration_ms: 6.236089
  ...
# Subtest: choosing a priority roll writes immediately with a deterministic reason instead of prompting
ok 1930 - choosing a priority roll writes immediately with a deterministic reason instead of prompting
  ---
  duration_ms: 6.674398
  ...
# Subtest: counted scheduled picker requires one shared configured priority
ok 1931 - counted scheduled picker requires one shared configured priority
  ---
  duration_ms: 4.736607
  ...
# Subtest: buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
ok 1932 - buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
  ---
  duration_ms: 4.224499
  ...
# Subtest: buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
ok 1933 - buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
  ---
  duration_ms: 0.401206
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
ok 1934 - buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
  ---
  duration_ms: 0.566311
  ...
# Subtest: buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
ok 1935 - buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
  ---
  duration_ms: 0.428679
  ...
# Subtest: buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
ok 1936 - buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
  ---
  duration_ms: 0.589416
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
ok 1937 - buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
  ---
  duration_ms: 0.233857
  ...
# Subtest: buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
ok 1938 - buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
  ---
  duration_ms: 0.326353
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
ok 1939 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
  ---
  duration_ms: 0.507249
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child work log under the project task
ok 1940 - buildProjectSeedFromChildBullets moves a direct-child work log under the project task
  ---
  duration_ms: 0.459037
  ...
# Subtest: buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
ok 1941 - buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
  ---
  duration_ms: 0.609033
  ...
# Subtest: buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
ok 1942 - buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
  ---
  duration_ms: 0.365128
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
ok 1943 - buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
  ---
  duration_ms: 0.226733
  ...
# Subtest: buildProjectSeedFromChildBullets moves an empty work log without forcing task output
ok 1944 - buildProjectSeedFromChildBullets moves an empty work log without forcing task output
  ---
  duration_ms: 0.168942
  ...
# Subtest: buildProjectSeedFromChildBullets moves both logs in source order without sorting by kind
ok 1945 - buildProjectSeedFromChildBullets moves both logs in source order without sorting by kind
  ---
  duration_ms: 0.16771
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
ok 1946 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
  ---
  duration_ms: 0.359346
  ...
# Subtest: parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
ok 1947 - parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
  ---
  duration_ms: 0.350399
  ...
# Subtest: parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
ok 1948 - parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
  ---
  duration_ms: 0.223467
  ...
# Subtest: parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
ok 1949 - parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
  ---
  duration_ms: 0.672754
  ...
# Subtest: normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
ok 1950 - normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
  ---
  duration_ms: 0.125249
  ...
# Subtest: parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
ok 1951 - parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
  ---
  duration_ms: 0.146059
  ...
# Subtest: formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
ok 1952 - formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
  ---
  duration_ms: 0.161138
  ...
# Subtest: insertProjectSectionNotes fills an empty existing section with a blank line then the notes
ok 1953 - insertProjectSectionNotes fills an empty existing section with a blank line then the notes
  ---
  duration_ms: 0.846166
  ...
# Subtest: insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
ok 1954 - insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
  ---
  duration_ms: 0.237504
  ...
# Subtest: insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
ok 1955 - insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
  ---
  duration_ms: 0.199081
  ...
# Subtest: insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
ok 1956 - insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
  ---
  duration_ms: 0.307467
  ...
# Subtest: insertProjectSectionNotes does not add a trailing newline when the original content had none
ok 1957 - insertProjectSectionNotes does not add a trailing newline when the original content had none
  ---
  duration_ms: 0.185714
  ...
# Subtest: insertProjectSectionNotes preserves CRLF line endings for an existing section
ok 1958 - insertProjectSectionNotes preserves CRLF line endings for an existing section
  ---
  duration_ms: 0.248094
  ...
# Subtest: insertProjectSectionNotes creates a new section using the document's CRLF line ending
ok 1959 - insertProjectSectionNotes creates a new section using the document's CRLF line ending
  ---
  duration_ms: 0.173902
  ...
# Subtest: buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
ok 1960 - buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
  ---
  duration_ms: 0.247021
  ...
# Subtest: buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
ok 1961 - buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
  ---
  duration_ms: 0.458285
  ...
# Subtest: buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
ok 1962 - buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
  ---
  duration_ms: 0.159495
  ...
# Subtest: buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
ok 1963 - buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
  ---
  duration_ms: 1.563867
  ...
# Subtest: project conversion accepts blocked sources and extracts their managed dependency child
ok 1964 - project conversion accepts blocked sources and extracts their managed dependency child
  ---
  duration_ms: 2.813714
  ...
# Subtest: project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
ok 1965 - project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
  ---
  duration_ms: 1.530313
  ...
# Subtest: buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
ok 1966 - buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
  ---
  duration_ms: 0.495046
  ...
# Subtest: buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
ok 1967 - buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
  ---
  duration_ms: 0.301075
  ...
# Subtest: buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
ok 1968 - buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
  ---
  duration_ms: 0.280847
  ...
# Subtest: insertProjectManagedLogLines preserves CRLF line endings
ok 1969 - insertProjectManagedLogLines preserves CRLF line endings
  ---
  duration_ms: 0.208258
  ...
# Subtest: findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
ok 1970 - findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
  ---
  duration_ms: 0.269565
  ...
# Subtest: getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
ok 1971 - getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
  ---
  duration_ms: 0.27768
  ...
# Subtest: getProjectFromTaskNoticeText reports moved log kinds in a fixed order
ok 1972 - getProjectFromTaskNoticeText reports moved log kinds in a fixed order
  ---
  duration_ms: 0.158643
  ...
# Subtest: forward conversion leaves the project Ready when only the source status was Blocked
ok 1973 - forward conversion leaves the project Ready when only the source status was Blocked
  ---
  duration_ms: 0.4921
  ...
# Subtest: buildTaskBlockFromProjectNote restores the worked example and round-trips
ok 1974 - buildTaskBlockFromProjectNote restores the worked example and round-trips
  ---
  duration_ms: 7.411556
  ...
# Subtest: project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
ok 1975 - project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
  ---
  duration_ms: 2.316585
  ...
# Subtest: buildTaskLineFromProjectNote preserves status, tags, and fields
ok 1976 - buildTaskLineFromProjectNote preserves status, tags, and fields
  ---
  duration_ms: 1.415173
  ...
# Subtest: getProjectReversalBlockId inverts the forward basename helper
ok 1977 - getProjectReversalBlockId inverts the forward basename helper
  ---
  duration_ms: 0.140939
  ...
# Subtest: formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
ok 1978 - formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
  ---
  duration_ms: 0.142592
  ...
# Subtest: splitProjectNoteForReversal treats TASKS as the task section and keeps section order
ok 1979 - splitProjectNoteForReversal treats TASKS as the task section and keeps section order
  ---
  duration_ms: 0.896311
  ...
# Subtest: indentProjectReversalLine preserves relative depth and drops blanks
ok 1980 - indentProjectReversalLine preserves relative depth and drops blanks
  ---
  duration_ms: 0.459518
  ...
# Subtest: buildTaskBlockFromProjectNote reports structure and frontmatter errors
ok 1981 - buildTaskBlockFromProjectNote reports structure and frontmatter errors
  ---
  duration_ms: 1.28279
  ...
# Subtest: buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
ok 1982 - buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
  ---
  duration_ms: 1.066677
  ...
# Subtest: rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
ok 1983 - rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
  ---
  duration_ms: 0.517408
  ...
# Subtest: collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
ok 1984 - collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
  ---
  duration_ms: 0.604875
  ...
# Subtest: getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
ok 1985 - getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
  ---
  duration_ms: 0.203909
  ...
# Subtest: convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
ok 1986 - convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
  ---
  duration_ms: 5.065514
  ...
# Subtest: project reversal recovers tagged residents when they leave a blocked project
ok 1987 - project reversal recovers tagged residents when they leave a blocked project
  ---
  duration_ms: 3.761594
  ...
# Subtest: convertProjectNoteToTask separates the restored task from a count-only parent section
ok 1988 - convertProjectNoteToTask separates the restored task from a count-only parent section
  ---
  duration_ms: 1.18303
  ...
# Subtest: createProjectNoteFromTask dispatches reverse only on a real ^prj line
ok 1989 - createProjectNoteFromTask dispatches reverse only on a real ^prj line
  ---
  duration_ms: 1.887706
  ...
# Subtest: convertProjectNoteToTask refusals leave every file untouched
ok 1990 - convertProjectNoteToTask refusals leave every file untouched
  ---
  duration_ms: 5.210112
  ...
# Subtest: planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
ok 1991 - planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
  ---
  duration_ms: 0.242914
  ...
# Subtest: convertProjectNoteToTask writes the parent first when it links to \#^prj
ok 1992 - convertProjectNoteToTask writes the parent first when it links to \#^prj
  ---
  duration_ms: 1.276609
  ...
# Subtest: convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
ok 1993 - convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
  ---
  duration_ms: 3.032341
  ...
# Subtest: convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
ok 1994 - convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
  ---
  duration_ms: 1.128575
  ...
# Subtest: convertProjectNoteToTask reports post-write failures without rolling back
ok 1995 - convertProjectNoteToTask reports post-write failures without rolling back
  ---
  duration_ms: 1.263493
  ...
# Subtest: convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
ok 1996 - convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
  ---
  duration_ms: 1.130409
  ...
# Subtest: convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
ok 1997 - convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
  ---
  duration_ms: 1.636525
  ...
# Subtest: v2 reading task opens its source_pdf in Highlights without writes
ok 1998 - v2 reading task opens its source_pdf in Highlights without writes
  ---
  duration_ms: 3.130517
  ...
# Subtest: every reading-task lane and \#REF casing opens
ok 1999 - every reading-task lane and \#REF casing opens
  ---
  duration_ms: 1.359376
  ...
# Subtest: v1 tracker resolves a PDF link or falls back to its own source_pdf
ok 2000 - v1 tracker resolves a PDF link or falls back to its own source_pdf
  ---
  duration_ms: 0.55537
  ...
# Subtest: plain, embedded, struck, and 🍅 Task Links resolve reading tasks
ok 2001 - plain, embedded, struck, and 🍅 Task Links resolve reading tasks
  ---
  duration_ms: 1.902333
  ...
# Subtest: bare managed embed in a reference note resolves its embedded task
ok 2002 - bare managed embed in a reference note resolves its embedded task
  ---
  duration_ms: 0.401367
  ...
# Subtest: ordinary lines, unresolved Task Links, fences, and outside focus delegate once
ok 2003 - ordinary lines, unresolved Task Links, fences, and outside focus delegate once
  ---
  duration_ms: 0.794588
  ...
# Subtest: identified reading tasks show notices without delegating
ok 2004 - identified reading tasks show notices without delegating
  ---
  duration_ms: 0.503151
  ...
# Subtest: unsafe source_pdf values are refused
ok 2005 - unsafe source_pdf values are refused
  ---
  duration_ms: 0.222304
  ...
# Subtest: bundle launch retries with the app name, and reports stderr on total failure
ok 2006 - bundle launch retries with the app name, and reports stderr on total failure
  ---
  duration_ms: 1.031972
  ...
# Subtest: off macOS shows the selected notice and managed ref-note prose delegates
ok 2007 - off macOS shows the selected notice and managed ref-note prose delegates
  ---
  duration_ms: 0.531725
  ...
# Subtest: pure helpers normalize and parse reference PDF paths
ok 2008 - pure helpers normalize and parse reference PDF paths
  ---
  duration_ms: 0.262721
  ...
# Subtest: command registration is custom-hotkey only
ok 2009 - command registration is custom-hotkey only
  ---
  duration_ms: 0.303149
  ...
# Subtest: nav api openReferencePdf hands a source_pdf to Highlights without version or vault writes
ok 2010 - nav api openReferencePdf hands a source_pdf to Highlights without version or vault writes
  ---
  duration_ms: 0.580088
  ...
# Subtest: nav api openReferencePdf settles to a reason instead of throwing
ok 2011 - nav api openReferencePdf settles to a reason instead of throwing
  ---
  duration_ms: 0.344097
  ...
# Subtest: reading tasks read with the book prefix, plain tasks unchanged
ok 2012 - reading tasks read with the book prefix, plain tasks unchanged
  ---
  duration_ms: 1.268813
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 2013 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.248946
  ...
# Subtest: picker rows carry the book prefix in displayText
ok 2014 - picker rows carry the book prefix in displayText
  ---
  duration_ms: 0.661985
  ...
# Subtest: managed reference rename modal and submit are refused
ok 2015 - managed reference rename modal and submit are refused
  ---
  duration_ms: 1.153794
  ...
# Subtest: legacy ref notes and non-ref notes still rename
ok 2016 - legacy ref notes and non-ref notes still rename
  ---
  duration_ms: 0.861927
  ...
# Subtest: managed reference predicate checks path and non-empty source_pdf
ok 2017 - managed reference predicate checks path and non-empty source_pdf
  ---
  duration_ms: 0.210482
  ...
# Subtest: planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
ok 2018 - planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
  ---
  duration_ms: 4.752748
  ...
# Subtest: planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
ok 2019 - planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
  ---
  duration_ms: 1.584195
  ...
# Subtest: runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
ok 2020 - runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
  ---
  duration_ms: 3.809606
  ...
# Subtest: runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
ok 2021 - runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
  ---
  duration_ms: 2.589426
  ...
# Subtest: runtime: no daily note today still writes the schedule with no Pomodoro chip
ok 2022 - runtime: no daily note today still writes the schedule with no Pomodoro chip
  ---
  duration_ms: 0.394925
  ...
# Subtest: runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
ok 2023 - runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
  ---
  duration_ms: 0.856957
  ...
# Subtest: runtime: vault.process throwing during the daily-note write is reported without throwing
ok 2024 - runtime: vault.process throwing during the daily-note write is reported without throwing
  ---
  duration_ms: 0.748851
  ...
# Subtest: runtime: the daily note open in another editor is written through that editor in its own transaction
ok 2025 - runtime: the daily note open in another editor is written through that editor in its own transaction
  ---
  duration_ms: 1.47144
  ...
# Subtest: runtime: re-running the same deferral gesture is idempotent
ok 2026 - runtime: re-running the same deferral gesture is idempotent
  ---
  duration_ms: 0.792233
  ...
# Subtest: runtime: a counted scheduled batch prunes exactly the targets that land on a future date
ok 2027 - runtime: a counted scheduled batch prunes exactly the targets that land on a future date
  ---
  duration_ms: 3.308459
  ...
# Subtest: runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
ok 2028 - runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
  ---
  duration_ms: 2.808033
  ...
# Subtest: runtime: the source note being today's daily note folds the prune into a single editor transaction
ok 2029 - runtime: the source note being today's daily note folds the prune into a single editor transaction
  ---
  duration_ms: 0.7069
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: bare future scheduled writes block only real supported open inline tasks
ok 2030 - bare future scheduled writes block only real supported open inline tasks
  ---
  duration_ms: 5.257041
  ...
# Subtest: single runtime transclusion toggle preserves viewport in one line transaction
ok 2031 - single runtime transclusion toggle preserves viewport in one line transaction
  ---
  duration_ms: 2.050076
  ...
# Subtest: same-file runtime toggle changes only markers, never fields or statuses
ok 2032 - same-file runtime toggle changes only markers, never fields or statuses
  ---
  duration_ms: 0.715166
  ...
# Subtest: pure toggle leaves a cursor moved during the toggle where it landed
ok 2033 - pure toggle leaves a cursor moved during the toggle where it landed
  ---
  duration_ms: 0.296997
  ...
# Subtest: counted runtime transclusion toggle preserves viewport and caret
ok 2034 - counted runtime transclusion toggle preserves viewport and caret
  ---
  duration_ms: 0.780631
  ...
# Subtest: counted property runtime uses one transaction and preserves caret and viewport
ok 2035 - counted property runtime uses one transaction and preserves caret and viewport
  ---
  duration_ms: 3.730295
  ...
# Subtest: bare due schedule recovery is guarded and can change only task status
ok 2036 - bare due schedule recovery is guarded and can change only task status
  ---
  duration_ms: 2.448897
  ...
# Subtest: counted due recovery applies Ready Next and In Progress in one transaction
ok 2037 - counted due recovery applies Ready Next and In Progress in one transaction
  ---
  duration_ms: 4.386288
  ...
# Subtest: scheduled recovery aborts after an asynchronous source change
ok 2038 - scheduled recovery aborts after an asynchronous source change
  ---
  duration_ms: 0.788356
  ...
# Subtest: counted property runtime aborts a stale batch without a transaction
ok 2039 - counted property runtime aborts a stale batch without a transaction
  ---
  duration_ms: 0.480428
  ...
# Subtest: counted project scheduling writes an inline date and blocks tagged residents
ok 2040 - counted project scheduling writes an inline date and blocks tagged residents
  ---
  duration_ms: 2.624081
  ...
# Subtest: future project scheduling prunes resident links and an emptied Pomodoro
ok 2041 - future project scheduling prunes resident links and an emptied Pomodoro
  ---
  duration_ms: 2.930667
  ...
# Subtest: single project scheduling recovers due residents through the gate
ok 2042 - single project scheduling recovers due residents through the gate
  ---
  duration_ms: 1.819785
  ...
# Subtest: single project schedule deletion removes propagated copies and recovers
ok 2043 - single project schedule deletion removes propagated copies and recovers
  ---
  duration_ms: 1.635874
  ...
# Subtest: formatPriorityRollScheduleReason covers all four shapes
ok 2044 - formatPriorityRollScheduleReason covers all four shapes
  ---
  duration_ms: 1.279293
  ...
# Subtest: the priority-roll picker row keeps range detail and stores the exact roll
ok 2045 - the priority-roll picker row keeps range detail and stores the exact roll
  ---
  duration_ms: 0.599335
  ...
# Subtest: buildPriorityRollScheduleLog returns null when the roll does not move the date
ok 2046 - buildPriorityRollScheduleLog returns null when the roll does not move the date
  ---
  duration_ms: 0.726969
  ...
# Subtest: getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
ok 2047 - getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
  ---
  duration_ms: 0.75913
  ...
# Subtest: a priority roll onto the current date writes the date but no log
ok 2048 - a priority roll onto the current date writes the date but no log
  ---
  duration_ms: 14.361211
  ...
# Subtest: a typed reason on an unchanged date is still written
ok 2049 - a typed reason on an unchanged date is still written
  ---
  duration_ms: 0.890611
  ...
# Subtest: schedule log bullet formatting and parsing round-trip with and without a previous value
ok 2050 - schedule log bullet formatting and parsing round-trip with and without a previous value
  ---
  duration_ms: 0.931899
  ...
# Subtest: formatScheduleLogEntryText renders entry text without indent or marker
ok 2051 - formatScheduleLogEntryText renders entry text without indent or marker
  ---
  duration_ms: 0.131721
  ...
# Subtest: schedule reason text normalization trims, collapses whitespace, and flags inline fields
ok 2052 - schedule reason text normalization trims, collapses whitespace, and flags inline fields
  ---
  duration_ms: 0.36141
  ...
# Subtest: findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
ok 2053 - findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
  ---
  duration_ms: 0.868128
  ...
# Subtest: getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
ok 2054 - getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
  ---
  duration_ms: 0.311625
  ...
# Subtest: planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
ok 2055 - planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
  ---
  duration_ms: 0.65963
  ...
# Subtest: planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
ok 2056 - planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
  ---
  duration_ms: 0.255918
  ...
# Subtest: planScheduleLogEntry uses the fallback only when a marker exists
ok 2057 - planScheduleLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.273282
  ...
# Subtest: a typed reason wins over the fallback
ok 2058 - a typed reason wins over the fallback
  ---
  duration_ms: 0.196164
  ...
# Subtest: the fallback is suppressed on an unchanged date
ok 2059 - the fallback is suppressed on an unchanged date
  ---
  duration_ms: 0.159204
  ...
# Subtest: no reason and no fallback still guards empty-reason
ok 2060 - no reason and no fallback still guards empty-reason
  ---
  duration_ms: 0.128395
  ...
# Subtest: getScheduleLogWriteOutcome maps plan outcomes for writers
ok 2061 - getScheduleLogWriteOutcome maps plan outcomes for writers
  ---
  duration_ms: 0.179723
  ...
# Subtest: hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
ok 2062 - hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
  ---
  duration_ms: 0.198569
  ...
# Subtest: counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
ok 2063 - counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
  ---
  duration_ms: 2.453856
  ...
# Subtest: empty reason through the counted planner writes no schedule log entries
ok 2064 - empty reason through the counted planner writes no schedule log entries
  ---
  duration_ms: 0.794528
  ...
# Subtest: a counted scheduled session logs only the tasks that already keep a log
ok 2065 - a counted scheduled session logs only the tasks that already keep a log
  ---
  duration_ms: 0.85339
  ...
# Subtest: the counted notice wording distinguishes a fallback batch from a typed-reason batch
ok 2066 - the counted notice wording distinguishes a fallback batch from a typed-reason batch
  ---
  duration_ms: 6.053262
  ...
# Subtest: setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
ok 2067 - setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
  ---
  duration_ms: 0.543859
  ...
# Subtest: setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
ok 2068 - setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
  ---
  duration_ms: 4.478925
  ...
# Subtest: priority bullet property config normalizes frozen levels and preserves existing shapes
ok 2069 - priority bullet property config normalizes frozen levels and preserves existing shapes
  ---
  duration_ms: 2.137032
  ...
# Subtest: priority bullet property config rejects each invalid schema category once
ok 2070 - priority bullet property config rejects each invalid schema category once
  ---
  duration_ms: 0.982677
  ...
# Subtest: project scheduling targets the inline ^prj field
ok 2071 - project scheduling targets the inline ^prj field
  ---
  duration_ms: 1.766214
  ...
# Subtest: local task properties are addable only on valid tasks but invalid metadata stays removable
ok 2072 - local task properties are addable only on valid tasks but invalid metadata stays removable
  ---
  duration_ms: 0.295044
  ...
# Subtest: dependency parent write validation rejects stale, Pomodoro, and fenced parents
ok 2073 - dependency parent write validation rejects stale, Pomodoro, and fenced parents
  ---
  duration_ms: 0.483033
  ...
# Subtest: counted property targets mean current plus N real tasks without wrapping
ok 2074 - counted property targets mean current plus N real tasks without wrapping
  ---
  duration_ms: 0.686361
  ...
# Subtest: counted property metadata distinguishes absent, common, and mixed values
ok 2075 - counted property metadata distinguishes absent, common, and mixed values
  ---
  duration_ms: 0.648909
  ...
# Subtest: counted priority metadata reports labels for common and mixed values
ok 2076 - counted priority metadata reports labels for common and mixed values
  ---
  duration_ms: 0.569769
  ...
# Subtest: counted scheduled planning updates the motivating three tasks atomically
ok 2077 - counted scheduled planning updates the motivating three tasks atomically
  ---
  duration_ms: 2.243595
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: project schedule validation accepts only real YYYY-MM-DD dates
ok 2078 - project schedule validation accepts only real YYYY-MM-DD dates
  ---
  duration_ms: 1.017173
  ...
# Subtest: source task schedule is extracted without losing task metadata
ok 2079 - source task schedule is extracted without losing task metadata
  ---
  duration_ms: 1.277891
  ...
# Subtest: source task schedule errors are focused and ambiguous fields fail
ok 2080 - source task schedule errors are focused and ambiguous fields fail
  ---
  duration_ms: 0.345079
  ...
# Subtest: project creation frontmatter never stores the task schedule
ok 2081 - project creation frontmatter never stores the task schedule
  ---
  duration_ms: 0.155907
  ...
# Subtest: future schedule labels use local date-only boundaries
ok 2082 - future schedule labels use local date-only boundaries
  ---
  duration_ms: 0.5602
  ...
# Subtest: scheduled recovery selects current and newest earlier daily across gaps
ok 2083 - scheduled recovery selects current and newest earlier daily across gaps
  ---
  duration_ms: 0.532417
  ...
# Subtest: scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
ok 2084 - scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
  ---
  duration_ms: 8.114658
  ...
# Subtest: scheduled recovery defers incompatible status settings and ambiguous identities
ok 2085 - scheduled recovery defers incompatible status settings and ambiguous identities
  ---
  duration_ms: 0.433137
  ...
# Subtest: scheduled recovery honors custom open and closed Tasks status types
ok 2086 - scheduled recovery honors custom open and closed Tasks status types
  ---
  duration_ms: 0.64415
  ...
# Subtest: scheduled recovery honors the configured Tasks global filter
ok 2087 - scheduled recovery honors the configured Tasks global filter
  ---
  duration_ms: 0.520674
  ...
# Subtest: child picker schedule metadata reads the inline ^prj date
ok 2088 - child picker schedule metadata reads the inline ^prj date
  ---
  duration_ms: 0.925327
  ...
# Subtest: task move destination schedule hydration reads cached ^prj content
ok 2089 - task move destination schedule hydration reads cached ^prj content
  ---
  duration_ms: 0.469306
  ...
# Subtest: project lifecycle task classification requires unfenced \#task with trailing ^prj
ok 2090 - project lifecycle task classification requires unfenced \#task with trailing ^prj
  ---
  duration_ms: 0.162731
  ...
# Subtest: valid Obsidian tasks require a standalone \#task checkbox in real note content
ok 2091 - valid Obsidian tasks require a standalone \#task checkbox in real note content
  ---
  duration_ms: 0.151419
  ...
# Subtest: choosing a scheduled date enters the combined review without writing anything
ok 2092 - choosing a scheduled date enters the combined review without writing anything
  ---
  duration_ms: 18.031487
  ...
# Subtest: choosing a priority level does not enter the schedule review
ok 2093 - choosing a priority level does not enter the schedule review
  ---
  duration_ms: 9.240249
  ...
# Subtest: confirming an empty reason on a task with an existing schedule log appends an unexplained entry
ok 2094 - confirming an empty reason on a task with an existing schedule log appends an unexplained entry
  ---
  duration_ms: 6.443637
  ...
# Subtest: confirming an empty reason on a task with no schedule log writes only the date
ok 2095 - confirming an empty reason on a task with no schedule log writes only the date
  ---
  duration_ms: 3.038764
  ...
# Subtest: review stage getFilteredItems always returns exactly one synthetic preview item
ok 2096 - review stage getFilteredItems always returns exactly one synthetic preview item
  ---
  duration_ms: 1.635072
  ...
# Subtest: the review preview row previews the entry it will write
ok 2097 - the review preview row previews the entry it will write
  ---
  duration_ms: 3.176576
  ...
# Subtest: the review footer flips between Skip optional logs and Apply schedule as the Reason changes
ok 2098 - the review footer flips between Skip optional logs and Apply schedule as the Reason changes
  ---
  duration_ms: 1.357583
  ...
# Subtest: closing the picker during the review clears pending schedule state and writes nothing
ok 2099 - closing the picker during the review clears pending schedule state and writes nothing
  ---
  duration_ms: 1.126571
  ...
# Subtest: scheduling Work Log eligibility requires Pending or Next \#task lines
ok 2100 - scheduling Work Log eligibility requires Pending or Next \#task lines
  ---
  duration_ms: 1.227375
  ...
# Subtest: single Pending explicit date opens one review and writes both logs
ok 2101 - single Pending explicit date opens one review and writes both logs
  ---
  duration_ms: 22.310931
  ...
# Subtest: single Next blank and whitespace summaries schedule without a Work Log
ok 2102 - single Next blank and whitespace summaries schedule without a Work Log
  ---
  duration_ms: 5.515945
  ...
# Subtest: Escape at the review writes nothing, with or without typed text
ok 2103 - Escape at the review writes nothing, with or without typed text
  ---
  duration_ms: 5.327646
  ...
# Subtest: Ready and Blocked explicit dates review the Reason with no Work summary field
ok 2104 - Ready and Blocked explicit dates review the Reason with no Work summary field
  ---
  duration_ms: 3.869912
  ...
# Subtest: future scheduling on Pending marks Blocked but still writes the Work Log
ok 2105 - future scheduling on Pending marks Blocked but still writes the Work Log
  ---
  duration_ms: 2.081485
  ...
# Subtest: today date on Pending still offers the Work Log
ok 2106 - today date on Pending still offers the Work Log
  ---
  duration_ms: 2.517588
  ...
# Subtest: priority pick on Pending freezes its roll and offers the Work Log
ok 2107 - priority pick on Pending freezes its roll and offers the Work Log
  ---
  duration_ms: 3.991692
  ...
# Subtest: counted mixed statuses share one summary only on Pending and Next
ok 2108 - counted mixed statuses share one summary only on Pending and Next
  ---
  duration_ms: 7.889249
  ...
# Subtest: counted planner composes Schedule and Work Logs bottom-up above later targets
ok 2109 - counted planner composes Schedule and Work Logs bottom-up above later targets
  ---
  duration_ms: 0.962338
  ...
# Subtest: counted planner writes a Work Log even when the date is unchanged
ok 2110 - counted planner writes a Work Log even when the date is unchanged
  ---
  duration_ms: 0.31937
  ...
# Subtest: scheduling Work Log ownership keeps nested logs and CRLF endings
ok 2111 - scheduling Work Log ownership keeps nested logs and CRLF endings
  ---
  duration_ms: 0.766484
  ...
# Subtest: scheduling Work Log warns on :: and preserves Markdown
ok 2112 - scheduling Work Log warns on :: and preserves Markdown
  ---
  duration_ms: 2.106053
  ...
# Subtest: stale task while reviewing refuses with no scheduling or log writes
ok 2113 - stale task while reviewing refuses with no scheduling or log writes
  ---
  duration_ms: 1.268613
  ...
# Subtest: scheduling prompts never leak into lane or cancel stages
ok 2114 - scheduling prompts never leak into lane or cancel stages
  ---
  duration_ms: 2.100633
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: Pomodoro-marked links are not managed dependency bullets
ok 2115 - Pomodoro-marked links are not managed dependency bullets
  ---
  duration_ms: 2.070174
  ...
# Subtest: deleting inline scheduled metadata recovers Blocked targets by snapshot rank
ok 2116 - deleting inline scheduled metadata recovers Blocked targets by snapshot rank
  ---
  duration_ms: 5.394654
  ...
# Subtest: counted future scheduling blocks only supported open inline task statuses
ok 2117 - counted future scheduling blocks only supported open inline task statuses
  ---
  duration_ms: 2.75391
  ...
# Subtest: counted property planning rejects any stale source with no partial result
ok 2118 - counted property planning rejects any stale source with no partial result
  ---
  duration_ms: 0.419301
  ...
# Subtest: counted project scheduling writes the ^prj inline date and blocks tagged residents
ok 2119 - counted project scheduling writes the ^prj inline date and blocks tagged residents
  ---
  duration_ms: 2.872106
  ...
# Subtest: moving a project schedule earlier replaces only exact old-date copies
ok 2120 - moving a project schedule earlier replaces only exact old-date copies
  ---
  duration_ms: 0.623822
  ...
# Subtest: future project schedules block every open resident and consume review status
ok 2121 - future project schedules block every open resident and consume review status
  ---
  duration_ms: 0.846217
  ...
# Subtest: due project dates recover residents through the gate and write unblocked markers
ok 2122 - due project dates recover residents through the gate and write unblocked markers
  ---
  duration_ms: 0.857768
  ...
# Subtest: schedule deletion removes only exact project-date copies and recovers residents
ok 2123 - schedule deletion removes only exact project-date copies and recovers residents
  ---
  duration_ms: 1.230601
  ...
# Subtest: dependency lines render one canonical Depends-On line per parent
ok 2124 - dependency lines render one canonical Depends-On line per parent
  ---
  duration_ms: 0.828252
  ...
# Subtest: dependency IDs encode root and nested Markdown paths deterministically
ok 2125 - dependency IDs encode root and nested Markdown paths deterministically
  ---
  duration_ms: 1.028595
  ...
# Subtest: prompted block IDs truthfully replace legacy id fields
ok 2126 - prompted block IDs truthfully replace legacy id fields
  ---
  duration_ms: 0.268994
  ...
# Subtest: dependency navigation identity includes note path and folds legacy children
ok 2127 - dependency navigation identity includes note path and folds legacy children
  ---
  duration_ms: 1.024647
  ...
# Subtest: retired dependency bullets are excluded from single and counted toggles
ok 2128 - retired dependency bullets are excluded from single and counted toggles
  ---
  duration_ms: 1.414201
  ...
# Subtest: dependsOn replacement accepts spaces around field name and separator
ok 2129 - dependsOn replacement accepts spaces around field name and separator
  ---
  duration_ms: 0.300604
  ...
# Subtest: task status helpers keep Blocked open but rankless
ok 2130 - task status helpers keep Blocked open but rankless
  ---
  duration_ms: 0.299843
  ...
# Subtest: a due project date with only closed Depends-On history strips the tag
ok 2131 - a due project date with only closed Depends-On history strips the tag
  ---
  duration_ms: 0.788506
  ...
# Subtest: Ctrl+D with only closed Depends-On history strips the tag
ok 2132 - Ctrl+D with only closed Depends-On history strips the tag
  ---
  duration_ms: 0.422066
  ...
# Subtest: Ctrl+D with an open Depends-On link remaining keeps the tag
ok 2133 - Ctrl+D with an open Depends-On link remaining keeps the tag
  ---
  duration_ms: 0.290625
  ...
# Subtest: counted ^prj schedule sessions write [unblocked::] when the writer is passed
ok 2134 - counted ^prj schedule sessions write [unblocked::] when the writer is passed
  ---
  duration_ms: 0.482882
  ...
# Subtest: a due project date keeps the tag while ^prj holds Depends-On links
ok 2135 - a due project date keeps the tag while ^prj holds Depends-On links
  ---
  duration_ms: 0.30386
  ...
# Subtest: a due project date strips the tag while a resident with its own reason stays Blocked
ok 2136 - a due project date strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.262631
  ...
# Subtest: Ctrl+D strips the tag while a resident with its own reason stays Blocked
ok 2137 - Ctrl+D strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.343395
  ...
# Subtest: counted scheduled deletes recover with [unblocked::] when the writer is passed
ok 2138 - counted scheduled deletes recover with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.222485
  ...
# Subtest: section-header navigation moves normally and cycles at boundaries
ok 2139 - section-header navigation moves normally and cycles at boundaries
  ---
  duration_ms: 1.913624
  ...
# Subtest: section-header navigation wraps from beyond document boundaries
ok 2140 - section-header navigation wraps from beyond document boundaries
  ---
  duration_ms: 0.191425
  ...
# Subtest: section-header navigation handles single-header and no-header notes
ok 2141 - section-header navigation handles single-header and no-header notes
  ---
  duration_ms: 0.206264
  ...
# Subtest: open-task navigation scan includes Ready In Progress and Next and excludes Blocked
ok 2142 - open-task navigation scan includes Ready In Progress and Next and excludes Blocked
  ---
  duration_ms: 0.545081
  ...
# Subtest: open-task navigation keeps existing Pomodoro ledger targets
ok 2143 - open-task navigation keeps existing Pomodoro ledger targets
  ---
  duration_ms: 0.681492
  ...
# Subtest: next and previous jumps skip Blocked tasks and wrap to an allowed task
ok 2144 - next and previous jumps skip Blocked tasks and wrap to an allowed task
  ---
  duration_ms: 0.456793
  ...
# Subtest: blocked-only notes and a sole current allowed task have no jump target
ok 2145 - blocked-only notes and a sole current allowed task have no jump target
  ---
  duration_ms: 0.168622
  ...
# Subtest: counted open-task jumps select the Nth eligible target and wrap modulo the list
ok 2146 - counted open-task jumps select the Nth eligible target and wrap modulo the list
  ---
  duration_ms: 0.292068
  ...
# Subtest: counted open-task jumps keep sole-target and invalid-repeat behavior
ok 2147 - counted open-task jumps keep sole-target and invalid-repeat behavior
  ---
  duration_ms: 0.446022
  ...
# Subtest: tab pin Vim action registers once and toggles only the active leaf once
ok 2148 - tab pin Vim action registers once and toggles only the active leaf once
  ---
  duration_ms: 2.336262
  ...
# Subtest: tab pin toggle fails safely without a supported active leaf
ok 2149 - tab pin toggle fails safely without a supported active leaf
  ---
  duration_ms: 0.194532
  ...
# Subtest: close tabs left preserves pinned sibling tabs and refocuses active tab
ok 2150 - close tabs left preserves pinned sibling tabs and refocuses active tab
  ---
  duration_ms: 0.750784
  ...
# Subtest: close tabs right preserves pinned siblings and ignores the left side
ok 2151 - close tabs right preserves pinned siblings and ignores the left side
  ---
  duration_ms: 0.372581
  ...
# Subtest: close other tabs preserves pinned siblings on both sides
ok 2152 - close other tabs preserves pinned siblings on both sides
  ---
  duration_ms: 0.253323
  ...
# Subtest: close sibling tabs is a silent no-op when the scoped range is all pinned
ok 2153 - close sibling tabs is a silent no-op when the scoped range is all pinned
  ---
  duration_ms: 0.214249
  ...
# Subtest: close sibling tabs honors every pinned leaf representation
ok 2154 - close sibling tabs honors every pinned leaf representation
  ---
  duration_ms: 0.294843
  ...
# Subtest: close sibling tabs treats throwing view state as unpinned
ok 2155 - close sibling tabs treats throwing view state as unpinned
  ---
  duration_ms: 0.391588
  ...
# Subtest: tab pin Vim registration retries after adapter availability
ok 2156 - tab pin Vim registration retries after adapter availability
  ---
  duration_ms: 0.810227
  ...
# Subtest: isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
ok 2157 - isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
  ---
  duration_ms: 3.86349
  ...
# Subtest: isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
ok 2158 - isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
  ---
  duration_ms: 0.617009
  ...
# Subtest: isPomodoroTaskLinkLine refuses Depends-On lines and prose links
ok 2159 - isPomodoroTaskLinkLine refuses Depends-On lines and prose links
  ---
  duration_ms: 0.220942
  ...
# Subtest: decideTaskLinkLaneMode starts when any target is Next
ok 2160 - decideTaskLinkLaneMode starts when any target is Next
  ---
  duration_ms: 0.173451
  ...
# Subtest: taskLinkLaneRefusalFor renders every D5 refusal
ok 2161 - taskLinkLaneRefusalFor renders every D5 refusal
  ---
  duration_ms: 0.162501
  ...
# Subtest: planTaskLinkLaneBatch starts Next targets and leaves the rest alone
ok 2162 - planTaskLinkLaneBatch starts Next targets and leaves the rest alone
  ---
  duration_ms: 1.200984
  ...
# Subtest: planTaskLinkLaneBatch pauses with one shared Work Log entry
ok 2163 - planTaskLinkLaneBatch pauses with one shared Work Log entry
  ---
  duration_ms: 0.773577
  ...
# Subtest: planTaskLinkLaneBatch applies the freshness stamp last
ok 2164 - planTaskLinkLaneBatch applies the freshness stamp last
  ---
  duration_ms: 0.300243
  ...
# Subtest: planTaskLinkLaneBatch dedupes lines and refuses stale preimages
ok 2165 - planTaskLinkLaneBatch dedupes lines and refuses stale preimages
  ---
  duration_ms: 0.490758
  ...
# Subtest: buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
ok 2166 - buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
  ---
  duration_ms: 0.679889
  ...
# Subtest: taskLinkLanePromptState drives the Move to Next prompt
ok 2167 - taskLinkLanePromptState drives the Move to Next prompt
  ---
  duration_ms: 0.255639
  ...
# Subtest: TaskLinkLanePromptModal submits, previews live, and cancels silently
ok 2168 - TaskLinkLanePromptModal submits, previews live, and cancels silently
  ---
  duration_ms: 1.606058
  ...
# Subtest: TaskLinkLanePromptModal renders the batch context card
ok 2169 - TaskLinkLanePromptModal renders the batch context card
  ---
  duration_ms: 0.364847
  ...
# Subtest: findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
ok 2170 - findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
  ---
  duration_ms: 0.310463
  ...
# Subtest: L1: toggle starts a Next link, stamps, hints, and notices
ok 2171 - L1: toggle starts a Next link, stamps, hints, and notices
  ---
  duration_ms: 3.461701
  ...
# Subtest: L2/L3: toggle pauses through the prompt, logging one shared entry
ok 2172 - L2/L3: toggle pauses through the prompt, logging one shared entry
  ---
  duration_ms: 11.740652
  ...
# Subtest: L4: cancelling the prompt writes nothing and shows no Notice
ok 2173 - L4: cancelling the prompt writes nothing and shows no Notice
  ---
  duration_ms: 0.96333
  ...
# Subtest: L5: both directions run the same toggle twice for a round trip
ok 2174 - L5: both directions run the same toggle twice for a round trip
  ---
  duration_ms: 1.352063
  ...
# Subtest: L6: Ready, Blocked, done, and cancelled targets are refused
ok 2175 - L6: Ready, Blocked, done, and cancelled targets are refused
  ---
  duration_ms: 1.64895
  ...
# Subtest: L6: missing targets keep the existing resolver error
ok 2176 - L6: missing targets keep the existing resolver error
  ---
  duration_ms: 0.261369
  ...
# Subtest: L7: a counted start flips every Next sibling and leaves In Progress alone
ok 2177 - L7: a counted start flips every Next sibling and leaves In Progress alone
  ---
  duration_ms: 0.53961
  ...
# Subtest: L8: a counted pause prompts once and skips Blocked with a count
ok 2178 - L8: a counted pause prompts once and skips Blocked with a count
  ---
  duration_ms: 1.673076
  ...
# Subtest: L9: an over-long count clamps at the entry end without error
ok 2179 - L9: an over-long count clamps at the entry end without error
  ---
  duration_ms: 0.661353
  ...
# Subtest: L10: a closed-entry history line toggles the task and keeps the line
ok 2180 - L10: a closed-entry history line toggles the task and keeps the line
  ---
  duration_ms: 0.325081
  ...
# Subtest: L11: a target edited while the prompt is open refuses stale
ok 2181 - L11: a target edited while the prompt is open refuses stale
  ---
  duration_ms: 1.702282
  ...
# Subtest: L12: an embedded Pomodoro link takes the two-state toggle
ok 2182 - L12: an embedded Pomodoro link takes the two-state toggle
  ---
  duration_ms: 0.554589
  ...
# Subtest: L14: the same task linked twice in a batch is written once
ok 2183 - L14: the same task linked twice in a batch is written once
  ---
  duration_ms: 1.491088
  ...
# Subtest: L15: a second toggle while one is in flight is swallowed as busy
ok 2184 - L15: a second toggle while one is in flight is swallowed as busy
  ---
  duration_ms: 0.747057
  ...
# Subtest: toggle on a non-link line refuses without writing
ok 2185 - toggle on a non-link line refuses without writing
  ---
  duration_ms: 0.252994
  ...
# Subtest: api.taskLinkLane is a frozen v1 namespace that never throws
ok 2186 - api.taskLinkLane is a frozen v1 namespace that never throws
  ---
  duration_ms: 0.869681
  ...
# Subtest: the progressMarks hint is a no-op without the ledger-tools api
ok 2187 - the progressMarks hint is a no-op without the ledger-tools api
  ---
  duration_ms: 0.30871
  ...
# Subtest: task move records one Vim jump and round-trips without extra writes
ok 2188 - task move records one Vim jump and round-trips without extra writes
  ---
  duration_ms: 9.489553
  ...
# Subtest: counted task move records a single jump to the first moved task
ok 2189 - counted task move records a single jump to the first moved task
  ---
  duration_ms: 1.322766
  ...
# Subtest: deferred task landing re-anchors and records the resolved cursor once
ok 2190 - deferred task landing re-anchors and records the resolved cursor once
  ---
  duration_ms: 4.596198
  ...
# Subtest: failed task move preserves seeded history including the forward branch
ok 2191 - failed task move preserves seeded history including the forward branch
  ---
  duration_ms: 0.543037
  ...
# Subtest: post-commit open failure keeps the move committed with no jump
ok 2192 - post-commit open failure keeps the move committed with no jump
  ---
  duration_ms: 1.028565
  ...
# Subtest: a newer move supersedes a pending landing without stale placement
ok 2193 - a newer move supersedes a pending landing without stale placement
  ---
  duration_ms: 10.661654
  ...
# Subtest: shared destination helper without a move context records no jump
ok 2194 - shared destination helper without a move context records no jump
  ---
  duration_ms: 0.813584
  ...
# Subtest: task moves carry the Depends-On line and repath stranded same-note links
ok 2195 - task moves carry the Depends-On line and repath stranded same-note links
  ---
  duration_ms: 5.714555
  ...
# Subtest: task moves keep pathless links when the target moves along
ok 2196 - task moves keep pathless links when the target moves along
  ---
  duration_ms: 0.984009
  ...
# Subtest: counted task moves discover movable tasks without wrapping or examples
ok 2197 - counted task moves discover movable tasks without wrapping or examples
  ---
  duration_ms: 1.12577
  ...
# Subtest: task move ranges preserve quoted subtrees and collapse overlapping selections
ok 2198 - task move ranges preserve quoted subtrees and collapse overlapping selections
  ---
  duration_ms: 0.665802
  ...
# Subtest: task move removal handles disjoint ranges, blank seams, and CRLF
ok 2199 - task move removal handles disjoint ranges, blank seams, and CRLF
  ---
  duration_ms: 0.464588
  ...
# Subtest: task move destinations include areas and only open projects
ok 2200 - task move destinations include areas and only open projects
  ---
  duration_ms: 0.628721
  ...
# Subtest: moves into a blocked project leave closed tagged lines alone
ok 2201 - moves into a blocked project leave closed tagged lines alone
  ---
  duration_ms: 1.892705
  ...
# Subtest: moves into a blocked project promote open prerequisites to the moved lane
ok 2202 - moves into a blocked project promote open prerequisites to the moved lane
  ---
  duration_ms: 2.111733
  ...
# Subtest: task move insertion preserves exact task and section spacing
ok 2203 - task move insertion preserves exact task and section spacing
  ---
  duration_ms: 2.866996
  ...
# Subtest: task move planning migrates identities and links across every affected note
ok 2204 - task move planning migrates identities and links across every affected note
  ---
  duration_ms: 4.235029
  ...
# Subtest: task move planning exposes a destination anchor for area destinations and counted moves
ok 2205 - task move planning exposes a destination anchor for area destinations and counted moves
  ---
  duration_ms: 0.789498
  ...
# Subtest: task move into a blocked project tags the moved task and consumes today's live Pomodoro link
ok 2206 - task move into a blocked project tags the moved task and consumes today's live Pomodoro link
  ---
  duration_ms: 3.884428
  ...
# Subtest: task move out of a blocked project recovers through the shared gate and writes the unblocked mark
ok 2207 - task move out of a blocked project recovers through the shared gate and writes the unblocked mark
  ---
  duration_ms: 3.470729
  ...
# Subtest: move promotion walks through a ^prj target without raising it
ok 2208 - move promotion walks through a ^prj target without raising it
  ---
  duration_ms: 2.226212
  ...
# Subtest: move promotion walks through a [?] ^prj to its open prerequisite
ok 2209 - move promotion walks through a [?] ^prj to its open prerequisite
  ---
  duration_ms: 0.889789
  ...
# Subtest: move promotion uses each open task's own lane, not the strongest moved lane
ok 2210 - move promotion uses each open task's own lane, not the strongest moved lane
  ---
  duration_ms: 1.159695
  ...
# Subtest: move promotion skips Depends-On lines of closed tasks
ok 2211 - move promotion skips Depends-On lines of closed tasks
  ---
  duration_ms: 0.806009
  ...
# Subtest: task move planning rejects destination collisions and malformed identities
ok 2212 - task move planning rejects destination collisions and malformed identities
  ---
  duration_ms: 0.547125
  ...
# Subtest: resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
ok 2213 - resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
  ---
  duration_ms: 0.605647
  ...
# Subtest: focusTaskMoveDestination opens the destination file and anchors the cursor
ok 2214 - focusTaskMoveDestination opens the destination file and anchors the cursor
  ---
  duration_ms: 1.066858
  ...
# Subtest: focusTaskMoveDestination returns false without moving the cursor when the open fails
ok 2215 - focusTaskMoveDestination returns false without moving the cursor when the open fails
  ---
  duration_ms: 0.246461
  ...
# Subtest: focusTaskMoveDestination re-anchors by block ID when the destination content drifted
ok 2216 - focusTaskMoveDestination re-anchors by block ID when the destination content drifted
  ---
  duration_ms: 0.245038
  ...
# Subtest: physical task move chord declines auto-repeat and consumes Vim normal input once
ok 2217 - physical task move chord declines auto-repeat and consumes Vim normal input once
  ---
  duration_ms: 0.873107
  ...
# Subtest: counted task move dispatch keeps its count through cold async destinations
ok 2218 - counted task move dispatch keeps its count through cold async destinations
  ---
  duration_ms: 12.921947
  ...
# Subtest: counted task move dispatch with warm async destinations opens one counted picker
ok 2219 - counted task move dispatch with warm async destinations opens one counted picker
  ---
  duration_ms: 5.038955
  ...
# Subtest: bare task move command ignores stale Vim count outside normal mode
ok 2220 - bare task move command ignores stale Vim count outside normal mode
  ---
  duration_ms: 0.77987
  ...
# Subtest: bare task move command opens one uncounted target in Vim normal mode
ok 2221 - bare task move command opens one uncounted target in Vim normal mode
  ---
  duration_ms: 0.385356
  ...
# Subtest: already handled task move event leaves pending Vim state alone
ok 2222 - already handled task move event leaves pending Vim state alone
  ---
  duration_ms: 0.144336
  ...
# Subtest: counted task move command dispatch counts Pomodoro sub-bullets once
ok 2223 - counted task move command dispatch counts Pomodoro sub-bullets once
  ---
  duration_ms: 2.383202
  ...
# Subtest: physical transclusion toggle owns bare and counted Vim normal input
ok 2224 - physical transclusion toggle owns bare and counted Vim normal input
  ---
  duration_ms: 1.382581
  ...
# Subtest: runtime task move writes destination before source and rolls back source failures
ok 2225 - runtime task move writes destination before source and rolls back source failures
  ---
  duration_ms: 2.3298
  ...
# Subtest: runtime task move groups open-editor source and destination changes
ok 2226 - runtime task move groups open-editor source and destination changes
  ---
  duration_ms: 1.499454
  ...
# Subtest: runtime task move guards destination, auxiliary, and rollback failures
ok 2227 - runtime task move guards destination, auxiliary, and rollback failures
  ---
  duration_ms: 1.619203
  ...
# Subtest: task move insertion separates the section's first task from preamble and placeholders
ok 2228 - task move insertion separates the section's first task from preamble and placeholders
  ---
  duration_ms: 0.3665
  ...
# Subtest: task move insertion keeps populated sections compact and second moves stable
ok 2229 - task move insertion keeps populated sections compact and second moves stable
  ---
  duration_ms: 0.193259
  ...
# Subtest: task move planning separates a counted move into a count-only section
ok 2230 - task move planning separates a counted move into a count-only section
  ---
  duration_ms: 0.385717
  ...
# Subtest: runtime counted move into a count-only section focuses the first moved task
ok 2231 - runtime counted move into a count-only section focuses the first moved task
  ---
  duration_ms: 0.918915
  ...
# Subtest: absent local key with folder template writes the trigger and one notice
ok 2232 - absent local key with folder template writes the trigger and one notice
  ---
  duration_ms: 2.394763
  ...
# Subtest: existing local object keeps other keys and only adds the trigger
ok 2233 - existing local object keeps other keys and only adds the trigger
  ---
  duration_ms: 0.349036
  ...
# Subtest: stored true is already-enabled with no write and no notice
ok 2234 - stored true is already-enabled with no write and no notice
  ---
  duration_ms: 0.359206
  ...
# Subtest: stored false is device-opt-out with no write and no notice
ok 2235 - stored false is device-opt-out with no write and no notice
  ---
  duration_ms: 0.223397
  ...
# Subtest: mode none and blank folder templates skip as no-creation-templates
ok 2236 - mode none and blank folder templates skip as no-creation-templates
  ---
  duration_ms: 0.350981
  ...
# Subtest: regex mode with a non-empty file template enables
ok 2237 - regex mode with a non-empty file template enables
  ---
  duration_ms: 0.266379
  ...
# Subtest: legacy settings without a mode key skip as legacy-templater
ok 2238 - legacy settings without a mode key skip as legacy-templater
  ---
  duration_ms: 0.264155
  ...
# Subtest: missing Templater plugin or settings skip as no-templater without throwing
ok 2239 - missing Templater plugin or settings skip as no-templater without throwing
  ---
  duration_ms: 0.421675
  ...
# Subtest: missing loadLocalStorage or saveLocalStorage returns without throwing
ok 2240 - missing loadLocalStorage or saveLocalStorage returns without throwing
  ---
  duration_ms: 0.431694
  ...
# Subtest: string or array stored local values skip as unknown-local-shape
ok 2241 - string or array stored local values skip as unknown-local-shape
  ---
  duration_ms: 0.568526
  ...
# Subtest: saveLocalStorage throw shows one failure notice and does not escape
ok 2242 - saveLocalStorage throw shows one failure notice and does not escape
  ---
  duration_ms: 0.300183
  ...
# Subtest: planTemplaterLocalTrigger covers helper cases and never adds extra keys
ok 2243 - planTemplaterLocalTrigger covers helper cases and never adds extra keys
  ---
  duration_ms: 0.291397
  ...
# Subtest: unblocked model returns null when there is nothing to show
ok 2244 - unblocked model returns null when there is nothing to show
  ---
  duration_ms: 1.344679
  ...
# Subtest: unblocked card renders a single linked row with receipt and chips
ok 2245 - unblocked card renders a single linked row with receipt and chips
  ---
  duration_ms: 1.56547
  ...
# Subtest: unblocked card renders several linked rows with one entry
ok 2246 - unblocked card renders several linked rows with one entry
  ---
  duration_ms: 0.304581
  ...
# Subtest: unblocked card renders a created continuation with next up
ok 2247 - unblocked card renders a created continuation with next up
  ---
  duration_ms: 0.396176
  ...
# Subtest: unblocked card renders recovered-only and still-blocked rows
ok 2248 - unblocked card renders recovered-only and still-blocked rows
  ---
  duration_ms: 0.676442
  ...
# Subtest: current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
ok 2249 - current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
  ---
  duration_ms: 0.882264
  ...
# Subtest: project pull-in rows label empty projects and preserve project blocking reasons
ok 2250 - project pull-in rows label empty projects and preserve project blocking reasons
  ---
  duration_ms: 0.992375
  ...
# Subtest: unblocked card caps visible rows with +N more
ok 2251 - unblocked card caps visible rows with +N more
  ---
  duration_ms: 0.336363
  ...
# Subtest: unblocked card renders the breaker variant
ok 2252 - unblocked card renders the breaker variant
  ---
  duration_ms: 0.511978
  ...
# Subtest: unblocked card renders the failure variant
ok 2253 - unblocked card renders the failure variant
  ---
  duration_ms: 0.516977
  ...
# Subtest: unblocked rows open their task without dismissing the notice
ok 2254 - unblocked rows open their task without dismissing the notice
  ---
  duration_ms: 1.109769
  ...
# Subtest: unblocked row without a block id opens the note path
ok 2255 - unblocked row without a block id opens the note path
  ---
  duration_ms: 0.307748
  ...
# Subtest: unblocked card omits the plan chip when daily content is null
ok 2256 - unblocked card omits the plan chip when daily content is null
  ---
  duration_ms: 0.228977
  ...
# Subtest: unblocked notice shows one card with duration through showNotice
ok 2257 - unblocked notice shows one card with duration through showNotice
  ---
  duration_ms: 0.317336
  ...
# Subtest: unblocked notice falls back to plain text without a DOM
ok 2258 - unblocked notice falls back to plain text without a DOM
  ---
  duration_ms: 0.156248
  ...
# Subtest: unblocked text truncates to 48 characters with an ellipsis
ok 2259 - unblocked text truncates to 48 characters with an ellipsis
  ---
  duration_ms: 0.141921
  ...
# Subtest: nav api exposes additive notice v1 and keeps version 3
ok 2260 - nav api exposes additive notice v1 and keeps version 3
  ---
  duration_ms: 0.374014
  ...
# Subtest: unblocked stylesheet scopes notice overrides and uses task tokens
ok 2261 - unblocked stylesheet scopes notice overrides and uses task tokens
  ---
  duration_ms: 0.51867
  ...
# Subtest: physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
ok 2262 - physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
  ---
  duration_ms: 2.373444
  ...
# Subtest: open-task command ids omit repeat so the shared route resolves the pending Vim count
ok 2263 - open-task command ids omit repeat so the shared route resolves the pending Vim count
  ---
  duration_ms: 1.178932
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
ok 2264 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
  ---
  duration_ms: 4.431735
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
ok 2265 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
  ---
  duration_ms: 0.589827
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
ok 2266 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
  ---
  duration_ms: 1.117605
  ...
# Subtest: dispatch guard applies a command-route Vim count when the capture route fires second
ok 2267 - dispatch guard applies a command-route Vim count when the capture route fires second
  ---
  duration_ms: 1.19916
  ...
# Subtest: dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
ok 2268 - dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
  ---
  duration_ms: 1.052761
  ...
# Subtest: command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
ok 2269 - command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
  ---
  duration_ms: 0.920407
  ...
# Subtest: command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
ok 2270 - command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
  ---
  duration_ms: 2.777965
  ...
# Subtest: command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
ok 2271 - command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
  ---
  duration_ms: 1.149135
  ...
# Subtest: explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
ok 2272 - explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
  ---
  duration_ms: 0.761084
  ...
# Subtest: getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
ok 2273 - getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
  ---
  duration_ms: 0.229268
  ...
# Subtest: physical counted property chord consumes only explicit normal-mode Vim counts
ok 2274 - physical counted property chord consumes only explicit normal-mode Vim counts
  ---
  duration_ms: 0.695959
  ...
# Subtest: physical counted Ctrl+Shift+B and Ctrl+Shift+Alt+B route to their Task Card rows
ok 2275 - physical counted Ctrl+Shift+B and Ctrl+Shift+Alt+B route to their Task Card rows
  ---
  duration_ms: 0.522388
  ...
# Subtest: parser finds vault embed with size hint
ok 2276 - parser finds vault embed with size hint
  ---
  duration_ms: 1.444528
  ...
# Subtest: parser finds plain image wikilink and blockquoted embed
ok 2277 - parser finds plain image wikilink and blockquoted embed
  ---
  duration_ms: 0.235349
  ...
# Subtest: parser ignores callout bracket and finds the embed
ok 2278 - parser ignores callout bracket and finds the embed
  ---
  duration_ms: 0.343165
  ...
# Subtest: parser ignores image links inside single and double backticks
ok 2279 - parser ignores image links inside single and double backticks
  ---
  duration_ms: 0.741206
  ...
# Subtest: non-image wiki targets are recognized but not candidates
ok 2280 - non-image wiki targets are recognized but not candidates
  ---
  duration_ms: 0.236933
  ...
# Subtest: parser finds two image refs and lines with no refs
ok 2281 - parser finds two image refs and lines with no refs
  ---
  duration_ms: 0.17304
  ...
# Subtest: parser handles Markdown angle, title, and balanced parens
ok 2282 - parser handles Markdown angle, title, and balanced parens
  ---
  duration_ms: 0.505065
  ...
# Subtest: picker uses containing, next, then previous rule
ok 2283 - picker uses containing, next, then previous rule
  ---
  duration_ms: 0.384023
  ...
# Subtest: resolution records sourcePath and resolves duplicate basenames
ok 2284 - resolution records sourcePath and resolves duplicate basenames
  ---
  duration_ms: 1.053372
  ...
# Subtest: resolution handles relative, unicode, and space names
ok 2285 - resolution handles relative, unicode, and space names
  ---
  duration_ms: 0.527979
  ...
# Subtest: missing file, non-image cursor, and fenced lines show exact notices
ok 2286 - missing file, non-image cursor, and fenced lines show exact notices
  ---
  duration_ms: 0.302859
  ...
# Subtest: vault resolution calls getResourcePath with the resolved file
ok 2287 - vault resolution calls getResourcePath with the resolved file
  ---
  duration_ms: 0.330771
  ...
# Subtest: http embed passes through and non-image urls are not candidates
ok 2288 - http embed passes through and non-image urls are not candidates
  ---
  duration_ms: 0.565771
  ...
# Subtest: fit never exceeds 1 and respects padding for landscape, portrait, and tiny images
ok 2289 - fit never exceeds 1 and respects padding for landscape, portrait, and tiny images
  ---
  duration_ms: 1.297607
  ...
# Subtest: min and max bounds follow fit, 1:1, and the max factor
ok 2290 - min and max bounds follow fit, 1:1, and the max factor
  ---
  duration_ms: 0.232514
  ...
# Subtest: stepping clamps at both bounds
ok 2291 - stepping clamps at both bounds
  ---
  duration_ms: 0.440731
  ...
# Subtest: zoom-at-point keeps the point fixed
ok 2292 - zoom-at-point keeps the point fixed
  ---
  duration_ms: 0.153273
  ...
# Subtest: clamp centres small axes and limits large ones
ok 2293 - clamp centres small axes and limits large ones
  ---
  duration_ms: 0.279043
  ...
# Subtest: key Escape → close
ok 2294 - key Escape → close
  ---
  duration_ms: 0.707821
  ...
# Subtest: key q → close
ok 2295 - key q → close
  ---
  duration_ms: 0.190013
  ...
# Subtest: key Q → close
ok 2296 - key Q → close
  ---
  duration_ms: 0.097767
  ...
# Subtest: key Ctrl+[ → close
ok 2297 - key Ctrl+[ → close
  ---
  duration_ms: 0.371078
  ...
# Subtest: key Z → close
ok 2298 - key Z → close
  ---
  duration_ms: 0.392991
  ...
# Subtest: key + → zoomIn
ok 2299 - key + → zoomIn
  ---
  duration_ms: 0.171027
  ...
# Subtest: key = → zoomIn
ok 2300 - key = → zoomIn
  ---
  duration_ms: 0.096946
  ...
# Subtest: key Shift+= → zoomIn
ok 2301 - key Shift+= → zoomIn
  ---
  duration_ms: 0.087838
  ...
# Subtest: key Shift++ → zoomIn
ok 2302 - key Shift++ → zoomIn
  ---
  duration_ms: 0.149155
  ...
# Subtest: key - → zoomOut
ok 2303 - key - → zoomOut
  ---
  duration_ms: 0.086135
  ...
# Subtest: key 0 → fit
ok 2304 - key 0 → fit
  ---
  duration_ms: 0.149806
  ...
# Subtest: key 1 → actual
ok 2305 - key 1 → actual
  ---
  duration_ms: 0.093098
  ...
# Subtest: key h → pan:left
ok 2306 - key h → pan:left
  ---
  duration_ms: 0.095342
  ...
# Subtest: key j → pan:down
ok 2307 - key j → pan:down
  ---
  duration_ms: 0.080133
  ...
# Subtest: key k → pan:up
ok 2308 - key k → pan:up
  ---
  duration_ms: 0.077348
  ...
# Subtest: key l → pan:right
ok 2309 - key l → pan:right
  ---
  duration_ms: 0.084181
  ...
# Subtest: key Shift+H → pan:left
ok 2310 - key Shift+H → pan:left
  ---
  duration_ms: 0.091424
  ...
# Subtest: key Shift+J → pan:down
ok 2311 - key Shift+J → pan:down
  ---
  duration_ms: 0.071597
  ...
# Subtest: key Shift+K → pan:up
ok 2312 - key Shift+K → pan:up
  ---
  duration_ms: 0.074713
  ...
# Subtest: key Shift+L → pan:right
ok 2313 - key Shift+L → pan:right
  ---
  duration_ms: 0.073501
  ...
# Subtest: key ArrowLeft → pan:left
ok 2314 - key ArrowLeft → pan:left
  ---
  duration_ms: 0.073551
  ...
# Subtest: key ArrowDown → pan:down
ok 2315 - key ArrowDown → pan:down
  ---
  duration_ms: 0.080704
  ...
# Subtest: key ArrowUp → pan:up
ok 2316 - key ArrowUp → pan:up
  ---
  duration_ms: 0.073661
  ...
# Subtest: key ArrowRight → pan:right
ok 2317 - key ArrowRight → pan:right
  ---
  duration_ms: 0.078219
  ...
# Subtest: key Shift+ArrowLeft → pan:left
ok 2318 - key Shift+ArrowLeft → pan:left
  ---
  duration_ms: 0.137864
  ...
# Subtest: key Ctrl+q → ignore
ok 2319 - key Ctrl+q → ignore
  ---
  duration_ms: 0.097746
  ...
# Subtest: key Meta+z → ignore
ok 2320 - key Meta+z → ignore
  ---
  duration_ms: 0.087928
  ...
# Subtest: key Meta+Z → ignore
ok 2321 - key Meta+Z → ignore
  ---
  duration_ms: 0.196205
  ...
# Subtest: key a composing → ignore
ok 2322 - key a composing → ignore
  ---
  duration_ms: 0.088249
  ...
# Subtest: key a keyCode 229 → ignore
ok 2323 - key a keyCode 229 → ignore
  ---
  duration_ms: 0.072479
  ...
# Subtest: key x → ignore
ok 2324 - key x → ignore
  ---
  duration_ms: 0.060535
  ...
# Subtest: keys before arming are ignored
ok 2325 - keys before arming are ignored
  ---
  duration_ms: 1.028454
  ...
# Subtest: Z closes after arming, and a repeated Z does not
ok 2326 - Z closes after arming, and a repeated Z does not
  ---
  duration_ms: 0.493553
  ...
# Subtest: load sets fit state and dimensions
ok 2327 - load sets fit state and dimensions
  ---
  duration_ms: 0.484836
  ...
# Subtest: a load error shows a notice, closes, and calls onClosed once
ok 2328 - a load error shows a notice, closes, and calls onClosed once
  ---
  duration_ms: 0.276989
  ...
# Subtest: Escape closes once, unregisters the scope handler, and aborts the signal
ok 2329 - Escape closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.238045
  ...
# Subtest: q closes once, unregisters the scope handler, and aborts the signal
ok 2330 - q closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.216834
  ...
# Subtest: Q closes once, unregisters the scope handler, and aborts the signal
ok 2331 - Q closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.154425
  ...
# Subtest: Ctrl+[ closes once, unregisters the scope handler, and aborts the signal
ok 2332 - Ctrl+[ closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.234598
  ...
# Subtest: Z closes once, unregisters the scope handler, and aborts the signal
ok 2333 - Z closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.260988
  ...
# Subtest: a stray x key changes nothing
ok 2334 - a stray x key changes nothing
  ---
  duration_ms: 0.321414
  ...
# Subtest: the app's vault stubs throw and are never called
ok 2335 - the app's vault stubs throw and are never called
  ---
  duration_ms: 0.220181
  ...
# Subtest: task-card-gate arms only on open inbox tasks
ok 2336 - task-card-gate arms only on open inbox tasks
  ---
  duration_ms: 3.570769
  ...
# Subtest: task-card-gate header shows the Inbox chip only when armed
ok 2337 - task-card-gate header shows the Inbox chip only when armed
  ---
  duration_ms: 5.784788
  ...
# Subtest: task-card-gate priority: cancel writes nothing
ok 2338 - task-card-gate priority: cancel writes nothing
  ---
  duration_ms: 1.062449
  ...
# Subtest: task-card-gate priority: stay runs today's write
ok 2339 - task-card-gate priority: stay runs today's write
  ---
  duration_ms: 0.258184
  ...
# Subtest: task-card-gate priority: move writes then moves
ok 2340 - task-card-gate priority: move writes then moves
  ---
  duration_ms: 0.559659
  ...
# Subtest: task-card-gate scheduled: cancel writes nothing
ok 2341 - task-card-gate scheduled: cancel writes nothing
  ---
  duration_ms: 0.159284
  ...
# Subtest: task-card-gate scheduled: stay runs today's write
ok 2342 - task-card-gate scheduled: stay runs today's write
  ---
  duration_ms: 0.232214
  ...
# Subtest: task-card-gate scheduled: move writes then moves
ok 2343 - task-card-gate scheduled: move writes then moves
  ---
  duration_ms: 0.201394
  ...
# Subtest: task-card-gate generic-property: cancel writes nothing
ok 2344 - task-card-gate generic-property: cancel writes nothing
  ---
  duration_ms: 0.3876
  ...
# Subtest: task-card-gate generic-property: stay runs today's write
ok 2345 - task-card-gate generic-property: stay runs today's write
  ---
  duration_ms: 0.439319
  ...
# Subtest: task-card-gate generic-property: move writes then moves
ok 2346 - task-card-gate generic-property: move writes then moves
  ---
  duration_ms: 0.30369
  ...
# Subtest: task-card-gate refresh-interval: cancel writes nothing
ok 2347 - task-card-gate refresh-interval: cancel writes nothing
  ---
  duration_ms: 0.169825
  ...
# Subtest: task-card-gate refresh-interval: stay runs today's write
ok 2348 - task-card-gate refresh-interval: stay runs today's write
  ---
  duration_ms: 0.126682
  ...
# Subtest: task-card-gate refresh-interval: move writes then moves
ok 2349 - task-card-gate refresh-interval: move writes then moves
  ---
  duration_ms: 0.139025
  ...
# Subtest: task-card-gate refresh-custom: cancel writes nothing
ok 2350 - task-card-gate refresh-custom: cancel writes nothing
  ---
  duration_ms: 0.105943
  ...
# Subtest: task-card-gate refresh-custom: stay runs today's write
ok 2351 - task-card-gate refresh-custom: stay runs today's write
  ---
  duration_ms: 0.129206
  ...
# Subtest: task-card-gate refresh-custom: move writes then moves
ok 2352 - task-card-gate refresh-custom: move writes then moves
  ---
  duration_ms: 0.319891
  ...
# Subtest: task-card-gate clear-priority: cancel writes nothing
ok 2353 - task-card-gate clear-priority: cancel writes nothing
  ---
  duration_ms: 0.134487
  ...
# Subtest: task-card-gate clear-priority: stay runs today's write
ok 2354 - task-card-gate clear-priority: stay runs today's write
  ---
  duration_ms: 0.110921
  ...
# Subtest: task-card-gate clear-priority: move writes then moves
ok 2355 - task-card-gate clear-priority: move writes then moves
  ---
  duration_ms: 0.219759
  ...
# Subtest: task-card-gate recommended-roll: cancel writes nothing
ok 2356 - task-card-gate recommended-roll: cancel writes nothing
  ---
  duration_ms: 0.097817
  ...
# Subtest: task-card-gate recommended-roll: stay runs today's write
ok 2357 - task-card-gate recommended-roll: stay runs today's write
  ---
  duration_ms: 0.102446
  ...
# Subtest: task-card-gate recommended-roll: move writes then moves
ok 2358 - task-card-gate recommended-roll: move writes then moves
  ---
  duration_ms: 0.118506
  ...
# Subtest: task-card-gate recommended-decay: cancel writes nothing
ok 2359 - task-card-gate recommended-decay: cancel writes nothing
  ---
  duration_ms: 0.092657
  ...
# Subtest: task-card-gate recommended-decay: stay runs today's write
ok 2360 - task-card-gate recommended-decay: stay runs today's write
  ---
  duration_ms: 0.087557
  ...
# Subtest: task-card-gate recommended-decay: move writes then moves
ok 2361 - task-card-gate recommended-decay: move writes then moves
  ---
  duration_ms: 0.118276
  ...
# Subtest: task-card-gate counted-roll: cancel writes nothing
ok 2362 - task-card-gate counted-roll: cancel writes nothing
  ---
  duration_ms: 0.170966
  ...
# Subtest: task-card-gate counted-roll: stay runs today's write
ok 2363 - task-card-gate counted-roll: stay runs today's write
  ---
  duration_ms: 0.100993
  ...
# Subtest: task-card-gate counted-roll: move writes then moves
ok 2364 - task-card-gate counted-roll: move writes then moves
  ---
  duration_ms: 0.208068
  ...
# Subtest: task-card-gate lane-toggle: cancel writes nothing
ok 2365 - task-card-gate lane-toggle: cancel writes nothing
  ---
  duration_ms: 0.101674
  ...
# Subtest: task-card-gate lane-toggle: stay runs today's write
ok 2366 - task-card-gate lane-toggle: stay runs today's write
  ---
  duration_ms: 0.097686
  ...
# Subtest: task-card-gate lane-toggle: move writes then moves
ok 2367 - task-card-gate lane-toggle: move writes then moves
  ---
  duration_ms: 0.152711
  ...
# Subtest: task-card-gate dependency-single: cancel writes nothing
ok 2368 - task-card-gate dependency-single: cancel writes nothing
  ---
  duration_ms: 0.085323
  ...
# Subtest: task-card-gate dependency-single: stay runs today's write
ok 2369 - task-card-gate dependency-single: stay runs today's write
  ---
  duration_ms: 0.088469
  ...
# Subtest: task-card-gate dependency-single: move writes then moves
ok 2370 - task-card-gate dependency-single: move writes then moves
  ---
  duration_ms: 0.368584
  ...
# Subtest: task-card-gate dependency-marked: cancel writes nothing
ok 2371 - task-card-gate dependency-marked: cancel writes nothing
  ---
  duration_ms: 0.100722
  ...
# Subtest: task-card-gate dependency-marked: stay runs today's write
ok 2372 - task-card-gate dependency-marked: stay runs today's write
  ---
  duration_ms: 0.090092
  ...
# Subtest: task-card-gate dependency-marked: move writes then moves
ok 2373 - task-card-gate dependency-marked: move writes then moves
  ---
  duration_ms: 0.111032
  ...
# Subtest: task-card-gate dependency-vault: cancel writes nothing
ok 2374 - task-card-gate dependency-vault: cancel writes nothing
  ---
  duration_ms: 0.087738
  ...
# Subtest: task-card-gate dependency-vault: stay runs today's write
ok 2375 - task-card-gate dependency-vault: stay runs today's write
  ---
  duration_ms: 0.095553
  ...
# Subtest: task-card-gate dependency-vault: move writes then moves
ok 2376 - task-card-gate dependency-vault: move writes then moves
  ---
  duration_ms: 0.108737
  ...
# Subtest: task-card-gate dependency-counted: cancel writes nothing
ok 2377 - task-card-gate dependency-counted: cancel writes nothing
  ---
  duration_ms: 0.091495
  ...
# Subtest: task-card-gate dependency-counted: stay runs today's write
ok 2378 - task-card-gate dependency-counted: stay runs today's write
  ---
  duration_ms: 0.096815
  ...
# Subtest: task-card-gate dependency-counted: move writes then moves
ok 2379 - task-card-gate dependency-counted: move writes then moves
  ---
  duration_ms: 0.123005
  ...
# Subtest: task-card-gate negative rows never prompt
ok 2380 - task-card-gate negative rows never prompt
  ---
  duration_ms: 0.707191
  ...
# Subtest: task-card-gate counted sessions capture N targets
ok 2381 - task-card-gate counted sessions capture N targets
  ---
  duration_ms: 0.258915
  ...
# Subtest: task-card-gate walk: move advances once with Moved first
ok 2382 - task-card-gate walk: move advances once with Moved first
  ---
  duration_ms: 0.20944
  ...
# Subtest: task-card-gate walk: move failure falls back to card with partial
ok 2383 - task-card-gate walk: move failure falls back to card with partial
  ---
  duration_ms: 0.312346
  ...
# Subtest: task-card-gate walk: exactly one settle per origin
ok 2384 - task-card-gate walk: exactly one settle per origin
  ---
  duration_ms: 22.523717
  ...
# Subtest: task-card-gate route outcome resolves like lane and link-today
ok 2385 - task-card-gate route outcome resolves like lane and link-today
  ---
  duration_ms: 0.518109
  ...
# Subtest: inbox classifier covers the inbox contract
ok 2386 - inbox classifier covers the inbox contract
  ---
  duration_ms: 1.513982
  ...
# Subtest: isInboxNotePath matches the inbox contract through the vault
ok 2387 - isInboxNotePath matches the inbox contract through the vault
  ---
  duration_ms: 1.244227
  ...
# Subtest: isInboxNotePath is false without an inbox note and never throws
ok 2388 - isInboxNotePath is false without an inbox note and never throws
  ---
  duration_ms: 0.153292
  ...
# Subtest: route destinations drop every inbox note, the source, and templates
ok 2389 - route destinations drop every inbox note, the source, and templates
  ---
  duration_ms: 0.745484
  ...
# Subtest: route preflight accepts a live area destination
ok 2390 - route preflight accepts a live area destination
  ---
  duration_ms: 3.935988
  ...
# Subtest: route preflight refuses stale and colliding destinations
ok 2391 - route preflight refuses stale and colliding destinations
  ---
  duration_ms: 1.480247
  ...
# Subtest: route picker resolves move, stay, cancel, and close exactly once
ok 2392 - route picker resolves move, stay, cancel, and close exactly once
  ---
  duration_ms: 3.160036
  ...
# Subtest: route picker footer names the move, the hatch, and the way back
ok 2393 - route picker footer names the move, the hatch, and the way back
  ---
  duration_ms: 0.467683
  ...
# Subtest: route picker preflight refusal keeps the picker open with a notice
ok 2394 - route picker preflight refusal keeps the picker open with a notice
  ---
  duration_ms: 6.936579
  ...
# Subtest: route picker honors the shared move-picker guard
ok 2395 - route picker honors the shared move-picker guard
  ---
  duration_ms: 2.205683
  ...
# Subtest: promptInboxRoute moves, stays, and cancels with suspend pairing
ok 2396 - promptInboxRoute moves, stays, and cancels with suspend pairing
  ---
  duration_ms: 2.485868
  ...
# Subtest: commitInboxRoute moves the verified task with its children
ok 2397 - commitInboxRoute moves the verified task with its children
  ---
  duration_ms: 3.584426
  ...
# Subtest: commitInboxRoute into a blocked project tags the moved task
ok 2398 - commitInboxRoute into a blocked project tags the moved task
  ---
  duration_ms: 2.70715
  ...
# Subtest: commitInboxRoute moves a counted run and refuses on identity drift
ok 2399 - commitInboxRoute moves a counted run and refuses on identity drift
  ---
  duration_ms: 3.690768
  ...
# Subtest: reviewOutcomeResolves treats route like lane and link-today
ok 2400 - reviewOutcomeResolves treats route like lane and link-today
  ---
  duration_ms: 0.285726
  ...
# Subtest: nav api inboxRoute v1 delegates, shapes, and never throws
ok 2401 - nav api inboxRoute v1 delegates, shapes, and never throws
  ---
  duration_ms: 1.416485
  ...
# Subtest: history records ordered locations with file identity and dedupes adjacent repeats
ok 2402 - history records ordered locations with file identity and dedupes adjacent repeats
  ---
  duration_ms: 1.285706
  ...
# Subtest: transition records origin then destination and truncates forward only on success
ok 2403 - transition records origin then destination and truncates forward only on success
  ---
  duration_ms: 0.903335
  ...
# Subtest: history retains at most 100 locations and refreshes the live tip
ok 2404 - history retains at most 100 locations and refreshes the live tip
  ---
  duration_ms: 0.742528
  ...
# Subtest: rename updates paths and delete prunes without corrupting the index
ok 2405 - rename updates paths and delete prunes without corrupting the index
  ---
  duration_ms: 0.311235
  ...
# Subtest: bridge wraps add once, mirrors native jumps, and preserves the original call
ok 2406 - bridge wraps add once, mirrors native jumps, and preserves the original call
  ---
  duration_ms: 1.576491
  ...
# Subtest: bridge without a jump list preserves keys and emits one compatibility diagnostic
ok 2407 - bridge without a jump list preserves keys and emits one compatibility diagnostic
  ---
  duration_ms: 0.342574
  ...
# Subtest: registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
ok 2408 - registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
  ---
  duration_ms: 0.322286
  ...
# Subtest: Enter A->B round-trips with Ctrl+O and Ctrl+I
ok 2409 - Enter A->B round-trips with Ctrl+O and Ctrl+I
  ---
  duration_ms: 22.736226
  ...
# Subtest: counted Enter returns to the original cursor, not the counted link line
ok 2410 - counted Enter returns to the original cursor, not the counted link line
  ---
  duration_ms: 21.023613
  ...
# Subtest: picker choice records one jump and cancellation records none
ok 2411 - picker choice records one jump and cancellation records none
  ---
  duration_ms: 21.686417
  ...
# Subtest: stale picker origin is rejected and failed opens record nothing
ok 2412 - stale picker origin is rejected and failed opens record nothing
  ---
  duration_ms: 20.902163
  ...
# Subtest: Backspace shares the link path and no-link lines fall through
ok 2413 - Backspace shares the link path and no-link lines fall through
  ---
  duration_ms: 21.511524
  ...
# Subtest: counted traversal honors boundaries and new jumps replace the forward branch
ok 2414 - counted traversal honors boundaries and new jumps replace the forward branch
  ---
  duration_ms: 0.727219
  ...
# Subtest: ordinary motion before back is preserved for forward restore
ok 2415 - ordinary motion before back is preserved for forward restore
  ---
  duration_ms: 0.29813
  ...
# Subtest: deleted entries are skipped and heading links settle before recording
ok 2416 - deleted entries are skipped and heading links settle before recording
  ---
  duration_ms: 20.776092
  ...
# Subtest: native fallback runs with empty history and boundaries never replay natives
ok 2417 - native fallback runs with empty history and boundaries never replay natives
  ---
  duration_ms: 0.615485
  ...
# Subtest: unload restores the native add and keeps a foreign later mapping
ok 2418 - unload restores the native add and keeps a foreign later mapping
  ---
  duration_ms: 0.412027
  ...
# Subtest: exact eligibility authorizes one due-Ready ROTTEN row
ok 2419 - exact eligibility authorizes one due-Ready ROTTEN row
  ---
  duration_ms: 1.297488
  ...
# Subtest: exact eligibility authorizes a TICKLER row
ok 2420 - exact eligibility authorizes a TICKLER row
  ---
  duration_ms: 0.192398
  ...
# Subtest: exact eligibility refuses every stale-cache shape
ok 2421 - exact eligibility refuses every stale-cache shape
  ---
  duration_ms: 0.481329
  ...
# Subtest: exact eligibility refuses non-Ready and non-due rows
ok 2422 - exact eligibility refuses non-Ready and non-due rows
  ---
  duration_ms: 0.258955
  ...
# Subtest: legacy refs still match line-only while exact refuses
ok 2423 - legacy refs still match line-only while exact refuses
  ---
  duration_ms: 0.578144
  ...
# Subtest: keeps support needs namespace v5 with keepLine
ok 2424 - keeps support needs namespace v5 with keepLine
  ---
  duration_ms: 0.153794
  ...
# Subtest: decay decisions need namespace v6 with keepLine
ok 2425 - decay decisions need namespace v6 with keepLine
  ---
  duration_ms: 0.20916
  ...
# Subtest: batch forwards per-target counted decisions to the stamper
ok 2426 - batch forwards per-target counted decisions to the stamper
  ---
  duration_ms: 0.712271
  ...
# Subtest: batch keeps legacy index targets uncounted
ok 2427 - batch keeps legacy index targets uncounted
  ---
  duration_ms: 0.356711
  ...
# Subtest: a throwing stamper refuses the batch with no partial write
ok 2428 - a throwing stamper refuses the batch with no partial write
  ---
  duration_ms: 0.461843
  ...
# Subtest: parseKeepsCount reads the first valid value only
ok 2429 - parseKeepsCount reads the first valid value only
  ---
  duration_ms: 0.310934
  ...
# Subtest: countFreshStampKept measures actual increments only
ok 2430 - countFreshStampKept measures actual increments only
  ---
  duration_ms: 0.171197
  ...
# Subtest: fresh stamp notice tails kept increments without promises
ok 2431 - fresh stamp notice tails kept increments without promises
  ---
  duration_ms: 0.21511
  ...
# Subtest: duplicate source targets dedupe to one write
ok 2432 - duplicate source targets dedupe to one write
  ---
  duration_ms: 0.169073
  ...
# Subtest: single Alt+F increments an exact due-Ready ROTTEN task
ok 2433 - single Alt+F increments an exact due-Ready ROTTEN task
  ---
  duration_ms: 5.200233
  ...
# Subtest: single Alt+F preserves NEW, lane, and early tasks without counting
ok 2434 - single Alt+F preserves NEW, lane, and early tasks without counting
  ---
  duration_ms: 2.09401
  ...
# Subtest: same-day repeat stays identical and counts nothing
ok 2435 - same-day repeat stays identical and counts nothing
  ---
  duration_ms: 0.589937
  ...
# Subtest: Pending Alt+F writes its summary with the stamp in one edit
ok 2436 - Pending Alt+F writes its summary with the stamp in one edit
  ---
  duration_ms: 1.462875
  ...
# Subtest: counted Pending refresh shares one summary only with Pending targets
ok 2437 - counted Pending refresh shares one summary only with Pending targets
  ---
  duration_ms: 0.751025
  ...
# Subtest: a refusing counted target refuses before the Pending Work Log prompt
ok 2438 - a refusing counted target refuses before the Pending Work Log prompt
  ---
  duration_ms: 0.44485
  ...
# Subtest: blank Pending refresh advances; cancelled or stale prompts write nothing
ok 2439 - blank Pending refresh advances; cancelled or stale prompts write nothing
  ---
  duration_ms: 1.179513
  ...
# Subtest: stale queue match stamps uncounted and never inflates
ok 2440 - stale queue match stamps uncounted and never inflates
  ---
  duration_ms: 0.613051
  ...
# Subtest: counted Alt+F increments every exact target once
ok 2441 - counted Alt+F increments every exact target once
  ---
  duration_ms: 0.640002
  ...
# Subtest: stale editor source refuses with no write
ok 2442 - stale editor source refuses with no write
  ---
  duration_ms: 0.200283
  ...
# Subtest: single-note write lands in one editor transaction and keeps CRLF
ok 2443 - single-note write lands in one editor transaction and keeps CRLF
  ---
  duration_ms: 0.631566
  ...
# Subtest: v5 without keepLine fails without writing
ok 2444 - v5 without keepLine fails without writing
  ---
  duration_ms: 0.19863
  ...
# Subtest: throwing v5 keepLine refuses the batch with no partial write
ok 2445 - throwing v5 keepLine refuses the batch with no partial write
  ---
  duration_ms: 0.379745
  ...
# Subtest: pre-v5 ledger stamps uncounted through the old stamper
ok 2446 - pre-v5 ledger stamps uncounted through the old stamper
  ---
  duration_ms: 0.421445
  ...
# Subtest: Task Link session skips an at-limit decide target
ok 2447 - Task Link session skips an at-limit decide target
  ---
  duration_ms: 2.07386
  ...
# Subtest: Task Link refresh counts one exact target
ok 2448 - Task Link refresh counts one exact target
  ---
  duration_ms: 1.040176
  ...
# Subtest: duplicate Task Links to one target stamp and count once
ok 2449 - duplicate Task Links to one target stamp and count once
  ---
  duration_ms: 0.655752
  ...
# Subtest: counted Task Links dedupe targets and log only the Pending target
ok 2450 - counted Task Links dedupe targets and log only the Pending target
  ---
  duration_ms: 0.929525
  ...
# Subtest: multi-note stale preimage refuses with no writes
ok 2451 - multi-note stale preimage refuses with no writes
  ---
  duration_ms: 0.904547
  ...
# Subtest: multi-note write failure rolls back the first note
ok 2452 - multi-note write failure rolls back the first note
  ---
  duration_ms: 0.974612
  ...
# Subtest: one physical key through two routes stamps once
ok 2453 - one physical key through two routes stamps once
  ---
  duration_ms: 1.571502
  ...
# Subtest: Ctrl+Alt+F capture advances once and consumes a Vim prefix
ok 2454 - Ctrl+Alt+F capture advances once and consumes a Vim prefix
  ---
  duration_ms: 0.585689
  ...
# Subtest: obsolete and extra-modifier F chords stay unconsumed
ok 2455 - obsolete and extra-modifier F chords stay unconsumed
  ---
  duration_ms: 0.252271
  ...
# Subtest: live Ctrl+Alt+F double dispatch asks once on a Pending task
ok 2456 - live Ctrl+Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.729504
  ...
# Subtest: live Alt+F double dispatch asks once on a Pending task
ok 2457 - live Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.674479
  ...
# Subtest: already-handled refresh keydown leaves Vim state alone
ok 2458 - already-handled refresh keydown leaves Vim state alone
  ---
  duration_ms: 0.256129
  ...
# Subtest: parseBobOpenNotesParams accepts indexed entries and ignores unknown keys
ok 2459 - parseBobOpenNotesParams accepts indexed entries and ignores unknown keys
  ---
  duration_ms: 1.852899
  ...
# Subtest: parseBobOpenNotesParams rejects every malformed URI field
ok 2460 - parseBobOpenNotesParams rejects every malformed URI field
  ---
  duration_ms: 0.471381
  ...
# Subtest: invalid batches show one notice and open nothing
ok 2461 - invalid batches show one notice and open nothing
  ---
  duration_ms: 1.12025
  ...
# Subtest: path mapping follows a symlink realpath into the vault
ok 2462 - path mapping follows a symlink realpath into the vault
  ---
  duration_ms: 3.138845
  ...
# Subtest: new-tab policy reuses existing tabs and the active empty tab, keeping order and primary active
ok 2463 - new-tab policy reuses existing tabs and the active empty tab, keeping order and primary active
  ---
  duration_ms: 1.408771
  ...
# Subtest: an absent or outside entry fails independently and a PDF opens without landing
ok 2464 - an absent or outside entry fails independently and a PDF opens without landing
  ---
  duration_ms: 2001.442802
  ...
# Subtest: a resolved note that is not open waits until its captured digest is cached
ok 2465 - a resolved note that is not open waits until its captured digest is cached
  ---
  duration_ms: 64.203933
  ...
# Subtest: a per-entry open failure does not prevent later notes from opening
ok 2466 - a per-entry open failure does not prevent later notes from opening
  ---
  duration_ms: 0.901652
  ...
# Subtest: waits for a newly created vault file and a late visible line digest
ok 2467 - waits for a newly created vault file and a late visible line digest
  ---
  duration_ms: 61.679102
  ...
# Subtest: re-finds a moved digest on any line, including prose and Pomodoro rows
ok 2468 - re-finds a moved digest on any line, including prose and Pomodoro rows
  ---
  duration_ms: 1.20922
  ...
# Subtest: deadline fallback opens near the planned line and reports a changed capture
ok 2469 - deadline fallback opens near the planned line and reports a changed capture
  ---
  duration_ms: 2000.775266
  ...
# Subtest: truncation reports how many of the full list opened
ok 2470 - truncation reports how many of the full list opened
  ---
  duration_ms: 0.776864
  ...
# Subtest: serializes quick URLs and leaves the later URL active
ok 2471 - serializes quick URLs and leaves the later URL active
  ---
  duration_ms: 1.925909
  ...
# Subtest: primary landing flashes briefly, secondary landings do not, and the handler is read-only
ok 2472 - primary landing flashes briefly, secondary landings do not, and the handler is read-only
  ---
  duration_ms: 16.325569
  ...
# Subtest: onload registers bob-open-notes beside bob-goto-task
ok 2473 - onload registers bob-open-notes beside bob-goto-task
  ---
  duration_ms: 1.765352
  ...
# Subtest: a non-file sidebar view is not reused as an empty tab
ok 2474 - a non-file sidebar view is not reused as an empty tab
  ---
  duration_ms: 0.747017
  ...
# Subtest: a true empty tab is reused for the first entry
ok 2475 - a true empty tab is reused for the first entry
  ---
  duration_ms: 0.355679
  ...
# Subtest: three new tabs follow entry order in the tab strip
ok 2476 - three new tabs follow entry order in the tab strip
  ---
  duration_ms: 0.651294
  ...
# Subtest: two tabs of the same note reuse the first matching leaf
ok 2477 - two tabs of the same note reuse the first matching leaf
  ---
  duration_ms: 0.339408
  ...
# Subtest: a missing file does not scan vault lists when getAbstractFileByPath exists
ok 2478 - a missing file does not scan vault lists when getAbstractFileByPath exists
  ---
  duration_ms: 2001.058968
  ...
# Subtest: new tabs append at the far right when the middle tab is active
ok 2479 - new tabs append at the far right when the middle tab is active
  ---
  duration_ms: 1.115651
  ...
# Subtest: a reused tab stays put while a new one is appended
ok 2480 - a reused tab stays put while a new one is appended
  ---
  duration_ms: 0.500616
  ...
# Subtest: a deferred tab is reused and findMarkdownLeafByPath sees it
ok 2481 - a deferred tab is reused and findMarkdownLeafByPath sees it
  ---
  duration_ms: 0.652115
  ...
# Subtest: a deferred sidebar leaf whose saved state names the note is not reused
ok 2482 - a deferred sidebar leaf whose saved state names the note is not reused
  ---
  duration_ms: 0.458847
  ...
# Subtest: a loaded main-area match beats an earlier loaded sidebar match
ok 2483 - a loaded main-area match beats an earlier loaded sidebar match
  ---
  duration_ms: 0.390346
  ...
# Subtest: a new tab goes to the end of the main group when a sidebar leaf is active
ok 2484 - a new tab goes to the end of the main group when a sidebar leaf is active
  ---
  duration_ms: 0.465068
  ...
# Subtest: falling back without createLeafInParent still opens a new tab
ok 2485 - falling back without createLeafInParent still opens a new tab
  ---
  duration_ms: 0.432015
  ...
# Subtest: falling back when createLeafInParent throws still opens a new tab
ok 2486 - falling back when createLeafInParent throws still opens a new tab
  ---
  duration_ms: 0.42964
  ...
# Subtest: collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
ok 2487 - collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
  ---
  duration_ms: 2.354898
  ...
# Subtest: getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
ok 2488 - getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
  ---
  duration_ms: 2.079592
  ...
# Subtest: getProjectBlockState reports an open external prerequisite
ok 2489 - getProjectBlockState reports an open external prerequisite
  ---
  duration_ms: 0.557575
  ...
# Subtest: getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
ok 2490 - getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
  ---
  duration_ms: 0.531476
  ...
# Subtest: getProjectBlockState scheduledValue override is the inline date, not frontmatter
ok 2491 - getProjectBlockState scheduledValue override is the inline date, not frontmatter
  ---
  duration_ms: 0.395576
  ...
# Subtest: getProjectBlockState skips internal and archive Depends-On links
ok 2492 - getProjectBlockState skips internal and archive Depends-On links
  ---
  duration_ms: 0.32454
  ...
# Subtest: getProjectBlockState is a no-op for terminal, daily, and non-project notes
ok 2493 - getProjectBlockState is a no-op for terminal, daily, and non-project notes
  ---
  duration_ms: 0.555111
  ...
# Subtest: projectLooksBlockedByPrjShortcut is the single [?] ^prj row
ok 2494 - projectLooksBlockedByPrjShortcut is the single [?] ^prj row
  ---
  duration_ms: 0.226282
  ...
# Subtest: taskHasProjectBlockedTag is token-bounded and does not match \#prj
ok 2495 - taskHasProjectBlockedTag is token-bounded and does not match \#prj
  ---
  duration_ms: 0.296756
  ...
# Subtest: setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
ok 2496 - setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
  ---
  duration_ms: 0.814035
  ...
# Subtest: reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
ok 2497 - reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
  ---
  duration_ms: 0.413831
  ...
# Subtest: reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
ok 2498 - reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
  ---
  duration_ms: 0.239768
  ...
# Subtest: reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
ok 2499 - reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
  ---
  duration_ms: 0.168733
  ...
# Subtest: ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
ok 2500 - ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
  ---
  duration_ms: 4.623221
  ...
# Subtest: recovery gate keeps a resident of a blocked project blocked after own deps close
ok 2501 - recovery gate keeps a resident of a blocked project blocked after own deps close
  ---
  duration_ms: 1.891823
  ...
# Subtest: recovery gate blocks residents on a future inline project date with no deps
ok 2502 - recovery gate blocks residents on a future inline project date with no deps
  ---
  duration_ms: 0.464317
  ...
# Subtest: planDeferredPomodoroLinkCleanup always deletes a last-child open entry
ok 2503 - planDeferredPomodoroLinkCleanup always deletes a last-child open entry
  ---
  duration_ms: 1.634772
  ...
# Subtest: TICKLER notice uses unblocked <date> when returnedBy is unblocked
ok 2504 - TICKLER notice uses unblocked <date> when returnedBy is unblocked
  ---
  duration_ms: 0.42892
  ...
# Subtest: recognition: a `^prj` parent in a project note carries its residents
ok 2505 - recognition: a `^prj` parent in a project note carries its residents
  ---
  duration_ms: 2.969942
  ...
# Subtest: recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
ok 2506 - recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
  ---
  duration_ms: 0.488884
  ...
# Subtest: add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
ok 2507 - add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
  ---
  duration_ms: 5.001122
  ...
# Subtest: add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
ok 2508 - add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
  ---
  duration_ms: 2.65438
  ...
# Subtest: guards: a same-note add to `^prj` refuses, including mixed batches
ok 2509 - guards: a same-note add to `^prj` refuses, including mixed batches
  ---
  duration_ms: 0.876133
  ...
# Subtest: guards: the stage disables same-note rows for `^prj` with `inside this project`
ok 2510 - guards: the stage disables same-note rows for `^prj` with `inside this project`
  ---
  duration_ms: 1.135429
  ...
# Subtest: guards: cycle detection includes the implicit resident edges (§13.6)
ok 2511 - guards: cycle detection includes the implicit resident edges (§13.6)
  ---
  duration_ms: 1.338295
  ...
# Subtest: removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
ok 2512 - removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
  ---
  duration_ms: 3.744881
  ...
# Subtest: removal: a resident with its own reason stays `[?]` without the tag (PDB3)
ok 2513 - removal: a resident with its own reason stays `[?]` without the tag (PDB3)
  ---
  duration_ms: 1.527446
  ...
# Subtest: removal without a registry defers to reconcile: residents keep `[?]` and the tag
ok 2514 - removal without a registry defers to reconcile: residents keep `[?]` and the tag
  ---
  duration_ms: 1.369305
  ...
# Subtest: writer: one gesture commits `^prj` and its residents in a single undo group
ok 2515 - writer: one gesture commits `^prj` and its residents in a single undo group
  ---
  duration_ms: 1.032031
  ...
# Subtest: writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
ok 2516 - writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
  ---
  duration_ms: 2.337836
  ...
# Subtest: notices: the project strings name the task, the flips, and the Pomodoro cleanup
ok 2517 - notices: the project strings name the task, the flips, and the Pomodoro cleanup
  ---
  duration_ms: 0.285977
  ...
# Subtest: mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
ok 2518 - mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
  ---
  duration_ms: 0.209481
  ...
# Subtest: api v3: removeDependencyByRef delegates removals to the single-transaction writer
ok 2519 - api v3: removeDependencyByRef delegates removals to the single-transaction writer
  ---
  duration_ms: 0.690259
  ...
# Subtest: api v3: openDependencyStageForRef opens the Depends on stage on the owning task
ok 2520 - api v3: openDependencyStageForRef opens the Depends on stage on the owning task
  ---
  duration_ms: 0.283882
  ...
# Subtest: internal links stay on the line but leave the field (PDR7)
ok 2521 - internal links stay on the line but leave the field (PDR7)
  ---
  duration_ms: 0.619273
  ...
# Subtest: removal from an unblocked ^prj never recovers own-reason residents (§13.10)
ok 2522 - removal from an unblocked ^prj never recovers own-reason residents (§13.10)
  ---
  duration_ms: 0.439309
  ...
# Subtest: resident recovery touches only tagged residents (§13.10)
ok 2523 - resident recovery touches only tagged residents (§13.10)
  ---
  duration_ms: 0.962708
  ...
# Subtest: stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
ok 2524 - stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
  ---
  duration_ms: 0.849913
  ...
# Subtest: projectDependentResidentKeys lists open residents with block ids
ok 2525 - projectDependentResidentKeys lists open residents with block ids
  ---
  duration_ms: 0.301907
  ...
# Subtest: navNoteScopeFlags marks daily notes; a missing writer stays null
ok 2526 - navNoteScopeFlags marks daily notes; a missing writer stays null
  ---
  duration_ms: 0.265968
  ...
# Subtest: reconcileBlockedScheduledTaskLine forwards scope flags to the writer
ok 2527 - reconcileBlockedScheduledTaskLine forwards scope flags to the writer
  ---
  duration_ms: 0.130399
  ...
# Subtest: parseProjectNoteFrontmatter ignores leftover scheduled keys
ok 2528 - parseProjectNoteFrontmatter ignores leftover scheduled keys
  ---
  duration_ms: 0.455851
  ...
# Subtest: formatTaskMoveProjectCountsNotice names blocked and recovered counts
ok 2529 - formatTaskMoveProjectCountsNotice names blocked and recovered counts
  ---
  duration_ms: 0.129668
  ...
# Subtest: PDS15: projectParentTarget keeps the path and drops alias and heading
ok 2530 - PDS15: projectParentTarget keeps the path and drops alias and heading
  ---
  duration_ms: 1.139045
  ...
# Subtest: PDS6: list-form, missing, and non-wikilink parents yield none
ok 2531 - PDS6: list-form, missing, and non-wikilink parents yield none
  ---
  duration_ms: 0.486509
  ...
# Subtest: PDS15: resolveProjectParentPath accepts alias, path, and heading forms
ok 2532 - PDS15: resolveProjectParentPath accepts alias, path, and heading forms
  ---
  duration_ms: 0.439119
  ...
# Subtest: PDS6: self, unresolved, and ambiguous basenames yield no parent
ok 2533 - PDS6: self, unresolved, and ambiguous basenames yield no parent
  ---
  duration_ms: 0.17781
  ...
# Subtest: buildProjectChildrenMap and descendants BFS skip cycles and cap depth
ok 2534 - buildProjectChildrenMap and descendants BFS skip cycles and cap depth
  ---
  duration_ms: 3.56125
  ...
# Subtest: PDS6: area, terminal, daily, and self-parent notes are not children
ok 2535 - PDS6: area, terminal, daily, and self-parent notes are not children
  ---
  duration_ms: 0.544089
  ...
# Subtest: PDG8: planner blocks child and grandchild ^prj and residents
ok 2536 - PDG8: planner blocks child and grandchild ^prj and residents
  ---
  duration_ms: 3.090191
  ...
# Subtest: PDG9: planner recovers tagged descendants with [unblocked::]
ok 2537 - PDG9: planner recovers tagged descendants with [unblocked::]
  ---
  duration_ms: 1.421556
  ...
# Subtest: PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
ok 2538 - PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
  ---
  duration_ms: 1.82204
  ...
# Subtest: PDG11: a tagged root re-asserts descendant tags and recovers nothing
ok 2539 - PDG11: a tagged root re-asserts descendant tags and recovers nothing
  ---
  duration_ms: 0.815597
  ...
# Subtest: tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
ok 2540 - tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
  ---
  duration_ms: 0.245949
  ...
# Subtest: tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
ok 2541 - tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
  ---
  duration_ms: 1.54959
  ...
# Subtest: tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
ok 2542 - tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
  ---
  duration_ms: 0.157921
  ...
# Subtest: tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
ok 2543 - tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
  ---
  duration_ms: 1.789879
  ...
# Subtest: PDG13: failProjectPrjInternalAdd refuses descendant targets
ok 2544 - PDG13: failProjectPrjInternalAdd refuses descendant targets
  ---
  duration_ms: 0.241722
  ...
# Subtest: PDG13: planDependencyEdit refuses a descendant add from the files map
ok 2545 - PDG13: planDependencyEdit refuses a descendant add from the files map
  ---
  duration_ms: 1.174874
  ...
# Subtest: PDG13: the stage disables descendant rows
ok 2546 - PDG13: the stage disables descendant rows
  ---
  duration_ms: 1.280917
  ...
# Subtest: reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
ok 2547 - reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
  ---
  duration_ms: 0.307588
  ...
# Subtest: tag proxy: removing the last own dep of a tagged ^prj recovers nobody
ok 2548 - tag proxy: removing the last own dep of a tagged ^prj recovers nobody
  ---
  duration_ms: 2.390877
  ...
# Subtest: PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
ok 2549 - PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
  ---
  duration_ms: 31.535471
  ...
# Subtest: PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
ok 2550 - PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
  ---
  duration_ms: 7.852997
  ...
# Subtest: PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
ok 2551 - PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
  ---
  duration_ms: 6.36176
  ...
# Subtest: PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
ok 2552 - PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
  ---
  duration_ms: 4.186857
  ...
# Subtest: PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
ok 2553 - PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
  ---
  duration_ms: 5.543378
  ...
# Subtest: PDG12: moving the project date due recovers descendants
ok 2554 - PDG12: moving the project date due recovers descendants
  ---
  duration_ms: 4.038594
  ...
# Subtest: PDG12: deleting the project date recovers descendants
ok 2555 - PDG12: deleting the project date recovers descendants
  ---
  duration_ms: 3.172439
  ...
# Subtest: PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
ok 2556 - PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
  ---
  duration_ms: 6.03163
  ...
# Subtest: PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
ok 2557 - PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
  ---
  duration_ms: 4.439238
  ...
# Subtest: Task Link Depends on writer preserves the internal-target guard on a project task
ok 2558 - Task Link Depends on writer preserves the internal-target guard on a project task
  ---
  duration_ms: 1.142571
  ...
# Subtest: api v3 removeDependencyByRef runs the recovery cascade for a linked project task
ok 2559 - api v3 removeDependencyByRef runs the recovery cascade for a linked project task
  ---
  duration_ms: 3.279051
  ...
# Subtest: counted Schedule writer cascades a future date through descendants
ok 2560 - counted Schedule writer cascades a future date through descendants
  ---
  duration_ms: 3.648579
  ...
# Subtest: counted subtree roots are ancestor-first and each descendant note is planned once
ok 2561 - counted subtree roots are ancestor-first and each descendant note is planned once
  ---
  duration_ms: 2.014659
  ...
# Subtest: Ctrl+D on the Depends on row removes the line and recovers the subtree
ok 2562 - Ctrl+D on the Depends on row removes the line and recovers the subtree
  ---
  duration_ms: 4.374716
  ...
# Subtest: a ^prj with no children reads no other note
ok 2563 - a ^prj with no children reads no other note
  ---
  duration_ms: 0.264676
  ...
# Subtest: single seeds from raw text, not display decorations
ok 2564 - single seeds from raw text, not display decorations
  ---
  duration_ms: 8.616467
  ...
# Subtest: legacy valid free wins; invalid and taken fall through
ok 2565 - legacy valid free wins; invalid and taken fall through
  ---
  duration_ms: 1.43476
  ...
# Subtest: batch reserves suffixes for two same-text tasks
ok 2566 - batch reserves suffixes for two same-text tasks
  ---
  duration_ms: 0.826048
  ...
# Subtest: counted-source, vault-single, and vault-counted seed per mode
ok 2567 - counted-source, vault-single, and vault-counted seed per mode
  ---
  duration_ms: 0.998597
  ...
# Subtest: cross-note uses the target note, never the dependent fallback
ok 2568 - cross-note uses the target note, never the dependent fallback
  ---
  duration_ms: 1.014888
  ...
# Subtest: staging writes nothing until confirmed
ok 2569 - staging writes nothing until confirmed
  ---
  duration_ms: 0.5446
  ...
# Subtest: Less often picker renders actual rows from 90 days and Escape writes nothing
ok 2570 - Less often picker renders actual rows from 90 days and Escape writes nothing
  ---
  duration_ms: 5.65452
  ...
# Subtest: Less often picker renders actual rows from 120 days and Escape writes nothing
ok 2571 - Less often picker renders actual rows from 120 days and Escape writes nothing
  ---
  duration_ms: 0.583524
  ...
# Subtest: Less often picker renders actual rows from 180 days and Escape writes nothing
ok 2572 - Less often picker renders actual rows from 180 days and Escape writes nothing
  ---
  duration_ms: 0.510135
  ...
# Subtest: renderFooter skips malformed hints and retains valid structured hints
ok 2573 - renderFooter skips malformed hints and retains valid structured hints
  ---
  duration_ms: 0.255378
  ...
# Subtest: Pending refresh modal previews the dated Work Log and confirms once
ok 2574 - Pending refresh modal previews the dated Work Log and confirms once
  ---
  duration_ms: 1.250308
  ...
# Subtest: dismissing the Pending refresh modal cancels without a summary
ok 2575 - dismissing the Pending refresh modal cancels without a summary
  ---
  duration_ms: 0.307858
  ...
# Subtest: nav LK1–LK18 parse relation grammar and reject the other relation parser
ok 2576 - nav LK1–LK18 parse relation grammar and reject the other relation parser
  ---
  duration_ms: 2.689286
  ...
# Subtest: nav LK14–LK19 context and cross-parse rules
ok 2577 - nav LK14–LK19 context and cross-parse rules
  ---
  duration_ms: 0.57562
  ...
# Subtest: nav MC5 refuses relation embeds and MC16 keeps LINKS while dropping LINKED FROM
ok 2578 - nav MC5 refuses relation embeds and MC16 keeps LINKS while dropping LINKED FROM
  ---
  duration_ms: 1.349859
  ...
# Subtest: nav MC15 hand-edit mirror ignores relation-only bursts and notices LINKED FROM once
ok 2579 - nav MC15 hand-edit mirror ignores relation-only bursts and notices LINKED FROM once
  ---
  duration_ms: 2.784589
  ...
# Subtest: Alt+N release from a NEXT landing advances with one composed toast
ok 2580 - Alt+N release from a NEXT landing advances with one composed toast
  ---
  duration_ms: 23.33558
  ...
# Subtest: counted Alt+N lands past every handled key in one jump
ok 2581 - counted Alt+N lands past every handled key in one jump
  ---
  duration_ms: 11.398059
  ...
# Subtest: a cancelled Alt+N release prompt stays and frees the lock
ok 2582 - a cancelled Alt+N release prompt stays and frees the lock
  ---
  duration_ms: 11.941628
  ...
# Subtest: Alt+N on a checklist landing stays with the plain notice
ok 2583 - Alt+N on a checklist landing stays with the plain notice
  ---
  duration_ms: 9.913514
  ...
# Subtest: Alt+N off a landing behaves exactly as today
ok 2584 - Alt+N off a landing behaves exactly as today
  ---
  duration_ms: 9.453163
  ...
# Subtest: Alt+N while the gesture lock is held is swallowed
ok 2585 - Alt+N while the gesture lock is held is swallowed
  ---
  duration_ms: 9.087638
  ...
# Subtest: a Task Card priority commit on NEXT advances, landing after the rich card
ok 2586 - a Task Card priority commit on NEXT advances, landing after the rich card
  ---
  duration_ms: 29.349545
  ...
# Subtest: dismissing the Task Card stays and frees the lock
ok 2587 - dismissing the Task Card stays and frees the lock
  ---
  duration_ms: 11.81128
  ...
# Subtest: a frontmatter-only project edit from the card stays
ok 2588 - a frontmatter-only project edit from the card stays
  ---
  duration_ms: 11.271417
  ...
# Subtest: a same-day priority schedule on a checklist row stays
ok 2589 - a same-day priority schedule on a checklist row stays
  ---
  duration_ms: 12.610496
  ...
# Subtest: a future schedule on a checklist row advances
ok 2590 - a future schedule on a checklist row advances
  ---
  duration_ms: 18.006178
  ...
# Subtest: a Task Card cancel on a checklist row advances with the cancel card first
ok 2591 - a Task Card cancel on a checklist row advances with the cancel card first
  ---
  duration_ms: 14.300534
  ...
# Subtest: Ctrl+Shift+M from a landing follows the task and never advances
ok 2592 - Ctrl+Shift+M from a landing follows the task and never advances
  ---
  duration_ms: 15.65089
  ...
# Subtest: Ctrl+Shift+M from a checklist landing keeps the destination focus
ok 2593 - Ctrl+Shift+M from a checklist landing keeps the destination focus
  ---
  duration_ms: 12.041148
  ...
# Subtest: ]s after a landed move resumes at the successor despite the line shift
ok 2594 - ]s after a landed move resumes at the successor despite the line shift
  ---
  duration_ms: 32.962355
  ...
# Subtest: [s after a landed move resumes at the predecessor
ok 2595 - [s after a landed move resumes at the predecessor
  ---
  duration_ms: 11.412468
  ...
# Subtest: a counted move from a landing resumes past every moved target
ok 2596 - a counted move from a landing resumes past every moved target
  ---
  duration_ms: 11.135316
  ...
# Subtest: counted Ctrl+Shift+M command dispatch preserves a landed move count
ok 2597 - counted Ctrl+Shift+M command dispatch preserves a landed move count
  ---
  duration_ms: 20.912562
  ...
# Subtest: a stale landing is not parked
ok 2598 - a stale landing is not parked
  ---
  duration_ms: 11.41949
  ...
# Subtest: Ctrl+Shift+M while the gesture lock is held is swallowed
ok 2599 - Ctrl+Shift+M while the gesture lock is held is swallowed
  ---
  duration_ms: 0.738911
  ...
# Subtest: dismissing the move picker stays and frees the lock
ok 2600 - dismissing the move picker stays and frees the lock
  ---
  duration_ms: 10.416073
  ...
# Subtest: Ctrl+Shift+M off a landing behaves exactly as today
ok 2601 - Ctrl+Shift+M off a landing behaves exactly as today
  ---
  duration_ms: 10.301425
  ...
# Subtest: answer, move, answer stays in queue order past an accumulator alias
ok 2602 - answer, move, answer stays in queue order past an accumulator alias
  ---
  duration_ms: 3.185053
  ...
# Subtest: a move park ignores a stale accumulator alias
ok 2603 - a move park ignores a stale accumulator alias
  ---
  duration_ms: 0.611549
  ...
# Subtest: a re-indexed origin still advances from the landed row
ok 2604 - a re-indexed origin still advances from the landed row
  ---
  duration_ms: 3.842259
  ...
# Subtest: a landed move park clears the current review task
ok 2605 - a landed move park clears the current review task
  ---
  duration_ms: 0.462624
  ...
# Subtest: predicate: reviewOutcomeResolves across tiers and kinds
ok 2606 - predicate: reviewOutcomeResolves across tiers and kinds
  ---
  duration_ms: 3.053613
  ...
# Subtest: findReviewResumeIndex identifies rows by path and text
ok 2607 - findReviewResumeIndex identifies rows by path and text
  ---
  duration_ms: 0.444228
  ...
# Subtest: buildReviewMoveAnchor parks text-identified resume neighbours
ok 2608 - buildReviewMoveAnchor parks text-identified resume neighbours
  ---
  duration_ms: 0.788767
  ...
# Subtest: planReviewJump with a move anchor resumes at the walk neighbour
ok 2609 - planReviewJump with a move anchor resumes at the walk neighbour
  ---
  duration_ms: 1.49715
  ...
# Subtest: capture: null off a landing
ok 2610 - capture: null off a landing
  ---
  duration_ms: 5.00505
  ...
# Subtest: capture: frozen origin shape, BUSY while locked, expiry
ok 2611 - capture: frozen origin shape, BUSY while locked, expiry
  ---
  duration_ms: 0.728321
  ...
# Subtest: successor picker keeps a captured completion locked through selection and one walk toast
ok 2612 - successor picker keeps a captured completion locked through selection and one walk toast
  ---
  duration_ms: 18.140545
  ...
# Subtest: continue: refuses stale origins, showing the notice once
ok 2613 - continue: refuses stale origins, showing the notice once
  ---
  duration_ms: 6.580619
  ...
# Subtest: continue: stays on null and non-resolving outcomes
ok 2614 - continue: stays on null and non-resolving outcomes
  ---
  duration_ms: 2.415984
  ...
# Subtest: continue: stays for lane answers and mixed-version completes on checklist rows
ok 2615 - continue: stays for lane answers and mixed-version completes on checklist rows
  ---
  duration_ms: 3.736286
  ...
# Subtest: continue: a resolving lane answer advances exactly once with one composed toast
ok 2616 - continue: a resolving lane answer advances exactly once with one composed toast
  ---
  duration_ms: 4.35601
  ...
# Subtest: continue: counted handled refs land past every handled key in one jump
ok 2617 - continue: counted handled refs land past every handled key in one jump
  ---
  duration_ms: 2.767286
  ...
# Subtest: continue: wrap is announced and the empty queue composes the empty notice
ok 2618 - continue: wrap is announced and the empty queue composes the empty notice
  ---
  duration_ms: 3.692
  ...
# Subtest: continue: anchor-only planning survives cursor drift and lagging queues
ok 2619 - continue: anchor-only planning survives cursor drift and lagging queues
  ---
  duration_ms: 2.152611
  ...
# Subtest: continue: POST origins never wrap
ok 2620 - continue: POST origins never wrap
  ---
  duration_ms: 1.078359
  ...
# Subtest: complete: the last lane row before POST stays with the next-step toast
ok 2621 - complete: the last lane row before POST stays with the next-step toast
  ---
  duration_ms: 0.850274
  ...
# Subtest: complete: a wrap onto a skipped PRE row stays
ok 2622 - complete: a wrap onto a skipped PRE row stays
  ---
  duration_ms: 0.883347
  ...
# Subtest: complete: a step into ROTTEN shows the boundary line
ok 2623 - complete: a step into ROTTEN shows the boundary line
  ---
  duration_ms: 2.118156
  ...
# Subtest: busy: walk keys, refresh, claim, and capture are swallowed in the settle window
ok 2624 - busy: walk keys, refresh, claim, and capture are swallowed in the settle window
  ---
  duration_ms: 3.688736
  ...
# Subtest: advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
ok 2625 - advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
  ---
  duration_ms: 3.361911
  ...
# Subtest: advance: decay choices advance except reword, with no preamble of their own
ok 2626 - advance: decay choices advance except reword, with no preamble of their own
  ---
  duration_ms: 0.539621
  ...
# Subtest: jump history: same-note and cross-note auto-advances record, and <C-o> returns
ok 2627 - jump history: same-note and cross-note auto-advances record, and <C-o> returns
  ---
  duration_ms: 6.01021
  ...
# Subtest: jump history: a manual ]s also records its landing
ok 2628 - jump history: a manual ]s also records its landing
  ---
  duration_ms: 0.759681
  ...
# Subtest: api: reviewWalk v3 is frozen with version 1, degrades null, never throws
ok 2629 - api: reviewWalk v3 is frozen with version 1, degrades null, never throws
  ---
  duration_ms: 1.752427
  ...
# Subtest: walk identity: a stale accumulator key never moves the anchor
ok 2630 - walk identity: a stale accumulator key never moves the anchor
  ---
  duration_ms: 0.280316
  ...
# Subtest: walk identity: a lagging answered row stays excluded
ok 2631 - walk identity: a lagging answered row stays excluded
  ---
  duration_ms: 0.15177
  ...
# Subtest: walk identity: a line-shifting answer lands on the true successor by text
ok 2632 - walk identity: a line-shifting answer lands on the true successor by text
  ---
  duration_ms: 0.271088
  ...
# Subtest: walk identity: legacy anchors without text resolve as before
ok 2633 - walk identity: legacy anchors without text resolve as before
  ---
  duration_ms: 0.240339
  ...
# Subtest: walk identity: matchFreshStampRefs prefers text over line
ok 2634 - walk identity: matchFreshStampRefs prefers text over line
  ---
  duration_ms: 0.138425
  ...
# Subtest: walk identity: collectReviewAnswerKeys separates position from exclusion
ok 2635 - walk identity: collectReviewAnswerKeys separates position from exclusion
  ---
  duration_ms: 0.391438
  ...
# Subtest: return: planReviewWalkReturn pure decisions
ok 2636 - return: planReviewWalkReturn pure decisions
  ---
  duration_ms: 0.270777
  ...
# Subtest: return: same-note ]s returns then steps, both directions
ok 2637 - return: same-note ]s returns then steps, both directions
  ---
  duration_ms: 1.032572
  ...
# Subtest: return: a different due row returns instead of stepping from there
ok 2638 - return: a different due row returns instead of stepping from there
  ---
  duration_ms: 0.409112
  ...
# Subtest: return: cross-note return re-arms and records <C-o>
ok 2639 - return: cross-note return re-arms and records <C-o>
  ---
  duration_ms: 5.383041
  ...
# Subtest: return: a count is consumed and ignored
ok 2640 - return: a count is consumed and ignored
  ---
  duration_ms: 0.676692
  ...
# Subtest: return: endpoints never return
ok 2641 - return: endpoints never return
  ---
  duration_ms: 0.570529
  ...
# Subtest: return: its own stamp ends it
ok 2642 - return: its own stamp ends it
  ---
  duration_ms: 0.7699
  ...
# Subtest: return: a stamp elsewhere does not end it
ok 2643 - return: a stamp elsewhere does not end it
  ---
  duration_ms: 0.593573
  ...
# Subtest: return: answers move the current task, a stopped Ctrl+Enter clears it
ok 2644 - return: answers move the current task, a stopped Ctrl+Enter clears it
  ---
  duration_ms: 3.626365
  ...
# Subtest: return: a stale landing falls through in the same press
ok 2645 - return: a stale landing falls through in the same press
  ---
  duration_ms: 0.333036
  ...
# Subtest: return: a day change never returns
ok 2646 - return: a day change never returns
  ---
  duration_ms: 0.447434
  ...
# Subtest: predicate: reviewOutcomeResolves for the RECURRING resolution table
ok 2647 - predicate: reviewOutcomeResolves for the RECURRING resolution table
  ---
  duration_ms: 0.439009
  ...
# Subtest: recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
ok 2648 - recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
  ---
  duration_ms: 0.183791
  ...
# Subtest: return: a RECURRING landing rearms the current-task return
ok 2649 - return: a RECURRING landing rearms the current-task return
  ---
  duration_ms: 0.279655
  ...
# Subtest: review answer outcome vectors map to the schema vocabulary
ok 2650 - review answer outcome vectors map to the schema vocabulary
  ---
  duration_ms: 1.462773
  ...
# Subtest: event builder uses the walk row key and its tier, once per distinct key
ok 2651 - event builder uses the walk row key and its tier, once per distinct key
  ---
  duration_ms: 0.880071
  ...
# Subtest: journal appends are queued and failures retain events without failing answers
ok 2652 - journal appends are queued and failures retain events without failing answers
  ---
  duration_ms: 4.525714
  ...
# Subtest: card after-line outcomes map done, drop, defer, sequence, and card
ok 2653 - card after-line outcomes map done, drop, defer, sequence, and card
  ---
  duration_ms: 1.054955
  ...
# Subtest: journal events carry plugin@manifest version with a 2.x fallback
ok 2654 - journal events carry plugin@manifest version with a 2.x fallback
  ---
  duration_ms: 1.022362
  ...
# Subtest: write failures show one notice per burst and a recovery notice
ok 2655 - write failures show one notice per burst and a recovery notice
  ---
  duration_ms: 0.864411
  ...
# Subtest: missing api.stats shows one session notice and later delivers retained events
ok 2656 - missing api.stats shows one session notice and later delivers retained events
  ---
  duration_ms: 1.087968
  ...
# Subtest: validation rejects drop the event and continue the drain
ok 2657 - validation rejects drop the event and continue the drain
  ---
  duration_ms: 0.742869
  ...
# Subtest: pending journal events cap at 500 and warn once per burst
ok 2658 - pending journal events cap at 500 and warn once per burst
  ---
  duration_ms: 2.284653
  ...
# Subtest: decay config defaults to enabled with one roll per level
ok 2659 - decay config defaults to enabled with one roll per level
  ---
  duration_ms: 2.539902
  ...
# Subtest: decay:false disables decay and level rolls are accepted but ignored
ok 2660 - decay:false disables decay and level rolls are accepted but ignored
  ---
  duration_ms: 0.698063
  ...
# Subtest: decay.rolls sets the limit and levels[].rolls overrides it
ok 2661 - decay.rolls sets the limit and levels[].rolls overrides it
  ---
  duration_ms: 0.227876
  ...
# Subtest: decay config rejects bad rolls, unknown keys and non-priority use
ok 2662 - decay config rejects bad rolls, unknown keys and non-priority use
  ---
  duration_ms: 0.522518
  ...
# Subtest: classifyScheduleLogRollReason sorts automatic heads from deliberate ones
ok 2663 - classifyScheduleLogRollReason sorts automatic heads from deliberate ones
  ---
  duration_ms: 0.646124
  ...
# Subtest: conformance vectors 1-10: streaks at P2 with the default limit
ok 2664 - conformance vectors 1-10: streaks at P2 with the default limit
  ---
  duration_ms: 2.929856
  ...
# Subtest: conformance vectors 11-15: custom limits, disabled decay and edges
ok 2665 - conformance vectors 11-15: custom limits, disabled decay and edges
  ---
  duration_ms: 0.786412
  ...
# Subtest: the streak reader follows log grammar: legacy labels, nesting and stops
ok 2666 - the streak reader follows log grammar: legacy labels, nesting and stops
  ---
  duration_ms: 0.490176
  ...
# Subtest: rollPriorityRecommendationDate avoids the current date when the window has room
ok 2667 - rollPriorityRecommendationDate avoids the current date when the window has room
  ---
  duration_ms: 0.614284
  ...
# Subtest: decay and cancel reason formatters use the exact ladder copy
ok 2668 - decay and cancel reason formatters use the exact ladder copy
  ---
  duration_ms: 0.452525
  ...
# Subtest: the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
ok 2669 - the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
  ---
  duration_ms: 0.34006
  ...
# Subtest: the planner returns null without a configured priority
ok 2670 - the planner returns null without a configured priority
  ---
  duration_ms: 0.155487
  ...
# Subtest: buildPriorityRollPreviewModel carries the row copy for every kind
ok 2671 - buildPriorityRollPreviewModel carries the row copy for every kind
  ---
  duration_ms: 0.513801
  ...
# Subtest: picker-single recognizes the recommended-roll keypress
ok 2672 - picker-single recognizes the recommended-roll keypress
  ---
  duration_ms: 0.141099
  ...
# Subtest: picker-single stage-two footers carry the recommended-roll hints
ok 2673 - picker-single stage-two footers carry the recommended-roll hints
  ---
  duration_ms: 0.407689
  ...
# Subtest: picker-single shares one roll between the preview and the pinned row
ok 2674 - picker-single shares one roll between the preview and the pinned row
  ---
  duration_ms: 0.341733
  ...
# Subtest: picker-single plans the next-roll hint for the notice chips
ok 2675 - picker-single plans the next-roll hint for the notice chips
  ---
  duration_ms: 0.557244
  ...
# Subtest: picker-single notice cards name the roll, decay and next press
ok 2676 - picker-single notice cards name the roll, decay and next press
  ---
  duration_ms: 1.469206
  ...
# Subtest: picker-single decay payload and preview-target comparison
ok 2677 - picker-single decay payload and preview-target comparison
  ---
  duration_ms: 0.349578
  ...
# Subtest: picker-counted plans one recommendation per target with skips
ok 2678 - picker-counted plans one recommendation per target with skips
  ---
  duration_ms: 1.776803
  ...
# Subtest: picker-counted batch preview, footer and notice copy
ok 2679 - picker-counted batch preview, footer and notice copy
  ---
  duration_ms: 1.448907
  ...
# Subtest: picker-counted composes cancel then set-priority into one postimage
ok 2680 - picker-counted composes cancel then set-priority into one postimage
  ---
  duration_ms: 3.221171
  ...
# Subtest: picker-counted refuses a recurring cancel as one batch
ok 2681 - picker-counted refuses a recurring cancel as one batch
  ---
  duration_ms: 0.409622
  ...
# Subtest: recommended roll recovers with [unblocked::] when the writer is passed
ok 2682 - recommended roll recovers with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.787945
  ...
# Subtest: picker-counted stale lines refuse and new options stay byte-identical
ok 2683 - picker-counted stale lines refuse and new options stay byte-identical
  ---
  duration_ms: 1.016321
  ...
# Subtest: picker-links aggregates one recommendation per note
ok 2684 - picker-links aggregates one recommendation per note
  ---
  duration_ms: 1.081636
  ...
# Subtest: picker-links refuses a recurring cancel as one batch
ok 2685 - picker-links refuses a recurring cancel as one batch
  ---
  duration_ms: 0.373965
  ...
# Subtest: picker-links takes a single recommended roll with Ctrl+Enter
ok 2686 - picker-links takes a single recommended roll with Ctrl+Enter
  ---
  duration_ms: 31.539298
  ...
# Subtest: picker-links shows no pinned roll row in stage two
ok 2687 - picker-links shows no pinned roll row in stage two
  ---
  duration_ms: 5.280735
  ...
# Subtest: picker-links decays and cancels a single Task Link
ok 2688 - picker-links decays and cancels a single Task Link
  ---
  duration_ms: 7.763248
  ...
# Subtest: picker-links applies a mixed batch across two notes
ok 2689 - picker-links applies a mixed batch across two notes
  ---
  duration_ms: 4.658959
  ...
# Subtest: picker-links refuses the whole batch when a linked note changed
ok 2690 - picker-links refuses the whole batch when a linked note changed
  ---
  duration_ms: 2.018906
  ...
# Subtest: picker-links prunes today's open Pomodoro links
ok 2691 - picker-links prunes today's open Pomodoro links
  ---
  duration_ms: 5.046669
  ...
# Subtest: picker-single Ctrl+Enter rolls a P2 task in one undo group
ok 2692 - picker-single Ctrl+Enter rolls a P2 task in one undo group
  ---
  duration_ms: 14.796109
  ...
# Subtest: picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
ok 2693 - picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
  ---
  duration_ms: 11.629541
  ...
# Subtest: picker-single opens a ^prj task on inline scheduled for an immediate roll
ok 2694 - picker-single opens a ^prj task on inline scheduled for an immediate roll
  ---
  duration_ms: 13.451692
  ...
# Subtest: picker-counted opens on scheduled for an immediate mixed batch
ok 2695 - picker-counted opens on scheduled for an immediate mixed batch
  ---
  duration_ms: 13.290906
  ...
# Subtest: picker-links opens on scheduled for an immediate roll
ok 2696 - picker-links opens on scheduled for an immediate roll
  ---
  duration_ms: 11.903853
  ...
# Subtest: picker-single Ctrl+Enter decays a P2 task in one undo group
ok 2697 - picker-single Ctrl+Enter decays a P2 task in one undo group
  ---
  duration_ms: 12.411366
  ...
# Subtest: picker-single Ctrl+Enter cancels a P4 task in one undo group
ok 2698 - picker-single Ctrl+Enter cancels a P4 task in one undo group
  ---
  duration_ms: 13.117965
  ...
# Subtest: picker-single Ctrl+Enter in stage two writes the recommended roll
ok 2699 - picker-single Ctrl+Enter in stage two writes the recommended roll
  ---
  duration_ms: 12.134744
  ...
# Subtest: picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
ok 2700 - picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
  ---
  duration_ms: 3.469827
  ...
# Subtest: picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
ok 2701 - picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
  ---
  duration_ms: 4.334108
  ...
# Subtest: picker-single recurring P4 past the limit refuses and keeps the picker open
ok 2702 - picker-single recurring P4 past the limit refuses and keeps the picker open
  ---
  duration_ms: 11.389043
  ...
# Subtest: picker-single stale tasks refuse and re-render the decay preview
ok 2703 - picker-single stale tasks refuse and re-render the decay preview
  ---
  duration_ms: 12.05367
  ...
# Subtest: picker-single Ctrl+R on the card re-rolls the recommendation date
ok 2704 - picker-single Ctrl+R on the card re-rolls the recommendation date
  ---
  duration_ms: 3.761222
  ...
# Subtest: picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
ok 2705 - picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
  ---
  duration_ms: 1.728922
  ...
# Subtest: picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
ok 2706 - picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
  ---
  duration_ms: 11.478024
  ...
# Subtest: picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
ok 2707 - picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
  ---
  duration_ms: 11.855263
  ...
# Subtest: picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
ok 2708 - picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
  ---
  duration_ms: 11.885789
  ...
# Subtest: picker-counted Ctrl+Enter refuses when a target line changed
ok 2709 - picker-counted Ctrl+Enter refuses when a target line changed
  ---
  duration_ms: 11.97947
  ...
# Subtest: picker-counted Ctrl+Enter refuses a recurring cancel batch
ok 2710 - picker-counted Ctrl+Enter refuses a recurring cancel batch
  ---
  duration_ms: 11.257652
  ...
# Subtest: recommended roll on Pending offers a Work Log with the frozen date
ok 2711 - recommended roll on Pending offers a Work Log with the frozen date
  ---
  duration_ms: 1026.119938
  ...
# Subtest: recommended roll blank summary skips the Work Log without a fallback
ok 2712 - recommended roll blank summary skips the Work Log without a fallback
  ---
  duration_ms: 1033.798885
  ...
# Subtest: Ctrl+Enter in the Work Log stage confirms instead of re-rolling
ok 2713 - Ctrl+Enter in the Work Log stage confirms instead of re-rolling
  ---
  duration_ms: 1096.373329
  ...
# Subtest: counted recommended mixed batch logs only eligible roll and decay targets
ok 2714 - counted recommended mixed batch logs only eligible roll and decay targets
  ---
  duration_ms: 1056.162847
  ...
# Subtest: Task Link recommended roll deletes the emptied Pomodoro in the same daily write
ok 2715 - Task Link recommended roll deletes the emptied Pomodoro in the same daily write
  ---
  duration_ms: 3.721428
  ...
# Subtest: lane commit stamps an open Ready task
ok 2716 - lane commit stamps an open Ready task
  ---
  duration_ms: 2.824174
  ...
# Subtest: lane release stamps an open Next task
ok 2717 - lane release stamps an open Next task
  ---
  duration_ms: 0.41336
  ...
# Subtest: lane without a stamper leaves lines as they were
ok 2718 - lane without a stamper leaves lines as they were
  ---
  duration_ms: 0.180314
  ...
# Subtest: counted property set stamps every rewritten open task
ok 2719 - counted property set stamps every rewritten open task
  ---
  duration_ms: 2.087277
  ...
# Subtest: counted delete-property stamps the rewritten task
ok 2720 - counted delete-property stamps the rewritten task
  ---
  duration_ms: 0.516556
  ...
# Subtest: stamp lands before the suffix after a priority edit on a stamped line
ok 2721 - stamp lands before the suffix after a priority edit on a stamped line
  ---
  duration_ms: 0.490898
  ...
# Subtest: recurring tasks are never stamped
ok 2722 - recurring tasks are never stamped
  ---
  duration_ms: 0.279243
  ...
# Subtest: cancel never stamps
ok 2723 - cancel never stamps
  ---
  duration_ms: 1.037131
  ...
# Subtest: fresh and refresh never go through the end-append writers
ok 2724 - fresh and refresh never go through the end-append writers
  ---
  duration_ms: 0.495155
  ...
# Subtest: counted dependency edit stamps the rewritten parent
ok 2725 - counted dependency edit stamps the rewritten parent
  ---
  duration_ms: 5.445542
  ...
# Subtest: moved tasks are stamped at their destination
ok 2726 - moved tasks are stamped at their destination
  ---
  duration_ms: 3.236331
  ...
# Subtest: move without a stamper leaves lines as they were
ok 2727 - move without a stamper leaves lines as they were
  ---
  duration_ms: 0.602
  ...
# Subtest: refresh row shows the effective interval in task mode
ok 2728 - refresh row shows the effective interval in task mode
  ---
  duration_ms: 0.739423
  ...
# Subtest: refresh row hides without the api and on closed tasks
ok 2729 - refresh row hides without the api and on closed tasks
  ---
  duration_ms: 0.126392
  ...
# Subtest: refresh row covers counted and link modes, including mixed
ok 2730 - refresh row covers counted and link modes, including mixed
  ---
  duration_ms: 0.262952
  ...
# Subtest: refresh value items offer presets and use default
ok 2731 - refresh value items offer presets and use default
  ---
  duration_ms: 0.693134
  ...
# Subtest: setRefreshLine stamps and sets or clears the interval
ok 2732 - setRefreshLine stamps and sets or clears the interval
  ---
  duration_ms: 0.426605
  ...
# Subtest: 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
ok 2733 - 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
  ---
  duration_ms: 8.905139
  ...
# Subtest: Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
ok 2734 - Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
  ---
  duration_ms: 2.91167
  ...
# Subtest: filtering expands matches, collapse state survives clearing, and hidden marks still submit
ok 2735 - filtering expands matches, collapse state survives clearing, and hidden marks still submit
  ---
  duration_ms: 4.627877
  ...
# Subtest: group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
ok 2736 - group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
  ---
  duration_ms: 1.346501
  ...
# Subtest: Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
ok 2737 - Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
  ---
  duration_ms: 0.681893
  ...
# Subtest: Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
ok 2738 - Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
  ---
  duration_ms: 3.857798
  ...
# Subtest: the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
ok 2739 - the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
  ---
  duration_ms: 0.755362
  ...
# Subtest: destination override shapes normalize and label
ok 2740 - destination override shapes normalize and label
  ---
  duration_ms: 0.228427
  ...
# Subtest: destination picker detection needs block-id-prompt api v1 with pick
ok 2741 - destination picker detection needs block-id-prompt api v1 with pick
  ---
  duration_ms: 0.408691
  ...
# Subtest: Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks
ok 2742 - Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks
  ---
  duration_ms: 2.536314
  ...
# Subtest: Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked
ok 2743 - Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked
  ---
  duration_ms: 1.019698
  ...
# Subtest: a cancelled destination pick and a missing picker leave rows untouched
ok 2744 - a cancelled destination pick and a missing picker leave rows untouched
  ---
  duration_ms: 1.180003
  ...
# Subtest: unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
ok 2745 - unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
  ---
  duration_ms: 0.81652
  ...
# Subtest: card model builds stable rows, scope metadata, and an existing recommendation
ok 2746 - card model builds stable rows, scope metadata, and an existing recommendation
  ---
  duration_ms: 9.131662
  ...
# Subtest: explicit preview builder matches writer rolls and deduplicates linked targets
ok 2747 - explicit preview builder matches writer rolls and deduplicates linked targets
  ---
  duration_ms: 0.869551
  ...
# Subtest: counted and linked card models report real target counts and mixed values
ok 2748 - counted and linked card models report real target counts and mixed values
  ---
  duration_ms: 4.60316
  ...
# Subtest: priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
ok 2749 - priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
  ---
  duration_ms: 2.362501
  ...
# Subtest: Escape, bare q, and Ctrl+[ close the card; nothing else does
ok 2750 - Escape, bare q, and Ctrl+[ close the card; nothing else does
  ---
  duration_ms: 0.943762
  ...
# Subtest: close keys never fire during composition or inside a text field
ok 2751 - close keys never fire during composition or inside a text field
  ---
  duration_ms: 1.290344
  ...
# Subtest: unavailable actions, input composition, and repeats stay safe
ok 2752 - unavailable actions, input composition, and repeats stay safe
  ---
  duration_ms: 1.840235
  ...
# Subtest: Blocks row summarizes warm-cache dependents and their last open reason
ok 2753 - Blocks row summarizes warm-cache dependents and their last open reason
  ---
  duration_ms: 1.075574
  ...
# Subtest: Blocks row refuses closed tasks and unencodable paths without an id
ok 2754 - Blocks row refuses closed tasks and unencodable paths without an id
  ---
  duration_ms: 1.980503
  ...
# Subtest: key resolver table covers lane state, API availability, and modifier guards
ok 2755 - key resolver table covers lane state, API availability, and modifier guards
  ---
  duration_ms: 1.473294
  ...
# Subtest: recurring cancellation and blocked lanes expose reasons instead of writes
ok 2756 - recurring cancellation and blocked lanes expose reasons instead of writes
  ---
  duration_ms: 0.634072
  ...
# Subtest: identity keys distinguish linked notes that share a line number
ok 2757 - identity keys distinguish linked notes that share a line number
  ---
  duration_ms: 2.046679
  ...
# Subtest: planScheduleReview opens for a bare date and skips when reason is known without Work Log
ok 2758 - planScheduleReview opens for a bare date and skips when reason is known without Work Log
  ---
  duration_ms: 1.18336
  ...
# Subtest: planScheduleReview counts unique tasks when Task Links repeat a target
ok 2759 - planScheduleReview counts unique tasks when Task Links repeat a target
  ---
  duration_ms: 0.407078
  ...
# Subtest: bare date on Ready opens a reason-only review and writes nothing until Enter
ok 2760 - bare date on Ready opens a reason-only review and writes nothing until Enter
  ---
  duration_ms: 23.523048
  ...
# Subtest: typed reason and blank reason on an existing Schedule Log keep per-target rules
ok 2761 - typed reason and blank reason on an existing Schedule Log keep per-target rules
  ---
  duration_ms: 8.792694
  ...
# Subtest: Ready vs Next vs Pending: only Next/Pending show Work summary
ok 2762 - Ready vs Next vs Pending: only Next/Pending show Work summary
  ---
  duration_ms: 11.416422
  ...
# Subtest: inline reason on Ready dispatches immediately; on Next it still reviews Work summary
ok 2763 - inline reason on Ready dispatches immediately; on Next it still reviews Work summary
  ---
  duration_ms: 7.272391
  ...
# Subtest: Tab moves from Reason to Work summary and Enter commits from either field
ok 2764 - Tab moves from Reason to Work summary and Enter commits from either field
  ---
  duration_ms: 2.441594
  ...
# Subtest: Back and Escape at both review fields write nothing
ok 2765 - Back and Escape at both review fields write nothing
  ---
  duration_ms: 5.185825
  ...
# Subtest: a target changed during review refuses with no write
ok 2766 - a target changed during review refuses with no write
  ---
  duration_ms: 2.257301
  ...
# Subtest: counted mixed targets share one review and one adapter call
ok 2767 - counted mixed targets share one review and one adapter call
  ---
  duration_ms: 3.477642
  ...
# Subtest: linked notes with equal line numbers both qualify
ok 2768 - linked notes with equal line numbers both qualify
  ---
  duration_ms: 2.212915
  ...
# Subtest: project lifecycle review names propagation and still writes once
ok 2769 - project lifecycle review names propagation and still writes once
  ---
  duration_ms: 2.281186
  ...
# Subtest: priority picks still skip the combined review and keep Work Log-only prompts
ok 2770 - priority picks still skip the combined review and keep Work Log-only prompts
  ---
  duration_ms: 1.797203
  ...
# Subtest: a typed date from the card's schedule row uses the combined review
ok 2771 - a typed date from the card's schedule row uses the combined review
  ---
  duration_ms: 1.511036
  ...
# Subtest: scheduling a Pending task goes straight to the combined review, never serial prompts
ok 2772 - scheduling a Pending task goes straight to the combined review, never serial prompts
  ---
  duration_ms: 1.284724
  ...
# Subtest: classic parser keeps ISO, M/D, and signed units and ignores concise forms
ok 2773 - classic parser keeps ISO, M/D, and signed units and ignores concise forms
  ---
  duration_ms: 1.35664
  ...
# Subtest: typed schedule resolver covers bare days, units, weekdays, and inline reasons
ok 2774 - typed schedule resolver covers bare days, units, weekdays, and inline reasons
  ---
  duration_ms: 1.126781
  ...
# Subtest: weekdays resolve to the next occurrence strictly after today
ok 2775 - weekdays resolve to the next occurrence strictly after today
  ---
  duration_ms: 0.157701
  ...
# Subtest: invalid leap dates, end-of-month offsets, and December rollover
ok 2776 - invalid leap dates, end-of-month offsets, and December rollover
  ---
  duration_ms: 0.367732
  ...
# Subtest: negative, overflow, malformed, and preset-filter queries are rejected without dates
ok 2777 - negative, overflow, malformed, and preset-filter queries are rejected without dates
  ---
  duration_ms: 0.166788
  ...
# Subtest: DST local-calendar arithmetic stays on calendar days in America/New_York
ok 2778 - DST local-calendar arithmetic stays on calendar days in America/New_York
  ---
  duration_ms: 86.791414
  ...
# Subtest: Task Card date stage previews weekday, ISO, relative distance, and rollover year
ok 2779 - Task Card date stage previews weekday, ISO, relative distance, and rollover year
  ---
  duration_ms: 14.572112
  ...
# Subtest: inline reason is preserved on the preview and skips the reason stage
ok 2780 - inline reason is preserved on the preview and skips the reason stage
  ---
  duration_ms: 11.376389
  ...
# Subtest: Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
ok 2781 - Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
  ---
  duration_ms: 4.406446
  ...
# Subtest: Shift+Enter on a Ready task commits in four gestures without a Work Log
ok 2782 - Shift+Enter on a Ready task commits in four gestures without a Work Log
  ---
  duration_ms: 2.413027
  ...
# Subtest: invalid typed dates render an error preview and do not write
ok 2783 - invalid typed dates render an error preview and do not write
  ---
  duration_ms: 2.450159
  ...
# Subtest: the card's schedule stage always uses the concise resolver
ok 2784 - the card's schedule stage always uses the concise resolver
  ---
  duration_ms: 1.776913
  ...
# Subtest: tomorrow stays a preset filter and is not stolen as a typed date
ok 2785 - tomorrow stays a preset filter and is not stolen as a typed date
  ---
  duration_ms: 1.38785
  ...
# Subtest: mixed Task Links preview one date and freeze that action with the inline reason
ok 2786 - mixed Task Links preview one date and freeze that action with the inline reason
  ---
  duration_ms: 7.330652
  ...
# Subtest: Ctrl+Enter still takes the recommended roll from the Task Card date stage
ok 2787 - Ctrl+Enter still takes the recommended roll from the Task Card date stage
  ---
  duration_ms: 2.661363
  ...
# Subtest: Modal harness models Obsidian 1.14 attachment and idempotent close
ok 2788 - Modal harness models Obsidian 1.14 attachment and idempotent close
  ---
  duration_ms: 2.362592
  ...
# Subtest: styles share key-card tokens and compact Task Card dimensions
ok 2789 - styles share key-card tokens and compact Task Card dimensions
  ---
  duration_ms: 0.412437
  ...
# Subtest: card renderer paints header, banner, strip, stable rows, more, and footer from the model
ok 2790 - card renderer paints header, banner, strip, stable rows, more, and footer from the model
  ---
  duration_ms: 15.140274
  ...
# Subtest: renderer does not consume randomness or invent recommendation data
ok 2791 - renderer does not consume randomness or invent recommendation data
  ---
  duration_ms: 1.773767
  ...
# Subtest: no-recommendation, cancel, mixed, long text, missing API, and error states render
ok 2792 - no-recommendation, cancel, mixed, long text, missing API, and error states render
  ---
  duration_ms: 4.690008
  ...
# Subtest: counted and linked cards disclose mixed values and Task Link notes
ok 2793 - counted and linked cards disclose mixed values and Task Link notes
  ---
  duration_ms: 5.495246
  ...
# Subtest: Ctrl+Shift+P always opens the Task Card, never the classic property list
ok 2794 - Ctrl+Shift+P always opens the Task Card, never the classic property list
  ---
  duration_ms: 3.236181
  ...
# Subtest: the plugin carries no Task Card pilot setting, date gate, or classic preference
ok 2795 - the plugin carries no Task Card pilot setting, date gate, or classic preference
  ---
  duration_ms: 18.841977
  ...
# Subtest: a leftover persisted taskCard flag is ignored and never rewritten
ok 2796 - a leftover persisted taskCard flag is ignored and never rewritten
  ---
  duration_ms: 6.490817
  ...
# Subtest: palette command is named Task card (set properties)
ok 2797 - palette command is named Task card (set properties)
  ---
  duration_ms: 10.511845
  ...
# Subtest: Task Card opens the compact card with dialog semantics and a close control
ok 2798 - Task Card opens the compact card with dialog semantics and a close control
  ---
  duration_ms: 1.706179
  ...
# Subtest: a More row opens that property's value stage, never a filter list, and Back restores the card
ok 2799 - a More row opens that property's value stage, never a filter list, and Back restores the card
  ---
  duration_ms: 3.473805
  ...
# Subtest: after open the actions list, not the Close button, has focus
ok 2800 - after open the actions list, not the Close button, has focus
  ---
  duration_ms: 4.454578
  ...
# Subtest: clicking card text keeps the card key router active exactly once
ok 2801 - clicking card text keeps the card key router active exactly once
  ---
  duration_ms: 16.624431
  ...
# Subtest: Ready card writes close from a key, P1 click, recommendations, and Alt+N
ok 2802 - Ready card writes close from a key, P1 click, recommendations, and Alt+N
  ---
  duration_ms: 7.13746
  ...
# Subtest: Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
ok 2803 - Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
  ---
  duration_ms: 4.452093
  ...
# Subtest: Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
ok 2804 - Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
  ---
  duration_ms: 3.783567
  ...
# Subtest: Ctrl+R recomputes and repaints the card recommendation
ok 2805 - Ctrl+R recomputes and repaints the card recommendation
  ---
  duration_ms: 1.442886
  ...
# Subtest: Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
ok 2806 - Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
  ---
  duration_ms: 27.031988
  ...
# Subtest: Task Link opens focused while resolving and consumes keys without replay
ok 2807 - Task Link opens focused while resolving and consumes keys without replay
  ---
  duration_ms: 4.797102
  ...
# Subtest: Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card
ok 2808 - Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card
  ---
  duration_ms: 2.73336
  ...
# Subtest: Ctrl+Shift+Alt+B on a Task Link opens the linked Blocks stage
ok 2809 - Ctrl+Shift+Alt+B on a Task Link opens the linked Blocks stage
  ---
  duration_ms: 1.667655
  ...
# Subtest: Task Link count replacement and source edits invalidate old resolutions
ok 2810 - Task Link count replacement and source edits invalidate old resolutions
  ---
  duration_ms: 1.208569
  ...
# Subtest: Task Link resolution failure and plugin unload close their shells
ok 2811 - Task Link resolution failure and plugin unload close their shells
  ---
  duration_ms: 1.985692
  ...
# Subtest: direct Depends on entry opens the dependency stage without painting the card or the list
ok 2812 - direct Depends on entry opens the dependency stage without painting the card or the list
  ---
  duration_ms: 1.033594
  ...
# Subtest: a direct stage for an unconfigured property closes instead of leaving an empty modal
ok 2813 - a direct stage for an unconfigured property closes instead of leaving an empty modal
  ---
  duration_ms: 0.313989
  ...
# Subtest: a refused direct stage closes instead of landing on a card or a list
ok 2814 - a refused direct stage closes instead of landing on a card or a list
  ---
  duration_ms: 0.613211
  ...
# Subtest: Ctrl+Shift+B lands on the Depends on stage with the same intent as card b
ok 2815 - Ctrl+Shift+B lands on the Depends on stage with the same intent as card b
  ---
  duration_ms: 2.143594
  ...
# Subtest: Ctrl+Shift+B Back returns to the card without re-dispatching
ok 2816 - Ctrl+Shift+B Back returns to the card without re-dispatching
  ---
  duration_ms: 1.140889
  ...
# Subtest: Ctrl+Shift+B on a plain bullet notices and closes the card
ok 2817 - Ctrl+Shift+B on a plain bullet notices and closes the card
  ---
  duration_ms: 0.669559
  ...
# Subtest: Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch
ok 2818 - Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch
  ---
  duration_ms: 2.7332
  ...
# Subtest: Ctrl+Shift+Alt+B on Depends-On and BLOCKS lines opens the owner's stage directly
ok 2819 - Ctrl+Shift+Alt+B on Depends-On and BLOCKS lines opens the owner's stage directly
  ---
  duration_ms: 1.96829
  ...
# Subtest: Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not
ok 2820 - Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not
  ---
  duration_ms: 2.013175
  ...
# Subtest: priority gesture writes the frozen date and duplicate dispatch is single-flight
ok 2821 - priority gesture writes the frozen date and duplicate dispatch is single-flight
  ---
  duration_ms: 9.953628
  ...
# Subtest: pending priority action passes its card preview through the Work Log adapter
ok 2822 - pending priority action passes its card preview through the Work Log adapter
  ---
  duration_ms: 1.593574
  ...
# Subtest: Task Link priority action refuses a stale cross-note preflight before writes
ok 2823 - Task Link priority action refuses a stale cross-note preflight before writes
  ---
  duration_ms: 5.090563
  ...
# Subtest: Task Link priority action rolls back earlier note writes after a later write fails
ok 2824 - Task Link priority action rolls back earlier note writes after a later write fails
  ---
  duration_ms: 2.111994
  ...
# Subtest: Task Link transaction reports a cleanup failure without implying global undo
ok 2825 - Task Link transaction reports a cleanup failure without implying global undo
  ---
  duration_ms: 1.081526
  ...
# Subtest: selected-property deletion uses the existing writer; other card rows stay non-deletable
ok 2826 - selected-property deletion uses the existing writer; other card rows stay non-deletable
  ---
  duration_ms: 2.451703
  ...
# Subtest: failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
ok 2827 - failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
  ---
  duration_ms: 1.489465
  ...
# Subtest: a refused deletion rebuilds the card from the refreshed line
ok 2828 - a refused deletion rebuilds the card from the refreshed line
  ---
  duration_ms: 1.885562
  ...
# Subtest: 0 deletes only priority and keeps the scheduled field byte-for-byte
ok 2829 - 0 deletes only priority and keeps the scheduled field byte-for-byte
  ---
  duration_ms: 4.763278
  ...
# Subtest: card keys pressed on a priority radio or the banner reach the resolver exactly once
ok 2830 - card keys pressed on a priority radio or the banner reach the resolver exactly once
  ---
  duration_ms: 2.833532
  ...
# Subtest: held or composing Enter on a radio or the banner never writes
ok 2831 - held or composing Enter on a radio or the banner never writes
  ---
  duration_ms: 1.094801
  ...
# Subtest: Escape, q, Q, and Ctrl+[ close the card without writing
ok 2832 - Escape, q, Q, and Ctrl+[ close the card without writing
  ---
  duration_ms: 3.124076
  ...
# Subtest: Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
ok 2833 - Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
  ---
  duration_ms: 0.620545
  ...
# Subtest: repeated close keys and a second close() are harmless
ok 2834 - repeated close keys and a second close() are harmless
  ---
  duration_ms: 1.093599
  ...
# Subtest: composition never closes the card or a stage
ok 2835 - composition never closes the card or a stage
  ---
  duration_ms: 0.844412
  ...
# Subtest: q typed into a stage's text field never closes the modal
ok 2836 - q typed into a stage's text field never closes the modal
  ---
  duration_ms: 0.873448
  ...
# Subtest: Ctrl+[ closes from a focused date field without writing
ok 2837 - Ctrl+[ closes from a focused date field without writing
  ---
  duration_ms: 0.878597
  ...
# Subtest: Ctrl+[ closes the schedule review from its Reason and Work summary fields
ok 2838 - Ctrl+[ closes the schedule review from its Reason and Work summary fields
  ---
  duration_ms: 4.697593
  ...
# Subtest: Ctrl+[ closes the summary-only schedule-work-log stage without writing
ok 2839 - Ctrl+[ closes the summary-only schedule-work-log stage without writing
  ---
  duration_ms: 1.035648
  ...
# Subtest: Ctrl+[ closes the lane-release Work summary without writing
ok 2840 - Ctrl+[ closes the lane-release Work summary without writing
  ---
  duration_ms: 0.993107
  ...
# Subtest: q closes from a focused More row and from the Close button
ok 2841 - q closes from a focused More row and from the Close button
  ---
  duration_ms: 1.839804
  ...
# Subtest: Ctrl+[ closes from focused card controls, the Back button, and the modal frame
ok 2842 - Ctrl+[ closes from focused card controls, the Back button, and the modal frame
  ---
  duration_ms: 2.624884
  ...
# Subtest: a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
ok 2843 - a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
  ---
  duration_ms: 10.794578
  ...
# Subtest: a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
ok 2844 - a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
  ---
  duration_ms: 2.577874
  ...
# Subtest: a direct dependency stage closes on Ctrl+[ but keeps q as typed text
ok 2845 - a direct dependency stage closes on Ctrl+[ but keeps q as typed text
  ---
  duration_ms: 0.577984
  ...
# Subtest: q and Ctrl+[ are not global closes: other modals and the decay card ignore them
ok 2846 - q and Ctrl+[ are not global closes: other modals and the decay card ignore them
  ---
  duration_ms: 0.824064
  ...
# Subtest: missing freshness API disables Review every with an honest reason
ok 2847 - missing freshness API disables Review every with an honest reason
  ---
  duration_ms: 0.681481
  ...
# Subtest: child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
ok 2848 - child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
  ---
  duration_ms: 0.888467
  ...
# Subtest: decay card keeps its classes and shares key-card tokens
ok 2849 - decay card keeps its classes and shares key-card tokens
  ---
  duration_ms: 0.163221
  ...
# Subtest: decay card footer always names the X drop alias; the trial date is not this gate
ok 2850 - decay card footer always names the X drop alias; the trial date is not this gate
  ---
  duration_ms: 0.299271
  ...
# Subtest: task card level chips reuse the shared priority mark when available
ok 2851 - task card level chips reuse the shared priority mark when available
  ---
  duration_ms: 1.121051
  ...
# Subtest: task card labels are unchanged without the priority mark api
ok 2852 - task card labels are unchanged without the priority mark api
  ---
  duration_ms: 9.021789
  ...
# Subtest: manifest order is authoritative and fragments share one lexical scope
ok 2853 - manifest order is authoritative and fragments share one lexical scope
  ---
  duration_ms: 103.595558
  ...
# Subtest: builds are deterministic and build:check is read-only on success
ok 2854 - builds are deterministic and build:check is read-only on success
  ---
  duration_ms: 185.018598
  ...
# Subtest: read-only check rejects changed fragments and edited generated output
ok 2855 - read-only check rejects changed fragments and edited generated output
  ---
  duration_ms: 157.958626
  ...
# Subtest: check rejects a missing generated bundle without writing it
ok 2856 - check rejects a missing generated bundle without writing it
  ---
  duration_ms: 52.248963
  ...
# Subtest: fragment line limit is enforced before writing output
ok 2857 - fragment line limit is enforced before writing output
  ---
  duration_ms: 1.304161
  ...
# Subtest: fragment syntax errors are rejected before writing output
ok 2858 - fragment syntax errors are rejected before writing output
  ---
  duration_ms: 29.987453
  ...
# Subtest: malformed, empty, duplicate, and traversal manifests are rejected read-only
    # Subtest: invalid JSON
    ok 1 - invalid JSON
      ---
      duration_ms: 0.714455
      ...
    # Subtest: empty manifest
    ok 2 - empty manifest
      ---
      duration_ms: 0.592181
      ...
    # Subtest: non-array manifest
    ok 3 - non-array manifest
      ---
      duration_ms: 0.634011
      ...
    # Subtest: duplicate entries
    ok 4 - duplicate entries
      ---
      duration_ms: 26.909204
      ...
    # Subtest: traversal entry
    ok 5 - traversal entry
      ---
      duration_ms: 0.511807
      ...
    # Subtest: absolute entry
    ok 6 - absolute entry
      ---
      duration_ms: 0.45014
      ...
    1..6
ok 2859 - malformed, empty, duplicate, and traversal manifests are rejected read-only
  ---
  duration_ms: 30.651902
  ...
# Subtest: missing and omitted fragments are rejected read-only
    # Subtest: missing manifest entry
    ok 1 - missing manifest entry
      ---
      duration_ms: 0.503131
      ...
    # Subtest: unlisted JavaScript source
    ok 2 - unlisted JavaScript source
      ---
      duration_ms: 24.22042
      ...
    1..2
ok 2860 - missing and omitted fragments are rejected read-only
  ---
  duration_ms: 24.954322
  ...
# Subtest: escaping fragment symlinks are rejected read-only
ok 2861 - escaping fragment symlinks are rejected read-only
  ---
  duration_ms: 0.962959
  ...
# Subtest: parity comparator identifies changed helper and plugin methods
ok 2862 - parity comparator identifies changed helper and plugin methods
  ---
  duration_ms: 8.506366
  ...
# Subtest: parity comparator accepts a mixin-split helper class but not a changed method or superclass
ok 2863 - parity comparator accepts a mixin-split helper class but not a changed method or superclass
  ---
  duration_ms: 0.444379
  ...
# Subtest: snapshot commands are available only for active Markdown files
ok 2864 - snapshot commands are available only for active Markdown files
  ---
  duration_ms: 1.68575
  ...
# Subtest: commands run bob ref create on the active path, with -C for closed tasks
ok 2865 - commands run bob ref create on the active path, with -C for closed tasks
  ---
  duration_ms: 7.548768
  ...
# Subtest: bob spawn uses the resolved path, vault environment, timeout, and NO_COLOR
ok 2866 - bob spawn uses the resolved path, vault environment, timeout, and NO_COLOR
  ---
  duration_ms: 1.318248
  ...
# Subtest: failure notices retain bob error and hint lines verbatim
ok 2867 - failure notices retain bob error and hint lines verbatim
  ---
  duration_ms: 0.56566
  ...
# Subtest: off desktop, bob spawning is refused with the desktop-app explanation
ok 2868 - off desktop, bob spawning is refused with the desktop-app explanation
  ---
  duration_ms: 0.512779
  ...
# Subtest: both prompt copies pass the shared fixture table identically
ok 2869 - both prompt copies pass the shared fixture table identically
  ---
  duration_ms: 6.824624
  ...
# Subtest: suggestion is valid, compact, and collision-aware
ok 2870 - suggestion is valid, compact, and collision-aware
  ---
  duration_ms: 0.724493
  ...
# Subtest: rename excludes exactly one old-ID occurrence
ok 2871 - rename excludes exactly one old-ID occurrence
  ---
  duration_ms: 0.227033
  ...
# Subtest: dependency legacy [id::] reuses only valid free IDs
ok 2872 - dependency legacy [id::] reuses only valid free IDs
  ---
  duration_ms: 0.3976
  ...
# Subtest: project conversion keeps the existing suggestBlockIdFromTask
ok 2873 - project conversion keeps the existing suggestBlockIdFromTask
  ---
  duration_ms: 0.969822
  ...
# Subtest: successor SB vectors are unchanged
ok 2874 - successor SB vectors are unchanged
  ---
  duration_ms: 1.044334
  ...
# Subtest: option-bracket ring reads Blocked as a source-only slot ahead of Ready
ok 2875 - option-bracket ring reads Blocked as a source-only slot ahead of Ready
  ---
  duration_ms: 1.169935
  ...
# Subtest: isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
ok 2876 - isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
  ---
  duration_ms: 0.331783
  ...
# Subtest: option-bracket refuses to change a member while its project is Blocked
ok 2877 - option-bracket refuses to change a member while its project is Blocked
  ---
  duration_ms: 2.422928
  ...
# Subtest: tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
ok 2878 - tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
  ---
  duration_ms: 1.270327
  ...
# Subtest: project resident notice reads the inline ^prj date and ignores frontmatter scheduled
ok 2879 - project resident notice reads the inline ^prj date and ignores frontmatter scheduled
  ---
  duration_ms: 0.464487
  ...
# Subtest: findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
ok 2880 - findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
  ---
  duration_ms: 0.281357
  ...
# Subtest: field removal collapses only the exposed span and preserves the rest of the line
ok 2881 - field removal collapses only the exposed span and preserves the rest of the line
  ---
  duration_ms: 0.241511
  ...
# Subtest: vault-path retirement preserves CRLF and a missing final newline
ok 2882 - vault-path retirement preserves CRLF and a missing final newline
  ---
  duration_ms: 0.860153
  ...
# Subtest: Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
ok 2883 - Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
  ---
  duration_ms: 0.593994
  ...
# Subtest: Schedule Log discovery ignores a marker owned by a nested grandchild
ok 2884 - Schedule Log discovery ignores a marker owned by a nested grandchild
  ---
  duration_ms: 0.394804
  ...
# Subtest: Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
ok 2885 - Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
  ---
  duration_ms: 0.459357
  ...
# Subtest: a task with no Schedule Log gets its field retired without any insertion or new marker
ok 2886 - a task with no Schedule Log gets its field retired without any insertion or new marker
  ---
  duration_ms: 0.133044
  ...
# Subtest: Schedule Log entry uses the canonical arrow, dash, and lock bytes
ok 2887 - Schedule Log entry uses the canonical arrow, dash, and lock bytes
  ---
  duration_ms: 0.091645
  ...
# Subtest: retirement stays a no-op for shapes that are not proof of a blocking date
ok 2888 - retirement stays a no-op for shapes that are not proof of a blocking date
  ---
  duration_ms: 0.170396
  ...
# Subtest: cycling Blocked backward to Cancelled retires the date and logs, matching forward
ok 2889 - cycling Blocked backward to Cancelled retires the date and logs, matching forward
  ---
  duration_ms: 3.894267
  ...
# Subtest: single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
ok 2890 - single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
  ---
  duration_ms: 0.986684
  ...
# Subtest: counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
ok 2891 - counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
  ---
  duration_ms: 1.453095
  ...
# Subtest: counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
ok 2892 - counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
  ---
  duration_ms: 0.627829
  ...
# Subtest: transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
ok 2893 - transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
  ---
  duration_ms: 1.847048
  ...
# Subtest: pressing again after Blocked retirement performs an ordinary transition with no further changes
ok 2894 - pressing again after Blocked retirement performs an ordinary transition with no further changes
  ---
  duration_ms: 0.231583
  ...
# Subtest: Alt+] on a date-blocked ^prj recovers open residents in step
ok 2895 - Alt+] on a date-blocked ^prj recovers open residents in step
  ---
  duration_ms: 15.876956
  ...
# Subtest: Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
ok 2896 - Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
  ---
  duration_ms: 1.454338
  ...
# Subtest: planProjectResidentRecoveryEdits recovers when a cross-note id is not open
ok 2897 - planProjectResidentRecoveryEdits recovers when a cross-note id is not open
  ---
  duration_ms: 0.370347
  ...
# Subtest: Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
ok 2898 - Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
  ---
  duration_ms: 1.299341
  ...
# Subtest: Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
ok 2899 - Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
  ---
  duration_ms: 0.833402
  ...
# Subtest: Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
ok 2900 - Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
  ---
  duration_ms: 1.673206
  ...
# Subtest: cycling a transcluded ^prj recovers residents in the source note
ok 2901 - cycling a transcluded ^prj recovers residents in the source note
  ---
  duration_ms: 1.096564
  ...
# Subtest: cycler BK1–BK12 accept and empty
ok 2902 - cycler BK1–BK12 accept and empty
  ---
  duration_ms: 1.091184
  ...
# Subtest: cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded
ok 2903 - cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded
  ---
  duration_ms: 0.577553
  ...
# Subtest: cycler MC4 strike/restore skip BLOCKS lines
ok 2904 - cycler MC4 strike/restore skip BLOCKS lines
  ---
  duration_ms: 0.819626
  ...
# Subtest: cycler MC3 tree close skips BLOCKS embeds
ok 2905 - cycler MC3 tree close skips BLOCKS embeds
  ---
  duration_ms: 0.941187
  ...
# Subtest: cycler MC1/MC2 Pomodoro and successor scanners skip managed lines
ok 2906 - cycler MC1/MC2 Pomodoro and successor scanners skip managed lines
  ---
  duration_ms: 0.984069
  ...
# Subtest: cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS
ok 2907 - cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS
  ---
  duration_ms: 0.206965
  ...
# Subtest: range planner preserves every single-item mode without an effective count
ok 2908 - range planner preserves every single-item mode without an effective count
  ---
  duration_ms: 7.1471
  ...
# Subtest: item counts carry children, skip blank lines and loose continuations, and clamp
ok 2909 - item counts carry children, skip blank lines and loose continuations, and clamp
  ---
  duration_ms: 0.328568
  ...
# Subtest: range stops at headings, shallower lines, same-level paragraphs and fences
ok 2910 - range stops at headings, shallower lines, same-level paragraphs and fences
  ---
  duration_ms: 0.189532
  ...
# Subtest: siblings require the exact whitespace and blockquote prefix
ok 2911 - siblings require the exact whitespace and blockquote prefix
  ---
  duration_ms: 0.19882
  ...
# Subtest: counted demotion moves four complete blocks to one existing section
ok 2912 - counted demotion moves four complete blocks to one existing section
  ---
  duration_ms: 4.106614
  ...
# Subtest: counted demotion creates a typed section or one default Requirements section
ok 2913 - counted demotion creates a typed section or one default Requirements section
  ---
  duration_ms: 2.169324
  ...
# Subtest: bottom-up removal splices blank seams and maps destinations before the source
ok 2914 - bottom-up removal splices blank seams and maps destinations before the source
  ---
  duration_ms: 0.435722
  ...
# Subtest: counted promotion Enter appends tasks in order and removes an emptied source section
ok 2915 - counted promotion Enter appends tasks in order and removes an emptied source section
  ---
  duration_ms: 0.864842
  ...
# Subtest: counted promotion to existing or new non-Tasks destinations keeps all bullets plain
ok 2916 - counted promotion to existing or new non-Tasks destinations keeps all bullets plain
  ---
  duration_ms: 0.489204
  ...
# Subtest: same-source Tasks promotion rewrites all selected lines in place
ok 2917 - same-source Tasks promotion rewrites all selected lines in place
  ---
  duration_ms: 0.878428
  ...
# Subtest: counted demotion outside Tasks moves to the next section in one write
ok 2918 - counted demotion outside Tasks moves to the next section in one write
  ---
  duration_ms: 0.360839
  ...
# Subtest: in-place ranges write once without centering for nested, non-dash, and unrouted items
ok 2919 - in-place ranges write once without centering for nested, non-dash, and unrouted items
  ---
  duration_ms: 0.801932
  ...
# Subtest: mixed demotion ranges count unchanged siblings and only move top-level dash tasks
ok 2920 - mixed demotion ranges count unchanged siblings and only move top-level dash tasks
  ---
  duration_ms: 0.396627
  ...
# Subtest: mixed promotion preserves existing tasks and a nonempty source section
ok 2921 - mixed promotion preserves existing tasks and a nonempty source section
  ---
  duration_ms: 0.218017
  ...
# Subtest: Vim action consumes explicit additional-item counts and preserves bare behavior
ok 2922 - Vim action consumes explicit additional-item counts and preserves bare behavior
  ---
  duration_ms: 2.421335
  ...
# Subtest: command checking preserves pending count; execution consumes it once and resets Vim
ok 2923 - command checking preserves pending count; execution consumes it once and resets Vim
  ---
  duration_ms: 0.993628
  ...
# Subtest: command route stays single without normal-mode explicit count and supports in-place ranges
ok 2924 - command route stays single without normal-mode explicit count and supports in-place ranges
  ---
  duration_ms: 0.376559
  ...
# Subtest: picker displays at most five preview rows plus overflow; single picker is unchanged
ok 2925 - picker displays at most five preview rows plus overflow; single picker is unchanged
  ---
  duration_ms: 1.234638
  ...
# Subtest: stale counted picker and cancelled picker never write
ok 2926 - stale counted picker and cancelled picker never write
  ---
  duration_ms: 0.912723
  ...
# Subtest: counted moves round-trip CRLF and preserve the presence or absence of a final newline
ok 2927 - counted moves round-trip CRLF and preserve the presence or absence of a final newline
  ---
  duration_ms: 3.646715
  ...
# Subtest: direct open/done transitions include incomplete statuses without broadening excluded statuses
ok 2928 - direct open/done transitions include incomplete statuses without broadening excluded statuses
  ---
  duration_ms: 1.289022
  ...
# Subtest: Ctrl+Enter block-link selection recognizes live and retired forms
ok 2929 - Ctrl+Enter block-link selection recognizes live and retired forms
  ---
  duration_ms: 2.09408
  ...
# Subtest: Pomodoro child ownership is status-neutral and bounded by contiguous list structure
ok 2930 - Pomodoro child ownership is status-neutral and bounded by contiguous list structure
  ---
  duration_ms: 0.78517
  ...
# Subtest: daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
ok 2931 - daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
  ---
  duration_ms: 0.295134
  ...
# Subtest: parsePomodoroEntryLineParts reads placeholder and range names conservatively
ok 2932 - parsePomodoroEntryLineParts reads placeholder and range names conservatively
  ---
  duration_ms: 0.831849
  ...
# Subtest: formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
ok 2933 - formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
  ---
  duration_ms: 0.155707
  ...
# Subtest: Pomodoro bullet toggle accepts empty indented list items
ok 2934 - Pomodoro bullet toggle accepts empty indented list items
  ---
  duration_ms: 0.289703
  ...
# Subtest: Pomodoro bullet toggle rejects non-empty or out-of-section bullets
ok 2935 - Pomodoro bullet toggle rejects non-empty or out-of-section bullets
  ---
  duration_ms: 0.20458
  ...
# Subtest: Pomodoro bullet toggle reverses only empty open childless placeholders
ok 2936 - Pomodoro bullet toggle reverses only empty open childless placeholders
  ---
  duration_ms: 0.500937
  ...
# Subtest: Pomodoro bullet toggle reverses named empty open childless placeholders
ok 2937 - Pomodoro bullet toggle reverses named empty open childless placeholders
  ---
  duration_ms: 0.380306
  ...
# Subtest: Pomodoro bullet toggle round trips and normalizes child indentation
ok 2938 - Pomodoro bullet toggle round trips and normalizes child indentation
  ---
  duration_ms: 0.213668
  ...
# Subtest: Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
ok 2939 - Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
  ---
  duration_ms: 0.145949
  ...
# Subtest: Pomodoro toggle key gate does not shadow bare Option bracket cycling
ok 2940 - Pomodoro toggle key gate does not shadow bare Option bracket cycling
  ---
  duration_ms: 0.173421
  ...
# Subtest: Pomodoro toggle command is daily-only and places the cursor for both directions
ok 2941 - Pomodoro toggle command is daily-only and places the cursor for both directions
  ---
  duration_ms: 0.525143
  ...
# Subtest: Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
ok 2942 - Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
  ---
  duration_ms: 0.310293
  ...
# Subtest: Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
ok 2943 - Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
  ---
  duration_ms: 1.880201
  ...
# Subtest: Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
ok 2944 - Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
  ---
  duration_ms: 23.83427
  ...
# Subtest: Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
ok 2945 - Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
  ---
  duration_ms: 1.793807
  ...
# Subtest: Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
ok 2946 - Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
  ---
  duration_ms: 1.941127
  ...
# Subtest: Ctrl+Enter closing the local line over an already-closed target does not write it a second time
ok 2947 - Ctrl+Enter closing the local line over an already-closed target does not write it a second time
  ---
  duration_ms: 0.783196
  ...
# Subtest: Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
ok 2948 - Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
  ---
  duration_ms: 0.662806
  ...
# Subtest: Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
ok 2949 - Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
  ---
  duration_ms: 1.649791
  ...
# Subtest: Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
ok 2950 - Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
  ---
  duration_ms: 0.550431
  ...
# Subtest: Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
ok 2951 - Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
  ---
  duration_ms: 0.604775
  ...
# Subtest: Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
ok 2952 - Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
  ---
  duration_ms: 0.800278
  ...
# Subtest: Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
ok 2953 - Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
  ---
  duration_ms: 0.609995
  ...
# Subtest: getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
ok 2954 - getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
  ---
  duration_ms: 0.286848
  ...
# Subtest: Ctrl+Enter close continues the walk with complete after finalize ran
ok 2955 - Ctrl+Enter close continues the walk with complete after finalize ran
  ---
  duration_ms: 11.745274
  ...
# Subtest: Ctrl+Enter close continues only after transclusion propagation landed
ok 2956 - Ctrl+Enter close continues only after transclusion propagation landed
  ---
  duration_ms: 12.458023
  ...
# Subtest: Ctrl+Enter reopen settles the walk with null
ok 2957 - Ctrl+Enter reopen settles the walk with null
  ---
  duration_ms: 11.410293
  ...
# Subtest: Ctrl+Enter swallows the key with no write while the walk is busy
ok 2958 - Ctrl+Enter swallows the key with no write while the walk is busy
  ---
  duration_ms: 11.026408
  ...
# Subtest: Ctrl+Enter with a null capture behaves exactly like today
ok 2959 - Ctrl+Enter with a null capture behaves exactly like today
  ---
  duration_ms: 11.65442
  ...
# Subtest: Ctrl+Enter with nav v2 or no nav keeps today's behavior
ok 2960 - Ctrl+Enter with nav v2 or no nav keeps today's behavior
  ---
  duration_ms: 22.157938
  ...
# Subtest: Ctrl+Enter lets the checklist claim win before capturing
ok 2961 - Ctrl+Enter lets the checklist claim win before capturing
  ---
  duration_ms: 0.928774
  ...
# Subtest: Ctrl+Enter settles the walk with null when the toggle rejects
ok 2962 - Ctrl+Enter settles the walk with null when the toggle rejects
  ---
  duration_ms: 12.67017
  ...
# Subtest: Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
ok 2963 - Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
  ---
  duration_ms: 1.971105
  ...
# Subtest: eligible Tasks demotions prompt in project and non-project notes
ok 2964 - eligible Tasks demotions prompt in project and non-project notes
  ---
  duration_ms: 3.337255
  ...
# Subtest: selectable headings skip YAML, fences, empty titles, and Tasks
ok 2965 - selectable headings skip YAML, fences, empty titles, and Tasks
  ---
  duration_ms: 1.163473
  ...
# Subtest: duplicate heading identities stay distinct and route to the chosen occurrence
ok 2966 - duplicate heading identities stay distinct and route to the chosen occurrence
  ---
  duration_ms: 1.31936
  ...
# Subtest: demotion picker defaults and typed names resolve without synthetic duplicates
ok 2967 - demotion picker defaults and typed names resolve without synthetic duplicates
  ---
  duration_ms: 2.252913
  ...
# Subtest: picker keyboard state wraps, clamps, and refuses invalid Enter
ok 2968 - picker keyboard state wraps, clamps, and refuses invalid Enter
  ---
  duration_ms: 0.401968
  ...
# Subtest: new-section formatting keeps extra blanks, final newlines, and nested children
ok 2969 - new-section formatting keeps extra blanks, final newlines, and nested children
  ---
  duration_ms: 0.908505
  ...
# Subtest: existing-section insertion works before and after the source on CRLF-backed editors
ok 2970 - existing-section insertion works before and after the source on CRLF-backed editors
  ---
  duration_ms: 3.414772
  ...
# Subtest: command opens one picker, writes only on accept, and restores cursor plus center
ok 2971 - command opens one picker, writes only on accept, and restores cursor plus center
  ---
  duration_ms: 1.227254
  ...
# Subtest: pointer activation, Escape, and double-submit protection leave a consistent note
ok 2972 - pointer activation, Escape, and double-submit protection leave a consistent note
  ---
  duration_ms: 1.469557
  ...
# Subtest: stale document, changed editor, or missing heading notice without writing
ok 2973 - stale document, changed editor, or missing heading notice without writing
  ---
  duration_ms: 2.897944
  ...
# Subtest: dependency normalizer writes path-qualified IDs and is idempotent
ok 2974 - dependency normalizer writes path-qualified IDs and is idempotent
  ---
  duration_ms: 2.231763
  ...
# Subtest: Tasks-generated IDs become local block IDs when none exists
ok 2975 - Tasks-generated IDs become local block IDs when none exists
  ---
  duration_ms: 0.794608
  ...
# Subtest: note rename rewrites target IDs and yields exact propagation mappings
ok 2976 - note rename rewrites target IDs and yields exact propagation mappings
  ---
  duration_ms: 0.291707
  ...
# Subtest: note rename also rewrites same-file dependsOn references
ok 2977 - note rename also rewrites same-file dependsOn references
  ---
  duration_ms: 0.234708
  ...
# Subtest: dependency normalization skips unsupported paths and fenced examples
ok 2978 - dependency normalization skips unsupported paths and fenced examples
  ---
  duration_ms: 0.339078
  ...
# Subtest: blocked-dependent planner matches the CLI dependency truth table
ok 2979 - blocked-dependent planner matches the CLI dependency truth table
  ---
  duration_ms: 2.491509
  ...
# Subtest: blocked-dependent edits preserve EOLs and skip stale lines idempotently
ok 2980 - blocked-dependent edits preserve EOLs and skip stale lines idempotently
  ---
  duration_ms: 0.836298
  ...
# Subtest: project recovery strips resident tags and works without freshness v12
ok 2981 - project recovery strips resident tags and works without freshness v12
  ---
  duration_ms: 1.467784
  ...
# Subtest: recovery passes daily-note and Today skip flags to ledger freshness
ok 2982 - recovery passes daily-note and Today skip flags to ledger freshness
  ---
  duration_ms: 0.425132
  ...
# Subtest: normalization mappings propagate to every dependent file
ok 2983 - normalization mappings propagate to every dependent file
  ---
  duration_ms: 1.133976
  ...
# Subtest: runtime normalizer skips unsupported paths with one informative notice
ok 2984 - runtime normalizer skips unsupported paths with one informative notice
  ---
  duration_ms: 0.715647
  ...
# Subtest: rename reconciliation rewrites the target and every dependent
ok 2985 - rename reconciliation rewrites the target and every dependent
  ---
  duration_ms: 0.567965
  ...
# Subtest: editor dependency normalization abandons and reschedules stale snapshots
ok 2986 - editor dependency normalization abandons and reschedules stale snapshots
  ---
  duration_ms: 0.522428
  ...
# Subtest: rename reconciliation abandons and reschedules stale editor snapshots
ok 2987 - rename reconciliation abandons and reschedules stale editor snapshots
  ---
  duration_ms: 0.264545
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 2988 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.815007
  ...
# Subtest: close-time retirement skips Depends-On lines
ok 2989 - close-time retirement skips Depends-On lines
  ---
  duration_ms: 1.195062
  ...
# Subtest: reopen restoration skips Depends-On lines instead of re-embedding them
ok 2990 - reopen restoration skips Depends-On lines instead of re-embedding them
  ---
  duration_ms: 0.564158
  ...
# Subtest: embedded-tree close collection ignores Depends-On lines
ok 2991 - embedded-tree close collection ignores Depends-On lines
  ---
  duration_ms: 0.292498
  ...
# Subtest: Alt-bracket bullet formatting never applies to Depends-On lines
ok 2992 - Alt-bracket bullet formatting never applies to Depends-On lines
  ---
  duration_ms: 0.539961
  ...
# Subtest: Ctrl+Enter on a dependency link closes only the target and runs the recovery
ok 2993 - Ctrl+Enter on a dependency link closes only the target and runs the recovery
  ---
  duration_ms: 1.680669
  ...
# Subtest: Ctrl+Enter on a dependency link reopens only the target, root-only
ok 2994 - Ctrl+Enter on a dependency link reopens only the target, root-only
  ---
  duration_ms: 1.165556
  ...
# Subtest: single and counted Alt-bracket cycle the dependency target under the cursor
ok 2995 - single and counted Alt-bracket cycle the dependency target under the cursor
  ---
  duration_ms: 15.046339
  ...
# Subtest: single and counted Alt-bracket report when the cursor is off every dependency link
ok 2996 - single and counted Alt-bracket report when the cursor is off every dependency link
  ---
  duration_ms: 0.609494
  ...
# Subtest: Ctrl+Enter candidate resolution finds plain links on Depends-On lines
ok 2997 - Ctrl+Enter candidate resolution finds plain links on Depends-On lines
  ---
  duration_ms: 0.208659
  ...
# Subtest: dependency-id normalisation never edits Depends-On lines
ok 2998 - dependency-id normalisation never edits Depends-On lines
  ---
  duration_ms: 0.32462
  ...
# Subtest: note rename rewrites fields while leaving Depends-On lines alone
ok 2999 - note rename rewrites fields while leaving Depends-On lines alone
  ---
  duration_ms: 0.190985
  ...
# Subtest: recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
ok 3000 - recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
  ---
  duration_ms: 2.373704
  ...
# Subtest: cycler freshness: local-fallback rewrite stamps last via injected stamper
ok 3001 - cycler freshness: local-fallback rewrite stamps last via injected stamper
  ---
  duration_ms: 1.687743
  ...
# Subtest: cycler freshness: rewrites without a stamper are unchanged (identity default)
ok 3002 - cycler freshness: rewrites without a stamper are unchanged (identity default)
  ---
  duration_ms: 0.438658
  ...
# Subtest: cycler freshness: a throwing stamper leaves the rewritten line intact
ok 3003 - cycler freshness: a throwing stamper leaves the rewritten line intact
  ---
  duration_ms: 0.156028
  ...
# Subtest: cycler freshness: transcluded rewrite stamps last via injected stamper
ok 3004 - cycler freshness: transcluded rewrite stamps last via injected stamper
  ---
  duration_ms: 0.18888
  ...
# Subtest: cycler freshness: cycling a plain line stamps through the follow-up edit
ok 3005 - cycler freshness: cycling a plain line stamps through the follow-up edit
  ---
  duration_ms: 0.842829
  ...
# Subtest: cycler freshness: Tasks-command rewrite with the expected status is stamped
ok 3006 - cycler freshness: Tasks-command rewrite with the expected status is stamped
  ---
  duration_ms: 0.359977
  ...
# Subtest: cycler freshness: Tasks command that inserts a line never stamps
ok 3007 - cycler freshness: Tasks command that inserts a line never stamps
  ---
  duration_ms: 0.343336
  ...
# Subtest: cycler freshness: Tasks command that deletes the line never stamps the next task
ok 3008 - cycler freshness: Tasks command that deletes the line never stamps the next task
  ---
  duration_ms: 0.197387
  ...
# Subtest: cycler freshness: Tasks command that leaves a different status never stamps
ok 3009 - cycler freshness: Tasks command that leaves a different status never stamps
  ---
  duration_ms: 0.388372
  ...
# Subtest: cycler freshness: cycling without ledger-tools writes no stamp
ok 3010 - cycler freshness: cycling without ledger-tools writes no stamp
  ---
  duration_ms: 0.454067
  ...
# Subtest: cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
ok 3011 - cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
  ---
  duration_ms: 0.204661
  ...
# Subtest: Pomodoro marker helpers normalize every block link and preserve fences and EOLs
ok 3012 - Pomodoro marker helpers normalize every block link and preserve fences and EOLs
  ---
  duration_ms: 2.695978
  ...
# Subtest: completed Pomodoro markers are normalized per occurrence
ok 3013 - completed Pomodoro markers are normalized per occurrence
  ---
  duration_ms: 0.489104
  ...
# Subtest: move-only Pomodoro links require a strict immediate hash directive
ok 3014 - move-only Pomodoro links require a strict immediate hash directive
  ---
  duration_ms: 2.687643
  ...
# Subtest: Pomodoro move-only planner toggles links across additional physical lines
ok 3015 - Pomodoro move-only planner toggles links across additional physical lines
  ---
  duration_ms: 1.194681
  ...
# Subtest: Pomodoro move-only planner round trips exact text and rejects strict non-matches
ok 3016 - Pomodoro move-only planner round trips exact text and rejects strict non-matches
  ---
  duration_ms: 0.499093
  ...
# Subtest: bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
ok 3017 - bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
  ---
  duration_ms: 1.463855
  ...
# Subtest: Pomodoro move-only runtime removes locally and validates additions independently
ok 3018 - Pomodoro move-only runtime removes locally and validates additions independently
  ---
  duration_ms: 0.919596
  ...
# Subtest: Pomodoro move-only runtime protects live lines after asynchronous failures
ok 3019 - Pomodoro move-only runtime protects live lines after asynchronous failures
  ---
  duration_ms: 0.377621
  ...
# Subtest: Pomodoro hash Vim mapping distinguishes bare and explicit repeats
ok 3020 - Pomodoro hash Vim mapping distinguishes bare and explicit repeats
  ---
  duration_ms: 8.427667
  ...
# Subtest: Pomodoro completion marks originals and carries clean live copies
ok 3021 - Pomodoro completion marks originals and carries clean live copies
  ---
  duration_ms: 1.759069
  ...
# Subtest: Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
ok 3022 - Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
  ---
  duration_ms: 0.838952
  ...
# Subtest: Pomodoro completion carries the closed Pomodoro name onto created entries
ok 3023 - Pomodoro completion carries the closed Pomodoro name onto created entries
  ---
  duration_ms: 0.413931
  ...
# Subtest: buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
ok 3024 - buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
  ---
  duration_ms: 0.400304
  ...
# Subtest: buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
ok 3025 - buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
  ---
  duration_ms: 0.268613
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is marked
ok 3026 - buildPomodoroCompletionPlan keeps source order when every carried link is marked
  ---
  duration_ms: 0.200673
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
ok 3027 - buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
  ---
  duration_ms: 0.219028
  ...
# Subtest: Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
ok 3028 - Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
  ---
  duration_ms: 4.799708
  ...
# Subtest: deferred-only close deletes the emptied entry and carries stripped links
ok 3029 - deferred-only close deletes the emptied entry and carries stripped links
  ---
  duration_ms: 0.384906
  ...
# Subtest: deferred-only close at EOF leaves no dangling newline
ok 3030 - deferred-only close at EOF leaves no dangling newline
  ---
  duration_ms: 0.208748
  ...
# Subtest: a close with a remaining copyable link keeps the [x] entry
ok 3031 - a close with a remaining copyable link keeps the [x] entry
  ---
  duration_ms: 0.252191
  ...
# Subtest: a prose sibling keeps the closed entry on a deferred close
ok 3032 - a prose sibling keeps the closed entry on a deferred close
  ---
  duration_ms: 0.283402
  ...
# Subtest: Ctrl+Enter deferred-only close deletes the entry in one gesture
ok 3033 - Ctrl+Enter deferred-only close deletes the entry in one gesture
  ---
  duration_ms: 3.100752
  ...
# Subtest: deferred-only close keeps a separated prose child and deletes fence-only leftovers whole
ok 3034 - deferred-only close keeps a separated prose child and deletes fence-only leftovers whole
  ---
  duration_ms: 0.741946
  ...
# Subtest: deferred-only successor relocation uses the inserted placeholder
ok 3035 - deferred-only successor relocation uses the inserted placeholder
  ---
  duration_ms: 0.259616
  ...
# Subtest: selected Done Pomodoro transclusion reopens only its cross-file root
ok 3036 - selected Done Pomodoro transclusion reopens only its cross-file root
  ---
  duration_ms: 6.65474
  ...
# Subtest: selected same-file Done target reopens root-only in the live editor
ok 3037 - selected same-file Done target reopens root-only in the live editor
  ---
  duration_ms: 1.588974
  ...
# Subtest: selected retired link reopens its root and restores the historical occurrence
ok 3038 - selected retired link reopens its root and restores the historical occurrence
  ---
  duration_ms: 1.456511
  ...
# Subtest: incomplete selected Pomodoro transclusion still closes recursively
ok 3039 - incomplete selected Pomodoro transclusion still closes recursively
  ---
  duration_ms: 2.404672
  ...
# Subtest: Done Pomodoro reopens direct roots and clears only its block-link markers
ok 3040 - Done Pomodoro reopens direct roots and clears only its block-link markers
  ---
  duration_ms: 3.907142
  ...
# Subtest: Done Pomodoro reopen restores its own block reference after reopening direct roots
ok 3041 - Done Pomodoro reopen restores its own block reference after reopening direct roots
  ---
  duration_ms: 1.025027
  ...
# Subtest: Done Pomodoro markers remain when the Todo transition does not occur
ok 3042 - Done Pomodoro markers remain when the Todo transition does not occur
  ---
  duration_ms: 0.327786
  ...
# Subtest: registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
ok 3043 - registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
  ---
  duration_ms: 13.785741
  ...
# Subtest: registered Ctrl+Enter immediately recovers a same-file dependent
ok 3044 - registered Ctrl+Enter immediately recovers a same-file dependent
  ---
  duration_ms: 11.011562
  ...
# Subtest: registered Ctrl+Enter immediately recovers a cross-file dependent
ok 3045 - registered Ctrl+Enter immediately recovers a cross-file dependent
  ---
  duration_ms: 3.057549
  ...
# Subtest: child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
ok 3046 - child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
  ---
  duration_ms: 4.515613
  ...
# Subtest: Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
ok 3047 - Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
  ---
  duration_ms: 1.500095
  ...
# Subtest: selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
ok 3048 - selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
  ---
  duration_ms: 2.756445
  ...
# Subtest: selected unresolved or excluded embedded children are consumed as no-ops
ok 3049 - selected unresolved or excluded embedded children are consumed as no-ops
  ---
  duration_ms: 1.2356
  ...
# Subtest: Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
ok 3050 - Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
  ---
  duration_ms: 3.404823
  ...
# Subtest: Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
ok 3051 - Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
  ---
  duration_ms: 2.269875
  ...
# Subtest: Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
ok 3052 - Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
  ---
  duration_ms: 0.908886
  ...
# Subtest: Pomodoro Work Log note-group collection scopes to direct children and requires descendants
ok 3053 - Pomodoro Work Log note-group collection scopes to direct children and requires descendants
  ---
  duration_ms: 0.799588
  ...
# Subtest: Work Log entry body formats as *date* — summary
ok 3054 - Work Log entry body formats as *date* — summary
  ---
  duration_ms: 0.126882
  ...
# Subtest: buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
ok 3055 - buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
  ---
  duration_ms: 0.225251
  ...
# Subtest: planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
ok 3056 - planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
  ---
  duration_ms: 0.335551
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
ok 3057 - planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
  ---
  duration_ms: 0.291266
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
ok 3058 - planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
  ---
  duration_ms: 0.186917
  ...
# Subtest: planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
ok 3059 - planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
  ---
  duration_ms: 0.362563
  ...
# Subtest: planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
ok 3060 - planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
  ---
  duration_ms: 0.380186
  ...
# Subtest: full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
ok 3061 - full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
  ---
  duration_ms: 6.242333
  ...
# Subtest: full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
ok 3062 - full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
  ---
  duration_ms: 1.494705
  ...
# Subtest: full Pomodoro completion keeps two same-task Work Log note sets in source order
ok 3063 - full Pomodoro completion keeps two same-task Work Log note sets in source order
  ---
  duration_ms: 1.141691
  ...
# Subtest: full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
ok 3064 - full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
  ---
  duration_ms: 0.831609
  ...
# Subtest: full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
ok 3065 - full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
  ---
  duration_ms: 0.83743
  ...
# Subtest: full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
ok 3066 - full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
  ---
  duration_ms: 0.546444
  ...
# Subtest: PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
ok 3067 - PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
  ---
  duration_ms: 1.435091
  ...
# Subtest: PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
ok 3068 - PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
  ---
  duration_ms: 0.846988
  ...
# Subtest: PP1 links the emptied project's ^prj as Next and strips \#hide
ok 3069 - PP1 links the emptied project's ^prj as Next and strips \#hide
  ---
  duration_ms: 9.182486
  ...
# Subtest: PP29 closing a child ^prj pulls in its empty parent project
ok 3070 - PP29 closing a child ^prj pulls in its empty parent project
  ---
  duration_ms: 2.390985
  ...
# Subtest: PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
ok 3071 - PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
  ---
  duration_ms: 1.092827
  ...
# Subtest: PP30 keeps the parent untouched while another child or task remains
ok 3072 - PP30 keeps the parent untouched while another child or task remains
  ---
  duration_ms: 0.906702
  ...
# Subtest: PP31 skips missing, ambiguous, and non-project parents
ok 3073 - PP31 skips missing, ambiguous, and non-project parents
  ---
  duration_ms: 1.16777
  ...
# Subtest: PP33 cancellation surfaces the parent without linking it
ok 3074 - PP33 cancellation surfaces the parent without linking it
  ---
  duration_ms: 2.335481
  ...
# Subtest: PP2 and PP3 leave a project with remaining work alone
ok 3075 - PP2 and PP3 leave a project with remaining work alone
  ---
  duration_ms: 1.442255
  ...
# Subtest: PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
ok 3076 - PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
  ---
  duration_ms: 2.480448
  ...
# Subtest: PP6 Sub-projects marker states match display_for_wikilink
ok 3077 - PP6 Sub-projects marker states match display_for_wikilink
  ---
  duration_ms: 1.231682
  ...
# Subtest: PP7 and PP28 keep a future-scheduled ^prj byte-identical
ok 3078 - PP7 and PP28 keep a future-scheduled ^prj byte-identical
  ---
  duration_ms: 1.055997
  ...
# Subtest: PP8 still-blocks a ^prj that waits on another open prerequisite
ok 3079 - PP8 still-blocks a ^prj that waits on another open prerequisite
  ---
  duration_ms: 0.611628
  ...
# Subtest: PP9 already-planned ^prj raises to Next without a new link
ok 3080 - PP9 already-planned ^prj raises to Next without a new link
  ---
  duration_ms: 0.566512
  ...
# Subtest: PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
ok 3081 - PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
  ---
  duration_ms: 1.890822
  ...
# Subtest: PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
ok 3082 - PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
  ---
  duration_ms: 0.701109
  ...
# Subtest: PP14 an id-less last task still pulls in
ok 3083 - PP14 an id-less last task still pulls in
  ---
  duration_ms: 0.422517
  ...
# Subtest: PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
ok 3084 - PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
  ---
  duration_ms: 9.757206
  ...
# Subtest: PP17 one pull-in row wins over project_task
ok 3085 - PP17 one pull-in row wins over project_task
  ---
  duration_ms: 0.608362
  ...
# Subtest: PP18 cancel recovers only
ok 3086 - PP18 cancel recovers only
  ---
  duration_ms: 0.420332
  ...
# Subtest: PP20 unrecognised or unplannable notes never pull in
ok 3087 - PP20 unrecognised or unplannable notes never pull in
  ---
  duration_ms: 1.04739
  ...
# Subtest: PP24 closing an external prerequisite pulls in only when N is empty
ok 3088 - PP24 closing an external prerequisite pulls in only when N is empty
  ---
  duration_ms: 0.794818
  ...
# Subtest: PP25 cascades project_member recovery after a [?] pull-in
ok 3089 - PP25 cascades project_member recovery after a [?] pull-in
  ---
  duration_ms: 0.978048
  ...
# Subtest: PP26 dated recount treats a hidden leftover as remaining work
ok 3090 - PP26 dated recount treats a hidden leftover as remaining work
  ---
  duration_ms: 0.590908
  ...
# Subtest: PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
ok 3091 - PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
  ---
  duration_ms: 1.831818
  ...
# Subtest: successorNoticeText uses the §12.6 pull-in and surfaced copy
ok 3092 - successorNoticeText uses the §12.6 pull-in and surfaced copy
  ---
  duration_ms: 0.472352
  ...
# Subtest: Ctrl+Enter on the last task link inserts the ^prj and rewrites R
ok 3093 - Ctrl+Enter on the last task link inserts the ^prj and rewrites R
  ---
  duration_ms: 9.746215
  ...
# Subtest: PP29 runtime close and reopen use the parent pull-in receipt
ok 3094 - PP29 runtime close and reopen use the parent pull-in receipt
  ---
  duration_ms: 4.668306
  ...
# Subtest: PP18 Alt+[ cancel of the last task surfaces R without linking
ok 3095 - PP18 Alt+[ cancel of the last task surfaces R without linking
  ---
  duration_ms: 15.363595
  ...
# Subtest: PP19 same-day reopen restores R byte-for-byte and takes back the link
ok 3096 - PP19 same-day reopen restores R byte-for-byte and takes back the link
  ---
  duration_ms: 2.769799
  ...
# Subtest: a close in a project that still has work stays inside the gate
ok 3097 - a close in a project that still has work stays inside the gate
  ---
  duration_ms: 0.977978
  ...
# Subtest: P1 path-qualified skip keys: same ^review in another note does not suppress
ok 3098 - P1 path-qualified skip keys: same ^review in another note does not suppress
  ---
  duration_ms: 0.595236
  ...
# Subtest: P3 id-less cascade: stale [?] R recovers resident without [id::]
ok 3099 - P3 id-less cascade: stale [?] R recovers resident without [id::]
  ---
  duration_ms: 1.77541
  ...
# Subtest: P4 frontmatter scheduled validity mirrors Rust
ok 3100 - P4 frontmatter scheduled validity mirrors Rust
  ---
  duration_ms: 0.564208
  ...
# Subtest: P5 recognition mirrors Rust (status/type/prj line)
ok 3101 - P5 recognition mirrors Rust (status/type/prj line)
  ---
  duration_ms: 1.234909
  ...
# Subtest: P6 SUBOPEN blank line stops the marker scan (PP6)
ok 3102 - P6 SUBOPEN blank line stops the marker scan (PP6)
  ---
  duration_ms: 0.461411
  ...
# Subtest: promotion prompts default to Tasks in ordinary and project notes
ok 3103 - promotion prompts default to Tasks in ordinary and project notes
  ---
  duration_ms: 4.137703
  ...
# Subtest: promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
ok 3104 - promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
  ---
  duration_ms: 1.033514
  ...
# Subtest: promotion command writes only on accept and Enter selects Tasks
ok 3105 - promotion command writes only on accept and Enter selects Tasks
  ---
  duration_ms: 2.919886
  ...
# Subtest: promotion removes only genuinely empty source sections
ok 3106 - promotion removes only genuinely empty source sections
  ---
  duration_ms: 1.200102
  ...
# Subtest: promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
ok 3107 - promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
  ---
  duration_ms: 1.103707
  ...
# Subtest: Tasks-only preamble promotions prompt and blank Enter moves into Tasks
ok 3108 - Tasks-only preamble promotions prompt and blank Enter moves into Tasks
  ---
  duration_ms: 0.812672
  ...
# Subtest: plain bullets already in Tasks prompt and blank Enter promotes in place
ok 3109 - plain bullets already in Tasks prompt and blank Enter promotes in place
  ---
  duration_ms: 1.051688
  ...
# Subtest: promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
ok 3110 - promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
  ---
  duration_ms: 0.498572
  ...
# Subtest: always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
ok 3111 - always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
  ---
  duration_ms: 4.201956
  ...
# Could not restore all reopened task references [ 'Broken.md: unreadable' ]
# Could not recover all blocked dependents [
#   'BrokenRead.md: read failed',
#   'Stale.md: line 1 changed before recovery',
#   'BrokenWrite.md: write failed'
# ]
# Subtest: direct Done Tasks task reopens through the metadata-aware fallback
ok 3112 - direct Done Tasks task reopens through the metadata-aware fallback
  ---
  duration_ms: 1.93714
  ...
# Subtest: recursive completion status policy includes Next without broadening excluded statuses
ok 3113 - recursive completion status policy includes Next without broadening excluded statuses
  ---
  duration_ms: 0.2461
  ...
# Subtest: recursive completion closes a Next root and its nested Next descendant
ok 3114 - recursive completion closes a Next root and its nested Next descendant
  ---
  duration_ms: 3.453294
  ...
# Subtest: recursive completion traverses Done parents and skips excluded siblings
ok 3115 - recursive completion traverses Done parents and skips excluded siblings
  ---
  duration_ms: 1.103137
  ...
# Subtest: closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
ok 3116 - closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
  ---
  duration_ms: 1.556822
  ...
# Subtest: reopened-reference restoration is ancestry-aware, conservative, and idempotent
ok 3117 - reopened-reference restoration is ancestry-aware, conservative, and idempotent
  ---
  duration_ms: 1.654971
  ...
# Subtest: retirement preserves task-tree markers and unmarks Pomodoro embeds
ok 3118 - retirement preserves task-tree markers and unmarks Pomodoro embeds
  ---
  duration_ms: 0.404362
  ...
# Subtest: done Pomodoro retirement removes only the matching embedded marker
ok 3119 - done Pomodoro retirement removes only the matching embedded marker
  ---
  duration_ms: 0.273502
  ...
# Subtest: retirement stops at prose boundaries and pairs strikethrough spans
ok 3120 - retirement stops at prose boundaries and pairs strikethrough spans
  ---
  duration_ms: 0.415213
  ...
# Subtest: retired Pomodoro links are not copied into the next Pomodoro
ok 3121 - retired Pomodoro links are not copied into the next Pomodoro
  ---
  duration_ms: 1.29279
  ...
# Subtest: retirement coordinator rewrites active editor and vault notes together
ok 3122 - retirement coordinator rewrites active editor and vault notes together
  ---
  duration_ms: 1.076627
  ...
# Subtest: restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
ok 3123 - restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
  ---
  duration_ms: 1.360669
  ...
# Subtest: close and reopen reference mutations share one serialized queue
ok 3124 - close and reopen reference mutations share one serialized queue
  ---
  duration_ms: 0.274504
  ...
# Subtest: post-close finalizer runs one gated plan before reference retirement
ok 3125 - post-close finalizer runs one gated plan before reference retirement
  ---
  duration_ms: 0.534872
  ...
# Subtest: dependent recovery uses live editor buffers and preserves the cursor
ok 3126 - dependent recovery uses live editor buffers and preserves the cursor
  ---
  duration_ms: 2.913325
  ...
# Subtest: dependent recovery preserves successful siblings across stale and failed notes
ok 3127 - dependent recovery preserves successful siblings across stale and failed notes
  ---
  duration_ms: 1.284954
  ...
# Subtest: no-op vault transforms and irrelevant retirement files avoid process writes
ok 3128 - no-op vault transforms and irrelevant retirement files avoid process writes
  ---
  duration_ms: 0.306044
  ...
# Subtest: ambiguity scans and notices are cached while dependency identity lines stay stable
ok 3129 - ambiguity scans and notices are cached while dependency identity lines stay stable
  ---
  duration_ms: 0.639932
  ...
# Subtest: non-Vim open/done command finalizes the closed task identity
ok 3130 - non-Vim open/done command finalizes the closed task identity
  ---
  duration_ms: 0.395255
  ...
# Subtest: non-Vim open/done command restores the reopened task identity
ok 3131 - non-Vim open/done command restores the reopened task identity
  ---
  duration_ms: 0.334459
  ...
# Subtest: full Pomodoro completion retires embeds only after carry-forward planning
ok 3132 - full Pomodoro completion retires embeds only after carry-forward planning
  ---
  duration_ms: 5.564028
  ...
# Subtest: full Pomodoro completion recovers after a deduplicated multi-target batch
ok 3133 - full Pomodoro completion recovers after a deduplicated multi-target batch
  ---
  duration_ms: 6.443988
  ...
# Subtest: full Pomodoro completion moves a marked same-note link without history
ok 3134 - full Pomodoro completion moves a marked same-note link without history
  ---
  duration_ms: 0.573545
  ...
# Subtest: cycler LK1–LK19 recognises only relation line shapes
ok 3135 - cycler LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 1.643839
  ...
# Subtest: cycler MC10, MC11, MC12 and MC14 keep relations inert while allowing root-only gestures
ok 3136 - cycler MC10, MC11, MC12 and MC14 keep relations inert while allowing root-only gestures
  ---
  duration_ms: 2.17873
  ...
# Subtest: SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
ok 3137 - SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
  ---
  duration_ms: 20.881344
  ...
# Subtest: SO2–SO5 fan-outs with explicit selection (SO32 twenty)
ok 3138 - SO2–SO5 fan-outs with explicit selection (SO32 twenty)
  ---
  duration_ms: 6.747096
  ...
# Subtest: SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
ok 3139 - SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
  ---
  duration_ms: 1.089351
  ...
# Subtest: SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
ok 3140 - SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
  ---
  duration_ms: 1.20968
  ...
# Subtest: SO stable keys survive insertions/status changes; ambiguous rebinding refused
ok 3141 - SO stable keys survive insertions/status changes; ambiguous rebinding refused
  ---
  duration_ms: 2.128564
  ...
# Subtest: SO picker model, pick normalization, and API detection
ok 3142 - SO picker model, pick normalization, and API detection
  ---
  duration_ms: 0.703784
  ...
# Subtest: SO notice copy for offers (SO20, mixed, failure)
ok 3143 - SO notice copy for offers (SO20, mixed, failure)
  ---
  duration_ms: 0.524592
  ...
# Subtest: destination override to an existing entry inserts as its child
ok 3144 - destination override to an existing entry inserts as its child
  ---
  duration_ms: 2.546163
  ...
# Subtest: destination override with a stale preimage skips loudly
ok 3145 - destination override with a stale preimage skips loudly
  ---
  duration_ms: 0.881614
  ...
# Subtest: destination override with a closed entry skips loudly
ok 3146 - destination override with a closed entry skips loudly
  ---
  duration_ms: 0.975203
  ...
# Subtest: destination override with a new name creates one placeholder after the running entry
ok 3147 - destination override with a new name creates one placeholder after the running entry
  ---
  duration_ms: 0.765562
  ...
# Subtest: destination override with a new name racing an open entry joins it
ok 3148 - destination override with a new name racing an open entry joins it
  ---
  duration_ms: 0.644781
  ...
# Subtest: reopen takes back the untouched successor link and restores status
ok 3149 - reopen takes back the untouched successor link and restores status
  ---
  duration_ms: 22.479606
  ...
# Subtest: an edited successor bullet survives while its status still restores
ok 3150 - an edited successor bullet survives while its status still restores
  ---
  duration_ms: 4.032621
  ...
# Subtest: an edited successor status line survives while its link is taken back
ok 3151 - an edited successor status line survives while its link is taken back
  ---
  duration_ms: 4.606558
  ...
# Subtest: reopen on a different day leaves successor links alone
ok 3152 - reopen on a different day leaves successor links alone
  ---
  duration_ms: 3.147312
  ...
# Subtest: reopening a task closed without a pass shows no take-back
ok 3153 - reopening a task closed without a pass shows no take-back
  ---
  duration_ms: 1.762447
  ...
# Subtest: Alt+] on a planned prerequisite links its successor
ok 3154 - Alt+] on a planned prerequisite links its successor
  ---
  duration_ms: 11.422337
  ...
# Subtest: take-back deletes a pre-existing entry it empties
ok 3155 - take-back deletes a pre-existing entry it empties
  ---
  duration_ms: 3.480688
  ...
# Subtest: take-back deletes a stub-replaced entry through the vault
ok 3156 - take-back deletes a stub-replaced entry through the vault
  ---
  duration_ms: 0.496168
  ...
# Subtest: take-back keeps entries that are closed or keep another child
ok 3157 - take-back keeps entries that are closed or keep another child
  ---
  duration_ms: 0.462974
  ...
# Subtest: closing-entry relocation finds a deferred-only placeholder
ok 3158 - closing-entry relocation finds a deferred-only placeholder
  ---
  duration_ms: 0.547225
  ...
# Subtest: Alt+[ into Cancelled recovers its dependents without linking
ok 3159 - Alt+[ into Cancelled recovers its dependents without linking
  ---
  duration_ms: 2.880301
  ...
# Subtest: take-back keeps an entry whose prose survives across a blank line (both paths)
ok 3160 - take-back keeps an entry whose prose survives across a blank line (both paths)
  ---
  duration_ms: 0.556984
  ...
# Subtest: take-back deletes a whole block with continuation/fence leftovers (LF/CRLF, final newline)
ok 3161 - take-back deletes a whole block with continuation/fence leftovers (LF/CRLF, final newline)
  ---
  duration_ms: 0.870973
  ...
# Subtest: link close links the unblocked successor into the slot and shows the nav card
ok 3162 - link close links the unblocked successor into the slot and shows the nav card
  ---
  duration_ms: 19.536144
  ...
# Subtest: close with no [id::] performs zero vault reads and shows nothing
ok 3163 - close with no [id::] performs zero vault reads and shows nothing
  ---
  duration_ms: 1.022974
  ...
# Subtest: Warm finalize reads no unrelated note bodies on the real close path
ok 3164 - Warm finalize reads no unrelated note bodies on the real close path
  ---
  duration_ms: 2.764369
  ...
# Subtest: cold fallback still recovers and links without a Tasks cache
ok 3165 - cold fallback still recovers and links without a Tasks cache
  ---
  duration_ms: 3.239225
  ...
# Subtest: recovered-only close reports unblocked without linking (SO4 Esc)
ok 3166 - recovered-only close reports unblocked without linking (SO4 Esc)
  ---
  duration_ms: 1.444569
  ...
# Subtest: walk landing composes a single toast and shows no card
ok 3167 - walk landing composes a single toast and shows no card
  ---
  duration_ms: 7.473665
  ...
# Subtest: nav absent falls back to a plain Notice with no link (SO missing picker)
ok 3168 - nav absent falls back to a plain Notice with no link (SO missing picker)
  ---
  duration_ms: 2.037261
  ...
# Subtest: stale cache heals via re-plan from fresh text (SO30)
ok 3169 - stale cache heals via re-plan from fresh text (SO30)
  ---
  duration_ms: 1.798435
  ...
# Subtest: Pomodoro-line close appends the successor to the created continuation
ok 3170 - Pomodoro-line close appends the successor to the created continuation
  ---
  duration_ms: 5.01074
  ...
# Subtest: Pomodoro-line close keeps the closing anchor after the picker re-plan
ok 3171 - Pomodoro-line close keeps the closing anchor after the picker re-plan
  ---
  duration_ms: 2.682994
  ...
# Subtest: completeTaskAtCursor returns the notice and shows nothing itself
ok 3172 - completeTaskAtCursor returns the notice and shows nothing itself
  ---
  duration_ms: 2.373894
  ...
# Subtest: successor apply recovers project residents without ledger v12
ok 3173 - successor apply recovers project residents without ledger v12
  ---
  duration_ms: 12.730864
  ...
# Subtest: SB vectors pin the successor mint pipeline
ok 3174 - SB vectors pin the successor mint pipeline
  ---
  duration_ms: 2.510605
  ...
# Subtest: successor suggester ports the Rust candidate and suffix rules
ok 3175 - successor suggester ports the Rust candidate and suffix rules
  ---
  duration_ms: 0.847799
  ...
# Subtest: successor link form names unique basenames short and the day file always
ok 3176 - successor link form names unique basenames short and the day file always
  ---
  duration_ms: 0.442004
  ...
# Subtest: tasksFromDocuments normalizes vault lines to pool shape
ok 3177 - tasksFromDocuments normalizes vault lines to pool shape
  ---
  duration_ms: 1.140619
  ...
# Subtest: normalizeTasksCacheTask ports every known Tasks shape
ok 3178 - normalizeTasksCacheTask ports every known Tasks shape
  ---
  duration_ms: 0.477081
  ...
# Subtest: buildDependentsIndex keeps first task IDs and groups dependents
ok 3179 - buildDependentsIndex keeps first task IDs and groups dependents
  ---
  duration_ms: 0.204921
  ...
# Subtest: findLiveLinks counts plain, embedded, and deferred links under open entries only
ok 3180 - findLiveLinks counts plain, embedded, and deferred links under open entries only
  ---
  duration_ms: 2.426074
  ...
# Subtest: computeSuccessorAnchors implements closing, slot, inherit, and none
ok 3181 - computeSuccessorAnchors implements closing, slot, inherit, and none
  ---
  duration_ms: 0.885251
  ...
# Subtest: SL1 links the successor right after the predecessor bullet
ok 3182 - SL1 links the successor right after the predecessor bullet
  ---
  duration_ms: 5.630784
  ...
# Subtest: SL3 still-blocked rows count the open prerequisites left
ok 3183 - SL3 still-blocked rows count the open prerequisites left
  ---
  duration_ms: 0.878678
  ...
# Subtest: SL4 future-scheduled dependents stay Blocked with the date row
ok 3184 - SL4 future-scheduled dependents stay Blocked with the date row
  ---
  duration_ms: 0.598924
  ...
# Subtest: SL5 already-planned dependents recover without a duplicate link
ok 3185 - SL5 already-planned dependents recover without a duplicate link
  ---
  duration_ms: 0.993497
  ...
# Subtest: SL6 struck and closed-entry links do not count as planned
ok 3186 - SL6 struck and closed-entry links do not count as planned
  ---
  duration_ms: 1.453556
  ...
# Subtest: SL7 closing anchors create the continuation placeholder
ok 3187 - SL7 closing anchors create the continuation placeholder
  ---
  duration_ms: 1.008456
  ...
# Subtest: SL8 closing anchors append after carried lines in the continuation
ok 3188 - SL8 closing anchors append after carried lines in the continuation
  ---
  duration_ms: 0.821659
  ...
# Subtest: SL9 unplanned predecessors offer at the implicit destination (SO14)
ok 3189 - SL9 unplanned predecessors offer at the implicit destination (SO14)
  ---
  duration_ms: 1.269665
  ...
# Subtest: SL10 missing block IDs mint through the SB rule
ok 3190 - SL10 missing block IDs mint through the SB rule
  ---
  duration_ms: 0.560251
  ...
# Subtest: SL11 project and hidden tasks recover but never link
ok 3191 - SL11 project and hidden tasks recover but never link
  ---
  duration_ms: 9.061498
  ...
# Subtest: PDC1 leaves a dependency-ready resident Blocked while its project still waits
ok 3192 - PDC1 leaves a dependency-ready resident Blocked while its project still waits
  ---
  duration_ms: 2.106393
  ...
# Subtest: PDC2 residents are offered under the project group (SO1)
ok 3193 - PDC2 residents are offered under the project group (SO1)
  ---
  duration_ms: 1.426715
  ...
# Subtest: PDC3 keeps a project resident Blocked when its own prerequisite remains open
ok 3194 - PDC3 keeps a project resident Blocked when its own prerequisite remains open
  ---
  duration_ms: 0.891593
  ...
# Subtest: PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
ok 3195 - PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
  ---
  duration_ms: 2.407769
  ...
# Subtest: SL12 one gesture closing two prerequisites links once with both causes
ok 3196 - SL12 one gesture closing two prerequisites links once with both causes
  ---
  duration_ms: 0.561583
  ...
# Subtest: SL13 chains do not recurse: the dependent's own dependents wait
ok 3197 - SL13 chains do not recurse: the dependent's own dependents wait
  ---
  duration_ms: 0.341251
  ...
# Subtest: SL14 ambiguous basenames link long
ok 3198 - SL14 ambiguous basenames link long
  ---
  duration_ms: 0.313038
  ...
# Subtest: SL15 stale open dependents link and become Next
ok 3199 - SL15 stale open dependents link and become Next
  ---
  duration_ms: 0.279644
  ...
# Subtest: SL16 gates on [id::]: no identity means no lookup and empty rows
ok 3200 - SL16 gates on [id::]: no identity means no lookup and empty rows
  ---
  duration_ms: 0.19925
  ...
# Subtest: SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
ok 3201 - SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
  ---
  duration_ms: 1.204771
  ...
# Subtest: SL18 the kill switch recovers without linking or minting
ok 3202 - SL18 the kill switch recovers without linking or minting
  ---
  duration_ms: 0.331423
  ...
# Subtest: SL19 re-applied closes write nothing and report nothing
ok 3203 - SL19 re-applied closes write nothing and report nothing
  ---
  duration_ms: 0.272831
  ...
# Subtest: SL23 subtasks anchor at their root's link
ok 3204 - SL23 subtasks anchor at their root's link
  ---
  duration_ms: 0.415283
  ...
# Subtest: SL24 later same-name entries take the closing successors
ok 3205 - SL24 later same-name entries take the closing successors
  ---
  duration_ms: 0.539781
  ...
# Subtest: SL25 already-Next planned dependents produce no row
ok 3206 - SL25 already-Next planned dependents produce no row
  ---
  duration_ms: 0.461972
  ...
# Subtest: SL26 inbox successors carry the inbox flag
ok 3207 - SL26 inbox successors carry the inbox flag
  ---
  duration_ms: 0.356692
  ...
# Subtest: SL27 dropped links are never re-linked and recover to Ready
ok 3208 - SL27 dropped links are never re-linked and recover to Ready
  ---
  duration_ms: 0.445441
  ...
# Subtest: SL28 day-file successors name the note, never the bare link
ok 3209 - SL28 day-file successors name the note, never the bare link
  ---
  duration_ms: 0.355419
  ...
# Subtest: slot insertions land after the anchor subtree with its indent
ok 3210 - slot insertions land after the anchor subtree with its indent
  ---
  duration_ms: 0.374806
  ...
# Subtest: closing insertions replace a lone stub child
ok 3211 - closing insertions replace a lone stub child
  ---
  duration_ms: 0.546854
  ...
# Subtest: insertions skip placements with no valid target
ok 3212 - insertions skip placements with no valid target
  ---
  duration_ms: 0.160887
  ...
# Subtest: successorNoticeText implements the §12.6 table
ok 3213 - successorNoticeText implements the §12.6 table
  ---
  duration_ms: 0.535012
  ...
# Subtest: parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
ok 3214 - parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
  ---
  duration_ms: 0.402469
  ...
# Subtest: loadLinkUnblocked stat-caches the config read
ok 3215 - loadLinkUnblocked stat-caches the config read
  ---
  duration_ms: 0.302718
  ...
# Subtest: loadLinkUnblocked treats missing or unreadable config as true
ok 3216 - loadLinkUnblocked treats missing or unreadable config as true
  ---
  duration_ms: 1.264004
  ...
# Subtest: successorPlanConfigPath honors XDG_CONFIG_HOME
ok 3217 - successorPlanConfigPath honors XDG_CONFIG_HOME
  ---
  duration_ms: 0.174604
  ...
# Subtest: todayDailyPath mirrors the ledger daily path
ok 3218 - todayDailyPath mirrors the ledger daily path
  ---
  duration_ms: 0.560501
  ...
# Subtest: normalizeClosedTaskIdentities keeps the anchor root off the match gate
ok 3219 - normalizeClosedTaskIdentities keeps the anchor root off the match gate
  ---
  duration_ms: 0.215501
  ...
# Subtest: ID-less planned roots anchor ID-bearing children without minting IDs
ok 3220 - ID-less planned roots anchor ID-bearing children without minting IDs
  ---
  duration_ms: 0.780009
  ...
# Subtest: successor anchors never guess across roots
ok 3221 - successor anchors never guess across roots
  ---
  duration_ms: 0.476981
  ...
# Subtest: a child with its own live link keeps its own slot
ok 3222 - a child with its own live link keeps its own slot
  ---
  duration_ms: 0.464257
  ...
# Subtest: getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
ok 3223 - getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
  ---
  duration_ms: 0.295835
  ...
# Subtest: countSuccessorBasenames walks the vault set, not the task set
ok 3224 - countSuccessorBasenames walks the vault set, not the task set
  ---
  duration_ms: 0.351451
  ...
# Subtest: the pass threads a richer isInbox into unblocked rows
ok 3225 - the pass threads a richer isInbox into unblocked rows
  ---
  duration_ms: 0.394434
  ...
# Subtest: getTaskLinkLaneApi returns the lane only when version and both functions exist
ok 3226 - getTaskLinkLaneApi returns the lane only when version and both functions exist
  ---
  duration_ms: 1.088248
  ...
# Subtest: isTaskLinkLaneLine passes content, line, and path and never throws
ok 3227 - isTaskLinkLaneLine passes content, line, and path and never throws
  ---
  duration_ms: 1.07843
  ...
# Subtest: single Alt+] on a Task Link delegates with exactly { editor, view }
ok 3228 - single Alt+] on a Task Link delegates with exactly { editor, view }
  ---
  duration_ms: 0.525754
  ...
# Subtest: Alt+[ and Alt+] delegate identically; direction is ignored
ok 3229 - Alt+[ and Alt+] delegate identically; direction is ignored
  ---
  duration_ms: 0.318979
  ...
# Subtest: embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
ok 3230 - embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
  ---
  duration_ms: 0.314521
  ...
# Subtest: entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
ok 3231 - entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
  ---
  duration_ms: 2.769049
  ...
# Subtest: counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
ok 3232 - counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
  ---
  duration_ms: 0.641545
  ...
# Subtest: counted dispatch without an explicit repeat leaves the key alone
ok 3233 - counted dispatch without an explicit repeat leaves the key alone
  ---
  duration_ms: 0.20952
  ...
# Subtest: counted range starting elsewhere skips Task Link lines
ok 3234 - counted range starting elsewhere skips Task Link lines
  ---
  duration_ms: 1.820888
  ...
# Subtest: legacy fallback with no api keeps today's behavior
ok 3235 - legacy fallback with no api keeps today's behavior
  ---
  duration_ms: 0.71174
  ...
# Subtest: plain Task Link in an open Pomodoro closes the task root-only and strikes the link
ok 3236 - plain Task Link in an open Pomodoro closes the task root-only and strikes the link
  ---
  duration_ms: 13.982904
  ...
# Subtest: marked plain Task Link drops its marker when struck under Pomodoro ancestry
ok 3237 - marked plain Task Link drops its marker when struck under Pomodoro ancestry
  ---
  duration_ms: 1.54464
  ...
# Subtest: plain Pomodoro Task Link closes root-only while embedded closes recursively
ok 3238 - plain Pomodoro Task Link closes root-only while embedded closes recursively
  ---
  duration_ms: 2.19366
  ...
# Subtest: embedded Pomodoro Task Link still closes recursively and retires to struck form
ok 3239 - embedded Pomodoro Task Link still closes recursively and retires to struck form
  ---
  duration_ms: 2.516396
  ...
# Subtest: Ctrl+Enter toggles a struck plain Pomodoro link back to open
ok 3240 - Ctrl+Enter toggles a struck plain Pomodoro link back to open
  ---
  duration_ms: 1.637137
  ...
# Subtest: same-file plain Task Link closes and strikes the correct line
ok 3241 - same-file plain Task Link closes and strikes the correct line
  ---
  duration_ms: 1.138525
  ...
# Subtest: cursor selects which of several Task Links closes and strikes
ok 3242 - cursor selects which of several Task Links closes and strikes
  ---
  duration_ms: 1.328307
  ...
# Subtest: plain links to Blocked or non-task blocks still complete the Pomodoro
ok 3243 - plain links to Blocked or non-task blocks still complete the Pomodoro
  ---
  duration_ms: 3.613031
  ...
# Subtest: strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
ok 3244 - strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
  ---
  duration_ms: 0.518411
  ...
# Subtest: completeTaskAtCursor closes each open symbol through the Tasks command
ok 3245 - completeTaskAtCursor closes each open symbol through the Tasks command
  ---
  duration_ms: 1.624483
  ...
# Subtest: completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
ok 3246 - completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
  ---
  duration_ms: 0.344658
  ...
# Subtest: completeTaskAtCursor refuses closed, cancelled, and non-task lines
ok 3247 - completeTaskAtCursor refuses closed, cancelled, and non-task lines
  ---
  duration_ms: 0.309881
  ...
# Subtest: completeTaskAtCursor refuses a missing Tasks command with no write
ok 3248 - completeTaskAtCursor refuses a missing Tasks command with no write
  ---
  duration_ms: 0.166748
  ...
# Subtest: Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
ok 3249 - Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
  ---
  duration_ms: 0.500657
  ...
# Subtest: completeTaskAtCursor reports not-closed when Tasks does not write [x]
ok 3250 - completeTaskAtCursor reports not-closed when Tasks does not write [x]
  ---
  duration_ms: 0.16748
  ...
# Subtest: recovery api is frozen at version 2 and recovers without striking references
ok 3251 - recovery api is frozen at version 2 and recovers without striking references
  ---
  duration_ms: 2.53392
  ...
# Subtest: recovery api never throws and reports failures
ok 3252 - recovery api never throws and reports failures
  ---
  duration_ms: 0.199501
  ...
# Subtest: future-scheduled dependents stay Blocked on the planner, api, and close paths
ok 3253 - future-scheduled dependents stay Blocked on the planner, api, and close paths
  ---
  duration_ms: 15.115117
  ...
# Subtest: Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
ok 3254 - Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
  ---
  duration_ms: 3.867407
  ...
# Subtest: every printable non-space ASCII key resolves to a surround pair
ok 3255 - every printable non-space ASCII key resolves to a surround pair
  ---
  duration_ms: 3.931259
  ...
# Subtest: visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
ok 3256 - visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
  ---
  duration_ms: 0.715837
  ...
# Subtest: non-visible, combining, multi-character, and multi-code-unit values are rejected
ok 3257 - non-visible, combining, multi-character, and multi-code-unit values are rejected
  ---
  duration_ms: 0.245829
  ...
# Subtest: ys adds broad symmetric delimiters through pending keydown
ok 3258 - ys adds broad symmetric delimiters through pending keydown
  ---
  duration_ms: 1.275867
  ...
# Subtest: rejected keydown input never edits or leaks into a pending ys
ok 3259 - rejected keydown input never edits or leaks into a pending ys
  ---
  duration_ms: 0.43432
  ...
# Subtest: Escape cancels ys, cs, and ds pending state without editing
ok 3260 - Escape cancels ys, cs, and ds pending state without editing
  ---
  duration_ms: 0.272691
  ...
# Subtest: cs accepts broad target and replacement characters independently
ok 3261 - cs accepts broad target and replacement characters independently
  ---
  duration_ms: 1.107596
  ...
# Subtest: cs preserves structural alias and padding rules
ok 3262 - cs preserves structural alias and padding rules
  ---
  duration_ms: 1.624723
  ...
# Subtest: cs replaces repeated symmetric runs exactly once on each side
ok 3263 - cs replaces repeated symmetric runs exactly once on each side
  ---
  duration_ms: 0.542967
  ...
# Subtest: ds removes representative broad symmetric delimiters
ok 3264 - ds removes representative broad symmetric delimiters
  ---
  duration_ms: 0.787935
  ...
# Subtest: ds preserves structural alias and padding rules
ok 3265 - ds preserves structural alias and padding rules
  ---
  duration_ms: 0.312827
  ...
# Subtest: ds removes one pair from repeated runs, including the reported block link
ok 3266 - ds removes one pair from repeated runs, including the reported block link
  ---
  duration_ms: 1.096164
  ...
# Subtest: consecutive ds commands peel a triple symmetric surround
ok 3267 - consecutive ds commands peel a triple symmetric surround
  ---
  duration_ms: 0.267561
  ...
# Subtest: symmetric discovery uses deterministic sequential same-line run pairs
ok 3268 - symmetric discovery uses deterministic sequential same-line run pairs
  ---
  duration_ms: 0.185093
  ...
# Subtest: symmetric discovery includes every character in repeated boundaries
ok 3269 - symmetric discovery includes every character in repeated boundaries
  ---
  duration_ms: 0.301767
  ...
# Subtest: unpaired and unequal symmetric runs are safe no-ops
ok 3270 - unpaired and unequal symmetric runs are safe no-ops
  ---
  duration_ms: 0.247883
  ...
# Subtest: ordinary normal-mode keys remain untouched outside pending state
ok 3271 - ordinary normal-mode keys remain untouched outside pending state
  ---
  duration_ms: 0.215241
  ...
# Subtest: dot while a surround is pending is a literal delimiter, not repeat
ok 3272 - dot while a surround is pending is a literal delimiter, not repeat
  ---
  duration_ms: 0.123155
  ...
# Subtest: dot-repeat records and replays broad-character ys
ok 3273 - dot-repeat records and replays broad-character ys
  ---
  duration_ms: 0.252031
  ...
# Subtest: dot-repeat records and replays broad-character cs
ok 3274 - dot-repeat records and replays broad-character cs
  ---
  duration_ms: 0.190133
  ...
# Subtest: dot-repeat records and replays broad-character ds
ok 3275 - dot-repeat records and replays broad-character ds
  ---
  duration_ms: 0.187739
  ...
# Subtest: dot-repeat replays cs against repeated symmetric runs
ok 3276 - dot-repeat replays cs against repeated symmetric runs
  ---
  duration_ms: 0.221694
  ...
# Subtest: dot-repeat replays ds against repeated symmetric runs
ok 3277 - dot-repeat replays ds against repeated symmetric runs
  ---
  duration_ms: 0.226202
  ...
# Subtest: consecutive dot-repeats peel a triple symmetric surround
ok 3278 - consecutive dot-repeats peel a triple symmetric surround
  ---
  duration_ms: 0.222414
  ...
1..3278
# tests 3288
# suites 0
# pass 3282
# fail 6
# cancelled 0
# skipped 0
# todo 0
# duration_ms 7165.985477
failed  exit=1  duration=15635ms

