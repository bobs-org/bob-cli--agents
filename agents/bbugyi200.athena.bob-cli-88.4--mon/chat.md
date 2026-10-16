# Chat History - ace-run (bob-cli-88.4--mon)

- **TIMESTAMP:** 2026-10-16 08:24:44 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-88.4--mon

## Prompt

sase monitor start --command 'npm test && bob plugins sync --no-pull -r /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins' --reason 'Run the full bob-plugins test suite and deploy all plugins after the docs update'

## Response

sase tool run 2df7921db4f75dc9b2280b22227ed24e

> bob-plugins@0.1.0 test
> node scripts/build-plugins.mjs --check && node --test scripts/test-dependency-line-migration.cjs scripts/test-navigation-hotkeys-section-nav.cjs scripts/test-navigation-hotkeys-rename.cjs scripts/test-navigation-hotkeys-schedule-recovery.cjs scripts/test-navigation-hotkeys-schedule-properties.cjs scripts/test-navigation-hotkeys-schedule-writes.cjs scripts/test-navigation-hotkeys-runtime-schedule.cjs scripts/test-navigation-hotkeys-dependencies.cjs scripts/test-navigation-blocks-guards.cjs scripts/test-navigation-blocks-writers.cjs scripts/test-navigation-hotkeys-dependency-mirror.cjs scripts/test-navigation-hotkeys-task-move-plan.cjs scripts/test-navigation-hotkeys-priority-notice.cjs scripts/test-navigation-successor-picker.cjs scripts/test-navigation-hotkeys-unblocked-notice.cjs scripts/test-navigation-project-blocking.cjs scripts/test-navigation-project-dependency-stage.cjs scripts/test-navigation-project-subprojects.cjs scripts/test-navigation-project-subtree-gestures.cjs scripts/test-navigation-hotkeys-priority-picker.cjs scripts/test-navigation-hotkeys-picker-lifecycle.cjs scripts/test-navigation-hotkeys-ref-picker-text.cjs scripts/test-navigation-hotkeys-pomodoro-move-pickers.cjs scripts/test-navigation-inbox-route.cjs scripts/test-navigation-inbox-route-card.cjs scripts/test-navigation-hotkeys-task-move.cjs scripts/test-navigation-goto-task-uri.cjs scripts/test-navigation-hotkeys-open-task-jump.cjs scripts/test-navigation-hotkeys-vim-counts.cjs scripts/test-navigation-hotkeys-tab-pin.cjs scripts/test-navigation-hotkeys-schedule-log.cjs scripts/test-navigation-hotkeys-schedule-review.cjs scripts/test-navigation-hotkeys-deferred-pomodoro.cjs scripts/test-navigation-hotkeys-pomodoro-parse.cjs scripts/test-navigation-hotkeys-pomodoro-bullet-move.cjs scripts/test-navigation-hotkeys-pomodoro-split-rename.cjs scripts/test-navigation-hotkeys-pomodoro-reorder.cjs scripts/test-navigation-hotkeys-runtime-prune.cjs scripts/test-navigation-hotkeys-project-from-task.cjs scripts/test-navigation-hotkeys-project-reversal.cjs scripts/test-navigation-hotkeys-link-picker.cjs scripts/test-navigation-hotkeys-lane-toggle.cjs scripts/test-navigation-hotkeys-task-link-lane.cjs scripts/test-navigation-hotkeys-cancel-log.cjs scripts/test-navigation-hotkeys-cancel-task.cjs scripts/test-navigation-hotkeys-forward-promotion.cjs scripts/test-navigation-hotkeys-schedule-work-log.cjs scripts/test-navigation-hotkeys-task-move-history.cjs scripts/test-navigation-jump-history.cjs scripts/test-navigation-dependencies.cjs scripts/test-navigation-roll-decay.cjs scripts/test-navigation-decay-planner.cjs scripts/test-navigation-task-card-model.cjs scripts/test-navigation-task-card-view.cjs scripts/test-navigation-task-card-schedule.cjs scripts/test-navigation-task-card-review.cjs scripts/test-navigation-decision-card.cjs scripts/test-navigation-decision-card-handlers.cjs scripts/test-navigation-refresh-modal.cjs scripts/test-navigation-freshness.cjs scripts/test-navigation-stamps.cjs scripts/test-navigation-keep-counting.cjs scripts/test-navigation-checklist.cjs scripts/test-navigation-review-advance.cjs scripts/test-navigation-review-advance-gestures.cjs scripts/test-navigation-checklist-ctrl-enter.cjs scripts/test-ledger-tools-navigation.cjs scripts/test-ledger-tools-plan-budget.cjs scripts/test-ledger-tools-ready-badge.cjs scripts/test-ledger-tools-note-ready.cjs scripts/test-ledger-tools-note-ready-views.cjs scripts/test-ledger-tools-dashboard-parity.cjs scripts/test-ledger-tools-work-badge-tone.cjs scripts/test-ledger-tools-dashboard-collections.cjs scripts/test-ledger-tools-today.cjs scripts/test-ledger-tools-freshness-placement.cjs scripts/test-ledger-tools-freshness-states.cjs scripts/test-ledger-tools-freshness-namespace.cjs scripts/test-ledger-tools-freshness-review-model.cjs scripts/test-ledger-tools-freshness-queue.cjs scripts/test-ledger-tools-freshness-tracking.cjs scripts/test-ledger-tools-freshness-footer.cjs scripts/test-ledger-tools-freshness-recurring.cjs scripts/test-ledger-tools-freshness-mark.cjs scripts/test-ledger-tools-freshness-mark-surfaces.cjs scripts/test-ledger-tools-priority-marks.cjs scripts/test-ledger-tools-task-tag-marks.cjs scripts/test-ledger-tools-unblocked-glyph.cjs scripts/test-ledger-tools-progress-marks.cjs scripts/test-ledger-tools-date-marks.cjs scripts/test-ledger-tools-date-marks-tasks.cjs scripts/test-ledger-tools-freshness-keeps.cjs scripts/test-ledger-tools-freshness-unblocked.cjs scripts/test-ledger-tools-freshness-decision-card.cjs scripts/test-ledger-tools-dependency-chips.cjs scripts/test-ledger-tools-blocks-chips.cjs scripts/test-ledger-tools-snippets.cjs scripts/test-ledger-tools-vim-mappings.cjs scripts/test-task-status-cycler-dependencies.cjs scripts/test-task-status-cycler-blocks-guards.cjs scripts/test-task-status-cycler-ctrl-enter.cjs scripts/test-task-status-cycler-reference-lifecycle.cjs scripts/test-task-status-cycler-pomodoro-completion.cjs scripts/test-task-status-cycler-pomodoro-work-log.cjs scripts/test-task-status-cycler-pomodoro-reopen.cjs scripts/test-task-status-cycler-blocked-schedule.cjs scripts/test-task-status-cycler-demotion-picker.cjs scripts/test-task-status-cycler-promotion.cjs scripts/test-task-status-cycler-counted-toggle.cjs scripts/test-task-status-cycler-successors.cjs scripts/test-task-status-cycler-successor-wiring.cjs scripts/test-task-status-cycler-successor-polish.cjs scripts/test-task-status-cycler-successor-offers.cjs scripts/test-task-status-cycler-project-pull-in.cjs scripts/test-task-status-cycler-task-links-api.cjs scripts/test-task-status-cycler-task-link-lane.cjs scripts/test-task-status-cycler-freshness.cjs scripts/test-block-id-prompt-dependencies.cjs scripts/test-block-id-prompt-blocks-guards.cjs scripts/test-block-id-prompt-ref-picker-text.cjs scripts/test-block-id-prompt-markers.cjs scripts/test-block-id-prompt-pomodoro-context.cjs scripts/test-block-id-prompt-target-update.cjs scripts/test-block-id-prompt-pomodoro-insertion.cjs scripts/test-block-id-prompt-pomodoro-targets.cjs scripts/test-block-id-prompt-pomodoro-picker-view.cjs scripts/test-block-id-prompt-pomodoro-picker-runtime.cjs scripts/test-block-id-prompt-work-log.cjs scripts/test-block-id-prompt-pomodoro-link-runtime.cjs scripts/test-block-id-prompt-pomodoro-link-picker-api.cjs scripts/test-block-id-prompt-pomodoro-unlink-runtime.cjs scripts/test-block-id-prompt-task-link-deletion.cjs scripts/test-block-id-prompt-plan-budget-and-freshness.cjs scripts/test-prompt-block-id-naming.cjs scripts/test-block-id-prompt-prefill.cjs scripts/test-vim-surround.cjs scripts/test-navigation-dependencies-stage-ranker-and-pool.cjs scripts/test-navigation-dependencies-stage-entry-and-view.cjs scripts/test-navigation-dependencies-stage-writes.cjs scripts/test-navigation-dependencies-stage-mirror-and-badge.cjs scripts/test-navigation-dependencies-stage-stale-guards.cjs scripts/test-navigation-dependencies-stage-performance.cjs scripts/test-navigation-prompt-block-id-stage.cjs scripts/test-navigation-dependencies-writer.cjs scripts/test-navigation-dependency-link-consumption.cjs scripts/test-plugin-build.cjs scripts/test-ledger-tools-stats-journal.cjs scripts/test-ledger-tools-stats-data.cjs scripts/test-ledger-tools-stats-block.cjs scripts/test-ledger-tools-stats-charts.cjs scripts/test-navigation-review-journal.cjs scripts/test-ledger-tools-stats-panels.cjs

  checked   block-id-prompt
  checked   bob-ledger-tools
  checked   bob-navigation-hotkeys
  checked   task-status-cycler
TAP version 13
# Subtest: bip BK1–BK12 accept and empty
ok 1 - bip BK1–BK12 accept and empty
  ---
  duration_ms: 1.127974
  ...
# Subtest: bip BK13–BK15 malformed split mirrors the Depends-On twin
ok 2 - bip BK13–BK15 malformed split mirrors the Depends-On twin
  ---
  duration_ms: 0.358173
  ...
# Subtest: bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
ok 3 - bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
  ---
  duration_ms: 0.168031
  ...
# Subtest: bip MC1/MC2 Pomodoro scanners skip managed lines
ok 4 - bip MC1/MC2 Pomodoro scanners skip managed lines
  ---
  duration_ms: 1.048973
  ...
# Subtest: explicit task IDs exclusively own dependency lookup
ok 5 - explicit task IDs exclusively own dependency lookup
  ---
  duration_ms: 2.564344
  ...
# Subtest: legacy tasks without an id field still fall back to their block ID
ok 6 - legacy tasks without an id field still fall back to their block ID
  ---
  duration_ms: 0.301014
  ...
# Subtest: blocked-link consumption raises open prerequisites and leaves the dependent blocked
ok 7 - blocked-link consumption raises open prerequisites and leaves the dependent blocked
  ---
  duration_ms: 1.122743
  ...
# Subtest: project-blocked member consumption promotes the project's open prerequisite
ok 8 - project-blocked member consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.668426
  ...
# Subtest: project-blocked resident consumption promotes the project's open prerequisite
ok 9 - project-blocked resident consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.41387
  ...
# Subtest: a tagged inherited ^prj target is refused with its parent named
ok 10 - a tagged inherited ^prj target is refused with its parent named
  ---
  duration_ms: 0.418249
  ...
# Subtest: project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
ok 11 - project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
  ---
  duration_ms: 1.596558
  ...
# Subtest: project date refusal applies only when the date is the sole project reason
ok 12 - project date refusal applies only when the date is the sole project reason
  ---
  duration_ms: 0.269645
  ...
# Subtest: a project-blocked tag is token-bounded and ignored on lookalike tags
ok 13 - a project-blocked tag is token-bounded and ignored on lookalike tags
  ---
  duration_ms: 0.401566
  ...
# Subtest: task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
ok 14 - task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
  ---
  duration_ms: 0.660591
  ...
# Subtest: task blocked state unifies status and dependency reasons
ok 15 - task blocked state unifies status and dependency reasons
  ---
  duration_ms: 0.343556
  ...
# Subtest: task picker partition sinks blocked tasks while preserving group order
ok 16 - task picker partition sinks blocked tasks while preserving group order
  ---
  duration_ms: 0.202276
  ...
# Subtest: blocked chip labels show useful unmet dependency counts
ok 17 - blocked chip labels show useful unmet dependency counts
  ---
  duration_ms: 0.108617
  ...
# Subtest: blocked tooltips explain dependency and status-only reasons
ok 18 - blocked tooltips explain dependency and status-only reasons
  ---
  duration_ms: 0.216433
  ...
# Subtest: task status classes cover every open task status
ok 19 - task status classes cover every open task status
  ---
  duration_ms: 0.096214
  ...
# Subtest: Blocked tasks remain unmet dependency targets
ok 20 - Blocked tasks remain unmet dependency targets
  ---
  duration_ms: 0.132863
  ...
# Subtest: blocked task count covers both reasons without double-counting
ok 21 - blocked task count covers both reasons without double-counting
  ---
  duration_ms: 0.117404
  ...
# Subtest: single caret relocation preserves embedding and removes aliases
ok 22 - single caret relocation preserves embedding and removes aliases
  ---
  duration_ms: 1.504823
  ...
# Subtest: single caret relocation resets aliased block links
ok 23 - single caret relocation resets aliased block links
  ---
  duration_ms: 0.236502
  ...
# Subtest: single caret relocation strips heading and block subpaths
ok 24 - single caret relocation strips heading and block subpaths
  ---
  duration_ms: 0.252492
  ...
# Subtest: task picker normalizes every supported wiki block-link form
ok 25 - task picker normalizes every supported wiki block-link form
  ---
  duration_ms: 0.661532
  ...
# Subtest: three or more carets never trigger the task picker
ok 26 - three or more carets never trigger the task picker
  ---
  duration_ms: 0.149746
  ...
# Subtest: rapid aliased task picker completion preserves the alias
ok 27 - rapid aliased task picker completion preserves the alias
  ---
  duration_ms: 2.451199
  ...
# Subtest: task picker recognition is independent of Markdown source context
ok 28 - task picker recognition is independent of Markdown source context
  ---
  duration_ms: 0.809786
  ...
# Subtest: task picker recognition respects cursor proximity and fenced code
ok 29 - task picker recognition respects cursor proximity and fenced code
  ---
  duration_ms: 0.258162
  ...
# Subtest: plan budget suffix: link Notice appends the meter computed on post-write daily content
ok 30 - plan budget suffix: link Notice appends the meter computed on post-write daily content
  ---
  duration_ms: 6.976276
  ...
# Subtest: plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
ok 31 - plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
  ---
  duration_ms: 0.858579
  ...
# Subtest: plan budget suffix: unlink Notice marks an over-cap plan with 🔴
ok 32 - plan budget suffix: unlink Notice marks an over-cap plan with 🔴
  ---
  duration_ms: 2.754347
  ...
# Subtest: plan budget suffix: Next task without a block ID prompts for one and omits the meter
ok 33 - plan budget suffix: Next task without a block ID prompts for one and omits the meter
  ---
  duration_ms: 0.427816
  ...
# Subtest: plan budget suffix: Task Link Notice appends the meter from post-write daily content
ok 34 - plan budget suffix: Task Link Notice appends the meter from post-write daily content
  ---
  duration_ms: 1.88012
  ...
# Subtest: plan budget suffix: Task Link Notice omits the meter when no daily note takes part
ok 35 - plan budget suffix: Task Link Notice omits the meter when no daily note takes part
  ---
  duration_ms: 0.506617
  ...
# Subtest: planTargetTaskUpdate stamps the rewritten line last via injected stamper
ok 36 - planTargetTaskUpdate stamps the rewritten line last via injected stamper
  ---
  duration_ms: 0.270306
  ...
# Subtest: planTargetTaskUpdate without a stamper never stamps (identity default)
ok 37 - planTargetTaskUpdate without a stamper never stamps (identity default)
  ---
  duration_ms: 0.14191
  ...
# Subtest: planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
ok 38 - planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
  ---
  duration_ms: 0.345259
  ...
# Subtest: planTargetTaskUpdate stamps a Next task that gains a block ID
ok 39 - planTargetTaskUpdate stamps a Next task that gains a block ID
  ---
  duration_ms: 0.46598
  ...
# Subtest: planTargetTaskUpdate tolerates a throwing stamper
ok 40 - planTargetTaskUpdate tolerates a throwing stamper
  ---
  duration_ms: 0.22498
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 41 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.449037
  ...
# Subtest: dedicated-link helpers reject Depends-On lines
ok 42 - dedicated-link helpers reject Depends-On lines
  ---
  duration_ms: 0.32478
  ...
# Subtest: Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
ok 43 - Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
  ---
  duration_ms: 0.306044
  ...
# Subtest: malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
ok 44 - malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
  ---
  duration_ms: 0.107966
  ...
# Subtest: Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
ok 45 - Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
  ---
  duration_ms: 0.238916
  ...
# Subtest: Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
ok 46 - Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
  ---
  duration_ms: 0.198269
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent
ok 47 - readPlanBudgetMeter keeps per-cap over flags independent
  ---
  duration_ms: 0.188971
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent (mirror)
ok 48 - readPlanBudgetMeter keeps per-cap over flags independent (mirror)
  ---
  duration_ms: 0.097036
  ...
# Subtest: block-id-prompt freshness accessors degrade without ledger-tools
ok 49 - block-id-prompt freshness accessors degrade without ledger-tools
  ---
  duration_ms: 0.208588
  ...
# Subtest: list item body bounds trim whitespace and reject empty bullets
ok 50 - list item body bounds trim whitespace and reject empty bullets
  ---
  duration_ms: 1.41423
  ...
# Subtest: Pomodoro activation eligibility requires a sole-content sub-bullet
ok 51 - Pomodoro activation eligibility requires a sole-content sub-bullet
  ---
  duration_ms: 2.00676
  ...
# Subtest: Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
ok 52 - Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
  ---
  duration_ms: 0.278582
  ...
# Subtest: Pomodoro source context distinguishes ledger ancestry and open state
ok 53 - Pomodoro source context distinguishes ledger ancestry and open state
  ---
  duration_ms: 0.466461
  ...
# Subtest: future cleanup touches only later open Pomodoros and counts duplicates
ok 54 - future cleanup touches only later open Pomodoros and counts duplicates
  ---
  duration_ms: 2.122441
  ...
# Subtest: cleanup resolves aliases, embeds, same-note links, and alternate paths
ok 55 - cleanup resolves aliases, embeds, same-note links, and alternate paths
  ---
  duration_ms: 1.525061
  ...
# Subtest: dedicated bullet subtree cleanup preserves CRLF line endings
ok 56 - dedicated bullet subtree cleanup preserves CRLF line endings
  ---
  duration_ms: 0.374655
  ...
# Subtest: existing-ID task completion prunes future links in the source editor
ok 57 - existing-ID task completion prunes future links in the source editor
  ---
  duration_ms: 2.310972
  ...
# Subtest: new-ID same-file completion plans cleanup after the task edit
ok 58 - new-ID same-file completion plans cleanup after the task edit
  ---
  duration_ms: 1.268832
  ...
# Subtest: findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
ok 59 - findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
  ---
  duration_ms: 1.993475
  ...
# Subtest: findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
ok 60 - findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
  ---
  duration_ms: 0.180043
  ...
# Subtest: findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
ok 61 - findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
  ---
  duration_ms: 0.188881
  ...
# Subtest: todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
ok 62 - todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
  ---
  duration_ms: 0.58677
  ...
# Subtest: todayDailyPath honors a custom Daily Notes format and an empty folder
ok 63 - todayDailyPath honors a custom Daily Notes format and an empty folder
  ---
  duration_ms: 1.233054
  ...
# Subtest: formatDailyDate resolves bracketed literal text alongside date tokens
ok 64 - formatDailyDate resolves bracketed literal text alongside date tokens
  ---
  duration_ms: 0.140779
  ...
# Subtest: getDailyNotesOptions reads the daily-notes core plugin's configured options
ok 65 - getDailyNotesOptions reads the daily-notes core plugin's configured options
  ---
  duration_ms: 0.794005
  ...
# Subtest: computeFencedLineFlags marks opening and closing fence lines and everything between
ok 66 - computeFencedLineFlags marks opening and closing fence lines and everything between
  ---
  duration_ms: 0.249938
  ...
# Subtest: selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
ok 67 - selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
  ---
  duration_ms: 0.742708
  ...
# Subtest: selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
ok 68 - selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
  ---
  duration_ms: 0.445841
  ...
# Subtest: selectPomodoroInsertionTarget rejects more than one open timed entry
ok 69 - selectPomodoroInsertionTarget rejects more than one open timed entry
  ---
  duration_ms: 0.211594
  ...
# Subtest: selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
ok 70 - selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
  ---
  duration_ms: 0.18324
  ...
# Subtest: findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
ok 71 - findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
  ---
  duration_ms: 0.172339
  ...
# Subtest: planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
ok 72 - planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
  ---
  duration_ms: 1.10528
  ...
# Subtest: planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
ok 73 - planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
  ---
  duration_ms: 1.198428
  ...
# Subtest: planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
ok 74 - planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
  ---
  duration_ms: 0.211394
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
ok 75 - planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
  ---
  duration_ms: 0.4925
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
ok 76 - planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
  ---
  duration_ms: 0.467272
  ...
# Subtest: planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
ok 77 - planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
  ---
  duration_ms: 0.305824
  ...
# Subtest: planPomodoroLinkInsertion inserts before the separator preceding later content
ok 78 - planPomodoroLinkInsertion inserts before the separator preceding later content
  ---
  duration_ms: 0.247492
  ...
# Subtest: planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
ok 79 - planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
  ---
  duration_ms: 0.275846
  ...
# Subtest: planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
ok 80 - planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
  ---
  duration_ms: 0.342143
  ...
# Subtest: existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
ok 81 - existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
  ---
  duration_ms: 3.021589
  ...
# Subtest: same-note Pomodoro link runtime composes the task update with adjacent insertion
ok 82 - same-note Pomodoro link runtime composes the task update with adjacent insertion
  ---
  duration_ms: 1.098878
  ...
# Subtest: new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
ok 83 - new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
  ---
  duration_ms: 0.607339
  ...
# Subtest: planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
ok 84 - planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
  ---
  duration_ms: 0.279303
  ...
# Subtest: all-open cleanup removes current and future links while preserving history and unresolved links
ok 85 - all-open cleanup removes current and future links while preserving history and unresolved links
  ---
  duration_ms: 0.765792
  ...
# Subtest: all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
ok 86 - all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
  ---
  duration_ms: 1.028293
  ...
# Subtest: all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
ok 87 - all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
  ---
  duration_ms: 0.18327
  ...
# Subtest: all-open cleanup treats missing section, no open entries, and no matches as no-op successes
ok 88 - all-open cleanup treats missing section, no open entries, and no matches as no-op successes
  ---
  duration_ms: 0.223046
  ...
# Subtest: pomodoro link picker choices normalize to existing/new or null
ok 89 - pomodoro link picker choices normalize to existing/new or null
  ---
  duration_ms: 1.21577
  ...
# Subtest: pomodoroLinkPicker api never rejects and validates choices
ok 90 - pomodoroLinkPicker api never rejects and validates choices
  ---
  duration_ms: 0.383823
  ...
# Subtest: destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
ok 91 - destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
  ---
  duration_ms: 0.780821
  ...
# Subtest: destination pick with a section releases its guards when the modal cannot open
ok 92 - destination pick with a section releases its guards when the modal cannot open
  ---
  duration_ms: 1.631485
  ...
# Subtest: plugin lifecycle installs the api and drops it on unload
ok 93 - plugin lifecycle installs the api and drops it on unload
  ---
  duration_ms: 0.301736
  ...
# Subtest: Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
ok 94 - Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
  ---
  duration_ms: 2.623218
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor requires a single cursor
ok 95 - resolvePomodoroLinkTaskFromEditor requires a single cursor
  ---
  duration_ms: 0.317576
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
ok 96 - resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
  ---
  duration_ms: 0.368102
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
ok 97 - resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
  ---
  duration_ms: 0.420283
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
ok 98 - resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
  ---
  duration_ms: 0.501367
  ...
# Subtest: blocked-link consumption reports dependency reasons before the project date
ok 99 - blocked-link consumption reports dependency reasons before the project date
  ---
  duration_ms: 6.412651
  ...
# Subtest: Pomodoro link checks do not read other notes for a non-Blocked task
ok 100 - Pomodoro link checks do not read other notes for a non-Blocked task
  ---
  duration_ms: 0.289192
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
ok 101 - resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
  ---
  duration_ms: 0.352703
  ...
# Subtest: task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
ok 102 - task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
  ---
  duration_ms: 5.602554
  ...
# Subtest: task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
ok 103 - task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
  ---
  duration_ms: 1.728439
  ...
# Subtest: task-mode toggle: linked only under a completed Pomodoro links again
ok 104 - task-mode toggle: linked only under a completed Pomodoro links again
  ---
  duration_ms: 0.763658
  ...
# Subtest: task-mode toggle: a task without a block ID is never linked and prompts for one
ok 105 - task-mode toggle: a task without a block ID is never linked and prompts for one
  ---
  duration_ms: 0.39807
  ...
# Subtest: existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
ok 106 - existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
  ---
  duration_ms: 1.057198
  ...
# Subtest: forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
ok 107 - forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
  ---
  duration_ms: 0.556251
  ...
# Subtest: new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
ok 108 - new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
  ---
  duration_ms: 0.514843
  ...
# Subtest: submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
ok 109 - submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
  ---
  duration_ms: 0.146089
  ...
# Subtest: submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
ok 110 - submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
  ---
  duration_ms: 0.145898
  ...
# Subtest: same-note Pomodoro link runtime: task and ledger edits merge into one transaction
ok 111 - same-note Pomodoro link runtime: task and ledger edits merge into one transaction
  ---
  duration_ms: 1.182658
  ...
# Subtest: linking an already-linked Ready task raises it to Next without duplicating the link
ok 112 - linking an already-linked Ready task raises it to Next without duplicating the link
  ---
  duration_ms: 0.564848
  ...
# Subtest: Next task without a block ID preflights the picker before prompting
ok 113 - Next task without a block ID preflights the picker before prompting
  ---
  duration_ms: 0.481409
  ...
# Subtest: Pomodoro link stops before any mutation when today's daily note is missing
ok 114 - Pomodoro link stops before any mutation when today's daily note is missing
  ---
  duration_ms: 0.180434
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
ok 115 - Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
  ---
  duration_ms: 0.535973
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
ok 116 - Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
  ---
  duration_ms: 0.282269
  ...
# Subtest: Pomodoro link aborts without any write when the task line changed since it was selected
ok 117 - Pomodoro link aborts without any write when the task line changed since it was selected
  ---
  duration_ms: 0.163392
  ...
# Subtest: Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
ok 118 - Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
  ---
  duration_ms: 0.665009
  ...
# Subtest: canceling the Pomodoro block-ID modal leaves the note untouched
ok 119 - canceling the Pomodoro block-ID modal leaves the note untouched
  ---
  duration_ms: 0.156038
  ...
# Subtest: review-walk: existing-ID link hands its Linked notice to continue with no separate notice
ok 120 - review-walk: existing-ID link hands its Linked notice to continue with no separate notice
  ---
  duration_ms: 0.804977
  ...
# Subtest: review-walk: prompted-ID link continues after submit
ok 121 - review-walk: prompted-ID link continues after submit
  ---
  duration_ms: 0.932099
  ...
# Subtest: review-walk: prompt cancel settles with null
ok 122 - review-walk: prompt cancel settles with null
  ---
  duration_ms: 0.131611
  ...
# Subtest: review-walk: BUSY swallows the key with no write
ok 123 - review-walk: BUSY swallows the key with no write
  ---
  duration_ms: 0.273061
  ...
# Subtest: review-walk: failed link keeps its notice and settles with null
ok 124 - review-walk: failed link keeps its notice and settles with null
  ---
  duration_ms: 0.216443
  ...
# Subtest: review-walk: partial link keeps its notice and never continues with an outcome
ok 125 - review-walk: partial link keeps its notice and never continues with an outcome
  ---
  duration_ms: 0.699545
  ...
# Subtest: inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
ok 126 - inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
  ---
  duration_ms: 0.201945
  ...
# Subtest: inbox-route: non-inbox notes and task-link mode never prompt
ok 127 - inbox-route: non-inbox notes and task-link mode never prompt
  ---
  duration_ms: 0.6026
  ...
# Subtest: inbox-route: cancel writes nothing and settles once
ok 128 - inbox-route: cancel writes nothing and settles once
  ---
  duration_ms: 0.462382
  ...
# Subtest: inbox-route: stay matches today
ok 129 - inbox-route: stay matches today
  ---
  duration_ms: 1.20499
  ...
# Subtest: inbox-route: move links, then moves, with one composed toast and a route continue
ok 130 - inbox-route: move links, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.596048
  ...
# Subtest: inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
ok 131 - inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
  ---
  duration_ms: 0.661603
  ...
# Subtest: inbox-route: a move failure gives the partial notice plus a link-today continue
ok 132 - inbox-route: a move failure gives the partial notice plus a link-today continue
  ---
  duration_ms: 0.433618
  ...
# Subtest: review-walk: no nav or nav v2 keeps today's notices
ok 133 - review-walk: no nav or nav v2 keeps today's notices
  ---
  duration_ms: 0.877475
  ...
# Subtest: inbox-route: source drift during route prompt refuses without writes
ok 134 - inbox-route: source drift during route prompt refuses without writes
  ---
  duration_ms: 0.298811
  ...
# Subtest: inbox-route: block-ID route cancel returns sentinel and settles null once
ok 135 - inbox-route: block-ID route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.347844
  ...
# Subtest: inbox-route: link no-op with move never commits
ok 136 - inbox-route: link no-op with move never commits
  ---
  duration_ms: 0.186436
  ...
# Subtest: picker opens only on the link direction, never on unlink
ok 137 - picker opens only on the link direction, never on unlink
  ---
  duration_ms: 8.554971
  ...
# Subtest: picker never opens in task-link mode
ok 138 - picker never opens in task-link mode
  ---
  duration_ms: 3.141306
  ...
# Subtest: Depends-On refusals never open the picker
ok 139 - Depends-On refusals never open the picker
  ---
  duration_ms: 0.861013
  ...
# Subtest: preflight refusals open nothing
ok 140 - preflight refusals open nothing
  ---
  duration_ms: 0.473304
  ...
# Subtest: picking a non-default entry links there
ok 141 - picking a non-default entry links there
  ---
  duration_ms: 1.067558
  ...
# Subtest: cancel writes nothing with no Notice and settles the walk null
ok 142 - cancel writes nothing with no Notice and settles the walk null
  ---
  duration_ms: 0.598853
  ...
# Subtest: a no-ID task gets picker, then the block-ID prompt with the target carried
ok 143 - a no-ID task gets picker, then the block-ID prompt with the target carried
  ---
  duration_ms: 0.883907
  ...
# Subtest: inbox order is picker, then route, then write
ok 144 - inbox order is picker, then route, then write
  ---
  duration_ms: 0.722149
  ...
# Subtest: a review-walk landing continues with link-today and the new text
ok 145 - a review-walk landing continues with link-today and the new text
  ---
  duration_ms: 0.875031
  ...
# Subtest: an all-closed ledger creates a new entry after the last completed block
ok 146 - an all-closed ledger creates a new entry after the last completed block
  ---
  duration_ms: 1.563084
  ...
# Subtest: several running entries allow an explicit pick
ok 147 - several running entries allow an explicit pick
  ---
  duration_ms: 0.785449
  ...
# Subtest: a target that changed before commit refuses with no writes
ok 148 - a target that changed before commit refuses with no writes
  ---
  duration_ms: 0.466861
  ...
# Subtest: a target that closed before commit refuses with no writes
ok 149 - a target that closed before commit refuses with no writes
  ---
  duration_ms: 0.3719
  ...
# Subtest: the task note being the daily note uses one editor transaction
ok 150 - the task note being the daily note uses one editor transaction
  ---
  duration_ms: 0.588694
  ...
# Subtest: promptOpen blocks re-entry while the picker is open
ok 151 - promptOpen blocks re-entry while the picker is open
  ---
  duration_ms: 10.822519
  ...
# Subtest: header shows title, subtitle, lane chip per status, and block-ID chip
ok 152 - header shows title, subtitle, lane chip per status, and block-ID chip
  ---
  duration_ms: 7.538189
  ...
# Subtest: rows render in document order with the default selected
ok 153 - rows render in document order with the default selected
  ---
  duration_ms: 0.956596
  ...
# Subtest: running row shows progress fraction and minutes-left meta
ok 154 - running row shows progress fraction and minutes-left meta
  ---
  duration_ms: 0.976133
  ...
# Subtest: unnamed entries render muted italic
ok 155 - unnamed entries render muted italic
  ---
  duration_ms: 0.51341
  ...
# Subtest: filtering ranks, highlights, and clearing restores the default
ok 156 - filtering ranks, highlights, and clearing restores the default
  ---
  duration_ms: 1.238023
  ...
# Subtest: create row meta, divider, and theme badge
ok 157 - create row meta, divider, and theme badge
  ---
  duration_ms: 1.842767
  ...
# Subtest: exact open names suppress the create row; prefix matches keep it
ok 158 - exact open names suppress the create row; prefix matches keep it
  ---
  duration_ms: 0.831407
  ...
# Subtest: theme badge turns red over cap; a throwing budget hides the detail
ok 159 - theme badge turns red over cap; a throwing budget hides the detail
  ---
  duration_ms: 2.627476
  ...
# Subtest: invalid rows explain the grammar and are inert on Enter
ok 160 - invalid rows explain the grammar and are inert on Enter
  ---
  duration_ms: 9.522917
  ...
# Subtest: multiple running entries show the banner, no pills, and block creation
ok 161 - multiple running entries show the banner, no pills, and block creation
  ---
  duration_ms: 1.615885
  ...
# Subtest: navigation wraps and skips non-selectable rows
ok 162 - navigation wraps and skips non-selectable rows
  ---
  duration_ms: 1.497929
  ...
# Subtest: empty state invites planning a Pomodoro
ok 163 - empty state invites planning a Pomodoro
  ---
  duration_ms: 0.295745
  ...
# Subtest: footer hints and plan meter
ok 164 - footer hints and plan meter
  ---
  duration_ms: 1.255407
  ...
# Subtest: Enter chooses the selected row; click chooses that row
ok 165 - Enter chooses the selected row; click chooses that row
  ---
  duration_ms: 0.87015
  ...
# Subtest: Shift+Enter creates; an exact open name links there instead
ok 166 - Shift+Enter creates; an exact open name links there instead
  ---
  duration_ms: 0.967537
  ...
# Subtest: Ctrl+Shift+Enter commits exactly like Enter
ok 167 - Ctrl+Shift+Enter commits exactly like Enter
  ---
  duration_ms: 2.275274
  ...
# Subtest: Escape and Ctrl+[ cancel with no choice; settle-once holds
ok 168 - Escape and Ctrl+[ cancel with no choice; settle-once holds
  ---
  duration_ms: 0.830065
  ...
# Subtest: canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
ok 169 - canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
  ---
  duration_ms: 1.66113
  ...
# Subtest: canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
ok 170 - canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
  ---
  duration_ms: 0.280205
  ...
# Subtest: pomodoroLinkSelectorSlug mirrors capture slugs
ok 171 - pomodoroLinkSelectorSlug mirrors capture slugs
  ---
  duration_ms: 0.239928
  ...
# Subtest: parsePomodoroEntryParts reads canonical and legacy entry lines
ok 172 - parsePomodoroEntryParts reads canonical and legacy entry lines
  ---
  duration_ms: 1.731895
  ...
# Subtest: collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
ok 173 - collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
  ---
  duration_ms: 1.402748
  ...
# Subtest: collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
ok 174 - collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
  ---
  duration_ms: 0.976264
  ...
# Subtest: collectPomodoroLinkEntries counts links but excludes struck references
ok 175 - collectPomodoroLinkEntries counts links but excludes struck references
  ---
  duration_ms: 0.385085
  ...
# Subtest: collectPomodoroLinkEntries falls back to range text and position titles
ok 176 - collectPomodoroLinkEntries falls back to range text and position titles
  ---
  duration_ms: 0.237513
  ...
# Subtest: pomodoroRunProgress reports fractions, overtime, and midnight wrap
ok 177 - pomodoroRunProgress reports fractions, overtime, and midnight wrap
  ---
  duration_ms: 0.522959
  ...
# Subtest: buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
ok 178 - buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
  ---
  duration_ms: 0.777714
  ...
# Subtest: buildPomodoroLinkPickerRows keeps the create row for prefix matches
ok 179 - buildPomodoroLinkPickerRows keeps the create row for prefix matches
  ---
  duration_ms: 0.277309
  ...
# Subtest: buildPomodoroLinkPickerRows marks completed-only names as again
ok 180 - buildPomodoroLinkPickerRows marks completed-only names as again
  ---
  duration_ms: 0.165606
  ...
# Subtest: buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
ok 181 - buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
  ---
  duration_ms: 0.369846
  ...
# Subtest: buildPomodoroLinkPickerRows matches times, positions, and block IDs
ok 182 - buildPomodoroLinkPickerRows matches times, positions, and block IDs
  ---
  duration_ms: 0.451552
  ...
# Subtest: resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
ok 183 - resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
  ---
  duration_ms: 0.27786
  ...
# Subtest: defaultPomodoroLinkChoice returns the default entry or null
ok 184 - defaultPomodoroLinkChoice returns the default entry or null
  ---
  duration_ms: 0.178411
  ...
# Subtest: planExplicitPomodoroLinkInsertion links under a chosen existing entry
ok 185 - planExplicitPomodoroLinkInsertion links under a chosen existing entry
  ---
  duration_ms: 0.895749
  ...
# Subtest: planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
ok 186 - planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
  ---
  duration_ms: 0.242062
  ...
# Subtest: planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
ok 187 - planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
  ---
  duration_ms: 0.927049
  ...
# Subtest: planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
ok 188 - planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
  ---
  duration_ms: 0.319119
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after the running entry
ok 189 - planExplicitPomodoroLinkInsertion creates after the running entry
  ---
  duration_ms: 0.573405
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
ok 190 - planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
  ---
  duration_ms: 0.654229
  ...
# Subtest: planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
ok 191 - planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
  ---
  duration_ms: 0.195974
  ...
# Subtest: planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
ok 192 - planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
  ---
  duration_ms: 0.306244
  ...
# Subtest: planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
ok 193 - planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
  ---
  duration_ms: 0.364346
  ...
# Subtest: buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
ok 194 - buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
  ---
  duration_ms: 0.182859
  ...
# Subtest: buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
ok 195 - buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
  ---
  duration_ms: 0.157982
  ...
# Subtest: planExplicitPomodoroLinkInsertion matches mixed-case raced open names
ok 196 - planExplicitPomodoroLinkInsertion matches mixed-case raced open names
  ---
  duration_ms: 0.18891
  ...
# Subtest: buildPomodoroLinkPickerRows bounds \#N position matches
ok 197 - buildPomodoroLinkPickerRows bounds \#N position matches
  ---
  duration_ms: 0.480918
  ...
# Subtest: planPomodoroLinkInsertion without a target keeps today's behavior and shape
ok 198 - planPomodoroLinkInsertion without a target keeps today's behavior and shape
  ---
  duration_ms: 0.414321
  ...
# Subtest: direct unlink without a daily note keeps the Next lane and reports it
ok 199 - direct unlink without a daily note keeps the Next lane and reports it
  ---
  duration_ms: 2.461248
  ...
# Subtest: In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
ok 200 - In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
  ---
  duration_ms: 0.468764
  ...
# Subtest: In Progress unlink with a summary keeps the lane and creates a Work Log
ok 201 - In Progress unlink with a summary keeps the lane and creates a Work Log
  ---
  duration_ms: 1.281837
  ...
# Subtest: In Progress unlink revalidates task text and block-ID uniqueness at confirmation
ok 202 - In Progress unlink revalidates task text and block-ID uniqueness at confirmation
  ---
  duration_ms: 0.310432
  ...
# Subtest: Next task unlink removes current and future links and keeps the Next lane
ok 203 - Next task unlink removes current and future links and keeps the Next lane
  ---
  duration_ms: 4.486133
  ...
# Subtest: In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
ok 204 - In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
  ---
  duration_ms: 0.872205
  ...
# Subtest: same-note Next unlink merges the Work Log and all-open cleanup in the active editor
ok 205 - same-note Next unlink merges the Work Log and all-open cleanup in the active editor
  ---
  duration_ms: 0.706098
  ...
# Subtest: same-note In Progress unlink merges cleanup and Work Log in the active editor
ok 206 - same-note In Progress unlink merges cleanup and Work Log in the active editor
  ---
  duration_ms: 0.546955
  ...
# Subtest: Next unlink stops before any write when daily cleanup write is stale
ok 207 - Next unlink stops before any write when daily cleanup write is stale
  ---
  duration_ms: 0.726557
  ...
# Subtest: Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
ok 208 - Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
  ---
  duration_ms: 1.022822
  ...
# Subtest: In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
ok 209 - In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
  ---
  duration_ms: 0.656673
  ...
# Subtest: review-walk: unlink settles with null and keeps its notice
ok 210 - review-walk: unlink settles with null and keeps its notice
  ---
  duration_ms: 1.211893
  ...
# Subtest: inbox-route: unlink cancel writes nothing
ok 211 - inbox-route: unlink cancel writes nothing
  ---
  duration_ms: 0.413319
  ...
# Subtest: inbox-route: unlink stay matches today and never commits
ok 212 - inbox-route: unlink stay matches today and never commits
  ---
  duration_ms: 0.500805
  ...
# Subtest: inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
ok 213 - inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.574066
  ...
# Subtest: inbox-route: In Progress unlink with a Work summary routes
ok 214 - inbox-route: In Progress unlink with a Work summary routes
  ---
  duration_ms: 0.615595
  ...
# Subtest: inbox-route: unlink move failure gives the partial notice and stays
ok 215 - inbox-route: unlink move failure gives the partial notice and stays
  ---
  duration_ms: 0.313949
  ...
# Subtest: inbox-route: non-inbox unlink never prompts
ok 216 - inbox-route: non-inbox unlink never prompts
  ---
  duration_ms: 0.295374
  ...
# Subtest: review-walk: Work-summary unlink path retains origin until submit
ok 217 - review-walk: Work-summary unlink path retains origin until submit
  ---
  duration_ms: 0.308639
  ...
# Subtest: inbox-route: unlink source drift during route prompt refuses without writes
ok 218 - inbox-route: unlink source drift during route prompt refuses without writes
  ---
  duration_ms: 0.229658
  ...
# Subtest: inbox-route: Work-summary route cancel returns sentinel and settles null once
ok 219 - inbox-route: Work-summary route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.258494
  ...
# Subtest: inbox-route: unlink no-op with move never commits
ok 220 - inbox-route: unlink no-op with move never commits
  ---
  duration_ms: 0.226302
  ...
# Subtest: direct-add seeds from the task headline, not non-task blocks
ok 221 - direct-add seeds from the task headline, not non-task blocks
  ---
  duration_ms: 4.406221
  ...
# Subtest: link-task-complete seeds from the target, prefers open buffers
ok 222 - link-task-complete seeds from the target, prefers open buffers
  ---
  duration_ms: 1.221511
  ...
# Subtest: link-task-complete reports stale and unreadable targets
ok 223 - link-task-complete reports stale and unreadable targets
  ---
  duration_ms: 0.365007
  ...
# Subtest: pomodoro link seeds after the choice from the cursor task
ok 224 - pomodoro link seeds after the choice from the cursor task
  ---
  duration_ms: 0.366219
  ...
# Subtest: marker rename suggests from the unique task, never hiding ambiguity
ok 225 - marker rename suggests from the unique task, never hiding ambiguity
  ---
  duration_ms: 0.730485
  ...
# Subtest: modal seeds the value, selects once, and never overwrites typing
ok 226 - modal seeds the value, selects once, and never overwrites typing
  ---
  duration_ms: 1.685848
  ...
# Subtest: modal disables Save while loading and survives close/reopen
ok 227 - modal disables Save while loading and survives close/reopen
  ---
  duration_ms: 2.455908
  ...
# Subtest: submit revalidates: occupied IDs and stale tasks fail editable
ok 228 - submit revalidates: occupied IDs and stale tasks fail editable
  ---
  duration_ms: 0.630955
  ...
# Subtest: cancelling writes no ID and explicit renames keep the current ID
ok 229 - cancelling writes no ID and explicit renames keep the current ID
  ---
  duration_ms: 0.829874
  ...
# Subtest: the task picker drops the paired \#ref and prefixes the book
ok 230 - the task picker drops the paired \#ref and prefixes the book
  ---
  duration_ms: 2.535199
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 231 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.323427
  ...
# Subtest: calendar date parsing rejects malformed width and impossible dates
ok 232 - calendar date parsing rejects malformed width and impossible dates
  ---
  duration_ms: 1.6239
  ...
# Subtest: future scheduled field detection respects the yesterday/today/tomorrow boundary
ok 233 - future scheduled field detection respects the yesterday/today/tomorrow boundary
  ---
  duration_ms: 1.595095
  ...
# Subtest: scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
ok 234 - scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
  ---
  duration_ms: 0.231202
  ...
# Subtest: planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
ok 235 - planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
  ---
  duration_ms: 1.093157
  ...
# Subtest: planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
ok 236 - planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
  ---
  duration_ms: 0.233235
  ...
# Subtest: planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
ok 237 - planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
  ---
  duration_ms: 0.179974
  ...
# Subtest: planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
ok 238 - planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
  ---
  duration_ms: 0.184823
  ...
# Subtest: planTargetTaskUpdate leaves today and past schedules untouched
ok 239 - planTargetTaskUpdate leaves today and past schedules untouched
  ---
  duration_ms: 0.317135
  ...
# Subtest: planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
ok 240 - planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
  ---
  duration_ms: 0.372171
  ...
# Subtest: two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
ok 241 - two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
  ---
  duration_ms: 0.484044
  ...
# Subtest: a malformed single scheduled field is never treated as future
ok 242 - a malformed single scheduled field is never treated as future
  ---
  duration_ms: 0.189662
  ...
# Subtest: an ambiguous scheduled field does not block the legacy Ready promotion
ok 243 - an ambiguous scheduled field does not block the legacy Ready promotion
  ---
  duration_ms: 0.210321
  ...
# Subtest: planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
ok 244 - planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
  ---
  duration_ms: 0.153233
  ...
# Subtest: Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
ok 245 - Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
  ---
  duration_ms: 0.51354
  ...
# Subtest: Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
ok 246 - Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
  ---
  duration_ms: 0.179723
  ...
# Subtest: planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
ok 247 - planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
  ---
  duration_ms: 0.268783
  ...
# Subtest: planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
ok 248 - planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
  ---
  duration_ms: 0.13603
  ...
# Subtest: planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
ok 249 - planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.122413
  ...
# Subtest: planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
ok 250 - planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
  ---
  duration_ms: 0.155167
  ...
# Subtest: planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
ok 251 - planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
  ---
  duration_ms: 0.14126
  ...
# Subtest: planTargetTaskUpdate preserves a trailing newline when one was already present
ok 252 - planTargetTaskUpdate preserves a trailing newline when one was already present
  ---
  duration_ms: 0.144436
  ...
# Subtest: planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
ok 253 - planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
  ---
  duration_ms: 0.124287
  ...
# Subtest: planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
ok 254 - planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
  ---
  duration_ms: 0.173211
  ...
# Subtest: planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
ok 255 - planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
  ---
  duration_ms: 0.148824
  ...
# Subtest: existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
ok 256 - existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
  ---
  duration_ms: 3.289699
  ...
# Subtest: new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
ok 257 - new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
  ---
  duration_ms: 0.804826
  ...
# Subtest: activation runtime aborts without any write when the target preimage goes stale
ok 258 - activation runtime aborts without any write when the target preimage goes stale
  ---
  duration_ms: 0.453706
  ...
# Subtest: same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
ok 259 - same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
  ---
  duration_ms: 2.250156
  ...
# Subtest: same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
ok 260 - same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
  ---
  duration_ms: 0.606037
  ...
# Subtest: a source marker edited after a successful existing-ID target write reports an accurate partial notice
ok 261 - a source marker edited after a successful existing-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.543929
  ...
# Subtest: a source marker edited after a successful new-ID target write reports an accurate partial notice
ok 262 - a source marker edited after a successful new-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.519201
  ...
# Subtest: planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
ok 263 - planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
  ---
  duration_ms: 0.181155
  ...
# Subtest: planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
ok 264 - planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
  ---
  duration_ms: 0.123525
  ...
# Subtest: planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
ok 265 - planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
  ---
  duration_ms: 0.134977
  ...
# Subtest: planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
ok 266 - planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.115821
  ...
# Subtest: direct Task Links raise ^prj while never pulling its date forward
ok 267 - direct Task Links raise ^prj while never pulling its date forward
  ---
  duration_ms: 0.128526
  ...
# Subtest: task-link selection: one link is selectable from any column, several are chosen by cursor
ok 268 - task-link selection: one link is selectable from any column, several are chosen by cursor
  ---
  duration_ms: 3.67196
  ...
# Subtest: task-link selection ignores picker/rename markers, plain links, and Markdown-style links
ok 269 - task-link selection ignores picker/rename markers, plain links, and Markdown-style links
  ---
  duration_ms: 0.32524
  ...
# Subtest: dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
ok 270 - dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
  ---
  duration_ms: 0.682072
  ...
# Subtest: inline Task Link deletion removes the token with its decoration and collapses whitespace
ok 271 - inline Task Link deletion removes the token with its decoration and collapses whitespace
  ---
  duration_ms: 0.642226
  ...
# Subtest: dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
ok 272 - dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
  ---
  duration_ms: 0.850543
  ...
# Subtest: mergeCoveringEdits keeps the covering edit and the earlier of identical edits
ok 273 - mergeCoveringEdits keeps the covering edit and the earlier of identical edits
  ---
  duration_ms: 0.220942
  ...
# Subtest: dependency transclusion detection needs an embedded sole-content child of a \#task line
ok 274 - dependency transclusion detection needs an embedded sole-content child of a \#task line
  ---
  duration_ms: 0.474015
  ...
# Subtest: Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
ok 275 - Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
  ---
  duration_ms: 4.516972
  ...
# Subtest: Task Link on a Next target works from an embedded aliased link outside any Pomodoro
ok 276 - Task Link on a Next target works from an embedded aliased link outside any Pomodoro
  ---
  duration_ms: 1.15252
  ...
# Subtest: same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
ok 277 - same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
  ---
  duration_ms: 1.12164
  ...
# Subtest: same-note Task Link deletion clamps the restored cursor to the shortened note
ok 278 - same-note Task Link deletion clamps the restored cursor to the shortened note
  ---
  duration_ms: 0.675329
  ...
# Subtest: a cleanup subtree that covers a nested selected link wins and links are not double counted
ok 279 - a cleanup subtree that covers a nested selected link wins and links are not double counted
  ---
  duration_ms: 1.036398
  ...
# Subtest: same-note Task Link in a closed entry deletes the closed entry it empties
ok 280 - same-note Task Link in a closed entry deletes the closed entry it empties
  ---
  duration_ms: 0.639661
  ...
# Subtest: Task Link in another day's note deletes the emptied entry there and in today's note
ok 281 - Task Link in another day's note deletes the emptied entry there and in today's note
  ---
  duration_ms: 0.579567
  ...
# Subtest: Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
ok 282 - Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
  ---
  duration_ms: 1.429529
  ...
# Subtest: Task Link on an In Progress target with a blank summary logs nothing
ok 283 - Task Link on an In Progress target with a blank summary logs nothing
  ---
  duration_ms: 0.786882
  ...
# Subtest: canceling the In Progress Task Link prompt leaves everything untouched
ok 284 - canceling the In Progress Task Link prompt leaves everything untouched
  ---
  duration_ms: 0.321454
  ...
# Subtest: canceling the In Progress unlink prompt in task mode leaves everything untouched
ok 285 - canceling the In Progress unlink prompt in task mode leaves everything untouched
  ---
  duration_ms: 0.608322
  ...
# Subtest: In Progress Task Link submit revalidates the link line and the target task
ok 286 - In Progress Task Link submit revalidates the link line and the target task
  ---
  duration_ms: 0.603663
  ...
# Subtest: Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
ok 287 - Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
  ---
  duration_ms: 0.694486
  ...
# Subtest: Task Link on a Done or Cancelled target is refused without edits
ok 288 - Task Link on a Done or Cancelled target is refused without edits
  ---
  duration_ms: 0.438968
  ...
# Subtest: Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
ok 289 - Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
  ---
  duration_ms: 0.713171
  ...
# Subtest: precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
ok 290 - precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
  ---
  duration_ms: 1.368221
  ...
# Subtest: Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
ok 291 - Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
  ---
  duration_ms: 0.365859
  ...
# Subtest: Task Link that is a sub-task dependency transclusion is refused without edits
ok 292 - Task Link that is a sub-task dependency transclusion is refused without edits
  ---
  duration_ms: 0.305563
  ...
# Subtest: Task Link partial failure after the daily write is retryable
ok 293 - Task Link partial failure after the daily write is retryable
  ---
  duration_ms: 2.364795
  ...
# Subtest: Task Link stops before any write when the target note changes after planning
ok 294 - Task Link stops before any write when the target note changes after planning
  ---
  duration_ms: 0.50783
  ...
# Subtest: Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
ok 295 - Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
  ---
  duration_ms: 0.448165
  ...
# Subtest: Task Link subtree deletion removes a nested target task without any status write
ok 296 - Task Link subtree deletion removes a nested target task without any status write
  ---
  duration_ms: 0.305713
  ...
# Subtest: work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
ok 297 - work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
  ---
  duration_ms: 1.826877
  ...
# Subtest: work log date helpers use local calendar components
ok 298 - work log date helpers use local calendar components
  ---
  duration_ms: 0.289312
  ...
# Subtest: planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
ok 299 - planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
  ---
  duration_ms: 0.806769
  ...
# Subtest: planWorkLogInsertion inherits an existing space-indented child prefix
ok 300 - planWorkLogInsertion inherits an existing space-indented child prefix
  ---
  duration_ms: 0.595707
  ...
# Subtest: planWorkLogInsertion inherits an existing tab-indented child prefix
ok 301 - planWorkLogInsertion inherits an existing tab-indented child prefix
  ---
  duration_ms: 0.285375
  ...
# Subtest: planWorkLogInsertion prepends newest-first entries into existing marker spellings
ok 302 - planWorkLogInsertion prepends newest-first entries into existing marker spellings
  ---
  duration_ms: 0.584435
  ...
# Subtest: planWorkLogInsertion ignores nested child-task markers and preserves CRLF
ok 303 - planWorkLogInsertion ignores nested child-task markers and preserves CRLF
  ---
  duration_ms: 0.458205
  ...
# Subtest: planWorkLogInsertion treats blank summaries as no-op structural edits
ok 304 - planWorkLogInsertion treats blank summaries as no-op structural edits
  ---
  duration_ms: 0.169884
  ...
# Subtest: the Open-reset planner is removed: unlink plans only a Work Log insertion
ok 305 - the Open-reset planner is removed: unlink plans only a Work Log insertion
  ---
  duration_ms: 0.391708
  ...
# Subtest: unlink Work Log plan keeps the In Progress checkbox and appends one entry
ok 306 - unlink Work Log plan keeps the In Progress checkbox and appends one entry
  ---
  duration_ms: 0.454608
  ...
# Subtest: folds embed, struck, and plain legacy children into one canonical line
ok 307 - folds embed, struck, and plain legacy children into one canonical line
  ---
  duration_ms: 74.986499
  ...
# Subtest: legacy-label row links come first, then legacy children in order
ok 308 - legacy-label row links come first, then legacy children in order
  ---
  duration_ms: 3.44664
  ...
# Subtest: R2 adopts field-only open dependents; unadoptable ids stay warned
ok 309 - R2 adopts field-only open dependents; unadoptable ids stay warned
  ---
  duration_ms: 0.888416
  ...
# Subtest: closed dependents gain the line but keep the field untouched
ok 310 - closed dependents gain the line but keep the field untouched
  ---
  duration_ms: 1.392418
  ...
# Subtest: open dependents drop stale field ids and stamp targets missing [id::]
ok 311 - open dependents drop stale field ids and stamp targets missing [id::]
  ---
  duration_ms: 0.7338
  ...
# Subtest: unresolved links stay verbatim and keep field ids as breadcrumbs
ok 312 - unresolved links stay verbatim and keep field ids as breadcrumbs
  ---
  duration_ms: 0.624011
  ...
# Subtest: leaves \#^ref embeds, non-task parents, fences, and conflict children alone
ok 313 - leaves \#^ref embeds, non-task parents, fences, and conflict children alone
  ---
  duration_ms: 0.884288
  ...
# Subtest: malformed rows leave the whole dependent alone
ok 314 - malformed rows leave the whole dependent alone
  ---
  duration_ms: 0.647375
  ...
# Subtest: R9 deletes label-only rows and removes the open field
ok 315 - R9 deletes label-only rows and removes the open field
  ---
  duration_ms: 0.775961
  ...
# Subtest: cross-note links use the shortest unambiguous form
ok 316 - cross-note links use the shortest unambiguous form
  ---
  duration_ms: 0.636085
  ...
# Subtest: ambiguous basenames fall back to the full path
ok 317 - ambiguous basenames fall back to the full path
  ---
  duration_ms: 0.443868
  ...
# Subtest: duplicate ids are ambiguous and fatal for --write
ok 318 - duplicate ids are ambiguous and fatal for --write
  ---
  duration_ms: 0.229528
  ...
# Subtest: archive targets keep the done/ path and are never stamped
ok 319 - archive targets keep the done/ path and are never stamped
  ---
  duration_ms: 0.264866
  ...
# Subtest: self links stay on the line but are not projected
ok 320 - self links stay on the line but are not projected
  ---
  duration_ms: 0.312227
  ...
# Subtest: non-task targets stay on the line but are not projected
ok 321 - non-task targets stay on the line but are not projected
  ---
  duration_ms: 0.250408
  ...
# Subtest: preserves CRLF, missing final newline, and cancel-log position
ok 322 - preserves CRLF, missing final newline, and cancel-log position
  ---
  duration_ms: 0.344217
  ...
# Subtest: migration is idempotent
ok 323 - migration is idempotent
  ---
  duration_ms: 1.027412
  ...
# Subtest: parseArgs handles --vault, --write, --help, and rejects unknowns
ok 324 - parseArgs handles --vault, --write, --help, and rejects unknowns
  ---
  duration_ms: 0.565579
  ...
# Subtest: BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
ok 325 - BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
  ---
  duration_ms: 4.017588
  ...
# Subtest: reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
ok 326 - reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
  ---
  duration_ms: 3.131527
  ...
# Subtest: stale, missing, canonical append, and frozen-owner models (BC8-BC10)
ok 327 - stale, missing, canonical append, and frozen-owner models (BC8-BC10)
  ---
  duration_ms: 0.676281
  ...
# Subtest: Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
ok 328 - Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
  ---
  duration_ms: 8.021362
  ...
# Subtest: budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
ok 329 - budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
  ---
  duration_ms: 1.483932
  ...
# Subtest: chip builder includes the 🔑 badge and has no edit controls
ok 330 - chip builder includes the 🔑 badge and has no edit controls
  ---
  duration_ms: 0.507048
  ...
# Subtest: collections namespace version is additive v1
ok 331 - collections namespace version is additive v1
  ---
  duration_ms: 0.929464
  ...
# Subtest: collection chip classes stay collection-specific through paint and refresh
ok 332 - collection chip classes stay collection-specific through paint and refresh
  ---
  duration_ms: 3.183016
  ...
# Subtest: projects: scalar resolved links count, lists never widen
ok 333 - projects: scalar resolved links count, lists never widen
  ---
  duration_ms: 0.321394
  ...
# Subtest: projects: templates, status, and containsAny edges
ok 334 - projects: templates, status, and containsAny edges
  ---
  duration_ms: 0.302588
  ...
# Subtest: references: exact prefix, md only, exact scalar status
ok 335 - references: exact prefix, md only, exact scalar status
  ---
  duration_ms: 0.254376
  ...
# Subtest: base contracts: accept current files, reject drift, tolerate presentation
ok 336 - base contracts: accept current files, reject drift, tolerate presentation
  ---
  duration_ms: 0.590197
  ...
# Subtest: entries: true zero vs unavailable with reason, failure isolation
ok 337 - entries: true zero vs unavailable with reason, failure isolation
  ---
  duration_ms: 0.275105
  ...
# Subtest: snapshot counts both collections once, true zero stays clickable
ok 338 - snapshot counts both collections once, true zero stays clickable
  ---
  duration_ms: 0.375527
  ...
# Subtest: snapshot never presents partial counts as final
ok 339 - snapshot never presents partial counts as final
  ---
  duration_ms: 0.379204
  ...
# Subtest: changed definitions fail closed per collection, never stale
ok 340 - changed definitions fail closed per collection, never stale
  ---
  duration_ms: 0.464997
  ...
# Subtest: renderChip links, labels, and cleans up per component
ok 341 - renderChip links, labels, and cleans up per component
  ---
  duration_ms: 0.591168
  ...
# Subtest: PENDING section excludes TODAY while the whole lane keeps it
ok 342 - PENDING section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 3.408696
  ...
# Subtest: NEXT section excludes TODAY while the whole lane keeps it
ok 343 - NEXT section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 0.531595
  ...
# Subtest: NEXT uses symbol *, not name matching
ok 344 - NEXT uses symbol *, not name matching
  ---
  duration_ms: 0.359005
  ...
# Subtest: READY badge and query agree on hide and path case variants
ok 345 - READY badge and query agree on hide and path case variants
  ---
  duration_ms: 0.785619
  ...
# Subtest: blocked uses the full list even outside the visible subset
ok 346 - blocked uses the full list even outside the visible subset
  ---
  duration_ms: 0.27233
  ...
# Subtest: duplicate block IDs, missing IDs, and reused objects stay per-row
ok 347 - duplicate block IDs, missing IDs, and reused objects stay per-row
  ---
  duration_ms: 0.307186
  ...
# Subtest: READY gating keeps exempt rows and drops NEW/ROTTEN
ok 348 - READY gating keeps exempt rows and drops NEW/ROTTEN
  ---
  duration_ms: 0.396718
  ...
# Subtest: throwing Today degrades to unavailable, never zero
ok 349 - throwing Today degrades to unavailable, never zero
  ---
  duration_ms: 8.258525
  ...
# Subtest: dashboard badges color the displayed section count and label whole-lane pressure
ok 350 - dashboard badges color the displayed section count and label whole-lane pressure
  ---
  duration_ms: 0.892945
  ...
# Subtest: dashboard section warning boundaries ignore TODAY-only whole-lane excess
ok 351 - dashboard section warning boundaries ignore TODAY-only whole-lane excess
  ---
  duration_ms: 2.821075
  ...
# Subtest: dashboard lane badge keeps unavailable data neutral
ok 352 - dashboard lane badge keeps unavailable data neutral
  ---
  duration_ms: 0.309651
  ...
# Subtest: dashboard lane paint and refresh keep color aligned with the visible section
ok 353 - dashboard lane paint and refresh keep color aligned with the visible section
  ---
  duration_ms: 2.514099
  ...
# Subtest: dashboard lane widgets refresh together and prune on unload
ok 354 - dashboard lane widgets refresh together and prune on unload
  ---
  duration_ms: 1.885569
  ...
# Subtest: daily paint matches dashboard section badges on screenshot fixtures
ok 355 - daily paint matches dashboard section badges on screenshot fixtures
  ---
  duration_ms: 18.827459
  ...
# Subtest: daily and dashboard membership agree for exclusions and custom IN_PROGRESS
ok 356 - daily and dashboard membership agree for exclusions and custom IN_PROGRESS
  ---
  duration_ms: 5.239732
  ...
# Subtest: daily paint refreshes with dashboard when Today, lane, and cap change
ok 357 - daily paint refreshes with dashboard when Today, lane, and cap change
  ---
  duration_ms: 7.375798
  ...
# Subtest: older daily notes follow today's dashboard lanes
ok 358 - older daily notes follow today's dashboard lanes
  ---
  duration_ms: 2.527625
  ...
# Subtest: daily lane anchors keep shared navigation and reject stale paints
ok 359 - daily lane anchors keep shared navigation and reject stale paints
  ---
  duration_ms: 2.659057
  ...
# Subtest: daily paint stays unavailable until Tasks and Today are ready
ok 360 - daily paint stays unavailable until Tasks and Today are ready
  ---
  duration_ms: 1.181935
  ...
# Subtest: work tones: dashboard lane models carry section tones
ok 361 - work tones: dashboard lane models carry section tones
  ---
  duration_ms: 0.238615
  ...
# Subtest: T1 scheduled full-mode row gets a Fri mark inside the span
ok 362 - T1 scheduled full-mode row gets a Fri mark inside the span
  ---
  duration_ms: 2.828649
  ...
# Subtest: T2 done row maps to a completion Oct 5 mark
ok 363 - T2 done row maps to a completion Oct 5 mark
  ---
  duration_ms: 0.505906
  ...
# Subtest: T3 short-mode created span is left untouched by JS
ok 364 - T3 short-mode created span is left untouched by JS
  ---
  duration_ms: 0.310853
  ...
# Subtest: T4 pending row decorates once data-task appears; exhausted rows stay native
ok 365 - T4 pending row decorates once data-task appears; exhausted rows stay native
  ---
  duration_ms: 1.0374
  ...
# Subtest: T5 a second pass adds nothing
ok 366 - T5 a second pass adds nothing
  ---
  duration_ms: 0.268322
  ...
# Subtest: T6 task-due and task-start spans are untouched
ok 367 - T6 task-due and task-start spans are untouched
  ---
  duration_ms: 0.284624
  ...
# Subtest: T7 an invalid date is untouched
ok 368 - T7 an invalid date is untouched
  ---
  duration_ms: 0.291366
  ...
# Subtest: T8 nothing is scheduled with marks off or for connected non-Tasks elements
ok 369 - T8 nothing is scheduled with marks off or for connected non-Tasks elements
  ---
  duration_ms: 0.278552
  ...
# Subtest: T9 a Tasks-host Fri mark relabels to tomorrow on rollover
ok 370 - T9 a Tasks-host Fri mark relabels to tomorrow on rollover
  ---
  duration_ms: 0.757786
  ...
# Subtest: renderDateMarksIn schedules one shared frame for every row
ok 371 - renderDateMarksIn schedules one shared frame for every row
  ---
  duration_ms: 1.104579
  ...
# Subtest: the Tasks pass never throws on hostile input
ok 372 - the Tasks pass never throws on hostile input
  ---
  duration_ms: 0.452133
  ...
# Subtest: T10 real-DOM NodeList children decorate via direct and queued passes
ok 373 - T10 real-DOM NodeList children decorate via direct and queued passes
  ---
  duration_ms: 2.034844
  ...
# Subtest: T11 toggling off before a queued frame runs writes nothing
ok 374 - T11 toggling off before a queued frame runs writes nothing
  ---
  duration_ms: 0.412498
  ...
# Subtest: T12 a pending-row retry followed by disabling writes nothing
ok 375 - T12 a pending-row retry followed by disabling writes nothing
  ---
  duration_ms: 0.316735
  ...
# Subtest: T13 unloading before a callback runs writes nothing
ok 376 - T13 unloading before a callback runs writes nothing
  ---
  duration_ms: 0.740463
  ...
# Subtest: styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
ok 377 - styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
  ---
  duration_ms: 0.561301
  ...
# Subtest: DATE_MARK_FIELDS lists the four dates with verbs
ok 378 - DATE_MARK_FIELDS lists the four dates with verbs
  ---
  duration_ms: 1.646223
  ...
# Subtest: DM1 created today: label, tooltip, fold, quiet field
ok 379 - DM1 created today: label, tooltip, fold, quiet field
  ---
  duration_ms: 1.457292
  ...
# Subtest: DM2 created yesterday without space after the colons
ok 380 - DM2 created yesterday without space after the colons
  ---
  duration_ms: 0.379174
  ...
# Subtest: DM3-DM6 scheduled tomorrow, weekday, and month/day labels
ok 381 - DM3-DM6 scheduled tomorrow, weekday, and month/day labels
  ---
  duration_ms: 0.233506
  ...
# Subtest: DM7 scheduled today reads with emphasis timing
ok 382 - DM7 scheduled today reads with emphasis timing
  ---
  duration_ms: 0.231823
  ...
# Subtest: DM8 past scheduled uses month/day, never a weekday
ok 383 - DM8 past scheduled uses month/day, never a weekday
  ---
  duration_ms: 0.158673
  ...
# Subtest: DM9 completion on a closed task keeps the timeline grammar
ok 384 - DM9 completion on a closed task keeps the timeline grammar
  ---
  duration_ms: 0.188089
  ...
# Subtest: DM10 cancelled across years appends the year
ok 385 - DM10 cancelled across years appends the year
  ---
  duration_ms: 0.139025
  ...
# Subtest: DM11 next-year date appends the year
ok 386 - DM11 next-year date appends the year
  ---
  duration_ms: 0.317837
  ...
# Subtest: DM12 the weekday rule wins across the year boundary
ok 387 - DM12 the weekday rule wins across the year boundary
  ---
  duration_ms: 0.384765
  ...
# Subtest: DM13 two marks in order with folds 1 and 2
ok 388 - DM13 two marks in order with folds 1 and 2
  ---
  duration_ms: 0.435181
  ...
# Subtest: DM14 created and scheduled ranges stay disjoint from the fresh mark
ok 389 - DM14 created and scheduled ranges stay disjoint from the fresh mark
  ---
  duration_ms: 0.307687
  ...
# Subtest: DM15-DM16 paren and padded brackets are canonical
ok 390 - DM15-DM16 paren and padded brackets are canonical
  ---
  duration_ms: 0.177219
  ...
# Subtest: DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
ok 391 - DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
  ---
  duration_ms: 0.320743
  ...
# Subtest: DM22 code still parses pure but decorates nothing (see Live Preview)
ok 392 - DM22 code still parses pure but decorates nothing (see Live Preview)
  ---
  duration_ms: 0.119708
  ...
# Subtest: DM23 rescheduled is untouched and never a duplicate
ok 393 - DM23 rescheduled is untouched and never a duplicate
  ---
  duration_ms: 0.144616
  ...
# Subtest: DN1-DN9 non-canonical fields get no mark
ok 394 - DN1-DN9 non-canonical fields get no mark
  ---
  duration_ms: 0.238465
  ...
# Subtest: dateMarkContentStart finds content on list, quoted, and plain lines
ok 395 - dateMarkContentStart finds content on list, quoted, and plain lines
  ---
  duration_ms: 0.10487
  ...
# Subtest: dateMarkRelativePhrase covers the exact-day phrases
ok 396 - dateMarkRelativePhrase covers the exact-day phrases
  ---
  duration_ms: 0.08383
  ...
# Subtest: dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
ok 397 - dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
  ---
  duration_ms: 0.379193
  ...
# Subtest: no model output contains a double colon
ok 398 - no model output contains a double colon
  ---
  duration_ms: 1.092756
  ...
# Subtest: a new day always changes the widget key
ok 399 - a new day always changes the widget key
  ---
  duration_ms: 0.142783
  ...
# Subtest: element structure and the decorative/inheritColor/rendered options
ok 400 - element structure and the decorative/inheritColor/rendered options
  ---
  duration_ms: 0.418278
  ...
# Subtest: Live Preview emits several decorations in ascending order
ok 401 - Live Preview emits several decorations in ascending order
  ---
  duration_ms: 0.954442
  ...
# Subtest: Live Preview reveals per field, never the whole line
ok 402 - Live Preview reveals per field, never the whole line
  ---
  duration_ms: 0.284653
  ...
# Subtest: Live Preview refuses source mode, code, and disabled marks
ok 403 - Live Preview refuses source mode, code, and disabled marks
  ---
  duration_ms: 0.418359
  ...
# Subtest: widget mousedown anchors at the field start for folds 0, 1, and 2
ok 404 - widget mousedown anchors at the field start for folds 0, 1, and 2
  ---
  duration_ms: 0.827449
  ...
# Subtest: DM24 a cursor in the folded run unfolds the mark (vim cw)
ok 405 - DM24 a cursor in the folded run unfolds the mark (vim cw)
  ---
  duration_ms: 0.23048
  ...
# Subtest: DM25 a cursor in Tasks double space unfolds only that field
ok 406 - DM25 a cursor in Tasks double space unfolds only that field
  ---
  duration_ms: 0.165636
  ...
# Subtest: a selection ending inside the run unfolds; ending at its start keeps the fold
ok 407 - a selection ending inside the run unfolds; ending at its start keeps the fold
  ---
  duration_ms: 0.16259
  ...
# Subtest: no emitted decoration ever hides a cursor, and reveal still means field overlap
ok 408 - no emitted decoration ever hides a cursor, and reveal still means field overlap
  ---
  duration_ms: 8.835165
  ...
# Subtest: dateMarkSelectionFold: reveal, unfold, fold, and garbage input
ok 409 - dateMarkSelectionFold: reveal, unfold, fold, and garbage input
  ---
  duration_ms: 0.197346
  ...
# Subtest: mousedown on an unfolded (fold-0) widget anchors at the field start
ok 410 - mousedown on an unfolded (fold-0) widget anchors at the field start
  ---
  duration_ms: 0.300253
  ...
# Subtest: rendered views split several fields in one node
ok 411 - rendered views split several fields in one node
  ---
  duration_ms: 1.3407
  ...
# Subtest: rendered views skip exclusions and duplicates
ok 412 - rendered views skip exclusions and duplicates
  ---
  duration_ms: 0.479045
  ...
# Subtest: RO1 rendered marks relabel in place across midnight
ok 413 - RO1 rendered marks relabel in place across midnight
  ---
  duration_ms: 0.452864
  ...
# Subtest: rollover dispatches once per day change and never touches widgets
ok 414 - rollover dispatches once per day change and never touches widgets
  ---
  duration_ms: 0.33005
  ...
# Subtest: api.dateMarks v1 is additive, sync, and never throwing
ok 415 - api.dateMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.433227
  ...
# Subtest: session toggle and onload wiring
ok 416 - session toggle and onload wiring
  ---
  duration_ms: 3.124073
  ...
# Subtest: styles.css contract: masks, tones, repair flag, resting
ok 417 - styles.css contract: masks, tones, repair flag, resting
  ---
  duration_ms: 0.693474
  ...
# Subtest: DP parse vectors
ok 418 - DP parse vectors
  ---
  duration_ms: 3.125907
  ...
# Subtest: DC chip model vectors
ok 419 - DC chip model vectors
  ---
  duration_ms: 2.312795
  ...
# Subtest: decoration builds one widget, reveals on cursor, skips code and ranges
ok 420 - decoration builds one widget, reveals on cursor, skips code and ranges
  ---
  duration_ms: 8.956347
  ...
# Subtest: decoration skips paragraphs, grandchildren, and Work Log lines
ok 421 - decoration skips paragraphs, grandchildren, and Work Log lines
  ---
  duration_ms: 2.426392
  ...
# Subtest: decoration renders chips on DP30 and still skips DP20
ok 422 - decoration renders chips on DP30 and still skips DP20
  ---
  duration_ms: 0.852999
  ...
# Subtest: ownership check reads O(depth) lines, not the whole note
ok 423 - ownership check reads O(depth) lines, not the whole note
  ---
  duration_ms: 1.087666
  ...
# Subtest: widget identity covers the line and the interactive flag
ok 424 - widget identity covers the line and the interactive flag
  ---
  duration_ms: 1.511856
  ...
# Subtest: element hides actions without nav api v1
ok 425 - element hides actions without nav api v1
  ---
  duration_ms: 0.723961
  ...
# Subtest: nav api feature detection gates actions
ok 426 - nav api feature detection gates actions
  ---
  duration_ms: 0.404001
  ...
# Subtest: reading view decorates only the Depends-On row, hides chrome, stays idempotent
ok 427 - reading view decorates only the Depends-On row, hides chrome, stays idempotent
  ---
  duration_ms: 2.917649
  ...
# Subtest: reading view collapses more than three Done targets to one chip
ok 428 - reading view collapses more than three Done targets to one chip
  ---
  duration_ms: 1.327063
  ...
# Subtest: DC chip model vectors by id: DC2, DC5, DC6, DC9
ok 429 - DC chip model vectors by id: DC2, DC5, DC6, DC9
  ---
  duration_ms: 0.330221
  ...
# Subtest: chip actions send the 0-based line index through nav api v1
ok 430 - chip actions send the 0-based line index through nav api v1
  ---
  duration_ms: 1.083659
  ...
# Subtest: chip hover passes the chip element and its row to the preview
ok 431 - chip hover passes the chip element and its row to the preview
  ---
  duration_ms: 0.162761
  ...
# Subtest: chip lookup index lives on the freshness memo
ok 432 - chip lookup index lives on the freshness memo
  ---
  duration_ms: 0.469316
  ...
# Subtest: reading view hides actions when the line cannot be derived
ok 433 - reading view hides actions when the line cannot be derived
  ---
  duration_ms: 10.161035
  ...
# Subtest: reading view actions carry the derived 0-based line
ok 434 - reading view actions carry the derived 0-based line
  ---
  duration_ms: 2.212745
  ...
# Subtest: reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
ok 435 - reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
  ---
  duration_ms: 0.569918
  ...
# Subtest: reading view renders chips on DP30 (owner is a task under a Work Log entry)
ok 436 - reading view renders chips on DP30 (owner is a task under a Work Log entry)
  ---
  duration_ms: 0.58165
  ...
# Subtest: reading view DP30 row actions send the owned Depends-On line
ok 437 - reading view DP30 row actions send the owned Depends-On line
  ---
  duration_ms: 3.265693
  ...
# Subtest: reading view second-row remove sends the second line when two tasks share a prerequisite
ok 438 - reading view second-row remove sends the second line when two tasks share a prerequisite
  ---
  duration_ms: 1.631836
  ...
# Subtest: chip lookup index builds once per freshness memo
ok 439 - chip lookup index builds once per freshness memo
  ---
  duration_ms: 0.369215
  ...
# Subtest: decoration evaluates ownership without copying the note
ok 440 - decoration evaluates ownership without copying the note
  ---
  duration_ms: 0.418218
  ...
# Subtest: toggle flips the body class and onload wires chips
ok 441 - toggle flips the body class and onload wires chips
  ---
  duration_ms: 3.039822
  ...
# Subtest: capability: nav card v2 is capable
ok 442 - capability: nav card v2 is capable
  ---
  duration_ms: 0.945054
  ...
# Subtest: capability: nav card v1 is not capable
ok 443 - capability: nav card v1 is not capable
  ---
  duration_ms: 0.181216
  ...
# Subtest: capability: absent nav, missing api, and old versions are not capable
ok 444 - capability: absent nav, missing api, and old versions are not capable
  ---
  duration_ms: 0.141039
  ...
# Subtest: capability: a throwing app never throws
ok 445 - capability: a throwing app never throws
  ---
  duration_ms: 0.201224
  ...
# Subtest: leaf: active capable due choice replaces refresh with a leaf
ok 446 - leaf: active capable due choice replaces refresh with a leaf
  ---
  duration_ms: 3.116459
  ...
# Subtest: leaf: the same row without the card keeps refresh and counting words
ok 447 - leaf: the same row without the card keeps refresh and counting words
  ---
  duration_ms: 0.48231
  ...
# Subtest: leaf: early dates still leaf when capable
ok 448 - leaf: early dates still leaf when capable
  ---
  duration_ms: 0.411836
  ...
# Subtest: leaf: decay-off rows never leaf even when capable
ok 449 - leaf: decay-off rows never leaf even when capable
  ---
  duration_ms: 0.39785
  ...
# Subtest: leaf: below-threshold rows never leaf
ok 450 - leaf: below-threshold rows never leaf
  ---
  duration_ms: 0.538187
  ...
# Subtest: leaf: threshold zero asks on every due re-confirmation when capable
ok 451 - leaf: threshold zero asks on every due re-confirmation when capable
  ---
  duration_ms: 0.572302
  ...
# Subtest: leaf: overflow renders capped dots with +N and the exact count in text
ok 452 - leaf: overflow renders capped dots with +N and the exact count in text
  ---
  duration_ms: 0.351151
  ...
# Subtest: leaf: out-of-scope and closed tasks show dots quietly, never a leaf
ok 453 - leaf: out-of-scope and closed tasks show dots quietly, never a leaf
  ---
  duration_ms: 0.747708
  ...
# Subtest: leaf: unresolved marks show dots quietly with counting-only wording
ok 454 - leaf: unresolved marks show dots quietly with counting-only wording
  ---
  duration_ms: 0.219559
  ...
# Subtest: element: leaf marks carry data-decide true and a leaf path
ok 455 - element: leaf marks carry data-decide true and a leaf path
  ---
  duration_ms: 0.726136
  ...
# Subtest: element: non-decision marks carry data-decide false
ok 456 - element: non-decision marks carry data-decide false
  ---
  duration_ms: 0.28314
  ...
# Subtest: footer groups omit every zero tier and keep walk order
ok 457 - footer groups omit every zero tier and keep walk order
  ---
  duration_ms: 1.633017
  ...
# Subtest: PRE and POST groups bracket the nine-tier queue and expose completion hints
ok 458 - PRE and POST groups bracket the nine-tier queue and expose completion hints
  ---
  duration_ms: 0.8589
  ...
# Subtest: a NEW-state project appears only in its walk tier
ok 459 - a NEW-state project appears only in its walk tier
  ---
  duration_ms: 0.206985
  ...
# Subtest: empty queue hides the footer even with upkeep or a met budget
ok 460 - empty queue hides the footer even with upkeep or a met budget
  ---
  duration_ms: 0.152742
  ...
# Subtest: unavailable or missing data never render false counts
ok 461 - unavailable or missing data never render false counts
  ---
  duration_ms: 0.140468
  ...
# Subtest: generic summary names due, commitments, and nonempty groups
ok 462 - generic summary names due, commitments, and nonempty groups
  ---
  duration_ms: 0.301325
  ...
# Subtest: current-task context uses shared ranks and compact wording
ok 463 - current-task context uses shared ranks and compact wording
  ---
  duration_ms: 0.688505
  ...
# Subtest: only ROTTEN remaining names commitments done or a met budget
ok 464 - only ROTTEN remaining names commitments done or a met budget
  ---
  duration_ms: 0.290635
  ...
# Subtest: NEW and commitments take precedence over a met budget
ok 465 - NEW and commitments take precedence over a met budget
  ---
  duration_ms: 0.362492
  ...
# Subtest: reviewEntryView compact and detail cover the original freshness tiers
ok 466 - reviewEntryView compact and detail cover the original freshness tiers
  ---
  duration_ms: 0.745302
  ...
# Subtest: cursor matching requires a unique verified identity
ok 467 - cursor matching requires a unique verified identity
  ---
  duration_ms: 0.342824
  ...
# Subtest: footer paint hides the host and keeps a stable button
ok 468 - footer paint hides the host and keeps a stable button
  ---
  duration_ms: 1.054162
  ...
# Subtest: status bar 0-1-0 transitions hide without a reload
ok 469 - status bar 0-1-0 transitions hide without a reload
  ---
  duration_ms: 7.290437
  ...
# Subtest: cursor-only updates reuse a warm memo
ok 470 - cursor-only updates reuse a warm memo
  ---
  duration_ms: 1.264172
  ...
# Subtest: unload disconnects the observer and click handler
ok 471 - unload disconnects the observer and click handler
  ---
  duration_ms: 2.93423
  ...
# Subtest: queue-built ranks agree with the footer current entry
ok 472 - queue-built ranks agree with the footer current entry
  ---
  duration_ms: 0.825365
  ...
# Subtest: footer short labels map every tier
ok 473 - footer short labels map every tier
  ---
  duration_ms: 0.121071
  ...
# Subtest: current-row footer context uses short labels while entry views keep full labels
ok 474 - current-row footer context uses short labels while entry views keep full labels
  ---
  duration_ms: 0.241631
  ...
# Subtest: legend line lists only current abbreviated tiers
ok 475 - legend line lists only current abbreviated tiers
  ---
  duration_ms: 0.253754
  ...
# Subtest: K1 absent: no keeps means 0 with no lints
ok 476 - K1 absent: no keeps means 0 with no lints
  ---
  duration_ms: 2.426562
  ...
# Subtest: K8 misplaced: keeps inside the Tasks suffix reads with a lint
ok 477 - K8 misplaced: keeps inside the Tasks suffix reads with a lint
  ---
  duration_ms: 0.414912
  ...
# Subtest: K9 duplicates and invalid values: first valid wins, else 0
ok 478 - K9 duplicates and invalid values: first valid wins, else 0
  ---
  duration_ms: 0.607038
  ...
# Subtest: K10 ceiling and NEW: 999 reads, never-confirmed reads 0
ok 479 - K10 ceiling and NEW: 999 reads, never-confirmed reads 0
  ---
  duration_ms: 0.195273
  ...
# Subtest: K13 exact keys: near-miss keys are not keeps; parens read
ok 480 - K13 exact keys: near-miss keys are not keeps; parens read
  ---
  duration_ms: 0.195744
  ...
# Subtest: keeps value parser accepts only decimal 1-999
ok 481 - keeps value parser accepts only decimal 1-999
  ---
  duration_ms: 0.176076
  ...
# Subtest: K2 first valid canonical: uncounted keep preserves and repairs
ok 482 - K2 first valid canonical: uncounted keep preserves and repairs
  ---
  duration_ms: 0.77026
  ...
# Subtest: K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
ok 483 - K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
  ---
  duration_ms: 0.494665
  ...
# Subtest: K4 same-day preserve noop: canonical kept line is byte-identical
ok 484 - K4 same-day preserve noop: canonical kept line is byte-identical
  ---
  duration_ms: 0.415073
  ...
# Subtest: K5 generic stamp clears, even same-day
ok 485 - K5 generic stamp clears, even same-day
  ---
  duration_ms: 0.461461
  ...
# Subtest: K6 set-refresh clears keeps
ok 486 - K6 set-refresh clears keeps
  ---
  duration_ms: 0.285595
  ...
# Subtest: K7 stale stamp clears keeps
ok 487 - K7 stale stamp clears keeps
  ---
  duration_ms: 0.171537
  ...
# Subtest: K8b misplaced keeps repaired to canonical order by a keep
ok 488 - K8b misplaced keeps repaired to canonical order by a keep
  ---
  duration_ms: 0.191666
  ...
# Subtest: K11 refusals preserve: closed and recurring lines never write
ok 489 - K11 refusals preserve: closed and recurring lines never write
  ---
  duration_ms: 1.8706
  ...
# Subtest: counted keep increments a stale streak once in the same write
ok 490 - counted keep increments a stale streak once in the same write
  ---
  duration_ms: 0.227524
  ...
# Subtest: first counted keep on a streakless due task writes keeps 1
ok 491 - first counted keep on a streakless due task writes keeps 1
  ---
  duration_ms: 0.138825
  ...
# Subtest: counted keep saturates at 999 and never wraps
ok 492 - counted keep saturates at 999 and never wraps
  ---
  duration_ms: 0.217466
  ...
# Subtest: counted keep needs a valid prior fresh before today
ok 493 - counted keep needs a valid prior fresh before today
  ---
  duration_ms: 0.271388
  ...
# Subtest: counted keep repairs malformed and duplicate placement
ok 494 - counted keep repairs malformed and duplicate placement
  ---
  duration_ms: 0.218507
  ...
# Subtest: uncounted keep preserves the valid value while canonicalizing
ok 495 - uncounted keep preserves the valid value while canonicalizing
  ---
  duration_ms: 0.195604
  ...
# Subtest: UB13 keep on an unblock TICKLER preserves the streak and skips the card
ok 496 - UB13 keep on an unblock TICKLER preserves the streak and skips the card
  ---
  duration_ms: 0.747036
  ...
# Subtest: a scheduled tickler still counts when schedule wins an unblock tie
ok 497 - a scheduled tickler still counts when schedule wins an unblock tie
  ---
  duration_ms: 0.273382
  ...
# Subtest: decay normalization: absent, null, true, and {} enable with 3
ok 498 - decay normalization: absent, null, true, and {} enable with 3
  ---
  duration_ms: 0.695086
  ...
# Subtest: decay false counts and displays but never asks
ok 499 - decay false counts and displays but never asks
  ---
  duration_ms: 0.149595
  ...
# Subtest: decay keeps 0 and fixed entry normalize
ok 500 - decay keeps 0 and fixed entry normalize
  ---
  duration_ms: 0.140318
  ...
# Subtest: invalid decay shapes fail the freshness config contract
ok 501 - invalid decay shapes fail the freshness config contract
  ---
  duration_ms: 0.260007
  ...
# Subtest: B: at-limit Ready due rows decide on every local day
ok 502 - B: at-limit Ready due rows decide on every local day
  ---
  duration_ms: 0.462403
  ...
# Subtest: D1 early date: an at-limit Ready due row decides
ok 503 - D1 early date: an at-limit Ready due row decides
  ---
  duration_ms: 0.109058
  ...
# Subtest: D2 at limit decides; D3 below limit stamps without a card
ok 504 - D2 at limit decides; D3 below limit stamps without a card
  ---
  duration_ms: 0.117515
  ...
# Subtest: D4 tickler counts as due; D5 NEW never decides
ok 505 - D4 tickler counts as due; D5 NEW never decides
  ---
  duration_ms: 0.171497
  ...
# Subtest: D6 zero limit asks on every due Ready re-confirmation
ok 506 - D6 zero limit asks on every due Ready re-confirmation
  ---
  duration_ms: 0.085754
  ...
# Subtest: D7 off never asks; D8 lane rows never decide
ok 507 - D7 off never asks; D8 lane rows never decide
  ---
  duration_ms: 0.075274
  ...
# Subtest: evaluator, queue, and counts carry keeps and decide
ok 508 - evaluator, queue, and counts carry keeps and decide
  ---
  duration_ms: 1.085752
  ...
# Subtest: no keeps: the existing mark is unchanged
ok 509 - no keeps: the existing mark is unchanged
  ---
  duration_ms: 0.899326
  ...
# Subtest: aging with two keeps: faint pips plus a counting-only line
ok 510 - aging with two keeps: faint pips plus a counting-only line
  ---
  duration_ms: 0.281858
  ...
# Subtest: confirmed today with two keeps: check glyph, faint dots
ok 511 - confirmed today with two keeps: check glyph, faint dots
  ---
  duration_ms: 0.207816
  ...
# Subtest: due below threshold: orange capsule keeps its glyph, adds dots
ok 512 - due below threshold: orange capsule keeps its glyph, adds dots
  ---
  duration_ms: 0.213798
  ...
# Subtest: resting marks show historical dots quietly and never decide
ok 513 - resting marks show historical dots quietly and never decide
  ---
  duration_ms: 0.31431
  ...
# Subtest: active decision due: data stays truthful, leaf stays gated
ok 514 - active decision due: data stays truthful, leaf stays gated
  ---
  duration_ms: 0.233005
  ...
# Subtest: dot caps follow the threshold with +N overflow
ok 515 - dot caps follow the threshold with +N overflow
  ---
  duration_ms: 0.582442
  ...
# Subtest: keeps tooltip wording: singulars, zero threshold, off state
ok 516 - keeps tooltip wording: singulars, zero threshold, off state
  ---
  duration_ms: 0.1048
  ...
# Subtest: noncanonical keeps never fold but keep their repair pill
ok 517 - noncanonical keeps never fold but keep their repair pill
  ---
  duration_ms: 0.317196
  ...
# Subtest: quoted lines fold; rendered fragments fold without task checks
ok 518 - quoted lines fold; rendered fragments fold without task checks
  ---
  duration_ms: 0.196956
  ...
# Subtest: unresolved marks show the line's own pips quietly and never decide
ok 519 - unresolved marks show the line's own pips quietly and never decide
  ---
  duration_ms: 0.174313
  ...
# Subtest: consensus sees count and decision eligibility: ambiguity stays neutral
ok 520 - consensus sees count and decision eligibility: ambiguity stays neutral
  ---
  duration_ms: 0.406506
  ...
# Subtest: pips render as one aria-hidden span with the count in the label
ok 521 - pips render as one aria-hidden span with the count in the label
  ---
  duration_ms: 0.941628
  ...
# Subtest: Live Preview decorates the folded range including space and refresh
ok 522 - Live Preview decorates the folded range including space and refresh
  ---
  duration_ms: 5.691174
  ...
# Subtest: Live Preview reveals the raw field when the cursor overlaps either edge
ok 523 - Live Preview reveals the raw field when the cursor overlaps either edge
  ---
  duration_ms: 1.429018
  ...
# Subtest: Live Preview skips codeblock and inline code spans
ok 524 - Live Preview skips codeblock and inline code spans
  ---
  duration_ms: 0.664469
  ...
# Subtest: source mode and marks-off yield no decorations
ok 525 - source mode and marks-off yield no decorations
  ---
  duration_ms: 0.166668
  ...
# Subtest: update rebuilds on the refresh effect and widget eq is stable
ok 526 - update rebuilds on the refresh effect and widget eq is stable
  ---
  duration_ms: 1.005248
  ...
# Subtest: widget click reveals the field at the folded offset
ok 527 - widget click reveals the field at the folded offset
  ---
  duration_ms: 0.68663
  ...
# Subtest: line resolver prefers exact, then consensus, then unresolved
ok 528 - line resolver prefers exact, then consensus, then unresolved
  ---
  duration_ms: 1.181856
  ...
# Subtest: decoration builds reuse the snapshot without touching the loader
ok 529 - decoration builds reuse the snapshot without touching the loader
  ---
  duration_ms: 0.393961
  ...
# Subtest: rendered views split text nodes and skip excluded ancestors
ok 530 - rendered views split text nodes and skip excluded ancestors
  ---
  duration_ms: 1.414449
  ...
# Subtest: rendered views stay idempotent
ok 531 - rendered views stay idempotent
  ---
  duration_ms: 2.223033
  ...
# Subtest: text resolver reaches consensus and degrades to neutral
ok 532 - text resolver reaches consensus and degrades to neutral
  ---
  duration_ms: 0.680419
  ...
# Subtest: session toggle flips the body class and notifies
ok 533 - session toggle flips the body class and notifies
  ---
  duration_ms: 0.787353
  ...
# Subtest: onload registers the toggle, extension, and post-processor
ok 534 - onload registers the toggle, extension, and post-processor
  ---
  duration_ms: 2.825715
  ...
# Subtest: M1 today: check glyph, today label, full ring
ok 535 - M1 today: check glyph, today label, full ring
  ---
  duration_ms: 3.51553
  ...
# Subtest: M2 aging: ring glyph, 3d label, draining lease
ok 536 - M2 aging: ring glyph, 3d label, draining lease
  ---
  duration_ms: 0.511687
  ...
# Subtest: M3 boundary: ROTTEN due capsule with Alt+F hint
ok 537 - M3 boundary: ROTTEN due capsule with Alt+F hint
  ---
  duration_ms: 0.357693
  ...
# Subtest: checklist marks replace stamp hints with their completion tier
ok 538 - checklist marks replace stamp hints with their completion tier
  ---
  duration_ms: 0.668286
  ...
# Subtest: M4 yesterday uses the yesterday relative
ok 539 - M4 yesterday uses the yesterday relative
  ---
  duration_ms: 0.271739
  ...
# Subtest: M5 folded refresh shows the /14d suffix
ok 540 - M5 folded refresh shows the /14d suffix
  ---
  duration_ms: 0.417738
  ...
# Subtest: M6 refresh today: today tone hides the interval suffix
ok 541 - M6 refresh today: today tone hides the interval suffix
  ---
  duration_ms: 0.301125
  ...
# Subtest: M7 note interval stays tooltip-only
ok 542 - M7 note interval stays tooltip-only
  ---
  duration_ms: 0.462804
  ...
# Subtest: M8 resurfaced: due tone on the scheduled return
ok 543 - M8 resurfaced: due tone on the scheduled return
  ---
  duration_ms: 0.48151
  ...
# Subtest: M9 due NEXT lane with keep/release/today keys
ok 544 - M9 due NEXT lane with keep/release/today keys
  ---
  duration_ms: 0.567633
  ...
# Subtest: M10 NEXT lane stamped today
ok 545 - M10 NEXT lane stamped today
  ---
  duration_ms: 0.28859
  ...
# Subtest: M19 disabled Next lane rests
ok 546 - M19 disabled Next lane rests
  ---
  duration_ms: 0.268883
  ...
# Subtest: M20 PENDING lane folds refresh without the suffix
ok 547 - M20 PENDING lane folds refresh without the suffix
  ---
  duration_ms: 1.491076
  ...
# Subtest: M11 closed: resting beats age 0
ok 548 - M11 closed: resting beats age 0
  ---
  duration_ms: 0.244907
  ...
# Subtest: M12 unresolved running and M13 unresolved lease over
ok 549 - M12 unresolved running and M13 unresolved lease over
  ---
  duration_ms: 0.231401
  ...
# Subtest: M14 linked today rests with its reason
ok 550 - M14 linked today rests with its reason
  ---
  duration_ms: 0.174603
  ...
# Subtest: M15 other year shows the year and the 282d age
ok 551 - M15 other year shows the year and the 282d age
  ---
  duration_ms: 0.127684
  ...
# Subtest: M16 quoted line keeps foldSpace
ok 552 - M16 quoted line keeps foldSpace
  ---
  duration_ms: 0.128084
  ...
# Subtest: M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
ok 553 - M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
  ---
  duration_ms: 0.351991
  ...
# Subtest: N1-N6 non-canonical lines get no mark
ok 554 - N1-N6 non-canonical lines get no mark
  ---
  duration_ms: 0.161719
  ...
# Subtest: C1-C3 consensus is exact or unresolved
ok 555 - C1-C3 consensus is exact or unresolved
  ---
  duration_ms: 0.609503
  ...
# Subtest: freshnessMarkResolution treats evaluator new as unresolved
ok 556 - freshnessMarkResolution treats evaluator new as unresolved
  ---
  duration_ms: 0.124838
  ...
# Subtest: freshnessMarkSourceInText covers rendered fragments
ok 557 - freshnessMarkSourceInText covers rendered fragments
  ---
  duration_ms: 0.190714
  ...
# Subtest: tone order: closed, then due, then age 0, then out of scope
ok 558 - tone order: closed, then due, then age 0, then out of scope
  ---
  duration_ms: 0.355349
  ...
# Subtest: no tooltip ever contains a double colon
ok 559 - no tooltip ever contains a double colon
  ---
  duration_ms: 0.611999
  ...
# Subtest: freshnessShortDate pins English names and the year rule
ok 560 - freshnessShortDate pins English names and the year rule
  ---
  duration_ms: 0.107836
  ...
# Subtest: DOM builder structure, attributes, and ring geometry
ok 561 - DOM builder structure, attributes, and ring geometry
  ---
  duration_ms: 0.903825
  ...
# Subtest: every mark helper is synchronous and never throws on bad input
ok 562 - every mark helper is synchronous and never throws on bad input
  ---
  duration_ms: 0.106343
  ...
# Subtest: freshness namespace v12 exposes unblock TICKLER metadata and writers
ok 563 - freshness namespace v12 exposes unblock TICKLER metadata and writers
  ---
  duration_ms: 10.937398
  ...
# Subtest: freshness state and count API expose an unblock return source
ok 564 - freshness state and count API expose an unblock return source
  ---
  duration_ms: 1.468854
  ...
# Subtest: checklist rows report tier and rank while keeping the READY bucket null
ok 565 - checklist rows report tier and rank while keeping the READY bucket null
  ---
  duration_ms: 1.15263
  ...
# Subtest: tier, isDue, and rank cover lane rows
ok 566 - tier, isDue, and rank cover lane rows
  ---
  duration_ms: 2.502768
  ...
# Subtest: memo invalidates on a new tasks array, rollover, and frontmatter
ok 567 - memo invalidates on a new tasks array, rollover, and frontmatter
  ---
  duration_ms: 5.044489
  ...
# Subtest: the reload event fires only when the due key set changes
ok 568 - the reload event fires only when the due key set changes
  ---
  duration_ms: 1.342623
  ...
# Subtest: status bar text covers every state, and a missing host stays quiet
ok 569 - status bar text covers every state, and a missing host stays quiet
  ---
  duration_ms: 1.100942
  ...
# Subtest: status bar clicks through, falling back to rotten
ok 570 - status bar clicks through, falling back to rotten
  ---
  duration_ms: 3.463922
  ...
# Subtest: every freshness api member is synchronous and never throws
ok 571 - every freshness api member is synchronous and never throws
  ---
  duration_ms: 1.693612
  ...
# Subtest: placement vectors P1-P11, P14-P16, P18 stamp canonically
ok 572 - placement vectors P1-P11, P14-P16, P18 stamp canonically
  ---
  duration_ms: 3.969406
  ...
# Subtest: P12 set and clear refresh stamps alongside
ok 573 - P12 set and clear refresh stamps alongside
  ---
  duration_ms: 0.448326
  ...
# Subtest: P13 recurring and P17 done tasks are refused unchanged
ok 574 - P13 recurring and P17 done tasks are refused unchanged
  ---
  duration_ms: 0.224509
  ...
# Subtest: U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
ok 575 - U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
  ---
  duration_ms: 1.132492
  ...
# Subtest: reader reports misplaced and duplicate fields
ok 576 - reader reports misplaced and duplicate fields
  ---
  duration_ms: 0.322956
  ...
# Subtest: Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
ok 577 - Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
  ---
  duration_ms: 6.122418
  ...
# Subtest: Q2 tier order beats path order
ok 578 - Q2 tier order beats path order
  ---
  duration_ms: 1.384703
  ...
# Subtest: L1 lane due and stamped today
ok 579 - L1 lane due and stamped today
  ---
  duration_ms: 0.472912
  ...
# Subtest: L2 lane overrides refresh
ok 580 - L2 lane overrides refresh
  ---
  duration_ms: 0.317606
  ...
# Subtest: L3 lane exclusions have no tier
ok 581 - L3 lane exclusions have no tier
  ---
  duration_ms: 0.500746
  ...
# Subtest: L4 lane off switch and null default
ok 582 - L4 lane off switch and null default
  ---
  duration_ms: 0.318699
  ...
# Subtest: L5 lane order never stamped first
ok 583 - L5 lane order never stamped first
  ---
  duration_ms: 0.508651
  ...
# Subtest: R1 TICKLER beats older ROTTEN
ok 584 - R1 TICKLER beats older ROTTEN
  ---
  duration_ms: 0.405233
  ...
# Subtest: R2 tickler orders by due date then path and line
ok 585 - R2 tickler orders by due date then path and line
  ---
  duration_ms: 0.706558
  ...
# Subtest: missing created sorts after dated peers
ok 586 - missing created sorts after dated peers
  ---
  duration_ms: 0.945876
  ...
# Subtest: B1 upkeep counts outside the lanes
ok 587 - B1 upkeep counts outside the lanes
  ---
  duration_ms: 4.362538
  ...
# Subtest: review model meter uses upkeep and exposes refreshed
ok 588 - review model meter uses upkeep and exposes refreshed
  ---
  duration_ms: 0.476539
  ...
# Subtest: RC1 arrived: past scheduled walks RECURRING with lane and null state
ok 589 - RC1 arrived: past scheduled walks RECURRING with lane and null state
  ---
  duration_ms: 2.951825
  ...
# Subtest: RC2 arrives today: due today with zero days overdue
ok 590 - RC2 arrives today: due today with zero days overdue
  ---
  duration_ms: 0.340139
  ...
# Subtest: RC3 not yet: future scheduled walks nowhere
ok 591 - RC3 not yet: future scheduled walks nowhere
  ---
  duration_ms: 0.244476
  ...
# Subtest: RC4 due only, past: the due date is the occurrence
ok 592 - RC4 due only, past: the due date is the occurrence
  ---
  duration_ms: 0.223557
  ...
# Subtest: RC5 due only, future: walks nowhere
ok 593 - RC5 due only, future: walks nowhere
  ---
  duration_ms: 0.244407
  ...
# Subtest: RC6 earliest date wins across start and due
ok 594 - RC6 earliest date wins across start and due
  ---
  duration_ms: 0.257311
  ...
# Subtest: RC7 undated: no occurrence, no tier
ok 595 - RC7 undated: no occurrence, no tier
  ---
  duration_ms: 0.30405
  ...
# Subtest: RC8 lanes: recurring lane rows keep their lane with null state
ok 596 - RC8 lanes: recurring lane rows keep their lane with null state
  ---
  duration_ms: 0.47147
  ...
# Subtest: RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
ok 597 - RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
  ---
  duration_ms: 1.614251
  ...
# Subtest: RC10 checklist wins: a recurring chore stays in its checklist tier
ok 598 - RC10 checklist wins: a recurring chore stays in its checklist tier
  ---
  duration_ms: 0.422717
  ...
# Subtest: RC11 a stray stamp is ignored: recurring with null state
ok 599 - RC11 a stray stamp is ignored: recurring with null state
  ---
  duration_ms: 0.365607
  ...
# Subtest: RC12 order and counts: due_on, then path, then line; recurring adds no due
ok 600 - RC12 order and counts: due_on, then path, then line; recurring adds no due
  ---
  duration_ms: 1.064512
  ...
# Subtest: recurring rows adapt due and start from Tasks fields and inline fallbacks
ok 601 - recurring rows adapt due and start from Tasks fields and inline fallbacks
  ---
  duration_ms: 1.192346
  ...
# Subtest: status view counts RECURRING as a due commitment tier
ok 602 - status view counts RECURRING as a due commitment tier
  ---
  duration_ms: 0.31465
  ...
# Subtest: footer groups, entry view, and legend cover RECURRING
ok 603 - footer groups, entry view, and legend cover RECURRING
  ---
  duration_ms: 0.78607
  ...
# Subtest: a stale-stamped recurring row marks due with the resolve hint
ok 604 - a stale-stamped recurring row marks due with the resolve hint
  ---
  duration_ms: 0.883767
  ...
# Subtest: freshness namespace v12 keeps recurring and removes reference capabilities
ok 605 - freshness namespace v12 keeps recurring and removes reference capabilities
  ---
  duration_ms: 5.237046
  ...
# Subtest: hidden recurring ^ref keeps ordinary visibility (Rust parity)
ok 606 - hidden recurring ^ref keeps ordinary visibility (Rust parity)
  ---
  duration_ms: 0.839052
  ...
# Subtest: bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
ok 607 - bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
  ---
  duration_ms: 3.621003
  ...
# Subtest: day numbers stay calendar-local across a DST boundary
ok 608 - day numbers stay calendar-local across a DST boundary
  ---
  duration_ms: 0.441403
  ...
# Subtest: reviewModel shares counts, meter, tooltip, and severity
ok 609 - reviewModel shares counts, meter, tooltip, and severity
  ---
  duration_ms: 0.444187
  ...
# Subtest: memo serves warm map hits and misses use the per-row evaluator
ok 610 - memo serves warm map hits and misses use the per-row evaluator
  ---
  duration_ms: 6.345912
  ...
# Subtest: config snapshot caches the parse and invalidates explicitly
ok 611 - config snapshot caches the parse and invalidates explicitly
  ---
  duration_ms: 1.395744
  ...
# Subtest: review chips share the model with severity classes
ok 612 - review chips share the model with severity classes
  ---
  duration_ms: 1.004017
  ...
# Subtest: warm lookups reuse one snapshot without re-reading config
ok 613 - warm lookups reuse one snapshot without re-reading config
  ---
  duration_ms: 1.699575
  ...
# Subtest: same-array cache updates and Today changes rebuild the memo
ok 614 - same-array cache updates and Today changes rebuild the memo
  ---
  duration_ms: 4.5635
  ...
# Subtest: duplicate block IDs keep each row's own classification
ok 615 - duplicate block IDs keep each row's own classification
  ---
  duration_ms: 1.850814
  ...
# Subtest: line identity separates same-path rows without block IDs
ok 616 - line identity separates same-path rows without block IDs
  ---
  duration_ms: 1.008275
  ...
# Subtest: interval lookup serves the cached interval with one memo acquisition
ok 617 - interval lookup serves the cached interval with one memo acquisition
  ---
  duration_ms: 1.037341
  ...
# Subtest: S1 new through S4 overdue
ok 618 - S1 new through S4 overdue
  ---
  duration_ms: 4.564392
  ...
# Subtest: S5 task beats note, S6 note beats config, S7 config
ok 619 - S5 task beats note, S6 note beats config, S7 config
  ---
  duration_ms: 0.77501
  ...
# Subtest: S8 invalid overrides fall through with lints
ok 620 - S8 invalid overrides fall through with lints
  ---
  duration_ms: 0.395154
  ...
# Subtest: S9 malformed and S10 future stamps read as new
ok 621 - S9 malformed and S10 future stamps read as new
  ---
  duration_ms: 0.222305
  ...
# Subtest: S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
ok 622 - S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
  ---
  duration_ms: 0.333196
  ...
# Subtest: S13 out-of-scope rows read null
ok 623 - S13 out-of-scope rows read null
  ---
  duration_ms: 0.312566
  ...
# Subtest: S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
ok 624 - S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
  ---
  duration_ms: 1.405413
  ...
# Subtest: S15 counts (updated): upkeep outside the lanes drives the budget
ok 625 - S15 counts (updated): upkeep outside the lanes drives the budget
  ---
  duration_ms: 1.261709
  ...
# Subtest: config coercion keeps defaults, flags invalid, ignores unknown keys
ok 626 - config coercion keeps defaults, flags invalid, ignores unknown keys
  ---
  duration_ms: 1.306584
  ...
# Subtest: loadFreshnessConfig reads the block with plan-style injectables
ok 627 - loadFreshnessConfig reads the block with plan-style injectables
  ---
  duration_ms: 0.89623
  ...
# Subtest: interval precedence is task, note, config, default
ok 628 - interval precedence is task, note, config, default
  ---
  duration_ms: 0.220551
  ...
# Subtest: intervalForLine covers every source with its Ready fallback
ok 629 - intervalForLine covers every source with its Ready fallback
  ---
  duration_ms: 0.7069
  ...
# Subtest: project tracking stays special while reference tasks use ordinary Ready freshness
ok 630 - project tracking stays special while reference tasks use ordinary Ready freshness
  ---
  duration_ms: 4.580032
  ...
# Subtest: reference tasks match ordinary interval precedence and lane behavior
ok 631 - reference tasks match ordinary interval precedence and lane behavior
  ---
  duration_ms: 2.065804
  ...
# Subtest: obsolete reference interval keys are ignored and project config still validates
ok 632 - obsolete reference interval keys are ignored and project config still validates
  ---
  duration_ms: 0.626466
  ...
# Subtest: references use ordinary keep decisions and the nine-tier queue shape
ok 633 - references use ordinary keep decisions and the nine-tier queue shape
  ---
  duration_ms: 1.170113
  ...
# Subtest: CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
ok 634 - CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
  ---
  duration_ms: 2.366527
  ...
# Subtest: CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
ok 635 - CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
  ---
  duration_ms: 3.204027
  ...
# Subtest: freshness namespace v12 retains the tracker capability contract
ok 636 - freshness namespace v12 retains the tracker capability contract
  ---
  duration_ms: 3.404288
  ...
# Subtest: UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
ok 637 - UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
  ---
  duration_ms: 4.220677
  ...
# Subtest: UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
ok 638 - UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
  ---
  duration_ms: 0.468634
  ...
# Subtest: UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
ok 639 - UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
  ---
  duration_ms: 0.310944
  ...
# Subtest: UB11 scheduled wins a tie with the unblock date
ok 640 - UB11 scheduled wins a tie with the unblock date
  ---
  duration_ms: 0.281247
  ...
# Subtest: unblocked reader takes the latest valid duplicate and reports malformed values
ok 641 - unblocked reader takes the latest valid duplicate and reports malformed values
  ---
  duration_ms: 0.268523
  ...
# Subtest: UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
ok 642 - UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
  ---
  duration_ms: 0.427115
  ...
# Subtest: UB14 TICKLERs with the same due date sort only by path and line
ok 643 - UB14 TICKLERs with the same due date sort only by path and line
  ---
  duration_ms: 1.458154
  ...
# Subtest: UB15 a scheduled ^prj resurfaces in PROJECTS
ok 644 - UB15 a scheduled ^prj resurfaces in PROJECTS
  ---
  duration_ms: 0.231923
  ...
# Subtest: an active-note Pomodoro target still jumps and centers immediately
ok 645 - an active-note Pomodoro target still jumps and centers immediately
  ---
  duration_ms: 8.817322
  ...
# Subtest: the first fallback press only opens daily and the second press jumps
ok 646 - the first fallback press only opens daily and the second press jumps
  ---
  duration_ms: 2.172617
  ...
# Subtest: a daily note with no target defers its notice until the second press
ok 647 - a daily note with no target defers its notice until the second press
  ---
  duration_ms: 0.90084
  ...
# Subtest: an already-open daily leaf retains its live cursor and viewport
ok 648 - an already-open daily leaf retains its live cursor and viewport
  ---
  duration_ms: 1.23091
  ...
# Subtest: a second press after reused-leaf fallback performs the Pomodoro jump
ok 649 - a second press after reused-leaf fallback performs the Pomodoro jump
  ---
  duration_ms: 1.148632
  ...
# Subtest: the standalone daily-note command activates a reused daily leaf
ok 650 - the standalone daily-note command activates a reused daily leaf
  ---
  duration_ms: 0.898615
  ...
# Subtest: a closed then reopened daily note restores its in-session location
ok 651 - a closed then reopened daily note restores its in-session location
  ---
  duration_ms: 6.744926
  ...
# Subtest: different-path and invalid locations do not leak into a daily note
ok 652 - different-path and invalid locations do not leak into a daily note
  ---
  duration_ms: 1.305772
  ...
# Subtest: out-of-range remembered coordinates are clamped safely
ok 653 - out-of-range remembered coordinates are clamped safely
  ---
  duration_ms: 2.576559
  ...
# Subtest: a rapid second press cancels an older fallback restore
ok 654 - a rapid second press cancels an older fallback restore
  ---
  duration_ms: 1.51381
  ...
# Subtest: navigation and unload clean up daily scroll listeners and deferred work
ok 655 - navigation and unload clean up daily scroll listeners and deferred work
  ---
  duration_ms: 0.820837
  ...
# Subtest: crowded chip: over count is red with tooltip, aria, and names
ok 656 - crowded chip: over count is red with tooltip, aria, and names
  ---
  duration_ms: 1.196364
  ...
# Subtest: crowded chip: calm zero and unavailable dash
ok 657 - crowded chip: calm zero and unavailable dash
  ---
  duration_ms: 0.209079
  ...
# Subtest: crowded chip: names at most five notes
ok 658 - crowded chip: names at most five notes
  ---
  duration_ms: 0.219249
  ...
# Subtest: crowded chip: classes, text, aria, and arrow
ok 659 - crowded chip: classes, text, aria, and arrow
  ---
  duration_ms: 1.690907
  ...
# Subtest: crowded chip: refresh in place keeps the anchor, unload drops it
ok 660 - crowded chip: refresh in place keeps the anchor, unload drops it
  ---
  duration_ms: 0.681941
  ...
# Subtest: anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
ok 661 - anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
  ---
  duration_ms: 0.582512
  ...
# Subtest: ready-notes summary: crowded, calm, and unavailable
ok 662 - ready-notes summary: crowded, calm, and unavailable
  ---
  duration_ms: 0.198138
  ...
# Subtest: ready-notes bar: cap tick and red overflow within 30 cells
ok 663 - ready-notes bar: cap tick and red overflow within 30 cells
  ---
  duration_ms: 0.250368
  ...
# Subtest: ready-notes block: model and render with grid, pills, and footer
ok 664 - ready-notes block: model and render with grid, pills, and footer
  ---
  duration_ms: 1.5144
  ...
# Subtest: ready-notes block: unavailable renders a dash line
ok 665 - ready-notes block: unavailable renders a dash line
  ---
  duration_ms: 0.537366
  ...
# Subtest: heading matcher: fences, level, case, and first-only
ok 666 - heading matcher: fences, level, case, and first-only
  ---
  duration_ms: 0.465569
  ...
# Subtest: heading chip copy: room, full, crowded, exempt, unavailable
ok 667 - heading chip copy: room, full, crowded, exempt, unavailable
  ---
  duration_ms: 0.371118
  ...
# Subtest: heading chip key is stable for equal models
ok 668 - heading chip key is stable for equal models
  ---
  duration_ms: 0.177068
  ...
# Subtest: reading view: appends the chip to the matching h2 only
ok 669 - reading view: appends the chip to the matching h2 only
  ---
  duration_ms: 1.487991
  ...
# Subtest: reading view: no chip for ineligible notes
ok 670 - reading view: no chip for ineligible notes
  ---
  duration_ms: 0.144636
  ...
# Subtest: one live-refresh fan-out reaches every family
ok 671 - one live-refresh fan-out reaches every family
  ---
  duration_ms: 0.96949
  ...
# Subtest: ledger-tools CSS is theme-safe for the new views
ok 672 - ledger-tools CSS is theme-safe for the new views
  ---
  duration_ms: 0.593604
  ...
# Subtest: maxReadyPerNote defaults to 5 and validates 1–999
ok 673 - maxReadyPerNote defaults to 5 and validates 1–999
  ---
  duration_ms: 3.226519
  ...
# Subtest: loadPlanCaps caches on a stat key and detects edits
ok 674 - loadPlanCaps caches on a stat key and detects edits
  ---
  duration_ms: 0.736045
  ...
# Subtest: loadPlanCaps handles deletion, invalid edits, and recovery
ok 675 - loadPlanCaps handles deletion, invalid edits, and recovery
  ---
  duration_ms: 0.626145
  ...
# Subtest: loadPlanCaps without statSync reads through uncached
ok 676 - loadPlanCaps without statSync reads through uncached
  ---
  duration_ms: 0.400034
  ...
# Subtest: noteFrontmatter resolves through getFileCache, not getCache
ok 677 - noteFrontmatter resolves through getFileCache, not getCache
  ---
  duration_ms: 0.877545
  ...
# Subtest: task_refresh applies through the shared reader
ok 678 - task_refresh applies through the shared reader
  ---
  duration_ms: 4.078706
  ...
# Subtest: noteReadyKindFromType covers every R11 form
ok 679 - noteReadyKindFromType covers every R11 form
  ---
  duration_ms: 0.621997
  ...
# Subtest: noteReadyStatusLabel mirrors ProjectStatus::parse
ok 680 - noteReadyStatusLabel mirrors ProjectStatus::parse
  ---
  duration_ms: 0.395244
  ...
# Subtest: noteReadyParentStem strips alias, heading, and path
ok 681 - noteReadyParentStem strips alias, heading, and path
  ---
  duration_ms: 0.433798
  ...
# Subtest: parseNoteReadyCap covers every R8 form
ok 682 - parseNoteReadyCap covers every R8 form
  ---
  duration_ms: 4.622874
  ...
# Subtest: R1: 6 tasks at the default cap are crowded with over_by 1
ok 683 - R1: 6 tasks at the default cap are crowded with over_by 1
  ---
  duration_ms: 11.041166
  ...
# Subtest: R2: 5 tasks are full with no lint
ok 684 - R2: 5 tasks are full with no lint
  ---
  duration_ms: 2.781971
  ...
# Subtest: R3: hidden, future, blocked, and non-TODO rows never count
ok 685 - R3: hidden, future, blocked, and non-TODO rows never count
  ---
  duration_ms: 2.913111
  ...
# Subtest: R4: make-up splits 1 ready + 1 new + 1 rotten
ok 686 - R4: make-up splits 1 ready + 1 new + 1 rotten
  ---
  duration_ms: 2.20026
  ...
# Subtest: R5: recurring rows are excluded but tallied
ok 687 - R5: recurring rows are excluded but tallied
  ---
  duration_ms: 1.656041
  ...
# Subtest: R6: a visible ^prj task never counts
ok 688 - R6: a visible ^prj task never counts
  ---
  duration_ms: 1.315821
  ...
# Subtest: R7: daily, untyped, template, done, and dash rows are absent
ok 689 - R7: daily, untyped, template, done, and dash rows are absent
  ---
  duration_ms: 2.277567
  ...
# Subtest: R8: ready_cap forms map to cap, exempt, or lint-then-default
ok 690 - R8: ready_cap forms map to cap, exempt, or lint-then-default
  ---
  duration_ms: 3.659647
  ...
# Subtest: R9: a parent with two children counts 3
ok 691 - R9: a parent with two children counts 3
  ---
  duration_ms: 1.240367
  ...
# Subtest: R10: terminal projects are not capped and lint once
ok 692 - R10: terminal projects are not capped and lint once
  ---
  duration_ms: 1.6134
  ...
# Subtest: R11: every type form and nested folders are eligible
ok 693 - R11: every type form and nested folders are eligible
  ---
  duration_ms: 1.573053
  ...
# Subtest: R12: stamping a NEW task keeps the count and moves the make-up
ok 694 - R12: stamping a NEW task keeps the count and moves the make-up
  ---
  duration_ms: 2.832988
  ...
# Subtest: R13: a Today-linked task still counts
ok 695 - R13: a Today-linked task still counts
  ---
  duration_ms: 0.823512
  ...
# Subtest: R14: max_ready_per_note 3 caps others while ready_cap 8 holds
ok 696 - R14: max_ready_per_note 3 caps others while ready_cap 8 holds
  ---
  duration_ms: 3.309056
  ...
# Subtest: api.noteReady is frozen at version 1 under api v3
ok 697 - api.noteReady is frozen at version 1 under api v3
  ---
  duration_ms: 0.362973
  ...
# Subtest: counted and inCrowdedNote resolve per task
ok 698 - counted and inCrowdedNote resolve per task
  ---
  duration_ms: 5.016446
  ...
# Subtest: groupLabel ranks crowded notes by excess
ok 699 - groupLabel ranks crowded notes by excess
  ---
  duration_ms: 9.363203
  ...
# Subtest: snapshot sorts crowded, full, room, empty, exempt and splits totals
ok 700 - snapshot sorts crowded, full, room, empty, exempt and splits totals
  ---
  duration_ms: 9.365076
  ...
# Subtest: missing Tasks data and a cold cache are unavailable, never zero
ok 701 - missing Tasks data and a cold cache are unavailable, never zero
  ---
  duration_ms: 1.903144
  ...
# Subtest: throwing Tasks guards never throw
ok 702 - throwing Tasks guards never throw
  ---
  duration_ms: 1.182748
  ...
# Subtest: snapshot reuses the memo without reparsing or re-walking
ok 703 - snapshot reuses the memo without reparsing or re-walking
  ---
  duration_ms: 1.598851
  ...
# Subtest: a task edit rebuilds through the cache-update handler
ok 704 - a task edit rebuilds through the cache-update handler
  ---
  duration_ms: 1.746614
  ...
# Subtest: a ready_cap edit rebuilds and fires the query-refresh trigger
ok 705 - a ready_cap edit rebuilds and fires the query-refresh trigger
  ---
  duration_ms: 1.366448
  ...
# Subtest: rename and delete move the eligibility entry
ok 706 - rename and delete move the eligibility entry
  ---
  duration_ms: 3.199397
  ...
# Subtest: day rollover rebuilds the snapshot date
ok 707 - day rollover rebuilds the snapshot date
  ---
  duration_ms: 1.337103
  ...
# Subtest: a config edit flows through the stat cache
ok 708 - a config edit flows through the stat cache
  ---
  duration_ms: 38.433043
  ...
# Subtest: untyped and non-markdown vault events are no-ops
ok 709 - untyped and non-markdown vault events are no-ops
  ---
  duration_ms: 1.628069
  ...
# Subtest: memo hits never re-walk the vault
ok 710 - memo hits never re-walk the vault
  ---
  duration_ms: 69.033005
  ...
# Subtest: the startup storm is linear
ok 711 - the startup storm is linear
  ---
  duration_ms: 20.549577
  ...
# Subtest: the first resolved event forces one rebuild and later ones do not
ok 712 - the first resolved event forces one rebuild and later ones do not
  ---
  duration_ms: 1.842297
  ...
# Subtest: noteReadyEvaluate is pure and mirrors the Rust totals
ok 713 - noteReadyEvaluate is pure and mirrors the Rust totals
  ---
  duration_ms: 0.344498
  ...
# Subtest: conformance: merged name with duplicate
ok 714 - conformance: merged name with duplicate
  ---
  duration_ms: 3.769054
  ...
# Subtest: conformance: link forms and exclusions
ok 715 - conformance: link forms and exclusions
  ---
  duration_ms: 1.865732
  ...
# Subtest: conformance: unnamed placeholders
ok 716 - conformance: unnamed placeholders
  ---
  duration_ms: 0.423959
  ...
# Subtest: conformance: subheading in the section
ok 717 - conformance: subheading in the section
  ---
  duration_ms: 0.244326
  ...
# Subtest: conformance: open inventory label
ok 718 - conformance: open inventory label
  ---
  duration_ms: 0.319741
  ...
# Subtest: conformance: over the cap
ok 719 - conformance: over the cap
  ---
  duration_ms: 0.221402
  ...
# Subtest: conformance: cancelled and completed entries
ok 720 - conformance: cancelled and completed entries
  ---
  duration_ms: 0.258062
  ...
# Subtest: exactly at the cap is fine
ok 721 - exactly at the cap is fine
  ---
  duration_ms: 0.223798
  ...
# Subtest: no Pomodoros section degrades to an empty budget
ok 722 - no Pomodoros section degrades to an empty budget
  ---
  duration_ms: 0.496568
  ...
# Subtest: fenced code never counts
ok 723 - fenced code never counts
  ---
  duration_ms: 0.493802
  ...
# Subtest: highlight is the first open non-exempt entry; running is the timed one
ok 724 - highlight is the first open non-exempt entry; running is the timed one
  ---
  duration_ms: 0.431454
  ...
# Subtest: coercePlanCaps ignores a legacy max_now instead of failing
ok 725 - coercePlanCaps ignores a legacy max_now instead of failing
  ---
  duration_ms: 0.314431
  ...
# Subtest: parsePlanCaps defaults, overrides, and invalid fallbacks
ok 726 - parsePlanCaps defaults, overrides, and invalid fallbacks
  ---
  duration_ms: 0.416956
  ...
# Subtest: loadPlanCaps falls back to defaults without fs
ok 727 - loadPlanCaps falls back to defaults without fs
  ---
  duration_ms: 0.488623
  ...
# Subtest: loadPlanCaps falls back to defaults on mobile
ok 728 - loadPlanCaps falls back to defaults on mobile
  ---
  duration_ms: 0.266478
  ...
# Subtest: loadPlanCaps reads plan: and flags invalid values
ok 729 - loadPlanCaps reads plan: and flags invalid values
  ---
  duration_ms: 0.457373
  ...
# Subtest: planBlockTargetPath prefers the containing daily note
ok 730 - planBlockTargetPath prefers the containing daily note
  ---
  duration_ms: 0.80691
  ...
# Subtest: planBlockModel degrades to placeholders, never an error
ok 731 - planBlockModel degrades to placeholders, never an error
  ---
  duration_ms: 0.881824
  ...
# Subtest: planBlockModel renders chips, themes, and lints
ok 732 - planBlockModel renders chips, themes, and lints
  ---
  duration_ms: 1.085973
  ...
# Subtest: planBlockModel adds lane cap lints when a lane is over
ok 733 - planBlockModel adds lane cap lints when a lane is over
  ---
  duration_ms: 3.272607
  ...
# Subtest: plugin exposes the versioned api and registers the bob-plan block
ok 734 - plugin exposes the versioned api and registers the bob-plan block
  ---
  duration_ms: 4.673881
  ...
# Subtest: invalid plan block falls back to full defaults
ok 735 - invalid plan block falls back to full defaults
  ---
  duration_ms: 0.297328
  ...
# Subtest: entries require column-0 dash-space with one status char
ok 736 - entries require column-0 dash-space with one status char
  ---
  duration_ms: 0.195323
  ...
# Subtest: crlf line endings split like lf
ok 737 - crlf line endings split like lf
  ---
  duration_ms: 0.231141
  ...
# Subtest: conformance: empty target means the daily note
ok 738 - conformance: empty target means the daily note
  ---
  duration_ms: 0.201946
  ...
# Subtest: lane predicate matches hide subtags, case, and non-task
ok 739 - lane predicate matches hide subtags, case, and non-task
  ---
  duration_ms: 0.217655
  ...
# Subtest: planBlockModel daily badges follow dashboard section counts
ok 740 - planBlockModel daily badges follow dashboard section counts
  ---
  duration_ms: 1.903344
  ...
# Subtest: planBlockModel keeps a supplied unavailable dashboard budget
ok 741 - planBlockModel keeps a supplied unavailable dashboard budget
  ---
  duration_ms: 0.321304
  ...
# Subtest: work tones: TODAY override and unavailable stay neutral in planBlockModel
ok 742 - work tones: TODAY override and unavailable stay neutral in planBlockModel
  ---
  duration_ms: 0.281267
  ...
# Subtest: parser accepts the PM1-PM5 conformance vectors verbatim
ok 743 - parser accepts the PM1-PM5 conformance vectors verbatim
  ---
  duration_ms: 1.832298
  ...
# Subtest: parser rejects the PM7-PM12 conformance vectors verbatim
ok 744 - parser rejects the PM7-PM12 conformance vectors verbatim
  ---
  duration_ms: 0.284263
  ...
# Subtest: PM6 with the ladder unknown omits P-labels instead of guessing
ok 745 - PM6 with the ladder unknown omits P-labels instead of guessing
  ---
  duration_ms: 0.19419
  ...
# Subtest: PM13-PM17 ladder and line variants hold
ok 746 - PM13-PM17 ladder and line variants hold
  ---
  duration_ms: 0.323818
  ...
# Subtest: no model output contains a double colon
ok 747 - no model output contains a double colon
  ---
  duration_ms: 0.831306
  ...
# Subtest: element structure and the decorative/inheritColor options
ok 748 - element structure and the decorative/inheritColor options
  ---
  duration_ms: 0.354596
  ...
# Subtest: Live Preview decorations fold space, reveal, and refuse
ok 749 - Live Preview decorations fold space, reveal, and refuse
  ---
  duration_ms: 1.263672
  ...
# Subtest: a line with fresh and priority fields gets a disjoint decoration
ok 750 - a line with fresh and priority fields gets a disjoint decoration
  ---
  duration_ms: 0.203448
  ...
# Subtest: widget mousedown reveals the field at the folded offset
ok 751 - widget mousedown reveals the field at the folded offset
  ---
  duration_ms: 0.608562
  ...
# Subtest: rendered views split task nodes and skip exclusions
ok 752 - rendered views split task nodes and skip exclusions
  ---
  duration_ms: 1.505374
  ...
# Subtest: ladder coercion is lenient: valid, partial, and unknown
ok 753 - ladder coercion is lenient: valid, partial, and unknown
  ---
  duration_ms: 0.526145
  ...
# Subtest: ladder snapshot reads the file and reuses the cache
ok 754 - ladder snapshot reads the file and reuses the cache
  ---
  duration_ms: 2.660828
  ...
# Subtest: ladder snapshot degrades on missing files and parse errors
ok 755 - ladder snapshot degrades on missing files and parse errors
  ---
  duration_ms: 1.359335
  ...
# Subtest: ladder snapshot is unknown on mobile
ok 756 - ladder snapshot is unknown on mobile
  ---
  duration_ms: 9.876202
  ...
# Subtest: api.priorityMarks v1 is additive, sync, and never throwing
ok 757 - api.priorityMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 3.812087
  ...
# Subtest: session toggle and onload wiring
ok 758 - session toggle and onload wiring
  ---
  duration_ms: 0.79076
  ...
# Subtest: styles.css contract: masks, both hosts, repair flag, resting
ok 759 - styles.css contract: masks, both hosts, repair flag, resting
  ---
  duration_ms: 0.662735
  ...
# Subtest: P1/P3/P4: open entries mark plain and aliased links
ok 760 - P1/P3/P4: open entries mark plain and aliased links
  ---
  duration_ms: 3.067506
  ...
# Subtest: P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
ok 761 - P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
  ---
  duration_ms: 2.637856
  ...
# Subtest: P5: closed entries never mark, even with 🍅 history
ok 762 - P5: closed entries never mark, even with 🍅 history
  ---
  duration_ms: 0.572914
  ...
# Subtest: P6/P7: embedded and struck links never mark
ok 763 - P6/P7: embedded and struck links never mark
  ---
  duration_ms: 0.220661
  ...
# Subtest: P8: both trailing-\# move-only forms mark
ok 764 - P8: both trailing-\# move-only forms mark
  ---
  duration_ms: 0.242584
  ...
# Subtest: P9: nested and prose-mixed links never mark
ok 765 - P9: nested and prose-mixed links never mark
  ---
  duration_ms: 0.155707
  ...
# Subtest: P10: fenced, off-section, and off-note links never mark
ok 766 - P10: fenced, off-section, and off-note links never mark
  ---
  duration_ms: 0.380166
  ...
# Subtest: P11: unresolved targets and non-task blocks get no mark
ok 767 - P11: unresolved targets and non-task blocks get no mark
  ---
  duration_ms: 0.466841
  ...
# Subtest: P13: a same-note target reads the live doc
ok 768 - P13: a same-note target reads the live doc
  ---
  duration_ms: 0.792783
  ...
# Subtest: P14: expect() wins until the cache agrees or 4 s pass
ok 769 - P14: expect() wins until the cache agrees or 4 s pass
  ---
  duration_ms: 0.961525
  ...
# Subtest: tooltip, element structure, and eq
ok 770 - tooltip, element structure, and eq
  ---
  duration_ms: 0.299242
  ...
# Subtest: Live Preview places one widget at each In Progress link
ok 771 - Live Preview places one widget at each In Progress link
  ---
  duration_ms: 0.506406
  ...
# Subtest: widget mousedown places the cursor at the link start
ok 772 - widget mousedown places the cursor at the link start
  ---
  duration_ms: 0.355669
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
ok 773 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 0.434589
  ...
# Subtest: Reading view marks In Progress rows and dedupes
ok 774 - Reading view marks In Progress rows and dedupes
  ---
  duration_ms: 3.682228
  ...
# Subtest: Reading view refuses every non-mark row
ok 775 - Reading view refuses every non-mark row
  ---
  duration_ms: 1.17384
  ...
# Subtest: Reading view allows the 🍅 prefix and the trailing \# marker
ok 776 - Reading view allows the 🍅 prefix and the trailing \# marker
  ---
  duration_ms: 0.337875
  ...
# Subtest: api.progressMarks v1 is additive, sync, and never throwing
ok 777 - api.progressMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.657375
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 778 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 0.857778
  ...
# Subtest: changed-file and rollover refreshes
ok 779 - changed-file and rollover refreshes
  ---
  duration_ms: 0.442074
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 780 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.101554
  ...
# Subtest: styles.css contract: glyph, box, motion, toggle, calm
ok 781 - styles.css contract: glyph, box, motion, toggle, calm
  ---
  duration_ms: 0.596358
  ...
# Subtest: max_ready defaults to 100 for missing, absent, and null values
ok 782 - max_ready defaults to 100 for missing, absent, and null values
  ---
  duration_ms: 1.626826
  ...
# Subtest: max_ready accepts a custom positive cap
ok 783 - max_ready accepts a custom positive cap
  ---
  duration_ms: 0.19901
  ...
# Subtest: max_ready rejects zero, negative, fractions, strings, booleans, and overflow
ok 784 - max_ready rejects zero, negative, fractions, strings, booleans, and overflow
  ---
  duration_ms: 0.951286
  ...
# Subtest: old configurations and legacy max_now still load
ok 785 - old configurations and legacy max_now still load
  ---
  duration_ms: 0.263874
  ...
# Subtest: READY boundary: only a strict excess turns red
ok 786 - READY boundary: only a strict excess turns red
  ---
  duration_ms: 2.038571
  ...
# Subtest: READY custom-cap boundary
ok 787 - READY custom-cap boundary
  ---
  duration_ms: 0.259355
  ...
# Subtest: READY over is independent of the PLAN ledger status
ok 788 - READY over is independent of the PLAN ledger status
  ---
  duration_ms: 7.655404
  ...
# Subtest: READY predicate: statuses, custom TODO symbols, and non-tasks
ok 789 - READY predicate: statuses, custom TODO symbols, and non-tasks
  ---
  duration_ms: 0.229518
  ...
# Subtest: READY predicate: blocked uses the full list, even outside the queue
ok 790 - READY predicate: blocked uses the full list, even outside the queue
  ---
  duration_ms: 0.441262
  ...
# Subtest: READY predicate: past, today, and future schedules
ok 791 - READY predicate: past, today, and future schedules
  ---
  duration_ms: 0.492079
  ...
# Subtest: READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
ok 792 - READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
  ---
  duration_ms: 0.283642
  ...
# Subtest: READY predicate: Today exclusion
ok 793 - READY predicate: Today exclusion
  ---
  duration_ms: 0.153924
  ...
# Subtest: readyTaskVisible excludes hide variants like Tasks
ok 794 - readyTaskVisible excludes hide variants like Tasks
  ---
  duration_ms: 0.148693
  ...
# Subtest: daily and dashboard share the READY element contract
ok 795 - daily and dashboard share the READY element contract
  ---
  duration_ms: 10.872183
  ...
# Subtest: READY placeholder keeps the limit in its tooltip
ok 796 - READY placeholder keeps the limit in its tooltip
  ---
  duration_ms: 0.142833
  ...
# Subtest: READY keyboard and modifier-key navigation
ok 797 - READY keyboard and modifier-key navigation
  ---
  duration_ms: 0.734021
  ...
# Subtest: READY unavailable without Tasks, on Cold/Initializing, or before Today
ok 798 - READY unavailable without Tasks, on Cold/Initializing, or before Today
  ---
  duration_ms: 1.659257
  ...
# Subtest: READY counts a valid empty queue as zero, not unavailable
ok 799 - READY counts a valid empty queue as zero, not unavailable
  ---
  duration_ms: 0.849903
  ...
# Subtest: READY stays compatible with hosts exposing only getTasks()
ok 800 - READY stays compatible with hosts exposing only getTasks()
  ---
  duration_ms: 1.770621
  ...
# Subtest: READY degrades to unavailable when the Today predicate throws
ok 801 - READY degrades to unavailable when the Today predicate throws
  ---
  duration_ms: 0.568115
  ...
# Subtest: READY renders label/value spans for every budget state
ok 802 - READY renders label/value spans for every budget state
  ---
  duration_ms: 1.022161
  ...
# Subtest: READY live refresh keeps the anchor, spans, and handlers
ok 803 - READY live refresh keeps the anchor, spans, and handlers
  ---
  duration_ms: 1.185473
  ...
# Subtest: READY refresh crosses the over-cap boundary and back
ok 804 - READY refresh crosses the over-cap boundary and back
  ---
  duration_ms: 0.617999
  ...
# Subtest: READY refresh crosses the unavailable boundary and back
ok 805 - READY refresh crosses the unavailable boundary and back
  ---
  duration_ms: 0.557404
  ...
# Subtest: READY never assigns the Obsidian text setter
ok 806 - READY never assigns the Obsidian text setter
  ---
  duration_ms: 1.17875
  ...
# Subtest: READY gating excludes review buckets and keeps the partition
ok 807 - READY gating excludes review buckets and keeps the partition
  ---
  duration_ms: 0.402909
  ...
# Subtest: gated READY tooltip carries total lane pressure
ok 808 - gated READY tooltip carries total lane pressure
  ---
  duration_ms: 0.134026
  ...
# Subtest: planBlockModel gates READY and shares the lane tooltip
ok 809 - planBlockModel gates READY and shares the lane tooltip
  ---
  duration_ms: 0.603512
  ...
# Subtest: READY lint appears only on a strict excess
ok 810 - READY lint appears only on a strict excess
  ---
  duration_ms: 3.737675
  ...
# Subtest: READY lint uses a custom cap
ok 811 - READY lint uses a custom cap
  ---
  duration_ms: 0.74414
  ...
# Subtest: lane lints appear in NEXT, PENDING, READY order
ok 812 - lane lints appear in NEXT, PENDING, READY order
  ---
  duration_ms: 3.121278
  ...
# Subtest: READY lint uses the gated count
ok 813 - READY lint uses the gated count
  ---
  duration_ms: 1.496887
  ...
# Subtest: READY lint stays silent while unavailable
ok 814 - READY lint stays silent while unavailable
  ---
  duration_ms: 0.488783
  ...
# Subtest: READY speaks each host's chip language (daily single-tone, dash two-tone)
ok 815 - READY speaks each host's chip language (daily single-tone, dash two-tone)
  ---
  duration_ms: 2.489322
  ...
# Subtest: daily paint carries lane pressure to the shared READY renderer
ok 816 - daily paint carries lane pressure to the shared READY renderer
  ---
  duration_ms: 20.922978
  ...
# Subtest: daily paint degrades to the legacy tooltip without freshness
ok 817 - daily paint degrades to the legacy tooltip without freshness
  ---
  duration_ms: 2.050144
  ...
# Subtest: work tones: READY model carries the displayed-count tone
ok 818 - work tones: READY model carries the displayed-count tone
  ---
  duration_ms: 0.180054
  ...
# Subtest: parseTrigger parses D[-]<N> dated-entry triggers with offset and span
ok 819 - parseTrigger parses D[-]<N> dated-entry triggers with offset and span
  ---
  duration_ms: 2.982914
  ...
# Subtest: computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
ok 820 - computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
  ---
  duration_ms: 0.438988
  ...
# Subtest: expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
ok 821 - expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
  ---
  duration_ms: 0.489935
  ...
# Subtest: findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
ok 822 - findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
  ---
  duration_ms: 0.349527
  ...
# Subtest: compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
ok 823 - compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
  ---
  duration_ms: 0.370707
  ...
# Subtest: parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
ok 824 - parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
  ---
  duration_ms: 0.202747
  ...
# Subtest: computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
ok 825 - computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
  ---
  duration_ms: 0.191516
  ...
# Subtest: findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
ok 826 - findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
  ---
  duration_ms: 0.192287
  ...
# Subtest: findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
ok 827 - findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
  ---
  duration_ms: 0.317355
  ...
# Subtest: expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
ok 828 - expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
  ---
  duration_ms: 0.829744
  ...
# Subtest: regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
ok 829 - regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
  ---
  duration_ms: 0.425712
  ...
# Subtest: expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
ok 830 - expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
  ---
  duration_ms: 0.36193
  ...
# Subtest: stats fence body sets defaults only and ignores the rest
ok 831 - stats fence body sets defaults only and ignores the rest
  ---
  duration_ms: 3.060863
  ...
# Subtest: stats tile models cover every unit and every quality
ok 832 - stats tile models cover every unit and every quality
  ---
  duration_ms: 0.567102
  ...
# Subtest: stats spark bars mark null gaps, zero ticks, and hollow today
ok 833 - stats spark bars mark null gaps, zero ticks, and hollow today
  ---
  duration_ms: 0.381057
  ...
# Subtest: stats table rows and CSV share the same points
ok 834 - stats table rows and CSV share the same points
  ---
  duration_ms: 0.776121
  ...
# Subtest: stats overview ids prefer the fence, then config, then report order
ok 835 - stats overview ids prefer the fence, then config, then report order
  ---
  duration_ms: 1.122482
  ...
# Subtest: stats window label always states today and tracking start
ok 836 - stats window label always states today and tracking start
  ---
  duration_ms: 0.258052
  ...
# Subtest: stats view state is session-only and per source path
ok 837 - stats view state is session-only and per source path
  ---
  duration_ms: 3.755669
  ...
# Subtest: stats block renders header, tiles, table, and footer from JSON
ok 838 - stats block renders header, tiles, table, and footer from JSON
  ---
  duration_ms: 43.960265
  ...
# Subtest: stats block shows an actionable card with Retry when bob fails
ok 839 - stats block shows an actionable card with Retry when bob fails
  ---
  duration_ms: 43.898867
  ...
# Subtest: stats block registers the processor and the Open Stats command
ok 840 - stats block registers the processor and the Open Stats command
  ---
  duration_ms: 1.402447
  ...
# Subtest: stats stylesheet contract: selectors, tabular-nums, motion, colors
ok 841 - stats stylesheet contract: selectors, tabular-nums, motion, colors
  ---
  duration_ms: 1.223315
  ...
# Subtest: Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
ok 842 - Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
  ---
  duration_ms: 3.014955
  ...
# Subtest: prior buckets align by elapsed position and omit invalid and provisional points
ok 843 - prior buckets align by elapsed position and omit invalid and provisional points
  ---
  duration_ms: 1.012824
  ...
# Subtest: chart renders SVG safely and keeps secondary focus metrics selectable
ok 844 - chart renders SVG safely and keeps secondary focus metrics selectable
  ---
  duration_ms: 11.001279
  ...
# Subtest: grouped chart pins honest buckets, bounds daily detail, and opens validated notes
ok 845 - grouped chart pins honest buckets, bounds daily detail, and opens validated notes
  ---
  duration_ms: 5.262415
  ...
# Subtest: local focus, table, pin, and definition changes reuse the retained report
ok 846 - local focus, table, pin, and definition changes reuse the retained report
  ---
  duration_ms: 6.514174
  ...
# Subtest: keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
ok 847 - keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
  ---
  duration_ms: 37.654698
  ...
# Subtest: schema-1 fallback keeps day quartiles and never invents grouped daily history
ok 848 - schema-1 fallback keeps day quartiles and never invents grouped daily history
  ---
  duration_ms: 2.607266
  ...
# Subtest: ResizeObserver redraws cached data and disconnects across rerenders and unload
ok 849 - ResizeObserver redraws cached data and disconnects across rerenders and unload
  ---
  duration_ms: 132.208047
  ...
# Subtest: stats resolution prefers stats.bob_path, then candidates, then PATH
ok 850 - stats resolution prefers stats.bob_path, then candidates, then PATH
  ---
  duration_ms: 3.354022
  ...
# Subtest: stats home expansion and range/offset normalization
ok 851 - stats home expansion and range/offset normalization
  ---
  duration_ms: 0.477341
  ...
# Subtest: stats fetch always runs show -a -f json plus the chosen flags
ok 852 - stats fetch always runs show -a -f json plus the chosen flags
  ---
  duration_ms: 0.486107
  ...
# Subtest: stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
ok 853 - stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
  ---
  duration_ms: 5.726081
  ...
# Subtest: stats spawn maps ENOENT, timeouts, and stderr to named errors
ok 854 - stats spawn maps ENOENT, timeouts, and stderr to named errors
  ---
  duration_ms: 2.553113
  ...
# Subtest: stats decode accepts schema 1 and rejects the rest defensively
ok 855 - stats decode accepts schema 1 and rejects the rest defensively
  ---
  duration_ms: 0.29859
  ...
# Subtest: stats error cards name the cause and the stats.bob_path fix
ok 856 - stats error cards name the cause and the stats.bob_path fix
  ---
  duration_ms: 0.431143
  ...
# Subtest: stats fetch shares one flight and coalesces one follow-up
ok 857 - stats fetch shares one flight and coalesces one follow-up
  ---
  duration_ms: 22.784753
  ...
# Subtest: stats cache is a small LRU keyed by the argument list
ok 858 - stats cache is a small LRU keyed by the argument list
  ---
  duration_ms: 2.509551
  ...
# Subtest: stats stale entries return immediately and refresh in the background
ok 859 - stats stale entries return immediately and refresh in the background
  ---
  duration_ms: 1.62919
  ...
# Subtest: stats api v2 keeps append and adds fetch plus bobPath
ok 860 - stats api v2 keeps append and adds fetch plus bobPath
  ---
  duration_ms: 0.735834
  ...
# Subtest: statsHomeDir defaults to the real home and strips a trailing slash
ok 861 - statsHomeDir defaults to the real home and strips a trailing slash
  ---
  duration_ms: 0.22044
  ...
# Subtest: stats mac regression: un-injected resolution probes the real home first
ok 862 - stats mac regression: un-injected resolution probes the real home first
  ---
  duration_ms: 0.245188
  ...
# Subtest: stats absolute candidates are probed verbatim with no doubled slashes
ok 863 - stats absolute candidates are probed verbatim with no doubled slashes
  ---
  duration_ms: 0.260167
  ...
# Subtest: stats with no home probes only absolute candidates
ok 864 - stats with no home probes only absolute candidates
  ---
  duration_ms: 0.292027
  ...
# Subtest: stats tilde config expands against the real home
ok 865 - stats tilde config expands against the real home
  ---
  duration_ms: 0.177018
  ...
# Subtest: stats candidate and tried lists share one source of truth
ok 866 - stats candidate and tried lists share one source of truth
  ---
  duration_ms: 0.189341
  ...
# Subtest: stats spawn bob-not-found tried list uses the real home
ok 867 - stats spawn bob-not-found tried list uses the real home
  ---
  duration_ms: 1.338265
  ...
# Subtest: stats unload clears views, timers, cache, and flights
ok 868 - stats unload clears views, timers, cache, and flights
  ---
  duration_ms: 0.677543
  ...
# Subtest: stats namespace v1 serializes versioned review answer JSONL
ok 869 - stats namespace v1 serializes versioned review answer JSONL
  ---
  duration_ms: 6.967469
  ...
# Subtest: stats journal rejects invalid calendar days and outcomes
ok 870 - stats journal rejects invalid calendar days and outcomes
  ---
  duration_ms: 1.134406
  ...
# Subtest: statsReviewHost lowercases, cuts at the first dot, and never throws
ok 871 - statsReviewHost lowercases, cuts at the first dot, and never throws
  ---
  duration_ms: 0.159324
  ...
# Subtest: stats journal plugin passthrough keeps a semver writer and falls back otherwise
ok 872 - stats journal plugin passthrough keeps a semver writer and falls back otherwise
  ---
  duration_ms: 1.032691
  ...
# Subtest: panel dispatch covers every family, custom kinds, and the net exception
ok 873 - panel dispatch covers every family, custom kinds, and the net exception
  ---
  duration_ms: 2.438885
  ...
# Subtest: pomodoro panel shows the supplied total, shares, hue, and safe text
ok 874 - pomodoro panel shows the supplied total, shares, hue, and safe text
  ---
  duration_ms: 12.199778
  ...
# Subtest: task flow stacks signed values, keeps missing constituents missing, and labels series
ok 875 - task flow stacks signed values, keeps missing constituents missing, and labels series
  ---
  duration_ms: 6.921482
  ...
# Subtest: absent companions are named, custom filters are labeled overall, and net splits breakdowns
ok 876 - absent companions are named, custom filters are labeled overall, and net splits breakdowns
  ---
  duration_ms: 5.764343
  ...
# Subtest: journal panels pair answers with review time and a gapped keep chart under 90%
ok 877 - journal panels pair answers with review time and a gapped keep chart under 90%
  ---
  duration_ms: 17.721719
  ...
# Subtest: checklist calendar aligns Monday weeks with states, reasons, and provisional today
ok 878 - checklist calendar aligns Monday weeks with states, reasons, and provisional today
  ---
  duration_ms: 8.033616
  ...
# Subtest: grouped calendars reuse daily points and old schemas fall back with a label
ok 879 - grouped calendars reuse daily points and old schemas fall back with a label
  ---
  duration_ms: 4.863413
  ...
# Subtest: ISO year boundaries stay in one Monday week and chore dots expose text
ok 880 - ISO year boundaries stay in one Monday week and chore dots expose text
  ---
  duration_ms: 2.900658
  ...
# Subtest: panel day selection pins the shared day and never fetches
ok 881 - panel day selection pins the shared day and never fetches
  ---
  duration_ms: 7.934356
  ...
# Subtest: field and formula metrics keep only the focus chart and table
ok 882 - field and formula metrics keep only the focus chart and table
  ---
  duration_ms: 2.259523
  ...
# Subtest: TT vectors verbatim: task-line gate plus boundary tokens
ok 883 - TT vectors verbatim: task-line gate plus boundary tokens
  ---
  duration_ms: 4.940412
  ...
# Subtest: TT13-TT14 cursor reveal is inclusive
ok 884 - TT13-TT14 cursor reveal is inclusive
  ---
  duration_ms: 1.383671
  ...
# Subtest: TT16 coexistence: task tag range is disjoint from priority and date marks
ok 885 - TT16 coexistence: task tag range is disjoint from priority and date marks
  ---
  duration_ms: 1.391035
  ...
# Subtest: tooltip is exact and never contains a double colon
ok 886 - tooltip is exact and never contains a double colon
  ---
  duration_ms: 0.219289
  ...
# Subtest: element structure: empty widget span with tooltip attributes
ok 887 - element structure: empty widget span with tooltip attributes
  ---
  duration_ms: 0.307908
  ...
# Subtest: Live Preview decorations cover exactly the tag and respect reveal and code
ok 888 - Live Preview decorations cover exactly the tag and respect reveal and code
  ---
  duration_ms: 0.68126
  ...
# Subtest: widget mousedown reveals the tag start
ok 889 - widget mousedown reveals the tag start
  ---
  duration_ms: 0.508
  ...
# Subtest: TR vectors verbatim: rendered views annotate eligible anchors in place
ok 890 - TR vectors verbatim: rendered views annotate eligible anchors in place
  ---
  duration_ms: 1.612649
  ...
# Subtest: TR9 toggle strips document-wide and re-annotates on enable
ok 891 - TR9 toggle strips document-wide and re-annotates on enable
  ---
  duration_ms: 1.135017
  ...
# Subtest: annotate and strip helpers are idempotent and defensive
ok 892 - annotate and strip helpers are idempotent and defensive
  ---
  duration_ms: 0.478002
  ...
# Subtest: session toggle and onload wiring
ok 893 - session toggle and onload wiring
  ---
  duration_ms: 4.129572
  ...
# Subtest: styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
ok 894 - styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
  ---
  duration_ms: 1.022191
  ...
# Subtest: TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
ok 895 - TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
  ---
  duration_ms: 0.514072
  ...
# Subtest: Live Preview ref decorations replace the whole pair and reveal both tags at once
ok 896 - Live Preview ref decorations replace the whole pair and reveal both tags at once
  ---
  duration_ms: 0.503962
  ...
# Subtest: ref element structure: book classes, reference label, and tooltip
ok 897 - ref element structure: book classes, reference label, and tooltip
  ---
  duration_ms: 0.189161
  ...
# Subtest: TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
ok 898 - TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
  ---
  duration_ms: 3.857625
  ...
# Subtest: TR11 verbatim: \#task \#references and reversed order keep the hash only
ok 899 - TR11 verbatim: \#task \#references and reversed order keep the hash only
  ---
  duration_ms: 0.378653
  ...
# Subtest: TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
ok 900 - TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
  ---
  duration_ms: 0.214189
  ...
# Subtest: TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
ok 901 - TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
  ---
  duration_ms: 0.701389
  ...
# Subtest: styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
ok 902 - styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
  ---
  duration_ms: 0.79117
  ...
# Subtest: T1 GTD: empty target resolves to the daily note
ok 903 - T1 GTD: empty target resolves to the daily note
  ---
  duration_ms: 3.795205
  ...
# Subtest: T2 markers: pomodoro mark counts, struck drops, embed counts
ok 904 - T2 markers: pomodoro mark counts, struck drops, embed counts
  ---
  duration_ms: 0.599624
  ...
# Subtest: T3 closed entries: links under completed/cancelled entries drop
ok 905 - T3 closed entries: links under completed/cancelled entries drop
  ---
  duration_ms: 0.189702
  ...
# Subtest: T4 shapes: mixed text and deeper descendants drop
ok 906 - T4 shapes: mixed text and deeper descendants drop
  ---
  duration_ms: 0.306595
  ...
# Subtest: T5 dedupe: same task twice keeps the first position
ok 907 - T5 dedupe: same task twice keeps the first position
  ---
  duration_ms: 0.357342
  ...
# Subtest: T6 fenced: links inside fenced blocks drop
ok 908 - T6 fenced: links inside fenced blocks drop
  ---
  duration_ms: 0.242252
  ...
# Subtest: T7 status: the link layer lists every dedicated link
ok 909 - T7 status: the link layer lists every dedicated link
  ---
  duration_ms: 0.304661
  ...
# Subtest: T8 unresolved: missing notes give no key
ok 910 - T8 unresolved: missing notes give no key
  ---
  duration_ms: 0.175906
  ...
# Subtest: T9 alias: aliased links count under their target
ok 911 - T9 alias: aliased links count under their target
  ---
  duration_ms: 0.391388
  ...
# Subtest: laneBudgetFromTasks counts the whole Next lane, Today included
ok 912 - laneBudgetFromTasks counts the whole Next lane, Today included
  ---
  duration_ms: 1.212404
  ...
# Subtest: laneBudgetFromTasks counts Pending by type and flags over-cap
ok 913 - laneBudgetFromTasks counts Pending by type and flags over-cap
  ---
  duration_ms: 0.379494
  ...
# Subtest: lane caps come from max_next/max_pending; legacy max_now is ignored
ok 914 - lane caps come from max_next/max_pending; legacy max_now is ignored
  ---
  duration_ms: 0.182658
  ...
# Subtest: reload event name matches the Tasks bundle subscription
ok 915 - reload event name matches the Tasks bundle subscription
  ---
  duration_ms: 0.100662
  ...
# Subtest: api v2 shape: Today and lane budgets, no nowBudget
ok 916 - api v2 shape: Today and lane budgets, no nowBudget
  ---
  duration_ms: 3.808931
  ...
# Subtest: cache rebuild answers isToday/todayRank in ledger order
ok 917 - cache rebuild answers isToday/todayRank in ledger order
  ---
  duration_ms: 1.412868
  ...
# Subtest: refresh fires only when the key set changes
ok 918 - refresh fires only when the key set changes
  ---
  duration_ms: 0.820166
  ...
# Subtest: unready to ready with empty TODAY still refreshes open badges
ok 919 - unready to ready with empty TODAY still refreshes open badges
  ---
  duration_ms: 0.616556
  ...
# Subtest: cache rebuilds on the daily changed event with the event content
ok 920 - cache rebuilds on the daily changed event with the event content
  ---
  duration_ms: 2.869748
  ...
# Subtest: cache rebuilds once on resolved and at midnight rollover
ok 921 - cache rebuilds once on resolved and at midnight rollover
  ---
  duration_ms: 1.003265
  ...
# Subtest: a done-today prerequisite shows the glyph
ok 922 - a done-today prerequisite shows the glyph
  ---
  duration_ms: 3.411623
  ...
# Subtest: done yesterday does not show the glyph
ok 923 - done yesterday does not show the glyph
  ---
  duration_ms: 0.410253
  ...
# Subtest: a struck link does not show the glyph
ok 924 - a struck link does not show the glyph
  ---
  duration_ms: 0.261499
  ...
# Subtest: a closed entry does not show the glyph
ok 925 - a closed entry does not show the glyph
  ---
  duration_ms: 0.23089
  ...
# Subtest: several prerequisites give +N
ok 926 - several prerequisites give +N
  ---
  duration_ms: 1.108606
  ...
# Subtest: the model refuses every non-glyph shape
ok 927 - the model refuses every non-glyph shape
  ---
  duration_ms: 0.806109
  ...
# Subtest: unblockedGlyphDoneToday needs DONE plus a today done date
ok 928 - unblockedGlyphDoneToday needs DONE plus a today done date
  ---
  duration_ms: 0.253594
  ...
# Subtest: tooltip names one prerequisite and counts several
ok 929 - tooltip names one prerequisite and counts several
  ---
  duration_ms: 0.287178
  ...
# Subtest: Live Preview places one glyph after each unblocked link
not ok 930 - Live Preview places one glyph after each unblocked link
  ---
  duration_ms: 1.989207
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:546:1'
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
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:553:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Live Preview draws nothing without a warm cache or a live link
ok 931 - Live Preview draws nothing without a warm cache or a live link
  ---
  duration_ms: 0.767054
  ...
# Subtest: widget mousedown places the cursor past the link
not ok 932 - widget mousedown places the cursor past the link
  ---
  duration_ms: 0.452374
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:612:1'
  failureType: 'testCodeFailure'
  error: "Cannot read properties of undefined (reading 'value')"
  code: 'ERR_TEST_FAILURE'
  name: 'TypeError'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:615:69)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
not ok 933 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 0.3825
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:654:1'
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
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:662:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Reading view glyphs unblocked rows and dedupes
not ok 934 - Reading view glyphs unblocked rows and dedupes
  ---
  duration_ms: 1.218305
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:849:1'
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
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-unblocked-glyph.cjs:858:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Reading view refuses every non-glyph row
ok 935 - Reading view refuses every non-glyph row
  ---
  duration_ms: 3.028581
  ...
# Subtest: api.unblockedGlyph v1 is additive, sync, and never throwing
ok 936 - api.unblockedGlyph v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.835154
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 937 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 0.986183
  ...
# Subtest: changed-file and rollover refreshes
ok 938 - changed-file and rollover refreshes
  ---
  duration_ms: 0.249296
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 939 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.081084
  ...
# Subtest: styles.css contract: faint glyph, Done token, toggle
ok 940 - styles.css contract: faint glyph, Done token, toggle
  ---
  duration_ms: 0.513089
  ...
# Subtest: Ledger Vim mappings restore \\p and retain the other normal-mode actions
ok 941 - Ledger Vim mappings restore \\p and retain the other normal-mode actions
  ---
  duration_ms: 2.120287
  ...
# Subtest: workBadgeTone boundary vectors at cap 100 use exact comparisons
ok 942 - workBadgeTone boundary vectors at cap 100 use exact comparisons
  ---
  duration_ms: 1.053521
  ...
# Subtest: workBadgeTone at cap 15 has no percentage rounding
ok 943 - workBadgeTone at cap 15 has no percentage rounding
  ---
  duration_ms: 0.210342
  ...
# Subtest: workBadgeTone default caps, small caps, and cap changes
ok 944 - workBadgeTone default caps, small caps, and cap changes
  ---
  duration_ms: 0.182789
  ...
# Subtest: workBadgeTone never coerces invalid input to zero
ok 945 - workBadgeTone never coerces invalid input to zero
  ---
  duration_ms: 0.276618
  ...
# Subtest: TODAY links bands with themes at cap 3
ok 946 - TODAY links bands with themes at cap 3
  ---
  duration_ms: 0.404953
  ...
# Subtest: TODAY theme overflow forces red, exact cap does not
ok 947 - TODAY theme overflow forces red, exact cap does not
  ---
  duration_ms: 0.263332
  ...
# Subtest: TODAY unavailable stays neutral, empty section is grey
ok 948 - TODAY unavailable stays neutral, empty section is grey
  ---
  duration_ms: 1.565138
  ...
# Subtest: PENDING/NEXT models color the section, READY its gated count
ok 949 - PENDING/NEXT models color the section, READY its gated count
  ---
  duration_ms: 0.614753
  ...
# Subtest: READY uses its gated count even when the total lane is larger
ok 950 - READY uses its gated count even when the total lane is larger
  ---
  duration_ms: 0.469596
  ...
# Subtest: cap equality still emits no cap lint
ok 951 - cap equality still emits no cap lint
  ---
  duration_ms: 3.228323
  ...
# Subtest: lane DOM keeps exactly one tone through transitions and unavailability
ok 952 - lane DOM keeps exactly one tone through transitions and unavailability
  ---
  duration_ms: 6.657778
  ...
# Subtest: READY DOM keeps exactly one tone and daily/dashboard models agree
ok 953 - READY DOM keeps exactly one tone and daily/dashboard models agree
  ---
  duration_ms: 1.02687
  ...
# SKIP dashboard integration: BOB_DASHBOARD_FILE is not set
# SKIP dashboard fallback integration: BOB_DASHBOARD_FILE is not set
# Subtest: daily TODAY chip uses the theme-overflow tone
ok 954 - daily TODAY chip uses the theme-overflow tone
  ---
  duration_ms: 15.239081
  ...
# Subtest: dashboard integration uses Work tones, TODAY override, and keeps Work order
ok 955 - dashboard integration uses Work tones, TODAY override, and keeps Work order
  ---
  duration_ms: 0.524311
  ...
# Subtest: dashboard fallbacks keep Work tones without plugin renderers or colors
ok 956 - dashboard fallbacks keep Work tones without plugin renderers or colors
  ---
  duration_ms: 0.337153
  ...
# Subtest: nav BK1–BK2 accept canonical BLOCKS lines
ok 957 - nav BK1–BK2 accept canonical BLOCKS lines
  ---
  duration_ms: 2.804603
  ...
# Subtest: nav BK3–BK11 canonicalise
ok 958 - nav BK3–BK11 canonicalise
  ---
  duration_ms: 0.731947
  ...
# Subtest: nav BK12 empty, BK13–BK15 malformed
ok 959 - nav BK12 empty, BK13–BK15 malformed
  ---
  duration_ms: 0.239747
  ...
# Subtest: nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse
ok 960 - nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse
  ---
  duration_ms: 0.417227
  ...
# Subtest: nav BK21 code-point sort and writer format
ok 961 - nav BK21 code-point sort and writer format
  ---
  duration_ms: 0.339278
  ...
# Subtest: nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS
ok 962 - nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS
  ---
  duration_ms: 0.525634
  ...
# Subtest: nav BW18 conversion drops BLOCKS like Sub-projects
ok 963 - nav BW18 conversion drops BLOCKS like Sub-projects
  ---
  duration_ms: 0.734051
  ...
# Subtest: nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner
ok 964 - nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner
  ---
  duration_ms: 0.903786
  ...
# Subtest: nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists
ok 965 - nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists
  ---
  duration_ms: 1.866394
  ...
# Subtest: nav MC1/MC2 deferred Pomodoro cleanup skips managed lines
ok 966 - nav MC1/MC2 deferred Pomodoro cleanup skips managed lines
  ---
  duration_ms: 0.48192
  ...
# Subtest: SB1-SB9 dependent IDs match the successor mint vectors
ok 967 - SB1-SB9 dependent IDs match the successor mint vectors
  ---
  duration_ms: 1.960894
  ...
# Subtest: BW1 same-note add mints and writes BLOCKS in the dependent's single transaction
ok 968 - BW1 same-note add mints and writes BLOCKS in the dependent's single transaction
  ---
  duration_ms: 10.403458
  ...
# Subtest: BW2 cross-note add follows the dependent commit and writes the target note
ok 969 - BW2 cross-note add follows the dependent commit and writes the target note
  ---
  duration_ms: 2.261187
  ...
# Subtest: BW4 cross-note target preparation precedes the reverse-line preimage
ok 970 - BW4 cross-note target preparation precedes the reverse-line preimage
  ---
  duration_ms: 1.917801
  ...
# Subtest: BW3 stale cross-note preimage leaves the forward write standing and shows the suffix
ok 971 - BW3 stale cross-note preimage leaves the forward write standing and shows the suffix
  ---
  duration_ms: 1.398319
  ...
# Subtest: BW5 removal deletes the reverse line when its last dependent leaves
ok 972 - BW5 removal deletes the reverse line when its last dependent leaves
  ---
  duration_ms: 3.575395
  ...
# Subtest: BW6 an already mirrored edge is a byte-identical no-op
ok 973 - BW6 an already mirrored edge is a byte-identical no-op
  ---
  duration_ms: 0.649229
  ...
# Subtest: BW7 closed owners stay frozen
ok 974 - BW7 closed owners stay frozen
  ---
  duration_ms: 1.48787
  ...
# Subtest: BW8 malformed reverse lines stay untouched and report the failed mirror
ok 975 - BW8 malformed reverse lines stay untouched and report the failed mirror
  ---
  duration_ms: 1.343995
  ...
# Subtest: BW15 config defaults on, honors false, and invalid values fall back on
ok 976 - BW15 config defaults on, honors false, and invalid values fall back on
  ---
  duration_ms: 0.596389
  ...
# Subtest: BW17 planner output follows BK21 Unicode code-point ordering
ok 977 - BW17 planner output follows BK21 Unicode code-point ordering
  ---
  duration_ms: 0.431483
  ...
# Subtest: duplicate BLOCKS children merge their known dependents and preserve CRLF
ok 978 - duplicate BLOCKS children merge their known dependents and preserve CRLF
  ---
  duration_ms: 0.422887
  ...
# Subtest: BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270)
ok 979 - BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270)
  ---
  duration_ms: 3.092312
  ...
# Subtest: counted remove-from-all drops every dependent from the same-note BLOCKS line (420)
ok 980 - counted remove-from-all drops every dependent from the same-note BLOCKS line (420)
  ---
  duration_ms: 1.065533
  ...
# Subtest: vault counted add composes cross-note follow-ups for every source (420)
ok 981 - vault counted add composes cross-note follow-ups for every source (420)
  ---
  duration_ms: 0.645733
  ...
# Subtest: marked batch add writes every same-note target onto BLOCKS in one plan (430)
ok 982 - marked batch add writes every same-note target onto BLOCKS in one plan (430)
  ---
  duration_ms: 0.446041
  ...
# Subtest: counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600)
ok 983 - counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600)
  ---
  duration_ms: 4.195469
  ...
# Subtest: BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves
ok 984 - BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves
  ---
  duration_ms: 1.233414
  ...
# Subtest: BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS
ok 985 - BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS
  ---
  duration_ms: 1.948118
  ...
# Subtest: hand-edit clear path routes through the BLOCKS seam (600)
ok 986 - hand-edit clear path routes through the BLOCKS seam (600)
  ---
  duration_ms: 0.514753
  ...
# Subtest: BW18 conversion never copies a BLOCKS line as a user child
ok 987 - BW18 conversion never copies a BLOCKS line as a user child
  ---
  duration_ms: 0.533709
  ...
# Subtest: BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it
ok 988 - BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it
  ---
  duration_ms: 2.961323
  ...
# Subtest: review checklist group helpers format exact completion and close notices
ok 989 - review checklist group helpers format exact completion and close notices
  ---
  duration_ms: 2.301694
  ...
# Subtest: claim declines without a current exact PRE/POST walk landing
ok 990 - claim declines without a current exact PRE/POST walk landing
  ---
  duration_ms: 7.626086
  ...
# Subtest: a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
ok 991 - a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
  ---
  duration_ms: 3.166806
  ...
# Subtest: checklist Ctrl+Enter holds its landing through the actual successor picker
ok 992 - checklist Ctrl+Enter holds its landing through the actual successor picker
  ---
  duration_ms: 9.01045
  ...
# Subtest: seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
ok 993 - seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
  ---
  duration_ms: 14.582997
  ...
# Subtest: a landed [?] checklist chore is claimed and completed
ok 994 - a landed [?] checklist chore is claimed and completed
  ---
  duration_ms: 0.671
  ...
# Subtest: ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
ok 995 - ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
  ---
  duration_ms: 1.982074
  ...
# Subtest: live successor filtering skips a stale completed row
ok 996 - live successor filtering skips a stale completed row
  ---
  duration_ms: 0.585608
  ...
# Subtest: live group filtering reads each cross-note path once
ok 997 - live group filtering reads each cross-note path once
  ---
  duration_ms: 0.590868
  ...
# Subtest: Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
ok 998 - Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
  ---
  duration_ms: 2.809944
  ...
# Subtest: POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
ok 999 - POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
  ---
  duration_ms: 1.064131
  ...
# Subtest: ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
ok 1000 - ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
  ---
  duration_ms: 0.617108
  ...
# Subtest: completion failure preserves cursor and landing and reports the Tasks failure
ok 1001 - completion failure preserves cursor and landing and reports the Tasks failure
  ---
  duration_ms: 0.289853
  ...
# Subtest: reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
ok 1002 - reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
  ---
  duration_ms: 1.361468
  ...
# Subtest: Alt+F on PRE stays with remaining PRE count and never stamps
ok 1003 - Alt+F on PRE stays with remaining PRE count and never stamps
  ---
  duration_ms: 5.544073
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a stale cache
ok 1004 - Ctrl+Alt+F completes seven PRE rows from a stale cache
  ---
  duration_ms: 11.438995
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a refreshed cache
ok 1005 - Ctrl+Alt+F completes seven PRE rows from a refreshed cache
  ---
  duration_ms: 4.170801
  ...
# Subtest: POST stays put with the closing notice
ok 1006 - POST stays put with the closing notice
  ---
  duration_ms: 0.85397
  ...
# Subtest: manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
ok 1007 - manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
  ---
  duration_ms: 1.002333
  ...
# Subtest: manual Ctrl+Enter then ]s from a stale cache uses text-first identity
ok 1008 - manual Ctrl+Enter then ]s from a stale cache uses text-first identity
  ---
  duration_ms: 0.667605
  ...
# Subtest: counted Alt+F skips checklist rows with the skip tail
ok 1009 - counted Alt+F skips checklist rows with the skip tail
  ---
  duration_ms: 2.552713
  ...
# Subtest: missing cycler gate on a PRE row writes nothing
ok 1010 - missing cycler gate on a PRE row writes nothing
  ---
  duration_ms: 0.667705
  ...
# Subtest: missing ledger checklist gate on a tagged line writes nothing
ok 1011 - missing ledger checklist gate on a tagged line writes nothing
  ---
  duration_ms: 0.687392
  ...
# Subtest: a tagged line that is not a queue match falls through to recurring refusal
ok 1012 - a tagged line that is not a queue match falls through to recurring refusal
  ---
  duration_ms: 0.357973
  ...
# Subtest: formatFreshStampChecklistSkipTail names the skipped count
ok 1013 - formatFreshStampChecklistSkipTail names the skipped count
  ---
  duration_ms: 0.117034
  ...
# Subtest: partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
ok 1014 - partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
  ---
  duration_ms: 0.243725
  ...
# Subtest: Task Link Alt+F skips a PRE target with the skip notice
ok 1015 - Task Link Alt+F skips a PRE target with the skip notice
  ---
  duration_ms: 2.036097
  ...
# Subtest: P0 at interval 7 enters P2 with a previewed decay date and kept tail
ok 1016 - P0 at interval 7 enters P2 with a previewed decay date and kept tail
  ---
  duration_ms: 3.592778
  ...
# Subtest: P0 at interval 30 enters P3
ok 1017 - P0 at interval 30 enters P3
  ---
  duration_ms: 0.548948
  ...
# Subtest: fixed enter overrides the interval scan
ok 1018 - fixed enter overrides the interval scan
  ---
  duration_ms: 0.493401
  ...
# Subtest: unknown enter disables Not now without disabling Keep/Reword
ok 1019 - unknown enter disables Not now without disabling Keep/Reword
  ---
  duration_ms: 0.411385
  ...
# Subtest: P0 with no suitable level stays unavailable and never shortens the lease
ok 1020 - P0 with no suitable level stays unavailable and never shortens the lease
  ---
  duration_ms: 0.411315
  ...
# Subtest: custom level order resolves entry in ladder order
ok 1021 - custom level order resolves entry in ladder order
  ---
  duration_ms: 0.317937
  ...
# Subtest: unknown priority value disables Not now only
ok 1022 - unknown priority value disables Not now only
  ---
  duration_ms: 0.351761
  ...
# Subtest: prioritized P2 below its roll limit stays on the same level
ok 1023 - prioritized P2 below its roll limit stays on the same level
  ---
  duration_ms: 0.645843
  ...
# Subtest: P2 at its roll limit decays to P3
ok 1024 - P2 at its roll limit decays to P3
  ---
  duration_ms: 0.760351
  ...
# Subtest: P2 streak derives from the task Schedule Log
ok 1025 - P2 streak derives from the task Schedule Log
  ---
  duration_ms: 3.868976
  ...
# Subtest: configured decay:false keeps rolling past the limit
ok 1026 - configured decay:false keeps rolling past the limit
  ---
  duration_ms: 0.502038
  ...
# Subtest: per-level rolls:0 decays immediately
ok 1027 - per-level rolls:0 decays immediately
  ---
  duration_ms: 0.341683
  ...
# Subtest: terminal cancel substitutes a truthful same-level card roll
ok 1028 - terminal cancel substitutes a truthful same-level card roll
  ---
  duration_ms: 0.349427
  ...
# Subtest: no future date in the window refuses Not now
ok 1029 - no future date in the window refuses Not now
  ---
  duration_ms: 0.238725
  ...
# Subtest: Less often steps 7/14/30 to the next preset with a decision reason
ok 1030 - Less often steps 7/14/30 to the next preset with a decision reason
  ---
  duration_ms: 0.561041
  ...
# Subtest: Less often at 90+ opens the constrained custom picker; 365 is unavailable
ok 1031 - Less often at 90+ opens the constrained custom picker; 365 is unavailable
  ---
  duration_ms: 0.304441
  ...
# Subtest: previewed dates are stable for one random draw
ok 1032 - previewed dates are stable for one random draw
  ---
  duration_ms: 0.299372
  ...
# Subtest: Keep saturates at 999 and Drop preserves keeps history
ok 1033 - Keep saturates at 999 and Drop preserves keeps history
  ---
  duration_ms: 0.316204
  ...
# Subtest: kept tails preserve roll classification; decisions break it deliberately
ok 1034 - kept tails preserve roll classification; decisions break it deliberately
  ---
  duration_ms: 0.91167
  ...
# Subtest: invalid priority config offers no priority-changing action
ok 1035 - invalid priority config offers no priority-changing action
  ---
  duration_ms: 0.23582
  ...
# Subtest: decay off disables Not now but keeps counting
ok 1036 - decay off disables Not now but keeps counting
  ---
  duration_ms: 0.254686
  ...
# Subtest: explicit level picks cover the ladder with previewed rolls
ok 1037 - explicit level picks cover the ladder with previewed rolls
  ---
  duration_ms: 0.87496
  ...
# Subtest: card model is deeply frozen
ok 1038 - card model is deeply frozen
  ---
  duration_ms: 0.206714
  ...
# Subtest: single Alt+F on an at-limit task opens the card and writes nothing
ok 1039 - single Alt+F on an at-limit task opens the card and writes nothing
  ---
  duration_ms: 7.791172
  ...
# Subtest: dismissing the card writes nothing and does not advance
ok 1040 - dismissing the card writes nothing and does not advance
  ---
  duration_ms: 1.005239
  ...
# Subtest: early dates open the card and write nothing
ok 1041 - early dates open the card and write nothing
  ---
  duration_ms: 0.837238
  ...
# Subtest: namespace v5 with decide true stamps counted and opens no card
ok 1042 - namespace v5 with decide true stamps counted and opens no card
  ---
  duration_ms: 3.926606
  ...
# Subtest: stale task-line change writes nothing
ok 1043 - stale task-line change writes nothing
  ---
  duration_ms: 1.284091
  ...
# Subtest: stale local-day change writes nothing
ok 1044 - stale local-day change writes nothing
  ---
  duration_ms: 1.325931
  ...
# Subtest: stale decay-config change writes nothing
ok 1045 - stale decay-config change writes nothing
  ---
  duration_ms: 1.214488
  ...
# Subtest: stale priority-ladder config writes nothing
ok 1046 - stale priority-ladder config writes nothing
  ---
  duration_ms: 2.942847
  ...
# Subtest: stale child Schedule Log writes nothing
ok 1047 - stale child Schedule Log writes nothing
  ---
  duration_ms: 2.019375
  ...
# Subtest: Not now stamps, clears keeps, and advances exactly once
ok 1048 - Not now stamps, clears keeps, and advances exactly once
  ---
  duration_ms: 5.702976
  ...
# Subtest: Keep counts once and saturates at 999 without reset
not ok 1049 - Keep counts once and saturates at 999 without reset
  ---
  duration_ms: 1.758947
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/test-navigation-decision-card-handlers.cjs:546:1'
  failureType: 'testCodeFailure'
  error: '- [ ] #task Buy milk [fresh:: 2026-09-30] [keeps:: 3]'
  code: 'ERR_ASSERTION'
  name: 'AssertionError'
  expected:
  actual: 'Update Bob Ledger Tools to record review stats'
  operator: 'match'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/test-navigation-decision-card-handlers.cjs:569:12)
    async Test.run (node:internal/test_runner/test:980:9)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: Reword stamps, clears, logs, and never advances
ok 1050 - Reword stamps, clears, logs, and never advances
  ---
  duration_ms: 1.030067
  ...
# Subtest: Drop cancels with the dropped-after-keeps reason and keeps history
ok 1051 - Drop cancels with the dropped-after-keeps reason and keeps history
  ---
  duration_ms: 0.671863
  ...
# Subtest: Less often at 90+ opens the picker and dismiss writes nothing
ok 1052 - Less often at 90+ opens the picker and dismiss writes nothing
  ---
  duration_ms: 0.543297
  ...
# Subtest: counted session skips at-limit and counts below-limit
ok 1053 - counted session skips at-limit and counts below-limit
  ---
  duration_ms: 0.667895
  ...
# Subtest: counted session skips at-limit on an early date
ok 1054 - counted session skips at-limit on an early date
  ---
  duration_ms: 0.614052
  ...
# Subtest: counted session with every target skipped writes nothing
ok 1055 - counted session with every target skipped writes nothing
  ---
  duration_ms: 0.285294
  ...
# Subtest: availability: decay on (or absent) may ask; decay off never asks
ok 1056 - availability: decay on (or absent) may ask; decay off never asks
  ---
  duration_ms: 1.024295
  ...
# Subtest: trigger: only an explicit decide row decides
ok 1057 - trigger: only an explicit decide row decides
  ---
  duration_ms: 0.218878
  ...
# Subtest: partition: exact at-limit rows skip, everything else stamps
ok 1058 - partition: exact at-limit rows skip, everything else stamps
  ---
  duration_ms: 0.738199
  ...
# Subtest: partition: empty and malformed input stamps nothing and skips nothing
ok 1059 - partition: empty and malformed input stamps nothing and skips nothing
  ---
  duration_ms: 0.143193
  ...
# Subtest: partition: enabled false stamps decision rows (older namespace fallback)
ok 1060 - partition: enabled false stamps decision rows (older namespace fallback)
  ---
  duration_ms: 0.177169
  ...
# Subtest: skip wording: singular, plural, and all-skipped notices
ok 1061 - skip wording: singular, plural, and all-skipped notices
  ---
  duration_ms: 0.211163
  ...
# Subtest: reword cursor: lands at the end of the task body before metadata
ok 1062 - reword cursor: lands at the end of the task body before metadata
  ---
  duration_ms: 0.384383
  ...
# Subtest: captured age: optional context ages, null when created is missing
ok 1063 - captured age: optional context ages, null when created is missing
  ---
  duration_ms: 0.36129
  ...
# Subtest: rows: P0 entry shows the recommended Not now with a clean window
ok 1064 - rows: P0 entry shows the recommended Not now with a clean window
  ---
  duration_ms: 2.96527
  ...
# Subtest: rows: invalid priority config disables Not now and levels, keeps safe rows
ok 1065 - rows: invalid priority config disables Not now and levels, keeps safe rows
  ---
  duration_ms: 0.664949
  ...
# Subtest: rows: picker-mode Less often and 365-day cap
ok 1066 - rows: picker-mode Less often and 365-day cap
  ---
  duration_ms: 0.897624
  ...
# Subtest: rows: terminal ladder keeps Enter available and never cancels
ok 1067 - rows: terminal ladder keeps Enter available and never cancels
  ---
  duration_ms: 0.561001
  ...
# Subtest: modal: Enter approves once; later keys cannot approve again
ok 1068 - modal: Enter approves once; later keys cannot approve again
  ---
  duration_ms: 0.506948
  ...
# Subtest: modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
ok 1069 - modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
  ---
  duration_ms: 0.33018
  ...
# Subtest: modal: key repeat and modified keys never approve
ok 1070 - modal: key repeat and modified keys never approve
  ---
  duration_ms: 0.223377
  ...
# Subtest: modal: Esc changes nothing — dismiss without a choice
ok 1071 - modal: Esc changes nothing — dismiss without a choice
  ---
  duration_ms: 0.127624
  ...
# Subtest: modal: unavailable actions cannot be chosen
ok 1072 - modal: unavailable actions cannot be chosen
  ---
  duration_ms: 0.18333
  ...
# Subtest: modal: a double callback applies once
ok 1073 - modal: a double callback applies once
  ---
  duration_ms: 0.112023
  ...
# Subtest: capability: the nav api exposes the card while loaded
ok 1074 - capability: the nav api exposes the card while loaded
  ---
  duration_ms: 0.338726
  ...
# Subtest: capability: unload drops the card so marks stop promising it
ok 1075 - capability: unload drops the card so marks stop promising it
  ---
  duration_ms: 0.385626
  ...
# Subtest: ladder lookup: the first priority property wins, null without one
ok 1076 - ladder lookup: the first priority property wins, null without one
  ---
  duration_ms: 0.23049
  ...
# Subtest: stage entry resolves the line itself and refuses prose
ok 1077 - stage entry resolves the line itself and refuses prose
  ---
  duration_ms: 2.733858
  ...
# Subtest: stage canonical order ranks \#hide last ahead of the lane
ok 1078 - stage canonical order ranks \#hide last ahead of the lane
  ---
  duration_ms: 0.212876
  ...
# Subtest: stage empty query shows same-note plus In Progress and Next only
ok 1079 - stage empty query shows same-note plus In Progress and Next only
  ---
  duration_ms: 3.560077
  ...
# Subtest: stage cap appends a type-to-search-more hint row
ok 1080 - stage cap appends a type-to-search-more hint row
  ---
  duration_ms: 2.635941
  ...
# Subtest: stage BLOCKED rows carry waits-on counts and short guard reasons
ok 1081 - stage BLOCKED rows carry waits-on counts and short guard reasons
  ---
  duration_ms: 1.285784
  ...
# Subtest: stage removal notices name the task description, not the block id
ok 1082 - stage removal notices name the task description, not the block id
  ---
  duration_ms: 0.543257
  ...
# Subtest: stage Task Link batches keep Depends on without refusal
ok 1083 - stage Task Link batches keep Depends on without refusal
  ---
  duration_ms: 0.505324
  ...
# Subtest: stage batch cycle check runs on the post-batch graph
ok 1084 - stage batch cycle check runs on the post-batch graph
  ---
  duration_ms: 0.878316
  ...
# Subtest: stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
ok 1085 - stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
  ---
  duration_ms: 9.299682
  ...
# Subtest: stage stale single add refuses and reopens
ok 1086 - stage stale single add refuses and reopens
  ---
  duration_ms: 5.381973
  ...
# Subtest: Task Link Depends on focuses a linked note open in a background tab
ok 1087 - Task Link Depends on focuses a linked note open in a background tab
  ---
  duration_ms: 0.506126
  ...
# Subtest: Task Link Depends on refuses clearly when the linked note cannot be focused
    # Subtest: focus reports success but the active view stays elsewhere
    ok 1 - focus reports success but the active view stays elsewhere
      ---
      duration_ms: 1.374094
      ...
    # Subtest: focus reports failure
    ok 2 - focus reports failure
      ---
      duration_ms: 0.158943
      ...
    1..2
ok 1088 - Task Link Depends on refuses clearly when the linked note cannot be focused
  ---
  duration_ms: 2.48269
  ...
# Subtest: stage mirror burst keeps the baseline owner across an insertion above
ok 1089 - stage mirror burst keeps the baseline owner across an insertion above
  ---
  duration_ms: 1003.589644
  ...
# Subtest: stage mirror burst clears on a text-only line deletion
ok 1090 - stage mirror burst clears on a text-only line deletion
  ---
  duration_ms: 1000.545603
  ...
# Subtest: stage mirror vim dd clears the deleted line's owner
ok 1091 - stage mirror vim dd clears the deleted line's owner
  ---
  duration_ms: 1000.880051
  ...
# Subtest: stage badge counts open prerequisites without a block id
ok 1092 - stage badge counts open prerequisites without a block id
  ---
  duration_ms: 8.535072
  ...
# Subtest: stage badge names the future scheduled date with no open prerequisite
ok 1093 - stage badge names the future scheduled date with no open prerequisite
  ---
  duration_ms: 2.2317
  ...
# Subtest: stage badge reads blocked with nothing waiting and no schedule
ok 1094 - stage badge reads blocked with nothing waiting and no schedule
  ---
  duration_ms: 1.440129
  ...
# Subtest: stage vault batch with a stale row refuses and reopens
ok 1095 - stage vault batch with a stale row refuses and reopens
  ---
  duration_ms: 10.038984
  ...
# Subtest: stage opening builds 200/400/1000-task notes without cubic growth
ok 1096 - stage opening builds 200/400/1000-task notes without cubic growth
  ---
  duration_ms: 45.174361
  ...
# Subtest: stage snapshots match standalone parsing across grammar vectors
ok 1097 - stage snapshots match standalone parsing across grammar vectors
  ---
  duration_ms: 5.427562
  ...
# Subtest: stage Warm-empty cache is ready without a vault fallback
ok 1098 - stage Warm-empty cache is ready without a vault fallback
  ---
  duration_ms: 0.479735
  ...
# Subtest: stage opening renders cross-note results with zero writes and cap
ok 1099 - stage opening renders cross-note results with zero writes and cap
  ---
  duration_ms: 43.038614
  ...
# Subtest: stage CURRENT covers same-note, cross-note, blocked, and counted parents
ok 1100 - stage CURRENT covers same-note, cross-note, blocked, and counted parents
  ---
  duration_ms: 1.999036
  ...
# Subtest: stage collections reuse one snapshot per parent
ok 1101 - stage collections reuse one snapshot per parent
  ---
  duration_ms: 0.494303
  ...
# Subtest: stage cold refresh yields, preserves state, and performs no search reads
ok 1102 - stage cold refresh yields, preserves state, and performs no search reads
  ---
  duration_ms: 115.709132
  ...
# Subtest: stage cold refresh abandons after dismissal or replacement
ok 1103 - stage cold refresh abandons after dismissal or replacement
  ---
  duration_ms: 52.836868
  ...
# Subtest: stage 400-task opening finishes in a child process before the parent timeout
ok 1104 - stage 400-task opening finishes in a child process before the parent timeout
  ---
  duration_ms: 142.323646
  ...
# Subtest: stage ranker passes the DK contract vectors verbatim
ok 1105 - stage ranker passes the DK contract vectors verbatim
  ---
  duration_ms: 2.721906
  ...
# Subtest: stage ranker tiers match the capture ranker tier order
ok 1106 - stage ranker tiers match the capture ranker tier order
  ---
  duration_ms: 0.348886
  ...
# Subtest: stage pool excludes daily notes, done, templates, and dot-dirs
ok 1107 - stage pool excludes daily notes, done, templates, and dot-dirs
  ---
  duration_ms: 0.427456
  ...
# Subtest: stage pool collects open vault tasks with buffers as given
ok 1108 - stage pool collects open vault tasks with buffers as given
  ---
  duration_ms: 2.840792
  ...
# Subtest: stage CURRENT resolves same-note, missing, closed, and non-task targets
ok 1109 - stage CURRENT resolves same-note, missing, closed, and non-task targets
  ---
  duration_ms: 2.394851
  ...
# Subtest: stage cycle guard reports the path back to the dependent
ok 1110 - stage cycle guard reports the path back to the dependent
  ---
  duration_ms: 1.000841
  ...
# Subtest: stage view groups CURRENT, RESULTS, and BLOCKED with guards
ok 1111 - stage view groups CURRENT, RESULTS, and BLOCKED with guards
  ---
  duration_ms: 2.412335
  ...
# Subtest: stage view disables cycles and unencodable targets, keeps +id rows
ok 1112 - stage view disables cycles and unencodable targets, keeps +id rows
  ---
  duration_ms: 0.970172
  ...
# Subtest: stage cache tasks normalize across Tasks shapes, buffers win
ok 1113 - stage cache tasks normalize across Tasks shapes, buffers win
  ---
  duration_ms: 0.784948
  ...
# Subtest: stage Task Link mode shows Depends on for one link and batches
ok 1114 - stage Task Link mode shows Depends on for one link and batches
  ---
  duration_ms: 0.872345
  ...
# Subtest: stage mark keys never collide across notes
ok 1115 - stage mark keys never collide across notes
  ---
  duration_ms: 0.197477
  ...
# Subtest: stage display-text locating matches one open task
ok 1116 - stage display-text locating matches one open task
  ---
  duration_ms: 0.269424
  ...
# Subtest: stage selection refusal spans tasks only
ok 1117 - stage selection refusal spans tasks only
  ---
  duration_ms: 0.23597
  ...
# Subtest: stage builder composes pool, current, guards, and pill title
ok 1118 - stage builder composes pool, current, guards, and pill title
  ---
  duration_ms: 1.792882
  ...
# Subtest: stage counted vault add with a stale target refuses and reopens
ok 1119 - stage counted vault add with a stale target refuses and reopens
  ---
  duration_ms: 9.798714
  ...
# Subtest: stage vault commit with a stale write notifies once and reopens
ok 1120 - stage vault commit with a stale write notifies once and reopens
  ---
  duration_ms: 7.743993
  ...
# Subtest: commitVaultRefs refuses a cycle through implicit resident edges
ok 1121 - commitVaultRefs refuses a cycle through implicit resident edges
  ---
  duration_ms: 1.537696
  ...
# Subtest: stage single remove with a stale write notifies once and reopens
ok 1122 - stage single remove with a stale write notifies once and reopens
  ---
  duration_ms: 2.701427
  ...
# Subtest: stage vault single +id guard refuses a stale target
ok 1123 - stage vault single +id guard refuses a stale target
  ---
  duration_ms: 1.299671
  ...
# Subtest: stage vault counted +id guard refuses a stale target
ok 1124 - stage vault counted +id guard refuses a stale target
  ---
  duration_ms: 0.810567
  ...
# Subtest: stage single +id guard refuses a stale target
ok 1125 - stage single +id guard refuses a stale target
  ---
  duration_ms: 0.888535
  ...
# Subtest: stage counted remove with a stale write refuses and reopens
ok 1126 - stage counted remove with a stale write refuses and reopens
  ---
  duration_ms: 2.806417
  ...
# Subtest: stage counted remove counts only changed sources
ok 1127 - stage counted remove counts only changed sources
  ---
  duration_ms: 3.99178
  ...
# Subtest: counted local add on [?] sources reads zero extra notes
ok 1128 - counted local add on [?] sources reads zero extra notes
  ---
  duration_ms: 5.852411
  ...
# Subtest: counted local toggle-off on a Pomodoro-linked [?] source recovers
ok 1129 - counted local toggle-off on a Pomodoro-linked [?] source recovers
  ---
  duration_ms: 6.280128
  ...
# Subtest: stage counted vault add counts only changed sources
ok 1130 - stage counted vault add counts only changed sources
  ---
  duration_ms: 2.387288
  ...
# Subtest: stage counted vault remove counts only changed sources
ok 1131 - stage counted vault remove counts only changed sources
  ---
  duration_ms: 1.57716
  ...
# Subtest: stage +id row prompts without writing
ok 1132 - stage +id row prompts without writing
  ---
  duration_ms: 6.757459
  ...
# Subtest: stage dismissal writes no bytes and drops the batch
ok 1133 - stage dismissal writes no bytes and drops the batch
  ---
  duration_ms: 0.893927
  ...
# Subtest: stage same-note batch commits in one undo group
ok 1134 - stage same-note batch commits in one undo group
  ---
  duration_ms: 10.291064
  ...
# Subtest: stage batch with a stale row refuses and reopens
ok 1135 - stage batch with a stale row refuses and reopens
  ---
  duration_ms: 0.979891
  ...
# Subtest: stage counted add applies to every source task
ok 1136 - stage counted add applies to every source task
  ---
  duration_ms: 34.879911
  ...
# Subtest: stage batch cycle rows stay guarded and write nothing
ok 1137 - stage batch cycle rows stay guarded and write nothing
  ---
  duration_ms: 29.031716
  ...
# Subtest: stage edit-task-dependencies registers with no default hotkey
ok 1138 - stage edit-task-dependencies registers with no default hotkey
  ---
  duration_ms: 1.46131
  ...
# Subtest: task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row
ok 1139 - task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row
  ---
  duration_ms: 0.841617
  ...
# Subtest: stage waits-on badge counts open prerequisites only
ok 1140 - stage waits-on badge counts open prerequisites only
  ---
  duration_ms: 2.088367
  ...
# Subtest: stage cycle tooltip shows task descriptions
ok 1141 - stage cycle tooltip shows task descriptions
  ---
  duration_ms: 1.617266
  ...
# Subtest: cross-note add awaits preparation before the one commit
ok 1142 - cross-note add awaits preparation before the one commit
  ---
  duration_ms: 17.436062
  ...
# Subtest: a failed async preparation leaves the dependent untouched
ok 1143 - a failed async preparation leaves the dependent untouched
  ---
  duration_ms: 7.439532
  ...
# Subtest: links to unloaded notes tolerate add, remove, and deleted targets
ok 1144 - links to unloaded notes tolerate add, remove, and deleted targets
  ---
  duration_ms: 5.468449
  ...
# Subtest: Pomodoro-linked dependents recover through the plugin vault read
ok 1145 - Pomodoro-linked dependents recover through the plugin vault read
  ---
  duration_ms: 7.985113
  ...
# Subtest: same-note batch +id stamps the target and links in one undo group
ok 1146 - same-note batch +id stamps the target and links in one undo group
  ---
  duration_ms: 11.073658
  ...
# Subtest: confirmBatchBlockId collects the id and executes the batch
ok 1147 - confirmBatchBlockId collects the id and executes the batch
  ---
  duration_ms: 2.814964
  ...
# Subtest: commitMarkedDependencies executes ready additions at once
ok 1148 - commitMarkedDependencies executes ready additions at once
  ---
  duration_ms: 2.517144
  ...
# Subtest: counted vault add links two siblings bottom-up
ok 1149 - counted vault add links two siblings bottom-up
  ---
  duration_ms: 4.985806
  ...
# Subtest: counted CURRENT rows without a line remove from every source
ok 1150 - counted CURRENT rows without a line remove from every source
  ---
  duration_ms: 5.637452
  ...
# Subtest: a stale editor between await and commit refuses
ok 1151 - a stale editor between await and commit refuses
  ---
  duration_ms: 1.575106
  ...
# Subtest: removeDependencyByRef refuses targets that are not on the line
ok 1152 - removeDependencyByRef refuses targets that are not on the line
  ---
  duration_ms: 1.528197
  ...
# Subtest: kept unloaded links resolve the field id by line position
ok 1153 - kept unloaded links resolve the field id by line position
  ---
  duration_ms: 4.980338
  ...
# Subtest: pendingTargetLine commits the same-note target id with the link
ok 1154 - pendingTargetLine commits the same-note target id with the link
  ---
  duration_ms: 3.322311
  ...
# Subtest: counted vault add commits every source in one transaction
ok 1155 - counted vault add commits every source in one transaction
  ---
  duration_ms: 4.518294
  ...
# Subtest: field-only clears snapshot the vault and recover
ok 1156 - field-only clears snapshot the vault and recover
  ---
  duration_ms: 2.405592
  ...
# Subtest: adds without recovery read zero extra vault notes
ok 1157 - adds without recovery read zero extra vault notes
  ---
  duration_ms: 1.239846
  ...
# Subtest: hand-edit clear recovers Pomodoro-linked dependents to Next
ok 1158 - hand-edit clear recovers Pomodoro-linked dependents to Next
  ---
  duration_ms: 1.557694
  ...
# Subtest: hand-edit clear on a non-Blocked parent reads zero extra notes
ok 1159 - hand-edit clear on a non-Blocked parent reads zero extra notes
  ---
  duration_ms: 0.574998
  ...
# Subtest: writer keeps the full route for duplicate basenames
ok 1160 - writer keeps the full route for duplicate basenames
  ---
  duration_ms: 1.373712
  ...
# Subtest: adds on Blocked parents and non-Blocked mirror touches read nothing
ok 1161 - adds on Blocked parents and non-Blocked mirror touches read nothing
  ---
  duration_ms: 1.431734
  ...
# Subtest: counted vault add loads each source's existing links
ok 1162 - counted vault add loads each source's existing links
  ---
  duration_ms: 4.067645
  ...
# Subtest: counted Ctrl+D on a blockquoted task refuses with the blockquote notice
ok 1163 - counted Ctrl+D on a blockquoted task refuses with the blockquote notice
  ---
  duration_ms: 0.829113
  ...
# Subtest: single Ctrl+D on a quoted task without a field refuses as a blockquote
ok 1164 - single Ctrl+D on a quoted task without a field refuses as a blockquote
  ---
  duration_ms: 0.297548
  ...
# Subtest: confirmSingleBlockId folds the target id into one transaction
ok 1165 - confirmSingleBlockId folds the target id into one transaction
  ---
  duration_ms: 2.290812
  ...
# Subtest: chooseTaskDependency folds a missing target id into one transaction
ok 1166 - chooseTaskDependency folds a missing target id into one transaction
  ---
  duration_ms: 2.110518
  ...
# Subtest: counted remove commits every source in one transaction
ok 1167 - counted remove commits every source in one transaction
  ---
  duration_ms: 3.863566
  ...
# Subtest: DP parse vectors accept, empty, malformed, and not-a-line
ok 1168 - DP parse vectors accept, empty, malformed, and not-a-line
  ---
  duration_ms: 3.029412
  ...
# Subtest: DP30 attributes a Work-Log-nested Depends-On line to the inner task
ok 1169 - DP30 attributes a Work-Log-nested Depends-On line to the inner task
  ---
  duration_ms: 2.256308
  ...
# Subtest: fenced lines never collect as Depends-On lines
ok 1170 - fenced lines never collect as Depends-On lines
  ---
  duration_ms: 0.386117
  ...
# Subtest: DW1 creates the line as the first child
ok 1171 - DW1 creates the line as the first child
  ---
  duration_ms: 4.717755
  ...
# Subtest: DW2 creates the line after a Cancel Log
ok 1172 - DW2 creates the line after a Cancel Log
  ---
  duration_ms: 1.120569
  ...
# Subtest: DW3-DW5 append, remove the middle, and delete on the last link
ok 1173 - DW3-DW5 append, remove the middle, and delete on the last link
  ---
  duration_ms: 4.085879
  ...
# Subtest: DW6-DW7 re-add moves to the end and the field mirrors the line
ok 1174 - DW6-DW7 re-add moves to the end and the field mirrors the line
  ---
  duration_ms: 0.6548
  ...
# Subtest: DW8 tab parents deepen the child by one tab
ok 1175 - DW8 tab parents deepen the child by one tab
  ---
  duration_ms: 1.107234
  ...
# Subtest: DW9 space parents reuse the existing child indent
ok 1176 - DW9 space parents reuse the existing child indent
  ---
  duration_ms: 0.919616
  ...
# Subtest: DW10-DW11 CRLF and final-newline state survive
ok 1177 - DW10-DW11 CRLF and final-newline state survive
  ---
  duration_ms: 1.022522
  ...
# Subtest: DW12-DW14 link form is the shortest unambiguous form
ok 1178 - DW12-DW14 link form is the shortest unambiguous form
  ---
  duration_ms: 0.320371
  ...
# Subtest: archive targets keep the explicit done/ path form
ok 1179 - archive targets keep the explicit done/ path form
  ---
  duration_ms: 0.236371
  ...
# Subtest: DW15 an existing id is never rewritten
ok 1180 - DW15 an existing id is never rewritten
  ---
  duration_ms: 0.384063
  ...
# Subtest: DW16 an unencodable path without an id refuses
ok 1181 - DW16 an unencodable path without an id refuses
  ---
  duration_ms: 0.307397
  ...
# Subtest: DW17 field placement follows fresh and precedes the block id
ok 1182 - DW17 field placement follows fresh and precedes the block id
  ---
  duration_ms: 0.304411
  ...
# Subtest: DW18 legacy children fold into the line
ok 1183 - DW18 legacy children fold into the line
  ---
  duration_ms: 0.850944
  ...
# Subtest: DW19 variants canonicalise to the writer form
ok 1184 - DW19 variants canonicalise to the writer form
  ---
  duration_ms: 1.392658
  ...
# Subtest: adding an open prerequisite blocks the dependent
ok 1185 - adding an open prerequisite blocks the dependent
  ---
  duration_ms: 0.362271
  ...
# Subtest: adding transfers Next and In Progress commitment to the open target
ok 1186 - adding transfers Next and In Progress commitment to the open target
  ---
  duration_ms: 0.641094
  ...
# Subtest: removing the last open prerequisite recovers immediately
ok 1187 - removing the last open prerequisite recovers immediately
  ---
  duration_ms: 0.784037
  ...
# Subtest: removal stays Blocked while another prerequisite is open
ok 1188 - removal stays Blocked while another prerequisite is open
  ---
  duration_ms: 0.344448
  ...
# Subtest: removal stays Blocked with a future schedule
ok 1189 - removal stays Blocked with a future schedule
  ---
  duration_ms: 0.309
  ...
# Subtest: one gesture commits the dependent note in a single transaction
ok 1190 - one gesture commits the dependent note in a single transaction
  ---
  duration_ms: 0.98502
  ...
# Subtest: a failed preparation leaves the dependent untouched
ok 1191 - a failed preparation leaves the dependent untouched
  ---
  duration_ms: 0.383913
  ...
# Subtest: recovery references follow the line plus covered legacy children
ok 1192 - recovery references follow the line plus covered legacy children
  ---
  duration_ms: 0.653688
  ...
# Subtest: task-block helpers find owners, lines, and insertion points
ok 1193 - task-block helpers find owners, lines, and insertion points
  ---
  duration_ms: 0.4401
  ...
# Subtest: dependency notices follow the contract shapes
ok 1194 - dependency notices follow the contract shapes
  ---
  duration_ms: 0.168241
  ...
# Subtest: nav api v3 resolves results and never throws
ok 1195 - nav api v3 resolves results and never throws
  ---
  duration_ms: 1.04802
  ...
# Subtest: getDependencyInsertLine lands after a Cancel Log subtree
ok 1196 - getDependencyInsertLine lands after a Cancel Log subtree
  ---
  duration_ms: 0.347754
  ...
# Subtest: planner: an ordinary dependent with a block id plus an open add yields one target
ok 1197 - planner: an ordinary dependent with a block id plus an open add yields one target
  ---
  duration_ms: 7.62264
  ...
# Subtest: planner: adding only a closed target yields none
ok 1198 - planner: adding only a closed target yields none
  ---
  duration_ms: 0.836457
  ...
# Subtest: planner: no block id yields none
ok 1199 - planner: no block id yields none
  ---
  duration_ms: 0.466239
  ...
# Subtest: planner: a dependent already [?] with an open add yields a target
ok 1200 - planner: a dependent already [?] with an open add yields a target
  ---
  duration_ms: 1.890869
  ...
# Subtest: planner: a removal yields none
ok 1201 - planner: a removal yields none
  ---
  duration_ms: 1.206343
  ...
# Subtest: planner: mirrorTouch emits no ordinary consumption target
ok 1202 - planner: mirrorTouch emits no ordinary consumption target
  ---
  duration_ms: 0.385536
  ...
# Subtest: planner: ^prj keeps project targets and a deduplicated union
ok 1203 - planner: ^prj keeps project targets and a deduplicated union
  ---
  duration_ms: 2.333405
  ...
# Subtest: suffix helper names the removed count and the failed follow-up
ok 1204 - suffix helper names the removed count and the failed follow-up
  ---
  duration_ms: 0.173682
  ...
# Subtest: applyDependencyEdit cross-file consumes live links and emptied entries
ok 1205 - applyDependencyEdit cross-file consumes live links and emptied entries
  ---
  duration_ms: 8.637959
  ...
# Subtest: applyDependencyEdit removes one live link and reports it
ok 1206 - applyDependencyEdit removes one live link and reports it
  ---
  duration_ms: 2.142159
  ...
# Subtest: applyDependencyEdit keeps the dependent write when the daily preimage changes
ok 1207 - applyDependencyEdit keeps the dependent write when the daily preimage changes
  ---
  duration_ms: 1.396936
  ...
# Subtest: same-file fold lands the dependency and the cleanup in one undo group
ok 1208 - same-file fold lands the dependency and the cleanup in one undo group
  ---
  duration_ms: 1.738288
  ...
# Subtest: setLocalTaskDependencyLink stays synchronous and folds same-file cleanup
ok 1209 - setLocalTaskDependencyLink stays synchronous and folds same-file cleanup
  ---
  duration_ms: 2.125237
  ...
# Subtest: setLocalTaskDependencyLink cross-file continuation removes the live link
ok 1210 - setLocalTaskDependencyLink cross-file continuation removes the live link
  ---
  duration_ms: 10.826898
  ...
# Subtest: same-note marked batch consumes every newly Blocked source
ok 1211 - same-note marked batch consumes every newly Blocked source
  ---
  duration_ms: 9.580728
  ...
# Subtest: counted same-note writer consumes every newly Blocked source
ok 1212 - counted same-note writer consumes every newly Blocked source
  ---
  duration_ms: 7.683717
  ...
# Subtest: counted vault writer consumes every newly Blocked source
ok 1213 - counted vault writer consumes every newly Blocked source
  ---
  duration_ms: 4.11192
  ...
# Subtest: counted ^prj source consumes its project targets
ok 1214 - counted ^prj source consumes its project targets
  ---
  duration_ms: 3.006028
  ...
# Subtest: a dependent without a block id does zero cachedReads even when today's daily exists
ok 1215 - a dependent without a block id does zero cachedReads even when today's daily exists
  ---
  duration_ms: 1.416815
  ...
# Subtest: missing ledger-tools api refuses the review namespace
ok 1216 - missing ledger-tools api refuses the review namespace
  ---
  duration_ms: 2.427113
  ...
# Subtest: review jump on an empty queue
ok 1217 - review jump on an empty queue
  ---
  duration_ms: 1.301023
  ...
# Subtest: review jump from a queued task goes to the neighbor
ok 1218 - review jump from a queued task goes to the neighbor
  ---
  duration_ms: 3.10683
  ...
# Subtest: review jump wraps at the ends
ok 1219 - review jump wraps at the ends
  ---
  duration_ms: 0.442044
  ...
# Subtest: review jump from elsewhere goes to the first or last entry
ok 1220 - review jump from elsewhere goes to the first or last entry
  ---
  duration_ms: 0.273342
  ...
# Subtest: review jump matches a moved cursor task by text
ok 1221 - review jump matches a moved cursor task by text
  ---
  duration_ms: 0.207617
  ...
# Subtest: review jump from a just-stamped rank goes to the entry after it
ok 1222 - review jump from a just-stamped rank goes to the entry after it
  ---
  duration_ms: 0.326503
  ...
# Subtest: review jump skips just-stamped keys the lagging cache still shows
ok 1223 - review jump skips just-stamped keys the lagging cache still shows
  ---
  duration_ms: 0.199952
  ...
# Subtest: review jump after stamping everything reports empty or wraps
ok 1224 - review jump after stamping everything reports empty or wraps
  ---
  duration_ms: 0.854451
  ...
# Subtest: review queue line resolves at the entry line
ok 1225 - review queue line resolves at the entry line
  ---
  duration_ms: 0.807902
  ...
# Subtest: review queue line follows a moved line to its unique match
ok 1226 - review queue line follows a moved line to its unique match
  ---
  duration_ms: 0.574046
  ...
# Subtest: review queue line goes stale on duplicates or a missing line
ok 1227 - review queue line goes stale on duplicates or a missing line
  ---
  duration_ms: 0.262712
  ...
# Subtest: review jump notices name the state
ok 1228 - review jump notices name the state
  ---
  duration_ms: 0.664739
  ...
# Subtest: fresh stamp targets refuse closed and recurring tasks
ok 1229 - fresh stamp targets refuse closed and recurring tasks
  ---
  duration_ms: 0.807021
  ...
# Subtest: fresh stamp batch stamps every target and nothing else
ok 1230 - fresh stamp batch stamps every target and nothing else
  ---
  duration_ms: 0.423318
  ...
# Subtest: one refusal refuses the whole fresh stamp batch
ok 1231 - one refusal refuses the whole fresh stamp batch
  ---
  duration_ms: 0.348946
  ...
# Subtest: a throwing stamper refuses the fresh stamp batch
ok 1232 - a throwing stamper refuses the fresh stamp batch
  ---
  duration_ms: 0.201324
  ...
# Subtest: fresh stamp plus Work Log prepends only stamped Pending targets
ok 1233 - fresh stamp plus Work Log prepends only stamped Pending targets
  ---
  duration_ms: 1.300472
  ...
# Subtest: blank Work Log summary and stamp refusal never create a log marker
ok 1234 - blank Work Log summary and stamp refusal never create a log marker
  ---
  duration_ms: 0.243114
  ...
# Subtest: fresh stamp notices adjust the pre-write counts
ok 1235 - fresh stamp notices adjust the pre-write counts
  ---
  duration_ms: 0.219048
  ...
# Subtest: today detection only matches today's fresh field
ok 1236 - today detection only matches today's fresh field
  ---
  duration_ms: 0.200943
  ...
# Subtest: stamped refs match the pre-write queue by line or text
ok 1237 - stamped refs match the pre-write queue by line or text
  ---
  duration_ms: 0.44012
  ...
# Subtest: review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
ok 1238 - review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
  ---
  duration_ms: 0.32491
  ...
# Subtest: tier-aware jump notices name each tier
ok 1239 - tier-aware jump notices name each tier
  ---
  duration_ms: 0.77575
  ...
# Subtest: projects tier walks with commitment rank and empty-project notice
ok 1240 - projects tier walks with commitment rank and empty-project notice
  ---
  duration_ms: 0.274344
  ...
# Subtest: references tier walks with commitment rank and reference notice
ok 1241 - references tier walks with commitment rank and reference notice
  ---
  duration_ms: 0.604063
  ...
# Subtest: jump notices use reviewEntryView when provided and keep the fallback
ok 1242 - jump notices use reviewEntryView when provided and keep the fallback
  ---
  duration_ms: 0.369025
  ...
# Subtest: tier notices fall back without tier ranks and wrap on the last line
ok 1243 - tier notices fall back without tier ranks and wrap on the last line
  ---
  duration_ms: 0.210181
  ...
# Subtest: boundary notice names commitments done and rotten next
ok 1244 - boundary notice names commitments done and rotten next
  ---
  duration_ms: 0.184492
  ...
# Subtest: walk anchor records handled keys with their neighbors
ok 1245 - walk anchor records handled keys with their neighbors
  ---
  duration_ms: 0.692391
  ...
# Subtest: cursor on a live entry wins over a lagging anchor
ok 1246 - cursor on a live entry wins over a lagging anchor
  ---
  duration_ms: 0.371089
  ...
# Subtest: [s after a stamp goes backwards from the anchor
ok 1247 - [s after a stamp goes backwards from the anchor
  ---
  duration_ms: 5.077854
  ...
# Subtest: release-then-]s continues from the anchor successor
ok 1248 - release-then-]s continues from the anchor successor
  ---
  duration_ms: 0.41884
  ...
# Subtest: non-contiguous counted stamp advances past the last handled rank
ok 1249 - non-contiguous counted stamp advances past the last handled rank
  ---
  duration_ms: 0.430151
  ...
# Subtest: anchor wraps at both ends
ok 1250 - anchor wraps at both ends
  ---
  duration_ms: 0.516596
  ...
# Subtest: advance across NEXT to TICKLER to ROTTEN lands the boundary
ok 1251 - advance across NEXT to TICKLER to ROTTEN lands the boundary
  ---
  duration_ms: 0.526485
  ...
# Subtest: tier capability gates on the freshness namespace version
ok 1252 - tier capability gates on the freshness namespace version
  ---
  duration_ms: 0.170536
  ...
# Subtest: empty queue notice reads the upkeep meter
ok 1253 - empty queue notice reads the upkeep meter
  ---
  duration_ms: 0.146619
  ...
# Subtest: refresh row reads lane intervals from the api with the once-Ready return
ok 1254 - refresh row reads lane intervals from the api with the once-Ready return
  ---
  duration_ms: 1.462873
  ...
# Subtest: endpoint jumps select the queue ends with full rank and total
ok 1255 - endpoint jumps select the queue ends with full rank and total
  ---
  duration_ms: 0.435852
  ...
# Subtest: endpoint jumps ignore cursor, anchor, and direction
ok 1256 - endpoint jumps ignore cursor, anchor, and direction
  ---
  duration_ms: 0.297198
  ...
# Subtest: endpoint jumps on empty and one-entry queues
ok 1257 - endpoint jumps on empty and one-entry queues
  ---
  duration_ms: 0.243555
  ...
# Subtest: a visited endpoint is still due under its own anchor
ok 1258 - a visited endpoint is still due under its own anchor
  ---
  duration_ms: 0.237664
  ...
# Subtest: lowercase steps continue from an endpoint anchor
ok 1259 - lowercase steps continue from an endpoint anchor
  ---
  duration_ms: 0.35088
  ...
# Subtest: counted review jump repeat 1 matches omitted repeat
ok 1260 - counted review jump repeat 1 matches omitted repeat
  ---
  duration_ms: 0.68609
  ...
# Subtest: counted review jump from the first entry lands N steps ahead
ok 1261 - counted review jump from the first entry lands N steps ahead
  ---
  duration_ms: 0.319119
  ...
# Subtest: counted review jump from the last entry wraps past the start
ok 1262 - counted review jump from the last entry wraps past the start
  ---
  duration_ms: 0.164855
  ...
# Subtest: counted review jump larger than the queue wraps once
ok 1263 - counted review jump larger than the queue wraps once
  ---
  duration_ms: 0.189862
  ...
# Subtest: counted review jump on a one-entry queue stays there
ok 1264 - counted review jump on a one-entry queue stays there
  ---
  duration_ms: 0.211303
  ...
# Subtest: counted review jump with no origin lands on the Nth entry
ok 1265 - counted review jump with no origin lands on the Nth entry
  ---
  duration_ms: 0.200612
  ...
# Subtest: counted review jump from a shaped anchor takes N surviving successors
ok 1266 - counted review jump from a shaped anchor takes N surviving successors
  ---
  duration_ms: 0.255557
  ...
# Subtest: counted review jump does not change endpoint selection
ok 1267 - counted review jump does not change endpoint selection
  ---
  duration_ms: 0.238615
  ...
# Subtest: a stamped endpoint that moved is stale and cannot land from old text
ok 1268 - a stamped endpoint that moved is stale and cannot land from old text
  ---
  duration_ms: 0.247723
  ...
# Subtest: stale endpoint target reselects the same endpoint in the new queue
ok 1269 - stale endpoint target reselects the same endpoint in the new queue
  ---
  duration_ms: 1.856072
  ...
# Subtest: endpoint retry is bounded and failures preserve the anchor
ok 1270 - endpoint retry is bounded and failures preserve the anchor
  ---
  duration_ms: 0.653347
  ...
# Subtest: endpoint jump to ROTTEN carries no boundary preamble
ok 1271 - endpoint jump to ROTTEN carries no boundary preamble
  ---
  duration_ms: 0.90094
  ...
# Subtest: endpoint notices keep v4 tier details and legacy v3 text
ok 1272 - endpoint notices keep v4 tier details and legacy v3 text
  ---
  duration_ms: 0.175094
  ...
# Subtest: onload registers first/last commands routed to the shared jump
ok 1273 - onload registers first/last commands routed to the shared jump
  ---
  duration_ms: 1.929382
  ...
# Subtest: jumpToDueTask consumes a pending Vim prefix as N review steps
ok 1274 - jumpToDueTask consumes a pending Vim prefix as N review steps
  ---
  duration_ms: 1.276106
  ...
# Subtest: registered next-due-task callback reads the pending Vim prefix
ok 1275 - registered next-due-task callback reads the pending Vim prefix
  ---
  duration_ms: 1.076375
  ...
# Subtest: explicit jumpToDueTask repeat skips the Vim prefix
ok 1276 - explicit jumpToDueTask repeat skips the Vim prefix
  ---
  duration_ms: 0.413379
  ...
# Subtest: non-normal editor with a pending prefix still jumps one entry
ok 1277 - non-normal editor with a pending prefix still jumps one entry
  ---
  duration_ms: 0.350609
  ...
# Subtest: stale counted replan reuses the captured repeat
ok 1278 - stale counted replan reuses the captured repeat
  ---
  duration_ms: 0.405154
  ...
# Subtest: endpoint jump with a pending prefix still lands on the endpoint
ok 1279 - endpoint jump with a pending prefix still lands on the endpoint
  ---
  duration_ms: 0.338286
  ...
# Subtest: counted forward landing on ROTTEN keeps the boundary preamble
ok 1280 - counted forward landing on ROTTEN keeps the boundary preamble
  ---
  duration_ms: 0.629983
  ...
# Subtest: PRE and POST are machine tiers; PRE is a commitment
ok 1281 - PRE and POST are machine tiers; PRE is a commitment
  ---
  duration_ms: 0.295815
  ...
# Subtest: fallback notices name PRE checklist and POST closeout
ok 1282 - fallback notices name PRE checklist and POST closeout
  ---
  duration_ms: 0.355479
  ...
# Subtest: text-first cursor matching does not skip Pills after an above-insert
ok 1283 - text-first cursor matching does not skip Pills after an above-insert
  ---
  duration_ms: 0.201985
  ...
# Subtest: day-scoped anchors from another day are ignored
ok 1284 - day-scoped anchors from another day are ignored
  ---
  duration_ms: 0.311855
  ...
# Subtest: boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
ok 1285 - boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
  ---
  duration_ms: 0.290064
  ...
# Subtest: ]S reaches POST with 77 ROTTEN rows and a null budget
ok 1286 - ]S reaches POST with 77 ROTTEN rows and a null budget
  ---
  duration_ms: 0.765581
  ...
# Subtest: nav normalizes a legacy v7 returned tier to tickler
ok 1287 - nav normalizes a legacy v7 returned tier to tickler
  ---
  duration_ms: 0.151539
  ...
# Subtest: RECURRING is a machine tier, a commitment, and a v9 capability
ok 1288 - RECURRING is a machine tier, a commitment, and a v9 capability
  ---
  duration_ms: 0.194732
  ...
# Subtest: RECURRING counts in reviewWalkRemaining and gates the boundary
ok 1289 - RECURRING counts in reviewWalkRemaining and gates the boundary
  ---
  duration_ms: 0.203819
  ...
# Subtest: matchReviewRecurringCursor is text-first like the checklist matcher
ok 1290 - matchReviewRecurringCursor is text-first like the checklist matcher
  ---
  duration_ms: 0.247373
  ...
# Subtest: fallback notices name RECURRING due detail with the reschedule hint
ok 1291 - fallback notices name RECURRING due detail with the reschedule hint
  ---
  duration_ms: 0.198238
  ...
# Subtest: Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
ok 1292 - Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
  ---
  duration_ms: 0.160927
  ...
# Subtest: bobLineDigest matches the shared bob-cli vectors
ok 1293 - bobLineDigest matches the shared bob-cli vectors
  ---
  duration_ms: 8.931879
  ...
# Subtest: parseGoToTaskParams accepts a complete v1 link and ignores extra keys
ok 1294 - parseGoToTaskParams accepts a complete v1 link and ignores extra keys
  ---
  duration_ms: 1.142631
  ...
# Subtest: parseGoToTaskParams treats ref and block as optional
ok 1295 - parseGoToTaskParams treats ref and block as optional
  ---
  duration_ms: 0.193139
  ...
# Subtest: parseGoToTaskParams rejects each malformed field
ok 1296 - parseGoToTaskParams rejects each malformed field
  ---
  duration_ms: 0.316223
  ...
# Subtest: vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
ok 1297 - vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
  ---
  duration_ms: 0.359176
  ...
# Subtest: refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
ok 1298 - refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
  ---
  duration_ms: 1.742918
  ...
# Subtest: handleGoToTaskUri notices each malformed parameter
ok 1299 - handleGoToTaskUri notices each malformed parameter
  ---
  duration_ms: 1.619682
  ...
# Subtest: handleGoToTaskUri notices a path outside the vault
ok 1300 - handleGoToTaskUri notices a path outside the vault
  ---
  duration_ms: 0.66538
  ...
# Subtest: handleGoToTaskUri notices a missing file inside the vault
ok 1301 - handleGoToTaskUri notices a missing file inside the vault
  ---
  duration_ms: 0.694926
  ...
# Subtest: handleGoToTaskUri maps a trailing-slash vault base
ok 1302 - handleGoToTaskUri maps a trailing-slash vault base
  ---
  duration_ms: 2.542393
  ...
# Subtest: handleGoToTaskUri prefers the open buffer over cachedRead
ok 1303 - handleGoToTaskUri prefers the open buffer over cachedRead
  ---
  duration_ms: 1.093527
  ...
# Subtest: handleGoToTaskUri re-finds by block id after an insert above the task
ok 1304 - handleGoToTaskUri re-finds by block id after an insert above the task
  ---
  duration_ms: 0.676221
  ...
# Subtest: handleGoToTaskUri re-finds a unique digest after a shift with no block
ok 1305 - handleGoToTaskUri re-finds a unique digest after a shift with no block
  ---
  duration_ms: 0.702291
  ...
# Subtest: handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
ok 1306 - handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
  ---
  duration_ms: 0.530793
  ...
# Subtest: handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
ok 1307 - handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
  ---
  duration_ms: 0.529721
  ...
# Subtest: handleGoToTaskUri reuses a leaf that already shows the note
ok 1308 - handleGoToTaskUri reuses a leaf that already shows the note
  ---
  duration_ms: 0.590316
  ...
# Subtest: handleGoToTaskUri switches a Reading-view leaf to editing
ok 1309 - handleGoToTaskUri switches a Reading-view leaf to editing
  ---
  duration_ms: 0.519822
  ...
# Subtest: handleGoToTaskUri records a jump from the prior cursor and none without one
ok 1310 - handleGoToTaskUri records a jump from the prior cursor and none without one
  ---
  duration_ms: 0.847237
  ...
# Subtest: handleGoToTaskUri never writes the vault or advances the walk
ok 1311 - handleGoToTaskUri never writes the vault or advances the walk
  ---
  duration_ms: 0.365748
  ...
# Subtest: handleGoToTaskUri reports when the note cannot be opened
ok 1312 - handleGoToTaskUri reports when the note cannot be opened
  ---
  duration_ms: 0.285064
  ...
# Subtest: focusTaskMoveDestination still lands without switching Reading view
ok 1313 - focusTaskMoveDestination still lands without switching Reading view
  ---
  duration_ms: 0.357262
  ...
# Subtest: onload registers bob-goto-task when the protocol API exists
ok 1314 - onload registers bob-goto-task when the protocol API exists
  ---
  duration_ms: 0.959462
  ...
# Subtest: onload skips protocol registration when the API is missing
ok 1315 - onload skips protocol registration when the API is missing
  ---
  duration_ms: 0.305974
  ...
# Subtest: registered protocol handler forwards params to handleGoToTaskUri
ok 1316 - registered protocol handler forwards params to handleGoToTaskUri
  ---
  duration_ms: 0.38792
  ...
# Subtest: handleGoToTaskUri maps a path through realpath when prefixes differ
ok 1317 - handleGoToTaskUri maps a path through realpath when prefixes differ
  ---
  duration_ms: 2.612196
  ...
# Subtest: cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
ok 1318 - cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
  ---
  duration_ms: 2.131709
  ...
# Subtest: findCancelLogParent finds a direct child but ignores a grandchild
ok 1319 - findCancelLogParent finds a direct child but ignores a grandchild
  ---
  duration_ms: 0.858589
  ...
# Subtest: getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
ok 1320 - getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
  ---
  duration_ms: 0.310793
  ...
# Subtest: formatCancelLogEntryText renders the exact preview text
ok 1321 - formatCancelLogEntryText renders the exact preview text
  ---
  duration_ms: 0.200012
  ...
# Subtest: planCancelLogEntry inserts a first-child log with tabs or spaces
ok 1322 - planCancelLogEntry inserts a first-child log with tabs or spaces
  ---
  duration_ms: 0.973148
  ...
# Subtest: planCancelLogEntry prepends under an existing log wherever it sits
ok 1323 - planCancelLogEntry prepends under an existing log wherever it sits
  ---
  duration_ms: 0.35589
  ...
# Subtest: planCancelLogEntry uses the fallback only when a marker exists
ok 1324 - planCancelLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.354947
  ...
# Subtest: isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
ok 1325 - isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
  ---
  duration_ms: 0.387049
  ...
# Subtest: describeCancelTaskRow covers single, counted, link, recurring, and hidden
ok 1326 - describeCancelTaskRow covers single, counted, link, recurring, and hidden
  ---
  duration_ms: 2.522184
  ...
# Subtest: planTaskCancelBatch cancels a single task with a first-child log
ok 1327 - planTaskCancelBatch cancels a single task with a first-child log
  ---
  duration_ms: 1.683853
  ...
# Subtest: planTaskCancelBatch upserts cancelled before the block id and preserves fields
ok 1328 - planTaskCancelBatch upserts cancelled before the block id and preserves fields
  ---
  duration_ms: 0.690368
  ...
# Subtest: planTaskCancelBatch records id-field task identities
ok 1329 - planTaskCancelBatch records id-field task identities
  ---
  duration_ms: 0.26164
  ...
# Subtest: planTaskCancelBatch skips closed targets and stays bottom-up
ok 1330 - planTaskCancelBatch skips closed targets and stays bottom-up
  ---
  duration_ms: 0.463815
  ...
# Subtest: planTaskCancelBatch refuses recurring targets in all three syntaxes
ok 1331 - planTaskCancelBatch refuses recurring targets in all three syntaxes
  ---
  duration_ms: 0.492219
  ...
# Subtest: planTaskCancelBatch handles empty reasons and stale preimages
ok 1332 - planTaskCancelBatch handles empty reasons and stale preimages
  ---
  duration_ms: 0.396527
  ...
# Subtest: planTaskCancelBatch preserves CRLF line endings
ok 1333 - planTaskCancelBatch preserves CRLF line endings
  ---
  duration_ms: 0.264475
  ...
# Subtest: cancel project conversion carries the log and reports it
ok 1334 - cancel project conversion carries the log and reports it
  ---
  duration_ms: 3.708921
  ...
# Subtest: getCancelTaskRowTitle names single, counted, and link sessions
ok 1335 - getCancelTaskRowTitle names single, counted, and link sessions
  ---
  duration_ms: 1.482741
  ...
# Subtest: getCancelReasonHints labels Enter per state and Esc as Keep open
ok 1336 - getCancelReasonHints labels Enter per state and Esc as Keep open
  ---
  duration_ms: 1.113175
  ...
# Subtest: the Cancel property item and the card's cancel row describe an open task
ok 1337 - the Cancel property item and the card's cancel row describe an open task
  ---
  duration_ms: 14.360954
  ...
# Subtest: Cancel row hides on closed tasks, plain bullets, and all-closed sessions
ok 1338 - Cancel row hides on closed tasks, plain bullets, and all-closed sessions
  ---
  duration_ms: 5.127077
  ...
# Subtest: Cancel row reports skipped closed targets in a counted session
ok 1339 - Cancel row reports skipped closed targets in a counted session
  ---
  duration_ms: 1.231541
  ...
# Subtest: the card refuses the cancel row on a recurring task and stays on the card
ok 1340 - the card refuses the cancel row on a recurring task and stays on the card
  ---
  duration_ms: 1.737287
  ...
# Subtest: cancel reason stage previews the typed, empty, fallback, and :: cases
ok 1341 - cancel reason stage previews the typed, empty, fallback, and :: cases
  ---
  duration_ms: 2.528938
  ...
# Subtest: cancel reason footer flips between plain, log, and fallback labels
ok 1342 - cancel reason footer flips between plain, log, and fallback labels
  ---
  duration_ms: 0.841396
  ...
# Subtest: Esc from the cancel reason stage writes nothing
ok 1343 - Esc from the cancel reason stage writes nothing
  ---
  duration_ms: 2.135235
  ...
# Subtest: single cancel writes [-], stamp, and first-child log in one transaction
ok 1344 - single cancel writes [-], stamp, and first-child log in one transaction
  ---
  duration_ms: 4.140073
  ...
# Subtest: empty reason writes no log unless one already exists
ok 1345 - empty reason writes no log unless one already exists
  ---
  duration_ms: 3.839711
  ...
# Subtest: stale single preimage refuses with nothing written
ok 1346 - stale single preimage refuses with nothing written
  ---
  duration_ms: 1.141539
  ...
# Subtest: cancel writes [-] with no NOW chip
ok 1347 - cancel writes [-] with no NOW chip
  ---
  duration_ms: 3.862543
  ...
# Subtest: TSC recovery runs with cancelled identities; a missing API still succeeds
ok 1348 - TSC recovery runs with cancelled identities; a missing API still succeeds
  ---
  duration_ms: 3.454324
  ...
# Subtest: a throwing TSC API is skipped silently with no chip
ok 1349 - a throwing TSC API is skipped silently with no chip
  ---
  duration_ms: 1.687291
  ...
# Subtest: counted cancel skips closed targets and reports them
ok 1350 - counted cancel skips closed targets and reports them
  ---
  duration_ms: 2.133212
  ...
# Subtest: same-file cancel folds today's Pomodoro prune into one transaction
ok 1351 - same-file cancel folds today's Pomodoro prune into one transaction
  ---
  duration_ms: 3.586014
  ...
# Subtest: link session cancels the target and removes the invoking link bullet
ok 1352 - link session cancels the target and removes the invoking link bullet
  ---
  duration_ms: 6.059126
  ...
# Subtest: buildCancelNoticeModel text covers every chip
ok 1353 - buildCancelNoticeModel text covers every chip
  ---
  duration_ms: 0.263503
  ...
# Subtest: renderCancelNoticeFragment builds the is-cancel card
ok 1354 - renderCancelNoticeFragment builds the is-cancel card
  ---
  duration_ms: 0.677093
  ...
# Subtest: isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
ok 1355 - isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
  ---
  duration_ms: 1.489333
  ...
# Subtest: findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
ok 1356 - findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
  ---
  duration_ms: 1.600455
  ...
# Subtest: collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
ok 1357 - collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
  ---
  duration_ms: 0.59702
  ...
# Subtest: planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
ok 1358 - planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
  ---
  duration_ms: 1.174633
  ...
# Subtest: planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
ok 1359 - planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
  ---
  duration_ms: 1.024035
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
ok 1360 - planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
  ---
  duration_ms: 0.930957
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
ok 1361 - planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
  ---
  duration_ms: 0.772284
  ...
# Subtest: planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
ok 1362 - planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
  ---
  duration_ms: 0.284463
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
ok 1363 - planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
  ---
  duration_ms: 1.187576
  ...
# Subtest: planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
ok 1364 - planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
  ---
  duration_ms: 0.914786
  ...
# Subtest: planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
ok 1365 - planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
  ---
  duration_ms: 0.748639
  ...
# Subtest: planDeferredPomodoroLinkCleanup preserves CRLF line endings
ok 1366 - planDeferredPomodoroLinkCleanup preserves CRLF line endings
  ---
  duration_ms: 0.303289
  ...
# Subtest: deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
ok 1367 - deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
  ---
  duration_ms: 0.285836
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks\#^x]] \#
ok 1368 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks\#^x]] \#
  ---
  duration_ms: 0.28813
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks\#^x|alias]] \#
ok 1369 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks\#^x|alias]] \#
  ---
  duration_ms: 0.159414
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks\#^x]]
ok 1370 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks\#^x]]
  ---
  duration_ms: 0.205322
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks\#^x]]
ok 1371 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks\#^x]]
  ---
  duration_ms: 0.16742
  ...
# Subtest: dedicated decoration check accepts paired strikes but cleanup never removes struck links
ok 1372 - dedicated decoration check accepts paired strikes but cleanup never removes struck links
  ---
  duration_ms: 0.352052
  ...
# Subtest: cleanup deletes only touched childless entries, preserving prose, placeholders and closed history
ok 1373 - cleanup deletes only touched childless entries, preserving prose, placeholders and closed history
  ---
  duration_ms: 0.47691
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\n", final newline false)
ok 1374 - cleanup handles adjacent EOF entries ("\\n", final newline false)
  ---
  duration_ms: 0.283681
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\n", final newline true)
ok 1375 - cleanup handles adjacent EOF entries ("\\n", final newline true)
  ---
  duration_ms: 0.264034
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\r\\n", final newline false)
ok 1376 - cleanup handles adjacent EOF entries ("\\r\\n", final newline false)
  ---
  duration_ms: 0.244416
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\r\\n", final newline true)
ok 1377 - cleanup handles adjacent EOF entries ("\\r\\n", final newline true)
  ---
  duration_ms: 0.222195
  ...
# Subtest: counted dependencies converge mixed sources and maintain one link per parent
ok 1378 - counted dependencies converge mixed sources and maintain one link per parent
  ---
  duration_ms: 11.895116
  ...
# Subtest: counted and single dependency gestures refuse inside a blockquote (DP29)
ok 1379 - counted and single dependency gestures refuse inside a blockquote (DP29)
  ---
  duration_ms: 0.495857
  ...
# Subtest: counted dependency candidates exclude every source and expose mixed state
ok 1380 - counted dependency candidates exclude every source and expose mixed state
  ---
  duration_ms: 0.989529
  ...
# Subtest: counted dependency block-ID prompting is planned atomically
ok 1381 - counted dependency block-ID prompting is planned atomically
  ---
  duration_ms: 2.076855
  ...
# Subtest: counted dependency runtime applies target, parents, and navigation in one undo group
ok 1382 - counted dependency runtime applies target, parents, and navigation in one undo group
  ---
  duration_ms: 6.414795
  ...
# Subtest: counted Depends-on removal recovers residents with [unblocked::]
ok 1383 - counted Depends-on removal recovers residents with [unblocked::]
  ---
  duration_ms: 4.50553
  ...
# Subtest: counted Depends-on removal writes [unblocked::] through the wired freshness API
ok 1384 - counted Depends-on removal writes [unblocked::] through the wired freshness API
  ---
  duration_ms: 4.182154
  ...
# Subtest: cross-file toggle changes only the source link
ok 1385 - cross-file toggle changes only the source link
  ---
  duration_ms: 1.471008
  ...
# Subtest: cross-file write failure still toggles only the source link
ok 1386 - cross-file write failure still toggles only the source link
  ---
  duration_ms: 0.732268
  ...
# Subtest: line-local fallback applies bottom-up and preserves CRLF
ok 1387 - line-local fallback applies bottom-up and preserves CRLF
  ---
  duration_ms: 0.849642
  ...
# Subtest: source line-count invariant rejects embedded newline changes
ok 1388 - source line-count invariant rejects embedded newline changes
  ---
  duration_ms: 0.266289
  ...
# Subtest: pure toggle refuses when the source changed under it
ok 1389 - pure toggle refuses when the source changed under it
  ---
  duration_ms: 0.191646
  ...
# Subtest: counted transclusion toggle evaluates each line independently
ok 1390 - counted transclusion toggle evaluates each line independently
  ---
  duration_ms: 0.406056
  ...
# Subtest: transclusion toggle is refused on Depends-On lines
ok 1391 - transclusion toggle is refused on Depends-On lines
  ---
  duration_ms: 0.274514
  ...
# Subtest: legacy sole-link children toggle purely, without field or status writes
ok 1392 - legacy sole-link children toggle purely, without field or status writes
  ---
  duration_ms: 0.364496
  ...
# Subtest: Ctrl+D on the Depends on row clears the line, field, and legacy children
ok 1393 - Ctrl+D on the Depends on row clears the line, field, and legacy children
  ---
  duration_ms: 2.866683
  ...
# Subtest: Ctrl+D clears a field-only dependency without a line
ok 1394 - Ctrl+D clears a field-only dependency without a line
  ---
  duration_ms: 1.014677
  ...
# Subtest: counted Ctrl+D on the Depends on row clears every targeted task
ok 1395 - counted Ctrl+D on the Depends on row clears every targeted task
  ---
  duration_ms: 2.367579
  ...
# Subtest: findRemovedLineText reports deleted lines
ok 1396 - findRemovedLineText reports deleted lines
  ---
  duration_ms: 0.248294
  ...
# Subtest: hand-edit mirror projects an edited line into the field
ok 1397 - hand-edit mirror projects an edited line into the field
  ---
  duration_ms: 1.462381
  ...
# Subtest: hand-edit mirror canonicalises a hand-written line variant
ok 1398 - hand-edit mirror canonicalises a hand-written line variant
  ---
  duration_ms: 0.674518
  ...
# Subtest: hand-edit mirror drops a linkless line and the field
ok 1399 - hand-edit mirror drops a linkless line and the field
  ---
  duration_ms: 2.019114
  ...
# Subtest: hand-edit mirror clears the field after the line is deleted
ok 1400 - hand-edit mirror clears the field after the line is deleted
  ---
  duration_ms: 0.793996
  ...
# Subtest: hand-edit mirror leaves malformed lines alone
ok 1401 - hand-edit mirror leaves malformed lines alone
  ---
  duration_ms: 0.231131
  ...
# Subtest: hand-edit mirror leaves legacy-only children for the hooks
ok 1402 - hand-edit mirror leaves legacy-only children for the hooks
  ---
  duration_ms: 0.294883
  ...
# Subtest: hand-edit mirror blocks when an open prerequisite is added by hand
ok 1403 - hand-edit mirror blocks when an open prerequisite is added by hand
  ---
  duration_ms: 0.7071
  ...
# Subtest: hand-edit mirror never transfers commitment to the target
ok 1404 - hand-edit mirror never transfers commitment to the target
  ---
  duration_ms: 0.888215
  ...
# Subtest: hand-edit mirror recovers when the last open prerequisite is removed by hand
ok 1405 - hand-edit mirror recovers when the last open prerequisite is removed by hand
  ---
  duration_ms: 1.202716
  ...
# Subtest: hand-edit mirror leaves a half-typed link alone
ok 1406 - hand-edit mirror leaves a half-typed link alone
  ---
  duration_ms: 0.323598
  ...
# Subtest: hand-edit mirror clears the owning task when its last-child line is deleted
ok 1407 - hand-edit mirror clears the owning task when its last-child line is deleted
  ---
  duration_ms: 0.85877
  ...
# Subtest: mirror scheduler debounces at the contract interval
ok 1408 - mirror scheduler debounces at the contract interval
  ---
  duration_ms: 0.935706
  ...
# Subtest: mirror scheduler seeds the baseline from the update start state
ok 1409 - mirror scheduler seeds the baseline from the update start state
  ---
  duration_ms: 1.875259
  ...
# Subtest: mirror scheduler keeps the first baseline and maps the owner across a burst
ok 1410 - mirror scheduler keeps the first baseline and maps the owner across a burst
  ---
  duration_ms: 0.603852
  ...
# Subtest: mirror listener runs clear-field for a first-edit deletion with a following sibling
ok 1411 - mirror listener runs clear-field for a first-edit deletion with a following sibling
  ---
  duration_ms: 10.662013
  ...
# Subtest: mirror fire re-arms while the cursor stays on the edited line
ok 1412 - mirror fire re-arms while the cursor stays on the edited line
  ---
  duration_ms: 2.428796
  ...
# Subtest: mirror scheduler reads changed ranges from the CM6 update
ok 1413 - mirror scheduler reads changed ranges from the CM6 update
  ---
  duration_ms: 0.28262
  ...
# Subtest: mirror scheduler skips IME composition
ok 1414 - mirror scheduler skips IME composition
  ---
  duration_ms: 0.213127
  ...
# Subtest: mirror scheduler skips open modals
ok 1415 - mirror scheduler skips open modals
  ---
  duration_ms: 0.191796
  ...
# Subtest: counted Ctrl+D clears every targeted task in one transaction with one notice
ok 1416 - counted Ctrl+D clears every targeted task in one transaction with one notice
  ---
  duration_ms: 4.491805
  ...
# Subtest: counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
ok 1417 - counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
  ---
  duration_ms: 2.854278
  ...
# Subtest: counted N! on only a Depends-On line refuses without writing
ok 1418 - counted N! on only a Depends-On line refuses without writing
  ---
  duration_ms: 0.399733
  ...
# Subtest: promotion targets enumerate real tasks and assign stable IDs
ok 1419 - promotion targets enumerate real tasks and assign stable IDs
  ---
  duration_ms: 3.722116
  ...
# Subtest: promotion file planner expands live links and preserves history
ok 1420 - promotion file planner expands live links and preserves history
  ---
  duration_ms: 4.039772
  ...
# Subtest: promotion file planner handles forms, whitespace, and subtrees
ok 1421 - promotion file planner handles forms, whitespace, and subtrees
  ---
  duration_ms: 1.114698
  ...
# Subtest: promotion file planner keeps compatibility for non-live references
ok 1422 - promotion file planner keeps compatibility for non-live references
  ---
  duration_ms: 0.666151
  ...
# Subtest: forward promotion expands live links, persists anchors, and removes the source
ok 1423 - forward promotion expands live links, persists anchors, and removes the source
  ---
  duration_ms: 7.182311
  ...
# Subtest: forward promotion uses zero-task fallback and keeps reverse one-to-one
ok 1424 - forward promotion uses zero-task fallback and keeps reverse one-to-one
  ---
  duration_ms: 0.945434
  ...
# Subtest: forward promotion retains the source on ambiguous, stale, and write failures
ok 1425 - forward promotion retains the source on ambiguous, stale, and write failures
  ---
  duration_ms: 1.091904
  ...
# Subtest: forward promotion discovers live links without a backlink cache and uses one open-editor write
ok 1426 - forward promotion discovers live links without a backlink cache and uses one open-editor write
  ---
  duration_ms: 1.410893
  ...
# Subtest: forward conversion carries a Depends-On line and reverse restores it
not ok 1427 - forward conversion carries a Depends-On line and reverse restores it
  ---
  duration_ms: 17.426826
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/test-navigation-hotkeys-forward-promotion.cjs:662:1'
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
      '- [?] #task Ship it [created::2026-10-16] [id:: Areas__Work__ship] [dependsOn:: Areas__Work__prereq] ^ship\n' +
      '\t- ⛓️ **DEPENDS ON:** [[#^prereq]]\n' +
      '\t- [?] #task Follow up [created::2026-10-16] ^follow-up'
    
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
    - [?] #task Ship it [created::2026-10-16] [id:: Areas__Work__ship] [dependsOn:: Areas__Work__prereq] ^ship
    	- ⛓️ **DEPENDS ON:** [[#^prereq]]
    	- [?] #task Follow up [created::2026-10-16] ^follow-up
  operator: 'doesNotMatch'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-plugins/scripts/test-navigation-hotkeys-forward-promotion.cjs:734:10)
    async Test.run (node:internal/test_runner/test:980:9)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: planTaskLaneBatch commits every Ready target to Next
ok 1428 - planTaskLaneBatch commits every Ready target to Next
  ---
  duration_ms: 3.364803
  ...
# Subtest: planTaskLaneBatch releases Next and In Progress to Ready
ok 1429 - planTaskLaneBatch releases Next and In Progress to Ready
  ---
  duration_ms: 0.504854
  ...
# Subtest: planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
ok 1430 - planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
  ---
  duration_ms: 0.916188
  ...
# Subtest: planTaskLaneBatch skips Blocked and refuses stale preimages
ok 1431 - planTaskLaneBatch skips Blocked and refuses stale preimages
  ---
  duration_ms: 0.361119
  ...
# Subtest: buildLaneToggleNotice reports commit and release with and without budgets
ok 1432 - buildLaneToggleNotice reports commit and release with and without budgets
  ---
  duration_ms: 0.381759
  ...
# Subtest: describeLaneRow covers task, counted, and link sessions
ok 1433 - describeLaneRow covers task, counted, and link sessions
  ---
  duration_ms: 0.506557
  ...
# Subtest: toggleTaskLane commits Ready to Next and reports lane budgets
ok 1434 - toggleTaskLane commits Ready to Next and reports lane budgets
  ---
  duration_ms: 2.387577
  ...
# Subtest: toggleTaskLane releases to Ready without the api
ok 1435 - toggleTaskLane releases to Ready without the api
  ---
  duration_ms: 1.295673
  ...
# Subtest: toggleTaskLane release logs the summary on In Progress tasks
ok 1436 - toggleTaskLane release logs the summary on In Progress tasks
  ---
  duration_ms: 0.83293
  ...
# Subtest: toggleTaskLane skips Blocked targets
ok 1437 - toggleTaskLane skips Blocked targets
  ---
  duration_ms: 0.778567
  ...
# Subtest: counted toggleTaskLane covers the current task plus the next N tasks
ok 1438 - counted toggleTaskLane covers the current task plus the next N tasks
  ---
  duration_ms: 0.467122
  ...
# Subtest: toggleTaskLane on a Task Link writes through the open buffer
ok 1439 - toggleTaskLane on a Task Link writes through the open buffer
  ---
  duration_ms: 3.034613
  ...
# Subtest: toggleTaskLane on Task Links releases across notes
ok 1440 - toggleTaskLane on Task Links releases across notes
  ---
  duration_ms: 1.062448
  ...
# Subtest: toggleTaskLane refuses when a preimage changed
ok 1441 - toggleTaskLane refuses when a preimage changed
  ---
  duration_ms: 0.179021
  ...
# Subtest: Ctrl+Shift+P shows a pinned lane row that commits immediately
ok 1442 - Ctrl+Shift+P shows a pinned lane row that commits immediately
  ---
  duration_ms: 9.934915
  ...
# Subtest: Ctrl+Shift+P link mode shows the lane row with release detail
ok 1443 - Ctrl+Shift+P link mode shows the lane row with release detail
  ---
  duration_ms: 3.962593
  ...
# Subtest: Ctrl+Shift+P lane release with In Progress goes through the reason stage
ok 1444 - Ctrl+Shift+P lane release with In Progress goes through the reason stage
  ---
  duration_ms: 2.280874
  ...
# Subtest: getLinkPickerSessionSubtitle keeps the clamp for a single link
ok 1445 - getLinkPickerSessionSubtitle keeps the clamp for a single link
  ---
  duration_ms: 0.131882
  ...
# Subtest: link-mode priority notice keeps via Task Links visible
ok 1446 - link-mode priority notice keeps via Task Links visible
  ---
  duration_ms: 0.68621
  ...
# Subtest: already-handled Alt+N leaves Vim state alone
ok 1447 - already-handled Alt+N leaves Vim state alone
  ---
  duration_ms: 0.363955
  ...
# Subtest: Alt+N fallback still dispatches once with the Vim count
ok 1448 - Alt+N fallback still dispatches once with the Vim count
  ---
  duration_ms: 0.637807
  ...
# Subtest: lane release deletes an emptied entry (cross-file, Alt+N)
ok 1449 - lane release deletes an emptied entry (cross-file, Alt+N)
  ---
  duration_ms: 2.372499
  ...
# Subtest: lane release deletes an emptied entry (cross-file, card)
ok 1450 - lane release deletes an emptied entry (cross-file, card)
  ---
  duration_ms: 1.921116
  ...
# Subtest: lane release deletes an emptied entry (same-file, Alt+N)
ok 1451 - lane release deletes an emptied entry (same-file, Alt+N)
  ---
  duration_ms: 0.68119
  ...
# Subtest: lane release deletes an emptied entry (same-file, card)
ok 1452 - lane release deletes an emptied entry (same-file, card)
  ---
  duration_ms: 1.631384
  ...
# Subtest: Task Link release deletes its entry in one undo group (separate, Alt+N)
ok 1453 - Task Link release deletes its entry in one undo group (separate, Alt+N)
  ---
  duration_ms: 1.269774
  ...
# Subtest: Task Link release deletes its entry in one undo group (separate, card)
ok 1454 - Task Link release deletes its entry in one undo group (separate, card)
  ---
  duration_ms: 4.700192
  ...
# Subtest: Task Link release deletes its entry in one undo group (folded, Alt+N)
ok 1455 - Task Link release deletes its entry in one undo group (folded, Alt+N)
  ---
  duration_ms: 1.107724
  ...
# Subtest: Task Link release deletes its entry in one undo group (folded, card)
ok 1456 - Task Link release deletes its entry in one undo group (folded, card)
  ---
  duration_ms: 2.501836
  ...
# Subtest: parseLinkPickerTaskLink recognizes dedicated Task Link bullets
ok 1457 - parseLinkPickerTaskLink recognizes dedicated Task Link bullets
  ---
  duration_ms: 2.065572
  ...
# Subtest: discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
ok 1458 - discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
  ---
  duration_ms: 1.041619
  ...
# Subtest: discoverLinkPickerTargets leaves \#task lines to the regular picker
ok 1459 - discoverLinkPickerTargets leaves \#task lines to the regular picker
  ---
  duration_ms: 0.286947
  ...
# Subtest: findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
ok 1460 - findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
  ---
  duration_ms: 0.454237
  ...
# Subtest: createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
ok 1461 - createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
  ---
  duration_ms: 1.891781
  ...
# Subtest: getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
ok 1462 - getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
  ---
  duration_ms: 0.659799
  ...
# Subtest: bare link mode edits the task behind a Task Link through the open buffer
ok 1463 - bare link mode edits the task behind a Task Link through the open buffer
  ---
  duration_ms: 14.797186
  ...
# Subtest: counted link mode writes across notes through both the open buffer and the vault
ok 1464 - counted link mode writes across notes through both the open buffer and the vault
  ---
  duration_ms: 3.978974
  ...
# Subtest: Task Link scheduled delete recovers a Blocked task through the wired freshness API
ok 1465 - Task Link scheduled delete recovers a Blocked task through the wired freshness API
  ---
  duration_ms: 6.378025
  ...
# Subtest: link mode refuses the whole operation when a linked note changed
ok 1466 - link mode refuses the whole operation when a linked note changed
  ---
  duration_ms: 3.562299
  ...
# Subtest: link mode reports a closed target and changes nothing
ok 1467 - link mode reports a closed target and changes nothing
  ---
  duration_ms: 3.102582
  ...
# Subtest: link mode defers to a future date, blocks the task, and prunes today
ok 1468 - link mode defers to a future date, blocks the task, and prunes today
  ---
  duration_ms: 10.837769
  ...
# Subtest: bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
ok 1469 - bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
  ---
  duration_ms: 2.11673
  ...
# Subtest: Task Link scheduled write deletes its entry (separate)
ok 1470 - Task Link scheduled write deletes its entry (separate)
  ---
  duration_ms: 3.115697
  ...
# Subtest: Task Link scheduled write deletes its entry (folded)
ok 1471 - Task Link scheduled write deletes its entry (folded)
  ---
  duration_ms: 4.271754
  ...
# Subtest: folded Task Link scheduling maps the cursor past logs inserted before the emptied entry
ok 1472 - folded Task Link scheduling maps the cursor past logs inserted before the emptied entry
  ---
  duration_ms: 3.744298
  ...
# Subtest: dash restore suppresses editor notice after deliberate navigation
ok 1473 - dash restore suppresses editor notice after deliberate navigation
  ---
  duration_ms: 21.855499
  ...
# Subtest: open-task dispatch timeout is registered for plugin cleanup
ok 1474 - open-task dispatch timeout is registered for plugin cleanup
  ---
  duration_ms: 0.523689
  ...
# Subtest: jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
ok 1475 - jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
  ---
  duration_ms: 4.285871
  ...
# Subtest: jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
ok 1476 - jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
  ---
  duration_ms: 1.172769
  ...
# Subtest: jumpToOpenObsidianTask keeps current-swap transaction failures local
ok 1477 - jumpToOpenObsidianTask keeps current-swap transaction failures local
  ---
  duration_ms: 0.591128
  ...
# Subtest: jumpToOpenObsidianTask refuses current-up without jumping or mutating
ok 1478 - jumpToOpenObsidianTask refuses current-up without jumping or mutating
  ---
  duration_ms: 0.390304
  ...
# Subtest: jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
ok 1479 - jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
  ---
  duration_ms: 2.6353
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
ok 1480 - Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
  ---
  duration_ms: 0.590648
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
ok 1481 - Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
  ---
  duration_ms: 0.615445
  ...
# Subtest: counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
ok 1482 - counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
  ---
  duration_ms: 0.87482
  ...
# Subtest: an impossible counted Pomodoro move refuses without jumping or mutating
ok 1483 - an impossible counted Pomodoro move refuses without jumping or mutating
  ---
  duration_ms: 0.4298
  ...
# Subtest: counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
ok 1484 - counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
  ---
  duration_ms: 0.547856
  ...
# Subtest: counted open-task jump on a sole current target keeps the existing notice
ok 1485 - counted open-task jump on a sole current target keeps the existing notice
  ---
  duration_ms: 0.170346
  ...
# Subtest: dispatch guard allows exactly one counted Pomodoro move when the command route also fires
ok 1486 - dispatch guard allows exactly one counted Pomodoro move when the command route also fires
  ---
  duration_ms: 0.622378
  ...
# Subtest: bullet property picker reconciles duplicate bare and counted opens
ok 1487 - bullet property picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 14.01367
  ...
# Subtest: bullet property picker close lifecycle clears tracking for fresh sessions
ok 1488 - bullet property picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 8.98995
  ...
# Subtest: task move picker reconciles duplicate bare and counted opens
ok 1489 - task move picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 2.842988
  ...
# Subtest: task move picker close lifecycle clears tracking for fresh sessions
ok 1490 - task move picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 1.05828
  ...
# Subtest: Pomodoro bullet move picker opens sessions and clears the shared move picker slot
ok 1491 - Pomodoro bullet move picker opens sessions and clears the shared move picker slot
  ---
  duration_ms: 3.122099
  ...
# Subtest: Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
ok 1492 - Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
  ---
  duration_ms: 0.902112
  ...
# Subtest: move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
ok 1493 - move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
  ---
  duration_ms: 1.244315
  ...
# Subtest: commitPomodoroBulletMoveSession applies one guarded same-file transaction
ok 1494 - commitPomodoroBulletMoveSession applies one guarded same-file transaction
  ---
  duration_ms: 1.929153
  ...
# Subtest: Pomodoro bullet move picker confirms = through the actual picker callback
ok 1495 - Pomodoro bullet move picker confirms = through the actual picker callback
  ---
  duration_ms: 1.262811
  ...
# Subtest: Pomodoro bullet move picker reserves =NAME for peeling a named merged component
ok 1496 - Pomodoro bullet move picker reserves =NAME for peeling a named merged component
  ---
  duration_ms: 1.458975
  ...
# Subtest: Pomodoro bullet move picker confirms =email through the actual picker callback
ok 1497 - Pomodoro bullet move picker confirms =email through the actual picker callback
  ---
  duration_ms: 1.284792
  ...
# Subtest: Pomodoro bullet move picker confirms = review through the actual picker callback
ok 1498 - Pomodoro bullet move picker confirms = review through the actual picker callback
  ---
  duration_ms: 0.694095
  ...
# Subtest: Pomodoro bullet move picker confirms =focus by unnaming a single-name source
ok 1499 - Pomodoro bullet move picker confirms =focus by unnaming a single-name source
  ---
  duration_ms: 0.665079
  ...
# Subtest: Pomodoro bullet split stale-content guard does not write
ok 1500 - Pomodoro bullet split stale-content guard does not write
  ---
  duration_ms: 0.312536
  ...
# Subtest: Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
ok 1501 - Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
  ---
  duration_ms: 2.360515
  ...
# Subtest: native isOpen regression: pickers attach, close clears slot, reopen works
ok 1502 - native isOpen regression: pickers attach, close clears slot, reopen works
  ---
  duration_ms: 2.638597
  ...
# Subtest: stale registered pickers fail open on the next key
ok 1503 - stale registered pickers fail open on the next key
  ---
  duration_ms: 2.443565
  ...
# Subtest: planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
ok 1504 - planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
  ---
  duration_ms: 4.850408
  ...
# Subtest: planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
ok 1505 - planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
  ---
  duration_ms: 0.608462
  ...
# Subtest: planPomodoroBulletMove preserves the source when only some siblings move out
ok 1506 - planPomodoroBulletMove preserves the source when only some siblings move out
  ---
  duration_ms: 0.380617
  ...
# Subtest: planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
ok 1507 - planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
  ---
  duration_ms: 0.422847
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
ok 1508 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
  ---
  duration_ms: 0.658527
  ...
# Subtest: planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
ok 1509 - planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
  ---
  duration_ms: 0.840765
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
ok 1510 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
  ---
  duration_ms: 0.485427
  ...
# Subtest: planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
ok 1511 - planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
  ---
  duration_ms: 0.351852
  ...
# Subtest: planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
ok 1512 - planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
  ---
  duration_ms: 0.568926
  ...
# Subtest: planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
ok 1513 - planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
  ---
  duration_ms: 0.919746
  ...
# Subtest: planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
ok 1514 - planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
  ---
  duration_ms: 0.354456
  ...
# Subtest: planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
ok 1515 - planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
  ---
  duration_ms: 0.287479
  ...
# Subtest: planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
ok 1516 - planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
  ---
  duration_ms: 0.483764
  ...
# Subtest: planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
ok 1517 - planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
  ---
  duration_ms: 0.382961
  ...
# Subtest: planPomodoroBulletMove deletes both open and closed source entries the same way
ok 1518 - planPomodoroBulletMove deletes both open and closed source entries the same way
  ---
  duration_ms: 0.411596
  ...
# Subtest: planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
ok 1519 - planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
  ---
  duration_ms: 0.312467
  ...
# Subtest: planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
ok 1520 - planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
  ---
  duration_ms: 0.351331
  ...
# Subtest: planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
ok 1521 - planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
  ---
  duration_ms: 0.465108
  ...
# Subtest: planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
ok 1522 - planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
  ---
  duration_ms: 0.304983
  ...
# Subtest: planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
ok 1523 - planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
  ---
  duration_ms: 0.516837
  ...
# Subtest: planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
ok 1524 - planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
  ---
  duration_ms: 0.348606
  ...
# Subtest: planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
ok 1525 - planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
  ---
  duration_ms: 0.353705
  ...
# Subtest: planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
ok 1526 - planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
  ---
  duration_ms: 0.257642
  ...
# Subtest: planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
ok 1527 - planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
  ---
  duration_ms: 0.508942
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
ok 1528 - planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
  ---
  duration_ms: 0.250368
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
ok 1529 - planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
  ---
  duration_ms: 0.692542
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
ok 1530 - planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
  ---
  duration_ms: 5.75309
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
ok 1531 - planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
  ---
  duration_ms: 0.545111
  ...
# Subtest: Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
ok 1532 - Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
  ---
  duration_ms: 5.61599
  ...
# Subtest: commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
ok 1533 - commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
  ---
  duration_ms: 2.330228
  ...
# Subtest: commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
ok 1534 - commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
  ---
  duration_ms: 0.836257
  ...
# Subtest: commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
ok 1535 - commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
  ---
  duration_ms: 0.489324
  ...
# Subtest: commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
ok 1536 - commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
  ---
  duration_ms: 0.387921
  ...
# Subtest: Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
ok 1537 - Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
  ---
  duration_ms: 7.662226
  ...
# Subtest: Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
ok 1538 - Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
  ---
  duration_ms: 0.909076
  ...
# Subtest: Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
ok 1539 - Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
  ---
  duration_ms: 0.763628
  ...
# Subtest: Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
ok 1540 - Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
  ---
  duration_ms: 1.205992
  ...
# Subtest: task move picker closes before commit while other pickers retain delayed close
ok 1541 - task move picker closes before commit while other pickers retain delayed close
  ---
  duration_ms: 0.89589
  ...
# Subtest: parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
ok 1542 - parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
  ---
  duration_ms: 2.019645
  ...
# Subtest: normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
ok 1543 - normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
  ---
  duration_ms: 0.391207
  ...
# Subtest: formatPomodoroEntryLine emits a placeholder entry with or without a name
ok 1544 - formatPomodoroEntryLine emits a placeholder entry with or without a name
  ---
  duration_ms: 0.154094
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
ok 1545 - createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
  ---
  duration_ms: 2.149843
  ...
# Subtest: createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
ok 1546 - createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
  ---
  duration_ms: 0.898545
  ...
# Subtest: createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
ok 1547 - createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
  ---
  duration_ms: 0.688153
  ...
# Subtest: createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
ok 1548 - createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
  ---
  duration_ms: 0.645111
  ...
# Subtest: buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
ok 1549 - buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
  ---
  duration_ms: 0.238676
  ...
# Subtest: buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
ok 1550 - buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
  ---
  duration_ms: 0.376298
  ...
# Subtest: createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
ok 1551 - createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
  ---
  duration_ms: 0.64461
  ...
# Subtest: createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
ok 1552 - createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
  ---
  duration_ms: 0.370106
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
ok 1553 - createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
  ---
  duration_ms: 0.466461
  ...
# Subtest: collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
ok 1554 - collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
  ---
  duration_ms: 0.552234
  ...
# Subtest: findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
ok 1555 - findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
  ---
  duration_ms: 0.650712
  ...
# Subtest: findPomodoroBulletContext leaves plain \#task lines on the task-move route
ok 1556 - findPomodoroBulletContext leaves plain \#task lines on the task-move route
  ---
  duration_ms: 0.425793
  ...
# Subtest: discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
ok 1557 - discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
  ---
  duration_ms: 1.0631
  ...
# Subtest: findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
ok 1558 - findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
  ---
  duration_ms: 0.820326
  ...
# Subtest: discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
ok 1559 - discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
  ---
  duration_ms: 0.89077
  ...
# Subtest: isMovablePomodoroEntryContext matches open current and future Pomodoro entries
ok 1560 - isMovablePomodoroEntryContext matches open current and future Pomodoro entries
  ---
  duration_ms: 2.912229
  ...
# Subtest: planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
ok 1561 - planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
  ---
  duration_ms: 0.788194
  ...
# Subtest: planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
ok 1562 - planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
  ---
  duration_ms: 0.328837
  ...
# Subtest: planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
ok 1563 - planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
  ---
  duration_ms: 0.379475
  ...
# Subtest: planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
ok 1564 - planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
  ---
  duration_ms: 0.422216
  ...
# Subtest: planPomodoroEntryReorder handles counted current swaps and their inverses
ok 1565 - planPomodoroEntryReorder handles counted current swaps and their inverses
  ---
  duration_ms: 0.495706
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
ok 1566 - planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
  ---
  duration_ms: 0.269034
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
ok 1567 - planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
  ---
  duration_ms: 0.22518
  ...
# Subtest: planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
ok 1568 - planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
  ---
  duration_ms: 0.484414
  ...
# Subtest: planPomodoroEntryReorder round-trips a future-up swap across the current open entry
ok 1569 - planPomodoroEntryReorder round-trips a future-up swap across the current open entry
  ---
  duration_ms: 0.577443
  ...
# Subtest: planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
ok 1570 - planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
  ---
  duration_ms: 0.579696
  ...
# Subtest: planPomodoroEntryReorder refuses moving down past the last placeholder in the section
ok 1571 - planPomodoroEntryReorder refuses moving down past the last placeholder in the section
  ---
  duration_ms: 0.2466
  ...
# Subtest: planPomodoroEntryReorder refuses both directions for a lone placeholder
ok 1572 - planPomodoroEntryReorder refuses both directions for a lone placeholder
  ---
  duration_ms: 0.16759
  ...
# Subtest: planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
ok 1573 - planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
  ---
  duration_ms: 0.160968
  ...
# Subtest: planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
ok 1574 - planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
  ---
  duration_ms: 0.264084
  ...
# Subtest: planPomodoroEntryReorder refuses illegal current/future spans atomically
ok 1575 - planPomodoroEntryReorder refuses illegal current/future spans atomically
  ---
  duration_ms: 0.55565
  ...
# Subtest: planPomodoroEntryReorder rejects a stale source line
ok 1576 - planPomodoroEntryReorder rejects a stale source line
  ---
  duration_ms: 0.185444
  ...
# Subtest: planPomodoroEntryReorder round-trips CRLF content
ok 1577 - planPomodoroEntryReorder round-trips CRLF content
  ---
  duration_ms: 0.353555
  ...
# Subtest: planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
ok 1578 - planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
  ---
  duration_ms: 0.278512
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
ok 1579 - planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
  ---
  duration_ms: 0.402989
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up three positions and round-trips
ok 1580 - planPomodoroEntryReorder moves a placeholder up three positions and round-trips
  ---
  duration_ms: 0.539139
  ...
# Subtest: planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
ok 1581 - planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
  ---
  duration_ms: 0.265217
  ...
# Subtest: planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
ok 1582 - planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
  ---
  duration_ms: 0.693615
  ...
# Subtest: planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
ok 1583 - planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
  ---
  duration_ms: 0.756053
  ...
# Subtest: planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
ok 1584 - planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
  ---
  duration_ms: 0.327155
  ...
# Subtest: peelPomodoroMergedName removes every matching canonical plus component
ok 1585 - peelPomodoroMergedName removes every matching canonical plus component
  ---
  duration_ms: 1.518058
  ...
# Subtest: planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
ok 1586 - planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
  ---
  duration_ms: 3.91345
  ...
# Subtest: planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
ok 1587 - planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
  ---
  duration_ms: 0.728802
  ...
# Subtest: planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
ok 1588 - planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
  ---
  duration_ms: 0.819224
  ...
# Subtest: planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
ok 1589 - planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
  ---
  duration_ms: 1.047199
  ...
# Subtest: planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
ok 1590 - planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
  ---
  duration_ms: 1.54558
  ...
# Subtest: planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
ok 1591 - planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
  ---
  duration_ms: 0.760361
  ...
# Subtest: planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
ok 1592 - planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
  ---
  duration_ms: 1.62948
  ...
# Subtest: Pomodoro bullet move picker typing =NAME or Escape does not write
ok 1593 - Pomodoro bullet move picker typing =NAME or Escape does not write
  ---
  duration_ms: 3.076443
  ...
# Subtest: planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
ok 1594 - planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
  ---
  duration_ms: 0.531435
  ...
# Subtest: planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
ok 1595 - planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
  ---
  duration_ms: 0.263052
  ...
# Subtest: planPomodoroEntryRename reports unchanged when the normalized name matches the current name
ok 1596 - planPomodoroEntryRename reports unchanged when the normalized name matches the current name
  ---
  duration_ms: 0.133154
  ...
# Subtest: planPomodoroEntryRename rejects unsupported trailing content and a stale source line
ok 1597 - planPomodoroEntryRename rejects unsupported trailing content and a stale source line
  ---
  duration_ms: 0.149896
  ...
# Subtest: planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
ok 1598 - planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
  ---
  duration_ms: 0.14698
  ...
# Subtest: planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
ok 1599 - planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
  ---
  duration_ms: 1.533667
  ...
# Subtest: planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
ok 1600 - planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
  ---
  duration_ms: 1.007462
  ...
# Subtest: planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
ok 1601 - planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
  ---
  duration_ms: 0.490596
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: priority notice relative day helpers handle offsets ranges and icons
ok 1602 - priority notice relative day helpers handle offsets ranges and icons
  ---
  duration_ms: 1.73929
  ...
# Subtest: priority notice model summarizes single counted and project writes
ok 1603 - priority notice model summarizes single counted and project writes
  ---
  duration_ms: 3.494761
  ...
# Subtest: priority notice renderer builds an accessible fragment
ok 1604 - priority notice renderer builds an accessible fragment
  ---
  duration_ms: 2.099879
  ...
# Subtest: priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
ok 1605 - priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
  ---
  duration_ms: 7.698366
  ...
# Subtest: priority notice falls back to one plain notice without a DOM
ok 1606 - priority notice falls back to one plain notice without a DOM
  ---
  duration_ms: 0.53456
  ...
# Subtest: priority notice falls back to plain text when fragment rendering fails
ok 1607 - priority notice falls back to plain text when fragment rendering fails
  ---
  duration_ms: 0.354527
  ...
# Subtest: priority scheduling rolls inclusively and clamps a random value of one
ok 1608 - priority scheduling rolls inclusively and clamps a random value of one
  ---
  duration_ms: 0.48183
  ...
# Subtest: priority value rows preserve config order and expose labels ranges and current state
ok 1609 - priority value rows preserve config order and expose labels ranges and current state
  ---
  duration_ms: 0.757526
  ...
# Subtest: priority picker writes priority then rolled schedule in one guarded edit
ok 1610 - priority picker writes priority then rolled schedule in one guarded edit
  ---
  duration_ms: 12.919261
  ...
# Subtest: priority picker writes lowest priority with a wide rolled schedule
ok 1611 - priority picker writes lowest priority with a wide rolled schedule
  ---
  duration_ms: 2.618579
  ...
# Subtest: priority picker replaces both existing values without duplicating fields
ok 1612 - priority picker replaces both existing values without duplicating fields
  ---
  duration_ms: 2.960712
  ...
# Subtest: counted priority writes keep the rolled date right of the priority
ok 1613 - counted priority writes keep the rolled date right of the priority
  ---
  duration_ms: 4.679883
  ...
# Subtest: priority picker writes project priority and schedule inline atomically
ok 1614 - priority picker writes project priority and schedule inline atomically
  ---
  duration_ms: 5.614058
  ...
# Subtest: counted priority picker rolls an independent schedule for every task
ok 1615 - counted priority picker rolls an independent schedule for every task
  ---
  duration_ms: 2.219256
  ...
# Subtest: counted priority planning keeps project schedules inline
ok 1616 - counted priority planning keeps project schedules inline
  ---
  duration_ms: 1.216853
  ...
# Subtest: counted priority planning evaluates Blocked recovery per rolled date
ok 1617 - counted priority planning evaluates Blocked recovery per rolled date
  ---
  duration_ms: 1.055545
  ...
# Subtest: a counted priority batch writes one entry per task using each task's own previous level
ok 1618 - a counted priority batch writes one entry per task using each task's own previous level
  ---
  duration_ms: 0.791631
  ...
# Subtest: priority notice models carry the stored level value for the glyph
ok 1619 - priority notice models carry the stored level value for the glyph
  ---
  duration_ms: 0.374856
  ...
# Subtest: ledger priority mark lookup guards version and render
ok 1620 - ledger priority mark lookup guards version and render
  ---
  duration_ms: 0.134927
  ...
# Subtest: priority notice header reuses the shared mark when available
ok 1621 - priority notice header reuses the shared mark when available
  ---
  duration_ms: 1.287076
  ...
# Subtest: priority notice keeps the Lucide icon without a usable mark api
ok 1622 - priority notice keeps the Lucide icon without a usable mark api
  ---
  duration_ms: 1.043391
  ...
# Subtest: a counted priority batch skips a task whose rolled date equals its current date
ok 1623 - a counted priority batch skips a task whose rolled date equals its current date
  ---
  duration_ms: 6.669662
  ...
# Subtest: counted priority runtime aborts a stale session without rolling writes
ok 1624 - counted priority runtime aborts a stale session without rolling writes
  ---
  duration_ms: 1.98569
  ...
# Subtest: scheduled picker pins a priority roll only for configured current priorities
ok 1625 - scheduled picker pins a priority roll only for configured current priorities
  ---
  duration_ms: 15.474439
  ...
# Subtest: Ctrl+R replaces only the pinned priority roll and keeps it selected
ok 1626 - Ctrl+R replaces only the pinned priority roll and keeps it selected
  ---
  duration_ms: 5.837793
  ...
# Subtest: choosing a priority roll writes immediately with a deterministic reason instead of prompting
ok 1627 - choosing a priority roll writes immediately with a deterministic reason instead of prompting
  ---
  duration_ms: 4.836772
  ...
# Subtest: counted scheduled picker requires one shared configured priority
ok 1628 - counted scheduled picker requires one shared configured priority
  ---
  duration_ms: 5.538442
  ...
# Subtest: buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
ok 1629 - buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
  ---
  duration_ms: 2.733207
  ...
# Subtest: buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
ok 1630 - buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
  ---
  duration_ms: 0.295775
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
ok 1631 - buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
  ---
  duration_ms: 0.464336
  ...
# Subtest: buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
ok 1632 - buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
  ---
  duration_ms: 0.436153
  ...
# Subtest: buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
ok 1633 - buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
  ---
  duration_ms: 0.419481
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
ok 1634 - buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
  ---
  duration_ms: 0.183671
  ...
# Subtest: buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
ok 1635 - buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
  ---
  duration_ms: 0.236481
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
ok 1636 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
  ---
  duration_ms: 0.44002
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child work log under the project task
ok 1637 - buildProjectSeedFromChildBullets moves a direct-child work log under the project task
  ---
  duration_ms: 0.391938
  ...
# Subtest: buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
ok 1638 - buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
  ---
  duration_ms: 0.541414
  ...
# Subtest: buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
ok 1639 - buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
  ---
  duration_ms: 0.362572
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
ok 1640 - buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
  ---
  duration_ms: 0.249126
  ...
# Subtest: buildProjectSeedFromChildBullets moves an empty work log without forcing task output
ok 1641 - buildProjectSeedFromChildBullets moves an empty work log without forcing task output
  ---
  duration_ms: 0.169814
  ...
# Subtest: buildProjectSeedFromChildBullets moves both logs in source order without sorting by kind
ok 1642 - buildProjectSeedFromChildBullets moves both logs in source order without sorting by kind
  ---
  duration_ms: 0.247252
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
ok 1643 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
  ---
  duration_ms: 0.353114
  ...
# Subtest: parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
ok 1644 - parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
  ---
  duration_ms: 0.271889
  ...
# Subtest: parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
ok 1645 - parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
  ---
  duration_ms: 0.155206
  ...
# Subtest: parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
ok 1646 - parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
  ---
  duration_ms: 0.51344
  ...
# Subtest: normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
ok 1647 - normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
  ---
  duration_ms: 0.092717
  ...
# Subtest: parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
ok 1648 - parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
  ---
  duration_ms: 0.107375
  ...
# Subtest: formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
ok 1649 - formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
  ---
  duration_ms: 0.117174
  ...
# Subtest: insertProjectSectionNotes fills an empty existing section with a blank line then the notes
ok 1650 - insertProjectSectionNotes fills an empty existing section with a blank line then the notes
  ---
  duration_ms: 0.600115
  ...
# Subtest: insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
ok 1651 - insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
  ---
  duration_ms: 0.175976
  ...
# Subtest: insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
ok 1652 - insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
  ---
  duration_ms: 0.135008
  ...
# Subtest: insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
ok 1653 - insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
  ---
  duration_ms: 0.240208
  ...
# Subtest: insertProjectSectionNotes does not add a trailing newline when the original content had none
ok 1654 - insertProjectSectionNotes does not add a trailing newline when the original content had none
  ---
  duration_ms: 0.155808
  ...
# Subtest: insertProjectSectionNotes preserves CRLF line endings for an existing section
ok 1655 - insertProjectSectionNotes preserves CRLF line endings for an existing section
  ---
  duration_ms: 0.213608
  ...
# Subtest: insertProjectSectionNotes creates a new section using the document's CRLF line ending
ok 1656 - insertProjectSectionNotes creates a new section using the document's CRLF line ending
  ---
  duration_ms: 0.167189
  ...
# Subtest: buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
ok 1657 - buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
  ---
  duration_ms: 0.250027
  ...
# Subtest: buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
ok 1658 - buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
  ---
  duration_ms: 0.490236
  ...
# Subtest: buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
ok 1659 - buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
  ---
  duration_ms: 0.139286
  ...
# Subtest: buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
ok 1660 - buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
  ---
  duration_ms: 1.381507
  ...
# Subtest: project conversion accepts blocked sources and extracts their managed dependency child
ok 1661 - project conversion accepts blocked sources and extracts their managed dependency child
  ---
  duration_ms: 2.137661
  ...
# Subtest: project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
ok 1662 - project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
  ---
  duration_ms: 1.15259
  ...
# Subtest: buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
ok 1663 - buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
  ---
  duration_ms: 0.368824
  ...
# Subtest: buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
ok 1664 - buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
  ---
  duration_ms: 0.225681
  ...
# Subtest: buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
ok 1665 - buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
  ---
  duration_ms: 0.199611
  ...
# Subtest: insertProjectManagedLogLines preserves CRLF line endings
ok 1666 - insertProjectManagedLogLines preserves CRLF line endings
  ---
  duration_ms: 0.160066
  ...
# Subtest: findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
ok 1667 - findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
  ---
  duration_ms: 0.207206
  ...
# Subtest: getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
ok 1668 - getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
  ---
  duration_ms: 0.211464
  ...
# Subtest: getProjectFromTaskNoticeText reports moved log kinds in a fixed order
ok 1669 - getProjectFromTaskNoticeText reports moved log kinds in a fixed order
  ---
  duration_ms: 0.118146
  ...
# Subtest: forward conversion leaves the project Ready when only the source status was Blocked
ok 1670 - forward conversion leaves the project Ready when only the source status was Blocked
  ---
  duration_ms: 0.376559
  ...
# Subtest: buildTaskBlockFromProjectNote restores the worked example and round-trips
ok 1671 - buildTaskBlockFromProjectNote restores the worked example and round-trips
  ---
  duration_ms: 6.78489
  ...
# Subtest: project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
ok 1672 - project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
  ---
  duration_ms: 2.138342
  ...
# Subtest: buildTaskLineFromProjectNote preserves status, tags, and fields
ok 1673 - buildTaskLineFromProjectNote preserves status, tags, and fields
  ---
  duration_ms: 1.355889
  ...
# Subtest: getProjectReversalBlockId inverts the forward basename helper
ok 1674 - getProjectReversalBlockId inverts the forward basename helper
  ---
  duration_ms: 0.122444
  ...
# Subtest: formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
ok 1675 - formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
  ---
  duration_ms: 0.13102
  ...
# Subtest: splitProjectNoteForReversal treats TASKS as the task section and keeps section order
ok 1676 - splitProjectNoteForReversal treats TASKS as the task section and keeps section order
  ---
  duration_ms: 0.907613
  ...
# Subtest: indentProjectReversalLine preserves relative depth and drops blanks
ok 1677 - indentProjectReversalLine preserves relative depth and drops blanks
  ---
  duration_ms: 0.525042
  ...
# Subtest: buildTaskBlockFromProjectNote reports structure and frontmatter errors
ok 1678 - buildTaskBlockFromProjectNote reports structure and frontmatter errors
  ---
  duration_ms: 1.226651
  ...
# Subtest: buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
ok 1679 - buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
  ---
  duration_ms: 1.023133
  ...
# Subtest: rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
ok 1680 - rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
  ---
  duration_ms: 0.536955
  ...
# Subtest: collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
ok 1681 - collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
  ---
  duration_ms: 0.614563
  ...
# Subtest: getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
ok 1682 - getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
  ---
  duration_ms: 0.211804
  ...
# Subtest: convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
ok 1683 - convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
  ---
  duration_ms: 5.111097
  ...
# Subtest: project reversal recovers tagged residents when they leave a blocked project
ok 1684 - project reversal recovers tagged residents when they leave a blocked project
  ---
  duration_ms: 3.799652
  ...
# Subtest: convertProjectNoteToTask separates the restored task from a count-only parent section
ok 1685 - convertProjectNoteToTask separates the restored task from a count-only parent section
  ---
  duration_ms: 1.219778
  ...
# Subtest: createProjectNoteFromTask dispatches reverse only on a real ^prj line
ok 1686 - createProjectNoteFromTask dispatches reverse only on a real ^prj line
  ---
  duration_ms: 1.808011
  ...
# Subtest: convertProjectNoteToTask refusals leave every file untouched
ok 1687 - convertProjectNoteToTask refusals leave every file untouched
  ---
  duration_ms: 3.887922
  ...
# Subtest: planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
ok 1688 - planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
  ---
  duration_ms: 0.168291
  ...
# Subtest: convertProjectNoteToTask writes the parent first when it links to \#^prj
ok 1689 - convertProjectNoteToTask writes the parent first when it links to \#^prj
  ---
  duration_ms: 1.260536
  ...
# Subtest: convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
ok 1690 - convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
  ---
  duration_ms: 3.551188
  ...
# Subtest: convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
ok 1691 - convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
  ---
  duration_ms: 0.841897
  ...
# Subtest: convertProjectNoteToTask reports post-write failures without rolling back
ok 1692 - convertProjectNoteToTask reports post-write failures without rolling back
  ---
  duration_ms: 0.91659
  ...
# Subtest: convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
ok 1693 - convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
  ---
  duration_ms: 0.830355
  ...
# Subtest: convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
ok 1694 - convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
  ---
  duration_ms: 1.137221
  ...
# Subtest: reading tasks read with the book prefix, plain tasks unchanged
ok 1695 - reading tasks read with the book prefix, plain tasks unchanged
  ---
  duration_ms: 1.228084
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 1696 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.249506
  ...
# Subtest: picker rows carry the book prefix in displayText
ok 1697 - picker rows carry the book prefix in displayText
  ---
  duration_ms: 0.645272
  ...
# Subtest: managed reference rename modal and submit are refused
ok 1698 - managed reference rename modal and submit are refused
  ---
  duration_ms: 1.20539
  ...
# Subtest: legacy ref notes and non-ref notes still rename
ok 1699 - legacy ref notes and non-ref notes still rename
  ---
  duration_ms: 0.908113
  ...
# Subtest: managed reference predicate checks path and non-empty source_pdf
ok 1700 - managed reference predicate checks path and non-empty source_pdf
  ---
  duration_ms: 0.219008
  ...
# Subtest: planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
ok 1701 - planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
  ---
  duration_ms: 4.326989
  ...
# Subtest: planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
ok 1702 - planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
  ---
  duration_ms: 1.566951
  ...
# Subtest: runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
ok 1703 - runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
  ---
  duration_ms: 3.583271
  ...
# Subtest: runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
ok 1704 - runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
  ---
  duration_ms: 2.281815
  ...
# Subtest: runtime: no daily note today still writes the schedule with no Pomodoro chip
ok 1705 - runtime: no daily note today still writes the schedule with no Pomodoro chip
  ---
  duration_ms: 0.367731
  ...
# Subtest: runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
ok 1706 - runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
  ---
  duration_ms: 0.779357
  ...
# Subtest: runtime: vault.process throwing during the daily-note write is reported without throwing
ok 1707 - runtime: vault.process throwing during the daily-note write is reported without throwing
  ---
  duration_ms: 0.867406
  ...
# Subtest: runtime: the daily note open in another editor is written through that editor in its own transaction
ok 1708 - runtime: the daily note open in another editor is written through that editor in its own transaction
  ---
  duration_ms: 0.928894
  ...
# Subtest: runtime: re-running the same deferral gesture is idempotent
ok 1709 - runtime: re-running the same deferral gesture is idempotent
  ---
  duration_ms: 0.625494
  ...
# Subtest: runtime: a counted scheduled batch prunes exactly the targets that land on a future date
ok 1710 - runtime: a counted scheduled batch prunes exactly the targets that land on a future date
  ---
  duration_ms: 2.680146
  ...
# Subtest: runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
ok 1711 - runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
  ---
  duration_ms: 2.285593
  ...
# Subtest: runtime: the source note being today's daily note folds the prune into a single editor transaction
ok 1712 - runtime: the source note being today's daily note folds the prune into a single editor transaction
  ---
  duration_ms: 0.60246
  ...
# Subtest: bare future scheduled writes block only real supported open inline tasks
ok 1713 - bare future scheduled writes block only real supported open inline tasks
  ---
  duration_ms: 4.985907
  ...
# Subtest: single runtime transclusion toggle preserves viewport in one line transaction
ok 1714 - single runtime transclusion toggle preserves viewport in one line transaction
  ---
  duration_ms: 1.537886
  ...
# Subtest: same-file runtime toggle changes only markers, never fields or statuses
ok 1715 - same-file runtime toggle changes only markers, never fields or statuses
  ---
  duration_ms: 0.697692
  ...
# Subtest: pure toggle leaves a cursor moved during the toggle where it landed
ok 1716 - pure toggle leaves a cursor moved during the toggle where it landed
  ---
  duration_ms: 0.279865
  ...
# Subtest: counted runtime transclusion toggle preserves viewport and caret
ok 1717 - counted runtime transclusion toggle preserves viewport and caret
  ---
  duration_ms: 0.719744
  ...
# Subtest: counted property runtime uses one transaction and preserves caret and viewport
ok 1718 - counted property runtime uses one transaction and preserves caret and viewport
  ---
  duration_ms: 2.966873
  ...
# Subtest: bare due schedule recovery is guarded and can change only task status
ok 1719 - bare due schedule recovery is guarded and can change only task status
  ---
  duration_ms: 3.104647
  ...
# Subtest: counted due recovery applies Ready Next and In Progress in one transaction
ok 1720 - counted due recovery applies Ready Next and In Progress in one transaction
  ---
  duration_ms: 4.361646
  ...
# Subtest: scheduled recovery aborts after an asynchronous source change
ok 1721 - scheduled recovery aborts after an asynchronous source change
  ---
  duration_ms: 0.825235
  ...
# Subtest: counted property runtime aborts a stale batch without a transaction
ok 1722 - counted property runtime aborts a stale batch without a transaction
  ---
  duration_ms: 0.478544
  ...
# Subtest: counted project scheduling writes an inline date and blocks tagged residents
ok 1723 - counted project scheduling writes an inline date and blocks tagged residents
  ---
  duration_ms: 2.581117
  ...
# Subtest: future project scheduling prunes resident links and an emptied Pomodoro
ok 1724 - future project scheduling prunes resident links and an emptied Pomodoro
  ---
  duration_ms: 2.615582
  ...
# Subtest: single project scheduling recovers due residents through the gate
ok 1725 - single project scheduling recovers due residents through the gate
  ---
  duration_ms: 1.879227
  ...
# Subtest: single project schedule deletion removes propagated copies and recovers
ok 1726 - single project schedule deletion removes propagated copies and recovers
  ---
  duration_ms: 1.626324
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: formatPriorityRollScheduleReason covers all four shapes
ok 1727 - formatPriorityRollScheduleReason covers all four shapes
  ---
  duration_ms: 1.410853
  ...
# Subtest: the priority-roll picker row keeps range detail and stores the exact roll
ok 1728 - the priority-roll picker row keeps range detail and stores the exact roll
  ---
  duration_ms: 0.629702
  ...
# Subtest: buildPriorityRollScheduleLog returns null when the roll does not move the date
ok 1729 - buildPriorityRollScheduleLog returns null when the roll does not move the date
  ---
  duration_ms: 0.673175
  ...
# Subtest: getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
ok 1730 - getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
  ---
  duration_ms: 0.835175
  ...
# Subtest: a priority roll onto the current date writes the date but no log
ok 1731 - a priority roll onto the current date writes the date but no log
  ---
  duration_ms: 14.009763
  ...
# Subtest: a typed reason on an unchanged date is still written
ok 1732 - a typed reason on an unchanged date is still written
  ---
  duration_ms: 0.781893
  ...
# Subtest: schedule log bullet formatting and parsing round-trip with and without a previous value
ok 1733 - schedule log bullet formatting and parsing round-trip with and without a previous value
  ---
  duration_ms: 0.925737
  ...
# Subtest: formatScheduleLogEntryText renders entry text without indent or marker
ok 1734 - formatScheduleLogEntryText renders entry text without indent or marker
  ---
  duration_ms: 0.122544
  ...
# Subtest: schedule reason text normalization trims, collapses whitespace, and flags inline fields
ok 1735 - schedule reason text normalization trims, collapses whitespace, and flags inline fields
  ---
  duration_ms: 0.369956
  ...
# Subtest: findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
ok 1736 - findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
  ---
  duration_ms: 0.760051
  ...
# Subtest: getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
ok 1737 - getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
  ---
  duration_ms: 0.297648
  ...
# Subtest: planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
ok 1738 - planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
  ---
  duration_ms: 0.57601
  ...
# Subtest: planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
ok 1739 - planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
  ---
  duration_ms: 0.257712
  ...
# Subtest: planScheduleLogEntry uses the fallback only when a marker exists
ok 1740 - planScheduleLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.22514
  ...
# Subtest: a typed reason wins over the fallback
ok 1741 - a typed reason wins over the fallback
  ---
  duration_ms: 0.148203
  ...
# Subtest: the fallback is suppressed on an unchanged date
ok 1742 - the fallback is suppressed on an unchanged date
  ---
  duration_ms: 0.127413
  ...
# Subtest: no reason and no fallback still guards empty-reason
ok 1743 - no reason and no fallback still guards empty-reason
  ---
  duration_ms: 0.151108
  ...
# Subtest: getScheduleLogWriteOutcome maps plan outcomes for writers
ok 1744 - getScheduleLogWriteOutcome maps plan outcomes for writers
  ---
  duration_ms: 0.14638
  ...
# Subtest: hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
ok 1745 - hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
  ---
  duration_ms: 0.128706
  ...
# Subtest: counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
ok 1746 - counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
  ---
  duration_ms: 1.823881
  ...
# Subtest: empty reason through the counted planner writes no schedule log entries
ok 1747 - empty reason through the counted planner writes no schedule log entries
  ---
  duration_ms: 0.605616
  ...
# Subtest: a counted scheduled session logs only the tasks that already keep a log
ok 1748 - a counted scheduled session logs only the tasks that already keep a log
  ---
  duration_ms: 0.675279
  ...
# Subtest: the counted notice wording distinguishes a fallback batch from a typed-reason batch
ok 1749 - the counted notice wording distinguishes a fallback batch from a typed-reason batch
  ---
  duration_ms: 3.274692
  ...
# Subtest: setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
ok 1750 - setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
  ---
  duration_ms: 0.37675
  ...
# Subtest: setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
ok 1751 - setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
  ---
  duration_ms: 2.842646
  ...
# Subtest: priority bullet property config normalizes frozen levels and preserves existing shapes
ok 1752 - priority bullet property config normalizes frozen levels and preserves existing shapes
  ---
  duration_ms: 2.410881
  ...
# Subtest: priority bullet property config rejects each invalid schema category once
ok 1753 - priority bullet property config rejects each invalid schema category once
  ---
  duration_ms: 1.113696
  ...
# Subtest: project scheduling targets the inline ^prj field
ok 1754 - project scheduling targets the inline ^prj field
  ---
  duration_ms: 2.051927
  ...
# Subtest: local task properties are addable only on valid tasks but invalid metadata stays removable
ok 1755 - local task properties are addable only on valid tasks but invalid metadata stays removable
  ---
  duration_ms: 0.345239
  ...
# Subtest: dependency parent write validation rejects stale, Pomodoro, and fenced parents
ok 1756 - dependency parent write validation rejects stale, Pomodoro, and fenced parents
  ---
  duration_ms: 0.52892
  ...
# Subtest: counted property targets mean current plus N real tasks without wrapping
ok 1757 - counted property targets mean current plus N real tasks without wrapping
  ---
  duration_ms: 0.740063
  ...
# Subtest: counted property metadata distinguishes absent, common, and mixed values
ok 1758 - counted property metadata distinguishes absent, common, and mixed values
  ---
  duration_ms: 0.670199
  ...
# Subtest: counted priority metadata reports labels for common and mixed values
ok 1759 - counted priority metadata reports labels for common and mixed values
  ---
  duration_ms: 0.531775
  ...
# Subtest: counted scheduled planning updates the motivating three tasks atomically
ok 1760 - counted scheduled planning updates the motivating three tasks atomically
  ---
  duration_ms: 2.284149
  ...
# Subtest: project schedule validation accepts only real YYYY-MM-DD dates
ok 1761 - project schedule validation accepts only real YYYY-MM-DD dates
  ---
  duration_ms: 1.090351
  ...
# Subtest: source task schedule is extracted without losing task metadata
ok 1762 - source task schedule is extracted without losing task metadata
  ---
  duration_ms: 1.286986
  ...
# Subtest: source task schedule errors are focused and ambiguous fields fail
ok 1763 - source task schedule errors are focused and ambiguous fields fail
  ---
  duration_ms: 0.358274
  ...
# Subtest: project creation frontmatter never stores the task schedule
ok 1764 - project creation frontmatter never stores the task schedule
  ---
  duration_ms: 0.16771
  ...
# Subtest: future schedule labels use local date-only boundaries
ok 1765 - future schedule labels use local date-only boundaries
  ---
  duration_ms: 0.581129
  ...
# Subtest: scheduled recovery selects current and newest earlier daily across gaps
ok 1766 - scheduled recovery selects current and newest earlier daily across gaps
  ---
  duration_ms: 0.548697
  ...
# Subtest: scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
ok 1767 - scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
  ---
  duration_ms: 9.636344
  ...
# Subtest: scheduled recovery defers incompatible status settings and ambiguous identities
ok 1768 - scheduled recovery defers incompatible status settings and ambiguous identities
  ---
  duration_ms: 0.526806
  ...
# Subtest: scheduled recovery honors custom open and closed Tasks status types
ok 1769 - scheduled recovery honors custom open and closed Tasks status types
  ---
  duration_ms: 0.746735
  ...
# Subtest: scheduled recovery honors the configured Tasks global filter
ok 1770 - scheduled recovery honors the configured Tasks global filter
  ---
  duration_ms: 0.653838
  ...
# Subtest: child picker schedule metadata reads the inline ^prj date
ok 1771 - child picker schedule metadata reads the inline ^prj date
  ---
  duration_ms: 1.058321
  ...
# Subtest: task move destination schedule hydration reads cached ^prj content
ok 1772 - task move destination schedule hydration reads cached ^prj content
  ---
  duration_ms: 0.545612
  ...
# Subtest: project lifecycle task classification requires unfenced \#task with trailing ^prj
ok 1773 - project lifecycle task classification requires unfenced \#task with trailing ^prj
  ---
  duration_ms: 0.195664
  ...
# Subtest: valid Obsidian tasks require a standalone \#task checkbox in real note content
ok 1774 - valid Obsidian tasks require a standalone \#task checkbox in real note content
  ---
  duration_ms: 0.184332
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: choosing a scheduled date enters the combined review without writing anything
ok 1775 - choosing a scheduled date enters the combined review without writing anything
  ---
  duration_ms: 11.830492
  ...
# Subtest: choosing a priority level does not enter the schedule review
ok 1776 - choosing a priority level does not enter the schedule review
  ---
  duration_ms: 8.100844
  ...
# Subtest: confirming an empty reason on a task with an existing schedule log appends an unexplained entry
ok 1777 - confirming an empty reason on a task with an existing schedule log appends an unexplained entry
  ---
  duration_ms: 5.498054
  ...
# Subtest: confirming an empty reason on a task with no schedule log writes only the date
ok 1778 - confirming an empty reason on a task with no schedule log writes only the date
  ---
  duration_ms: 2.826877
  ...
# Subtest: review stage getFilteredItems always returns exactly one synthetic preview item
ok 1779 - review stage getFilteredItems always returns exactly one synthetic preview item
  ---
  duration_ms: 1.243394
  ...
# Subtest: the review preview row previews the entry it will write
ok 1780 - the review preview row previews the entry it will write
  ---
  duration_ms: 3.244102
  ...
# Subtest: the review footer flips between Skip optional logs and Apply schedule as the Reason changes
ok 1781 - the review footer flips between Skip optional logs and Apply schedule as the Reason changes
  ---
  duration_ms: 1.291886
  ...
# Subtest: closing the picker during the review clears pending schedule state and writes nothing
ok 1782 - closing the picker during the review clears pending schedule state and writes nothing
  ---
  duration_ms: 1.186996
  ...
# Subtest: scheduling Work Log eligibility requires Pending or Next \#task lines
ok 1783 - scheduling Work Log eligibility requires Pending or Next \#task lines
  ---
  duration_ms: 1.263071
  ...
# Subtest: single Pending explicit date opens one review and writes both logs
ok 1784 - single Pending explicit date opens one review and writes both logs
  ---
  duration_ms: 20.613277
  ...
# Subtest: single Next blank and whitespace summaries schedule without a Work Log
ok 1785 - single Next blank and whitespace summaries schedule without a Work Log
  ---
  duration_ms: 6.054979
  ...
# Subtest: Escape at the review writes nothing, with or without typed text
ok 1786 - Escape at the review writes nothing, with or without typed text
  ---
  duration_ms: 6.130362
  ...
# Subtest: Ready and Blocked explicit dates review the Reason with no Work summary field
ok 1787 - Ready and Blocked explicit dates review the Reason with no Work summary field
  ---
  duration_ms: 6.07771
  ...
# Subtest: future scheduling on Pending marks Blocked but still writes the Work Log
ok 1788 - future scheduling on Pending marks Blocked but still writes the Work Log
  ---
  duration_ms: 2.703079
  ...
# Subtest: today date on Pending still offers the Work Log
ok 1789 - today date on Pending still offers the Work Log
  ---
  duration_ms: 3.09558
  ...
# Subtest: priority pick on Pending freezes its roll and offers the Work Log
ok 1790 - priority pick on Pending freezes its roll and offers the Work Log
  ---
  duration_ms: 5.117518
  ...
# Subtest: counted mixed statuses share one summary only on Pending and Next
ok 1791 - counted mixed statuses share one summary only on Pending and Next
  ---
  duration_ms: 7.696772
  ...
# Subtest: counted planner composes Schedule and Work Logs bottom-up above later targets
ok 1792 - counted planner composes Schedule and Work Logs bottom-up above later targets
  ---
  duration_ms: 1.208918
  ...
# Subtest: counted planner writes a Work Log even when the date is unchanged
ok 1793 - counted planner writes a Work Log even when the date is unchanged
  ---
  duration_ms: 0.387199
  ...
# Subtest: scheduling Work Log ownership keeps nested logs and CRLF endings
ok 1794 - scheduling Work Log ownership keeps nested logs and CRLF endings
  ---
  duration_ms: 0.967316
  ...
# Subtest: scheduling Work Log warns on :: and preserves Markdown
ok 1795 - scheduling Work Log warns on :: and preserves Markdown
  ---
  duration_ms: 5.078135
  ...
# Subtest: stale task while reviewing refuses with no scheduling or log writes
ok 1796 - stale task while reviewing refuses with no scheduling or log writes
  ---
  duration_ms: 1.951535
  ...
# Subtest: scheduling prompts never leak into lane or cancel stages
ok 1797 - scheduling prompts never leak into lane or cancel stages
  ---
  duration_ms: 2.718108
  ...
# Subtest: Pomodoro-marked links are not managed dependency bullets
ok 1798 - Pomodoro-marked links are not managed dependency bullets
  ---
  duration_ms: 1.549989
  ...
# Subtest: deleting inline scheduled metadata recovers Blocked targets by snapshot rank
ok 1799 - deleting inline scheduled metadata recovers Blocked targets by snapshot rank
  ---
  duration_ms: 4.354472
  ...
# Subtest: counted future scheduling blocks only supported open inline task statuses
ok 1800 - counted future scheduling blocks only supported open inline task statuses
  ---
  duration_ms: 1.809384
  ...
# Subtest: counted property planning rejects any stale source with no partial result
ok 1801 - counted property planning rejects any stale source with no partial result
  ---
  duration_ms: 0.271709
  ...
# Subtest: counted project scheduling writes the ^prj inline date and blocks tagged residents
ok 1802 - counted project scheduling writes the ^prj inline date and blocks tagged residents
  ---
  duration_ms: 1.763577
  ...
# Subtest: moving a project schedule earlier replaces only exact old-date copies
ok 1803 - moving a project schedule earlier replaces only exact old-date copies
  ---
  duration_ms: 0.440771
  ...
# Subtest: future project schedules block every open resident and consume review status
ok 1804 - future project schedules block every open resident and consume review status
  ---
  duration_ms: 0.58153
  ...
# Subtest: due project dates recover residents through the gate and write unblocked markers
ok 1805 - due project dates recover residents through the gate and write unblocked markers
  ---
  duration_ms: 0.542725
  ...
# Subtest: schedule deletion removes only exact project-date copies and recovers residents
ok 1806 - schedule deletion removes only exact project-date copies and recovers residents
  ---
  duration_ms: 0.895098
  ...
# Subtest: dependency lines render one canonical Depends-On line per parent
ok 1807 - dependency lines render one canonical Depends-On line per parent
  ---
  duration_ms: 0.631425
  ...
# Subtest: dependency IDs encode root and nested Markdown paths deterministically
ok 1808 - dependency IDs encode root and nested Markdown paths deterministically
  ---
  duration_ms: 0.879909
  ...
# Subtest: prompted block IDs truthfully replace legacy id fields
ok 1809 - prompted block IDs truthfully replace legacy id fields
  ---
  duration_ms: 0.175495
  ...
# Subtest: dependency navigation identity includes note path and folds legacy children
ok 1810 - dependency navigation identity includes note path and folds legacy children
  ---
  duration_ms: 0.844682
  ...
# Subtest: retired dependency bullets are excluded from single and counted toggles
ok 1811 - retired dependency bullets are excluded from single and counted toggles
  ---
  duration_ms: 0.832259
  ...
# Subtest: dependsOn replacement accepts spaces around field name and separator
ok 1812 - dependsOn replacement accepts spaces around field name and separator
  ---
  duration_ms: 0.286136
  ...
# Subtest: task status helpers keep Blocked open but rankless
ok 1813 - task status helpers keep Blocked open but rankless
  ---
  duration_ms: 0.295194
  ...
# Subtest: a due project date with only closed Depends-On history strips the tag
ok 1814 - a due project date with only closed Depends-On history strips the tag
  ---
  duration_ms: 0.760812
  ...
# Subtest: Ctrl+D with only closed Depends-On history strips the tag
ok 1815 - Ctrl+D with only closed Depends-On history strips the tag
  ---
  duration_ms: 0.457623
  ...
# Subtest: Ctrl+D with an open Depends-On link remaining keeps the tag
ok 1816 - Ctrl+D with an open Depends-On link remaining keeps the tag
  ---
  duration_ms: 0.364376
  ...
# Subtest: counted ^prj schedule sessions write [unblocked::] when the writer is passed
ok 1817 - counted ^prj schedule sessions write [unblocked::] when the writer is passed
  ---
  duration_ms: 0.507528
  ...
# Subtest: a due project date keeps the tag while ^prj holds Depends-On links
ok 1818 - a due project date keeps the tag while ^prj holds Depends-On links
  ---
  duration_ms: 0.294052
  ...
# Subtest: a due project date strips the tag while a resident with its own reason stays Blocked
ok 1819 - a due project date strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.279844
  ...
# Subtest: Ctrl+D strips the tag while a resident with its own reason stays Blocked
ok 1820 - Ctrl+D strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.339498
  ...
# Subtest: counted scheduled deletes recover with [unblocked::] when the writer is passed
ok 1821 - counted scheduled deletes recover with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.222876
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: section-header navigation moves normally and cycles at boundaries
ok 1822 - section-header navigation moves normally and cycles at boundaries
  ---
  duration_ms: 1.775078
  ...
# Subtest: section-header navigation wraps from beyond document boundaries
ok 1823 - section-header navigation wraps from beyond document boundaries
  ---
  duration_ms: 0.182038
  ...
# Subtest: section-header navigation handles single-header and no-header notes
ok 1824 - section-header navigation handles single-header and no-header notes
  ---
  duration_ms: 0.200132
  ...
# Subtest: open-task navigation scan includes Ready In Progress and Next and excludes Blocked
ok 1825 - open-task navigation scan includes Ready In Progress and Next and excludes Blocked
  ---
  duration_ms: 0.500375
  ...
# Subtest: open-task navigation keeps existing Pomodoro ledger targets
ok 1826 - open-task navigation keeps existing Pomodoro ledger targets
  ---
  duration_ms: 0.503451
  ...
# Subtest: next and previous jumps skip Blocked tasks and wrap to an allowed task
ok 1827 - next and previous jumps skip Blocked tasks and wrap to an allowed task
  ---
  duration_ms: 0.319109
  ...
# Subtest: blocked-only notes and a sole current allowed task have no jump target
ok 1828 - blocked-only notes and a sole current allowed task have no jump target
  ---
  duration_ms: 0.153192
  ...
# Subtest: counted open-task jumps select the Nth eligible target and wrap modulo the list
ok 1829 - counted open-task jumps select the Nth eligible target and wrap modulo the list
  ---
  duration_ms: 0.275866
  ...
# Subtest: counted open-task jumps keep sole-target and invalid-repeat behavior
ok 1830 - counted open-task jumps keep sole-target and invalid-repeat behavior
  ---
  duration_ms: 0.435331
  ...
# Subtest: tab pin Vim action registers once and toggles only the active leaf once
ok 1831 - tab pin Vim action registers once and toggles only the active leaf once
  ---
  duration_ms: 2.20058
  ...
# Subtest: tab pin toggle fails safely without a supported active leaf
ok 1832 - tab pin toggle fails safely without a supported active leaf
  ---
  duration_ms: 0.161769
  ...
# Subtest: close tabs left preserves pinned sibling tabs and refocuses active tab
ok 1833 - close tabs left preserves pinned sibling tabs and refocuses active tab
  ---
  duration_ms: 0.663206
  ...
# Subtest: close tabs right preserves pinned siblings and ignores the left side
ok 1834 - close tabs right preserves pinned siblings and ignores the left side
  ---
  duration_ms: 0.272139
  ...
# Subtest: close other tabs preserves pinned siblings on both sides
ok 1835 - close other tabs preserves pinned siblings on both sides
  ---
  duration_ms: 0.224438
  ...
# Subtest: close sibling tabs is a silent no-op when the scoped range is all pinned
ok 1836 - close sibling tabs is a silent no-op when the scoped range is all pinned
  ---
  duration_ms: 0.191415
  ...
# Subtest: close sibling tabs honors every pinned leaf representation
ok 1837 - close sibling tabs honors every pinned leaf representation
  ---
  duration_ms: 0.247072
  ...
# Subtest: close sibling tabs treats throwing view state as unpinned
ok 1838 - close sibling tabs treats throwing view state as unpinned
  ---
  duration_ms: 0.329489
  ...
# Subtest: tab pin Vim registration retries after adapter availability
ok 1839 - tab pin Vim registration retries after adapter availability
  ---
  duration_ms: 0.676631
  ...
# Subtest: isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
ok 1840 - isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
  ---
  duration_ms: 4.239832
  ...
# Subtest: isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
ok 1841 - isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
  ---
  duration_ms: 0.689376
  ...
# Subtest: isPomodoroTaskLinkLine refuses Depends-On lines and prose links
ok 1842 - isPomodoroTaskLinkLine refuses Depends-On lines and prose links
  ---
  duration_ms: 0.25153
  ...
# Subtest: decideTaskLinkLaneMode starts when any target is Next
ok 1843 - decideTaskLinkLaneMode starts when any target is Next
  ---
  duration_ms: 0.1988
  ...
# Subtest: taskLinkLaneRefusalFor renders every D5 refusal
ok 1844 - taskLinkLaneRefusalFor renders every D5 refusal
  ---
  duration_ms: 0.164985
  ...
# Subtest: planTaskLinkLaneBatch starts Next targets and leaves the rest alone
ok 1845 - planTaskLinkLaneBatch starts Next targets and leaves the rest alone
  ---
  duration_ms: 1.444898
  ...
# Subtest: planTaskLinkLaneBatch pauses with one shared Work Log entry
ok 1846 - planTaskLinkLaneBatch pauses with one shared Work Log entry
  ---
  duration_ms: 0.790129
  ...
# Subtest: planTaskLinkLaneBatch applies the freshness stamp last
ok 1847 - planTaskLinkLaneBatch applies the freshness stamp last
  ---
  duration_ms: 0.300193
  ...
# Subtest: planTaskLinkLaneBatch dedupes lines and refuses stale preimages
ok 1848 - planTaskLinkLaneBatch dedupes lines and refuses stale preimages
  ---
  duration_ms: 0.546774
  ...
# Subtest: buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
ok 1849 - buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
  ---
  duration_ms: 0.727168
  ...
# Subtest: taskLinkLanePromptState drives the Move to Next prompt
ok 1850 - taskLinkLanePromptState drives the Move to Next prompt
  ---
  duration_ms: 0.246992
  ...
# Subtest: TaskLinkLanePromptModal submits, previews live, and cancels silently
ok 1851 - TaskLinkLanePromptModal submits, previews live, and cancels silently
  ---
  duration_ms: 1.574194
  ...
# Subtest: TaskLinkLanePromptModal renders the batch context card
ok 1852 - TaskLinkLanePromptModal renders the batch context card
  ---
  duration_ms: 0.441122
  ...
# Subtest: findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
ok 1853 - findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
  ---
  duration_ms: 0.367662
  ...
# Subtest: L1: toggle starts a Next link, stamps, hints, and notices
ok 1854 - L1: toggle starts a Next link, stamps, hints, and notices
  ---
  duration_ms: 4.380121
  ...
# Subtest: L2/L3: toggle pauses through the prompt, logging one shared entry
ok 1855 - L2/L3: toggle pauses through the prompt, logging one shared entry
  ---
  duration_ms: 12.399781
  ...
# Subtest: L4: cancelling the prompt writes nothing and shows no Notice
ok 1856 - L4: cancelling the prompt writes nothing and shows no Notice
  ---
  duration_ms: 3.0172
  ...
# Subtest: L5: both directions run the same toggle twice for a round trip
ok 1857 - L5: both directions run the same toggle twice for a round trip
  ---
  duration_ms: 2.313336
  ...
# Subtest: L6: Ready, Blocked, done, and cancelled targets are refused
ok 1858 - L6: Ready, Blocked, done, and cancelled targets are refused
  ---
  duration_ms: 1.891661
  ...
# Subtest: L6: missing targets keep the existing resolver error
ok 1859 - L6: missing targets keep the existing resolver error
  ---
  duration_ms: 0.286417
  ...
# Subtest: L7: a counted start flips every Next sibling and leaves In Progress alone
ok 1860 - L7: a counted start flips every Next sibling and leaves In Progress alone
  ---
  duration_ms: 0.60741
  ...
# Subtest: L8: a counted pause prompts once and skips Blocked with a count
ok 1861 - L8: a counted pause prompts once and skips Blocked with a count
  ---
  duration_ms: 2.020437
  ...
# Subtest: L9: an over-long count clamps at the entry end without error
ok 1862 - L9: an over-long count clamps at the entry end without error
  ---
  duration_ms: 0.766143
  ...
# Subtest: L10: a closed-entry history line toggles the task and keeps the line
ok 1863 - L10: a closed-entry history line toggles the task and keeps the line
  ---
  duration_ms: 0.338296
  ...
# Subtest: L11: a target edited while the prompt is open refuses stale
ok 1864 - L11: a target edited while the prompt is open refuses stale
  ---
  duration_ms: 2.091914
  ...
# Subtest: L12: an embedded Pomodoro link takes the two-state toggle
ok 1865 - L12: an embedded Pomodoro link takes the two-state toggle
  ---
  duration_ms: 0.687132
  ...
# Subtest: L14: the same task linked twice in a batch is written once
ok 1866 - L14: the same task linked twice in a batch is written once
  ---
  duration_ms: 1.52973
  ...
# Subtest: L15: a second toggle while one is in flight is swallowed as busy
ok 1867 - L15: a second toggle while one is in flight is swallowed as busy
  ---
  duration_ms: 0.875421
  ...
# Subtest: toggle on a non-link line refuses without writing
ok 1868 - toggle on a non-link line refuses without writing
  ---
  duration_ms: 0.530643
  ...
# Subtest: api.taskLinkLane is a frozen v1 namespace that never throws
ok 1869 - api.taskLinkLane is a frozen v1 namespace that never throws
  ---
  duration_ms: 1.07905
  ...
# Subtest: the progressMarks hint is a no-op without the ledger-tools api
ok 1870 - the progressMarks hint is a no-op without the ledger-tools api
  ---
  duration_ms: 0.464667
  ...
# Subtest: task move records one Vim jump and round-trips without extra writes
ok 1871 - task move records one Vim jump and round-trips without extra writes
  ---
  duration_ms: 9.301013
  ...
# Subtest: counted task move records a single jump to the first moved task
ok 1872 - counted task move records a single jump to the first moved task
  ---
  duration_ms: 1.794967
  ...
# Subtest: deferred task landing re-anchors and records the resolved cursor once
ok 1873 - deferred task landing re-anchors and records the resolved cursor once
  ---
  duration_ms: 6.214823
  ...
# Subtest: failed task move preserves seeded history including the forward branch
ok 1874 - failed task move preserves seeded history including the forward branch
  ---
  duration_ms: 0.576631
  ...
# Subtest: post-commit open failure keeps the move committed with no jump
ok 1875 - post-commit open failure keeps the move committed with no jump
  ---
  duration_ms: 1.263231
  ...
# Subtest: a newer move supersedes a pending landing without stale placement
ok 1876 - a newer move supersedes a pending landing without stale placement
  ---
  duration_ms: 9.957206
  ...
# Subtest: shared destination helper without a move context records no jump
ok 1877 - shared destination helper without a move context records no jump
  ---
  duration_ms: 0.76467
  ...
# Subtest: task moves carry the Depends-On line and repath stranded same-note links
ok 1878 - task moves carry the Depends-On line and repath stranded same-note links
  ---
  duration_ms: 6.22873
  ...
# Subtest: task moves keep pathless links when the target moves along
ok 1879 - task moves keep pathless links when the target moves along
  ---
  duration_ms: 1.153471
  ...
# Subtest: counted task moves discover movable tasks without wrapping or examples
ok 1880 - counted task moves discover movable tasks without wrapping or examples
  ---
  duration_ms: 0.909046
  ...
# Subtest: task move ranges preserve quoted subtrees and collapse overlapping selections
ok 1881 - task move ranges preserve quoted subtrees and collapse overlapping selections
  ---
  duration_ms: 0.568926
  ...
# Subtest: task move removal handles disjoint ranges, blank seams, and CRLF
ok 1882 - task move removal handles disjoint ranges, blank seams, and CRLF
  ---
  duration_ms: 0.35138
  ...
# Subtest: task move destinations include areas and only open projects
ok 1883 - task move destinations include areas and only open projects
  ---
  duration_ms: 0.47677
  ...
# Subtest: moves into a blocked project leave closed tagged lines alone
ok 1884 - moves into a blocked project leave closed tagged lines alone
  ---
  duration_ms: 2.086552
  ...
# Subtest: moves into a blocked project promote open prerequisites to the moved lane
ok 1885 - moves into a blocked project promote open prerequisites to the moved lane
  ---
  duration_ms: 2.125637
  ...
# Subtest: task move insertion preserves exact task and section spacing
ok 1886 - task move insertion preserves exact task and section spacing
  ---
  duration_ms: 4.154981
  ...
# Subtest: task move planning migrates identities and links across every affected note
ok 1887 - task move planning migrates identities and links across every affected note
  ---
  duration_ms: 5.494248
  ...
# Subtest: task move planning exposes a destination anchor for area destinations and counted moves
ok 1888 - task move planning exposes a destination anchor for area destinations and counted moves
  ---
  duration_ms: 1.154153
  ...
# Subtest: task move into a blocked project tags the moved task and consumes today's live Pomodoro link
ok 1889 - task move into a blocked project tags the moved task and consumes today's live Pomodoro link
  ---
  duration_ms: 4.419336
  ...
# Subtest: task move out of a blocked project recovers through the shared gate and writes the unblocked mark
ok 1890 - task move out of a blocked project recovers through the shared gate and writes the unblocked mark
  ---
  duration_ms: 4.424295
  ...
# Subtest: move promotion walks through a ^prj target without raising it
ok 1891 - move promotion walks through a ^prj target without raising it
  ---
  duration_ms: 2.42056
  ...
# Subtest: move promotion walks through a [?] ^prj to its open prerequisite
ok 1892 - move promotion walks through a [?] ^prj to its open prerequisite
  ---
  duration_ms: 1.286386
  ...
# Subtest: move promotion uses each open task's own lane, not the strongest moved lane
ok 1893 - move promotion uses each open task's own lane, not the strongest moved lane
  ---
  duration_ms: 1.493812
  ...
# Subtest: move promotion skips Depends-On lines of closed tasks
ok 1894 - move promotion skips Depends-On lines of closed tasks
  ---
  duration_ms: 0.849592
  ...
# Subtest: task move planning rejects destination collisions and malformed identities
ok 1895 - task move planning rejects destination collisions and malformed identities
  ---
  duration_ms: 0.606508
  ...
# Subtest: resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
ok 1896 - resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
  ---
  duration_ms: 0.678936
  ...
# Subtest: focusTaskMoveDestination opens the destination file and anchors the cursor
ok 1897 - focusTaskMoveDestination opens the destination file and anchors the cursor
  ---
  duration_ms: 3.291462
  ...
# Subtest: focusTaskMoveDestination returns false without moving the cursor when the open fails
ok 1898 - focusTaskMoveDestination returns false without moving the cursor when the open fails
  ---
  duration_ms: 0.283922
  ...
# Subtest: focusTaskMoveDestination re-anchors by block ID when the destination content drifted
ok 1899 - focusTaskMoveDestination re-anchors by block ID when the destination content drifted
  ---
  duration_ms: 0.252091
  ...
# Subtest: physical task move chord declines auto-repeat and consumes Vim normal input once
ok 1900 - physical task move chord declines auto-repeat and consumes Vim normal input once
  ---
  duration_ms: 0.863879
  ...
# Subtest: counted task move dispatch keeps its count through cold async destinations
ok 1901 - counted task move dispatch keeps its count through cold async destinations
  ---
  duration_ms: 12.744829
  ...
# Subtest: counted task move dispatch with warm async destinations opens one counted picker
ok 1902 - counted task move dispatch with warm async destinations opens one counted picker
  ---
  duration_ms: 5.835529
  ...
# Subtest: bare task move command ignores stale Vim count outside normal mode
ok 1903 - bare task move command ignores stale Vim count outside normal mode
  ---
  duration_ms: 1.170174
  ...
# Subtest: bare task move command opens one uncounted target in Vim normal mode
ok 1904 - bare task move command opens one uncounted target in Vim normal mode
  ---
  duration_ms: 0.447715
  ...
# Subtest: already handled task move event leaves pending Vim state alone
ok 1905 - already handled task move event leaves pending Vim state alone
  ---
  duration_ms: 0.207786
  ...
# Subtest: counted task move command dispatch counts Pomodoro sub-bullets once
ok 1906 - counted task move command dispatch counts Pomodoro sub-bullets once
  ---
  duration_ms: 2.901249
  ...
# Subtest: physical transclusion toggle owns bare and counted Vim normal input
ok 1907 - physical transclusion toggle owns bare and counted Vim normal input
  ---
  duration_ms: 1.35653
  ...
# Subtest: runtime task move writes destination before source and rolls back source failures
ok 1908 - runtime task move writes destination before source and rolls back source failures
  ---
  duration_ms: 2.288528
  ...
# Subtest: runtime task move groups open-editor source and destination changes
ok 1909 - runtime task move groups open-editor source and destination changes
  ---
  duration_ms: 1.46177
  ...
# Subtest: runtime task move guards destination, auxiliary, and rollback failures
ok 1910 - runtime task move guards destination, auxiliary, and rollback failures
  ---
  duration_ms: 2.455598
  ...
# Subtest: task move insertion separates the section's first task from preamble and placeholders
ok 1911 - task move insertion separates the section's first task from preamble and placeholders
  ---
  duration_ms: 0.506236
  ...
# Subtest: task move insertion keeps populated sections compact and second moves stable
ok 1912 - task move insertion keeps populated sections compact and second moves stable
  ---
  duration_ms: 0.234337
  ...
# Subtest: task move planning separates a counted move into a count-only section
ok 1913 - task move planning separates a counted move into a count-only section
  ---
  duration_ms: 0.579376
  ...
# Subtest: runtime counted move into a count-only section focuses the first moved task
ok 1914 - runtime counted move into a count-only section focuses the first moved task
  ---
  duration_ms: 1.223456
  ...
# Subtest: unblocked model returns null when there is nothing to show
ok 1915 - unblocked model returns null when there is nothing to show
  ---
  duration_ms: 1.430731
  ...
# Subtest: unblocked card renders a single linked row with receipt and chips
ok 1916 - unblocked card renders a single linked row with receipt and chips
  ---
  duration_ms: 1.652534
  ...
# Subtest: unblocked card renders several linked rows with one entry
ok 1917 - unblocked card renders several linked rows with one entry
  ---
  duration_ms: 0.324199
  ...
# Subtest: unblocked card renders a created continuation with next up
ok 1918 - unblocked card renders a created continuation with next up
  ---
  duration_ms: 0.406445
  ...
# Subtest: unblocked card renders recovered-only and still-blocked rows
ok 1919 - unblocked card renders recovered-only and still-blocked rows
  ---
  duration_ms: 0.68625
  ...
# Subtest: current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
ok 1920 - current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
  ---
  duration_ms: 0.918754
  ...
# Subtest: project pull-in rows label empty projects and preserve project blocking reasons
ok 1921 - project pull-in rows label empty projects and preserve project blocking reasons
  ---
  duration_ms: 1.190112
  ...
# Subtest: unblocked card caps visible rows with +N more
ok 1922 - unblocked card caps visible rows with +N more
  ---
  duration_ms: 0.468124
  ...
# Subtest: unblocked card renders the breaker variant
ok 1923 - unblocked card renders the breaker variant
  ---
  duration_ms: 0.608922
  ...
# Subtest: unblocked card renders the failure variant
ok 1924 - unblocked card renders the failure variant
  ---
  duration_ms: 0.5921
  ...
# Subtest: unblocked rows open their task without dismissing the notice
ok 1925 - unblocked rows open their task without dismissing the notice
  ---
  duration_ms: 1.281416
  ...
# Subtest: unblocked row without a block id opens the note path
ok 1926 - unblocked row without a block id opens the note path
  ---
  duration_ms: 0.27194
  ...
# Subtest: unblocked card omits the plan chip when daily content is null
ok 1927 - unblocked card omits the plan chip when daily content is null
  ---
  duration_ms: 0.265487
  ...
# Subtest: unblocked notice shows one card with duration through showNotice
ok 1928 - unblocked notice shows one card with duration through showNotice
  ---
  duration_ms: 0.427145
  ...
# Subtest: unblocked notice falls back to plain text without a DOM
ok 1929 - unblocked notice falls back to plain text without a DOM
  ---
  duration_ms: 0.164605
  ...
# Subtest: unblocked text truncates to 48 characters with an ellipsis
ok 1930 - unblocked text truncates to 48 characters with an ellipsis
  ---
  duration_ms: 0.153764
  ...
# Subtest: nav api exposes additive notice v1 and keeps version 3
ok 1931 - nav api exposes additive notice v1 and keeps version 3
  ---
  duration_ms: 0.384855
  ...
# Subtest: unblocked stylesheet scopes notice overrides and uses task tokens
ok 1932 - unblocked stylesheet scopes notice overrides and uses task tokens
  ---
  duration_ms: 0.596569
  ...
# Subtest: physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
ok 1933 - physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
  ---
  duration_ms: 2.345708
  ...
# Subtest: open-task command ids omit repeat so the shared route resolves the pending Vim count
ok 1934 - open-task command ids omit repeat so the shared route resolves the pending Vim count
  ---
  duration_ms: 1.212354
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
ok 1935 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
  ---
  duration_ms: 5.073985
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
ok 1936 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
  ---
  duration_ms: 0.610947
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
ok 1937 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
  ---
  duration_ms: 1.103217
  ...
# Subtest: dispatch guard applies a command-route Vim count when the capture route fires second
ok 1938 - dispatch guard applies a command-route Vim count when the capture route fires second
  ---
  duration_ms: 0.924455
  ...
# Subtest: dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
ok 1939 - dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
  ---
  duration_ms: 0.687693
  ...
# Subtest: command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
ok 1940 - command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
  ---
  duration_ms: 0.62368
  ...
# Subtest: command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
ok 1941 - command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
  ---
  duration_ms: 2.231519
  ...
# Subtest: command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
ok 1942 - command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
  ---
  duration_ms: 0.998506
  ...
# Subtest: explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
ok 1943 - explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
  ---
  duration_ms: 0.589184
  ...
# Subtest: getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
ok 1944 - getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
  ---
  duration_ms: 0.173762
  ...
# Subtest: physical counted property chord consumes only explicit normal-mode Vim counts
ok 1945 - physical counted property chord consumes only explicit normal-mode Vim counts
  ---
  duration_ms: 0.53406
  ...
# Subtest: physical counted Ctrl+Shift+B opens the Depends on row; KeyP options stay unchanged
ok 1946 - physical counted Ctrl+Shift+B opens the Depends on row; KeyP options stay unchanged
  ---
  duration_ms: 0.407357
  ...
# Subtest: task-card-gate arms only on open inbox tasks
ok 1947 - task-card-gate arms only on open inbox tasks
  ---
  duration_ms: 3.889895
  ...
# Subtest: task-card-gate header shows the Inbox chip only when armed
ok 1948 - task-card-gate header shows the Inbox chip only when armed
  ---
  duration_ms: 5.393066
  ...
# Subtest: task-card-gate priority: cancel writes nothing
ok 1949 - task-card-gate priority: cancel writes nothing
  ---
  duration_ms: 1.10017
  ...
# Subtest: task-card-gate priority: stay runs today's write
ok 1950 - task-card-gate priority: stay runs today's write
  ---
  duration_ms: 0.249957
  ...
# Subtest: task-card-gate priority: move writes then moves
ok 1951 - task-card-gate priority: move writes then moves
  ---
  duration_ms: 0.596859
  ...
# Subtest: task-card-gate scheduled: cancel writes nothing
ok 1952 - task-card-gate scheduled: cancel writes nothing
  ---
  duration_ms: 0.158552
  ...
# Subtest: task-card-gate scheduled: stay runs today's write
ok 1953 - task-card-gate scheduled: stay runs today's write
  ---
  duration_ms: 0.226472
  ...
# Subtest: task-card-gate scheduled: move writes then moves
ok 1954 - task-card-gate scheduled: move writes then moves
  ---
  duration_ms: 0.181928
  ...
# Subtest: task-card-gate generic-property: cancel writes nothing
ok 1955 - task-card-gate generic-property: cancel writes nothing
  ---
  duration_ms: 0.376699
  ...
# Subtest: task-card-gate generic-property: stay runs today's write
ok 1956 - task-card-gate generic-property: stay runs today's write
  ---
  duration_ms: 0.435872
  ...
# Subtest: task-card-gate generic-property: move writes then moves
ok 1957 - task-card-gate generic-property: move writes then moves
  ---
  duration_ms: 0.306405
  ...
# Subtest: task-card-gate refresh-interval: cancel writes nothing
ok 1958 - task-card-gate refresh-interval: cancel writes nothing
  ---
  duration_ms: 0.181827
  ...
# Subtest: task-card-gate refresh-interval: stay runs today's write
ok 1959 - task-card-gate refresh-interval: stay runs today's write
  ---
  duration_ms: 0.234137
  ...
# Subtest: task-card-gate refresh-interval: move writes then moves
ok 1960 - task-card-gate refresh-interval: move writes then moves
  ---
  duration_ms: 0.166888
  ...
# Subtest: task-card-gate refresh-custom: cancel writes nothing
ok 1961 - task-card-gate refresh-custom: cancel writes nothing
  ---
  duration_ms: 0.10511
  ...
# Subtest: task-card-gate refresh-custom: stay runs today's write
ok 1962 - task-card-gate refresh-custom: stay runs today's write
  ---
  duration_ms: 0.103808
  ...
# Subtest: task-card-gate refresh-custom: move writes then moves
ok 1963 - task-card-gate refresh-custom: move writes then moves
  ---
  duration_ms: 0.321463
  ...
# Subtest: task-card-gate clear-priority: cancel writes nothing
ok 1964 - task-card-gate clear-priority: cancel writes nothing
  ---
  duration_ms: 0.143764
  ...
# Subtest: task-card-gate clear-priority: stay runs today's write
ok 1965 - task-card-gate clear-priority: stay runs today's write
  ---
  duration_ms: 0.108868
  ...
# Subtest: task-card-gate clear-priority: move writes then moves
ok 1966 - task-card-gate clear-priority: move writes then moves
  ---
  duration_ms: 0.135789
  ...
# Subtest: task-card-gate recommended-roll: cancel writes nothing
ok 1967 - task-card-gate recommended-roll: cancel writes nothing
  ---
  duration_ms: 0.090853
  ...
# Subtest: task-card-gate recommended-roll: stay runs today's write
ok 1968 - task-card-gate recommended-roll: stay runs today's write
  ---
  duration_ms: 0.095512
  ...
# Subtest: task-card-gate recommended-roll: move writes then moves
ok 1969 - task-card-gate recommended-roll: move writes then moves
  ---
  duration_ms: 0.119268
  ...
# Subtest: task-card-gate recommended-decay: cancel writes nothing
ok 1970 - task-card-gate recommended-decay: cancel writes nothing
  ---
  duration_ms: 0.110601
  ...
# Subtest: task-card-gate recommended-decay: stay runs today's write
ok 1971 - task-card-gate recommended-decay: stay runs today's write
  ---
  duration_ms: 0.087657
  ...
# Subtest: task-card-gate recommended-decay: move writes then moves
ok 1972 - task-card-gate recommended-decay: move writes then moves
  ---
  duration_ms: 0.110782
  ...
# Subtest: task-card-gate counted-roll: cancel writes nothing
ok 1973 - task-card-gate counted-roll: cancel writes nothing
  ---
  duration_ms: 0.136691
  ...
# Subtest: task-card-gate counted-roll: stay runs today's write
ok 1974 - task-card-gate counted-roll: stay runs today's write
  ---
  duration_ms: 0.100171
  ...
# Subtest: task-card-gate counted-roll: move writes then moves
ok 1975 - task-card-gate counted-roll: move writes then moves
  ---
  duration_ms: 0.254256
  ...
# Subtest: task-card-gate lane-toggle: cancel writes nothing
ok 1976 - task-card-gate lane-toggle: cancel writes nothing
  ---
  duration_ms: 0.099059
  ...
# Subtest: task-card-gate lane-toggle: stay runs today's write
ok 1977 - task-card-gate lane-toggle: stay runs today's write
  ---
  duration_ms: 0.100672
  ...
# Subtest: task-card-gate lane-toggle: move writes then moves
ok 1978 - task-card-gate lane-toggle: move writes then moves
  ---
  duration_ms: 0.15733
  ...
# Subtest: task-card-gate dependency-single: cancel writes nothing
ok 1979 - task-card-gate dependency-single: cancel writes nothing
  ---
  duration_ms: 0.103959
  ...
# Subtest: task-card-gate dependency-single: stay runs today's write
ok 1980 - task-card-gate dependency-single: stay runs today's write
  ---
  duration_ms: 0.107845
  ...
# Subtest: task-card-gate dependency-single: move writes then moves
ok 1981 - task-card-gate dependency-single: move writes then moves
  ---
  duration_ms: 0.376278
  ...
# Subtest: task-card-gate dependency-marked: cancel writes nothing
ok 1982 - task-card-gate dependency-marked: cancel writes nothing
  ---
  duration_ms: 0.090142
  ...
# Subtest: task-card-gate dependency-marked: stay runs today's write
ok 1983 - task-card-gate dependency-marked: stay runs today's write
  ---
  duration_ms: 0.09455
  ...
# Subtest: task-card-gate dependency-marked: move writes then moves
ok 1984 - task-card-gate dependency-marked: move writes then moves
  ---
  duration_ms: 0.103678
  ...
# Subtest: task-card-gate dependency-vault: cancel writes nothing
ok 1985 - task-card-gate dependency-vault: cancel writes nothing
  ---
  duration_ms: 0.086114
  ...
# Subtest: task-card-gate dependency-vault: stay runs today's write
ok 1986 - task-card-gate dependency-vault: stay runs today's write
  ---
  duration_ms: 0.088459
  ...
# Subtest: task-card-gate dependency-vault: move writes then moves
ok 1987 - task-card-gate dependency-vault: move writes then moves
  ---
  duration_ms: 0.106994
  ...
# Subtest: task-card-gate dependency-counted: cancel writes nothing
ok 1988 - task-card-gate dependency-counted: cancel writes nothing
  ---
  duration_ms: 0.08914
  ...
# Subtest: task-card-gate dependency-counted: stay runs today's write
ok 1989 - task-card-gate dependency-counted: stay runs today's write
  ---
  duration_ms: 0.087146
  ...
# Subtest: task-card-gate dependency-counted: move writes then moves
ok 1990 - task-card-gate dependency-counted: move writes then moves
  ---
  duration_ms: 0.108807
  ...
# Subtest: task-card-gate negative rows never prompt
ok 1991 - task-card-gate negative rows never prompt
  ---
  duration_ms: 0.667905
  ...
# Subtest: task-card-gate counted sessions capture N targets
ok 1992 - task-card-gate counted sessions capture N targets
  ---
  duration_ms: 0.26153
  ...
# Subtest: task-card-gate walk: move advances once with Moved first
ok 1993 - task-card-gate walk: move advances once with Moved first
  ---
  duration_ms: 0.202376
  ...
# Subtest: task-card-gate walk: move failure falls back to card with partial
ok 1994 - task-card-gate walk: move failure falls back to card with partial
  ---
  duration_ms: 0.298921
  ...
# Subtest: task-card-gate walk: exactly one settle per origin
ok 1995 - task-card-gate walk: exactly one settle per origin
  ---
  duration_ms: 21.849087
  ...
# Subtest: task-card-gate route outcome resolves like lane and link-today
ok 1996 - task-card-gate route outcome resolves like lane and link-today
  ---
  duration_ms: 0.374886
  ...
# Subtest: inbox classifier covers the inbox contract
ok 1997 - inbox classifier covers the inbox contract
  ---
  duration_ms: 1.59776
  ...
# Subtest: isInboxNotePath matches the inbox contract through the vault
ok 1998 - isInboxNotePath matches the inbox contract through the vault
  ---
  duration_ms: 1.058882
  ...
# Subtest: isInboxNotePath is false without an inbox note and never throws
ok 1999 - isInboxNotePath is false without an inbox note and never throws
  ---
  duration_ms: 0.16234
  ...
# Subtest: route destinations drop every inbox note, the source, and templates
ok 2000 - route destinations drop every inbox note, the source, and templates
  ---
  duration_ms: 0.72787
  ...
# Subtest: route preflight accepts a live area destination
ok 2001 - route preflight accepts a live area destination
  ---
  duration_ms: 3.864126
  ...
# Subtest: route preflight refuses stale and colliding destinations
ok 2002 - route preflight refuses stale and colliding destinations
  ---
  duration_ms: 2.718038
  ...
# Subtest: route picker resolves move, stay, cancel, and close exactly once
ok 2003 - route picker resolves move, stay, cancel, and close exactly once
  ---
  duration_ms: 3.302134
  ...
# Subtest: route picker footer names the move, the hatch, and the way back
ok 2004 - route picker footer names the move, the hatch, and the way back
  ---
  duration_ms: 0.48724
  ...
# Subtest: route picker preflight refusal keeps the picker open with a notice
ok 2005 - route picker preflight refusal keeps the picker open with a notice
  ---
  duration_ms: 6.651687
  ...
# Subtest: route picker honors the shared move-picker guard
ok 2006 - route picker honors the shared move-picker guard
  ---
  duration_ms: 2.096012
  ...
# Subtest: promptInboxRoute moves, stays, and cancels with suspend pairing
ok 2007 - promptInboxRoute moves, stays, and cancels with suspend pairing
  ---
  duration_ms: 2.417064
  ...
# Subtest: commitInboxRoute moves the verified task with its children
ok 2008 - commitInboxRoute moves the verified task with its children
  ---
  duration_ms: 2.844459
  ...
# Subtest: commitInboxRoute into a blocked project tags the moved task
ok 2009 - commitInboxRoute into a blocked project tags the moved task
  ---
  duration_ms: 1.708531
  ...
# Subtest: commitInboxRoute moves a counted run and refuses on identity drift
ok 2010 - commitInboxRoute moves a counted run and refuses on identity drift
  ---
  duration_ms: 1.24699
  ...
# Subtest: reviewOutcomeResolves treats route like lane and link-today
ok 2011 - reviewOutcomeResolves treats route like lane and link-today
  ---
  duration_ms: 0.237704
  ...
# Subtest: nav api inboxRoute v1 delegates, shapes, and never throws
ok 2012 - nav api inboxRoute v1 delegates, shapes, and never throws
  ---
  duration_ms: 1.368702
  ...
# Subtest: history records ordered locations with file identity and dedupes adjacent repeats
ok 2013 - history records ordered locations with file identity and dedupes adjacent repeats
  ---
  duration_ms: 1.325971
  ...
# Subtest: transition records origin then destination and truncates forward only on success
ok 2014 - transition records origin then destination and truncates forward only on success
  ---
  duration_ms: 0.755201
  ...
# Subtest: history retains at most 100 locations and refreshes the live tip
ok 2015 - history retains at most 100 locations and refreshes the live tip
  ---
  duration_ms: 2.247359
  ...
# Subtest: rename updates paths and delete prunes without corrupting the index
ok 2016 - rename updates paths and delete prunes without corrupting the index
  ---
  duration_ms: 0.226483
  ...
# Subtest: bridge wraps add once, mirrors native jumps, and preserves the original call
ok 2017 - bridge wraps add once, mirrors native jumps, and preserves the original call
  ---
  duration_ms: 1.160104
  ...
# Subtest: bridge without a jump list preserves keys and emits one compatibility diagnostic
ok 2018 - bridge without a jump list preserves keys and emits one compatibility diagnostic
  ---
  duration_ms: 0.249857
  ...
# Subtest: registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
ok 2019 - registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
  ---
  duration_ms: 0.296485
  ...
# Subtest: Enter A->B round-trips with Ctrl+O and Ctrl+I
ok 2020 - Enter A->B round-trips with Ctrl+O and Ctrl+I
  ---
  duration_ms: 22.239983
  ...
# Subtest: counted Enter returns to the original cursor, not the counted link line
ok 2021 - counted Enter returns to the original cursor, not the counted link line
  ---
  duration_ms: 21.67753
  ...
# Subtest: picker choice records one jump and cancellation records none
ok 2022 - picker choice records one jump and cancellation records none
  ---
  duration_ms: 21.254463
  ...
# Subtest: stale picker origin is rejected and failed opens record nothing
ok 2023 - stale picker origin is rejected and failed opens record nothing
  ---
  duration_ms: 20.736363
  ...
# Subtest: Backspace shares the link path and no-link lines fall through
ok 2024 - Backspace shares the link path and no-link lines fall through
  ---
  duration_ms: 21.472918
  ...
# Subtest: counted traversal honors boundaries and new jumps replace the forward branch
ok 2025 - counted traversal honors boundaries and new jumps replace the forward branch
  ---
  duration_ms: 0.934284
  ...
# Subtest: ordinary motion before back is preserved for forward restore
ok 2026 - ordinary motion before back is preserved for forward restore
  ---
  duration_ms: 0.440341
  ...
# Subtest: deleted entries are skipped and heading links settle before recording
ok 2027 - deleted entries are skipped and heading links settle before recording
  ---
  duration_ms: 20.496165
  ...
# Subtest: native fallback runs with empty history and boundaries never replay natives
ok 2028 - native fallback runs with empty history and boundaries never replay natives
  ---
  duration_ms: 0.585447
  ...
# Subtest: unload restores the native add and keeps a foreign later mapping
ok 2029 - unload restores the native add and keeps a foreign later mapping
  ---
  duration_ms: 0.405464
  ...
# Subtest: exact eligibility authorizes one due-Ready ROTTEN row
ok 2030 - exact eligibility authorizes one due-Ready ROTTEN row
  ---
  duration_ms: 1.391146
  ...
# Subtest: exact eligibility authorizes a TICKLER row
ok 2031 - exact eligibility authorizes a TICKLER row
  ---
  duration_ms: 0.204099
  ...
# Subtest: exact eligibility refuses every stale-cache shape
ok 2032 - exact eligibility refuses every stale-cache shape
  ---
  duration_ms: 0.480197
  ...
# Subtest: exact eligibility refuses non-Ready and non-due rows
ok 2033 - exact eligibility refuses non-Ready and non-due rows
  ---
  duration_ms: 0.289913
  ...
# Subtest: legacy refs still match line-only while exact refuses
ok 2034 - legacy refs still match line-only while exact refuses
  ---
  duration_ms: 0.56589
  ...
# Subtest: keeps support needs namespace v5 with keepLine
ok 2035 - keeps support needs namespace v5 with keepLine
  ---
  duration_ms: 0.174854
  ...
# Subtest: decay decisions need namespace v6 with keepLine
ok 2036 - decay decisions need namespace v6 with keepLine
  ---
  duration_ms: 0.211083
  ...
# Subtest: batch forwards per-target counted decisions to the stamper
ok 2037 - batch forwards per-target counted decisions to the stamper
  ---
  duration_ms: 0.821909
  ...
# Subtest: batch keeps legacy index targets uncounted
ok 2038 - batch keeps legacy index targets uncounted
  ---
  duration_ms: 0.439168
  ...
# Subtest: a throwing stamper refuses the batch with no partial write
ok 2039 - a throwing stamper refuses the batch with no partial write
  ---
  duration_ms: 0.595667
  ...
# Subtest: parseKeepsCount reads the first valid value only
ok 2040 - parseKeepsCount reads the first valid value only
  ---
  duration_ms: 0.412317
  ...
# Subtest: countFreshStampKept measures actual increments only
ok 2041 - countFreshStampKept measures actual increments only
  ---
  duration_ms: 0.195874
  ...
# Subtest: fresh stamp notice tails kept increments without promises
ok 2042 - fresh stamp notice tails kept increments without promises
  ---
  duration_ms: 0.228266
  ...
# Subtest: duplicate source targets dedupe to one write
ok 2043 - duplicate source targets dedupe to one write
  ---
  duration_ms: 0.177559
  ...
# Subtest: single Alt+F increments an exact due-Ready ROTTEN task
ok 2044 - single Alt+F increments an exact due-Ready ROTTEN task
  ---
  duration_ms: 4.995727
  ...
# Subtest: single Alt+F preserves NEW, lane, and early tasks without counting
ok 2045 - single Alt+F preserves NEW, lane, and early tasks without counting
  ---
  duration_ms: 3.172395
  ...
# Subtest: same-day repeat stays identical and counts nothing
ok 2046 - same-day repeat stays identical and counts nothing
  ---
  duration_ms: 0.709164
  ...
# Subtest: Pending Alt+F writes its summary with the stamp in one edit
ok 2047 - Pending Alt+F writes its summary with the stamp in one edit
  ---
  duration_ms: 1.043753
  ...
# Subtest: counted Pending refresh shares one summary only with Pending targets
ok 2048 - counted Pending refresh shares one summary only with Pending targets
  ---
  duration_ms: 0.600937
  ...
# Subtest: a refusing counted target refuses before the Pending Work Log prompt
ok 2049 - a refusing counted target refuses before the Pending Work Log prompt
  ---
  duration_ms: 0.443577
  ...
# Subtest: blank Pending refresh advances; cancelled or stale prompts write nothing
ok 2050 - blank Pending refresh advances; cancelled or stale prompts write nothing
  ---
  duration_ms: 1.114197
  ...
# Subtest: stale queue match stamps uncounted and never inflates
ok 2051 - stale queue match stamps uncounted and never inflates
  ---
  duration_ms: 0.500746
  ...
# Subtest: counted Alt+F increments every exact target once
ok 2052 - counted Alt+F increments every exact target once
  ---
  duration_ms: 0.61307
  ...
# Subtest: stale editor source refuses with no write
ok 2053 - stale editor source refuses with no write
  ---
  duration_ms: 0.222074
  ...
# Subtest: single-note write lands in one editor transaction and keeps CRLF
ok 2054 - single-note write lands in one editor transaction and keeps CRLF
  ---
  duration_ms: 0.49269
  ...
# Subtest: v5 without keepLine fails without writing
ok 2055 - v5 without keepLine fails without writing
  ---
  duration_ms: 0.171568
  ...
# Subtest: throwing v5 keepLine refuses the batch with no partial write
ok 2056 - throwing v5 keepLine refuses the batch with no partial write
  ---
  duration_ms: 0.325691
  ...
# Subtest: pre-v5 ledger stamps uncounted through the old stamper
ok 2057 - pre-v5 ledger stamps uncounted through the old stamper
  ---
  duration_ms: 0.443356
  ...
# Subtest: Task Link session skips an at-limit decide target
ok 2058 - Task Link session skips an at-limit decide target
  ---
  duration_ms: 1.917871
  ...
# Subtest: Task Link refresh counts one exact target
ok 2059 - Task Link refresh counts one exact target
  ---
  duration_ms: 0.949883
  ...
# Subtest: duplicate Task Links to one target stamp and count once
ok 2060 - duplicate Task Links to one target stamp and count once
  ---
  duration_ms: 0.51352
  ...
# Subtest: counted Task Links dedupe targets and log only the Pending target
ok 2061 - counted Task Links dedupe targets and log only the Pending target
  ---
  duration_ms: 0.759771
  ...
# Subtest: multi-note stale preimage refuses with no writes
ok 2062 - multi-note stale preimage refuses with no writes
  ---
  duration_ms: 0.764409
  ...
# Subtest: multi-note write failure rolls back the first note
ok 2063 - multi-note write failure rolls back the first note
  ---
  duration_ms: 0.873127
  ...
# Subtest: one physical key through two routes stamps once
ok 2064 - one physical key through two routes stamps once
  ---
  duration_ms: 1.152059
  ...
# Subtest: Ctrl+Alt+F capture advances once and consumes a Vim prefix
ok 2065 - Ctrl+Alt+F capture advances once and consumes a Vim prefix
  ---
  duration_ms: 0.550029
  ...
# Subtest: obsolete and extra-modifier F chords stay unconsumed
ok 2066 - obsolete and extra-modifier F chords stay unconsumed
  ---
  duration_ms: 0.261068
  ...
# Subtest: live Ctrl+Alt+F double dispatch asks once on a Pending task
ok 2067 - live Ctrl+Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.614062
  ...
# Subtest: live Alt+F double dispatch asks once on a Pending task
ok 2068 - live Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.669849
  ...
# Subtest: already-handled refresh keydown leaves Vim state alone
ok 2069 - already-handled refresh keydown leaves Vim state alone
  ---
  duration_ms: 0.205984
  ...
# Subtest: collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
ok 2070 - collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
  ---
  duration_ms: 2.381296
  ...
# Subtest: getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
ok 2071 - getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
  ---
  duration_ms: 2.196021
  ...
# Subtest: getProjectBlockState reports an open external prerequisite
ok 2072 - getProjectBlockState reports an open external prerequisite
  ---
  duration_ms: 0.576981
  ...
# Subtest: getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
ok 2073 - getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
  ---
  duration_ms: 0.544279
  ...
# Subtest: getProjectBlockState scheduledValue override is the inline date, not frontmatter
ok 2074 - getProjectBlockState scheduledValue override is the inline date, not frontmatter
  ---
  duration_ms: 0.490827
  ...
# Subtest: getProjectBlockState skips internal and archive Depends-On links
ok 2075 - getProjectBlockState skips internal and archive Depends-On links
  ---
  duration_ms: 0.398671
  ...
# Subtest: getProjectBlockState is a no-op for terminal, daily, and non-project notes
ok 2076 - getProjectBlockState is a no-op for terminal, daily, and non-project notes
  ---
  duration_ms: 0.647086
  ...
# Subtest: projectLooksBlockedByPrjShortcut is the single [?] ^prj row
ok 2077 - projectLooksBlockedByPrjShortcut is the single [?] ^prj row
  ---
  duration_ms: 0.258103
  ...
# Subtest: taskHasProjectBlockedTag is token-bounded and does not match \#prj
ok 2078 - taskHasProjectBlockedTag is token-bounded and does not match \#prj
  ---
  duration_ms: 0.350349
  ...
# Subtest: setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
ok 2079 - setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
  ---
  duration_ms: 0.80669
  ...
# Subtest: reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
ok 2080 - reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
  ---
  duration_ms: 0.390065
  ...
# Subtest: reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
ok 2081 - reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
  ---
  duration_ms: 0.263453
  ...
# Subtest: reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
ok 2082 - reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
  ---
  duration_ms: 0.16753
  ...
# Subtest: ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
ok 2083 - ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
  ---
  duration_ms: 4.340174
  ...
# Subtest: recovery gate keeps a resident of a blocked project blocked after own deps close
ok 2084 - recovery gate keeps a resident of a blocked project blocked after own deps close
  ---
  duration_ms: 1.817719
  ...
# Subtest: recovery gate blocks residents on a future inline project date with no deps
ok 2085 - recovery gate blocks residents on a future inline project date with no deps
  ---
  duration_ms: 0.42464
  ...
# Subtest: planDeferredPomodoroLinkCleanup always deletes a last-child open entry
ok 2086 - planDeferredPomodoroLinkCleanup always deletes a last-child open entry
  ---
  duration_ms: 1.67096
  ...
# Subtest: TICKLER notice uses unblocked <date> when returnedBy is unblocked
ok 2087 - TICKLER notice uses unblocked <date> when returnedBy is unblocked
  ---
  duration_ms: 0.425292
  ...
# Subtest: recognition: a `^prj` parent in a project note carries its residents
ok 2088 - recognition: a `^prj` parent in a project note carries its residents
  ---
  duration_ms: 2.772742
  ...
# Subtest: recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
ok 2089 - recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
  ---
  duration_ms: 0.444278
  ...
# Subtest: add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
ok 2090 - add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
  ---
  duration_ms: 4.758944
  ...
# Subtest: add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
ok 2091 - add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
  ---
  duration_ms: 2.516775
  ...
# Subtest: guards: a same-note add to `^prj` refuses, including mixed batches
ok 2092 - guards: a same-note add to `^prj` refuses, including mixed batches
  ---
  duration_ms: 0.913203
  ...
# Subtest: guards: the stage disables same-note rows for `^prj` with `inside this project`
ok 2093 - guards: the stage disables same-note rows for `^prj` with `inside this project`
  ---
  duration_ms: 1.097925
  ...
# Subtest: guards: cycle detection includes the implicit resident edges (§13.6)
ok 2094 - guards: cycle detection includes the implicit resident edges (§13.6)
  ---
  duration_ms: 1.282789
  ...
# Subtest: removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
ok 2095 - removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
  ---
  duration_ms: 3.334946
  ...
# Subtest: removal: a resident with its own reason stays `[?]` without the tag (PDB3)
ok 2096 - removal: a resident with its own reason stays `[?]` without the tag (PDB3)
  ---
  duration_ms: 1.419981
  ...
# Subtest: removal without a registry defers to reconcile: residents keep `[?]` and the tag
ok 2097 - removal without a registry defers to reconcile: residents keep `[?]` and the tag
  ---
  duration_ms: 1.177878
  ...
# Subtest: writer: one gesture commits `^prj` and its residents in a single undo group
ok 2098 - writer: one gesture commits `^prj` and its residents in a single undo group
  ---
  duration_ms: 1.137972
  ...
# Subtest: writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
ok 2099 - writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
  ---
  duration_ms: 3.098214
  ...
# Subtest: notices: the project strings name the task, the flips, and the Pomodoro cleanup
ok 2100 - notices: the project strings name the task, the flips, and the Pomodoro cleanup
  ---
  duration_ms: 0.434039
  ...
# Subtest: mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
ok 2101 - mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
  ---
  duration_ms: 0.281447
  ...
# Subtest: api v3: removeDependencyByRef delegates removals to the single-transaction writer
ok 2102 - api v3: removeDependencyByRef delegates removals to the single-transaction writer
  ---
  duration_ms: 0.965132
  ...
# Subtest: api v3: openDependencyStageForRef opens the Depends on stage on the owning task
ok 2103 - api v3: openDependencyStageForRef opens the Depends on stage on the owning task
  ---
  duration_ms: 0.377621
  ...
# Subtest: internal links stay on the line but leave the field (PDR7)
ok 2104 - internal links stay on the line but leave the field (PDR7)
  ---
  duration_ms: 0.905809
  ...
# Subtest: removal from an unblocked ^prj never recovers own-reason residents (§13.10)
ok 2105 - removal from an unblocked ^prj never recovers own-reason residents (§13.10)
  ---
  duration_ms: 0.593172
  ...
# Subtest: resident recovery touches only tagged residents (§13.10)
ok 2106 - resident recovery touches only tagged residents (§13.10)
  ---
  duration_ms: 1.26759
  ...
# Subtest: stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
ok 2107 - stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
  ---
  duration_ms: 0.9635
  ...
# Subtest: projectDependentResidentKeys lists open residents with block ids
ok 2108 - projectDependentResidentKeys lists open residents with block ids
  ---
  duration_ms: 0.41406
  ...
# Subtest: navNoteScopeFlags marks daily notes; a missing writer stays null
ok 2109 - navNoteScopeFlags marks daily notes; a missing writer stays null
  ---
  duration_ms: 0.305674
  ...
# Subtest: reconcileBlockedScheduledTaskLine forwards scope flags to the writer
ok 2110 - reconcileBlockedScheduledTaskLine forwards scope flags to the writer
  ---
  duration_ms: 0.195694
  ...
# Subtest: parseProjectNoteFrontmatter ignores leftover scheduled keys
ok 2111 - parseProjectNoteFrontmatter ignores leftover scheduled keys
  ---
  duration_ms: 0.608411
  ...
# Subtest: formatTaskMoveProjectCountsNotice names blocked and recovered counts
ok 2112 - formatTaskMoveProjectCountsNotice names blocked and recovered counts
  ---
  duration_ms: 0.188439
  ...
# Subtest: PDS15: projectParentTarget keeps the path and drops alias and heading
ok 2113 - PDS15: projectParentTarget keeps the path and drops alias and heading
  ---
  duration_ms: 1.270716
  ...
# Subtest: PDS6: list-form, missing, and non-wikilink parents yield none
ok 2114 - PDS6: list-form, missing, and non-wikilink parents yield none
  ---
  duration_ms: 0.529691
  ...
# Subtest: PDS15: resolveProjectParentPath accepts alias, path, and heading forms
ok 2115 - PDS15: resolveProjectParentPath accepts alias, path, and heading forms
  ---
  duration_ms: 0.51882
  ...
# Subtest: PDS6: self, unresolved, and ambiguous basenames yield no parent
ok 2116 - PDS6: self, unresolved, and ambiguous basenames yield no parent
  ---
  duration_ms: 0.237123
  ...
# Subtest: buildProjectChildrenMap and descendants BFS skip cycles and cap depth
ok 2117 - buildProjectChildrenMap and descendants BFS skip cycles and cap depth
  ---
  duration_ms: 3.561308
  ...
# Subtest: PDS6: area, terminal, daily, and self-parent notes are not children
ok 2118 - PDS6: area, terminal, daily, and self-parent notes are not children
  ---
  duration_ms: 0.512779
  ...
# Subtest: PDG8: planner blocks child and grandchild ^prj and residents
ok 2119 - PDG8: planner blocks child and grandchild ^prj and residents
  ---
  duration_ms: 3.136949
  ...
# Subtest: PDG9: planner recovers tagged descendants with [unblocked::]
ok 2120 - PDG9: planner recovers tagged descendants with [unblocked::]
  ---
  duration_ms: 1.613189
  ...
# Subtest: PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
ok 2121 - PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
  ---
  duration_ms: 2.146297
  ...
# Subtest: PDG11: a tagged root re-asserts descendant tags and recovers nothing
ok 2122 - PDG11: a tagged root re-asserts descendant tags and recovers nothing
  ---
  duration_ms: 0.930105
  ...
# Subtest: tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
ok 2123 - tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
  ---
  duration_ms: 0.255027
  ...
# Subtest: tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
ok 2124 - tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
  ---
  duration_ms: 1.496948
  ...
# Subtest: tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
ok 2125 - tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
  ---
  duration_ms: 0.15718
  ...
# Subtest: tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
ok 2126 - tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
  ---
  duration_ms: 1.784035
  ...
# Subtest: PDG13: failProjectPrjInternalAdd refuses descendant targets
ok 2127 - PDG13: failProjectPrjInternalAdd refuses descendant targets
  ---
  duration_ms: 0.224508
  ...
# Subtest: PDG13: planDependencyEdit refuses a descendant add from the files map
ok 2128 - PDG13: planDependencyEdit refuses a descendant add from the files map
  ---
  duration_ms: 1.206353
  ...
# Subtest: PDG13: the stage disables descendant rows
ok 2129 - PDG13: the stage disables descendant rows
  ---
  duration_ms: 1.263692
  ...
# Subtest: reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
ok 2130 - reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
  ---
  duration_ms: 0.294993
  ...
# Subtest: tag proxy: removing the last own dep of a tagged ^prj recovers nobody
ok 2131 - tag proxy: removing the last own dep of a tagged ^prj recovers nobody
  ---
  duration_ms: 2.233773
  ...
# Subtest: PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
ok 2132 - PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
  ---
  duration_ms: 23.02958
  ...
# Subtest: PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
ok 2133 - PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
  ---
  duration_ms: 6.838104
  ...
# Subtest: PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
ok 2134 - PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
  ---
  duration_ms: 4.908389
  ...
# Subtest: PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
ok 2135 - PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
  ---
  duration_ms: 4.39504
  ...
# Subtest: PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
ok 2136 - PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
  ---
  duration_ms: 4.685393
  ...
# Subtest: PDG12: moving the project date due recovers descendants
ok 2137 - PDG12: moving the project date due recovers descendants
  ---
  duration_ms: 3.253551
  ...
# Subtest: PDG12: deleting the project date recovers descendants
ok 2138 - PDG12: deleting the project date recovers descendants
  ---
  duration_ms: 3.067355
  ...
# Subtest: PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
ok 2139 - PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
  ---
  duration_ms: 5.307471
  ...
# Subtest: PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
ok 2140 - PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
  ---
  duration_ms: 4.740019
  ...
# Subtest: Task Link Depends on writer preserves the internal-target guard on a project task
ok 2141 - Task Link Depends on writer preserves the internal-target guard on a project task
  ---
  duration_ms: 0.965272
  ...
# Subtest: api v3 removeDependencyByRef runs the recovery cascade for a linked project task
ok 2142 - api v3 removeDependencyByRef runs the recovery cascade for a linked project task
  ---
  duration_ms: 4.023179
  ...
# Subtest: counted Schedule writer cascades a future date through descendants
ok 2143 - counted Schedule writer cascades a future date through descendants
  ---
  duration_ms: 3.405061
  ...
# Subtest: counted subtree roots are ancestor-first and each descendant note is planned once
ok 2144 - counted subtree roots are ancestor-first and each descendant note is planned once
  ---
  duration_ms: 2.025166
  ...
# Subtest: Ctrl+D on the Depends on row removes the line and recovers the subtree
ok 2145 - Ctrl+D on the Depends on row removes the line and recovers the subtree
  ---
  duration_ms: 3.849237
  ...
# Subtest: a ^prj with no children reads no other note
ok 2146 - a ^prj with no children reads no other note
  ---
  duration_ms: 0.223256
  ...
# Subtest: single seeds from raw text, not display decorations
ok 2147 - single seeds from raw text, not display decorations
  ---
  duration_ms: 7.701432
  ...
# Subtest: legacy valid free wins; invalid and taken fall through
ok 2148 - legacy valid free wins; invalid and taken fall through
  ---
  duration_ms: 1.177197
  ...
# Subtest: batch reserves suffixes for two same-text tasks
ok 2149 - batch reserves suffixes for two same-text tasks
  ---
  duration_ms: 0.783466
  ...
# Subtest: counted-source, vault-single, and vault-counted seed per mode
ok 2150 - counted-source, vault-single, and vault-counted seed per mode
  ---
  duration_ms: 0.958359
  ...
# Subtest: cross-note uses the target note, never the dependent fallback
ok 2151 - cross-note uses the target note, never the dependent fallback
  ---
  duration_ms: 1.078598
  ...
# Subtest: staging writes nothing until confirmed
ok 2152 - staging writes nothing until confirmed
  ---
  duration_ms: 0.538408
  ...
# Subtest: Less often picker renders actual rows from 90 days and Escape writes nothing
ok 2153 - Less often picker renders actual rows from 90 days and Escape writes nothing
  ---
  duration_ms: 6.527742
  ...
# Subtest: Less often picker renders actual rows from 120 days and Escape writes nothing
ok 2154 - Less often picker renders actual rows from 120 days and Escape writes nothing
  ---
  duration_ms: 0.745373
  ...
# Subtest: Less often picker renders actual rows from 180 days and Escape writes nothing
ok 2155 - Less often picker renders actual rows from 180 days and Escape writes nothing
  ---
  duration_ms: 0.496197
  ...
# Subtest: renderFooter skips malformed hints and retains valid structured hints
ok 2156 - renderFooter skips malformed hints and retains valid structured hints
  ---
  duration_ms: 0.337575
  ...
# Subtest: Pending refresh modal previews the dated Work Log and confirms once
ok 2157 - Pending refresh modal previews the dated Work Log and confirms once
  ---
  duration_ms: 1.525051
  ...
# Subtest: dismissing the Pending refresh modal cancels without a summary
ok 2158 - dismissing the Pending refresh modal cancels without a summary
  ---
  duration_ms: 0.388832
  ...
# Subtest: Alt+N release from a NEXT landing advances with one composed toast
ok 2159 - Alt+N release from a NEXT landing advances with one composed toast
  ---
  duration_ms: 20.50439
  ...
# Subtest: counted Alt+N lands past every handled key in one jump
ok 2160 - counted Alt+N lands past every handled key in one jump
  ---
  duration_ms: 9.853179
  ...
# Subtest: a cancelled Alt+N release prompt stays and frees the lock
ok 2161 - a cancelled Alt+N release prompt stays and frees the lock
  ---
  duration_ms: 11.0587
  ...
# Subtest: Alt+N on a checklist landing stays with the plain notice
ok 2162 - Alt+N on a checklist landing stays with the plain notice
  ---
  duration_ms: 10.470457
  ...
# Subtest: Alt+N off a landing behaves exactly as today
ok 2163 - Alt+N off a landing behaves exactly as today
  ---
  duration_ms: 10.060424
  ...
# Subtest: Alt+N while the gesture lock is held is swallowed
ok 2164 - Alt+N while the gesture lock is held is swallowed
  ---
  duration_ms: 9.798954
  ...
# Subtest: a Task Card priority commit on NEXT advances, landing after the rich card
ok 2165 - a Task Card priority commit on NEXT advances, landing after the rich card
  ---
  duration_ms: 26.214119
  ...
# Subtest: dismissing the Task Card stays and frees the lock
ok 2166 - dismissing the Task Card stays and frees the lock
  ---
  duration_ms: 11.58794
  ...
# Subtest: a frontmatter-only project edit from the card stays
ok 2167 - a frontmatter-only project edit from the card stays
  ---
  duration_ms: 12.60469
  ...
# Subtest: a same-day priority schedule on a checklist row stays
ok 2168 - a same-day priority schedule on a checklist row stays
  ---
  duration_ms: 11.148011
  ...
# Subtest: a future schedule on a checklist row advances
ok 2169 - a future schedule on a checklist row advances
  ---
  duration_ms: 16.393311
  ...
# Subtest: a Task Card cancel on a checklist row advances with the cancel card first
ok 2170 - a Task Card cancel on a checklist row advances with the cancel card first
  ---
  duration_ms: 13.689873
  ...
# Subtest: Ctrl+Shift+M from a landing follows the task and never advances
ok 2171 - Ctrl+Shift+M from a landing follows the task and never advances
  ---
  duration_ms: 16.280757
  ...
# Subtest: Ctrl+Shift+M from a checklist landing keeps the destination focus
ok 2172 - Ctrl+Shift+M from a checklist landing keeps the destination focus
  ---
  duration_ms: 10.543937
  ...
# Subtest: ]s after a landed move resumes at the successor despite the line shift
ok 2173 - ]s after a landed move resumes at the successor despite the line shift
  ---
  duration_ms: 35.039185
  ...
# Subtest: [s after a landed move resumes at the predecessor
ok 2174 - [s after a landed move resumes at the predecessor
  ---
  duration_ms: 15.48519
  ...
# Subtest: a counted move from a landing resumes past every moved target
ok 2175 - a counted move from a landing resumes past every moved target
  ---
  duration_ms: 11.154983
  ...
# Subtest: counted Ctrl+Shift+M command dispatch preserves a landed move count
ok 2176 - counted Ctrl+Shift+M command dispatch preserves a landed move count
  ---
  duration_ms: 21.380753
  ...
# Subtest: a stale landing is not parked
ok 2177 - a stale landing is not parked
  ---
  duration_ms: 10.447382
  ...
# Subtest: Ctrl+Shift+M while the gesture lock is held is swallowed
ok 2178 - Ctrl+Shift+M while the gesture lock is held is swallowed
  ---
  duration_ms: 0.45596
  ...
# Subtest: dismissing the move picker stays and frees the lock
ok 2179 - dismissing the move picker stays and frees the lock
  ---
  duration_ms: 8.893025
  ...
# Subtest: Ctrl+Shift+M off a landing behaves exactly as today
ok 2180 - Ctrl+Shift+M off a landing behaves exactly as today
  ---
  duration_ms: 9.849171
  ...
# Subtest: answer, move, answer stays in queue order past an accumulator alias
ok 2181 - answer, move, answer stays in queue order past an accumulator alias
  ---
  duration_ms: 3.681266
  ...
# Subtest: a move park ignores a stale accumulator alias
ok 2182 - a move park ignores a stale accumulator alias
  ---
  duration_ms: 0.470789
  ...
# Subtest: a re-indexed origin still advances from the landed row
ok 2183 - a re-indexed origin still advances from the landed row
  ---
  duration_ms: 1.009567
  ...
# Subtest: a landed move park clears the current review task
ok 2184 - a landed move park clears the current review task
  ---
  duration_ms: 0.356731
  ...
# Subtest: predicate: reviewOutcomeResolves across tiers and kinds
ok 2185 - predicate: reviewOutcomeResolves across tiers and kinds
  ---
  duration_ms: 2.241338
  ...
# Subtest: findReviewResumeIndex identifies rows by path and text
ok 2186 - findReviewResumeIndex identifies rows by path and text
  ---
  duration_ms: 0.434891
  ...
# Subtest: buildReviewMoveAnchor parks text-identified resume neighbours
ok 2187 - buildReviewMoveAnchor parks text-identified resume neighbours
  ---
  duration_ms: 0.846425
  ...
# Subtest: planReviewJump with a move anchor resumes at the walk neighbour
ok 2188 - planReviewJump with a move anchor resumes at the walk neighbour
  ---
  duration_ms: 1.555931
  ...
# Subtest: capture: null off a landing
ok 2189 - capture: null off a landing
  ---
  duration_ms: 4.724428
  ...
# Subtest: capture: frozen origin shape, BUSY while locked, expiry
ok 2190 - capture: frozen origin shape, BUSY while locked, expiry
  ---
  duration_ms: 0.777764
  ...
# Subtest: successor picker keeps a captured completion locked through selection and one walk toast
ok 2191 - successor picker keeps a captured completion locked through selection and one walk toast
  ---
  duration_ms: 18.496587
  ...
# Subtest: continue: refuses stale origins, showing the notice once
ok 2192 - continue: refuses stale origins, showing the notice once
  ---
  duration_ms: 7.745725
  ...
# Subtest: continue: stays on null and non-resolving outcomes
ok 2193 - continue: stays on null and non-resolving outcomes
  ---
  duration_ms: 1.658736
  ...
# Subtest: continue: stays for lane answers and mixed-version completes on checklist rows
ok 2194 - continue: stays for lane answers and mixed-version completes on checklist rows
  ---
  duration_ms: 3.345786
  ...
# Subtest: continue: a resolving lane answer advances exactly once with one composed toast
ok 2195 - continue: a resolving lane answer advances exactly once with one composed toast
  ---
  duration_ms: 1.367992
  ...
# Subtest: continue: counted handled refs land past every handled key in one jump
ok 2196 - continue: counted handled refs land past every handled key in one jump
  ---
  duration_ms: 2.119296
  ...
# Subtest: continue: wrap is announced and the empty queue composes the empty notice
ok 2197 - continue: wrap is announced and the empty queue composes the empty notice
  ---
  duration_ms: 4.364721
  ...
# Subtest: continue: anchor-only planning survives cursor drift and lagging queues
ok 2198 - continue: anchor-only planning survives cursor drift and lagging queues
  ---
  duration_ms: 1.345137
  ...
# Subtest: continue: POST origins never wrap
ok 2199 - continue: POST origins never wrap
  ---
  duration_ms: 3.107862
  ...
# Subtest: complete: the last lane row before POST stays with the next-step toast
ok 2200 - complete: the last lane row before POST stays with the next-step toast
  ---
  duration_ms: 1.984849
  ...
# Subtest: complete: a wrap onto a skipped PRE row stays
ok 2201 - complete: a wrap onto a skipped PRE row stays
  ---
  duration_ms: 2.061575
  ...
# Subtest: complete: a step into ROTTEN shows the boundary line
ok 2202 - complete: a step into ROTTEN shows the boundary line
  ---
  duration_ms: 2.282446
  ...
# Subtest: busy: walk keys, refresh, claim, and capture are swallowed in the settle window
ok 2203 - busy: walk keys, refresh, claim, and capture are swallowed in the settle window
  ---
  duration_ms: 2.558113
  ...
# Subtest: advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
ok 2204 - advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
  ---
  duration_ms: 3.240787
  ...
# Subtest: advance: decay choices advance except reword, with no preamble of their own
ok 2205 - advance: decay choices advance except reword, with no preamble of their own
  ---
  duration_ms: 0.604083
  ...
# Subtest: jump history: same-note and cross-note auto-advances record, and <C-o> returns
ok 2206 - jump history: same-note and cross-note auto-advances record, and <C-o> returns
  ---
  duration_ms: 7.482442
  ...
# Subtest: jump history: a manual ]s also records its landing
ok 2207 - jump history: a manual ]s also records its landing
  ---
  duration_ms: 0.74912
  ...
# Subtest: api: reviewWalk v3 is frozen with version 1, degrades null, never throws
ok 2208 - api: reviewWalk v3 is frozen with version 1, degrades null, never throws
  ---
  duration_ms: 1.682262
  ...
# Subtest: walk identity: a stale accumulator key never moves the anchor
ok 2209 - walk identity: a stale accumulator key never moves the anchor
  ---
  duration_ms: 0.265637
  ...
# Subtest: walk identity: a lagging answered row stays excluded
ok 2210 - walk identity: a lagging answered row stays excluded
  ---
  duration_ms: 0.136681
  ...
# Subtest: walk identity: a line-shifting answer lands on the true successor by text
ok 2211 - walk identity: a line-shifting answer lands on the true successor by text
  ---
  duration_ms: 0.242533
  ...
# Subtest: walk identity: legacy anchors without text resolve as before
ok 2212 - walk identity: legacy anchors without text resolve as before
  ---
  duration_ms: 0.233165
  ...
# Subtest: walk identity: matchFreshStampRefs prefers text over line
ok 2213 - walk identity: matchFreshStampRefs prefers text over line
  ---
  duration_ms: 0.121201
  ...
# Subtest: walk identity: collectReviewAnswerKeys separates position from exclusion
ok 2214 - walk identity: collectReviewAnswerKeys separates position from exclusion
  ---
  duration_ms: 0.381919
  ...
# Subtest: return: planReviewWalkReturn pure decisions
ok 2215 - return: planReviewWalkReturn pure decisions
  ---
  duration_ms: 0.258523
  ...
# Subtest: return: same-note ]s returns then steps, both directions
ok 2216 - return: same-note ]s returns then steps, both directions
  ---
  duration_ms: 1.071104
  ...
# Subtest: return: a different due row returns instead of stepping from there
ok 2217 - return: a different due row returns instead of stepping from there
  ---
  duration_ms: 0.457814
  ...
# Subtest: return: cross-note return re-arms and records <C-o>
ok 2218 - return: cross-note return re-arms and records <C-o>
  ---
  duration_ms: 2.831564
  ...
# Subtest: return: a count is consumed and ignored
ok 2219 - return: a count is consumed and ignored
  ---
  duration_ms: 0.441062
  ...
# Subtest: return: endpoints never return
ok 2220 - return: endpoints never return
  ---
  duration_ms: 0.672243
  ...
# Subtest: return: its own stamp ends it
ok 2221 - return: its own stamp ends it
  ---
  duration_ms: 0.944132
  ...
# Subtest: return: a stamp elsewhere does not end it
ok 2222 - return: a stamp elsewhere does not end it
  ---
  duration_ms: 0.689286
  ...
# Subtest: return: answers move the current task, a stopped Ctrl+Enter clears it
ok 2223 - return: answers move the current task, a stopped Ctrl+Enter clears it
  ---
  duration_ms: 3.360726
  ...
# Subtest: return: a stale landing falls through in the same press
ok 2224 - return: a stale landing falls through in the same press
  ---
  duration_ms: 0.283661
  ...
# Subtest: return: a day change never returns
ok 2225 - return: a day change never returns
  ---
  duration_ms: 0.377801
  ...
# Subtest: predicate: reviewOutcomeResolves for the RECURRING resolution table
ok 2226 - predicate: reviewOutcomeResolves for the RECURRING resolution table
  ---
  duration_ms: 0.467783
  ...
# Subtest: recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
ok 2227 - recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
  ---
  duration_ms: 0.185835
  ...
# Subtest: return: a RECURRING landing rearms the current-task return
ok 2228 - return: a RECURRING landing rearms the current-task return
  ---
  duration_ms: 0.279844
  ...
# Subtest: review answer outcome vectors map to the schema vocabulary
ok 2229 - review answer outcome vectors map to the schema vocabulary
  ---
  duration_ms: 1.174222
  ...
# Subtest: event builder uses the walk row key and its tier, once per distinct key
ok 2230 - event builder uses the walk row key and its tier, once per distinct key
  ---
  duration_ms: 1.003326
  ...
# Subtest: journal appends are queued and failures retain events without failing answers
ok 2231 - journal appends are queued and failures retain events without failing answers
  ---
  duration_ms: 4.744357
  ...
# Subtest: card after-line outcomes map done, drop, defer, sequence, and card
ok 2232 - card after-line outcomes map done, drop, defer, sequence, and card
  ---
  duration_ms: 1.005068
  ...
# Subtest: journal events carry plugin@manifest version with a 2.x fallback
ok 2233 - journal events carry plugin@manifest version with a 2.x fallback
  ---
  duration_ms: 1.056737
  ...
# Subtest: write failures show one notice per burst and a recovery notice
ok 2234 - write failures show one notice per burst and a recovery notice
  ---
  duration_ms: 1.004227
  ...
# Subtest: missing api.stats shows one session notice and later delivers retained events
ok 2235 - missing api.stats shows one session notice and later delivers retained events
  ---
  duration_ms: 1.357341
  ...
# Subtest: validation rejects drop the event and continue the drain
ok 2236 - validation rejects drop the event and continue the drain
  ---
  duration_ms: 0.88518
  ...
# Subtest: pending journal events cap at 500 and warn once per burst
ok 2237 - pending journal events cap at 500 and warn once per burst
  ---
  duration_ms: 2.252711
  ...
# Subtest: decay config defaults to enabled with one roll per level
ok 2238 - decay config defaults to enabled with one roll per level
  ---
  duration_ms: 2.725122
  ...
# Subtest: decay:false disables decay and level rolls are accepted but ignored
ok 2239 - decay:false disables decay and level rolls are accepted but ignored
  ---
  duration_ms: 0.507709
  ...
# Subtest: decay.rolls sets the limit and levels[].rolls overrides it
ok 2240 - decay.rolls sets the limit and levels[].rolls overrides it
  ---
  duration_ms: 0.219589
  ...
# Subtest: decay config rejects bad rolls, unknown keys and non-priority use
ok 2241 - decay config rejects bad rolls, unknown keys and non-priority use
  ---
  duration_ms: 0.45564
  ...
# Subtest: classifyScheduleLogRollReason sorts automatic heads from deliberate ones
ok 2242 - classifyScheduleLogRollReason sorts automatic heads from deliberate ones
  ---
  duration_ms: 0.60267
  ...
# Subtest: conformance vectors 1-10: streaks at P2 with the default limit
ok 2243 - conformance vectors 1-10: streaks at P2 with the default limit
  ---
  duration_ms: 2.437533
  ...
# Subtest: conformance vectors 11-15: custom limits, disabled decay and edges
ok 2244 - conformance vectors 11-15: custom limits, disabled decay and edges
  ---
  duration_ms: 0.713372
  ...
# Subtest: the streak reader follows log grammar: legacy labels, nesting and stops
ok 2245 - the streak reader follows log grammar: legacy labels, nesting and stops
  ---
  duration_ms: 0.427857
  ...
# Subtest: rollPriorityRecommendationDate avoids the current date when the window has room
ok 2246 - rollPriorityRecommendationDate avoids the current date when the window has room
  ---
  duration_ms: 0.585588
  ...
# Subtest: decay and cancel reason formatters use the exact ladder copy
ok 2247 - decay and cancel reason formatters use the exact ladder copy
  ---
  duration_ms: 0.441052
  ...
# Subtest: the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
ok 2248 - the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
  ---
  duration_ms: 0.336002
  ...
# Subtest: the planner returns null without a configured priority
ok 2249 - the planner returns null without a configured priority
  ---
  duration_ms: 0.14153
  ...
# Subtest: buildPriorityRollPreviewModel carries the row copy for every kind
ok 2250 - buildPriorityRollPreviewModel carries the row copy for every kind
  ---
  duration_ms: 0.437475
  ...
# Subtest: picker-single recognizes the recommended-roll keypress
ok 2251 - picker-single recognizes the recommended-roll keypress
  ---
  duration_ms: 0.131902
  ...
# Subtest: picker-single stage-two footers carry the recommended-roll hints
ok 2252 - picker-single stage-two footers carry the recommended-roll hints
  ---
  duration_ms: 0.266238
  ...
# Subtest: picker-single shares one roll between the preview and the pinned row
ok 2253 - picker-single shares one roll between the preview and the pinned row
  ---
  duration_ms: 0.327976
  ...
# Subtest: picker-single plans the next-roll hint for the notice chips
ok 2254 - picker-single plans the next-roll hint for the notice chips
  ---
  duration_ms: 0.496388
  ...
# Subtest: picker-single notice cards name the roll, decay and next press
ok 2255 - picker-single notice cards name the roll, decay and next press
  ---
  duration_ms: 1.356389
  ...
# Subtest: picker-single decay payload and preview-target comparison
ok 2256 - picker-single decay payload and preview-target comparison
  ---
  duration_ms: 0.279955
  ...
# Subtest: picker-counted plans one recommendation per target with skips
ok 2257 - picker-counted plans one recommendation per target with skips
  ---
  duration_ms: 1.711908
  ...
# Subtest: picker-counted batch preview, footer and notice copy
ok 2258 - picker-counted batch preview, footer and notice copy
  ---
  duration_ms: 1.316342
  ...
# Subtest: picker-counted composes cancel then set-priority into one postimage
ok 2259 - picker-counted composes cancel then set-priority into one postimage
  ---
  duration_ms: 3.072154
  ...
# Subtest: picker-counted refuses a recurring cancel as one batch
ok 2260 - picker-counted refuses a recurring cancel as one batch
  ---
  duration_ms: 0.375978
  ...
# Subtest: recommended roll recovers with [unblocked::] when the writer is passed
ok 2261 - recommended roll recovers with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.741526
  ...
# Subtest: picker-counted stale lines refuse and new options stay byte-identical
ok 2262 - picker-counted stale lines refuse and new options stay byte-identical
  ---
  duration_ms: 0.996412
  ...
# Subtest: picker-links aggregates one recommendation per note
ok 2263 - picker-links aggregates one recommendation per note
  ---
  duration_ms: 1.025087
  ...
# Subtest: picker-links refuses a recurring cancel as one batch
ok 2264 - picker-links refuses a recurring cancel as one batch
  ---
  duration_ms: 0.355519
  ...
# Subtest: picker-links takes a single recommended roll with Ctrl+Enter
ok 2265 - picker-links takes a single recommended roll with Ctrl+Enter
  ---
  duration_ms: 27.889707
  ...
# Subtest: picker-links shows no pinned roll row in stage two
ok 2266 - picker-links shows no pinned roll row in stage two
  ---
  duration_ms: 5.058586
  ...
# Subtest: picker-links decays and cancels a single Task Link
ok 2267 - picker-links decays and cancels a single Task Link
  ---
  duration_ms: 4.778793
  ...
# Subtest: picker-links applies a mixed batch across two notes
ok 2268 - picker-links applies a mixed batch across two notes
  ---
  duration_ms: 3.780096
  ...
# Subtest: picker-links refuses the whole batch when a linked note changed
ok 2269 - picker-links refuses the whole batch when a linked note changed
  ---
  duration_ms: 2.983464
  ...
# Subtest: picker-links prunes today's open Pomodoro links
ok 2270 - picker-links prunes today's open Pomodoro links
  ---
  duration_ms: 4.060401
  ...
# Subtest: picker-single Ctrl+Enter rolls a P2 task in one undo group
ok 2271 - picker-single Ctrl+Enter rolls a P2 task in one undo group
  ---
  duration_ms: 13.999052
  ...
# Subtest: picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
ok 2272 - picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
  ---
  duration_ms: 12.654756
  ...
# Subtest: picker-single opens a ^prj task on inline scheduled for an immediate roll
ok 2273 - picker-single opens a ^prj task on inline scheduled for an immediate roll
  ---
  duration_ms: 13.40553
  ...
# Subtest: picker-counted opens on scheduled for an immediate mixed batch
ok 2274 - picker-counted opens on scheduled for an immediate mixed batch
  ---
  duration_ms: 14.66872
  ...
# Subtest: picker-links opens on scheduled for an immediate roll
ok 2275 - picker-links opens on scheduled for an immediate roll
  ---
  duration_ms: 12.801445
  ...
# Subtest: picker-single Ctrl+Enter decays a P2 task in one undo group
ok 2276 - picker-single Ctrl+Enter decays a P2 task in one undo group
  ---
  duration_ms: 13.886637
  ...
# Subtest: picker-single Ctrl+Enter cancels a P4 task in one undo group
ok 2277 - picker-single Ctrl+Enter cancels a P4 task in one undo group
  ---
  duration_ms: 13.705743
  ...
# Subtest: picker-single Ctrl+Enter in stage two writes the recommended roll
ok 2278 - picker-single Ctrl+Enter in stage two writes the recommended roll
  ---
  duration_ms: 13.417733
  ...
# Subtest: picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
ok 2279 - picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
  ---
  duration_ms: 3.689172
  ...
# Subtest: picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
ok 2280 - picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
  ---
  duration_ms: 5.00761
  ...
# Subtest: picker-single recurring P4 past the limit refuses and keeps the picker open
ok 2281 - picker-single recurring P4 past the limit refuses and keeps the picker open
  ---
  duration_ms: 12.868073
  ...
# Subtest: picker-single stale tasks refuse and re-render the decay preview
ok 2282 - picker-single stale tasks refuse and re-render the decay preview
  ---
  duration_ms: 13.623194
  ...
# Subtest: picker-single Ctrl+R on the card re-rolls the recommendation date
ok 2283 - picker-single Ctrl+R on the card re-rolls the recommendation date
  ---
  duration_ms: 2.905878
  ...
# Subtest: picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
ok 2284 - picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
  ---
  duration_ms: 2.300481
  ...
# Subtest: picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
ok 2285 - picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
  ---
  duration_ms: 11.628617
  ...
# Subtest: picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
ok 2286 - picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
  ---
  duration_ms: 13.847554
  ...
# Subtest: picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
ok 2287 - picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
  ---
  duration_ms: 13.50018
  ...
# Subtest: picker-counted Ctrl+Enter refuses when a target line changed
ok 2288 - picker-counted Ctrl+Enter refuses when a target line changed
  ---
  duration_ms: 13.327661
  ...
# Subtest: picker-counted Ctrl+Enter refuses a recurring cancel batch
ok 2289 - picker-counted Ctrl+Enter refuses a recurring cancel batch
  ---
  duration_ms: 11.112282
  ...
# Subtest: recommended roll on Pending offers a Work Log with the frozen date
ok 2290 - recommended roll on Pending offers a Work Log with the frozen date
  ---
  duration_ms: 1025.470521
  ...
# Subtest: recommended roll blank summary skips the Work Log without a fallback
ok 2291 - recommended roll blank summary skips the Work Log without a fallback
  ---
  duration_ms: 1025.229711
  ...
# Subtest: Ctrl+Enter in the Work Log stage confirms instead of re-rolling
ok 2292 - Ctrl+Enter in the Work Log stage confirms instead of re-rolling
  ---
  duration_ms: 1032.345494
  ...
# Subtest: counted recommended mixed batch logs only eligible roll and decay targets
ok 2293 - counted recommended mixed batch logs only eligible roll and decay targets
  ---
  duration_ms: 1021.395724
  ...
# Subtest: Task Link recommended roll deletes the emptied Pomodoro in the same daily write
ok 2294 - Task Link recommended roll deletes the emptied Pomodoro in the same daily write
  ---
  duration_ms: 3.979987
  ...
# Subtest: lane commit stamps an open Ready task
ok 2295 - lane commit stamps an open Ready task
  ---
  duration_ms: 2.650709
  ...
# Subtest: lane release stamps an open Next task
ok 2296 - lane release stamps an open Next task
  ---
  duration_ms: 0.511366
  ...
# Subtest: lane without a stamper leaves lines as they were
ok 2297 - lane without a stamper leaves lines as they were
  ---
  duration_ms: 0.219058
  ...
# Subtest: counted property set stamps every rewritten open task
ok 2298 - counted property set stamps every rewritten open task
  ---
  duration_ms: 2.104998
  ...
# Subtest: counted delete-property stamps the rewritten task
ok 2299 - counted delete-property stamps the rewritten task
  ---
  duration_ms: 0.504273
  ...
# Subtest: stamp lands before the suffix after a priority edit on a stamped line
ok 2300 - stamp lands before the suffix after a priority edit on a stamped line
  ---
  duration_ms: 0.486578
  ...
# Subtest: recurring tasks are never stamped
ok 2301 - recurring tasks are never stamped
  ---
  duration_ms: 0.351341
  ...
# Subtest: cancel never stamps
ok 2302 - cancel never stamps
  ---
  duration_ms: 1.007764
  ...
# Subtest: fresh and refresh never go through the end-append writers
ok 2303 - fresh and refresh never go through the end-append writers
  ---
  duration_ms: 0.404602
  ...
# Subtest: counted dependency edit stamps the rewritten parent
ok 2304 - counted dependency edit stamps the rewritten parent
  ---
  duration_ms: 4.63611
  ...
# Subtest: moved tasks are stamped at their destination
ok 2305 - moved tasks are stamped at their destination
  ---
  duration_ms: 2.64036
  ...
# Subtest: move without a stamper leaves lines as they were
ok 2306 - move without a stamper leaves lines as they were
  ---
  duration_ms: 0.564006
  ...
# Subtest: refresh row shows the effective interval in task mode
ok 2307 - refresh row shows the effective interval in task mode
  ---
  duration_ms: 0.730324
  ...
# Subtest: refresh row hides without the api and on closed tasks
ok 2308 - refresh row hides without the api and on closed tasks
  ---
  duration_ms: 0.128796
  ...
# Subtest: refresh row covers counted and link modes, including mixed
ok 2309 - refresh row covers counted and link modes, including mixed
  ---
  duration_ms: 0.261569
  ...
# Subtest: refresh value items offer presets and use default
ok 2310 - refresh value items offer presets and use default
  ---
  duration_ms: 0.697231
  ...
# Subtest: setRefreshLine stamps and sets or clears the interval
ok 2311 - setRefreshLine stamps and sets or clears the interval
  ---
  duration_ms: 0.458625
  ...
# Subtest: 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
ok 2312 - 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
  ---
  duration_ms: 8.985321
  ...
# Subtest: Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
ok 2313 - Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
  ---
  duration_ms: 3.610273
  ...
# Subtest: filtering expands matches, collapse state survives clearing, and hidden marks still submit
ok 2314 - filtering expands matches, collapse state survives clearing, and hidden marks still submit
  ---
  duration_ms: 4.365062
  ...
# Subtest: group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
ok 2315 - group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
  ---
  duration_ms: 1.312044
  ...
# Subtest: Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
ok 2316 - Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
  ---
  duration_ms: 0.721017
  ...
# Subtest: Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
ok 2317 - Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
  ---
  duration_ms: 1.386066
  ...
# Subtest: the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
ok 2318 - the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
  ---
  duration_ms: 0.619212
  ...
# Subtest: destination override shapes normalize and label
ok 2319 - destination override shapes normalize and label
  ---
  duration_ms: 0.221142
  ...
# Subtest: destination picker detection needs block-id-prompt api v1 with pick
ok 2320 - destination picker detection needs block-id-prompt api v1 with pick
  ---
  duration_ms: 0.378002
  ...
# Subtest: Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks
ok 2321 - Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks
  ---
  duration_ms: 3.848276
  ...
# Subtest: Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked
ok 2322 - Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked
  ---
  duration_ms: 0.7753
  ...
# Subtest: a cancelled destination pick and a missing picker leave rows untouched
ok 2323 - a cancelled destination pick and a missing picker leave rows untouched
  ---
  duration_ms: 0.746845
  ...
# Subtest: unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
ok 2324 - unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
  ---
  duration_ms: 0.705337
  ...
# Subtest: card model builds stable rows, scope metadata, and an existing recommendation
ok 2325 - card model builds stable rows, scope metadata, and an existing recommendation
  ---
  duration_ms: 7.775282
  ...
# Subtest: explicit preview builder matches writer rolls and deduplicates linked targets
ok 2326 - explicit preview builder matches writer rolls and deduplicates linked targets
  ---
  duration_ms: 0.81683
  ...
# Subtest: counted and linked card models report real target counts and mixed values
ok 2327 - counted and linked card models report real target counts and mixed values
  ---
  duration_ms: 4.014113
  ...
# Subtest: priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
ok 2328 - priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
  ---
  duration_ms: 2.528597
  ...
# Subtest: Escape, bare q, and Ctrl+[ close the card; nothing else does
ok 2329 - Escape, bare q, and Ctrl+[ close the card; nothing else does
  ---
  duration_ms: 1.178049
  ...
# Subtest: close keys never fire during composition or inside a text field
ok 2330 - close keys never fire during composition or inside a text field
  ---
  duration_ms: 1.518538
  ...
# Subtest: unavailable actions, input composition, and repeats stay safe
ok 2331 - unavailable actions, input composition, and repeats stay safe
  ---
  duration_ms: 1.867375
  ...
# Subtest: key resolver table covers lane state, API availability, and modifier guards
ok 2332 - key resolver table covers lane state, API availability, and modifier guards
  ---
  duration_ms: 1.582491
  ...
# Subtest: recurring cancellation and blocked lanes expose reasons instead of writes
ok 2333 - recurring cancellation and blocked lanes expose reasons instead of writes
  ---
  duration_ms: 0.839763
  ...
# Subtest: identity keys distinguish linked notes that share a line number
ok 2334 - identity keys distinguish linked notes that share a line number
  ---
  duration_ms: 2.007352
  ...
# Subtest: planScheduleReview opens for a bare date and skips when reason is known without Work Log
ok 2335 - planScheduleReview opens for a bare date and skips when reason is known without Work Log
  ---
  duration_ms: 1.108886
  ...
# Subtest: planScheduleReview counts unique tasks when Task Links repeat a target
ok 2336 - planScheduleReview counts unique tasks when Task Links repeat a target
  ---
  duration_ms: 0.346822
  ...
# Subtest: bare date on Ready opens a reason-only review and writes nothing until Enter
ok 2337 - bare date on Ready opens a reason-only review and writes nothing until Enter
  ---
  duration_ms: 21.424326
  ...
# Subtest: typed reason and blank reason on an existing Schedule Log keep per-target rules
ok 2338 - typed reason and blank reason on an existing Schedule Log keep per-target rules
  ---
  duration_ms: 10.045686
  ...
# Subtest: Ready vs Next vs Pending: only Next/Pending show Work summary
ok 2339 - Ready vs Next vs Pending: only Next/Pending show Work summary
  ---
  duration_ms: 16.03023
  ...
# Subtest: inline reason on Ready dispatches immediately; on Next it still reviews Work summary
ok 2340 - inline reason on Ready dispatches immediately; on Next it still reviews Work summary
  ---
  duration_ms: 7.367783
  ...
# Subtest: Tab moves from Reason to Work summary and Enter commits from either field
ok 2341 - Tab moves from Reason to Work summary and Enter commits from either field
  ---
  duration_ms: 2.628568
  ...
# Subtest: Back and Escape at both review fields write nothing
ok 2342 - Back and Escape at both review fields write nothing
  ---
  duration_ms: 5.79955
  ...
# Subtest: a target changed during review refuses with no write
ok 2343 - a target changed during review refuses with no write
  ---
  duration_ms: 2.48786
  ...
# Subtest: counted mixed targets share one review and one adapter call
ok 2344 - counted mixed targets share one review and one adapter call
  ---
  duration_ms: 3.717195
  ...
# Subtest: linked notes with equal line numbers both qualify
ok 2345 - linked notes with equal line numbers both qualify
  ---
  duration_ms: 2.817408
  ...
# Subtest: project lifecycle review names propagation and still writes once
ok 2346 - project lifecycle review names propagation and still writes once
  ---
  duration_ms: 2.202454
  ...
# Subtest: priority picks still skip the combined review and keep Work Log-only prompts
ok 2347 - priority picks still skip the combined review and keep Work Log-only prompts
  ---
  duration_ms: 2.094178
  ...
# Subtest: a typed date from the card's schedule row uses the combined review
ok 2348 - a typed date from the card's schedule row uses the combined review
  ---
  duration_ms: 2.029655
  ...
# Subtest: scheduling a Pending task goes straight to the combined review, never serial prompts
ok 2349 - scheduling a Pending task goes straight to the combined review, never serial prompts
  ---
  duration_ms: 1.935043
  ...
# Subtest: classic parser keeps ISO, M/D, and signed units and ignores concise forms
ok 2350 - classic parser keeps ISO, M/D, and signed units and ignores concise forms
  ---
  duration_ms: 1.38251
  ...
# Subtest: typed schedule resolver covers bare days, units, weekdays, and inline reasons
ok 2351 - typed schedule resolver covers bare days, units, weekdays, and inline reasons
  ---
  duration_ms: 1.125398
  ...
# Subtest: weekdays resolve to the next occurrence strictly after today
ok 2352 - weekdays resolve to the next occurrence strictly after today
  ---
  duration_ms: 0.143403
  ...
# Subtest: invalid leap dates, end-of-month offsets, and December rollover
ok 2353 - invalid leap dates, end-of-month offsets, and December rollover
  ---
  duration_ms: 0.362251
  ...
# Subtest: negative, overflow, malformed, and preset-filter queries are rejected without dates
ok 2354 - negative, overflow, malformed, and preset-filter queries are rejected without dates
  ---
  duration_ms: 0.166628
  ...
# Subtest: DST local-calendar arithmetic stays on calendar days in America/New_York
ok 2355 - DST local-calendar arithmetic stays on calendar days in America/New_York
  ---
  duration_ms: 80.982134
  ...
# Subtest: Task Card date stage previews weekday, ISO, relative distance, and rollover year
ok 2356 - Task Card date stage previews weekday, ISO, relative distance, and rollover year
  ---
  duration_ms: 13.392865
  ...
# Subtest: inline reason is preserved on the preview and skips the reason stage
ok 2357 - inline reason is preserved on the preview and skips the reason stage
  ---
  duration_ms: 9.484225
  ...
# Subtest: Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
ok 2358 - Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
  ---
  duration_ms: 5.240854
  ...
# Subtest: Shift+Enter on a Ready task commits in four gestures without a Work Log
ok 2359 - Shift+Enter on a Ready task commits in four gestures without a Work Log
  ---
  duration_ms: 4.042307
  ...
# Subtest: invalid typed dates render an error preview and do not write
ok 2360 - invalid typed dates render an error preview and do not write
  ---
  duration_ms: 3.355425
  ...
# Subtest: the card's schedule stage always uses the concise resolver
ok 2361 - the card's schedule stage always uses the concise resolver
  ---
  duration_ms: 1.669588
  ...
# Subtest: tomorrow stays a preset filter and is not stolen as a typed date
ok 2362 - tomorrow stays a preset filter and is not stolen as a typed date
  ---
  duration_ms: 1.362953
  ...
# Subtest: mixed Task Links preview one date and freeze that action with the inline reason
ok 2363 - mixed Task Links preview one date and freeze that action with the inline reason
  ---
  duration_ms: 9.791079
  ...
# Subtest: Ctrl+Enter still takes the recommended roll from the Task Card date stage
ok 2364 - Ctrl+Enter still takes the recommended roll from the Task Card date stage
  ---
  duration_ms: 2.884978
  ...
# Subtest: Modal harness models Obsidian 1.14 attachment and idempotent close
ok 2365 - Modal harness models Obsidian 1.14 attachment and idempotent close
  ---
  duration_ms: 1.41937
  ...
# Subtest: styles share key-card tokens and compact Task Card dimensions
ok 2366 - styles share key-card tokens and compact Task Card dimensions
  ---
  duration_ms: 0.2832
  ...
# Subtest: card renderer paints header, banner, strip, stable rows, more, and footer from the model
ok 2367 - card renderer paints header, banner, strip, stable rows, more, and footer from the model
  ---
  duration_ms: 8.794356
  ...
# Subtest: renderer does not consume randomness or invent recommendation data
ok 2368 - renderer does not consume randomness or invent recommendation data
  ---
  duration_ms: 1.755431
  ...
# Subtest: no-recommendation, cancel, mixed, long text, missing API, and error states render
ok 2369 - no-recommendation, cancel, mixed, long text, missing API, and error states render
  ---
  duration_ms: 4.480683
  ...
# Subtest: counted and linked cards disclose mixed values and Task Link notes
ok 2370 - counted and linked cards disclose mixed values and Task Link notes
  ---
  duration_ms: 4.246516
  ...
# Subtest: Ctrl+Shift+P always opens the Task Card, never the classic property list
ok 2371 - Ctrl+Shift+P always opens the Task Card, never the classic property list
  ---
  duration_ms: 4.25382
  ...
# Subtest: the plugin carries no Task Card pilot setting, date gate, or classic preference
ok 2372 - the plugin carries no Task Card pilot setting, date gate, or classic preference
  ---
  duration_ms: 17.158763
  ...
# Subtest: a leftover persisted taskCard flag is ignored and never rewritten
ok 2373 - a leftover persisted taskCard flag is ignored and never rewritten
  ---
  duration_ms: 5.932154
  ...
# Subtest: palette command is named Task card (set properties)
ok 2374 - palette command is named Task card (set properties)
  ---
  duration_ms: 9.912111
  ...
# Subtest: Task Card opens the compact card with dialog semantics and a close control
ok 2375 - Task Card opens the compact card with dialog semantics and a close control
  ---
  duration_ms: 1.397337
  ...
# Subtest: a More row opens that property's value stage, never a filter list, and Back restores the card
ok 2376 - a More row opens that property's value stage, never a filter list, and Back restores the card
  ---
  duration_ms: 3.176933
  ...
# Subtest: after open the actions list, not the Close button, has focus
ok 2377 - after open the actions list, not the Close button, has focus
  ---
  duration_ms: 4.239925
  ...
# Subtest: clicking card text keeps the card key router active exactly once
ok 2378 - clicking card text keeps the card key router active exactly once
  ---
  duration_ms: 16.186808
  ...
# Subtest: Ready card writes close from a key, P1 click, recommendations, and Alt+N
ok 2379 - Ready card writes close from a key, P1 click, recommendations, and Alt+N
  ---
  duration_ms: 5.841431
  ...
# Subtest: Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
ok 2380 - Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
  ---
  duration_ms: 3.961481
  ...
# Subtest: Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
ok 2381 - Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
  ---
  duration_ms: 3.402556
  ...
# Subtest: Ctrl+R recomputes and repaints the card recommendation
ok 2382 - Ctrl+R recomputes and repaints the card recommendation
  ---
  duration_ms: 1.589365
  ...
# Subtest: Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
ok 2383 - Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
  ---
  duration_ms: 18.028754
  ...
# Subtest: Task Link opens focused while resolving and consumes keys without replay
ok 2384 - Task Link opens focused while resolving and consumes keys without replay
  ---
  duration_ms: 6.064857
  ...
# Subtest: Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card
ok 2385 - Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card
  ---
  duration_ms: 2.456068
  ...
# Subtest: Task Link count replacement and source edits invalidate old resolutions
ok 2386 - Task Link count replacement and source edits invalidate old resolutions
  ---
  duration_ms: 0.950334
  ...
# Subtest: Task Link resolution failure and plugin unload close their shells
ok 2387 - Task Link resolution failure and plugin unload close their shells
  ---
  duration_ms: 1.459286
  ...
# Subtest: direct Depends on entry opens the dependency stage without painting the card or the list
ok 2388 - direct Depends on entry opens the dependency stage without painting the card or the list
  ---
  duration_ms: 1.083197
  ...
# Subtest: a direct stage for an unconfigured property closes instead of leaving an empty modal
ok 2389 - a direct stage for an unconfigured property closes instead of leaving an empty modal
  ---
  duration_ms: 0.323377
  ...
# Subtest: a refused direct stage closes instead of landing on a card or a list
ok 2390 - a refused direct stage closes instead of landing on a card or a list
  ---
  duration_ms: 0.685068
  ...
# Subtest: Ctrl+Shift+B lands on the Depends on stage with the same intent as card b
ok 2391 - Ctrl+Shift+B lands on the Depends on stage with the same intent as card b
  ---
  duration_ms: 2.524499
  ...
# Subtest: Ctrl+Shift+B Back returns to the card without re-dispatching
ok 2392 - Ctrl+Shift+B Back returns to the card without re-dispatching
  ---
  duration_ms: 0.991122
  ...
# Subtest: Ctrl+Shift+B on a plain bullet notices and closes the card
ok 2393 - Ctrl+Shift+B on a plain bullet notices and closes the card
  ---
  duration_ms: 0.575158
  ...
# Subtest: Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch
ok 2394 - Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch
  ---
  duration_ms: 2.597268
  ...
# Subtest: Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not
ok 2395 - Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not
  ---
  duration_ms: 2.00105
  ...
# Subtest: priority gesture writes the frozen date and duplicate dispatch is single-flight
ok 2396 - priority gesture writes the frozen date and duplicate dispatch is single-flight
  ---
  duration_ms: 6.913516
  ...
# Subtest: pending priority action passes its card preview through the Work Log adapter
ok 2397 - pending priority action passes its card preview through the Work Log adapter
  ---
  duration_ms: 1.939592
  ...
# Subtest: Task Link priority action refuses a stale cross-note preflight before writes
ok 2398 - Task Link priority action refuses a stale cross-note preflight before writes
  ---
  duration_ms: 4.828177
  ...
# Subtest: Task Link priority action rolls back earlier note writes after a later write fails
ok 2399 - Task Link priority action rolls back earlier note writes after a later write fails
  ---
  duration_ms: 1.853417
  ...
# Subtest: Task Link transaction reports a cleanup failure without implying global undo
ok 2400 - Task Link transaction reports a cleanup failure without implying global undo
  ---
  duration_ms: 0.928201
  ...
# Subtest: selected-property deletion uses the existing writer; other card rows stay non-deletable
ok 2401 - selected-property deletion uses the existing writer; other card rows stay non-deletable
  ---
  duration_ms: 3.75626
  ...
# Subtest: failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
ok 2402 - failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
  ---
  duration_ms: 1.172859
  ...
# Subtest: a refused deletion rebuilds the card from the refreshed line
ok 2403 - a refused deletion rebuilds the card from the refreshed line
  ---
  duration_ms: 1.179231
  ...
# Subtest: 0 deletes only priority and keeps the scheduled field byte-for-byte
ok 2404 - 0 deletes only priority and keeps the scheduled field byte-for-byte
  ---
  duration_ms: 1.394703
  ...
# Subtest: card keys pressed on a priority radio or the banner reach the resolver exactly once
ok 2405 - card keys pressed on a priority radio or the banner reach the resolver exactly once
  ---
  duration_ms: 2.595794
  ...
# Subtest: held or composing Enter on a radio or the banner never writes
ok 2406 - held or composing Enter on a radio or the banner never writes
  ---
  duration_ms: 1.030857
  ...
# Subtest: Escape, q, Q, and Ctrl+[ close the card without writing
ok 2407 - Escape, q, Q, and Ctrl+[ close the card without writing
  ---
  duration_ms: 6.018088
  ...
# Subtest: Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
ok 2408 - Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
  ---
  duration_ms: 0.769529
  ...
# Subtest: repeated close keys and a second close() are harmless
ok 2409 - repeated close keys and a second close() are harmless
  ---
  duration_ms: 0.875161
  ...
# Subtest: composition never closes the card or a stage
ok 2410 - composition never closes the card or a stage
  ---
  duration_ms: 0.7964
  ...
# Subtest: q typed into a stage's text field never closes the modal
ok 2411 - q typed into a stage's text field never closes the modal
  ---
  duration_ms: 0.602691
  ...
# Subtest: Ctrl+[ closes from a focused date field without writing
ok 2412 - Ctrl+[ closes from a focused date field without writing
  ---
  duration_ms: 0.612629
  ...
# Subtest: Ctrl+[ closes the schedule review from its Reason and Work summary fields
ok 2413 - Ctrl+[ closes the schedule review from its Reason and Work summary fields
  ---
  duration_ms: 3.919001
  ...
# Subtest: Ctrl+[ closes the summary-only schedule-work-log stage without writing
ok 2414 - Ctrl+[ closes the summary-only schedule-work-log stage without writing
  ---
  duration_ms: 0.761314
  ...
# Subtest: Ctrl+[ closes the lane-release Work summary without writing
ok 2415 - Ctrl+[ closes the lane-release Work summary without writing
  ---
  duration_ms: 0.802392
  ...
# Subtest: q closes from a focused More row and from the Close button
ok 2416 - q closes from a focused More row and from the Close button
  ---
  duration_ms: 1.431743
  ...
# Subtest: Ctrl+[ closes from focused card controls, the Back button, and the modal frame
ok 2417 - Ctrl+[ closes from focused card controls, the Back button, and the modal frame
  ---
  duration_ms: 2.575877
  ...
# Subtest: a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
ok 2418 - a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
  ---
  duration_ms: 5.9409
  ...
# Subtest: a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
ok 2419 - a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
  ---
  duration_ms: 2.270505
  ...
# Subtest: a direct dependency stage closes on Ctrl+[ but keeps q as typed text
ok 2420 - a direct dependency stage closes on Ctrl+[ but keeps q as typed text
  ---
  duration_ms: 0.526896
  ...
# Subtest: q and Ctrl+[ are not global closes: other modals and the decay card ignore them
ok 2421 - q and Ctrl+[ are not global closes: other modals and the decay card ignore them
  ---
  duration_ms: 0.798053
  ...
# Subtest: missing freshness API disables Review every with an honest reason
ok 2422 - missing freshness API disables Review every with an honest reason
  ---
  duration_ms: 0.609403
  ...
# Subtest: child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
ok 2423 - child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
  ---
  duration_ms: 0.875851
  ...
# Subtest: decay card keeps its classes and shares key-card tokens
ok 2424 - decay card keeps its classes and shares key-card tokens
  ---
  duration_ms: 0.150988
  ...
# Subtest: decay card footer always names the X drop alias; the trial date is not this gate
ok 2425 - decay card footer always names the X drop alias; the trial date is not this gate
  ---
  duration_ms: 0.281798
  ...
# Subtest: task card level chips reuse the shared priority mark when available
ok 2426 - task card level chips reuse the shared priority mark when available
  ---
  duration_ms: 0.9008
  ...
# Subtest: task card labels are unchanged without the priority mark api
ok 2427 - task card labels are unchanged without the priority mark api
  ---
  duration_ms: 3.547132
  ...
# Subtest: manifest order is authoritative and fragments share one lexical scope
ok 2428 - manifest order is authoritative and fragments share one lexical scope
  ---
  duration_ms: 108.436229
  ...
# Subtest: builds are deterministic and build:check is read-only on success
ok 2429 - builds are deterministic and build:check is read-only on success
  ---
  duration_ms: 168.333304
  ...
# Subtest: read-only check rejects changed fragments and edited generated output
ok 2430 - read-only check rejects changed fragments and edited generated output
  ---
  duration_ms: 162.245734
  ...
# Subtest: check rejects a missing generated bundle without writing it
ok 2431 - check rejects a missing generated bundle without writing it
  ---
  duration_ms: 55.14805
  ...
# Subtest: fragment line limit is enforced before writing output
ok 2432 - fragment line limit is enforced before writing output
  ---
  duration_ms: 1.328386
  ...
# Subtest: fragment syntax errors are rejected before writing output
ok 2433 - fragment syntax errors are rejected before writing output
  ---
  duration_ms: 27.830835
  ...
# Subtest: malformed, empty, duplicate, and traversal manifests are rejected read-only
    # Subtest: invalid JSON
    ok 1 - invalid JSON
      ---
      duration_ms: 0.803004
      ...
    # Subtest: empty manifest
    ok 2 - empty manifest
      ---
      duration_ms: 1.421043
      ...
    # Subtest: non-array manifest
    ok 3 - non-array manifest
      ---
      duration_ms: 1.426924
      ...
    # Subtest: duplicate entries
    ok 4 - duplicate entries
      ---
      duration_ms: 28.824422
      ...
    # Subtest: traversal entry
    ok 5 - traversal entry
      ---
      duration_ms: 0.878476
      ...
    # Subtest: absolute entry
    ok 6 - absolute entry
      ---
      duration_ms: 0.551663
      ...
    1..6
ok 2434 - malformed, empty, duplicate, and traversal manifests are rejected read-only
  ---
  duration_ms: 35.556953
  ...
# Subtest: missing and omitted fragments are rejected read-only
    # Subtest: missing manifest entry
    ok 1 - missing manifest entry
      ---
      duration_ms: 0.603592
      ...
    # Subtest: unlisted JavaScript source
    ok 2 - unlisted JavaScript source
      ---
      duration_ms: 25.36591
      ...
    1..2
ok 2435 - missing and omitted fragments are rejected read-only
  ---
  duration_ms: 26.270225
  ...
# Subtest: escaping fragment symlinks are rejected read-only
ok 2436 - escaping fragment symlinks are rejected read-only
  ---
  duration_ms: 1.105441
  ...
# Subtest: parity comparator identifies changed helper and plugin methods
ok 2437 - parity comparator identifies changed helper and plugin methods
  ---
  duration_ms: 9.217465
  ...
# Subtest: parity comparator accepts a mixin-split helper class but not a changed method or superclass
ok 2438 - parity comparator accepts a mixin-split helper class but not a changed method or superclass
  ---
  duration_ms: 0.516877
  ...
# Subtest: both prompt copies pass the shared fixture table identically
ok 2439 - both prompt copies pass the shared fixture table identically
  ---
  duration_ms: 7.740075
  ...
# Subtest: suggestion is valid, compact, and collision-aware
ok 2440 - suggestion is valid, compact, and collision-aware
  ---
  duration_ms: 0.665921
  ...
# Subtest: rename excludes exactly one old-ID occurrence
ok 2441 - rename excludes exactly one old-ID occurrence
  ---
  duration_ms: 1.38809
  ...
# Subtest: dependency legacy [id::] reuses only valid free IDs
ok 2442 - dependency legacy [id::] reuses only valid free IDs
  ---
  duration_ms: 0.422737
  ...
# Subtest: project conversion keeps the existing suggestBlockIdFromTask
ok 2443 - project conversion keeps the existing suggestBlockIdFromTask
  ---
  duration_ms: 0.875902
  ...
# Subtest: successor SB vectors are unchanged
ok 2444 - successor SB vectors are unchanged
  ---
  duration_ms: 1.051397
  ...
# Subtest: option-bracket ring reads Blocked as a source-only slot ahead of Ready
ok 2445 - option-bracket ring reads Blocked as a source-only slot ahead of Ready
  ---
  duration_ms: 1.675268
  ...
# Subtest: isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
ok 2446 - isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
  ---
  duration_ms: 0.428448
  ...
# Subtest: option-bracket refuses to change a member while its project is Blocked
ok 2447 - option-bracket refuses to change a member while its project is Blocked
  ---
  duration_ms: 2.90208
  ...
# Subtest: tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
ok 2448 - tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
  ---
  duration_ms: 1.69224
  ...
# Subtest: project resident notice reads the inline ^prj date and ignores frontmatter scheduled
ok 2449 - project resident notice reads the inline ^prj date and ignores frontmatter scheduled
  ---
  duration_ms: 0.615455
  ...
# Subtest: findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
ok 2450 - findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
  ---
  duration_ms: 0.359997
  ...
# Subtest: field removal collapses only the exposed span and preserves the rest of the line
ok 2451 - field removal collapses only the exposed span and preserves the rest of the line
  ---
  duration_ms: 0.329449
  ...
# Subtest: vault-path retirement preserves CRLF and a missing final newline
ok 2452 - vault-path retirement preserves CRLF and a missing final newline
  ---
  duration_ms: 0.988697
  ...
# Subtest: Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
ok 2453 - Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
  ---
  duration_ms: 0.577572
  ...
# Subtest: Schedule Log discovery ignores a marker owned by a nested grandchild
ok 2454 - Schedule Log discovery ignores a marker owned by a nested grandchild
  ---
  duration_ms: 0.405314
  ...
# Subtest: Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
ok 2455 - Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
  ---
  duration_ms: 0.463164
  ...
# Subtest: a task with no Schedule Log gets its field retired without any insertion or new marker
ok 2456 - a task with no Schedule Log gets its field retired without any insertion or new marker
  ---
  duration_ms: 0.133425
  ...
# Subtest: Schedule Log entry uses the canonical arrow, dash, and lock bytes
ok 2457 - Schedule Log entry uses the canonical arrow, dash, and lock bytes
  ---
  duration_ms: 0.095833
  ...
# Subtest: retirement stays a no-op for shapes that are not proof of a blocking date
ok 2458 - retirement stays a no-op for shapes that are not proof of a blocking date
  ---
  duration_ms: 0.165546
  ...
# Subtest: cycling Blocked backward to Cancelled retires the date and logs, matching forward
ok 2459 - cycling Blocked backward to Cancelled retires the date and logs, matching forward
  ---
  duration_ms: 3.80832
  ...
# Subtest: single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
ok 2460 - single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
  ---
  duration_ms: 1.045706
  ...
# Subtest: counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
ok 2461 - counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
  ---
  duration_ms: 1.327343
  ...
# Subtest: counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
ok 2462 - counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
  ---
  duration_ms: 0.629892
  ...
# Subtest: transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
ok 2463 - transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
  ---
  duration_ms: 1.848729
  ...
# Subtest: pressing again after Blocked retirement performs an ordinary transition with no further changes
ok 2464 - pressing again after Blocked retirement performs an ordinary transition with no further changes
  ---
  duration_ms: 0.219569
  ...
# Subtest: Alt+] on a date-blocked ^prj recovers open residents in step
ok 2465 - Alt+] on a date-blocked ^prj recovers open residents in step
  ---
  duration_ms: 14.110005
  ...
# Subtest: Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
ok 2466 - Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
  ---
  duration_ms: 1.009697
  ...
# Subtest: planProjectResidentRecoveryEdits recovers when a cross-note id is not open
ok 2467 - planProjectResidentRecoveryEdits recovers when a cross-note id is not open
  ---
  duration_ms: 0.357242
  ...
# Subtest: Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
ok 2468 - Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
  ---
  duration_ms: 1.386767
  ...
# Subtest: Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
ok 2469 - Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
  ---
  duration_ms: 0.891261
  ...
# Subtest: Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
ok 2470 - Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
  ---
  duration_ms: 1.703992
  ...
# Subtest: cycling a transcluded ^prj recovers residents in the source note
ok 2471 - cycling a transcluded ^prj recovers residents in the source note
  ---
  duration_ms: 0.857357
  ...
# Subtest: cycler BK1–BK12 accept and empty
ok 2472 - cycler BK1–BK12 accept and empty
  ---
  duration_ms: 1.228074
  ...
# Subtest: cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded
ok 2473 - cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded
  ---
  duration_ms: 0.604524
  ...
# Subtest: cycler MC4 strike/restore skip BLOCKS lines
ok 2474 - cycler MC4 strike/restore skip BLOCKS lines
  ---
  duration_ms: 0.847507
  ...
# Subtest: cycler MC3 tree close skips BLOCKS embeds
ok 2475 - cycler MC3 tree close skips BLOCKS embeds
  ---
  duration_ms: 0.773145
  ...
# Subtest: cycler MC1/MC2 Pomodoro and successor scanners skip managed lines
ok 2476 - cycler MC1/MC2 Pomodoro and successor scanners skip managed lines
  ---
  duration_ms: 0.979981
  ...
# Subtest: cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS
ok 2477 - cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS
  ---
  duration_ms: 0.253444
  ...
# Subtest: range planner preserves every single-item mode without an effective count
ok 2478 - range planner preserves every single-item mode without an effective count
  ---
  duration_ms: 7.420826
  ...
# Subtest: item counts carry children, skip blank lines and loose continuations, and clamp
ok 2479 - item counts carry children, skip blank lines and loose continuations, and clamp
  ---
  duration_ms: 0.305243
  ...
# Subtest: range stops at headings, shallower lines, same-level paragraphs and fences
ok 2480 - range stops at headings, shallower lines, same-level paragraphs and fences
  ---
  duration_ms: 0.179052
  ...
# Subtest: siblings require the exact whitespace and blockquote prefix
ok 2481 - siblings require the exact whitespace and blockquote prefix
  ---
  duration_ms: 0.199822
  ...
# Subtest: counted demotion moves four complete blocks to one existing section
ok 2482 - counted demotion moves four complete blocks to one existing section
  ---
  duration_ms: 3.982342
  ...
# Subtest: counted demotion creates a typed section or one default Requirements section
ok 2483 - counted demotion creates a typed section or one default Requirements section
  ---
  duration_ms: 2.076704
  ...
# Subtest: bottom-up removal splices blank seams and maps destinations before the source
ok 2484 - bottom-up removal splices blank seams and maps destinations before the source
  ---
  duration_ms: 0.36141
  ...
# Subtest: counted promotion Enter appends tasks in order and removes an emptied source section
ok 2485 - counted promotion Enter appends tasks in order and removes an emptied source section
  ---
  duration_ms: 0.845173
  ...
# Subtest: counted promotion to existing or new non-Tasks destinations keeps all bullets plain
ok 2486 - counted promotion to existing or new non-Tasks destinations keeps all bullets plain
  ---
  duration_ms: 0.495646
  ...
# Subtest: same-source Tasks promotion rewrites all selected lines in place
ok 2487 - same-source Tasks promotion rewrites all selected lines in place
  ---
  duration_ms: 0.87488
  ...
# Subtest: counted demotion outside Tasks moves to the next section in one write
ok 2488 - counted demotion outside Tasks moves to the next section in one write
  ---
  duration_ms: 0.368934
  ...
# Subtest: in-place ranges write once without centering for nested, non-dash, and unrouted items
ok 2489 - in-place ranges write once without centering for nested, non-dash, and unrouted items
  ---
  duration_ms: 0.846145
  ...
# Subtest: mixed demotion ranges count unchanged siblings and only move top-level dash tasks
ok 2490 - mixed demotion ranges count unchanged siblings and only move top-level dash tasks
  ---
  duration_ms: 0.404853
  ...
# Subtest: mixed promotion preserves existing tasks and a nonempty source section
ok 2491 - mixed promotion preserves existing tasks and a nonempty source section
  ---
  duration_ms: 0.214038
  ...
# Subtest: Vim action consumes explicit additional-item counts and preserves bare behavior
ok 2492 - Vim action consumes explicit additional-item counts and preserves bare behavior
  ---
  duration_ms: 2.425359
  ...
# Subtest: command checking preserves pending count; execution consumes it once and resets Vim
ok 2493 - command checking preserves pending count; execution consumes it once and resets Vim
  ---
  duration_ms: 0.980171
  ...
# Subtest: command route stays single without normal-mode explicit count and supports in-place ranges
ok 2494 - command route stays single without normal-mode explicit count and supports in-place ranges
  ---
  duration_ms: 0.404652
  ...
# Subtest: picker displays at most five preview rows plus overflow; single picker is unchanged
ok 2495 - picker displays at most five preview rows plus overflow; single picker is unchanged
  ---
  duration_ms: 1.282479
  ...
# Subtest: stale counted picker and cancelled picker never write
ok 2496 - stale counted picker and cancelled picker never write
  ---
  duration_ms: 0.810538
  ...
# Subtest: counted moves round-trip CRLF and preserve the presence or absence of a final newline
ok 2497 - counted moves round-trip CRLF and preserve the presence or absence of a final newline
  ---
  duration_ms: 3.196712
  ...
# Subtest: direct open/done transitions include incomplete statuses without broadening excluded statuses
ok 2498 - direct open/done transitions include incomplete statuses without broadening excluded statuses
  ---
  duration_ms: 1.203507
  ...
# Subtest: Ctrl+Enter block-link selection recognizes live and retired forms
ok 2499 - Ctrl+Enter block-link selection recognizes live and retired forms
  ---
  duration_ms: 2.093276
  ...
# Subtest: Pomodoro child ownership is status-neutral and bounded by contiguous list structure
ok 2500 - Pomodoro child ownership is status-neutral and bounded by contiguous list structure
  ---
  duration_ms: 0.783015
  ...
# Subtest: daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
ok 2501 - daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
  ---
  duration_ms: 0.269865
  ...
# Subtest: parsePomodoroEntryLineParts reads placeholder and range names conservatively
ok 2502 - parsePomodoroEntryLineParts reads placeholder and range names conservatively
  ---
  duration_ms: 0.8013
  ...
# Subtest: formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
ok 2503 - formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
  ---
  duration_ms: 0.153623
  ...
# Subtest: Pomodoro bullet toggle accepts empty indented list items
ok 2504 - Pomodoro bullet toggle accepts empty indented list items
  ---
  duration_ms: 0.280085
  ...
# Subtest: Pomodoro bullet toggle rejects non-empty or out-of-section bullets
ok 2505 - Pomodoro bullet toggle rejects non-empty or out-of-section bullets
  ---
  duration_ms: 0.227615
  ...
# Subtest: Pomodoro bullet toggle reverses only empty open childless placeholders
ok 2506 - Pomodoro bullet toggle reverses only empty open childless placeholders
  ---
  duration_ms: 0.489204
  ...
# Subtest: Pomodoro bullet toggle reverses named empty open childless placeholders
ok 2507 - Pomodoro bullet toggle reverses named empty open childless placeholders
  ---
  duration_ms: 0.360869
  ...
# Subtest: Pomodoro bullet toggle round trips and normalizes child indentation
ok 2508 - Pomodoro bullet toggle round trips and normalizes child indentation
  ---
  duration_ms: 0.206885
  ...
# Subtest: Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
ok 2509 - Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
  ---
  duration_ms: 0.161529
  ...
# Subtest: Pomodoro toggle key gate does not shadow bare Option bracket cycling
ok 2510 - Pomodoro toggle key gate does not shadow bare Option bracket cycling
  ---
  duration_ms: 0.169183
  ...
# Subtest: Pomodoro toggle command is daily-only and places the cursor for both directions
ok 2511 - Pomodoro toggle command is daily-only and places the cursor for both directions
  ---
  duration_ms: 0.496178
  ...
# Subtest: Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
ok 2512 - Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
  ---
  duration_ms: 0.29319
  ...
# Subtest: Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
ok 2513 - Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
  ---
  duration_ms: 1.87011
  ...
# Subtest: Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
ok 2514 - Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
  ---
  duration_ms: 26.707381
  ...
# Subtest: Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
ok 2515 - Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
  ---
  duration_ms: 2.129255
  ...
# Subtest: Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
ok 2516 - Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
  ---
  duration_ms: 2.154201
  ...
# Subtest: Ctrl+Enter closing the local line over an already-closed target does not write it a second time
ok 2517 - Ctrl+Enter closing the local line over an already-closed target does not write it a second time
  ---
  duration_ms: 0.797032
  ...
# Subtest: Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
ok 2518 - Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
  ---
  duration_ms: 0.703182
  ...
# Subtest: Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
ok 2519 - Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
  ---
  duration_ms: 1.614351
  ...
# Subtest: Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
ok 2520 - Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
  ---
  duration_ms: 0.471109
  ...
# Subtest: Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
ok 2521 - Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
  ---
  duration_ms: 0.552034
  ...
# Subtest: Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
ok 2522 - Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
  ---
  duration_ms: 0.800678
  ...
# Subtest: Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
ok 2523 - Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
  ---
  duration_ms: 0.663837
  ...
# Subtest: getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
ok 2524 - getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
  ---
  duration_ms: 0.38219
  ...
# Subtest: Ctrl+Enter close continues the walk with complete after finalize ran
ok 2525 - Ctrl+Enter close continues the walk with complete after finalize ran
  ---
  duration_ms: 12.166855
  ...
# Subtest: Ctrl+Enter close continues only after transclusion propagation landed
ok 2526 - Ctrl+Enter close continues only after transclusion propagation landed
  ---
  duration_ms: 13.511262
  ...
# Subtest: Ctrl+Enter reopen settles the walk with null
ok 2527 - Ctrl+Enter reopen settles the walk with null
  ---
  duration_ms: 11.828449
  ...
# Subtest: Ctrl+Enter swallows the key with no write while the walk is busy
ok 2528 - Ctrl+Enter swallows the key with no write while the walk is busy
  ---
  duration_ms: 11.170282
  ...
# Subtest: Ctrl+Enter with a null capture behaves exactly like today
ok 2529 - Ctrl+Enter with a null capture behaves exactly like today
  ---
  duration_ms: 11.699412
  ...
# Subtest: Ctrl+Enter with nav v2 or no nav keeps today's behavior
ok 2530 - Ctrl+Enter with nav v2 or no nav keeps today's behavior
  ---
  duration_ms: 22.279038
  ...
# Subtest: Ctrl+Enter lets the checklist claim win before capturing
ok 2531 - Ctrl+Enter lets the checklist claim win before capturing
  ---
  duration_ms: 0.850023
  ...
# Subtest: Ctrl+Enter settles the walk with null when the toggle rejects
ok 2532 - Ctrl+Enter settles the walk with null when the toggle rejects
  ---
  duration_ms: 12.265674
  ...
# Subtest: Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
ok 2533 - Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
  ---
  duration_ms: 2.44145
  ...
# Subtest: eligible Tasks demotions prompt in project and non-project notes
ok 2534 - eligible Tasks demotions prompt in project and non-project notes
  ---
  duration_ms: 2.914464
  ...
# Subtest: selectable headings skip YAML, fences, empty titles, and Tasks
ok 2535 - selectable headings skip YAML, fences, empty titles, and Tasks
  ---
  duration_ms: 0.912812
  ...
# Subtest: duplicate heading identities stay distinct and route to the chosen occurrence
ok 2536 - duplicate heading identities stay distinct and route to the chosen occurrence
  ---
  duration_ms: 1.064833
  ...
# Subtest: demotion picker defaults and typed names resolve without synthetic duplicates
ok 2537 - demotion picker defaults and typed names resolve without synthetic duplicates
  ---
  duration_ms: 1.932368
  ...
# Subtest: picker keyboard state wraps, clamps, and refuses invalid Enter
ok 2538 - picker keyboard state wraps, clamps, and refuses invalid Enter
  ---
  duration_ms: 0.364426
  ...
# Subtest: new-section formatting keeps extra blanks, final newlines, and nested children
ok 2539 - new-section formatting keeps extra blanks, final newlines, and nested children
  ---
  duration_ms: 0.829393
  ...
# Subtest: existing-section insertion works before and after the source on CRLF-backed editors
ok 2540 - existing-section insertion works before and after the source on CRLF-backed editors
  ---
  duration_ms: 3.006328
  ...
# Subtest: command opens one picker, writes only on accept, and restores cursor plus center
ok 2541 - command opens one picker, writes only on accept, and restores cursor plus center
  ---
  duration_ms: 0.779288
  ...
# Subtest: pointer activation, Escape, and double-submit protection leave a consistent note
ok 2542 - pointer activation, Escape, and double-submit protection leave a consistent note
  ---
  duration_ms: 1.209229
  ...
# Subtest: stale document, changed editor, or missing heading notice without writing
ok 2543 - stale document, changed editor, or missing heading notice without writing
  ---
  duration_ms: 1.505724
  ...
# Subtest: dependency normalizer writes path-qualified IDs and is idempotent
ok 2544 - dependency normalizer writes path-qualified IDs and is idempotent
  ---
  duration_ms: 1.949381
  ...
# Subtest: Tasks-generated IDs become local block IDs when none exists
ok 2545 - Tasks-generated IDs become local block IDs when none exists
  ---
  duration_ms: 0.721808
  ...
# Subtest: note rename rewrites target IDs and yields exact propagation mappings
ok 2546 - note rename rewrites target IDs and yields exact propagation mappings
  ---
  duration_ms: 0.280415
  ...
# Subtest: note rename also rewrites same-file dependsOn references
ok 2547 - note rename also rewrites same-file dependsOn references
  ---
  duration_ms: 0.229347
  ...
# Subtest: dependency normalization skips unsupported paths and fenced examples
ok 2548 - dependency normalization skips unsupported paths and fenced examples
  ---
  duration_ms: 0.344337
  ...
# Subtest: blocked-dependent planner matches the CLI dependency truth table
ok 2549 - blocked-dependent planner matches the CLI dependency truth table
  ---
  duration_ms: 2.344586
  ...
# Subtest: blocked-dependent edits preserve EOLs and skip stale lines idempotently
ok 2550 - blocked-dependent edits preserve EOLs and skip stale lines idempotently
  ---
  duration_ms: 0.802392
  ...
# Subtest: project recovery strips resident tags and works without freshness v12
ok 2551 - project recovery strips resident tags and works without freshness v12
  ---
  duration_ms: 1.420021
  ...
# Subtest: recovery passes daily-note and Today skip flags to ledger freshness
ok 2552 - recovery passes daily-note and Today skip flags to ledger freshness
  ---
  duration_ms: 0.426154
  ...
# Subtest: normalization mappings propagate to every dependent file
ok 2553 - normalization mappings propagate to every dependent file
  ---
  duration_ms: 1.101572
  ...
# Subtest: runtime normalizer skips unsupported paths with one informative notice
ok 2554 - runtime normalizer skips unsupported paths with one informative notice
  ---
  duration_ms: 0.684576
  ...
# Subtest: rename reconciliation rewrites the target and every dependent
ok 2555 - rename reconciliation rewrites the target and every dependent
  ---
  duration_ms: 0.556873
  ...
# Subtest: editor dependency normalization abandons and reschedules stale snapshots
ok 2556 - editor dependency normalization abandons and reschedules stale snapshots
  ---
  duration_ms: 0.589555
  ...
# Subtest: rename reconciliation abandons and reschedules stale editor snapshots
ok 2557 - rename reconciliation abandons and reschedules stale editor snapshots
  ---
  duration_ms: 0.2567
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 2558 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.788866
  ...
# Subtest: close-time retirement skips Depends-On lines
ok 2559 - close-time retirement skips Depends-On lines
  ---
  duration_ms: 1.124036
  ...
# Subtest: reopen restoration skips Depends-On lines instead of re-embedding them
ok 2560 - reopen restoration skips Depends-On lines instead of re-embedding them
  ---
  duration_ms: 0.559658
  ...
# Subtest: embedded-tree close collection ignores Depends-On lines
ok 2561 - embedded-tree close collection ignores Depends-On lines
  ---
  duration_ms: 0.316174
  ...
# Subtest: Alt-bracket bullet formatting never applies to Depends-On lines
ok 2562 - Alt-bracket bullet formatting never applies to Depends-On lines
  ---
  duration_ms: 0.539289
  ...
# Subtest: Ctrl+Enter on a dependency link closes only the target and runs the recovery
ok 2563 - Ctrl+Enter on a dependency link closes only the target and runs the recovery
  ---
  duration_ms: 1.651132
  ...
# Subtest: Ctrl+Enter on a dependency link reopens only the target, root-only
ok 2564 - Ctrl+Enter on a dependency link reopens only the target, root-only
  ---
  duration_ms: 1.170725
  ...
# Subtest: single and counted Alt-bracket cycle the dependency target under the cursor
ok 2565 - single and counted Alt-bracket cycle the dependency target under the cursor
  ---
  duration_ms: 19.647815
  ...
# Subtest: single and counted Alt-bracket report when the cursor is off every dependency link
ok 2566 - single and counted Alt-bracket report when the cursor is off every dependency link
  ---
  duration_ms: 0.561181
  ...
# Subtest: Ctrl+Enter candidate resolution finds plain links on Depends-On lines
ok 2567 - Ctrl+Enter candidate resolution finds plain links on Depends-On lines
  ---
  duration_ms: 0.197998
  ...
# Subtest: dependency-id normalisation never edits Depends-On lines
ok 2568 - dependency-id normalisation never edits Depends-On lines
  ---
  duration_ms: 0.257151
  ...
# Subtest: note rename rewrites fields while leaving Depends-On lines alone
ok 2569 - note rename rewrites fields while leaving Depends-On lines alone
  ---
  duration_ms: 0.195463
  ...
# Subtest: recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
ok 2570 - recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
  ---
  duration_ms: 1.865971
  ...
# Subtest: cycler freshness: local-fallback rewrite stamps last via injected stamper
ok 2571 - cycler freshness: local-fallback rewrite stamps last via injected stamper
  ---
  duration_ms: 1.764609
  ...
# Subtest: cycler freshness: rewrites without a stamper are unchanged (identity default)
ok 2572 - cycler freshness: rewrites without a stamper are unchanged (identity default)
  ---
  duration_ms: 0.39815
  ...
# Subtest: cycler freshness: a throwing stamper leaves the rewritten line intact
ok 2573 - cycler freshness: a throwing stamper leaves the rewritten line intact
  ---
  duration_ms: 0.152471
  ...
# Subtest: cycler freshness: transcluded rewrite stamps last via injected stamper
ok 2574 - cycler freshness: transcluded rewrite stamps last via injected stamper
  ---
  duration_ms: 0.216082
  ...
# Subtest: cycler freshness: cycling a plain line stamps through the follow-up edit
ok 2575 - cycler freshness: cycling a plain line stamps through the follow-up edit
  ---
  duration_ms: 0.821337
  ...
# Subtest: cycler freshness: Tasks-command rewrite with the expected status is stamped
ok 2576 - cycler freshness: Tasks-command rewrite with the expected status is stamped
  ---
  duration_ms: 0.346562
  ...
# Subtest: cycler freshness: Tasks command that inserts a line never stamps
ok 2577 - cycler freshness: Tasks command that inserts a line never stamps
  ---
  duration_ms: 0.268743
  ...
# Subtest: cycler freshness: Tasks command that deletes the line never stamps the next task
ok 2578 - cycler freshness: Tasks command that deletes the line never stamps the next task
  ---
  duration_ms: 0.26695
  ...
# Subtest: cycler freshness: Tasks command that leaves a different status never stamps
ok 2579 - cycler freshness: Tasks command that leaves a different status never stamps
  ---
  duration_ms: 0.383482
  ...
# Subtest: cycler freshness: cycling without ledger-tools writes no stamp
ok 2580 - cycler freshness: cycling without ledger-tools writes no stamp
  ---
  duration_ms: 0.479485
  ...
# Subtest: cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
ok 2581 - cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
  ---
  duration_ms: 0.195523
  ...
# Subtest: Pomodoro marker helpers normalize every block link and preserve fences and EOLs
ok 2582 - Pomodoro marker helpers normalize every block link and preserve fences and EOLs
  ---
  duration_ms: 2.630511
  ...
# Subtest: completed Pomodoro markers are normalized per occurrence
ok 2583 - completed Pomodoro markers are normalized per occurrence
  ---
  duration_ms: 0.549118
  ...
# Subtest: move-only Pomodoro links require a strict immediate hash directive
ok 2584 - move-only Pomodoro links require a strict immediate hash directive
  ---
  duration_ms: 2.574254
  ...
# Subtest: Pomodoro move-only planner toggles links across additional physical lines
ok 2585 - Pomodoro move-only planner toggles links across additional physical lines
  ---
  duration_ms: 1.193729
  ...
# Subtest: Pomodoro move-only planner round trips exact text and rejects strict non-matches
ok 2586 - Pomodoro move-only planner round trips exact text and rejects strict non-matches
  ---
  duration_ms: 0.553066
  ...
# Subtest: bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
ok 2587 - bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
  ---
  duration_ms: 1.625062
  ...
# Subtest: Pomodoro move-only runtime removes locally and validates additions independently
ok 2588 - Pomodoro move-only runtime removes locally and validates additions independently
  ---
  duration_ms: 1.078558
  ...
# Subtest: Pomodoro move-only runtime protects live lines after asynchronous failures
ok 2589 - Pomodoro move-only runtime protects live lines after asynchronous failures
  ---
  duration_ms: 0.438086
  ...
# Subtest: Pomodoro hash Vim mapping distinguishes bare and explicit repeats
ok 2590 - Pomodoro hash Vim mapping distinguishes bare and explicit repeats
  ---
  duration_ms: 12.491604
  ...
# Subtest: Pomodoro completion marks originals and carries clean live copies
ok 2591 - Pomodoro completion marks originals and carries clean live copies
  ---
  duration_ms: 2.12651
  ...
# Subtest: Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
ok 2592 - Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
  ---
  duration_ms: 0.959441
  ...
# Subtest: Pomodoro completion carries the closed Pomodoro name onto created entries
ok 2593 - Pomodoro completion carries the closed Pomodoro name onto created entries
  ---
  duration_ms: 0.462133
  ...
# Subtest: buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
ok 2594 - buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
  ---
  duration_ms: 0.516075
  ...
# Subtest: buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
ok 2595 - buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
  ---
  duration_ms: 0.233416
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is marked
ok 2596 - buildPomodoroCompletionPlan keeps source order when every carried link is marked
  ---
  duration_ms: 0.183841
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
ok 2597 - buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
  ---
  duration_ms: 0.215752
  ...
# Subtest: Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
ok 2598 - Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
  ---
  duration_ms: 6.415836
  ...
# Subtest: deferred-only close deletes the emptied entry and carries stripped links
ok 2599 - deferred-only close deletes the emptied entry and carries stripped links
  ---
  duration_ms: 0.854842
  ...
# Subtest: deferred-only close at EOF leaves no dangling newline
ok 2600 - deferred-only close at EOF leaves no dangling newline
  ---
  duration_ms: 0.293791
  ...
# Subtest: a close with a remaining copyable link keeps the [x] entry
ok 2601 - a close with a remaining copyable link keeps the [x] entry
  ---
  duration_ms: 0.383131
  ...
# Subtest: a prose sibling keeps the closed entry on a deferred close
ok 2602 - a prose sibling keeps the closed entry on a deferred close
  ---
  duration_ms: 0.348655
  ...
# Subtest: Ctrl+Enter deferred-only close deletes the entry in one gesture
ok 2603 - Ctrl+Enter deferred-only close deletes the entry in one gesture
  ---
  duration_ms: 4.076882
  ...
# Subtest: selected Done Pomodoro transclusion reopens only its cross-file root
ok 2604 - selected Done Pomodoro transclusion reopens only its cross-file root
  ---
  duration_ms: 6.395249
  ...
# Subtest: selected same-file Done target reopens root-only in the live editor
ok 2605 - selected same-file Done target reopens root-only in the live editor
  ---
  duration_ms: 1.327333
  ...
# Subtest: selected retired link reopens its root and restores the historical occurrence
ok 2606 - selected retired link reopens its root and restores the historical occurrence
  ---
  duration_ms: 1.100521
  ...
# Subtest: incomplete selected Pomodoro transclusion still closes recursively
ok 2607 - incomplete selected Pomodoro transclusion still closes recursively
  ---
  duration_ms: 2.030605
  ...
# Subtest: Done Pomodoro reopens direct roots and clears only its block-link markers
ok 2608 - Done Pomodoro reopens direct roots and clears only its block-link markers
  ---
  duration_ms: 3.420129
  ...
# Subtest: Done Pomodoro reopen restores its own block reference after reopening direct roots
ok 2609 - Done Pomodoro reopen restores its own block reference after reopening direct roots
  ---
  duration_ms: 0.84324
  ...
# Subtest: Done Pomodoro markers remain when the Todo transition does not occur
ok 2610 - Done Pomodoro markers remain when the Todo transition does not occur
  ---
  duration_ms: 0.28824
  ...
# Subtest: registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
ok 2611 - registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
  ---
  duration_ms: 11.711055
  ...
# Subtest: registered Ctrl+Enter immediately recovers a same-file dependent
ok 2612 - registered Ctrl+Enter immediately recovers a same-file dependent
  ---
  duration_ms: 10.371237
  ...
# Subtest: registered Ctrl+Enter immediately recovers a cross-file dependent
ok 2613 - registered Ctrl+Enter immediately recovers a cross-file dependent
  ---
  duration_ms: 2.818029
  ...
# Subtest: child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
ok 2614 - child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
  ---
  duration_ms: 3.193247
  ...
# Subtest: Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
ok 2615 - Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
  ---
  duration_ms: 1.216953
  ...
# Subtest: selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
ok 2616 - selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
  ---
  duration_ms: 2.229826
  ...
# Subtest: selected unresolved or excluded embedded children are consumed as no-ops
ok 2617 - selected unresolved or excluded embedded children are consumed as no-ops
  ---
  duration_ms: 0.869751
  ...
# Subtest: Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
ok 2618 - Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
  ---
  duration_ms: 2.655598
  ...
# Subtest: Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
ok 2619 - Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
  ---
  duration_ms: 2.520321
  ...
# Subtest: Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
ok 2620 - Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
  ---
  duration_ms: 0.825225
  ...
# Subtest: Pomodoro Work Log note-group collection scopes to direct children and requires descendants
ok 2621 - Pomodoro Work Log note-group collection scopes to direct children and requires descendants
  ---
  duration_ms: 0.815557
  ...
# Subtest: Work Log entry body formats as *date* — summary
ok 2622 - Work Log entry body formats as *date* — summary
  ---
  duration_ms: 0.131
  ...
# Subtest: buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
ok 2623 - buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
  ---
  duration_ms: 0.231622
  ...
# Subtest: planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
ok 2624 - planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
  ---
  duration_ms: 0.362622
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
ok 2625 - planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
  ---
  duration_ms: 0.303659
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
ok 2626 - planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
  ---
  duration_ms: 0.185074
  ...
# Subtest: planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
ok 2627 - planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
  ---
  duration_ms: 0.367071
  ...
# Subtest: planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
ok 2628 - planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
  ---
  duration_ms: 0.380075
  ...
# Subtest: full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
ok 2629 - full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
  ---
  duration_ms: 6.157013
  ...
# Subtest: full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
ok 2630 - full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
  ---
  duration_ms: 1.436442
  ...
# Subtest: full Pomodoro completion keeps two same-task Work Log note sets in source order
ok 2631 - full Pomodoro completion keeps two same-task Work Log note sets in source order
  ---
  duration_ms: 1.085222
  ...
# Subtest: full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
ok 2632 - full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
  ---
  duration_ms: 0.776352
  ...
# Subtest: full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
ok 2633 - full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
  ---
  duration_ms: 0.905048
  ...
# Subtest: full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
ok 2634 - full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
  ---
  duration_ms: 0.481119
  ...
# Subtest: PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
ok 2635 - PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
  ---
  duration_ms: 1.573764
  ...
# Subtest: PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
ok 2636 - PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
  ---
  duration_ms: 0.913473
  ...
# Subtest: PP1 links the emptied project's ^prj as Next and strips \#hide
ok 2637 - PP1 links the emptied project's ^prj as Next and strips \#hide
  ---
  duration_ms: 10.227272
  ...
# Subtest: PP29 closing a child ^prj pulls in its empty parent project
ok 2638 - PP29 closing a child ^prj pulls in its empty parent project
  ---
  duration_ms: 2.113393
  ...
# Subtest: PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
ok 2639 - PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
  ---
  duration_ms: 1.290764
  ...
# Subtest: PP30 keeps the parent untouched while another child or task remains
ok 2640 - PP30 keeps the parent untouched while another child or task remains
  ---
  duration_ms: 1.038072
  ...
# Subtest: PP31 skips missing, ambiguous, and non-project parents
ok 2641 - PP31 skips missing, ambiguous, and non-project parents
  ---
  duration_ms: 1.346701
  ...
# Subtest: PP33 cancellation surfaces the parent without linking it
ok 2642 - PP33 cancellation surfaces the parent without linking it
  ---
  duration_ms: 3.244663
  ...
# Subtest: PP2 and PP3 leave a project with remaining work alone
ok 2643 - PP2 and PP3 leave a project with remaining work alone
  ---
  duration_ms: 1.976022
  ...
# Subtest: PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
ok 2644 - PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
  ---
  duration_ms: 2.502858
  ...
# Subtest: PP6 Sub-projects marker states match display_for_wikilink
ok 2645 - PP6 Sub-projects marker states match display_for_wikilink
  ---
  duration_ms: 1.519971
  ...
# Subtest: PP7 and PP28 keep a future-scheduled ^prj byte-identical
ok 2646 - PP7 and PP28 keep a future-scheduled ^prj byte-identical
  ---
  duration_ms: 1.190232
  ...
# Subtest: PP8 still-blocks a ^prj that waits on another open prerequisite
ok 2647 - PP8 still-blocks a ^prj that waits on another open prerequisite
  ---
  duration_ms: 0.788776
  ...
# Subtest: PP9 already-planned ^prj raises to Next without a new link
ok 2648 - PP9 already-planned ^prj raises to Next without a new link
  ---
  duration_ms: 0.609103
  ...
# Subtest: PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
ok 2649 - PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
  ---
  duration_ms: 2.009676
  ...
# Subtest: PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
ok 2650 - PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
  ---
  duration_ms: 0.640092
  ...
# Subtest: PP14 an id-less last task still pulls in
ok 2651 - PP14 an id-less last task still pulls in
  ---
  duration_ms: 0.383642
  ...
# Subtest: PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
ok 2652 - PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
  ---
  duration_ms: 10.202505
  ...
# Subtest: PP17 one pull-in row wins over project_task
ok 2653 - PP17 one pull-in row wins over project_task
  ---
  duration_ms: 0.676692
  ...
# Subtest: PP18 cancel recovers only
ok 2654 - PP18 cancel recovers only
  ---
  duration_ms: 0.360879
  ...
# Subtest: PP20 unrecognised or unplannable notes never pull in
ok 2655 - PP20 unrecognised or unplannable notes never pull in
  ---
  duration_ms: 1.129997
  ...
# Subtest: PP24 closing an external prerequisite pulls in only when N is empty
ok 2656 - PP24 closing an external prerequisite pulls in only when N is empty
  ---
  duration_ms: 1.006482
  ...
# Subtest: PP25 cascades project_member recovery after a [?] pull-in
ok 2657 - PP25 cascades project_member recovery after a [?] pull-in
  ---
  duration_ms: 1.202515
  ...
# Subtest: PP26 dated recount treats a hidden leftover as remaining work
ok 2658 - PP26 dated recount treats a hidden leftover as remaining work
  ---
  duration_ms: 0.740283
  ...
# Subtest: PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
ok 2659 - PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
  ---
  duration_ms: 2.771951
  ...
# Subtest: successorNoticeText uses the §12.6 pull-in and surfaced copy
ok 2660 - successorNoticeText uses the §12.6 pull-in and surfaced copy
  ---
  duration_ms: 0.472171
  ...
# Subtest: Ctrl+Enter on the last task link inserts the ^prj and rewrites R
ok 2661 - Ctrl+Enter on the last task link inserts the ^prj and rewrites R
  ---
  duration_ms: 10.544979
  ...
# Subtest: PP29 runtime close and reopen use the parent pull-in receipt
ok 2662 - PP29 runtime close and reopen use the parent pull-in receipt
  ---
  duration_ms: 5.077692
  ...
# Subtest: PP18 Alt+[ cancel of the last task surfaces R without linking
ok 2663 - PP18 Alt+[ cancel of the last task surfaces R without linking
  ---
  duration_ms: 15.12905
  ...
# Subtest: PP19 same-day reopen restores R byte-for-byte and takes back the link
ok 2664 - PP19 same-day reopen restores R byte-for-byte and takes back the link
  ---
  duration_ms: 3.715192
  ...
# Subtest: a close in a project that still has work stays inside the gate
ok 2665 - a close in a project that still has work stays inside the gate
  ---
  duration_ms: 1.11559
  ...
# Subtest: P1 path-qualified skip keys: same ^review in another note does not suppress
ok 2666 - P1 path-qualified skip keys: same ^review in another note does not suppress
  ---
  duration_ms: 0.516526
  ...
# Subtest: P3 id-less cascade: stale [?] R recovers resident without [id::]
ok 2667 - P3 id-less cascade: stale [?] R recovers resident without [id::]
  ---
  duration_ms: 1.622637
  ...
# Subtest: P4 frontmatter scheduled validity mirrors Rust
ok 2668 - P4 frontmatter scheduled validity mirrors Rust
  ---
  duration_ms: 0.554107
  ...
# Subtest: P5 recognition mirrors Rust (status/type/prj line)
ok 2669 - P5 recognition mirrors Rust (status/type/prj line)
  ---
  duration_ms: 1.360487
  ...
# Subtest: P6 SUBOPEN blank line stops the marker scan (PP6)
ok 2670 - P6 SUBOPEN blank line stops the marker scan (PP6)
  ---
  duration_ms: 0.390926
  ...
# Subtest: promotion prompts default to Tasks in ordinary and project notes
ok 2671 - promotion prompts default to Tasks in ordinary and project notes
  ---
  duration_ms: 5.624898
  ...
# Subtest: promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
ok 2672 - promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
  ---
  duration_ms: 1.429138
  ...
# Subtest: promotion command writes only on accept and Enter selects Tasks
ok 2673 - promotion command writes only on accept and Enter selects Tasks
  ---
  duration_ms: 4.41648
  ...
# Subtest: promotion removes only genuinely empty source sections
ok 2674 - promotion removes only genuinely empty source sections
  ---
  duration_ms: 1.953409
  ...
# Subtest: promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
ok 2675 - promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
  ---
  duration_ms: 1.420592
  ...
# Subtest: Tasks-only preamble promotions prompt and blank Enter moves into Tasks
ok 2676 - Tasks-only preamble promotions prompt and blank Enter moves into Tasks
  ---
  duration_ms: 1.375967
  ...
# Subtest: plain bullets already in Tasks prompt and blank Enter promotes in place
ok 2677 - plain bullets already in Tasks prompt and blank Enter promotes in place
  ---
  duration_ms: 1.406805
  ...
# Subtest: promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
ok 2678 - promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
  ---
  duration_ms: 0.678695
  ...
# Subtest: always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
ok 2679 - always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
  ---
  duration_ms: 4.469031
  ...
# Could not restore all reopened task references [ 'Broken.md: unreadable' ]
# Could not recover all blocked dependents [
#   'BrokenRead.md: read failed',
#   'Stale.md: line 1 changed before recovery',
#   'BrokenWrite.md: write failed'
# ]
# Subtest: direct Done Tasks task reopens through the metadata-aware fallback
ok 2680 - direct Done Tasks task reopens through the metadata-aware fallback
  ---
  duration_ms: 2.446059
  ...
# Subtest: recursive completion status policy includes Next without broadening excluded statuses
ok 2681 - recursive completion status policy includes Next without broadening excluded statuses
  ---
  duration_ms: 0.406025
  ...
# Subtest: recursive completion closes a Next root and its nested Next descendant
ok 2682 - recursive completion closes a Next root and its nested Next descendant
  ---
  duration_ms: 3.791698
  ...
# Subtest: recursive completion traverses Done parents and skips excluded siblings
ok 2683 - recursive completion traverses Done parents and skips excluded siblings
  ---
  duration_ms: 1.353072
  ...
# Subtest: closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
ok 2684 - closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
  ---
  duration_ms: 1.558565
  ...
# Subtest: reopened-reference restoration is ancestry-aware, conservative, and idempotent
ok 2685 - reopened-reference restoration is ancestry-aware, conservative, and idempotent
  ---
  duration_ms: 1.548756
  ...
# Subtest: retirement preserves task-tree markers and unmarks Pomodoro embeds
ok 2686 - retirement preserves task-tree markers and unmarks Pomodoro embeds
  ---
  duration_ms: 0.398841
  ...
# Subtest: done Pomodoro retirement removes only the matching embedded marker
ok 2687 - done Pomodoro retirement removes only the matching embedded marker
  ---
  duration_ms: 0.270657
  ...
# Subtest: retirement stops at prose boundaries and pairs strikethrough spans
ok 2688 - retirement stops at prose boundaries and pairs strikethrough spans
  ---
  duration_ms: 0.413389
  ...
# Subtest: retired Pomodoro links are not copied into the next Pomodoro
ok 2689 - retired Pomodoro links are not copied into the next Pomodoro
  ---
  duration_ms: 1.24156
  ...
# Subtest: retirement coordinator rewrites active editor and vault notes together
ok 2690 - retirement coordinator rewrites active editor and vault notes together
  ---
  duration_ms: 1.00581
  ...
# Subtest: restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
ok 2691 - restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
  ---
  duration_ms: 1.260666
  ...
# Subtest: close and reopen reference mutations share one serialized queue
ok 2692 - close and reopen reference mutations share one serialized queue
  ---
  duration_ms: 0.266468
  ...
# Subtest: post-close finalizer runs one gated plan before reference retirement
ok 2693 - post-close finalizer runs one gated plan before reference retirement
  ---
  duration_ms: 0.504142
  ...
# Subtest: dependent recovery uses live editor buffers and preserves the cursor
ok 2694 - dependent recovery uses live editor buffers and preserves the cursor
  ---
  duration_ms: 2.868265
  ...
# Subtest: dependent recovery preserves successful siblings across stale and failed notes
ok 2695 - dependent recovery preserves successful siblings across stale and failed notes
  ---
  duration_ms: 1.309439
  ...
# Subtest: no-op vault transforms and irrelevant retirement files avoid process writes
ok 2696 - no-op vault transforms and irrelevant retirement files avoid process writes
  ---
  duration_ms: 0.294402
  ...
# Subtest: ambiguity scans and notices are cached while dependency identity lines stay stable
ok 2697 - ambiguity scans and notices are cached while dependency identity lines stay stable
  ---
  duration_ms: 0.533819
  ...
# Subtest: non-Vim open/done command finalizes the closed task identity
ok 2698 - non-Vim open/done command finalizes the closed task identity
  ---
  duration_ms: 0.384153
  ...
# Subtest: non-Vim open/done command restores the reopened task identity
ok 2699 - non-Vim open/done command restores the reopened task identity
  ---
  duration_ms: 0.349207
  ...
# Subtest: full Pomodoro completion retires embeds only after carry-forward planning
ok 2700 - full Pomodoro completion retires embeds only after carry-forward planning
  ---
  duration_ms: 6.609538
  ...
# Subtest: full Pomodoro completion recovers after a deduplicated multi-target batch
ok 2701 - full Pomodoro completion recovers after a deduplicated multi-target batch
  ---
  duration_ms: 6.864934
  ...
# Subtest: full Pomodoro completion moves a marked same-note link without history
ok 2702 - full Pomodoro completion moves a marked same-note link without history
  ---
  duration_ms: 0.642546
  ...
# Subtest: SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
ok 2703 - SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
  ---
  duration_ms: 19.835143
  ...
# Subtest: SO2–SO5 fan-outs with explicit selection (SO32 twenty)
ok 2704 - SO2–SO5 fan-outs with explicit selection (SO32 twenty)
  ---
  duration_ms: 6.870605
  ...
# Subtest: SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
ok 2705 - SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
  ---
  duration_ms: 1.132301
  ...
# Subtest: SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
ok 2706 - SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
  ---
  duration_ms: 1.243484
  ...
# Subtest: SO stable keys survive insertions/status changes; ambiguous rebinding refused
ok 2707 - SO stable keys survive insertions/status changes; ambiguous rebinding refused
  ---
  duration_ms: 2.141527
  ...
# Subtest: SO picker model, pick normalization, and API detection
ok 2708 - SO picker model, pick normalization, and API detection
  ---
  duration_ms: 0.685278
  ...
# Subtest: SO notice copy for offers (SO20, mixed, failure)
ok 2709 - SO notice copy for offers (SO20, mixed, failure)
  ---
  duration_ms: 0.523018
  ...
# Subtest: destination override to an existing entry inserts as its child
ok 2710 - destination override to an existing entry inserts as its child
  ---
  duration_ms: 2.41518
  ...
# Subtest: destination override with a stale preimage skips loudly
ok 2711 - destination override with a stale preimage skips loudly
  ---
  duration_ms: 0.952439
  ...
# Subtest: destination override with a closed entry skips loudly
ok 2712 - destination override with a closed entry skips loudly
  ---
  duration_ms: 0.908374
  ...
# Subtest: destination override with a new name creates one placeholder after the running entry
ok 2713 - destination override with a new name creates one placeholder after the running entry
  ---
  duration_ms: 0.814675
  ...
# Subtest: destination override with a new name racing an open entry joins it
ok 2714 - destination override with a new name racing an open entry joins it
  ---
  duration_ms: 0.671552
  ...
# Subtest: reopen takes back the untouched successor link and restores status
ok 2715 - reopen takes back the untouched successor link and restores status
  ---
  duration_ms: 22.158167
  ...
# Subtest: an edited successor bullet survives while its status still restores
ok 2716 - an edited successor bullet survives while its status still restores
  ---
  duration_ms: 3.692468
  ...
# Subtest: an edited successor status line survives while its link is taken back
ok 2717 - an edited successor status line survives while its link is taken back
  ---
  duration_ms: 3.952485
  ...
# Subtest: reopen on a different day leaves successor links alone
ok 2718 - reopen on a different day leaves successor links alone
  ---
  duration_ms: 2.179981
  ...
# Subtest: reopening a task closed without a pass shows no take-back
ok 2719 - reopening a task closed without a pass shows no take-back
  ---
  duration_ms: 1.465828
  ...
# Subtest: Alt+] on a planned prerequisite links its successor
ok 2720 - Alt+] on a planned prerequisite links its successor
  ---
  duration_ms: 12.012189
  ...
# Subtest: take-back deletes a pre-existing entry it empties
ok 2721 - take-back deletes a pre-existing entry it empties
  ---
  duration_ms: 3.093757
  ...
# Subtest: take-back deletes a stub-replaced entry through the vault
ok 2722 - take-back deletes a stub-replaced entry through the vault
  ---
  duration_ms: 0.447434
  ...
# Subtest: take-back keeps entries that are closed or keep another child
ok 2723 - take-back keeps entries that are closed or keep another child
  ---
  duration_ms: 0.386247
  ...
# Subtest: closing-entry relocation finds a deferred-only placeholder
ok 2724 - closing-entry relocation finds a deferred-only placeholder
  ---
  duration_ms: 0.486529
  ...
# Subtest: Alt+[ into Cancelled recovers its dependents without linking
ok 2725 - Alt+[ into Cancelled recovers its dependents without linking
  ---
  duration_ms: 3.131888
  ...
# Subtest: link close links the unblocked successor into the slot and shows the nav card
ok 2726 - link close links the unblocked successor into the slot and shows the nav card
  ---
  duration_ms: 22.532632
  ...
# Subtest: close with no [id::] performs zero vault reads and shows nothing
ok 2727 - close with no [id::] performs zero vault reads and shows nothing
  ---
  duration_ms: 1.537645
  ...
# Subtest: Warm finalize reads no unrelated note bodies on the real close path
ok 2728 - Warm finalize reads no unrelated note bodies on the real close path
  ---
  duration_ms: 3.988433
  ...
# Subtest: cold fallback still recovers and links without a Tasks cache
ok 2729 - cold fallback still recovers and links without a Tasks cache
  ---
  duration_ms: 4.681156
  ...
# Subtest: recovered-only close reports unblocked without linking (SO4 Esc)
ok 2730 - recovered-only close reports unblocked without linking (SO4 Esc)
  ---
  duration_ms: 2.212744
  ...
# Subtest: walk landing composes a single toast and shows no card
ok 2731 - walk landing composes a single toast and shows no card
  ---
  duration_ms: 9.563185
  ...
# Subtest: nav absent falls back to a plain Notice with no link (SO missing picker)
ok 2732 - nav absent falls back to a plain Notice with no link (SO missing picker)
  ---
  duration_ms: 2.222853
  ...
# Subtest: stale cache heals via re-plan from fresh text (SO30)
ok 2733 - stale cache heals via re-plan from fresh text (SO30)
  ---
  duration_ms: 2.659778
  ...
# Subtest: Pomodoro-line close appends the successor to the created continuation
ok 2734 - Pomodoro-line close appends the successor to the created continuation
  ---
  duration_ms: 7.300204
  ...
# Subtest: Pomodoro-line close keeps the closing anchor after the picker re-plan
ok 2735 - Pomodoro-line close keeps the closing anchor after the picker re-plan
  ---
  duration_ms: 3.245246
  ...
# Subtest: completeTaskAtCursor returns the notice and shows nothing itself
ok 2736 - completeTaskAtCursor returns the notice and shows nothing itself
  ---
  duration_ms: 2.652764
  ...
# Subtest: successor apply recovers project residents without ledger v12
ok 2737 - successor apply recovers project residents without ledger v12
  ---
  duration_ms: 13.252537
  ...
# Subtest: SB vectors pin the successor mint pipeline
ok 2738 - SB vectors pin the successor mint pipeline
  ---
  duration_ms: 2.60382
  ...
# Subtest: successor suggester ports the Rust candidate and suffix rules
ok 2739 - successor suggester ports the Rust candidate and suffix rules
  ---
  duration_ms: 0.682894
  ...
# Subtest: successor link form names unique basenames short and the day file always
ok 2740 - successor link form names unique basenames short and the day file always
  ---
  duration_ms: 0.906601
  ...
# Subtest: tasksFromDocuments normalizes vault lines to pool shape
ok 2741 - tasksFromDocuments normalizes vault lines to pool shape
  ---
  duration_ms: 1.41448
  ...
# Subtest: normalizeTasksCacheTask ports every known Tasks shape
ok 2742 - normalizeTasksCacheTask ports every known Tasks shape
  ---
  duration_ms: 0.459628
  ...
# Subtest: buildDependentsIndex keeps first task IDs and groups dependents
ok 2743 - buildDependentsIndex keeps first task IDs and groups dependents
  ---
  duration_ms: 0.232244
  ...
# Subtest: findLiveLinks counts plain, embedded, and deferred links under open entries only
ok 2744 - findLiveLinks counts plain, embedded, and deferred links under open entries only
  ---
  duration_ms: 3.146427
  ...
# Subtest: computeSuccessorAnchors implements closing, slot, inherit, and none
ok 2745 - computeSuccessorAnchors implements closing, slot, inherit, and none
  ---
  duration_ms: 1.064762
  ...
# Subtest: SL1 links the successor right after the predecessor bullet
ok 2746 - SL1 links the successor right after the predecessor bullet
  ---
  duration_ms: 5.858653
  ...
# Subtest: SL3 still-blocked rows count the open prerequisites left
ok 2747 - SL3 still-blocked rows count the open prerequisites left
  ---
  duration_ms: 1.011782
  ...
# Subtest: SL4 future-scheduled dependents stay Blocked with the date row
ok 2748 - SL4 future-scheduled dependents stay Blocked with the date row
  ---
  duration_ms: 0.689296
  ...
# Subtest: SL5 already-planned dependents recover without a duplicate link
ok 2749 - SL5 already-planned dependents recover without a duplicate link
  ---
  duration_ms: 1.108326
  ...
# Subtest: SL6 struck and closed-entry links do not count as planned
ok 2750 - SL6 struck and closed-entry links do not count as planned
  ---
  duration_ms: 1.679817
  ...
# Subtest: SL7 closing anchors create the continuation placeholder
ok 2751 - SL7 closing anchors create the continuation placeholder
  ---
  duration_ms: 1.139826
  ...
# Subtest: SL8 closing anchors append after carried lines in the continuation
ok 2752 - SL8 closing anchors append after carried lines in the continuation
  ---
  duration_ms: 0.942058
  ...
# Subtest: SL9 unplanned predecessors offer at the implicit destination (SO14)
ok 2753 - SL9 unplanned predecessors offer at the implicit destination (SO14)
  ---
  duration_ms: 1.282578
  ...
# Subtest: SL10 missing block IDs mint through the SB rule
ok 2754 - SL10 missing block IDs mint through the SB rule
  ---
  duration_ms: 0.520123
  ...
# Subtest: SL11 project and hidden tasks recover but never link
ok 2755 - SL11 project and hidden tasks recover but never link
  ---
  duration_ms: 9.084111
  ...
# Subtest: PDC1 leaves a dependency-ready resident Blocked while its project still waits
ok 2756 - PDC1 leaves a dependency-ready resident Blocked while its project still waits
  ---
  duration_ms: 2.110439
  ...
# Subtest: PDC2 residents are offered under the project group (SO1)
ok 2757 - PDC2 residents are offered under the project group (SO1)
  ---
  duration_ms: 1.374354
  ...
# Subtest: PDC3 keeps a project resident Blocked when its own prerequisite remains open
ok 2758 - PDC3 keeps a project resident Blocked when its own prerequisite remains open
  ---
  duration_ms: 0.852888
  ...
# Subtest: PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
ok 2759 - PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
  ---
  duration_ms: 2.348914
  ...
# Subtest: SL12 one gesture closing two prerequisites links once with both causes
ok 2760 - SL12 one gesture closing two prerequisites links once with both causes
  ---
  duration_ms: 0.687372
  ...
# Subtest: SL13 chains do not recurse: the dependent's own dependents wait
ok 2761 - SL13 chains do not recurse: the dependent's own dependents wait
  ---
  duration_ms: 0.440671
  ...
# Subtest: SL14 ambiguous basenames link long
ok 2762 - SL14 ambiguous basenames link long
  ---
  duration_ms: 0.404772
  ...
# Subtest: SL15 stale open dependents link and become Next
ok 2763 - SL15 stale open dependents link and become Next
  ---
  duration_ms: 0.491177
  ...
# Subtest: SL16 gates on [id::]: no identity means no lookup and empty rows
ok 2764 - SL16 gates on [id::]: no identity means no lookup and empty rows
  ---
  duration_ms: 0.294583
  ...
# Subtest: SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
ok 2765 - SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
  ---
  duration_ms: 1.877434
  ...
# Subtest: SL18 the kill switch recovers without linking or minting
ok 2766 - SL18 the kill switch recovers without linking or minting
  ---
  duration_ms: 0.370026
  ...
# Subtest: SL19 re-applied closes write nothing and report nothing
ok 2767 - SL19 re-applied closes write nothing and report nothing
  ---
  duration_ms: 0.334348
  ...
# Subtest: SL23 subtasks anchor at their root's link
ok 2768 - SL23 subtasks anchor at their root's link
  ---
  duration_ms: 0.400825
  ...
# Subtest: SL24 later same-name entries take the closing successors
ok 2769 - SL24 later same-name entries take the closing successors
  ---
  duration_ms: 0.56568
  ...
# Subtest: SL25 already-Next planned dependents produce no row
ok 2770 - SL25 already-Next planned dependents produce no row
  ---
  duration_ms: 0.474465
  ...
# Subtest: SL26 inbox successors carry the inbox flag
ok 2771 - SL26 inbox successors carry the inbox flag
  ---
  duration_ms: 0.368574
  ...
# Subtest: SL27 dropped links are never re-linked and recover to Ready
ok 2772 - SL27 dropped links are never re-linked and recover to Ready
  ---
  duration_ms: 0.433237
  ...
# Subtest: SL28 day-file successors name the note, never the bare link
ok 2773 - SL28 day-file successors name the note, never the bare link
  ---
  duration_ms: 0.330261
  ...
# Subtest: slot insertions land after the anchor subtree with its indent
ok 2774 - slot insertions land after the anchor subtree with its indent
  ---
  duration_ms: 0.241311
  ...
# Subtest: closing insertions replace a lone stub child
ok 2775 - closing insertions replace a lone stub child
  ---
  duration_ms: 0.526094
  ...
# Subtest: insertions skip placements with no valid target
ok 2776 - insertions skip placements with no valid target
  ---
  duration_ms: 0.15182
  ...
# Subtest: successorNoticeText implements the §12.6 table
ok 2777 - successorNoticeText implements the §12.6 table
  ---
  duration_ms: 0.545932
  ...
# Subtest: parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
ok 2778 - parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
  ---
  duration_ms: 0.427385
  ...
# Subtest: loadLinkUnblocked stat-caches the config read
ok 2779 - loadLinkUnblocked stat-caches the config read
  ---
  duration_ms: 0.343345
  ...
# Subtest: loadLinkUnblocked treats missing or unreadable config as true
ok 2780 - loadLinkUnblocked treats missing or unreadable config as true
  ---
  duration_ms: 1.28895
  ...
# Subtest: successorPlanConfigPath honors XDG_CONFIG_HOME
ok 2781 - successorPlanConfigPath honors XDG_CONFIG_HOME
  ---
  duration_ms: 0.192698
  ...
# Subtest: todayDailyPath mirrors the ledger daily path
ok 2782 - todayDailyPath mirrors the ledger daily path
  ---
  duration_ms: 0.522908
  ...
# Subtest: normalizeClosedTaskIdentities keeps the anchor root off the match gate
ok 2783 - normalizeClosedTaskIdentities keeps the anchor root off the match gate
  ---
  duration_ms: 0.234508
  ...
# Subtest: ID-less planned roots anchor ID-bearing children without minting IDs
ok 2784 - ID-less planned roots anchor ID-bearing children without minting IDs
  ---
  duration_ms: 0.710476
  ...
# Subtest: successor anchors never guess across roots
ok 2785 - successor anchors never guess across roots
  ---
  duration_ms: 0.410143
  ...
# Subtest: a child with its own live link keeps its own slot
ok 2786 - a child with its own live link keeps its own slot
  ---
  duration_ms: 0.370688
  ...
# Subtest: getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
ok 2787 - getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
  ---
  duration_ms: 0.244486
  ...
# Subtest: countSuccessorBasenames walks the vault set, not the task set
ok 2788 - countSuccessorBasenames walks the vault set, not the task set
  ---
  duration_ms: 0.333627
  ...
# Subtest: the pass threads a richer isInbox into unblocked rows
ok 2789 - the pass threads a richer isInbox into unblocked rows
  ---
  duration_ms: 0.388923
  ...
# Subtest: getTaskLinkLaneApi returns the lane only when version and both functions exist
ok 2790 - getTaskLinkLaneApi returns the lane only when version and both functions exist
  ---
  duration_ms: 1.36192
  ...
# Subtest: isTaskLinkLaneLine passes content, line, and path and never throws
ok 2791 - isTaskLinkLaneLine passes content, line, and path and never throws
  ---
  duration_ms: 1.423787
  ...
# Subtest: single Alt+] on a Task Link delegates with exactly { editor, view }
ok 2792 - single Alt+] on a Task Link delegates with exactly { editor, view }
  ---
  duration_ms: 0.663046
  ...
# Subtest: Alt+[ and Alt+] delegate identically; direction is ignored
ok 2793 - Alt+[ and Alt+] delegate identically; direction is ignored
  ---
  duration_ms: 0.454778
  ...
# Subtest: embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
ok 2794 - embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
  ---
  duration_ms: 0.429549
  ...
# Subtest: entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
ok 2795 - entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
  ---
  duration_ms: 4.501814
  ...
# Subtest: counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
ok 2796 - counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
  ---
  duration_ms: 0.912743
  ...
# Subtest: counted dispatch without an explicit repeat leaves the key alone
ok 2797 - counted dispatch without an explicit repeat leaves the key alone
  ---
  duration_ms: 0.29365
  ...
# Subtest: counted range starting elsewhere skips Task Link lines
ok 2798 - counted range starting elsewhere skips Task Link lines
  ---
  duration_ms: 2.502186
  ...
# Subtest: legacy fallback with no api keeps today's behavior
ok 2799 - legacy fallback with no api keeps today's behavior
  ---
  duration_ms: 1.030968
  ...
# Subtest: plain Task Link in an open Pomodoro closes the task root-only and strikes the link
ok 2800 - plain Task Link in an open Pomodoro closes the task root-only and strikes the link
  ---
  duration_ms: 16.650904
  ...
# Subtest: marked plain Task Link drops its marker when struck under Pomodoro ancestry
ok 2801 - marked plain Task Link drops its marker when struck under Pomodoro ancestry
  ---
  duration_ms: 1.949612
  ...
# Subtest: plain Pomodoro Task Link closes root-only while embedded closes recursively
ok 2802 - plain Pomodoro Task Link closes root-only while embedded closes recursively
  ---
  duration_ms: 2.966893
  ...
# Subtest: embedded Pomodoro Task Link still closes recursively and retires to struck form
ok 2803 - embedded Pomodoro Task Link still closes recursively and retires to struck form
  ---
  duration_ms: 2.655599
  ...
# Subtest: Ctrl+Enter toggles a struck plain Pomodoro link back to open
ok 2804 - Ctrl+Enter toggles a struck plain Pomodoro link back to open
  ---
  duration_ms: 1.893545
  ...
# Subtest: same-file plain Task Link closes and strikes the correct line
ok 2805 - same-file plain Task Link closes and strikes the correct line
  ---
  duration_ms: 1.317786
  ...
# Subtest: cursor selects which of several Task Links closes and strikes
ok 2806 - cursor selects which of several Task Links closes and strikes
  ---
  duration_ms: 1.439657
  ...
# Subtest: plain links to Blocked or non-task blocks still complete the Pomodoro
ok 2807 - plain links to Blocked or non-task blocks still complete the Pomodoro
  ---
  duration_ms: 4.287754
  ...
# Subtest: strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
ok 2808 - strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
  ---
  duration_ms: 0.58705
  ...
# Subtest: completeTaskAtCursor closes each open symbol through the Tasks command
ok 2809 - completeTaskAtCursor closes each open symbol through the Tasks command
  ---
  duration_ms: 1.761072
  ...
# Subtest: completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
ok 2810 - completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
  ---
  duration_ms: 0.378833
  ...
# Subtest: completeTaskAtCursor refuses closed, cancelled, and non-task lines
ok 2811 - completeTaskAtCursor refuses closed, cancelled, and non-task lines
  ---
  duration_ms: 0.336743
  ...
# Subtest: completeTaskAtCursor refuses a missing Tasks command with no write
ok 2812 - completeTaskAtCursor refuses a missing Tasks command with no write
  ---
  duration_ms: 0.169434
  ...
# Subtest: Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
ok 2813 - Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
  ---
  duration_ms: 0.587191
  ...
# Subtest: completeTaskAtCursor reports not-closed when Tasks does not write [x]
ok 2814 - completeTaskAtCursor reports not-closed when Tasks does not write [x]
  ---
  duration_ms: 0.190183
  ...
# Subtest: recovery api is frozen at version 2 and recovers without striking references
ok 2815 - recovery api is frozen at version 2 and recovers without striking references
  ---
  duration_ms: 2.725453
  ...
# Subtest: recovery api never throws and reports failures
ok 2816 - recovery api never throws and reports failures
  ---
  duration_ms: 0.279553
  ...
# Subtest: future-scheduled dependents stay Blocked on the planner, api, and close paths
ok 2817 - future-scheduled dependents stay Blocked on the planner, api, and close paths
  ---
  duration_ms: 15.637439
  ...
# Subtest: Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
ok 2818 - Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
  ---
  duration_ms: 3.990057
  ...
# Subtest: every printable non-space ASCII key resolves to a surround pair
ok 2819 - every printable non-space ASCII key resolves to a surround pair
  ---
  duration_ms: 4.776587
  ...
# Subtest: visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
ok 2820 - visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
  ---
  duration_ms: 0.639641
  ...
# Subtest: non-visible, combining, multi-character, and multi-code-unit values are rejected
ok 2821 - non-visible, combining, multi-character, and multi-code-unit values are rejected
  ---
  duration_ms: 0.265908
  ...
# Subtest: ys adds broad symmetric delimiters through pending keydown
ok 2822 - ys adds broad symmetric delimiters through pending keydown
  ---
  duration_ms: 1.138353
  ...
# Subtest: rejected keydown input never edits or leaks into a pending ys
ok 2823 - rejected keydown input never edits or leaks into a pending ys
  ---
  duration_ms: 0.360348
  ...
# Subtest: Escape cancels ys, cs, and ds pending state without editing
ok 2824 - Escape cancels ys, cs, and ds pending state without editing
  ---
  duration_ms: 0.257602
  ...
# Subtest: cs accepts broad target and replacement characters independently
ok 2825 - cs accepts broad target and replacement characters independently
  ---
  duration_ms: 1.837979
  ...
# Subtest: cs preserves structural alias and padding rules
ok 2826 - cs preserves structural alias and padding rules
  ---
  duration_ms: 0.562494
  ...
# Subtest: cs replaces repeated symmetric runs exactly once on each side
ok 2827 - cs replaces repeated symmetric runs exactly once on each side
  ---
  duration_ms: 0.505154
  ...
# Subtest: ds removes representative broad symmetric delimiters
ok 2828 - ds removes representative broad symmetric delimiters
  ---
  duration_ms: 0.704996
  ...
# Subtest: ds preserves structural alias and padding rules
ok 2829 - ds preserves structural alias and padding rules
  ---
  duration_ms: 0.32462
  ...
# Subtest: ds removes one pair from repeated runs, including the reported block link
ok 2830 - ds removes one pair from repeated runs, including the reported block link
  ---
  duration_ms: 0.947208
  ...
# Subtest: consecutive ds commands peel a triple symmetric surround
ok 2831 - consecutive ds commands peel a triple symmetric surround
  ---
  duration_ms: 0.189452
  ...
# Subtest: symmetric discovery uses deterministic sequential same-line run pairs
ok 2832 - symmetric discovery uses deterministic sequential same-line run pairs
  ---
  duration_ms: 0.133324
  ...
# Subtest: symmetric discovery includes every character in repeated boundaries
ok 2833 - symmetric discovery includes every character in repeated boundaries
  ---
  duration_ms: 0.242272
  ...
# Subtest: unpaired and unequal symmetric runs are safe no-ops
ok 2834 - unpaired and unequal symmetric runs are safe no-ops
  ---
  duration_ms: 0.197006
  ...
# Subtest: ordinary normal-mode keys remain untouched outside pending state
ok 2835 - ordinary normal-mode keys remain untouched outside pending state
  ---
  duration_ms: 0.200001
  ...
# Subtest: dot while a surround is pending is a literal delimiter, not repeat
ok 2836 - dot while a surround is pending is a literal delimiter, not repeat
  ---
  duration_ms: 0.121211
  ...
# Subtest: dot-repeat records and replays broad-character ys
ok 2837 - dot-repeat records and replays broad-character ys
  ---
  duration_ms: 0.234568
  ...
# Subtest: dot-repeat records and replays broad-character cs
ok 2838 - dot-repeat records and replays broad-character cs
  ---
  duration_ms: 0.195122
  ...
# Subtest: dot-repeat records and replays broad-character ds
ok 2839 - dot-repeat records and replays broad-character ds
  ---
  duration_ms: 0.17795
  ...
# Subtest: dot-repeat replays cs against repeated symmetric runs
ok 2840 - dot-repeat replays cs against repeated symmetric runs
  ---
  duration_ms: 0.198228
  ...
# Subtest: dot-repeat replays ds against repeated symmetric runs
ok 2841 - dot-repeat replays ds against repeated symmetric runs
  ---
  duration_ms: 0.197808
  ...
# Subtest: consecutive dot-repeats peel a triple symmetric surround
ok 2842 - consecutive dot-repeats peel a triple symmetric surround
  ---
  duration_ms: 0.23075
  ...
1..2842
# tests 2852
# suites 0
# pass 2846
# fail 6
# cancelled 0
# skipped 0
# todo 0
# duration_ms 5298.905806
failed  exit=1  duration=11304ms

