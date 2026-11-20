# Chat History - ace-run (bob-cli-nh.7.1.1--mon-0)

- **TIMESTAMP:** 2026-11-19 23:32:16 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-nh.7.1.1--mon-0

## Prompt

sase monitor start --command 'npm test && npm run validate && bob plugins sync --repo "$PWD" --no-pull --dry-run -p bob-ledger-tools && bob plugins sync --repo "$PWD" --no-pull -p bob-ledger-tools' --reason 'Run full bob-plugins validation and sync the intention card'

## Response

sase tool run 4e9343cd2952fc4ce94a75a613d23375

> bob-plugins@0.1.0 test
> node scripts/build-plugins.mjs --check && npm run docs:inventory:check && { npm run test:unit; u=$?; npm run test:perf; p=$?; exit $((u||p)); }

  checked   block-id-prompt
  checked   bob-articles
  checked   bob-command-mode
  checked   bob-copy-chips
  checked   bob-emoji
  checked   bob-ledger-tools
  checked   bob-mail
  checked   bob-navigation-hotkeys
  checked   task-status-cycler

> bob-plugins@0.1.0 docs:inventory:check
> node scripts/docs-inventory.mjs --check

Plugin documentation inventory is up to date.

> bob-plugins@0.1.0 test:unit
> node --test scripts/test-navigation-leaf-switch-guard.cjs scripts/test-project-tasks-snapshot.cjs scripts/test-bob-articles.cjs scripts/test-command-mode-resolver-env.cjs scripts/test-command-mode-catalog.cjs scripts/test-command-mode-runner.cjs scripts/test-command-mode-outcomes-api.cjs scripts/test-command-mode-pager.cjs scripts/test-command-mode-args-vim.cjs scripts/test-command-mode-sheet.cjs scripts/test-command-mode-album-schema-surface.cjs scripts/test-command-mode-sheet-keys.cjs scripts/test-command-mode-sheet-sequence.cjs scripts/test-command-mode-sheet-sequence-dom.cjs scripts/test-command-mode-status-chip.cjs scripts/test-command-mode-sequence-engine.cjs scripts/test-command-mode-sequence-feedback.cjs scripts/test-navigation-hotkeys-section-nav.cjs scripts/test-navigation-hotkeys-rename.cjs scripts/test-navigation-delete-guard.cjs scripts/test-navigation-copy-card-model.cjs scripts/test-navigation-copy-card-view.cjs scripts/test-navigation-hotkeys-ref-pdf.cjs scripts/test-navigation-hotkeys-ref-pdf-page.cjs scripts/test-navigation-ref-annotation-locator.cjs scripts/test-navigation-highlights-notice.cjs scripts/test-navigation-highlights-hints.cjs scripts/test-navigation-hotkeys-templater-trigger.cjs scripts/test-navigation-hotkeys-schedule-recovery.cjs scripts/test-navigation-hotkeys-schedule-properties.cjs scripts/test-navigation-hotkeys-schedule-writes.cjs scripts/test-navigation-hotkeys-runtime-schedule.cjs scripts/test-navigation-hotkeys-dependencies.cjs scripts/test-navigation-blocks-guards.cjs scripts/test-navigation-blocks-writers.cjs scripts/test-navigation-blocks-edit.cjs scripts/test-navigation-blocks-stage-view.cjs scripts/test-navigation-hotkeys-dependency-mirror.cjs scripts/test-navigation-hotkeys-task-move-plan.cjs scripts/test-navigation-hotkeys-priority-notice.cjs scripts/test-navigation-successor-picker.cjs scripts/test-navigation-successor-verdicts.cjs scripts/test-navigation-image-zoom-viewer.cjs scripts/test-navigation-video-zoom-viewer.cjs scripts/test-navigation-image-zoom-origin.cjs scripts/test-navigation-image-zoom-path.cjs scripts/test-navigation-hotkeys-unblocked-notice.cjs scripts/test-navigation-hotkeys-offer-close-apis.cjs scripts/test-navigation-project-blocking.cjs scripts/test-navigation-project-dependency-stage.cjs scripts/test-navigation-project-subprojects.cjs scripts/test-navigation-project-subtree-gestures.cjs scripts/test-navigation-hotkeys-priority-picker.cjs scripts/test-navigation-hotkeys-picker-lifecycle.cjs scripts/test-navigation-hotkeys-ref-picker-text.cjs scripts/test-navigation-hotkeys-pomodoro-move-pickers.cjs scripts/test-navigation-inbox-route.cjs scripts/test-navigation-inbox-route-card.cjs scripts/test-navigation-hotkeys-task-move.cjs scripts/test-navigation-open-notes-uri.cjs scripts/test-navigation-parent-change.cjs scripts/test-navigation-parent-album-record.cjs scripts/test-navigation-album-schema-fallback.cjs scripts/test-navigation-hotkeys-dash-open.cjs scripts/test-navigation-goto-task-uri.cjs scripts/test-navigation-hotkeys-open-task-jump.cjs scripts/test-navigation-hotkeys-vim-counts.cjs scripts/test-navigation-hotkeys-tab-pin.cjs scripts/test-navigation-hotkeys-schedule-log.cjs scripts/test-navigation-hotkeys-schedule-review.cjs scripts/test-navigation-hotkeys-deferred-pomodoro.cjs scripts/test-navigation-hotkeys-pomodoro-parse.cjs scripts/test-navigation-hotkeys-pomodoro-bullet-move.cjs scripts/test-navigation-hotkeys-pomodoro-split-rename.cjs scripts/test-navigation-hotkeys-pomodoro-split.cjs scripts/test-navigation-hotkeys-pomodoro-themes-manager.cjs scripts/test-navigation-hotkeys-pomodoro-reorder.cjs scripts/test-navigation-hotkeys-runtime-prune.cjs scripts/test-navigation-hotkeys-project-from-task.cjs scripts/test-navigation-hotkeys-project-reversal.cjs scripts/test-navigation-hotkeys-link-picker.cjs scripts/test-navigation-hotkeys-lane-toggle.cjs scripts/test-navigation-hotkeys-task-link-lane.cjs scripts/test-navigation-hotkeys-cancel-log.cjs scripts/test-navigation-hotkeys-cancel-task.cjs scripts/test-navigation-hotkeys-forward-promotion.cjs scripts/test-navigation-hotkeys-promotion-verdicts.cjs scripts/test-navigation-hotkeys-schedule-work-log.cjs scripts/test-navigation-hotkeys-work-log-stamp-closeout.cjs scripts/test-navigation-hotkeys-task-move-history.cjs scripts/test-navigation-jump-history.cjs scripts/test-navigation-dependencies.cjs scripts/test-navigation-editor-line-diff.cjs scripts/test-navigation-quick-roll.cjs scripts/test-navigation-quick-roll-preview.cjs scripts/test-navigation-roll-decay.cjs scripts/test-navigation-decay-planner.cjs scripts/test-navigation-task-card-model.cjs scripts/test-navigation-task-card-view.cjs scripts/test-navigation-task-card-theme-edit.cjs scripts/test-navigation-task-card-schedule.cjs scripts/test-navigation-task-card-review.cjs scripts/test-navigation-decision-card.cjs scripts/test-navigation-decision-card-handlers.cjs scripts/test-navigation-decision-card-keep.cjs scripts/test-navigation-refresh-modal.cjs scripts/test-navigation-freshness.cjs scripts/test-navigation-review-groups.cjs scripts/test-navigation-stamps.cjs scripts/test-navigation-keep-counting.cjs scripts/test-navigation-rotten-keep.cjs scripts/test-navigation-rotten-log.cjs scripts/test-navigation-checklist.cjs scripts/test-navigation-review-advance.cjs scripts/test-navigation-review-advance-gestures.cjs scripts/test-navigation-checklist-ctrl-enter.cjs scripts/test-ledger-tools-navigation.cjs scripts/test-ledger-tools-plan-budget.cjs scripts/test-ledger-tools-plan-budget-off-clock.cjs scripts/test-ledger-tools-plan-today-roots.cjs scripts/test-ledger-tools-ready-badge.cjs scripts/test-ledger-tools-note-ready.cjs scripts/test-ledger-tools-note-ready-views.cjs scripts/test-ledger-tools-dashboard-parity.cjs scripts/test-ledger-tools-work-badge-tone.cjs scripts/test-ledger-tools-dashboard-collections.cjs scripts/test-ledger-tools-today.cjs scripts/test-ledger-tools-period-notes.cjs scripts/test-ledger-tools-gcal-events.cjs scripts/test-ledger-tools-event-link-times.cjs scripts/test-ledger-tools-meet-event-run.cjs scripts/test-ledger-tools-pomodoro-clock.cjs scripts/test-ledger-tools-freshness-placement.cjs scripts/test-ledger-tools-freshness-states.cjs scripts/test-ledger-tools-freshness-namespace.cjs scripts/test-ledger-tools-freshness-review-model.cjs scripts/test-ledger-tools-freshness-queue.cjs scripts/test-ledger-tools-freshness-stages.cjs scripts/test-ledger-tools-freshness-tracking.cjs scripts/test-ledger-tools-freshness-footer.cjs scripts/test-ledger-tools-walker-footer.cjs scripts/test-ledger-tools-walk-attention-vectors.cjs scripts/test-ledger-tools-keep-inbox.cjs scripts/test-ledger-tools-freshness-recurring.cjs scripts/test-ledger-tools-freshness-mark.cjs scripts/test-ledger-tools-freshness-mark-surfaces.cjs scripts/test-ledger-tools-priority-marks.cjs scripts/test-ledger-tools-block-marks.cjs scripts/test-ledger-tools-block-marks-contrast.cjs scripts/test-ledger-tools-block-marks-editor.cjs scripts/test-ledger-tools-block-marks-reading.cjs scripts/test-ledger-tools-mail-link-marks.cjs scripts/test-ledger-tools-no-reply-pills.cjs scripts/test-ledger-tools-task-tag-marks.cjs scripts/test-ledger-tools-task-link-marks.cjs scripts/test-ledger-tools-task-link-marks-live.cjs scripts/test-ledger-tools-task-link-marks-reading.cjs scripts/test-ledger-tools-task-type-identity.cjs scripts/test-ledger-tools-today-marks.cjs scripts/test-ledger-tools-today-marks-reading.cjs scripts/test-ledger-tools-unblocked-glyph.cjs scripts/test-ledger-tools-frees-marks.cjs scripts/test-ledger-tools-off-clock-link-chips.cjs scripts/test-ledger-tools-progress-marks.cjs scripts/test-ledger-tools-keep-moving-marks.cjs scripts/test-ledger-tools-keep-moving-render.cjs scripts/test-ledger-tools-keep-moving-marks-surface.cjs scripts/test-ledger-tools-date-marks.cjs scripts/test-ledger-tools-recurrence-marks.cjs scripts/test-ledger-tools-date-marks-tasks.cjs scripts/test-ledger-tools-freshness-keeps.cjs scripts/test-ledger-tools-freshness-unblocked.cjs scripts/test-ledger-tools-freshness-decision-card.cjs scripts/test-ledger-tools-dependency-chips.cjs scripts/test-ledger-tools-blocks-chips.cjs scripts/test-ledger-tools-command-mode-refresh.cjs scripts/test-ledger-tools-snippets.cjs scripts/test-ledger-tools-vim-mappings.cjs scripts/test-task-status-cycler-dependencies.cjs scripts/test-task-status-cycler-blocks-guards.cjs scripts/test-task-status-cycler-complete-vectors.cjs scripts/test-task-status-cycler-bank-guard.cjs scripts/test-task-status-cycler-ctrl-enter.cjs scripts/test-task-status-cycler-event-task-close.cjs scripts/test-task-status-cycler-reference-lifecycle.cjs scripts/test-task-status-cycler-pomodoro-completion.cjs scripts/test-task-status-cycler-pomodoro-clock.cjs scripts/test-task-status-cycler-pomodoro-work-log.cjs scripts/test-task-status-cycler-pomodoro-reopen.cjs scripts/test-task-status-cycler-blocked-schedule.cjs scripts/test-task-status-cycler-demotion-picker.cjs scripts/test-task-status-cycler-event-ledger-guard.cjs scripts/test-task-status-cycler-promotion.cjs scripts/test-task-status-cycler-promotion-verdicts.cjs scripts/test-task-status-cycler-counted-toggle.cjs scripts/test-task-status-cycler-successors.cjs scripts/test-task-status-cycler-successor-wiring.cjs scripts/test-task-status-cycler-successor-polish.cjs scripts/test-task-status-cycler-keep-moving.cjs scripts/test-keep-moving-marks-parity.cjs scripts/test-task-status-cycler-relation-successors.cjs scripts/test-task-status-cycler-parked-successors.cjs scripts/test-task-status-cycler-successor-offers.cjs scripts/test-task-status-cycler-successor-verdicts.cjs scripts/test-task-status-cycler-successor-apply.cjs scripts/test-task-status-cycler-successor-theme-write.cjs scripts/test-task-status-cycler-project-catalog.cjs scripts/test-task-status-cycler-project-pull-in.cjs scripts/test-task-status-cycler-task-links-api.cjs scripts/test-task-status-cycler-closed-pomodoro-links.cjs scripts/test-task-status-cycler-task-link-lane.cjs scripts/test-task-status-cycler-freshness.cjs scripts/test-block-id-prompt-dependencies.cjs scripts/test-block-id-prompt-blocks-guards.cjs scripts/test-block-id-prompt-ref-picker-text.cjs scripts/test-block-id-prompt-markers.cjs scripts/test-block-id-prompt-pomodoro-context.cjs scripts/test-block-id-prompt-target-update.cjs scripts/test-block-id-prompt-pomodoro-insertion.cjs scripts/test-block-id-prompt-pomodoro-targets.cjs scripts/test-block-id-prompt-pomodoro-picker-view.cjs scripts/test-block-id-prompt-pomodoro-picker-runtime.cjs scripts/test-block-id-prompt-work-log.cjs scripts/test-block-id-prompt-pomodoro-link-runtime.cjs scripts/test-block-id-prompt-pomodoro-theme-write.cjs scripts/test-block-id-prompt-pomodoro-link-picker-api.cjs scripts/test-block-id-prompt-pomodoro-unlink-runtime.cjs scripts/test-block-id-prompt-parked-successors.cjs scripts/test-block-id-prompt-task-link-deletion.cjs scripts/test-block-id-prompt-task-wikilink-model.cjs scripts/test-block-id-prompt-task-wikilink-token.cjs scripts/test-block-id-prompt-task-wikilink-index.cjs scripts/test-block-id-prompt-task-wikilink-picker-view.cjs scripts/test-block-id-prompt-task-wikilink-picker-runtime.cjs scripts/test-block-id-prompt-task-wikilink-naming.cjs scripts/test-block-id-prompt-task-wikilink-pomodoro.cjs scripts/test-block-id-prompt-plan-budget-and-freshness.cjs scripts/test-prompt-block-id-naming.cjs scripts/test-block-id-prompt-prefill.cjs scripts/test-block-id-prompt-rename-atomic.cjs scripts/test-vim-surround.cjs scripts/test-vim-yank-flash.cjs scripts/test-navigation-dependencies-stage-ranker-and-pool.cjs scripts/test-navigation-dependencies-stage-entry-and-view.cjs scripts/test-navigation-dependencies-stage-writes.cjs scripts/test-navigation-dependencies-stage-mirror-and-badge.cjs scripts/test-navigation-dependencies-stage-stale-guards.cjs scripts/test-navigation-dependencies-stage-performance.cjs scripts/test-navigation-prompt-block-id-stage.cjs scripts/test-navigation-dependencies-writer.cjs scripts/test-navigation-dependency-link-consumption.cjs scripts/test-plugin-build.cjs scripts/test-ledger-tools-stats-journal.cjs scripts/test-ledger-tools-stats-clocks.cjs scripts/test-ledger-tools-stats-data.cjs scripts/test-ledger-tools-stats-block.cjs scripts/test-ledger-tools-stats-charts.cjs scripts/test-ledger-tools-stats-clock-charts.cjs scripts/test-navigation-review-journal.cjs scripts/test-ledger-tools-stats-panels.cjs scripts/test-ledger-tools-stats-lanes.cjs scripts/test-ledger-tools-reading-board-data.cjs scripts/test-ledger-tools-notebooks-data.cjs scripts/test-ledger-tools-albums-data.cjs scripts/test-ledger-tools-areas-data.cjs scripts/test-ledger-tools-areas-catalog.cjs scripts/test-ledger-tools-projects-data.cjs scripts/test-ledger-tools-projects-catalog.cjs scripts/test-ledger-tools-album-update.cjs scripts/test-ledger-tools-bank-config-update.cjs scripts/test-ledger-tools-bank-decode.cjs scripts/test-ledger-tools-bank-period-model.cjs scripts/test-ledger-tools-bank-period-paint.cjs scripts/test-ledger-tools-bank-period-balance.cjs scripts/test-ledger-tools-bank-source.cjs scripts/test-ledger-tools-bank-data.cjs scripts/test-ledger-tools-bank-actions.cjs scripts/test-ledger-tools-bank-category-card.cjs scripts/test-ledger-tools-bank-walk.cjs scripts/test-ledger-tools-bank-walk-index.cjs scripts/test-ledger-tools-bank-category-card-ui.cjs scripts/test-ledger-tools-bank-emoji-slot.cjs scripts/test-ledger-tools-notebook-catalog.cjs scripts/test-ledger-tools-notebook-header.cjs scripts/test-ledger-tools-reading-board-models.cjs scripts/test-ledger-tools-reading-board-block.cjs scripts/test-ledger-tools-pomodoro-home-chips.cjs scripts/test-ledger-tools-pomodoro-themes.cjs scripts/test-ledger-tools-task-theme-marks.cjs scripts/test-ledger-tools-task-theme-rendered.cjs scripts/test-navigation-image-zoom-target.cjs scripts/test-navigation-image-zoom-command.cjs scripts/test-done-archive-path.cjs scripts/test-navigation-relation-lines.cjs scripts/test-navigation-relation-mentions.cjs scripts/test-navigation-relation-writer.cjs scripts/test-navigation-task-cancel-vectors.cjs scripts/test-navigation-task-split-vectors.cjs scripts/test-navigation-window-tab-numbers.cjs scripts/test-navigation-window-tab-model.cjs scripts/test-navigation-window-tab-actions.cjs scripts/test-navigation-window-prefix-model.cjs scripts/test-navigation-window-prefix-actions.cjs scripts/test-navigation-window-hint-view.cjs scripts/test-navigation-window-prefix-commands.cjs scripts/test-navigation-window-prefix.cjs scripts/test-navigation-task-split-gesture.cjs scripts/test-navigation-relation-cancel-writer.cjs scripts/test-navigation-relation-complete-writer.cjs scripts/test-navigation-relation-complete-vectors.cjs scripts/test-navigation-relation-links-stage.cjs scripts/test-navigation-relation-merge.cjs scripts/test-navigation-relation-successor-vectors.cjs scripts/test-navigation-relation-stage-render.cjs scripts/test-relation-index-linked-from-stage.cjs scripts/test-ledger-tools-relations.cjs scripts/test-ledger-tools-task-merge.cjs scripts/test-ledger-tools-notebooks-api.cjs scripts/test-navigation-notebook-gestures.cjs scripts/test-ledger-tools-relation-index.cjs scripts/test-ledger-tools-attachments-api.cjs scripts/test-ledger-tools-relation-mentions.cjs scripts/test-ledger-tools-relation-chips.cjs scripts/test-task-status-cycler-relations.cjs scripts/test-task-status-cycler-restore.cjs scripts/test-block-id-prompt-relations.cjs scripts/test-ledger-tools-day-strip.cjs scripts/test-ledger-tools-day-strip-themes.cjs scripts/test-ledger-tools-day-strip-plan-host.cjs scripts/test-ledger-tools-period-strip.cjs scripts/test-ledger-tools-period-strip-charts.cjs scripts/test-ledger-tools-period-parts.cjs scripts/test-ledger-tools-fakenode-inspect.cjs scripts/test-ledger-tools-day-strip-lanes.cjs scripts/test-ledger-tools-day-strip-hosts.cjs scripts/test-obsidian-startup-smoke.cjs scripts/test-obsidian-bank-ui-e2e.cjs scripts/test-obsidian-bank-ui-e2e-setup.cjs scripts/test-obsidian-album-ui-e2e.cjs scripts/test-obsidian-album-schema-writer-e2e.cjs scripts/test-obsidian-record-writer-e2e.cjs scripts/test-obsidian-record-walk-e2e.cjs scripts/test-obsidian-notebook-ui-e2e.cjs scripts/test-obsidian-projects-ui-e2e.cjs scripts/test-obsidian-record-card-e2e.cjs scripts/test-obsidian-task-wikilink-e2e.cjs scripts/test-obsidian-block-id-rename-e2e.cjs scripts/test-obsidian-task-link-marks-e2e.cjs scripts/test-obsidian-block-marks-e2e.cjs scripts/test-obsidian-frees-marks-e2e.cjs scripts/test-obsidian-keep-moving-marks-e2e.cjs scripts/test-obsidian-off-clock-link-chips-e2e.cjs scripts/test-obsidian-event-link-times-e2e.cjs scripts/test-obsidian-decay-ladder-e2e.cjs scripts/test-obsidian-quick-roll-e2e.cjs scripts/test-task-link-marks-motion.cjs scripts/test-ledger-tools-lane-walk.cjs scripts/test-navigation-bank-walk.cjs scripts/test-navigation-lane-walk.cjs scripts/test-ledger-tools-root-marks.cjs scripts/test-navigation-bracket-repeat.cjs scripts/test-navigation-period-links.cjs scripts/test-navigation-bracket-mode-indicator.cjs scripts/test-navigation-lane-inbox-route.cjs scripts/test-navigation-review-due-row.cjs scripts/test-bob-mail.cjs scripts/test-bob-mail-compose.cjs scripts/test-bob-mail-archive-banner.cjs scripts/test-navigation-reload-history.cjs scripts/test-obsidian-video-zoom-e2e.cjs scripts/test-obsidian-redo-history-e2e.cjs scripts/test-obsidian-closed-pomodoro-link-e2e.cjs scripts/test-obsidian-command-mode-tab-e2e.cjs scripts/test-obsidian-walker-footer-e2e.cjs scripts/test-obsidian-vim-yank-flash-e2e.cjs scripts/test-obsidian-copy-card-e2e.cjs scripts/test-obsidian-window-prefix-e2e.cjs scripts/test-ledger-tools-bank-cards.cjs scripts/test-ledger-tools-bank-badge-hosts.cjs scripts/test-ledger-tools-bank-setup.cjs scripts/test-ledger-tools-bank-setup-group-jump.cjs scripts/test-ledger-tools-bank-setup-arrange.cjs scripts/test-ledger-tools-schema-arrange.cjs scripts/test-ledger-tools-bank-marks.cjs scripts/test-ledger-tools-bank-subscription.cjs scripts/test-ledger-tools-bank-subscription-surfaces.cjs scripts/test-ledger-tools-bank-subscription-linker.cjs scripts/test-ledger-tools-album-catalog.cjs scripts/test-ledger-tools-album-records.cjs scripts/test-ledger-tools-album-header.cjs scripts/test-ledger-tools-record-sheet.cjs scripts/test-ledger-tools-record-walk.cjs scripts/test-ledger-tools-record-update.cjs scripts/test-ledger-tools-record-card.cjs scripts/test-ledger-tools-record-card-stages.cjs scripts/test-ledger-tools-album-schema-card-shell.cjs scripts/test-ledger-tools-album-schema-arrange-card.cjs scripts/test-ledger-tools-album-schema-field-jump.cjs scripts/test-ledger-tools-album-schema-place-drag.cjs scripts/test-ledger-tools-album-entrypoints.cjs scripts/test-ledger-tools-schema-double-equals.cjs scripts/test-ledger-tools-intention-card.cjs scripts/test-ledger-tools-property-card-ownership.cjs scripts/test-ledger-tools-property-card-host.cjs scripts/test-ledger-tools-album-yaml-excursion.cjs scripts/test-bob-emoji-model.cjs scripts/test-bob-emoji-trigger.cjs scripts/test-bob-emoji-suggest.cjs scripts/test-bob-emoji-catalog.cjs scripts/test-bob-emoji-api.cjs scripts/test-copy-chips-grammar.cjs scripts/test-copy-chips-roundtrip.cjs scripts/test-copy-chips-cursor-api.cjs scripts/test-copy-chips-feedback-dom.cjs scripts/test-copy-chips-live-preview.cjs scripts/test-copy-chips-reading.cjs scripts/test-copy-chips-fence.cjs scripts/test-copy-chips-author-model.cjs scripts/test-copy-chips-author-modal.cjs scripts/test-obsidian-copy-chips-e2e.cjs scripts/test-ledger-tools-bank-period-hosts.cjs scripts/test-command-mode-bank-setup-surface.cjs scripts/test-command-mode-record-surface.cjs scripts/test-record-card-vault-coverage.cjs scripts/test-navigation-log-recall.cjs scripts/test-ledger-tools-log-history.cjs

TAP version 13
# Subtest: bip BK1–BK12 accept and empty
ok 1 - bip BK1–BK12 accept and empty
  ---
  duration_ms: 1.102375
  ...
# Subtest: bip BK13–BK15 malformed split mirrors the Depends-On twin
ok 2 - bip BK13–BK15 malformed split mirrors the Depends-On twin
  ---
  duration_ms: 0.36619
  ...
# Subtest: bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
ok 3 - bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
  ---
  duration_ms: 0.110992
  ...
# Subtest: bip MC1/MC2 Pomodoro scanners skip managed lines
ok 4 - bip MC1/MC2 Pomodoro scanners skip managed lines
  ---
  duration_ms: 1.291226
  ...
# Subtest: explicit task IDs exclusively own dependency lookup
ok 5 - explicit task IDs exclusively own dependency lookup
  ---
  duration_ms: 3.763467
  ...
# Subtest: legacy tasks without an id field still fall back to their block ID
ok 6 - legacy tasks without an id field still fall back to their block ID
  ---
  duration_ms: 0.292459
  ...
# Subtest: blocked-link consumption raises open prerequisites and leaves the dependent blocked
ok 7 - blocked-link consumption raises open prerequisites and leaves the dependent blocked
  ---
  duration_ms: 1.018475
  ...
# Subtest: project-blocked member consumption promotes the project's open prerequisite
ok 8 - project-blocked member consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.652707
  ...
# Subtest: project-blocked resident consumption promotes the project's open prerequisite
ok 9 - project-blocked resident consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.366811
  ...
# Subtest: a tagged inherited ^prj target is refused with its parent named
ok 10 - a tagged inherited ^prj target is refused with its parent named
  ---
  duration_ms: 0.348195
  ...
# Subtest: project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
ok 11 - project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
  ---
  duration_ms: 0.689797
  ...
# Subtest: project date refusal applies only when the date is the sole project reason
ok 12 - project date refusal applies only when the date is the sole project reason
  ---
  duration_ms: 0.237343
  ...
# Subtest: a project-blocked tag is token-bounded and ignored on lookalike tags
ok 13 - a project-blocked tag is token-bounded and ignored on lookalike tags
  ---
  duration_ms: 0.363524
  ...
# Subtest: task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
ok 14 - task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
  ---
  duration_ms: 0.627158
  ...
# Subtest: task blocked state unifies status and dependency reasons
ok 15 - task blocked state unifies status and dependency reasons
  ---
  duration_ms: 0.317787
  ...
# Subtest: task picker partition sinks blocked tasks while preserving group order
ok 16 - task picker partition sinks blocked tasks while preserving group order
  ---
  duration_ms: 0.186406
  ...
# Subtest: blocked chip labels show useful unmet dependency counts
ok 17 - blocked chip labels show useful unmet dependency counts
  ---
  duration_ms: 0.096364
  ...
# Subtest: blocked tooltips explain dependency and status-only reasons
ok 18 - blocked tooltips explain dependency and status-only reasons
  ---
  duration_ms: 0.20435
  ...
# Subtest: task status classes cover every open task status
ok 19 - task status classes cover every open task status
  ---
  duration_ms: 0.082267
  ...
# Subtest: Blocked tasks remain unmet dependency targets
ok 20 - Blocked tasks remain unmet dependency targets
  ---
  duration_ms: 0.122133
  ...
# Subtest: blocked task count covers both reasons without double-counting
ok 21 - blocked task count covers both reasons without double-counting
  ---
  duration_ms: 0.105532
  ...
# Subtest: single caret relocation preserves embedding and removes aliases
ok 22 - single caret relocation preserves embedding and removes aliases
  ---
  duration_ms: 1.569136
  ...
# Subtest: single caret relocation resets aliased block links
ok 23 - single caret relocation resets aliased block links
  ---
  duration_ms: 0.242363
  ...
# Subtest: single caret relocation strips heading and block subpaths
ok 24 - single caret relocation strips heading and block subpaths
  ---
  duration_ms: 0.940647
  ...
# Subtest: task picker normalizes every supported wiki block-link form
ok 25 - task picker normalizes every supported wiki block-link form
  ---
  duration_ms: 0.642437
  ...
# Subtest: three or more carets never trigger the task picker
ok 26 - three or more carets never trigger the task picker
  ---
  duration_ms: 0.137132
  ...
# Subtest: rapid aliased task picker completion preserves the alias
ok 27 - rapid aliased task picker completion preserves the alias
  ---
  duration_ms: 2.72786
  ...
# Subtest: task picker recognition is independent of Markdown source context
ok 28 - task picker recognition is independent of Markdown source context
  ---
  duration_ms: 0.736517
  ...
# Subtest: task picker recognition respects cursor proximity and fenced code
ok 29 - task picker recognition respects cursor proximity and fenced code
  ---
  duration_ms: 0.236862
  ...
# Subtest: SA33 settled Unlink task prompt offers parked successors with the removed slot
ok 30 - SA33 settled Unlink task prompt offers parked successors with the removed slot
  ---
  duration_ms: 6.838107
  ...
# Subtest: SA33 Esc on Unlink task offers nothing
ok 31 - SA33 Esc on Unlink task offers nothing
  ---
  duration_ms: 0.428378
  ...
# Subtest: non-Pending unlink stays silent even with a live cycler
ok 32 - non-Pending unlink stays silent even with a live cycler
  ---
  duration_ms: 0.583414
  ...
# Subtest: older cycler api v3 is silence
ok 33 - older cycler api v3 is silence
  ---
  duration_ms: 0.466501
  ...
# Subtest: In Progress unlink with no removed links does not offer
ok 34 - In Progress unlink with no removed links does not offer
  ---
  duration_ms: 0.320132
  ...
# Subtest: Task Link Unlink of a Pending target offers parked successors
ok 35 - Task Link Unlink of a Pending target offers parked successors
  ---
  duration_ms: 2.355447
  ...
# Subtest: plan budget suffix: link Notice appends the meter computed on post-write daily content
ok 36 - plan budget suffix: link Notice appends the meter computed on post-write daily content
  ---
  duration_ms: 7.689033
  ...
# Subtest: plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
ok 37 - plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
  ---
  duration_ms: 0.908715
  ...
# Subtest: plan budget suffix: unlink Notice marks an over-cap plan with 🔴
ok 38 - plan budget suffix: unlink Notice marks an over-cap plan with 🔴
  ---
  duration_ms: 2.062028
  ...
# Subtest: plan budget suffix: Next task without a block ID prompts for one and omits the meter
ok 39 - plan budget suffix: Next task without a block ID prompts for one and omits the meter
  ---
  duration_ms: 0.343316
  ...
# Subtest: plan budget suffix: Task Link Notice appends the meter from post-write daily content
ok 40 - plan budget suffix: Task Link Notice appends the meter from post-write daily content
  ---
  duration_ms: 2.25213
  ...
# Subtest: plan budget suffix: Task Link Notice omits the meter when no daily note takes part
ok 41 - plan budget suffix: Task Link Notice omits the meter when no daily note takes part
  ---
  duration_ms: 0.517639
  ...
# Subtest: planTargetTaskUpdate stamps the rewritten line last via injected stamper
ok 42 - planTargetTaskUpdate stamps the rewritten line last via injected stamper
  ---
  duration_ms: 0.38231
  ...
# Subtest: planTargetTaskUpdate without a stamper never stamps (identity default)
ok 43 - planTargetTaskUpdate without a stamper never stamps (identity default)
  ---
  duration_ms: 0.140609
  ...
# Subtest: planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
ok 44 - planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
  ---
  duration_ms: 0.331573
  ...
# Subtest: planTargetTaskUpdate stamps a Next task that gains a block ID
ok 45 - planTargetTaskUpdate stamps a Next task that gains a block ID
  ---
  duration_ms: 0.525554
  ...
# Subtest: planTargetTaskUpdate tolerates a throwing stamper
ok 46 - planTargetTaskUpdate tolerates a throwing stamper
  ---
  duration_ms: 0.266549
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 47 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.472282
  ...
# Subtest: dedicated-link helpers reject Depends-On lines
ok 48 - dedicated-link helpers reject Depends-On lines
  ---
  duration_ms: 0.330551
  ...
# Subtest: Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
ok 49 - Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
  ---
  duration_ms: 0.384674
  ...
# Subtest: malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
ok 50 - malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
  ---
  duration_ms: 0.119789
  ...
# Subtest: Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
ok 51 - Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
  ---
  duration_ms: 0.262521
  ...
# Subtest: Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
ok 52 - Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
  ---
  duration_ms: 0.205342
  ...
# Subtest: readPlanBudgetMeter ignores stale theme meters and follows links only
ok 53 - readPlanBudgetMeter ignores stale theme meters and follows links only
  ---
  duration_ms: 0.189602
  ...
# Subtest: readPlanBudgetMeter marks an over-link plan red
ok 54 - readPlanBudgetMeter marks an over-link plan red
  ---
  duration_ms: 0.102967
  ...
# Subtest: block-id-prompt freshness accessors degrade without ledger-tools
ok 55 - block-id-prompt freshness accessors degrade without ledger-tools
  ---
  duration_ms: 0.22488
  ...
# Subtest: block-id-prompt refuses Pomodoro ledger lines before calling a stamper
ok 56 - block-id-prompt refuses Pomodoro ledger lines before calling a stamper
  ---
  duration_ms: 0.195824
  ...
# Subtest: list item body bounds trim whitespace and reject empty bullets
ok 57 - list item body bounds trim whitespace and reject empty bullets
  ---
  duration_ms: 2.073569
  ...
# Subtest: Pomodoro activation eligibility requires a sole-content sub-bullet
ok 58 - Pomodoro activation eligibility requires a sole-content sub-bullet
  ---
  duration_ms: 1.993788
  ...
# Subtest: Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
ok 59 - Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
  ---
  duration_ms: 0.270497
  ...
# Subtest: Pomodoro source context distinguishes ledger ancestry and open state
ok 60 - Pomodoro source context distinguishes ledger ancestry and open state
  ---
  duration_ms: 0.469697
  ...
# Subtest: the open-Pomodoro task-link gate recognizes both ^^ and (( sources
ok 61 - the open-Pomodoro task-link gate recognizes both ^^ and (( sources
  ---
  duration_ms: 1.610074
  ...
# Subtest: future cleanup touches only later open Pomodoros and counts duplicates
ok 62 - future cleanup touches only later open Pomodoros and counts duplicates
  ---
  duration_ms: 1.579817
  ...
# Subtest: cleanup resolves aliases, embeds, same-note links, and alternate paths
ok 63 - cleanup resolves aliases, embeds, same-note links, and alternate paths
  ---
  duration_ms: 0.675389
  ...
# Subtest: dedicated bullet subtree cleanup preserves CRLF line endings
ok 64 - dedicated bullet subtree cleanup preserves CRLF line endings
  ---
  duration_ms: 0.296977
  ...
# Subtest: existing-ID task completion prunes future links in the source editor
ok 65 - existing-ID task completion prunes future links in the source editor
  ---
  duration_ms: 2.936808
  ...
# Subtest: new-ID same-file completion plans cleanup after the task edit
ok 66 - new-ID same-file completion plans cleanup after the task edit
  ---
  duration_ms: 1.486228
  ...
# Subtest: findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
ok 67 - findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
  ---
  duration_ms: 2.102145
  ...
# Subtest: findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
ok 68 - findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
  ---
  duration_ms: 0.163773
  ...
# Subtest: findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
ok 69 - findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
  ---
  duration_ms: 0.161478
  ...
# Subtest: todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
ok 70 - todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
  ---
  duration_ms: 0.43466
  ...
# Subtest: todayDailyPath honors a custom Daily Notes format and an empty folder
ok 71 - todayDailyPath honors a custom Daily Notes format and an empty folder
  ---
  duration_ms: 0.214189
  ...
# Subtest: formatDailyDate resolves bracketed literal text alongside date tokens
ok 72 - formatDailyDate resolves bracketed literal text alongside date tokens
  ---
  duration_ms: 0.109799
  ...
# Subtest: getDailyNotesOptions reads the daily-notes core plugin's configured options
ok 73 - getDailyNotesOptions reads the daily-notes core plugin's configured options
  ---
  duration_ms: 0.636976
  ...
# Subtest: computeFencedLineFlags marks opening and closing fence lines and everything between
ok 74 - computeFencedLineFlags marks opening and closing fence lines and everything between
  ---
  duration_ms: 0.233957
  ...
# Subtest: selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
ok 75 - selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
  ---
  duration_ms: 0.692011
  ...
# Subtest: selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
ok 76 - selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
  ---
  duration_ms: 0.44519
  ...
# Subtest: selectPomodoroInsertionTarget rejects more than one open timed entry
ok 77 - selectPomodoroInsertionTarget rejects more than one open timed entry
  ---
  duration_ms: 0.197727
  ...
# Subtest: selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
ok 78 - selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
  ---
  duration_ms: 0.181967
  ...
# Subtest: findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
ok 79 - findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
  ---
  duration_ms: 0.162691
  ...
# Subtest: planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
ok 80 - planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
  ---
  duration_ms: 1.137081
  ...
# Subtest: planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
ok 81 - planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
  ---
  duration_ms: 1.463244
  ...
# Subtest: planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
ok 82 - planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
  ---
  duration_ms: 0.216403
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
ok 83 - planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
  ---
  duration_ms: 0.523389
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
ok 84 - planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
  ---
  duration_ms: 0.561923
  ...
# Subtest: planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
ok 85 - planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
  ---
  duration_ms: 0.323407
  ...
# Subtest: planPomodoroLinkInsertion inserts before the separator preceding later content
ok 86 - planPomodoroLinkInsertion inserts before the separator preceding later content
  ---
  duration_ms: 0.261088
  ...
# Subtest: planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
ok 87 - planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
  ---
  duration_ms: 0.296046
  ...
# Subtest: planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
ok 88 - planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
  ---
  duration_ms: 0.375978
  ...
# Subtest: existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
ok 89 - existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
  ---
  duration_ms: 3.674637
  ...
# Subtest: same-note Pomodoro link runtime composes the task update with adjacent insertion
ok 90 - same-note Pomodoro link runtime composes the task update with adjacent insertion
  ---
  duration_ms: 1.226202
  ...
# Subtest: new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
ok 91 - new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
  ---
  duration_ms: 0.628079
  ...
# Subtest: planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
ok 92 - planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
  ---
  duration_ms: 0.313289
  ...
# Subtest: all-open cleanup removes current and future links while preserving history and unresolved links
ok 93 - all-open cleanup removes current and future links while preserving history and unresolved links
  ---
  duration_ms: 0.893686
  ...
# Subtest: all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
ok 94 - all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
  ---
  duration_ms: 1.098738
  ...
# Subtest: all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
ok 95 - all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
  ---
  duration_ms: 0.228226
  ...
# Subtest: all-open cleanup treats missing section, no open entries, and no matches as no-op successes
ok 96 - all-open cleanup treats missing section, no open entries, and no matches as no-op successes
  ---
  duration_ms: 0.256529
  ...
# Subtest: composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
ok 97 - composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
  ---
  duration_ms: 0.231963
  ...
# Subtest: pomodoro link picker choices normalize to existing/new or null
ok 98 - pomodoro link picker choices normalize to existing/new or null
  ---
  duration_ms: 2.184141
  ...
# Subtest: pomodoroLinkPicker api never rejects and validates choices
ok 99 - pomodoroLinkPicker api never rejects and validates choices
  ---
  duration_ms: 0.404783
  ...
# Subtest: destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
ok 100 - destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
  ---
  duration_ms: 0.640874
  ...
# Subtest: destination pick with a section releases its guards when the modal cannot open
ok 101 - destination pick with a section releases its guards when the modal cannot open
  ---
  duration_ms: 1.747086
  ...
# Subtest: public pick accepts one-based full-note task context and suggests once
ok 102 - public pick accepts one-based full-note task context and suggests once
  ---
  duration_ms: 1.508731
  ...
# Subtest: public pick without task context stays generic; missing themes degrades safely
ok 103 - public pick without task context stays generic; missing themes degrades safely
  ---
  duration_ms: 0.586931
  ...
# Subtest: plugin lifecycle installs the api and drops it on unload
ok 104 - plugin lifecycle installs the api and drops it on unload
  ---
  duration_ms: 0.640864
  ...
# Subtest: task-aware choices retain a valid themeIntent; absent intent keeps the legacy shape
ok 105 - task-aware choices retain a valid themeIntent; absent intent keeps the legacy shape
  ---
  duration_ms: 0.349548
  ...
# Subtest: malformed themeIntent is dropped so it can never enable a write
ok 106 - malformed themeIntent is dropped so it can never enable a write
  ---
  duration_ms: 0.473574
  ...
# Subtest: taskLineTextAt reads one-based lines and degrades to empty
ok 107 - taskLineTextAt reads one-based lines and degrades to empty
  ---
  duration_ms: 0.355308
  ...
# Subtest: public pick tolerates an out-of-range task line and releases its guards
ok 108 - public pick tolerates an out-of-range task line and releases its guards
  ---
  duration_ms: 0.433147
  ...
# Subtest: Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
ok 109 - Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
  ---
  duration_ms: 2.091705
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor requires a single cursor
ok 110 - resolvePomodoroLinkTaskFromEditor requires a single cursor
  ---
  duration_ms: 0.316614
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
ok 111 - resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
  ---
  duration_ms: 0.371539
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
ok 112 - resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
  ---
  duration_ms: 0.46636
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
ok 113 - resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
  ---
  duration_ms: 0.656393
  ...
# Subtest: blocked-link consumption reports dependency reasons before the project date
ok 114 - blocked-link consumption reports dependency reasons before the project date
  ---
  duration_ms: 2.384383
  ...
# Subtest: Pomodoro link checks do not read other notes for a non-Blocked task
ok 115 - Pomodoro link checks do not read other notes for a non-Blocked task
  ---
  duration_ms: 0.301836
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
ok 116 - resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
  ---
  duration_ms: 0.390916
  ...
# Subtest: task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
ok 117 - task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
  ---
  duration_ms: 6.575898
  ...
# Subtest: task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
ok 118 - task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
  ---
  duration_ms: 2.031971
  ...
# Subtest: task-mode toggle: linked only under a completed Pomodoro links again
ok 119 - task-mode toggle: linked only under a completed Pomodoro links again
  ---
  duration_ms: 0.835475
  ...
# Subtest: task-mode toggle: a task without a block ID is never linked and prompts for one
ok 120 - task-mode toggle: a task without a block ID is never linked and prompts for one
  ---
  duration_ms: 0.445079
  ...
# Subtest: existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
ok 121 - existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
  ---
  duration_ms: 1.132583
  ...
# Subtest: forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
ok 122 - forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
  ---
  duration_ms: 0.577843
  ...
# Subtest: new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
ok 123 - new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
  ---
  duration_ms: 0.545912
  ...
# Subtest: submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
ok 124 - submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
  ---
  duration_ms: 0.147261
  ...
# Subtest: submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
ok 125 - submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
  ---
  duration_ms: 0.143204
  ...
# Subtest: same-note Pomodoro link runtime: task and ledger edits merge into one transaction
ok 126 - same-note Pomodoro link runtime: task and ledger edits merge into one transaction
  ---
  duration_ms: 1.218897
  ...
# Subtest: linking an already-linked Ready task raises it to Next without duplicating the link
ok 127 - linking an already-linked Ready task raises it to Next without duplicating the link
  ---
  duration_ms: 0.501157
  ...
# Subtest: Next task without a block ID preflights the picker before prompting
ok 128 - Next task without a block ID preflights the picker before prompting
  ---
  duration_ms: 0.4605
  ...
# Subtest: Pomodoro link stops before any mutation when today's daily note is missing
ok 129 - Pomodoro link stops before any mutation when today's daily note is missing
  ---
  duration_ms: 0.165225
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
ok 130 - Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
  ---
  duration_ms: 0.450069
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
ok 131 - Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
  ---
  duration_ms: 0.287439
  ...
# Subtest: Pomodoro link aborts without any write when the task line changed since it was selected
ok 132 - Pomodoro link aborts without any write when the task line changed since it was selected
  ---
  duration_ms: 0.154905
  ...
# Subtest: Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
ok 133 - Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
  ---
  duration_ms: 0.711859
  ...
# Subtest: canceling the Pomodoro block-ID modal leaves the note untouched
ok 134 - canceling the Pomodoro block-ID modal leaves the note untouched
  ---
  duration_ms: 0.213177
  ...
# Subtest: review-walk: existing-ID link hands its Linked notice to continue with no separate notice
ok 135 - review-walk: existing-ID link hands its Linked notice to continue with no separate notice
  ---
  duration_ms: 1.193148
  ...
# Subtest: review-walk: prompted-ID link continues after submit
ok 136 - review-walk: prompted-ID link continues after submit
  ---
  duration_ms: 1.553957
  ...
# Subtest: review-walk: prompt cancel settles with null
ok 137 - review-walk: prompt cancel settles with null
  ---
  duration_ms: 0.15151
  ...
# Subtest: review-walk: BUSY swallows the key with no write
ok 138 - review-walk: BUSY swallows the key with no write
  ---
  duration_ms: 0.232234
  ...
# Subtest: review-walk: failed link keeps its notice and settles with null
ok 139 - review-walk: failed link keeps its notice and settles with null
  ---
  duration_ms: 0.166838
  ...
# Subtest: review-walk: partial link keeps its notice and never continues with an outcome
ok 140 - review-walk: partial link keeps its notice and never continues with an outcome
  ---
  duration_ms: 0.627288
  ...
# Subtest: inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
ok 141 - inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
  ---
  duration_ms: 0.201415
  ...
# Subtest: inbox-route: non-inbox notes and task-link mode never prompt
ok 142 - inbox-route: non-inbox notes and task-link mode never prompt
  ---
  duration_ms: 0.788916
  ...
# Subtest: inbox-route: cancel writes nothing and settles once
ok 143 - inbox-route: cancel writes nothing and settles once
  ---
  duration_ms: 0.306075
  ...
# Subtest: inbox-route: stay matches today
ok 144 - inbox-route: stay matches today
  ---
  duration_ms: 0.564337
  ...
# Subtest: inbox-route: move links, then moves, with one composed toast and a route continue
ok 145 - inbox-route: move links, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.643669
  ...
# Subtest: inbox-route: a new block ID goes through the route, then the picker, then the ID prompt
ok 146 - inbox-route: a new block ID goes through the route, then the picker, then the ID prompt
  ---
  duration_ms: 0.67562
  ...
# Subtest: inbox-route: a submitted ID that already exists in the destination keeps the prompt open
ok 147 - inbox-route: a submitted ID that already exists in the destination keeps the prompt open
  ---
  duration_ms: 0.361611
  ...
# Subtest: inbox-route: a move failure gives the partial notice plus a link-today continue
ok 148 - inbox-route: a move failure gives the partial notice plus a link-today continue
  ---
  duration_ms: 0.552465
  ...
# Subtest: review-walk: no nav or nav v2 keeps today's notices
ok 149 - review-walk: no nav or nav v2 keeps today's notices
  ---
  duration_ms: 0.93713
  ...
# Subtest: inbox-route: source drift during route prompt refuses without writes
ok 150 - inbox-route: source drift during route prompt refuses without writes
  ---
  duration_ms: 0.263223
  ...
# Subtest: inbox-route: route cancel up front writes nothing, opens no ID prompt, and settles null once
ok 151 - inbox-route: route cancel up front writes nothing, opens no ID prompt, and settles null once
  ---
  duration_ms: 0.234739
  ...
# Subtest: inbox-route: link no-op with move never commits
ok 152 - inbox-route: link no-op with move never commits
  ---
  duration_ms: 0.181968
  ...
# Subtest: picker opens only on the link direction, never on unlink
ok 153 - picker opens only on the link direction, never on unlink
  ---
  duration_ms: 9.712456
  ...
# Subtest: picker never opens in task-link mode
ok 154 - picker never opens in task-link mode
  ---
  duration_ms: 2.21533
  ...
# Subtest: Depends-On refusals never open the picker
ok 155 - Depends-On refusals never open the picker
  ---
  duration_ms: 0.917633
  ...
# Subtest: preflight refusals open nothing
ok 156 - preflight refusals open nothing
  ---
  duration_ms: 0.491318
  ...
# Subtest: direct picker captures one task suggestion with a one-based line and live note text
ok 157 - direct picker captures one task suggestion with a one-based line and live note text
  ---
  duration_ms: 1.016821
  ...
# Subtest: missing task-theme APIs leave the direct picker on its existing default
ok 158 - missing task-theme APIs leave the direct picker on its existing default
  ---
  duration_ms: 0.666422
  ...
# Subtest: picking a non-default entry links there
ok 159 - picking a non-default entry links there
  ---
  duration_ms: 1.121792
  ...
# Subtest: cancel writes nothing with no Notice and settles the walk null
ok 160 - cancel writes nothing with no Notice and settles the walk null
  ---
  duration_ms: 0.611919
  ...
# Subtest: a no-ID task gets picker, then the block-ID prompt with the target carried
ok 161 - a no-ID task gets picker, then the block-ID prompt with the target carried
  ---
  duration_ms: 1.013335
  ...
# Subtest: inbox order is route, then picker, then write
ok 162 - inbox order is route, then picker, then write
  ---
  duration_ms: 0.986875
  ...
# Subtest: a route cancel never opens the picker and writes nothing
ok 163 - a route cancel never opens the picker and writes nothing
  ---
  duration_ms: 0.336052
  ...
# Subtest: a routed move suggests from the destination with a one-line virtual note
ok 164 - a routed move suggests from the destination with a one-line virtual note
  ---
  duration_ms: 0.485207
  ...
# Subtest: a routed stay suggests from the inbox path
ok 165 - a routed stay suggests from the inbox path
  ---
  duration_ms: 0.515835
  ...
# Subtest: a routed move carries the destination chip and a stay carries none
ok 166 - a routed move carries the destination chip and a stay carries none
  ---
  duration_ms: 0.498973
  ...
# Subtest: a review-walk landing continues with link-today and the new text
ok 167 - a review-walk landing continues with link-today and the new text
  ---
  duration_ms: 0.510204
  ...
# Subtest: an all-closed ledger creates a new entry after the last completed block
ok 168 - an all-closed ledger creates a new entry after the last completed block
  ---
  duration_ms: 1.412537
  ...
# Subtest: several running entries allow an explicit pick
ok 169 - several running entries allow an explicit pick
  ---
  duration_ms: 0.583243
  ...
# Subtest: a target that changed before commit refuses with no writes
ok 170 - a target that changed before commit refuses with no writes
  ---
  duration_ms: 0.406817
  ...
# Subtest: a target that closed before commit refuses with no writes
ok 171 - a target that closed before commit refuses with no writes
  ---
  duration_ms: 0.357192
  ...
# Subtest: the task note being the daily note uses one editor transaction
ok 172 - the task note being the daily note uses one editor transaction
  ---
  duration_ms: 0.683085
  ...
# Subtest: promptOpen blocks re-entry while the picker is open
ok 173 - promptOpen blocks re-entry while the picker is open
  ---
  duration_ms: 11.424526
  ...
# Subtest: direct picker request carries the task line text for the footer
ok 174 - direct picker request carries the task line text for the footer
  ---
  duration_ms: 0.379955
  ...
# Subtest: direct picker stays task-aware when the live note text is unavailable
ok 175 - direct picker stays task-aware when the live note text is unavailable
  ---
  duration_ms: 0.243605
  ...
# Subtest: header shows title, subtitle, lane chip per status, and block-ID chip
ok 176 - header shows title, subtitle, lane chip per status, and block-ID chip
  ---
  duration_ms: 7.896179
  ...
# Subtest: rows render in document order with the default selected
ok 177 - rows render in document order with the default selected
  ---
  duration_ms: 1.012804
  ...
# Subtest: recent theme rows follow today's rows and render component swatches
ok 178 - recent theme rows follow today's rows and render component swatches
  ---
  duration_ms: 28.130617
  ...
# Subtest: exact recent themes suppress generic creation and preserve catalog spelling
ok 179 - exact recent themes suppress generic creation and preserve catalog spelling
  ---
  duration_ms: 4.759088
  ...
# Subtest: Ctrl+D hides a Recent suggestion as an undoable ghost and leaves Today unchanged
ok 180 - Ctrl+D hides a Recent suggestion as an undoable ghost and leaves Today unchanged
  ---
  duration_ms: 13.732774
  ...
# Subtest: new-name rows show near-duplicate and hidden-theme hints
ok 181 - new-name rows show near-duplicate and hidden-theme hints
  ---
  duration_ms: 2.734021
  ...
# Subtest: running row shows progress fraction and minutes-left meta
ok 182 - running row shows progress fraction and minutes-left meta
  ---
  duration_ms: 0.75946
  ...
# Subtest: unnamed entries render muted italic
ok 183 - unnamed entries render muted italic
  ---
  duration_ms: 0.399794
  ...
# Subtest: filtering ranks, highlights, and clearing restores the default
ok 184 - filtering ranks, highlights, and clearing restores the default
  ---
  duration_ms: 0.865773
  ...
# Subtest: create row meta and divider
ok 185 - create row meta and divider
  ---
  duration_ms: 4.195692
  ...
# Subtest: exact open names suppress the create row; prefix matches keep it
ok 186 - exact open names suppress the create row; prefix matches keep it
  ---
  duration_ms: 0.855203
  ...
# Subtest: create rows have no type budget badge
ok 187 - create rows have no type budget badge
  ---
  duration_ms: 0.687573
  ...
# Subtest: invalid rows explain the grammar and are inert on Enter
ok 188 - invalid rows explain the grammar and are inert on Enter
  ---
  duration_ms: 2.924454
  ...
# Subtest: multiple running entries show the banner, no pills, and block creation
ok 189 - multiple running entries show the banner, no pills, and block creation
  ---
  duration_ms: 0.859031
  ...
# Subtest: navigation wraps and skips non-selectable rows
ok 190 - navigation wraps and skips non-selectable rows
  ---
  duration_ms: 1.274524
  ...
# Subtest: empty state invites planning a Pomodoro
ok 191 - empty state invites planning a Pomodoro
  ---
  duration_ms: 0.247452
  ...
# Subtest: footer hints and plan meter
ok 192 - footer hints and plan meter
  ---
  duration_ms: 0.990041
  ...
# Subtest: Enter chooses the selected row; click chooses that row
ok 193 - Enter chooses the selected row; click chooses that row
  ---
  duration_ms: 0.78004
  ...
# Subtest: Shift+Enter creates; an exact open name links there instead
ok 194 - Shift+Enter creates; an exact open name links there instead
  ---
  duration_ms: 0.745964
  ...
# Subtest: Ctrl+Shift+Enter commits exactly like Enter
ok 195 - Ctrl+Shift+Enter commits exactly like Enter
  ---
  duration_ms: 0.362793
  ...
# Subtest: Escape and Ctrl+[ cancel with no choice; settle-once holds
ok 196 - Escape and Ctrl+[ cancel with no choice; settle-once holds
  ---
  duration_ms: 2.038303
  ...
# Subtest: done-today themes stay in Recent while open Today themes stay excluded
ok 197 - done-today themes stay in Recent while open Today themes stay excluded
  ---
  duration_ms: 0.948421
  ...
# Subtest: configured theme menu vectors scope Recent, preserve config order, and flag new names
ok 198 - configured theme menu vectors scope Recent, preserve config order, and flag new names
  ---
  duration_ms: 2.471138
  ...
# Subtest: configured empty-query picker shows up to twelve configured themes
ok 199 - configured empty-query picker shows up to twelve configured themes
  ---
  duration_ms: 0.305123
  ...
# Subtest: link success notice names an unconfigured theme after creating its Pomodoro
ok 200 - link success notice names an unconfigured theme after creating its Pomodoro
  ---
  duration_ms: 0.392981
  ...
# Subtest: typing done shows only the Recent DONE row and keeps catalog spelling
ok 201 - typing done shows only the Recent DONE row and keeps catalog spelling
  ---
  duration_ms: 0.990211
  ...
# Subtest: Today exclusions apply before query filtering; cancelled themes stay Recent
ok 202 - Today exclusions apply before query filtering; cancelled themes stay Recent
  ---
  duration_ms: 1.165536
  ...
# Subtest: suggested entry rows render the reason, dot, theme pill, and accessible label
ok 203 - suggested entry rows render the reason, dot, theme pill, and accessible label
  ---
  duration_ms: 1.442414
  ...
# Subtest: reading and note suggestions render their own reasons and footer phrases
ok 204 - reading and note suggestions render their own reasons and footer phrases
  ---
  duration_ms: 1.04188
  ...
# Subtest: footer previews the default merge and the explicit retype with suggestion context
ok 205 - footer previews the default merge and the explicit retype with suggestion context
  ---
  duration_ms: 1.423078
  ...
# Subtest: footer hides without task context or theme APIs
ok 206 - footer hides without task context or theme APIs
  ---
  duration_ms: 2.413078
  ...
# Subtest: footer states a keep consequence when the destination already agrees
ok 207 - footer states a keep consequence when the destination already agrees
  ---
  duration_ms: 0.733932
  ...
# Subtest: footer previews PLAN, LATER, and Tab cycling on a composite
ok 208 - footer previews PLAN, LATER, and Tab cycling on a composite
  ---
  duration_ms: 1.265326
  ...
# Subtest: footer refreshes on selection moves and hides on inert rows
ok 209 - footer refreshes on selection moves and hides on inert rows
  ---
  duration_ms: 0.80644
  ...
# Subtest: untouched refresh preserves a still-eligible suggested entry; arrivals adopt a first default
ok 210 - untouched refresh preserves a still-eligible suggested entry; arrivals adopt a first default
  ---
  duration_ms: 11.669502
  ...
# Subtest: refresh after typing preserves the user's position and initial key
ok 211 - refresh after typing preserves the user's position and initial key
  ---
  duration_ms: 3.484023
  ...
# Subtest: removed rows fall back deterministically without clearing interaction
ok 212 - removed rows fall back deterministically without clearing interaction
  ---
  duration_ms: 2.003616
  ...
# Subtest: clearing a query keeps interaction but returning home is not deliberate
ok 213 - clearing a query keeps interaction but returning home is not deliberate
  ---
  duration_ms: 1.028023
  ...
# Subtest: suggestion never recomputes on refresh and survives API changes
ok 214 - suggestion never recomputes on refresh and survives API changes
  ---
  duration_ms: 2.134726
  ...
# Subtest: deferred fetch makes an unknown suggestion eligible and settles the untouched default
ok 215 - deferred fetch makes an unknown suggestion eligible and settles the untouched default
  ---
  duration_ms: 1.280044
  ...
# Subtest: onChange adopts a newly eligible existing match only before interaction
ok 216 - onChange adopts a newly eligible existing match only before interaction
  ---
  duration_ms: 0.702352
  ...
# Subtest: refresh after arrows and after typing then clearing keeps the settled user key
ok 217 - refresh after arrows and after typing then clearing keeps the settled user key
  ---
  duration_ms: 0.786662
  ...
# Subtest: typed theme suggestion decorates the final Recent row without changing PT7 order
ok 218 - typed theme suggestion decorates the final Recent row without changing PT7 order
  ---
  duration_ms: 3.244205
  ...
# Subtest: Alt+Enter explicitly requests retype; plain commits keep the default merge
ok 219 - Alt+Enter explicitly requests retype; plain commits keep the default merge
  ---
  duration_ms: 0.72799
  ...
# Subtest: Enter, click, and Ctrl+Shift+Enter share the deliberate rule
ok 220 - Enter, click, and Ctrl+Shift+Enter share the deliberate rule
  ---
  duration_ms: 1.547104
  ...
# Subtest: Shift+Enter named commits are always deliberate
ok 221 - Shift+Enter named commits are always deliberate
  ---
  duration_ms: 1.028774
  ...
# Subtest: cancellation writes nothing even when task-aware
ok 222 - cancellation writes nothing even when task-aware
  ---
  duration_ms: 0.40331
  ...
# Subtest: Ctrl+D on the suggested create row is consumed without writes
ok 223 - Ctrl+D on the suggested create row is consumed without writes
  ---
  duration_ms: 5.921578
  ...
# Subtest: canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
ok 224 - canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
  ---
  duration_ms: 1.690909
  ...
# Subtest: canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
ok 225 - canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
  ---
  duration_ms: 0.297448
  ...
# Subtest: pomodoroLinkSelectorSlug mirrors capture slugs
ok 226 - pomodoroLinkSelectorSlug mirrors capture slugs
  ---
  duration_ms: 0.230791
  ...
# Subtest: parsePomodoroEntryParts reads canonical and legacy entry lines
ok 227 - parsePomodoroEntryParts reads canonical and legacy entry lines
  ---
  duration_ms: 0.949112
  ...
# Subtest: collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
ok 228 - collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
  ---
  duration_ms: 1.534971
  ...
# Subtest: collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
ok 229 - collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
  ---
  duration_ms: 0.993196
  ...
# Subtest: collectPomodoroLinkEntries counts links but excludes struck references
ok 230 - collectPomodoroLinkEntries counts links but excludes struck references
  ---
  duration_ms: 0.469276
  ...
# Subtest: collectPomodoroLinkEntries falls back to range text and position titles
ok 231 - collectPomodoroLinkEntries falls back to range text and position titles
  ---
  duration_ms: 0.286487
  ...
# Subtest: pomodoroRunProgress reports fractions, overtime, and midnight wrap
ok 232 - pomodoroRunProgress reports fractions, overtime, and midnight wrap
  ---
  duration_ms: 0.485116
  ...
# Subtest: buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
ok 233 - buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
  ---
  duration_ms: 1.386687
  ...
# Subtest: buildPomodoroLinkPickerRows keeps the create row for prefix matches
ok 234 - buildPomodoroLinkPickerRows keeps the create row for prefix matches
  ---
  duration_ms: 0.423409
  ...
# Subtest: buildPomodoroLinkPickerRows marks completed-only names as again
ok 235 - buildPomodoroLinkPickerRows marks completed-only names as again
  ---
  duration_ms: 0.264836
  ...
# Subtest: buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
ok 236 - buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
  ---
  duration_ms: 0.529561
  ...
# Subtest: buildPomodoroLinkPickerRows matches times, positions, and block IDs
ok 237 - buildPomodoroLinkPickerRows matches times, positions, and block IDs
  ---
  duration_ms: 0.538648
  ...
# Subtest: resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
ok 238 - resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
  ---
  duration_ms: 0.332686
  ...
# Subtest: defaultPomodoroLinkChoice returns the default entry or null
ok 239 - defaultPomodoroLinkChoice returns the default entry or null
  ---
  duration_ms: 0.200172
  ...
# Subtest: planExplicitPomodoroLinkInsertion links under a chosen existing entry
ok 240 - planExplicitPomodoroLinkInsertion links under a chosen existing entry
  ---
  duration_ms: 1.471931
  ...
# Subtest: planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
ok 241 - planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
  ---
  duration_ms: 0.525243
  ...
# Subtest: planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
ok 242 - planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
  ---
  duration_ms: 1.288982
  ...
# Subtest: planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
ok 243 - planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
  ---
  duration_ms: 0.471501
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after the running entry
ok 244 - planExplicitPomodoroLinkInsertion creates after the running entry
  ---
  duration_ms: 0.782865
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
ok 245 - planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
  ---
  duration_ms: 0.904247
  ...
# Subtest: planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
ok 246 - planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
  ---
  duration_ms: 0.274234
  ...
# Subtest: planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
ok 247 - planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
  ---
  duration_ms: 0.371529
  ...
# Subtest: planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
ok 248 - planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
  ---
  duration_ms: 0.435542
  ...
# Subtest: buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
ok 249 - buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
  ---
  duration_ms: 0.243836
  ...
# Subtest: buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
ok 250 - buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
  ---
  duration_ms: 0.20469
  ...
# Subtest: planExplicitPomodoroLinkInsertion matches mixed-case raced open names
ok 251 - planExplicitPomodoroLinkInsertion matches mixed-case raced open names
  ---
  duration_ms: 0.23015
  ...
# Subtest: buildPomodoroLinkPickerRows bounds \#N position matches
ok 252 - buildPomodoroLinkPickerRows bounds \#N position matches
  ---
  duration_ms: 0.454488
  ...
# Subtest: planPomodoroLinkInsertion without a target keeps today's behavior and shape
ok 253 - planPomodoroLinkInsertion without a target keeps today's behavior and shape
  ---
  duration_ms: 0.52323
  ...
# Subtest: buildPomodoroLinkPickerRows keeps a done-only theme in Recent
ok 254 - buildPomodoroLinkPickerRows keeps a done-only theme in Recent
  ---
  duration_ms: 1.719203
  ...
# Subtest: shared task-theme preselection vectors match the bob-cli model
ok 255 - shared task-theme preselection vectors match the bob-cli model
  ---
  duration_ms: 1.710937
  ...
# Subtest: task-theme preselection normalizes exemptions without a type cap
ok 256 - task-theme preselection normalizes exemptions without a type cap
  ---
  duration_ms: 0.171487
  ...
# Subtest: task-aware rows preselect an existing match when creation is blocked
ok 257 - task-aware rows preselect an existing match when creation is blocked
  ---
  duration_ms: 0.393832
  ...
# Subtest: task-aware typed queries keep PT7 order and only annotate the matching row
ok 258 - task-aware typed queries keep PT7 order and only annotate the matching row
  ---
  duration_ms: 0.330892
  ...
# Subtest: suggested creation uses catalog spelling and removes its duplicate Recent row
ok 259 - suggested creation uses catalog spelling and removes its duplicate Recent row
  ---
  duration_ms: 0.875321
  ...
# Subtest: theme suggestion identity ignores decorative hue and catalog flags
ok 260 - theme suggestion identity ignores decorative hue and catalog flags
  ---
  duration_ms: 1.313769
  ...
# Subtest: theme suggestion identity treats a changed declaring note as a different suggestion
ok 261 - theme suggestion identity treats a changed declaring note as a different suggestion
  ---
  duration_ms: 0.191776
  ...
# Subtest: current exempt keys distinguish valid empty configuration from unavailable caps
ok 262 - current exempt keys distinguish valid empty configuration from unavailable caps
  ---
  duration_ms: 1.153212
  ...
# Subtest: planTargetTaskUpdate applies themeEdit after lane changes and before a new block ID
ok 263 - planTargetTaskUpdate applies themeEdit after lane changes and before a new block ID
  ---
  duration_ms: 0.864481
  ...
# Subtest: planTargetTaskUpdate theme-only Next task never stamps freshness
ok 264 - planTargetTaskUpdate theme-only Next task never stamps freshness
  ---
  duration_ms: 0.36692
  ...
# Subtest: planTargetTaskUpdate stamps a lane rewrite after the theme field is in place
ok 265 - planTargetTaskUpdate stamps a lane rewrite after the theme field is in place
  ---
  duration_ms: 0.360589
  ...
# Subtest: planTargetTaskUpdate without themeEdit preserves an authored theme field
ok 266 - planTargetTaskUpdate without themeEdit preserves an authored theme field
  ---
  duration_ms: 0.210061
  ...
# Subtest: planTargetTaskUpdate clears a theme field and keeps CRLF plus a trailing block ID
ok 267 - planTargetTaskUpdate clears a theme field and keeps CRLF plus a trailing block ID
  ---
  duration_ms: 0.173511
  ...
# Subtest: a named destination retypes the task in the same cross-note write
ok 268 - a named destination retypes the task in the same cross-note write
  ---
  duration_ms: 5.642564
  ...
# Subtest: a newly named picker entry forces the retype landing path
ok 269 - a newly named picker entry forces the retype landing path
  ---
  duration_ms: 0.514743
  ...
# Subtest: Pomodoro cleanup agrees only touched open entries in the same edit plan
ok 270 - Pomodoro cleanup agrees only touched open entries in the same edit plan
  ---
  duration_ms: 0.626186
  ...
# Subtest: unavailable current caps still retype the task and retain lane, ID, and freshness edits
ok 271 - unavailable current caps still retype the task and retain lane, ID, and freshness edits
  ---
  duration_ms: 4.562402
  ...
# Subtest: real Ledger Tools planner writes with an empty exempt list and custom exemptions
ok 272 - real Ledger Tools planner writes with an empty exempt list and custom exemptions
  ---
  duration_ms: 2.16789
  ...
# Subtest: a Ready scheduled task sets Next, logs the date, and remembers the theme
ok 273 - a Ready scheduled task sets Next, logs the date, and remembers the theme
  ---
  duration_ms: 1.467422
  ...
# Subtest: choosing the inherited destination clears an existing task theme
ok 274 - choosing the inherited destination clears an existing task theme
  ---
  duration_ms: 0.422557
  ...
# Subtest: a theme-only Next task with a new block ID still stamps because the ID rewrote the line
ok 275 - a theme-only Next task with a new block ID still stamps because the ID rewrote the line
  ---
  duration_ms: 0.405224
  ...
# Subtest: duplicate and paren theme fields repair only on an eligible deliberate write
ok 276 - duplicate and paren theme fields repair only on an eligible deliberate write
  ---
  duration_ms: 0.373012
  ...
# Subtest: a stale shown suggestion links and skips the theme edit
ok 277 - a stale shown suggestion links and skips the theme edit
  ---
  duration_ms: 0.358474
  ...
# Subtest: decorative catalog metadata on a live suggestion does not skip the write
ok 278 - decorative catalog metadata on a live suggestion does not skip the write
  ---
  duration_ms: 0.396396
  ...
# Subtest: Enter merges the current type into the destination name
ok 279 - Enter merges the current type into the destination name
  ---
  duration_ms: 0.380326
  ...
# Subtest: a container keeps the type on the default landing
ok 280 - a container keeps the type on the default landing
  ---
  duration_ms: 0.315482
  ...
# Subtest: untouched default (not deliberate) links without storing a field
ok 281 - untouched default (not deliberate) links without storing a field
  ---
  duration_ms: 0.331513
  ...
# Subtest: absent theme APIs leave the picker write path usable without a field
ok 282 - absent theme APIs leave the picker write path usable without a field
  ---
  duration_ms: 0.395835
  ...
# Subtest: a blocked dependency consumption never writes a theme field
ok 283 - a blocked dependency consumption never writes a theme field
  ---
  duration_ms: 1.871604
  ...
# Subtest: same-note combined edit writes the theme and the link in one editor transaction
ok 284 - same-note combined edit writes the theme and the link in one editor transaction
  ---
  duration_ms: 0.634451
  ...
# Subtest: a failed daily write after a saved theme reports the theme and the link failure
ok 285 - a failed daily write after a saved theme reports the theme and the link failure
  ---
  duration_ms: 0.42933
  ...
# Subtest: catalog spelling wins over a canonical landing name
ok 286 - catalog spelling wins over a canonical landing name
  ---
  duration_ms: 0.338546
  ...
# Subtest: a routed inbox task retypes from the destination suggestion
ok 287 - a routed inbox task retypes from the destination suggestion
  ---
  duration_ms: 0.713152
  ...
# Subtest: the inbox and the destination inherit different types, and the user picks the destination's suggested Pomodoro
ok 288 - the inbox and the destination inherit different types, and the user picks the destination's suggested Pomodoro
  ---
  duration_ms: 0.394152
  ...
# Subtest: a routed link that picks a different type writes the field
ok 289 - a routed link that picks a different type writes the field
  ---
  duration_ms: 0.436123
  ...
# Subtest: malformed themeIntent never enables a write
ok 290 - malformed themeIntent never enables a write
  ---
  duration_ms: 0.272961
  ...
# Subtest: themeIntent survives normalizePomodoroLinkPickerChoice for a later consumer
ok 291 - themeIntent survives normalizePomodoroLinkPickerChoice for a later consumer
  ---
  duration_ms: 0.215111
  ...
# Subtest: Tab pick chooses that type component of a composite destination
ok 292 - Tab pick chooses that type component of a composite destination
  ---
  duration_ms: 0.335741
  ...
# Subtest: unlink preserves an authored task theme
ok 293 - unlink preserves an authored task theme
  ---
  duration_ms: 2.977305
  ...
# Subtest: direct unlink without a daily note keeps the Next lane and reports it
ok 294 - direct unlink without a daily note keeps the Next lane and reports it
  ---
  duration_ms: 2.743108
  ...
# Subtest: In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
ok 295 - In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
  ---
  duration_ms: 0.506417
  ...
# Subtest: In Progress unlink with a summary keeps the lane and creates a Work Log
ok 296 - In Progress unlink with a summary keeps the lane and creates a Work Log
  ---
  duration_ms: 1.22034
  ...
# Subtest: In Progress unlink revalidates task text and block-ID uniqueness at confirmation
ok 297 - In Progress unlink revalidates task text and block-ID uniqueness at confirmation
  ---
  duration_ms: 0.325111
  ...
# Subtest: Next task unlink removes current and future links and keeps the Next lane
ok 298 - Next task unlink removes current and future links and keeps the Next lane
  ---
  duration_ms: 3.714914
  ...
# Subtest: In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
ok 299 - In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
  ---
  duration_ms: 0.754731
  ...
# Subtest: same-note Next unlink merges the Work Log and all-open cleanup in the active editor
ok 300 - same-note Next unlink merges the Work Log and all-open cleanup in the active editor
  ---
  duration_ms: 0.809485
  ...
# Subtest: same-note In Progress unlink merges cleanup and Work Log in the active editor
ok 301 - same-note In Progress unlink merges cleanup and Work Log in the active editor
  ---
  duration_ms: 0.590748
  ...
# Subtest: Next unlink stops before any write when daily cleanup write is stale
ok 302 - Next unlink stops before any write when daily cleanup write is stale
  ---
  duration_ms: 0.678005
  ...
# Subtest: Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
ok 303 - Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
  ---
  duration_ms: 1.055375
  ...
# Subtest: In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
ok 304 - In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
  ---
  duration_ms: 0.70647
  ...
# Subtest: review-walk: unlink settles with null and keeps its notice
ok 305 - review-walk: unlink settles with null and keeps its notice
  ---
  duration_ms: 1.333577
  ...
# Subtest: inbox-route: unlink cancel writes nothing
ok 306 - inbox-route: unlink cancel writes nothing
  ---
  duration_ms: 0.350589
  ...
# Subtest: inbox-route: unlink stay matches today and never commits
ok 307 - inbox-route: unlink stay matches today and never commits
  ---
  duration_ms: 0.594315
  ...
# Subtest: inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
ok 308 - inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.71228
  ...
# Subtest: inbox-route: In Progress unlink with a Work summary routes
ok 309 - inbox-route: In Progress unlink with a Work summary routes
  ---
  duration_ms: 0.601959
  ...
# Subtest: inbox-route: unlink move failure gives the partial notice and stays
ok 310 - inbox-route: unlink move failure gives the partial notice and stays
  ---
  duration_ms: 0.310563
  ...
# Subtest: inbox-route: non-inbox unlink never prompts
ok 311 - inbox-route: non-inbox unlink never prompts
  ---
  duration_ms: 0.305052
  ...
# Subtest: review-walk: Work-summary unlink path retains origin until submit
ok 312 - review-walk: Work-summary unlink path retains origin until submit
  ---
  duration_ms: 0.309681
  ...
# Subtest: inbox-route: unlink source drift during route prompt refuses without writes
ok 313 - inbox-route: unlink source drift during route prompt refuses without writes
  ---
  duration_ms: 0.223256
  ...
# Subtest: inbox-route: Work-summary route cancel returns sentinel and settles null once
ok 314 - inbox-route: Work-summary route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.261259
  ...
# Subtest: inbox-route: unlink no-op with move never commits
ok 315 - inbox-route: unlink no-op with move never commits
  ---
  duration_ms: 0.233215
  ...
# Subtest: same-note unlink maps a task below removed entries through Work-summary inserts
ok 316 - same-note unlink maps a task below removed entries through Work-summary inserts
  ---
  duration_ms: 0.768177
  ...
# Subtest: the unlink preview shows the write-instant stamp and re-renders on the clock
ok 317 - the unlink preview shows the write-instant stamp and re-renders on the clock
  ---
  duration_ms: 0.531975
  ...
# Subtest: a prompt opened at 23:59 and committed at 00:01 stamps the commit instant
ok 318 - a prompt opened at 23:59 and committed at 00:01 stamps the commit instant
  ---
  duration_ms: 0.458305
  ...
# Subtest: direct-add seeds from the task headline, not non-task blocks
ok 319 - direct-add seeds from the task headline, not non-task blocks
  ---
  duration_ms: 3.957678
  ...
# Subtest: direct-add seeds a plain note bullet from its text without the created stamp
ok 320 - direct-add seeds a plain note bullet from its text without the created stamp
  ---
  duration_ms: 0.61775
  ...
# Subtest: link-task-complete seeds from the target, prefers open buffers
ok 321 - link-task-complete seeds from the target, prefers open buffers
  ---
  duration_ms: 0.913785
  ...
# Subtest: link-task-complete reports stale and unreadable targets
ok 322 - link-task-complete reports stale and unreadable targets
  ---
  duration_ms: 0.274885
  ...
# Subtest: pomodoro link seeds after the choice from the cursor task
ok 323 - pomodoro link seeds after the choice from the cursor task
  ---
  duration_ms: 0.329389
  ...
# Subtest: marker rename suggests from the unique task, never hiding ambiguity
ok 324 - marker rename suggests from the unique task, never hiding ambiguity
  ---
  duration_ms: 0.516437
  ...
# Subtest: marker rename suggests from a unique plain note bullet
ok 325 - marker rename suggests from a unique plain note bullet
  ---
  duration_ms: 0.323698
  ...
# Subtest: modal seeds the value, selects once, and never overwrites typing
ok 326 - modal seeds the value, selects once, and never overwrites typing
  ---
  duration_ms: 1.094309
  ...
# Subtest: modal disables Save while loading and survives close/reopen
ok 327 - modal disables Save while loading and survives close/reopen
  ---
  duration_ms: 1.180925
  ...
# Subtest: submit revalidates: occupied IDs and stale tasks fail editable
ok 328 - submit revalidates: occupied IDs and stale tasks fail editable
  ---
  duration_ms: 1.004919
  ...
# Subtest: cancelling writes no ID and explicit renames keep the current ID
ok 329 - cancelling writes no ID and explicit renames keep the current ID
  ---
  duration_ms: 0.542586
  ...
# Subtest: the task picker drops the paired \#ref and prefixes the book
ok 330 - the task picker drops the paired \#ref and prefixes the book
  ---
  duration_ms: 3.315221
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 331 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.388582
  ...
# Subtest: block-id-prompt LK1–LK19 recognises only relation line shapes
ok 332 - block-id-prompt LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 1.297849
  ...
# Subtest: block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
ok 333 - block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
  ---
  duration_ms: 2.046387
  ...
# Subtest: block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
ok 334 - block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
  ---
  duration_ms: 1.352553
  ...
# Subtest: a rename writes each open note as one editor transaction and undoes in one step
ok 335 - a rename writes each open note as one editor transaction and undoes in one step
  ---
  duration_ms: 12.851821
  ...
# Subtest: a note open in a non-active leaf is edited through its editor, unsaved text included
ok 336 - a note open in a non-active leaf is edited through its editor, unsaved text included
  ---
  duration_ms: 0.766714
  ...
# Subtest: disagreeing open buffers for one note refuse the rename
ok 337 - disagreeing open buffers for one note refuse the rename
  ---
  duration_ms: 0.589836
  ...
# Subtest: a closed note that changed since planning refuses and earlier writes roll back
ok 338 - a closed note that changed since planning refuses and earlier writes roll back
  ---
  duration_ms: 0.786031
  ...
# Subtest: an open note that changed while closed notes were written refuses and rolls back
ok 339 - an open note that changed while closed notes were written refuses and rolls back
  ---
  duration_ms: 0.580098
  ...
# Subtest: undoing the rename in its note rewrites the other notes back, and redo re-applies it
ok 340 - undoing the rename in its note rewrites the other notes back, and redo re-applies it
  ---
  duration_ms: 1.926939
  ...
# Subtest: undoing in a referencing note follows into the destination and the other notes
ok 341 - undoing in a referencing note follows into the destination and the other notes
  ---
  duration_ms: 1.06825
  ...
# Subtest: an ambiguous note is left alone and named in a sticky Notice
ok 342 - an ambiguous note is left alone and named in a sticky Notice
  ---
  duration_ms: 0.752036
  ...
# Subtest: a recorded span that was edited makes its note ambiguous
ok 343 - a recorded span that was edited makes its note ambiguous
  ---
  duration_ms: 1.035547
  ...
# Subtest: editing a note the follow could not rewrite never redoes the rename
ok 344 - editing a note the follow could not rewrite never redoes the rename
  ---
  duration_ms: 1.138565
  ...
# Subtest: records expire, and edits without a live record schedule nothing
ok 345 - records expire, and edits without a live record schedule nothing
  ---
  duration_ms: 0.875101
  ...
# Subtest: a redo during closed-note undo follow converges on the latest editor form
ok 346 - a redo during closed-note undo follow converges on the latest editor form
  ---
  duration_ms: 0.997665
  ...
# Subtest: an undo during closed-note redo follow converges on the latest editor form
ok 347 - an undo during closed-note redo follow converges on the latest editor form
  ---
  duration_ms: 1.612449
  ...
# Subtest: an unrelated edit in a second editor during closed follow is preserved
ok 348 - an unrelated edit in a second editor during closed follow is preserved
  ---
  duration_ms: 0.69654
  ...
# Subtest: blockRenameNoteForm reads token and link forms and refuses mixed or missing states
ok 349 - blockRenameNoteForm reads token and link forms and refuses mixed or missing states
  ---
  duration_ms: 0.256369
  ...
# Subtest: calendar date parsing rejects malformed width and impossible dates
ok 350 - calendar date parsing rejects malformed width and impossible dates
  ---
  duration_ms: 1.715065
  ...
# Subtest: future scheduled field detection respects the yesterday/today/tomorrow boundary
ok 351 - future scheduled field detection respects the yesterday/today/tomorrow boundary
  ---
  duration_ms: 0.453596
  ...
# Subtest: scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
ok 352 - scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
  ---
  duration_ms: 0.190654
  ...
# Subtest: planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
ok 353 - planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
  ---
  duration_ms: 0.85912
  ...
# Subtest: planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
ok 354 - planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
  ---
  duration_ms: 0.214379
  ...
# Subtest: planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
ok 355 - planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
  ---
  duration_ms: 0.172429
  ...
# Subtest: planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
ok 356 - planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
  ---
  duration_ms: 0.163772
  ...
# Subtest: planTargetTaskUpdate leaves today and past schedules untouched
ok 357 - planTargetTaskUpdate leaves today and past schedules untouched
  ---
  duration_ms: 0.2987
  ...
# Subtest: planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
ok 358 - planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
  ---
  duration_ms: 0.364917
  ...
# Subtest: two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
ok 359 - two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
  ---
  duration_ms: 0.517008
  ...
# Subtest: a malformed single scheduled field is never treated as future
ok 360 - a malformed single scheduled field is never treated as future
  ---
  duration_ms: 0.188861
  ...
# Subtest: an ambiguous scheduled field does not block the legacy Ready promotion
ok 361 - an ambiguous scheduled field does not block the legacy Ready promotion
  ---
  duration_ms: 0.202607
  ...
# Subtest: planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
ok 362 - planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
  ---
  duration_ms: 0.140489
  ...
# Subtest: Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
ok 363 - Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
  ---
  duration_ms: 0.47679
  ...
# Subtest: Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
ok 364 - Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
  ---
  duration_ms: 0.173311
  ...
# Subtest: planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
ok 365 - planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
  ---
  duration_ms: 0.251901
  ...
# Subtest: planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
ok 366 - planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
  ---
  duration_ms: 0.156379
  ...
# Subtest: planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
ok 367 - planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.118436
  ...
# Subtest: planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
ok 368 - planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
  ---
  duration_ms: 0.150558
  ...
# Subtest: planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
ok 369 - planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
  ---
  duration_ms: 0.134256
  ...
# Subtest: planTargetTaskUpdate preserves a trailing newline when one was already present
ok 370 - planTargetTaskUpdate preserves a trailing newline when one was already present
  ---
  duration_ms: 0.135468
  ...
# Subtest: planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
ok 371 - planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
  ---
  duration_ms: 0.104269
  ...
# Subtest: planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
ok 372 - planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
  ---
  duration_ms: 0.161238
  ...
# Subtest: planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
ok 373 - planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
  ---
  duration_ms: 0.122665
  ...
# Subtest: existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
ok 374 - existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
  ---
  duration_ms: 3.701548
  ...
# Subtest: new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
ok 375 - new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
  ---
  duration_ms: 0.835615
  ...
# Subtest: activation runtime aborts without any write when the target preimage goes stale
ok 376 - activation runtime aborts without any write when the target preimage goes stale
  ---
  duration_ms: 0.433137
  ...
# Subtest: same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
ok 377 - same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
  ---
  duration_ms: 2.384874
  ...
# Subtest: same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
ok 378 - same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
  ---
  duration_ms: 0.59198
  ...
# Subtest: a source marker edited after a successful existing-ID target write reports an accurate partial notice
ok 379 - a source marker edited after a successful existing-ID target write reports an accurate partial notice
  ---
  duration_ms: 4.797541
  ...
# Subtest: a source marker edited after a successful new-ID target write reports an accurate partial notice
ok 380 - a source marker edited after a successful new-ID target write reports an accurate partial notice
  ---
  duration_ms: 1.029616
  ...
# Subtest: planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
ok 381 - planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
  ---
  duration_ms: 0.257211
  ...
# Subtest: planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
ok 382 - planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
  ---
  duration_ms: 0.171658
  ...
# Subtest: planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
ok 383 - planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
  ---
  duration_ms: 0.197106
  ...
# Subtest: Pomodoro forceNext stamps the pulled-forward Ready task before its block ID
ok 384 - Pomodoro forceNext stamps the pulled-forward Ready task before its block ID
  ---
  duration_ms: 0.587211
  ...
# Subtest: planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
ok 385 - planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.17255
  ...
# Subtest: direct Task Links raise ^prj while never pulling its date forward
ok 386 - direct Task Links raise ^prj while never pulling its date forward
  ---
  duration_ms: 0.184152
  ...
# Subtest: task-link selection: one link is selectable from any column, several are chosen by cursor
ok 387 - task-link selection: one link is selectable from any column, several are chosen by cursor
  ---
  duration_ms: 2.668616
  ...
# Subtest: task-link selection ignores picker/rename markers, plain links, and Markdown-style links
ok 388 - task-link selection ignores picker/rename markers, plain links, and Markdown-style links
  ---
  duration_ms: 0.305303
  ...
# Subtest: dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
ok 389 - dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
  ---
  duration_ms: 0.634712
  ...
# Subtest: inline Task Link deletion removes the token with its decoration and collapses whitespace
ok 390 - inline Task Link deletion removes the token with its decoration and collapses whitespace
  ---
  duration_ms: 0.669298
  ...
# Subtest: dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
ok 391 - dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
  ---
  duration_ms: 0.875432
  ...
# Subtest: mergeCoveringEdits keeps the covering edit and the earlier of identical edits
ok 392 - mergeCoveringEdits keeps the covering edit and the earlier of identical edits
  ---
  duration_ms: 0.212736
  ...
# Subtest: dependency transclusion detection needs an embedded sole-content child of a \#task line
ok 393 - dependency transclusion detection needs an embedded sole-content child of a \#task line
  ---
  duration_ms: 0.43501
  ...
# Subtest: Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
ok 394 - Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
  ---
  duration_ms: 5.03822
  ...
# Subtest: Task Link on a Next target works from an embedded aliased link outside any Pomodoro
ok 395 - Task Link on a Next target works from an embedded aliased link outside any Pomodoro
  ---
  duration_ms: 1.097977
  ...
# Subtest: same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
ok 396 - same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
  ---
  duration_ms: 1.873839
  ...
# Subtest: same-note Task Link deletion clamps the restored cursor to the shortened note
ok 397 - same-note Task Link deletion clamps the restored cursor to the shortened note
  ---
  duration_ms: 0.99495
  ...
# Subtest: a cleanup subtree that covers a nested selected link wins and links are not double counted
ok 398 - a cleanup subtree that covers a nested selected link wins and links are not double counted
  ---
  duration_ms: 1.15727
  ...
# Subtest: same-note Task Link in a closed entry deletes the closed entry it empties
ok 399 - same-note Task Link in a closed entry deletes the closed entry it empties
  ---
  duration_ms: 1.027091
  ...
# Subtest: Task Link in another day's note deletes the emptied entry there and in today's note
ok 400 - Task Link in another day's note deletes the emptied entry there and in today's note
  ---
  duration_ms: 0.838902
  ...
# Subtest: Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
ok 401 - Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
  ---
  duration_ms: 1.620134
  ...
# Subtest: Task Link on an In Progress target with a blank summary logs nothing
ok 402 - Task Link on an In Progress target with a blank summary logs nothing
  ---
  duration_ms: 1.047971
  ...
# Subtest: canceling the In Progress Task Link prompt leaves everything untouched
ok 403 - canceling the In Progress Task Link prompt leaves everything untouched
  ---
  duration_ms: 0.406606
  ...
# Subtest: canceling the In Progress unlink prompt in task mode leaves everything untouched
ok 404 - canceling the In Progress unlink prompt in task mode leaves everything untouched
  ---
  duration_ms: 0.748279
  ...
# Subtest: In Progress Task Link submit revalidates the link line and the target task
ok 405 - In Progress Task Link submit revalidates the link line and the target task
  ---
  duration_ms: 0.856786
  ...
# Subtest: Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
ok 406 - Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
  ---
  duration_ms: 2.267209
  ...
# Subtest: Task Link on a Done or Cancelled target is refused without edits
ok 407 - Task Link on a Done or Cancelled target is refused without edits
  ---
  duration_ms: 0.387029
  ...
# Subtest: Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
ok 408 - Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
  ---
  duration_ms: 0.621998
  ...
# Subtest: precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
ok 409 - precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
  ---
  duration_ms: 1.583093
  ...
# Subtest: Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
ok 410 - Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
  ---
  duration_ms: 0.518189
  ...
# Subtest: Task Link that is a sub-task dependency transclusion is refused without edits
ok 411 - Task Link that is a sub-task dependency transclusion is refused without edits
  ---
  duration_ms: 0.253754
  ...
# Subtest: Task Link partial failure after the daily write is retryable
ok 412 - Task Link partial failure after the daily write is retryable
  ---
  duration_ms: 0.760713
  ...
# Subtest: Task Link stops before any write when the target note changes after planning
ok 413 - Task Link stops before any write when the target note changes after planning
  ---
  duration_ms: 0.452063
  ...
# Subtest: Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
ok 414 - Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
  ---
  duration_ms: 0.406927
  ...
# Subtest: Task Link subtree deletion removes a nested target task without any status write
ok 415 - Task Link subtree deletion removes a nested target task without any status write
  ---
  duration_ms: 0.308739
  ...
# Subtest: whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
ok 416 - whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
  ---
  duration_ms: 0.604965
  ...
# Subtest: selected-link deletion maps a cursor inside a removed entry to its former start
ok 417 - selected-link deletion maps a cursor inside a removed entry to its former start
  ---
  duration_ms: 0.50788
  ...
# Subtest: cache prefilter skips taskless files without reading, reads cacheless files
ok 418 - cache prefilter skips taskless files without reading, reads cacheless files
  ---
  duration_ms: 3.530591
  ...
# Subtest: a throwing file cache falls back to reading
ok 419 - a throwing file cache falls back to reading
  ---
  duration_ms: 0.351842
  ...
# Subtest: non-note and excluded paths never enter the store
ok 420 - non-note and excluded paths never enter the store
  ---
  duration_ms: 0.398331
  ...
# Subtest: unreadable files produce bounded warnings and a quiet footer note
ok 421 - unreadable files produce bounded warnings and a quiet footer note
  ---
  duration_ms: 0.738821
  ...
# Subtest: blockIdsFor exposes the note id set for the detail strip preview
ok 422 - blockIdsFor exposes the note id set for the detail strip preview
  ---
  duration_ms: 0.316704
  ...
# Subtest: taskBearingDocuments reads fresh text on demand
ok 423 - taskBearingDocuments reads fresh text on demand
  ---
  duration_ms: 0.515014
  ...
# Subtest: metadataCache changed re-parses from event data with no extra read
ok 424 - metadataCache changed re-parses from event data with no extra read
  ---
  duration_ms: 0.450661
  ...
# Subtest: vault rename re-keys rows and recomputes the basename index
ok 425 - vault rename re-keys rows and recomputes the basename index
  ---
  duration_ms: 0.929666
  ...
# Subtest: renaming onto an excluded path drops the note
ok 426 - renaming onto an excluded path drops the note
  ---
  duration_ms: 0.390957
  ...
# Subtest: vault delete drops rows
ok 427 - vault delete drops rows
  ---
  duration_ms: 0.512629
  ...
# Subtest: open-time mtime validation queues changed files for background re-parse
ok 428 - open-time mtime validation queues changed files for background re-parse
  ---
  duration_ms: 0.546423
  ...
# Subtest: a vanished file is removed when the reparse queue drains
ok 429 - a vanished file is removed when the reparse queue drains
  ---
  duration_ms: 0.377712
  ...
# Subtest: live overlays win over disk and never persist
ok 430 - live overlays win over disk and never persist
  ---
  duration_ms: 0.316975
  ...
# Subtest: snapshot returns ordered rows, progress, and a live subscription
ok 431 - snapshot returns ordered rows, progress, and a live subscription
  ---
  duration_ms: 0.433608
  ...
# Subtest: filtering performs no vault reads
ok 432 - filtering performs no vault reads
  ---
  duration_ms: 0.335891
  ...
# Subtest: refreshPaths applies post-write content and recomputes locators
ok 433 - refreshPaths applies post-write content and recomputes locators
  ---
  duration_ms: 0.479235
  ...
# Subtest: refreshPathsFromVault re-reads named paths
ok 434 - refreshPathsFromVault re-reads named paths
  ---
  duration_ms: 0.719614
  ...
# Subtest: collectEditorOverlays reads every open markdown editor
ok 435 - collectEditorOverlays reads every open markdown editor
  ---
  duration_ms: 0.43975
  ...
# Subtest: attachLiveUpdates without a host is a safe no-op
ok 436 - attachLiveUpdates without a host is a safe no-op
  ---
  duration_ms: 0.136971
  ...
# Subtest: custom settings narrow the parsed pool
ok 437 - custom settings narrow the parsed pool
  ---
  duration_ms: 0.27235
  ...
# Subtest: snapshot rows keep parsed metadata, leave stored rows bare, and cache search-text-first fields
ok 438 - snapshot rows keep parsed metadata, leave stored rows bare, and cache search-text-first fields
  ---
  duration_ms: 2.50852
  ...
# Subtest: cached and uncached matching stay aligned across overlay, rename collision, delete, and refresh
ok 439 - cached and uncached matching stay aligned across overlay, rename collision, delete, and refresh
  ---
  duration_ms: 5.113675
  ...
# Subtest: task wikilink fixture mirrors bob-cli byte for byte
ok 440 - task wikilink fixture mirrors bob-cli byte for byte
  ---
  duration_ms: 1.689667
  ...
# Subtest: every vector ranks the same rows bob serves
ok 441 - every vector ranks the same rows bob serves
  ---
  duration_ms: 7.783493
  ...
# Subtest: frontmatter tasks never parse, unclosed fences stay open
ok 442 - frontmatter tasks never parse, unclosed fences stay open
  ---
  duration_ms: 0.403851
  ...
# Subtest: task grammar mirrors bob: dashes only, exact filter token
ok 443 - task grammar mirrors bob: dashes only, exact filter token
  ---
  duration_ms: 0.174974
  ...
# Subtest: trailing IDs need whitespace and clean bytes; every line counts
ok 444 - trailing IDs need whitespace and clean bytes; every line counts
  ---
  duration_ms: 0.190854
  ...
# Subtest: hide and project-block tags are exact tokens
ok 445 - hide and project-block tags are exact tokens
  ---
  duration_ms: 0.369546
  ...
# Subtest: search text drops filters, fields, and the block ID
ok 446 - search text drops filters, fields, and the block ID
  ---
  duration_ms: 0.461782
  ...
# Subtest: sections track headings and depth counts indentation
ok 447 - sections track headings and depth counts indentation
  ---
  duration_ms: 0.45561
  ...
# Subtest: note paths, locators, and archive targets
ok 448 - note paths, locators, and archive targets
  ---
  duration_ms: 0.520624
  ...
# Subtest: match tiers, AND terms, and empty queries
ok 449 - match tiers, AND terms, and empty queries
  ---
  duration_ms: 0.578114
  ...
# Subtest: previous daily is the latest daily before the anchor
ok 450 - previous daily is the latest daily before the anchor
  ---
  duration_ms: 0.245369
  ...
# Subtest: guards mirror bob, minus the read-only check
ok 451 - guards mirror bob, minus the read-only check
  ---
  duration_ms: 0.174062
  ...
# Subtest: fused scorer matches the layered scorer across randomized rows and queries
ok 452 - fused scorer matches the layered scorer across randomized rows and queries
  ---
  duration_ms: 53.496895
  ...
# Subtest: ID-less task identity relocates only to one exact line
ok 453 - ID-less task identity relocates only to one exact line
  ---
  duration_ms: 1.570018
  ...
# Subtest: wikilink naming validates closed tasks and rejects duplicate target IDs
ok 454 - wikilink naming validates closed tasks and rejects duplicate target IDs
  ---
  duration_ms: 0.830186
  ...
# Subtest: wikilink naming adds an ID to a moved closed task and links the original token
ok 455 - wikilink naming adds an ID to a moved closed task and links the original token
  ---
  duration_ms: 2.167038
  ...
# Subtest: ^^ naming preserves a cross-note target and alias through the final link
ok 456 - ^^ naming preserves a cross-note target and alias through the final link
  ---
  duration_ms: 2.629962
  ...
# Subtest: auto-open only on a written second paren, including auto-pair and closed shapes
ok 457 - auto-open only on a written second paren, including auto-pair and closed shapes
  ---
  duration_ms: 27.298768
  ...
# Subtest: caret-only, undo, and programmatic edits never auto-open
ok 458 - caret-only, undo, and programmatic edits never auto-open
  ---
  duration_ms: 0.450951
  ...
# Subtest: query seeds from the token and keys move, accept, escape, and backspace
ok 459 - query seeds from the token and keys move, accept, escape, and backspace
  ---
  duration_ms: 5.834501
  ...
# Subtest: Backspace undoes closed ((q)) to () and unclosed ((q to (
ok 460 - Backspace undoes closed ((q)) to () and unclosed ((q to (
  ---
  duration_ms: 2.041629
  ...
# Subtest: identified accept splices one transaction, caret after ]], no notice
ok 461 - identified accept splices one transaction, caret after ]], no notice
  ---
  duration_ms: 1.645412
  ...
# Subtest: stale target paths keep the picker open with a Notice
ok 462 - stale target paths keep the picker open with a Notice
  ---
  duration_ms: 1.413249
  ...
# Subtest: command opens on a token, a selection, or the caret
ok 463 - command opens on a token, a selection, or the caret
  ---
  duration_ms: 2.572873
  ...
# Subtest: managed-line (( shows that line's guard notice and never opens
ok 464 - managed-line (( shows that line's guard notice and never opens
  ---
  duration_ms: 0.506908
  ...
# Subtest: command in an excluded context shows Task wikilinks can't go here
ok 465 - command in an excluded context shows Task wikilinks can't go here
  ---
  duration_ms: 0.478775
  ...
# Subtest: ^^ marker still opens the per-note picker when (( is absent
ok 466 - ^^ marker still opens the per-note picker when (( is absent
  ---
  duration_ms: 0.678786
  ...
# Subtest: ID-less Enter opens naming mode with the picker state
ok 467 - ID-less Enter opens naming mode with the picker state
  ---
  duration_ms: 10.301782
  ...
# Subtest: Page Down clamps at the final selectable row instead of wrapping
ok 468 - Page Down clamps at the final selectable row instead of wrapping
  ---
  duration_ms: 14.765636
  ...
# Subtest: naming cancel paths restore query, selection, row limit, and scroll
ok 469 - naming cancel paths restore query, selection, row limit, and scroll
  ---
  duration_ms: 1.594525
  ...
# Subtest: a scan that exits early clears old written ranges before a later scan
ok 470 - a scan that exits early clears old written ranges before a later scan
  ---
  duration_ms: 0.326323
  ...
# Subtest: identified accept dispatches one isolated CodeMirror completion event
ok 471 - identified accept dispatches one isolated CodeMirror completion event
  ---
  duration_ms: 0.740934
  ...
# Subtest: guarded rows never open the naming prompt
ok 472 - guarded rows never open the naming prompt
  ---
  duration_ms: 1.185113
  ...
# Subtest: cheap Pomodoro guards disable non-selected duplicate rows
ok 473 - cheap Pomodoro guards disable non-selected duplicate rows
  ---
  duration_ms: 3.10546
  ...
# Subtest: stale Backspace closes with a notice and leaves the changed token alone
ok 474 - stale Backspace closes with a notice and leaves the changed token alone
  ---
  duration_ms: 0.489344
  ...
# Subtest: onEscapeKey clears a non-empty filter first and closes on an empty one
ok 475 - onEscapeKey clears a non-empty filter first and closes on an empty one
  ---
  duration_ms: 0.794467
  ...
# Subtest: empty filter groups This note, In progress, Next, Other open, Hidden, Completed
ok 476 - empty filter groups This note, In progress, Next, Other open, Hidden, Completed
  ---
  duration_ms: 21.186596
  ...
# Subtest: per-note headers expose sticky data, kind icons, and count pills
ok 477 - per-note headers expose sticky data, kind icons, and count pills
  ---
  duration_ms: 0.954533
  ...
# Subtest: row anatomy, locator parts, and action lines cover identified, id-less, and guarded
ok 478 - row anatomy, locator parts, and action lines cover identified, id-less, and guarded
  ---
  duration_ms: 2.322074
  ...
# Subtest: title parts render code, wikilinks, markdown labels, and URL hosts
ok 479 - title parts render code, wikilinks, markdown labels, and URL hosts
  ---
  duration_ms: 0.475167
  ...
# Subtest: counts, empty states, indexing, and footer hints
ok 480 - counts, empty states, indexing, and footer hints
  ---
  duration_ms: 1.083589
  ...
# Subtest: windowing emits 100-row windows and renderAll exhausts
ok 481 - windowing emits 100-row windows and renderAll exhausts
  ---
  duration_ms: 6.85998
  ...
# Subtest: narrow layout keeps basename plus id and drops the backspace hint
ok 482 - narrow layout keeps basename plus id and drops the backspace hint
  ---
  duration_ms: 0.376309
  ...
# Subtest: filtered list is flat with a Completed history divider
ok 483 - filtered list is flat with a Completed history divider
  ---
  duration_ms: 0.366389
  ...
# Subtest: caret-task and unlinkable-path guards disable the row
ok 484 - caret-task and unlinkable-path guards disable the row
  ---
  duration_ms: 0.602891
  ...
# Subtest: card DOM helpers are exported for Chromium previews
ok 485 - card DOM helpers are exported for Chromium previews
  ---
  duration_ms: 0.357754
  ...
# Subtest: Pomodoro (( picker limits the pool to open tasks and shows commit consequences
ok 486 - Pomodoro (( picker limits the pool to open tasks and shows commit consequences
  ---
  duration_ms: 21.492239
  ...
# Subtest: ^^ under an open Pomodoro raises blocked prerequisites, leaves the task unlinked, and reverts the marker
ok 487 - ^^ under an open Pomodoro raises blocked prerequisites, leaves the task unlinked, and reverts the marker
  ---
  duration_ms: 9.198606
  ...
# Subtest: ^^ refuses a project-blocked task without consuming its prerequisites
ok 488 - ^^ refuses a project-blocked task without consuming its prerequisites
  ---
  duration_ms: 1.333417
  ...
# Subtest: ^^ refuses a closed target under an open Pomodoro
ok 489 - ^^ refuses a closed target under an open Pomodoro
  ---
  duration_ms: 1.08931
  ...
# Subtest: (( refuses a \#prj_is_blocked resident without consuming prerequisites
ok 490 - (( refuses a \#prj_is_blocked resident without consuming prerequisites
  ---
  duration_ms: 1.182458
  ...
# Subtest: (( refuses a task inherited-blocked by its \#prj_is_blocked project
ok 491 - (( refuses a task inherited-blocked by its \#prj_is_blocked project
  ---
  duration_ms: 1.222575
  ...
# Subtest: (( refuses a ^prj whose own future date is the sole remaining reason
ok 492 - (( refuses a ^prj whose own future date is the sole remaining reason
  ---
  duration_ms: 1.18329
  ...
# Subtest: ^^ links and promotes an existing-ID task under an open Pomodoro
ok 493 - ^^ links and promotes an existing-ID task under an open Pomodoro
  ---
  duration_ms: 2.67596
  ...
# Subtest: ID-less ^^ names, links, and retains its target alias in Pomodoro mode
ok 494 - ID-less ^^ names, links, and retains its target alias in Pomodoro mode
  ---
  duration_ms: 1.419711
  ...
# Subtest: an unrelated unreadable note does not block a Ready Pomodoro target
ok 495 - an unrelated unreadable note does not block a Ready Pomodoro target
  ---
  duration_ms: 1.147301
  ...
# Subtest: a ^prj blocked only by its own prerequisite raises that prerequisite
ok 496 - a ^prj blocked only by its own prerequisite raises that prerequisite
  ---
  duration_ms: 0.686631
  ...
# Subtest: Pomodoro prerequisite raise pins every promoted task and selects the first
ok 497 - Pomodoro prerequisite raise pins every promoted task and selects the first
  ---
  duration_ms: 2.223246
  ...
# Subtest: the task wikilink Pomodoro preview omits type text when the themes API is absent
ok 498 - the task wikilink Pomodoro preview omits type text when the themes API is absent
  ---
  duration_ms: 0.304571
  ...
# Subtest: Pomodoro commit rechecks the selected task before writing
ok 499 - Pomodoro commit rechecks the selected task before writing
  ---
  duration_ms: 0.282049
  ...
# Subtest: ID-less (( selection names the task and completes through the shared Pomodoro commit
ok 500 - ID-less (( selection names the task and completes through the shared Pomodoro commit
  ---
  duration_ms: 2.096654
  ...
# Subtest: Pomodoro commit merges the task type into the Pomodoro, pulls a future schedule forward, and includes notices
ok 501 - Pomodoro commit merges the task type into the Pomodoro, pulls a future schedule forward, and includes notices
  ---
  duration_ms: 1.841316
  ...
# Subtest: task-wikilink trigger vectors match bob's shared core
ok 502 - task-wikilink trigger vectors match bob's shared core
  ---
  duration_ms: 3.353554
  ...
# Subtest: task-wikilink context vectors allow prose and exclude note-only spans
ok 503 - task-wikilink context vectors allow prose and exclude note-only spans
  ---
  duration_ms: 3.994258
  ...
# Subtest: task-wikilink written-second-paren vectors gate auto-open on user input
ok 504 - task-wikilink written-second-paren vectors gate auto-open on user input
  ---
  duration_ms: 0.313709
  ...
# Subtest: findTaskWikilinkToken rejects unusable caret positions
ok 505 - findTaskWikilinkToken rejects unusable caret positions
  ---
  duration_ms: 0.124037
  ...
# Subtest: taskWikilinkContextAt rejects unusable positions
ok 506 - taskWikilinkContextAt rejects unusable positions
  ---
  duration_ms: 0.158313
  ...
# Subtest: addTaskWikilinkChanges records insertions and maps earlier ranges forward
ok 507 - addTaskWikilinkChanges records insertions and maps earlier ranges forward
  ---
  duration_ms: 0.381228
  ...
# Subtest: addTaskWikilinkChanges accepts the wrapper and CodeMirror spellings
ok 508 - addTaskWikilinkChanges accepts the wrapper and CodeMirror spellings
  ---
  duration_ms: 0.228557
  ...
# Subtest: mapTaskWikilinkRanges maps without recording
ok 509 - mapTaskWikilinkRanges maps without recording
  ---
  duration_ms: 0.14662
  ...
# Subtest: mapTaskWikilinkRanges tolerates array ranges and empty sets
ok 510 - mapTaskWikilinkRanges tolerates array ranges and empty sets
  ---
  duration_ms: 0.452324
  ...
# Subtest: work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
ok 511 - work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
  ---
  duration_ms: 2.619092
  ...
# Subtest: formatWorkLogStamp matches the shared conformance vectors
ok 512 - formatWorkLogStamp matches the shared conformance vectors
  ---
  duration_ms: 0.374144
  ...
# Subtest: work log stamps use local wall-clock components
ok 513 - work log stamps use local wall-clock components
  ---
  duration_ms: 0.203729
  ...
# Subtest: planWorkLogInsertion stamps the injected clock when no stamp is given
ok 514 - planWorkLogInsertion stamps the injected clock when no stamp is given
  ---
  duration_ms: 0.762426
  ...
# Subtest: workSummaryPromptState previews the clock at render time
ok 515 - workSummaryPromptState previews the clock at render time
  ---
  duration_ms: 0.161649
  ...
# Subtest: successful Work Summary writes add the phrase to nav log recall
ok 516 - successful Work Summary writes add the phrase to nav log recall
  ---
  duration_ms: 0.511667
  ...
# Subtest: planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
ok 517 - planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
  ---
  duration_ms: 0.25642
  ...
# Subtest: planWorkLogInsertion inherits an existing space-indented child prefix
ok 518 - planWorkLogInsertion inherits an existing space-indented child prefix
  ---
  duration_ms: 0.386428
  ...
# Subtest: planWorkLogInsertion inherits an existing tab-indented child prefix
ok 519 - planWorkLogInsertion inherits an existing tab-indented child prefix
  ---
  duration_ms: 0.421615
  ...
# Subtest: planWorkLogInsertion prepends newest-first entries into existing marker spellings
ok 520 - planWorkLogInsertion prepends newest-first entries into existing marker spellings
  ---
  duration_ms: 0.757978
  ...
# Subtest: planWorkLogInsertion ignores nested child-task markers and preserves CRLF
ok 521 - planWorkLogInsertion ignores nested child-task markers and preserves CRLF
  ---
  duration_ms: 0.360669
  ...
# Subtest: planWorkLogInsertion treats blank summaries as no-op structural edits
ok 522 - planWorkLogInsertion treats blank summaries as no-op structural edits
  ---
  duration_ms: 0.112935
  ...
# Subtest: the Open-reset planner is removed: unlink plans only a Work Log insertion
ok 523 - the Open-reset planner is removed: unlink plans only a Work Log insertion
  ---
  duration_ms: 0.088659
  ...
# Subtest: unlink Work Log plan keeps the In Progress checkbox and appends one entry
ok 524 - unlink Work Log plan keeps the In Progress checkbox and appends one entry
  ---
  duration_ms: 0.122865
  ...
# Subtest: article detection accepts scalar and list frontmatter values
ok 525 - article detection accepts scalar and list frontmatter values
  ---
  duration_ms: 1.377931
  ...
# Subtest: bob resolution prefers its setting, then known install paths, then PATH
ok 526 - bob resolution prefers its setting, then known install paths, then PATH
  ---
  duration_ms: 0.703534
  ...
# Subtest: plan decoder accepts v1 and rejects a foreign schema version
ok 527 - plan decoder accepts v1 and rejects a foreign schema version
  ---
  duration_ms: 0.274254
  ...
# Subtest: bob stdin spawn passes the article contract and vault environment
ok 528 - bob stdin spawn passes the article contract and vault environment
  ---
  duration_ms: 2.006371
  ...
# Subtest: bob plan stdout decodes UTF-8 split across chunks
ok 529 - bob plan stdout decodes UTF-8 split across chunks
  ---
  duration_ms: 0.819815
  ...
# Subtest: early bob exit on stdin reports EPIPE as a run failure
ok 530 - early bob exit on stdin reports EPIPE as a run failure
  ---
  duration_ms: 0.663617
  ...
# Subtest: line hunks become minimal cursor-preserving changes
ok 531 - line hunks become minimal cursor-preserving changes
  ---
  duration_ms: 0.57082
  ...
# Subtest: insert, multi-line replace, and deletion hunks reproduce the formatted note
ok 532 - insert, multi-line replace, and deletion hunks reproduce the formatted note
  ---
  duration_ms: 2.725315
  ...
# Subtest: notice shows bob's text and at most two warning findings
ok 533 - notice shows bob's text and at most two warning findings
  ---
  duration_ms: 0.377672
  ...
# Subtest: inbound changes apply only when their target line still matches the preimage
ok 534 - inbound changes apply only when their target line still matches the preimage
  ---
  duration_ms: 0.642697
  ...
# Subtest: undo guard blocks a reformat until a fresh input or delete event
ok 535 - undo guard blocks a reformat until a fresh input or delete event
  ---
  duration_ms: 0.368844
  ...
# Subtest: leave formatting observes the undo guard before saving or reading
ok 536 - leave formatting observes the undo guard before saving or reading
  ---
  duration_ms: 0.314029
  ...
# Subtest: Convert shows bob's refusal on every invocation
ok 537 - Convert shows bob's refusal on every invocation
  ---
  duration_ms: 0.346382
  ...
# Subtest: old bob's non-JSON article response gets one update notice per session
ok 538 - old bob's non-JSON article response gets one update notice per session
  ---
  duration_ms: 0.198149
  ...
# Subtest: format drops its response if the editor changed while bob was running
ok 539 - format drops its response if the editor changed while bob was running
  ---
  duration_ms: 0.290425
  ...
# Subtest: decoration ranges mark written section numbers from the outline
ok 540 - decoration ranges mark written section numbers from the outline
  ---
  duration_ms: 0.726808
  ...
# Subtest: a new outline rerenders each open Reading view once for that generation
ok 541 - a new outline rerenders each open Reading view once for that generation
  ---
  duration_ms: 0.350018
  ...
# Subtest: section at a given line uses the innermost outline range
ok 542 - section at a given line uses the innermost outline range
  ---
  duration_ms: 0.262501
  ...
# Subtest: stale-hint debounce and in-flight state machine
ok 543 - stale-hint debounce and in-flight state machine
  ---
  duration_ms: 0.255398
  ...
# Subtest: reading-view wrapping puts the leading number token in span.bob-secno
ok 544 - reading-view wrapping puts the leading number token in span.bob-secno
  ---
  duration_ms: 0.563035
  ...
# Subtest: applied plans remap outline lines onto the formatted buffer
ok 545 - applied plans remap outline lines onto the formatted buffer
  ---
  duration_ms: 0.132664
  ...
# Subtest: article styles scope the reading look under .bob-article
ok 546 - article styles scope the reading look under .bob-article
  ---
  duration_ms: 0.443577
  ...
# Subtest: look settings default to serif typeface and stale-number hints
ok 547 - look settings default to serif typeface and stale-number hints
  ---
  duration_ms: 0.133876
  ...
# Subtest: catalog carries category and CLDR keywords
ok 548 - catalog carries category and CLDR keywords
  ---
  duration_ms: 4.809263
  ...
# Subtest: tiered ranking regression set
ok 549 - tiered ranking regression set
  ---
  duration_ms: 92.051219
  ...
# Subtest: multi-token AND, boost stays within tier, and VS16-insensitive glyphs
ok 550 - multi-token AND, boost stays within tier, and VS16-insensitive glyphs
  ---
  duration_ms: 30.603269
  ...
# Subtest: suggestForLabel examples
ok 551 - suggestForLabel examples
  ---
  duration_ms: 10.043679
  ...
# Subtest: api v1 is frozen, total, and shares recents
ok 552 - api v1 is frozen, total, and shares recents
  ---
  duration_ms: 23.088419
  ...
# Subtest: api exists without EditorSuggest
ok 553 - api exists without EditorSuggest
  ---
  duration_ms: 9.987752
  ...
# Subtest: generated catalog exactly matches the vendored gemoji database
ok 554 - generated catalog exactly matches the vendored gemoji database
  ---
  duration_ms: 91.366539
  ...
# Subtest: catalog integrity and popular aliases
ok 555 - catalog integrity and popular aliases
  ---
  duration_ms: 3.428006
  ...
# Subtest: query normalization, alias ranking, tags, descriptions, and recents
ok 556 - query normalization, alias ranking, tags, descriptions, and recents
  ---
  duration_ms: 38.047194
  ...
# Subtest: empty query puts newest recents before popular entries and deduplicates
ok 557 - empty query puts newest recents before popular entries and deduplicates
  ---
  duration_ms: 0.496819
  ...
# Subtest: recent history deduplicates by alias and caps at thirty
ok 558 - recent history deduplicates by alias and caps at thirty
  ---
  duration_ms: 3.094389
  ...
# Subtest: renderSuggestion builds styled glyph, shortcode, hint, and match nodes
ok 559 - renderSuggestion builds styled glyph, shortcode, hint, and match nodes
  ---
  duration_ms: 41.307488
  ...
# Subtest: selection replaces the stored range with the emoji, saves recents, and closes
ok 560 - selection replaces the stored range with the emoji, saves recents, and closes
  ---
  duration_ms: 29.637095
  ...
# Subtest: missing and corrupt plugin data reset recents safely; valid recents persist
ok 561 - missing and corrupt plugin data reset recents safely; valid recents persist
  ---
  duration_ms: 51.22647
  ...
# Subtest: trigger opens at line start and after whitespace, including a bare colon
ok 562 - trigger opens at line start and after whitespace, including a bare colon
  ---
  duration_ms: 1.830174
  ...
# Subtest: trigger excludes mid-word, clock, dataview, doubled, and punctuated colons
ok 563 - trigger excludes mid-word, clock, dataview, doubled, and punctuated colons
  ---
  duration_ms: 0.278192
  ...
# Subtest: closing colon remains literal and does not autocommit
ok 564 - closing colon remains literal and does not autocommit
  ---
  duration_ms: 0.121262
  ...
# Subtest: syntax tree guards code, math, comments, and frontmatter
ok 565 - syntax tree guards code, math, comments, and frontmatter
  ---
  duration_ms: 0.296697
  ...
# Subtest: missing or failing syntax APIs allow the trigger
ok 566 - missing or failing syntax APIs allow the trigger
  ---
  duration_ms: 0.343406
  ...
# Subtest: banner date accepts the saved line and the rendered text
ok 567 - banner date accepts the saved line and the rendered text
  ---
  duration_ms: 1.237282
  ...
# Subtest: banner date rejects hostile subjects and malformed dates
ok 568 - banner date rejects hostile subjects and malformed dates
  ---
  duration_ms: 0.21491
  ...
# Subtest: trusted spans need the exact markers in order
ok 569 - trusted spans need the exact markers in order
  ---
  duration_ms: 0.698544
  ...
# Subtest: fake banners without markers and damaged spans stay untrusted
ok 570 - fake banners without markers and damaged spans stay untrusted
  ---
  duration_ms: 0.268904
  ...
# Subtest: unarchive argv pins the exact note behind -- with JSON output
ok 571 - unarchive argv pins the exact note behind -- with JSON output
  ---
  duration_ms: 0.15176
  ...
# Subtest: list decoding maps receipts per note and confirms empty arrays
ok 572 - list decoding maps receipts per note and confirms empty arrays
  ---
  duration_ms: 0.342495
  ...
# Subtest: list decoding never fabricates ownership from malformed rows
ok 573 - list decoding never fabricates ownership from malformed rows
  ---
  duration_ms: 0.215582
  ...
# Subtest: per-note state distinguishes receipts, none, and unavailable
ok 574 - per-note state distinguishes receipts, none, and unavailable
  ---
  duration_ms: 0.227334
  ...
# Subtest: cache refresh coalesces concurrent callers into one list call
ok 575 - cache refresh coalesces concurrent callers into one list call
  ---
  duration_ms: 0.555611
  ...
# Subtest: cache refresh settles old-bob and failures without throwing
ok 576 - cache refresh settles old-bob and failures without throwing
  ---
  duration_ms: 0.553457
  ...
# Subtest: tooltip names the exact count and label, never guesses
ok 577 - tooltip names the exact count and label, never guesses
  ---
  duration_ms: 0.338396
  ...
# Subtest: undo outcomes match the exact note, then input, then a single row
ok 578 - undo outcomes match the exact note, then input, then a single row
  ---
  duration_ms: 0.337595
  ...
# Subtest: banner element uses text APIs and reports clicks once
ok 579 - banner element uses text APIs and reports clicks once
  ---
  duration_ms: 0.500335
  ...
# Subtest: reading view enhances the trusted banner with one undo button
ok 580 - reading view enhances the trusted banner with one undo button
  ---
  duration_ms: 22.851828
  ...
# Subtest: reading view leaves fakes, damage, and non-mail notes inert
ok 581 - reading view leaves fakes, damage, and non-mail notes inert
  ---
  duration_ms: 21.981896
  ...
# Subtest: reading sweep removes the button once the banner is gone
ok 582 - reading sweep removes the button once the banner is gone
  ---
  duration_ms: 21.953582
  ...
# Subtest: banner click runs one exact unarchive, ignores doubles, then reloads state
ok 583 - banner click runs one exact unarchive, ignores doubles, then reloads state
  ---
  duration_ms: 1.294893
  ...
# Subtest: banner click surfaces unchanged and failed outcomes without guessing
ok 584 - banner click surfaces unchanged and failed outcomes without guessing
  ---
  duration_ms: 0.693534
  ...
# Subtest: reading sweep on an unloaded cache fires one coalesced snapshot
ok 585 - reading sweep on an unloaded cache fires one coalesced snapshot
  ---
  duration_ms: 41.015001
  ...
# Subtest: live preview decorates the trusted banner line and nothing else
ok 586 - live preview decorates the trusted banner line and nothing else
  ---
  duration_ms: 1.491609
  ...
# Subtest: live extension registers once and refreshes on the shared effect
ok 587 - live extension registers once and refreshes on the shared effect
  ---
  duration_ms: 0.358134
  ...
# Subtest: shared cache api serves plain JSON for ledger tools
ok 588 - shared cache api serves plain JSON for ledger tools
  ---
  duration_ms: 0.524442
  ...
# Subtest: shared cache api notifies Ledger Tools after a completed snapshot refresh
ok 589 - shared cache api notifies Ledger Tools after a completed snapshot refresh
  ---
  duration_ms: 0.323718
  ...
# Subtest: unload clears banner hosts, views, and pending bits
ok 590 - unload clears banner hosts, views, and pending bits
  ---
  duration_ms: 20.708003
  ...
# Subtest: compose arg builders match the bob gmail CLI contract
ok 591 - compose arg builders match the bob gmail CLI contract
  ---
  duration_ms: 1.48209
  ...
# Subtest: preview and error payload helpers classify bob documents
ok 592 - preview and error payload helpers classify bob documents
  ---
  duration_ms: 1.515183
  ...
# Subtest: the send modal renders the exact preview from fixture JSON
ok 593 - the send modal renders the exact preview from fixture JSON
  ---
  duration_ms: 1.110781
  ...
# Subtest: undo cancels the send before bob is called
ok 594 - undo cancels the send before bob is called
  ---
  duration_ms: 0.793345
  ...
# Subtest: a second send is ignored while one is in flight, and the digest passes through
ok 595 - a second send is ignored while one is in flight, and the digest passes through
  ---
  duration_ms: 5.258662
  ...
# Subtest: a digest mismatch re-previews instead of sending
ok 596 - a digest mismatch re-previews instead of sending
  ---
  duration_ms: 0.48709
  ...
# Subtest: the send modal ignores a double click on Send
ok 597 - the send modal ignores a double click on Send
  ---
  duration_ms: 1.653538
  ...
# Subtest: compose commands appear only with a mail-note context, except New email
ok 598 - compose commands appear only with a mail-note context, except New email
  ---
  duration_ms: 1.195633
  ...
# Subtest: picker insertion uses a rechecked editor transaction and aborts stale buffers
ok 599 - picker insertion uses a rechecked editor transaction and aborts stale buffers
  ---
  duration_ms: 2.263863
  ...
# Subtest: paste conversion replaces only an unchanged Gmail URL in the original view and file
ok 600 - paste conversion replaces only an unchanged Gmail URL in the original view and file
  ---
  duration_ms: 0.657336
  ...
# Subtest: a failed save leaves a pasted Gmail URL untouched
ok 601 - a failed save leaves a pasted Gmail URL untouched
  ---
  duration_ms: 0.420824
  ...
# Subtest: old Bob shows one update notice
ok 602 - old Bob shows one update notice
  ---
  duration_ms: 0.782575
  ...
# Subtest: commands appear according to mail-note context
ok 603 - commands appear according to mail-note context
  ---
  duration_ms: 1.372651
  ...
# Subtest: a mail URL under the cursor exposes the email context
ok 604 - a mail URL under the cursor exposes the email context
  ---
  duration_ms: 0.375237
  ...
# Subtest: line-borne context works anywhere on the line and ignores task status
ok 605 - line-borne context works anywhere on the line and ignores task status
  ---
  duration_ms: 0.622939
  ...
# Subtest: child hop opens from the task row through a link-only child
ok 606 - child hop opens from the task row through a link-only child
  ---
  duration_ms: 0.462824
  ...
# Subtest: code, non-mail links, and bad URLs stay silent
ok 607 - code, non-mail links, and bad URLs stay silent
  ---
  duration_ms: 0.592181
  ...
# Subtest: first mail link wins and own links beat the child hop
ok 608 - first mail link wins and own links beat the child hop
  ---
  duration_ms: 0.517708
  ...
# Subtest: inside a mail note the whole-note fallback still opens
ok 609 - inside a mail note the whole-note fallback still opens
  ---
  duration_ms: 0.187829
  ...
# Subtest: vim Cmd+Enter mapping registers once and opens exactly gmail_url
ok 610 - vim Cmd+Enter mapping registers once and opens exactly gmail_url
  ---
  duration_ms: 0.798696
  ...
# Subtest: vim registration fails closed without an adapter
ok 611 - vim registration fails closed without an adapter
  ---
  duration_ms: 0.112204
  ...
# Subtest: task links point to the message block under the cursor
ok 612 - task links point to the message block under the cursor
  ---
  duration_ms: 0.356971
  ...
# Subtest: task-link hop opens the Gmail thread from the daily-note bullet
ok 613 - task-link hop opens the Gmail thread from the daily-note bullet
  ---
  duration_ms: 0.557946
  ...
# Subtest: task-link hop rejects multi-link, embed, struck, and non-gmail targets
ok 614 - task-link hop rejects multi-link, embed, struck, and non-gmail targets
  ---
  duration_ms: 1.173401
  ...
# Subtest: task-link hop supports hop-then-child-hop targets
ok 615 - task-link hop supports hop-then-child-hop targets
  ---
  duration_ms: 0.207897
  ...
# Subtest: mailOpen api v1 opens at the cursor and degrades to false
ok 616 - mailOpen api v1 opens at the cursor and degrades to false
  ---
  duration_ms: 0.491439
  ...
# Subtest: Edit album schema is a Vault surface row behind the palette command
ok 617 - Edit album schema is a Vault surface row behind the palette command
  ---
  duration_ms: 0.967057
  ...
# Subtest: missing plugin disables the surface row with an enable hint
ok 618 - missing plugin disables the surface row with an enable hint
  ---
  duration_ms: 1.204911
  ...
# Subtest: Command Mode executes the album schema surface through Obsidian's command route
ok 619 - Command Mode executes the album schema surface through Obsidian's command route
  ---
  duration_ms: 0.878247
  ...
# Subtest: typed argv tokenizer handles quotes, escapes, literal shell syntax, and errors
ok 620 - typed argv tokenizer handles quotes, escapes, literal shell syntax, and errors
  ---
  duration_ms: 1.561201
  ...
# Subtest: typed argv resolves aliases to the longest catalog entry and refuses excluded paths
ok 621 - typed argv resolves aliases to the longest catalog entry and refuses excluded paths
  ---
  duration_ms: 0.69113
  ...
# Subtest: the list pins typed metadata, disabled exclusions, and the explicit Vim fallback
ok 622 - the list pins typed metadata, disabled exclusions, and the explicit Vim fallback
  ---
  duration_ms: 9.386976
  ...
# Subtest: typed runs pass the catalog title to the run record
ok 623 - typed runs pass the catalog title to the run record
  ---
  duration_ms: 2.850563
  ...
# Subtest: Vim-shaped input follows the agreed positive and negative rules
ok 624 - Vim-shaped input follows the agreed positive and negative rules
  ---
  duration_ms: 0.187948
  ...
# Subtest: vimrc parser finds recursive colon mappings and exmap names
ok 625 - vimrc parser finds recursive colon mappings and exmap names
  ---
  duration_ms: 0.423078
  ...
# Subtest: argument completion passes the entry path, fixed args, and current tokens to bob
ok 626 - argument completion passes the entry path, fixed args, and current tokens to bob
  ---
  duration_ms: 4.474856
  ...
# Subtest: completion directives group candidates, preserve prefixes, and expand vault paths
ok 627 - completion directives group candidates, preserve prefixes, and expand vault paths
  ---
  duration_ms: 8.801066
  ...
# Subtest: stale completion replies are discarded and Enter reports missing required positionals
ok 628 - stale completion replies are discarded and Enter reports missing required positionals
  ---
  duration_ms: 5.522806
  ...
# Subtest: argument completion requests debounce edits by 60 ms
ok 629 - argument completion requests debounce edits by 60 ms
  ---
  duration_ms: 83.650687
  ...
# Subtest: Vim ex dispatch restores and targets the editor captured when the sheet opened
ok 630 - Vim ex dispatch restores and targets the editor captured when the sheet opened
  ---
  duration_ms: 4.530571
  ...
# Subtest: double colon enters Vim stage and Escape returns to the list
ok 631 - double colon enters Vim stage and Escape returns to the list
  ---
  duration_ms: 4.324808
  ...
# Subtest: vimrc lint reads the configured file and shows only one session notice
ok 632 - vimrc lint reads the configured file and shows only one session notice
  ---
  duration_ms: 0.74865
  ...
# Subtest: Edit bank setup is a Vault surface row behind the palette command
ok 633 - Edit bank setup is a Vault surface row behind the palette command
  ---
  duration_ms: 1.152551
  ...
# Subtest: missing ledger-tools plugin disables Edit bank setup with an enable hint
ok 634 - missing ledger-tools plugin disables Edit bank setup with an enable hint
  ---
  duration_ms: 1.268582
  ...
# Subtest: Command Mode runs Edit bank setup through Obsidian's command route
ok 635 - Command Mode runs Edit bank setup through Obsidian's command route
  ---
  duration_ms: 1.094681
  ...
# Subtest: fingerprints compare path, mtime, and size
ok 636 - fingerprints compare path, mtime, and size
  ---
  duration_ms: 2.127202
  ...
# Subtest: validation accepts the fixture and rejects malformed catalogs
ok 637 - validation accepts the fixture and rejects malformed catalogs
  ---
  duration_ms: 0.353725
  ...
# Subtest: refresh fetches and validates through the real protocol
ok 638 - refresh fetches and validates through the real protocol
  ---
  duration_ms: 67.040378
  ...
# Subtest: lookup resolves entries, aliases of entries, and excluded paths
ok 639 - lookup resolves entries, aliases of entries, and excluded paths
  ---
  duration_ms: 0.514452
  ...
# Subtest: argv assembly puts preview args before fixed args
ok 640 - argv assembly puts preview args before fixed args
  ---
  duration_ms: 0.418749
  ...
# Subtest: cmRecordArgs strips a leading bob binary and leaves queued argv
ok 641 - cmRecordArgs strips a leading bob binary and leaves queued argv
  ---
  duration_ms: 0.525674
  ...
# Subtest: cmReplayRun is the inverse of cmAssembleArgv
ok 642 - cmReplayRun is the inverse of cmAssembleArgv
  ---
  duration_ms: 0.664469
  ...
# Subtest: palette entries need policy run and all-optional positionals
ok 643 - palette entries need policy run and all-optional positionals
  ---
  duration_ms: 0.232724
  ...
# Subtest: classification order: stop, spawn, timeout, signal
ok 644 - classification order: stop, spawn, timeout, signal
  ---
  duration_ms: 1.771473
  ...
# Subtest: lock phrase wins over exit codes and adapters
ok 645 - lock phrase wins over exit codes and adapters
  ---
  duration_ms: 0.234738
  ...
# Subtest: exit-code hints beat the generic rule; unknown ids are ignored
ok 646 - exit-code hints beat the generic rule; unknown ids are ignored
  ---
  duration_ms: 0.175064
  ...
# Subtest: adapters adjust the result; failures stay honest
ok 647 - adapters adjust the result; failures stay honest
  ---
  duration_ms: 1.053712
  ...
# Subtest: gcal-sync summarizes added Event Tasks, context, and MEET links
ok 648 - gcal-sync summarizes added Event Tasks, context, and MEET links
  ---
  duration_ms: 0.381218
  ...
# Subtest: gcal-sync reports unchanged and waiting outcomes
ok 649 - gcal-sync reports unchanged and waiting outcomes
  ---
  duration_ms: 0.268543
  ...
# Subtest: api.commandMode settles, never rejects, and fires the workspace event
ok 650 - api.commandMode settles, never rejects, and fires the workspace event
  ---
  duration_ms: 118.569878
  ...
# Subtest: plugin onload registers run-* commands and exposes the frozen api
ok 651 - plugin onload registers run-* commands and exposes the frozen api
  ---
  duration_ms: 32.697859
  ...
# Subtest: plugin reports missing-bob when the binary is absent
ok 652 - plugin reports missing-bob when the binary is absent
  ---
  duration_ms: 0.932721
  ...
# Subtest: runner notifies with a plain summary after each finish
ok 653 - runner notifies with a plain summary after each finish
  ---
  duration_ms: 1.847618
  ...
# Subtest: catalog outcome adapters cover command-specific results and actions
ok 654 - catalog outcome adapters cover command-specific results and actions
  ---
  duration_ms: 1.819063
  ...
# Subtest: toast classes have distinct timing and newer failures replace older cards
ok 655 - toast classes have distinct timing and newer failures replace older cards
  ---
  duration_ms: 1.934364
  ...
# Subtest: status chip waits 400 ms, tracks multiple runs, and marks overdue writers
ok 656 - status chip waits 400 ms, tracks multiple runs, and marks overdue writers
  ---
  duration_ms: 1.316063
  ...
# Subtest: OS notifications only fire for long runs while Obsidian is unfocused
ok 657 - OS notifications only fire for long runs while Obsidian is unfocused
  ---
  duration_ms: 1.761624
  ...
# Subtest: rerun-last preserves arguments and preview mode; Apply carries the replay seed
ok 658 - rerun-last preserves arguments and preview mode; Apply carries the replay seed
  ---
  duration_ms: 0.546604
  ...
# Subtest: commandModeRerun retries an applied preview-first run and Apply carries the seed
ok 659 - commandModeRerun retries an applied preview-first run and Apply carries the seed
  ---
  duration_ms: 736.705115
  ...
# Subtest: ANSI parsing keeps SGR that splits across chunks
ok 660 - ANSI parsing keeps SGR that splits across chunks
  ---
  duration_ms: 2.421173
  ...
# Subtest: linkify positives resolve and negatives stay plain
ok 661 - linkify positives resolve and negatives stay plain
  ---
  duration_ms: 0.951788
  ...
# Subtest: JSON pretty-print mutes keys on a single document
ok 662 - JSON pretty-print mutes keys on a single document
  ---
  duration_ms: 0.837319
  ...
# Subtest: interleave replay preserves arrival order for copy
ok 663 - interleave replay preserves arrival order for copy
  ---
  duration_ms: 0.671092
  ...
# Subtest: stamped sequence runs add a step label to the pager header
ok 664 - stamped sequence runs add a step label to the pager header
  ---
  duration_ms: 1.723772
  ...
# Subtest: pager keys: scroll, wrap, search, copy, history, stop, close
ok 665 - pager keys: scroll, wrap, search, copy, history, stop, close
  ---
  duration_ms: 0.585428
  ...
# Subtest: history stepping is newest-first
ok 666 - history stepping is newest-first
  ---
  duration_ms: 0.161488
  ...
# Subtest: search matches are exact and advance
ok 667 - search matches are exact and advance
  ---
  duration_ms: 0.173331
  ...
# Subtest: status pill covers running, outcomes, and queued-behind
ok 668 - status pill covers running, outcomes, and queued-behind
  ---
  duration_ms: 0.406126
  ...
# Subtest: plugin pager opens from Output, show-last-output, history, copy, and stop
ok 669 - plugin pager opens from Output, show-last-output, history, copy, and stop
  ---
  duration_ms: 16.974424
  ...
# Subtest: writer stop needs confirmation; reads stop immediately
ok 670 - writer stop needs confirmation; reads stop immediately
  ---
  duration_ms: 2.389723
  ...
# Subtest: watching a run skips the toast
ok 671 - watching a run skips the toast
  ---
  duration_ms: 1.412007
  ...
# Subtest: pretty JSON and ANSI land in the pager body
ok 672 - pretty JSON and ANSI land in the pager body
  ---
  duration_ms: 1.070935
  ...
# Subtest: Edit record is a Vault surface row behind the palette command
ok 673 - Edit record is a Vault surface row behind the palette command
  ---
  duration_ms: 1.346351
  ...
# Subtest: missing ledger-tools plugin disables Edit record with an enable hint
ok 674 - missing ledger-tools plugin disables Edit record with an enable hint
  ---
  duration_ms: 1.445791
  ...
# Subtest: Command Mode runs Edit record through Obsidian's command route
ok 675 - Command Mode runs Edit record through Obsidian's command route
  ---
  duration_ms: 1.212445
  ...
# Subtest: resolver prefers the explicit setting and expands home
ok 676 - resolver prefers the explicit setting and expands home
  ---
  duration_ms: 2.531354
  ...
# Subtest: resolver consults ledger-tools before the candidates
ok 677 - resolver consults ledger-tools before the candidates
  ---
  duration_ms: 0.275767
  ...
# Subtest: resolver walks candidates, records every path tried, then PATH
ok 678 - resolver walks candidates, records every path tried, then PATH
  ---
  duration_ms: 0.306826
  ...
# Subtest: child env points at the vault, honors features, and drops completion vars
ok 679 - child env points at the vault, honors features, and drops completion vars
  ---
  duration_ms: 0.509383
  ...
# Subtest: inherited NO_COLOR wins; without the color feature NO_COLOR is set
ok 680 - inherited NO_COLOR wins; without the color feature NO_COLOR is set
  ---
  duration_ms: 0.230189
  ...
# Subtest: vault base requires a local folder
ok 681 - vault base requires a local folder
  ---
  duration_ms: 0.215572
  ...
# Subtest: ansi stripping, quoting, durations, and run ids
ok 682 - ansi stripping, quoting, durations, and run ids
  ---
  duration_ms: 0.901271
  ...
# Subtest: completed read writes files, receipt, and an honest record
ok 683 - completed read writes files, receipt, and an honest record
  ---
  duration_ms: 132.682847
  ...
# Subtest: child env carries vault, features, receipt, and tool paths
ok 684 - child env carries vault, features, receipt, and tool paths
  ---
  duration_ms: 138.402297
  ...
# Subtest: literal args with spaces, quotes, and $() stay literal
ok 685 - literal args with spaces, quotes, and $() stay literal
  ---
  duration_ms: 194.397845
  ...
# Subtest: split multi-byte characters survive and big output stays intact
ok 686 - split multi-byte characters survive and big output stays intact
  ---
  duration_ms: 705.447497
  ...
# Subtest: in-memory text truncates past the cap while files keep everything
ok 687 - in-memory text truncates past the cap while files keep everything
  ---
  duration_ms: 118.647455
  ...
# Subtest: a double run is one run: duplicates share the settlement
ok 688 - a double run is one run: duplicates share the settlement
  ---
  duration_ms: 703.653642
  ...
# Subtest: writers serialize FIFO while reads run in parallel
ok 689 - writers serialize FIFO while reads run in parallel
  ---
  duration_ms: 3507.050613
  ...
# Subtest: a failed save refuses the writer
ok 690 - a failed save refuses the writer
  ---
  duration_ms: 1.658177
  ...
# Subtest: read budgets kill; writer budgets mark overdue; stop stops
ok 691 - read budgets kill; writer budgets mark overdue; stop stops
  ---
  duration_ms: 7119.80683
  ...
# Subtest: failures classify: non-zero, signals, lock, and missing bob
ok 692 - failures classify: non-zero, signals, lock, and missing bob
  ---
  duration_ms: 4066.363851
  ...
# Subtest: policy and entry guards refuse with reasons
ok 693 - policy and entry guards refuse with reasons
  ---
  duration_ms: 970.040527
  ...
# Subtest: retention keeps the newest fifty and never an unfinished run
ok 694 - retention keeps the newest fifty and never an unfinished run
  ---
  duration_ms: 355.543283
  ...
# Subtest: adoption finalizes from receipts and reports unknown without one
ok 695 - adoption finalizes from receipts and reports unknown without one
  ---
  duration_ms: 15.78919
  ...
# Subtest: cmNewRecord copies a sanitized sequence stamp and omits the field otherwise
ok 696 - cmNewRecord copies a sanitized sequence stamp and omits the field otherwise
  ---
  duration_ms: 2.297738
  ...
# Subtest: step display, title, copy text, guards, continues, and focus run
ok 697 - step display, title, copy text, guards, continues, and focus run
  ---
  duration_ms: 1.189291
  ...
# Subtest: history groups by id, newest record per index wins, and states include interrupted
ok 698 - history groups by id, newest record per index wins, and states include interrupted
  ---
  duration_ms: 0.962067
  ...
# Subtest: cmRunSequence runs reads in order, stamps every record, and survives throwing hooks
ok 699 - cmRunSequence runs reads in order, stamps every record, and survives throwing hooks
  ---
  duration_ms: 576.152812
  ...
# Subtest: a failing step 2 halts the sequence and skips later steps
ok 700 - a failing step 2 halts the sequence and skips later steps
  ---
  duration_ms: 968.407066
  ...
# Subtest: attention continues the sequence
ok 701 - attention continues the sequence
  ---
  duration_ms: 5728.229007
  ...
# Subtest: an early saveAllMarkdown refusal halts with its reason
ok 702 - an early saveAllMarkdown refusal halts with its reason
  ---
  duration_ms: 3645.474153
  ...
# Subtest: a stale entry_id falls back to argv
ok 703 - a stale entry_id falls back to argv
  ---
  duration_ms: 1948.84103
  ...
# Subtest: resume reuses the id and history folds into one group
ok 704 - resume reuses the id and history folds into one group
  ---
  duration_ms: 5563.615324
  ...
# Subtest: cancelled() stops before the next step
ok 705 - cancelled() stops before the next step
  ---
  duration_ms: 706.135303
  ...
# Subtest: plugin suppresses per-step toasts and skips chip settle for an active sequence
ok 706 - plugin suppresses per-step toasts and skips chip settle for an active sequence
  ---
  duration_ms: 472.240453
  ...
# Subtest: duplicate signatures are refused and rerun-last replays a stamped newest record
ok 707 - duplicate signatures are refused and rerun-last replays a stamped newest record
  ---
  duration_ms: 815.772603
  ...
# Subtest: rerun-last command callback points at commandModeRerunLast
ok 708 - rerun-last command callback points at commandModeRerunLast
  ---
  duration_ms: 8.983845
  ...
# Subtest: summary model covers completed, attention, halted, and stopped sequences
ok 709 - summary model covers completed, attention, halted, and stopped sequences
  ---
  duration_ms: 3.991382
  ...
# Subtest: summary card renders accessible rows and routes the body to its focus run
ok 710 - summary card renders accessible rows and routes the body to its focus run
  ---
  duration_ms: 0.934274
  ...
# Subtest: resume keeps the sequence id and skips completed steps; rerun gets a new id
ok 711 - resume keeps the sequence id and skips completed steps; rerun gets a new id
  ---
  duration_ms: 2.113706
  ...
# Subtest: Output opens the focus run and Copy writes the sequence shell line
ok 712 - Output opens the focus run and Copy writes the sequence shell line
  ---
  duration_ms: 0.532457
  ...
# Subtest: a repeated sticky sequence card replaces the previous card by signature
ok 713 - a repeated sticky sequence card replaces the previous card by signature
  ---
  duration_ms: 0.81172
  ...
# Subtest: three Ctrl+N presses move three rows, keep focus, and wrap
ok 714 - three Ctrl+N presses move three rows, keep focus, and wrap
  ---
  duration_ms: 19.425915
  ...
# Subtest: Caps Lock and layout variants navigate; Ctrl+Shift+N does not
ok 715 - Caps Lock and layout variants navigate; Ctrl+Shift+N does not
  ---
  duration_ms: 7.319988
  ...
# Subtest: Ctrl+[ matches Escape in list, args, vim, confirm, and output
ok 716 - Ctrl+[ matches Escape in list, args, vim, confirm, and output
  ---
  duration_ms: 9.844559
  ...
# Subtest: standalone pager Ctrl+[ behaves like Escape
ok 717 - standalone pager Ctrl+[ behaves like Escape
  ---
  duration_ms: 1.161508
  ...
# Subtest: focus and caret survive re-renders with scroll preserved on same query
ok 718 - focus and caret survive re-renders with scroll preserved on same query
  ---
  duration_ms: 3.520913
  ...
# Subtest: argument mode walks rendered order and Tab accepts the visible first row
ok 719 - argument mode walks rendered order and Tab accepts the visible first row
  ---
  duration_ms: 3.684857
  ...
# Subtest: Tab enters argument mode from entry and typed rows through the modal keydown listener
ok 720 - Tab enters argument mode from entry and typed rows through the modal keydown listener
  ---
  duration_ms: 3.248042
  ...
# Subtest: Tab on an eligible single-run RECENT row prefills its recorded arguments
ok 721 - Tab on an eligible single-run RECENT row prefills its recorded arguments
  ---
  duration_ms: 4.066956
  ...
# Subtest: Tab hints on surfaces, plain rows, sequence recents, and unmapped recents
ok 722 - Tab hints on surfaces, plain rows, sequence recents, and unmapped recents
  ---
  duration_ms: 30.38395
  ...
# Subtest: row mousedown is defaultPrevented and scope fallback routes body keys once
ok 723 - row mousedown is defaultPrevented and scope fallback routes body keys once
  ---
  duration_ms: 4.516605
  ...
# Subtest: Ctrl+M marks with Caps Lock and layout; Ctrl+Shift+M is ignored
ok 724 - Ctrl+M marks with Caps Lock and layout; Ctrl+Shift+M is ignored
  ---
  duration_ms: 12.618686
  ...
# Subtest: Ctrl+[ clears pending marks like Escape
ok 725 - Ctrl+[ clears pending marks like Escape
  ---
  duration_ms: 4.06937
  ...
# Subtest: empty query walks every row with unique keys and survives a type-and-clear
ok 726 - empty query walks every row with unique keys and survives a type-and-clear
  ---
  duration_ms: 90.694767
  ...
# Subtest: production sheet render and clicks use real DOM APIs
ok 727 - production sheet render and clicks use real DOM APIs
  ---
  duration_ms: 3046.841813
  ...
# Subtest: marking, toggling, and renumbering
ok 728 - marking, toggling, and renumbering
  ---
  duration_ms: 24.384594
  ...
# Subtest: the badge and tray text
ok 729 - the badge and tray text
  ---
  duration_ms: 10.943888
  ...
# Subtest: query select-all after a mark
ok 730 - query select-all after a mark
  ---
  duration_ms: 4.855942
  ...
# Subtest: each refusal reason
ok 731 - each refusal reason
  ---
  duration_ms: 5.611575
  ...
# Subtest: Ctrl+M into argument mode, then marking from it
ok 732 - Ctrl+M into argument mode, then marking from it
  ---
  duration_ms: 4.673194
  ...
# Subtest: argument mode Ctrl+M with incomplete args shows Needs
ok 733 - argument mode Ctrl+M with incomplete args shows Needs
  ---
  duration_ms: 3.475217
  ...
# Subtest: Backspace pops the last step
ok 734 - Backspace pops the last step
  ---
  duration_ms: 13.566657
  ...
# Subtest: Esc first clears marks, second closes
ok 735 - Esc first clears marks, second closes
  ---
  duration_ms: 10.564744
  ...
# Subtest: click and Ctrl+click toggles
ok 736 - click and Ctrl+click toggles
  ---
  duration_ms: 11.932576
  ...
# Subtest: Shift+Enter with marks runs nothing
ok 737 - Shift+Enter with marks runs nothing
  ---
  duration_ms: 9.001218
  ...
# Subtest: one mark activates like Enter
ok 738 - one mark activates like Enter
  ---
  duration_ms: 161.438156
  ...
# Subtest: one confirm mark opens its card
ok 739 - one confirm mark opens its card
  ---
  duration_ms: 5.239866
  ...
# Subtest: Enter with unguarded steps closes and runs
ok 740 - Enter with unguarded steps closes and runs
  ---
  duration_ms: 9.327051
  ...
# Subtest: Enter with guards shows the review card
ok 741 - Enter with guards shows the review card
  ---
  duration_ms: 10.924161
  ...
# Subtest: Ctrl+Enter skips the card
ok 742 - Ctrl+Enter skips the card
  ---
  duration_ms: 17.358377
  ...
# Subtest: argument-mode add and run
ok 743 - argument-mode add and run
  ---
  duration_ms: 37.63136
  ...
# Subtest: the already-running hint
ok 744 - the already-running hint
  ---
  duration_ms: 30.178198
  ...
# Subtest: RECENT grouping folds one sequence into one row
ok 745 - RECENT grouping folds one sequence into one row
  ---
  duration_ms: 1.652837
  ...
# Subtest: RECENT dedupe, limit, interrupted glyph, and about lines
ok 746 - RECENT dedupe, limit, interrupted glyph, and about lines
  ---
  duration_ms: 1.63911
  ...
# Subtest: RECENT Enter reruns all steps and Ctrl+M loads and unloads them
ok 747 - RECENT Enter reruns all steps and Ctrl+M loads and unloads them
  ---
  duration_ms: 43.004108
  ...
# Subtest: clicking a descendant toggles while marks are pending
ok 748 - clicking a descendant toggles while marks are pending
  ---
  duration_ms: 11.926435
  ...
# Subtest: no-mark argument Shift+Enter still previews
ok 749 - no-mark argument Shift+Enter still previews
  ---
  duration_ms: 4.619271
  ...
# Subtest: marked argument Ctrl+Enter with a highlighted completion adds and runs now
ok 750 - marked argument Ctrl+Enter with a highlighted completion adds and runs now
  ---
  duration_ms: 31.761181
  ...
# Subtest: incomplete marked arguments leave marks and show the missing positional
ok 751 - incomplete marked arguments leave marks and show the missing positional
  ---
  duration_ms: 10.753445
  ...
# Subtest: a RECENT sequence reduced to one report uses the normal activation chain
ok 752 - a RECENT sequence reduced to one report uses the normal activation chain
  ---
  duration_ms: 179.608253
  ...
# Subtest: a RECENT sequence reduced to one confirm opens its card
ok 753 - a RECENT sequence reduced to one confirm opens its card
  ---
  duration_ms: 13.729988
  ...
# Subtest: a RECENT sequence reduced to one preview-first command previews
ok 754 - a RECENT sequence reduced to one preview-first command previews
  ---
  duration_ms: 229.477823
  ...
# Subtest: rebuildRows passes live sequence ids so a running sequence shows ⟳
ok 755 - rebuildRows passes live sequence ids so a running sequence shows ⟳
  ---
  duration_ms: 15.310777
  ...
# Subtest: an active sequence refuses a duplicate rerun without closing the sheet
ok 756 - an active sequence refuses a duplicate rerun without closing the sheet
  ---
  duration_ms: 39.147485
  ...
# Subtest: an incomplete sequence with no active id stays interrupted after reload
ok 757 - an incomplete sequence with no active id stays interrupted after reload
  ---
  duration_ms: 0.464106
  ...
# Subtest: fuzzy ranking matches every token and prefers paths, prefixes, and keywords
ok 758 - fuzzy ranking matches every token and prefers paths, prefixes, and keywords
  ---
  duration_ms: 3.403589
  ...
# Subtest: bare capture has no row but named capture rows keep theirs
ok 759 - bare capture has no row but named capture rows keep theirs
  ---
  duration_ms: 1.417547
  ...
# Subtest: unavailable rows stay visible with reasons
ok 760 - unavailable rows stay visible with reasons
  ---
  duration_ms: 0.527497
  ...
# Subtest: frecency weights recent runs and the last-ten window
ok 761 - frecency weights recent runs and the last-ten window
  ---
  duration_ms: 1.032461
  ...
# Subtest: context rows fill For this note and From clipboard
ok 762 - context rows fill For this note and From clipboard
  ---
  duration_ms: 1.08944
  ...
# Subtest: note kinds follow frontmatter type with the article rule
ok 763 - note kinds follow frontmatter type with the article rule
  ---
  duration_ms: 0.226593
  ...
# Subtest: empty query groups RECENT, note, clipboard, then catalog sections
ok 764 - empty query groups RECENT, note, clipboard, then catalog sections
  ---
  duration_ms: 0.559348
  ...
# Subtest: list keys map to intents and plain text stays unhandled
ok 765 - list keys map to intents and plain text stays unhandled
  ---
  duration_ms: 0.331974
  ...
# Subtest: help argv targets the selected row or bare bob
ok 766 - help argv targets the selected row or bare bob
  ---
  duration_ms: 0.396647
  ...
# Subtest: median duration hides fast rows under the two-second floor
ok 767 - median duration hides fast rows under the two-second floor
  ---
  duration_ms: 0.557375
  ...
# Subtest: the open command focuses an already-open sheet
ok 768 - the open command focuses an already-open sheet
  ---
  duration_ms: 8.528015
  ...
# Subtest: Enter on a report row streams it in the sheet output stage
ok 769 - Enter on a report row streams it in the sheet output stage
  ---
  duration_ms: 125.234675
  ...
# Subtest: report footer shows its running line until the output opens
ok 770 - report footer shows its running line until the output opens
  ---
  duration_ms: 8.468209
  ...
# Subtest: preview footer shows a running line while the preview is pending
ok 771 - preview footer shows a running line while the preview is pending
  ---
  duration_ms: 9.166855
  ...
# Subtest: help start failure replaces its running line with the warning hint
ok 772 - help start failure replaces its running line with the warning hint
  ---
  duration_ms: 6.559646
  ...
# Subtest: a rejected sheet run clears the running line before propagating
ok 773 - a rejected sheet run clears the running line before propagating
  ---
  duration_ms: 10.837455
  ...
# Subtest: confirm rows need Ctrl+Enter and run confirmed
ok 774 - confirm rows need Ctrl+Enter and run confirmed
  ---
  duration_ms: 227.402109
  ...
# Subtest: Shift+Enter previews first and Apply reruns without the preview flag
ok 775 - Shift+Enter previews first and Apply reruns without the preview flag
  ---
  duration_ms: 544.52159
  ...
# Subtest: api.preview opens the sheet into a preview-first row's preview stage
ok 776 - api.preview opens the sheet into a preview-first row's preview stage
  ---
  duration_ms: 1464.41725
  ...
# Subtest: api.preview opens a report row in the output stage
ok 777 - api.preview opens a report row in the output stage
  ---
  duration_ms: 411.162984
  ...
# Subtest: api.preview refuses excluded, unknown, unapplied-write, and unavailable rows
ok 778 - api.preview refuses excluded, unknown, unapplied-write, and unavailable rows
  ---
  duration_ms: 2.518369
  ...
# Subtest: api.preview focuses an already-open sheet and replaces its stage
ok 779 - api.preview focuses an already-open sheet and replaces its stage
  ---
  duration_ms: 1854.10269
  ...
# Subtest: missing positionals enter argument mode instead of running
ok 780 - missing positionals enter argument mode instead of running
  ---
  duration_ms: 14.231125
  ...
# Subtest: a trailing ? runs help for the selected row in the output stage
ok 781 - a trailing ? runs help for the selected row in the output stage
  ---
  duration_ms: 2118.200753
  ...
# Subtest: watching the sheet output suppresses the finish toast
ok 782 - watching the sheet output suppresses the finish toast
  ---
  duration_ms: 3613.565219
  ...
# Subtest: unavailable rows never activate
ok 783 - unavailable rows never activate
  ---
  duration_ms: 4.617167
  ...
# Subtest: RECENT rows drop the bob binary and keep unique keys
ok 784 - RECENT rows drop the bob binary and keep unique keys
  ---
  duration_ms: 4.169653
  ...
# Subtest: RECENT vault-sync reruns without doubling the path
ok 785 - RECENT vault-sync reruns without doubling the path
  ---
  duration_ms: 4209.006888
  ...
# Subtest: two RECENT rows for one entry select one at a time
ok 786 - two RECENT rows for one entry select one at a time
  ---
  duration_ms: 2967.426207
  ...
# Subtest: RECENT preview-first and confirm rows honor their guards
ok 787 - RECENT preview-first and confirm rows honor their guards
  ---
  duration_ms: 2427.500155
  ...
# Subtest: in-sheet r reruns vault-sync without doubling the path
ok 788 - in-sheet r reruns vault-sync without doubling the path
  ---
  duration_ms: 307.968777
  ...
# Subtest: hidden below 400 ms, and never settles for such runs
ok 789 - hidden below 400 ms, and never settles for such runs
  ---
  duration_ms: 1.876493
  ...
# Subtest: running keeps one mark element, brand label, tabular clock, and native tooltip
ok 790 - running keeps one mark element, brand label, tabular clock, and native tooltip
  ---
  duration_ms: 1.100241
  ...
# Subtest: two runs show count, longest clock, and click opens the newest
ok 791 - two runs show count, longest clock, and click opens the newest
  ---
  duration_ms: 0.781863
  ...
# Subtest: queued-only gives is-queued and overdue writer gives is-overdue with budget tooltip
ok 792 - queued-only gives is-queued and overdue writer gives is-overdue with budget tooltip
  ---
  duration_ms: 0.531895
  ...
# Subtest: settle shows outcome glyph for 1600 ms, then leaving, then hidden
ok 793 - settle shows outcome glyph for 1600 ms, then leaving, then hidden
  ---
  duration_ms: 0.619813
  ...
# Subtest: sequence model shows step, sequence clock, tooltip, and between-step visibility
ok 794 - sequence model shows step, sequence clock, tooltip, and between-step visibility
  ---
  duration_ms: 0.86952
  ...
# Subtest: sequence chip lazily inserts step and title before the clock and hides them when idle
ok 795 - sequence chip lazily inserts step and title before the clock and hides them when idle
  ---
  duration_ms: 2.386487
  ...
# Subtest: sequence settle displays its final step and opens the focus run
ok 796 - sequence settle displays its final step and opens the focus run
  ---
  duration_ms: 0.338667
  ...
# Subtest: a new run during a settle shows running at once and click opens the settled run
ok 797 - a new run during a settle shows running at once and click opens the settled run
  ---
  duration_ms: 0.471851
  ...
# Subtest: adopted unfinished runs appear flagged and all triggers light the indicator
ok 798 - adopted unfinished runs appear flagged and all triggers light the indicator
  ---
  duration_ms: 0.484045
  ...
# Subtest: first visible paint uses HTMLCollection semantics and preserves existing classes
ok 799 - first visible paint uses HTMLCollection semantics and preserves existing classes
  ---
  duration_ms: 0.393832
  ...
# Subtest: DOM-like repaints keep the mark and anatomy idempotent
ok 800 - DOM-like repaints keep the mark and anatomy idempotent
  ---
  duration_ms: 0.358765
  ...
# Subtest: DOM-like settle paint shows its outcome, then hides after the settle window
ok 801 - DOM-like settle paint shows its outcome, then hides after the settle window
  ---
  duration_ms: 0.285074
  ...
# Subtest: plugin status-chip path paints an HTMLCollection-like status item
ok 802 - plugin status-chip path paints an HTMLCollection-like status item
  ---
  duration_ms: 2.277449
  ...
# Subtest: make-or-edit command registers with Mod+Shift+Y
ok 803 - make-or-edit command registers with Mod+Shift+Y
  ---
  duration_ms: 1.976084
  ...
# Subtest: author modal renders fields, live preview, and exact markdown
ok 804 - author modal renders fields, live preview, and exact markdown
  ---
  duration_ms: 4.242762
  ...
# Subtest: inert fence preview has no focusable copy or fold controls
ok 805 - inert fence preview has no focusable copy or fold controls
  ---
  duration_ms: 1.497289
  ...
# Subtest: Esc, Ctrl+[, and q outside fields cancel; q types in a field
ok 806 - Esc, Ctrl+[, and q outside fields cancel; q types in a field
  ---
  duration_ms: 1.182618
  ...
# Subtest: Tab cycles fields and Enter saves once
ok 807 - Tab cycles fields and Enter saves once
  ---
  duration_ms: 0.591439
  ...
# Subtest: Shift+Enter inserts a newline in Text
ok 808 - Shift+Enter inserts a newline in Text
  ---
  duration_ms: 0.592602
  ...
# Subtest: late clipboard fill never overwrites typing or a closed card
ok 809 - late clipboard fill never overwrites typing or a closed card
  ---
  duration_ms: 9.898221
  ...
# Subtest: save writes one transaction and a repeat hotkey saves the open card
ok 810 - save writes one transaction and a repeat hotkey saves the open card
  ---
  duration_ms: 1.108637
  ...
# Subtest: invalid drafts and stale notes write nothing
ok 811 - invalid drafts and stale notes write nothing
  ---
  duration_ms: 0.547896
  ...
# Subtest: Alt+Click opens the clicked occurrence and never copies
ok 812 - Alt+Click opens the clicked occurrence and never copies
  ---
  duration_ms: 2.034155
  ...
# Subtest: Live Preview tooltip appends the Alt+Click hint
ok 813 - Live Preview tooltip appends the Alt+Click hint
  ---
  duration_ms: 0.474626
  ...
# Subtest: resolve refuses multiple selections
ok 814 - resolve refuses multiple selections
  ---
  duration_ms: 2.088297
  ...
# Subtest: resolve wraps a nonempty selection, including reversed ranges
ok 815 - resolve wraps a nonempty selection, including reversed ranges
  ---
  duration_ms: 0.564468
  ...
# Subtest: resolve wraps a multiline selection as a block
ok 816 - resolve wraps a multiline selection as a block
  ---
  duration_ms: 0.157771
  ...
# Subtest: resolve edits the chip under the cursor and refuses ambiguous lines
ok 817 - resolve edits the chip under the cursor and refuses ambiguous lines
  ---
  duration_ms: 1.049674
  ...
# Subtest: resolve uses a block fence range, not the flash line range
ok 818 - resolve uses a block fence range, not the flash line range
  ---
  duration_ms: 0.752206
  ...
# Subtest: resolve captures an unclosed fence through EOF
ok 819 - resolve captures an unclosed fence through EOF
  ---
  duration_ms: 0.211413
  ...
# Subtest: resolve converts a plain code span and skips inert contexts
ok 820 - resolve converts a plain code span and skips inert contexts
  ---
  duration_ms: 1.093659
  ...
# Subtest: resolve inserts at the cursor and may preload clipboard text
ok 821 - resolve inserts at the cursor and may preload clipboard text
  ---
  duration_ms: 0.2933
  ...
# Subtest: resolve honors UTF-16 offsets
ok 822 - resolve honors UTF-16 offsets
  ---
  duration_ms: 0.511176
  ...
# Subtest: list indent uses the item content column
ok 823 - list indent uses the item content column
  ---
  duration_ms: 0.378533
  ...
# Subtest: plan wraps an inline selection exactly
ok 824 - plan wraps an inline selection exactly
  ---
  duration_ms: 0.535633
  ...
# Subtest: plan inserts a fence with mid-line separators
ok 825 - plan inserts a fence with mid-line separators
  ---
  duration_ms: 0.216394
  ...
# Subtest: plan indents a list-item insert to the content column
ok 826 - plan indents a list-item insert to the content column
  ---
  duration_ms: 0.231412
  ...
# Subtest: plan keeps payload whitespace under nested and task lists
ok 827 - plan keeps payload whitespace under nested and task lists
  ---
  duration_ms: 0.200723
  ...
# Subtest: plan serializes table pipes and refuses a table-cell fence
ok 828 - plan serializes table pipes and refuses a table-cell fence
  ---
  duration_ms: 0.158934
  ...
# Subtest: plan round-trips backticks, labels, and trailing whitespace
ok 829 - plan round-trips backticks, labels, and trailing whitespace
  ---
  duration_ms: 0.353625
  ...
# Subtest: plan replaces a fence with an inline chip and keeps opening indent
ok 830 - plan replaces a fence with an inline chip and keeps opening indent
  ---
  duration_ms: 0.30901
  ...
# Subtest: plan and validation refuse empty, whitespace, and multiline labels
ok 831 - plan and validation refuse empty, whitespace, and multiline labels
  ---
  duration_ms: 0.229368
  ...
# Subtest: stale detection compares the full original buffer
ok 832 - stale detection compares the full original buffer
  ---
  duration_ms: 0.111182
  ...
# Subtest: key actions save, cancel, type q in fields, and ignore composition
ok 833 - key actions save, cancel, type q in fields, and ignore composition
  ---
  duration_ms: 0.337815
  ...
# Subtest: apply write uses one CM6 transaction and isolateHistory
ok 834 - apply write uses one CM6 transaction and isolateHistory
  ---
  duration_ms: 0.317016
  ...
# Subtest: commit refuses stale, detached, and identity-mismatched editors
ok 835 - commit refuses stale, detached, and identity-mismatched editors
  ---
  duration_ms: 0.354928
  ...
# Subtest: chipAt resolves every vector chip line
ok 836 - chipAt resolves every vector chip line
  ---
  duration_ms: 3.52979
  ...
# Subtest: chipAt honors cursor precedence and UTF-16 positions
ok 837 - chipAt honors cursor precedence and UTF-16 positions
  ---
  duration_ms: 0.307878
  ...
# Subtest: chipAt skips fenced, frontmatter, and invalid input
ok 838 - chipAt skips fenced, frontmatter, and invalid input
  ---
  duration_ms: 0.492029
  ...
# Subtest: chipAt matches the related fence helper on nested fences
ok 839 - chipAt matches the related fence helper on nested fences
  ---
  duration_ms: 0.282199
  ...
# Subtest: chipAt uses one task chip only when the cursor line has none
ok 840 - chipAt uses one task chip only when the cursor line has none
  ---
  duration_ms: 0.844333
  ...
# Subtest: chipAt keeps cursor-line precedence and counts scoped bob-copy fences once
ok 841 - chipAt keeps cursor-line precedence and counts scoped bob-copy fences once
  ---
  duration_ms: 0.390656
  ...
# Subtest: chipAt never falls through from fences or frontmatter and ignores malformed scopes
ok 842 - chipAt never falls through from fences or frontmatter and ignores malformed scopes
  ---
  duration_ms: 0.307207
  ...
# Subtest: api namespace is frozen, versioned, and never throws
ok 843 - api namespace is frozen, versioned, and never throws
  ---
  duration_ms: 1.525533
  ...
# Subtest: copy unavailable clipboard reports a useful reason
ok 844 - copy unavailable clipboard reports a useful reason
  ---
  duration_ms: 0.72294
  ...
# Subtest: cursor command resolves through chipAt and uses the shared copy path
ok 845 - cursor command resolves through chipAt and uses the shared copy path
  ---
  duration_ms: 8.046806
  ...
# Subtest: all vector payloads survive clipboard byte-exact
ok 846 - all vector payloads survive clipboard byte-exact
  ---
  duration_ms: 3.056858
  ...
# Subtest: empty and whitespace payloads never overwrite the clipboard
ok 847 - empty and whitespace payloads never overwrite the clipboard
  ---
  duration_ms: 0.275456
  ...
# Subtest: chip DOM uses textContent only and keeps payloads out of attributes
ok 848 - chip DOM uses textContent only and keeps payloads out of attributes
  ---
  duration_ms: 1.19927
  ...
# Subtest: accessible name is Copy plus the face
ok 849 - accessible name is Copy plus the face
  ---
  duration_ms: 0.247663
  ...
# Subtest: inert preview never registers gestures or writes
ok 850 - inert preview never registers gestures or writes
  ---
  duration_ms: 0.176788
  ...
# Subtest: success and failure feedback follow the timers and Notices
ok 851 - success and failure feedback follow the timers and Notices
  ---
  duration_ms: 0.86967
  ...
# Subtest: clipboard rejection shows the alert glyph and exactly one Notice
ok 852 - clipboard rejection shows the alert glyph and exactly one Notice
  ---
  duration_ms: 0.494033
  ...
# Subtest: flash shows feedback without a clipboard write
ok 853 - flash shows feedback without a clipboard write
  ---
  duration_ms: 0.182889
  ...
# Subtest: fence source payload is verbatim with CRLF normalized
ok 854 - fence source payload is verbatim with CRLF normalized
  ---
  duration_ms: 2.515995
  ...
# Subtest: fence opening parses marker, indent, and info
ok 855 - fence opening parses marker, indent, and info
  ---
  duration_ms: 0.954392
  ...
# Subtest: fence label comes from the section opening line
ok 856 - fence label comes from the section opening line
  ---
  duration_ms: 0.483303
  ...
# Subtest: fence counts, meta, and title
ok 857 - fence counts, meta, and title
  ---
  duration_ms: 0.481419
  ...
# Subtest: fence card renders title, meta, and byte-exact body
ok 858 - fence card renders title, meta, and byte-exact body
  ---
  duration_ms: 1.15756
  ...
# Subtest: fence payload never reaches attributes
ok 859 - fence payload never reaches attributes
  ---
  duration_ms: 0.369746
  ...
# Subtest: fence card folds after eight lines behind a toggle
ok 860 - fence card folds after eight lines behind a toggle
  ---
  duration_ms: 0.405264
  ...
# Subtest: fence copy button copies byte-exact; body clicks never copy
ok 861 - fence copy button copies byte-exact; body clicks never copy
  ---
  duration_ms: 21.962088
  ...
# Subtest: fence copy failure shows the failure state with one Notice
ok 862 - fence copy failure shows the failure state with one Notice
  ---
  duration_ms: 11.067284
  ...
# Subtest: fence processor renders the card with section label
ok 863 - fence processor renders the card with section label
  ---
  duration_ms: 1.202175
  ...
# Subtest: chipAt resolves opening, body, and closing lines as one block
ok 864 - chipAt resolves opening, body, and closing lines as one block
  ---
  duration_ms: 0.886452
  ...
# Subtest: chipAt block payload keeps blank lines and the trailing newline rule
ok 865 - chipAt block payload keeps blank lines and the trailing newline rule
  ---
  duration_ms: 0.294181
  ...
# Subtest: chipAt dedents list-nested fences under the opening
ok 866 - chipAt dedents list-nested fences under the opening
  ---
  duration_ms: 0.557374
  ...
# Subtest: body spans never win as inline chips inside a bob-copy fence
ok 867 - body spans never win as inline chips inside a bob-copy fence
  ---
  duration_ms: 0.210973
  ...
# Subtest: chipAt fence edge cases: unclosed, nested, and wrong-char closers
ok 868 - chipAt fence edge cases: unclosed, nested, and wrong-char closers
  ---
  duration_ms: 0.205562
  ...
# Subtest: block chips copy through the shared path and flash the fence card
ok 869 - block chips copy through the shared path and flash the fence card
  ---
  duration_ms: 0.833522
  ...
# Subtest: inert fence preview is a noninteractive span without a fold toggle
ok 870 - inert fence preview is a noninteractive span without a fold toggle
  ---
  duration_ms: 1.042761
  ...
# Subtest: payload-unique fence labels win over a stale section info
ok 871 - payload-unique fence labels win over a stale section info
  ---
  duration_ms: 0.662796
  ...
# Subtest: api exposes the fence source helper and block resolution
ok 872 - api exposes the fence source helper and block resolution
  ---
  duration_ms: 0.777866
  ...
# Subtest: vector chips match scanLine
ok 873 - vector chips match scanLine
  ---
  duration_ms: 2.409411
  ...
# Subtest: vector non-chips never scan
ok 874 - vector non-chips never scan
  ---
  duration_ms: 1.367691
  ...
# Subtest: vector serialize matches exact markdown
ok 875 - vector serialize matches exact markdown
  ---
  duration_ms: 0.635764
  ...
# Subtest: vector fence_info matches parseFenceInfo
ok 876 - vector fence_info matches parseFenceInfo
  ---
  duration_ms: 0.267771
  ...
# Subtest: grammar results are frozen
ok 877 - grammar results are frozen
  ---
  duration_ms: 0.247893
  ...
# Subtest: normalizeSpan follows CommonMark padding and table unescape
ok 878 - normalizeSpan follows CommonMark padding and table unescape
  ---
  duration_ms: 0.196595
  ...
# Subtest: fence payload joins with LF and keeps a trailing empty line
ok 879 - fence payload joins with LF and keeps a trailing empty line
  ---
  duration_ms: 0.145959
  ...
# Subtest: the frozen api never throws and exposes grammar helpers
ok 880 - the frozen api never throws and exposes grammar helpers
  ---
  duration_ms: 0.883116
  ...
# Subtest: every vector line decorates in visible ranges
ok 881 - every vector line decorates in visible ranges
  ---
  duration_ms: 2.288
  ...
# Subtest: inert contexts never decorate
ok 882 - inert contexts never decorate
  ---
  duration_ms: 1.500325
  ...
# Subtest: selection reveal uses the closed boundary interval
ok 883 - selection reveal uses the closed boundary interval
  ---
  duration_ms: 0.303169
  ...
# Subtest: rebuild triggers cover document, viewport, selection, and mode
ok 884 - rebuild triggers cover document, viewport, selection, and mode
  ---
  duration_ms: 0.261389
  ...
# Subtest: gesture rule copies only on short primary releases inside
ok 885 - gesture rule copies only on short primary releases inside
  ---
  duration_ms: 0.324138
  ...
# Subtest: widget equality compares label, text, and position
ok 886 - widget equality compares label, text, and position
  ---
  duration_ms: 0.333497
  ...
# Subtest: mode changes rebuild without cross-mode DOM state
ok 887 - mode changes rebuild without cross-mode DOM state
  ---
  duration_ms: 0.254616
  ...
# Subtest: reading replaces valid code with a real button
ok 888 - reading replaces valid code with a real button
  ---
  duration_ms: 1.721868
  ...
# Subtest: reading skips pre, links, internal links, and existing chips
ok 889 - reading skips pre, links, internal links, and existing chips
  ---
  duration_ms: 0.229718
  ...
# Subtest: reading is idempotent across repeated processing
ok 890 - reading is idempotent across repeated processing
  ---
  duration_ms: 0.204801
  ...
# Subtest: reading parses renderer textContent once and leaves neighbors alone
ok 891 - reading parses renderer textContent once and leaves neighbors alone
  ---
  duration_ms: 1.101694
  ...
# Subtest: reading buttons activate with click and keyboard without duplicate writes
ok 892 - reading buttons activate with click and keyboard without duplicate writes
  ---
  duration_ms: 5.164742
  ...
# Subtest: reading processes the root code element itself
ok 893 - reading processes the root code element itself
  ---
  duration_ms: 0.218287
  ...
# Subtest: serialize round-trips through scanLine and fence payload
ok 894 - serialize round-trips through scanLine and fence payload
  ---
  duration_ms: 51.984839
  ...
# Subtest: done/ fixtures mirror bob-cli byte for byte
ok 895 - done/ fixtures mirror bob-cli byte for byte
  ---
  duration_ms: 2.636975
  ...
# Subtest: every plugin helper agrees with the shared vectors
ok 896 - every plugin helper agrees with the shared vectors
  ---
  duration_ms: 0.990221
  ...
# Subtest: KB24: mark identities and folds equal the full planner for a sub-project
ok 897 - KB24: mark identities and folds equal the full planner for a sub-project
  ---
  duration_ms: 43.550022
  ...
# Subtest: KB24: mark identities and folds equal the full planner for a root
ok 898 - KB24: mark identities and folds equal the full planner for a root
  ---
  duration_ms: 8.870428
  ...
# Subtest: LP1–LP17: ledger leafness agrees with the reverted cycler walk
ok 899 - LP1–LP17: ledger leafness agrees with the reverted cycler walk
  ---
  duration_ms: 11.163718
  ...
# Subtest: lead tally respects declared order, grammar, peeks and last-added meaning
ok 900 - lead tally respects declared order, grammar, peeks and last-added meaning
  ---
  duration_ms: 2.313918
  ...
# Subtest: Reading cards match aliases and paths, skip nested project headings and ordinary same-stem notes
ok 901 - Reading cards match aliases and paths, skip nested project headings and ordinary same-stem notes
  ---
  duration_ms: 6.105198
  ...
# Subtest: peeks are inert text and repeated paints preserve keyboard focus and listeners
ok 902 - peeks are inert text and repeated paints preserve keyboard focus and listeners
  ---
  duration_ms: 4.019946
  ...
# Subtest: unavailable, stale, invalid and damaged reports keep distinct feedback and shared repair actions
ok 903 - unavailable, stale, invalid and damaged reports keep distinct feedback and shared repair actions
  ---
  duration_ms: 6.078408
  ...
# Subtest: missing or damaged catalog with no albums has an actionable host anchor and diagnostics
ok 904 - missing or damaged catalog with no albums has an actionable host anchor and diagnostics
  ---
  duration_ms: 1.579255
  ...
# Subtest: source scanner and group jump ignore YAML/fenced/nested examples and handle escaped labels
ok 905 - source scanner and group jump ignore YAML/fenced/nested examples and handle escaped labels
  ---
  duration_ms: 1.410654
  ...
# Subtest: lead activation keeps modifier navigation, records jump history, and calls the pane fold hook before scrolling
ok 906 - lead activation keeps modifier navigation, records jump history, and calls the pane fold hook before scrolling
  ---
  duration_ms: 2.092887
  ...
# Subtest: Reading children clean on unload, panes stay independent, file switches remove old facts
ok 907 - Reading children clean on unload, panes stay independent, file switches remove old facts
  ---
  duration_ms: 3.1893
  ...
# Subtest: Live Preview paints native callouts, leaves source text/caret intact, and removes paint in Source mode
ok 908 - Live Preview paints native callouts, leaves source text/caret intact, and removes paint in Source mode
  ---
  duration_ms: 2.378482
  ...
# Subtest: Live Preview missing-catalog action is a widget outside frontmatter, with source mode gated
ok 909 - Live Preview missing-catalog action is a widget outside frontmatter, with source mode gated
  ---
  duration_ms: 1.368063
  ...
# Subtest: CSS uses pane container wrapping, scoped album hue, safe peeks and keyboard outlines
ok 910 - CSS uses pane container wrapping, scoped album hue, safe peeks and keyboard outlines
  ---
  duration_ms: 2.788224
  ...
# Subtest: missing-catalog controls occur only in the selected source section
ok 911 - missing-catalog controls occur only in the selected source section
  ---
  duration_ms: 5.223394
  ...
# Subtest: keyboard and middle-click group controls activate once without changing the editor caret
ok 912 - keyboard and middle-click group controls activate once without changing the editor caret
  ---
  duration_ms: 19.34494
  ...
# Subtest: Live Preview extension paints after updates and cleans file switches, destroy and pending timers
ok 913 - Live Preview extension paints after updates and cleans file switches, destroy and pending timers
  ---
  duration_ms: 3.465778
  ...
# Subtest: entry kind covers scalar, list, wikilink, and legacy noun types
ok 914 - entry kind covers scalar, list, wikilink, and legacy noun types
  ---
  duration_ms: 1.171357
  ...
# Subtest: parent target handles scalar, list, and ambiguous forms
ok 915 - parent target handles scalar, list, and ambiguous forms
  ---
  duration_ms: 0.288311
  ...
# Subtest: direct album paths resolve through the report
ok 916 - direct album paths resolve through the report
  ---
  duration_ms: 0.692793
  ...
# Subtest: record notes resolve their actual parent link
ok 917 - record notes resolve their actual parent link
  ---
  duration_ms: 0.281097
  ...
# Subtest: record legacy types resolve like records
ok 918 - record legacy types resolve like records
  ---
  duration_ms: 0.183971
  ...
# Subtest: missing, cyclic, ambiguous, and non-album parents teach instead of guessing
ok 919 - missing, cyclic, ambiguous, and non-album parents teach instead of guessing
  ---
  duration_ms: 0.388492
  ...
# Subtest: palette command is registered as a literal addCommand for the inventory
ok 920 - palette command is registered as a literal addCommand for the inventory
  ---
  duration_ms: 28.922329
  ...
# Subtest: header resolves real parent paths and ignores breadcrumb labels
ok 921 - header resolves real parent paths and ignores breadcrumb labels
  ---
  duration_ms: 3.713691
  ...
# Subtest: owner ancestry stops without warning at the conventional type note or a direct non-home parent
ok 922 - owner ancestry stops without warning at the conventional type note or a direct non-home parent
  ---
  duration_ms: 0.724864
  ...
# Subtest: missing, malformed, cyclic, and depth-limited owner chains still warn
ok 923 - missing, malformed, cyclic, and depth-limited owner chains still warn
  ---
  duration_ms: 1.965594
  ...
# Subtest: schema model preserves declaration and choice order; empty and invalid routes stay explicit
ok 924 - schema model preserves declaration and choice order; empty and invalid routes stay explicit
  ---
  duration_ms: 1.09937
  ...
# Subtest: broken schema remains visible and disables the capture route with its diagnostic
ok 925 - broken schema remains visible and disables the capture route with its diagnostic
  ---
  duration_ms: 4.408549
  ...
# Subtest: rendering is idempotent, keeps schema labels as text, scopes Properties, and clears on type change
ok 926 - rendering is idempotent, keeps schema labels as text, scopes Properties, and clears on type change
  ---
  duration_ms: 3.107965
  ...
# Subtest: clipboard failure is surfaced and does not mutate a note
ok 927 - clipboard failure is surfaced and does not mutate a note
  ---
  duration_ms: 0.635995
  ...
# Subtest: Live Preview widgets follow album identity and remove the Properties scope on view switches
ok 928 - Live Preview widgets follow album identity and remove the Properties scope on view switches
  ---
  duration_ms: 2.450359
  ...
# Subtest: Reading lifecycle unload restores Properties visibility
ok 929 - Reading lifecycle unload restores Properties visibility
  ---
  duration_ms: 1.825917
  ...
# Subtest: detached callout chunks never paint reading headers, including after editor attachment
ok 930 - detached callout chunks never paint reading headers, including after editor attachment
  ---
  duration_ms: 1.235449
  ...
# Subtest: reading batches pick attached chunks, stay idempotent, and keep pane/embed lifetimes separate
ok 931 - reading batches pick attached chunks, stay idempotent, and keep pane/embed lifetimes separate
  ---
  duration_ms: 5.076083
  ...
# Subtest: chunks attaching before the flush share the preview/sizer identity
ok 932 - chunks attaching before the flush share the preview/sizer identity
  ---
  duration_ms: 1.112945
  ...
# Subtest: late reading attachment paints on refresh and unload uses the live surface
ok 933 - late reading attachment paints on refresh and unload uses the live surface
  ---
  duration_ms: 2.355488
  ...
# Subtest: repaint sweeps stray reading chrome from editor chunks without removing CM widgets
ok 934 - repaint sweeps stray reading chrome from editor chunks without removing CM widgets
  ---
  duration_ms: 0.627899
  ...
# Subtest: teardown cancels pending reading batches
ok 935 - teardown cancels pending reading batches
  ---
  duration_ms: 0.589756
  ...
# Subtest: H1-less albums paint at the start and embeds keep their own property scope
ok 936 - H1-less albums paint at the start and embeds keep their own property scope
  ---
  duration_ms: 0.649249
  ...
# Subtest: schema summary starts expanded and collapses per album in view state
ok 937 - schema summary starts expanded and collapses per album in view state
  ---
  duration_ms: 3.532526
  ...
# Subtest: chip rows cover kinds, flags, grouping, legacy, and empty teaching copy
ok 938 - chip rows cover kinds, flags, grouping, legacy, and empty teaching copy
  ---
  duration_ms: 4.063209
  ...
# Subtest: read-only Schema Card paints counts, lint, and a navigation/y/esc footer
ok 939 - read-only Schema Card paints counts, lint, and a navigation/y/esc footer
  ---
  duration_ms: 45.681149
  ...
# Subtest: same-message child warnings name each file and keep distinct focus and card targets
ok 940 - same-message child warnings name each file and keep distinct focus and card targets
  ---
  duration_ms: 8.953327
  ...
# Subtest: y jumps to the field or lint line in Source mode without writing the vault
ok 941 - y jumps to the field or lint line in Source mode without writing the vault
  ---
  duration_ms: 1.71226
  ...
# Subtest: theme accent, schema button, and keyboard labels stay on the header
ok 942 - theme accent, schema button, and keyboard labels stay on the header
  ---
  duration_ms: 5.546962
  ...
# Subtest: schema edit model preserves typed defaults and stable field and choice targets
ok 943 - schema edit model preserves typed defaults and stable field and choice targets
  ---
  duration_ms: 1.481269
  ...
# Subtest: Schema Card uses bob's singular display label for one record and keeps the legacy fallback
ok 944 - Schema Card uses bob's singular display label for one record and keeps the legacy fallback
  ---
  duration_ms: 0.603322
  ...
# Subtest: Schema Card key events reorder fields and choices while plain navigation stays read-only
ok 945 - Schema Card key events reorder fields and choices while plain navigation stays read-only
  ---
  duration_ms: 64.775463
  ...
# Subtest: Schema Card preserves typed draft, caret, and focus through report repaint and debounces edits
ok 946 - Schema Card preserves typed draft, caret, and focus through report repaint and debounces edits
  ---
  duration_ms: 371.068821
  ...
# Subtest: Schema Card Enter is gated by current preview across pending, refused, stale, and duplicate input events
ok 947 - Schema Card Enter is gated by current preview across pending, refused, stale, and duplicate input events
  ---
  duration_ms: 730.017205
  ...
# Subtest: a repainted Apply preview uses live session state and double Enter applies once
ok 948 - a repainted Apply preview uses live session state and double Enter applies once
  ---
  duration_ms: 333.064216
  ...
# Subtest: an enabled Apply control routes a newly stale preview to a visible refusal
ok 949 - an enabled Apply control routes a newly stale preview to a visible refusal
  ---
  duration_ms: 317.11366
  ...
# Subtest: new choice field rows keep live order and values as early and middle choices are removed
ok 950 - new choice field rows keep live order and values as early and middle choices are removed
  ---
  duration_ms: 62.160219
  ...
# Subtest: Schema Card stages typed edits, previews one op, and applies only after confirmation
ok 951 - Schema Card stages typed edits, previews one op, and applies only after confirmation
  ---
  duration_ms: 12.491534
  ...
# Subtest: open album panes save in order and missing save support refuses
ok 952 - open album panes save in order and missing save support refuses
  ---
  duration_ms: 0.632849
  ...
# Subtest: Schema Card maps album, field, choice, ordering, toggle, and removal gestures
ok 953 - Schema Card maps album, field, choice, ordering, toggle, and removal gestures
  ---
  duration_ms: 41.885003
  ...
# Subtest: Schema Card Escape follows one dispatch: stage cancel, draft clear, then close
ok 954 - Schema Card Escape follows one dispatch: stage cancel, draft clear, then close
  ---
  duration_ms: 8.736673
  ...
# Subtest: default folds: first group stays open, later groups fold only above twelve records
ok 955 - default folds: first group stays open, later groups fold only above twelve records
  ---
  duration_ms: 9.415971
  ...
# Subtest: later group of twelve stays open; thirteen folds even when only two subgroup items exist
ok 956 - later group of twelve stays open; thirteen folds even when only two subgroup items exist
  ---
  duration_ms: 4.175283
  ...
# Subtest: empty and flat indexes stay readable without fold controls
ok 957 - empty and flat indexes stay readable without fold controls
  ---
  duration_ms: 1.510945
  ...
# Subtest: user fold choices persist across refresh and stay isolated per pane
ok 958 - user fold choices persist across refresh and stay isolated per pane
  ---
  duration_ms: 8.558653
  ...
# Subtest: group jump expands only the destination pane before scroll
ok 959 - group jump expands only the destination pane before scroll
  ---
  duration_ms: 4.532616
  ...
# Subtest: visited and watched_on chips are distinct, skip invalid/future dates, and refresh on day rollover
ok 960 - visited and watched_on chips are distinct, skip invalid/future dates, and refresh on day rollover
  ---
  duration_ms: 4.285233
  ...
# Subtest: painting, folding, and date chips never write note bytes
ok 961 - painting, folding, and date chips never write note bytes
  ---
  duration_ms: 3.652955
  ...
# Subtest: fenced examples are ignored; Live Preview paints, Source mode removes chrome
ok 962 - fenced examples are ignored; Live Preview paints, Source mode removes chrome
  ---
  duration_ms: 3.969661
  ...
# Subtest: reading children clean on unload and teardown restores hidden rows
ok 963 - reading children clean on unload and teardown restores hidden rows
  ---
  duration_ms: 20.344769
  ...
# Subtest: non-album notes and embeds in the outer editor are left alone
ok 964 - non-album notes and embeds in the outer editor are left alone
  ---
  duration_ms: 7.653263
  ...
# Subtest: CSS hides folded nested lists and styles the tally with area hue
ok 965 - CSS hides folded nested lists and styles the tally with area hue
  ---
  duration_ms: 8.320258
  ...
# Subtest: multi-slot arrange compiles one envelope, paints projected order with zero writer calls, and revert clears the draft
ok 966 - multi-slot arrange compiles one envelope, paints projected order with zero writer calls, and revert clears the draft
  ---
  duration_ms: 95.79183
  ...
# Subtest: quiet saves on one Enter while loud needs Confirm save
ok 967 - quiet saves on one Enter while loud needs Confirm save
  ---
  duration_ms: 46.558046
  ...
# Subtest: follow-on moves during an in-flight apply never call setDraft until it settles
ok 968 - follow-on moves during an in-flight apply never call setDraft until it settles
  ---
  duration_ms: 35.010816
  ...
# Subtest: refusal keeps the arrangement pending; u and esc walk the ladder; gap hints place by keystroke; macOS codes move
ok 969 - refusal keeps the arrangement pending; u and esc walk the ladder; gap hints place by keystroke; macOS codes move
  ---
  duration_ms: 33.466427
  ...
# Subtest: close-during-save records the plugin-level undo and seeds a reopened card
ok 970 - close-during-save records the plugin-level undo and seeds a reopened card
  ---
  duration_ms: 22.327767
  ...
# Subtest: Schema Card shell paints stable regions, pills, and a hidden empty status rule
ok 971 - Schema Card shell paints stable regions, pills, and a hidden empty status rule
  ---
  duration_ms: 28.35674
  ...
# Subtest: record field entry survives the host modal's initial focus and preserves Ctrl+J/K
ok 972 - record field entry survives the host modal's initial focus and preserves Ctrl+J/K
  ---
  duration_ms: 18.541186
  ...
# Subtest: selection and session paints keep body and stage input nodes
ok 973 - selection and session paints keep body and stage input nodes
  ---
  duration_ms: 370.482199
  ...
# Subtest: Enter latches a pending preview and applies when that revision succeeds
ok 974 - Enter latches a pending preview and applies when that revision succeeds
  ---
  duration_ms: 364.921452
  ...
# Subtest: a further edit clears the Enter latch before a stale preview can apply
ok 975 - a further edit clears the Enter latch before a stale preview can apply
  ---
  duration_ms: 354.512594
  ...
# Subtest: Emoji Slot preserves graphemes and ports split_icon fixtures
ok 976 - Emoji Slot preserves graphemes and ports split_icon fixtures
  ---
  duration_ms: 1.873477
  ...
# Subtest: Emoji Slot searches, browses, marks sibling duplicates, and Enter picks without saving the stage
ok 977 - Emoji Slot searches, browses, marks sibling duplicates, and Enter picks without saving the stage
  ---
  duration_ms: 39.437048
  ...
# Subtest: Emoji Slot Escape closes the panel before the stage and direct pasted graphemes stay exact
ok 978 - Emoji Slot Escape closes the panel before the stage and direct pasted graphemes stay exact
  ---
  duration_ms: 51.365566
  ...
# Subtest: every field-add initial choice gets an Emoji Slot and missing or v0 apis use the plain input
ok 979 - every field-add initial choice gets an Emoji Slot and missing or v0 apis use the plain input
  ---
  duration_ms: 79.009362
  ...
# Subtest: Emoji Slot result assembly handles full catalogs under the filter paint budget
ok 980 - Emoji Slot result assembly handles full catalogs under the filter paint budget
  ---
  duration_ms: 15.372565
  ...
# Subtest: Emoji Slot Ctrl+N / Ctrl+P step one emoji at a time and wrap at the ends
ok 981 - Emoji Slot Ctrl+N / Ctrl+P step one emoji at a time and wrap at the ends
  ---
  duration_ms: 0.509844
  ...
# Subtest: Emoji Slot move-key alias matches the exact Ctrl chord only
ok 982 - Emoji Slot move-key alias matches the exact Ctrl chord only
  ---
  duration_ms: 0.34075
  ...
# Subtest: Emoji Slot Ctrl+N steps one emoji, Ctrl+P wraps to the last, and the highlight stays in view
ok 983 - Emoji Slot Ctrl+N steps one emoji, Ctrl+P wraps to the last, and the highlight stays in view
  ---
  duration_ms: 18.295537
  ...
# Subtest: lock wait paints the pending line and Esc stops without closing
ok 984 - lock wait paints the pending line and Esc stops without closing
  ---
  duration_ms: 26.697571
  ...
# Subtest: Emoji Slot hint teaches the gesture and follows open, pick, and clear
ok 985 - Emoji Slot hint teaches the gesture and follows open, pick, and clear
  ---
  duration_ms: 99.248903
  ...
# Subtest: every field-add initial choice shows the hint until its glyph is set
ok 986 - every field-add initial choice shows the hint until its glyph is set
  ---
  duration_ms: 46.352935
  ...
# Subtest: close-key predicate accepts q/Q/Ctrl+[ and rejects modifiers/composition
ok 987 - close-key predicate accepts q/Q/Ctrl+[ and rejects modifiers/composition
  ---
  duration_ms: 0.65959
  ...
# Subtest: q and Ctrl+[ close from the editor behind the modal and are consumed
ok 988 - q and Ctrl+[ close from the editor behind the modal and are consumed
  ---
  duration_ms: 2.425061
  ...
# Subtest: q types in a stage input while Ctrl+[ cancels the stage then closes
ok 989 - q types in a stage input while Ctrl+[ cancels the stage then closes
  ---
  duration_ms: 23.260736
  ...
# Subtest: q and Ctrl+[ leave hint mode without picking a gap
ok 990 - q and Ctrl+[ leave hint mode without picking a gap
  ---
  duration_ms: 176.062194
  ...
# Subtest: close keys follow Esc through pending moves, All actions, drag, and applying
ok 991 - close keys follow Esc through pending moves, All actions, drag, and applying
  ---
  duration_ms: 254.356049
  ...
# Subtest: scope handler passes unrelated keys through and unregisters on close
ok 992 - scope handler passes unrelated keys through and unregisters on close
  ---
  duration_ms: 113.82777
  ...
# Subtest: Emoji Slot search types q while Ctrl+[ closes only the picker
ok 993 - Emoji Slot search types q while Ctrl+[ closes only the picker
  ---
  duration_ms: 44.440342
  ...
# Subtest: plain-browsing close hint reads esc/q
ok 994 - plain-browsing close hint reads esc/q
  ---
  duration_ms: 51.183368
  ...
# Subtest: field jumps follow one painted order shared with the body painter
ok 995 - field jumps follow one painted order shared with the body painter
  ---
  duration_ms: 143.246739
  ...
# Subtest: painted targets put body issues before + field
ok 996 - painted targets put body issues before + field
  ---
  duration_ms: 0.608432
  ...
# Subtest: field step helpers scan strictly to the next field row
ok 997 - field step helpers scan strictly to the next field row
  ---
  duration_ms: 0.521226
  ...
# Subtest: Ctrl+J/K walk every row of the field-step table
ok 998 - Ctrl+J/K walk every row of the field-step table
  ---
  duration_ms: 75.381376
  ...
# Subtest: digits jump straight to field N as painted
ok 999 - digits jump straight to field N as painted
  ---
  duration_ms: 29.421382
  ...
# Subtest: 3 then Alt+K nudges field 3 exactly one slot
ok 1000 - 3 then Alt+K nudges field 3 exactly one slot
  ---
  duration_ms: 16.920781
  ...
# Subtest: Shift+1 still stages required while shifted digits jump
ok 1001 - Shift+1 still stages required while shifted digits jump
  ---
  duration_ms: 15.173624
  ...
# Subtest: Alt arrange remains separate from Ctrl field jumps
ok 1002 - Alt arrange remains separate from Ctrl field jumps
  ---
  duration_ms: 33.977933
  ...
# Subtest: jumps are inert in stages, inputs, composition, applying, the read-only card, and hint mode
ok 1003 - jumps are inert in stages, inputs, composition, applying, the read-only card, and hint mode
  ---
  duration_ms: 30.100188
  ...
# Subtest: jumps never touch the session preview, apply, or the arrangement nudge
ok 1004 - jumps never touch the session preview, apply, or the arrangement nudge
  ---
  duration_ms: 14.527541
  ...
# Subtest: a held clamp key bumps once, then stays silent
ok 1005 - a held clamp key bumps once, then stays silent
  ---
  duration_ms: 15.033577
  ...
# Subtest: zero fields announce the empty lane on every jump key
ok 1006 - zero fields announce the empty lane on every jump key
  ---
  duration_ms: 11.816094
  ...
# Subtest: one field uses the singular lane noun
ok 1007 - one field uses the singular lane noun
  ---
  duration_ms: 9.54142
  ...
# Subtest: jumps reveal the group and leave the announcer visible to screen readers
ok 1008 - jumps reveal the group and leave the announcer visible to screen readers
  ---
  duration_ms: 9.667019
  ...
# Subtest: a missing scroller never throws
ok 1009 - a missing scroller never throws
  ---
  duration_ms: 16.413734
  ...
# Subtest: reduced motion turns off every bump, including the nudge shake
ok 1010 - reduced motion turns off every bump, including the nudge shake
  ---
  duration_ms: 16.36984
  ...
# Subtest: keycaps number painted fields 1-9 and keep a hidden column at 10
ok 1011 - keycaps number painted fields 1-9 and keep a hidden column at 10
  ---
  duration_ms: 3.88559
  ...
# Subtest: keycap numbers re-flow after a field nudge
ok 1012 - keycap numbers re-flow after a field nudge
  ---
  duration_ms: 15.499909
  ...
# Subtest: is-current-group follows chip and + choice selection and clears on field or stats
ok 1013 - is-current-group follows chip and + choice selection and clears on field or stats
  ---
  duration_ms: 8.508347
  ...
# Subtest: plain browsing paints a field hint with two keycaps after Enter
ok 1014 - plain browsing paints a field hint with two keycaps after Enter
  ---
  duration_ms: 5.129315
  ...
# Subtest: the field hint uses 1 for a single field and 1-9 when there are ten
ok 1015 - the field hint uses 1 for a single field and 1-9 when there are ten
  ---
  duration_ms: 0.428027
  ...
# Subtest: the field hint is absent with zero fields, a stage, hint mode, pending moves, saving, a lock wait, and the read-only card
ok 1016 - the field hint is absent with zero fields, a stage, hint mode, pending moves, saving, a lock wait, and the read-only card
  ---
  duration_ms: 0.466401
  ...
# Subtest: the read-only card paints no field keycaps
ok 1017 - the read-only card paints no field keycaps
  ---
  duration_ms: 9.317062
  ...
# Subtest: ghost defaults land after the selected choice and stay out of the envelope
ok 1018 - ghost defaults land after the selected choice and stay out of the envelope
  ---
  duration_ms: 57.03426
  ...
# Subtest: Alt+J inside the label input moves the ghost and inserts no macOS glyph
ok 1019 - Alt+J inside the label input moves the ghost and inserts no macOS glyph
  ---
  duration_ms: 45.178772
  ...
# Subtest: ghost gap badges place by keystroke and Esc leaves hint mode with the stage open
ok 1020 - ghost gap badges place by keystroke and Esc leaves hint mode with the stage open
  ---
  duration_ms: 25.298168
  ...
# Subtest: field-add paints a ghost row whose moves set the field position
ok 1021 - field-add paints a ghost row whose moves set the field position
  ---
  duration_ms: 25.287148
  ...
# Subtest: grip handles paint while browsing and hide while a stage is open
ok 1022 - grip handles paint while browsing and hide while a stage is open
  ---
  duration_ms: 8.376326
  ...
# Subtest: drag gap math tracks pointer position in both orientations
ok 1023 - drag gap math tracks pointer position in both orientations
  ---
  duration_ms: 0.488653
  ...
# Subtest: drag sessions drop through the same placeAtGap path as the keyboard
ok 1024 - drag sessions drop through the same placeAtGap path as the keyboard
  ---
  duration_ms: 11.093975
  ...
# Subtest: out-of-scope drops and Esc cancel without touching the arrangement
ok 1025 - out-of-scope drops and Esc cancel without touching the arrangement
  ---
  duration_ms: 11.742553
  ...
# Subtest: autoscroll steps only inside the edge zone of a scrollable card
ok 1026 - autoscroll steps only inside the edge zone of a scrollable card
  ---
  duration_ms: 0.72278
  ...
# Subtest: update argv, envelope, and timeout follow the guarded writer contract
ok 1027 - update argv, envelope, and timeout follow the guarded writer contract
  ---
  duration_ms: 3.328506
  ...
# Subtest: update decoder keeps typed refusals on numeric exits and rejects wire errors
ok 1028 - update decoder keeps typed refusals on numeric exits and rejects wire errors
  ---
  duration_ms: 1.013786
  ...
# Subtest: stdin carries shell-looking labels byte-identical and never as shell text
ok 1029 - stdin carries shell-looking labels byte-identical and never as shell text
  ---
  duration_ms: 4.113325
  ...
# Subtest: stdin failure and timeout surface as transport errors, never refusals
ok 1030 - stdin failure and timeout surface as transport errors, never refusals
  ---
  duration_ms: 2.654129
  ...
# Subtest: typing settles through a 250 ms debounce; navigation never previews
ok 1031 - typing settles through a 250 ms debounce; navigation never previews
  ---
  duration_ms: 3.370416
  ...
# Subtest: stale preview responses are suppressed; draft or vault changes invalidate Apply
ok 1032 - stale preview responses are suppressed; draft or vault changes invalidate Apply
  ---
  duration_ms: 2.438066
  ...
# Subtest: close cancels a pending preview and ignores late work
ok 1033 - close cancels a pending preview and ignores late work
  ---
  duration_ms: 1.328697
  ...
# Subtest: apply returns the refreshed display report for changed and unchanged saves
ok 1034 - apply returns the refreshed display report for changed and unchanged saves
  ---
  duration_ms: 1.319209
  ...
# Subtest: apply awaits editor saves, refuses on failure, and teaches missing support
ok 1035 - apply awaits editor saves, refuses on failure, and teaches missing support
  ---
  duration_ms: 2.070423
  ...
# Subtest: a save that invalidates the preview requires confirmation again
ok 1036 - a save that invalidates the preview requires confirmation again
  ---
  duration_ms: 3.615614
  ...
# Subtest: an in-flight save cannot apply its captured envelope after a newer draft arrives
ok 1037 - an in-flight save cannot apply its captured envelope after a newer draft arrives
  ---
  duration_ms: 0.995631
  ...
# Subtest: double Enter and parallel applies share one apply guard
ok 1038 - double Enter and parallel applies share one apply guard
  ---
  duration_ms: 0.740143
  ...
# Subtest: no-op success keeps Undo; changed success stores the opaque inverse
ok 1039 - no-op success keeps Undo; changed success stores the opaque inverse
  ---
  duration_ms: 0.876123
  ...
# Subtest: u stages the inverse on the preview-and-Enter path without reconstruction
ok 1040 - u stages the inverse on the preview-and-Enter path without reconstruction
  ---
  duration_ms: 1.468364
  ...
# Subtest: refusals keep the draft unconfirmed and never retry automatically
ok 1041 - refusals keep the draft unconfirmed and never retry automatically
  ---
  duration_ms: 0.625825
  ...
# Subtest: stale apply responses refresh and keep the draft without retrying
ok 1042 - stale apply responses refresh and keep the draft without retrying
  ---
  duration_ms: 0.631957
  ...
# Subtest: lock_busy then success retries the identical envelope once and never resaves
ok 1043 - lock_busy then success retries the identical envelope once and never resaves
  ---
  duration_ms: 5.89627
  ...
# Subtest: repeated lock_busy advances attempts and ticks elapsed time every second
ok 1044 - repeated lock_busy advances attempts and ticks elapsed time every second
  ---
  duration_ms: 2.674177
  ...
# Subtest: stopWaiting with no in-flight attempt restores preview-ready and Enter retries
ok 1045 - stopWaiting with no in-flight attempt restores preview-ready and Enter retries
  ---
  duration_ms: 5.980601
  ...
# Subtest: stopWaiting during an in-flight attempt that succeeds is a normal save
ok 1046 - stopWaiting during an in-flight attempt that succeeds is a normal save
  ---
  duration_ms: 1.082136
  ...
# Subtest: budget exhaustion restores preview-ready with lockNotice
ok 1047 - budget exhaustion restores preview-ready with lockNotice
  ---
  duration_ms: 6.537503
  ...
# Subtest: generation move with the same consequence keeps waiting; a different one ends the wait
ok 1048 - generation move with the same consequence keeps waiting; a different one ends the wait
  ---
  duration_ms: 2.158893
  ...
# Subtest: close mid-wait starts no further spawnApply calls
ok 1049 - close mid-wait starts no further spawnApply calls
  ---
  duration_ms: 0.763518
  ...
# Subtest: transport failure after lock_busy takes today's unknown path with no retry
ok 1050 - transport failure after lock_busy takes today's unknown path with no retry
  ---
  duration_ms: 0.773647
  ...
# Subtest: unknown apply outcomes refuse and demand explicit reconciliation
ok 1051 - unknown apply outcomes refuse and demand explicit reconciliation
  ---
  duration_ms: 0.532316
  ...
# Subtest: post-sync failure keeps the commit and Undo and retries with vault-sync only
ok 1052 - post-sync failure keeps the commit and Undo and retries with vault-sync only
  ---
  duration_ms: 0.855874
  ...
# Subtest: vault-sync retry failures keep the warning without losing Undo
ok 1053 - vault-sync retry failures keep the warning without losing Undo
  ---
  duration_ms: 0.516877
  ...
# Subtest: the service skips the forced revalidate on lock_busy
ok 1054 - the service skips the forced revalidate on lock_busy
  ---
  duration_ms: 1.086454
  ...
# Subtest: duplicate applies refuse busy while the first flight owns the lifecycle
ok 1055 - duplicate applies refuse busy while the first flight owns the lifecycle
  ---
  duration_ms: 1.818282
  ...
# Subtest: an apply waits out a running sync instead of overlapping it
ok 1056 - an apply waits out a running sync instead of overlapping it
  ---
  duration_ms: 1.721888
  ...
# Subtest: the writer's own echo schedules no sync while unrelated changes coalesce one trailing sync
ok 1057 - the writer's own echo schedules no sync while unrelated changes coalesce one trailing sync
  ---
  duration_ms: 4.155214
  ...
# Subtest: a pre-write list flight never becomes the post-write report
ok 1058 - a pre-write list flight never becomes the post-write report
  ---
  duration_ms: 2.472611
  ...
# Subtest: cancelled and refused service sessions never touch the plugin vault writer
ok 1059 - cancelled and refused service sessions never touch the plugin vault writer
  ---
  duration_ms: 0.559118
  ...
# Subtest: real bob fixtures decode: dry-run, refusal, stale, and no-op
ok 1060 - real bob fixtures decode: dry-run, refusal, stale, and no-op
  ---
  duration_ms: 111.801874
  ...
# Subtest: error focus picks the first error line with message and suggestions
ok 1061 - error focus picks the first error line with message and suggestions
  ---
  duration_ms: 1.859771
  ...
# Subtest: Done refuses failed saves before touching the report
ok 1062 - Done refuses failed saves before touching the report
  ---
  duration_ms: 0.328969
  ...
# Subtest: Done refuses unavailable or stale reports
ok 1063 - Done refuses unavailable or stale reports
  ---
  duration_ms: 0.266198
  ...
# Subtest: Done shares one pending save across concurrent clicks
ok 1064 - Done shares one pending save across concurrent clicks
  ---
  duration_ms: 1.013225
  ...
# Subtest: Done retries when a vault generation advances during the forced report
ok 1065 - Done retries when a vault generation advances during the forced report
  ---
  duration_ms: 0.373543
  ...
# Subtest: Done abandons delayed saves after navigation, pane close, or plugin unload
ok 1066 - Done abandons delayed saves after navigation, pane close, or plugin unload
  ---
  duration_ms: 0.473574
  ...
# Subtest: Done does not reopen the card if its pane navigates during view restoration
ok 1067 - Done does not reopen the card if its pane navigates during view restoration
  ---
  duration_ms: 6.25829
  ...
# Subtest: Done keeps Source mode on schema errors and paints the diagnostic line
ok 1068 - Done keeps Source mode on schema errors and paints the diagnostic line
  ---
  duration_ms: 0.472793
  ...
# Subtest: Done approves valid schemas and warning-only reports
ok 1069 - Done approves valid schemas and warning-only reports
  ---
  duration_ms: 0.863299
  ...
# Subtest: Done button is a small accessible affordance outside the note text
ok 1070 - Done button is a small accessible affordance outside the note text
  ---
  duration_ms: 0.830936
  ...
# Subtest: two panes keep separate excursions: decisions are per-leaf records
ok 1071 - two panes keep separate excursions: decisions are per-leaf records
  ---
  duration_ms: 0.362853
  ...
# Subtest: album list and sync use fixed JSON argv and the versioned report decoders
ok 1072 - album list and sync use fixed JSON argv and the versioned report decoders
  ---
  duration_ms: 4.514721
  ...
# Subtest: album field and album-entry report additions stay optional
ok 1073 - album field and album-entry report additions stay optional
  ---
  duration_ms: 0.678736
  ...
# Subtest: catalog-only damage stays visible when no album rows exist
ok 1074 - catalog-only damage stays visible when no album rows exist
  ---
  duration_ms: 0.280496
  ...
# Subtest: type encodings normalize like Bob; schema and choice order is significant
ok 1075 - type encodings normalize like Bob; schema and choice order is significant
  ---
  duration_ms: 2.270837
  ...
# Subtest: album subprocess uses bobSpawnJson with vault, timeout, and bounded output
ok 1076 - album subprocess uses bobSpawnJson with vault, timeout, and bounded output
  ---
  duration_ms: 5.38832
  ...
# Subtest: one vault-scoped list flight serves simultaneous subscribers
ok 1077 - one vault-scoped list flight serves simultaneous subscribers
  ---
  duration_ms: 1.514001
  ...
# Subtest: a change during list fetch coalesces into one later generation
ok 1078 - a change during list fetch coalesces into one later generation
  ---
  duration_ms: 1.321143
  ...
# Subtest: failed refresh keeps last good data stale and retries only on new demand
ok 1079 - failed refresh keeps last good data stale and retries only on new demand
  ---
  duration_ms: 0.783025
  ...
# Subtest: unload clears subscriptions and prevents a late list result from repainting
ok 1080 - unload clears subscriptions and prevents a late list result from repainting
  ---
  duration_ms: 1.137473
  ...
# Subtest: startup seeds frontmatter silently; only structural album edits debounce sync
ok 1081 - startup seeds frontmatter silently; only structural album edits debounce sync
  ---
  duration_ms: 2.206504
  ...
# Subtest: record edits sync, body edits and unrelated notes do not
ok 1082 - record edits sync, body edits and unrelated notes do not
  ---
  duration_ms: 1.960564
  ...
# Subtest: owner ancestry and type changes invalidate and sync; other owner edits do not
ok 1083 - owner ancestry and type changes invalidate and sync; other owner edits do not
  ---
  duration_ms: 0.845074
  ...
# Subtest: deletion and rename schedule sync across membership boundaries
ok 1084 - deletion and rename schedule sync across membership boundaries
  ---
  duration_ms: 0.733481
  ...
# Subtest: generated index writes do not restart a sync loop
ok 1085 - generated index writes do not restart a sync loop
  ---
  duration_ms: 1.663607
  ...
# Subtest: a real frontmatter change during sync coalesces one trailing sync
ok 1086 - a real frontmatter change during sync coalesces one trailing sync
  ---
  duration_ms: 1.32477
  ...
# Subtest: partial sync failure keeps its report and still revalidates the list
ok 1087 - partial sync failure keeps its report and still revalidates the list
  ---
  duration_ms: 1.486498
  ...
# Subtest: sync waits out a pre-write list and then fetches a post-sync report
ok 1088 - sync waits out a pre-write list and then fetches a post-sync report
  ---
  duration_ms: 1.064293
  ...
# Subtest: the trailing three-second sync fires once after schema and member edits
ok 1089 - the trailing three-second sync fires once after schema and member edits
  ---
  duration_ms: 1.808423
  ...
# Subtest: a view-show demand refreshes the shared report and local-day rollover notifies
ok 1090 - a view-show demand refreshes the shared report and local-day rollover notifies
  ---
  duration_ms: 1.044394
  ...
# Subtest: headless setup does not keep the process alive with a browser rollover timer
ok 1091 - headless setup does not keep the process alive with a browser rollover timer
  ---
  duration_ms: 0.358264
  ...
# Subtest: real bob fixtures decode: healthy and broken albums in one vault
ok 1092 - real bob fixtures decode: healthy and broken albums in one vault
  ---
  duration_ms: 79.65091
  ...
# Subtest: Areas host, row, hue, health, status, and unplaced models follow Bob's report
ok 1093 - Areas host, row, hue, health, status, and unplaced models follow Bob's report
  ---
  duration_ms: 4.554097
  ...
# Subtest: Reading card paints reported hue dots, sync and root warning without editing Markdown
ok 1094 - Reading card paints reported hue dots, sync and root warning without editing Markdown
  ---
  duration_ms: 7.886229
  ...
# Subtest: standalone cards show report rows; non-host and unavailable notes get no phantom card
ok 1095 - standalone cards show report rows; non-host and unavailable notes get no phantom card
  ---
  duration_ms: 2.311103
  ...
# Subtest: standalone row nodes stay stable until rows, folds, or source path change
ok 1096 - standalone row nodes stay stable until rows, folds, or source path change
  ---
  duration_ms: 2.579656
  ...
# Subtest: standalone area links open their target and request hover previews
ok 1097 - standalone area links open their target and request hover previews
  ---
  duration_ms: 1.490437
  ...
# Subtest: Areas renderer registers in Reading and Live Preview at the family priority
ok 1098 - Areas renderer registers in Reading and Live Preview at the family priority
  ---
  duration_ms: 15.804259
  ...
# Subtest: workspace scroll guard resets forbidden containers and logs once per window
ok 1099 - workspace scroll guard resets forbidden containers and logs once per window
  ---
  duration_ms: 6.980971
  ...
# Subtest: fold helpers default expanded and key by pane host plus row
ok 1100 - fold helpers default expanded and key by pane host plus row
  ---
  duration_ms: 0.333046
  ...
# Subtest: chips follow fold state and hide zeros; tooltips keep stems visible
ok 1101 - chips follow fold state and hide zeros; tooltips keep stems visible
  ---
  duration_ms: 0.913945
  ...
# Subtest: nested rows fold per map, switch chips, and keep stored stem link text
ok 1102 - nested rows fold per map, switch chips, and keep stored stem link text
  ---
  duration_ms: 12.747623
  ...
# Subtest: add-summary is hover-only in CSS and opens the notebooks summary path
ok 1103 - add-summary is hover-only in CSS and opens the notebooks summary path
  ---
  duration_ms: 2.243875
  ...
# Subtest: two panes keep independent folds across a repaint
ok 1104 - two panes keep independent folds across a repaint
  ---
  duration_ms: 4.166657
  ...
# Subtest: Areas list and sync use JSON argv and strict schema-1 report decoders
ok 1105 - Areas list and sync use JSON argv and strict schema-1 report decoders
  ---
  duration_ms: 4.391927
  ...
# Subtest: relevance is limited to area, project, root, and today's note
ok 1106 - relevance is limited to area, project, root, and today's note
  ---
  duration_ms: 0.710146
  ...
# Subtest: report refreshes are debounced, stale rows survive a failed refresh, and sync is explicit
ok 1107 - report refreshes are debounced, stale rows survive a failed refresh, and sync is explicit
  ---
  duration_ms: 5.138242
  ...
# Subtest: missing bob waits for new demand instead of polling every debounce interval
ok 1108 - missing bob waits for new demand instead of polling every debounce interval
  ---
  duration_ms: 4.27833
  ...
# Subtest: failed invalidation refresh keeps cached rows and concurrent waiters settle without another attempt
ok 1109 - failed invalidation refresh keeps cached rows and concurrent waiters settle without another attempt
  ---
  duration_ms: 1.889679
  ...
# Subtest: a vault change during a failed fetch still gets one refresh for the newer generation
ok 1110 - a vault change during a failed fetch still gets one refresh for the newer generation
  ---
  duration_ms: 13.893801
  ...
# Subtest: api.attachments v1 sends origin and import requests to bob
ok 1111 - api.attachments v1 sends origin and import requests to bob
  ---
  duration_ms: 2.324518
  ...
# Subtest: origin and import decoders validate schema and payload shape
ok 1112 - origin and import decoders validate schema and payload shape
  ---
  duration_ms: 1.233335
  ...
# Subtest: attachment API preserves bob payloads through bobSpawnJson
ok 1113 - attachment API preserves bob payloads through bobSpawnJson
  ---
  duration_ms: 3.80163
  ...
# Subtest: attachment API passes bob JSON failures through
ok 1114 - attachment API passes bob JSON failures through
  ---
  duration_ms: 2.019196
  ...
# Subtest: attachment API refuses mobile calls and never rejects
ok 1115 - attachment API refuses mobile calls and never rejects
  ---
  duration_ms: 0.394263
  ...
# Subtest: ensure argv never passes -o and ack argv carries only deduped IDs
ok 1116 - ensure argv never passes -o and ack argv carries only deduped IDs
  ---
  duration_ms: 2.91694
  ...
# Subtest: ensure and ack decoders reject bad shapes without claiming success
ok 1117 - ensure and ack decoders reject bad shapes without claiming success
  ---
  duration_ms: 1.029866
  ...
# Subtest: source rows expose bank ids; other block ids stay plain block ids
ok 1118 - source rows expose bank ids; other block ids stay plain block ids
  ---
  duration_ms: 2.13688
  ...
# Subtest: day snapshots carry exact waiting IDs and count ID-less rows
ok 1119 - day snapshots carry exact waiting IDs and count ID-less rows
  ---
  duration_ms: 0.805669
  ...
# Subtest: ack summaries never claim a full day while ID-less rows remain
ok 1120 - ack summaries never claim a full day while ID-less rows remain
  ---
  duration_ms: 0.360618
  ...
# Subtest: cursor day context follows heading boundaries, not fallback lines
ok 1121 - cursor day context follows heading boundaries, not fallback lines
  ---
  duration_ms: 0.932
  ...
# Subtest: guarded checkbox plans verify the exact displayed row and day context
ok 1122 - guarded checkbox plans verify the exact displayed row and day context
  ---
  duration_ms: 1.002635
  ...
# Subtest: Enter continues only complete rows and clears only empty stubs
ok 1123 - Enter continues only complete rows and clears only empty stubs
  ---
  duration_ms: 0.617379
  ...
# Subtest: category completions keep declared order and insert only keys
ok 1124 - category completions keep declared order and insert only keys
  ---
  duration_ms: 0.75375
  ...
# Subtest: action commands register without default hotkeys
ok 1125 - action commands register without default hotkeys
  ---
  duration_ms: 0.998447
  ...
# Subtest: ack submits the exact snapshot IDs and reports remaining ID-less rows
ok 1126 - ack submits the exact snapshot IDs and reports remaining ID-less rows
  ---
  duration_ms: 2.483923
  ...
# Subtest: ack refuses empty selections, busy locks, and failures without refresh
ok 1127 - ack refuses empty selections, busy locks, and failures without refresh
  ---
  duration_ms: 1.028645
  ...
# Subtest: acknowledge-day snapshots the cursor day and never falls back to ack -D
ok 1128 - acknowledge-day snapshots the cursor day and never falls back to ack -D
  ---
  duration_ms: 1.679808
  ...
# Subtest: ensure opens the returned path and lands the cursor on the next row
ok 1129 - ensure opens the returned path and lands the cursor on the next row
  ---
  duration_ms: 1.512428
  ...
# Subtest: guarded ID-less edits flip one byte only when the snapshot still matches
ok 1130 - guarded ID-less edits flip one byte only when the snapshot still matches
  ---
  duration_ms: 0.562955
  ...
# Subtest: snippet expansion never rewrites bank rows
ok 1131 - snippet expansion never rewrites bank rows
  ---
  duration_ms: 0.407589
  ...
# Subtest: Enter handling inserts rows and clears stubs through the real editor
ok 1132 - Enter handling inserts rows and clears stubs through the real editor
  ---
  duration_ms: 0.604093
  ...
# Subtest: strip, badge, and period hosts land on period fences; day fences keep two
ok 1133 - strip, badge, and period hosts land on period fences; day fences keep two
  ---
  duration_ms: 95.725685
  ...
# Subtest: a strip repaint keeps the badge node
ok 1134 - a strip repaint keeps the badge node
  ---
  duration_ms: 38.469881
  ...
# Subtest: each strip kind fetches the matching bank report args
ok 1135 - each strip kind fetches the matching bank report args
  ---
  duration_ms: 145.643676
  ...
# Subtest: fence badges wait for visibility and skip future periods
ok 1136 - fence badges wait for visibility and skip future periods
  ---
  duration_ms: 96.591448
  ...
# Subtest: older bob -p refusals hide the host and warn once
ok 1137 - older bob -p refusals hide the host and warn once
  ---
  duration_ms: 143.11687
  ...
# Subtest: unload unsubscribes and pref off clears every fence badge
ok 1138 - unload unsubscribes and pref off clears every fence badge
  ---
  duration_ms: 264.88187
  ...
# Subtest: hidden fences subscribe once they become visible without an observer
ok 1139 - hidden fences subscribe once they become visible without an observer
  ---
  duration_ms: 107.654884
  ...
# Subtest: day fences retry badge subscription when shown later without an observer
ok 1140 - day fences retry badge subscription when shown later without an observer
  ---
  duration_ms: 209.887514
  ...
# Subtest: losing periodId in the host adapter cannot silently undo validation
ok 1141 - losing periodId in the host adapter cannot silently undo validation
  ---
  duration_ms: 122.23773
  ...
# Subtest: opening a waiting badge row selects family b and sets the walk anchor
ok 1142 - opening a waiting badge row selects family b and sets the walk anchor
  ---
  duration_ms: 107.902568
  ...
# Subtest: heading and hub badge opens leave the family and walk anchor alone
ok 1143 - heading and hub badge opens leave the family and walk anchor alone
  ---
  duration_ms: 161.485306
  ...
# Subtest: old nav still anchors a waiting badge open and skips select
ok 1144 - old nav still anchors a waiting badge open and skips select
  ---
  duration_ms: 171.985747
  ...
# Subtest: bank card fence and filename frontmatter validation are explicit
ok 1145 - bank card fence and filename frontmatter validation are explicit
  ---
  duration_ms: 4.515553
  ...
# Subtest: unknown bob-bank views render nothing
ok 1146 - unknown bob-bank views render nothing
  ---
  duration_ms: 9.992832
  ...
# Subtest: month card model keeps Bob totals, ordered category shares, account caveats, and waiting row
ok 1147 - month card model keeps Bob totals, ordered category shares, account caveats, and waiting row
  ---
  duration_ms: 1.554489
  ...
# Subtest: heat strip is Monday-first, includes the whole month, and ties share a quantile
ok 1148 - heat strip is Monday-first, includes the whole month, and ties share a quantile
  ---
  duration_ms: 0.484636
  ...
# Subtest: queue model sorts oldest-first, snapshots displayed IDs, and bounds existing month footer to six
ok 1149 - queue model sorts oldest-first, snapshots displayed IDs, and bounds existing month footer to six
  ---
  duration_ms: 12.188114
  ...
# Subtest: bank badge model hides empty periods and selects copy and tone from counted cents
ok 1150 - bank badge model hides empty periods and selects copy and tone from counted cents
  ---
  duration_ms: 2.608511
  ...
# Subtest: bank badge rejects mismatches, hides teaching-empty and future reports, and keeps stale state
ok 1151 - bank badge rejects mismatches, hides teaching-empty and future reports, and keeps stale state
  ---
  duration_ms: 0.901752
  ...
# Subtest: bank badge enforces period identity at the boundary
ok 1152 - bank badge enforces period identity at the boundary
  ---
  duration_ms: 1.493882
  ...
# Subtest: bank badge quarter amounts round half up but preserve nonzero cents below one dollar
ok 1153 - bank badge quarter amounts round half up but preserve nonzero cents below one dollar
  ---
  duration_ms: 0.804597
  ...
# Subtest: bank badge coverage copy handles partial starts, short imports, both bounds, and all time
ok 1154 - bank badge coverage copy handles partial starts, short imports, both bounds, and all time
  ---
  duration_ms: 2.869179
  ...
# Subtest: bank badge chooses waiting, strip-first, one-month, hub, and old-bob targets
ok 1155 - bank badge chooses waiting, strip-first, one-month, hub, and old-bob targets
  ---
  duration_ms: 1.485677
  ...
# Subtest: today-only all-month waiting is tooltip-only
ok 1156 - today-only all-month waiting is tooltip-only
  ---
  duration_ms: 0.286317
  ...
# Subtest: bank badge painter uses one accessible span, joins present parts, and leaves hidden hosts empty
ok 1157 - bank badge painter uses one accessible span, joins present parts, and leaves hidden hosts empty
  ---
  duration_ms: 5.095591
  ...
# Subtest: month card renders report data and disables days without real headings
ok 1158 - month card renders report data and disables days without real headings
  ---
  duration_ms: 17.135401
  ...
# Subtest: queue card keeps account caveats visible, lists bounded report months, and sends its drawn ID snapshot
ok 1159 - queue card keeps account caveats visible, lists bounded report months, and sends its drawn ID snapshot
  ---
  duration_ms: 4.045455
  ...
# Subtest: queue card weekly-import chip previews the exact argv in Command Mode
ok 1160 - queue card weekly-import chip previews the exact argv in Command Mode
  ---
  duration_ms: 5.754609
  ...
# Subtest: queue card weekly-import chip falls back to a notice without Command Mode
ok 1161 - queue card weekly-import chip falls back to a notice without Command Mode
  ---
  duration_ms: 2.704534
  ...
# Subtest: queue card weekly-import chip stays quiet when preview settles refused
ok 1162 - queue card weekly-import chip stays quiet when preview settles refused
  ---
  duration_ms: 2.230019
  ...
# Subtest: queue card paints a subscription chip after the category
ok 1163 - queue card paints a subscription chip after the category
  ---
  duration_ms: 1.579556
  ...
# Subtest: missing day headings and changed row snapshots cannot navigate to fallback line one
ok 1164 - missing day headings and changed row snapshots cannot navigate to fallback line one
  ---
  duration_ms: 0.745263
  ...
# Subtest: daily badge mounts after the day strip and click opens its read-only target
ok 1165 - daily badge mounts after the day strip and click opens its read-only target
  ---
  duration_ms: 8.232731
  ...
# Subtest: daily badge is hidden without bank.md and follows the cached persistent default-on preference
ok 1166 - daily badge is hidden without bank.md and follows the cached persistent default-on preference
  ---
  duration_ms: 4.501747
  ...
# Subtest: stats.bank_badge overrides the stats.bank_chip legacy alias, which defaults on
ok 1167 - stats.bank_badge overrides the stats.bank_chip legacy alias, which defaults on
  ---
  duration_ms: 9.009414
  ...
# Subtest: badge modifier navigation opens a new leaf without saving a bank note
ok 1168 - badge modifier navigation opens a new leaf without saving a bank note
  ---
  duration_ms: 0.802222
  ...
# Subtest: disabled render children unsubscribe and unload blocks later repaint
ok 1169 - disabled render children unsubscribe and unload blocks later repaint
  ---
  duration_ms: 2.564357
  ...
# Subtest: bank UI keeps narrow-pane stacking and badge CSS has the approved tones and focus
ok 1170 - bank UI keeps narrow-pane stacking and badge CSS has the approved tones and focus
  ---
  duration_ms: 3.315041
  ...
# Subtest: bank card actions use the public API, while badges navigate without ensure writes
ok 1171 - bank card actions use the public API, while badges navigate without ensure writes
  ---
  duration_ms: 4.398249
  ...
# Subtest: the modal key contract dispatches every action in close and set modes
ok 1172 - the modal key contract dispatches every action in close and set modes
  ---
  duration_ms: 6.914785
  ...
# Subtest: new-category lockNotice paints without Preview again and keeps Save
ok 1173 - new-category lockNotice paints without Preview again and keeps Save
  ---
  duration_ms: 1.050446
  ...
# Subtest: plus opens the new-category stage and letters no longer file
ok 1174 - plus opens the new-category stage and letters no longer file
  ---
  duration_ms: 1.005991
  ...
# Subtest: the opening chord and landing lock swallow repeated Ctrl+Enter
ok 1175 - the opening chord and landing lock swallow repeated Ctrl+Enter
  ---
  duration_ms: 0.582502
  ...
# Subtest: old Bob uses arrow navigation and Enter when no category has a hotkey
ok 1176 - old Bob uses arrow navigation and Enter when no category has a hotkey
  ---
  duration_ms: 0.491329
  ...
# Subtest: hidden categories are absent from completions and one line edit combines the write
ok 1177 - hidden categories are absent from completions and one line edit combines the write
  ---
  duration_ms: 0.452684
  ...
# Subtest: api.bank v2 exposes guarded close and set-category actions plus the command
ok 1178 - api.bank v2 exposes guarded close and set-category actions plus the command
  ---
  duration_ms: 0.754801
  ...
# Subtest: close commits once, refreshes, and lands at the next payee in the same note
ok 1179 - close commits once, refreshes, and lands at the next payee in the same note
  ---
  duration_ms: 6.883514
  ...
# Subtest: a rejected month refresh after a successful close still clears waitingRefresh
ok 1180 - a rejected month refresh after a successful close still clears waitingRefresh
  ---
  duration_ms: 1.601939
  ...
# Subtest: a landed context exposes cardRow so a learned report highlights for Ctrl+Enter
ok 1181 - a landed context exposes cardRow so a learned report highlights for Ctrl+Enter
  ---
  duration_ms: 1.270476
  ...
# Subtest: a close landing records a jump when nav provides recordJump
ok 1182 - a close landing records a jump when nav provides recordJump
  ---
  duration_ms: 1.564407
  ...
# Subtest: claimRowClose focuses an open card and swallows the lock instead of flipping
ok 1183 - claimRowClose focuses an open card and swallows the lock instead of flipping
  ---
  duration_ms: 0.452013
  ...
# Subtest: the painted root uses bob-bank-category-card and not the month-card token
ok 1184 - the painted root uses bob-bank-category-card and not the month-card token
  ---
  duration_ms: 2.50322
  ...
# Subtest: the header puts amount first, inflows show +, and progress names the month
ok 1185 - the header puts amount first, inflows show +, and progress names the month
  ---
  duration_ms: 2.489524
  ...
# Subtest: tiles render keycaps, aria-keyshortcuts, and a live region after filing
ok 1186 - tiles render keycaps, aria-keyshortcuts, and a live region after filing
  ---
  duration_ms: 1.207536
  ...
# Subtest: the subscription context strip sits above tiles and the picker exposes an accessible list
ok 1187 - the subscription context strip sits above tiles and the picker exposes an accessible list
  ---
  duration_ms: 1.770361
  ...
# Subtest: the completion state paints the other-month ]b walk line
ok 1188 - the completion state paints the other-month ]b walk line
  ---
  duration_ms: 0.591209
  ...
# Subtest: restricted mode shows only acknowledge keys and the loading reason
ok 1189 - restricted mode shows only acknowledge keys and the loading reason
  ---
  duration_ms: 0.631436
  ...
# Subtest: set-category replaces the category without ticking or advancing
ok 1190 - set-category replaces the category without ticking or advancing
  ---
  duration_ms: 0.880651
  ...
# Subtest: a successful close saves the note before requesting a refresh
ok 1191 - a successful close saves the note before requesting a refresh
  ---
  duration_ms: 1.20965
  ...
# Subtest: a throwing save still refreshes after a successful close
ok 1192 - a throwing save still refreshes after a successful close
  ---
  duration_ms: 1.014928
  ...
# Subtest: the scope catch-all is registered once and replaces the contentEl keydown listener
ok 1193 - the scope catch-all is registered once and replaces the contentEl keydown listener
  ---
  duration_ms: 0.50289
  ...
# Subtest: real-path scope keys file, accept, and move while swallowing every key
ok 1194 - real-path scope keys file, accept, and move while swallowing every key
  ---
  duration_ms: 26.227283
  ...
# Subtest: unbound scope keys are swallowed with no filing and the card stays open
ok 1195 - unbound scope keys are swallowed with no filing and the card stays open
  ---
  duration_ms: 3.636915
  ...
# Subtest: modifier letters never file while Shift+letter still files
ok 1196 - modifier letters never file while Shift+letter still files
  ---
  duration_ms: 6.000829
  ...
# Subtest: held-key repeats never file but repeats still move the highlight
ok 1197 - held-key repeats never file but repeats still move the highlight
  ---
  duration_ms: 8.578511
  ...
# Subtest: busy, waiting, and summary states swallow scope keys with no action
ok 1198 - busy, waiting, and summary states swallow scope keys with no action
  ---
  duration_ms: 6.623398
  ...
# Subtest: onClose unregisters the scope catch-all
ok 1199 - onClose unregisters the scope catch-all
  ---
  duration_ms: 0.466601
  ...
# Subtest: without a scope the fallback contentEl keydown listener still files
ok 1200 - without a scope the fallback contentEl keydown listener still files
  ---
  duration_ms: 0.35128
  ...
# Subtest: decode keeps hotkey, group, hidden, and suggestion; old bob degrades
ok 1201 - decode keeps hotkey, group, hidden, and suggestion; old bob degrades
  ---
  duration_ms: 5.32585
  ...
# Subtest: card sections follow first-appearance order; hidden never renders; inflow reorders
ok 1202 - card sections follow first-appearance order; hidden never renders; inflow reorders
  ---
  duration_ms: 1.300303
  ...
# Subtest: highlight follows row category then suggestion; each footer variant
ok 1203 - highlight follows row category then suggestion; each footer variant
  ---
  duration_ms: 2.28359
  ...
# Subtest: key table is case-insensitive; q/Esc cancel; chord and lock are pure state
ok 1204 - key table is case-insensitive; q/Esc cancel; chord and lock are pure state
  ---
  duration_ms: 0.677254
  ...
# Subtest: write planner inserts, replaces, and removes in one line; refusals carry the notice
ok 1205 - write planner inserts, replaces, and removes in one line; refusals carry the notice
  ---
  duration_ms: 4.92241
  ...
# Subtest: write planner resolves imported rows by ID and handles CRLF
ok 1206 - write planner resolves imported rows by ID and handles CRLF
  ---
  duration_ms: 0.744812
  ...
# Subtest: next-waiting finder walks in order, wraps once, and skips non-rows
ok 1207 - next-waiting finder walks in order, wraps once, and skips non-rows
  ---
  duration_ms: 1.263182
  ...
# Subtest: session counts progress and the summary owns every number
ok 1208 - session counts progress and the summary owns every number
  ---
  duration_ms: 1.000801
  ...
# Subtest: other-month walk line names the oldest waiting month from the snapshot
ok 1209 - other-month walk line names the oldest waiting month from the snapshot
  ---
  duration_ms: 2.838661
  ...
# Subtest: close advances in note order and anchors the landed waiting row
ok 1210 - close advances in note order and anchors the landed waiting row
  ---
  duration_ms: 4.125197
  ...
# Subtest: completing a month anchors the last filed row and surfaces the other-month ]b line
ok 1211 - completing a month anchors the last filed row and surfaces the other-month ]b line
  ---
  duration_ms: 2.75459
  ...
# Subtest: completion omits the other-month ]b line when the snapshot has no other waiting months
ok 1212 - completion omits the other-month ]b line when the snapshot has no other waiting months
  ---
  duration_ms: 1.426815
  ...
# Subtest: update argv, envelope, and timeout follow the guarded writer contract
ok 1213 - update argv, envelope, and timeout follow the guarded writer contract
  ---
  duration_ms: 2.74908
  ...
# Subtest: update decoder keeps typed refusals and the derived stored key
ok 1214 - update decoder keeps typed refusals and the derived stored key
  ---
  duration_ms: 1.31413
  ...
# Subtest: list and report keep config_fingerprint for the guarded expect
ok 1215 - list and report keep config_fingerprint for the guarded expect
  ---
  duration_ms: 0.580619
  ...
# Subtest: stdin carries shell-looking labels byte-identical and never as shell text
ok 1216 - stdin carries shell-looking labels byte-identical and never as shell text
  ---
  duration_ms: 3.483923
  ...
# Subtest: own bank.md echo is suppressed while apply is in flight
ok 1217 - own bank.md echo is suppressed while apply is in flight
  ---
  duration_ms: 0.716999
  ...
# Subtest: preview debounce, matching apply, and double Enter share one flight
ok 1218 - preview debounce, matching apply, and double Enter share one flight
  ---
  duration_ms: 3.024766
  ...
# Subtest: Enter is inert without a matching preview; apply failure files nothing
ok 1219 - Enter is inert without a matching preview; apply failure files nothing
  ---
  duration_ms: 0.942831
  ...
# Subtest: stale_config rebases; sync retry never replays the mutation
ok 1220 - stale_config rebases; sync retry never replays the mutation
  ---
  duration_ms: 1.13631
  ...
# Subtest: stage defaults the group, cycles it, and keeps taken or reserved keys inert
ok 1221 - stage defaults the group, cycles it, and keeps taken or reserved keys inert
  ---
  duration_ms: 1.418028
  ...
# Subtest: + and = open the stage; letters type; they never file; Esc closes the stage first
ok 1222 - + and = open the stage; letters type; they never file; Esc closes the stage first
  ---
  duration_ms: 2.556432
  ...
# Subtest: the new-category tile click opens the stage; missing fingerprint refuses
ok 1223 - the new-category tile click opens the stage; missing fingerprint refuses
  ---
  duration_ms: 0.488663
  ...
# Subtest: Enter is inert on a taken key and without a matching preview
ok 1224 - Enter is inert on a taken key and without a matching preview
  ---
  duration_ms: 0.729393
  ...
# Subtest: apply-then-file uses the derived key and one choose; failure files nothing
ok 1225 - apply-then-file uses the derived key and one choose; failure files nothing
  ---
  duration_ms: 1.08418
  ...
# Subtest: setCategories repaints after interaction; setReport stays ignored then
ok 1226 - setCategories repaints after interaction; setReport stays ignored then
  ---
  duration_ms: 0.375487
  ...
# Subtest: bank lock_busy waits then retries the same envelope
ok 1227 - bank lock_busy waits then retries the same envelope
  ---
  duration_ms: 1.163822
  ...
# Subtest: the bank service skips forced revalidate on lock_busy
ok 1228 - the bank service skips forced revalidate on lock_busy
  ---
  duration_ms: 0.820286
  ...
# Subtest: new-category Esc during a lock wait stops waiting and keeps the stage open
ok 1229 - new-category Esc during a lock wait stops waiting and keeps the stage open
  ---
  duration_ms: 0.479847
  ...
# Subtest: apply-busy refuses a second plugin apply; timeout is never a blind retry
ok 1230 - apply-busy refuses a second plugin apply; timeout is never a blind retry
  ---
  duration_ms: 0.825496
  ...
# Subtest: bank subprocess uses bobSpawnJson with vault, timeout, and bounded output
ok 1231 - bank subprocess uses bobSpawnJson with vault, timeout, and bounded output
  ---
  duration_ms: 5.743198
  ...
# Subtest: shared bob spawn maps missing binary and timeout failures
ok 1232 - shared bob spawn maps missing binary and timeout failures
  ---
  duration_ms: 2.191585
  ...
# Subtest: bank cache returns stale data while revalidating and keeps a bounded LRU
ok 1233 - bank cache returns stale data while revalidating and keeps a bounded LRU
  ---
  duration_ms: 4.328936
  ...
# Subtest: identical list flights coalesce and different keys spawn in parallel
ok 1234 - identical list flights coalesce and different keys spawn in parallel
  ---
  duration_ms: 0.804066
  ...
# Subtest: a late older generation cannot overwrite a newer cached report
ok 1235 - a late older generation cannot overwrite a newer cached report
  ---
  duration_ms: 0.572243
  ...
# Subtest: failed refresh keeps last good data stale without a retry loop
ok 1236 - failed refresh keeps last good data stale without a retry loop
  ---
  duration_ms: 0.510054
  ...
# Subtest: only hub and canonical month notes invalidate, and debounce coalesces
ok 1237 - only hub and canonical month notes invalidate, and debounce coalesces
  ---
  duration_ms: 2.560039
  ...
# Subtest: config apply refreshes once, updates other mounts, and retains newer invalidations
ok 1238 - config apply refreshes once, updates other mounts, and retains newer invalidations
  ---
  duration_ms: 4.33102
  ...
# Subtest: local midnight bumps generation and command-mode bank tag invalidates
ok 1239 - local midnight bumps generation and command-mode bank tag invalidates
  ---
  duration_ms: 1.358394
  ...
# Subtest: unload clears mounts and a late result cannot repaint
ok 1240 - unload clears mounts and a late result cannot repaint
  ---
  duration_ms: 0.95811
  ...
# Subtest: headless setup does not keep the process alive with a browser rollover timer
ok 1241 - headless setup does not keep the process alive with a browser rollover timer
  ---
  duration_ms: 0.687293
  ...
# Subtest: bank argv is keyed by command and exact flags
ok 1242 - bank argv is keyed by command and exact flags
  ---
  duration_ms: 4.171747
  ...
# Subtest: list decoder accepts the waiting fixture and keeps integer cents
ok 1243 - list decoder accepts the waiting fixture and keeps integer cents
  ---
  duration_ms: 1.092225
  ...
# Subtest: report decoder preserves transfers, cash, inflows, and account caveats
ok 1244 - report decoder preserves transfers, cash, inflows, and account caveats
  ---
  duration_ms: 1.176617
  ...
# Subtest: report decoder validates and passes through optional badge coverage and navigation
ok 1245 - report decoder validates and passes through optional badge coverage and navigation
  ---
  duration_ms: 2.543247
  ...
# Subtest: teaching-empty is success and never a zero-dollar report
ok 1246 - teaching-empty is success and never a zero-dollar report
  ---
  duration_ms: 0.397448
  ...
# Subtest: malformed JSON, schema mismatch, and bob errors never become zero success
ok 1247 - malformed JSON, schema mismatch, and bob errors never become zero success
  ---
  duration_ms: 0.343566
  ...
# Subtest: non-integer cents and numeric payees are rejected
ok 1248 - non-integer cents and numeric payees are rejected
  ---
  duration_ms: 0.800518
  ...
# Subtest: cent formatting is exact and presentation models do not invent totals
ok 1249 - cent formatting is exact and presentation models do not invent totals
  ---
  duration_ms: 0.539069
  ...
# Subtest: bank error cards explain not-found, timeout, schema, and bob errors
ok 1250 - bank error cards explain not-found, timeout, schema, and bob errors
  ---
  duration_ms: 0.824805
  ...
# Subtest: reports without charts decode exactly as today
ok 1251 - reports without charts decode exactly as today
  ---
  duration_ms: 1.085022
  ...
# Subtest: charts decoder accepts a week payload and rejects malformed values with bad-shape
ok 1252 - charts decoder accepts a week payload and rejects malformed values with bad-shape
  ---
  duration_ms: 6.035986
  ...
# Subtest: charts decoder accepts ISO-year groups and null all-time charts
ok 1253 - charts decoder accepts ISO-year groups and null all-time charts
  ---
  duration_ms: 2.940405
  ...
# Subtest: compose and split round-trip fused labels including ZWJ and flags
ok 1254 - compose and split round-trip fused labels including ZWJ and flags
  ---
  duration_ms: 19.342886
  ...
# Subtest: a rename keeps the emoji and an explicit clear removes it
ok 1255 - a rename keeps the emoji and an explicit clear removes it
  ---
  duration_ms: 0.557074
  ...
# Subtest: bank vocabulary is every category emoji; siblings skip hidden and the row being edited
ok 1256 - bank vocabulary is every category emoji; siblings skip hidden and the row being edited
  ---
  duration_ms: 0.519482
  ...
# Subtest: an open panel's Enter picks and never files a new category
ok 1257 - an open panel's Enter picks and never files a new category
  ---
  duration_ms: 1.447534
  ...
# Subtest: the fused slot falls back without bob-emoji and keeps the enable-search hint
ok 1258 - the fused slot falls back without bob-emoji and keeps the enable-search hint
  ---
  duration_ms: 2.1627
  ...
# Subtest: the fused hint shows for an empty slot and follows open, pick, and clear
ok 1259 - the fused hint shows for an empty slot and follows open, pick, and clear
  ---
  duration_ms: 6.335468
  ...
# Subtest: the hint stays hidden for filled, disabled, and fallback slots; the Category card shows it
ok 1260 - the hint stays hidden for filled, disabled, and fallback slots; the Category card shows it
  ---
  duration_ms: 1.019086
  ...
# Subtest: glyph-well stylesheet beats Obsidian button chrome with no hex colors
ok 1261 - glyph-well stylesheet beats Obsidian button chrome with no hex colors
  ---
  duration_ms: 2.531644
  ...
# Subtest: Ctrl+N steps the shared slot by one and the card keeps the key
ok 1262 - Ctrl+N steps the shared slot by one and the card keeps the key
  ---
  duration_ms: 1.926168
  ...
# Subtest: Ctrl+[ closes the open bank Emoji Slot like Esc while q in the search types
ok 1263 - Ctrl+[ closes the open bank Emoji Slot like Esc while q in the search types
  ---
  duration_ms: 0.726116
  ...
# Subtest: tokenizer covers amount variants and tail order including flags, notes, links, and ids
ok 1264 - tokenizer covers amount variants and tail order including flags, notes, links, and ids
  ---
  duration_ms: 4.010759
  ...
# Subtest: source scan never consumes indented children, fences, or ordinary prose
ok 1265 - source scan never consumes indented children, fences, or ordinary prose
  ---
  duration_ms: 2.878637
  ...
# Subtest: presentation keeps unknown labels, greens inflows, and replaces only imported bank ids
ok 1266 - presentation keeps unknown labels, greens inflows, and replaces only imported bank ids
  ---
  duration_ms: 0.949784
  ...
# Subtest: real day headings get report totals or muted nothing posted; missing days stay absent
ok 1267 - real day headings get report totals or muted nothing posted; missing days stay absent
  ---
  duration_ms: 1.083629
  ...
# Subtest: two nearby bank-row dollars form a math conflict; ordinary math is left alone
ok 1268 - two nearby bank-row dollars form a math conflict; ordinary math is left alone
  ---
  duration_ms: 1.121582
  ...
# Subtest: reading-view math unwrap restores bank amounts and leaves ordinary math intact
ok 1269 - reading-view math unwrap restores bank amounts and leaves ordinary math intact
  ---
  duration_ms: 1.35139
  ...
# Subtest: Live Preview replaces amounts off the cursor line, reveals on it, and skips Source mode and code
ok 1270 - Live Preview replaces amounts off the cursor line, reveals on it, and skips Source mode and code
  ---
  duration_ms: 9.266745
  ...
# Subtest: toggle, config, and popout gate control decorations together; math dollars remain when marks are off
ok 1271 - toggle, config, and popout gate control decorations together; math dollars remain when marks are off
  ---
  duration_ms: 1.573104
  ...
# Subtest: Reading view is idempotent, preserves links, and does not rewrite note bytes
ok 1272 - Reading view is idempotent, preserves links, and does not rewrite note bytes
  ---
  duration_ms: 3.975882
  ...
# Subtest: hub property hiding is owned by the setup surface, never by bank marks
ok 1273 - hub property hiding is owned by the setup surface, never by bank marks
  ---
  duration_ms: 1.818643
  ...
# Subtest: Live Preview replaces a 🔁 wikilink with a subscription chip and parks a ghost widget
ok 1274 - Live Preview replaces a 🔁 wikilink with a subscription chip and parks a ghost widget
  ---
  duration_ms: 3.11599
  ...
# Subtest: Reading view wraps a 🔁 internal-link and appends a ghost that restore removes
ok 1275 - Reading view wraps a 🔁 internal-link and appends a ghost that restore removes
  ---
  duration_ms: 3.327614
  ...
# Subtest: cursor reveal helper and note bytes stay unchanged after tokenize
ok 1276 - cursor reveal helper and note bytes stay unchanged after tokenize
  ---
  duration_ms: 0.436593
  ...
# Subtest: malformed balances warn once and never fail the report
ok 1277 - malformed balances warn once and never fail the report
  ---
  duration_ms: 3.001492
  ...
# Subtest: balances decode: absent stays absent, null stays null, valid normalizes
ok 1278 - balances decode: absent stays absent, null stays null, valid normalizes
  ---
  duration_ms: 10.10164
  ...
# Subtest: balance model: as_of golden with tooltip, aria, and activation
ok 1279 - balance model: as_of golden with tooltip, aria, and activation
  ---
  duration_ms: 1.60231
  ...
# Subtest: balance model: settled names the close and drops the not-imported line
ok 1280 - balance model: settled names the close and drops the not-imported line
  ---
  duration_ms: 0.446082
  ...
# Subtest: balance model: so_far says so far, flags stale, and reads today
ok 1281 - balance model: so_far says so far, flags stale, and reads today
  ---
  duration_ms: 0.622448
  ...
# Subtest: balance model: words states, negative and zero amounts
ok 1282 - balance model: words states, negative and zero amounts
  ---
  duration_ms: 0.787835
  ...
# Subtest: balance model: delta status adds a ledger line; null without hero or numbers
ok 1283 - balance model: delta status adds a ledger line; null without hero or numbers
  ---
  duration_ms: 0.675841
  ...
# Subtest: charts model: older-bob, missing hero, and none stay byte-identical
ok 1284 - charts model: older-bob, missing hero, and none stay byte-identical
  ---
  duration_ms: 21.56504
  ...
# Subtest: charts model: quiet weeks and waiting-badge weeks become header-only balance states
ok 1285 - charts model: quiet weeks and waiting-badge weeks become header-only balance states
  ---
  duration_ms: 2.215671
  ...
# Subtest: paint: header order, link role, and inert balance
ok 1286 - paint: header order, link role, and inert balance
  ---
  duration_ms: 8.324336
  ...
# Subtest: paint: header-only root, waiting line, and collapsed panels
ok 1287 - paint: header-only root, waiting line, and collapsed panels
  ---
  duration_ms: 2.081945
  ...
# Subtest: real bob JSON decodes into models and paints through the period host
ok 1288 - real bob JSON decodes into models and paints through the period host
  ---
  duration_ms: 112.413691
  ...
# Subtest: only non-day strip fences mount a third host, and future or unsupported hosts do not subscribe
ok 1289 - only non-day strip fences mount a third host, and future or unsupported hosts do not subscribe
  ---
  duration_ms: 161.088971
  ...
# Subtest: the period fetch waits for visibility and has a cache key separate from the badge
ok 1290 - the period fetch waits for visibility and has a cache key separate from the badge
  ---
  duration_ms: 81.368147
  ...
# Subtest: the no-observer hidden-to-shown retry subscribes once
ok 1291 - the no-observer hidden-to-shown retry subscribes once
  ---
  duration_ms: 90.45476
  ...
# Subtest: bank_period and bank_badge gate independently; older bob warns once
ok 1292 - bank_period and bank_badge gate independently; older bob warns once
  ---
  duration_ms: 218.873653
  ...
# Subtest: read-only navigation, isolated repaint, persistence, and release work
ok 1293 - read-only navigation, isolated repaint, persistence, and release work
  ---
  duration_ms: 619.244326
  ...
# Subtest: the panel's waiting link hands the row to bank walk family b like the badge
ok 1294 - the panel's waiting link hands the row to bank walk family b like the badge
  ---
  duration_ms: 368.012545
  ...
# Subtest: compact labels follow the k/m ladder and keep sub-dollar cents
ok 1295 - compact labels follow the k/m ladder and keep sub-dollar cents
  ---
  duration_ms: 1.84327
  ...
# Subtest: invalid persisted view and collapsed values fall back to both / expanded
ok 1296 - invalid persisted view and collapsed values fall back to both / expanded
  ---
  duration_ms: 8.087143
  ...
# Subtest: panel model states: teaching-empty, older-bob, unavailable, empty, waiting, charts, stale
ok 1297 - panel model states: teaching-empty, older-bob, unavailable, empty, waiting, charts, stale
  ---
  duration_ms: 3.752265
  ...
# Subtest: hide rule with the badge on and off, and waiting-only copy
ok 1298 - hide rule with the badge on and off, and waiting-only copy
  ---
  duration_ms: 5.075142
  ...
# Subtest: today's real shape: one counted day, six awaiting_import, $249.77 out
ok 1299 - today's real shape: one counted day, six awaiting_import, $249.77 out
  ---
  duration_ms: 1.400514
  ...
# Subtest: in-only shows cashflow and hides the view switch
ok 1300 - in-only shows cashflow and hides the view switch
  ---
  duration_ms: 0.84285
  ...
# Subtest: week markers hang Out below the line; mirrored ratios collapse a zero side
ok 1301 - week markers hang Out below the line; mirrored ratios collapse a zero side
  ---
  duration_ms: 4.302696
  ...
# Subtest: categories keep pinned cash/unclassified, rest, and the one-leftover series row
ok 1302 - categories keep pinned cash/unclassified, rest, and the one-leftover series row
  ---
  duration_ms: 6.666109
  ...
# Subtest: every bucket state has words, decorations, and table-twin rows
ok 1303 - every bucket state has words, decorations, and table-twin rows
  ---
  duration_ms: 3.097585
  ...
# Subtest: period identity uses the badge rule: wrong key or right key with wrong bounds
ok 1304 - period identity uses the badge rule: wrong key or right key with wrong bounds
  ---
  duration_ms: 0.802923
  ...
# Subtest: 14-week Q4, 53-week ISO year fallback, all-time leading ghost, year grain, null charts, single bucket
ok 1305 - 14-week Q4, 53-week ISO year fallback, all-time leading ghost, year grain, null charts, single bucket
  ---
  duration_ms: 3.239426
  ...
# Subtest: not-counted parts omit badge waiting when the badge is on, and include it when off
ok 1306 - not-counted parts omit badge waiting when the badge is on, and include it when off
  ---
  duration_ms: 0.802282
  ...
# Subtest: digest changes when the view, collapse, or stale flag changes
ok 1307 - digest changes when the view, collapse, or stale flag changes
  ---
  duration_ms: 0.965573
  ...
# Subtest: decoded -c JSON round-trips through the panel model
ok 1308 - decoded -c JSON round-trips through the panel model
  ---
  duration_ms: 1.995952
  ...
# Subtest: textContent reads naturally with real separators, not CSS content
ok 1309 - textContent reads naturally with real separators, not CSS content
  ---
  duration_ms: 11.345585
  ...
# Subtest: child order and roles carry no button element
ok 1310 - child order and roles carry no button element
  ---
  duration_ms: 3.682452
  ...
# Subtest: aria labels name the period, money, top category, and coverage
ok 1311 - aria labels name the period, money, top category, and coverage
  ---
  duration_ms: 2.046268
  ...
# Subtest: the cashflow axis keeps one roving tab stop across arrows, Home, and End
ok 1312 - the cashflow axis keeps one roving tab stop across arrows, Home, and End
  ---
  duration_ms: 3.364575
  ...
# Subtest: hover and focus dim siblings and fill the readout; Escape clears it
ok 1313 - hover and focus dim siblings and fill the readout; Escape clears it
  ---
  duration_ms: 2.410252
  ...
# Subtest: Enter, Space, click, Ctrl-click, and middle-click activate with newLeaf
ok 1314 - Enter, Space, click, Ctrl-click, and middle-click activate with newLeaf
  ---
  duration_ms: 2.446612
  ...
# Subtest: the view switch cycles and the disclosure collapses
ok 1315 - the view switch cycles and the disclosure collapses
  ---
  duration_ms: 3.785168
  ...
# Subtest: table twins carry cashflow and category rows with exact copy
ok 1316 - table twins carry cashflow and category rows with exact copy
  ---
  duration_ms: 2.261238
  ...
# Subtest: stale paints last-good values with a dashed edge and a hint
ok 1317 - stale paints last-good values with a dashed edge and a hint
  ---
  duration_ms: 1.802071
  ...
# Subtest: unavailable paints one muted line with a hint title
ok 1318 - unavailable paints one muted line with a hint title
  ---
  duration_ms: 0.662294
  ...
# Subtest: hidden states empty the host
ok 1319 - hidden states empty the host
  ---
  duration_ms: 0.373033
  ...
# Subtest: waiting paints one quiet line that opens the waiting target
ok 1320 - waiting paints one quiet line that opens the waiting target
  ---
  duration_ms: 0.385706
  ...
# Subtest: a category label containing markup renders literally
ok 1321 - a category label containing markup renders literally
  ---
  duration_ms: 0.982617
  ...
# Subtest: collapsed shows only the header row
ok 1322 - collapsed shows only the header row
  ---
  duration_ms: 0.565129
  ...
# Subtest: a single available chart shows alone and hides the switch
ok 1323 - a single available chart shows alone and hides the switch
  ---
  duration_ms: 1.160296
  ...
# Subtest: ghost columns are inert while real columns stay activatable
ok 1324 - ghost columns are inert while real columns stay activatable
  ---
  duration_ms: 0.671642
  ...
# Subtest: contrast tokens ship calibrated fills and keep state words meaningful
ok 1325 - contrast tokens ship calibrated fills and keep state words meaningful
  ---
  duration_ms: 3.531123
  ...
# Subtest: category, group, and rule multi-moves each compile one envelope without a confirm stage
ok 1326 - category, group, and rule multi-moves each compile one envelope without a confirm stage
  ---
  duration_ms: 87.873581
  ...
# Subtest: quiet category saves on one Enter; rule moves confirm; dry-run mismatch blocks; G→H badges paint
ok 1327 - quiet category saves on one Enter; rule moves confirm; dry-run mismatch blocks; G→H badges paint
  ---
  duration_ms: 83.276912
  ...
# Subtest: Ctrl+Z ladders, region identity, Alt chords by code, and ⌥M never hijacks hotkey letters
ok 1328 - Ctrl+Z ladders, region identity, Alt chords by code, and ⌥M never hijacks hotkey letters
  ---
  duration_ms: 94.259666
  ...
# Subtest: category moves clamp at the group edge and Money is not auto-reordered on open
ok 1329 - category moves clamp at the group edge and Money is not auto-reordered on open
  ---
  duration_ms: 8.139473
  ...
# Subtest: q and Ctrl+[ leave gap-hint mode without picking a gap
ok 1330 - q and Ctrl+[ leave gap-hint mode without picking a gap
  ---
  duration_ms: 19.643461
  ...
# Subtest: hint badge letters never claim Ctrl+[ and dirty moves revert through backOut
ok 1331 - hint badge letters never claim Ctrl+[ and dirty moves revert through backOut
  ---
  duration_ms: 19.702133
  ...
# Subtest: group jumps walk painted groups with parent-first K and HIDDEN last
ok 1332 - group jumps walk painted groups with parent-first K and HIDDEN last
  ---
  duration_ms: 63.90943
  ...
# Subtest: Ctrl+K jumps before hotkeys while lowercase hotkeys still select
ok 1333 - Ctrl+K jumps before hotkeys while lowercase hotkeys still select
  ---
  duration_ms: 13.925702
  ...
# Subtest: jumps stay inert on other tabs and behind every gate
ok 1334 - jumps stay inert on other tabs and behind every gate
  ---
  duration_ms: 21.860293
  ...
# Subtest: projected group order drives Ctrl+J and the arrows while dirty
ok 1335 - projected group order drives Ctrl+J and the arrows while dirty
  ---
  duration_ms: 56.162826
  ...
# Subtest: current-group label, footer hint, silence, and reduced-motion bumps
ok 1336 - current-group label, footer hint, silence, and reduced-motion bumps
  ---
  duration_ms: 44.408962
  ...
# Subtest: config decode keeps every report field and tolerates absent ones
ok 1337 - config decode keeps every report field and tolerates absent ones
  ---
  duration_ms: 3.980912
  ...
# Subtest: config decode reads invalid, missing, and teaching-empty states with located findings
ok 1338 - config decode reads invalid, missing, and teaching-empty states with located findings
  ---
  duration_ms: 0.845985
  ...
# Subtest: config decode maps an older bob to unsupported and rejects bad shapes
ok 1339 - config decode maps an older bob to unsupported and rejects bad shapes
  ---
  duration_ms: 0.643609
  ...
# Subtest: config fetch args use the bare config member
ok 1340 - config fetch args use the bare config member
  ---
  duration_ms: 0.750663
  ...
# Subtest: collapsed grammar covers one vs several accounts, hidden counts, and rule plurals
ok 1341 - collapsed grammar covers one vs several accounts, hidden counts, and rule plurals
  ---
  duration_ms: 2.711547
  ...
# Subtest: invalid configs auto-expand and label every finding with its line
ok 1342 - invalid configs auto-expand and label every finding with its line
  ---
  duration_ms: 0.912072
  ...
# Subtest: state selection covers mobile, unsupported, loading, refresh failures, and missing
ok 1343 - state selection covers mobile, unsupported, loading, refresh failures, and missing
  ---
  duration_ms: 1.652956
  ...
# Subtest: tiles enrich keycap style, tooltips, accessible names, and jump lines
ok 1344 - tiles enrich keycap style, tooltips, accessible names, and jump lines
  ---
  duration_ms: 0.565851
  ...
# Subtest: widget identity folds the signature with surface options
ok 1345 - widget identity folds the signature with surface options
  ---
  duration_ms: 0.770101
  ...
# Subtest: tiles follow Category card order and the signature moves with row counts
ok 1346 - tiles follow Category card order and the signature moves with row counts
  ---
  duration_ms: 1.118726
  ...
# Subtest: accounts carry status words and since labels; dead rules are flagged
ok 1347 - accounts carry status words and since labels; dead rules are flagged
  ---
  duration_ms: 0.546183
  ...
# Subtest: shared tile keeps the card look and keys the header apart
ok 1348 - shared tile keeps the card look and keys the header apart
  ---
  duration_ms: 2.214389
  ...
# Subtest: valid header paints collapsed and expanded states with jumps and accessible names
ok 1349 - valid header paints collapsed and expanded states with jumps and accessible names
  ---
  duration_ms: 3.264453
  ...
# Subtest: invalid header auto-expands with a live-region banner and a last-good note
ok 1350 - invalid header auto-expands with a live-region banner and a last-good note
  ---
  duration_ms: 1.224769
  ...
# Subtest: missing, unsupported, mobile, and failed states paint their lines
ok 1351 - missing, unsupported, mobile, and failed states paint their lines
  ---
  duration_ms: 1.380616
  ...
# Subtest: lint marks map through edits and drop from edited lines
ok 1352 - lint marks map through edits and drop from edited lines
  ---
  duration_ms: 0.771664
  ...
# Subtest: setup registers surfaces on desktop and skips the fetch on mobile
ok 1353 - setup registers surfaces on desktop and skips the fetch on mobile
  ---
  duration_ms: 115.159604
  ...
# Subtest: hub mounts once per surface, survives repaint, and leaves other notes alone
ok 1354 - hub mounts once per surface, survives repaint, and leaves other notes alone
  ---
  duration_ms: 4.213316
  ...
# Subtest: setup header starts expanded and collapses per hub in view state
ok 1355 - setup header starts expanded and collapses per hub in view state
  ---
  duration_ms: 4.427535
  ...
# Subtest: hiding never touches document.body and is owned only by bob-bank-setup-surface
ok 1356 - hiding never touches document.body and is owned only by bob-bank-setup-surface
  ---
  duration_ms: 1.09976
  ...
# Subtest: tile, account, and finding jumps open Source mode on the exact line
ok 1357 - tile, account, and finding jumps open Source mode on the exact line
  ---
  duration_ms: 0.576321
  ...
# Subtest: queue card points at Setup instead of the raw first message
ok 1358 - queue card points at Setup instead of the raw first message
  ---
  duration_ms: 0.634131
  ...
# Subtest: Setup card model preserves Category-card order and maps category gestures to guarded ops
ok 1359 - Setup card model preserves Category-card order and maps category gestures to guarded ops
  ---
  duration_ms: 1.749972
  ...
# Subtest: Setup card selects by key, protects focused typing, and stages shared New category input
ok 1360 - Setup card selects by key, protects focused typing, and stages shared New category input
  ---
  duration_ms: 7.848408
  ...
# Subtest: Setup checks YAML action preserves its located line through one delegated click
ok 1361 - Setup checks YAML action preserves its located line through one delegated click
  ---
  duration_ms: 1.268813
  ...
# Subtest: Setup card requires a current preview before Apply and exposes the shared Undo stage
ok 1362 - Setup card requires a current preview before Apply and exposes the shared Undo stage
  ---
  duration_ms: 26.345118
  ...
# Subtest: stale Setup preview refreshes data, keeps the draft, and waits for explicit re-preview
ok 1363 - stale Setup preview refreshes data, keeps the draft, and waits for explicit re-preview
  ---
  duration_ms: 13.485412
  ...
# Subtest: invalid config opens Checks read-only and the palette command is registered
ok 1364 - invalid config opens Checks read-only and the palette command is registered
  ---
  duration_ms: 1.227424
  ...
# Subtest: Setup card paints its loading shell before the first report arrives
ok 1365 - Setup card paints its loading shell before the first report arrives
  ---
  duration_ms: 1.234507
  ...
# Subtest: bank YAML Done stays on an invalid line and returns only after a valid fresh report
ok 1366 - bank YAML Done stays on an invalid line and returns only after a valid fresh report
  ---
  duration_ms: 1.097175
  ...
# Subtest: valid bank YAML Done restores the prior view and reopens the card selection
ok 1367 - valid bank YAML Done restores the prior view and reopens the card selection
  ---
  duration_ms: 0.619222
  ...
# Subtest: Setup header shows Edit on desktop valid/invalid states and degrades without it on mobile
ok 1368 - Setup header shows Edit on desktop valid/invalid states and degrades without it on mobile
  ---
  duration_ms: 0.944664
  ...
# Subtest: Setup card models accounts, rules, and findings alongside categories
ok 1369 - Setup card models accounts, rules, and findings alongside categories
  ---
  duration_ms: 0.665871
  ...
# Subtest: Setup card maps account, rule, and stale-after gestures to guarded ops
ok 1370 - Setup card maps account, rule, and stale-after gestures to guarded ops
  ---
  duration_ms: 1.250458
  ...
# Subtest: Setup card paints interactive account, rule, and finding rows
ok 1371 - Setup card paints interactive account, rule, and finding rows
  ---
  duration_ms: 2.97467
  ...
# Subtest: Setup card stages account and rule gestures through bob previews
ok 1372 - Setup card stages account and rule gestures through bob previews
  ---
  duration_ms: 11.663082
  ...
# Subtest: Setup card checks Enter jumps to the finding line
ok 1373 - Setup card checks Enter jumps to the finding line
  ---
  duration_ms: 1.464607
  ...
# Subtest: Setup card paints lock wait as pending and Esc stops without closing
ok 1374 - Setup card paints lock wait as pending and Esc stops without closing
  ---
  duration_ms: 1.436984
  ...
# Subtest: q, Ctrl+[, and onEscapeKey stop a lock wait without closing
ok 1375 - q, Ctrl+[, and onEscapeKey stop a lock wait without closing
  ---
  duration_ms: 3.093367
  ...
# Subtest: onEscapeKey cancels a stage without closing, then closes from browsing
ok 1376 - onEscapeKey cancels a stage without closing, then closes from browsing
  ---
  duration_ms: 2.777624
  ...
# Subtest: bank scope handler routes q/Ctrl+[ through backOut and leaves other keys alone
ok 1377 - bank scope handler routes q/Ctrl+[ through backOut and leaves other keys alone
  ---
  duration_ms: 1.191285
  ...
# Subtest: bank plain-browsing close hint reads esc/q
ok 1378 - bank plain-browsing close hint reads esc/q
  ---
  duration_ms: 1.636926
  ...
# Subtest: only the hub and canonical month paths are bank-relevant
ok 1379 - only the hub and canonical month paths are bank-relevant
  ---
  duration_ms: 10.87163
  ...
# Subtest: amount leads match the Rust grammar vectors
ok 1380 - amount leads match the Rust grammar vectors
  ---
  duration_ms: 0.970173
  ...
# Subtest: day headings parse canonical, month-day, and ISO spellings
ok 1381 - day headings parse canonical, month-day, and ISO spellings
  ---
  duration_ms: 0.613261
  ...
# Subtest: source scan keeps spans and ignores fences, stubs, children, and non-day sections
ok 1382 - source scan keeps spans and ignores fences, stubs, children, and non-day sections
  ---
  duration_ms: 1.910197
  ...
# Subtest: empty month notes have no rows and arbitrary dollar signs are not bank rows
ok 1383 - empty month notes have no rows and arbitrary dollar signs are not bank rows
  ---
  duration_ms: 0.31398
  ...
# Subtest: heading location requires a real day heading in the current source
ok 1384 - heading location requires a real day heading in the current source
  ---
  duration_ms: 0.626135
  ...
# Subtest: subscription picker filters titles and needles and ranks row matches first
ok 1385 - subscription picker filters titles and needles and ranks row matches first
  ---
  duration_ms: 2.102204
  ...
# Subtest: picker ranks the resolver's record before rule-renamed payee matches
ok 1386 - picker ranks the resolver's record before rule-renamed payee matches
  ---
  duration_ms: 0.286307
  ...
# Subtest: context strip compacts title, status, amount, and signed price drift
ok 1387 - context strip compacts title, status, amount, and signed price drift
  ---
  duration_ms: 0.349788
  ...
# Subtest: record selection inserts one link, fills a missing category, and closes in one edit
ok 1388 - record selection inserts one link, fills a missing category, and closes in one edit
  ---
  duration_ms: 3.569867
  ...
# Subtest: set mode can link without a category and replaces one prior subscription link
ok 1389 - set mode can link without a category and replaces one prior subscription link
  ---
  duration_ms: 0.910098
  ...
# Subtest: set-mode subscription pick fills a missing category in its atomic edit
ok 1390 - set-mode subscription pick fills a missing category in its atomic edit
  ---
  duration_ms: 0.635524
  ...
# Subtest: set-mode subscription pick keeps an existing category and adds the link
ok 1391 - set-mode subscription pick keeps an existing category and adds the link
  ---
  duration_ms: 0.430823
  ...
# Subtest: new subscription fields default from the candidate proposal and stay argv-safe
ok 1392 - new subscription fields default from the candidate proposal and stay argv-safe
  ---
  duration_ms: 0.68066
  ...
# Subtest: subscription JSON decoders accept reports and reject malformed record paths
ok 1393 - subscription JSON decoders accept reports and reject malformed record paths
  ---
  duration_ms: 0.820857
  ...
# Subtest: slash picker returns its selected record through the card writer options
ok 1394 - slash picker returns its selected record through the card writer options
  ---
  duration_ms: 2.146249
  ...
# Subtest: picker arrows move, Escape backs out, and the opening chord cannot double-commit
ok 1395 - picker arrows move, Escape backs out, and the opening chord cannot double-commit
  ---
  duration_ms: 11.107942
  ...
# Subtest: new subscription sheet creates a record then links that created path
ok 1396 - new subscription sheet creates a record then links that created path
  ---
  duration_ms: 1.128645
  ...
# Subtest: bank subscription fetch builds an argv command without changing other readers
ok 1397 - bank subscription fetch builds an argv command without changing other readers
  ---
  duration_ms: 0.591479
  ...
# Subtest: candidate ghost activation opens the row in set mode and starts the picker
ok 1398 - candidate ghost activation opens the row in set mode and starts the picker
  ---
  duration_ms: 10.204275
  ...
# Subtest: subscription argv includes -a for cancelled records on surfaces
ok 1399 - subscription argv includes -a for cancelled records on surfaces
  ---
  duration_ms: 2.636103
  ...
# Subtest: record header reads money, last/next, timeline, and finding sentence
ok 1400 - record header reads money, last/next, timeline, and finding sentence
  ---
  duration_ms: 1.62912
  ...
# Subtest: yearly record header shows its monthly equivalent
ok 1401 - yearly record header shows its monthly equivalent
  ---
  duration_ms: 0.60719
  ...
# Subtest: timeline paints amber on the price-changed bucket, else the latest charged
ok 1402 - timeline paints amber on the price-changed bucket, else the latest charged
  ---
  duration_ms: 0.362522
  ...
# Subtest: finding fallbacks stay generic and never invent amounts
ok 1403 - finding fallbacks stay generic and never invent amounts
  ---
  duration_ms: 0.214329
  ...
# Subtest: album card estimates commitments, counts statuses, and ranks live bars
ok 1404 - album card estimates commitments, counts statuses, and ranks live bars
  ---
  duration_ms: 0.760923
  ...
# Subtest: teaching empty points at bob albums create
ok 1405 - teaching empty points at bob albums create
  ---
  duration_ms: 0.175615
  ...
# Subtest: index pretty paints bank category labels, money cadence, and next chip
ok 1406 - index pretty paints bank category labels, money cadence, and next chip
  ---
  duration_ms: 1.034275
  ...
# Subtest: header and card paint fictional Tunely/Cloudbox chrome
ok 1407 - header and card paint fictional Tunely/Cloudbox chrome
  ---
  duration_ms: 2.179481
  ...
# Subtest: unknown bob-bank views stay quiet and subscriptions is a real view
ok 1408 - unknown bob-bank views stay quiet and subscriptions is a real view
  ---
  duration_ms: 0.90613
  ...
# Subtest: older bob rows decode without subscription fields and stay unchipped
ok 1409 - older bob rows decode without subscription fields and stay unchipped
  ---
  duration_ms: 5.251888
  ...
# Subtest: row decoder accepts subscription JSON and the subscription suggestion source
ok 1410 - row decoder accepts subscription JSON and the subscription suggestion source
  ---
  duration_ms: 2.721497
  ...
# Subtest: linked chip labels follow state, payee containment, and tooltip copy
ok 1411 - linked chip labels follow state, payee containment, and tooltip copy
  ---
  duration_ms: 2.152309
  ...
# Subtest: subscription tooltip uses the record latest date when available
ok 1412 - subscription tooltip uses the record latest date when available
  ---
  duration_ms: 0.454788
  ...
# Subtest: matched-unlinked rows are dashed ghosts; candidates stay tooltip-only
ok 1413 - matched-unlinked rows are dashed ghosts; candidates stay tooltip-only
  ---
  duration_ms: 4.956535
  ...
# Subtest: a 🔁 wikilink without JSON still paints a linked chip
ok 1414 - a 🔁 wikilink without JSON still paints a linked chip
  ---
  duration_ms: 0.488773
  ...
# Subtest: ghost write plan inserts the wikilink before the bank id as one edit
ok 1415 - ghost write plan inserts the wikilink before the bank id as one edit
  ---
  duration_ms: 3.111652
  ...
# Subtest: queue helper paints the same chip model as the month-note token
ok 1416 - queue helper paints the same chip model as the month-note token
  ---
  duration_ms: 0.45581
  ...
# Subtest: Reading wrap hides the native 🔁 link and restore removes appended ghosts
ok 1417 - Reading wrap hides the native 🔁 link and restore removes appended ghosts
  ---
  duration_ms: 2.617208
  ...
# Subtest: initial scan uses the bank folder and never walks every Markdown file
ok 1418 - initial scan uses the bank folder and never walks every Markdown file
  ---
  duration_ms: 24.232812
  ...
# Subtest: a missing bank folder becomes ready with no months and still skips the Markdown walk
ok 1419 - a missing bank folder becomes ready with no months and still skips the Markdown walk
  ---
  duration_ms: 0.890932
  ...
# Subtest: Markdown walk is the fallback only when the vault has no folder API
ok 1420 - Markdown walk is the fallback only when the vault has no folder API
  ---
  duration_ms: 0.653608
  ...
# Subtest: a two-month edit burst re-reads both months after one debounce
ok 1421 - a two-month edit burst re-reads both months after one debounce
  ---
  duration_ms: 1.797282
  ...
# Subtest: delete and rename-away drop the month; rename onto a month reads it
ok 1422 - delete and rename-away drop the month; rename onto a month reads it
  ---
  duration_ms: 9.537282
  ...
# Subtest: a closed-editor tick stays out of WAITING until a later disk read
ok 1423 - a closed-editor tick stays out of WAITING until a later disk read
  ---
  duration_ms: 7.99138
  ...
# Subtest: an older disk read never beats a newer overlay
ok 1424 - an older disk read never beats a newer overlay
  ---
  duration_ms: 1.078339
  ...
# Subtest: overlay snapshot signature uses per-path seq, not full overlay text
ok 1425 - overlay snapshot signature uses per-path seq, not full overlay text
  ---
  duration_ms: 1.705296
  ...
# Subtest: listeners registered before setupBankWalk survive it in onload order
ok 1426 - listeners registered before setupBankWalk survive it in onload order
  ---
  duration_ms: 1.095532
  ...
# Subtest: membership: only amount-led top-level checkboxes under a day count
ok 1427 - membership: only amount-led top-level checkboxes under a day count
  ---
  duration_ms: 6.492818
  ...
# Subtest: card waiting predicate cannot drift from walk predicate
ok 1428 - card waiting predicate cannot drift from walk predicate
  ---
  duration_ms: 3.074961
  ...
# Subtest: snapshot: waiting scope, order, keys, labels, counts
ok 1429 - snapshot: waiting scope, order, keys, labels, counts
  ---
  duration_ms: 9.432452
  ...
# Subtest: parity: index rows and waiting flags equal bob bank list -a
ok 1430 - parity: index rows and waiting flags equal bob bank list -a
  ---
  duration_ms: 2.72308
  ...
# Subtest: scope flips to all when nothing waits
ok 1431 - scope flips to all when nothing waits
  ---
  duration_ms: 1.488121
  ...
# Subtest: step wraps in both directions and both scopes
ok 1432 - step wraps in both directions and both scopes
  ---
  duration_ms: 3.179391
  ...
# Subtest: day jumps skip empty headings, merge duplicates, cross months, step from mid-day
ok 1433 - day jumps skip empty headings, merge duplicates, cross months, step from mid-day
  ---
  duration_ms: 1.632437
  ...
# Subtest: counts: N]b, N]B and counted wraps take one snapshot
ok 1434 - counts: N]b, N]B and counted wraps take one snapshot
  ---
  duration_ms: 2.008505
  ...
# Subtest: origins: cursor gap, daily, anchor, entry
ok 1435 - origins: cursor gap, daily, anchor, entry
  ---
  duration_ms: 3.06367
  ...
# Subtest: locate: member, gap, daily-outside, nulls
ok 1436 - locate: member, gap, daily-outside, nulls
  ---
  duration_ms: 1.772655
  ...
# Subtest: overlay tick leaves WAITING immediately and beats disk
ok 1437 - overlay tick leaves WAITING immediately and beats disk
  ---
  duration_ms: 2.40371
  ...
# Subtest: resolve: id, line text, same-day uniqueness, payee-start ch
ok 1438 - resolve: id, line text, same-day uniqueness, payee-start ch
  ---
  duration_ms: 3.255216
  ...
# Subtest: api guards: frozen, never throws, busy and anchor
ok 1439 - api guards: frozen, never throws, busy and anchor
  ---
  duration_ms: 2.112955
  ...
# Subtest: mixin snapshot: indexing until ready, overlay signature memo, change registry
ok 1440 - mixin snapshot: indexing until ready, overlay signature memo, change registry
  ---
  duration_ms: 0.906521
  ...
# Subtest: scan memo reuses the same path content and rescans only a changed month
ok 1441 - scan memo reuses the same path content and rescans only a changed month
  ---
  duration_ms: 2.093408
  ...
# Subtest: cursor above November's first heading stays in November
ok 1442 - cursor above November's first heading stays in November
  ---
  duration_ms: 1.126461
  ...
# Subtest: anchor-gap day jumps leave a day that still has rows
ok 1443 - anchor-gap day jumps leave a day that still has rows
  ---
  duration_ms: 1.053161
  ...
# Subtest: counted daily jumps move days and rows from the day's first landing
ok 1444 - counted daily jumps move days and rows from the day's first landing
  ---
  duration_ms: 1.298159
  ...
# Subtest: bankWalkStepFromTuple is the shared cursor-gap and anchor-gap stepper
ok 1445 - bankWalkStepFromTuple is the shared cursor-gap and anchor-gap stepper
  ---
  duration_ms: 1.133094
  ...
# Subtest: render appends one listener-free miniature with row-identical attributes
ok 1446 - render appends one listener-free miniature with row-identical attributes
  ---
  duration_ms: 3.092415
  ...
# Subtest: render decorative miniatures hide from assistive tech
ok 1447 - render decorative miniatures hide from assistive tech
  ---
  duration_ms: 0.309952
  ...
# Subtest: render accepts a synthetic digit model with no source task
ok 1448 - render accepts a synthetic digit model with no source task
  ---
  duration_ms: 0.207837
  ...
# Subtest: render uses the host ownerDocument, never a foreign one
ok 1449 - render uses the host ownerDocument, never a foreign one
  ---
  duration_ms: 0.243746
  ...
# Subtest: render returns null for bad input, a disabled gate, or no DOM
ok 1450 - render returns null for bad input, a disabled gate, or no DOM
  ---
  duration_ms: 0.33517
  ...
# Subtest: api.blockMarks v1 keeps model and adds a gated render
ok 1451 - api.blockMarks v1 keeps model and adds a gated render
  ---
  duration_ms: 0.301396
  ...
# Subtest: paint covers miniature, Live Preview, and reading rows under one gate
ok 1452 - paint covers miniature, Live Preview, and reading rows under one gate
  ---
  duration_ms: 3.423508
  ...
# Subtest: chip-box fallback rules are body-gated and never !important
ok 1453 - chip-box fallback rules are body-gated and never !important
  ---
  duration_ms: 2.869719
  ...
# Subtest: every paint rule except the token block and motion query carries the gate
ok 1454 - every paint rule except the token block and motion query carries the gate
  ---
  duration_ms: 2.796961
  ...
# Subtest: paint keeps pip geometry, reduced motion, and the 120ms budget
ok 1455 - paint keeps pip geometry, reduced motion, and the 120ms budget
  ---
  duration_ms: 3.290293
  ...
# Subtest: shipped mixes match the calibrated contract ramp
ok 1456 - shipped mixes match the calibrated contract ramp
  ---
  duration_ms: 2.922691
  ...
# Subtest: waiting glyphs meet 4.5:1 on their washed rows, both themes
ok 1457 - waiting glyphs meet 4.5:1 on their washed rows, both themes
  ---
  duration_ms: 2.725454
  ...
# Subtest: white on the darkened held fill meets 4.5:1, both themes
ok 1458 - white on the darkened held fill meets 4.5:1, both themes
  ---
  duration_ms: 2.3037
  ...
# Subtest: row tint and rail percentages ship in the gated rules
ok 1459 - row tint and rail percentages ship in the gated rules
  ---
  duration_ms: 1.997494
  ...
# Subtest: helpers never throw on bad input
ok 1460 - helpers never throw on bad input
  ---
  duration_ms: 0.388402
  ...
# Subtest: the plane mask is one hollow stroked path matched to the chevron
ok 1461 - the plane mask is one hollow stroked path matched to the chevron
  ---
  duration_ms: 4.281746
  ...
# Subtest: awaiting paints the P1 waiting box, the plane, the row tint, and the pip
ok 1462 - awaiting paints the P1 waiting box, the plane, the row tint, and the pip
  ---
  duration_ms: 2.553145
  ...
# Subtest: the plane renders as a miniature for chips and the Task Card
ok 1463 - the plane renders as a miniature for chips and the Task Card
  ---
  duration_ms: 0.295304
  ...
# Subtest: Live Preview emits own-row line attributes once across visible ranges
ok 1464 - Live Preview emits own-row line attributes once across visible ranges
  ---
  duration_ms: 7.738727
  ...
# Subtest: neutral rows, inline code, and fenced content stay unmarked
ok 1465 - neutral rows, inline code, and fenced content stay unmarked
  ---
  duration_ms: 0.581821
  ...
# Subtest: current unsaved document text changes or removes the visible mark
ok 1466 - current unsaved document text changes or removes the visible mark
  ---
  duration_ms: 1.151329
  ...
# Subtest: rebuilds on document, viewport, live-preview, path, and refresh effect, never selection alone
ok 1467 - rebuilds on document, viewport, live-preview, path, and refresh effect, never selection alone
  ---
  duration_ms: 0.444679
  ...
# Subtest: hot model calls use the in-memory ladder and project lookup is memoized per path
ok 1468 - hot model calls use the in-memory ladder and project lookup is memoized per path
  ---
  duration_ms: 1.489354
  ...
# Subtest: capture-phase tooltip attaches to the existing checkbox and restores owned attributes
ok 1469 - capture-phase tooltip attaches to the existing checkbox and restores owned attributes
  ---
  duration_ms: 2.282609
  ...
# Subtest: runBlockMarksRefresh rebuilds dependency chip editors
ok 1470 - runBlockMarksRefresh rebuilds dependency chip editors
  ---
  duration_ms: 0.313018
  ...
# Subtest: toggle is reversible, refreshes views, rerenders Tasks, and shows exact Notices
ok 1471 - toggle is reversible, refreshes views, rerenders Tasks, and shows exact Notices
  ---
  duration_ms: 0.341121
  ...
# Subtest: ladder invalidation compares semantic content and resume registers each editor document
ok 1472 - ladder invalidation compares semantic content and resume registers each editor document
  ---
  duration_ms: 1.157009
  ...
# Subtest: setup owns the gate and plugin-registered unload cleanup
ok 1473 - setup owns the gate and plugin-registered unload cleanup
  ---
  duration_ms: 1.261198
  ...
# Subtest: requestMeasure write-pass attaches tooltips after rebuild
ok 1474 - requestMeasure write-pass attaches tooltips after rebuild
  ---
  duration_ms: 3.013955
  ...
# Subtest: unscanned collect does not restore mouseover tooltip bindings
ok 1475 - unscanned collect does not restore mouseover tooltip bindings
  ---
  duration_ms: 1.568806
  ...
# Subtest: prj rows fold the project tag; dep-over-prj keeps it; selection reveals
ok 1476 - prj rows fold the project tag; dep-over-prj keeps it; selection reveals
  ---
  duration_ms: 14.764203
  ...
# Subtest: awaiting rows fold the \#awaiting_reply tag; losing rows keep it (AW1/AW3/AW4/AW6)
ok 1477 - awaiting rows fold the \#awaiting_reply tag; losing rows keep it (AW1/AW3/AW4/AW6)
  ---
  duration_ms: 7.77144
  ...
# Subtest: registers the reading processor before field-transforming marks
ok 1478 - registers the reading processor before field-transforming marks
  ---
  duration_ms: 1.790068
  ...
# Subtest: maps every family and pip from exact section source
ok 1479 - maps every family and pip from exact section source
  ---
  duration_ms: 11.876529
  ...
# Subtest: section-only text uses data-line offsets; full-note text adds lineStart
ok 1480 - section-only text uses data-line offsets; full-note text adds lineStart
  ---
  duration_ms: 0.872656
  ...
# Subtest: quoted tasks and nested children classify independently
ok 1481 - quoted tasks and nested children classify independently
  ---
  duration_ms: 0.754641
  ...
# Subtest: cold cache stays unmarked until Tasks is ready, then sweep paints
ok 1482 - cold cache stays unmarked until Tasks is ready, then sweep paints
  ---
  duration_ms: 0.919687
  ...
# Subtest: removed fields and recycled rows invalidate the retained mapping
ok 1483 - removed fields and recycled rows invalidate the retained mapping
  ---
  duration_ms: 0.646845
  ...
# Subtest: mismatched status or origin stays unmarked
ok 1484 - mismatched status or origin stays unmarked
  ---
  duration_ms: 0.346692
  ...
# Subtest: own-text fallback accepts raw fields and rejects transformed pills
ok 1485 - own-text fallback accepts raw fields and rejects transformed pills
  ---
  duration_ms: 1.104389
  ...
# Subtest: fallback never manufactures stale from lost field information
ok 1486 - fallback never manufactures stale from lost field information
  ---
  duration_ms: 0.604494
  ...
# Subtest: Dataview delayed rows use proven origin and never the query note stem
ok 1487 - Dataview delayed rows use proven origin and never the query note stem
  ---
  duration_ms: 1.531234
  ...
# Subtest: query result indexes are not read as source lines
ok 1488 - query result indexes are not read as source lines
  ---
  duration_ms: 0.442675
  ...
# Subtest: Tasks query rows stay excluded
ok 1489 - Tasks query rows stay excluded
  ---
  duration_ms: 0.250859
  ...
# Subtest: source-note lis Tasks also classifies still take JS marks
ok 1490 - source-note lis Tasks also classifies still take JS marks
  ---
  duration_ms: 3.483382
  ...
# Subtest: tooltip attributes restore when the mark leaves or the toggle turns off
ok 1491 - tooltip attributes restore when the mark leaves or the toggle turns off
  ---
  duration_ms: 0.955875
  ...
# Subtest: toggle off and on reclassifies tracked hosts in place
ok 1492 - toggle off and on reclassifies tracked hosts in place
  ---
  duration_ms: 1.263473
  ...
# Subtest: detached hosts dispose observers and drop owned attributes
ok 1493 - detached hosts dispose observers and drop owned attributes
  ---
  duration_ms: 0.574607
  ...
# Subtest: retained canonical text survives later field-transforming processors
ok 1494 - retained canonical text survives later field-transforming processors
  ---
  duration_ms: 0.455279
  ...
# Subtest: landing: recycled fallback row must drop the old scheduled reason
ok 1495 - landing: recycled fallback row must drop the old scheduled reason
  ---
  duration_ms: 0.493813
  ...
# Subtest: landing: off-state sweep must preserve a later external tooltip
ok 1496 - landing: off-state sweep must preserve a later external tooltip
  ---
  duration_ms: 0.462293
  ...
# Subtest: landing: a Tasks row used as processor root must stay excluded
ok 1497 - landing: a Tasks row used as processor root must stay excluded
  ---
  duration_ms: 0.2092
  ...
# Subtest: landing: Dataview without proven origin must remain neutral
ok 1498 - landing: Dataview without proven origin must remain neutral
  ---
  duration_ms: 0.250147
  ...
# Subtest: Dataview transformed rows recover canonical text from the Tasks cache
ok 1499 - Dataview transformed rows recover canonical text from the Tasks cache
  ---
  duration_ms: 1.653538
  ...
# Subtest: Dataview file links prove origin without data-task-path
ok 1500 - Dataview file links prove origin without data-task-path
  ---
  duration_ms: 0.437997
  ...
# Subtest: code and pre processor roots stay excluded like Tasks roots
ok 1501 - code and pre processor roots stay excluded like Tasks roots
  ---
  duration_ms: 0.239287
  ...
# Subtest: source-note fallback still paints when section mapping is absent
ok 1502 - source-note fallback still paints when section mapping is absent
  ---
  duration_ms: 0.346952
  ...
# Subtest: query origin-loss and same-status origin-change invalidate retained marks
ok 1503 - query origin-loss and same-status origin-change invalidate retained marks
  ---
  duration_ms: 0.640864
  ...
# Subtest: repeated off sweeps, unload, and toggle after an external aria edit
ok 1504 - repeated off sweeps, unload, and toggle after an external aria edit
  ---
  duration_ms: 0.796501
  ...
# Subtest: replacement checkbox nodes do not inherit the previous node's attributes
ok 1505 - replacement checkbox nodes do not inherit the previous node's attributes
  ---
  duration_ms: 0.477732
  ...
# Subtest: neutral status transition releases owned tooltip attributes
ok 1506 - neutral status transition releases owned tooltip attributes
  ---
  duration_ms: 0.387059
  ...
# Subtest: BM7 folds the project tag; BM19 keeps it
ok 1507 - BM7 folds the project tag; BM19 keeps it
  ---
  duration_ms: 0.807522
  ...
# Subtest: source-note lis Tasks also classifies still fold BM7 and keep BM19
ok 1508 - source-note lis Tasks also classifies still fold BM7 and keep BM19
  ---
  duration_ms: 0.58642
  ...
# Subtest: AW1 folds the \#awaiting_reply pill; AW3, AW6, and prj rows keep it
ok 1509 - AW1 folds the \#awaiting_reply pill; AW3, AW6, and prj rows keep it
  ---
  duration_ms: 2.155967
  ...
# Subtest: BM1–BM27 model vectors pass verbatim except Tasks-only BM24
ok 1510 - BM1–BM27 model vectors pass verbatim except Tasks-only BM24
  ---
  duration_ms: 20.098951
  ...
# Subtest: BM tooltip wording and losing-reason order match the contract
ok 1511 - BM tooltip wording and losing-reason order match the contract
  ---
  duration_ms: 1.74425
  ...
# Subtest: pure helpers preserve canonical eligibility, ids, digits, and decisions
ok 1512 - pure helpers preserve canonical eligibility, ids, digits, and decisions
  ---
  duration_ms: 4.340639
  ...
# Subtest: memo-local open-ID index keeps duplicate task IDs and project reasons one hop
ok 1513 - memo-local open-ID index keeps duplicate task IDs and project reasons one hop
  ---
  duration_ms: 1.436734
  ...
# Subtest: api.blockMarks v1 model is synchronous, frozen, toggle-aware, and neutral while cold
ok 1514 - api.blockMarks v1 model is synchronous, frozen, toggle-aware, and neutral while cold
  ---
  duration_ms: 0.672775
  ...
# Subtest: model keys are stable for equal results and change with a changed mark
ok 1515 - model keys are stable for equal results and change with a changed mark
  ---
  duration_ms: 0.498021
  ...
# Subtest: fold helpers: digit keys, BM1/BM8/BM9 bars, BM7/BM19 pills
ok 1516 - fold helpers: digit keys, BM1/BM8/BM9 bars, BM7/BM19 pills
  ---
  duration_ms: 10.975598
  ...
# Subtest: BM24 Tasks CSS cascade: digit from future scheduled + medium, no project tag
ok 1517 - BM24 Tasks CSS cascade: digit from future scheduled + medium, no project tag
  ---
  duration_ms: 7.843427
  ...
# Subtest: AW1–AW6 awaiting-reply model vectors pass verbatim
ok 1518 - AW1–AW6 awaiting-reply model vectors pass verbatim
  ---
  duration_ms: 10.508376
  ...
# Subtest: awaiting owns its date: no date reason, no digit, no Also scheduled pip
ok 1519 - awaiting owns its date: no date reason, no digit, no Also scheduled pip
  ---
  duration_ms: 1.800718
  ...
# Subtest: AP1–AP4 Also-replied tooltip pip vectors pass verbatim
ok 1520 - AP1–AP4 Also-replied tooltip pip vectors pass verbatim
  ---
  duration_ms: 0.7122
  ...
# Subtest: awaiting tooltip omits <who> when unknown and never throws on odd who
ok 1521 - awaiting tooltip omits <who> when unknown and never throws on odd who
  ---
  duration_ms: 0.799396
  ...
# Subtest: awaiting tag source is exact, quote-aware, and folds with its space
ok 1522 - awaiting tag source is exact, quote-aware, and folds with its space
  ---
  duration_ms: 3.956375
  ...
# Subtest: plugin <who> lookup reads the first linked mail note through the metadata cache
ok 1523 - plugin <who> lookup reads the first linked mail note through the metadata cache
  ---
  duration_ms: 1.785459
  ...
# Subtest: AW7 Tasks CSS cascade: the plane beats the digit, prj beats the plane
ok 1524 - AW7 Tasks CSS cascade: the plane beats the digit, prj beats the plane
  ---
  duration_ms: 6.905817
  ...
# Subtest: BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
ok 1525 - BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
  ---
  duration_ms: 13.923217
  ...
# Subtest: reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
ok 1526 - reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
  ---
  duration_ms: 14.253558
  ...
# Subtest: stale, missing, canonical append, and frozen-owner models (BC8-BC10)
ok 1527 - stale, missing, canonical append, and frozen-owner models (BC8-BC10)
  ---
  duration_ms: 1.164073
  ...
# Subtest: Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
ok 1528 - Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
  ---
  duration_ms: 17.135181
  ...
# Subtest: Reading BLOCKS chips map when the post-processor root is the nested list
ok 1529 - Reading BLOCKS chips map when the post-processor root is the nested list
  ---
  duration_ms: 2.442904
  ...
# Subtest: budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
ok 1530 - budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
  ---
  duration_ms: 2.525343
  ...
# Subtest: chip builder includes the 🔑 badge and has no edit controls
ok 1531 - chip builder includes the 🔑 badge and has no edit controls
  ---
  duration_ms: 1.577963
  ...
# Subtest: BLOCKS chip box covers prj, p2, stale miniatures and a throwing render
ok 1532 - BLOCKS chip box covers prj, p2, stale miniatures and a throwing render
  ---
  duration_ms: 1.149726
  ...
# Subtest: RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
ok 1533 - RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
  ---
  duration_ms: 3.321042
  ...
# Subtest: RBC2 hover × on a live chip calls removeDependent; notice is nav's
ok 1534 - RBC2 hover × on a live chip calls removeDependent; notice is nav's
  ---
  duration_ms: 1.213738
  ...
# Subtest: RBC3 frozen, stale, and no api.blocks stay navigation-only
ok 1535 - RBC3 frozen, stale, and no api.blocks stay navigation-only
  ---
  duration_ms: 1.237162
  ...
# Subtest: RBC4 Reading view matches Live Preview ＋ / ×
ok 1536 - RBC4 Reading view matches Live Preview ＋ / ×
  ---
  duration_ms: 4.08997
  ...
# Subtest: setup subscribes to the command-mode run-finished workspace event
ok 1537 - setup subscribes to the command-mode run-finished workspace event
  ---
  duration_ms: 7.735572
  ...
# Subtest: each invalidates tag refreshes its ledger cache and unknown tags are ignored
ok 1538 - each invalidates tag refreshes its ledger cache and unknown tags are ignored
  ---
  duration_ms: 1.62344
  ...
# Subtest: duplicate tags refresh once and a failing hook never blocks the others
ok 1539 - duplicate tags refresh once and a failing hook never blocks the others
  ---
  duration_ms: 0.312937
  ...
# Subtest: payloads without invalidates and setups without a workspace never throw
ok 1540 - payloads without invalidates and setups without a workspace never throw
  ---
  duration_ms: 0.415584
  ...
# Subtest: collections namespace version is additive v1
ok 1541 - collections namespace version is additive v1
  ---
  duration_ms: 1.28823
  ...
# Subtest: collection chip classes stay collection-specific through paint and refresh
ok 1542 - collection chip classes stay collection-specific through paint and refresh
  ---
  duration_ms: 3.258993
  ...
# Subtest: projects: scalar resolved links count, lists never widen
ok 1543 - projects: scalar resolved links count, lists never widen
  ---
  duration_ms: 0.393161
  ...
# Subtest: projects: templates, status, and containsAny edges
ok 1544 - projects: templates, status, and containsAny edges
  ---
  duration_ms: 0.379705
  ...
# Subtest: references: exact prefix, md only, exact scalar status
ok 1545 - references: exact prefix, md only, exact scalar status
  ---
  duration_ms: 0.320683
  ...
# Subtest: base contracts: accept current files, reject drift, tolerate presentation
ok 1546 - base contracts: accept current files, reject drift, tolerate presentation
  ---
  duration_ms: 0.755363
  ...
# Subtest: entries: true zero vs unavailable with reason, failure isolation
ok 1547 - entries: true zero vs unavailable with reason, failure isolation
  ---
  duration_ms: 0.285425
  ...
# Subtest: snapshot counts both collections once, true zero stays clickable
ok 1548 - snapshot counts both collections once, true zero stays clickable
  ---
  duration_ms: 0.553366
  ...
# Subtest: snapshot never presents partial counts as final
ok 1549 - snapshot never presents partial counts as final
  ---
  duration_ms: 0.486509
  ...
# Subtest: changed definitions fail closed per collection, never stale
ok 1550 - changed definitions fail closed per collection, never stale
  ---
  duration_ms: 0.69114
  ...
# Subtest: renderChip links, labels, and cleans up per component
ok 1551 - renderChip links, labels, and cleans up per component
  ---
  duration_ms: 0.950646
  ...
# Subtest: PENDING section excludes TODAY while the whole lane keeps it
ok 1552 - PENDING section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 9.239814
  ...
# Subtest: NEXT section excludes TODAY while the whole lane keeps it
ok 1553 - NEXT section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 0.864
  ...
# Subtest: NEXT uses symbol *, not name matching
ok 1554 - NEXT uses symbol *, not name matching
  ---
  duration_ms: 0.467613
  ...
# Subtest: READY badge and query agree on hide and path case variants
ok 1555 - READY badge and query agree on hide and path case variants
  ---
  duration_ms: 0.906311
  ...
# Subtest: blocked uses the full list even outside the visible subset
ok 1556 - blocked uses the full list even outside the visible subset
  ---
  duration_ms: 0.302127
  ...
# Subtest: duplicate block IDs, missing IDs, and reused objects stay per-row
ok 1557 - duplicate block IDs, missing IDs, and reused objects stay per-row
  ---
  duration_ms: 4.691179
  ...
# Subtest: READY gating keeps exempt rows and drops NEW/ROTTEN
ok 1558 - READY gating keeps exempt rows and drops NEW/ROTTEN
  ---
  duration_ms: 0.600647
  ...
# Subtest: throwing Today degrades to unavailable, never zero
ok 1559 - throwing Today degrades to unavailable, never zero
  ---
  duration_ms: 420.395813
  ...
# Subtest: dashboard badges color the displayed section count and label whole-lane pressure
ok 1560 - dashboard badges color the displayed section count and label whole-lane pressure
  ---
  duration_ms: 19.18754
  ...
# Subtest: dashboard section warning boundaries ignore TODAY-only whole-lane excess
ok 1561 - dashboard section warning boundaries ignore TODAY-only whole-lane excess
  ---
  duration_ms: 1.291957
  ...
# Subtest: dashboard lane badge keeps unavailable data neutral
ok 1562 - dashboard lane badge keeps unavailable data neutral
  ---
  duration_ms: 0.393672
  ...
# Subtest: dashboard lane paint and refresh keep color aligned with the visible section
ok 1563 - dashboard lane paint and refresh keep color aligned with the visible section
  ---
  duration_ms: 117.750543
  ...
# Subtest: dashboard lane widgets refresh together and prune on unload
ok 1564 - dashboard lane widgets refresh together and prune on unload
  ---
  duration_ms: 144.437512
  ...
# Subtest: daily paint matches dashboard section badges on screenshot fixtures
ok 1565 - daily paint matches dashboard section badges on screenshot fixtures
  ---
  duration_ms: 505.380698
  ...
# Subtest: daily paint lane lint matches a red badge section count
ok 1566 - daily paint lane lint matches a red badge section count
  ---
  duration_ms: 611.9348
  ...
# Subtest: daily and dashboard membership agree for exclusions and custom IN_PROGRESS
ok 1567 - daily and dashboard membership agree for exclusions and custom IN_PROGRESS
  ---
  duration_ms: 388.015731
  ...
# Subtest: daily paint refreshes with dashboard when Today, lane, and cap change
ok 1568 - daily paint refreshes with dashboard when Today, lane, and cap change
  ---
  duration_ms: 786.877384
  ...
# Subtest: older daily notes follow today's dashboard lanes
ok 1569 - older daily notes follow today's dashboard lanes
  ---
  duration_ms: 529.621116
  ...
# Subtest: daily lane anchors keep shared navigation and reject stale paints
ok 1570 - daily lane anchors keep shared navigation and reject stale paints
  ---
  duration_ms: 569.673659
  ...
# Subtest: daily paint stays unavailable until Tasks and Today are ready
ok 1571 - daily paint stays unavailable until Tasks and Today are ready
  ---
  duration_ms: 170.019984
  ...
# Subtest: work tones: dashboard lane models carry section tones
ok 1572 - work tones: dashboard lane models carry section tones
  ---
  duration_ms: 0.273953
  ...
# Subtest: T1 scheduled full-mode row gets a Fri mark inside the span
ok 1573 - T1 scheduled full-mode row gets a Fri mark inside the span
  ---
  duration_ms: 4.740001
  ...
# Subtest: T2 done row maps to a completion Oct 5 mark
ok 1574 - T2 done row maps to a completion Oct 5 mark
  ---
  duration_ms: 1.601188
  ...
# Subtest: T3 short-mode created span is left untouched by JS
ok 1575 - T3 short-mode created span is left untouched by JS
  ---
  duration_ms: 0.611979
  ...
# Subtest: T4 pending row decorates once data-task appears; exhausted rows stay native
ok 1576 - T4 pending row decorates once data-task appears; exhausted rows stay native
  ---
  duration_ms: 11.853225
  ...
# Subtest: T5 a second pass adds nothing
ok 1577 - T5 a second pass adds nothing
  ---
  duration_ms: 0.71189
  ...
# Subtest: T6 task-due and task-start spans are untouched
ok 1578 - T6 task-due and task-start spans are untouched
  ---
  duration_ms: 0.359907
  ...
# Subtest: T7 an invalid date is untouched
ok 1579 - T7 an invalid date is untouched
  ---
  duration_ms: 0.358435
  ...
# Subtest: T8 nothing is scheduled with marks off or for connected non-Tasks elements
ok 1580 - T8 nothing is scheduled with marks off or for connected non-Tasks elements
  ---
  duration_ms: 0.415353
  ...
# Subtest: T9 a Tasks-host Fri mark relabels to tomorrow on rollover
ok 1581 - T9 a Tasks-host Fri mark relabels to tomorrow on rollover
  ---
  duration_ms: 0.85917
  ...
# Subtest: renderDateMarksIn schedules one shared frame for every row
ok 1582 - renderDateMarksIn schedules one shared frame for every row
  ---
  duration_ms: 1.26698
  ...
# Subtest: the Tasks pass never throws on hostile input
ok 1583 - the Tasks pass never throws on hostile input
  ---
  duration_ms: 0.703804
  ...
# Subtest: T10 real-DOM NodeList children decorate via direct and queued passes
ok 1584 - T10 real-DOM NodeList children decorate via direct and queued passes
  ---
  duration_ms: 8.418065
  ...
# Subtest: T11 toggling off before a queued frame runs writes nothing
ok 1585 - T11 toggling off before a queued frame runs writes nothing
  ---
  duration_ms: 0.970163
  ...
# Subtest: T12 a pending-row retry followed by disabling writes nothing
ok 1586 - T12 a pending-row retry followed by disabling writes nothing
  ---
  duration_ms: 0.477792
  ...
# Subtest: T13 unloading before a callback runs writes nothing
ok 1587 - T13 unloading before a callback runs writes nothing
  ---
  duration_ms: 6.350367
  ...
# Subtest: RT1 full-mode recurring result gets a daily mark and stays idempotent
ok 1588 - RT1 full-mode recurring result gets a daily mark and stays idempotent
  ---
  duration_ms: 1.795168
  ...
# Subtest: RT2 recurring labels use the shared cadence grammar
ok 1589 - RT2 recurring labels use the shared cadence grammar
  ---
  duration_ms: 1.64398
  ...
# Subtest: RT2a unknown inherited-name rules stay readable in Tasks results
ok 1590 - RT2a unknown inherited-name rules stay readable in Tasks results
  ---
  duration_ms: 0.513941
  ...
# Subtest: RT3 short-mode recurring spans stay native to JS and use the CSS loop
ok 1591 - RT3 short-mode recurring spans stay native to JS and use the CSS loop
  ---
  duration_ms: 2.682933
  ...
# Subtest: RT4 open checklist members keep recurrence pills without `when done`
ok 1592 - RT4 open checklist members keep recurrence pills without `when done`
  ---
  duration_ms: 0.85874
  ...
# Subtest: RT5 invalid recurrence stays native and incomplete rows are retried
ok 1593 - RT5 invalid recurrence stays native and incomplete rows are retried
  ---
  duration_ms: 0.633771
  ...
# Subtest: styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
ok 1594 - styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
  ---
  duration_ms: 2.426033
  ...
# Subtest: DATE_MARK_FIELDS lists the four dates with verbs
ok 1595 - DATE_MARK_FIELDS lists the four dates with verbs
  ---
  duration_ms: 3.054432
  ...
# Subtest: DM1 created today: label, tooltip, fold, quiet field
ok 1596 - DM1 created today: label, tooltip, fold, quiet field
  ---
  duration_ms: 1.938522
  ...
# Subtest: DM2 created yesterday without space after the colons
ok 1597 - DM2 created yesterday without space after the colons
  ---
  duration_ms: 0.520133
  ...
# Subtest: DM3-DM6 scheduled tomorrow, weekday, and month/day labels
ok 1598 - DM3-DM6 scheduled tomorrow, weekday, and month/day labels
  ---
  duration_ms: 0.295234
  ...
# Subtest: DM7 scheduled today reads with emphasis timing
ok 1599 - DM7 scheduled today reads with emphasis timing
  ---
  duration_ms: 0.353656
  ...
# Subtest: DM8 past scheduled uses month/day, never a weekday
ok 1600 - DM8 past scheduled uses month/day, never a weekday
  ---
  duration_ms: 0.319831
  ...
# Subtest: DM9 completion on a closed task keeps the timeline grammar
ok 1601 - DM9 completion on a closed task keeps the timeline grammar
  ---
  duration_ms: 0.239928
  ...
# Subtest: DM10 cancelled across years appends the year
ok 1602 - DM10 cancelled across years appends the year
  ---
  duration_ms: 0.165546
  ...
# Subtest: DM11 next-year date appends the year
ok 1603 - DM11 next-year date appends the year
  ---
  duration_ms: 0.397649
  ...
# Subtest: DM12 the weekday rule wins across the year boundary
ok 1604 - DM12 the weekday rule wins across the year boundary
  ---
  duration_ms: 0.498091
  ...
# Subtest: DM13 two marks in order with folds 1 and 2
ok 1605 - DM13 two marks in order with folds 1 and 2
  ---
  duration_ms: 0.679948
  ...
# Subtest: DM14 created and scheduled ranges stay disjoint from the fresh mark
ok 1606 - DM14 created and scheduled ranges stay disjoint from the fresh mark
  ---
  duration_ms: 0.390716
  ...
# Subtest: DM15-DM16 paren and padded brackets are canonical
ok 1607 - DM15-DM16 paren and padded brackets are canonical
  ---
  duration_ms: 0.215221
  ...
# Subtest: DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
ok 1608 - DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
  ---
  duration_ms: 0.731107
  ...
# Subtest: DM22 code still parses pure but decorates nothing (see Live Preview)
ok 1609 - DM22 code still parses pure but decorates nothing (see Live Preview)
  ---
  duration_ms: 0.149766
  ...
# Subtest: DM23 rescheduled is untouched and never a duplicate
ok 1610 - DM23 rescheduled is untouched and never a duplicate
  ---
  duration_ms: 0.236452
  ...
# Subtest: DN1-DN9 non-canonical fields get no mark
ok 1611 - DN1-DN9 non-canonical fields get no mark
  ---
  duration_ms: 0.357873
  ...
# Subtest: dateMarkContentStart finds content on list, quoted, and plain lines
ok 1612 - dateMarkContentStart finds content on list, quoted, and plain lines
  ---
  duration_ms: 0.149526
  ...
# Subtest: dateMarkRelativePhrase covers the exact-day phrases
ok 1613 - dateMarkRelativePhrase covers the exact-day phrases
  ---
  duration_ms: 0.125099
  ...
# Subtest: dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
ok 1614 - dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
  ---
  duration_ms: 0.480718
  ...
# Subtest: no model output contains a double colon
ok 1615 - no model output contains a double colon
  ---
  duration_ms: 1.960103
  ...
# Subtest: a new day always changes the widget key
ok 1616 - a new day always changes the widget key
  ---
  duration_ms: 0.223356
  ...
# Subtest: element structure and the decorative/inheritColor/rendered options
ok 1617 - element structure and the decorative/inheritColor/rendered options
  ---
  duration_ms: 0.621677
  ...
# Subtest: Live Preview emits several decorations in ascending order
ok 1618 - Live Preview emits several decorations in ascending order
  ---
  duration_ms: 1.774208
  ...
# Subtest: Live Preview reveals per field, never the whole line
ok 1619 - Live Preview reveals per field, never the whole line
  ---
  duration_ms: 0.347243
  ...
# Subtest: Live Preview refuses source mode, code, and disabled marks
ok 1620 - Live Preview refuses source mode, code, and disabled marks
  ---
  duration_ms: 4.870601
  ...
# Subtest: widget mousedown anchors at the field start for folds 0, 1, and 2
ok 1621 - widget mousedown anchors at the field start for folds 0, 1, and 2
  ---
  duration_ms: 1.669749
  ...
# Subtest: DM24 a cursor in the folded run unfolds the mark (vim cw)
ok 1622 - DM24 a cursor in the folded run unfolds the mark (vim cw)
  ---
  duration_ms: 0.339449
  ...
# Subtest: DM25 a cursor in Tasks double space unfolds only that field
ok 1623 - DM25 a cursor in Tasks double space unfolds only that field
  ---
  duration_ms: 0.243886
  ...
# Subtest: a selection ending inside the run unfolds; ending at its start keeps the fold
ok 1624 - a selection ending inside the run unfolds; ending at its start keeps the fold
  ---
  duration_ms: 0.268773
  ...
# Subtest: no emitted decoration ever hides a cursor, and reveal still means field overlap
ok 1625 - no emitted decoration ever hides a cursor, and reveal still means field overlap
  ---
  duration_ms: 21.38682
  ...
# Subtest: dateMarkSelectionFold: reveal, unfold, fold, and garbage input
ok 1626 - dateMarkSelectionFold: reveal, unfold, fold, and garbage input
  ---
  duration_ms: 0.340019
  ...
# Subtest: mousedown on an unfolded (fold-0) widget anchors at the field start
ok 1627 - mousedown on an unfolded (fold-0) widget anchors at the field start
  ---
  duration_ms: 0.505465
  ...
# Subtest: rendered views split several fields in one node
ok 1628 - rendered views split several fields in one node
  ---
  duration_ms: 2.245037
  ...
# Subtest: rendered views skip exclusions and duplicates
ok 1629 - rendered views skip exclusions and duplicates
  ---
  duration_ms: 0.907353
  ...
# Subtest: RO1 rendered marks relabel in place across midnight
ok 1630 - RO1 rendered marks relabel in place across midnight
  ---
  duration_ms: 0.67019
  ...
# Subtest: rollover dispatches once per day change and never touches widgets
ok 1631 - rollover dispatches once per day change and never touches widgets
  ---
  duration_ms: 1.518139
  ...
# Subtest: api.dateMarks v1 is additive, sync, and never throwing
ok 1632 - api.dateMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.670861
  ...
# Subtest: session toggle and onload wiring
ok 1633 - session toggle and onload wiring
  ---
  duration_ms: 100.088825
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 1634 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 0.867366
  ...
# Subtest: styles.css contract: masks, tones, repair flag, resting
ok 1635 - styles.css contract: masks, tones, repair flag, resting
  ---
  duration_ms: 3.136559
  ...
# Subtest: day identity follows the canonical path, never the tab or mtime
ok 1636 - day identity follows the canonical path, never the tab or mtime
  ---
  duration_ms: 2.242903
  ...
# Subtest: fence day parsing accepts YAML mappings and plain lines, nothing else
ok 1637 - fence day parsing accepts YAML mappings and plain lines, nothing else
  ---
  duration_ms: 0.857437
  ...
# Subtest: report selection reads the default entry, an 8-day range, or nothing
ok 1638 - report selection reads the default entry, an 8-day range, or nothing
  ---
  duration_ms: 137.713171
  ...
# Subtest: report window checks keep the page window only when it shows D
ok 1639 - report window checks keep the page window only when it shows D
  ---
  duration_ms: 179.735367
  ...
# Subtest: week-grouped default never covers D, and a cold-cache today re-selects once
ok 1640 - week-grouped default never covers D, and a cold-cache today re-selects once
  ---
  duration_ms: 656.263207
  ...
# Subtest: a report that differs only in typical repaints
ok 1641 - a report that differs only in typical repaints
  ---
  duration_ms: 311.658703
  ...
# Subtest: paint from cache costs one frame and zero spawns
ok 1642 - paint from cache costs one frame and zero spawns
  ---
  duration_ms: 604.291413
  ...
# Subtest: off-screen and hidden-tab strips spawn nothing
ok 1643 - off-screen and hidden-tab strips spawn nothing
  ---
  duration_ms: 809.429459
  ...
# Subtest: clean fresh entries never refetch, whatever changes
ok 1644 - clean fresh entries never refetch, whatever changes
  ---
  duration_ms: 222.1764
  ...
# Subtest: visible changing strips spawn at most once per 30 s
ok 1645 - visible changing strips spawn at most once per 30 s
  ---
  duration_ms: 398.111511
  ...
# Subtest: the 10-minute age rule refetches today without any change
ok 1646 - the 10-minute age rule refetches today without any change
  ---
  duration_ms: 290.655594
  ...
# Subtest: past days wait out the 10-minute gate
ok 1647 - past days wait out the 10-minute gate
  ---
  duration_ms: 395.482751
  ...
# Subtest: several strips and the page share one spawn per key
ok 1648 - several strips and the page share one spawn per key
  ---
  duration_ms: 318.569129
  ...
# Subtest: strips repaint for free when the page refreshes the shared key
ok 1649 - strips repaint for free when the page refreshes the shared key
  ---
  duration_ms: 673.510682
  ...
# Subtest: rollover re-keys today to a past day and refetches
ok 1650 - rollover re-keys today to a past day and refetches
  ---
  duration_ms: 276.49219
  ...
# Subtest: a stale-across-midnight report is never shown as so far
ok 1651 - a stale-across-midnight report is never shown as so far
  ---
  duration_ms: 478.265992
  ...
# Subtest: window-edge days fetch the 8-day range
ok 1652 - window-edge days fetch the 8-day range
  ---
  duration_ms: 462.600155
  ...
# Subtest: future days render nothing and spawn nothing
ok 1653 - future days render nothing and spawn nothing
  ---
  duration_ms: 351.85959
  ...
# Subtest: a failed refresh keeps the frame and shows the stale dot
ok 1654 - a failed refresh keeps the frame and shows the stale dot
  ---
  duration_ms: 1281.364029
  ...
# Subtest: a failure with nothing cached shows the one-line error and Retry
ok 1655 - a failure with nothing cached shows the one-line error and Retry
  ---
  duration_ms: 422.197623
  ...
# Subtest: bob-not-found with nothing cached names stats.bob_path
ok 1656 - bob-not-found with nothing cached names stats.bob_path
  ---
  duration_ms: 410.610288
  ...
# Subtest: the fence parses day:, falls back to the note date, or explains itself
ok 1657 - the fence parses day:, falls back to the note date, or explains itself
  ---
  duration_ms: 475.489197
  ...
# Subtest: the fence skips hover popovers and embeds, and unregisters on unload
ok 1658 - the fence skips hover popovers and embeds, and unregisters on unload
  ---
  duration_ms: 540.284279
  ...
# Subtest: openStatsForDay pins the day, focuses the metric, and opens a new tab
ok 1659 - openStatsForDay pins the day, focuses the metric, and opens a new tab
  ---
  duration_ms: 484.454279
  ...
# Subtest: openStatsForDay opens a new tab when Stats is already open
ok 1660 - openStatsForDay opens a new tab when Stats is already open
  ---
  duration_ms: 391.072928
  ...
# Subtest: openStatsForDay keeps the page window when it already shows D
ok 1661 - openStatsForDay keeps the page window when it already shows D
  ---
  duration_ms: 1422.574781
  ...
# Subtest: openStatsForDay panel themes selects the Themes view
ok 1662 - openStatsForDay panel themes selects the Themes view
  ---
  duration_ms: 464.383361
  ...
# Subtest: openStatsForDay Notices when Stats cannot open
ok 1663 - openStatsForDay Notices when Stats cannot open
  ---
  duration_ms: 417.962947
  ...
# Subtest: the page honours a pinned day on its first paint
ok 1664 - the page honours a pinned day on its first paint
  ---
  duration_ms: 496.570856
  ...
# Subtest: renderStatsResult consumes the one-shot revealPanel
ok 1665 - renderStatsResult consumes the one-shot revealPanel
  ---
  duration_ms: 215.396063
  ...
# Subtest: every strip paints facts and links with no buttons and no vault writes
ok 1666 - every strip paints facts and links with no buttons and no vault writes
  ---
  duration_ms: 415.428679
  ...
# Subtest: change bursts coalesce behind one trailing quiet window
ok 1667 - change bursts coalesce behind one trailing quiet window
  ---
  duration_ms: 479.299443
  ...
# Subtest: mobile and spawn-less hosts render nothing and spawn nothing
ok 1668 - mobile and spawn-less hosts render nothing and spawn nothing
  ---
  duration_ms: 269.900583
  ...
# Subtest: rollover synchronously skeletons visible and offscreen fences; visible refetch resolves as past
ok 1669 - rollover synchronously skeletons visible and offscreen fences; visible refetch resolves as past
  ---
  duration_ms: 918.550985
  ...
# Subtest: fit observer registers once, refits on width change, and releases
ok 1670 - fit observer registers once, refits on width change, and releases
  ---
  duration_ms: 43.364658
  ...
# Subtest: missing ResizeObserver is harmless
ok 1671 - missing ResizeObserver is harmless
  ---
  duration_ms: 0.449308
  ...
# Subtest: openStatsForDay explicit clock selects the lens, pins the day, and persists the preference
ok 1672 - openStatsForDay explicit clock selects the lens, pins the day, and persists the preference
  ---
  duration_ms: 153.453629
  ...
# Subtest: openStatsForDay explicit worked survives a remembered off-clock preference
ok 1673 - openStatsForDay explicit worked survives a remembered off-clock preference
  ---
  duration_ms: 150.653052
  ...
# Subtest: muted roots stay gray, unshaded, claim no hue, and sort before the buckets
ok 1674 - muted roots stay gray, unshaded, claim no hue, and sort before the buckets
  ---
  duration_ms: 23.771273
  ...
# Subtest: root hues follow identity order when minutes change
ok 1675 - root hues follow identity order when minutes change
  ---
  duration_ms: 0.467072
  ...
# Subtest: lane view sanitizes and cycles both -> roots -> themes -> both
ok 1676 - lane view sanitizes and cycles both -> roots -> themes -> both
  ---
  duration_ms: 0.175855
  ...
# Subtest: layout matrix: availability, skeleton, and hidden states
ok 1677 - layout matrix: availability, skeleton, and hidden states
  ---
  duration_ms: 0.728551
  ...
# Subtest: layout copy uses areas under the area fallback with exact strings
ok 1678 - layout copy uses areas under the area fallback with exact strings
  ---
  duration_ms: 0.241822
  ...
# Subtest: painter per view: order, first-row meta and switch, themes-first
ok 1679 - painter per view: order, first-row meta and switch, themes-first
  ---
  duration_ms: 6.678964
  ...
# Subtest: switch attributes, marks, and skeleton placeholder
ok 1680 - switch attributes, marks, and skeleton placeholder
  ---
  duration_ms: 4.700777
  ...
# Subtest: switch activation: click, Enter, Space call cycleLanes once with focus
ok 1681 - switch activation: click, Enter, Space call cycleLanes once with focus
  ---
  duration_ms: 2.20463
  ...
# Subtest: group aria-label names only the shown lanes
ok 1682 - group aria-label names only the shown lanes
  ---
  duration_ms: 1.105271
  ...
# Subtest: lane-enter class appears only on a same-day view change
ok 1683 - lane-enter class appears only on a same-day view change
  ---
  duration_ms: 9.863936
  ...
# Subtest: registry: a switch repaints every record without a spawn, dedupes, and restores focus
ok 1684 - registry: a switch repaints every record without a spawn, dedupes, and restores focus
  ---
  duration_ms: 240.063126
  ...
# Subtest: command Cycle Day stats bars is registered with its Notice copy
ok 1685 - command Cycle Day stats bars is registered with its Notice copy
  ---
  duration_ms: 144.938809
  ...
# Subtest: persistence remember = device: setup loads, saves, and tolerates missing storage
ok 1686 - persistence remember = device: setup loads, saves, and tolerates missing storage
  ---
  duration_ms: 899.714234
  ...
# Subtest: require time adds no eager StateEffect.define()
ok 1687 - require time adds no eager StateEffect.define()
  ---
  duration_ms: 1.321313
  ...
# Subtest: renderPlanBlock puts exactly one host first with .bob-plan after it on canonical days
ok 1688 - renderPlanBlock puts exactly one host first with .bob-plan after it on canonical days
  ---
  duration_ms: 234.949311
  ...
# Subtest: non-daily, future, dashboard, mobile, spawn-less, and excluded blocks get no host
ok 1689 - non-daily, future, dashboard, mobile, spawn-less, and excluded blocks get no host
  ---
  duration_ms: 314.268005
  ...
# Subtest: paintPlanBlock keeps the same host node first with .bob-plan after it and no strip repaint or spawn
ok 1690 - paintPlanBlock keeps the same host node first with .bob-plan after it and no strip repaint or spawn
  ---
  duration_ms: 467.850261
  ...
# Subtest: toggle and stats.day_strip remove the host and class, re-enabling restores them
ok 1691 - toggle and stats.day_strip remove the host and class, re-enabling restores them
  ---
  duration_ms: 849.483053
  ...
# Subtest: unload releases the record and its observer
ok 1692 - unload releases the record and its observer
  ---
  duration_ms: 499.810751
  ...
# Subtest: rollover attaches future blocks and repaints today as a past day
ok 1693 - rollover attaches future blocks and repaints today as a past day
  ---
  duration_ms: 425.230767
  ...
# Subtest: rollover skeletons a visible automatic today host synchronously; it resolves as past
ok 1694 - rollover skeletons a visible automatic today host synchronously; it resolves as past
  ---
  duration_ms: 716.449197
  ...
# Subtest: plan hosts never write the vault or journals
ok 1695 - plan hosts never write the vault or journals
  ---
  duration_ms: 730.864813
  ...
# Subtest: cold plan host waits for visibility: no spawn before callback, false stays zero, true fetches once
ok 1696 - cold plan host waits for visibility: no spawn before callback, false stays zero, true fetches once
  ---
  duration_ms: 867.549994
  ...
# Subtest: plan host paints synchronously from cache with zero spawn before visibility
ok 1697 - plan host paints synchronously from cache with zero spawn before visibility
  ---
  duration_ms: 694.658106
  ...
# Subtest: detached excluded blocks get no host; detached ordinary blocks attach synchronously
ok 1698 - detached excluded blocks get no host; detached ordinary blocks attach synchronously
  ---
  duration_ms: 858.432233
  ...
# Subtest: no-observer fallback attaches detached, fetches on check after connect, releases excluded
ok 1699 - no-observer fallback attaches detached, fetches on check after connect, releases excluded
  ---
  duration_ms: 697.848018
  ...
# Subtest: excluded after attach releases on the first observer callback
ok 1700 - excluded after attach releases on the first observer callback
  ---
  duration_ms: 4628.977147
  ...
# Subtest: excluded processor container gets no host
ok 1701 - excluded processor container gets no host
  ---
  duration_ms: 756.309935
  ...
# Subtest: reading-view order attaches detached, virtualized stays quiet until attach
ok 1702 - reading-view order attaches detached, virtualized stays quiet until attach
  ---
  duration_ms: 1063.150576
  ...
# Subtest: today host shows so far HH:MM from the fetch stamp
ok 1703 - today host shows so far HH:MM from the fetch stamp
  ---
  duration_ms: 580.437754
  ...
# Subtest: failed refresh over a cached report names the HH:MM it shows
ok 1704 - failed refresh over a cached report names the HH:MM it shows
  ---
  duration_ms: 608.507887
  ...
# Subtest: placeholder finds .bob-plan by class and toggle-off restores it first
ok 1705 - placeholder finds .bob-plan by class and toggle-off restores it first
  ---
  duration_ms: 1139.391184
  ...
# Subtest: statsThemeRef prefers theme_hues names and hues, with gray fallbacks
ok 1706 - statsThemeRef prefers theme_hues names and hues, with gray fallbacks
  ---
  duration_ms: 1.592892
  ...
# Subtest: theme mix orders coloured by minutes then gray, with unnamed last
ok 1707 - theme mix orders coloured by minutes then gray, with unnamed last
  ---
  duration_ms: 14.388776
  ...
# Subtest: same-hue coloured themes take shade 0 then 1 then 2; gray is never shaded
ok 1708 - same-hue coloured themes take shade 0 then 1 then 2; gray is never shaded
  ---
  duration_ms: 1.117344
  ...
# Subtest: same-hue type shades follow label identity while segment position follows minutes
ok 1709 - same-hue type shades follow label identity while segment position follows minutes
  ---
  duration_ms: 0.367872
  ...
# Subtest: theme mix labels, ranks, overflow, titles, and aria follow the report
ok 1710 - theme mix labels, ranks, overflow, titles, and aria follow the report
  ---
  duration_ms: 3.778686
  ...
# Subtest: theme lane is omitted for zero days, missing parts, and redefined worked
ok 1711 - theme lane is omitted for zero days, missing parts, and redefined worked
  ---
  duration_ms: 5.944391
  ...
# Subtest: fallback hue uses context.themeHueFor and stays gray without it
ok 1712 - fallback hue uses context.themeHueFor and stays gray without it
  ---
  duration_ms: 0.483493
  ...
# Subtest: painter uses swatches, shades, data-lane, and no buttons on the theme lane
ok 1713 - painter uses swatches, shades, data-lane, and no buttons on the theme lane
  ---
  duration_ms: 4.82315
  ...
# Subtest: theme legend and bar open Stats on the Themes view
ok 1714 - theme legend and bar open Stats on the Themes view
  ---
  duration_ms: 3.491988
  ...
# Subtest: fitter fits both legends independently and returns the roots result
ok 1715 - fitter fits both legends independently and returns the roots result
  ---
  duration_ms: 4.124716
  ...
# Subtest: date words and day shifts use calendar integers, including leap day
ok 1716 - date words and day shifts use calendar integers, including leap day
  ---
  duration_ms: 1.859541
  ...
# Subtest: fact displays are selected from the exact day point, even with null headline and grouped input
ok 1717 - fact displays are selected from the exact day point, even with null headline and grouped input
  ---
  duration_ms: 20.382993
  ...
# Subtest: honest states carry meta text for today, past, stale today, and stale past
ok 1718 - honest states carry meta text for today, past, stale today, and stale past
  ---
  duration_ms: 3.441612
  ...
# Subtest: time mix reuses Stats area ordering and hues, with buckets last and a tooltip title
ok 1719 - time mix reuses Stats area ordering and hues, with buckets last and a tooltip title
  ---
  duration_ms: 7.134454
  ...
# Subtest: root_parent is preferred with an honest area fallback
ok 1720 - root_parent is preferred with an honest area fallback
  ---
  duration_ms: 0.944564
  ...
# Subtest: zero worked renders no Pomodoros and redefined worked omits its mix
ok 1721 - zero worked renders no Pomodoros and redefined worked omits its mix
  ---
  duration_ms: 2.064061
  ...
# Subtest: aria label carries the date, values, provisional state, and area names
ok 1722 - aria label carries the date, values, provisional state, and area names
  ---
  duration_ms: 0.463505
  ...
# Subtest: skeleton carries placeholder text per fact and the same tag and class sequence
ok 1723 - skeleton carries placeholder text per fact and the same tag and class sequence
  ---
  duration_ms: 4.439417
  ...
# Subtest: painter repaints in place, emits no buttons, and shows unavailable controls
ok 1724 - painter repaints in place, emits no buttons, and shows unavailable controls
  ---
  duration_ms: 9.172997
  ...
# Subtest: facts, mix, and Retry preserve day, focus, and new-leaf modifiers
ok 1725 - facts, mix, and Retry preserve day, focus, and new-leaf modifiers
  ---
  duration_ms: 3.247251
  ...
# Subtest: future and hidden models paint no children
ok 1726 - future and hidden models paint no children
  ---
  duration_ms: 0.360619
  ...
# Subtest: strip paints facts, legend row, then full-width bar with no buttons
ok 1727 - strip paints facts, legend row, then full-width bar with no buttons
  ---
  duration_ms: 3.527065
  ...
# Subtest: bar click opens Stats homes with day and new-leaf modifiers
ok 1728 - bar click opens Stats homes with day and new-leaf modifiers
  ---
  duration_ms: 2.747526
  ...
# Subtest: same-area roots get distinct hues and legend dots match their segments
ok 1729 - same-area roots get distinct hues and legend dots match their segments
  ---
  duration_ms: 2.776592
  ...
# Subtest: dayStripValueRuns splits numerals from units and keeps words whole
ok 1730 - dayStripValueRuns splits numerals from units and keeps words whole
  ---
  duration_ms: 0.701159
  ...
# Subtest: facts stack a label head over a faithful value with warnings in the head
ok 1731 - facts stack a label head over a faithful value with warnings in the head
  ---
  duration_ms: 63.019859
  ...
# Subtest: root-parent labels use Bob's full home label
ok 1732 - root-parent labels use Bob's full home label
  ---
  duration_ms: 1.389554
  ...
# Subtest: unfiled root paints its label in gray after real roots
ok 1733 - unfiled root paints its label in gray after real roots
  ---
  duration_ms: 1.444338
  ...
# Subtest: area roots paint the bare label with a project_label tooltip
ok 1734 - area roots paint the bare label with a project_label tooltip
  ---
  duration_ms: 1.03186
  ...
# Subtest: case-insensitive legend labels keep their full root names
ok 1735 - case-insensitive legend labels keep their full root names
  ---
  duration_ms: 1.221372
  ...
# Subtest: dayStripLegendFit fits every root, reserves the counter, and handles empty
ok 1736 - dayStripLegendFit fits every root, reserves the counter, and handles empty
  ---
  duration_ms: 0.401296
  ...
# Subtest: names mode wins only when it names strictly more roots
ok 1737 - names mode wins only when it names strictly more roots
  ---
  duration_ms: 0.205973
  ...
# Subtest: DOM glue hides overflow, writes the counter, and toggles names mode
ok 1738 - DOM glue hides overflow, writes the counter, and toggles names mode
  ---
  duration_ms: 2.428037
  ...
# Subtest: dayStripMarkState maps bool points from the bob point, never the word
ok 1739 - dayStripMarkState maps bool points from the bob point, never the word
  ---
  duration_ms: 0.679056
  ...
# Subtest: boolean facts paint an aria-hidden mark with hidden display text
ok 1740 - boolean facts paint an aria-hidden mark with hidden display text
  ---
  duration_ms: 3.270976
  ...
# Subtest: docs without createElementNS keep word runs
ok 1741 - docs without createElementNS keep word runs
  ---
  duration_ms: 7.450878
  ...
# Subtest: bool skeleton paints a round placeholder and no svg
ok 1742 - bool skeleton paints a round placeholder and no svg
  ---
  duration_ms: 1.846346
  ...
# Subtest: pending mark tooltip drops so far; numeric provisional keeps it
ok 1743 - pending mark tooltip drops so far; numeric provisional keeps it
  ---
  duration_ms: 4.935114
  ...
# Subtest: pending to met on the same host and day draws the check once
ok 1744 - pending to met on the same host and day draws the check once
  ---
  duration_ms: 3.970362
  ...
# Subtest: arrive class stays off for other mark transitions
ok 1745 - arrive class stays off for other mark transitions
  ---
  duration_ms: 16.161111
  ...
# Subtest: stroke-dashoffset lives only inside keyframes
ok 1746 - stroke-dashoffset lives only inside keyframes
  ---
  duration_ms: 4.451871
  ...
# Subtest: dayStripRef classifies bob's typical without computing it
ok 1747 - dayStripRef classifies bob's typical without computing it
  ---
  duration_ms: 0.423709
  ...
# Subtest: typical line covers every States-table row
ok 1748 - typical line covers every States-table row
  ---
  duration_ms: 2.048852
  ...
# Subtest: typical line is aria-hidden, reserved, and never a tab stop
ok 1749 - typical line is aria-hidden, reserved, and never a tab stop
  ---
  duration_ms: 16.521869
  ...
# Subtest: off-clock hint prefers Bob's display and falls back to raw Nm without arithmetic
ok 1750 - off-clock hint prefers Bob's display and falls back to raw Nm without arithmetic
  ---
  duration_ms: 1.022733
  ...
# Subtest: hint renders below WORKED beside the typical line as its own activation target
ok 1751 - hint renders below WORKED beside the typical line as its own activation target
  ---
  duration_ms: 2.12112
  ...
# Subtest: lane legends and bars keep Worked meaning while the hint opens Off-clock
ok 1752 - lane legends and bars keep Worked meaning while the hint opens Off-clock
  ---
  duration_ms: 0.926139
  ...
# Subtest: DP parse vectors
ok 1753 - DP parse vectors
  ---
  duration_ms: 3.91157
  ...
# Subtest: DC chip model vectors
ok 1754 - DC chip model vectors
  ---
  duration_ms: 9.764155
  ...
# Subtest: decoration builds one widget, reveals on cursor, skips code and ranges
ok 1755 - decoration builds one widget, reveals on cursor, skips code and ranges
  ---
  duration_ms: 29.375234
  ...
# Subtest: decoration skips paragraphs, grandchildren, and Work Log lines
ok 1756 - decoration skips paragraphs, grandchildren, and Work Log lines
  ---
  duration_ms: 16.119471
  ...
# Subtest: decoration renders chips on DP30 and still skips DP20
ok 1757 - decoration renders chips on DP30 and still skips DP20
  ---
  duration_ms: 2.050145
  ...
# Subtest: ownership check reads O(depth) lines, not the whole note
ok 1758 - ownership check reads O(depth) lines, not the whole note
  ---
  duration_ms: 7.007912
  ...
# Subtest: widget identity covers the line and the interactive flag
ok 1759 - widget identity covers the line and the interactive flag
  ---
  duration_ms: 7.634027
  ...
# Subtest: element hides actions without nav api v1
ok 1760 - element hides actions without nav api v1
  ---
  duration_ms: 1.741315
  ...
# Subtest: nav api feature detection gates actions
ok 1761 - nav api feature detection gates actions
  ---
  duration_ms: 0.579347
  ...
# Subtest: reading view decorates only the Depends-On row, hides chrome, stays idempotent
ok 1762 - reading view decorates only the Depends-On row, hides chrome, stays idempotent
  ---
  duration_ms: 16.518704
  ...
# Subtest: reading view blocked chips draw a miniature and reason line
ok 1763 - reading view blocked chips draw a miniature and reason line
  ---
  duration_ms: 6.754018
  ...
# Subtest: reading view collapses more than three Done targets to one chip
ok 1764 - reading view collapses more than three Done targets to one chip
  ---
  duration_ms: 3.455087
  ...
# Subtest: DC chip model vectors by id: DC2, DC5, DC6, DC9
ok 1765 - DC chip model vectors by id: DC2, DC5, DC6, DC9
  ---
  duration_ms: 0.604284
  ...
# Subtest: chip actions send the 0-based line index through nav api v1
ok 1766 - chip actions send the 0-based line index through nav api v1
  ---
  duration_ms: 2.175424
  ...
# Subtest: chip hover passes the chip element and its row to the preview
ok 1767 - chip hover passes the chip element and its row to the preview
  ---
  duration_ms: 0.245619
  ...
# Subtest: chip lookup index lives on the freshness memo
ok 1768 - chip lookup index lives on the freshness memo
  ---
  duration_ms: 0.770241
  ...
# Subtest: reading view hides actions when the line cannot be derived
ok 1769 - reading view hides actions when the line cannot be derived
  ---
  duration_ms: 63.893088
  ...
# Subtest: reading view actions carry the derived 0-based line
ok 1770 - reading view actions carry the derived 0-based line
  ---
  duration_ms: 9.427453
  ...
# Subtest: reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
ok 1771 - reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
  ---
  duration_ms: 9.611413
  ...
# Subtest: reading view renders chips on DP30 (owner is a task under a Work Log entry)
ok 1772 - reading view renders chips on DP30 (owner is a task under a Work Log entry)
  ---
  duration_ms: 8.922198
  ...
# Subtest: reading view DP30 row actions send the owned Depends-On line
ok 1773 - reading view DP30 row actions send the owned Depends-On line
  ---
  duration_ms: 16.875774
  ...
# Subtest: reading view second-row remove sends the second line when two tasks share a prerequisite
ok 1774 - reading view second-row remove sends the second line when two tasks share a prerequisite
  ---
  duration_ms: 23.433478
  ...
# Subtest: chip lookup index builds once per freshness memo
ok 1775 - chip lookup index builds once per freshness memo
  ---
  duration_ms: 0.728812
  ...
# Subtest: decoration evaluates ownership without copying the note
ok 1776 - decoration evaluates ownership without copying the note
  ---
  duration_ms: 3.952718
  ...
# Subtest: blockMarkReasonLine keeps only the first tooltip line
ok 1777 - blockMarkReasonLine keeps only the first tooltip line
  ---
  duration_ms: 0.18307
  ...
# Subtest: chip box fill keeps a CSS fallback glyph beside the miniature
ok 1778 - chip box fill keeps a CSS fallback glyph beside the miniature
  ---
  duration_ms: 0.748479
  ...
# Subtest: toggle flips the body class and onload wires chips
ok 1779 - toggle flips the body class and onload wires chips
  ---
  duration_ms: 242.445906
  ...
# event-link-times build: 17.6 ms
# Subtest: EL — ledger rows qualify exactly per the contract
ok 1780 - EL — ledger rows qualify exactly per the contract
  ---
  duration_ms: 15.967992
  ...
# Subtest: EL18 — a fenced ledger row gets no pill
ok 1781 - EL18 — a fenced ledger row gets no pill
  ---
  duration_ms: 0.593854
  ...
# Subtest: EL19 — a non-daily note gets no pills
ok 1782 - EL19 — a non-daily note gets no pills
  ---
  duration_ms: 0.193399
  ...
# Subtest: EL16 — the previous day's ledger pills without state
ok 1783 - EL16 — the previous day's ledger pills without state
  ---
  duration_ms: 13.522001
  ...
# Subtest: ES — the shared clock answers the contract states
ok 1784 - ES — the shared clock answers the contract states
  ---
  duration_ms: 0.645543
  ...
# Subtest: ER — resolution matches the Events pill inputs
ok 1785 - ER — resolution matches the Events pill inputs
  ---
  duration_ms: 28.652975
  ...
# Subtest: ER — non-events, duplicates, and cross-note links resolve to no pill
ok 1786 - ER — non-events, duplicates, and cross-note links resolve to no pill
  ---
  duration_ms: 0.829474
  ...
# Subtest: ER5 — Live Preview reads the live document, unsaved edits included
ok 1787 - ER5 — Live Preview reads the live document, unsaved edits included
  ---
  duration_ms: 15.763762
  ...
# Subtest: ER6 — Live Preview dashes an unsaved off-clock tag on the same frame
ok 1788 - ER6 — Live Preview dashes an unsaved off-clock tag on the same frame
  ---
  duration_ms: 11.720621
  ...
# Subtest: ER7 — the inner pill carries the Events pill attributes, minus title
ok 1789 - ER7 — the inner pill carries the Events pill attributes, minus title
  ---
  duration_ms: 16.871497
  ...
# Subtest: ET — tooltips name the event and its pill state
ok 1790 - ET — tooltips name the event and its pill state
  ---
  duration_ms: 1.838371
  ...
# Subtest: EP1 — Live Preview places the pill at the link start, side -3
ok 1791 - EP1 — Live Preview places the pill at the link start, side -3
  ---
  duration_ms: 8.553613
  ...
# Subtest: EP4 — selection alone never rebuilds the pills
ok 1792 - EP4 — selection alone never rebuilds the pills
  ---
  duration_ms: 14.876337
  ...
# Subtest: EP2/EP5 — Reading view orders the pill before progress marks and keeps the ledger context
ok 1793 - EP2/EP5 — Reading view orders the pill before progress marks and keeps the ledger context
  ---
  duration_ms: 7.431942
  ...
# Subtest: EP3 — the pill lands before the link container beside a trailing chip
ok 1794 - EP3 — the pill lands before the link container beside a trailing chip
  ---
  duration_ms: 0.671473
  ...
# Subtest: EP3/OC — Reading sweeps preserve pill/link/marks/chip order and clock parity
ok 1795 - EP3/OC — Reading sweeps preserve pill/link/marks/chip order and clock parity
  ---
  duration_ms: 9.888082
  ...
# Subtest: EP7 — a struck link keeps the pill outside the strike
ok 1796 - EP7 — a struck link keeps the pill outside the strike
  ---
  duration_ms: 2.523439
  ...
# Subtest: EL20 — either toggle off hides every pill, in JS and CSS
ok 1797 - EL20 — either toggle off hides every pill, in JS and CSS
  ---
  duration_ms: 3.130698
  ...
# Subtest: setup — toggle command, popout gates, and clock repaint wiring
ok 1798 - setup — toggle command, popout gates, and clock repaint wiring
  ---
  duration_ms: 2.641875
  ...
# Subtest: liveness — metadata and vault events coalesce into one refresh
ok 1799 - liveness — metadata and vault events coalesce into one refresh
  ---
  duration_ms: 3.922891
  ...
# Subtest: liveness — a source-text fill refreshes link pills
ok 1800 - liveness — a source-text fill refreshes link pills
  ---
  duration_ms: 1.086645
  ...
# Subtest: perf — one build over a 200-link ledger stays under 25 ms
ok 1801 - perf — one build over a 200-link ledger stays under 25 ms
  ---
  duration_ms: 36.177333
  ...
# Subtest: widget — identity follows time, state, clock, buffer, and tooltip
ok 1802 - widget — identity follows time, state, clock, buffer, and tooltip
  ---
  duration_ms: 19.149648
  ...
# Subtest: regression FakeNode hides the plan-host cycles and builds 85 nodes
ok 1803 - regression FakeNode hides the plan-host cycles and builds 85 nodes
  ---
  duration_ms: 6.005588
  ...
# Subtest: failing assert.equal and assert.deepEqual report under a 1024MB cap
ok 1804 - failing assert.equal and assert.deepEqual report under a 1024MB cap
  ---
  duration_ms: 683.837835
  ...
# Subtest: every ledger-tools FakeNode-style fake has a descriptor and hides its cyclic fields
ok 1805 - every ledger-tools FakeNode-style fake has a descriptor and hides its cyclic fields
  ---
  duration_ms: 6.202565
  ...
# Subtest: FL1-FL16: the ledger link gates match the display contract
ok 1806 - FL1-FL16: the ledger link gates match the display contract
  ---
  duration_ms: 25.850333
  ...
# Subtest: motion identity is the resolved owner path and block ID
ok 1807 - motion identity is the resolved owner path and block ID
  ---
  duration_ms: 11.928369
  ...
# Subtest: duplicate and aliased links resolve and count once per owner per build
ok 1808 - duplicate and aliased links resolve and count once per owner per build
  ---
  duration_ms: 11.012009
  ...
# Subtest: offscreen ledger targets do no resolution or count work until visible
ok 1809 - offscreen ledger targets do no resolution or count work until visible
  ---
  duration_ms: 0.545462
  ...
# Subtest: 200-link / 2000-task build stays within the 25 ms budget
not ok 1810 - 200-link / 2000-task build stays within the 25 ms budget
  ---
  duration_ms: 82.947614
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-frees-marks.cjs:481:1'
  failureType: 'testCodeFailure'
  error: 'synthetic build took 33 ms (budget 25 ms)'
  code: 'ERR_ASSERTION'
  name: 'AssertionError'
  expected: true
  actual: false
  operator: '=='
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/scripts/test-ledger-tools-frees-marks.cjs:509:10)
    Test.runInAsyncScope (node:async_hooks:211:14)
    Test.run (node:internal/test_runner/test:979:25)
    Test.processPendingSubtests (node:internal/test_runner/test:677:18)
    Test.postRun (node:internal/test_runner/test:1090:19)
    Test.run (node:internal/test_runner/test:1018:12)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: FC1-FC17: counts follow the BLOCKS last-blocker set
ok 1811 - FC1-FC17: counts follow the BLOCKS last-blocker set
  ---
  duration_ms: 16.81023
  ...
# Subtest: FT1-FT6: tooltips use BLOCKS order, clean titles, and waiting count
ok 1812 - FT1-FT6: tooltips use BLOCKS order, clean titles, and waiting count
  ---
  duration_ms: 5.38859
  ...
# Subtest: FC7-FC8: project and hidden labels follow the contract
ok 1813 - FC7-FC8: project and hidden labels follow the contract
  ---
  duration_ms: 0.554769
  ...
# Subtest: FP1-FP2: Live Preview places the widget after the link with side 2
ok 1814 - FP1-FP2: Live Preview places the widget after the link with side 2
  ---
  duration_ms: 1.967577
  ...
# Subtest: FP3-FP4: Reading view inserts after the link or after 🔓
ok 1815 - FP3-FP4: Reading view inserts after the link or after 🔓
  ---
  duration_ms: 6.686877
  ...
# Subtest: Reading view inserts beside a task-link-mark sibling and through one wrapping p
ok 1816 - Reading view inserts beside a task-link-mark sibling and through one wrapping p
  ---
  duration_ms: 6.159983
  ...
# Subtest: pinned midnight invalidates yesterday and gives today's editor a silent first paint
ok 1817 - pinned midnight invalidates yesterday and gives today's editor a silent first paint
  ---
  duration_ms: 1.919575
  ...
# Subtest: FT element and widget keep accessible attributes without a title
ok 1818 - FT element and widget keep accessible attributes without a title
  ---
  duration_ms: 0.845103
  ...
# Subtest: Live Preview tick LRU tracks 0 → N, count changes, and the 2000-key bound
ok 1819 - Live Preview tick LRU tracks 0 → N, count changes, and the 2000-key bound
  ---
  duration_ms: 6.094087
  ...
# Subtest: viewport-only rebuilds update visible count history without animating scroll-in
ok 1820 - viewport-only rebuilds update visible count history without animating scroll-in
  ---
  duration_ms: 1.109148
  ...
# Subtest: toggle, refresh effect, and modifier navigation are wired
ok 1821 - toggle, refresh effect, and modifier navigation are wired
  ---
  duration_ms: 5.559757
  ...
# Subtest: setup is idempotent and teardown clears the rollover interval
ok 1822 - setup is idempotent and teardown clears the rollover interval
  ---
  duration_ms: 0.425422
  ...
# Subtest: capability: nav card v2 is capable
ok 1823 - capability: nav card v2 is capable
  ---
  duration_ms: 1.484124
  ...
# Subtest: capability: nav card v1 is not capable
ok 1824 - capability: nav card v1 is not capable
  ---
  duration_ms: 0.430693
  ...
# Subtest: capability: absent nav, missing api, and old versions are not capable
ok 1825 - capability: absent nav, missing api, and old versions are not capable
  ---
  duration_ms: 0.192318
  ...
# Subtest: capability: a throwing app never throws
ok 1826 - capability: a throwing app never throws
  ---
  duration_ms: 0.270797
  ...
# Subtest: lane capability: nav card v3 is lane-capable, v2 is not
ok 1827 - lane capability: nav card v3 is lane-capable, v2 is not
  ---
  duration_ms: 0.276298
  ...
# Subtest: leaf: active capable due choice replaces refresh with a leaf
ok 1828 - leaf: active capable due choice replaces refresh with a leaf
  ---
  duration_ms: 34.552691
  ...
# Subtest: leaf: the same row without the card keeps refresh and counting words
ok 1829 - leaf: the same row without the card keeps refresh and counting words
  ---
  duration_ms: 0.771242
  ...
# Subtest: leaf: early dates still leaf when capable
ok 1830 - leaf: early dates still leaf when capable
  ---
  duration_ms: 0.495005
  ...
# Subtest: leaf: decay-off rows never leaf even when capable
ok 1831 - leaf: decay-off rows never leaf even when capable
  ---
  duration_ms: 0.834374
  ...
# Subtest: leaf: below-threshold rows never leaf
ok 1832 - leaf: below-threshold rows never leaf
  ---
  duration_ms: 1.309872
  ...
# Subtest: leaf: threshold zero asks on every due re-confirmation when capable
ok 1833 - leaf: threshold zero asks on every due re-confirmation when capable
  ---
  duration_ms: 0.444909
  ...
# Subtest: leaf: overflow renders capped dots with +N and the exact count in text
ok 1834 - leaf: overflow renders capped dots with +N and the exact count in text
  ---
  duration_ms: 0.337945
  ...
# Subtest: leaf: out-of-scope and closed tasks show dots quietly, never a leaf
ok 1835 - leaf: out-of-scope and closed tasks show dots quietly, never a leaf
  ---
  duration_ms: 1.050747
  ...
# Subtest: leaf: unresolved marks show dots quietly with counting-only wording
ok 1836 - leaf: unresolved marks show dots quietly with counting-only wording
  ---
  duration_ms: 9.825693
  ...
# Subtest: element: leaf marks carry data-decide true and a leaf path
ok 1837 - element: leaf marks carry data-decide true and a leaf path
  ---
  duration_ms: 1.295534
  ...
# Subtest: element: non-decision marks carry data-decide false
ok 1838 - element: non-decision marks carry data-decide false
  ---
  duration_ms: 44.625906
  ...
# Subtest: lane leaf: an at-limit Next row leaves only with the v3 card
ok 1839 - lane leaf: an at-limit Next row leaves only with the v3 card
  ---
  duration_ms: 0.637718
  ...
# Subtest: lane leaf: the same row with only the v2 card keeps counting pips
ok 1840 - lane leaf: the same row with only the v2 card keeps counting pips
  ---
  duration_ms: 0.319299
  ...
# Subtest: lane leaf: an at-limit WIP row leaves only with the v3 card
ok 1841 - lane leaf: an at-limit WIP row leaves only with the v3 card
  ---
  duration_ms: 0.379735
  ...
# Subtest: lane leaf: a false rung counts and displays but never asks
ok 1842 - lane leaf: a false rung counts and displays but never asks
  ---
  duration_ms: 0.293641
  ...
# Subtest: lane leaf: a per-rung limit drives the keeps wording
ok 1843 - lane leaf: a per-rung limit drives the keeps wording
  ---
  duration_ms: 0.269254
  ...
# Subtest: footer groups omit every zero tier and keep walk order
ok 1844 - footer groups omit every zero tier and keep walk order
  ---
  duration_ms: 6.939893
  ...
# Subtest: PRE and POST groups bracket the nine-tier queue and expose completion hints
ok 1845 - PRE and POST groups bracket the nine-tier queue and expose completion hints
  ---
  duration_ms: 13.946802
  ...
# Subtest: a NEW-state project appears only in its walk tier
ok 1846 - a NEW-state project appears only in its walk tier
  ---
  duration_ms: 0.396046
  ...
# Subtest: empty queue hides the footer even with upkeep or a met budget
ok 1847 - empty queue hides the footer even with upkeep or a met budget
  ---
  duration_ms: 0.327976
  ...
# Subtest: unavailable or missing data never render false counts
ok 1848 - unavailable or missing data never render false counts
  ---
  duration_ms: 0.21442
  ...
# Subtest: generic summary names due, commitments, and nonempty groups
ok 1849 - generic summary names due, commitments, and nonempty groups
  ---
  duration_ms: 0.562424
  ...
# Subtest: current-task context uses shared ranks and compact wording
ok 1850 - current-task context uses shared ranks and compact wording
  ---
  duration_ms: 0.962258
  ...
# Subtest: only ROTTEN remaining names commitments done or a met budget
ok 1851 - only ROTTEN remaining names commitments done or a met budget
  ---
  duration_ms: 0.330291
  ...
# Subtest: NEW and commitments take precedence over a met budget
ok 1852 - NEW and commitments take precedence over a met budget
  ---
  duration_ms: 0.551664
  ...
# Subtest: reviewEntryView compact and detail cover the original freshness tiers
ok 1853 - reviewEntryView compact and detail cover the original freshness tiers
  ---
  duration_ms: 1.142231
  ...
# Subtest: cursor matching requires a unique verified identity
ok 1854 - cursor matching requires a unique verified identity
  ---
  duration_ms: 0.515364
  ...
# Subtest: footer paint hides the host and keeps a stable button
ok 1855 - footer paint hides the host and keeps a stable button
  ---
  duration_ms: 14.796214
  ...
# Subtest: groups paint as tier-keyed tokens and repaint without stale nodes
ok 1856 - groups paint as tier-keyed tokens and repaint without stale nodes
  ---
  duration_ms: 1.340069
  ...
# Subtest: group boundary marks only the commitments-to-upkeep cut
ok 1857 - group boundary marks only the commitments-to-upkeep cut
  ---
  duration_ms: 0.703784
  ...
# Subtest: context ink follows supported current tiers and clears on other views
ok 1858 - context ink follows supported current tiers and clears on other views
  ---
  duration_ms: 17.313361
  ...
# Subtest: progressive fit sheds tail groups, then detail, hint, and meter
ok 1859 - progressive fit sheds tail groups, then detail, hint, and meter
  ---
  duration_ms: 3.887203
  ...
# Subtest: the footer stylesheet defines every tier ink and removes NEW accent overrides
ok 1860 - the footer stylesheet defines every tier ink and removes NEW accent overrides
  ---
  duration_ms: 2.28804
  ...
# Subtest: status bar 0-1-0 transitions hide without a reload
ok 1861 - status bar 0-1-0 transitions hide without a reload
  ---
  duration_ms: 146.415289
  ...
# Subtest: cursor-only updates reuse a warm memo
ok 1862 - cursor-only updates reuse a warm memo
  ---
  duration_ms: 179.79536
  ...
# Subtest: unload disconnects the observer and click handler
ok 1863 - unload disconnects the observer and click handler
  ---
  duration_ms: 227.315464
  ...
# Subtest: queue-built ranks agree with the footer current entry
ok 1864 - queue-built ranks agree with the footer current entry
  ---
  duration_ms: 1.73874
  ...
# Subtest: footer short labels map every tier
ok 1865 - footer short labels map every tier
  ---
  duration_ms: 0.175204
  ...
# Subtest: current-row footer context uses short labels while entry views keep full labels
ok 1866 - current-row footer context uses short labels while entry views keep full labels
  ---
  duration_ms: 0.319079
  ...
# Subtest: legend line lists only current abbreviated tiers
ok 1867 - legend line lists only current abbreviated tiers
  ---
  duration_ms: 0.384014
  ...
# Subtest: queue-row quickRoll preview takes the hint slot, tooltip, and aria
ok 1868 - queue-row quickRoll preview takes the hint slot, tooltip, and aria
  ---
  duration_ms: 15.345784
  ...
# Subtest: quickRoll detail sits next to the action hint on lane rows
ok 1869 - quickRoll detail sits next to the action hint on lane rows
  ---
  duration_ms: 0.373874
  ...
# Subtest: missing or failed quickRoll leaves a queue-row footer byte-identical
ok 1870 - missing or failed quickRoll leaves a queue-row footer byte-identical
  ---
  duration_ms: 0.631666
  ...
# Subtest: off-walk prioritized preview replaces ]s next
ok 1871 - off-walk prioritized preview replaces ]s next
  ---
  duration_ms: 0.441643
  ...
# Subtest: off-walk assign or kind-less preview keeps ]s next
ok 1872 - off-walk assign or kind-less preview keeps ]s next
  ---
  duration_ms: 0.400384
  ...
# Subtest: empty queue with a prioritized preview paints a hint-only footer
ok 1873 - empty queue with a prioritized preview paints a hint-only footer
  ---
  duration_ms: 0.404002
  ...
# Subtest: PRE rows stay unchanged under the nav checklist-tier contract
ok 1874 - PRE rows stay unchanged under the nav checklist-tier contract
  ---
  duration_ms: 0.274023
  ...
# Subtest: status bar wires nav api.quickRoll into the hint slot
ok 1875 - status bar wires nav api.quickRoll into the hint slot
  ---
  duration_ms: 209.551341
  ...
# Subtest: empty-queue status bar previews only a checkbox task line
ok 1876 - empty-queue status bar previews only a checkbox task line
  ---
  duration_ms: 342.752248
  ...
# Subtest: off-walk task preview works with a queue and survives its 1-to-0 transition
ok 1877 - off-walk task preview works with a queue and survives its 1-to-0 transition
  ---
  duration_ms: 286.114124
  ...
# Subtest: status bar ignores missing, v0, or throwing quickRoll namespaces
ok 1878 - status bar ignores missing, v0, or throwing quickRoll namespaces
  ---
  duration_ms: 1286.901753
  ...
# Subtest: answer tiers list only tickler
ok 1879 - answer tiers list only tickler
  ---
  duration_ms: 0.311675
  ...
# Subtest: freshnessFooterAnswerChip builds structured segments for every kind
ok 1880 - freshnessFooterAnswerChip builds structured segments for every kind
  ---
  duration_ms: 1.710176
  ...
# Subtest: a TICK row with a preview has answer set and unchanged hint, tooltip, and aria
ok 1881 - a TICK row with a preview has answer set and unchanged hint, tooltip, and aria
  ---
  duration_ms: 0.696881
  ...
# Subtest: a TICK view paints the answer chip and reuses or clears it by key
ok 1882 - a TICK view paints the answer chip and reuses or clears it by key
  ---
  duration_ms: 42.586021
  ...
# Subtest: a TICK fit sheds the meter before the hint chip
ok 1883 - a TICK fit sheds the meter before the hint chip
  ---
  duration_ms: 1.152441
  ...
# Subtest: the footer stylesheet defines the TICK answer chip
ok 1884 - the footer stylesheet defines the TICK answer chip
  ---
  duration_ms: 14.635526
  ...
# Subtest: walker host keeps the same status item and marks it
ok 1885 - walker host keeps the same status item and marks it
  ---
  duration_ms: 175.69931
  ...
# Subtest: gated s panel keeps the review footer with ]] next hints
ok 1886 - gated s panel keeps the review footer with ]] next hints
  ---
  duration_ms: 184.902082
  ...
# Subtest: n routes to links while w and unset hide the panel
ok 1887 - n routes to links while w and unset hide the panel
  ---
  duration_ms: 621.269745
  ...
# Subtest: an invalid stored family never paints as s
ok 1888 - an invalid stored family never paints as s
  ---
  duration_ms: 197.627011
  ...
# Subtest: doorbell repaints synchronously on family change
ok 1889 - doorbell repaints synchronously on family change
  ---
  duration_ms: 204.761264
  ...
# Subtest: empty queue paints Review clear while s is selected
ok 1890 - empty queue paints Review clear while s is selected
  ---
  duration_ms: 305.696288
  ...
# Subtest: clear state keeps the prioritized Alt+P preview
ok 1891 - clear state keeps the prioritized Alt+P preview
  ---
  duration_ms: 153.425768
  ...
# Subtest: legacy fallback without nav paints today's footer byte-identical
ok 1892 - legacy fallback without nav paints today's footer byte-identical
  ---
  duration_ms: 72.219276
  ...
# Subtest: old nav without walkMode keeps the ]s next legacy footer
ok 1893 - old nav without walkMode keeps the ]s next legacy footer
  ---
  duration_ms: 119.310893
  ...
# Subtest: late nav arrival gates the footer; nav removal restores legacy
ok 1894 - late nav arrival gates the footer; nav removal restores legacy
  ---
  duration_ms: 398.906527
  ...
# Subtest: unload and reload mount one item and one doorbell subscription
ok 1895 - unload and reload mount one item and one doorbell subscription
  ---
  duration_ms: 280.976233
  ...
# Subtest: a throwing doorbell path never breaks setup or painting
ok 1896 - a throwing doorbell path never breaks setup or painting
  ---
  duration_ms: 119.634852
  ...
# Subtest: K1 absent: no keeps means 0 with no lints
ok 1897 - K1 absent: no keeps means 0 with no lints
  ---
  duration_ms: 28.899746
  ...
# Subtest: K8 misplaced: keeps inside the Tasks suffix reads with a lint
ok 1898 - K8 misplaced: keeps inside the Tasks suffix reads with a lint
  ---
  duration_ms: 17.163094
  ...
# Subtest: K9 duplicates and invalid values: first valid wins, else 0
ok 1899 - K9 duplicates and invalid values: first valid wins, else 0
  ---
  duration_ms: 19.254666
  ...
# Subtest: K10 ceiling and NEW: 999 reads, never-confirmed reads 0
ok 1900 - K10 ceiling and NEW: 999 reads, never-confirmed reads 0
  ---
  duration_ms: 0.420373
  ...
# Subtest: K13 exact keys: near-miss keys are not keeps; parens read
ok 1901 - K13 exact keys: near-miss keys are not keeps; parens read
  ---
  duration_ms: 0.256941
  ...
# Subtest: keeps value parser accepts only decimal 1-999
ok 1902 - keeps value parser accepts only decimal 1-999
  ---
  duration_ms: 0.241942
  ...
# Subtest: K2 first valid canonical: uncounted keep preserves and repairs
ok 1903 - K2 first valid canonical: uncounted keep preserves and repairs
  ---
  duration_ms: 1.301806
  ...
# Subtest: K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
ok 1904 - K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
  ---
  duration_ms: 0.745724
  ...
# Subtest: K4 same-day preserve noop: canonical kept line is byte-identical
ok 1905 - K4 same-day preserve noop: canonical kept line is byte-identical
  ---
  duration_ms: 28.843208
  ...
# Subtest: K5 generic stamp clears, even same-day
ok 1906 - K5 generic stamp clears, even same-day
  ---
  duration_ms: 0.855293
  ...
# Subtest: K6 set-refresh clears keeps
ok 1907 - K6 set-refresh clears keeps
  ---
  duration_ms: 0.381218
  ...
# Subtest: K7 stale stamp clears keeps
ok 1908 - K7 stale stamp clears keeps
  ---
  duration_ms: 0.241351
  ...
# Subtest: K8b misplaced keeps repaired to canonical order by a keep
ok 1909 - K8b misplaced keeps repaired to canonical order by a keep
  ---
  duration_ms: 0.274093
  ...
# Subtest: K11 refusals preserve: closed and recurring lines never write
ok 1910 - K11 refusals preserve: closed and recurring lines never write
  ---
  duration_ms: 0.31915
  ...
# Subtest: Pomodoro ledger rows are refused byte-for-byte by counted and uncounted keep
ok 1911 - Pomodoro ledger rows are refused byte-for-byte by counted and uncounted keep
  ---
  duration_ms: 0.569708
  ...
# Subtest: counted keep increments a stale streak once in the same write
ok 1912 - counted keep increments a stale streak once in the same write
  ---
  duration_ms: 0.274123
  ...
# Subtest: first counted keep on a streakless due task writes keeps 1
ok 1913 - first counted keep on a streakless due task writes keeps 1
  ---
  duration_ms: 5.338514
  ...
# Subtest: counted keep saturates at 999 and never wraps
ok 1914 - counted keep saturates at 999 and never wraps
  ---
  duration_ms: 0.610676
  ...
# Subtest: counted keep needs a valid prior fresh before today
ok 1915 - counted keep needs a valid prior fresh before today
  ---
  duration_ms: 0.468465
  ...
# Subtest: counted keep repairs malformed and duplicate placement
ok 1916 - counted keep repairs malformed and duplicate placement
  ---
  duration_ms: 0.437175
  ...
# Subtest: uncounted keep preserves the valid value while canonicalizing
ok 1917 - uncounted keep preserves the valid value while canonicalizing
  ---
  duration_ms: 0.316404
  ...
# Subtest: UB13 keep on an unblock TICKLER preserves the streak and skips the card
ok 1918 - UB13 keep on an unblock TICKLER preserves the streak and skips the card
  ---
  duration_ms: 18.83147
  ...
# Subtest: a scheduled tickler still counts when schedule wins an unblock tie
ok 1919 - a scheduled tickler still counts when schedule wins an unblock tie
  ---
  duration_ms: 0.519652
  ...
# Subtest: decay normalization: absent, null, true, and {} enable with 3
ok 1920 - decay normalization: absent, null, true, and {} enable with 3
  ---
  duration_ms: 18.89933
  ...
# Subtest: decay false counts and displays but never asks
ok 1921 - decay false counts and displays but never asks
  ---
  duration_ms: 0.294432
  ...
# Subtest: decay keeps 0 and fixed entry normalize
ok 1922 - decay keeps 0 and fixed entry normalize
  ---
  duration_ms: 0.241912
  ...
# Subtest: C14 pending override resolves while other rungs fall back
ok 1923 - C14 pending override resolves while other rungs fall back
  ---
  duration_ms: 0.168872
  ...
# Subtest: C15 fallback plus next override
ok 1924 - C15 fallback plus next override
  ---
  duration_ms: 0.176948
  ...
# Subtest: C16 zero, false, and 999 rungs
ok 1925 - C16 zero, false, and 999 rungs
  ---
  duration_ms: 0.293801
  ...
# Subtest: C17 null rung falls back to keeps
ok 1926 - C17 null rung falls back to keeps
  ---
  duration_ms: 0.264254
  ...
# Subtest: rung limit helper resolves numbers, false, and fallbacks
ok 1927 - rung limit helper resolves numbers, false, and fallbacks
  ---
  duration_ms: 0.17316
  ...
# Subtest: invalid decay shapes fail the freshness config contract
ok 1928 - invalid decay shapes fail the freshness config contract
  ---
  duration_ms: 31.328845
  ...
# Subtest: B: at-limit Ready due rows decide on every local day
ok 1929 - B: at-limit Ready due rows decide on every local day
  ---
  duration_ms: 1.009788
  ...
# Subtest: D1 early date: an at-limit Ready due row decides
ok 1930 - D1 early date: an at-limit Ready due row decides
  ---
  duration_ms: 0.179613
  ...
# Subtest: D2 at limit decides; D3 below limit stamps without a card
ok 1931 - D2 at limit decides; D3 below limit stamps without a card
  ---
  duration_ms: 0.181357
  ...
# Subtest: D4 tickler counts as due; D5 NEW never decides
ok 1932 - D4 tickler counts as due; D5 NEW never decides
  ---
  duration_ms: 0.142662
  ...
# Subtest: D6 zero limit asks on every due Ready re-confirmation
ok 1933 - D6 zero limit asks on every due Ready re-confirmation
  ---
  duration_ms: 0.134657
  ...
# Subtest: D7 off never asks; D8 an at-limit Next due row decides
ok 1934 - D7 off never asks; D8 an at-limit Next due row decides
  ---
  duration_ms: 0.134697
  ...
# Subtest: D9 pending at limit decides; D10-D11 below limit stay quiet
ok 1935 - D9 pending at limit decides; D10-D11 below limit stay quiet
  ---
  duration_ms: 0.132914
  ...
# Subtest: D12 next_keeps false never asks; D13 pending_keeps 0 always asks
ok 1936 - D12 next_keeps false never asks; D13 pending_keeps 0 always asks
  ---
  duration_ms: 0.296627
  ...
# Subtest: D14 today-linked lane rows never decide
ok 1937 - D14 today-linked lane rows never decide
  ---
  duration_ms: 0.132383
  ...
# Subtest: D15 projects never decide; D16 unblock ticklers never decide
ok 1938 - D15 projects never decide; D16 unblock ticklers never decide
  ---
  duration_ms: 0.124177
  ...
# Subtest: D17-D18 next_keeps override of 5 decides at 5, quiet at 4
ok 1939 - D17-D18 next_keeps override of 5 decides at 5, quiet at 4
  ---
  duration_ms: 0.155517
  ...
# Subtest: lane rows decide through the evaluator, queue, and counts
ok 1940 - lane rows decide through the evaluator, queue, and counts
  ---
  duration_ms: 0.99477
  ...
# Subtest: evaluator, queue, and counts carry keeps and decide
ok 1941 - evaluator, queue, and counts carry keeps and decide
  ---
  duration_ms: 38.020994
  ...
# Subtest: no keeps: the existing mark is unchanged
ok 1942 - no keeps: the existing mark is unchanged
  ---
  duration_ms: 1.58139
  ...
# Subtest: aging with two keeps: faint pips plus a counting-only line
ok 1943 - aging with two keeps: faint pips plus a counting-only line
  ---
  duration_ms: 0.425773
  ...
# Subtest: confirmed today with two keeps: check glyph, faint dots
ok 1944 - confirmed today with two keeps: check glyph, faint dots
  ---
  duration_ms: 0.307136
  ...
# Subtest: due below threshold: orange capsule keeps its glyph, adds dots
ok 1945 - due below threshold: orange capsule keeps its glyph, adds dots
  ---
  duration_ms: 0.332535
  ...
# Subtest: resting marks show historical dots quietly and never decide
ok 1946 - resting marks show historical dots quietly and never decide
  ---
  duration_ms: 52.982194
  ...
# Subtest: active decision due: data stays truthful, leaf stays gated
ok 1947 - active decision due: data stays truthful, leaf stays gated
  ---
  duration_ms: 0.473584
  ...
# Subtest: dot caps follow the threshold with +N overflow
ok 1948 - dot caps follow the threshold with +N overflow
  ---
  duration_ms: 0.867917
  ...
# Subtest: keeps tooltip wording: singulars, zero threshold, off state
ok 1949 - keeps tooltip wording: singulars, zero threshold, off state
  ---
  duration_ms: 0.144646
  ...
# Subtest: noncanonical keeps never fold but keep their repair pill
ok 1950 - noncanonical keeps never fold but keep their repair pill
  ---
  duration_ms: 0.412528
  ...
# Subtest: quoted lines fold; rendered fragments fold without task checks
ok 1951 - quoted lines fold; rendered fragments fold without task checks
  ---
  duration_ms: 0.301496
  ...
# Subtest: unresolved marks show the line's own pips quietly and never decide
ok 1952 - unresolved marks show the line's own pips quietly and never decide
  ---
  duration_ms: 0.227324
  ...
# Subtest: consensus sees count and decision eligibility: ambiguity stays neutral
ok 1953 - consensus sees count and decision eligibility: ambiguity stays neutral
  ---
  duration_ms: 25.051858
  ...
# Subtest: pips render as one aria-hidden span with the count in the label
ok 1954 - pips render as one aria-hidden span with the count in the label
  ---
  duration_ms: 1.510985
  ...
# Subtest: Live Preview decorates the folded range including space and refresh
ok 1955 - Live Preview decorates the folded range including space and refresh
  ---
  duration_ms: 15.387053
  ...
# Subtest: Live Preview reveals the raw field when the cursor overlaps either edge
ok 1956 - Live Preview reveals the raw field when the cursor overlaps either edge
  ---
  duration_ms: 1.940926
  ...
# Subtest: Live Preview skips codeblock and inline code spans
ok 1957 - Live Preview skips codeblock and inline code spans
  ---
  duration_ms: 0.852308
  ...
# Subtest: source mode and marks-off yield no decorations
ok 1958 - source mode and marks-off yield no decorations
  ---
  duration_ms: 0.210582
  ...
# Subtest: update rebuilds on the refresh effect and widget eq is stable
ok 1959 - update rebuilds on the refresh effect and widget eq is stable
  ---
  duration_ms: 1.363794
  ...
# Subtest: widget click reveals the field at the folded offset
ok 1960 - widget click reveals the field at the folded offset
  ---
  duration_ms: 1.069061
  ...
# Subtest: line resolver prefers exact, then consensus, then unresolved
ok 1961 - line resolver prefers exact, then consensus, then unresolved
  ---
  duration_ms: 1.76975
  ...
# Subtest: decoration builds reuse the snapshot without touching the loader
ok 1962 - decoration builds reuse the snapshot without touching the loader
  ---
  duration_ms: 0.633519
  ...
# Subtest: rendered views split text nodes and skip excluded ancestors
ok 1963 - rendered views split text nodes and skip excluded ancestors
  ---
  duration_ms: 2.718611
  ...
# Subtest: rendered views stay idempotent
ok 1964 - rendered views stay idempotent
  ---
  duration_ms: 0.805598
  ...
# Subtest: text resolver reaches consensus and degrades to neutral
ok 1965 - text resolver reaches consensus and degrades to neutral
  ---
  duration_ms: 0.860403
  ...
# Subtest: session toggle flips the body class and notifies
ok 1966 - session toggle flips the body class and notifies
  ---
  duration_ms: 1.315532
  ...
# Subtest: Live Preview reads only the child block and never calls doc.toString
ok 1967 - Live Preview reads only the child block and never calls doc.toString
  ---
  duration_ms: 2.234117
  ...
# Subtest: Live Preview stops at the first nonblank line at or above the task
ok 1968 - Live Preview stops at the first nonblank line at or above the task
  ---
  duration_ms: 0.41909
  ...
# Subtest: Live Preview performance stays bounded on a large child block
ok 1969 - Live Preview performance stays bounded on a large child block
  ---
  duration_ms: 2102.600634
  ...
# Subtest: reading view shows the rotten line and excludes Tasks and Dataview rows
ok 1970 - reading view shows the rotten line and excludes Tasks and Dataview rows
  ---
  duration_ms: 1.036138
  ...
# Subtest: reading-view DOM history counts a Next lane entry
ok 1971 - reading-view DOM history counts a Next lane entry
  ---
  duration_ms: 0.905279
  ...
# Subtest: query-row consensus stays byte-identical with and without a Rotten Log
ok 1972 - query-row consensus stays byte-identical with and without a Rotten Log
  ---
  duration_ms: 0.537146
  ...
# Subtest: onload registers the toggle, extension, and post-processor
ok 1973 - onload registers the toggle, extension, and post-processor
  ---
  duration_ms: 73.00651
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 1974 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 0.86375
  ...
# Subtest: shared grammar fixture round-trips parse vectors and tallies
ok 1975 - shared grammar fixture round-trips parse vectors and tallies
  ---
  duration_ms: 48.061496
  ...
# Subtest: M1 today: check glyph, today label, full ring
ok 1976 - M1 today: check glyph, today label, full ring
  ---
  duration_ms: 24.400665
  ...
# Subtest: M2 aging: ring glyph, 3d label, draining lease
ok 1977 - M2 aging: ring glyph, 3d label, draining lease
  ---
  duration_ms: 0.661252
  ...
# Subtest: M3 boundary: ROTTEN due capsule with Alt+F hint
ok 1978 - M3 boundary: ROTTEN due capsule with Alt+F hint
  ---
  duration_ms: 12.240023
  ...
# Subtest: checklist marks replace stamp hints with their completion tier
ok 1979 - checklist marks replace stamp hints with their completion tier
  ---
  duration_ms: 1.289051
  ...
# Subtest: M4 yesterday uses the yesterday relative
ok 1980 - M4 yesterday uses the yesterday relative
  ---
  duration_ms: 0.345209
  ...
# Subtest: M5 folded refresh shows the /14d suffix
ok 1981 - M5 folded refresh shows the /14d suffix
  ---
  duration_ms: 0.702021
  ...
# Subtest: M6 refresh today: today tone hides the interval suffix
ok 1982 - M6 refresh today: today tone hides the interval suffix
  ---
  duration_ms: 0.34588
  ...
# Subtest: M7 note interval stays tooltip-only
ok 1983 - M7 note interval stays tooltip-only
  ---
  duration_ms: 21.395226
  ...
# Subtest: M8 resurfaced: due tone on the scheduled return
ok 1984 - M8 resurfaced: due tone on the scheduled return
  ---
  duration_ms: 1.017343
  ...
# Subtest: M9 due NEXT lane with keep/release/today keys
ok 1985 - M9 due NEXT lane with keep/release/today keys
  ---
  duration_ms: 42.406268
  ...
# Subtest: M10 NEXT lane stamped today
ok 1986 - M10 NEXT lane stamped today
  ---
  duration_ms: 0.552625
  ...
# Subtest: M19 disabled Next lane rests
ok 1987 - M19 disabled Next lane rests
  ---
  duration_ms: 0.425863
  ...
# Subtest: M20 PENDING lane folds refresh without the suffix
ok 1988 - M20 PENDING lane folds refresh without the suffix
  ---
  duration_ms: 0.333296
  ...
# Subtest: M11 closed: resting beats age 0
ok 1989 - M11 closed: resting beats age 0
  ---
  duration_ms: 0.289042
  ...
# Subtest: M12 unresolved running and M13 unresolved lease over
ok 1990 - M12 unresolved running and M13 unresolved lease over
  ---
  duration_ms: 0.297658
  ...
# Subtest: M14 linked today rests with its reason
ok 1991 - M14 linked today rests with its reason
  ---
  duration_ms: 0.317577
  ...
# Subtest: M15 other year shows the year and the 282d age
ok 1992 - M15 other year shows the year and the 282d age
  ---
  duration_ms: 0.250879
  ...
# Subtest: M16 quoted line keeps foldSpace
ok 1993 - M16 quoted line keeps foldSpace
  ---
  duration_ms: 0.207576
  ...
# Subtest: M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
ok 1994 - M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
  ---
  duration_ms: 0.509383
  ...
# Subtest: N1-N6 non-canonical lines get no mark
ok 1995 - N1-N6 non-canonical lines get no mark
  ---
  duration_ms: 24.487731
  ...
# Subtest: C1-C3 consensus is exact or unresolved
ok 1996 - C1-C3 consensus is exact or unresolved
  ---
  duration_ms: 0.887394
  ...
# Subtest: freshnessMarkResolution treats evaluator new as unresolved
ok 1997 - freshnessMarkResolution treats evaluator new as unresolved
  ---
  duration_ms: 0.149676
  ...
# Subtest: freshnessMarkSourceInText covers rendered fragments
ok 1998 - freshnessMarkSourceInText covers rendered fragments
  ---
  duration_ms: 0.255578
  ...
# Subtest: tone order: closed, then due, then age 0, then out of scope
ok 1999 - tone order: closed, then due, then age 0, then out of scope
  ---
  duration_ms: 0.550181
  ...
# Subtest: no tooltip ever contains a double colon
ok 2000 - no tooltip ever contains a double colon
  ---
  duration_ms: 0.994298
  ...
# Subtest: freshnessShortDate pins English names and the year rule
ok 2001 - freshnessShortDate pins English names and the year rule
  ---
  duration_ms: 0.144867
  ...
# Subtest: DOM builder structure, attributes, and ring geometry
ok 2002 - DOM builder structure, attributes, and ring geometry
  ---
  duration_ms: 30.524709
  ...
# Subtest: every mark helper is synchronous and never throws on bad input
ok 2003 - every mark helper is synchronous and never throws on bad input
  ---
  duration_ms: 0.191906
  ...
# Subtest: rotten line wording covers 0, 1, and many entries
ok 2004 - rotten line wording covers 0, 1, and many entries
  ---
  duration_ms: 0.623982
  ...
# Subtest: rotten line date format includes the year only when it differs
ok 2005 - rotten line date format includes the year only when it differs
  ---
  duration_ms: 0.197617
  ...
# Subtest: rotten line truncates the reason to 48 code points without splitting emoji
ok 2006 - rotten line truncates the reason to 48 code points without splitting emoji
  ---
  duration_ms: 0.19882
  ...
# Subtest: rotten history rejects ambiguous, invalid, and nested entries
ok 2007 - rotten history rejects ambiguous, invalid, and nested entries
  ---
  duration_ms: 19.991195
  ...
# Subtest: rotten marker vectors reject mismatched emoji and missing spaces
ok 2008 - rotten marker vectors reject mismatched emoji and missing spaces
  ---
  duration_ms: 4.988606
  ...
# Subtest: rotten line splices before the action line and reaches aria-label
ok 2009 - rotten line splices before the action line and reaches aria-label
  ---
  duration_ms: 0.816128
  ...
# Subtest: freshness namespace v14 exposes checklist stages with per-rung decay and unblock TICKLER writers
ok 2010 - freshness namespace v14 exposes checklist stages with per-rung decay and unblock TICKLER writers
  ---
  duration_ms: 287.786667
  ...
# Subtest: freshness state and count API expose an unblock return source
ok 2011 - freshness state and count API expose an unblock return source
  ---
  duration_ms: 186.415152
  ...
# Subtest: checklist rows report tier and rank while keeping the READY bucket null
ok 2012 - checklist rows report tier and rank while keeping the READY bucket null
  ---
  duration_ms: 245.618304
  ...
# Subtest: tier, isDue, and rank cover lane rows
ok 2013 - tier, isDue, and rank cover lane rows
  ---
  duration_ms: 256.759959
  ...
# Subtest: memo invalidates on a new tasks array, rollover, and frontmatter
ok 2014 - memo invalidates on a new tasks array, rollover, and frontmatter
  ---
  duration_ms: 86.23405
  ...
# Subtest: the reload event fires only when the due key set changes
ok 2015 - the reload event fires only when the due key set changes
  ---
  duration_ms: 243.246355
  ...
# Subtest: status bar text covers every state, and a missing host stays quiet
ok 2016 - status bar text covers every state, and a missing host stays quiet
  ---
  duration_ms: 311.611623
  ...
# Subtest: status bar clicks through, falling back to rotten
ok 2017 - status bar clicks through, falling back to rotten
  ---
  duration_ms: 662.726138
  ...
# Subtest: every freshness api member is synchronous and never throws
ok 2018 - every freshness api member is synchronous and never throws
  ---
  duration_ms: 319.28723
  ...
# Subtest: placement vectors P1-P11, P14-P16, P18 stamp canonically
ok 2019 - placement vectors P1-P11, P14-P16, P18 stamp canonically
  ---
  duration_ms: 25.57138
  ...
# Subtest: P12 set and clear refresh stamps alongside
ok 2020 - P12 set and clear refresh stamps alongside
  ---
  duration_ms: 0.596239
  ...
# Subtest: P13 recurring and P17 done tasks are refused unchanged
ok 2021 - P13 recurring and P17 done tasks are refused unchanged
  ---
  duration_ms: 0.357453
  ...
# Subtest: Pomodoro ledger rows are refused byte-for-byte by every fresh writer
ok 2022 - Pomodoro ledger rows are refused byte-for-byte by every fresh writer
  ---
  duration_ms: 0.765001
  ...
# Subtest: a time range later in task prose remains eligible for freshness
ok 2023 - a time range later in task prose remains eligible for freshness
  ---
  duration_ms: 0.229689
  ...
# Subtest: U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
ok 2024 - U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
  ---
  duration_ms: 21.552917
  ...
# Subtest: reader reports misplaced and duplicate fields
ok 2025 - reader reports misplaced and duplicate fields
  ---
  duration_ms: 0.528749
  ...
# Subtest: Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
ok 2026 - Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
  ---
  duration_ms: 74.305311
  ...
# Subtest: Q2 tier order beats path order
ok 2027 - Q2 tier order beats path order
  ---
  duration_ms: 1.464446
  ...
# Subtest: L1 lane due and stamped today
ok 2028 - L1 lane due and stamped today
  ---
  duration_ms: 0.465519
  ...
# Subtest: L2 lane overrides refresh
ok 2029 - L2 lane overrides refresh
  ---
  duration_ms: 17.086558
  ...
# Subtest: L3 lane exclusions have no tier
ok 2030 - L3 lane exclusions have no tier
  ---
  duration_ms: 0.546975
  ...
# Subtest: L4 lane off switch and null default
ok 2031 - L4 lane off switch and null default
  ---
  duration_ms: 0.234368
  ...
# Subtest: L5 lane order never stamped first
ok 2032 - L5 lane order never stamped first
  ---
  duration_ms: 0.631837
  ...
# Subtest: R1 TICKLER beats older ROTTEN
ok 2033 - R1 TICKLER beats older ROTTEN
  ---
  duration_ms: 0.37706
  ...
# Subtest: R2 tickler orders by due date then path and line
ok 2034 - R2 tickler orders by due date then path and line
  ---
  duration_ms: 24.889346
  ...
# Subtest: missing created sorts after dated peers
ok 2035 - missing created sorts after dated peers
  ---
  duration_ms: 1.517488
  ...
# Subtest: B1 upkeep counts outside the lanes
ok 2036 - B1 upkeep counts outside the lanes
  ---
  duration_ms: 31.145074
  ...
# Subtest: review model meter uses upkeep and exposes refreshed
ok 2037 - review model meter uses upkeep and exposes refreshed
  ---
  duration_ms: 0.537857
  ...
# Subtest: RC1 arrived: past scheduled walks RECURRING with lane and null state
ok 2038 - RC1 arrived: past scheduled walks RECURRING with lane and null state
  ---
  duration_ms: 12.139852
  ...
# Subtest: RC2 arrives today: due today with zero days overdue
ok 2039 - RC2 arrives today: due today with zero days overdue
  ---
  duration_ms: 0.689758
  ...
# Subtest: RC3 not yet: future scheduled walks nowhere
ok 2040 - RC3 not yet: future scheduled walks nowhere
  ---
  duration_ms: 0.300965
  ...
# Subtest: RC4 due only, past: the due date is the occurrence
ok 2041 - RC4 due only, past: the due date is the occurrence
  ---
  duration_ms: 0.320141
  ...
# Subtest: RC5 due only, future: walks nowhere
ok 2042 - RC5 due only, future: walks nowhere
  ---
  duration_ms: 0.31928
  ...
# Subtest: RC6 earliest date wins across start and due
ok 2043 - RC6 earliest date wins across start and due
  ---
  duration_ms: 0.34588
  ...
# Subtest: RC7 undated: no occurrence, no tier
ok 2044 - RC7 undated: no occurrence, no tier
  ---
  duration_ms: 0.38754
  ...
# Subtest: RC8 lanes: recurring lane rows keep their lane with null state
ok 2045 - RC8 lanes: recurring lane rows keep their lane with null state
  ---
  duration_ms: 0.625083
  ...
# Subtest: RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
ok 2046 - RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
  ---
  duration_ms: 6.53051
  ...
# Subtest: RC10 checklist wins: a recurring chore stays in its checklist tier
ok 2047 - RC10 checklist wins: a recurring chore stays in its checklist tier
  ---
  duration_ms: 0.5974
  ...
# Subtest: RC11 a stray stamp is ignored: recurring with null state
ok 2048 - RC11 a stray stamp is ignored: recurring with null state
  ---
  duration_ms: 0.511507
  ...
# Subtest: RC12 order and counts: due_on, then path, then line; recurring adds no due
ok 2049 - RC12 order and counts: due_on, then path, then line; recurring adds no due
  ---
  duration_ms: 5.979378
  ...
# Subtest: recurring rows adapt due and start from Tasks fields and inline fallbacks
ok 2050 - recurring rows adapt due and start from Tasks fields and inline fallbacks
  ---
  duration_ms: 1.700497
  ...
# Subtest: status view counts RECURRING as a due commitment tier
ok 2051 - status view counts RECURRING as a due commitment tier
  ---
  duration_ms: 0.46117
  ...
# Subtest: footer groups, entry view, and legend cover RECURRING
ok 2052 - footer groups, entry view, and legend cover RECURRING
  ---
  duration_ms: 5.886801
  ...
# Subtest: a stale-stamped recurring row marks due with the resolve hint
ok 2053 - a stale-stamped recurring row marks due with the resolve hint
  ---
  duration_ms: 1.348385
  ...
# Subtest: freshness namespace v14 keeps recurring and removes reference capabilities
ok 2054 - freshness namespace v14 keeps recurring and removes reference capabilities
  ---
  duration_ms: 133.873642
  ...
# Subtest: hidden recurring ^ref keeps ordinary visibility (Rust parity)
ok 2055 - hidden recurring ^ref keeps ordinary visibility (Rust parity)
  ---
  duration_ms: 1.341311
  ...
# Subtest: bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
ok 2056 - bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
  ---
  duration_ms: 4.479825
  ...
# Subtest: day numbers stay calendar-local across a DST boundary
ok 2057 - day numbers stay calendar-local across a DST boundary
  ---
  duration_ms: 0.467273
  ...
# Subtest: reviewModel shares counts, meter, tooltip, and severity
ok 2058 - reviewModel shares counts, meter, tooltip, and severity
  ---
  duration_ms: 0.584115
  ...
# Subtest: memo serves warm map hits and misses use the per-row evaluator
ok 2059 - memo serves warm map hits and misses use the per-row evaluator
  ---
  duration_ms: 72.448435
  ...
# Subtest: config snapshot caches the parse and invalidates explicitly
ok 2060 - config snapshot caches the parse and invalidates explicitly
  ---
  duration_ms: 61.126314
  ...
# Subtest: review chips share the model with severity classes
ok 2061 - review chips share the model with severity classes
  ---
  duration_ms: 1.941748
  ...
# Subtest: warm lookups reuse one snapshot without re-reading config
ok 2062 - warm lookups reuse one snapshot without re-reading config
  ---
  duration_ms: 66.469037
  ...
# Subtest: same-array cache updates and Today changes rebuild the memo
ok 2063 - same-array cache updates and Today changes rebuild the memo
  ---
  duration_ms: 98.062938
  ...
# Subtest: duplicate block IDs keep each row's own classification
ok 2064 - duplicate block IDs keep each row's own classification
  ---
  duration_ms: 232.765291
  ...
# Subtest: line identity separates same-path rows without block IDs
ok 2065 - line identity separates same-path rows without block IDs
  ---
  duration_ms: 211.00094
  ...
# Subtest: interval lookup serves the cached interval with one memo acquisition
ok 2066 - interval lookup serves the cached interval with one memo acquisition
  ---
  duration_ms: 315.651808
  ...
# Subtest: SC stage config vectors normalize valid lists and isolate rejected lists
ok 2067 - SC stage config vectors normalize valid lists and isolate rejected lists
  ---
  duration_ms: 4.523448
  ...
# Subtest: CS stage queue vectors resolve tags and sort staged checklist rows
ok 2068 - CS stage queue vectors resolve tags and sort staged checklist rows
  ---
  duration_ms: 6.215418
  ...
# Subtest: stage names are rendered in footer details and counts compact before labels
ok 2069 - stage names are rendered in footer details and counts compact before labels
  ---
  duration_ms: 0.589205
  ...
# Subtest: FT1-FT6 footer details preserve tier semantics, stage color, and compact counts
ok 2070 - FT1-FT6 footer details preserve tier semantics, stage color, and compact counts
  ---
  duration_ms: 3.443536
  ...
# Subtest: invalid stage lists emit one config lint without invalidating freshness
ok 2071 - invalid stage lists emit one config lint without invalidating freshness
  ---
  duration_ms: 134.364657
  ...
# Subtest: namespace v14 exposes normalized stage config and queue fields from Tasks rows
ok 2072 - namespace v14 exposes normalized stage config and queue fields from Tasks rows
  ---
  duration_ms: 152.13362
  ...
# Subtest: S1 new through S4 overdue
ok 2073 - S1 new through S4 overdue
  ---
  duration_ms: 33.10197
  ...
# Subtest: S5 task beats note, S6 note beats config, S7 config
ok 2074 - S5 task beats note, S6 note beats config, S7 config
  ---
  duration_ms: 1.133955
  ...
# Subtest: S8 invalid overrides fall through with lints
ok 2075 - S8 invalid overrides fall through with lints
  ---
  duration_ms: 0.523519
  ...
# Subtest: S9 malformed and S10 future stamps read as new
ok 2076 - S9 malformed and S10 future stamps read as new
  ---
  duration_ms: 0.288591
  ...
# Subtest: S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
ok 2077 - S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
  ---
  duration_ms: 29.072816
  ...
# Subtest: S13 out-of-scope rows read null
ok 2078 - S13 out-of-scope rows read null
  ---
  duration_ms: 1.118576
  ...
# Subtest: S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
ok 2079 - S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
  ---
  duration_ms: 1.872125
  ...
# Subtest: S15 counts (updated): upkeep outside the lanes drives the budget
ok 2080 - S15 counts (updated): upkeep outside the lanes drives the budget
  ---
  duration_ms: 26.469154
  ...
# Subtest: config coercion keeps defaults, flags invalid, ignores unknown keys
ok 2081 - config coercion keeps defaults, flags invalid, ignores unknown keys
  ---
  duration_ms: 42.913707
  ...
# Subtest: loadFreshnessConfig reads the block with plan-style injectables
ok 2082 - loadFreshnessConfig reads the block with plan-style injectables
  ---
  duration_ms: 1.495415
  ...
# Subtest: interval precedence is task, note, config, default
ok 2083 - interval precedence is task, note, config, default
  ---
  duration_ms: 0.289884
  ...
# Subtest: intervalForLine covers every source with its Ready fallback
ok 2084 - intervalForLine covers every source with its Ready fallback
  ---
  duration_ms: 49.630513
  ...
# Subtest: project tracking stays special while reference tasks use ordinary Ready freshness
ok 2085 - project tracking stays special while reference tasks use ordinary Ready freshness
  ---
  duration_ms: 5.607608
  ...
# Subtest: reference tasks match ordinary interval precedence and lane behavior
ok 2086 - reference tasks match ordinary interval precedence and lane behavior
  ---
  duration_ms: 2.835575
  ...
# Subtest: obsolete reference interval keys are ignored and project config still validates
ok 2087 - obsolete reference interval keys are ignored and project config still validates
  ---
  duration_ms: 1.399522
  ...
# Subtest: references use ordinary keep decisions and the nine-tier queue shape
ok 2088 - references use ordinary keep decisions and the nine-tier queue shape
  ---
  duration_ms: 1.777464
  ...
# Subtest: CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
ok 2089 - CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
  ---
  duration_ms: 3.765671
  ...
# Subtest: CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
ok 2090 - CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
  ---
  duration_ms: 2.349016
  ...
# Subtest: freshness namespace v14 retains the tracker capability contract
ok 2091 - freshness namespace v14 retains the tracker capability contract
  ---
  duration_ms: 143.929162
  ...
# Subtest: UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
ok 2092 - UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
  ---
  duration_ms: 56.501282
  ...
# Subtest: UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
ok 2093 - UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
  ---
  duration_ms: 57.061142
  ...
# Subtest: UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
ok 2094 - UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
  ---
  duration_ms: 0.590718
  ...
# Subtest: UB11 scheduled wins a tie with the unblock date
ok 2095 - UB11 scheduled wins a tie with the unblock date
  ---
  duration_ms: 0.483233
  ...
# Subtest: unblocked reader takes the latest valid duplicate and reports malformed values
ok 2096 - unblocked reader takes the latest valid duplicate and reports malformed values
  ---
  duration_ms: 0.375908
  ...
# Subtest: UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
ok 2097 - UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
  ---
  duration_ms: 0.614163
  ...
# Subtest: UB14 TICKLERs with the same due date sort only by path and line
ok 2098 - UB14 TICKLERs with the same due date sort only by path and line
  ---
  duration_ms: 50.719853
  ...
# Subtest: UB15 a scheduled ^prj resurfaces in PROJECTS
ok 2099 - UB15 a scheduled ^prj resurfaces in PROJECTS
  ---
  duration_ms: 0.38767
  ...
# Subtest: calendar scan stays within an unfenced Events section
ok 2100 - calendar scan stays within an unfenced Events section
  ---
  duration_ms: 4.627827
  ...
# Subtest: calendar scan finds same-day and dated Events stamps and ignores lookalikes
ok 2101 - calendar scan finds same-day and dated Events stamps and ignores lookalikes
  ---
  duration_ms: 1.332735
  ...
# Subtest: stamp state stays fresh on change, including old, future, and dated stamps
ok 2102 - stamp state stays fresh on change, including old, future, and dated stamps
  ---
  duration_ms: 0.426093
  ...
# Subtest: event clock state distinguishes future, running, and past
ok 2103 - event clock state distinguishes future, running, and past
  ---
  duration_ms: 0.25144
  ...
# Subtest: afternoon and evening spans stay future until they start (ES1-ES10)
ok 2104 - afternoon and evening spans stay future until they start (ES1-ES10)
  ---
  duration_ms: 0.408801
  ...
# Subtest: a buffer delays past fade and lights lead-in / lead-out wings
ok 2105 - a buffer delays past fade and lights lead-in / lead-out wings
  ---
  duration_ms: 0.206254
  ...
# Subtest: calendar scan reads [buffer::] and exposes wing data
ok 2106 - calendar scan reads [buffer::] and exposes wing data
  ---
  duration_ms: 1.193459
  ...
# Subtest: Reading view inserts hatched buffer wings beside the time pill
ok 2107 - Reading view inserts hatched buffer wings beside the time pill
  ---
  duration_ms: 0.617419
  ...
# Subtest: sync-on-create gate only accepts today's canonical daily note
ok 2108 - sync-on-create gate only accepts today's canonical daily note
  ---
  duration_ms: 1.087556
  ...
# Subtest: create listener runs once for today's note after layout readiness
ok 2109 - create listener runs once for today's note after layout readiness
  ---
  duration_ms: 1.213447
  ...
# Subtest: sync-on-create waits for Templater's Pomodoros section, then stops at its deadline
ok 2110 - sync-on-create waits for Templater's Pomodoros section, then stops at its deadline
  ---
  duration_ms: 0.860162
  ...
# Subtest: pending Templater tags are found everywhere except fenced and inline code
ok 2111 - pending Templater tags are found everywhere except fenced and inline code
  ---
  duration_ms: 0.35621
  ...
# Subtest: a raw template is not ready; a rendered note is
ok 2112 - a raw template is not ready; a rendered note is
  ---
  duration_ms: 0.185244
  ...
# Subtest: the waiter settles on two identical ready reads
ok 2113 - the waiter settles on two identical ready reads
  ---
  duration_ms: 1.888797
  ...
# Subtest: the waiter restarts settle when the note changes
ok 2114 - the waiter restarts settle when the note changes
  ---
  duration_ms: 0.475148
  ...
# Subtest: gcal sync spawns with --format json
ok 2115 - gcal sync spawns with --format json
  ---
  duration_ms: 0.151169
  ...
# Subtest: gcalEventsDecodeSync accepts held and ignores unknown future fields
ok 2116 - gcalEventsDecodeSync accepts held and ignores unknown future fields
  ---
  duration_ms: 0.94223
  ...
# Subtest: waiting and held notices fire once per day
ok 2117 - waiting and held notices fire once per day
  ---
  duration_ms: 0.484144
  ...
# Subtest: calendar hook spawns sync after the wait times out and notices waiting
ok 2118 - calendar hook spawns sync after the wait times out and notices waiting
  ---
  duration_ms: 201.647829
  ...
# bob gcal sync wait timed out: today's note never settled into a rendered note with \#\# Pomodoros; spawning sync anyway
# Subtest: calendar hook notices a held sync once per day
ok 2119 - calendar hook notices a held sync once per day
  ---
  duration_ms: 119.778325
  ...
# Subtest: calendar paint teardown clears the clock refresh interval
ok 2120 - calendar paint teardown clears the clock refresh interval
  ---
  duration_ms: 0.610716
  ...
# Subtest: off-clock Live Preview paints one chip widget and no split marks
ok 2121 - off-clock Live Preview paints one chip widget and no split marks
  ---
  duration_ms: 23.485567
  ...
# Subtest: off-clock chip preserves alias spelling and case
ok 2122 - off-clock chip preserves alias spelling and case
  ---
  duration_ms: 1.439589
  ...
# Subtest: off-clock chip reveals the raw tag while the cursor is on the line
ok 2123 - off-clock chip reveals the raw tag while the cursor is on the line
  ---
  duration_ms: 0.588354
  ...
# Subtest: buffer and off-clock decorations stay sorted and disjoint
ok 2124 - buffer and off-clock decorations stay sorted and disjoint
  ---
  duration_ms: 1.049925
  ...
# Subtest: a selection-only update reuses the cached scan
ok 2125 - a selection-only update reuses the cached scan
  ---
  duration_ms: 0.766313
  ...
# Subtest: the off-clock chip DOM carries the class, marker, and title
ok 2126 - the off-clock chip DOM carries the class, marker, and title
  ---
  duration_ms: 0.239217
  ...
# Subtest: scan treats \#on as on-clock even beside an off spelling
ok 2127 - scan treats \#on as on-clock even beside an off spelling
  ---
  duration_ms: 0.253053
  ...
# Subtest: inherited off-clock Event Tasks dash the pill with a from-note tooltip
ok 2128 - inherited off-clock Event Tasks dash the pill with a from-note tooltip
  ---
  duration_ms: 3.132081
  ...
# Subtest: Live Preview dashes inherited rows and keeps \#off chips
ok 2129 - Live Preview dashes inherited rows and keeps \#off chips
  ---
  duration_ms: 6.406804
  ...
# Subtest: Reading view dashes inherited pills and tooltips \#on overrides
ok 2130 - Reading view dashes inherited pills and tooltips \#on overrides
  ---
  duration_ms: 0.606458
  ...
# Subtest: gcalEventsDecodeSync treats missing deprecations as empty
ok 2131 - gcalEventsDecodeSync treats missing deprecations as empty
  ---
  duration_ms: 0.191867
  ...
# Subtest: gcalEventsDecodeSync keeps additive deprecations[]
ok 2132 - gcalEventsDecodeSync keeps additive deprecations[]
  ---
  duration_ms: 0.438627
  ...
# Subtest: deprecation Notice fires once per day from a successful auto-sync
ok 2133 - deprecation Notice fires once per day from a successful auto-sync
  ---
  duration_ms: 0.291016
  ...
# Subtest: gmail sync-on-create gate only accepts today's canonical daily note
ok 2134 - gmail sync-on-create gate only accepts today's canonical daily note
  ---
  duration_ms: 0.339969
  ...
# Subtest: gmailEventsDecodeSync accepts schema_version 1
ok 2135 - gmailEventsDecodeSync accepts schema_version 1
  ---
  duration_ms: 0.537827
  ...
# Subtest: gmailEventsFailureKind routes exit 1 to a Notice and exit 2 / unknown subcommand to info
ok 2136 - gmailEventsFailureKind routes exit 1 to a Notice and exit 2 / unknown subcommand to info
  ---
  duration_ms: 0.463665
  ...
# Subtest: morning archive notice validates the snapshot and deduplicates by local day and note
ok 2137 - morning archive notice validates the snapshot and deduplicates by local day and note
  ---
  duration_ms: 10.485804
  ...
# Subtest: shared create listener runs gmail after gcal, and gmail when gcal is off
ok 2138 - shared create listener runs gmail after gcal, and gmail when gcal is off
  ---
  duration_ms: 24.92709
  ...
# Subtest: gmailSyncCreatedDailyNote spawns bob gmail sync with a 120s timeout
ok 2139 - gmailSyncCreatedDailyNote spawns bob gmail sync with a 120s timeout
  ---
  duration_ms: 1037.540061
  ...
# Subtest: intention subjects accept only canonical day and period notes, including ISO W53
ok 2140 - intention subjects accept only canonical day and period notes, including ISO W53
  ---
  duration_ms: 25.75414
  ...
# Subtest: frontmatter validation is strict and summary provenance follows digest parity
ok 2141 - frontmatter validation is strict and summary provenance follows digest parity
  ---
  duration_ms: 2.231721
  ...
# Subtest: summary digest matches the bob-cli golden vectors
ok 2142 - summary digest matches the bob-cli golden vectors
  ---
  duration_ms: 2.060715
  ...
# Subtest: placement skips only canonical navigation and direct-child link lines
ok 2143 - placement skips only canonical navigation and direct-child link lines
  ---
  duration_ms: 13.744897
  ...
# Subtest: Reading anchor follows canonical nav and child DOM rows, then stops at unrelated links
ok 2144 - Reading anchor follows canonical nav and child DOM rows, then stops at unrelated links
  ---
  duration_ms: 4.8389
  ...
# Subtest: missing file, heading, and block links are detected through Obsidian resolution
ok 2145 - missing file, heading, and block links are detected through Obsidian resolution
  ---
  duration_ms: 0.767936
  ...
# Subtest: only recent closed notes with intentions show missing summary and reflection bands
ok 2146 - only recent closed notes with intentions show missing summary and reflection bands
  ---
  duration_ms: 0.875652
  ...
# Subtest: parent cache updates are re-read from the vault and property ownership releases cleanly
ok 2147 - parent cache updates are re-read from the vault and property ownership releases cleanly
  ---
  duration_ms: 4.33111
  ...
# Subtest: intention host registers Reading and Live Preview once and keeps embeds out
ok 2148 - intention host registers Reading and Live Preview once and keeps embeds out
  ---
  duration_ms: 1.464947
  ...
# Subtest: decode accepts schema 1 and marks the rest unsupported
ok 2149 - decode accepts schema 1 and marks the rest unsupported
  ---
  duration_ms: 83.004884
  ...
# Subtest: parity fixture counts 5 open top-level tasks
ok 2150 - parity fixture counts 5 open top-level tasks
  ---
  duration_ms: 0.738921
  ...
# Subtest: inbox tree membership walks area notes under inbox.md
ok 2151 - inbox tree membership walks area notes under inbox.md
  ---
  duration_ms: 46.507317
  ...
# Subtest: keepInboxTreeCounts skips nested done cancelled and non-members
ok 2152 - keepInboxTreeCounts skips nested done cancelled and non-members
  ---
  duration_ms: 1.506096
  ...
# Subtest: hidden before the first read and when unconfigured
ok 2153 - hidden before the first read and when unconfigured
  ---
  duration_ms: 0.41847
  ...
# Subtest: unverified hides Keep but keeps a live inbox
ok 2154 - unverified hides Keep but keeps a live inbox
  ---
  duration_ms: 44.981896
  ...
# Subtest: fresh, stale, and signin tones
ok 2155 - fresh, stale, and signin tones
  ---
  duration_ms: 1.238144
  ...
# Subtest: each segment hides at zero and the item hides when both are empty
ok 2156 - each segment hides at zero and the item hides when both are empty
  ---
  duration_ms: 0.405565
  ...
# Subtest: old verified ok counts hide Keep until checked again
ok 2157 - old verified ok counts hide Keep until checked again
  ---
  duration_ms: 0.57089
  ...
# Subtest: unsupported hides Keep and lives only with a positive inbox count
ok 2158 - unsupported hides Keep and lives only with a positive inbox count
  ---
  duration_ms: 41.656236
  ...
# Subtest: tasks-not-ready hides the inbox even when bob's inbox.open is positive
ok 2159 - tasks-not-ready hides the inbox even when bob's inbox.open is positive
  ---
  duration_ms: 0.634531
  ...
# Subtest: tooltip and aria copy with a fixed now
ok 2160 - tooltip and aria copy with a fixed now
  ---
  duration_ms: 0.285876
  ...
# Subtest: inbox tooltip lists the tree breakdown and names the click target
ok 2161 - inbox tooltip lists the tree breakdown and names the click target
  ---
  duration_ms: 0.402689
  ...
# Subtest: paint draws Lucide icons from the obsidian setIcon export
ok 2162 - paint draws Lucide icons from the obsidian setIcon export
  ---
  duration_ms: 10.8349
  ...
# Subtest: paint hides the item when both counts are zero and restores it
ok 2163 - paint hides the item when both counts are zero and restores it
  ---
  duration_ms: 0.487401
  ...
# Subtest: paint key is stable and paint skips unchanged frames
ok 2164 - paint key is stable and paint skips unchanged frames
  ---
  duration_ms: 0.297298
  ...
# Subtest: spawn wiring uses cache-only status with the Keep decoder
ok 2165 - spawn wiring uses cache-only status with the Keep decoder
  ---
  duration_ms: 61.910232
  ...
# Subtest: gkeep command-mode tag routes to the Keep inbox refresh
ok 2166 - gkeep command-mode tag routes to the Keep inbox refresh
  ---
  duration_ms: 0.533178
  ...
# Subtest: automatic checks require attention and a deferred timer fires on input
ok 2167 - automatic checks require attention and a deferred timer fires on input
  ---
  duration_ms: 51.427635
  ...
# Subtest: status timers clamp to one minute through two hours and null cancels
ok 2168 - status timers clamp to one minute through two hours and null cancels
  ---
  duration_ms: 0.384233
  ...
# Subtest: layout schedules its first automatic check after fifteen seconds
ok 2169 - layout schedules its first automatic check after fifteen seconds
  ---
  duration_ms: 1.631125
  ...
# Subtest: focus triggers coalesce to one refresh per fifteen seconds
ok 2170 - focus triggers coalesce to one refresh per fifteen seconds
  ---
  duration_ms: 42.488984
  ...
# Subtest: unattended focus reads cached status without refreshing Keep
ok 2171 - unattended focus reads cached status without refreshing Keep
  ---
  duration_ms: 1.910568
  ...
# Subtest: unconfigured focus cache reads are throttled for ten minutes
ok 2172 - unconfigured focus cache reads are throttled for ten minutes
  ---
  duration_ms: 58.782038
  ...
# Subtest: single flight queues one request and upgrades it from cache to forced
ok 2173 - single flight queues one request and upgrades it from cache to forced
  ---
  duration_ms: 39.581363
  ...
# Subtest: forced check feedback follows the bob refresh result
ok 2174 - forced check feedback follows the bob refresh result
  ---
  duration_ms: 311.296521
  ...
# Subtest: bulb clicks route by tone and missing Command Mode gives a preview hint
ok 2175 - bulb clicks route by tone and missing Command Mode gives a preview hint
  ---
  duration_ms: 0.955304
  ...
# Subtest: context menus omit Command Mode actions when its preview API is unavailable
ok 2176 - context menus omit Command Mode actions when its preview API is unavailable
  ---
  duration_ms: 0.562955
  ...
# Subtest: turning the indicator off prevents all new automatic and forced checks
ok 2177 - turning the indicator off prevents all new automatic and forced checks
  ---
  duration_ms: 0.286437
  ...
# Subtest: keepInboxRecountNow stores the inbox-tree total and notes
ok 2178 - keepInboxRecountNow stores the inbox-tree total and notes
  ---
  duration_ms: 20.88958
  ...
# Subtest: layout-ready callbacks are not registered as disposable events
ok 2179 - layout-ready callbacks are not registered as disposable events
  ---
  duration_ms: 0.883186
  ...
# Subtest: inbox click opens the note with the most open tasks
ok 2180 - inbox click opens the note with the most open tasks
  ---
  duration_ms: 0.977417
  ...
# Subtest: context menu Open gkeep_inbox.md still opens the Keep target
ok 2181 - context menu Open gkeep_inbox.md still opens the Keep target
  ---
  duration_ms: 0.374796
  ...
# Subtest: verified transition to auth shows one sign-in notice per session
ok 2182 - verified transition to auth shows one sign-in notice per session
  ---
  duration_ms: 0.222305
  ...
# Subtest: KP1/KB7: Live Preview widget sits at the link end with side 3 and the screenshot count
ok 2183 - KP1/KB7: Live Preview widget sits at the link end with side 3 and the screenshot count
  ---
  duration_ms: 167.559997
  ...
# Subtest: KB6: a standalone project under an area renders no mark
ok 2184 - KB6: a standalone project under an area renders no mark
  ---
  duration_ms: 46.215501
  ...
# Subtest: KB2/KB3: a sibling link suppresses the mark and striking it passes the baton with one tick
ok 2185 - KB2/KB3: a sibling link suppresses the mark and striking it passes the baton with one tick
  ---
  duration_ms: 52.125237
  ...
# Subtest: viewport-only rebuilds never tick and selection alone never rebuilds
ok 2186 - viewport-only rebuilds never tick and selection alone never rebuilds
  ---
  duration_ms: 2.088629
  ...
# Subtest: KP6/toggle: off hides every mark and on restores them without touching vault text
ok 2187 - KP6/toggle: off hides every mark and on restores them without touching vault text
  ---
  duration_ms: 92.862276
  ...
# Subtest: cold Tasks memo and missing project text render nothing; a fill schedules a refresh
ok 2188 - cold Tasks memo and missing project text render nothing; a fill schedules a refresh
  ---
  duration_ms: 2.136099
  ...
# Subtest: rollover: the same day stays quiet and a new day resets baton counts
ok 2189 - rollover: the same day stays quiet and a new day resets baton counts
  ---
  duration_ms: 77.323876
  ...
# Subtest: liveness: the daily note and cached project notes refresh; strangers do not
ok 2190 - liveness: the daily note and cached project notes refresh; strangers do not
  ---
  duration_ms: 0.535583
  ...
# Subtest: setup registers the default-on command, the Live Preview extension, and the Reading processor
ok 2191 - setup registers the default-on command, the Live Preview extension, and the Reading processor
  ---
  duration_ms: 1.30403
  ...
# Subtest: KP3/KP4: Reading inserts the host after 🔓/mail/🔑 and before the off chip
ok 2192 - KP3/KP4: Reading inserts the host after 🔓/mail/🔑 and before the off chip
  ---
  duration_ms: 28.892462
  ...
# Subtest: Reading removes stale hosts when the link loses eligibility
ok 2193 - Reading removes stale hosts when the link loses eligibility
  ---
  duration_ms: 31.068497
  ...
# Subtest: off-clock Reading insertion steps past the ⏭ host so the off chip stays last
ok 2194 - off-clock Reading insertion steps past the ⏭ host so the off chip stays last
  ---
  duration_ms: 34.75678
  ...
# Subtest: progress context and the off-clock chip recognize the ⏭ host as a ledger mark
ok 2195 - progress context and the off-clock chip recognize the ⏭ host as a ledger mark
  ---
  duration_ms: 31.068688
  ...
# Subtest: 200-link / 50-target Live Preview build memoizes targets under the 250 ms CPU-work budget
ok 2196 - 200-link / 50-target Live Preview build memoizes targets under the 250 ms CPU-work budget
  ---
  duration_ms: 8501.601866
  ...
# 200-link build took 70.79 ms CPU (best of 7: 116.23, 200.54, 85.59, 70.79, 89.53, 85.13, 108.91 ms CPU; wall best 194.84 ms of 953.98, 365.53, 625.70, 194.84, 619.67, 1138.67, 933.55 ms; budget 250 ms; clock process.cpuUsage; load 100.1/27.4/14.0 on 64 cpus)
# Subtest: KB1/KB7/KB8: mixed lane order and exact count
ok 2197 - KB1/KB7/KB8: mixed lane order and exact count
  ---
  duration_ms: 231.384854
  ...
# Subtest: KB2–KB6/KB9/KB10: live-link, root, folds, and final-close gates
ok 2198 - KB2–KB6/KB9/KB10: live-link, root, folds, and final-close gates
  ---
  duration_ms: 18.935128
  ...
# Subtest: KB11–KB15/KB19/KB20/KB23: post-close blockers and uncertainty
ok 2199 - KB11–KB15/KB19/KB20/KB23: post-close blockers and uncertainty
  ---
  duration_ms: 5.610063
  ...
# Subtest: KB16–KB22: duplicate marks, reference rows, residency, and candidate gates
ok 2200 - KB16–KB22: duplicate marks, reference rows, residency, and candidate gates
  ---
  duration_ms: 5.518608
  ...
# Subtest: LP1–LP17: the root-parent rule matches the documented vectors
ok 2201 - LP1–LP17: the root-parent rule matches the documented vectors
  ---
  duration_ms: 4.059211
  ...
# Subtest: KT1–KT8: tooltip, accessible element, config cache, and bounded counting
ok 2202 - KT1–KT8: tooltip, accessible element, config cache, and bounded counting
  ---
  duration_ms: 616.493655
  ...
# Subtest: keep-moving widget positions the caret and opens its project from a modifier click
ok 2203 - keep-moving widget positions the caret and opens its project from a modifier click
  ---
  duration_ms: 2.945264
  ...
# Subtest: membership: pending/next/ready in, exclusions counted, today dropped
ok 2204 - membership: pending/next/ready in, exclusions counted, today dropped
  ---
  duration_ms: 6.523678
  ...
# Subtest: membership: review-bucket Ready tasks are excluded and counted as reviewReady
ok 2205 - membership: review-bucket Ready tasks are excluded and counted as reviewReady
  ---
  duration_ms: 0.472021
  ...
# Subtest: parity: pending/next match the dash section; ready matches readyCountFromTasks
ok 2206 - parity: pending/next match the dash section; ready matches readyCountFromTasks
  ---
  duration_ms: 7.133532
  ...
# Subtest: order: pending, then next, then ready, path then line inside each lane
ok 2207 - order: pending, then next, then ready, path then line inside each lane
  ---
  duration_ms: 0.587171
  ...
# Subtest: ranks: rank/total plus per-lane laneRank/laneTotal
ok 2208 - ranks: rank/total plus per-lane laneRank/laneTotal
  ---
  duration_ms: 0.632878
  ...
# Subtest: identity: keys match freshnessRowKey
ok 2209 - identity: keys match freshnessRowKey
  ---
  duration_ms: 0.481149
  ...
# Subtest: unavailable: throwing isToday propagates to the caller
ok 2210 - unavailable: throwing isToday propagates to the caller
  ---
  duration_ms: 0.399533
  ...
# Subtest: mixin: memo hits and invalidates; version 2; ready matches the chip
ok 2211 - mixin: memo hits and invalidates; version 2; ready matches the chip
  ---
  duration_ms: 8.977824
  ...
# Subtest: mixin: unavailable reasons for tasks, today, and error
ok 2212 - mixin: unavailable reasons for tasks, today, and error
  ---
  duration_ms: 0.618221
  ...
# Subtest: shape: the result and its entries are frozen
ok 2213 - shape: the result and its entries are frozen
  ---
  duration_ms: 0.65956
  ...
# Subtest: api.logs validates the schema and catalog shape
ok 2214 - api.logs validates the schema and catalog shape
  ---
  duration_ms: 1.72248
  ...
# Subtest: api.logs fetch is single-flight and returns a stale snapshot while it revalidates
ok 2215 - api.logs fetch is single-flight and returns a stale snapshot while it revalidates
  ---
  duration_ms: 1.671291
  ...
# Subtest: api.logs snapshot merges a capped, idempotent session overlay without changing catalog counts
ok 2216 - api.logs snapshot merges a capped, idempotent session overlay without changing catalog counts
  ---
  duration_ms: 170.454764
  ...
# Subtest: api.logs reports mobile and remembers an unsupported bob path until reload
ok 2217 - api.logs reports mobile and remembers an unsupported bob path until reload
  ---
  duration_ms: 0.741366
  ...
# Subtest: ML1–ML6, ML9: reply badge model vectors pass verbatim
ok 2218 - ML1–ML6, ML9: reply badge model vectors pass verbatim
  ---
  duration_ms: 3.391005
  ...
# Subtest: ML7 and ML10: no mail link and inline-code wikilinks produce no tokens
ok 2219 - ML7 and ML10: no mail link and inline-code wikilinks produce no tokens
  ---
  duration_ms: 1.342684
  ...
# Subtest: mailNoteFactsFromFrontmatter accepts type:[[mail]] or gmail_thread_id
ok 2220 - mailNoteFactsFromFrontmatter accepts type:[[mail]] or gmail_thread_id
  ---
  duration_ms: 0.457954
  ...
# Subtest: reply badge host is listener-free with no title
ok 2221 - reply badge host is listener-free with no title
  ---
  duration_ms: 0.294172
  ...
# Subtest: ML1 Live Preview widget sits after the closing ]]
ok 2222 - ML1 Live Preview widget sits after the closing ]]
  ---
  duration_ms: 1.401416
  ...
# Subtest: ML8: toggle off yields no decorations
ok 2223 - ML8: toggle off yields no decorations
  ---
  duration_ms: 0.181036
  ...
# Subtest: toggle-mail-link-marks flips the gate and Notice
ok 2224 - toggle-mail-link-marks flips the gate and Notice
  ---
  duration_ms: 0.416846
  ...
# Subtest: styles.css contract: muted badge, no pill, toggle hide
ok 2225 - styles.css contract: muted badge, no pill, toggle hide
  ---
  duration_ms: 2.114498
  ...
# Subtest: AR1–AR7, AR10–AR11: archive chip is closed-task and identity gated
ok 2226 - AR1–AR7, AR10–AR11: archive chip is closed-task and identity gated
  ---
  duration_ms: 3.747737
  ...
# Subtest: AR12–AR15: tooltip preserves receipt counts and treats labels as text
ok 2227 - AR12–AR15: tooltip preserves receipt counts and treats labels as text
  ---
  duration_ms: 0.733601
  ...
# Subtest: archive list cache validates identity, coalesces reads, and invalidates
ok 2228 - archive list cache validates identity, coalesces reads, and invalidates
  ---
  duration_ms: 0.904467
  ...
# Subtest: closed task targets resolve same-line and direct link-only child mail notes only
ok 2229 - closed task targets resolve same-line and direct link-only child mail notes only
  ---
  duration_ms: 0.959162
  ...
# Subtest: AR Live Preview adds one display-only widget after a closed task line
ok 2230 - AR Live Preview adds one display-only widget after a closed task line
  ---
  duration_ms: 0.541003
  ...
# Subtest: AR Reading view paints each receipt chip under its closed task row
ok 2231 - AR Reading view paints each receipt chip under its closed task row
  ---
  duration_ms: 1.144115
  ...
# Subtest: shared vector: back-to-back-worked-run
ok 2232 - shared vector: back-to-back-worked-run
  ---
  duration_ms: 142.952207
  ...
# Subtest: shared vector: off-clock-event-stamps-key
ok 2233 - shared vector: off-clock-event-stamps-key
  ---
  duration_ms: 1.19941
  ...
# Subtest: shared vector: off-clock-run-breaks-at-worked-event
ok 2234 - shared vector: off-clock-run-breaks-at-worked-event
  ---
  duration_ms: 17.292731
  ...
# Subtest: shared vector: worked-run-breaks-at-off-clock-event
ok 2235 - shared vector: worked-run-breaks-at-off-clock-event
  ---
  duration_ms: 0.728361
  ...
# Subtest: shared vector: overlapping-events-share-a-run
ok 2236 - shared vector: overlapping-events-share-a-run
  ---
  duration_ms: 0.706259
  ...
# Subtest: shared vector: late-join-clamps-to-closed-session
ok 2237 - shared vector: late-join-clamps-to-closed-session
  ---
  duration_ms: 0.708153
  ...
# Subtest: shared vector: running-event-starts-at-its-own-start
ok 2238 - shared vector: running-event-starts-at-its-own-start
  ---
  duration_ms: 20.80055
  ...
# Subtest: shared vector: early-start-writes-future-start
ok 2239 - shared vector: early-start-writes-future-start
  ---
  duration_ms: 0.992946
  ...
# Subtest: shared vector: far-run-warns-with-escape-hatch
ok 2240 - shared vector: far-run-warns-with-escape-hatch
  ---
  duration_ms: 0.998727
  ...
# Subtest: shared vector: ended-done-and-cancelled-events-are-skipped
ok 2241 - shared vector: ended-done-and-cancelled-events-are-skipped
  ---
  duration_ms: 0.987476
  ...
# Subtest: shared vector: no-lineup-events-keeps-the-default-pomodoro
ok 2242 - shared vector: no-lineup-events-keeps-the-default-pomodoro
  ---
  duration_ms: 25.850632
  ...
# Subtest: shared vector: counted-suffix-keeps-clock-classification
ok 2243 - shared vector: counted-suffix-keeps-clock-classification
  ---
  duration_ms: 0.517418
  ...
# Subtest: shared vector: restart-rederives-the-run
ok 2244 - shared vector: restart-rederives-the-run
  ---
  duration_ms: 0.377741
  ...
# Subtest: shared vector (capture-only): drop-removes-an-event-from-the-run
ok 2245 - shared vector (capture-only): drop-removes-an-event-from-the-run
  ---
  duration_ms: 0.128275
  ...
# Subtest: shared vector (capture-only): kept-swap-into-off-clock-meet-moves-key
ok 2246 - shared vector (capture-only): kept-swap-into-off-clock-meet-moves-key
  ---
  duration_ms: 0.089862
  ...
# Subtest: shared vector (capture-only): kept-swap-out-of-off-clock-meet-restores-worked-key
ok 2247 - shared vector (capture-only): kept-swap-out-of-off-clock-meet-restores-worked-key
  ---
  duration_ms: 0.088198
  ...
# Subtest: shared vector: named-meet-start-uses-the-run
ok 2248 - shared vector: named-meet-start-uses-the-run
  ---
  duration_ms: 0.262381
  ...
# Subtest: shared vector: non-meet-lineup-follows-counted-links
ok 2249 - shared vector: non-meet-lineup-follows-counted-links
  ---
  duration_ms: 34.982903
  ...
# Subtest: shared vector: pre-buffer-starts-the-run-early
ok 2250 - shared vector: pre-buffer-starts-the-run-early
  ---
  duration_ms: 0.9844
  ...
# Subtest: shared vector: post-buffer-bridges-to-the-next-event
ok 2251 - shared vector: post-buffer-bridges-to-the-next-event
  ---
  duration_ms: 0.428519
  ...
# Subtest: shared vector: buffer-never-bridges-trackedness
ok 2252 - shared vector: buffer-never-bridges-trackedness
  ---
  duration_ms: 0.911481
  ...
# Subtest: shared vector: now-inside-a-lead-out-keeps-the-run
ok 2253 - shared vector: now-inside-a-lead-out-keeps-the-run
  ---
  duration_ms: 0.31965
  ...
# Subtest: shared vector: buffered-far-run-warns-from-the-buffered-start
ok 2254 - shared vector: buffered-far-run-warns-from-the-buffered-start
  ---
  duration_ms: 24.990732
  ...
# Subtest: shared vector: inherited-root-event-is-off-clock
ok 2255 - shared vector: inherited-root-event-is-off-clock
  ---
  duration_ms: 2.178259
  ...
# Subtest: shared vector: signed-later-unnamed-reaches-meet
ok 2256 - shared vector: signed-later-unnamed-reaches-meet
  ---
  duration_ms: 0.2879
  ...
# Subtest: shared vector: signed-later-named-meet-is-explicit
ok 2257 - shared vector: signed-later-named-meet-is-explicit
  ---
  duration_ms: 0.232233
  ...
# Subtest: shared vector: signed-later-fit-draft-keeps-plus
ok 2258 - shared vector: signed-later-fit-draft-keeps-plus
  ---
  duration_ms: 0.738921
  ...
# Subtest: every vector is either mirrored or listed as capture-only
ok 2259 - every vector is either mirrored or listed as capture-only
  ---
  duration_ms: 0.167931
  ...
# Subtest: off-clock tag detection mirrors bob's Rust rules for every spelling
ok 2260 - off-clock tag detection mirrors bob's Rust rules for every spelling
  ---
  duration_ms: 0.598042
  ...
# Subtest: clean titles strip every off-clock spelling and its sentence punctuation
ok 2261 - clean titles strip every off-clock spelling and its sentence punctuation
  ---
  duration_ms: 0.290585
  ...
# Subtest: Event rows carry status, clock, ids, and clean titles
ok 2262 - Event rows carry status, clock, ids, and clean titles
  ---
  duration_ms: 0.426464
  ...
# Subtest: N\\p and N\\P keep the row's key; a bare span is stamped [off::]; a conflict resolves to [t::]
ok 2263 - N\\p and N\\P keep the row's key; a bare span is stamped [off::]; a conflict resolves to [t::]
  ---
  duration_ms: 62.311157
  ...
# Subtest: N\\o and N\\O keep every key and field byte-for-byte
ok 2264 - N\\o and N\\O keep every key and field byte-for-byte
  ---
  duration_ms: 0.290825
  ...
# Subtest: pomodoroSessionClock reads all five row shapes like Rust session_clock
ok 2265 - pomodoroSessionClock reads all five row shapes like Rust session_clock
  ---
  duration_ms: 0.616127
  ...
# Subtest: setPomodoroLineClock moves the recorded minutes between keys like Rust set_ledger_clock
ok 2266 - setPomodoroLineClock moves the recorded minutes between keys like Rust set_ledger_clock
  ---
  duration_ms: 0.485678
  ...
# Subtest: a non-MEET se<X> start warns when it newly crosses an open event
ok 2267 - a non-MEET se<X> start warns when it newly crosses an open event
  ---
  duration_ms: 49.489774
  ...
# Subtest: a counted start that fits ends before the event and stays silent
ok 2268 - a counted start that fits ends before the event and stays silent
  ---
  duration_ms: 0.691881
  ...
# Subtest: a start with no fitting count omits the fit draft
ok 2269 - a start with no fitting count omits the fit draft
  ---
  duration_ms: 0.580479
  ...
# Subtest: MEET sessions, own-lineup events, and done events never warn
ok 2270 - MEET sessions, own-lineup events, and done events never warn
  ---
  duration_ms: 0.562875
  ...
# Subtest: \\p and \\o warn on new crossings only; \\P never warns
ok 2271 - \\p and \\o warn on new crossings only; \\P never warns
  ---
  duration_ms: 0.745824
  ...
# Subtest: event_buffer row vectors: parse, buffered span, clean title, field, label
ok 2272 - event_buffer row vectors: parse, buffered span, clean title, field, label
  ---
  duration_ms: 1.5657
  ...
# Subtest: event_buffer conflict vectors: shared predicate
ok 2273 - event_buffer conflict vectors: shared predicate
  ---
  duration_ms: 1.232714
  ...
# Subtest: event_buffer description vectors stay bob-cli's HTML reader
ok 2274 - event_buffer description vectors stay bob-cli's HTML reader
  ---
  duration_ms: 60.344733
  ...
# Subtest: a buffered se<X> start warns into the lead-in and fits at the buffered start
ok 2275 - a buffered se<X> start warns into the lead-in and fits at the buffered start
  ---
  duration_ms: 0.885951
  ...
# Subtest: a start that runs through the meeting names the event plus its buffer label
ok 2276 - a start that runs through the meeting names the event plus its buffer label
  ---
  duration_ms: 0.36628
  ...
# Subtest: a lead-out start names the after buffer and offers no fit
ok 2277 - a lead-out start names the after buffer and offers no fit
  ---
  duration_ms: 0.352734
  ...
# Subtest: an Event Task with a typed off-clock tag is painted by the Event scan
ok 2278 - an Event Task with a typed off-clock tag is painted by the Event scan
  ---
  duration_ms: 1.503871
  ...
# Subtest: an off-clock session's home chip is dashed, shows its minutes, and says so
ok 2279 - an off-clock session's home chip is dashed, shows its minutes, and says so
  ---
  duration_ms: 72.775841
  ...
# Subtest: Reading view marks the off-clock tag link and dashes the row's time pill
ok 2280 - Reading view marks the off-clock tag link and dashes the row's time pill
  ---
  duration_ms: 0.705156
  ...
# Subtest: Reading view marks every off-clock tag spelling and nothing else
ok 2281 - Reading view marks every off-clock tag spelling and nothing else
  ---
  duration_ms: 0.469015
  ...
# Subtest: an active-note Pomodoro target still jumps and centers immediately
ok 2282 - an active-note Pomodoro target still jumps and centers immediately
  ---
  duration_ms: 1014.712309
  ...
# Subtest: Ctrl+9 from an unpinned daily copy switches to the pinned home tab
ok 2283 - Ctrl+9 from an unpinned daily copy switches to the pinned home tab
  ---
  duration_ms: 865.10763
  ...
# Subtest: Ctrl+9 on the pinned daily tab jumps in place when a copy exists
ok 2284 - Ctrl+9 on the pinned daily tab jumps in place when a copy exists
  ---
  duration_ms: 151.347439
  ...
# Subtest: Ctrl+9 switches daily copies without a Pomodoros section and stays quiet
ok 2285 - Ctrl+9 switches daily copies without a Pomodoros section and stays quiet
  ---
  duration_ms: 174.118039
  ...
# Subtest: Ctrl+9 keeps the active daily tab when equal-ranked copies exist
ok 2286 - Ctrl+9 keeps the active daily tab when equal-ranked copies exist
  ---
  duration_ms: 164.341521
  ...
# Subtest: Ctrl+9 from a sidebar daily copy switches to a main-area home tab
ok 2287 - Ctrl+9 from a sidebar daily copy switches to a main-area home tab
  ---
  duration_ms: 363.785633
  ...
# Subtest: the first fallback press only opens daily and the second press jumps
ok 2288 - the first fallback press only opens daily and the second press jumps
  ---
  duration_ms: 861.394831
  ...
# Subtest: a daily note with no target defers its notice until the second press
ok 2289 - a daily note with no target defers its notice until the second press
  ---
  duration_ms: 155.801092
  ...
# Subtest: an already-open daily leaf retains its live cursor and viewport
ok 2290 - an already-open daily leaf retains its live cursor and viewport
  ---
  duration_ms: 1703.400526
  ...
# Subtest: a second press after reused-leaf fallback performs the Pomodoro jump
ok 2291 - a second press after reused-leaf fallback performs the Pomodoro jump
  ---
  duration_ms: 568.901846
  ...
# Subtest: the standalone daily-note command activates a reused daily leaf
ok 2292 - the standalone daily-note command activates a reused daily leaf
  ---
  duration_ms: 576.993236
  ...
# Subtest: Ctrl+9 loads and reuses a deferred pinned daily tab before falling back
ok 2293 - Ctrl+9 loads and reuses a deferred pinned daily tab before falling back
  ---
  duration_ms: 299.384976
  ...
# Subtest: pinned daily tabs win over earlier unpinned tabs
ok 2294 - pinned daily tabs win over earlier unpinned tabs
  ---
  duration_ms: 464.882002
  ...
# Subtest: a deferred sidebar daily tab is reused only without a main-area match
ok 2295 - a deferred sidebar daily tab is reused only without a main-area match
  ---
  duration_ms: 371.805558
  ...
# Subtest: a deferred sidebar daily tab is reused when there is no main-area match
ok 2296 - a deferred sidebar daily tab is reused when there is no main-area match
  ---
  duration_ms: 251.662406
  ...
# Subtest: a deferred non-Markdown daily path is ignored and uses the daily-note fallback
ok 2297 - a deferred non-Markdown daily path is ignored and uses the daily-note fallback
  ---
  duration_ms: 203.658208
  ...
# Subtest: the standalone daily-note command reuses a deferred pinned tab
ok 2298 - the standalone daily-note command reuses a deferred pinned tab
  ---
  duration_ms: 194.109354
  ...
# Subtest: Ctrl+9 opens the pinned daily tab from a non-Markdown active leaf
ok 2299 - Ctrl+9 opens the pinned daily tab from a non-Markdown active leaf
  ---
  duration_ms: 313.875466
  ...
# Subtest: a closed then reopened daily note restores its in-session location
ok 2300 - a closed then reopened daily note restores its in-session location
  ---
  duration_ms: 333.093635
  ...
# Subtest: different-path and invalid locations do not leak into a daily note
ok 2301 - different-path and invalid locations do not leak into a daily note
  ---
  duration_ms: 394.624783
  ...
# Subtest: out-of-range remembered coordinates are clamped safely
ok 2302 - out-of-range remembered coordinates are clamped safely
  ---
  duration_ms: 263.103393
  ...
# Subtest: a rapid second press cancels an older fallback restore
ok 2303 - a rapid second press cancels an older fallback restore
  ---
  duration_ms: 271.172752
  ...
# Subtest: navigation and unload clean up daily scroll listeners and deferred work
ok 2304 - navigation and unload clean up daily scroll listeners and deferred work
  ---
  duration_ms: 219.869154
  ...
# Subtest: NR1–NR7: no-reply pill model vectors pass verbatim
ok 2305 - NR1–NR7: no-reply pill model vectors pass verbatim
  ---
  duration_ms: 3.470417
  ...
# Subtest: no-reply pill replaces the exact \#awaiting_reply span
ok 2306 - no-reply pill replaces the exact \#awaiting_reply span
  ---
  duration_ms: 0.776954
  ...
# Subtest: NR1 Live Preview replace widget covers the tag; NR8 toggle off is empty
ok 2307 - NR1 Live Preview replace widget covers the tag; NR8 toggle off is empty
  ---
  duration_ms: 0.787925
  ...
# Subtest: Tasks query rows keep the native \#awaiting_reply pill
ok 2308 - Tasks query rows keep the native \#awaiting_reply pill
  ---
  duration_ms: 0.362732
  ...
# Subtest: styles.css contract: muted capsule under task-tag-marks
ok 2309 - styles.css contract: muted capsule under task-tag-marks
  ---
  duration_ms: 2.658826
  ...
# Subtest: crowded chip: over count is red with tooltip, aria, and names
ok 2310 - crowded chip: over count is red with tooltip, aria, and names
  ---
  duration_ms: 1.725845
  ...
# Subtest: crowded chip: calm zero and unavailable dash
ok 2311 - crowded chip: calm zero and unavailable dash
  ---
  duration_ms: 0.290635
  ...
# Subtest: crowded chip: names at most five notes
ok 2312 - crowded chip: names at most five notes
  ---
  duration_ms: 0.312386
  ...
# Subtest: crowded chip: classes, text, aria, and arrow
ok 2313 - crowded chip: classes, text, aria, and arrow
  ---
  duration_ms: 2.145998
  ...
# Subtest: crowded chip: refresh in place keeps the anchor, unload drops it
ok 2314 - crowded chip: refresh in place keeps the anchor, unload drops it
  ---
  duration_ms: 0.828752
  ...
# Subtest: anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
ok 2315 - anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
  ---
  duration_ms: 0.753829
  ...
# Subtest: ready-notes summary: crowded, calm, and unavailable
ok 2316 - ready-notes summary: crowded, calm, and unavailable
  ---
  duration_ms: 0.338256
  ...
# Subtest: ready-notes bar: cap tick and red overflow within 30 cells
ok 2317 - ready-notes bar: cap tick and red overflow within 30 cells
  ---
  duration_ms: 0.272511
  ...
# Subtest: ready-notes block: model and render with grid, pills, and footer
ok 2318 - ready-notes block: model and render with grid, pills, and footer
  ---
  duration_ms: 1.938652
  ...
# Subtest: ready-notes block: unavailable renders a dash line
ok 2319 - ready-notes block: unavailable renders a dash line
  ---
  duration_ms: 0.597611
  ...
# Subtest: heading matcher: fences, level, case, and first-only
ok 2320 - heading matcher: fences, level, case, and first-only
  ---
  duration_ms: 0.509133
  ...
# Subtest: heading chip copy: room, full, crowded, exempt, unavailable
ok 2321 - heading chip copy: room, full, crowded, exempt, unavailable
  ---
  duration_ms: 0.48698
  ...
# Subtest: heading chip key is stable for equal models
ok 2322 - heading chip key is stable for equal models
  ---
  duration_ms: 0.216714
  ...
# Subtest: reading view: appends the chip to the matching h2 only
ok 2323 - reading view: appends the chip to the matching h2 only
  ---
  duration_ms: 1.802051
  ...
# Subtest: reading view: no chip for ineligible notes
ok 2324 - reading view: no chip for ineligible notes
  ---
  duration_ms: 0.160787
  ...
# Subtest: one live-refresh fan-out reaches every family
ok 2325 - one live-refresh fan-out reaches every family
  ---
  duration_ms: 2.086885
  ...
# Subtest: ledger-tools CSS is theme-safe for the new views
ok 2326 - ledger-tools CSS is theme-safe for the new views
  ---
  duration_ms: 2.22032
  ...

