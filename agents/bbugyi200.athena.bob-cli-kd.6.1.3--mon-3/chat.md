# Chat History - ace-run (bob-cli-kd.6.1.3--mon-3)

- **TIMESTAMP:** 2026-11-12 00:53:13 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-kd.6.1.3--mon-3

## Prompt

sase monitor start --command 'npx --yes --package=node@22 -- npm test' --reason 'Run the full bob-plugins test suite after the bank UI rollout'

## Response

sase tool run 837709786bf0f6e5c1eb31c109512369

> bob-plugins@0.1.0 test
> node scripts/build-plugins.mjs --check && npm run docs:inventory:check && { npm run test:unit; u=$?; npm run test:perf; p=$?; exit $((u||p)); }

  checked   block-id-prompt
  checked   bob-articles
  checked   bob-command-mode
  checked   bob-ledger-tools
  checked   bob-mail
  checked   bob-navigation-hotkeys
  checked   task-status-cycler

> bob-plugins@0.1.0 docs:inventory:check
> node scripts/docs-inventory.mjs --check

Plugin documentation inventory is up to date.

> bob-plugins@0.1.0 test:unit
> node --test scripts/test-navigation-leaf-switch-guard.cjs scripts/test-project-tasks-snapshot.cjs scripts/test-bob-articles.cjs scripts/test-command-mode-resolver-env.cjs scripts/test-command-mode-catalog.cjs scripts/test-command-mode-runner.cjs scripts/test-command-mode-outcomes-api.cjs scripts/test-command-mode-pager.cjs scripts/test-command-mode-args-vim.cjs scripts/test-command-mode-sheet.cjs scripts/test-command-mode-sheet-keys.cjs scripts/test-command-mode-sheet-sequence.cjs scripts/test-command-mode-sheet-sequence-dom.cjs scripts/test-command-mode-status-chip.cjs scripts/test-command-mode-sequence-engine.cjs scripts/test-command-mode-sequence-feedback.cjs scripts/test-navigation-hotkeys-section-nav.cjs scripts/test-navigation-hotkeys-rename.cjs scripts/test-navigation-delete-guard.cjs scripts/test-navigation-copy-card-model.cjs scripts/test-navigation-copy-card-view.cjs scripts/test-navigation-hotkeys-ref-pdf.cjs scripts/test-navigation-hotkeys-ref-pdf-page.cjs scripts/test-navigation-ref-annotation-locator.cjs scripts/test-navigation-highlights-notice.cjs scripts/test-navigation-highlights-hints.cjs scripts/test-navigation-hotkeys-templater-trigger.cjs scripts/test-navigation-hotkeys-schedule-recovery.cjs scripts/test-navigation-hotkeys-schedule-properties.cjs scripts/test-navigation-hotkeys-schedule-writes.cjs scripts/test-navigation-hotkeys-runtime-schedule.cjs scripts/test-navigation-hotkeys-dependencies.cjs scripts/test-navigation-blocks-guards.cjs scripts/test-navigation-blocks-writers.cjs scripts/test-navigation-blocks-edit.cjs scripts/test-navigation-blocks-stage-view.cjs scripts/test-navigation-hotkeys-dependency-mirror.cjs scripts/test-navigation-hotkeys-task-move-plan.cjs scripts/test-navigation-hotkeys-priority-notice.cjs scripts/test-navigation-successor-picker.cjs scripts/test-navigation-successor-verdicts.cjs scripts/test-navigation-image-zoom-viewer.cjs scripts/test-navigation-image-zoom-origin.cjs scripts/test-navigation-image-zoom-path.cjs scripts/test-navigation-hotkeys-unblocked-notice.cjs scripts/test-navigation-hotkeys-offer-close-apis.cjs scripts/test-navigation-project-blocking.cjs scripts/test-navigation-project-dependency-stage.cjs scripts/test-navigation-project-subprojects.cjs scripts/test-navigation-project-subtree-gestures.cjs scripts/test-navigation-hotkeys-priority-picker.cjs scripts/test-navigation-hotkeys-picker-lifecycle.cjs scripts/test-navigation-hotkeys-ref-picker-text.cjs scripts/test-navigation-hotkeys-pomodoro-move-pickers.cjs scripts/test-navigation-inbox-route.cjs scripts/test-navigation-inbox-route-card.cjs scripts/test-navigation-hotkeys-task-move.cjs scripts/test-navigation-open-notes-uri.cjs scripts/test-navigation-parent-change.cjs scripts/test-navigation-hotkeys-dash-open.cjs scripts/test-navigation-goto-task-uri.cjs scripts/test-navigation-hotkeys-open-task-jump.cjs scripts/test-navigation-hotkeys-vim-counts.cjs scripts/test-navigation-hotkeys-tab-pin.cjs scripts/test-navigation-hotkeys-schedule-log.cjs scripts/test-navigation-hotkeys-schedule-review.cjs scripts/test-navigation-hotkeys-deferred-pomodoro.cjs scripts/test-navigation-hotkeys-pomodoro-parse.cjs scripts/test-navigation-hotkeys-pomodoro-bullet-move.cjs scripts/test-navigation-hotkeys-pomodoro-split-rename.cjs scripts/test-navigation-hotkeys-pomodoro-split.cjs scripts/test-navigation-hotkeys-pomodoro-themes-manager.cjs scripts/test-navigation-hotkeys-pomodoro-reorder.cjs scripts/test-navigation-hotkeys-runtime-prune.cjs scripts/test-navigation-hotkeys-project-from-task.cjs scripts/test-navigation-hotkeys-project-reversal.cjs scripts/test-navigation-hotkeys-link-picker.cjs scripts/test-navigation-hotkeys-lane-toggle.cjs scripts/test-navigation-hotkeys-task-link-lane.cjs scripts/test-navigation-hotkeys-cancel-log.cjs scripts/test-navigation-hotkeys-cancel-task.cjs scripts/test-navigation-hotkeys-forward-promotion.cjs scripts/test-navigation-hotkeys-promotion-verdicts.cjs scripts/test-navigation-hotkeys-schedule-work-log.cjs scripts/test-navigation-hotkeys-work-log-stamp-closeout.cjs scripts/test-navigation-hotkeys-task-move-history.cjs scripts/test-navigation-jump-history.cjs scripts/test-navigation-dependencies.cjs scripts/test-navigation-editor-line-diff.cjs scripts/test-navigation-quick-roll.cjs scripts/test-navigation-quick-roll-preview.cjs scripts/test-navigation-roll-decay.cjs scripts/test-navigation-decay-planner.cjs scripts/test-navigation-task-card-model.cjs scripts/test-navigation-task-card-view.cjs scripts/test-navigation-task-card-theme-edit.cjs scripts/test-navigation-task-card-schedule.cjs scripts/test-navigation-task-card-review.cjs scripts/test-navigation-decision-card.cjs scripts/test-navigation-decision-card-handlers.cjs scripts/test-navigation-decision-card-keep.cjs scripts/test-navigation-refresh-modal.cjs scripts/test-navigation-freshness.cjs scripts/test-navigation-review-groups.cjs scripts/test-navigation-stamps.cjs scripts/test-navigation-keep-counting.cjs scripts/test-navigation-rotten-keep.cjs scripts/test-navigation-rotten-log.cjs scripts/test-navigation-checklist.cjs scripts/test-navigation-review-advance.cjs scripts/test-navigation-review-advance-gestures.cjs scripts/test-navigation-checklist-ctrl-enter.cjs scripts/test-ledger-tools-navigation.cjs scripts/test-ledger-tools-plan-budget.cjs scripts/test-ledger-tools-plan-budget-off-clock.cjs scripts/test-ledger-tools-plan-today-roots.cjs scripts/test-ledger-tools-ready-badge.cjs scripts/test-ledger-tools-note-ready.cjs scripts/test-ledger-tools-note-ready-views.cjs scripts/test-ledger-tools-dashboard-parity.cjs scripts/test-ledger-tools-work-badge-tone.cjs scripts/test-ledger-tools-dashboard-collections.cjs scripts/test-ledger-tools-today.cjs scripts/test-ledger-tools-period-notes.cjs scripts/test-ledger-tools-gcal-events.cjs scripts/test-ledger-tools-event-link-times.cjs scripts/test-ledger-tools-meet-event-run.cjs scripts/test-ledger-tools-pomodoro-clock.cjs scripts/test-ledger-tools-freshness-placement.cjs scripts/test-ledger-tools-freshness-states.cjs scripts/test-ledger-tools-freshness-namespace.cjs scripts/test-ledger-tools-freshness-review-model.cjs scripts/test-ledger-tools-freshness-queue.cjs scripts/test-ledger-tools-freshness-stages.cjs scripts/test-ledger-tools-freshness-tracking.cjs scripts/test-ledger-tools-freshness-footer.cjs scripts/test-ledger-tools-keep-inbox.cjs scripts/test-ledger-tools-freshness-recurring.cjs scripts/test-ledger-tools-freshness-mark.cjs scripts/test-ledger-tools-freshness-mark-surfaces.cjs scripts/test-ledger-tools-priority-marks.cjs scripts/test-ledger-tools-block-marks.cjs scripts/test-ledger-tools-block-marks-contrast.cjs scripts/test-ledger-tools-block-marks-editor.cjs scripts/test-ledger-tools-block-marks-reading.cjs scripts/test-ledger-tools-mail-link-marks.cjs scripts/test-ledger-tools-no-reply-pills.cjs scripts/test-ledger-tools-task-tag-marks.cjs scripts/test-ledger-tools-task-link-marks.cjs scripts/test-ledger-tools-task-link-marks-live.cjs scripts/test-ledger-tools-task-link-marks-reading.cjs scripts/test-ledger-tools-task-type-identity.cjs scripts/test-ledger-tools-today-marks.cjs scripts/test-ledger-tools-today-marks-reading.cjs scripts/test-ledger-tools-unblocked-glyph.cjs scripts/test-ledger-tools-frees-marks.cjs scripts/test-ledger-tools-off-clock-link-chips.cjs scripts/test-ledger-tools-progress-marks.cjs scripts/test-ledger-tools-keep-moving-marks.cjs scripts/test-ledger-tools-keep-moving-render.cjs scripts/test-ledger-tools-keep-moving-marks-surface.cjs scripts/test-ledger-tools-date-marks.cjs scripts/test-ledger-tools-recurrence-marks.cjs scripts/test-ledger-tools-date-marks-tasks.cjs scripts/test-ledger-tools-freshness-keeps.cjs scripts/test-ledger-tools-freshness-unblocked.cjs scripts/test-ledger-tools-freshness-decision-card.cjs scripts/test-ledger-tools-dependency-chips.cjs scripts/test-ledger-tools-blocks-chips.cjs scripts/test-ledger-tools-command-mode-refresh.cjs scripts/test-ledger-tools-snippets.cjs scripts/test-ledger-tools-vim-mappings.cjs scripts/test-task-status-cycler-dependencies.cjs scripts/test-task-status-cycler-blocks-guards.cjs scripts/test-task-status-cycler-complete-vectors.cjs scripts/test-task-status-cycler-bank-guard.cjs scripts/test-task-status-cycler-ctrl-enter.cjs scripts/test-task-status-cycler-event-task-close.cjs scripts/test-task-status-cycler-reference-lifecycle.cjs scripts/test-task-status-cycler-pomodoro-completion.cjs scripts/test-task-status-cycler-pomodoro-clock.cjs scripts/test-task-status-cycler-pomodoro-work-log.cjs scripts/test-task-status-cycler-pomodoro-reopen.cjs scripts/test-task-status-cycler-blocked-schedule.cjs scripts/test-task-status-cycler-demotion-picker.cjs scripts/test-task-status-cycler-event-ledger-guard.cjs scripts/test-task-status-cycler-promotion.cjs scripts/test-task-status-cycler-promotion-verdicts.cjs scripts/test-task-status-cycler-counted-toggle.cjs scripts/test-task-status-cycler-successors.cjs scripts/test-task-status-cycler-successor-wiring.cjs scripts/test-task-status-cycler-successor-polish.cjs scripts/test-task-status-cycler-keep-moving.cjs scripts/test-keep-moving-marks-parity.cjs scripts/test-task-status-cycler-relation-successors.cjs scripts/test-task-status-cycler-parked-successors.cjs scripts/test-task-status-cycler-successor-offers.cjs scripts/test-task-status-cycler-successor-verdicts.cjs scripts/test-task-status-cycler-successor-apply.cjs scripts/test-task-status-cycler-successor-theme-write.cjs scripts/test-task-status-cycler-project-pull-in.cjs scripts/test-task-status-cycler-task-links-api.cjs scripts/test-task-status-cycler-task-link-lane.cjs scripts/test-task-status-cycler-freshness.cjs scripts/test-block-id-prompt-dependencies.cjs scripts/test-block-id-prompt-blocks-guards.cjs scripts/test-block-id-prompt-ref-picker-text.cjs scripts/test-block-id-prompt-markers.cjs scripts/test-block-id-prompt-pomodoro-context.cjs scripts/test-block-id-prompt-target-update.cjs scripts/test-block-id-prompt-pomodoro-insertion.cjs scripts/test-block-id-prompt-pomodoro-targets.cjs scripts/test-block-id-prompt-pomodoro-picker-view.cjs scripts/test-block-id-prompt-pomodoro-picker-runtime.cjs scripts/test-block-id-prompt-work-log.cjs scripts/test-block-id-prompt-pomodoro-link-runtime.cjs scripts/test-block-id-prompt-pomodoro-theme-write.cjs scripts/test-block-id-prompt-pomodoro-link-picker-api.cjs scripts/test-block-id-prompt-pomodoro-unlink-runtime.cjs scripts/test-block-id-prompt-parked-successors.cjs scripts/test-block-id-prompt-task-link-deletion.cjs scripts/test-block-id-prompt-task-wikilink-model.cjs scripts/test-block-id-prompt-task-wikilink-token.cjs scripts/test-block-id-prompt-task-wikilink-index.cjs scripts/test-block-id-prompt-task-wikilink-picker-view.cjs scripts/test-block-id-prompt-task-wikilink-picker-runtime.cjs scripts/test-block-id-prompt-task-wikilink-naming.cjs scripts/test-block-id-prompt-task-wikilink-pomodoro.cjs scripts/test-block-id-prompt-plan-budget-and-freshness.cjs scripts/test-prompt-block-id-naming.cjs scripts/test-block-id-prompt-prefill.cjs scripts/test-block-id-prompt-rename-atomic.cjs scripts/test-vim-surround.cjs scripts/test-vim-yank-flash.cjs scripts/test-navigation-dependencies-stage-ranker-and-pool.cjs scripts/test-navigation-dependencies-stage-entry-and-view.cjs scripts/test-navigation-dependencies-stage-writes.cjs scripts/test-navigation-dependencies-stage-mirror-and-badge.cjs scripts/test-navigation-dependencies-stage-stale-guards.cjs scripts/test-navigation-dependencies-stage-performance.cjs scripts/test-navigation-prompt-block-id-stage.cjs scripts/test-navigation-dependencies-writer.cjs scripts/test-navigation-dependency-link-consumption.cjs scripts/test-plugin-build.cjs scripts/test-ledger-tools-stats-journal.cjs scripts/test-ledger-tools-stats-clocks.cjs scripts/test-ledger-tools-stats-data.cjs scripts/test-ledger-tools-stats-block.cjs scripts/test-ledger-tools-stats-charts.cjs scripts/test-ledger-tools-stats-clock-charts.cjs scripts/test-navigation-review-journal.cjs scripts/test-ledger-tools-stats-panels.cjs scripts/test-ledger-tools-stats-lanes.cjs scripts/test-ledger-tools-reading-board-data.cjs scripts/test-ledger-tools-notebooks-data.cjs scripts/test-ledger-tools-bank-decode.cjs scripts/test-ledger-tools-bank-source.cjs scripts/test-ledger-tools-bank-data.cjs scripts/test-ledger-tools-bank-actions.cjs scripts/test-ledger-tools-notebook-catalog.cjs scripts/test-ledger-tools-notebook-header.cjs scripts/test-ledger-tools-reading-board-models.cjs scripts/test-ledger-tools-reading-board-block.cjs scripts/test-ledger-tools-pomodoro-home-chips.cjs scripts/test-ledger-tools-pomodoro-themes.cjs scripts/test-ledger-tools-task-theme-marks.cjs scripts/test-ledger-tools-task-theme-rendered.cjs scripts/test-navigation-image-zoom-target.cjs scripts/test-navigation-image-zoom-command.cjs scripts/test-done-archive-path.cjs scripts/test-docs-inventory.mjs scripts/test-docs-check.mjs scripts/test-navigation-relation-lines.cjs scripts/test-navigation-relation-mentions.cjs scripts/test-navigation-relation-writer.cjs scripts/test-navigation-task-cancel-vectors.cjs scripts/test-navigation-task-split-vectors.cjs scripts/test-navigation-task-split-gesture.cjs scripts/test-navigation-relation-cancel-writer.cjs scripts/test-navigation-relation-complete-writer.cjs scripts/test-navigation-relation-complete-vectors.cjs scripts/test-navigation-relation-links-stage.cjs scripts/test-navigation-relation-merge.cjs scripts/test-navigation-relation-successor-vectors.cjs scripts/test-navigation-relation-stage-render.cjs scripts/test-relation-index-linked-from-stage.cjs scripts/test-ledger-tools-relations.cjs scripts/test-ledger-tools-task-merge.cjs scripts/test-ledger-tools-notebooks-api.cjs scripts/test-navigation-notebook-gestures.cjs scripts/test-ledger-tools-relation-index.cjs scripts/test-ledger-tools-attachments-api.cjs scripts/test-ledger-tools-relation-mentions.cjs scripts/test-ledger-tools-relation-chips.cjs scripts/test-task-status-cycler-relations.cjs scripts/test-task-status-cycler-restore.cjs scripts/test-block-id-prompt-relations.cjs scripts/test-ledger-tools-day-strip.cjs scripts/test-ledger-tools-day-strip-themes.cjs scripts/test-ledger-tools-day-strip-plan-host.cjs scripts/test-ledger-tools-period-strip.cjs scripts/test-ledger-tools-period-strip-charts.cjs scripts/test-ledger-tools-period-parts.cjs scripts/test-ledger-tools-fakenode-inspect.cjs scripts/test-ledger-tools-day-strip-lanes.cjs scripts/test-ledger-tools-day-strip-hosts.cjs scripts/test-obsidian-startup-smoke.cjs scripts/test-obsidian-notebook-ui-e2e.cjs scripts/test-obsidian-task-wikilink-e2e.cjs scripts/test-obsidian-block-id-rename-e2e.cjs scripts/test-obsidian-task-link-marks-e2e.cjs scripts/test-obsidian-block-marks-e2e.cjs scripts/test-obsidian-frees-marks-e2e.cjs scripts/test-obsidian-keep-moving-marks-e2e.cjs scripts/test-obsidian-off-clock-link-chips-e2e.cjs scripts/test-obsidian-event-link-times-e2e.cjs scripts/test-obsidian-decay-ladder-e2e.cjs scripts/test-obsidian-quick-roll-e2e.cjs scripts/test-task-link-marks-motion.cjs scripts/test-ledger-tools-lane-walk.cjs scripts/test-navigation-lane-walk.cjs scripts/test-ledger-tools-root-marks.cjs scripts/test-navigation-bracket-repeat.cjs scripts/test-navigation-period-links.cjs scripts/test-navigation-bracket-mode-indicator.cjs scripts/test-navigation-lane-inbox-route.cjs scripts/test-navigation-review-due-row.cjs scripts/test-bob-mail.cjs scripts/test-bob-mail-compose.cjs scripts/test-navigation-reload-history.cjs scripts/test-obsidian-redo-history-e2e.cjs scripts/test-obsidian-vim-yank-flash-e2e.cjs scripts/test-obsidian-copy-card-e2e.cjs scripts/test-ledger-tools-bank-cards.cjs

TAP version 13
# Subtest: bip BK1–BK12 accept and empty
ok 1 - bip BK1–BK12 accept and empty
  ---
  duration_ms: 2.967868
  type: 'test'
  ...
# Subtest: bip BK13–BK15 malformed split mirrors the Depends-On twin
ok 2 - bip BK13–BK15 malformed split mirrors the Depends-On twin
  ---
  duration_ms: 0.626938
  type: 'test'
  ...
# Subtest: bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
ok 3 - bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
  ---
  duration_ms: 0.156769
  type: 'test'
  ...
# Subtest: bip MC1/MC2 Pomodoro scanners skip managed lines
ok 4 - bip MC1/MC2 Pomodoro scanners skip managed lines
  ---
  duration_ms: 3.466691
  type: 'test'
  ...
# Subtest: explicit task IDs exclusively own dependency lookup
ok 5 - explicit task IDs exclusively own dependency lookup
  ---
  duration_ms: 7.114077
  type: 'test'
  ...
# Subtest: legacy tasks without an id field still fall back to their block ID
ok 6 - legacy tasks without an id field still fall back to their block ID
  ---
  duration_ms: 0.499224
  type: 'test'
  ...
# Subtest: blocked-link consumption raises open prerequisites and leaves the dependent blocked
ok 7 - blocked-link consumption raises open prerequisites and leaves the dependent blocked
  ---
  duration_ms: 1.62873
  type: 'test'
  ...
# Subtest: project-blocked member consumption promotes the project's open prerequisite
ok 8 - project-blocked member consumption promotes the project's open prerequisite
  ---
  duration_ms: 1.004989
  type: 'test'
  ...
# Subtest: project-blocked resident consumption promotes the project's open prerequisite
ok 9 - project-blocked resident consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.663727
  type: 'test'
  ...
# Subtest: a tagged inherited ^prj target is refused with its parent named
ok 10 - a tagged inherited ^prj target is refused with its parent named
  ---
  duration_ms: 0.524832
  type: 'test'
  ...
# Subtest: project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
ok 11 - project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
  ---
  duration_ms: 1.045206
  type: 'test'
  ...
# Subtest: project date refusal applies only when the date is the sole project reason
ok 12 - project date refusal applies only when the date is the sole project reason
  ---
  duration_ms: 0.45048
  type: 'test'
  ...
# Subtest: a project-blocked tag is token-bounded and ignored on lookalike tags
ok 13 - a project-blocked tag is token-bounded and ignored on lookalike tags
  ---
  duration_ms: 0.597131
  type: 'test'
  ...
# Subtest: task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
ok 14 - task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
  ---
  duration_ms: 1.040217
  type: 'test'
  ...
# Subtest: task blocked state unifies status and dependency reasons
ok 15 - task blocked state unifies status and dependency reasons
  ---
  duration_ms: 0.414973
  type: 'test'
  ...
# Subtest: task picker partition sinks blocked tasks while preserving group order
ok 16 - task picker partition sinks blocked tasks while preserving group order
  ---
  duration_ms: 0.301125
  type: 'test'
  ...
# Subtest: blocked chip labels show useful unmet dependency counts
ok 17 - blocked chip labels show useful unmet dependency counts
  ---
  duration_ms: 0.166127
  type: 'test'
  ...
# Subtest: blocked tooltips explain dependency and status-only reasons
ok 18 - blocked tooltips explain dependency and status-only reasons
  ---
  duration_ms: 0.358835
  type: 'test'
  ...
# Subtest: task status classes cover every open task status
ok 19 - task status classes cover every open task status
  ---
  duration_ms: 0.151619
  type: 'test'
  ...
# Subtest: Blocked tasks remain unmet dependency targets
ok 20 - Blocked tasks remain unmet dependency targets
  ---
  duration_ms: 0.248665
  type: 'test'
  ...
# Subtest: blocked task count covers both reasons without double-counting
ok 21 - blocked task count covers both reasons without double-counting
  ---
  duration_ms: 0.203819
  type: 'test'
  ...
# Subtest: single caret relocation preserves embedding and removes aliases
ok 22 - single caret relocation preserves embedding and removes aliases
  ---
  duration_ms: 2.481369
  type: 'test'
  ...
# Subtest: single caret relocation resets aliased block links
ok 23 - single caret relocation resets aliased block links
  ---
  duration_ms: 2.924164
  type: 'test'
  ...
# Subtest: single caret relocation strips heading and block subpaths
ok 24 - single caret relocation strips heading and block subpaths
  ---
  duration_ms: 0.420833
  type: 'test'
  ...
# Subtest: task picker normalizes every supported wiki block-link form
ok 25 - task picker normalizes every supported wiki block-link form
  ---
  duration_ms: 0.91659
  type: 'test'
  ...
# Subtest: three or more carets never trigger the task picker
ok 26 - three or more carets never trigger the task picker
  ---
  duration_ms: 0.209269
  type: 'test'
  ...
# Subtest: rapid aliased task picker completion preserves the alias
ok 27 - rapid aliased task picker completion preserves the alias
  ---
  duration_ms: 3.858579
  type: 'test'
  ...
# Subtest: task picker recognition is independent of Markdown source context
ok 28 - task picker recognition is independent of Markdown source context
  ---
  duration_ms: 0.884389
  type: 'test'
  ...
# Subtest: task picker recognition respects cursor proximity and fenced code
ok 29 - task picker recognition respects cursor proximity and fenced code
  ---
  duration_ms: 0.33996
  type: 'test'
  ...
# Subtest: SA33 settled Unlink task prompt offers parked successors with the removed slot
ok 30 - SA33 settled Unlink task prompt offers parked successors with the removed slot
  ---
  duration_ms: 9.969299
  type: 'test'
  ...
# Subtest: SA33 Esc on Unlink task offers nothing
ok 31 - SA33 Esc on Unlink task offers nothing
  ---
  duration_ms: 0.569217
  type: 'test'
  ...
# Subtest: non-Pending unlink stays silent even with a live cycler
ok 32 - non-Pending unlink stays silent even with a live cycler
  ---
  duration_ms: 0.971185
  type: 'test'
  ...
# Subtest: older cycler api v3 is silence
ok 33 - older cycler api v3 is silence
  ---
  duration_ms: 0.66478
  type: 'test'
  ...
# Subtest: In Progress unlink with no removed links does not offer
ok 34 - In Progress unlink with no removed links does not offer
  ---
  duration_ms: 0.500576
  type: 'test'
  ...
# Subtest: Task Link Unlink of a Pending target offers parked successors
ok 35 - Task Link Unlink of a Pending target offers parked successors
  ---
  duration_ms: 3.341412
  type: 'test'
  ...
# Subtest: plan budget suffix: link Notice appends the meter computed on post-write daily content
ok 36 - plan budget suffix: link Notice appends the meter computed on post-write daily content
  ---
  duration_ms: 10.847629
  type: 'test'
  ...
# Subtest: plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
ok 37 - plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
  ---
  duration_ms: 1.862387
  type: 'test'
  ...
# Subtest: plan budget suffix: unlink Notice marks an over-cap plan with 🔴
ok 38 - plan budget suffix: unlink Notice marks an over-cap plan with 🔴
  ---
  duration_ms: 2.982106
  type: 'test'
  ...
# Subtest: plan budget suffix: Next task without a block ID prompts for one and omits the meter
ok 39 - plan budget suffix: Next task without a block ID prompts for one and omits the meter
  ---
  duration_ms: 0.632528
  type: 'test'
  ...
# Subtest: plan budget suffix: Task Link Notice appends the meter from post-write daily content
ok 40 - plan budget suffix: Task Link Notice appends the meter from post-write daily content
  ---
  duration_ms: 3.093849
  type: 'test'
  ...
# Subtest: plan budget suffix: Task Link Notice omits the meter when no daily note takes part
ok 41 - plan budget suffix: Task Link Notice omits the meter when no daily note takes part
  ---
  duration_ms: 0.811079
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate stamps the rewritten line last via injected stamper
ok 42 - planTargetTaskUpdate stamps the rewritten line last via injected stamper
  ---
  duration_ms: 0.563376
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate without a stamper never stamps (identity default)
ok 43 - planTargetTaskUpdate without a stamper never stamps (identity default)
  ---
  duration_ms: 0.423208
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
ok 44 - planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
  ---
  duration_ms: 0.493343
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate stamps a Next task that gains a block ID
ok 45 - planTargetTaskUpdate stamps a Next task that gains a block ID
  ---
  duration_ms: 0.748469
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate tolerates a throwing stamper
ok 46 - planTargetTaskUpdate tolerates a throwing stamper
  ---
  duration_ms: 0.297368
  type: 'test'
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 47 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.735946
  type: 'test'
  ...
# Subtest: dedicated-link helpers reject Depends-On lines
ok 48 - dedicated-link helpers reject Depends-On lines
  ---
  duration_ms: 0.396768
  type: 'test'
  ...
# Subtest: Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
ok 49 - Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
  ---
  duration_ms: 0.480668
  type: 'test'
  ...
# Subtest: malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
ok 50 - malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
  ---
  duration_ms: 0.175946
  type: 'test'
  ...
# Subtest: Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
ok 51 - Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
  ---
  duration_ms: 0.352524
  type: 'test'
  ...
# Subtest: Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
ok 52 - Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
  ---
  duration_ms: 0.283862
  type: 'test'
  ...
# Subtest: readPlanBudgetMeter ignores stale theme meters and follows links only
ok 53 - readPlanBudgetMeter ignores stale theme meters and follows links only
  ---
  duration_ms: 0.168201
  type: 'test'
  ...
# Subtest: readPlanBudgetMeter marks an over-link plan red
ok 54 - readPlanBudgetMeter marks an over-link plan red
  ---
  duration_ms: 0.108367
  type: 'test'
  ...
# Subtest: block-id-prompt freshness accessors degrade without ledger-tools
ok 55 - block-id-prompt freshness accessors degrade without ledger-tools
  ---
  duration_ms: 0.299181
  type: 'test'
  ...
# Subtest: block-id-prompt refuses Pomodoro ledger lines before calling a stamper
ok 56 - block-id-prompt refuses Pomodoro ledger lines before calling a stamper
  ---
  duration_ms: 0.287178
  type: 'test'
  ...
# Subtest: list item body bounds trim whitespace and reject empty bullets
ok 57 - list item body bounds trim whitespace and reject empty bullets
  ---
  duration_ms: 3.662264
  type: 'test'
  ...
# Subtest: Pomodoro activation eligibility requires a sole-content sub-bullet
ok 58 - Pomodoro activation eligibility requires a sole-content sub-bullet
  ---
  duration_ms: 2.691791
  type: 'test'
  ...
# Subtest: Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
ok 59 - Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
  ---
  duration_ms: 0.412598
  type: 'test'
  ...
# Subtest: Pomodoro source context distinguishes ledger ancestry and open state
ok 60 - Pomodoro source context distinguishes ledger ancestry and open state
  ---
  duration_ms: 0.625625
  type: 'test'
  ...
# Subtest: the open-Pomodoro task-link gate recognizes both ^^ and (( sources
ok 61 - the open-Pomodoro task-link gate recognizes both ^^ and (( sources
  ---
  duration_ms: 2.389534
  type: 'test'
  ...
# Subtest: future cleanup touches only later open Pomodoros and counts duplicates
ok 62 - future cleanup touches only later open Pomodoros and counts duplicates
  ---
  duration_ms: 2.336773
  type: 'test'
  ...
# Subtest: cleanup resolves aliases, embeds, same-note links, and alternate paths
ok 63 - cleanup resolves aliases, embeds, same-note links, and alternate paths
  ---
  duration_ms: 1.018856
  type: 'test'
  ...
# Subtest: dedicated bullet subtree cleanup preserves CRLF line endings
ok 64 - dedicated bullet subtree cleanup preserves CRLF line endings
  ---
  duration_ms: 0.441203
  type: 'test'
  ...
# Subtest: existing-ID task completion prunes future links in the source editor
ok 65 - existing-ID task completion prunes future links in the source editor
  ---
  duration_ms: 4.635043
  type: 'test'
  ...
# Subtest: new-ID same-file completion plans cleanup after the task edit
ok 66 - new-ID same-file completion plans cleanup after the task edit
  ---
  duration_ms: 2.029055
  type: 'test'
  ...
# Subtest: findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
ok 67 - findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
  ---
  duration_ms: 3.140859
  type: 'test'
  ...
# Subtest: findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
ok 68 - findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
  ---
  duration_ms: 0.245198
  type: 'test'
  ...
# Subtest: findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
ok 69 - findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
  ---
  duration_ms: 0.227744
  type: 'test'
  ...
# Subtest: todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
ok 70 - todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
  ---
  duration_ms: 0.632278
  type: 'test'
  ...
# Subtest: todayDailyPath honors a custom Daily Notes format and an empty folder
ok 71 - todayDailyPath honors a custom Daily Notes format and an empty folder
  ---
  duration_ms: 0.310162
  type: 'test'
  ...
# Subtest: formatDailyDate resolves bracketed literal text alongside date tokens
ok 72 - formatDailyDate resolves bracketed literal text alongside date tokens
  ---
  duration_ms: 0.175926
  type: 'test'
  ...
# Subtest: getDailyNotesOptions reads the daily-notes core plugin's configured options
ok 73 - getDailyNotesOptions reads the daily-notes core plugin's configured options
  ---
  duration_ms: 0.988248
  type: 'test'
  ...
# Subtest: computeFencedLineFlags marks opening and closing fence lines and everything between
ok 74 - computeFencedLineFlags marks opening and closing fence lines and everything between
  ---
  duration_ms: 0.329519
  type: 'test'
  ...
# Subtest: selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
ok 75 - selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
  ---
  duration_ms: 0.93159
  type: 'test'
  ...
# Subtest: selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
ok 76 - selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
  ---
  duration_ms: 0.599014
  type: 'test'
  ...
# Subtest: selectPomodoroInsertionTarget rejects more than one open timed entry
ok 77 - selectPomodoroInsertionTarget rejects more than one open timed entry
  ---
  duration_ms: 0.280917
  type: 'test'
  ...
# Subtest: selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
ok 78 - selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
  ---
  duration_ms: 0.215551
  type: 'test'
  ...
# Subtest: findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
ok 79 - findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
  ---
  duration_ms: 0.21474
  type: 'test'
  ...
# Subtest: planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
ok 80 - planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
  ---
  duration_ms: 1.890541
  type: 'test'
  ...
# Subtest: planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
ok 81 - planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
  ---
  duration_ms: 1.838591
  type: 'test'
  ...
# Subtest: planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
ok 82 - planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
  ---
  duration_ms: 0.36153
  type: 'test'
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
ok 83 - planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
  ---
  duration_ms: 0.651875
  type: 'test'
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
ok 84 - planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
  ---
  duration_ms: 0.67052
  type: 'test'
  ...
# Subtest: planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
ok 85 - planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
  ---
  duration_ms: 0.423819
  type: 'test'
  ...
# Subtest: planPomodoroLinkInsertion inserts before the separator preceding later content
ok 86 - planPomodoroLinkInsertion inserts before the separator preceding later content
  ---
  duration_ms: 0.314321
  type: 'test'
  ...
# Subtest: planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
ok 87 - planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
  ---
  duration_ms: 0.304301
  type: 'test'
  ...
# Subtest: planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
ok 88 - planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
  ---
  duration_ms: 0.470319
  type: 'test'
  ...
# Subtest: existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
ok 89 - existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
  ---
  duration_ms: 5.155357
  type: 'test'
  ...
# Subtest: same-note Pomodoro link runtime composes the task update with adjacent insertion
ok 90 - same-note Pomodoro link runtime composes the task update with adjacent insertion
  ---
  duration_ms: 1.788516
  type: 'test'
  ...
# Subtest: new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
ok 91 - new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
  ---
  duration_ms: 1.077227
  type: 'test'
  ...
# Subtest: planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
ok 92 - planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
  ---
  duration_ms: 0.463966
  type: 'test'
  ...
# Subtest: all-open cleanup removes current and future links while preserving history and unresolved links
ok 93 - all-open cleanup removes current and future links while preserving history and unresolved links
  ---
  duration_ms: 1.274675
  type: 'test'
  ...
# Subtest: all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
ok 94 - all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
  ---
  duration_ms: 1.512729
  type: 'test'
  ...
# Subtest: all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
ok 95 - all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
  ---
  duration_ms: 0.319179
  type: 'test'
  ...
# Subtest: all-open cleanup treats missing section, no open entries, and no matches as no-op successes
ok 96 - all-open cleanup treats missing section, no open entries, and no matches as no-op successes
  ---
  duration_ms: 0.265246
  type: 'test'
  ...
# Subtest: composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
ok 97 - composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
  ---
  duration_ms: 0.299983
  type: 'test'
  ...
# Subtest: pomodoro link picker choices normalize to existing/new or null
ok 98 - pomodoro link picker choices normalize to existing/new or null
  ---
  duration_ms: 3.586259
  type: 'test'
  ...
# Subtest: pomodoroLinkPicker api never rejects and validates choices
ok 99 - pomodoroLinkPicker api never rejects and validates choices
  ---
  duration_ms: 0.618572
  type: 'test'
  ...
# Subtest: destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
ok 100 - destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
  ---
  duration_ms: 0.784489
  type: 'test'
  ...
# Subtest: destination pick with a section releases its guards when the modal cannot open
ok 101 - destination pick with a section releases its guards when the modal cannot open
  ---
  duration_ms: 2.13114
  type: 'test'
  ...
# Subtest: public pick accepts one-based full-note task context and suggests once
ok 102 - public pick accepts one-based full-note task context and suggests once
  ---
  duration_ms: 1.918164
  type: 'test'
  ...
# Subtest: public pick without task context stays generic; missing themes degrades safely
ok 103 - public pick without task context stays generic; missing themes degrades safely
  ---
  duration_ms: 0.844974
  type: 'test'
  ...
# Subtest: plugin lifecycle installs the api and drops it on unload
ok 104 - plugin lifecycle installs the api and drops it on unload
  ---
  duration_ms: 0.814566
  type: 'test'
  ...
# Subtest: task-aware choices retain a valid themeIntent; absent intent keeps the legacy shape
ok 105 - task-aware choices retain a valid themeIntent; absent intent keeps the legacy shape
  ---
  duration_ms: 0.390556
  type: 'test'
  ...
# Subtest: malformed themeIntent is dropped so it can never enable a write
ok 106 - malformed themeIntent is dropped so it can never enable a write
  ---
  duration_ms: 0.616047
  type: 'test'
  ...
# Subtest: taskLineTextAt reads one-based lines and degrades to empty
ok 107 - taskLineTextAt reads one-based lines and degrades to empty
  ---
  duration_ms: 0.437396
  type: 'test'
  ...
# Subtest: public pick tolerates an out-of-range task line and releases its guards
ok 108 - public pick tolerates an out-of-range task line and releases its guards
  ---
  duration_ms: 0.575489
  type: 'test'
  ...
# Subtest: Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
ok 109 - Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
  ---
  duration_ms: 3.01045
  type: 'test'
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor requires a single cursor
ok 110 - resolvePomodoroLinkTaskFromEditor requires a single cursor
  ---
  duration_ms: 0.523671
  type: 'test'
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
ok 111 - resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
  ---
  duration_ms: 0.452975
  type: 'test'
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
ok 112 - resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
  ---
  duration_ms: 0.542666
  type: 'test'
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
ok 113 - resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
  ---
  duration_ms: 0.934254
  type: 'test'
  ...
# Subtest: blocked-link consumption reports dependency reasons before the project date
ok 114 - blocked-link consumption reports dependency reasons before the project date
  ---
  duration_ms: 3.318359
  type: 'test'
  ...
# Subtest: Pomodoro link checks do not read other notes for a non-Blocked task
ok 115 - Pomodoro link checks do not read other notes for a non-Blocked task
  ---
  duration_ms: 0.408811
  type: 'test'
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
ok 116 - resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
  ---
  duration_ms: 0.494264
  type: 'test'
  ...
# Subtest: task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
ok 117 - task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
  ---
  duration_ms: 8.983488
  type: 'test'
  ...
# Subtest: task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
ok 118 - task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
  ---
  duration_ms: 3.354907
  type: 'test'
  ...
# Subtest: task-mode toggle: linked only under a completed Pomodoro links again
ok 119 - task-mode toggle: linked only under a completed Pomodoro links again
  ---
  duration_ms: 1.310412
  type: 'test'
  ...
# Subtest: task-mode toggle: a task without a block ID is never linked and prompts for one
ok 120 - task-mode toggle: a task without a block ID is never linked and prompts for one
  ---
  duration_ms: 0.660381
  type: 'test'
  ...
# Subtest: existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
ok 121 - existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
  ---
  duration_ms: 1.77525
  type: 'test'
  ...
# Subtest: forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
ok 122 - forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
  ---
  duration_ms: 0.837119
  type: 'test'
  ...
# Subtest: new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
ok 123 - new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
  ---
  duration_ms: 0.807793
  type: 'test'
  ...
# Subtest: submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
ok 124 - submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
  ---
  duration_ms: 0.201194
  type: 'test'
  ...
# Subtest: submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
ok 125 - submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
  ---
  duration_ms: 0.197507
  type: 'test'
  ...
# Subtest: same-note Pomodoro link runtime: task and ledger edits merge into one transaction
ok 126 - same-note Pomodoro link runtime: task and ledger edits merge into one transaction
  ---
  duration_ms: 1.686431
  type: 'test'
  ...
# Subtest: linking an already-linked Ready task raises it to Next without duplicating the link
ok 127 - linking an already-linked Ready task raises it to Next without duplicating the link
  ---
  duration_ms: 0.679378
  type: 'test'
  ...
# Subtest: Next task without a block ID preflights the picker before prompting
ok 128 - Next task without a block ID preflights the picker before prompting
  ---
  duration_ms: 0.821339
  type: 'test'
  ...
# Subtest: Pomodoro link stops before any mutation when today's daily note is missing
ok 129 - Pomodoro link stops before any mutation when today's daily note is missing
  ---
  duration_ms: 0.242784
  type: 'test'
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
ok 130 - Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
  ---
  duration_ms: 0.772716
  type: 'test'
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
ok 131 - Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
  ---
  duration_ms: 0.392991
  type: 'test'
  ...
# Subtest: Pomodoro link aborts without any write when the task line changed since it was selected
ok 132 - Pomodoro link aborts without any write when the task line changed since it was selected
  ---
  duration_ms: 0.228506
  type: 'test'
  ...
# Subtest: Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
ok 133 - Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
  ---
  duration_ms: 1.235049
  type: 'test'
  ...
# Subtest: canceling the Pomodoro block-ID modal leaves the note untouched
ok 134 - canceling the Pomodoro block-ID modal leaves the note untouched
  ---
  duration_ms: 0.264626
  type: 'test'
  ...
# Subtest: review-walk: existing-ID link hands its Linked notice to continue with no separate notice
ok 135 - review-walk: existing-ID link hands its Linked notice to continue with no separate notice
  ---
  duration_ms: 3.412979
  type: 'test'
  ...
# Subtest: review-walk: prompted-ID link continues after submit
ok 136 - review-walk: prompted-ID link continues after submit
  ---
  duration_ms: 1.177869
  type: 'test'
  ...
# Subtest: review-walk: prompt cancel settles with null
ok 137 - review-walk: prompt cancel settles with null
  ---
  duration_ms: 0.210753
  type: 'test'
  ...
# Subtest: review-walk: BUSY swallows the key with no write
ok 138 - review-walk: BUSY swallows the key with no write
  ---
  duration_ms: 0.240719
  type: 'test'
  ...
# Subtest: review-walk: failed link keeps its notice and settles with null
ok 139 - review-walk: failed link keeps its notice and settles with null
  ---
  duration_ms: 0.264626
  type: 'test'
  ...
# Subtest: review-walk: partial link keeps its notice and never continues with an outcome
ok 140 - review-walk: partial link keeps its notice and never continues with an outcome
  ---
  duration_ms: 1.142993
  type: 'test'
  ...
# Subtest: inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
ok 141 - inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
  ---
  duration_ms: 0.35086
  type: 'test'
  ...
# Subtest: inbox-route: non-inbox notes and task-link mode never prompt
ok 142 - inbox-route: non-inbox notes and task-link mode never prompt
  ---
  duration_ms: 1.333267
  type: 'test'
  ...
# Subtest: inbox-route: cancel writes nothing and settles once
ok 143 - inbox-route: cancel writes nothing and settles once
  ---
  duration_ms: 0.539741
  type: 'test'
  ...
# Subtest: inbox-route: stay matches today
ok 144 - inbox-route: stay matches today
  ---
  duration_ms: 0.800579
  type: 'test'
  ...
# Subtest: inbox-route: move links, then moves, with one composed toast and a route continue
ok 145 - inbox-route: move links, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.960805
  type: 'test'
  ...
# Subtest: inbox-route: a new block ID goes through the route, then the picker, then the ID prompt
ok 146 - inbox-route: a new block ID goes through the route, then the picker, then the ID prompt
  ---
  duration_ms: 1.070004
  type: 'test'
  ...
# Subtest: inbox-route: a submitted ID that already exists in the destination keeps the prompt open
ok 147 - inbox-route: a submitted ID that already exists in the destination keeps the prompt open
  ---
  duration_ms: 0.522758
  type: 'test'
  ...
# Subtest: inbox-route: a move failure gives the partial notice plus a link-today continue
ok 148 - inbox-route: a move failure gives the partial notice plus a link-today continue
  ---
  duration_ms: 0.831187
  type: 'test'
  ...
# Subtest: review-walk: no nav or nav v2 keeps today's notices
ok 149 - review-walk: no nav or nav v2 keeps today's notices
  ---
  duration_ms: 1.425403
  type: 'test'
  ...
# Subtest: inbox-route: source drift during route prompt refuses without writes
ok 150 - inbox-route: source drift during route prompt refuses without writes
  ---
  duration_ms: 0.416976
  type: 'test'
  ...
# Subtest: inbox-route: route cancel up front writes nothing, opens no ID prompt, and settles null once
ok 151 - inbox-route: route cancel up front writes nothing, opens no ID prompt, and settles null once
  ---
  duration_ms: 0.305143
  type: 'test'
  ...
# Subtest: inbox-route: link no-op with move never commits
ok 152 - inbox-route: link no-op with move never commits
  ---
  duration_ms: 0.234588
  type: 'test'
  ...
# Subtest: picker opens only on the link direction, never on unlink
ok 153 - picker opens only on the link direction, never on unlink
  ---
  duration_ms: 12.755113
  type: 'test'
  ...
# Subtest: picker never opens in task-link mode
ok 154 - picker never opens in task-link mode
  ---
  duration_ms: 3.378181
  type: 'test'
  ...
# Subtest: Depends-On refusals never open the picker
ok 155 - Depends-On refusals never open the picker
  ---
  duration_ms: 1.344186
  type: 'test'
  ...
# Subtest: preflight refusals open nothing
ok 156 - preflight refusals open nothing
  ---
  duration_ms: 0.770131
  type: 'test'
  ...
# Subtest: direct picker captures one task suggestion with a one-based line and live note text
ok 157 - direct picker captures one task suggestion with a one-based line and live note text
  ---
  duration_ms: 1.365026
  type: 'test'
  ...
# Subtest: missing task-theme APIs leave the direct picker on its existing default
ok 158 - missing task-theme APIs leave the direct picker on its existing default
  ---
  duration_ms: 1.014698
  type: 'test'
  ...
# Subtest: picking a non-default entry links there
ok 159 - picking a non-default entry links there
  ---
  duration_ms: 1.789628
  type: 'test'
  ...
# Subtest: cancel writes nothing with no Notice and settles the walk null
ok 160 - cancel writes nothing with no Notice and settles the walk null
  ---
  duration_ms: 0.888157
  type: 'test'
  ...
# Subtest: a no-ID task gets picker, then the block-ID prompt with the target carried
ok 161 - a no-ID task gets picker, then the block-ID prompt with the target carried
  ---
  duration_ms: 1.546714
  type: 'test'
  ...
# Subtest: inbox order is route, then picker, then write
ok 162 - inbox order is route, then picker, then write
  ---
  duration_ms: 1.435172
  type: 'test'
  ...
# Subtest: a route cancel never opens the picker and writes nothing
ok 163 - a route cancel never opens the picker and writes nothing
  ---
  duration_ms: 0.436765
  type: 'test'
  ...
# Subtest: a routed move suggests from the destination with a one-line virtual note
ok 164 - a routed move suggests from the destination with a one-line virtual note
  ---
  duration_ms: 0.574077
  type: 'test'
  ...
# Subtest: a routed stay suggests from the inbox path
ok 165 - a routed stay suggests from the inbox path
  ---
  duration_ms: 0.704015
  type: 'test'
  ...
# Subtest: a routed move carries the destination chip and a stay carries none
ok 166 - a routed move carries the destination chip and a stay carries none
  ---
  duration_ms: 0.726087
  type: 'test'
  ...
# Subtest: a review-walk landing continues with link-today and the new text
ok 167 - a review-walk landing continues with link-today and the new text
  ---
  duration_ms: 0.820568
  type: 'test'
  ...
# Subtest: an all-closed ledger creates a new entry after the last completed block
ok 168 - an all-closed ledger creates a new entry after the last completed block
  ---
  duration_ms: 2.320102
  type: 'test'
  ...
# Subtest: several running entries allow an explicit pick
ok 169 - several running entries allow an explicit pick
  ---
  duration_ms: 0.957088
  type: 'test'
  ...
# Subtest: a target that changed before commit refuses with no writes
ok 170 - a target that changed before commit refuses with no writes
  ---
  duration_ms: 0.827851
  type: 'test'
  ...
# Subtest: a target that closed before commit refuses with no writes
ok 171 - a target that closed before commit refuses with no writes
  ---
  duration_ms: 0.521586
  type: 'test'
  ...
# Subtest: the task note being the daily note uses one editor transaction
ok 172 - the task note being the daily note uses one editor transaction
  ---
  duration_ms: 0.955465
  type: 'test'
  ...
# Subtest: promptOpen blocks re-entry while the picker is open
ok 173 - promptOpen blocks re-entry while the picker is open
  ---
  duration_ms: 17.154005
  type: 'test'
  ...
# Subtest: direct picker request carries the task line text for the footer
ok 174 - direct picker request carries the task line text for the footer
  ---
  duration_ms: 0.656604
  type: 'test'
  ...
# Subtest: direct picker stays task-aware when the live note text is unavailable
ok 175 - direct picker stays task-aware when the live note text is unavailable
  ---
  duration_ms: 0.364686
  type: 'test'
  ...
# Subtest: header shows title, subtitle, lane chip per status, and block-ID chip
ok 176 - header shows title, subtitle, lane chip per status, and block-ID chip
  ---
  duration_ms: 13.940352
  type: 'test'
  ...
# Subtest: rows render in document order with the default selected
ok 177 - rows render in document order with the default selected
  ---
  duration_ms: 1.80642
  type: 'test'
  ...
# Subtest: recent theme rows follow today's rows and render component swatches
ok 178 - recent theme rows follow today's rows and render component swatches
  ---
  duration_ms: 23.600638
  type: 'test'
  ...
# Subtest: exact recent themes suppress generic creation and preserve catalog spelling
ok 179 - exact recent themes suppress generic creation and preserve catalog spelling
  ---
  duration_ms: 6.738912
  type: 'test'
  ...
# Subtest: Ctrl+D hides a Recent suggestion as an undoable ghost and leaves Today unchanged
ok 180 - Ctrl+D hides a Recent suggestion as an undoable ghost and leaves Today unchanged
  ---
  duration_ms: 18.926246
  type: 'test'
  ...
# Subtest: new-name rows show near-duplicate and hidden-theme hints
ok 181 - new-name rows show near-duplicate and hidden-theme hints
  ---
  duration_ms: 4.611869
  type: 'test'
  ...
# Subtest: running row shows progress fraction and minutes-left meta
ok 182 - running row shows progress fraction and minutes-left meta
  ---
  duration_ms: 1.435201
  type: 'test'
  ...
# Subtest: unnamed entries render muted italic
ok 183 - unnamed entries render muted italic
  ---
  duration_ms: 0.568837
  type: 'test'
  ...
# Subtest: filtering ranks, highlights, and clearing restores the default
ok 184 - filtering ranks, highlights, and clearing restores the default
  ---
  duration_ms: 1.15174
  type: 'test'
  ...
# Subtest: create row meta and divider
ok 185 - create row meta and divider
  ---
  duration_ms: 4.824625
  type: 'test'
  ...
# Subtest: exact open names suppress the create row; prefix matches keep it
ok 186 - exact open names suppress the create row; prefix matches keep it
  ---
  duration_ms: 1.796892
  type: 'test'
  ...
# Subtest: create rows have no type budget badge
ok 187 - create rows have no type budget badge
  ---
  duration_ms: 0.86944
  type: 'test'
  ...
# Subtest: invalid rows explain the grammar and are inert on Enter
ok 188 - invalid rows explain the grammar and are inert on Enter
  ---
  duration_ms: 4.6698
  type: 'test'
  ...
# Subtest: multiple running entries show the banner, no pills, and block creation
ok 189 - multiple running entries show the banner, no pills, and block creation
  ---
  duration_ms: 1.676002
  type: 'test'
  ...
# Subtest: navigation wraps and skips non-selectable rows
ok 190 - navigation wraps and skips non-selectable rows
  ---
  duration_ms: 2.056287
  type: 'test'
  ...
# Subtest: empty state invites planning a Pomodoro
ok 191 - empty state invites planning a Pomodoro
  ---
  duration_ms: 0.38757
  type: 'test'
  ...
# Subtest: footer hints and plan meter
ok 192 - footer hints and plan meter
  ---
  duration_ms: 1.437905
  type: 'test'
  ...
# Subtest: Enter chooses the selected row; click chooses that row
ok 193 - Enter chooses the selected row; click chooses that row
  ---
  duration_ms: 1.060826
  type: 'test'
  ...
# Subtest: Shift+Enter creates; an exact open name links there instead
ok 194 - Shift+Enter creates; an exact open name links there instead
  ---
  duration_ms: 1.118426
  type: 'test'
  ...
# Subtest: Ctrl+Shift+Enter commits exactly like Enter
ok 195 - Ctrl+Shift+Enter commits exactly like Enter
  ---
  duration_ms: 0.60189
  type: 'test'
  ...
# Subtest: Escape and Ctrl+[ cancel with no choice; settle-once holds
ok 196 - Escape and Ctrl+[ cancel with no choice; settle-once holds
  ---
  duration_ms: 5.290134
  type: 'test'
  ...
# Subtest: done-today themes stay in Recent while open Today themes stay excluded
ok 197 - done-today themes stay in Recent while open Today themes stay excluded
  ---
  duration_ms: 1.614824
  type: 'test'
  ...
# Subtest: configured theme menu vectors scope Recent, preserve config order, and flag new names
ok 198 - configured theme menu vectors scope Recent, preserve config order, and flag new names
  ---
  duration_ms: 3.396056
  type: 'test'
  ...
# Subtest: configured empty-query picker shows up to twelve configured themes
ok 199 - configured empty-query picker shows up to twelve configured themes
  ---
  duration_ms: 0.380617
  type: 'test'
  ...
# Subtest: link success notice names an unconfigured theme after creating its Pomodoro
ok 200 - link success notice names an unconfigured theme after creating its Pomodoro
  ---
  duration_ms: 0.475408
  type: 'test'
  ...
# Subtest: typing done shows only the Recent DONE row and keeps catalog spelling
ok 201 - typing done shows only the Recent DONE row and keeps catalog spelling
  ---
  duration_ms: 1.972377
  type: 'test'
  ...
# Subtest: Today exclusions apply before query filtering; cancelled themes stay Recent
ok 202 - Today exclusions apply before query filtering; cancelled themes stay Recent
  ---
  duration_ms: 1.526696
  type: 'test'
  ...
# Subtest: suggested entry rows render the reason, dot, theme pill, and accessible label
ok 203 - suggested entry rows render the reason, dot, theme pill, and accessible label
  ---
  duration_ms: 1.865924
  type: 'test'
  ...
# Subtest: reading and note suggestions render their own reasons and footer phrases
ok 204 - reading and note suggestions render their own reasons and footer phrases
  ---
  duration_ms: 1.458305
  type: 'test'
  ...
# Subtest: footer previews the default merge and the explicit retype with suggestion context
ok 205 - footer previews the default merge and the explicit retype with suggestion context
  ---
  duration_ms: 3.032032
  type: 'test'
  ...
# Subtest: footer hides without task context or theme APIs
ok 206 - footer hides without task context or theme APIs
  ---
  duration_ms: 2.892104
  type: 'test'
  ...
# Subtest: footer states a keep consequence when the destination already agrees
ok 207 - footer states a keep consequence when the destination already agrees
  ---
  duration_ms: 2.071877
  type: 'test'
  ...
# Subtest: footer previews PLAN, LATER, and Tab cycling on a composite
ok 208 - footer previews PLAN, LATER, and Tab cycling on a composite
  ---
  duration_ms: 2.188089
  type: 'test'
  ...
# Subtest: footer refreshes on selection moves and hides on inert rows
ok 209 - footer refreshes on selection moves and hides on inert rows
  ---
  duration_ms: 1.051048
  type: 'test'
  ...
# Subtest: untouched refresh preserves a still-eligible suggested entry; arrivals adopt a first default
ok 210 - untouched refresh preserves a still-eligible suggested entry; arrivals adopt a first default
  ---
  duration_ms: 22.531452
  type: 'test'
  ...
# Subtest: refresh after typing preserves the user's position and initial key
ok 211 - refresh after typing preserves the user's position and initial key
  ---
  duration_ms: 5.242193
  type: 'test'
  ...
# Subtest: removed rows fall back deterministically without clearing interaction
ok 212 - removed rows fall back deterministically without clearing interaction
  ---
  duration_ms: 3.287519
  type: 'test'
  ...
# Subtest: clearing a query keeps interaction but returning home is not deliberate
ok 213 - clearing a query keeps interaction but returning home is not deliberate
  ---
  duration_ms: 1.709826
  type: 'test'
  ...
# Subtest: suggestion never recomputes on refresh and survives API changes
ok 214 - suggestion never recomputes on refresh and survives API changes
  ---
  duration_ms: 3.920158
  type: 'test'
  ...
# Subtest: deferred fetch makes an unknown suggestion eligible and settles the untouched default
ok 215 - deferred fetch makes an unknown suggestion eligible and settles the untouched default
  ---
  duration_ms: 2.878368
  type: 'test'
  ...
# Subtest: onChange adopts a newly eligible existing match only before interaction
ok 216 - onChange adopts a newly eligible existing match only before interaction
  ---
  duration_ms: 1.362111
  type: 'test'
  ...
# Subtest: refresh after arrows and after typing then clearing keeps the settled user key
ok 217 - refresh after arrows and after typing then clearing keeps the settled user key
  ---
  duration_ms: 2.148794
  type: 'test'
  ...
# Subtest: typed theme suggestion decorates the final Recent row without changing PT7 order
ok 218 - typed theme suggestion decorates the final Recent row without changing PT7 order
  ---
  duration_ms: 5.63457
  type: 'test'
  ...
# Subtest: Alt+Enter explicitly requests retype; plain commits keep the default merge
ok 219 - Alt+Enter explicitly requests retype; plain commits keep the default merge
  ---
  duration_ms: 1.019547
  type: 'test'
  ...
# Subtest: Enter, click, and Ctrl+Shift+Enter share the deliberate rule
ok 220 - Enter, click, and Ctrl+Shift+Enter share the deliberate rule
  ---
  duration_ms: 2.500455
  type: 'test'
  ...
# Subtest: Shift+Enter named commits are always deliberate
ok 221 - Shift+Enter named commits are always deliberate
  ---
  duration_ms: 1.625956
  type: 'test'
  ...
# Subtest: cancellation writes nothing even when task-aware
ok 222 - cancellation writes nothing even when task-aware
  ---
  duration_ms: 0.848952
  type: 'test'
  ...
# Subtest: Ctrl+D on the suggested create row is consumed without writes
ok 223 - Ctrl+D on the suggested create row is consumed without writes
  ---
  duration_ms: 15.405805
  type: 'test'
  ...
# Subtest: canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
ok 224 - canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
  ---
  duration_ms: 2.590458
  type: 'test'
  ...
# Subtest: canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
ok 225 - canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
  ---
  duration_ms: 0.480738
  type: 'test'
  ...
# Subtest: pomodoroLinkSelectorSlug mirrors capture slugs
ok 226 - pomodoroLinkSelectorSlug mirrors capture slugs
  ---
  duration_ms: 0.344918
  type: 'test'
  ...
# Subtest: parsePomodoroEntryParts reads canonical and legacy entry lines
ok 227 - parsePomodoroEntryParts reads canonical and legacy entry lines
  ---
  duration_ms: 1.116462
  type: 'test'
  ...
# Subtest: collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
ok 228 - collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
  ---
  duration_ms: 1.774088
  type: 'test'
  ...
# Subtest: collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
ok 229 - collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
  ---
  duration_ms: 1.232133
  type: 'test'
  ...
# Subtest: collectPomodoroLinkEntries counts links but excludes struck references
ok 230 - collectPomodoroLinkEntries counts links but excludes struck references
  ---
  duration_ms: 0.640483
  type: 'test'
  ...
# Subtest: collectPomodoroLinkEntries falls back to range text and position titles
ok 231 - collectPomodoroLinkEntries falls back to range text and position titles
  ---
  duration_ms: 0.363685
  type: 'test'
  ...
# Subtest: pomodoroRunProgress reports fractions, overtime, and midnight wrap
ok 232 - pomodoroRunProgress reports fractions, overtime, and midnight wrap
  ---
  duration_ms: 0.48169
  type: 'test'
  ...
# Subtest: buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
ok 233 - buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
  ---
  duration_ms: 1.208808
  type: 'test'
  ...
# Subtest: buildPomodoroLinkPickerRows keeps the create row for prefix matches
ok 234 - buildPomodoroLinkPickerRows keeps the create row for prefix matches
  ---
  duration_ms: 0.316935
  type: 'test'
  ...
# Subtest: buildPomodoroLinkPickerRows marks completed-only names as again
ok 235 - buildPomodoroLinkPickerRows marks completed-only names as again
  ---
  duration_ms: 0.274915
  type: 'test'
  ...
# Subtest: buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
ok 236 - buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
  ---
  duration_ms: 0.577353
  type: 'test'
  ...
# Subtest: buildPomodoroLinkPickerRows matches times, positions, and block IDs
ok 237 - buildPomodoroLinkPickerRows matches times, positions, and block IDs
  ---
  duration_ms: 0.703484
  type: 'test'
  ...
# Subtest: resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
ok 238 - resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
  ---
  duration_ms: 0.434811
  type: 'test'
  ...
# Subtest: defaultPomodoroLinkChoice returns the default entry or null
ok 239 - defaultPomodoroLinkChoice returns the default entry or null
  ---
  duration_ms: 0.25676
  type: 'test'
  ...
# Subtest: planExplicitPomodoroLinkInsertion links under a chosen existing entry
ok 240 - planExplicitPomodoroLinkInsertion links under a chosen existing entry
  ---
  duration_ms: 1.399232
  type: 'test'
  ...
# Subtest: planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
ok 241 - planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
  ---
  duration_ms: 0.460991
  type: 'test'
  ...
# Subtest: planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
ok 242 - planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
  ---
  duration_ms: 1.463245
  type: 'test'
  ...
# Subtest: planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
ok 243 - planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
  ---
  duration_ms: 0.536985
  type: 'test'
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after the running entry
ok 244 - planExplicitPomodoroLinkInsertion creates after the running entry
  ---
  duration_ms: 0.947199
  type: 'test'
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
ok 245 - planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
  ---
  duration_ms: 1.110942
  type: 'test'
  ...
# Subtest: planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
ok 246 - planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
  ---
  duration_ms: 0.280245
  type: 'test'
  ...
# Subtest: planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
ok 247 - planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
  ---
  duration_ms: 0.277139
  type: 'test'
  ...
# Subtest: planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
ok 248 - planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
  ---
  duration_ms: 0.428578
  type: 'test'
  ...
# Subtest: buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
ok 249 - buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
  ---
  duration_ms: 0.248565
  type: 'test'
  ...
# Subtest: buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
ok 250 - buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
  ---
  duration_ms: 0.233145
  type: 'test'
  ...
# Subtest: planExplicitPomodoroLinkInsertion matches mixed-case raced open names
ok 251 - planExplicitPomodoroLinkInsertion matches mixed-case raced open names
  ---
  duration_ms: 0.267551
  type: 'test'
  ...
# Subtest: buildPomodoroLinkPickerRows bounds \#N position matches
ok 252 - buildPomodoroLinkPickerRows bounds \#N position matches
  ---
  duration_ms: 0.514632
  type: 'test'
  ...
# Subtest: planPomodoroLinkInsertion without a target keeps today's behavior and shape
ok 253 - planPomodoroLinkInsertion without a target keeps today's behavior and shape
  ---
  duration_ms: 0.563747
  type: 'test'
  ...
# Subtest: buildPomodoroLinkPickerRows keeps a done-only theme in Recent
ok 254 - buildPomodoroLinkPickerRows keeps a done-only theme in Recent
  ---
  duration_ms: 1.080694
  type: 'test'
  ...
# Subtest: shared task-theme preselection vectors match the bob-cli model
ok 255 - shared task-theme preselection vectors match the bob-cli model
  ---
  duration_ms: 3.289433
  type: 'test'
  ...
# Subtest: task-theme preselection normalizes exemptions without a type cap
ok 256 - task-theme preselection normalizes exemptions without a type cap
  ---
  duration_ms: 0.227725
  type: 'test'
  ...
# Subtest: task-aware rows preselect an existing match when creation is blocked
ok 257 - task-aware rows preselect an existing match when creation is blocked
  ---
  duration_ms: 0.564268
  type: 'test'
  ...
# Subtest: task-aware typed queries keep PT7 order and only annotate the matching row
ok 258 - task-aware typed queries keep PT7 order and only annotate the matching row
  ---
  duration_ms: 0.563406
  type: 'test'
  ...
# Subtest: suggested creation uses catalog spelling and removes its duplicate Recent row
ok 259 - suggested creation uses catalog spelling and removes its duplicate Recent row
  ---
  duration_ms: 1.200503
  type: 'test'
  ...
# Subtest: theme suggestion identity ignores decorative hue and catalog flags
ok 260 - theme suggestion identity ignores decorative hue and catalog flags
  ---
  duration_ms: 2.114609
  type: 'test'
  ...
# Subtest: theme suggestion identity treats a changed declaring note as a different suggestion
ok 261 - theme suggestion identity treats a changed declaring note as a different suggestion
  ---
  duration_ms: 0.315703
  type: 'test'
  ...
# Subtest: current exempt keys distinguish valid empty configuration from unavailable caps
ok 262 - current exempt keys distinguish valid empty configuration from unavailable caps
  ---
  duration_ms: 1.778247
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate applies themeEdit after lane changes and before a new block ID
ok 263 - planTargetTaskUpdate applies themeEdit after lane changes and before a new block ID
  ---
  duration_ms: 1.202136
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate theme-only Next task never stamps freshness
ok 264 - planTargetTaskUpdate theme-only Next task never stamps freshness
  ---
  duration_ms: 0.443246
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate stamps a lane rewrite after the theme field is in place
ok 265 - planTargetTaskUpdate stamps a lane rewrite after the theme field is in place
  ---
  duration_ms: 0.526496
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate without themeEdit preserves an authored theme field
ok 266 - planTargetTaskUpdate without themeEdit preserves an authored theme field
  ---
  duration_ms: 0.219309
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate clears a theme field and keeps CRLF plus a trailing block ID
ok 267 - planTargetTaskUpdate clears a theme field and keeps CRLF plus a trailing block ID
  ---
  duration_ms: 0.257422
  type: 'test'
  ...
# Subtest: a named destination retypes the task in the same cross-note write
ok 268 - a named destination retypes the task in the same cross-note write
  ---
  duration_ms: 9.264115
  type: 'test'
  ...
# Subtest: a newly named picker entry forces the retype landing path
ok 269 - a newly named picker entry forces the retype landing path
  ---
  duration_ms: 0.830676
  type: 'test'
  ...
# Subtest: Pomodoro cleanup agrees only touched open entries in the same edit plan
ok 270 - Pomodoro cleanup agrees only touched open entries in the same edit plan
  ---
  duration_ms: 0.878257
  type: 'test'
  ...
# Subtest: unavailable current caps still retype the task and retain lane, ID, and freshness edits
ok 271 - unavailable current caps still retype the task and retain lane, ID, and freshness edits
  ---
  duration_ms: 6.73488
  type: 'test'
  ...
# Subtest: real Ledger Tools planner writes with an empty exempt list and custom exemptions
ok 272 - real Ledger Tools planner writes with an empty exempt list and custom exemptions
  ---
  duration_ms: 3.019187
  type: 'test'
  ...
# Subtest: a Ready scheduled task sets Next, logs the date, and remembers the theme
ok 273 - a Ready scheduled task sets Next, logs the date, and remembers the theme
  ---
  duration_ms: 2.207787
  type: 'test'
  ...
# Subtest: choosing the inherited destination clears an existing task theme
ok 274 - choosing the inherited destination clears an existing task theme
  ---
  duration_ms: 0.660392
  type: 'test'
  ...
# Subtest: a theme-only Next task with a new block ID still stamps because the ID rewrote the line
ok 275 - a theme-only Next task with a new block ID still stamps because the ID rewrote the line
  ---
  duration_ms: 0.576661
  type: 'test'
  ...
# Subtest: duplicate and paren theme fields repair only on an eligible deliberate write
ok 276 - duplicate and paren theme fields repair only on an eligible deliberate write
  ---
  duration_ms: 0.539891
  type: 'test'
  ...
# Subtest: a stale shown suggestion links and skips the theme edit
ok 277 - a stale shown suggestion links and skips the theme edit
  ---
  duration_ms: 0.747267
  type: 'test'
  ...
# Subtest: decorative catalog metadata on a live suggestion does not skip the write
ok 278 - decorative catalog metadata on a live suggestion does not skip the write
  ---
  duration_ms: 0.545923
  type: 'test'
  ...
# Subtest: Enter merges the current type into the destination name
ok 279 - Enter merges the current type into the destination name
  ---
  duration_ms: 0.530694
  type: 'test'
  ...
# Subtest: a container keeps the type on the default landing
ok 280 - a container keeps the type on the default landing
  ---
  duration_ms: 0.502099
  type: 'test'
  ...
# Subtest: untouched default (not deliberate) links without storing a field
ok 281 - untouched default (not deliberate) links without storing a field
  ---
  duration_ms: 0.517608
  type: 'test'
  ...
# Subtest: absent theme APIs leave the picker write path usable without a field
ok 282 - absent theme APIs leave the picker write path usable without a field
  ---
  duration_ms: 0.522228
  type: 'test'
  ...
# Subtest: a blocked dependency consumption never writes a theme field
ok 283 - a blocked dependency consumption never writes a theme field
  ---
  duration_ms: 7.58084
  type: 'test'
  ...
# Subtest: same-note combined edit writes the theme and the link in one editor transaction
ok 284 - same-note combined edit writes the theme and the link in one editor transaction
  ---
  duration_ms: 5.444229
  type: 'test'
  ...
# Subtest: a failed daily write after a saved theme reports the theme and the link failure
ok 285 - a failed daily write after a saved theme reports the theme and the link failure
  ---
  duration_ms: 1.276408
  type: 'test'
  ...
# Subtest: catalog spelling wins over a canonical landing name
ok 286 - catalog spelling wins over a canonical landing name
  ---
  duration_ms: 0.599535
  type: 'test'
  ...
# Subtest: a routed inbox task retypes from the destination suggestion
ok 287 - a routed inbox task retypes from the destination suggestion
  ---
  duration_ms: 1.148454
  type: 'test'
  ...
# Subtest: the inbox and the destination inherit different types, and the user picks the destination's suggested Pomodoro
ok 288 - the inbox and the destination inherit different types, and the user picks the destination's suggested Pomodoro
  ---
  duration_ms: 1.522749
  type: 'test'
  ...
# Subtest: a routed link that picks a different type writes the field
ok 289 - a routed link that picks a different type writes the field
  ---
  duration_ms: 0.679268
  type: 'test'
  ...
# Subtest: malformed themeIntent never enables a write
ok 290 - malformed themeIntent never enables a write
  ---
  duration_ms: 0.437746
  type: 'test'
  ...
# Subtest: themeIntent survives normalizePomodoroLinkPickerChoice for a later consumer
ok 291 - themeIntent survives normalizePomodoroLinkPickerChoice for a later consumer
  ---
  duration_ms: 0.446823
  type: 'test'
  ...
# Subtest: Tab pick chooses that type component of a composite destination
ok 292 - Tab pick chooses that type component of a composite destination
  ---
  duration_ms: 0.538399
  type: 'test'
  ...
# Subtest: unlink preserves an authored task theme
ok 293 - unlink preserves an authored task theme
  ---
  duration_ms: 4.773295
  type: 'test'
  ...
# Subtest: direct unlink without a daily note keeps the Next lane and reports it
ok 294 - direct unlink without a daily note keeps the Next lane and reports it
  ---
  duration_ms: 4.039946
  type: 'test'
  ...
# Subtest: In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
ok 295 - In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
  ---
  duration_ms: 0.883106
  type: 'test'
  ...
# Subtest: In Progress unlink with a summary keeps the lane and creates a Work Log
ok 296 - In Progress unlink with a summary keeps the lane and creates a Work Log
  ---
  duration_ms: 2.269905
  type: 'test'
  ...
# Subtest: In Progress unlink revalidates task text and block-ID uniqueness at confirmation
ok 297 - In Progress unlink revalidates task text and block-ID uniqueness at confirmation
  ---
  duration_ms: 0.457443
  type: 'test'
  ...
# Subtest: Next task unlink removes current and future links and keeps the Next lane
ok 298 - Next task unlink removes current and future links and keeps the Next lane
  ---
  duration_ms: 5.333016
  type: 'test'
  ...
# Subtest: In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
ok 299 - In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
  ---
  duration_ms: 1.379555
  type: 'test'
  ...
# Subtest: same-note Next unlink merges the Work Log and all-open cleanup in the active editor
ok 300 - same-note Next unlink merges the Work Log and all-open cleanup in the active editor
  ---
  duration_ms: 1.280465
  type: 'test'
  ...
# Subtest: same-note In Progress unlink merges cleanup and Work Log in the active editor
ok 301 - same-note In Progress unlink merges cleanup and Work Log in the active editor
  ---
  duration_ms: 0.847209
  type: 'test'
  ...
# Subtest: Next unlink stops before any write when daily cleanup write is stale
ok 302 - Next unlink stops before any write when daily cleanup write is stale
  ---
  duration_ms: 0.968349
  type: 'test'
  ...
# Subtest: Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
ok 303 - Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
  ---
  duration_ms: 1.486649
  type: 'test'
  ...
# Subtest: In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
ok 304 - In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
  ---
  duration_ms: 0.970162
  type: 'test'
  ...
# Subtest: review-walk: unlink settles with null and keeps its notice
ok 305 - review-walk: unlink settles with null and keeps its notice
  ---
  duration_ms: 1.851445
  type: 'test'
  ...
# Subtest: inbox-route: unlink cancel writes nothing
ok 306 - inbox-route: unlink cancel writes nothing
  ---
  duration_ms: 0.520775
  type: 'test'
  ...
# Subtest: inbox-route: unlink stay matches today and never commits
ok 307 - inbox-route: unlink stay matches today and never commits
  ---
  duration_ms: 0.761184
  type: 'test'
  ...
# Subtest: inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
ok 308 - inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.923113
  type: 'test'
  ...
# Subtest: inbox-route: In Progress unlink with a Work summary routes
ok 309 - inbox-route: In Progress unlink with a Work summary routes
  ---
  duration_ms: 0.79068
  type: 'test'
  ...
# Subtest: inbox-route: unlink move failure gives the partial notice and stays
ok 310 - inbox-route: unlink move failure gives the partial notice and stays
  ---
  duration_ms: 0.401546
  type: 'test'
  ...
# Subtest: inbox-route: non-inbox unlink never prompts
ok 311 - inbox-route: non-inbox unlink never prompts
  ---
  duration_ms: 0.513301
  type: 'test'
  ...
# Subtest: review-walk: Work-summary unlink path retains origin until submit
ok 312 - review-walk: Work-summary unlink path retains origin until submit
  ---
  duration_ms: 0.836277
  type: 'test'
  ...
# Subtest: inbox-route: unlink source drift during route prompt refuses without writes
ok 313 - inbox-route: unlink source drift during route prompt refuses without writes
  ---
  duration_ms: 0.358886
  type: 'test'
  ...
# Subtest: inbox-route: Work-summary route cancel returns sentinel and settles null once
ok 314 - inbox-route: Work-summary route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.332936
  type: 'test'
  ...
# Subtest: inbox-route: unlink no-op with move never commits
ok 315 - inbox-route: unlink no-op with move never commits
  ---
  duration_ms: 0.633049
  type: 'test'
  ...
# Subtest: same-note unlink maps a task below removed entries through Work-summary inserts
ok 316 - same-note unlink maps a task below removed entries through Work-summary inserts
  ---
  duration_ms: 1.008546
  type: 'test'
  ...
# Subtest: the unlink preview shows the write-instant stamp and re-renders on the clock
ok 317 - the unlink preview shows the write-instant stamp and re-renders on the clock
  ---
  duration_ms: 0.976334
  type: 'test'
  ...
# Subtest: a prompt opened at 23:59 and committed at 00:01 stamps the commit instant
ok 318 - a prompt opened at 23:59 and committed at 00:01 stamps the commit instant
  ---
  duration_ms: 0.691621
  type: 'test'
  ...
# Subtest: direct-add seeds from the task headline, not non-task blocks
ok 319 - direct-add seeds from the task headline, not non-task blocks
  ---
  duration_ms: 6.013756
  type: 'test'
  ...
# Subtest: direct-add seeds a plain note bullet from its text without the created stamp
ok 320 - direct-add seeds a plain note bullet from its text without the created stamp
  ---
  duration_ms: 0.752828
  type: 'test'
  ...
# Subtest: link-task-complete seeds from the target, prefers open buffers
ok 321 - link-task-complete seeds from the target, prefers open buffers
  ---
  duration_ms: 1.119949
  type: 'test'
  ...
# Subtest: link-task-complete reports stale and unreadable targets
ok 322 - link-task-complete reports stale and unreadable targets
  ---
  duration_ms: 0.377571
  type: 'test'
  ...
# Subtest: pomodoro link seeds after the choice from the cursor task
ok 323 - pomodoro link seeds after the choice from the cursor task
  ---
  duration_ms: 0.358395
  type: 'test'
  ...
# Subtest: marker rename suggests from the unique task, never hiding ambiguity
ok 324 - marker rename suggests from the unique task, never hiding ambiguity
  ---
  duration_ms: 0.632428
  type: 'test'
  ...
# Subtest: marker rename suggests from a unique plain note bullet
ok 325 - marker rename suggests from a unique plain note bullet
  ---
  duration_ms: 0.45558
  type: 'test'
  ...
# Subtest: modal seeds the value, selects once, and never overwrites typing
ok 326 - modal seeds the value, selects once, and never overwrites typing
  ---
  duration_ms: 1.431855
  type: 'test'
  ...
# Subtest: modal disables Save while loading and survives close/reopen
ok 327 - modal disables Save while loading and survives close/reopen
  ---
  duration_ms: 1.541865
  type: 'test'
  ...
# Subtest: submit revalidates: occupied IDs and stale tasks fail editable
ok 328 - submit revalidates: occupied IDs and stale tasks fail editable
  ---
  duration_ms: 1.414131
  type: 'test'
  ...
# Subtest: cancelling writes no ID and explicit renames keep the current ID
ok 329 - cancelling writes no ID and explicit renames keep the current ID
  ---
  duration_ms: 0.752717
  type: 'test'
  ...
# Subtest: the task picker drops the paired \#ref and prefixes the book
ok 330 - the task picker drops the paired \#ref and prefixes the book
  ---
  duration_ms: 4.23657
  type: 'test'
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 331 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.619423
  type: 'test'
  ...
# Subtest: block-id-prompt LK1–LK19 recognises only relation line shapes
ok 332 - block-id-prompt LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 1.946126
  type: 'test'
  ...
# Subtest: block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
ok 333 - block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
  ---
  duration_ms: 4.957107
  type: 'test'
  ...
# Subtest: block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
ok 334 - block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
  ---
  duration_ms: 2.113297
  type: 'test'
  ...
# Subtest: a rename writes each open note as one editor transaction and undoes in one step
ok 335 - a rename writes each open note as one editor transaction and undoes in one step
  ---
  duration_ms: 17.479476
  type: 'test'
  ...
# Subtest: a note open in a non-active leaf is edited through its editor, unsaved text included
ok 336 - a note open in a non-active leaf is edited through its editor, unsaved text included
  ---
  duration_ms: 2.178281
  type: 'test'
  ...
# Subtest: disagreeing open buffers for one note refuse the rename
ok 337 - disagreeing open buffers for one note refuse the rename
  ---
  duration_ms: 0.7852
  type: 'test'
  ...
# Subtest: a closed note that changed since planning refuses and earlier writes roll back
ok 338 - a closed note that changed since planning refuses and earlier writes roll back
  ---
  duration_ms: 1.017354
  type: 'test'
  ...
# Subtest: an open note that changed while closed notes were written refuses and rolls back
ok 339 - an open note that changed while closed notes were written refuses and rolls back
  ---
  duration_ms: 0.904267
  type: 'test'
  ...
# Subtest: undoing the rename in its note rewrites the other notes back, and redo re-applies it
ok 340 - undoing the rename in its note rewrites the other notes back, and redo re-applies it
  ---
  duration_ms: 2.627428
  type: 'test'
  ...
# Subtest: undoing in a referencing note follows into the destination and the other notes
ok 341 - undoing in a referencing note follows into the destination and the other notes
  ---
  duration_ms: 1.367532
  type: 'test'
  ...
# Subtest: an ambiguous note is left alone and named in a sticky Notice
ok 342 - an ambiguous note is left alone and named in a sticky Notice
  ---
  duration_ms: 1.080194
  type: 'test'
  ...
# Subtest: a recorded span that was edited makes its note ambiguous
ok 343 - a recorded span that was edited makes its note ambiguous
  ---
  duration_ms: 1.281338
  type: 'test'
  ...
# Subtest: editing a note the follow could not rewrite never redoes the rename
ok 344 - editing a note the follow could not rewrite never redoes the rename
  ---
  duration_ms: 1.480517
  type: 'test'
  ...
# Subtest: records expire, and edits without a live record schedule nothing
ok 345 - records expire, and edits without a live record schedule nothing
  ---
  duration_ms: 1.080824
  type: 'test'
  ...
# Subtest: a redo during closed-note undo follow converges on the latest editor form
ok 346 - a redo during closed-note undo follow converges on the latest editor form
  ---
  duration_ms: 1.506497
  type: 'test'
  ...
# Subtest: an undo during closed-note redo follow converges on the latest editor form
ok 347 - an undo during closed-note redo follow converges on the latest editor form
  ---
  duration_ms: 1.373092
  type: 'test'
  ...
# Subtest: an unrelated edit in a second editor during closed follow is preserved
ok 348 - an unrelated edit in a second editor during closed follow is preserved
  ---
  duration_ms: 1.105271
  type: 'test'
  ...
# Subtest: blockRenameNoteForm reads token and link forms and refuses mixed or missing states
ok 349 - blockRenameNoteForm reads token and link forms and refuses mixed or missing states
  ---
  duration_ms: 0.396037
  type: 'test'
  ...
# Subtest: calendar date parsing rejects malformed width and impossible dates
ok 350 - calendar date parsing rejects malformed width and impossible dates
  ---
  duration_ms: 2.186336
  type: 'test'
  ...
# Subtest: future scheduled field detection respects the yesterday/today/tomorrow boundary
ok 351 - future scheduled field detection respects the yesterday/today/tomorrow boundary
  ---
  duration_ms: 0.650643
  type: 'test'
  ...
# Subtest: scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
ok 352 - scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
  ---
  duration_ms: 0.197858
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
ok 353 - planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
  ---
  duration_ms: 1.297178
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
ok 354 - planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
  ---
  duration_ms: 0.288932
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
ok 355 - planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
  ---
  duration_ms: 0.296176
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
ok 356 - planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
  ---
  duration_ms: 0.228817
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate leaves today and past schedules untouched
ok 357 - planTargetTaskUpdate leaves today and past schedules untouched
  ---
  duration_ms: 0.396498
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
ok 358 - planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
  ---
  duration_ms: 0.616828
  type: 'test'
  ...
# Subtest: two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
ok 359 - two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
  ---
  duration_ms: 0.653218
  type: 'test'
  ...
# Subtest: a malformed single scheduled field is never treated as future
ok 360 - a malformed single scheduled field is never treated as future
  ---
  duration_ms: 0.25127
  type: 'test'
  ...
# Subtest: an ambiguous scheduled field does not block the legacy Ready promotion
ok 361 - an ambiguous scheduled field does not block the legacy Ready promotion
  ---
  duration_ms: 0.299442
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
ok 362 - planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
  ---
  duration_ms: 0.226182
  type: 'test'
  ...
# Subtest: Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
ok 363 - Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
  ---
  duration_ms: 0.670631
  type: 'test'
  ...
# Subtest: Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
ok 364 - Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
  ---
  duration_ms: 0.24608
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
ok 365 - planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
  ---
  duration_ms: 0.353826
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
ok 366 - planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
  ---
  duration_ms: 0.249937
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
ok 367 - planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.19879
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
ok 368 - planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
  ---
  duration_ms: 0.184372
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
ok 369 - planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
  ---
  duration_ms: 0.406807
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate preserves a trailing newline when one was already present
ok 370 - planTargetTaskUpdate preserves a trailing newline when one was already present
  ---
  duration_ms: 0.188149
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
ok 371 - planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
  ---
  duration_ms: 0.14691
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
ok 372 - planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
  ---
  duration_ms: 0.253203
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
ok 373 - planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
  ---
  duration_ms: 0.168813
  type: 'test'
  ...
# Subtest: existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
ok 374 - existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
  ---
  duration_ms: 5.186296
  type: 'test'
  ...
# Subtest: new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
ok 375 - new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
  ---
  duration_ms: 1.328989
  type: 'test'
  ...
# Subtest: activation runtime aborts without any write when the target preimage goes stale
ok 376 - activation runtime aborts without any write when the target preimage goes stale
  ---
  duration_ms: 0.598663
  type: 'test'
  ...
# Subtest: same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
ok 377 - same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
  ---
  duration_ms: 3.538659
  type: 'test'
  ...
# Subtest: same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
ok 378 - same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
  ---
  duration_ms: 0.825356
  type: 'test'
  ...
# Subtest: a source marker edited after a successful existing-ID target write reports an accurate partial notice
ok 379 - a source marker edited after a successful existing-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.635133
  type: 'test'
  ...
# Subtest: a source marker edited after a successful new-ID target write reports an accurate partial notice
ok 380 - a source marker edited after a successful new-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.850174
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
ok 381 - planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
  ---
  duration_ms: 0.24089
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
ok 382 - planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
  ---
  duration_ms: 0.158583
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
ok 383 - planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
  ---
  duration_ms: 0.179002
  type: 'test'
  ...
# Subtest: Pomodoro forceNext stamps the pulled-forward Ready task before its block ID
ok 384 - Pomodoro forceNext stamps the pulled-forward Ready task before its block ID
  ---
  duration_ms: 0.652156
  type: 'test'
  ...
# Subtest: planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
ok 385 - planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.156589
  type: 'test'
  ...
# Subtest: direct Task Links raise ^prj while never pulling its date forward
ok 386 - direct Task Links raise ^prj while never pulling its date forward
  ---
  duration_ms: 0.169644
  type: 'test'
  ...
# Subtest: task-link selection: one link is selectable from any column, several are chosen by cursor
ok 387 - task-link selection: one link is selectable from any column, several are chosen by cursor
  ---
  duration_ms: 3.52358
  type: 'test'
  ...
# Subtest: task-link selection ignores picker/rename markers, plain links, and Markdown-style links
ok 388 - task-link selection ignores picker/rename markers, plain links, and Markdown-style links
  ---
  duration_ms: 0.41905
  type: 'test'
  ...
# Subtest: dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
ok 389 - dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
  ---
  duration_ms: 0.819395
  type: 'test'
  ...
# Subtest: inline Task Link deletion removes the token with its decoration and collapses whitespace
ok 390 - inline Task Link deletion removes the token with its decoration and collapses whitespace
  ---
  duration_ms: 0.831428
  type: 'test'
  ...
# Subtest: dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
ok 391 - dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
  ---
  duration_ms: 1.087637
  type: 'test'
  ...
# Subtest: mergeCoveringEdits keeps the covering edit and the earlier of identical edits
ok 392 - mergeCoveringEdits keeps the covering edit and the earlier of identical edits
  ---
  duration_ms: 0.311064
  type: 'test'
  ...
# Subtest: dependency transclusion detection needs an embedded sole-content child of a \#task line
ok 393 - dependency transclusion detection needs an embedded sole-content child of a \#task line
  ---
  duration_ms: 0.525003
  type: 'test'
  ...
# Subtest: Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
ok 394 - Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
  ---
  duration_ms: 7.191706
  type: 'test'
  ...
# Subtest: Task Link on a Next target works from an embedded aliased link outside any Pomodoro
ok 395 - Task Link on a Next target works from an embedded aliased link outside any Pomodoro
  ---
  duration_ms: 1.841587
  type: 'test'
  ...
# Subtest: same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
ok 396 - same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
  ---
  duration_ms: 1.605016
  type: 'test'
  ...
# Subtest: same-note Task Link deletion clamps the restored cursor to the shortened note
ok 397 - same-note Task Link deletion clamps the restored cursor to the shortened note
  ---
  duration_ms: 0.686661
  type: 'test'
  ...
# Subtest: a cleanup subtree that covers a nested selected link wins and links are not double counted
ok 398 - a cleanup subtree that covers a nested selected link wins and links are not double counted
  ---
  duration_ms: 0.972798
  type: 'test'
  ...
# Subtest: same-note Task Link in a closed entry deletes the closed entry it empties
ok 399 - same-note Task Link in a closed entry deletes the closed entry it empties
  ---
  duration_ms: 0.960494
  type: 'test'
  ...
# Subtest: Task Link in another day's note deletes the emptied entry there and in today's note
ok 400 - Task Link in another day's note deletes the emptied entry there and in today's note
  ---
  duration_ms: 0.842388
  type: 'test'
  ...
# Subtest: Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
ok 401 - Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
  ---
  duration_ms: 1.642206
  type: 'test'
  ...
# Subtest: Task Link on an In Progress target with a blank summary logs nothing
ok 402 - Task Link on an In Progress target with a blank summary logs nothing
  ---
  duration_ms: 1.065023
  type: 'test'
  ...
# Subtest: canceling the In Progress Task Link prompt leaves everything untouched
ok 403 - canceling the In Progress Task Link prompt leaves everything untouched
  ---
  duration_ms: 0.367121
  type: 'test'
  ...
# Subtest: canceling the In Progress unlink prompt in task mode leaves everything untouched
ok 404 - canceling the In Progress unlink prompt in task mode leaves everything untouched
  ---
  duration_ms: 0.725175
  type: 'test'
  ...
# Subtest: In Progress Task Link submit revalidates the link line and the target task
ok 405 - In Progress Task Link submit revalidates the link line and the target task
  ---
  duration_ms: 0.796792
  type: 'test'
  ...
# Subtest: Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
ok 406 - Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
  ---
  duration_ms: 2.865594
  type: 'test'
  ...
# Subtest: Task Link on a Done or Cancelled target is refused without edits
ok 407 - Task Link on a Done or Cancelled target is refused without edits
  ---
  duration_ms: 0.615516
  type: 'test'
  ...
# Subtest: Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
ok 408 - Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
  ---
  duration_ms: 0.910379
  type: 'test'
  ...
# Subtest: precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
ok 409 - precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
  ---
  duration_ms: 2.275556
  type: 'test'
  ...
# Subtest: Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
ok 410 - Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
  ---
  duration_ms: 0.985873
  type: 'test'
  ...
# Subtest: Task Link that is a sub-task dependency transclusion is refused without edits
ok 411 - Task Link that is a sub-task dependency transclusion is refused without edits
  ---
  duration_ms: 0.280275
  type: 'test'
  ...
# Subtest: Task Link partial failure after the daily write is retryable
ok 412 - Task Link partial failure after the daily write is retryable
  ---
  duration_ms: 1.354066
  type: 'test'
  ...
# Subtest: Task Link stops before any write when the target note changes after planning
ok 413 - Task Link stops before any write when the target note changes after planning
  ---
  duration_ms: 0.636947
  type: 'test'
  ...
# Subtest: Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
ok 414 - Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
  ---
  duration_ms: 0.576892
  type: 'test'
  ...
# Subtest: Task Link subtree deletion removes a nested target task without any status write
ok 415 - Task Link subtree deletion removes a nested target task without any status write
  ---
  duration_ms: 0.371159
  type: 'test'
  ...
# Subtest: whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
ok 416 - whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
  ---
  duration_ms: 0.823523
  type: 'test'
  ...
# Subtest: selected-link deletion maps a cursor inside a removed entry to its former start
ok 417 - selected-link deletion maps a cursor inside a removed entry to its former start
  ---
  duration_ms: 0.741557
  type: 'test'
  ...
# Subtest: cache prefilter skips taskless files without reading, reads cacheless files
ok 418 - cache prefilter skips taskless files without reading, reads cacheless files
  ---
  duration_ms: 4.866676
  type: 'test'
  ...
# Subtest: a throwing file cache falls back to reading
ok 419 - a throwing file cache falls back to reading
  ---
  duration_ms: 0.399573
  type: 'test'
  ...
# Subtest: non-note and excluded paths never enter the store
ok 420 - non-note and excluded paths never enter the store
  ---
  duration_ms: 0.51283
  type: 'test'
  ...
# Subtest: unreadable files produce bounded warnings and a quiet footer note
ok 421 - unreadable files produce bounded warnings and a quiet footer note
  ---
  duration_ms: 0.976746
  type: 'test'
  ...
# Subtest: blockIdsFor exposes the note id set for the detail strip preview
ok 422 - blockIdsFor exposes the note id set for the detail strip preview
  ---
  duration_ms: 0.377692
  type: 'test'
  ...
# Subtest: taskBearingDocuments reads fresh text on demand
ok 423 - taskBearingDocuments reads fresh text on demand
  ---
  duration_ms: 0.786833
  type: 'test'
  ...
# Subtest: metadataCache changed re-parses from event data with no extra read
ok 424 - metadataCache changed re-parses from event data with no extra read
  ---
  duration_ms: 0.671583
  type: 'test'
  ...
# Subtest: vault rename re-keys rows and recomputes the basename index
ok 425 - vault rename re-keys rows and recomputes the basename index
  ---
  duration_ms: 1.252081
  type: 'test'
  ...
# Subtest: renaming onto an excluded path drops the note
ok 426 - renaming onto an excluded path drops the note
  ---
  duration_ms: 0.584646
  type: 'test'
  ...
# Subtest: vault delete drops rows
ok 427 - vault delete drops rows
  ---
  duration_ms: 0.713122
  type: 'test'
  ...
# Subtest: open-time mtime validation queues changed files for background re-parse
ok 428 - open-time mtime validation queues changed files for background re-parse
  ---
  duration_ms: 0.75394
  type: 'test'
  ...
# Subtest: a vanished file is removed when the reparse queue drains
ok 429 - a vanished file is removed when the reparse queue drains
  ---
  duration_ms: 0.501307
  type: 'test'
  ...
# Subtest: live overlays win over disk and never persist
ok 430 - live overlays win over disk and never persist
  ---
  duration_ms: 0.425854
  type: 'test'
  ...
# Subtest: snapshot returns ordered rows, progress, and a live subscription
ok 431 - snapshot returns ordered rows, progress, and a live subscription
  ---
  duration_ms: 0.612299
  type: 'test'
  ...
# Subtest: filtering performs no vault reads
ok 432 - filtering performs no vault reads
  ---
  duration_ms: 0.476029
  type: 'test'
  ...
# Subtest: refreshPaths applies post-write content and recomputes locators
ok 433 - refreshPaths applies post-write content and recomputes locators
  ---
  duration_ms: 0.396608
  type: 'test'
  ...
# Subtest: refreshPathsFromVault re-reads named paths
ok 434 - refreshPathsFromVault re-reads named paths
  ---
  duration_ms: 0.388411
  type: 'test'
  ...
# Subtest: collectEditorOverlays reads every open markdown editor
ok 435 - collectEditorOverlays reads every open markdown editor
  ---
  duration_ms: 0.372712
  type: 'test'
  ...
# Subtest: attachLiveUpdates without a host is a safe no-op
ok 436 - attachLiveUpdates without a host is a safe no-op
  ---
  duration_ms: 0.127032
  type: 'test'
  ...
# Subtest: custom settings narrow the parsed pool
ok 437 - custom settings narrow the parsed pool
  ---
  duration_ms: 0.256209
  type: 'test'
  ...
# Subtest: snapshot rows keep parsed metadata, leave stored rows bare, and cache search-text-first fields
ok 438 - snapshot rows keep parsed metadata, leave stored rows bare, and cache search-text-first fields
  ---
  duration_ms: 2.155566
  type: 'test'
  ...
# Subtest: cached and uncached matching stay aligned across overlay, rename collision, delete, and refresh
ok 439 - cached and uncached matching stay aligned across overlay, rename collision, delete, and refresh
  ---
  duration_ms: 7.382561
  type: 'test'
  ...
# Subtest: task wikilink fixture mirrors bob-cli byte for byte
ok 440 - task wikilink fixture mirrors bob-cli byte for byte
  ---
  duration_ms: 2.201845
  type: 'test'
  ...
# Subtest: every vector ranks the same rows bob serves
ok 441 - every vector ranks the same rows bob serves
  ---
  duration_ms: 8.780692
  type: 'test'
  ...
# Subtest: frontmatter tasks never parse, unclosed fences stay open
ok 442 - frontmatter tasks never parse, unclosed fences stay open
  ---
  duration_ms: 0.483814
  type: 'test'
  ...
# Subtest: task grammar mirrors bob: dashes only, exact filter token
ok 443 - task grammar mirrors bob: dashes only, exact filter token
  ---
  duration_ms: 0.236451
  type: 'test'
  ...
# Subtest: trailing IDs need whitespace and clean bytes; every line counts
ok 444 - trailing IDs need whitespace and clean bytes; every line counts
  ---
  duration_ms: 0.25125
  type: 'test'
  ...
# Subtest: hide and project-block tags are exact tokens
ok 445 - hide and project-block tags are exact tokens
  ---
  duration_ms: 0.27235
  type: 'test'
  ...
# Subtest: search text drops filters, fields, and the block ID
ok 446 - search text drops filters, fields, and the block ID
  ---
  duration_ms: 0.527056
  type: 'test'
  ...
# Subtest: sections track headings and depth counts indentation
ok 447 - sections track headings and depth counts indentation
  ---
  duration_ms: 0.428769
  type: 'test'
  ...
# Subtest: note paths, locators, and archive targets
ok 448 - note paths, locators, and archive targets
  ---
  duration_ms: 0.671453
  type: 'test'
  ...
# Subtest: match tiers, AND terms, and empty queries
ok 449 - match tiers, AND terms, and empty queries
  ---
  duration_ms: 0.601028
  type: 'test'
  ...
# Subtest: previous daily is the latest daily before the anchor
ok 450 - previous daily is the latest daily before the anchor
  ---
  duration_ms: 0.283762
  type: 'test'
  ...
# Subtest: guards mirror bob, minus the read-only check
ok 451 - guards mirror bob, minus the read-only check
  ---
  duration_ms: 0.216343
  type: 'test'
  ...
# Subtest: fused scorer matches the layered scorer across randomized rows and queries
ok 452 - fused scorer matches the layered scorer across randomized rows and queries
  ---
  duration_ms: 112.579099
  type: 'test'
  ...
# Subtest: ID-less task identity relocates only to one exact line
ok 453 - ID-less task identity relocates only to one exact line
  ---
  duration_ms: 1.78527
  type: 'test'
  ...
# Subtest: wikilink naming validates closed tasks and rejects duplicate target IDs
ok 454 - wikilink naming validates closed tasks and rejects duplicate target IDs
  ---
  duration_ms: 1.016231
  type: 'test'
  ...
# Subtest: wikilink naming adds an ID to a moved closed task and links the original token
ok 455 - wikilink naming adds an ID to a moved closed task and links the original token
  ---
  duration_ms: 4.556393
  type: 'test'
  ...
# Subtest: ^^ naming preserves a cross-note target and alias through the final link
ok 456 - ^^ naming preserves a cross-note target and alias through the final link
  ---
  duration_ms: 3.467433
  type: 'test'
  ...
# Subtest: auto-open only on a written second paren, including auto-pair and closed shapes
ok 457 - auto-open only on a written second paren, including auto-pair and closed shapes
  ---
  duration_ms: 41.199427
  type: 'test'
  ...
# Subtest: caret-only, undo, and programmatic edits never auto-open
ok 458 - caret-only, undo, and programmatic edits never auto-open
  ---
  duration_ms: 0.83249
  type: 'test'
  ...
# Subtest: query seeds from the token and keys move, accept, escape, and backspace
ok 459 - query seeds from the token and keys move, accept, escape, and backspace
  ---
  duration_ms: 12.299021
  type: 'test'
  ...
# Subtest: Backspace undoes closed ((q)) to () and unclosed ((q to (
ok 460 - Backspace undoes closed ((q)) to () and unclosed ((q to (
  ---
  duration_ms: 3.892004
  type: 'test'
  ...
# Subtest: identified accept splices one transaction, caret after ]], no notice
ok 461 - identified accept splices one transaction, caret after ]], no notice
  ---
  duration_ms: 2.419642
  type: 'test'
  ...
# Subtest: stale target paths keep the picker open with a Notice
ok 462 - stale target paths keep the picker open with a Notice
  ---
  duration_ms: 2.086816
  type: 'test'
  ...
# Subtest: command opens on a token, a selection, or the caret
ok 463 - command opens on a token, a selection, or the caret
  ---
  duration_ms: 5.991924
  type: 'test'
  ...
# Subtest: managed-line (( shows that line's guard notice and never opens
ok 464 - managed-line (( shows that line's guard notice and never opens
  ---
  duration_ms: 1.053472
  type: 'test'
  ...
# Subtest: command in an excluded context shows Task wikilinks can't go here
ok 465 - command in an excluded context shows Task wikilinks can't go here
  ---
  duration_ms: 0.671082
  type: 'test'
  ...
# Subtest: ^^ marker still opens the per-note picker when (( is absent
ok 466 - ^^ marker still opens the per-note picker when (( is absent
  ---
  duration_ms: 1.07811
  type: 'test'
  ...
# Subtest: ID-less Enter opens naming mode with the picker state
ok 467 - ID-less Enter opens naming mode with the picker state
  ---
  duration_ms: 18.170362
  type: 'test'
  ...
# Subtest: Page Down clamps at the final selectable row instead of wrapping
ok 468 - Page Down clamps at the final selectable row instead of wrapping
  ---
  duration_ms: 39.636873
  type: 'test'
  ...
# Subtest: naming cancel paths restore query, selection, row limit, and scroll
ok 469 - naming cancel paths restore query, selection, row limit, and scroll
  ---
  duration_ms: 3.971345
  type: 'test'
  ...
# Subtest: a scan that exits early clears old written ranges before a later scan
ok 470 - a scan that exits early clears old written ranges before a later scan
  ---
  duration_ms: 0.859591
  type: 'test'
  ...
# Subtest: identified accept dispatches one isolated CodeMirror completion event
ok 471 - identified accept dispatches one isolated CodeMirror completion event
  ---
  duration_ms: 1.702672
  type: 'test'
  ...
# Subtest: guarded rows never open the naming prompt
ok 472 - guarded rows never open the naming prompt
  ---
  duration_ms: 2.206694
  type: 'test'
  ...
# Subtest: cheap Pomodoro guards disable non-selected duplicate rows
ok 473 - cheap Pomodoro guards disable non-selected duplicate rows
  ---
  duration_ms: 5.804907
  type: 'test'
  ...
# Subtest: stale Backspace closes with a notice and leaves the changed token alone
ok 474 - stale Backspace closes with a notice and leaves the changed token alone
  ---
  duration_ms: 0.945385
  type: 'test'
  ...
# Subtest: onEscapeKey clears a non-empty filter first and closes on an empty one
ok 475 - onEscapeKey clears a non-empty filter first and closes on an empty one
  ---
  duration_ms: 1.495948
  type: 'test'
  ...
# Subtest: empty filter groups This note, In progress, Next, Other open, Hidden, Completed
ok 476 - empty filter groups This note, In progress, Next, Other open, Hidden, Completed
  ---
  duration_ms: 27.520384
  type: 'test'
  ...
# Subtest: per-note headers expose sticky data, kind icons, and count pills
ok 477 - per-note headers expose sticky data, kind icons, and count pills
  ---
  duration_ms: 1.543567
  type: 'test'
  ...
# Subtest: row anatomy, locator parts, and action lines cover identified, id-less, and guarded
ok 478 - row anatomy, locator parts, and action lines cover identified, id-less, and guarded
  ---
  duration_ms: 3.363493
  type: 'test'
  ...
# Subtest: title parts render code, wikilinks, markdown labels, and URL hosts
ok 479 - title parts render code, wikilinks, markdown labels, and URL hosts
  ---
  duration_ms: 0.747748
  type: 'test'
  ...
# Subtest: counts, empty states, indexing, and footer hints
ok 480 - counts, empty states, indexing, and footer hints
  ---
  duration_ms: 1.722529
  type: 'test'
  ...
# Subtest: windowing emits 100-row windows and renderAll exhausts
ok 481 - windowing emits 100-row windows and renderAll exhausts
  ---
  duration_ms: 12.470649
  type: 'test'
  ...
# Subtest: narrow layout keeps basename plus id and drops the backspace hint
ok 482 - narrow layout keeps basename plus id and drops the backspace hint
  ---
  duration_ms: 0.67537
  type: 'test'
  ...
# Subtest: filtered list is flat with a Completed history divider
ok 483 - filtered list is flat with a Completed history divider
  ---
  duration_ms: 0.492862
  type: 'test'
  ...
# Subtest: caret-task and unlinkable-path guards disable the row
ok 484 - caret-task and unlinkable-path guards disable the row
  ---
  duration_ms: 0.856155
  type: 'test'
  ...
# Subtest: card DOM helpers are exported for Chromium previews
ok 485 - card DOM helpers are exported for Chromium previews
  ---
  duration_ms: 0.485878
  type: 'test'
  ...
# Subtest: Pomodoro (( picker limits the pool to open tasks and shows commit consequences
ok 486 - Pomodoro (( picker limits the pool to open tasks and shows commit consequences
  ---
  duration_ms: 30.682512
  type: 'test'
  ...
# Subtest: ^^ under an open Pomodoro raises blocked prerequisites, leaves the task unlinked, and reverts the marker
ok 487 - ^^ under an open Pomodoro raises blocked prerequisites, leaves the task unlinked, and reverts the marker
  ---
  duration_ms: 8.721798
  type: 'test'
  ...
# Subtest: ^^ refuses a project-blocked task without consuming its prerequisites
ok 488 - ^^ refuses a project-blocked task without consuming its prerequisites
  ---
  duration_ms: 1.443707
  type: 'test'
  ...
# Subtest: ^^ refuses a closed target under an open Pomodoro
ok 489 - ^^ refuses a closed target under an open Pomodoro
  ---
  duration_ms: 1.141861
  type: 'test'
  ...
# Subtest: (( refuses a \#prj_is_blocked resident without consuming prerequisites
ok 490 - (( refuses a \#prj_is_blocked resident without consuming prerequisites
  ---
  duration_ms: 1.115991
  type: 'test'
  ...
# Subtest: (( refuses a task inherited-blocked by its \#prj_is_blocked project
ok 491 - (( refuses a task inherited-blocked by its \#prj_is_blocked project
  ---
  duration_ms: 1.29369
  type: 'test'
  ...
# Subtest: (( refuses a ^prj whose own future date is the sole remaining reason
ok 492 - (( refuses a ^prj whose own future date is the sole remaining reason
  ---
  duration_ms: 1.261319
  type: 'test'
  ...
# Subtest: ^^ links and promotes an existing-ID task under an open Pomodoro
ok 493 - ^^ links and promotes an existing-ID task under an open Pomodoro
  ---
  duration_ms: 3.203709
  type: 'test'
  ...
# Subtest: ID-less ^^ names, links, and retains its target alias in Pomodoro mode
ok 494 - ID-less ^^ names, links, and retains its target alias in Pomodoro mode
  ---
  duration_ms: 2.475769
  type: 'test'
  ...
# Subtest: an unrelated unreadable note does not block a Ready Pomodoro target
ok 495 - an unrelated unreadable note does not block a Ready Pomodoro target
  ---
  duration_ms: 1.932411
  type: 'test'
  ...
# Subtest: a ^prj blocked only by its own prerequisite raises that prerequisite
ok 496 - a ^prj blocked only by its own prerequisite raises that prerequisite
  ---
  duration_ms: 1.858089
  type: 'test'
  ...
# Subtest: Pomodoro prerequisite raise pins every promoted task and selects the first
ok 497 - Pomodoro prerequisite raise pins every promoted task and selects the first
  ---
  duration_ms: 4.670901
  type: 'test'
  ...
# Subtest: the task wikilink Pomodoro preview omits type text when the themes API is absent
ok 498 - the task wikilink Pomodoro preview omits type text when the themes API is absent
  ---
  duration_ms: 0.690038
  type: 'test'
  ...
# Subtest: Pomodoro commit rechecks the selected task before writing
ok 499 - Pomodoro commit rechecks the selected task before writing
  ---
  duration_ms: 0.505375
  type: 'test'
  ...
# Subtest: ID-less (( selection names the task and completes through the shared Pomodoro commit
ok 500 - ID-less (( selection names the task and completes through the shared Pomodoro commit
  ---
  duration_ms: 1.867878
  type: 'test'
  ...
# Subtest: Pomodoro commit merges the task type into the Pomodoro, pulls a future schedule forward, and includes notices
ok 501 - Pomodoro commit merges the task type into the Pomodoro, pulls a future schedule forward, and includes notices
  ---
  duration_ms: 1.924757
  type: 'test'
  ...
# Subtest: task-wikilink trigger vectors match bob's shared core
ok 502 - task-wikilink trigger vectors match bob's shared core
  ---
  duration_ms: 3.253233
  type: 'test'
  ...
# Subtest: task-wikilink context vectors allow prose and exclude note-only spans
ok 503 - task-wikilink context vectors allow prose and exclude note-only spans
  ---
  duration_ms: 5.173551
  type: 'test'
  ...
# Subtest: task-wikilink written-second-paren vectors gate auto-open on user input
ok 504 - task-wikilink written-second-paren vectors gate auto-open on user input
  ---
  duration_ms: 0.480908
  type: 'test'
  ...
# Subtest: findTaskWikilinkToken rejects unusable caret positions
ok 505 - findTaskWikilinkToken rejects unusable caret positions
  ---
  duration_ms: 0.174653
  type: 'test'
  ...
# Subtest: taskWikilinkContextAt rejects unusable positions
ok 506 - taskWikilinkContextAt rejects unusable positions
  ---
  duration_ms: 0.276488
  type: 'test'
  ...
# Subtest: addTaskWikilinkChanges records insertions and maps earlier ranges forward
ok 507 - addTaskWikilinkChanges records insertions and maps earlier ranges forward
  ---
  duration_ms: 0.516206
  type: 'test'
  ...
# Subtest: addTaskWikilinkChanges accepts the wrapper and CodeMirror spellings
ok 508 - addTaskWikilinkChanges accepts the wrapper and CodeMirror spellings
  ---
  duration_ms: 0.310062
  type: 'test'
  ...
# Subtest: mapTaskWikilinkRanges maps without recording
ok 509 - mapTaskWikilinkRanges maps without recording
  ---
  duration_ms: 0.264335
  type: 'test'
  ...
# Subtest: mapTaskWikilinkRanges tolerates array ranges and empty sets
ok 510 - mapTaskWikilinkRanges tolerates array ranges and empty sets
  ---
  duration_ms: 0.505987
  type: 'test'
  ...
# Subtest: work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
ok 511 - work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
  ---
  duration_ms: 2.414271
  type: 'test'
  ...
# Subtest: formatWorkLogStamp matches the shared conformance vectors
ok 512 - formatWorkLogStamp matches the shared conformance vectors
  ---
  duration_ms: 0.490136
  type: 'test'
  ...
# Subtest: work log stamps use local wall-clock components
ok 513 - work log stamps use local wall-clock components
  ---
  duration_ms: 0.296436
  type: 'test'
  ...
# Subtest: planWorkLogInsertion stamps the injected clock when no stamp is given
ok 514 - planWorkLogInsertion stamps the injected clock when no stamp is given
  ---
  duration_ms: 1.223267
  type: 'test'
  ...
# Subtest: workSummaryPromptState previews the clock at render time
ok 515 - workSummaryPromptState previews the clock at render time
  ---
  duration_ms: 0.257011
  type: 'test'
  ...
# Subtest: planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
ok 516 - planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
  ---
  duration_ms: 0.347454
  type: 'test'
  ...
# Subtest: planWorkLogInsertion inherits an existing space-indented child prefix
ok 517 - planWorkLogInsertion inherits an existing space-indented child prefix
  ---
  duration_ms: 0.620154
  type: 'test'
  ...
# Subtest: planWorkLogInsertion inherits an existing tab-indented child prefix
ok 518 - planWorkLogInsertion inherits an existing tab-indented child prefix
  ---
  duration_ms: 0.29849
  type: 'test'
  ...
# Subtest: planWorkLogInsertion prepends newest-first entries into existing marker spellings
ok 519 - planWorkLogInsertion prepends newest-first entries into existing marker spellings
  ---
  duration_ms: 0.964021
  type: 'test'
  ...
# Subtest: planWorkLogInsertion ignores nested child-task markers and preserves CRLF
ok 520 - planWorkLogInsertion ignores nested child-task markers and preserves CRLF
  ---
  duration_ms: 0.84309
  type: 'test'
  ...
# Subtest: planWorkLogInsertion treats blank summaries as no-op structural edits
ok 521 - planWorkLogInsertion treats blank summaries as no-op structural edits
  ---
  duration_ms: 0.270496
  type: 'test'
  ...
# Subtest: the Open-reset planner is removed: unlink plans only a Work Log insertion
ok 522 - the Open-reset planner is removed: unlink plans only a Work Log insertion
  ---
  duration_ms: 0.165746
  type: 'test'
  ...
# Subtest: unlink Work Log plan keeps the In Progress checkbox and appends one entry
ok 523 - unlink Work Log plan keeps the In Progress checkbox and appends one entry
  ---
  duration_ms: 0.218878
  type: 'test'
  ...
# Subtest: article detection accepts scalar and list frontmatter values
ok 524 - article detection accepts scalar and list frontmatter values
  ---
  duration_ms: 1.691842
  type: 'test'
  ...
# Subtest: bob resolution prefers its setting, then known install paths, then PATH
ok 525 - bob resolution prefers its setting, then known install paths, then PATH
  ---
  duration_ms: 1.016331
  type: 'test'
  ...
# Subtest: plan decoder accepts v1 and rejects a foreign schema version
ok 526 - plan decoder accepts v1 and rejects a foreign schema version
  ---
  duration_ms: 0.360749
  type: 'test'
  ...
# Subtest: bob stdin spawn passes the article contract and vault environment
ok 527 - bob stdin spawn passes the article contract and vault environment
  ---
  duration_ms: 3.479114
  type: 'test'
  ...
# Subtest: bob plan stdout decodes UTF-8 split across chunks
ok 528 - bob plan stdout decodes UTF-8 split across chunks
  ---
  duration_ms: 1.022252
  type: 'test'
  ...
# Subtest: early bob exit on stdin reports EPIPE as a run failure
ok 529 - early bob exit on stdin reports EPIPE as a run failure
  ---
  duration_ms: 0.752217
  type: 'test'
  ...
# Subtest: line hunks become minimal cursor-preserving changes
ok 530 - line hunks become minimal cursor-preserving changes
  ---
  duration_ms: 0.647256
  type: 'test'
  ...
# Subtest: insert, multi-line replace, and deletion hunks reproduce the formatted note
ok 531 - insert, multi-line replace, and deletion hunks reproduce the formatted note
  ---
  duration_ms: 4.108435
  type: 'test'
  ...
# Subtest: notice shows bob's text and at most two warning findings
ok 532 - notice shows bob's text and at most two warning findings
  ---
  duration_ms: 0.689126
  type: 'test'
  ...
# Subtest: inbound changes apply only when their target line still matches the preimage
ok 533 - inbound changes apply only when their target line still matches the preimage
  ---
  duration_ms: 0.907363
  type: 'test'
  ...
# Subtest: undo guard blocks a reformat until a fresh input or delete event
ok 534 - undo guard blocks a reformat until a fresh input or delete event
  ---
  duration_ms: 0.533639
  type: 'test'
  ...
# Subtest: leave formatting observes the undo guard before saving or reading
ok 535 - leave formatting observes the undo guard before saving or reading
  ---
  duration_ms: 0.389043
  type: 'test'
  ...
# Subtest: Convert shows bob's refusal on every invocation
ok 536 - Convert shows bob's refusal on every invocation
  ---
  duration_ms: 0.422507
  type: 'test'
  ...
# Subtest: old bob's non-JSON article response gets one update notice per session
ok 537 - old bob's non-JSON article response gets one update notice per session
  ---
  duration_ms: 0.260748
  type: 'test'
  ...
# Subtest: format drops its response if the editor changed while bob was running
ok 538 - format drops its response if the editor changed while bob was running
  ---
  duration_ms: 0.467402
  type: 'test'
  ...
# Subtest: decoration ranges mark written section numbers from the outline
ok 539 - decoration ranges mark written section numbers from the outline
  ---
  duration_ms: 1.034185
  type: 'test'
  ...
# Subtest: a new outline rerenders each open Reading view once for that generation
ok 540 - a new outline rerenders each open Reading view once for that generation
  ---
  duration_ms: 0.493954
  type: 'test'
  ...
# Subtest: section at a given line uses the innermost outline range
ok 541 - section at a given line uses the innermost outline range
  ---
  duration_ms: 0.396728
  type: 'test'
  ...
# Subtest: stale-hint debounce and in-flight state machine
ok 542 - stale-hint debounce and in-flight state machine
  ---
  duration_ms: 0.389664
  type: 'test'
  ...
# Subtest: reading-view wrapping puts the leading number token in span.bob-secno
ok 543 - reading-view wrapping puts the leading number token in span.bob-secno
  ---
  duration_ms: 0.839043
  type: 'test'
  ...
# Subtest: applied plans remap outline lines onto the formatted buffer
ok 544 - applied plans remap outline lines onto the formatted buffer
  ---
  duration_ms: 0.222004
  type: 'test'
  ...
# Subtest: article styles scope the reading look under .bob-article
ok 545 - article styles scope the reading look under .bob-article
  ---
  duration_ms: 0.598894
  type: 'test'
  ...
# Subtest: look settings default to serif typeface and stale-number hints
ok 546 - look settings default to serif typeface and stale-number hints
  ---
  duration_ms: 0.17793
  type: 'test'
  ...
# Subtest: compose arg builders match the bob gmail CLI contract
ok 547 - compose arg builders match the bob gmail CLI contract
  ---
  duration_ms: 1.836817
  type: 'test'
  ...
# Subtest: preview and error payload helpers classify bob documents
ok 548 - preview and error payload helpers classify bob documents
  ---
  duration_ms: 0.776433
  type: 'test'
  ...
# Subtest: the send modal renders the exact preview from fixture JSON
ok 549 - the send modal renders the exact preview from fixture JSON
  ---
  duration_ms: 1.56588
  type: 'test'
  ...
# Subtest: undo cancels the send before bob is called
ok 550 - undo cancels the send before bob is called
  ---
  duration_ms: 2.112373
  type: 'test'
  ...
# Subtest: a second send is ignored while one is in flight, and the digest passes through
ok 551 - a second send is ignored while one is in flight, and the digest passes through
  ---
  duration_ms: 8.317676
  type: 'test'
  ...
# Subtest: a digest mismatch re-previews instead of sending
ok 552 - a digest mismatch re-previews instead of sending
  ---
  duration_ms: 0.726909
  type: 'test'
  ...
# Subtest: the send modal ignores a double click on Send
ok 553 - the send modal ignores a double click on Send
  ---
  duration_ms: 2.461321
  type: 'test'
  ...
# Subtest: compose commands appear only with a mail-note context, except New email
ok 554 - compose commands appear only with a mail-note context, except New email
  ---
  duration_ms: 1.269985
  type: 'test'
  ...
# Subtest: picker insertion uses a rechecked editor transaction and aborts stale buffers
ok 555 - picker insertion uses a rechecked editor transaction and aborts stale buffers
  ---
  duration_ms: 2.62871
  type: 'test'
  ...
# Subtest: paste conversion replaces only an unchanged Gmail URL in the original view and file
ok 556 - paste conversion replaces only an unchanged Gmail URL in the original view and file
  ---
  duration_ms: 1.048693
  type: 'test'
  ...
# Subtest: a failed save leaves a pasted Gmail URL untouched
ok 557 - a failed save leaves a pasted Gmail URL untouched
  ---
  duration_ms: 0.494665
  type: 'test'
  ...
# Subtest: old Bob shows one update notice
ok 558 - old Bob shows one update notice
  ---
  duration_ms: 1.119649
  type: 'test'
  ...
# Subtest: commands appear according to mail-note context
ok 559 - commands appear according to mail-note context
  ---
  duration_ms: 0.970303
  type: 'test'
  ...
# Subtest: a mail URL under the cursor exposes the email context
ok 560 - a mail URL under the cursor exposes the email context
  ---
  duration_ms: 0.255037
  type: 'test'
  ...
# Subtest: task links point to the message block under the cursor
ok 561 - task links point to the message block under the cursor
  ---
  duration_ms: 0.648919
  type: 'test'
  ...
# Subtest: typed argv tokenizer handles quotes, escapes, literal shell syntax, and errors
ok 562 - typed argv tokenizer handles quotes, escapes, literal shell syntax, and errors
  ---
  duration_ms: 2.573846
  type: 'test'
  ...
# Subtest: typed argv resolves aliases to the longest catalog entry and refuses excluded paths
ok 563 - typed argv resolves aliases to the longest catalog entry and refuses excluded paths
  ---
  duration_ms: 0.956847
  type: 'test'
  ...
# Subtest: the list pins typed metadata, disabled exclusions, and the explicit Vim fallback
ok 564 - the list pins typed metadata, disabled exclusions, and the explicit Vim fallback
  ---
  duration_ms: 14.802593
  type: 'test'
  ...
# Subtest: Vim-shaped input follows the agreed positive and negative rules
ok 565 - Vim-shaped input follows the agreed positive and negative rules
  ---
  duration_ms: 0.344769
  type: 'test'
  ...
# Subtest: vimrc parser finds recursive colon mappings and exmap names
ok 566 - vimrc parser finds recursive colon mappings and exmap names
  ---
  duration_ms: 0.744853
  type: 'test'
  ...
# Subtest: argument completion passes the entry path, fixed args, and current tokens to bob
ok 567 - argument completion passes the entry path, fixed args, and current tokens to bob
  ---
  duration_ms: 6.807148
  type: 'test'
  ...
# Subtest: completion directives group candidates, preserve prefixes, and expand vault paths
ok 568 - completion directives group candidates, preserve prefixes, and expand vault paths
  ---
  duration_ms: 11.085834
  type: 'test'
  ...
# Subtest: stale completion replies are discarded and Enter reports missing required positionals
ok 569 - stale completion replies are discarded and Enter reports missing required positionals
  ---
  duration_ms: 35.714161
  type: 'test'
  ...
# Subtest: argument completion requests debounce edits by 60 ms
ok 570 - argument completion requests debounce edits by 60 ms
  ---
  duration_ms: 86.281151
  type: 'test'
  ...
# Subtest: Vim ex dispatch restores and targets the editor captured when the sheet opened
ok 571 - Vim ex dispatch restores and targets the editor captured when the sheet opened
  ---
  duration_ms: 10.483704
  type: 'test'
  ...
# Subtest: double colon enters Vim stage and Escape returns to the list
ok 572 - double colon enters Vim stage and Escape returns to the list
  ---
  duration_ms: 10.404784
  type: 'test'
  ...
# Subtest: vimrc lint reads the configured file and shows only one session notice
ok 573 - vimrc lint reads the configured file and shows only one session notice
  ---
  duration_ms: 1.043283
  type: 'test'
  ...
# Subtest: fingerprints compare path, mtime, and size
ok 574 - fingerprints compare path, mtime, and size
  ---
  duration_ms: 2.257781
  type: 'test'
  ...
# Subtest: validation accepts the fixture and rejects malformed catalogs
ok 575 - validation accepts the fixture and rejects malformed catalogs
  ---
  duration_ms: 0.522989
  type: 'test'
  ...
# Subtest: refresh fetches and validates through the real protocol
ok 576 - refresh fetches and validates through the real protocol
  ---
  duration_ms: 109.417309
  type: 'test'
  ...
# Subtest: lookup resolves entries, aliases of entries, and excluded paths
ok 577 - lookup resolves entries, aliases of entries, and excluded paths
  ---
  duration_ms: 0.646335
  type: 'test'
  ...
# Subtest: argv assembly puts preview args before fixed args
ok 578 - argv assembly puts preview args before fixed args
  ---
  duration_ms: 0.397629
  type: 'test'
  ...
# Subtest: cmRecordArgs strips a leading bob binary and leaves queued argv
ok 579 - cmRecordArgs strips a leading bob binary and leaves queued argv
  ---
  duration_ms: 0.566652
  type: 'test'
  ...
# Subtest: cmReplayRun is the inverse of cmAssembleArgv
ok 580 - cmReplayRun is the inverse of cmAssembleArgv
  ---
  duration_ms: 0.640063
  type: 'test'
  ...
# Subtest: palette entries need policy run and all-optional positionals
ok 581 - palette entries need policy run and all-optional positionals
  ---
  duration_ms: 0.273272
  type: 'test'
  ...
# Subtest: classification order: stop, spawn, timeout, signal
ok 582 - classification order: stop, spawn, timeout, signal
  ---
  duration_ms: 2.404813
  type: 'test'
  ...
# Subtest: lock phrase wins over exit codes and adapters
ok 583 - lock phrase wins over exit codes and adapters
  ---
  duration_ms: 0.239437
  type: 'test'
  ...
# Subtest: exit-code hints beat the generic rule; unknown ids are ignored
ok 584 - exit-code hints beat the generic rule; unknown ids are ignored
  ---
  duration_ms: 0.207467
  type: 'test'
  ...
# Subtest: adapters adjust the result; failures stay honest
ok 585 - adapters adjust the result; failures stay honest
  ---
  duration_ms: 0.981565
  type: 'test'
  ...
# Subtest: gcal-sync summarizes added Event Tasks, context, and MEET links
ok 586 - gcal-sync summarizes added Event Tasks, context, and MEET links
  ---
  duration_ms: 0.359507
  type: 'test'
  ...
# Subtest: gcal-sync reports unchanged and waiting outcomes
ok 587 - gcal-sync reports unchanged and waiting outcomes
  ---
  duration_ms: 0.300644
  type: 'test'
  ...
# Subtest: api.commandMode settles, never rejects, and fires the workspace event
ok 588 - api.commandMode settles, never rejects, and fires the workspace event
  ---
  duration_ms: 251.939895
  type: 'test'
  ...
# Subtest: plugin onload registers run-* commands and exposes the frozen api
ok 589 - plugin onload registers run-* commands and exposes the frozen api
  ---
  duration_ms: 70.306461
  type: 'test'
  ...
# Subtest: plugin reports missing-bob when the binary is absent
ok 590 - plugin reports missing-bob when the binary is absent
  ---
  duration_ms: 1.336833
  type: 'test'
  ...
# Subtest: runner notifies with a plain summary after each finish
ok 591 - runner notifies with a plain summary after each finish
  ---
  duration_ms: 2.847228
  type: 'test'
  ...
# Subtest: catalog outcome adapters cover command-specific results and actions
ok 592 - catalog outcome adapters cover command-specific results and actions
  ---
  duration_ms: 2.847549
  type: 'test'
  ...
# Subtest: toast classes have distinct timing and newer failures replace older cards
ok 593 - toast classes have distinct timing and newer failures replace older cards
  ---
  duration_ms: 4.686681
  type: 'test'
  ...
# Subtest: status chip waits 400 ms, tracks multiple runs, and marks overdue writers
ok 594 - status chip waits 400 ms, tracks multiple runs, and marks overdue writers
  ---
  duration_ms: 1.801751
  type: 'test'
  ...
# Subtest: OS notifications only fire for long runs while Obsidian is unfocused
ok 595 - OS notifications only fire for long runs while Obsidian is unfocused
  ---
  duration_ms: 0.588343
  type: 'test'
  ...
# Subtest: rerun-last preserves arguments and preview mode; Apply carries the replay seed
ok 596 - rerun-last preserves arguments and preview mode; Apply carries the replay seed
  ---
  duration_ms: 0.944263
  type: 'test'
  ...
# Subtest: commandModeRerun retries an applied preview-first run and Apply carries the seed
ok 597 - commandModeRerun retries an applied preview-first run and Apply carries the seed
  ---
  duration_ms: 1348.313912
  type: 'test'
  ...
# Subtest: ANSI parsing keeps SGR that splits across chunks
ok 598 - ANSI parsing keeps SGR that splits across chunks
  ---
  duration_ms: 3.160356
  type: 'test'
  ...
# Subtest: linkify positives resolve and negatives stay plain
ok 599 - linkify positives resolve and negatives stay plain
  ---
  duration_ms: 1.588454
  type: 'test'
  ...
# Subtest: JSON pretty-print mutes keys on a single document
ok 600 - JSON pretty-print mutes keys on a single document
  ---
  duration_ms: 1.077769
  type: 'test'
  ...
# Subtest: interleave replay preserves arrival order for copy
ok 601 - interleave replay preserves arrival order for copy
  ---
  duration_ms: 0.789407
  type: 'test'
  ...
# Subtest: stamped sequence runs add a step label to the pager header
ok 602 - stamped sequence runs add a step label to the pager header
  ---
  duration_ms: 2.499374
  type: 'test'
  ...
# Subtest: pager keys: scroll, wrap, search, copy, history, stop, close
ok 603 - pager keys: scroll, wrap, search, copy, history, stop, close
  ---
  duration_ms: 0.744161
  type: 'test'
  ...
# Subtest: history stepping is newest-first
ok 604 - history stepping is newest-first
  ---
  duration_ms: 0.196335
  type: 'test'
  ...
# Subtest: search matches are exact and advance
ok 605 - search matches are exact and advance
  ---
  duration_ms: 0.202847
  type: 'test'
  ...
# Subtest: status pill covers running, outcomes, and queued-behind
ok 606 - status pill covers running, outcomes, and queued-behind
  ---
  duration_ms: 0.522588
  type: 'test'
  ...
# Subtest: plugin pager opens from Output, show-last-output, history, copy, and stop
ok 607 - plugin pager opens from Output, show-last-output, history, copy, and stop
  ---
  duration_ms: 27.58274
  type: 'test'
  ...
# Subtest: writer stop needs confirmation; reads stop immediately
ok 608 - writer stop needs confirmation; reads stop immediately
  ---
  duration_ms: 9.319901
  type: 'test'
  ...
# Subtest: watching a run skips the toast
ok 609 - watching a run skips the toast
  ---
  duration_ms: 3.224178
  type: 'test'
  ...
# Subtest: pretty JSON and ANSI land in the pager body
ok 610 - pretty JSON and ANSI land in the pager body
  ---
  duration_ms: 2.880602
  type: 'test'
  ...
# Subtest: resolver prefers the explicit setting and expands home
ok 611 - resolver prefers the explicit setting and expands home
  ---
  duration_ms: 1.98979
  type: 'test'
  ...
# Subtest: resolver consults ledger-tools before the candidates
ok 612 - resolver consults ledger-tools before the candidates
  ---
  duration_ms: 0.279343
  type: 'test'
  ...
# Subtest: resolver walks candidates, records every path tried, then PATH
ok 613 - resolver walks candidates, records every path tried, then PATH
  ---
  duration_ms: 0.363173
  type: 'test'
  ...
# Subtest: child env points at the vault, honors features, and drops completion vars
ok 614 - child env points at the vault, honors features, and drops completion vars
  ---
  duration_ms: 0.58662
  type: 'test'
  ...
# Subtest: inherited NO_COLOR wins; without the color feature NO_COLOR is set
ok 615 - inherited NO_COLOR wins; without the color feature NO_COLOR is set
  ---
  duration_ms: 0.379515
  type: 'test'
  ...
# Subtest: vault base requires a local folder
ok 616 - vault base requires a local folder
  ---
  duration_ms: 0.237944
  type: 'test'
  ...
# Subtest: ansi stripping, quoting, durations, and run ids
ok 617 - ansi stripping, quoting, durations, and run ids
  ---
  duration_ms: 1.030318
  type: 'test'
  ...
# Subtest: completed read writes files, receipt, and an honest record
ok 618 - completed read writes files, receipt, and an honest record
  ---
  duration_ms: 276.47516
  type: 'test'
  ...
# Subtest: child env carries vault, features, receipt, and tool paths
ok 619 - child env carries vault, features, receipt, and tool paths
  ---
  duration_ms: 235.757739
  type: 'test'
  ...
# Subtest: literal args with spaces, quotes, and $() stay literal
ok 620 - literal args with spaces, quotes, and $() stay literal
  ---
  duration_ms: 270.68692
  type: 'test'
  ...
# Subtest: split multi-byte characters survive and big output stays intact
ok 621 - split multi-byte characters survive and big output stays intact
  ---
  duration_ms: 492.760106
  type: 'test'
  ...
# Subtest: in-memory text truncates past the cap while files keep everything
ok 622 - in-memory text truncates past the cap while files keep everything
  ---
  duration_ms: 85.663882
  type: 'test'
  ...
# Subtest: a double run is one run: duplicates share the settlement
ok 623 - a double run is one run: duplicates share the settlement
  ---
  duration_ms: 690.58699
  type: 'test'
  ...
# Subtest: writers serialize FIFO while reads run in parallel
ok 624 - writers serialize FIFO while reads run in parallel
  ---
  duration_ms: 1523.556131
  type: 'test'
  ...
# Subtest: a failed save refuses the writer
ok 625 - a failed save refuses the writer
  ---
  duration_ms: 1.865864
  type: 'test'
  ...
# Subtest: read budgets kill; writer budgets mark overdue; stop stops
ok 626 - read budgets kill; writer budgets mark overdue; stop stops
  ---
  duration_ms: 2586.23649
  type: 'test'
  ...
# Subtest: failures classify: non-zero, signals, lock, and missing bob
ok 627 - failures classify: non-zero, signals, lock, and missing bob
  ---
  duration_ms: 423.034795
  type: 'test'
  ...
# Subtest: policy and entry guards refuse with reasons
ok 628 - policy and entry guards refuse with reasons
  ---
  duration_ms: 233.251643
  type: 'test'
  ...
# Subtest: retention keeps the newest fifty and never an unfinished run
ok 629 - retention keeps the newest fifty and never an unfinished run
  ---
  duration_ms: 112.788076
  type: 'test'
  ...
# Subtest: adoption finalizes from receipts and reports unknown without one
ok 630 - adoption finalizes from receipts and reports unknown without one
  ---
  duration_ms: 3.081696
  type: 'test'
  ...
# Subtest: cmNewRecord copies a sanitized sequence stamp and omits the field otherwise
ok 631 - cmNewRecord copies a sanitized sequence stamp and omits the field otherwise
  ---
  duration_ms: 2.981425
  type: 'test'
  ...
# Subtest: step display, title, copy text, guards, continues, and focus run
ok 632 - step display, title, copy text, guards, continues, and focus run
  ---
  duration_ms: 1.795039
  type: 'test'
  ...
# Subtest: history groups by id, newest record per index wins, and states include interrupted
ok 633 - history groups by id, newest record per index wins, and states include interrupted
  ---
  duration_ms: 1.42437
  type: 'test'
  ...
# Subtest: cmRunSequence runs reads in order, stamps every record, and survives throwing hooks
ok 634 - cmRunSequence runs reads in order, stamps every record, and survives throwing hooks
  ---
  duration_ms: 794.387921
  type: 'test'
  ...
# Subtest: a failing step 2 halts the sequence and skips later steps
ok 635 - a failing step 2 halts the sequence and skips later steps
  ---
  duration_ms: 913.56435
  type: 'test'
  ...
# Subtest: attention continues the sequence
ok 636 - attention continues the sequence
  ---
  duration_ms: 1545.931916
  type: 'test'
  ...
# Subtest: an early saveAllMarkdown refusal halts with its reason
ok 637 - an early saveAllMarkdown refusal halts with its reason
  ---
  duration_ms: 556.799197
  type: 'test'
  ...
# Subtest: a stale entry_id falls back to argv
ok 638 - a stale entry_id falls back to argv
  ---
  duration_ms: 295.027118
  type: 'test'
  ...
# Subtest: resume reuses the id and history folds into one group
ok 639 - resume reuses the id and history folds into one group
  ---
  duration_ms: 884.547432
  type: 'test'
  ...
# Subtest: cancelled() stops before the next step
ok 640 - cancelled() stops before the next step
  ---
  duration_ms: 232.624284
  type: 'test'
  ...
# Subtest: plugin suppresses per-step toasts and skips chip settle for an active sequence
ok 641 - plugin suppresses per-step toasts and skips chip settle for an active sequence
  ---
  duration_ms: 344.135895
  type: 'test'
  ...
# Subtest: duplicate signatures are refused and rerun-last replays a stamped newest record
ok 642 - duplicate signatures are refused and rerun-last replays a stamped newest record
  ---
  duration_ms: 591.611542
  type: 'test'
  ...
# Subtest: rerun-last command callback points at commandModeRerunLast
ok 643 - rerun-last command callback points at commandModeRerunLast
  ---
  duration_ms: 7.516546
  type: 'test'
  ...
# Subtest: summary model covers completed, attention, halted, and stopped sequences
ok 644 - summary model covers completed, attention, halted, and stopped sequences
  ---
  duration_ms: 6.16756
  type: 'test'
  ...
# Subtest: summary card renders accessible rows and routes the body to its focus run
ok 645 - summary card renders accessible rows and routes the body to its focus run
  ---
  duration_ms: 1.438117
  type: 'test'
  ...
# Subtest: resume keeps the sequence id and skips completed steps; rerun gets a new id
ok 646 - resume keeps the sequence id and skips completed steps; rerun gets a new id
  ---
  duration_ms: 4.266429
  type: 'test'
  ...
# Subtest: Output opens the focus run and Copy writes the sequence shell line
ok 647 - Output opens the focus run and Copy writes the sequence shell line
  ---
  duration_ms: 0.935988
  type: 'test'
  ...
# Subtest: a repeated sticky sequence card replaces the previous card by signature
ok 648 - a repeated sticky sequence card replaces the previous card by signature
  ---
  duration_ms: 3.770421
  type: 'test'
  ...
# Subtest: three Ctrl+N presses move three rows, keep focus, and wrap
ok 649 - three Ctrl+N presses move three rows, keep focus, and wrap
  ---
  duration_ms: 41.473902
  type: 'test'
  ...
# Subtest: Caps Lock and layout variants navigate; Ctrl+Shift+N does not
ok 650 - Caps Lock and layout variants navigate; Ctrl+Shift+N does not
  ---
  duration_ms: 15.341609
  type: 'test'
  ...
# Subtest: Ctrl+[ matches Escape in list, args, vim, confirm, and output
ok 651 - Ctrl+[ matches Escape in list, args, vim, confirm, and output
  ---
  duration_ms: 26.934225
  type: 'test'
  ...
# Subtest: standalone pager Ctrl+[ behaves like Escape
ok 652 - standalone pager Ctrl+[ behaves like Escape
  ---
  duration_ms: 2.251621
  type: 'test'
  ...
# Subtest: focus and caret survive re-renders with scroll preserved on same query
ok 653 - focus and caret survive re-renders with scroll preserved on same query
  ---
  duration_ms: 6.209799
  type: 'test'
  ...
# Subtest: argument mode walks rendered order and Tab accepts the visible first row
ok 654 - argument mode walks rendered order and Tab accepts the visible first row
  ---
  duration_ms: 7.107874
  type: 'test'
  ...
# Subtest: row mousedown is defaultPrevented and scope fallback routes body keys once
ok 655 - row mousedown is defaultPrevented and scope fallback routes body keys once
  ---
  duration_ms: 9.560501
  type: 'test'
  ...
# Subtest: Ctrl+M marks with Caps Lock and layout; Ctrl+Shift+M is ignored
ok 656 - Ctrl+M marks with Caps Lock and layout; Ctrl+Shift+M is ignored
  ---
  duration_ms: 15.233436
  type: 'test'
  ...
# Subtest: Ctrl+[ clears pending marks like Escape
ok 657 - Ctrl+[ clears pending marks like Escape
  ---
  duration_ms: 8.085231
  type: 'test'
  ...
# Subtest: empty query walks every row with unique keys and survives a type-and-clear
ok 658 - empty query walks every row with unique keys and survives a type-and-clear
  ---
  duration_ms: 288.128945
  type: 'test'
  ...
# Subtest: production sheet render and clicks use real DOM APIs
ok 659 - production sheet render and clicks use real DOM APIs
  ---
  duration_ms: 1176.479561
  type: 'test'
  ...
# Subtest: marking, toggling, and renumbering
ok 660 - marking, toggling, and renumbering
  ---
  duration_ms: 30.122972
  type: 'test'
  ...
# Subtest: the badge and tray text
ok 661 - the badge and tray text
  ---
  duration_ms: 19.22648
  type: 'test'
  ...
# Subtest: query select-all after a mark
ok 662 - query select-all after a mark
  ---
  duration_ms: 12.847598
  type: 'test'
  ...
# Subtest: each refusal reason
ok 663 - each refusal reason
  ---
  duration_ms: 9.867196
  type: 'test'
  ...
# Subtest: Ctrl+M into argument mode, then marking from it
ok 664 - Ctrl+M into argument mode, then marking from it
  ---
  duration_ms: 11.224248
  type: 'test'
  ...
# Subtest: argument mode Ctrl+M with incomplete args shows Needs
ok 665 - argument mode Ctrl+M with incomplete args shows Needs
  ---
  duration_ms: 6.666541
  type: 'test'
  ...
# Subtest: Backspace pops the last step
ok 666 - Backspace pops the last step
  ---
  duration_ms: 26.678185
  type: 'test'
  ...
# Subtest: Esc first clears marks, second closes
ok 667 - Esc first clears marks, second closes
  ---
  duration_ms: 17.906868
  type: 'test'
  ...
# Subtest: click and Ctrl+click toggles
ok 668 - click and Ctrl+click toggles
  ---
  duration_ms: 23.412328
  type: 'test'
  ...
# Subtest: Shift+Enter with marks runs nothing
ok 669 - Shift+Enter with marks runs nothing
  ---
  duration_ms: 11.713551
  type: 'test'
  ...
# Subtest: one mark activates like Enter
ok 670 - one mark activates like Enter
  ---
  duration_ms: 211.480232
  type: 'test'
  ...
# Subtest: one confirm mark opens its card
ok 671 - one confirm mark opens its card
  ---
  duration_ms: 15.469337
  type: 'test'
  ...
# Subtest: Enter with unguarded steps closes and runs
ok 672 - Enter with unguarded steps closes and runs
  ---
  duration_ms: 32.52009
  type: 'test'
  ...
# Subtest: Enter with guards shows the review card
ok 673 - Enter with guards shows the review card
  ---
  duration_ms: 32.657713
  type: 'test'
  ...
# Subtest: Ctrl+Enter skips the card
ok 674 - Ctrl+Enter skips the card
  ---
  duration_ms: 19.753178
  type: 'test'
  ...
# Subtest: argument-mode add and run
ok 675 - argument-mode add and run
  ---
  duration_ms: 30.817588
  type: 'test'
  ...
# Subtest: the already-running hint
ok 676 - the already-running hint
  ---
  duration_ms: 18.085003
  type: 'test'
  ...
# Subtest: RECENT grouping folds one sequence into one row
ok 677 - RECENT grouping folds one sequence into one row
  ---
  duration_ms: 1.67545
  type: 'test'
  ...
# Subtest: RECENT dedupe, limit, interrupted glyph, and about lines
ok 678 - RECENT dedupe, limit, interrupted glyph, and about lines
  ---
  duration_ms: 1.237644
  type: 'test'
  ...
# Subtest: RECENT Enter reruns all steps and Ctrl+M loads and unloads them
ok 679 - RECENT Enter reruns all steps and Ctrl+M loads and unloads them
  ---
  duration_ms: 24.674805
  type: 'test'
  ...
# Subtest: clicking a descendant toggles while marks are pending
ok 680 - clicking a descendant toggles while marks are pending
  ---
  duration_ms: 24.825303
  type: 'test'
  ...
# Subtest: no-mark argument Shift+Enter still previews
ok 681 - no-mark argument Shift+Enter still previews
  ---
  duration_ms: 4.846787
  type: 'test'
  ...
# Subtest: marked argument Ctrl+Enter with a highlighted completion adds and runs now
ok 682 - marked argument Ctrl+Enter with a highlighted completion adds and runs now
  ---
  duration_ms: 30.57067
  type: 'test'
  ...
# Subtest: incomplete marked arguments leave marks and show the missing positional
ok 683 - incomplete marked arguments leave marks and show the missing positional
  ---
  duration_ms: 7.422584
  type: 'test'
  ...
# Subtest: a RECENT sequence reduced to one report uses the normal activation chain
ok 684 - a RECENT sequence reduced to one report uses the normal activation chain
  ---
  duration_ms: 429.312637
  type: 'test'
  ...
# Subtest: a RECENT sequence reduced to one confirm opens its card
ok 685 - a RECENT sequence reduced to one confirm opens its card
  ---
  duration_ms: 20.771842
  type: 'test'
  ...
# Subtest: a RECENT sequence reduced to one preview-first command previews
ok 686 - a RECENT sequence reduced to one preview-first command previews
  ---
  duration_ms: 546.75428
  type: 'test'
  ...
# Subtest: rebuildRows passes live sequence ids so a running sequence shows ⟳
ok 687 - rebuildRows passes live sequence ids so a running sequence shows ⟳
  ---
  duration_ms: 9.148895
  type: 'test'
  ...
# Subtest: an active sequence refuses a duplicate rerun without closing the sheet
ok 688 - an active sequence refuses a duplicate rerun without closing the sheet
  ---
  duration_ms: 24.050704
  type: 'test'
  ...
# Subtest: an incomplete sequence with no active id stays interrupted after reload
ok 689 - an incomplete sequence with no active id stays interrupted after reload
  ---
  duration_ms: 0.4186
  type: 'test'
  ...
# Subtest: fuzzy ranking matches every token and prefers paths, prefixes, and keywords
ok 690 - fuzzy ranking matches every token and prefers paths, prefixes, and keywords
  ---
  duration_ms: 7.144684
  type: 'test'
  ...
# Subtest: bare capture has no row but named capture rows keep theirs
ok 691 - bare capture has no row but named capture rows keep theirs
  ---
  duration_ms: 0.621186
  type: 'test'
  ...
# Subtest: unavailable rows stay visible with reasons
ok 692 - unavailable rows stay visible with reasons
  ---
  duration_ms: 0.827871
  type: 'test'
  ...
# Subtest: frecency weights recent runs and the last-ten window
ok 693 - frecency weights recent runs and the last-ten window
  ---
  duration_ms: 1.480969
  type: 'test'
  ...
# Subtest: context rows fill For this note and From clipboard
ok 694 - context rows fill For this note and From clipboard
  ---
  duration_ms: 1.090543
  type: 'test'
  ...
# Subtest: note kinds follow frontmatter type with the article rule
ok 695 - note kinds follow frontmatter type with the article rule
  ---
  duration_ms: 0.266439
  type: 'test'
  ...
# Subtest: empty query groups RECENT, note, clipboard, then catalog sections
ok 696 - empty query groups RECENT, note, clipboard, then catalog sections
  ---
  duration_ms: 0.634412
  type: 'test'
  ...
# Subtest: list keys map to intents and plain text stays unhandled
ok 697 - list keys map to intents and plain text stays unhandled
  ---
  duration_ms: 0.285406
  type: 'test'
  ...
# Subtest: help argv targets the selected row or bare bob
ok 698 - help argv targets the selected row or bare bob
  ---
  duration_ms: 0.416876
  type: 'test'
  ...
# Subtest: median duration hides fast rows under the two-second floor
ok 699 - median duration hides fast rows under the two-second floor
  ---
  duration_ms: 0.608702
  type: 'test'
  ...
# Subtest: the open command focuses an already-open sheet
ok 700 - the open command focuses an already-open sheet
  ---
  duration_ms: 14.803605
  type: 'test'
  ...
# Subtest: Enter on a report row streams it in the sheet output stage
ok 701 - Enter on a report row streams it in the sheet output stage
  ---
  duration_ms: 237.681864
  type: 'test'
  ...
# Subtest: report footer shows its running line until the output opens
ok 702 - report footer shows its running line until the output opens
  ---
  duration_ms: 16.313028
  type: 'test'
  ...
# Subtest: preview footer shows a running line while the preview is pending
ok 703 - preview footer shows a running line while the preview is pending
  ---
  duration_ms: 17.240687
  type: 'test'
  ...
# Subtest: help start failure replaces its running line with the warning hint
ok 704 - help start failure replaces its running line with the warning hint
  ---
  duration_ms: 6.524552
  type: 'test'
  ...
# Subtest: a rejected sheet run clears the running line before propagating
ok 705 - a rejected sheet run clears the running line before propagating
  ---
  duration_ms: 18.362632
  type: 'test'
  ...
# Subtest: confirm rows need Ctrl+Enter and run confirmed
ok 706 - confirm rows need Ctrl+Enter and run confirmed
  ---
  duration_ms: 234.006574
  type: 'test'
  ...
# Subtest: Shift+Enter previews first and Apply reruns without the preview flag
ok 707 - Shift+Enter previews first and Apply reruns without the preview flag
  ---
  duration_ms: 819.168881
  type: 'test'
  ...
# Subtest: api.preview opens the sheet into a preview-first row's preview stage
ok 708 - api.preview opens the sheet into a preview-first row's preview stage
  ---
  duration_ms: 268.340122
  type: 'test'
  ...
# Subtest: api.preview opens a report row in the output stage
ok 709 - api.preview opens a report row in the output stage
  ---
  duration_ms: 352.434513
  type: 'test'
  ...
# Subtest: api.preview refuses excluded, unknown, unapplied-write, and unavailable rows
ok 710 - api.preview refuses excluded, unknown, unapplied-write, and unavailable rows
  ---
  duration_ms: 4.105351
  type: 'test'
  ...
# Subtest: api.preview focuses an already-open sheet and replaces its stage
ok 711 - api.preview focuses an already-open sheet and replaces its stage
  ---
  duration_ms: 814.762405
  type: 'test'
  ...
# Subtest: missing positionals enter argument mode instead of running
ok 712 - missing positionals enter argument mode instead of running
  ---
  duration_ms: 47.562341
  type: 'test'
  ...
# Subtest: a trailing ? runs help for the selected row in the output stage
ok 713 - a trailing ? runs help for the selected row in the output stage
  ---
  duration_ms: 441.667383
  type: 'test'
  ...
# Subtest: watching the sheet output suppresses the finish toast
ok 714 - watching the sheet output suppresses the finish toast
  ---
  duration_ms: 473.503234
  type: 'test'
  ...
# Subtest: unavailable rows never activate
ok 715 - unavailable rows never activate
  ---
  duration_ms: 3.996794
  type: 'test'
  ...
# Subtest: RECENT rows drop the bob binary and keep unique keys
ok 716 - RECENT rows drop the bob binary and keep unique keys
  ---
  duration_ms: 1.100372
  type: 'test'
  ...
# Subtest: RECENT vault-sync reruns without doubling the path
ok 717 - RECENT vault-sync reruns without doubling the path
  ---
  duration_ms: 614.187874
  type: 'test'
  ...
# Subtest: two RECENT rows for one entry select one at a time
ok 718 - two RECENT rows for one entry select one at a time
  ---
  duration_ms: 409.142702
  type: 'test'
  ...
# Subtest: RECENT preview-first and confirm rows honor their guards
ok 719 - RECENT preview-first and confirm rows honor their guards
  ---
  duration_ms: 1072.159906
  type: 'test'
  ...
# Subtest: in-sheet r reruns vault-sync without doubling the path
ok 720 - in-sheet r reruns vault-sync without doubling the path
  ---
  duration_ms: 233.834035
  type: 'test'
  ...
# Subtest: hidden below 400 ms, and never settles for such runs
ok 721 - hidden below 400 ms, and never settles for such runs
  ---
  duration_ms: 3.067118
  type: 'test'
  ...
# Subtest: running keeps one mark element, brand label, tabular clock, and native tooltip
ok 722 - running keeps one mark element, brand label, tabular clock, and native tooltip
  ---
  duration_ms: 1.692152
  type: 'test'
  ...
# Subtest: two runs show count, longest clock, and click opens the newest
ok 723 - two runs show count, longest clock, and click opens the newest
  ---
  duration_ms: 1.317126
  type: 'test'
  ...
# Subtest: queued-only gives is-queued and overdue writer gives is-overdue with budget tooltip
ok 724 - queued-only gives is-queued and overdue writer gives is-overdue with budget tooltip
  ---
  duration_ms: 0.867878
  type: 'test'
  ...
# Subtest: settle shows outcome glyph for 1600 ms, then leaving, then hidden
ok 725 - settle shows outcome glyph for 1600 ms, then leaving, then hidden
  ---
  duration_ms: 0.912403
  type: 'test'
  ...
# Subtest: sequence model shows step, sequence clock, tooltip, and between-step visibility
ok 726 - sequence model shows step, sequence clock, tooltip, and between-step visibility
  ---
  duration_ms: 1.116583
  type: 'test'
  ...
# Subtest: sequence chip lazily inserts step and title before the clock and hides them when idle
ok 727 - sequence chip lazily inserts step and title before the clock and hides them when idle
  ---
  duration_ms: 5.138835
  type: 'test'
  ...
# Subtest: sequence settle displays its final step and opens the focus run
ok 728 - sequence settle displays its final step and opens the focus run
  ---
  duration_ms: 0.533639
  type: 'test'
  ...
# Subtest: a new run during a settle shows running at once and click opens the settled run
ok 729 - a new run during a settle shows running at once and click opens the settled run
  ---
  duration_ms: 0.891944
  type: 'test'
  ...
# Subtest: adopted unfinished runs appear flagged and all triggers light the indicator
ok 730 - adopted unfinished runs appear flagged and all triggers light the indicator
  ---
  duration_ms: 0.825046
  type: 'test'
  ...
# Subtest: first visible paint uses HTMLCollection semantics and preserves existing classes
ok 731 - first visible paint uses HTMLCollection semantics and preserves existing classes
  ---
  duration_ms: 0.513802
  type: 'test'
  ...
# Subtest: DOM-like repaints keep the mark and anatomy idempotent
ok 732 - DOM-like repaints keep the mark and anatomy idempotent
  ---
  duration_ms: 0.581732
  type: 'test'
  ...
# Subtest: DOM-like settle paint shows its outcome, then hides after the settle window
ok 733 - DOM-like settle paint shows its outcome, then hides after the settle window
  ---
  duration_ms: 0.389173
  type: 'test'
  ...
# Subtest: plugin status-chip path paints an HTMLCollection-like status item
ok 734 - plugin status-chip path paints an HTMLCollection-like status item
  ---
  duration_ms: 4.393091
  type: 'test'
  ...
# Subtest: BOB_CLI_DIR wins over a sibling checkout and a cache
ok 735 - BOB_CLI_DIR wins over a sibling checkout and a cache
  ---
  duration_ms: 49.538073
  type: 'test'
  ...
# Subtest: sibling bob-cli is used when BOB_CLI_DIR is unset
ok 736 - sibling bob-cli is used when BOB_CLI_DIR is unset
  ---
  duration_ms: 39.77642
  type: 'test'
  ...
# Subtest: an invalid BOB_CLI_DIR does not fall through
ok 737 - an invalid BOB_CLI_DIR does not fall through
  ---
  duration_ms: 22.022022
  type: 'test'
  ...
# Subtest: cache clone is used when no user-owned checkout exists
ok 738 - cache clone is used when no user-owned checkout exists
  ---
  duration_ms: 53.343059
  type: 'test'
  ...
# Subtest: refreshing an existing cache keeps git chatter off stdout and forwards exact paths
ok 739 - refreshing an existing cache keeps git chatter off stdout and forwards exact paths
  ---
  duration_ms: 65.442973
  type: 'test'
  ...
# Subtest: a cache clone with a foreign origin fails before fetch or reset
ok 740 - a cache clone with a foreign origin fails before fetch or reset
  ---
  duration_ms: 26.644257
  type: 'test'
  ...
# Subtest: a justfile alone is rejected as an explicit bob-cli checkout
ok 741 - a justfile alone is rejected as an explicit bob-cli checkout
  ---
  duration_ms: 22.495767
  type: 'test'
  ...
# Subtest: just failures propagate
ok 742 - just failures propagate
  ---
  duration_ms: 25.471928
  type: 'test'
  ...
# Subtest: scans multiline, one-line, and guarded literal registrations
ok 743 - scans multiline, one-line, and guarded literal registrations
  ---
  duration_ms: 4.860323
  type: 'test'
  ...
# Subtest: scans an optional addCommand call
ok 744 - scans an optional addCommand call
  ---
  duration_ms: 0.606178
  type: 'test'
  ...
# Subtest: allows addCommand references only in a typeof guard
ok 745 - allows addCommand references only in a typeof guard
  ---
  duration_ms: 0.539791
  type: 'test'
  ...
# Subtest: rejects bind, call, and aliased addCommand references with source locations
ok 746 - rejects bind, call, and aliased addCommand references with source locations
  ---
  duration_ms: 0.987326
  type: 'test'
  ...
# Subtest: expands literal command data from a constant-array forEach across source files
ok 747 - expands literal command data from a constant-array forEach across source files
  ---
  duration_ms: 1.461341
  type: 'test'
  ...
# Subtest: balances nested callback syntax and ignores misleading comments, strings, templates, and regexes
ok 748 - balances nested callback syntax and ignores misleading comments, strings, templates, and regexes
  ---
  duration_ms: 1.315283
  type: 'test'
  ...
# Subtest: decodes escaped string metadata and literal default hotkeys
ok 749 - decodes escaped string metadata and literal default hotkeys
  ---
  duration_ms: 0.678607
  type: 'test'
  ...
# Subtest: returns no commands for a plugin without registrations
ok 750 - returns no commands for a plugin without registrations
  ---
  duration_ms: 0.321114
  type: 'test'
  ...
# Subtest: fails with source locations for dynamic metadata, hotkeys, and malformed tables
ok 751 - fails with source locations for dynamic metadata, hotkeys, and malformed tables
  ---
  duration_ms: 1.71231
  type: 'test'
  ...
# Subtest: fails duplicate command ids with both registration locations
ok 752 - fails duplicate command ids with both registration locations
  ---
  duration_ms: 0.799687
  type: 'test'
  ...
# Subtest: checks drift without writes, preserves prose, and generates deterministically
ok 753 - checks drift without writes, preserves prose, and generates deterministically
  ---
  duration_ms: 50.809924
  type: 'test'
  ...
# Subtest: code-span table cells preserve backslashes and use a safe backtick fence
ok 754 - code-span table cells preserve backslashes and use a safe backtick fence
  ---
  duration_ms: 9.160063
  type: 'test'
  ...
# Subtest: does not write any output when source validation fails
ok 755 - does not write any output when source validation fails
  ---
  duration_ms: 2.174794
  type: 'test'
  ...
# Subtest: done/ fixtures mirror bob-cli byte for byte
ok 756 - done/ fixtures mirror bob-cli byte for byte
  ---
  duration_ms: 6.259396
  type: 'test'
  ...
# Subtest: every plugin helper agrees with the shared vectors
ok 757 - every plugin helper agrees with the shared vectors
  ---
  duration_ms: 0.781302
  type: 'test'
  ...
# Subtest: KB24: mark identities and folds equal the full planner for a sub-project
ok 758 - KB24: mark identities and folds equal the full planner for a sub-project
  ---
  duration_ms: 39.823811
  type: 'test'
  ...
# Subtest: KB24: mark identities and folds equal the full planner for a root
ok 759 - KB24: mark identities and folds equal the full planner for a root
  ---
  duration_ms: 3.740484
  type: 'test'
  ...
# Subtest: LP1–LP17: ledger leafness agrees with the reverted cycler walk
ok 760 - LP1–LP17: ledger leafness agrees with the reverted cycler walk
  ---
  duration_ms: 10.517727
  type: 'test'
  ...
# Subtest: api.attachments v1 sends origin and import requests to bob
ok 761 - api.attachments v1 sends origin and import requests to bob
  ---
  duration_ms: 5.142312
  type: 'test'
  ...
# Subtest: origin and import decoders validate schema and payload shape
ok 762 - origin and import decoders validate schema and payload shape
  ---
  duration_ms: 0.673827
  type: 'test'
  ...
# Subtest: attachment API preserves bob payloads through bobSpawnJson
ok 763 - attachment API preserves bob payloads through bobSpawnJson
  ---
  duration_ms: 3.400355
  type: 'test'
  ...
# Subtest: attachment API passes bob JSON failures through
ok 764 - attachment API passes bob JSON failures through
  ---
  duration_ms: 2.020369
  type: 'test'
  ...
# Subtest: attachment API refuses mobile calls and never rejects
ok 765 - attachment API refuses mobile calls and never rejects
  ---
  duration_ms: 0.439148
  type: 'test'
  ...
# Subtest: ensure argv never passes -o and ack argv carries only deduped IDs
ok 766 - ensure argv never passes -o and ack argv carries only deduped IDs
  ---
  duration_ms: 2.481399
  type: 'test'
  ...
# Subtest: ensure and ack decoders reject bad shapes without claiming success
ok 767 - ensure and ack decoders reject bad shapes without claiming success
  ---
  duration_ms: 1.108427
  type: 'test'
  ...
# Subtest: source rows expose bank ids; other block ids stay plain block ids
ok 768 - source rows expose bank ids; other block ids stay plain block ids
  ---
  duration_ms: 2.346242
  type: 'test'
  ...
# Subtest: day snapshots carry exact waiting IDs and count ID-less rows
ok 769 - day snapshots carry exact waiting IDs and count ID-less rows
  ---
  duration_ms: 0.799587
  type: 'test'
  ...
# Subtest: ack summaries never claim a full day while ID-less rows remain
ok 770 - ack summaries never claim a full day while ID-less rows remain
  ---
  duration_ms: 0.314841
  type: 'test'
  ...
# Subtest: cursor day context follows heading boundaries, not fallback lines
ok 771 - cursor day context follows heading boundaries, not fallback lines
  ---
  duration_ms: 0.929064
  type: 'test'
  ...
# Subtest: guarded checkbox plans verify the exact displayed row and day context
ok 772 - guarded checkbox plans verify the exact displayed row and day context
  ---
  duration_ms: 0.980773
  type: 'test'
  ...
# Subtest: Enter continues only complete rows and clears only empty stubs
ok 773 - Enter continues only complete rows and clears only empty stubs
  ---
  duration_ms: 0.691962
  type: 'test'
  ...
# Subtest: category completions keep declared order and insert only keys
ok 774 - category completions keep declared order and insert only keys
  ---
  duration_ms: 0.69164
  type: 'test'
  ...
# Subtest: action commands register without default hotkeys
ok 775 - action commands register without default hotkeys
  ---
  duration_ms: 1.017272
  type: 'test'
  ...
# Subtest: ack submits the exact snapshot IDs and reports remaining ID-less rows
ok 776 - ack submits the exact snapshot IDs and reports remaining ID-less rows
  ---
  duration_ms: 2.41899
  type: 'test'
  ...
# Subtest: ack refuses empty selections, busy locks, and failures without refresh
ok 777 - ack refuses empty selections, busy locks, and failures without refresh
  ---
  duration_ms: 1.112685
  type: 'test'
  ...
# Subtest: acknowledge-day snapshots the cursor day and never falls back to ack -D
ok 778 - acknowledge-day snapshots the cursor day and never falls back to ack -D
  ---
  duration_ms: 2.384594
  type: 'test'
  ...
# Subtest: ensure opens the returned path and lands the cursor on the next row
ok 779 - ensure opens the returned path and lands the cursor on the next row
  ---
  duration_ms: 1.405043
  type: 'test'
  ...
# Subtest: guarded ID-less edits flip one byte only when the snapshot still matches
ok 780 - guarded ID-less edits flip one byte only when the snapshot still matches
  ---
  duration_ms: 0.645363
  type: 'test'
  ...
# Subtest: snippet expansion never rewrites bank rows
ok 781 - snippet expansion never rewrites bank rows
  ---
  duration_ms: 0.414401
  type: 'test'
  ...
# Subtest: Enter handling inserts rows and clears stubs through the real editor
ok 782 - Enter handling inserts rows and clears stubs through the real editor
  ---
  duration_ms: 0.683165
  type: 'test'
  ...
# Subtest: bank card fence and filename frontmatter validation are explicit
ok 783 - bank card fence and filename frontmatter validation are explicit
  ---
  duration_ms: 3.248194
  type: 'test'
  ...
# Subtest: month card model keeps Bob totals, ordered category shares, account caveats, and waiting row
ok 784 - month card model keeps Bob totals, ordered category shares, account caveats, and waiting row
  ---
  duration_ms: 2.066897
  type: 'test'
  ...
# Subtest: heat strip is Monday-first, includes the whole month, and ties share a quantile
ok 785 - heat strip is Monday-first, includes the whole month, and ties share a quantile
  ---
  duration_ms: 0.64917
  type: 'test'
  ...
# Subtest: queue model sorts oldest-first, snapshots displayed IDs, and bounds existing month footer to six
ok 786 - queue model sorts oldest-first, snapshots displayed IDs, and bounds existing month footer to six
  ---
  duration_ms: 12.973759
  type: 'test'
  ...
# Subtest: daily chip distinguishes today from history and never turns missing data into zero
ok 787 - daily chip distinguishes today from history and never turns missing data into zero
  ---
  duration_ms: 0.4398
  type: 'test'
  ...
# Subtest: month card renders report data and disables days without real headings
ok 788 - month card renders report data and disables days without real headings
  ---
  duration_ms: 23.114569
  type: 'test'
  ...
# Subtest: queue card keeps account caveats visible, lists bounded report months, and sends its drawn ID snapshot
ok 789 - queue card keeps account caveats visible, lists bounded report months, and sends its drawn ID snapshot
  ---
  duration_ms: 7.411263
  type: 'test'
  ...
# Subtest: missing day headings and changed row snapshots cannot navigate to fallback line one
ok 790 - missing day headings and changed row snapshots cannot navigate to fallback line one
  ---
  duration_ms: 1.418439
  type: 'test'
  ...
# Subtest: daily chip mounts after the day strip even when it is disabled, and clicks ensure its exact date
ok 791 - daily chip mounts after the day strip even when it is disabled, and clicks ensure its exact date
  ---
  duration_ms: 4.384284
  type: 'test'
  ...
# Subtest: daily chip is hidden without bank.md and follows the cached persistent default-on preference
ok 792 - daily chip is hidden without bank.md and follows the cached persistent default-on preference
  ---
  duration_ms: 1.801932
  type: 'test'
  ...
# Subtest: disabled render children unsubscribe and unload blocks later repaint
ok 793 - disabled render children unsubscribe and unload blocks later repaint
  ---
  duration_ms: 3.289804
  type: 'test'
  ...
# Subtest: bank UI keeps narrow-pane stacking and native keyboard focus styles
ok 794 - bank UI keeps narrow-pane stacking and native keyboard focus styles
  ---
  duration_ms: 2.372181
  type: 'test'
  ...
# Subtest: bank subprocess uses bobSpawnJson with vault, timeout, and bounded output
ok 795 - bank subprocess uses bobSpawnJson with vault, timeout, and bounded output
  ---
  duration_ms: 4.838621
  type: 'test'
  ...
# Subtest: shared bob spawn maps missing binary and timeout failures
ok 796 - shared bob spawn maps missing binary and timeout failures
  ---
  duration_ms: 1.84263
  type: 'test'
  ...
# Subtest: bank cache returns stale data while revalidating and keeps a 16-entry LRU
ok 797 - bank cache returns stale data while revalidating and keeps a 16-entry LRU
  ---
  duration_ms: 3.273552
  type: 'test'
  ...
# Subtest: identical list flights coalesce and different keys spawn in parallel
ok 798 - identical list flights coalesce and different keys spawn in parallel
  ---
  duration_ms: 0.883136
  type: 'test'
  ...
# Subtest: a late older generation cannot overwrite a newer cached report
ok 799 - a late older generation cannot overwrite a newer cached report
  ---
  duration_ms: 0.659449
  type: 'test'
  ...
# Subtest: failed refresh keeps last good data stale without a retry loop
ok 800 - failed refresh keeps last good data stale without a retry loop
  ---
  duration_ms: 0.601759
  type: 'test'
  ...
# Subtest: only hub and canonical month notes invalidate, and debounce coalesces
ok 801 - only hub and canonical month notes invalidate, and debounce coalesces
  ---
  duration_ms: 2.221713
  type: 'test'
  ...
# Subtest: local midnight bumps generation and command-mode bank tag invalidates
ok 802 - local midnight bumps generation and command-mode bank tag invalidates
  ---
  duration_ms: 1.087176
  type: 'test'
  ...
# Subtest: unload clears mounts and a late result cannot repaint
ok 803 - unload clears mounts and a late result cannot repaint
  ---
  duration_ms: 0.987295
  type: 'test'
  ...
# Subtest: headless setup does not keep the process alive with a browser rollover timer
ok 804 - headless setup does not keep the process alive with a browser rollover timer
  ---
  duration_ms: 0.772476
  type: 'test'
  ...
# Subtest: bank argv is keyed by command and exact flags
ok 805 - bank argv is keyed by command and exact flags
  ---
  duration_ms: 2.411626
  type: 'test'
  ...
# Subtest: list decoder accepts the waiting fixture and keeps integer cents
ok 806 - list decoder accepts the waiting fixture and keeps integer cents
  ---
  duration_ms: 0.964692
  type: 'test'
  ...
# Subtest: report decoder preserves transfers, cash, inflows, and account caveats
ok 807 - report decoder preserves transfers, cash, inflows, and account caveats
  ---
  duration_ms: 1.091474
  type: 'test'
  ...
# Subtest: teaching-empty is success and never a zero-dollar report
ok 808 - teaching-empty is success and never a zero-dollar report
  ---
  duration_ms: 0.389203
  type: 'test'
  ...
# Subtest: malformed JSON, schema mismatch, and bob errors never become zero success
ok 809 - malformed JSON, schema mismatch, and bob errors never become zero success
  ---
  duration_ms: 0.370077
  type: 'test'
  ...
# Subtest: non-integer cents and numeric payees are rejected
ok 810 - non-integer cents and numeric payees are rejected
  ---
  duration_ms: 0.733992
  type: 'test'
  ...
# Subtest: cent formatting is exact and presentation models do not invent totals
ok 811 - cent formatting is exact and presentation models do not invent totals
  ---
  duration_ms: 0.964281
  type: 'test'
  ...
# Subtest: bank error cards explain not-found, timeout, schema, and bob errors
ok 812 - bank error cards explain not-found, timeout, schema, and bob errors
  ---
  duration_ms: 0.747738
  type: 'test'
  ...
# Subtest: only the hub and canonical month paths are bank-relevant
ok 813 - only the hub and canonical month paths are bank-relevant
  ---
  duration_ms: 14.987286
  type: 'test'
  ...
# Subtest: amount leads match the Rust grammar vectors
ok 814 - amount leads match the Rust grammar vectors
  ---
  duration_ms: 1.179122
  type: 'test'
  ...
# Subtest: day headings parse canonical, month-day, and ISO spellings
ok 815 - day headings parse canonical, month-day, and ISO spellings
  ---
  duration_ms: 1.003627
  type: 'test'
  ...
# Subtest: source scan keeps spans and ignores fences, stubs, children, and non-day sections
ok 816 - source scan keeps spans and ignores fences, stubs, children, and non-day sections
  ---
  duration_ms: 2.082889
  type: 'test'
  ...
# Subtest: empty month notes have no rows and arbitrary dollar signs are not bank rows
ok 817 - empty month notes have no rows and arbitrary dollar signs are not bank rows
  ---
  duration_ms: 0.34035
  type: 'test'
  ...
# Subtest: heading location requires a real day heading in the current source
ok 818 - heading location requires a real day heading in the current source
  ---
  duration_ms: 0.68053
  type: 'test'
  ...
# Subtest: render appends one listener-free miniature with row-identical attributes
ok 819 - render appends one listener-free miniature with row-identical attributes
  ---
  duration_ms: 2.488914
  type: 'test'
  ...
# Subtest: render decorative miniatures hide from assistive tech
ok 820 - render decorative miniatures hide from assistive tech
  ---
  duration_ms: 0.250549
  type: 'test'
  ...
# Subtest: render accepts a synthetic digit model with no source task
ok 821 - render accepts a synthetic digit model with no source task
  ---
  duration_ms: 0.167079
  type: 'test'
  ...
# Subtest: render uses the host ownerDocument, never a foreign one
ok 822 - render uses the host ownerDocument, never a foreign one
  ---
  duration_ms: 0.259205
  type: 'test'
  ...
# Subtest: render returns null for bad input, a disabled gate, or no DOM
ok 823 - render returns null for bad input, a disabled gate, or no DOM
  ---
  duration_ms: 0.529801
  type: 'test'
  ...
# Subtest: api.blockMarks v1 keeps model and adds a gated render
ok 824 - api.blockMarks v1 keeps model and adds a gated render
  ---
  duration_ms: 0.294482
  type: 'test'
  ...
# Subtest: paint covers miniature, Live Preview, and reading rows under one gate
ok 825 - paint covers miniature, Live Preview, and reading rows under one gate
  ---
  duration_ms: 2.24672
  type: 'test'
  ...
# Subtest: chip-box fallback rules are body-gated and never !important
ok 826 - chip-box fallback rules are body-gated and never !important
  ---
  duration_ms: 2.164183
  type: 'test'
  ...
# Subtest: every paint rule except the token block and motion query carries the gate
ok 827 - every paint rule except the token block and motion query carries the gate
  ---
  duration_ms: 2.262761
  type: 'test'
  ...
# Subtest: paint keeps pip geometry, reduced motion, and the 120ms budget
ok 828 - paint keeps pip geometry, reduced motion, and the 120ms budget
  ---
  duration_ms: 5.900039
  type: 'test'
  ...
# Subtest: shipped mixes match the calibrated contract ramp
ok 829 - shipped mixes match the calibrated contract ramp
  ---
  duration_ms: 1.982025
  type: 'test'
  ...
# Subtest: waiting glyphs meet 4.5:1 on their washed rows, both themes
ok 830 - waiting glyphs meet 4.5:1 on their washed rows, both themes
  ---
  duration_ms: 1.849262
  type: 'test'
  ...
# Subtest: white on the darkened held fill meets 4.5:1, both themes
ok 831 - white on the darkened held fill meets 4.5:1, both themes
  ---
  duration_ms: 1.589827
  type: 'test'
  ...
# Subtest: row tint and rail percentages ship in the gated rules
ok 832 - row tint and rail percentages ship in the gated rules
  ---
  duration_ms: 3.653959
  type: 'test'
  ...
# Subtest: helpers never throw on bad input
ok 833 - helpers never throw on bad input
  ---
  duration_ms: 0.510685
  type: 'test'
  ...
# Subtest: the plane mask is one hollow stroked path matched to the chevron
ok 834 - the plane mask is one hollow stroked path matched to the chevron
  ---
  duration_ms: 3.451212
  type: 'test'
  ...
# Subtest: awaiting paints the P1 waiting box, the plane, the row tint, and the pip
ok 835 - awaiting paints the P1 waiting box, the plane, the row tint, and the pip
  ---
  duration_ms: 1.776834
  type: 'test'
  ...
# Subtest: the plane renders as a miniature for chips and the Task Card
ok 836 - the plane renders as a miniature for chips and the Task Card
  ---
  duration_ms: 0.335561
  type: 'test'
  ...
# Subtest: Live Preview emits own-row line attributes once across visible ranges
ok 837 - Live Preview emits own-row line attributes once across visible ranges
  ---
  duration_ms: 7.41387
  type: 'test'
  ...
# Subtest: neutral rows, inline code, and fenced content stay unmarked
ok 838 - neutral rows, inline code, and fenced content stay unmarked
  ---
  duration_ms: 2.514292
  type: 'test'
  ...
# Subtest: current unsaved document text changes or removes the visible mark
ok 839 - current unsaved document text changes or removes the visible mark
  ---
  duration_ms: 2.971866
  type: 'test'
  ...
# Subtest: rebuilds on document, viewport, live-preview, path, and refresh effect, never selection alone
ok 840 - rebuilds on document, viewport, live-preview, path, and refresh effect, never selection alone
  ---
  duration_ms: 0.635995
  type: 'test'
  ...
# Subtest: hot model calls use the in-memory ladder and project lookup is memoized per path
ok 841 - hot model calls use the in-memory ladder and project lookup is memoized per path
  ---
  duration_ms: 1.790339
  type: 'test'
  ...
# Subtest: capture-phase tooltip attaches to the existing checkbox and restores owned attributes
ok 842 - capture-phase tooltip attaches to the existing checkbox and restores owned attributes
  ---
  duration_ms: 4.084832
  type: 'test'
  ...
# Subtest: runBlockMarksRefresh rebuilds dependency chip editors
ok 843 - runBlockMarksRefresh rebuilds dependency chip editors
  ---
  duration_ms: 0.352523
  type: 'test'
  ...
# Subtest: toggle is reversible, refreshes views, rerenders Tasks, and shows exact Notices
ok 844 - toggle is reversible, refreshes views, rerenders Tasks, and shows exact Notices
  ---
  duration_ms: 0.295464
  type: 'test'
  ...
# Subtest: ladder invalidation compares semantic content and resume registers each editor document
ok 845 - ladder invalidation compares semantic content and resume registers each editor document
  ---
  duration_ms: 2.356901
  type: 'test'
  ...
# Subtest: setup owns the gate and plugin-registered unload cleanup
ok 846 - setup owns the gate and plugin-registered unload cleanup
  ---
  duration_ms: 1.266128
  type: 'test'
  ...
# Subtest: requestMeasure write-pass attaches tooltips after rebuild
ok 847 - requestMeasure write-pass attaches tooltips after rebuild
  ---
  duration_ms: 2.680097
  type: 'test'
  ...
# Subtest: unscanned collect does not restore mouseover tooltip bindings
ok 848 - unscanned collect does not restore mouseover tooltip bindings
  ---
  duration_ms: 0.787053
  type: 'test'
  ...
# Subtest: prj rows fold the project tag; dep-over-prj keeps it; selection reveals
ok 849 - prj rows fold the project tag; dep-over-prj keeps it; selection reveals
  ---
  duration_ms: 2.582382
  type: 'test'
  ...
# Subtest: awaiting rows fold the \#awaiting_reply tag; losing rows keep it (AW1/AW3/AW4/AW6)
ok 850 - awaiting rows fold the \#awaiting_reply tag; losing rows keep it (AW1/AW3/AW4/AW6)
  ---
  duration_ms: 6.386889
  type: 'test'
  ...
# Subtest: registers the reading processor before field-transforming marks
ok 851 - registers the reading processor before field-transforming marks
  ---
  duration_ms: 1.932812
  type: 'test'
  ...
# Subtest: maps every family and pip from exact section source
ok 852 - maps every family and pip from exact section source
  ---
  duration_ms: 11.44622
  type: 'test'
  ...
# Subtest: section-only text uses data-line offsets; full-note text adds lineStart
ok 853 - section-only text uses data-line offsets; full-note text adds lineStart
  ---
  duration_ms: 1.280856
  type: 'test'
  ...
# Subtest: quoted tasks and nested children classify independently
ok 854 - quoted tasks and nested children classify independently
  ---
  duration_ms: 1.06278
  type: 'test'
  ...
# Subtest: cold cache stays unmarked until Tasks is ready, then sweep paints
ok 855 - cold cache stays unmarked until Tasks is ready, then sweep paints
  ---
  duration_ms: 0.981985
  type: 'test'
  ...
# Subtest: removed fields and recycled rows invalidate the retained mapping
ok 856 - removed fields and recycled rows invalidate the retained mapping
  ---
  duration_ms: 0.698154
  type: 'test'
  ...
# Subtest: mismatched status or origin stays unmarked
ok 857 - mismatched status or origin stays unmarked
  ---
  duration_ms: 0.417938
  type: 'test'
  ...
# Subtest: own-text fallback accepts raw fields and rejects transformed pills
ok 858 - own-text fallback accepts raw fields and rejects transformed pills
  ---
  duration_ms: 1.356311
  type: 'test'
  ...
# Subtest: fallback never manufactures stale from lost field information
ok 859 - fallback never manufactures stale from lost field information
  ---
  duration_ms: 0.873979
  type: 'test'
  ...
# Subtest: Dataview delayed rows use proven origin and never the query note stem
ok 860 - Dataview delayed rows use proven origin and never the query note stem
  ---
  duration_ms: 1.815567
  type: 'test'
  ...
# Subtest: query result indexes are not read as source lines
ok 861 - query result indexes are not read as source lines
  ---
  duration_ms: 0.614593
  type: 'test'
  ...
# Subtest: Tasks query rows stay excluded
ok 862 - Tasks query rows stay excluded
  ---
  duration_ms: 0.284814
  type: 'test'
  ...
# Subtest: source-note lis Tasks also classifies still take JS marks
ok 863 - source-note lis Tasks also classifies still take JS marks
  ---
  duration_ms: 4.408119
  type: 'test'
  ...
# Subtest: tooltip attributes restore when the mark leaves or the toggle turns off
ok 864 - tooltip attributes restore when the mark leaves or the toggle turns off
  ---
  duration_ms: 1.074192
  type: 'test'
  ...
# Subtest: toggle off and on reclassifies tracked hosts in place
ok 865 - toggle off and on reclassifies tracked hosts in place
  ---
  duration_ms: 1.578395
  type: 'test'
  ...
# Subtest: detached hosts dispose observers and drop owned attributes
ok 866 - detached hosts dispose observers and drop owned attributes
  ---
  duration_ms: 0.734803
  type: 'test'
  ...
# Subtest: retained canonical text survives later field-transforming processors
ok 867 - retained canonical text survives later field-transforming processors
  ---
  duration_ms: 1.670992
  type: 'test'
  ...
# Subtest: landing: recycled fallback row must drop the old scheduled reason
ok 868 - landing: recycled fallback row must drop the old scheduled reason
  ---
  duration_ms: 1.15157
  type: 'test'
  ...
# Subtest: landing: off-state sweep must preserve a later external tooltip
ok 869 - landing: off-state sweep must preserve a later external tooltip
  ---
  duration_ms: 0.777656
  type: 'test'
  ...
# Subtest: landing: a Tasks row used as processor root must stay excluded
ok 870 - landing: a Tasks row used as processor root must stay excluded
  ---
  duration_ms: 0.280997
  type: 'test'
  ...
# Subtest: landing: Dataview without proven origin must remain neutral
ok 871 - landing: Dataview without proven origin must remain neutral
  ---
  duration_ms: 0.320452
  type: 'test'
  ...
# Subtest: Dataview transformed rows recover canonical text from the Tasks cache
ok 872 - Dataview transformed rows recover canonical text from the Tasks cache
  ---
  duration_ms: 2.39272
  type: 'test'
  ...
# Subtest: Dataview file links prove origin without data-task-path
ok 873 - Dataview file links prove origin without data-task-path
  ---
  duration_ms: 0.67
  type: 'test'
  ...
# Subtest: code and pre processor roots stay excluded like Tasks roots
ok 874 - code and pre processor roots stay excluded like Tasks roots
  ---
  duration_ms: 0.344337
  type: 'test'
  ...
# Subtest: source-note fallback still paints when section mapping is absent
ok 875 - source-note fallback still paints when section mapping is absent
  ---
  duration_ms: 0.452494
  type: 'test'
  ...
# Subtest: query origin-loss and same-status origin-change invalidate retained marks
ok 876 - query origin-loss and same-status origin-change invalidate retained marks
  ---
  duration_ms: 0.836968
  type: 'test'
  ...
# Subtest: repeated off sweeps, unload, and toggle after an external aria edit
ok 877 - repeated off sweeps, unload, and toggle after an external aria edit
  ---
  duration_ms: 1.031019
  type: 'test'
  ...
# Subtest: replacement checkbox nodes do not inherit the previous node's attributes
ok 878 - replacement checkbox nodes do not inherit the previous node's attributes
  ---
  duration_ms: 0.5653
  type: 'test'
  ...
# Subtest: neutral status transition releases owned tooltip attributes
ok 879 - neutral status transition releases owned tooltip attributes
  ---
  duration_ms: 0.446683
  type: 'test'
  ...
# Subtest: BM7 folds the project tag; BM19 keeps it
ok 880 - BM7 folds the project tag; BM19 keeps it
  ---
  duration_ms: 0.869752
  type: 'test'
  ...
# Subtest: source-note lis Tasks also classifies still fold BM7 and keep BM19
ok 881 - source-note lis Tasks also classifies still fold BM7 and keep BM19
  ---
  duration_ms: 0.642006
  type: 'test'
  ...
# Subtest: AW1 folds the \#awaiting_reply pill; AW3, AW6, and prj rows keep it
ok 882 - AW1 folds the \#awaiting_reply pill; AW3, AW6, and prj rows keep it
  ---
  duration_ms: 3.018976
  type: 'test'
  ...
# Subtest: BM1–BM27 model vectors pass verbatim except Tasks-only BM24
ok 883 - BM1–BM27 model vectors pass verbatim except Tasks-only BM24
  ---
  duration_ms: 10.657643
  type: 'test'
  ...
# Subtest: BM tooltip wording and losing-reason order match the contract
ok 884 - BM tooltip wording and losing-reason order match the contract
  ---
  duration_ms: 1.461562
  type: 'test'
  ...
# Subtest: pure helpers preserve canonical eligibility, ids, digits, and decisions
ok 885 - pure helpers preserve canonical eligibility, ids, digits, and decisions
  ---
  duration_ms: 1.218397
  type: 'test'
  ...
# Subtest: memo-local open-ID index keeps duplicate task IDs and project reasons one hop
ok 886 - memo-local open-ID index keeps duplicate task IDs and project reasons one hop
  ---
  duration_ms: 1.31945
  type: 'test'
  ...
# Subtest: api.blockMarks v1 model is synchronous, frozen, toggle-aware, and neutral while cold
ok 887 - api.blockMarks v1 model is synchronous, frozen, toggle-aware, and neutral while cold
  ---
  duration_ms: 0.558427
  type: 'test'
  ...
# Subtest: model keys are stable for equal results and change with a changed mark
ok 888 - model keys are stable for equal results and change with a changed mark
  ---
  duration_ms: 0.488623
  type: 'test'
  ...
# Subtest: fold helpers: digit keys, BM1/BM8/BM9 bars, BM7/BM19 pills
ok 889 - fold helpers: digit keys, BM1/BM8/BM9 bars, BM7/BM19 pills
  ---
  duration_ms: 2.712471
  type: 'test'
  ...
# Subtest: BM24 Tasks CSS cascade: digit from future scheduled + medium, no project tag
ok 890 - BM24 Tasks CSS cascade: digit from future scheduled + medium, no project tag
  ---
  duration_ms: 4.039856
  type: 'test'
  ...
# Subtest: AW1–AW6 awaiting-reply model vectors pass verbatim
ok 891 - AW1–AW6 awaiting-reply model vectors pass verbatim
  ---
  duration_ms: 3.224839
  type: 'test'
  ...
# Subtest: awaiting owns its date: no date reason, no digit, no Also scheduled pip
ok 892 - awaiting owns its date: no date reason, no digit, no Also scheduled pip
  ---
  duration_ms: 3.552335
  type: 'test'
  ...
# Subtest: AP1–AP4 Also-replied tooltip pip vectors pass verbatim
ok 893 - AP1–AP4 Also-replied tooltip pip vectors pass verbatim
  ---
  duration_ms: 1.158834
  type: 'test'
  ...
# Subtest: awaiting tooltip omits <who> when unknown and never throws on odd who
ok 894 - awaiting tooltip omits <who> when unknown and never throws on odd who
  ---
  duration_ms: 1.139898
  type: 'test'
  ...
# Subtest: awaiting tag source is exact, quote-aware, and folds with its space
ok 895 - awaiting tag source is exact, quote-aware, and folds with its space
  ---
  duration_ms: 0.448767
  type: 'test'
  ...
# Subtest: plugin <who> lookup reads the first linked mail note through the metadata cache
ok 896 - plugin <who> lookup reads the first linked mail note through the metadata cache
  ---
  duration_ms: 1.857298
  type: 'test'
  ...
# Subtest: AW7 Tasks CSS cascade: the plane beats the digit, prj beats the plane
ok 897 - AW7 Tasks CSS cascade: the plane beats the digit, prj beats the plane
  ---
  duration_ms: 2.386899
  type: 'test'
  ...
# Subtest: BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
ok 898 - BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
  ---
  duration_ms: 7.093577
  type: 'test'
  ...
# Subtest: reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
ok 899 - reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
  ---
  duration_ms: 14.787204
  type: 'test'
  ...
# Subtest: stale, missing, canonical append, and frozen-owner models (BC8-BC10)
ok 900 - stale, missing, canonical append, and frozen-owner models (BC8-BC10)
  ---
  duration_ms: 1.163191
  type: 'test'
  ...
# Subtest: Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
ok 901 - Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
  ---
  duration_ms: 27.390623
  type: 'test'
  ...
# Subtest: Reading BLOCKS chips map when the post-processor root is the nested list
ok 902 - Reading BLOCKS chips map when the post-processor root is the nested list
  ---
  duration_ms: 2.767216
  type: 'test'
  ...
# Subtest: budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
ok 903 - budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
  ---
  duration_ms: 2.592572
  type: 'test'
  ...
# Subtest: chip builder includes the 🔑 badge and has no edit controls
ok 904 - chip builder includes the 🔑 badge and has no edit controls
  ---
  duration_ms: 1.499925
  type: 'test'
  ...
# Subtest: BLOCKS chip box covers prj, p2, stale miniatures and a throwing render
ok 905 - BLOCKS chip box covers prj, p2, stale miniatures and a throwing render
  ---
  duration_ms: 1.311495
  type: 'test'
  ...
# Subtest: RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
ok 906 - RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
  ---
  duration_ms: 8.639562
  type: 'test'
  ...
# Subtest: RBC2 hover × on a live chip calls removeDependent; notice is nav's
ok 907 - RBC2 hover × on a live chip calls removeDependent; notice is nav's
  ---
  duration_ms: 1.580188
  type: 'test'
  ...
# Subtest: RBC3 frozen, stale, and no api.blocks stay navigation-only
ok 908 - RBC3 frozen, stale, and no api.blocks stay navigation-only
  ---
  duration_ms: 1.516387
  type: 'test'
  ...
# Subtest: RBC4 Reading view matches Live Preview ＋ / ×
ok 909 - RBC4 Reading view matches Live Preview ＋ / ×
  ---
  duration_ms: 5.527848
  type: 'test'
  ...
# Subtest: setup subscribes to the command-mode run-finished workspace event
ok 910 - setup subscribes to the command-mode run-finished workspace event
  ---
  duration_ms: 1.391837
  type: 'test'
  ...
# Subtest: each invalidates tag refreshes its ledger cache and unknown tags are ignored
ok 911 - each invalidates tag refreshes its ledger cache and unknown tags are ignored
  ---
  duration_ms: 1.553035
  type: 'test'
  ...
# Subtest: duplicate tags refresh once and a failing hook never blocks the others
ok 912 - duplicate tags refresh once and a failing hook never blocks the others
  ---
  duration_ms: 0.364596
  type: 'test'
  ...
# Subtest: payloads without invalidates and setups without a workspace never throw
ok 913 - payloads without invalidates and setups without a workspace never throw
  ---
  duration_ms: 0.520404
  type: 'test'
  ...
# Subtest: collections namespace version is additive v1
ok 914 - collections namespace version is additive v1
  ---
  duration_ms: 1.301816
  type: 'test'
  ...
# Subtest: collection chip classes stay collection-specific through paint and refresh
ok 915 - collection chip classes stay collection-specific through paint and refresh
  ---
  duration_ms: 7.648857
  type: 'test'
  ...
# Subtest: projects: scalar resolved links count, lists never widen
ok 916 - projects: scalar resolved links count, lists never widen
  ---
  duration_ms: 0.487882
  type: 'test'
  ...
# Subtest: projects: templates, status, and containsAny edges
ok 917 - projects: templates, status, and containsAny edges
  ---
  duration_ms: 0.446182
  type: 'test'
  ...
# Subtest: references: exact prefix, md only, exact scalar status
ok 918 - references: exact prefix, md only, exact scalar status
  ---
  duration_ms: 0.926078
  type: 'test'
  ...
# Subtest: base contracts: accept current files, reject drift, tolerate presentation
ok 919 - base contracts: accept current files, reject drift, tolerate presentation
  ---
  duration_ms: 0.961597
  type: 'test'
  ...
# Subtest: entries: true zero vs unavailable with reason, failure isolation
ok 920 - entries: true zero vs unavailable with reason, failure isolation
  ---
  duration_ms: 0.339449
  type: 'test'
  ...
# Subtest: snapshot counts both collections once, true zero stays clickable
ok 921 - snapshot counts both collections once, true zero stays clickable
  ---
  duration_ms: 0.537217
  type: 'test'
  ...
# Subtest: snapshot never presents partial counts as final
ok 922 - snapshot never presents partial counts as final
  ---
  duration_ms: 0.514963
  type: 'test'
  ...
# Subtest: changed definitions fail closed per collection, never stale
ok 923 - changed definitions fail closed per collection, never stale
  ---
  duration_ms: 0.671372
  type: 'test'
  ...
# Subtest: renderChip links, labels, and cleans up per component
ok 924 - renderChip links, labels, and cleans up per component
  ---
  duration_ms: 0.888226
  type: 'test'
  ...
# Subtest: PENDING section excludes TODAY while the whole lane keeps it
ok 925 - PENDING section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 4.206385
  type: 'test'
  ...
# Subtest: NEXT section excludes TODAY while the whole lane keeps it
ok 926 - NEXT section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 0.602961
  type: 'test'
  ...
# Subtest: NEXT uses symbol *, not name matching
ok 927 - NEXT uses symbol *, not name matching
  ---
  duration_ms: 0.452484
  type: 'test'
  ...
# Subtest: READY badge and query agree on hide and path case variants
ok 928 - READY badge and query agree on hide and path case variants
  ---
  duration_ms: 0.826308
  type: 'test'
  ...
# Subtest: blocked uses the full list even outside the visible subset
ok 929 - blocked uses the full list even outside the visible subset
  ---
  duration_ms: 0.261129
  type: 'test'
  ...
# Subtest: duplicate block IDs, missing IDs, and reused objects stay per-row
ok 930 - duplicate block IDs, missing IDs, and reused objects stay per-row
  ---
  duration_ms: 0.699236
  type: 'test'
  ...
# Subtest: READY gating keeps exempt rows and drops NEW/ROTTEN
ok 931 - READY gating keeps exempt rows and drops NEW/ROTTEN
  ---
  duration_ms: 0.412528
  type: 'test'
  ...
# Subtest: throwing Today degrades to unavailable, never zero
ok 932 - throwing Today degrades to unavailable, never zero
  ---
  duration_ms: 66.282273
  type: 'test'
  ...
# Subtest: dashboard badges color the displayed section count and label whole-lane pressure
ok 933 - dashboard badges color the displayed section count and label whole-lane pressure
  ---
  duration_ms: 1.270046
  type: 'test'
  ...
# Subtest: dashboard section warning boundaries ignore TODAY-only whole-lane excess
ok 934 - dashboard section warning boundaries ignore TODAY-only whole-lane excess
  ---
  duration_ms: 1.329218
  type: 'test'
  ...
# Subtest: dashboard lane badge keeps unavailable data neutral
ok 935 - dashboard lane badge keeps unavailable data neutral
  ---
  duration_ms: 0.366049
  type: 'test'
  ...
# Subtest: dashboard lane paint and refresh keep color aligned with the visible section
ok 936 - dashboard lane paint and refresh keep color aligned with the visible section
  ---
  duration_ms: 11.600838
  type: 'test'
  ...
# Subtest: dashboard lane widgets refresh together and prune on unload
ok 937 - dashboard lane widgets refresh together and prune on unload
  ---
  duration_ms: 15.923072
  type: 'test'
  ...
# Subtest: daily paint matches dashboard section badges on screenshot fixtures
ok 938 - daily paint matches dashboard section badges on screenshot fixtures
  ---
  duration_ms: 51.13872
  type: 'test'
  ...
# Subtest: daily paint lane lint matches a red badge section count
ok 939 - daily paint lane lint matches a red badge section count
  ---
  duration_ms: 21.632257
  type: 'test'
  ...
# Subtest: daily and dashboard membership agree for exclusions and custom IN_PROGRESS
ok 940 - daily and dashboard membership agree for exclusions and custom IN_PROGRESS
  ---
  duration_ms: 23.972614
  type: 'test'
  ...
# Subtest: daily paint refreshes with dashboard when Today, lane, and cap change
ok 941 - daily paint refreshes with dashboard when Today, lane, and cap change
  ---
  duration_ms: 59.361638
  type: 'test'
  ...
# Subtest: older daily notes follow today's dashboard lanes
ok 942 - older daily notes follow today's dashboard lanes
  ---
  duration_ms: 15.532804
  type: 'test'
  ...
# Subtest: daily lane anchors keep shared navigation and reject stale paints
ok 943 - daily lane anchors keep shared navigation and reject stale paints
  ---
  duration_ms: 15.427987
  type: 'test'
  ...
# Subtest: daily paint stays unavailable until Tasks and Today are ready
ok 944 - daily paint stays unavailable until Tasks and Today are ready
  ---
  duration_ms: 17.218247
  type: 'test'
  ...
# Subtest: work tones: dashboard lane models carry section tones
ok 945 - work tones: dashboard lane models carry section tones
  ---
  duration_ms: 0.392209
  type: 'test'
  ...
# Subtest: T1 scheduled full-mode row gets a Fri mark inside the span
ok 946 - T1 scheduled full-mode row gets a Fri mark inside the span
  ---
  duration_ms: 4.828773
  type: 'test'
  ...
# Subtest: T2 done row maps to a completion Oct 5 mark
ok 947 - T2 done row maps to a completion Oct 5 mark
  ---
  duration_ms: 0.796622
  type: 'test'
  ...
# Subtest: T3 short-mode created span is left untouched by JS
ok 948 - T3 short-mode created span is left untouched by JS
  ---
  duration_ms: 0.430091
  type: 'test'
  ...
# Subtest: T4 pending row decorates once data-task appears; exhausted rows stay native
ok 949 - T4 pending row decorates once data-task appears; exhausted rows stay native
  ---
  duration_ms: 1.764641
  type: 'test'
  ...
# Subtest: T5 a second pass adds nothing
ok 950 - T5 a second pass adds nothing
  ---
  duration_ms: 0.480568
  type: 'test'
  ...
# Subtest: T6 task-due and task-start spans are untouched
ok 951 - T6 task-due and task-start spans are untouched
  ---
  duration_ms: 0.389624
  type: 'test'
  ...
# Subtest: T7 an invalid date is untouched
ok 952 - T7 an invalid date is untouched
  ---
  duration_ms: 0.368013
  type: 'test'
  ...
# Subtest: T8 nothing is scheduled with marks off or for connected non-Tasks elements
ok 953 - T8 nothing is scheduled with marks off or for connected non-Tasks elements
  ---
  duration_ms: 0.369305
  type: 'test'
  ...
# Subtest: T9 a Tasks-host Fri mark relabels to tomorrow on rollover
ok 954 - T9 a Tasks-host Fri mark relabels to tomorrow on rollover
  ---
  duration_ms: 1.132593
  type: 'test'
  ...
# Subtest: renderDateMarksIn schedules one shared frame for every row
ok 955 - renderDateMarksIn schedules one shared frame for every row
  ---
  duration_ms: 1.506959
  type: 'test'
  ...
# Subtest: the Tasks pass never throws on hostile input
ok 956 - the Tasks pass never throws on hostile input
  ---
  duration_ms: 0.709655
  type: 'test'
  ...
# Subtest: T10 real-DOM NodeList children decorate via direct and queued passes
ok 957 - T10 real-DOM NodeList children decorate via direct and queued passes
  ---
  duration_ms: 0.899328
  type: 'test'
  ...
# Subtest: T11 toggling off before a queued frame runs writes nothing
ok 958 - T11 toggling off before a queued frame runs writes nothing
  ---
  duration_ms: 0.819375
  type: 'test'
  ...
# Subtest: T12 a pending-row retry followed by disabling writes nothing
ok 959 - T12 a pending-row retry followed by disabling writes nothing
  ---
  duration_ms: 0.425422
  type: 'test'
  ...
# Subtest: T13 unloading before a callback runs writes nothing
ok 960 - T13 unloading before a callback runs writes nothing
  ---
  duration_ms: 3.207436
  type: 'test'
  ...
# Subtest: RT1 full-mode recurring result gets a daily mark and stays idempotent
ok 961 - RT1 full-mode recurring result gets a daily mark and stays idempotent
  ---
  duration_ms: 1.489906
  type: 'test'
  ...
# Subtest: RT2 recurring labels use the shared cadence grammar
ok 962 - RT2 recurring labels use the shared cadence grammar
  ---
  duration_ms: 1.562595
  type: 'test'
  ...
# Subtest: RT2a unknown inherited-name rules stay readable in Tasks results
ok 963 - RT2a unknown inherited-name rules stay readable in Tasks results
  ---
  duration_ms: 0.49762
  type: 'test'
  ...
# Subtest: RT3 short-mode recurring spans stay native to JS and use the CSS loop
ok 964 - RT3 short-mode recurring spans stay native to JS and use the CSS loop
  ---
  duration_ms: 1.685309
  type: 'test'
  ...
# Subtest: RT4 open checklist members keep recurrence pills without `when done`
ok 965 - RT4 open checklist members keep recurrence pills without `when done`
  ---
  duration_ms: 0.689667
  type: 'test'
  ...
# Subtest: RT5 invalid recurrence stays native and incomplete rows are retried
ok 966 - RT5 invalid recurrence stays native and incomplete rows are retried
  ---
  duration_ms: 0.864
  type: 'test'
  ...
# Subtest: styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
ok 967 - styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
  ---
  duration_ms: 2.619842
  type: 'test'
  ...
# Subtest: DATE_MARK_FIELDS lists the four dates with verbs
ok 968 - DATE_MARK_FIELDS lists the four dates with verbs
  ---
  duration_ms: 4.096935
  type: 'test'
  ...
# Subtest: DM1 created today: label, tooltip, fold, quiet field
ok 969 - DM1 created today: label, tooltip, fold, quiet field
  ---
  duration_ms: 2.934875
  type: 'test'
  ...
# Subtest: DM2 created yesterday without space after the colons
ok 970 - DM2 created yesterday without space after the colons
  ---
  duration_ms: 0.544811
  type: 'test'
  ...
# Subtest: DM3-DM6 scheduled tomorrow, weekday, and month/day labels
ok 971 - DM3-DM6 scheduled tomorrow, weekday, and month/day labels
  ---
  duration_ms: 0.362032
  type: 'test'
  ...
# Subtest: DM7 scheduled today reads with emphasis timing
ok 972 - DM7 scheduled today reads with emphasis timing
  ---
  duration_ms: 1.016151
  type: 'test'
  ...
# Subtest: DM8 past scheduled uses month/day, never a weekday
ok 973 - DM8 past scheduled uses month/day, never a weekday
  ---
  duration_ms: 0.255318
  type: 'test'
  ...
# Subtest: DM9 completion on a closed task keeps the timeline grammar
ok 974 - DM9 completion on a closed task keeps the timeline grammar
  ---
  duration_ms: 0.310353
  type: 'test'
  ...
# Subtest: DM10 cancelled across years appends the year
ok 975 - DM10 cancelled across years appends the year
  ---
  duration_ms: 0.224859
  type: 'test'
  ...
# Subtest: DM11 next-year date appends the year
ok 976 - DM11 next-year date appends the year
  ---
  duration_ms: 0.509554
  type: 'test'
  ...
# Subtest: DM12 the weekday rule wins across the year boundary
ok 977 - DM12 the weekday rule wins across the year boundary
  ---
  duration_ms: 0.603172
  type: 'test'
  ...
# Subtest: DM13 two marks in order with folds 1 and 2
ok 978 - DM13 two marks in order with folds 1 and 2
  ---
  duration_ms: 0.871846
  type: 'test'
  ...
# Subtest: DM14 created and scheduled ranges stay disjoint from the fresh mark
ok 979 - DM14 created and scheduled ranges stay disjoint from the fresh mark
  ---
  duration_ms: 0.423499
  type: 'test'
  ...
# Subtest: DM15-DM16 paren and padded brackets are canonical
ok 980 - DM15-DM16 paren and padded brackets are canonical
  ---
  duration_ms: 0.257492
  type: 'test'
  ...
# Subtest: DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
ok 981 - DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
  ---
  duration_ms: 0.540833
  type: 'test'
  ...
# Subtest: DM22 code still parses pure but decorates nothing (see Live Preview)
ok 982 - DM22 code still parses pure but decorates nothing (see Live Preview)
  ---
  duration_ms: 0.2456
  type: 'test'
  ...
# Subtest: DM23 rescheduled is untouched and never a duplicate
ok 983 - DM23 rescheduled is untouched and never a duplicate
  ---
  duration_ms: 0.219659
  type: 'test'
  ...
# Subtest: DN1-DN9 non-canonical fields get no mark
ok 984 - DN1-DN9 non-canonical fields get no mark
  ---
  duration_ms: 0.553618
  type: 'test'
  ...
# Subtest: dateMarkContentStart finds content on list, quoted, and plain lines
ok 985 - dateMarkContentStart finds content on list, quoted, and plain lines
  ---
  duration_ms: 0.176046
  type: 'test'
  ...
# Subtest: dateMarkRelativePhrase covers the exact-day phrases
ok 986 - dateMarkRelativePhrase covers the exact-day phrases
  ---
  duration_ms: 0.155276
  type: 'test'
  ...
# Subtest: dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
ok 987 - dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
  ---
  duration_ms: 0.56567
  type: 'test'
  ...
# Subtest: no model output contains a double colon
ok 988 - no model output contains a double colon
  ---
  duration_ms: 2.87439
  type: 'test'
  ...
# Subtest: a new day always changes the widget key
ok 989 - a new day always changes the widget key
  ---
  duration_ms: 0.436784
  type: 'test'
  ...
# Subtest: element structure and the decorative/inheritColor/rendered options
ok 990 - element structure and the decorative/inheritColor/rendered options
  ---
  duration_ms: 0.885461
  type: 'test'
  ...
# Subtest: Live Preview emits several decorations in ascending order
ok 991 - Live Preview emits several decorations in ascending order
  ---
  duration_ms: 2.304262
  type: 'test'
  ...
# Subtest: Live Preview reveals per field, never the whole line
ok 992 - Live Preview reveals per field, never the whole line
  ---
  duration_ms: 0.482622
  type: 'test'
  ...
# Subtest: Live Preview refuses source mode, code, and disabled marks
ok 993 - Live Preview refuses source mode, code, and disabled marks
  ---
  duration_ms: 0.745584
  type: 'test'
  ...
# Subtest: widget mousedown anchors at the field start for folds 0, 1, and 2
ok 994 - widget mousedown anchors at the field start for folds 0, 1, and 2
  ---
  duration_ms: 1.752207
  type: 'test'
  ...
# Subtest: DM24 a cursor in the folded run unfolds the mark (vim cw)
ok 995 - DM24 a cursor in the folded run unfolds the mark (vim cw)
  ---
  duration_ms: 0.443887
  type: 'test'
  ...
# Subtest: DM25 a cursor in Tasks double space unfolds only that field
ok 996 - DM25 a cursor in Tasks double space unfolds only that field
  ---
  duration_ms: 0.295845
  type: 'test'
  ...
# Subtest: a selection ending inside the run unfolds; ending at its start keeps the fold
ok 997 - a selection ending inside the run unfolds; ending at its start keeps the fold
  ---
  duration_ms: 0.339499
  type: 'test'
  ...
# Subtest: no emitted decoration ever hides a cursor, and reveal still means field overlap
ok 998 - no emitted decoration ever hides a cursor, and reveal still means field overlap
  ---
  duration_ms: 24.875098
  type: 'test'
  ...
# Subtest: dateMarkSelectionFold: reveal, unfold, fold, and garbage input
ok 999 - dateMarkSelectionFold: reveal, unfold, fold, and garbage input
  ---
  duration_ms: 0.643599
  type: 'test'
  ...
# Subtest: mousedown on an unfolded (fold-0) widget anchors at the field start
ok 1000 - mousedown on an unfolded (fold-0) widget anchors at the field start
  ---
  duration_ms: 0.679798
  type: 'test'
  ...
# Subtest: rendered views split several fields in one node
ok 1001 - rendered views split several fields in one node
  ---
  duration_ms: 2.139366
  type: 'test'
  ...
# Subtest: rendered views skip exclusions and duplicates
ok 1002 - rendered views skip exclusions and duplicates
  ---
  duration_ms: 0.900009
  type: 'test'
  ...
# Subtest: RO1 rendered marks relabel in place across midnight
ok 1003 - RO1 rendered marks relabel in place across midnight
  ---
  duration_ms: 0.719144
  type: 'test'
  ...
# Subtest: rollover dispatches once per day change and never touches widgets
ok 1004 - rollover dispatches once per day change and never touches widgets
  ---
  duration_ms: 1.871525
  type: 'test'
  ...
# Subtest: api.dateMarks v1 is additive, sync, and never throwing
ok 1005 - api.dateMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.746746
  type: 'test'
  ...
# Subtest: session toggle and onload wiring
ok 1006 - session toggle and onload wiring
  ---
  duration_ms: 34.61437
  type: 'test'
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 1007 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 0.830095
  type: 'test'
  ...
# Subtest: styles.css contract: masks, tones, repair flag, resting
ok 1008 - styles.css contract: masks, tones, repair flag, resting
  ---
  duration_ms: 7.014137
  type: 'test'
  ...
# Subtest: day identity follows the canonical path, never the tab or mtime
ok 1009 - day identity follows the canonical path, never the tab or mtime
  ---
  duration_ms: 2.61831
  type: 'test'
  ...
# Subtest: fence day parsing accepts YAML mappings and plain lines, nothing else
ok 1010 - fence day parsing accepts YAML mappings and plain lines, nothing else
  ---
  duration_ms: 0.814465
  type: 'test'
  ...
# Subtest: report selection reads the default entry, an 8-day range, or nothing
ok 1011 - report selection reads the default entry, an 8-day range, or nothing
  ---
  duration_ms: 49.885816
  type: 'test'
  ...
# Subtest: report window checks keep the page window only when it shows D
ok 1012 - report window checks keep the page window only when it shows D
  ---
  duration_ms: 14.265668
  type: 'test'
  ...
# Subtest: week-grouped default never covers D, and a cold-cache today re-selects once
ok 1013 - week-grouped default never covers D, and a cold-cache today re-selects once
  ---
  duration_ms: 108.819967
  type: 'test'
  ...
# Subtest: a report that differs only in typical repaints
ok 1014 - a report that differs only in typical repaints
  ---
  duration_ms: 56.496876
  type: 'test'
  ...
# Subtest: paint from cache costs one frame and zero spawns
ok 1015 - paint from cache costs one frame and zero spawns
  ---
  duration_ms: 47.464705
  type: 'test'
  ...
# Subtest: off-screen and hidden-tab strips spawn nothing
ok 1016 - off-screen and hidden-tab strips spawn nothing
  ---
  duration_ms: 155.945484
  type: 'test'
  ...
# Subtest: clean fresh entries never refetch, whatever changes
ok 1017 - clean fresh entries never refetch, whatever changes
  ---
  duration_ms: 129.038645
  type: 'test'
  ...
# Subtest: visible changing strips spawn at most once per 30 s
ok 1018 - visible changing strips spawn at most once per 30 s
  ---
  duration_ms: 223.165559
  type: 'test'
  ...
# Subtest: the 10-minute age rule refetches today without any change
ok 1019 - the 10-minute age rule refetches today without any change
  ---
  duration_ms: 95.943134
  type: 'test'
  ...
# Subtest: past days wait out the 10-minute gate
ok 1020 - past days wait out the 10-minute gate
  ---
  duration_ms: 131.260769
  type: 'test'
  ...
# Subtest: several strips and the page share one spawn per key
ok 1021 - several strips and the page share one spawn per key
  ---
  duration_ms: 166.214808
  type: 'test'
  ...
# Subtest: strips repaint for free when the page refreshes the shared key
ok 1022 - strips repaint for free when the page refreshes the shared key
  ---
  duration_ms: 116.409814
  type: 'test'
  ...
# Subtest: rollover re-keys today to a past day and refetches
ok 1023 - rollover re-keys today to a past day and refetches
  ---
  duration_ms: 127.386118
  type: 'test'
  ...
# Subtest: a stale-across-midnight report is never shown as so far
ok 1024 - a stale-across-midnight report is never shown as so far
  ---
  duration_ms: 93.150141
  type: 'test'
  ...
# Subtest: window-edge days fetch the 8-day range
ok 1025 - window-edge days fetch the 8-day range
  ---
  duration_ms: 88.211156
  type: 'test'
  ...
# Subtest: future days render nothing and spawn nothing
ok 1026 - future days render nothing and spawn nothing
  ---
  duration_ms: 55.731032
  type: 'test'
  ...
# Subtest: a failed refresh keeps the frame and shows the stale dot
ok 1027 - a failed refresh keeps the frame and shows the stale dot
  ---
  duration_ms: 116.771705
  type: 'test'
  ...
# Subtest: a failure with nothing cached shows the one-line error and Retry
ok 1028 - a failure with nothing cached shows the one-line error and Retry
  ---
  duration_ms: 136.38167
  type: 'test'
  ...
# Subtest: bob-not-found with nothing cached names stats.bob_path
ok 1029 - bob-not-found with nothing cached names stats.bob_path
  ---
  duration_ms: 86.821283
  type: 'test'
  ...
# Subtest: the fence parses day:, falls back to the note date, or explains itself
ok 1030 - the fence parses day:, falls back to the note date, or explains itself
  ---
  duration_ms: 168.808752
  type: 'test'
  ...
# Subtest: the fence skips hover popovers and embeds, and unregisters on unload
ok 1031 - the fence skips hover popovers and embeds, and unregisters on unload
  ---
  duration_ms: 31.549607
  type: 'test'
  ...
# Subtest: openStatsForDay pins the day, focuses the metric, and opens a new tab
ok 1032 - openStatsForDay pins the day, focuses the metric, and opens a new tab
  ---
  duration_ms: 16.504583
  type: 'test'
  ...
# Subtest: openStatsForDay opens a new tab when Stats is already open
ok 1033 - openStatsForDay opens a new tab when Stats is already open
  ---
  duration_ms: 12.512316
  type: 'test'
  ...
# Subtest: openStatsForDay keeps the page window when it already shows D
ok 1034 - openStatsForDay keeps the page window when it already shows D
  ---
  duration_ms: 131.657086
  type: 'test'
  ...
# Subtest: openStatsForDay panel themes selects the Themes view
ok 1035 - openStatsForDay panel themes selects the Themes view
  ---
  duration_ms: 126.797504
  type: 'test'
  ...
# Subtest: openStatsForDay Notices when Stats cannot open
ok 1036 - openStatsForDay Notices when Stats cannot open
  ---
  duration_ms: 27.068197
  type: 'test'
  ...
# Subtest: the page honours a pinned day on its first paint
ok 1037 - the page honours a pinned day on its first paint
  ---
  duration_ms: 101.261882
  type: 'test'
  ...
# Subtest: renderStatsResult consumes the one-shot revealPanel
ok 1038 - renderStatsResult consumes the one-shot revealPanel
  ---
  duration_ms: 88.209915
  type: 'test'
  ...
# Subtest: every strip paints facts and links with no buttons and no vault writes
ok 1039 - every strip paints facts and links with no buttons and no vault writes
  ---
  duration_ms: 112.425576
  type: 'test'
  ...
# Subtest: change bursts coalesce behind one trailing quiet window
ok 1040 - change bursts coalesce behind one trailing quiet window
  ---
  duration_ms: 137.692592
  type: 'test'
  ...
# Subtest: mobile and spawn-less hosts render nothing and spawn nothing
ok 1041 - mobile and spawn-less hosts render nothing and spawn nothing
  ---
  duration_ms: 55.342151
  type: 'test'
  ...
# Subtest: rollover synchronously skeletons visible and offscreen fences; visible refetch resolves as past
ok 1042 - rollover synchronously skeletons visible and offscreen fences; visible refetch resolves as past
  ---
  duration_ms: 225.278934
  type: 'test'
  ...
# Subtest: fit observer registers once, refits on width change, and releases
ok 1043 - fit observer registers once, refits on width change, and releases
  ---
  duration_ms: 9.04179
  type: 'test'
  ...
# Subtest: missing ResizeObserver is harmless
ok 1044 - missing ResizeObserver is harmless
  ---
  duration_ms: 0.409232
  type: 'test'
  ...
# Subtest: openStatsForDay explicit clock selects the lens, pins the day, and persists the preference
ok 1045 - openStatsForDay explicit clock selects the lens, pins the day, and persists the preference
  ---
  duration_ms: 8.77497
  type: 'test'
  ...
# Subtest: openStatsForDay explicit worked survives a remembered off-clock preference
ok 1046 - openStatsForDay explicit worked survives a remembered off-clock preference
  ---
  duration_ms: 8.471109
  type: 'test'
  ...
# Subtest: muted roots stay gray, unshaded, claim no hue, and sort before the buckets
ok 1047 - muted roots stay gray, unshaded, claim no hue, and sort before the buckets
  ---
  duration_ms: 28.438375
  type: 'test'
  ...
# Subtest: root hues follow identity order when minutes change
ok 1048 - root hues follow identity order when minutes change
  ---
  duration_ms: 0.596229
  type: 'test'
  ...
# Subtest: lane view sanitizes and cycles both -> roots -> themes -> both
ok 1049 - lane view sanitizes and cycles both -> roots -> themes -> both
  ---
  duration_ms: 0.180905
  type: 'test'
  ...
# Subtest: layout matrix: availability, skeleton, and hidden states
ok 1050 - layout matrix: availability, skeleton, and hidden states
  ---
  duration_ms: 0.810348
  type: 'test'
  ...
# Subtest: layout copy uses areas under the area fallback with exact strings
ok 1051 - layout copy uses areas under the area fallback with exact strings
  ---
  duration_ms: 0.269755
  type: 'test'
  ...
# Subtest: painter per view: order, first-row meta and switch, themes-first
ok 1052 - painter per view: order, first-row meta and switch, themes-first
  ---
  duration_ms: 9.950385
  type: 'test'
  ...
# Subtest: switch attributes, marks, and skeleton placeholder
ok 1053 - switch attributes, marks, and skeleton placeholder
  ---
  duration_ms: 8.410814
  type: 'test'
  ...
# Subtest: switch activation: click, Enter, Space call cycleLanes once with focus
ok 1054 - switch activation: click, Enter, Space call cycleLanes once with focus
  ---
  duration_ms: 3.340952
  type: 'test'
  ...
# Subtest: group aria-label names only the shown lanes
ok 1055 - group aria-label names only the shown lanes
  ---
  duration_ms: 1.697472
  type: 'test'
  ...
# Subtest: lane-enter class appears only on a same-day view change
ok 1056 - lane-enter class appears only on a same-day view change
  ---
  duration_ms: 11.589706
  type: 'test'
  ...
# Subtest: registry: a switch repaints every record without a spawn, dedupes, and restores focus
ok 1057 - registry: a switch repaints every record without a spawn, dedupes, and restores focus
  ---
  duration_ms: 51.822836
  type: 'test'
  ...
# Subtest: command Cycle Day stats bars is registered with its Notice copy
ok 1058 - command Cycle Day stats bars is registered with its Notice copy
  ---
  duration_ms: 11.904077
  type: 'test'
  ...
# Subtest: persistence remember = device: setup loads, saves, and tolerates missing storage
ok 1059 - persistence remember = device: setup loads, saves, and tolerates missing storage
  ---
  duration_ms: 57.544567
  type: 'test'
  ...
# Subtest: require time adds no eager StateEffect.define()
ok 1060 - require time adds no eager StateEffect.define()
  ---
  duration_ms: 1.606828
  type: 'test'
  ...
# Subtest: renderPlanBlock puts exactly one host first with .bob-plan after it on canonical days
ok 1061 - renderPlanBlock puts exactly one host first with .bob-plan after it on canonical days
  ---
  duration_ms: 124.873579
  type: 'test'
  ...
# Subtest: non-daily, future, dashboard, mobile, spawn-less, and excluded blocks get no host
ok 1062 - non-daily, future, dashboard, mobile, spawn-less, and excluded blocks get no host
  ---
  duration_ms: 229.435204
  type: 'test'
  ...
# Subtest: paintPlanBlock keeps the same host node first with .bob-plan after it and no strip repaint or spawn
ok 1063 - paintPlanBlock keeps the same host node first with .bob-plan after it and no strip repaint or spawn
  ---
  duration_ms: 307.962826
  type: 'test'
  ...
# Subtest: toggle and stats.day_strip remove the host and class, re-enabling restores them
ok 1064 - toggle and stats.day_strip remove the host and class, re-enabling restores them
  ---
  duration_ms: 137.771233
  type: 'test'
  ...
# Subtest: unload releases the record and its observer
ok 1065 - unload releases the record and its observer
  ---
  duration_ms: 65.881088
  type: 'test'
  ...
# Subtest: rollover attaches future blocks and repaints today as a past day
ok 1066 - rollover attaches future blocks and repaints today as a past day
  ---
  duration_ms: 131.697593
  type: 'test'
  ...
# Subtest: rollover skeletons a visible automatic today host synchronously; it resolves as past
ok 1067 - rollover skeletons a visible automatic today host synchronously; it resolves as past
  ---
  duration_ms: 252.129829
  type: 'test'
  ...
# Subtest: plan hosts never write the vault or journals
ok 1068 - plan hosts never write the vault or journals
  ---
  duration_ms: 150.380967
  type: 'test'
  ...
# Subtest: cold plan host waits for visibility: no spawn before callback, false stays zero, true fetches once
ok 1069 - cold plan host waits for visibility: no spawn before callback, false stays zero, true fetches once
  ---
  duration_ms: 189.278839
  type: 'test'
  ...
# Subtest: plan host paints synchronously from cache with zero spawn before visibility
ok 1070 - plan host paints synchronously from cache with zero spawn before visibility
  ---
  duration_ms: 79.565564
  type: 'test'
  ...
# Subtest: detached excluded blocks get no host; detached ordinary blocks attach synchronously
ok 1071 - detached excluded blocks get no host; detached ordinary blocks attach synchronously
  ---
  duration_ms: 221.736841
  type: 'test'
  ...
# Subtest: no-observer fallback attaches detached, fetches on check after connect, releases excluded
ok 1072 - no-observer fallback attaches detached, fetches on check after connect, releases excluded
  ---
  duration_ms: 325.67733
  type: 'test'
  ...
# Subtest: excluded after attach releases on the first observer callback
ok 1073 - excluded after attach releases on the first observer callback
  ---
  duration_ms: 238.378005
  type: 'test'
  ...
# Subtest: excluded processor container gets no host
ok 1074 - excluded processor container gets no host
  ---
  duration_ms: 50.930413
  type: 'test'
  ...
# Subtest: reading-view order attaches detached, virtualized stays quiet until attach
ok 1075 - reading-view order attaches detached, virtualized stays quiet until attach
  ---
  duration_ms: 203.289777
  type: 'test'
  ...
# Subtest: today host shows so far HH:MM from the fetch stamp
ok 1076 - today host shows so far HH:MM from the fetch stamp
  ---
  duration_ms: 156.502357
  type: 'test'
  ...
# Subtest: failed refresh over a cached report names the HH:MM it shows
ok 1077 - failed refresh over a cached report names the HH:MM it shows
  ---
  duration_ms: 202.568873
  type: 'test'
  ...
# Subtest: placeholder finds .bob-plan by class and toggle-off restores it first
ok 1078 - placeholder finds .bob-plan by class and toggle-off restores it first
  ---
  duration_ms: 77.143819
  type: 'test'
  ...
# Subtest: statsThemeRef prefers theme_hues names and hues, with gray fallbacks
ok 1079 - statsThemeRef prefers theme_hues names and hues, with gray fallbacks
  ---
  duration_ms: 2.220371
  type: 'test'
  ...
# Subtest: theme mix orders coloured by minutes then gray, with unnamed last
ok 1080 - theme mix orders coloured by minutes then gray, with unnamed last
  ---
  duration_ms: 15.359166
  type: 'test'
  ...
# Subtest: same-hue coloured themes take shade 0 then 1 then 2; gray is never shaded
ok 1081 - same-hue coloured themes take shade 0 then 1 then 2; gray is never shaded
  ---
  duration_ms: 1.516165
  type: 'test'
  ...
# Subtest: same-hue type shades follow label identity while segment position follows minutes
ok 1082 - same-hue type shades follow label identity while segment position follows minutes
  ---
  duration_ms: 0.390986
  type: 'test'
  ...
# Subtest: theme mix labels, ranks, overflow, titles, and aria follow the report
ok 1083 - theme mix labels, ranks, overflow, titles, and aria follow the report
  ---
  duration_ms: 4.676752
  type: 'test'
  ...
# Subtest: theme lane is omitted for zero days, missing parts, and redefined worked
ok 1084 - theme lane is omitted for zero days, missing parts, and redefined worked
  ---
  duration_ms: 6.700919
  type: 'test'
  ...
# Subtest: fallback hue uses context.themeHueFor and stays gray without it
ok 1085 - fallback hue uses context.themeHueFor and stays gray without it
  ---
  duration_ms: 0.768798
  type: 'test'
  ...
# Subtest: painter uses swatches, shades, data-lane, and no buttons on the theme lane
ok 1086 - painter uses swatches, shades, data-lane, and no buttons on the theme lane
  ---
  duration_ms: 7.997915
  type: 'test'
  ...
# Subtest: theme legend and bar open Stats on the Themes view
ok 1087 - theme legend and bar open Stats on the Themes view
  ---
  duration_ms: 10.580738
  type: 'test'
  ...
# Subtest: fitter fits both legends independently and returns the roots result
ok 1088 - fitter fits both legends independently and returns the roots result
  ---
  duration_ms: 8.79583
  type: 'test'
  ...
# Subtest: date words and day shifts use calendar integers, including leap day
ok 1089 - date words and day shifts use calendar integers, including leap day
  ---
  duration_ms: 1.814947
  type: 'test'
  ...
# Subtest: fact displays are selected from the exact day point, even with null headline and grouped input
ok 1090 - fact displays are selected from the exact day point, even with null headline and grouped input
  ---
  duration_ms: 19.885458
  type: 'test'
  ...
# Subtest: honest states carry meta text for today, past, stale today, and stale past
ok 1091 - honest states carry meta text for today, past, stale today, and stale past
  ---
  duration_ms: 3.948763
  type: 'test'
  ...
# Subtest: time mix reuses Stats area ordering and hues, with buckets last and a tooltip title
ok 1092 - time mix reuses Stats area ordering and hues, with buckets last and a tooltip title
  ---
  duration_ms: 6.742548
  type: 'test'
  ...
# Subtest: root_parent is preferred with an honest area fallback
ok 1093 - root_parent is preferred with an honest area fallback
  ---
  duration_ms: 1.059073
  type: 'test'
  ...
# Subtest: zero worked renders no Pomodoros and redefined worked omits its mix
ok 1094 - zero worked renders no Pomodoros and redefined worked omits its mix
  ---
  duration_ms: 2.373393
  type: 'test'
  ...
# Subtest: aria label carries the date, values, provisional state, and area names
ok 1095 - aria label carries the date, values, provisional state, and area names
  ---
  duration_ms: 0.569989
  type: 'test'
  ...
# Subtest: skeleton carries placeholder text per fact and the same tag and class sequence
ok 1096 - skeleton carries placeholder text per fact and the same tag and class sequence
  ---
  duration_ms: 12.107015
  type: 'test'
  ...
# Subtest: painter repaints in place, emits no buttons, and shows unavailable controls
ok 1097 - painter repaints in place, emits no buttons, and shows unavailable controls
  ---
  duration_ms: 9.391545
  type: 'test'
  ...
# Subtest: facts, mix, and Retry preserve day, focus, and new-leaf modifiers
ok 1098 - facts, mix, and Retry preserve day, focus, and new-leaf modifiers
  ---
  duration_ms: 15.29843
  type: 'test'
  ...
# Subtest: future and hidden models paint no children
ok 1099 - future and hidden models paint no children
  ---
  duration_ms: 0.34048
  type: 'test'
  ...
# Subtest: strip paints facts, legend row, then full-width bar with no buttons
ok 1100 - strip paints facts, legend row, then full-width bar with no buttons
  ---
  duration_ms: 11.487932
  type: 'test'
  ...
# Subtest: bar click opens Stats homes with day and new-leaf modifiers
ok 1101 - bar click opens Stats homes with day and new-leaf modifiers
  ---
  duration_ms: 15.949971
  type: 'test'
  ...
# Subtest: same-area roots get distinct hues and legend dots match their segments
ok 1102 - same-area roots get distinct hues and legend dots match their segments
  ---
  duration_ms: 10.695329
  type: 'test'
  ...
# Subtest: dayStripValueRuns splits numerals from units and keeps words whole
ok 1103 - dayStripValueRuns splits numerals from units and keeps words whole
  ---
  duration_ms: 0.698243
  type: 'test'
  ...
# Subtest: facts stack a label head over a faithful value with warnings in the head
ok 1104 - facts stack a label head over a faithful value with warnings in the head
  ---
  duration_ms: 149.937438
  type: 'test'
  ...
# Subtest: root-parent labels use Bob's full home label
ok 1105 - root-parent labels use Bob's full home label
  ---
  duration_ms: 10.293391
  type: 'test'
  ...
# Subtest: unfiled root paints its label in gray after real roots
ok 1106 - unfiled root paints its label in gray after real roots
  ---
  duration_ms: 1.517558
  type: 'test'
  ...
# Subtest: area roots paint the bare label with a project_label tooltip
ok 1107 - area roots paint the bare label with a project_label tooltip
  ---
  duration_ms: 9.88987
  type: 'test'
  ...
# Subtest: case-insensitive legend labels keep their full root names
ok 1108 - case-insensitive legend labels keep their full root names
  ---
  duration_ms: 1.587011
  type: 'test'
  ...
# Subtest: dayStripLegendFit fits every root, reserves the counter, and handles empty
ok 1109 - dayStripLegendFit fits every root, reserves the counter, and handles empty
  ---
  duration_ms: 0.363634
  type: 'test'
  ...
# Subtest: names mode wins only when it names strictly more roots
ok 1110 - names mode wins only when it names strictly more roots
  ---
  duration_ms: 0.18876
  type: 'test'
  ...
# Subtest: DOM glue hides overflow, writes the counter, and toggles names mode
ok 1111 - DOM glue hides overflow, writes the counter, and toggles names mode
  ---
  duration_ms: 7.29813
  type: 'test'
  ...
# Subtest: dayStripMarkState maps bool points from the bob point, never the word
ok 1112 - dayStripMarkState maps bool points from the bob point, never the word
  ---
  duration_ms: 0.822151
  type: 'test'
  ...
# Subtest: boolean facts paint an aria-hidden mark with hidden display text
ok 1113 - boolean facts paint an aria-hidden mark with hidden display text
  ---
  duration_ms: 13.306612
  type: 'test'
  ...
# Subtest: docs without createElementNS keep word runs
ok 1114 - docs without createElementNS keep word runs
  ---
  duration_ms: 1.476501
  type: 'test'
  ...
# Subtest: bool skeleton paints a round placeholder and no svg
ok 1115 - bool skeleton paints a round placeholder and no svg
  ---
  duration_ms: 6.752688
  type: 'test'
  ...
# Subtest: pending mark tooltip drops so far; numeric provisional keeps it
ok 1116 - pending mark tooltip drops so far; numeric provisional keeps it
  ---
  duration_ms: 0.671733
  type: 'test'
  ...
# Subtest: pending to met on the same host and day draws the check once
ok 1117 - pending to met on the same host and day draws the check once
  ---
  duration_ms: 5.491599
  type: 'test'
  ...
# Subtest: arrive class stays off for other mark transitions
ok 1118 - arrive class stays off for other mark transitions
  ---
  duration_ms: 42.246147
  type: 'test'
  ...
# Subtest: stroke-dashoffset lives only inside keyframes
ok 1119 - stroke-dashoffset lives only inside keyframes
  ---
  duration_ms: 12.121011
  type: 'test'
  ...
# Subtest: dayStripRef classifies bob's typical without computing it
ok 1120 - dayStripRef classifies bob's typical without computing it
  ---
  duration_ms: 0.341883
  type: 'test'
  ...
# Subtest: typical line covers every States-table row
ok 1121 - typical line covers every States-table row
  ---
  duration_ms: 10.0698
  type: 'test'
  ...
# Subtest: typical line is aria-hidden, reserved, and never a tab stop
ok 1122 - typical line is aria-hidden, reserved, and never a tab stop
  ---
  duration_ms: 54.104747
  type: 'test'
  ...
# Subtest: off-clock hint prefers Bob's display and falls back to raw Nm without arithmetic
ok 1123 - off-clock hint prefers Bob's display and falls back to raw Nm without arithmetic
  ---
  duration_ms: 2.23048
  type: 'test'
  ...
# Subtest: hint renders below WORKED beside the typical line as its own activation target
ok 1124 - hint renders below WORKED beside the typical line as its own activation target
  ---
  duration_ms: 19.638677
  type: 'test'
  ...
# Subtest: lane legends and bars keep Worked meaning while the hint opens Off-clock
ok 1125 - lane legends and bars keep Worked meaning while the hint opens Off-clock
  ---
  duration_ms: 1.269484
  type: 'test'
  ...
# Subtest: DP parse vectors
ok 1126 - DP parse vectors
  ---
  duration_ms: 3.412708
  type: 'test'
  ...
# Subtest: DC chip model vectors
ok 1127 - DC chip model vectors
  ---
  duration_ms: 2.634752
  type: 'test'
  ...
# Subtest: decoration builds one widget, reveals on cursor, skips code and ranges
ok 1128 - decoration builds one widget, reveals on cursor, skips code and ranges
  ---
  duration_ms: 10.898123
  type: 'test'
  ...
# Subtest: decoration skips paragraphs, grandchildren, and Work Log lines
ok 1129 - decoration skips paragraphs, grandchildren, and Work Log lines
  ---
  duration_ms: 1.105862
  type: 'test'
  ...
# Subtest: decoration renders chips on DP30 and still skips DP20
ok 1130 - decoration renders chips on DP30 and still skips DP20
  ---
  duration_ms: 1.194481
  type: 'test'
  ...
# Subtest: ownership check reads O(depth) lines, not the whole note
ok 1131 - ownership check reads O(depth) lines, not the whole note
  ---
  duration_ms: 1.873158
  type: 'test'
  ...
# Subtest: widget identity covers the line and the interactive flag
ok 1132 - widget identity covers the line and the interactive flag
  ---
  duration_ms: 1.983669
  type: 'test'
  ...
# Subtest: element hides actions without nav api v1
ok 1133 - element hides actions without nav api v1
  ---
  duration_ms: 3.731908
  type: 'test'
  ...
# Subtest: nav api feature detection gates actions
ok 1134 - nav api feature detection gates actions
  ---
  duration_ms: 0.57567
  type: 'test'
  ...
# Subtest: reading view decorates only the Depends-On row, hides chrome, stays idempotent
ok 1135 - reading view decorates only the Depends-On row, hides chrome, stays idempotent
  ---
  duration_ms: 4.579387
  type: 'test'
  ...
# Subtest: reading view blocked chips draw a miniature and reason line
ok 1136 - reading view blocked chips draw a miniature and reason line
  ---
  duration_ms: 2.315934
  type: 'test'
  ...
# Subtest: reading view collapses more than three Done targets to one chip
ok 1137 - reading view collapses more than three Done targets to one chip
  ---
  duration_ms: 2.112565
  type: 'test'
  ...
# Subtest: DC chip model vectors by id: DC2, DC5, DC6, DC9
ok 1138 - DC chip model vectors by id: DC2, DC5, DC6, DC9
  ---
  duration_ms: 0.473845
  type: 'test'
  ...
# Subtest: chip actions send the 0-based line index through nav api v1
ok 1139 - chip actions send the 0-based line index through nav api v1
  ---
  duration_ms: 1.81163
  type: 'test'
  ...
# Subtest: chip hover passes the chip element and its row to the preview
ok 1140 - chip hover passes the chip element and its row to the preview
  ---
  duration_ms: 0.386528
  type: 'test'
  ...
# Subtest: chip lookup index lives on the freshness memo
ok 1141 - chip lookup index lives on the freshness memo
  ---
  duration_ms: 0.904878
  type: 'test'
  ...
# Subtest: reading view hides actions when the line cannot be derived
ok 1142 - reading view hides actions when the line cannot be derived
  ---
  duration_ms: 31.615582
  type: 'test'
  ...
# Subtest: reading view actions carry the derived 0-based line
ok 1143 - reading view actions carry the derived 0-based line
  ---
  duration_ms: 3.643399
  type: 'test'
  ...
# Subtest: reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
ok 1144 - reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
  ---
  duration_ms: 0.886853
  type: 'test'
  ...
# Subtest: reading view renders chips on DP30 (owner is a task under a Work Log entry)
ok 1145 - reading view renders chips on DP30 (owner is a task under a Work Log entry)
  ---
  duration_ms: 0.979451
  type: 'test'
  ...
# Subtest: reading view DP30 row actions send the owned Depends-On line
ok 1146 - reading view DP30 row actions send the owned Depends-On line
  ---
  duration_ms: 3.155076
  type: 'test'
  ...
# Subtest: reading view second-row remove sends the second line when two tasks share a prerequisite
ok 1147 - reading view second-row remove sends the second line when two tasks share a prerequisite
  ---
  duration_ms: 2.62817
  type: 'test'
  ...
# Subtest: chip lookup index builds once per freshness memo
ok 1148 - chip lookup index builds once per freshness memo
  ---
  duration_ms: 0.69131
  type: 'test'
  ...
# Subtest: decoration evaluates ownership without copying the note
ok 1149 - decoration evaluates ownership without copying the note
  ---
  duration_ms: 0.732439
  type: 'test'
  ...
# Subtest: blockMarkReasonLine keeps only the first tooltip line
ok 1150 - blockMarkReasonLine keeps only the first tooltip line
  ---
  duration_ms: 0.150998
  type: 'test'
  ...
# Subtest: chip box fill keeps a CSS fallback glyph beside the miniature
ok 1151 - chip box fill keeps a CSS fallback glyph beside the miniature
  ---
  duration_ms: 0.664479
  type: 'test'
  ...
# Subtest: toggle flips the body class and onload wires chips
ok 1152 - toggle flips the body class and onload wires chips
  ---
  duration_ms: 28.76547
  type: 'test'
  ...
# event-link-times build: 7.1 ms
# Subtest: EL — ledger rows qualify exactly per the contract
ok 1153 - EL — ledger rows qualify exactly per the contract
  ---
  duration_ms: 7.643827
  type: 'test'
  ...
# Subtest: EL18 — a fenced ledger row gets no pill
ok 1154 - EL18 — a fenced ledger row gets no pill
  ---
  duration_ms: 0.604665
  type: 'test'
  ...
# Subtest: EL19 — a non-daily note gets no pills
ok 1155 - EL19 — a non-daily note gets no pills
  ---
  duration_ms: 0.205653
  type: 'test'
  ...
# Subtest: EL16 — the previous day's ledger pills without state
ok 1156 - EL16 — the previous day's ledger pills without state
  ---
  duration_ms: 6.26697
  type: 'test'
  ...
# Subtest: ES — the shared clock answers the contract states
ok 1157 - ES — the shared clock answers the contract states
  ---
  duration_ms: 0.776954
  type: 'test'
  ...
# Subtest: ER — resolution matches the Events pill inputs
ok 1158 - ER — resolution matches the Events pill inputs
  ---
  duration_ms: 9.447465
  type: 'test'
  ...
# Subtest: ER — non-events, duplicates, and cross-note links resolve to no pill
ok 1159 - ER — non-events, duplicates, and cross-note links resolve to no pill
  ---
  duration_ms: 0.831438
  type: 'test'
  ...
# Subtest: ER5 — Live Preview reads the live document, unsaved edits included
ok 1160 - ER5 — Live Preview reads the live document, unsaved edits included
  ---
  duration_ms: 11.512429
  type: 'test'
  ...
# Subtest: ER6 — Live Preview dashes an unsaved off-clock tag on the same frame
ok 1161 - ER6 — Live Preview dashes an unsaved off-clock tag on the same frame
  ---
  duration_ms: 3.454948
  type: 'test'
  ...
# Subtest: ER7 — the inner pill carries the Events pill attributes, minus title
ok 1162 - ER7 — the inner pill carries the Events pill attributes, minus title
  ---
  duration_ms: 9.240707
  type: 'test'
  ...
# Subtest: ET — tooltips name the event and its pill state
ok 1163 - ET — tooltips name the event and its pill state
  ---
  duration_ms: 1.629923
  type: 'test'
  ...
# Subtest: EP1 — Live Preview places the pill at the link start, side -3
ok 1164 - EP1 — Live Preview places the pill at the link start, side -3
  ---
  duration_ms: 3.507148
  type: 'test'
  ...
# Subtest: EP4 — selection alone never rebuilds the pills
ok 1165 - EP4 — selection alone never rebuilds the pills
  ---
  duration_ms: 4.866956
  type: 'test'
  ...
# Subtest: EP2/EP5 — Reading view orders the pill before progress marks and keeps the ledger context
ok 1166 - EP2/EP5 — Reading view orders the pill before progress marks and keeps the ledger context
  ---
  duration_ms: 6.23561
  type: 'test'
  ...
# Subtest: EP3 — the pill lands before the link container beside a trailing chip
ok 1167 - EP3 — the pill lands before the link container beside a trailing chip
  ---
  duration_ms: 0.897223
  type: 'test'
  ...
# Subtest: EP3/OC — Reading sweeps preserve pill/link/marks/chip order and clock parity
ok 1168 - EP3/OC — Reading sweeps preserve pill/link/marks/chip order and clock parity
  ---
  duration_ms: 13.217184
  type: 'test'
  ...
# Subtest: EP7 — a struck link keeps the pill outside the strike
ok 1169 - EP7 — a struck link keeps the pill outside the strike
  ---
  duration_ms: 3.717629
  type: 'test'
  ...
# Subtest: EL20 — either toggle off hides every pill, in JS and CSS
ok 1170 - EL20 — either toggle off hides every pill, in JS and CSS
  ---
  duration_ms: 3.581741
  type: 'test'
  ...
# Subtest: setup — toggle command, popout gates, and clock repaint wiring
ok 1171 - setup — toggle command, popout gates, and clock repaint wiring
  ---
  duration_ms: 2.337745
  type: 'test'
  ...
# Subtest: liveness — metadata and vault events coalesce into one refresh
ok 1172 - liveness — metadata and vault events coalesce into one refresh
  ---
  duration_ms: 0.661764
  type: 'test'
  ...
# Subtest: liveness — a source-text fill refreshes link pills
ok 1173 - liveness — a source-text fill refreshes link pills
  ---
  duration_ms: 1.163272
  type: 'test'
  ...
# Subtest: perf — one build over a 200-link ledger stays under 25 ms
ok 1174 - perf — one build over a 200-link ledger stays under 25 ms
  ---
  duration_ms: 22.154014
  type: 'test'
  ...
# Subtest: widget — identity follows time, state, clock, buffer, and tooltip
ok 1175 - widget — identity follows time, state, clock, buffer, and tooltip
  ---
  duration_ms: 2.003266
  type: 'test'
  ...
# Subtest: regression FakeNode hides the plan-host cycles and builds 85 nodes
ok 1176 - regression FakeNode hides the plan-host cycles and builds 85 nodes
  ---
  duration_ms: 7.172266
  type: 'test'
  ...
# Subtest: failing assert.equal and assert.deepEqual report under a 1024MB cap
ok 1177 - failing assert.equal and assert.deepEqual report under a 1024MB cap
  ---
  duration_ms: 133.382231
  type: 'test'
  ...
# Subtest: every ledger-tools FakeNode-style fake has a descriptor and hides its cyclic fields
ok 1178 - every ledger-tools FakeNode-style fake has a descriptor and hides its cyclic fields
  ---
  duration_ms: 13.137863
  type: 'test'
  ...
# Subtest: FL1-FL16: the ledger link gates match the display contract
ok 1179 - FL1-FL16: the ledger link gates match the display contract
  ---
  duration_ms: 11.54457
  type: 'test'
  ...
# Subtest: motion identity is the resolved owner path and block ID
ok 1180 - motion identity is the resolved owner path and block ID
  ---
  duration_ms: 3.772947
  type: 'test'
  ...
# Subtest: duplicate and aliased links resolve and count once per owner per build
ok 1181 - duplicate and aliased links resolve and count once per owner per build
  ---
  duration_ms: 1.982526
  type: 'test'
  ...
# Subtest: offscreen ledger targets do no resolution or count work until visible
ok 1182 - offscreen ledger targets do no resolution or count work until visible
  ---
  duration_ms: 0.491829
  type: 'test'
  ...
# Subtest: 200-link / 2000-task build stays within the 25 ms budget
ok 1183 - 200-link / 2000-task build stays within the 25 ms budget
  ---
  duration_ms: 40.324156
  type: 'test'
  ...
# Subtest: FC1-FC17: counts follow the BLOCKS last-blocker set
ok 1184 - FC1-FC17: counts follow the BLOCKS last-blocker set
  ---
  duration_ms: 20.190141
  type: 'test'
  ...
# Subtest: FT1-FT6: tooltips use BLOCKS order, clean titles, and waiting count
ok 1185 - FT1-FT6: tooltips use BLOCKS order, clean titles, and waiting count
  ---
  duration_ms: 1.088278
  type: 'test'
  ...
# Subtest: FC7-FC8: project and hidden labels follow the contract
ok 1186 - FC7-FC8: project and hidden labels follow the contract
  ---
  duration_ms: 0.490387
  type: 'test'
  ...
# Subtest: FP1-FP2: Live Preview places the widget after the link with side 2
ok 1187 - FP1-FP2: Live Preview places the widget after the link with side 2
  ---
  duration_ms: 1.935577
  type: 'test'
  ...
# Subtest: FP3-FP4: Reading view inserts after the link or after 🔓
ok 1188 - FP3-FP4: Reading view inserts after the link or after 🔓
  ---
  duration_ms: 1.940326
  type: 'test'
  ...
# Subtest: Reading view inserts beside a task-link-mark sibling and through one wrapping p
ok 1189 - Reading view inserts beside a task-link-mark sibling and through one wrapping p
  ---
  duration_ms: 1.862016
  type: 'test'
  ...
# Subtest: pinned midnight invalidates yesterday and gives today's editor a silent first paint
ok 1190 - pinned midnight invalidates yesterday and gives today's editor a silent first paint
  ---
  duration_ms: 1.865122
  type: 'test'
  ...
# Subtest: FT element and widget keep accessible attributes without a title
ok 1191 - FT element and widget keep accessible attributes without a title
  ---
  duration_ms: 0.769319
  type: 'test'
  ...
# Subtest: Live Preview tick LRU tracks 0 → N, count changes, and the 2000-key bound
ok 1192 - Live Preview tick LRU tracks 0 → N, count changes, and the 2000-key bound
  ---
  duration_ms: 1.595658
  type: 'test'
  ...
# Subtest: viewport-only rebuilds update visible count history without animating scroll-in
ok 1193 - viewport-only rebuilds update visible count history without animating scroll-in
  ---
  duration_ms: 0.872657
  type: 'test'
  ...
# Subtest: toggle, refresh effect, and modifier navigation are wired
ok 1194 - toggle, refresh effect, and modifier navigation are wired
  ---
  duration_ms: 1.255799
  type: 'test'
  ...
# Subtest: setup is idempotent and teardown clears the rollover interval
ok 1195 - setup is idempotent and teardown clears the rollover interval
  ---
  duration_ms: 0.310833
  type: 'test'
  ...
# Subtest: capability: nav card v2 is capable
ok 1196 - capability: nav card v2 is capable
  ---
  duration_ms: 1.610095
  type: 'test'
  ...
# Subtest: capability: nav card v1 is not capable
ok 1197 - capability: nav card v1 is not capable
  ---
  duration_ms: 0.27193
  type: 'test'
  ...
# Subtest: capability: absent nav, missing api, and old versions are not capable
ok 1198 - capability: absent nav, missing api, and old versions are not capable
  ---
  duration_ms: 0.198469
  type: 'test'
  ...
# Subtest: capability: a throwing app never throws
ok 1199 - capability: a throwing app never throws
  ---
  duration_ms: 0.278773
  type: 'test'
  ...
# Subtest: lane capability: nav card v3 is lane-capable, v2 is not
ok 1200 - lane capability: nav card v3 is lane-capable, v2 is not
  ---
  duration_ms: 0.279384
  type: 'test'
  ...
# Subtest: leaf: active capable due choice replaces refresh with a leaf
ok 1201 - leaf: active capable due choice replaces refresh with a leaf
  ---
  duration_ms: 3.917732
  type: 'test'
  ...
# Subtest: leaf: the same row without the card keeps refresh and counting words
ok 1202 - leaf: the same row without the card keeps refresh and counting words
  ---
  duration_ms: 0.772645
  type: 'test'
  ...
# Subtest: leaf: early dates still leaf when capable
ok 1203 - leaf: early dates still leaf when capable
  ---
  duration_ms: 0.532006
  type: 'test'
  ...
# Subtest: leaf: decay-off rows never leaf even when capable
ok 1204 - leaf: decay-off rows never leaf even when capable
  ---
  duration_ms: 0.966776
  type: 'test'
  ...
# Subtest: leaf: below-threshold rows never leaf
ok 1205 - leaf: below-threshold rows never leaf
  ---
  duration_ms: 0.944945
  type: 'test'
  ...
# Subtest: leaf: threshold zero asks on every due re-confirmation when capable
ok 1206 - leaf: threshold zero asks on every due re-confirmation when capable
  ---
  duration_ms: 0.442775
  type: 'test'
  ...
# Subtest: leaf: overflow renders capped dots with +N and the exact count in text
ok 1207 - leaf: overflow renders capped dots with +N and the exact count in text
  ---
  duration_ms: 0.291026
  type: 'test'
  ...
# Subtest: leaf: out-of-scope and closed tasks show dots quietly, never a leaf
ok 1208 - leaf: out-of-scope and closed tasks show dots quietly, never a leaf
  ---
  duration_ms: 1.028804
  type: 'test'
  ...
# Subtest: leaf: unresolved marks show dots quietly with counting-only wording
ok 1209 - leaf: unresolved marks show dots quietly with counting-only wording
  ---
  duration_ms: 0.294653
  type: 'test'
  ...
# Subtest: element: leaf marks carry data-decide true and a leaf path
ok 1210 - element: leaf marks carry data-decide true and a leaf path
  ---
  duration_ms: 0.878729
  type: 'test'
  ...
# Subtest: element: non-decision marks carry data-decide false
ok 1211 - element: non-decision marks carry data-decide false
  ---
  duration_ms: 0.365228
  type: 'test'
  ...
# Subtest: lane leaf: an at-limit Next row leaves only with the v3 card
ok 1212 - lane leaf: an at-limit Next row leaves only with the v3 card
  ---
  duration_ms: 0.339037
  type: 'test'
  ...
# Subtest: lane leaf: the same row with only the v2 card keeps counting pips
ok 1213 - lane leaf: the same row with only the v2 card keeps counting pips
  ---
  duration_ms: 0.317817
  type: 'test'
  ...
# Subtest: lane leaf: an at-limit WIP row leaves only with the v3 card
ok 1214 - lane leaf: an at-limit WIP row leaves only with the v3 card
  ---
  duration_ms: 0.41907
  type: 'test'
  ...
# Subtest: lane leaf: a false rung counts and displays but never asks
ok 1215 - lane leaf: a false rung counts and displays but never asks
  ---
  duration_ms: 0.321665
  type: 'test'
  ...
# Subtest: lane leaf: a per-rung limit drives the keeps wording
ok 1216 - lane leaf: a per-rung limit drives the keeps wording
  ---
  duration_ms: 0.293741
  type: 'test'
  ...
# Subtest: footer groups omit every zero tier and keep walk order
ok 1217 - footer groups omit every zero tier and keep walk order
  ---
  duration_ms: 2.878738
  type: 'test'
  ...
# Subtest: PRE and POST groups bracket the nine-tier queue and expose completion hints
ok 1218 - PRE and POST groups bracket the nine-tier queue and expose completion hints
  ---
  duration_ms: 1.089922
  type: 'test'
  ...
# Subtest: a NEW-state project appears only in its walk tier
ok 1219 - a NEW-state project appears only in its walk tier
  ---
  duration_ms: 0.236171
  type: 'test'
  ...
# Subtest: empty queue hides the footer even with upkeep or a met budget
ok 1220 - empty queue hides the footer even with upkeep or a met budget
  ---
  duration_ms: 0.223467
  type: 'test'
  ...
# Subtest: unavailable or missing data never render false counts
ok 1221 - unavailable or missing data never render false counts
  ---
  duration_ms: 0.218498
  type: 'test'
  ...
# Subtest: generic summary names due, commitments, and nonempty groups
ok 1222 - generic summary names due, commitments, and nonempty groups
  ---
  duration_ms: 0.368113
  type: 'test'
  ...
# Subtest: current-task context uses shared ranks and compact wording
ok 1223 - current-task context uses shared ranks and compact wording
  ---
  duration_ms: 0.761344
  type: 'test'
  ...
# Subtest: only ROTTEN remaining names commitments done or a met budget
ok 1224 - only ROTTEN remaining names commitments done or a met budget
  ---
  duration_ms: 0.269915
  type: 'test'
  ...
# Subtest: NEW and commitments take precedence over a met budget
ok 1225 - NEW and commitments take precedence over a met budget
  ---
  duration_ms: 0.406066
  type: 'test'
  ...
# Subtest: reviewEntryView compact and detail cover the original freshness tiers
ok 1226 - reviewEntryView compact and detail cover the original freshness tiers
  ---
  duration_ms: 0.775932
  type: 'test'
  ...
# Subtest: cursor matching requires a unique verified identity
ok 1227 - cursor matching requires a unique verified identity
  ---
  duration_ms: 0.39266
  type: 'test'
  ...
# Subtest: footer paint hides the host and keeps a stable button
ok 1228 - footer paint hides the host and keeps a stable button
  ---
  duration_ms: 1.519251
  type: 'test'
  ...
# Subtest: groups paint as tier-keyed tokens and repaint without stale nodes
ok 1229 - groups paint as tier-keyed tokens and repaint without stale nodes
  ---
  duration_ms: 0.96885
  type: 'test'
  ...
# Subtest: group boundary marks only the commitments-to-upkeep cut
ok 1230 - group boundary marks only the commitments-to-upkeep cut
  ---
  duration_ms: 0.589456
  type: 'test'
  ...
# Subtest: context ink follows supported current tiers and clears on other views
ok 1231 - context ink follows supported current tiers and clears on other views
  ---
  duration_ms: 0.681342
  type: 'test'
  ...
# Subtest: progressive fit sheds tail groups, then detail, hint, and meter
ok 1232 - progressive fit sheds tail groups, then detail, hint, and meter
  ---
  duration_ms: 1.592721
  type: 'test'
  ...
# Subtest: the footer stylesheet defines every tier ink and removes NEW accent overrides
ok 1233 - the footer stylesheet defines every tier ink and removes NEW accent overrides
  ---
  duration_ms: 2.787854
  type: 'test'
  ...
# Subtest: status bar 0-1-0 transitions hide without a reload
ok 1234 - status bar 0-1-0 transitions hide without a reload
  ---
  duration_ms: 39.893594
  type: 'test'
  ...
# Subtest: cursor-only updates reuse a warm memo
ok 1235 - cursor-only updates reuse a warm memo
  ---
  duration_ms: 12.927862
  type: 'test'
  ...
# Subtest: unload disconnects the observer and click handler
ok 1236 - unload disconnects the observer and click handler
  ---
  duration_ms: 25.957028
  type: 'test'
  ...
# Subtest: queue-built ranks agree with the footer current entry
ok 1237 - queue-built ranks agree with the footer current entry
  ---
  duration_ms: 1.652806
  type: 'test'
  ...
# Subtest: footer short labels map every tier
ok 1238 - footer short labels map every tier
  ---
  duration_ms: 0.190073
  type: 'test'
  ...
# Subtest: current-row footer context uses short labels while entry views keep full labels
ok 1239 - current-row footer context uses short labels while entry views keep full labels
  ---
  duration_ms: 0.351802
  type: 'test'
  ...
# Subtest: legend line lists only current abbreviated tiers
ok 1240 - legend line lists only current abbreviated tiers
  ---
  duration_ms: 10.427995
  type: 'test'
  ...
# Subtest: queue-row quickRoll preview takes the hint slot, tooltip, and aria
ok 1241 - queue-row quickRoll preview takes the hint slot, tooltip, and aria
  ---
  duration_ms: 0.834374
  type: 'test'
  ...
# Subtest: quickRoll detail sits next to the action hint on lane rows
ok 1242 - quickRoll detail sits next to the action hint on lane rows
  ---
  duration_ms: 1.46041
  type: 'test'
  ...
# Subtest: missing or failed quickRoll leaves a queue-row footer byte-identical
ok 1243 - missing or failed quickRoll leaves a queue-row footer byte-identical
  ---
  duration_ms: 0.412047
  type: 'test'
  ...
# Subtest: off-walk prioritized preview replaces ]s next
ok 1244 - off-walk prioritized preview replaces ]s next
  ---
  duration_ms: 0.364326
  type: 'test'
  ...
# Subtest: off-walk assign or kind-less preview keeps ]s next
ok 1245 - off-walk assign or kind-less preview keeps ]s next
  ---
  duration_ms: 0.248064
  type: 'test'
  ...
# Subtest: empty queue with a prioritized preview paints a hint-only footer
ok 1246 - empty queue with a prioritized preview paints a hint-only footer
  ---
  duration_ms: 0.291236
  type: 'test'
  ...
# Subtest: PRE rows stay unchanged under the nav checklist-tier contract
ok 1247 - PRE rows stay unchanged under the nav checklist-tier contract
  ---
  duration_ms: 0.283472
  type: 'test'
  ...
# Subtest: status bar wires nav api.quickRoll into the hint slot
ok 1248 - status bar wires nav api.quickRoll into the hint slot
  ---
  duration_ms: 22.74866
  type: 'test'
  ...
# Subtest: empty-queue status bar previews only a checkbox task line
ok 1249 - empty-queue status bar previews only a checkbox task line
  ---
  duration_ms: 51.766989
  type: 'test'
  ...
# Subtest: off-walk task preview works with a queue and survives its 1-to-0 transition
ok 1250 - off-walk task preview works with a queue and survives its 1-to-0 transition
  ---
  duration_ms: 26.232454
  type: 'test'
  ...
# Subtest: status bar ignores missing, v0, or throwing quickRoll namespaces
ok 1251 - status bar ignores missing, v0, or throwing quickRoll namespaces
  ---
  duration_ms: 62.250241
  type: 'test'
  ...
# Subtest: answer tiers list only tickler
ok 1252 - answer tiers list only tickler
  ---
  duration_ms: 0.318659
  type: 'test'
  ...
# Subtest: freshnessFooterAnswerChip builds structured segments for every kind
ok 1253 - freshnessFooterAnswerChip builds structured segments for every kind
  ---
  duration_ms: 1.317166
  type: 'test'
  ...
# Subtest: a TICK row with a preview has answer set and unchanged hint, tooltip, and aria
ok 1254 - a TICK row with a preview has answer set and unchanged hint, tooltip, and aria
  ---
  duration_ms: 0.520304
  type: 'test'
  ...
# Subtest: a TICK view paints the answer chip and reuses or clears it by key
ok 1255 - a TICK view paints the answer chip and reuses or clears it by key
  ---
  duration_ms: 0.815588
  type: 'test'
  ...
# Subtest: a TICK fit sheds the meter before the hint chip
ok 1256 - a TICK fit sheds the meter before the hint chip
  ---
  duration_ms: 0.82222
  type: 'test'
  ...
# Subtest: the footer stylesheet defines the TICK answer chip
ok 1257 - the footer stylesheet defines the TICK answer chip
  ---
  duration_ms: 1.562895
  type: 'test'
  ...
# Subtest: K1 absent: no keeps means 0 with no lints
ok 1258 - K1 absent: no keeps means 0 with no lints
  ---
  duration_ms: 4.173621
  type: 'test'
  ...
# Subtest: K8 misplaced: keeps inside the Tasks suffix reads with a lint
ok 1259 - K8 misplaced: keeps inside the Tasks suffix reads with a lint
  ---
  duration_ms: 0.876083
  type: 'test'
  ...
# Subtest: K9 duplicates and invalid values: first valid wins, else 0
ok 1260 - K9 duplicates and invalid values: first valid wins, else 0
  ---
  duration_ms: 0.854311
  type: 'test'
  ...
# Subtest: K10 ceiling and NEW: 999 reads, never-confirmed reads 0
ok 1261 - K10 ceiling and NEW: 999 reads, never-confirmed reads 0
  ---
  duration_ms: 0.352023
  type: 'test'
  ...
# Subtest: K13 exact keys: near-miss keys are not keeps; parens read
ok 1262 - K13 exact keys: near-miss keys are not keeps; parens read
  ---
  duration_ms: 0.284213
  type: 'test'
  ...
# Subtest: keeps value parser accepts only decimal 1-999
ok 1263 - keeps value parser accepts only decimal 1-999
  ---
  duration_ms: 0.260247
  type: 'test'
  ...
# Subtest: K2 first valid canonical: uncounted keep preserves and repairs
ok 1264 - K2 first valid canonical: uncounted keep preserves and repairs
  ---
  duration_ms: 1.277029
  type: 'test'
  ...
# Subtest: K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
ok 1265 - K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
  ---
  duration_ms: 0.828101
  type: 'test'
  ...
# Subtest: K4 same-day preserve noop: canonical kept line is byte-identical
ok 1266 - K4 same-day preserve noop: canonical kept line is byte-identical
  ---
  duration_ms: 0.57616
  type: 'test'
  ...
# Subtest: K5 generic stamp clears, even same-day
ok 1267 - K5 generic stamp clears, even same-day
  ---
  duration_ms: 0.69635
  type: 'test'
  ...
# Subtest: K6 set-refresh clears keeps
ok 1268 - K6 set-refresh clears keeps
  ---
  duration_ms: 0.375667
  type: 'test'
  ...
# Subtest: K7 stale stamp clears keeps
ok 1269 - K7 stale stamp clears keeps
  ---
  duration_ms: 0.257762
  type: 'test'
  ...
# Subtest: K8b misplaced keeps repaired to canonical order by a keep
ok 1270 - K8b misplaced keeps repaired to canonical order by a keep
  ---
  duration_ms: 0.326344
  type: 'test'
  ...
# Subtest: K11 refusals preserve: closed and recurring lines never write
ok 1271 - K11 refusals preserve: closed and recurring lines never write
  ---
  duration_ms: 0.359476
  type: 'test'
  ...
# Subtest: Pomodoro ledger rows are refused byte-for-byte by counted and uncounted keep
ok 1272 - Pomodoro ledger rows are refused byte-for-byte by counted and uncounted keep
  ---
  duration_ms: 0.67586
  type: 'test'
  ...
# Subtest: counted keep increments a stale streak once in the same write
ok 1273 - counted keep increments a stale streak once in the same write
  ---
  duration_ms: 0.347845
  type: 'test'
  ...
# Subtest: first counted keep on a streakless due task writes keeps 1
ok 1274 - first counted keep on a streakless due task writes keeps 1
  ---
  duration_ms: 0.331974
  type: 'test'
  ...
# Subtest: counted keep saturates at 999 and never wraps
ok 1275 - counted keep saturates at 999 and never wraps
  ---
  duration_ms: 0.421204
  type: 'test'
  ...
# Subtest: counted keep needs a valid prior fresh before today
ok 1276 - counted keep needs a valid prior fresh before today
  ---
  duration_ms: 0.545292
  type: 'test'
  ...
# Subtest: counted keep repairs malformed and duplicate placement
ok 1277 - counted keep repairs malformed and duplicate placement
  ---
  duration_ms: 0.491378
  type: 'test'
  ...
# Subtest: uncounted keep preserves the valid value while canonicalizing
ok 1278 - uncounted keep preserves the valid value while canonicalizing
  ---
  duration_ms: 0.357663
  type: 'test'
  ...
# Subtest: UB13 keep on an unblock TICKLER preserves the streak and skips the card
ok 1279 - UB13 keep on an unblock TICKLER preserves the streak and skips the card
  ---
  duration_ms: 1.325983
  type: 'test'
  ...
# Subtest: a scheduled tickler still counts when schedule wins an unblock tie
ok 1280 - a scheduled tickler still counts when schedule wins an unblock tie
  ---
  duration_ms: 0.612069
  type: 'test'
  ...
# Subtest: decay normalization: absent, null, true, and {} enable with 3
ok 1281 - decay normalization: absent, null, true, and {} enable with 3
  ---
  duration_ms: 1.469176
  type: 'test'
  ...
# Subtest: decay false counts and displays but never asks
ok 1282 - decay false counts and displays but never asks
  ---
  duration_ms: 0.203759
  type: 'test'
  ...
# Subtest: decay keeps 0 and fixed entry normalize
ok 1283 - decay keeps 0 and fixed entry normalize
  ---
  duration_ms: 0.239166
  type: 'test'
  ...
# Subtest: C14 pending override resolves while other rungs fall back
ok 1284 - C14 pending override resolves while other rungs fall back
  ---
  duration_ms: 0.192798
  type: 'test'
  ...
# Subtest: C15 fallback plus next override
ok 1285 - C15 fallback plus next override
  ---
  duration_ms: 0.19391
  type: 'test'
  ...
# Subtest: C16 zero, false, and 999 rungs
ok 1286 - C16 zero, false, and 999 rungs
  ---
  duration_ms: 0.302858
  type: 'test'
  ...
# Subtest: C17 null rung falls back to keeps
ok 1287 - C17 null rung falls back to keeps
  ---
  duration_ms: 0.454127
  type: 'test'
  ...
# Subtest: rung limit helper resolves numbers, false, and fallbacks
ok 1288 - rung limit helper resolves numbers, false, and fallbacks
  ---
  duration_ms: 0.186376
  type: 'test'
  ...
# Subtest: invalid decay shapes fail the freshness config contract
ok 1289 - invalid decay shapes fail the freshness config contract
  ---
  duration_ms: 0.553527
  type: 'test'
  ...
# Subtest: B: at-limit Ready due rows decide on every local day
ok 1290 - B: at-limit Ready due rows decide on every local day
  ---
  duration_ms: 0.955255
  type: 'test'
  ...
# Subtest: D1 early date: an at-limit Ready due row decides
ok 1291 - D1 early date: an at-limit Ready due row decides
  ---
  duration_ms: 0.195192
  type: 'test'
  ...
# Subtest: D2 at limit decides; D3 below limit stamps without a card
ok 1292 - D2 at limit decides; D3 below limit stamps without a card
  ---
  duration_ms: 2.882205
  type: 'test'
  ...
# Subtest: D4 tickler counts as due; D5 NEW never decides
ok 1293 - D4 tickler counts as due; D5 NEW never decides
  ---
  duration_ms: 0.310994
  type: 'test'
  ...
# Subtest: D6 zero limit asks on every due Ready re-confirmation
ok 1294 - D6 zero limit asks on every due Ready re-confirmation
  ---
  duration_ms: 0.154305
  type: 'test'
  ...
# Subtest: D7 off never asks; D8 an at-limit Next due row decides
ok 1295 - D7 off never asks; D8 an at-limit Next due row decides
  ---
  duration_ms: 0.162531
  type: 'test'
  ...
# Subtest: D9 pending at limit decides; D10-D11 below limit stay quiet
ok 1296 - D9 pending at limit decides; D10-D11 below limit stay quiet
  ---
  duration_ms: 0.164214
  type: 'test'
  ...
# Subtest: D12 next_keeps false never asks; D13 pending_keeps 0 always asks
ok 1297 - D12 next_keeps false never asks; D13 pending_keeps 0 always asks
  ---
  duration_ms: 0.354337
  type: 'test'
  ...
# Subtest: D14 today-linked lane rows never decide
ok 1298 - D14 today-linked lane rows never decide
  ---
  duration_ms: 0.138895
  type: 'test'
  ...
# Subtest: D15 projects never decide; D16 unblock ticklers never decide
ok 1299 - D15 projects never decide; D16 unblock ticklers never decide
  ---
  duration_ms: 0.152391
  type: 'test'
  ...
# Subtest: D17-D18 next_keeps override of 5 decides at 5, quiet at 4
ok 1300 - D17-D18 next_keeps override of 5 decides at 5, quiet at 4
  ---
  duration_ms: 0.1784
  type: 'test'
  ...
# Subtest: lane rows decide through the evaluator, queue, and counts
ok 1301 - lane rows decide through the evaluator, queue, and counts
  ---
  duration_ms: 3.151871
  type: 'test'
  ...
# Subtest: evaluator, queue, and counts carry keeps and decide
ok 1302 - evaluator, queue, and counts carry keeps and decide
  ---
  duration_ms: 3.615816
  type: 'test'
  ...
# Subtest: no keeps: the existing mark is unchanged
ok 1303 - no keeps: the existing mark is unchanged
  ---
  duration_ms: 1.54981
  type: 'test'
  ...
# Subtest: aging with two keeps: faint pips plus a counting-only line
ok 1304 - aging with two keeps: faint pips plus a counting-only line
  ---
  duration_ms: 0.454738
  type: 'test'
  ...
# Subtest: confirmed today with two keeps: check glyph, faint dots
ok 1305 - confirmed today with two keeps: check glyph, faint dots
  ---
  duration_ms: 0.360167
  type: 'test'
  ...
# Subtest: due below threshold: orange capsule keeps its glyph, adds dots
ok 1306 - due below threshold: orange capsule keeps its glyph, adds dots
  ---
  duration_ms: 0.36117
  type: 'test'
  ...
# Subtest: resting marks show historical dots quietly and never decide
ok 1307 - resting marks show historical dots quietly and never decide
  ---
  duration_ms: 0.538639
  type: 'test'
  ...
# Subtest: active decision due: data stays truthful, leaf stays gated
ok 1308 - active decision due: data stays truthful, leaf stays gated
  ---
  duration_ms: 0.390135
  type: 'test'
  ...
# Subtest: dot caps follow the threshold with +N overflow
ok 1309 - dot caps follow the threshold with +N overflow
  ---
  duration_ms: 1.044275
  type: 'test'
  ...
# Subtest: keeps tooltip wording: singulars, zero threshold, off state
ok 1310 - keeps tooltip wording: singulars, zero threshold, off state
  ---
  duration_ms: 0.194321
  type: 'test'
  ...
# Subtest: noncanonical keeps never fold but keep their repair pill
ok 1311 - noncanonical keeps never fold but keep their repair pill
  ---
  duration_ms: 0.611779
  type: 'test'
  ...
# Subtest: quoted lines fold; rendered fragments fold without task checks
ok 1312 - quoted lines fold; rendered fragments fold without task checks
  ---
  duration_ms: 0.399122
  type: 'test'
  ...
# Subtest: unresolved marks show the line's own pips quietly and never decide
ok 1313 - unresolved marks show the line's own pips quietly and never decide
  ---
  duration_ms: 0.281818
  type: 'test'
  ...
# Subtest: consensus sees count and decision eligibility: ambiguity stays neutral
ok 1314 - consensus sees count and decision eligibility: ambiguity stays neutral
  ---
  duration_ms: 0.792003
  type: 'test'
  ...
# Subtest: pips render as one aria-hidden span with the count in the label
ok 1315 - pips render as one aria-hidden span with the count in the label
  ---
  duration_ms: 1.633209
  type: 'test'
  ...
# Subtest: Live Preview decorates the folded range including space and refresh
ok 1316 - Live Preview decorates the folded range including space and refresh
  ---
  duration_ms: 8.604012
  type: 'test'
  ...
# Subtest: Live Preview reveals the raw field when the cursor overlaps either edge
ok 1317 - Live Preview reveals the raw field when the cursor overlaps either edge
  ---
  duration_ms: 2.843101
  type: 'test'
  ...
# Subtest: Live Preview skips codeblock and inline code spans
ok 1318 - Live Preview skips codeblock and inline code spans
  ---
  duration_ms: 1.420453
  type: 'test'
  ...
# Subtest: source mode and marks-off yield no decorations
ok 1319 - source mode and marks-off yield no decorations
  ---
  duration_ms: 0.273692
  type: 'test'
  ...
# Subtest: update rebuilds on the refresh effect and widget eq is stable
ok 1320 - update rebuilds on the refresh effect and widget eq is stable
  ---
  duration_ms: 1.553538
  type: 'test'
  ...
# Subtest: widget click reveals the field at the folded offset
ok 1321 - widget click reveals the field at the folded offset
  ---
  duration_ms: 1.293751
  type: 'test'
  ...
# Subtest: line resolver prefers exact, then consensus, then unresolved
ok 1322 - line resolver prefers exact, then consensus, then unresolved
  ---
  duration_ms: 1.919166
  type: 'test'
  ...
# Subtest: decoration builds reuse the snapshot without touching the loader
ok 1323 - decoration builds reuse the snapshot without touching the loader
  ---
  duration_ms: 0.647747
  type: 'test'
  ...
# Subtest: rendered views split text nodes and skip excluded ancestors
ok 1324 - rendered views split text nodes and skip excluded ancestors
  ---
  duration_ms: 4.171618
  type: 'test'
  ...
# Subtest: rendered views stay idempotent
ok 1325 - rendered views stay idempotent
  ---
  duration_ms: 2.269013
  type: 'test'
  ...
# Subtest: text resolver reaches consensus and degrades to neutral
ok 1326 - text resolver reaches consensus and degrades to neutral
  ---
  duration_ms: 8.824455
  type: 'test'
  ...
# Subtest: session toggle flips the body class and notifies
ok 1327 - session toggle flips the body class and notifies
  ---
  duration_ms: 2.045206
  type: 'test'
  ...
# Subtest: Live Preview reads only the child block and never calls doc.toString
ok 1328 - Live Preview reads only the child block and never calls doc.toString
  ---
  duration_ms: 14.341218
  type: 'test'
  ...
# Subtest: Live Preview stops at the first nonblank line at or above the task
ok 1329 - Live Preview stops at the first nonblank line at or above the task
  ---
  duration_ms: 0.742509
  type: 'test'
  ...
# Subtest: Live Preview performance stays bounded on a large child block
ok 1330 - Live Preview performance stays bounded on a large child block
  ---
  duration_ms: 2819.4386
  type: 'test'
  ...
# Subtest: reading view shows the rotten line and excludes Tasks and Dataview rows
ok 1331 - reading view shows the rotten line and excludes Tasks and Dataview rows
  ---
  duration_ms: 1.45007
  type: 'test'
  ...
# Subtest: reading-view DOM history counts a Next lane entry
ok 1332 - reading-view DOM history counts a Next lane entry
  ---
  duration_ms: 2.247012
  type: 'test'
  ...
# Subtest: query-row consensus stays byte-identical with and without a Rotten Log
ok 1333 - query-row consensus stays byte-identical with and without a Rotten Log
  ---
  duration_ms: 0.60192
  type: 'test'
  ...
# Subtest: onload registers the toggle, extension, and post-processor
ok 1334 - onload registers the toggle, extension, and post-processor
  ---
  duration_ms: 28.825593
  type: 'test'
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 1335 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 0.718462
  type: 'test'
  ...
# Subtest: shared grammar fixture round-trips parse vectors and tallies
ok 1336 - shared grammar fixture round-trips parse vectors and tallies
  ---
  duration_ms: 4.187257
  type: 'test'
  ...
# Subtest: M1 today: check glyph, today label, full ring
ok 1337 - M1 today: check glyph, today label, full ring
  ---
  duration_ms: 4.174473
  type: 'test'
  ...
# Subtest: M2 aging: ring glyph, 3d label, draining lease
ok 1338 - M2 aging: ring glyph, 3d label, draining lease
  ---
  duration_ms: 0.651744
  type: 'test'
  ...
# Subtest: M3 boundary: ROTTEN due capsule with Alt+F hint
ok 1339 - M3 boundary: ROTTEN due capsule with Alt+F hint
  ---
  duration_ms: 0.488974
  type: 'test'
  ...
# Subtest: checklist marks replace stamp hints with their completion tier
ok 1340 - checklist marks replace stamp hints with their completion tier
  ---
  duration_ms: 1.08855
  type: 'test'
  ...
# Subtest: M4 yesterday uses the yesterday relative
ok 1341 - M4 yesterday uses the yesterday relative
  ---
  duration_ms: 0.353525
  type: 'test'
  ...
# Subtest: M5 folded refresh shows the /14d suffix
ok 1342 - M5 folded refresh shows the /14d suffix
  ---
  duration_ms: 1.595367
  type: 'test'
  ...
# Subtest: M6 refresh today: today tone hides the interval suffix
ok 1343 - M6 refresh today: today tone hides the interval suffix
  ---
  duration_ms: 0.389213
  type: 'test'
  ...
# Subtest: M7 note interval stays tooltip-only
ok 1344 - M7 note interval stays tooltip-only
  ---
  duration_ms: 1.00537
  type: 'test'
  ...
# Subtest: M8 resurfaced: due tone on the scheduled return
ok 1345 - M8 resurfaced: due tone on the scheduled return
  ---
  duration_ms: 0.808514
  type: 'test'
  ...
# Subtest: M9 due NEXT lane with keep/release/today keys
ok 1346 - M9 due NEXT lane with keep/release/today keys
  ---
  duration_ms: 0.488573
  type: 'test'
  ...
# Subtest: M10 NEXT lane stamped today
ok 1347 - M10 NEXT lane stamped today
  ---
  duration_ms: 0.300975
  type: 'test'
  ...
# Subtest: M19 disabled Next lane rests
ok 1348 - M19 disabled Next lane rests
  ---
  duration_ms: 0.408912
  type: 'test'
  ...
# Subtest: M20 PENDING lane folds refresh without the suffix
ok 1349 - M20 PENDING lane folds refresh without the suffix
  ---
  duration_ms: 0.364606
  type: 'test'
  ...
# Subtest: M11 closed: resting beats age 0
ok 1350 - M11 closed: resting beats age 0
  ---
  duration_ms: 0.2776
  type: 'test'
  ...
# Subtest: M12 unresolved running and M13 unresolved lease over
ok 1351 - M12 unresolved running and M13 unresolved lease over
  ---
  duration_ms: 0.273783
  type: 'test'
  ...
# Subtest: M14 linked today rests with its reason
ok 1352 - M14 linked today rests with its reason
  ---
  duration_ms: 0.345319
  type: 'test'
  ...
# Subtest: M15 other year shows the year and the 282d age
ok 1353 - M15 other year shows the year and the 282d age
  ---
  duration_ms: 0.184853
  type: 'test'
  ...
# Subtest: M16 quoted line keeps foldSpace
ok 1354 - M16 quoted line keeps foldSpace
  ---
  duration_ms: 0.196195
  type: 'test'
  ...
# Subtest: M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
ok 1355 - M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
  ---
  duration_ms: 0.446092
  type: 'test'
  ...
# Subtest: N1-N6 non-canonical lines get no mark
ok 1356 - N1-N6 non-canonical lines get no mark
  ---
  duration_ms: 0.197848
  type: 'test'
  ...
# Subtest: C1-C3 consensus is exact or unresolved
ok 1357 - C1-C3 consensus is exact or unresolved
  ---
  duration_ms: 0.719615
  type: 'test'
  ...
# Subtest: freshnessMarkResolution treats evaluator new as unresolved
ok 1358 - freshnessMarkResolution treats evaluator new as unresolved
  ---
  duration_ms: 0.149796
  type: 'test'
  ...
# Subtest: freshnessMarkSourceInText covers rendered fragments
ok 1359 - freshnessMarkSourceInText covers rendered fragments
  ---
  duration_ms: 0.288812
  type: 'test'
  ...
# Subtest: tone order: closed, then due, then age 0, then out of scope
ok 1360 - tone order: closed, then due, then age 0, then out of scope
  ---
  duration_ms: 0.603323
  type: 'test'
  ...
# Subtest: no tooltip ever contains a double colon
ok 1361 - no tooltip ever contains a double colon
  ---
  duration_ms: 0.971416
  type: 'test'
  ...
# Subtest: freshnessShortDate pins English names and the year rule
ok 1362 - freshnessShortDate pins English names and the year rule
  ---
  duration_ms: 0.178752
  type: 'test'
  ...
# Subtest: DOM builder structure, attributes, and ring geometry
ok 1363 - DOM builder structure, attributes, and ring geometry
  ---
  duration_ms: 1.795239
  type: 'test'
  ...
# Subtest: every mark helper is synchronous and never throws on bad input
ok 1364 - every mark helper is synchronous and never throws on bad input
  ---
  duration_ms: 0.194912
  type: 'test'
  ...
# Subtest: rotten line wording covers 0, 1, and many entries
ok 1365 - rotten line wording covers 0, 1, and many entries
  ---
  duration_ms: 0.566012
  type: 'test'
  ...
# Subtest: rotten line date format includes the year only when it differs
ok 1366 - rotten line date format includes the year only when it differs
  ---
  duration_ms: 0.208528
  type: 'test'
  ...
# Subtest: rotten line truncates the reason to 48 code points without splitting emoji
ok 1367 - rotten line truncates the reason to 48 code points without splitting emoji
  ---
  duration_ms: 0.247964
  type: 'test'
  ...
# Subtest: rotten history rejects ambiguous, invalid, and nested entries
ok 1368 - rotten history rejects ambiguous, invalid, and nested entries
  ---
  duration_ms: 1.07336
  type: 'test'
  ...
# Subtest: rotten marker vectors reject mismatched emoji and missing spaces
ok 1369 - rotten marker vectors reject mismatched emoji and missing spaces
  ---
  duration_ms: 1.628811
  type: 'test'
  ...
# Subtest: rotten line splices before the action line and reaches aria-label
ok 1370 - rotten line splices before the action line and reaches aria-label
  ---
  duration_ms: 0.894769
  type: 'test'
  ...
# Subtest: freshness namespace v14 exposes checklist stages with per-rung decay and unblock TICKLER writers
ok 1371 - freshness namespace v14 exposes checklist stages with per-rung decay and unblock TICKLER writers
  ---
  duration_ms: 94.598604
  type: 'test'
  ...
# Subtest: freshness state and count API expose an unblock return source
ok 1372 - freshness state and count API expose an unblock return source
  ---
  duration_ms: 19.613983
  type: 'test'
  ...
# Subtest: checklist rows report tier and rank while keeping the READY bucket null
ok 1373 - checklist rows report tier and rank while keeping the READY bucket null
  ---
  duration_ms: 8.934996
  type: 'test'
  ...
# Subtest: tier, isDue, and rank cover lane rows
ok 1374 - tier, isDue, and rank cover lane rows
  ---
  duration_ms: 15.979668
  type: 'test'
  ...
# Subtest: memo invalidates on a new tasks array, rollover, and frontmatter
ok 1375 - memo invalidates on a new tasks array, rollover, and frontmatter
  ---
  duration_ms: 26.864492
  type: 'test'
  ...
# Subtest: the reload event fires only when the due key set changes
ok 1376 - the reload event fires only when the due key set changes
  ---
  duration_ms: 34.36827
  type: 'test'
  ...
# Subtest: status bar text covers every state, and a missing host stays quiet
ok 1377 - status bar text covers every state, and a missing host stays quiet
  ---
  duration_ms: 19.293988
  type: 'test'
  ...
# Subtest: status bar clicks through, falling back to rotten
ok 1378 - status bar clicks through, falling back to rotten
  ---
  duration_ms: 68.471397
  type: 'test'
  ...
# Subtest: every freshness api member is synchronous and never throws
ok 1379 - every freshness api member is synchronous and never throws
  ---
  duration_ms: 16.981141
  type: 'test'
  ...
# Subtest: placement vectors P1-P11, P14-P16, P18 stamp canonically
ok 1380 - placement vectors P1-P11, P14-P16, P18 stamp canonically
  ---
  duration_ms: 5.119047
  type: 'test'
  ...
# Subtest: P12 set and clear refresh stamps alongside
ok 1381 - P12 set and clear refresh stamps alongside
  ---
  duration_ms: 0.437025
  type: 'test'
  ...
# Subtest: P13 recurring and P17 done tasks are refused unchanged
ok 1382 - P13 recurring and P17 done tasks are refused unchanged
  ---
  duration_ms: 0.254666
  type: 'test'
  ...
# Subtest: Pomodoro ledger rows are refused byte-for-byte by every fresh writer
ok 1383 - Pomodoro ledger rows are refused byte-for-byte by every fresh writer
  ---
  duration_ms: 0.74358
  type: 'test'
  ...
# Subtest: a time range later in task prose remains eligible for freshness
ok 1384 - a time range later in task prose remains eligible for freshness
  ---
  duration_ms: 0.213598
  type: 'test'
  ...
# Subtest: U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
ok 1385 - U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
  ---
  duration_ms: 0.925377
  type: 'test'
  ...
# Subtest: reader reports misplaced and duplicate fields
ok 1386 - reader reports misplaced and duplicate fields
  ---
  duration_ms: 0.550992
  type: 'test'
  ...
# Subtest: Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
ok 1387 - Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
  ---
  duration_ms: 6.548867
  type: 'test'
  ...
# Subtest: Q2 tier order beats path order
ok 1388 - Q2 tier order beats path order
  ---
  duration_ms: 1.775672
  type: 'test'
  ...
# Subtest: L1 lane due and stamped today
ok 1389 - L1 lane due and stamped today
  ---
  duration_ms: 0.635924
  type: 'test'
  ...
# Subtest: L2 lane overrides refresh
ok 1390 - L2 lane overrides refresh
  ---
  duration_ms: 0.411756
  type: 'test'
  ...
# Subtest: L3 lane exclusions have no tier
ok 1391 - L3 lane exclusions have no tier
  ---
  duration_ms: 0.5131
  type: 'test'
  ...
# Subtest: L4 lane off switch and null default
ok 1392 - L4 lane off switch and null default
  ---
  duration_ms: 0.246721
  type: 'test'
  ...
# Subtest: L5 lane order never stamped first
ok 1393 - L5 lane order never stamped first
  ---
  duration_ms: 0.65424
  type: 'test'
  ...
# Subtest: R1 TICKLER beats older ROTTEN
ok 1394 - R1 TICKLER beats older ROTTEN
  ---
  duration_ms: 0.478614
  type: 'test'
  ...
# Subtest: R2 tickler orders by due date then path and line
ok 1395 - R2 tickler orders by due date then path and line
  ---
  duration_ms: 0.762226
  type: 'test'
  ...
# Subtest: missing created sorts after dated peers
ok 1396 - missing created sorts after dated peers
  ---
  duration_ms: 1.666142
  type: 'test'
  ...
# Subtest: B1 upkeep counts outside the lanes
ok 1397 - B1 upkeep counts outside the lanes
  ---
  duration_ms: 3.365538
  type: 'test'
  ...
# Subtest: review model meter uses upkeep and exposes refreshed
ok 1398 - review model meter uses upkeep and exposes refreshed
  ---
  duration_ms: 0.542546
  type: 'test'
  ...
# Subtest: RC1 arrived: past scheduled walks RECURRING with lane and null state
ok 1399 - RC1 arrived: past scheduled walks RECURRING with lane and null state
  ---
  duration_ms: 4.474987
  type: 'test'
  ...
# Subtest: RC2 arrives today: due today with zero days overdue
ok 1400 - RC2 arrives today: due today with zero days overdue
  ---
  duration_ms: 0.433238
  type: 'test'
  ...
# Subtest: RC3 not yet: future scheduled walks nowhere
ok 1401 - RC3 not yet: future scheduled walks nowhere
  ---
  duration_ms: 0.264796
  type: 'test'
  ...
# Subtest: RC4 due only, past: the due date is the occurrence
ok 1402 - RC4 due only, past: the due date is the occurrence
  ---
  duration_ms: 0.342775
  type: 'test'
  ...
# Subtest: RC5 due only, future: walks nowhere
ok 1403 - RC5 due only, future: walks nowhere
  ---
  duration_ms: 2.855604
  type: 'test'
  ...
# Subtest: RC6 earliest date wins across start and due
ok 1404 - RC6 earliest date wins across start and due
  ---
  duration_ms: 0.58107
  type: 'test'
  ...
# Subtest: RC7 undated: no occurrence, no tier
ok 1405 - RC7 undated: no occurrence, no tier
  ---
  duration_ms: 0.472252
  type: 'test'
  ...
# Subtest: RC8 lanes: recurring lane rows keep their lane with null state
ok 1406 - RC8 lanes: recurring lane rows keep their lane with null state
  ---
  duration_ms: 0.747708
  type: 'test'
  ...
# Subtest: RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
ok 1407 - RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
  ---
  duration_ms: 2.540131
  type: 'test'
  ...
# Subtest: RC10 checklist wins: a recurring chore stays in its checklist tier
ok 1408 - RC10 checklist wins: a recurring chore stays in its checklist tier
  ---
  duration_ms: 8.853778
  type: 'test'
  ...
# Subtest: RC11 a stray stamp is ignored: recurring with null state
ok 1409 - RC11 a stray stamp is ignored: recurring with null state
  ---
  duration_ms: 0.731828
  type: 'test'
  ...
# Subtest: RC12 order and counts: due_on, then path, then line; recurring adds no due
ok 1410 - RC12 order and counts: due_on, then path, then line; recurring adds no due
  ---
  duration_ms: 1.70155
  type: 'test'
  ...
# Subtest: recurring rows adapt due and start from Tasks fields and inline fallbacks
ok 1411 - recurring rows adapt due and start from Tasks fields and inline fallbacks
  ---
  duration_ms: 6.115431
  type: 'test'
  ...
# Subtest: status view counts RECURRING as a due commitment tier
ok 1412 - status view counts RECURRING as a due commitment tier
  ---
  duration_ms: 0.554779
  type: 'test'
  ...
# Subtest: footer groups, entry view, and legend cover RECURRING
ok 1413 - footer groups, entry view, and legend cover RECURRING
  ---
  duration_ms: 1.41863
  type: 'test'
  ...
# Subtest: a stale-stamped recurring row marks due with the resolve hint
ok 1414 - a stale-stamped recurring row marks due with the resolve hint
  ---
  duration_ms: 5.844413
  type: 'test'
  ...
# Subtest: freshness namespace v14 keeps recurring and removes reference capabilities
ok 1415 - freshness namespace v14 keeps recurring and removes reference capabilities
  ---
  duration_ms: 57.922919
  type: 'test'
  ...
# Subtest: hidden recurring ^ref keeps ordinary visibility (Rust parity)
ok 1416 - hidden recurring ^ref keeps ordinary visibility (Rust parity)
  ---
  duration_ms: 1.513941
  type: 'test'
  ...
# Subtest: bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
ok 1417 - bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
  ---
  duration_ms: 14.323084
  type: 'test'
  ...
# Subtest: day numbers stay calendar-local across a DST boundary
ok 1418 - day numbers stay calendar-local across a DST boundary
  ---
  duration_ms: 0.860223
  type: 'test'
  ...
# Subtest: reviewModel shares counts, meter, tooltip, and severity
ok 1419 - reviewModel shares counts, meter, tooltip, and severity
  ---
  duration_ms: 0.80121
  type: 'test'
  ...
# Subtest: memo serves warm map hits and misses use the per-row evaluator
ok 1420 - memo serves warm map hits and misses use the per-row evaluator
  ---
  duration_ms: 58.368501
  type: 'test'
  ...
# Subtest: config snapshot caches the parse and invalidates explicitly
ok 1421 - config snapshot caches the parse and invalidates explicitly
  ---
  duration_ms: 14.983064
  type: 'test'
  ...
# Subtest: review chips share the model with severity classes
ok 1422 - review chips share the model with severity classes
  ---
  duration_ms: 1.950546
  type: 'test'
  ...
# Subtest: warm lookups reuse one snapshot without re-reading config
ok 1423 - warm lookups reuse one snapshot without re-reading config
  ---
  duration_ms: 9.673887
  type: 'test'
  ...
# Subtest: same-array cache updates and Today changes rebuild the memo
ok 1424 - same-array cache updates and Today changes rebuild the memo
  ---
  duration_ms: 40.490153
  type: 'test'
  ...
# Subtest: duplicate block IDs keep each row's own classification
ok 1425 - duplicate block IDs keep each row's own classification
  ---
  duration_ms: 42.613178
  type: 'test'
  ...
# Subtest: line identity separates same-path rows without block IDs
ok 1426 - line identity separates same-path rows without block IDs
  ---
  duration_ms: 43.75022
  type: 'test'
  ...
# Subtest: interval lookup serves the cached interval with one memo acquisition
ok 1427 - interval lookup serves the cached interval with one memo acquisition
  ---
  duration_ms: 24.186073
  type: 'test'
  ...
# Subtest: SC stage config vectors normalize valid lists and isolate rejected lists
ok 1428 - SC stage config vectors normalize valid lists and isolate rejected lists
  ---
  duration_ms: 8.923051
  type: 'test'
  ...
# Subtest: CS stage queue vectors resolve tags and sort staged checklist rows
ok 1429 - CS stage queue vectors resolve tags and sort staged checklist rows
  ---
  duration_ms: 17.889429
  type: 'test'
  ...
# Subtest: stage names are rendered in footer details and counts compact before labels
ok 1430 - stage names are rendered in footer details and counts compact before labels
  ---
  duration_ms: 0.91628
  type: 'test'
  ...
# Subtest: FT1-FT6 footer details preserve tier semantics, stage color, and compact counts
ok 1431 - FT1-FT6 footer details preserve tier semantics, stage color, and compact counts
  ---
  duration_ms: 3.195243
  type: 'test'
  ...
# Subtest: invalid stage lists emit one config lint without invalidating freshness
ok 1432 - invalid stage lists emit one config lint without invalidating freshness
  ---
  duration_ms: 27.269321
  type: 'test'
  ...
# Subtest: namespace v14 exposes normalized stage config and queue fields from Tasks rows
ok 1433 - namespace v14 exposes normalized stage config and queue fields from Tasks rows
  ---
  duration_ms: 20.922802
  type: 'test'
  ...
# Subtest: S1 new through S4 overdue
ok 1434 - S1 new through S4 overdue
  ---
  duration_ms: 4.736197
  type: 'test'
  ...
# Subtest: S5 task beats note, S6 note beats config, S7 config
ok 1435 - S5 task beats note, S6 note beats config, S7 config
  ---
  duration_ms: 1.074302
  type: 'test'
  ...
# Subtest: S8 invalid overrides fall through with lints
ok 1436 - S8 invalid overrides fall through with lints
  ---
  duration_ms: 0.569928
  type: 'test'
  ...
# Subtest: S9 malformed and S10 future stamps read as new
ok 1437 - S9 malformed and S10 future stamps read as new
  ---
  duration_ms: 0.325271
  type: 'test'
  ...
# Subtest: S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
ok 1438 - S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
  ---
  duration_ms: 0.52349
  type: 'test'
  ...
# Subtest: S13 out-of-scope rows read null
ok 1439 - S13 out-of-scope rows read null
  ---
  duration_ms: 0.590358
  type: 'test'
  ...
# Subtest: S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
ok 1440 - S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
  ---
  duration_ms: 2.056328
  type: 'test'
  ...
# Subtest: S15 counts (updated): upkeep outside the lanes drives the budget
ok 1441 - S15 counts (updated): upkeep outside the lanes drives the budget
  ---
  duration_ms: 1.61783
  type: 'test'
  ...
# Subtest: config coercion keeps defaults, flags invalid, ignores unknown keys
ok 1442 - config coercion keeps defaults, flags invalid, ignores unknown keys
  ---
  duration_ms: 2.845325
  type: 'test'
  ...
# Subtest: loadFreshnessConfig reads the block with plan-style injectables
ok 1443 - loadFreshnessConfig reads the block with plan-style injectables
  ---
  duration_ms: 1.436975
  type: 'test'
  ...
# Subtest: interval precedence is task, note, config, default
ok 1444 - interval precedence is task, note, config, default
  ---
  duration_ms: 0.348827
  type: 'test'
  ...
# Subtest: intervalForLine covers every source with its Ready fallback
ok 1445 - intervalForLine covers every source with its Ready fallback
  ---
  duration_ms: 1.329028
  type: 'test'
  ...
# Subtest: project tracking stays special while reference tasks use ordinary Ready freshness
ok 1446 - project tracking stays special while reference tasks use ordinary Ready freshness
  ---
  duration_ms: 5.548928
  type: 'test'
  ...
# Subtest: reference tasks match ordinary interval precedence and lane behavior
ok 1447 - reference tasks match ordinary interval precedence and lane behavior
  ---
  duration_ms: 3.41872
  type: 'test'
  ...
# Subtest: obsolete reference interval keys are ignored and project config still validates
ok 1448 - obsolete reference interval keys are ignored and project config still validates
  ---
  duration_ms: 1.090713
  type: 'test'
  ...
# Subtest: references use ordinary keep decisions and the nine-tier queue shape
ok 1449 - references use ordinary keep decisions and the nine-tier queue shape
  ---
  duration_ms: 1.230721
  type: 'test'
  ...
# Subtest: CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
ok 1450 - CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
  ---
  duration_ms: 6.232484
  type: 'test'
  ...
# Subtest: CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
ok 1451 - CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
  ---
  duration_ms: 2.915479
  type: 'test'
  ...
# Subtest: freshness namespace v14 retains the tracker capability contract
ok 1452 - freshness namespace v14 retains the tracker capability contract
  ---
  duration_ms: 25.79776
  type: 'test'
  ...
# Subtest: UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
ok 1453 - UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
  ---
  duration_ms: 4.425573
  type: 'test'
  ...
# Subtest: UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
ok 1454 - UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
  ---
  duration_ms: 0.725235
  type: 'test'
  ...
# Subtest: UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
ok 1455 - UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
  ---
  duration_ms: 0.436554
  type: 'test'
  ...
# Subtest: UB11 scheduled wins a tie with the unblock date
ok 1456 - UB11 scheduled wins a tie with the unblock date
  ---
  duration_ms: 1.212656
  type: 'test'
  ...
# Subtest: unblocked reader takes the latest valid duplicate and reports malformed values
ok 1457 - unblocked reader takes the latest valid duplicate and reports malformed values
  ---
  duration_ms: 0.386709
  type: 'test'
  ...
# Subtest: UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
ok 1458 - UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
  ---
  duration_ms: 0.624603
  type: 'test'
  ...
# Subtest: UB14 TICKLERs with the same due date sort only by path and line
ok 1459 - UB14 TICKLERs with the same due date sort only by path and line
  ---
  duration_ms: 5.234939
  type: 'test'
  ...
# Subtest: UB15 a scheduled ^prj resurfaces in PROJECTS
ok 1460 - UB15 a scheduled ^prj resurfaces in PROJECTS
  ---
  duration_ms: 0.369175
  type: 'test'
  ...
# Subtest: calendar scan stays within an unfenced Events section
ok 1461 - calendar scan stays within an unfenced Events section
  ---
  duration_ms: 10.03661
  type: 'test'
  ...
# Subtest: calendar scan finds same-day and dated Events stamps and ignores lookalikes
ok 1462 - calendar scan finds same-day and dated Events stamps and ignores lookalikes
  ---
  duration_ms: 1.761304
  type: 'test'
  ...
# Subtest: stamp state stays fresh on change, including old, future, and dated stamps
ok 1463 - stamp state stays fresh on change, including old, future, and dated stamps
  ---
  duration_ms: 0.485397
  type: 'test'
  ...
# Subtest: event clock state distinguishes future, running, and past
ok 1464 - event clock state distinguishes future, running, and past
  ---
  duration_ms: 0.230299
  type: 'test'
  ...
# Subtest: afternoon and evening spans stay future until they start (ES1-ES10)
ok 1465 - afternoon and evening spans stay future until they start (ES1-ES10)
  ---
  duration_ms: 0.398401
  type: 'test'
  ...
# Subtest: a buffer delays past fade and lights lead-in / lead-out wings
ok 1466 - a buffer delays past fade and lights lead-in / lead-out wings
  ---
  duration_ms: 0.212236
  type: 'test'
  ...
# Subtest: calendar scan reads [buffer::] and exposes wing data
ok 1467 - calendar scan reads [buffer::] and exposes wing data
  ---
  duration_ms: 6.413447
  type: 'test'
  ...
# Subtest: Reading view inserts hatched buffer wings beside the time pill
ok 1468 - Reading view inserts hatched buffer wings beside the time pill
  ---
  duration_ms: 0.770751
  type: 'test'
  ...
# Subtest: sync-on-create gate only accepts today's canonical daily note
ok 1469 - sync-on-create gate only accepts today's canonical daily note
  ---
  duration_ms: 5.304281
  type: 'test'
  ...
# Subtest: create listener runs once for today's note after layout readiness
ok 1470 - create listener runs once for today's note after layout readiness
  ---
  duration_ms: 1.333717
  type: 'test'
  ...
# Subtest: sync-on-create waits for Templater's Pomodoros section, then stops at its deadline
ok 1471 - sync-on-create waits for Templater's Pomodoros section, then stops at its deadline
  ---
  duration_ms: 1.017753
  type: 'test'
  ...
# Subtest: pending Templater tags are found everywhere except fenced and inline code
ok 1472 - pending Templater tags are found everywhere except fenced and inline code
  ---
  duration_ms: 0.410805
  type: 'test'
  ...
# Subtest: a raw template is not ready; a rendered note is
ok 1473 - a raw template is not ready; a rendered note is
  ---
  duration_ms: 0.196716
  type: 'test'
  ...
# Subtest: the waiter settles on two identical ready reads
ok 1474 - the waiter settles on two identical ready reads
  ---
  duration_ms: 6.435692
  type: 'test'
  ...
# Subtest: the waiter restarts settle when the note changes
ok 1475 - the waiter restarts settle when the note changes
  ---
  duration_ms: 0.575459
  type: 'test'
  ...
# Subtest: gcal sync spawns with --format json
ok 1476 - gcal sync spawns with --format json
  ---
  duration_ms: 0.168431
  type: 'test'
  ...
# bob gcal sync wait timed out: today's note never settled into a rendered note with \#\# Pomodoros; spawning sync anyway
# Subtest: gcalEventsDecodeSync accepts held and ignores unknown future fields
ok 1477 - gcalEventsDecodeSync accepts held and ignores unknown future fields
  ---
  duration_ms: 0.40304
  type: 'test'
  ...
# Subtest: waiting and held notices fire once per day
ok 1478 - waiting and held notices fire once per day
  ---
  duration_ms: 4.669138
  type: 'test'
  ...
# Subtest: calendar hook spawns sync after the wait times out and notices waiting
ok 1479 - calendar hook spawns sync after the wait times out and notices waiting
  ---
  duration_ms: 204.694512
  type: 'test'
  ...
# Subtest: calendar hook notices a held sync once per day
ok 1480 - calendar hook notices a held sync once per day
  ---
  duration_ms: 103.18804
  type: 'test'
  ...
# Subtest: calendar paint teardown clears the clock refresh interval
ok 1481 - calendar paint teardown clears the clock refresh interval
  ---
  duration_ms: 0.787775
  type: 'test'
  ...
# Subtest: off-clock Live Preview paints one chip widget and no split marks
ok 1482 - off-clock Live Preview paints one chip widget and no split marks
  ---
  duration_ms: 7.367352
  type: 'test'
  ...
# Subtest: off-clock chip preserves alias spelling and case
ok 1483 - off-clock chip preserves alias spelling and case
  ---
  duration_ms: 2.503853
  type: 'test'
  ...
# Subtest: off-clock chip reveals the raw tag while the cursor is on the line
ok 1484 - off-clock chip reveals the raw tag while the cursor is on the line
  ---
  duration_ms: 0.626707
  type: 'test'
  ...
# Subtest: buffer and off-clock decorations stay sorted and disjoint
ok 1485 - buffer and off-clock decorations stay sorted and disjoint
  ---
  duration_ms: 1.136792
  type: 'test'
  ...
# Subtest: a selection-only update reuses the cached scan
ok 1486 - a selection-only update reuses the cached scan
  ---
  duration_ms: 0.800089
  type: 'test'
  ...
# Subtest: the off-clock chip DOM carries the class, marker, and title
ok 1487 - the off-clock chip DOM carries the class, marker, and title
  ---
  duration_ms: 2.04691
  type: 'test'
  ...
# Subtest: scan treats \#on as on-clock even beside an off spelling
ok 1488 - scan treats \#on as on-clock even beside an off spelling
  ---
  duration_ms: 0.373173
  type: 'test'
  ...
# Subtest: inherited off-clock Event Tasks dash the pill with a from-note tooltip
ok 1489 - inherited off-clock Event Tasks dash the pill with a from-note tooltip
  ---
  duration_ms: 3.385336
  type: 'test'
  ...
# Subtest: Live Preview dashes inherited rows and keeps \#off chips
ok 1490 - Live Preview dashes inherited rows and keeps \#off chips
  ---
  duration_ms: 7.682393
  type: 'test'
  ...
# Subtest: Reading view dashes inherited pills and tooltips \#on overrides
ok 1491 - Reading view dashes inherited pills and tooltips \#on overrides
  ---
  duration_ms: 1.070584
  type: 'test'
  ...
# Subtest: gcalEventsDecodeSync treats missing deprecations as empty
ok 1492 - gcalEventsDecodeSync treats missing deprecations as empty
  ---
  duration_ms: 0.23557
  type: 'test'
  ...
# Subtest: gcalEventsDecodeSync keeps additive deprecations[]
ok 1493 - gcalEventsDecodeSync keeps additive deprecations[]
  ---
  duration_ms: 0.480357
  type: 'test'
  ...
# Subtest: deprecation Notice fires once per day from a successful auto-sync
ok 1494 - deprecation Notice fires once per day from a successful auto-sync
  ---
  duration_ms: 0.353835
  type: 'test'
  ...
# Subtest: gmail sync-on-create gate only accepts today's canonical daily note
ok 1495 - gmail sync-on-create gate only accepts today's canonical daily note
  ---
  duration_ms: 0.334479
  type: 'test'
  ...
# Subtest: gmailEventsDecodeSync accepts schema_version 1
ok 1496 - gmailEventsDecodeSync accepts schema_version 1
  ---
  duration_ms: 0.691791
  type: 'test'
  ...
# Subtest: gmailEventsFailureKind routes exit 1 to a Notice and exit 2 / unknown subcommand to info
ok 1497 - gmailEventsFailureKind routes exit 1 to a Notice and exit 2 / unknown subcommand to info
  ---
  duration_ms: 4.907602
  type: 'test'
  ...
# Subtest: shared create listener runs gmail after gcal, and gmail when gcal is off
ok 1498 - shared create listener runs gmail after gcal, and gmail when gcal is off
  ---
  duration_ms: 39.878075
  type: 'test'
  ...
# Subtest: gmailSyncCreatedDailyNote spawns bob gmail sync with a 120s timeout
ok 1499 - gmailSyncCreatedDailyNote spawns bob gmail sync with a 120s timeout
  ---
  duration_ms: 1005.440057
  type: 'test'
  ...
# Subtest: decode accepts schema 1 and marks the rest unsupported
ok 1500 - decode accepts schema 1 and marks the rest unsupported
  ---
  duration_ms: 2.121381
  type: 'test'
  ...
# Subtest: parity fixture counts 5 open top-level tasks
ok 1501 - parity fixture counts 5 open top-level tasks
  ---
  duration_ms: 0.73312
  type: 'test'
  ...
# Subtest: inbox tree membership walks area notes under inbox.md
ok 1502 - inbox tree membership walks area notes under inbox.md
  ---
  duration_ms: 2.230901
  type: 'test'
  ...
# Subtest: keepInboxTreeCounts skips nested done cancelled and non-members
ok 1503 - keepInboxTreeCounts skips nested done cancelled and non-members
  ---
  duration_ms: 1.578264
  type: 'test'
  ...
# Subtest: hidden before the first read and when unconfigured
ok 1504 - hidden before the first read and when unconfigured
  ---
  duration_ms: 0.422276
  type: 'test'
  ...
# Subtest: unverified hides Keep but keeps a live inbox
ok 1505 - unverified hides Keep but keeps a live inbox
  ---
  duration_ms: 0.547196
  type: 'test'
  ...
# Subtest: fresh, stale, and signin tones
ok 1506 - fresh, stale, and signin tones
  ---
  duration_ms: 1.061648
  type: 'test'
  ...
# Subtest: each segment hides at zero and the item hides when both are empty
ok 1507 - each segment hides at zero and the item hides when both are empty
  ---
  duration_ms: 0.501608
  type: 'test'
  ...
# Subtest: old verified ok counts hide Keep until checked again
ok 1508 - old verified ok counts hide Keep until checked again
  ---
  duration_ms: 0.580067
  type: 'test'
  ...
# Subtest: unsupported hides Keep and lives only with a positive inbox count
ok 1509 - unsupported hides Keep and lives only with a positive inbox count
  ---
  duration_ms: 0.726979
  type: 'test'
  ...
# Subtest: tasks-not-ready hides the inbox even when bob's inbox.open is positive
ok 1510 - tasks-not-ready hides the inbox even when bob's inbox.open is positive
  ---
  duration_ms: 0.449508
  type: 'test'
  ...
# Subtest: tooltip and aria copy with a fixed now
ok 1511 - tooltip and aria copy with a fixed now
  ---
  duration_ms: 0.285735
  type: 'test'
  ...
# Subtest: inbox tooltip lists the tree breakdown and names the click target
ok 1512 - inbox tooltip lists the tree breakdown and names the click target
  ---
  duration_ms: 0.561973
  type: 'test'
  ...
# Subtest: paint draws Lucide icons from the obsidian setIcon export
ok 1513 - paint draws Lucide icons from the obsidian setIcon export
  ---
  duration_ms: 1.543277
  type: 'test'
  ...
# Subtest: paint hides the item when both counts are zero and restores it
ok 1514 - paint hides the item when both counts are zero and restores it
  ---
  duration_ms: 0.452885
  type: 'test'
  ...
# Subtest: paint key is stable and paint skips unchanged frames
ok 1515 - paint key is stable and paint skips unchanged frames
  ---
  duration_ms: 0.306956
  type: 'test'
  ...
# Subtest: spawn wiring uses cache-only status with the Keep decoder
ok 1516 - spawn wiring uses cache-only status with the Keep decoder
  ---
  duration_ms: 6.095722
  type: 'test'
  ...
# Subtest: gkeep command-mode tag routes to the Keep inbox refresh
ok 1517 - gkeep command-mode tag routes to the Keep inbox refresh
  ---
  duration_ms: 0.547306
  type: 'test'
  ...
# Subtest: automatic checks require attention and a deferred timer fires on input
ok 1518 - automatic checks require attention and a deferred timer fires on input
  ---
  duration_ms: 11.844173
  type: 'test'
  ...
# Subtest: status timers clamp to one minute through two hours and null cancels
ok 1519 - status timers clamp to one minute through two hours and null cancels
  ---
  duration_ms: 0.295635
  type: 'test'
  ...
# Subtest: layout schedules its first automatic check after fifteen seconds
ok 1520 - layout schedules its first automatic check after fifteen seconds
  ---
  duration_ms: 1.511036
  type: 'test'
  ...
# Subtest: focus triggers coalesce to one refresh per fifteen seconds
ok 1521 - focus triggers coalesce to one refresh per fifteen seconds
  ---
  duration_ms: 14.039725
  type: 'test'
  ...
# Subtest: unattended focus reads cached status without refreshing Keep
ok 1522 - unattended focus reads cached status without refreshing Keep
  ---
  duration_ms: 1.591389
  type: 'test'
  ...
# Subtest: unconfigured focus cache reads are throttled for ten minutes
ok 1523 - unconfigured focus cache reads are throttled for ten minutes
  ---
  duration_ms: 6.76538
  type: 'test'
  ...
# Subtest: single flight queues one request and upgrades it from cache to forced
ok 1524 - single flight queues one request and upgrades it from cache to forced
  ---
  duration_ms: 6.945366
  type: 'test'
  ...
# Subtest: forced check feedback follows the bob refresh result
ok 1525 - forced check feedback follows the bob refresh result
  ---
  duration_ms: 26.920228
  type: 'test'
  ...
# Subtest: bulb clicks route by tone and missing Command Mode gives a preview hint
ok 1526 - bulb clicks route by tone and missing Command Mode gives a preview hint
  ---
  duration_ms: 0.91133
  type: 'test'
  ...
# Subtest: context menus omit Command Mode actions when its preview API is unavailable
ok 1527 - context menus omit Command Mode actions when its preview API is unavailable
  ---
  duration_ms: 0.507559
  type: 'test'
  ...
# Subtest: turning the indicator off prevents all new automatic and forced checks
ok 1528 - turning the indicator off prevents all new automatic and forced checks
  ---
  duration_ms: 0.273021
  type: 'test'
  ...
# Subtest: keepInboxRecountNow stores the inbox-tree total and notes
ok 1529 - keepInboxRecountNow stores the inbox-tree total and notes
  ---
  duration_ms: 0.784428
  type: 'test'
  ...
# Subtest: inbox click opens the note with the most open tasks
ok 1530 - inbox click opens the note with the most open tasks
  ---
  duration_ms: 1.302067
  type: 'test'
  ...
# Subtest: context menu Open gkeep_inbox.md still opens the Keep target
ok 1531 - context menu Open gkeep_inbox.md still opens the Keep target
  ---
  duration_ms: 0.593213
  type: 'test'
  ...
# Subtest: verified transition to auth shows one sign-in notice per session
ok 1532 - verified transition to auth shows one sign-in notice per session
  ---
  duration_ms: 0.251881
  type: 'test'
  ...
# Subtest: KP1/KB7: Live Preview widget sits at the link end with side 3 and the screenshot count
ok 1533 - KP1/KB7: Live Preview widget sits at the link end with side 3 and the screenshot count
  ---
  duration_ms: 9.896633
  type: 'test'
  ...
# Subtest: KB6: a standalone project under an area renders no mark
ok 1534 - KB6: a standalone project under an area renders no mark
  ---
  duration_ms: 1.32455
  type: 'test'
  ...
# Subtest: KB2/KB3: a sibling link suppresses the mark and striking it passes the baton with one tick
ok 1535 - KB2/KB3: a sibling link suppresses the mark and striking it passes the baton with one tick
  ---
  duration_ms: 4.751315
  type: 'test'
  ...
# Subtest: viewport-only rebuilds never tick and selection alone never rebuilds
ok 1536 - viewport-only rebuilds never tick and selection alone never rebuilds
  ---
  duration_ms: 2.155477
  type: 'test'
  ...
# Subtest: KP6/toggle: off hides every mark and on restores them without touching vault text
ok 1537 - KP6/toggle: off hides every mark and on restores them without touching vault text
  ---
  duration_ms: 3.585529
  type: 'test'
  ...
# Subtest: cold Tasks memo and missing project text render nothing; a fill schedules a refresh
ok 1538 - cold Tasks memo and missing project text render nothing; a fill schedules a refresh
  ---
  duration_ms: 2.239337
  type: 'test'
  ...
# Subtest: rollover: the same day stays quiet and a new day resets baton counts
ok 1539 - rollover: the same day stays quiet and a new day resets baton counts
  ---
  duration_ms: 1.468414
  type: 'test'
  ...
# Subtest: liveness: the daily note and cached project notes refresh; strangers do not
ok 1540 - liveness: the daily note and cached project notes refresh; strangers do not
  ---
  duration_ms: 0.321303
  type: 'test'
  ...
# Subtest: setup registers the default-on command, the Live Preview extension, and the Reading processor
ok 1541 - setup registers the default-on command, the Live Preview extension, and the Reading processor
  ---
  duration_ms: 1.440481
  type: 'test'
  ...
# Subtest: KP3/KP4: Reading inserts the host after 🔓/mail/🔑 and before the off chip
ok 1542 - KP3/KP4: Reading inserts the host after 🔓/mail/🔑 and before the off chip
  ---
  duration_ms: 4.454178
  type: 'test'
  ...
# Subtest: Reading removes stale hosts when the link loses eligibility
ok 1543 - Reading removes stale hosts when the link loses eligibility
  ---
  duration_ms: 2.58194
  type: 'test'
  ...
# Subtest: off-clock Reading insertion steps past the ⏭ host so the off chip stays last
ok 1544 - off-clock Reading insertion steps past the ⏭ host so the off chip stays last
  ---
  duration_ms: 2.16783
  type: 'test'
  ...
# Subtest: progress context and the off-clock chip recognize the ⏭ host as a ledger mark
ok 1545 - progress context and the off-clock chip recognize the ⏭ host as a ledger mark
  ---
  duration_ms: 0.668858
  type: 'test'
  ...
# Subtest: 200-link / 50-target Live Preview build memoizes targets and stays near the 25 ms budget
ok 1546 - 200-link / 50-target Live Preview build memoizes targets and stays near the 25 ms budget
  ---
  duration_ms: 198.228324
  type: 'test'
  ...
# Subtest: KB1/KB7/KB8: mixed lane order and exact count
ok 1547 - KB1/KB7/KB8: mixed lane order and exact count
  ---
  duration_ms: 8.917883
  type: 'test'
  ...
# Subtest: KB2–KB6/KB9/KB10: live-link, root, folds, and final-close gates
ok 1548 - KB2–KB6/KB9/KB10: live-link, root, folds, and final-close gates
  ---
  duration_ms: 5.364967
  type: 'test'
  ...
# Subtest: KB11–KB15/KB19/KB20/KB23: post-close blockers and uncertainty
ok 1549 - KB11–KB15/KB19/KB20/KB23: post-close blockers and uncertainty
  ---
  duration_ms: 5.291086
  type: 'test'
  ...
# Subtest: KB16–KB22: duplicate marks, reference rows, residency, and candidate gates
ok 1550 - KB16–KB22: duplicate marks, reference rows, residency, and candidate gates
  ---
  duration_ms: 6.411637
  type: 'test'
  ...
# Subtest: LP1–LP17: the root-parent rule matches the documented vectors
ok 1551 - LP1–LP17: the root-parent rule matches the documented vectors
  ---
  duration_ms: 16.110808
  type: 'test'
  ...
# Subtest: KT1–KT8: tooltip, accessible element, config cache, and bounded counting
ok 1552 - KT1–KT8: tooltip, accessible element, config cache, and bounded counting
  ---
  duration_ms: 198.247981
  type: 'test'
  ...
# Subtest: keep-moving widget positions the caret and opens its project from a modifier click
ok 1553 - keep-moving widget positions the caret and opens its project from a modifier click
  ---
  duration_ms: 2.574057
  type: 'test'
  ...
# Subtest: membership: pending/next/ready in, exclusions counted, today dropped
ok 1554 - membership: pending/next/ready in, exclusions counted, today dropped
  ---
  duration_ms: 15.68043
  type: 'test'
  ...
# Subtest: membership: review-bucket Ready tasks are excluded and counted as reviewReady
ok 1555 - membership: review-bucket Ready tasks are excluded and counted as reviewReady
  ---
  duration_ms: 0.679979
  type: 'test'
  ...
# Subtest: parity: pending/next match the dash section; ready matches readyCountFromTasks
ok 1556 - parity: pending/next match the dash section; ready matches readyCountFromTasks
  ---
  duration_ms: 2.84352
  type: 'test'
  ...
# Subtest: order: pending, then next, then ready, path then line inside each lane
ok 1557 - order: pending, then next, then ready, path then line inside each lane
  ---
  duration_ms: 0.543638
  type: 'test'
  ...
# Subtest: ranks: rank/total plus per-lane laneRank/laneTotal
ok 1558 - ranks: rank/total plus per-lane laneRank/laneTotal
  ---
  duration_ms: 0.57573
  type: 'test'
  ...
# Subtest: identity: keys match freshnessRowKey
ok 1559 - identity: keys match freshnessRowKey
  ---
  duration_ms: 2.336823
  type: 'test'
  ...
# Subtest: unavailable: throwing isToday propagates to the caller
ok 1560 - unavailable: throwing isToday propagates to the caller
  ---
  duration_ms: 1.685429
  type: 'test'
  ...
# Subtest: mixin: memo hits and invalidates; version 2; ready matches the chip
ok 1561 - mixin: memo hits and invalidates; version 2; ready matches the chip
  ---
  duration_ms: 8.589677
  type: 'test'
  ...
# Subtest: mixin: unavailable reasons for tasks, today, and error
ok 1562 - mixin: unavailable reasons for tasks, today, and error
  ---
  duration_ms: 0.707572
  type: 'test'
  ...
# Subtest: shape: the result and its entries are frozen
ok 1563 - shape: the result and its entries are frozen
  ---
  duration_ms: 0.767346
  type: 'test'
  ...
# Subtest: ML1–ML6, ML9: reply badge model vectors pass verbatim
ok 1564 - ML1–ML6, ML9: reply badge model vectors pass verbatim
  ---
  duration_ms: 4.107566
  type: 'test'
  ...
# Subtest: ML7 and ML10: no mail link and inline-code wikilinks produce no tokens
ok 1565 - ML7 and ML10: no mail link and inline-code wikilinks produce no tokens
  ---
  duration_ms: 1.43483
  type: 'test'
  ...
# Subtest: mailNoteFactsFromFrontmatter accepts type:[[mail]] or gmail_thread_id
ok 1566 - mailNoteFactsFromFrontmatter accepts type:[[mail]] or gmail_thread_id
  ---
  duration_ms: 0.437516
  type: 'test'
  ...
# Subtest: reply badge host is listener-free with no title
ok 1567 - reply badge host is listener-free with no title
  ---
  duration_ms: 0.325301
  type: 'test'
  ...
# Subtest: ML1 Live Preview widget sits after the closing ]]
ok 1568 - ML1 Live Preview widget sits after the closing ]]
  ---
  duration_ms: 2.974532
  type: 'test'
  ...
# Subtest: ML8: toggle off yields no decorations
ok 1569 - ML8: toggle off yields no decorations
  ---
  duration_ms: 0.189091
  type: 'test'
  ...
# Subtest: toggle-mail-link-marks flips the gate and Notice
ok 1570 - toggle-mail-link-marks flips the gate and Notice
  ---
  duration_ms: 0.365518
  type: 'test'
  ...
# Subtest: styles.css contract: muted badge, no pill, toggle hide
ok 1571 - styles.css contract: muted badge, no pill, toggle hide
  ---
  duration_ms: 5.787054
  type: 'test'
  ...
# Subtest: shared vector: back-to-back-worked-run
ok 1572 - shared vector: back-to-back-worked-run
  ---
  duration_ms: 8.991072
  type: 'test'
  ...
# Subtest: shared vector: off-clock-event-stamps-key
ok 1573 - shared vector: off-clock-event-stamps-key
  ---
  duration_ms: 1.120479
  type: 'test'
  ...
# Subtest: shared vector: off-clock-run-breaks-at-worked-event
ok 1574 - shared vector: off-clock-run-breaks-at-worked-event
  ---
  duration_ms: 0.567814
  type: 'test'
  ...
# Subtest: shared vector: worked-run-breaks-at-off-clock-event
ok 1575 - shared vector: worked-run-breaks-at-off-clock-event
  ---
  duration_ms: 0.55007
  type: 'test'
  ...
# Subtest: shared vector: overlapping-events-share-a-run
ok 1576 - shared vector: overlapping-events-share-a-run
  ---
  duration_ms: 0.58122
  type: 'test'
  ...
# Subtest: shared vector: late-join-clamps-to-closed-session
ok 1577 - shared vector: late-join-clamps-to-closed-session
  ---
  duration_ms: 0.513871
  type: 'test'
  ...
# Subtest: shared vector: running-event-starts-at-its-own-start
ok 1578 - shared vector: running-event-starts-at-its-own-start
  ---
  duration_ms: 0.416195
  type: 'test'
  ...
# Subtest: shared vector: early-start-writes-future-start
ok 1579 - shared vector: early-start-writes-future-start
  ---
  duration_ms: 0.500767
  type: 'test'
  ...
# Subtest: shared vector: far-run-warns-with-escape-hatch
ok 1580 - shared vector: far-run-warns-with-escape-hatch
  ---
  duration_ms: 0.846607
  type: 'test'
  ...
# Subtest: shared vector: ended-done-and-cancelled-events-are-skipped
ok 1581 - shared vector: ended-done-and-cancelled-events-are-skipped
  ---
  duration_ms: 0.920619
  type: 'test'
  ...
# Subtest: shared vector: no-lineup-events-keeps-the-default-pomodoro
ok 1582 - shared vector: no-lineup-events-keeps-the-default-pomodoro
  ---
  duration_ms: 1.044835
  type: 'test'
  ...
# Subtest: shared vector: counted-suffix-keeps-clock-classification
ok 1583 - shared vector: counted-suffix-keeps-clock-classification
  ---
  duration_ms: 0.322436
  type: 'test'
  ...
# Subtest: shared vector: restart-rederives-the-run
ok 1584 - shared vector: restart-rederives-the-run
  ---
  duration_ms: 0.269425
  type: 'test'
  ...
# Subtest: shared vector (capture-only): drop-removes-an-event-from-the-run
ok 1585 - shared vector (capture-only): drop-removes-an-event-from-the-run
  ---
  duration_ms: 0.123466
  type: 'test'
  ...
# Subtest: shared vector (capture-only): kept-swap-into-off-clock-meet-moves-key
ok 1586 - shared vector (capture-only): kept-swap-into-off-clock-meet-moves-key
  ---
  duration_ms: 0.084382
  type: 'test'
  ...
# Subtest: shared vector (capture-only): kept-swap-out-of-off-clock-meet-restores-worked-key
ok 1587 - shared vector (capture-only): kept-swap-out-of-off-clock-meet-restores-worked-key
  ---
  duration_ms: 0.067078
  type: 'test'
  ...
# Subtest: shared vector: named-meet-start-uses-the-run
ok 1588 - shared vector: named-meet-start-uses-the-run
  ---
  duration_ms: 0.218127
  type: 'test'
  ...
# Subtest: shared vector: non-meet-lineup-follows-counted-links
ok 1589 - shared vector: non-meet-lineup-follows-counted-links
  ---
  duration_ms: 0.545763
  type: 'test'
  ...
# Subtest: shared vector: pre-buffer-starts-the-run-early
ok 1590 - shared vector: pre-buffer-starts-the-run-early
  ---
  duration_ms: 0.534461
  type: 'test'
  ...
# Subtest: shared vector: post-buffer-bridges-to-the-next-event
ok 1591 - shared vector: post-buffer-bridges-to-the-next-event
  ---
  duration_ms: 0.415854
  type: 'test'
  ...
# Subtest: shared vector: buffer-never-bridges-trackedness
ok 1592 - shared vector: buffer-never-bridges-trackedness
  ---
  duration_ms: 0.353746
  type: 'test'
  ...
# Subtest: shared vector: now-inside-a-lead-out-keeps-the-run
ok 1593 - shared vector: now-inside-a-lead-out-keeps-the-run
  ---
  duration_ms: 0.300494
  type: 'test'
  ...
# Subtest: shared vector: buffered-far-run-warns-from-the-buffered-start
ok 1594 - shared vector: buffered-far-run-warns-from-the-buffered-start
  ---
  duration_ms: 4.309041
  type: 'test'
  ...
# Subtest: shared vector: inherited-root-event-is-off-clock
ok 1595 - shared vector: inherited-root-event-is-off-clock
  ---
  duration_ms: 2.331904
  type: 'test'
  ...
# Subtest: shared vector: signed-later-unnamed-reaches-meet
ok 1596 - shared vector: signed-later-unnamed-reaches-meet
  ---
  duration_ms: 0.309681
  type: 'test'
  ...
# Subtest: shared vector: signed-later-named-meet-is-explicit
ok 1597 - shared vector: signed-later-named-meet-is-explicit
  ---
  duration_ms: 0.249707
  type: 'test'
  ...
# Subtest: shared vector: signed-later-fit-draft-keeps-plus
ok 1598 - shared vector: signed-later-fit-draft-keeps-plus
  ---
  duration_ms: 0.695819
  type: 'test'
  ...
# Subtest: every vector is either mirrored or listed as capture-only
ok 1599 - every vector is either mirrored or listed as capture-only
  ---
  duration_ms: 0.175254
  type: 'test'
  ...
# Subtest: off-clock tag detection mirrors bob's Rust rules for every spelling
ok 1600 - off-clock tag detection mirrors bob's Rust rules for every spelling
  ---
  duration_ms: 0.699206
  type: 'test'
  ...
# Subtest: clean titles strip every off-clock spelling and its sentence punctuation
ok 1601 - clean titles strip every off-clock spelling and its sentence punctuation
  ---
  duration_ms: 0.20929
  type: 'test'
  ...
# Subtest: Event rows carry status, clock, ids, and clean titles
ok 1602 - Event rows carry status, clock, ids, and clean titles
  ---
  duration_ms: 0.430482
  type: 'test'
  ...
# Subtest: N\\p and N\\P keep the row's key; a bare span is stamped [off::]; a conflict resolves to [t::]
ok 1603 - N\\p and N\\P keep the row's key; a bare span is stamped [off::]; a conflict resolves to [t::]
  ---
  duration_ms: 1.372521
  type: 'test'
  ...
# Subtest: N\\o and N\\O keep every key and field byte-for-byte
ok 1604 - N\\o and N\\O keep every key and field byte-for-byte
  ---
  duration_ms: 0.229228
  type: 'test'
  ...
# Subtest: pomodoroSessionClock reads all five row shapes like Rust session_clock
ok 1605 - pomodoroSessionClock reads all five row shapes like Rust session_clock
  ---
  duration_ms: 0.433347
  type: 'test'
  ...
# Subtest: setPomodoroLineClock moves the recorded minutes between keys like Rust set_ledger_clock
ok 1606 - setPomodoroLineClock moves the recorded minutes between keys like Rust set_ledger_clock
  ---
  duration_ms: 0.555471
  type: 'test'
  ...
# Subtest: a non-MEET se<X> start warns when it newly crosses an open event
ok 1607 - a non-MEET se<X> start warns when it newly crosses an open event
  ---
  duration_ms: 0.828502
  type: 'test'
  ...
# Subtest: a counted start that fits ends before the event and stays silent
ok 1608 - a counted start that fits ends before the event and stays silent
  ---
  duration_ms: 0.642738
  type: 'test'
  ...
# Subtest: a start with no fitting count omits the fit draft
ok 1609 - a start with no fitting count omits the fit draft
  ---
  duration_ms: 0.654801
  type: 'test'
  ...
# Subtest: MEET sessions, own-lineup events, and done events never warn
ok 1610 - MEET sessions, own-lineup events, and done events never warn
  ---
  duration_ms: 6.235049
  type: 'test'
  ...
# Subtest: \\p and \\o warn on new crossings only; \\P never warns
ok 1611 - \\p and \\o warn on new crossings only; \\P never warns
  ---
  duration_ms: 1.022283
  type: 'test'
  ...
# Subtest: event_buffer row vectors: parse, buffered span, clean title, field, label
ok 1612 - event_buffer row vectors: parse, buffered span, clean title, field, label
  ---
  duration_ms: 1.123887
  type: 'test'
  ...
# Subtest: event_buffer conflict vectors: shared predicate
ok 1613 - event_buffer conflict vectors: shared predicate
  ---
  duration_ms: 1.26202
  type: 'test'
  ...
# Subtest: event_buffer description vectors stay bob-cli's HTML reader
ok 1614 - event_buffer description vectors stay bob-cli's HTML reader
  ---
  duration_ms: 0.130039
  type: 'test'
  ...
# Subtest: a buffered se<X> start warns into the lead-in and fits at the buffered start
ok 1615 - a buffered se<X> start warns into the lead-in and fits at the buffered start
  ---
  duration_ms: 0.469998
  type: 'test'
  ...
# Subtest: a start that runs through the meeting names the event plus its buffer label
ok 1616 - a start that runs through the meeting names the event plus its buffer label
  ---
  duration_ms: 0.349868
  type: 'test'
  ...
# Subtest: a lead-out start names the after buffer and offers no fit
ok 1617 - a lead-out start names the after buffer and offers no fit
  ---
  duration_ms: 0.349838
  type: 'test'
  ...
# Subtest: an Event Task with a typed off-clock tag is painted by the Event scan
ok 1618 - an Event Task with a typed off-clock tag is painted by the Event scan
  ---
  duration_ms: 1.421636
  type: 'test'
  ...
# Subtest: an off-clock session's home chip is dashed, shows its minutes, and says so
ok 1619 - an off-clock session's home chip is dashed, shows its minutes, and says so
  ---
  duration_ms: 0.593704
  type: 'test'
  ...
# Subtest: Reading view marks the off-clock tag link and dashes the row's time pill
ok 1620 - Reading view marks the off-clock tag link and dashes the row's time pill
  ---
  duration_ms: 0.557535
  type: 'test'
  ...
# Subtest: Reading view marks every off-clock tag spelling and nothing else
ok 1621 - Reading view marks every off-clock tag spelling and nothing else
  ---
  duration_ms: 0.485638
  type: 'test'
  ...
# Subtest: an active-note Pomodoro target still jumps and centers immediately
ok 1622 - an active-note Pomodoro target still jumps and centers immediately
  ---
  duration_ms: 35.573334
  type: 'test'
  ...
# Subtest: Ctrl+9 from an unpinned daily copy switches to the pinned home tab
ok 1623 - Ctrl+9 from an unpinned daily copy switches to the pinned home tab
  ---
  duration_ms: 27.320281
  type: 'test'
  ...
# Subtest: Ctrl+9 on the pinned daily tab jumps in place when a copy exists
ok 1624 - Ctrl+9 on the pinned daily tab jumps in place when a copy exists
  ---
  duration_ms: 12.783685
  type: 'test'
  ...
# Subtest: Ctrl+9 switches daily copies without a Pomodoros section and stays quiet
ok 1625 - Ctrl+9 switches daily copies without a Pomodoros section and stays quiet
  ---
  duration_ms: 12.359256
  type: 'test'
  ...
# Subtest: Ctrl+9 keeps the active daily tab when equal-ranked copies exist
ok 1626 - Ctrl+9 keeps the active daily tab when equal-ranked copies exist
  ---
  duration_ms: 7.550402
  type: 'test'
  ...
# Subtest: Ctrl+9 from a sidebar daily copy switches to a main-area home tab
ok 1627 - Ctrl+9 from a sidebar daily copy switches to a main-area home tab
  ---
  duration_ms: 15.282851
  type: 'test'
  ...
# Subtest: the first fallback press only opens daily and the second press jumps
ok 1628 - the first fallback press only opens daily and the second press jumps
  ---
  duration_ms: 10.35266
  type: 'test'
  ...
# Subtest: a daily note with no target defers its notice until the second press
ok 1629 - a daily note with no target defers its notice until the second press
  ---
  duration_ms: 13.766594
  type: 'test'
  ...
# Subtest: an already-open daily leaf retains its live cursor and viewport
ok 1630 - an already-open daily leaf retains its live cursor and viewport
  ---
  duration_ms: 12.830987
  type: 'test'
  ...
# Subtest: a second press after reused-leaf fallback performs the Pomodoro jump
ok 1631 - a second press after reused-leaf fallback performs the Pomodoro jump
  ---
  duration_ms: 11.910226
  type: 'test'
  ...
# Subtest: the standalone daily-note command activates a reused daily leaf
ok 1632 - the standalone daily-note command activates a reused daily leaf
  ---
  duration_ms: 10.778647
  type: 'test'
  ...
# Subtest: Ctrl+9 loads and reuses a deferred pinned daily tab before falling back
ok 1633 - Ctrl+9 loads and reuses a deferred pinned daily tab before falling back
  ---
  duration_ms: 16.994169
  type: 'test'
  ...
# Subtest: pinned daily tabs win over earlier unpinned tabs
ok 1634 - pinned daily tabs win over earlier unpinned tabs
  ---
  duration_ms: 11.2374
  type: 'test'
  ...
# Subtest: a deferred sidebar daily tab is reused only without a main-area match
ok 1635 - a deferred sidebar daily tab is reused only without a main-area match
  ---
  duration_ms: 36.660411
  type: 'test'
  ...
# Subtest: a deferred sidebar daily tab is reused when there is no main-area match
ok 1636 - a deferred sidebar daily tab is reused when there is no main-area match
  ---
  duration_ms: 18.404399
  type: 'test'
  ...
# Subtest: a deferred non-Markdown daily path is ignored and uses the daily-note fallback
ok 1637 - a deferred non-Markdown daily path is ignored and uses the daily-note fallback
  ---
  duration_ms: 20.196406
  type: 'test'
  ...
# Subtest: the standalone daily-note command reuses a deferred pinned tab
ok 1638 - the standalone daily-note command reuses a deferred pinned tab
  ---
  duration_ms: 11.708891
  type: 'test'
  ...
# Subtest: Ctrl+9 opens the pinned daily tab from a non-Markdown active leaf
ok 1639 - Ctrl+9 opens the pinned daily tab from a non-Markdown active leaf
  ---
  duration_ms: 21.257712
  type: 'test'
  ...
# Subtest: a closed then reopened daily note restores its in-session location
ok 1640 - a closed then reopened daily note restores its in-session location
  ---
  duration_ms: 22.304959
  type: 'test'
  ...
# Subtest: different-path and invalid locations do not leak into a daily note
ok 1641 - different-path and invalid locations do not leak into a daily note
  ---
  duration_ms: 24.345671
  type: 'test'
  ...
# Subtest: out-of-range remembered coordinates are clamped safely
ok 1642 - out-of-range remembered coordinates are clamped safely
  ---
  duration_ms: 18.110708
  type: 'test'
  ...
# Subtest: a rapid second press cancels an older fallback restore
ok 1643 - a rapid second press cancels an older fallback restore
  ---
  duration_ms: 29.61797
  type: 'test'
  ...
# Subtest: navigation and unload clean up daily scroll listeners and deferred work
ok 1644 - navigation and unload clean up daily scroll listeners and deferred work
  ---
  duration_ms: 19.952637
  type: 'test'
  ...
# Subtest: NR1–NR7: no-reply pill model vectors pass verbatim
ok 1645 - NR1–NR7: no-reply pill model vectors pass verbatim
  ---
  duration_ms: 18.942869
  type: 'test'
  ...
# Subtest: no-reply pill replaces the exact \#awaiting_reply span
ok 1646 - no-reply pill replaces the exact \#awaiting_reply span
  ---
  duration_ms: 1.166538
  type: 'test'
  ...
# Subtest: NR1 Live Preview replace widget covers the tag; NR8 toggle off is empty
ok 1647 - NR1 Live Preview replace widget covers the tag; NR8 toggle off is empty
  ---
  duration_ms: 1.070284
  type: 'test'
  ...
# Subtest: Tasks query rows keep the native \#awaiting_reply pill
ok 1648 - Tasks query rows keep the native \#awaiting_reply pill
  ---
  duration_ms: 0.411486
  type: 'test'
  ...
# Subtest: styles.css contract: muted capsule under task-tag-marks
ok 1649 - styles.css contract: muted capsule under task-tag-marks
  ---
  duration_ms: 7.381799
  type: 'test'
  ...
# Subtest: crowded chip: over count is red with tooltip, aria, and names
ok 1650 - crowded chip: over count is red with tooltip, aria, and names
  ---
  duration_ms: 1.811881
  type: 'test'
  ...
# Subtest: crowded chip: calm zero and unavailable dash
ok 1651 - crowded chip: calm zero and unavailable dash
  ---
  duration_ms: 0.288331
  type: 'test'
  ...
# Subtest: crowded chip: names at most five notes
ok 1652 - crowded chip: names at most five notes
  ---
  duration_ms: 0.3402
  type: 'test'
  ...
# Subtest: crowded chip: classes, text, aria, and arrow
ok 1653 - crowded chip: classes, text, aria, and arrow
  ---
  duration_ms: 2.175315
  type: 'test'
  ...
# Subtest: crowded chip: refresh in place keeps the anchor, unload drops it
ok 1654 - crowded chip: refresh in place keeps the anchor, unload drops it
  ---
  duration_ms: 0.862597
  type: 'test'
  ...
# Subtest: anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
ok 1655 - anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
  ---
  duration_ms: 0.825006
  type: 'test'
  ...
# Subtest: ready-notes summary: crowded, calm, and unavailable
ok 1656 - ready-notes summary: crowded, calm, and unavailable
  ---
  duration_ms: 0.365788
  type: 'test'
  ...
# Subtest: ready-notes bar: cap tick and red overflow within 30 cells
ok 1657 - ready-notes bar: cap tick and red overflow within 30 cells
  ---
  duration_ms: 0.305023
  type: 'test'
  ...
# Subtest: ready-notes block: model and render with grid, pills, and footer
ok 1658 - ready-notes block: model and render with grid, pills, and footer
  ---
  duration_ms: 1.976595
  type: 'test'
  ...
# Subtest: ready-notes block: unavailable renders a dash line
ok 1659 - ready-notes block: unavailable renders a dash line
  ---
  duration_ms: 0.619243
  type: 'test'
  ...
# Subtest: heading matcher: fences, level, case, and first-only
ok 1660 - heading matcher: fences, level, case, and first-only
  ---
  duration_ms: 0.572002
  type: 'test'
  ...
# Subtest: heading chip copy: room, full, crowded, exempt, unavailable
ok 1661 - heading chip copy: room, full, crowded, exempt, unavailable
  ---
  duration_ms: 0.527177
  type: 'test'
  ...
# Subtest: heading chip key is stable for equal models
ok 1662 - heading chip key is stable for equal models
  ---
  duration_ms: 0.239587
  type: 'test'
  ...
# Subtest: reading view: appends the chip to the matching h2 only
ok 1663 - reading view: appends the chip to the matching h2 only
  ---
  duration_ms: 1.862217
  type: 'test'
  ...
# Subtest: reading view: no chip for ineligible notes
ok 1664 - reading view: no chip for ineligible notes
  ---
  duration_ms: 0.187408
  type: 'test'
  ...
# Subtest: one live-refresh fan-out reaches every family
ok 1665 - one live-refresh fan-out reaches every family
  ---
  duration_ms: 2.983869
  type: 'test'
  ...
# Subtest: ledger-tools CSS is theme-safe for the new views
ok 1666 - ledger-tools CSS is theme-safe for the new views
  ---
  duration_ms: 1.751696
  type: 'test'
  ...
# Subtest: maxReadyPerNote defaults to 5 and validates 1–999
ok 1667 - maxReadyPerNote defaults to 5 and validates 1–999
  ---
  duration_ms: 3.451372
  type: 'test'
  ...
# Subtest: loadPlanCaps caches on a stat key and detects edits
ok 1668 - loadPlanCaps caches on a stat key and detects edits
  ---
  duration_ms: 0.637046
  type: 'test'
  ...
# Subtest: loadPlanCaps handles deletion, invalid edits, and recovery
ok 1669 - loadPlanCaps handles deletion, invalid edits, and recovery
  ---
  duration_ms: 0.618802
  type: 'test'
  ...
# Subtest: loadPlanCaps without statSync reads through uncached
ok 1670 - loadPlanCaps without statSync reads through uncached
  ---
  duration_ms: 0.385626
  type: 'test'
  ...
# Subtest: noteFrontmatter resolves through getFileCache, not getCache
ok 1671 - noteFrontmatter resolves through getFileCache, not getCache
  ---
  duration_ms: 0.788727
  type: 'test'
  ...
# Subtest: task_refresh applies through the shared reader
ok 1672 - task_refresh applies through the shared reader
  ---
  duration_ms: 30.276815
  type: 'test'
  ...
# Subtest: noteReadyKindFromType covers every R11 form
ok 1673 - noteReadyKindFromType covers every R11 form
  ---
  duration_ms: 0.864251
  type: 'test'
  ...
# Subtest: noteReadyStatusLabel mirrors ProjectStatus::parse
ok 1674 - noteReadyStatusLabel mirrors ProjectStatus::parse
  ---
  duration_ms: 0.380266
  type: 'test'
  ...
# Subtest: noteReadyParentStem strips alias, heading, and path
ok 1675 - noteReadyParentStem strips alias, heading, and path
  ---
  duration_ms: 0.515053
  type: 'test'
  ...
# Subtest: parseNoteReadyCap covers every R8 form
ok 1676 - parseNoteReadyCap covers every R8 form
  ---
  duration_ms: 1.19853
  type: 'test'
  ...
# Subtest: R1: 6 tasks at the default cap are crowded with over_by 1
ok 1677 - R1: 6 tasks at the default cap are crowded with over_by 1
  ---
  duration_ms: 24.188146
  type: 'test'
  ...
# Subtest: R2: 5 tasks are full with no lint
ok 1678 - R2: 5 tasks are full with no lint
  ---
  duration_ms: 30.443876
  type: 'test'
  ...
# Subtest: R3: hidden, future, blocked, and non-TODO rows never count
ok 1679 - R3: hidden, future, blocked, and non-TODO rows never count
  ---
  duration_ms: 49.193315
  type: 'test'
  ...
# Subtest: R4: make-up splits 1 ready + 1 new + 1 rotten
ok 1680 - R4: make-up splits 1 ready + 1 new + 1 rotten
  ---
  duration_ms: 48.174069
  type: 'test'
  ...
# Subtest: R5: recurring rows are excluded but tallied
ok 1681 - R5: recurring rows are excluded but tallied
  ---
  duration_ms: 36.756602
  type: 'test'
  ...
# Subtest: R6: a visible ^prj task never counts
ok 1682 - R6: a visible ^prj task never counts
  ---
  duration_ms: 40.864849
  type: 'test'
  ...
# Subtest: R7: daily, untyped, template, done, and dash rows are absent
ok 1683 - R7: daily, untyped, template, done, and dash rows are absent
  ---
  duration_ms: 73.526471
  type: 'test'
  ...
# Subtest: R8: ready_cap forms map to cap, exempt, or lint-then-default
ok 1684 - R8: ready_cap forms map to cap, exempt, or lint-then-default
  ---
  duration_ms: 77.611343
  type: 'test'
  ...
# Subtest: R9: a parent with two children counts 3
ok 1685 - R9: a parent with two children counts 3
  ---
  duration_ms: 40.565897
  type: 'test'
  ...
# Subtest: R10: terminal projects are not capped and lint once
ok 1686 - R10: terminal projects are not capped and lint once
  ---
  duration_ms: 46.89232
  type: 'test'
  ...
# Subtest: R11: every type form and nested folders are eligible
ok 1687 - R11: every type form and nested folders are eligible
  ---
  duration_ms: 22.487341
  type: 'test'
  ...
# Subtest: R12: stamping a NEW task keeps the count and moves the make-up
ok 1688 - R12: stamping a NEW task keeps the count and moves the make-up
  ---
  duration_ms: 22.230046
  type: 'test'
  ...
# Subtest: R13: a Today-linked task still counts
ok 1689 - R13: a Today-linked task still counts
  ---
  duration_ms: 13.784659
  type: 'test'
  ...
# Subtest: R14: max_ready_per_note 3 caps others while ready_cap 8 holds
ok 1690 - R14: max_ready_per_note 3 caps others while ready_cap 8 holds
  ---
  duration_ms: 13.728151
  type: 'test'
  ...
# Subtest: api.noteReady is frozen at version 1 under api v3
ok 1691 - api.noteReady is frozen at version 1 under api v3
  ---
  duration_ms: 18.711876
  type: 'test'
  ...
# Subtest: counted and inCrowdedNote resolve per task
ok 1692 - counted and inCrowdedNote resolve per task
  ---
  duration_ms: 30.747426
  type: 'test'
  ...
# Subtest: groupLabel ranks crowded notes by excess
ok 1693 - groupLabel ranks crowded notes by excess
  ---
  duration_ms: 100.2499
  type: 'test'
  ...
# Subtest: snapshot sorts crowded, full, room, empty, exempt and splits totals
ok 1694 - snapshot sorts crowded, full, room, empty, exempt and splits totals
  ---
  duration_ms: 67.819699
  type: 'test'
  ...
# Subtest: missing Tasks data and a cold cache are unavailable, never zero
ok 1695 - missing Tasks data and a cold cache are unavailable, never zero
  ---
  duration_ms: 59.79749
  type: 'test'
  ...
# Subtest: throwing Tasks guards never throw
ok 1696 - throwing Tasks guards never throw
  ---
  duration_ms: 35.855401
  type: 'test'
  ...
# Subtest: snapshot reuses the memo without reparsing or re-walking
ok 1697 - snapshot reuses the memo without reparsing or re-walking
  ---
  duration_ms: 32.02273
  type: 'test'
  ...
# Subtest: a task edit rebuilds through the cache-update handler
ok 1698 - a task edit rebuilds through the cache-update handler
  ---
  duration_ms: 47.992462
  type: 'test'
  ...
# Subtest: a ready_cap edit rebuilds and fires the query-refresh trigger
ok 1699 - a ready_cap edit rebuilds and fires the query-refresh trigger
  ---
  duration_ms: 55.910256
  type: 'test'
  ...
# Subtest: rename and delete move the eligibility entry
ok 1700 - rename and delete move the eligibility entry
  ---
  duration_ms: 39.808902
  type: 'test'
  ...
# Subtest: day rollover rebuilds the snapshot date
ok 1701 - day rollover rebuilds the snapshot date
  ---
  duration_ms: 51.998482
  type: 'test'
  ...
# Subtest: a config edit flows through the stat cache
ok 1702 - a config edit flows through the stat cache
  ---
  duration_ms: 37.360616
  type: 'test'
  ...
# Subtest: untyped and non-markdown vault events are no-ops
ok 1703 - untyped and non-markdown vault events are no-ops
  ---
  duration_ms: 25.831046
  type: 'test'
  ...
# Subtest: memo hits never re-walk the vault
ok 1704 - memo hits never re-walk the vault
  ---
  duration_ms: 459.760248
  type: 'test'
  ...
# Subtest: the startup storm is linear
ok 1705 - the startup storm is linear
  ---
  duration_ms: 292.807851
  type: 'test'
  ...
# Subtest: the first resolved event forces one rebuild and later ones do not
ok 1706 - the first resolved event forces one rebuild and later ones do not
  ---
  duration_ms: 53.161895
  type: 'test'
  ...
# Subtest: noteReadyEvaluate is pure and mirrors the Rust totals
ok 1707 - noteReadyEvaluate is pure and mirrors the Rust totals
  ---
  duration_ms: 0.476209
  type: 'test'
  ...
# Subtest: styles.css scopes the notebook card, icon, tree, chips, and focus
ok 1708 - styles.css scopes the notebook card, icon, tree, chips, and focus
  ---
  duration_ms: 17.016983
  type: 'test'
  ...
# Subtest: age and count chips treat missing data as unavailable, not zero
ok 1709 - age and count chips treat missing data as unavailable, not zero
  ---
  duration_ms: 0.993508
  type: 'test'
  ...
# Subtest: source regions skip fenced examples and classify project groups
ok 1710 - source regions skip fenced examples and classify project groups
  ---
  duration_ms: 7.338657
  type: 'test'
  ...
# Subtest: sync action follows catalog state and stays hidden when current
ok 1711 - sync action follows catalog state and stays hidden when current
  ---
  duration_ms: 0.378634
  type: 'test'
  ...
# Subtest: rows match by resolved path/stem, not display title
ok 1712 - rows match by resolved path/stem, not display title
  ---
  duration_ms: 1.519021
  type: 'test'
  ...
# Subtest: host hue uses pomodoro home ancestry and falls back to neutral
ok 1713 - host hue uses pomodoro home ancestry and falls back to neutral
  ---
  duration_ms: 7.486778
  type: 'test'
  ...
# Subtest: Reading view paints hue, nested chips, and skips project groups on a real callout
ok 1714 - Reading view paints hue, nested chips, and skips project groups on a real callout
  ---
  duration_ms: 25.263712
  type: 'test'
  ...
# Subtest: folded callout chrome still receives data-root-hue
ok 1715 - folded callout chrome still receives data-root-hue
  ---
  duration_ms: 1.720136
  type: 'test'
  ...
# Subtest: repeat mounting does not duplicate chips or sync actions
ok 1716 - repeat mounting does not duplicate chips or sync actions
  ---
  duration_ms: 3.540632
  type: 'test'
  ...
# Subtest: malicious report strings never become HTML
ok 1717 - malicious report strings never become HTML
  ---
  duration_ms: 5.437305
  type: 'test'
  ...
# Subtest: fenced example callouts are left alone
ok 1718 - fenced example callouts are left alone
  ---
  duration_ms: 1.684006
  type: 'test'
  ...
# Subtest: missing catalog without an H2 puts sync on the host title
ok 1719 - missing catalog without an H2 puts sync on the host title
  ---
  duration_ms: 0.775962
  type: 'test'
  ...
# Subtest: busy sync disables the same action mouse and keyboard invoke
ok 1720 - busy sync disables the same action mouse and keyboard invoke
  ---
  duration_ms: 9.824152
  type: 'test'
  ...
# Subtest: add-summary fallback opens the notebook and explains Properties
ok 1721 - add-summary fallback opens the notebook and explains Properties
  ---
  duration_ms: 1.430693
  type: 'test'
  ...
# Subtest: catalog paint never writes note bytes, including hue-only refresh
ok 1722 - catalog paint never writes note bytes, including hue-only refresh
  ---
  duration_ms: 7.540984
  type: 'test'
  ...
# Subtest: Live Preview decorations gate on live preview and skip source mode
ok 1723 - Live Preview decorations gate on live preview and skip source mode
  ---
  duration_ms: 1.971646
  type: 'test'
  ...
# Subtest: Live Preview paints the actual callout DOM, not only source lines
ok 1724 - Live Preview paints the actual callout DOM, not only source lines
  ---
  duration_ms: 6.630204
  type: 'test'
  ...
# Subtest: reading postprocessor registers a render child and unloads it
ok 1725 - reading postprocessor registers a render child and unloads it
  ---
  duration_ms: 1.330973
  type: 'test'
  ...
# Subtest: all catalog states stay visible until the list report changes them
ok 1726 - all catalog states stay visible until the list report changes them
  ---
  duration_ms: 0.527648
  type: 'test'
  ...
# Subtest: first list failure is unavailable with a list retry, not invented zeros
ok 1727 - first list failure is unavailable with a list retry, not invented zeros
  ---
  duration_ms: 5.09935
  type: 'test'
  ...
# Subtest: stale last-good catalog keeps counts and offers retry
ok 1728 - stale last-good catalog keeps counts and offers retry
  ---
  duration_ms: 1.452665
  type: 'test'
  ...
# Subtest: retry recovers after a later successful list
ok 1729 - retry recovers after a later successful list
  ---
  duration_ms: 4.305613
  type: 'test'
  ...
# Subtest: sync refusal keeps damaged feedback until the list succeeds
ok 1730 - sync refusal keeps damaged feedback until the list succeeds
  ---
  duration_ms: 0.619172
  type: 'test'
  ...
# Subtest: missing catalog without H1 or H2 uses a rendered-only anchor
ok 1731 - missing catalog without H1 or H2 uses a rendered-only anchor
  ---
  duration_ms: 0.559719
  type: 'test'
  ...
# Subtest: host hue uses the local override and honour mute, not root_hue
ok 1732 - host hue uses the local override and honour mute, not root_hue
  ---
  duration_ms: 0.538939
  type: 'test'
  ...
# Subtest: Live Preview and Reading both expose retry after a first fetch failure
ok 1733 - Live Preview and Reading both expose retry after a first fetch failure
  ---
  duration_ms: 1.07887
  type: 'test'
  ...
# Subtest: daily note with generation lag gets no catalog chrome
ok 1734 - daily note with generation lag gets no catalog chrome
  ---
  duration_ms: 0.507199
  type: 'test'
  ...
# Subtest: non-host note with a failed report gets no catalog chrome
ok 1735 - non-host note with a failed report gets no catalog chrome
  ---
  duration_ms: 0.5442
  type: 'test'
  ...
# Subtest: host with a failed refresh shows Retry at its H2
ok 1736 - host with a failed refresh shows Retry at its H2
  ---
  duration_ms: 0.74338
  type: 'test'
  ...
# Subtest: host with lag only shows no Retry
ok 1737 - host with lag only shows no Retry
  ---
  duration_ms: 11.561633
  type: 'test'
  ...
# Subtest: bare callout blocks are regions and legacy pairs are recognized
ok 1738 - bare callout blocks are regions and legacy pairs are recognized
  ---
  duration_ms: 0.435452
  type: 'test'
  ...
# Subtest: add-summary focuses the opened notebook view, never another pane
ok 1739 - add-summary focuses the opened notebook view, never another pane
  ---
  duration_ms: 8.746856
  type: 'test'
  ...
# Subtest: create and metadata events refresh the shared catalog through one cache
ok 1740 - create and metadata events refresh the shared catalog through one cache
  ---
  duration_ms: 33.191733
  type: 'test'
  ...
# Subtest: desktop-unavailable live data is explicit and read-only styling still paints
ok 1741 - desktop-unavailable live data is explicit and read-only styling still paints
  ---
  duration_ms: 1.432667
  type: 'test'
  ...
# Subtest: header model follows parent identities, not breadcrumb labels
ok 1742 - header model follows parent identities, not breadcrumb labels
  ---
  duration_ms: 2.714384
  type: 'test'
  ...
# Subtest: deep ancestry collapses with ellipsis and stays bounded
ok 1743 - deep ancestry collapses with ellipsis and stays bounded
  ---
  duration_ms: 1.053933
  type: 'test'
  ...
# Subtest: missing parent is bounded and honest; cycles do not loop
ok 1744 - missing parent is bounded and honest; cycles do not loop
  ---
  duration_ms: 0.449678
  type: 'test'
  ...
# Subtest: non-root project owner shows root and owner; duplicate titles order by path
ok 1745 - non-root project owner shows root and owner; duplicate titles order by path
  ---
  duration_ms: 24.820113
  type: 'test'
  ...
# Subtest: empty children omit the row; renamed/missing children are filtered
ok 1746 - empty children omit the row; renamed/missing children are filtered
  ---
  duration_ms: 0.699546
  type: 'test'
  ...
# Subtest: non-notebook paths produce no header
ok 1747 - non-notebook paths produce no header
  ---
  duration_ms: 0.245329
  type: 'test'
  ...
# Subtest: chips default on; catalog paint respects the toggle
ok 1748 - chips default on; catalog paint respects the toggle
  ---
  duration_ms: 0.422537
  type: 'test'
  ...
# Subtest: settings persist without discarding unrelated keys
ok 1749 - settings persist without discarding unrelated keys
  ---
  duration_ms: 0.494094
  type: 'test'
  ...
# Subtest: Reading paint inserts below H1, avoids duplicates, preserves focus
ok 1750 - Reading paint inserts below H1, avoids duplicates, preserves focus
  ---
  duration_ms: 9.624663
  type: 'test'
  ...
# Subtest: Live Preview anchor skips frontmatter; Source mode yields no decorations
ok 1751 - Live Preview anchor skips frontmatter; Source mode yields no decorations
  ---
  duration_ms: 11.729704
  type: 'test'
  ...
# Subtest: lifecycle setup and teardown manage header widgets
ok 1752 - lifecycle setup and teardown manage header widgets
  ---
  duration_ms: 0.768919
  type: 'test'
  ...
# Subtest: self crumb links to the notebook; ellipsis stays inert
ok 1753 - self crumb links to the notebook; ellipsis stays inert
  ---
  duration_ms: 1.267371
  type: 'test'
  ...
# Subtest: widget signature changes with labels, hue, and chips
ok 1754 - widget signature changes with labels, hue, and chips
  ---
  duration_ms: 0.398912
  type: 'test'
  ...
# Subtest: deep non-root project ancestry keeps intermediate owners
ok 1755 - deep non-root project ancestry keeps intermediate owners
  ---
  duration_ms: 5.252051
  type: 'test'
  ...
# Subtest: H1-less notes place the header at the first content position
ok 1756 - H1-less notes place the header at the first content position
  ---
  duration_ms: 0.537917
  type: 'test'
  ...
# Subtest: Reading embed stays in its surface; host cleanup leaves it
ok 1757 - Reading embed stays in its surface; host cleanup leaves it
  ---
  duration_ms: 0.744061
  type: 'test'
  ...
# Subtest: Live Preview widget survives paint, refresh, and equality transitions
ok 1758 - Live Preview widget survives paint, refresh, and equality transitions
  ---
  duration_ms: 1.283531
  type: 'test'
  ...
# Subtest: header refresh restores keyboard focus
ok 1759 - header refresh restores keyboard focus
  ---
  duration_ms: 5.781271
  type: 'test'
  ...
# Subtest: refreshNotebookHeaderAll restores header focus after editor refresh
ok 1760 - refreshNotebookHeaderAll restores header focus after editor refresh
  ---
  duration_ms: 1.274264
  type: 'test'
  ...
# Subtest: late chips load refreshes catalogs and ignores a stale epoch
ok 1761 - late chips load refreshes catalogs and ignores a stale epoch
  ---
  duration_ms: 0.322907
  type: 'test'
  ...
# Subtest: Reading section paints coalesce onto one attached surface
ok 1762 - Reading section paints coalesce onto one attached surface
  ---
  duration_ms: 9.365418
  type: 'test'
  ...
# Subtest: notebooksCreateDecodeReport accepts the bob notebooks create envelope
ok 1763 - notebooksCreateDecodeReport accepts the bob notebooks create envelope
  ---
  duration_ms: 1.596609
  type: 'test'
  ...
# Subtest: notebooksCreateDecodeReport keeps the refusal code, message, and hint
ok 1764 - notebooksCreateDecodeReport keeps the refusal code, message, and hint
  ---
  duration_ms: 0.397669
  type: 'test'
  ...
# Subtest: notebooksCreateDecodeReport rejects unknown bob, versions, and shapes
ok 1765 - notebooksCreateDecodeReport rejects unknown bob, versions, and shapes
  ---
  duration_ms: 0.421044
  type: 'test'
  ...
# Subtest: notebooksCreateArgs puts free text in long options and positionals after --
ok 1766 - notebooksCreateArgs puts free text in long options and positionals after --
  ---
  duration_ms: 1.201875
  type: 'test'
  ...
# Subtest: apiNotebooksCreate spawns one real create and returns the report
ok 1767 - apiNotebooksCreate spawns one real create and returns the report
  ---
  duration_ms: 0.508651
  type: 'test'
  ...
# Subtest: apiNotebooksCreate refuses a blank request without spawning
ok 1768 - apiNotebooksCreate refuses a blank request without spawning
  ---
  duration_ms: 0.227845
  type: 'test'
  ...
# Subtest: apiNotebooksCreate resolves desktop_only off the desktop and never throws
ok 1769 - apiNotebooksCreate resolves desktop_only off the desktop and never throws
  ---
  duration_ms: 0.505606
  type: 'test'
  ...
# Subtest: the notebooks api shape carries version 1 with create
ok 1770 - the notebooks api shape carries version 1 with create
  ---
  duration_ms: 0.247122
  type: 'test'
  ...
# Subtest: notebook list and sync use fixed JSON argv and the versioned report decoders
ok 1771 - notebook list and sync use fixed JSON argv and the versioned report decoders
  ---
  duration_ms: 5.175836
  type: 'test'
  ...
# Subtest: type encodings normalize like Bob and only notebook frontmatter changes sync
ok 1772 - type encodings normalize like Bob and only notebook frontmatter changes sync
  ---
  duration_ms: 2.247362
  type: 'test'
  ...
# Subtest: notebook subprocess uses bobSpawnJson with vault, timeout, and bounded output
ok 1773 - notebook subprocess uses bobSpawnJson with vault, timeout, and bounded output
  ---
  duration_ms: 4.15146
  type: 'test'
  ...
# Subtest: one vault-scoped list flight serves simultaneous subscribers
ok 1774 - one vault-scoped list flight serves simultaneous subscribers
  ---
  duration_ms: 1.064413
  type: 'test'
  ...
# Subtest: a change during list fetch coalesces into one later generation
ok 1775 - a change during list fetch coalesces into one later generation
  ---
  duration_ms: 1.248444
  type: 'test'
  ...
# Subtest: failed refresh keeps last good data stale and retries only on new demand
ok 1776 - failed refresh keeps last good data stale and retries only on new demand
  ---
  duration_ms: 0.674318
  type: 'test'
  ...
# Subtest: unload clears subscriptions and prevents a late list result from repainting
ok 1777 - unload clears subscriptions and prevents a late list result from repainting
  ---
  duration_ms: 0.63346
  type: 'test'
  ...
# Subtest: startup seeds frontmatter silently; only structural notebook edits debounce sync
ok 1778 - startup seeds frontmatter silently; only structural notebook edits debounce sync
  ---
  duration_ms: 0.973439
  type: 'test'
  ...
# Subtest: headless setup does not keep the process alive with a browser rollover timer
ok 1779 - headless setup does not keep the process alive with a browser rollover timer
  ---
  duration_ms: 0.587212
  type: 'test'
  ...
# Subtest: body edits invalidate display data without scheduling catalog sync
ok 1780 - body edits invalidate display data without scheduling catalog sync
  ---
  duration_ms: 8.657395
  type: 'test'
  ...
# Subtest: frontmatter notebook type transitions sync in both directions
ok 1781 - frontmatter notebook type transitions sync in both directions
  ---
  duration_ms: 0.873688
  type: 'test'
  ...
# Subtest: automatic and manual sync share one flight and revalidate after a partial failure
ok 1782 - automatic and manual sync share one flight and revalidate after a partial failure
  ---
  duration_ms: 1.188459
  type: 'test'
  ...
# Subtest: sync waits out a pre-write list and then fetches a post-sync catalog report
ok 1783 - sync waits out a pre-write list and then fetches a post-sync catalog report
  ---
  duration_ms: 0.885441
  type: 'test'
  ...
# Subtest: the trailing three-second sync fires once after parent and summary edits
ok 1784 - the trailing three-second sync fires once after parent and summary edits
  ---
  duration_ms: 9.688914
  type: 'test'
  ...
# Subtest: a view-show demand refreshes the shared report and local-day rollover notifies
ok 1785 - a view-show demand refreshes the shared report and local-day rollover notifies
  ---
  duration_ms: 1.041369
  type: 'test'
  ...
# Subtest: OC: only exact ledger Task Link rows in canonical daily Pomodoros qualify
ok 1786 - OC: only exact ledger Task Link rows in canonical daily Pomodoros qualify
  ---
  duration_ms: 6.494945
  type: 'test'
  ...
# Subtest: OC10 and OC15: history is included and toggle-off is a CSS and JavaScript gate
ok 1787 - OC10 and OC15: history is included and toggle-off is a CSS and JavaScript gate
  ---
  duration_ms: 2.245388
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: unlinked-stays-on-the-clock
ok 1788 - OV parity with the se<X> writer: unlinked-stays-on-the-clock
  ---
  duration_ms: 1.666583
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: all-off-clock-non-meet
ok 1789 - OV parity with the se<X> writer: all-off-clock-non-meet
  ---
  duration_ms: 1.643489
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: mixed-stays-on-the-clock
ok 1790 - OV parity with the se<X> writer: mixed-stays-on-the-clock
  ---
  duration_ms: 1.831327
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: unresolved-stays-on-the-clock
ok 1791 - OV parity with the se<X> writer: unresolved-stays-on-the-clock
  ---
  duration_ms: 0.493984
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: alias-off-clock
ok 1792 - OV parity with the se<X> writer: alias-off-clock
  ---
  duration_ms: 0.475889
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: nested-tag-rejected
ok 1793 - OV parity with the se<X> writer: nested-tag-rejected
  ---
  duration_ms: 0.426003
  type: 'test'
  ...
# Subtest: OV excluded: meet-run-ignores-future-off-clock-queue
ok 1794 - OV excluded: meet-run-ignores-future-off-clock-queue
  ---
  duration_ms: 0.489785
  type: 'test'
  ...
# Subtest: OV excluded: close-defers-not-started-off-clock
ok 1795 - OV excluded: close-defers-not-started-off-clock
  ---
  duration_ms: 4.739182
  type: 'test'
  ...
# Subtest: OV excluded: close-mixed-after-dropping-on-clock
ok 1796 - OV excluded: close-mixed-after-dropping-on-clock
  ---
  duration_ms: 0.528339
  type: 'test'
  ...
# Subtest: OV excluded: kept-ledger-swap-switches-key
ok 1797 - OV excluded: kept-ledger-swap-switches-key
  ---
  duration_ms: 0.131521
  type: 'test'
  ...
# Subtest: OV excluded: bare-row-restamped-at-close
ok 1798 - OV excluded: bare-row-restamped-at-close
  ---
  duration_ms: 0.105842
  type: 'test'
  ...
# Subtest: OV excluded: conflict-row-at-close
ok 1799 - OV excluded: conflict-row-at-close
  ---
  duration_ms: 0.105772
  type: 'test'
  ...
# Subtest: OV excluded: running-link-restamps
ok 1800 - OV excluded: running-link-restamps
  ---
  duration_ms: 0.096274
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: love-default-untagged-child-is-off-clock
ok 1801 - OV parity with the se<X> writer: love-default-untagged-child-is-off-clock
  ---
  duration_ms: 1.389193
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: event-task-root-abby-inherits-love
ok 1802 - OV parity with the se<X> writer: event-task-root-abby-inherits-love
  ---
  duration_ms: 13.309561
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: false-child-true-grandchild-is-off-clock
ok 1803 - OV parity with the se<X> writer: false-child-true-grandchild-is-off-clock
  ---
  duration_ms: 1.110631
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: untyped-dog-passes-inheritance-through
ok 1804 - OV parity with the se<X> writer: untyped-dog-passes-inheritance-through
  ---
  duration_ms: 0.453587
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: on-tag-under-love-stays-worked
ok 1805 - OV parity with the se<X> writer: on-tag-under-love-stays-worked
  ---
  duration_ms: 0.296656
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: on-off-conflict-stays-worked
ok 1806 - OV parity with the se<X> writer: on-off-conflict-stays-worked
  ---
  duration_ms: 0.197447
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: invalid-note-offclock-stays-worked
ok 1807 - OV parity with the se<X> writer: invalid-note-offclock-stays-worked
  ---
  duration_ms: 0.412959
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: invalid-root-on-daily-stays-worked
ok 1808 - OV parity with the se<X> writer: invalid-root-on-daily-stays-worked
  ---
  duration_ms: 0.668096
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: love-plus-job-stays-worked-mixed
ok 1809 - OV parity with the se<X> writer: love-plus-job-stays-worked-mixed
  ---
  duration_ms: 2.80134
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: explicit-off-beats-false-child
ok 1810 - OV parity with the se<X> writer: explicit-off-beats-false-child
  ---
  duration_ms: 0.480699
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: type-list-meet-at-love-child-is-off-clock
ok 1811 - OV parity with the se<X> writer: type-list-meet-at-love-child-is-off-clock
  ---
  duration_ms: 2.084692
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: type-list-chore-at-love-child-is-worked
ok 1812 - OV parity with the se<X> writer: type-list-chore-at-love-child-is-worked
  ---
  duration_ms: 0.348195
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: type-list-meet-plus-chore-is-mixed
ok 1813 - OV parity with the se<X> writer: type-list-meet-plus-chore-is-mixed
  ---
  duration_ms: 0.344197
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: child-list-narrows-parent-true
ok 1814 - OV parity with the se<X> writer: child-list-narrows-parent-true
  ---
  duration_ms: 0.312998
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: child-false-under-parent-list-is-worked
ok 1815 - OV parity with the se<X> writer: child-false-under-parent-list-is-worked
  ---
  duration_ms: 0.190814
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: dual-key-list-wins-without-capture-warning
ok 1816 - OV parity with the se<X> writer: dual-key-list-wins-without-capture-warning
  ---
  duration_ms: 0.258774
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: scalar-type-list-is-one-item-list
ok 1817 - OV parity with the se<X> writer: scalar-type-list-is-one-item-list
  ---
  duration_ms: 0.245499
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: empty-type-list-blank-inherits-true
ok 1818 - OV parity with the se<X> writer: empty-type-list-blank-inherits-true
  ---
  duration_ms: 0.252342
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: empty-type-list-flow-empty-inherits-true
ok 1819 - OV parity with the se<X> writer: empty-type-list-flow-empty-inherits-true
  ---
  duration_ms: 0.229949
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: empty-type-list-null-inherits-true
ok 1820 - OV parity with the se<X> writer: empty-type-list-null-inherits-true
  ---
  duration_ms: 0.283582
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: empty-type-list-lone-dash-inherits-true
ok 1821 - OV parity with the se<X> writer: empty-type-list-lone-dash-inherits-true
  ---
  duration_ms: 4.857045
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: invalid-type-list-item-stays-worked
ok 1822 - OV parity with the se<X> writer: invalid-type-list-item-stays-worked
  ---
  duration_ms: 0.291486
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: type-list-on-note-is-ignored
ok 1823 - OV parity with the se<X> writer: type-list-on-note-is-ignored
  ---
  duration_ms: 0.265396
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: on-tag-on-meet-stays-worked
ok 1824 - OV parity with the se<X> writer: on-tag-on-meet-stays-worked
  ---
  duration_ms: 0.184402
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: off-tag-on-chore-is-off-clock
ok 1825 - OV parity with the se<X> writer: off-tag-on-chore-is-off-clock
  ---
  duration_ms: 0.196936
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: meet-from-note-task-type-default-is-off-clock
ok 1826 - OV parity with the se<X> writer: meet-from-note-task-type-default-is-off-clock
  ---
  duration_ms: 1.616568
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: closed-untyped-link-under-type-list-is-worked
ok 1827 - OV parity with the se<X> writer: closed-untyped-link-under-type-list-is-worked
  ---
  duration_ms: 4.683335
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: chore-from-config-default-type-is-off-clock
ok 1828 - OV parity with the se<X> writer: chore-from-config-default-type-is-off-clock
  ---
  duration_ms: 0.628881
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: reading-task-with-ref-block-is-off-clock
ok 1829 - OV parity with the se<X> writer: reading-task-with-ref-block-is-off-clock
  ---
  duration_ms: 0.417337
  type: 'test'
  ...
# Subtest: OV parity with the se<X> writer: task-type-off-with-configured-default-is-off-clock
ok 1830 - OV parity with the se<X> writer: task-type-off-with-configured-default-is-off-clock
  ---
  duration_ms: 0.495577
  type: 'test'
  ...
# Subtest: OV exclusions account for every vector omitted from link-level parity
ok 1831 - OV exclusions account for every vector omitted from link-level parity
  ---
  duration_ms: 3.761605
  type: 'test'
  ...
# Subtest: OR/OT: target line facts select tagged and inherited clocks with canonical tooltip text
ok 1832 - OR/OT: target line facts select tagged and inherited clocks with canonical tooltip text
  ---
  duration_ms: 1.676362
  type: 'test'
  ...
# Subtest: OT and OP3: builder uses one listener-free accessible host with no title
ok 1833 - OT and OP3: builder uses one listener-free accessible host with no title
  ---
  duration_ms: 0.355119
  type: 'test'
  ...
# Subtest: OP1, OP2, and OP4: widget placement is side 4, after other chips, and selection-only updates do not rebuild
ok 1834 - OP1, OP2, and OP4: widget placement is side 4, after other chips, and selection-only updates do not rebuild
  ---
  duration_ms: 8.028815
  type: 'test'
  ...
# Subtest: OP1/interaction: plain mousedown restores the caret; Mod-click opens the task
ok 1835 - OP1/interaction: plain mousedown restores the caret; Mod-click opens the task
  ---
  duration_ms: 0.632347
  type: 'test'
  ...
# Subtest: writer delegation and metadata-cache freshness preserve path-aware resolution
ok 1836 - writer delegation and metadata-cache freshness preserve path-aware resolution
  ---
  duration_ms: 0.876334
  type: 'test'
  ...
# Subtest: toggle refreshes both surfaces and the Reading context allow-list recognizes the chip
ok 1837 - toggle refreshes both surfaces and the Reading context allow-list recognizes the chip
  ---
  duration_ms: 0.432657
  type: 'test'
  ...
# Subtest: setup registers the default-on command, Live Preview extension, Reading processor, and source listeners
ok 1838 - setup registers the default-on command, Live Preview extension, Reading processor, and source listeners
  ---
  duration_ms: 0.744161
  type: 'test'
  ...
# Subtest: 200-link / 50-target Live Preview build memoizes targets and stays near the 25 ms budget
ok 1839 - 200-link / 50-target Live Preview build memoizes targets and stays near the 25 ms budget
  ---
  duration_ms: 17.287256
  type: 'test'
  ...
# Subtest: Reading sweep handles closed daily ledger rows and reconciles the chip after its anchor
ok 1840 - Reading sweep handles closed daily ledger rows and reconciles the chip after its anchor
  ---
  duration_ms: 2.22525
  type: 'test'
  ...
# Subtest: Event Task CSS keeps one shared chip appearance while link chips are independent
ok 1841 - Event Task CSS keeps one shared chip appearance while link chips are independent
  ---
  duration_ms: 2.418008
  type: 'test'
  ...
# Subtest: week note paths follow the ISO week-year golden facts
ok 1842 - week note paths follow the ISO week-year golden facts
  ---
  duration_ms: 2.835546
  type: 'test'
  ...
# Subtest: ensure argv, adoption path, and timing constants match the contract
ok 1843 - ensure argv, adoption path, and timing constants match the contract
  ---
  duration_ms: 0.281969
  type: 'test'
  ...
# Subtest: adoption gate keeps ensure inert without all_time.md
ok 1844 - adoption gate keeps ensure inert without all_time.md
  ---
  duration_ms: 0.503943
  type: 'test'
  ...
# Subtest: create trigger reuses the daily-note file test and fires once per path
ok 1845 - create trigger reuses the daily-note file test and fires once per path
  ---
  duration_ms: 25.476367
  type: 'test'
  ...
# Subtest: create trigger shares the gcal file test
ok 1846 - create trigger shares the gcal file test
  ---
  duration_ms: 0.767536
  type: 'test'
  ...
# Subtest: layout-ready and midnight ticks share one once-per-day slot
ok 1847 - layout-ready and midnight ticks share one once-per-day slot
  ---
  duration_ms: 23.068629
  type: 'test'
  ...
# Subtest: decode maps ensure JSON and failure shapes
ok 1848 - decode maps ensure JSON and failure shapes
  ---
  duration_ms: 1.652345
  type: 'test'
  ...
# Subtest: older bob warns once per session and never notices
ok 1849 - older bob warns once per session and never notices
  ---
  duration_ms: 0.668286
  type: 'test'
  ...
# Subtest: lock_busy retries once, then surfaces the second outcome
ok 1850 - lock_busy retries once, then surfaces the second outcome
  ---
  duration_ms: 5.656724
  type: 'test'
  ...
# Subtest: other failures notice once per local day
ok 1851 - other failures notice once per local day
  ---
  duration_ms: 1.613943
  type: 'test'
  ...
# Subtest: open-this-weeks-note honors the gate and the missing note
ok 1852 - open-this-weeks-note honors the gate and the missing note
  ---
  duration_ms: 1.112966
  type: 'test'
  ...
# Subtest: setup registers the open-week command and teardown clears the retry timer
ok 1853 - setup registers the open-week command and teardown clears the retry timer
  ---
  duration_ms: 0.452194
  type: 'test'
  ...
# Subtest: period paths map to the date bob periods ensure -d needs
ok 1854 - period paths map to the date bob periods ensure -d needs
  ---
  duration_ms: 0.701811
  type: 'test'
  ...
# Subtest: unfilled period notes are blank or a frontmatter-only Templater stub
ok 1855 - unfilled period notes are blank or a frontmatter-only Templater stub
  ---
  duration_ms: 0.404352
  type: 'test'
  ...
# Subtest: a stubbed period note is filled once through ensure -d; bob scaffolds never cascade
ok 1856 - a stubbed period note is filled once through ensure -d; bob scaffolds never cascade
  ---
  duration_ms: 41.218915
  type: 'test'
  ...
# Subtest: api.periodNotes.ensureNote creates a missing period note through bob, never a template
ok 1857 - api.periodNotes.ensureNote creates a missing period note through bob, never a template
  ---
  duration_ms: 5.358785
  type: 'test'
  ...
# Subtest: the midnight ticker starts only on hosts that can register it
ok 1858 - the midnight ticker starts only on hosts that can register it
  ---
  duration_ms: 0.619764
  type: 'test'
  ...
# Subtest: quarter parts render week columns, month ticks, review marks, and future ghosts
ok 1859 - quarter parts render week columns, month ticks, review marks, and future ghosts
  ---
  duration_ms: 24.547943
  type: 'test'
  ...
# Subtest: year parts group 53 weeks by quarter and keep a four-quarter narrow fallback
ok 1860 - year parts group 53 weeks by quarter and keep a four-quarter narrow fallback
  ---
  duration_ms: 7.982317
  type: 'test'
  ...
# Subtest: all-time parts group quarters by year and keep year captions
ok 1861 - all-time parts group quarters by year and keep year captions
  ---
  duration_ms: 2.648869
  type: 'test'
  ...
# Subtest: parts table uses live internal links, Headline or mostly, review states, and day closeout rows
ok 1862 - parts table uses live internal links, Headline or mostly, review states, and day closeout rows
  ---
  duration_ms: 11.922272
  type: 'test'
  ...
# Subtest: table future rows stop at Child and Dates; not-tracked years and missing pre-adoption links are clear
ok 1863 - table future rows stop at Child and Dates; not-tracked years and missing pre-adoption links are clear
  ---
  duration_ms: 3.591049
  type: 'test'
  ...
# Subtest: shared report command remains keyed once by the period id
ok 1864 - shared report command remains keyed once by the period id
  ---
  duration_ms: 0.217676
  type: 'test'
  ...

