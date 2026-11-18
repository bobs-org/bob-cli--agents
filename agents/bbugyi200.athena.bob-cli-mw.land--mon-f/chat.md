# Chat History - ace-run (bob-cli-mw.land--mon-f)

- **TIMESTAMP:** 2026-11-18 05:51:26 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-mw.land--mon-f

## Prompt

sase monitor start --command 'NODE_OPTIONS=--require=/tmp/bob-cli-freeze-plugin-test-date.cjs sh /tmp/bob-cli-headline-gates.sh' --reason 'Repeat the daily headline gates after the plugin test run stalled without failures'

## Response

sase: running unwrapped (no profile (monitor.tool_wrap is verify))

> bob-plugins@0.1.0 test
> node scripts/build-plugins.mjs --check && npm run docs:inventory:check && { npm run test:unit; u=$?; npm run test:perf; p=$?; exit $((u||p)); }

  checked   block-id-prompt
  checked   bob-articles
  checked   bob-command-mode
  checked   bob-emoji
  checked   bob-ledger-tools
  checked   bob-mail
  checked   bob-navigation-hotkeys
  checked   task-status-cycler

> bob-plugins@0.1.0 docs:inventory:check
> node scripts/docs-inventory.mjs --check

Plugin documentation inventory is up to date.

> bob-plugins@0.1.0 test:unit
> node --test scripts/test-navigation-leaf-switch-guard.cjs scripts/test-project-tasks-snapshot.cjs scripts/test-bob-articles.cjs scripts/test-command-mode-resolver-env.cjs scripts/test-command-mode-catalog.cjs scripts/test-command-mode-runner.cjs scripts/test-command-mode-outcomes-api.cjs scripts/test-command-mode-pager.cjs scripts/test-command-mode-args-vim.cjs scripts/test-command-mode-sheet.cjs scripts/test-command-mode-album-schema-surface.cjs scripts/test-command-mode-sheet-keys.cjs scripts/test-command-mode-sheet-sequence.cjs scripts/test-command-mode-sheet-sequence-dom.cjs scripts/test-command-mode-status-chip.cjs scripts/test-command-mode-sequence-engine.cjs scripts/test-command-mode-sequence-feedback.cjs scripts/test-navigation-hotkeys-section-nav.cjs scripts/test-navigation-hotkeys-rename.cjs scripts/test-navigation-delete-guard.cjs scripts/test-navigation-copy-card-model.cjs scripts/test-navigation-copy-card-view.cjs scripts/test-navigation-hotkeys-ref-pdf.cjs scripts/test-navigation-hotkeys-ref-pdf-page.cjs scripts/test-navigation-ref-annotation-locator.cjs scripts/test-navigation-highlights-notice.cjs scripts/test-navigation-highlights-hints.cjs scripts/test-navigation-hotkeys-templater-trigger.cjs scripts/test-navigation-hotkeys-schedule-recovery.cjs scripts/test-navigation-hotkeys-schedule-properties.cjs scripts/test-navigation-hotkeys-schedule-writes.cjs scripts/test-navigation-hotkeys-runtime-schedule.cjs scripts/test-navigation-hotkeys-dependencies.cjs scripts/test-navigation-blocks-guards.cjs scripts/test-navigation-blocks-writers.cjs scripts/test-navigation-blocks-edit.cjs scripts/test-navigation-blocks-stage-view.cjs scripts/test-navigation-hotkeys-dependency-mirror.cjs scripts/test-navigation-hotkeys-task-move-plan.cjs scripts/test-navigation-hotkeys-priority-notice.cjs scripts/test-navigation-successor-picker.cjs scripts/test-navigation-successor-verdicts.cjs scripts/test-navigation-image-zoom-viewer.cjs scripts/test-navigation-video-zoom-viewer.cjs scripts/test-navigation-image-zoom-origin.cjs scripts/test-navigation-image-zoom-path.cjs scripts/test-navigation-hotkeys-unblocked-notice.cjs scripts/test-navigation-hotkeys-offer-close-apis.cjs scripts/test-navigation-project-blocking.cjs scripts/test-navigation-project-dependency-stage.cjs scripts/test-navigation-project-subprojects.cjs scripts/test-navigation-project-subtree-gestures.cjs scripts/test-navigation-hotkeys-priority-picker.cjs scripts/test-navigation-hotkeys-picker-lifecycle.cjs scripts/test-navigation-hotkeys-ref-picker-text.cjs scripts/test-navigation-hotkeys-pomodoro-move-pickers.cjs scripts/test-navigation-inbox-route.cjs scripts/test-navigation-inbox-route-card.cjs scripts/test-navigation-hotkeys-task-move.cjs scripts/test-navigation-open-notes-uri.cjs scripts/test-navigation-parent-change.cjs scripts/test-navigation-parent-album-record.cjs scripts/test-navigation-album-schema-fallback.cjs scripts/test-navigation-hotkeys-dash-open.cjs scripts/test-navigation-goto-task-uri.cjs scripts/test-navigation-hotkeys-open-task-jump.cjs scripts/test-navigation-hotkeys-vim-counts.cjs scripts/test-navigation-hotkeys-tab-pin.cjs scripts/test-navigation-hotkeys-schedule-log.cjs scripts/test-navigation-hotkeys-schedule-review.cjs scripts/test-navigation-hotkeys-deferred-pomodoro.cjs scripts/test-navigation-hotkeys-pomodoro-parse.cjs scripts/test-navigation-hotkeys-pomodoro-bullet-move.cjs scripts/test-navigation-hotkeys-pomodoro-split-rename.cjs scripts/test-navigation-hotkeys-pomodoro-split.cjs scripts/test-navigation-hotkeys-pomodoro-themes-manager.cjs scripts/test-navigation-hotkeys-pomodoro-reorder.cjs scripts/test-navigation-hotkeys-runtime-prune.cjs scripts/test-navigation-hotkeys-project-from-task.cjs scripts/test-navigation-hotkeys-project-reversal.cjs scripts/test-navigation-hotkeys-link-picker.cjs scripts/test-navigation-hotkeys-lane-toggle.cjs scripts/test-navigation-hotkeys-task-link-lane.cjs scripts/test-navigation-hotkeys-cancel-log.cjs scripts/test-navigation-hotkeys-cancel-task.cjs scripts/test-navigation-hotkeys-forward-promotion.cjs scripts/test-navigation-hotkeys-promotion-verdicts.cjs scripts/test-navigation-hotkeys-schedule-work-log.cjs scripts/test-navigation-hotkeys-work-log-stamp-closeout.cjs scripts/test-navigation-hotkeys-task-move-history.cjs scripts/test-navigation-jump-history.cjs scripts/test-navigation-dependencies.cjs scripts/test-navigation-editor-line-diff.cjs scripts/test-navigation-quick-roll.cjs scripts/test-navigation-quick-roll-preview.cjs scripts/test-navigation-roll-decay.cjs scripts/test-navigation-decay-planner.cjs scripts/test-navigation-task-card-model.cjs scripts/test-navigation-task-card-view.cjs scripts/test-navigation-task-card-theme-edit.cjs scripts/test-navigation-task-card-schedule.cjs scripts/test-navigation-task-card-review.cjs scripts/test-navigation-decision-card.cjs scripts/test-navigation-decision-card-handlers.cjs scripts/test-navigation-decision-card-keep.cjs scripts/test-navigation-refresh-modal.cjs scripts/test-navigation-freshness.cjs scripts/test-navigation-review-groups.cjs scripts/test-navigation-stamps.cjs scripts/test-navigation-keep-counting.cjs scripts/test-navigation-rotten-keep.cjs scripts/test-navigation-rotten-log.cjs scripts/test-navigation-checklist.cjs scripts/test-navigation-review-advance.cjs scripts/test-navigation-review-advance-gestures.cjs scripts/test-navigation-checklist-ctrl-enter.cjs scripts/test-ledger-tools-navigation.cjs scripts/test-ledger-tools-plan-budget.cjs scripts/test-ledger-tools-plan-budget-off-clock.cjs scripts/test-ledger-tools-plan-today-roots.cjs scripts/test-ledger-tools-ready-badge.cjs scripts/test-ledger-tools-note-ready.cjs scripts/test-ledger-tools-note-ready-views.cjs scripts/test-ledger-tools-dashboard-parity.cjs scripts/test-ledger-tools-work-badge-tone.cjs scripts/test-ledger-tools-dashboard-collections.cjs scripts/test-ledger-tools-today.cjs scripts/test-ledger-tools-period-notes.cjs scripts/test-ledger-tools-gcal-events.cjs scripts/test-ledger-tools-event-link-times.cjs scripts/test-ledger-tools-meet-event-run.cjs scripts/test-ledger-tools-pomodoro-clock.cjs scripts/test-ledger-tools-freshness-placement.cjs scripts/test-ledger-tools-freshness-states.cjs scripts/test-ledger-tools-freshness-namespace.cjs scripts/test-ledger-tools-freshness-review-model.cjs scripts/test-ledger-tools-freshness-queue.cjs scripts/test-ledger-tools-freshness-stages.cjs scripts/test-ledger-tools-freshness-tracking.cjs scripts/test-ledger-tools-freshness-footer.cjs scripts/test-ledger-tools-walker-footer.cjs scripts/test-ledger-tools-keep-inbox.cjs scripts/test-ledger-tools-freshness-recurring.cjs scripts/test-ledger-tools-freshness-mark.cjs scripts/test-ledger-tools-freshness-mark-surfaces.cjs scripts/test-ledger-tools-priority-marks.cjs scripts/test-ledger-tools-block-marks.cjs scripts/test-ledger-tools-block-marks-contrast.cjs scripts/test-ledger-tools-block-marks-editor.cjs scripts/test-ledger-tools-block-marks-reading.cjs scripts/test-ledger-tools-mail-link-marks.cjs scripts/test-ledger-tools-no-reply-pills.cjs scripts/test-ledger-tools-task-tag-marks.cjs scripts/test-ledger-tools-task-link-marks.cjs scripts/test-ledger-tools-task-link-marks-live.cjs scripts/test-ledger-tools-task-link-marks-reading.cjs scripts/test-ledger-tools-task-type-identity.cjs scripts/test-ledger-tools-today-marks.cjs scripts/test-ledger-tools-today-marks-reading.cjs scripts/test-ledger-tools-unblocked-glyph.cjs scripts/test-ledger-tools-frees-marks.cjs scripts/test-ledger-tools-off-clock-link-chips.cjs scripts/test-ledger-tools-progress-marks.cjs scripts/test-ledger-tools-keep-moving-marks.cjs scripts/test-ledger-tools-keep-moving-render.cjs scripts/test-ledger-tools-keep-moving-marks-surface.cjs scripts/test-ledger-tools-date-marks.cjs scripts/test-ledger-tools-recurrence-marks.cjs scripts/test-ledger-tools-date-marks-tasks.cjs scripts/test-ledger-tools-freshness-keeps.cjs scripts/test-ledger-tools-freshness-unblocked.cjs scripts/test-ledger-tools-freshness-decision-card.cjs scripts/test-ledger-tools-dependency-chips.cjs scripts/test-ledger-tools-blocks-chips.cjs scripts/test-ledger-tools-command-mode-refresh.cjs scripts/test-ledger-tools-snippets.cjs scripts/test-ledger-tools-vim-mappings.cjs scripts/test-task-status-cycler-dependencies.cjs scripts/test-task-status-cycler-blocks-guards.cjs scripts/test-task-status-cycler-complete-vectors.cjs scripts/test-task-status-cycler-bank-guard.cjs scripts/test-task-status-cycler-ctrl-enter.cjs scripts/test-task-status-cycler-event-task-close.cjs scripts/test-task-status-cycler-reference-lifecycle.cjs scripts/test-task-status-cycler-pomodoro-completion.cjs scripts/test-task-status-cycler-pomodoro-clock.cjs scripts/test-task-status-cycler-pomodoro-work-log.cjs scripts/test-task-status-cycler-pomodoro-reopen.cjs scripts/test-task-status-cycler-blocked-schedule.cjs scripts/test-task-status-cycler-demotion-picker.cjs scripts/test-task-status-cycler-event-ledger-guard.cjs scripts/test-task-status-cycler-promotion.cjs scripts/test-task-status-cycler-promotion-verdicts.cjs scripts/test-task-status-cycler-counted-toggle.cjs scripts/test-task-status-cycler-successors.cjs scripts/test-task-status-cycler-successor-wiring.cjs scripts/test-task-status-cycler-successor-polish.cjs scripts/test-task-status-cycler-keep-moving.cjs scripts/test-keep-moving-marks-parity.cjs scripts/test-task-status-cycler-relation-successors.cjs scripts/test-task-status-cycler-parked-successors.cjs scripts/test-task-status-cycler-successor-offers.cjs scripts/test-task-status-cycler-successor-verdicts.cjs scripts/test-task-status-cycler-successor-apply.cjs scripts/test-task-status-cycler-successor-theme-write.cjs scripts/test-task-status-cycler-project-catalog.cjs scripts/test-task-status-cycler-project-pull-in.cjs scripts/test-task-status-cycler-task-links-api.cjs scripts/test-task-status-cycler-closed-pomodoro-links.cjs scripts/test-task-status-cycler-task-link-lane.cjs scripts/test-task-status-cycler-freshness.cjs scripts/test-block-id-prompt-dependencies.cjs scripts/test-block-id-prompt-blocks-guards.cjs scripts/test-block-id-prompt-ref-picker-text.cjs scripts/test-block-id-prompt-markers.cjs scripts/test-block-id-prompt-pomodoro-context.cjs scripts/test-block-id-prompt-target-update.cjs scripts/test-block-id-prompt-pomodoro-insertion.cjs scripts/test-block-id-prompt-pomodoro-targets.cjs scripts/test-block-id-prompt-pomodoro-picker-view.cjs scripts/test-block-id-prompt-pomodoro-picker-runtime.cjs scripts/test-block-id-prompt-work-log.cjs scripts/test-block-id-prompt-pomodoro-link-runtime.cjs scripts/test-block-id-prompt-pomodoro-theme-write.cjs scripts/test-block-id-prompt-pomodoro-link-picker-api.cjs scripts/test-block-id-prompt-pomodoro-unlink-runtime.cjs scripts/test-block-id-prompt-parked-successors.cjs scripts/test-block-id-prompt-task-link-deletion.cjs scripts/test-block-id-prompt-task-wikilink-model.cjs scripts/test-block-id-prompt-task-wikilink-token.cjs scripts/test-block-id-prompt-task-wikilink-index.cjs scripts/test-block-id-prompt-task-wikilink-picker-view.cjs scripts/test-block-id-prompt-task-wikilink-picker-runtime.cjs scripts/test-block-id-prompt-task-wikilink-naming.cjs scripts/test-block-id-prompt-task-wikilink-pomodoro.cjs scripts/test-block-id-prompt-plan-budget-and-freshness.cjs scripts/test-prompt-block-id-naming.cjs scripts/test-block-id-prompt-prefill.cjs scripts/test-block-id-prompt-rename-atomic.cjs scripts/test-vim-surround.cjs scripts/test-vim-yank-flash.cjs scripts/test-navigation-dependencies-stage-ranker-and-pool.cjs scripts/test-navigation-dependencies-stage-entry-and-view.cjs scripts/test-navigation-dependencies-stage-writes.cjs scripts/test-navigation-dependencies-stage-mirror-and-badge.cjs scripts/test-navigation-dependencies-stage-stale-guards.cjs scripts/test-navigation-dependencies-stage-performance.cjs scripts/test-navigation-prompt-block-id-stage.cjs scripts/test-navigation-dependencies-writer.cjs scripts/test-navigation-dependency-link-consumption.cjs scripts/test-plugin-build.cjs scripts/test-ledger-tools-stats-journal.cjs scripts/test-ledger-tools-stats-clocks.cjs scripts/test-ledger-tools-stats-data.cjs scripts/test-ledger-tools-stats-block.cjs scripts/test-ledger-tools-stats-charts.cjs scripts/test-ledger-tools-stats-clock-charts.cjs scripts/test-navigation-review-journal.cjs scripts/test-ledger-tools-stats-panels.cjs scripts/test-ledger-tools-stats-lanes.cjs scripts/test-ledger-tools-reading-board-data.cjs scripts/test-ledger-tools-notebooks-data.cjs scripts/test-ledger-tools-albums-data.cjs scripts/test-ledger-tools-areas-data.cjs scripts/test-ledger-tools-areas-catalog.cjs scripts/test-ledger-tools-projects-data.cjs scripts/test-ledger-tools-projects-catalog.cjs scripts/test-ledger-tools-album-update.cjs scripts/test-ledger-tools-bank-config-update.cjs scripts/test-ledger-tools-bank-decode.cjs scripts/test-ledger-tools-bank-period-model.cjs scripts/test-ledger-tools-bank-period-paint.cjs scripts/test-ledger-tools-bank-period-balance.cjs scripts/test-ledger-tools-bank-source.cjs scripts/test-ledger-tools-bank-data.cjs scripts/test-ledger-tools-bank-actions.cjs scripts/test-ledger-tools-bank-category-card.cjs scripts/test-ledger-tools-bank-walk.cjs scripts/test-ledger-tools-bank-walk-index.cjs scripts/test-ledger-tools-bank-category-card-ui.cjs scripts/test-ledger-tools-bank-emoji-slot.cjs scripts/test-ledger-tools-notebook-catalog.cjs scripts/test-ledger-tools-notebook-header.cjs scripts/test-ledger-tools-reading-board-models.cjs scripts/test-ledger-tools-reading-board-block.cjs scripts/test-ledger-tools-pomodoro-home-chips.cjs scripts/test-ledger-tools-pomodoro-themes.cjs scripts/test-ledger-tools-task-theme-marks.cjs scripts/test-ledger-tools-task-theme-rendered.cjs scripts/test-navigation-image-zoom-target.cjs scripts/test-navigation-image-zoom-command.cjs scripts/test-done-archive-path.cjs scripts/test-navigation-relation-lines.cjs scripts/test-navigation-relation-mentions.cjs scripts/test-navigation-relation-writer.cjs scripts/test-navigation-task-cancel-vectors.cjs scripts/test-navigation-task-split-vectors.cjs scripts/test-navigation-window-tab-numbers.cjs scripts/test-navigation-window-tab-model.cjs scripts/test-navigation-window-tab-actions.cjs scripts/test-navigation-window-prefix-model.cjs scripts/test-navigation-window-prefix-actions.cjs scripts/test-navigation-window-hint-view.cjs scripts/test-navigation-window-prefix-commands.cjs scripts/test-navigation-window-prefix.cjs scripts/test-navigation-task-split-gesture.cjs scripts/test-navigation-relation-cancel-writer.cjs scripts/test-navigation-relation-complete-writer.cjs scripts/test-navigation-relation-complete-vectors.cjs scripts/test-navigation-relation-links-stage.cjs scripts/test-navigation-relation-merge.cjs scripts/test-navigation-relation-successor-vectors.cjs scripts/test-navigation-relation-stage-render.cjs scripts/test-relation-index-linked-from-stage.cjs scripts/test-ledger-tools-relations.cjs scripts/test-ledger-tools-task-merge.cjs scripts/test-ledger-tools-notebooks-api.cjs scripts/test-navigation-notebook-gestures.cjs scripts/test-ledger-tools-relation-index.cjs scripts/test-ledger-tools-attachments-api.cjs scripts/test-ledger-tools-relation-mentions.cjs scripts/test-ledger-tools-relation-chips.cjs scripts/test-task-status-cycler-relations.cjs scripts/test-task-status-cycler-restore.cjs scripts/test-block-id-prompt-relations.cjs scripts/test-ledger-tools-day-strip.cjs scripts/test-ledger-tools-day-strip-themes.cjs scripts/test-ledger-tools-day-strip-plan-host.cjs scripts/test-ledger-tools-period-strip.cjs scripts/test-ledger-tools-period-strip-charts.cjs scripts/test-ledger-tools-period-parts.cjs scripts/test-ledger-tools-fakenode-inspect.cjs scripts/test-ledger-tools-day-strip-lanes.cjs scripts/test-ledger-tools-day-strip-hosts.cjs scripts/test-obsidian-startup-smoke.cjs scripts/test-obsidian-bank-ui-e2e.cjs scripts/test-obsidian-bank-ui-e2e-setup.cjs scripts/test-obsidian-album-ui-e2e.cjs scripts/test-obsidian-album-schema-writer-e2e.cjs scripts/test-obsidian-record-writer-e2e.cjs scripts/test-obsidian-notebook-ui-e2e.cjs scripts/test-obsidian-projects-ui-e2e.cjs scripts/test-obsidian-task-wikilink-e2e.cjs scripts/test-obsidian-block-id-rename-e2e.cjs scripts/test-obsidian-task-link-marks-e2e.cjs scripts/test-obsidian-block-marks-e2e.cjs scripts/test-obsidian-frees-marks-e2e.cjs scripts/test-obsidian-keep-moving-marks-e2e.cjs scripts/test-obsidian-off-clock-link-chips-e2e.cjs scripts/test-obsidian-event-link-times-e2e.cjs scripts/test-obsidian-decay-ladder-e2e.cjs scripts/test-obsidian-quick-roll-e2e.cjs scripts/test-task-link-marks-motion.cjs scripts/test-ledger-tools-lane-walk.cjs scripts/test-navigation-bank-walk.cjs scripts/test-navigation-lane-walk.cjs scripts/test-ledger-tools-root-marks.cjs scripts/test-navigation-bracket-repeat.cjs scripts/test-navigation-period-links.cjs scripts/test-navigation-bracket-mode-indicator.cjs scripts/test-navigation-lane-inbox-route.cjs scripts/test-navigation-review-due-row.cjs scripts/test-bob-mail.cjs scripts/test-bob-mail-compose.cjs scripts/test-bob-mail-archive-banner.cjs scripts/test-navigation-reload-history.cjs scripts/test-obsidian-video-zoom-e2e.cjs scripts/test-obsidian-redo-history-e2e.cjs scripts/test-obsidian-closed-pomodoro-link-e2e.cjs scripts/test-obsidian-command-mode-tab-e2e.cjs scripts/test-obsidian-walker-footer-e2e.cjs scripts/test-obsidian-vim-yank-flash-e2e.cjs scripts/test-obsidian-copy-card-e2e.cjs scripts/test-obsidian-window-prefix-e2e.cjs scripts/test-ledger-tools-bank-cards.cjs scripts/test-ledger-tools-bank-badge-hosts.cjs scripts/test-ledger-tools-bank-setup.cjs scripts/test-ledger-tools-bank-setup-group-jump.cjs scripts/test-ledger-tools-bank-setup-arrange.cjs scripts/test-ledger-tools-schema-arrange.cjs scripts/test-ledger-tools-bank-marks.cjs scripts/test-ledger-tools-bank-subscription.cjs scripts/test-ledger-tools-bank-subscription-surfaces.cjs scripts/test-ledger-tools-bank-subscription-linker.cjs scripts/test-ledger-tools-album-catalog.cjs scripts/test-ledger-tools-album-records.cjs scripts/test-ledger-tools-album-header.cjs scripts/test-ledger-tools-record-sheet.cjs scripts/test-ledger-tools-record-update.cjs scripts/test-ledger-tools-record-card.cjs scripts/test-ledger-tools-album-schema-card-shell.cjs scripts/test-ledger-tools-album-schema-arrange-card.cjs scripts/test-ledger-tools-album-schema-field-jump.cjs scripts/test-ledger-tools-album-schema-place-drag.cjs scripts/test-ledger-tools-album-entrypoints.cjs scripts/test-ledger-tools-schema-double-equals.cjs scripts/test-ledger-tools-album-yaml-excursion.cjs scripts/test-bob-emoji-model.cjs scripts/test-bob-emoji-trigger.cjs scripts/test-bob-emoji-suggest.cjs scripts/test-bob-emoji-catalog.cjs scripts/test-bob-emoji-api.cjs scripts/test-ledger-tools-bank-period-hosts.cjs scripts/test-command-mode-bank-setup-surface.cjs

TAP version 13
# Subtest: bip BK1–BK12 accept and empty
ok 1 - bip BK1–BK12 accept and empty
  ---
  duration_ms: 1.260176
  ...
# Subtest: bip BK13–BK15 malformed split mirrors the Depends-On twin
ok 2 - bip BK13–BK15 malformed split mirrors the Depends-On twin
  ---
  duration_ms: 0.356581
  ...
# Subtest: bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
ok 3 - bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
  ---
  duration_ms: 0.118927
  ...
# Subtest: bip MC1/MC2 Pomodoro scanners skip managed lines
ok 4 - bip MC1/MC2 Pomodoro scanners skip managed lines
  ---
  duration_ms: 1.961044
  ...
# Subtest: explicit task IDs exclusively own dependency lookup
ok 5 - explicit task IDs exclusively own dependency lookup
  ---
  duration_ms: 3.43053
  ...
# Subtest: legacy tasks without an id field still fall back to their block ID
ok 6 - legacy tasks without an id field still fall back to their block ID
  ---
  duration_ms: 0.286668
  ...
# Subtest: blocked-link consumption raises open prerequisites and leaves the dependent blocked
ok 7 - blocked-link consumption raises open prerequisites and leaves the dependent blocked
  ---
  duration_ms: 1.017273
  ...
# Subtest: project-blocked member consumption promotes the project's open prerequisite
ok 8 - project-blocked member consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.64921
  ...
# Subtest: project-blocked resident consumption promotes the project's open prerequisite
ok 9 - project-blocked resident consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.360528
  ...
# Subtest: a tagged inherited ^prj target is refused with its parent named
ok 10 - a tagged inherited ^prj target is refused with its parent named
  ---
  duration_ms: 0.353535
  ...
# Subtest: project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
ok 11 - project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
  ---
  duration_ms: 0.677344
  ...
# Subtest: project date refusal applies only when the date is the sole project reason
ok 12 - project date refusal applies only when the date is the sole project reason
  ---
  duration_ms: 0.263373
  ...
# Subtest: a project-blocked tag is token-bounded and ignored on lookalike tags
ok 13 - a project-blocked tag is token-bounded and ignored on lookalike tags
  ---
  duration_ms: 0.380667
  ...
# Subtest: task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
ok 14 - task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
  ---
  duration_ms: 0.628209
  ...
# Subtest: task blocked state unifies status and dependency reasons
ok 15 - task blocked state unifies status and dependency reasons
  ---
  duration_ms: 0.316023
  ...
# Subtest: task picker partition sinks blocked tasks while preserving group order
ok 16 - task picker partition sinks blocked tasks while preserving group order
  ---
  duration_ms: 0.195383
  ...
# Subtest: blocked chip labels show useful unmet dependency counts
ok 17 - blocked chip labels show useful unmet dependency counts
  ---
  duration_ms: 0.108968
  ...
# Subtest: blocked tooltips explain dependency and status-only reasons
ok 18 - blocked tooltips explain dependency and status-only reasons
  ---
  duration_ms: 0.212877
  ...
# Subtest: task status classes cover every open task status
ok 19 - task status classes cover every open task status
  ---
  duration_ms: 0.08358
  ...
# Subtest: Blocked tasks remain unmet dependency targets
ok 20 - Blocked tasks remain unmet dependency targets
  ---
  duration_ms: 0.130079
  ...
# Subtest: blocked task count covers both reasons without double-counting
ok 21 - blocked task count covers both reasons without double-counting
  ---
  duration_ms: 0.110451
  ...
# Subtest: single caret relocation preserves embedding and removes aliases
ok 22 - single caret relocation preserves embedding and removes aliases
  ---
  duration_ms: 1.642176
  ...
# Subtest: single caret relocation resets aliased block links
ok 23 - single caret relocation resets aliased block links
  ---
  duration_ms: 0.24053
  ...
# Subtest: single caret relocation strips heading and block subpaths
ok 24 - single caret relocation strips heading and block subpaths
  ---
  duration_ms: 0.30897
  ...
# Subtest: task picker normalizes every supported wiki block-link form
ok 25 - task picker normalizes every supported wiki block-link form
  ---
  duration_ms: 0.819254
  ...
# Subtest: three or more carets never trigger the task picker
ok 26 - three or more carets never trigger the task picker
  ---
  duration_ms: 0.193199
  ...
# Subtest: rapid aliased task picker completion preserves the alias
ok 27 - rapid aliased task picker completion preserves the alias
  ---
  duration_ms: 3.26831
  ...
# Subtest: task picker recognition is independent of Markdown source context
ok 28 - task picker recognition is independent of Markdown source context
  ---
  duration_ms: 0.746375
  ...
# Subtest: task picker recognition respects cursor proximity and fenced code
ok 29 - task picker recognition respects cursor proximity and fenced code
  ---
  duration_ms: 0.237394
  ...
# Subtest: SA33 settled Unlink task prompt offers parked successors with the removed slot
ok 30 - SA33 settled Unlink task prompt offers parked successors with the removed slot
  ---
  duration_ms: 6.414096
  ...
# Subtest: SA33 Esc on Unlink task offers nothing
ok 31 - SA33 Esc on Unlink task offers nothing
  ---
  duration_ms: 0.380867
  ...
# Subtest: non-Pending unlink stays silent even with a live cycler
ok 32 - non-Pending unlink stays silent even with a live cycler
  ---
  duration_ms: 0.526435
  ...
# Subtest: older cycler api v3 is silence
ok 33 - older cycler api v3 is silence
  ---
  duration_ms: 0.453887
  ...
# Subtest: In Progress unlink with no removed links does not offer
ok 34 - In Progress unlink with no removed links does not offer
  ---
  duration_ms: 0.323928
  ...
# Subtest: Task Link Unlink of a Pending target offers parked successors
ok 35 - Task Link Unlink of a Pending target offers parked successors
  ---
  duration_ms: 2.256197
  ...
# Subtest: plan budget suffix: link Notice appends the meter computed on post-write daily content
ok 36 - plan budget suffix: link Notice appends the meter computed on post-write daily content
  ---
  duration_ms: 7.67357
  ...
# Subtest: plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
ok 37 - plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
  ---
  duration_ms: 0.931538
  ...
# Subtest: plan budget suffix: unlink Notice marks an over-cap plan with 🔴
ok 38 - plan budget suffix: unlink Notice marks an over-cap plan with 🔴
  ---
  duration_ms: 2.162027
  ...
# Subtest: plan budget suffix: Next task without a block ID prompts for one and omits the meter
ok 39 - plan budget suffix: Next task without a block ID prompts for one and omits the meter
  ---
  duration_ms: 0.339338
  ...
# Subtest: plan budget suffix: Task Link Notice appends the meter from post-write daily content
ok 40 - plan budget suffix: Task Link Notice appends the meter from post-write daily content
  ---
  duration_ms: 2.216632
  ...
# Subtest: plan budget suffix: Task Link Notice omits the meter when no daily note takes part
ok 41 - plan budget suffix: Task Link Notice omits the meter when no daily note takes part
  ---
  duration_ms: 0.492941
  ...
# Subtest: planTargetTaskUpdate stamps the rewritten line last via injected stamper
ok 42 - planTargetTaskUpdate stamps the rewritten line last via injected stamper
  ---
  duration_ms: 0.368022
  ...
# Subtest: planTargetTaskUpdate without a stamper never stamps (identity default)
ok 43 - planTargetTaskUpdate without a stamper never stamps (identity default)
  ---
  duration_ms: 0.131772
  ...
# Subtest: planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
ok 44 - planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
  ---
  duration_ms: 0.317556
  ...
# Subtest: planTargetTaskUpdate stamps a Next task that gains a block ID
ok 45 - planTargetTaskUpdate stamps a Next task that gains a block ID
  ---
  duration_ms: 0.51321
  ...
# Subtest: planTargetTaskUpdate tolerates a throwing stamper
ok 46 - planTargetTaskUpdate tolerates a throwing stamper
  ---
  duration_ms: 0.22517
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 47 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.460419
  ...
# Subtest: dedicated-link helpers reject Depends-On lines
ok 48 - dedicated-link helpers reject Depends-On lines
  ---
  duration_ms: 0.321033
  ...
# Subtest: Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
ok 49 - Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
  ---
  duration_ms: 0.386819
  ...
# Subtest: malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
ok 50 - malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
  ---
  duration_ms: 0.122283
  ...
# Subtest: Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
ok 51 - Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
  ---
  duration_ms: 0.270697
  ...
# Subtest: Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
ok 52 - Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
  ---
  duration_ms: 0.20954
  ...
# Subtest: readPlanBudgetMeter ignores stale theme meters and follows links only
ok 53 - readPlanBudgetMeter ignores stale theme meters and follows links only
  ---
  duration_ms: 0.18844
  ...
# Subtest: readPlanBudgetMeter marks an over-link plan red
ok 54 - readPlanBudgetMeter marks an over-link plan red
  ---
  duration_ms: 0.103928
  ...
# Subtest: block-id-prompt freshness accessors degrade without ledger-tools
ok 55 - block-id-prompt freshness accessors degrade without ledger-tools
  ---
  duration_ms: 0.206755
  ...
# Subtest: block-id-prompt refuses Pomodoro ledger lines before calling a stamper
ok 56 - block-id-prompt refuses Pomodoro ledger lines before calling a stamper
  ---
  duration_ms: 0.189813
  ...
# Subtest: list item body bounds trim whitespace and reject empty bullets
ok 57 - list item body bounds trim whitespace and reject empty bullets
  ---
  duration_ms: 2.120708
  ...
# Subtest: Pomodoro activation eligibility requires a sole-content sub-bullet
ok 58 - Pomodoro activation eligibility requires a sole-content sub-bullet
  ---
  duration_ms: 1.979449
  ...
# Subtest: Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
ok 59 - Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
  ---
  duration_ms: 0.252983
  ...
# Subtest: Pomodoro source context distinguishes ledger ancestry and open state
ok 60 - Pomodoro source context distinguishes ledger ancestry and open state
  ---
  duration_ms: 0.430211
  ...
# Subtest: the open-Pomodoro task-link gate recognizes both ^^ and (( sources
ok 61 - the open-Pomodoro task-link gate recognizes both ^^ and (( sources
  ---
  duration_ms: 1.612218
  ...
# Subtest: future cleanup touches only later open Pomodoros and counts duplicates
ok 62 - future cleanup touches only later open Pomodoros and counts duplicates
  ---
  duration_ms: 1.666641
  ...
# Subtest: cleanup resolves aliases, embeds, same-note links, and alternate paths
ok 63 - cleanup resolves aliases, embeds, same-note links, and alternate paths
  ---
  duration_ms: 0.672003
  ...
# Subtest: dedicated bullet subtree cleanup preserves CRLF line endings
ok 64 - dedicated bullet subtree cleanup preserves CRLF line endings
  ---
  duration_ms: 0.308229
  ...
# Subtest: existing-ID task completion prunes future links in the source editor
ok 65 - existing-ID task completion prunes future links in the source editor
  ---
  duration_ms: 3.005408
  ...
# Subtest: new-ID same-file completion plans cleanup after the task edit
ok 66 - new-ID same-file completion plans cleanup after the task edit
  ---
  duration_ms: 1.415963
  ...
# Subtest: findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
ok 67 - findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
  ---
  duration_ms: 2.256148
  ...
# Subtest: findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
ok 68 - findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
  ---
  duration_ms: 0.177478
  ...
# Subtest: findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
ok 69 - findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
  ---
  duration_ms: 0.185674
  ...
# Subtest: todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
ok 70 - todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
  ---
  duration_ms: 0.447354
  ...
# Subtest: todayDailyPath honors a custom Daily Notes format and an empty folder
ok 71 - todayDailyPath honors a custom Daily Notes format and an empty folder
  ---
  duration_ms: 0.222384
  ...
# Subtest: formatDailyDate resolves bracketed literal text alongside date tokens
ok 72 - formatDailyDate resolves bracketed literal text alongside date tokens
  ---
  duration_ms: 0.121603
  ...
# Subtest: getDailyNotesOptions reads the daily-notes core plugin's configured options
ok 73 - getDailyNotesOptions reads the daily-notes core plugin's configured options
  ---
  duration_ms: 0.664339
  ...
# Subtest: computeFencedLineFlags marks opening and closing fence lines and everything between
ok 74 - computeFencedLineFlags marks opening and closing fence lines and everything between
  ---
  duration_ms: 0.238416
  ...
# Subtest: selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
ok 75 - selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
  ---
  duration_ms: 0.697712
  ...
# Subtest: selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
ok 76 - selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
  ---
  duration_ms: 0.468734
  ...
# Subtest: selectPomodoroInsertionTarget rejects more than one open timed entry
ok 77 - selectPomodoroInsertionTarget rejects more than one open timed entry
  ---
  duration_ms: 0.220862
  ...
# Subtest: selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
ok 78 - selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
  ---
  duration_ms: 0.190143
  ...
# Subtest: findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
ok 79 - findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
  ---
  duration_ms: 0.168221
  ...
# Subtest: planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
ok 80 - planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
  ---
  duration_ms: 1.150857
  ...
# Subtest: planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
ok 81 - planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
  ---
  duration_ms: 1.438857
  ...
# Subtest: planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
ok 82 - planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
  ---
  duration_ms: 0.249577
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
ok 83 - planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
  ---
  duration_ms: 0.463676
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
ok 84 - planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
  ---
  duration_ms: 0.508049
  ...
# Subtest: planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
ok 85 - planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
  ---
  duration_ms: 0.341742
  ...
# Subtest: planPomodoroLinkInsertion inserts before the separator preceding later content
ok 86 - planPomodoroLinkInsertion inserts before the separator preceding later content
  ---
  duration_ms: 0.263193
  ...
# Subtest: planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
ok 87 - planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
  ---
  duration_ms: 0.310873
  ...
# Subtest: planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
ok 88 - planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
  ---
  duration_ms: 0.399332
  ...
# Subtest: existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
ok 89 - existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
  ---
  duration_ms: 3.676208
  ...
# Subtest: same-note Pomodoro link runtime composes the task update with adjacent insertion
ok 90 - same-note Pomodoro link runtime composes the task update with adjacent insertion
  ---
  duration_ms: 1.194651
  ...
# Subtest: new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
ok 91 - new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
  ---
  duration_ms: 0.632627
  ...
# Subtest: planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
ok 92 - planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
  ---
  duration_ms: 0.31429
  ...
# Subtest: all-open cleanup removes current and future links while preserving history and unresolved links
ok 93 - all-open cleanup removes current and future links while preserving history and unresolved links
  ---
  duration_ms: 0.925717
  ...
# Subtest: all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
ok 94 - all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
  ---
  duration_ms: 1.092777
  ...
# Subtest: all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
ok 95 - all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
  ---
  duration_ms: 0.238505
  ...
# Subtest: all-open cleanup treats missing section, no open entries, and no matches as no-op successes
ok 96 - all-open cleanup treats missing section, no open entries, and no matches as no-op successes
  ---
  duration_ms: 0.227976
  ...
# Subtest: composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
ok 97 - composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
  ---
  duration_ms: 0.220932
  ...
# Subtest: pomodoro link picker choices normalize to existing/new or null
ok 98 - pomodoro link picker choices normalize to existing/new or null
  ---
  duration_ms: 1.983387
  ...
# Subtest: pomodoroLinkPicker api never rejects and validates choices
ok 99 - pomodoroLinkPicker api never rejects and validates choices
  ---
  duration_ms: 0.401777
  ...
# Subtest: destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
ok 100 - destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
  ---
  duration_ms: 0.62354
  ...
# Subtest: destination pick with a section releases its guards when the modal cannot open
ok 101 - destination pick with a section releases its guards when the modal cannot open
  ---
  duration_ms: 1.688283
  ...
# Subtest: public pick accepts one-based full-note task context and suggests once
ok 102 - public pick accepts one-based full-note task context and suggests once
  ---
  duration_ms: 1.492679
  ...
# Subtest: public pick without task context stays generic; missing themes degrades safely
ok 103 - public pick without task context stays generic; missing themes degrades safely
  ---
  duration_ms: 0.600557
  ...
# Subtest: plugin lifecycle installs the api and drops it on unload
ok 104 - plugin lifecycle installs the api and drops it on unload
  ---
  duration_ms: 0.606558
  ...
# Subtest: task-aware choices retain a valid themeIntent; absent intent keeps the legacy shape
ok 105 - task-aware choices retain a valid themeIntent; absent intent keeps the legacy shape
  ---
  duration_ms: 0.286737
  ...
# Subtest: malformed themeIntent is dropped so it can never enable a write
ok 106 - malformed themeIntent is dropped so it can never enable a write
  ---
  duration_ms: 0.461711
  ...
# Subtest: taskLineTextAt reads one-based lines and degrades to empty
ok 107 - taskLineTextAt reads one-based lines and degrades to empty
  ---
  duration_ms: 0.363534
  ...
# Subtest: public pick tolerates an out-of-range task line and releases its guards
ok 108 - public pick tolerates an out-of-range task line and releases its guards
  ---
  duration_ms: 0.456592
  ...
# Subtest: Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
ok 109 - Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
  ---
  duration_ms: 2.196633
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor requires a single cursor
ok 110 - resolvePomodoroLinkTaskFromEditor requires a single cursor
  ---
  duration_ms: 0.328257
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
ok 111 - resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
  ---
  duration_ms: 0.452875
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
ok 112 - resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
  ---
  duration_ms: 0.423839
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
ok 113 - resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
  ---
  duration_ms: 0.657115
  ...
# Subtest: blocked-link consumption reports dependency reasons before the project date
ok 114 - blocked-link consumption reports dependency reasons before the project date
  ---
  duration_ms: 2.45683
  ...
# Subtest: Pomodoro link checks do not read other notes for a non-Blocked task
ok 115 - Pomodoro link checks do not read other notes for a non-Blocked task
  ---
  duration_ms: 0.303729
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
ok 116 - resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
  ---
  duration_ms: 0.401907
  ...
# Subtest: task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
ok 117 - task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
  ---
  duration_ms: 7.01864
  ...
# Subtest: task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
ok 118 - task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
  ---
  duration_ms: 2.683775
  ...
# Subtest: task-mode toggle: linked only under a completed Pomodoro links again
ok 119 - task-mode toggle: linked only under a completed Pomodoro links again
  ---
  duration_ms: 0.85902
  ...
# Subtest: task-mode toggle: a task without a block ID is never linked and prompts for one
ok 120 - task-mode toggle: a task without a block ID is never linked and prompts for one
  ---
  duration_ms: 0.431134
  ...
# Subtest: existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
ok 121 - existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
  ---
  duration_ms: 1.156919
  ...
# Subtest: forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
ok 122 - forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
  ---
  duration_ms: 0.574046
  ...
# Subtest: new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
ok 123 - new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
  ---
  duration_ms: 0.535893
  ...
# Subtest: submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
ok 124 - submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
  ---
  duration_ms: 0.135419
  ...
# Subtest: submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
ok 125 - submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
  ---
  duration_ms: 0.142411
  ...
# Subtest: same-note Pomodoro link runtime: task and ledger edits merge into one transaction
ok 126 - same-note Pomodoro link runtime: task and ledger edits merge into one transaction
  ---
  duration_ms: 1.165855
  ...
# Subtest: linking an already-linked Ready task raises it to Next without duplicating the link
ok 127 - linking an already-linked Ready task raises it to Next without duplicating the link
  ---
  duration_ms: 0.493091
  ...
# Subtest: Next task without a block ID preflights the picker before prompting
ok 128 - Next task without a block ID preflights the picker before prompting
  ---
  duration_ms: 0.442906
  ...
# Subtest: Pomodoro link stops before any mutation when today's daily note is missing
ok 129 - Pomodoro link stops before any mutation when today's daily note is missing
  ---
  duration_ms: 0.162119
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
ok 130 - Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
  ---
  duration_ms: 0.444087
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
ok 131 - Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
  ---
  duration_ms: 0.282599
  ...
# Subtest: Pomodoro link aborts without any write when the task line changed since it was selected
ok 132 - Pomodoro link aborts without any write when the task line changed since it was selected
  ---
  duration_ms: 0.146209
  ...
# Subtest: Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
ok 133 - Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
  ---
  duration_ms: 0.674297
  ...
# Subtest: canceling the Pomodoro block-ID modal leaves the note untouched
ok 134 - canceling the Pomodoro block-ID modal leaves the note untouched
  ---
  duration_ms: 0.174614
  ...
# Subtest: review-walk: existing-ID link hands its Linked notice to continue with no separate notice
ok 135 - review-walk: existing-ID link hands its Linked notice to continue with no separate notice
  ---
  duration_ms: 0.940255
  ...
# Subtest: review-walk: prompted-ID link continues after submit
ok 136 - review-walk: prompted-ID link continues after submit
  ---
  duration_ms: 1.721667
  ...
# Subtest: review-walk: prompt cancel settles with null
ok 137 - review-walk: prompt cancel settles with null
  ---
  duration_ms: 0.135388
  ...
# Subtest: review-walk: BUSY swallows the key with no write
ok 138 - review-walk: BUSY swallows the key with no write
  ---
  duration_ms: 0.231322
  ...
# Subtest: review-walk: failed link keeps its notice and settles with null
ok 139 - review-walk: failed link keeps its notice and settles with null
  ---
  duration_ms: 0.180955
  ...
# Subtest: review-walk: partial link keeps its notice and never continues with an outcome
ok 140 - review-walk: partial link keeps its notice and never continues with an outcome
  ---
  duration_ms: 0.745914
  ...
# Subtest: inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
ok 141 - inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
  ---
  duration_ms: 0.201555
  ...
# Subtest: inbox-route: non-inbox notes and task-link mode never prompt
ok 142 - inbox-route: non-inbox notes and task-link mode never prompt
  ---
  duration_ms: 0.70168
  ...
# Subtest: inbox-route: cancel writes nothing and settles once
ok 143 - inbox-route: cancel writes nothing and settles once
  ---
  duration_ms: 0.28289
  ...
# Subtest: inbox-route: stay matches today
ok 144 - inbox-route: stay matches today
  ---
  duration_ms: 0.524011
  ...
# Subtest: inbox-route: move links, then moves, with one composed toast and a route continue
ok 145 - inbox-route: move links, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.639772
  ...
# Subtest: inbox-route: a new block ID goes through the route, then the picker, then the ID prompt
ok 146 - inbox-route: a new block ID goes through the route, then the picker, then the ID prompt
  ---
  duration_ms: 0.719614
  ...
# Subtest: inbox-route: a submitted ID that already exists in the destination keeps the prompt open
ok 147 - inbox-route: a submitted ID that already exists in the destination keeps the prompt open
  ---
  duration_ms: 0.351912
  ...
# Subtest: inbox-route: a move failure gives the partial notice plus a link-today continue
ok 148 - inbox-route: a move failure gives the partial notice plus a link-today continue
  ---
  duration_ms: 0.499974
  ...
# Subtest: review-walk: no nav or nav v2 keeps today's notices
ok 149 - review-walk: no nav or nav v2 keeps today's notices
  ---
  duration_ms: 0.858128
  ...
# Subtest: inbox-route: source drift during route prompt refuses without writes
ok 150 - inbox-route: source drift during route prompt refuses without writes
  ---
  duration_ms: 0.25666
  ...
# Subtest: inbox-route: route cancel up front writes nothing, opens no ID prompt, and settles null once
ok 151 - inbox-route: route cancel up front writes nothing, opens no ID prompt, and settles null once
  ---
  duration_ms: 0.223386
  ...
# Subtest: inbox-route: link no-op with move never commits
ok 152 - inbox-route: link no-op with move never commits
  ---
  duration_ms: 0.176627
  ...
# Subtest: picker opens only on the link direction, never on unlink
ok 153 - picker opens only on the link direction, never on unlink
  ---
  duration_ms: 9.467805
  ...
# Subtest: picker never opens in task-link mode
ok 154 - picker never opens in task-link mode
  ---
  duration_ms: 2.260054
  ...
# Subtest: Depends-On refusals never open the picker
ok 155 - Depends-On refusals never open the picker
  ---
  duration_ms: 0.952749
  ...
# Subtest: preflight refusals open nothing
ok 156 - preflight refusals open nothing
  ---
  duration_ms: 0.549279
  ...
# Subtest: direct picker captures one task suggestion with a one-based line and live note text
ok 157 - direct picker captures one task suggestion with a one-based line and live note text
  ---
  duration_ms: 1.02113
  ...
# Subtest: missing task-theme APIs leave the direct picker on its existing default
ok 158 - missing task-theme APIs leave the direct picker on its existing default
  ---
  duration_ms: 0.675069
  ...
# Subtest: picking a non-default entry links there
ok 159 - picking a non-default entry links there
  ---
  duration_ms: 1.135829
  ...
# Subtest: cancel writes nothing with no Notice and settles the walk null
ok 160 - cancel writes nothing with no Notice and settles the walk null
  ---
  duration_ms: 0.624723
  ...
# Subtest: a no-ID task gets picker, then the block-ID prompt with the target carried
ok 161 - a no-ID task gets picker, then the block-ID prompt with the target carried
  ---
  duration_ms: 1.035277
  ...
# Subtest: inbox order is route, then picker, then write
ok 162 - inbox order is route, then picker, then write
  ---
  duration_ms: 0.96874
  ...
# Subtest: a route cancel never opens the picker and writes nothing
ok 163 - a route cancel never opens the picker and writes nothing
  ---
  duration_ms: 0.344238
  ...
# Subtest: a routed move suggests from the destination with a one-line virtual note
ok 164 - a routed move suggests from the destination with a one-line virtual note
  ---
  duration_ms: 0.49234
  ...
# Subtest: a routed stay suggests from the inbox path
ok 165 - a routed stay suggests from the inbox path
  ---
  duration_ms: 0.543889
  ...
# Subtest: a routed move carries the destination chip and a stay carries none
ok 166 - a routed move carries the destination chip and a stay carries none
  ---
  duration_ms: 0.503321
  ...
# Subtest: a review-walk landing continues with link-today and the new text
ok 167 - a review-walk landing continues with link-today and the new text
  ---
  duration_ms: 0.499894
  ...
# Subtest: an all-closed ledger creates a new entry after the last completed block
ok 168 - an all-closed ledger creates a new entry after the last completed block
  ---
  duration_ms: 1.39334
  ...
# Subtest: several running entries allow an explicit pick
ok 169 - several running entries allow an explicit pick
  ---
  duration_ms: 0.594034
  ...
# Subtest: a target that changed before commit refuses with no writes
ok 170 - a target that changed before commit refuses with no writes
  ---
  duration_ms: 0.379915
  ...
# Subtest: a target that closed before commit refuses with no writes
ok 171 - a target that closed before commit refuses with no writes
  ---
  duration_ms: 0.340149
  ...
# Subtest: the task note being the daily note uses one editor transaction
ok 172 - the task note being the daily note uses one editor transaction
  ---
  duration_ms: 0.666342
  ...
# Subtest: promptOpen blocks re-entry while the picker is open
ok 173 - promptOpen blocks re-entry while the picker is open
  ---
  duration_ms: 11.774349
  ...
# Subtest: direct picker request carries the task line text for the footer
ok 174 - direct picker request carries the task line text for the footer
  ---
  duration_ms: 0.444068
  ...
# Subtest: direct picker stays task-aware when the live note text is unavailable
ok 175 - direct picker stays task-aware when the live note text is unavailable
  ---
  duration_ms: 0.279533
  ...
# Subtest: header shows title, subtitle, lane chip per status, and block-ID chip
ok 176 - header shows title, subtitle, lane chip per status, and block-ID chip
  ---
  duration_ms: 7.903399
  ...
# Subtest: rows render in document order with the default selected
ok 177 - rows render in document order with the default selected
  ---
  duration_ms: 0.998737
  ...
# Subtest: recent theme rows follow today's rows and render component swatches
ok 178 - recent theme rows follow today's rows and render component swatches
  ---
  duration_ms: 28.911788
  ...
# Subtest: exact recent themes suppress generic creation and preserve catalog spelling
ok 179 - exact recent themes suppress generic creation and preserve catalog spelling
  ---
  duration_ms: 3.727095
  ...
# Subtest: Ctrl+D hides a Recent suggestion as an undoable ghost and leaves Today unchanged
ok 180 - Ctrl+D hides a Recent suggestion as an undoable ghost and leaves Today unchanged
  ---
  duration_ms: 13.30335
  ...
# Subtest: new-name rows show near-duplicate and hidden-theme hints
ok 181 - new-name rows show near-duplicate and hidden-theme hints
  ---
  duration_ms: 2.440319
  ...
# Subtest: running row shows progress fraction and minutes-left meta
ok 182 - running row shows progress fraction and minutes-left meta
  ---
  duration_ms: 0.909326
  ...
# Subtest: unnamed entries render muted italic
ok 183 - unnamed entries render muted italic
  ---
  duration_ms: 0.384785
  ...
# Subtest: filtering ranks, highlights, and clearing restores the default
ok 184 - filtering ranks, highlights, and clearing restores the default
  ---
  duration_ms: 0.899748
  ...
# Subtest: create row meta and divider
ok 185 - create row meta and divider
  ---
  duration_ms: 2.871903
  ...
# Subtest: exact open names suppress the create row; prefix matches keep it
ok 186 - exact open names suppress the create row; prefix matches keep it
  ---
  duration_ms: 0.626035
  ...
# Subtest: create rows have no type budget badge
ok 187 - create rows have no type budget badge
  ---
  duration_ms: 0.527748
  ...
# Subtest: invalid rows explain the grammar and are inert on Enter
ok 188 - invalid rows explain the grammar and are inert on Enter
  ---
  duration_ms: 2.810966
  ...
# Subtest: multiple running entries show the banner, no pills, and block creation
ok 189 - multiple running entries show the banner, no pills, and block creation
  ---
  duration_ms: 0.979019
  ...
# Subtest: navigation wraps and skips non-selectable rows
ok 190 - navigation wraps and skips non-selectable rows
  ---
  duration_ms: 1.559076
  ...
# Subtest: empty state invites planning a Pomodoro
ok 191 - empty state invites planning a Pomodoro
  ---
  duration_ms: 0.274705
  ...
# Subtest: footer hints and plan meter
ok 192 - footer hints and plan meter
  ---
  duration_ms: 1.102976
  ...
# Subtest: Enter chooses the selected row; click chooses that row
ok 193 - Enter chooses the selected row; click chooses that row
  ---
  duration_ms: 1.000741
  ...
# Subtest: Shift+Enter creates; an exact open name links there instead
ok 194 - Shift+Enter creates; an exact open name links there instead
  ---
  duration_ms: 0.973007
  ...
# Subtest: Ctrl+Shift+Enter commits exactly like Enter
ok 195 - Ctrl+Shift+Enter commits exactly like Enter
  ---
  duration_ms: 0.47148
  ...
# Subtest: Escape and Ctrl+[ cancel with no choice; settle-once holds
ok 196 - Escape and Ctrl+[ cancel with no choice; settle-once holds
  ---
  duration_ms: 2.450087
  ...
# Subtest: done-today themes stay in Recent while open Today themes stay excluded
ok 197 - done-today themes stay in Recent while open Today themes stay excluded
  ---
  duration_ms: 1.044083
  ...
# Subtest: configured theme menu vectors scope Recent, preserve config order, and flag new names
ok 198 - configured theme menu vectors scope Recent, preserve config order, and flag new names
  ---
  duration_ms: 3.46269
  ...
# Subtest: configured empty-query picker shows up to twelve configured themes
ok 199 - configured empty-query picker shows up to twelve configured themes
  ---
  duration_ms: 0.370928
  ...
# Subtest: link success notice names an unconfigured theme after creating its Pomodoro
ok 200 - link success notice names an unconfigured theme after creating its Pomodoro
  ---
  duration_ms: 0.4714
  ...
# Subtest: typing done shows only the Recent DONE row and keeps catalog spelling
ok 201 - typing done shows only the Recent DONE row and keeps catalog spelling
  ---
  duration_ms: 1.590937
  ...
# Subtest: Today exclusions apply before query filtering; cancelled themes stay Recent
ok 202 - Today exclusions apply before query filtering; cancelled themes stay Recent
  ---
  duration_ms: 1.415433
  ...
# Subtest: suggested entry rows render the reason, dot, theme pill, and accessible label
ok 203 - suggested entry rows render the reason, dot, theme pill, and accessible label
  ---
  duration_ms: 1.663125
  ...
# Subtest: reading and note suggestions render their own reasons and footer phrases
ok 204 - reading and note suggestions render their own reasons and footer phrases
  ---
  duration_ms: 1.305894
  ...
# Subtest: footer previews the default merge and the explicit retype with suggestion context
ok 205 - footer previews the default merge and the explicit retype with suggestion context
  ---
  duration_ms: 2.1109
  ...
# Subtest: footer hides without task context or theme APIs
ok 206 - footer hides without task context or theme APIs
  ---
  duration_ms: 2.815826
  ...
# Subtest: footer states a keep consequence when the destination already agrees
ok 207 - footer states a keep consequence when the destination already agrees
  ---
  duration_ms: 0.960754
  ...
# Subtest: footer previews PLAN, LATER, and Tab cycling on a composite
ok 208 - footer previews PLAN, LATER, and Tab cycling on a composite
  ---
  duration_ms: 1.830855
  ...
# Subtest: footer refreshes on selection moves and hides on inert rows
ok 209 - footer refreshes on selection moves and hides on inert rows
  ---
  duration_ms: 0.863639
  ...
# Subtest: untouched refresh preserves a still-eligible suggested entry; arrivals adopt a first default
ok 210 - untouched refresh preserves a still-eligible suggested entry; arrivals adopt a first default
  ---
  duration_ms: 12.806079
  ...
# Subtest: refresh after typing preserves the user's position and initial key
ok 211 - refresh after typing preserves the user's position and initial key
  ---
  duration_ms: 4.538344
  ...
# Subtest: removed rows fall back deterministically without clearing interaction
ok 212 - removed rows fall back deterministically without clearing interaction
  ---
  duration_ms: 1.902322
  ...
# Subtest: clearing a query keeps interaction but returning home is not deliberate
ok 213 - clearing a query keeps interaction but returning home is not deliberate
  ---
  duration_ms: 1.065074
  ...
# Subtest: suggestion never recomputes on refresh and survives API changes
ok 214 - suggestion never recomputes on refresh and survives API changes
  ---
  duration_ms: 2.473863
  ...
# Subtest: deferred fetch makes an unknown suggestion eligible and settles the untouched default
ok 215 - deferred fetch makes an unknown suggestion eligible and settles the untouched default
  ---
  duration_ms: 1.705557
  ...
# Subtest: onChange adopts a newly eligible existing match only before interaction
ok 216 - onChange adopts a newly eligible existing match only before interaction
  ---
  duration_ms: 0.634121
  ...
# Subtest: refresh after arrows and after typing then clearing keeps the settled user key
ok 217 - refresh after arrows and after typing then clearing keeps the settled user key
  ---
  duration_ms: 0.741075
  ...
# Subtest: typed theme suggestion decorates the final Recent row without changing PT7 order
ok 218 - typed theme suggestion decorates the final Recent row without changing PT7 order
  ---
  duration_ms: 3.240306
  ...
# Subtest: Alt+Enter explicitly requests retype; plain commits keep the default merge
ok 219 - Alt+Enter explicitly requests retype; plain commits keep the default merge
  ---
  duration_ms: 0.689997
  ...
# Subtest: Enter, click, and Ctrl+Shift+Enter share the deliberate rule
ok 220 - Enter, click, and Ctrl+Shift+Enter share the deliberate rule
  ---
  duration_ms: 1.60751
  ...
# Subtest: Shift+Enter named commits are always deliberate
ok 221 - Shift+Enter named commits are always deliberate
  ---
  duration_ms: 1.038373
  ...
# Subtest: cancellation writes nothing even when task-aware
ok 222 - cancellation writes nothing even when task-aware
  ---
  duration_ms: 0.416295
  ...
# Subtest: Ctrl+D on the suggested create row is consumed without writes
ok 223 - Ctrl+D on the suggested create row is consumed without writes
  ---
  duration_ms: 5.128231
  ...
# Subtest: canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
ok 224 - canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
  ---
  duration_ms: 1.692622
  ...
# Subtest: canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
ok 225 - canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
  ---
  duration_ms: 0.273563
  ...
# Subtest: pomodoroLinkSelectorSlug mirrors capture slugs
ok 226 - pomodoroLinkSelectorSlug mirrors capture slugs
  ---
  duration_ms: 0.228416
  ...
# Subtest: parsePomodoroEntryParts reads canonical and legacy entry lines
ok 227 - parsePomodoroEntryParts reads canonical and legacy entry lines
  ---
  duration_ms: 0.852849
  ...
# Subtest: collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
ok 228 - collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
  ---
  duration_ms: 1.525522
  ...
# Subtest: collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
ok 229 - collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
  ---
  duration_ms: 1.079912
  ...
# Subtest: collectPomodoroLinkEntries counts links but excludes struck references
ok 230 - collectPomodoroLinkEntries counts links but excludes struck references
  ---
  duration_ms: 0.55533
  ...
# Subtest: collectPomodoroLinkEntries falls back to range text and position titles
ok 231 - collectPomodoroLinkEntries falls back to range text and position titles
  ---
  duration_ms: 0.34026
  ...
# Subtest: pomodoroRunProgress reports fractions, overtime, and midnight wrap
ok 232 - pomodoroRunProgress reports fractions, overtime, and midnight wrap
  ---
  duration_ms: 0.518551
  ...
# Subtest: buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
ok 233 - buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
  ---
  duration_ms: 1.001363
  ...
# Subtest: buildPomodoroLinkPickerRows keeps the create row for prefix matches
ok 234 - buildPomodoroLinkPickerRows keeps the create row for prefix matches
  ---
  duration_ms: 0.282219
  ...
# Subtest: buildPomodoroLinkPickerRows marks completed-only names as again
ok 235 - buildPomodoroLinkPickerRows marks completed-only names as again
  ---
  duration_ms: 0.182829
  ...
# Subtest: buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
ok 236 - buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
  ---
  duration_ms: 0.404142
  ...
# Subtest: buildPomodoroLinkPickerRows matches times, positions, and block IDs
ok 237 - buildPomodoroLinkPickerRows matches times, positions, and block IDs
  ---
  duration_ms: 0.5079
  ...
# Subtest: resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
ok 238 - resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
  ---
  duration_ms: 0.321725
  ...
# Subtest: defaultPomodoroLinkChoice returns the default entry or null
ok 239 - defaultPomodoroLinkChoice returns the default entry or null
  ---
  duration_ms: 0.19916
  ...
# Subtest: planExplicitPomodoroLinkInsertion links under a chosen existing entry
ok 240 - planExplicitPomodoroLinkInsertion links under a chosen existing entry
  ---
  duration_ms: 1.038402
  ...
# Subtest: planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
ok 241 - planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
  ---
  duration_ms: 0.381549
  ...
# Subtest: planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
ok 242 - planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
  ---
  duration_ms: 1.071215
  ...
# Subtest: planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
ok 243 - planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
  ---
  duration_ms: 0.395556
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after the running entry
ok 244 - planExplicitPomodoroLinkInsertion creates after the running entry
  ---
  duration_ms: 0.640573
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
ok 245 - planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
  ---
  duration_ms: 0.737658
  ...
# Subtest: planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
ok 246 - planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
  ---
  duration_ms: 0.26723
  ...
# Subtest: planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
ok 247 - planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
  ---
  duration_ms: 0.352443
  ...
# Subtest: planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
ok 248 - planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
  ---
  duration_ms: 0.453767
  ...
# Subtest: buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
ok 249 - buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
  ---
  duration_ms: 0.224759
  ...
# Subtest: buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
ok 250 - buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
  ---
  duration_ms: 0.205853
  ...
# Subtest: planExplicitPomodoroLinkInsertion matches mixed-case raced open names
ok 251 - planExplicitPomodoroLinkInsertion matches mixed-case raced open names
  ---
  duration_ms: 0.237573
  ...
# Subtest: buildPomodoroLinkPickerRows bounds \#N position matches
ok 252 - buildPomodoroLinkPickerRows bounds \#N position matches
  ---
  duration_ms: 0.454588
  ...
# Subtest: planPomodoroLinkInsertion without a target keeps today's behavior and shape
ok 253 - planPomodoroLinkInsertion without a target keeps today's behavior and shape
  ---
  duration_ms: 0.531204
  ...
# Subtest: buildPomodoroLinkPickerRows keeps a done-only theme in Recent
ok 254 - buildPomodoroLinkPickerRows keeps a done-only theme in Recent
  ---
  duration_ms: 2.001371
  ...
# Subtest: shared task-theme preselection vectors match the bob-cli model
ok 255 - shared task-theme preselection vectors match the bob-cli model
  ---
  duration_ms: 2.315621
  ...
# Subtest: task-theme preselection normalizes exemptions without a type cap
ok 256 - task-theme preselection normalizes exemptions without a type cap
  ---
  duration_ms: 0.201544
  ...
# Subtest: task-aware rows preselect an existing match when creation is blocked
ok 257 - task-aware rows preselect an existing match when creation is blocked
  ---
  duration_ms: 0.387229
  ...
# Subtest: task-aware typed queries keep PT7 order and only annotate the matching row
ok 258 - task-aware typed queries keep PT7 order and only annotate the matching row
  ---
  duration_ms: 0.63395
  ...
# Subtest: suggested creation uses catalog spelling and removes its duplicate Recent row
ok 259 - suggested creation uses catalog spelling and removes its duplicate Recent row
  ---
  duration_ms: 1.1107
  ...
# Subtest: theme suggestion identity ignores decorative hue and catalog flags
ok 260 - theme suggestion identity ignores decorative hue and catalog flags
  ---
  duration_ms: 1.390805
  ...
# Subtest: theme suggestion identity treats a changed declaring note as a different suggestion
ok 261 - theme suggestion identity treats a changed declaring note as a different suggestion
  ---
  duration_ms: 0.190574
  ...
# Subtest: current exempt keys distinguish valid empty configuration from unavailable caps
ok 262 - current exempt keys distinguish valid empty configuration from unavailable caps
  ---
  duration_ms: 1.211623
  ...
# Subtest: planTargetTaskUpdate applies themeEdit after lane changes and before a new block ID
ok 263 - planTargetTaskUpdate applies themeEdit after lane changes and before a new block ID
  ---
  duration_ms: 0.858288
  ...
# Subtest: planTargetTaskUpdate theme-only Next task never stamps freshness
ok 264 - planTargetTaskUpdate theme-only Next task never stamps freshness
  ---
  duration_ms: 0.387229
  ...
# Subtest: planTargetTaskUpdate stamps a lane rewrite after the theme field is in place
ok 265 - planTargetTaskUpdate stamps a lane rewrite after the theme field is in place
  ---
  duration_ms: 0.364987
  ...
# Subtest: planTargetTaskUpdate without themeEdit preserves an authored theme field
ok 266 - planTargetTaskUpdate without themeEdit preserves an authored theme field
  ---
  duration_ms: 0.217856
  ...
# Subtest: planTargetTaskUpdate clears a theme field and keeps CRLF plus a trailing block ID
ok 267 - planTargetTaskUpdate clears a theme field and keeps CRLF plus a trailing block ID
  ---
  duration_ms: 0.180134
  ...
# Subtest: a named destination retypes the task in the same cross-note write
ok 268 - a named destination retypes the task in the same cross-note write
  ---
  duration_ms: 5.906428
  ...
# Subtest: a newly named picker entry forces the retype landing path
ok 269 - a newly named picker entry forces the retype landing path
  ---
  duration_ms: 0.580348
  ...
# Subtest: Pomodoro cleanup agrees only touched open entries in the same edit plan
ok 270 - Pomodoro cleanup agrees only touched open entries in the same edit plan
  ---
  duration_ms: 0.601759
  ...
# Subtest: unavailable current caps still retype the task and retain lane, ID, and freshness edits
ok 271 - unavailable current caps still retype the task and retain lane, ID, and freshness edits
  ---
  duration_ms: 4.574533
  ...
# Subtest: real Ledger Tools planner writes with an empty exempt list and custom exemptions
ok 272 - real Ledger Tools planner writes with an empty exempt list and custom exemptions
  ---
  duration_ms: 2.119426
  ...
# Subtest: a Ready scheduled task sets Next, logs the date, and remembers the theme
ok 273 - a Ready scheduled task sets Next, logs the date, and remembers the theme
  ---
  duration_ms: 16.355375
  ...
# Subtest: choosing the inherited destination clears an existing task theme
ok 274 - choosing the inherited destination clears an existing task theme
  ---
  duration_ms: 11.125211
  ...
# Subtest: a theme-only Next task with a new block ID still stamps because the ID rewrote the line
ok 275 - a theme-only Next task with a new block ID still stamps because the ID rewrote the line
  ---
  duration_ms: 0.473614
  ...
# Subtest: duplicate and paren theme fields repair only on an eligible deliberate write
ok 276 - duplicate and paren theme fields repair only on an eligible deliberate write
  ---
  duration_ms: 0.414301
  ...
# Subtest: a stale shown suggestion links and skips the theme edit
ok 277 - a stale shown suggestion links and skips the theme edit
  ---
  duration_ms: 0.362923
  ...
# Subtest: decorative catalog metadata on a live suggestion does not skip the write
ok 278 - decorative catalog metadata on a live suggestion does not skip the write
  ---
  duration_ms: 0.38767
  ...
# Subtest: Enter merges the current type into the destination name
ok 279 - Enter merges the current type into the destination name
  ---
  duration_ms: 0.386428
  ...
# Subtest: a container keeps the type on the default landing
ok 280 - a container keeps the type on the default landing
  ---
  duration_ms: 0.297879
  ...
# Subtest: untouched default (not deliberate) links without storing a field
ok 281 - untouched default (not deliberate) links without storing a field
  ---
  duration_ms: 0.34557
  ...
# Subtest: absent theme APIs leave the picker write path usable without a field
ok 282 - absent theme APIs leave the picker write path usable without a field
  ---
  duration_ms: 0.359646
  ...
# Subtest: a blocked dependency consumption never writes a theme field
ok 283 - a blocked dependency consumption never writes a theme field
  ---
  duration_ms: 1.863237
  ...
# Subtest: same-note combined edit writes the theme and the link in one editor transaction
ok 284 - same-note combined edit writes the theme and the link in one editor transaction
  ---
  duration_ms: 0.507839
  ...
# Subtest: a failed daily write after a saved theme reports the theme and the link failure
ok 285 - a failed daily write after a saved theme reports the theme and the link failure
  ---
  duration_ms: 0.414762
  ...
# Subtest: catalog spelling wins over a canonical landing name
ok 286 - catalog spelling wins over a canonical landing name
  ---
  duration_ms: 0.325481
  ...
# Subtest: a routed inbox task retypes from the destination suggestion
ok 287 - a routed inbox task retypes from the destination suggestion
  ---
  duration_ms: 0.695047
  ...
# Subtest: the inbox and the destination inherit different types, and the user picks the destination's suggested Pomodoro
ok 288 - the inbox and the destination inherit different types, and the user picks the destination's suggested Pomodoro
  ---
  duration_ms: 0.390585
  ...
# Subtest: a routed link that picks a different type writes the field
ok 289 - a routed link that picks a different type writes the field
  ---
  duration_ms: 0.421716
  ...
# Subtest: malformed themeIntent never enables a write
ok 290 - malformed themeIntent never enables a write
  ---
  duration_ms: 0.264845
  ...
# Subtest: themeIntent survives normalizePomodoroLinkPickerChoice for a later consumer
ok 291 - themeIntent survives normalizePomodoroLinkPickerChoice for a later consumer
  ---
  duration_ms: 0.218146
  ...
# Subtest: Tab pick chooses that type component of a composite destination
ok 292 - Tab pick chooses that type component of a composite destination
  ---
  duration_ms: 0.310542
  ...
# Subtest: unlink preserves an authored task theme
ok 293 - unlink preserves an authored task theme
  ---
  duration_ms: 2.878185
  ...
# Subtest: direct unlink without a daily note keeps the Next lane and reports it
ok 294 - direct unlink without a daily note keeps the Next lane and reports it
  ---
  duration_ms: 2.670579
  ...
# Subtest: In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
ok 295 - In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
  ---
  duration_ms: 0.475768
  ...
# Subtest: In Progress unlink with a summary keeps the lane and creates a Work Log
ok 296 - In Progress unlink with a summary keeps the lane and creates a Work Log
  ---
  duration_ms: 1.150477
  ...
# Subtest: In Progress unlink revalidates task text and block-ID uniqueness at confirmation
ok 297 - In Progress unlink revalidates task text and block-ID uniqueness at confirmation
  ---
  duration_ms: 0.317125
  ...
# Subtest: Next task unlink removes current and future links and keeps the Next lane
ok 298 - Next task unlink removes current and future links and keeps the Next lane
  ---
  duration_ms: 3.968557
  ...
# Subtest: In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
ok 299 - In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
  ---
  duration_ms: 1.007063
  ...
# Subtest: same-note Next unlink merges the Work Log and all-open cleanup in the active editor
ok 300 - same-note Next unlink merges the Work Log and all-open cleanup in the active editor
  ---
  duration_ms: 0.894297
  ...
# Subtest: same-note In Progress unlink merges cleanup and Work Log in the active editor
ok 301 - same-note In Progress unlink merges cleanup and Work Log in the active editor
  ---
  duration_ms: 0.616847
  ...
# Subtest: Next unlink stops before any write when daily cleanup write is stale
ok 302 - Next unlink stops before any write when daily cleanup write is stale
  ---
  duration_ms: 0.708753
  ...
# Subtest: Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
ok 303 - Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
  ---
  duration_ms: 1.395935
  ...
# Subtest: In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
ok 304 - In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
  ---
  duration_ms: 0.932811
  ...
# Subtest: review-walk: unlink settles with null and keeps its notice
ok 305 - review-walk: unlink settles with null and keeps its notice
  ---
  duration_ms: 1.667423
  ...
# Subtest: inbox-route: unlink cancel writes nothing
ok 306 - inbox-route: unlink cancel writes nothing
  ---
  duration_ms: 0.432696
  ...
# Subtest: inbox-route: unlink stay matches today and never commits
ok 307 - inbox-route: unlink stay matches today and never commits
  ---
  duration_ms: 0.642247
  ...
# Subtest: inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
ok 308 - inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.766894
  ...
# Subtest: inbox-route: In Progress unlink with a Work summary routes
ok 309 - inbox-route: In Progress unlink with a Work summary routes
  ---
  duration_ms: 0.707982
  ...
# Subtest: inbox-route: unlink move failure gives the partial notice and stays
ok 310 - inbox-route: unlink move failure gives the partial notice and stays
  ---
  duration_ms: 0.32486
  ...
# Subtest: inbox-route: non-inbox unlink never prompts
ok 311 - inbox-route: non-inbox unlink never prompts
  ---
  duration_ms: 0.324801
  ...
# Subtest: review-walk: Work-summary unlink path retains origin until submit
ok 312 - review-walk: Work-summary unlink path retains origin until submit
  ---
  duration_ms: 0.314882
  ...
# Subtest: inbox-route: unlink source drift during route prompt refuses without writes
ok 313 - inbox-route: unlink source drift during route prompt refuses without writes
  ---
  duration_ms: 0.247373
  ...
# Subtest: inbox-route: Work-summary route cancel returns sentinel and settles null once
ok 314 - inbox-route: Work-summary route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.259486
  ...
# Subtest: inbox-route: unlink no-op with move never commits
ok 315 - inbox-route: unlink no-op with move never commits
  ---
  duration_ms: 0.237042
  ...
# Subtest: same-note unlink maps a task below removed entries through Work-summary inserts
ok 316 - same-note unlink maps a task below removed entries through Work-summary inserts
  ---
  duration_ms: 0.606037
  ...
# Subtest: the unlink preview shows the write-instant stamp and re-renders on the clock
ok 317 - the unlink preview shows the write-instant stamp and re-renders on the clock
  ---
  duration_ms: 0.484254
  ...
# Subtest: a prompt opened at 23:59 and committed at 00:01 stamps the commit instant
ok 318 - a prompt opened at 23:59 and committed at 00:01 stamps the commit instant
  ---
  duration_ms: 0.459678
  ...
# Subtest: direct-add seeds from the task headline, not non-task blocks
ok 319 - direct-add seeds from the task headline, not non-task blocks
  ---
  duration_ms: 3.793733
  ...
# Subtest: direct-add seeds a plain note bullet from its text without the created stamp
ok 320 - direct-add seeds a plain note bullet from its text without the created stamp
  ---
  duration_ms: 0.571882
  ...
# Subtest: link-task-complete seeds from the target, prefers open buffers
ok 321 - link-task-complete seeds from the target, prefers open buffers
  ---
  duration_ms: 0.895059
  ...
# Subtest: link-task-complete reports stale and unreadable targets
ok 322 - link-task-complete reports stale and unreadable targets
  ---
  duration_ms: 0.275115
  ...
# Subtest: pomodoro link seeds after the choice from the cursor task
ok 323 - pomodoro link seeds after the choice from the cursor task
  ---
  duration_ms: 0.329489
  ...
# Subtest: marker rename suggests from the unique task, never hiding ambiguity
ok 324 - marker rename suggests from the unique task, never hiding ambiguity
  ---
  duration_ms: 0.517188
  ...
# Subtest: marker rename suggests from a unique plain note bullet
ok 325 - marker rename suggests from a unique plain note bullet
  ---
  duration_ms: 0.342223
  ...
# Subtest: modal seeds the value, selects once, and never overwrites typing
ok 326 - modal seeds the value, selects once, and never overwrites typing
  ---
  duration_ms: 1.0895
  ...
# Subtest: modal disables Save while loading and survives close/reopen
ok 327 - modal disables Save while loading and survives close/reopen
  ---
  duration_ms: 1.230469
  ...
# Subtest: submit revalidates: occupied IDs and stale tasks fail editable
ok 328 - submit revalidates: occupied IDs and stale tasks fail editable
  ---
  duration_ms: 1.041108
  ...
# Subtest: cancelling writes no ID and explicit renames keep the current ID
ok 329 - cancelling writes no ID and explicit renames keep the current ID
  ---
  duration_ms: 0.570579
  ...
# Subtest: the task picker drops the paired \#ref and prefixes the book
ok 330 - the task picker drops the paired \#ref and prefixes the book
  ---
  duration_ms: 3.141518
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 331 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.396607
  ...
# Subtest: block-id-prompt LK1–LK19 recognises only relation line shapes
ok 332 - block-id-prompt LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 1.378141
  ...
# Subtest: block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
ok 333 - block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
  ---
  duration_ms: 0.999078
  ...
# Subtest: block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
ok 334 - block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
  ---
  duration_ms: 2.358011
  ...
# Subtest: a rename writes each open note as one editor transaction and undoes in one step
ok 335 - a rename writes each open note as one editor transaction and undoes in one step
  ---
  duration_ms: 15.461859
  ...
# Subtest: a note open in a non-active leaf is edited through its editor, unsaved text included
ok 336 - a note open in a non-active leaf is edited through its editor, unsaved text included
  ---
  duration_ms: 0.773897
  ...
# Subtest: disagreeing open buffers for one note refuse the rename
ok 337 - disagreeing open buffers for one note refuse the rename
  ---
  duration_ms: 0.608773
  ...
# Subtest: a closed note that changed since planning refuses and earlier writes roll back
ok 338 - a closed note that changed since planning refuses and earlier writes roll back
  ---
  duration_ms: 0.774489
  ...
# Subtest: an open note that changed while closed notes were written refuses and rolls back
ok 339 - an open note that changed while closed notes were written refuses and rolls back
  ---
  duration_ms: 0.606418
  ...
# Subtest: undoing the rename in its note rewrites the other notes back, and redo re-applies it
ok 340 - undoing the rename in its note rewrites the other notes back, and redo re-applies it
  ---
  duration_ms: 1.776552
  ...
# Subtest: undoing in a referencing note follows into the destination and the other notes
ok 341 - undoing in a referencing note follows into the destination and the other notes
  ---
  duration_ms: 0.986724
  ...
# Subtest: an ambiguous note is left alone and named in a sticky Notice
ok 342 - an ambiguous note is left alone and named in a sticky Notice
  ---
  duration_ms: 0.831938
  ...
# Subtest: a recorded span that was edited makes its note ambiguous
ok 343 - a recorded span that was edited makes its note ambiguous
  ---
  duration_ms: 1.034314
  ...
# Subtest: editing a note the follow could not rewrite never redoes the rename
ok 344 - editing a note the follow could not rewrite never redoes the rename
  ---
  duration_ms: 1.038834
  ...
# Subtest: records expire, and edits without a live record schedule nothing
ok 345 - records expire, and edits without a live record schedule nothing
  ---
  duration_ms: 0.952609
  ...
# Subtest: a redo during closed-note undo follow converges on the latest editor form
ok 346 - a redo during closed-note undo follow converges on the latest editor form
  ---
  duration_ms: 1.090212
  ...
# Subtest: an undo during closed-note redo follow converges on the latest editor form
ok 347 - an undo during closed-note redo follow converges on the latest editor form
  ---
  duration_ms: 1.773536
  ...
# Subtest: an unrelated edit in a second editor during closed follow is preserved
ok 348 - an unrelated edit in a second editor during closed follow is preserved
  ---
  duration_ms: 0.944593
  ...
# Subtest: blockRenameNoteForm reads token and link forms and refuses mixed or missing states
ok 349 - blockRenameNoteForm reads token and link forms and refuses mixed or missing states
  ---
  duration_ms: 0.326663
  ...
# Subtest: calendar date parsing rejects malformed width and impossible dates
ok 350 - calendar date parsing rejects malformed width and impossible dates
  ---
  duration_ms: 2.127762
  ...
# Subtest: future scheduled field detection respects the yesterday/today/tomorrow boundary
ok 351 - future scheduled field detection respects the yesterday/today/tomorrow boundary
  ---
  duration_ms: 0.46619
  ...
# Subtest: scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
ok 352 - scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
  ---
  duration_ms: 0.199621
  ...
# Subtest: planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
ok 353 - planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
  ---
  duration_ms: 0.862767
  ...
# Subtest: planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
ok 354 - planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
  ---
  duration_ms: 0.280375
  ...
# Subtest: planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
ok 355 - planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
  ---
  duration_ms: 0.170926
  ...
# Subtest: planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
ok 356 - planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
  ---
  duration_ms: 0.155998
  ...
# Subtest: planTargetTaskUpdate leaves today and past schedules untouched
ok 357 - planTargetTaskUpdate leaves today and past schedules untouched
  ---
  duration_ms: 0.309591
  ...
# Subtest: planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
ok 358 - planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
  ---
  duration_ms: 0.362953
  ...
# Subtest: two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
ok 359 - two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
  ---
  duration_ms: 0.47646
  ...
# Subtest: a malformed single scheduled field is never treated as future
ok 360 - a malformed single scheduled field is never treated as future
  ---
  duration_ms: 0.174774
  ...
# Subtest: an ambiguous scheduled field does not block the legacy Ready promotion
ok 361 - an ambiguous scheduled field does not block the legacy Ready promotion
  ---
  duration_ms: 0.193059
  ...
# Subtest: planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
ok 362 - planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
  ---
  duration_ms: 0.139396
  ...
# Subtest: Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
ok 363 - Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
  ---
  duration_ms: 0.486088
  ...
# Subtest: Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
ok 364 - Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
  ---
  duration_ms: 0.155306
  ...
# Subtest: planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
ok 365 - planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
  ---
  duration_ms: 0.253294
  ...
# Subtest: planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
ok 366 - planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
  ---
  duration_ms: 0.145518
  ...
# Subtest: planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
ok 367 - planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.10999
  ...
# Subtest: planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
ok 368 - planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
  ---
  duration_ms: 0.286787
  ...
# Subtest: planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
ok 369 - planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
  ---
  duration_ms: 0.142953
  ...
# Subtest: planTargetTaskUpdate preserves a trailing newline when one was already present
ok 370 - planTargetTaskUpdate preserves a trailing newline when one was already present
  ---
  duration_ms: 0.153543
  ...
# Subtest: planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
ok 371 - planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
  ---
  duration_ms: 0.109249
  ...
# Subtest: planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
ok 372 - planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
  ---
  duration_ms: 0.172069
  ...
# Subtest: planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
ok 373 - planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
  ---
  duration_ms: 0.124207
  ...
# Subtest: existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
ok 374 - existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
  ---
  duration_ms: 3.767412
  ...
# Subtest: new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
ok 375 - new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
  ---
  duration_ms: 0.836698
  ...
# Subtest: activation runtime aborts without any write when the target preimage goes stale
ok 376 - activation runtime aborts without any write when the target preimage goes stale
  ---
  duration_ms: 0.443426
  ...
# Subtest: same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
ok 377 - same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
  ---
  duration_ms: 2.475246
  ...
# Subtest: same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
ok 378 - same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
  ---
  duration_ms: 0.617038
  ...
# Subtest: a source marker edited after a successful existing-ID target write reports an accurate partial notice
ok 379 - a source marker edited after a successful existing-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.491729
  ...
# Subtest: a source marker edited after a successful new-ID target write reports an accurate partial notice
ok 380 - a source marker edited after a successful new-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.554168
  ...
# Subtest: planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
ok 381 - planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
  ---
  duration_ms: 0.215001
  ...
# Subtest: planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
ok 382 - planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
  ---
  duration_ms: 0.130169
  ...
# Subtest: planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
ok 383 - planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
  ---
  duration_ms: 0.135909
  ...
# Subtest: Pomodoro forceNext stamps the pulled-forward Ready task before its block ID
ok 384 - Pomodoro forceNext stamps the pulled-forward Ready task before its block ID
  ---
  duration_ms: 0.40286
  ...
# Subtest: planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
ok 385 - planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.113587
  ...
# Subtest: direct Task Links raise ^prj while never pulling its date forward
ok 386 - direct Task Links raise ^prj while never pulling its date forward
  ---
  duration_ms: 0.128395
  ...
# Subtest: task-link selection: one link is selectable from any column, several are chosen by cursor
ok 387 - task-link selection: one link is selectable from any column, several are chosen by cursor
  ---
  duration_ms: 2.804324
  ...
# Subtest: task-link selection ignores picker/rename markers, plain links, and Markdown-style links
ok 388 - task-link selection ignores picker/rename markers, plain links, and Markdown-style links
  ---
  duration_ms: 0.306134
  ...
# Subtest: dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
ok 389 - dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
  ---
  duration_ms: 0.907623
  ...
# Subtest: inline Task Link deletion removes the token with its decoration and collapses whitespace
ok 390 - inline Task Link deletion removes the token with its decoration and collapses whitespace
  ---
  duration_ms: 0.63391
  ...
# Subtest: dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
ok 391 - dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
  ---
  duration_ms: 0.871524
  ...
# Subtest: mergeCoveringEdits keeps the covering edit and the earlier of identical edits
ok 392 - mergeCoveringEdits keeps the covering edit and the earlier of identical edits
  ---
  duration_ms: 0.21463
  ...
# Subtest: dependency transclusion detection needs an embedded sole-content child of a \#task line
ok 393 - dependency transclusion detection needs an embedded sole-content child of a \#task line
  ---
  duration_ms: 0.575659
  ...
# Subtest: Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
ok 394 - Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
  ---
  duration_ms: 5.542501
  ...
# Subtest: Task Link on a Next target works from an embedded aliased link outside any Pomodoro
ok 395 - Task Link on a Next target works from an embedded aliased link outside any Pomodoro
  ---
  duration_ms: 1.197366
  ...
# Subtest: same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
ok 396 - same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
  ---
  duration_ms: 1.266448
  ...
# Subtest: same-note Task Link deletion clamps the restored cursor to the shortened note
ok 397 - same-note Task Link deletion clamps the restored cursor to the shortened note
  ---
  duration_ms: 0.592792
  ...
# Subtest: a cleanup subtree that covers a nested selected link wins and links are not double counted
ok 398 - a cleanup subtree that covers a nested selected link wins and links are not double counted
  ---
  duration_ms: 0.901862
  ...
# Subtest: same-note Task Link in a closed entry deletes the closed entry it empties
ok 399 - same-note Task Link in a closed entry deletes the closed entry it empties
  ---
  duration_ms: 0.943161
  ...
# Subtest: Task Link in another day's note deletes the emptied entry there and in today's note
ok 400 - Task Link in another day's note deletes the emptied entry there and in today's note
  ---
  duration_ms: 0.824174
  ...
# Subtest: Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
ok 401 - Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
  ---
  duration_ms: 1.67622
  ...
# Subtest: Task Link on an In Progress target with a blank summary logs nothing
ok 402 - Task Link on an In Progress target with a blank summary logs nothing
  ---
  duration_ms: 1.071956
  ...
# Subtest: canceling the In Progress Task Link prompt leaves everything untouched
ok 403 - canceling the In Progress Task Link prompt leaves everything untouched
  ---
  duration_ms: 0.430842
  ...
# Subtest: canceling the In Progress unlink prompt in task mode leaves everything untouched
ok 404 - canceling the In Progress unlink prompt in task mode leaves everything untouched
  ---
  duration_ms: 0.828783
  ...
# Subtest: In Progress Task Link submit revalidates the link line and the target task
ok 405 - In Progress Task Link submit revalidates the link line and the target task
  ---
  duration_ms: 0.611948
  ...
# Subtest: Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
ok 406 - Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
  ---
  duration_ms: 1.357892
  ...
# Subtest: Task Link on a Done or Cancelled target is refused without edits
ok 407 - Task Link on a Done or Cancelled target is refused without edits
  ---
  duration_ms: 0.289954
  ...
# Subtest: Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
ok 408 - Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
  ---
  duration_ms: 0.547876
  ...
# Subtest: precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
ok 409 - precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
  ---
  duration_ms: 1.636334
  ...
# Subtest: Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
ok 410 - Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
  ---
  duration_ms: 0.54475
  ...
# Subtest: Task Link that is a sub-task dependency transclusion is refused without edits
ok 411 - Task Link that is a sub-task dependency transclusion is refused without edits
  ---
  duration_ms: 0.235159
  ...
# Subtest: Task Link partial failure after the daily write is retryable
ok 412 - Task Link partial failure after the daily write is retryable
  ---
  duration_ms: 0.694656
  ...
# Subtest: Task Link stops before any write when the target note changes after planning
ok 413 - Task Link stops before any write when the target note changes after planning
  ---
  duration_ms: 0.381949
  ...
# Subtest: Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
ok 414 - Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
  ---
  duration_ms: 0.423088
  ...
# Subtest: Task Link subtree deletion removes a nested target task without any status write
ok 415 - Task Link subtree deletion removes a nested target task without any status write
  ---
  duration_ms: 0.31435
  ...
# Subtest: whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
ok 416 - whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
  ---
  duration_ms: 0.619824
  ...
# Subtest: selected-link deletion maps a cursor inside a removed entry to its former start
ok 417 - selected-link deletion maps a cursor inside a removed entry to its former start
  ---
  duration_ms: 0.555701
  ...
# Subtest: cache prefilter skips taskless files without reading, reads cacheless files
ok 418 - cache prefilter skips taskless files without reading, reads cacheless files
  ---
  duration_ms: 4.774025
  ...
# Subtest: a throwing file cache falls back to reading
ok 419 - a throwing file cache falls back to reading
  ---
  duration_ms: 0.431413
  ...
# Subtest: non-note and excluded paths never enter the store
ok 420 - non-note and excluded paths never enter the store
  ---
  duration_ms: 0.458385
  ...
# Subtest: unreadable files produce bounded warnings and a quiet footer note
ok 421 - unreadable files produce bounded warnings and a quiet footer note
  ---
  duration_ms: 0.888556
  ...
# Subtest: blockIdsFor exposes the note id set for the detail strip preview
ok 422 - blockIdsFor exposes the note id set for the detail strip preview
  ---
  duration_ms: 0.331503
  ...
# Subtest: taskBearingDocuments reads fresh text on demand
ok 423 - taskBearingDocuments reads fresh text on demand
  ---
  duration_ms: 0.510044
  ...
# Subtest: metadataCache changed re-parses from event data with no extra read
ok 424 - metadataCache changed re-parses from event data with no extra read
  ---
  duration_ms: 0.449128
  ...
# Subtest: vault rename re-keys rows and recomputes the basename index
ok 425 - vault rename re-keys rows and recomputes the basename index
  ---
  duration_ms: 0.868979
  ...
# Subtest: renaming onto an excluded path drops the note
ok 426 - renaming onto an excluded path drops the note
  ---
  duration_ms: 0.382069
  ...
# Subtest: vault delete drops rows
ok 427 - vault delete drops rows
  ---
  duration_ms: 0.497509
  ...
# Subtest: open-time mtime validation queues changed files for background re-parse
ok 428 - open-time mtime validation queues changed files for background re-parse
  ---
  duration_ms: 0.615916
  ...
# Subtest: a vanished file is removed when the reparse queue drains
ok 429 - a vanished file is removed when the reparse queue drains
  ---
  duration_ms: 0.352583
  ...
# Subtest: live overlays win over disk and never persist
ok 430 - live overlays win over disk and never persist
  ---
  duration_ms: 0.297959
  ...
# Subtest: snapshot returns ordered rows, progress, and a live subscription
ok 431 - snapshot returns ordered rows, progress, and a live subscription
  ---
  duration_ms: 0.439238
  ...
# Subtest: filtering performs no vault reads
ok 432 - filtering performs no vault reads
  ---
  duration_ms: 0.340801
  ...
# Subtest: refreshPaths applies post-write content and recomputes locators
ok 433 - refreshPaths applies post-write content and recomputes locators
  ---
  duration_ms: 0.278963
  ...
# Subtest: refreshPathsFromVault re-reads named paths
ok 434 - refreshPathsFromVault re-reads named paths
  ---
  duration_ms: 0.283771
  ...
# Subtest: collectEditorOverlays reads every open markdown editor
ok 435 - collectEditorOverlays reads every open markdown editor
  ---
  duration_ms: 0.280125
  ...
# Subtest: attachLiveUpdates without a host is a safe no-op
ok 436 - attachLiveUpdates without a host is a safe no-op
  ---
  duration_ms: 0.119248
  ...
# Subtest: custom settings narrow the parsed pool
ok 437 - custom settings narrow the parsed pool
  ---
  duration_ms: 0.192698
  ...
# Subtest: snapshot rows keep parsed metadata, leave stored rows bare, and cache search-text-first fields
ok 438 - snapshot rows keep parsed metadata, leave stored rows bare, and cache search-text-first fields
  ---
  duration_ms: 1.709103
  ...
# Subtest: cached and uncached matching stay aligned across overlay, rename collision, delete, and refresh
ok 439 - cached and uncached matching stay aligned across overlay, rename collision, delete, and refresh
  ---
  duration_ms: 3.686778
  ...
# Subtest: task wikilink fixture mirrors bob-cli byte for byte
ok 440 - task wikilink fixture mirrors bob-cli byte for byte
  ---
  duration_ms: 1.509733
  ...
# Subtest: every vector ranks the same rows bob serves
ok 441 - every vector ranks the same rows bob serves
  ---
  duration_ms: 6.900977
  ...
# Subtest: frontmatter tasks never parse, unclosed fences stay open
ok 442 - frontmatter tasks never parse, unclosed fences stay open
  ---
  duration_ms: 0.357603
  ...
# Subtest: task grammar mirrors bob: dashes only, exact filter token
ok 443 - task grammar mirrors bob: dashes only, exact filter token
  ---
  duration_ms: 0.169443
  ...
# Subtest: trailing IDs need whitespace and clean bytes; every line counts
ok 444 - trailing IDs need whitespace and clean bytes; every line counts
  ---
  duration_ms: 0.183049
  ...
# Subtest: hide and project-block tags are exact tokens
ok 445 - hide and project-block tags are exact tokens
  ---
  duration_ms: 0.213147
  ...
# Subtest: search text drops filters, fields, and the block ID
ok 446 - search text drops filters, fields, and the block ID
  ---
  duration_ms: 0.322256
  ...
# Subtest: sections track headings and depth counts indentation
ok 447 - sections track headings and depth counts indentation
  ---
  duration_ms: 0.311444
  ...
# Subtest: note paths, locators, and archive targets
ok 448 - note paths, locators, and archive targets
  ---
  duration_ms: 0.426625
  ...
# Subtest: match tiers, AND terms, and empty queries
ok 449 - match tiers, AND terms, and empty queries
  ---
  duration_ms: 0.430021
  ...
# Subtest: previous daily is the latest daily before the anchor
ok 450 - previous daily is the latest daily before the anchor
  ---
  duration_ms: 0.201404
  ...
# Subtest: guards mirror bob, minus the read-only check
ok 451 - guards mirror bob, minus the read-only check
  ---
  duration_ms: 0.192327
  ...
# Subtest: fused scorer matches the layered scorer across randomized rows and queries
ok 452 - fused scorer matches the layered scorer across randomized rows and queries
  ---
  duration_ms: 62.112283
  ...
# Subtest: ID-less task identity relocates only to one exact line
ok 453 - ID-less task identity relocates only to one exact line
  ---
  duration_ms: 1.117795
  ...
# Subtest: wikilink naming validates closed tasks and rejects duplicate target IDs
ok 454 - wikilink naming validates closed tasks and rejects duplicate target IDs
  ---
  duration_ms: 0.740083
  ...
# Subtest: wikilink naming adds an ID to a moved closed task and links the original token
ok 455 - wikilink naming adds an ID to a moved closed task and links the original token
  ---
  duration_ms: 1.931779
  ...
# Subtest: ^^ naming preserves a cross-note target and alias through the final link
ok 456 - ^^ naming preserves a cross-note target and alias through the final link
  ---
  duration_ms: 2.520372
  ...
# Subtest: auto-open only on a written second paren, including auto-pair and closed shapes
ok 457 - auto-open only on a written second paren, including auto-pair and closed shapes
  ---
  duration_ms: 28.98132
  ...
# Subtest: caret-only, undo, and programmatic edits never auto-open
ok 458 - caret-only, undo, and programmatic edits never auto-open
  ---
  duration_ms: 0.531745
  ...
# Subtest: query seeds from the token and keys move, accept, escape, and backspace
ok 459 - query seeds from the token and keys move, accept, escape, and backspace
  ---
  duration_ms: 5.978805
  ...
# Subtest: Backspace undoes closed ((q)) to () and unclosed ((q to (
ok 460 - Backspace undoes closed ((q)) to () and unclosed ((q to (
  ---
  duration_ms: 2.118405
  ...
# Subtest: identified accept splices one transaction, caret after ]], no notice
ok 461 - identified accept splices one transaction, caret after ]], no notice
  ---
  duration_ms: 1.538067
  ...
# Subtest: stale target paths keep the picker open with a Notice
ok 462 - stale target paths keep the picker open with a Notice
  ---
  duration_ms: 1.352192
  ...
# Subtest: command opens on a token, a selection, or the caret
ok 463 - command opens on a token, a selection, or the caret
  ---
  duration_ms: 2.46659
  ...
# Subtest: managed-line (( shows that line's guard notice and never opens
ok 464 - managed-line (( shows that line's guard notice and never opens
  ---
  duration_ms: 0.478544
  ...
# Subtest: command in an excluded context shows Task wikilinks can't go here
ok 465 - command in an excluded context shows Task wikilinks can't go here
  ---
  duration_ms: 0.44037
  ...
# Subtest: ^^ marker still opens the per-note picker when (( is absent
ok 466 - ^^ marker still opens the per-note picker when (( is absent
  ---
  duration_ms: 0.65488
  ...
# Subtest: ID-less Enter opens naming mode with the picker state
ok 467 - ID-less Enter opens naming mode with the picker state
  ---
  duration_ms: 8.745046
  ...
# Subtest: Page Down clamps at the final selectable row instead of wrapping
ok 468 - Page Down clamps at the final selectable row instead of wrapping
  ---
  duration_ms: 13.806047
  ...
# Subtest: naming cancel paths restore query, selection, row limit, and scroll
ok 469 - naming cancel paths restore query, selection, row limit, and scroll
  ---
  duration_ms: 2.029885
  ...
# Subtest: a scan that exits early clears old written ranges before a later scan
ok 470 - a scan that exits early clears old written ranges before a later scan
  ---
  duration_ms: 0.431774
  ...
# Subtest: identified accept dispatches one isolated CodeMirror completion event
ok 471 - identified accept dispatches one isolated CodeMirror completion event
  ---
  duration_ms: 0.651825
  ...
# Subtest: guarded rows never open the naming prompt
ok 472 - guarded rows never open the naming prompt
  ---
  duration_ms: 1.407087
  ...
# Subtest: cheap Pomodoro guards disable non-selected duplicate rows
ok 473 - cheap Pomodoro guards disable non-selected duplicate rows
  ---
  duration_ms: 4.275434
  ...
# Subtest: stale Backspace closes with a notice and leaves the changed token alone
ok 474 - stale Backspace closes with a notice and leaves the changed token alone
  ---
  duration_ms: 0.493442
  ...
# Subtest: onEscapeKey clears a non-empty filter first and closes on an empty one
ok 475 - onEscapeKey clears a non-empty filter first and closes on an empty one
  ---
  duration_ms: 0.836567
  ...
# Subtest: empty filter groups This note, In progress, Next, Other open, Hidden, Completed
ok 476 - empty filter groups This note, In progress, Next, Other open, Hidden, Completed
  ---
  duration_ms: 18.764284
  ...
# Subtest: per-note headers expose sticky data, kind icons, and count pills
ok 477 - per-note headers expose sticky data, kind icons, and count pills
  ---
  duration_ms: 0.826648
  ...
# Subtest: row anatomy, locator parts, and action lines cover identified, id-less, and guarded
ok 478 - row anatomy, locator parts, and action lines cover identified, id-less, and guarded
  ---
  duration_ms: 2.083979
  ...
# Subtest: title parts render code, wikilinks, markdown labels, and URL hosts
ok 479 - title parts render code, wikilinks, markdown labels, and URL hosts
  ---
  duration_ms: 0.483243
  ...
# Subtest: counts, empty states, indexing, and footer hints
ok 480 - counts, empty states, indexing, and footer hints
  ---
  duration_ms: 1.158341
  ...
# Subtest: windowing emits 100-row windows and renderAll exhausts
ok 481 - windowing emits 100-row windows and renderAll exhausts
  ---
  duration_ms: 6.352948
  ...
# Subtest: narrow layout keeps basename plus id and drops the backspace hint
ok 482 - narrow layout keeps basename plus id and drops the backspace hint
  ---
  duration_ms: 0.321915
  ...
# Subtest: filtered list is flat with a Completed history divider
ok 483 - filtered list is flat with a Completed history divider
  ---
  duration_ms: 0.334588
  ...
# Subtest: caret-task and unlinkable-path guards disable the row
ok 484 - caret-task and unlinkable-path guards disable the row
  ---
  duration_ms: 0.558266
  ...
# Subtest: card DOM helpers are exported for Chromium previews
ok 485 - card DOM helpers are exported for Chromium previews
  ---
  duration_ms: 0.344768
  ...
# Subtest: Pomodoro (( picker limits the pool to open tasks and shows commit consequences
ok 486 - Pomodoro (( picker limits the pool to open tasks and shows commit consequences
  ---
  duration_ms: 18.631851
  ...
# Subtest: ^^ under an open Pomodoro raises blocked prerequisites, leaves the task unlinked, and reverts the marker
ok 487 - ^^ under an open Pomodoro raises blocked prerequisites, leaves the task unlinked, and reverts the marker
  ---
  duration_ms: 6.415087
  ...
# Subtest: ^^ refuses a project-blocked task without consuming its prerequisites
ok 488 - ^^ refuses a project-blocked task without consuming its prerequisites
  ---
  duration_ms: 0.858729
  ...
# Subtest: ^^ refuses a closed target under an open Pomodoro
ok 489 - ^^ refuses a closed target under an open Pomodoro
  ---
  duration_ms: 0.912983
  ...
# Subtest: (( refuses a \#prj_is_blocked resident without consuming prerequisites
ok 490 - (( refuses a \#prj_is_blocked resident without consuming prerequisites
  ---
  duration_ms: 1.080503
  ...
# Subtest: (( refuses a task inherited-blocked by its \#prj_is_blocked project
ok 491 - (( refuses a task inherited-blocked by its \#prj_is_blocked project
  ---
  duration_ms: 1.050606
  ...
# Subtest: (( refuses a ^prj whose own future date is the sole remaining reason
ok 492 - (( refuses a ^prj whose own future date is the sole remaining reason
  ---
  duration_ms: 0.867686
  ...
# Subtest: ^^ links and promotes an existing-ID task under an open Pomodoro
ok 493 - ^^ links and promotes an existing-ID task under an open Pomodoro
  ---
  duration_ms: 2.184701
  ...
# Subtest: ID-less ^^ names, links, and retains its target alias in Pomodoro mode
ok 494 - ID-less ^^ names, links, and retains its target alias in Pomodoro mode
  ---
  duration_ms: 1.38809
  ...
# Subtest: an unrelated unreadable note does not block a Ready Pomodoro target
ok 495 - an unrelated unreadable note does not block a Ready Pomodoro target
  ---
  duration_ms: 1.112694
  ...
# Subtest: a ^prj blocked only by its own prerequisite raises that prerequisite
ok 496 - a ^prj blocked only by its own prerequisite raises that prerequisite
  ---
  duration_ms: 0.661603
  ...
# Subtest: Pomodoro prerequisite raise pins every promoted task and selects the first
ok 497 - Pomodoro prerequisite raise pins every promoted task and selects the first
  ---
  duration_ms: 2.246701
  ...
# Subtest: the task wikilink Pomodoro preview omits type text when the themes API is absent
ok 498 - the task wikilink Pomodoro preview omits type text when the themes API is absent
  ---
  duration_ms: 0.294903
  ...
# Subtest: Pomodoro commit rechecks the selected task before writing
ok 499 - Pomodoro commit rechecks the selected task before writing
  ---
  duration_ms: 0.2779
  ...
# Subtest: ID-less (( selection names the task and completes through the shared Pomodoro commit
ok 500 - ID-less (( selection names the task and completes through the shared Pomodoro commit
  ---
  duration_ms: 1.514883
  ...
# Subtest: Pomodoro commit merges the task type into the Pomodoro, pulls a future schedule forward, and includes notices
ok 501 - Pomodoro commit merges the task type into the Pomodoro, pulls a future schedule forward, and includes notices
  ---
  duration_ms: 1.415332
  ...
# Subtest: task-wikilink trigger vectors match bob's shared core
ok 502 - task-wikilink trigger vectors match bob's shared core
  ---
  duration_ms: 3.002983
  ...
# Subtest: task-wikilink context vectors allow prose and exclude note-only spans
ok 503 - task-wikilink context vectors allow prose and exclude note-only spans
  ---
  duration_ms: 4.112822
  ...
# Subtest: task-wikilink written-second-paren vectors gate auto-open on user input
ok 504 - task-wikilink written-second-paren vectors gate auto-open on user input
  ---
  duration_ms: 0.318589
  ...
# Subtest: findTaskWikilinkToken rejects unusable caret positions
ok 505 - findTaskWikilinkToken rejects unusable caret positions
  ---
  duration_ms: 0.117364
  ...
# Subtest: taskWikilinkContextAt rejects unusable positions
ok 506 - taskWikilinkContextAt rejects unusable positions
  ---
  duration_ms: 0.143524
  ...
# Subtest: addTaskWikilinkChanges records insertions and maps earlier ranges forward
ok 507 - addTaskWikilinkChanges records insertions and maps earlier ranges forward
  ---
  duration_ms: 0.365538
  ...
# Subtest: addTaskWikilinkChanges accepts the wrapper and CodeMirror spellings
ok 508 - addTaskWikilinkChanges accepts the wrapper and CodeMirror spellings
  ---
  duration_ms: 0.265557
  ...
# Subtest: mapTaskWikilinkRanges maps without recording
ok 509 - mapTaskWikilinkRanges maps without recording
  ---
  duration_ms: 0.158863
  ...
# Subtest: mapTaskWikilinkRanges tolerates array ranges and empty sets
ok 510 - mapTaskWikilinkRanges tolerates array ranges and empty sets
  ---
  duration_ms: 0.378603
  ...
# Subtest: work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
ok 511 - work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
  ---
  duration_ms: 2.851363
  ...
# Subtest: formatWorkLogStamp matches the shared conformance vectors
ok 512 - formatWorkLogStamp matches the shared conformance vectors
  ---
  duration_ms: 0.343857
  ...
# Subtest: work log stamps use local wall-clock components
ok 513 - work log stamps use local wall-clock components
  ---
  duration_ms: 0.182208
  ...
# Subtest: planWorkLogInsertion stamps the injected clock when no stamp is given
ok 514 - planWorkLogInsertion stamps the injected clock when no stamp is given
  ---
  duration_ms: 0.713302
  ...
# Subtest: workSummaryPromptState previews the clock at render time
ok 515 - workSummaryPromptState previews the clock at render time
  ---
  duration_ms: 0.161659
  ...
# Subtest: planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
ok 516 - planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
  ---
  duration_ms: 0.249567
  ...
# Subtest: planWorkLogInsertion inherits an existing space-indented child prefix
ok 517 - planWorkLogInsertion inherits an existing space-indented child prefix
  ---
  duration_ms: 0.525743
  ...
# Subtest: planWorkLogInsertion inherits an existing tab-indented child prefix
ok 518 - planWorkLogInsertion inherits an existing tab-indented child prefix
  ---
  duration_ms: 0.228917
  ...
# Subtest: planWorkLogInsertion prepends newest-first entries into existing marker spellings
ok 519 - planWorkLogInsertion prepends newest-first entries into existing marker spellings
  ---
  duration_ms: 0.905239
  ...
# Subtest: planWorkLogInsertion ignores nested child-task markers and preserves CRLF
ok 520 - planWorkLogInsertion ignores nested child-task markers and preserves CRLF
  ---
  duration_ms: 0.667004
  ...
# Subtest: planWorkLogInsertion treats blank summaries as no-op structural edits
ok 521 - planWorkLogInsertion treats blank summaries as no-op structural edits
  ---
  duration_ms: 0.181667
  ...
# Subtest: the Open-reset planner is removed: unlink plans only a Work Log insertion
ok 522 - the Open-reset planner is removed: unlink plans only a Work Log insertion
  ---
  duration_ms: 0.095693
  ...
# Subtest: unlink Work Log plan keeps the In Progress checkbox and appends one entry
ok 523 - unlink Work Log plan keeps the In Progress checkbox and appends one entry
  ---
  duration_ms: 0.134877
  ...
# Subtest: article detection accepts scalar and list frontmatter values
ok 524 - article detection accepts scalar and list frontmatter values
  ---
  duration_ms: 1.294061
  ...
# Subtest: bob resolution prefers its setting, then known install paths, then PATH
ok 525 - bob resolution prefers its setting, then known install paths, then PATH
  ---
  duration_ms: 0.700488
  ...
# Subtest: plan decoder accepts v1 and rejects a foreign schema version
ok 526 - plan decoder accepts v1 and rejects a foreign schema version
  ---
  duration_ms: 0.273542
  ...
# Subtest: bob stdin spawn passes the article contract and vault environment
ok 527 - bob stdin spawn passes the article contract and vault environment
  ---
  duration_ms: 2.218856
  ...
# Subtest: bob plan stdout decodes UTF-8 split across chunks
ok 528 - bob plan stdout decodes UTF-8 split across chunks
  ---
  duration_ms: 0.779599
  ...
# Subtest: early bob exit on stdin reports EPIPE as a run failure
ok 529 - early bob exit on stdin reports EPIPE as a run failure
  ---
  duration_ms: 0.655642
  ...
# Subtest: line hunks become minimal cursor-preserving changes
ok 530 - line hunks become minimal cursor-preserving changes
  ---
  duration_ms: 0.56058
  ...
# Subtest: insert, multi-line replace, and deletion hunks reproduce the formatted note
ok 531 - insert, multi-line replace, and deletion hunks reproduce the formatted note
  ---
  duration_ms: 2.764688
  ...
# Subtest: notice shows bob's text and at most two warning findings
ok 532 - notice shows bob's text and at most two warning findings
  ---
  duration_ms: 0.519221
  ...
# Subtest: inbound changes apply only when their target line still matches the preimage
ok 533 - inbound changes apply only when their target line still matches the preimage
  ---
  duration_ms: 0.808043
  ...
# Subtest: undo guard blocks a reformat until a fresh input or delete event
ok 534 - undo guard blocks a reformat until a fresh input or delete event
  ---
  duration_ms: 0.39768
  ...
# Subtest: leave formatting observes the undo guard before saving or reading
ok 535 - leave formatting observes the undo guard before saving or reading
  ---
  duration_ms: 0.254777
  ...
# Subtest: Convert shows bob's refusal on every invocation
ok 536 - Convert shows bob's refusal on every invocation
  ---
  duration_ms: 0.269564
  ...
# Subtest: old bob's non-JSON article response gets one update notice per session
ok 537 - old bob's non-JSON article response gets one update notice per session
  ---
  duration_ms: 0.157641
  ...
# Subtest: format drops its response if the editor changed while bob was running
ok 538 - format drops its response if the editor changed while bob was running
  ---
  duration_ms: 0.295404
  ...
# Subtest: decoration ranges mark written section numbers from the outline
ok 539 - decoration ranges mark written section numbers from the outline
  ---
  duration_ms: 0.636686
  ...
# Subtest: a new outline rerenders each open Reading view once for that generation
ok 540 - a new outline rerenders each open Reading view once for that generation
  ---
  duration_ms: 0.291687
  ...
# Subtest: section at a given line uses the innermost outline range
ok 541 - section at a given line uses the innermost outline range
  ---
  duration_ms: 0.265487
  ...
# Subtest: stale-hint debounce and in-flight state machine
ok 542 - stale-hint debounce and in-flight state machine
  ---
  duration_ms: 0.275175
  ...
# Subtest: reading-view wrapping puts the leading number token in span.bob-secno
ok 543 - reading-view wrapping puts the leading number token in span.bob-secno
  ---
  duration_ms: 1.114087
  ...
# Subtest: applied plans remap outline lines onto the formatted buffer
ok 544 - applied plans remap outline lines onto the formatted buffer
  ---
  duration_ms: 0.117545
  ...
# Subtest: article styles scope the reading look under .bob-article
ok 545 - article styles scope the reading look under .bob-article
  ---
  duration_ms: 0.524992
  ...
# Subtest: look settings default to serif typeface and stale-number hints
ok 546 - look settings default to serif typeface and stale-number hints
  ---
  duration_ms: 0.102335
  ...
# Subtest: catalog carries category and CLDR keywords
ok 547 - catalog carries category and CLDR keywords
  ---
  duration_ms: 4.217402
  ...
# Subtest: tiered ranking regression set
ok 548 - tiered ranking regression set
  ---
  duration_ms: 87.217155
  ...
# Subtest: multi-token AND, boost stays within tier, and VS16-insensitive glyphs
ok 549 - multi-token AND, boost stays within tier, and VS16-insensitive glyphs
  ---
  duration_ms: 48.851896
  ...
# Subtest: suggestForLabel examples
ok 550 - suggestForLabel examples
  ---
  duration_ms: 6.664714
  ...
# Subtest: api v1 is frozen, total, and shares recents
ok 551 - api v1 is frozen, total, and shares recents
  ---
  duration_ms: 41.509228
  ...
# Subtest: api exists without EditorSuggest
ok 552 - api exists without EditorSuggest
  ---
  duration_ms: 7.952503
  ...
# Subtest: generated catalog exactly matches the vendored gemoji database
ok 553 - generated catalog exactly matches the vendored gemoji database
  ---
  duration_ms: 105.343388
  ...
# Subtest: catalog integrity and popular aliases
ok 554 - catalog integrity and popular aliases
  ---
  duration_ms: 3.878084
  ...
# Subtest: query normalization, alias ranking, tags, descriptions, and recents
ok 555 - query normalization, alias ranking, tags, descriptions, and recents
  ---
  duration_ms: 34.62235
  ...
# Subtest: empty query puts newest recents before popular entries and deduplicates
ok 556 - empty query puts newest recents before popular entries and deduplicates
  ---
  duration_ms: 0.305664
  ...
# Subtest: recent history deduplicates by alias and caps at thirty
ok 557 - recent history deduplicates by alias and caps at thirty
  ---
  duration_ms: 1.9119
  ...
# Subtest: renderSuggestion builds styled glyph, shortcode, hint, and match nodes
ok 558 - renderSuggestion builds styled glyph, shortcode, hint, and match nodes
  ---
  duration_ms: 37.568094
  ...
# Subtest: selection replaces the stored range with the emoji, saves recents, and closes
ok 559 - selection replaces the stored range with the emoji, saves recents, and closes
  ---
  duration_ms: 25.438397
  ...
# Subtest: missing and corrupt plugin data reset recents safely; valid recents persist
ok 560 - missing and corrupt plugin data reset recents safely; valid recents persist
  ---
  duration_ms: 50.323416
  ...
# Subtest: trigger opens at line start and after whitespace, including a bare colon
ok 561 - trigger opens at line start and after whitespace, including a bare colon
  ---
  duration_ms: 1.694735
  ...
# Subtest: trigger excludes mid-word, clock, dataview, doubled, and punctuated colons
ok 562 - trigger excludes mid-word, clock, dataview, doubled, and punctuated colons
  ---
  duration_ms: 0.282459
  ...
# Subtest: closing colon remains literal and does not autocommit
ok 563 - closing colon remains literal and does not autocommit
  ---
  duration_ms: 0.128445
  ...
# Subtest: syntax tree guards code, math, comments, and frontmatter
ok 564 - syntax tree guards code, math, comments, and frontmatter
  ---
  duration_ms: 0.281808
  ...
# Subtest: missing or failing syntax APIs allow the trigger
ok 565 - missing or failing syntax APIs allow the trigger
  ---
  duration_ms: 0.313959
  ...
# Subtest: banner date accepts the saved line and the rendered text
ok 566 - banner date accepts the saved line and the rendered text
  ---
  duration_ms: 1.198628
  ...
# Subtest: banner date rejects hostile subjects and malformed dates
ok 567 - banner date rejects hostile subjects and malformed dates
  ---
  duration_ms: 0.206023
  ...
# Subtest: trusted spans need the exact markers in order
ok 568 - trusted spans need the exact markers in order
  ---
  duration_ms: 0.668867
  ...
# Subtest: fake banners without markers and damaged spans stay untrusted
ok 569 - fake banners without markers and damaged spans stay untrusted
  ---
  duration_ms: 0.271508
  ...
# Subtest: unarchive argv pins the exact note behind -- with JSON output
ok 570 - unarchive argv pins the exact note behind -- with JSON output
  ---
  duration_ms: 0.154525
  ...
# Subtest: list decoding maps receipts per note and confirms empty arrays
ok 571 - list decoding maps receipts per note and confirms empty arrays
  ---
  duration_ms: 0.326673
  ...
# Subtest: list decoding never fabricates ownership from malformed rows
ok 572 - list decoding never fabricates ownership from malformed rows
  ---
  duration_ms: 0.221994
  ...
# Subtest: per-note state distinguishes receipts, none, and unavailable
ok 573 - per-note state distinguishes receipts, none, and unavailable
  ---
  duration_ms: 0.218537
  ...
# Subtest: cache refresh coalesces concurrent callers into one list call
ok 574 - cache refresh coalesces concurrent callers into one list call
  ---
  duration_ms: 0.558306
  ...
# Subtest: cache refresh settles old-bob and failures without throwing
ok 575 - cache refresh settles old-bob and failures without throwing
  ---
  duration_ms: 0.561321
  ...
# Subtest: tooltip names the exact count and label, never guesses
ok 576 - tooltip names the exact count and label, never guesses
  ---
  duration_ms: 0.327906
  ...
# Subtest: undo outcomes match the exact note, then input, then a single row
ok 577 - undo outcomes match the exact note, then input, then a single row
  ---
  duration_ms: 0.358374
  ...
# Subtest: banner element uses text APIs and reports clicks once
ok 578 - banner element uses text APIs and reports clicks once
  ---
  duration_ms: 0.45061
  ...
# Subtest: reading view enhances the trusted banner with one undo button
ok 579 - reading view enhances the trusted banner with one undo button
  ---
  duration_ms: 23.708905
  ...
# Subtest: reading view leaves fakes, damage, and non-mail notes inert
ok 580 - reading view leaves fakes, damage, and non-mail notes inert
  ---
  duration_ms: 21.160608
  ...
# Subtest: reading sweep removes the button once the banner is gone
ok 581 - reading sweep removes the button once the banner is gone
  ---
  duration_ms: 21.577366
  ...
# Subtest: banner click runs one exact unarchive, ignores doubles, then reloads state
ok 582 - banner click runs one exact unarchive, ignores doubles, then reloads state
  ---
  duration_ms: 1.507338
  ...
# Subtest: banner click surfaces unchanged and failed outcomes without guessing
ok 583 - banner click surfaces unchanged and failed outcomes without guessing
  ---
  duration_ms: 0.723742
  ...
# Subtest: reading sweep on an unloaded cache fires one coalesced snapshot
ok 584 - reading sweep on an unloaded cache fires one coalesced snapshot
  ---
  duration_ms: 41.31088
  ...
# Subtest: live preview decorates the trusted banner line and nothing else
ok 585 - live preview decorates the trusted banner line and nothing else
  ---
  duration_ms: 1.046107
  ...
# Subtest: live extension registers once and refreshes on the shared effect
ok 586 - live extension registers once and refreshes on the shared effect
  ---
  duration_ms: 0.275576
  ...
# Subtest: shared cache api serves plain JSON for ledger tools
ok 587 - shared cache api serves plain JSON for ledger tools
  ---
  duration_ms: 0.428848
  ...
# Subtest: shared cache api notifies Ledger Tools after a completed snapshot refresh
ok 588 - shared cache api notifies Ledger Tools after a completed snapshot refresh
  ---
  duration_ms: 0.250969
  ...
# Subtest: unload clears banner hosts, views, and pending bits
ok 589 - unload clears banner hosts, views, and pending bits
  ---
  duration_ms: 21.310316
  ...
# Subtest: compose arg builders match the bob gmail CLI contract
ok 590 - compose arg builders match the bob gmail CLI contract
  ---
  duration_ms: 1.274142
  ...
# Subtest: preview and error payload helpers classify bob documents
ok 591 - preview and error payload helpers classify bob documents
  ---
  duration_ms: 0.554299
  ...
# Subtest: the send modal renders the exact preview from fixture JSON
ok 592 - the send modal renders the exact preview from fixture JSON
  ---
  duration_ms: 1.074381
  ...
# Subtest: undo cancels the send before bob is called
ok 593 - undo cancels the send before bob is called
  ---
  duration_ms: 0.751675
  ...
# Subtest: a second send is ignored while one is in flight, and the digest passes through
ok 594 - a second send is ignored while one is in flight, and the digest passes through
  ---
  duration_ms: 5.015756
  ...
# Subtest: a digest mismatch re-previews instead of sending
ok 595 - a digest mismatch re-previews instead of sending
  ---
  duration_ms: 0.452133
  ...
# Subtest: the send modal ignores a double click on Send
ok 596 - the send modal ignores a double click on Send
  ---
  duration_ms: 1.39892
  ...
# Subtest: compose commands appear only with a mail-note context, except New email
ok 597 - compose commands appear only with a mail-note context, except New email
  ---
  duration_ms: 0.987345
  ...
# Subtest: picker insertion uses a rechecked editor transaction and aborts stale buffers
ok 598 - picker insertion uses a rechecked editor transaction and aborts stale buffers
  ---
  duration_ms: 3.02741
  ...
# Subtest: paste conversion replaces only an unchanged Gmail URL in the original view and file
ok 599 - paste conversion replaces only an unchanged Gmail URL in the original view and file
  ---
  duration_ms: 0.911831
  ...
# Subtest: a failed save leaves a pasted Gmail URL untouched
ok 600 - a failed save leaves a pasted Gmail URL untouched
  ---
  duration_ms: 0.53414
  ...
# Subtest: old Bob shows one update notice
ok 601 - old Bob shows one update notice
  ---
  duration_ms: 0.980933
  ...
# Subtest: commands appear according to mail-note context
ok 602 - commands appear according to mail-note context
  ---
  duration_ms: 1.702872
  ...
# Subtest: a mail URL under the cursor exposes the email context
ok 603 - a mail URL under the cursor exposes the email context
  ---
  duration_ms: 0.509212
  ...
# Subtest: line-borne context works anywhere on the line and ignores task status
ok 604 - line-borne context works anywhere on the line and ignores task status
  ---
  duration_ms: 0.813183
  ...
# Subtest: child hop opens from the task row through a link-only child
ok 605 - child hop opens from the task row through a link-only child
  ---
  duration_ms: 0.562264
  ...
# Subtest: code, non-mail links, and bad URLs stay silent
ok 606 - code, non-mail links, and bad URLs stay silent
  ---
  duration_ms: 0.732398
  ...
# Subtest: first mail link wins and own links beat the child hop
ok 607 - first mail link wins and own links beat the child hop
  ---
  duration_ms: 0.600045
  ...
# Subtest: inside a mail note the whole-note fallback still opens
ok 608 - inside a mail note the whole-note fallback still opens
  ---
  duration_ms: 0.238746
  ...
# Subtest: vim Cmd+Enter mapping registers once and opens exactly gmail_url
ok 609 - vim Cmd+Enter mapping registers once and opens exactly gmail_url
  ---
  duration_ms: 0.764239
  ...
# Subtest: vim registration fails closed without an adapter
ok 610 - vim registration fails closed without an adapter
  ---
  duration_ms: 0.189923
  ...
# Subtest: task links point to the message block under the cursor
ok 611 - task links point to the message block under the cursor
  ---
  duration_ms: 0.448025
  ...
# Subtest: task-link hop opens the Gmail thread from the daily-note bullet
ok 612 - task-link hop opens the Gmail thread from the daily-note bullet
  ---
  duration_ms: 0.669769
  ...
# Subtest: task-link hop rejects multi-link, embed, struck, and non-gmail targets
ok 613 - task-link hop rejects multi-link, embed, struck, and non-gmail targets
  ---
  duration_ms: 1.637656
  ...
# Subtest: task-link hop supports hop-then-child-hop targets
ok 614 - task-link hop supports hop-then-child-hop targets
  ---
  duration_ms: 0.262711
  ...
# Subtest: mailOpen api v1 opens at the cursor and degrades to false
ok 615 - mailOpen api v1 opens at the cursor and degrades to false
  ---
  duration_ms: 0.688044
  ...
# Subtest: Edit album schema is a Vault surface row behind the palette command
ok 616 - Edit album schema is a Vault surface row behind the palette command
  ---
  duration_ms: 0.910037
  ...
# Subtest: missing plugin disables the surface row with an enable hint
ok 617 - missing plugin disables the surface row with an enable hint
  ---
  duration_ms: 1.329178
  ...
# Subtest: Command Mode executes the album schema surface through Obsidian's command route
ok 618 - Command Mode executes the album schema surface through Obsidian's command route
  ---
  duration_ms: 0.925598
  ...
# Subtest: typed argv tokenizer handles quotes, escapes, literal shell syntax, and errors
ok 619 - typed argv tokenizer handles quotes, escapes, literal shell syntax, and errors
  ---
  duration_ms: 1.661371
  ...
# Subtest: typed argv resolves aliases to the longest catalog entry and refuses excluded paths
ok 620 - typed argv resolves aliases to the longest catalog entry and refuses excluded paths
  ---
  duration_ms: 0.698092
  ...
# Subtest: the list pins typed metadata, disabled exclusions, and the explicit Vim fallback
ok 621 - the list pins typed metadata, disabled exclusions, and the explicit Vim fallback
  ---
  duration_ms: 9.49038
  ...
# Subtest: typed runs pass the catalog title to the run record
ok 622 - typed runs pass the catalog title to the run record
  ---
  duration_ms: 2.718219
  ...
# Subtest: Vim-shaped input follows the agreed positive and negative rules
ok 623 - Vim-shaped input follows the agreed positive and negative rules
  ---
  duration_ms: 0.193109
  ...
# Subtest: vimrc parser finds recursive colon mappings and exmap names
ok 624 - vimrc parser finds recursive colon mappings and exmap names
  ---
  duration_ms: 0.453876
  ...
# Subtest: argument completion passes the entry path, fixed args, and current tokens to bob
ok 625 - argument completion passes the entry path, fixed args, and current tokens to bob
  ---
  duration_ms: 6.770155
  ...
# Subtest: completion directives group candidates, preserve prefixes, and expand vault paths
ok 626 - completion directives group candidates, preserve prefixes, and expand vault paths
  ---
  duration_ms: 8.677527
  ...
# Subtest: stale completion replies are discarded and Enter reports missing required positionals
ok 627 - stale completion replies are discarded and Enter reports missing required positionals
  ---
  duration_ms: 12.846617
  ...
# Subtest: argument completion requests debounce edits by 60 ms
ok 628 - argument completion requests debounce edits by 60 ms
  ---
  duration_ms: 95.467654
  ...
# Subtest: Vim ex dispatch restores and targets the editor captured when the sheet opened
ok 629 - Vim ex dispatch restores and targets the editor captured when the sheet opened
  ---
  duration_ms: 3.306332
  ...
# Subtest: double colon enters Vim stage and Escape returns to the list
ok 630 - double colon enters Vim stage and Escape returns to the list
  ---
  duration_ms: 4.051455
  ...
# Subtest: vimrc lint reads the configured file and shows only one session notice
ok 631 - vimrc lint reads the configured file and shows only one session notice
  ---
  duration_ms: 1.409792
  ...
# Subtest: Edit bank setup is a Vault surface row behind the palette command
ok 632 - Edit bank setup is a Vault surface row behind the palette command
  ---
  duration_ms: 0.847598
  ...
# Subtest: missing ledger-tools plugin disables Edit bank setup with an enable hint
ok 633 - missing ledger-tools plugin disables Edit bank setup with an enable hint
  ---
  duration_ms: 1.123104
  ...
# Subtest: Command Mode runs Edit bank setup through Obsidian's command route
ok 634 - Command Mode runs Edit bank setup through Obsidian's command route
  ---
  duration_ms: 0.829524
  ...
# Subtest: fingerprints compare path, mtime, and size
ok 635 - fingerprints compare path, mtime, and size
  ---
  duration_ms: 2.185162
  ...
# Subtest: validation accepts the fixture and rejects malformed catalogs
ok 636 - validation accepts the fixture and rejects malformed catalogs
  ---
  duration_ms: 0.300975
  ...
# Subtest: refresh fetches and validates through the real protocol
ok 637 - refresh fetches and validates through the real protocol
  ---
  duration_ms: 140.807846
  ...
# Subtest: lookup resolves entries, aliases of entries, and excluded paths
ok 638 - lookup resolves entries, aliases of entries, and excluded paths
  ---
  duration_ms: 0.494464
  ...
# Subtest: argv assembly puts preview args before fixed args
ok 639 - argv assembly puts preview args before fixed args
  ---
  duration_ms: 0.292478
  ...
# Subtest: cmRecordArgs strips a leading bob binary and leaves queued argv
ok 640 - cmRecordArgs strips a leading bob binary and leaves queued argv
  ---
  duration_ms: 0.626246
  ...
# Subtest: cmReplayRun is the inverse of cmAssembleArgv
ok 641 - cmReplayRun is the inverse of cmAssembleArgv
  ---
  duration_ms: 0.484395
  ...
# Subtest: palette entries need policy run and all-optional positionals
ok 642 - palette entries need policy run and all-optional positionals
  ---
  duration_ms: 0.189963
  ...
# Subtest: classification order: stop, spawn, timeout, signal
ok 643 - classification order: stop, spawn, timeout, signal
  ---
  duration_ms: 1.898935
  ...
# Subtest: lock phrase wins over exit codes and adapters
ok 644 - lock phrase wins over exit codes and adapters
  ---
  duration_ms: 0.214088
  ...
# Subtest: exit-code hints beat the generic rule; unknown ids are ignored
ok 645 - exit-code hints beat the generic rule; unknown ids are ignored
  ---
  duration_ms: 0.154715
  ...
# Subtest: adapters adjust the result; failures stay honest
ok 646 - adapters adjust the result; failures stay honest
  ---
  duration_ms: 0.986744
  ...
# Subtest: gcal-sync summarizes added Event Tasks, context, and MEET links
ok 647 - gcal-sync summarizes added Event Tasks, context, and MEET links
  ---
  duration_ms: 0.400264
  ...
# Subtest: gcal-sync reports unchanged and waiting outcomes
ok 648 - gcal-sync reports unchanged and waiting outcomes
  ---
  duration_ms: 0.27744
  ...
# Subtest: api.commandMode settles, never rejects, and fires the workspace event
ok 649 - api.commandMode settles, never rejects, and fires the workspace event
  ---
  duration_ms: 709.69222
  ...
# Subtest: plugin onload registers run-* commands and exposes the frozen api
ok 650 - plugin onload registers run-* commands and exposes the frozen api
  ---
  duration_ms: 1225.356625
  ...
# Subtest: plugin reports missing-bob when the binary is absent
ok 651 - plugin reports missing-bob when the binary is absent
  ---
  duration_ms: 0.791952
  ...
# Subtest: runner notifies with a plain summary after each finish
ok 652 - runner notifies with a plain summary after each finish
  ---
  duration_ms: 64.541482
  ...
# Subtest: catalog outcome adapters cover command-specific results and actions
ok 653 - catalog outcome adapters cover command-specific results and actions
  ---
  duration_ms: 2.089158
  ...
# Subtest: toast classes have distinct timing and newer failures replace older cards
ok 654 - toast classes have distinct timing and newer failures replace older cards
  ---
  duration_ms: 3.258221
  ...
# Subtest: status chip waits 400 ms, tracks multiple runs, and marks overdue writers
ok 655 - status chip waits 400 ms, tracks multiple runs, and marks overdue writers
  ---
  duration_ms: 1.3564
  ...
# Subtest: OS notifications only fire for long runs while Obsidian is unfocused
ok 656 - OS notifications only fire for long runs while Obsidian is unfocused
  ---
  duration_ms: 0.321634
  ...
# Subtest: rerun-last preserves arguments and preview mode; Apply carries the replay seed
ok 657 - rerun-last preserves arguments and preview mode; Apply carries the replay seed
  ---
  duration_ms: 1.66554
  ...
# Subtest: commandModeRerun retries an applied preview-first run and Apply carries the seed
ok 658 - commandModeRerun retries an applied preview-first run and Apply carries the seed
  ---
  duration_ms: 3319.308575
  ...
# Subtest: ANSI parsing keeps SGR that splits across chunks
ok 659 - ANSI parsing keeps SGR that splits across chunks
  ---
  duration_ms: 2.626995
  ...
# Subtest: linkify positives resolve and negatives stay plain
ok 660 - linkify positives resolve and negatives stay plain
  ---
  duration_ms: 1.008335
  ...
# Subtest: JSON pretty-print mutes keys on a single document
ok 661 - JSON pretty-print mutes keys on a single document
  ---
  duration_ms: 0.864631
  ...
# Subtest: interleave replay preserves arrival order for copy
ok 662 - interleave replay preserves arrival order for copy
  ---
  duration_ms: 0.533538
  ...
# Subtest: stamped sequence runs add a step label to the pager header
ok 663 - stamped sequence runs add a step label to the pager header
  ---
  duration_ms: 1.824443
  ...
# Subtest: pager keys: scroll, wrap, search, copy, history, stop, close
ok 664 - pager keys: scroll, wrap, search, copy, history, stop, close
  ---
  duration_ms: 0.676712
  ...
# Subtest: history stepping is newest-first
ok 665 - history stepping is newest-first
  ---
  duration_ms: 0.164985
  ...
# Subtest: search matches are exact and advance
ok 666 - search matches are exact and advance
  ---
  duration_ms: 0.175175
  ...
# Subtest: status pill covers running, outcomes, and queued-behind
ok 667 - status pill covers running, outcomes, and queued-behind
  ---
  duration_ms: 0.414431
  ...
# Subtest: plugin pager opens from Output, show-last-output, history, copy, and stop
ok 668 - plugin pager opens from Output, show-last-output, history, copy, and stop
  ---
  duration_ms: 16.618969
  ...
# Subtest: writer stop needs confirmation; reads stop immediately
ok 669 - writer stop needs confirmation; reads stop immediately
  ---
  duration_ms: 2.327583
  ...
# Subtest: watching a run skips the toast
ok 670 - watching a run skips the toast
  ---
  duration_ms: 1.431503
  ...
# Subtest: pretty JSON and ANSI land in the pager body
ok 671 - pretty JSON and ANSI land in the pager body
  ---
  duration_ms: 1.103237
  ...
# Subtest: resolver prefers the explicit setting and expands home
ok 672 - resolver prefers the explicit setting and expands home
  ---
  duration_ms: 2.132181
  ...
# Subtest: resolver consults ledger-tools before the candidates
ok 673 - resolver consults ledger-tools before the candidates
  ---
  duration_ms: 0.221993
  ...
# Subtest: resolver walks candidates, records every path tried, then PATH
ok 674 - resolver walks candidates, records every path tried, then PATH
  ---
  duration_ms: 0.221092
  ...
# Subtest: child env points at the vault, honors features, and drops completion vars
ok 675 - child env points at the vault, honors features, and drops completion vars
  ---
  duration_ms: 0.363453
  ...
# Subtest: inherited NO_COLOR wins; without the color feature NO_COLOR is set
ok 676 - inherited NO_COLOR wins; without the color feature NO_COLOR is set
  ---
  duration_ms: 0.184793
  ...
# Subtest: vault base requires a local folder
ok 677 - vault base requires a local folder
  ---
  duration_ms: 0.188971
  ...
# Subtest: ansi stripping, quoting, durations, and run ids
ok 678 - ansi stripping, quoting, durations, and run ids
  ---
  duration_ms: 0.567493
  ...
# Subtest: completed read writes files, receipt, and an honest record
ok 679 - completed read writes files, receipt, and an honest record
  ---
  duration_ms: 231.289352
  ...
# Subtest: child env carries vault, features, receipt, and tool paths
ok 680 - child env carries vault, features, receipt, and tool paths
  ---
  duration_ms: 2115.074296
  ...
# Subtest: literal args with spaces, quotes, and $() stay literal
ok 681 - literal args with spaces, quotes, and $() stay literal
  ---
  duration_ms: 359.75623
  ...
# Subtest: split multi-byte characters survive and big output stays intact
ok 682 - split multi-byte characters survive and big output stays intact
  ---
  duration_ms: 873.926672
  ...
# Subtest: in-memory text truncates past the cap while files keep everything
ok 683 - in-memory text truncates past the cap while files keep everything
  ---
  duration_ms: 71.00415
  ...
# Subtest: a double run is one run: duplicates share the settlement
ok 684 - a double run is one run: duplicates share the settlement
  ---
  duration_ms: 1472.450222
  ...
# Subtest: writers serialize FIFO while reads run in parallel
ok 685 - writers serialize FIFO while reads run in parallel
  ---
  duration_ms: 5250.192111
  ...
# Subtest: a failed save refuses the writer
ok 686 - a failed save refuses the writer
  ---
  duration_ms: 22.040312
  ...
# Subtest: read budgets kill; writer budgets mark overdue; stop stops
ok 687 - read budgets kill; writer budgets mark overdue; stop stops
  ---
  duration_ms: 3910.024533
  ...
# Subtest: failures classify: non-zero, signals, lock, and missing bob
ok 688 - failures classify: non-zero, signals, lock, and missing bob
  ---
  duration_ms: 3334.909233
  ...
# Subtest: policy and entry guards refuse with reasons
ok 689 - policy and entry guards refuse with reasons
  ---
  duration_ms: 1483.649114
  ...
# Subtest: retention keeps the newest fifty and never an unfinished run
ok 690 - retention keeps the newest fifty and never an unfinished run
  ---
  duration_ms: 202.773272
  ...
# Subtest: adoption finalizes from receipts and reports unknown without one
ok 691 - adoption finalizes from receipts and reports unknown without one
  ---
  duration_ms: 6.205928
  ...
# Subtest: cmNewRecord copies a sanitized sequence stamp and omits the field otherwise
ok 692 - cmNewRecord copies a sanitized sequence stamp and omits the field otherwise
  ---
  duration_ms: 1.75972
  ...
# Subtest: step display, title, copy text, guards, continues, and focus run
ok 693 - step display, title, copy text, guards, continues, and focus run
  ---
  duration_ms: 1.012503
  ...
# Subtest: history groups by id, newest record per index wins, and states include interrupted
ok 694 - history groups by id, newest record per index wins, and states include interrupted
  ---
  duration_ms: 0.994148
  ...
# Subtest: cmRunSequence runs reads in order, stamps every record, and survives throwing hooks
not ok 695 - cmRunSequence runs reads in order, stamps every record, and survives throwing hooks
  ---
  duration_ms: 2793.978276
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-command-mode-sequence-engine.cjs:228:1'
  failureType: 'testCodeFailure'
  error: |-
    Expected values to be strictly equal:
    
    3 !== 1
    
  code: 'ERR_ASSERTION'
  name: 'AssertionError'
  expected: 1
  actual: 3
  operator: 'strictEqual'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-command-mode-sequence-engine.cjs:252:14)
    process.processTicksAndRejections (node:internal/process/task_queues:105:5)
    async Test.run (node:internal/test_runner/test:980:9)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: a failing step 2 halts the sequence and skips later steps
ok 696 - a failing step 2 halts the sequence and skips later steps
  ---
  duration_ms: 1380.954371
  ...
# Subtest: attention continues the sequence
ok 697 - attention continues the sequence
  ---
  duration_ms: 3003.723068
  ...
# Subtest: an early saveAllMarkdown refusal halts with its reason
ok 698 - an early saveAllMarkdown refusal halts with its reason
  ---
  duration_ms: 2232.975593
  ...
# Subtest: a stale entry_id falls back to argv
ok 699 - a stale entry_id falls back to argv
  ---
  duration_ms: 2260.299237
  ...
# Subtest: resume reuses the id and history folds into one group
not ok 700 - resume reuses the id and history folds into one group
  ---
  duration_ms: 6174.88442
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-command-mode-sequence-engine.cjs:346:1'
  failureType: 'testCodeFailure'
  error: |-
    Expected values to be strictly equal:
    + actual - expected
    
    + 'failed'
    - 'completed'
    
  code: 'ERR_ASSERTION'
  name: 'AssertionError'
  expected: 'completed'
  actual: 'failed'
  operator: 'strictEqual'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins/scripts/test-command-mode-sequence-engine.cjs:371:12)
    process.processTicksAndRejections (node:internal/process/task_queues:105:5)
    async Test.run (node:internal/test_runner/test:980:9)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: cancelled() stops before the next step
ok 701 - cancelled() stops before the next step
  ---
  duration_ms: 583.283314
  ...
# Subtest: plugin suppresses per-step toasts and skips chip settle for an active sequence
ok 702 - plugin suppresses per-step toasts and skips chip settle for an active sequence
  ---
  duration_ms: 1375.932955
  ...
# Subtest: duplicate signatures are refused and rerun-last replays a stamped newest record
ok 703 - duplicate signatures are refused and rerun-last replays a stamped newest record
  ---
  duration_ms: 1248.238373
  ...
# Subtest: rerun-last command callback points at commandModeRerunLast
ok 704 - rerun-last command callback points at commandModeRerunLast
  ---
  duration_ms: 17.588683
  ...
# Subtest: summary model covers completed, attention, halted, and stopped sequences
ok 705 - summary model covers completed, attention, halted, and stopped sequences
  ---
  duration_ms: 4.119154
  ...
# Subtest: summary card renders accessible rows and routes the body to its focus run
ok 706 - summary card renders accessible rows and routes the body to its focus run
  ---
  duration_ms: 0.933522
  ...
# Subtest: resume keeps the sequence id and skips completed steps; rerun gets a new id
ok 707 - resume keeps the sequence id and skips completed steps; rerun gets a new id
  ---
  duration_ms: 3.298467
  ...
# Subtest: Output opens the focus run and Copy writes the sequence shell line
ok 708 - Output opens the focus run and Copy writes the sequence shell line
  ---
  duration_ms: 0.516036
  ...
# Subtest: a repeated sticky sequence card replaces the previous card by signature
ok 709 - a repeated sticky sequence card replaces the previous card by signature
  ---
  duration_ms: 0.859371
  ...
# Subtest: three Ctrl+N presses move three rows, keep focus, and wrap
ok 710 - three Ctrl+N presses move three rows, keep focus, and wrap
  ---
  duration_ms: 18.816625
  ...
# Subtest: Caps Lock and layout variants navigate; Ctrl+Shift+N does not
ok 711 - Caps Lock and layout variants navigate; Ctrl+Shift+N does not
  ---
  duration_ms: 58.181118
  ...
# Subtest: Ctrl+[ matches Escape in list, args, vim, confirm, and output
ok 712 - Ctrl+[ matches Escape in list, args, vim, confirm, and output
  ---
  duration_ms: 11.83204
  ...
# Subtest: standalone pager Ctrl+[ behaves like Escape
ok 713 - standalone pager Ctrl+[ behaves like Escape
  ---
  duration_ms: 38.528577
  ...
# Subtest: focus and caret survive re-renders with scroll preserved on same query
ok 714 - focus and caret survive re-renders with scroll preserved on same query
  ---
  duration_ms: 4.227783
  ...
# Subtest: argument mode walks rendered order and Tab accepts the visible first row
ok 715 - argument mode walks rendered order and Tab accepts the visible first row
  ---
  duration_ms: 3.56201
  ...
# Subtest: Tab enters argument mode from entry and typed rows through the modal keydown listener
ok 716 - Tab enters argument mode from entry and typed rows through the modal keydown listener
  ---
  duration_ms: 2.970972
  ...
# Subtest: Tab on an eligible single-run RECENT row prefills its recorded arguments
ok 717 - Tab on an eligible single-run RECENT row prefills its recorded arguments
  ---
  duration_ms: 4.251386
  ...
# Subtest: Tab hints on surfaces, plain rows, sequence recents, and unmapped recents
ok 718 - Tab hints on surfaces, plain rows, sequence recents, and unmapped recents
  ---
  duration_ms: 28.112082
  ...
# Subtest: row mousedown is defaultPrevented and scope fallback routes body keys once
ok 719 - row mousedown is defaultPrevented and scope fallback routes body keys once
  ---
  duration_ms: 3.948599
  ...
# Subtest: Ctrl+M marks with Caps Lock and layout; Ctrl+Shift+M is ignored
ok 720 - Ctrl+M marks with Caps Lock and layout; Ctrl+Shift+M is ignored
  ---
  duration_ms: 16.585104
  ...
# Subtest: Ctrl+[ clears pending marks like Escape
ok 721 - Ctrl+[ clears pending marks like Escape
  ---
  duration_ms: 4.955
  ...
# Subtest: empty query walks every row with unique keys and survives a type-and-clear
ok 722 - empty query walks every row with unique keys and survives a type-and-clear
  ---
  duration_ms: 518.231026
  ...
# Subtest: production sheet render and clicks use real DOM APIs
ok 723 - production sheet render and clicks use real DOM APIs
  ---
  duration_ms: 3540.946833
  ...
# Subtest: marking, toggling, and renumbering
ok 724 - marking, toggling, and renumbering
  ---
  duration_ms: 80.358399
  ...
# Subtest: the badge and tray text
ok 725 - the badge and tray text
  ---
  duration_ms: 13.326974
  ...
# Subtest: query select-all after a mark
ok 726 - query select-all after a mark
  ---
  duration_ms: 7.993402
  ...
# Subtest: each refusal reason
ok 727 - each refusal reason
  ---
  duration_ms: 5.198053
  ...
# Subtest: Ctrl+M into argument mode, then marking from it
ok 728 - Ctrl+M into argument mode, then marking from it
  ---
  duration_ms: 4.533696
  ...
# Subtest: argument mode Ctrl+M with incomplete args shows Needs
ok 729 - argument mode Ctrl+M with incomplete args shows Needs
  ---
  duration_ms: 3.248863
  ...
# Subtest: Backspace pops the last step
ok 730 - Backspace pops the last step
  ---
  duration_ms: 67.525188
  ...
# Subtest: Esc first clears marks, second closes
ok 731 - Esc first clears marks, second closes
  ---
  duration_ms: 8.642229
  ...
# Subtest: click and Ctrl+click toggles
ok 732 - click and Ctrl+click toggles
  ---
  duration_ms: 12.966534
  ...
# Subtest: Shift+Enter with marks runs nothing
ok 733 - Shift+Enter with marks runs nothing
  ---
  duration_ms: 13.525023
  ...
# Subtest: one mark activates like Enter
ok 734 - one mark activates like Enter
  ---
  duration_ms: 1849.222087
  ...
# Subtest: one confirm mark opens its card
ok 735 - one confirm mark opens its card
  ---
  duration_ms: 3.378971
  ...
# Subtest: Enter with unguarded steps closes and runs
ok 736 - Enter with unguarded steps closes and runs
  ---
  duration_ms: 7.366123
  ...
# Subtest: Enter with guards shows the review card
ok 737 - Enter with guards shows the review card
  ---
  duration_ms: 90.705673
  ...
# Subtest: Ctrl+Enter skips the card
ok 738 - Ctrl+Enter skips the card
  ---
  duration_ms: 15.00584
  ...
# Subtest: argument-mode add and run
ok 739 - argument-mode add and run
  ---
  duration_ms: 39.607638
  ...
# Subtest: the already-running hint
ok 740 - the already-running hint
  ---
  duration_ms: 59.987867
  ...
# Subtest: RECENT grouping folds one sequence into one row
ok 741 - RECENT grouping folds one sequence into one row
  ---
  duration_ms: 0.935977
  ...
# Subtest: RECENT dedupe, limit, interrupted glyph, and about lines
ok 742 - RECENT dedupe, limit, interrupted glyph, and about lines
  ---
  duration_ms: 57.299776
  ...
# Subtest: RECENT Enter reruns all steps and Ctrl+M loads and unloads them
ok 743 - RECENT Enter reruns all steps and Ctrl+M loads and unloads them
  ---
  duration_ms: 47.323168
  ...
# Subtest: clicking a descendant toggles while marks are pending
ok 744 - clicking a descendant toggles while marks are pending
  ---
  duration_ms: 12.224909
  ...
# Subtest: no-mark argument Shift+Enter still previews
ok 745 - no-mark argument Shift+Enter still previews
  ---
  duration_ms: 8.073624
  ...
# Subtest: marked argument Ctrl+Enter with a highlighted completion adds and runs now
ok 746 - marked argument Ctrl+Enter with a highlighted completion adds and runs now
  ---
  duration_ms: 38.066165
  ...
# Subtest: incomplete marked arguments leave marks and show the missing positional
ok 747 - incomplete marked arguments leave marks and show the missing positional
  ---
  duration_ms: 5.90877
  ...
# Subtest: a RECENT sequence reduced to one report uses the normal activation chain
ok 748 - a RECENT sequence reduced to one report uses the normal activation chain
  ---
  duration_ms: 390.051828
  ...
# Subtest: a RECENT sequence reduced to one confirm opens its card
ok 749 - a RECENT sequence reduced to one confirm opens its card
  ---
  duration_ms: 11.012345
  ...
# Subtest: a RECENT sequence reduced to one preview-first command previews
ok 750 - a RECENT sequence reduced to one preview-first command previews
  ---
  duration_ms: 500.170304
  ...
# Subtest: rebuildRows passes live sequence ids so a running sequence shows ⟳
ok 751 - rebuildRows passes live sequence ids so a running sequence shows ⟳
  ---
  duration_ms: 21.121093
  ...
# Subtest: an active sequence refuses a duplicate rerun without closing the sheet
ok 752 - an active sequence refuses a duplicate rerun without closing the sheet
  ---
  duration_ms: 51.100301
  ...
# Subtest: an incomplete sequence with no active id stays interrupted after reload
ok 753 - an incomplete sequence with no active id stays interrupted after reload
  ---
  duration_ms: 0.574788
  ...
# Subtest: fuzzy ranking matches every token and prefers paths, prefixes, and keywords
ok 754 - fuzzy ranking matches every token and prefers paths, prefixes, and keywords
  ---
  duration_ms: 3.620281
  ...
# Subtest: bare capture has no row but named capture rows keep theirs
ok 755 - bare capture has no row but named capture rows keep theirs
  ---
  duration_ms: 1.379805
  ...
# Subtest: unavailable rows stay visible with reasons
ok 756 - unavailable rows stay visible with reasons
  ---
  duration_ms: 0.533919
  ...
# Subtest: frecency weights recent runs and the last-ten window
ok 757 - frecency weights recent runs and the last-ten window
  ---
  duration_ms: 0.889869
  ...
# Subtest: context rows fill For this note and From clipboard
ok 758 - context rows fill For this note and From clipboard
  ---
  duration_ms: 0.896892
  ...
# Subtest: note kinds follow frontmatter type with the article rule
ok 759 - note kinds follow frontmatter type with the article rule
  ---
  duration_ms: 0.229017
  ...
# Subtest: empty query groups RECENT, note, clipboard, then catalog sections
ok 760 - empty query groups RECENT, note, clipboard, then catalog sections
  ---
  duration_ms: 0.50242
  ...
# Subtest: list keys map to intents and plain text stays unhandled
ok 761 - list keys map to intents and plain text stays unhandled
  ---
  duration_ms: 0.292458
  ...
# Subtest: help argv targets the selected row or bare bob
ok 762 - help argv targets the selected row or bare bob
  ---
  duration_ms: 0.320172
  ...
# Subtest: median duration hides fast rows under the two-second floor
ok 763 - median duration hides fast rows under the two-second floor
  ---
  duration_ms: 0.444198
  ...
# Subtest: the open command focuses an already-open sheet
ok 764 - the open command focuses an already-open sheet
  ---
  duration_ms: 8.1082
  ...
# Subtest: Enter on a report row streams it in the sheet output stage
ok 765 - Enter on a report row streams it in the sheet output stage
  ---
  duration_ms: 1940.052519
  ...
# Subtest: report footer shows its running line until the output opens
ok 766 - report footer shows its running line until the output opens
  ---
  duration_ms: 10.698926
  ...
# Subtest: preview footer shows a running line while the preview is pending
ok 767 - preview footer shows a running line while the preview is pending
  ---
  duration_ms: 10.03626
  ...
# Subtest: help start failure replaces its running line with the warning hint
ok 768 - help start failure replaces its running line with the warning hint
  ---
  duration_ms: 12.232354
  ...
# Subtest: a rejected sheet run clears the running line before propagating
ok 769 - a rejected sheet run clears the running line before propagating
  ---
  duration_ms: 12.250138
  ...
# Subtest: confirm rows need Ctrl+Enter and run confirmed
ok 770 - confirm rows need Ctrl+Enter and run confirmed
  ---
  duration_ms: 706.873509
  ...
# Subtest: Shift+Enter previews first and Apply reruns without the preview flag
ok 771 - Shift+Enter previews first and Apply reruns without the preview flag
  ---
  duration_ms: 1277.078712
  ...
# Subtest: api.preview opens the sheet into a preview-first row's preview stage
ok 772 - api.preview opens the sheet into a preview-first row's preview stage
  ---
  duration_ms: 518.34834
  ...
# Subtest: api.preview opens a report row in the output stage
ok 773 - api.preview opens a report row in the output stage
  ---
  duration_ms: 1782.933992
  ...
# Subtest: api.preview refuses excluded, unknown, unapplied-write, and unavailable rows
ok 774 - api.preview refuses excluded, unknown, unapplied-write, and unavailable rows
  ---
  duration_ms: 2.129937
  ...
# Subtest: api.preview focuses an already-open sheet and replaces its stage
ok 775 - api.preview focuses an already-open sheet and replaces its stage
  ---
  duration_ms: 2041.072264
  ...
# Subtest: missing positionals enter argument mode instead of running
ok 776 - missing positionals enter argument mode instead of running
  ---
  duration_ms: 16.889997
  ...
# Subtest: a trailing ? runs help for the selected row in the output stage
ok 777 - a trailing ? runs help for the selected row in the output stage
  ---
  duration_ms: 1337.138258
  ...
# Subtest: watching the sheet output suppresses the finish toast
ok 778 - watching the sheet output suppresses the finish toast
  ---
  duration_ms: 2035.168073
  ...
# Subtest: unavailable rows never activate
ok 779 - unavailable rows never activate
  ---
  duration_ms: 10.1774
  ...
# Subtest: RECENT rows drop the bob binary and keep unique keys
ok 780 - RECENT rows drop the bob binary and keep unique keys
  ---
  duration_ms: 5.512925
  ...
# Subtest: RECENT vault-sync reruns without doubling the path
ok 781 - RECENT vault-sync reruns without doubling the path
  ---
  duration_ms: 5587.321416
  ...
# Subtest: two RECENT rows for one entry select one at a time
ok 782 - two RECENT rows for one entry select one at a time
  ---
  duration_ms: 1245.914195
  ...
# Subtest: RECENT preview-first and confirm rows honor their guards
ok 783 - RECENT preview-first and confirm rows honor their guards
  ---
  duration_ms: 2476.755635
  ...
# Subtest: in-sheet r reruns vault-sync without doubling the path
ok 784 - in-sheet r reruns vault-sync without doubling the path
  ---
  duration_ms: 326.973683
  ...
# Subtest: hidden below 400 ms, and never settles for such runs
ok 785 - hidden below 400 ms, and never settles for such runs
  ---
  duration_ms: 2.452002
  ...
# Subtest: running keeps one mark element, brand label, tabular clock, and native tooltip
ok 786 - running keeps one mark element, brand label, tabular clock, and native tooltip
  ---
  duration_ms: 1.221422
  ...
# Subtest: two runs show count, longest clock, and click opens the newest
ok 787 - two runs show count, longest clock, and click opens the newest
  ---
  duration_ms: 0.857056
  ...
# Subtest: queued-only gives is-queued and overdue writer gives is-overdue with budget tooltip
ok 788 - queued-only gives is-queued and overdue writer gives is-overdue with budget tooltip
  ---
  duration_ms: 0.562444
  ...
# Subtest: settle shows outcome glyph for 1600 ms, then leaving, then hidden
ok 789 - settle shows outcome glyph for 1600 ms, then leaving, then hidden
  ---
  duration_ms: 0.689967
  ...
# Subtest: sequence model shows step, sequence clock, tooltip, and between-step visibility
ok 790 - sequence model shows step, sequence clock, tooltip, and between-step visibility
  ---
  duration_ms: 0.919967
  ...
# Subtest: sequence chip lazily inserts step and title before the clock and hides them when idle
ok 791 - sequence chip lazily inserts step and title before the clock and hides them when idle
  ---
  duration_ms: 2.578053
  ...
# Subtest: sequence settle displays its final step and opens the focus run
ok 792 - sequence settle displays its final step and opens the focus run
  ---
  duration_ms: 0.333397
  ...
# Subtest: a new run during a settle shows running at once and click opens the settled run
ok 793 - a new run during a settle shows running at once and click opens the settled run
  ---
  duration_ms: 0.537786
  ...
# Subtest: adopted unfinished runs appear flagged and all triggers light the indicator
ok 794 - adopted unfinished runs appear flagged and all triggers light the indicator
  ---
  duration_ms: 0.527627
  ...
# Subtest: first visible paint uses HTMLCollection semantics and preserves existing classes
ok 795 - first visible paint uses HTMLCollection semantics and preserves existing classes
  ---
  duration_ms: 0.462723
  ...
# Subtest: DOM-like repaints keep the mark and anatomy idempotent
ok 796 - DOM-like repaints keep the mark and anatomy idempotent
  ---
  duration_ms: 0.379515
  ...
# Subtest: DOM-like settle paint shows its outcome, then hides after the settle window
ok 797 - DOM-like settle paint shows its outcome, then hides after the settle window
  ---
  duration_ms: 0.307427
  ...
# Subtest: plugin status-chip path paints an HTMLCollection-like status item
ok 798 - plugin status-chip path paints an HTMLCollection-like status item
  ---
  duration_ms: 51.172116
  ...
# Subtest: done/ fixtures mirror bob-cli byte for byte
ok 799 - done/ fixtures mirror bob-cli byte for byte
  ---
  duration_ms: 53.689804
  ...
# Subtest: every plugin helper agrees with the shared vectors
ok 800 - every plugin helper agrees with the shared vectors
  ---
  duration_ms: 79.539796
  ...
# Subtest: KB24: mark identities and folds equal the full planner for a sub-project
ok 801 - KB24: mark identities and folds equal the full planner for a sub-project
  ---
  duration_ms: 58.482064
  ...
# Subtest: KB24: mark identities and folds equal the full planner for a root
ok 802 - KB24: mark identities and folds equal the full planner for a root
  ---
  duration_ms: 6.718606
  ...
# Subtest: LP1–LP17: ledger leafness agrees with the reverted cycler walk
ok 803 - LP1–LP17: ledger leafness agrees with the reverted cycler walk
  ---
  duration_ms: 11.163683
  ...
# Subtest: lead tally respects declared order, grammar, peeks and last-added meaning
ok 804 - lead tally respects declared order, grammar, peeks and last-added meaning
  ---
  duration_ms: 1.854341
  ...
# Subtest: Reading cards match aliases and paths, skip nested project headings and ordinary same-stem notes
ok 805 - Reading cards match aliases and paths, skip nested project headings and ordinary same-stem notes
  ---
  duration_ms: 4.816997
  ...
# Subtest: peeks are inert text and repeated paints preserve keyboard focus and listeners
ok 806 - peeks are inert text and repeated paints preserve keyboard focus and listeners
  ---
  duration_ms: 2.955863
  ...
# Subtest: unavailable, stale, invalid and damaged reports keep distinct feedback and shared repair actions
ok 807 - unavailable, stale, invalid and damaged reports keep distinct feedback and shared repair actions
  ---
  duration_ms: 4.255835
  ...
# Subtest: missing or damaged catalog with no albums has an actionable host anchor and diagnostics
ok 808 - missing or damaged catalog with no albums has an actionable host anchor and diagnostics
  ---
  duration_ms: 1.123034
  ...
# Subtest: source scanner and group jump ignore YAML/fenced/nested examples and handle escaped labels
ok 809 - source scanner and group jump ignore YAML/fenced/nested examples and handle escaped labels
  ---
  duration_ms: 0.921208
  ...
# Subtest: lead activation keeps modifier navigation, records jump history, and calls the pane fold hook before scrolling
ok 810 - lead activation keeps modifier navigation, records jump history, and calls the pane fold hook before scrolling
  ---
  duration_ms: 1.353474
  ...
# Subtest: Reading children clean on unload, panes stay independent, file switches remove old facts
ok 811 - Reading children clean on unload, panes stay independent, file switches remove old facts
  ---
  duration_ms: 133.21993
  ...
# Subtest: Live Preview paints native callouts, leaves source text/caret intact, and removes paint in Source mode
ok 812 - Live Preview paints native callouts, leaves source text/caret intact, and removes paint in Source mode
  ---
  duration_ms: 162.321071
  ...
# Subtest: Live Preview missing-catalog action is a widget outside frontmatter, with source mode gated
ok 813 - Live Preview missing-catalog action is a widget outside frontmatter, with source mode gated
  ---
  duration_ms: 117.085427
  ...
# Subtest: CSS uses pane container wrapping, scoped album hue, safe peeks and keyboard outlines
ok 814 - CSS uses pane container wrapping, scoped album hue, safe peeks and keyboard outlines
  ---
  duration_ms: 45.549633
  ...
# Subtest: missing-catalog controls occur only in the selected source section
ok 815 - missing-catalog controls occur only in the selected source section
  ---
  duration_ms: 323.786607
  ...
# Subtest: keyboard and middle-click group controls activate once without changing the editor caret
ok 816 - keyboard and middle-click group controls activate once without changing the editor caret
  ---
  duration_ms: 255.280005
  ...
# Subtest: Live Preview extension paints after updates and cleans file switches, destroy and pending timers
ok 817 - Live Preview extension paints after updates and cleans file switches, destroy and pending timers
  ---
  duration_ms: 103.680214
  ...
# Subtest: entry kind covers scalar, list, wikilink, and legacy noun types
ok 818 - entry kind covers scalar, list, wikilink, and legacy noun types
  ---
  duration_ms: 1.519141
  ...
# Subtest: parent target handles scalar, list, and ambiguous forms
ok 819 - parent target handles scalar, list, and ambiguous forms
  ---
  duration_ms: 0.308529
  ...
# Subtest: direct album paths resolve through the report
ok 820 - direct album paths resolve through the report
  ---
  duration_ms: 0.660932
  ...
# Subtest: record notes resolve their actual parent link
ok 821 - record notes resolve their actual parent link
  ---
  duration_ms: 0.294051
  ...
# Subtest: record legacy types resolve like records
ok 822 - record legacy types resolve like records
  ---
  duration_ms: 0.210622
  ...
# Subtest: missing, cyclic, ambiguous, and non-album parents teach instead of guessing
ok 823 - missing, cyclic, ambiguous, and non-album parents teach instead of guessing
  ---
  duration_ms: 0.446032
  ...
# Subtest: palette command is registered as a literal addCommand for the inventory
ok 824 - palette command is registered as a literal addCommand for the inventory
  ---
  duration_ms: 139.473992
  ...
# Subtest: header resolves real parent paths and ignores breadcrumb labels
ok 825 - header resolves real parent paths and ignores breadcrumb labels
  ---
  duration_ms: 60.669318
  ...
# Subtest: owner ancestry stops without warning at the conventional type note or a direct non-home parent
ok 826 - owner ancestry stops without warning at the conventional type note or a direct non-home parent
  ---
  duration_ms: 0.94265
  ...
# Subtest: missing, malformed, cyclic, and depth-limited owner chains still warn
ok 827 - missing, malformed, cyclic, and depth-limited owner chains still warn
  ---
  duration_ms: 1.666461
  ...
# Subtest: schema model preserves declaration and choice order; empty and invalid routes stay explicit
ok 828 - schema model preserves declaration and choice order; empty and invalid routes stay explicit
  ---
  duration_ms: 1.022993
  ...
# Subtest: broken schema remains visible and disables the capture route with its diagnostic
ok 829 - broken schema remains visible and disables the capture route with its diagnostic
  ---
  duration_ms: 3.771631
  ...
# Subtest: rendering is idempotent, keeps schema labels as text, scopes Properties, and clears on type change
ok 830 - rendering is idempotent, keeps schema labels as text, scopes Properties, and clears on type change
  ---
  duration_ms: 3.000649
  ...
# Subtest: clipboard failure is surfaced and does not mutate a note
ok 831 - clipboard failure is surfaced and does not mutate a note
  ---
  duration_ms: 0.571501
  ...
# Subtest: Live Preview widgets follow album identity and remove the Properties scope on view switches
ok 832 - Live Preview widgets follow album identity and remove the Properties scope on view switches
  ---
  duration_ms: 1.635813
  ...
# Subtest: Reading lifecycle unload restores Properties visibility
ok 833 - Reading lifecycle unload restores Properties visibility
  ---
  duration_ms: 1.268842
  ...
# Subtest: detached callout chunks never paint reading headers, including after editor attachment
ok 834 - detached callout chunks never paint reading headers, including after editor attachment
  ---
  duration_ms: 0.973699
  ...
# Subtest: reading batches pick attached chunks, stay idempotent, and keep pane/embed lifetimes separate
ok 835 - reading batches pick attached chunks, stay idempotent, and keep pane/embed lifetimes separate
  ---
  duration_ms: 49.1355
  ...
# Subtest: chunks attaching before the flush share the preview/sizer identity
ok 836 - chunks attaching before the flush share the preview/sizer identity
  ---
  duration_ms: 0.788856
  ...
# Subtest: late reading attachment paints on refresh and unload uses the live surface
ok 837 - late reading attachment paints on refresh and unload uses the live surface
  ---
  duration_ms: 0.935486
  ...
# Subtest: repaint sweeps stray reading chrome from editor chunks without removing CM widgets
ok 838 - repaint sweeps stray reading chrome from editor chunks without removing CM widgets
  ---
  duration_ms: 0.349066
  ...
# Subtest: teardown cancels pending reading batches
ok 839 - teardown cancels pending reading batches
  ---
  duration_ms: 0.250498
  ...
# Subtest: H1-less albums paint at the start and embeds keep their own property scope
ok 840 - H1-less albums paint at the start and embeds keep their own property scope
  ---
  duration_ms: 0.50266
  ...
# Subtest: schema summary starts expanded and collapses per album in view state
ok 841 - schema summary starts expanded and collapses per album in view state
  ---
  duration_ms: 79.593839
  ...
# Subtest: chip rows cover kinds, flags, grouping, legacy, and empty teaching copy
ok 842 - chip rows cover kinds, flags, grouping, legacy, and empty teaching copy
  ---
  duration_ms: 5.419005
  ...
# Subtest: read-only Schema Card paints counts, lint, and a navigation/y/esc footer
ok 843 - read-only Schema Card paints counts, lint, and a navigation/y/esc footer
  ---
  duration_ms: 56.491893
  ...
# Subtest: same-message child warnings name each file and keep distinct focus and card targets
ok 844 - same-message child warnings name each file and keep distinct focus and card targets
  ---
  duration_ms: 3.999166
  ...
# Subtest: y jumps to the field or lint line in Source mode without writing the vault
ok 845 - y jumps to the field or lint line in Source mode without writing the vault
  ---
  duration_ms: 56.997317
  ...
# Subtest: theme accent, schema button, and keyboard labels stay on the header
ok 846 - theme accent, schema button, and keyboard labels stay on the header
  ---
  duration_ms: 0.582603
  ...
# Subtest: schema edit model preserves typed defaults and stable field and choice targets
ok 847 - schema edit model preserves typed defaults and stable field and choice targets
  ---
  duration_ms: 0.577292
  ...
# Subtest: Schema Card uses bob's singular display label for one record and keeps the legacy fallback
ok 848 - Schema Card uses bob's singular display label for one record and keeps the legacy fallback
  ---
  duration_ms: 0.449077
  ...
# Subtest: Schema Card key events reorder fields and choices while plain navigation stays read-only
ok 849 - Schema Card key events reorder fields and choices while plain navigation stays read-only
  ---
  duration_ms: 138.632175
  ...
# Subtest: Schema Card preserves typed draft, caret, and focus through report repaint and debounces edits
ok 850 - Schema Card preserves typed draft, caret, and focus through report repaint and debounces edits
  ---
  duration_ms: 364.137244
  ...
# Subtest: Schema Card Enter is gated by current preview across pending, refused, stale, and duplicate input events
ok 851 - Schema Card Enter is gated by current preview across pending, refused, stale, and duplicate input events
  ---
  duration_ms: 744.596848
  ...
# Subtest: a repainted Apply preview uses live session state and double Enter applies once
ok 852 - a repainted Apply preview uses live session state and double Enter applies once
  ---
  duration_ms: 383.845229
  ...
# Subtest: an enabled Apply control routes a newly stale preview to a visible refusal
ok 853 - an enabled Apply control routes a newly stale preview to a visible refusal
  ---
  duration_ms: 336.714168
  ...
# Subtest: new choice field rows keep live order and values as early and middle choices are removed
ok 854 - new choice field rows keep live order and values as early and middle choices are removed
  ---
  duration_ms: 594.619104
  ...
# Subtest: Schema Card stages typed edits, previews one op, and applies only after confirmation
ok 855 - Schema Card stages typed edits, previews one op, and applies only after confirmation
  ---
  duration_ms: 43.137257
  ...
# Subtest: open album panes save in order and missing save support refuses
ok 856 - open album panes save in order and missing save support refuses
  ---
  duration_ms: 0.478935
  ...
# Subtest: Schema Card maps album, field, choice, ordering, toggle, and removal gestures
ok 857 - Schema Card maps album, field, choice, ordering, toggle, and removal gestures
  ---
  duration_ms: 347.344393
  ...
# Subtest: Schema Card Escape follows one dispatch: stage cancel, draft clear, then close
ok 858 - Schema Card Escape follows one dispatch: stage cancel, draft clear, then close
  ---
  duration_ms: 78.782279
  ...
# Subtest: default folds: first group stays open, later groups fold only above twelve records
ok 859 - default folds: first group stays open, later groups fold only above twelve records
  ---
  duration_ms: 6.141516
  ...
# Subtest: later group of twelve stays open; thirteen folds even when only two subgroup items exist
ok 860 - later group of twelve stays open; thirteen folds even when only two subgroup items exist
  ---
  duration_ms: 2.556791
  ...
# Subtest: empty and flat indexes stay readable without fold controls
ok 861 - empty and flat indexes stay readable without fold controls
  ---
  duration_ms: 1.001742
  ...
# Subtest: user fold choices persist across refresh and stay isolated per pane
ok 862 - user fold choices persist across refresh and stay isolated per pane
  ---
  duration_ms: 83.513302
  ...
# Subtest: group jump expands only the destination pane before scroll
ok 863 - group jump expands only the destination pane before scroll
  ---
  duration_ms: 3.525019
  ...
# Subtest: visited and watched_on chips are distinct, skip invalid/future dates, and refresh on day rollover
ok 864 - visited and watched_on chips are distinct, skip invalid/future dates, and refresh on day rollover
  ---
  duration_ms: 3.813922
  ...
# Subtest: painting, folding, and date chips never write note bytes
ok 865 - painting, folding, and date chips never write note bytes
  ---
  duration_ms: 48.314301
  ...
# Subtest: fenced examples are ignored; Live Preview paints, Source mode removes chrome
ok 866 - fenced examples are ignored; Live Preview paints, Source mode removes chrome
  ---
  duration_ms: 5.502716
  ...
# Subtest: reading children clean on unload and teardown restores hidden rows
ok 867 - reading children clean on unload and teardown restores hidden rows
  ---
  duration_ms: 123.102715
  ...
# Subtest: non-album notes and embeds in the outer editor are left alone
ok 868 - non-album notes and embeds in the outer editor are left alone
  ---
  duration_ms: 12.190022
  ...
# Subtest: CSS hides folded nested lists and styles the tally with area hue
ok 869 - CSS hides folded nested lists and styles the tally with area hue
  ---
  duration_ms: 7.398796
  ...
# Subtest: multi-slot arrange compiles one envelope, paints projected order with zero writer calls, and revert clears the draft
ok 870 - multi-slot arrange compiles one envelope, paints projected order with zero writer calls, and revert clears the draft
  ---
  duration_ms: 353.091366
  ...
# Subtest: quiet saves on one Enter while loud needs Confirm save
ok 871 - quiet saves on one Enter while loud needs Confirm save
  ---
  duration_ms: 380.59818
  ...
# Subtest: follow-on moves during an in-flight apply never call setDraft until it settles
ok 872 - follow-on moves during an in-flight apply never call setDraft until it settles
  ---
  duration_ms: 180.874382
  ...
# Subtest: refusal keeps the arrangement pending; u and esc walk the ladder; gap hints place by keystroke; macOS codes move
ok 873 - refusal keeps the arrangement pending; u and esc walk the ladder; gap hints place by keystroke; macOS codes move
  ---
  duration_ms: 77.774716
  ...
# Subtest: close-during-save records the plugin-level undo and seeds a reopened card
ok 874 - close-during-save records the plugin-level undo and seeds a reopened card
  ---
  duration_ms: 113.079399
  ...
# Subtest: Schema Card shell paints stable regions, pills, and a hidden empty status rule
ok 875 - Schema Card shell paints stable regions, pills, and a hidden empty status rule
  ---
  duration_ms: 169.100462
  ...
# Subtest: selection and session paints keep body and stage input nodes
ok 876 - selection and session paints keep body and stage input nodes
  ---
  duration_ms: 378.253514
  ...
# Subtest: Enter latches a pending preview and applies when that revision succeeds
ok 877 - Enter latches a pending preview and applies when that revision succeeds
  ---
  duration_ms: 336.090246
  ...
# Subtest: a further edit clears the Enter latch before a stale preview can apply
ok 878 - a further edit clears the Enter latch before a stale preview can apply
  ---
  duration_ms: 347.75622
  ...
# Subtest: Emoji Slot preserves graphemes and ports split_icon fixtures
ok 879 - Emoji Slot preserves graphemes and ports split_icon fixtures
  ---
  duration_ms: 7.392423
  ...
# Subtest: Emoji Slot searches, browses, marks sibling duplicates, and Enter picks without saving the stage
ok 880 - Emoji Slot searches, browses, marks sibling duplicates, and Enter picks without saving the stage
  ---
  duration_ms: 18.935691
  ...
# Subtest: Emoji Slot Escape closes the panel before the stage and direct pasted graphemes stay exact
ok 881 - Emoji Slot Escape closes the panel before the stage and direct pasted graphemes stay exact
  ---
  duration_ms: 22.267122
  ...
# Subtest: every field-add initial choice gets an Emoji Slot and missing or v0 apis use the plain input
ok 882 - every field-add initial choice gets an Emoji Slot and missing or v0 apis use the plain input
  ---
  duration_ms: 29.710994
  ...
# Subtest: Emoji Slot result assembly handles full catalogs under the filter paint budget
ok 883 - Emoji Slot result assembly handles full catalogs under the filter paint budget
  ---
  duration_ms: 2.920525
  ...
# Subtest: Emoji Slot Ctrl+N / Ctrl+P step one emoji at a time and wrap at the ends
ok 884 - Emoji Slot Ctrl+N / Ctrl+P step one emoji at a time and wrap at the ends
  ---
  duration_ms: 0.42448
  ...
# Subtest: Emoji Slot move-key alias matches the exact Ctrl chord only
ok 885 - Emoji Slot move-key alias matches the exact Ctrl chord only
  ---
  duration_ms: 0.305904
  ...
# Subtest: Emoji Slot Ctrl+N steps one emoji, Ctrl+P wraps to the last, and the highlight stays in view
ok 886 - Emoji Slot Ctrl+N steps one emoji, Ctrl+P wraps to the last, and the highlight stays in view
  ---
  duration_ms: 12.673275
  ...
# Subtest: lock wait paints the pending line and Esc stops without closing
ok 887 - lock wait paints the pending line and Esc stops without closing
  ---
  duration_ms: 6.077723
  ...
# Subtest: Emoji Slot hint teaches the gesture and follows open, pick, and clear
ok 888 - Emoji Slot hint teaches the gesture and follows open, pick, and clear
  ---
  duration_ms: 24.734893
  ...
# Subtest: every field-add initial choice shows the hint until its glyph is set
ok 889 - every field-add initial choice shows the hint until its glyph is set
  ---
  duration_ms: 4.951312
  ...
# Subtest: close-key predicate accepts q/Q/Ctrl+[ and rejects modifiers/composition
ok 890 - close-key predicate accepts q/Q/Ctrl+[ and rejects modifiers/composition
  ---
  duration_ms: 0.593272
  ...
# Subtest: q and Ctrl+[ close from the editor behind the modal and are consumed
ok 891 - q and Ctrl+[ close from the editor behind the modal and are consumed
  ---
  duration_ms: 1.936597
  ...
# Subtest: q types in a stage input while Ctrl+[ cancels the stage then closes
ok 892 - q types in a stage input while Ctrl+[ cancels the stage then closes
  ---
  duration_ms: 5.316059
  ...
# Subtest: q and Ctrl+[ leave hint mode without picking a gap
ok 893 - q and Ctrl+[ leave hint mode without picking a gap
  ---
  duration_ms: 5.163278
  ...
# Subtest: close keys follow Esc through pending moves, All actions, drag, and applying
ok 894 - close keys follow Esc through pending moves, All actions, drag, and applying
  ---
  duration_ms: 5.512144
  ...
# Subtest: scope handler passes unrelated keys through and unregisters on close
ok 895 - scope handler passes unrelated keys through and unregisters on close
  ---
  duration_ms: 4.121509
  ...
# Subtest: Emoji Slot search types q while Ctrl+[ closes only the picker
ok 896 - Emoji Slot search types q while Ctrl+[ closes only the picker
  ---
  duration_ms: 2.578753
  ...
# Subtest: plain-browsing close hint reads esc/q
ok 897 - plain-browsing close hint reads esc/q
  ---
  duration_ms: 1.158221
  ...
# Subtest: field jumps follow one painted order shared with the body painter
ok 898 - field jumps follow one painted order shared with the body painter
  ---
  duration_ms: 289.576975
  ...
# Subtest: painted targets put body issues before + field
ok 899 - painted targets put body issues before + field
  ---
  duration_ms: 0.405945
  ...
# Subtest: field step helpers scan strictly to the next field row
ok 900 - field step helpers scan strictly to the next field row
  ---
  duration_ms: 0.381197
  ...
# Subtest: Shift+J/K walk every row of the field-step table
ok 901 - Shift+J/K walk every row of the field-step table
  ---
  duration_ms: 53.670396
  ...
# Subtest: digits jump straight to field N as painted
ok 902 - digits jump straight to field N as painted
  ---
  duration_ms: 23.516729
  ...
# Subtest: 3 then Alt+K nudges field 3 exactly one slot
ok 903 - 3 then Alt+K nudges field 3 exactly one slot
  ---
  duration_ms: 12.536544
  ...
# Subtest: Shift+1 still stages required while shifted digits jump
ok 904 - Shift+1 still stages required while shifted digits jump
  ---
  duration_ms: 72.132975
  ...
# Subtest: Alt and Ctrl jumps keep their arrange meanings
ok 905 - Alt and Ctrl jumps keep their arrange meanings
  ---
  duration_ms: 86.587531
  ...
# Subtest: jumps are inert in stages, inputs, composition, applying, the read-only card, and hint mode
ok 906 - jumps are inert in stages, inputs, composition, applying, the read-only card, and hint mode
  ---
  duration_ms: 26.89608
  ...
# Subtest: jumps never touch the session preview, apply, or the arrangement nudge
ok 907 - jumps never touch the session preview, apply, or the arrangement nudge
  ---
  duration_ms: 13.697161
  ...
# Subtest: a held clamp key bumps once, then stays silent
ok 908 - a held clamp key bumps once, then stays silent
  ---
  duration_ms: 7.918327
  ...
# Subtest: zero fields announce the empty lane on every jump key
ok 909 - zero fields announce the empty lane on every jump key
  ---
  duration_ms: 28.022449
  ...
# Subtest: one field uses the singular lane noun
ok 910 - one field uses the singular lane noun
  ---
  duration_ms: 9.430255
  ...
# Subtest: jumps reveal the group and leave the announcer visible to screen readers
ok 911 - jumps reveal the group and leave the announcer visible to screen readers
  ---
  duration_ms: 7.28086
  ...
# Subtest: a missing scroller never throws
ok 912 - a missing scroller never throws
  ---
  duration_ms: 15.497026
  ...
# Subtest: reduced motion turns off every bump, including the nudge shake
ok 913 - reduced motion turns off every bump, including the nudge shake
  ---
  duration_ms: 17.292235
  ...
# Subtest: keycaps number painted fields 1-9 and keep a hidden column at 10
ok 914 - keycaps number painted fields 1-9 and keep a hidden column at 10
  ---
  duration_ms: 10.905841
  ...
# Subtest: keycap numbers re-flow after a field nudge
ok 915 - keycap numbers re-flow after a field nudge
  ---
  duration_ms: 7.964676
  ...
# Subtest: is-current-group follows chip and + choice selection and clears on field or stats
ok 916 - is-current-group follows chip and + choice selection and clears on field or stats
  ---
  duration_ms: 5.95536
  ...
# Subtest: plain browsing paints a field hint with two keycaps after Enter
ok 917 - plain browsing paints a field hint with two keycaps after Enter
  ---
  duration_ms: 2.035066
  ...
# Subtest: the field hint uses 1 for a single field and 1-9 when there are ten
ok 918 - the field hint uses 1 for a single field and 1-9 when there are ten
  ---
  duration_ms: 0.306625
  ...
# Subtest: the field hint is absent with zero fields, a stage, hint mode, pending moves, saving, a lock wait, and the read-only card
ok 919 - the field hint is absent with zero fields, a stage, hint mode, pending moves, saving, a lock wait, and the read-only card
  ---
  duration_ms: 0.382901
  ...
# Subtest: the read-only card paints no field keycaps
ok 920 - the read-only card paints no field keycaps
  ---
  duration_ms: 3.42527
  ...
# Subtest: ghost defaults land after the selected choice and stay out of the envelope
ok 921 - ghost defaults land after the selected choice and stay out of the envelope
  ---
  duration_ms: 164.18597
  ...
# Subtest: Alt+J inside the label input moves the ghost and inserts no macOS glyph
ok 922 - Alt+J inside the label input moves the ghost and inserts no macOS glyph
  ---
  duration_ms: 67.942785
  ...
# Subtest: ghost gap badges place by keystroke and Esc leaves hint mode with the stage open
ok 923 - ghost gap badges place by keystroke and Esc leaves hint mode with the stage open
  ---
  duration_ms: 115.591004
  ...
# Subtest: field-add paints a ghost row whose moves set the field position
ok 924 - field-add paints a ghost row whose moves set the field position
  ---
  duration_ms: 65.057237
  ...
# Subtest: grip handles paint while browsing and hide while a stage is open
ok 925 - grip handles paint while browsing and hide while a stage is open
  ---
  duration_ms: 7.352297
  ...
# Subtest: drag gap math tracks pointer position in both orientations
ok 926 - drag gap math tracks pointer position in both orientations
  ---
  duration_ms: 0.736697
  ...
# Subtest: drag sessions drop through the same placeAtGap path as the keyboard
ok 927 - drag sessions drop through the same placeAtGap path as the keyboard
  ---
  duration_ms: 16.968467
  ...
# Subtest: out-of-scope drops and Esc cancel without touching the arrangement
ok 928 - out-of-scope drops and Esc cancel without touching the arrangement
  ---
  duration_ms: 7.748974
  ...
# Subtest: autoscroll steps only inside the edge zone of a scrollable card
ok 929 - autoscroll steps only inside the edge zone of a scrollable card
  ---
  duration_ms: 0.772385
  ...
# Subtest: update argv, envelope, and timeout follow the guarded writer contract
ok 930 - update argv, envelope, and timeout follow the guarded writer contract
  ---
  duration_ms: 2.568193
  ...
# Subtest: update decoder keeps typed refusals on numeric exits and rejects wire errors
ok 931 - update decoder keeps typed refusals on numeric exits and rejects wire errors
  ---
  duration_ms: 0.751705
  ...
# Subtest: stdin carries shell-looking labels byte-identical and never as shell text
ok 932 - stdin carries shell-looking labels byte-identical and never as shell text
  ---
  duration_ms: 2.208797
  ...
# Subtest: stdin failure and timeout surface as transport errors, never refusals
ok 933 - stdin failure and timeout surface as transport errors, never refusals
  ---
  duration_ms: 92.036916
  ...
# Subtest: typing settles through a 250 ms debounce; navigation never previews
ok 934 - typing settles through a 250 ms debounce; navigation never previews
  ---
  duration_ms: 1.810076
  ...
# Subtest: stale preview responses are suppressed; draft or vault changes invalidate Apply
ok 935 - stale preview responses are suppressed; draft or vault changes invalidate Apply
  ---
  duration_ms: 1.210722
  ...
# Subtest: close cancels a pending preview and ignores late work
ok 936 - close cancels a pending preview and ignores late work
  ---
  duration_ms: 0.678846
  ...
# Subtest: apply returns the refreshed display report for changed and unchanged saves
ok 937 - apply returns the refreshed display report for changed and unchanged saves
  ---
  duration_ms: 0.802242
  ...
# Subtest: apply awaits editor saves, refuses on failure, and teaches missing support
ok 938 - apply awaits editor saves, refuses on failure, and teaches missing support
  ---
  duration_ms: 1.17835
  ...
# Subtest: a save that invalidates the preview requires confirmation again
ok 939 - a save that invalidates the preview requires confirmation again
  ---
  duration_ms: 56.269096
  ...
# Subtest: an in-flight save cannot apply its captured envelope after a newer draft arrives
ok 940 - an in-flight save cannot apply its captured envelope after a newer draft arrives
  ---
  duration_ms: 0.655942
  ...
# Subtest: double Enter and parallel applies share one apply guard
ok 941 - double Enter and parallel applies share one apply guard
  ---
  duration_ms: 0.504874
  ...
# Subtest: no-op success keeps Undo; changed success stores the opaque inverse
ok 942 - no-op success keeps Undo; changed success stores the opaque inverse
  ---
  duration_ms: 0.524
  ...
# Subtest: u stages the inverse on the preview-and-Enter path without reconstruction
ok 943 - u stages the inverse on the preview-and-Enter path without reconstruction
  ---
  duration_ms: 0.907332
  ...
# Subtest: refusals keep the draft unconfirmed and never retry automatically
ok 944 - refusals keep the draft unconfirmed and never retry automatically
  ---
  duration_ms: 0.413349
  ...
# Subtest: stale apply responses refresh and keep the draft without retrying
ok 945 - stale apply responses refresh and keep the draft without retrying
  ---
  duration_ms: 0.441082
  ...
# Subtest: lock_busy then success retries the identical envelope once and never resaves
ok 946 - lock_busy then success retries the identical envelope once and never resaves
  ---
  duration_ms: 0.803775
  ...
# Subtest: repeated lock_busy advances attempts and ticks elapsed time every second
ok 947 - repeated lock_busy advances attempts and ticks elapsed time every second
  ---
  duration_ms: 1.248354
  ...
# Subtest: stopWaiting with no in-flight attempt restores preview-ready and Enter retries
ok 948 - stopWaiting with no in-flight attempt restores preview-ready and Enter retries
  ---
  duration_ms: 0.642187
  ...
# Subtest: stopWaiting during an in-flight attempt that succeeds is a normal save
ok 949 - stopWaiting during an in-flight attempt that succeeds is a normal save
  ---
  duration_ms: 74.782132
  ...
# Subtest: budget exhaustion restores preview-ready with lockNotice
ok 950 - budget exhaustion restores preview-ready with lockNotice
  ---
  duration_ms: 146.351612
  ...
# Subtest: generation move with the same consequence keeps waiting; a different one ends the wait
ok 951 - generation move with the same consequence keeps waiting; a different one ends the wait
  ---
  duration_ms: 1.025467
  ...
# Subtest: close mid-wait starts no further spawnApply calls
ok 952 - close mid-wait starts no further spawnApply calls
  ---
  duration_ms: 0.381599
  ...
# Subtest: transport failure after lock_busy takes today's unknown path with no retry
ok 953 - transport failure after lock_busy takes today's unknown path with no retry
  ---
  duration_ms: 0.432286
  ...
# Subtest: unknown apply outcomes refuse and demand explicit reconciliation
ok 954 - unknown apply outcomes refuse and demand explicit reconciliation
  ---
  duration_ms: 0.270627
  ...
# Subtest: post-sync failure keeps the commit and Undo and retries with vault-sync only
ok 955 - post-sync failure keeps the commit and Undo and retries with vault-sync only
  ---
  duration_ms: 0.397188
  ...
# Subtest: vault-sync retry failures keep the warning without losing Undo
ok 956 - vault-sync retry failures keep the warning without losing Undo
  ---
  duration_ms: 0.302187
  ...
# Subtest: the service skips the forced revalidate on lock_busy
ok 957 - the service skips the forced revalidate on lock_busy
  ---
  duration_ms: 0.685609
  ...
# Subtest: duplicate applies refuse busy while the first flight owns the lifecycle
ok 958 - duplicate applies refuse busy while the first flight owns the lifecycle
  ---
  duration_ms: 1.467722
  ...
# Subtest: an apply waits out a running sync instead of overlapping it
ok 959 - an apply waits out a running sync instead of overlapping it
  ---
  duration_ms: 0.90084
  ...
# Subtest: the writer's own echo schedules no sync while unrelated changes coalesce one trailing sync
ok 960 - the writer's own echo schedules no sync while unrelated changes coalesce one trailing sync
  ---
  duration_ms: 2.236099
  ...
# Subtest: a pre-write list flight never becomes the post-write report
ok 961 - a pre-write list flight never becomes the post-write report
  ---
  duration_ms: 109.411094
  ...
# Subtest: cancelled and refused service sessions never touch the plugin vault writer
ok 962 - cancelled and refused service sessions never touch the plugin vault writer
  ---
  duration_ms: 0.406958
  ...
# Subtest: real bob fixtures decode: dry-run, refusal, stale, and no-op
ok 963 - real bob fixtures decode: dry-run, refusal, stale, and no-op
  ---
  duration_ms: 438.081927
  ...
# Subtest: error focus picks the first error line with message and suggestions
ok 964 - error focus picks the first error line with message and suggestions
  ---
  duration_ms: 66.056935
  ...
# Subtest: Done refuses failed saves before touching the report
ok 965 - Done refuses failed saves before touching the report
  ---
  duration_ms: 0.31959
  ...
# Subtest: Done refuses unavailable or stale reports
ok 966 - Done refuses unavailable or stale reports
  ---
  duration_ms: 0.246541
  ...
# Subtest: Done shares one pending save across concurrent clicks
ok 967 - Done shares one pending save across concurrent clicks
  ---
  duration_ms: 0.973488
  ...
# Subtest: Done retries when a vault generation advances during the forced report
ok 968 - Done retries when a vault generation advances during the forced report
  ---
  duration_ms: 0.396768
  ...
# Subtest: Done abandons delayed saves after navigation, pane close, or plugin unload
ok 969 - Done abandons delayed saves after navigation, pane close, or plugin unload
  ---
  duration_ms: 0.465218
  ...
# Subtest: Done does not reopen the card if its pane navigates during view restoration
ok 970 - Done does not reopen the card if its pane navigates during view restoration
  ---
  duration_ms: 95.824788
  ...
# Subtest: Done keeps Source mode on schema errors and paints the diagnostic line
ok 971 - Done keeps Source mode on schema errors and paints the diagnostic line
  ---
  duration_ms: 0.417176
  ...
# Subtest: Done approves valid schemas and warning-only reports
ok 972 - Done approves valid schemas and warning-only reports
  ---
  duration_ms: 0.67017
  ...
# Subtest: Done button is a small accessible affordance outside the note text
ok 973 - Done button is a small accessible affordance outside the note text
  ---
  duration_ms: 0.633049
  ...
# Subtest: two panes keep separate excursions: decisions are per-leaf records
ok 974 - two panes keep separate excursions: decisions are per-leaf records
  ---
  duration_ms: 0.323868
  ...
# Subtest: album list and sync use fixed JSON argv and the versioned report decoders
ok 975 - album list and sync use fixed JSON argv and the versioned report decoders
  ---
  duration_ms: 6.390681
  ...
# Subtest: album field and album-entry report additions stay optional
ok 976 - album field and album-entry report additions stay optional
  ---
  duration_ms: 0.57616
  ...
# Subtest: catalog-only damage stays visible when no album rows exist
ok 977 - catalog-only damage stays visible when no album rows exist
  ---
  duration_ms: 0.28804
  ...
# Subtest: type encodings normalize like Bob; schema and choice order is significant
ok 978 - type encodings normalize like Bob; schema and choice order is significant
  ---
  duration_ms: 4.563854
  ...
# Subtest: album subprocess uses bobSpawnJson with vault, timeout, and bounded output
ok 979 - album subprocess uses bobSpawnJson with vault, timeout, and bounded output
  ---
  duration_ms: 4.343442
  ...
# Subtest: one vault-scoped list flight serves simultaneous subscribers
ok 980 - one vault-scoped list flight serves simultaneous subscribers
  ---
  duration_ms: 1.336672
  ...
# Subtest: a change during list fetch coalesces into one later generation
ok 981 - a change during list fetch coalesces into one later generation
  ---
  duration_ms: 1.110941
  ...
# Subtest: failed refresh keeps last good data stale and retries only on new demand
ok 982 - failed refresh keeps last good data stale and retries only on new demand
  ---
  duration_ms: 0.718903
  ...
# Subtest: unload clears subscriptions and prevents a late list result from repainting
ok 983 - unload clears subscriptions and prevents a late list result from repainting
  ---
  duration_ms: 1.038503
  ...
# Subtest: startup seeds frontmatter silently; only structural album edits debounce sync
ok 984 - startup seeds frontmatter silently; only structural album edits debounce sync
  ---
  duration_ms: 2.127221
  ...
# Subtest: record edits sync, body edits and unrelated notes do not
ok 985 - record edits sync, body edits and unrelated notes do not
  ---
  duration_ms: 1.631835
  ...
# Subtest: owner ancestry and type changes invalidate and sync; other owner edits do not
ok 986 - owner ancestry and type changes invalidate and sync; other owner edits do not
  ---
  duration_ms: 0.75961
  ...
# Subtest: deletion and rename schedule sync across membership boundaries
ok 987 - deletion and rename schedule sync across membership boundaries
  ---
  duration_ms: 0.619302
  ...
# Subtest: generated index writes do not restart a sync loop
ok 988 - generated index writes do not restart a sync loop
  ---
  duration_ms: 1.483032
  ...
# Subtest: a real frontmatter change during sync coalesces one trailing sync
ok 989 - a real frontmatter change during sync coalesces one trailing sync
  ---
  duration_ms: 1.480317
  ...
# Subtest: partial sync failure keeps its report and still revalidates the list
ok 990 - partial sync failure keeps its report and still revalidates the list
  ---
  duration_ms: 1.323938
  ...
# Subtest: sync waits out a pre-write list and then fetches a post-sync report
ok 991 - sync waits out a pre-write list and then fetches a post-sync report
  ---
  duration_ms: 1.080723
  ...
# Subtest: the trailing three-second sync fires once after schema and member edits
ok 992 - the trailing three-second sync fires once after schema and member edits
  ---
  duration_ms: 1.570549
  ...
# Subtest: a view-show demand refreshes the shared report and local-day rollover notifies
ok 993 - a view-show demand refreshes the shared report and local-day rollover notifies
  ---
  duration_ms: 1.15225
  ...
# Subtest: headless setup does not keep the process alive with a browser rollover timer
ok 994 - headless setup does not keep the process alive with a browser rollover timer
  ---
  duration_ms: 0.337404
  ...
# Subtest: real bob fixtures decode: healthy and broken albums in one vault
ok 995 - real bob fixtures decode: healthy and broken albums in one vault
  ---
  duration_ms: 225.631491
  ...
# Subtest: Areas host, row, hue, health, status, and unplaced models follow Bob's report
ok 996 - Areas host, row, hue, health, status, and unplaced models follow Bob's report
  ---
  duration_ms: 2.761372
  ...
# Subtest: Reading card paints reported hue dots, sync and root warning without editing Markdown
ok 997 - Reading card paints reported hue dots, sync and root warning without editing Markdown
  ---
  duration_ms: 4.946463
  ...
# Subtest: standalone cards show report rows; non-host and unavailable notes get no phantom card
ok 998 - standalone cards show report rows; non-host and unavailable notes get no phantom card
  ---
  duration_ms: 1.148443
  ...
# Subtest: standalone row nodes stay stable until rows, folds, or source path change
ok 999 - standalone row nodes stay stable until rows, folds, or source path change
  ---
  duration_ms: 1.787353
  ...
# Subtest: standalone area links open their target and request hover previews
ok 1000 - standalone area links open their target and request hover previews
  ---
  duration_ms: 0.938442
  ...
# Subtest: Areas renderer registers in Reading and Live Preview at the family priority
ok 1001 - Areas renderer registers in Reading and Live Preview at the family priority
  ---
  duration_ms: 89.071282
  ...
# Subtest: workspace scroll guard resets forbidden containers and logs once per window
ok 1002 - workspace scroll guard resets forbidden containers and logs once per window
  ---
  duration_ms: 14.293189
  ...
# Subtest: fold helpers default expanded and key by pane host plus row
ok 1003 - fold helpers default expanded and key by pane host plus row
  ---
  duration_ms: 0.165917
  ...
# Subtest: chips follow fold state and hide zeros; tooltips keep stems visible
ok 1004 - chips follow fold state and hide zeros; tooltips keep stems visible
  ---
  duration_ms: 0.614773
  ...
# Subtest: nested rows fold per map, switch chips, and keep stored stem link text
ok 1005 - nested rows fold per map, switch chips, and keep stored stem link text
  ---
  duration_ms: 6.272925
  ...
# Subtest: add-summary is hover-only in CSS and opens the notebooks summary path
ok 1006 - add-summary is hover-only in CSS and opens the notebooks summary path
  ---
  duration_ms: 29.596966
  ...
# Subtest: two panes keep independent folds across a repaint
ok 1007 - two panes keep independent folds across a repaint
  ---
  duration_ms: 3.971673
  ...
# Subtest: Areas list and sync use JSON argv and strict schema-1 report decoders
ok 1008 - Areas list and sync use JSON argv and strict schema-1 report decoders
  ---
  duration_ms: 9.453368
  ...
# Subtest: relevance is limited to area, project, root, and today's note
ok 1009 - relevance is limited to area, project, root, and today's note
  ---
  duration_ms: 0.920187
  ...
# Subtest: report refreshes are debounced, stale rows survive a failed refresh, and sync is explicit
ok 1010 - report refreshes are debounced, stale rows survive a failed refresh, and sync is explicit
  ---
  duration_ms: 3.702067
  ...
# Subtest: missing bob waits for new demand instead of polling every debounce interval
ok 1011 - missing bob waits for new demand instead of polling every debounce interval
  ---
  duration_ms: 0.80133
  ...
# Subtest: failed invalidation refresh keeps cached rows and concurrent waiters settle without another attempt
ok 1012 - failed invalidation refresh keeps cached rows and concurrent waiters settle without another attempt
  ---
  duration_ms: 1.154074
  ...
# Subtest: a vault change during a failed fetch still gets one refresh for the newer generation
ok 1013 - a vault change during a failed fetch still gets one refresh for the newer generation
  ---
  duration_ms: 1.200291
  ...
# Subtest: api.attachments v1 sends origin and import requests to bob
ok 1014 - api.attachments v1 sends origin and import requests to bob
  ---
  duration_ms: 2.497929
  ...
# Subtest: origin and import decoders validate schema and payload shape
ok 1015 - origin and import decoders validate schema and payload shape
  ---
  duration_ms: 0.588704
  ...
# Subtest: attachment API preserves bob payloads through bobSpawnJson
ok 1016 - attachment API preserves bob payloads through bobSpawnJson
  ---
  duration_ms: 5.904462
  ...
# Subtest: attachment API passes bob JSON failures through
ok 1017 - attachment API passes bob JSON failures through
  ---
  duration_ms: 2.3831
  ...
# Subtest: attachment API refuses mobile calls and never rejects
ok 1018 - attachment API refuses mobile calls and never rejects
  ---
  duration_ms: 0.465729
  ...
# Subtest: ensure argv never passes -o and ack argv carries only deduped IDs
ok 1019 - ensure argv never passes -o and ack argv carries only deduped IDs
  ---
  duration_ms: 2.208146
  ...
# Subtest: ensure and ack decoders reject bad shapes without claiming success
ok 1020 - ensure and ack decoders reject bad shapes without claiming success
  ---
  duration_ms: 0.966445
  ...
# Subtest: source rows expose bank ids; other block ids stay plain block ids
ok 1021 - source rows expose bank ids; other block ids stay plain block ids
  ---
  duration_ms: 2.046598
  ...
# Subtest: day snapshots carry exact waiting IDs and count ID-less rows
ok 1022 - day snapshots carry exact waiting IDs and count ID-less rows
  ---
  duration_ms: 0.670871
  ...
# Subtest: ack summaries never claim a full day while ID-less rows remain
ok 1023 - ack summaries never claim a full day while ID-less rows remain
  ---
  duration_ms: 0.307837
  ...
# Subtest: cursor day context follows heading boundaries, not fallback lines
ok 1024 - cursor day context follows heading boundaries, not fallback lines
  ---
  duration_ms: 72.378523
  ...
# Subtest: guarded checkbox plans verify the exact displayed row and day context
ok 1025 - guarded checkbox plans verify the exact displayed row and day context
  ---
  duration_ms: 0.920367
  ...
# Subtest: Enter continues only complete rows and clears only empty stubs
ok 1026 - Enter continues only complete rows and clears only empty stubs
  ---
  duration_ms: 0.485687
  ...
# Subtest: category completions keep declared order and insert only keys
ok 1027 - category completions keep declared order and insert only keys
  ---
  duration_ms: 0.585228
  ...
# Subtest: action commands register without default hotkeys
ok 1028 - action commands register without default hotkeys
  ---
  duration_ms: 0.799246
  ...
# Subtest: ack submits the exact snapshot IDs and reports remaining ID-less rows
ok 1029 - ack submits the exact snapshot IDs and reports remaining ID-less rows
  ---
  duration_ms: 15.720995
  ...
# Subtest: ack refuses empty selections, busy locks, and failures without refresh
ok 1030 - ack refuses empty selections, busy locks, and failures without refresh
  ---
  duration_ms: 1.150216
  ...
# Subtest: acknowledge-day snapshots the cursor day and never falls back to ack -D
ok 1031 - acknowledge-day snapshots the cursor day and never falls back to ack -D
  ---
  duration_ms: 1.37275
  ...
# Subtest: ensure opens the returned path and lands the cursor on the next row
ok 1032 - ensure opens the returned path and lands the cursor on the next row
  ---
  duration_ms: 1.222253
  ...
# Subtest: guarded ID-less edits flip one byte only when the snapshot still matches
ok 1033 - guarded ID-less edits flip one byte only when the snapshot still matches
  ---
  duration_ms: 0.444068
  ...
# Subtest: snippet expansion never rewrites bank rows
ok 1034 - snippet expansion never rewrites bank rows
  ---
  duration_ms: 0.311345
  ...
# Subtest: Enter handling inserts rows and clears stubs through the real editor
ok 1035 - Enter handling inserts rows and clears stubs through the real editor
  ---
  duration_ms: 0.49742
  ...
# Subtest: strip, badge, and period hosts land on period fences; day fences keep two
ok 1036 - strip, badge, and period hosts land on period fences; day fences keep two
  ---
  duration_ms: 211.594383
  ...
# Subtest: a strip repaint keeps the badge node
ok 1037 - a strip repaint keeps the badge node
  ---
  duration_ms: 93.364208
  ...
# Subtest: each strip kind fetches the matching bank report args
ok 1038 - each strip kind fetches the matching bank report args
  ---
  duration_ms: 337.975415
  ...
# Subtest: fence badges wait for visibility and skip future periods
ok 1039 - fence badges wait for visibility and skip future periods
  ---
  duration_ms: 108.165898
  ...
# Subtest: older bob -p refusals hide the host and warn once
ok 1040 - older bob -p refusals hide the host and warn once
  ---
  duration_ms: 94.857229
  ...
# Subtest: unload unsubscribes and pref off clears every fence badge
ok 1041 - unload unsubscribes and pref off clears every fence badge
  ---
  duration_ms: 151.46755
  ...
# Subtest: hidden fences subscribe once they become visible without an observer
ok 1042 - hidden fences subscribe once they become visible without an observer
  ---
  duration_ms: 457.872671
  ...
# Subtest: day fences retry badge subscription when shown later without an observer
ok 1043 - day fences retry badge subscription when shown later without an observer
  ---
  duration_ms: 386.050329
  ...
# Subtest: losing periodId in the host adapter cannot silently undo validation
ok 1044 - losing periodId in the host adapter cannot silently undo validation
  ---
  duration_ms: 222.748317
  ...
# Subtest: opening a waiting badge row selects family b and sets the walk anchor
ok 1045 - opening a waiting badge row selects family b and sets the walk anchor
  ---
  duration_ms: 80.646248
  ...
# Subtest: heading and hub badge opens leave the family and walk anchor alone
ok 1046 - heading and hub badge opens leave the family and walk anchor alone
  ---
  duration_ms: 47.073211
  ...
# Subtest: old nav still anchors a waiting badge open and skips select
ok 1047 - old nav still anchors a waiting badge open and skips select
  ---
  duration_ms: 140.607135
  ...
# Subtest: bank card fence and filename frontmatter validation are explicit
ok 1048 - bank card fence and filename frontmatter validation are explicit
  ---
  duration_ms: 3.446039
  ...
# Subtest: unknown bob-bank views render nothing
ok 1049 - unknown bob-bank views render nothing
  ---
  duration_ms: 10.907796
  ...
# Subtest: month card model keeps Bob totals, ordered category shares, account caveats, and waiting row
ok 1050 - month card model keeps Bob totals, ordered category shares, account caveats, and waiting row
  ---
  duration_ms: 1.553406
  ...
# Subtest: heat strip is Monday-first, includes the whole month, and ties share a quantile
ok 1051 - heat strip is Monday-first, includes the whole month, and ties share a quantile
  ---
  duration_ms: 0.596258
  ...
# Subtest: queue model sorts oldest-first, snapshots displayed IDs, and bounds existing month footer to six
ok 1052 - queue model sorts oldest-first, snapshots displayed IDs, and bounds existing month footer to six
  ---
  duration_ms: 12.851065
  ...
# Subtest: bank badge model hides empty periods and selects copy and tone from counted cents
ok 1053 - bank badge model hides empty periods and selects copy and tone from counted cents
  ---
  duration_ms: 6.440255
  ...
# Subtest: bank badge rejects mismatches, hides teaching-empty and future reports, and keeps stale state
ok 1054 - bank badge rejects mismatches, hides teaching-empty and future reports, and keeps stale state
  ---
  duration_ms: 0.955525
  ...
# Subtest: bank badge enforces period identity at the boundary
ok 1055 - bank badge enforces period identity at the boundary
  ---
  duration_ms: 6.616334
  ...
# Subtest: bank badge quarter amounts round half up but preserve nonzero cents below one dollar
ok 1056 - bank badge quarter amounts round half up but preserve nonzero cents below one dollar
  ---
  duration_ms: 0.855564
  ...
# Subtest: bank badge coverage copy handles partial starts, short imports, both bounds, and all time
ok 1057 - bank badge coverage copy handles partial starts, short imports, both bounds, and all time
  ---
  duration_ms: 0.660571
  ...
# Subtest: bank badge chooses waiting, strip-first, one-month, hub, and old-bob targets
ok 1058 - bank badge chooses waiting, strip-first, one-month, hub, and old-bob targets
  ---
  duration_ms: 0.908856
  ...
# Subtest: today-only all-month waiting is tooltip-only
ok 1059 - today-only all-month waiting is tooltip-only
  ---
  duration_ms: 0.200473
  ...
# Subtest: bank badge painter uses one accessible span, joins present parts, and leaves hidden hosts empty
ok 1060 - bank badge painter uses one accessible span, joins present parts, and leaves hidden hosts empty
  ---
  duration_ms: 56.906344
  ...
# Subtest: month card renders report data and disables days without real headings
ok 1061 - month card renders report data and disables days without real headings
  ---
  duration_ms: 122.588463
  ...
# Subtest: queue card keeps account caveats visible, lists bounded report months, and sends its drawn ID snapshot
ok 1062 - queue card keeps account caveats visible, lists bounded report months, and sends its drawn ID snapshot
  ---
  duration_ms: 3.406615
  ...
# Subtest: queue card paints a subscription chip after the category
ok 1063 - queue card paints a subscription chip after the category
  ---
  duration_ms: 1.07329
  ...
# Subtest: missing day headings and changed row snapshots cannot navigate to fallback line one
ok 1064 - missing day headings and changed row snapshots cannot navigate to fallback line one
  ---
  duration_ms: 4.778814
  ...
# Subtest: daily badge mounts after the day strip and click opens its read-only target
ok 1065 - daily badge mounts after the day strip and click opens its read-only target
  ---
  duration_ms: 7.865105
  ...
# Subtest: daily badge is hidden without bank.md and follows the cached persistent default-on preference
ok 1066 - daily badge is hidden without bank.md and follows the cached persistent default-on preference
  ---
  duration_ms: 18.105876
  ...
# Subtest: stats.bank_badge overrides the stats.bank_chip legacy alias, which defaults on
ok 1067 - stats.bank_badge overrides the stats.bank_chip legacy alias, which defaults on
  ---
  duration_ms: 7.529546
  ...
# Subtest: badge modifier navigation opens a new leaf without saving a bank note
ok 1068 - badge modifier navigation opens a new leaf without saving a bank note
  ---
  duration_ms: 0.783766
  ...
# Subtest: disabled render children unsubscribe and unload blocks later repaint
ok 1069 - disabled render children unsubscribe and unload blocks later repaint
  ---
  duration_ms: 3.519961
  ...
# Subtest: bank UI keeps narrow-pane stacking and badge CSS has the approved tones and focus
ok 1070 - bank UI keeps narrow-pane stacking and badge CSS has the approved tones and focus
  ---
  duration_ms: 7.818948
  ...
# Subtest: bank card actions use the public API, while badges navigate without ensure writes
ok 1071 - bank card actions use the public API, while badges navigate without ensure writes
  ---
  duration_ms: 4.63081
  ...
# Subtest: the modal key contract dispatches every action in close and set modes
ok 1072 - the modal key contract dispatches every action in close and set modes
  ---
  duration_ms: 7.905042
  ...
# Subtest: new-category lockNotice paints without Preview again and keeps Save
ok 1073 - new-category lockNotice paints without Preview again and keeps Save
  ---
  duration_ms: 1.047499
  ...
# Subtest: plus opens the new-category stage and letters no longer file
ok 1074 - plus opens the new-category stage and letters no longer file
  ---
  duration_ms: 0.932961
  ...
# Subtest: the opening chord and landing lock swallow repeated Ctrl+Enter
ok 1075 - the opening chord and landing lock swallow repeated Ctrl+Enter
  ---
  duration_ms: 0.580218
  ...
# Subtest: old Bob uses arrow navigation and Enter when no category has a hotkey
ok 1076 - old Bob uses arrow navigation and Enter when no category has a hotkey
  ---
  duration_ms: 0.496347
  ...
# Subtest: hidden categories are absent from completions and one line edit combines the write
ok 1077 - hidden categories are absent from completions and one line edit combines the write
  ---
  duration_ms: 2.634872
  ...
# Subtest: api.bank v2 exposes guarded close and set-category actions plus the command
ok 1078 - api.bank v2 exposes guarded close and set-category actions plus the command
  ---
  duration_ms: 1.088228
  ...
# Subtest: close commits once, refreshes, and lands at the next payee in the same note
ok 1079 - close commits once, refreshes, and lands at the next payee in the same note
  ---
  duration_ms: 6.724508
  ...
# Subtest: a rejected month refresh after a successful close still clears waitingRefresh
ok 1080 - a rejected month refresh after a successful close still clears waitingRefresh
  ---
  duration_ms: 1.707169
  ...
# Subtest: a landed context exposes cardRow so a learned report highlights for Ctrl+Enter
ok 1081 - a landed context exposes cardRow so a learned report highlights for Ctrl+Enter
  ---
  duration_ms: 1.223075
  ...
# Subtest: a close landing records a jump when nav provides recordJump
ok 1082 - a close landing records a jump when nav provides recordJump
  ---
  duration_ms: 1.341031
  ...
# Subtest: claimRowClose focuses an open card and swallows the lock instead of flipping
ok 1083 - claimRowClose focuses an open card and swallows the lock instead of flipping
  ---
  duration_ms: 0.347724
  ...
# Subtest: the painted root uses bob-bank-category-card and not the month-card token
ok 1084 - the painted root uses bob-bank-category-card and not the month-card token
  ---
  duration_ms: 2.328275
  ...
# Subtest: the header puts amount first, inflows show +, and progress names the month
ok 1085 - the header puts amount first, inflows show +, and progress names the month
  ---
  duration_ms: 7.303463
  ...
# Subtest: tiles render keycaps, aria-keyshortcuts, and a live region after filing
ok 1086 - tiles render keycaps, aria-keyshortcuts, and a live region after filing
  ---
  duration_ms: 1.813071
  ...
# Subtest: the subscription context strip sits above tiles and the picker exposes an accessible list
ok 1087 - the subscription context strip sits above tiles and the picker exposes an accessible list
  ---
  duration_ms: 2.093216
  ...
# Subtest: the completion state paints the other-month ]b walk line
ok 1088 - the completion state paints the other-month ]b walk line
  ---
  duration_ms: 0.643799
  ...
# Subtest: restricted mode shows only acknowledge keys and the loading reason
ok 1089 - restricted mode shows only acknowledge keys and the loading reason
  ---
  duration_ms: 0.59208
  ...
# Subtest: set-category replaces the category without ticking or advancing
ok 1090 - set-category replaces the category without ticking or advancing
  ---
  duration_ms: 1.014657
  ...
# Subtest: a successful close saves the note before requesting a refresh
ok 1091 - a successful close saves the note before requesting a refresh
  ---
  duration_ms: 1.422215
  ...
# Subtest: a throwing save still refreshes after a successful close
ok 1092 - a throwing save still refreshes after a successful close
  ---
  duration_ms: 1.100591
  ...
# Subtest: the scope catch-all is registered once and replaces the contentEl keydown listener
ok 1093 - the scope catch-all is registered once and replaces the contentEl keydown listener
  ---
  duration_ms: 0.574146
  ...
# Subtest: real-path scope keys file, accept, and move while swallowing every key
ok 1094 - real-path scope keys file, accept, and move while swallowing every key
  ---
  duration_ms: 25.151018
  ...
# Subtest: unbound scope keys are swallowed with no filing and the card stays open
ok 1095 - unbound scope keys are swallowed with no filing and the card stays open
  ---
  duration_ms: 12.694375
  ...
# Subtest: modifier letters never file while Shift+letter still files
ok 1096 - modifier letters never file while Shift+letter still files
  ---
  duration_ms: 8.789792
  ...
# Subtest: held-key repeats never file but repeats still move the highlight
ok 1097 - held-key repeats never file but repeats still move the highlight
  ---
  duration_ms: 58.542648
  ...
# Subtest: busy, waiting, and summary states swallow scope keys with no action
ok 1098 - busy, waiting, and summary states swallow scope keys with no action
  ---
  duration_ms: 2.966083
  ...
# Subtest: onClose unregisters the scope catch-all
ok 1099 - onClose unregisters the scope catch-all
  ---
  duration_ms: 0.187589
  ...
# Subtest: without a scope the fallback contentEl keydown listener still files
ok 1100 - without a scope the fallback contentEl keydown listener still files
  ---
  duration_ms: 0.292899
  ...
# Subtest: decode keeps hotkey, group, hidden, and suggestion; old bob degrades
ok 1101 - decode keeps hotkey, group, hidden, and suggestion; old bob degrades
  ---
  duration_ms: 17.827625
  ...
# Subtest: card sections follow first-appearance order; hidden never renders; inflow reorders
ok 1102 - card sections follow first-appearance order; hidden never renders; inflow reorders
  ---
  duration_ms: 2.046427
  ...
# Subtest: highlight follows row category then suggestion; each footer variant
ok 1103 - highlight follows row category then suggestion; each footer variant
  ---
  duration_ms: 1.412426
  ...
# Subtest: key table is case-insensitive; q/Esc cancel; chord and lock are pure state
ok 1104 - key table is case-insensitive; q/Esc cancel; chord and lock are pure state
  ---
  duration_ms: 0.477762
  ...
# Subtest: write planner inserts, replaces, and removes in one line; refusals carry the notice
ok 1105 - write planner inserts, replaces, and removes in one line; refusals carry the notice
  ---
  duration_ms: 3.527476
  ...
# Subtest: write planner resolves imported rows by ID and handles CRLF
ok 1106 - write planner resolves imported rows by ID and handles CRLF
  ---
  duration_ms: 0.509594
  ...
# Subtest: next-waiting finder walks in order, wraps once, and skips non-rows
ok 1107 - next-waiting finder walks in order, wraps once, and skips non-rows
  ---
  duration_ms: 0.912893
  ...
# Subtest: session counts progress and the summary owns every number
ok 1108 - session counts progress and the summary owns every number
  ---
  duration_ms: 0.715406
  ...
# Subtest: other-month walk line names the oldest waiting month from the snapshot
ok 1109 - other-month walk line names the oldest waiting month from the snapshot
  ---
  duration_ms: 1.946997
  ...
# Subtest: close advances in note order and anchors the landed waiting row
ok 1110 - close advances in note order and anchors the landed waiting row
  ---
  duration_ms: 2.8125
  ...
# Subtest: completing a month anchors the last filed row and surfaces the other-month ]b line
ok 1111 - completing a month anchors the last filed row and surfaces the other-month ]b line
  ---
  duration_ms: 2.070393
  ...
# Subtest: completion omits the other-month ]b line when the snapshot has no other waiting months
ok 1112 - completion omits the other-month ]b line when the snapshot has no other waiting months
  ---
  duration_ms: 1.166777
  ...
# Subtest: update argv, envelope, and timeout follow the guarded writer contract
ok 1113 - update argv, envelope, and timeout follow the guarded writer contract
  ---
  duration_ms: 2.496426
  ...
# Subtest: update decoder keeps typed refusals and the derived stored key
ok 1114 - update decoder keeps typed refusals and the derived stored key
  ---
  duration_ms: 1.462733
  ...
# Subtest: list and report keep config_fingerprint for the guarded expect
ok 1115 - list and report keep config_fingerprint for the guarded expect
  ---
  duration_ms: 0.5764
  ...
# Subtest: stdin carries shell-looking labels byte-identical and never as shell text
ok 1116 - stdin carries shell-looking labels byte-identical and never as shell text
  ---
  duration_ms: 3.948638
  ...
# Subtest: own bank.md echo is suppressed while apply is in flight
ok 1117 - own bank.md echo is suppressed while apply is in flight
  ---
  duration_ms: 0.717871
  ...
# Subtest: preview debounce, matching apply, and double Enter share one flight
ok 1118 - preview debounce, matching apply, and double Enter share one flight
  ---
  duration_ms: 19.035972
  ...
# Subtest: Enter is inert without a matching preview; apply failure files nothing
ok 1119 - Enter is inert without a matching preview; apply failure files nothing
  ---
  duration_ms: 0.914476
  ...
# Subtest: stale_config rebases; sync retry never replays the mutation
ok 1120 - stale_config rebases; sync retry never replays the mutation
  ---
  duration_ms: 1.330831
  ...
# Subtest: stage defaults the group, cycles it, and keeps taken or reserved keys inert
ok 1121 - stage defaults the group, cycles it, and keeps taken or reserved keys inert
  ---
  duration_ms: 1.461862
  ...
# Subtest: + and = open the stage; letters type; they never file; Esc closes the stage first
ok 1122 - + and = open the stage; letters type; they never file; Esc closes the stage first
  ---
  duration_ms: 3.144093
  ...
# Subtest: the new-category tile click opens the stage; missing fingerprint refuses
ok 1123 - the new-category tile click opens the stage; missing fingerprint refuses
  ---
  duration_ms: 0.582643
  ...
# Subtest: Enter is inert on a taken key and without a matching preview
ok 1124 - Enter is inert on a taken key and without a matching preview
  ---
  duration_ms: 0.776202
  ...
# Subtest: apply-then-file uses the derived key and one choose; failure files nothing
ok 1125 - apply-then-file uses the derived key and one choose; failure files nothing
  ---
  duration_ms: 1.098708
  ...
# Subtest: setCategories repaints after interaction; setReport stays ignored then
ok 1126 - setCategories repaints after interaction; setReport stays ignored then
  ---
  duration_ms: 0.419871
  ...
# Subtest: bank lock_busy waits then retries the same envelope
ok 1127 - bank lock_busy waits then retries the same envelope
  ---
  duration_ms: 3.261376
  ...
# Subtest: the bank service skips forced revalidate on lock_busy
ok 1128 - the bank service skips forced revalidate on lock_busy
  ---
  duration_ms: 1.071085
  ...
# Subtest: new-category Esc during a lock wait stops waiting and keeps the stage open
ok 1129 - new-category Esc during a lock wait stops waiting and keeps the stage open
  ---
  duration_ms: 0.611697
  ...
# Subtest: apply-busy refuses a second plugin apply; timeout is never a blind retry
ok 1130 - apply-busy refuses a second plugin apply; timeout is never a blind retry
  ---
  duration_ms: 5.093825
  ...
# Subtest: bank subprocess uses bobSpawnJson with vault, timeout, and bounded output
ok 1131 - bank subprocess uses bobSpawnJson with vault, timeout, and bounded output
  ---
  duration_ms: 85.656755
  ...
# Subtest: shared bob spawn maps missing binary and timeout failures
ok 1132 - shared bob spawn maps missing binary and timeout failures
  ---
  duration_ms: 1.940655
  ...
# Subtest: bank cache returns stale data while revalidating and keeps a bounded LRU
ok 1133 - bank cache returns stale data while revalidating and keeps a bounded LRU
  ---
  duration_ms: 3.988424
  ...
# Subtest: identical list flights coalesce and different keys spawn in parallel
ok 1134 - identical list flights coalesce and different keys spawn in parallel
  ---
  duration_ms: 0.802623
  ...
# Subtest: a late older generation cannot overwrite a newer cached report
ok 1135 - a late older generation cannot overwrite a newer cached report
  ---
  duration_ms: 0.480497
  ...
# Subtest: failed refresh keeps last good data stale without a retry loop
ok 1136 - failed refresh keeps last good data stale without a retry loop
  ---
  duration_ms: 0.504573
  ...
# Subtest: only hub and canonical month notes invalidate, and debounce coalesces
ok 1137 - only hub and canonical month notes invalidate, and debounce coalesces
  ---
  duration_ms: 2.233664
  ...
# Subtest: config apply refreshes once, updates other mounts, and retains newer invalidations
ok 1138 - config apply refreshes once, updates other mounts, and retains newer invalidations
  ---
  duration_ms: 7.108531
  ...
# Subtest: local midnight bumps generation and command-mode bank tag invalidates
ok 1139 - local midnight bumps generation and command-mode bank tag invalidates
  ---
  duration_ms: 1.092105
  ...
# Subtest: unload clears mounts and a late result cannot repaint
ok 1140 - unload clears mounts and a late result cannot repaint
  ---
  duration_ms: 0.765081
  ...
# Subtest: headless setup does not keep the process alive with a browser rollover timer
ok 1141 - headless setup does not keep the process alive with a browser rollover timer
  ---
  duration_ms: 11.936718
  ...
# Subtest: bank argv is keyed by command and exact flags
ok 1142 - bank argv is keyed by command and exact flags
  ---
  duration_ms: 3.782032
  ...
# Subtest: list decoder accepts the waiting fixture and keeps integer cents
ok 1143 - list decoder accepts the waiting fixture and keeps integer cents
  ---
  duration_ms: 1.15758
  ...
# Subtest: report decoder preserves transfers, cash, inflows, and account caveats
ok 1144 - report decoder preserves transfers, cash, inflows, and account caveats
  ---
  duration_ms: 1.145466
  ...
# Subtest: report decoder validates and passes through optional badge coverage and navigation
ok 1145 - report decoder validates and passes through optional badge coverage and navigation
  ---
  duration_ms: 2.404521
  ...
# Subtest: teaching-empty is success and never a zero-dollar report
ok 1146 - teaching-empty is success and never a zero-dollar report
  ---
  duration_ms: 0.410814
  ...
# Subtest: malformed JSON, schema mismatch, and bob errors never become zero success
ok 1147 - malformed JSON, schema mismatch, and bob errors never become zero success
  ---
  duration_ms: 0.390596
  ...
# Subtest: non-integer cents and numeric payees are rejected
ok 1148 - non-integer cents and numeric payees are rejected
  ---
  duration_ms: 0.778065
  ...
# Subtest: cent formatting is exact and presentation models do not invent totals
ok 1149 - cent formatting is exact and presentation models do not invent totals
  ---
  duration_ms: 0.593033
  ...
# Subtest: bank error cards explain not-found, timeout, schema, and bob errors
ok 1150 - bank error cards explain not-found, timeout, schema, and bob errors
  ---
  duration_ms: 2.340157
  ...
# Subtest: reports without charts decode exactly as today
ok 1151 - reports without charts decode exactly as today
  ---
  duration_ms: 1.408889
  ...
# Subtest: charts decoder accepts a week payload and rejects malformed values with bad-shape
ok 1152 - charts decoder accepts a week payload and rejects malformed values with bad-shape
  ---
  duration_ms: 5.838928
  ...
# Subtest: charts decoder accepts ISO-year groups and null all-time charts
ok 1153 - charts decoder accepts ISO-year groups and null all-time charts
  ---
  duration_ms: 12.336162
  ...
# Subtest: compose and split round-trip fused labels including ZWJ and flags
ok 1154 - compose and split round-trip fused labels including ZWJ and flags
  ---
  duration_ms: 66.877702
  ...
# Subtest: a rename keeps the emoji and an explicit clear removes it
ok 1155 - a rename keeps the emoji and an explicit clear removes it
  ---
  duration_ms: 0.562695
  ...
# Subtest: bank vocabulary is every category emoji; siblings skip hidden and the row being edited
ok 1156 - bank vocabulary is every category emoji; siblings skip hidden and the row being edited
  ---
  duration_ms: 0.574907
  ...
# Subtest: an open panel's Enter picks and never files a new category
ok 1157 - an open panel's Enter picks and never files a new category
  ---
  duration_ms: 1.491628
  ...
# Subtest: the fused slot falls back without bob-emoji and keeps the enable-search hint
ok 1158 - the fused slot falls back without bob-emoji and keeps the enable-search hint
  ---
  duration_ms: 113.267137
  ...
# Subtest: the fused hint shows for an empty slot and follows open, pick, and clear
ok 1159 - the fused hint shows for an empty slot and follows open, pick, and clear
  ---
  duration_ms: 18.612656
  ...
# Subtest: the hint stays hidden for filled, disabled, and fallback slots; the Category card shows it
ok 1160 - the hint stays hidden for filled, disabled, and fallback slots; the Category card shows it
  ---
  duration_ms: 0.894217
  ...
# Subtest: glyph-well stylesheet beats Obsidian button chrome with no hex colors
ok 1161 - glyph-well stylesheet beats Obsidian button chrome with no hex colors
  ---
  duration_ms: 2.46216
  ...
# Subtest: Ctrl+N steps the shared slot by one and the card keeps the key
ok 1162 - Ctrl+N steps the shared slot by one and the card keeps the key
  ---
  duration_ms: 15.925144
  ...
# Subtest: Ctrl+[ closes the open bank Emoji Slot like Esc while q in the search types
ok 1163 - Ctrl+[ closes the open bank Emoji Slot like Esc while q in the search types
  ---
  duration_ms: 0.676722
  ...
# Subtest: tokenizer covers amount variants and tail order including flags, notes, links, and ids
ok 1164 - tokenizer covers amount variants and tail order including flags, notes, links, and ids
  ---
  duration_ms: 2.993545
  ...
# Subtest: source scan never consumes indented children, fences, or ordinary prose
ok 1165 - source scan never consumes indented children, fences, or ordinary prose
  ---
  duration_ms: 1.970301
  ...
# Subtest: presentation keeps unknown labels, greens inflows, and replaces only imported bank ids
ok 1166 - presentation keeps unknown labels, greens inflows, and replaces only imported bank ids
  ---
  duration_ms: 0.60268
  ...
# Subtest: real day headings get report totals or muted nothing posted; missing days stay absent
ok 1167 - real day headings get report totals or muted nothing posted; missing days stay absent
  ---
  duration_ms: 0.875912
  ...
# Subtest: two nearby bank-row dollars form a math conflict; ordinary math is left alone
ok 1168 - two nearby bank-row dollars form a math conflict; ordinary math is left alone
  ---
  duration_ms: 0.5814
  ...
# Subtest: reading-view math unwrap restores bank amounts and leaves ordinary math intact
ok 1169 - reading-view math unwrap restores bank amounts and leaves ordinary math intact
  ---
  duration_ms: 2.553204
  ...
# Subtest: Live Preview replaces amounts off the cursor line, reveals on it, and skips Source mode and code
ok 1170 - Live Preview replaces amounts off the cursor line, reveals on it, and skips Source mode and code
  ---
  duration_ms: 7.592986
  ...
# Subtest: toggle, config, and popout gate control decorations together; math dollars remain when marks are off
ok 1171 - toggle, config, and popout gate control decorations together; math dollars remain when marks are off
  ---
  duration_ms: 1.028043
  ...
# Subtest: Reading view is idempotent, preserves links, and does not rewrite note bytes
ok 1172 - Reading view is idempotent, preserves links, and does not rewrite note bytes
  ---
  duration_ms: 2.878886
  ...
# Subtest: hub property hiding is owned by the setup surface, never by bank marks
ok 1173 - hub property hiding is owned by the setup surface, never by bank marks
  ---
  duration_ms: 1.257842
  ...
# Subtest: Live Preview replaces a 🔁 wikilink with a subscription chip and parks a ghost widget
ok 1174 - Live Preview replaces a 🔁 wikilink with a subscription chip and parks a ghost widget
  ---
  duration_ms: 3.088207
  ...
# Subtest: Reading view wraps a 🔁 internal-link and appends a ghost that restore removes
ok 1175 - Reading view wraps a 🔁 internal-link and appends a ghost that restore removes
  ---
  duration_ms: 2.708702
  ...
# Subtest: cursor reveal helper and note bytes stay unchanged after tokenize
ok 1176 - cursor reveal helper and note bytes stay unchanged after tokenize
  ---
  duration_ms: 0.365147
  ...
# Subtest: malformed balances warn once and never fail the report
ok 1177 - malformed balances warn once and never fail the report
  ---
  duration_ms: 78.553422
  ...
# Subtest: balances decode: absent stays absent, null stays null, valid normalizes
ok 1178 - balances decode: absent stays absent, null stays null, valid normalizes
  ---
  duration_ms: 1.682422
  ...
# Subtest: balance model: as_of golden with tooltip, aria, and activation
ok 1179 - balance model: as_of golden with tooltip, aria, and activation
  ---
  duration_ms: 2.082075
  ...
# Subtest: balance model: settled names the close and drops the not-imported line
ok 1180 - balance model: settled names the close and drops the not-imported line
  ---
  duration_ms: 0.395736
  ...
# Subtest: balance model: so_far says so far, flags stale, and reads today
ok 1181 - balance model: so_far says so far, flags stale, and reads today
  ---
  duration_ms: 0.606849
  ...
# Subtest: balance model: words states, negative and zero amounts
ok 1182 - balance model: words states, negative and zero amounts
  ---
  duration_ms: 1.731014
  ...
# Subtest: balance model: delta status adds a ledger line; null without hero or numbers
ok 1183 - balance model: delta status adds a ledger line; null without hero or numbers
  ---
  duration_ms: 0.646184
  ...
# Subtest: charts model: older-bob, missing hero, and none stay byte-identical
ok 1184 - charts model: older-bob, missing hero, and none stay byte-identical
  ---
  duration_ms: 58.897006
  ...
# Subtest: charts model: quiet weeks and waiting-badge weeks become header-only balance states
ok 1185 - charts model: quiet weeks and waiting-badge weeks become header-only balance states
  ---
  duration_ms: 46.34974
  ...
# Subtest: paint: header order, link role, and inert balance
ok 1186 - paint: header order, link role, and inert balance
  ---
  duration_ms: 101.979798
  ...
# Subtest: paint: header-only root, waiting line, and collapsed panels
ok 1187 - paint: header-only root, waiting line, and collapsed panels
  ---
  duration_ms: 2.487198
  ...
# Subtest: real bob JSON decodes into models and paints through the period host
ok 1188 - real bob JSON decodes into models and paints through the period host
  ---
  duration_ms: 193.315964
  ...
# Subtest: only non-day strip fences mount a third host, and future or unsupported hosts do not subscribe
ok 1189 - only non-day strip fences mount a third host, and future or unsupported hosts do not subscribe
  ---
  duration_ms: 166.013209
  ...
# Subtest: the period fetch waits for visibility and has a cache key separate from the badge
ok 1190 - the period fetch waits for visibility and has a cache key separate from the badge
  ---
  duration_ms: 96.139127
  ...
# Subtest: the no-observer hidden-to-shown retry subscribes once
ok 1191 - the no-observer hidden-to-shown retry subscribes once
  ---
  duration_ms: 40.807348
  ...
# Subtest: bank_period and bank_badge gate independently; older bob warns once
ok 1192 - bank_period and bank_badge gate independently; older bob warns once
  ---
  duration_ms: 77.139153
  ...
# Subtest: read-only navigation, isolated repaint, persistence, and release work
ok 1193 - read-only navigation, isolated repaint, persistence, and release work
  ---
  duration_ms: 398.54259
  ...
# Subtest: the panel's waiting link hands the row to bank walk family b like the badge
ok 1194 - the panel's waiting link hands the row to bank walk family b like the badge
  ---
  duration_ms: 260.33236
  ...
# Subtest: compact labels follow the k/m ladder and keep sub-dollar cents
ok 1195 - compact labels follow the k/m ladder and keep sub-dollar cents
  ---
  duration_ms: 9.847341
  ...
# Subtest: invalid persisted view and collapsed values fall back to both / expanded
ok 1196 - invalid persisted view and collapsed values fall back to both / expanded
  ---
  duration_ms: 23.226363
  ...
# Subtest: panel model states: teaching-empty, older-bob, unavailable, empty, waiting, charts, stale
ok 1197 - panel model states: teaching-empty, older-bob, unavailable, empty, waiting, charts, stale
  ---
  duration_ms: 11.751776
  ...
# Subtest: hide rule with the badge on and off, and waiting-only copy
ok 1198 - hide rule with the badge on and off, and waiting-only copy
  ---
  duration_ms: 0.894829
  ...
# Subtest: today's real shape: one counted day, six awaiting_import, $249.77 out
ok 1199 - today's real shape: one counted day, six awaiting_import, $249.77 out
  ---
  duration_ms: 2.436983
  ...
# Subtest: in-only shows cashflow and hides the view switch
ok 1200 - in-only shows cashflow and hides the view switch
  ---
  duration_ms: 6.779423
  ...
# Subtest: week markers hang Out below the line; mirrored ratios collapse a zero side
ok 1201 - week markers hang Out below the line; mirrored ratios collapse a zero side
  ---
  duration_ms: 2.840042
  ...
# Subtest: categories keep pinned cash/unclassified, rest, and the one-leftover series row
ok 1202 - categories keep pinned cash/unclassified, rest, and the one-leftover series row
  ---
  duration_ms: 2.146959
  ...
# Subtest: every bucket state has words, decorations, and table-twin rows
ok 1203 - every bucket state has words, decorations, and table-twin rows
  ---
  duration_ms: 2.00637
  ...
# Subtest: period identity uses the badge rule: wrong key or right key with wrong bounds
ok 1204 - period identity uses the badge rule: wrong key or right key with wrong bounds
  ---
  duration_ms: 0.82223
  ...
# Subtest: 14-week Q4, 53-week ISO year fallback, all-time leading ghost, year grain, null charts, single bucket
ok 1205 - 14-week Q4, 53-week ISO year fallback, all-time leading ghost, year grain, null charts, single bucket
  ---
  duration_ms: 13.518959
  ...
# Subtest: not-counted parts omit badge waiting when the badge is on, and include it when off
ok 1206 - not-counted parts omit badge waiting when the badge is on, and include it when off
  ---
  duration_ms: 1.242863
  ...
# Subtest: digest changes when the view, collapse, or stale flag changes
ok 1207 - digest changes when the view, collapse, or stale flag changes
  ---
  duration_ms: 1.369625
  ...
# Subtest: decoded -c JSON round-trips through the panel model
ok 1208 - decoded -c JSON round-trips through the panel model
  ---
  duration_ms: 3.113875
  ...
# Subtest: textContent reads naturally with real separators, not CSS content
ok 1209 - textContent reads naturally with real separators, not CSS content
  ---
  duration_ms: 8.29203
  ...
# Subtest: child order and roles carry no button element
ok 1210 - child order and roles carry no button element
  ---
  duration_ms: 2.536703
  ...
# Subtest: aria labels name the period, money, top category, and coverage
ok 1211 - aria labels name the period, money, top category, and coverage
  ---
  duration_ms: 1.772544
  ...
# Subtest: the cashflow axis keeps one roving tab stop across arrows, Home, and End
ok 1212 - the cashflow axis keeps one roving tab stop across arrows, Home, and End
  ---
  duration_ms: 6.637552
  ...
# Subtest: hover and focus dim siblings and fill the readout; Escape clears it
ok 1213 - hover and focus dim siblings and fill the readout; Escape clears it
  ---
  duration_ms: 1.834733
  ...
# Subtest: Enter, Space, click, Ctrl-click, and middle-click activate with newLeaf
ok 1214 - Enter, Space, click, Ctrl-click, and middle-click activate with newLeaf
  ---
  duration_ms: 1.572842
  ...
# Subtest: the view switch cycles and the disclosure collapses
ok 1215 - the view switch cycles and the disclosure collapses
  ---
  duration_ms: 5.775617
  ...
# Subtest: table twins carry cashflow and category rows with exact copy
ok 1216 - table twins carry cashflow and category rows with exact copy
  ---
  duration_ms: 1.921217
  ...
# Subtest: stale paints last-good values with a dashed edge and a hint
ok 1217 - stale paints last-good values with a dashed edge and a hint
  ---
  duration_ms: 59.822873
  ...
# Subtest: unavailable paints one muted line with a hint title
ok 1218 - unavailable paints one muted line with a hint title
  ---
  duration_ms: 0.878597
  ...
# Subtest: hidden states empty the host
ok 1219 - hidden states empty the host
  ---
  duration_ms: 0.378623
  ...
# Subtest: waiting paints one quiet line that opens the waiting target
ok 1220 - waiting paints one quiet line that opens the waiting target
  ---
  duration_ms: 0.418379
  ...
# Subtest: a category label containing markup renders literally
ok 1221 - a category label containing markup renders literally
  ---
  duration_ms: 1.37234
  ...
# Subtest: collapsed shows only the header row
ok 1222 - collapsed shows only the header row
  ---
  duration_ms: 1.049313
  ...
# Subtest: a single available chart shows alone and hides the switch
ok 1223 - a single available chart shows alone and hides the switch
  ---
  duration_ms: 1.300854
  ...
# Subtest: ghost columns are inert while real columns stay activatable
ok 1224 - ghost columns are inert while real columns stay activatable
  ---
  duration_ms: 0.572844
  ...
# Subtest: contrast tokens ship calibrated fills and keep state words meaningful
ok 1225 - contrast tokens ship calibrated fills and keep state words meaningful
  ---
  duration_ms: 18.270913
  ...
# Subtest: category, group, and rule multi-moves each compile one envelope without a confirm stage
ok 1226 - category, group, and rule multi-moves each compile one envelope without a confirm stage
  ---
  duration_ms: 86.833841
  ...
# Subtest: quiet category saves on one Enter; rule moves confirm; dry-run mismatch blocks; G→H badges paint
ok 1227 - quiet category saves on one Enter; rule moves confirm; dry-run mismatch blocks; G→H badges paint
  ---
  duration_ms: 64.947526
  ...
# Subtest: Ctrl+Z ladders, region identity, Alt chords by code, and ⌥M never hijacks hotkey letters
ok 1228 - Ctrl+Z ladders, region identity, Alt chords by code, and ⌥M never hijacks hotkey letters
  ---
  duration_ms: 164.541688
  ...
# Subtest: category moves clamp at the group edge and Money is not auto-reordered on open
ok 1229 - category moves clamp at the group edge and Money is not auto-reordered on open
  ---
  duration_ms: 2.138042
  ...
# Subtest: q and Ctrl+[ leave gap-hint mode without picking a gap
ok 1230 - q and Ctrl+[ leave gap-hint mode without picking a gap
  ---
  duration_ms: 18.037798
  ...
# Subtest: hint badge letters never claim Ctrl+[ and dirty moves revert through backOut
ok 1231 - hint badge letters never claim Ctrl+[ and dirty moves revert through backOut
  ---
  duration_ms: 14.362149
  ...
# Subtest: group jumps walk painted groups with parent-first K and HIDDEN last
ok 1232 - group jumps walk painted groups with parent-first K and HIDDEN last
  ---
  duration_ms: 105.355463
  ...
# Subtest: Shift+K never fires a hotkey while lowercase keys still select
ok 1233 - Shift+K never fires a hotkey while lowercase keys still select
  ---
  duration_ms: 18.824118
  ...
# Subtest: jumps stay inert on other tabs and behind every gate
ok 1234 - jumps stay inert on other tabs and behind every gate
  ---
  duration_ms: 11.593255
  ...
# Subtest: projected group order drives Shift+J and the arrows while dirty
ok 1235 - projected group order drives Shift+J and the arrows while dirty
  ---
  duration_ms: 45.77396
  ...
# Subtest: current-group label, footer hint, silence, and reduced-motion bumps
ok 1236 - current-group label, footer hint, silence, and reduced-motion bumps
  ---
  duration_ms: 33.228289
  ...
# Subtest: config decode keeps every report field and tolerates absent ones
ok 1237 - config decode keeps every report field and tolerates absent ones
  ---
  duration_ms: 3.6035
  ...
# Subtest: config decode reads invalid, missing, and teaching-empty states with located findings
ok 1238 - config decode reads invalid, missing, and teaching-empty states with located findings
  ---
  duration_ms: 0.616757
  ...
# Subtest: config decode maps an older bob to unsupported and rejects bad shapes
ok 1239 - config decode maps an older bob to unsupported and rejects bad shapes
  ---
  duration_ms: 0.630164
  ...
# Subtest: config fetch args use the bare config member
ok 1240 - config fetch args use the bare config member
  ---
  duration_ms: 0.658567
  ...
# Subtest: collapsed grammar covers one vs several accounts, hidden counts, and rule plurals
ok 1241 - collapsed grammar covers one vs several accounts, hidden counts, and rule plurals
  ---
  duration_ms: 2.410252
  ...
# Subtest: invalid configs auto-expand and label every finding with its line
ok 1242 - invalid configs auto-expand and label every finding with its line
  ---
  duration_ms: 14.620282
  ...
# Subtest: state selection covers mobile, unsupported, loading, refresh failures, and missing
ok 1243 - state selection covers mobile, unsupported, loading, refresh failures, and missing
  ---
  duration_ms: 1.357501
  ...
# Subtest: tiles enrich keycap style, tooltips, accessible names, and jump lines
ok 1244 - tiles enrich keycap style, tooltips, accessible names, and jump lines
  ---
  duration_ms: 0.591299
  ...
# Subtest: widget identity folds the signature with surface options
ok 1245 - widget identity folds the signature with surface options
  ---
  duration_ms: 0.768306
  ...
# Subtest: tiles follow Category card order and the signature moves with row counts
ok 1246 - tiles follow Category card order and the signature moves with row counts
  ---
  duration_ms: 1.092356
  ...
# Subtest: accounts carry status words and since labels; dead rules are flagged
ok 1247 - accounts carry status words and since labels; dead rules are flagged
  ---
  duration_ms: 0.531575
  ...
# Subtest: shared tile keeps the card look and keys the header apart
ok 1248 - shared tile keeps the card look and keys the header apart
  ---
  duration_ms: 1.965924
  ...
# Subtest: valid header paints collapsed and expanded states with jumps and accessible names
ok 1249 - valid header paints collapsed and expanded states with jumps and accessible names
  ---
  duration_ms: 3.65033
  ...
# Subtest: invalid header auto-expands with a live-region banner and a last-good note
ok 1250 - invalid header auto-expands with a live-region banner and a last-good note
  ---
  duration_ms: 1.181396
  ...
# Subtest: missing, unsupported, mobile, and failed states paint their lines
ok 1251 - missing, unsupported, mobile, and failed states paint their lines
  ---
  duration_ms: 0.943932
  ...
# Subtest: lint marks map through edits and drop from edited lines
ok 1252 - lint marks map through edits and drop from edited lines
  ---
  duration_ms: 0.68081
  ...
# Subtest: setup registers surfaces on desktop and skips the fetch on mobile
ok 1253 - setup registers surfaces on desktop and skips the fetch on mobile
  ---
  duration_ms: 104.649633
  ...
# Subtest: hub mounts once per surface, survives repaint, and leaves other notes alone
ok 1254 - hub mounts once per surface, survives repaint, and leaves other notes alone
  ---
  duration_ms: 5.540309
  ...
# Subtest: setup header starts expanded and collapses per hub in view state
ok 1255 - setup header starts expanded and collapses per hub in view state
  ---
  duration_ms: 4.499179
  ...
# Subtest: hiding never touches document.body and is owned only by bob-bank-setup-surface
ok 1256 - hiding never touches document.body and is owned only by bob-bank-setup-surface
  ---
  duration_ms: 1.109048
  ...
# Subtest: tile, account, and finding jumps open Source mode on the exact line
ok 1257 - tile, account, and finding jumps open Source mode on the exact line
  ---
  duration_ms: 0.625595
  ...
# Subtest: queue card points at Setup instead of the raw first message
ok 1258 - queue card points at Setup instead of the raw first message
  ---
  duration_ms: 0.653828
  ...
# Subtest: Setup card model preserves Category-card order and maps category gestures to guarded ops
ok 1259 - Setup card model preserves Category-card order and maps category gestures to guarded ops
  ---
  duration_ms: 1.708291
  ...
# Subtest: Setup card selects by key, protects focused typing, and stages shared New category input
ok 1260 - Setup card selects by key, protects focused typing, and stages shared New category input
  ---
  duration_ms: 8.243989
  ...
# Subtest: Setup checks YAML action preserves its located line through one delegated click
ok 1261 - Setup checks YAML action preserves its located line through one delegated click
  ---
  duration_ms: 1.224478
  ...
# Subtest: Setup card requires a current preview before Apply and exposes the shared Undo stage
ok 1262 - Setup card requires a current preview before Apply and exposes the shared Undo stage
  ---
  duration_ms: 4.698009
  ...
# Subtest: stale Setup preview refreshes data, keeps the draft, and waits for explicit re-preview
ok 1263 - stale Setup preview refreshes data, keeps the draft, and waits for explicit re-preview
  ---
  duration_ms: 2.587469
  ...
# Subtest: invalid config opens Checks read-only and the palette command is registered
ok 1264 - invalid config opens Checks read-only and the palette command is registered
  ---
  duration_ms: 0.99511
  ...
# Subtest: Setup card paints its loading shell before the first report arrives
ok 1265 - Setup card paints its loading shell before the first report arrives
  ---
  duration_ms: 1.111061
  ...
# Subtest: bank YAML Done stays on an invalid line and returns only after a valid fresh report
ok 1266 - bank YAML Done stays on an invalid line and returns only after a valid fresh report
  ---
  duration_ms: 1.201113
  ...
# Subtest: valid bank YAML Done restores the prior view and reopens the card selection
ok 1267 - valid bank YAML Done restores the prior view and reopens the card selection
  ---
  duration_ms: 0.668096
  ...
# Subtest: Setup header shows Edit on desktop valid/invalid states and degrades without it on mobile
ok 1268 - Setup header shows Edit on desktop valid/invalid states and degrades without it on mobile
  ---
  duration_ms: 0.90065
  ...
# Subtest: Setup card models accounts, rules, and findings alongside categories
ok 1269 - Setup card models accounts, rules, and findings alongside categories
  ---
  duration_ms: 0.619513
  ...
# Subtest: Setup card maps account, rule, and stale-after gestures to guarded ops
ok 1270 - Setup card maps account, rule, and stale-after gestures to guarded ops
  ---
  duration_ms: 1.306454
  ...
# Subtest: Setup card paints interactive account, rule, and finding rows
ok 1271 - Setup card paints interactive account, rule, and finding rows
  ---
  duration_ms: 2.879669
  ...
# Subtest: Setup card stages account and rule gestures through bob previews
ok 1272 - Setup card stages account and rule gestures through bob previews
  ---
  duration_ms: 43.254089
  ...
# Subtest: Setup card checks Enter jumps to the finding line
ok 1273 - Setup card checks Enter jumps to the finding line
  ---
  duration_ms: 1.510394
  ...
# Subtest: Setup card paints lock wait as pending and Esc stops without closing
ok 1274 - Setup card paints lock wait as pending and Esc stops without closing
  ---
  duration_ms: 1.566681
  ...
# Subtest: q, Ctrl+[, and onEscapeKey stop a lock wait without closing
ok 1275 - q, Ctrl+[, and onEscapeKey stop a lock wait without closing
  ---
  duration_ms: 4.252128
  ...
# Subtest: onEscapeKey cancels a stage without closing, then closes from browsing
ok 1276 - onEscapeKey cancels a stage without closing, then closes from browsing
  ---
  duration_ms: 2.277849
  ...
# Subtest: bank scope handler routes q/Ctrl+[ through backOut and leaves other keys alone
ok 1277 - bank scope handler routes q/Ctrl+[ through backOut and leaves other keys alone
  ---
  duration_ms: 1.198769
  ...
# Subtest: bank plain-browsing close hint reads esc/q
ok 1278 - bank plain-browsing close hint reads esc/q
  ---
  duration_ms: 1.957558
  ...
# Subtest: only the hub and canonical month paths are bank-relevant
ok 1279 - only the hub and canonical month paths are bank-relevant
  ---
  duration_ms: 14.305451
  ...
# Subtest: amount leads match the Rust grammar vectors
ok 1280 - amount leads match the Rust grammar vectors
  ---
  duration_ms: 1.05249
  ...
# Subtest: day headings parse canonical, month-day, and ISO spellings
ok 1281 - day headings parse canonical, month-day, and ISO spellings
  ---
  duration_ms: 0.611718
  ...
# Subtest: source scan keeps spans and ignores fences, stubs, children, and non-day sections
ok 1282 - source scan keeps spans and ignores fences, stubs, children, and non-day sections
  ---
  duration_ms: 2.260435
  ...
# Subtest: empty month notes have no rows and arbitrary dollar signs are not bank rows
ok 1283 - empty month notes have no rows and arbitrary dollar signs are not bank rows
  ---
  duration_ms: 0.304802
  ...
# Subtest: heading location requires a real day heading in the current source
ok 1284 - heading location requires a real day heading in the current source
  ---
  duration_ms: 0.583023
  ...
# Subtest: subscription picker filters titles and needles and ranks row matches first
ok 1285 - subscription picker filters titles and needles and ranks row matches first
  ---
  duration_ms: 2.815324
  ...
# Subtest: picker ranks the resolver's record before rule-renamed payee matches
ok 1286 - picker ranks the resolver's record before rule-renamed payee matches
  ---
  duration_ms: 0.319279
  ...
# Subtest: context strip compacts title, status, amount, and signed price drift
ok 1287 - context strip compacts title, status, amount, and signed price drift
  ---
  duration_ms: 0.379584
  ...
# Subtest: record selection inserts one link, fills a missing category, and closes in one edit
ok 1288 - record selection inserts one link, fills a missing category, and closes in one edit
  ---
  duration_ms: 4.627766
  ...
# Subtest: set mode can link without a category and replaces one prior subscription link
ok 1289 - set mode can link without a category and replaces one prior subscription link
  ---
  duration_ms: 1.71269
  ...
# Subtest: set-mode subscription pick fills a missing category in its atomic edit
ok 1290 - set-mode subscription pick fills a missing category in its atomic edit
  ---
  duration_ms: 1.030978
  ...
# Subtest: set-mode subscription pick keeps an existing category and adds the link
ok 1291 - set-mode subscription pick keeps an existing category and adds the link
  ---
  duration_ms: 0.595267
  ...
# Subtest: new subscription fields default from the candidate proposal and stay argv-safe
ok 1292 - new subscription fields default from the candidate proposal and stay argv-safe
  ---
  duration_ms: 0.762465
  ...
# Subtest: subscription JSON decoders accept reports and reject malformed record paths
ok 1293 - subscription JSON decoders accept reports and reject malformed record paths
  ---
  duration_ms: 1.02676
  ...
# Subtest: slash picker returns its selected record through the card writer options
ok 1294 - slash picker returns its selected record through the card writer options
  ---
  duration_ms: 3.710734
  ...
# Subtest: picker arrows move, Escape backs out, and the opening chord cannot double-commit
ok 1295 - picker arrows move, Escape backs out, and the opening chord cannot double-commit
  ---
  duration_ms: 12.113667
  ...
# Subtest: new subscription sheet creates a record then links that created path
ok 1296 - new subscription sheet creates a record then links that created path
  ---
  duration_ms: 1.009227
  ...
# Subtest: bank subscription fetch builds an argv command without changing other readers
ok 1297 - bank subscription fetch builds an argv command without changing other readers
  ---
  duration_ms: 0.206985
  ...
# Subtest: candidate ghost activation opens the row in set mode and starts the picker
ok 1298 - candidate ghost activation opens the row in set mode and starts the picker
  ---
  duration_ms: 10.611008
  ...
# Subtest: subscription argv includes -a for cancelled records on surfaces
ok 1299 - subscription argv includes -a for cancelled records on surfaces
  ---
  duration_ms: 1.859189
  ...
# Subtest: record header reads money, last/next, timeline, and finding sentence
ok 1300 - record header reads money, last/next, timeline, and finding sentence
  ---
  duration_ms: 1.14237
  ...
# Subtest: yearly record header shows its monthly equivalent
ok 1301 - yearly record header shows its monthly equivalent
  ---
  duration_ms: 0.424961
  ...
# Subtest: timeline paints amber on the price-changed bucket, else the latest charged
ok 1302 - timeline paints amber on the price-changed bucket, else the latest charged
  ---
  duration_ms: 0.302878
  ...
# Subtest: finding fallbacks stay generic and never invent amounts
ok 1303 - finding fallbacks stay generic and never invent amounts
  ---
  duration_ms: 0.188279
  ...
# Subtest: album card estimates commitments, counts statuses, and ranks live bars
ok 1304 - album card estimates commitments, counts statuses, and ranks live bars
  ---
  duration_ms: 1.77558
  ...
# Subtest: teaching empty points at bob albums create
ok 1305 - teaching empty points at bob albums create
  ---
  duration_ms: 0.163843
  ...
# Subtest: index pretty paints bank category labels, money cadence, and next chip
ok 1306 - index pretty paints bank category labels, money cadence, and next chip
  ---
  duration_ms: 0.725104
  ...
# Subtest: header and card paint fictional Tunely/Cloudbox chrome
ok 1307 - header and card paint fictional Tunely/Cloudbox chrome
  ---
  duration_ms: 1.72338
  ...
# Subtest: unknown bob-bank views stay quiet and subscriptions is a real view
ok 1308 - unknown bob-bank views stay quiet and subscriptions is a real view
  ---
  duration_ms: 0.712981
  ...
# Subtest: older bob rows decode without subscription fields and stay unchipped
ok 1309 - older bob rows decode without subscription fields and stay unchipped
  ---
  duration_ms: 4.289271
  ...
# Subtest: row decoder accepts subscription JSON and the subscription suggestion source
ok 1310 - row decoder accepts subscription JSON and the subscription suggestion source
  ---
  duration_ms: 2.22608
  ...
# Subtest: linked chip labels follow state, payee containment, and tooltip copy
ok 1311 - linked chip labels follow state, payee containment, and tooltip copy
  ---
  duration_ms: 2.0111
  ...
# Subtest: subscription tooltip uses the record latest date when available
ok 1312 - subscription tooltip uses the record latest date when available
  ---
  duration_ms: 0.444769
  ...
# Subtest: matched-unlinked rows are dashed ghosts; candidates stay tooltip-only
ok 1313 - matched-unlinked rows are dashed ghosts; candidates stay tooltip-only
  ---
  duration_ms: 0.684647
  ...
# Subtest: a 🔁 wikilink without JSON still paints a linked chip
ok 1314 - a 🔁 wikilink without JSON still paints a linked chip
  ---
  duration_ms: 0.409422
  ...
# Subtest: ghost write plan inserts the wikilink before the bank id as one edit
ok 1315 - ghost write plan inserts the wikilink before the bank id as one edit
  ---
  duration_ms: 2.834371
  ...
# Subtest: queue helper paints the same chip model as the month-note token
ok 1316 - queue helper paints the same chip model as the month-note token
  ---
  duration_ms: 0.409782
  ...
# Subtest: Reading wrap hides the native 🔁 link and restore removes appended ghosts
ok 1317 - Reading wrap hides the native 🔁 link and restore removes appended ghosts
  ---
  duration_ms: 3.966363
  ...
# Subtest: initial scan uses the bank folder and never walks every Markdown file
ok 1318 - initial scan uses the bank folder and never walks every Markdown file
  ---
  duration_ms: 20.492042
  ...
# Subtest: a missing bank folder becomes ready with no months and still skips the Markdown walk
ok 1319 - a missing bank folder becomes ready with no months and still skips the Markdown walk
  ---
  duration_ms: 0.504162
  ...
# Subtest: Markdown walk is the fallback only when the vault has no folder API
ok 1320 - Markdown walk is the fallback only when the vault has no folder API
  ---
  duration_ms: 0.529841
  ...
# Subtest: a two-month edit burst re-reads both months after one debounce
ok 1321 - a two-month edit burst re-reads both months after one debounce
  ---
  duration_ms: 3.584463
  ...
# Subtest: delete and rename-away drop the month; rename onto a month reads it
ok 1322 - delete and rename-away drop the month; rename onto a month reads it
  ---
  duration_ms: 4.865529
  ...
# Subtest: a closed-editor tick stays out of WAITING until a later disk read
ok 1323 - a closed-editor tick stays out of WAITING until a later disk read
  ---
  duration_ms: 1.696739
  ...
# Subtest: an older disk read never beats a newer overlay
ok 1324 - an older disk read never beats a newer overlay
  ---
  duration_ms: 0.850023
  ...
# Subtest: overlay snapshot signature uses per-path seq, not full overlay text
ok 1325 - overlay snapshot signature uses per-path seq, not full overlay text
  ---
  duration_ms: 1.339418
  ...
# Subtest: listeners registered before setupBankWalk survive it in onload order
ok 1326 - listeners registered before setupBankWalk survive it in onload order
  ---
  duration_ms: 0.969511
  ...
# Subtest: membership: only amount-led top-level checkboxes under a day count
ok 1327 - membership: only amount-led top-level checkboxes under a day count
  ---
  duration_ms: 18.853564
  ...
# Subtest: card waiting predicate cannot drift from walk predicate
ok 1328 - card waiting predicate cannot drift from walk predicate
  ---
  duration_ms: 7.540336
  ...
# Subtest: snapshot: waiting scope, order, keys, labels, counts
ok 1329 - snapshot: waiting scope, order, keys, labels, counts
  ---
  duration_ms: 10.081508
  ...
# Subtest: parity: index rows and waiting flags equal bob bank list -a
ok 1330 - parity: index rows and waiting flags equal bob bank list -a
  ---
  duration_ms: 2.874688
  ...
# Subtest: scope flips to all when nothing waits
ok 1331 - scope flips to all when nothing waits
  ---
  duration_ms: 5.961301
  ...
# Subtest: step wraps in both directions and both scopes
ok 1332 - step wraps in both directions and both scopes
  ---
  duration_ms: 11.357343
  ...
# Subtest: day jumps skip empty headings, merge duplicates, cross months, step from mid-day
ok 1333 - day jumps skip empty headings, merge duplicates, cross months, step from mid-day
  ---
  duration_ms: 1.563034
  ...
# Subtest: counts: N]b, N]B and counted wraps take one snapshot
ok 1334 - counts: N]b, N]B and counted wraps take one snapshot
  ---
  duration_ms: 6.152908
  ...
# Subtest: origins: cursor gap, daily, anchor, entry
ok 1335 - origins: cursor gap, daily, anchor, entry
  ---
  duration_ms: 9.118228
  ...
# Subtest: locate: member, gap, daily-outside, nulls
ok 1336 - locate: member, gap, daily-outside, nulls
  ---
  duration_ms: 3.526764
  ...
# Subtest: overlay tick leaves WAITING immediately and beats disk
ok 1337 - overlay tick leaves WAITING immediately and beats disk
  ---
  duration_ms: 7.471474
  ...
# Subtest: resolve: id, line text, same-day uniqueness, payee-start ch
ok 1338 - resolve: id, line text, same-day uniqueness, payee-start ch
  ---
  duration_ms: 14.771
  ...
# Subtest: api guards: frozen, never throws, busy and anchor
ok 1339 - api guards: frozen, never throws, busy and anchor
  ---
  duration_ms: 8.192022
  ...
# Subtest: mixin snapshot: indexing until ready, overlay signature memo, change registry
ok 1340 - mixin snapshot: indexing until ready, overlay signature memo, change registry
  ---
  duration_ms: 1.211633
  ...
# Subtest: scan memo reuses the same path content and rescans only a changed month
ok 1341 - scan memo reuses the same path content and rescans only a changed month
  ---
  duration_ms: 10.574127
  ...
# Subtest: cursor above November's first heading stays in November
ok 1342 - cursor above November's first heading stays in November
  ---
  duration_ms: 1.967616
  ...
# Subtest: anchor-gap day jumps leave a day that still has rows
ok 1343 - anchor-gap day jumps leave a day that still has rows
  ---
  duration_ms: 14.815215
  ...
# Subtest: counted daily jumps move days and rows from the day's first landing
ok 1344 - counted daily jumps move days and rows from the day's first landing
  ---
  duration_ms: 1.85882
  ...
# Subtest: bankWalkStepFromTuple is the shared cursor-gap and anchor-gap stepper
ok 1345 - bankWalkStepFromTuple is the shared cursor-gap and anchor-gap stepper
  ---
  duration_ms: 1.776572
  ...
# Subtest: render appends one listener-free miniature with row-identical attributes
ok 1346 - render appends one listener-free miniature with row-identical attributes
  ---
  duration_ms: 2.47743
  ...
# Subtest: render decorative miniatures hide from assistive tech
ok 1347 - render decorative miniatures hide from assistive tech
  ---
  duration_ms: 0.286517
  ...
# Subtest: render accepts a synthetic digit model with no source task
ok 1348 - render accepts a synthetic digit model with no source task
  ---
  duration_ms: 0.2097
  ...
# Subtest: render uses the host ownerDocument, never a foreign one
ok 1349 - render uses the host ownerDocument, never a foreign one
  ---
  duration_ms: 0.211895
  ...
# Subtest: render returns null for bad input, a disabled gate, or no DOM
ok 1350 - render returns null for bad input, a disabled gate, or no DOM
  ---
  duration_ms: 0.286287
  ...
# Subtest: api.blockMarks v1 keeps model and adds a gated render
ok 1351 - api.blockMarks v1 keeps model and adds a gated render
  ---
  duration_ms: 0.254176
  ...
# Subtest: paint covers miniature, Live Preview, and reading rows under one gate
ok 1352 - paint covers miniature, Live Preview, and reading rows under one gate
  ---
  duration_ms: 2.398769
  ...
# Subtest: chip-box fallback rules are body-gated and never !important
ok 1353 - chip-box fallback rules are body-gated and never !important
  ---
  duration_ms: 2.060133
  ...
# Subtest: every paint rule except the token block and motion query carries the gate
ok 1354 - every paint rule except the token block and motion query carries the gate
  ---
  duration_ms: 2.404681
  ...
# Subtest: paint keeps pip geometry, reduced motion, and the 120ms budget
ok 1355 - paint keeps pip geometry, reduced motion, and the 120ms budget
  ---
  duration_ms: 2.493981
  ...
# Subtest: shipped mixes match the calibrated contract ramp
ok 1356 - shipped mixes match the calibrated contract ramp
  ---
  duration_ms: 2.151347
  ...
# Subtest: waiting glyphs meet 4.5:1 on their washed rows, both themes
ok 1357 - waiting glyphs meet 4.5:1 on their washed rows, both themes
  ---
  duration_ms: 2.331491
  ...
# Subtest: white on the darkened held fill meets 4.5:1, both themes
ok 1358 - white on the darkened held fill meets 4.5:1, both themes
  ---
  duration_ms: 2.026388
  ...
# Subtest: row tint and rail percentages ship in the gated rules
ok 1359 - row tint and rail percentages ship in the gated rules
  ---
  duration_ms: 1.788294
  ...
# Subtest: helpers never throw on bad input
ok 1360 - helpers never throw on bad input
  ---
  duration_ms: 0.311124
  ...
# Subtest: the plane mask is one hollow stroked path matched to the chevron
ok 1361 - the plane mask is one hollow stroked path matched to the chevron
  ---
  duration_ms: 4.9284
  ...
# Subtest: awaiting paints the P1 waiting box, the plane, the row tint, and the pip
ok 1362 - awaiting paints the P1 waiting box, the plane, the row tint, and the pip
  ---
  duration_ms: 6.438112
  ...
# Subtest: the plane renders as a miniature for chips and the Task Card
ok 1363 - the plane renders as a miniature for chips and the Task Card
  ---
  duration_ms: 0.344668
  ...
# Subtest: Live Preview emits own-row line attributes once across visible ranges
ok 1364 - Live Preview emits own-row line attributes once across visible ranges
  ---
  duration_ms: 6.725922
  ...
# Subtest: neutral rows, inline code, and fenced content stay unmarked
ok 1365 - neutral rows, inline code, and fenced content stay unmarked
  ---
  duration_ms: 0.610796
  ...
# Subtest: current unsaved document text changes or removes the visible mark
ok 1366 - current unsaved document text changes or removes the visible mark
  ---
  duration_ms: 1.139335
  ...
# Subtest: rebuilds on document, viewport, live-preview, path, and refresh effect, never selection alone
ok 1367 - rebuilds on document, viewport, live-preview, path, and refresh effect, never selection alone
  ---
  duration_ms: 0.441643
  ...
# Subtest: hot model calls use the in-memory ladder and project lookup is memoized per path
ok 1368 - hot model calls use the in-memory ladder and project lookup is memoized per path
  ---
  duration_ms: 1.436032
  ...
# Subtest: capture-phase tooltip attaches to the existing checkbox and restores owned attributes
ok 1369 - capture-phase tooltip attaches to the existing checkbox and restores owned attributes
  ---
  duration_ms: 2.736394
  ...
# Subtest: runBlockMarksRefresh rebuilds dependency chip editors
ok 1370 - runBlockMarksRefresh rebuilds dependency chip editors
  ---
  duration_ms: 0.299041
  ...
# Subtest: toggle is reversible, refreshes views, rerenders Tasks, and shows exact Notices
ok 1371 - toggle is reversible, refreshes views, rerenders Tasks, and shows exact Notices
  ---
  duration_ms: 0.318889
  ...
# Subtest: ladder invalidation compares semantic content and resume registers each editor document
ok 1372 - ladder invalidation compares semantic content and resume registers each editor document
  ---
  duration_ms: 5.25896
  ...
# Subtest: setup owns the gate and plugin-registered unload cleanup
ok 1373 - setup owns the gate and plugin-registered unload cleanup
  ---
  duration_ms: 1.385986
  ...
# Subtest: requestMeasure write-pass attaches tooltips after rebuild
ok 1374 - requestMeasure write-pass attaches tooltips after rebuild
  ---
  duration_ms: 8.696031
  ...
# Subtest: unscanned collect does not restore mouseover tooltip bindings
ok 1375 - unscanned collect does not restore mouseover tooltip bindings
  ---
  duration_ms: 0.802422
  ...
# Subtest: prj rows fold the project tag; dep-over-prj keeps it; selection reveals
ok 1376 - prj rows fold the project tag; dep-over-prj keeps it; selection reveals
  ---
  duration_ms: 8.111376
  ...
# Subtest: awaiting rows fold the \#awaiting_reply tag; losing rows keep it (AW1/AW3/AW4/AW6)
ok 1377 - awaiting rows fold the \#awaiting_reply tag; losing rows keep it (AW1/AW3/AW4/AW6)
  ---
  duration_ms: 7.142779
  ...
# Subtest: registers the reading processor before field-transforming marks
ok 1378 - registers the reading processor before field-transforming marks
  ---
  duration_ms: 1.947398
  ...
# Subtest: maps every family and pip from exact section source
ok 1379 - maps every family and pip from exact section source
  ---
  duration_ms: 13.78578
  ...
# Subtest: section-only text uses data-line offsets; full-note text adds lineStart
ok 1380 - section-only text uses data-line offsets; full-note text adds lineStart
  ---
  duration_ms: 1.700176
  ...
# Subtest: quoted tasks and nested children classify independently
ok 1381 - quoted tasks and nested children classify independently
  ---
  duration_ms: 0.953831
  ...
# Subtest: cold cache stays unmarked until Tasks is ready, then sweep paints
ok 1382 - cold cache stays unmarked until Tasks is ready, then sweep paints
  ---
  duration_ms: 0.97951
  ...
# Subtest: removed fields and recycled rows invalidate the retained mapping
ok 1383 - removed fields and recycled rows invalidate the retained mapping
  ---
  duration_ms: 0.77549
  ...
# Subtest: mismatched status or origin stays unmarked
ok 1384 - mismatched status or origin stays unmarked
  ---
  duration_ms: 0.42407
  ...
# Subtest: own-text fallback accepts raw fields and rejects transformed pills
ok 1385 - own-text fallback accepts raw fields and rejects transformed pills
  ---
  duration_ms: 1.382218
  ...
# Subtest: fallback never manufactures stale from lost field information
ok 1386 - fallback never manufactures stale from lost field information
  ---
  duration_ms: 0.763848
  ...
# Subtest: Dataview delayed rows use proven origin and never the query note stem
ok 1387 - Dataview delayed rows use proven origin and never the query note stem
  ---
  duration_ms: 1.856405
  ...
# Subtest: query result indexes are not read as source lines
ok 1388 - query result indexes are not read as source lines
  ---
  duration_ms: 0.577652
  ...
# Subtest: Tasks query rows stay excluded
ok 1389 - Tasks query rows stay excluded
  ---
  duration_ms: 0.310422
  ...
# Subtest: source-note lis Tasks also classifies still take JS marks
ok 1390 - source-note lis Tasks also classifies still take JS marks
  ---
  duration_ms: 4.001459
  ...
# Subtest: tooltip attributes restore when the mark leaves or the toggle turns off
ok 1391 - tooltip attributes restore when the mark leaves or the toggle turns off
  ---
  duration_ms: 0.950776
  ...
# Subtest: toggle off and on reclassifies tracked hosts in place
ok 1392 - toggle off and on reclassifies tracked hosts in place
  ---
  duration_ms: 1.587461
  ...
# Subtest: detached hosts dispose observers and drop owned attributes
ok 1393 - detached hosts dispose observers and drop owned attributes
  ---
  duration_ms: 0.691901
  ...
# Subtest: retained canonical text survives later field-transforming processors
ok 1394 - retained canonical text survives later field-transforming processors
  ---
  duration_ms: 0.559238
  ...
# Subtest: landing: recycled fallback row must drop the old scheduled reason
ok 1395 - landing: recycled fallback row must drop the old scheduled reason
  ---
  duration_ms: 0.898545
  ...
# Subtest: landing: off-state sweep must preserve a later external tooltip
ok 1396 - landing: off-state sweep must preserve a later external tooltip
  ---
  duration_ms: 0.55513
  ...
# Subtest: landing: a Tasks row used as processor root must stay excluded
ok 1397 - landing: a Tasks row used as processor root must stay excluded
  ---
  duration_ms: 0.244798
  ...
# Subtest: landing: Dataview without proven origin must remain neutral
ok 1398 - landing: Dataview without proven origin must remain neutral
  ---
  duration_ms: 0.308008
  ...
# Subtest: Dataview transformed rows recover canonical text from the Tasks cache
ok 1399 - Dataview transformed rows recover canonical text from the Tasks cache
  ---
  duration_ms: 1.553546
  ...
# Subtest: Dataview file links prove origin without data-task-path
ok 1400 - Dataview file links prove origin without data-task-path
  ---
  duration_ms: 0.515194
  ...
# Subtest: code and pre processor roots stay excluded like Tasks roots
ok 1401 - code and pre processor roots stay excluded like Tasks roots
  ---
  duration_ms: 0.292118
  ...
# Subtest: source-note fallback still paints when section mapping is absent
ok 1402 - source-note fallback still paints when section mapping is absent
  ---
  duration_ms: 0.464647
  ...
# Subtest: query origin-loss and same-status origin-change invalidate retained marks
ok 1403 - query origin-loss and same-status origin-change invalidate retained marks
  ---
  duration_ms: 0.750303
  ...
# Subtest: repeated off sweeps, unload, and toggle after an external aria edit
ok 1404 - repeated off sweeps, unload, and toggle after an external aria edit
  ---
  duration_ms: 0.866264
  ...
# Subtest: replacement checkbox nodes do not inherit the previous node's attributes
ok 1405 - replacement checkbox nodes do not inherit the previous node's attributes
  ---
  duration_ms: 0.441212
  ...
# Subtest: neutral status transition releases owned tooltip attributes
ok 1406 - neutral status transition releases owned tooltip attributes
  ---
  duration_ms: 0.364155
  ...
# Subtest: BM7 folds the project tag; BM19 keeps it
ok 1407 - BM7 folds the project tag; BM19 keeps it
  ---
  duration_ms: 0.858459
  ...
# Subtest: source-note lis Tasks also classifies still fold BM7 and keep BM19
ok 1408 - source-note lis Tasks also classifies still fold BM7 and keep BM19
  ---
  duration_ms: 0.663196
  ...
# Subtest: AW1 folds the \#awaiting_reply pill; AW3, AW6, and prj rows keep it
ok 1409 - AW1 folds the \#awaiting_reply pill; AW3, AW6, and prj rows keep it
  ---
  duration_ms: 2.357861
  ...
# Subtest: BM1–BM27 model vectors pass verbatim except Tasks-only BM24
ok 1410 - BM1–BM27 model vectors pass verbatim except Tasks-only BM24
  ---
  duration_ms: 51.481968
  ...
# Subtest: BM tooltip wording and losing-reason order match the contract
ok 1411 - BM tooltip wording and losing-reason order match the contract
  ---
  duration_ms: 7.127127
  ...
# Subtest: pure helpers preserve canonical eligibility, ids, digits, and decisions
ok 1412 - pure helpers preserve canonical eligibility, ids, digits, and decisions
  ---
  duration_ms: 1.087195
  ...
# Subtest: memo-local open-ID index keeps duplicate task IDs and project reasons one hop
ok 1413 - memo-local open-ID index keeps duplicate task IDs and project reasons one hop
  ---
  duration_ms: 29.522975
  ...
# Subtest: api.blockMarks v1 model is synchronous, frozen, toggle-aware, and neutral while cold
ok 1414 - api.blockMarks v1 model is synchronous, frozen, toggle-aware, and neutral while cold
  ---
  duration_ms: 0.997264
  ...
# Subtest: model keys are stable for equal results and change with a changed mark
ok 1415 - model keys are stable for equal results and change with a changed mark
  ---
  duration_ms: 0.561963
  ...
# Subtest: fold helpers: digit keys, BM1/BM8/BM9 bars, BM7/BM19 pills
ok 1416 - fold helpers: digit keys, BM1/BM8/BM9 bars, BM7/BM19 pills
  ---
  duration_ms: 15.25721
  ...
# Subtest: BM24 Tasks CSS cascade: digit from future scheduled + medium, no project tag
ok 1417 - BM24 Tasks CSS cascade: digit from future scheduled + medium, no project tag
  ---
  duration_ms: 18.87784
  ...
# Subtest: AW1–AW6 awaiting-reply model vectors pass verbatim
ok 1418 - AW1–AW6 awaiting-reply model vectors pass verbatim
  ---
  duration_ms: 16.758736
  ...
# Subtest: awaiting owns its date: no date reason, no digit, no Also scheduled pip
ok 1419 - awaiting owns its date: no date reason, no digit, no Also scheduled pip
  ---
  duration_ms: 1.628489
  ...
# Subtest: AP1–AP4 Also-replied tooltip pip vectors pass verbatim
ok 1420 - AP1–AP4 Also-replied tooltip pip vectors pass verbatim
  ---
  duration_ms: 21.58014
  ...
# Subtest: awaiting tooltip omits <who> when unknown and never throws on odd who
ok 1421 - awaiting tooltip omits <who> when unknown and never throws on odd who
  ---
  duration_ms: 0.915057
  ...
# Subtest: awaiting tag source is exact, quote-aware, and folds with its space
ok 1422 - awaiting tag source is exact, quote-aware, and folds with its space
  ---
  duration_ms: 0.446031
  ...
# Subtest: plugin <who> lookup reads the first linked mail note through the metadata cache
ok 1423 - plugin <who> lookup reads the first linked mail note through the metadata cache
  ---
  duration_ms: 9.915131
  ...
# Subtest: AW7 Tasks CSS cascade: the plane beats the digit, prj beats the plane
ok 1424 - AW7 Tasks CSS cascade: the plane beats the digit, prj beats the plane
  ---
  duration_ms: 2.740352
  ...
# Subtest: BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
ok 1425 - BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
  ---
  duration_ms: 5.994947
  ...
# Subtest: reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
ok 1426 - reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
  ---
  duration_ms: 4.225416
  ...
# Subtest: stale, missing, canonical append, and frozen-owner models (BC8-BC10)
ok 1427 - stale, missing, canonical append, and frozen-owner models (BC8-BC10)
  ---
  duration_ms: 1.048832
  ...
# Subtest: Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
ok 1428 - Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
  ---
  duration_ms: 11.232715
  ...
# Subtest: Reading BLOCKS chips map when the post-processor root is the nested list
ok 1429 - Reading BLOCKS chips map when the post-processor root is the nested list
  ---
  duration_ms: 2.596828
  ...
# Subtest: budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
ok 1430 - budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
  ---
  duration_ms: 2.405393
  ...
# Subtest: chip builder includes the 🔑 badge and has no edit controls
ok 1431 - chip builder includes the 🔑 badge and has no edit controls
  ---
  duration_ms: 1.086825
  ...
# Subtest: BLOCKS chip box covers prj, p2, stale miniatures and a throwing render
ok 1432 - BLOCKS chip box covers prj, p2, stale miniatures and a throwing render
  ---
  duration_ms: 0.807863
  ...
# Subtest: RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
ok 1433 - RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
  ---
  duration_ms: 2.085441
  ...
# Subtest: RBC2 hover × on a live chip calls removeDependent; notice is nav's
ok 1434 - RBC2 hover × on a live chip calls removeDependent; notice is nav's
  ---
  duration_ms: 1.07379
  ...
# Subtest: RBC3 frozen, stale, and no api.blocks stay navigation-only
ok 1435 - RBC3 frozen, stale, and no api.blocks stay navigation-only
  ---
  duration_ms: 1.198838
  ...
# Subtest: RBC4 Reading view matches Live Preview ＋ / ×
ok 1436 - RBC4 Reading view matches Live Preview ＋ / ×
  ---
  duration_ms: 4.107844
  ...
# Subtest: setup subscribes to the command-mode run-finished workspace event
ok 1437 - setup subscribes to the command-mode run-finished workspace event
  ---
  duration_ms: 3.028221
  ...
# Subtest: each invalidates tag refreshes its ledger cache and unknown tags are ignored
ok 1438 - each invalidates tag refreshes its ledger cache and unknown tags are ignored
  ---
  duration_ms: 7.391531
  ...
# Subtest: duplicate tags refresh once and a failing hook never blocks the others
ok 1439 - duplicate tags refresh once and a failing hook never blocks the others
  ---
  duration_ms: 0.382099
  ...
# Subtest: payloads without invalidates and setups without a workspace never throw
ok 1440 - payloads without invalidates and setups without a workspace never throw
  ---
  duration_ms: 0.41354
  ...
# Subtest: collections namespace version is additive v1
ok 1441 - collections namespace version is additive v1
  ---
  duration_ms: 13.692321
  ...
# Subtest: collection chip classes stay collection-specific through paint and refresh
ok 1442 - collection chip classes stay collection-specific through paint and refresh
  ---
  duration_ms: 15.910084
  ...
# Subtest: projects: scalar resolved links count, lists never widen
ok 1443 - projects: scalar resolved links count, lists never widen
  ---
  duration_ms: 15.02658
  ...
# Subtest: projects: templates, status, and containsAny edges
ok 1444 - projects: templates, status, and containsAny edges
  ---
  duration_ms: 0.548186
  ...
# Subtest: references: exact prefix, md only, exact scalar status
ok 1445 - references: exact prefix, md only, exact scalar status
  ---
  duration_ms: 0.351822
  ...
# Subtest: base contracts: accept current files, reject drift, tolerate presentation
ok 1446 - base contracts: accept current files, reject drift, tolerate presentation
  ---
  duration_ms: 0.888787
  ...
# Subtest: entries: true zero vs unavailable with reason, failure isolation
ok 1447 - entries: true zero vs unavailable with reason, failure isolation
  ---
  duration_ms: 0.690147
  ...
# Subtest: snapshot counts both collections once, true zero stays clickable
ok 1448 - snapshot counts both collections once, true zero stays clickable
  ---
  duration_ms: 0.629111
  ...
# Subtest: snapshot never presents partial counts as final
ok 1449 - snapshot never presents partial counts as final
  ---
  duration_ms: 0.490466
  ...
# Subtest: changed definitions fail closed per collection, never stale
ok 1450 - changed definitions fail closed per collection, never stale
  ---
  duration_ms: 0.641755
  ...
# Subtest: renderChip links, labels, and cleans up per component
ok 1451 - renderChip links, labels, and cleans up per component
  ---
  duration_ms: 0.793024
  ...
# Subtest: PENDING section excludes TODAY while the whole lane keeps it
ok 1452 - PENDING section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 29.809823
  ...
# Subtest: NEXT section excludes TODAY while the whole lane keeps it
ok 1453 - NEXT section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 0.856234
  ...
# Subtest: NEXT uses symbol *, not name matching
ok 1454 - NEXT uses symbol *, not name matching
  ---
  duration_ms: 0.486188
  ...
# Subtest: READY badge and query agree on hide and path case variants
ok 1455 - READY badge and query agree on hide and path case variants
  ---
  duration_ms: 13.157359
  ...
# Subtest: blocked uses the full list even outside the visible subset
ok 1456 - blocked uses the full list even outside the visible subset
  ---
  duration_ms: 0.456632
  ...
# Subtest: duplicate block IDs, missing IDs, and reused objects stay per-row
ok 1457 - duplicate block IDs, missing IDs, and reused objects stay per-row
  ---
  duration_ms: 0.302187
  ...
# Subtest: READY gating keeps exempt rows and drops NEW/ROTTEN
ok 1458 - READY gating keeps exempt rows and drops NEW/ROTTEN
  ---
  duration_ms: 0.384895
  ...
# Subtest: throwing Today degrades to unavailable, never zero
ok 1459 - throwing Today degrades to unavailable, never zero
  ---
  duration_ms: 703.599157
  ...
# Subtest: dashboard badges color the displayed section count and label whole-lane pressure
ok 1460 - dashboard badges color the displayed section count and label whole-lane pressure
  ---
  duration_ms: 1.198197
  ...
# Subtest: dashboard section warning boundaries ignore TODAY-only whole-lane excess
ok 1461 - dashboard section warning boundaries ignore TODAY-only whole-lane excess
  ---
  duration_ms: 29.512884
  ...
# Subtest: dashboard lane badge keeps unavailable data neutral
ok 1462 - dashboard lane badge keeps unavailable data neutral
  ---
  duration_ms: 0.626106
  ...
# Subtest: dashboard lane paint and refresh keep color aligned with the visible section
ok 1463 - dashboard lane paint and refresh keep color aligned with the visible section
  ---
  duration_ms: 287.555274
  ...
# Subtest: dashboard lane widgets refresh together and prune on unload
ok 1464 - dashboard lane widgets refresh together and prune on unload
  ---
  duration_ms: 448.550594
  ...
# Subtest: daily paint matches dashboard section badges on screenshot fixtures
ok 1465 - daily paint matches dashboard section badges on screenshot fixtures
  ---
  duration_ms: 1172.232402
  ...
# Subtest: daily paint lane lint matches a red badge section count
ok 1466 - daily paint lane lint matches a red badge section count
  ---
  duration_ms: 904.786891
  ...
# Subtest: daily and dashboard membership agree for exclusions and custom IN_PROGRESS
ok 1467 - daily and dashboard membership agree for exclusions and custom IN_PROGRESS
  ---
  duration_ms: 662.522135
  ...
# Subtest: daily paint refreshes with dashboard when Today, lane, and cap change
ok 1468 - daily paint refreshes with dashboard when Today, lane, and cap change
  ---
  duration_ms: 822.807979
  ...
# Subtest: older daily notes follow today's dashboard lanes
ok 1469 - older daily notes follow today's dashboard lanes
  ---
  duration_ms: 568.936271
  ...
# Subtest: daily lane anchors keep shared navigation and reject stale paints
ok 1470 - daily lane anchors keep shared navigation and reject stale paints
  ---
  duration_ms: 426.141972
  ...
# Subtest: daily paint stays unavailable until Tasks and Today are ready
ok 1471 - daily paint stays unavailable until Tasks and Today are ready
  ---
  duration_ms: 523.639141
  ...
# Subtest: work tones: dashboard lane models carry section tones
ok 1472 - work tones: dashboard lane models carry section tones
  ---
  duration_ms: 0.385696
  ...
# Subtest: T1 scheduled full-mode row gets a Fri mark inside the span
ok 1473 - T1 scheduled full-mode row gets a Fri mark inside the span
  ---
  duration_ms: 4.189778
  ...
# Subtest: T2 done row maps to a completion Oct 5 mark
ok 1474 - T2 done row maps to a completion Oct 5 mark
  ---
  duration_ms: 0.786752
  ...
# Subtest: T3 short-mode created span is left untouched by JS
ok 1475 - T3 short-mode created span is left untouched by JS
  ---
  duration_ms: 0.362252
  ...
# Subtest: T4 pending row decorates once data-task appears; exhausted rows stay native
ok 1476 - T4 pending row decorates once data-task appears; exhausted rows stay native
  ---
  duration_ms: 1.410202
  ...
# Subtest: T5 a second pass adds nothing
ok 1477 - T5 a second pass adds nothing
  ---
  duration_ms: 0.338005
  ...
# Subtest: T6 task-due and task-start spans are untouched
ok 1478 - T6 task-due and task-start spans are untouched
  ---
  duration_ms: 0.269535
  ...
# Subtest: T7 an invalid date is untouched
ok 1479 - T7 an invalid date is untouched
  ---
  duration_ms: 0.313107
  ...
# Subtest: T8 nothing is scheduled with marks off or for connected non-Tasks elements
ok 1480 - T8 nothing is scheduled with marks off or for connected non-Tasks elements
  ---
  duration_ms: 0.286347
  ...
# Subtest: T9 a Tasks-host Fri mark relabels to tomorrow on rollover
ok 1481 - T9 a Tasks-host Fri mark relabels to tomorrow on rollover
  ---
  duration_ms: 1.039194
  ...
# Subtest: renderDateMarksIn schedules one shared frame for every row
ok 1482 - renderDateMarksIn schedules one shared frame for every row
  ---
  duration_ms: 2.55086
  ...
# Subtest: the Tasks pass never throws on hostile input
ok 1483 - the Tasks pass never throws on hostile input
  ---
  duration_ms: 0.441273
  ...
# Subtest: T10 real-DOM NodeList children decorate via direct and queued passes
ok 1484 - T10 real-DOM NodeList children decorate via direct and queued passes
  ---
  duration_ms: 2.829392
  ...
# Subtest: T11 toggling off before a queued frame runs writes nothing
ok 1485 - T11 toggling off before a queued frame runs writes nothing
  ---
  duration_ms: 0.738581
  ...
# Subtest: T12 a pending-row retry followed by disabling writes nothing
ok 1486 - T12 a pending-row retry followed by disabling writes nothing
  ---
  duration_ms: 0.402468
  ...
# Subtest: T13 unloading before a callback runs writes nothing
ok 1487 - T13 unloading before a callback runs writes nothing
  ---
  duration_ms: 4.764616
  ...
# Subtest: RT1 full-mode recurring result gets a daily mark and stays idempotent
ok 1488 - RT1 full-mode recurring result gets a daily mark and stays idempotent
  ---
  duration_ms: 1.51869
  ...
# Subtest: RT2 recurring labels use the shared cadence grammar
ok 1489 - RT2 recurring labels use the shared cadence grammar
  ---
  duration_ms: 1.546683
  ...
# Subtest: RT2a unknown inherited-name rules stay readable in Tasks results
ok 1490 - RT2a unknown inherited-name rules stay readable in Tasks results
  ---
  duration_ms: 0.625804
  ...
# Subtest: RT3 short-mode recurring spans stay native to JS and use the CSS loop
ok 1491 - RT3 short-mode recurring spans stay native to JS and use the CSS loop
  ---
  duration_ms: 1.938912
  ...
# Subtest: RT4 open checklist members keep recurrence pills without `when done`
ok 1492 - RT4 open checklist members keep recurrence pills without `when done`
  ---
  duration_ms: 0.884909
  ...
# Subtest: RT5 invalid recurrence stays native and incomplete rows are retried
ok 1493 - RT5 invalid recurrence stays native and incomplete rows are retried
  ---
  duration_ms: 0.562614
  ...
# Subtest: styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
ok 1494 - styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
  ---
  duration_ms: 2.191554
  ...
# Subtest: DATE_MARK_FIELDS lists the four dates with verbs
ok 1495 - DATE_MARK_FIELDS lists the four dates with verbs
  ---
  duration_ms: 6.574893
  ...
# Subtest: DM1 created today: label, tooltip, fold, quiet field
ok 1496 - DM1 created today: label, tooltip, fold, quiet field
  ---
  duration_ms: 1.971644
  ...
# Subtest: DM2 created yesterday without space after the colons
ok 1497 - DM2 created yesterday without space after the colons
  ---
  duration_ms: 0.57602
  ...
# Subtest: DM3-DM6 scheduled tomorrow, weekday, and month/day labels
ok 1498 - DM3-DM6 scheduled tomorrow, weekday, and month/day labels
  ---
  duration_ms: 0.360549
  ...
# Subtest: DM7 scheduled today reads with emphasis timing
ok 1499 - DM7 scheduled today reads with emphasis timing
  ---
  duration_ms: 0.315422
  ...
# Subtest: DM8 past scheduled uses month/day, never a weekday
ok 1500 - DM8 past scheduled uses month/day, never a weekday
  ---
  duration_ms: 0.230981
  ...
# Subtest: DM9 completion on a closed task keeps the timeline grammar
ok 1501 - DM9 completion on a closed task keeps the timeline grammar
  ---
  duration_ms: 0.240829
  ...
# Subtest: DM10 cancelled across years appends the year
ok 1502 - DM10 cancelled across years appends the year
  ---
  duration_ms: 0.155146
  ...
# Subtest: DM11 next-year date appends the year
ok 1503 - DM11 next-year date appends the year
  ---
  duration_ms: 0.357953
  ...
# Subtest: DM12 the weekday rule wins across the year boundary
ok 1504 - DM12 the weekday rule wins across the year boundary
  ---
  duration_ms: 0.44011
  ...
# Subtest: DM13 two marks in order with folds 1 and 2
ok 1505 - DM13 two marks in order with folds 1 and 2
  ---
  duration_ms: 0.503822
  ...
# Subtest: DM14 created and scheduled ranges stay disjoint from the fresh mark
ok 1506 - DM14 created and scheduled ranges stay disjoint from the fresh mark
  ---
  duration_ms: 0.331963
  ...
# Subtest: DM15-DM16 paren and padded brackets are canonical
ok 1507 - DM15-DM16 paren and padded brackets are canonical
  ---
  duration_ms: 0.184883
  ...
# Subtest: DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
ok 1508 - DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
  ---
  duration_ms: 0.371318
  ...
# Subtest: DM22 code still parses pure but decorates nothing (see Live Preview)
ok 1509 - DM22 code still parses pure but decorates nothing (see Live Preview)
  ---
  duration_ms: 0.11027
  ...
# Subtest: DM23 rescheduled is untouched and never a duplicate
ok 1510 - DM23 rescheduled is untouched and never a duplicate
  ---
  duration_ms: 0.149065
  ...
# Subtest: DN1-DN9 non-canonical fields get no mark
ok 1511 - DN1-DN9 non-canonical fields get no mark
  ---
  duration_ms: 0.254877
  ...
# Subtest: dateMarkContentStart finds content on list, quoted, and plain lines
ok 1512 - dateMarkContentStart finds content on list, quoted, and plain lines
  ---
  duration_ms: 0.11539
  ...
# Subtest: dateMarkRelativePhrase covers the exact-day phrases
ok 1513 - dateMarkRelativePhrase covers the exact-day phrases
  ---
  duration_ms: 0.088609
  ...
# Subtest: dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
ok 1514 - dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
  ---
  duration_ms: 0.22019
  ...
# Subtest: no model output contains a double colon
ok 1515 - no model output contains a double colon
  ---
  duration_ms: 1.727288
  ...
# Subtest: a new day always changes the widget key
ok 1516 - a new day always changes the widget key
  ---
  duration_ms: 0.17281
  ...
# Subtest: element structure and the decorative/inheritColor/rendered options
ok 1517 - element structure and the decorative/inheritColor/rendered options
  ---
  duration_ms: 0.503612
  ...
# Subtest: Live Preview emits several decorations in ascending order
ok 1518 - Live Preview emits several decorations in ascending order
  ---
  duration_ms: 1.370447
  ...
# Subtest: Live Preview reveals per field, never the whole line
ok 1519 - Live Preview reveals per field, never the whole line
  ---
  duration_ms: 0.322065
  ...
# Subtest: Live Preview refuses source mode, code, and disabled marks
ok 1520 - Live Preview refuses source mode, code, and disabled marks
  ---
  duration_ms: 0.52909
  ...
# Subtest: widget mousedown anchors at the field start for folds 0, 1, and 2
ok 1521 - widget mousedown anchors at the field start for folds 0, 1, and 2
  ---
  duration_ms: 1.625514
  ...
# Subtest: DM24 a cursor in the folded run unfolds the mark (vim cw)
ok 1522 - DM24 a cursor in the folded run unfolds the mark (vim cw)
  ---
  duration_ms: 0.342203
  ...
# Subtest: DM25 a cursor in Tasks double space unfolds only that field
ok 1523 - DM25 a cursor in Tasks double space unfolds only that field
  ---
  duration_ms: 0.259976
  ...
# Subtest: a selection ending inside the run unfolds; ending at its start keeps the fold
ok 1524 - a selection ending inside the run unfolds; ending at its start keeps the fold
  ---
  duration_ms: 0.281677
  ...
# Subtest: no emitted decoration ever hides a cursor, and reveal still means field overlap
ok 1525 - no emitted decoration ever hides a cursor, and reveal still means field overlap
  ---
  duration_ms: 36.987727
  ...
# Subtest: dateMarkSelectionFold: reveal, unfold, fold, and garbage input
ok 1526 - dateMarkSelectionFold: reveal, unfold, fold, and garbage input
  ---
  duration_ms: 0.334148
  ...
# Subtest: mousedown on an unfolded (fold-0) widget anchors at the field start
ok 1527 - mousedown on an unfolded (fold-0) widget anchors at the field start
  ---
  duration_ms: 0.60785
  ...
# Subtest: rendered views split several fields in one node
ok 1528 - rendered views split several fields in one node
  ---
  duration_ms: 2.100119
  ...
# Subtest: rendered views skip exclusions and duplicates
ok 1529 - rendered views skip exclusions and duplicates
  ---
  duration_ms: 1.008506
  ...
# Subtest: RO1 rendered marks relabel in place across midnight
ok 1530 - RO1 rendered marks relabel in place across midnight
  ---
  duration_ms: 0.735073
  ...
# Subtest: rollover dispatches once per day change and never touches widgets
ok 1531 - rollover dispatches once per day change and never touches widgets
  ---
  duration_ms: 1.818793
  ...
# Subtest: api.dateMarks v1 is additive, sync, and never throwing
ok 1532 - api.dateMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.740003
  ...
# Subtest: session toggle and onload wiring
ok 1533 - session toggle and onload wiring
  ---
  duration_ms: 114.443223
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 1534 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 0.986965
  ...
# Subtest: styles.css contract: masks, tones, repair flag, resting
ok 1535 - styles.css contract: masks, tones, repair flag, resting
  ---
  duration_ms: 15.664868
  ...
# Subtest: day identity follows the canonical path, never the tab or mtime
ok 1536 - day identity follows the canonical path, never the tab or mtime
  ---
  duration_ms: 16.039541
  ...
# Subtest: fence day parsing accepts YAML mappings and plain lines, nothing else
ok 1537 - fence day parsing accepts YAML mappings and plain lines, nothing else
  ---
  duration_ms: 5.733797
  ...
# Subtest: report selection reads the default entry, an 8-day range, or nothing
ok 1538 - report selection reads the default entry, an 8-day range, or nothing
  ---
  duration_ms: 287.875657
  ...
# Subtest: report window checks keep the page window only when it shows D
ok 1539 - report window checks keep the page window only when it shows D
  ---
  duration_ms: 279.374898
  ...
# Subtest: week-grouped default never covers D, and a cold-cache today re-selects once
ok 1540 - week-grouped default never covers D, and a cold-cache today re-selects once
  ---
  duration_ms: 580.575091
  ...
# Subtest: a report that differs only in typical repaints
ok 1541 - a report that differs only in typical repaints
  ---
  duration_ms: 211.055143
  ...
# Subtest: paint from cache costs one frame and zero spawns
ok 1542 - paint from cache costs one frame and zero spawns
  ---
  duration_ms: 462.040157
  ...
# Subtest: off-screen and hidden-tab strips spawn nothing
ok 1543 - off-screen and hidden-tab strips spawn nothing
  ---
  duration_ms: 821.942396
  ...
# Subtest: clean fresh entries never refetch, whatever changes
ok 1544 - clean fresh entries never refetch, whatever changes
  ---
  duration_ms: 718.318499
  ...
# Subtest: visible changing strips spawn at most once per 30 s
ok 1545 - visible changing strips spawn at most once per 30 s
  ---
  duration_ms: 1089.311481
  ...
# Subtest: the 10-minute age rule refetches today without any change
ok 1546 - the 10-minute age rule refetches today without any change
  ---
  duration_ms: 658.137303
  ...
# Subtest: past days wait out the 10-minute gate
ok 1547 - past days wait out the 10-minute gate
  ---
  duration_ms: 741.602323
  ...
# Subtest: several strips and the page share one spawn per key
ok 1548 - several strips and the page share one spawn per key
  ---
  duration_ms: 855.726205
  ...
# Subtest: strips repaint for free when the page refreshes the shared key
ok 1549 - strips repaint for free when the page refreshes the shared key
  ---
  duration_ms: 497.937012
  ...
# Subtest: rollover re-keys today to a past day and refetches
ok 1550 - rollover re-keys today to a past day and refetches
  ---
  duration_ms: 987.516326
  ...
# Subtest: a stale-across-midnight report is never shown as so far
ok 1551 - a stale-across-midnight report is never shown as so far
  ---
  duration_ms: 676.283818
  ...
# Subtest: window-edge days fetch the 8-day range
ok 1552 - window-edge days fetch the 8-day range
  ---
  duration_ms: 758.526533
  ...
# Subtest: future days render nothing and spawn nothing
ok 1553 - future days render nothing and spawn nothing
  ---
  duration_ms: 563.972727
  ...
# Subtest: a failed refresh keeps the frame and shows the stale dot
ok 1554 - a failed refresh keeps the frame and shows the stale dot
  ---
  duration_ms: 391.551792
  ...
# Subtest: a failure with nothing cached shows the one-line error and Retry
ok 1555 - a failure with nothing cached shows the one-line error and Retry
  ---
  duration_ms: 402.406849
  ...
# Subtest: bob-not-found with nothing cached names stats.bob_path
ok 1556 - bob-not-found with nothing cached names stats.bob_path
  ---
  duration_ms: 406.332159
  ...
# Subtest: the fence parses day:, falls back to the note date, or explains itself
ok 1557 - the fence parses day:, falls back to the note date, or explains itself
  ---
  duration_ms: 803.002027
  ...
# Subtest: the fence skips hover popovers and embeds, and unregisters on unload
ok 1558 - the fence skips hover popovers and embeds, and unregisters on unload
  ---
  duration_ms: 852.224723
  ...
# Subtest: openStatsForDay pins the day, focuses the metric, and opens a new tab
ok 1559 - openStatsForDay pins the day, focuses the metric, and opens a new tab
  ---
  duration_ms: 332.863495
  ...
# Subtest: openStatsForDay opens a new tab when Stats is already open
ok 1560 - openStatsForDay opens a new tab when Stats is already open
  ---
  duration_ms: 622.534923
  ...
# Subtest: openStatsForDay keeps the page window when it already shows D
ok 1561 - openStatsForDay keeps the page window when it already shows D
  ---
  duration_ms: 874.307021
  ...
# Subtest: openStatsForDay panel themes selects the Themes view
ok 1562 - openStatsForDay panel themes selects the Themes view
  ---
  duration_ms: 395.022538
  ...
# Subtest: openStatsForDay Notices when Stats cannot open
ok 1563 - openStatsForDay Notices when Stats cannot open
  ---
  duration_ms: 170.529184
  ...
# Subtest: the page honours a pinned day on its first paint
ok 1564 - the page honours a pinned day on its first paint
  ---
  duration_ms: 222.716155
  ...
# Subtest: renderStatsResult consumes the one-shot revealPanel
ok 1565 - renderStatsResult consumes the one-shot revealPanel
  ---
  duration_ms: 289.61102
  ...
# Subtest: every strip paints facts and links with no buttons and no vault writes
ok 1566 - every strip paints facts and links with no buttons and no vault writes
  ---
  duration_ms: 268.910787
  ...
# Subtest: change bursts coalesce behind one trailing quiet window
ok 1567 - change bursts coalesce behind one trailing quiet window
  ---
  duration_ms: 283.995048
  ...
# Subtest: mobile and spawn-less hosts render nothing and spawn nothing
ok 1568 - mobile and spawn-less hosts render nothing and spawn nothing
  ---
  duration_ms: 155.709116
  ...
# Subtest: rollover synchronously skeletons visible and offscreen fences; visible refetch resolves as past
ok 1569 - rollover synchronously skeletons visible and offscreen fences; visible refetch resolves as past
  ---
  duration_ms: 370.768254
  ...
# Subtest: fit observer registers once, refits on width change, and releases
ok 1570 - fit observer registers once, refits on width change, and releases
  ---
  duration_ms: 3.567112
  ...
# Subtest: missing ResizeObserver is harmless
ok 1571 - missing ResizeObserver is harmless
  ---
  duration_ms: 0.332284
  ...
# Subtest: openStatsForDay explicit clock selects the lens, pins the day, and persists the preference
ok 1572 - openStatsForDay explicit clock selects the lens, pins the day, and persists the preference
  ---
  duration_ms: 64.308514
  ...
# Subtest: openStatsForDay explicit worked survives a remembered off-clock preference
ok 1573 - openStatsForDay explicit worked survives a remembered off-clock preference
  ---
  duration_ms: 112.987786
  ...
# Subtest: muted roots stay gray, unshaded, claim no hue, and sort before the buckets
ok 1574 - muted roots stay gray, unshaded, claim no hue, and sort before the buckets
  ---
  duration_ms: 131.318932
  ...
# Subtest: root hues follow identity order when minutes change
ok 1575 - root hues follow identity order when minutes change
  ---
  duration_ms: 0.561732
  ...
# Subtest: lane view sanitizes and cycles both -> roots -> themes -> both
ok 1576 - lane view sanitizes and cycles both -> roots -> themes -> both
  ---
  duration_ms: 0.186576
  ...
# Subtest: layout matrix: availability, skeleton, and hidden states
ok 1577 - layout matrix: availability, skeleton, and hidden states
  ---
  duration_ms: 13.628098
  ...
# Subtest: layout copy uses areas under the area fallback with exact strings
ok 1578 - layout copy uses areas under the area fallback with exact strings
  ---
  duration_ms: 0.365739
  ...
# Subtest: painter per view: order, first-row meta and switch, themes-first
ok 1579 - painter per view: order, first-row meta and switch, themes-first
  ---
  duration_ms: 31.528614
  ...
# Subtest: switch attributes, marks, and skeleton placeholder
ok 1580 - switch attributes, marks, and skeleton placeholder
  ---
  duration_ms: 17.936214
  ...
# Subtest: switch activation: click, Enter, Space call cycleLanes once with focus
ok 1581 - switch activation: click, Enter, Space call cycleLanes once with focus
  ---
  duration_ms: 14.9022
  ...
# Subtest: group aria-label names only the shown lanes
ok 1582 - group aria-label names only the shown lanes
  ---
  duration_ms: 1.40381
  ...
# Subtest: lane-enter class appears only on a same-day view change
ok 1583 - lane-enter class appears only on a same-day view change
  ---
  duration_ms: 46.270929
  ...
# Subtest: registry: a switch repaints every record without a spawn, dedupes, and restores focus
ok 1584 - registry: a switch repaints every record without a spawn, dedupes, and restores focus
  ---
  duration_ms: 331.873827
  ...
# Subtest: command Cycle Day stats bars is registered with its Notice copy
ok 1585 - command Cycle Day stats bars is registered with its Notice copy
  ---
  duration_ms: 280.992917
  ...
# Subtest: persistence remember = device: setup loads, saves, and tolerates missing storage
ok 1586 - persistence remember = device: setup loads, saves, and tolerates missing storage
  ---
  duration_ms: 1558.273073
  ...
# Subtest: require time adds no eager StateEffect.define()
ok 1587 - require time adds no eager StateEffect.define()
  ---
  duration_ms: 1.66017
  ...
# Subtest: renderPlanBlock puts exactly one host first with .bob-plan after it on canonical days
ok 1588 - renderPlanBlock puts exactly one host first with .bob-plan after it on canonical days
  ---
  duration_ms: 339.63806
  ...
# Subtest: non-daily, future, dashboard, mobile, spawn-less, and excluded blocks get no host
ok 1589 - non-daily, future, dashboard, mobile, spawn-less, and excluded blocks get no host
  ---
  duration_ms: 334.626592
  ...
# Subtest: paintPlanBlock keeps the same host node first with .bob-plan after it and no strip repaint or spawn
ok 1590 - paintPlanBlock keeps the same host node first with .bob-plan after it and no strip repaint or spawn
  ---
  duration_ms: 380.111331
  ...
# Subtest: toggle and stats.day_strip remove the host and class, re-enabling restores them
ok 1591 - toggle and stats.day_strip remove the host and class, re-enabling restores them
  ---
  duration_ms: 632.296387
  ...
# Subtest: unload releases the record and its observer
ok 1592 - unload releases the record and its observer
  ---
  duration_ms: 303.597433
  ...
# Subtest: rollover attaches future blocks and repaints today as a past day
ok 1593 - rollover attaches future blocks and repaints today as a past day
  ---
  duration_ms: 613.959318
  ...
# Subtest: rollover skeletons a visible automatic today host synchronously; it resolves as past
ok 1594 - rollover skeletons a visible automatic today host synchronously; it resolves as past
  ---
  duration_ms: 985.726399
  ...
# Subtest: plan hosts never write the vault or journals
ok 1595 - plan hosts never write the vault or journals
  ---
  duration_ms: 544.239643
  ...
# Subtest: cold plan host waits for visibility: no spawn before callback, false stays zero, true fetches once
ok 1596 - cold plan host waits for visibility: no spawn before callback, false stays zero, true fetches once
  ---
  duration_ms: 826.28737
  ...
# Subtest: plan host paints synchronously from cache with zero spawn before visibility
ok 1597 - plan host paints synchronously from cache with zero spawn before visibility
  ---
  duration_ms: 427.885058
  ...
# Subtest: detached excluded blocks get no host; detached ordinary blocks attach synchronously
ok 1598 - detached excluded blocks get no host; detached ordinary blocks attach synchronously
  ---
  duration_ms: 1628.76663
  ...
# Subtest: no-observer fallback attaches detached, fetches on check after connect, releases excluded
ok 1599 - no-observer fallback attaches detached, fetches on check after connect, releases excluded
  ---
  duration_ms: 1153.63053
  ...
# Subtest: excluded after attach releases on the first observer callback
ok 1600 - excluded after attach releases on the first observer callback
  ---
  duration_ms: 867.519449
  ...
# Subtest: excluded processor container gets no host
ok 1601 - excluded processor container gets no host
  ---
  duration_ms: 475.138968
  ...
# Subtest: reading-view order attaches detached, virtualized stays quiet until attach
ok 1602 - reading-view order attaches detached, virtualized stays quiet until attach
  ---
  duration_ms: 950.782957
  ...
# Subtest: today host shows so far HH:MM from the fetch stamp
ok 1603 - today host shows so far HH:MM from the fetch stamp
  ---
  duration_ms: 389.817951
  ...
# Subtest: failed refresh over a cached report names the HH:MM it shows
ok 1604 - failed refresh over a cached report names the HH:MM it shows
  ---
  duration_ms: 720.869801
  ...
# Subtest: placeholder finds .bob-plan by class and toggle-off restores it first
ok 1605 - placeholder finds .bob-plan by class and toggle-off restores it first
  ---
  duration_ms: 705.709305
  ...
# Subtest: statsThemeRef prefers theme_hues names and hues, with gray fallbacks
ok 1606 - statsThemeRef prefers theme_hues names and hues, with gray fallbacks
  ---
  duration_ms: 7.400509
  ...
# Subtest: theme mix orders coloured by minutes then gray, with unnamed last
ok 1607 - theme mix orders coloured by minutes then gray, with unnamed last
  ---
  duration_ms: 62.831017
  ...
# Subtest: same-hue coloured themes take shade 0 then 1 then 2; gray is never shaded
ok 1608 - same-hue coloured themes take shade 0 then 1 then 2; gray is never shaded
  ---
  duration_ms: 1.300292
  ...
# Subtest: same-hue type shades follow label identity while segment position follows minutes
ok 1609 - same-hue type shades follow label identity while segment position follows minutes
  ---
  duration_ms: 11.914286
  ...
# Subtest: theme mix labels, ranks, overflow, titles, and aria follow the report
ok 1610 - theme mix labels, ranks, overflow, titles, and aria follow the report
  ---
  duration_ms: 12.784939
  ...
# Subtest: theme lane is omitted for zero days, missing parts, and redefined worked
ok 1611 - theme lane is omitted for zero days, missing parts, and redefined worked
  ---
  duration_ms: 8.234522
  ...
# Subtest: fallback hue uses context.themeHueFor and stays gray without it
ok 1612 - fallback hue uses context.themeHueFor and stays gray without it
  ---
  duration_ms: 0.516556
  ...
# Subtest: painter uses swatches, shades, data-lane, and no buttons on the theme lane
ok 1613 - painter uses swatches, shades, data-lane, and no buttons on the theme lane
  ---
  duration_ms: 3.124846
  ...
# Subtest: theme legend and bar open Stats on the Themes view
ok 1614 - theme legend and bar open Stats on the Themes view
  ---
  duration_ms: 3.315951
  ...
# Subtest: fitter fits both legends independently and returns the roots result
ok 1615 - fitter fits both legends independently and returns the roots result
  ---
  duration_ms: 3.782511
  ...
# Subtest: date words and day shifts use calendar integers, including leap day
ok 1616 - date words and day shifts use calendar integers, including leap day
  ---
  duration_ms: 6.183526
  ...
# Subtest: fact displays are selected from the exact day point, even with null headline and grouped input
ok 1617 - fact displays are selected from the exact day point, even with null headline and grouped input
  ---
  duration_ms: 46.128006
  ...
# Subtest: honest states carry meta text for today, past, stale today, and stale past
ok 1618 - honest states carry meta text for today, past, stale today, and stale past
  ---
  duration_ms: 3.213074
  ...
# Subtest: time mix reuses Stats area ordering and hues, with buckets last and a tooltip title
ok 1619 - time mix reuses Stats area ordering and hues, with buckets last and a tooltip title
  ---
  duration_ms: 11.5445
  ...
# Subtest: root_parent is preferred with an honest area fallback
ok 1620 - root_parent is preferred with an honest area fallback
  ---
  duration_ms: 0.977255
  ...
# Subtest: zero worked renders no Pomodoros and redefined worked omits its mix
ok 1621 - zero worked renders no Pomodoros and redefined worked omits its mix
  ---
  duration_ms: 2.114587
  ...
# Subtest: aria label carries the date, values, provisional state, and area names
ok 1622 - aria label carries the date, values, provisional state, and area names
  ---
  duration_ms: 0.581861
  ...
# Subtest: skeleton carries placeholder text per fact and the same tag and class sequence
ok 1623 - skeleton carries placeholder text per fact and the same tag and class sequence
  ---
  duration_ms: 4.70853
  ...
# Subtest: painter repaints in place, emits no buttons, and shows unavailable controls
ok 1624 - painter repaints in place, emits no buttons, and shows unavailable controls
  ---
  duration_ms: 6.729028
  ...
# Subtest: facts, mix, and Retry preserve day, focus, and new-leaf modifiers
ok 1625 - facts, mix, and Retry preserve day, focus, and new-leaf modifiers
  ---
  duration_ms: 3.056134
  ...
# Subtest: future and hidden models paint no children
ok 1626 - future and hidden models paint no children
  ---
  duration_ms: 0.349757
  ...
# Subtest: strip paints facts, legend row, then full-width bar with no buttons
ok 1627 - strip paints facts, legend row, then full-width bar with no buttons
  ---
  duration_ms: 3.543205
  ...
# Subtest: bar click opens Stats homes with day and new-leaf modifiers
ok 1628 - bar click opens Stats homes with day and new-leaf modifiers
  ---
  duration_ms: 9.435173
  ...
# Subtest: same-area roots get distinct hues and legend dots match their segments
ok 1629 - same-area roots get distinct hues and legend dots match their segments
  ---
  duration_ms: 2.703701
  ...
# Subtest: dayStripValueRuns splits numerals from units and keeps words whole
ok 1630 - dayStripValueRuns splits numerals from units and keeps words whole
  ---
  duration_ms: 0.598733
  ...
# Subtest: facts stack a label head over a faithful value with warnings in the head
ok 1631 - facts stack a label head over a faithful value with warnings in the head
  ---
  duration_ms: 215.907647
  ...
# Subtest: root-parent labels use Bob's full home label
ok 1632 - root-parent labels use Bob's full home label
  ---
  duration_ms: 9.93137
  ...
# Subtest: unfiled root paints its label in gray after real roots
ok 1633 - unfiled root paints its label in gray after real roots
  ---
  duration_ms: 1.615204
  ...
# Subtest: area roots paint the bare label with a project_label tooltip
ok 1634 - area roots paint the bare label with a project_label tooltip
  ---
  duration_ms: 24.021142
  ...
# Subtest: case-insensitive legend labels keep their full root names
ok 1635 - case-insensitive legend labels keep their full root names
  ---
  duration_ms: 4.218614
  ...
# Subtest: dayStripLegendFit fits every root, reserves the counter, and handles empty
ok 1636 - dayStripLegendFit fits every root, reserves the counter, and handles empty
  ---
  duration_ms: 0.469547
  ...
# Subtest: names mode wins only when it names strictly more roots
ok 1637 - names mode wins only when it names strictly more roots
  ---
  duration_ms: 13.140166
  ...
# Subtest: DOM glue hides overflow, writes the counter, and toggles names mode
ok 1638 - DOM glue hides overflow, writes the counter, and toggles names mode
  ---
  duration_ms: 2.777883
  ...
# Subtest: dayStripMarkState maps bool points from the bob point, never the word
ok 1639 - dayStripMarkState maps bool points from the bob point, never the word
  ---
  duration_ms: 17.11132
  ...
# Subtest: boolean facts paint an aria-hidden mark with hidden display text
ok 1640 - boolean facts paint an aria-hidden mark with hidden display text
  ---
  duration_ms: 7.780944
  ...
# Subtest: docs without createElementNS keep word runs
ok 1641 - docs without createElementNS keep word runs
  ---
  duration_ms: 1.641744
  ...
# Subtest: bool skeleton paints a round placeholder and no svg
ok 1642 - bool skeleton paints a round placeholder and no svg
  ---
  duration_ms: 6.892148
  ...
# Subtest: pending mark tooltip drops so far; numeric provisional keeps it
ok 1643 - pending mark tooltip drops so far; numeric provisional keeps it
  ---
  duration_ms: 0.600546
  ...
# Subtest: pending to met on the same host and day draws the check once
ok 1644 - pending to met on the same host and day draws the check once
  ---
  duration_ms: 27.995078
  ...
# Subtest: arrive class stays off for other mark transitions
ok 1645 - arrive class stays off for other mark transitions
  ---
  duration_ms: 32.354851
  ...
# Subtest: stroke-dashoffset lives only inside keyframes
ok 1646 - stroke-dashoffset lives only inside keyframes
  ---
  duration_ms: 12.119868
  ...
# Subtest: dayStripRef classifies bob's typical without computing it
ok 1647 - dayStripRef classifies bob's typical without computing it
  ---
  duration_ms: 0.310052
  ...
# Subtest: typical line covers every States-table row
ok 1648 - typical line covers every States-table row
  ---
  duration_ms: 10.224811
  ...
# Subtest: typical line is aria-hidden, reserved, and never a tab stop
ok 1649 - typical line is aria-hidden, reserved, and never a tab stop
  ---
  duration_ms: 48.483815
  ...
# Subtest: off-clock hint prefers Bob's display and falls back to raw Nm without arithmetic
ok 1650 - off-clock hint prefers Bob's display and falls back to raw Nm without arithmetic
  ---
  duration_ms: 1.666031
  ...
# Subtest: hint renders below WORKED beside the typical line as its own activation target
ok 1651 - hint renders below WORKED beside the typical line as its own activation target
  ---
  duration_ms: 20.386951
  ...
# Subtest: lane legends and bars keep Worked meaning while the hint opens Off-clock
ok 1652 - lane legends and bars keep Worked meaning while the hint opens Off-clock
  ---
  duration_ms: 2.506876
  ...
# Subtest: DP parse vectors
ok 1653 - DP parse vectors
  ---
  duration_ms: 7.029932
  ...
# Subtest: DC chip model vectors
ok 1654 - DC chip model vectors
  ---
  duration_ms: 6.686827
  ...
# Subtest: decoration builds one widget, reveals on cursor, skips code and ranges
ok 1655 - decoration builds one widget, reveals on cursor, skips code and ranges
  ---
  duration_ms: 17.602575
  ...
# Subtest: decoration skips paragraphs, grandchildren, and Work Log lines
ok 1656 - decoration skips paragraphs, grandchildren, and Work Log lines
  ---
  duration_ms: 2.946024
  ...
# Subtest: decoration renders chips on DP30 and still skips DP20
ok 1657 - decoration renders chips on DP30 and still skips DP20
  ---
  duration_ms: 1.150857
  ...
# Subtest: ownership check reads O(depth) lines, not the whole note
ok 1658 - ownership check reads O(depth) lines, not the whole note
  ---
  duration_ms: 2.353914
  ...
# Subtest: widget identity covers the line and the interactive flag
ok 1659 - widget identity covers the line and the interactive flag
  ---
  duration_ms: 1.940174
  ...
# Subtest: element hides actions without nav api v1
ok 1660 - element hides actions without nav api v1
  ---
  duration_ms: 1.401777
  ...
# Subtest: nav api feature detection gates actions
ok 1661 - nav api feature detection gates actions
  ---
  duration_ms: 0.934193
  ...
# Subtest: reading view decorates only the Depends-On row, hides chrome, stays idempotent
ok 1662 - reading view decorates only the Depends-On row, hides chrome, stays idempotent
  ---
  duration_ms: 9.403845
  ...
# Subtest: reading view blocked chips draw a miniature and reason line
ok 1663 - reading view blocked chips draw a miniature and reason line
  ---
  duration_ms: 3.199007
  ...
# Subtest: reading view collapses more than three Done targets to one chip
ok 1664 - reading view collapses more than three Done targets to one chip
  ---
  duration_ms: 1.594985
  ...
# Subtest: DC chip model vectors by id: DC2, DC5, DC6, DC9
ok 1665 - DC chip model vectors by id: DC2, DC5, DC6, DC9
  ---
  duration_ms: 0.349047
  ...
# Subtest: chip actions send the 0-based line index through nav api v1
ok 1666 - chip actions send the 0-based line index through nav api v1
  ---
  duration_ms: 8.499426
  ...
# Subtest: chip hover passes the chip element and its row to the preview
ok 1667 - chip hover passes the chip element and its row to the preview
  ---
  duration_ms: 0.342704
  ...
# Subtest: chip lookup index lives on the freshness memo
ok 1668 - chip lookup index lives on the freshness memo
  ---
  duration_ms: 1.190813
  ...
# Subtest: reading view hides actions when the line cannot be derived
ok 1669 - reading view hides actions when the line cannot be derived
  ---
  duration_ms: 15.624812
  ...
# Subtest: reading view actions carry the derived 0-based line
ok 1670 - reading view actions carry the derived 0-based line
  ---
  duration_ms: 3.453423
  ...
# Subtest: reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
ok 1671 - reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
  ---
  duration_ms: 0.851125
  ...
# Subtest: reading view renders chips on DP30 (owner is a task under a Work Log entry)
ok 1672 - reading view renders chips on DP30 (owner is a task under a Work Log entry)
  ---
  duration_ms: 2.579415
  ...
# Subtest: reading view DP30 row actions send the owned Depends-On line
ok 1673 - reading view DP30 row actions send the owned Depends-On line
  ---
  duration_ms: 4.807779
  ...
# Subtest: reading view second-row remove sends the second line when two tasks share a prerequisite
ok 1674 - reading view second-row remove sends the second line when two tasks share a prerequisite
  ---
  duration_ms: 2.486316
  ...
# Subtest: chip lookup index builds once per freshness memo
ok 1675 - chip lookup index builds once per freshness memo
  ---
  duration_ms: 0.678095
  ...
# Subtest: decoration evaluates ownership without copying the note
ok 1676 - decoration evaluates ownership without copying the note
  ---
  duration_ms: 0.662394
  ...
# Subtest: blockMarkReasonLine keeps only the first tooltip line
ok 1677 - blockMarkReasonLine keeps only the first tooltip line
  ---
  duration_ms: 0.139527
  ...
# Subtest: chip box fill keeps a CSS fallback glyph beside the miniature
ok 1678 - chip box fill keeps a CSS fallback glyph beside the miniature
  ---
  duration_ms: 0.634922
  ...
# Subtest: toggle flips the body class and onload wires chips
ok 1679 - toggle flips the body class and onload wires chips
  ---
  duration_ms: 62.982225
  ...
# event-link-times build: 15.7 ms
# Subtest: EL — ledger rows qualify exactly per the contract
ok 1680 - EL — ledger rows qualify exactly per the contract
  ---
  duration_ms: 16.990197
  ...
# Subtest: EL18 — a fenced ledger row gets no pill
ok 1681 - EL18 — a fenced ledger row gets no pill
  ---
  duration_ms: 0.637337
  ...
# Subtest: EL19 — a non-daily note gets no pills
ok 1682 - EL19 — a non-daily note gets no pills
  ---
  duration_ms: 0.239226
  ...
# Subtest: EL16 — the previous day's ledger pills without state
ok 1683 - EL16 — the previous day's ledger pills without state
  ---
  duration_ms: 3.039864
  ...
# Subtest: ES — the shared clock answers the contract states
ok 1684 - ES — the shared clock answers the contract states
  ---
  duration_ms: 0.673195
  ...
# Subtest: ER — resolution matches the Events pill inputs
ok 1685 - ER — resolution matches the Events pill inputs
  ---
  duration_ms: 15.846544
  ...
# Subtest: ER — non-events, duplicates, and cross-note links resolve to no pill
ok 1686 - ER — non-events, duplicates, and cross-note links resolve to no pill
  ---
  duration_ms: 0.725725
  ...
# Subtest: ER5 — Live Preview reads the live document, unsaved edits included
ok 1687 - ER5 — Live Preview reads the live document, unsaved edits included
  ---
  duration_ms: 9.77911
  ...
# Subtest: ER6 — Live Preview dashes an unsaved off-clock tag on the same frame
ok 1688 - ER6 — Live Preview dashes an unsaved off-clock tag on the same frame
  ---
  duration_ms: 3.927298
  ...
# Subtest: ER7 — the inner pill carries the Events pill attributes, minus title
ok 1689 - ER7 — the inner pill carries the Events pill attributes, minus title
  ---
  duration_ms: 6.336309
  ...
# Subtest: ET — tooltips name the event and its pill state
ok 1690 - ET — tooltips name the event and its pill state
  ---
  duration_ms: 1.289071
  ...
# Subtest: EP1 — Live Preview places the pill at the link start, side -3
ok 1691 - EP1 — Live Preview places the pill at the link start, side -3
  ---
  duration_ms: 6.696375
  ...
# Subtest: EP4 — selection alone never rebuilds the pills
ok 1692 - EP4 — selection alone never rebuilds the pills
  ---
  duration_ms: 3.558463
  ...
# Subtest: EP2/EP5 — Reading view orders the pill before progress marks and keeps the ledger context
ok 1693 - EP2/EP5 — Reading view orders the pill before progress marks and keeps the ledger context
  ---
  duration_ms: 4.645809
  ...
# Subtest: EP3 — the pill lands before the link container beside a trailing chip
ok 1694 - EP3 — the pill lands before the link container beside a trailing chip
  ---
  duration_ms: 1.01058
  ...
# Subtest: EP3/OC — Reading sweeps preserve pill/link/marks/chip order and clock parity
ok 1695 - EP3/OC — Reading sweeps preserve pill/link/marks/chip order and clock parity
  ---
  duration_ms: 10.760974
  ...
# Subtest: EP7 — a struck link keeps the pill outside the strike
ok 1696 - EP7 — a struck link keeps the pill outside the strike
  ---
  duration_ms: 2.179712
  ...
# Subtest: EL20 — either toggle off hides every pill, in JS and CSS
ok 1697 - EL20 — either toggle off hides every pill, in JS and CSS
  ---
  duration_ms: 2.437465
  ...
# Subtest: setup — toggle command, popout gates, and clock repaint wiring
ok 1698 - setup — toggle command, popout gates, and clock repaint wiring
  ---
  duration_ms: 1.752116
  ...
# Subtest: liveness — metadata and vault events coalesce into one refresh
ok 1699 - liveness — metadata and vault events coalesce into one refresh
  ---
  duration_ms: 0.462282
  ...
# Subtest: liveness — a source-text fill refreshes link pills
ok 1700 - liveness — a source-text fill refreshes link pills
  ---
  duration_ms: 0.919145
  ...
# Subtest: perf — one build over a 200-link ledger stays under 25 ms
ok 1701 - perf — one build over a 200-link ledger stays under 25 ms
  ---
  duration_ms: 24.584094
  ...
# Subtest: widget — identity follows time, state, clock, buffer, and tooltip
ok 1702 - widget — identity follows time, state, clock, buffer, and tooltip
  ---
  duration_ms: 0.908514
  ...
# Subtest: regression FakeNode hides the plan-host cycles and builds 85 nodes
ok 1703 - regression FakeNode hides the plan-host cycles and builds 85 nodes
  ---
  duration_ms: 5.990006
  ...
# Subtest: failing assert.equal and assert.deepEqual report under a 1024MB cap
ok 1704 - failing assert.equal and assert.deepEqual report under a 1024MB cap
  ---
  duration_ms: 1139.228091
  ...
# Subtest: every ledger-tools FakeNode-style fake has a descriptor and hides its cyclic fields
ok 1705 - every ledger-tools FakeNode-style fake has a descriptor and hides its cyclic fields
  ---
  duration_ms: 53.540108
  ...
# Subtest: FL1-FL16: the ledger link gates match the display contract
ok 1706 - FL1-FL16: the ledger link gates match the display contract
  ---
  duration_ms: 21.795312
  ...
# Subtest: motion identity is the resolved owner path and block ID
ok 1707 - motion identity is the resolved owner path and block ID
  ---
  duration_ms: 3.0905
  ...
# Subtest: duplicate and aliased links resolve and count once per owner per build
ok 1708 - duplicate and aliased links resolve and count once per owner per build
  ---
  duration_ms: 2.15235
  ...
# Subtest: offscreen ledger targets do no resolution or count work until visible
ok 1709 - offscreen ledger targets do no resolution or count work until visible
  ---
  duration_ms: 0.488602
  ...
# Subtest: 200-link / 2000-task build stays within the 25 ms budget
ok 1710 - 200-link / 2000-task build stays within the 25 ms budget
  ---
  duration_ms: 50.270235
  ...
# Subtest: FC1-FC17: counts follow the BLOCKS last-blocker set
ok 1711 - FC1-FC17: counts follow the BLOCKS last-blocker set
  ---
  duration_ms: 6.837966
  ...
# Subtest: FT1-FT6: tooltips use BLOCKS order, clean titles, and waiting count
ok 1712 - FT1-FT6: tooltips use BLOCKS order, clean titles, and waiting count
  ---
  duration_ms: 0.918213
  ...
# Subtest: FC7-FC8: project and hidden labels follow the contract
ok 1713 - FC7-FC8: project and hidden labels follow the contract
  ---
  duration_ms: 0.346161
  ...
# Subtest: FP1-FP2: Live Preview places the widget after the link with side 2
ok 1714 - FP1-FP2: Live Preview places the widget after the link with side 2
  ---
  duration_ms: 7.12874
  ...
# Subtest: FP3-FP4: Reading view inserts after the link or after 🔓
ok 1715 - FP3-FP4: Reading view inserts after the link or after 🔓
  ---
  duration_ms: 2.417866
  ...
# Subtest: Reading view inserts beside a task-link-mark sibling and through one wrapping p
ok 1716 - Reading view inserts beside a task-link-mark sibling and through one wrapping p
  ---
  duration_ms: 6.060421
  ...
# Subtest: pinned midnight invalidates yesterday and gives today's editor a silent first paint
ok 1717 - pinned midnight invalidates yesterday and gives today's editor a silent first paint
  ---
  duration_ms: 1.834593
  ...
# Subtest: FT element and widget keep accessible attributes without a title
ok 1718 - FT element and widget keep accessible attributes without a title
  ---
  duration_ms: 6.55238
  ...
# Subtest: Live Preview tick LRU tracks 0 → N, count changes, and the 2000-key bound
ok 1719 - Live Preview tick LRU tracks 0 → N, count changes, and the 2000-key bound
  ---
  duration_ms: 2.868476
  ...
# Subtest: viewport-only rebuilds update visible count history without animating scroll-in
ok 1720 - viewport-only rebuilds update visible count history without animating scroll-in
  ---
  duration_ms: 1.214228
  ...
# Subtest: toggle, refresh effect, and modifier navigation are wired
ok 1721 - toggle, refresh effect, and modifier navigation are wired
  ---
  duration_ms: 5.181392
  ...
# Subtest: setup is idempotent and teardown clears the rollover interval
ok 1722 - setup is idempotent and teardown clears the rollover interval
  ---
  duration_ms: 0.397288
  ...
# Subtest: capability: nav card v2 is capable
ok 1723 - capability: nav card v2 is capable
  ---
  duration_ms: 1.42468
  ...
# Subtest: capability: nav card v1 is not capable
ok 1724 - capability: nav card v1 is not capable
  ---
  duration_ms: 0.223297
  ...
# Subtest: capability: absent nav, missing api, and old versions are not capable
ok 1725 - capability: absent nav, missing api, and old versions are not capable
  ---
  duration_ms: 0.176607
  ...
# Subtest: capability: a throwing app never throws
ok 1726 - capability: a throwing app never throws
  ---
  duration_ms: 0.261099
  ...
# Subtest: lane capability: nav card v3 is lane-capable, v2 is not
ok 1727 - lane capability: nav card v3 is lane-capable, v2 is not
  ---
  duration_ms: 0.243945
  ...
# Subtest: leaf: active capable due choice replaces refresh with a leaf
ok 1728 - leaf: active capable due choice replaces refresh with a leaf
  ---
  duration_ms: 4.017079
  ...
# Subtest: leaf: the same row without the card keeps refresh and counting words
ok 1729 - leaf: the same row without the card keeps refresh and counting words
  ---
  duration_ms: 0.719253
  ...
# Subtest: leaf: early dates still leaf when capable
ok 1730 - leaf: early dates still leaf when capable
  ---
  duration_ms: 0.506167
  ...
# Subtest: leaf: decay-off rows never leaf even when capable
ok 1731 - leaf: decay-off rows never leaf even when capable
  ---
  duration_ms: 0.877175
  ...
# Subtest: leaf: below-threshold rows never leaf
ok 1732 - leaf: below-threshold rows never leaf
  ---
  duration_ms: 0.81685
  ...
# Subtest: leaf: threshold zero asks on every due re-confirmation when capable
ok 1733 - leaf: threshold zero asks on every due re-confirmation when capable
  ---
  duration_ms: 0.428478
  ...
# Subtest: leaf: overflow renders capped dots with +N and the exact count in text
ok 1734 - leaf: overflow renders capped dots with +N and the exact count in text
  ---
  duration_ms: 0.345139
  ...
# Subtest: leaf: out-of-scope and closed tasks show dots quietly, never a leaf
ok 1735 - leaf: out-of-scope and closed tasks show dots quietly, never a leaf
  ---
  duration_ms: 1.071035
  ...
# Subtest: leaf: unresolved marks show dots quietly with counting-only wording
ok 1736 - leaf: unresolved marks show dots quietly with counting-only wording
  ---
  duration_ms: 0.2828
  ...
# Subtest: element: leaf marks carry data-decide true and a leaf path
ok 1737 - element: leaf marks carry data-decide true and a leaf path
  ---
  duration_ms: 0.882235
  ...
# Subtest: element: non-decision marks carry data-decide false
ok 1738 - element: non-decision marks carry data-decide false
  ---
  duration_ms: 0.351391
  ...
# Subtest: lane leaf: an at-limit Next row leaves only with the v3 card
ok 1739 - lane leaf: an at-limit Next row leaves only with the v3 card
  ---
  duration_ms: 0.338527
  ...
# Subtest: lane leaf: the same row with only the v2 card keeps counting pips
ok 1740 - lane leaf: the same row with only the v2 card keeps counting pips
  ---
  duration_ms: 0.311074
  ...
# Subtest: lane leaf: an at-limit WIP row leaves only with the v3 card
ok 1741 - lane leaf: an at-limit WIP row leaves only with the v3 card
  ---
  duration_ms: 0.370337
  ...
# Subtest: lane leaf: a false rung counts and displays but never asks
ok 1742 - lane leaf: a false rung counts and displays but never asks
  ---
  duration_ms: 0.301346
  ...
# Subtest: lane leaf: a per-rung limit drives the keeps wording
ok 1743 - lane leaf: a per-rung limit drives the keeps wording
  ---
  duration_ms: 0.264225
  ...
# Subtest: footer groups omit every zero tier and keep walk order
ok 1744 - footer groups omit every zero tier and keep walk order
  ---
  duration_ms: 11.0929
  ...
# Subtest: PRE and POST groups bracket the nine-tier queue and expose completion hints
ok 1745 - PRE and POST groups bracket the nine-tier queue and expose completion hints
  ---
  duration_ms: 1.339317
  ...
# Subtest: a NEW-state project appears only in its walk tier
ok 1746 - a NEW-state project appears only in its walk tier
  ---
  duration_ms: 0.307497
  ...
# Subtest: empty queue hides the footer even with upkeep or a met budget
ok 1747 - empty queue hides the footer even with upkeep or a met budget
  ---
  duration_ms: 0.268182
  ...
# Subtest: unavailable or missing data never render false counts
ok 1748 - unavailable or missing data never render false counts
  ---
  duration_ms: 0.195733
  ...
# Subtest: generic summary names due, commitments, and nonempty groups
ok 1749 - generic summary names due, commitments, and nonempty groups
  ---
  duration_ms: 4.876429
  ...
# Subtest: current-task context uses shared ranks and compact wording
ok 1750 - current-task context uses shared ranks and compact wording
  ---
  duration_ms: 0.909186
  ...
# Subtest: only ROTTEN remaining names commitments done or a met budget
ok 1751 - only ROTTEN remaining names commitments done or a met budget
  ---
  duration_ms: 0.306184
  ...
# Subtest: NEW and commitments take precedence over a met budget
ok 1752 - NEW and commitments take precedence over a met budget
  ---
  duration_ms: 0.509963
  ...
# Subtest: reviewEntryView compact and detail cover the original freshness tiers
ok 1753 - reviewEntryView compact and detail cover the original freshness tiers
  ---
  duration_ms: 5.329796
  ...
# Subtest: cursor matching requires a unique verified identity
ok 1754 - cursor matching requires a unique verified identity
  ---
  duration_ms: 0.651203
  ...
# Subtest: footer paint hides the host and keeps a stable button
ok 1755 - footer paint hides the host and keeps a stable button
  ---
  duration_ms: 2.314919
  ...
# Subtest: groups paint as tier-keyed tokens and repaint without stale nodes
ok 1756 - groups paint as tier-keyed tokens and repaint without stale nodes
  ---
  duration_ms: 5.596554
  ...
# Subtest: group boundary marks only the commitments-to-upkeep cut
ok 1757 - group boundary marks only the commitments-to-upkeep cut
  ---
  duration_ms: 0.575038
  ...
# Subtest: context ink follows supported current tiers and clears on other views
ok 1758 - context ink follows supported current tiers and clears on other views
  ---
  duration_ms: 0.712751
  ...
# Subtest: progressive fit sheds tail groups, then detail, hint, and meter
ok 1759 - progressive fit sheds tail groups, then detail, hint, and meter
  ---
  duration_ms: 6.294998
  ...
# Subtest: the footer stylesheet defines every tier ink and removes NEW accent overrides
ok 1760 - the footer stylesheet defines every tier ink and removes NEW accent overrides
  ---
  duration_ms: 2.141068
  ...
# Subtest: status bar 0-1-0 transitions hide without a reload
ok 1761 - status bar 0-1-0 transitions hide without a reload
  ---
  duration_ms: 426.732841
  ...
# Subtest: cursor-only updates reuse a warm memo
ok 1762 - cursor-only updates reuse a warm memo
  ---
  duration_ms: 174.535979
  ...
# Subtest: unload disconnects the observer and click handler
ok 1763 - unload disconnects the observer and click handler
  ---
  duration_ms: 173.394813
  ...
# Subtest: queue-built ranks agree with the footer current entry
ok 1764 - queue-built ranks agree with the footer current entry
  ---
  duration_ms: 42.468159
  ...
# Subtest: footer short labels map every tier
ok 1765 - footer short labels map every tier
  ---
  duration_ms: 0.381578
  ...
# Subtest: current-row footer context uses short labels while entry views keep full labels
ok 1766 - current-row footer context uses short labels while entry views keep full labels
  ---
  duration_ms: 0.572974
  ...
# Subtest: legend line lists only current abbreviated tiers
ok 1767 - legend line lists only current abbreviated tiers
  ---
  duration_ms: 0.474937
  ...
# Subtest: queue-row quickRoll preview takes the hint slot, tooltip, and aria
ok 1768 - queue-row quickRoll preview takes the hint slot, tooltip, and aria
  ---
  duration_ms: 0.362532
  ...
# Subtest: quickRoll detail sits next to the action hint on lane rows
ok 1769 - quickRoll detail sits next to the action hint on lane rows
  ---
  duration_ms: 0.301095
  ...
# Subtest: missing or failed quickRoll leaves a queue-row footer byte-identical
ok 1770 - missing or failed quickRoll leaves a queue-row footer byte-identical
  ---
  duration_ms: 0.556081
  ...
# Subtest: off-walk prioritized preview replaces ]s next
ok 1771 - off-walk prioritized preview replaces ]s next
  ---
  duration_ms: 0.343356
  ...
# Subtest: off-walk assign or kind-less preview keeps ]s next
ok 1772 - off-walk assign or kind-less preview keeps ]s next
  ---
  duration_ms: 0.236181
  ...
# Subtest: empty queue with a prioritized preview paints a hint-only footer
ok 1773 - empty queue with a prioritized preview paints a hint-only footer
  ---
  duration_ms: 37.049534
  ...
# Subtest: PRE rows stay unchanged under the nav checklist-tier contract
ok 1774 - PRE rows stay unchanged under the nav checklist-tier contract
  ---
  duration_ms: 0.381307
  ...
# Subtest: status bar wires nav api.quickRoll into the hint slot
ok 1775 - status bar wires nav api.quickRoll into the hint slot
  ---
  duration_ms: 207.257452
  ...
# Subtest: empty-queue status bar previews only a checkbox task line
ok 1776 - empty-queue status bar previews only a checkbox task line
  ---
  duration_ms: 551.836705
  ...
# Subtest: off-walk task preview works with a queue and survives its 1-to-0 transition
ok 1777 - off-walk task preview works with a queue and survives its 1-to-0 transition
  ---
  duration_ms: 234.5087
  ...
# Subtest: status bar ignores missing, v0, or throwing quickRoll namespaces
ok 1778 - status bar ignores missing, v0, or throwing quickRoll namespaces
  ---
  duration_ms: 1137.835151
  ...
# Subtest: answer tiers list only tickler
ok 1779 - answer tiers list only tickler
  ---
  duration_ms: 0.252752
  ...
# Subtest: freshnessFooterAnswerChip builds structured segments for every kind
ok 1780 - freshnessFooterAnswerChip builds structured segments for every kind
  ---
  duration_ms: 1.640492
  ...
# Subtest: a TICK row with a preview has answer set and unchanged hint, tooltip, and aria
ok 1781 - a TICK row with a preview has answer set and unchanged hint, tooltip, and aria
  ---
  duration_ms: 0.613011
  ...
# Subtest: a TICK view paints the answer chip and reuses or clears it by key
ok 1782 - a TICK view paints the answer chip and reuses or clears it by key
  ---
  duration_ms: 1.388541
  ...
# Subtest: a TICK fit sheds the meter before the hint chip
ok 1783 - a TICK fit sheds the meter before the hint chip
  ---
  duration_ms: 1.013014
  ...
# Subtest: the footer stylesheet defines the TICK answer chip
ok 1784 - the footer stylesheet defines the TICK answer chip
  ---
  duration_ms: 38.70211
  ...
# Subtest: walker host keeps the same status item and marks it
ok 1785 - walker host keeps the same status item and marks it
  ---
  duration_ms: 270.539909
  ...
# Subtest: gated s panel keeps the review footer with ]] next hints
ok 1786 - gated s panel keeps the review footer with ]] next hints
  ---
  duration_ms: 351.862377
  ...
# Subtest: n routes to links while w and unset hide the panel
ok 1787 - n routes to links while w and unset hide the panel
  ---
  duration_ms: 784.382617
  ...
# Subtest: an invalid stored family never paints as s
ok 1788 - an invalid stored family never paints as s
  ---
  duration_ms: 207.008988
  ...
# Subtest: doorbell repaints synchronously on family change
ok 1789 - doorbell repaints synchronously on family change
  ---
  duration_ms: 240.61712
  ...
# Subtest: empty queue paints Review clear while s is selected
ok 1790 - empty queue paints Review clear while s is selected
  ---
  duration_ms: 325.087862
  ...
# Subtest: clear state keeps the prioritized Alt+P preview
ok 1791 - clear state keeps the prioritized Alt+P preview
  ---
  duration_ms: 274.915052
  ...
# Subtest: legacy fallback without nav paints today's footer byte-identical
ok 1792 - legacy fallback without nav paints today's footer byte-identical
  ---
  duration_ms: 267.49143
  ...
# Subtest: old nav without walkMode keeps the ]s next legacy footer
ok 1793 - old nav without walkMode keeps the ]s next legacy footer
  ---
  duration_ms: 372.669995
  ...
# Subtest: late nav arrival gates the footer; nav removal restores legacy
ok 1794 - late nav arrival gates the footer; nav removal restores legacy
  ---
  duration_ms: 175.25915
  ...
# Subtest: unload and reload mount one item and one doorbell subscription
ok 1795 - unload and reload mount one item and one doorbell subscription
  ---
  duration_ms: 1084.384547
  ...
# Subtest: a throwing doorbell path never breaks setup or painting
ok 1796 - a throwing doorbell path never breaks setup or painting
  ---
  duration_ms: 451.377892
  ...
# Subtest: K1 absent: no keeps means 0 with no lints
ok 1797 - K1 absent: no keeps means 0 with no lints
  ---
  duration_ms: 7.843936
  ...
# Subtest: K8 misplaced: keeps inside the Tasks suffix reads with a lint
ok 1798 - K8 misplaced: keeps inside the Tasks suffix reads with a lint
  ---
  duration_ms: 0.742087
  ...
# Subtest: K9 duplicates and invalid values: first valid wins, else 0
ok 1799 - K9 duplicates and invalid values: first valid wins, else 0
  ---
  duration_ms: 0.866965
  ...
# Subtest: K10 ceiling and NEW: 999 reads, never-confirmed reads 0
ok 1800 - K10 ceiling and NEW: 999 reads, never-confirmed reads 0
  ---
  duration_ms: 0.271138
  ...
# Subtest: K13 exact keys: near-miss keys are not keeps; parens read
ok 1801 - K13 exact keys: near-miss keys are not keeps; parens read
  ---
  duration_ms: 2.57677
  ...
# Subtest: keeps value parser accepts only decimal 1-999
ok 1802 - keeps value parser accepts only decimal 1-999
  ---
  duration_ms: 4.754878
  ...
# Subtest: K2 first valid canonical: uncounted keep preserves and repairs
ok 1803 - K2 first valid canonical: uncounted keep preserves and repairs
  ---
  duration_ms: 4.126738
  ...
# Subtest: K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
ok 1804 - K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
  ---
  duration_ms: 3.277938
  ...
# Subtest: K4 same-day preserve noop: canonical kept line is byte-identical
ok 1805 - K4 same-day preserve noop: canonical kept line is byte-identical
  ---
  duration_ms: 0.685429
  ...
# Subtest: K5 generic stamp clears, even same-day
ok 1806 - K5 generic stamp clears, even same-day
  ---
  duration_ms: 0.826548
  ...
# Subtest: K6 set-refresh clears keeps
ok 1807 - K6 set-refresh clears keeps
  ---
  duration_ms: 0.346672
  ...
# Subtest: K7 stale stamp clears keeps
ok 1808 - K7 stale stamp clears keeps
  ---
  duration_ms: 0.223697
  ...
# Subtest: K8b misplaced keeps repaired to canonical order by a keep
ok 1809 - K8b misplaced keeps repaired to canonical order by a keep
  ---
  duration_ms: 0.252823
  ...
# Subtest: K11 refusals preserve: closed and recurring lines never write
ok 1810 - K11 refusals preserve: closed and recurring lines never write
  ---
  duration_ms: 0.284813
  ...
# Subtest: Pomodoro ledger rows are refused byte-for-byte by counted and uncounted keep
ok 1811 - Pomodoro ledger rows are refused byte-for-byte by counted and uncounted keep
  ---
  duration_ms: 0.543318
  ...
# Subtest: counted keep increments a stale streak once in the same write
ok 1812 - counted keep increments a stale streak once in the same write
  ---
  duration_ms: 0.30376
  ...
# Subtest: first counted keep on a streakless due task writes keeps 1
ok 1813 - first counted keep on a streakless due task writes keeps 1
  ---
  duration_ms: 0.252622
  ...
# Subtest: counted keep saturates at 999 and never wraps
ok 1814 - counted keep saturates at 999 and never wraps
  ---
  duration_ms: 0.226372
  ...
# Subtest: counted keep needs a valid prior fresh before today
ok 1815 - counted keep needs a valid prior fresh before today
  ---
  duration_ms: 0.401156
  ...
# Subtest: counted keep repairs malformed and duplicate placement
ok 1816 - counted keep repairs malformed and duplicate placement
  ---
  duration_ms: 1.70774
  ...
# Subtest: uncounted keep preserves the valid value while canonicalizing
ok 1817 - uncounted keep preserves the valid value while canonicalizing
  ---
  duration_ms: 0.327525
  ...
# Subtest: UB13 keep on an unblock TICKLER preserves the streak and skips the card
ok 1818 - UB13 keep on an unblock TICKLER preserves the streak and skips the card
  ---
  duration_ms: 1.113055
  ...
# Subtest: a scheduled tickler still counts when schedule wins an unblock tie
ok 1819 - a scheduled tickler still counts when schedule wins an unblock tie
  ---
  duration_ms: 0.458405
  ...
# Subtest: decay normalization: absent, null, true, and {} enable with 3
ok 1820 - decay normalization: absent, null, true, and {} enable with 3
  ---
  duration_ms: 1.368442
  ...
# Subtest: decay false counts and displays but never asks
ok 1821 - decay false counts and displays but never asks
  ---
  duration_ms: 0.14637
  ...
# Subtest: decay keeps 0 and fixed entry normalize
ok 1822 - decay keeps 0 and fixed entry normalize
  ---
  duration_ms: 0.204962
  ...
# Subtest: C14 pending override resolves while other rungs fall back
ok 1823 - C14 pending override resolves while other rungs fall back
  ---
  duration_ms: 0.150578
  ...
# Subtest: C15 fallback plus next override
ok 1824 - C15 fallback plus next override
  ---
  duration_ms: 0.152451
  ...
# Subtest: C16 zero, false, and 999 rungs
ok 1825 - C16 zero, false, and 999 rungs
  ---
  duration_ms: 0.498923
  ...
# Subtest: C17 null rung falls back to keeps
ok 1826 - C17 null rung falls back to keeps
  ---
  duration_ms: 0.245628
  ...
# Subtest: rung limit helper resolves numbers, false, and fallbacks
ok 1827 - rung limit helper resolves numbers, false, and fallbacks
  ---
  duration_ms: 0.143444
  ...
# Subtest: invalid decay shapes fail the freshness config contract
ok 1828 - invalid decay shapes fail the freshness config contract
  ---
  duration_ms: 0.438478
  ...
# Subtest: B: at-limit Ready due rows decide on every local day
ok 1829 - B: at-limit Ready due rows decide on every local day
  ---
  duration_ms: 0.808724
  ...
# Subtest: D1 early date: an at-limit Ready due row decides
ok 1830 - D1 early date: an at-limit Ready due row decides
  ---
  duration_ms: 0.290184
  ...
# Subtest: D2 at limit decides; D3 below limit stamps without a card
ok 1831 - D2 at limit decides; D3 below limit stamps without a card
  ---
  duration_ms: 0.180394
  ...
# Subtest: D4 tickler counts as due; D5 NEW never decides
ok 1832 - D4 tickler counts as due; D5 NEW never decides
  ---
  duration_ms: 0.124518
  ...
# Subtest: D6 zero limit asks on every due Ready re-confirmation
ok 1833 - D6 zero limit asks on every due Ready re-confirmation
  ---
  duration_ms: 0.131671
  ...
# Subtest: D7 off never asks; D8 an at-limit Next due row decides
ok 1834 - D7 off never asks; D8 an at-limit Next due row decides
  ---
  duration_ms: 0.134317
  ...
# Subtest: D9 pending at limit decides; D10-D11 below limit stay quiet
ok 1835 - D9 pending at limit decides; D10-D11 below limit stay quiet
  ---
  duration_ms: 0.138975
  ...
# Subtest: D12 next_keeps false never asks; D13 pending_keeps 0 always asks
ok 1836 - D12 next_keeps false never asks; D13 pending_keeps 0 always asks
  ---
  duration_ms: 0.272941
  ...
# Subtest: D14 today-linked lane rows never decide
ok 1837 - D14 today-linked lane rows never decide
  ---
  duration_ms: 0.116702
  ...
# Subtest: D15 projects never decide; D16 unblock ticklers never decide
ok 1838 - D15 projects never decide; D16 unblock ticklers never decide
  ---
  duration_ms: 0.12024
  ...
# Subtest: D17-D18 next_keeps override of 5 decides at 5, quiet at 4
ok 1839 - D17-D18 next_keeps override of 5 decides at 5, quiet at 4
  ---
  duration_ms: 0.226573
  ...
# Subtest: lane rows decide through the evaluator, queue, and counts
ok 1840 - lane rows decide through the evaluator, queue, and counts
  ---
  duration_ms: 1.020157
  ...
# Subtest: evaluator, queue, and counts carry keeps and decide
ok 1841 - evaluator, queue, and counts carry keeps and decide
  ---
  duration_ms: 3.430609
  ...
# Subtest: no keeps: the existing mark is unchanged
ok 1842 - no keeps: the existing mark is unchanged
  ---
  duration_ms: 1.22002
  ...
# Subtest: aging with two keeps: faint pips plus a counting-only line
ok 1843 - aging with two keeps: faint pips plus a counting-only line
  ---
  duration_ms: 1.991813
  ...
# Subtest: confirmed today with two keeps: check glyph, faint dots
ok 1844 - confirmed today with two keeps: check glyph, faint dots
  ---
  duration_ms: 0.255347
  ...
# Subtest: due below threshold: orange capsule keeps its glyph, adds dots
ok 1845 - due below threshold: orange capsule keeps its glyph, adds dots
  ---
  duration_ms: 0.311565
  ...
# Subtest: resting marks show historical dots quietly and never decide
ok 1846 - resting marks show historical dots quietly and never decide
  ---
  duration_ms: 0.496247
  ...
# Subtest: active decision due: data stays truthful, leaf stays gated
ok 1847 - active decision due: data stays truthful, leaf stays gated
  ---
  duration_ms: 0.319891
  ...
# Subtest: dot caps follow the threshold with +N overflow
ok 1848 - dot caps follow the threshold with +N overflow
  ---
  duration_ms: 1.067549
  ...
# Subtest: keeps tooltip wording: singulars, zero threshold, off state
ok 1849 - keeps tooltip wording: singulars, zero threshold, off state
  ---
  duration_ms: 0.164274
  ...
# Subtest: noncanonical keeps never fold but keep their repair pill
ok 1850 - noncanonical keeps never fold but keep their repair pill
  ---
  duration_ms: 0.433538
  ...
# Subtest: quoted lines fold; rendered fragments fold without task checks
ok 1851 - quoted lines fold; rendered fragments fold without task checks
  ---
  duration_ms: 0.453456
  ...
# Subtest: unresolved marks show the line's own pips quietly and never decide
ok 1852 - unresolved marks show the line's own pips quietly and never decide
  ---
  duration_ms: 0.249536
  ...
# Subtest: consensus sees count and decision eligibility: ambiguity stays neutral
ok 1853 - consensus sees count and decision eligibility: ambiguity stays neutral
  ---
  duration_ms: 0.641745
  ...
# Subtest: pips render as one aria-hidden span with the count in the label
ok 1854 - pips render as one aria-hidden span with the count in the label
  ---
  duration_ms: 1.243053
  ...
# Subtest: Live Preview decorates the folded range including space and refresh
ok 1855 - Live Preview decorates the folded range including space and refresh
  ---
  duration_ms: 15.754369
  ...
# Subtest: Live Preview reveals the raw field when the cursor overlaps either edge
ok 1856 - Live Preview reveals the raw field when the cursor overlaps either edge
  ---
  duration_ms: 1.987375
  ...
# Subtest: Live Preview skips codeblock and inline code spans
ok 1857 - Live Preview skips codeblock and inline code spans
  ---
  duration_ms: 0.983568
  ...
# Subtest: source mode and marks-off yield no decorations
ok 1858 - source mode and marks-off yield no decorations
  ---
  duration_ms: 0.521054
  ...
# Subtest: update rebuilds on the refresh effect and widget eq is stable
ok 1859 - update rebuilds on the refresh effect and widget eq is stable
  ---
  duration_ms: 1.794236
  ...
# Subtest: widget click reveals the field at the folded offset
ok 1860 - widget click reveals the field at the folded offset
  ---
  duration_ms: 18.381284
  ...
# Subtest: line resolver prefers exact, then consensus, then unresolved
ok 1861 - line resolver prefers exact, then consensus, then unresolved
  ---
  duration_ms: 1.911249
  ...
# Subtest: decoration builds reuse the snapshot without touching the loader
ok 1862 - decoration builds reuse the snapshot without touching the loader
  ---
  duration_ms: 0.627308
  ...
# Subtest: rendered views split text nodes and skip excluded ancestors
ok 1863 - rendered views split text nodes and skip excluded ancestors
  ---
  duration_ms: 27.219717
  ...
# Subtest: rendered views stay idempotent
ok 1864 - rendered views stay idempotent
  ---
  duration_ms: 14.188478
  ...
# Subtest: text resolver reaches consensus and degrades to neutral
ok 1865 - text resolver reaches consensus and degrades to neutral
  ---
  duration_ms: 1.180043
  ...
# Subtest: session toggle flips the body class and notifies
ok 1866 - session toggle flips the body class and notifies
  ---
  duration_ms: 13.883736
  ...
# Subtest: Live Preview reads only the child block and never calls doc.toString
ok 1867 - Live Preview reads only the child block and never calls doc.toString
  ---
  duration_ms: 2.375505
  ...
# Subtest: Live Preview stops at the first nonblank line at or above the task
ok 1868 - Live Preview stops at the first nonblank line at or above the task
  ---
  duration_ms: 0.405474
  ...
# Subtest: Live Preview performance stays bounded on a large child block
ok 1869 - Live Preview performance stays bounded on a large child block
  ---
  duration_ms: 6914.816699
  ...
# Subtest: reading view shows the rotten line and excludes Tasks and Dataview rows
ok 1870 - reading view shows the rotten line and excludes Tasks and Dataview rows
  ---
  duration_ms: 0.902543
  ...
# Subtest: reading-view DOM history counts a Next lane entry
ok 1871 - reading-view DOM history counts a Next lane entry
  ---
  duration_ms: 54.346698
  ...
# Subtest: query-row consensus stays byte-identical with and without a Rotten Log
ok 1872 - query-row consensus stays byte-identical with and without a Rotten Log
  ---
  duration_ms: 0.678004
  ...
# Subtest: onload registers the toggle, extension, and post-processor
ok 1873 - onload registers the toggle, extension, and post-processor
  ---
  duration_ms: 1011.851115
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 1874 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 0.88015
  ...
# Subtest: shared grammar fixture round-trips parse vectors and tallies
ok 1875 - shared grammar fixture round-trips parse vectors and tallies
  ---
  duration_ms: 5.453561
  ...
# Subtest: M1 today: check glyph, today label, full ring
ok 1876 - M1 today: check glyph, today label, full ring
  ---
  duration_ms: 3.593651
  ...
# Subtest: M2 aging: ring glyph, 3d label, draining lease
ok 1877 - M2 aging: ring glyph, 3d label, draining lease
  ---
  duration_ms: 0.689146
  ...
# Subtest: M3 boundary: ROTTEN due capsule with Alt+F hint
ok 1878 - M3 boundary: ROTTEN due capsule with Alt+F hint
  ---
  duration_ms: 0.547586
  ...
# Subtest: checklist marks replace stamp hints with their completion tier
ok 1879 - checklist marks replace stamp hints with their completion tier
  ---
  duration_ms: 1.863327
  ...
# Subtest: M4 yesterday uses the yesterday relative
ok 1880 - M4 yesterday uses the yesterday relative
  ---
  duration_ms: 0.343957
  ...
# Subtest: M5 folded refresh shows the /14d suffix
ok 1881 - M5 folded refresh shows the /14d suffix
  ---
  duration_ms: 0.648769
  ...
# Subtest: M6 refresh today: today tone hides the interval suffix
ok 1882 - M6 refresh today: today tone hides the interval suffix
  ---
  duration_ms: 0.321184
  ...
# Subtest: M7 note interval stays tooltip-only
ok 1883 - M7 note interval stays tooltip-only
  ---
  duration_ms: 0.867878
  ...
# Subtest: M8 resurfaced: due tone on the scheduled return
ok 1884 - M8 resurfaced: due tone on the scheduled return
  ---
  duration_ms: 0.829594
  ...
# Subtest: M9 due NEXT lane with keep/release/today keys
ok 1885 - M9 due NEXT lane with keep/release/today keys
  ---
  duration_ms: 0.385647
  ...
# Subtest: M10 NEXT lane stamped today
ok 1886 - M10 NEXT lane stamped today
  ---
  duration_ms: 0.29861
  ...
# Subtest: M19 disabled Next lane rests
ok 1887 - M19 disabled Next lane rests
  ---
  duration_ms: 0.367592
  ...
# Subtest: M20 PENDING lane folds refresh without the suffix
ok 1888 - M20 PENDING lane folds refresh without the suffix
  ---
  duration_ms: 0.330982
  ...
# Subtest: M11 closed: resting beats age 0
ok 1889 - M11 closed: resting beats age 0
  ---
  duration_ms: 0.272
  ...
# Subtest: M12 unresolved running and M13 unresolved lease over
ok 1890 - M12 unresolved running and M13 unresolved lease over
  ---
  duration_ms: 0.288069
  ...
# Subtest: M14 linked today rests with its reason
ok 1891 - M14 linked today rests with its reason
  ---
  duration_ms: 0.282248
  ...
# Subtest: M15 other year shows the year and the 282d age
ok 1892 - M15 other year shows the year and the 282d age
  ---
  duration_ms: 0.190835
  ...
# Subtest: M16 quoted line keeps foldSpace
ok 1893 - M16 quoted line keeps foldSpace
  ---
  duration_ms: 0.199881
  ...
# Subtest: M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
ok 1894 - M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
  ---
  duration_ms: 0.495516
  ...
# Subtest: N1-N6 non-canonical lines get no mark
ok 1895 - N1-N6 non-canonical lines get no mark
  ---
  duration_ms: 0.282068
  ...
# Subtest: C1-C3 consensus is exact or unresolved
ok 1896 - C1-C3 consensus is exact or unresolved
  ---
  duration_ms: 0.692782
  ...
# Subtest: freshnessMarkResolution treats evaluator new as unresolved
ok 1897 - freshnessMarkResolution treats evaluator new as unresolved
  ---
  duration_ms: 0.149445
  ...
# Subtest: freshnessMarkSourceInText covers rendered fragments
ok 1898 - freshnessMarkSourceInText covers rendered fragments
  ---
  duration_ms: 0.277249
  ...
# Subtest: tone order: closed, then due, then age 0, then out of scope
ok 1899 - tone order: closed, then due, then age 0, then out of scope
  ---
  duration_ms: 0.449438
  ...
# Subtest: no tooltip ever contains a double colon
ok 1900 - no tooltip ever contains a double colon
  ---
  duration_ms: 0.938733
  ...
# Subtest: freshnessShortDate pins English names and the year rule
ok 1901 - freshnessShortDate pins English names and the year rule
  ---
  duration_ms: 0.139918
  ...
# Subtest: DOM builder structure, attributes, and ring geometry
ok 1902 - DOM builder structure, attributes, and ring geometry
  ---
  duration_ms: 1.421253
  ...
# Subtest: every mark helper is synchronous and never throws on bad input
ok 1903 - every mark helper is synchronous and never throws on bad input
  ---
  duration_ms: 0.140989
  ...
# Subtest: rotten line wording covers 0, 1, and many entries
ok 1904 - rotten line wording covers 0, 1, and many entries
  ---
  duration_ms: 0.878728
  ...
# Subtest: rotten line date format includes the year only when it differs
ok 1905 - rotten line date format includes the year only when it differs
  ---
  duration_ms: 0.176988
  ...
# Subtest: rotten line truncates the reason to 48 code points without splitting emoji
ok 1906 - rotten line truncates the reason to 48 code points without splitting emoji
  ---
  duration_ms: 0.207386
  ...
# Subtest: rotten history rejects ambiguous, invalid, and nested entries
ok 1907 - rotten history rejects ambiguous, invalid, and nested entries
  ---
  duration_ms: 1.028293
  ...
# Subtest: rotten marker vectors reject mismatched emoji and missing spaces
ok 1908 - rotten marker vectors reject mismatched emoji and missing spaces
  ---
  duration_ms: 0.681482
  ...
# Subtest: rotten line splices before the action line and reaches aria-label
ok 1909 - rotten line splices before the action line and reaches aria-label
  ---
  duration_ms: 0.483102
  ...
# Subtest: freshness namespace v14 exposes checklist stages with per-rung decay and unblock TICKLER writers
ok 1910 - freshness namespace v14 exposes checklist stages with per-rung decay and unblock TICKLER writers
  ---
  duration_ms: 174.448904
  ...
# Subtest: freshness state and count API expose an unblock return source
ok 1911 - freshness state and count API expose an unblock return source
  ---
  duration_ms: 180.109752
  ...
# Subtest: checklist rows report tier and rank while keeping the READY bucket null
ok 1912 - checklist rows report tier and rank while keeping the READY bucket null
  ---
  duration_ms: 69.479309
  ...
# Subtest: tier, isDue, and rank cover lane rows
ok 1913 - tier, isDue, and rank cover lane rows
  ---
  duration_ms: 401.681623
  ...
# Subtest: memo invalidates on a new tasks array, rollover, and frontmatter
ok 1914 - memo invalidates on a new tasks array, rollover, and frontmatter
  ---
  duration_ms: 269.085082
  ...
# Subtest: the reload event fires only when the due key set changes
ok 1915 - the reload event fires only when the due key set changes
  ---
  duration_ms: 181.80027
  ...
# Subtest: status bar text covers every state, and a missing host stays quiet
ok 1916 - status bar text covers every state, and a missing host stays quiet
  ---
  duration_ms: 196.255677
  ...
# Subtest: status bar clicks through, falling back to rotten
ok 1917 - status bar clicks through, falling back to rotten
  ---
  duration_ms: 567.497805
  ...
# Subtest: every freshness api member is synchronous and never throws
ok 1918 - every freshness api member is synchronous and never throws
  ---
  duration_ms: 243.94274
  ...
# Subtest: placement vectors P1-P11, P14-P16, P18 stamp canonically
ok 1919 - placement vectors P1-P11, P14-P16, P18 stamp canonically
  ---
  duration_ms: 25.605835
  ...
# Subtest: P12 set and clear refresh stamps alongside
ok 1920 - P12 set and clear refresh stamps alongside
  ---
  duration_ms: 20.883972
  ...
# Subtest: P13 recurring and P17 done tasks are refused unchanged
ok 1921 - P13 recurring and P17 done tasks are refused unchanged
  ---
  duration_ms: 0.501678
  ...
# Subtest: Pomodoro ledger rows are refused byte-for-byte by every fresh writer
ok 1922 - Pomodoro ledger rows are refused byte-for-byte by every fresh writer
  ---
  duration_ms: 0.804426
  ...
# Subtest: a time range later in task prose remains eligible for freshness
ok 1923 - a time range later in task prose remains eligible for freshness
  ---
  duration_ms: 0.255418
  ...
# Subtest: U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
ok 1924 - U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
  ---
  duration_ms: 0.986283
  ...
# Subtest: reader reports misplaced and duplicate fields
ok 1925 - reader reports misplaced and duplicate fields
  ---
  duration_ms: 15.691276
  ...
# Subtest: Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
ok 1926 - Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
  ---
  duration_ms: 17.731934
  ...
# Subtest: Q2 tier order beats path order
ok 1927 - Q2 tier order beats path order
  ---
  duration_ms: 1.813993
  ...
# Subtest: L1 lane due and stamped today
ok 1928 - L1 lane due and stamped today
  ---
  duration_ms: 0.492691
  ...
# Subtest: L2 lane overrides refresh
ok 1929 - L2 lane overrides refresh
  ---
  duration_ms: 0.318138
  ...
# Subtest: L3 lane exclusions have no tier
ok 1930 - L3 lane exclusions have no tier
  ---
  duration_ms: 0.465298
  ...
# Subtest: L4 lane off switch and null default
ok 1931 - L4 lane off switch and null default
  ---
  duration_ms: 12.882736
  ...
# Subtest: L5 lane order never stamped first
ok 1932 - L5 lane order never stamped first
  ---
  duration_ms: 0.955444
  ...
# Subtest: R1 TICKLER beats older ROTTEN
ok 1933 - R1 TICKLER beats older ROTTEN
  ---
  duration_ms: 0.405284
  ...
# Subtest: R2 tickler orders by due date then path and line
ok 1934 - R2 tickler orders by due date then path and line
  ---
  duration_ms: 0.762876
  ...
# Subtest: missing created sorts after dated peers
ok 1935 - missing created sorts after dated peers
  ---
  duration_ms: 13.66597
  ...
# Subtest: B1 upkeep counts outside the lanes
ok 1936 - B1 upkeep counts outside the lanes
  ---
  duration_ms: 15.676159
  ...
# Subtest: review model meter uses upkeep and exposes refreshed
ok 1937 - review model meter uses upkeep and exposes refreshed
  ---
  duration_ms: 0.514582
  ...
# Subtest: RC1 arrived: past scheduled walks RECURRING with lane and null state
ok 1938 - RC1 arrived: past scheduled walks RECURRING with lane and null state
  ---
  duration_ms: 6.570043
  ...
# Subtest: RC2 arrives today: due today with zero days overdue
ok 1939 - RC2 arrives today: due today with zero days overdue
  ---
  duration_ms: 14.666462
  ...
# Subtest: RC3 not yet: future scheduled walks nowhere
ok 1940 - RC3 not yet: future scheduled walks nowhere
  ---
  duration_ms: 0.590698
  ...
# Subtest: RC4 due only, past: the due date is the occurrence
ok 1941 - RC4 due only, past: the due date is the occurrence
  ---
  duration_ms: 0.689466
  ...
# Subtest: RC5 due only, future: walks nowhere
ok 1942 - RC5 due only, future: walks nowhere
  ---
  duration_ms: 0.393301
  ...
# Subtest: RC6 earliest date wins across start and due
ok 1943 - RC6 earliest date wins across start and due
  ---
  duration_ms: 0.385426
  ...
# Subtest: RC7 undated: no occurrence, no tier
ok 1944 - RC7 undated: no occurrence, no tier
  ---
  duration_ms: 0.427175
  ...
# Subtest: RC8 lanes: recurring lane rows keep their lane with null state
ok 1945 - RC8 lanes: recurring lane rows keep their lane with null state
  ---
  duration_ms: 0.628641
  ...
# Subtest: RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
ok 1946 - RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
  ---
  duration_ms: 18.996667
  ...
# Subtest: RC10 checklist wins: a recurring chore stays in its checklist tier
ok 1947 - RC10 checklist wins: a recurring chore stays in its checklist tier
  ---
  duration_ms: 0.690217
  ...
# Subtest: RC11 a stray stamp is ignored: recurring with null state
ok 1948 - RC11 a stray stamp is ignored: recurring with null state
  ---
  duration_ms: 0.532888
  ...
# Subtest: RC12 order and counts: due_on, then path, then line; recurring adds no due
ok 1949 - RC12 order and counts: due_on, then path, then line; recurring adds no due
  ---
  duration_ms: 18.333373
  ...
# Subtest: recurring rows adapt due and start from Tasks fields and inline fallbacks
ok 1950 - recurring rows adapt due and start from Tasks fields and inline fallbacks
  ---
  duration_ms: 1.735704
  ...
# Subtest: status view counts RECURRING as a due commitment tier
ok 1951 - status view counts RECURRING as a due commitment tier
  ---
  duration_ms: 19.678179
  ...
# Subtest: footer groups, entry view, and legend cover RECURRING
ok 1952 - footer groups, entry view, and legend cover RECURRING
  ---
  duration_ms: 2.782483
  ...
# Subtest: a stale-stamped recurring row marks due with the resolve hint
ok 1953 - a stale-stamped recurring row marks due with the resolve hint
  ---
  duration_ms: 1.454868
  ...
# Subtest: freshness namespace v14 keeps recurring and removes reference capabilities
ok 1954 - freshness namespace v14 keeps recurring and removes reference capabilities
  ---
  duration_ms: 277.440273
  ...
# Subtest: hidden recurring ^ref keeps ordinary visibility (Rust parity)
ok 1955 - hidden recurring ^ref keeps ordinary visibility (Rust parity)
  ---
  duration_ms: 1.449337
  ...
# Subtest: bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
ok 1956 - bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
  ---
  duration_ms: 12.484805
  ...
# Subtest: day numbers stay calendar-local across a DST boundary
ok 1957 - day numbers stay calendar-local across a DST boundary
  ---
  duration_ms: 0.426525
  ...
# Subtest: reviewModel shares counts, meter, tooltip, and severity
ok 1958 - reviewModel shares counts, meter, tooltip, and severity
  ---
  duration_ms: 0.669398
  ...
# Subtest: memo serves warm map hits and misses use the per-row evaluator
ok 1959 - memo serves warm map hits and misses use the per-row evaluator
  ---
  duration_ms: 105.936803
  ...
# Subtest: config snapshot caches the parse and invalidates explicitly
ok 1960 - config snapshot caches the parse and invalidates explicitly
  ---
  duration_ms: 69.256643
  ...
# Subtest: review chips share the model with severity classes
ok 1961 - review chips share the model with severity classes
  ---
  duration_ms: 1.71275
  ...
# Subtest: warm lookups reuse one snapshot without re-reading config
ok 1962 - warm lookups reuse one snapshot without re-reading config
  ---
  duration_ms: 76.507406
  ...
# Subtest: same-array cache updates and Today changes rebuild the memo
ok 1963 - same-array cache updates and Today changes rebuild the memo
  ---
  duration_ms: 111.58239
  ...
# Subtest: duplicate block IDs keep each row's own classification
ok 1964 - duplicate block IDs keep each row's own classification
  ---
  duration_ms: 110.024076
  ...
# Subtest: line identity separates same-path rows without block IDs
ok 1965 - line identity separates same-path rows without block IDs
  ---
  duration_ms: 92.963924
  ...
# Subtest: interval lookup serves the cached interval with one memo acquisition
ok 1966 - interval lookup serves the cached interval with one memo acquisition
  ---
  duration_ms: 93.644755
  ...
# Subtest: SC stage config vectors normalize valid lists and isolate rejected lists
ok 1967 - SC stage config vectors normalize valid lists and isolate rejected lists
  ---
  duration_ms: 9.168917
  ...
# Subtest: CS stage queue vectors resolve tags and sort staged checklist rows
ok 1968 - CS stage queue vectors resolve tags and sort staged checklist rows
  ---
  duration_ms: 6.06553
  ...
# Subtest: stage names are rendered in footer details and counts compact before labels
ok 1969 - stage names are rendered in footer details and counts compact before labels
  ---
  duration_ms: 0.622448
  ...
# Subtest: FT1-FT6 footer details preserve tier semantics, stage color, and compact counts
ok 1970 - FT1-FT6 footer details preserve tier semantics, stage color, and compact counts
  ---
  duration_ms: 4.477187
  ...
# Subtest: invalid stage lists emit one config lint without invalidating freshness
ok 1971 - invalid stage lists emit one config lint without invalidating freshness
  ---
  duration_ms: 81.14499
  ...
# Subtest: namespace v14 exposes normalized stage config and queue fields from Tasks rows
ok 1972 - namespace v14 exposes normalized stage config and queue fields from Tasks rows
  ---
  duration_ms: 149.249855
  ...
# Subtest: S1 new through S4 overdue
ok 1973 - S1 new through S4 overdue
  ---
  duration_ms: 8.554061
  ...
# Subtest: S5 task beats note, S6 note beats config, S7 config
ok 1974 - S5 task beats note, S6 note beats config, S7 config
  ---
  duration_ms: 1.209099
  ...
# Subtest: S8 invalid overrides fall through with lints
ok 1975 - S8 invalid overrides fall through with lints
  ---
  duration_ms: 1.062178
  ...
# Subtest: S9 malformed and S10 future stamps read as new
ok 1976 - S9 malformed and S10 future stamps read as new
  ---
  duration_ms: 0.343997
  ...
# Subtest: S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
ok 1977 - S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
  ---
  duration_ms: 0.549629
  ...
# Subtest: S13 out-of-scope rows read null
ok 1978 - S13 out-of-scope rows read null
  ---
  duration_ms: 0.595026
  ...
# Subtest: S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
ok 1979 - S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
  ---
  duration_ms: 2.845603
  ...
# Subtest: S15 counts (updated): upkeep outside the lanes drives the budget
ok 1980 - S15 counts (updated): upkeep outside the lanes drives the budget
  ---
  duration_ms: 1.880701
  ...
# Subtest: config coercion keeps defaults, flags invalid, ignores unknown keys
ok 1981 - config coercion keeps defaults, flags invalid, ignores unknown keys
  ---
  duration_ms: 2.418767
  ...
# Subtest: loadFreshnessConfig reads the block with plan-style injectables
ok 1982 - loadFreshnessConfig reads the block with plan-style injectables
  ---
  duration_ms: 1.282428
  ...
# Subtest: interval precedence is task, note, config, default
ok 1983 - interval precedence is task, note, config, default
  ---
  duration_ms: 0.864491
  ...
# Subtest: intervalForLine covers every source with its Ready fallback
ok 1984 - intervalForLine covers every source with its Ready fallback
  ---
  duration_ms: 0.781352
  ...
# Subtest: project tracking stays special while reference tasks use ordinary Ready freshness
ok 1985 - project tracking stays special while reference tasks use ordinary Ready freshness
  ---
  duration_ms: 8.492874
  ...
# Subtest: reference tasks match ordinary interval precedence and lane behavior
ok 1986 - reference tasks match ordinary interval precedence and lane behavior
  ---
  duration_ms: 3.071955
  ...
# Subtest: obsolete reference interval keys are ignored and project config still validates
ok 1987 - obsolete reference interval keys are ignored and project config still validates
  ---
  duration_ms: 1.677102
  ...
# Subtest: references use ordinary keep decisions and the nine-tier queue shape
ok 1988 - references use ordinary keep decisions and the nine-tier queue shape
  ---
  duration_ms: 1.900117
  ...
# Subtest: CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
ok 1989 - CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
  ---
  duration_ms: 4.032269
  ...
# Subtest: CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
ok 1990 - CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
  ---
  duration_ms: 2.759117
  ...
# Subtest: freshness namespace v14 retains the tracker capability contract
ok 1991 - freshness namespace v14 retains the tracker capability contract
  ---
  duration_ms: 121.825486
  ...
# Subtest: UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
ok 1992 - UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
  ---
  duration_ms: 3.620823
  ...
# Subtest: UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
ok 1993 - UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
  ---
  duration_ms: 0.589475
  ...
# Subtest: UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
ok 1994 - UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
  ---
  duration_ms: 0.433849
  ...
# Subtest: UB11 scheduled wins a tie with the unblock date
ok 1995 - UB11 scheduled wins a tie with the unblock date
  ---
  duration_ms: 0.484565
  ...
# Subtest: unblocked reader takes the latest valid duplicate and reports malformed values
ok 1996 - unblocked reader takes the latest valid duplicate and reports malformed values
  ---
  duration_ms: 0.357152
  ...
# Subtest: UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
ok 1997 - UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
  ---
  duration_ms: 0.626656
  ...
# Subtest: UB14 TICKLERs with the same due date sort only by path and line
ok 1998 - UB14 TICKLERs with the same due date sort only by path and line
  ---
  duration_ms: 2.013023
  ...
# Subtest: UB15 a scheduled ^prj resurfaces in PROJECTS
ok 1999 - UB15 a scheduled ^prj resurfaces in PROJECTS
  ---
  duration_ms: 0.275797
  ...

