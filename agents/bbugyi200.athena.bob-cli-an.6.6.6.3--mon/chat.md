# Chat History - ace-run (bob-cli-an.6.6.6.3--mon)

- **TIMESTAMP:** 2026-10-24 05:53:04 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-an.6.6.6.3--mon

## Prompt

sase monitor start --command 'npm test' --reason 'Run the full bob-plugins suite for phase bob-cli-an.6.6.6.3'

## Response

sase tool run 9a68e8fc1af40406411d7b183d3f0980

> bob-plugins@0.1.0 test
> node scripts/build-plugins.mjs --check && npm run docs:inventory:check && node --test scripts/test-project-tasks-snapshot.cjs scripts/test-bob-articles.cjs scripts/test-dependency-line-migration.cjs scripts/test-navigation-hotkeys-section-nav.cjs scripts/test-navigation-hotkeys-rename.cjs scripts/test-navigation-hotkeys-ref-pdf.cjs scripts/test-navigation-hotkeys-templater-trigger.cjs scripts/test-navigation-hotkeys-schedule-recovery.cjs scripts/test-navigation-hotkeys-schedule-properties.cjs scripts/test-navigation-hotkeys-schedule-writes.cjs scripts/test-navigation-hotkeys-runtime-schedule.cjs scripts/test-navigation-hotkeys-dependencies.cjs scripts/test-navigation-blocks-guards.cjs scripts/test-navigation-blocks-writers.cjs scripts/test-navigation-blocks-edit.cjs scripts/test-navigation-blocks-stage-view.cjs scripts/test-navigation-hotkeys-dependency-mirror.cjs scripts/test-navigation-hotkeys-task-move-plan.cjs scripts/test-navigation-hotkeys-priority-notice.cjs scripts/test-navigation-successor-picker.cjs scripts/test-navigation-image-zoom-viewer.cjs scripts/test-navigation-hotkeys-unblocked-notice.cjs scripts/test-navigation-project-blocking.cjs scripts/test-navigation-project-dependency-stage.cjs scripts/test-navigation-project-subprojects.cjs scripts/test-navigation-project-subtree-gestures.cjs scripts/test-navigation-hotkeys-priority-picker.cjs scripts/test-navigation-hotkeys-picker-lifecycle.cjs scripts/test-navigation-hotkeys-ref-picker-text.cjs scripts/test-navigation-hotkeys-pomodoro-move-pickers.cjs scripts/test-navigation-inbox-route.cjs scripts/test-navigation-inbox-route-card.cjs scripts/test-navigation-hotkeys-task-move.cjs scripts/test-navigation-open-notes-uri.cjs scripts/test-navigation-hotkeys-dash-open.cjs scripts/test-navigation-goto-task-uri.cjs scripts/test-navigation-hotkeys-open-task-jump.cjs scripts/test-navigation-hotkeys-vim-counts.cjs scripts/test-navigation-hotkeys-tab-pin.cjs scripts/test-navigation-hotkeys-schedule-log.cjs scripts/test-navigation-hotkeys-schedule-review.cjs scripts/test-navigation-hotkeys-deferred-pomodoro.cjs scripts/test-navigation-hotkeys-pomodoro-parse.cjs scripts/test-navigation-hotkeys-pomodoro-bullet-move.cjs scripts/test-navigation-hotkeys-pomodoro-split-rename.cjs scripts/test-navigation-hotkeys-pomodoro-reorder.cjs scripts/test-navigation-hotkeys-runtime-prune.cjs scripts/test-navigation-hotkeys-project-from-task.cjs scripts/test-navigation-hotkeys-project-reversal.cjs scripts/test-navigation-hotkeys-link-picker.cjs scripts/test-navigation-hotkeys-lane-toggle.cjs scripts/test-navigation-hotkeys-task-link-lane.cjs scripts/test-navigation-hotkeys-cancel-log.cjs scripts/test-navigation-hotkeys-cancel-task.cjs scripts/test-navigation-hotkeys-forward-promotion.cjs scripts/test-navigation-hotkeys-schedule-work-log.cjs scripts/test-navigation-hotkeys-task-move-history.cjs scripts/test-navigation-jump-history.cjs scripts/test-navigation-dependencies.cjs scripts/test-navigation-editor-line-diff.cjs scripts/test-navigation-quick-roll.cjs scripts/test-navigation-quick-roll-preview.cjs scripts/test-navigation-roll-decay.cjs scripts/test-navigation-decay-planner.cjs scripts/test-navigation-task-card-model.cjs scripts/test-navigation-task-card-view.cjs scripts/test-navigation-task-card-schedule.cjs scripts/test-navigation-task-card-review.cjs scripts/test-navigation-decision-card.cjs scripts/test-navigation-decision-card-handlers.cjs scripts/test-navigation-decision-card-keep.cjs scripts/test-navigation-refresh-modal.cjs scripts/test-navigation-freshness.cjs scripts/test-navigation-stamps.cjs scripts/test-navigation-keep-counting.cjs scripts/test-navigation-rotten-keep.cjs scripts/test-navigation-rotten-log.cjs scripts/test-navigation-checklist.cjs scripts/test-navigation-review-advance.cjs scripts/test-navigation-review-advance-gestures.cjs scripts/test-navigation-checklist-ctrl-enter.cjs scripts/test-ledger-tools-navigation.cjs scripts/test-ledger-tools-plan-budget.cjs scripts/test-ledger-tools-ready-badge.cjs scripts/test-ledger-tools-note-ready.cjs scripts/test-ledger-tools-note-ready-views.cjs scripts/test-ledger-tools-dashboard-parity.cjs scripts/test-ledger-tools-work-badge-tone.cjs scripts/test-ledger-tools-dashboard-collections.cjs scripts/test-ledger-tools-today.cjs scripts/test-ledger-tools-freshness-placement.cjs scripts/test-ledger-tools-freshness-states.cjs scripts/test-ledger-tools-freshness-namespace.cjs scripts/test-ledger-tools-freshness-review-model.cjs scripts/test-ledger-tools-freshness-queue.cjs scripts/test-ledger-tools-freshness-tracking.cjs scripts/test-ledger-tools-freshness-footer.cjs scripts/test-ledger-tools-freshness-recurring.cjs scripts/test-ledger-tools-freshness-mark.cjs scripts/test-ledger-tools-freshness-mark-surfaces.cjs scripts/test-ledger-tools-priority-marks.cjs scripts/test-ledger-tools-task-tag-marks.cjs scripts/test-ledger-tools-today-marks.cjs scripts/test-ledger-tools-today-marks-reading.cjs scripts/test-ledger-tools-unblocked-glyph.cjs scripts/test-ledger-tools-progress-marks.cjs scripts/test-ledger-tools-date-marks.cjs scripts/test-ledger-tools-recurrence-marks.cjs scripts/test-ledger-tools-date-marks-tasks.cjs scripts/test-ledger-tools-freshness-keeps.cjs scripts/test-ledger-tools-freshness-unblocked.cjs scripts/test-ledger-tools-freshness-decision-card.cjs scripts/test-ledger-tools-dependency-chips.cjs scripts/test-ledger-tools-blocks-chips.cjs scripts/test-ledger-tools-snippets.cjs scripts/test-ledger-tools-vim-mappings.cjs scripts/test-task-status-cycler-dependencies.cjs scripts/test-task-status-cycler-blocks-guards.cjs scripts/test-task-status-cycler-ctrl-enter.cjs scripts/test-task-status-cycler-reference-lifecycle.cjs scripts/test-task-status-cycler-pomodoro-completion.cjs scripts/test-task-status-cycler-pomodoro-work-log.cjs scripts/test-task-status-cycler-pomodoro-reopen.cjs scripts/test-task-status-cycler-blocked-schedule.cjs scripts/test-task-status-cycler-demotion-picker.cjs scripts/test-task-status-cycler-promotion.cjs scripts/test-task-status-cycler-counted-toggle.cjs scripts/test-task-status-cycler-successors.cjs scripts/test-task-status-cycler-successor-wiring.cjs scripts/test-task-status-cycler-successor-polish.cjs scripts/test-task-status-cycler-successor-offers.cjs scripts/test-task-status-cycler-project-pull-in.cjs scripts/test-task-status-cycler-task-links-api.cjs scripts/test-task-status-cycler-task-link-lane.cjs scripts/test-task-status-cycler-freshness.cjs scripts/test-block-id-prompt-dependencies.cjs scripts/test-block-id-prompt-blocks-guards.cjs scripts/test-block-id-prompt-ref-picker-text.cjs scripts/test-block-id-prompt-markers.cjs scripts/test-block-id-prompt-pomodoro-context.cjs scripts/test-block-id-prompt-target-update.cjs scripts/test-block-id-prompt-pomodoro-insertion.cjs scripts/test-block-id-prompt-pomodoro-targets.cjs scripts/test-block-id-prompt-pomodoro-picker-view.cjs scripts/test-block-id-prompt-pomodoro-picker-runtime.cjs scripts/test-block-id-prompt-work-log.cjs scripts/test-block-id-prompt-pomodoro-link-runtime.cjs scripts/test-block-id-prompt-pomodoro-link-picker-api.cjs scripts/test-block-id-prompt-pomodoro-unlink-runtime.cjs scripts/test-block-id-prompt-task-link-deletion.cjs scripts/test-block-id-prompt-plan-budget-and-freshness.cjs scripts/test-prompt-block-id-naming.cjs scripts/test-block-id-prompt-prefill.cjs scripts/test-vim-surround.cjs scripts/test-navigation-dependencies-stage-ranker-and-pool.cjs scripts/test-navigation-dependencies-stage-entry-and-view.cjs scripts/test-navigation-dependencies-stage-writes.cjs scripts/test-navigation-dependencies-stage-mirror-and-badge.cjs scripts/test-navigation-dependencies-stage-stale-guards.cjs scripts/test-navigation-dependencies-stage-performance.cjs scripts/test-navigation-prompt-block-id-stage.cjs scripts/test-navigation-dependencies-writer.cjs scripts/test-navigation-dependency-link-consumption.cjs scripts/test-plugin-build.cjs scripts/test-ledger-tools-stats-journal.cjs scripts/test-ledger-tools-stats-data.cjs scripts/test-ledger-tools-stats-block.cjs scripts/test-ledger-tools-stats-charts.cjs scripts/test-navigation-review-journal.cjs scripts/test-ledger-tools-stats-panels.cjs scripts/test-ledger-tools-reading-board-data.cjs scripts/test-ledger-tools-reading-board-models.cjs scripts/test-ledger-tools-reading-board-block.cjs scripts/test-ledger-tools-pomodoro-home-chips.cjs scripts/test-navigation-image-zoom-target.cjs scripts/test-navigation-image-zoom-command.cjs scripts/test-docs-inventory.mjs scripts/test-docs-check.mjs scripts/test-navigation-relation-lines.cjs scripts/test-navigation-relation-writer.cjs scripts/test-navigation-relation-links-stage.cjs scripts/test-relation-index-linked-from-stage.cjs scripts/test-ledger-tools-relations.cjs scripts/test-ledger-tools-relation-index.cjs scripts/test-ledger-tools-relation-chips.cjs scripts/test-task-status-cycler-relations.cjs scripts/test-block-id-prompt-relations.cjs

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
  duration_ms: 1.603229
  ...
# Subtest: bip BK13–BK15 malformed split mirrors the Depends-On twin
ok 2 - bip BK13–BK15 malformed split mirrors the Depends-On twin
  ---
  duration_ms: 0.518399
  ...
# Subtest: bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
ok 3 - bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
  ---
  duration_ms: 0.145568
  ...
# Subtest: bip MC1/MC2 Pomodoro scanners skip managed lines
ok 4 - bip MC1/MC2 Pomodoro scanners skip managed lines
  ---
  duration_ms: 1.532946
  ...
# Subtest: explicit task IDs exclusively own dependency lookup
ok 5 - explicit task IDs exclusively own dependency lookup
  ---
  duration_ms: 3.750258
  ...
# Subtest: legacy tasks without an id field still fall back to their block ID
ok 6 - legacy tasks without an id field still fall back to their block ID
  ---
  duration_ms: 0.409301
  ...
# Subtest: blocked-link consumption raises open prerequisites and leaves the dependent blocked
ok 7 - blocked-link consumption raises open prerequisites and leaves the dependent blocked
  ---
  duration_ms: 1.542303
  ...
# Subtest: project-blocked member consumption promotes the project's open prerequisite
ok 8 - project-blocked member consumption promotes the project's open prerequisite
  ---
  duration_ms: 1.109117
  ...
# Subtest: project-blocked resident consumption promotes the project's open prerequisite
ok 9 - project-blocked resident consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.653797
  ...
# Subtest: a tagged inherited ^prj target is refused with its parent named
ok 10 - a tagged inherited ^prj target is refused with its parent named
  ---
  duration_ms: 0.407207
  ...
# Subtest: project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
ok 11 - project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
  ---
  duration_ms: 1.758816
  ...
# Subtest: project date refusal applies only when the date is the sole project reason
ok 12 - project date refusal applies only when the date is the sole project reason
  ---
  duration_ms: 0.289403
  ...
# Subtest: a project-blocked tag is token-bounded and ignored on lookalike tags
ok 13 - a project-blocked tag is token-bounded and ignored on lookalike tags
  ---
  duration_ms: 0.556271
  ...
# Subtest: task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
ok 14 - task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
  ---
  duration_ms: 1.008224
  ...
# Subtest: task blocked state unifies status and dependency reasons
ok 15 - task blocked state unifies status and dependency reasons
  ---
  duration_ms: 0.423959
  ...
# Subtest: task picker partition sinks blocked tasks while preserving group order
ok 16 - task picker partition sinks blocked tasks while preserving group order
  ---
  duration_ms: 0.295504
  ...
# Subtest: blocked chip labels show useful unmet dependency counts
ok 17 - blocked chip labels show useful unmet dependency counts
  ---
  duration_ms: 0.149174
  ...
# Subtest: blocked tooltips explain dependency and status-only reasons
ok 18 - blocked tooltips explain dependency and status-only reasons
  ---
  duration_ms: 0.323107
  ...
# Subtest: task status classes cover every open task status
ok 19 - task status classes cover every open task status
  ---
  duration_ms: 0.145188
  ...
# Subtest: Blocked tasks remain unmet dependency targets
ok 20 - Blocked tasks remain unmet dependency targets
  ---
  duration_ms: 0.189361
  ...
# Subtest: blocked task count covers both reasons without double-counting
ok 21 - blocked task count covers both reasons without double-counting
  ---
  duration_ms: 0.164665
  ...
# Subtest: single caret relocation preserves embedding and removes aliases
ok 22 - single caret relocation preserves embedding and removes aliases
  ---
  duration_ms: 2.420839
  ...
# Subtest: single caret relocation resets aliased block links
ok 23 - single caret relocation resets aliased block links
  ---
  duration_ms: 0.36176
  ...
# Subtest: single caret relocation strips heading and block subpaths
ok 24 - single caret relocation strips heading and block subpaths
  ---
  duration_ms: 0.354066
  ...
# Subtest: task picker normalizes every supported wiki block-link form
ok 25 - task picker normalizes every supported wiki block-link form
  ---
  duration_ms: 0.976112
  ...
# Subtest: three or more carets never trigger the task picker
ok 26 - three or more carets never trigger the task picker
  ---
  duration_ms: 0.205462
  ...
# Subtest: rapid aliased task picker completion preserves the alias
ok 27 - rapid aliased task picker completion preserves the alias
  ---
  duration_ms: 3.782439
  ...
# Subtest: task picker recognition is independent of Markdown source context
ok 28 - task picker recognition is independent of Markdown source context
  ---
  duration_ms: 1.128133
  ...
# Subtest: task picker recognition respects cursor proximity and fenced code
ok 29 - task picker recognition respects cursor proximity and fenced code
  ---
  duration_ms: 0.371609
  ...
# Subtest: plan budget suffix: link Notice appends the meter computed on post-write daily content
ok 30 - plan budget suffix: link Notice appends the meter computed on post-write daily content
  ---
  duration_ms: 7.182176
  ...
# Subtest: plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
ok 31 - plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
  ---
  duration_ms: 1.704874
  ...
# Subtest: plan budget suffix: unlink Notice marks an over-cap plan with 🔴
ok 32 - plan budget suffix: unlink Notice marks an over-cap plan with 🔴
  ---
  duration_ms: 1.86002
  ...
# Subtest: plan budget suffix: Next task without a block ID prompts for one and omits the meter
ok 33 - plan budget suffix: Next task without a block ID prompts for one and omits the meter
  ---
  duration_ms: 0.39316
  ...
# Subtest: plan budget suffix: Task Link Notice appends the meter from post-write daily content
ok 34 - plan budget suffix: Task Link Notice appends the meter from post-write daily content
  ---
  duration_ms: 2.181403
  ...
# Subtest: plan budget suffix: Task Link Notice omits the meter when no daily note takes part
ok 35 - plan budget suffix: Task Link Notice omits the meter when no daily note takes part
  ---
  duration_ms: 0.57112
  ...
# Subtest: planTargetTaskUpdate stamps the rewritten line last via injected stamper
ok 36 - planTargetTaskUpdate stamps the rewritten line last via injected stamper
  ---
  duration_ms: 0.2722
  ...
# Subtest: planTargetTaskUpdate without a stamper never stamps (identity default)
ok 37 - planTargetTaskUpdate without a stamper never stamps (identity default)
  ---
  duration_ms: 0.141369
  ...
# Subtest: planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
ok 38 - planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
  ---
  duration_ms: 0.363042
  ...
# Subtest: planTargetTaskUpdate stamps a Next task that gains a block ID
ok 39 - planTargetTaskUpdate stamps a Next task that gains a block ID
  ---
  duration_ms: 0.467612
  ...
# Subtest: planTargetTaskUpdate tolerates a throwing stamper
ok 40 - planTargetTaskUpdate tolerates a throwing stamper
  ---
  duration_ms: 0.224689
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 41 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.436623
  ...
# Subtest: dedicated-link helpers reject Depends-On lines
ok 42 - dedicated-link helpers reject Depends-On lines
  ---
  duration_ms: 0.316625
  ...
# Subtest: Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
ok 43 - Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
  ---
  duration_ms: 0.359175
  ...
# Subtest: malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
ok 44 - malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
  ---
  duration_ms: 0.12569
  ...
# Subtest: Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
ok 45 - Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
  ---
  duration_ms: 0.265076
  ...
# Subtest: Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
ok 46 - Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
  ---
  duration_ms: 0.208348
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent
ok 47 - readPlanBudgetMeter keeps per-cap over flags independent
  ---
  duration_ms: 0.193139
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent (mirror)
ok 48 - readPlanBudgetMeter keeps per-cap over flags independent (mirror)
  ---
  duration_ms: 0.105421
  ...
# Subtest: block-id-prompt freshness accessors degrade without ledger-tools
ok 49 - block-id-prompt freshness accessors degrade without ledger-tools
  ---
  duration_ms: 0.209971
  ...
# Subtest: list item body bounds trim whitespace and reject empty bullets
ok 50 - list item body bounds trim whitespace and reject empty bullets
  ---
  duration_ms: 1.379062
  ...
# Subtest: Pomodoro activation eligibility requires a sole-content sub-bullet
ok 51 - Pomodoro activation eligibility requires a sole-content sub-bullet
  ---
  duration_ms: 1.958167
  ...
# Subtest: Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
ok 52 - Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
  ---
  duration_ms: 0.273762
  ...
# Subtest: Pomodoro source context distinguishes ledger ancestry and open state
ok 53 - Pomodoro source context distinguishes ledger ancestry and open state
  ---
  duration_ms: 0.525793
  ...
# Subtest: future cleanup touches only later open Pomodoros and counts duplicates
ok 54 - future cleanup touches only later open Pomodoros and counts duplicates
  ---
  duration_ms: 2.258711
  ...
# Subtest: cleanup resolves aliases, embeds, same-note links, and alternate paths
ok 55 - cleanup resolves aliases, embeds, same-note links, and alternate paths
  ---
  duration_ms: 1.714091
  ...
# Subtest: dedicated bullet subtree cleanup preserves CRLF line endings
ok 56 - dedicated bullet subtree cleanup preserves CRLF line endings
  ---
  duration_ms: 0.384814
  ...
# Subtest: existing-ID task completion prunes future links in the source editor
ok 57 - existing-ID task completion prunes future links in the source editor
  ---
  duration_ms: 2.464423
  ...
# Subtest: new-ID same-file completion plans cleanup after the task edit
ok 58 - new-ID same-file completion plans cleanup after the task edit
  ---
  duration_ms: 1.342793
  ...
# Subtest: findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
ok 59 - findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
  ---
  duration_ms: 1.963698
  ...
# Subtest: findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
ok 60 - findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
  ---
  duration_ms: 0.171036
  ...
# Subtest: findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
ok 61 - findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
  ---
  duration_ms: 0.184602
  ...
# Subtest: todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
ok 62 - todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
  ---
  duration_ms: 1.441612
  ...
# Subtest: todayDailyPath honors a custom Daily Notes format and an empty folder
ok 63 - todayDailyPath honors a custom Daily Notes format and an empty folder
  ---
  duration_ms: 0.221623
  ...
# Subtest: formatDailyDate resolves bracketed literal text alongside date tokens
ok 64 - formatDailyDate resolves bracketed literal text alongside date tokens
  ---
  duration_ms: 0.113216
  ...
# Subtest: getDailyNotesOptions reads the daily-notes core plugin's configured options
ok 65 - getDailyNotesOptions reads the daily-notes core plugin's configured options
  ---
  duration_ms: 0.614543
  ...
# Subtest: computeFencedLineFlags marks opening and closing fence lines and everything between
ok 66 - computeFencedLineFlags marks opening and closing fence lines and everything between
  ---
  duration_ms: 0.233556
  ...
# Subtest: selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
ok 67 - selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
  ---
  duration_ms: 0.714063
  ...
# Subtest: selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
ok 68 - selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
  ---
  duration_ms: 0.449749
  ...
# Subtest: selectPomodoroInsertionTarget rejects more than one open timed entry
ok 69 - selectPomodoroInsertionTarget rejects more than one open timed entry
  ---
  duration_ms: 0.199271
  ...
# Subtest: selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
ok 70 - selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
  ---
  duration_ms: 0.18313
  ...
# Subtest: findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
ok 71 - findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
  ---
  duration_ms: 0.173461
  ...
# Subtest: planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
ok 72 - planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
  ---
  duration_ms: 1.111832
  ...
# Subtest: planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
ok 73 - planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
  ---
  duration_ms: 1.432524
  ...
# Subtest: planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
ok 74 - planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
  ---
  duration_ms: 0.21984
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
ok 75 - planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
  ---
  duration_ms: 0.536373
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
ok 76 - planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
  ---
  duration_ms: 0.483572
  ...
# Subtest: planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
ok 77 - planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
  ---
  duration_ms: 0.328847
  ...
# Subtest: planPomodoroLinkInsertion inserts before the separator preceding later content
ok 78 - planPomodoroLinkInsertion inserts before the separator preceding later content
  ---
  duration_ms: 0.2563
  ...
# Subtest: planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
ok 79 - planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
  ---
  duration_ms: 0.298219
  ...
# Subtest: planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
ok 80 - planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
  ---
  duration_ms: 0.342704
  ...
# Subtest: existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
ok 81 - existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
  ---
  duration_ms: 2.973886
  ...
# Subtest: same-note Pomodoro link runtime composes the task update with adjacent insertion
ok 82 - same-note Pomodoro link runtime composes the task update with adjacent insertion
  ---
  duration_ms: 1.125889
  ...
# Subtest: new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
ok 83 - new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
  ---
  duration_ms: 0.589004
  ...
# Subtest: planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
ok 84 - planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
  ---
  duration_ms: 0.289623
  ...
# Subtest: all-open cleanup removes current and future links while preserving history and unresolved links
ok 85 - all-open cleanup removes current and future links while preserving history and unresolved links
  ---
  duration_ms: 0.842478
  ...
# Subtest: all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
ok 86 - all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
  ---
  duration_ms: 1.079951
  ...
# Subtest: all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
ok 87 - all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
  ---
  duration_ms: 0.218868
  ...
# Subtest: all-open cleanup treats missing section, no open entries, and no matches as no-op successes
ok 88 - all-open cleanup treats missing section, no open entries, and no matches as no-op successes
  ---
  duration_ms: 0.178521
  ...
# Subtest: composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
ok 89 - composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
  ---
  duration_ms: 0.265626
  ...
# Subtest: pomodoro link picker choices normalize to existing/new or null
ok 90 - pomodoro link picker choices normalize to existing/new or null
  ---
  duration_ms: 1.29947
  ...
# Subtest: pomodoroLinkPicker api never rejects and validates choices
ok 91 - pomodoroLinkPicker api never rejects and validates choices
  ---
  duration_ms: 0.389072
  ...
# Subtest: destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
ok 92 - destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
  ---
  duration_ms: 0.825816
  ...
# Subtest: destination pick with a section releases its guards when the modal cannot open
ok 93 - destination pick with a section releases its guards when the modal cannot open
  ---
  duration_ms: 1.663675
  ...
# Subtest: plugin lifecycle installs the api and drops it on unload
ok 94 - plugin lifecycle installs the api and drops it on unload
  ---
  duration_ms: 0.331353
  ...
# Subtest: Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
ok 95 - Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
  ---
  duration_ms: 2.412434
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor requires a single cursor
ok 96 - resolvePomodoroLinkTaskFromEditor requires a single cursor
  ---
  duration_ms: 0.326032
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
ok 97 - resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
  ---
  duration_ms: 0.432726
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
ok 98 - resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
  ---
  duration_ms: 0.498501
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
ok 99 - resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
  ---
  duration_ms: 0.507678
  ...
# Subtest: blocked-link consumption reports dependency reasons before the project date
ok 100 - blocked-link consumption reports dependency reasons before the project date
  ---
  duration_ms: 2.428074
  ...
# Subtest: Pomodoro link checks do not read other notes for a non-Blocked task
ok 101 - Pomodoro link checks do not read other notes for a non-Blocked task
  ---
  duration_ms: 0.285625
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
ok 102 - resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
  ---
  duration_ms: 0.362712
  ...
# Subtest: task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
ok 103 - task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
  ---
  duration_ms: 6.04105
  ...
# Subtest: task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
ok 104 - task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
  ---
  duration_ms: 1.847947
  ...
# Subtest: task-mode toggle: linked only under a completed Pomodoro links again
ok 105 - task-mode toggle: linked only under a completed Pomodoro links again
  ---
  duration_ms: 0.780129
  ...
# Subtest: task-mode toggle: a task without a block ID is never linked and prompts for one
ok 106 - task-mode toggle: a task without a block ID is never linked and prompts for one
  ---
  duration_ms: 0.411866
  ...
# Subtest: existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
ok 107 - existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
  ---
  duration_ms: 1.092224
  ...
# Subtest: forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
ok 108 - forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
  ---
  duration_ms: 0.572302
  ...
# Subtest: new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
ok 109 - new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
  ---
  duration_ms: 0.519411
  ...
# Subtest: submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
ok 110 - submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
  ---
  duration_ms: 0.143864
  ...
# Subtest: submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
ok 111 - submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
  ---
  duration_ms: 0.192447
  ...
# Subtest: same-note Pomodoro link runtime: task and ledger edits merge into one transaction
ok 112 - same-note Pomodoro link runtime: task and ledger edits merge into one transaction
  ---
  duration_ms: 1.276305
  ...
# Subtest: linking an already-linked Ready task raises it to Next without duplicating the link
ok 113 - linking an already-linked Ready task raises it to Next without duplicating the link
  ---
  duration_ms: 0.549919
  ...
# Subtest: Next task without a block ID preflights the picker before prompting
ok 114 - Next task without a block ID preflights the picker before prompting
  ---
  duration_ms: 0.543337
  ...
# Subtest: Pomodoro link stops before any mutation when today's daily note is missing
ok 115 - Pomodoro link stops before any mutation when today's daily note is missing
  ---
  duration_ms: 0.19397
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
ok 116 - Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
  ---
  duration_ms: 0.561873
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
ok 117 - Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
  ---
  duration_ms: 0.358564
  ...
# Subtest: Pomodoro link aborts without any write when the task line changed since it was selected
ok 118 - Pomodoro link aborts without any write when the task line changed since it was selected
  ---
  duration_ms: 0.167831
  ...
# Subtest: Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
ok 119 - Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
  ---
  duration_ms: 0.64464
  ...
# Subtest: canceling the Pomodoro block-ID modal leaves the note untouched
ok 120 - canceling the Pomodoro block-ID modal leaves the note untouched
  ---
  duration_ms: 0.16216
  ...
# Subtest: review-walk: existing-ID link hands its Linked notice to continue with no separate notice
ok 121 - review-walk: existing-ID link hands its Linked notice to continue with no separate notice
  ---
  duration_ms: 0.795999
  ...
# Subtest: review-walk: prompted-ID link continues after submit
ok 122 - review-walk: prompted-ID link continues after submit
  ---
  duration_ms: 0.952087
  ...
# Subtest: review-walk: prompt cancel settles with null
ok 123 - review-walk: prompt cancel settles with null
  ---
  duration_ms: 0.143204
  ...
# Subtest: review-walk: BUSY swallows the key with no write
ok 124 - review-walk: BUSY swallows the key with no write
  ---
  duration_ms: 0.327415
  ...
# Subtest: review-walk: failed link keeps its notice and settles with null
ok 125 - review-walk: failed link keeps its notice and settles with null
  ---
  duration_ms: 0.211183
  ...
# Subtest: review-walk: partial link keeps its notice and never continues with an outcome
ok 126 - review-walk: partial link keeps its notice and never continues with an outcome
  ---
  duration_ms: 0.741605
  ...
# Subtest: inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
ok 127 - inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
  ---
  duration_ms: 0.213127
  ...
# Subtest: inbox-route: non-inbox notes and task-link mode never prompt
ok 128 - inbox-route: non-inbox notes and task-link mode never prompt
  ---
  duration_ms: 0.622338
  ...
# Subtest: inbox-route: cancel writes nothing and settles once
ok 129 - inbox-route: cancel writes nothing and settles once
  ---
  duration_ms: 0.461871
  ...
# Subtest: inbox-route: stay matches today
ok 130 - inbox-route: stay matches today
  ---
  duration_ms: 1.386536
  ...
# Subtest: inbox-route: move links, then moves, with one composed toast and a route continue
ok 131 - inbox-route: move links, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.563515
  ...
# Subtest: inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
ok 132 - inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
  ---
  duration_ms: 0.6603
  ...
# Subtest: inbox-route: a move failure gives the partial notice plus a link-today continue
ok 133 - inbox-route: a move failure gives the partial notice plus a link-today continue
  ---
  duration_ms: 0.379655
  ...
# Subtest: review-walk: no nav or nav v2 keeps today's notices
ok 134 - review-walk: no nav or nav v2 keeps today's notices
  ---
  duration_ms: 0.821407
  ...
# Subtest: inbox-route: source drift during route prompt refuses without writes
ok 135 - inbox-route: source drift during route prompt refuses without writes
  ---
  duration_ms: 0.30417
  ...
# Subtest: inbox-route: block-ID route cancel returns sentinel and settles null once
ok 136 - inbox-route: block-ID route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.287709
  ...
# Subtest: inbox-route: link no-op with move never commits
ok 137 - inbox-route: link no-op with move never commits
  ---
  duration_ms: 0.189151
  ...
# Subtest: picker opens only on the link direction, never on unlink
ok 138 - picker opens only on the link direction, never on unlink
  ---
  duration_ms: 8.324878
  ...
# Subtest: picker never opens in task-link mode
ok 139 - picker never opens in task-link mode
  ---
  duration_ms: 3.008671
  ...
# Subtest: Depends-On refusals never open the picker
ok 140 - Depends-On refusals never open the picker
  ---
  duration_ms: 0.837518
  ...
# Subtest: preflight refusals open nothing
ok 141 - preflight refusals open nothing
  ---
  duration_ms: 0.4926
  ...
# Subtest: picking a non-default entry links there
ok 142 - picking a non-default entry links there
  ---
  duration_ms: 1.186384
  ...
# Subtest: cancel writes nothing with no Notice and settles the walk null
ok 143 - cancel writes nothing with no Notice and settles the walk null
  ---
  duration_ms: 0.589475
  ...
# Subtest: a no-ID task gets picker, then the block-ID prompt with the target carried
ok 144 - a no-ID task gets picker, then the block-ID prompt with the target carried
  ---
  duration_ms: 0.841827
  ...
# Subtest: inbox order is picker, then route, then write
ok 145 - inbox order is picker, then route, then write
  ---
  duration_ms: 0.689546
  ...
# Subtest: a review-walk landing continues with link-today and the new text
ok 146 - a review-walk landing continues with link-today and the new text
  ---
  duration_ms: 0.849291
  ...
# Subtest: an all-closed ledger creates a new entry after the last completed block
ok 147 - an all-closed ledger creates a new entry after the last completed block
  ---
  duration_ms: 1.676379
  ...
# Subtest: several running entries allow an explicit pick
ok 148 - several running entries allow an explicit pick
  ---
  duration_ms: 0.704024
  ...
# Subtest: a target that changed before commit refuses with no writes
ok 149 - a target that changed before commit refuses with no writes
  ---
  duration_ms: 0.455289
  ...
# Subtest: a target that closed before commit refuses with no writes
ok 150 - a target that closed before commit refuses with no writes
  ---
  duration_ms: 0.360688
  ...
# Subtest: the task note being the daily note uses one editor transaction
ok 151 - the task note being the daily note uses one editor transaction
  ---
  duration_ms: 0.572983
  ...
# Subtest: promptOpen blocks re-entry while the picker is open
ok 152 - promptOpen blocks re-entry while the picker is open
  ---
  duration_ms: 9.021327
  ...
# Subtest: header shows title, subtitle, lane chip per status, and block-ID chip
ok 153 - header shows title, subtitle, lane chip per status, and block-ID chip
  ---
  duration_ms: 7.993155
  ...
# Subtest: rows render in document order with the default selected
ok 154 - rows render in document order with the default selected
  ---
  duration_ms: 1.097955
  ...
# Subtest: running row shows progress fraction and minutes-left meta
ok 155 - running row shows progress fraction and minutes-left meta
  ---
  duration_ms: 0.975682
  ...
# Subtest: unnamed entries render muted italic
ok 156 - unnamed entries render muted italic
  ---
  duration_ms: 0.43466
  ...
# Subtest: filtering ranks, highlights, and clearing restores the default
ok 157 - filtering ranks, highlights, and clearing restores the default
  ---
  duration_ms: 0.999478
  ...
# Subtest: create row meta, divider, and theme badge
ok 158 - create row meta, divider, and theme badge
  ---
  duration_ms: 1.491005
  ...
# Subtest: exact open names suppress the create row; prefix matches keep it
ok 159 - exact open names suppress the create row; prefix matches keep it
  ---
  duration_ms: 1.701217
  ...
# Subtest: theme badge turns red over cap; a throwing budget hides the detail
ok 160 - theme badge turns red over cap; a throwing budget hides the detail
  ---
  duration_ms: 0.987094
  ...
# Subtest: invalid rows explain the grammar and are inert on Enter
ok 161 - invalid rows explain the grammar and are inert on Enter
  ---
  duration_ms: 9.027356
  ...
# Subtest: multiple running entries show the banner, no pills, and block creation
ok 162 - multiple running entries show the banner, no pills, and block creation
  ---
  duration_ms: 1.271927
  ...
# Subtest: navigation wraps and skips non-selectable rows
ok 163 - navigation wraps and skips non-selectable rows
  ---
  duration_ms: 1.276256
  ...
# Subtest: empty state invites planning a Pomodoro
ok 164 - empty state invites planning a Pomodoro
  ---
  duration_ms: 0.27228
  ...
# Subtest: footer hints and plan meter
ok 165 - footer hints and plan meter
  ---
  duration_ms: 1.113145
  ...
# Subtest: Enter chooses the selected row; click chooses that row
ok 166 - Enter chooses the selected row; click chooses that row
  ---
  duration_ms: 0.787413
  ...
# Subtest: Shift+Enter creates; an exact open name links there instead
ok 167 - Shift+Enter creates; an exact open name links there instead
  ---
  duration_ms: 0.945885
  ...
# Subtest: Ctrl+Shift+Enter commits exactly like Enter
ok 168 - Ctrl+Shift+Enter commits exactly like Enter
  ---
  duration_ms: 1.705625
  ...
# Subtest: Escape and Ctrl+[ cancel with no choice; settle-once holds
ok 169 - Escape and Ctrl+[ cancel with no choice; settle-once holds
  ---
  duration_ms: 0.616556
  ...
# Subtest: canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
ok 170 - canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
  ---
  duration_ms: 2.360946
  ...
# Subtest: canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
ok 171 - canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
  ---
  duration_ms: 0.388752
  ...
# Subtest: pomodoroLinkSelectorSlug mirrors capture slugs
ok 172 - pomodoroLinkSelectorSlug mirrors capture slugs
  ---
  duration_ms: 0.318317
  ...
# Subtest: parsePomodoroEntryParts reads canonical and legacy entry lines
ok 173 - parsePomodoroEntryParts reads canonical and legacy entry lines
  ---
  duration_ms: 2.279621
  ...
# Subtest: collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
ok 174 - collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
  ---
  duration_ms: 2.235226
  ...
# Subtest: collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
ok 175 - collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
  ---
  duration_ms: 1.460057
  ...
# Subtest: collectPomodoroLinkEntries counts links but excludes struck references
ok 176 - collectPomodoroLinkEntries counts links but excludes struck references
  ---
  duration_ms: 0.638118
  ...
# Subtest: collectPomodoroLinkEntries falls back to range text and position titles
ok 177 - collectPomodoroLinkEntries falls back to range text and position titles
  ---
  duration_ms: 0.381047
  ...
# Subtest: pomodoroRunProgress reports fractions, overtime, and midnight wrap
ok 178 - pomodoroRunProgress reports fractions, overtime, and midnight wrap
  ---
  duration_ms: 0.633479
  ...
# Subtest: buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
ok 179 - buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
  ---
  duration_ms: 1.06425
  ...
# Subtest: buildPomodoroLinkPickerRows keeps the create row for prefix matches
ok 180 - buildPomodoroLinkPickerRows keeps the create row for prefix matches
  ---
  duration_ms: 0.411385
  ...
# Subtest: buildPomodoroLinkPickerRows marks completed-only names as again
ok 181 - buildPomodoroLinkPickerRows marks completed-only names as again
  ---
  duration_ms: 0.264104
  ...
# Subtest: buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
ok 182 - buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
  ---
  duration_ms: 0.554308
  ...
# Subtest: buildPomodoroLinkPickerRows matches times, positions, and block IDs
ok 183 - buildPomodoroLinkPickerRows matches times, positions, and block IDs
  ---
  duration_ms: 0.70729
  ...
# Subtest: resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
ok 184 - resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
  ---
  duration_ms: 0.407487
  ...
# Subtest: defaultPomodoroLinkChoice returns the default entry or null
ok 185 - defaultPomodoroLinkChoice returns the default entry or null
  ---
  duration_ms: 0.226973
  ...
# Subtest: planExplicitPomodoroLinkInsertion links under a chosen existing entry
ok 186 - planExplicitPomodoroLinkInsertion links under a chosen existing entry
  ---
  duration_ms: 1.339887
  ...
# Subtest: planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
ok 187 - planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
  ---
  duration_ms: 0.338707
  ...
# Subtest: planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
ok 188 - planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
  ---
  duration_ms: 1.563103
  ...
# Subtest: planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
ok 189 - planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
  ---
  duration_ms: 0.520984
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after the running entry
ok 190 - planExplicitPomodoroLinkInsertion creates after the running entry
  ---
  duration_ms: 0.865362
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
ok 191 - planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
  ---
  duration_ms: 0.928392
  ...
# Subtest: planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
ok 192 - planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
  ---
  duration_ms: 0.334509
  ...
# Subtest: planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
ok 193 - planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
  ---
  duration_ms: 0.388842
  ...
# Subtest: planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
ok 194 - planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
  ---
  duration_ms: 0.536815
  ...
# Subtest: buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
ok 195 - buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
  ---
  duration_ms: 0.226041
  ...
# Subtest: buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
ok 196 - buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
  ---
  duration_ms: 0.200042
  ...
# Subtest: planExplicitPomodoroLinkInsertion matches mixed-case raced open names
ok 197 - planExplicitPomodoroLinkInsertion matches mixed-case raced open names
  ---
  duration_ms: 0.235459
  ...
# Subtest: buildPomodoroLinkPickerRows bounds \#N position matches
ok 198 - buildPomodoroLinkPickerRows bounds \#N position matches
  ---
  duration_ms: 0.469386
  ...
# Subtest: planPomodoroLinkInsertion without a target keeps today's behavior and shape
ok 199 - planPomodoroLinkInsertion without a target keeps today's behavior and shape
  ---
  duration_ms: 0.516636
  ...
# Subtest: direct unlink without a daily note keeps the Next lane and reports it
ok 200 - direct unlink without a daily note keeps the Next lane and reports it
  ---
  duration_ms: 2.294639
  ...
# Subtest: In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
ok 201 - In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
  ---
  duration_ms: 0.438707
  ...
# Subtest: In Progress unlink with a summary keeps the lane and creates a Work Log
ok 202 - In Progress unlink with a summary keeps the lane and creates a Work Log
  ---
  duration_ms: 1.13727
  ...
# Subtest: In Progress unlink revalidates task text and block-ID uniqueness at confirmation
ok 203 - In Progress unlink revalidates task text and block-ID uniqueness at confirmation
  ---
  duration_ms: 1.176134
  ...
# Subtest: Next task unlink removes current and future links and keeps the Next lane
ok 204 - Next task unlink removes current and future links and keeps the Next lane
  ---
  duration_ms: 3.550115
  ...
# Subtest: In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
ok 205 - In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
  ---
  duration_ms: 0.733239
  ...
# Subtest: same-note Next unlink merges the Work Log and all-open cleanup in the active editor
ok 206 - same-note Next unlink merges the Work Log and all-open cleanup in the active editor
  ---
  duration_ms: 0.962958
  ...
# Subtest: same-note In Progress unlink merges cleanup and Work Log in the active editor
ok 207 - same-note In Progress unlink merges cleanup and Work Log in the active editor
  ---
  duration_ms: 0.580869
  ...
# Subtest: Next unlink stops before any write when daily cleanup write is stale
ok 208 - Next unlink stops before any write when daily cleanup write is stale
  ---
  duration_ms: 0.758067
  ...
# Subtest: Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
ok 209 - Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
  ---
  duration_ms: 0.910678
  ...
# Subtest: In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
ok 210 - In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
  ---
  duration_ms: 0.662594
  ...
# Subtest: review-walk: unlink settles with null and keeps its notice
ok 211 - review-walk: unlink settles with null and keeps its notice
  ---
  duration_ms: 1.191884
  ...
# Subtest: inbox-route: unlink cancel writes nothing
ok 212 - inbox-route: unlink cancel writes nothing
  ---
  duration_ms: 0.328827
  ...
# Subtest: inbox-route: unlink stay matches today and never commits
ok 213 - inbox-route: unlink stay matches today and never commits
  ---
  duration_ms: 0.546032
  ...
# Subtest: inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
ok 214 - inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.629832
  ...
# Subtest: inbox-route: In Progress unlink with a Work summary routes
ok 215 - inbox-route: In Progress unlink with a Work summary routes
  ---
  duration_ms: 0.57121
  ...
# Subtest: inbox-route: unlink move failure gives the partial notice and stays
ok 216 - inbox-route: unlink move failure gives the partial notice and stays
  ---
  duration_ms: 0.28831
  ...
# Subtest: inbox-route: non-inbox unlink never prompts
ok 217 - inbox-route: non-inbox unlink never prompts
  ---
  duration_ms: 0.304912
  ...
# Subtest: review-walk: Work-summary unlink path retains origin until submit
ok 218 - review-walk: Work-summary unlink path retains origin until submit
  ---
  duration_ms: 0.299652
  ...
# Subtest: inbox-route: unlink source drift during route prompt refuses without writes
ok 219 - inbox-route: unlink source drift during route prompt refuses without writes
  ---
  duration_ms: 0.226302
  ...
# Subtest: inbox-route: Work-summary route cancel returns sentinel and settles null once
ok 220 - inbox-route: Work-summary route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.253755
  ...
# Subtest: inbox-route: unlink no-op with move never commits
ok 221 - inbox-route: unlink no-op with move never commits
  ---
  duration_ms: 0.210432
  ...
# Subtest: same-note unlink maps a task below removed entries through Work-summary inserts
ok 222 - same-note unlink maps a task below removed entries through Work-summary inserts
  ---
  duration_ms: 0.517929
  ...
# Subtest: direct-add seeds from the task headline, not non-task blocks
ok 223 - direct-add seeds from the task headline, not non-task blocks
  ---
  duration_ms: 3.597015
  ...
# Subtest: link-task-complete seeds from the target, prefers open buffers
ok 224 - link-task-complete seeds from the target, prefers open buffers
  ---
  duration_ms: 1.197155
  ...
# Subtest: link-task-complete reports stale and unreadable targets
ok 225 - link-task-complete reports stale and unreadable targets
  ---
  duration_ms: 0.390055
  ...
# Subtest: pomodoro link seeds after the choice from the cursor task
ok 226 - pomodoro link seeds after the choice from the cursor task
  ---
  duration_ms: 0.36191
  ...
# Subtest: marker rename suggests from the unique task, never hiding ambiguity
ok 227 - marker rename suggests from the unique task, never hiding ambiguity
  ---
  duration_ms: 0.69716
  ...
# Subtest: modal seeds the value, selects once, and never overwrites typing
ok 228 - modal seeds the value, selects once, and never overwrites typing
  ---
  duration_ms: 1.508188
  ...
# Subtest: modal disables Save while loading and survives close/reopen
ok 229 - modal disables Save while loading and survives close/reopen
  ---
  duration_ms: 2.540107
  ...
# Subtest: submit revalidates: occupied IDs and stale tasks fail editable
ok 230 - submit revalidates: occupied IDs and stale tasks fail editable
  ---
  duration_ms: 0.676551
  ...
# Subtest: cancelling writes no ID and explicit renames keep the current ID
ok 231 - cancelling writes no ID and explicit renames keep the current ID
  ---
  duration_ms: 0.88544
  ...
# Subtest: the task picker drops the paired \#ref and prefixes the book
ok 232 - the task picker drops the paired \#ref and prefixes the book
  ---
  duration_ms: 2.517825
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 233 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.321493
  ...
# Subtest: block-id-prompt LK1–LK19 recognises only relation line shapes
ok 234 - block-id-prompt LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 1.337562
  ...
# Subtest: block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
ok 235 - block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
  ---
  duration_ms: 1.001952
  ...
# Subtest: block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
ok 236 - block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
  ---
  duration_ms: 1.389632
  ...
# Subtest: calendar date parsing rejects malformed width and impossible dates
ok 237 - calendar date parsing rejects malformed width and impossible dates
  ---
  duration_ms: 1.673584
  ...
# Subtest: future scheduled field detection respects the yesterday/today/tomorrow boundary
ok 238 - future scheduled field detection respects the yesterday/today/tomorrow boundary
  ---
  duration_ms: 1.386797
  ...
# Subtest: scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
ok 239 - scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
  ---
  duration_ms: 0.18349
  ...
# Subtest: planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
ok 240 - planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
  ---
  duration_ms: 0.993146
  ...
# Subtest: planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
ok 241 - planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
  ---
  duration_ms: 0.204029
  ...
# Subtest: planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
ok 242 - planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
  ---
  duration_ms: 0.164073
  ...
# Subtest: planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
ok 243 - planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
  ---
  duration_ms: 0.164894
  ...
# Subtest: planTargetTaskUpdate leaves today and past schedules untouched
ok 244 - planTargetTaskUpdate leaves today and past schedules untouched
  ---
  duration_ms: 0.295534
  ...
# Subtest: planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
ok 245 - planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
  ---
  duration_ms: 0.34577
  ...
# Subtest: two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
ok 246 - two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
  ---
  duration_ms: 0.451642
  ...
# Subtest: a malformed single scheduled field is never treated as future
ok 247 - a malformed single scheduled field is never treated as future
  ---
  duration_ms: 0.182849
  ...
# Subtest: an ambiguous scheduled field does not block the legacy Ready promotion
ok 248 - an ambiguous scheduled field does not block the legacy Ready promotion
  ---
  duration_ms: 0.190253
  ...
# Subtest: planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
ok 249 - planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
  ---
  duration_ms: 0.142782
  ...
# Subtest: Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
ok 250 - Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
  ---
  duration_ms: 0.48204
  ...
# Subtest: Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
ok 251 - Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
  ---
  duration_ms: 0.154565
  ...
# Subtest: planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
ok 252 - planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
  ---
  duration_ms: 0.25712
  ...
# Subtest: planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
ok 253 - planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
  ---
  duration_ms: 0.145047
  ...
# Subtest: planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
ok 254 - planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.148573
  ...
# Subtest: planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
ok 255 - planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
  ---
  duration_ms: 0.160376
  ...
# Subtest: planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
ok 256 - planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
  ---
  duration_ms: 0.152542
  ...
# Subtest: planTargetTaskUpdate preserves a trailing newline when one was already present
ok 257 - planTargetTaskUpdate preserves a trailing newline when one was already present
  ---
  duration_ms: 0.144506
  ...
# Subtest: planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
ok 258 - planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
  ---
  duration_ms: 0.125499
  ...
# Subtest: planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
ok 259 - planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
  ---
  duration_ms: 0.175275
  ...
# Subtest: planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
ok 260 - planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
  ---
  duration_ms: 0.12594
  ...
# Subtest: existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
ok 261 - existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
  ---
  duration_ms: 3.159589
  ...
# Subtest: new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
ok 262 - new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
  ---
  duration_ms: 0.745543
  ...
# Subtest: activation runtime aborts without any write when the target preimage goes stale
ok 263 - activation runtime aborts without any write when the target preimage goes stale
  ---
  duration_ms: 0.410374
  ...
# Subtest: same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
ok 264 - same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
  ---
  duration_ms: 2.356247
  ...
# Subtest: same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
ok 265 - same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
  ---
  duration_ms: 0.624071
  ...
# Subtest: a source marker edited after a successful existing-ID target write reports an accurate partial notice
ok 266 - a source marker edited after a successful existing-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.481368
  ...
# Subtest: a source marker edited after a successful new-ID target write reports an accurate partial notice
ok 267 - a source marker edited after a successful new-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.492149
  ...
# Subtest: planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
ok 268 - planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
  ---
  duration_ms: 0.166758
  ...
# Subtest: planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
ok 269 - planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
  ---
  duration_ms: 0.119508
  ...
# Subtest: planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
ok 270 - planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
  ---
  duration_ms: 0.127583
  ...
# Subtest: planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
ok 271 - planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.112906
  ...
# Subtest: direct Task Links raise ^prj while never pulling its date forward
ok 272 - direct Task Links raise ^prj while never pulling its date forward
  ---
  duration_ms: 0.134928
  ...
# Subtest: task-link selection: one link is selectable from any column, several are chosen by cursor
ok 273 - task-link selection: one link is selectable from any column, several are chosen by cursor
  ---
  duration_ms: 3.670334
  ...
# Subtest: task-link selection ignores picker/rename markers, plain links, and Markdown-style links
ok 274 - task-link selection ignores picker/rename markers, plain links, and Markdown-style links
  ---
  duration_ms: 0.320281
  ...
# Subtest: dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
ok 275 - dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
  ---
  duration_ms: 0.667794
  ...
# Subtest: inline Task Link deletion removes the token with its decoration and collapses whitespace
ok 276 - inline Task Link deletion removes the token with its decoration and collapses whitespace
  ---
  duration_ms: 0.669928
  ...
# Subtest: dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
ok 277 - dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
  ---
  duration_ms: 0.918493
  ...
# Subtest: mergeCoveringEdits keeps the covering edit and the earlier of identical edits
ok 278 - mergeCoveringEdits keeps the covering edit and the earlier of identical edits
  ---
  duration_ms: 0.219118
  ...
# Subtest: dependency transclusion detection needs an embedded sole-content child of a \#task line
ok 279 - dependency transclusion detection needs an embedded sole-content child of a \#task line
  ---
  duration_ms: 0.463695
  ...
# Subtest: Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
ok 280 - Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
  ---
  duration_ms: 4.903479
  ...
# Subtest: Task Link on a Next target works from an embedded aliased link outside any Pomodoro
ok 281 - Task Link on a Next target works from an embedded aliased link outside any Pomodoro
  ---
  duration_ms: 1.319237
  ...
# Subtest: same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
ok 282 - same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
  ---
  duration_ms: 1.209758
  ...
# Subtest: same-note Task Link deletion clamps the restored cursor to the shortened note
ok 283 - same-note Task Link deletion clamps the restored cursor to the shortened note
  ---
  duration_ms: 0.588974
  ...
# Subtest: a cleanup subtree that covers a nested selected link wins and links are not double counted
ok 284 - a cleanup subtree that covers a nested selected link wins and links are not double counted
  ---
  duration_ms: 0.821608
  ...
# Subtest: same-note Task Link in a closed entry deletes the closed entry it empties
ok 285 - same-note Task Link in a closed entry deletes the closed entry it empties
  ---
  duration_ms: 0.68125
  ...
# Subtest: Task Link in another day's note deletes the emptied entry there and in today's note
ok 286 - Task Link in another day's note deletes the emptied entry there and in today's note
  ---
  duration_ms: 0.586529
  ...
# Subtest: Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
ok 287 - Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
  ---
  duration_ms: 1.347432
  ...
# Subtest: Task Link on an In Progress target with a blank summary logs nothing
ok 288 - Task Link on an In Progress target with a blank summary logs nothing
  ---
  duration_ms: 0.731877
  ...
# Subtest: canceling the In Progress Task Link prompt leaves everything untouched
ok 289 - canceling the In Progress Task Link prompt leaves everything untouched
  ---
  duration_ms: 0.303689
  ...
# Subtest: canceling the In Progress unlink prompt in task mode leaves everything untouched
ok 290 - canceling the In Progress unlink prompt in task mode leaves everything untouched
  ---
  duration_ms: 0.545701
  ...
# Subtest: In Progress Task Link submit revalidates the link line and the target task
ok 291 - In Progress Task Link submit revalidates the link line and the target task
  ---
  duration_ms: 0.570399
  ...
# Subtest: Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
ok 292 - Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
  ---
  duration_ms: 0.636395
  ...
# Subtest: Task Link on a Done or Cancelled target is refused without edits
ok 293 - Task Link on a Done or Cancelled target is refused without edits
  ---
  duration_ms: 0.38263
  ...
# Subtest: Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
ok 294 - Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
  ---
  duration_ms: 0.849221
  ...
# Subtest: precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
ok 295 - precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
  ---
  duration_ms: 1.803702
  ...
# Subtest: Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
ok 296 - Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
  ---
  duration_ms: 0.443917
  ...
# Subtest: Task Link that is a sub-task dependency transclusion is refused without edits
ok 297 - Task Link that is a sub-task dependency transclusion is refused without edits
  ---
  duration_ms: 0.311714
  ...
# Subtest: Task Link partial failure after the daily write is retryable
ok 298 - Task Link partial failure after the daily write is retryable
  ---
  duration_ms: 2.257638
  ...
# Subtest: Task Link stops before any write when the target note changes after planning
ok 299 - Task Link stops before any write when the target note changes after planning
  ---
  duration_ms: 0.586359
  ...
# Subtest: Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
ok 300 - Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
  ---
  duration_ms: 0.460789
  ...
# Subtest: Task Link subtree deletion removes a nested target task without any status write
ok 301 - Task Link subtree deletion removes a nested target task without any status write
  ---
  duration_ms: 0.306064
  ...
# Subtest: whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
ok 302 - whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
  ---
  duration_ms: 0.843169
  ...
# Subtest: selected-link deletion maps a cursor inside a removed entry to its former start
ok 303 - selected-link deletion maps a cursor inside a removed entry to its former start
  ---
  duration_ms: 0.499132
  ...
# Subtest: work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
ok 304 - work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
  ---
  duration_ms: 1.440098
  ...
# Subtest: work log date helpers use local calendar components
ok 305 - work log date helpers use local calendar components
  ---
  duration_ms: 0.249636
  ...
# Subtest: planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
ok 306 - planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
  ---
  duration_ms: 0.658486
  ...
# Subtest: planWorkLogInsertion inherits an existing space-indented child prefix
ok 307 - planWorkLogInsertion inherits an existing space-indented child prefix
  ---
  duration_ms: 0.615114
  ...
# Subtest: planWorkLogInsertion inherits an existing tab-indented child prefix
ok 308 - planWorkLogInsertion inherits an existing tab-indented child prefix
  ---
  duration_ms: 0.286307
  ...
# Subtest: planWorkLogInsertion prepends newest-first entries into existing marker spellings
ok 309 - planWorkLogInsertion prepends newest-first entries into existing marker spellings
  ---
  duration_ms: 0.512498
  ...
# Subtest: planWorkLogInsertion ignores nested child-task markers and preserves CRLF
ok 310 - planWorkLogInsertion ignores nested child-task markers and preserves CRLF
  ---
  duration_ms: 0.354106
  ...
# Subtest: planWorkLogInsertion treats blank summaries as no-op structural edits
ok 311 - planWorkLogInsertion treats blank summaries as no-op structural edits
  ---
  duration_ms: 0.142331
  ...
# Subtest: the Open-reset planner is removed: unlink plans only a Work Log insertion
ok 312 - the Open-reset planner is removed: unlink plans only a Work Log insertion
  ---
  duration_ms: 0.331121
  ...
# Subtest: unlink Work Log plan keeps the In Progress checkbox and appends one entry
ok 313 - unlink Work Log plan keeps the In Progress checkbox and appends one entry
  ---
  duration_ms: 0.401115
  ...
# Subtest: article detection accepts scalar and list frontmatter values
ok 314 - article detection accepts scalar and list frontmatter values
  ---
  duration_ms: 1.462382
  ...
# Subtest: bob resolution prefers its setting, then known install paths, then PATH
ok 315 - bob resolution prefers its setting, then known install paths, then PATH
  ---
  duration_ms: 0.769369
  ...
# Subtest: plan decoder accepts v1 and rejects a foreign schema version
ok 316 - plan decoder accepts v1 and rejects a foreign schema version
  ---
  duration_ms: 0.311324
  ...
# Subtest: bob stdin spawn passes the article contract and vault environment
ok 317 - bob stdin spawn passes the article contract and vault environment
  ---
  duration_ms: 2.778212
  ...
# Subtest: bob plan stdout decodes UTF-8 split across chunks
ok 318 - bob plan stdout decodes UTF-8 split across chunks
  ---
  duration_ms: 0.809595
  ...
# Subtest: early bob exit on stdin reports EPIPE as a run failure
ok 319 - early bob exit on stdin reports EPIPE as a run failure
  ---
  duration_ms: 0.679707
  ...
# Subtest: line hunks become minimal cursor-preserving changes
ok 320 - line hunks become minimal cursor-preserving changes
  ---
  duration_ms: 0.633078
  ...
# Subtest: insert, multi-line replace, and deletion hunks reproduce the formatted note
ok 321 - insert, multi-line replace, and deletion hunks reproduce the formatted note
  ---
  duration_ms: 3.211739
  ...
# Subtest: notice shows bob's text and at most two warning findings
ok 322 - notice shows bob's text and at most two warning findings
  ---
  duration_ms: 0.443196
  ...
# Subtest: inbound changes apply only when their target line still matches the preimage
ok 323 - inbound changes apply only when their target line still matches the preimage
  ---
  duration_ms: 0.697792
  ...
# Subtest: undo guard blocks a reformat until a fresh input or delete event
ok 324 - undo guard blocks a reformat until a fresh input or delete event
  ---
  duration_ms: 0.386187
  ...
# Subtest: leave formatting observes the undo guard before saving or reading
ok 325 - leave formatting observes the undo guard before saving or reading
  ---
  duration_ms: 0.279845
  ...
# Subtest: Convert shows bob's refusal on every invocation
ok 326 - Convert shows bob's refusal on every invocation
  ---
  duration_ms: 0.372
  ...
# Subtest: old bob's non-JSON article response gets one update notice per session
ok 327 - old bob's non-JSON article response gets one update notice per session
  ---
  duration_ms: 0.217114
  ...
# Subtest: format drops its response if the editor changed while bob was running
ok 328 - format drops its response if the editor changed while bob was running
  ---
  duration_ms: 0.405775
  ...
# Subtest: decoration ranges mark written section numbers from the outline
ok 329 - decoration ranges mark written section numbers from the outline
  ---
  duration_ms: 0.951356
  ...
# Subtest: a new outline rerenders each open Reading view once for that generation
ok 330 - a new outline rerenders each open Reading view once for that generation
  ---
  duration_ms: 0.459467
  ...
# Subtest: section at a given line uses the innermost outline range
ok 331 - section at a given line uses the innermost outline range
  ---
  duration_ms: 0.381037
  ...
# Subtest: stale-hint debounce and in-flight state machine
ok 332 - stale-hint debounce and in-flight state machine
  ---
  duration_ms: 0.345169
  ...
# Subtest: reading-view wrapping puts the leading number token in span.bob-secno
ok 333 - reading-view wrapping puts the leading number token in span.bob-secno
  ---
  duration_ms: 0.902062
  ...
# Subtest: applied plans remap outline lines onto the formatted buffer
ok 334 - applied plans remap outline lines onto the formatted buffer
  ---
  duration_ms: 0.188119
  ...
# Subtest: article styles scope the reading look under .bob-article
ok 335 - article styles scope the reading look under .bob-article
  ---
  duration_ms: 0.583634
  ...
# Subtest: look settings default to serif typeface and stale-number hints
ok 336 - look settings default to serif typeface and stale-number hints
  ---
  duration_ms: 0.153353
  ...
# Subtest: folds embed, struck, and plain legacy children into one canonical line
ok 337 - folds embed, struck, and plain legacy children into one canonical line
  ---
  duration_ms: 69.374574
  ...
# Subtest: legacy-label row links come first, then legacy children in order
ok 338 - legacy-label row links come first, then legacy children in order
  ---
  duration_ms: 1.741954
  ...
# Subtest: R2 adopts field-only open dependents; unadoptable ids stay warned
ok 339 - R2 adopts field-only open dependents; unadoptable ids stay warned
  ---
  duration_ms: 0.571952
  ...
# Subtest: closed dependents gain the line but keep the field untouched
ok 340 - closed dependents gain the line but keep the field untouched
  ---
  duration_ms: 0.96409
  ...
# Subtest: open dependents drop stale field ids and stamp targets missing [id::]
ok 341 - open dependents drop stale field ids and stamp targets missing [id::]
  ---
  duration_ms: 0.528038
  ...
# Subtest: unresolved links stay verbatim and keep field ids as breadcrumbs
ok 342 - unresolved links stay verbatim and keep field ids as breadcrumbs
  ---
  duration_ms: 0.499102
  ...
# Subtest: leaves \#^ref embeds, non-task parents, fences, and conflict children alone
ok 343 - leaves \#^ref embeds, non-task parents, fences, and conflict children alone
  ---
  duration_ms: 0.650892
  ...
# Subtest: malformed rows leave the whole dependent alone
ok 344 - malformed rows leave the whole dependent alone
  ---
  duration_ms: 0.476088
  ...
# Subtest: R9 deletes label-only rows and removes the open field
ok 345 - R9 deletes label-only rows and removes the open field
  ---
  duration_ms: 0.628069
  ...
# Subtest: cross-note links use the shortest unambiguous form
ok 346 - cross-note links use the shortest unambiguous form
  ---
  duration_ms: 0.685007
  ...
# Subtest: ambiguous basenames fall back to the full path
ok 347 - ambiguous basenames fall back to the full path
  ---
  duration_ms: 1.475967
  ...
# Subtest: duplicate ids are ambiguous and fatal for --write
ok 348 - duplicate ids are ambiguous and fatal for --write
  ---
  duration_ms: 0.272119
  ...
# Subtest: archive targets keep the done/ path and are never stamped
ok 349 - archive targets keep the done/ path and are never stamped
  ---
  duration_ms: 0.291156
  ...
# Subtest: self links stay on the line but are not projected
ok 350 - self links stay on the line but are not projected
  ---
  duration_ms: 0.31436
  ...
# Subtest: non-task targets stay on the line but are not projected
ok 351 - non-task targets stay on the line but are not projected
  ---
  duration_ms: 0.250368
  ...
# Subtest: preserves CRLF, missing final newline, and cancel-log position
ok 352 - preserves CRLF, missing final newline, and cancel-log position
  ---
  duration_ms: 0.352984
  ...
# Subtest: migration is idempotent
ok 353 - migration is idempotent
  ---
  duration_ms: 1.027311
  ...
# Subtest: parseArgs handles --vault, --write, --help, and rejects unknowns
ok 354 - parseArgs handles --vault, --write, --help, and rejects unknowns
  ---
  duration_ms: 0.530432
  ...
# Subtest: BOB_CLI_DIR wins over a sibling checkout and a cache
ok 355 - BOB_CLI_DIR wins over a sibling checkout and a cache
  ---
  duration_ms: 17.492444
  ...
# Subtest: sibling bob-cli is used when BOB_CLI_DIR is unset
ok 356 - sibling bob-cli is used when BOB_CLI_DIR is unset
  ---
  duration_ms: 15.710581
  ...
# Subtest: an invalid BOB_CLI_DIR does not fall through
ok 357 - an invalid BOB_CLI_DIR does not fall through
  ---
  duration_ms: 8.4779
  ...
# Subtest: cache clone is used when no user-owned checkout exists
ok 358 - cache clone is used when no user-owned checkout exists
  ---
  duration_ms: 19.894116
  ...
# Subtest: refreshing an existing cache keeps git chatter off stdout and forwards exact paths
ok 359 - refreshing an existing cache keeps git chatter off stdout and forwards exact paths
  ---
  duration_ms: 30.96851
  ...
# Subtest: a cache clone with a foreign origin fails before fetch or reset
ok 360 - a cache clone with a foreign origin fails before fetch or reset
  ---
  duration_ms: 19.956335
  ...
# Subtest: a justfile alone is rejected as an explicit bob-cli checkout
ok 361 - a justfile alone is rejected as an explicit bob-cli checkout
  ---
  duration_ms: 11.367544
  ...
# Subtest: just failures propagate
ok 362 - just failures propagate
  ---
  duration_ms: 14.921115
  ...
# Subtest: scans multiline, one-line, and guarded literal registrations
ok 363 - scans multiline, one-line, and guarded literal registrations
  ---
  duration_ms: 2.996398
  ...
# Subtest: scans an optional addCommand call
ok 364 - scans an optional addCommand call
  ---
  duration_ms: 0.327425
  ...
# Subtest: allows addCommand references only in a typeof guard
ok 365 - allows addCommand references only in a typeof guard
  ---
  duration_ms: 0.368573
  ...
# Subtest: rejects bind, call, and aliased addCommand references with source locations
ok 366 - rejects bind, call, and aliased addCommand references with source locations
  ---
  duration_ms: 0.655831
  ...
# Subtest: expands literal command data from a constant-array forEach across source files
ok 367 - expands literal command data from a constant-array forEach across source files
  ---
  duration_ms: 2.377057
  ...
# Subtest: balances nested callback syntax and ignores misleading comments, strings, templates, and regexes
ok 368 - balances nested callback syntax and ignores misleading comments, strings, templates, and regexes
  ---
  duration_ms: 0.643327
  ...
# Subtest: decodes escaped string metadata and literal default hotkeys
ok 369 - decodes escaped string metadata and literal default hotkeys
  ---
  duration_ms: 0.54482
  ...
# Subtest: returns no commands for a plugin without registrations
ok 370 - returns no commands for a plugin without registrations
  ---
  duration_ms: 0.268092
  ...
# Subtest: fails with source locations for dynamic metadata, hotkeys, and malformed tables
ok 371 - fails with source locations for dynamic metadata, hotkeys, and malformed tables
  ---
  duration_ms: 1.413517
  ...
# Subtest: fails duplicate command ids with both registration locations
ok 372 - fails duplicate command ids with both registration locations
  ---
  duration_ms: 0.735634
  ...
# Subtest: checks drift without writes, preserves prose, and generates deterministically
ok 373 - checks drift without writes, preserves prose, and generates deterministically
  ---
  duration_ms: 10.478878
  ...
# Subtest: code-span table cells preserve backslashes and use a safe backtick fence
ok 374 - code-span table cells preserve backslashes and use a safe backtick fence
  ---
  duration_ms: 1.803061
  ...
# Subtest: does not write any output when source validation fails
ok 375 - does not write any output when source validation fails
  ---
  duration_ms: 1.191464
  ...
# Subtest: BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
ok 376 - BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
  ---
  duration_ms: 3.149249
  ...
# Subtest: reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
ok 377 - reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
  ---
  duration_ms: 3.292673
  ...
# Subtest: stale, missing, canonical append, and frozen-owner models (BC8-BC10)
ok 378 - stale, missing, canonical append, and frozen-owner models (BC8-BC10)
  ---
  duration_ms: 0.751975
  ...
# Subtest: Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
ok 379 - Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
  ---
  duration_ms: 7.963488
  ...
# Subtest: budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
ok 380 - budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
  ---
  duration_ms: 1.590876
  ...
# Subtest: chip builder includes the 🔑 badge and has no edit controls
ok 381 - chip builder includes the 🔑 badge and has no edit controls
  ---
  duration_ms: 0.567302
  ...
# Subtest: RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
ok 382 - RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
  ---
  duration_ms: 1.938329
  ...
# Subtest: RBC2 hover × on a live chip calls removeDependent; notice is nav's
ok 383 - RBC2 hover × on a live chip calls removeDependent; notice is nav's
  ---
  duration_ms: 0.474486
  ...
# Subtest: RBC3 frozen, stale, and no api.blocks stay navigation-only
ok 384 - RBC3 frozen, stale, and no api.blocks stay navigation-only
  ---
  duration_ms: 0.924464
  ...
# Subtest: RBC4 Reading view matches Live Preview ＋ / ×
ok 385 - RBC4 Reading view matches Live Preview ＋ / ×
  ---
  duration_ms: 3.864796
  ...
# Subtest: collections namespace version is additive v1
ok 386 - collections namespace version is additive v1
  ---
  duration_ms: 0.988997
  ...
# Subtest: collection chip classes stay collection-specific through paint and refresh
ok 387 - collection chip classes stay collection-specific through paint and refresh
  ---
  duration_ms: 2.686898
  ...
# Subtest: projects: scalar resolved links count, lists never widen
ok 388 - projects: scalar resolved links count, lists never widen
  ---
  duration_ms: 0.304591
  ...
# Subtest: projects: templates, status, and containsAny edges
ok 389 - projects: templates, status, and containsAny edges
  ---
  duration_ms: 0.316644
  ...
# Subtest: references: exact prefix, md only, exact scalar status
ok 390 - references: exact prefix, md only, exact scalar status
  ---
  duration_ms: 0.261318
  ...
# Subtest: base contracts: accept current files, reject drift, tolerate presentation
ok 391 - base contracts: accept current files, reject drift, tolerate presentation
  ---
  duration_ms: 0.596419
  ...
# Subtest: entries: true zero vs unavailable with reason, failure isolation
ok 392 - entries: true zero vs unavailable with reason, failure isolation
  ---
  duration_ms: 0.244947
  ...
# Subtest: snapshot counts both collections once, true zero stays clickable
ok 393 - snapshot counts both collections once, true zero stays clickable
  ---
  duration_ms: 0.355609
  ...
# Subtest: snapshot never presents partial counts as final
ok 394 - snapshot never presents partial counts as final
  ---
  duration_ms: 0.383592
  ...
# Subtest: changed definitions fail closed per collection, never stale
ok 395 - changed definitions fail closed per collection, never stale
  ---
  duration_ms: 0.530914
  ...
# Subtest: renderChip links, labels, and cleans up per component
ok 396 - renderChip links, labels, and cleans up per component
  ---
  duration_ms: 0.575929
  ...
# Subtest: PENDING section excludes TODAY while the whole lane keeps it
ok 397 - PENDING section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 2.643515
  ...
# Subtest: NEXT section excludes TODAY while the whole lane keeps it
ok 398 - NEXT section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 0.433498
  ...
# Subtest: NEXT uses symbol *, not name matching
ok 399 - NEXT uses symbol *, not name matching
  ---
  duration_ms: 0.274043
  ...
# Subtest: READY badge and query agree on hide and path case variants
ok 400 - READY badge and query agree on hide and path case variants
  ---
  duration_ms: 0.595135
  ...
# Subtest: blocked uses the full list even outside the visible subset
ok 401 - blocked uses the full list even outside the visible subset
  ---
  duration_ms: 0.21491
  ...
# Subtest: duplicate block IDs, missing IDs, and reused objects stay per-row
ok 402 - duplicate block IDs, missing IDs, and reused objects stay per-row
  ---
  duration_ms: 0.244686
  ...
# Subtest: READY gating keeps exempt rows and drops NEW/ROTTEN
ok 403 - READY gating keeps exempt rows and drops NEW/ROTTEN
  ---
  duration_ms: 0.353134
  ...
# Subtest: throwing Today degrades to unavailable, never zero
ok 404 - throwing Today degrades to unavailable, never zero
  ---
  duration_ms: 7.478763
  ...
# Subtest: dashboard badges color the displayed section count and label whole-lane pressure
ok 405 - dashboard badges color the displayed section count and label whole-lane pressure
  ---
  duration_ms: 0.650832
  ...
# Subtest: dashboard section warning boundaries ignore TODAY-only whole-lane excess
ok 406 - dashboard section warning boundaries ignore TODAY-only whole-lane excess
  ---
  duration_ms: 0.77078
  ...
# Subtest: dashboard lane badge keeps unavailable data neutral
ok 407 - dashboard lane badge keeps unavailable data neutral
  ---
  duration_ms: 0.313368
  ...
# Subtest: dashboard lane paint and refresh keep color aligned with the visible section
ok 408 - dashboard lane paint and refresh keep color aligned with the visible section
  ---
  duration_ms: 2.619929
  ...
# Subtest: dashboard lane widgets refresh together and prune on unload
ok 409 - dashboard lane widgets refresh together and prune on unload
  ---
  duration_ms: 3.22777
  ...
# Subtest: daily paint matches dashboard section badges on screenshot fixtures
ok 410 - daily paint matches dashboard section badges on screenshot fixtures
  ---
  duration_ms: 21.695153
  ...
# Subtest: daily paint lane lint matches a red badge section count
ok 411 - daily paint lane lint matches a red badge section count
  ---
  duration_ms: 5.784269
  ...
# Subtest: daily and dashboard membership agree for exclusions and custom IN_PROGRESS
ok 412 - daily and dashboard membership agree for exclusions and custom IN_PROGRESS
  ---
  duration_ms: 5.40292
  ...
# Subtest: daily paint refreshes with dashboard when Today, lane, and cap change
ok 413 - daily paint refreshes with dashboard when Today, lane, and cap change
  ---
  duration_ms: 7.898073
  ...
# Subtest: older daily notes follow today's dashboard lanes
ok 414 - older daily notes follow today's dashboard lanes
  ---
  duration_ms: 4.001937
  ...
# Subtest: daily lane anchors keep shared navigation and reject stale paints
ok 415 - daily lane anchors keep shared navigation and reject stale paints
  ---
  duration_ms: 2.89244
  ...
# Subtest: daily paint stays unavailable until Tasks and Today are ready
ok 416 - daily paint stays unavailable until Tasks and Today are ready
  ---
  duration_ms: 1.263521
  ...
# Subtest: work tones: dashboard lane models carry section tones
ok 417 - work tones: dashboard lane models carry section tones
  ---
  duration_ms: 0.178601
  ...
# Subtest: T1 scheduled full-mode row gets a Fri mark inside the span
ok 418 - T1 scheduled full-mode row gets a Fri mark inside the span
  ---
  duration_ms: 2.99251
  ...
# Subtest: T2 done row maps to a completion Oct 5 mark
ok 419 - T2 done row maps to a completion Oct 5 mark
  ---
  duration_ms: 0.485676
  ...
# Subtest: T3 short-mode created span is left untouched by JS
ok 420 - T3 short-mode created span is left untouched by JS
  ---
  duration_ms: 0.292117
  ...
# Subtest: T4 pending row decorates once data-task appears; exhausted rows stay native
ok 421 - T4 pending row decorates once data-task appears; exhausted rows stay native
  ---
  duration_ms: 1.207475
  ...
# Subtest: T5 a second pass adds nothing
ok 422 - T5 a second pass adds nothing
  ---
  duration_ms: 0.292969
  ...
# Subtest: T6 task-due and task-start spans are untouched
ok 423 - T6 task-due and task-start spans are untouched
  ---
  duration_ms: 0.246931
  ...
# Subtest: T7 an invalid date is untouched
ok 424 - T7 an invalid date is untouched
  ---
  duration_ms: 0.279153
  ...
# Subtest: T8 nothing is scheduled with marks off or for connected non-Tasks elements
ok 425 - T8 nothing is scheduled with marks off or for connected non-Tasks elements
  ---
  duration_ms: 0.252953
  ...
# Subtest: T9 a Tasks-host Fri mark relabels to tomorrow on rollover
ok 426 - T9 a Tasks-host Fri mark relabels to tomorrow on rollover
  ---
  duration_ms: 0.690378
  ...
# Subtest: renderDateMarksIn schedules one shared frame for every row
ok 427 - renderDateMarksIn schedules one shared frame for every row
  ---
  duration_ms: 0.97417
  ...
# Subtest: the Tasks pass never throws on hostile input
ok 428 - the Tasks pass never throws on hostile input
  ---
  duration_ms: 0.504352
  ...
# Subtest: T10 real-DOM NodeList children decorate via direct and queued passes
ok 429 - T10 real-DOM NodeList children decorate via direct and queued passes
  ---
  duration_ms: 0.578023
  ...
# Subtest: T11 toggling off before a queued frame runs writes nothing
ok 430 - T11 toggling off before a queued frame runs writes nothing
  ---
  duration_ms: 0.401637
  ...
# Subtest: T12 a pending-row retry followed by disabling writes nothing
ok 431 - T12 a pending-row retry followed by disabling writes nothing
  ---
  duration_ms: 0.299893
  ...
# Subtest: T13 unloading before a callback runs writes nothing
ok 432 - T13 unloading before a callback runs writes nothing
  ---
  duration_ms: 0.957587
  ...
# Subtest: RT1 full-mode recurring result gets a daily mark and stays idempotent
ok 433 - RT1 full-mode recurring result gets a daily mark and stays idempotent
  ---
  duration_ms: 1.066675
  ...
# Subtest: RT2 recurring labels use the shared cadence grammar
ok 434 - RT2 recurring labels use the shared cadence grammar
  ---
  duration_ms: 2.165452
  ...
# Subtest: RT2a unknown inherited-name rules stay readable in Tasks results
ok 435 - RT2a unknown inherited-name rules stay readable in Tasks results
  ---
  duration_ms: 0.436603
  ...
# Subtest: RT3 short-mode recurring spans stay native to JS and use the CSS loop
ok 436 - RT3 short-mode recurring spans stay native to JS and use the CSS loop
  ---
  duration_ms: 0.611096
  ...
# Subtest: RT4 open checklist members keep recurrence pills without `when done`
ok 437 - RT4 open checklist members keep recurrence pills without `when done`
  ---
  duration_ms: 0.506386
  ...
# Subtest: RT5 invalid recurrence stays native and incomplete rows are retried
ok 438 - RT5 invalid recurrence stays native and incomplete rows are retried
  ---
  duration_ms: 0.477922
  ...
# Subtest: styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
ok 439 - styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
  ---
  duration_ms: 0.857366
  ...
# Subtest: DATE_MARK_FIELDS lists the four dates with verbs
ok 440 - DATE_MARK_FIELDS lists the four dates with verbs
  ---
  duration_ms: 1.636374
  ...
# Subtest: DM1 created today: label, tooltip, fold, quiet field
ok 441 - DM1 created today: label, tooltip, fold, quiet field
  ---
  duration_ms: 1.395634
  ...
# Subtest: DM2 created yesterday without space after the colons
ok 442 - DM2 created yesterday without space after the colons
  ---
  duration_ms: 0.364566
  ...
# Subtest: DM3-DM6 scheduled tomorrow, weekday, and month/day labels
ok 443 - DM3-DM6 scheduled tomorrow, weekday, and month/day labels
  ---
  duration_ms: 0.221683
  ...
# Subtest: DM7 scheduled today reads with emphasis timing
ok 444 - DM7 scheduled today reads with emphasis timing
  ---
  duration_ms: 0.220852
  ...
# Subtest: DM8 past scheduled uses month/day, never a weekday
ok 445 - DM8 past scheduled uses month/day, never a weekday
  ---
  duration_ms: 0.154655
  ...
# Subtest: DM9 completion on a closed task keeps the timeline grammar
ok 446 - DM9 completion on a closed task keeps the timeline grammar
  ---
  duration_ms: 0.190233
  ...
# Subtest: DM10 cancelled across years appends the year
ok 447 - DM10 cancelled across years appends the year
  ---
  duration_ms: 0.131331
  ...
# Subtest: DM11 next-year date appends the year
ok 448 - DM11 next-year date appends the year
  ---
  duration_ms: 0.305113
  ...
# Subtest: DM12 the weekday rule wins across the year boundary
ok 449 - DM12 the weekday rule wins across the year boundary
  ---
  duration_ms: 0.382099
  ...
# Subtest: DM13 two marks in order with folds 1 and 2
ok 450 - DM13 two marks in order with folds 1 and 2
  ---
  duration_ms: 0.412878
  ...
# Subtest: DM14 created and scheduled ranges stay disjoint from the fresh mark
ok 451 - DM14 created and scheduled ranges stay disjoint from the fresh mark
  ---
  duration_ms: 0.321383
  ...
# Subtest: DM15-DM16 paren and padded brackets are canonical
ok 452 - DM15-DM16 paren and padded brackets are canonical
  ---
  duration_ms: 0.165856
  ...
# Subtest: DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
ok 453 - DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
  ---
  duration_ms: 0.320601
  ...
# Subtest: DM22 code still parses pure but decorates nothing (see Live Preview)
ok 454 - DM22 code still parses pure but decorates nothing (see Live Preview)
  ---
  duration_ms: 0.111603
  ...
# Subtest: DM23 rescheduled is untouched and never a duplicate
ok 455 - DM23 rescheduled is untouched and never a duplicate
  ---
  duration_ms: 0.142091
  ...
# Subtest: DN1-DN9 non-canonical fields get no mark
ok 456 - DN1-DN9 non-canonical fields get no mark
  ---
  duration_ms: 0.23096
  ...
# Subtest: dateMarkContentStart finds content on list, quoted, and plain lines
ok 457 - dateMarkContentStart finds content on list, quoted, and plain lines
  ---
  duration_ms: 0.104019
  ...
# Subtest: dateMarkRelativePhrase covers the exact-day phrases
ok 458 - dateMarkRelativePhrase covers the exact-day phrases
  ---
  duration_ms: 0.085443
  ...
# Subtest: dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
ok 459 - dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
  ---
  duration_ms: 0.320371
  ...
# Subtest: no model output contains a double colon
ok 460 - no model output contains a double colon
  ---
  duration_ms: 2.288578
  ...
# Subtest: a new day always changes the widget key
ok 461 - a new day always changes the widget key
  ---
  duration_ms: 0.166688
  ...
# Subtest: element structure and the decorative/inheritColor/rendered options
ok 462 - element structure and the decorative/inheritColor/rendered options
  ---
  duration_ms: 0.453997
  ...
# Subtest: Live Preview emits several decorations in ascending order
ok 463 - Live Preview emits several decorations in ascending order
  ---
  duration_ms: 1.43006
  ...
# Subtest: Live Preview reveals per field, never the whole line
ok 464 - Live Preview reveals per field, never the whole line
  ---
  duration_ms: 0.261679
  ...
# Subtest: Live Preview refuses source mode, code, and disabled marks
ok 465 - Live Preview refuses source mode, code, and disabled marks
  ---
  duration_ms: 0.458656
  ...
# Subtest: widget mousedown anchors at the field start for folds 0, 1, and 2
ok 466 - widget mousedown anchors at the field start for folds 0, 1, and 2
  ---
  duration_ms: 0.961635
  ...
# Subtest: DM24 a cursor in the folded run unfolds the mark (vim cw)
ok 467 - DM24 a cursor in the folded run unfolds the mark (vim cw)
  ---
  duration_ms: 0.246631
  ...
# Subtest: DM25 a cursor in Tasks double space unfolds only that field
ok 468 - DM25 a cursor in Tasks double space unfolds only that field
  ---
  duration_ms: 0.186896
  ...
# Subtest: a selection ending inside the run unfolds; ending at its start keeps the fold
ok 469 - a selection ending inside the run unfolds; ending at its start keeps the fold
  ---
  duration_ms: 0.182128
  ...
# Subtest: no emitted decoration ever hides a cursor, and reveal still means field overlap
ok 470 - no emitted decoration ever hides a cursor, and reveal still means field overlap
  ---
  duration_ms: 10.272985
  ...
# Subtest: dateMarkSelectionFold: reveal, unfold, fold, and garbage input
ok 471 - dateMarkSelectionFold: reveal, unfold, fold, and garbage input
  ---
  duration_ms: 0.310883
  ...
# Subtest: mousedown on an unfolded (fold-0) widget anchors at the field start
ok 472 - mousedown on an unfolded (fold-0) widget anchors at the field start
  ---
  duration_ms: 0.436463
  ...
# Subtest: rendered views split several fields in one node
ok 473 - rendered views split several fields in one node
  ---
  duration_ms: 1.663815
  ...
# Subtest: rendered views skip exclusions and duplicates
ok 474 - rendered views skip exclusions and duplicates
  ---
  duration_ms: 0.510103
  ...
# Subtest: RO1 rendered marks relabel in place across midnight
ok 475 - RO1 rendered marks relabel in place across midnight
  ---
  duration_ms: 0.470818
  ...
# Subtest: rollover dispatches once per day change and never touches widgets
ok 476 - rollover dispatches once per day change and never touches widgets
  ---
  duration_ms: 0.377871
  ...
# Subtest: api.dateMarks v1 is additive, sync, and never throwing
ok 477 - api.dateMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.480527
  ...
# Subtest: session toggle and onload wiring
ok 478 - session toggle and onload wiring
  ---
  duration_ms: 4.273054
  ...
# Subtest: styles.css contract: masks, tones, repair flag, resting
ok 479 - styles.css contract: masks, tones, repair flag, resting
  ---
  duration_ms: 0.871774
  ...
# Subtest: DP parse vectors
ok 480 - DP parse vectors
  ---
  duration_ms: 3.123551
  ...
# Subtest: DC chip model vectors
ok 481 - DC chip model vectors
  ---
  duration_ms: 2.073026
  ...
# Subtest: decoration builds one widget, reveals on cursor, skips code and ranges
ok 482 - decoration builds one widget, reveals on cursor, skips code and ranges
  ---
  duration_ms: 8.066823
  ...
# Subtest: decoration skips paragraphs, grandchildren, and Work Log lines
ok 483 - decoration skips paragraphs, grandchildren, and Work Log lines
  ---
  duration_ms: 0.760792
  ...
# Subtest: decoration renders chips on DP30 and still skips DP20
ok 484 - decoration renders chips on DP30 and still skips DP20
  ---
  duration_ms: 0.85917
  ...
# Subtest: ownership check reads O(depth) lines, not the whole note
ok 485 - ownership check reads O(depth) lines, not the whole note
  ---
  duration_ms: 3.135524
  ...
# Subtest: widget identity covers the line and the interactive flag
ok 486 - widget identity covers the line and the interactive flag
  ---
  duration_ms: 1.673374
  ...
# Subtest: element hides actions without nav api v1
ok 487 - element hides actions without nav api v1
  ---
  duration_ms: 0.758027
  ...
# Subtest: nav api feature detection gates actions
ok 488 - nav api feature detection gates actions
  ---
  duration_ms: 0.45566
  ...
# Subtest: reading view decorates only the Depends-On row, hides chrome, stays idempotent
ok 489 - reading view decorates only the Depends-On row, hides chrome, stays idempotent
  ---
  duration_ms: 4.152324
  ...
# Subtest: reading view collapses more than three Done targets to one chip
ok 490 - reading view collapses more than three Done targets to one chip
  ---
  duration_ms: 1.419159
  ...
# Subtest: DC chip model vectors by id: DC2, DC5, DC6, DC9
ok 491 - DC chip model vectors by id: DC2, DC5, DC6, DC9
  ---
  duration_ms: 0.317286
  ...
# Subtest: chip actions send the 0-based line index through nav api v1
ok 492 - chip actions send the 0-based line index through nav api v1
  ---
  duration_ms: 1.206032
  ...
# Subtest: chip hover passes the chip element and its row to the preview
ok 493 - chip hover passes the chip element and its row to the preview
  ---
  duration_ms: 0.202456
  ...
# Subtest: chip lookup index lives on the freshness memo
ok 494 - chip lookup index lives on the freshness memo
  ---
  duration_ms: 0.526886
  ...
# Subtest: reading view hides actions when the line cannot be derived
ok 495 - reading view hides actions when the line cannot be derived
  ---
  duration_ms: 11.793527
  ...
# Subtest: reading view actions carry the derived 0-based line
ok 496 - reading view actions carry the derived 0-based line
  ---
  duration_ms: 2.294399
  ...
# Subtest: reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
ok 497 - reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
  ---
  duration_ms: 0.517909
  ...
# Subtest: reading view renders chips on DP30 (owner is a task under a Work Log entry)
ok 498 - reading view renders chips on DP30 (owner is a task under a Work Log entry)
  ---
  duration_ms: 0.567322
  ...
# Subtest: reading view DP30 row actions send the owned Depends-On line
ok 499 - reading view DP30 row actions send the owned Depends-On line
  ---
  duration_ms: 2.126618
  ...
# Subtest: reading view second-row remove sends the second line when two tasks share a prerequisite
ok 500 - reading view second-row remove sends the second line when two tasks share a prerequisite
  ---
  duration_ms: 1.935263
  ...
# Subtest: chip lookup index builds once per freshness memo
ok 501 - chip lookup index builds once per freshness memo
  ---
  duration_ms: 0.542034
  ...
# Subtest: decoration evaluates ownership without copying the note
ok 502 - decoration evaluates ownership without copying the note
  ---
  duration_ms: 0.564858
  ...
# Subtest: toggle flips the body class and onload wires chips
ok 503 - toggle flips the body class and onload wires chips
  ---
  duration_ms: 4.388937
  ...
# Subtest: capability: nav card v2 is capable
ok 504 - capability: nav card v2 is capable
  ---
  duration_ms: 0.934533
  ...
# Subtest: capability: nav card v1 is not capable
ok 505 - capability: nav card v1 is not capable
  ---
  duration_ms: 0.169313
  ...
# Subtest: capability: absent nav, missing api, and old versions are not capable
ok 506 - capability: absent nav, missing api, and old versions are not capable
  ---
  duration_ms: 0.138103
  ...
# Subtest: capability: a throwing app never throws
ok 507 - capability: a throwing app never throws
  ---
  duration_ms: 0.200243
  ...
# Subtest: leaf: active capable due choice replaces refresh with a leaf
ok 508 - leaf: active capable due choice replaces refresh with a leaf
  ---
  duration_ms: 2.656068
  ...
# Subtest: leaf: the same row without the card keeps refresh and counting words
ok 509 - leaf: the same row without the card keeps refresh and counting words
  ---
  duration_ms: 0.430942
  ...
# Subtest: leaf: early dates still leaf when capable
ok 510 - leaf: early dates still leaf when capable
  ---
  duration_ms: 0.412478
  ...
# Subtest: leaf: decay-off rows never leaf even when capable
ok 511 - leaf: decay-off rows never leaf even when capable
  ---
  duration_ms: 0.40879
  ...
# Subtest: leaf: below-threshold rows never leaf
ok 512 - leaf: below-threshold rows never leaf
  ---
  duration_ms: 0.548176
  ...
# Subtest: leaf: threshold zero asks on every due re-confirmation when capable
ok 513 - leaf: threshold zero asks on every due re-confirmation when capable
  ---
  duration_ms: 0.489114
  ...
# Subtest: leaf: overflow renders capped dots with +N and the exact count in text
ok 514 - leaf: overflow renders capped dots with +N and the exact count in text
  ---
  duration_ms: 0.306385
  ...
# Subtest: leaf: out-of-scope and closed tasks show dots quietly, never a leaf
ok 515 - leaf: out-of-scope and closed tasks show dots quietly, never a leaf
  ---
  duration_ms: 0.706469
  ...
# Subtest: leaf: unresolved marks show dots quietly with counting-only wording
ok 516 - leaf: unresolved marks show dots quietly with counting-only wording
  ---
  duration_ms: 0.198218
  ...
# Subtest: element: leaf marks carry data-decide true and a leaf path
ok 517 - element: leaf marks carry data-decide true and a leaf path
  ---
  duration_ms: 0.639581
  ...
# Subtest: element: non-decision marks carry data-decide false
ok 518 - element: non-decision marks carry data-decide false
  ---
  duration_ms: 0.224999
  ...
# Subtest: footer groups omit every zero tier and keep walk order
ok 519 - footer groups omit every zero tier and keep walk order
  ---
  duration_ms: 1.658455
  ...
# Subtest: PRE and POST groups bracket the nine-tier queue and expose completion hints
ok 520 - PRE and POST groups bracket the nine-tier queue and expose completion hints
  ---
  duration_ms: 0.81204
  ...
# Subtest: a NEW-state project appears only in its walk tier
ok 521 - a NEW-state project appears only in its walk tier
  ---
  duration_ms: 0.205381
  ...
# Subtest: empty queue hides the footer even with upkeep or a met budget
ok 522 - empty queue hides the footer even with upkeep or a met budget
  ---
  duration_ms: 0.149145
  ...
# Subtest: unavailable or missing data never render false counts
ok 523 - unavailable or missing data never render false counts
  ---
  duration_ms: 0.135489
  ...
# Subtest: generic summary names due, commitments, and nonempty groups
ok 524 - generic summary names due, commitments, and nonempty groups
  ---
  duration_ms: 0.340299
  ...
# Subtest: current-task context uses shared ranks and compact wording
ok 525 - current-task context uses shared ranks and compact wording
  ---
  duration_ms: 0.625875
  ...
# Subtest: only ROTTEN remaining names commitments done or a met budget
ok 526 - only ROTTEN remaining names commitments done or a met budget
  ---
  duration_ms: 0.259064
  ...
# Subtest: NEW and commitments take precedence over a met budget
ok 527 - NEW and commitments take precedence over a met budget
  ---
  duration_ms: 0.43517
  ...
# Subtest: reviewEntryView compact and detail cover the original freshness tiers
ok 528 - reviewEntryView compact and detail cover the original freshness tiers
  ---
  duration_ms: 0.838601
  ...
# Subtest: cursor matching requires a unique verified identity
ok 529 - cursor matching requires a unique verified identity
  ---
  duration_ms: 0.365868
  ...
# Subtest: footer paint hides the host and keeps a stable button
ok 530 - footer paint hides the host and keeps a stable button
  ---
  duration_ms: 1.061206
  ...
# Subtest: status bar 0-1-0 transitions hide without a reload
ok 531 - status bar 0-1-0 transitions hide without a reload
  ---
  duration_ms: 8.585774
  ...
# Subtest: cursor-only updates reuse a warm memo
ok 532 - cursor-only updates reuse a warm memo
  ---
  duration_ms: 1.492739
  ...
# Subtest: unload disconnects the observer and click handler
ok 533 - unload disconnects the observer and click handler
  ---
  duration_ms: 1.474093
  ...
# Subtest: queue-built ranks agree with the footer current entry
ok 534 - queue-built ranks agree with the footer current entry
  ---
  duration_ms: 1.095
  ...
# Subtest: footer short labels map every tier
ok 535 - footer short labels map every tier
  ---
  duration_ms: 0.145218
  ...
# Subtest: current-row footer context uses short labels while entry views keep full labels
ok 536 - current-row footer context uses short labels while entry views keep full labels
  ---
  duration_ms: 0.338576
  ...
# Subtest: legend line lists only current abbreviated tiers
ok 537 - legend line lists only current abbreviated tiers
  ---
  duration_ms: 0.373803
  ...
# Subtest: queue-row quickRoll preview takes the hint slot, tooltip, and aria
ok 538 - queue-row quickRoll preview takes the hint slot, tooltip, and aria
  ---
  duration_ms: 1.547924
  ...
# Subtest: quickRoll detail sits next to the action hint on lane rows
ok 539 - quickRoll detail sits next to the action hint on lane rows
  ---
  duration_ms: 0.264334
  ...
# Subtest: missing, failed, or off-row quickRoll leaves the footer byte-identical
ok 540 - missing, failed, or off-row quickRoll leaves the footer byte-identical
  ---
  duration_ms: 0.474416
  ...
# Subtest: PRE rows stay unchanged under the nav checklist-tier contract
ok 541 - PRE rows stay unchanged under the nav checklist-tier contract
  ---
  duration_ms: 0.290214
  ...
# Subtest: status bar wires nav api.quickRoll into the hint slot
ok 542 - status bar wires nav api.quickRoll into the hint slot
  ---
  duration_ms: 1.78743
  ...
# Subtest: status bar ignores missing, v0, or throwing quickRoll namespaces
ok 543 - status bar ignores missing, v0, or throwing quickRoll namespaces
  ---
  duration_ms: 3.104985
  ...
# Subtest: K1 absent: no keeps means 0 with no lints
ok 544 - K1 absent: no keeps means 0 with no lints
  ---
  duration_ms: 2.302013
  ...
# Subtest: K8 misplaced: keeps inside the Tasks suffix reads with a lint
ok 545 - K8 misplaced: keeps inside the Tasks suffix reads with a lint
  ---
  duration_ms: 0.432335
  ...
# Subtest: K9 duplicates and invalid values: first valid wins, else 0
ok 546 - K9 duplicates and invalid values: first valid wins, else 0
  ---
  duration_ms: 0.636525
  ...
# Subtest: K10 ceiling and NEW: 999 reads, never-confirmed reads 0
ok 547 - K10 ceiling and NEW: 999 reads, never-confirmed reads 0
  ---
  duration_ms: 0.242263
  ...
# Subtest: K13 exact keys: near-miss keys are not keeps; parens read
ok 548 - K13 exact keys: near-miss keys are not keeps; parens read
  ---
  duration_ms: 0.196104
  ...
# Subtest: keeps value parser accepts only decimal 1-999
ok 549 - keeps value parser accepts only decimal 1-999
  ---
  duration_ms: 0.18329
  ...
# Subtest: K2 first valid canonical: uncounted keep preserves and repairs
ok 550 - K2 first valid canonical: uncounted keep preserves and repairs
  ---
  duration_ms: 0.770841
  ...
# Subtest: K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
ok 551 - K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
  ---
  duration_ms: 0.493461
  ...
# Subtest: K4 same-day preserve noop: canonical kept line is byte-identical
ok 552 - K4 same-day preserve noop: canonical kept line is byte-identical
  ---
  duration_ms: 0.451431
  ...
# Subtest: K5 generic stamp clears, even same-day
ok 553 - K5 generic stamp clears, even same-day
  ---
  duration_ms: 0.460058
  ...
# Subtest: K6 set-refresh clears keeps
ok 554 - K6 set-refresh clears keeps
  ---
  duration_ms: 0.284363
  ...
# Subtest: K7 stale stamp clears keeps
ok 555 - K7 stale stamp clears keeps
  ---
  duration_ms: 0.214379
  ...
# Subtest: K8b misplaced keeps repaired to canonical order by a keep
ok 556 - K8b misplaced keeps repaired to canonical order by a keep
  ---
  duration_ms: 0.246961
  ...
# Subtest: K11 refusals preserve: closed and recurring lines never write
ok 557 - K11 refusals preserve: closed and recurring lines never write
  ---
  duration_ms: 0.254185
  ...
# Subtest: counted keep increments a stale streak once in the same write
ok 558 - counted keep increments a stale streak once in the same write
  ---
  duration_ms: 0.249376
  ...
# Subtest: first counted keep on a streakless due task writes keeps 1
ok 559 - first counted keep on a streakless due task writes keeps 1
  ---
  duration_ms: 0.17828
  ...
# Subtest: counted keep saturates at 999 and never wraps
ok 560 - counted keep saturates at 999 and never wraps
  ---
  duration_ms: 0.245238
  ...
# Subtest: counted keep needs a valid prior fresh before today
ok 561 - counted keep needs a valid prior fresh before today
  ---
  duration_ms: 0.329639
  ...
# Subtest: counted keep repairs malformed and duplicate placement
ok 562 - counted keep repairs malformed and duplicate placement
  ---
  duration_ms: 0.273593
  ...
# Subtest: uncounted keep preserves the valid value while canonicalizing
ok 563 - uncounted keep preserves the valid value while canonicalizing
  ---
  duration_ms: 0.211794
  ...
# Subtest: UB13 keep on an unblock TICKLER preserves the streak and skips the card
ok 564 - UB13 keep on an unblock TICKLER preserves the streak and skips the card
  ---
  duration_ms: 1.871872
  ...
# Subtest: a scheduled tickler still counts when schedule wins an unblock tie
ok 565 - a scheduled tickler still counts when schedule wins an unblock tie
  ---
  duration_ms: 0.360218
  ...
# Subtest: decay normalization: absent, null, true, and {} enable with 3
ok 566 - decay normalization: absent, null, true, and {} enable with 3
  ---
  duration_ms: 0.743629
  ...
# Subtest: decay false counts and displays but never asks
ok 567 - decay false counts and displays but never asks
  ---
  duration_ms: 0.140588
  ...
# Subtest: decay keeps 0 and fixed entry normalize
ok 568 - decay keeps 0 and fixed entry normalize
  ---
  duration_ms: 0.174433
  ...
# Subtest: invalid decay shapes fail the freshness config contract
ok 569 - invalid decay shapes fail the freshness config contract
  ---
  duration_ms: 0.325761
  ...
# Subtest: B: at-limit Ready due rows decide on every local day
ok 570 - B: at-limit Ready due rows decide on every local day
  ---
  duration_ms: 0.63936
  ...
# Subtest: D1 early date: an at-limit Ready due row decides
ok 571 - D1 early date: an at-limit Ready due row decides
  ---
  duration_ms: 0.165706
  ...
# Subtest: D2 at limit decides; D3 below limit stamps without a card
ok 572 - D2 at limit decides; D3 below limit stamps without a card
  ---
  duration_ms: 0.169283
  ...
# Subtest: D4 tickler counts as due; D5 NEW never decides
ok 573 - D4 tickler counts as due; D5 NEW never decides
  ---
  duration_ms: 0.225731
  ...
# Subtest: D6 zero limit asks on every due Ready re-confirmation
ok 574 - D6 zero limit asks on every due Ready re-confirmation
  ---
  duration_ms: 0.128796
  ...
# Subtest: D7 off never asks; D8 lane rows never decide
ok 575 - D7 off never asks; D8 lane rows never decide
  ---
  duration_ms: 0.124017
  ...
# Subtest: evaluator, queue, and counts carry keeps and decide
ok 576 - evaluator, queue, and counts carry keeps and decide
  ---
  duration_ms: 1.240457
  ...
# Subtest: no keeps: the existing mark is unchanged
ok 577 - no keeps: the existing mark is unchanged
  ---
  duration_ms: 0.938211
  ...
# Subtest: aging with two keeps: faint pips plus a counting-only line
ok 578 - aging with two keeps: faint pips plus a counting-only line
  ---
  duration_ms: 0.276478
  ...
# Subtest: confirmed today with two keeps: check glyph, faint dots
ok 579 - confirmed today with two keeps: check glyph, faint dots
  ---
  duration_ms: 0.21449
  ...
# Subtest: due below threshold: orange capsule keeps its glyph, adds dots
ok 580 - due below threshold: orange capsule keeps its glyph, adds dots
  ---
  duration_ms: 0.256129
  ...
# Subtest: resting marks show historical dots quietly and never decide
ok 581 - resting marks show historical dots quietly and never decide
  ---
  duration_ms: 0.471049
  ...
# Subtest: active decision due: data stays truthful, leaf stays gated
ok 582 - active decision due: data stays truthful, leaf stays gated
  ---
  duration_ms: 0.360929
  ...
# Subtest: dot caps follow the threshold with +N overflow
ok 583 - dot caps follow the threshold with +N overflow
  ---
  duration_ms: 0.628439
  ...
# Subtest: keeps tooltip wording: singulars, zero threshold, off state
ok 584 - keeps tooltip wording: singulars, zero threshold, off state
  ---
  duration_ms: 0.11545
  ...
# Subtest: noncanonical keeps never fold but keep their repair pill
ok 585 - noncanonical keeps never fold but keep their repair pill
  ---
  duration_ms: 0.34052
  ...
# Subtest: quoted lines fold; rendered fragments fold without task checks
ok 586 - quoted lines fold; rendered fragments fold without task checks
  ---
  duration_ms: 0.226132
  ...
# Subtest: unresolved marks show the line's own pips quietly and never decide
ok 587 - unresolved marks show the line's own pips quietly and never decide
  ---
  duration_ms: 0.189452
  ...
# Subtest: consensus sees count and decision eligibility: ambiguity stays neutral
ok 588 - consensus sees count and decision eligibility: ambiguity stays neutral
  ---
  duration_ms: 0.489564
  ...
# Subtest: pips render as one aria-hidden span with the count in the label
ok 589 - pips render as one aria-hidden span with the count in the label
  ---
  duration_ms: 1.055985
  ...
# Subtest: Live Preview decorates the folded range including space and refresh
ok 590 - Live Preview decorates the folded range including space and refresh
  ---
  duration_ms: 5.110965
  ...
# Subtest: Live Preview reveals the raw field when the cursor overlaps either edge
ok 591 - Live Preview reveals the raw field when the cursor overlaps either edge
  ---
  duration_ms: 1.203016
  ...
# Subtest: Live Preview skips codeblock and inline code spans
ok 592 - Live Preview skips codeblock and inline code spans
  ---
  duration_ms: 0.663065
  ...
# Subtest: source mode and marks-off yield no decorations
ok 593 - source mode and marks-off yield no decorations
  ---
  duration_ms: 0.179573
  ...
# Subtest: update rebuilds on the refresh effect and widget eq is stable
ok 594 - update rebuilds on the refresh effect and widget eq is stable
  ---
  duration_ms: 0.962446
  ...
# Subtest: widget click reveals the field at the folded offset
ok 595 - widget click reveals the field at the folded offset
  ---
  duration_ms: 0.691209
  ...
# Subtest: line resolver prefers exact, then consensus, then unresolved
ok 596 - line resolver prefers exact, then consensus, then unresolved
  ---
  duration_ms: 1.381777
  ...
# Subtest: decoration builds reuse the snapshot without touching the loader
ok 597 - decoration builds reuse the snapshot without touching the loader
  ---
  duration_ms: 0.480086
  ...
# Subtest: rendered views split text nodes and skip excluded ancestors
ok 598 - rendered views split text nodes and skip excluded ancestors
  ---
  duration_ms: 2.286443
  ...
# Subtest: rendered views stay idempotent
ok 599 - rendered views stay idempotent
  ---
  duration_ms: 0.688594
  ...
# Subtest: text resolver reaches consensus and degrades to neutral
ok 600 - text resolver reaches consensus and degrades to neutral
  ---
  duration_ms: 0.627147
  ...
# Subtest: session toggle flips the body class and notifies
ok 601 - session toggle flips the body class and notifies
  ---
  duration_ms: 0.771693
  ...
# Subtest: Live Preview reads only the child block and never calls doc.toString
ok 602 - Live Preview reads only the child block and never calls doc.toString
  ---
  duration_ms: 1.355317
  ...
# Subtest: Live Preview stops at the first nonblank line at or above the task
ok 603 - Live Preview stops at the first nonblank line at or above the task
  ---
  duration_ms: 0.320211
  ...
# Subtest: Live Preview performance stays bounded on a large child block
ok 604 - Live Preview performance stays bounded on a large child block
  ---
  duration_ms: 1444.093446
  ...
# Subtest: reading view shows the rotten line and excludes Tasks and Dataview rows
ok 605 - reading view shows the rotten line and excludes Tasks and Dataview rows
  ---
  duration_ms: 0.688274
  ...
# Subtest: query-row consensus stays byte-identical with and without a Rotten Log
ok 606 - query-row consensus stays byte-identical with and without a Rotten Log
  ---
  duration_ms: 0.313649
  ...
# Subtest: onload registers the toggle, extension, and post-processor
ok 607 - onload registers the toggle, extension, and post-processor
  ---
  duration_ms: 3.777589
  ...
# Subtest: M1 today: check glyph, today label, full ring
ok 608 - M1 today: check glyph, today label, full ring
  ---
  duration_ms: 3.996777
  ...
# Subtest: M2 aging: ring glyph, 3d label, draining lease
ok 609 - M2 aging: ring glyph, 3d label, draining lease
  ---
  duration_ms: 0.443807
  ...
# Subtest: M3 boundary: ROTTEN due capsule with Alt+F hint
ok 610 - M3 boundary: ROTTEN due capsule with Alt+F hint
  ---
  duration_ms: 0.384894
  ...
# Subtest: checklist marks replace stamp hints with their completion tier
ok 611 - checklist marks replace stamp hints with their completion tier
  ---
  duration_ms: 0.783295
  ...
# Subtest: M4 yesterday uses the yesterday relative
ok 612 - M4 yesterday uses the yesterday relative
  ---
  duration_ms: 0.254135
  ...
# Subtest: M5 folded refresh shows the /14d suffix
ok 613 - M5 folded refresh shows the /14d suffix
  ---
  duration_ms: 0.436133
  ...
# Subtest: M6 refresh today: today tone hides the interval suffix
ok 614 - M6 refresh today: today tone hides the interval suffix
  ---
  duration_ms: 0.318197
  ...
# Subtest: M7 note interval stays tooltip-only
ok 615 - M7 note interval stays tooltip-only
  ---
  duration_ms: 0.507879
  ...
# Subtest: M8 resurfaced: due tone on the scheduled return
ok 616 - M8 resurfaced: due tone on the scheduled return
  ---
  duration_ms: 0.50297
  ...
# Subtest: M9 due NEXT lane with keep/release/today keys
ok 617 - M9 due NEXT lane with keep/release/today keys
  ---
  duration_ms: 0.525493
  ...
# Subtest: M10 NEXT lane stamped today
ok 618 - M10 NEXT lane stamped today
  ---
  duration_ms: 0.318348
  ...
# Subtest: M19 disabled Next lane rests
ok 619 - M19 disabled Next lane rests
  ---
  duration_ms: 0.283651
  ...
# Subtest: M20 PENDING lane folds refresh without the suffix
ok 620 - M20 PENDING lane folds refresh without the suffix
  ---
  duration_ms: 0.263122
  ...
# Subtest: M11 closed: resting beats age 0
ok 621 - M11 closed: resting beats age 0
  ---
  duration_ms: 0.205763
  ...
# Subtest: M12 unresolved running and M13 unresolved lease over
ok 622 - M12 unresolved running and M13 unresolved lease over
  ---
  duration_ms: 0.22511
  ...
# Subtest: M14 linked today rests with its reason
ok 623 - M14 linked today rests with its reason
  ---
  duration_ms: 0.176597
  ...
# Subtest: M15 other year shows the year and the 282d age
ok 624 - M15 other year shows the year and the 282d age
  ---
  duration_ms: 0.138524
  ...
# Subtest: M16 quoted line keeps foldSpace
ok 625 - M16 quoted line keeps foldSpace
  ---
  duration_ms: 0.186686
  ...
# Subtest: M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
ok 626 - M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
  ---
  duration_ms: 0.420452
  ...
# Subtest: N1-N6 non-canonical lines get no mark
ok 627 - N1-N6 non-canonical lines get no mark
  ---
  duration_ms: 0.179532
  ...
# Subtest: C1-C3 consensus is exact or unresolved
ok 628 - C1-C3 consensus is exact or unresolved
  ---
  duration_ms: 0.617048
  ...
# Subtest: freshnessMarkResolution treats evaluator new as unresolved
ok 629 - freshnessMarkResolution treats evaluator new as unresolved
  ---
  duration_ms: 0.13595
  ...
# Subtest: freshnessMarkSourceInText covers rendered fragments
ok 630 - freshnessMarkSourceInText covers rendered fragments
  ---
  duration_ms: 0.198329
  ...
# Subtest: tone order: closed, then due, then age 0, then out of scope
ok 631 - tone order: closed, then due, then age 0, then out of scope
  ---
  duration_ms: 0.361981
  ...
# Subtest: no tooltip ever contains a double colon
ok 632 - no tooltip ever contains a double colon
  ---
  duration_ms: 0.674136
  ...
# Subtest: freshnessShortDate pins English names and the year rule
ok 633 - freshnessShortDate pins English names and the year rule
  ---
  duration_ms: 0.101553
  ...
# Subtest: DOM builder structure, attributes, and ring geometry
ok 634 - DOM builder structure, attributes, and ring geometry
  ---
  duration_ms: 1.062768
  ...
# Subtest: every mark helper is synchronous and never throws on bad input
ok 635 - every mark helper is synchronous and never throws on bad input
  ---
  duration_ms: 0.112585
  ...
# Subtest: rotten line wording covers 0, 1, and many entries
ok 636 - rotten line wording covers 0, 1, and many entries
  ---
  duration_ms: 0.389974
  ...
# Subtest: rotten line date format includes the year only when it differs
ok 637 - rotten line date format includes the year only when it differs
  ---
  duration_ms: 0.194722
  ...
# Subtest: rotten line truncates the reason to 48 code points without splitting emoji
ok 638 - rotten line truncates the reason to 48 code points without splitting emoji
  ---
  duration_ms: 0.15196
  ...
# Subtest: rotten history rejects ambiguous, invalid, and nested entries
ok 639 - rotten history rejects ambiguous, invalid, and nested entries
  ---
  duration_ms: 1.118725
  ...
# Subtest: rotten marker vectors reject mismatched emoji and missing spaces
ok 640 - rotten marker vectors reject mismatched emoji and missing spaces
  ---
  duration_ms: 0.300573
  ...
# Subtest: rotten line splices before the action line and reaches aria-label
ok 641 - rotten line splices before the action line and reaches aria-label
  ---
  duration_ms: 0.357883
  ...
# Subtest: freshness namespace v12 exposes unblock TICKLER metadata and writers
ok 642 - freshness namespace v12 exposes unblock TICKLER metadata and writers
  ---
  duration_ms: 12.232645
  ...
# Subtest: freshness state and count API expose an unblock return source
ok 643 - freshness state and count API expose an unblock return source
  ---
  duration_ms: 1.826245
  ...
# Subtest: checklist rows report tier and rank while keeping the READY bucket null
ok 644 - checklist rows report tier and rank while keeping the READY bucket null
  ---
  duration_ms: 1.445138
  ...
# Subtest: tier, isDue, and rank cover lane rows
ok 645 - tier, isDue, and rank cover lane rows
  ---
  duration_ms: 2.29564
  ...
# Subtest: memo invalidates on a new tasks array, rollover, and frontmatter
ok 646 - memo invalidates on a new tasks array, rollover, and frontmatter
  ---
  duration_ms: 2.472258
  ...
# Subtest: the reload event fires only when the due key set changes
ok 647 - the reload event fires only when the due key set changes
  ---
  duration_ms: 2.741863
  ...
# Subtest: status bar text covers every state, and a missing host stays quiet
ok 648 - status bar text covers every state, and a missing host stays quiet
  ---
  duration_ms: 1.295723
  ...
# Subtest: status bar clicks through, falling back to rotten
ok 649 - status bar clicks through, falling back to rotten
  ---
  duration_ms: 4.61086
  ...
# Subtest: every freshness api member is synchronous and never throws
ok 650 - every freshness api member is synchronous and never throws
  ---
  duration_ms: 2.299338
  ...
# Subtest: placement vectors P1-P11, P14-P16, P18 stamp canonically
ok 651 - placement vectors P1-P11, P14-P16, P18 stamp canonically
  ---
  duration_ms: 3.171141
  ...
# Subtest: P12 set and clear refresh stamps alongside
ok 652 - P12 set and clear refresh stamps alongside
  ---
  duration_ms: 0.301756
  ...
# Subtest: P13 recurring and P17 done tasks are refused unchanged
ok 653 - P13 recurring and P17 done tasks are refused unchanged
  ---
  duration_ms: 0.172018
  ...
# Subtest: U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
ok 654 - U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
  ---
  duration_ms: 0.777183
  ...
# Subtest: reader reports misplaced and duplicate fields
ok 655 - reader reports misplaced and duplicate fields
  ---
  duration_ms: 0.334188
  ...
# Subtest: Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
ok 656 - Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
  ---
  duration_ms: 5.172171
  ...
# Subtest: Q2 tier order beats path order
ok 657 - Q2 tier order beats path order
  ---
  duration_ms: 1.205991
  ...
# Subtest: L1 lane due and stamped today
ok 658 - L1 lane due and stamped today
  ---
  duration_ms: 0.456782
  ...
# Subtest: L2 lane overrides refresh
ok 659 - L2 lane overrides refresh
  ---
  duration_ms: 0.289923
  ...
# Subtest: L3 lane exclusions have no tier
ok 660 - L3 lane exclusions have no tier
  ---
  duration_ms: 0.358904
  ...
# Subtest: L4 lane off switch and null default
ok 661 - L4 lane off switch and null default
  ---
  duration_ms: 0.229818
  ...
# Subtest: L5 lane order never stamped first
ok 662 - L5 lane order never stamped first
  ---
  duration_ms: 0.376749
  ...
# Subtest: R1 TICKLER beats older ROTTEN
ok 663 - R1 TICKLER beats older ROTTEN
  ---
  duration_ms: 0.353043
  ...
# Subtest: R2 tickler orders by due date then path and line
ok 664 - R2 tickler orders by due date then path and line
  ---
  duration_ms: 0.681992
  ...
# Subtest: missing created sorts after dated peers
ok 665 - missing created sorts after dated peers
  ---
  duration_ms: 0.953239
  ...
# Subtest: B1 upkeep counts outside the lanes
ok 666 - B1 upkeep counts outside the lanes
  ---
  duration_ms: 2.82428
  ...
# Subtest: review model meter uses upkeep and exposes refreshed
ok 667 - review model meter uses upkeep and exposes refreshed
  ---
  duration_ms: 0.389564
  ...
# Subtest: RC1 arrived: past scheduled walks RECURRING with lane and null state
ok 668 - RC1 arrived: past scheduled walks RECURRING with lane and null state
  ---
  duration_ms: 2.764397
  ...
# Subtest: RC2 arrives today: due today with zero days overdue
ok 669 - RC2 arrives today: due today with zero days overdue
  ---
  duration_ms: 0.288921
  ...
# Subtest: RC3 not yet: future scheduled walks nowhere
ok 670 - RC3 not yet: future scheduled walks nowhere
  ---
  duration_ms: 0.254195
  ...
# Subtest: RC4 due only, past: the due date is the occurrence
ok 671 - RC4 due only, past: the due date is the occurrence
  ---
  duration_ms: 0.228055
  ...
# Subtest: RC5 due only, future: walks nowhere
ok 672 - RC5 due only, future: walks nowhere
  ---
  duration_ms: 0.266118
  ...
# Subtest: RC6 earliest date wins across start and due
ok 673 - RC6 earliest date wins across start and due
  ---
  duration_ms: 0.271338
  ...
# Subtest: RC7 undated: no occurrence, no tier
ok 674 - RC7 undated: no occurrence, no tier
  ---
  duration_ms: 0.304661
  ...
# Subtest: RC8 lanes: recurring lane rows keep their lane with null state
ok 675 - RC8 lanes: recurring lane rows keep their lane with null state
  ---
  duration_ms: 0.477661
  ...
# Subtest: RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
ok 676 - RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
  ---
  duration_ms: 1.597389
  ...
# Subtest: RC10 checklist wins: a recurring chore stays in its checklist tier
ok 677 - RC10 checklist wins: a recurring chore stays in its checklist tier
  ---
  duration_ms: 0.45591
  ...
# Subtest: RC11 a stray stamp is ignored: recurring with null state
ok 678 - RC11 a stray stamp is ignored: recurring with null state
  ---
  duration_ms: 0.359466
  ...
# Subtest: RC12 order and counts: due_on, then path, then line; recurring adds no due
ok 679 - RC12 order and counts: due_on, then path, then line; recurring adds no due
  ---
  duration_ms: 1.101793
  ...
# Subtest: recurring rows adapt due and start from Tasks fields and inline fallbacks
ok 680 - recurring rows adapt due and start from Tasks fields and inline fallbacks
  ---
  duration_ms: 1.23172
  ...
# Subtest: status view counts RECURRING as a due commitment tier
ok 681 - status view counts RECURRING as a due commitment tier
  ---
  duration_ms: 0.339378
  ...
# Subtest: footer groups, entry view, and legend cover RECURRING
ok 682 - footer groups, entry view, and legend cover RECURRING
  ---
  duration_ms: 0.846065
  ...
# Subtest: a stale-stamped recurring row marks due with the resolve hint
ok 683 - a stale-stamped recurring row marks due with the resolve hint
  ---
  duration_ms: 1.145706
  ...
# Subtest: freshness namespace v12 keeps recurring and removes reference capabilities
ok 684 - freshness namespace v12 keeps recurring and removes reference capabilities
  ---
  duration_ms: 3.964166
  ...
# Subtest: hidden recurring ^ref keeps ordinary visibility (Rust parity)
ok 685 - hidden recurring ^ref keeps ordinary visibility (Rust parity)
  ---
  duration_ms: 0.830194
  ...
# Subtest: bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
ok 686 - bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
  ---
  duration_ms: 3.871308
  ...
# Subtest: day numbers stay calendar-local across a DST boundary
ok 687 - day numbers stay calendar-local across a DST boundary
  ---
  duration_ms: 0.49226
  ...
# Subtest: reviewModel shares counts, meter, tooltip, and severity
ok 688 - reviewModel shares counts, meter, tooltip, and severity
  ---
  duration_ms: 0.514121
  ...
# Subtest: memo serves warm map hits and misses use the per-row evaluator
ok 689 - memo serves warm map hits and misses use the per-row evaluator
  ---
  duration_ms: 8.377358
  ...
# Subtest: config snapshot caches the parse and invalidates explicitly
ok 690 - config snapshot caches the parse and invalidates explicitly
  ---
  duration_ms: 1.812319
  ...
# Subtest: review chips share the model with severity classes
ok 691 - review chips share the model with severity classes
  ---
  duration_ms: 1.109177
  ...
# Subtest: warm lookups reuse one snapshot without re-reading config
ok 692 - warm lookups reuse one snapshot without re-reading config
  ---
  duration_ms: 2.071283
  ...
# Subtest: same-array cache updates and Today changes rebuild the memo
ok 693 - same-array cache updates and Today changes rebuild the memo
  ---
  duration_ms: 3.200077
  ...
# Subtest: duplicate block IDs keep each row's own classification
ok 694 - duplicate block IDs keep each row's own classification
  ---
  duration_ms: 3.767942
  ...
# Subtest: line identity separates same-path rows without block IDs
ok 695 - line identity separates same-path rows without block IDs
  ---
  duration_ms: 1.455408
  ...
# Subtest: interval lookup serves the cached interval with one memo acquisition
ok 696 - interval lookup serves the cached interval with one memo acquisition
  ---
  duration_ms: 1.250085
  ...
# Subtest: S1 new through S4 overdue
ok 697 - S1 new through S4 overdue
  ---
  duration_ms: 3.172303
  ...
# Subtest: S5 task beats note, S6 note beats config, S7 config
ok 698 - S5 task beats note, S6 note beats config, S7 config
  ---
  duration_ms: 0.742186
  ...
# Subtest: S8 invalid overrides fall through with lints
ok 699 - S8 invalid overrides fall through with lints
  ---
  duration_ms: 0.392349
  ...
# Subtest: S9 malformed and S10 future stamps read as new
ok 700 - S9 malformed and S10 future stamps read as new
  ---
  duration_ms: 0.235409
  ...
# Subtest: S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
ok 701 - S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
  ---
  duration_ms: 0.333988
  ...
# Subtest: S13 out-of-scope rows read null
ok 702 - S13 out-of-scope rows read null
  ---
  duration_ms: 0.326884
  ...
# Subtest: S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
ok 703 - S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
  ---
  duration_ms: 1.383371
  ...
# Subtest: S15 counts (updated): upkeep outside the lanes drives the budget
ok 704 - S15 counts (updated): upkeep outside the lanes drives the budget
  ---
  duration_ms: 1.2416
  ...
# Subtest: config coercion keeps defaults, flags invalid, ignores unknown keys
ok 705 - config coercion keeps defaults, flags invalid, ignores unknown keys
  ---
  duration_ms: 1.396034
  ...
# Subtest: loadFreshnessConfig reads the block with plan-style injectables
ok 706 - loadFreshnessConfig reads the block with plan-style injectables
  ---
  duration_ms: 1.204348
  ...
# Subtest: interval precedence is task, note, config, default
ok 707 - interval precedence is task, note, config, default
  ---
  duration_ms: 0.269113
  ...
# Subtest: intervalForLine covers every source with its Ready fallback
ok 708 - intervalForLine covers every source with its Ready fallback
  ---
  duration_ms: 0.714273
  ...
# Subtest: project tracking stays special while reference tasks use ordinary Ready freshness
ok 709 - project tracking stays special while reference tasks use ordinary Ready freshness
  ---
  duration_ms: 3.733276
  ...
# Subtest: reference tasks match ordinary interval precedence and lane behavior
ok 710 - reference tasks match ordinary interval precedence and lane behavior
  ---
  duration_ms: 2.053719
  ...
# Subtest: obsolete reference interval keys are ignored and project config still validates
ok 711 - obsolete reference interval keys are ignored and project config still validates
  ---
  duration_ms: 0.632216
  ...
# Subtest: references use ordinary keep decisions and the nine-tier queue shape
ok 712 - references use ordinary keep decisions and the nine-tier queue shape
  ---
  duration_ms: 1.21598
  ...
# Subtest: CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
ok 713 - CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
  ---
  duration_ms: 2.41611
  ...
# Subtest: CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
ok 714 - CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
  ---
  duration_ms: 1.469524
  ...
# Subtest: freshness namespace v12 retains the tracker capability contract
ok 715 - freshness namespace v12 retains the tracker capability contract
  ---
  duration_ms: 4.036494
  ...
# Subtest: UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
ok 716 - UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
  ---
  duration_ms: 2.948818
  ...
# Subtest: UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
ok 717 - UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
  ---
  duration_ms: 0.462342
  ...
# Subtest: UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
ok 718 - UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
  ---
  duration_ms: 0.303108
  ...
# Subtest: UB11 scheduled wins a tie with the unblock date
ok 719 - UB11 scheduled wins a tie with the unblock date
  ---
  duration_ms: 0.277119
  ...
# Subtest: unblocked reader takes the latest valid duplicate and reports malformed values
ok 720 - unblocked reader takes the latest valid duplicate and reports malformed values
  ---
  duration_ms: 0.274524
  ...
# Subtest: UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
ok 721 - UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
  ---
  duration_ms: 0.525342
  ...
# Subtest: UB14 TICKLERs with the same due date sort only by path and line
ok 722 - UB14 TICKLERs with the same due date sort only by path and line
  ---
  duration_ms: 1.642284
  ...
# Subtest: UB15 a scheduled ^prj resurfaces in PROJECTS
ok 723 - UB15 a scheduled ^prj resurfaces in PROJECTS
  ---
  duration_ms: 0.199832
  ...
# Subtest: an active-note Pomodoro target still jumps and centers immediately
ok 724 - an active-note Pomodoro target still jumps and centers immediately
  ---
  duration_ms: 10.444032
  ...
# Subtest: Ctrl+9 from an unpinned daily copy switches to the pinned home tab
ok 725 - Ctrl+9 from an unpinned daily copy switches to the pinned home tab
  ---
  duration_ms: 2.841753
  ...
# Subtest: Ctrl+9 on the pinned daily tab jumps in place when a copy exists
ok 726 - Ctrl+9 on the pinned daily tab jumps in place when a copy exists
  ---
  duration_ms: 1.109307
  ...
# Subtest: Ctrl+9 switches daily copies without a Pomodoros section and stays quiet
ok 727 - Ctrl+9 switches daily copies without a Pomodoros section and stays quiet
  ---
  duration_ms: 1.133464
  ...
# Subtest: Ctrl+9 keeps the active daily tab when equal-ranked copies exist
ok 728 - Ctrl+9 keeps the active daily tab when equal-ranked copies exist
  ---
  duration_ms: 1.113295
  ...
# Subtest: Ctrl+9 from a sidebar daily copy switches to a main-area home tab
ok 729 - Ctrl+9 from a sidebar daily copy switches to a main-area home tab
  ---
  duration_ms: 0.971264
  ...
# Subtest: the first fallback press only opens daily and the second press jumps
ok 730 - the first fallback press only opens daily and the second press jumps
  ---
  duration_ms: 1.280754
  ...
# Subtest: a daily note with no target defers its notice until the second press
ok 731 - a daily note with no target defers its notice until the second press
  ---
  duration_ms: 2.147067
  ...
# Subtest: an already-open daily leaf retains its live cursor and viewport
ok 732 - an already-open daily leaf retains its live cursor and viewport
  ---
  duration_ms: 2.149011
  ...
# Subtest: a second press after reused-leaf fallback performs the Pomodoro jump
ok 733 - a second press after reused-leaf fallback performs the Pomodoro jump
  ---
  duration_ms: 1.271286
  ...
# Subtest: the standalone daily-note command activates a reused daily leaf
ok 734 - the standalone daily-note command activates a reused daily leaf
  ---
  duration_ms: 0.693884
  ...
# Subtest: Ctrl+9 loads and reuses a deferred pinned daily tab before falling back
ok 735 - Ctrl+9 loads and reuses a deferred pinned daily tab before falling back
  ---
  duration_ms: 0.764398
  ...
# Subtest: pinned daily tabs win over earlier unpinned tabs
ok 736 - pinned daily tabs win over earlier unpinned tabs
  ---
  duration_ms: 0.739411
  ...
# Subtest: a deferred sidebar daily tab is reused only without a main-area match
ok 737 - a deferred sidebar daily tab is reused only without a main-area match
  ---
  duration_ms: 0.708652
  ...
# Subtest: a deferred sidebar daily tab is reused when there is no main-area match
ok 738 - a deferred sidebar daily tab is reused when there is no main-area match
  ---
  duration_ms: 0.886281
  ...
# Subtest: a deferred non-Markdown daily path is ignored and uses the daily-note fallback
ok 739 - a deferred non-Markdown daily path is ignored and uses the daily-note fallback
  ---
  duration_ms: 0.777413
  ...
# Subtest: the standalone daily-note command reuses a deferred pinned tab
ok 740 - the standalone daily-note command reuses a deferred pinned tab
  ---
  duration_ms: 0.880792
  ...
# Subtest: Ctrl+9 opens the pinned daily tab from a non-Markdown active leaf
ok 741 - Ctrl+9 opens the pinned daily tab from a non-Markdown active leaf
  ---
  duration_ms: 0.698062
  ...
# Subtest: a closed then reopened daily note restores its in-session location
ok 742 - a closed then reopened daily note restores its in-session location
  ---
  duration_ms: 1.395182
  ...
# Subtest: different-path and invalid locations do not leak into a daily note
ok 743 - different-path and invalid locations do not leak into a daily note
  ---
  duration_ms: 0.605927
  ...
# Subtest: out-of-range remembered coordinates are clamped safely
ok 744 - out-of-range remembered coordinates are clamped safely
  ---
  duration_ms: 0.67591
  ...
# Subtest: a rapid second press cancels an older fallback restore
ok 745 - a rapid second press cancels an older fallback restore
  ---
  duration_ms: 4.438359
  ...
# Subtest: navigation and unload clean up daily scroll listeners and deferred work
ok 746 - navigation and unload clean up daily scroll listeners and deferred work
  ---
  duration_ms: 0.84913
  ...
# Subtest: crowded chip: over count is red with tooltip, aria, and names
ok 747 - crowded chip: over count is red with tooltip, aria, and names
  ---
  duration_ms: 1.693131
  ...
# Subtest: crowded chip: calm zero and unavailable dash
ok 748 - crowded chip: calm zero and unavailable dash
  ---
  duration_ms: 0.326063
  ...
# Subtest: crowded chip: names at most five notes
ok 749 - crowded chip: names at most five notes
  ---
  duration_ms: 0.355238
  ...
# Subtest: crowded chip: classes, text, aria, and arrow
ok 750 - crowded chip: classes, text, aria, and arrow
  ---
  duration_ms: 2.404148
  ...
# Subtest: crowded chip: refresh in place keeps the anchor, unload drops it
ok 751 - crowded chip: refresh in place keeps the anchor, unload drops it
  ---
  duration_ms: 0.912241
  ...
# Subtest: anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
ok 752 - anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
  ---
  duration_ms: 0.740273
  ...
# Subtest: ready-notes summary: crowded, calm, and unavailable
ok 753 - ready-notes summary: crowded, calm, and unavailable
  ---
  duration_ms: 0.355819
  ...
# Subtest: ready-notes bar: cap tick and red overflow within 30 cells
ok 754 - ready-notes bar: cap tick and red overflow within 30 cells
  ---
  duration_ms: 0.281387
  ...
# Subtest: ready-notes block: model and render with grid, pills, and footer
ok 755 - ready-notes block: model and render with grid, pills, and footer
  ---
  duration_ms: 2.123523
  ...
# Subtest: ready-notes block: unavailable renders a dash line
ok 756 - ready-notes block: unavailable renders a dash line
  ---
  duration_ms: 0.605255
  ...
# Subtest: heading matcher: fences, level, case, and first-only
ok 757 - heading matcher: fences, level, case, and first-only
  ---
  duration_ms: 1.174942
  ...
# Subtest: heading chip copy: room, full, crowded, exempt, unavailable
ok 758 - heading chip copy: room, full, crowded, exempt, unavailable
  ---
  duration_ms: 0.427475
  ...
# Subtest: heading chip key is stable for equal models
ok 759 - heading chip key is stable for equal models
  ---
  duration_ms: 0.181246
  ...
# Subtest: reading view: appends the chip to the matching h2 only
ok 760 - reading view: appends the chip to the matching h2 only
  ---
  duration_ms: 1.738828
  ...
# Subtest: reading view: no chip for ineligible notes
ok 761 - reading view: no chip for ineligible notes
  ---
  duration_ms: 0.135228
  ...
# Subtest: one live-refresh fan-out reaches every family
ok 762 - one live-refresh fan-out reaches every family
  ---
  duration_ms: 1.050685
  ...
# Subtest: ledger-tools CSS is theme-safe for the new views
ok 763 - ledger-tools CSS is theme-safe for the new views
  ---
  duration_ms: 0.759208
  ...
# Subtest: maxReadyPerNote defaults to 5 and validates 1–999
ok 764 - maxReadyPerNote defaults to 5 and validates 1–999
  ---
  duration_ms: 3.499629
  ...
# Subtest: loadPlanCaps caches on a stat key and detects edits
ok 765 - loadPlanCaps caches on a stat key and detects edits
  ---
  duration_ms: 0.758227
  ...
# Subtest: loadPlanCaps handles deletion, invalid edits, and recovery
ok 766 - loadPlanCaps handles deletion, invalid edits, and recovery
  ---
  duration_ms: 0.787123
  ...
# Subtest: loadPlanCaps without statSync reads through uncached
ok 767 - loadPlanCaps without statSync reads through uncached
  ---
  duration_ms: 0.441523
  ...
# Subtest: noteFrontmatter resolves through getFileCache, not getCache
ok 768 - noteFrontmatter resolves through getFileCache, not getCache
  ---
  duration_ms: 1.042229
  ...
# Subtest: task_refresh applies through the shared reader
ok 769 - task_refresh applies through the shared reader
  ---
  duration_ms: 4.78958
  ...
# Subtest: noteReadyKindFromType covers every R11 form
ok 770 - noteReadyKindFromType covers every R11 form
  ---
  duration_ms: 0.599754
  ...
# Subtest: noteReadyStatusLabel mirrors ProjectStatus::parse
ok 771 - noteReadyStatusLabel mirrors ProjectStatus::parse
  ---
  duration_ms: 0.334168
  ...
# Subtest: noteReadyParentStem strips alias, heading, and path
ok 772 - noteReadyParentStem strips alias, heading, and path
  ---
  duration_ms: 0.403049
  ...
# Subtest: parseNoteReadyCap covers every R8 form
ok 773 - parseNoteReadyCap covers every R8 form
  ---
  duration_ms: 0.841135
  ...
# Subtest: R1: 6 tasks at the default cap are crowded with over_by 1
ok 774 - R1: 6 tasks at the default cap are crowded with over_by 1
  ---
  duration_ms: 10.985174
  ...
# Subtest: R2: 5 tasks are full with no lint
ok 775 - R2: 5 tasks are full with no lint
  ---
  duration_ms: 5.693286
  ...
# Subtest: R3: hidden, future, blocked, and non-TODO rows never count
ok 776 - R3: hidden, future, blocked, and non-TODO rows never count
  ---
  duration_ms: 4.022486
  ...
# Subtest: R4: make-up splits 1 ready + 1 new + 1 rotten
ok 777 - R4: make-up splits 1 ready + 1 new + 1 rotten
  ---
  duration_ms: 2.788491
  ...
# Subtest: R5: recurring rows are excluded but tallied
ok 778 - R5: recurring rows are excluded but tallied
  ---
  duration_ms: 1.784967
  ...
# Subtest: R6: a visible ^prj task never counts
ok 779 - R6: a visible ^prj task never counts
  ---
  duration_ms: 1.381747
  ...
# Subtest: R7: daily, untyped, template, done, and dash rows are absent
ok 780 - R7: daily, untyped, template, done, and dash rows are absent
  ---
  duration_ms: 2.209267
  ...
# Subtest: R8: ready_cap forms map to cap, exempt, or lint-then-default
ok 781 - R8: ready_cap forms map to cap, exempt, or lint-then-default
  ---
  duration_ms: 4.279116
  ...
# Subtest: R9: a parent with two children counts 3
ok 782 - R9: a parent with two children counts 3
  ---
  duration_ms: 4.440134
  ...
# Subtest: R10: terminal projects are not capped and lint once
ok 783 - R10: terminal projects are not capped and lint once
  ---
  duration_ms: 2.487297
  ...
# Subtest: R11: every type form and nested folders are eligible
ok 784 - R11: every type form and nested folders are eligible
  ---
  duration_ms: 1.766921
  ...
# Subtest: R12: stamping a NEW task keeps the count and moves the make-up
ok 785 - R12: stamping a NEW task keeps the count and moves the make-up
  ---
  duration_ms: 3.140894
  ...
# Subtest: R13: a Today-linked task still counts
ok 786 - R13: a Today-linked task still counts
  ---
  duration_ms: 0.966133
  ...
# Subtest: R14: max_ready_per_note 3 caps others while ready_cap 8 holds
ok 787 - R14: max_ready_per_note 3 caps others while ready_cap 8 holds
  ---
  duration_ms: 3.744927
  ...
# Subtest: api.noteReady is frozen at version 1 under api v3
ok 788 - api.noteReady is frozen at version 1 under api v3
  ---
  duration_ms: 0.488683
  ...
# Subtest: counted and inCrowdedNote resolve per task
ok 789 - counted and inCrowdedNote resolve per task
  ---
  duration_ms: 2.74531
  ...
# Subtest: groupLabel ranks crowded notes by excess
ok 790 - groupLabel ranks crowded notes by excess
  ---
  duration_ms: 9.373028
  ...
# Subtest: snapshot sorts crowded, full, room, empty, exempt and splits totals
ok 791 - snapshot sorts crowded, full, room, empty, exempt and splits totals
  ---
  duration_ms: 6.244316
  ...
# Subtest: missing Tasks data and a cold cache are unavailable, never zero
ok 792 - missing Tasks data and a cold cache are unavailable, never zero
  ---
  duration_ms: 1.443184
  ...
# Subtest: throwing Tasks guards never throw
ok 793 - throwing Tasks guards never throw
  ---
  duration_ms: 0.815757
  ...
# Subtest: snapshot reuses the memo without reparsing or re-walking
ok 794 - snapshot reuses the memo without reparsing or re-walking
  ---
  duration_ms: 1.108957
  ...
# Subtest: a task edit rebuilds through the cache-update handler
ok 795 - a task edit rebuilds through the cache-update handler
  ---
  duration_ms: 1.261878
  ...
# Subtest: a ready_cap edit rebuilds and fires the query-refresh trigger
ok 796 - a ready_cap edit rebuilds and fires the query-refresh trigger
  ---
  duration_ms: 1.034775
  ...
# Subtest: rename and delete move the eligibility entry
ok 797 - rename and delete move the eligibility entry
  ---
  duration_ms: 1.175854
  ...
# Subtest: day rollover rebuilds the snapshot date
ok 798 - day rollover rebuilds the snapshot date
  ---
  duration_ms: 0.910567
  ...
# Subtest: a config edit flows through the stat cache
ok 799 - a config edit flows through the stat cache
  ---
  duration_ms: 1.935172
  ...
# Subtest: untyped and non-markdown vault events are no-ops
ok 800 - untyped and non-markdown vault events are no-ops
  ---
  duration_ms: 0.981904
  ...
# Subtest: memo hits never re-walk the vault
ok 801 - memo hits never re-walk the vault
  ---
  duration_ms: 62.755753
  ...
# Subtest: the startup storm is linear
ok 802 - the startup storm is linear
  ---
  duration_ms: 30.82657
  ...
# Subtest: the first resolved event forces one rebuild and later ones do not
ok 803 - the first resolved event forces one rebuild and later ones do not
  ---
  duration_ms: 1.900587
  ...
# Subtest: noteReadyEvaluate is pure and mirrors the Rust totals
ok 804 - noteReadyEvaluate is pure and mirrors the Rust totals
  ---
  duration_ms: 0.378502
  ...
# Subtest: conformance: merged name with duplicate
ok 805 - conformance: merged name with duplicate
  ---
  duration_ms: 5.581211
  ...
# Subtest: conformance: link forms and exclusions
ok 806 - conformance: link forms and exclusions
  ---
  duration_ms: 1.101762
  ...
# Subtest: conformance: unnamed placeholders
ok 807 - conformance: unnamed placeholders
  ---
  duration_ms: 0.48238
  ...
# Subtest: conformance: subheading in the section
ok 808 - conformance: subheading in the section
  ---
  duration_ms: 0.322395
  ...
# Subtest: conformance: open inventory label
ok 809 - conformance: open inventory label
  ---
  duration_ms: 0.427135
  ...
# Subtest: conformance: over the cap
ok 810 - conformance: over the cap
  ---
  duration_ms: 0.290996
  ...
# Subtest: conformance: cancelled and completed entries
ok 811 - conformance: cancelled and completed entries
  ---
  duration_ms: 0.354536
  ...
# Subtest: exactly at the cap is fine
ok 812 - exactly at the cap is fine
  ---
  duration_ms: 0.268182
  ...
# Subtest: no Pomodoros section degrades to an empty budget
ok 813 - no Pomodoros section degrades to an empty budget
  ---
  duration_ms: 0.653878
  ...
# Subtest: fenced code never counts
ok 814 - fenced code never counts
  ---
  duration_ms: 1.397136
  ...
# Subtest: highlight is the first open non-exempt entry; running is the timed one
ok 815 - highlight is the first open non-exempt entry; running is the timed one
  ---
  duration_ms: 0.504823
  ...
# Subtest: coercePlanCaps ignores a legacy max_now instead of failing
ok 816 - coercePlanCaps ignores a legacy max_now instead of failing
  ---
  duration_ms: 0.401296
  ...
# Subtest: parsePlanCaps defaults, overrides, and invalid fallbacks
ok 817 - parsePlanCaps defaults, overrides, and invalid fallbacks
  ---
  duration_ms: 0.427426
  ...
# Subtest: loadPlanCaps falls back to defaults without fs
ok 818 - loadPlanCaps falls back to defaults without fs
  ---
  duration_ms: 0.617007
  ...
# Subtest: loadPlanCaps falls back to defaults on mobile
ok 819 - loadPlanCaps falls back to defaults on mobile
  ---
  duration_ms: 0.316715
  ...
# Subtest: loadPlanCaps reads plan: and flags invalid values
ok 820 - loadPlanCaps reads plan: and flags invalid values
  ---
  duration_ms: 0.547746
  ...
# Subtest: planBlockTargetPath prefers the containing daily note
ok 821 - planBlockTargetPath prefers the containing daily note
  ---
  duration_ms: 1.00113
  ...
# Subtest: planBlockModel degrades to placeholders, never an error
ok 822 - planBlockModel degrades to placeholders, never an error
  ---
  duration_ms: 1.237822
  ...
# Subtest: planBlockModel renders chips, themes, and lints
ok 823 - planBlockModel renders chips, themes, and lints
  ---
  duration_ms: 1.31506
  ...
# Subtest: planBlockModel adds lane cap lints when a lane is over
ok 824 - planBlockModel adds lane cap lints when a lane is over
  ---
  duration_ms: 0.905017
  ...
# Subtest: plugin exposes the versioned api and registers the bob-plan block
ok 825 - plugin exposes the versioned api and registers the bob-plan block
  ---
  duration_ms: 7.593372
  ...
# Subtest: invalid plan block falls back to full defaults
ok 826 - invalid plan block falls back to full defaults
  ---
  duration_ms: 0.376548
  ...
# Subtest: entries require column-0 dash-space with one status char
ok 827 - entries require column-0 dash-space with one status char
  ---
  duration_ms: 0.26218
  ...
# Subtest: crlf line endings split like lf
ok 828 - crlf line endings split like lf
  ---
  duration_ms: 1.781079
  ...
# Subtest: conformance: empty target means the daily note
ok 829 - conformance: empty target means the daily note
  ---
  duration_ms: 0.263663
  ...
# Subtest: lane predicate matches hide subtags, case, and non-task
ok 830 - lane predicate matches hide subtags, case, and non-task
  ---
  duration_ms: 0.325471
  ...
# Subtest: planBlockModel daily badges follow dashboard section counts
ok 831 - planBlockModel daily badges follow dashboard section counts
  ---
  duration_ms: 2.692458
  ...
# Subtest: planBlockModel keeps a supplied unavailable dashboard budget
ok 832 - planBlockModel keeps a supplied unavailable dashboard budget
  ---
  duration_ms: 0.506546
  ...
# Subtest: work tones: TODAY override and unavailable stay neutral in planBlockModel
ok 833 - work tones: TODAY override and unavailable stay neutral in planBlockModel
  ---
  duration_ms: 0.301415
  ...
# Subtest: shared vector: rollup-archive-review
ok 834 - shared vector: rollup-archive-review
  ---
  duration_ms: 6.253354
  ...
# Subtest: shared vector: review-decisions
ok 835 - shared vector: review-decisions
  ---
  duration_ms: 1.552403
  ...
# Subtest: shared vector: resolution-and-lints
ok 836 - shared vector: resolution-and-lints
  ---
  duration_ms: 1.986941
  ...
# Subtest: shared vector: chips, forecast shares, empty forecasts, and session identity
ok 837 - shared vector: chips, forecast shares, empty forecasts, and session identity
  ---
  duration_ms: 1.138272
  ...
# Subtest: shared vector: split-rounding-and-duration
ok 838 - shared vector: split-rounding-and-duration
  ---
  duration_ms: 1.882863
  ...
# Subtest: shared vector: share-rounding
ok 839 - shared vector: share-rounding
  ---
  duration_ms: 0.403651
  ...
# Subtest: shared vector: daily-review-link
ok 840 - shared vector: daily-review-link
  ---
  duration_ms: 0.344968
  ...
# Subtest: shared vector: rollup-depth-and-parent-shapes
ok 841 - shared vector: rollup-depth-and-parent-shapes
  ---
  duration_ms: 1.172147
  ...
# Subtest: shared vector: unresolved-and-closed-zero
ok 842 - shared vector: unresolved-and-closed-zero
  ---
  duration_ms: 1.081684
  ...
# Subtest: shared vector: parent-scalar-shapes
ok 843 - shared vector: parent-scalar-shapes
  ---
  duration_ms: 0.632366
  ...
# Subtest: dedicated link parser keeps embeds and one struck link, but rejects prose
ok 844 - dedicated link parser keeps embeds and one struck link, but rejects prose
  ---
  duration_ms: 0.22015
  ...
# Subtest: FNV-1a fallback for job maps to the pinned magenta slot
ok 845 - FNV-1a fallback for job maps to the pinned magenta slot
  ---
  duration_ms: 0.112315
  ...
# Subtest: rollup and area-color lints are reported once per note
ok 846 - rollup and area-color lints are reported once per note
  ---
  duration_ms: 0.379966
  ...
# Subtest: chip DOM exposes forecast, hue, accessible text, and tooltip
ok 847 - chip DOM exposes forecast, hue, accessible text, and tooltip
  ---
  duration_ms: 0.232694
  ...
# Subtest: Reading view appends a forecast chip before its Task Link list
ok 848 - Reading view appends a forecast chip before its Task Link list
  ---
  duration_ms: 5.570331
  ...
# Subtest: Live Preview places a chip widget at the end of the Pomodoro line
ok 849 - Live Preview places a chip widget at the end of the Pomodoro line
  ---
  duration_ms: 0.962166
  ...
# Subtest: Live Preview skips chips in Source mode
ok 850 - Live Preview skips chips in Source mode
  ---
  duration_ms: 0.234167
  ...
# Subtest: Reading view finds embedded Task Links via src
ok 851 - Reading view finds embedded Task Links via src
  ---
  duration_ms: 0.597941
  ...
# Subtest: Obsidian frontmatter shapes unwrap nested wikilink arrays
ok 852 - Obsidian frontmatter shapes unwrap nested wikilink arrays
  ---
  duration_ms: 0.207887
  ...
# Subtest: parser accepts the PM1-PM5 conformance vectors verbatim
ok 853 - parser accepts the PM1-PM5 conformance vectors verbatim
  ---
  duration_ms: 1.820174
  ...
# Subtest: parser rejects the PM7-PM12 conformance vectors verbatim
ok 854 - parser rejects the PM7-PM12 conformance vectors verbatim
  ---
  duration_ms: 0.268863
  ...
# Subtest: PM6 with the ladder unknown omits P-labels instead of guessing
ok 855 - PM6 with the ladder unknown omits P-labels instead of guessing
  ---
  duration_ms: 0.199491
  ...
# Subtest: PM13-PM17 ladder and line variants hold
ok 856 - PM13-PM17 ladder and line variants hold
  ---
  duration_ms: 0.321764
  ...
# Subtest: no model output contains a double colon
ok 857 - no model output contains a double colon
  ---
  duration_ms: 0.780639
  ...
# Subtest: element structure and the decorative/inheritColor options
ok 858 - element structure and the decorative/inheritColor options
  ---
  duration_ms: 0.338105
  ...
# Subtest: Live Preview decorations fold space, reveal, and refuse
ok 859 - Live Preview decorations fold space, reveal, and refuse
  ---
  duration_ms: 1.422073
  ...
# Subtest: a line with fresh and priority fields gets a disjoint decoration
ok 860 - a line with fresh and priority fields gets a disjoint decoration
  ---
  duration_ms: 0.205632
  ...
# Subtest: widget mousedown reveals the field at the folded offset
ok 861 - widget mousedown reveals the field at the folded offset
  ---
  duration_ms: 0.612719
  ...
# Subtest: rendered views split task nodes and skip exclusions
ok 862 - rendered views split task nodes and skip exclusions
  ---
  duration_ms: 1.465587
  ...
# Subtest: ladder coercion is lenient: valid, partial, and unknown
ok 863 - ladder coercion is lenient: valid, partial, and unknown
  ---
  duration_ms: 0.471921
  ...
# Subtest: ladder snapshot reads the file and reuses the cache
ok 864 - ladder snapshot reads the file and reuses the cache
  ---
  duration_ms: 2.045956
  ...
# Subtest: ladder snapshot degrades on missing files and parse errors
ok 865 - ladder snapshot degrades on missing files and parse errors
  ---
  duration_ms: 0.912131
  ...
# Subtest: ladder snapshot is unknown on mobile
ok 866 - ladder snapshot is unknown on mobile
  ---
  duration_ms: 19.089579
  ...
# Subtest: api.priorityMarks v1 is additive, sync, and never throwing
ok 867 - api.priorityMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 5.463668
  ...
# Subtest: session toggle and onload wiring
ok 868 - session toggle and onload wiring
  ---
  duration_ms: 0.887173
  ...
# Subtest: styles.css contract: masks, both hosts, repair flag, resting
ok 869 - styles.css contract: masks, both hosts, repair flag, resting
  ---
  duration_ms: 0.746124
  ...
# Subtest: P1/P3/P4: open entries mark plain and aliased links
ok 870 - P1/P3/P4: open entries mark plain and aliased links
  ---
  duration_ms: 2.205349
  ...
# Subtest: P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
ok 871 - P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
  ---
  duration_ms: 2.119725
  ...
# Subtest: P5: closed entries never mark, even with 🍅 history
ok 872 - P5: closed entries never mark, even with 🍅 history
  ---
  duration_ms: 0.57598
  ...
# Subtest: P6/P7: embedded and struck links never mark
ok 873 - P6/P7: embedded and struck links never mark
  ---
  duration_ms: 0.226342
  ...
# Subtest: P8: both trailing-\# move-only forms mark
ok 874 - P8: both trailing-\# move-only forms mark
  ---
  duration_ms: 0.242663
  ...
# Subtest: P9: nested and prose-mixed links never mark
ok 875 - P9: nested and prose-mixed links never mark
  ---
  duration_ms: 0.164284
  ...
# Subtest: P10: fenced, off-section, and off-note links never mark
ok 876 - P10: fenced, off-section, and off-note links never mark
  ---
  duration_ms: 0.416344
  ...
# Subtest: P11: unresolved targets and non-task blocks get no mark
ok 877 - P11: unresolved targets and non-task blocks get no mark
  ---
  duration_ms: 0.477692
  ...
# Subtest: P13: a same-note target reads the live doc
ok 878 - P13: a same-note target reads the live doc
  ---
  duration_ms: 0.757626
  ...
# Subtest: P14: expect() wins until the cache agrees or 4 s pass
ok 879 - P14: expect() wins until the cache agrees or 4 s pass
  ---
  duration_ms: 0.943571
  ...
# Subtest: tooltip, element structure, and eq
ok 880 - tooltip, element structure, and eq
  ---
  duration_ms: 0.291036
  ...
# Subtest: Live Preview places one widget at each In Progress link
ok 881 - Live Preview places one widget at each In Progress link
  ---
  duration_ms: 0.499092
  ...
# Subtest: widget mousedown places the cursor at the link start
ok 882 - widget mousedown places the cursor at the link start
  ---
  duration_ms: 0.378863
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
ok 883 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 0.470578
  ...
# Subtest: Reading view marks In Progress rows and dedupes
ok 884 - Reading view marks In Progress rows and dedupes
  ---
  duration_ms: 1.232783
  ...
# Subtest: Reading view refuses every non-mark row
ok 885 - Reading view refuses every non-mark row
  ---
  duration_ms: 1.063209
  ...
# Subtest: Reading view allows the 🍅 prefix and the trailing \# marker
ok 886 - Reading view allows the 🍅 prefix and the trailing \# marker
  ---
  duration_ms: 0.341832
  ...
# Subtest: api.progressMarks v1 is additive, sync, and never throwing
ok 887 - api.progressMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.711437
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 888 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 0.94329
  ...
# Subtest: changed-file and rollover refreshes
ok 889 - changed-file and rollover refreshes
  ---
  duration_ms: 2.200439
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 890 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.119218
  ...
# Subtest: styles.css contract: glyph, box, motion, toggle, calm
ok 891 - styles.css contract: glyph, box, motion, toggle, calm
  ---
  duration_ms: 0.762034
  ...
# Subtest: the board registers its code block processor and the Open Reading Board command
ok 892 - the board registers its code block processor and the Open Reading Board command
  ---
  duration_ms: 5.796382
  ...
# Subtest: four lanes render with counts, list and listitem roles, and one hint
ok 893 - four lanes render with counts, list and listitem roles, and one hint
  ---
  duration_ms: 17.793026
  ...
# Subtest: awake cards show kind, topic, added mark, counts, priority, and the pending-sync star
ok 894 - awake cards show kind, topic, added mark, counts, priority, and the pending-sync star
  ---
  duration_ms: 6.054775
  ...
# Subtest: a path-valued Bob audio field produces exactly one visible music marker
ok 895 - a path-valued Bob audio field produces exactly one visible music marker
  ---
  duration_ms: 4.10305
  ...
# Subtest: Snoozed shows Waking, date groups, and Waiting-on rows with their reasons
ok 896 - Snoozed shows Waking, date groups, and Waiting-on rows with their reasons
  ---
  duration_ms: 4.472915
  ...
# Subtest: TODAY pills float linked cards first, and never appear without a ready Today cache
ok 897 - TODAY pills float linked cards first, and never appear without a ready Today cache
  ---
  duration_ms: 5.802485
  ...
# Subtest: the PDF button needs the nav member, macOS, and a source_pdf
ok 898 - the PDF button needs the nav member, macOS, and a source_pdf
  ---
  duration_ms: 12.783847
  ...
# Subtest: click, modifier-click, middle-click, and the Task button route to openLinkText
ok 899 - click, modifier-click, middle-click, and the Task button route to openLinkText
  ---
  duration_ms: 2.107402
  ...
# Subtest: the board is one Tab stop and every key moves or acts
ok 900 - the board is one Tab stop and every key moves or acts
  ---
  duration_ms: 17.70087
  ...
# Subtest: movement targets stay inside the lanes that show cards
ok 901 - movement targets stay inside the lanes that show cards
  ---
  duration_ms: 0.601168
  ...
# Subtest: hovering a Waiting-on row outlines its prerequisite card on the board
ok 902 - hovering a Waiting-on row outlines its prerequisite card on the board
  ---
  duration_ms: 2.000879
  ...
# Subtest: the board never calls a vault write API, in the source or in any gesture
ok 903 - the board never calls a vault write API, in the source or in any gesture
  ---
  duration_ms: 11.113258
  ...
# Subtest: a repaint keeps focus by note path and each lane's scroll position
ok 904 - a repaint keeps focus by note path and each lane's scroll position
  ---
  duration_ms: 3.124022
  ...
# Subtest: a task move and topic/type update repaint handlers while preserving focus and scroll
ok 905 - a task move and topic/type update repaint handlers while preserving focus and scroll
  ---
  duration_ms: 3.964485
  ...
# Subtest: prerequisite identity changes repaint highlighting even when reason text is unchanged
ok 906 - prerequisite identity changes repaint highlighting even when reason text is unchanged
  ---
  duration_ms: 3.443642
  ...
# Subtest: an unchanged board is not repainted; only the data time updates in place
ok 907 - an unchanged board is not repainted; only the data time updates in place
  ---
  duration_ms: 3.89842
  ...
# Subtest: a Today cache change repaints boards from cached data without spawning bob
ok 908 - a Today cache change repaints boards from cached data without spawning bob
  ---
  duration_ms: 4.75815
  ...
# Subtest: first paint is a skeleton in the real grid, then the board without a layout jump
ok 909 - first paint is a skeleton in the real grid, then the board without a layout jump
  ---
  duration_ms: 7.730413
  ...
# Subtest: failures without a frame render an actionable card with Retry
ok 910 - failures without a frame render an actionable card with Retry
  ---
  duration_ms: 19.750221
  ...
# Subtest: a failed manual refresh keeps the last frame and says why with Retry
ok 911 - a failed manual refresh keeps the last frame and says why with Retry
  ---
  duration_ms: 9.441058
  ...
# Subtest: metadata revalidation delivers a silent stale-frame error and recovery updates freshness
ok 912 - metadata revalidation delivers a silent stale-frame error and recovery updates freshness
  ---
  duration_ms: 12.821438
  ...
# Subtest: stale-cache mount refresh failures reach the mounted view
ok 913 - stale-cache mount refresh failures reach the mounted view
  ---
  duration_ms: 8.553134
  ...
# Subtest: unload during a fetch prevents late repaint and queued spawns
ok 914 - unload during a fetch prevents late repaint and queued spawns
  ---
  duration_ms: 4.326787
  ...
# Subtest: in-flight edits and forced refreshes coalesce without dropping mounted fences
ok 915 - in-flight edits and forced refreshes coalesce without dropping mounted fences
  ---
  duration_ms: 19.652025
  ...
# Subtest: manual refresh shows a busy state until the result lands, then announces it
ok 916 - manual refresh shows a busy state until the result lands, then announces it
  ---
  duration_ms: 5.487101
  ...
# Subtest: an older bob without blocked_by falls back to Waiting-on with one lint line
ok 917 - an older bob without blocked_by falls back to Waiting-on with one lint line
  ---
  duration_ms: 4.133229
  ...
# Subtest: an empty queue shows bob's own phrase instead of lanes
ok 918 - an empty queue shows bob's own phrase instead of lanes
  ---
  duration_ms: 1.21045
  ...
# Subtest: fence options reach the fetch and bad options show as muted lint lines
ok 919 - fence options reach the fetch and bad options show as muted lint lines
  ---
  duration_ms: 11.764291
  ...
# Subtest: Snoozed collapses per source path, leaves the key order, and survives repaints
ok 920 - Snoozed collapses per source path, leaves the key order, and survives repaints
  ---
  duration_ms: 9.372285
  ...
# Subtest: unloading a block releases its view, and teardown clears the session state
ok 921 - unloading a block releases its view, and teardown clears the session state
  ---
  duration_ms: 2.150474
  ...
# Subtest: reading board stylesheet contract: selectors, layout, tabular-nums, motion, colors
ok 922 - reading board stylesheet contract: selectors, layout, tabular-nums, motion, colors
  ---
  duration_ms: 0.876533
  ...
# Subtest: Reading Board argv carries bob's fixed queue and optional fence filters
ok 923 - Reading Board argv carries bob's fixed queue and optional fence filters
  ---
  duration_ms: 1.620373
  ...
# Subtest: Reading Board decoder accepts the shared bob fixture and normalizes optional fields
ok 924 - Reading Board decoder accepts the shared bob fixture and normalizes optional fields
  ---
  duration_ms: 0.272951
  ...
# Subtest: Reading Board audio presence survives raw JSON decoding and model construction
ok 925 - Reading Board audio presence survives raw JSON decoding and model construction
  ---
  duration_ms: 5.618883
  ...
# Subtest: Reading Board decoder rejects malformed JSON, shapes, schema, and bob errors
ok 926 - Reading Board decoder rejects malformed JSON, shapes, schema, and bob errors
  ---
  duration_ms: 0.310062
  ...
# Subtest: shared bob spawn passes the vault environment, timeout, and buffer
ok 927 - shared bob spawn passes the vault environment, timeout, and buffer
  ---
  duration_ms: 6.878166
  ...
# Subtest: shared bob spawn maps missing binary and timeout failures
ok 928 - shared bob spawn maps missing binary and timeout failures
  ---
  duration_ms: 2.277586
  ...
# Subtest: Reading Board error cards explain not-found, timeout, schema, and bob errors
ok 929 - Reading Board error cards explain not-found, timeout, schema, and bob errors
  ---
  duration_ms: 0.490275
  ...
# Subtest: Reading Board cache returns stale data while revalidating and keeps a four-entry LRU
ok 930 - Reading Board cache returns stale data while revalidating and keeps a four-entry LRU
  ---
  duration_ms: 1.416212
  ...
# Subtest: Reading Board shares identical flights and coalesces one different follow-up
ok 931 - Reading Board shares identical flights and coalesces one different follow-up
  ---
  duration_ms: 1.131489
  ...
# Subtest: Reading Board refresh is mounted-only, debounced, and reacts to rollover and stale active leaves
ok 932 - Reading Board refresh is mounted-only, debounced, and reacts to rollover and stale active leaves
  ---
  duration_ms: 0.714593
  ...
# Subtest: the shared bob output builds the expected four lanes and preserves bob order
ok 933 - the shared bob output builds the expected four lanes and preserves bob order
  ---
  duration_ms: 4.424975
  ...
# Subtest: each status uses its awake lane and every blocked status uses Snoozed
ok 934 - each status uses its awake lane and every blocked status uses Snoozed
  ---
  duration_ms: 0.474876
  ...
# Subtest: Today floats cards by ledger rank only when the cache is ready
ok 935 - Today floats cards by ledger rank only when the cache is ready
  ---
  duration_ms: 1.361469
  ...
# Subtest: Snoozed groups show waking, schedule, dependency, project, return lane, and mark models
ok 936 - Snoozed groups show waking, schedule, dependency, project, return lane, and mark models
  ---
  duration_ms: 0.668766
  ...
# Subtest: schedule groups follow Monday-start weeks through Sunday across month and year ends
ok 937 - schedule groups follow Monday-start weeks through Sunday across month and year ends
  ---
  duration_ms: 0.284543
  ...
# Subtest: older bob output remains visible in Waiting on and explains the missing reasons
ok 938 - older bob output remains visible in Waiting on and explains the missing reasons
  ---
  duration_ms: 1.204138
  ...
# Subtest: fence options accept parent and type lists while turning bad input into lints
ok 939 - fence options accept parent and type lists while turning bad input into lints
  ---
  duration_ms: 1.347412
  ...
# Subtest: kind names, title code spans, and render signatures are deterministic
ok 940 - kind names, title code spans, and render signatures are deterministic
  ---
  duration_ms: 5.387803
  ...
# Subtest: max_ready defaults to 100 for missing, absent, and null values
ok 941 - max_ready defaults to 100 for missing, absent, and null values
  ---
  duration_ms: 2.186302
  ...
# Subtest: max_ready accepts a custom positive cap
ok 942 - max_ready accepts a custom positive cap
  ---
  duration_ms: 0.29835
  ...
# Subtest: max_ready rejects zero, negative, fractions, strings, booleans, and overflow
ok 943 - max_ready rejects zero, negative, fractions, strings, booleans, and overflow
  ---
  duration_ms: 1.32023
  ...
# Subtest: old configurations and legacy max_now still load
ok 944 - old configurations and legacy max_now still load
  ---
  duration_ms: 0.376128
  ...
# Subtest: READY boundary: only a strict excess turns red
ok 945 - READY boundary: only a strict excess turns red
  ---
  duration_ms: 2.945701
  ...
# Subtest: READY custom-cap boundary
ok 946 - READY custom-cap boundary
  ---
  duration_ms: 0.355669
  ...
# Subtest: READY over is independent of the PLAN ledger status
ok 947 - READY over is independent of the PLAN ledger status
  ---
  duration_ms: 7.816367
  ...
# Subtest: READY predicate: statuses, custom TODO symbols, and non-tasks
ok 948 - READY predicate: statuses, custom TODO symbols, and non-tasks
  ---
  duration_ms: 0.279955
  ...
# Subtest: READY predicate: blocked uses the full list, even outside the queue
ok 949 - READY predicate: blocked uses the full list, even outside the queue
  ---
  duration_ms: 0.596539
  ...
# Subtest: READY predicate: past, today, and future schedules
ok 950 - READY predicate: past, today, and future schedules
  ---
  duration_ms: 0.573274
  ...
# Subtest: READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
ok 951 - READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
  ---
  duration_ms: 0.414962
  ...
# Subtest: READY predicate: Today exclusion
ok 952 - READY predicate: Today exclusion
  ---
  duration_ms: 0.180154
  ...
# Subtest: readyTaskVisible excludes hide variants like Tasks
ok 953 - readyTaskVisible excludes hide variants like Tasks
  ---
  duration_ms: 0.174152
  ...
# Subtest: daily and dashboard share the READY element contract
ok 954 - daily and dashboard share the READY element contract
  ---
  duration_ms: 15.616192
  ...
# Subtest: READY placeholder keeps the limit in its tooltip
ok 955 - READY placeholder keeps the limit in its tooltip
  ---
  duration_ms: 0.201084
  ...
# Subtest: READY keyboard and modifier-key navigation
ok 956 - READY keyboard and modifier-key navigation
  ---
  duration_ms: 1.206001
  ...
# Subtest: READY unavailable without Tasks, on Cold/Initializing, or before Today
ok 957 - READY unavailable without Tasks, on Cold/Initializing, or before Today
  ---
  duration_ms: 2.750379
  ...
# Subtest: READY counts a valid empty queue as zero, not unavailable
ok 958 - READY counts a valid empty queue as zero, not unavailable
  ---
  duration_ms: 1.111482
  ...
# Subtest: READY stays compatible with hosts exposing only getTasks()
ok 959 - READY stays compatible with hosts exposing only getTasks()
  ---
  duration_ms: 2.42588
  ...
# Subtest: READY degrades to unavailable when the Today predicate throws
ok 960 - READY degrades to unavailable when the Today predicate throws
  ---
  duration_ms: 0.539629
  ...
# Subtest: READY renders label/value spans for every budget state
ok 961 - READY renders label/value spans for every budget state
  ---
  duration_ms: 1.131239
  ...
# Subtest: READY live refresh keeps the anchor, spans, and handlers
ok 962 - READY live refresh keeps the anchor, spans, and handlers
  ---
  duration_ms: 1.209829
  ...
# Subtest: READY refresh crosses the over-cap boundary and back
ok 963 - READY refresh crosses the over-cap boundary and back
  ---
  duration_ms: 0.59759
  ...
# Subtest: READY refresh crosses the unavailable boundary and back
ok 964 - READY refresh crosses the unavailable boundary and back
  ---
  duration_ms: 0.593783
  ...
# Subtest: READY never assigns the Obsidian text setter
ok 965 - READY never assigns the Obsidian text setter
  ---
  duration_ms: 2.782049
  ...
# Subtest: READY gating excludes review buckets and keeps the partition
ok 966 - READY gating excludes review buckets and keeps the partition
  ---
  duration_ms: 0.328868
  ...
# Subtest: gated READY tooltip carries total lane pressure
ok 967 - gated READY tooltip carries total lane pressure
  ---
  duration_ms: 0.114358
  ...
# Subtest: planBlockModel gates READY and shares the lane tooltip
ok 968 - planBlockModel gates READY and shares the lane tooltip
  ---
  duration_ms: 0.625494
  ...
# Subtest: READY lint appears only on a strict excess
ok 969 - READY lint appears only on a strict excess
  ---
  duration_ms: 3.754115
  ...
# Subtest: READY lint uses a custom cap
ok 970 - READY lint uses a custom cap
  ---
  duration_ms: 0.656713
  ...
# Subtest: lane lints appear in NEXT, PENDING, READY order
ok 971 - lane lints appear in NEXT, PENDING, READY order
  ---
  duration_ms: 1.926476
  ...
# Subtest: READY lint uses the gated count
ok 972 - READY lint uses the gated count
  ---
  duration_ms: 1.630371
  ...
# Subtest: READY lint stays silent while unavailable
ok 973 - READY lint stays silent while unavailable
  ---
  duration_ms: 0.449718
  ...
# Subtest: READY speaks each host's chip language (daily single-tone, dash two-tone)
ok 974 - READY speaks each host's chip language (daily single-tone, dash two-tone)
  ---
  duration_ms: 2.817577
  ...
# Subtest: daily paint carries lane pressure to the shared READY renderer
ok 975 - daily paint carries lane pressure to the shared READY renderer
  ---
  duration_ms: 20.668774
  ...
# Subtest: daily paint degrades to the legacy tooltip without freshness
ok 976 - daily paint degrades to the legacy tooltip without freshness
  ---
  duration_ms: 2.60944
  ...
# Subtest: work tones: READY model carries the displayed-count tone
ok 977 - work tones: READY model carries the displayed-count tone
  ---
  duration_ms: 0.245619
  ...
# Subtest: recurrence helpers are exported and frozen where shaped
ok 978 - recurrence helpers are exported and frozen where shaped
  ---
  duration_ms: 2.187955
  ...
# Subtest: RM1 daily with when done: fold, label, tooltip
ok 979 - RM1 daily with when done: fold, label, tooltip
  ---
  duration_ms: 1.182116
  ...
# Subtest: RM2 non-checklist row without when done still marks
ok 980 - RM2 non-checklist row without when done still marks
  ---
  duration_ms: 0.746535
  ...
# Subtest: RM3 weekday plurals keep the full name
ok 981 - RM3 weekday plurals keep the full name
  ---
  duration_ms: 0.484595
  ...
# Subtest: RM4 monthly ordinals use the written token
ok 982 - RM4 monthly ordinals use the written token
  ---
  duration_ms: 0.401326
  ...
# Subtest: RM5 every N days stays verbatim with its count
ok 983 - RM5 every N days stays verbatim with its count
  ---
  duration_ms: 0.136851
  ...
# Subtest: RM6 weekly, N-week, and yearly forms
ok 984 - RM6 weekly, N-week, and yearly forms
  ---
  duration_ms: 0.391697
  ...
# Subtest: RM7 week lists join with Tue, Fri and weekday alone
ok 985 - RM7 week lists join with Tue, Fri and weekday alone
  ---
  duration_ms: 0.16766
  ...
# Subtest: RM8 unknown rules stay verbatim
ok 986 - RM8 unknown rules stay verbatim
  ---
  duration_ms: 0.594294
  ...
# Subtest: RM9 parens and padded brackets are canonical
ok 987 - RM9 parens and padded brackets are canonical
  ---
  duration_ms: 0.628158
  ...
# Subtest: RM10 case is preserved in the rule and tooltip
ok 988 - RM10 case is preserved in the rule and tooltip
  ---
  duration_ms: 0.252402
  ...
# Subtest: RM11 cursor in the field reveals it, RM12 closed rows still mark
ok 989 - RM11 cursor in the field reveals it, RM12 closed rows still mark
  ---
  duration_ms: 0.291978
  ...
# Subtest: RN1 unreadable rules get no mark
ok 990 - RN1 unreadable rules get no mark
  ---
  duration_ms: 0.888716
  ...
# Subtest: RN2 the checklist guard follows membership, not the glyph slot
ok 991 - RN2 the checklist guard follows membership, not the glyph slot
  ---
  duration_ms: 0.190613
  ...
# Subtest: RN3 code still parses pure but decorates nothing
ok 992 - RN3 code still parses pure but decorates nothing
  ---
  duration_ms: 0.305203
  ...
# Subtest: element anatomy: repeat host, rule, quiet tone, no date
ok 993 - element anatomy: repeat host, rule, quiet tone, no date
  ---
  duration_ms: 0.506287
  ...
# Subtest: family dispatch keeps dates working and sorts adds
ok 994 - family dispatch keeps dates working and sorts adds
  ---
  duration_ms: 0.684326
  ...
# Subtest: Live Preview decorates repeat and respects the guard and code
ok 995 - Live Preview decorates repeat and respects the guard and code
  ---
  duration_ms: 1.105991
  ...
# Subtest: RR1 reading view honors the guard, RO2 rollover skips repeat
ok 996 - RR1 reading view honors the guard, RO2 rollover skips repeat
  ---
  duration_ms: 2.559505
  ...
# Subtest: RA1 api.dateMarks stays dates-only and tooltips never contain ::
ok 997 - RA1 api.dateMarks stays dates-only and tooltips never contain ::
  ---
  duration_ms: 0.413539
  ...
# Subtest: styles.css contract: repeat glyph, ink, resting, repair flag
ok 998 - styles.css contract: repeat glyph, ink, resting, repair flag
  ---
  duration_ms: 0.677673
  ...
# Subtest: LC1 one unlabelled open target renders links-to arrow chip
ok 999 - LC1 one unlabelled open target renders links-to arrow chip
  ---
  duration_ms: 4.292131
  ...
# Subtest: LC2 labelled target carries a pill
ok 1000 - LC2 labelled target carries a pill
  ---
  duration_ms: 0.684376
  ...
# Subtest: LC3 closed and archived targets dim without strike; \#hide mutes
ok 1001 - LC3 closed and archived targets dim without strike; \#hide mutes
  ---
  duration_ms: 2.095549
  ...
# Subtest: LC4 unresolvable target is a dashed missing chip
ok 1002 - LC4 unresolvable target is a dashed missing chip
  ---
  duration_ms: 0.673787
  ...
# Subtest: LC5 LINKED FROM shows the builtin inverse phrase
ok 1003 - LC5 LINKED FROM shows the builtin inverse phrase
  ---
  duration_ms: 1.350548
  ...
# Subtest: LC6 LINKED FROM with an unknown label reads chip, label, this
ok 1004 - LC6 LINKED FROM with an unknown label reads chip, label, this
  ---
  duration_ms: 0.663927
  ...
# Subtest: LC7 live edges missing from the text append in canonical order
ok 1005 - LC7 live edges missing from the text append in canonical order
  ---
  duration_ms: 0.825325
  ...
# Subtest: LC8 stored entries that are no longer live are dashed and uncounted
ok 1006 - LC8 stored entries that are no longer live are dashed and uncounted
  ---
  duration_ms: 0.62351
  ...
# Subtest: LC9 three or more closed chips collapse to ✓×N and expand
ok 1007 - LC9 three or more closed chips collapse to ✓×N and expand
  ---
  duration_ms: 1.274932
  ...
# Subtest: LC10 labelled rows wrap one entry per visual row
ok 1008 - LC10 labelled rows wrap one entry per visual row
  ---
  duration_ms: 1.125378
  ...
# Subtest: LC11 controls need api.relations v1; linked_from_remove calls removeLink(S, T)
ok 1009 - LC11 controls need api.relations v1; linked_from_remove calls removeLink(S, T)
  ---
  duration_ms: 1.494962
  ...
# Subtest: LC12 toggle-dependency-chips covers both relation rows
ok 1010 - LC12 toggle-dependency-chips covers both relation rows
  ---
  duration_ms: 0.620184
  ...
# Subtest: LC13 malformed and not-a-line rows have no model
ok 1011 - LC13 malformed and not-a-line rows have no model
  ---
  duration_ms: 0.190032
  ...
# Subtest: LC14 unsaved editor text refreshes the live model
ok 1012 - LC14 unsaved editor text refreshes the live model
  ---
  duration_ms: 14.803291
  ...
# Subtest: Live Preview decorates relation rows from the index
ok 1013 - Live Preview decorates relation rows from the index
  ---
  duration_ms: 4.001698
  ...
# Subtest: Reading view decorates stored anchors and appends live edges
ok 1014 - Reading view decorates stored anchors and appends live edges
  ---
  duration_ms: 3.179016
  ...
# Subtest: Reading view with api.relations v1 shows ＋ and ×
ok 1015 - Reading view with api.relations v1 shows ＋ and ×
  ---
  duration_ms: 1.736564
  ...
# Subtest: ledger parser agrees with shared LK vectors and parses source task children
ok 1016 - ledger parser agrees with shared LK vectors and parses source task children
  ---
  duration_ms: 3.936964
  ...
# Subtest: relationIndex scans done sources, resolves both directions, and orders label suggestions
ok 1017 - relationIndex scans done sources, resolves both directions, and orders label suggestions
  ---
  duration_ms: 6.69666
  ...
# Subtest: relationIndex applies changed, delete, rename, and unsaved editor overlays
ok 1018 - relationIndex applies changed, delete, rename, and unsaved editor overlays
  ---
  duration_ms: 21.717757
  ...
# Subtest: relationIndex registers after layout-ready and never reads non-markdown during startup replay
ok 1019 - relationIndex registers after layout-ready and never reads non-markdown during startup replay
  ---
  duration_ms: 32.76578
  ...
# Subtest: relationIndex ignores non-markdown live events
ok 1020 - relationIndex ignores non-markdown live events
  ---
  duration_ms: 32.096222
  ...
# Subtest: relationIndex layout-ready after unload registers nothing
ok 1021 - relationIndex layout-ready after unload registers nothing
  ---
  duration_ms: 32.277989
  ...
# Subtest: parseTaskRelationFile indexes every checkbox status as a task
ok 1022 - parseTaskRelationFile indexes every checkbox status as a task
  ---
  duration_ms: 1.087214
  ...
# Subtest: relationIndex incoming and suggestions include Next and Blocked sources
ok 1023 - relationIndex incoming and suggestions include Next and Blocked sources
  ---
  duration_ms: 7.254605
  ...
# Subtest: ledger LK1–LK19 recognises relation shapes and keeps them out of plan links
ok 1024 - ledger LK1–LK19 recognises relation shapes and keeps them out of plan links
  ---
  duration_ms: 2.567229
  ...
# Subtest: parseTrigger parses D[-]<N> dated-entry triggers with offset and span
ok 1025 - parseTrigger parses D[-]<N> dated-entry triggers with offset and span
  ---
  duration_ms: 1.853147
  ...
# Subtest: computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
ok 1026 - computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
  ---
  duration_ms: 0.597891
  ...
# Subtest: expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
ok 1027 - expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
  ---
  duration_ms: 0.629331
  ...
# Subtest: findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
ok 1028 - findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
  ---
  duration_ms: 0.459878
  ...
# Subtest: compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
ok 1029 - compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
  ---
  duration_ms: 0.411696
  ...
# Subtest: parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
ok 1030 - parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
  ---
  duration_ms: 0.211464
  ...
# Subtest: computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
ok 1031 - computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
  ---
  duration_ms: 0.273682
  ...
# Subtest: findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
ok 1032 - findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
  ---
  duration_ms: 0.255538
  ...
# Subtest: findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
ok 1033 - findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
  ---
  duration_ms: 0.42976
  ...
# Subtest: expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
ok 1034 - expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
  ---
  duration_ms: 0.865121
  ...
# Subtest: regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
ok 1035 - regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
  ---
  duration_ms: 0.380777
  ...
# Subtest: expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
ok 1036 - expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
  ---
  duration_ms: 0.316735
  ...
# Subtest: stats fence body sets defaults only and ignores the rest
ok 1037 - stats fence body sets defaults only and ignores the rest
  ---
  duration_ms: 1.726195
  ...
# Subtest: stats tile models cover every unit and every quality
ok 1038 - stats tile models cover every unit and every quality
  ---
  duration_ms: 0.514602
  ...
# Subtest: stats spark bars mark null gaps, zero ticks, and hollow today
ok 1039 - stats spark bars mark null gaps, zero ticks, and hollow today
  ---
  duration_ms: 0.317125
  ...
# Subtest: stats table rows and CSV share the same points
ok 1040 - stats table rows and CSV share the same points
  ---
  duration_ms: 0.671241
  ...
# Subtest: stats overview ids prefer the fence, then config, then report order
ok 1041 - stats overview ids prefer the fence, then config, then report order
  ---
  duration_ms: 0.933852
  ...
# Subtest: stats window label always states today and tracking start
ok 1042 - stats window label always states today and tracking start
  ---
  duration_ms: 0.224459
  ...
# Subtest: stats view state is session-only and per source path
ok 1043 - stats view state is session-only and per source path
  ---
  duration_ms: 4.663669
  ...
# Subtest: stats block renders header, tiles, table, and footer from JSON
ok 1044 - stats block renders header, tiles, table, and footer from JSON
  ---
  duration_ms: 42.905412
  ...
# Subtest: stats block shows an actionable card with Retry when bob fails
ok 1045 - stats block shows an actionable card with Retry when bob fails
  ---
  duration_ms: 42.027494
  ...
# Subtest: stats block registers the processor and the Open Stats command
ok 1046 - stats block registers the processor and the Open Stats command
  ---
  duration_ms: 1.713209
  ...
# Subtest: stats stylesheet contract: selectors, tabular-nums, motion, colors
ok 1047 - stats stylesheet contract: selectors, tabular-nums, motion, colors
  ---
  duration_ms: 1.800887
  ...
# Subtest: Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
ok 1048 - Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
  ---
  duration_ms: 2.262878
  ...
# Subtest: prior buckets align by elapsed position and omit invalid and provisional points
ok 1049 - prior buckets align by elapsed position and omit invalid and provisional points
  ---
  duration_ms: 0.941647
  ...
# Subtest: chart renders SVG safely and keeps secondary focus metrics selectable
ok 1050 - chart renders SVG safely and keeps secondary focus metrics selectable
  ---
  duration_ms: 17.132596
  ...
# Subtest: grouped chart pins honest buckets, bounds daily detail, and opens validated notes
ok 1051 - grouped chart pins honest buckets, bounds daily detail, and opens validated notes
  ---
  duration_ms: 7.93373
  ...
# Subtest: local focus, table, pin, and definition changes reuse the retained report
ok 1052 - local focus, table, pin, and definition changes reuse the retained report
  ---
  duration_ms: 8.645149
  ...
# Subtest: keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
ok 1053 - keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
  ---
  duration_ms: 35.304165
  ...
# Subtest: schema-1 fallback keeps day quartiles and never invents grouped daily history
ok 1054 - schema-1 fallback keeps day quartiles and never invents grouped daily history
  ---
  duration_ms: 4.546466
  ...
# Subtest: ResizeObserver redraws cached data and disconnects across rerenders and unload
ok 1055 - ResizeObserver redraws cached data and disconnects across rerenders and unload
  ---
  duration_ms: 132.667823
  ...
# Subtest: stats resolution prefers stats.bob_path, then candidates, then PATH
ok 1056 - stats resolution prefers stats.bob_path, then candidates, then PATH
  ---
  duration_ms: 2.156807
  ...
# Subtest: stats home expansion and range/offset normalization
ok 1057 - stats home expansion and range/offset normalization
  ---
  duration_ms: 0.533288
  ...
# Subtest: stats fetch always runs show -a -f json plus the chosen flags
ok 1058 - stats fetch always runs show -a -f json plus the chosen flags
  ---
  duration_ms: 0.430902
  ...
# Subtest: stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
ok 1059 - stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
  ---
  duration_ms: 7.340357
  ...
# Subtest: stats spawn maps ENOENT, timeouts, and stderr to named errors
ok 1060 - stats spawn maps ENOENT, timeouts, and stderr to named errors
  ---
  duration_ms: 2.655849
  ...
# Subtest: stats decode accepts schema 1 and rejects the rest defensively
ok 1061 - stats decode accepts schema 1 and rejects the rest defensively
  ---
  duration_ms: 0.278461
  ...
# Subtest: stats error cards name the cause and the stats.bob_path fix
ok 1062 - stats error cards name the cause and the stats.bob_path fix
  ---
  duration_ms: 0.325231
  ...
# Subtest: stats fetch shares one flight and coalesces one follow-up
ok 1063 - stats fetch shares one flight and coalesces one follow-up
  ---
  duration_ms: 22.910542
  ...
# Subtest: stats cache is a small LRU keyed by the argument list
ok 1064 - stats cache is a small LRU keyed by the argument list
  ---
  duration_ms: 2.884134
  ...
# Subtest: stats stale entries return immediately and refresh in the background
ok 1065 - stats stale entries return immediately and refresh in the background
  ---
  duration_ms: 1.475426
  ...
# Subtest: stats api v2 keeps append and adds fetch plus bobPath
ok 1066 - stats api v2 keeps append and adds fetch plus bobPath
  ---
  duration_ms: 0.837859
  ...
# Subtest: statsHomeDir defaults to the real home and strips a trailing slash
ok 1067 - statsHomeDir defaults to the real home and strips a trailing slash
  ---
  duration_ms: 0.191766
  ...
# Subtest: stats mac regression: un-injected resolution probes the real home first
ok 1068 - stats mac regression: un-injected resolution probes the real home first
  ---
  duration_ms: 0.226181
  ...
# Subtest: stats absolute candidates are probed verbatim with no doubled slashes
ok 1069 - stats absolute candidates are probed verbatim with no doubled slashes
  ---
  duration_ms: 0.259385
  ...
# Subtest: stats with no home probes only absolute candidates
ok 1070 - stats with no home probes only absolute candidates
  ---
  duration_ms: 0.299582
  ...
# Subtest: stats tilde config expands against the real home
ok 1071 - stats tilde config expands against the real home
  ---
  duration_ms: 0.185704
  ...
# Subtest: stats candidate and tried lists share one source of truth
ok 1072 - stats candidate and tried lists share one source of truth
  ---
  duration_ms: 0.175976
  ...
# Subtest: stats spawn bob-not-found tried list uses the real home
ok 1073 - stats spawn bob-not-found tried list uses the real home
  ---
  duration_ms: 1.441551
  ...
# Subtest: stats unload clears views, timers, cache, and flights
ok 1074 - stats unload clears views, timers, cache, and flights
  ---
  duration_ms: 0.914145
  ...
# Subtest: stats namespace v1 serializes versioned review answer JSONL
ok 1075 - stats namespace v1 serializes versioned review answer JSONL
  ---
  duration_ms: 6.898194
  ...
# Subtest: stats journal rejects invalid calendar days and outcomes
ok 1076 - stats journal rejects invalid calendar days and outcomes
  ---
  duration_ms: 1.29417
  ...
# Subtest: statsReviewHost lowercases, cuts at the first dot, and never throws
ok 1077 - statsReviewHost lowercases, cuts at the first dot, and never throws
  ---
  duration_ms: 0.157361
  ...
# Subtest: stats journal plugin passthrough keeps a semver writer and falls back otherwise
ok 1078 - stats journal plugin passthrough keeps a semver writer and falls back otherwise
  ---
  duration_ms: 0.882013
  ...
# Subtest: panel dispatch covers every family, custom kinds, and the net exception
ok 1079 - panel dispatch covers every family, custom kinds, and the net exception
  ---
  duration_ms: 1.012843
  ...
# Subtest: pomodoro panel shows the supplied total, shares, hue, and safe text
ok 1080 - pomodoro panel shows the supplied total, shares, hue, and safe text
  ---
  duration_ms: 11.322017
  ...
# Subtest: home parts use the report catalog for labels, hue slots, and pinned values
ok 1081 - home parts use the report catalog for labels, hue slots, and pinned values
  ---
  duration_ms: 11.327447
  ...
# Subtest: areas panel toggles Themes, pins spans, expands projects, and opens home links
ok 1082 - areas panel toggles Themes, pins spans, expands projects, and opens home links
  ---
  duration_ms: 19.068171
  ...
# Subtest: chart pin refreshes Where the time went and Themes honor the pinned span
ok 1083 - chart pin refreshes Where the time went and Themes honor the pinned span
  ---
  duration_ms: 4.505548
  ...
# Subtest: review rows keep their area hue and a missing homes report keeps the saved view
ok 1084 - review rows keep their area hue and a missing homes report keeps the saved view
  ---
  duration_ms: 2.806376
  ...
# Subtest: task home table uses catalog labels and keeps hue dots and mini-bars
ok 1085 - task home table uses catalog labels and keeps hue dots and mini-bars
  ---
  duration_ms: 5.188061
  ...
# Subtest: task flow stacks signed values, keeps missing constituents missing, and labels series
ok 1086 - task flow stacks signed values, keeps missing constituents missing, and labels series
  ---
  duration_ms: 4.131624
  ...
# Subtest: absent companions are named, custom filters are labeled overall, and net splits breakdowns
ok 1087 - absent companions are named, custom filters are labeled overall, and net splits breakdowns
  ---
  duration_ms: 6.288651
  ...
# Subtest: journal panels pair answers with review time and a gapped keep chart under 90%
ok 1088 - journal panels pair answers with review time and a gapped keep chart under 90%
  ---
  duration_ms: 4.817063
  ...
# Subtest: checklist calendar aligns Monday weeks with states, reasons, and provisional today
ok 1089 - checklist calendar aligns Monday weeks with states, reasons, and provisional today
  ---
  duration_ms: 4.80017
  ...
# Subtest: grouped calendars reuse daily points and old schemas fall back with a label
ok 1090 - grouped calendars reuse daily points and old schemas fall back with a label
  ---
  duration_ms: 2.290772
  ...
# Subtest: ISO year boundaries stay in one Monday week and chore dots expose text
ok 1091 - ISO year boundaries stay in one Monday week and chore dots expose text
  ---
  duration_ms: 1.689746
  ...
# Subtest: panel day selection pins the shared day and never fetches
ok 1092 - panel day selection pins the shared day and never fetches
  ---
  duration_ms: 7.286384
  ...
# Subtest: field and formula metrics keep only the focus chart and table
ok 1093 - field and formula metrics keep only the focus chart and table
  ---
  duration_ms: 1.714432
  ...
# Subtest: TT vectors verbatim: task-line gate plus boundary tokens
ok 1094 - TT vectors verbatim: task-line gate plus boundary tokens
  ---
  duration_ms: 3.373748
  ...
# Subtest: TT13-TT14 cursor reveal is inclusive
ok 1095 - TT13-TT14 cursor reveal is inclusive
  ---
  duration_ms: 1.164492
  ...
# Subtest: TT16 coexistence: task tag range is disjoint from priority and date marks
ok 1096 - TT16 coexistence: task tag range is disjoint from priority and date marks
  ---
  duration_ms: 1.167408
  ...
# Subtest: tooltip is exact and never contains a double colon
ok 1097 - tooltip is exact and never contains a double colon
  ---
  duration_ms: 0.19391
  ...
# Subtest: element structure: empty widget span with tooltip attributes
ok 1098 - element structure: empty widget span with tooltip attributes
  ---
  duration_ms: 0.261719
  ...
# Subtest: Live Preview decorations cover exactly the tag and respect reveal and code
ok 1099 - Live Preview decorations cover exactly the tag and respect reveal and code
  ---
  duration_ms: 0.606588
  ...
# Subtest: widget mousedown reveals the tag start
ok 1100 - widget mousedown reveals the tag start
  ---
  duration_ms: 0.351982
  ...
# Subtest: TR vectors verbatim: rendered views annotate eligible anchors in place
ok 1101 - TR vectors verbatim: rendered views annotate eligible anchors in place
  ---
  duration_ms: 1.42524
  ...
# Subtest: TR9 toggle strips document-wide and re-annotates on enable
ok 1102 - TR9 toggle strips document-wide and re-annotates on enable
  ---
  duration_ms: 0.901
  ...
# Subtest: annotate and strip helpers are idempotent and defensive
ok 1103 - annotate and strip helpers are idempotent and defensive
  ---
  duration_ms: 0.517017
  ...
# Subtest: session toggle and onload wiring
ok 1104 - session toggle and onload wiring
  ---
  duration_ms: 4.354531
  ...
# Subtest: styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
ok 1105 - styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
  ---
  duration_ms: 1.010729
  ...
# Subtest: TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
ok 1106 - TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
  ---
  duration_ms: 0.420683
  ...
# Subtest: Live Preview ref decorations replace the whole pair and reveal both tags at once
ok 1107 - Live Preview ref decorations replace the whole pair and reveal both tags at once
  ---
  duration_ms: 0.419901
  ...
# Subtest: ref element structure: book classes, reference label, and tooltip
ok 1108 - ref element structure: book classes, reference label, and tooltip
  ---
  duration_ms: 0.148553
  ...
# Subtest: TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
ok 1109 - TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
  ---
  duration_ms: 0.615374
  ...
# Subtest: TR11 verbatim: \#task \#references and reversed order keep the hash only
ok 1110 - TR11 verbatim: \#task \#references and reversed order keep the hash only
  ---
  duration_ms: 0.275816
  ...
# Subtest: TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
ok 1111 - TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
  ---
  duration_ms: 0.142662
  ...
# Subtest: TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
ok 1112 - TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
  ---
  duration_ms: 1.678012
  ...
# Subtest: styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
ok 1113 - styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
  ---
  duration_ms: 0.792683
  ...
# Subtest: CK vectors: canonical PRE/POST checklist runs share membership semantics
ok 1114 - CK vectors: canonical PRE/POST checklist runs share membership semantics
  ---
  duration_ms: 0.913353
  ...
# Subtest: CK live preview and widget vectors: one stable glyph replaces the full run
ok 1115 - CK live preview and widget vectors: one stable glyph replaces the full run
  ---
  duration_ms: 0.42936
  ...
# Subtest: CR vectors: rendered checklist anchors annotate in place, conflict stays native
ok 1116 - CR vectors: rendered checklist anchors annotate in place, conflict stays native
  ---
  duration_ms: 0.934083
  ...
# Subtest: CR3 toggle restores all checklist pills and re-annotates them
ok 1117 - CR3 toggle restores all checklist pills and re-annotates them
  ---
  duration_ms: 0.390816
  ...
# Subtest: CR4 Today reading-view anchor follows the second checklist tag
ok 1118 - CR4 Today reading-view anchor follows the second checklist tag
  ---
  duration_ms: 0.336653
  ...
# Subtest: checklist task mark CSS contract covers glyphs, conflict gates, Tasks rows, and resting
ok 1119 - checklist task mark CSS contract covers glyphs, conflict gates, Tasks rows, and resting
  ---
  duration_ms: 0.821448
  ...
# Subtest: section info null stays neutral (TM19)
ok 1120 - section info null stays neutral (TM19)
  ---
  duration_ms: 2.198756
  ...
# Subtest: data-line mapping stamps and marks an exact Today row
ok 1121 - data-line mapping stamps and marks an exact Today row
  ---
  duration_ms: 4.377353
  ...
# Subtest: data-line mapping rejects a status mismatch
ok 1122 - data-line mapping rejects a status mismatch
  ---
  duration_ms: 0.474054
  ...
# Subtest: row-index fallback maps when counts agree and refuses when they disagree
ok 1123 - row-index fallback maps when counts agree and refuses when they disagree
  ---
  duration_ms: 1.972103
  ...
# Subtest: Tasks result rows and code are skipped
ok 1124 - Tasks result rows and code are skipped
  ---
  duration_ms: 0.574386
  ...
# Subtest: a daily-note sourcePath is skipped
ok 1125 - a daily-note sourcePath is skipped
  ---
  duration_ms: 0.27237
  ...
# Subtest: duplicate ids stay neutral
ok 1126 - duplicate ids stay neutral
  ---
  duration_ms: 0.732418
  ...
# Subtest: insertion points: \#task anchor, \#ref pair, checkbox, whitespace split
ok 1127 - insertion points: \#task anchor, \#ref pair, checkbox, whitespace split
  ---
  duration_ms: 1.814173
  ...
# Subtest: identity-proven non-Today rows are stamped without a mark
ok 1128 - identity-proven non-Today rows are stamped without a mark
  ---
  duration_ms: 0.736596
  ...
# Subtest: sweep adds on link, removes on unlink or completion, updates tooltip, respects toggle, skips daily ancestors
ok 1129 - sweep adds on link, removes on unlink or completion, updates tooltip, respects toggle, skips daily ancestors
  ---
  duration_ms: 2.233201
  ...
# Subtest: daily-view class is set on open daily leaves and cleared on switch
ok 1130 - daily-view class is set on open daily leaves and cleared on switch
  ---
  duration_ms: 0.455719
  ...
# Subtest: delegated Mod+click jumps; plain click does not
ok 1131 - delegated Mod+click jumps; plain click does not
  ---
  duration_ms: 3.222369
  ...
# Subtest: setupTodayMarks registers the reading post-processor at order 60
ok 1132 - setupTodayMarks registers the reading post-processor at order 60
  ---
  duration_ms: 0.365698
  ...
# Subtest: styles.css daily-view suppression is present
ok 1133 - styles.css daily-view suppression is present
  ---
  duration_ms: 0.735033
  ...
# Subtest: Live Preview marks do not double-jump in Reading view
ok 1134 - Live Preview marks do not double-jump in Reading view
  ---
  duration_ms: 0.467062
  ...
# Subtest: mid-body \#task goes at the body start
ok 1135 - mid-body \#task goes at the body start
  ---
  duration_ms: 0.619031
  ...
# Subtest: \#task inside inline code stays neutral
ok 1136 - \#task inside inline code stays neutral
  ---
  duration_ms: 0.297047
  ...
# Subtest: re-render with a new path refreshes the mark key
ok 1137 - re-render with a new path refreshes the mark key
  ---
  duration_ms: 0.344057
  ...
# Subtest: one duplicate scan per render
ok 1138 - one duplicate scan per render
  ---
  duration_ms: 0.594735
  ...
# Subtest: row-index fallback uses every list item
ok 1139 - row-index fallback uses every list item
  ---
  duration_ms: 0.48756
  ...
# Subtest: open statuses are exactly space, star, slash, and question
ok 1140 - open statuses are exactly space, star, slash, and question
  ---
  duration_ms: 1.670327
  ...
# Subtest: trailing-id rules: leading space, trailing-only, valid charset
ok 1141 - trailing-id rules: leading space, trailing-only, valid charset
  ---
  duration_ms: 0.386107
  ...
# Subtest: candidate: TM9 closed stays null, TM10 open statuses pass
ok 1142 - candidate: TM9 closed stays null, TM10 open statuses pass
  ---
  duration_ms: 1.793091
  ...
# Subtest: candidate: TM11 needs an exact \#task tag and a trailing id
ok 1143 - candidate: TM11 needs an exact \#task tag and a trailing id
  ---
  duration_ms: 0.272019
  ...
# Subtest: candidate: TM21 code is left for the call-site code check
ok 1144 - candidate: TM21 code is left for the call-site code check
  ---
  duration_ms: 0.290555
  ...
# Subtest: insert offset: \#task first lands before the title
ok 1145 - insert offset: \#task first lands before the title
  ---
  duration_ms: 0.209069
  ...
# Subtest: insert offset: TM16 \#task \#ref spans the pair, \#prj sits between
ok 1146 - insert offset: TM16 \#task \#ref spans the pair, \#prj sits between
  ---
  duration_ms: 0.268843
  ...
# Subtest: insert offset: mid-body \#task falls back to the body start
ok 1147 - insert offset: mid-body \#task falls back to the body start
  ---
  duration_ms: 0.158452
  ...
# Subtest: insert offset: blockquote, spaces, numbered, empty title, emoji
ok 1148 - insert offset: blockquote, spaces, numbered, empty title, emoji
  ---
  duration_ms: 0.838371
  ...
# Subtest: duplicates: TM15 marks neither line
ok 1149 - duplicates: TM15 marks neither line
  ---
  duration_ms: 0.493712
  ...
# Subtest: session text: named, home label, range-only, unnamed
ok 1150 - session text: named, home label, range-only, unnamed
  ---
  duration_ms: 0.302628
  ...
# Subtest: tooltip: TM1 running, TM2 queued, and the platform variants
ok 1151 - tooltip: TM1 running, TM2 queued, and the platform variants
  ---
  duration_ms: 0.259155
  ...
# Subtest: tooltip: running wins as primary with a +N more suffix
ok 1152 - tooltip: running wins as primary with a +N more suffix
  ---
  duration_ms: 0.13073
  ...
# Subtest: tooltip: empty input yields Today and output never has ::
ok 1153 - tooltip: empty input yields Today and output never has ::
  ---
  duration_ms: 0.210291
  ...
# Subtest: entering window: 600 ms after join, never before or at load
ok 1154 - entering window: 600 ms after join, never before or at load
  ---
  duration_ms: 0.118076
  ...
# Subtest: modifier: primary button with meta on mac, ctrl elsewhere
ok 1155 - modifier: primary button with meta on mac, ctrl elsewhere
  ---
  duration_ms: 0.150517
  ...
# Subtest: element: empty span with tooltip attributes and no listeners
ok 1156 - element: empty span with tooltip attributes and no listeners
  ---
  duration_ms: 0.290715
  ...
# Subtest: widget: eq ignores entering and the callback
ok 1157 - widget: eq ignores entering and the callback
  ---
  duration_ms: 0.170095
  ...
# Subtest: widget: plain mousedown moves the cursor, Mod mousedown jumps
ok 1158 - widget: plain mousedown moves the cursor, Mod mousedown jumps
  ---
  duration_ms: 0.476279
  ...
# Subtest: refresh effect is lazy and stable
ok 1159 - refresh effect is lazy and stable
  ---
  duration_ms: 0.117284
  ...
# Subtest: styles.css implements the glyph anatomy contract
ok 1160 - styles.css implements the glyph anatomy contract
  ---
  duration_ms: 0.690828
  ...
# Subtest: Live Preview applies the TM1-TM22 line, cache, and refresh vectors
ok 1161 - Live Preview applies the TM1-TM22 line, cache, and refresh vectors
  ---
  duration_ms: 28.973132
  ...
# Subtest: Today mark lifecycle registers the toggle, keyboard command, and reading processor
ok 1162 - Today mark lifecycle registers the toggle, keyboard command, and reading processor
  ---
  duration_ms: 22.818217
  ...
# Subtest: keyboard jump uses the task under the cursor and reports non-membership
ok 1163 - keyboard jump uses the task under the cursor and reports non-membership
  ---
  duration_ms: 23.732261
  ...
# Subtest: Mod-click and keyboard jumps land on the current running Task Link
ok 1164 - Mod-click and keyboard jumps land on the current running Task Link
  ---
  duration_ms: 21.293077
  ...
# Subtest: reduced motion stops the entrance pop
ok 1165 - reduced motion stops the entrance pop
  ---
  duration_ms: 0.865291
  ...
# Subtest: tooltips never contain ::
ok 1166 - tooltips never contain ::
  ---
  duration_ms: 0.203909
  ...
# Subtest: todayMarkPosInInlineCode: single, double, unmatched, positions
ok 1167 - todayMarkPosInInlineCode: single, double, unmatched, positions
  ---
  duration_ms: 0.369435
  ...
# Subtest: builder gates on Today ids without touching doc lines
ok 1168 - builder gates on Today ids without touching doc lines
  ---
  duration_ms: 25.110481
  ...
# Subtest: two rebuilds on the same doc compute duplicates once
ok 1169 - two rebuilds on the same doc compute duplicates once
  ---
  duration_ms: 25.174192
  ...
# Subtest: todayMarksNow override drives readiness
ok 1170 - todayMarksNow override drives readiness
  ---
  duration_ms: 14.3003
  ...
# Subtest: refresh dispatches only to non-daily leaves and uses 16 ms
ok 1171 - refresh dispatches only to non-daily leaves and uses 16 ms
  ---
  duration_ms: 10.554853
  ...
# Subtest: keyboard command gates closed status and daily notes
ok 1172 - keyboard command gates closed status and daily notes
  ---
  duration_ms: 16.628214
  ...
# Subtest: TM14 rollover: day N+1 shows no decoration
ok 1173 - TM14 rollover: day N+1 shows no decoration
  ---
  duration_ms: 18.26701
  ...
# Subtest: TM17 widget sits at line.from + insertCh with side -1
ok 1174 - TM17 widget sits at line.from + insertCh with side -1
  ---
  duration_ms: 11.530334
  ...
# Subtest: TM18 entering: new key pops then settles
ok 1175 - TM18 entering: new key pops then settles
  ---
  duration_ms: 18.613683
  ...
# Subtest: TM20 toggle flips class, notice, and refreshes non-daily leaves
ok 1176 - TM20 toggle flips class, notice, and refreshes non-daily leaves
  ---
  duration_ms: 19.444347
  ...
# Subtest: rebuild triggers: doc, viewport, LP field, file switch rebuild; selection alone does not
ok 1177 - rebuild triggers: doc, viewport, LP field, file switch rebuild; selection alone does not
  ---
  duration_ms: 10.239441
  ...
# Subtest: jump guards in-flight, prefers cached ledgerLine over later match
ok 1178 - jump guards in-flight, prefers cached ledgerLine over later match
  ---
  duration_ms: 14.903452
  ...
# Subtest: jump with no open daily leaf attempts the daily open
ok 1179 - jump with no open daily leaf attempts the daily open
  ---
  duration_ms: 18.575089
  ...
# Subtest: home labels: unnamed timed entry uses derived label and 1-based entryLine
ok 1180 - home labels: unnamed timed entry uses derived label and 1-based entryLine
  ---
  duration_ms: 14.806116
  ...
# Subtest: T1 GTD: empty target resolves to the daily note
ok 1181 - T1 GTD: empty target resolves to the daily note
  ---
  duration_ms: 3.69906
  ...
# Subtest: T2 markers: pomodoro mark counts, struck drops, embed counts
ok 1182 - T2 markers: pomodoro mark counts, struck drops, embed counts
  ---
  duration_ms: 0.816829
  ...
# Subtest: T3 closed entries: links under completed/cancelled entries drop
ok 1183 - T3 closed entries: links under completed/cancelled entries drop
  ---
  duration_ms: 0.255357
  ...
# Subtest: T4 shapes: mixed text and deeper descendants drop
ok 1184 - T4 shapes: mixed text and deeper descendants drop
  ---
  duration_ms: 0.356119
  ...
# Subtest: T5 dedupe: same task twice keeps the first position
ok 1185 - T5 dedupe: same task twice keeps the first position
  ---
  duration_ms: 0.46116
  ...
# Subtest: T6 fenced: links inside fenced blocks drop
ok 1186 - T6 fenced: links inside fenced blocks drop
  ---
  duration_ms: 0.343165
  ...
# Subtest: T7 status: the link layer lists every dedicated link
ok 1187 - T7 status: the link layer lists every dedicated link
  ---
  duration_ms: 0.364807
  ...
# Subtest: T8 unresolved: missing notes give no key
ok 1188 - T8 unresolved: missing notes give no key
  ---
  duration_ms: 0.199089
  ...
# Subtest: T9 alias: aliased links count under their target
ok 1189 - T9 alias: aliased links count under their target
  ---
  duration_ms: 0.519271
  ...
# Subtest: laneBudgetFromTasks counts the whole Next lane, Today included
ok 1190 - laneBudgetFromTasks counts the whole Next lane, Today included
  ---
  duration_ms: 1.765499
  ...
# Subtest: laneBudgetFromTasks counts Pending by type and flags over-cap
ok 1191 - laneBudgetFromTasks counts Pending by type and flags over-cap
  ---
  duration_ms: 0.441252
  ...
# Subtest: lane caps come from max_next/max_pending; legacy max_now is ignored
ok 1192 - lane caps come from max_next/max_pending; legacy max_now is ignored
  ---
  duration_ms: 0.212997
  ...
# Subtest: reload event name matches the Tasks bundle subscription
ok 1193 - reload event name matches the Tasks bundle subscription
  ---
  duration_ms: 0.111042
  ...
# Subtest: api v2 shape: Today and lane budgets, no nowBudget
ok 1194 - api v2 shape: Today and lane budgets, no nowBudget
  ---
  duration_ms: 5.933274
  ...
# Subtest: cache rebuild answers isToday/todayRank in ledger order
ok 1195 - cache rebuild answers isToday/todayRank in ledger order
  ---
  duration_ms: 2.467509
  ...
# Subtest: refresh fires only when the key set changes
ok 1196 - refresh fires only when the key set changes
  ---
  duration_ms: 1.039283
  ...
# Subtest: unready to ready with empty TODAY still refreshes open badges
ok 1197 - unready to ready with empty TODAY still refreshes open badges
  ---
  duration_ms: 0.907031
  ...
# Subtest: cache rebuilds on the daily changed event with the event content
ok 1198 - cache rebuilds on the daily changed event with the event content
  ---
  duration_ms: 0.694896
  ...
# Subtest: cache rebuilds once on resolved and at midnight rollover
ok 1199 - cache rebuilds once on resolved and at midnight rollover
  ---
  duration_ms: 3.130384
  ...
# Subtest: computeTodayLinks records entry range and placeholder
ok 1200 - computeTodayLinks records entry range and placeholder
  ---
  duration_ms: 0.417417
  ...
# Subtest: todayOpenEntries and todayRunningEntryLine follow the unique timed rule
ok 1201 - todayOpenEntries and todayRunningEntryLine follow the unique timed rule
  ---
  duration_ms: 0.425552
  ...
# Subtest: resolveTodayLinkKeys keeps duplicates; resolveTodayKeys is first-occurrence
ok 1202 - resolveTodayLinkKeys keeps duplicates; resolveTodayKeys is first-occurrence
  ---
  duration_ms: 0.184092
  ...
# Subtest: todayLinkDetails: named running, placeholder, unnamed home, unnamed none
ok 1203 - todayLinkDetails: named running, placeholder, unnamed home, unnamed none
  ---
  duration_ms: 0.206705
  ...
# Subtest: todayLinkDetails orders running first and keeps one detail per key+entry
ok 1204 - todayLinkDetails orders running first and keeps one detail per key+entry
  ---
  duration_ms: 0.161368
  ...
# Subtest: todayKeyParts splits at the last hash; idsByPath groups block ids
ok 1205 - todayKeyParts splits at the last hash; idsByPath groups block ids
  ---
  duration_ms: 0.12079
  ...
# Subtest: todayDetailsSignature changes only when details change
ok 1206 - todayDetailsSignature changes only when details change
  ---
  duration_ms: 0.182368
  ...
# Subtest: idsByPath and details accessors follow the rebuilt cache
ok 1207 - idsByPath and details accessors follow the rebuilt cache
  ---
  duration_ms: 1.033854
  ...
# Subtest: details-only change refreshes marks without a Tasks reload
ok 1208 - details-only change refreshes marks without a Tasks reload
  ---
  duration_ms: 0.807381
  ...
# Subtest: entered stamps only when the cache was already ready, then prune
ok 1209 - entered stamps only when the cache was already ready, then prune
  ---
  duration_ms: 1.251789
  ...
# Subtest: generation guard: reverse-order async reads keep the newer
ok 1210 - generation guard: reverse-order async reads keep the newer
  ---
  duration_ms: 0.840333
  ...
# Subtest: generation guard: a sync rebuild wins over an in-flight async read
ok 1211 - generation guard: a sync rebuild wins over an in-flight async read
  ---
  duration_ms: 0.570258
  ...
# Subtest: revalidateTodayCache is throttled and refreshes when not ready
ok 1212 - revalidateTodayCache is throttled and refreshes when not ready
  ---
  duration_ms: 0.596358
  ...
# Subtest: revalidateTodayCache respects layoutReady and backwards clock steps
ok 1213 - revalidateTodayCache respects layoutReady and backwards clock steps
  ---
  duration_ms: 0.451722
  ...
# Subtest: a done-today prerequisite shows the glyph
ok 1214 - a done-today prerequisite shows the glyph
  ---
  duration_ms: 3.417862
  ...
# Subtest: done yesterday does not show the glyph
ok 1215 - done yesterday does not show the glyph
  ---
  duration_ms: 0.413529
  ...
# Subtest: a struck link does not show the glyph
ok 1216 - a struck link does not show the glyph
  ---
  duration_ms: 0.291316
  ...
# Subtest: a closed entry does not show the glyph
ok 1217 - a closed entry does not show the glyph
  ---
  duration_ms: 0.245799
  ...
# Subtest: several prerequisites give +N
ok 1218 - several prerequisites give +N
  ---
  duration_ms: 0.490746
  ...
# Subtest: the model refuses every non-glyph shape
ok 1219 - the model refuses every non-glyph shape
  ---
  duration_ms: 0.901511
  ...
# Subtest: unblockedGlyphDoneToday needs DONE plus a today done date
ok 1220 - unblockedGlyphDoneToday needs DONE plus a today done date
  ---
  duration_ms: 0.256951
  ...
# Subtest: tooltip names one prerequisite and counts several
ok 1221 - tooltip names one prerequisite and counts several
  ---
  duration_ms: 0.294402
  ...
# Subtest: Live Preview places one glyph after each unblocked link
ok 1222 - Live Preview places one glyph after each unblocked link
  ---
  duration_ms: 1.801338
  ...
# Subtest: Live Preview draws nothing without a warm cache or a live link
ok 1223 - Live Preview draws nothing without a warm cache or a live link
  ---
  duration_ms: 0.695888
  ...
# Subtest: widget mousedown places the cursor past the link
ok 1224 - widget mousedown places the cursor past the link
  ---
  duration_ms: 0.623189
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
ok 1225 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 0.704615
  ...
# Subtest: Reading view glyphs unblocked rows and dedupes
ok 1226 - Reading view glyphs unblocked rows and dedupes
  ---
  duration_ms: 1.322253
  ...
# Subtest: Reading view refuses every non-glyph row
ok 1227 - Reading view refuses every non-glyph row
  ---
  duration_ms: 1.316132
  ...
# Subtest: api.unblockedGlyph v1 is additive, sync, and never throwing
ok 1228 - api.unblockedGlyph v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.557273
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 1229 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 1.0795
  ...
# Subtest: changed-file and rollover refreshes
ok 1230 - changed-file and rollover refreshes
  ---
  duration_ms: 0.323066
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 1231 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.125901
  ...
# Subtest: styles.css contract: faint glyph, Done token, toggle
ok 1232 - styles.css contract: faint glyph, Done token, toggle
  ---
  duration_ms: 0.622969
  ...
# Subtest: Ledger Vim mappings restore \\p and retain the other normal-mode actions
ok 1233 - Ledger Vim mappings restore \\p and retain the other normal-mode actions
  ---
  duration_ms: 2.23729
  ...
# Subtest: workBadgeTone boundary vectors at cap 100 use exact comparisons
ok 1234 - workBadgeTone boundary vectors at cap 100 use exact comparisons
  ---
  duration_ms: 1.020217
  ...
# Subtest: workBadgeTone at cap 15 has no percentage rounding
ok 1235 - workBadgeTone at cap 15 has no percentage rounding
  ---
  duration_ms: 0.201875
  ...
# Subtest: workBadgeTone default caps, small caps, and cap changes
ok 1236 - workBadgeTone default caps, small caps, and cap changes
  ---
  duration_ms: 0.164604
  ...
# Subtest: workBadgeTone never coerces invalid input to zero
ok 1237 - workBadgeTone never coerces invalid input to zero
  ---
  duration_ms: 0.929334
  ...
# Subtest: TODAY links bands with themes at cap 3
ok 1238 - TODAY links bands with themes at cap 3
  ---
  duration_ms: 0.348385
  ...
# Subtest: TODAY theme overflow forces red, exact cap does not
ok 1239 - TODAY theme overflow forces red, exact cap does not
  ---
  duration_ms: 0.219298
  ...
# Subtest: TODAY unavailable stays neutral, empty section is grey
ok 1240 - TODAY unavailable stays neutral, empty section is grey
  ---
  duration_ms: 1.075191
  ...
# Subtest: PENDING/NEXT models color the section, READY its gated count
ok 1241 - PENDING/NEXT models color the section, READY its gated count
  ---
  duration_ms: 0.510003
  ...
# Subtest: READY uses its gated count even when the total lane is larger
ok 1242 - READY uses its gated count even when the total lane is larger
  ---
  duration_ms: 0.583634
  ...
# Subtest: cap equality still emits no cap lint
ok 1243 - cap equality still emits no cap lint
  ---
  duration_ms: 3.219625
  ...
# Subtest: lane DOM keeps exactly one tone through transitions and unavailability
ok 1244 - lane DOM keeps exactly one tone through transitions and unavailability
  ---
  duration_ms: 7.292526
  ...
# Subtest: READY DOM keeps exactly one tone and daily/dashboard models agree
ok 1245 - READY DOM keeps exactly one tone and daily/dashboard models agree
  ---
  duration_ms: 1.146818
  ...
# SKIP dashboard integration: BOB_DASHBOARD_FILE is not set
# SKIP dashboard fallback integration: BOB_DASHBOARD_FILE is not set
# SKIP dash CSS contract: BOB_DASHBOARD_FILE is not set
# Subtest: daily TODAY chip uses the theme-overflow tone
ok 1246 - daily TODAY chip uses the theme-overflow tone
  ---
  duration_ms: 16.893411
  ...
# Subtest: dashboard integration uses Work tones, TODAY override, and keeps Work order
ok 1247 - dashboard integration uses Work tones, TODAY override, and keeps Work order
  ---
  duration_ms: 0.749491
  ...
# Subtest: dashboard fallbacks keep Work tones without plugin renderers or colors
ok 1248 - dashboard fallbacks keep Work tones without plugin renderers or colors
  ---
  duration_ms: 0.388963
  ...
# Subtest: Work tone CSS covers each tone and uses the shared magenta value
ok 1249 - Work tone CSS covers each tone and uses the shared magenta value
  ---
  duration_ms: 1.130357
  ...
# Subtest: RBW6 mergeTargetPreparations keeps one write at the strongest lane
ok 1250 - RBW6 mergeTargetPreparations keeps one write at the strongest lane
  ---
  duration_ms: 2.818819
  ...
# Subtest: §15.7 notices use curly quotes and the Ready → Blocked copy
ok 1251 - §15.7 notices use curly quotes and the Ready → Blocked copy
  ---
  duration_ms: 0.690067
  ...
# Subtest: RBP1 same-note add is one transaction and matches forward bytes
ok 1252 - RBP1 same-note add is one transaction and matches forward bytes
  ---
  duration_ms: 24.258314
  ...
# Subtest: RBP2 background-leaf T matches forward bytes
ok 1253 - RBP2 background-leaf T matches forward bytes
  ---
  duration_ms: 5.893879
  ...
# Subtest: RBP3 closed T is written through vault.process and matches forward bytes
ok 1254 - RBP3 closed T is written through vault.process and matches forward bytes
  ---
  duration_ms: 4.128268
  ...
# Subtest: RBP4 ordinary transfer; a ^prj N is never raised
ok 1255 - RBP4 ordinary transfer; a ^prj N is never raised
  ---
  duration_ms: 17.195446
  ...
# Subtest: RBP5 consumed Pomodoro link matches forward bytes
ok 1256 - RBP5 consumed Pomodoro link matches forward bytes
  ---
  duration_ms: 6.757626
  ...
# Subtest: RBP6 project T with residents and a sub-project matches forward bytes
ok 1257 - RBP6 project T with residents and a sub-project matches forward bytes
  ---
  duration_ms: 18.509104
  ...
# Subtest: RBP7 two dependents in different lanes prepare N once at [/]
ok 1258 - RBP7 two dependents in different lanes prepare N once at [/]
  ---
  duration_ms: 5.277551
  ...
# Subtest: RBP8 counted sources N1 and N2 match forward(T + N1, N2)
ok 1259 - RBP8 counted sources N1 and N2 match forward(T + N1, N2)
  ---
  duration_ms: 3.566016
  ...
# Subtest: RBP9 blocks_lines false writes no BLOCKS and still ids N
ok 1260 - RBP9 blocks_lines false writes no BLOCKS and still ids N
  ---
  duration_ms: 1.617126
  ...
# Subtest: RBP10 removing the last reason matches forward removal
ok 1261 - RBP10 removing the last reason matches forward removal
  ---
  duration_ms: 3.137827
  ...
# Subtest: RBW1 a changed source note writes nothing
ok 1262 - RBW1 a changed source note writes nothing
  ---
  duration_ms: 1.393079
  ...
# Subtest: RBW2 one changed T note still lands the others and omits it from BLOCKS
ok 1263 - RBW2 one changed T note still lands the others and omits it from BLOCKS
  ---
  duration_ms: 1.451309
  ...
# Subtest: RBW3 already-present picks write nothing
ok 1264 - RBW3 already-present picks write nothing
  ---
  duration_ms: 1.057107
  ...
# Subtest: RBW4 cleanup runs for T's that committed when N lives in today's daily note
ok 1265 - RBW4 cleanup runs for T's that committed when N lives in today's daily note
  ---
  duration_ms: 2.007581
  ...
# Subtest: RBW6 counted forward two-lane dependents prepare N once
ok 1266 - RBW6 counted forward two-lane dependents prepare N once
  ---
  duration_ms: 10.568459
  ...
# Subtest: A1 N above two T's in one note matches forward (open and closed note)
ok 1267 - A1 N above two T's in one note matches forward (open and closed note)
  ---
  duration_ms: 14.976873
  ...
# Subtest: A1 N below two T's matches forward bytes
ok 1268 - A1 N below two T's matches forward bytes
  ---
  duration_ms: 2.442061
  ...
# Subtest: A2 forward stamps the dependent when a prerequisite above gains BLOCKS
ok 1269 - A2 forward stamps the dependent when a prerequisite above gains BLOCKS
  ---
  duration_ms: 0.748408
  ...
# Subtest: A1 mixed same-note and cross-note picks keep N's lane rise (RBP7 variant)
ok 1270 - A1 mixed same-note and cross-note picks keep N's lane rise (RBP7 variant)
  ---
  duration_ms: 2.507114
  ...
# Subtest: A1 RBP1 with N truly lacking ^id is prompted an id and matches forward
ok 1271 - A1 RBP1 with N truly lacking ^id is prompted an id and matches forward
  ---
  duration_ms: 1.412165
  ...
# Subtest: A1 N lacking ^id in a closed note above T keeps its BLOCKS line under N
ok 1272 - A1 N lacking ^id in a closed note above T keeps its BLOCKS line under N
  ---
  duration_ms: 0.951356
  ...
# Subtest: A3 mirror lists the committed T's by identity (N above T1, X, T2)
ok 1273 - A3 mirror lists the committed T's by identity (N above T1, X, T2)
  ---
  duration_ms: 1.411955
  ...
# Subtest: A4 notices name T, not N (add, remove, project, counted)
ok 1274 - A4 notices name T, not N (add, remove, project, counted)
  ---
  duration_ms: 4.546588
  ...
# Subtest: A5 the writer's stale notice is returned once and never shown by the writer
ok 1275 - A5 the writer's stale notice is returned once and never shown by the writer
  ---
  duration_ms: 1.263071
  ...
# Subtest: A6 a changed T row (rawLine) is refused before any write
ok 1276 - A6 a changed T row (rawLine) is refused before any write
  ---
  duration_ms: 0.199401
  ...
# Subtest: A7 RBW2 keeps the failed T's Pomodoro link and consumes the committed one
ok 1277 - A7 RBW2 keeps the failed T's Pomodoro link and consumes the committed one
  ---
  duration_ms: 1.826024
  ...
# Subtest: A8 closed-note T guards run when the gesture is applied
ok 1278 - A8 closed-note T guards run when the gesture is applied
  ---
  duration_ms: 2.578691
  ...
# Subtest: A9 a ^prj T's residents recover with [unblocked::] when N lives in a daily note
ok 1279 - A9 a ^prj T's residents recover with [unblocked::] when N lives in a daily note
  ---
  duration_ms: 8.356027
  ...
# Subtest: A5 a preparation no write can carry fails the plan instead of being dropped
ok 1280 - A5 a preparation no write can carry fails the plan instead of being dropped
  ---
  duration_ms: 0.930145
  ...
# Subtest: applyDependencyEdit adding a first cross-note prerequisite keeps the dependent's cursor
ok 1281 - applyDependencyEdit adding a first cross-note prerequisite keeps the dependent's cursor
  ---
  duration_ms: 1.79705
  ...
# Subtest: applyBlocksEdit giving a source its first BLOCKS line keeps the source's cursor
ok 1282 - applyBlocksEdit giving a source its first BLOCKS line keeps the source's cursor
  ---
  duration_ms: 5.001636
  ...
# Subtest: nav BK1–BK2 accept canonical BLOCKS lines
ok 1283 - nav BK1–BK2 accept canonical BLOCKS lines
  ---
  duration_ms: 3.248298
  ...
# Subtest: nav BK3–BK11 canonicalise
ok 1284 - nav BK3–BK11 canonicalise
  ---
  duration_ms: 0.867556
  ...
# Subtest: nav BK12 empty, BK13–BK15 malformed
ok 1285 - nav BK12 empty, BK13–BK15 malformed
  ---
  duration_ms: 0.243625
  ...
# Subtest: nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse
ok 1286 - nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse
  ---
  duration_ms: 0.463464
  ...
# Subtest: nav BK21 code-point sort and writer format
ok 1287 - nav BK21 code-point sort and writer format
  ---
  duration_ms: 0.404953
  ...
# Subtest: nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS
ok 1288 - nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS
  ---
  duration_ms: 0.624411
  ...
# Subtest: nav BW18 conversion drops BLOCKS like Sub-projects
ok 1289 - nav BW18 conversion drops BLOCKS like Sub-projects
  ---
  duration_ms: 1.4779
  ...
# Subtest: nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner
ok 1290 - nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner
  ---
  duration_ms: 1.158842
  ...
# Subtest: nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists
ok 1291 - nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists
  ---
  duration_ms: 2.167547
  ...
# Subtest: nav MC1/MC2 deferred Pomodoro cleanup skips managed lines
ok 1292 - nav MC1/MC2 deferred Pomodoro cleanup skips managed lines
  ---
  duration_ms: 0.577121
  ...
# Subtest: showBlocksStage opens from a task with reverse CURRENT and RESULTS
ok 1293 - showBlocksStage opens from a task with reverse CURRENT and RESULTS
  ---
  duration_ms: 14.629468
  ...
# Subtest: showBlocksStage opens from a counted session
ok 1294 - showBlocksStage opens from a counted session
  ---
  duration_ms: 1.778874
  ...
# Subtest: showBlocksStage opens on a Task Link target note
ok 1295 - showBlocksStage opens on a Task Link target note
  ---
  duration_ms: 1.297276
  ...
# Subtest: RBU1 empty query uses today-first then In Progress, Next, same-note, rest
ok 1296 - RBU1 empty query uses today-first then In Progress, Next, same-note, rest
  ---
  duration_ms: 1.51394
  ...
# Subtest: RBU2 today-linked rows carry 🍅 running and strip names the entry
ok 1297 - RBU2 today-linked rows carry 🍅 running and strip names the entry
  ---
  duration_ms: 1.045335
  ...
# Subtest: RBU3 CURRENT 🔑 only when N is the last reason
ok 1298 - RBU3 CURRENT 🔑 only when N is the last reason
  ---
  duration_ms: 1.530511
  ...
# Subtest: RBU4 footer verbs are block, remove, and apply N
ok 1299 - RBU4 footer verbs are block, remove, and apply N
  ---
  duration_ms: 1.817979
  ...
# Subtest: RBU5 subtitle at rest, with marks, and names this task first
ok 1300 - RBU5 subtitle at rest, with marks, and names this task first
  ---
  duration_ms: 2.09635
  ...
# Subtest: RBG1 N itself is excluded from RESULTS
ok 1301 - RBG1 N itself is excluded from RESULTS
  ---
  duration_ms: 0.749701
  ...
# Subtest: RBG2 a cycle disables the row with path tooltip copy
ok 1302 - RBG2 a cycle disables the row with path tooltip copy
  ---
  duration_ms: 0.950674
  ...
# Subtest: RBG3 ^prj T with N inside the project is inside this project
ok 1303 - RBG3 ^prj T with N inside the project is inside this project
  ---
  duration_ms: 2.097323
  ...
# Subtest: RBG3 descendant N disables the parent project as a sub-project
ok 1304 - RBG3 descendant N disables the parent project as a sub-project
  ---
  duration_ms: 1.386647
  ...
# Subtest: RBG4 a malformed or second Depends-On line is guarded
ok 1305 - RBG4 a malformed or second Depends-On line is guarded
  ---
  duration_ms: 0.731637
  ...
# Subtest: RBG5 stale refuse reopens in the Blocks direction
ok 1306 - RBG5 stale refuse reopens in the Blocks direction
  ---
  duration_ms: 3.528213
  ...
# Subtest: RBG5 for T: a T changed after stage open refuses once and writes nothing
ok 1307 - RBG5 for T: a T changed after stage open refuses once and writes nothing
  ---
  duration_ms: 2.482097
  ...
# Subtest: today's links survive a pool refresh that lands while the daily note loads
ok 1308 - today's links survive a pool refresh that lands while the daily note loads
  ---
  duration_ms: 31.718302
  ...
# Subtest: RBG8 Esc from the stage or the block-ID prompt writes nothing
ok 1309 - RBG8 Esc from the stage or the block-ID prompt writes nothing
  ---
  duration_ms: 2.88241
  ...
# Subtest: missing source ^id opens the block-ID prompt and Esc allocates none
ok 1310 - missing source ^id opens the block-ID prompt and Esc allocates none
  ---
  duration_ms: 1.354154
  ...
# Subtest: RBP11 inbox route runs first then the Blocks write
ok 1311 - RBP11 inbox route runs first then the Blocks write
  ---
  duration_ms: 1.02712
  ...
# Subtest: RBW5 review walk stays unless the commit takes N out of today's walk
ok 1312 - RBW5 review walk stays unless the commit takes N out of today's walk
  ---
  duration_ms: 6.159636
  ...
# Subtest: marks commit add and remove together; counted uses k/n block
ok 1313 - marks commit add and remove together; counted uses k/n block
  ---
  duration_ms: 3.099755
  ...
# Subtest: strip text covers RESULTS, BLOCKED, CURRENT, disabled, marks, and ^prj
ok 1314 - strip text covers RESULTS, BLOCKED, CURRENT, disabled, marks, and ^prj
  ---
  duration_ms: 0.570909
  ...
# Subtest: counted subtitle drops the ⇥ hint because marks are off in counted sessions
ok 1315 - counted subtitle drops the ⇥ hint because marks are off in counted sessions
  ---
  duration_ms: 1.041858
  ...
# Subtest: 🔑 tooltip and 🍅 tooltip render on badges
ok 1316 - 🔑 tooltip and 🍅 tooltip render on badges
  ---
  duration_ms: 1.146959
  ...
# Subtest: Tab marks Blocks CURRENT rows and Enter removes both dependents
ok 1317 - Tab marks Blocks CURRENT rows and Enter removes both dependents
  ---
  duration_ms: 17.117047
  ...
# Subtest: SB1-SB9 dependent IDs match the successor mint vectors
ok 1318 - SB1-SB9 dependent IDs match the successor mint vectors
  ---
  duration_ms: 2.551729
  ...
# Subtest: BW1 same-note add mints and writes BLOCKS in the dependent's single transaction
ok 1319 - BW1 same-note add mints and writes BLOCKS in the dependent's single transaction
  ---
  duration_ms: 11.025211
  ...
# Subtest: BW2 cross-note add follows the dependent commit and writes the target note
ok 1320 - BW2 cross-note add follows the dependent commit and writes the target note
  ---
  duration_ms: 2.85574
  ...
# Subtest: BW4 cross-note target preparation precedes the reverse-line preimage
ok 1321 - BW4 cross-note target preparation precedes the reverse-line preimage
  ---
  duration_ms: 2.003585
  ...
# Subtest: BW3 stale cross-note preimage leaves the forward write standing and shows the suffix
ok 1322 - BW3 stale cross-note preimage leaves the forward write standing and shows the suffix
  ---
  duration_ms: 1.530371
  ...
# Subtest: BW5 removal deletes the reverse line when its last dependent leaves
ok 1323 - BW5 removal deletes the reverse line when its last dependent leaves
  ---
  duration_ms: 3.580403
  ...
# Subtest: BW6 an already mirrored edge is a byte-identical no-op
ok 1324 - BW6 an already mirrored edge is a byte-identical no-op
  ---
  duration_ms: 1.306393
  ...
# Subtest: BW7 closed owners stay frozen
ok 1325 - BW7 closed owners stay frozen
  ---
  duration_ms: 1.774987
  ...
# Subtest: BW8 malformed reverse lines stay untouched and report the failed mirror
ok 1326 - BW8 malformed reverse lines stay untouched and report the failed mirror
  ---
  duration_ms: 1.50942
  ...
# Subtest: BW15 config defaults on, honors false, and invalid values fall back on
ok 1327 - BW15 config defaults on, honors false, and invalid values fall back on
  ---
  duration_ms: 0.886241
  ...
# Subtest: BW17 planner output follows BK21 Unicode code-point ordering
ok 1328 - BW17 planner output follows BK21 Unicode code-point ordering
  ---
  duration_ms: 0.479234
  ...
# Subtest: duplicate BLOCKS children merge their known dependents and preserve CRLF
ok 1329 - duplicate BLOCKS children merge their known dependents and preserve CRLF
  ---
  duration_ms: 0.533298
  ...
# Subtest: BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270)
ok 1330 - BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270)
  ---
  duration_ms: 3.853063
  ...
# Subtest: counted remove-from-all drops every dependent from the same-note BLOCKS line (420)
ok 1331 - counted remove-from-all drops every dependent from the same-note BLOCKS line (420)
  ---
  duration_ms: 1.193588
  ...
# Subtest: vault counted add composes cross-note follow-ups for every source (420)
ok 1332 - vault counted add composes cross-note follow-ups for every source (420)
  ---
  duration_ms: 2.882671
  ...
# Subtest: marked batch add writes every same-note target onto BLOCKS in one plan (430)
ok 1333 - marked batch add writes every same-note target onto BLOCKS in one plan (430)
  ---
  duration_ms: 0.92774
  ...
# Subtest: counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600)
ok 1334 - counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600)
  ---
  duration_ms: 6.241642
  ...
# Subtest: BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves
ok 1335 - BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves
  ---
  duration_ms: 2.647532
  ...
# Subtest: BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS
ok 1336 - BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS
  ---
  duration_ms: 2.564103
  ...
# Subtest: hand-edit clear path routes through the BLOCKS seam (600)
ok 1337 - hand-edit clear path routes through the BLOCKS seam (600)
  ---
  duration_ms: 0.633129
  ...
# Subtest: BW18 conversion never copies a BLOCKS line as a user child
ok 1338 - BW18 conversion never copies a BLOCKS line as a user child
  ---
  duration_ms: 0.619552
  ...
# Subtest: BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it
ok 1339 - BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it
  ---
  duration_ms: 2.988925
  ...
# Subtest: review checklist group helpers format exact completion and close notices
ok 1340 - review checklist group helpers format exact completion and close notices
  ---
  duration_ms: 2.280011
  ...
# Subtest: claim declines without a current exact PRE/POST walk landing
ok 1341 - claim declines without a current exact PRE/POST walk landing
  ---
  duration_ms: 8.069741
  ...
# Subtest: a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
ok 1342 - a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
  ---
  duration_ms: 2.635008
  ...
# Subtest: checklist Ctrl+Enter holds its landing through the actual successor picker
ok 1343 - checklist Ctrl+Enter holds its landing through the actual successor picker
  ---
  duration_ms: 9.948025
  ...
# Subtest: seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
ok 1344 - seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
  ---
  duration_ms: 15.749917
  ...
# Subtest: a landed [?] checklist chore is claimed and completed
ok 1345 - a landed [?] checklist chore is claimed and completed
  ---
  duration_ms: 0.627157
  ...
# Subtest: ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
ok 1346 - ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
  ---
  duration_ms: 1.847916
  ...
# Subtest: live successor filtering skips a stale completed row
ok 1347 - live successor filtering skips a stale completed row
  ---
  duration_ms: 0.900759
  ...
# Subtest: live group filtering reads each cross-note path once
ok 1348 - live group filtering reads each cross-note path once
  ---
  duration_ms: 0.639451
  ...
# Subtest: Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
ok 1349 - Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
  ---
  duration_ms: 2.639217
  ...
# Subtest: POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
ok 1350 - POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
  ---
  duration_ms: 1.270234
  ...
# Subtest: ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
ok 1351 - ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
  ---
  duration_ms: 0.628268
  ...
# Subtest: completion failure preserves cursor and landing and reports the Tasks failure
ok 1352 - completion failure preserves cursor and landing and reports the Tasks failure
  ---
  duration_ms: 0.321623
  ...
# Subtest: reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
ok 1353 - reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
  ---
  duration_ms: 1.385965
  ...
# Subtest: Alt+F on PRE stays with remaining PRE count and never stamps
ok 1354 - Alt+F on PRE stays with remaining PRE count and never stamps
  ---
  duration_ms: 5.11374
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a stale cache
ok 1355 - Ctrl+Alt+F completes seven PRE rows from a stale cache
  ---
  duration_ms: 10.876317
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a refreshed cache
ok 1356 - Ctrl+Alt+F completes seven PRE rows from a refreshed cache
  ---
  duration_ms: 4.457957
  ...
# Subtest: POST stays put with the closing notice
ok 1357 - POST stays put with the closing notice
  ---
  duration_ms: 0.934414
  ...
# Subtest: manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
ok 1358 - manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
  ---
  duration_ms: 1.244815
  ...
# Subtest: manual Ctrl+Enter then ]s from a stale cache uses text-first identity
ok 1359 - manual Ctrl+Enter then ]s from a stale cache uses text-first identity
  ---
  duration_ms: 4.215255
  ...
# Subtest: counted Alt+F skips checklist rows with the skip tail
ok 1360 - counted Alt+F skips checklist rows with the skip tail
  ---
  duration_ms: 3.109334
  ...
# Subtest: missing cycler gate on a PRE row writes nothing
ok 1361 - missing cycler gate on a PRE row writes nothing
  ---
  duration_ms: 0.679477
  ...
# Subtest: missing ledger checklist gate on a tagged line writes nothing
ok 1362 - missing ledger checklist gate on a tagged line writes nothing
  ---
  duration_ms: 0.621896
  ...
# Subtest: a tagged line that is not a queue match falls through to recurring refusal
ok 1363 - a tagged line that is not a queue match falls through to recurring refusal
  ---
  duration_ms: 0.401015
  ...
# Subtest: formatFreshStampChecklistSkipTail names the skipped count
ok 1364 - formatFreshStampChecklistSkipTail names the skipped count
  ---
  duration_ms: 0.133034
  ...
# Subtest: partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
ok 1365 - partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
  ---
  duration_ms: 0.20921
  ...
# Subtest: Task Link Alt+F skips a PRE target with the skip notice
ok 1366 - Task Link Alt+F skips a PRE target with the skip notice
  ---
  duration_ms: 2.189428
  ...
# Subtest: P0 at interval 7 enters P2 with a previewed decay date and kept tail
ok 1367 - P0 at interval 7 enters P2 with a previewed decay date and kept tail
  ---
  duration_ms: 3.287073
  ...
# Subtest: P0 at interval 30 enters P3
ok 1368 - P0 at interval 30 enters P3
  ---
  duration_ms: 0.442485
  ...
# Subtest: fixed enter overrides the interval scan
ok 1369 - fixed enter overrides the interval scan
  ---
  duration_ms: 0.429429
  ...
# Subtest: unknown enter disables Not now without disabling Keep/Reword
ok 1370 - unknown enter disables Not now without disabling Keep/Reword
  ---
  duration_ms: 0.441072
  ...
# Subtest: P0 with no suitable level stays unavailable and never shortens the lease
ok 1371 - P0 with no suitable level stays unavailable and never shortens the lease
  ---
  duration_ms: 0.343676
  ...
# Subtest: custom level order resolves entry in ladder order
ok 1372 - custom level order resolves entry in ladder order
  ---
  duration_ms: 0.275436
  ...
# Subtest: unknown priority value disables Not now only
ok 1373 - unknown priority value disables Not now only
  ---
  duration_ms: 0.318928
  ...
# Subtest: prioritized P2 below its roll limit stays on the same level
ok 1374 - prioritized P2 below its roll limit stays on the same level
  ---
  duration_ms: 0.527918
  ...
# Subtest: P2 at its roll limit decays to P3
ok 1375 - P2 at its roll limit decays to P3
  ---
  duration_ms: 0.638418
  ...
# Subtest: P2 streak derives from the task Schedule Log
ok 1376 - P2 streak derives from the task Schedule Log
  ---
  duration_ms: 2.873895
  ...
# Subtest: configured decay:false keeps rolling past the limit
ok 1377 - configured decay:false keeps rolling past the limit
  ---
  duration_ms: 0.310292
  ...
# Subtest: per-level rolls:0 decays immediately
ok 1378 - per-level rolls:0 decays immediately
  ---
  duration_ms: 0.264986
  ...
# Subtest: terminal cancel substitutes a truthful same-level card roll
ok 1379 - terminal cancel substitutes a truthful same-level card roll
  ---
  duration_ms: 0.275736
  ...
# Subtest: no future date in the window refuses Not now
ok 1380 - no future date in the window refuses Not now
  ---
  duration_ms: 0.19358
  ...
# Subtest: Less often steps 7/14/30 to the next preset with a decision reason
ok 1381 - Less often steps 7/14/30 to the next preset with a decision reason
  ---
  duration_ms: 0.457874
  ...
# Subtest: Less often at 90+ opens the constrained custom picker; 365 is unavailable
ok 1382 - Less often at 90+ opens the constrained custom picker; 365 is unavailable
  ---
  duration_ms: 0.272169
  ...
# Subtest: previewed dates are stable for one random draw
ok 1383 - previewed dates are stable for one random draw
  ---
  duration_ms: 0.282198
  ...
# Subtest: Keep saturates at 999 and Drop preserves keeps history
ok 1384 - Keep saturates at 999 and Drop preserves keeps history
  ---
  duration_ms: 0.326192
  ...
# Subtest: kept tails preserve roll classification; decisions break it deliberately
ok 1385 - kept tails preserve roll classification; decisions break it deliberately
  ---
  duration_ms: 0.782323
  ...
# Subtest: invalid priority config offers no priority-changing action
ok 1386 - invalid priority config offers no priority-changing action
  ---
  duration_ms: 0.231241
  ...
# Subtest: decay off disables Not now but keeps counting
ok 1387 - decay off disables Not now but keeps counting
  ---
  duration_ms: 0.200052
  ...
# Subtest: explicit level picks cover the ladder with previewed rolls
ok 1388 - explicit level picks cover the ladder with previewed rolls
  ---
  duration_ms: 0.788625
  ...
# Subtest: card model is deeply frozen
ok 1389 - card model is deeply frozen
  ---
  duration_ms: 0.1934
  ...
# Subtest: single Alt+F on an at-limit task opens the card and writes nothing
ok 1390 - single Alt+F on an at-limit task opens the card and writes nothing
  ---
  duration_ms: 10.181801
  ...
# Subtest: dismissing the card writes nothing and does not advance
ok 1391 - dismissing the card writes nothing and does not advance
  ---
  duration_ms: 1.734731
  ...
# Subtest: early dates open the card and write nothing
ok 1392 - early dates open the card and write nothing
  ---
  duration_ms: 1.569055
  ...
# Subtest: namespace v5 with decide true stamps counted and opens no card
ok 1393 - namespace v5 with decide true stamps counted and opens no card
  ---
  duration_ms: 5.193891
  ...
# Subtest: stale task-line change writes nothing
ok 1394 - stale task-line change writes nothing
  ---
  duration_ms: 1.570657
  ...
# Subtest: stale local-day change writes nothing
ok 1395 - stale local-day change writes nothing
  ---
  duration_ms: 1.532965
  ...
# Subtest: stale decay-config change writes nothing
ok 1396 - stale decay-config change writes nothing
  ---
  duration_ms: 1.563083
  ...
# Subtest: stale priority-ladder config writes nothing
ok 1397 - stale priority-ladder config writes nothing
  ---
  duration_ms: 2.024224
  ...
# Subtest: stale child Schedule Log writes nothing
ok 1398 - stale child Schedule Log writes nothing
  ---
  duration_ms: 2.277335
  ...
# Subtest: Not now stamps, clears keeps, and advances exactly once
ok 1399 - Not now stamps, clears keeps, and advances exactly once
  ---
  duration_ms: 5.396057
  ...
# Subtest: Keep counts once and saturates at 999 without reset
ok 1400 - Keep counts once and saturates at 999 without reset
  ---
  duration_ms: 3.352969
  ...
# Subtest: Keep with a reason logs that reason in the Rotten Log entry
ok 1401 - Keep with a reason logs that reason in the Rotten Log entry
  ---
  duration_ms: 1.259995
  ...
# Subtest: Keep carries the logged history and preview keeps in its context
ok 1402 - Keep carries the logged history and preview keeps in its context
  ---
  duration_ms: 1.321121
  ...
# Subtest: Keep with a stale child log during the stage refuses and rebuilds
ok 1403 - Keep with a stale child log during the stage refuses and rebuilds
  ---
  duration_ms: 1.104387
  ...
# Subtest: Keep with advance commits once and advances exactly once
ok 1404 - Keep with advance commits once and advances exactly once
  ---
  duration_ms: 1.34151
  ...
# Subtest: Reword stamps, clears, logs, and never advances
ok 1405 - Reword stamps, clears, logs, and never advances
  ---
  duration_ms: 1.521313
  ...
# Subtest: Drop cancels with the dropped-after-keeps reason and keeps history
ok 1406 - Drop cancels with the dropped-after-keeps reason and keeps history
  ---
  duration_ms: 1.140045
  ...
# Subtest: Less often at 90+ opens the picker and dismiss writes nothing
ok 1407 - Less often at 90+ opens the picker and dismiss writes nothing
  ---
  duration_ms: 1.086624
  ...
# Subtest: counted session skips at-limit and counts below-limit
ok 1408 - counted session skips at-limit and counts below-limit
  ---
  duration_ms: 1.380545
  ...
# Subtest: counted session skips at-limit on an early date
ok 1409 - counted session skips at-limit on an early date
  ---
  duration_ms: 1.058189
  ...
# Subtest: counted session with every target skipped writes nothing
ok 1410 - counted session with every target skipped writes nothing
  ---
  duration_ms: 0.491007
  ...
# Subtest: opening the card writes nothing and shows the Keep row detail
ok 1411 - opening the card writes nothing and shows the Keep row detail
  ---
  duration_ms: 12.37673
  ...
# Subtest: Esc on the rows closes the card and writes nothing
ok 1412 - Esc on the rows closes the card and writes nothing
  ---
  duration_ms: 2.484432
  ...
# Subtest: Keep swaps the rows for the reason stage without closing
ok 1413 - Keep swaps the rows for the reason stage without closing
  ---
  duration_ms: 3.170721
  ...
# Subtest: repeat Alt+F never enters or submits the stage
ok 1414 - repeat Alt+F never enters or submits the stage
  ---
  duration_ms: 2.57279
  ...
# Subtest: Esc in the stage returns to the rows; a second Esc writes nothing
ok 1415 - Esc in the stage returns to the rows; a second Esc writes nothing
  ---
  duration_ms: 2.359483
  ...
# Subtest: Keep stage Enter logs the reason with one transaction; one undo restores
ok 1416 - Keep stage Enter logs the reason with one transaction; one undo restores
  ---
  duration_ms: 17.796373
  ...
# Subtest: blank Keep stage Enter logs no reason given
ok 1417 - blank Keep stage Enter logs no reason given
  ---
  duration_ms: 13.413508
  ...
# Subtest: a double Enter submits once
ok 1418 - a double Enter submits once
  ---
  duration_ms: 13.237272
  ...
# Subtest: IME Enter never submits the stage
ok 1419 - IME Enter never submits the stage
  ---
  duration_ms: 2.996969
  ...
# Subtest: the card header shows the logged count and last reason
ok 1420 - the card header shows the logged count and last reason
  ---
  duration_ms: 2.495653
  ...
# Subtest: an unreadable log shows the header even with no countable entries
ok 1421 - an unreadable log shows the header even with no countable entries
  ---
  duration_ms: 0.222244
  ...
# Subtest: the decay card Keep stage uses the reviews streak copy
ok 1422 - the decay card Keep stage uses the reviews streak copy
  ---
  duration_ms: 0.224449
  ...
# Subtest: ambiguous Rotten Logs refuse the Keep write
ok 1423 - ambiguous Rotten Logs refuse the Keep write
  ---
  duration_ms: 1.349866
  ...
# Subtest: availability: decay on (or absent) may ask; decay off never asks
ok 1424 - availability: decay on (or absent) may ask; decay off never asks
  ---
  duration_ms: 1.261026
  ...
# Subtest: trigger: only an explicit decide row decides
ok 1425 - trigger: only an explicit decide row decides
  ---
  duration_ms: 0.208899
  ...
# Subtest: partition: exact at-limit rows skip, everything else stamps
ok 1426 - partition: exact at-limit rows skip, everything else stamps
  ---
  duration_ms: 0.715425
  ...
# Subtest: partition: empty and malformed input stamps nothing and skips nothing
ok 1427 - partition: empty and malformed input stamps nothing and skips nothing
  ---
  duration_ms: 0.144475
  ...
# Subtest: partition: enabled false stamps decision rows (older namespace fallback)
ok 1428 - partition: enabled false stamps decision rows (older namespace fallback)
  ---
  duration_ms: 0.160116
  ...
# Subtest: skip wording: singular, plural, and all-skipped notices
ok 1429 - skip wording: singular, plural, and all-skipped notices
  ---
  duration_ms: 0.194481
  ...
# Subtest: reword cursor: lands at the end of the task body before metadata
ok 1430 - reword cursor: lands at the end of the task body before metadata
  ---
  duration_ms: 0.402368
  ...
# Subtest: captured age: optional context ages, null when created is missing
ok 1431 - captured age: optional context ages, null when created is missing
  ---
  duration_ms: 0.458706
  ...
# Subtest: rows: P0 entry shows the recommended Not now with a clean window
ok 1432 - rows: P0 entry shows the recommended Not now with a clean window
  ---
  duration_ms: 3.149221
  ...
# Subtest: rows: invalid priority config disables Not now and levels, keeps safe rows
ok 1433 - rows: invalid priority config disables Not now and levels, keeps safe rows
  ---
  duration_ms: 0.660951
  ...
# Subtest: rows: picker-mode Less often and 365-day cap
ok 1434 - rows: picker-mode Less often and 365-day cap
  ---
  duration_ms: 0.957628
  ...
# Subtest: rows: terminal ladder keeps Enter available and never cancels
ok 1435 - rows: terminal ladder keeps Enter available and never cancels
  ---
  duration_ms: 0.622497
  ...
# Subtest: modal: Enter approves once; later keys cannot approve again
ok 1436 - modal: Enter approves once; later keys cannot approve again
  ---
  duration_ms: 0.579406
  ...
# Subtest: modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
ok 1437 - modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
  ---
  duration_ms: 0.420924
  ...
# Subtest: modal: key repeat and modified keys never approve
ok 1438 - modal: key repeat and modified keys never approve
  ---
  duration_ms: 0.242162
  ...
# Subtest: modal: Esc changes nothing — dismiss without a choice
ok 1439 - modal: Esc changes nothing — dismiss without a choice
  ---
  duration_ms: 0.139557
  ...
# Subtest: modal: unavailable actions cannot be chosen
ok 1440 - modal: unavailable actions cannot be chosen
  ---
  duration_ms: 0.160025
  ...
# Subtest: modal: a double callback applies once
ok 1441 - modal: a double callback applies once
  ---
  duration_ms: 0.112445
  ...
# Subtest: capability: the nav api exposes the card while loaded
ok 1442 - capability: the nav api exposes the card while loaded
  ---
  duration_ms: 0.480016
  ...
# Subtest: capability: unload drops the card so marks stop promising it
ok 1443 - capability: unload drops the card so marks stop promising it
  ---
  duration_ms: 0.163281
  ...
# Subtest: ladder lookup: the first priority property wins, null without one
ok 1444 - ladder lookup: the first priority property wins, null without one
  ---
  duration_ms: 0.176176
  ...
# Subtest: stage entry resolves the line itself and refuses prose
ok 1445 - stage entry resolves the line itself and refuses prose
  ---
  duration_ms: 4.091047
  ...
# Subtest: Ctrl+Shift+P on a BLOCKS line opens the owner's Blocks stage directly
ok 1446 - Ctrl+Shift+P on a BLOCKS line opens the owner's Blocks stage directly
  ---
  duration_ms: 1.727838
  ...
# Subtest: Ctrl+Shift+P hotkey path on a BLOCKS line opens the owner's Blocks stage directly
ok 1447 - Ctrl+Shift+P hotkey path on a BLOCKS line opens the owner's Blocks stage directly
  ---
  duration_ms: 0.923393
  ...
# Subtest: Ctrl+Shift+Alt+B on a BLOCKS or Depends-On line opens the owner's Blocks stage
ok 1448 - Ctrl+Shift+Alt+B on a BLOCKS or Depends-On line opens the owner's Blocks stage
  ---
  duration_ms: 0.531034
  ...
# Subtest: Ctrl+Shift+P on a Depends-On line is unchanged forward behavior
ok 1449 - Ctrl+Shift+P on a Depends-On line is unchanged forward behavior
  ---
  duration_ms: 0.618941
  ...
# Subtest: Ctrl+Shift+P on a plain child bullet and a nested Task Link are unchanged (3e359a6)
ok 1450 - Ctrl+Shift+P on a plain child bullet and a nested Task Link are unchanged (3e359a6)
  ---
  duration_ms: 8.729267
  ...
# Subtest: forward counted mixed row in BLOCKED keeps the waits-on badge (3e359a6 order)
ok 1451 - forward counted mixed row in BLOCKED keeps the waits-on badge (3e359a6 order)
  ---
  duration_ms: 2.849599
  ...
# Subtest: api.blocks opens the stage and removes only a listed dependent
ok 1452 - api.blocks opens the stage and removes only a listed dependent
  ---
  duration_ms: 2.288227
  ...
# Subtest: api.blocks removeDependent on an owner with no ^id is not-a-dependent
ok 1453 - api.blocks removeDependent on an owner with no ^id is not-a-dependent
  ---
  duration_ms: 0.517618
  ...
# Subtest: stage canonical order ranks \#hide last ahead of the lane
ok 1454 - stage canonical order ranks \#hide last ahead of the lane
  ---
  duration_ms: 0.529461
  ...
# Subtest: stage empty query shows same-note plus In Progress and Next only
ok 1455 - stage empty query shows same-note plus In Progress and Next only
  ---
  duration_ms: 3.006146
  ...
# Subtest: stage cap appends a type-to-search-more hint row
ok 1456 - stage cap appends a type-to-search-more hint row
  ---
  duration_ms: 4.090196
  ...
# Subtest: stage BLOCKED rows carry waits-on counts and short guard reasons
ok 1457 - stage BLOCKED rows carry waits-on counts and short guard reasons
  ---
  duration_ms: 1.460628
  ...
# Subtest: stage removal notices name the task description, not the block id
ok 1458 - stage removal notices name the task description, not the block id
  ---
  duration_ms: 0.519001
  ...
# Subtest: stage Task Link batches keep Depends on without refusal
ok 1459 - stage Task Link batches keep Depends on without refusal
  ---
  duration_ms: 0.54998
  ...
# Subtest: stage batch cycle check runs on the post-batch graph
ok 1460 - stage batch cycle check runs on the post-batch graph
  ---
  duration_ms: 0.49789
  ...
# Subtest: stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
ok 1461 - stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
  ---
  duration_ms: 12.615345
  ...
# Subtest: stage stale single add refuses and reopens
ok 1462 - stage stale single add refuses and reopens
  ---
  duration_ms: 1.358202
  ...
# Subtest: Task Link Depends on focuses a linked note open in a background tab
ok 1463 - Task Link Depends on focuses a linked note open in a background tab
  ---
  duration_ms: 0.378262
  ...
# Subtest: Task Link Blocks focuses the linked note and opens Blocks directly
ok 1464 - Task Link Blocks focuses the linked note and opens Blocks directly
  ---
  duration_ms: 0.381388
  ...
# Subtest: Task Link Depends on refuses clearly when the linked note cannot be focused
    # Subtest: focus reports success but the active view stays elsewhere
    ok 1 - focus reports success but the active view stays elsewhere
      ---
      duration_ms: 0.247642
      ...
    # Subtest: focus reports failure
    ok 2 - focus reports failure
      ---
      duration_ms: 0.226362
      ...
    1..2
ok 1465 - Task Link Depends on refuses clearly when the linked note cannot be focused
  ---
  duration_ms: 0.828161
  ...
# Subtest: stage mirror burst keeps the baseline owner across an insertion above
ok 1466 - stage mirror burst keeps the baseline owner across an insertion above
  ---
  duration_ms: 1004.939085
  ...
# Subtest: stage mirror burst clears on a text-only line deletion
ok 1467 - stage mirror burst clears on a text-only line deletion
  ---
  duration_ms: 1001.384533
  ...
# Subtest: stage mirror vim dd clears the deleted line's owner
ok 1468 - stage mirror vim dd clears the deleted line's owner
  ---
  duration_ms: 1001.160664
  ...
# Subtest: stage badge counts open prerequisites without a block id
ok 1469 - stage badge counts open prerequisites without a block id
  ---
  duration_ms: 4.880575
  ...
# Subtest: stage badge names the future scheduled date with no open prerequisite
ok 1470 - stage badge names the future scheduled date with no open prerequisite
  ---
  duration_ms: 1.405382
  ...
# Subtest: stage badge reads blocked with nothing waiting and no schedule
ok 1471 - stage badge reads blocked with nothing waiting and no schedule
  ---
  duration_ms: 0.802321
  ...
# Subtest: stage vault batch with a stale row refuses and reopens
ok 1472 - stage vault batch with a stale row refuses and reopens
  ---
  duration_ms: 6.797182
  ...
# Subtest: stage opening builds 200/400/1000-task notes without cubic growth
ok 1473 - stage opening builds 200/400/1000-task notes without cubic growth
  ---
  duration_ms: 43.89504
  ...
# Subtest: stage snapshots match standalone parsing across grammar vectors
ok 1474 - stage snapshots match standalone parsing across grammar vectors
  ---
  duration_ms: 6.975061
  ...
# Subtest: stage Warm-empty cache is ready without a vault fallback
ok 1475 - stage Warm-empty cache is ready without a vault fallback
  ---
  duration_ms: 0.672323
  ...
# Subtest: stage opening renders cross-note results with zero writes and cap
ok 1476 - stage opening renders cross-note results with zero writes and cap
  ---
  duration_ms: 46.093975
  ...
# Subtest: stage CURRENT covers same-note, cross-note, blocked, and counted parents
ok 1477 - stage CURRENT covers same-note, cross-note, blocked, and counted parents
  ---
  duration_ms: 1.516665
  ...
# Subtest: stage collections reuse one snapshot per parent
ok 1478 - stage collections reuse one snapshot per parent
  ---
  duration_ms: 0.347905
  ...
# Subtest: stage cold refresh yields, preserves state, and performs no search reads
ok 1479 - stage cold refresh yields, preserves state, and performs no search reads
  ---
  duration_ms: 116.924458
  ...
# Subtest: stage cold refresh abandons after dismissal or replacement
ok 1480 - stage cold refresh abandons after dismissal or replacement
  ---
  duration_ms: 54.409626
  ...
# Subtest: stage 400-task opening finishes in a child process before the parent timeout
ok 1481 - stage 400-task opening finishes in a child process before the parent timeout
  ---
  duration_ms: 89.779885
  ...
# Subtest: stage ranker passes the DK contract vectors verbatim
ok 1482 - stage ranker passes the DK contract vectors verbatim
  ---
  duration_ms: 2.948076
  ...
# Subtest: stage ranker tiers match the capture ranker tier order
ok 1483 - stage ranker tiers match the capture ranker tier order
  ---
  duration_ms: 1.691879
  ...
# Subtest: stage pool excludes daily notes, done, templates, and dot-dirs
ok 1484 - stage pool excludes daily notes, done, templates, and dot-dirs
  ---
  duration_ms: 0.770431
  ...
# Subtest: stage pool collects open vault tasks with buffers as given
ok 1485 - stage pool collects open vault tasks with buffers as given
  ---
  duration_ms: 2.912719
  ...
# Subtest: stage CURRENT resolves same-note, missing, closed, and non-task targets
ok 1486 - stage CURRENT resolves same-note, missing, closed, and non-task targets
  ---
  duration_ms: 2.276996
  ...
# Subtest: stage cycle guard reports the path back to the dependent
ok 1487 - stage cycle guard reports the path back to the dependent
  ---
  duration_ms: 0.846024
  ...
# Subtest: stage view groups CURRENT, RESULTS, and BLOCKED with guards
ok 1488 - stage view groups CURRENT, RESULTS, and BLOCKED with guards
  ---
  duration_ms: 2.60458
  ...
# Subtest: stage view disables cycles and unencodable targets, keeps +id rows
ok 1489 - stage view disables cycles and unencodable targets, keeps +id rows
  ---
  duration_ms: 1.067347
  ...
# Subtest: stage cache tasks normalize across Tasks shapes, buffers win
ok 1490 - stage cache tasks normalize across Tasks shapes, buffers win
  ---
  duration_ms: 0.834593
  ...
# Subtest: stage Task Link mode shows Depends on for one link and batches
ok 1491 - stage Task Link mode shows Depends on for one link and batches
  ---
  duration_ms: 0.863358
  ...
# Subtest: stage mark keys never collide across notes
ok 1492 - stage mark keys never collide across notes
  ---
  duration_ms: 0.203929
  ...
# Subtest: stage display-text locating matches one open task
ok 1493 - stage display-text locating matches one open task
  ---
  duration_ms: 0.239667
  ...
# Subtest: stage selection refusal spans tasks only
ok 1494 - stage selection refusal spans tasks only
  ---
  duration_ms: 0.263293
  ...
# Subtest: stage builder composes pool, current, guards, and pill title
ok 1495 - stage builder composes pool, current, guards, and pill title
  ---
  duration_ms: 2.093485
  ...
# Subtest: stage counted vault add with a stale target refuses and reopens
ok 1496 - stage counted vault add with a stale target refuses and reopens
  ---
  duration_ms: 10.172032
  ...
# Subtest: stage vault commit with a stale write notifies once and reopens
ok 1497 - stage vault commit with a stale write notifies once and reopens
  ---
  duration_ms: 7.814182
  ...
# Subtest: commitVaultRefs refuses a cycle through implicit resident edges
ok 1498 - commitVaultRefs refuses a cycle through implicit resident edges
  ---
  duration_ms: 2.16374
  ...
# Subtest: stage single remove with a stale write notifies once and reopens
ok 1499 - stage single remove with a stale write notifies once and reopens
  ---
  duration_ms: 2.78769
  ...
# Subtest: stage vault single +id guard refuses a stale target
ok 1500 - stage vault single +id guard refuses a stale target
  ---
  duration_ms: 1.426062
  ...
# Subtest: stage vault counted +id guard refuses a stale target
ok 1501 - stage vault counted +id guard refuses a stale target
  ---
  duration_ms: 0.852717
  ...
# Subtest: stage single +id guard refuses a stale target
ok 1502 - stage single +id guard refuses a stale target
  ---
  duration_ms: 0.852356
  ...
# Subtest: stage counted remove with a stale write refuses and reopens
ok 1503 - stage counted remove with a stale write refuses and reopens
  ---
  duration_ms: 2.827846
  ...
# Subtest: stage counted remove counts only changed sources
ok 1504 - stage counted remove counts only changed sources
  ---
  duration_ms: 4.81035
  ...
# Subtest: counted local add on [?] sources reads zero extra notes
ok 1505 - counted local add on [?] sources reads zero extra notes
  ---
  duration_ms: 5.918725
  ...
# Subtest: counted local toggle-off on a Pomodoro-linked [?] source recovers
ok 1506 - counted local toggle-off on a Pomodoro-linked [?] source recovers
  ---
  duration_ms: 7.345007
  ...
# Subtest: stage counted vault add counts only changed sources
ok 1507 - stage counted vault add counts only changed sources
  ---
  duration_ms: 2.815813
  ...
# Subtest: stage counted vault remove counts only changed sources
ok 1508 - stage counted vault remove counts only changed sources
  ---
  duration_ms: 1.513939
  ...
# Subtest: stage +id row prompts without writing
ok 1509 - stage +id row prompts without writing
  ---
  duration_ms: 11.731408
  ...
# Subtest: stage dismissal writes no bytes and drops the batch
ok 1510 - stage dismissal writes no bytes and drops the batch
  ---
  duration_ms: 1.555238
  ...
# Subtest: stage same-note batch commits in one undo group
ok 1511 - stage same-note batch commits in one undo group
  ---
  duration_ms: 13.004758
  ...
# Subtest: stage batch with a stale row refuses and reopens
ok 1512 - stage batch with a stale row refuses and reopens
  ---
  duration_ms: 1.376277
  ...
# Subtest: stage counted add applies to every source task
ok 1513 - stage counted add applies to every source task
  ---
  duration_ms: 37.475448
  ...
# Subtest: stage batch cycle rows stay guarded and write nothing
ok 1514 - stage batch cycle rows stay guarded and write nothing
  ---
  duration_ms: 29.598845
  ...
# Subtest: stage edit-task-dependencies registers with no default hotkey
ok 1515 - stage edit-task-dependencies registers with no default hotkey
  ---
  duration_ms: 1.998915
  ...
# Subtest: task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row
ok 1516 - task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row
  ---
  duration_ms: 1.162228
  ...
# Subtest: task-card-blocks registers Ctrl+Shift+Alt+B and opens the Blocks row
ok 1517 - task-card-blocks registers Ctrl+Shift+Alt+B and opens the Blocks row
  ---
  duration_ms: 0.749891
  ...
# Subtest: stage waits-on badge counts open prerequisites only
ok 1518 - stage waits-on badge counts open prerequisites only
  ---
  duration_ms: 2.709551
  ...
# Subtest: stage cycle tooltip shows task descriptions
ok 1519 - stage cycle tooltip shows task descriptions
  ---
  duration_ms: 1.753145
  ...
# Subtest: stage same-note single add stamps the dependent and keeps its cursor
ok 1520 - stage same-note single add stamps the dependent and keeps its cursor
  ---
  duration_ms: 6.868288
  ...
# Subtest: stage same-note marked batch stamps the dependent and keeps its cursor
ok 1521 - stage same-note marked batch stamps the dependent and keeps its cursor
  ---
  duration_ms: 8.091962
  ...
# Subtest: Tab marks a same-note CURRENT row and Enter removes it
ok 1522 - Tab marks a same-note CURRENT row and Enter removes it
  ---
  duration_ms: 33.235768
  ...
# Subtest: Tab twice unmarks a CURRENT row
ok 1523 - Tab twice unmarks a CURRENT row
  ---
  duration_ms: 27.427723
  ...
# Subtest: Tab mixed CURRENT removal and RESULTS add apply in one commit
ok 1524 - Tab mixed CURRENT removal and RESULTS add apply in one commit
  ---
  duration_ms: 30.03504
  ...
# Subtest: Tab marks a missing CURRENT target and the batch removes it
ok 1525 - Tab marks a missing CURRENT target and the batch removes it
  ---
  duration_ms: 30.703965
  ...
# Subtest: Tab same-note and cross-note CURRENT removals apply in one vault batch
ok 1526 - Tab same-note and cross-note CURRENT removals apply in one vault batch
  ---
  duration_ms: 31.578405
  ...
# Subtest: cross-note add awaits preparation before the one commit
ok 1527 - cross-note add awaits preparation before the one commit
  ---
  duration_ms: 18.219
  ...
# Subtest: a failed async preparation leaves the dependent untouched
ok 1528 - a failed async preparation leaves the dependent untouched
  ---
  duration_ms: 7.034574
  ...
# Subtest: links to unloaded notes tolerate add, remove, and deleted targets
ok 1529 - links to unloaded notes tolerate add, remove, and deleted targets
  ---
  duration_ms: 3.307282
  ...
# Subtest: Pomodoro-linked dependents recover through the plugin vault read
ok 1530 - Pomodoro-linked dependents recover through the plugin vault read
  ---
  duration_ms: 5.233648
  ...
# Subtest: same-note batch +id stamps the target and links in one undo group
ok 1531 - same-note batch +id stamps the target and links in one undo group
  ---
  duration_ms: 8.091543
  ...
# Subtest: confirmBatchBlockId collects the id and executes the batch
ok 1532 - confirmBatchBlockId collects the id and executes the batch
  ---
  duration_ms: 2.166054
  ...
# Subtest: commitMarkedDependencies executes ready additions at once
ok 1533 - commitMarkedDependencies executes ready additions at once
  ---
  duration_ms: 3.270992
  ...
# Subtest: counted vault add links two siblings bottom-up
ok 1534 - counted vault add links two siblings bottom-up
  ---
  duration_ms: 3.582707
  ...
# Subtest: counted CURRENT rows without a line remove from every source
ok 1535 - counted CURRENT rows without a line remove from every source
  ---
  duration_ms: 6.029146
  ...
# Subtest: a stale editor between await and commit refuses
ok 1536 - a stale editor between await and commit refuses
  ---
  duration_ms: 1.440539
  ...
# Subtest: removeDependencyByRef refuses targets that are not on the line
ok 1537 - removeDependencyByRef refuses targets that are not on the line
  ---
  duration_ms: 1.213746
  ...
# Subtest: kept unloaded links resolve the field id by line position
ok 1538 - kept unloaded links resolve the field id by line position
  ---
  duration_ms: 2.567329
  ...
# Subtest: pendingTargetLine commits the same-note target id with the link
ok 1539 - pendingTargetLine commits the same-note target id with the link
  ---
  duration_ms: 2.624169
  ...
# Subtest: counted vault add commits every source in one transaction
ok 1540 - counted vault add commits every source in one transaction
  ---
  duration_ms: 3.241637
  ...
# Subtest: field-only clears snapshot the vault and recover
ok 1541 - field-only clears snapshot the vault and recover
  ---
  duration_ms: 1.636332
  ...
# Subtest: adds without recovery read zero extra vault notes
ok 1542 - adds without recovery read zero extra vault notes
  ---
  duration_ms: 0.792623
  ...
# Subtest: hand-edit clear recovers Pomodoro-linked dependents to Next
ok 1543 - hand-edit clear recovers Pomodoro-linked dependents to Next
  ---
  duration_ms: 1.004577
  ...
# Subtest: hand-edit clear on a non-Blocked parent reads zero extra notes
ok 1544 - hand-edit clear on a non-Blocked parent reads zero extra notes
  ---
  duration_ms: 0.446051
  ...
# Subtest: writer keeps the full route for duplicate basenames
ok 1545 - writer keeps the full route for duplicate basenames
  ---
  duration_ms: 2.331389
  ...
# Subtest: adds on Blocked parents and non-Blocked mirror touches read nothing
ok 1546 - adds on Blocked parents and non-Blocked mirror touches read nothing
  ---
  duration_ms: 1.121621
  ...
# Subtest: counted vault add loads each source's existing links
ok 1547 - counted vault add loads each source's existing links
  ---
  duration_ms: 3.760286
  ...
# Subtest: counted Ctrl+D on a blockquoted task refuses with the blockquote notice
ok 1548 - counted Ctrl+D on a blockquoted task refuses with the blockquote notice
  ---
  duration_ms: 0.729792
  ...
# Subtest: single Ctrl+D on a quoted task without a field refuses as a blockquote
ok 1549 - single Ctrl+D on a quoted task without a field refuses as a blockquote
  ---
  duration_ms: 0.239928
  ...
# Subtest: confirmSingleBlockId folds the target id into one transaction
ok 1550 - confirmSingleBlockId folds the target id into one transaction
  ---
  duration_ms: 3.206188
  ...
# Subtest: chooseTaskDependency folds a missing target id into one transaction
ok 1551 - chooseTaskDependency folds a missing target id into one transaction
  ---
  duration_ms: 2.744678
  ...
# Subtest: counted remove commits every source in one transaction
ok 1552 - counted remove commits every source in one transaction
  ---
  duration_ms: 4.34865
  ...
# Subtest: DP parse vectors accept, empty, malformed, and not-a-line
ok 1553 - DP parse vectors accept, empty, malformed, and not-a-line
  ---
  duration_ms: 2.430348
  ...
# Subtest: DP30 attributes a Work-Log-nested Depends-On line to the inner task
ok 1554 - DP30 attributes a Work-Log-nested Depends-On line to the inner task
  ---
  duration_ms: 1.897562
  ...
# Subtest: fenced lines never collect as Depends-On lines
ok 1555 - fenced lines never collect as Depends-On lines
  ---
  duration_ms: 0.318017
  ...
# Subtest: DW1 creates the line as the first child
ok 1556 - DW1 creates the line as the first child
  ---
  duration_ms: 4.3022
  ...
# Subtest: DW2 creates the line after a Cancel Log
ok 1557 - DW2 creates the line after a Cancel Log
  ---
  duration_ms: 0.993105
  ...
# Subtest: DW3-DW5 append, remove the middle, and delete on the last link
ok 1558 - DW3-DW5 append, remove the middle, and delete on the last link
  ---
  duration_ms: 5.055067
  ...
# Subtest: DW6-DW7 re-add moves to the end and the field mirrors the line
ok 1559 - DW6-DW7 re-add moves to the end and the field mirrors the line
  ---
  duration_ms: 1.025708
  ...
# Subtest: DW8 tab parents deepen the child by one tab
ok 1560 - DW8 tab parents deepen the child by one tab
  ---
  duration_ms: 1.550039
  ...
# Subtest: DW9 space parents reuse the existing child indent
ok 1561 - DW9 space parents reuse the existing child indent
  ---
  duration_ms: 1.153862
  ...
# Subtest: DW10-DW11 CRLF and final-newline state survive
ok 1562 - DW10-DW11 CRLF and final-newline state survive
  ---
  duration_ms: 1.17373
  ...
# Subtest: DW12-DW14 link form is the shortest unambiguous form
ok 1563 - DW12-DW14 link form is the shortest unambiguous form
  ---
  duration_ms: 0.352923
  ...
# Subtest: archive targets keep the explicit done/ path form
ok 1564 - archive targets keep the explicit done/ path form
  ---
  duration_ms: 0.234898
  ...
# Subtest: DW15 an existing id is never rewritten
ok 1565 - DW15 an existing id is never rewritten
  ---
  duration_ms: 0.396467
  ...
# Subtest: DW16 an unencodable path without an id refuses
ok 1566 - DW16 an unencodable path without an id refuses
  ---
  duration_ms: 0.339047
  ...
# Subtest: DW17 field placement follows fresh and precedes the block id
ok 1567 - DW17 field placement follows fresh and precedes the block id
  ---
  duration_ms: 0.326312
  ...
# Subtest: DW18 legacy children fold into the line
ok 1568 - DW18 legacy children fold into the line
  ---
  duration_ms: 0.898334
  ...
# Subtest: DW19 variants canonicalise to the writer form
ok 1569 - DW19 variants canonicalise to the writer form
  ---
  duration_ms: 1.484683
  ...
# Subtest: adding an open prerequisite blocks the dependent
ok 1570 - adding an open prerequisite blocks the dependent
  ---
  duration_ms: 0.360669
  ...
# Subtest: adding transfers Next and In Progress commitment to the open target
ok 1571 - adding transfers Next and In Progress commitment to the open target
  ---
  duration_ms: 0.551733
  ...
# Subtest: removing the last open prerequisite recovers immediately
ok 1572 - removing the last open prerequisite recovers immediately
  ---
  duration_ms: 0.819183
  ...
# Subtest: removal stays Blocked while another prerequisite is open
ok 1573 - removal stays Blocked while another prerequisite is open
  ---
  duration_ms: 0.522627
  ...
# Subtest: removal stays Blocked with a future schedule
ok 1574 - removal stays Blocked with a future schedule
  ---
  duration_ms: 0.376087
  ...
# Subtest: one gesture commits the dependent note in a single transaction
ok 1575 - one gesture commits the dependent note in a single transaction
  ---
  duration_ms: 1.694934
  ...
# Subtest: a failed preparation leaves the dependent untouched
ok 1576 - a failed preparation leaves the dependent untouched
  ---
  duration_ms: 0.381939
  ...
# Subtest: recovery references follow the line plus covered legacy children
ok 1577 - recovery references follow the line plus covered legacy children
  ---
  duration_ms: 0.427285
  ...
# Subtest: task-block helpers find owners, lines, and insertion points
ok 1578 - task-block helpers find owners, lines, and insertion points
  ---
  duration_ms: 0.30872
  ...
# Subtest: dependency notices follow the contract shapes
ok 1579 - dependency notices follow the contract shapes
  ---
  duration_ms: 0.13644
  ...
# Subtest: nav api v3 resolves results and never throws
ok 1580 - nav api v3 resolves results and never throws
  ---
  duration_ms: 1.095821
  ...
# Subtest: getDependencyInsertLine lands after a Cancel Log subtree
ok 1581 - getDependencyInsertLine lands after a Cancel Log subtree
  ---
  duration_ms: 0.210893
  ...
# Subtest: planner: an ordinary dependent with a block id plus an open add yields one target
ok 1582 - planner: an ordinary dependent with a block id plus an open add yields one target
  ---
  duration_ms: 7.010248
  ...
# Subtest: planner: adding only a closed target yields none
ok 1583 - planner: adding only a closed target yields none
  ---
  duration_ms: 0.865882
  ...
# Subtest: planner: no block id yields none
ok 1584 - planner: no block id yields none
  ---
  duration_ms: 0.452153
  ...
# Subtest: planner: a dependent already [?] with an open add yields a target
ok 1585 - planner: a dependent already [?] with an open add yields a target
  ---
  duration_ms: 1.621224
  ...
# Subtest: planner: a removal yields none
ok 1586 - planner: a removal yields none
  ---
  duration_ms: 1.392377
  ...
# Subtest: planner: mirrorTouch emits no ordinary consumption target
ok 1587 - planner: mirrorTouch emits no ordinary consumption target
  ---
  duration_ms: 0.630564
  ...
# Subtest: planner: ^prj keeps project targets and a deduplicated union
ok 1588 - planner: ^prj keeps project targets and a deduplicated union
  ---
  duration_ms: 2.360905
  ...
# Subtest: suffix helper names the removed count and the failed follow-up
ok 1589 - suffix helper names the removed count and the failed follow-up
  ---
  duration_ms: 0.194731
  ...
# Subtest: applyDependencyEdit cross-file consumes live links and emptied entries
ok 1590 - applyDependencyEdit cross-file consumes live links and emptied entries
  ---
  duration_ms: 8.842154
  ...
# Subtest: applyDependencyEdit removes one live link and reports it
ok 1591 - applyDependencyEdit removes one live link and reports it
  ---
  duration_ms: 2.385643
  ...
# Subtest: applyDependencyEdit keeps the dependent write when the daily preimage changes
ok 1592 - applyDependencyEdit keeps the dependent write when the daily preimage changes
  ---
  duration_ms: 1.365786
  ...
# Subtest: same-file fold lands the dependency and the cleanup in one undo group
ok 1593 - same-file fold lands the dependency and the cleanup in one undo group
  ---
  duration_ms: 1.657113
  ...
# Subtest: setLocalTaskDependencyLink stays synchronous and folds same-file cleanup
ok 1594 - setLocalTaskDependencyLink stays synchronous and folds same-file cleanup
  ---
  duration_ms: 2.041846
  ...
# Subtest: setLocalTaskDependencyLink cross-file continuation removes the live link
ok 1595 - setLocalTaskDependencyLink cross-file continuation removes the live link
  ---
  duration_ms: 10.604809
  ...
# Subtest: same-note marked batch consumes every newly Blocked source
ok 1596 - same-note marked batch consumes every newly Blocked source
  ---
  duration_ms: 9.298465
  ...
# Subtest: counted same-note writer consumes every newly Blocked source
ok 1597 - counted same-note writer consumes every newly Blocked source
  ---
  duration_ms: 4.263896
  ...
# Subtest: counted vault writer consumes every newly Blocked source
ok 1598 - counted vault writer consumes every newly Blocked source
  ---
  duration_ms: 3.720721
  ...
# Subtest: counted ^prj source consumes its project targets
ok 1599 - counted ^prj source consumes its project targets
  ---
  duration_ms: 3.36398
  ...
# Subtest: a dependent without a block id does zero cachedReads even when today's daily exists
ok 1600 - a dependent without a block id does zero cachedReads even when today's daily exists
  ---
  duration_ms: 1.601225
  ...
# Subtest: alignment key ignores fields, the block id, the status and trailing space
ok 1601 - alignment key ignores fields, the block id, the status and trailing space
  ---
  duration_ms: 1.772613
  ...
# Subtest: insertion after a modified line edits that line and inserts after it
ok 1602 - insertion after a modified line edits that line and inserts after it
  ---
  duration_ms: 2.301583
  ...
# Subtest: adjacent prerequisite and parent both change while two lines insert
ok 1603 - adjacent prerequisite and parent both change while two lines insert
  ---
  duration_ms: 0.632097
  ...
# Subtest: deletion at the end of the document
ok 1604 - deletion at the end of the document
  ---
  duration_ms: 0.477261
  ...
# Subtest: insertion at the top and at the end of the document
ok 1605 - insertion at the top and at the end of the document
  ---
  duration_ms: 0.447334
  ...
# Subtest: empty documents align and apply
ok 1606 - empty documents align and apply
  ---
  duration_ms: 0.261519
  ...
# Subtest: CRLF documents insert and delete with CRLF
ok 1607 - CRLF documents insert and delete with CRLF
  ---
  duration_ms: 0.393521
  ...
# Subtest: equal-count shifted edits take the aligned path
ok 1608 - equal-count shifted edits take the aligned path
  ---
  duration_ms: 0.610836
  ...
# Subtest: pure in-place edits keep the line-bounded change shapes
ok 1609 - pure in-place edits keep the line-bounded change shapes
  ---
  duration_ms: 0.888195
  ...
# Subtest: an unchanged document writes nothing
ok 1610 - an unchanged document writes nothing
  ---
  duration_ms: 0.423579
  ...
# Subtest: an explicit final cursor wins over the mapped cursor
ok 1611 - an explicit final cursor wins over the mapped cursor
  ---
  duration_ms: 0.267882
  ...
# Subtest: the machine-write annotation still reaches the transaction
ok 1612 - the machine-write annotation still reaches the transaction
  ---
  duration_ms: 0.166367
  ...
# Subtest: an editor without transaction falls back to bottom-up replaceRange
ok 1613 - an editor without transaction falls back to bottom-up replaceRange
  ---
  duration_ms: 0.315562
  ...
# Subtest: positions map through aligned, changed, gap and deleted lines
ok 1614 - positions map through aligned, changed, gap and deleted lines
  ---
  duration_ms: 0.396687
  ...
# Subtest: a deletion at the end of the document maps to the last line
ok 1615 - a deletion at the end of the document maps to the last line
  ---
  duration_ms: 0.111583
  ...
# Subtest: a gap with new lines maps by offset and clamps to its last line
ok 1616 - a gap with new lines maps by offset and clamps to its last line
  ---
  duration_ms: 0.154054
  ...
# Subtest: seeded property: planned changes rebuild the new text and map unchanged lines
ok 1617 - seeded property: planned changes rebuild the new text and map unchanged lines
  ---
  duration_ms: 39.712998
  ...
# Subtest: a diff past the edit cap becomes one unaligned gap
ok 1618 - a diff past the edit cap becomes one unaligned gap
  ---
  duration_ms: 78.647441
  ...
# Subtest: the CM6 double reproduces the whole-document replacement jump
ok 1619 - the CM6 double reproduces the whole-document replacement jump
  ---
  duration_ms: 0.621686
  ...
# Subtest: first cross-note prerequisite keeps the cursor and the viewport
ok 1620 - first cross-note prerequisite keeps the cursor and the viewport
  ---
  duration_ms: 5.402209
  ...
# Subtest: same-note prerequisite directly above keeps the dependent's line
ok 1621 - same-note prerequisite directly above keeps the dependent's line
  ---
  duration_ms: 3.16429
  ...
# Subtest: removing the last prerequisite keeps the dependent's line
ok 1622 - removing the last prerequisite keeps the dependent's line
  ---
  duration_ms: 3.920261
  ...
# Subtest: a Blocks source gaining its first BLOCKS line keeps its line
ok 1623 - a Blocks source gaining its first BLOCKS line keeps its line
  ---
  duration_ms: 0.468193
  ...
# Subtest: missing ledger-tools api refuses the review namespace
ok 1624 - missing ledger-tools api refuses the review namespace
  ---
  duration_ms: 1.82353
  ...
# Subtest: review jump on an empty queue
ok 1625 - review jump on an empty queue
  ---
  duration_ms: 1.006591
  ...
# Subtest: review jump from a queued task goes to the neighbor
ok 1626 - review jump from a queued task goes to the neighbor
  ---
  duration_ms: 0.737718
  ...
# Subtest: review jump wraps at the ends
ok 1627 - review jump wraps at the ends
  ---
  duration_ms: 0.284864
  ...
# Subtest: review jump from elsewhere goes to the first or last entry
ok 1628 - review jump from elsewhere goes to the first or last entry
  ---
  duration_ms: 0.184032
  ...
# Subtest: review jump matches a moved cursor task by text
ok 1629 - review jump matches a moved cursor task by text
  ---
  duration_ms: 0.152611
  ...
# Subtest: review jump from a just-stamped rank goes to the entry after it
ok 1630 - review jump from a just-stamped rank goes to the entry after it
  ---
  duration_ms: 0.2619
  ...
# Subtest: review jump skips just-stamped keys the lagging cache still shows
ok 1631 - review jump skips just-stamped keys the lagging cache still shows
  ---
  duration_ms: 0.144546
  ...
# Subtest: review jump after stamping everything reports empty or wraps
ok 1632 - review jump after stamping everything reports empty or wraps
  ---
  duration_ms: 0.536033
  ...
# Subtest: review queue line resolves at the entry line
ok 1633 - review queue line resolves at the entry line
  ---
  duration_ms: 0.532196
  ...
# Subtest: review queue line follows a moved line to its unique match
ok 1634 - review queue line follows a moved line to its unique match
  ---
  duration_ms: 0.417216
  ...
# Subtest: review queue line goes stale on duplicates or a missing line
ok 1635 - review queue line goes stale on duplicates or a missing line
  ---
  duration_ms: 0.198418
  ...
# Subtest: review jump notices name the state
ok 1636 - review jump notices name the state
  ---
  duration_ms: 0.425772
  ...
# Subtest: fresh stamp targets refuse closed and recurring tasks
ok 1637 - fresh stamp targets refuse closed and recurring tasks
  ---
  duration_ms: 0.653717
  ...
# Subtest: fresh stamp batch stamps every target and nothing else
ok 1638 - fresh stamp batch stamps every target and nothing else
  ---
  duration_ms: 0.377441
  ...
# Subtest: one refusal refuses the whole fresh stamp batch
ok 1639 - one refusal refuses the whole fresh stamp batch
  ---
  duration_ms: 0.367942
  ...
# Subtest: a throwing stamper refuses the fresh stamp batch
ok 1640 - a throwing stamper refuses the fresh stamp batch
  ---
  duration_ms: 0.194842
  ...
# Subtest: fresh stamp plus Work Log prepends only stamped Pending targets
ok 1641 - fresh stamp plus Work Log prepends only stamped Pending targets
  ---
  duration_ms: 1.17909
  ...
# Subtest: blank Work Log summary and stamp refusal never create a log marker
ok 1642 - blank Work Log summary and stamp refusal never create a log marker
  ---
  duration_ms: 0.270967
  ...
# Subtest: fresh stamp notices adjust the pre-write counts
ok 1643 - fresh stamp notices adjust the pre-write counts
  ---
  duration_ms: 0.223126
  ...
# Subtest: today detection only matches today's fresh field
ok 1644 - today detection only matches today's fresh field
  ---
  duration_ms: 0.189321
  ...
# Subtest: stamped refs match the pre-write queue by line or text
ok 1645 - stamped refs match the pre-write queue by line or text
  ---
  duration_ms: 0.344677
  ...
# Subtest: review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
ok 1646 - review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
  ---
  duration_ms: 0.234768
  ...
# Subtest: tier-aware jump notices name each tier
ok 1647 - tier-aware jump notices name each tier
  ---
  duration_ms: 0.577532
  ...
# Subtest: projects tier walks with commitment rank and empty-project notice
ok 1648 - projects tier walks with commitment rank and empty-project notice
  ---
  duration_ms: 0.207196
  ...
# Subtest: references tier walks with commitment rank and reference notice
ok 1649 - references tier walks with commitment rank and reference notice
  ---
  duration_ms: 0.451181
  ...
# Subtest: jump notices use reviewEntryView when provided and keep the fallback
ok 1650 - jump notices use reviewEntryView when provided and keep the fallback
  ---
  duration_ms: 0.285024
  ...
# Subtest: tier notices fall back without tier ranks and wrap on the last line
ok 1651 - tier notices fall back without tier ranks and wrap on the last line
  ---
  duration_ms: 0.150978
  ...
# Subtest: boundary notice names commitments done and rotten next
ok 1652 - boundary notice names commitments done and rotten next
  ---
  duration_ms: 0.126812
  ...
# Subtest: walk anchor records handled keys with their neighbors
ok 1653 - walk anchor records handled keys with their neighbors
  ---
  duration_ms: 0.495135
  ...
# Subtest: cursor on a live entry wins over a lagging anchor
ok 1654 - cursor on a live entry wins over a lagging anchor
  ---
  duration_ms: 0.314109
  ...
# Subtest: [s after a stamp goes backwards from the anchor
ok 1655 - [s after a stamp goes backwards from the anchor
  ---
  duration_ms: 1.512727
  ...
# Subtest: release-then-]s continues from the anchor successor
ok 1656 - release-then-]s continues from the anchor successor
  ---
  duration_ms: 0.279944
  ...
# Subtest: non-contiguous counted stamp advances past the last handled rank
ok 1657 - non-contiguous counted stamp advances past the last handled rank
  ---
  duration_ms: 0.332134
  ...
# Subtest: anchor wraps at both ends
ok 1658 - anchor wraps at both ends
  ---
  duration_ms: 0.332835
  ...
# Subtest: advance across NEXT to TICKLER to ROTTEN lands the boundary
ok 1659 - advance across NEXT to TICKLER to ROTTEN lands the boundary
  ---
  duration_ms: 0.384654
  ...
# Subtest: tier capability gates on the freshness namespace version
ok 1660 - tier capability gates on the freshness namespace version
  ---
  duration_ms: 0.121902
  ...
# Subtest: empty queue notice reads the upkeep meter
ok 1661 - empty queue notice reads the upkeep meter
  ---
  duration_ms: 0.101113
  ...
# Subtest: refresh row reads lane intervals from the api with the once-Ready return
ok 1662 - refresh row reads lane intervals from the api with the once-Ready return
  ---
  duration_ms: 1.427324
  ...
# Subtest: endpoint jumps select the queue ends with full rank and total
ok 1663 - endpoint jumps select the queue ends with full rank and total
  ---
  duration_ms: 0.399573
  ...
# Subtest: endpoint jumps ignore cursor, anchor, and direction
ok 1664 - endpoint jumps ignore cursor, anchor, and direction
  ---
  duration_ms: 0.318688
  ...
# Subtest: endpoint jumps on empty and one-entry queues
ok 1665 - endpoint jumps on empty and one-entry queues
  ---
  duration_ms: 0.276618
  ...
# Subtest: a visited endpoint is still due under its own anchor
ok 1666 - a visited endpoint is still due under its own anchor
  ---
  duration_ms: 0.206965
  ...
# Subtest: lowercase steps continue from an endpoint anchor
ok 1667 - lowercase steps continue from an endpoint anchor
  ---
  duration_ms: 0.361009
  ...
# Subtest: counted review jump repeat 1 matches omitted repeat
ok 1668 - counted review jump repeat 1 matches omitted repeat
  ---
  duration_ms: 0.725064
  ...
# Subtest: counted review jump from the first entry lands N steps ahead
ok 1669 - counted review jump from the first entry lands N steps ahead
  ---
  duration_ms: 0.300183
  ...
# Subtest: counted review jump from the last entry wraps past the start
ok 1670 - counted review jump from the last entry wraps past the start
  ---
  duration_ms: 0.158051
  ...
# Subtest: counted review jump larger than the queue wraps once
ok 1671 - counted review jump larger than the queue wraps once
  ---
  duration_ms: 0.212115
  ...
# Subtest: counted review jump on a one-entry queue stays there
ok 1672 - counted review jump on a one-entry queue stays there
  ---
  duration_ms: 0.17843
  ...
# Subtest: counted review jump with no origin lands on the Nth entry
ok 1673 - counted review jump with no origin lands on the Nth entry
  ---
  duration_ms: 0.19944
  ...
# Subtest: counted review jump from a shaped anchor takes N surviving successors
ok 1674 - counted review jump from a shaped anchor takes N surviving successors
  ---
  duration_ms: 0.237353
  ...
# Subtest: counted review jump does not change endpoint selection
ok 1675 - counted review jump does not change endpoint selection
  ---
  duration_ms: 0.184032
  ...
# Subtest: a stamped endpoint that moved is stale and cannot land from old text
ok 1676 - a stamped endpoint that moved is stale and cannot land from old text
  ---
  duration_ms: 0.224618
  ...
# Subtest: stale endpoint target reselects the same endpoint in the new queue
ok 1677 - stale endpoint target reselects the same endpoint in the new queue
  ---
  duration_ms: 1.998203
  ...
# Subtest: endpoint retry is bounded and failures preserve the anchor
ok 1678 - endpoint retry is bounded and failures preserve the anchor
  ---
  duration_ms: 0.632908
  ...
# Subtest: endpoint jump to ROTTEN carries no boundary preamble
ok 1679 - endpoint jump to ROTTEN carries no boundary preamble
  ---
  duration_ms: 0.865402
  ...
# Subtest: endpoint notices keep v4 tier details and legacy v3 text
ok 1680 - endpoint notices keep v4 tier details and legacy v3 text
  ---
  duration_ms: 0.164935
  ...
# Subtest: onload registers first/last commands routed to the shared jump
ok 1681 - onload registers first/last commands routed to the shared jump
  ---
  duration_ms: 1.99131
  ...
# Subtest: jumpToDueTask consumes a pending Vim prefix as N review steps
ok 1682 - jumpToDueTask consumes a pending Vim prefix as N review steps
  ---
  duration_ms: 1.051868
  ...
# Subtest: registered next-due-task callback reads the pending Vim prefix
ok 1683 - registered next-due-task callback reads the pending Vim prefix
  ---
  duration_ms: 0.942157
  ...
# Subtest: explicit jumpToDueTask repeat skips the Vim prefix
ok 1684 - explicit jumpToDueTask repeat skips the Vim prefix
  ---
  duration_ms: 2.204597
  ...
# Subtest: non-normal editor with a pending prefix still jumps one entry
ok 1685 - non-normal editor with a pending prefix still jumps one entry
  ---
  duration_ms: 0.426594
  ...
# Subtest: stale counted replan reuses the captured repeat
ok 1686 - stale counted replan reuses the captured repeat
  ---
  duration_ms: 0.422556
  ...
# Subtest: endpoint jump with a pending prefix still lands on the endpoint
ok 1687 - endpoint jump with a pending prefix still lands on the endpoint
  ---
  duration_ms: 0.341011
  ...
# Subtest: counted forward landing on ROTTEN keeps the boundary preamble
ok 1688 - counted forward landing on ROTTEN keeps the boundary preamble
  ---
  duration_ms: 0.643368
  ...
# Subtest: PRE and POST are machine tiers; PRE is a commitment
ok 1689 - PRE and POST are machine tiers; PRE is a commitment
  ---
  duration_ms: 0.284623
  ...
# Subtest: fallback notices name PRE checklist and POST closeout
ok 1690 - fallback notices name PRE checklist and POST closeout
  ---
  duration_ms: 0.316564
  ...
# Subtest: text-first cursor matching does not skip Pills after an above-insert
ok 1691 - text-first cursor matching does not skip Pills after an above-insert
  ---
  duration_ms: 0.196565
  ...
# Subtest: day-scoped anchors from another day are ignored
ok 1692 - day-scoped anchors from another day are ignored
  ---
  duration_ms: 0.293139
  ...
# Subtest: boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
ok 1693 - boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
  ---
  duration_ms: 0.271618
  ...
# Subtest: ]S reaches POST with 77 ROTTEN rows and a null budget
ok 1694 - ]S reaches POST with 77 ROTTEN rows and a null budget
  ---
  duration_ms: 0.802952
  ...
# Subtest: nav normalizes a legacy v7 returned tier to tickler
ok 1695 - nav normalizes a legacy v7 returned tier to tickler
  ---
  duration_ms: 0.148283
  ...
# Subtest: RECURRING is a machine tier, a commitment, and a v9 capability
ok 1696 - RECURRING is a machine tier, a commitment, and a v9 capability
  ---
  duration_ms: 0.177929
  ...
# Subtest: RECURRING counts in reviewWalkRemaining and gates the boundary
ok 1697 - RECURRING counts in reviewWalkRemaining and gates the boundary
  ---
  duration_ms: 0.201224
  ...
# Subtest: matchReviewRecurringCursor is text-first like the checklist matcher
ok 1698 - matchReviewRecurringCursor is text-first like the checklist matcher
  ---
  duration_ms: 0.243204
  ...
# Subtest: fallback notices name RECURRING due detail with the reschedule hint
ok 1699 - fallback notices name RECURRING due detail with the reschedule hint
  ---
  duration_ms: 0.188189
  ...
# Subtest: Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
ok 1700 - Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
  ---
  duration_ms: 0.166798
  ...
# Subtest: bobLineDigest matches the shared bob-cli vectors
ok 1701 - bobLineDigest matches the shared bob-cli vectors
  ---
  duration_ms: 5.768589
  ...
# Subtest: parseGoToTaskParams accepts a complete v1 link and ignores extra keys
ok 1702 - parseGoToTaskParams accepts a complete v1 link and ignores extra keys
  ---
  duration_ms: 1.022271
  ...
# Subtest: parseGoToTaskParams treats ref and block as optional
ok 1703 - parseGoToTaskParams treats ref and block as optional
  ---
  duration_ms: 0.181947
  ...
# Subtest: parseGoToTaskParams rejects each malformed field
ok 1704 - parseGoToTaskParams rejects each malformed field
  ---
  duration_ms: 0.310493
  ...
# Subtest: vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
ok 1705 - vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
  ---
  duration_ms: 0.378782
  ...
# Subtest: refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
ok 1706 - refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
  ---
  duration_ms: 1.889035
  ...
# Subtest: handleGoToTaskUri notices each malformed parameter
ok 1707 - handleGoToTaskUri notices each malformed parameter
  ---
  duration_ms: 1.663014
  ...
# Subtest: handleGoToTaskUri notices a path outside the vault
ok 1708 - handleGoToTaskUri notices a path outside the vault
  ---
  duration_ms: 0.580447
  ...
# Subtest: handleGoToTaskUri notices a missing file inside the vault
ok 1709 - handleGoToTaskUri notices a missing file inside the vault
  ---
  duration_ms: 0.711878
  ...
# Subtest: handleGoToTaskUri maps a trailing-slash vault base
ok 1710 - handleGoToTaskUri maps a trailing-slash vault base
  ---
  duration_ms: 2.45206
  ...
# Subtest: handleGoToTaskUri prefers the open buffer over cachedRead
ok 1711 - handleGoToTaskUri prefers the open buffer over cachedRead
  ---
  duration_ms: 1.011992
  ...
# Subtest: handleGoToTaskUri re-finds by block id after an insert above the task
ok 1712 - handleGoToTaskUri re-finds by block id after an insert above the task
  ---
  duration_ms: 0.637477
  ...
# Subtest: handleGoToTaskUri re-finds a unique digest after a shift with no block
ok 1713 - handleGoToTaskUri re-finds a unique digest after a shift with no block
  ---
  duration_ms: 0.73888
  ...
# Subtest: handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
ok 1714 - handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
  ---
  duration_ms: 0.527477
  ...
# Subtest: handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
ok 1715 - handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
  ---
  duration_ms: 0.606246
  ...
# Subtest: handleGoToTaskUri reuses a leaf that already shows the note
ok 1716 - handleGoToTaskUri reuses a leaf that already shows the note
  ---
  duration_ms: 0.789396
  ...
# Subtest: handleGoToTaskUri switches a Reading-view leaf to editing
ok 1717 - handleGoToTaskUri switches a Reading-view leaf to editing
  ---
  duration_ms: 0.771112
  ...
# Subtest: handleGoToTaskUri records a jump from the prior cursor and none without one
ok 1718 - handleGoToTaskUri records a jump from the prior cursor and none without one
  ---
  duration_ms: 1.217483
  ...
# Subtest: handleGoToTaskUri never writes the vault or advances the walk
ok 1719 - handleGoToTaskUri never writes the vault or advances the walk
  ---
  duration_ms: 0.538678
  ...
# Subtest: handleGoToTaskUri reports when the note cannot be opened
ok 1720 - handleGoToTaskUri reports when the note cannot be opened
  ---
  duration_ms: 0.407518
  ...
# Subtest: focusTaskMoveDestination still lands without switching Reading view
ok 1721 - focusTaskMoveDestination still lands without switching Reading view
  ---
  duration_ms: 0.490556
  ...
# Subtest: onload registers both read-only navigation protocols when available
ok 1722 - onload registers both read-only navigation protocols when available
  ---
  duration_ms: 1.449687
  ...
# Subtest: onload skips protocol registration when the API is missing
ok 1723 - onload skips protocol registration when the API is missing
  ---
  duration_ms: 0.396867
  ...
# Subtest: registered protocol handler forwards params to handleGoToTaskUri
ok 1724 - registered protocol handler forwards params to handleGoToTaskUri
  ---
  duration_ms: 0.410092
  ...
# Subtest: handleGoToTaskUri maps a path through realpath when prefixes differ
ok 1725 - handleGoToTaskUri maps a path through realpath when prefixes differ
  ---
  duration_ms: 2.220819
  ...
# Subtest: cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
ok 1726 - cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
  ---
  duration_ms: 2.244012
  ...
# Subtest: findCancelLogParent finds a direct child but ignores a grandchild
ok 1727 - findCancelLogParent finds a direct child but ignores a grandchild
  ---
  duration_ms: 0.649439
  ...
# Subtest: getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
ok 1728 - getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
  ---
  duration_ms: 0.207847
  ...
# Subtest: formatCancelLogEntryText renders the exact preview text
ok 1729 - formatCancelLogEntryText renders the exact preview text
  ---
  duration_ms: 0.172099
  ...
# Subtest: planCancelLogEntry inserts a first-child log with tabs or spaces
ok 1730 - planCancelLogEntry inserts a first-child log with tabs or spaces
  ---
  duration_ms: 0.773776
  ...
# Subtest: planCancelLogEntry prepends under an existing log wherever it sits
ok 1731 - planCancelLogEntry prepends under an existing log wherever it sits
  ---
  duration_ms: 0.283842
  ...
# Subtest: planCancelLogEntry uses the fallback only when a marker exists
ok 1732 - planCancelLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.358293
  ...
# Subtest: isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
ok 1733 - isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
  ---
  duration_ms: 0.368143
  ...
# Subtest: describeCancelTaskRow covers single, counted, link, recurring, and hidden
ok 1734 - describeCancelTaskRow covers single, counted, link, recurring, and hidden
  ---
  duration_ms: 2.397896
  ...
# Subtest: planTaskCancelBatch cancels a single task with a first-child log
ok 1735 - planTaskCancelBatch cancels a single task with a first-child log
  ---
  duration_ms: 1.888605
  ...
# Subtest: planTaskCancelBatch upserts cancelled before the block id and preserves fields
ok 1736 - planTaskCancelBatch upserts cancelled before the block id and preserves fields
  ---
  duration_ms: 0.555401
  ...
# Subtest: planTaskCancelBatch records id-field task identities
ok 1737 - planTaskCancelBatch records id-field task identities
  ---
  duration_ms: 0.320131
  ...
# Subtest: planTaskCancelBatch skips closed targets and stays bottom-up
ok 1738 - planTaskCancelBatch skips closed targets and stays bottom-up
  ---
  duration_ms: 0.47166
  ...
# Subtest: planTaskCancelBatch refuses recurring targets in all three syntaxes
ok 1739 - planTaskCancelBatch refuses recurring targets in all three syntaxes
  ---
  duration_ms: 0.549358
  ...
# Subtest: planTaskCancelBatch handles empty reasons and stale preimages
ok 1740 - planTaskCancelBatch handles empty reasons and stale preimages
  ---
  duration_ms: 0.384444
  ...
# Subtest: planTaskCancelBatch preserves CRLF line endings
ok 1741 - planTaskCancelBatch preserves CRLF line endings
  ---
  duration_ms: 0.264254
  ...
# Subtest: cancel project conversion carries the log and reports it
ok 1742 - cancel project conversion carries the log and reports it
  ---
  duration_ms: 3.712314
  ...
# Subtest: getCancelTaskRowTitle names single, counted, and link sessions
ok 1743 - getCancelTaskRowTitle names single, counted, and link sessions
  ---
  duration_ms: 1.024566
  ...
# Subtest: getCancelReasonHints labels Enter per state and Esc as Keep open
ok 1744 - getCancelReasonHints labels Enter per state and Esc as Keep open
  ---
  duration_ms: 1.013594
  ...
# Subtest: the Cancel property item and the card's cancel row describe an open task
ok 1745 - the Cancel property item and the card's cancel row describe an open task
  ---
  duration_ms: 11.882396
  ...
# Subtest: Cancel row hides on closed tasks, plain bullets, and all-closed sessions
ok 1746 - Cancel row hides on closed tasks, plain bullets, and all-closed sessions
  ---
  duration_ms: 5.461142
  ...
# Subtest: Cancel row reports skipped closed targets in a counted session
ok 1747 - Cancel row reports skipped closed targets in a counted session
  ---
  duration_ms: 1.360356
  ...
# Subtest: the card refuses the cancel row on a recurring task and stays on the card
ok 1748 - the card refuses the cancel row on a recurring task and stays on the card
  ---
  duration_ms: 1.887342
  ...
# Subtest: cancel reason stage previews the typed, empty, fallback, and :: cases
ok 1749 - cancel reason stage previews the typed, empty, fallback, and :: cases
  ---
  duration_ms: 2.596466
  ...
# Subtest: cancel reason footer flips between plain, log, and fallback labels
ok 1750 - cancel reason footer flips between plain, log, and fallback labels
  ---
  duration_ms: 0.928031
  ...
# Subtest: Esc from the cancel reason stage writes nothing
ok 1751 - Esc from the cancel reason stage writes nothing
  ---
  duration_ms: 3.62106
  ...
# Subtest: single cancel writes [-], stamp, and first-child log in one transaction
ok 1752 - single cancel writes [-], stamp, and first-child log in one transaction
  ---
  duration_ms: 9.36366
  ...
# Subtest: empty reason writes no log unless one already exists
ok 1753 - empty reason writes no log unless one already exists
  ---
  duration_ms: 5.859411
  ...
# Subtest: stale single preimage refuses with nothing written
ok 1754 - stale single preimage refuses with nothing written
  ---
  duration_ms: 1.427465
  ...
# Subtest: cancel writes [-] with no NOW chip
ok 1755 - cancel writes [-] with no NOW chip
  ---
  duration_ms: 1.835413
  ...
# Subtest: TSC recovery runs with cancelled identities; a missing API still succeeds
ok 1756 - TSC recovery runs with cancelled identities; a missing API still succeeds
  ---
  duration_ms: 5.080996
  ...
# Subtest: a throwing TSC API is skipped silently with no chip
ok 1757 - a throwing TSC API is skipped silently with no chip
  ---
  duration_ms: 1.993634
  ...
# Subtest: counted cancel skips closed targets and reports them
ok 1758 - counted cancel skips closed targets and reports them
  ---
  duration_ms: 2.535629
  ...
# Subtest: same-file cancel folds today's Pomodoro prune into one transaction
ok 1759 - same-file cancel folds today's Pomodoro prune into one transaction
  ---
  duration_ms: 4.252265
  ...
# Subtest: link session cancels the target and removes the invoking link bullet
ok 1760 - link session cancels the target and removes the invoking link bullet
  ---
  duration_ms: 6.373712
  ...
# Subtest: buildCancelNoticeModel text covers every chip
ok 1761 - buildCancelNoticeModel text covers every chip
  ---
  duration_ms: 0.299853
  ...
# Subtest: renderCancelNoticeFragment builds the is-cancel card
ok 1762 - renderCancelNoticeFragment builds the is-cancel card
  ---
  duration_ms: 0.670681
  ...
# Subtest: Ctrl+0 loads and focuses a deferred pinned dash tab without jumping or restoring
ok 1763 - Ctrl+0 loads and focuses a deferred pinned dash tab without jumping or restoring
  ---
  duration_ms: 3.092031
  ...
# Subtest: Ctrl+0 from an unpinned dash copy switches to the pinned home tab
ok 1764 - Ctrl+0 from an unpinned dash copy switches to the pinned home tab
  ---
  duration_ms: 0.532627
  ...
# Subtest: Ctrl+0 stays on the pinned dash tab when an unpinned copy exists
ok 1765 - Ctrl+0 stays on the pinned dash tab when an unpinned copy exists
  ---
  duration_ms: 0.297187
  ...
# Subtest: Ctrl+0 keeps the active dash tab when equal-ranked copies exist
ok 1766 - Ctrl+0 keeps the active dash tab when equal-ranked copies exist
  ---
  duration_ms: 0.322586
  ...
# Subtest: a pinned dash tab wins over an earlier unpinned tab
ok 1767 - a pinned dash tab wins over an earlier unpinned tab
  ---
  duration_ms: 0.385305
  ...
# Subtest: a main-area dash tab wins over a pinned sidebar tab
ok 1768 - a main-area dash tab wins over a pinned sidebar tab
  ---
  duration_ms: 0.2782
  ...
# Subtest: a deferred sidebar dash tab is reused when there is no main-area match
ok 1769 - a deferred sidebar dash tab is reused when there is no main-area match
  ---
  duration_ms: 0.344227
  ...
# Subtest: a markdown saved state is considered even when the leaf is not deferred
ok 1770 - a markdown saved state is considered even when the leaf is not deferred
  ---
  duration_ms: 0.251861
  ...
# Subtest: Ctrl+0 opens dash in the current tab when no matching tab exists
ok 1771 - Ctrl+0 opens dash in the current tab when no matching tab exists
  ---
  duration_ms: 0.667523
  ...
# Subtest: Ctrl+0 leaves an already active dash tab alone
ok 1772 - Ctrl+0 leaves an already active dash tab alone
  ---
  duration_ms: 0.621787
  ...
# Subtest: isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
ok 1773 - isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
  ---
  duration_ms: 1.345498
  ...
# Subtest: findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
ok 1774 - findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
  ---
  duration_ms: 1.287918
  ...
# Subtest: collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
ok 1775 - collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
  ---
  duration_ms: 0.501547
  ...
# Subtest: planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
ok 1776 - planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
  ---
  duration_ms: 1.026489
  ...
# Subtest: planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
ok 1777 - planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
  ---
  duration_ms: 0.831196
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
ok 1778 - planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
  ---
  duration_ms: 0.862696
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
ok 1779 - planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
  ---
  duration_ms: 0.545561
  ...
# Subtest: planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
ok 1780 - planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
  ---
  duration_ms: 0.215431
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
ok 1781 - planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
  ---
  duration_ms: 0.826607
  ...
# Subtest: planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
ok 1782 - planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
  ---
  duration_ms: 0.767294
  ...
# Subtest: planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
ok 1783 - planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
  ---
  duration_ms: 0.654579
  ...
# Subtest: planDeferredPomodoroLinkCleanup preserves CRLF line endings
ok 1784 - planDeferredPomodoroLinkCleanup preserves CRLF line endings
  ---
  duration_ms: 0.271448
  ...
# Subtest: deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
ok 1785 - deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
  ---
  duration_ms: 0.287589
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks\#^x]] \#
ok 1786 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks\#^x]] \#
  ---
  duration_ms: 0.571851
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks\#^x|alias]] \#
ok 1787 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks\#^x|alias]] \#
  ---
  duration_ms: 0.17257
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks\#^x]]
ok 1788 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks\#^x]]
  ---
  duration_ms: 0.196996
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks\#^x]]
ok 1789 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks\#^x]]
  ---
  duration_ms: 0.160426
  ...
# Subtest: dedicated decoration check accepts paired strikes but cleanup never removes struck links
ok 1790 - dedicated decoration check accepts paired strikes but cleanup never removes struck links
  ---
  duration_ms: 0.302758
  ...
# Subtest: cleanup deletes only touched childless entries, preserving prose, placeholders and closed history
ok 1791 - cleanup deletes only touched childless entries, preserving prose, placeholders and closed history
  ---
  duration_ms: 0.389193
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\n", final newline false)
ok 1792 - cleanup handles adjacent EOF entries ("\\n", final newline false)
  ---
  duration_ms: 0.225911
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\n", final newline true)
ok 1793 - cleanup handles adjacent EOF entries ("\\n", final newline true)
  ---
  duration_ms: 0.185995
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\r\\n", final newline false)
ok 1794 - cleanup handles adjacent EOF entries ("\\r\\n", final newline false)
  ---
  duration_ms: 0.154364
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\r\\n", final newline true)
ok 1795 - cleanup handles adjacent EOF entries ("\\r\\n", final newline true)
  ---
  duration_ms: 0.150216
  ...
# Subtest: counted dependencies converge mixed sources and maintain one link per parent
ok 1796 - counted dependencies converge mixed sources and maintain one link per parent
  ---
  duration_ms: 10.906605
  ...
# Subtest: counted and single dependency gestures refuse inside a blockquote (DP29)
ok 1797 - counted and single dependency gestures refuse inside a blockquote (DP29)
  ---
  duration_ms: 0.388802
  ...
# Subtest: counted dependency candidates exclude every source and expose mixed state
ok 1798 - counted dependency candidates exclude every source and expose mixed state
  ---
  duration_ms: 0.83838
  ...
# Subtest: counted dependency block-ID prompting is planned atomically
ok 1799 - counted dependency block-ID prompting is planned atomically
  ---
  duration_ms: 1.922919
  ...
# Subtest: counted dependency runtime applies target, parents, and navigation in one undo group
ok 1800 - counted dependency runtime applies target, parents, and navigation in one undo group
  ---
  duration_ms: 6.553097
  ...
# Subtest: counted Depends-on removal recovers residents with [unblocked::]
ok 1801 - counted Depends-on removal recovers residents with [unblocked::]
  ---
  duration_ms: 4.451195
  ...
# Subtest: counted Depends-on removal writes [unblocked::] through the wired freshness API
ok 1802 - counted Depends-on removal writes [unblocked::] through the wired freshness API
  ---
  duration_ms: 5.643811
  ...
# Subtest: cross-file toggle changes only the source link
ok 1803 - cross-file toggle changes only the source link
  ---
  duration_ms: 1.825144
  ...
# Subtest: cross-file write failure still toggles only the source link
ok 1804 - cross-file write failure still toggles only the source link
  ---
  duration_ms: 0.654108
  ...
# Subtest: line-local fallback applies bottom-up and preserves CRLF
ok 1805 - line-local fallback applies bottom-up and preserves CRLF
  ---
  duration_ms: 0.814073
  ...
# Subtest: source line-count invariant rejects embedded newline changes
ok 1806 - source line-count invariant rejects embedded newline changes
  ---
  duration_ms: 0.217616
  ...
# Subtest: pure toggle refuses when the source changed under it
ok 1807 - pure toggle refuses when the source changed under it
  ---
  duration_ms: 0.161048
  ...
# Subtest: counted transclusion toggle evaluates each line independently
ok 1808 - counted transclusion toggle evaluates each line independently
  ---
  duration_ms: 0.369265
  ...
# Subtest: transclusion toggle is refused on Depends-On lines
ok 1809 - transclusion toggle is refused on Depends-On lines
  ---
  duration_ms: 0.311574
  ...
# Subtest: legacy sole-link children toggle purely, without field or status writes
ok 1810 - legacy sole-link children toggle purely, without field or status writes
  ---
  duration_ms: 0.413048
  ...
# Subtest: Ctrl+D on the Depends on row clears the line, field, and legacy children
ok 1811 - Ctrl+D on the Depends on row clears the line, field, and legacy children
  ---
  duration_ms: 3.603186
  ...
# Subtest: Ctrl+D clears a field-only dependency without a line
ok 1812 - Ctrl+D clears a field-only dependency without a line
  ---
  duration_ms: 1.235167
  ...
# Subtest: counted Ctrl+D on the Depends on row clears every targeted task
ok 1813 - counted Ctrl+D on the Depends on row clears every targeted task
  ---
  duration_ms: 2.537965
  ...
# Subtest: findRemovedLineText reports deleted lines
ok 1814 - findRemovedLineText reports deleted lines
  ---
  duration_ms: 0.158803
  ...
# Subtest: hand-edit mirror projects an edited line into the field
ok 1815 - hand-edit mirror projects an edited line into the field
  ---
  duration_ms: 1.720323
  ...
# Subtest: hand-edit mirror canonicalises a hand-written line variant
ok 1816 - hand-edit mirror canonicalises a hand-written line variant
  ---
  duration_ms: 0.857416
  ...
# Subtest: hand-edit mirror drops a linkless line and the field
ok 1817 - hand-edit mirror drops a linkless line and the field
  ---
  duration_ms: 0.9906
  ...
# Subtest: hand-edit mirror clears the field after the line is deleted
ok 1818 - hand-edit mirror clears the field after the line is deleted
  ---
  duration_ms: 0.963779
  ...
# Subtest: hand-edit mirror leaves malformed lines alone
ok 1819 - hand-edit mirror leaves malformed lines alone
  ---
  duration_ms: 0.275966
  ...
# Subtest: hand-edit mirror leaves legacy-only children for the hooks
ok 1820 - hand-edit mirror leaves legacy-only children for the hooks
  ---
  duration_ms: 0.399192
  ...
# Subtest: hand-edit mirror blocks when an open prerequisite is added by hand
ok 1821 - hand-edit mirror blocks when an open prerequisite is added by hand
  ---
  duration_ms: 0.774959
  ...
# Subtest: hand-edit mirror never transfers commitment to the target
ok 1822 - hand-edit mirror never transfers commitment to the target
  ---
  duration_ms: 0.971274
  ...
# Subtest: hand-edit mirror recovers when the last open prerequisite is removed by hand
ok 1823 - hand-edit mirror recovers when the last open prerequisite is removed by hand
  ---
  duration_ms: 1.164021
  ...
# Subtest: hand-edit mirror leaves a half-typed link alone
ok 1824 - hand-edit mirror leaves a half-typed link alone
  ---
  duration_ms: 0.330651
  ...
# Subtest: hand-edit mirror clears the owning task when its last-child line is deleted
ok 1825 - hand-edit mirror clears the owning task when its last-child line is deleted
  ---
  duration_ms: 0.920446
  ...
# Subtest: mirror scheduler debounces at the contract interval
ok 1826 - mirror scheduler debounces at the contract interval
  ---
  duration_ms: 1.007623
  ...
# Subtest: mirror scheduler seeds the baseline from the update start state
ok 1827 - mirror scheduler seeds the baseline from the update start state
  ---
  duration_ms: 1.940453
  ...
# Subtest: mirror scheduler keeps the first baseline and maps the owner across a burst
ok 1828 - mirror scheduler keeps the first baseline and maps the owner across a burst
  ---
  duration_ms: 0.639671
  ...
# Subtest: mirror listener runs clear-field for a first-edit deletion with a following sibling
ok 1829 - mirror listener runs clear-field for a first-edit deletion with a following sibling
  ---
  duration_ms: 14.798832
  ...
# Subtest: mirror fire re-arms while the cursor stays on the edited line
ok 1830 - mirror fire re-arms while the cursor stays on the edited line
  ---
  duration_ms: 2.971461
  ...
# Subtest: mirror scheduler reads changed ranges from the CM6 update
ok 1831 - mirror scheduler reads changed ranges from the CM6 update
  ---
  duration_ms: 0.346561
  ...
# Subtest: mirror scheduler skips IME composition
ok 1832 - mirror scheduler skips IME composition
  ---
  duration_ms: 0.217726
  ...
# Subtest: mirror scheduler skips open modals
ok 1833 - mirror scheduler skips open modals
  ---
  duration_ms: 0.227534
  ...
# Subtest: counted Ctrl+D clears every targeted task in one transaction with one notice
ok 1834 - counted Ctrl+D clears every targeted task in one transaction with one notice
  ---
  duration_ms: 4.900181
  ...
# Subtest: counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
ok 1835 - counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
  ---
  duration_ms: 1.614561
  ...
# Subtest: counted N! on only a Depends-On line refuses without writing
ok 1836 - counted N! on only a Depends-On line refuses without writing
  ---
  duration_ms: 0.267892
  ...
# Subtest: promotion targets enumerate real tasks and assign stable IDs
ok 1837 - promotion targets enumerate real tasks and assign stable IDs
  ---
  duration_ms: 4.664593
  ...
# Subtest: promotion file planner expands live links and preserves history
ok 1838 - promotion file planner expands live links and preserves history
  ---
  duration_ms: 5.435202
  ...
# Subtest: promotion file planner handles forms, whitespace, and subtrees
ok 1839 - promotion file planner handles forms, whitespace, and subtrees
  ---
  duration_ms: 1.335199
  ...
# Subtest: promotion file planner keeps compatibility for non-live references
ok 1840 - promotion file planner keeps compatibility for non-live references
  ---
  duration_ms: 0.920547
  ...
# Subtest: forward promotion expands live links, persists anchors, and removes the source
ok 1841 - forward promotion expands live links, persists anchors, and removes the source
  ---
  duration_ms: 10.021605
  ...
# Subtest: forward promotion uses zero-task fallback and keeps reverse one-to-one
ok 1842 - forward promotion uses zero-task fallback and keeps reverse one-to-one
  ---
  duration_ms: 1.2418
  ...
# Subtest: forward promotion retains the source on ambiguous, stale, and write failures
ok 1843 - forward promotion retains the source on ambiguous, stale, and write failures
  ---
  duration_ms: 1.431472
  ...
# Subtest: forward promotion discovers live links without a backlink cache and uses one open-editor write
ok 1844 - forward promotion discovers live links without a backlink cache and uses one open-editor write
  ---
  duration_ms: 2.424586
  ...
# Subtest: forward conversion carries a Depends-On line and reverse restores it
ok 1845 - forward conversion carries a Depends-On line and reverse restores it
  ---
  duration_ms: 30.783207
  ...
# Subtest: reverse conversion re-keys a cross-note prerequisite BLOCKS link
ok 1846 - reverse conversion re-keys a cross-note prerequisite BLOCKS link
  ---
  duration_ms: 9.302814
  ...
# Subtest: planTaskLaneBatch commits every Ready target to Next
ok 1847 - planTaskLaneBatch commits every Ready target to Next
  ---
  duration_ms: 2.603428
  ...
# Subtest: planTaskLaneBatch releases Next and In Progress to Ready
ok 1848 - planTaskLaneBatch releases Next and In Progress to Ready
  ---
  duration_ms: 0.441423
  ...
# Subtest: planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
ok 1849 - planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
  ---
  duration_ms: 0.794135
  ...
# Subtest: planTaskLaneBatch skips Blocked and refuses stale preimages
ok 1850 - planTaskLaneBatch skips Blocked and refuses stale preimages
  ---
  duration_ms: 0.288421
  ...
# Subtest: buildLaneToggleNotice reports commit and release with and without budgets
ok 1851 - buildLaneToggleNotice reports commit and release with and without budgets
  ---
  duration_ms: 0.353725
  ...
# Subtest: describeLaneRow covers task, counted, and link sessions
ok 1852 - describeLaneRow covers task, counted, and link sessions
  ---
  duration_ms: 0.404913
  ...
# Subtest: toggleTaskLane commits Ready to Next and reports lane budgets
ok 1853 - toggleTaskLane commits Ready to Next and reports lane budgets
  ---
  duration_ms: 2.434857
  ...
# Subtest: toggleTaskLane releases to Ready without the api
ok 1854 - toggleTaskLane releases to Ready without the api
  ---
  duration_ms: 0.947278
  ...
# Subtest: toggleTaskLane release logs the summary on In Progress tasks
ok 1855 - toggleTaskLane release logs the summary on In Progress tasks
  ---
  duration_ms: 1.068099
  ...
# Subtest: toggleTaskLane skips Blocked targets
ok 1856 - toggleTaskLane skips Blocked targets
  ---
  duration_ms: 0.865712
  ...
# Subtest: counted toggleTaskLane covers the current task plus the next N tasks
ok 1857 - counted toggleTaskLane covers the current task plus the next N tasks
  ---
  duration_ms: 0.600145
  ...
# Subtest: toggleTaskLane on a Task Link writes through the open buffer
ok 1858 - toggleTaskLane on a Task Link writes through the open buffer
  ---
  duration_ms: 3.041695
  ...
# Subtest: toggleTaskLane on Task Links releases across notes
ok 1859 - toggleTaskLane on Task Links releases across notes
  ---
  duration_ms: 1.018163
  ...
# Subtest: toggleTaskLane refuses when a preimage changed
ok 1860 - toggleTaskLane refuses when a preimage changed
  ---
  duration_ms: 0.174033
  ...
# Subtest: Ctrl+Shift+P shows a pinned lane row that commits immediately
ok 1861 - Ctrl+Shift+P shows a pinned lane row that commits immediately
  ---
  duration_ms: 11.496029
  ...
# Subtest: Ctrl+Shift+P link mode shows the lane row with release detail
ok 1862 - Ctrl+Shift+P link mode shows the lane row with release detail
  ---
  duration_ms: 4.112149
  ...
# Subtest: Ctrl+Shift+P lane release with In Progress goes through the reason stage
ok 1863 - Ctrl+Shift+P lane release with In Progress goes through the reason stage
  ---
  duration_ms: 4.411919
  ...
# Subtest: getLinkPickerSessionSubtitle keeps the clamp for a single link
ok 1864 - getLinkPickerSessionSubtitle keeps the clamp for a single link
  ---
  duration_ms: 0.207616
  ...
# Subtest: link-mode priority notice keeps via Task Links visible
ok 1865 - link-mode priority notice keeps via Task Links visible
  ---
  duration_ms: 0.906449
  ...
# Subtest: already-handled Alt+N leaves Vim state alone
ok 1866 - already-handled Alt+N leaves Vim state alone
  ---
  duration_ms: 0.413859
  ...
# Subtest: Alt+N fallback still dispatches once with the Vim count
ok 1867 - Alt+N fallback still dispatches once with the Vim count
  ---
  duration_ms: 0.962016
  ...
# Subtest: lane release deletes an emptied entry (cross-file, Alt+N)
ok 1868 - lane release deletes an emptied entry (cross-file, Alt+N)
  ---
  duration_ms: 3.160352
  ...
# Subtest: lane release deletes an emptied entry (cross-file, card)
ok 1869 - lane release deletes an emptied entry (cross-file, card)
  ---
  duration_ms: 3.126216
  ...
# Subtest: lane release deletes an emptied entry (same-file, Alt+N)
ok 1870 - lane release deletes an emptied entry (same-file, Alt+N)
  ---
  duration_ms: 0.904566
  ...
# Subtest: lane release deletes an emptied entry (same-file, card)
ok 1871 - lane release deletes an emptied entry (same-file, card)
  ---
  duration_ms: 2.817767
  ...
# Subtest: Task Link release deletes its entry in one undo group (separate, Alt+N)
ok 1872 - Task Link release deletes its entry in one undo group (separate, Alt+N)
  ---
  duration_ms: 1.58251
  ...
# Subtest: Task Link release deletes its entry in one undo group (separate, card)
ok 1873 - Task Link release deletes its entry in one undo group (separate, card)
  ---
  duration_ms: 3.209736
  ...
# Subtest: Task Link release deletes its entry in one undo group (folded, Alt+N)
ok 1874 - Task Link release deletes its entry in one undo group (folded, Alt+N)
  ---
  duration_ms: 1.062017
  ...
# Subtest: Task Link release deletes its entry in one undo group (folded, card)
ok 1875 - Task Link release deletes its entry in one undo group (folded, card)
  ---
  duration_ms: 3.09188
  ...
# Subtest: parseLinkPickerTaskLink recognizes dedicated Task Link bullets
ok 1876 - parseLinkPickerTaskLink recognizes dedicated Task Link bullets
  ---
  duration_ms: 2.626012
  ...
# Subtest: discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
ok 1877 - discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
  ---
  duration_ms: 1.354996
  ...
# Subtest: discoverLinkPickerTargets leaves \#task lines to the regular picker
ok 1878 - discoverLinkPickerTargets leaves \#task lines to the regular picker
  ---
  duration_ms: 0.355578
  ...
# Subtest: findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
ok 1879 - findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
  ---
  duration_ms: 0.689205
  ...
# Subtest: createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
ok 1880 - createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
  ---
  duration_ms: 2.361316
  ...
# Subtest: getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
ok 1881 - getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
  ---
  duration_ms: 0.934934
  ...
# Subtest: bare link mode edits the task behind a Task Link through the open buffer
ok 1882 - bare link mode edits the task behind a Task Link through the open buffer
  ---
  duration_ms: 21.204016
  ...
# Subtest: counted link mode writes across notes through both the open buffer and the vault
ok 1883 - counted link mode writes across notes through both the open buffer and the vault
  ---
  duration_ms: 4.72085
  ...
# Subtest: Task Link scheduled delete recovers a Blocked task through the wired freshness API
ok 1884 - Task Link scheduled delete recovers a Blocked task through the wired freshness API
  ---
  duration_ms: 7.243883
  ...
# Subtest: link mode refuses the whole operation when a linked note changed
ok 1885 - link mode refuses the whole operation when a linked note changed
  ---
  duration_ms: 3.097561
  ...
# Subtest: link mode reports a closed target and changes nothing
ok 1886 - link mode reports a closed target and changes nothing
  ---
  duration_ms: 1.073168
  ...
# Subtest: link mode defers to a future date, blocks the task, and prunes today
ok 1887 - link mode defers to a future date, blocks the task, and prunes today
  ---
  duration_ms: 8.290612
  ...
# Subtest: bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
ok 1888 - bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
  ---
  duration_ms: 3.078726
  ...
# Subtest: Task Link scheduled write deletes its entry (separate)
ok 1889 - Task Link scheduled write deletes its entry (separate)
  ---
  duration_ms: 5.325975
  ...
# Subtest: Task Link scheduled write deletes its entry (folded)
ok 1890 - Task Link scheduled write deletes its entry (folded)
  ---
  duration_ms: 3.417101
  ...
# Subtest: folded Task Link scheduling maps the cursor past logs inserted before the emptied entry
ok 1891 - folded Task Link scheduling maps the cursor past logs inserted before the emptied entry
  ---
  duration_ms: 3.372677
  ...
# Subtest: dash restore suppresses editor notice after deliberate navigation
ok 1892 - dash restore suppresses editor notice after deliberate navigation
  ---
  duration_ms: 22.718406
  ...
# Subtest: open-task dispatch timeout is registered for plugin cleanup
ok 1893 - open-task dispatch timeout is registered for plugin cleanup
  ---
  duration_ms: 0.639881
  ...
# Subtest: jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
ok 1894 - jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
  ---
  duration_ms: 6.259665
  ...
# Subtest: jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
ok 1895 - jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
  ---
  duration_ms: 1.534749
  ...
# Subtest: jumpToOpenObsidianTask keeps current-swap transaction failures local
ok 1896 - jumpToOpenObsidianTask keeps current-swap transaction failures local
  ---
  duration_ms: 0.876683
  ...
# Subtest: jumpToOpenObsidianTask refuses current-up without jumping or mutating
ok 1897 - jumpToOpenObsidianTask refuses current-up without jumping or mutating
  ---
  duration_ms: 0.566972
  ...
# Subtest: jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
ok 1898 - jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
  ---
  duration_ms: 2.380973
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
ok 1899 - Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
  ---
  duration_ms: 0.876332
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
ok 1900 - Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
  ---
  duration_ms: 0.966645
  ...
# Subtest: counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
ok 1901 - counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
  ---
  duration_ms: 1.473822
  ...
# Subtest: an impossible counted Pomodoro move refuses without jumping or mutating
ok 1902 - an impossible counted Pomodoro move refuses without jumping or mutating
  ---
  duration_ms: 0.630353
  ...
# Subtest: counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
ok 1903 - counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
  ---
  duration_ms: 0.85457
  ...
# Subtest: counted open-task jump on a sole current target keeps the existing notice
ok 1904 - counted open-task jump on a sole current target keeps the existing notice
  ---
  duration_ms: 0.275796
  ...
# Subtest: dispatch guard allows exactly one counted Pomodoro move when the command route also fires
ok 1905 - dispatch guard allows exactly one counted Pomodoro move when the command route also fires
  ---
  duration_ms: 0.97438
  ...
# Subtest: bullet property picker reconciles duplicate bare and counted opens
ok 1906 - bullet property picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 16.257376
  ...
# Subtest: bullet property picker close lifecycle clears tracking for fresh sessions
ok 1907 - bullet property picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 8.657231
  ...
# Subtest: task move picker reconciles duplicate bare and counted opens
ok 1908 - task move picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 3.05444
  ...
# Subtest: task move picker close lifecycle clears tracking for fresh sessions
ok 1909 - task move picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 3.544644
  ...
# Subtest: Pomodoro bullet move picker opens sessions and clears the shared move picker slot
ok 1910 - Pomodoro bullet move picker opens sessions and clears the shared move picker slot
  ---
  duration_ms: 3.395759
  ...
# Subtest: Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
ok 1911 - Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
  ---
  duration_ms: 0.957507
  ...
# Subtest: move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
ok 1912 - move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
  ---
  duration_ms: 1.436512
  ...
# Subtest: commitPomodoroBulletMoveSession applies one guarded same-file transaction
ok 1913 - commitPomodoroBulletMoveSession applies one guarded same-file transaction
  ---
  duration_ms: 2.273459
  ...
# Subtest: Pomodoro bullet move picker confirms = through the actual picker callback
ok 1914 - Pomodoro bullet move picker confirms = through the actual picker callback
  ---
  duration_ms: 1.081795
  ...
# Subtest: Pomodoro bullet move picker reserves =NAME for peeling a named merged component
ok 1915 - Pomodoro bullet move picker reserves =NAME for peeling a named merged component
  ---
  duration_ms: 1.172628
  ...
# Subtest: Pomodoro bullet move picker confirms =email through the actual picker callback
ok 1916 - Pomodoro bullet move picker confirms =email through the actual picker callback
  ---
  duration_ms: 1.384702
  ...
# Subtest: Pomodoro bullet move picker confirms = review through the actual picker callback
ok 1917 - Pomodoro bullet move picker confirms = review through the actual picker callback
  ---
  duration_ms: 0.695247
  ...
# Subtest: Pomodoro bullet move picker confirms =focus by unnaming a single-name source
ok 1918 - Pomodoro bullet move picker confirms =focus by unnaming a single-name source
  ---
  duration_ms: 0.721887
  ...
# Subtest: Pomodoro bullet split stale-content guard does not write
ok 1919 - Pomodoro bullet split stale-content guard does not write
  ---
  duration_ms: 0.33007
  ...
# Subtest: Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
ok 1920 - Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
  ---
  duration_ms: 0.632126
  ...
# Subtest: native isOpen regression: pickers attach, close clears slot, reopen works
ok 1921 - native isOpen regression: pickers attach, close clears slot, reopen works
  ---
  duration_ms: 5.598986
  ...
# Subtest: stale registered pickers fail open on the next key
ok 1922 - stale registered pickers fail open on the next key
  ---
  duration_ms: 2.935933
  ...
# Subtest: planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
ok 1923 - planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
  ---
  duration_ms: 6.705779
  ...
# Subtest: planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
ok 1924 - planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
  ---
  duration_ms: 0.863849
  ...
# Subtest: planPomodoroBulletMove preserves the source when only some siblings move out
ok 1925 - planPomodoroBulletMove preserves the source when only some siblings move out
  ---
  duration_ms: 0.376118
  ...
# Subtest: planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
ok 1926 - planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
  ---
  duration_ms: 0.478543
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
ok 1927 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
  ---
  duration_ms: 0.872134
  ...
# Subtest: planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
ok 1928 - planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
  ---
  duration_ms: 1.201422
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
ok 1929 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
  ---
  duration_ms: 0.531024
  ...
# Subtest: planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
ok 1930 - planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
  ---
  duration_ms: 0.392539
  ...
# Subtest: planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
ok 1931 - planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
  ---
  duration_ms: 0.64957
  ...
# Subtest: planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
ok 1932 - planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
  ---
  duration_ms: 1.164672
  ...
# Subtest: planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
ok 1933 - planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
  ---
  duration_ms: 0.390536
  ...
# Subtest: planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
ok 1934 - planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
  ---
  duration_ms: 0.245659
  ...
# Subtest: planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
ok 1935 - planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
  ---
  duration_ms: 0.501447
  ...
# Subtest: planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
ok 1936 - planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
  ---
  duration_ms: 0.509633
  ...
# Subtest: planPomodoroBulletMove deletes both open and closed source entries the same way
ok 1937 - planPomodoroBulletMove deletes both open and closed source entries the same way
  ---
  duration_ms: 0.541774
  ...
# Subtest: planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
ok 1938 - planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
  ---
  duration_ms: 0.426073
  ...
# Subtest: planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
ok 1939 - planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
  ---
  duration_ms: 0.558567
  ...
# Subtest: planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
ok 1940 - planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
  ---
  duration_ms: 0.707901
  ...
# Subtest: planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
ok 1941 - planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
  ---
  duration_ms: 0.421855
  ...
# Subtest: planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
ok 1942 - planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
  ---
  duration_ms: 0.640853
  ...
# Subtest: planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
ok 1943 - planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
  ---
  duration_ms: 3.682858
  ...
# Subtest: planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
ok 1944 - planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
  ---
  duration_ms: 0.630212
  ...
# Subtest: planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
ok 1945 - planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
  ---
  duration_ms: 0.353084
  ...
# Subtest: planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
ok 1946 - planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
  ---
  duration_ms: 0.614563
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
ok 1947 - planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
  ---
  duration_ms: 0.32518
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
ok 1948 - planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
  ---
  duration_ms: 0.779938
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
ok 1949 - planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
  ---
  duration_ms: 3.732093
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
ok 1950 - planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
  ---
  duration_ms: 0.849361
  ...
# Subtest: Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
ok 1951 - Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
  ---
  duration_ms: 8.526321
  ...
# Subtest: commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
ok 1952 - commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
  ---
  duration_ms: 4.671846
  ...
# Subtest: commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
ok 1953 - commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
  ---
  duration_ms: 1.437403
  ...
# Subtest: commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
ok 1954 - commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
  ---
  duration_ms: 0.683605
  ...
# Subtest: commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
ok 1955 - commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
  ---
  duration_ms: 0.566021
  ...
# Subtest: Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
ok 1956 - Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
  ---
  duration_ms: 12.195344
  ...
# Subtest: Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
ok 1957 - Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
  ---
  duration_ms: 1.227352
  ...
# Subtest: Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
ok 1958 - Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
  ---
  duration_ms: 1.204529
  ...
# Subtest: Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
ok 1959 - Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
  ---
  duration_ms: 1.397858
  ...
# Subtest: task move picker closes before commit while other pickers retain delayed close
ok 1960 - task move picker closes before commit while other pickers retain delayed close
  ---
  duration_ms: 1.158091
  ...
# Subtest: parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
ok 1961 - parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
  ---
  duration_ms: 2.02839
  ...
# Subtest: normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
ok 1962 - normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
  ---
  duration_ms: 0.383241
  ...
# Subtest: formatPomodoroEntryLine emits a placeholder entry with or without a name
ok 1963 - formatPomodoroEntryLine emits a placeholder entry with or without a name
  ---
  duration_ms: 0.136801
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
ok 1964 - createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
  ---
  duration_ms: 2.09558
  ...
# Subtest: createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
ok 1965 - createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
  ---
  duration_ms: 0.798754
  ...
# Subtest: createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
ok 1966 - createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
  ---
  duration_ms: 0.658847
  ...
# Subtest: createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
ok 1967 - createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
  ---
  duration_ms: 0.656243
  ...
# Subtest: buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
ok 1968 - buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
  ---
  duration_ms: 0.226873
  ...
# Subtest: buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
ok 1969 - buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
  ---
  duration_ms: 0.375397
  ...
# Subtest: createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
ok 1970 - createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
  ---
  duration_ms: 0.609924
  ...
# Subtest: createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
ok 1971 - createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
  ---
  duration_ms: 0.333727
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
ok 1972 - createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
  ---
  duration_ms: 0.320532
  ...
# Subtest: collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
ok 1973 - collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
  ---
  duration_ms: 0.414702
  ...
# Subtest: findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
ok 1974 - findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
  ---
  duration_ms: 0.479375
  ...
# Subtest: findPomodoroBulletContext leaves plain \#task lines on the task-move route
ok 1975 - findPomodoroBulletContext leaves plain \#task lines on the task-move route
  ---
  duration_ms: 0.305814
  ...
# Subtest: discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
ok 1976 - discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
  ---
  duration_ms: 0.851585
  ...
# Subtest: findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
ok 1977 - findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
  ---
  duration_ms: 0.745823
  ...
# Subtest: discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
ok 1978 - discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
  ---
  duration_ms: 0.883396
  ...
# Subtest: isMovablePomodoroEntryContext matches open current and future Pomodoro entries
ok 1979 - isMovablePomodoroEntryContext matches open current and future Pomodoro entries
  ---
  duration_ms: 3.087483
  ...
# Subtest: planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
ok 1980 - planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
  ---
  duration_ms: 0.810296
  ...
# Subtest: planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
ok 1981 - planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
  ---
  duration_ms: 0.316343
  ...
# Subtest: planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
ok 1982 - planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
  ---
  duration_ms: 0.400253
  ...
# Subtest: planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
ok 1983 - planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
  ---
  duration_ms: 0.519913
  ...
# Subtest: planPomodoroEntryReorder handles counted current swaps and their inverses
ok 1984 - planPomodoroEntryReorder handles counted current swaps and their inverses
  ---
  duration_ms: 0.516405
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
ok 1985 - planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
  ---
  duration_ms: 0.250187
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
ok 1986 - planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
  ---
  duration_ms: 0.220811
  ...
# Subtest: planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
ok 1987 - planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
  ---
  duration_ms: 0.506607
  ...
# Subtest: planPomodoroEntryReorder round-trips a future-up swap across the current open entry
ok 1988 - planPomodoroEntryReorder round-trips a future-up swap across the current open entry
  ---
  duration_ms: 0.584535
  ...
# Subtest: planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
ok 1989 - planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
  ---
  duration_ms: 0.508952
  ...
# Subtest: planPomodoroEntryReorder refuses moving down past the last placeholder in the section
ok 1990 - planPomodoroEntryReorder refuses moving down past the last placeholder in the section
  ---
  duration_ms: 0.206213
  ...
# Subtest: planPomodoroEntryReorder refuses both directions for a lone placeholder
ok 1991 - planPomodoroEntryReorder refuses both directions for a lone placeholder
  ---
  duration_ms: 0.163823
  ...
# Subtest: planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
ok 1992 - planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
  ---
  duration_ms: 0.15179
  ...
# Subtest: planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
ok 1993 - planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
  ---
  duration_ms: 0.243585
  ...
# Subtest: planPomodoroEntryReorder refuses illegal current/future spans atomically
ok 1994 - planPomodoroEntryReorder refuses illegal current/future spans atomically
  ---
  duration_ms: 0.545631
  ...
# Subtest: planPomodoroEntryReorder rejects a stale source line
ok 1995 - planPomodoroEntryReorder rejects a stale source line
  ---
  duration_ms: 0.18854
  ...
# Subtest: planPomodoroEntryReorder round-trips CRLF content
ok 1996 - planPomodoroEntryReorder round-trips CRLF content
  ---
  duration_ms: 0.306735
  ...
# Subtest: planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
ok 1997 - planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
  ---
  duration_ms: 0.247532
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
ok 1998 - planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
  ---
  duration_ms: 0.378422
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up three positions and round-trips
ok 1999 - planPomodoroEntryReorder moves a placeholder up three positions and round-trips
  ---
  duration_ms: 0.550601
  ...
# Subtest: planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
ok 2000 - planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
  ---
  duration_ms: 0.275766
  ...
# Subtest: planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
ok 2001 - planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
  ---
  duration_ms: 0.601849
  ...
# Subtest: planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
ok 2002 - planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
  ---
  duration_ms: 2.195851
  ...
# Subtest: planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
ok 2003 - planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
  ---
  duration_ms: 0.380466
  ...
# Subtest: peelPomodoroMergedName removes every matching canonical plus component
ok 2004 - peelPomodoroMergedName removes every matching canonical plus component
  ---
  duration_ms: 1.658755
  ...
# Subtest: planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
ok 2005 - planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
  ---
  duration_ms: 4.035843
  ...
# Subtest: planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
ok 2006 - planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
  ---
  duration_ms: 0.782644
  ...
# Subtest: planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
ok 2007 - planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
  ---
  duration_ms: 0.731546
  ...
# Subtest: planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
ok 2008 - planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
  ---
  duration_ms: 0.902683
  ...
# Subtest: planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
ok 2009 - planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
  ---
  duration_ms: 1.386596
  ...
# Subtest: planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
ok 2010 - planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
  ---
  duration_ms: 0.992945
  ...
# Subtest: planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
ok 2011 - planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
  ---
  duration_ms: 1.831956
  ...
# Subtest: Pomodoro bullet move picker typing =NAME or Escape does not write
ok 2012 - Pomodoro bullet move picker typing =NAME or Escape does not write
  ---
  duration_ms: 3.140544
  ...
# Subtest: planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
ok 2013 - planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
  ---
  duration_ms: 0.667364
  ...
# Subtest: planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
ok 2014 - planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
  ---
  duration_ms: 0.343726
  ...
# Subtest: planPomodoroEntryRename reports unchanged when the normalized name matches the current name
ok 2015 - planPomodoroEntryRename reports unchanged when the normalized name matches the current name
  ---
  duration_ms: 0.17284
  ...
# Subtest: planPomodoroEntryRename rejects unsupported trailing content and a stale source line
ok 2016 - planPomodoroEntryRename rejects unsupported trailing content and a stale source line
  ---
  duration_ms: 0.195844
  ...
# Subtest: planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
ok 2017 - planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
  ---
  duration_ms: 0.198529
  ...
# Subtest: planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
ok 2018 - planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
  ---
  duration_ms: 3.385481
  ...
# Subtest: planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
ok 2019 - planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
  ---
  duration_ms: 1.106802
  ...
# Subtest: planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
ok 2020 - planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
  ---
  duration_ms: 0.521715
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: priority notice relative day helpers handle offsets ranges and icons
ok 2021 - priority notice relative day helpers handle offsets ranges and icons
  ---
  duration_ms: 1.868987
  ...
# Subtest: priority notice model summarizes single counted and project writes
ok 2022 - priority notice model summarizes single counted and project writes
  ---
  duration_ms: 4.667659
  ...
# Subtest: priority notice renderer builds an accessible fragment
ok 2023 - priority notice renderer builds an accessible fragment
  ---
  duration_ms: 2.868634
  ...
# Subtest: priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
ok 2024 - priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
  ---
  duration_ms: 13.335068
  ...
# Subtest: priority notice falls back to one plain notice without a DOM
ok 2025 - priority notice falls back to one plain notice without a DOM
  ---
  duration_ms: 0.620945
  ...
# Subtest: priority notice falls back to plain text when fragment rendering fails
ok 2026 - priority notice falls back to plain text when fragment rendering fails
  ---
  duration_ms: 0.374093
  ...
# Subtest: priority scheduling rolls inclusively and clamps a random value of one
ok 2027 - priority scheduling rolls inclusively and clamps a random value of one
  ---
  duration_ms: 0.515764
  ...
# Subtest: priority value rows preserve config order and expose labels ranges and current state
ok 2028 - priority value rows preserve config order and expose labels ranges and current state
  ---
  duration_ms: 0.89592
  ...
# Subtest: priority picker writes priority then rolled schedule in one guarded edit
ok 2029 - priority picker writes priority then rolled schedule in one guarded edit
  ---
  duration_ms: 17.277333
  ...
# Subtest: priority picker writes lowest priority with a wide rolled schedule
ok 2030 - priority picker writes lowest priority with a wide rolled schedule
  ---
  duration_ms: 2.478179
  ...
# Subtest: priority picker replaces both existing values without duplicating fields
ok 2031 - priority picker replaces both existing values without duplicating fields
  ---
  duration_ms: 2.574824
  ...
# Subtest: counted priority writes keep the rolled date right of the priority
ok 2032 - counted priority writes keep the rolled date right of the priority
  ---
  duration_ms: 5.463969
  ...
# Subtest: priority picker writes project priority and schedule inline atomically
ok 2033 - priority picker writes project priority and schedule inline atomically
  ---
  duration_ms: 4.801031
  ...
# Subtest: counted priority picker rolls an independent schedule for every task
ok 2034 - counted priority picker rolls an independent schedule for every task
  ---
  duration_ms: 2.3893
  ...
# Subtest: counted priority planning keeps project schedules inline
ok 2035 - counted priority planning keeps project schedules inline
  ---
  duration_ms: 0.840393
  ...
# Subtest: counted priority planning evaluates Blocked recovery per rolled date
ok 2036 - counted priority planning evaluates Blocked recovery per rolled date
  ---
  duration_ms: 0.959652
  ...
# Subtest: a counted priority batch writes one entry per task using each task's own previous level
ok 2037 - a counted priority batch writes one entry per task using each task's own previous level
  ---
  duration_ms: 0.789887
  ...
# Subtest: priority notice models carry the stored level value for the glyph
ok 2038 - priority notice models carry the stored level value for the glyph
  ---
  duration_ms: 0.358083
  ...
# Subtest: ledger priority mark lookup guards version and render
ok 2039 - ledger priority mark lookup guards version and render
  ---
  duration_ms: 0.156709
  ...
# Subtest: priority notice header reuses the shared mark when available
ok 2040 - priority notice header reuses the shared mark when available
  ---
  duration_ms: 0.369816
  ...
# Subtest: priority notice keeps the Lucide icon without a usable mark api
ok 2041 - priority notice keeps the Lucide icon without a usable mark api
  ---
  duration_ms: 1.119106
  ...
# Subtest: a counted priority batch skips a task whose rolled date equals its current date
ok 2042 - a counted priority batch skips a task whose rolled date equals its current date
  ---
  duration_ms: 4.277583
  ...
# Subtest: counted priority runtime aborts a stale session without rolling writes
ok 2043 - counted priority runtime aborts a stale session without rolling writes
  ---
  duration_ms: 1.983406
  ...
# Subtest: scheduled picker pins a priority roll only for configured current priorities
ok 2044 - scheduled picker pins a priority roll only for configured current priorities
  ---
  duration_ms: 17.991134
  ...
# Subtest: Ctrl+R replaces only the pinned priority roll and keeps it selected
ok 2045 - Ctrl+R replaces only the pinned priority roll and keeps it selected
  ---
  duration_ms: 7.4301
  ...
# Subtest: choosing a priority roll writes immediately with a deterministic reason instead of prompting
ok 2046 - choosing a priority roll writes immediately with a deterministic reason instead of prompting
  ---
  duration_ms: 5.36597
  ...
# Subtest: counted scheduled picker requires one shared configured priority
ok 2047 - counted scheduled picker requires one shared configured priority
  ---
  duration_ms: 8.01181
  ...
# Subtest: buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
ok 2048 - buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
  ---
  duration_ms: 3.181141
  ...
# Subtest: buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
ok 2049 - buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
  ---
  duration_ms: 0.370477
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
ok 2050 - buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
  ---
  duration_ms: 0.447134
  ...
# Subtest: buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
ok 2051 - buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
  ---
  duration_ms: 0.275966
  ...
# Subtest: buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
ok 2052 - buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
  ---
  duration_ms: 0.498451
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
ok 2053 - buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
  ---
  duration_ms: 0.179964
  ...
# Subtest: buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
ok 2054 - buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
  ---
  duration_ms: 0.294221
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
ok 2055 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
  ---
  duration_ms: 0.379144
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child work log under the project task
ok 2056 - buildProjectSeedFromChildBullets moves a direct-child work log under the project task
  ---
  duration_ms: 0.350749
  ...
# Subtest: buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
ok 2057 - buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
  ---
  duration_ms: 0.449157
  ...
# Subtest: buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
ok 2058 - buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
  ---
  duration_ms: 0.266068
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
ok 2059 - buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
  ---
  duration_ms: 0.160457
  ...
# Subtest: buildProjectSeedFromChildBullets moves an empty work log without forcing task output
ok 2060 - buildProjectSeedFromChildBullets moves an empty work log without forcing task output
  ---
  duration_ms: 0.116893
  ...
# Subtest: buildProjectSeedFromChildBullets moves managed logs in source order without sorting by kind
ok 2061 - buildProjectSeedFromChildBullets moves managed logs in source order without sorting by kind
  ---
  duration_ms: 0.134687
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
ok 2062 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
  ---
  duration_ms: 0.260888
  ...
# Subtest: parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
ok 2063 - parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
  ---
  duration_ms: 0.244296
  ...
# Subtest: Rotten Log markers, history reading, formatting, and generic insertion
ok 2064 - Rotten Log markers, history reading, formatting, and generic insertion
  ---
  duration_ms: 1.41514
  ...
# Subtest: parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
ok 2065 - parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
  ---
  duration_ms: 0.161719
  ...
# Subtest: parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
ok 2066 - parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
  ---
  duration_ms: 0.240359
  ...
# Subtest: normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
ok 2067 - normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
  ---
  duration_ms: 0.088409
  ...
# Subtest: parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
ok 2068 - parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
  ---
  duration_ms: 0.101183
  ...
# Subtest: formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
ok 2069 - formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
  ---
  duration_ms: 0.118446
  ...
# Subtest: insertProjectSectionNotes fills an empty existing section with a blank line then the notes
ok 2070 - insertProjectSectionNotes fills an empty existing section with a blank line then the notes
  ---
  duration_ms: 0.563165
  ...
# Subtest: insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
ok 2071 - insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
  ---
  duration_ms: 0.177669
  ...
# Subtest: insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
ok 2072 - insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
  ---
  duration_ms: 0.132332
  ...
# Subtest: insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
ok 2073 - insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
  ---
  duration_ms: 0.228305
  ...
# Subtest: insertProjectSectionNotes does not add a trailing newline when the original content had none
ok 2074 - insertProjectSectionNotes does not add a trailing newline when the original content had none
  ---
  duration_ms: 0.138625
  ...
# Subtest: insertProjectSectionNotes preserves CRLF line endings for an existing section
ok 2075 - insertProjectSectionNotes preserves CRLF line endings for an existing section
  ---
  duration_ms: 0.184973
  ...
# Subtest: insertProjectSectionNotes creates a new section using the document's CRLF line ending
ok 2076 - insertProjectSectionNotes creates a new section using the document's CRLF line ending
  ---
  duration_ms: 0.129217
  ...
# Subtest: buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
ok 2077 - buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
  ---
  duration_ms: 0.210752
  ...
# Subtest: buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
ok 2078 - buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
  ---
  duration_ms: 0.371639
  ...
# Subtest: buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
ok 2079 - buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
  ---
  duration_ms: 0.123054
  ...
# Subtest: buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
ok 2080 - buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
  ---
  duration_ms: 1.130507
  ...
# Subtest: project conversion accepts blocked sources and extracts their managed dependency child
ok 2081 - project conversion accepts blocked sources and extracts their managed dependency child
  ---
  duration_ms: 1.994807
  ...
# Subtest: project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
ok 2082 - project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
  ---
  duration_ms: 1.342032
  ...
# Subtest: buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
ok 2083 - buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
  ---
  duration_ms: 0.375567
  ...
# Subtest: buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
ok 2084 - buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
  ---
  duration_ms: 0.220261
  ...
# Subtest: buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
ok 2085 - buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
  ---
  duration_ms: 0.197998
  ...
# Subtest: insertProjectManagedLogLines preserves CRLF line endings
ok 2086 - insertProjectManagedLogLines preserves CRLF line endings
  ---
  duration_ms: 0.174663
  ...
# Subtest: findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
ok 2087 - findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
  ---
  duration_ms: 0.207476
  ...
# Subtest: getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
ok 2088 - getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
  ---
  duration_ms: 0.212826
  ...
# Subtest: getProjectFromTaskNoticeText reports moved log kinds in a fixed order
ok 2089 - getProjectFromTaskNoticeText reports moved log kinds in a fixed order
  ---
  duration_ms: 0.110281
  ...
# Subtest: forward conversion leaves the project Ready when only the source status was Blocked
ok 2090 - forward conversion leaves the project Ready when only the source status was Blocked
  ---
  duration_ms: 0.370056
  ...
# Subtest: buildTaskBlockFromProjectNote restores the worked example and round-trips
ok 2091 - buildTaskBlockFromProjectNote restores the worked example and round-trips
  ---
  duration_ms: 9.627984
  ...
# Subtest: project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
ok 2092 - project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
  ---
  duration_ms: 2.476636
  ...
# Subtest: buildTaskLineFromProjectNote preserves status, tags, and fields
ok 2093 - buildTaskLineFromProjectNote preserves status, tags, and fields
  ---
  duration_ms: 1.567942
  ...
# Subtest: getProjectReversalBlockId inverts the forward basename helper
ok 2094 - getProjectReversalBlockId inverts the forward basename helper
  ---
  duration_ms: 0.146129
  ...
# Subtest: formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
ok 2095 - formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
  ---
  duration_ms: 0.145337
  ...
# Subtest: splitProjectNoteForReversal treats TASKS as the task section and keeps section order
ok 2096 - splitProjectNoteForReversal treats TASKS as the task section and keeps section order
  ---
  duration_ms: 0.931748
  ...
# Subtest: indentProjectReversalLine preserves relative depth and drops blanks
ok 2097 - indentProjectReversalLine preserves relative depth and drops blanks
  ---
  duration_ms: 0.477051
  ...
# Subtest: buildTaskBlockFromProjectNote reports structure and frontmatter errors
ok 2098 - buildTaskBlockFromProjectNote reports structure and frontmatter errors
  ---
  duration_ms: 1.427615
  ...
# Subtest: buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
ok 2099 - buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
  ---
  duration_ms: 1.054463
  ...
# Subtest: rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
ok 2100 - rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
  ---
  duration_ms: 0.53455
  ...
# Subtest: collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
ok 2101 - collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
  ---
  duration_ms: 0.59723
  ...
# Subtest: getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
ok 2102 - getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
  ---
  duration_ms: 0.212976
  ...
# Subtest: convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
ok 2103 - convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
  ---
  duration_ms: 7.070142
  ...
# Subtest: project reversal recovers tagged residents when they leave a blocked project
ok 2104 - project reversal recovers tagged residents when they leave a blocked project
  ---
  duration_ms: 4.84686
  ...
# Subtest: convertProjectNoteToTask separates the restored task from a count-only parent section
ok 2105 - convertProjectNoteToTask separates the restored task from a count-only parent section
  ---
  duration_ms: 1.868335
  ...
# Subtest: createProjectNoteFromTask dispatches reverse only on a real ^prj line
ok 2106 - createProjectNoteFromTask dispatches reverse only on a real ^prj line
  ---
  duration_ms: 4.030181
  ...
# Subtest: convertProjectNoteToTask refusals leave every file untouched
ok 2107 - convertProjectNoteToTask refusals leave every file untouched
  ---
  duration_ms: 3.923658
  ...
# Subtest: planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
ok 2108 - planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
  ---
  duration_ms: 0.17289
  ...
# Subtest: convertProjectNoteToTask writes the parent first when it links to \#^prj
ok 2109 - convertProjectNoteToTask writes the parent first when it links to \#^prj
  ---
  duration_ms: 1.235068
  ...
# Subtest: convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
ok 2110 - convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
  ---
  duration_ms: 3.07559
  ...
# Subtest: convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
ok 2111 - convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
  ---
  duration_ms: 0.966825
  ...
# Subtest: convertProjectNoteToTask reports post-write failures without rolling back
ok 2112 - convertProjectNoteToTask reports post-write failures without rolling back
  ---
  duration_ms: 0.998726
  ...
# Subtest: convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
ok 2113 - convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
  ---
  duration_ms: 1.074741
  ...
# Subtest: convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
ok 2114 - convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
  ---
  duration_ms: 1.475796
  ...
# Subtest: v2 reading task opens its source_pdf in Highlights without writes
ok 2115 - v2 reading task opens its source_pdf in Highlights without writes
  ---
  duration_ms: 4.766035
  ...
# Subtest: every reading-task lane and \#REF casing opens
ok 2116 - every reading-task lane and \#REF casing opens
  ---
  duration_ms: 1.847015
  ...
# Subtest: v1 tracker resolves a PDF link or falls back to its own source_pdf
ok 2117 - v1 tracker resolves a PDF link or falls back to its own source_pdf
  ---
  duration_ms: 0.775981
  ...
# Subtest: plain, embedded, struck, and 🍅 Task Links resolve reading tasks
ok 2118 - plain, embedded, struck, and 🍅 Task Links resolve reading tasks
  ---
  duration_ms: 2.679964
  ...
# Subtest: bare managed embed in a reference note resolves its embedded task
ok 2119 - bare managed embed in a reference note resolves its embedded task
  ---
  duration_ms: 0.528178
  ...
# Subtest: ordinary lines, unresolved Task Links, fences, and outside focus delegate once
ok 2120 - ordinary lines, unresolved Task Links, fences, and outside focus delegate once
  ---
  duration_ms: 1.073248
  ...
# Subtest: identified reading tasks show notices without delegating
ok 2121 - identified reading tasks show notices without delegating
  ---
  duration_ms: 0.618199
  ...
# Subtest: unsafe source_pdf values are refused
ok 2122 - unsafe source_pdf values are refused
  ---
  duration_ms: 0.307757
  ...
# Subtest: bundle launch retries with the app name, and reports stderr on total failure
ok 2123 - bundle launch retries with the app name, and reports stderr on total failure
  ---
  duration_ms: 0.854731
  ...
# Subtest: off macOS shows the selected notice and managed ref-note prose delegates
ok 2124 - off macOS shows the selected notice and managed ref-note prose delegates
  ---
  duration_ms: 0.670369
  ...
# Subtest: pure helpers normalize and parse reference PDF paths
ok 2125 - pure helpers normalize and parse reference PDF paths
  ---
  duration_ms: 0.3148
  ...
# Subtest: command registration is custom-hotkey only
ok 2126 - command registration is custom-hotkey only
  ---
  duration_ms: 0.392829
  ...
# Subtest: nav api openReferencePdf hands a source_pdf to Highlights without version or vault writes
ok 2127 - nav api openReferencePdf hands a source_pdf to Highlights without version or vault writes
  ---
  duration_ms: 0.781642
  ...
# Subtest: nav api openReferencePdf settles to a reason instead of throwing
ok 2128 - nav api openReferencePdf settles to a reason instead of throwing
  ---
  duration_ms: 0.451141
  ...
# Subtest: reading tasks read with the book prefix, plain tasks unchanged
ok 2129 - reading tasks read with the book prefix, plain tasks unchanged
  ---
  duration_ms: 1.267909
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 2130 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.248805
  ...
# Subtest: picker rows carry the book prefix in displayText
ok 2131 - picker rows carry the book prefix in displayText
  ---
  duration_ms: 0.727939
  ...
# Subtest: managed reference rename modal and submit are refused
ok 2132 - managed reference rename modal and submit are refused
  ---
  duration_ms: 1.310611
  ...
# Subtest: legacy ref notes and non-ref notes still rename
ok 2133 - legacy ref notes and non-ref notes still rename
  ---
  duration_ms: 0.895068
  ...
# Subtest: managed reference predicate checks path and non-empty source_pdf
ok 2134 - managed reference predicate checks path and non-empty source_pdf
  ---
  duration_ms: 0.200793
  ...
# Subtest: planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
ok 2135 - planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
  ---
  duration_ms: 6.292087
  ...
# Subtest: planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
ok 2136 - planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
  ---
  duration_ms: 2.225557
  ...
# Subtest: runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
ok 2137 - runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
  ---
  duration_ms: 5.305735
  ...
# Subtest: runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
ok 2138 - runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
  ---
  duration_ms: 3.487065
  ...
# Subtest: runtime: no daily note today still writes the schedule with no Pomodoro chip
ok 2139 - runtime: no daily note today still writes the schedule with no Pomodoro chip
  ---
  duration_ms: 0.601949
  ...
# Subtest: runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
ok 2140 - runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
  ---
  duration_ms: 1.148662
  ...
# Subtest: runtime: vault.process throwing during the daily-note write is reported without throwing
ok 2141 - runtime: vault.process throwing during the daily-note write is reported without throwing
  ---
  duration_ms: 0.910598
  ...
# Subtest: runtime: the daily note open in another editor is written through that editor in its own transaction
ok 2142 - runtime: the daily note open in another editor is written through that editor in its own transaction
  ---
  duration_ms: 1.771791
  ...
# Subtest: runtime: re-running the same deferral gesture is idempotent
ok 2143 - runtime: re-running the same deferral gesture is idempotent
  ---
  duration_ms: 0.935034
  ...
# Subtest: runtime: a counted scheduled batch prunes exactly the targets that land on a future date
ok 2144 - runtime: a counted scheduled batch prunes exactly the targets that land on a future date
  ---
  duration_ms: 3.711583
  ...
# Subtest: runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
ok 2145 - runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
  ---
  duration_ms: 3.389169
  ...
# Subtest: runtime: the source note being today's daily note folds the prune into a single editor transaction
ok 2146 - runtime: the source note being today's daily note folds the prune into a single editor transaction
  ---
  duration_ms: 0.907382
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: bare future scheduled writes block only real supported open inline tasks
ok 2147 - bare future scheduled writes block only real supported open inline tasks
  ---
  duration_ms: 5.133847
  ...
# Subtest: single runtime transclusion toggle preserves viewport in one line transaction
ok 2148 - single runtime transclusion toggle preserves viewport in one line transaction
  ---
  duration_ms: 2.105447
  ...
# Subtest: same-file runtime toggle changes only markers, never fields or statuses
ok 2149 - same-file runtime toggle changes only markers, never fields or statuses
  ---
  duration_ms: 0.754159
  ...
# Subtest: pure toggle leaves a cursor moved during the toggle where it landed
ok 2150 - pure toggle leaves a cursor moved during the toggle where it landed
  ---
  duration_ms: 0.293049
  ...
# Subtest: counted runtime transclusion toggle preserves viewport and caret
ok 2151 - counted runtime transclusion toggle preserves viewport and caret
  ---
  duration_ms: 0.795819
  ...
# Subtest: counted property runtime uses one transaction and preserves caret and viewport
ok 2152 - counted property runtime uses one transaction and preserves caret and viewport
  ---
  duration_ms: 3.383758
  ...
# Subtest: bare due schedule recovery is guarded and can change only task status
ok 2153 - bare due schedule recovery is guarded and can change only task status
  ---
  duration_ms: 2.359843
  ...
# Subtest: counted due recovery applies Ready Next and In Progress in one transaction
ok 2154 - counted due recovery applies Ready Next and In Progress in one transaction
  ---
  duration_ms: 4.588326
  ...
# Subtest: scheduled recovery aborts after an asynchronous source change
ok 2155 - scheduled recovery aborts after an asynchronous source change
  ---
  duration_ms: 0.777434
  ...
# Subtest: counted property runtime aborts a stale batch without a transaction
ok 2156 - counted property runtime aborts a stale batch without a transaction
  ---
  duration_ms: 0.480337
  ...
# Subtest: counted project scheduling writes an inline date and blocks tagged residents
ok 2157 - counted project scheduling writes an inline date and blocks tagged residents
  ---
  duration_ms: 2.555197
  ...
# Subtest: future project scheduling prunes resident links and an emptied Pomodoro
ok 2158 - future project scheduling prunes resident links and an emptied Pomodoro
  ---
  duration_ms: 2.868323
  ...
# Subtest: single project scheduling recovers due residents through the gate
ok 2159 - single project scheduling recovers due residents through the gate
  ---
  duration_ms: 1.858416
  ...
# Subtest: single project schedule deletion removes propagated copies and recovers
ok 2160 - single project schedule deletion removes propagated copies and recovers
  ---
  duration_ms: 1.65631
  ...
# Subtest: formatPriorityRollScheduleReason covers all four shapes
ok 2161 - formatPriorityRollScheduleReason covers all four shapes
  ---
  duration_ms: 1.410782
  ...
# Subtest: the priority-roll picker row keeps range detail and stores the exact roll
ok 2162 - the priority-roll picker row keeps range detail and stores the exact roll
  ---
  duration_ms: 0.780279
  ...
# Subtest: buildPriorityRollScheduleLog returns null when the roll does not move the date
ok 2163 - buildPriorityRollScheduleLog returns null when the roll does not move the date
  ---
  duration_ms: 0.906209
  ...
# Subtest: getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
ok 2164 - getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
  ---
  duration_ms: 1.056847
  ...
# Subtest: a priority roll onto the current date writes the date but no log
ok 2165 - a priority roll onto the current date writes the date but no log
  ---
  duration_ms: 15.327401
  ...
# Subtest: a typed reason on an unchanged date is still written
ok 2166 - a typed reason on an unchanged date is still written
  ---
  duration_ms: 0.784167
  ...
# Subtest: schedule log bullet formatting and parsing round-trip with and without a previous value
ok 2167 - schedule log bullet formatting and parsing round-trip with and without a previous value
  ---
  duration_ms: 0.962948
  ...
# Subtest: formatScheduleLogEntryText renders entry text without indent or marker
ok 2168 - formatScheduleLogEntryText renders entry text without indent or marker
  ---
  duration_ms: 0.129287
  ...
# Subtest: schedule reason text normalization trims, collapses whitespace, and flags inline fields
ok 2169 - schedule reason text normalization trims, collapses whitespace, and flags inline fields
  ---
  duration_ms: 0.435561
  ...
# Subtest: findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
ok 2170 - findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
  ---
  duration_ms: 0.756123
  ...
# Subtest: getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
ok 2171 - getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
  ---
  duration_ms: 0.250288
  ...
# Subtest: planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
ok 2172 - planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
  ---
  duration_ms: 0.464606
  ...
# Subtest: planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
ok 2173 - planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
  ---
  duration_ms: 0.188099
  ...
# Subtest: planScheduleLogEntry uses the fallback only when a marker exists
ok 2174 - planScheduleLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.213457
  ...
# Subtest: a typed reason wins over the fallback
ok 2175 - a typed reason wins over the fallback
  ---
  duration_ms: 0.148884
  ...
# Subtest: the fallback is suppressed on an unchanged date
ok 2176 - the fallback is suppressed on an unchanged date
  ---
  duration_ms: 0.121121
  ...
# Subtest: no reason and no fallback still guards empty-reason
ok 2177 - no reason and no fallback still guards empty-reason
  ---
  duration_ms: 0.102575
  ...
# Subtest: getScheduleLogWriteOutcome maps plan outcomes for writers
ok 2178 - getScheduleLogWriteOutcome maps plan outcomes for writers
  ---
  duration_ms: 0.143584
  ...
# Subtest: hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
ok 2179 - hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
  ---
  duration_ms: 0.128164
  ...
# Subtest: counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
ok 2180 - counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
  ---
  duration_ms: 1.824421
  ...
# Subtest: empty reason through the counted planner writes no schedule log entries
ok 2181 - empty reason through the counted planner writes no schedule log entries
  ---
  duration_ms: 0.549028
  ...
# Subtest: a counted scheduled session logs only the tasks that already keep a log
ok 2182 - a counted scheduled session logs only the tasks that already keep a log
  ---
  duration_ms: 0.598582
  ...
# Subtest: the counted notice wording distinguishes a fallback batch from a typed-reason batch
ok 2183 - the counted notice wording distinguishes a fallback batch from a typed-reason batch
  ---
  duration_ms: 3.985948
  ...
# Subtest: setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
ok 2184 - setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
  ---
  duration_ms: 0.398691
  ...
# Subtest: setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
ok 2185 - setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
  ---
  duration_ms: 3.050992
  ...
# Subtest: priority bullet property config normalizes frozen levels and preserves existing shapes
ok 2186 - priority bullet property config normalizes frozen levels and preserves existing shapes
  ---
  duration_ms: 2.152558
  ...
# Subtest: priority bullet property config rejects each invalid schema category once
ok 2187 - priority bullet property config rejects each invalid schema category once
  ---
  duration_ms: 0.958058
  ...
# Subtest: project scheduling targets the inline ^prj field
ok 2188 - project scheduling targets the inline ^prj field
  ---
  duration_ms: 1.863576
  ...
# Subtest: local task properties are addable only on valid tasks but invalid metadata stays removable
ok 2189 - local task properties are addable only on valid tasks but invalid metadata stays removable
  ---
  duration_ms: 0.302337
  ...
# Subtest: dependency parent write validation rejects stale, Pomodoro, and fenced parents
ok 2190 - dependency parent write validation rejects stale, Pomodoro, and fenced parents
  ---
  duration_ms: 0.479696
  ...
# Subtest: counted property targets mean current plus N real tasks without wrapping
ok 2191 - counted property targets mean current plus N real tasks without wrapping
  ---
  duration_ms: 0.687432
  ...
# Subtest: counted property metadata distinguishes absent, common, and mixed values
ok 2192 - counted property metadata distinguishes absent, common, and mixed values
  ---
  duration_ms: 0.658386
  ...
# Subtest: counted priority metadata reports labels for common and mixed values
ok 2193 - counted priority metadata reports labels for common and mixed values
  ---
  duration_ms: 0.566902
  ...
# Subtest: counted scheduled planning updates the motivating three tasks atomically
ok 2194 - counted scheduled planning updates the motivating three tasks atomically
  ---
  duration_ms: 2.336139
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: project schedule validation accepts only real YYYY-MM-DD dates
ok 2195 - project schedule validation accepts only real YYYY-MM-DD dates
  ---
  duration_ms: 1.043531
  ...
# Subtest: source task schedule is extracted without losing task metadata
ok 2196 - source task schedule is extracted without losing task metadata
  ---
  duration_ms: 1.308477
  ...
# Subtest: source task schedule errors are focused and ambiguous fields fail
ok 2197 - source task schedule errors are focused and ambiguous fields fail
  ---
  duration_ms: 0.361149
  ...
# Subtest: project creation frontmatter never stores the task schedule
ok 2198 - project creation frontmatter never stores the task schedule
  ---
  duration_ms: 0.163261
  ...
# Subtest: future schedule labels use local date-only boundaries
ok 2199 - future schedule labels use local date-only boundaries
  ---
  duration_ms: 0.582581
  ...
# Subtest: scheduled recovery selects current and newest earlier daily across gaps
ok 2200 - scheduled recovery selects current and newest earlier daily across gaps
  ---
  duration_ms: 0.557143
  ...
# Subtest: scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
ok 2201 - scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
  ---
  duration_ms: 8.562661
  ...
# Subtest: scheduled recovery defers incompatible status settings and ambiguous identities
ok 2202 - scheduled recovery defers incompatible status settings and ambiguous identities
  ---
  duration_ms: 0.457944
  ...
# Subtest: scheduled recovery honors custom open and closed Tasks status types
ok 2203 - scheduled recovery honors custom open and closed Tasks status types
  ---
  duration_ms: 0.625013
  ...
# Subtest: scheduled recovery honors the configured Tasks global filter
ok 2204 - scheduled recovery honors the configured Tasks global filter
  ---
  duration_ms: 0.540742
  ...
# Subtest: child picker schedule metadata reads the inline ^prj date
ok 2205 - child picker schedule metadata reads the inline ^prj date
  ---
  duration_ms: 0.985441
  ...
# Subtest: task move destination schedule hydration reads cached ^prj content
ok 2206 - task move destination schedule hydration reads cached ^prj content
  ---
  duration_ms: 0.47696
  ...
# Subtest: project lifecycle task classification requires unfenced \#task with trailing ^prj
ok 2207 - project lifecycle task classification requires unfenced \#task with trailing ^prj
  ---
  duration_ms: 0.165756
  ...
# Subtest: valid Obsidian tasks require a standalone \#task checkbox in real note content
ok 2208 - valid Obsidian tasks require a standalone \#task checkbox in real note content
  ---
  duration_ms: 0.155777
  ...
# Subtest: choosing a scheduled date enters the combined review without writing anything
ok 2209 - choosing a scheduled date enters the combined review without writing anything
  ---
  duration_ms: 12.253474
  ...
# Subtest: choosing a priority level does not enter the schedule review
ok 2210 - choosing a priority level does not enter the schedule review
  ---
  duration_ms: 9.288687
  ...
# Subtest: confirming an empty reason on a task with an existing schedule log appends an unexplained entry
ok 2211 - confirming an empty reason on a task with an existing schedule log appends an unexplained entry
  ---
  duration_ms: 6.355949
  ...
# Subtest: confirming an empty reason on a task with no schedule log writes only the date
ok 2212 - confirming an empty reason on a task with no schedule log writes only the date
  ---
  duration_ms: 3.121137
  ...
# Subtest: review stage getFilteredItems always returns exactly one synthetic preview item
ok 2213 - review stage getFilteredItems always returns exactly one synthetic preview item
  ---
  duration_ms: 1.359926
  ...
# Subtest: the review preview row previews the entry it will write
ok 2214 - the review preview row previews the entry it will write
  ---
  duration_ms: 4.065227
  ...
# Subtest: the review footer flips between Skip optional logs and Apply schedule as the Reason changes
ok 2215 - the review footer flips between Skip optional logs and Apply schedule as the Reason changes
  ---
  duration_ms: 1.407206
  ...
# Subtest: closing the picker during the review clears pending schedule state and writes nothing
ok 2216 - closing the picker during the review clears pending schedule state and writes nothing
  ---
  duration_ms: 1.166787
  ...
# Subtest: scheduling Work Log eligibility requires Pending or Next \#task lines
ok 2217 - scheduling Work Log eligibility requires Pending or Next \#task lines
  ---
  duration_ms: 1.209839
  ...
# Subtest: single Pending explicit date opens one review and writes both logs
ok 2218 - single Pending explicit date opens one review and writes both logs
  ---
  duration_ms: 20.635051
  ...
# Subtest: single Next blank and whitespace summaries schedule without a Work Log
ok 2219 - single Next blank and whitespace summaries schedule without a Work Log
  ---
  duration_ms: 5.520445
  ...
# Subtest: Escape at the review writes nothing, with or without typed text
ok 2220 - Escape at the review writes nothing, with or without typed text
  ---
  duration_ms: 5.975974
  ...
# Subtest: Ready and Blocked explicit dates review the Reason with no Work summary field
ok 2221 - Ready and Blocked explicit dates review the Reason with no Work summary field
  ---
  duration_ms: 3.793078
  ...
# Subtest: future scheduling on Pending marks Blocked but still writes the Work Log
ok 2222 - future scheduling on Pending marks Blocked but still writes the Work Log
  ---
  duration_ms: 4.918788
  ...
# Subtest: today date on Pending still offers the Work Log
ok 2223 - today date on Pending still offers the Work Log
  ---
  duration_ms: 3.298946
  ...
# Subtest: priority pick on Pending freezes its roll and offers the Work Log
ok 2224 - priority pick on Pending freezes its roll and offers the Work Log
  ---
  duration_ms: 4.250621
  ...
# Subtest: counted mixed statuses share one summary only on Pending and Next
ok 2225 - counted mixed statuses share one summary only on Pending and Next
  ---
  duration_ms: 6.709475
  ...
# Subtest: counted planner composes Schedule and Work Logs bottom-up above later targets
ok 2226 - counted planner composes Schedule and Work Logs bottom-up above later targets
  ---
  duration_ms: 1.149373
  ...
# Subtest: counted planner writes a Work Log even when the date is unchanged
ok 2227 - counted planner writes a Work Log even when the date is unchanged
  ---
  duration_ms: 0.348896
  ...
# Subtest: scheduling Work Log ownership keeps nested logs and CRLF endings
ok 2228 - scheduling Work Log ownership keeps nested logs and CRLF endings
  ---
  duration_ms: 0.82258
  ...
# Subtest: scheduling Work Log warns on :: and preserves Markdown
ok 2229 - scheduling Work Log warns on :: and preserves Markdown
  ---
  duration_ms: 2.040854
  ...
# Subtest: stale task while reviewing refuses with no scheduling or log writes
ok 2230 - stale task while reviewing refuses with no scheduling or log writes
  ---
  duration_ms: 1.527285
  ...
# Subtest: scheduling prompts never leak into lane or cancel stages
ok 2231 - scheduling prompts never leak into lane or cancel stages
  ---
  duration_ms: 2.633155
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: Pomodoro-marked links are not managed dependency bullets
ok 2232 - Pomodoro-marked links are not managed dependency bullets
  ---
  duration_ms: 1.386005
  ...
# Subtest: deleting inline scheduled metadata recovers Blocked targets by snapshot rank
ok 2233 - deleting inline scheduled metadata recovers Blocked targets by snapshot rank
  ---
  duration_ms: 3.613726
  ...
# Subtest: counted future scheduling blocks only supported open inline task statuses
ok 2234 - counted future scheduling blocks only supported open inline task statuses
  ---
  duration_ms: 1.693381
  ...
# Subtest: counted property planning rejects any stale source with no partial result
ok 2235 - counted property planning rejects any stale source with no partial result
  ---
  duration_ms: 0.303609
  ...
# Subtest: counted project scheduling writes the ^prj inline date and blocks tagged residents
ok 2236 - counted project scheduling writes the ^prj inline date and blocks tagged residents
  ---
  duration_ms: 1.768285
  ...
# Subtest: moving a project schedule earlier replaces only exact old-date copies
ok 2237 - moving a project schedule earlier replaces only exact old-date copies
  ---
  duration_ms: 0.385356
  ...
# Subtest: future project schedules block every open resident and consume review status
ok 2238 - future project schedules block every open resident and consume review status
  ---
  duration_ms: 0.589956
  ...
# Subtest: due project dates recover residents through the gate and write unblocked markers
ok 2239 - due project dates recover residents through the gate and write unblocked markers
  ---
  duration_ms: 0.564116
  ...
# Subtest: schedule deletion removes only exact project-date copies and recovers residents
ok 2240 - schedule deletion removes only exact project-date copies and recovers residents
  ---
  duration_ms: 0.921568
  ...
# Subtest: dependency lines render one canonical Depends-On line per parent
ok 2241 - dependency lines render one canonical Depends-On line per parent
  ---
  duration_ms: 0.630122
  ...
# Subtest: dependency IDs encode root and nested Markdown paths deterministically
ok 2242 - dependency IDs encode root and nested Markdown paths deterministically
  ---
  duration_ms: 0.940635
  ...
# Subtest: prompted block IDs truthfully replace legacy id fields
ok 2243 - prompted block IDs truthfully replace legacy id fields
  ---
  duration_ms: 0.158092
  ...
# Subtest: dependency navigation identity includes note path and folds legacy children
ok 2244 - dependency navigation identity includes note path and folds legacy children
  ---
  duration_ms: 0.838219
  ...
# Subtest: retired dependency bullets are excluded from single and counted toggles
ok 2245 - retired dependency bullets are excluded from single and counted toggles
  ---
  duration_ms: 1.323005
  ...
# Subtest: dependsOn replacement accepts spaces around field name and separator
ok 2246 - dependsOn replacement accepts spaces around field name and separator
  ---
  duration_ms: 0.274784
  ...
# Subtest: task status helpers keep Blocked open but rankless
ok 2247 - task status helpers keep Blocked open but rankless
  ---
  duration_ms: 0.282288
  ...
# Subtest: a due project date with only closed Depends-On history strips the tag
ok 2248 - a due project date with only closed Depends-On history strips the tag
  ---
  duration_ms: 0.693714
  ...
# Subtest: Ctrl+D with only closed Depends-On history strips the tag
ok 2249 - Ctrl+D with only closed Depends-On history strips the tag
  ---
  duration_ms: 0.37208
  ...
# Subtest: Ctrl+D with an open Depends-On link remaining keeps the tag
ok 2250 - Ctrl+D with an open Depends-On link remaining keeps the tag
  ---
  duration_ms: 0.290725
  ...
# Subtest: counted ^prj schedule sessions write [unblocked::] when the writer is passed
ok 2251 - counted ^prj schedule sessions write [unblocked::] when the writer is passed
  ---
  duration_ms: 0.445079
  ...
# Subtest: a due project date keeps the tag while ^prj holds Depends-On links
ok 2252 - a due project date keeps the tag while ^prj holds Depends-On links
  ---
  duration_ms: 0.286788
  ...
# Subtest: a due project date strips the tag while a resident with its own reason stays Blocked
ok 2253 - a due project date strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.29872
  ...
# Subtest: Ctrl+D strips the tag while a resident with its own reason stays Blocked
ok 2254 - Ctrl+D strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.350079
  ...
# Subtest: counted scheduled deletes recover with [unblocked::] when the writer is passed
ok 2255 - counted scheduled deletes recover with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.280465
  ...
# Subtest: section-header navigation moves normally and cycles at boundaries
ok 2256 - section-header navigation moves normally and cycles at boundaries
  ---
  duration_ms: 2.501463
  ...
# Subtest: section-header navigation wraps from beyond document boundaries
ok 2257 - section-header navigation wraps from beyond document boundaries
  ---
  duration_ms: 0.220781
  ...
# Subtest: section-header navigation handles single-header and no-header notes
ok 2258 - section-header navigation handles single-header and no-header notes
  ---
  duration_ms: 0.231542
  ...
# Subtest: open-task navigation scan includes Ready In Progress and Next and excludes Blocked
ok 2259 - open-task navigation scan includes Ready In Progress and Next and excludes Blocked
  ---
  duration_ms: 0.611697
  ...
# Subtest: open-task navigation keeps existing Pomodoro ledger targets
ok 2260 - open-task navigation keeps existing Pomodoro ledger targets
  ---
  duration_ms: 0.609423
  ...
# Subtest: next and previous jumps skip Blocked tasks and wrap to an allowed task
ok 2261 - next and previous jumps skip Blocked tasks and wrap to an allowed task
  ---
  duration_ms: 0.376168
  ...
# Subtest: blocked-only notes and a sole current allowed task have no jump target
ok 2262 - blocked-only notes and a sole current allowed task have no jump target
  ---
  duration_ms: 0.172059
  ...
# Subtest: counted open-task jumps select the Nth eligible target and wrap modulo the list
ok 2263 - counted open-task jumps select the Nth eligible target and wrap modulo the list
  ---
  duration_ms: 0.333446
  ...
# Subtest: counted open-task jumps keep sole-target and invalid-repeat behavior
ok 2264 - counted open-task jumps keep sole-target and invalid-repeat behavior
  ---
  duration_ms: 0.583794
  ...
# Subtest: tab pin Vim action registers once and toggles only the active leaf once
ok 2265 - tab pin Vim action registers once and toggles only the active leaf once
  ---
  duration_ms: 3.221117
  ...
# Subtest: tab pin toggle fails safely without a supported active leaf
ok 2266 - tab pin toggle fails safely without a supported active leaf
  ---
  duration_ms: 0.23075
  ...
# Subtest: close tabs left preserves pinned sibling tabs and refocuses active tab
ok 2267 - close tabs left preserves pinned sibling tabs and refocuses active tab
  ---
  duration_ms: 0.915577
  ...
# Subtest: close tabs right preserves pinned siblings and ignores the left side
ok 2268 - close tabs right preserves pinned siblings and ignores the left side
  ---
  duration_ms: 0.338235
  ...
# Subtest: close other tabs preserves pinned siblings on both sides
ok 2269 - close other tabs preserves pinned siblings on both sides
  ---
  duration_ms: 0.278642
  ...
# Subtest: close sibling tabs is a silent no-op when the scoped range is all pinned
ok 2270 - close sibling tabs is a silent no-op when the scoped range is all pinned
  ---
  duration_ms: 0.252552
  ...
# Subtest: close sibling tabs honors every pinned leaf representation
ok 2271 - close sibling tabs honors every pinned leaf representation
  ---
  duration_ms: 0.302448
  ...
# Subtest: close sibling tabs treats throwing view state as unpinned
ok 2272 - close sibling tabs treats throwing view state as unpinned
  ---
  duration_ms: 0.433918
  ...
# Subtest: tab pin Vim registration retries after adapter availability
ok 2273 - tab pin Vim registration retries after adapter availability
  ---
  duration_ms: 0.986122
  ...
# Subtest: isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
ok 2274 - isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
  ---
  duration_ms: 4.273364
  ...
# Subtest: isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
ok 2275 - isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
  ---
  duration_ms: 0.715826
  ...
# Subtest: isPomodoroTaskLinkLine refuses Depends-On lines and prose links
ok 2276 - isPomodoroTaskLinkLine refuses Depends-On lines and prose links
  ---
  duration_ms: 0.271388
  ...
# Subtest: decideTaskLinkLaneMode starts when any target is Next
ok 2277 - decideTaskLinkLaneMode starts when any target is Next
  ---
  duration_ms: 0.232313
  ...
# Subtest: taskLinkLaneRefusalFor renders every D5 refusal
ok 2278 - taskLinkLaneRefusalFor renders every D5 refusal
  ---
  duration_ms: 0.170185
  ...
# Subtest: planTaskLinkLaneBatch starts Next targets and leaves the rest alone
ok 2279 - planTaskLinkLaneBatch starts Next targets and leaves the rest alone
  ---
  duration_ms: 1.289892
  ...
# Subtest: planTaskLinkLaneBatch pauses with one shared Work Log entry
ok 2280 - planTaskLinkLaneBatch pauses with one shared Work Log entry
  ---
  duration_ms: 0.765852
  ...
# Subtest: planTaskLinkLaneBatch applies the freshness stamp last
ok 2281 - planTaskLinkLaneBatch applies the freshness stamp last
  ---
  duration_ms: 0.305624
  ...
# Subtest: planTaskLinkLaneBatch dedupes lines and refuses stale preimages
ok 2282 - planTaskLinkLaneBatch dedupes lines and refuses stale preimages
  ---
  duration_ms: 0.500135
  ...
# Subtest: buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
ok 2283 - buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
  ---
  duration_ms: 0.700937
  ...
# Subtest: taskLinkLanePromptState drives the Move to Next prompt
ok 2284 - taskLinkLanePromptState drives the Move to Next prompt
  ---
  duration_ms: 0.263473
  ...
# Subtest: TaskLinkLanePromptModal submits, previews live, and cancels silently
ok 2285 - TaskLinkLanePromptModal submits, previews live, and cancels silently
  ---
  duration_ms: 1.538837
  ...
# Subtest: TaskLinkLanePromptModal renders the batch context card
ok 2286 - TaskLinkLanePromptModal renders the batch context card
  ---
  duration_ms: 0.358965
  ...
# Subtest: findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
ok 2287 - findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
  ---
  duration_ms: 0.307396
  ...
# Subtest: L1: toggle starts a Next link, stamps, hints, and notices
ok 2288 - L1: toggle starts a Next link, stamps, hints, and notices
  ---
  duration_ms: 3.439774
  ...
# Subtest: L2/L3: toggle pauses through the prompt, logging one shared entry
ok 2289 - L2/L3: toggle pauses through the prompt, logging one shared entry
  ---
  duration_ms: 12.454859
  ...
# Subtest: L4: cancelling the prompt writes nothing and shows no Notice
ok 2290 - L4: cancelling the prompt writes nothing and shows no Notice
  ---
  duration_ms: 1.155725
  ...
# Subtest: L5: both directions run the same toggle twice for a round trip
ok 2291 - L5: both directions run the same toggle twice for a round trip
  ---
  duration_ms: 1.979838
  ...
# Subtest: L6: Ready, Blocked, done, and cancelled targets are refused
ok 2292 - L6: Ready, Blocked, done, and cancelled targets are refused
  ---
  duration_ms: 2.072366
  ...
# Subtest: L6: missing targets keep the existing resolver error
ok 2293 - L6: missing targets keep the existing resolver error
  ---
  duration_ms: 0.306365
  ...
# Subtest: L7: a counted start flips every Next sibling and leaves In Progress alone
ok 2294 - L7: a counted start flips every Next sibling and leaves In Progress alone
  ---
  duration_ms: 0.642686
  ...
# Subtest: L8: a counted pause prompts once and skips Blocked with a count
ok 2295 - L8: a counted pause prompts once and skips Blocked with a count
  ---
  duration_ms: 2.22176
  ...
# Subtest: L9: an over-long count clamps at the entry end without error
ok 2296 - L9: an over-long count clamps at the entry end without error
  ---
  duration_ms: 0.955082
  ...
# Subtest: L10: a closed-entry history line toggles the task and keeps the line
ok 2297 - L10: a closed-entry history line toggles the task and keeps the line
  ---
  duration_ms: 0.444989
  ...
# Subtest: L11: a target edited while the prompt is open refuses stale
ok 2298 - L11: a target edited while the prompt is open refuses stale
  ---
  duration_ms: 2.230175
  ...
# Subtest: L12: an embedded Pomodoro link takes the two-state toggle
ok 2299 - L12: an embedded Pomodoro link takes the two-state toggle
  ---
  duration_ms: 0.626205
  ...
# Subtest: L14: the same task linked twice in a batch is written once
ok 2300 - L14: the same task linked twice in a batch is written once
  ---
  duration_ms: 1.436391
  ...
# Subtest: L15: a second toggle while one is in flight is swallowed as busy
ok 2301 - L15: a second toggle while one is in flight is swallowed as busy
  ---
  duration_ms: 6.219571
  ...
# Subtest: toggle on a non-link line refuses without writing
ok 2302 - toggle on a non-link line refuses without writing
  ---
  duration_ms: 0.490225
  ...
# Subtest: api.taskLinkLane is a frozen v1 namespace that never throws
ok 2303 - api.taskLinkLane is a frozen v1 namespace that never throws
  ---
  duration_ms: 1.621384
  ...
# Subtest: the progressMarks hint is a no-op without the ledger-tools api
ok 2304 - the progressMarks hint is a no-op without the ledger-tools api
  ---
  duration_ms: 0.473063
  ...
# Subtest: task move records one Vim jump and round-trips without extra writes
ok 2305 - task move records one Vim jump and round-trips without extra writes
  ---
  duration_ms: 10.916614
  ...
# Subtest: counted task move records a single jump to the first moved task
ok 2306 - counted task move records a single jump to the first moved task
  ---
  duration_ms: 1.859489
  ...
# Subtest: deferred task landing re-anchors and records the resolved cursor once
ok 2307 - deferred task landing re-anchors and records the resolved cursor once
  ---
  duration_ms: 5.10872
  ...
# Subtest: failed task move preserves seeded history including the forward branch
ok 2308 - failed task move preserves seeded history including the forward branch
  ---
  duration_ms: 0.569217
  ...
# Subtest: post-commit open failure keeps the move committed with no jump
ok 2309 - post-commit open failure keeps the move committed with no jump
  ---
  duration_ms: 1.083918
  ...
# Subtest: a newer move supersedes a pending landing without stale placement
ok 2310 - a newer move supersedes a pending landing without stale placement
  ---
  duration_ms: 10.656024
  ...
# Subtest: shared destination helper without a move context records no jump
ok 2311 - shared destination helper without a move context records no jump
  ---
  duration_ms: 0.736375
  ...
# Subtest: task moves carry the Depends-On line and repath stranded same-note links
ok 2312 - task moves carry the Depends-On line and repath stranded same-note links
  ---
  duration_ms: 7.775397
  ...
# Subtest: task moves keep pathless links when the target moves along
ok 2313 - task moves keep pathless links when the target moves along
  ---
  duration_ms: 1.181204
  ...
# Subtest: counted task moves discover movable tasks without wrapping or examples
ok 2314 - counted task moves discover movable tasks without wrapping or examples
  ---
  duration_ms: 1.159784
  ...
# Subtest: task move ranges preserve quoted subtrees and collapse overlapping selections
ok 2315 - task move ranges preserve quoted subtrees and collapse overlapping selections
  ---
  duration_ms: 0.666372
  ...
# Subtest: task move removal handles disjoint ranges, blank seams, and CRLF
ok 2316 - task move removal handles disjoint ranges, blank seams, and CRLF
  ---
  duration_ms: 0.442655
  ...
# Subtest: task move destinations include areas and only open projects
ok 2317 - task move destinations include areas and only open projects
  ---
  duration_ms: 0.663827
  ...
# Subtest: moves into a blocked project leave closed tagged lines alone
ok 2318 - moves into a blocked project leave closed tagged lines alone
  ---
  duration_ms: 2.561879
  ...
# Subtest: moves into a blocked project promote open prerequisites to the moved lane
ok 2319 - moves into a blocked project promote open prerequisites to the moved lane
  ---
  duration_ms: 2.832105
  ...
# Subtest: task move insertion preserves exact task and section spacing
ok 2320 - task move insertion preserves exact task and section spacing
  ---
  duration_ms: 2.899954
  ...
# Subtest: task move planning migrates identities and links across every affected note
ok 2321 - task move planning migrates identities and links across every affected note
  ---
  duration_ms: 4.385849
  ...
# Subtest: task move planning exposes a destination anchor for area destinations and counted moves
ok 2322 - task move planning exposes a destination anchor for area destinations and counted moves
  ---
  duration_ms: 0.820155
  ...
# Subtest: task move into a blocked project tags the moved task and consumes today's live Pomodoro link
ok 2323 - task move into a blocked project tags the moved task and consumes today's live Pomodoro link
  ---
  duration_ms: 3.242087
  ...
# Subtest: task move out of a blocked project recovers through the shared gate and writes the unblocked mark
ok 2324 - task move out of a blocked project recovers through the shared gate and writes the unblocked mark
  ---
  duration_ms: 3.398626
  ...
# Subtest: move promotion walks through a ^prj target without raising it
ok 2325 - move promotion walks through a ^prj target without raising it
  ---
  duration_ms: 2.165703
  ...
# Subtest: move promotion walks through a [?] ^prj to its open prerequisite
ok 2326 - move promotion walks through a [?] ^prj to its open prerequisite
  ---
  duration_ms: 0.920447
  ...
# Subtest: move promotion uses each open task's own lane, not the strongest moved lane
ok 2327 - move promotion uses each open task's own lane, not the strongest moved lane
  ---
  duration_ms: 1.182056
  ...
# Subtest: move promotion skips Depends-On lines of closed tasks
ok 2328 - move promotion skips Depends-On lines of closed tasks
  ---
  duration_ms: 0.763346
  ...
# Subtest: task move planning rejects destination collisions and malformed identities
ok 2329 - task move planning rejects destination collisions and malformed identities
  ---
  duration_ms: 0.561391
  ...
# Subtest: resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
ok 2330 - resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
  ---
  duration_ms: 0.633689
  ...
# Subtest: focusTaskMoveDestination opens the destination file and anchors the cursor
ok 2331 - focusTaskMoveDestination opens the destination file and anchors the cursor
  ---
  duration_ms: 1.078639
  ...
# Subtest: focusTaskMoveDestination returns false without moving the cursor when the open fails
ok 2332 - focusTaskMoveDestination returns false without moving the cursor when the open fails
  ---
  duration_ms: 0.24084
  ...
# Subtest: focusTaskMoveDestination re-anchors by block ID when the destination content drifted
ok 2333 - focusTaskMoveDestination re-anchors by block ID when the destination content drifted
  ---
  duration_ms: 0.244607
  ...
# Subtest: physical task move chord declines auto-repeat and consumes Vim normal input once
ok 2334 - physical task move chord declines auto-repeat and consumes Vim normal input once
  ---
  duration_ms: 0.818422
  ...
# Subtest: counted task move dispatch keeps its count through cold async destinations
ok 2335 - counted task move dispatch keeps its count through cold async destinations
  ---
  duration_ms: 15.94489
  ...
# Subtest: counted task move dispatch with warm async destinations opens one counted picker
ok 2336 - counted task move dispatch with warm async destinations opens one counted picker
  ---
  duration_ms: 5.939154
  ...
# Subtest: bare task move command ignores stale Vim count outside normal mode
ok 2337 - bare task move command ignores stale Vim count outside normal mode
  ---
  duration_ms: 1.402015
  ...
# Subtest: bare task move command opens one uncounted target in Vim normal mode
ok 2338 - bare task move command opens one uncounted target in Vim normal mode
  ---
  duration_ms: 0.499082
  ...
# Subtest: already handled task move event leaves pending Vim state alone
ok 2339 - already handled task move event leaves pending Vim state alone
  ---
  duration_ms: 0.199381
  ...
# Subtest: counted task move command dispatch counts Pomodoro sub-bullets once
ok 2340 - counted task move command dispatch counts Pomodoro sub-bullets once
  ---
  duration_ms: 3.900515
  ...
# Subtest: physical transclusion toggle owns bare and counted Vim normal input
ok 2341 - physical transclusion toggle owns bare and counted Vim normal input
  ---
  duration_ms: 2.43693
  ...
# Subtest: runtime task move writes destination before source and rolls back source failures
ok 2342 - runtime task move writes destination before source and rolls back source failures
  ---
  duration_ms: 3.439223
  ...
# Subtest: runtime task move groups open-editor source and destination changes
ok 2343 - runtime task move groups open-editor source and destination changes
  ---
  duration_ms: 2.228673
  ...
# Subtest: runtime task move guards destination, auxiliary, and rollback failures
ok 2344 - runtime task move guards destination, auxiliary, and rollback failures
  ---
  duration_ms: 2.49905
  ...
# Subtest: task move insertion separates the section's first task from preamble and placeholders
ok 2345 - task move insertion separates the section's first task from preamble and placeholders
  ---
  duration_ms: 0.520172
  ...
# Subtest: task move insertion keeps populated sections compact and second moves stable
ok 2346 - task move insertion keeps populated sections compact and second moves stable
  ---
  duration_ms: 0.253614
  ...
# Subtest: task move planning separates a counted move into a count-only section
ok 2347 - task move planning separates a counted move into a count-only section
  ---
  duration_ms: 0.485587
  ...
# Subtest: runtime counted move into a count-only section focuses the first moved task
ok 2348 - runtime counted move into a count-only section focuses the first moved task
  ---
  duration_ms: 1.347371
  ...
# Subtest: absent local key with folder template writes the trigger and one notice
ok 2349 - absent local key with folder template writes the trigger and one notice
  ---
  duration_ms: 2.401052
  ...
# Subtest: existing local object keeps other keys and only adds the trigger
ok 2350 - existing local object keeps other keys and only adds the trigger
  ---
  duration_ms: 0.336843
  ...
# Subtest: stored true is already-enabled with no write and no notice
ok 2351 - stored true is already-enabled with no write and no notice
  ---
  duration_ms: 0.326363
  ...
# Subtest: stored false is device-opt-out with no write and no notice
ok 2352 - stored false is device-opt-out with no write and no notice
  ---
  duration_ms: 0.206384
  ...
# Subtest: mode none and blank folder templates skip as no-creation-templates
ok 2353 - mode none and blank folder templates skip as no-creation-templates
  ---
  duration_ms: 0.353856
  ...
# Subtest: regex mode with a non-empty file template enables
ok 2354 - regex mode with a non-empty file template enables
  ---
  duration_ms: 0.242332
  ...
# Subtest: legacy settings without a mode key skip as legacy-templater
ok 2355 - legacy settings without a mode key skip as legacy-templater
  ---
  duration_ms: 0.243144
  ...
# Subtest: missing Templater plugin or settings skip as no-templater without throwing
ok 2356 - missing Templater plugin or settings skip as no-templater without throwing
  ---
  duration_ms: 0.358023
  ...
# Subtest: missing loadLocalStorage or saveLocalStorage returns without throwing
ok 2357 - missing loadLocalStorage or saveLocalStorage returns without throwing
  ---
  duration_ms: 0.449047
  ...
# Subtest: string or array stored local values skip as unknown-local-shape
ok 2358 - string or array stored local values skip as unknown-local-shape
  ---
  duration_ms: 0.556452
  ...
# Subtest: saveLocalStorage throw shows one failure notice and does not escape
ok 2359 - saveLocalStorage throw shows one failure notice and does not escape
  ---
  duration_ms: 0.296907
  ...
# Subtest: planTemplaterLocalTrigger covers helper cases and never adds extra keys
ok 2360 - planTemplaterLocalTrigger covers helper cases and never adds extra keys
  ---
  duration_ms: 0.269825
  ...
# Subtest: unblocked model returns null when there is nothing to show
ok 2361 - unblocked model returns null when there is nothing to show
  ---
  duration_ms: 1.429869
  ...
# Subtest: unblocked card renders a single linked row with receipt and chips
ok 2362 - unblocked card renders a single linked row with receipt and chips
  ---
  duration_ms: 1.643295
  ...
# Subtest: unblocked card renders several linked rows with one entry
ok 2363 - unblocked card renders several linked rows with one entry
  ---
  duration_ms: 0.317587
  ...
# Subtest: unblocked card renders a created continuation with next up
ok 2364 - unblocked card renders a created continuation with next up
  ---
  duration_ms: 0.39262
  ...
# Subtest: unblocked card renders recovered-only and still-blocked rows
ok 2365 - unblocked card renders recovered-only and still-blocked rows
  ---
  duration_ms: 0.726526
  ...
# Subtest: current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
ok 2366 - current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
  ---
  duration_ms: 0.897263
  ...
# Subtest: project pull-in rows label empty projects and preserve project blocking reasons
ok 2367 - project pull-in rows label empty projects and preserve project blocking reasons
  ---
  duration_ms: 0.951525
  ...
# Subtest: unblocked card caps visible rows with +N more
ok 2368 - unblocked card caps visible rows with +N more
  ---
  duration_ms: 0.319009
  ...
# Subtest: unblocked card renders the breaker variant
ok 2369 - unblocked card renders the breaker variant
  ---
  duration_ms: 0.525082
  ...
# Subtest: unblocked card renders the failure variant
ok 2370 - unblocked card renders the failure variant
  ---
  duration_ms: 0.480427
  ...
# Subtest: unblocked rows open their task without dismissing the notice
ok 2371 - unblocked rows open their task without dismissing the notice
  ---
  duration_ms: 1.094148
  ...
# Subtest: unblocked row without a block id opens the note path
ok 2372 - unblocked row without a block id opens the note path
  ---
  duration_ms: 0.265847
  ...
# Subtest: unblocked card omits the plan chip when daily content is null
ok 2373 - unblocked card omits the plan chip when daily content is null
  ---
  duration_ms: 0.229468
  ...
# Subtest: unblocked notice shows one card with duration through showNotice
ok 2374 - unblocked notice shows one card with duration through showNotice
  ---
  duration_ms: 0.296957
  ...
# Subtest: unblocked notice falls back to plain text without a DOM
ok 2375 - unblocked notice falls back to plain text without a DOM
  ---
  duration_ms: 0.160947
  ...
# Subtest: unblocked text truncates to 48 characters with an ellipsis
ok 2376 - unblocked text truncates to 48 characters with an ellipsis
  ---
  duration_ms: 0.13134
  ...
# Subtest: nav api exposes additive notice v1 and keeps version 3
ok 2377 - nav api exposes additive notice v1 and keeps version 3
  ---
  duration_ms: 0.445029
  ...
# Subtest: unblocked stylesheet scopes notice overrides and uses task tokens
ok 2378 - unblocked stylesheet scopes notice overrides and uses task tokens
  ---
  duration_ms: 0.542836
  ...
# Subtest: physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
ok 2379 - physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
  ---
  duration_ms: 3.417473
  ...
# Subtest: open-task command ids omit repeat so the shared route resolves the pending Vim count
ok 2380 - open-task command ids omit repeat so the shared route resolves the pending Vim count
  ---
  duration_ms: 2.106781
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
ok 2381 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
  ---
  duration_ms: 6.099038
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
ok 2382 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
  ---
  duration_ms: 0.852146
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
ok 2383 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
  ---
  duration_ms: 1.576839
  ...
# Subtest: dispatch guard applies a command-route Vim count when the capture route fires second
ok 2384 - dispatch guard applies a command-route Vim count when the capture route fires second
  ---
  duration_ms: 1.390965
  ...
# Subtest: dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
ok 2385 - dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
  ---
  duration_ms: 1.012653
  ...
# Subtest: command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
ok 2386 - command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
  ---
  duration_ms: 0.897483
  ...
# Subtest: command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
ok 2387 - command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
  ---
  duration_ms: 3.083404
  ...
# Subtest: command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
ok 2388 - command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
  ---
  duration_ms: 1.302035
  ...
# Subtest: explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
ok 2389 - explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
  ---
  duration_ms: 0.799285
  ...
# Subtest: getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
ok 2390 - getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
  ---
  duration_ms: 0.279163
  ...
# Subtest: physical counted property chord consumes only explicit normal-mode Vim counts
ok 2391 - physical counted property chord consumes only explicit normal-mode Vim counts
  ---
  duration_ms: 0.85886
  ...
# Subtest: physical counted relation and dependency chords route or refuse by direction
ok 2392 - physical counted relation and dependency chords route or refuse by direction
  ---
  duration_ms: 0.904076
  ...
# Subtest: onload registers the palette command without a default hotkey
ok 2393 - onload registers the palette command without a default hotkey
  ---
  duration_ms: 1.897141
  ...
# Subtest: an embed and a plain image link open the resolved vault resource
ok 2394 - an embed and a plain image link open the resolved vault resource
  ---
  duration_ms: 3.370392
  ...
# Subtest: no image, a missing image, and Reading view show notices without opening
ok 2395 - no image, a missing image, and Reading view show notices without opening
  ---
  duration_ms: 0.451812
  ...
# Subtest: a second command invocation is ignored while the viewer is open
ok 2396 - a second command invocation is ignored while the viewer is open
  ---
  duration_ms: 0.343856
  ...
# Subtest: closing restores focus and leaves an unchanged selection and scroll alone
ok 2397 - closing restores focus and leaves an unchanged selection and scroll alone
  ---
  duration_ms: 0.42418
  ...
# Subtest: closing restores moved selection and scroll only while the source view is active
ok 2398 - closing restores moved selection and scroll only while the source view is active
  ---
  duration_ms: 0.749801
  ...
# Subtest: unload closes the active viewer without restoring editor focus
ok 2399 - unload closes the active viewer without restoring editor focus
  ---
  duration_ms: 0.511746
  ...
# Subtest: parser finds vault embed with size hint
ok 2400 - parser finds vault embed with size hint
  ---
  duration_ms: 1.683262
  ...
# Subtest: parser finds plain image wikilink and blockquoted embed
ok 2401 - parser finds plain image wikilink and blockquoted embed
  ---
  duration_ms: 0.264975
  ...
# Subtest: parser ignores callout bracket and finds the embed
ok 2402 - parser ignores callout bracket and finds the embed
  ---
  duration_ms: 0.361139
  ...
# Subtest: parser ignores image links inside single and double backticks
ok 2403 - parser ignores image links inside single and double backticks
  ---
  duration_ms: 0.709895
  ...
# Subtest: non-image wiki targets are recognized but not candidates
ok 2404 - non-image wiki targets are recognized but not candidates
  ---
  duration_ms: 0.247702
  ...
# Subtest: parser finds two image refs and lines with no refs
ok 2405 - parser finds two image refs and lines with no refs
  ---
  duration_ms: 0.22557
  ...
# Subtest: parser handles Markdown angle, title, and balanced parens
ok 2406 - parser handles Markdown angle, title, and balanced parens
  ---
  duration_ms: 0.374876
  ...
# Subtest: picker uses containing, next, then previous rule
ok 2407 - picker uses containing, next, then previous rule
  ---
  duration_ms: 0.355518
  ...
# Subtest: resolution records sourcePath and resolves duplicate basenames
ok 2408 - resolution records sourcePath and resolves duplicate basenames
  ---
  duration_ms: 0.947258
  ...
# Subtest: resolution handles relative, unicode, and space names
ok 2409 - resolution handles relative, unicode, and space names
  ---
  duration_ms: 0.519091
  ...
# Subtest: missing file, non-image cursor, and fenced lines show exact notices
ok 2410 - missing file, non-image cursor, and fenced lines show exact notices
  ---
  duration_ms: 0.309741
  ...
# Subtest: vault resolution calls getResourcePath with the resolved file
ok 2411 - vault resolution calls getResourcePath with the resolved file
  ---
  duration_ms: 0.311615
  ...
# Subtest: http embed passes through and non-image urls are not candidates
ok 2412 - http embed passes through and non-image urls are not candidates
  ---
  duration_ms: 0.407989
  ...
# Subtest: remote URLs keep original bytes while titles decode once
ok 2413 - remote URLs keep original bytes while titles decode once
  ---
  duration_ms: 0.501648
  ...
# Subtest: escaped Markdown parentheses resolve to the unescaped vault file
ok 2414 - escaped Markdown parentheses resolve to the unescaped vault file
  ---
  duration_ms: 0.21509
  ...
# Subtest: vault percent escapes decode exactly once
ok 2415 - vault percent escapes decode exactly once
  ---
  duration_ms: 0.198028
  ...
# Subtest: extensionless http(s) needs Markdown image syntax
ok 2416 - extensionless http(s) needs Markdown image syntax
  ---
  duration_ms: 0.213828
  ...
# Subtest: fit never exceeds 1 and respects padding for landscape, portrait, and tiny images
ok 2417 - fit never exceeds 1 and respects padding for landscape, portrait, and tiny images
  ---
  duration_ms: 1.802089
  ...
# Subtest: min and max bounds follow fit, 1:1, and the max factor
ok 2418 - min and max bounds follow fit, 1:1, and the max factor
  ---
  duration_ms: 0.300413
  ...
# Subtest: stepping clamps at both bounds
ok 2419 - stepping clamps at both bounds
  ---
  duration_ms: 0.685459
  ...
# Subtest: zoom-at-point keeps the point fixed
ok 2420 - zoom-at-point keeps the point fixed
  ---
  duration_ms: 0.205732
  ...
# Subtest: clamp centres small axes and limits large ones
ok 2421 - clamp centres small axes and limits large ones
  ---
  duration_ms: 0.365227
  ...
# Subtest: key Escape → close
ok 2422 - key Escape → close
  ---
  duration_ms: 0.967988
  ...
# Subtest: key q → close
ok 2423 - key q → close
  ---
  duration_ms: 0.217716
  ...
# Subtest: key Q → close
ok 2424 - key Q → close
  ---
  duration_ms: 0.133324
  ...
# Subtest: key Ctrl+[ → close
ok 2425 - key Ctrl+[ → close
  ---
  duration_ms: 0.446552
  ...
# Subtest: key Z → close
ok 2426 - key Z → close
  ---
  duration_ms: 0.484375
  ...
# Subtest: key + → zoomIn
ok 2427 - key + → zoomIn
  ---
  duration_ms: 0.195994
  ...
# Subtest: key = → zoomIn
ok 2428 - key = → zoomIn
  ---
  duration_ms: 0.119238
  ...
# Subtest: key Shift+= → zoomIn
ok 2429 - key Shift+= → zoomIn
  ---
  duration_ms: 0.119899
  ...
# Subtest: key Shift++ → zoomIn
ok 2430 - key Shift++ → zoomIn
  ---
  duration_ms: 0.193921
  ...
# Subtest: key - → zoomOut
ok 2431 - key - → zoomOut
  ---
  duration_ms: 0.110622
  ...
# Subtest: key 0 → fit
ok 2432 - key 0 → fit
  ---
  duration_ms: 0.173041
  ...
# Subtest: key 1 → actual
ok 2433 - key 1 → actual
  ---
  duration_ms: 0.106073
  ...
# Subtest: key h → pan:left
ok 2434 - key h → pan:left
  ---
  duration_ms: 0.122294
  ...
# Subtest: key j → pan:down
ok 2435 - key j → pan:down
  ---
  duration_ms: 0.098708
  ...
# Subtest: key k → pan:up
ok 2436 - key k → pan:up
  ---
  duration_ms: 0.102665
  ...
# Subtest: key l → pan:right
ok 2437 - key l → pan:right
  ---
  duration_ms: 0.109549
  ...
# Subtest: key Shift+H → pan:left
ok 2438 - key Shift+H → pan:left
  ---
  duration_ms: 0.114649
  ...
# Subtest: key Shift+J → pan:down
ok 2439 - key Shift+J → pan:down
  ---
  duration_ms: 0.088098
  ...
# Subtest: key Shift+K → pan:up
ok 2440 - key Shift+K → pan:up
  ---
  duration_ms: 0.09933
  ...
# Subtest: key Shift+L → pan:right
ok 2441 - key Shift+L → pan:right
  ---
  duration_ms: 0.098639
  ...
# Subtest: key ArrowLeft → pan:left
ok 2442 - key ArrowLeft → pan:left
  ---
  duration_ms: 0.093739
  ...
# Subtest: key ArrowDown → pan:down
ok 2443 - key ArrowDown → pan:down
  ---
  duration_ms: 0.103137
  ...
# Subtest: key ArrowUp → pan:up
ok 2444 - key ArrowUp → pan:up
  ---
  duration_ms: 0.095512
  ...
# Subtest: key ArrowRight → pan:right
ok 2445 - key ArrowRight → pan:right
  ---
  duration_ms: 0.095152
  ...
# Subtest: key Shift+ArrowLeft → pan:left
ok 2446 - key Shift+ArrowLeft → pan:left
  ---
  duration_ms: 0.205102
  ...
# Subtest: key Ctrl+q → ignore
ok 2447 - key Ctrl+q → ignore
  ---
  duration_ms: 0.125129
  ...
# Subtest: key Meta+z → ignore
ok 2448 - key Meta+z → ignore
  ---
  duration_ms: 0.114168
  ...
# Subtest: key Meta+Z → ignore
ok 2449 - key Meta+Z → ignore
  ---
  duration_ms: 0.188339
  ...
# Subtest: key a composing → ignore
ok 2450 - key a composing → ignore
  ---
  duration_ms: 0.100031
  ...
# Subtest: key a keyCode 229 → ignore
ok 2451 - key a keyCode 229 → ignore
  ---
  duration_ms: 0.095412
  ...
# Subtest: key x → ignore
ok 2452 - key x → ignore
  ---
  duration_ms: 0.089972
  ...
# Subtest: keys before arming are ignored
ok 2453 - keys before arming are ignored
  ---
  duration_ms: 1.804274
  ...
# Subtest: Z closes after arming, and a repeated Z does not
ok 2454 - Z closes after arming, and a repeated Z does not
  ---
  duration_ms: 0.615976
  ...
# Subtest: load sets fit state and dimensions
ok 2455 - load sets fit state and dimensions
  ---
  duration_ms: 0.647596
  ...
# Subtest: a load error shows a notice, closes, and calls onClosed once
ok 2456 - a load error shows a notice, closes, and calls onClosed once
  ---
  duration_ms: 0.390325
  ...
# Subtest: Escape closes once, unregisters the scope handler, and aborts the signal
ok 2457 - Escape closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.31457
  ...
# Subtest: q closes once, unregisters the scope handler, and aborts the signal
ok 2458 - q closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.320041
  ...
# Subtest: Q closes once, unregisters the scope handler, and aborts the signal
ok 2459 - Q closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.266819
  ...
# Subtest: Ctrl+[ closes once, unregisters the scope handler, and aborts the signal
ok 2460 - Ctrl+[ closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.349737
  ...
# Subtest: Z closes once, unregisters the scope handler, and aborts the signal
ok 2461 - Z closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.378622
  ...
# Subtest: a stray x key changes nothing
ok 2462 - a stray x key changes nothing
  ---
  duration_ms: 0.363694
  ...
# Subtest: the app's vault stubs throw and are never called
ok 2463 - the app's vault stubs throw and are never called
  ---
  duration_ms: 0.302177
  ...
# Subtest: task-card-gate arms only on open inbox tasks
ok 2464 - task-card-gate arms only on open inbox tasks
  ---
  duration_ms: 3.510851
  ...
# Subtest: task-card-gate header shows the Inbox chip only when armed
ok 2465 - task-card-gate header shows the Inbox chip only when armed
  ---
  duration_ms: 6.351952
  ...
# Subtest: task-card-gate priority: cancel writes nothing
ok 2466 - task-card-gate priority: cancel writes nothing
  ---
  duration_ms: 1.138914
  ...
# Subtest: task-card-gate priority: stay runs today's write
ok 2467 - task-card-gate priority: stay runs today's write
  ---
  duration_ms: 0.254566
  ...
# Subtest: task-card-gate priority: move writes then moves
ok 2468 - task-card-gate priority: move writes then moves
  ---
  duration_ms: 0.520173
  ...
# Subtest: task-card-gate scheduled: cancel writes nothing
ok 2469 - task-card-gate scheduled: cancel writes nothing
  ---
  duration_ms: 0.166748
  ...
# Subtest: task-card-gate scheduled: stay runs today's write
ok 2470 - task-card-gate scheduled: stay runs today's write
  ---
  duration_ms: 0.14659
  ...
# Subtest: task-card-gate scheduled: move writes then moves
ok 2471 - task-card-gate scheduled: move writes then moves
  ---
  duration_ms: 0.171768
  ...
# Subtest: task-card-gate generic-property: cancel writes nothing
ok 2472 - task-card-gate generic-property: cancel writes nothing
  ---
  duration_ms: 0.361821
  ...
# Subtest: task-card-gate generic-property: stay runs today's write
ok 2473 - task-card-gate generic-property: stay runs today's write
  ---
  duration_ms: 0.42451
  ...
# Subtest: task-card-gate generic-property: move writes then moves
ok 2474 - task-card-gate generic-property: move writes then moves
  ---
  duration_ms: 0.315712
  ...
# Subtest: task-card-gate refresh-interval: cancel writes nothing
ok 2475 - task-card-gate refresh-interval: cancel writes nothing
  ---
  duration_ms: 0.170506
  ...
# Subtest: task-card-gate refresh-interval: stay runs today's write
ok 2476 - task-card-gate refresh-interval: stay runs today's write
  ---
  duration_ms: 0.130218
  ...
# Subtest: task-card-gate refresh-interval: move writes then moves
ok 2477 - task-card-gate refresh-interval: move writes then moves
  ---
  duration_ms: 0.142291
  ...
# Subtest: task-card-gate refresh-custom: cancel writes nothing
ok 2478 - task-card-gate refresh-custom: cancel writes nothing
  ---
  duration_ms: 0.108437
  ...
# Subtest: task-card-gate refresh-custom: stay runs today's write
ok 2479 - task-card-gate refresh-custom: stay runs today's write
  ---
  duration_ms: 0.101574
  ...
# Subtest: task-card-gate refresh-custom: move writes then moves
ok 2480 - task-card-gate refresh-custom: move writes then moves
  ---
  duration_ms: 0.344949
  ...
# Subtest: task-card-gate clear-priority: cancel writes nothing
ok 2481 - task-card-gate clear-priority: cancel writes nothing
  ---
  duration_ms: 0.16237
  ...
# Subtest: task-card-gate clear-priority: stay runs today's write
ok 2482 - task-card-gate clear-priority: stay runs today's write
  ---
  duration_ms: 0.131521
  ...
# Subtest: task-card-gate clear-priority: move writes then moves
ok 2483 - task-card-gate clear-priority: move writes then moves
  ---
  duration_ms: 0.156359
  ...
# Subtest: task-card-gate recommended-roll: cancel writes nothing
ok 2484 - task-card-gate recommended-roll: cancel writes nothing
  ---
  duration_ms: 0.105131
  ...
# Subtest: task-card-gate recommended-roll: stay runs today's write
ok 2485 - task-card-gate recommended-roll: stay runs today's write
  ---
  duration_ms: 0.112405
  ...
# Subtest: task-card-gate recommended-roll: move writes then moves
ok 2486 - task-card-gate recommended-roll: move writes then moves
  ---
  duration_ms: 0.140528
  ...
# Subtest: task-card-gate recommended-decay: cancel writes nothing
ok 2487 - task-card-gate recommended-decay: cancel writes nothing
  ---
  duration_ms: 0.107044
  ...
# Subtest: task-card-gate recommended-decay: stay runs today's write
ok 2488 - task-card-gate recommended-decay: stay runs today's write
  ---
  duration_ms: 0.099811
  ...
# Subtest: task-card-gate recommended-decay: move writes then moves
ok 2489 - task-card-gate recommended-decay: move writes then moves
  ---
  duration_ms: 0.133745
  ...
# Subtest: task-card-gate counted-roll: cancel writes nothing
ok 2490 - task-card-gate counted-roll: cancel writes nothing
  ---
  duration_ms: 0.186857
  ...
# Subtest: task-card-gate counted-roll: stay runs today's write
ok 2491 - task-card-gate counted-roll: stay runs today's write
  ---
  duration_ms: 0.122083
  ...
# Subtest: task-card-gate counted-roll: move writes then moves
ok 2492 - task-card-gate counted-roll: move writes then moves
  ---
  duration_ms: 0.233616
  ...
# Subtest: task-card-gate lane-toggle: cancel writes nothing
ok 2493 - task-card-gate lane-toggle: cancel writes nothing
  ---
  duration_ms: 0.129076
  ...
# Subtest: task-card-gate lane-toggle: stay runs today's write
ok 2494 - task-card-gate lane-toggle: stay runs today's write
  ---
  duration_ms: 0.117234
  ...
# Subtest: task-card-gate lane-toggle: move writes then moves
ok 2495 - task-card-gate lane-toggle: move writes then moves
  ---
  duration_ms: 0.217966
  ...
# Subtest: task-card-gate dependency-single: cancel writes nothing
ok 2496 - task-card-gate dependency-single: cancel writes nothing
  ---
  duration_ms: 0.107645
  ...
# Subtest: task-card-gate dependency-single: stay runs today's write
ok 2497 - task-card-gate dependency-single: stay runs today's write
  ---
  duration_ms: 0.100943
  ...
# Subtest: task-card-gate dependency-single: move writes then moves
ok 2498 - task-card-gate dependency-single: move writes then moves
  ---
  duration_ms: 0.42984
  ...
# Subtest: task-card-gate dependency-marked: cancel writes nothing
ok 2499 - task-card-gate dependency-marked: cancel writes nothing
  ---
  duration_ms: 0.110161
  ...
# Subtest: task-card-gate dependency-marked: stay runs today's write
ok 2500 - task-card-gate dependency-marked: stay runs today's write
  ---
  duration_ms: 0.107475
  ...
# Subtest: task-card-gate dependency-marked: move writes then moves
ok 2501 - task-card-gate dependency-marked: move writes then moves
  ---
  duration_ms: 0.140088
  ...
# Subtest: task-card-gate dependency-vault: cancel writes nothing
ok 2502 - task-card-gate dependency-vault: cancel writes nothing
  ---
  duration_ms: 0.105491
  ...
# Subtest: task-card-gate dependency-vault: stay runs today's write
ok 2503 - task-card-gate dependency-vault: stay runs today's write
  ---
  duration_ms: 0.095142
  ...
# Subtest: task-card-gate dependency-vault: move writes then moves
ok 2504 - task-card-gate dependency-vault: move writes then moves
  ---
  duration_ms: 0.112335
  ...
# Subtest: task-card-gate dependency-counted: cancel writes nothing
ok 2505 - task-card-gate dependency-counted: cancel writes nothing
  ---
  duration_ms: 0.101083
  ...
# Subtest: task-card-gate dependency-counted: stay runs today's write
ok 2506 - task-card-gate dependency-counted: stay runs today's write
  ---
  duration_ms: 0.095271
  ...
# Subtest: task-card-gate dependency-counted: move writes then moves
ok 2507 - task-card-gate dependency-counted: move writes then moves
  ---
  duration_ms: 0.12596
  ...
# Subtest: task-card-gate negative rows never prompt
ok 2508 - task-card-gate negative rows never prompt
  ---
  duration_ms: 0.718781
  ...
# Subtest: task-card-gate counted sessions capture N targets
ok 2509 - task-card-gate counted sessions capture N targets
  ---
  duration_ms: 1.953147
  ...
# Subtest: task-card-gate walk: move advances once with Moved first
ok 2510 - task-card-gate walk: move advances once with Moved first
  ---
  duration_ms: 0.307907
  ...
# Subtest: task-card-gate walk: move failure falls back to card with partial
ok 2511 - task-card-gate walk: move failure falls back to card with partial
  ---
  duration_ms: 0.428769
  ...
# Subtest: task-card-gate walk: exactly one settle per origin
ok 2512 - task-card-gate walk: exactly one settle per origin
  ---
  duration_ms: 25.773075
  ...
# Subtest: task-card-gate route outcome resolves like lane and link-today
ok 2513 - task-card-gate route outcome resolves like lane and link-today
  ---
  duration_ms: 0.312597
  ...
# Subtest: inbox classifier covers the inbox contract
ok 2514 - inbox classifier covers the inbox contract
  ---
  duration_ms: 2.090269
  ...
# Subtest: isInboxNotePath matches the inbox contract through the vault
ok 2515 - isInboxNotePath matches the inbox contract through the vault
  ---
  duration_ms: 1.336971
  ...
# Subtest: isInboxNotePath is false without an inbox note and never throws
ok 2516 - isInboxNotePath is false without an inbox note and never throws
  ---
  duration_ms: 0.182829
  ...
# Subtest: route destinations drop every inbox note, the source, and templates
ok 2517 - route destinations drop every inbox note, the source, and templates
  ---
  duration_ms: 0.805728
  ...
# Subtest: route preflight accepts a live area destination
ok 2518 - route preflight accepts a live area destination
  ---
  duration_ms: 4.054628
  ...
# Subtest: route preflight refuses stale and colliding destinations
ok 2519 - route preflight refuses stale and colliding destinations
  ---
  duration_ms: 1.590786
  ...
# Subtest: route picker resolves move, stay, cancel, and close exactly once
ok 2520 - route picker resolves move, stay, cancel, and close exactly once
  ---
  duration_ms: 3.57904
  ...
# Subtest: route picker footer names the move, the hatch, and the way back
ok 2521 - route picker footer names the move, the hatch, and the way back
  ---
  duration_ms: 0.508321
  ...
# Subtest: route picker preflight refusal keeps the picker open with a notice
ok 2522 - route picker preflight refusal keeps the picker open with a notice
  ---
  duration_ms: 12.055106
  ...
# Subtest: route picker honors the shared move-picker guard
ok 2523 - route picker honors the shared move-picker guard
  ---
  duration_ms: 3.097922
  ...
# Subtest: promptInboxRoute moves, stays, and cancels with suspend pairing
ok 2524 - promptInboxRoute moves, stays, and cancels with suspend pairing
  ---
  duration_ms: 3.519507
  ...
# Subtest: commitInboxRoute moves the verified task with its children
ok 2525 - commitInboxRoute moves the verified task with its children
  ---
  duration_ms: 4.38565
  ...
# Subtest: commitInboxRoute into a blocked project tags the moved task
ok 2526 - commitInboxRoute into a blocked project tags the moved task
  ---
  duration_ms: 2.413696
  ...
# Subtest: commitInboxRoute moves a counted run and refuses on identity drift
ok 2527 - commitInboxRoute moves a counted run and refuses on identity drift
  ---
  duration_ms: 1.709603
  ...
# Subtest: reviewOutcomeResolves treats route like lane and link-today
ok 2528 - reviewOutcomeResolves treats route like lane and link-today
  ---
  duration_ms: 0.318147
  ...
# Subtest: nav api inboxRoute v1 delegates, shapes, and never throws
ok 2529 - nav api inboxRoute v1 delegates, shapes, and never throws
  ---
  duration_ms: 1.687831
  ...
# Subtest: history records ordered locations with file identity and dedupes adjacent repeats
ok 2530 - history records ordered locations with file identity and dedupes adjacent repeats
  ---
  duration_ms: 1.550058
  ...
# Subtest: transition records origin then destination and truncates forward only on success
ok 2531 - transition records origin then destination and truncates forward only on success
  ---
  duration_ms: 0.926328
  ...
# Subtest: history retains at most 100 locations and refreshes the live tip
ok 2532 - history retains at most 100 locations and refreshes the live tip
  ---
  duration_ms: 0.666612
  ...
# Subtest: rename updates paths and delete prunes without corrupting the index
ok 2533 - rename updates paths and delete prunes without corrupting the index
  ---
  duration_ms: 0.258664
  ...
# Subtest: bridge wraps add once, mirrors native jumps, and preserves the original call
ok 2534 - bridge wraps add once, mirrors native jumps, and preserves the original call
  ---
  duration_ms: 1.533036
  ...
# Subtest: bridge without a jump list preserves keys and emits one compatibility diagnostic
ok 2535 - bridge without a jump list preserves keys and emits one compatibility diagnostic
  ---
  duration_ms: 0.299752
  ...
# Subtest: registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
ok 2536 - registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
  ---
  duration_ms: 0.375958
  ...
# Subtest: Enter A->B round-trips with Ctrl+O and Ctrl+I
ok 2537 - Enter A->B round-trips with Ctrl+O and Ctrl+I
  ---
  duration_ms: 22.645797
  ...
# Subtest: counted Enter returns to the original cursor, not the counted link line
ok 2538 - counted Enter returns to the original cursor, not the counted link line
  ---
  duration_ms: 22.001207
  ...
# Subtest: picker choice records one jump and cancellation records none
ok 2539 - picker choice records one jump and cancellation records none
  ---
  duration_ms: 22.640047
  ...
# Subtest: stale picker origin is rejected and failed opens record nothing
ok 2540 - stale picker origin is rejected and failed opens record nothing
  ---
  duration_ms: 21.879585
  ...
# Subtest: Backspace shares the link path and no-link lines fall through
ok 2541 - Backspace shares the link path and no-link lines fall through
  ---
  duration_ms: 22.193724
  ...
# Subtest: counted traversal honors boundaries and new jumps replace the forward branch
ok 2542 - counted traversal honors boundaries and new jumps replace the forward branch
  ---
  duration_ms: 1.000399
  ...
# Subtest: ordinary motion before back is preserved for forward restore
ok 2543 - ordinary motion before back is preserved for forward restore
  ---
  duration_ms: 0.427365
  ...
# Subtest: deleted entries are skipped and heading links settle before recording
ok 2544 - deleted entries are skipped and heading links settle before recording
  ---
  duration_ms: 21.550596
  ...
# Subtest: native fallback runs with empty history and boundaries never replay natives
ok 2545 - native fallback runs with empty history and boundaries never replay natives
  ---
  duration_ms: 0.790098
  ...
# Subtest: unload restores the native add and keeps a foreign later mapping
ok 2546 - unload restores the native add and keeps a foreign later mapping
  ---
  duration_ms: 0.49258
  ...
# Subtest: exact eligibility authorizes one due-Ready ROTTEN row
ok 2547 - exact eligibility authorizes one due-Ready ROTTEN row
  ---
  duration_ms: 1.440008
  ...
# Subtest: exact eligibility authorizes a TICKLER row
ok 2548 - exact eligibility authorizes a TICKLER row
  ---
  duration_ms: 0.199782
  ...
# Subtest: exact eligibility refuses every stale-cache shape
ok 2549 - exact eligibility refuses every stale-cache shape
  ---
  duration_ms: 0.466441
  ...
# Subtest: exact eligibility refuses non-Ready and non-due rows
ok 2550 - exact eligibility refuses non-Ready and non-due rows
  ---
  duration_ms: 0.28284
  ...
# Subtest: legacy refs still match line-only while exact refuses
ok 2551 - legacy refs still match line-only while exact refuses
  ---
  duration_ms: 0.62875
  ...
# Subtest: keeps support needs namespace v5 with keepLine
ok 2552 - keeps support needs namespace v5 with keepLine
  ---
  duration_ms: 0.157461
  ...
# Subtest: decay decisions need namespace v6 with keepLine
ok 2553 - decay decisions need namespace v6 with keepLine
  ---
  duration_ms: 0.214559
  ...
# Subtest: batch forwards per-target counted decisions to the stamper
ok 2554 - batch forwards per-target counted decisions to the stamper
  ---
  duration_ms: 0.722568
  ...
# Subtest: batch keeps legacy index targets uncounted
ok 2555 - batch keeps legacy index targets uncounted
  ---
  duration_ms: 0.370467
  ...
# Subtest: a throwing stamper refuses the batch with no partial write
ok 2556 - a throwing stamper refuses the batch with no partial write
  ---
  duration_ms: 0.46609
  ...
# Subtest: parseKeepsCount reads the first valid value only
ok 2557 - parseKeepsCount reads the first valid value only
  ---
  duration_ms: 0.31421
  ...
# Subtest: countFreshStampKept measures actual increments only
ok 2558 - countFreshStampKept measures actual increments only
  ---
  duration_ms: 0.184803
  ...
# Subtest: fresh stamp notice tails kept increments without promises
ok 2559 - fresh stamp notice tails kept increments without promises
  ---
  duration_ms: 0.231201
  ...
# Subtest: duplicate source targets dedupe to one write
ok 2560 - duplicate source targets dedupe to one write
  ---
  duration_ms: 0.170445
  ...
# Subtest: single Alt+F increments an exact due-Ready ROTTEN task
ok 2561 - single Alt+F increments an exact due-Ready ROTTEN task
  ---
  duration_ms: 6.944613
  ...
# Subtest: single Alt+F preserves NEW, lane, and early tasks without counting
ok 2562 - single Alt+F preserves NEW, lane, and early tasks without counting
  ---
  duration_ms: 2.256306
  ...
# Subtest: same-day repeat stays identical and counts nothing
ok 2563 - same-day repeat stays identical and counts nothing
  ---
  duration_ms: 0.506226
  ...
# Subtest: Pending Alt+F writes its summary with the stamp in one edit
ok 2564 - Pending Alt+F writes its summary with the stamp in one edit
  ---
  duration_ms: 0.989308
  ...
# Subtest: counted Pending refresh shares one summary only with Pending targets
ok 2565 - counted Pending refresh shares one summary only with Pending targets
  ---
  duration_ms: 0.905859
  ...
# Subtest: a refusing counted target refuses before the Pending Work Log prompt
ok 2566 - a refusing counted target refuses before the Pending Work Log prompt
  ---
  duration_ms: 0.330792
  ...
# Subtest: blank Pending refresh advances; cancelled or stale prompts write nothing
ok 2567 - blank Pending refresh advances; cancelled or stale prompts write nothing
  ---
  duration_ms: 1.450618
  ...
# Subtest: stale queue match stamps uncounted and never inflates
ok 2568 - stale queue match stamps uncounted and never inflates
  ---
  duration_ms: 0.555811
  ...
# Subtest: counted Alt+F increments every exact target once
ok 2569 - counted Alt+F increments every exact target once
  ---
  duration_ms: 1.846814
  ...
# Subtest: stale editor source refuses with no write
ok 2570 - stale editor source refuses with no write
  ---
  duration_ms: 0.379243
  ...
# Subtest: single-note write lands in one editor transaction and keeps CRLF
ok 2571 - single-note write lands in one editor transaction and keeps CRLF
  ---
  duration_ms: 0.663276
  ...
# Subtest: v5 without keepLine fails without writing
ok 2572 - v5 without keepLine fails without writing
  ---
  duration_ms: 0.163662
  ...
# Subtest: throwing v5 keepLine refuses the batch with no partial write
ok 2573 - throwing v5 keepLine refuses the batch with no partial write
  ---
  duration_ms: 0.36642
  ...
# Subtest: pre-v5 ledger stamps uncounted through the old stamper
ok 2574 - pre-v5 ledger stamps uncounted through the old stamper
  ---
  duration_ms: 0.451312
  ...
# Subtest: Task Link session skips an at-limit decide target
ok 2575 - Task Link session skips an at-limit decide target
  ---
  duration_ms: 2.254683
  ...
# Subtest: Task Link refresh counts one exact target
ok 2576 - Task Link refresh counts one exact target
  ---
  duration_ms: 1.357961
  ...
# Subtest: duplicate Task Links to one target stamp and count once
ok 2577 - duplicate Task Links to one target stamp and count once
  ---
  duration_ms: 0.760421
  ...
# Subtest: counted Task Link sessions combine Pending work and Rotten keep logs
ok 2578 - counted Task Link sessions combine Pending work and Rotten keep logs
  ---
  duration_ms: 1.401966
  ...
# Subtest: counted Task Links dedupe targets and log only the Pending target
ok 2579 - counted Task Links dedupe targets and log only the Pending target
  ---
  duration_ms: 1.010148
  ...
# Subtest: multi-note stale preimage refuses with no writes
ok 2580 - multi-note stale preimage refuses with no writes
  ---
  duration_ms: 0.897793
  ...
# Subtest: a linked note changed during the Keep prompt refuses before any write
ok 2581 - a linked note changed during the Keep prompt refuses before any write
  ---
  duration_ms: 0.587711
  ...
# Subtest: multi-note write failure rolls back the first note
ok 2582 - multi-note write failure rolls back the first note
  ---
  duration_ms: 1.815845
  ...
# Subtest: partial rollback is reported and a same-day retry does not duplicate the logged keep
ok 2583 - partial rollback is reported and a same-day retry does not duplicate the logged keep
  ---
  duration_ms: 2.57761
  ...
# Subtest: one physical key through two routes stamps once
ok 2584 - one physical key through two routes stamps once
  ---
  duration_ms: 1.469544
  ...
# Subtest: Ctrl+Alt+F capture advances once and consumes a Vim prefix
ok 2585 - Ctrl+Alt+F capture advances once and consumes a Vim prefix
  ---
  duration_ms: 0.77002
  ...
# Subtest: obsolete and extra-modifier F chords stay unconsumed
ok 2586 - obsolete and extra-modifier F chords stay unconsumed
  ---
  duration_ms: 0.256639
  ...
# Subtest: live Ctrl+Alt+F double dispatch asks once on a Pending task
ok 2587 - live Ctrl+Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.606888
  ...
# Subtest: live Alt+F double dispatch asks once on a Pending task
ok 2588 - live Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.472772
  ...
# Subtest: already-handled refresh keydown leaves Vim state alone
ok 2589 - already-handled refresh keydown leaves Vim state alone
  ---
  duration_ms: 0.179322
  ...
# Subtest: parseBobOpenNotesParams accepts indexed entries and ignores unknown keys
ok 2590 - parseBobOpenNotesParams accepts indexed entries and ignores unknown keys
  ---
  duration_ms: 2.636843
  ...
# Subtest: parseBobOpenNotesParams rejects every malformed URI field
ok 2591 - parseBobOpenNotesParams rejects every malformed URI field
  ---
  duration_ms: 0.652456
  ...
# Subtest: invalid batches show one notice and open nothing
ok 2592 - invalid batches show one notice and open nothing
  ---
  duration_ms: 1.654377
  ...
# Subtest: path mapping follows a symlink realpath into the vault
ok 2593 - path mapping follows a symlink realpath into the vault
  ---
  duration_ms: 4.935959
  ...
# Subtest: new-tab policy reuses existing tabs and the active empty tab, keeping order and primary active
ok 2594 - new-tab policy reuses existing tabs and the active empty tab, keeping order and primary active
  ---
  duration_ms: 2.403656
  ...
# Subtest: an absent or outside entry fails independently and a PDF opens without landing
ok 2595 - an absent or outside entry fails independently and a PDF opens without landing
  ---
  duration_ms: 2001.596787
  ...
# Subtest: a resolved note that is not open waits until its captured digest is cached
ok 2596 - a resolved note that is not open waits until its captured digest is cached
  ---
  duration_ms: 65.45224
  ...
# Subtest: a per-entry open failure does not prevent later notes from opening
ok 2597 - a per-entry open failure does not prevent later notes from opening
  ---
  duration_ms: 1.299851
  ...
# Subtest: waits for a newly created vault file and a late visible line digest
ok 2598 - waits for a newly created vault file and a late visible line digest
  ---
  duration_ms: 61.358887
  ...
# Subtest: re-finds a moved digest on any line, including prose and Pomodoro rows
ok 2599 - re-finds a moved digest on any line, including prose and Pomodoro rows
  ---
  duration_ms: 1.67649
  ...
# Subtest: deadline fallback opens near the planned line and reports a changed capture
ok 2600 - deadline fallback opens near the planned line and reports a changed capture
  ---
  duration_ms: 2001.066505
  ...
# Subtest: truncation reports how many of the full list opened
ok 2601 - truncation reports how many of the full list opened
  ---
  duration_ms: 0.847387
  ...
# Subtest: serializes quick URLs and leaves the later URL active
ok 2602 - serializes quick URLs and leaves the later URL active
  ---
  duration_ms: 5.60221
  ...
# Subtest: primary landing flashes briefly, secondary landings do not, and the handler is read-only
ok 2603 - primary landing flashes briefly, secondary landings do not, and the handler is read-only
  ---
  duration_ms: 15.999184
  ...
# Subtest: onload registers bob-open-notes beside bob-goto-task
ok 2604 - onload registers bob-open-notes beside bob-goto-task
  ---
  duration_ms: 1.878294
  ...
# Subtest: a non-file sidebar view is not reused as an empty tab
ok 2605 - a non-file sidebar view is not reused as an empty tab
  ---
  duration_ms: 0.62354
  ...
# Subtest: a true empty tab is reused for the first entry
ok 2606 - a true empty tab is reused for the first entry
  ---
  duration_ms: 0.375637
  ...
# Subtest: three new tabs follow entry order in the tab strip
ok 2607 - three new tabs follow entry order in the tab strip
  ---
  duration_ms: 0.715966
  ...
# Subtest: two tabs of the same note reuse the first matching leaf
ok 2608 - two tabs of the same note reuse the first matching leaf
  ---
  duration_ms: 0.380646
  ...
# Subtest: a missing file does not scan vault lists when getAbstractFileByPath exists
ok 2609 - a missing file does not scan vault lists when getAbstractFileByPath exists
  ---
  duration_ms: 2000.958388
  ...
# Subtest: new tabs append at the far right when the middle tab is active
ok 2610 - new tabs append at the far right when the middle tab is active
  ---
  duration_ms: 0.651473
  ...
# Subtest: a reused tab stays put while a new one is appended
ok 2611 - a reused tab stays put while a new one is appended
  ---
  duration_ms: 0.317687
  ...
# Subtest: a deferred tab is reused and findMarkdownLeafByPath sees it
ok 2612 - a deferred tab is reused and findMarkdownLeafByPath sees it
  ---
  duration_ms: 0.444288
  ...
# Subtest: a deferred sidebar leaf whose saved state names the note is not reused
ok 2613 - a deferred sidebar leaf whose saved state names the note is not reused
  ---
  duration_ms: 0.230389
  ...
# Subtest: a loaded main-area match beats an earlier loaded sidebar match
ok 2614 - a loaded main-area match beats an earlier loaded sidebar match
  ---
  duration_ms: 0.214188
  ...
# Subtest: a new tab goes to the end of the main group when a sidebar leaf is active
ok 2615 - a new tab goes to the end of the main group when a sidebar leaf is active
  ---
  duration_ms: 0.22499
  ...
# Subtest: falling back without createLeafInParent still opens a new tab
ok 2616 - falling back without createLeafInParent still opens a new tab
  ---
  duration_ms: 0.227604
  ...
# Subtest: falling back when createLeafInParent throws still opens a new tab
ok 2617 - falling back when createLeafInParent throws still opens a new tab
  ---
  duration_ms: 0.233415
  ...
# Subtest: collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
ok 2618 - collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
  ---
  duration_ms: 6.617079
  ...
# Subtest: getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
ok 2619 - getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
  ---
  duration_ms: 2.366326
  ...
# Subtest: getProjectBlockState reports an open external prerequisite
ok 2620 - getProjectBlockState reports an open external prerequisite
  ---
  duration_ms: 0.597791
  ...
# Subtest: getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
ok 2621 - getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
  ---
  duration_ms: 0.576881
  ...
# Subtest: getProjectBlockState scheduledValue override is the inline date, not frontmatter
ok 2622 - getProjectBlockState scheduledValue override is the inline date, not frontmatter
  ---
  duration_ms: 0.407267
  ...
# Subtest: getProjectBlockState skips internal and archive Depends-On links
ok 2623 - getProjectBlockState skips internal and archive Depends-On links
  ---
  duration_ms: 0.315252
  ...
# Subtest: getProjectBlockState is a no-op for terminal, daily, and non-project notes
ok 2624 - getProjectBlockState is a no-op for terminal, daily, and non-project notes
  ---
  duration_ms: 0.603381
  ...
# Subtest: projectLooksBlockedByPrjShortcut is the single [?] ^prj row
ok 2625 - projectLooksBlockedByPrjShortcut is the single [?] ^prj row
  ---
  duration_ms: 0.263102
  ...
# Subtest: taskHasProjectBlockedTag is token-bounded and does not match \#prj
ok 2626 - taskHasProjectBlockedTag is token-bounded and does not match \#prj
  ---
  duration_ms: 0.325301
  ...
# Subtest: setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
ok 2627 - setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
  ---
  duration_ms: 0.796942
  ...
# Subtest: reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
ok 2628 - reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
  ---
  duration_ms: 0.506687
  ...
# Subtest: reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
ok 2629 - reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
  ---
  duration_ms: 0.350859
  ...
# Subtest: reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
ok 2630 - reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
  ---
  duration_ms: 0.197006
  ...
# Subtest: ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
ok 2631 - ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
  ---
  duration_ms: 5.821119
  ...
# Subtest: recovery gate keeps a resident of a blocked project blocked after own deps close
ok 2632 - recovery gate keeps a resident of a blocked project blocked after own deps close
  ---
  duration_ms: 2.436369
  ...
# Subtest: recovery gate blocks residents on a future inline project date with no deps
ok 2633 - recovery gate blocks residents on a future inline project date with no deps
  ---
  duration_ms: 0.478403
  ...
# Subtest: planDeferredPomodoroLinkCleanup always deletes a last-child open entry
ok 2634 - planDeferredPomodoroLinkCleanup always deletes a last-child open entry
  ---
  duration_ms: 1.777823
  ...
# Subtest: TICKLER notice uses unblocked <date> when returnedBy is unblocked
ok 2635 - TICKLER notice uses unblocked <date> when returnedBy is unblocked
  ---
  duration_ms: 0.454518
  ...
# Subtest: recognition: a `^prj` parent in a project note carries its residents
ok 2636 - recognition: a `^prj` parent in a project note carries its residents
  ---
  duration_ms: 4.123859
  ...
# Subtest: recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
ok 2637 - recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
  ---
  duration_ms: 0.636234
  ...
# Subtest: add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
ok 2638 - add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
  ---
  duration_ms: 7.248013
  ...
# Subtest: add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
ok 2639 - add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
  ---
  duration_ms: 3.903358
  ...
# Subtest: guards: a same-note add to `^prj` refuses, including mixed batches
ok 2640 - guards: a same-note add to `^prj` refuses, including mixed batches
  ---
  duration_ms: 1.07951
  ...
# Subtest: guards: the stage disables same-note rows for `^prj` with `inside this project`
ok 2641 - guards: the stage disables same-note rows for `^prj` with `inside this project`
  ---
  duration_ms: 1.500995
  ...
# Subtest: guards: cycle detection includes the implicit resident edges (§13.6)
ok 2642 - guards: cycle detection includes the implicit resident edges (§13.6)
  ---
  duration_ms: 1.76598
  ...
# Subtest: removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
ok 2643 - removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
  ---
  duration_ms: 4.860074
  ...
# Subtest: removal: a resident with its own reason stays `[?]` without the tag (PDB3)
ok 2644 - removal: a resident with its own reason stays `[?]` without the tag (PDB3)
  ---
  duration_ms: 2.071283
  ...
# Subtest: removal without a registry defers to reconcile: residents keep `[?]` and the tag
ok 2645 - removal without a registry defers to reconcile: residents keep `[?]` and the tag
  ---
  duration_ms: 1.683853
  ...
# Subtest: writer: one gesture commits `^prj` and its residents in a single undo group
ok 2646 - writer: one gesture commits `^prj` and its residents in a single undo group
  ---
  duration_ms: 1.301224
  ...
# Subtest: writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
ok 2647 - writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
  ---
  duration_ms: 5.955165
  ...
# Subtest: notices: the project strings name the task, the flips, and the Pomodoro cleanup
ok 2648 - notices: the project strings name the task, the flips, and the Pomodoro cleanup
  ---
  duration_ms: 0.405354
  ...
# Subtest: mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
ok 2649 - mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
  ---
  duration_ms: 0.289412
  ...
# Subtest: api v3: removeDependencyByRef delegates removals to the single-transaction writer
ok 2650 - api v3: removeDependencyByRef delegates removals to the single-transaction writer
  ---
  duration_ms: 1.024314
  ...
# Subtest: api v3: openDependencyStageForRef opens the Depends on stage on the owning task
ok 2651 - api v3: openDependencyStageForRef opens the Depends on stage on the owning task
  ---
  duration_ms: 0.381818
  ...
# Subtest: internal links stay on the line but leave the field (PDR7)
ok 2652 - internal links stay on the line but leave the field (PDR7)
  ---
  duration_ms: 1.02208
  ...
# Subtest: removal from an unblocked ^prj never recovers own-reason residents (§13.10)
ok 2653 - removal from an unblocked ^prj never recovers own-reason residents (§13.10)
  ---
  duration_ms: 0.62318
  ...
# Subtest: resident recovery touches only tagged residents (§13.10)
ok 2654 - resident recovery touches only tagged residents (§13.10)
  ---
  duration_ms: 1.429609
  ...
# Subtest: stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
ok 2655 - stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
  ---
  duration_ms: 1.119226
  ...
# Subtest: projectDependentResidentKeys lists open residents with block ids
ok 2656 - projectDependentResidentKeys lists open residents with block ids
  ---
  duration_ms: 0.400054
  ...
# Subtest: navNoteScopeFlags marks daily notes; a missing writer stays null
ok 2657 - navNoteScopeFlags marks daily notes; a missing writer stays null
  ---
  duration_ms: 0.332014
  ...
# Subtest: reconcileBlockedScheduledTaskLine forwards scope flags to the writer
ok 2658 - reconcileBlockedScheduledTaskLine forwards scope flags to the writer
  ---
  duration_ms: 0.194471
  ...
# Subtest: parseProjectNoteFrontmatter ignores leftover scheduled keys
ok 2659 - parseProjectNoteFrontmatter ignores leftover scheduled keys
  ---
  duration_ms: 0.666262
  ...
# Subtest: formatTaskMoveProjectCountsNotice names blocked and recovered counts
ok 2660 - formatTaskMoveProjectCountsNotice names blocked and recovered counts
  ---
  duration_ms: 0.192217
  ...
# Subtest: PDS15: projectParentTarget keeps the path and drops alias and heading
ok 2661 - PDS15: projectParentTarget keeps the path and drops alias and heading
  ---
  duration_ms: 1.529308
  ...
# Subtest: PDS6: list-form, missing, and non-wikilink parents yield none
ok 2662 - PDS6: list-form, missing, and non-wikilink parents yield none
  ---
  duration_ms: 0.617388
  ...
# Subtest: PDS15: resolveProjectParentPath accepts alias, path, and heading forms
ok 2663 - PDS15: resolveProjectParentPath accepts alias, path, and heading forms
  ---
  duration_ms: 0.528329
  ...
# Subtest: PDS6: self, unresolved, and ambiguous basenames yield no parent
ok 2664 - PDS6: self, unresolved, and ambiguous basenames yield no parent
  ---
  duration_ms: 0.213898
  ...
# Subtest: buildProjectChildrenMap and descendants BFS skip cycles and cap depth
ok 2665 - buildProjectChildrenMap and descendants BFS skip cycles and cap depth
  ---
  duration_ms: 3.636249
  ...
# Subtest: PDS6: area, terminal, daily, and self-parent notes are not children
ok 2666 - PDS6: area, terminal, daily, and self-parent notes are not children
  ---
  duration_ms: 0.563665
  ...
# Subtest: PDG8: planner blocks child and grandchild ^prj and residents
ok 2667 - PDG8: planner blocks child and grandchild ^prj and residents
  ---
  duration_ms: 3.539857
  ...
# Subtest: PDG9: planner recovers tagged descendants with [unblocked::]
ok 2668 - PDG9: planner recovers tagged descendants with [unblocked::]
  ---
  duration_ms: 1.847305
  ...
# Subtest: PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
ok 2669 - PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
  ---
  duration_ms: 2.391844
  ...
# Subtest: PDG11: a tagged root re-asserts descendant tags and recovers nothing
ok 2670 - PDG11: a tagged root re-asserts descendant tags and recovers nothing
  ---
  duration_ms: 1.085882
  ...
# Subtest: tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
ok 2671 - tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
  ---
  duration_ms: 0.316293
  ...
# Subtest: tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
ok 2672 - tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
  ---
  duration_ms: 2.010646
  ...
# Subtest: tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
ok 2673 - tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
  ---
  duration_ms: 0.200493
  ...
# Subtest: tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
ok 2674 - tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
  ---
  duration_ms: 2.321271
  ...
# Subtest: PDG13: failProjectPrjInternalAdd refuses descendant targets
ok 2675 - PDG13: failProjectPrjInternalAdd refuses descendant targets
  ---
  duration_ms: 0.323438
  ...
# Subtest: PDG13: planDependencyEdit refuses a descendant add from the files map
ok 2676 - PDG13: planDependencyEdit refuses a descendant add from the files map
  ---
  duration_ms: 1.715504
  ...
# Subtest: PDG13: the stage disables descendant rows
ok 2677 - PDG13: the stage disables descendant rows
  ---
  duration_ms: 1.555398
  ...
# Subtest: reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
ok 2678 - reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
  ---
  duration_ms: 0.425813
  ...
# Subtest: tag proxy: removing the last own dep of a tagged ^prj recovers nobody
ok 2679 - tag proxy: removing the last own dep of a tagged ^prj recovers nobody
  ---
  duration_ms: 7.817699
  ...
# Subtest: PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
ok 2680 - PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
  ---
  duration_ms: 34.404007
  ...
# Subtest: PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
ok 2681 - PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
  ---
  duration_ms: 8.939009
  ...
# Subtest: PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
ok 2682 - PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
  ---
  duration_ms: 6.459977
  ...
# Subtest: PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
ok 2683 - PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
  ---
  duration_ms: 4.150732
  ...
# Subtest: PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
ok 2684 - PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
  ---
  duration_ms: 5.089543
  ...
# Subtest: PDG12: moving the project date due recovers descendants
ok 2685 - PDG12: moving the project date due recovers descendants
  ---
  duration_ms: 3.735689
  ...
# Subtest: PDG12: deleting the project date recovers descendants
ok 2686 - PDG12: deleting the project date recovers descendants
  ---
  duration_ms: 4.507362
  ...
# Subtest: PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
ok 2687 - PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
  ---
  duration_ms: 5.582392
  ...
# Subtest: PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
ok 2688 - PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
  ---
  duration_ms: 4.572206
  ...
# Subtest: Task Link Depends on writer preserves the internal-target guard on a project task
ok 2689 - Task Link Depends on writer preserves the internal-target guard on a project task
  ---
  duration_ms: 1.285773
  ...
# Subtest: api v3 removeDependencyByRef runs the recovery cascade for a linked project task
ok 2690 - api v3 removeDependencyByRef runs the recovery cascade for a linked project task
  ---
  duration_ms: 4.119892
  ...
# Subtest: counted Schedule writer cascades a future date through descendants
ok 2691 - counted Schedule writer cascades a future date through descendants
  ---
  duration_ms: 5.356914
  ...
# Subtest: counted subtree roots are ancestor-first and each descendant note is planned once
ok 2692 - counted subtree roots are ancestor-first and each descendant note is planned once
  ---
  duration_ms: 3.517704
  ...
# Subtest: Ctrl+D on the Depends on row removes the line and recovers the subtree
ok 2693 - Ctrl+D on the Depends on row removes the line and recovers the subtree
  ---
  duration_ms: 4.121736
  ...
# Subtest: a ^prj with no children reads no other note
ok 2694 - a ^prj with no children reads no other note
  ---
  duration_ms: 0.225731
  ...
# Subtest: single seeds from raw text, not display decorations
ok 2695 - single seeds from raw text, not display decorations
  ---
  duration_ms: 13.757285
  ...
# Subtest: legacy valid free wins; invalid and taken fall through
ok 2696 - legacy valid free wins; invalid and taken fall through
  ---
  duration_ms: 2.256446
  ...
# Subtest: batch reserves suffixes for two same-text tasks
ok 2697 - batch reserves suffixes for two same-text tasks
  ---
  duration_ms: 1.308376
  ...
# Subtest: counted-source, vault-single, and vault-counted seed per mode
ok 2698 - counted-source, vault-single, and vault-counted seed per mode
  ---
  duration_ms: 1.54603
  ...
# Subtest: cross-note uses the target note, never the dependent fallback
ok 2699 - cross-note uses the target note, never the dependent fallback
  ---
  duration_ms: 1.534859
  ...
# Subtest: staging writes nothing until confirmed
ok 2700 - staging writes nothing until confirmed
  ---
  duration_ms: 0.848209
  ...
# Subtest: the shared planner matches the Task Card recommendation
ok 2701 - the shared planner matches the Task Card recommendation
  ---
  duration_ms: 29.445794
  ...
# Subtest: the preview table strings are exact
ok 2702 - the preview table strings are exact
  ---
  duration_ms: 1.535841
  ...
# Subtest: checklist tiers and unpreviewable rows report ok:false
ok 2703 - checklist tiers and unpreviewable rows report ok:false
  ---
  duration_ms: 0.51364
  ...
# Subtest: a silent config failure reports ok:false with no Notice
ok 2704 - a silent config failure reports ok:false with no Notice
  ---
  duration_ms: 0.191556
  ...
# Subtest: landing toasts append the preview after tails
ok 2705 - landing toasts append the preview after tails
  ---
  duration_ms: 1.299951
  ...
# Subtest: api.quickRoll has the v1 shape and never throws
ok 2706 - api.quickRoll has the v1 shape and never throws
  ---
  duration_ms: 1.988925
  ...
# Subtest: the preview matches what Alt+P then writes
ok 2707 - the preview matches what Alt+P then writes
  ---
  duration_ms: 24.299223
  ...
# Subtest: Alt+P matches Ctrl+Enter for roll, decay, project, and counted task writes
ok 2708 - Alt+P matches Ctrl+Enter for roll, decay, project, and counted task writes
  ---
  duration_ms: 53.555835
  ...
# Subtest: Alt+P matches Ctrl+Enter for a counted Task Link batch
ok 2709 - Alt+P matches Ctrl+Enter for a counted Task Link batch
  ---
  duration_ms: 12.714504
  ...
# Subtest: Task Link resolution keeps the outer modal hidden until its targets are ready
ok 2710 - Task Link resolution keeps the outer modal hidden until its targets are ready
  ---
  duration_ms: 3.611213
  ...
# Subtest: Alt+P hides immediate rolls and reveals the optional Next Work summary
ok 2711 - Alt+P hides immediate rolls and reveals the optional Next Work summary
  ---
  duration_ms: 15.867261
  ...
# Subtest: a cancel recommendation waits for the visible card and the second Alt+P cancels
ok 2712 - a cancel recommendation waits for the visible card and the second Alt+P cancels
  ---
  duration_ms: 6.25176
  ...
# Subtest: no priority and unavailable recurring tasks reveal the card without writing
ok 2713 - no priority and unavailable recurring tasks reveal the card without writing
  ---
  duration_ms: 2.587659
  ...
# Subtest: inbox routing is shown before the write and a managed line redirects to its owner
ok 2714 - inbox routing is shown before the write and a managed line redirects to its owner
  ---
  duration_ms: 7.047729
  ...
# Subtest: a landed review row advances once after Alt+P writes
ok 2715 - a landed review row advances once after Alt+P writes
  ---
  duration_ms: 4.084225
  ...
# Subtest: the card alias uses the physical Alt+P code and ignores repeats
ok 2716 - the card alias uses the physical Alt+P code and ignores repeats
  ---
  duration_ms: 2.013042
  ...
# Subtest: a throwing one-shot dispatch always reveals the still-open card
ok 2717 - a throwing one-shot dispatch always reveals the still-open card
  ---
  duration_ms: 3.089545
  ...
# Subtest: the registered command owns Alt+P and a Vim count is consumed once
ok 2718 - the registered command owns Alt+P and a Vim count is consumed once
  ---
  duration_ms: 2.527894
  ...
# Subtest: quick-roll visibility CSS disables the modal entrance animation
ok 2719 - quick-roll visibility CSS disables the modal entrance animation
  ---
  duration_ms: 0.70198
  ...
# Subtest: Less often picker renders actual rows from 90 days and Escape writes nothing
ok 2720 - Less often picker renders actual rows from 90 days and Escape writes nothing
  ---
  duration_ms: 6.001082
  ...
# Subtest: Less often picker renders actual rows from 120 days and Escape writes nothing
ok 2721 - Less often picker renders actual rows from 120 days and Escape writes nothing
  ---
  duration_ms: 0.781662
  ...
# Subtest: Less often picker renders actual rows from 180 days and Escape writes nothing
ok 2722 - Less often picker renders actual rows from 180 days and Escape writes nothing
  ---
  duration_ms: 0.497339
  ...
# Subtest: renderFooter skips malformed hints and retains valid structured hints
ok 2723 - renderFooter skips malformed hints and retains valid structured hints
  ---
  duration_ms: 0.285815
  ...
# Subtest: Pending refresh modal previews the dated Work Log and confirms once
ok 2724 - Pending refresh modal previews the dated Work Log and confirms once
  ---
  duration_ms: 1.447834
  ...
# Subtest: dismissing the Pending refresh modal cancels without a summary
ok 2725 - dismissing the Pending refresh modal cancels without a summary
  ---
  duration_ms: 0.297848
  ...
# Subtest: nav LK1–LK18 parse relation grammar and reject the other relation parser
ok 2726 - nav LK1–LK18 parse relation grammar and reject the other relation parser
  ---
  duration_ms: 2.836793
  ...
# Subtest: nav LK14–LK19 context and cross-parse rules
ok 2727 - nav LK14–LK19 context and cross-parse rules
  ---
  duration_ms: 0.6078
  ...
# Subtest: nav MC5 refuses relation embeds and MC16 keeps LINKS while dropping LINKED FROM
ok 2728 - nav MC5 refuses relation embeds and MC16 keeps LINKS while dropping LINKED FROM
  ---
  duration_ms: 1.428486
  ...
# Subtest: nav MC15 hands LINKS edits to the relation mirror and notices generated lines once
ok 2729 - nav MC15 hands LINKS edits to the relation mirror and notices generated lines once
  ---
  duration_ms: 3.89294
  ...
# Subtest: LG3: typed relation labels commit their text through the relation field
    # Subtest: add writes the typed label and mirror
    ok 1 - add writes the typed label and mirror
      ---
      duration_ms: 11.77458
      ...
    # Subtest: typed text is normalized before commit
    ok 2 - typed text is normalized before commit
      ---
      duration_ms: 1.787541
      ...
    # Subtest: relabel replaces an existing label and its mirror
    ok 3 - relabel replaces an existing label and its mirror
      ---
      duration_ms: 5.671845
      ...
    # Subtest: Linked from labels the other task's LINKS line
    ok 4 - Linked from labels the other task's LINKS line
      ---
      duration_ms: 1.478331
      ...
    # Subtest: suggestion, plain, and raw-input paths remain supported
    ok 5 - suggestion, plain, and raw-input paths remain supported
      ---
      duration_ms: 2.455716
      ...
    1..5
ok 2730 - LG3: typed relation labels commit their text through the relation field
  ---
  duration_ms: 24.719845
  ...
# Subtest: links-to row follows blocks with N, first label, cut target, and +K
ok 2731 - links-to row follows blocks with N, first label, cut target, and +K
  ---
  duration_ms: 7.011752
  ...
# Subtest: links-to row stays available on closed tasks and empty LINKS lines
ok 2732 - links-to row stays available on closed tasks and empty LINKS lines
  ---
  duration_ms: 1.883194
  ...
# Subtest: links-to row refuses non-tasks and read-only notes
ok 2733 - links-to row refuses non-tasks and read-only notes
  ---
  duration_ms: 1.180623
  ...
# Subtest: card keycap l opens Links to; input focus keeps it quiet
ok 2734 - card keycap l opens Links to; input focus keeps it quiet
  ---
  duration_ms: 1.061095
  ...
# Subtest: card ⇧L shows live incoming detail and routes Ctrl+D by direction
ok 2735 - card ⇧L shows live incoming detail and routes Ctrl+D by direction
  ---
  duration_ms: 2.092193
  ...
# Subtest: index-only Linked-from rows convert 1-based edges into nav records
ok 2736 - index-only Linked-from rows convert 1-based edges into nav records
  ---
  duration_ms: 0.431935
  ...
# Subtest: card ⇧L detail cleans a raw index task line
ok 2737 - card ⇧L detail cleans a raw index task line
  ---
  duration_ms: 0.667725
  ...
# Subtest: Linked-from scans source LINKS, reverses built-in phrases, and ignores stored mirrors
ok 2738 - Linked-from scans source LINKS, reverses built-in phrases, and ignores stored mirrors
  ---
  duration_ms: 2.338063
  ...
# Subtest: LG7: reverse-stage Enter writes the source's LINKS and target mirror
ok 2739 - LG7: reverse-stage Enter writes the source's LINKS and target mirror
  ---
  duration_ms: 1.13154
  ...
# Subtest: LG12: counted Links to applies the chosen labelled target to every source
ok 2740 - LG12: counted Links to applies the chosen labelled target to every source
  ---
  duration_ms: 1.675276
  ...
# Subtest: LG8: Ctrl+Shift+P on a LINKS line resolves to the owner's stage
ok 2741 - LG8: Ctrl+Shift+P on a LINKS line resolves to the owner's stage
  ---
  duration_ms: 0.685368
  ...
# Subtest: pool keeps closed tasks and done/ archives, drops dailies and templates
ok 2742 - pool keeps closed tasks and done/ archives, drops dailies and templates
  ---
  duration_ms: 0.449447
  ...
# Subtest: stage lists CURRENT in authored order, then RESULTS, then CLOSED
ok 2743 - stage lists CURRENT in authored order, then RESULTS, then CLOSED
  ---
  duration_ms: 2.004425
  ...
# Subtest: LG4: missing CURRENT targets stay removable; malformed lines refuse
ok 2744 - LG4: missing CURRENT targets stay removable; malformed lines refuse
  ---
  duration_ms: 0.477852
  ...
# Subtest: prerequisite targets badge; id-less rows prompt
ok 2745 - prerequisite targets badge; id-less rows prompt
  ---
  duration_ms: 1.744058
  ...
# Subtest: subtitle, consequence strip, live sentence, and label refusal copy
ok 2746 - subtitle, consequence strip, live sentence, and label refusal copy
  ---
  duration_ms: 0.394543
  ...
# Subtest: LG15: marked rows plan one commit with adds and unlinks split
ok 2747 - LG15: marked rows plan one commit with adds and unlinks split
  ---
  duration_ms: 0.207366
  ...
# Subtest: LG1: stage link writes LINKS, mirror, and mint in one transaction
ok 2748 - LG1: stage link writes LINKS, mirror, and mint in one transaction
  ---
  duration_ms: 1.035797
  ...
# Subtest: LG2: cross-note mirror follows; a changed target suffixes the notice
ok 2749 - LG2: cross-note mirror follows; a changed target suffixes the notice
  ---
  duration_ms: 0.921489
  ...
# Subtest: LG4: CURRENT unlink removes the entry and its mirror entry
ok 2750 - LG4: CURRENT unlink removes the entry and its mirror entry
  ---
  duration_ms: 0.931998
  ...
# Subtest: LG6: archived targets link with the live-only suffix and no mirror
ok 2751 - LG6: archived targets link with the live-only suffix and no mirror
  ---
  duration_ms: 0.409551
  ...
# Subtest: LG13: linking never stamps, routes, or touches Depends-On lines
ok 2752 - LG13: linking never stamps, routes, or touches Depends-On lines
  ---
  duration_ms: 0.965002
  ...
# Subtest: LG15: two targets link in one gesture with one notice
ok 2753 - LG15: two targets link in one gesture with one notice
  ---
  duration_ms: 0.547585
  ...
# Subtest: LG5: id-less targets refuse at the writer, so the stage prompts first
ok 2754 - LG5: id-less targets refuse at the writer, so the stage prompts first
  ---
  duration_ms: 0.242262
  ...
# Subtest: LG7: Ctrl+Shift+P resolves LINKED FROM to its owner's reverse stage
ok 2755 - LG7: Ctrl+Shift+P resolves LINKED FROM to its owner's reverse stage
  ---
  duration_ms: 0.157801
  ...
# Subtest: api.relations openStage opens both directions at v1
ok 2756 - api.relations openStage opens both directions at v1
  ---
  duration_ms: 0.421865
  ...
# relations.linked_from_lines is invalid; treating as true
# Subtest: LW1 inserts an unlabelled LINKS line in the empty slot
ok 2757 - LW1 inserts an unlabelled LINKS line in the empty slot
  ---
  duration_ms: 3.986437
  ...
# Subtest: LW2 appends a labelled entry and LW3 is a byte-identical no-op
ok 2758 - LW2 appends a labelled entry and LW3 is a byte-identical no-op
  ---
  duration_ms: 2.014796
  ...
# Subtest: LW4 relabels in place and LW5/LW6 remove entries
ok 2759 - LW4 relabels in place and LW5/LW6 remove entries
  ---
  duration_ms: 1.223104
  ...
# Subtest: LW7 places LINKS after Sub-projects and LINKED FROM after LINKS
ok 2760 - LW7 places LINKS after Sub-projects and LINKED FROM after LINKS
  ---
  duration_ms: 2.53135
  ...
# Subtest: LW8 inserts LINKS as the first child when only user children exist
ok 2761 - LW8 inserts LINKS as the first child when only user children exist
  ---
  duration_ms: 0.631024
  ...
# Subtest: LW9 merges duplicate LINKS lines with first label winning
ok 2762 - LW9 merges duplicate LINKS lines with first label winning
  ---
  duration_ms: 0.579586
  ...
# Subtest: LW10 refuses a malformed LINKS line
ok 2763 - LW10 refuses a malformed LINKS line
  ---
  duration_ms: 0.319409
  ...
# Subtest: LW11 normalises and refuses labels
ok 2764 - LW11 normalises and refuses labels
  ---
  duration_ms: 0.864139
  ...
# Subtest: LW12 reuses a 4-space child indent
ok 2765 - LW12 reuses a 4-space child indent
  ---
  duration_ms: 0.470367
  ...
# Subtest: LW13 canonical link forms match Rust
ok 2766 - LW13 canonical link forms match Rust
  ---
  duration_ms: 1.024324
  ...
# Subtest: LW14 / LK20 LINKED FROM sort is byte-identical to Rust
ok 2767 - LW14 / LK20 LINKED FROM sort is byte-identical to Rust
  ---
  duration_ms: 0.588123
  ...
# Subtest: Rule 6 LINKED FROM planner table
ok 2768 - Rule 6 LINKED FROM planner table
  ---
  duration_ms: 1.675809
  ...
# Subtest: linkedFromDesiredAfterDelta keeps labels and sorts
ok 2769 - linkedFromDesiredAfterDelta keeps labels and sorts
  ---
  duration_ms: 0.517738
  ...
# Subtest: LG14 kill switch defaults on, honors false, and invalid values fall back on
ok 2770 - LG14 kill switch defaults on, honors false, and invalid values fall back on
  ---
  duration_ms: 1.580627
  ...
# Subtest: LG1 same-note add mints and writes LINKS plus LINKED FROM in one transaction
ok 2771 - LG1 same-note add mints and writes LINKS plus LINKED FROM in one transaction
  ---
  duration_ms: 6.169463
  ...
# Subtest: LG2 cross-note T follows the source commit; a changed target suffixes the notice
ok 2772 - LG2 cross-note T follows the source commit; a changed target suffixes the notice
  ---
  duration_ms: 2.59354
  ...
# Subtest: LG4 unlinks and relabels in place with the mirror
ok 2773 - LG4 unlinks and relabels in place with the mirror
  ---
  duration_ms: 3.461556
  ...
# Subtest: LG6 archived targets write LINKS without a mirror
ok 2774 - LG6 archived targets write LINKS without a mirror
  ---
  duration_ms: 0.860973
  ...
# Subtest: LG13 relation writes never stamp or change status
ok 2775 - LG13 relation writes never stamp or change status
  ---
  duration_ms: 0.746625
  ...
# Subtest: LG14 kill switch writes LINKS without a mirror or source mint
ok 2776 - LG14 kill switch writes LINKS without a mirror or source mint
  ---
  duration_ms: 0.362542
  ...
# Subtest: api.relations v1: removeLink works and openStage settles false without a plugin
ok 2777 - api.relations v1: removeLink works and openStage settles false without a plugin
  ---
  duration_ms: 2.207472
  ...
# Subtest: createDependencyNavApi mounts relations beside blocks
ok 2778 - createDependencyNavApi mounts relations beside blocks
  ---
  duration_ms: 0.629221
  ...
# Subtest: LG10: hand-edited LINKS mirrors to LINKED FROM and re-fires after undo
ok 2779 - LG10: hand-edited LINKS mirrors to LINKED FROM and re-fires after undo
  ---
  duration_ms: 5.172131
  ...
# Subtest: LG11: hand-editing generated LINKED FROM only shows its notice
ok 2780 - LG11: hand-editing generated LINKED FROM only shows its notice
  ---
  duration_ms: 0.637497
  ...
# Subtest: LG9: Ctrl+D's writer clears outgoing links and their generated mirrors
ok 2781 - LG9: Ctrl+D's writer clears outgoing links and their generated mirrors
  ---
  duration_ms: 2.382356
  ...
# Subtest: Alt+N release from a NEXT landing advances with one composed toast
ok 2782 - Alt+N release from a NEXT landing advances with one composed toast
  ---
  duration_ms: 31.746333
  ...
# Subtest: counted Alt+N lands past every handled key in one jump
ok 2783 - counted Alt+N lands past every handled key in one jump
  ---
  duration_ms: 12.812622
  ...
# Subtest: a cancelled Alt+N release prompt stays and frees the lock
ok 2784 - a cancelled Alt+N release prompt stays and frees the lock
  ---
  duration_ms: 11.316135
  ...
# Subtest: Alt+N on a checklist landing stays with the plain notice
ok 2785 - Alt+N on a checklist landing stays with the plain notice
  ---
  duration_ms: 9.896727
  ...
# Subtest: Alt+N off a landing behaves exactly as today
ok 2786 - Alt+N off a landing behaves exactly as today
  ---
  duration_ms: 11.980243
  ...
# Subtest: Alt+N while the gesture lock is held is swallowed
ok 2787 - Alt+N while the gesture lock is held is swallowed
  ---
  duration_ms: 10.455313
  ...
# Subtest: a Task Card priority commit on NEXT advances, landing after the rich card
ok 2788 - a Task Card priority commit on NEXT advances, landing after the rich card
  ---
  duration_ms: 34.638745
  ...
# Subtest: dismissing the Task Card stays and frees the lock
ok 2789 - dismissing the Task Card stays and frees the lock
  ---
  duration_ms: 13.240177
  ...
# Subtest: a frontmatter-only project edit from the card stays
ok 2790 - a frontmatter-only project edit from the card stays
  ---
  duration_ms: 12.674768
  ...
# Subtest: a same-day priority schedule on a checklist row stays
ok 2791 - a same-day priority schedule on a checklist row stays
  ---
  duration_ms: 12.438248
  ...
# Subtest: a future schedule on a checklist row advances
ok 2792 - a future schedule on a checklist row advances
  ---
  duration_ms: 19.369395
  ...
# Subtest: a Task Card cancel on a checklist row advances with the cancel card first
ok 2793 - a Task Card cancel on a checklist row advances with the cancel card first
  ---
  duration_ms: 15.094937
  ...
# Subtest: Ctrl+Shift+M from a landing follows the task and never advances
ok 2794 - Ctrl+Shift+M from a landing follows the task and never advances
  ---
  duration_ms: 14.698821
  ...
# Subtest: Ctrl+Shift+M from a checklist landing keeps the destination focus
ok 2795 - Ctrl+Shift+M from a checklist landing keeps the destination focus
  ---
  duration_ms: 10.995123
  ...
# Subtest: ]s after a landed move resumes at the successor despite the line shift
ok 2796 - ]s after a landed move resumes at the successor despite the line shift
  ---
  duration_ms: 34.073045
  ...
# Subtest: [s after a landed move resumes at the predecessor
ok 2797 - [s after a landed move resumes at the predecessor
  ---
  duration_ms: 11.74257
  ...
# Subtest: a counted move from a landing resumes past every moved target
ok 2798 - a counted move from a landing resumes past every moved target
  ---
  duration_ms: 10.512171
  ...
# Subtest: counted Ctrl+Shift+M command dispatch preserves a landed move count
ok 2799 - counted Ctrl+Shift+M command dispatch preserves a landed move count
  ---
  duration_ms: 22.3747
  ...
# Subtest: a stale landing is not parked
ok 2800 - a stale landing is not parked
  ---
  duration_ms: 11.234851
  ...
# Subtest: Ctrl+Shift+M while the gesture lock is held is swallowed
ok 2801 - Ctrl+Shift+M while the gesture lock is held is swallowed
  ---
  duration_ms: 0.853078
  ...
# Subtest: dismissing the move picker stays and frees the lock
ok 2802 - dismissing the move picker stays and frees the lock
  ---
  duration_ms: 10.473879
  ...
# Subtest: Ctrl+Shift+M off a landing behaves exactly as today
ok 2803 - Ctrl+Shift+M off a landing behaves exactly as today
  ---
  duration_ms: 10.249139
  ...
# Subtest: answer, move, answer stays in queue order past an accumulator alias
ok 2804 - answer, move, answer stays in queue order past an accumulator alias
  ---
  duration_ms: 4.262394
  ...
# Subtest: a move park ignores a stale accumulator alias
ok 2805 - a move park ignores a stale accumulator alias
  ---
  duration_ms: 0.583463
  ...
# Subtest: a re-indexed origin still advances from the landed row
ok 2806 - a re-indexed origin still advances from the landed row
  ---
  duration_ms: 2.044903
  ...
# Subtest: a landed move park clears the current review task
ok 2807 - a landed move park clears the current review task
  ---
  duration_ms: 0.417617
  ...
# Subtest: predicate: reviewOutcomeResolves across tiers and kinds
ok 2808 - predicate: reviewOutcomeResolves across tiers and kinds
  ---
  duration_ms: 2.775687
  ...
# Subtest: findReviewResumeIndex identifies rows by path and text
ok 2809 - findReviewResumeIndex identifies rows by path and text
  ---
  duration_ms: 0.575869
  ...
# Subtest: buildReviewMoveAnchor parks text-identified resume neighbours
ok 2810 - buildReviewMoveAnchor parks text-identified resume neighbours
  ---
  duration_ms: 1.084139
  ...
# Subtest: planReviewJump with a move anchor resumes at the walk neighbour
ok 2811 - planReviewJump with a move anchor resumes at the walk neighbour
  ---
  duration_ms: 1.902652
  ...
# Subtest: capture: null off a landing
ok 2812 - capture: null off a landing
  ---
  duration_ms: 8.313696
  ...
# Subtest: capture: frozen origin shape, BUSY while locked, expiry
ok 2813 - capture: frozen origin shape, BUSY while locked, expiry
  ---
  duration_ms: 1.15284
  ...
# Subtest: successor picker keeps a captured completion locked through selection and one walk toast
ok 2814 - successor picker keeps a captured completion locked through selection and one walk toast
  ---
  duration_ms: 23.713675
  ...
# Subtest: continue: refuses stale origins, showing the notice once
ok 2815 - continue: refuses stale origins, showing the notice once
  ---
  duration_ms: 8.161276
  ...
# Subtest: continue: stays on null and non-resolving outcomes
ok 2816 - continue: stays on null and non-resolving outcomes
  ---
  duration_ms: 2.246637
  ...
# Subtest: continue: stays for lane answers and mixed-version completes on checklist rows
ok 2817 - continue: stays for lane answers and mixed-version completes on checklist rows
  ---
  duration_ms: 2.208735
  ...
# Subtest: continue: a resolving lane answer advances exactly once with one composed toast
ok 2818 - continue: a resolving lane answer advances exactly once with one composed toast
  ---
  duration_ms: 1.240007
  ...
# Subtest: continue: counted handled refs land past every handled key in one jump
ok 2819 - continue: counted handled refs land past every handled key in one jump
  ---
  duration_ms: 2.192525
  ...
# Subtest: continue: wrap is announced and the empty queue composes the empty notice
ok 2820 - continue: wrap is announced and the empty queue composes the empty notice
  ---
  duration_ms: 3.7623
  ...
# Subtest: continue: anchor-only planning survives cursor drift and lagging queues
ok 2821 - continue: anchor-only planning survives cursor drift and lagging queues
  ---
  duration_ms: 2.566237
  ...
# Subtest: continue: POST origins never wrap
ok 2822 - continue: POST origins never wrap
  ---
  duration_ms: 1.131249
  ...
# Subtest: complete: the last lane row before POST stays with the next-step toast
ok 2823 - complete: the last lane row before POST stays with the next-step toast
  ---
  duration_ms: 0.899556
  ...
# Subtest: complete: a wrap onto a skipped PRE row stays
ok 2824 - complete: a wrap onto a skipped PRE row stays
  ---
  duration_ms: 1.036478
  ...
# Subtest: complete: a step into ROTTEN shows the boundary line
ok 2825 - complete: a step into ROTTEN shows the boundary line
  ---
  duration_ms: 2.817387
  ...
# Subtest: busy: walk keys, refresh, claim, and capture are swallowed in the settle window
ok 2826 - busy: walk keys, refresh, claim, and capture are swallowed in the settle window
  ---
  duration_ms: 3.842603
  ...
# Subtest: advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
ok 2827 - advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
  ---
  duration_ms: 3.679261
  ...
# Subtest: advance: decay choices advance except reword, with no preamble of their own
ok 2828 - advance: decay choices advance except reword, with no preamble of their own
  ---
  duration_ms: 0.690057
  ...
# Subtest: jump history: same-note and cross-note auto-advances record, and <C-o> returns
ok 2829 - jump history: same-note and cross-note auto-advances record, and <C-o> returns
  ---
  duration_ms: 8.785937
  ...
# Subtest: jump history: a manual ]s also records its landing
ok 2830 - jump history: a manual ]s also records its landing
  ---
  duration_ms: 2.240756
  ...
# Subtest: api: reviewWalk v3 is frozen with version 1, degrades null, never throws
ok 2831 - api: reviewWalk v3 is frozen with version 1, degrades null, never throws
  ---
  duration_ms: 1.093888
  ...
# Subtest: walk identity: a stale accumulator key never moves the anchor
ok 2832 - walk identity: a stale accumulator key never moves the anchor
  ---
  duration_ms: 0.364526
  ...
# Subtest: walk identity: a lagging answered row stays excluded
ok 2833 - walk identity: a lagging answered row stays excluded
  ---
  duration_ms: 0.21001
  ...
# Subtest: walk identity: a line-shifting answer lands on the true successor by text
ok 2834 - walk identity: a line-shifting answer lands on the true successor by text
  ---
  duration_ms: 0.260858
  ...
# Subtest: walk identity: legacy anchors without text resolve as before
ok 2835 - walk identity: legacy anchors without text resolve as before
  ---
  duration_ms: 0.294392
  ...
# Subtest: walk identity: matchFreshStampRefs prefers text over line
ok 2836 - walk identity: matchFreshStampRefs prefers text over line
  ---
  duration_ms: 0.16739
  ...
# Subtest: walk identity: collectReviewAnswerKeys separates position from exclusion
ok 2837 - walk identity: collectReviewAnswerKeys separates position from exclusion
  ---
  duration_ms: 0.495014
  ...
# Subtest: return: planReviewWalkReturn pure decisions
ok 2838 - return: planReviewWalkReturn pure decisions
  ---
  duration_ms: 0.343636
  ...
# Subtest: return: same-note ]s returns then steps, both directions
ok 2839 - return: same-note ]s returns then steps, both directions
  ---
  duration_ms: 4.978761
  ...
# Subtest: return: a different due row returns instead of stepping from there
ok 2840 - return: a different due row returns instead of stepping from there
  ---
  duration_ms: 0.723079
  ...
# Subtest: return: cross-note return re-arms and records <C-o>
ok 2841 - return: cross-note return re-arms and records <C-o>
  ---
  duration_ms: 4.070458
  ...
# Subtest: return: a count is consumed and ignored
ok 2842 - return: a count is consumed and ignored
  ---
  duration_ms: 0.933422
  ...
# Subtest: return: endpoints never return
ok 2843 - return: endpoints never return
  ---
  duration_ms: 0.88007
  ...
# Subtest: return: its own stamp ends it
ok 2844 - return: its own stamp ends it
  ---
  duration_ms: 1.265856
  ...
# Subtest: return: a stamp elsewhere does not end it
ok 2845 - return: a stamp elsewhere does not end it
  ---
  duration_ms: 0.949502
  ...
# Subtest: return: answers move the current task, a stopped Ctrl+Enter clears it
ok 2846 - return: answers move the current task, a stopped Ctrl+Enter clears it
  ---
  duration_ms: 3.95662
  ...
# Subtest: return: a stale landing falls through in the same press
ok 2847 - return: a stale landing falls through in the same press
  ---
  duration_ms: 0.479324
  ...
# Subtest: return: a day change never returns
ok 2848 - return: a day change never returns
  ---
  duration_ms: 0.603301
  ...
# Subtest: predicate: reviewOutcomeResolves for the RECURRING resolution table
ok 2849 - predicate: reviewOutcomeResolves for the RECURRING resolution table
  ---
  duration_ms: 0.552725
  ...
# Subtest: recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
ok 2850 - recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
  ---
  duration_ms: 0.248915
  ...
# Subtest: return: a RECURRING landing rearms the current-task return
ok 2851 - return: a RECURRING landing rearms the current-task return
  ---
  duration_ms: 0.470107
  ...
# Subtest: Ctrl+Alt+F after a Rotten Log insertion lands on the shifted successor exactly once
ok 2852 - Ctrl+Alt+F after a Rotten Log insertion lands on the shifted successor exactly once
  ---
  duration_ms: 3.976269
  ...
# Subtest: review answer outcome vectors map to the schema vocabulary
ok 2853 - review answer outcome vectors map to the schema vocabulary
  ---
  duration_ms: 1.128975
  ...
# Subtest: event builder uses the walk row key and its tier, once per distinct key
ok 2854 - event builder uses the walk row key and its tier, once per distinct key
  ---
  duration_ms: 0.904145
  ...
# Subtest: journal appends are queued and failures retain events without failing answers
ok 2855 - journal appends are queued and failures retain events without failing answers
  ---
  duration_ms: 4.736809
  ...
# Subtest: card after-line outcomes map done, drop, defer, sequence, and card
ok 2856 - card after-line outcomes map done, drop, defer, sequence, and card
  ---
  duration_ms: 1.169552
  ...
# Subtest: journal events carry plugin@manifest version with a 2.x fallback
ok 2857 - journal events carry plugin@manifest version with a 2.x fallback
  ---
  duration_ms: 1.228866
  ...
# Subtest: write failures show one notice per burst and a recovery notice
ok 2858 - write failures show one notice per burst and a recovery notice
  ---
  duration_ms: 0.915457
  ...
# Subtest: missing api.stats shows one session notice and later delivers retained events
ok 2859 - missing api.stats shows one session notice and later delivers retained events
  ---
  duration_ms: 1.11087
  ...
# Subtest: validation rejects drop the event and continue the drain
ok 2860 - validation rejects drop the event and continue the drain
  ---
  duration_ms: 0.724233
  ...
# Subtest: pending journal events cap at 500 and warn once per burst
ok 2861 - pending journal events cap at 500 and warn once per burst
  ---
  duration_ms: 2.355435
  ...
# Subtest: decay config defaults to enabled with one roll per level
ok 2862 - decay config defaults to enabled with one roll per level
  ---
  duration_ms: 3.202782
  ...
# Subtest: decay:false disables decay and level rolls are accepted but ignored
ok 2863 - decay:false disables decay and level rolls are accepted but ignored
  ---
  duration_ms: 0.768777
  ...
# Subtest: decay.rolls sets the limit and levels[].rolls overrides it
ok 2864 - decay.rolls sets the limit and levels[].rolls overrides it
  ---
  duration_ms: 0.305503
  ...
# Subtest: decay config rejects bad rolls, unknown keys and non-priority use
ok 2865 - decay config rejects bad rolls, unknown keys and non-priority use
  ---
  duration_ms: 0.677704
  ...
# Subtest: classifyScheduleLogRollReason sorts automatic heads from deliberate ones
ok 2866 - classifyScheduleLogRollReason sorts automatic heads from deliberate ones
  ---
  duration_ms: 0.934453
  ...
# Subtest: conformance vectors 1-10: streaks at P2 with the default limit
ok 2867 - conformance vectors 1-10: streaks at P2 with the default limit
  ---
  duration_ms: 3.690013
  ...
# Subtest: conformance vectors 11-15: custom limits, disabled decay and edges
ok 2868 - conformance vectors 11-15: custom limits, disabled decay and edges
  ---
  duration_ms: 1.144524
  ...
# Subtest: the streak reader follows log grammar: legacy labels, nesting and stops
ok 2869 - the streak reader follows log grammar: legacy labels, nesting and stops
  ---
  duration_ms: 0.826106
  ...
# Subtest: rollPriorityRecommendationDate avoids the current date when the window has room
ok 2870 - rollPriorityRecommendationDate avoids the current date when the window has room
  ---
  duration_ms: 0.916649
  ...
# Subtest: decay and cancel reason formatters use the exact ladder copy
ok 2871 - decay and cancel reason formatters use the exact ladder copy
  ---
  duration_ms: 0.651102
  ...
# Subtest: the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
ok 2872 - the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
  ---
  duration_ms: 0.491337
  ...
# Subtest: the planner returns null without a configured priority
ok 2873 - the planner returns null without a configured priority
  ---
  duration_ms: 0.214579
  ...
# Subtest: buildPriorityRollPreviewModel carries the row copy for every kind
ok 2874 - buildPriorityRollPreviewModel carries the row copy for every kind
  ---
  duration_ms: 0.751314
  ...
# Subtest: picker-single recognizes the recommended-roll keypress
ok 2875 - picker-single recognizes the recommended-roll keypress
  ---
  duration_ms: 0.199851
  ...
# Subtest: picker-single stage-two footers carry the recommended-roll hints
ok 2876 - picker-single stage-two footers carry the recommended-roll hints
  ---
  duration_ms: 0.447965
  ...
# Subtest: picker-single shares one roll between the preview and the pinned row
ok 2877 - picker-single shares one roll between the preview and the pinned row
  ---
  duration_ms: 0.519712
  ...
# Subtest: picker-single plans the next-roll hint for the notice chips
ok 2878 - picker-single plans the next-roll hint for the notice chips
  ---
  duration_ms: 0.858839
  ...
# Subtest: picker-single notice cards name the roll, decay and next press
ok 2879 - picker-single notice cards name the roll, decay and next press
  ---
  duration_ms: 2.511614
  ...
# Subtest: picker-single decay payload and preview-target comparison
ok 2880 - picker-single decay payload and preview-target comparison
  ---
  duration_ms: 0.449488
  ...
# Subtest: picker-counted plans one recommendation per target with skips
ok 2881 - picker-counted plans one recommendation per target with skips
  ---
  duration_ms: 2.980789
  ...
# Subtest: picker-counted batch preview, footer and notice copy
ok 2882 - picker-counted batch preview, footer and notice copy
  ---
  duration_ms: 2.263729
  ...
# Subtest: picker-counted composes cancel then set-priority into one postimage
ok 2883 - picker-counted composes cancel then set-priority into one postimage
  ---
  duration_ms: 4.369468
  ...
# Subtest: picker-counted refuses a recurring cancel as one batch
ok 2884 - picker-counted refuses a recurring cancel as one batch
  ---
  duration_ms: 0.534169
  ...
# Subtest: recommended roll recovers with [unblocked::] when the writer is passed
ok 2885 - recommended roll recovers with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.957849
  ...
# Subtest: picker-counted stale lines refuse and new options stay byte-identical
ok 2886 - picker-counted stale lines refuse and new options stay byte-identical
  ---
  duration_ms: 1.223105
  ...
# Subtest: picker-links aggregates one recommendation per note
ok 2887 - picker-links aggregates one recommendation per note
  ---
  duration_ms: 1.315541
  ...
# Subtest: picker-links refuses a recurring cancel as one batch
ok 2888 - picker-links refuses a recurring cancel as one batch
  ---
  duration_ms: 0.402698
  ...
# Subtest: picker-links takes a single recommended roll with Ctrl+Enter
ok 2889 - picker-links takes a single recommended roll with Ctrl+Enter
  ---
  duration_ms: 36.383815
  ...
# Subtest: picker-links shows no pinned roll row in stage two
ok 2890 - picker-links shows no pinned roll row in stage two
  ---
  duration_ms: 5.182109
  ...
# Subtest: picker-links decays and cancels a single Task Link
ok 2891 - picker-links decays and cancels a single Task Link
  ---
  duration_ms: 6.416797
  ...
# Subtest: picker-links applies a mixed batch across two notes
ok 2892 - picker-links applies a mixed batch across two notes
  ---
  duration_ms: 4.523281
  ...
# Subtest: picker-links refuses the whole batch when a linked note changed
ok 2893 - picker-links refuses the whole batch when a linked note changed
  ---
  duration_ms: 1.926908
  ...
# Subtest: picker-links prunes today's open Pomodoro links
ok 2894 - picker-links prunes today's open Pomodoro links
  ---
  duration_ms: 4.680632
  ...
# Subtest: picker-single Ctrl+Enter rolls a P2 task in one undo group
ok 2895 - picker-single Ctrl+Enter rolls a P2 task in one undo group
  ---
  duration_ms: 17.495428
  ...
# Subtest: picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
ok 2896 - picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
  ---
  duration_ms: 12.941699
  ...
# Subtest: picker-single opens a ^prj task on inline scheduled for an immediate roll
ok 2897 - picker-single opens a ^prj task on inline scheduled for an immediate roll
  ---
  duration_ms: 13.775119
  ...
# Subtest: picker-counted opens on scheduled for an immediate mixed batch
ok 2898 - picker-counted opens on scheduled for an immediate mixed batch
  ---
  duration_ms: 13.621396
  ...
# Subtest: picker-links opens on scheduled for an immediate roll
ok 2899 - picker-links opens on scheduled for an immediate roll
  ---
  duration_ms: 12.083721
  ...
# Subtest: picker-single Ctrl+Enter decays a P2 task in one undo group
ok 2900 - picker-single Ctrl+Enter decays a P2 task in one undo group
  ---
  duration_ms: 12.758879
  ...
# Subtest: picker-single Ctrl+Enter cancels a P4 task in one undo group
ok 2901 - picker-single Ctrl+Enter cancels a P4 task in one undo group
  ---
  duration_ms: 12.860864
  ...
# Subtest: picker-single Ctrl+Enter in stage two writes the recommended roll
ok 2902 - picker-single Ctrl+Enter in stage two writes the recommended roll
  ---
  duration_ms: 13.403559
  ...
# Subtest: picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
ok 2903 - picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
  ---
  duration_ms: 2.789052
  ...
# Subtest: picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
ok 2904 - picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
  ---
  duration_ms: 10.073545
  ...
# Subtest: picker-single recurring P4 past the limit refuses and keeps the picker open
ok 2905 - picker-single recurring P4 past the limit refuses and keeps the picker open
  ---
  duration_ms: 12.817691
  ...
# Subtest: picker-single stale tasks refuse and re-render the decay preview
ok 2906 - picker-single stale tasks refuse and re-render the decay preview
  ---
  duration_ms: 13.070935
  ...
# Subtest: picker-single Ctrl+R on the card re-rolls the recommendation date
ok 2907 - picker-single Ctrl+R on the card re-rolls the recommendation date
  ---
  duration_ms: 2.814071
  ...
# Subtest: picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
ok 2908 - picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
  ---
  duration_ms: 2.075732
  ...
# Subtest: picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
ok 2909 - picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
  ---
  duration_ms: 11.159747
  ...
# Subtest: picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
ok 2910 - picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
  ---
  duration_ms: 11.827882
  ...
# Subtest: picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
ok 2911 - picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
  ---
  duration_ms: 12.457294
  ...
# Subtest: picker-counted Ctrl+Enter refuses when a target line changed
ok 2912 - picker-counted Ctrl+Enter refuses when a target line changed
  ---
  duration_ms: 12.183661
  ...
# Subtest: picker-counted Ctrl+Enter refuses a recurring cancel batch
ok 2913 - picker-counted Ctrl+Enter refuses a recurring cancel batch
  ---
  duration_ms: 11.329471
  ...
# Subtest: recommended roll on Pending offers a Work Log with the frozen date
ok 2914 - recommended roll on Pending offers a Work Log with the frozen date
  ---
  duration_ms: 1026.549736
  ...
# Subtest: recommended roll blank summary skips the Work Log without a fallback
ok 2915 - recommended roll blank summary skips the Work Log without a fallback
  ---
  duration_ms: 1029.800982
  ...
# Subtest: Ctrl+Enter in the Work Log stage confirms instead of re-rolling
ok 2916 - Ctrl+Enter in the Work Log stage confirms instead of re-rolling
  ---
  duration_ms: 1045.948337
  ...
# Subtest: counted recommended mixed batch logs only eligible roll and decay targets
ok 2917 - counted recommended mixed batch logs only eligible roll and decay targets
  ---
  duration_ms: 1032.127321
  ...
# Subtest: Task Link recommended roll deletes the emptied Pomodoro in the same daily write
ok 2918 - Task Link recommended roll deletes the emptied Pomodoro in the same daily write
  ---
  duration_ms: 3.802266
  ...
# Subtest: single keep logs still the primer with stamp in one undo
ok 2919 - single keep logs still the primer with stamp in one undo
  ---
  duration_ms: 12.427016
  ...
# Subtest: single keep logs blank with stamp in one undo
ok 2920 - single keep logs blank with stamp in one undo
  ---
  duration_ms: 2.023773
  ...
# Subtest: Esc retains the document and walk anchor; repeat command cannot open another prompt
ok 2921 - Esc retains the document and walk anchor; repeat command cannot open another prompt
  ---
  duration_ms: 0.861183
  ...
# Subtest: same-day repeat never prompts or appends, including saturated 999
ok 2922 - same-day repeat never prompts or appends, including saturated 999
  ---
  duration_ms: 3.361985
  ...
# Subtest: counted predicate: scheduled tickler
ok 2923 - counted predicate: scheduled tickler
  ---
  duration_ms: 0.30424
  ...
# Subtest: counted predicate: unblock tickler
ok 2924 - counted predicate: unblock tickler
  ---
  duration_ms: 0.173491
  ...
# Subtest: counted predicate: new
ok 2925 - counted predicate: new
  ---
  duration_ms: 0.170576
  ...
# Subtest: counted predicate: Pending
ok 2926 - counted predicate: Pending
  ---
  duration_ms: 0.106934
  ...
# Subtest: counted predicate: Next
ok 2927 - counted predicate: Next
  ---
  duration_ms: 0.306646
  ...
# Subtest: counted predicate: PROJECTS
ok 2928 - counted predicate: PROJECTS
  ---
  duration_ms: 0.442144
  ...
# Subtest: counted predicate: recurring
ok 2929 - counted predicate: recurring
  ---
  duration_ms: 0.176236
  ...
# Subtest: counted predicate: checklist
ok 2930 - counted predicate: checklist
  ---
  duration_ms: 0.083229
  ...
# Subtest: counted predicate: closed
ok 2931 - counted predicate: closed
  ---
  duration_ms: 0.080654
  ...
# Subtest: counted predicate: early
ok 2932 - counted predicate: early
  ---
  duration_ms: 0.082487
  ...
# Subtest: scheduled tickler logs; unblocked and legacy keeps never prompt
ok 2933 - scheduled tickler logs; unblocked and legacy keeps never prompt
  ---
  duration_ms: 2.440778
  ...
# Subtest: Pending retains its Work summary prompt
ok 2934 - Pending retains its Work summary prompt
  ---
  duration_ms: 1.34111
  ...
# Subtest: counted mixed sessions use one Work-first prompt and route each answer to its log
ok 2935 - counted mixed sessions use one Work-first prompt and route each answer to its log
  ---
  duration_ms: 1.945292
  ...
# Subtest: counted at-limit Rotten targets skip without opening a prompt or logging
ok 2936 - counted at-limit Rotten targets skip without opening a prompt or logging
  ---
  duration_ms: 0.454787
  ...
# Subtest: unavailable decay card falls through the reason planner
ok 2937 - unavailable decay card falls through the reason planner
  ---
  duration_ms: 0.99025
  ...
# Subtest: document changes while prompt is open refuse the entire keep
ok 2938 - document changes while prompt is open refuse the entire keep
  ---
  duration_ms: 0.650712
  ...
# Subtest: day changes while prompt is open refuse the entire keep
ok 2939 - day changes while prompt is open refuse the entire keep
  ---
  duration_ms: 0.576971
  ...
# Subtest: prediction changes while prompt is open refuse the entire keep
ok 2940 - prediction changes while prompt is open refuse the entire keep
  ---
  duration_ms: 0.939763
  ...
# Subtest: guard changes while prompt is open refuse the entire keep
ok 2941 - guard changes while prompt is open refuse the entire keep
  ---
  duration_ms: 0.520834
  ...
# Subtest: ambiguous Rotten markers disable the prompt and refuse even a bypass
ok 2942 - ambiguous Rotten markers disable the prompt and refuse even a bypass
  ---
  duration_ms: 1.197435
  ...
# Subtest: combined planner inserts nested targets bottom-up and preserves CRLF
ok 2943 - combined planner inserts nested targets bottom-up and preserves CRLF
  ---
  duration_ms: 1.140837
  ...
# Subtest: prompt copy separates streak from history and previews exact formatter output
ok 2944 - prompt copy separates streak from history and previews exact formatter output
  ---
  duration_ms: 0.433197
  ...
# Subtest: keep stage warns for inline fields, ignores IME Enter, and swallows both keep chords
ok 2945 - keep stage warns for inline fields, ignores IME Enter, and swallows both keep chords
  ---
  duration_ms: 1.01631
  ...
# Subtest: marker vectors match the Rust Rotten cases
ok 2946 - marker vectors match the Rust Rotten cases
  ---
  duration_ms: 1.429909
  ...
# Subtest: entry parsing accepts valid entries and rejects bad counts
ok 2947 - entry parsing accepts valid entries and rejects bad counts
  ---
  duration_ms: 0.373693
  ...
# Subtest: readRottenLog statuses cover missing, empty, ok, and unknown
ok 2948 - readRottenLog statuses cover missing, empty, ok, and unknown
  ---
  duration_ms: 0.819734
  ...
# Subtest: planManagedTaskLogEntry creates the log last and prepends entries
ok 2949 - planManagedTaskLogEntry creates the log last and prepends entries
  ---
  duration_ms: 0.803794
  ...
# Subtest: Work Log writes never file under the Rotten marker
ok 2950 - Work Log writes never file under the Rotten marker
  ---
  duration_ms: 0.54466
  ...
# Subtest: lane commit stamps an open Ready task
ok 2951 - lane commit stamps an open Ready task
  ---
  duration_ms: 2.688161
  ...
# Subtest: lane release stamps an open Next task
ok 2952 - lane release stamps an open Next task
  ---
  duration_ms: 0.411616
  ...
# Subtest: lane without a stamper leaves lines as they were
ok 2953 - lane without a stamper leaves lines as they were
  ---
  duration_ms: 0.184232
  ...
# Subtest: counted property set stamps every rewritten open task
ok 2954 - counted property set stamps every rewritten open task
  ---
  duration_ms: 2.068027
  ...
# Subtest: counted delete-property stamps the rewritten task
ok 2955 - counted delete-property stamps the rewritten task
  ---
  duration_ms: 0.548456
  ...
# Subtest: stamp lands before the suffix after a priority edit on a stamped line
ok 2956 - stamp lands before the suffix after a priority edit on a stamped line
  ---
  duration_ms: 0.596788
  ...
# Subtest: recurring tasks are never stamped
ok 2957 - recurring tasks are never stamped
  ---
  duration_ms: 0.281658
  ...
# Subtest: cancel never stamps
ok 2958 - cancel never stamps
  ---
  duration_ms: 1.080351
  ...
# Subtest: fresh and refresh never go through the end-append writers
ok 2959 - fresh and refresh never go through the end-append writers
  ---
  duration_ms: 0.428228
  ...
# Subtest: counted dependency edit stamps the rewritten parent
ok 2960 - counted dependency edit stamps the rewritten parent
  ---
  duration_ms: 5.117426
  ...
# Subtest: moved tasks are stamped at their destination
ok 2961 - moved tasks are stamped at their destination
  ---
  duration_ms: 3.741931
  ...
# Subtest: move without a stamper leaves lines as they were
ok 2962 - move without a stamper leaves lines as they were
  ---
  duration_ms: 0.773506
  ...
# Subtest: refresh row shows the effective interval in task mode
ok 2963 - refresh row shows the effective interval in task mode
  ---
  duration_ms: 0.97482
  ...
# Subtest: refresh row hides without the api and on closed tasks
ok 2964 - refresh row hides without the api and on closed tasks
  ---
  duration_ms: 0.202086
  ...
# Subtest: refresh row covers counted and link modes, including mixed
ok 2965 - refresh row covers counted and link modes, including mixed
  ---
  duration_ms: 0.34033
  ...
# Subtest: refresh value items offer presets and use default
ok 2966 - refresh value items offer presets and use default
  ---
  duration_ms: 0.967026
  ...
# Subtest: setRefreshLine stamps and sets or clears the interval
ok 2967 - setRefreshLine stamps and sets or clears the interval
  ---
  duration_ms: 0.480758
  ...
# Subtest: 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
ok 2968 - 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
  ---
  duration_ms: 10.834256
  ...
# Subtest: Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
ok 2969 - Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
  ---
  duration_ms: 6.194511
  ...
# Subtest: filtering expands matches, collapse state survives clearing, and hidden marks still submit
ok 2970 - filtering expands matches, collapse state survives clearing, and hidden marks still submit
  ---
  duration_ms: 5.092239
  ...
# Subtest: group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
ok 2971 - group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
  ---
  duration_ms: 5.526406
  ...
# Subtest: Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
ok 2972 - Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
  ---
  duration_ms: 1.286805
  ...
# Subtest: Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
ok 2973 - Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
  ---
  duration_ms: 2.379321
  ...
# Subtest: the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
ok 2974 - the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
  ---
  duration_ms: 0.915497
  ...
# Subtest: destination override shapes normalize and label
ok 2975 - destination override shapes normalize and label
  ---
  duration_ms: 0.294312
  ...
# Subtest: destination picker detection needs block-id-prompt api v1 with pick
ok 2976 - destination picker detection needs block-id-prompt api v1 with pick
  ---
  duration_ms: 0.529019
  ...
# Subtest: Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks
ok 2977 - Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks
  ---
  duration_ms: 2.753886
  ...
# Subtest: Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked
ok 2978 - Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked
  ---
  duration_ms: 1.212784
  ...
# Subtest: a cancelled destination pick and a missing picker leave rows untouched
ok 2979 - a cancelled destination pick and a missing picker leave rows untouched
  ---
  duration_ms: 1.468523
  ...
# Subtest: unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
ok 2980 - unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
  ---
  duration_ms: 1.134495
  ...
# Subtest: card model builds stable rows, scope metadata, and an existing recommendation
ok 2981 - card model builds stable rows, scope metadata, and an existing recommendation
  ---
  duration_ms: 9.817084
  ...
# Subtest: explicit preview builder matches writer rolls and deduplicates linked targets
ok 2982 - explicit preview builder matches writer rolls and deduplicates linked targets
  ---
  duration_ms: 0.922772
  ...
# Subtest: counted and linked card models report real target counts and mixed values
ok 2983 - counted and linked card models report real target counts and mixed values
  ---
  duration_ms: 4.409716
  ...
# Subtest: priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
ok 2984 - priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
  ---
  duration_ms: 2.724629
  ...
# Subtest: Escape, bare q, and Ctrl+[ close the card; nothing else does
ok 2985 - Escape, bare q, and Ctrl+[ close the card; nothing else does
  ---
  duration_ms: 0.962146
  ...
# Subtest: close keys never fire during composition or inside a text field
ok 2986 - close keys never fire during composition or inside a text field
  ---
  duration_ms: 1.365586
  ...
# Subtest: unavailable actions, input composition, and repeats stay safe
ok 2987 - unavailable actions, input composition, and repeats stay safe
  ---
  duration_ms: 2.120266
  ...
# Subtest: Blocks row summarizes warm-cache dependents and their last open reason
ok 2988 - Blocks row summarizes warm-cache dependents and their last open reason
  ---
  duration_ms: 1.106031
  ...
# Subtest: Blocks row refuses closed tasks and unencodable paths without an id
ok 2989 - Blocks row refuses closed tasks and unencodable paths without an id
  ---
  duration_ms: 2.181143
  ...
# Subtest: key resolver table covers lane state, API availability, and modifier guards
ok 2990 - key resolver table covers lane state, API availability, and modifier guards
  ---
  duration_ms: 2.876259
  ...
# Subtest: recurring cancellation and blocked lanes expose reasons instead of writes
ok 2991 - recurring cancellation and blocked lanes expose reasons instead of writes
  ---
  duration_ms: 0.760311
  ...
# Subtest: identity keys distinguish linked notes that share a line number
ok 2992 - identity keys distinguish linked notes that share a line number
  ---
  duration_ms: 1.74511
  ...
# Subtest: planScheduleReview opens for a bare date and skips when reason is known without Work Log
ok 2993 - planScheduleReview opens for a bare date and skips when reason is known without Work Log
  ---
  duration_ms: 0.931217
  ...
# Subtest: planScheduleReview counts unique tasks when Task Links repeat a target
ok 2994 - planScheduleReview counts unique tasks when Task Links repeat a target
  ---
  duration_ms: 0.319149
  ...
# Subtest: bare date on Ready opens a reason-only review and writes nothing until Enter
ok 2995 - bare date on Ready opens a reason-only review and writes nothing until Enter
  ---
  duration_ms: 21.368309
  ...
# Subtest: typed reason and blank reason on an existing Schedule Log keep per-target rules
ok 2996 - typed reason and blank reason on an existing Schedule Log keep per-target rules
  ---
  duration_ms: 11.549131
  ...
# Subtest: Ready vs Next vs Pending: only Next/Pending show Work summary
ok 2997 - Ready vs Next vs Pending: only Next/Pending show Work summary
  ---
  duration_ms: 11.890973
  ...
# Subtest: inline reason on Ready dispatches immediately; on Next it still reviews Work summary
ok 2998 - inline reason on Ready dispatches immediately; on Next it still reviews Work summary
  ---
  duration_ms: 5.436815
  ...
# Subtest: Tab moves from Reason to Work summary and Enter commits from either field
ok 2999 - Tab moves from Reason to Work summary and Enter commits from either field
  ---
  duration_ms: 5.399776
  ...
# Subtest: Back and Escape at both review fields write nothing
ok 3000 - Back and Escape at both review fields write nothing
  ---
  duration_ms: 4.966548
  ...
# Subtest: a target changed during review refuses with no write
ok 3001 - a target changed during review refuses with no write
  ---
  duration_ms: 3.180319
  ...
# Subtest: counted mixed targets share one review and one adapter call
ok 3002 - counted mixed targets share one review and one adapter call
  ---
  duration_ms: 3.950009
  ...
# Subtest: linked notes with equal line numbers both qualify
ok 3003 - linked notes with equal line numbers both qualify
  ---
  duration_ms: 3.231807
  ...
# Subtest: project lifecycle review names propagation and still writes once
ok 3004 - project lifecycle review names propagation and still writes once
  ---
  duration_ms: 2.567239
  ...
# Subtest: priority picks still skip the combined review and keep Work Log-only prompts
ok 3005 - priority picks still skip the combined review and keep Work Log-only prompts
  ---
  duration_ms: 2.116459
  ...
# Subtest: a typed date from the card's schedule row uses the combined review
ok 3006 - a typed date from the card's schedule row uses the combined review
  ---
  duration_ms: 1.874688
  ...
# Subtest: scheduling a Pending task goes straight to the combined review, never serial prompts
ok 3007 - scheduling a Pending task goes straight to the combined review, never serial prompts
  ---
  duration_ms: 5.037795
  ...
# Subtest: classic parser keeps ISO, M/D, and signed units and ignores concise forms
ok 3008 - classic parser keeps ISO, M/D, and signed units and ignores concise forms
  ---
  duration_ms: 1.36216
  ...
# Subtest: typed schedule resolver covers bare days, units, weekdays, and inline reasons
ok 3009 - typed schedule resolver covers bare days, units, weekdays, and inline reasons
  ---
  duration_ms: 1.178249
  ...
# Subtest: weekdays resolve to the next occurrence strictly after today
ok 3010 - weekdays resolve to the next occurrence strictly after today
  ---
  duration_ms: 0.153052
  ...
# Subtest: invalid leap dates, end-of-month offsets, and December rollover
ok 3011 - invalid leap dates, end-of-month offsets, and December rollover
  ---
  duration_ms: 0.372241
  ...
# Subtest: negative, overflow, malformed, and preset-filter queries are rejected without dates
ok 3012 - negative, overflow, malformed, and preset-filter queries are rejected without dates
  ---
  duration_ms: 0.189201
  ...
# Subtest: DST local-calendar arithmetic stays on calendar days in America/New_York
ok 3013 - DST local-calendar arithmetic stays on calendar days in America/New_York
  ---
  duration_ms: 91.665635
  ...
# Subtest: Task Card date stage previews weekday, ISO, relative distance, and rollover year
ok 3014 - Task Card date stage previews weekday, ISO, relative distance, and rollover year
  ---
  duration_ms: 14.962876
  ...
# Subtest: inline reason is preserved on the preview and skips the reason stage
ok 3015 - inline reason is preserved on the preview and skips the reason stage
  ---
  duration_ms: 10.793559
  ...
# Subtest: Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
ok 3016 - Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
  ---
  duration_ms: 4.653942
  ...
# Subtest: Shift+Enter on a Ready task commits in four gestures without a Work Log
ok 3017 - Shift+Enter on a Ready task commits in four gestures without a Work Log
  ---
  duration_ms: 2.885145
  ...
# Subtest: invalid typed dates render an error preview and do not write
ok 3018 - invalid typed dates render an error preview and do not write
  ---
  duration_ms: 5.001135
  ...
# Subtest: the card's schedule stage always uses the concise resolver
ok 3019 - the card's schedule stage always uses the concise resolver
  ---
  duration_ms: 2.042848
  ...
# Subtest: tomorrow stays a preset filter and is not stolen as a typed date
ok 3020 - tomorrow stays a preset filter and is not stolen as a typed date
  ---
  duration_ms: 1.442603
  ...
# Subtest: mixed Task Links preview one date and freeze that action with the inline reason
ok 3021 - mixed Task Links preview one date and freeze that action with the inline reason
  ---
  duration_ms: 5.291779
  ...
# Subtest: Ctrl+Enter still takes the recommended roll from the Task Card date stage
ok 3022 - Ctrl+Enter still takes the recommended roll from the Task Card date stage
  ---
  duration_ms: 2.995006
  ...
# Subtest: Modal harness models Obsidian 1.14 attachment and idempotent close
ok 3023 - Modal harness models Obsidian 1.14 attachment and idempotent close
  ---
  duration_ms: 1.570618
  ...
# Subtest: styles share key-card tokens and compact Task Card dimensions
ok 3024 - styles share key-card tokens and compact Task Card dimensions
  ---
  duration_ms: 0.309892
  ...
# Subtest: card renderer paints header, banner, strip, stable rows, more, and footer from the model
ok 3025 - card renderer paints header, banner, strip, stable rows, more, and footer from the model
  ---
  duration_ms: 13.301324
  ...
# Subtest: renderer does not consume randomness or invent recommendation data
ok 3026 - renderer does not consume randomness or invent recommendation data
  ---
  duration_ms: 2.053418
  ...
# Subtest: no-recommendation, cancel, mixed, long text, missing API, and error states render
ok 3027 - no-recommendation, cancel, mixed, long text, missing API, and error states render
  ---
  duration_ms: 7.997462
  ...
# Subtest: counted and linked cards disclose mixed values and Task Link notes
ok 3028 - counted and linked cards disclose mixed values and Task Link notes
  ---
  duration_ms: 5.139948
  ...
# Subtest: Ctrl+Shift+P always opens the Task Card, never the classic property list
ok 3029 - Ctrl+Shift+P always opens the Task Card, never the classic property list
  ---
  duration_ms: 3.491282
  ...
# Subtest: the plugin carries no Task Card pilot setting, date gate, or classic preference
ok 3030 - the plugin carries no Task Card pilot setting, date gate, or classic preference
  ---
  duration_ms: 20.612467
  ...
# Subtest: a leftover persisted taskCard flag is ignored and never rewritten
ok 3031 - a leftover persisted taskCard flag is ignored and never rewritten
  ---
  duration_ms: 9.300199
  ...
# Subtest: palette command is named Task card (set properties)
ok 3032 - palette command is named Task card (set properties)
  ---
  duration_ms: 11.105734
  ...
# Subtest: Task Card opens the compact card with dialog semantics and a close control
ok 3033 - Task Card opens the compact card with dialog semantics and a close control
  ---
  duration_ms: 1.797349
  ...
# Subtest: a More row opens that property's value stage, never a filter list, and Back restores the card
ok 3034 - a More row opens that property's value stage, never a filter list, and Back restores the card
  ---
  duration_ms: 3.49542
  ...
# Subtest: after open the actions list, not the Close button, has focus
ok 3035 - after open the actions list, not the Close button, has focus
  ---
  duration_ms: 8.014064
  ...
# Subtest: clicking card text keeps the card key router active exactly once
ok 3036 - clicking card text keeps the card key router active exactly once
  ---
  duration_ms: 12.533358
  ...
# Subtest: Ready card writes close from a key, P1 click, recommendations, and Alt+N
ok 3037 - Ready card writes close from a key, P1 click, recommendations, and Alt+N
  ---
  duration_ms: 7.346721
  ...
# Subtest: Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
ok 3038 - Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
  ---
  duration_ms: 4.956759
  ...
# Subtest: Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
ok 3039 - Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
  ---
  duration_ms: 10.486562
  ...
# Subtest: Ctrl+R recomputes and repaints the card recommendation
ok 3040 - Ctrl+R recomputes and repaints the card recommendation
  ---
  duration_ms: 1.553073
  ...
# Subtest: Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
ok 3041 - Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
  ---
  duration_ms: 18.349298
  ...
# Subtest: Task Link opens focused while resolving and consumes keys without replay
ok 3042 - Task Link opens focused while resolving and consumes keys without replay
  ---
  duration_ms: 3.520659
  ...
# Subtest: Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card
ok 3043 - Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card
  ---
  duration_ms: 1.753376
  ...
# Subtest: Ctrl+Shift+Alt+B on a Task Link opens the linked Blocks stage
ok 3044 - Ctrl+Shift+Alt+B on a Task Link opens the linked Blocks stage
  ---
  duration_ms: 1.149854
  ...
# Subtest: Task Link count replacement and source edits invalidate old resolutions
ok 3045 - Task Link count replacement and source edits invalidate old resolutions
  ---
  duration_ms: 1.313386
  ...
# Subtest: Task Link resolution failure and plugin unload close their shells
ok 3046 - Task Link resolution failure and plugin unload close their shells
  ---
  duration_ms: 1.591367
  ...
# Subtest: direct Depends on entry opens the dependency stage without painting the card or the list
ok 3047 - direct Depends on entry opens the dependency stage without painting the card or the list
  ---
  duration_ms: 0.850904
  ...
# Subtest: a direct stage for an unconfigured property closes instead of leaving an empty modal
ok 3048 - a direct stage for an unconfigured property closes instead of leaving an empty modal
  ---
  duration_ms: 0.30427
  ...
# Subtest: a refused direct stage closes instead of landing on a card or a list
ok 3049 - a refused direct stage closes instead of landing on a card or a list
  ---
  duration_ms: 0.614583
  ...
# Subtest: Ctrl+Shift+B lands on the Depends on stage with the same intent as card b
ok 3050 - Ctrl+Shift+B lands on the Depends on stage with the same intent as card b
  ---
  duration_ms: 2.307204
  ...
# Subtest: Ctrl+Shift+B Back returns to the card without re-dispatching
ok 3051 - Ctrl+Shift+B Back returns to the card without re-dispatching
  ---
  duration_ms: 1.269853
  ...
# Subtest: Ctrl+Shift+B on a plain bullet notices and closes the card
ok 3052 - Ctrl+Shift+B on a plain bullet notices and closes the card
  ---
  duration_ms: 0.609142
  ...
# Subtest: Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch
ok 3053 - Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch
  ---
  duration_ms: 2.754136
  ...
# Subtest: Ctrl+Shift+Alt+B on Depends-On and BLOCKS lines opens the owner's stage directly
ok 3054 - Ctrl+Shift+Alt+B on Depends-On and BLOCKS lines opens the owner's stage directly
  ---
  duration_ms: 2.22679
  ...
# Subtest: Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not
ok 3055 - Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not
  ---
  duration_ms: 5.43869
  ...
# Subtest: priority gesture writes the frozen date and duplicate dispatch is single-flight
ok 3056 - priority gesture writes the frozen date and duplicate dispatch is single-flight
  ---
  duration_ms: 7.072286
  ...
# Subtest: pending priority action passes its card preview through the Work Log adapter
ok 3057 - pending priority action passes its card preview through the Work Log adapter
  ---
  duration_ms: 1.637656
  ...
# Subtest: Task Link priority action refuses a stale cross-note preflight before writes
ok 3058 - Task Link priority action refuses a stale cross-note preflight before writes
  ---
  duration_ms: 5.158495
  ...
# Subtest: Task Link priority action rolls back earlier note writes after a later write fails
ok 3059 - Task Link priority action rolls back earlier note writes after a later write fails
  ---
  duration_ms: 2.548272
  ...
# Subtest: Task Link transaction reports a cleanup failure without implying global undo
ok 3060 - Task Link transaction reports a cleanup failure without implying global undo
  ---
  duration_ms: 1.299399
  ...
# Subtest: selected-property deletion uses the existing writer; other card rows stay non-deletable
ok 3061 - selected-property deletion uses the existing writer; other card rows stay non-deletable
  ---
  duration_ms: 7.029606
  ...
# Subtest: failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
ok 3062 - failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
  ---
  duration_ms: 1.848257
  ...
# Subtest: a refused deletion rebuilds the card from the refreshed line
ok 3063 - a refused deletion rebuilds the card from the refreshed line
  ---
  duration_ms: 1.847827
  ...
# Subtest: 0 deletes only priority and keeps the scheduled field byte-for-byte
ok 3064 - 0 deletes only priority and keeps the scheduled field byte-for-byte
  ---
  duration_ms: 1.785046
  ...
# Subtest: card keys pressed on a priority radio or the banner reach the resolver exactly once
ok 3065 - card keys pressed on a priority radio or the banner reach the resolver exactly once
  ---
  duration_ms: 2.885037
  ...
# Subtest: held or composing Enter on a radio or the banner never writes
ok 3066 - held or composing Enter on a radio or the banner never writes
  ---
  duration_ms: 1.133284
  ...
# Subtest: Escape, q, Q, and Ctrl+[ close the card without writing
ok 3067 - Escape, q, Q, and Ctrl+[ close the card without writing
  ---
  duration_ms: 3.417632
  ...
# Subtest: Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
ok 3068 - Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
  ---
  duration_ms: 0.778596
  ...
# Subtest: repeated close keys and a second close() are harmless
ok 3069 - repeated close keys and a second close() are harmless
  ---
  duration_ms: 1.344776
  ...
# Subtest: composition never closes the card or a stage
ok 3070 - composition never closes the card or a stage
  ---
  duration_ms: 1.02696
  ...
# Subtest: q typed into a stage's text field never closes the modal
ok 3071 - q typed into a stage's text field never closes the modal
  ---
  duration_ms: 0.758548
  ...
# Subtest: Ctrl+[ closes from a focused date field without writing
ok 3072 - Ctrl+[ closes from a focused date field without writing
  ---
  duration_ms: 0.994298
  ...
# Subtest: Ctrl+[ closes the schedule review from its Reason and Work summary fields
ok 3073 - Ctrl+[ closes the schedule review from its Reason and Work summary fields
  ---
  duration_ms: 6.18272
  ...
# Subtest: Ctrl+[ closes the summary-only schedule-work-log stage without writing
ok 3074 - Ctrl+[ closes the summary-only schedule-work-log stage without writing
  ---
  duration_ms: 1.297146
  ...
# Subtest: Ctrl+[ closes the lane-release Work summary without writing
ok 3075 - Ctrl+[ closes the lane-release Work summary without writing
  ---
  duration_ms: 1.247671
  ...
# Subtest: q closes from a focused More row and from the Close button
ok 3076 - q closes from a focused More row and from the Close button
  ---
  duration_ms: 2.006529
  ...
# Subtest: Ctrl+[ closes from focused card controls, the Back button, and the modal frame
ok 3077 - Ctrl+[ closes from focused card controls, the Back button, and the modal frame
  ---
  duration_ms: 2.826885
  ...
# Subtest: a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
ok 3078 - a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
  ---
  duration_ms: 6.338536
  ...
# Subtest: a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
ok 3079 - a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
  ---
  duration_ms: 6.624853
  ...
# Subtest: a direct dependency stage closes on Ctrl+[ but keeps q as typed text
ok 3080 - a direct dependency stage closes on Ctrl+[ but keeps q as typed text
  ---
  duration_ms: 0.634602
  ...
# Subtest: q and Ctrl+[ are not global closes: other modals and the decay card ignore them
ok 3081 - q and Ctrl+[ are not global closes: other modals and the decay card ignore them
  ---
  duration_ms: 0.862436
  ...
# Subtest: missing freshness API disables Review every with an honest reason
ok 3082 - missing freshness API disables Review every with an honest reason
  ---
  duration_ms: 0.587671
  ...
# Subtest: child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
ok 3083 - child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
  ---
  duration_ms: 0.803824
  ...
# Subtest: decay card keeps its classes and shares key-card tokens
ok 3084 - decay card keeps its classes and shares key-card tokens
  ---
  duration_ms: 0.137983
  ...
# Subtest: decay card footer always names the X drop alias; the trial date is not this gate
ok 3085 - decay card footer always names the X drop alias; the trial date is not this gate
  ---
  duration_ms: 0.227645
  ...
# Subtest: task card level chips reuse the shared priority mark when available
ok 3086 - task card level chips reuse the shared priority mark when available
  ---
  duration_ms: 0.954952
  ...
# Subtest: task card labels are unchanged without the priority mark api
ok 3087 - task card labels are unchanged without the priority mark api
  ---
  duration_ms: 3.309375
  ...
# Subtest: manifest order is authoritative and fragments share one lexical scope
ok 3088 - manifest order is authoritative and fragments share one lexical scope
  ---
  duration_ms: 125.465918
  ...
# Subtest: builds are deterministic and build:check is read-only on success
ok 3089 - builds are deterministic and build:check is read-only on success
  ---
  duration_ms: 172.823808
  ...
# Subtest: read-only check rejects changed fragments and edited generated output
ok 3090 - read-only check rejects changed fragments and edited generated output
  ---
  duration_ms: 147.304195
  ...
# Subtest: check rejects a missing generated bundle without writing it
ok 3091 - check rejects a missing generated bundle without writing it
  ---
  duration_ms: 51.090531
  ...
# Subtest: fragment line limit is enforced before writing output
ok 3092 - fragment line limit is enforced before writing output
  ---
  duration_ms: 1.723489
  ...
# Subtest: fragment syntax errors are rejected before writing output
ok 3093 - fragment syntax errors are rejected before writing output
  ---
  duration_ms: 27.494249
  ...
# Subtest: malformed, empty, duplicate, and traversal manifests are rejected read-only
    # Subtest: invalid JSON
    ok 1 - invalid JSON
      ---
      duration_ms: 0.789066
      ...
    # Subtest: empty manifest
    ok 2 - empty manifest
      ---
      duration_ms: 0.631064
      ...
    # Subtest: non-array manifest
    ok 3 - non-array manifest
      ---
      duration_ms: 0.618991
      ...
    # Subtest: duplicate entries
    ok 4 - duplicate entries
      ---
      duration_ms: 22.816122
      ...
    # Subtest: traversal entry
    ok 5 - traversal entry
      ---
      duration_ms: 0.562924
      ...
    # Subtest: absolute entry
    ok 6 - absolute entry
      ---
      duration_ms: 0.438837
      ...
    1..6
ok 3094 - malformed, empty, duplicate, and traversal manifests are rejected read-only
  ---
  duration_ms: 26.735423
  ...
# Subtest: missing and omitted fragments are rejected read-only
    # Subtest: missing manifest entry
    ok 1 - missing manifest entry
      ---
      duration_ms: 0.505495
      ...
    # Subtest: unlisted JavaScript source
    ok 2 - unlisted JavaScript source
      ---
      duration_ms: 23.147204
      ...
    1..2
ok 3095 - missing and omitted fragments are rejected read-only
  ---
  duration_ms: 23.866447
  ...
# Subtest: escaping fragment symlinks are rejected read-only
ok 3096 - escaping fragment symlinks are rejected read-only
  ---
  duration_ms: 1.009807
  ...
# Subtest: parity comparator identifies changed helper and plugin methods
ok 3097 - parity comparator identifies changed helper and plugin methods
  ---
  duration_ms: 7.760509
  ...
# Subtest: parity comparator accepts a mixin-split helper class but not a changed method or superclass
ok 3098 - parity comparator accepts a mixin-split helper class but not a changed method or superclass
  ---
  duration_ms: 0.420854
  ...
# Subtest: snapshot commands are available only for active Markdown files
ok 3099 - snapshot commands are available only for active Markdown files
  ---
  duration_ms: 1.630842
  ...
# Subtest: commands run bob ref create on the active path, with -C for closed tasks
ok 3100 - commands run bob ref create on the active path, with -C for closed tasks
  ---
  duration_ms: 5.126883
  ...
# Subtest: bob spawn uses the resolved path, vault environment, timeout, and NO_COLOR
ok 3101 - bob spawn uses the resolved path, vault environment, timeout, and NO_COLOR
  ---
  duration_ms: 1.241119
  ...
# Subtest: failure notices retain bob error and hint lines verbatim
ok 3102 - failure notices retain bob error and hint lines verbatim
  ---
  duration_ms: 0.538227
  ...
# Subtest: off desktop, bob spawning is refused with the desktop-app explanation
ok 3103 - off desktop, bob spawning is refused with the desktop-app explanation
  ---
  duration_ms: 0.512338
  ...
# Subtest: both prompt copies pass the shared fixture table identically
ok 3104 - both prompt copies pass the shared fixture table identically
  ---
  duration_ms: 7.530983
  ...
# Subtest: suggestion is valid, compact, and collision-aware
ok 3105 - suggestion is valid, compact, and collision-aware
  ---
  duration_ms: 0.661262
  ...
# Subtest: rename excludes exactly one old-ID occurrence
ok 3106 - rename excludes exactly one old-ID occurrence
  ---
  duration_ms: 0.208729
  ...
# Subtest: dependency legacy [id::] reuses only valid free IDs
ok 3107 - dependency legacy [id::] reuses only valid free IDs
  ---
  duration_ms: 0.363274
  ...
# Subtest: project conversion keeps the existing suggestBlockIdFromTask
ok 3108 - project conversion keeps the existing suggestBlockIdFromTask
  ---
  duration_ms: 0.912732
  ...
# Subtest: successor SB vectors are unchanged
ok 3109 - successor SB vectors are unchanged
  ---
  duration_ms: 0.992554
  ...
# Subtest: Linked-from CURRENT lists every checkbox status from the live index
ok 3110 - Linked-from CURRENT lists every checkbox status from the live index
  ---
  duration_ms: 19.035328
  ...
# Subtest: option-bracket ring reads Blocked as a source-only slot ahead of Ready
ok 3111 - option-bracket ring reads Blocked as a source-only slot ahead of Ready
  ---
  duration_ms: 1.830323
  ...
# Subtest: isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
ok 3112 - isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
  ---
  duration_ms: 0.416185
  ...
# Subtest: option-bracket refuses to change a member while its project is Blocked
ok 3113 - option-bracket refuses to change a member while its project is Blocked
  ---
  duration_ms: 2.885917
  ...
# Subtest: tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
ok 3114 - tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
  ---
  duration_ms: 1.345087
  ...
# Subtest: project resident notice reads the inline ^prj date and ignores frontmatter scheduled
ok 3115 - project resident notice reads the inline ^prj date and ignores frontmatter scheduled
  ---
  duration_ms: 0.698303
  ...
# Subtest: findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
ok 3116 - findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
  ---
  duration_ms: 0.285895
  ...
# Subtest: field removal collapses only the exposed span and preserves the rest of the line
ok 3117 - field removal collapses only the exposed span and preserves the rest of the line
  ---
  duration_ms: 0.243375
  ...
# Subtest: vault-path retirement preserves CRLF and a missing final newline
ok 3118 - vault-path retirement preserves CRLF and a missing final newline
  ---
  duration_ms: 1.036799
  ...
# Subtest: Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
ok 3119 - Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
  ---
  duration_ms: 0.585478
  ...
# Subtest: Schedule Log discovery ignores a marker owned by a nested grandchild
ok 3120 - Schedule Log discovery ignores a marker owned by a nested grandchild
  ---
  duration_ms: 0.410755
  ...
# Subtest: Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
ok 3121 - Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
  ---
  duration_ms: 0.566642
  ...
# Subtest: a task with no Schedule Log gets its field retired without any insertion or new marker
ok 3122 - a task with no Schedule Log gets its field retired without any insertion or new marker
  ---
  duration_ms: 0.165416
  ...
# Subtest: Schedule Log entry uses the canonical arrow, dash, and lock bytes
ok 3123 - Schedule Log entry uses the canonical arrow, dash, and lock bytes
  ---
  duration_ms: 0.117584
  ...
# Subtest: retirement stays a no-op for shapes that are not proof of a blocking date
ok 3124 - retirement stays a no-op for shapes that are not proof of a blocking date
  ---
  duration_ms: 0.173191
  ...
# Subtest: cycling Blocked backward to Cancelled retires the date and logs, matching forward
ok 3125 - cycling Blocked backward to Cancelled retires the date and logs, matching forward
  ---
  duration_ms: 4.154488
  ...
# Subtest: single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
ok 3126 - single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
  ---
  duration_ms: 0.997063
  ...
# Subtest: counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
ok 3127 - counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
  ---
  duration_ms: 1.903412
  ...
# Subtest: counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
ok 3128 - counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
  ---
  duration_ms: 0.694506
  ...
# Subtest: transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
ok 3129 - transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
  ---
  duration_ms: 2.058648
  ...
# Subtest: pressing again after Blocked retirement performs an ordinary transition with no further changes
ok 3130 - pressing again after Blocked retirement performs an ordinary transition with no further changes
  ---
  duration_ms: 0.235459
  ...
# Subtest: Alt+] on a date-blocked ^prj recovers open residents in step
ok 3131 - Alt+] on a date-blocked ^prj recovers open residents in step
  ---
  duration_ms: 17.604267
  ...
# Subtest: Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
ok 3132 - Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
  ---
  duration_ms: 1.567071
  ...
# Subtest: planProjectResidentRecoveryEdits recovers when a cross-note id is not open
ok 3133 - planProjectResidentRecoveryEdits recovers when a cross-note id is not open
  ---
  duration_ms: 0.412998
  ...
# Subtest: Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
ok 3134 - Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
  ---
  duration_ms: 1.458614
  ...
# Subtest: Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
ok 3135 - Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
  ---
  duration_ms: 0.949281
  ...
# Subtest: Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
ok 3136 - Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
  ---
  duration_ms: 1.793864
  ...
# Subtest: cycling a transcluded ^prj recovers residents in the source note
ok 3137 - cycling a transcluded ^prj recovers residents in the source note
  ---
  duration_ms: 1.107865
  ...
# Subtest: cycler BK1–BK12 accept and empty
ok 3138 - cycler BK1–BK12 accept and empty
  ---
  duration_ms: 1.571109
  ...
# Subtest: cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded
ok 3139 - cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded
  ---
  duration_ms: 0.619041
  ...
# Subtest: cycler MC4 strike/restore skip BLOCKS lines
ok 3140 - cycler MC4 strike/restore skip BLOCKS lines
  ---
  duration_ms: 0.884498
  ...
# Subtest: cycler MC3 tree close skips BLOCKS embeds
ok 3141 - cycler MC3 tree close skips BLOCKS embeds
  ---
  duration_ms: 0.988266
  ...
# Subtest: cycler MC1/MC2 Pomodoro and successor scanners skip managed lines
ok 3142 - cycler MC1/MC2 Pomodoro and successor scanners skip managed lines
  ---
  duration_ms: 1.323626
  ...
# Subtest: cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS
ok 3143 - cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS
  ---
  duration_ms: 0.280916
  ...
# Subtest: range planner preserves every single-item mode without an effective count
ok 3144 - range planner preserves every single-item mode without an effective count
  ---
  duration_ms: 10.813877
  ...
# Subtest: item counts carry children, skip blank lines and loose continuations, and clamp
ok 3145 - item counts carry children, skip blank lines and loose continuations, and clamp
  ---
  duration_ms: 0.479665
  ...
# Subtest: range stops at headings, shallower lines, same-level paragraphs and fences
ok 3146 - range stops at headings, shallower lines, same-level paragraphs and fences
  ---
  duration_ms: 0.2618
  ...
# Subtest: siblings require the exact whitespace and blockquote prefix
ok 3147 - siblings require the exact whitespace and blockquote prefix
  ---
  duration_ms: 0.278141
  ...
# Subtest: counted demotion moves four complete blocks to one existing section
ok 3148 - counted demotion moves four complete blocks to one existing section
  ---
  duration_ms: 6.289973
  ...
# Subtest: counted demotion creates a typed section or one default Requirements section
ok 3149 - counted demotion creates a typed section or one default Requirements section
  ---
  duration_ms: 3.529525
  ...
# Subtest: bottom-up removal splices blank seams and maps destinations before the source
ok 3150 - bottom-up removal splices blank seams and maps destinations before the source
  ---
  duration_ms: 0.595196
  ...
# Subtest: counted promotion Enter appends tasks in order and removes an emptied source section
ok 3151 - counted promotion Enter appends tasks in order and removes an emptied source section
  ---
  duration_ms: 1.334206
  ...
# Subtest: counted promotion to existing or new non-Tasks destinations keeps all bullets plain
ok 3152 - counted promotion to existing or new non-Tasks destinations keeps all bullets plain
  ---
  duration_ms: 0.720575
  ...
# Subtest: same-source Tasks promotion rewrites all selected lines in place
ok 3153 - same-source Tasks promotion rewrites all selected lines in place
  ---
  duration_ms: 1.25225
  ...
# Subtest: counted demotion outside Tasks moves to the next section in one write
ok 3154 - counted demotion outside Tasks moves to the next section in one write
  ---
  duration_ms: 0.538768
  ...
# Subtest: in-place ranges write once without centering for nested, non-dash, and unrouted items
ok 3155 - in-place ranges write once without centering for nested, non-dash, and unrouted items
  ---
  duration_ms: 1.13168
  ...
# Subtest: mixed demotion ranges count unchanged siblings and only move top-level dash tasks
ok 3156 - mixed demotion ranges count unchanged siblings and only move top-level dash tasks
  ---
  duration_ms: 0.53456
  ...
# Subtest: mixed promotion preserves existing tasks and a nonempty source section
ok 3157 - mixed promotion preserves existing tasks and a nonempty source section
  ---
  duration_ms: 0.279644
  ...
# Subtest: Vim action consumes explicit additional-item counts and preserves bare behavior
ok 3158 - Vim action consumes explicit additional-item counts and preserves bare behavior
  ---
  duration_ms: 3.648392
  ...
# Subtest: command checking preserves pending count; execution consumes it once and resets Vim
ok 3159 - command checking preserves pending count; execution consumes it once and resets Vim
  ---
  duration_ms: 1.574686
  ...
# Subtest: command route stays single without normal-mode explicit count and supports in-place ranges
ok 3160 - command route stays single without normal-mode explicit count and supports in-place ranges
  ---
  duration_ms: 0.558005
  ...
# Subtest: picker displays at most five preview rows plus overflow; single picker is unchanged
ok 3161 - picker displays at most five preview rows plus overflow; single picker is unchanged
  ---
  duration_ms: 2.119315
  ...
# Subtest: stale counted picker and cancelled picker never write
ok 3162 - stale counted picker and cancelled picker never write
  ---
  duration_ms: 1.29981
  ...
# Subtest: counted moves round-trip CRLF and preserve the presence or absence of a final newline
ok 3163 - counted moves round-trip CRLF and preserve the presence or absence of a final newline
  ---
  duration_ms: 4.308842
  ...
# Subtest: direct open/done transitions include incomplete statuses without broadening excluded statuses
ok 3164 - direct open/done transitions include incomplete statuses without broadening excluded statuses
  ---
  duration_ms: 1.520833
  ...
# Subtest: Ctrl+Enter block-link selection recognizes live and retired forms
ok 3165 - Ctrl+Enter block-link selection recognizes live and retired forms
  ---
  duration_ms: 2.21574
  ...
# Subtest: Pomodoro child ownership is status-neutral and bounded by contiguous list structure
ok 3166 - Pomodoro child ownership is status-neutral and bounded by contiguous list structure
  ---
  duration_ms: 0.889407
  ...
# Subtest: daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
ok 3167 - daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
  ---
  duration_ms: 0.332134
  ...
# Subtest: parsePomodoroEntryLineParts reads placeholder and range names conservatively
ok 3168 - parsePomodoroEntryLineParts reads placeholder and range names conservatively
  ---
  duration_ms: 1.011671
  ...
# Subtest: formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
ok 3169 - formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
  ---
  duration_ms: 0.210291
  ...
# Subtest: Pomodoro bullet toggle accepts empty indented list items
ok 3170 - Pomodoro bullet toggle accepts empty indented list items
  ---
  duration_ms: 0.408499
  ...
# Subtest: Pomodoro bullet toggle rejects non-empty or out-of-section bullets
ok 3171 - Pomodoro bullet toggle rejects non-empty or out-of-section bullets
  ---
  duration_ms: 0.274083
  ...
# Subtest: Pomodoro bullet toggle reverses only empty open childless placeholders
ok 3172 - Pomodoro bullet toggle reverses only empty open childless placeholders
  ---
  duration_ms: 0.669428
  ...
# Subtest: Pomodoro bullet toggle reverses named empty open childless placeholders
ok 3173 - Pomodoro bullet toggle reverses named empty open childless placeholders
  ---
  duration_ms: 0.440741
  ...
# Subtest: Pomodoro bullet toggle round trips and normalizes child indentation
ok 3174 - Pomodoro bullet toggle round trips and normalizes child indentation
  ---
  duration_ms: 0.266448
  ...
# Subtest: Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
ok 3175 - Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
  ---
  duration_ms: 0.167529
  ...
# Subtest: Pomodoro toggle key gate does not shadow bare Option bracket cycling
ok 3176 - Pomodoro toggle key gate does not shadow bare Option bracket cycling
  ---
  duration_ms: 0.181015
  ...
# Subtest: Pomodoro toggle command is daily-only and places the cursor for both directions
ok 3177 - Pomodoro toggle command is daily-only and places the cursor for both directions
  ---
  duration_ms: 0.662354
  ...
# Subtest: Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
ok 3178 - Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
  ---
  duration_ms: 0.383071
  ...
# Subtest: Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
ok 3179 - Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
  ---
  duration_ms: 2.133491
  ...
# Subtest: Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
ok 3180 - Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
  ---
  duration_ms: 25.621326
  ...
# Subtest: Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
ok 3181 - Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
  ---
  duration_ms: 1.904555
  ...
# Subtest: Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
ok 3182 - Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
  ---
  duration_ms: 2.471096
  ...
# Subtest: Ctrl+Enter closing the local line over an already-closed target does not write it a second time
ok 3183 - Ctrl+Enter closing the local line over an already-closed target does not write it a second time
  ---
  duration_ms: 0.806789
  ...
# Subtest: Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
ok 3184 - Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
  ---
  duration_ms: 0.622808
  ...
# Subtest: Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
ok 3185 - Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
  ---
  duration_ms: 1.744419
  ...
# Subtest: Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
ok 3186 - Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
  ---
  duration_ms: 0.617628
  ...
# Subtest: Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
ok 3187 - Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
  ---
  duration_ms: 0.766943
  ...
# Subtest: Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
ok 3188 - Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
  ---
  duration_ms: 0.891822
  ...
# Subtest: Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
ok 3189 - Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
  ---
  duration_ms: 1.06347
  ...
# Subtest: getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
ok 3190 - getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
  ---
  duration_ms: 0.423819
  ...
# Subtest: Ctrl+Enter close continues the walk with complete after finalize ran
ok 3191 - Ctrl+Enter close continues the walk with complete after finalize ran
  ---
  duration_ms: 12.276087
  ...
# Subtest: Ctrl+Enter close continues only after transclusion propagation landed
ok 3192 - Ctrl+Enter close continues only after transclusion propagation landed
  ---
  duration_ms: 13.315542
  ...
# Subtest: Ctrl+Enter reopen settles the walk with null
ok 3193 - Ctrl+Enter reopen settles the walk with null
  ---
  duration_ms: 11.370219
  ...
# Subtest: Ctrl+Enter swallows the key with no write while the walk is busy
ok 3194 - Ctrl+Enter swallows the key with no write while the walk is busy
  ---
  duration_ms: 11.018287
  ...
# Subtest: Ctrl+Enter with a null capture behaves exactly like today
ok 3195 - Ctrl+Enter with a null capture behaves exactly like today
  ---
  duration_ms: 11.393844
  ...
# Subtest: Ctrl+Enter with nav v2 or no nav keeps today's behavior
ok 3196 - Ctrl+Enter with nav v2 or no nav keeps today's behavior
  ---
  duration_ms: 21.014565
  ...
# Subtest: Ctrl+Enter lets the checklist claim win before capturing
ok 3197 - Ctrl+Enter lets the checklist claim win before capturing
  ---
  duration_ms: 0.733019
  ...
# Subtest: Ctrl+Enter settles the walk with null when the toggle rejects
ok 3198 - Ctrl+Enter settles the walk with null when the toggle rejects
  ---
  duration_ms: 11.063714
  ...
# Subtest: Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
ok 3199 - Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
  ---
  duration_ms: 3.9558
  ...
# Subtest: eligible Tasks demotions prompt in project and non-project notes
ok 3200 - eligible Tasks demotions prompt in project and non-project notes
  ---
  duration_ms: 3.61061
  ...
# Subtest: selectable headings skip YAML, fences, empty titles, and Tasks
ok 3201 - selectable headings skip YAML, fences, empty titles, and Tasks
  ---
  duration_ms: 1.166636
  ...
# Subtest: duplicate heading identities stay distinct and route to the chosen occurrence
ok 3202 - duplicate heading identities stay distinct and route to the chosen occurrence
  ---
  duration_ms: 1.263581
  ...
# Subtest: demotion picker defaults and typed names resolve without synthetic duplicates
ok 3203 - demotion picker defaults and typed names resolve without synthetic duplicates
  ---
  duration_ms: 2.20039
  ...
# Subtest: picker keyboard state wraps, clamps, and refuses invalid Enter
ok 3204 - picker keyboard state wraps, clamps, and refuses invalid Enter
  ---
  duration_ms: 0.412377
  ...
# Subtest: new-section formatting keeps extra blanks, final newlines, and nested children
ok 3205 - new-section formatting keeps extra blanks, final newlines, and nested children
  ---
  duration_ms: 0.921288
  ...
# Subtest: existing-section insertion works before and after the source on CRLF-backed editors
ok 3206 - existing-section insertion works before and after the source on CRLF-backed editors
  ---
  duration_ms: 3.765576
  ...
# Subtest: command opens one picker, writes only on accept, and restores cursor plus center
ok 3207 - command opens one picker, writes only on accept, and restores cursor plus center
  ---
  duration_ms: 0.961856
  ...
# Subtest: pointer activation, Escape, and double-submit protection leave a consistent note
ok 3208 - pointer activation, Escape, and double-submit protection leave a consistent note
  ---
  duration_ms: 1.264493
  ...
# Subtest: stale document, changed editor, or missing heading notice without writing
ok 3209 - stale document, changed editor, or missing heading notice without writing
  ---
  duration_ms: 2.522293
  ...
# Subtest: dependency normalizer writes path-qualified IDs and is idempotent
ok 3210 - dependency normalizer writes path-qualified IDs and is idempotent
  ---
  duration_ms: 2.176855
  ...
# Subtest: Tasks-generated IDs become local block IDs when none exists
ok 3211 - Tasks-generated IDs become local block IDs when none exists
  ---
  duration_ms: 0.961515
  ...
# Subtest: note rename rewrites target IDs and yields exact propagation mappings
ok 3212 - note rename rewrites target IDs and yields exact propagation mappings
  ---
  duration_ms: 0.365528
  ...
# Subtest: note rename also rewrites same-file dependsOn references
ok 3213 - note rename also rewrites same-file dependsOn references
  ---
  duration_ms: 0.265867
  ...
# Subtest: dependency normalization skips unsupported paths and fenced examples
ok 3214 - dependency normalization skips unsupported paths and fenced examples
  ---
  duration_ms: 0.427506
  ...
# Subtest: blocked-dependent planner matches the CLI dependency truth table
ok 3215 - blocked-dependent planner matches the CLI dependency truth table
  ---
  duration_ms: 2.536711
  ...
# Subtest: blocked-dependent edits preserve EOLs and skip stale lines idempotently
ok 3216 - blocked-dependent edits preserve EOLs and skip stale lines idempotently
  ---
  duration_ms: 0.845654
  ...
# Subtest: project recovery strips resident tags and works without freshness v12
ok 3217 - project recovery strips resident tags and works without freshness v12
  ---
  duration_ms: 1.411734
  ...
# Subtest: recovery passes daily-note and Today skip flags to ledger freshness
ok 3218 - recovery passes daily-note and Today skip flags to ledger freshness
  ---
  duration_ms: 0.429229
  ...
# Subtest: normalization mappings propagate to every dependent file
ok 3219 - normalization mappings propagate to every dependent file
  ---
  duration_ms: 1.259133
  ...
# Subtest: runtime normalizer skips unsupported paths with one informative notice
ok 3220 - runtime normalizer skips unsupported paths with one informative notice
  ---
  duration_ms: 0.724322
  ...
# Subtest: rename reconciliation rewrites the target and every dependent
ok 3221 - rename reconciliation rewrites the target and every dependent
  ---
  duration_ms: 0.543237
  ...
# Subtest: editor dependency normalization abandons and reschedules stale snapshots
ok 3222 - editor dependency normalization abandons and reschedules stale snapshots
  ---
  duration_ms: 0.49789
  ...
# Subtest: rename reconciliation abandons and reschedules stale editor snapshots
ok 3223 - rename reconciliation abandons and reschedules stale editor snapshots
  ---
  duration_ms: 0.320252
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 3224 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.80201
  ...
# Subtest: close-time retirement skips Depends-On lines
ok 3225 - close-time retirement skips Depends-On lines
  ---
  duration_ms: 1.258031
  ...
# Subtest: reopen restoration skips Depends-On lines instead of re-embedding them
ok 3226 - reopen restoration skips Depends-On lines instead of re-embedding them
  ---
  duration_ms: 0.591088
  ...
# Subtest: embedded-tree close collection ignores Depends-On lines
ok 3227 - embedded-tree close collection ignores Depends-On lines
  ---
  duration_ms: 0.347463
  ...
# Subtest: Alt-bracket bullet formatting never applies to Depends-On lines
ok 3228 - Alt-bracket bullet formatting never applies to Depends-On lines
  ---
  duration_ms: 0.595576
  ...
# Subtest: Ctrl+Enter on a dependency link closes only the target and runs the recovery
ok 3229 - Ctrl+Enter on a dependency link closes only the target and runs the recovery
  ---
  duration_ms: 1.665028
  ...
# Subtest: Ctrl+Enter on a dependency link reopens only the target, root-only
ok 3230 - Ctrl+Enter on a dependency link reopens only the target, root-only
  ---
  duration_ms: 1.128955
  ...
# Subtest: single and counted Alt-bracket cycle the dependency target under the cursor
ok 3231 - single and counted Alt-bracket cycle the dependency target under the cursor
  ---
  duration_ms: 19.274344
  ...
# Subtest: single and counted Alt-bracket report when the cursor is off every dependency link
ok 3232 - single and counted Alt-bracket report when the cursor is off every dependency link
  ---
  duration_ms: 0.761483
  ...
# Subtest: Ctrl+Enter candidate resolution finds plain links on Depends-On lines
ok 3233 - Ctrl+Enter candidate resolution finds plain links on Depends-On lines
  ---
  duration_ms: 0.21452
  ...
# Subtest: dependency-id normalisation never edits Depends-On lines
ok 3234 - dependency-id normalisation never edits Depends-On lines
  ---
  duration_ms: 0.331312
  ...
# Subtest: note rename rewrites fields while leaving Depends-On lines alone
ok 3235 - note rename rewrites fields while leaving Depends-On lines alone
  ---
  duration_ms: 0.244446
  ...
# Subtest: recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
ok 3236 - recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
  ---
  duration_ms: 2.339885
  ...
# Subtest: cycler freshness: local-fallback rewrite stamps last via injected stamper
ok 3237 - cycler freshness: local-fallback rewrite stamps last via injected stamper
  ---
  duration_ms: 2.094718
  ...
# Subtest: cycler freshness: rewrites without a stamper are unchanged (identity default)
ok 3238 - cycler freshness: rewrites without a stamper are unchanged (identity default)
  ---
  duration_ms: 0.433848
  ...
# Subtest: cycler freshness: a throwing stamper leaves the rewritten line intact
ok 3239 - cycler freshness: a throwing stamper leaves the rewritten line intact
  ---
  duration_ms: 0.189932
  ...
# Subtest: cycler freshness: transcluded rewrite stamps last via injected stamper
ok 3240 - cycler freshness: transcluded rewrite stamps last via injected stamper
  ---
  duration_ms: 0.226211
  ...
# Subtest: cycler freshness: cycling a plain line stamps through the follow-up edit
ok 3241 - cycler freshness: cycling a plain line stamps through the follow-up edit
  ---
  duration_ms: 1.0583
  ...
# Subtest: cycler freshness: Tasks-command rewrite with the expected status is stamped
ok 3242 - cycler freshness: Tasks-command rewrite with the expected status is stamped
  ---
  duration_ms: 0.489093
  ...
# Subtest: cycler freshness: Tasks command that inserts a line never stamps
ok 3243 - cycler freshness: Tasks command that inserts a line never stamps
  ---
  duration_ms: 0.426124
  ...
# Subtest: cycler freshness: Tasks command that deletes the line never stamps the next task
ok 3244 - cycler freshness: Tasks command that deletes the line never stamps the next task
  ---
  duration_ms: 0.277439
  ...
# Subtest: cycler freshness: Tasks command that leaves a different status never stamps
ok 3245 - cycler freshness: Tasks command that leaves a different status never stamps
  ---
  duration_ms: 0.548717
  ...
# Subtest: cycler freshness: cycling without ledger-tools writes no stamp
ok 3246 - cycler freshness: cycling without ledger-tools writes no stamp
  ---
  duration_ms: 0.637837
  ...
# Subtest: cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
ok 3247 - cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
  ---
  duration_ms: 0.264795
  ...
# Subtest: Pomodoro marker helpers normalize every block link and preserve fences and EOLs
ok 3248 - Pomodoro marker helpers normalize every block link and preserve fences and EOLs
  ---
  duration_ms: 3.298144
  ...
# Subtest: completed Pomodoro markers are normalized per occurrence
ok 3249 - completed Pomodoro markers are normalized per occurrence
  ---
  duration_ms: 0.475137
  ...
# Subtest: move-only Pomodoro links require a strict immediate hash directive
ok 3250 - move-only Pomodoro links require a strict immediate hash directive
  ---
  duration_ms: 2.419317
  ...
# Subtest: Pomodoro move-only planner toggles links across additional physical lines
ok 3251 - Pomodoro move-only planner toggles links across additional physical lines
  ---
  duration_ms: 1.046007
  ...
# Subtest: Pomodoro move-only planner round trips exact text and rejects strict non-matches
ok 3252 - Pomodoro move-only planner round trips exact text and rejects strict non-matches
  ---
  duration_ms: 0.478133
  ...
# Subtest: bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
ok 3253 - bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
  ---
  duration_ms: 1.418286
  ...
# Subtest: Pomodoro move-only runtime removes locally and validates additions independently
ok 3254 - Pomodoro move-only runtime removes locally and validates additions independently
  ---
  duration_ms: 0.952547
  ...
# Subtest: Pomodoro move-only runtime protects live lines after asynchronous failures
ok 3255 - Pomodoro move-only runtime protects live lines after asynchronous failures
  ---
  duration_ms: 0.376689
  ...
# Subtest: Pomodoro hash Vim mapping distinguishes bare and explicit repeats
ok 3256 - Pomodoro hash Vim mapping distinguishes bare and explicit repeats
  ---
  duration_ms: 10.781947
  ...
# Subtest: Pomodoro completion marks originals and carries clean live copies
ok 3257 - Pomodoro completion marks originals and carries clean live copies
  ---
  duration_ms: 1.724992
  ...
# Subtest: Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
ok 3258 - Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
  ---
  duration_ms: 0.944121
  ...
# Subtest: Pomodoro completion carries the closed Pomodoro name onto created entries
ok 3259 - Pomodoro completion carries the closed Pomodoro name onto created entries
  ---
  duration_ms: 0.430301
  ...
# Subtest: buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
ok 3260 - buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
  ---
  duration_ms: 0.43988
  ...
# Subtest: buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
ok 3261 - buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
  ---
  duration_ms: 0.280165
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is marked
ok 3262 - buildPomodoroCompletionPlan keeps source order when every carried link is marked
  ---
  duration_ms: 0.200122
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
ok 3263 - buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
  ---
  duration_ms: 0.23074
  ...
# Subtest: Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
ok 3264 - Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
  ---
  duration_ms: 5.704758
  ...
# Subtest: deferred-only close deletes the emptied entry and carries stripped links
ok 3265 - deferred-only close deletes the emptied entry and carries stripped links
  ---
  duration_ms: 0.604533
  ...
# Subtest: deferred-only close at EOF leaves no dangling newline
ok 3266 - deferred-only close at EOF leaves no dangling newline
  ---
  duration_ms: 0.218336
  ...
# Subtest: a close with a remaining copyable link keeps the [x] entry
ok 3267 - a close with a remaining copyable link keeps the [x] entry
  ---
  duration_ms: 0.266147
  ...
# Subtest: a prose sibling keeps the closed entry on a deferred close
ok 3268 - a prose sibling keeps the closed entry on a deferred close
  ---
  duration_ms: 0.301425
  ...
# Subtest: Ctrl+Enter deferred-only close deletes the entry in one gesture
ok 3269 - Ctrl+Enter deferred-only close deletes the entry in one gesture
  ---
  duration_ms: 3.4586
  ...
# Subtest: deferred-only close keeps a separated prose child and deletes fence-only leftovers whole
ok 3270 - deferred-only close keeps a separated prose child and deletes fence-only leftovers whole
  ---
  duration_ms: 0.849782
  ...
# Subtest: deferred-only successor relocation uses the inserted placeholder
ok 3271 - deferred-only successor relocation uses the inserted placeholder
  ---
  duration_ms: 0.265286
  ...
# Subtest: selected Done Pomodoro transclusion reopens only its cross-file root
ok 3272 - selected Done Pomodoro transclusion reopens only its cross-file root
  ---
  duration_ms: 8.1427
  ...
# Subtest: selected same-file Done target reopens root-only in the live editor
ok 3273 - selected same-file Done target reopens root-only in the live editor
  ---
  duration_ms: 2.037568
  ...
# Subtest: selected retired link reopens its root and restores the historical occurrence
ok 3274 - selected retired link reopens its root and restores the historical occurrence
  ---
  duration_ms: 1.481367
  ...
# Subtest: incomplete selected Pomodoro transclusion still closes recursively
ok 3275 - incomplete selected Pomodoro transclusion still closes recursively
  ---
  duration_ms: 2.92878
  ...
# Subtest: Done Pomodoro reopens direct roots and clears only its block-link markers
ok 3276 - Done Pomodoro reopens direct roots and clears only its block-link markers
  ---
  duration_ms: 4.593576
  ...
# Subtest: Done Pomodoro reopen restores its own block reference after reopening direct roots
ok 3277 - Done Pomodoro reopen restores its own block reference after reopening direct roots
  ---
  duration_ms: 1.131609
  ...
# Subtest: Done Pomodoro markers remain when the Todo transition does not occur
ok 3278 - Done Pomodoro markers remain when the Todo transition does not occur
  ---
  duration_ms: 0.385355
  ...
# Subtest: registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
ok 3279 - registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
  ---
  duration_ms: 14.560827
  ...
# Subtest: registered Ctrl+Enter immediately recovers a same-file dependent
ok 3280 - registered Ctrl+Enter immediately recovers a same-file dependent
  ---
  duration_ms: 10.206118
  ...
# Subtest: registered Ctrl+Enter immediately recovers a cross-file dependent
ok 3281 - registered Ctrl+Enter immediately recovers a cross-file dependent
  ---
  duration_ms: 2.880587
  ...
# Subtest: child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
ok 3282 - child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
  ---
  duration_ms: 3.546349
  ...
# Subtest: Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
ok 3283 - Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
  ---
  duration_ms: 1.352712
  ...
# Subtest: selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
ok 3284 - selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
  ---
  duration_ms: 2.834018
  ...
# Subtest: selected unresolved or excluded embedded children are consumed as no-ops
ok 3285 - selected unresolved or excluded embedded children are consumed as no-ops
  ---
  duration_ms: 1.274863
  ...
# Subtest: Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
ok 3286 - Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
  ---
  duration_ms: 3.110275
  ...
# Subtest: Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
ok 3287 - Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
  ---
  duration_ms: 2.654946
  ...
# Subtest: Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
ok 3288 - Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
  ---
  duration_ms: 0.817891
  ...
# Subtest: Pomodoro Work Log note-group collection scopes to direct children and requires descendants
ok 3289 - Pomodoro Work Log note-group collection scopes to direct children and requires descendants
  ---
  duration_ms: 0.792012
  ...
# Subtest: Work Log entry body formats as *date* — summary
ok 3290 - Work Log entry body formats as *date* — summary
  ---
  duration_ms: 0.131651
  ...
# Subtest: buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
ok 3291 - buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
  ---
  duration_ms: 0.222484
  ...
# Subtest: planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
ok 3292 - planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
  ---
  duration_ms: 0.335541
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
ok 3293 - planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
  ---
  duration_ms: 0.295945
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
ok 3294 - planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
  ---
  duration_ms: 0.187488
  ...
# Subtest: planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
ok 3295 - planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
  ---
  duration_ms: 0.441212
  ...
# Subtest: planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
ok 3296 - planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
  ---
  duration_ms: 0.383812
  ...
# Subtest: full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
ok 3297 - full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
  ---
  duration_ms: 6.440612
  ...
# Subtest: full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
ok 3298 - full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
  ---
  duration_ms: 1.495233
  ...
# Subtest: full Pomodoro completion keeps two same-task Work Log note sets in source order
ok 3299 - full Pomodoro completion keeps two same-task Work Log note sets in source order
  ---
  duration_ms: 1.134455
  ...
# Subtest: full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
ok 3300 - full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
  ---
  duration_ms: 0.824854
  ...
# Subtest: full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
ok 3301 - full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
  ---
  duration_ms: 0.856995
  ...
# Subtest: full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
ok 3302 - full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
  ---
  duration_ms: 0.563035
  ...
# Subtest: PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
ok 3303 - PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
  ---
  duration_ms: 2.101861
  ...
# Subtest: PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
ok 3304 - PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
  ---
  duration_ms: 1.062918
  ...
# Subtest: PP1 links the emptied project's ^prj as Next and strips \#hide
ok 3305 - PP1 links the emptied project's ^prj as Next and strips \#hide
  ---
  duration_ms: 9.192814
  ...
# Subtest: PP29 closing a child ^prj pulls in its empty parent project
ok 3306 - PP29 closing a child ^prj pulls in its empty parent project
  ---
  duration_ms: 1.992742
  ...
# Subtest: PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
ok 3307 - PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
  ---
  duration_ms: 1.129716
  ...
# Subtest: PP30 keeps the parent untouched while another child or task remains
ok 3308 - PP30 keeps the parent untouched while another child or task remains
  ---
  duration_ms: 0.893084
  ...
# Subtest: PP31 skips missing, ambiguous, and non-project parents
ok 3309 - PP31 skips missing, ambiguous, and non-project parents
  ---
  duration_ms: 1.145306
  ...
# Subtest: PP33 cancellation surfaces the parent without linking it
ok 3310 - PP33 cancellation surfaces the parent without linking it
  ---
  duration_ms: 2.297845
  ...
# Subtest: PP2 and PP3 leave a project with remaining work alone
ok 3311 - PP2 and PP3 leave a project with remaining work alone
  ---
  duration_ms: 1.557863
  ...
# Subtest: PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
ok 3312 - PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
  ---
  duration_ms: 2.522053
  ...
# Subtest: PP6 Sub-projects marker states match display_for_wikilink
ok 3313 - PP6 Sub-projects marker states match display_for_wikilink
  ---
  duration_ms: 1.271587
  ...
# Subtest: PP7 and PP28 keep a future-scheduled ^prj byte-identical
ok 3314 - PP7 and PP28 keep a future-scheduled ^prj byte-identical
  ---
  duration_ms: 0.945535
  ...
# Subtest: PP8 still-blocks a ^prj that waits on another open prerequisite
ok 3315 - PP8 still-blocks a ^prj that waits on another open prerequisite
  ---
  duration_ms: 0.644921
  ...
# Subtest: PP9 already-planned ^prj raises to Next without a new link
ok 3316 - PP9 already-planned ^prj raises to Next without a new link
  ---
  duration_ms: 0.578434
  ...
# Subtest: PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
ok 3317 - PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
  ---
  duration_ms: 1.987342
  ...
# Subtest: PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
ok 3318 - PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
  ---
  duration_ms: 0.845072
  ...
# Subtest: PP14 an id-less last task still pulls in
ok 3319 - PP14 an id-less last task still pulls in
  ---
  duration_ms: 0.450861
  ...
# Subtest: PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
ok 3320 - PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
  ---
  duration_ms: 10.187653
  ...
# Subtest: PP17 one pull-in row wins over project_task
ok 3321 - PP17 one pull-in row wins over project_task
  ---
  duration_ms: 0.651203
  ...
# Subtest: PP18 cancel recovers only
ok 3322 - PP18 cancel recovers only
  ---
  duration_ms: 0.448836
  ...
# Subtest: PP20 unrecognised or unplannable notes never pull in
ok 3323 - PP20 unrecognised or unplannable notes never pull in
  ---
  duration_ms: 1.209107
  ...
# Subtest: PP24 closing an external prerequisite pulls in only when N is empty
ok 3324 - PP24 closing an external prerequisite pulls in only when N is empty
  ---
  duration_ms: 0.943431
  ...
# Subtest: PP25 cascades project_member recovery after a [?] pull-in
ok 3325 - PP25 cascades project_member recovery after a [?] pull-in
  ---
  duration_ms: 1.127251
  ...
# Subtest: PP26 dated recount treats a hidden leftover as remaining work
ok 3326 - PP26 dated recount treats a hidden leftover as remaining work
  ---
  duration_ms: 1.50356
  ...
# Subtest: PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
ok 3327 - PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
  ---
  duration_ms: 1.315831
  ...
# Subtest: successorNoticeText uses the §12.6 pull-in and surfaced copy
ok 3328 - successorNoticeText uses the §12.6 pull-in and surfaced copy
  ---
  duration_ms: 0.621846
  ...
# Subtest: Ctrl+Enter on the last task link inserts the ^prj and rewrites R
ok 3329 - Ctrl+Enter on the last task link inserts the ^prj and rewrites R
  ---
  duration_ms: 13.922139
  ...
# Subtest: PP29 runtime close and reopen use the parent pull-in receipt
ok 3330 - PP29 runtime close and reopen use the parent pull-in receipt
  ---
  duration_ms: 6.834544
  ...
# Subtest: PP18 Alt+[ cancel of the last task surfaces R without linking
ok 3331 - PP18 Alt+[ cancel of the last task surfaces R without linking
  ---
  duration_ms: 21.412022
  ...
# Subtest: PP19 same-day reopen restores R byte-for-byte and takes back the link
ok 3332 - PP19 same-day reopen restores R byte-for-byte and takes back the link
  ---
  duration_ms: 3.75629
  ...
# Subtest: a close in a project that still has work stays inside the gate
ok 3333 - a close in a project that still has work stays inside the gate
  ---
  duration_ms: 1.224066
  ...
# Subtest: P1 path-qualified skip keys: same ^review in another note does not suppress
ok 3334 - P1 path-qualified skip keys: same ^review in another note does not suppress
  ---
  duration_ms: 0.881372
  ...
# Subtest: P3 id-less cascade: stale [?] R recovers resident without [id::]
ok 3335 - P3 id-less cascade: stale [?] R recovers resident without [id::]
  ---
  duration_ms: 1.835382
  ...
# Subtest: P4 frontmatter scheduled validity mirrors Rust
ok 3336 - P4 frontmatter scheduled validity mirrors Rust
  ---
  duration_ms: 0.655621
  ...
# Subtest: P5 recognition mirrors Rust (status/type/prj line)
ok 3337 - P5 recognition mirrors Rust (status/type/prj line)
  ---
  duration_ms: 1.908252
  ...
# Subtest: P6 SUBOPEN blank line stops the marker scan (PP6)
ok 3338 - P6 SUBOPEN blank line stops the marker scan (PP6)
  ---
  duration_ms: 0.567262
  ...
# Subtest: promotion prompts default to Tasks in ordinary and project notes
ok 3339 - promotion prompts default to Tasks in ordinary and project notes
  ---
  duration_ms: 5.495908
  ...
# Subtest: promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
ok 3340 - promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
  ---
  duration_ms: 1.237572
  ...
# Subtest: promotion command writes only on accept and Enter selects Tasks
ok 3341 - promotion command writes only on accept and Enter selects Tasks
  ---
  duration_ms: 2.877212
  ...
# Subtest: promotion removes only genuinely empty source sections
ok 3342 - promotion removes only genuinely empty source sections
  ---
  duration_ms: 1.268902
  ...
# Subtest: promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
ok 3343 - promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
  ---
  duration_ms: 1.106171
  ...
# Subtest: Tasks-only preamble promotions prompt and blank Enter moves into Tasks
ok 3344 - Tasks-only preamble promotions prompt and blank Enter moves into Tasks
  ---
  duration_ms: 0.807491
  ...
# Subtest: plain bullets already in Tasks prompt and blank Enter promotes in place
ok 3345 - plain bullets already in Tasks prompt and blank Enter promotes in place
  ---
  duration_ms: 0.980862
  ...
# Subtest: promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
ok 3346 - promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
  ---
  duration_ms: 0.520814
  ...
# Subtest: always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
ok 3347 - always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
  ---
  duration_ms: 3.811243
  ...
# Could not restore all reopened task references [ 'Broken.md: unreadable' ]
# Could not recover all blocked dependents [
#   'BrokenRead.md: read failed',
#   'Stale.md: line 1 changed before recovery',
#   'BrokenWrite.md: write failed'
# ]
# Subtest: direct Done Tasks task reopens through the metadata-aware fallback
ok 3348 - direct Done Tasks task reopens through the metadata-aware fallback
  ---
  duration_ms: 2.129524
  ...
# Subtest: recursive completion status policy includes Next without broadening excluded statuses
ok 3349 - recursive completion status policy includes Next without broadening excluded statuses
  ---
  duration_ms: 0.262461
  ...
# Subtest: recursive completion closes a Next root and its nested Next descendant
ok 3350 - recursive completion closes a Next root and its nested Next descendant
  ---
  duration_ms: 3.535617
  ...
# Subtest: recursive completion traverses Done parents and skips excluded siblings
ok 3351 - recursive completion traverses Done parents and skips excluded siblings
  ---
  duration_ms: 1.101141
  ...
# Subtest: closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
ok 3352 - closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
  ---
  duration_ms: 1.598701
  ...
# Subtest: reopened-reference restoration is ancestry-aware, conservative, and idempotent
ok 3353 - reopened-reference restoration is ancestry-aware, conservative, and idempotent
  ---
  duration_ms: 1.473944
  ...
# Subtest: retirement preserves task-tree markers and unmarks Pomodoro embeds
ok 3354 - retirement preserves task-tree markers and unmarks Pomodoro embeds
  ---
  duration_ms: 0.430451
  ...
# Subtest: done Pomodoro retirement removes only the matching embedded marker
ok 3355 - done Pomodoro retirement removes only the matching embedded marker
  ---
  duration_ms: 0.298419
  ...
# Subtest: retirement stops at prose boundaries and pairs strikethrough spans
ok 3356 - retirement stops at prose boundaries and pairs strikethrough spans
  ---
  duration_ms: 0.444418
  ...
# Subtest: retired Pomodoro links are not copied into the next Pomodoro
ok 3357 - retired Pomodoro links are not copied into the next Pomodoro
  ---
  duration_ms: 1.445699
  ...
# Subtest: retirement coordinator rewrites active editor and vault notes together
ok 3358 - retirement coordinator rewrites active editor and vault notes together
  ---
  duration_ms: 1.014156
  ...
# Subtest: restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
ok 3359 - restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
  ---
  duration_ms: 1.337071
  ...
# Subtest: close and reopen reference mutations share one serialized queue
ok 3360 - close and reopen reference mutations share one serialized queue
  ---
  duration_ms: 0.267962
  ...
# Subtest: post-close finalizer runs one gated plan before reference retirement
ok 3361 - post-close finalizer runs one gated plan before reference retirement
  ---
  duration_ms: 0.510715
  ...
# Subtest: dependent recovery uses live editor buffers and preserves the cursor
ok 3362 - dependent recovery uses live editor buffers and preserves the cursor
  ---
  duration_ms: 3.07627
  ...
# Subtest: dependent recovery preserves successful siblings across stale and failed notes
ok 3363 - dependent recovery preserves successful siblings across stale and failed notes
  ---
  duration_ms: 1.485275
  ...
# Subtest: no-op vault transforms and irrelevant retirement files avoid process writes
ok 3364 - no-op vault transforms and irrelevant retirement files avoid process writes
  ---
  duration_ms: 0.317576
  ...
# Subtest: ambiguity scans and notices are cached while dependency identity lines stay stable
ok 3365 - ambiguity scans and notices are cached while dependency identity lines stay stable
  ---
  duration_ms: 0.52432
  ...
# Subtest: non-Vim open/done command finalizes the closed task identity
ok 3366 - non-Vim open/done command finalizes the closed task identity
  ---
  duration_ms: 0.406536
  ...
# Subtest: non-Vim open/done command restores the reopened task identity
ok 3367 - non-Vim open/done command restores the reopened task identity
  ---
  duration_ms: 1.055054
  ...
# Subtest: full Pomodoro completion retires embeds only after carry-forward planning
ok 3368 - full Pomodoro completion retires embeds only after carry-forward planning
  ---
  duration_ms: 5.215342
  ...
# Subtest: full Pomodoro completion recovers after a deduplicated multi-target batch
ok 3369 - full Pomodoro completion recovers after a deduplicated multi-target batch
  ---
  duration_ms: 7.664107
  ...
# Subtest: full Pomodoro completion moves a marked same-note link without history
ok 3370 - full Pomodoro completion moves a marked same-note link without history
  ---
  duration_ms: 0.830785
  ...
# Subtest: cycler LK1–LK19 recognises only relation line shapes
ok 3371 - cycler LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 1.419369
  ...
# Subtest: cycler MC10, MC11, MC12 and MC14 keep relations inert while allowing root-only gestures
ok 3372 - cycler MC10, MC11, MC12 and MC14 keep relations inert while allowing root-only gestures
  ---
  duration_ms: 2.371836
  ...
# Subtest: SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
ok 3373 - SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
  ---
  duration_ms: 22.797787
  ...
# Subtest: SO2–SO5 fan-outs with explicit selection (SO32 twenty)
ok 3374 - SO2–SO5 fan-outs with explicit selection (SO32 twenty)
  ---
  duration_ms: 7.385644
  ...
# Subtest: SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
ok 3375 - SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
  ---
  duration_ms: 1.089048
  ...
# Subtest: SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
ok 3376 - SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
  ---
  duration_ms: 1.21008
  ...
# Subtest: SO stable keys survive insertions/status changes; ambiguous rebinding refused
ok 3377 - SO stable keys survive insertions/status changes; ambiguous rebinding refused
  ---
  duration_ms: 2.184408
  ...
# Subtest: SO picker model, pick normalization, and API detection
ok 3378 - SO picker model, pick normalization, and API detection
  ---
  duration_ms: 0.895539
  ...
# Subtest: SO notice copy for offers (SO20, mixed, failure)
ok 3379 - SO notice copy for offers (SO20, mixed, failure)
  ---
  duration_ms: 0.686339
  ...
# Subtest: destination override to an existing entry inserts as its child
ok 3380 - destination override to an existing entry inserts as its child
  ---
  duration_ms: 3.523023
  ...
# Subtest: destination override with a stale preimage skips loudly
ok 3381 - destination override with a stale preimage skips loudly
  ---
  duration_ms: 1.063339
  ...
# Subtest: destination override with a closed entry skips loudly
ok 3382 - destination override with a closed entry skips loudly
  ---
  duration_ms: 1.050936
  ...
# Subtest: destination override with a new name creates one placeholder after the running entry
ok 3383 - destination override with a new name creates one placeholder after the running entry
  ---
  duration_ms: 1.023353
  ...
# Subtest: destination override with a new name racing an open entry joins it
ok 3384 - destination override with a new name racing an open entry joins it
  ---
  duration_ms: 0.963489
  ...
# Subtest: reopen takes back the untouched successor link and restores status
ok 3385 - reopen takes back the untouched successor link and restores status
  ---
  duration_ms: 21.256055
  ...
# Subtest: an edited successor bullet survives while its status still restores
ok 3386 - an edited successor bullet survives while its status still restores
  ---
  duration_ms: 3.137377
  ...
# Subtest: an edited successor status line survives while its link is taken back
ok 3387 - an edited successor status line survives while its link is taken back
  ---
  duration_ms: 3.768864
  ...
# Subtest: reopen on a different day leaves successor links alone
ok 3388 - reopen on a different day leaves successor links alone
  ---
  duration_ms: 2.522063
  ...
# Subtest: reopening a task closed without a pass shows no take-back
ok 3389 - reopening a task closed without a pass shows no take-back
  ---
  duration_ms: 1.517977
  ...
# Subtest: Alt+] on a planned prerequisite links its successor
ok 3390 - Alt+] on a planned prerequisite links its successor
  ---
  duration_ms: 12.16196
  ...
# Subtest: take-back deletes a pre-existing entry it empties
ok 3391 - take-back deletes a pre-existing entry it empties
  ---
  duration_ms: 4.347386
  ...
# Subtest: take-back deletes a stub-replaced entry through the vault
ok 3392 - take-back deletes a stub-replaced entry through the vault
  ---
  duration_ms: 0.585647
  ...
# Subtest: take-back keeps entries that are closed or keep another child
ok 3393 - take-back keeps entries that are closed or keep another child
  ---
  duration_ms: 0.56079
  ...
# Subtest: closing-entry relocation finds a deferred-only placeholder
ok 3394 - closing-entry relocation finds a deferred-only placeholder
  ---
  duration_ms: 0.646133
  ...
# Subtest: Alt+[ into Cancelled recovers its dependents without linking
ok 3395 - Alt+[ into Cancelled recovers its dependents without linking
  ---
  duration_ms: 4.712753
  ...
# Subtest: take-back keeps an entry whose prose survives across a blank line (both paths)
ok 3396 - take-back keeps an entry whose prose survives across a blank line (both paths)
  ---
  duration_ms: 1.015117
  ...
# Subtest: take-back deletes a whole block with continuation/fence leftovers (LF/CRLF, final newline)
ok 3397 - take-back deletes a whole block with continuation/fence leftovers (LF/CRLF, final newline)
  ---
  duration_ms: 1.263551
  ...
# Subtest: link close links the unblocked successor into the slot and shows the nav card
ok 3398 - link close links the unblocked successor into the slot and shows the nav card
  ---
  duration_ms: 21.230176
  ...
# Subtest: close with no [id::] performs zero vault reads and shows nothing
ok 3399 - close with no [id::] performs zero vault reads and shows nothing
  ---
  duration_ms: 1.008815
  ...
# Subtest: Warm finalize reads no unrelated note bodies on the real close path
ok 3400 - Warm finalize reads no unrelated note bodies on the real close path
  ---
  duration_ms: 2.902089
  ...
# Subtest: cold fallback still recovers and links without a Tasks cache
ok 3401 - cold fallback still recovers and links without a Tasks cache
  ---
  duration_ms: 3.302252
  ...
# Subtest: recovered-only close reports unblocked without linking (SO4 Esc)
ok 3402 - recovered-only close reports unblocked without linking (SO4 Esc)
  ---
  duration_ms: 1.524659
  ...
# Subtest: walk landing composes a single toast and shows no card
ok 3403 - walk landing composes a single toast and shows no card
  ---
  duration_ms: 8.535871
  ...
# Subtest: nav absent falls back to a plain Notice with no link (SO missing picker)
ok 3404 - nav absent falls back to a plain Notice with no link (SO missing picker)
  ---
  duration_ms: 2.281974
  ...
# Subtest: stale cache heals via re-plan from fresh text (SO30)
ok 3405 - stale cache heals via re-plan from fresh text (SO30)
  ---
  duration_ms: 2.178497
  ...
# Subtest: Pomodoro-line close appends the successor to the created continuation
ok 3406 - Pomodoro-line close appends the successor to the created continuation
  ---
  duration_ms: 5.65397
  ...
# Subtest: Pomodoro-line close keeps the closing anchor after the picker re-plan
ok 3407 - Pomodoro-line close keeps the closing anchor after the picker re-plan
  ---
  duration_ms: 3.451857
  ...
# Subtest: completeTaskAtCursor returns the notice and shows nothing itself
ok 3408 - completeTaskAtCursor returns the notice and shows nothing itself
  ---
  duration_ms: 2.424266
  ...
# Subtest: successor apply recovers project residents without ledger v12
ok 3409 - successor apply recovers project residents without ledger v12
  ---
  duration_ms: 11.186048
  ...
# Subtest: SB vectors pin the successor mint pipeline
ok 3410 - SB vectors pin the successor mint pipeline
  ---
  duration_ms: 2.214255
  ...
# Subtest: successor suggester ports the Rust candidate and suffix rules
ok 3411 - successor suggester ports the Rust candidate and suffix rules
  ---
  duration_ms: 0.643088
  ...
# Subtest: successor link form names unique basenames short and the day file always
ok 3412 - successor link form names unique basenames short and the day file always
  ---
  duration_ms: 0.402358
  ...
# Subtest: tasksFromDocuments normalizes vault lines to pool shape
ok 3413 - tasksFromDocuments normalizes vault lines to pool shape
  ---
  duration_ms: 1.093937
  ...
# Subtest: normalizeTasksCacheTask ports every known Tasks shape
ok 3414 - normalizeTasksCacheTask ports every known Tasks shape
  ---
  duration_ms: 0.390204
  ...
# Subtest: buildDependentsIndex keeps first task IDs and groups dependents
ok 3415 - buildDependentsIndex keeps first task IDs and groups dependents
  ---
  duration_ms: 0.206324
  ...
# Subtest: findLiveLinks counts plain, embedded, and deferred links under open entries only
ok 3416 - findLiveLinks counts plain, embedded, and deferred links under open entries only
  ---
  duration_ms: 2.439697
  ...
# Subtest: computeSuccessorAnchors implements closing, slot, inherit, and none
ok 3417 - computeSuccessorAnchors implements closing, slot, inherit, and none
  ---
  duration_ms: 1.028593
  ...
# Subtest: SL1 links the successor right after the predecessor bullet
ok 3418 - SL1 links the successor right after the predecessor bullet
  ---
  duration_ms: 6.642526
  ...
# Subtest: SL3 still-blocked rows count the open prerequisites left
ok 3419 - SL3 still-blocked rows count the open prerequisites left
  ---
  duration_ms: 1.237902
  ...
# Subtest: SL4 future-scheduled dependents stay Blocked with the date row
ok 3420 - SL4 future-scheduled dependents stay Blocked with the date row
  ---
  duration_ms: 0.777623
  ...
# Subtest: SL5 already-planned dependents recover without a duplicate link
ok 3421 - SL5 already-planned dependents recover without a duplicate link
  ---
  duration_ms: 1.042109
  ...
# Subtest: SL6 struck and closed-entry links do not count as planned
ok 3422 - SL6 struck and closed-entry links do not count as planned
  ---
  duration_ms: 1.556901
  ...
# Subtest: SL7 closing anchors create the continuation placeholder
ok 3423 - SL7 closing anchors create the continuation placeholder
  ---
  duration_ms: 0.968668
  ...
# Subtest: SL8 closing anchors append after carried lines in the continuation
ok 3424 - SL8 closing anchors append after carried lines in the continuation
  ---
  duration_ms: 0.844952
  ...
# Subtest: SL9 unplanned predecessors offer at the implicit destination (SO14)
ok 3425 - SL9 unplanned predecessors offer at the implicit destination (SO14)
  ---
  duration_ms: 1.224146
  ...
# Subtest: SL10 missing block IDs mint through the SB rule
ok 3426 - SL10 missing block IDs mint through the SB rule
  ---
  duration_ms: 0.553627
  ...
# Subtest: SL11 project and hidden tasks recover but never link
ok 3427 - SL11 project and hidden tasks recover but never link
  ---
  duration_ms: 10.106688
  ...
# Subtest: PDC1 leaves a dependency-ready resident Blocked while its project still waits
ok 3428 - PDC1 leaves a dependency-ready resident Blocked while its project still waits
  ---
  duration_ms: 2.769375
  ...
# Subtest: PDC2 residents are offered under the project group (SO1)
ok 3429 - PDC2 residents are offered under the project group (SO1)
  ---
  duration_ms: 1.663224
  ...
# Subtest: PDC3 keeps a project resident Blocked when its own prerequisite remains open
ok 3430 - PDC3 keeps a project resident Blocked when its own prerequisite remains open
  ---
  duration_ms: 1.153411
  ...
# Subtest: PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
ok 3431 - PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
  ---
  duration_ms: 2.643705
  ...
# Subtest: SL12 one gesture closing two prerequisites links once with both causes
ok 3432 - SL12 one gesture closing two prerequisites links once with both causes
  ---
  duration_ms: 0.485287
  ...
# Subtest: SL13 chains do not recurse: the dependent's own dependents wait
ok 3433 - SL13 chains do not recurse: the dependent's own dependents wait
  ---
  duration_ms: 0.359306
  ...
# Subtest: SL14 ambiguous basenames link long
ok 3434 - SL14 ambiguous basenames link long
  ---
  duration_ms: 0.307377
  ...
# Subtest: SL15 stale open dependents link and become Next
ok 3435 - SL15 stale open dependents link and become Next
  ---
  duration_ms: 0.279334
  ...
# Subtest: SL16 gates on [id::]: no identity means no lookup and empty rows
ok 3436 - SL16 gates on [id::]: no identity means no lookup and empty rows
  ---
  duration_ms: 0.202226
  ...
# Subtest: SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
ok 3437 - SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
  ---
  duration_ms: 1.221231
  ...
# Subtest: SL18 the kill switch recovers without linking or minting
ok 3438 - SL18 the kill switch recovers without linking or minting
  ---
  duration_ms: 0.357272
  ...
# Subtest: SL19 re-applied closes write nothing and report nothing
ok 3439 - SL19 re-applied closes write nothing and report nothing
  ---
  duration_ms: 0.279534
  ...
# Subtest: SL23 subtasks anchor at their root's link
ok 3440 - SL23 subtasks anchor at their root's link
  ---
  duration_ms: 0.361019
  ...
# Subtest: SL24 later same-name entries take the closing successors
ok 3441 - SL24 later same-name entries take the closing successors
  ---
  duration_ms: 0.493572
  ...
# Subtest: SL25 already-Next planned dependents produce no row
ok 3442 - SL25 already-Next planned dependents produce no row
  ---
  duration_ms: 0.510654
  ...
# Subtest: SL26 inbox successors carry the inbox flag
ok 3443 - SL26 inbox successors carry the inbox flag
  ---
  duration_ms: 0.376318
  ...
# Subtest: SL27 dropped links are never re-linked and recover to Ready
ok 3444 - SL27 dropped links are never re-linked and recover to Ready
  ---
  duration_ms: 0.443085
  ...
# Subtest: SL28 day-file successors name the note, never the bare link
ok 3445 - SL28 day-file successors name the note, never the bare link
  ---
  duration_ms: 0.368754
  ...
# Subtest: slot insertions land after the anchor subtree with its indent
ok 3446 - slot insertions land after the anchor subtree with its indent
  ---
  duration_ms: 0.262851
  ...
# Subtest: closing insertions replace a lone stub child
ok 3447 - closing insertions replace a lone stub child
  ---
  duration_ms: 0.667463
  ...
# Subtest: insertions skip placements with no valid target
ok 3448 - insertions skip placements with no valid target
  ---
  duration_ms: 0.207586
  ...
# Subtest: successorNoticeText implements the §12.6 table
ok 3449 - successorNoticeText implements the §12.6 table
  ---
  duration_ms: 0.679858
  ...
# Subtest: parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
ok 3450 - parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
  ---
  duration_ms: 0.479084
  ...
# Subtest: loadLinkUnblocked stat-caches the config read
ok 3451 - loadLinkUnblocked stat-caches the config read
  ---
  duration_ms: 0.318207
  ...
# Subtest: loadLinkUnblocked treats missing or unreadable config as true
ok 3452 - loadLinkUnblocked treats missing or unreadable config as true
  ---
  duration_ms: 1.40444
  ...
# Subtest: successorPlanConfigPath honors XDG_CONFIG_HOME
ok 3453 - successorPlanConfigPath honors XDG_CONFIG_HOME
  ---
  duration_ms: 0.191365
  ...
# Subtest: todayDailyPath mirrors the ledger daily path
ok 3454 - todayDailyPath mirrors the ledger daily path
  ---
  duration_ms: 0.581199
  ...
# Subtest: normalizeClosedTaskIdentities keeps the anchor root off the match gate
ok 3455 - normalizeClosedTaskIdentities keeps the anchor root off the match gate
  ---
  duration_ms: 0.231702
  ...
# Subtest: ID-less planned roots anchor ID-bearing children without minting IDs
ok 3456 - ID-less planned roots anchor ID-bearing children without minting IDs
  ---
  duration_ms: 0.753729
  ...
# Subtest: successor anchors never guess across roots
ok 3457 - successor anchors never guess across roots
  ---
  duration_ms: 0.386738
  ...
# Subtest: a child with its own live link keeps its own slot
ok 3458 - a child with its own live link keeps its own slot
  ---
  duration_ms: 0.348886
  ...
# Subtest: getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
ok 3459 - getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
  ---
  duration_ms: 0.263412
  ...
# Subtest: countSuccessorBasenames walks the vault set, not the task set
ok 3460 - countSuccessorBasenames walks the vault set, not the task set
  ---
  duration_ms: 0.3249
  ...
# Subtest: the pass threads a richer isInbox into unblocked rows
ok 3461 - the pass threads a richer isInbox into unblocked rows
  ---
  duration_ms: 0.343866
  ...
# Subtest: getTaskLinkLaneApi returns the lane only when version and both functions exist
ok 3462 - getTaskLinkLaneApi returns the lane only when version and both functions exist
  ---
  duration_ms: 1.015037
  ...
# Subtest: isTaskLinkLaneLine passes content, line, and path and never throws
ok 3463 - isTaskLinkLaneLine passes content, line, and path and never throws
  ---
  duration_ms: 1.043652
  ...
# Subtest: single Alt+] on a Task Link delegates with exactly { editor, view }
ok 3464 - single Alt+] on a Task Link delegates with exactly { editor, view }
  ---
  duration_ms: 0.492711
  ...
# Subtest: Alt+[ and Alt+] delegate identically; direction is ignored
ok 3465 - Alt+[ and Alt+] delegate identically; direction is ignored
  ---
  duration_ms: 0.302397
  ...
# Subtest: embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
ok 3466 - embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
  ---
  duration_ms: 0.292238
  ...
# Subtest: entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
ok 3467 - entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
  ---
  duration_ms: 2.734448
  ...
# Subtest: counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
ok 3468 - counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
  ---
  duration_ms: 0.615655
  ...
# Subtest: counted dispatch without an explicit repeat leaves the key alone
ok 3469 - counted dispatch without an explicit repeat leaves the key alone
  ---
  duration_ms: 0.200714
  ...
# Subtest: counted range starting elsewhere skips Task Link lines
ok 3470 - counted range starting elsewhere skips Task Link lines
  ---
  duration_ms: 1.736845
  ...
# Subtest: legacy fallback with no api keeps today's behavior
ok 3471 - legacy fallback with no api keeps today's behavior
  ---
  duration_ms: 0.677353
  ...
# Subtest: plain Task Link in an open Pomodoro closes the task root-only and strikes the link
ok 3472 - plain Task Link in an open Pomodoro closes the task root-only and strikes the link
  ---
  duration_ms: 14.318716
  ...
# Subtest: marked plain Task Link drops its marker when struck under Pomodoro ancestry
ok 3473 - marked plain Task Link drops its marker when struck under Pomodoro ancestry
  ---
  duration_ms: 1.535661
  ...
# Subtest: plain Pomodoro Task Link closes root-only while embedded closes recursively
ok 3474 - plain Pomodoro Task Link closes root-only while embedded closes recursively
  ---
  duration_ms: 2.249052
  ...
# Subtest: embedded Pomodoro Task Link still closes recursively and retires to struck form
ok 3475 - embedded Pomodoro Task Link still closes recursively and retires to struck form
  ---
  duration_ms: 2.501453
  ...
# Subtest: Ctrl+Enter toggles a struck plain Pomodoro link back to open
ok 3476 - Ctrl+Enter toggles a struck plain Pomodoro link back to open
  ---
  duration_ms: 1.790627
  ...
# Subtest: same-file plain Task Link closes and strikes the correct line
ok 3477 - same-file plain Task Link closes and strikes the correct line
  ---
  duration_ms: 1.32613
  ...
# Subtest: cursor selects which of several Task Links closes and strikes
ok 3478 - cursor selects which of several Task Links closes and strikes
  ---
  duration_ms: 1.558775
  ...
# Subtest: plain links to Blocked or non-task blocks still complete the Pomodoro
ok 3479 - plain links to Blocked or non-task blocks still complete the Pomodoro
  ---
  duration_ms: 3.921925
  ...
# Subtest: strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
ok 3480 - strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
  ---
  duration_ms: 0.531344
  ...
# Subtest: completeTaskAtCursor closes each open symbol through the Tasks command
ok 3481 - completeTaskAtCursor closes each open symbol through the Tasks command
  ---
  duration_ms: 1.701637
  ...
# Subtest: completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
ok 3482 - completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
  ---
  duration_ms: 0.356079
  ...
# Subtest: completeTaskAtCursor refuses closed, cancelled, and non-task lines
ok 3483 - completeTaskAtCursor refuses closed, cancelled, and non-task lines
  ---
  duration_ms: 0.341362
  ...
# Subtest: completeTaskAtCursor refuses a missing Tasks command with no write
ok 3484 - completeTaskAtCursor refuses a missing Tasks command with no write
  ---
  duration_ms: 0.175565
  ...
# Subtest: Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
ok 3485 - Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
  ---
  duration_ms: 0.537666
  ...
# Subtest: completeTaskAtCursor reports not-closed when Tasks does not write [x]
ok 3486 - completeTaskAtCursor reports not-closed when Tasks does not write [x]
  ---
  duration_ms: 0.175755
  ...
# Subtest: recovery api is frozen at version 2 and recovers without striking references
ok 3487 - recovery api is frozen at version 2 and recovers without striking references
  ---
  duration_ms: 2.650207
  ...
# Subtest: recovery api never throws and reports failures
ok 3488 - recovery api never throws and reports failures
  ---
  duration_ms: 0.245598
  ...
# Subtest: future-scheduled dependents stay Blocked on the planner, api, and close paths
ok 3489 - future-scheduled dependents stay Blocked on the planner, api, and close paths
  ---
  duration_ms: 15.671158
  ...
# Subtest: Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
ok 3490 - Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
  ---
  duration_ms: 4.455813
  ...
# Subtest: every printable non-space ASCII key resolves to a surround pair
ok 3491 - every printable non-space ASCII key resolves to a surround pair
  ---
  duration_ms: 3.259361
  ...
# Subtest: visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
ok 3492 - visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
  ---
  duration_ms: 0.590858
  ...
# Subtest: non-visible, combining, multi-character, and multi-code-unit values are rejected
ok 3493 - non-visible, combining, multi-character, and multi-code-unit values are rejected
  ---
  duration_ms: 0.228055
  ...
# Subtest: ys adds broad symmetric delimiters through pending keydown
ok 3494 - ys adds broad symmetric delimiters through pending keydown
  ---
  duration_ms: 1.133453
  ...
# Subtest: rejected keydown input never edits or leaks into a pending ys
ok 3495 - rejected keydown input never edits or leaks into a pending ys
  ---
  duration_ms: 0.356471
  ...
# Subtest: Escape cancels ys, cs, and ds pending state without editing
ok 3496 - Escape cancels ys, cs, and ds pending state without editing
  ---
  duration_ms: 0.25633
  ...
# Subtest: cs accepts broad target and replacement characters independently
ok 3497 - cs accepts broad target and replacement characters independently
  ---
  duration_ms: 1.621294
  ...
# Subtest: cs preserves structural alias and padding rules
ok 3498 - cs preserves structural alias and padding rules
  ---
  duration_ms: 0.507258
  ...
# Subtest: cs replaces repeated symmetric runs exactly once on each side
ok 3499 - cs replaces repeated symmetric runs exactly once on each side
  ---
  duration_ms: 0.50303
  ...
# Subtest: ds removes representative broad symmetric delimiters
ok 3500 - ds removes representative broad symmetric delimiters
  ---
  duration_ms: 0.714935
  ...
# Subtest: ds preserves structural alias and padding rules
ok 3501 - ds preserves structural alias and padding rules
  ---
  duration_ms: 0.307467
  ...
# Subtest: ds removes one pair from repeated runs, including the reported block link
ok 3502 - ds removes one pair from repeated runs, including the reported block link
  ---
  duration_ms: 1.118935
  ...
# Subtest: consecutive ds commands peel a triple symmetric surround
ok 3503 - consecutive ds commands peel a triple symmetric surround
  ---
  duration_ms: 0.221372
  ...
# Subtest: symmetric discovery uses deterministic sequential same-line run pairs
ok 3504 - symmetric discovery uses deterministic sequential same-line run pairs
  ---
  duration_ms: 0.146189
  ...
# Subtest: symmetric discovery includes every character in repeated boundaries
ok 3505 - symmetric discovery includes every character in repeated boundaries
  ---
  duration_ms: 0.263182
  ...
# Subtest: unpaired and unequal symmetric runs are safe no-ops
ok 3506 - unpaired and unequal symmetric runs are safe no-ops
  ---
  duration_ms: 0.227885
  ...
# Subtest: ordinary normal-mode keys remain untouched outside pending state
ok 3507 - ordinary normal-mode keys remain untouched outside pending state
  ---
  duration_ms: 0.179522
  ...
# Subtest: dot while a surround is pending is a literal delimiter, not repeat
ok 3508 - dot while a surround is pending is a literal delimiter, not repeat
  ---
  duration_ms: 0.113997
  ...
# Subtest: dot-repeat records and replays broad-character ys
ok 3509 - dot-repeat records and replays broad-character ys
  ---
  duration_ms: 0.236962
  ...
# Subtest: dot-repeat records and replays broad-character cs
ok 3510 - dot-repeat records and replays broad-character cs
  ---
  duration_ms: 0.187257
  ...
# Subtest: dot-repeat records and replays broad-character ds
ok 3511 - dot-repeat records and replays broad-character ds
  ---
  duration_ms: 0.176728
  ...
# Subtest: dot-repeat replays cs against repeated symmetric runs
ok 3512 - dot-repeat replays cs against repeated symmetric runs
  ---
  duration_ms: 0.196956
  ...
# Subtest: dot-repeat replays ds against repeated symmetric runs
ok 3513 - dot-repeat replays ds against repeated symmetric runs
  ---
  duration_ms: 0.19925
  ...
# Subtest: consecutive dot-repeats peel a triple symmetric surround
ok 3514 - consecutive dot-repeats peel a triple symmetric surround
  ---
  duration_ms: 0.228286
  ...
1..3514
# tests 3529
# suites 0
# pass 3529
# fail 0
# cancelled 0
# skipped 0
# todo 0
# duration_ms 7280.959801
succeeded  exit=0  duration=15924ms

