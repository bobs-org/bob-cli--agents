# Chat History - ace-run (bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.1--mon-1)

- **TIMESTAMP:** 2026-10-26 13:52:55 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.1--mon-1

## Prompt

sase monitor start --command 'set +e\nfailures=\nrun_gate() {\n  gate_name=$1\n  shift\n  printf "\\n=== %s ===\\n" "$gate_name"\n  "$@"\n  gate_rc=$?\n  printf "\\n=== EXIT %s: %s ===\\n" "$gate_name" "$gate_rc"\n  if [ "$gate_rc" -ne 0 ]; then\n    failures="${failures}${failures:+,}${gate_name}:${gate_rc}"\n  fi\n}\nrun_gate "just check" just check\nrun_gate "just docs-check" just docs-check\nrun_gate "bob-plugins build" sh -c "cd /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins && npm run build"\nrun_gate "bob-plugins test" sh -c "cd /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins && npm test"\nrun_gate "bob-plugins validate" sh -c "cd /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins && npm run validate"\nrun_gate "bob-plugins docs:check" sh -c "cd /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins && npm run docs:check"\nprintf "\\nFAILED GATES: %s\\n" "$failures"\n[ -z "$failures" ]' --reason 'Run the approved phase verification gates: just check, docs check, and all bob-plugins gates'

## Response

sase tool run 03a85925558162c89b9a8d959c29763a

=== just check ===

✅  CHECK
────────────────────────────────────────────────
cargo fmt --check
Diff in /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/src/native/freshness/placement_tests.rs:292:
             stamp_fresh_preserve_keeps(line, day()),
         ];
         for stamped in operations {
[31m-            assert_eq!(stamped.line, line, "ledger row must stay byte-exact: {line:?}");
[m[31m-            assert!(!stamped.changed, "ledger row must not be changed: {line:?}");
[m[32m+            assert_eq!(
[m[32m+                stamped.line, line,
[m[32m+                "ledger row must stay byte-exact: {line:?}"
[m[32m+            );
[m[32m+            assert!(
[m[32m+                !stamped.changed,
[m[32m+                "ledger row must not be changed: {line:?}"
[m[32m+            );
[m             assert_eq!(stamped.refused, Some(Refusal::NotTask), "{line:?}");
         }
     }
error: recipe `check` failed on line 26 with exit code 1

=== EXIT just check: 1 ===

=== just docs-check ===

✅  DOCS CHECK
────────────────────────────────────────────────
uv run --project tools/docs bob-docs check
docs-check: assemble and validate source context

docs-check: lint
src/native/highlights_ref/source_store.rs:185: environment: undocumented production environment name BOB_TEST_FIXTURE_PDF; document it in docs/reference/configuration.md or add a reasoned exact exception
bob-docs lint: 1 error(s)
docs-check: FAILED (lint, exit 1)
error: recipe `docs-check` failed on line 208 with exit code 1

=== EXIT just docs-check: 1 ===

=== bob-plugins build ===

> bob-plugins@0.1.0 build
> node scripts/build-plugins.mjs

  unchanged block-id-prompt
  unchanged bob-articles
  unchanged bob-command-mode
  unchanged bob-ledger-tools
  unchanged bob-navigation-hotkeys
  unchanged task-status-cycler

=== EXIT bob-plugins build: 0 ===

=== bob-plugins test ===

> bob-plugins@0.1.0 test
> node scripts/build-plugins.mjs --check && npm run docs:inventory:check && node --test scripts/test-project-tasks-snapshot.cjs scripts/test-bob-articles.cjs scripts/test-command-mode-resolver-env.cjs scripts/test-command-mode-catalog.cjs scripts/test-command-mode-runner.cjs scripts/test-command-mode-outcomes-api.cjs scripts/test-command-mode-pager.cjs scripts/test-dependency-line-migration.cjs scripts/test-navigation-hotkeys-section-nav.cjs scripts/test-navigation-hotkeys-rename.cjs scripts/test-navigation-hotkeys-ref-pdf.cjs scripts/test-navigation-hotkeys-templater-trigger.cjs scripts/test-navigation-hotkeys-schedule-recovery.cjs scripts/test-navigation-hotkeys-schedule-properties.cjs scripts/test-navigation-hotkeys-schedule-writes.cjs scripts/test-navigation-hotkeys-runtime-schedule.cjs scripts/test-navigation-hotkeys-dependencies.cjs scripts/test-navigation-blocks-guards.cjs scripts/test-navigation-blocks-writers.cjs scripts/test-navigation-blocks-edit.cjs scripts/test-navigation-blocks-stage-view.cjs scripts/test-navigation-hotkeys-dependency-mirror.cjs scripts/test-navigation-hotkeys-task-move-plan.cjs scripts/test-navigation-hotkeys-priority-notice.cjs scripts/test-navigation-successor-picker.cjs scripts/test-navigation-image-zoom-viewer.cjs scripts/test-navigation-hotkeys-unblocked-notice.cjs scripts/test-navigation-project-blocking.cjs scripts/test-navigation-project-dependency-stage.cjs scripts/test-navigation-project-subprojects.cjs scripts/test-navigation-project-subtree-gestures.cjs scripts/test-navigation-hotkeys-priority-picker.cjs scripts/test-navigation-hotkeys-picker-lifecycle.cjs scripts/test-navigation-hotkeys-ref-picker-text.cjs scripts/test-navigation-hotkeys-pomodoro-move-pickers.cjs scripts/test-navigation-inbox-route.cjs scripts/test-navigation-inbox-route-card.cjs scripts/test-navigation-hotkeys-task-move.cjs scripts/test-navigation-open-notes-uri.cjs scripts/test-navigation-hotkeys-dash-open.cjs scripts/test-navigation-goto-task-uri.cjs scripts/test-navigation-hotkeys-open-task-jump.cjs scripts/test-navigation-hotkeys-vim-counts.cjs scripts/test-navigation-hotkeys-tab-pin.cjs scripts/test-navigation-hotkeys-schedule-log.cjs scripts/test-navigation-hotkeys-schedule-review.cjs scripts/test-navigation-hotkeys-deferred-pomodoro.cjs scripts/test-navigation-hotkeys-pomodoro-parse.cjs scripts/test-navigation-hotkeys-pomodoro-bullet-move.cjs scripts/test-navigation-hotkeys-pomodoro-split-rename.cjs scripts/test-navigation-hotkeys-pomodoro-themes-manager.cjs scripts/test-navigation-hotkeys-pomodoro-reorder.cjs scripts/test-navigation-hotkeys-runtime-prune.cjs scripts/test-navigation-hotkeys-project-from-task.cjs scripts/test-navigation-hotkeys-project-reversal.cjs scripts/test-navigation-hotkeys-link-picker.cjs scripts/test-navigation-hotkeys-lane-toggle.cjs scripts/test-navigation-hotkeys-task-link-lane.cjs scripts/test-navigation-hotkeys-cancel-log.cjs scripts/test-navigation-hotkeys-cancel-task.cjs scripts/test-navigation-hotkeys-forward-promotion.cjs scripts/test-navigation-hotkeys-schedule-work-log.cjs scripts/test-navigation-hotkeys-task-move-history.cjs scripts/test-navigation-jump-history.cjs scripts/test-navigation-dependencies.cjs scripts/test-navigation-editor-line-diff.cjs scripts/test-navigation-quick-roll.cjs scripts/test-navigation-quick-roll-preview.cjs scripts/test-navigation-roll-decay.cjs scripts/test-navigation-decay-planner.cjs scripts/test-navigation-task-card-model.cjs scripts/test-navigation-task-card-view.cjs scripts/test-navigation-task-card-schedule.cjs scripts/test-navigation-task-card-review.cjs scripts/test-navigation-decision-card.cjs scripts/test-navigation-decision-card-handlers.cjs scripts/test-navigation-decision-card-keep.cjs scripts/test-navigation-refresh-modal.cjs scripts/test-navigation-freshness.cjs scripts/test-navigation-stamps.cjs scripts/test-navigation-keep-counting.cjs scripts/test-navigation-rotten-keep.cjs scripts/test-navigation-rotten-log.cjs scripts/test-navigation-checklist.cjs scripts/test-navigation-review-advance.cjs scripts/test-navigation-review-advance-gestures.cjs scripts/test-navigation-checklist-ctrl-enter.cjs scripts/test-ledger-tools-navigation.cjs scripts/test-ledger-tools-plan-budget.cjs scripts/test-ledger-tools-ready-badge.cjs scripts/test-ledger-tools-note-ready.cjs scripts/test-ledger-tools-note-ready-views.cjs scripts/test-ledger-tools-dashboard-parity.cjs scripts/test-ledger-tools-work-badge-tone.cjs scripts/test-ledger-tools-dashboard-collections.cjs scripts/test-ledger-tools-today.cjs scripts/test-ledger-tools-freshness-placement.cjs scripts/test-ledger-tools-freshness-states.cjs scripts/test-ledger-tools-freshness-namespace.cjs scripts/test-ledger-tools-freshness-review-model.cjs scripts/test-ledger-tools-freshness-queue.cjs scripts/test-ledger-tools-freshness-tracking.cjs scripts/test-ledger-tools-freshness-footer.cjs scripts/test-ledger-tools-freshness-recurring.cjs scripts/test-ledger-tools-freshness-mark.cjs scripts/test-ledger-tools-freshness-mark-surfaces.cjs scripts/test-ledger-tools-priority-marks.cjs scripts/test-ledger-tools-task-tag-marks.cjs scripts/test-ledger-tools-today-marks.cjs scripts/test-ledger-tools-today-marks-reading.cjs scripts/test-ledger-tools-unblocked-glyph.cjs scripts/test-ledger-tools-progress-marks.cjs scripts/test-ledger-tools-date-marks.cjs scripts/test-ledger-tools-recurrence-marks.cjs scripts/test-ledger-tools-date-marks-tasks.cjs scripts/test-ledger-tools-freshness-keeps.cjs scripts/test-ledger-tools-freshness-unblocked.cjs scripts/test-ledger-tools-freshness-decision-card.cjs scripts/test-ledger-tools-dependency-chips.cjs scripts/test-ledger-tools-blocks-chips.cjs scripts/test-ledger-tools-command-mode-refresh.cjs scripts/test-ledger-tools-snippets.cjs scripts/test-ledger-tools-vim-mappings.cjs scripts/test-task-status-cycler-dependencies.cjs scripts/test-task-status-cycler-blocks-guards.cjs scripts/test-task-status-cycler-ctrl-enter.cjs scripts/test-task-status-cycler-reference-lifecycle.cjs scripts/test-task-status-cycler-pomodoro-completion.cjs scripts/test-task-status-cycler-pomodoro-work-log.cjs scripts/test-task-status-cycler-pomodoro-reopen.cjs scripts/test-task-status-cycler-blocked-schedule.cjs scripts/test-task-status-cycler-demotion-picker.cjs scripts/test-task-status-cycler-promotion.cjs scripts/test-task-status-cycler-counted-toggle.cjs scripts/test-task-status-cycler-successors.cjs scripts/test-task-status-cycler-successor-wiring.cjs scripts/test-task-status-cycler-successor-polish.cjs scripts/test-task-status-cycler-successor-offers.cjs scripts/test-task-status-cycler-project-pull-in.cjs scripts/test-task-status-cycler-task-links-api.cjs scripts/test-task-status-cycler-task-link-lane.cjs scripts/test-task-status-cycler-freshness.cjs scripts/test-block-id-prompt-dependencies.cjs scripts/test-block-id-prompt-blocks-guards.cjs scripts/test-block-id-prompt-ref-picker-text.cjs scripts/test-block-id-prompt-markers.cjs scripts/test-block-id-prompt-pomodoro-context.cjs scripts/test-block-id-prompt-target-update.cjs scripts/test-block-id-prompt-pomodoro-insertion.cjs scripts/test-block-id-prompt-pomodoro-targets.cjs scripts/test-block-id-prompt-pomodoro-picker-view.cjs scripts/test-block-id-prompt-pomodoro-picker-runtime.cjs scripts/test-block-id-prompt-work-log.cjs scripts/test-block-id-prompt-pomodoro-link-runtime.cjs scripts/test-block-id-prompt-pomodoro-link-picker-api.cjs scripts/test-block-id-prompt-pomodoro-unlink-runtime.cjs scripts/test-block-id-prompt-task-link-deletion.cjs scripts/test-block-id-prompt-plan-budget-and-freshness.cjs scripts/test-prompt-block-id-naming.cjs scripts/test-block-id-prompt-prefill.cjs scripts/test-vim-surround.cjs scripts/test-navigation-dependencies-stage-ranker-and-pool.cjs scripts/test-navigation-dependencies-stage-entry-and-view.cjs scripts/test-navigation-dependencies-stage-writes.cjs scripts/test-navigation-dependencies-stage-mirror-and-badge.cjs scripts/test-navigation-dependencies-stage-stale-guards.cjs scripts/test-navigation-dependencies-stage-performance.cjs scripts/test-navigation-prompt-block-id-stage.cjs scripts/test-navigation-dependencies-writer.cjs scripts/test-navigation-dependency-link-consumption.cjs scripts/test-plugin-build.cjs scripts/test-ledger-tools-stats-journal.cjs scripts/test-ledger-tools-stats-data.cjs scripts/test-ledger-tools-stats-block.cjs scripts/test-ledger-tools-stats-charts.cjs scripts/test-navigation-review-journal.cjs scripts/test-ledger-tools-stats-panels.cjs scripts/test-ledger-tools-reading-board-data.cjs scripts/test-ledger-tools-reading-board-models.cjs scripts/test-ledger-tools-reading-board-block.cjs scripts/test-ledger-tools-pomodoro-home-chips.cjs scripts/test-ledger-tools-pomodoro-themes.cjs scripts/test-navigation-image-zoom-target.cjs scripts/test-navigation-image-zoom-command.cjs scripts/test-docs-inventory.mjs scripts/test-docs-check.mjs scripts/test-navigation-relation-lines.cjs scripts/test-navigation-relation-writer.cjs scripts/test-navigation-relation-links-stage.cjs scripts/test-relation-index-linked-from-stage.cjs scripts/test-ledger-tools-relations.cjs scripts/test-ledger-tools-relation-index.cjs scripts/test-ledger-tools-relation-chips.cjs scripts/test-task-status-cycler-relations.cjs scripts/test-block-id-prompt-relations.cjs scripts/test-ledger-tools-day-strip.cjs scripts/test-ledger-tools-day-strip-themes.cjs scripts/test-ledger-tools-day-strip-plan-host.cjs scripts/test-ledger-tools-fakenode-inspect.cjs scripts/test-ledger-tools-day-strip-hosts.cjs

  checked   block-id-prompt
  checked   bob-articles
  checked   bob-command-mode
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
  duration_ms: 1.17841
  ...
# Subtest: bip BK13–BK15 malformed split mirrors the Depends-On twin
ok 2 - bip BK13–BK15 malformed split mirrors the Depends-On twin
  ---
  duration_ms: 0.364897
  ...
# Subtest: bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
ok 3 - bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice
  ---
  duration_ms: 0.108678
  ...
# Subtest: bip MC1/MC2 Pomodoro scanners skip managed lines
ok 4 - bip MC1/MC2 Pomodoro scanners skip managed lines
  ---
  duration_ms: 1.640212
  ...
# Subtest: explicit task IDs exclusively own dependency lookup
ok 5 - explicit task IDs exclusively own dependency lookup
  ---
  duration_ms: 2.666261
  ...
# Subtest: legacy tasks without an id field still fall back to their block ID
ok 6 - legacy tasks without an id field still fall back to their block ID
  ---
  duration_ms: 0.470719
  ...
# Subtest: blocked-link consumption raises open prerequisites and leaves the dependent blocked
ok 7 - blocked-link consumption raises open prerequisites and leaves the dependent blocked
  ---
  duration_ms: 1.36166
  ...
# Subtest: project-blocked member consumption promotes the project's open prerequisite
ok 8 - project-blocked member consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.752347
  ...
# Subtest: project-blocked resident consumption promotes the project's open prerequisite
ok 9 - project-blocked resident consumption promotes the project's open prerequisite
  ---
  duration_ms: 0.400786
  ...
# Subtest: a tagged inherited ^prj target is refused with its parent named
ok 10 - a tagged inherited ^prj target is refused with its parent named
  ---
  duration_ms: 0.380517
  ...
# Subtest: project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
ok 11 - project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible
  ---
  duration_ms: 1.776383
  ...
# Subtest: project date refusal applies only when the date is the sole project reason
ok 12 - project date refusal applies only when the date is the sole project reason
  ---
  duration_ms: 0.284283
  ...
# Subtest: a project-blocked tag is token-bounded and ignored on lookalike tags
ok 13 - a project-blocked tag is token-bounded and ignored on lookalike tags
  ---
  duration_ms: 0.398732
  ...
# Subtest: task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
ok 14 - task picker includes Blocked tasks and excludes closed, hidden, and untagged lines
  ---
  duration_ms: 0.692302
  ...
# Subtest: task blocked state unifies status and dependency reasons
ok 15 - task blocked state unifies status and dependency reasons
  ---
  duration_ms: 0.336804
  ...
# Subtest: task picker partition sinks blocked tasks while preserving group order
ok 16 - task picker partition sinks blocked tasks while preserving group order
  ---
  duration_ms: 0.206515
  ...
# Subtest: blocked chip labels show useful unmet dependency counts
ok 17 - blocked chip labels show useful unmet dependency counts
  ---
  duration_ms: 0.118086
  ...
# Subtest: blocked tooltips explain dependency and status-only reasons
ok 18 - blocked tooltips explain dependency and status-only reasons
  ---
  duration_ms: 0.290264
  ...
# Subtest: task status classes cover every open task status
ok 19 - task status classes cover every open task status
  ---
  duration_ms: 0.126301
  ...
# Subtest: Blocked tasks remain unmet dependency targets
ok 20 - Blocked tasks remain unmet dependency targets
  ---
  duration_ms: 0.199701
  ...
# Subtest: blocked task count covers both reasons without double-counting
ok 21 - blocked task count covers both reasons without double-counting
  ---
  duration_ms: 0.154855
  ...
# Subtest: single caret relocation preserves embedding and removes aliases
ok 22 - single caret relocation preserves embedding and removes aliases
  ---
  duration_ms: 1.584866
  ...
# Subtest: single caret relocation resets aliased block links
ok 23 - single caret relocation resets aliased block links
  ---
  duration_ms: 0.246501
  ...
# Subtest: single caret relocation strips heading and block subpaths
ok 24 - single caret relocation strips heading and block subpaths
  ---
  duration_ms: 0.247914
  ...
# Subtest: task picker normalizes every supported wiki block-link form
ok 25 - task picker normalizes every supported wiki block-link form
  ---
  duration_ms: 0.665652
  ...
# Subtest: three or more carets never trigger the task picker
ok 26 - three or more carets never trigger the task picker
  ---
  duration_ms: 0.145999
  ...
# Subtest: rapid aliased task picker completion preserves the alias
ok 27 - rapid aliased task picker completion preserves the alias
  ---
  duration_ms: 2.485708
  ...
# Subtest: task picker recognition is independent of Markdown source context
ok 28 - task picker recognition is independent of Markdown source context
  ---
  duration_ms: 0.740414
  ...
# Subtest: task picker recognition respects cursor proximity and fenced code
ok 29 - task picker recognition respects cursor proximity and fenced code
  ---
  duration_ms: 0.239407
  ...
# Subtest: plan budget suffix: link Notice appends the meter computed on post-write daily content
ok 30 - plan budget suffix: link Notice appends the meter computed on post-write daily content
  ---
  duration_ms: 6.985692
  ...
# Subtest: plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
ok 31 - plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
  ---
  duration_ms: 1.731046
  ...
# Subtest: plan budget suffix: unlink Notice marks an over-cap plan with 🔴
ok 32 - plan budget suffix: unlink Notice marks an over-cap plan with 🔴
  ---
  duration_ms: 2.220992
  ...
# Subtest: plan budget suffix: Next task without a block ID prompts for one and omits the meter
ok 33 - plan budget suffix: Next task without a block ID prompts for one and omits the meter
  ---
  duration_ms: 0.412878
  ...
# Subtest: plan budget suffix: Task Link Notice appends the meter from post-write daily content
ok 34 - plan budget suffix: Task Link Notice appends the meter from post-write daily content
  ---
  duration_ms: 2.038132
  ...
# Subtest: plan budget suffix: Task Link Notice omits the meter when no daily note takes part
ok 35 - plan budget suffix: Task Link Notice omits the meter when no daily note takes part
  ---
  duration_ms: 0.559368
  ...
# Subtest: planTargetTaskUpdate stamps the rewritten line last via injected stamper
ok 36 - planTargetTaskUpdate stamps the rewritten line last via injected stamper
  ---
  duration_ms: 0.357403
  ...
# Subtest: planTargetTaskUpdate without a stamper never stamps (identity default)
ok 37 - planTargetTaskUpdate without a stamper never stamps (identity default)
  ---
  duration_ms: 0.129107
  ...
# Subtest: planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
ok 38 - planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
  ---
  duration_ms: 0.343336
  ...
# Subtest: planTargetTaskUpdate stamps a Next task that gains a block ID
ok 39 - planTargetTaskUpdate stamps a Next task that gains a block ID
  ---
  duration_ms: 0.505887
  ...
# Subtest: planTargetTaskUpdate tolerates a throwing stamper
ok 40 - planTargetTaskUpdate tolerates a throwing stamper
  ---
  duration_ms: 0.210712
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 41 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.429009
  ...
# Subtest: dedicated-link helpers reject Depends-On lines
ok 42 - dedicated-link helpers reject Depends-On lines
  ---
  duration_ms: 0.335331
  ...
# Subtest: Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
ok 43 - Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
  ---
  duration_ms: 0.350509
  ...
# Subtest: malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
ok 44 - malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
  ---
  duration_ms: 0.11525
  ...
# Subtest: Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
ok 45 - Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
  ---
  duration_ms: 0.250518
  ...
# Subtest: Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
ok 46 - Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
  ---
  duration_ms: 0.206013
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent
ok 47 - readPlanBudgetMeter keeps per-cap over flags independent
  ---
  duration_ms: 0.20946
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent (mirror)
ok 48 - readPlanBudgetMeter keeps per-cap over flags independent (mirror)
  ---
  duration_ms: 0.110491
  ...
# Subtest: block-id-prompt freshness accessors degrade without ledger-tools
ok 49 - block-id-prompt freshness accessors degrade without ledger-tools
  ---
  duration_ms: 0.242253
  ...
# Subtest: block-id-prompt refuses Pomodoro ledger lines before calling a stamper
ok 50 - block-id-prompt refuses Pomodoro ledger lines before calling a stamper
  ---
  duration_ms: 0.212025
  ...
# Subtest: list item body bounds trim whitespace and reject empty bullets
ok 51 - list item body bounds trim whitespace and reject empty bullets
  ---
  duration_ms: 1.47131
  ...
# Subtest: Pomodoro activation eligibility requires a sole-content sub-bullet
ok 52 - Pomodoro activation eligibility requires a sole-content sub-bullet
  ---
  duration_ms: 2.023926
  ...
# Subtest: Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
ok 53 - Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history
  ---
  duration_ms: 0.280145
  ...
# Subtest: Pomodoro source context distinguishes ledger ancestry and open state
ok 54 - Pomodoro source context distinguishes ledger ancestry and open state
  ---
  duration_ms: 0.46598
  ...
# Subtest: future cleanup touches only later open Pomodoros and counts duplicates
ok 55 - future cleanup touches only later open Pomodoros and counts duplicates
  ---
  duration_ms: 2.434139
  ...
# Subtest: cleanup resolves aliases, embeds, same-note links, and alternate paths
ok 56 - cleanup resolves aliases, embeds, same-note links, and alternate paths
  ---
  duration_ms: 1.558075
  ...
# Subtest: dedicated bullet subtree cleanup preserves CRLF line endings
ok 57 - dedicated bullet subtree cleanup preserves CRLF line endings
  ---
  duration_ms: 0.411156
  ...
# Subtest: existing-ID task completion prunes future links in the source editor
ok 58 - existing-ID task completion prunes future links in the source editor
  ---
  duration_ms: 2.553476
  ...
# Subtest: new-ID same-file completion plans cleanup after the task edit
ok 59 - new-ID same-file completion plans cleanup after the task edit
  ---
  duration_ms: 1.374364
  ...
# Subtest: findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
ok 60 - findDirectPomodoroLinkTask includes a \#hide project task, unlike the task-picker's own listing
  ---
  duration_ms: 1.992035
  ...
# Subtest: findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
ok 61 - findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines
  ---
  duration_ms: 0.1832
  ...
# Subtest: findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
ok 62 - findDirectPomodoroLinkTask accepts every open status and carries the existing block ID
  ---
  duration_ms: 0.175976
  ...
# Subtest: todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
ok 63 - todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder
  ---
  duration_ms: 0.605085
  ...
# Subtest: todayDailyPath honors a custom Daily Notes format and an empty folder
ok 64 - todayDailyPath honors a custom Daily Notes format and an empty folder
  ---
  duration_ms: 0.224409
  ...
# Subtest: formatDailyDate resolves bracketed literal text alongside date tokens
ok 65 - formatDailyDate resolves bracketed literal text alongside date tokens
  ---
  duration_ms: 0.126501
  ...
# Subtest: getDailyNotesOptions reads the daily-notes core plugin's configured options
ok 66 - getDailyNotesOptions reads the daily-notes core plugin's configured options
  ---
  duration_ms: 0.615315
  ...
# Subtest: computeFencedLineFlags marks opening and closing fence lines and everything between
ok 67 - computeFencedLineFlags marks opening and closing fence lines and everything between
  ---
  duration_ms: 0.255518
  ...
# Subtest: selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
ok 68 - selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder
  ---
  duration_ms: 0.752928
  ...
# Subtest: selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
ok 69 - selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed
  ---
  duration_ms: 0.451823
  ...
# Subtest: selectPomodoroInsertionTarget rejects more than one open timed entry
ok 70 - selectPomodoroInsertionTarget rejects more than one open timed entry
  ---
  duration_ms: 0.21475
  ...
# Subtest: selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
ok 71 - selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one
  ---
  duration_ms: 0.194441
  ...
# Subtest: findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
ok 72 - findPomodoroChildIndentation reuses existing child indentation before falling back to a tab
  ---
  duration_ms: 0.17799
  ...
# Subtest: planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
ok 73 - planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation
  ---
  duration_ms: 1.128706
  ...
# Subtest: planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
ok 74 - planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro
  ---
  duration_ms: 1.416925
  ...
# Subtest: planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
ok 75 - planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits
  ---
  duration_ms: 0.25145
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
ok 76 - planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings
  ---
  duration_ms: 0.539099
  ...
# Subtest: planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
ok 77 - planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings
  ---
  duration_ms: 0.498682
  ...
# Subtest: planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
ok 78 - planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees
  ---
  duration_ms: 0.300985
  ...
# Subtest: planPomodoroLinkInsertion inserts before the separator preceding later content
ok 79 - planPomodoroLinkInsertion inserts before the separator preceding later content
  ---
  duration_ms: 0.251891
  ...
# Subtest: planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
ok 80 - planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent
  ---
  duration_ms: 0.289092
  ...
# Subtest: planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
ok 81 - planPomodoroLinkInsertion before separators composes with future cleanup, preserving history
  ---
  duration_ms: 0.367292
  ...
# Subtest: existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
ok 82 - existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note)
  ---
  duration_ms: 3.081926
  ...
# Subtest: same-note Pomodoro link runtime composes the task update with adjacent insertion
ok 83 - same-note Pomodoro link runtime composes the task update with adjacent insertion
  ---
  duration_ms: 1.160886
  ...
# Subtest: new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
ok 84 - new-ID Pomodoro link runtime keeps terminal-newline separators adjacent
  ---
  duration_ms: 0.583644
  ...
# Subtest: planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
ok 85 - planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext
  ---
  duration_ms: 0.305293
  ...
# Subtest: all-open cleanup removes current and future links while preserving history and unresolved links
ok 86 - all-open cleanup removes current and future links while preserving history and unresolved links
  ---
  duration_ms: 0.8799
  ...
# Subtest: all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
ok 87 - all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties
  ---
  duration_ms: 1.108647
  ...
# Subtest: all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
ok 88 - all-open cleanup deletes an emptied entry under CRLF without disturbing line endings
  ---
  duration_ms: 0.221302
  ...
# Subtest: all-open cleanup treats missing section, no open entries, and no matches as no-op successes
ok 89 - all-open cleanup treats missing section, no open entries, and no matches as no-op successes
  ---
  duration_ms: 0.189562
  ...
# Subtest: composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
ok 90 - composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour)
  ---
  duration_ms: 0.266118
  ...
# Subtest: pomodoro link picker choices normalize to existing/new or null
ok 91 - pomodoro link picker choices normalize to existing/new or null
  ---
  duration_ms: 1.292027
  ...
# Subtest: pomodoroLinkPicker api never rejects and validates choices
ok 92 - pomodoroLinkPicker api never rejects and validates choices
  ---
  duration_ms: 0.418169
  ...
# Subtest: destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
ok 93 - destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless
  ---
  duration_ms: 0.791501
  ...
# Subtest: destination pick with a section releases its guards when the modal cannot open
ok 94 - destination pick with a section releases its guards when the modal cannot open
  ---
  duration_ms: 1.687452
  ...
# Subtest: plugin lifecycle installs the api and drops it on unload
ok 95 - plugin lifecycle installs the api and drops it on unload
  ---
  duration_ms: 0.325251
  ...
# Subtest: Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
ok 96 - Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command
  ---
  duration_ms: 2.473012
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor requires a single cursor
ok 97 - resolvePomodoroLinkTaskFromEditor requires a single cursor
  ---
  duration_ms: 0.318358
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
ok 98 - resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block
  ---
  duration_ms: 0.369616
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
ok 99 - resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task
  ---
  duration_ms: 0.493853
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
ok 100 - resolvePomodoroLinkTaskFromEditor accepts a \#hide project task directly under the cursor
  ---
  duration_ms: 0.524682
  ...
# Subtest: blocked-link consumption reports dependency reasons before the project date
ok 101 - blocked-link consumption reports dependency reasons before the project date
  ---
  duration_ms: 2.625714
  ...
# Subtest: Pomodoro link checks do not read other notes for a non-Blocked task
ok 102 - Pomodoro link checks do not read other notes for a non-Blocked task
  ---
  duration_ms: 0.305995
  ...
# Subtest: resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
ok 103 - resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note
  ---
  duration_ms: 0.368023
  ...
# Subtest: task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
ok 104 - task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress
  ---
  duration_ms: 6.025216
  ...
# Subtest: task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
ok 105 - task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next
  ---
  duration_ms: 1.922822
  ...
# Subtest: task-mode toggle: linked only under a completed Pomodoro links again
ok 106 - task-mode toggle: linked only under a completed Pomodoro links again
  ---
  duration_ms: 0.91138
  ...
# Subtest: task-mode toggle: a task without a block ID is never linked and prompts for one
ok 107 - task-mode toggle: a task without a block ID is never linked and prompts for one
  ---
  duration_ms: 0.424861
  ...
# Subtest: existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
ok 108 - existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice
  ---
  duration_ms: 1.071677
  ...
# Subtest: forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
ok 109 - forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link
  ---
  duration_ms: 0.530824
  ...
# Subtest: new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
ok 110 - new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task
  ---
  duration_ms: 0.514653
  ...
# Subtest: submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
ok 111 - submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time
  ---
  duration_ms: 0.149936
  ...
# Subtest: submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
ok 112 - submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open
  ---
  duration_ms: 0.197999
  ...
# Subtest: same-note Pomodoro link runtime: task and ledger edits merge into one transaction
ok 113 - same-note Pomodoro link runtime: task and ledger edits merge into one transaction
  ---
  duration_ms: 1.157381
  ...
# Subtest: linking an already-linked Ready task raises it to Next without duplicating the link
ok 114 - linking an already-linked Ready task raises it to Next without duplicating the link
  ---
  duration_ms: 0.488903
  ...
# Subtest: Next task without a block ID preflights the picker before prompting
ok 115 - Next task without a block ID preflights the picker before prompting
  ---
  duration_ms: 0.474086
  ...
# Subtest: Pomodoro link stops before any mutation when today's daily note is missing
ok 116 - Pomodoro link stops before any mutation when today's daily note is missing
  ---
  duration_ms: 0.19909
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
ok 117 - Pomodoro link stops before any task mutation when the daily note has no Pomodoros section
  ---
  duration_ms: 0.47142
  ...
# Subtest: Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
ok 118 - Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros
  ---
  duration_ms: 0.280085
  ...
# Subtest: Pomodoro link aborts without any write when the task line changed since it was selected
ok 119 - Pomodoro link aborts without any write when the task line changed since it was selected
  ---
  duration_ms: 0.157261
  ...
# Subtest: Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
ok 120 - Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds
  ---
  duration_ms: 0.609504
  ...
# Subtest: canceling the Pomodoro block-ID modal leaves the note untouched
ok 121 - canceling the Pomodoro block-ID modal leaves the note untouched
  ---
  duration_ms: 0.173611
  ...
# Subtest: review-walk: existing-ID link hands its Linked notice to continue with no separate notice
ok 122 - review-walk: existing-ID link hands its Linked notice to continue with no separate notice
  ---
  duration_ms: 0.893045
  ...
# Subtest: review-walk: prompted-ID link continues after submit
ok 123 - review-walk: prompted-ID link continues after submit
  ---
  duration_ms: 0.982777
  ...
# Subtest: review-walk: prompt cancel settles with null
ok 124 - review-walk: prompt cancel settles with null
  ---
  duration_ms: 0.165757
  ...
# Subtest: review-walk: BUSY swallows the key with no write
ok 125 - review-walk: BUSY swallows the key with no write
  ---
  duration_ms: 0.273843
  ...
# Subtest: review-walk: failed link keeps its notice and settles with null
ok 126 - review-walk: failed link keeps its notice and settles with null
  ---
  duration_ms: 0.190684
  ...
# Subtest: review-walk: partial link keeps its notice and never continues with an outcome
ok 127 - review-walk: partial link keeps its notice and never continues with an outcome
  ---
  duration_ms: 0.7124
  ...
# Subtest: inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
ok 128 - inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes
  ---
  duration_ms: 0.212946
  ...
# Subtest: inbox-route: non-inbox notes and task-link mode never prompt
ok 129 - inbox-route: non-inbox notes and task-link mode never prompt
  ---
  duration_ms: 0.622148
  ...
# Subtest: inbox-route: cancel writes nothing and settles once
ok 130 - inbox-route: cancel writes nothing and settles once
  ---
  duration_ms: 0.471531
  ...
# Subtest: inbox-route: stay matches today
ok 131 - inbox-route: stay matches today
  ---
  duration_ms: 1.36658
  ...
# Subtest: inbox-route: move links, then moves, with one composed toast and a route continue
ok 132 - inbox-route: move links, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.591399
  ...
# Subtest: inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
ok 133 - inbox-route: a new block ID goes through the ID prompt first, then the route, with the reserved ID passed
  ---
  duration_ms: 0.831768
  ...
# Subtest: inbox-route: a move failure gives the partial notice plus a link-today continue
ok 134 - inbox-route: a move failure gives the partial notice plus a link-today continue
  ---
  duration_ms: 0.450561
  ...
# Subtest: review-walk: no nav or nav v2 keeps today's notices
ok 135 - review-walk: no nav or nav v2 keeps today's notices
  ---
  duration_ms: 0.890621
  ...
# Subtest: inbox-route: source drift during route prompt refuses without writes
ok 136 - inbox-route: source drift during route prompt refuses without writes
  ---
  duration_ms: 0.320652
  ...
# Subtest: inbox-route: block-ID route cancel returns sentinel and settles null once
ok 137 - inbox-route: block-ID route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.315452
  ...
# Subtest: inbox-route: link no-op with move never commits
ok 138 - inbox-route: link no-op with move never commits
  ---
  duration_ms: 0.168531
  ...
# Subtest: picker opens only on the link direction, never on unlink
ok 139 - picker opens only on the link direction, never on unlink
  ---
  duration_ms: 8.807258
  ...
# Subtest: picker never opens in task-link mode
ok 140 - picker never opens in task-link mode
  ---
  duration_ms: 3.457071
  ...
# Subtest: Depends-On refusals never open the picker
ok 141 - Depends-On refusals never open the picker
  ---
  duration_ms: 0.945205
  ...
# Subtest: preflight refusals open nothing
ok 142 - preflight refusals open nothing
  ---
  duration_ms: 0.546904
  ...
# Subtest: picking a non-default entry links there
ok 143 - picking a non-default entry links there
  ---
  duration_ms: 1.102335
  ...
# Subtest: cancel writes nothing with no Notice and settles the walk null
ok 144 - cancel writes nothing with no Notice and settles the walk null
  ---
  duration_ms: 0.648308
  ...
# Subtest: a no-ID task gets picker, then the block-ID prompt with the target carried
ok 145 - a no-ID task gets picker, then the block-ID prompt with the target carried
  ---
  duration_ms: 0.876574
  ...
# Subtest: inbox order is picker, then route, then write
ok 146 - inbox order is picker, then route, then write
  ---
  duration_ms: 0.701018
  ...
# Subtest: a review-walk landing continues with link-today and the new text
ok 147 - a review-walk landing continues with link-today and the new text
  ---
  duration_ms: 0.881454
  ...
# Subtest: an all-closed ledger creates a new entry after the last completed block
ok 148 - an all-closed ledger creates a new entry after the last completed block
  ---
  duration_ms: 1.603122
  ...
# Subtest: several running entries allow an explicit pick
ok 149 - several running entries allow an explicit pick
  ---
  duration_ms: 0.680269
  ...
# Subtest: a target that changed before commit refuses with no writes
ok 150 - a target that changed before commit refuses with no writes
  ---
  duration_ms: 0.483985
  ...
# Subtest: a target that closed before commit refuses with no writes
ok 151 - a target that closed before commit refuses with no writes
  ---
  duration_ms: 0.394624
  ...
# Subtest: the task note being the daily note uses one editor transaction
ok 152 - the task note being the daily note uses one editor transaction
  ---
  duration_ms: 0.610917
  ...
# Subtest: promptOpen blocks re-entry while the picker is open
ok 153 - promptOpen blocks re-entry while the picker is open
  ---
  duration_ms: 9.602608
  ...
# Subtest: header shows title, subtitle, lane chip per status, and block-ID chip
ok 154 - header shows title, subtitle, lane chip per status, and block-ID chip
  ---
  duration_ms: 9.414868
  ...
# Subtest: rows render in document order with the default selected
ok 155 - rows render in document order with the default selected
  ---
  duration_ms: 1.166247
  ...
# Subtest: recent theme rows follow today's rows and render component swatches
ok 156 - recent theme rows follow today's rows and render component swatches
  ---
  duration_ms: 18.168057
  ...
# Subtest: exact recent themes suppress generic creation and preserve catalog spelling
ok 157 - exact recent themes suppress generic creation and preserve catalog spelling
  ---
  duration_ms: 2.374915
  ...
# Subtest: Ctrl+D hides a Recent suggestion as an undoable ghost and leaves Today unchanged
ok 158 - Ctrl+D hides a Recent suggestion as an undoable ghost and leaves Today unchanged
  ---
  duration_ms: 11.789313
  ...
# Subtest: new-name rows show near-duplicate and hidden-theme hints
ok 159 - new-name rows show near-duplicate and hidden-theme hints
  ---
  duration_ms: 4.650393
  ...
# Subtest: running row shows progress fraction and minutes-left meta
ok 160 - running row shows progress fraction and minutes-left meta
  ---
  duration_ms: 0.994509
  ...
# Subtest: unnamed entries render muted italic
ok 161 - unnamed entries render muted italic
  ---
  duration_ms: 0.33541
  ...
# Subtest: filtering ranks, highlights, and clearing restores the default
ok 162 - filtering ranks, highlights, and clearing restores the default
  ---
  duration_ms: 0.933323
  ...
# Subtest: create row meta, divider, and theme badge
ok 163 - create row meta, divider, and theme badge
  ---
  duration_ms: 1.467923
  ...
# Subtest: exact open names suppress the create row; prefix matches keep it
ok 164 - exact open names suppress the create row; prefix matches keep it
  ---
  duration_ms: 0.69623
  ...
# Subtest: theme badge turns red over cap; a throwing budget hides the detail
ok 165 - theme badge turns red over cap; a throwing budget hides the detail
  ---
  duration_ms: 2.617748
  ...
# Subtest: invalid rows explain the grammar and are inert on Enter
ok 166 - invalid rows explain the grammar and are inert on Enter
  ---
  duration_ms: 2.918253
  ...
# Subtest: multiple running entries show the banner, no pills, and block creation
ok 167 - multiple running entries show the banner, no pills, and block creation
  ---
  duration_ms: 0.929675
  ...
# Subtest: navigation wraps and skips non-selectable rows
ok 168 - navigation wraps and skips non-selectable rows
  ---
  duration_ms: 1.209389
  ...
# Subtest: empty state invites planning a Pomodoro
ok 169 - empty state invites planning a Pomodoro
  ---
  duration_ms: 0.379335
  ...
# Subtest: footer hints and plan meter
ok 170 - footer hints and plan meter
  ---
  duration_ms: 1.062439
  ...
# Subtest: Enter chooses the selected row; click chooses that row
ok 171 - Enter chooses the selected row; click chooses that row
  ---
  duration_ms: 0.765973
  ...
# Subtest: Shift+Enter creates; an exact open name links there instead
ok 172 - Shift+Enter creates; an exact open name links there instead
  ---
  duration_ms: 0.80154
  ...
# Subtest: Ctrl+Shift+Enter commits exactly like Enter
ok 173 - Ctrl+Shift+Enter commits exactly like Enter
  ---
  duration_ms: 0.382661
  ...
# Subtest: Escape and Ctrl+[ cancel with no choice; settle-once holds
ok 174 - Escape and Ctrl+[ cancel with no choice; settle-once holds
  ---
  duration_ms: 0.930506
  ...
# Subtest: canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
ok 175 - canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates
  ---
  duration_ms: 1.61796
  ...
# Subtest: canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
ok 176 - canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII
  ---
  duration_ms: 0.295264
  ...
# Subtest: pomodoroLinkSelectorSlug mirrors capture slugs
ok 177 - pomodoroLinkSelectorSlug mirrors capture slugs
  ---
  duration_ms: 0.263734
  ...
# Subtest: parsePomodoroEntryParts reads canonical and legacy entry lines
ok 178 - parsePomodoroEntryParts reads canonical and legacy entry lines
  ---
  duration_ms: 1.572493
  ...
# Subtest: collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
ok 179 - collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes
  ---
  duration_ms: 1.489614
  ...
# Subtest: collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
ok 180 - collectPomodoroLinkEntries detects running, next-up, default, and ambiguity
  ---
  duration_ms: 1.016081
  ...
# Subtest: collectPomodoroLinkEntries counts links but excludes struck references
ok 181 - collectPomodoroLinkEntries counts links but excludes struck references
  ---
  duration_ms: 0.460449
  ...
# Subtest: collectPomodoroLinkEntries falls back to range text and position titles
ok 182 - collectPomodoroLinkEntries falls back to range text and position titles
  ---
  duration_ms: 0.278031
  ...
# Subtest: pomodoroRunProgress reports fractions, overtime, and midnight wrap
ok 183 - pomodoroRunProgress reports fractions, overtime, and midnight wrap
  ---
  duration_ms: 0.517738
  ...
# Subtest: buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
ok 184 - buildPomodoroLinkPickerRows ranks exact slugs before prefix hits
  ---
  duration_ms: 1.097276
  ...
# Subtest: buildPomodoroLinkPickerRows keeps the create row for prefix matches
ok 185 - buildPomodoroLinkPickerRows keeps the create row for prefix matches
  ---
  duration_ms: 0.385706
  ...
# Subtest: buildPomodoroLinkPickerRows marks completed-only names as again
ok 186 - buildPomodoroLinkPickerRows marks completed-only names as again
  ---
  duration_ms: 0.199951
  ...
# Subtest: buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
ok 187 - buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection
  ---
  duration_ms: 0.454257
  ...
# Subtest: buildPomodoroLinkPickerRows matches times, positions, and block IDs
ok 188 - buildPomodoroLinkPickerRows matches times, positions, and block IDs
  ---
  duration_ms: 0.613462
  ...
# Subtest: resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
ok 189 - resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates
  ---
  duration_ms: 0.32962
  ...
# Subtest: defaultPomodoroLinkChoice returns the default entry or null
ok 190 - defaultPomodoroLinkChoice returns the default entry or null
  ---
  duration_ms: 0.196215
  ...
# Subtest: planExplicitPomodoroLinkInsertion links under a chosen existing entry
ok 191 - planExplicitPomodoroLinkInsertion links under a chosen existing entry
  ---
  duration_ms: 0.942941
  ...
# Subtest: planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
ok 192 - planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes
  ---
  duration_ms: 0.268433
  ...
# Subtest: planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
ok 193 - planExplicitPomodoroLinkInsertion is idempotent and cleans other opens
  ---
  duration_ms: 1.102325
  ...
# Subtest: planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
ok 194 - planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion
  ---
  duration_ms: 0.395094
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after the running entry
ok 195 - planExplicitPomodoroLinkInsertion creates after the running entry
  ---
  duration_ms: 0.656053
  ...
# Subtest: planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
ok 196 - planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top
  ---
  duration_ms: 0.713543
  ...
# Subtest: planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
ok 197 - planExplicitPomodoroLinkInsertion links into a raced open name without duplicating
  ---
  duration_ms: 0.20411
  ...
# Subtest: planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
ok 198 - planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets
  ---
  duration_ms: 0.29834
  ...
# Subtest: planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
ok 199 - planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline
  ---
  duration_ms: 0.399784
  ...
# Subtest: buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
ok 200 - buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names
  ---
  duration_ms: 0.196796
  ...
# Subtest: buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
ok 201 - buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names
  ---
  duration_ms: 0.192849
  ...
# Subtest: planExplicitPomodoroLinkInsertion matches mixed-case raced open names
ok 202 - planExplicitPomodoroLinkInsertion matches mixed-case raced open names
  ---
  duration_ms: 0.205142
  ...
# Subtest: buildPomodoroLinkPickerRows bounds \#N position matches
ok 203 - buildPomodoroLinkPickerRows bounds \#N position matches
  ---
  duration_ms: 0.483123
  ...
# Subtest: planPomodoroLinkInsertion without a target keeps today's behavior and shape
ok 204 - planPomodoroLinkInsertion without a target keeps today's behavior and shape
  ---
  duration_ms: 0.452795
  ...
# Subtest: direct unlink without a daily note keeps the Next lane and reports it
ok 205 - direct unlink without a daily note keeps the Next lane and reports it
  ---
  duration_ms: 2.37794
  ...
# Subtest: In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
ok 206 - In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists
  ---
  duration_ms: 0.480928
  ...
# Subtest: In Progress unlink with a summary keeps the lane and creates a Work Log
ok 207 - In Progress unlink with a summary keeps the lane and creates a Work Log
  ---
  duration_ms: 1.24587
  ...
# Subtest: In Progress unlink revalidates task text and block-ID uniqueness at confirmation
ok 208 - In Progress unlink revalidates task text and block-ID uniqueness at confirmation
  ---
  duration_ms: 1.035728
  ...
# Subtest: Next task unlink removes current and future links and keeps the Next lane
ok 209 - Next task unlink removes current and future links and keeps the Next lane
  ---
  duration_ms: 3.678826
  ...
# Subtest: In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
ok 210 - In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane
  ---
  duration_ms: 0.742999
  ...
# Subtest: same-note Next unlink merges the Work Log and all-open cleanup in the active editor
ok 211 - same-note Next unlink merges the Work Log and all-open cleanup in the active editor
  ---
  duration_ms: 0.84779
  ...
# Subtest: same-note In Progress unlink merges cleanup and Work Log in the active editor
ok 212 - same-note In Progress unlink merges cleanup and Work Log in the active editor
  ---
  duration_ms: 0.590879
  ...
# Subtest: Next unlink stops before any write when daily cleanup write is stale
ok 213 - Next unlink stops before any write when daily cleanup write is stale
  ---
  duration_ms: 0.778708
  ...
# Subtest: Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
ok 214 - Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale
  ---
  duration_ms: 0.973599
  ...
# Subtest: In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
ok 215 - In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale
  ---
  duration_ms: 0.672634
  ...
# Subtest: review-walk: unlink settles with null and keeps its notice
ok 216 - review-walk: unlink settles with null and keeps its notice
  ---
  duration_ms: 1.36697
  ...
# Subtest: inbox-route: unlink cancel writes nothing
ok 217 - inbox-route: unlink cancel writes nothing
  ---
  duration_ms: 0.335631
  ...
# Subtest: inbox-route: unlink stay matches today and never commits
ok 218 - inbox-route: unlink stay matches today and never commits
  ---
  duration_ms: 0.548007
  ...
# Subtest: inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
ok 219 - inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue
  ---
  duration_ms: 0.584166
  ...
# Subtest: inbox-route: In Progress unlink with a Work summary routes
ok 220 - inbox-route: In Progress unlink with a Work summary routes
  ---
  duration_ms: 0.59165
  ...
# Subtest: inbox-route: unlink move failure gives the partial notice and stays
ok 221 - inbox-route: unlink move failure gives the partial notice and stays
  ---
  duration_ms: 0.30391
  ...
# Subtest: inbox-route: non-inbox unlink never prompts
ok 222 - inbox-route: non-inbox unlink never prompts
  ---
  duration_ms: 0.291647
  ...
# Subtest: review-walk: Work-summary unlink path retains origin until submit
ok 223 - review-walk: Work-summary unlink path retains origin until submit
  ---
  duration_ms: 0.301646
  ...
# Subtest: inbox-route: unlink source drift during route prompt refuses without writes
ok 224 - inbox-route: unlink source drift during route prompt refuses without writes
  ---
  duration_ms: 0.244918
  ...
# Subtest: inbox-route: Work-summary route cancel returns sentinel and settles null once
ok 225 - inbox-route: Work-summary route cancel returns sentinel and settles null once
  ---
  duration_ms: 0.265998
  ...
# Subtest: inbox-route: unlink no-op with move never commits
ok 226 - inbox-route: unlink no-op with move never commits
  ---
  duration_ms: 0.212406
  ...
# Subtest: same-note unlink maps a task below removed entries through Work-summary inserts
ok 227 - same-note unlink maps a task below removed entries through Work-summary inserts
  ---
  duration_ms: 0.593513
  ...
# Subtest: direct-add seeds from the task headline, not non-task blocks
ok 228 - direct-add seeds from the task headline, not non-task blocks
  ---
  duration_ms: 5.92293
  ...
# Subtest: link-task-complete seeds from the target, prefers open buffers
ok 229 - link-task-complete seeds from the target, prefers open buffers
  ---
  duration_ms: 1.488161
  ...
# Subtest: link-task-complete reports stale and unreadable targets
ok 230 - link-task-complete reports stale and unreadable targets
  ---
  duration_ms: 0.442675
  ...
# Subtest: pomodoro link seeds after the choice from the cursor task
ok 231 - pomodoro link seeds after the choice from the cursor task
  ---
  duration_ms: 0.378032
  ...
# Subtest: marker rename suggests from the unique task, never hiding ambiguity
ok 232 - marker rename suggests from the unique task, never hiding ambiguity
  ---
  duration_ms: 0.74883
  ...
# Subtest: modal seeds the value, selects once, and never overwrites typing
ok 233 - modal seeds the value, selects once, and never overwrites typing
  ---
  duration_ms: 2.098287
  ...
# Subtest: modal disables Save while loading and survives close/reopen
ok 234 - modal disables Save while loading and survives close/reopen
  ---
  duration_ms: 3.086144
  ...
# Subtest: submit revalidates: occupied IDs and stale tasks fail editable
ok 235 - submit revalidates: occupied IDs and stale tasks fail editable
  ---
  duration_ms: 0.700387
  ...
# Subtest: cancelling writes no ID and explicit renames keep the current ID
ok 236 - cancelling writes no ID and explicit renames keep the current ID
  ---
  duration_ms: 0.853439
  ...
# Subtest: the task picker drops the paired \#ref and prefixes the book
ok 237 - the task picker drops the paired \#ref and prefixes the book
  ---
  duration_ms: 2.610836
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 238 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.31936
  ...
# Subtest: block-id-prompt LK1–LK19 recognises only relation line shapes
ok 239 - block-id-prompt LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 1.371069
  ...
# Subtest: block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
ok 240 - block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures
  ---
  duration_ms: 1.275736
  ...
# Subtest: block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
ok 241 - block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line
  ---
  duration_ms: 1.547355
  ...
# Subtest: calendar date parsing rejects malformed width and impossible dates
ok 242 - calendar date parsing rejects malformed width and impossible dates
  ---
  duration_ms: 2.355387
  ...
# Subtest: future scheduled field detection respects the yesterday/today/tomorrow boundary
ok 243 - future scheduled field detection respects the yesterday/today/tomorrow boundary
  ---
  duration_ms: 2.375086
  ...
# Subtest: scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
ok 244 - scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines
  ---
  duration_ms: 0.278682
  ...
# Subtest: planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
ok 245 - planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next
  ---
  duration_ms: 1.449038
  ...
# Subtest: planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
ok 246 - planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status
  ---
  duration_ms: 0.288771
  ...
# Subtest: planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
ok 247 - planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion
  ---
  duration_ms: 0.24619
  ...
# Subtest: planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
ok 248 - planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule
  ---
  duration_ms: 0.248925
  ...
# Subtest: planTargetTaskUpdate leaves today and past schedules untouched
ok 249 - planTargetTaskUpdate leaves today and past schedules untouched
  ---
  duration_ms: 0.406757
  ...
# Subtest: planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
ok 250 - planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible
  ---
  duration_ms: 0.556884
  ...
# Subtest: two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
ok 251 - two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists
  ---
  duration_ms: 0.49731
  ...
# Subtest: a malformed single scheduled field is never treated as future
ok 252 - a malformed single scheduled field is never treated as future
  ---
  duration_ms: 0.17754
  ...
# Subtest: an ambiguous scheduled field does not block the legacy Ready promotion
ok 253 - an ambiguous scheduled field does not block the legacy Ready promotion
  ---
  duration_ms: 0.194892
  ...
# Subtest: planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
ok 254 - planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields
  ---
  duration_ms: 0.127063
  ...
# Subtest: Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
ok 255 - Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren
  ---
  duration_ms: 0.477201
  ...
# Subtest: Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
ok 256 - Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab
  ---
  duration_ms: 0.172619
  ...
# Subtest: planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
ok 257 - planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists
  ---
  duration_ms: 0.265677
  ...
# Subtest: planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
ok 258 - planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet
  ---
  duration_ms: 0.143234
  ...
# Subtest: planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
ok 259 - planTargetTaskUpdate never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.125359
  ...
# Subtest: planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
ok 260 - planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry
  ---
  duration_ms: 0.159265
  ...
# Subtest: planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
ok 261 - planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file
  ---
  duration_ms: 0.17804
  ...
# Subtest: planTargetTaskUpdate preserves a trailing newline when one was already present
ok 262 - planTargetTaskUpdate preserves a trailing newline when one was already present
  ---
  duration_ms: 0.174884
  ...
# Subtest: planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
ok 263 - planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove
  ---
  duration_ms: 0.158994
  ...
# Subtest: planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
ok 264 - planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes
  ---
  duration_ms: 0.222284
  ...
# Subtest: planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
ok 265 - planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path
  ---
  duration_ms: 0.161278
  ...
# Subtest: existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
ok 266 - existing-ID activation runtime: cross-note guarded write, canonical link, and success notice
  ---
  duration_ms: 4.642475
  ...
# Subtest: new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
ok 267 - new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice
  ---
  duration_ms: 0.82177
  ...
# Subtest: activation runtime aborts without any write when the target preimage goes stale
ok 268 - activation runtime aborts without any write when the target preimage goes stale
  ---
  duration_ms: 0.431484
  ...
# Subtest: same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
ok 269 - same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it
  ---
  duration_ms: 2.934844
  ...
# Subtest: same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
ok 270 - same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it
  ---
  duration_ms: 0.761855
  ...
# Subtest: a source marker edited after a successful existing-ID target write reports an accurate partial notice
ok 271 - a source marker edited after a successful existing-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.582823
  ...
# Subtest: a source marker edited after a successful new-ID target write reports an accurate partial notice
ok 272 - a source marker edited after a successful new-ID target write reports an accurate partial notice
  ---
  duration_ms: 0.583715
  ...
# Subtest: planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
ok 273 - planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress
  ---
  duration_ms: 0.192347
  ...
# Subtest: planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
ok 274 - planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone
  ---
  duration_ms: 0.131522
  ...
# Subtest: planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
ok 275 - planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log
  ---
  duration_ms: 0.142282
  ...
# Subtest: planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
ok 276 - planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none
  ---
  duration_ms: 0.129668
  ...
# Subtest: direct Task Links raise ^prj while never pulling its date forward
ok 277 - direct Task Links raise ^prj while never pulling its date forward
  ---
  duration_ms: 0.143263
  ...
# Subtest: task-link selection: one link is selectable from any column, several are chosen by cursor
ok 278 - task-link selection: one link is selectable from any column, several are chosen by cursor
  ---
  duration_ms: 5.316112
  ...
# Subtest: task-link selection ignores picker/rename markers, plain links, and Markdown-style links
ok 279 - task-link selection ignores picker/rename markers, plain links, and Markdown-style links
  ---
  duration_ms: 0.547275
  ...
# Subtest: dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
ok 280 - dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms
  ---
  duration_ms: 1.012945
  ...
# Subtest: inline Task Link deletion removes the token with its decoration and collapses whitespace
ok 281 - inline Task Link deletion removes the token with its decoration and collapses whitespace
  ---
  duration_ms: 1.016672
  ...
# Subtest: dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
ok 282 - dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro
  ---
  duration_ms: 1.306776
  ...
# Subtest: mergeCoveringEdits keeps the covering edit and the earlier of identical edits
ok 283 - mergeCoveringEdits keeps the covering edit and the earlier of identical edits
  ---
  duration_ms: 1.724053
  ...
# Subtest: dependency transclusion detection needs an embedded sole-content child of a \#task line
ok 284 - dependency transclusion detection needs an embedded sole-content child of a \#task line
  ---
  duration_ms: 0.740294
  ...
# Subtest: Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
ok 285 - Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links
  ---
  duration_ms: 6.876362
  ...
# Subtest: Task Link on a Next target works from an embedded aliased link outside any Pomodoro
ok 286 - Task Link on a Next target works from an embedded aliased link outside any Pomodoro
  ---
  duration_ms: 1.460839
  ...
# Subtest: same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
ok 287 - same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored
  ---
  duration_ms: 1.279053
  ...
# Subtest: same-note Task Link deletion clamps the restored cursor to the shortened note
ok 288 - same-note Task Link deletion clamps the restored cursor to the shortened note
  ---
  duration_ms: 0.579527
  ...
# Subtest: a cleanup subtree that covers a nested selected link wins and links are not double counted
ok 289 - a cleanup subtree that covers a nested selected link wins and links are not double counted
  ---
  duration_ms: 0.858509
  ...
# Subtest: same-note Task Link in a closed entry deletes the closed entry it empties
ok 290 - same-note Task Link in a closed entry deletes the closed entry it empties
  ---
  duration_ms: 0.626857
  ...
# Subtest: Task Link in another day's note deletes the emptied entry there and in today's note
ok 291 - Task Link in another day's note deletes the emptied entry there and in today's note
  ---
  duration_ms: 0.625123
  ...
# Subtest: Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
ok 292 - Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit
  ---
  duration_ms: 1.36146
  ...
# Subtest: Task Link on an In Progress target with a blank summary logs nothing
ok 293 - Task Link on an In Progress target with a blank summary logs nothing
  ---
  duration_ms: 0.747056
  ...
# Subtest: canceling the In Progress Task Link prompt leaves everything untouched
ok 294 - canceling the In Progress Task Link prompt leaves everything untouched
  ---
  duration_ms: 0.305002
  ...
# Subtest: canceling the In Progress unlink prompt in task mode leaves everything untouched
ok 295 - canceling the In Progress unlink prompt in task mode leaves everything untouched
  ---
  duration_ms: 0.550701
  ...
# Subtest: In Progress Task Link submit revalidates the link line and the target task
ok 296 - In Progress Task Link submit revalidates the link line and the target task
  ---
  duration_ms: 0.610034
  ...
# Subtest: Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
ok 297 - Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked
  ---
  duration_ms: 0.631776
  ...
# Subtest: Task Link on a Done or Cancelled target is refused without edits
ok 298 - Task Link on a Done or Cancelled target is refused without edits
  ---
  duration_ms: 0.354397
  ...
# Subtest: Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
ok 299 - Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits
  ---
  duration_ms: 0.639852
  ...
# Subtest: precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
ok 300 - precedence: any \#task line keeps the task-line behavior; other lines fall to task-link mode or the notice
  ---
  duration_ms: 1.274093
  ...
# Subtest: Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
ok 301 - Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity
  ---
  duration_ms: 0.325111
  ...
# Subtest: Task Link that is a sub-task dependency transclusion is refused without edits
ok 302 - Task Link that is a sub-task dependency transclusion is refused without edits
  ---
  duration_ms: 0.225721
  ...
# Subtest: Task Link partial failure after the daily write is retryable
ok 303 - Task Link partial failure after the daily write is retryable
  ---
  duration_ms: 1.958801
  ...
# Subtest: Task Link stops before any write when the target note changes after planning
ok 304 - Task Link stops before any write when the target note changes after planning
  ---
  duration_ms: 0.390435
  ...
# Subtest: Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
ok 305 - Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks
  ---
  duration_ms: 0.349798
  ...
# Subtest: Task Link subtree deletion removes a nested target task without any status write
ok 306 - Task Link subtree deletion removes a nested target task without any status write
  ---
  duration_ms: 0.258474
  ...
# Subtest: whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
ok 307 - whole-entry deletion at EOF preserves final-newline state (LF/CRLF)
  ---
  duration_ms: 0.578895
  ...
# Subtest: selected-link deletion maps a cursor inside a removed entry to its former start
ok 308 - selected-link deletion maps a cursor inside a removed entry to its former start
  ---
  duration_ms: 0.466451
  ...
# Subtest: work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
ok 309 - work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields
  ---
  duration_ms: 1.53438
  ...
# Subtest: work log date helpers use local calendar components
ok 310 - work log date helpers use local calendar components
  ---
  duration_ms: 0.253725
  ...
# Subtest: planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
ok 311 - planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children
  ---
  duration_ms: 0.664048
  ...
# Subtest: planWorkLogInsertion inherits an existing space-indented child prefix
ok 312 - planWorkLogInsertion inherits an existing space-indented child prefix
  ---
  duration_ms: 0.48703
  ...
# Subtest: planWorkLogInsertion inherits an existing tab-indented child prefix
ok 313 - planWorkLogInsertion inherits an existing tab-indented child prefix
  ---
  duration_ms: 0.240228
  ...
# Subtest: planWorkLogInsertion prepends newest-first entries into existing marker spellings
ok 314 - planWorkLogInsertion prepends newest-first entries into existing marker spellings
  ---
  duration_ms: 0.665782
  ...
# Subtest: planWorkLogInsertion ignores nested child-task markers and preserves CRLF
ok 315 - planWorkLogInsertion ignores nested child-task markers and preserves CRLF
  ---
  duration_ms: 0.380437
  ...
# Subtest: planWorkLogInsertion treats blank summaries as no-op structural edits
ok 316 - planWorkLogInsertion treats blank summaries as no-op structural edits
  ---
  duration_ms: 0.135188
  ...
# Subtest: the Open-reset planner is removed: unlink plans only a Work Log insertion
ok 317 - the Open-reset planner is removed: unlink plans only a Work Log insertion
  ---
  duration_ms: 0.328948
  ...
# Subtest: unlink Work Log plan keeps the In Progress checkbox and appends one entry
ok 318 - unlink Work Log plan keeps the In Progress checkbox and appends one entry
  ---
  duration_ms: 0.412647
  ...
# Subtest: article detection accepts scalar and list frontmatter values
ok 319 - article detection accepts scalar and list frontmatter values
  ---
  duration_ms: 1.77008
  ...
# Subtest: bob resolution prefers its setting, then known install paths, then PATH
ok 320 - bob resolution prefers its setting, then known install paths, then PATH
  ---
  duration_ms: 0.740664
  ...
# Subtest: plan decoder accepts v1 and rejects a foreign schema version
ok 321 - plan decoder accepts v1 and rejects a foreign schema version
  ---
  duration_ms: 0.283982
  ...
# Subtest: bob stdin spawn passes the article contract and vault environment
ok 322 - bob stdin spawn passes the article contract and vault environment
  ---
  duration_ms: 2.402919
  ...
# Subtest: bob plan stdout decodes UTF-8 split across chunks
ok 323 - bob plan stdout decodes UTF-8 split across chunks
  ---
  duration_ms: 0.809907
  ...
# Subtest: early bob exit on stdin reports EPIPE as a run failure
ok 324 - early bob exit on stdin reports EPIPE as a run failure
  ---
  duration_ms: 0.715236
  ...
# Subtest: line hunks become minimal cursor-preserving changes
ok 325 - line hunks become minimal cursor-preserving changes
  ---
  duration_ms: 0.606138
  ...
# Subtest: insert, multi-line replace, and deletion hunks reproduce the formatted note
ok 326 - insert, multi-line replace, and deletion hunks reproduce the formatted note
  ---
  duration_ms: 3.310461
  ...
# Subtest: notice shows bob's text and at most two warning findings
ok 327 - notice shows bob's text and at most two warning findings
  ---
  duration_ms: 0.401286
  ...
# Subtest: inbound changes apply only when their target line still matches the preimage
ok 328 - inbound changes apply only when their target line still matches the preimage
  ---
  duration_ms: 0.682012
  ...
# Subtest: undo guard blocks a reformat until a fresh input or delete event
ok 329 - undo guard blocks a reformat until a fresh input or delete event
  ---
  duration_ms: 0.363615
  ...
# Subtest: leave formatting observes the undo guard before saving or reading
ok 330 - leave formatting observes the undo guard before saving or reading
  ---
  duration_ms: 0.262932
  ...
# Subtest: Convert shows bob's refusal on every invocation
ok 331 - Convert shows bob's refusal on every invocation
  ---
  duration_ms: 0.263433
  ...
# Subtest: old bob's non-JSON article response gets one update notice per session
ok 332 - old bob's non-JSON article response gets one update notice per session
  ---
  duration_ms: 0.187097
  ...
# Subtest: format drops its response if the editor changed while bob was running
ok 333 - format drops its response if the editor changed while bob was running
  ---
  duration_ms: 0.301627
  ...
# Subtest: decoration ranges mark written section numbers from the outline
ok 334 - decoration ranges mark written section numbers from the outline
  ---
  duration_ms: 0.674489
  ...
# Subtest: a new outline rerenders each open Reading view once for that generation
ok 335 - a new outline rerenders each open Reading view once for that generation
  ---
  duration_ms: 0.288641
  ...
# Subtest: section at a given line uses the innermost outline range
ok 336 - section at a given line uses the innermost outline range
  ---
  duration_ms: 0.274273
  ...
# Subtest: stale-hint debounce and in-flight state machine
ok 337 - stale-hint debounce and in-flight state machine
  ---
  duration_ms: 0.256119
  ...
# Subtest: reading-view wrapping puts the leading number token in span.bob-secno
ok 338 - reading-view wrapping puts the leading number token in span.bob-secno
  ---
  duration_ms: 0.557524
  ...
# Subtest: applied plans remap outline lines onto the formatted buffer
ok 339 - applied plans remap outline lines onto the formatted buffer
  ---
  duration_ms: 0.134086
  ...
# Subtest: article styles scope the reading look under .bob-article
ok 340 - article styles scope the reading look under .bob-article
  ---
  duration_ms: 3.998066
  ...
# Subtest: look settings default to serif typeface and stale-number hints
ok 341 - look settings default to serif typeface and stale-number hints
  ---
  duration_ms: 0.168111
  ...
# Subtest: fingerprints compare path, mtime, and size
ok 342 - fingerprints compare path, mtime, and size
  ---
  duration_ms: 1.818894
  ...
# Subtest: validation accepts the fixture and rejects malformed catalogs
ok 343 - validation accepts the fixture and rejects malformed catalogs
  ---
  duration_ms: 0.40302
  ...
# Subtest: refresh fetches and validates through the real protocol
ok 344 - refresh fetches and validates through the real protocol
  ---
  duration_ms: 78.194546
  ...
# Subtest: lookup resolves entries, aliases of entries, and excluded paths
ok 345 - lookup resolves entries, aliases of entries, and excluded paths
  ---
  duration_ms: 0.601258
  ...
# Subtest: argv assembly puts preview args before fixed args
ok 346 - argv assembly puts preview args before fixed args
  ---
  duration_ms: 0.378663
  ...
# Subtest: palette entries need policy run and all-optional positionals
ok 347 - palette entries need policy run and all-optional positionals
  ---
  duration_ms: 0.264646
  ...
# Subtest: classification order: stop, spawn, timeout, signal
ok 348 - classification order: stop, spawn, timeout, signal
  ---
  duration_ms: 2.648738
  ...
# Subtest: lock phrase wins over exit codes and adapters
ok 349 - lock phrase wins over exit codes and adapters
  ---
  duration_ms: 0.254385
  ...
# Subtest: exit-code hints beat the generic rule; unknown ids are ignored
ok 350 - exit-code hints beat the generic rule; unknown ids are ignored
  ---
  duration_ms: 0.191286
  ...
# Subtest: adapters adjust the result; failures stay honest
ok 351 - adapters adjust the result; failures stay honest
  ---
  duration_ms: 1.196635
  ...
# Subtest: api.commandMode settles, never rejects, and fires the workspace event
ok 352 - api.commandMode settles, never rejects, and fires the workspace event
  ---
  duration_ms: 167.528619
  ...
# Subtest: plugin onload registers run-* commands and exposes the frozen api
ok 353 - plugin onload registers run-* commands and exposes the frozen api
  ---
  duration_ms: 69.004147
  ...
# Subtest: plugin reports missing-bob when the binary is absent
ok 354 - plugin reports missing-bob when the binary is absent
  ---
  duration_ms: 0.674018
  ...
# Subtest: runner notifies with a plain summary after each finish
ok 355 - runner notifies with a plain summary after each finish
  ---
  duration_ms: 4.255768
  ...
# Subtest: catalog outcome adapters cover command-specific results and actions
ok 356 - catalog outcome adapters cover command-specific results and actions
  ---
  duration_ms: 2.77063
  ...
# Subtest: toast classes have distinct timing and newer failures replace older cards
ok 357 - toast classes have distinct timing and newer failures replace older cards
  ---
  duration_ms: 2.91683
  ...
# Subtest: status chip waits 400 ms, tracks multiple runs, and marks overdue writers
ok 358 - status chip waits 400 ms, tracks multiple runs, and marks overdue writers
  ---
  duration_ms: 0.772084
  ...
# Subtest: OS notifications only fire for long runs while Obsidian is unfocused
ok 359 - OS notifications only fire for long runs while Obsidian is unfocused
  ---
  duration_ms: 0.48675
  ...
# Subtest: rerun-last preserves arguments and preview mode; Apply carries the replay seed
ok 360 - rerun-last preserves arguments and preview mode; Apply carries the replay seed
  ---
  duration_ms: 0.501518
  ...
# Subtest: ANSI parsing keeps SGR that splits across chunks
ok 361 - ANSI parsing keeps SGR that splits across chunks
  ---
  duration_ms: 2.909967
  ...
# Subtest: linkify positives resolve and negatives stay plain
ok 362 - linkify positives resolve and negatives stay plain
  ---
  duration_ms: 0.929826
  ...
# Subtest: JSON pretty-print mutes keys on a single document
ok 363 - JSON pretty-print mutes keys on a single document
  ---
  duration_ms: 0.705858
  ...
# Subtest: interleave replay preserves arrival order for copy
ok 364 - interleave replay preserves arrival order for copy
  ---
  duration_ms: 0.509864
  ...
# Subtest: pager keys: scroll, wrap, search, copy, history, stop, close
ok 365 - pager keys: scroll, wrap, search, copy, history, stop, close
  ---
  duration_ms: 0.651034
  ...
# Subtest: history stepping is newest-first
ok 366 - history stepping is newest-first
  ---
  duration_ms: 0.21992
  ...
# Subtest: search matches are exact and advance
ok 367 - search matches are exact and advance
  ---
  duration_ms: 0.234047
  ...
# Subtest: status pill covers running, outcomes, and queued-behind
ok 368 - status pill covers running, outcomes, and queued-behind
  ---
  duration_ms: 0.335261
  ...
# Subtest: plugin pager opens from Output, show-last-output, history, copy, and stop
ok 369 - plugin pager opens from Output, show-last-output, history, copy, and stop
  ---
  duration_ms: 18.676966
  ...
# Subtest: writer stop needs confirmation; reads stop immediately
ok 370 - writer stop needs confirmation; reads stop immediately
  ---
  duration_ms: 2.668075
  ...
# Subtest: watching a run skips the toast
ok 371 - watching a run skips the toast
  ---
  duration_ms: 1.394402
  ...
# Subtest: pretty JSON and ANSI land in the pager body
ok 372 - pretty JSON and ANSI land in the pager body
  ---
  duration_ms: 1.107054
  ...
# Subtest: resolver prefers the explicit setting and expands home
ok 373 - resolver prefers the explicit setting and expands home
  ---
  duration_ms: 1.248905
  ...
# Subtest: resolver consults ledger-tools before the candidates
ok 374 - resolver consults ledger-tools before the candidates
  ---
  duration_ms: 0.196826
  ...
# Subtest: resolver walks candidates, records every path tried, then PATH
ok 375 - resolver walks candidates, records every path tried, then PATH
  ---
  duration_ms: 0.227374
  ...
# Subtest: child env points at the vault, honors features, and drops completion vars
ok 376 - child env points at the vault, honors features, and drops completion vars
  ---
  duration_ms: 0.387871
  ...
# Subtest: inherited NO_COLOR wins; without the color feature NO_COLOR is set
ok 377 - inherited NO_COLOR wins; without the color feature NO_COLOR is set
  ---
  duration_ms: 0.191746
  ...
# Subtest: vault base requires a local folder
ok 378 - vault base requires a local folder
  ---
  duration_ms: 0.165606
  ...
# Subtest: ansi stripping, quoting, durations, and run ids
ok 379 - ansi stripping, quoting, durations, and run ids
  ---
  duration_ms: 0.659149
  ...
# Subtest: completed read writes files, receipt, and an honest record
ok 380 - completed read writes files, receipt, and an honest record
  ---
  duration_ms: 192.822872
  ...
# Subtest: child env carries vault, features, receipt, and tool paths
not ok 381 - child env carries vault, features, receipt, and tool paths
  ---
  duration_ms: 151.152755
  location: '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-command-mode-runner.cjs:103:1'
  failureType: 'testCodeFailure'
  error: |-
    Expected values to be strictly equal:
    
    null !== '1'
    
  code: 'ERR_ASSERTION'
  name: 'AssertionError'
  expected: '1'
  actual: ~
  operator: 'strictEqual'
  stack: |-
    TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins/scripts/test-command-mode-runner.cjs:111:10)
    process.processTicksAndRejections (node:internal/process/task_queues:105:5)
    async Test.run (node:internal/test_runner/test:980:9)
    async Test.processPendingSubtests (node:internal/test_runner/test:677:7)
  ...
# Subtest: literal args with spaces, quotes, and $() stay literal
ok 382 - literal args with spaces, quotes, and $() stay literal
  ---
  duration_ms: 158.97814
  ...
# Subtest: split multi-byte characters survive and big output stays intact
ok 383 - split multi-byte characters survive and big output stays intact
  ---
  duration_ms: 317.28117
  ...
# Subtest: in-memory text truncates past the cap while files keep everything
ok 384 - in-memory text truncates past the cap while files keep everything
  ---
  duration_ms: 36.28875
  ...
# Subtest: a double run is one run: duplicates share the settlement
ok 385 - a double run is one run: duplicates share the settlement
  ---
  duration_ms: 456.227966
  ...
# Subtest: writers serialize FIFO while reads run in parallel
ok 386 - writers serialize FIFO while reads run in parallel
  ---
  duration_ms: 1483.874125
  ...
# Subtest: a failed save refuses the writer
ok 387 - a failed save refuses the writer
  ---
  duration_ms: 1.448486
  ...
# Subtest: read budgets kill; writer budgets mark overdue; stop stops
ok 388 - read budgets kill; writer budgets mark overdue; stop stops
  ---
  duration_ms: 2503.750807
  ...
# Subtest: failures classify: non-zero, signals, lock, and missing bob
ok 389 - failures classify: non-zero, signals, lock, and missing bob
  ---
  duration_ms: 397.632487
  ...
# Subtest: policy and entry guards refuse with reasons
ok 390 - policy and entry guards refuse with reasons
  ---
  duration_ms: 98.159423
  ...
# Subtest: retention keeps the newest fifty and never an unfinished run
ok 391 - retention keeps the newest fifty and never an unfinished run
  ---
  duration_ms: 119.953685
  ...
# Subtest: adoption finalizes from receipts and reports unknown without one
ok 392 - adoption finalizes from receipts and reports unknown without one
  ---
  duration_ms: 2.753078
  ...
# Subtest: folds embed, struck, and plain legacy children into one canonical line
ok 393 - folds embed, struck, and plain legacy children into one canonical line
  ---
  duration_ms: 110.096449
  ...
# Subtest: legacy-label row links come first, then legacy children in order
ok 394 - legacy-label row links come first, then legacy children in order
  ---
  duration_ms: 2.564347
  ...
# Subtest: R2 adopts field-only open dependents; unadoptable ids stay warned
ok 395 - R2 adopts field-only open dependents; unadoptable ids stay warned
  ---
  duration_ms: 0.804106
  ...
# Subtest: closed dependents gain the line but keep the field untouched
ok 396 - closed dependents gain the line but keep the field untouched
  ---
  duration_ms: 1.236512
  ...
# Subtest: open dependents drop stale field ids and stamp targets missing [id::]
ok 397 - open dependents drop stale field ids and stamp targets missing [id::]
  ---
  duration_ms: 0.700037
  ...
# Subtest: unresolved links stay verbatim and keep field ids as breadcrumbs
ok 398 - unresolved links stay verbatim and keep field ids as breadcrumbs
  ---
  duration_ms: 0.640203
  ...
# Subtest: leaves \#^ref embeds, non-task parents, fences, and conflict children alone
ok 399 - leaves \#^ref embeds, non-task parents, fences, and conflict children alone
  ---
  duration_ms: 0.83256
  ...
# Subtest: malformed rows leave the whole dependent alone
ok 400 - malformed rows leave the whole dependent alone
  ---
  duration_ms: 0.616688
  ...
# Subtest: R9 deletes label-only rows and removes the open field
ok 401 - R9 deletes label-only rows and removes the open field
  ---
  duration_ms: 0.754942
  ...
# Subtest: cross-note links use the shortest unambiguous form
ok 402 - cross-note links use the shortest unambiguous form
  ---
  duration_ms: 3.109308
  ...
# Subtest: ambiguous basenames fall back to the full path
ok 403 - ambiguous basenames fall back to the full path
  ---
  duration_ms: 0.651605
  ...
# Subtest: duplicate ids are ambiguous and fatal for --write
ok 404 - duplicate ids are ambiguous and fatal for --write
  ---
  duration_ms: 0.28829
  ...
# Subtest: archive targets keep the done/ path and are never stamped
ok 405 - archive targets keep the done/ path and are never stamped
  ---
  duration_ms: 0.351892
  ...
# Subtest: self links stay on the line but are not projected
ok 406 - self links stay on the line but are not projected
  ---
  duration_ms: 0.451291
  ...
# Subtest: non-task targets stay on the line but are not projected
ok 407 - non-task targets stay on the line but are not projected
  ---
  duration_ms: 0.336633
  ...
# Subtest: preserves CRLF, missing final newline, and cancel-log position
ok 408 - preserves CRLF, missing final newline, and cancel-log position
  ---
  duration_ms: 0.444489
  ...
# Subtest: migration is idempotent
ok 409 - migration is idempotent
  ---
  duration_ms: 1.317335
  ...
# Subtest: parseArgs handles --vault, --write, --help, and rejects unknowns
ok 410 - parseArgs handles --vault, --write, --help, and rejects unknowns
  ---
  duration_ms: 0.788857
  ...
# Subtest: BOB_CLI_DIR wins over a sibling checkout and a cache
ok 411 - BOB_CLI_DIR wins over a sibling checkout and a cache
  ---
  duration_ms: 26.444692
  ...
# Subtest: sibling bob-cli is used when BOB_CLI_DIR is unset
ok 412 - sibling bob-cli is used when BOB_CLI_DIR is unset
  ---
  duration_ms: 18.556715
  ...
# Subtest: an invalid BOB_CLI_DIR does not fall through
ok 413 - an invalid BOB_CLI_DIR does not fall through
  ---
  duration_ms: 10.567322
  ...
# Subtest: cache clone is used when no user-owned checkout exists
ok 414 - cache clone is used when no user-owned checkout exists
  ---
  duration_ms: 28.839765
  ...
# Subtest: refreshing an existing cache keeps git chatter off stdout and forwards exact paths
ok 415 - refreshing an existing cache keeps git chatter off stdout and forwards exact paths
  ---
  duration_ms: 34.188359
  ...
# Subtest: a cache clone with a foreign origin fails before fetch or reset
ok 416 - a cache clone with a foreign origin fails before fetch or reset
  ---
  duration_ms: 41.317743
  ...
# Subtest: a justfile alone is rejected as an explicit bob-cli checkout
ok 417 - a justfile alone is rejected as an explicit bob-cli checkout
  ---
  duration_ms: 35.084682
  ...
# Subtest: just failures propagate
ok 418 - just failures propagate
  ---
  duration_ms: 39.041378
  ...
# Subtest: scans multiline, one-line, and guarded literal registrations
ok 419 - scans multiline, one-line, and guarded literal registrations
  ---
  duration_ms: 3.960895
  ...
# Subtest: scans an optional addCommand call
ok 420 - scans an optional addCommand call
  ---
  duration_ms: 0.360418
  ...
# Subtest: allows addCommand references only in a typeof guard
ok 421 - allows addCommand references only in a typeof guard
  ---
  duration_ms: 0.441573
  ...
# Subtest: rejects bind, call, and aliased addCommand references with source locations
ok 422 - rejects bind, call, and aliased addCommand references with source locations
  ---
  duration_ms: 0.741026
  ...
# Subtest: expands literal command data from a constant-array forEach across source files
ok 423 - expands literal command data from a constant-array forEach across source files
  ---
  duration_ms: 2.353905
  ...
# Subtest: balances nested callback syntax and ignores misleading comments, strings, templates, and regexes
ok 424 - balances nested callback syntax and ignores misleading comments, strings, templates, and regexes
  ---
  duration_ms: 0.811279
  ...
# Subtest: decodes escaped string metadata and literal default hotkeys
ok 425 - decodes escaped string metadata and literal default hotkeys
  ---
  duration_ms: 0.679928
  ...
# Subtest: returns no commands for a plugin without registrations
ok 426 - returns no commands for a plugin without registrations
  ---
  duration_ms: 0.247893
  ...
# Subtest: fails with source locations for dynamic metadata, hotkeys, and malformed tables
ok 427 - fails with source locations for dynamic metadata, hotkeys, and malformed tables
  ---
  duration_ms: 1.155376
  ...
# Subtest: fails duplicate command ids with both registration locations
ok 428 - fails duplicate command ids with both registration locations
  ---
  duration_ms: 0.556373
  ...
# Subtest: checks drift without writes, preserves prose, and generates deterministically
ok 429 - checks drift without writes, preserves prose, and generates deterministically
  ---
  duration_ms: 10.257748
  ...
# Subtest: code-span table cells preserve backslashes and use a safe backtick fence
ok 430 - code-span table cells preserve backslashes and use a safe backtick fence
  ---
  duration_ms: 2.044093
  ...
# Subtest: does not write any output when source validation fails
ok 431 - does not write any output when source validation fails
  ---
  duration_ms: 1.280525
  ...
# Subtest: BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
ok 432 - BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering
  ---
  duration_ms: 3.514421
  ...
# Subtest: reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
ok 433 - reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13)
  ---
  duration_ms: 3.392199
  ...
# Subtest: stale, missing, canonical append, and frozen-owner models (BC8-BC10)
ok 434 - stale, missing, canonical append, and frozen-owner models (BC8-BC10)
  ---
  duration_ms: 0.714284
  ...
# Subtest: Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
ok 435 - Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15)
  ---
  duration_ms: 10.346069
  ...
# Subtest: budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
ok 436 - budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2)
  ---
  duration_ms: 2.100281
  ...
# Subtest: chip builder includes the 🔑 badge and has no edit controls
ok 437 - chip builder includes the 🔑 badge and has no edit controls
  ---
  duration_ms: 1.009037
  ...
# Subtest: RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
ok 438 - RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line
  ---
  duration_ms: 2.437074
  ...
# Subtest: RBC2 hover × on a live chip calls removeDependent; notice is nav's
ok 439 - RBC2 hover × on a live chip calls removeDependent; notice is nav's
  ---
  duration_ms: 0.812622
  ...
# Subtest: RBC3 frozen, stale, and no api.blocks stay navigation-only
ok 440 - RBC3 frozen, stale, and no api.blocks stay navigation-only
  ---
  duration_ms: 1.616046
  ...
# Subtest: RBC4 Reading view matches Live Preview ＋ / ×
ok 441 - RBC4 Reading view matches Live Preview ＋ / ×
  ---
  duration_ms: 3.850733
  ...
# Subtest: setup subscribes to the command-mode run-finished workspace event
ok 442 - setup subscribes to the command-mode run-finished workspace event
  ---
  duration_ms: 1.237684
  ...
# Subtest: each invalidates tag refreshes its ledger cache and unknown tags are ignored
ok 443 - each invalidates tag refreshes its ledger cache and unknown tags are ignored
  ---
  duration_ms: 1.048432
  ...
# Subtest: duplicate tags refresh once and a failing hook never blocks the others
ok 444 - duplicate tags refresh once and a failing hook never blocks the others
  ---
  duration_ms: 0.299502
  ...
# Subtest: payloads without invalidates and setups without a workspace never throw
ok 445 - payloads without invalidates and setups without a workspace never throw
  ---
  duration_ms: 0.340521
  ...
# Subtest: collections namespace version is additive v1
ok 446 - collections namespace version is additive v1
  ---
  duration_ms: 0.884198
  ...
# Subtest: collection chip classes stay collection-specific through paint and refresh
ok 447 - collection chip classes stay collection-specific through paint and refresh
  ---
  duration_ms: 2.481668
  ...
# Subtest: projects: scalar resolved links count, lists never widen
ok 448 - projects: scalar resolved links count, lists never widen
  ---
  duration_ms: 0.278161
  ...
# Subtest: projects: templates, status, and containsAny edges
ok 449 - projects: templates, status, and containsAny edges
  ---
  duration_ms: 0.294783
  ...
# Subtest: references: exact prefix, md only, exact scalar status
ok 450 - references: exact prefix, md only, exact scalar status
  ---
  duration_ms: 0.228176
  ...
# Subtest: base contracts: accept current files, reject drift, tolerate presentation
ok 451 - base contracts: accept current files, reject drift, tolerate presentation
  ---
  duration_ms: 0.555601
  ...
# Subtest: entries: true zero vs unavailable with reason, failure isolation
ok 452 - entries: true zero vs unavailable with reason, failure isolation
  ---
  duration_ms: 0.204
  ...
# Subtest: snapshot counts both collections once, true zero stays clickable
ok 453 - snapshot counts both collections once, true zero stays clickable
  ---
  duration_ms: 0.333958
  ...
# Subtest: snapshot never presents partial counts as final
ok 454 - snapshot never presents partial counts as final
  ---
  duration_ms: 0.344037
  ...
# Subtest: changed definitions fail closed per collection, never stale
ok 455 - changed definitions fail closed per collection, never stale
  ---
  duration_ms: 0.428729
  ...
# Subtest: renderChip links, labels, and cleans up per component
ok 456 - renderChip links, labels, and cleans up per component
  ---
  duration_ms: 0.523279
  ...
# Subtest: PENDING section excludes TODAY while the whole lane keeps it
ok 457 - PENDING section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 2.400935
  ...
# Subtest: NEXT section excludes TODAY while the whole lane keeps it
ok 458 - NEXT section excludes TODAY while the whole lane keeps it
  ---
  duration_ms: 0.380907
  ...
# Subtest: NEXT uses symbol *, not name matching
ok 459 - NEXT uses symbol *, not name matching
  ---
  duration_ms: 0.255368
  ...
# Subtest: READY badge and query agree on hide and path case variants
ok 460 - READY badge and query agree on hide and path case variants
  ---
  duration_ms: 0.527477
  ...
# Subtest: blocked uses the full list even outside the visible subset
ok 461 - blocked uses the full list even outside the visible subset
  ---
  duration_ms: 0.195583
  ...
# Subtest: duplicate block IDs, missing IDs, and reused objects stay per-row
ok 462 - duplicate block IDs, missing IDs, and reused objects stay per-row
  ---
  duration_ms: 0.216794
  ...
# Subtest: READY gating keeps exempt rows and drops NEW/ROTTEN
ok 463 - READY gating keeps exempt rows and drops NEW/ROTTEN
  ---
  duration_ms: 0.281528
  ...
# Subtest: throwing Today degrades to unavailable, never zero
ok 464 - throwing Today degrades to unavailable, never zero
  ---
  duration_ms: 8.617569
  ...
# Subtest: dashboard badges color the displayed section count and label whole-lane pressure
ok 465 - dashboard badges color the displayed section count and label whole-lane pressure
  ---
  duration_ms: 0.61282
  ...
# Subtest: dashboard section warning boundaries ignore TODAY-only whole-lane excess
ok 466 - dashboard section warning boundaries ignore TODAY-only whole-lane excess
  ---
  duration_ms: 0.787323
  ...
# Subtest: dashboard lane badge keeps unavailable data neutral
ok 467 - dashboard lane badge keeps unavailable data neutral
  ---
  duration_ms: 0.257872
  ...
# Subtest: dashboard lane paint and refresh keep color aligned with the visible section
ok 468 - dashboard lane paint and refresh keep color aligned with the visible section
  ---
  duration_ms: 2.650752
  ...
# Subtest: dashboard lane widgets refresh together and prune on unload
ok 469 - dashboard lane widgets refresh together and prune on unload
  ---
  duration_ms: 1.968959
  ...
# Subtest: daily paint matches dashboard section badges on screenshot fixtures
ok 470 - daily paint matches dashboard section badges on screenshot fixtures
  ---
  duration_ms: 20.012799
  ...
# Subtest: daily paint lane lint matches a red badge section count
ok 471 - daily paint lane lint matches a red badge section count
  ---
  duration_ms: 5.089449
  ...
# Subtest: daily and dashboard membership agree for exclusions and custom IN_PROGRESS
ok 472 - daily and dashboard membership agree for exclusions and custom IN_PROGRESS
  ---
  duration_ms: 3.622889
  ...
# Subtest: daily paint refreshes with dashboard when Today, lane, and cap change
ok 473 - daily paint refreshes with dashboard when Today, lane, and cap change
  ---
  duration_ms: 7.057447
  ...
# Subtest: older daily notes follow today's dashboard lanes
ok 474 - older daily notes follow today's dashboard lanes
  ---
  duration_ms: 5.793984
  ...
# Subtest: daily lane anchors keep shared navigation and reject stale paints
ok 475 - daily lane anchors keep shared navigation and reject stale paints
  ---
  duration_ms: 4.07308
  ...
# Subtest: daily paint stays unavailable until Tasks and Today are ready
ok 476 - daily paint stays unavailable until Tasks and Today are ready
  ---
  duration_ms: 2.104239
  ...
# Subtest: work tones: dashboard lane models carry section tones
ok 477 - work tones: dashboard lane models carry section tones
  ---
  duration_ms: 0.243676
  ...
# Subtest: T1 scheduled full-mode row gets a Fri mark inside the span
ok 478 - T1 scheduled full-mode row gets a Fri mark inside the span
  ---
  duration_ms: 2.713883
  ...
# Subtest: T2 done row maps to a completion Oct 5 mark
ok 479 - T2 done row maps to a completion Oct 5 mark
  ---
  duration_ms: 0.474647
  ...
# Subtest: T3 short-mode created span is left untouched by JS
ok 480 - T3 short-mode created span is left untouched by JS
  ---
  duration_ms: 0.281588
  ...
# Subtest: T4 pending row decorates once data-task appears; exhausted rows stay native
ok 481 - T4 pending row decorates once data-task appears; exhausted rows stay native
  ---
  duration_ms: 0.957759
  ...
# Subtest: T5 a second pass adds nothing
ok 482 - T5 a second pass adds nothing
  ---
  duration_ms: 0.269535
  ...
# Subtest: T6 task-due and task-start spans are untouched
ok 483 - T6 task-due and task-start spans are untouched
  ---
  duration_ms: 0.237243
  ...
# Subtest: T7 an invalid date is untouched
ok 484 - T7 an invalid date is untouched
  ---
  duration_ms: 0.26186
  ...
# Subtest: T8 nothing is scheduled with marks off or for connected non-Tasks elements
ok 485 - T8 nothing is scheduled with marks off or for connected non-Tasks elements
  ---
  duration_ms: 0.26157
  ...
# Subtest: T9 a Tasks-host Fri mark relabels to tomorrow on rollover
ok 486 - T9 a Tasks-host Fri mark relabels to tomorrow on rollover
  ---
  duration_ms: 0.670902
  ...
# Subtest: renderDateMarksIn schedules one shared frame for every row
ok 487 - renderDateMarksIn schedules one shared frame for every row
  ---
  duration_ms: 0.972066
  ...
# Subtest: the Tasks pass never throws on hostile input
ok 488 - the Tasks pass never throws on hostile input
  ---
  duration_ms: 0.423148
  ...
# Subtest: T10 real-DOM NodeList children decorate via direct and queued passes
ok 489 - T10 real-DOM NodeList children decorate via direct and queued passes
  ---
  duration_ms: 0.550432
  ...
# Subtest: T11 toggling off before a queued frame runs writes nothing
ok 490 - T11 toggling off before a queued frame runs writes nothing
  ---
  duration_ms: 0.496599
  ...
# Subtest: T12 a pending-row retry followed by disabling writes nothing
ok 491 - T12 a pending-row retry followed by disabling writes nothing
  ---
  duration_ms: 0.338407
  ...
# Subtest: T13 unloading before a callback runs writes nothing
ok 492 - T13 unloading before a callback runs writes nothing
  ---
  duration_ms: 1.135699
  ...
# Subtest: RT1 full-mode recurring result gets a daily mark and stays idempotent
ok 493 - RT1 full-mode recurring result gets a daily mark and stays idempotent
  ---
  duration_ms: 0.977507
  ...
# Subtest: RT2 recurring labels use the shared cadence grammar
ok 494 - RT2 recurring labels use the shared cadence grammar
  ---
  duration_ms: 0.973549
  ...
# Subtest: RT2a unknown inherited-name rules stay readable in Tasks results
ok 495 - RT2a unknown inherited-name rules stay readable in Tasks results
  ---
  duration_ms: 0.389995
  ...
# Subtest: RT3 short-mode recurring spans stay native to JS and use the CSS loop
ok 496 - RT3 short-mode recurring spans stay native to JS and use the CSS loop
  ---
  duration_ms: 2.455309
  ...
# Subtest: RT4 open checklist members keep recurrence pills without `when done`
ok 497 - RT4 open checklist members keep recurrence pills without `when done`
  ---
  duration_ms: 0.46046
  ...
# Subtest: RT5 invalid recurrence stays native and incomplete rows are retried
ok 498 - RT5 invalid recurrence stays native and incomplete rows are retried
  ---
  duration_ms: 0.367662
  ...
# Subtest: styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
ok 499 - styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs
  ---
  duration_ms: 0.68587
  ...
# Subtest: DATE_MARK_FIELDS lists the four dates with verbs
ok 500 - DATE_MARK_FIELDS lists the four dates with verbs
  ---
  duration_ms: 1.80116
  ...
# Subtest: DM1 created today: label, tooltip, fold, quiet field
ok 501 - DM1 created today: label, tooltip, fold, quiet field
  ---
  duration_ms: 1.287478
  ...
# Subtest: DM2 created yesterday without space after the colons
ok 502 - DM2 created yesterday without space after the colons
  ---
  duration_ms: 0.379225
  ...
# Subtest: DM3-DM6 scheduled tomorrow, weekday, and month/day labels
ok 503 - DM3-DM6 scheduled tomorrow, weekday, and month/day labels
  ---
  duration_ms: 0.23558
  ...
# Subtest: DM7 scheduled today reads with emphasis timing
ok 504 - DM7 scheduled today reads with emphasis timing
  ---
  duration_ms: 0.2932
  ...
# Subtest: DM8 past scheduled uses month/day, never a weekday
ok 505 - DM8 past scheduled uses month/day, never a weekday
  ---
  duration_ms: 0.170987
  ...
# Subtest: DM9 completion on a closed task keeps the timeline grammar
ok 506 - DM9 completion on a closed task keeps the timeline grammar
  ---
  duration_ms: 0.208919
  ...
# Subtest: DM10 cancelled across years appends the year
ok 507 - DM10 cancelled across years appends the year
  ---
  duration_ms: 0.140188
  ...
# Subtest: DM11 next-year date appends the year
ok 508 - DM11 next-year date appends the year
  ---
  duration_ms: 0.318258
  ...
# Subtest: DM12 the weekday rule wins across the year boundary
ok 509 - DM12 the weekday rule wins across the year boundary
  ---
  duration_ms: 0.390606
  ...
# Subtest: DM13 two marks in order with folds 1 and 2
ok 510 - DM13 two marks in order with folds 1 and 2
  ---
  duration_ms: 0.443216
  ...
# Subtest: DM14 created and scheduled ranges stay disjoint from the fresh mark
ok 511 - DM14 created and scheduled ranges stay disjoint from the fresh mark
  ---
  duration_ms: 0.29889
  ...
# Subtest: DM15-DM16 paren and padded brackets are canonical
ok 512 - DM15-DM16 paren and padded brackets are canonical
  ---
  duration_ms: 0.185464
  ...
# Subtest: DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
ok 513 - DM17-DM21 line shapes: bullets, quotes, and paragraphs mark
  ---
  duration_ms: 0.36109
  ...
# Subtest: DM22 code still parses pure but decorates nothing (see Live Preview)
ok 514 - DM22 code still parses pure but decorates nothing (see Live Preview)
  ---
  duration_ms: 0.101364
  ...
# Subtest: DM23 rescheduled is untouched and never a duplicate
ok 515 - DM23 rescheduled is untouched and never a duplicate
  ---
  duration_ms: 0.184282
  ...
# Subtest: DN1-DN9 non-canonical fields get no mark
ok 516 - DN1-DN9 non-canonical fields get no mark
  ---
  duration_ms: 0.274073
  ...
# Subtest: dateMarkContentStart finds content on list, quoted, and plain lines
ok 517 - dateMarkContentStart finds content on list, quoted, and plain lines
  ---
  duration_ms: 0.124939
  ...
# Subtest: dateMarkRelativePhrase covers the exact-day phrases
ok 518 - dateMarkRelativePhrase covers the exact-day phrases
  ---
  duration_ms: 0.134086
  ...
# Subtest: dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
ok 519 - dateMarkModel rejects unknown fields and bad dates, and falls back on bad today
  ---
  duration_ms: 0.383232
  ...
# Subtest: no model output contains a double colon
ok 520 - no model output contains a double colon
  ---
  duration_ms: 1.359055
  ...
# Subtest: a new day always changes the widget key
ok 521 - a new day always changes the widget key
  ---
  duration_ms: 0.176507
  ...
# Subtest: element structure and the decorative/inheritColor/rendered options
ok 522 - element structure and the decorative/inheritColor/rendered options
  ---
  duration_ms: 0.480919
  ...
# Subtest: Live Preview emits several decorations in ascending order
ok 523 - Live Preview emits several decorations in ascending order
  ---
  duration_ms: 1.536594
  ...
# Subtest: Live Preview reveals per field, never the whole line
ok 524 - Live Preview reveals per field, never the whole line
  ---
  duration_ms: 0.302808
  ...
# Subtest: Live Preview refuses source mode, code, and disabled marks
ok 525 - Live Preview refuses source mode, code, and disabled marks
  ---
  duration_ms: 0.453446
  ...
# Subtest: widget mousedown anchors at the field start for folds 0, 1, and 2
ok 526 - widget mousedown anchors at the field start for folds 0, 1, and 2
  ---
  duration_ms: 0.995271
  ...
# Subtest: DM24 a cursor in the folded run unfolds the mark (vim cw)
ok 527 - DM24 a cursor in the folded run unfolds the mark (vim cw)
  ---
  duration_ms: 0.307537
  ...
# Subtest: DM25 a cursor in Tasks double space unfolds only that field
ok 528 - DM25 a cursor in Tasks double space unfolds only that field
  ---
  duration_ms: 0.186386
  ...
# Subtest: a selection ending inside the run unfolds; ending at its start keeps the fold
ok 529 - a selection ending inside the run unfolds; ending at its start keeps the fold
  ---
  duration_ms: 0.199231
  ...
# Subtest: no emitted decoration ever hides a cursor, and reveal still means field overlap
ok 530 - no emitted decoration ever hides a cursor, and reveal still means field overlap
  ---
  duration_ms: 10.505635
  ...
# Subtest: dateMarkSelectionFold: reveal, unfold, fold, and garbage input
ok 531 - dateMarkSelectionFold: reveal, unfold, fold, and garbage input
  ---
  duration_ms: 0.285014
  ...
# Subtest: mousedown on an unfolded (fold-0) widget anchors at the field start
ok 532 - mousedown on an unfolded (fold-0) widget anchors at the field start
  ---
  duration_ms: 0.470729
  ...
# Subtest: rendered views split several fields in one node
ok 533 - rendered views split several fields in one node
  ---
  duration_ms: 2.114398
  ...
# Subtest: rendered views skip exclusions and duplicates
ok 534 - rendered views skip exclusions and duplicates
  ---
  duration_ms: 0.724384
  ...
# Subtest: RO1 rendered marks relabel in place across midnight
ok 535 - RO1 rendered marks relabel in place across midnight
  ---
  duration_ms: 0.665922
  ...
# Subtest: rollover dispatches once per day change and never touches widgets
ok 536 - rollover dispatches once per day change and never touches widgets
  ---
  duration_ms: 0.483243
  ...
# Subtest: api.dateMarks v1 is additive, sync, and never throwing
ok 537 - api.dateMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.648759
  ...
# Subtest: session toggle and onload wiring
ok 538 - session toggle and onload wiring
  ---
  duration_ms: 7.793903
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 539 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 0.57038
  ...
# Subtest: styles.css contract: masks, tones, repair flag, resting
ok 540 - styles.css contract: masks, tones, repair flag, resting
  ---
  duration_ms: 1.130469
  ...
# Subtest: day identity follows the canonical path, never the tab or mtime
ok 541 - day identity follows the canonical path, never the tab or mtime
  ---
  duration_ms: 1.814044
  ...
# Subtest: fence day parsing accepts YAML mappings and plain lines, nothing else
ok 542 - fence day parsing accepts YAML mappings and plain lines, nothing else
  ---
  duration_ms: 0.721297
  ...
# Subtest: report selection reads the default entry, an 8-day range, or nothing
ok 543 - report selection reads the default entry, an 8-day range, or nothing
  ---
  duration_ms: 8.999077
  ...
# Subtest: report window checks keep the page window only when it shows D
ok 544 - report window checks keep the page window only when it shows D
  ---
  duration_ms: 1.875912
  ...
# Subtest: paint from cache costs one frame and zero spawns
ok 545 - paint from cache costs one frame and zero spawns
  ---
  duration_ms: 43.145884
  ...
# Subtest: off-screen and hidden-tab strips spawn nothing
ok 546 - off-screen and hidden-tab strips spawn nothing
  ---
  duration_ms: 136.738098
  ...
# Subtest: clean fresh entries never refetch, whatever changes
ok 547 - clean fresh entries never refetch, whatever changes
  ---
  duration_ms: 98.988337
  ...
# Subtest: visible changing strips spawn at most once per 30 s
ok 548 - visible changing strips spawn at most once per 30 s
  ---
  duration_ms: 191.034587
  ...
# Subtest: the 10-minute age rule refetches today without any change
ok 549 - the 10-minute age rule refetches today without any change
  ---
  duration_ms: 66.242232
  ...
# Subtest: past days wait out the 10-minute gate
ok 550 - past days wait out the 10-minute gate
  ---
  duration_ms: 90.620969
  ...
# Subtest: several strips and the page share one spawn per key
ok 551 - several strips and the page share one spawn per key
  ---
  duration_ms: 67.558306
  ...
# Subtest: strips repaint for free when the page refreshes the shared key
ok 552 - strips repaint for free when the page refreshes the shared key
  ---
  duration_ms: 99.202375
  ...
# Subtest: rollover re-keys today to a past day and refetches
ok 553 - rollover re-keys today to a past day and refetches
  ---
  duration_ms: 99.072972
  ...
# Subtest: a stale-across-midnight report is never shown as so far
ok 554 - a stale-across-midnight report is never shown as so far
  ---
  duration_ms: 69.819973
  ...
# Subtest: window-edge days fetch the 8-day range
ok 555 - window-edge days fetch the 8-day range
  ---
  duration_ms: 62.777967
  ...
# Subtest: future days render nothing and spawn nothing
ok 556 - future days render nothing and spawn nothing
  ---
  duration_ms: 22.630398
  ...
# Subtest: a failed refresh keeps the frame and shows the stale dot
ok 557 - a failed refresh keeps the frame and shows the stale dot
  ---
  duration_ms: 99.593134
  ...
# Subtest: a failure with nothing cached shows the one-line error and Retry
ok 558 - a failure with nothing cached shows the one-line error and Retry
  ---
  duration_ms: 124.805289
  ...
# Subtest: bob-not-found with nothing cached names stats.bob_path
ok 559 - bob-not-found with nothing cached names stats.bob_path
  ---
  duration_ms: 62.493142
  ...
# Subtest: the fence parses day:, falls back to the note date, or explains itself
ok 560 - the fence parses day:, falls back to the note date, or explains itself
  ---
  duration_ms: 87.461595
  ...
# Subtest: the fence skips hover popovers and embeds, and unregisters on unload
ok 561 - the fence skips hover popovers and embeds, and unregisters on unload
  ---
  duration_ms: 3.623779
  ...
# Subtest: openStatsForDay pins the day, focuses the metric, and opens a new tab
ok 562 - openStatsForDay pins the day, focuses the metric, and opens a new tab
  ---
  duration_ms: 1.534881
  ...
# Subtest: openStatsForDay opens a new tab when Stats is already open
ok 563 - openStatsForDay opens a new tab when Stats is already open
  ---
  duration_ms: 0.825727
  ...
# Subtest: openStatsForDay keeps the page window when it already shows D
ok 564 - openStatsForDay keeps the page window when it already shows D
  ---
  duration_ms: 62.615318
  ...
# Subtest: openStatsForDay panel themes selects the Themes view
ok 565 - openStatsForDay panel themes selects the Themes view
  ---
  duration_ms: 61.648751
  ...
# Subtest: openStatsForDay Notices when Stats cannot open
ok 566 - openStatsForDay Notices when Stats cannot open
  ---
  duration_ms: 1.181065
  ...
# Subtest: the page honours a pinned day on its first paint
ok 567 - the page honours a pinned day on its first paint
  ---
  duration_ms: 62.461241
  ...
# Subtest: renderStatsResult consumes the one-shot revealPanel
ok 568 - renderStatsResult consumes the one-shot revealPanel
  ---
  duration_ms: 5.605234
  ...
# Subtest: every strip paints facts and links with no buttons and no vault writes
ok 569 - every strip paints facts and links with no buttons and no vault writes
  ---
  duration_ms: 63.321645
  ...
# Subtest: change bursts coalesce behind one trailing quiet window
ok 570 - change bursts coalesce behind one trailing quiet window
  ---
  duration_ms: 113.858565
  ...
# Subtest: mobile and spawn-less hosts render nothing and spawn nothing
ok 571 - mobile and spawn-less hosts render nothing and spawn nothing
  ---
  duration_ms: 31.516186
  ...
# Subtest: rollover synchronously skeletons visible and offscreen fences; visible refetch resolves as past
ok 572 - rollover synchronously skeletons visible and offscreen fences; visible refetch resolves as past
  ---
  duration_ms: 180.649428
  ...
# Subtest: fit observer registers once, refits on width change, and releases
ok 573 - fit observer registers once, refits on width change, and releases
  ---
  duration_ms: 1.500135
  ...
# Subtest: missing ResizeObserver is harmless
ok 574 - missing ResizeObserver is harmless
  ---
  duration_ms: 0.219479
  ...
# Subtest: require time adds no eager StateEffect.define()
ok 575 - require time adds no eager StateEffect.define()
  ---
  duration_ms: 1.029967
  ...
# Subtest: renderPlanBlock puts exactly one host first with .bob-plan after it on canonical days
ok 576 - renderPlanBlock puts exactly one host first with .bob-plan after it on canonical days
  ---
  duration_ms: 76.665407
  ...
# Subtest: non-daily, future, dashboard, mobile, spawn-less, and excluded blocks get no host
ok 577 - non-daily, future, dashboard, mobile, spawn-less, and excluded blocks get no host
  ---
  duration_ms: 219.56314
  ...
# Subtest: paintPlanBlock keeps the same host node first with .bob-plan after it and no strip repaint or spawn
ok 578 - paintPlanBlock keeps the same host node first with .bob-plan after it and no strip repaint or spawn
  ---
  duration_ms: 254.122016
  ...
# Subtest: toggle and stats.day_strip remove the host and class, re-enabling restores them
ok 579 - toggle and stats.day_strip remove the host and class, re-enabling restores them
  ---
  duration_ms: 108.368268
  ...
# Subtest: unload releases the record and its observer
ok 580 - unload releases the record and its observer
  ---
  duration_ms: 33.592723
  ...
# Subtest: rollover attaches future blocks and repaints today as a past day
ok 581 - rollover attaches future blocks and repaints today as a past day
  ---
  duration_ms: 95.029688
  ...
# Subtest: rollover skeletons a visible automatic today host synchronously; it resolves as past
ok 582 - rollover skeletons a visible automatic today host synchronously; it resolves as past
  ---
  duration_ms: 218.29259
  ...
# Subtest: plan hosts never write the vault or journals
ok 583 - plan hosts never write the vault or journals
  ---
  duration_ms: 125.87752
  ...
# Subtest: cold plan host waits for visibility: no spawn before callback, false stays zero, true fetches once
ok 584 - cold plan host waits for visibility: no spawn before callback, false stays zero, true fetches once
  ---
  duration_ms: 156.639121
  ...
# Subtest: plan host paints synchronously from cache with zero spawn before visibility
ok 585 - plan host paints synchronously from cache with zero spawn before visibility
  ---
  duration_ms: 33.90577
  ...
# Subtest: detached excluded blocks get no host; detached ordinary blocks attach synchronously
ok 586 - detached excluded blocks get no host; detached ordinary blocks attach synchronously
  ---
  duration_ms: 187.83546
  ...
# Subtest: no-observer fallback attaches detached, fetches on check after connect, releases excluded
ok 587 - no-observer fallback attaches detached, fetches on check after connect, releases excluded
  ---
  duration_ms: 253.418221
  ...
# Subtest: excluded after attach releases on the first observer callback
ok 588 - excluded after attach releases on the first observer callback
  ---
  duration_ms: 188.547667
  ...
# Subtest: excluded processor container gets no host
ok 589 - excluded processor container gets no host
  ---
  duration_ms: 32.091445
  ...
# Subtest: reading-view order attaches detached, virtualized stays quiet until attach
ok 590 - reading-view order attaches detached, virtualized stays quiet until attach
  ---
  duration_ms: 157.188383
  ...
# Subtest: today host shows so far HH:MM from the fetch stamp
ok 591 - today host shows so far HH:MM from the fetch stamp
  ---
  duration_ms: 114.761309
  ...
# Subtest: failed refresh over a cached report names the HH:MM it shows
ok 592 - failed refresh over a cached report names the HH:MM it shows
  ---
  duration_ms: 174.595624
  ...
# Subtest: placeholder finds .bob-plan by class and toggle-off restores it first
ok 593 - placeholder finds .bob-plan by class and toggle-off restores it first
  ---
  duration_ms: 64.334699
  ...
# Subtest: statsThemeRef prefers theme_hues names and hues, with gray fallbacks
ok 594 - statsThemeRef prefers theme_hues names and hues, with gray fallbacks
  ---
  duration_ms: 1.500025
  ...
# Subtest: theme mix orders coloured by minutes then gray, with unnamed last
ok 595 - theme mix orders coloured by minutes then gray, with unnamed last
  ---
  duration_ms: 9.864438
  ...
# Subtest: same-hue coloured themes take shade 0 then 1 then 2; gray is never shaded
ok 596 - same-hue coloured themes take shade 0 then 1 then 2; gray is never shaded
  ---
  duration_ms: 0.677053
  ...
# Subtest: theme mix labels, ranks, overflow, titles, and aria follow the report
ok 597 - theme mix labels, ranks, overflow, titles, and aria follow the report
  ---
  duration_ms: 2.418588
  ...
# Subtest: theme lane is omitted for zero days, missing parts, and redefined worked
ok 598 - theme lane is omitted for zero days, missing parts, and redefined worked
  ---
  duration_ms: 5.876913
  ...
# Subtest: fallback hue uses context.themeHueFor and stays gray without it
ok 599 - fallback hue uses context.themeHueFor and stays gray without it
  ---
  duration_ms: 0.281808
  ...
# Subtest: painter uses swatches, shades, data-lane, and no buttons on the theme lane
ok 600 - painter uses swatches, shades, data-lane, and no buttons on the theme lane
  ---
  duration_ms: 1.609263
  ...
# Subtest: theme legend and bar open Stats on the Themes view
ok 601 - theme legend and bar open Stats on the Themes view
  ---
  duration_ms: 1.962137
  ...
# Subtest: fitter fits both legends independently and returns the roots result
ok 602 - fitter fits both legends independently and returns the roots result
  ---
  duration_ms: 2.957347
  ...
# Subtest: date words and day shifts use calendar integers, including leap day
ok 603 - date words and day shifts use calendar integers, including leap day
  ---
  duration_ms: 1.938312
  ...
# Subtest: fact displays are selected from the exact day point, even with null headline and grouped input
ok 604 - fact displays are selected from the exact day point, even with null headline and grouped input
  ---
  duration_ms: 7.27778
  ...
# Subtest: honest states carry meta text for today, past, stale today, and stale past
ok 605 - honest states carry meta text for today, past, stale today, and stale past
  ---
  duration_ms: 2.130368
  ...
# Subtest: time mix reuses Stats area ordering and hues, with buckets last and a tooltip title
ok 606 - time mix reuses Stats area ordering and hues, with buckets last and a tooltip title
  ---
  duration_ms: 18.089213
  ...
# Subtest: root_parent is preferred with an honest area fallback
ok 607 - root_parent is preferred with an honest area fallback
  ---
  duration_ms: 0.579787
  ...
# Subtest: zero worked renders no Pomodoros and redefined worked omits its mix
ok 608 - zero worked renders no Pomodoros and redefined worked omits its mix
  ---
  duration_ms: 2.112845
  ...
# Subtest: aria label carries the date, values, provisional state, and area names
ok 609 - aria label carries the date, values, provisional state, and area names
  ---
  duration_ms: 0.410163
  ...
# Subtest: skeleton carries placeholder text per fact and the same tag and class sequence
ok 610 - skeleton carries placeholder text per fact and the same tag and class sequence
  ---
  duration_ms: 4.625876
  ...
# Subtest: painter repaints in place, emits no buttons, and shows unavailable controls
ok 611 - painter repaints in place, emits no buttons, and shows unavailable controls
  ---
  duration_ms: 4.566922
  ...
# Subtest: facts, mix, and Retry preserve day, focus, and new-leaf modifiers
ok 612 - facts, mix, and Retry preserve day, focus, and new-leaf modifiers
  ---
  duration_ms: 2.506386
  ...
# Subtest: future and hidden models paint no children
ok 613 - future and hidden models paint no children
  ---
  duration_ms: 0.3246
  ...
# Subtest: strip paints facts, legend row, then full-width bar with no buttons
ok 614 - strip paints facts, legend row, then full-width bar with no buttons
  ---
  duration_ms: 2.316553
  ...
# Subtest: bar click opens Stats homes with day and new-leaf modifiers
ok 615 - bar click opens Stats homes with day and new-leaf modifiers
  ---
  duration_ms: 2.208047
  ...
# Subtest: same-area roots get distinct hues and legend dots match their segments
ok 616 - same-area roots get distinct hues and legend dots match their segments
  ---
  duration_ms: 2.312797
  ...
# Subtest: dayStripValueRuns splits numerals from units and keeps words whole
ok 617 - dayStripValueRuns splits numerals from units and keeps words whole
  ---
  duration_ms: 0.704455
  ...
# Subtest: facts stack a label head over a faithful value with warnings in the head
ok 618 - facts stack a label head over a faithful value with warnings in the head
  ---
  duration_ms: 27.108589
  ...
# Subtest: short_label paints GTD with a full-label tooltip
ok 619 - short_label paints GTD with a full-label tooltip
  ---
  duration_ms: 3.044884
  ...
# Subtest: area roots paint the bare label with a project_label tooltip
ok 620 - area roots paint the bare label with a project_label tooltip
  ---
  duration_ms: 1.068972
  ...
# Subtest: case-insensitive legend collisions fall back to full labels
ok 621 - case-insensitive legend collisions fall back to full labels
  ---
  duration_ms: 1.341231
  ...
# Subtest: dayStripLegendFit fits every root, reserves the counter, and handles empty
ok 622 - dayStripLegendFit fits every root, reserves the counter, and handles empty
  ---
  duration_ms: 0.378613
  ...
# Subtest: names mode wins only when it names strictly more roots
ok 623 - names mode wins only when it names strictly more roots
  ---
  duration_ms: 0.191666
  ...
# Subtest: DOM glue hides overflow, writes the counter, and toggles names mode
ok 624 - DOM glue hides overflow, writes the counter, and toggles names mode
  ---
  duration_ms: 2.322626
  ...
# Subtest: dayStripMarkState maps bool points from the bob point, never the word
ok 625 - dayStripMarkState maps bool points from the bob point, never the word
  ---
  duration_ms: 0.506237
  ...
# Subtest: boolean facts paint an aria-hidden mark with hidden display text
ok 626 - boolean facts paint an aria-hidden mark with hidden display text
  ---
  duration_ms: 3.304922
  ...
# Subtest: docs without createElementNS keep word runs
ok 627 - docs without createElementNS keep word runs
  ---
  duration_ms: 1.313339
  ...
# Subtest: bool skeleton paints a round placeholder and no svg
ok 628 - bool skeleton paints a round placeholder and no svg
  ---
  duration_ms: 1.423939
  ...
# Subtest: pending mark tooltip drops so far; numeric provisional keeps it
ok 629 - pending mark tooltip drops so far; numeric provisional keeps it
  ---
  duration_ms: 0.398872
  ...
# Subtest: pending to met on the same host and day draws the check once
ok 630 - pending to met on the same host and day draws the check once
  ---
  duration_ms: 2.814464
  ...
# Subtest: arrive class stays off for other mark transitions
ok 631 - arrive class stays off for other mark transitions
  ---
  duration_ms: 5.988045
  ...
# Subtest: stroke-dashoffset lives only inside keyframes
ok 632 - stroke-dashoffset lives only inside keyframes
  ---
  duration_ms: 1.374585
  ...
# Subtest: DP parse vectors
ok 633 - DP parse vectors
  ---
  duration_ms: 3.415924
  ...
# Subtest: DC chip model vectors
ok 634 - DC chip model vectors
  ---
  duration_ms: 2.06261
  ...
# Subtest: decoration builds one widget, reveals on cursor, skips code and ranges
ok 635 - decoration builds one widget, reveals on cursor, skips code and ranges
  ---
  duration_ms: 9.561979
  ...
# Subtest: decoration skips paragraphs, grandchildren, and Work Log lines
ok 636 - decoration skips paragraphs, grandchildren, and Work Log lines
  ---
  duration_ms: 0.948271
  ...
# Subtest: decoration renders chips on DP30 and still skips DP20
ok 637 - decoration renders chips on DP30 and still skips DP20
  ---
  duration_ms: 1.117544
  ...
# Subtest: ownership check reads O(depth) lines, not the whole note
ok 638 - ownership check reads O(depth) lines, not the whole note
  ---
  duration_ms: 13.383467
  ...
# Subtest: widget identity covers the line and the interactive flag
ok 639 - widget identity covers the line and the interactive flag
  ---
  duration_ms: 4.284013
  ...
# Subtest: element hides actions without nav api v1
ok 640 - element hides actions without nav api v1
  ---
  duration_ms: 0.94206
  ...
# Subtest: nav api feature detection gates actions
ok 641 - nav api feature detection gates actions
  ---
  duration_ms: 0.579247
  ...
# Subtest: reading view decorates only the Depends-On row, hides chrome, stays idempotent
ok 642 - reading view decorates only the Depends-On row, hides chrome, stays idempotent
  ---
  duration_ms: 4.705817
  ...
# Subtest: reading view collapses more than three Done targets to one chip
ok 643 - reading view collapses more than three Done targets to one chip
  ---
  duration_ms: 2.174763
  ...
# Subtest: DC chip model vectors by id: DC2, DC5, DC6, DC9
ok 644 - DC chip model vectors by id: DC2, DC5, DC6, DC9
  ---
  duration_ms: 0.474707
  ...
# Subtest: chip actions send the 0-based line index through nav api v1
ok 645 - chip actions send the 0-based line index through nav api v1
  ---
  duration_ms: 6.326721
  ...
# Subtest: chip hover passes the chip element and its row to the preview
ok 646 - chip hover passes the chip element and its row to the preview
  ---
  duration_ms: 0.231151
  ...
# Subtest: chip lookup index lives on the freshness memo
ok 647 - chip lookup index lives on the freshness memo
  ---
  duration_ms: 0.621407
  ...
# Subtest: reading view hides actions when the line cannot be derived
ok 648 - reading view hides actions when the line cannot be derived
  ---
  duration_ms: 14.626193
  ...
# Subtest: reading view actions carry the derived 0-based line
ok 649 - reading view actions carry the derived 0-based line
  ---
  duration_ms: 3.183078
  ...
# Subtest: reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
ok 650 - reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows
  ---
  duration_ms: 0.825226
  ...
# Subtest: reading view renders chips on DP30 (owner is a task under a Work Log entry)
ok 651 - reading view renders chips on DP30 (owner is a task under a Work Log entry)
  ---
  duration_ms: 0.854432
  ...
# Subtest: reading view DP30 row actions send the owned Depends-On line
ok 652 - reading view DP30 row actions send the owned Depends-On line
  ---
  duration_ms: 7.319988
  ...
# Subtest: reading view second-row remove sends the second line when two tasks share a prerequisite
ok 653 - reading view second-row remove sends the second line when two tasks share a prerequisite
  ---
  duration_ms: 2.285995
  ...
# Subtest: chip lookup index builds once per freshness memo
ok 654 - chip lookup index builds once per freshness memo
  ---
  duration_ms: 0.629151
  ...
# Subtest: decoration evaluates ownership without copying the note
ok 655 - decoration evaluates ownership without copying the note
  ---
  duration_ms: 0.612029
  ...
# Subtest: toggle flips the body class and onload wires chips
ok 656 - toggle flips the body class and onload wires chips
  ---
  duration_ms: 7.918103
  ...
# Subtest: regression FakeNode hides the plan-host cycles and builds 85 nodes
ok 657 - regression FakeNode hides the plan-host cycles and builds 85 nodes
  ---
  duration_ms: 3.833491
  ...
# Subtest: failing assert.equal and assert.deepEqual report under a 1024MB cap
ok 658 - failing assert.equal and assert.deepEqual report under a 1024MB cap
  ---
  duration_ms: 243.526811
  ...
# Subtest: every ledger-tools FakeNode-style fake has a descriptor and hides its cyclic fields
ok 659 - every ledger-tools FakeNode-style fake has a descriptor and hides its cyclic fields
  ---
  duration_ms: 3.628761
  ...
# Subtest: capability: nav card v2 is capable
ok 660 - capability: nav card v2 is capable
  ---
  duration_ms: 1.273301
  ...
# Subtest: capability: nav card v1 is not capable
ok 661 - capability: nav card v1 is not capable
  ---
  duration_ms: 0.177048
  ...
# Subtest: capability: absent nav, missing api, and old versions are not capable
ok 662 - capability: absent nav, missing api, and old versions are not capable
  ---
  duration_ms: 0.148523
  ...
# Subtest: capability: a throwing app never throws
ok 663 - capability: a throwing app never throws
  ---
  duration_ms: 0.219038
  ...
# Subtest: leaf: active capable due choice replaces refresh with a leaf
ok 664 - leaf: active capable due choice replaces refresh with a leaf
  ---
  duration_ms: 2.964341
  ...
# Subtest: leaf: the same row without the card keeps refresh and counting words
ok 665 - leaf: the same row without the card keeps refresh and counting words
  ---
  duration_ms: 0.486278
  ...
# Subtest: leaf: early dates still leaf when capable
ok 666 - leaf: early dates still leaf when capable
  ---
  duration_ms: 0.44504
  ...
# Subtest: leaf: decay-off rows never leaf even when capable
ok 667 - leaf: decay-off rows never leaf even when capable
  ---
  duration_ms: 0.43488
  ...
# Subtest: leaf: below-threshold rows never leaf
ok 668 - leaf: below-threshold rows never leaf
  ---
  duration_ms: 0.589827
  ...
# Subtest: leaf: threshold zero asks on every due re-confirmation when capable
ok 669 - leaf: threshold zero asks on every due re-confirmation when capable
  ---
  duration_ms: 0.648439
  ...
# Subtest: leaf: overflow renders capped dots with +N and the exact count in text
ok 670 - leaf: overflow renders capped dots with +N and the exact count in text
  ---
  duration_ms: 0.367211
  ...
# Subtest: leaf: out-of-scope and closed tasks show dots quietly, never a leaf
ok 671 - leaf: out-of-scope and closed tasks show dots quietly, never a leaf
  ---
  duration_ms: 1.006552
  ...
# Subtest: leaf: unresolved marks show dots quietly with counting-only wording
ok 672 - leaf: unresolved marks show dots quietly with counting-only wording
  ---
  duration_ms: 0.28761
  ...
# Subtest: element: leaf marks carry data-decide true and a leaf path
ok 673 - element: leaf marks carry data-decide true and a leaf path
  ---
  duration_ms: 0.902523
  ...
# Subtest: element: non-decision marks carry data-decide false
ok 674 - element: non-decision marks carry data-decide false
  ---
  duration_ms: 0.332625
  ...
# Subtest: footer groups omit every zero tier and keep walk order
ok 675 - footer groups omit every zero tier and keep walk order
  ---
  duration_ms: 2.505555
  ...
# Subtest: PRE and POST groups bracket the nine-tier queue and expose completion hints
ok 676 - PRE and POST groups bracket the nine-tier queue and expose completion hints
  ---
  duration_ms: 1.188179
  ...
# Subtest: a NEW-state project appears only in its walk tier
ok 677 - a NEW-state project appears only in its walk tier
  ---
  duration_ms: 0.30373
  ...
# Subtest: empty queue hides the footer even with upkeep or a met budget
ok 678 - empty queue hides the footer even with upkeep or a met budget
  ---
  duration_ms: 0.229088
  ...
# Subtest: unavailable or missing data never render false counts
ok 679 - unavailable or missing data never render false counts
  ---
  duration_ms: 0.20415
  ...
# Subtest: generic summary names due, commitments, and nonempty groups
ok 680 - generic summary names due, commitments, and nonempty groups
  ---
  duration_ms: 0.425773
  ...
# Subtest: current-task context uses shared ranks and compact wording
ok 681 - current-task context uses shared ranks and compact wording
  ---
  duration_ms: 0.800649
  ...
# Subtest: only ROTTEN remaining names commitments done or a met budget
ok 682 - only ROTTEN remaining names commitments done or a met budget
  ---
  duration_ms: 0.360588
  ...
# Subtest: NEW and commitments take precedence over a met budget
ok 683 - NEW and commitments take precedence over a met budget
  ---
  duration_ms: 0.482341
  ...
# Subtest: reviewEntryView compact and detail cover the original freshness tiers
ok 684 - reviewEntryView compact and detail cover the original freshness tiers
  ---
  duration_ms: 2.997995
  ...
# Subtest: cursor matching requires a unique verified identity
ok 685 - cursor matching requires a unique verified identity
  ---
  duration_ms: 0.447514
  ...
# Subtest: footer paint hides the host and keeps a stable button
ok 686 - footer paint hides the host and keeps a stable button
  ---
  duration_ms: 1.381037
  ...
# Subtest: status bar 0-1-0 transitions hide without a reload
ok 687 - status bar 0-1-0 transitions hide without a reload
  ---
  duration_ms: 12.837196
  ...
# Subtest: cursor-only updates reuse a warm memo
ok 688 - cursor-only updates reuse a warm memo
  ---
  duration_ms: 3.060205
  ...
# Subtest: unload disconnects the observer and click handler
ok 689 - unload disconnects the observer and click handler
  ---
  duration_ms: 1.843421
  ...
# Subtest: queue-built ranks agree with the footer current entry
ok 690 - queue-built ranks agree with the footer current entry
  ---
  duration_ms: 1.127683
  ...
# Subtest: footer short labels map every tier
ok 691 - footer short labels map every tier
  ---
  duration_ms: 0.168622
  ...
# Subtest: current-row footer context uses short labels while entry views keep full labels
ok 692 - current-row footer context uses short labels while entry views keep full labels
  ---
  duration_ms: 0.815497
  ...
# Subtest: legend line lists only current abbreviated tiers
ok 693 - legend line lists only current abbreviated tiers
  ---
  duration_ms: 0.416776
  ...
# Subtest: queue-row quickRoll preview takes the hint slot, tooltip, and aria
ok 694 - queue-row quickRoll preview takes the hint slot, tooltip, and aria
  ---
  duration_ms: 0.72772
  ...
# Subtest: quickRoll detail sits next to the action hint on lane rows
ok 695 - quickRoll detail sits next to the action hint on lane rows
  ---
  duration_ms: 0.285646
  ...
# Subtest: missing, failed, or off-row quickRoll leaves the footer byte-identical
ok 696 - missing, failed, or off-row quickRoll leaves the footer byte-identical
  ---
  duration_ms: 5.193487
  ...
# Subtest: PRE rows stay unchanged under the nav checklist-tier contract
ok 697 - PRE rows stay unchanged under the nav checklist-tier contract
  ---
  duration_ms: 0.343726
  ...
# Subtest: status bar wires nav api.quickRoll into the hint slot
ok 698 - status bar wires nav api.quickRoll into the hint slot
  ---
  duration_ms: 1.866494
  ...
# Subtest: status bar ignores missing, v0, or throwing quickRoll namespaces
ok 699 - status bar ignores missing, v0, or throwing quickRoll namespaces
  ---
  duration_ms: 3.511305
  ...
# Subtest: K1 absent: no keeps means 0 with no lints
ok 700 - K1 absent: no keeps means 0 with no lints
  ---
  duration_ms: 3.339919
  ...
# Subtest: K8 misplaced: keeps inside the Tasks suffix reads with a lint
ok 701 - K8 misplaced: keeps inside the Tasks suffix reads with a lint
  ---
  duration_ms: 0.77495
  ...
# Subtest: K9 duplicates and invalid values: first valid wins, else 0
ok 702 - K9 duplicates and invalid values: first valid wins, else 0
  ---
  duration_ms: 1.377501
  ...
# Subtest: K10 ceiling and NEW: 999 reads, never-confirmed reads 0
ok 703 - K10 ceiling and NEW: 999 reads, never-confirmed reads 0
  ---
  duration_ms: 0.246932
  ...
# Subtest: K13 exact keys: near-miss keys are not keeps; parens read
ok 704 - K13 exact keys: near-miss keys are not keeps; parens read
  ---
  duration_ms: 0.208028
  ...
# Subtest: keeps value parser accepts only decimal 1-999
ok 705 - keeps value parser accepts only decimal 1-999
  ---
  duration_ms: 0.18327
  ...
# Subtest: K2 first valid canonical: uncounted keep preserves and repairs
ok 706 - K2 first valid canonical: uncounted keep preserves and repairs
  ---
  duration_ms: 0.891754
  ...
# Subtest: K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
ok 707 - K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
  ---
  duration_ms: 0.809306
  ...
# Subtest: K4 same-day preserve noop: canonical kept line is byte-identical
ok 708 - K4 same-day preserve noop: canonical kept line is byte-identical
  ---
  duration_ms: 0.493773
  ...
# Subtest: K5 generic stamp clears, even same-day
ok 709 - K5 generic stamp clears, even same-day
  ---
  duration_ms: 0.498291
  ...
# Subtest: K6 set-refresh clears keeps
ok 710 - K6 set-refresh clears keeps
  ---
  duration_ms: 0.290114
  ...
# Subtest: K7 stale stamp clears keeps
ok 711 - K7 stale stamp clears keeps
  ---
  duration_ms: 0.197427
  ...
# Subtest: K8b misplaced keeps repaired to canonical order by a keep
ok 712 - K8b misplaced keeps repaired to canonical order by a keep
  ---
  duration_ms: 0.253003
  ...
# Subtest: K11 refusals preserve: closed and recurring lines never write
ok 713 - K11 refusals preserve: closed and recurring lines never write
  ---
  duration_ms: 0.275266
  ...
# Subtest: counted keep increments a stale streak once in the same write
ok 714 - counted keep increments a stale streak once in the same write
  ---
  duration_ms: 0.230921
  ...
# Subtest: first counted keep on a streakless due task writes keeps 1
ok 715 - first counted keep on a streakless due task writes keeps 1
  ---
  duration_ms: 0.26189
  ...
# Subtest: counted keep saturates at 999 and never wraps
ok 716 - counted keep saturates at 999 and never wraps
  ---
  duration_ms: 0.216464
  ...
# Subtest: counted keep needs a valid prior fresh before today
ok 717 - counted keep needs a valid prior fresh before today
  ---
  duration_ms: 0.476801
  ...
# Subtest: counted keep repairs malformed and duplicate placement
ok 718 - counted keep repairs malformed and duplicate placement
  ---
  duration_ms: 0.386688
  ...
# Subtest: uncounted keep preserves the valid value while canonicalizing
ok 719 - uncounted keep preserves the valid value while canonicalizing
  ---
  duration_ms: 0.341862
  ...
# Subtest: UB13 keep on an unblock TICKLER preserves the streak and skips the card
ok 720 - UB13 keep on an unblock TICKLER preserves the streak and skips the card
  ---
  duration_ms: 1.269083
  ...
# Subtest: a scheduled tickler still counts when schedule wins an unblock tie
ok 721 - a scheduled tickler still counts when schedule wins an unblock tie
  ---
  duration_ms: 0.411796
  ...
# Subtest: decay normalization: absent, null, true, and {} enable with 3
ok 722 - decay normalization: absent, null, true, and {} enable with 3
  ---
  duration_ms: 0.736697
  ...
# Subtest: decay false counts and displays but never asks
ok 723 - decay false counts and displays but never asks
  ---
  duration_ms: 0.137953
  ...
# Subtest: decay keeps 0 and fixed entry normalize
ok 724 - decay keeps 0 and fixed entry normalize
  ---
  duration_ms: 0.161398
  ...
# Subtest: invalid decay shapes fail the freshness config contract
ok 725 - invalid decay shapes fail the freshness config contract
  ---
  duration_ms: 0.399172
  ...
# Subtest: B: at-limit Ready due rows decide on every local day
ok 726 - B: at-limit Ready due rows decide on every local day
  ---
  duration_ms: 0.555711
  ...
# Subtest: D1 early date: an at-limit Ready due row decides
ok 727 - D1 early date: an at-limit Ready due row decides
  ---
  duration_ms: 0.114008
  ...
# Subtest: D2 at limit decides; D3 below limit stamps without a card
ok 728 - D2 at limit decides; D3 below limit stamps without a card
  ---
  duration_ms: 0.133956
  ...
# Subtest: D4 tickler counts as due; D5 NEW never decides
ok 729 - D4 tickler counts as due; D5 NEW never decides
  ---
  duration_ms: 0.165826
  ...
# Subtest: D6 zero limit asks on every due Ready re-confirmation
ok 730 - D6 zero limit asks on every due Ready re-confirmation
  ---
  duration_ms: 0.107936
  ...
# Subtest: D7 off never asks; D8 lane rows never decide
ok 731 - D7 off never asks; D8 lane rows never decide
  ---
  duration_ms: 0.100602
  ...
# Subtest: evaluator, queue, and counts carry keeps and decide
ok 732 - evaluator, queue, and counts carry keeps and decide
  ---
  duration_ms: 1.246139
  ...
# Subtest: no keeps: the existing mark is unchanged
ok 733 - no keeps: the existing mark is unchanged
  ---
  duration_ms: 0.993808
  ...
# Subtest: aging with two keeps: faint pips plus a counting-only line
ok 734 - aging with two keeps: faint pips plus a counting-only line
  ---
  duration_ms: 0.322355
  ...
# Subtest: confirmed today with two keeps: check glyph, faint dots
ok 735 - confirmed today with two keeps: check glyph, faint dots
  ---
  duration_ms: 0.262491
  ...
# Subtest: due below threshold: orange capsule keeps its glyph, adds dots
ok 736 - due below threshold: orange capsule keeps its glyph, adds dots
  ---
  duration_ms: 0.262251
  ...
# Subtest: resting marks show historical dots quietly and never decide
ok 737 - resting marks show historical dots quietly and never decide
  ---
  duration_ms: 6.984567
  ...
# Subtest: active decision due: data stays truthful, leaf stays gated
ok 738 - active decision due: data stays truthful, leaf stays gated
  ---
  duration_ms: 0.301586
  ...
# Subtest: dot caps follow the threshold with +N overflow
ok 739 - dot caps follow the threshold with +N overflow
  ---
  duration_ms: 0.692792
  ...
# Subtest: keeps tooltip wording: singulars, zero threshold, off state
ok 740 - keeps tooltip wording: singulars, zero threshold, off state
  ---
  duration_ms: 0.130149
  ...
# Subtest: noncanonical keeps never fold but keep their repair pill
ok 741 - noncanonical keeps never fold but keep their repair pill
  ---
  duration_ms: 0.386147
  ...
# Subtest: quoted lines fold; rendered fragments fold without task checks
ok 742 - quoted lines fold; rendered fragments fold without task checks
  ---
  duration_ms: 0.27752
  ...
# Subtest: unresolved marks show the line's own pips quietly and never decide
ok 743 - unresolved marks show the line's own pips quietly and never decide
  ---
  duration_ms: 0.38748
  ...
# Subtest: consensus sees count and decision eligibility: ambiguity stays neutral
ok 744 - consensus sees count and decision eligibility: ambiguity stays neutral
  ---
  duration_ms: 0.652075
  ...
# Subtest: pips render as one aria-hidden span with the count in the label
ok 745 - pips render as one aria-hidden span with the count in the label
  ---
  duration_ms: 1.323187
  ...
# Subtest: Live Preview decorates the folded range including space and refresh
ok 746 - Live Preview decorates the folded range including space and refresh
  ---
  duration_ms: 4.919967
  ...
# Subtest: Live Preview reveals the raw field when the cursor overlaps either edge
ok 747 - Live Preview reveals the raw field when the cursor overlaps either edge
  ---
  duration_ms: 1.201655
  ...
# Subtest: Live Preview skips codeblock and inline code spans
ok 748 - Live Preview skips codeblock and inline code spans
  ---
  duration_ms: 0.672955
  ...
# Subtest: source mode and marks-off yield no decorations
ok 749 - source mode and marks-off yield no decorations
  ---
  duration_ms: 0.320462
  ...
# Subtest: update rebuilds on the refresh effect and widget eq is stable
ok 750 - update rebuilds on the refresh effect and widget eq is stable
  ---
  duration_ms: 0.975322
  ...
# Subtest: widget click reveals the field at the folded offset
ok 751 - widget click reveals the field at the folded offset
  ---
  duration_ms: 0.702812
  ...
# Subtest: line resolver prefers exact, then consensus, then unresolved
ok 752 - line resolver prefers exact, then consensus, then unresolved
  ---
  duration_ms: 1.144886
  ...
# Subtest: decoration builds reuse the snapshot without touching the loader
ok 753 - decoration builds reuse the snapshot without touching the loader
  ---
  duration_ms: 0.439529
  ...
# Subtest: rendered views split text nodes and skip excluded ancestors
ok 754 - rendered views split text nodes and skip excluded ancestors
  ---
  duration_ms: 2.597551
  ...
# Subtest: rendered views stay idempotent
ok 755 - rendered views stay idempotent
  ---
  duration_ms: 0.736146
  ...
# Subtest: text resolver reaches consensus and degrades to neutral
ok 756 - text resolver reaches consensus and degrades to neutral
  ---
  duration_ms: 0.760803
  ...
# Subtest: session toggle flips the body class and notifies
ok 757 - session toggle flips the body class and notifies
  ---
  duration_ms: 1.184682
  ...
# Subtest: Live Preview reads only the child block and never calls doc.toString
ok 758 - Live Preview reads only the child block and never calls doc.toString
  ---
  duration_ms: 1.376709
  ...
# Subtest: Live Preview stops at the first nonblank line at or above the task
ok 759 - Live Preview stops at the first nonblank line at or above the task
  ---
  duration_ms: 0.32978
  ...
# Subtest: Live Preview performance stays bounded on a large child block
ok 760 - Live Preview performance stays bounded on a large child block
  ---
  duration_ms: 1385.626332
  ...
# Subtest: reading view shows the rotten line and excludes Tasks and Dataview rows
ok 761 - reading view shows the rotten line and excludes Tasks and Dataview rows
  ---
  duration_ms: 0.674037
  ...
# Subtest: query-row consensus stays byte-identical with and without a Rotten Log
ok 762 - query-row consensus stays byte-identical with and without a Rotten Log
  ---
  duration_ms: 0.303991
  ...
# Subtest: onload registers the toggle, extension, and post-processor
ok 763 - onload registers the toggle, extension, and post-processor
  ---
  duration_ms: 4.854701
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 764 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 0.428638
  ...
# Subtest: M1 today: check glyph, today label, full ring
ok 765 - M1 today: check glyph, today label, full ring
  ---
  duration_ms: 5.693592
  ...
# Subtest: M2 aging: ring glyph, 3d label, draining lease
ok 766 - M2 aging: ring glyph, 3d label, draining lease
  ---
  duration_ms: 0.590177
  ...
# Subtest: M3 boundary: ROTTEN due capsule with Alt+F hint
ok 767 - M3 boundary: ROTTEN due capsule with Alt+F hint
  ---
  duration_ms: 0.51292
  ...
# Subtest: checklist marks replace stamp hints with their completion tier
ok 768 - checklist marks replace stamp hints with their completion tier
  ---
  duration_ms: 0.937801
  ...
# Subtest: M4 yesterday uses the yesterday relative
ok 769 - M4 yesterday uses the yesterday relative
  ---
  duration_ms: 0.316615
  ...
# Subtest: M5 folded refresh shows the /14d suffix
ok 770 - M5 folded refresh shows the /14d suffix
  ---
  duration_ms: 0.50825
  ...
# Subtest: M6 refresh today: today tone hides the interval suffix
ok 771 - M6 refresh today: today tone hides the interval suffix
  ---
  duration_ms: 2.148132
  ...
# Subtest: M7 note interval stays tooltip-only
ok 772 - M7 note interval stays tooltip-only
  ---
  duration_ms: 0.547356
  ...
# Subtest: M8 resurfaced: due tone on the scheduled return
ok 773 - M8 resurfaced: due tone on the scheduled return
  ---
  duration_ms: 0.522047
  ...
# Subtest: M9 due NEXT lane with keep/release/today keys
ok 774 - M9 due NEXT lane with keep/release/today keys
  ---
  duration_ms: 0.600557
  ...
# Subtest: M10 NEXT lane stamped today
ok 775 - M10 NEXT lane stamped today
  ---
  duration_ms: 0.321975
  ...
# Subtest: M19 disabled Next lane rests
ok 776 - M19 disabled Next lane rests
  ---
  duration_ms: 0.299251
  ...
# Subtest: M20 PENDING lane folds refresh without the suffix
ok 777 - M20 PENDING lane folds refresh without the suffix
  ---
  duration_ms: 0.254736
  ...
# Subtest: M11 closed: resting beats age 0
ok 778 - M11 closed: resting beats age 0
  ---
  duration_ms: 0.202527
  ...
# Subtest: M12 unresolved running and M13 unresolved lease over
ok 779 - M12 unresolved running and M13 unresolved lease over
  ---
  duration_ms: 0.266569
  ...
# Subtest: M14 linked today rests with its reason
ok 780 - M14 linked today rests with its reason
  ---
  duration_ms: 0.179483
  ...
# Subtest: M15 other year shows the year and the 282d age
ok 781 - M15 other year shows the year and the 282d age
  ---
  duration_ms: 0.142642
  ...
# Subtest: M16 quoted line keeps foldSpace
ok 782 - M16 quoted line keeps foldSpace
  ---
  duration_ms: 0.171858
  ...
# Subtest: M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
ok 783 - M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix
  ---
  duration_ms: 0.388822
  ...
# Subtest: N1-N6 non-canonical lines get no mark
ok 784 - N1-N6 non-canonical lines get no mark
  ---
  duration_ms: 0.164544
  ...
# Subtest: C1-C3 consensus is exact or unresolved
ok 785 - C1-C3 consensus is exact or unresolved
  ---
  duration_ms: 0.62835
  ...
# Subtest: freshnessMarkResolution treats evaluator new as unresolved
ok 786 - freshnessMarkResolution treats evaluator new as unresolved
  ---
  duration_ms: 0.134527
  ...
# Subtest: freshnessMarkSourceInText covers rendered fragments
ok 787 - freshnessMarkSourceInText covers rendered fragments
  ---
  duration_ms: 0.195553
  ...
# Subtest: tone order: closed, then due, then age 0, then out of scope
ok 788 - tone order: closed, then due, then age 0, then out of scope
  ---
  duration_ms: 0.455089
  ...
# Subtest: no tooltip ever contains a double colon
ok 789 - no tooltip ever contains a double colon
  ---
  duration_ms: 0.673256
  ...
# Subtest: freshnessShortDate pins English names and the year rule
ok 790 - freshnessShortDate pins English names and the year rule
  ---
  duration_ms: 0.127774
  ...
# Subtest: DOM builder structure, attributes, and ring geometry
ok 791 - DOM builder structure, attributes, and ring geometry
  ---
  duration_ms: 1.149545
  ...
# Subtest: every mark helper is synchronous and never throws on bad input
ok 792 - every mark helper is synchronous and never throws on bad input
  ---
  duration_ms: 0.129638
  ...
# Subtest: rotten line wording covers 0, 1, and many entries
ok 793 - rotten line wording covers 0, 1, and many entries
  ---
  duration_ms: 0.383222
  ...
# Subtest: rotten line date format includes the year only when it differs
ok 794 - rotten line date format includes the year only when it differs
  ---
  duration_ms: 0.21482
  ...
# Subtest: rotten line truncates the reason to 48 code points without splitting emoji
ok 795 - rotten line truncates the reason to 48 code points without splitting emoji
  ---
  duration_ms: 0.189061
  ...
# Subtest: rotten history rejects ambiguous, invalid, and nested entries
ok 796 - rotten history rejects ambiguous, invalid, and nested entries
  ---
  duration_ms: 1.12607
  ...
# Subtest: rotten marker vectors reject mismatched emoji and missing spaces
ok 797 - rotten marker vectors reject mismatched emoji and missing spaces
  ---
  duration_ms: 0.6755
  ...
# Subtest: rotten line splices before the action line and reaches aria-label
ok 798 - rotten line splices before the action line and reaches aria-label
  ---
  duration_ms: 0.506267
  ...
# Subtest: freshness namespace v12 exposes unblock TICKLER metadata and writers
ok 799 - freshness namespace v12 exposes unblock TICKLER metadata and writers
  ---
  duration_ms: 16.042965
  ...
# Subtest: freshness state and count API expose an unblock return source
ok 800 - freshness state and count API expose an unblock return source
  ---
  duration_ms: 1.870772
  ...
# Subtest: checklist rows report tier and rank while keeping the READY bucket null
ok 801 - checklist rows report tier and rank while keeping the READY bucket null
  ---
  duration_ms: 1.576281
  ...
# Subtest: tier, isDue, and rank cover lane rows
ok 802 - tier, isDue, and rank cover lane rows
  ---
  duration_ms: 3.197106
  ...
# Subtest: memo invalidates on a new tasks array, rollover, and frontmatter
ok 803 - memo invalidates on a new tasks array, rollover, and frontmatter
  ---
  duration_ms: 2.738641
  ...
# Subtest: the reload event fires only when the due key set changes
ok 804 - the reload event fires only when the due key set changes
  ---
  duration_ms: 2.543647
  ...
# Subtest: status bar text covers every state, and a missing host stays quiet
ok 805 - status bar text covers every state, and a missing host stays quiet
  ---
  duration_ms: 1.783235
  ...
# Subtest: status bar clicks through, falling back to rotten
ok 806 - status bar clicks through, falling back to rotten
  ---
  duration_ms: 5.689123
  ...
# Subtest: every freshness api member is synchronous and never throws
ok 807 - every freshness api member is synchronous and never throws
  ---
  duration_ms: 2.093628
  ...
# Subtest: placement vectors P1-P11, P14-P16, P18 stamp canonically
ok 808 - placement vectors P1-P11, P14-P16, P18 stamp canonically
  ---
  duration_ms: 9.644307
  ...
# Subtest: P12 set and clear refresh stamps alongside
ok 809 - P12 set and clear refresh stamps alongside
  ---
  duration_ms: 0.318398
  ...
# Subtest: P13 recurring and P17 done tasks are refused unchanged
ok 810 - P13 recurring and P17 done tasks are refused unchanged
  ---
  duration_ms: 0.219429
  ...
# Subtest: Pomodoro ledger rows are refused byte-for-byte by every fresh writer
ok 811 - Pomodoro ledger rows are refused byte-for-byte by every fresh writer
  ---
  duration_ms: 0.520905
  ...
# Subtest: a time range later in task prose remains eligible for freshness
ok 812 - a time range later in task prose remains eligible for freshness
  ---
  duration_ms: 0.181456
  ...
# Subtest: U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
ok 813 - U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
  ---
  duration_ms: 0.733721
  ...
# Subtest: reader reports misplaced and duplicate fields
ok 814 - reader reports misplaced and duplicate fields
  ---
  duration_ms: 0.352082
  ...
# Subtest: Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
ok 815 - Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created
  ---
  duration_ms: 4.270355
  ...
# Subtest: Q2 tier order beats path order
ok 816 - Q2 tier order beats path order
  ---
  duration_ms: 1.161087
  ...
# Subtest: L1 lane due and stamped today
ok 817 - L1 lane due and stamped today
  ---
  duration_ms: 0.42914
  ...
# Subtest: L2 lane overrides refresh
ok 818 - L2 lane overrides refresh
  ---
  duration_ms: 0.281007
  ...
# Subtest: L3 lane exclusions have no tier
ok 819 - L3 lane exclusions have no tier
  ---
  duration_ms: 0.389884
  ...
# Subtest: L4 lane off switch and null default
ok 820 - L4 lane off switch and null default
  ---
  duration_ms: 0.268502
  ...
# Subtest: L5 lane order never stamped first
ok 821 - L5 lane order never stamped first
  ---
  duration_ms: 0.384725
  ...
# Subtest: R1 TICKLER beats older ROTTEN
ok 822 - R1 TICKLER beats older ROTTEN
  ---
  duration_ms: 0.310333
  ...
# Subtest: R2 tickler orders by due date then path and line
ok 823 - R2 tickler orders by due date then path and line
  ---
  duration_ms: 0.548337
  ...
# Subtest: missing created sorts after dated peers
ok 824 - missing created sorts after dated peers
  ---
  duration_ms: 0.724364
  ...
# Subtest: B1 upkeep counts outside the lanes
ok 825 - B1 upkeep counts outside the lanes
  ---
  duration_ms: 1.868277
  ...
# Subtest: review model meter uses upkeep and exposes refreshed
ok 826 - review model meter uses upkeep and exposes refreshed
  ---
  duration_ms: 0.290364
  ...
# Subtest: RC1 arrived: past scheduled walks RECURRING with lane and null state
ok 827 - RC1 arrived: past scheduled walks RECURRING with lane and null state
  ---
  duration_ms: 4.434047
  ...
# Subtest: RC2 arrives today: due today with zero days overdue
ok 828 - RC2 arrives today: due today with zero days overdue
  ---
  duration_ms: 0.395425
  ...
# Subtest: RC3 not yet: future scheduled walks nowhere
ok 829 - RC3 not yet: future scheduled walks nowhere
  ---
  duration_ms: 0.53371
  ...
# Subtest: RC4 due only, past: the due date is the occurrence
ok 830 - RC4 due only, past: the due date is the occurrence
  ---
  duration_ms: 0.347133
  ...
# Subtest: RC5 due only, future: walks nowhere
ok 831 - RC5 due only, future: walks nowhere
  ---
  duration_ms: 0.411145
  ...
# Subtest: RC6 earliest date wins across start and due
ok 832 - RC6 earliest date wins across start and due
  ---
  duration_ms: 0.373753
  ...
# Subtest: RC7 undated: no occurrence, no tier
ok 833 - RC7 undated: no occurrence, no tier
  ---
  duration_ms: 0.434039
  ...
# Subtest: RC8 lanes: recurring lane rows keep their lane with null state
ok 834 - RC8 lanes: recurring lane rows keep their lane with null state
  ---
  duration_ms: 0.641705
  ...
# Subtest: RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
ok 835 - RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out
  ---
  duration_ms: 1.914216
  ...
# Subtest: RC10 checklist wins: a recurring chore stays in its checklist tier
ok 836 - RC10 checklist wins: a recurring chore stays in its checklist tier
  ---
  duration_ms: 0.521265
  ...
# Subtest: RC11 a stray stamp is ignored: recurring with null state
ok 837 - RC11 a stray stamp is ignored: recurring with null state
  ---
  duration_ms: 0.431904
  ...
# Subtest: RC12 order and counts: due_on, then path, then line; recurring adds no due
ok 838 - RC12 order and counts: due_on, then path, then line; recurring adds no due
  ---
  duration_ms: 1.312146
  ...
# Subtest: recurring rows adapt due and start from Tasks fields and inline fallbacks
ok 839 - recurring rows adapt due and start from Tasks fields and inline fallbacks
  ---
  duration_ms: 1.51333
  ...
# Subtest: status view counts RECURRING as a due commitment tier
ok 840 - status view counts RECURRING as a due commitment tier
  ---
  duration_ms: 0.397148
  ...
# Subtest: footer groups, entry view, and legend cover RECURRING
ok 841 - footer groups, entry view, and legend cover RECURRING
  ---
  duration_ms: 0.976284
  ...
# Subtest: a stale-stamped recurring row marks due with the resolve hint
ok 842 - a stale-stamped recurring row marks due with the resolve hint
  ---
  duration_ms: 1.069792
  ...
# Subtest: freshness namespace v12 keeps recurring and removes reference capabilities
ok 843 - freshness namespace v12 keeps recurring and removes reference capabilities
  ---
  duration_ms: 6.100602
  ...
# Subtest: hidden recurring ^ref keeps ordinary visibility (Rust parity)
ok 844 - hidden recurring ^ref keeps ordinary visibility (Rust parity)
  ---
  duration_ms: 1.02127
  ...
# Subtest: bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
ok 845 - bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null
  ---
  duration_ms: 5.918482
  ...
# Subtest: day numbers stay calendar-local across a DST boundary
ok 846 - day numbers stay calendar-local across a DST boundary
  ---
  duration_ms: 0.877506
  ...
# Subtest: reviewModel shares counts, meter, tooltip, and severity
ok 847 - reviewModel shares counts, meter, tooltip, and severity
  ---
  duration_ms: 0.617259
  ...
# Subtest: memo serves warm map hits and misses use the per-row evaluator
ok 848 - memo serves warm map hits and misses use the per-row evaluator
  ---
  duration_ms: 12.344041
  ...
# Subtest: config snapshot caches the parse and invalidates explicitly
ok 849 - config snapshot caches the parse and invalidates explicitly
  ---
  duration_ms: 2.038774
  ...
# Subtest: review chips share the model with severity classes
ok 850 - review chips share the model with severity classes
  ---
  duration_ms: 1.61256
  ...
# Subtest: warm lookups reuse one snapshot without re-reading config
ok 851 - warm lookups reuse one snapshot without re-reading config
  ---
  duration_ms: 2.412919
  ...
# Subtest: same-array cache updates and Today changes rebuild the memo
ok 852 - same-array cache updates and Today changes rebuild the memo
  ---
  duration_ms: 4.399082
  ...
# Subtest: duplicate block IDs keep each row's own classification
ok 853 - duplicate block IDs keep each row's own classification
  ---
  duration_ms: 3.142641
  ...
# Subtest: line identity separates same-path rows without block IDs
ok 854 - line identity separates same-path rows without block IDs
  ---
  duration_ms: 1.620124
  ...
# Subtest: interval lookup serves the cached interval with one memo acquisition
ok 855 - interval lookup serves the cached interval with one memo acquisition
  ---
  duration_ms: 1.783216
  ...
# Subtest: S1 new through S4 overdue
ok 856 - S1 new through S4 overdue
  ---
  duration_ms: 12.695794
  ...
# Subtest: S5 task beats note, S6 note beats config, S7 config
ok 857 - S5 task beats note, S6 note beats config, S7 config
  ---
  duration_ms: 1.034626
  ...
# Subtest: S8 invalid overrides fall through with lints
ok 858 - S8 invalid overrides fall through with lints
  ---
  duration_ms: 0.543378
  ...
# Subtest: S9 malformed and S10 future stamps read as new
ok 859 - S9 malformed and S10 future stamps read as new
  ---
  duration_ms: 0.332345
  ...
# Subtest: S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
ok 860 - S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh
  ---
  duration_ms: 0.494595
  ...
# Subtest: S13 out-of-scope rows read null
ok 861 - S13 out-of-scope rows read null
  ---
  duration_ms: 0.485618
  ...
# Subtest: S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
ok 862 - S14 queue order (rewritten): NEW then TICKLER beats ROTTEN
  ---
  duration_ms: 2.260368
  ...
# Subtest: S15 counts (updated): upkeep outside the lanes drives the budget
ok 863 - S15 counts (updated): upkeep outside the lanes drives the budget
  ---
  duration_ms: 1.651735
  ...
# Subtest: config coercion keeps defaults, flags invalid, ignores unknown keys
ok 864 - config coercion keeps defaults, flags invalid, ignores unknown keys
  ---
  duration_ms: 2.087256
  ...
# Subtest: loadFreshnessConfig reads the block with plan-style injectables
ok 865 - loadFreshnessConfig reads the block with plan-style injectables
  ---
  duration_ms: 1.696881
  ...
# Subtest: interval precedence is task, note, config, default
ok 866 - interval precedence is task, note, config, default
  ---
  duration_ms: 0.318028
  ...
# Subtest: intervalForLine covers every source with its Ready fallback
ok 867 - intervalForLine covers every source with its Ready fallback
  ---
  duration_ms: 1.263192
  ...
# Subtest: project tracking stays special while reference tasks use ordinary Ready freshness
ok 868 - project tracking stays special while reference tasks use ordinary Ready freshness
  ---
  duration_ms: 4.529091
  ...
# Subtest: reference tasks match ordinary interval precedence and lane behavior
ok 869 - reference tasks match ordinary interval precedence and lane behavior
  ---
  duration_ms: 7.192766
  ...
# Subtest: obsolete reference interval keys are ignored and project config still validates
ok 870 - obsolete reference interval keys are ignored and project config still validates
  ---
  duration_ms: 0.691531
  ...
# Subtest: references use ordinary keep decisions and the nine-tier queue shape
ok 871 - references use ordinary keep decisions and the nine-tier queue shape
  ---
  duration_ms: 1.262541
  ...
# Subtest: CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
ok 872 - CL1-CL7: exact checklist scope, precedence, and unchanged state buckets
  ---
  duration_ms: 2.4246
  ...
# Subtest: CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
ok 873 - CL8-CL12: nine tier order, checklist-only due counts, and completion semantics
  ---
  duration_ms: 2.04738
  ...
# Subtest: freshness namespace v12 retains the tracker capability contract
ok 874 - freshness namespace v12 retains the tracker capability contract
  ---
  duration_ms: 5.853558
  ...
# Subtest: UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
ok 875 - UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER
  ---
  duration_ms: 4.476388
  ...
# Subtest: UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
ok 876 - UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows
  ---
  duration_ms: 0.710476
  ...
# Subtest: UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
ok 877 - UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date
  ---
  duration_ms: 5.354916
  ...
# Subtest: UB11 scheduled wins a tie with the unblock date
ok 878 - UB11 scheduled wins a tie with the unblock date
  ---
  duration_ms: 0.560681
  ...
# Subtest: unblocked reader takes the latest valid duplicate and reports malformed values
ok 879 - unblocked reader takes the latest valid duplicate and reports malformed values
  ---
  duration_ms: 0.398241
  ...
# Subtest: UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
ok 880 - UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields
  ---
  duration_ms: 0.662265
  ...
# Subtest: UB14 TICKLERs with the same due date sort only by path and line
ok 881 - UB14 TICKLERs with the same due date sort only by path and line
  ---
  duration_ms: 2.213468
  ...
# Subtest: UB15 a scheduled ^prj resurfaces in PROJECTS
ok 882 - UB15 a scheduled ^prj resurfaces in PROJECTS
  ---
  duration_ms: 0.308059
  ...
# Subtest: an active-note Pomodoro target still jumps and centers immediately
ok 883 - an active-note Pomodoro target still jumps and centers immediately
  ---
  duration_ms: 12.496133
  ...
# Subtest: Ctrl+9 from an unpinned daily copy switches to the pinned home tab
ok 884 - Ctrl+9 from an unpinned daily copy switches to the pinned home tab
  ---
  duration_ms: 3.163852
  ...
# Subtest: Ctrl+9 on the pinned daily tab jumps in place when a copy exists
ok 885 - Ctrl+9 on the pinned daily tab jumps in place when a copy exists
  ---
  duration_ms: 1.21437
  ...
# Subtest: Ctrl+9 switches daily copies without a Pomodoros section and stays quiet
ok 886 - Ctrl+9 switches daily copies without a Pomodoros section and stays quiet
  ---
  duration_ms: 1.196736
  ...
# Subtest: Ctrl+9 keeps the active daily tab when equal-ranked copies exist
ok 887 - Ctrl+9 keeps the active daily tab when equal-ranked copies exist
  ---
  duration_ms: 1.252663
  ...
# Subtest: Ctrl+9 from a sidebar daily copy switches to a main-area home tab
ok 888 - Ctrl+9 from a sidebar daily copy switches to a main-area home tab
  ---
  duration_ms: 1.112445
  ...
# Subtest: the first fallback press only opens daily and the second press jumps
ok 889 - the first fallback press only opens daily and the second press jumps
  ---
  duration_ms: 1.391047
  ...
# Subtest: a daily note with no target defers its notice until the second press
ok 890 - a daily note with no target defers its notice until the second press
  ---
  duration_ms: 1.038935
  ...
# Subtest: an already-open daily leaf retains its live cursor and viewport
ok 891 - an already-open daily leaf retains its live cursor and viewport
  ---
  duration_ms: 2.281757
  ...
# Subtest: a second press after reused-leaf fallback performs the Pomodoro jump
ok 892 - a second press after reused-leaf fallback performs the Pomodoro jump
  ---
  duration_ms: 1.493732
  ...
# Subtest: the standalone daily-note command activates a reused daily leaf
ok 893 - the standalone daily-note command activates a reused daily leaf
  ---
  duration_ms: 0.834393
  ...
# Subtest: Ctrl+9 loads and reuses a deferred pinned daily tab before falling back
ok 894 - Ctrl+9 loads and reuses a deferred pinned daily tab before falling back
  ---
  duration_ms: 0.866195
  ...
# Subtest: pinned daily tabs win over earlier unpinned tabs
ok 895 - pinned daily tabs win over earlier unpinned tabs
  ---
  duration_ms: 0.925898
  ...
# Subtest: a deferred sidebar daily tab is reused only without a main-area match
ok 896 - a deferred sidebar daily tab is reused only without a main-area match
  ---
  duration_ms: 1.091675
  ...
# Subtest: a deferred sidebar daily tab is reused when there is no main-area match
ok 897 - a deferred sidebar daily tab is reused when there is no main-area match
  ---
  duration_ms: 0.732218
  ...
# Subtest: a deferred non-Markdown daily path is ignored and uses the daily-note fallback
ok 898 - a deferred non-Markdown daily path is ignored and uses the daily-note fallback
  ---
  duration_ms: 0.975372
  ...
# Subtest: the standalone daily-note command reuses a deferred pinned tab
ok 899 - the standalone daily-note command reuses a deferred pinned tab
  ---
  duration_ms: 0.732188
  ...
# Subtest: Ctrl+9 opens the pinned daily tab from a non-Markdown active leaf
ok 900 - Ctrl+9 opens the pinned daily tab from a non-Markdown active leaf
  ---
  duration_ms: 0.788696
  ...
# Subtest: a closed then reopened daily note restores its in-session location
ok 901 - a closed then reopened daily note restores its in-session location
  ---
  duration_ms: 1.636725
  ...
# Subtest: different-path and invalid locations do not leak into a daily note
ok 902 - different-path and invalid locations do not leak into a daily note
  ---
  duration_ms: 0.753529
  ...
# Subtest: out-of-range remembered coordinates are clamped safely
ok 903 - out-of-range remembered coordinates are clamped safely
  ---
  duration_ms: 0.768808
  ...
# Subtest: a rapid second press cancels an older fallback restore
ok 904 - a rapid second press cancels an older fallback restore
  ---
  duration_ms: 0.887254
  ...
# Subtest: navigation and unload clean up daily scroll listeners and deferred work
ok 905 - navigation and unload clean up daily scroll listeners and deferred work
  ---
  duration_ms: 0.791822
  ...
# Subtest: crowded chip: over count is red with tooltip, aria, and names
ok 906 - crowded chip: over count is red with tooltip, aria, and names
  ---
  duration_ms: 1.700988
  ...
# Subtest: crowded chip: calm zero and unavailable dash
ok 907 - crowded chip: calm zero and unavailable dash
  ---
  duration_ms: 0.281467
  ...
# Subtest: crowded chip: names at most five notes
ok 908 - crowded chip: names at most five notes
  ---
  duration_ms: 0.395746
  ...
# Subtest: crowded chip: classes, text, aria, and arrow
ok 909 - crowded chip: classes, text, aria, and arrow
  ---
  duration_ms: 2.076305
  ...
# Subtest: crowded chip: refresh in place keeps the anchor, unload drops it
ok 910 - crowded chip: refresh in place keeps the anchor, unload drops it
  ---
  duration_ms: 0.807232
  ...
# Subtest: anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
ok 911 - anchor helper keeps READY, PENDING, NEXT, and CROWDED classes
  ---
  duration_ms: 0.702472
  ...
# Subtest: ready-notes summary: crowded, calm, and unavailable
ok 912 - ready-notes summary: crowded, calm, and unavailable
  ---
  duration_ms: 0.329149
  ...
# Subtest: ready-notes bar: cap tick and red overflow within 30 cells
ok 913 - ready-notes bar: cap tick and red overflow within 30 cells
  ---
  duration_ms: 0.245269
  ...
# Subtest: ready-notes block: model and render with grid, pills, and footer
ok 914 - ready-notes block: model and render with grid, pills, and footer
  ---
  duration_ms: 1.851356
  ...
# Subtest: ready-notes block: unavailable renders a dash line
ok 915 - ready-notes block: unavailable renders a dash line
  ---
  duration_ms: 0.557125
  ...
# Subtest: heading matcher: fences, level, case, and first-only
ok 916 - heading matcher: fences, level, case, and first-only
  ---
  duration_ms: 0.470779
  ...
# Subtest: heading chip copy: room, full, crowded, exempt, unavailable
ok 917 - heading chip copy: room, full, crowded, exempt, unavailable
  ---
  duration_ms: 0.446002
  ...
# Subtest: heading chip key is stable for equal models
ok 918 - heading chip key is stable for equal models
  ---
  duration_ms: 0.192979
  ...
# Subtest: reading view: appends the chip to the matching h2 only
ok 919 - reading view: appends the chip to the matching h2 only
  ---
  duration_ms: 1.777354
  ...
# Subtest: reading view: no chip for ineligible notes
ok 920 - reading view: no chip for ineligible notes
  ---
  duration_ms: 0.16206
  ...
# Subtest: one live-refresh fan-out reaches every family
ok 921 - one live-refresh fan-out reaches every family
  ---
  duration_ms: 1.14154
  ...
# Subtest: ledger-tools CSS is theme-safe for the new views
ok 922 - ledger-tools CSS is theme-safe for the new views
  ---
  duration_ms: 0.861444
  ...
# Subtest: maxReadyPerNote defaults to 5 and validates 1–999
ok 923 - maxReadyPerNote defaults to 5 and validates 1–999
  ---
  duration_ms: 3.395965
  ...
# Subtest: loadPlanCaps caches on a stat key and detects edits
ok 924 - loadPlanCaps caches on a stat key and detects edits
  ---
  duration_ms: 0.792363
  ...
# Subtest: loadPlanCaps handles deletion, invalid edits, and recovery
ok 925 - loadPlanCaps handles deletion, invalid edits, and recovery
  ---
  duration_ms: 0.688254
  ...
# Subtest: loadPlanCaps without statSync reads through uncached
ok 926 - loadPlanCaps without statSync reads through uncached
  ---
  duration_ms: 0.437205
  ...
# Subtest: noteFrontmatter resolves through getFileCache, not getCache
ok 927 - noteFrontmatter resolves through getFileCache, not getCache
  ---
  duration_ms: 0.981614
  ...
# Subtest: task_refresh applies through the shared reader
ok 928 - task_refresh applies through the shared reader
  ---
  duration_ms: 5.177017
  ...
# Subtest: noteReadyKindFromType covers every R11 form
ok 929 - noteReadyKindFromType covers every R11 form
  ---
  duration_ms: 0.561092
  ...
# Subtest: noteReadyStatusLabel mirrors ProjectStatus::parse
ok 930 - noteReadyStatusLabel mirrors ProjectStatus::parse
  ---
  duration_ms: 0.366651
  ...
# Subtest: noteReadyParentStem strips alias, heading, and path
ok 931 - noteReadyParentStem strips alias, heading, and path
  ---
  duration_ms: 0.463966
  ...
# Subtest: parseNoteReadyCap covers every R8 form
ok 932 - parseNoteReadyCap covers every R8 form
  ---
  duration_ms: 0.90595
  ...
# Subtest: R1: 6 tasks at the default cap are crowded with over_by 1
ok 933 - R1: 6 tasks at the default cap are crowded with over_by 1
  ---
  duration_ms: 10.34775
  ...
# Subtest: R2: 5 tasks are full with no lint
ok 934 - R2: 5 tasks are full with no lint
  ---
  duration_ms: 3.121391
  ...
# Subtest: R3: hidden, future, blocked, and non-TODO rows never count
ok 935 - R3: hidden, future, blocked, and non-TODO rows never count
  ---
  duration_ms: 3.230379
  ...
# Subtest: R4: make-up splits 1 ready + 1 new + 1 rotten
ok 936 - R4: make-up splits 1 ready + 1 new + 1 rotten
  ---
  duration_ms: 2.129617
  ...
# Subtest: R5: recurring rows are excluded but tallied
ok 937 - R5: recurring rows are excluded but tallied
  ---
  duration_ms: 1.315953
  ...
# Subtest: R6: a visible ^prj task never counts
ok 938 - R6: a visible ^prj task never counts
  ---
  duration_ms: 1.175846
  ...
# Subtest: R7: daily, untyped, template, done, and dash rows are absent
ok 939 - R7: daily, untyped, template, done, and dash rows are absent
  ---
  duration_ms: 1.877916
  ...
# Subtest: R8: ready_cap forms map to cap, exempt, or lint-then-default
ok 940 - R8: ready_cap forms map to cap, exempt, or lint-then-default
  ---
  duration_ms: 3.047782
  ...
# Subtest: R9: a parent with two children counts 3
ok 941 - R9: a parent with two children counts 3
  ---
  duration_ms: 1.092477
  ...
# Subtest: R10: terminal projects are not capped and lint once
ok 942 - R10: terminal projects are not capped and lint once
  ---
  duration_ms: 2.15233
  ...
# Subtest: R11: every type form and nested folders are eligible
ok 943 - R11: every type form and nested folders are eligible
  ---
  duration_ms: 1.290975
  ...
# Subtest: R12: stamping a NEW task keeps the count and moves the make-up
ok 944 - R12: stamping a NEW task keeps the count and moves the make-up
  ---
  duration_ms: 2.046938
  ...
# Subtest: R13: a Today-linked task still counts
ok 945 - R13: a Today-linked task still counts
  ---
  duration_ms: 0.689247
  ...
# Subtest: R14: max_ready_per_note 3 caps others while ready_cap 8 holds
ok 946 - R14: max_ready_per_note 3 caps others while ready_cap 8 holds
  ---
  duration_ms: 2.595787
  ...
# Subtest: api.noteReady is frozen at version 1 under api v3
ok 947 - api.noteReady is frozen at version 1 under api v3
  ---
  duration_ms: 0.399492
  ...
# Subtest: counted and inCrowdedNote resolve per task
ok 948 - counted and inCrowdedNote resolve per task
  ---
  duration_ms: 2.002674
  ...
# Subtest: groupLabel ranks crowded notes by excess
ok 949 - groupLabel ranks crowded notes by excess
  ---
  duration_ms: 8.267838
  ...
# Subtest: snapshot sorts crowded, full, room, empty, exempt and splits totals
ok 950 - snapshot sorts crowded, full, room, empty, exempt and splits totals
  ---
  duration_ms: 6.166386
  ...
# Subtest: missing Tasks data and a cold cache are unavailable, never zero
ok 951 - missing Tasks data and a cold cache are unavailable, never zero
  ---
  duration_ms: 1.575419
  ...
# Subtest: throwing Tasks guards never throw
ok 952 - throwing Tasks guards never throw
  ---
  duration_ms: 0.961086
  ...
# Subtest: snapshot reuses the memo without reparsing or re-walking
ok 953 - snapshot reuses the memo without reparsing or re-walking
  ---
  duration_ms: 1.327846
  ...
# Subtest: a task edit rebuilds through the cache-update handler
ok 954 - a task edit rebuilds through the cache-update handler
  ---
  duration_ms: 1.315162
  ...
# Subtest: a ready_cap edit rebuilds and fires the query-refresh trigger
ok 955 - a ready_cap edit rebuilds and fires the query-refresh trigger
  ---
  duration_ms: 1.133465
  ...
# Subtest: rename and delete move the eligibility entry
ok 956 - rename and delete move the eligibility entry
  ---
  duration_ms: 1.316173
  ...
# Subtest: day rollover rebuilds the snapshot date
ok 957 - day rollover rebuilds the snapshot date
  ---
  duration_ms: 1.062158
  ...
# Subtest: a config edit flows through the stat cache
ok 958 - a config edit flows through the stat cache
  ---
  duration_ms: 2.209239
  ...
# Subtest: untyped and non-markdown vault events are no-ops
ok 959 - untyped and non-markdown vault events are no-ops
  ---
  duration_ms: 1.163181
  ...
# Subtest: memo hits never re-walk the vault
ok 960 - memo hits never re-walk the vault
  ---
  duration_ms: 66.407256
  ...
# Subtest: the startup storm is linear
ok 961 - the startup storm is linear
  ---
  duration_ms: 26.198972
  ...
# Subtest: the first resolved event forces one rebuild and later ones do not
ok 962 - the first resolved event forces one rebuild and later ones do not
  ---
  duration_ms: 1.614032
  ...
# Subtest: noteReadyEvaluate is pure and mirrors the Rust totals
ok 963 - noteReadyEvaluate is pure and mirrors the Rust totals
  ---
  duration_ms: 0.263924
  ...
# Subtest: conformance: merged name with duplicate
ok 964 - conformance: merged name with duplicate
  ---
  duration_ms: 3.692022
  ...
# Subtest: conformance: link forms and exclusions
ok 965 - conformance: link forms and exclusions
  ---
  duration_ms: 0.67531
  ...
# Subtest: conformance: unnamed placeholders
ok 966 - conformance: unnamed placeholders
  ---
  duration_ms: 0.370217
  ...
# Subtest: conformance: subheading in the section
ok 967 - conformance: subheading in the section
  ---
  duration_ms: 0.238385
  ...
# Subtest: conformance: open inventory label
ok 968 - conformance: open inventory label
  ---
  duration_ms: 0.333998
  ...
# Subtest: conformance: over the cap
ok 969 - conformance: over the cap
  ---
  duration_ms: 0.223437
  ...
# Subtest: conformance: cancelled and completed entries
ok 970 - conformance: cancelled and completed entries
  ---
  duration_ms: 0.270155
  ...
# Subtest: exactly at the cap is fine
ok 971 - exactly at the cap is fine
  ---
  duration_ms: 0.182618
  ...
# Subtest: no Pomodoros section degrades to an empty budget
ok 972 - no Pomodoros section degrades to an empty budget
  ---
  duration_ms: 0.438618
  ...
# Subtest: fenced code never counts
ok 973 - fenced code never counts
  ---
  duration_ms: 0.517048
  ...
# Subtest: highlight is the first open non-exempt entry; running is the timed one
ok 974 - highlight is the first open non-exempt entry; running is the timed one
  ---
  duration_ms: 0.384574
  ...
# Subtest: coercePlanCaps ignores a legacy max_now instead of failing
ok 975 - coercePlanCaps ignores a legacy max_now instead of failing
  ---
  duration_ms: 0.283241
  ...
# Subtest: parsePlanCaps defaults, overrides, and invalid fallbacks
ok 976 - parsePlanCaps defaults, overrides, and invalid fallbacks
  ---
  duration_ms: 0.33526
  ...
# Subtest: loadPlanCaps falls back to defaults without fs
ok 977 - loadPlanCaps falls back to defaults without fs
  ---
  duration_ms: 0.428468
  ...
# Subtest: loadPlanCaps falls back to defaults on mobile
ok 978 - loadPlanCaps falls back to defaults on mobile
  ---
  duration_ms: 0.232133
  ...
# Subtest: loadPlanCaps reads plan: and flags invalid values
ok 979 - loadPlanCaps reads plan: and flags invalid values
  ---
  duration_ms: 0.387811
  ...
# Subtest: planBlockTargetPath prefers the containing daily note
ok 980 - planBlockTargetPath prefers the containing daily note
  ---
  duration_ms: 0.6757
  ...
# Subtest: planBlockModel degrades to placeholders, never an error
ok 981 - planBlockModel degrades to placeholders, never an error
  ---
  duration_ms: 0.860192
  ...
# Subtest: planBlockModel renders chips, themes, and lints
ok 982 - planBlockModel renders chips, themes, and lints
  ---
  duration_ms: 1.075063
  ...
# Subtest: planBlockModel adds lane cap lints when a lane is over
ok 983 - planBlockModel adds lane cap lints when a lane is over
  ---
  duration_ms: 0.786642
  ...
# Subtest: plugin exposes the versioned api and registers the bob-plan block
ok 984 - plugin exposes the versioned api and registers the bob-plan block
  ---
  duration_ms: 6.336029
  ...
# Subtest: invalid plan block falls back to full defaults
ok 985 - invalid plan block falls back to full defaults
  ---
  duration_ms: 0.249707
  ...
# Subtest: entries require column-0 dash-space with one status char
ok 986 - entries require column-0 dash-space with one status char
  ---
  duration_ms: 0.201936
  ...
# Subtest: crlf line endings split like lf
ok 987 - crlf line endings split like lf
  ---
  duration_ms: 0.257622
  ...
# Subtest: conformance: empty target means the daily note
ok 988 - conformance: empty target means the daily note
  ---
  duration_ms: 0.233786
  ...
# Subtest: lane predicate matches hide subtags, case, and non-task
ok 989 - lane predicate matches hide subtags, case, and non-task
  ---
  duration_ms: 0.332395
  ...
# Subtest: planBlockModel daily badges follow dashboard section counts
ok 990 - planBlockModel daily badges follow dashboard section counts
  ---
  duration_ms: 2.411865
  ...
# Subtest: planBlockModel keeps a supplied unavailable dashboard budget
ok 991 - planBlockModel keeps a supplied unavailable dashboard budget
  ---
  duration_ms: 0.392019
  ...
# Subtest: work tones: TODAY override and unavailable stay neutral in planBlockModel
ok 992 - work tones: TODAY override and unavailable stay neutral in planBlockModel
  ---
  duration_ms: 0.206233
  ...
# Subtest: shared vector: subproject-archive-review
ok 993 - shared vector: subproject-archive-review
  ---
  duration_ms: 7.636113
  ...
# Subtest: shared vector: review-decisions
ok 994 - shared vector: review-decisions
  ---
  duration_ms: 2.102214
  ...
# Subtest: shared vector: resolution-and-lints
ok 995 - shared vector: resolution-and-lints
  ---
  duration_ms: 2.884298
  ...
# Subtest: shared vector: chips, forecast shares, empty forecasts, and session identity
ok 996 - shared vector: chips, forecast shares, empty forecasts, and session identity
  ---
  duration_ms: 1.89574
  ...
# Subtest: shared vector: split-rounding-and-duration
ok 997 - shared vector: split-rounding-and-duration
  ---
  duration_ms: 0.849542
  ...
# Subtest: shared vector: share-rounding
ok 998 - shared vector: share-rounding
  ---
  duration_ms: 0.598553
  ...
# Subtest: shared vector: daily-review-link
ok 999 - shared vector: daily-review-link
  ---
  duration_ms: 0.478424
  ...
# Subtest: shared vector: depth-and-parent-shapes
ok 1000 - shared vector: depth-and-parent-shapes
  ---
  duration_ms: 1.47676
  ...
# Subtest: shared vector: unresolved-and-closed-zero
ok 1001 - shared vector: unresolved-and-closed-zero
  ---
  duration_ms: 1.206785
  ...
# Subtest: shared vector: parent-scalar-shapes
ok 1002 - shared vector: parent-scalar-shapes
  ---
  duration_ms: 0.861004
  ...
# Subtest: dedicated link parser keeps embeds and one struck link, but rejects prose
ok 1003 - dedicated link parser keeps embeds and one struck link, but rejects prose
  ---
  duration_ms: 0.298129
  ...
# Subtest: FNV-1a fallback for job maps to the pinned magenta slot
ok 1004 - FNV-1a fallback for job maps to the pinned magenta slot
  ---
  duration_ms: 0.17256
  ...
# Subtest: area-color lints are reported once per note
ok 1005 - area-color lints are reported once per note
  ---
  duration_ms: 0.553136
  ...
# Subtest: a leftover rollup key neither regroups nor warns
ok 1006 - a leftover rollup key neither regroups nor warns
  ---
  duration_ms: 0.420964
  ...
# Subtest: chip DOM exposes forecast, hue, accessible text, and tooltip
ok 1007 - chip DOM exposes forecast, hue, accessible text, and tooltip
  ---
  duration_ms: 0.406316
  ...
# Subtest: Reading view appends a forecast chip before its Task Link list
ok 1008 - Reading view appends a forecast chip before its Task Link list
  ---
  duration_ms: 7.074182
  ...
# Subtest: Live Preview places a chip widget at the end of the Pomodoro line
ok 1009 - Live Preview places a chip widget at the end of the Pomodoro line
  ---
  duration_ms: 0.993717
  ...
# Subtest: Live Preview skips chips in Source mode
ok 1010 - Live Preview skips chips in Source mode
  ---
  duration_ms: 0.221443
  ...
# Subtest: Reading view finds embedded Task Links via src
ok 1011 - Reading view finds embedded Task Links via src
  ---
  duration_ms: 0.582623
  ...
# Subtest: Obsidian frontmatter shapes unwrap nested wikilink arrays
ok 1012 - Obsidian frontmatter shapes unwrap nested wikilink arrays
  ---
  duration_ms: 0.175004
  ...
# Subtest: theme vectors: components split and key like bob
ok 1013 - theme vectors: components split and key like bob
  ---
  duration_ms: 1.956636
  ...
# Subtest: theme vectors: hue rule resolves pin, exempt, area, then hash
ok 1014 - theme vectors: hue rule resolves pin, exempt, area, then hash
  ---
  duration_ms: 0.394273
  ...
# Subtest: theme vectors: journal fold is last writer wins with rename moves
ok 1015 - theme vectors: journal fold is last writer wins with rename moves
  ---
  duration_ms: 0.974551
  ...
# Subtest: theme vectors: history rank is exact, prefix, then substring
ok 1016 - theme vectors: history rank is exact, prefix, then substring
  ---
  duration_ms: 0.555811
  ...
# Subtest: theme hash hues match the known collisions
ok 1017 - theme hash hues match the known collisions
  ---
  duration_ms: 0.168352
  ...
# Subtest: theme similar keys follow the near-duplicate rule
ok 1018 - theme similar keys follow the near-duplicate rule
  ---
  duration_ms: 0.438648
  ...
# Subtest: theme decode accepts a schema 1 report and rejects the rest
ok 1019 - theme decode accepts a schema 1 report and rejects the rest
  ---
  duration_ms: 0.409011
  ...
# Subtest: theme write decode maps refusals and pre-writer bob output
ok 1020 - theme write decode maps refusals and pre-writer bob output
  ---
  duration_ms: 0.203359
  ...
# Subtest: theme components carry byte offsets excluding quotes and plus
ok 1021 - theme components carry byte offsets excluding quotes and plus
  ---
  duration_ms: 0.336462
  ...
# Subtest: theme pill models mark exempt components muted
ok 1022 - theme pill models mark exempt components muted
  ---
  duration_ms: 0.473434
  ...
# Subtest: theme name offsets anchor at the em dash of a ledger line
ok 1023 - theme name offsets anchor at the em dash of a ledger line
  ---
  duration_ms: 0.62833
  ...
# Subtest: parser accepts the PM1-PM5 conformance vectors verbatim
ok 1024 - parser accepts the PM1-PM5 conformance vectors verbatim
  ---
  duration_ms: 1.861675
  ...
# Subtest: parser rejects the PM7-PM12 conformance vectors verbatim
ok 1025 - parser rejects the PM7-PM12 conformance vectors verbatim
  ---
  duration_ms: 0.268934
  ...
# Subtest: PM6 with the ladder unknown omits P-labels instead of guessing
ok 1026 - PM6 with the ladder unknown omits P-labels instead of guessing
  ---
  duration_ms: 0.19383
  ...
# Subtest: PM13-PM17 ladder and line variants hold
ok 1027 - PM13-PM17 ladder and line variants hold
  ---
  duration_ms: 0.332876
  ...
# Subtest: no model output contains a double colon
ok 1028 - no model output contains a double colon
  ---
  duration_ms: 0.78028
  ...
# Subtest: element structure and the decorative/inheritColor options
ok 1029 - element structure and the decorative/inheritColor options
  ---
  duration_ms: 0.337074
  ...
# Subtest: Live Preview decorations fold space, reveal, and refuse
ok 1030 - Live Preview decorations fold space, reveal, and refuse
  ---
  duration_ms: 1.306275
  ...
# Subtest: a line with fresh and priority fields gets a disjoint decoration
ok 1031 - a line with fresh and priority fields gets a disjoint decoration
  ---
  duration_ms: 0.202457
  ...
# Subtest: widget mousedown reveals the field at the folded offset
ok 1032 - widget mousedown reveals the field at the folded offset
  ---
  duration_ms: 0.626958
  ...
# Subtest: rendered views split task nodes and skip exclusions
ok 1033 - rendered views split task nodes and skip exclusions
  ---
  duration_ms: 1.450921
  ...
# Subtest: ladder coercion is lenient: valid, partial, and unknown
ok 1034 - ladder coercion is lenient: valid, partial, and unknown
  ---
  duration_ms: 0.412949
  ...
# Subtest: ladder snapshot reads the file and reuses the cache
ok 1035 - ladder snapshot reads the file and reuses the cache
  ---
  duration_ms: 2.023224
  ...
# Subtest: ladder snapshot degrades on missing files and parse errors
ok 1036 - ladder snapshot degrades on missing files and parse errors
  ---
  duration_ms: 0.896632
  ...
# Subtest: ladder snapshot is unknown on mobile
ok 1037 - ladder snapshot is unknown on mobile
  ---
  duration_ms: 21.010663
  ...
# Subtest: api.priorityMarks v1 is additive, sync, and never throwing
ok 1038 - api.priorityMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 6.681661
  ...
# Subtest: session toggle and onload wiring
ok 1039 - session toggle and onload wiring
  ---
  duration_ms: 1.117223
  ...
# Subtest: styles.css contract: masks, both hosts, repair flag, resting
ok 1040 - styles.css contract: masks, both hosts, repair flag, resting
  ---
  duration_ms: 0.856786
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 1041 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 0.449038
  ...
# Subtest: P1/P3/P4: open entries mark plain and aliased links
ok 1042 - P1/P3/P4: open entries mark plain and aliased links
  ---
  duration_ms: 2.284363
  ...
# Subtest: P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
ok 1043 - P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark
  ---
  duration_ms: 3.202816
  ...
# Subtest: P5: closed entries never mark, even with 🍅 history
ok 1044 - P5: closed entries never mark, even with 🍅 history
  ---
  duration_ms: 0.852137
  ...
# Subtest: P6/P7: embedded and struck links never mark
ok 1045 - P6/P7: embedded and struck links never mark
  ---
  duration_ms: 0.347604
  ...
# Subtest: P8: both trailing-\# move-only forms mark
ok 1046 - P8: both trailing-\# move-only forms mark
  ---
  duration_ms: 0.338987
  ...
# Subtest: P9: nested and prose-mixed links never mark
ok 1047 - P9: nested and prose-mixed links never mark
  ---
  duration_ms: 0.232203
  ...
# Subtest: P10: fenced, off-section, and off-note links never mark
ok 1048 - P10: fenced, off-section, and off-note links never mark
  ---
  duration_ms: 0.520794
  ...
# Subtest: P11: unresolved targets and non-task blocks get no mark
ok 1049 - P11: unresolved targets and non-task blocks get no mark
  ---
  duration_ms: 0.634411
  ...
# Subtest: P13: a same-note target reads the live doc
ok 1050 - P13: a same-note target reads the live doc
  ---
  duration_ms: 1.117574
  ...
# Subtest: P14: expect() wins until the cache agrees or 4 s pass
ok 1051 - P14: expect() wins until the cache agrees or 4 s pass
  ---
  duration_ms: 1.322326
  ...
# Subtest: tooltip, element structure, and eq
ok 1052 - tooltip, element structure, and eq
  ---
  duration_ms: 0.395966
  ...
# Subtest: Live Preview places one widget at each In Progress link
ok 1053 - Live Preview places one widget at each In Progress link
  ---
  duration_ms: 0.584085
  ...
# Subtest: widget mousedown places the cursor at the link start
ok 1054 - widget mousedown places the cursor at the link start
  ---
  duration_ms: 0.384103
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
ok 1055 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 0.432526
  ...
# Subtest: Reading view marks In Progress rows and dedupes
ok 1056 - Reading view marks In Progress rows and dedupes
  ---
  duration_ms: 1.216323
  ...
# Subtest: Reading view refuses every non-mark row
ok 1057 - Reading view refuses every non-mark row
  ---
  duration_ms: 1.415032
  ...
# Subtest: Reading view allows the 🍅 prefix and the trailing \# marker
ok 1058 - Reading view allows the 🍅 prefix and the trailing \# marker
  ---
  duration_ms: 0.440732
  ...
# Subtest: api.progressMarks v1 is additive, sync, and never throwing
ok 1059 - api.progressMarks v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.765332
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 1060 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 1.216243
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 1061 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 0.613011
  ...
# Subtest: changed-file and rollover refreshes
ok 1062 - changed-file and rollover refreshes
  ---
  duration_ms: 0.594305
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 1063 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.134036
  ...
# Subtest: styles.css contract: glyph, box, motion, toggle, calm
ok 1064 - styles.css contract: glyph, box, motion, toggle, calm
  ---
  duration_ms: 0.953762
  ...
# Subtest: the board registers its code block processor and the Open Reading Board command
ok 1065 - the board registers its code block processor and the Open Reading Board command
  ---
  duration_ms: 7.617599
  ...
# Subtest: four lanes render with counts, list and listitem roles, and one hint
ok 1066 - four lanes render with counts, list and listitem roles, and one hint
  ---
  duration_ms: 13.425376
  ...
# Subtest: awake cards show kind, topic, added mark, counts, priority, and the pending-sync star
ok 1067 - awake cards show kind, topic, added mark, counts, priority, and the pending-sync star
  ---
  duration_ms: 5.84441
  ...
# Subtest: a path-valued Bob audio field produces exactly one visible music marker
ok 1068 - a path-valued Bob audio field produces exactly one visible music marker
  ---
  duration_ms: 3.916931
  ...
# Subtest: Snoozed shows Waking, date groups, and Waiting-on rows with their reasons
ok 1069 - Snoozed shows Waking, date groups, and Waiting-on rows with their reasons
  ---
  duration_ms: 6.642817
  ...
# Subtest: TODAY pills float linked cards first, and never appear without a ready Today cache
ok 1070 - TODAY pills float linked cards first, and never appear without a ready Today cache
  ---
  duration_ms: 7.490774
  ...
# Subtest: the PDF button needs the nav member, macOS, and a source_pdf
ok 1071 - the PDF button needs the nav member, macOS, and a source_pdf
  ---
  duration_ms: 19.500481
  ...
# Subtest: click, modifier-click, middle-click, and the Task button route to openLinkText
ok 1072 - click, modifier-click, middle-click, and the Task button route to openLinkText
  ---
  duration_ms: 2.789667
  ...
# Subtest: the board is one Tab stop and every key moves or acts
ok 1073 - the board is one Tab stop and every key moves or acts
  ---
  duration_ms: 21.013048
  ...
# Subtest: movement targets stay inside the lanes that show cards
ok 1074 - movement targets stay inside the lanes that show cards
  ---
  duration_ms: 0.715697
  ...
# Subtest: hovering a Waiting-on row outlines its prerequisite card on the board
ok 1075 - hovering a Waiting-on row outlines its prerequisite card on the board
  ---
  duration_ms: 2.99951
  ...
# Subtest: the board never calls a vault write API, in the source or in any gesture
ok 1076 - the board never calls a vault write API, in the source or in any gesture
  ---
  duration_ms: 11.453401
  ...
# Subtest: a repaint keeps focus by note path and each lane's scroll position
ok 1077 - a repaint keeps focus by note path and each lane's scroll position
  ---
  duration_ms: 7.684073
  ...
# Subtest: a task move and topic/type update repaint handlers while preserving focus and scroll
ok 1078 - a task move and topic/type update repaint handlers while preserving focus and scroll
  ---
  duration_ms: 8.145418
  ...
# Subtest: prerequisite identity changes repaint highlighting even when reason text is unchanged
ok 1079 - prerequisite identity changes repaint highlighting even when reason text is unchanged
  ---
  duration_ms: 11.01819
  ...
# Subtest: an unchanged board is not repainted; only the data time updates in place
ok 1080 - an unchanged board is not repainted; only the data time updates in place
  ---
  duration_ms: 4.100781
  ...
# Subtest: a Today cache change repaints boards from cached data without spawning bob
ok 1081 - a Today cache change repaints boards from cached data without spawning bob
  ---
  duration_ms: 5.805446
  ...
# Subtest: first paint is a skeleton in the real grid, then the board without a layout jump
ok 1082 - first paint is a skeleton in the real grid, then the board without a layout jump
  ---
  duration_ms: 7.19354
  ...
# Subtest: failures without a frame render an actionable card with Retry
ok 1083 - failures without a frame render an actionable card with Retry
  ---
  duration_ms: 32.655732
  ...
# Subtest: a failed manual refresh keeps the last frame and says why with Retry
ok 1084 - a failed manual refresh keeps the last frame and says why with Retry
  ---
  duration_ms: 7.061344
  ...
# Subtest: metadata revalidation delivers a silent stale-frame error and recovery updates freshness
ok 1085 - metadata revalidation delivers a silent stale-frame error and recovery updates freshness
  ---
  duration_ms: 11.402504
  ...
# Subtest: stale-cache mount refresh failures reach the mounted view
ok 1086 - stale-cache mount refresh failures reach the mounted view
  ---
  duration_ms: 7.679267
  ...
# Subtest: unload during a fetch prevents late repaint and queued spawns
ok 1087 - unload during a fetch prevents late repaint and queued spawns
  ---
  duration_ms: 4.247522
  ...
# Subtest: in-flight edits and forced refreshes coalesce without dropping mounted fences
ok 1088 - in-flight edits and forced refreshes coalesce without dropping mounted fences
  ---
  duration_ms: 16.607433
  ...
# Subtest: manual refresh shows a busy state until the result lands, then announces it
ok 1089 - manual refresh shows a busy state until the result lands, then announces it
  ---
  duration_ms: 6.83282
  ...
# Subtest: an older bob without blocked_by falls back to Waiting-on with one lint line
ok 1090 - an older bob without blocked_by falls back to Waiting-on with one lint line
  ---
  duration_ms: 5.549848
  ...
# Subtest: an empty queue shows bob's own phrase instead of lanes
ok 1091 - an empty queue shows bob's own phrase instead of lanes
  ---
  duration_ms: 1.229457
  ...
# Subtest: fence options reach the fetch and bad options show as muted lint lines
ok 1092 - fence options reach the fetch and bad options show as muted lint lines
  ---
  duration_ms: 6.104407
  ...
# Subtest: Snoozed collapses per source path, leaves the key order, and survives repaints
ok 1093 - Snoozed collapses per source path, leaves the key order, and survives repaints
  ---
  duration_ms: 17.843186
  ...
# Subtest: unloading a block releases its view, and teardown clears the session state
ok 1094 - unloading a block releases its view, and teardown clears the session state
  ---
  duration_ms: 2.370166
  ...
# Subtest: reading board stylesheet contract: selectors, layout, tabular-nums, motion, colors
ok 1095 - reading board stylesheet contract: selectors, layout, tabular-nums, motion, colors
  ---
  duration_ms: 0.873999
  ...
# Subtest: Reading Board argv carries bob's fixed queue and optional fence filters
ok 1096 - Reading Board argv carries bob's fixed queue and optional fence filters
  ---
  duration_ms: 1.44542
  ...
# Subtest: Reading Board decoder accepts the shared bob fixture and normalizes optional fields
ok 1097 - Reading Board decoder accepts the shared bob fixture and normalizes optional fields
  ---
  duration_ms: 0.252512
  ...
# Subtest: Reading Board audio presence survives raw JSON decoding and model construction
ok 1098 - Reading Board audio presence survives raw JSON decoding and model construction
  ---
  duration_ms: 4.669899
  ...
# Subtest: Reading Board decoder rejects malformed JSON, shapes, schema, and bob errors
ok 1099 - Reading Board decoder rejects malformed JSON, shapes, schema, and bob errors
  ---
  duration_ms: 0.244176
  ...
# Subtest: shared bob spawn passes the vault environment, timeout, and buffer
ok 1100 - shared bob spawn passes the vault environment, timeout, and buffer
  ---
  duration_ms: 6.414431
  ...
# Subtest: shared bob spawn maps missing binary and timeout failures
ok 1101 - shared bob spawn maps missing binary and timeout failures
  ---
  duration_ms: 2.1418
  ...
# Subtest: Reading Board error cards explain not-found, timeout, schema, and bob errors
ok 1102 - Reading Board error cards explain not-found, timeout, schema, and bob errors
  ---
  duration_ms: 0.398421
  ...
# Subtest: Reading Board cache returns stale data while revalidating and keeps a four-entry LRU
ok 1103 - Reading Board cache returns stale data while revalidating and keeps a four-entry LRU
  ---
  duration_ms: 1.599104
  ...
# Subtest: Reading Board shares identical flights and coalesces one different follow-up
ok 1104 - Reading Board shares identical flights and coalesces one different follow-up
  ---
  duration_ms: 1.149215
  ...
# Subtest: Reading Board refresh is mounted-only, debounced, and reacts to rollover and stale active leaves
ok 1105 - Reading Board refresh is mounted-only, debounced, and reacts to rollover and stale active leaves
  ---
  duration_ms: 0.766975
  ...
# Subtest: the shared bob output builds the expected four lanes and preserves bob order
ok 1106 - the shared bob output builds the expected four lanes and preserves bob order
  ---
  duration_ms: 4.903505
  ...
# Subtest: each status uses its awake lane and every blocked status uses Snoozed
ok 1107 - each status uses its awake lane and every blocked status uses Snoozed
  ---
  duration_ms: 0.491739
  ...
# Subtest: Today floats cards by ledger rank only when the cache is ready
ok 1108 - Today floats cards by ledger rank only when the cache is ready
  ---
  duration_ms: 1.184753
  ...
# Subtest: Snoozed groups show waking, schedule, dependency, project, return lane, and mark models
ok 1109 - Snoozed groups show waking, schedule, dependency, project, return lane, and mark models
  ---
  duration_ms: 0.709244
  ...
# Subtest: schedule groups follow Monday-start weeks through Sunday across month and year ends
ok 1110 - schedule groups follow Monday-start weeks through Sunday across month and year ends
  ---
  duration_ms: 0.305142
  ...
# Subtest: older bob output remains visible in Waiting on and explains the missing reasons
ok 1111 - older bob output remains visible in Waiting on and explains the missing reasons
  ---
  duration_ms: 0.890811
  ...
# Subtest: fence options accept parent and type lists while turning bad input into lints
ok 1112 - fence options accept parent and type lists while turning bad input into lints
  ---
  duration_ms: 1.3409
  ...
# Subtest: kind names, title code spans, and render signatures are deterministic
ok 1113 - kind names, title code spans, and render signatures are deterministic
  ---
  duration_ms: 2.969691
  ...
# Subtest: max_ready defaults to 100 for missing, absent, and null values
ok 1114 - max_ready defaults to 100 for missing, absent, and null values
  ---
  duration_ms: 1.523479
  ...
# Subtest: max_ready accepts a custom positive cap
ok 1115 - max_ready accepts a custom positive cap
  ---
  duration_ms: 0.218036
  ...
# Subtest: max_ready rejects zero, negative, fractions, strings, booleans, and overflow
ok 1116 - max_ready rejects zero, negative, fractions, strings, booleans, and overflow
  ---
  duration_ms: 0.999239
  ...
# Subtest: old configurations and legacy max_now still load
ok 1117 - old configurations and legacy max_now still load
  ---
  duration_ms: 0.40805
  ...
# Subtest: READY boundary: only a strict excess turns red
ok 1118 - READY boundary: only a strict excess turns red
  ---
  duration_ms: 2.076176
  ...
# Subtest: READY custom-cap boundary
ok 1119 - READY custom-cap boundary
  ---
  duration_ms: 0.266298
  ...
# Subtest: READY over is independent of the PLAN ledger status
ok 1120 - READY over is independent of the PLAN ledger status
  ---
  duration_ms: 4.841526
  ...
# Subtest: READY predicate: statuses, custom TODO symbols, and non-tasks
ok 1121 - READY predicate: statuses, custom TODO symbols, and non-tasks
  ---
  duration_ms: 0.195243
  ...
# Subtest: READY predicate: blocked uses the full list, even outside the queue
ok 1122 - READY predicate: blocked uses the full list, even outside the queue
  ---
  duration_ms: 0.470648
  ...
# Subtest: READY predicate: past, today, and future schedules
ok 1123 - READY predicate: past, today, and future schedules
  ---
  duration_ms: 0.522228
  ...
# Subtest: READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
ok 1124 - READY predicate: dash self-exclusion, daily files, templates, conflicts, hide
  ---
  duration_ms: 0.401226
  ...
# Subtest: READY predicate: Today exclusion
ok 1125 - READY predicate: Today exclusion
  ---
  duration_ms: 0.170646
  ...
# Subtest: readyTaskVisible excludes hide variants like Tasks
ok 1126 - readyTaskVisible excludes hide variants like Tasks
  ---
  duration_ms: 0.173291
  ...
# Subtest: daily and dashboard share the READY element contract
ok 1127 - daily and dashboard share the READY element contract
  ---
  duration_ms: 13.922676
  ...
# Subtest: READY placeholder keeps the limit in its tooltip
ok 1128 - READY placeholder keeps the limit in its tooltip
  ---
  duration_ms: 0.17803
  ...
# Subtest: READY keyboard and modifier-key navigation
ok 1129 - READY keyboard and modifier-key navigation
  ---
  duration_ms: 1.671472
  ...
# Subtest: READY unavailable without Tasks, on Cold/Initializing, or before Today
ok 1130 - READY unavailable without Tasks, on Cold/Initializing, or before Today
  ---
  duration_ms: 3.095322
  ...
# Subtest: READY counts a valid empty queue as zero, not unavailable
ok 1131 - READY counts a valid empty queue as zero, not unavailable
  ---
  duration_ms: 1.177209
  ...
# Subtest: READY stays compatible with hosts exposing only getTasks()
ok 1132 - READY stays compatible with hosts exposing only getTasks()
  ---
  duration_ms: 3.17265
  ...
# Subtest: READY degrades to unavailable when the Today predicate throws
ok 1133 - READY degrades to unavailable when the Today predicate throws
  ---
  duration_ms: 0.787173
  ...
# Subtest: READY renders label/value spans for every budget state
ok 1134 - READY renders label/value spans for every budget state
  ---
  duration_ms: 1.981664
  ...
# Subtest: READY live refresh keeps the anchor, spans, and handlers
ok 1135 - READY live refresh keeps the anchor, spans, and handlers
  ---
  duration_ms: 1.660922
  ...
# Subtest: READY refresh crosses the over-cap boundary and back
ok 1136 - READY refresh crosses the over-cap boundary and back
  ---
  duration_ms: 0.931609
  ...
# Subtest: READY refresh crosses the unavailable boundary and back
ok 1137 - READY refresh crosses the unavailable boundary and back
  ---
  duration_ms: 0.829654
  ...
# Subtest: READY never assigns the Obsidian text setter
ok 1138 - READY never assigns the Obsidian text setter
  ---
  duration_ms: 1.601318
  ...
# Subtest: READY gating excludes review buckets and keeps the partition
ok 1139 - READY gating excludes review buckets and keeps the partition
  ---
  duration_ms: 0.438217
  ...
# Subtest: gated READY tooltip carries total lane pressure
ok 1140 - gated READY tooltip carries total lane pressure
  ---
  duration_ms: 0.167209
  ...
# Subtest: planBlockModel gates READY and shares the lane tooltip
ok 1141 - planBlockModel gates READY and shares the lane tooltip
  ---
  duration_ms: 0.776693
  ...
# Subtest: READY lint appears only on a strict excess
ok 1142 - READY lint appears only on a strict excess
  ---
  duration_ms: 4.008254
  ...
# Subtest: READY lint uses a custom cap
ok 1143 - READY lint uses a custom cap
  ---
  duration_ms: 0.544199
  ...
# Subtest: lane lints appear in NEXT, PENDING, READY order
ok 1144 - lane lints appear in NEXT, PENDING, READY order
  ---
  duration_ms: 2.715595
  ...
# Subtest: READY lint uses the gated count
ok 1145 - READY lint uses the gated count
  ---
  duration_ms: 1.588243
  ...
# Subtest: READY lint stays silent while unavailable
ok 1146 - READY lint stays silent while unavailable
  ---
  duration_ms: 0.431564
  ...
# Subtest: READY speaks each host's chip language (daily single-tone, dash two-tone)
ok 1147 - READY speaks each host's chip language (daily single-tone, dash two-tone)
  ---
  duration_ms: 5.675099
  ...
# Subtest: daily paint carries lane pressure to the shared READY renderer
ok 1148 - daily paint carries lane pressure to the shared READY renderer
  ---
  duration_ms: 21.990103
  ...
# Subtest: daily paint degrades to the legacy tooltip without freshness
ok 1149 - daily paint degrades to the legacy tooltip without freshness
  ---
  duration_ms: 5.050296
  ...
# Subtest: work tones: READY model carries the displayed-count tone
ok 1150 - work tones: READY model carries the displayed-count tone
  ---
  duration_ms: 0.313909
  ...
# Subtest: recurrence helpers are exported and frozen where shaped
ok 1151 - recurrence helpers are exported and frozen where shaped
  ---
  duration_ms: 2.117124
  ...
# Subtest: RM1 daily with when done: fold, label, tooltip
ok 1152 - RM1 daily with when done: fold, label, tooltip
  ---
  duration_ms: 1.159144
  ...
# Subtest: RM2 non-checklist row without when done still marks
ok 1153 - RM2 non-checklist row without when done still marks
  ---
  duration_ms: 0.80112
  ...
# Subtest: RM3 weekday plurals keep the full name
ok 1154 - RM3 weekday plurals keep the full name
  ---
  duration_ms: 0.481299
  ...
# Subtest: RM4 monthly ordinals use the written token
ok 1155 - RM4 monthly ordinals use the written token
  ---
  duration_ms: 0.404923
  ...
# Subtest: RM5 every N days stays verbatim with its count
ok 1156 - RM5 every N days stays verbatim with its count
  ---
  duration_ms: 0.129156
  ...
# Subtest: RM6 weekly, N-week, and yearly forms
ok 1157 - RM6 weekly, N-week, and yearly forms
  ---
  duration_ms: 0.36131
  ...
# Subtest: RM7 week lists join with Tue, Fri and weekday alone
ok 1158 - RM7 week lists join with Tue, Fri and weekday alone
  ---
  duration_ms: 0.161048
  ...
# Subtest: RM8 unknown rules stay verbatim
ok 1159 - RM8 unknown rules stay verbatim
  ---
  duration_ms: 0.564668
  ...
# Subtest: RM9 parens and padded brackets are canonical
ok 1160 - RM9 parens and padded brackets are canonical
  ---
  duration_ms: 0.642066
  ...
# Subtest: RM10 case is preserved in the rule and tooltip
ok 1161 - RM10 case is preserved in the rule and tooltip
  ---
  duration_ms: 0.243434
  ...
# Subtest: RM11 cursor in the field reveals it, RM12 closed rows still mark
ok 1162 - RM11 cursor in the field reveals it, RM12 closed rows still mark
  ---
  duration_ms: 0.307427
  ...
# Subtest: RN1 unreadable rules get no mark
ok 1163 - RN1 unreadable rules get no mark
  ---
  duration_ms: 0.854752
  ...
# Subtest: RN2 the checklist guard follows membership, not the glyph slot
ok 1164 - RN2 the checklist guard follows membership, not the glyph slot
  ---
  duration_ms: 0.199882
  ...
# Subtest: RN3 code still parses pure but decorates nothing
ok 1165 - RN3 code still parses pure but decorates nothing
  ---
  duration_ms: 0.2407
  ...
# Subtest: element anatomy: repeat host, rule, quiet tone, no date
ok 1166 - element anatomy: repeat host, rule, quiet tone, no date
  ---
  duration_ms: 0.468915
  ...
# Subtest: family dispatch keeps dates working and sorts adds
ok 1167 - family dispatch keeps dates working and sorts adds
  ---
  duration_ms: 0.653067
  ...
# Subtest: Live Preview decorates repeat and respects the guard and code
ok 1168 - Live Preview decorates repeat and respects the guard and code
  ---
  duration_ms: 1.106883
  ...
# Subtest: RR1 reading view honors the guard, RO2 rollover skips repeat
ok 1169 - RR1 reading view honors the guard, RO2 rollover skips repeat
  ---
  duration_ms: 2.489965
  ...
# Subtest: RA1 api.dateMarks stays dates-only and tooltips never contain ::
ok 1170 - RA1 api.dateMarks stays dates-only and tooltips never contain ::
  ---
  duration_ms: 0.406807
  ...
# Subtest: styles.css contract: repeat glyph, ink, resting, repair flag
ok 1171 - styles.css contract: repeat glyph, ink, resting, repair flag
  ---
  duration_ms: 1.0471
  ...
# Subtest: LC1 one unlabelled open target renders links-to arrow chip
ok 1172 - LC1 one unlabelled open target renders links-to arrow chip
  ---
  duration_ms: 2.80681
  ...
# Subtest: LC2 labelled target carries a pill
ok 1173 - LC2 labelled target carries a pill
  ---
  duration_ms: 0.461632
  ...
# Subtest: LC3 closed and archived targets dim without strike; \#hide mutes
ok 1174 - LC3 closed and archived targets dim without strike; \#hide mutes
  ---
  duration_ms: 1.979169
  ...
# Subtest: LC4 unresolvable target is a dashed missing chip
ok 1175 - LC4 unresolvable target is a dashed missing chip
  ---
  duration_ms: 0.487951
  ...
# Subtest: LC5 LINKED FROM shows the builtin inverse phrase
ok 1176 - LC5 LINKED FROM shows the builtin inverse phrase
  ---
  duration_ms: 0.614263
  ...
# Subtest: LC6 LINKED FROM with an unknown label reads chip, label, this
ok 1177 - LC6 LINKED FROM with an unknown label reads chip, label, this
  ---
  duration_ms: 0.547716
  ...
# Subtest: LC7 live edges missing from the text append in canonical order
ok 1178 - LC7 live edges missing from the text append in canonical order
  ---
  duration_ms: 0.552165
  ...
# Subtest: LC8 stored entries that are no longer live are dashed and uncounted
ok 1179 - LC8 stored entries that are no longer live are dashed and uncounted
  ---
  duration_ms: 0.458055
  ...
# Subtest: LC9 three or more closed chips collapse to ✓×N and expand
ok 1180 - LC9 three or more closed chips collapse to ✓×N and expand
  ---
  duration_ms: 1.014848
  ...
# Subtest: LC10 labelled rows wrap one entry per visual row
ok 1181 - LC10 labelled rows wrap one entry per visual row
  ---
  duration_ms: 0.959583
  ...
# Subtest: LC11 controls need api.relations v1; linked_from_remove calls removeLink(S, T)
ok 1182 - LC11 controls need api.relations v1; linked_from_remove calls removeLink(S, T)
  ---
  duration_ms: 1.532867
  ...
# Subtest: LC12 toggle-dependency-chips covers both relation rows
ok 1183 - LC12 toggle-dependency-chips covers both relation rows
  ---
  duration_ms: 0.700528
  ...
# Subtest: LC13 malformed and not-a-line rows have no model
ok 1184 - LC13 malformed and not-a-line rows have no model
  ---
  duration_ms: 0.255057
  ...
# Subtest: LC14 unsaved editor text refreshes the live model
ok 1185 - LC14 unsaved editor text refreshes the live model
  ---
  duration_ms: 14.540159
  ...
# Subtest: Live Preview decorates relation rows from the index
ok 1186 - Live Preview decorates relation rows from the index
  ---
  duration_ms: 3.831838
  ...
# Subtest: Reading view decorates stored anchors and appends live edges
ok 1187 - Reading view decorates stored anchors and appends live edges
  ---
  duration_ms: 3.070283
  ...
# Subtest: Reading view with api.relations v1 shows ＋ and ×
ok 1188 - Reading view with api.relations v1 shows ＋ and ×
  ---
  duration_ms: 1.763398
  ...
# Subtest: ledger parser agrees with shared LK vectors and parses source task children
ok 1189 - ledger parser agrees with shared LK vectors and parses source task children
  ---
  duration_ms: 3.92237
  ...
# Subtest: relationIndex scans done sources, resolves both directions, and orders label suggestions
ok 1190 - relationIndex scans done sources, resolves both directions, and orders label suggestions
  ---
  duration_ms: 8.345908
  ...
# Subtest: relationIndex applies changed, delete, rename, and unsaved editor overlays
ok 1191 - relationIndex applies changed, delete, rename, and unsaved editor overlays
  ---
  duration_ms: 24.689941
  ...
# Subtest: relationIndex registers after layout-ready and never reads non-markdown during startup replay
ok 1192 - relationIndex registers after layout-ready and never reads non-markdown during startup replay
  ---
  duration_ms: 36.076947
  ...
# Subtest: relationIndex ignores non-markdown live events
ok 1193 - relationIndex ignores non-markdown live events
  ---
  duration_ms: 31.820657
  ...
# Subtest: relationIndex layout-ready after unload registers nothing
ok 1194 - relationIndex layout-ready after unload registers nothing
  ---
  duration_ms: 31.883428
  ...
# Subtest: parseTaskRelationFile indexes every checkbox status as a task
ok 1195 - parseTaskRelationFile indexes every checkbox status as a task
  ---
  duration_ms: 0.94803
  ...
# Subtest: relationIndex incoming and suggestions include Next and Blocked sources
ok 1196 - relationIndex incoming and suggestions include Next and Blocked sources
  ---
  duration_ms: 6.029915
  ...
# Subtest: relation-label JS mirrors match the shared bob-cli vectors
ok 1197 - relation-label JS mirrors match the shared bob-cli vectors
  ---
  duration_ms: 2.092585
  ...
# Subtest: api.relationLabels reads folded preferences and delegates desktop writes to bob
ok 1198 - api.relationLabels reads folded preferences and delegates desktop writes to bob
  ---
  duration_ms: 1.213377
  ...
# Subtest: ledger LK1–LK19 recognises relation shapes and keeps them out of plan links
ok 1199 - ledger LK1–LK19 recognises relation shapes and keeps them out of plan links
  ---
  duration_ms: 2.693213
  ...
# Subtest: parseTrigger parses D[-]<N> dated-entry triggers with offset and span
ok 1200 - parseTrigger parses D[-]<N> dated-entry triggers with offset and span
  ---
  duration_ms: 2.463134
  ...
# Subtest: computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
ok 1201 - computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset
  ---
  duration_ms: 0.603863
  ...
# Subtest: expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
ok 1202 - expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation
  ---
  duration_ms: 0.622238
  ...
# Subtest: findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
ok 1203 - findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers
  ---
  duration_ms: 0.45032
  ...
# Subtest: compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
ok 1204 - compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported
  ---
  duration_ms: 0.433197
  ...
# Subtest: parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
ok 1205 - parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans
  ---
  duration_ms: 0.216584
  ...
# Subtest: computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
ok 1206 - computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers
  ---
  duration_ms: 0.299843
  ...
# Subtest: findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
ok 1207 - findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix
  ---
  duration_ms: 0.276929
  ...
# Subtest: findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
ok 1208 - findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens
  ---
  duration_ms: 0.450741
  ...
# Subtest: expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
ok 1209 - expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true
  ---
  duration_ms: 0.912202
  ...
# Subtest: regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
ok 1210 - regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger
  ---
  duration_ms: 0.541304
  ...
# Subtest: expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
ok 1211 - expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position
  ---
  duration_ms: 0.415053
  ...
# Subtest: stats fence body sets defaults only and ignores the rest
ok 1212 - stats fence body sets defaults only and ignores the rest
  ---
  duration_ms: 2.378663
  ...
# Subtest: stats tile models cover every unit and every quality
ok 1213 - stats tile models cover every unit and every quality
  ---
  duration_ms: 0.689998
  ...
# Subtest: stats spark bars mark null gaps, zero ticks, and hollow today
ok 1214 - stats spark bars mark null gaps, zero ticks, and hollow today
  ---
  duration_ms: 0.411956
  ...
# Subtest: stats table rows and CSV share the same points
ok 1215 - stats table rows and CSV share the same points
  ---
  duration_ms: 0.894869
  ...
# Subtest: stats overview ids prefer the fence, then config, then report order
ok 1216 - stats overview ids prefer the fence, then config, then report order
  ---
  duration_ms: 1.295685
  ...
# Subtest: stats window label always states today and tracking start
ok 1217 - stats window label always states today and tracking start
  ---
  duration_ms: 0.307928
  ...
# Subtest: stats view state is session-only and per source path
ok 1218 - stats view state is session-only and per source path
  ---
  duration_ms: 7.613891
  ...
# Subtest: stats block renders header, tiles, table, and footer from JSON
ok 1219 - stats block renders header, tiles, table, and footer from JSON
  ---
  duration_ms: 46.28073
  ...
# Subtest: stats block shows an actionable card with Retry when bob fails
ok 1220 - stats block shows an actionable card with Retry when bob fails
  ---
  duration_ms: 44.039503
  ...
# Subtest: stats block registers the processor and the Open Stats command
ok 1221 - stats block registers the processor and the Open Stats command
  ---
  duration_ms: 1.779158
  ...
# Subtest: stats revalidation gates on visibility: hidden views never spawn
ok 1222 - stats revalidation gates on visibility: hidden views never spawn
  ---
  duration_ms: 92.404543
  ...
# Subtest: stats background tabs never spawn until the tab is visible again
ok 1223 - stats background tabs never spawn until the tab is visible again
  ---
  duration_ms: 75.834632
  ...
# Subtest: stats cache subscriber repaints only shown views reading the key
ok 1224 - stats cache subscriber repaints only shown views reading the key
  ---
  duration_ms: 23.3281
  ...
# Subtest: stats local-date rollover bumps the change generation once per day
ok 1225 - stats local-date rollover bumps the change generation once per day
  ---
  duration_ms: 2.066917
  ...
# Subtest: stats stylesheet contract: selectors, tabular-nums, motion, colors
ok 1226 - stats stylesheet contract: selectors, tabular-nums, motion, colors
  ---
  duration_ms: 2.09507
  ...
# Subtest: Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
ok 1227 - Stats chart geometry stays finite across empty, constant, signed, and narrow inputs
  ---
  duration_ms: 6.449367
  ...
# Subtest: prior buckets align by elapsed position and omit invalid and provisional points
ok 1228 - prior buckets align by elapsed position and omit invalid and provisional points
  ---
  duration_ms: 1.09459
  ...
# Subtest: chart renders SVG safely and keeps secondary focus metrics selectable
ok 1229 - chart renders SVG safely and keeps secondary focus metrics selectable
  ---
  duration_ms: 13.014333
  ...
# Subtest: grouped chart pins honest buckets, bounds daily detail, and opens validated notes
ok 1230 - grouped chart pins honest buckets, bounds daily detail, and opens validated notes
  ---
  duration_ms: 12.055051
  ...
# Subtest: local focus, table, pin, and definition changes reuse the retained report
ok 1231 - local focus, table, pin, and definition changes reuse the retained report
  ---
  duration_ms: 11.355837
  ...
# Subtest: keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
ok 1232 - keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts
  ---
  duration_ms: 38.466298
  ...
# Subtest: schema-1 fallback keeps day quartiles and never invents grouped daily history
ok 1233 - schema-1 fallback keeps day quartiles and never invents grouped daily history
  ---
  duration_ms: 5.102414
  ...
# Subtest: ResizeObserver redraws cached data and disconnects across rerenders and unload
ok 1234 - ResizeObserver redraws cached data and disconnects across rerenders and unload
  ---
  duration_ms: 133.026611
  ...
# Subtest: stats resolution prefers stats.bob_path, then candidates, then PATH
ok 1235 - stats resolution prefers stats.bob_path, then candidates, then PATH
  ---
  duration_ms: 1.686001
  ...
# Subtest: stats home expansion and range/offset normalization
ok 1236 - stats home expansion and range/offset normalization
  ---
  duration_ms: 0.3353
  ...
# Subtest: stats fetch always runs show -a -f json plus the chosen flags
ok 1237 - stats fetch always runs show -a -f json plus the chosen flags
  ---
  duration_ms: 0.329639
  ...
# Subtest: stats group emits -g before metric ids and rejects the rest
ok 1238 - stats group emits -g before metric ids and rejects the rest
  ---
  duration_ms: 0.242433
  ...
# Subtest: stats request resolves one shared key for the page and strip defaults
ok 1239 - stats request resolves one shared key for the page and strip defaults
  ---
  duration_ms: 1.077037
  ...
# Subtest: stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
ok 1240 - stats spawn passes vault env, NO_COLOR, timeout, and a large buffer
  ---
  duration_ms: 8.418697
  ...
# Subtest: stats spawn maps ENOENT, timeouts, and stderr to named errors
ok 1241 - stats spawn maps ENOENT, timeouts, and stderr to named errors
  ---
  duration_ms: 2.339317
  ...
# Subtest: stats decode accepts schema 1 and rejects the rest defensively
ok 1242 - stats decode accepts schema 1 and rejects the rest defensively
  ---
  duration_ms: 0.231692
  ...
# Subtest: stats error cards name the cause and the stats.bob_path fix
ok 1243 - stats error cards name the cause and the stats.bob_path fix
  ---
  duration_ms: 0.46628
  ...
# Subtest: stats fetch shares one flight per key and queues distinct keys FIFO
ok 1244 - stats fetch shares one flight per key and queues distinct keys FIFO
  ---
  duration_ms: 22.989153
  ...
# Subtest: stats fetch never loses waiters: A in flight, B then C settle with own reports
ok 1245 - stats fetch never loses waiters: A in flight, B then C settle with own reports
  ---
  duration_ms: 1.972637
  ...
# Subtest: stats queue caps at 8 distinct pending keys with explicit cancellation
ok 1246 - stats queue caps at 8 distinct pending keys with explicit cancellation
  ---
  duration_ms: 3.557162
  ...
# Subtest: stats cache is a 16-entry LRU keyed by the argument list
ok 1247 - stats cache is a 16-entry LRU keyed by the argument list
  ---
  duration_ms: 3.106211
  ...
# Subtest: stats warm remount with a clean fresh entry spawns nothing
ok 1248 - stats warm remount with a clean fresh entry spawns nothing
  ---
  duration_ms: 1.253363
  ...
# Subtest: stats change bump makes the next hit spawn exactly once
ok 1249 - stats change bump makes the next hit spawn exactly once
  ---
  duration_ms: 1.432596
  ...
# Subtest: stats change during a flight leaves the stored entry dirty
ok 1250 - stats change during a flight leaves the stored entry dirty
  ---
  duration_ms: 2.453695
  ...
# Subtest: stats entries older than the max clean age read dirty
ok 1251 - stats entries older than the max clean age read dirty
  ---
  duration_ms: 1.453726
  ...
# Subtest: stats revalidate never skips a miss but skips dirty hits
ok 1252 - stats revalidate never skips a miss but skips dirty hits
  ---
  duration_ms: 0.885862
  ...
# Subtest: stats peek reads synchronously and listeners fire per store
ok 1253 - stats peek reads synchronously and listeners fire per store
  ---
  duration_ms: 1.401867
  ...
# Subtest: stats unload settles every waiter with cancellation
ok 1254 - stats unload settles every waiter with cancellation
  ---
  duration_ms: 0.82718
  ...
# Subtest: stats spawn counters record each spawn
ok 1255 - stats spawn counters record each spawn
  ---
  duration_ms: 0.643689
  ...
# Subtest: stats block views count as shown without a visibility host
ok 1256 - stats block views count as shown without a visibility host
  ---
  duration_ms: 0.156469
  ...
# Subtest: stats api v2 keeps append and adds fetch plus bobPath
ok 1257 - stats api v2 keeps append and adds fetch plus bobPath
  ---
  duration_ms: 0.61762
  ...
# Subtest: statsHomeDir defaults to the real home and strips a trailing slash
ok 1258 - statsHomeDir defaults to the real home and strips a trailing slash
  ---
  duration_ms: 0.136692
  ...
# Subtest: stats mac regression: un-injected resolution probes the real home first
ok 1259 - stats mac regression: un-injected resolution probes the real home first
  ---
  duration_ms: 0.166248
  ...
# Subtest: stats absolute candidates are probed verbatim with no doubled slashes
ok 1260 - stats absolute candidates are probed verbatim with no doubled slashes
  ---
  duration_ms: 0.197057
  ...
# Subtest: stats with no home probes only absolute candidates
ok 1261 - stats with no home probes only absolute candidates
  ---
  duration_ms: 0.145267
  ...
# Subtest: stats tilde config expands against the real home
ok 1262 - stats tilde config expands against the real home
  ---
  duration_ms: 0.115651
  ...
# Subtest: stats candidate and tried lists share one source of truth
ok 1263 - stats candidate and tried lists share one source of truth
  ---
  duration_ms: 0.114258
  ...
# Subtest: stats spawn bob-not-found tried list uses the real home
ok 1264 - stats spawn bob-not-found tried list uses the real home
  ---
  duration_ms: 1.164595
  ...
# Subtest: stats unload clears views, timers, cache, flights, and queues
ok 1265 - stats unload clears views, timers, cache, flights, and queues
  ---
  duration_ms: 0.896102
  ...
# Subtest: stats queue outcomes carry fetchedAt
ok 1266 - stats queue outcomes carry fetchedAt
  ---
  duration_ms: 1.129317
  ...
# Subtest: stats namespace v1 serializes versioned review answer JSONL
ok 1267 - stats namespace v1 serializes versioned review answer JSONL
  ---
  duration_ms: 13.915253
  ...
# Subtest: stats journal rejects invalid calendar days and outcomes
ok 1268 - stats journal rejects invalid calendar days and outcomes
  ---
  duration_ms: 1.945084
  ...
# Subtest: statsReviewHost lowercases, cuts at the first dot, and never throws
ok 1269 - statsReviewHost lowercases, cuts at the first dot, and never throws
  ---
  duration_ms: 0.169934
  ...
# Subtest: stats journal plugin passthrough keeps a semver writer and falls back otherwise
ok 1270 - stats journal plugin passthrough keeps a semver writer and falls back otherwise
  ---
  duration_ms: 1.153904
  ...
# Subtest: panel dispatch covers every family, custom kinds, and the net exception
ok 1271 - panel dispatch covers every family, custom kinds, and the net exception
  ---
  duration_ms: 1.142151
  ...
# Subtest: pomodoro panel shows the supplied total, shares, hue, and safe text
ok 1272 - pomodoro panel shows the supplied total, shares, hue, and safe text
  ---
  duration_ms: 21.965328
  ...
# Subtest: home parts use the report catalog for labels, hue slots, and pinned values
ok 1273 - home parts use the report catalog for labels, hue slots, and pinned values
  ---
  duration_ms: 11.75146
  ...
# Subtest: roots panel toggles Themes, pins spans, discloses sub-projects, and opens home links
ok 1274 - roots panel toggles Themes, pins spans, discloses sub-projects, and opens home links
  ---
  duration_ms: 20.54694
  ...
# Subtest: a stale areas view maps to Root parents, and old bob falls back with copy
ok 1275 - a stale areas view maps to Root parents, and old bob falls back with copy
  ---
  duration_ms: 11.819931
  ...
# Subtest: Themes panel prefers report.theme_hues names and hues over the api lookup
ok 1276 - Themes panel prefers report.theme_hues names and hues over the api lookup
  ---
  duration_ms: 3.570981
  ...
# Subtest: chart pin refreshes Where the time went and Themes honor the pinned span
ok 1277 - chart pin refreshes Where the time went and Themes honor the pinned span
  ---
  duration_ms: 7.380896
  ...
# Subtest: review rows keep their area hue and a missing homes report keeps the saved view
ok 1278 - review rows keep their area hue and a missing homes report keeps the saved view
  ---
  duration_ms: 3.762474
  ...
# Subtest: task home table uses catalog labels and keeps hue dots and mini-bars
ok 1279 - task home table uses catalog labels and keeps hue dots and mini-bars
  ---
  duration_ms: 5.37805
  ...
# Subtest: task flow stacks signed values, keeps missing constituents missing, and labels series
ok 1280 - task flow stacks signed values, keeps missing constituents missing, and labels series
  ---
  duration_ms: 6.562983
  ...
# Subtest: absent companions are named, custom filters are labeled overall, and net splits breakdowns
ok 1281 - absent companions are named, custom filters are labeled overall, and net splits breakdowns
  ---
  duration_ms: 5.648278
  ...
# Subtest: journal panels pair answers with review time and a gapped keep chart under 90%
ok 1282 - journal panels pair answers with review time and a gapped keep chart under 90%
  ---
  duration_ms: 5.645111
  ...
# Subtest: checklist calendar aligns Monday weeks with states, reasons, and provisional today
ok 1283 - checklist calendar aligns Monday weeks with states, reasons, and provisional today
  ---
  duration_ms: 4.895318
  ...
# Subtest: grouped calendars reuse daily points and old schemas fall back with a label
ok 1284 - grouped calendars reuse daily points and old schemas fall back with a label
  ---
  duration_ms: 2.750422
  ...
# Subtest: ISO year boundaries stay in one Monday week and chore dots expose text
ok 1285 - ISO year boundaries stay in one Monday week and chore dots expose text
  ---
  duration_ms: 6.861833
  ...
# Subtest: panel day selection pins the shared day and never fetches
ok 1286 - panel day selection pins the shared day and never fetches
  ---
  duration_ms: 8.372331
  ...
# Subtest: field and formula metrics keep only the focus chart and table
ok 1287 - field and formula metrics keep only the focus chart and table
  ---
  duration_ms: 2.341081
  ...
# Subtest: statsPanelDistinctHues gives every root its own colour
ok 1288 - statsPanelDistinctHues gives every root its own colour
  ---
  duration_ms: 0.223827
  ...
# Subtest: statsPanelDistinctHues does not depend on input order
ok 1289 - statsPanelDistinctHues does not depend on input order
  ---
  duration_ms: 0.186706
  ...
# Subtest: statsPanelDistinctHues keeps different area hues and greys buckets
ok 1290 - statsPanelDistinctHues keeps different area hues and greys buckets
  ---
  duration_ms: 0.167681
  ...
# Subtest: statsPanelDistinctHues never throws past eight coloured roots
ok 1291 - statsPanelDistinctHues never throws past eight coloured roots
  ---
  duration_ms: 0.31971
  ...
# Subtest: root bar gives same-area roots distinct hues and GTD review stays coloured
ok 1292 - root bar gives same-area roots distinct hues and GTD review stays coloured
  ---
  duration_ms: 3.144044
  ...
# Subtest: root rows and their sub-project leaves share the mapped hue
ok 1293 - root rows and their sub-project leaves share the mapped hue
  ---
  duration_ms: 4.229507
  ...
# Subtest: TT vectors verbatim: task-line gate plus boundary tokens
ok 1294 - TT vectors verbatim: task-line gate plus boundary tokens
  ---
  duration_ms: 4.944742
  ...
# Subtest: TT13-TT14 cursor reveal is inclusive
ok 1295 - TT13-TT14 cursor reveal is inclusive
  ---
  duration_ms: 1.6128
  ...
# Subtest: TT16 coexistence: task tag range is disjoint from priority and date marks
ok 1296 - TT16 coexistence: task tag range is disjoint from priority and date marks
  ---
  duration_ms: 1.564267
  ...
# Subtest: tooltip is exact and never contains a double colon
ok 1297 - tooltip is exact and never contains a double colon
  ---
  duration_ms: 0.257962
  ...
# Subtest: element structure: empty widget span with tooltip attributes
ok 1298 - element structure: empty widget span with tooltip attributes
  ---
  duration_ms: 0.75934
  ...
# Subtest: Live Preview decorations cover exactly the tag and respect reveal and code
ok 1299 - Live Preview decorations cover exactly the tag and respect reveal and code
  ---
  duration_ms: 0.977427
  ...
# Subtest: widget mousedown reveals the tag start
ok 1300 - widget mousedown reveals the tag start
  ---
  duration_ms: 0.474426
  ...
# Subtest: TR vectors verbatim: rendered views annotate eligible anchors in place
ok 1301 - TR vectors verbatim: rendered views annotate eligible anchors in place
  ---
  duration_ms: 1.980141
  ...
# Subtest: TR9 toggle strips document-wide and re-annotates on enable
ok 1302 - TR9 toggle strips document-wide and re-annotates on enable
  ---
  duration_ms: 1.423599
  ...
# Subtest: annotate and strip helpers are idempotent and defensive
ok 1303 - annotate and strip helpers are idempotent and defensive
  ---
  duration_ms: 0.618601
  ...
# Subtest: session toggle and onload wiring
ok 1304 - session toggle and onload wiring
  ---
  duration_ms: 7.28321
  ...
# Subtest: styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
ok 1305 - styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion
  ---
  duration_ms: 1.012454
  ...
# Subtest: TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
ok 1306 - TT20-TT28 verbatim: the \#task \#ref pair yields one ref range spanning both tokens
  ---
  duration_ms: 0.368314
  ...
# Subtest: Live Preview ref decorations replace the whole pair and reveal both tags at once
ok 1307 - Live Preview ref decorations replace the whole pair and reveal both tags at once
  ---
  duration_ms: 0.391618
  ...
# Subtest: ref element structure: book classes, reference label, and tooltip
ok 1308 - ref element structure: book classes, reference label, and tooltip
  ---
  duration_ms: 0.13096
  ...
# Subtest: TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
ok 1309 - TR10 verbatim: the \#task anchor becomes the book and the adjacent \#ref anchor hides
  ---
  duration_ms: 0.573576
  ...
# Subtest: TR11 verbatim: \#task \#references and reversed order keep the hash only
ok 1310 - TR11 verbatim: \#task \#references and reversed order keep the hash only
  ---
  duration_ms: 0.217345
  ...
# Subtest: TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
ok 1311 - TR12 verbatim: Tasks rows never annotate (the \#ref book is CSS-only)
  ---
  duration_ms: 0.191576
  ...
# Subtest: TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
ok 1312 - TR13 toggle covers the new classes: off strips the book and reveals \#ref, on restores both
  ---
  duration_ms: 0.605216
  ...
# Subtest: styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
ok 1313 - styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book
  ---
  duration_ms: 0.834333
  ...
# Subtest: CK vectors: canonical PRE/POST checklist runs share membership semantics
ok 1314 - CK vectors: canonical PRE/POST checklist runs share membership semantics
  ---
  duration_ms: 0.650261
  ...
# Subtest: CK live preview and widget vectors: one stable glyph replaces the full run
ok 1315 - CK live preview and widget vectors: one stable glyph replaces the full run
  ---
  duration_ms: 0.372892
  ...
# Subtest: CR vectors: rendered checklist anchors annotate in place, conflict stays native
ok 1316 - CR vectors: rendered checklist anchors annotate in place, conflict stays native
  ---
  duration_ms: 0.828893
  ...
# Subtest: CR3 toggle restores all checklist pills and re-annotates them
ok 1317 - CR3 toggle restores all checklist pills and re-annotates them
  ---
  duration_ms: 0.385646
  ...
# Subtest: CR4 Today reading-view anchor follows the second checklist tag
ok 1318 - CR4 Today reading-view anchor follows the second checklist tag
  ---
  duration_ms: 0.322727
  ...
# Subtest: checklist task mark CSS contract covers glyphs, conflict gates, Tasks rows, and resting
ok 1319 - checklist task mark CSS contract covers glyphs, conflict gates, Tasks rows, and resting
  ---
  duration_ms: 0.918965
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 1320 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 0.554389
  ...
# Subtest: section info null stays neutral (TM19)
ok 1321 - section info null stays neutral (TM19)
  ---
  duration_ms: 3.88448
  ...
# Subtest: data-line mapping stamps and marks an exact Today row
ok 1322 - data-line mapping stamps and marks an exact Today row
  ---
  duration_ms: 5.326341
  ...
# Subtest: data-line mapping rejects a status mismatch
ok 1323 - data-line mapping rejects a status mismatch
  ---
  duration_ms: 0.515484
  ...
# Subtest: row-index fallback maps when counts agree and refuses when they disagree
ok 1324 - row-index fallback maps when counts agree and refuses when they disagree
  ---
  duration_ms: 2.001973
  ...
# Subtest: Tasks result rows and code are skipped
ok 1325 - Tasks result rows and code are skipped
  ---
  duration_ms: 0.620204
  ...
# Subtest: a daily-note sourcePath is skipped
ok 1326 - a daily-note sourcePath is skipped
  ---
  duration_ms: 0.269615
  ...
# Subtest: duplicate ids stay neutral
ok 1327 - duplicate ids stay neutral
  ---
  duration_ms: 0.765111
  ...
# Subtest: insertion points: \#task anchor, \#ref pair, checkbox, whitespace split
ok 1328 - insertion points: \#task anchor, \#ref pair, checkbox, whitespace split
  ---
  duration_ms: 1.740133
  ...
# Subtest: identity-proven non-Today rows are stamped without a mark
ok 1329 - identity-proven non-Today rows are stamped without a mark
  ---
  duration_ms: 0.716829
  ...
# Subtest: sweep adds on link, removes on unlink or completion, updates tooltip, respects toggle, skips daily ancestors
ok 1330 - sweep adds on link, removes on unlink or completion, updates tooltip, respects toggle, skips daily ancestors
  ---
  duration_ms: 2.274924
  ...
# Subtest: daily-view class is set on open daily leaves and cleared on switch
ok 1331 - daily-view class is set on open daily leaves and cleared on switch
  ---
  duration_ms: 0.359146
  ...
# Subtest: delegated Mod+click jumps; plain click does not
ok 1332 - delegated Mod+click jumps; plain click does not
  ---
  duration_ms: 1.139215
  ...
# Subtest: setupTodayMarks registers the reading post-processor at order 60
ok 1333 - setupTodayMarks registers the reading post-processor at order 60
  ---
  duration_ms: 0.422556
  ...
# Subtest: styles.css daily-view suppression is present
ok 1334 - styles.css daily-view suppression is present
  ---
  duration_ms: 0.853641
  ...
# Subtest: Live Preview marks do not double-jump in Reading view
ok 1335 - Live Preview marks do not double-jump in Reading view
  ---
  duration_ms: 0.38246
  ...
# Subtest: mid-body \#task goes at the body start
ok 1336 - mid-body \#task goes at the body start
  ---
  duration_ms: 0.54949
  ...
# Subtest: \#task inside inline code stays neutral
ok 1337 - \#task inside inline code stays neutral
  ---
  duration_ms: 0.243836
  ...
# Subtest: re-render with a new path refreshes the mark key
ok 1338 - re-render with a new path refreshes the mark key
  ---
  duration_ms: 0.336663
  ...
# Subtest: one duplicate scan per render
ok 1339 - one duplicate scan per render
  ---
  duration_ms: 0.552866
  ...
# Subtest: row-index fallback uses every list item
ok 1340 - row-index fallback uses every list item
  ---
  duration_ms: 0.425943
  ...
# Subtest: open statuses are exactly space, star, slash, and question
ok 1341 - open statuses are exactly space, star, slash, and question
  ---
  duration_ms: 2.442664
  ...
# Subtest: trailing-id rules: leading space, trailing-only, valid charset
ok 1342 - trailing-id rules: leading space, trailing-only, valid charset
  ---
  duration_ms: 0.453245
  ...
# Subtest: candidate: TM9 closed stays null, TM10 open statuses pass
ok 1343 - candidate: TM9 closed stays null, TM10 open statuses pass
  ---
  duration_ms: 2.47136
  ...
# Subtest: candidate: TM11 needs an exact \#task tag and a trailing id
ok 1344 - candidate: TM11 needs an exact \#task tag and a trailing id
  ---
  duration_ms: 0.335341
  ...
# Subtest: candidate: TM21 code is left for the call-site code check
ok 1345 - candidate: TM21 code is left for the call-site code check
  ---
  duration_ms: 0.359326
  ...
# Subtest: insert offset: \#task first lands before the title
ok 1346 - insert offset: \#task first lands before the title
  ---
  duration_ms: 0.271929
  ...
# Subtest: insert offset: TM16 \#task \#ref spans the pair, \#prj sits between
ok 1347 - insert offset: TM16 \#task \#ref spans the pair, \#prj sits between
  ---
  duration_ms: 0.363444
  ...
# Subtest: insert offset: mid-body \#task falls back to the body start
ok 1348 - insert offset: mid-body \#task falls back to the body start
  ---
  duration_ms: 0.180034
  ...
# Subtest: insert offset: blockquote, spaces, numbered, empty title, emoji
ok 1349 - insert offset: blockquote, spaces, numbered, empty title, emoji
  ---
  duration_ms: 1.078971
  ...
# Subtest: duplicates: TM15 marks neither line
ok 1350 - duplicates: TM15 marks neither line
  ---
  duration_ms: 0.695819
  ...
# Subtest: session text: named, home label, range-only, unnamed
ok 1351 - session text: named, home label, range-only, unnamed
  ---
  duration_ms: 0.40864
  ...
# Subtest: tooltip: TM1 running, TM2 queued, and the platform variants
ok 1352 - tooltip: TM1 running, TM2 queued, and the platform variants
  ---
  duration_ms: 0.322997
  ...
# Subtest: tooltip: running wins as primary with a +N more suffix
ok 1353 - tooltip: running wins as primary with a +N more suffix
  ---
  duration_ms: 0.168693
  ...
# Subtest: tooltip: empty input yields Today and output never has ::
ok 1354 - tooltip: empty input yields Today and output never has ::
  ---
  duration_ms: 0.27221
  ...
# Subtest: entering window: 600 ms after join, never before or at load
ok 1355 - entering window: 600 ms after join, never before or at load
  ---
  duration_ms: 0.169012
  ...
# Subtest: modifier: primary button with meta on mac, ctrl elsewhere
ok 1356 - modifier: primary button with meta on mac, ctrl elsewhere
  ---
  duration_ms: 0.185574
  ...
# Subtest: element: empty span with tooltip attributes and no listeners
ok 1357 - element: empty span with tooltip attributes and no listeners
  ---
  duration_ms: 0.390346
  ...
# Subtest: widget: eq ignores entering and the callback
ok 1358 - widget: eq ignores entering and the callback
  ---
  duration_ms: 0.230591
  ...
# Subtest: widget: plain mousedown moves the cursor, Mod mousedown jumps
ok 1359 - widget: plain mousedown moves the cursor, Mod mousedown jumps
  ---
  duration_ms: 0.664149
  ...
# Subtest: refresh effect is lazy and stable
ok 1360 - refresh effect is lazy and stable
  ---
  duration_ms: 0.153133
  ...
# Subtest: styles.css implements the glyph anatomy contract
ok 1361 - styles.css implements the glyph anatomy contract
  ---
  duration_ms: 0.964242
  ...
# Subtest: Live Preview applies the TM1-TM22 line, cache, and refresh vectors
ok 1362 - Live Preview applies the TM1-TM22 line, cache, and refresh vectors
  ---
  duration_ms: 36.050215
  ...
# Subtest: Today mark lifecycle registers the toggle, keyboard command, and reading processor
ok 1363 - Today mark lifecycle registers the toggle, keyboard command, and reading processor
  ---
  duration_ms: 24.525967
  ...
# Subtest: keyboard jump uses the task under the cursor and reports non-membership
ok 1364 - keyboard jump uses the task under the cursor and reports non-membership
  ---
  duration_ms: 25.367475
  ...
# Subtest: Mod-click and keyboard jumps land on the current running Task Link
ok 1365 - Mod-click and keyboard jumps land on the current running Task Link
  ---
  duration_ms: 32.166086
  ...
# Subtest: reduced motion stops the entrance pop
ok 1366 - reduced motion stops the entrance pop
  ---
  duration_ms: 0.824474
  ...
# Subtest: tooltips never contain ::
ok 1367 - tooltips never contain ::
  ---
  duration_ms: 0.18863
  ...
# Subtest: todayMarkPosInInlineCode: single, double, unmatched, positions
ok 1368 - todayMarkPosInInlineCode: single, double, unmatched, positions
  ---
  duration_ms: 0.441513
  ...
# Subtest: builder gates on Today ids without touching doc lines
ok 1369 - builder gates on Today ids without touching doc lines
  ---
  duration_ms: 14.909711
  ...
# Subtest: two rebuilds on the same doc compute duplicates once
ok 1370 - two rebuilds on the same doc compute duplicates once
  ---
  duration_ms: 28.850676
  ...
# Subtest: todayMarksNow override drives readiness
ok 1371 - todayMarksNow override drives readiness
  ---
  duration_ms: 14.461519
  ...
# Subtest: refresh dispatches only to non-daily leaves and uses 16 ms
ok 1372 - refresh dispatches only to non-daily leaves and uses 16 ms
  ---
  duration_ms: 24.097479
  ...
# Subtest: keyboard command gates closed status and daily notes
ok 1373 - keyboard command gates closed status and daily notes
  ---
  duration_ms: 29.134297
  ...
# Subtest: TM14 rollover: day N+1 shows no decoration
ok 1374 - TM14 rollover: day N+1 shows no decoration
  ---
  duration_ms: 14.240083
  ...
# Subtest: TM17 widget sits at line.from + insertCh with side -1
ok 1375 - TM17 widget sits at line.from + insertCh with side -1
  ---
  duration_ms: 27.017736
  ...
# Subtest: TM18 entering: new key pops then settles
ok 1376 - TM18 entering: new key pops then settles
  ---
  duration_ms: 20.52118
  ...
# Subtest: TM20 toggle flips class, notice, and refreshes non-daily leaves
ok 1377 - TM20 toggle flips class, notice, and refreshes non-daily leaves
  ---
  duration_ms: 31.012885
  ...
# Subtest: rebuild triggers: doc, viewport, LP field, file switch rebuild; selection alone does not
ok 1378 - rebuild triggers: doc, viewport, LP field, file switch rebuild; selection alone does not
  ---
  duration_ms: 19.424295
  ...
# Subtest: jump guards in-flight, prefers cached ledgerLine over later match
ok 1379 - jump guards in-flight, prefers cached ledgerLine over later match
  ---
  duration_ms: 21.583566
  ...
# Subtest: jump with no open daily leaf attempts the daily open
ok 1380 - jump with no open daily leaf attempts the daily open
  ---
  duration_ms: 21.073975
  ...
# Subtest: home labels: unnamed timed entry uses derived label and 1-based entryLine
ok 1381 - home labels: unnamed timed entry uses derived label and 1-based entryLine
  ---
  duration_ms: 20.654224
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 1382 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 21.432759
  ...
# Subtest: T1 GTD: empty target resolves to the daily note
ok 1383 - T1 GTD: empty target resolves to the daily note
  ---
  duration_ms: 2.831978
  ...
# Subtest: T2 markers: pomodoro mark counts, struck drops, embed counts
ok 1384 - T2 markers: pomodoro mark counts, struck drops, embed counts
  ---
  duration_ms: 0.709515
  ...
# Subtest: T3 closed entries: links under completed/cancelled entries drop
ok 1385 - T3 closed entries: links under completed/cancelled entries drop
  ---
  duration_ms: 0.194511
  ...
# Subtest: T4 shapes: mixed text and deeper descendants drop
ok 1386 - T4 shapes: mixed text and deeper descendants drop
  ---
  duration_ms: 0.287188
  ...
# Subtest: T5 dedupe: same task twice keeps the first position
ok 1387 - T5 dedupe: same task twice keeps the first position
  ---
  duration_ms: 0.325281
  ...
# Subtest: T6 fenced: links inside fenced blocks drop
ok 1388 - T6 fenced: links inside fenced blocks drop
  ---
  duration_ms: 0.271869
  ...
# Subtest: T7 status: the link layer lists every dedicated link
ok 1389 - T7 status: the link layer lists every dedicated link
  ---
  duration_ms: 0.293921
  ...
# Subtest: T8 unresolved: missing notes give no key
ok 1390 - T8 unresolved: missing notes give no key
  ---
  duration_ms: 0.168522
  ...
# Subtest: T9 alias: aliased links count under their target
ok 1391 - T9 alias: aliased links count under their target
  ---
  duration_ms: 0.381488
  ...
# Subtest: laneBudgetFromTasks counts the whole Next lane, Today included
ok 1392 - laneBudgetFromTasks counts the whole Next lane, Today included
  ---
  duration_ms: 1.458936
  ...
# Subtest: laneBudgetFromTasks counts Pending by type and flags over-cap
ok 1393 - laneBudgetFromTasks counts Pending by type and flags over-cap
  ---
  duration_ms: 0.484706
  ...
# Subtest: lane caps come from max_next/max_pending; legacy max_now is ignored
ok 1394 - lane caps come from max_next/max_pending; legacy max_now is ignored
  ---
  duration_ms: 0.239587
  ...
# Subtest: reload event name matches the Tasks bundle subscription
ok 1395 - reload event name matches the Tasks bundle subscription
  ---
  duration_ms: 0.119538
  ...
# Subtest: api v2 shape: Today and lane budgets, no nowBudget
ok 1396 - api v2 shape: Today and lane budgets, no nowBudget
  ---
  duration_ms: 6.87572
  ...
# Subtest: cache rebuild answers isToday/todayRank in ledger order
ok 1397 - cache rebuild answers isToday/todayRank in ledger order
  ---
  duration_ms: 2.771001
  ...
# Subtest: refresh fires only when the key set changes
ok 1398 - refresh fires only when the key set changes
  ---
  duration_ms: 1.843019
  ...
# Subtest: unready to ready with empty TODAY still refreshes open badges
ok 1399 - unready to ready with empty TODAY still refreshes open badges
  ---
  duration_ms: 1.207486
  ...
# Subtest: cache rebuilds on the daily changed event with the event content
ok 1400 - cache rebuilds on the daily changed event with the event content
  ---
  duration_ms: 1.039224
  ...
# Subtest: cache rebuilds once on resolved and at midnight rollover
ok 1401 - cache rebuilds once on resolved and at midnight rollover
  ---
  duration_ms: 1.453576
  ...
# Subtest: computeTodayLinks records entry range and placeholder
ok 1402 - computeTodayLinks records entry range and placeholder
  ---
  duration_ms: 0.380827
  ...
# Subtest: todayOpenEntries and todayRunningEntryLine follow the unique timed rule
ok 1403 - todayOpenEntries and todayRunningEntryLine follow the unique timed rule
  ---
  duration_ms: 0.401587
  ...
# Subtest: resolveTodayLinkKeys keeps duplicates; resolveTodayKeys is first-occurrence
ok 1404 - resolveTodayLinkKeys keeps duplicates; resolveTodayKeys is first-occurrence
  ---
  duration_ms: 0.216714
  ...
# Subtest: todayLinkDetails: named running, placeholder, unnamed home, unnamed none
ok 1405 - todayLinkDetails: named running, placeholder, unnamed home, unnamed none
  ---
  duration_ms: 0.254776
  ...
# Subtest: todayLinkDetails orders running first and keeps one detail per key+entry
ok 1406 - todayLinkDetails orders running first and keeps one detail per key+entry
  ---
  duration_ms: 0.188661
  ...
# Subtest: todayKeyParts splits at the last hash; idsByPath groups block ids
ok 1407 - todayKeyParts splits at the last hash; idsByPath groups block ids
  ---
  duration_ms: 0.156379
  ...
# Subtest: todayDetailsSignature changes only when details change
ok 1408 - todayDetailsSignature changes only when details change
  ---
  duration_ms: 0.227425
  ...
# Subtest: idsByPath and details accessors follow the rebuilt cache
ok 1409 - idsByPath and details accessors follow the rebuilt cache
  ---
  duration_ms: 1.435853
  ...
# Subtest: details-only change refreshes marks without a Tasks reload
ok 1410 - details-only change refreshes marks without a Tasks reload
  ---
  duration_ms: 1.127554
  ...
# Subtest: entered stamps only when the cache was already ready, then prune
ok 1411 - entered stamps only when the cache was already ready, then prune
  ---
  duration_ms: 1.424451
  ...
# Subtest: generation guard: reverse-order async reads keep the newer
ok 1412 - generation guard: reverse-order async reads keep the newer
  ---
  duration_ms: 1.039135
  ...
# Subtest: generation guard: a sync rebuild wins over an in-flight async read
ok 1413 - generation guard: a sync rebuild wins over an in-flight async read
  ---
  duration_ms: 0.715486
  ...
# Subtest: revalidateTodayCache is throttled and refreshes when not ready
ok 1414 - revalidateTodayCache is throttled and refreshes when not ready
  ---
  duration_ms: 0.676562
  ...
# Subtest: revalidateTodayCache respects layoutReady and backwards clock steps
ok 1415 - revalidateTodayCache respects layoutReady and backwards clock steps
  ---
  duration_ms: 0.592612
  ...
# Subtest: a done-today prerequisite shows the glyph
ok 1416 - a done-today prerequisite shows the glyph
  ---
  duration_ms: 3.566712
  ...
# Subtest: done yesterday does not show the glyph
ok 1417 - done yesterday does not show the glyph
  ---
  duration_ms: 0.415764
  ...
# Subtest: a struck link does not show the glyph
ok 1418 - a struck link does not show the glyph
  ---
  duration_ms: 0.259776
  ...
# Subtest: a closed entry does not show the glyph
ok 1419 - a closed entry does not show the glyph
  ---
  duration_ms: 0.223497
  ...
# Subtest: several prerequisites give +N
ok 1420 - several prerequisites give +N
  ---
  duration_ms: 0.4868
  ...
# Subtest: the model refuses every non-glyph shape
ok 1421 - the model refuses every non-glyph shape
  ---
  duration_ms: 0.788125
  ...
# Subtest: unblockedGlyphDoneToday needs DONE plus a today done date
ok 1422 - unblockedGlyphDoneToday needs DONE plus a today done date
  ---
  duration_ms: 0.254275
  ...
# Subtest: tooltip names one prerequisite and counts several
ok 1423 - tooltip names one prerequisite and counts several
  ---
  duration_ms: 0.256009
  ...
# Subtest: Live Preview places one glyph after each unblocked link
ok 1424 - Live Preview places one glyph after each unblocked link
  ---
  duration_ms: 1.791311
  ...
# Subtest: Live Preview draws nothing without a warm cache or a live link
ok 1425 - Live Preview draws nothing without a warm cache or a live link
  ---
  duration_ms: 0.788716
  ...
# Subtest: widget mousedown places the cursor past the link
ok 1426 - widget mousedown places the cursor past the link
  ---
  duration_ms: 0.489585
  ...
# Subtest: rebuild triggers skip the cursor but take doc, viewport, and refresh
ok 1427 - rebuild triggers skip the cursor but take doc, viewport, and refresh
  ---
  duration_ms: 0.690739
  ...
# Subtest: Reading view glyphs unblocked rows and dedupes
ok 1428 - Reading view glyphs unblocked rows and dedupes
  ---
  duration_ms: 1.793475
  ...
# Subtest: Reading view refuses every non-glyph row
ok 1429 - Reading view refuses every non-glyph row
  ---
  duration_ms: 1.65454
  ...
# Subtest: api.unblockedGlyph v1 is additive, sync, and never throwing
ok 1430 - api.unblockedGlyph v1 is additive, sync, and never throwing
  ---
  duration_ms: 0.534781
  ...
# Subtest: session toggle, onload wiring, and refresh fan-out
ok 1431 - session toggle, onload wiring, and refresh fan-out
  ---
  duration_ms: 0.960103
  ...
# Subtest: mark gate holds in popout windows for both toggle states
ok 1432 - mark gate holds in popout windows for both toggle states
  ---
  duration_ms: 0.480979
  ...
# Subtest: changed-file and rollover refreshes
ok 1433 - changed-file and rollover refreshes
  ---
  duration_ms: 0.29347
  ...
# Subtest: the refresh effect stays lazy: one eager define
ok 1434 - the refresh effect stays lazy: one eager define
  ---
  duration_ms: 0.101213
  ...
# Subtest: styles.css contract: faint glyph, Done token, toggle
ok 1435 - styles.css contract: faint glyph, Done token, toggle
  ---
  duration_ms: 0.784588
  ...
# Subtest: Ledger Vim mappings restore \\p and retain the other normal-mode actions
ok 1436 - Ledger Vim mappings restore \\p and retain the other normal-mode actions
  ---
  duration_ms: 5.947728
  ...
# Subtest: workBadgeTone boundary vectors at cap 100 use exact comparisons
ok 1437 - workBadgeTone boundary vectors at cap 100 use exact comparisons
  ---
  duration_ms: 1.01076
  ...
# Subtest: workBadgeTone at cap 15 has no percentage rounding
ok 1438 - workBadgeTone at cap 15 has no percentage rounding
  ---
  duration_ms: 0.254697
  ...
# Subtest: workBadgeTone default caps, small caps, and cap changes
ok 1439 - workBadgeTone default caps, small caps, and cap changes
  ---
  duration_ms: 0.148543
  ...
# Subtest: workBadgeTone never coerces invalid input to zero
ok 1440 - workBadgeTone never coerces invalid input to zero
  ---
  duration_ms: 0.875502
  ...
# Subtest: TODAY links bands with themes at cap 3
ok 1441 - TODAY links bands with themes at cap 3
  ---
  duration_ms: 0.3087
  ...
# Subtest: TODAY theme overflow forces red, exact cap does not
ok 1442 - TODAY theme overflow forces red, exact cap does not
  ---
  duration_ms: 0.197878
  ...
# Subtest: TODAY unavailable stays neutral, empty section is grey
ok 1443 - TODAY unavailable stays neutral, empty section is grey
  ---
  duration_ms: 1.135508
  ...
# Subtest: PENDING/NEXT models color the section, READY its gated count
ok 1444 - PENDING/NEXT models color the section, READY its gated count
  ---
  duration_ms: 0.443817
  ...
# Subtest: READY uses its gated count even when the total lane is larger
ok 1445 - READY uses its gated count even when the total lane is larger
  ---
  duration_ms: 0.333517
  ...
# Subtest: cap equality still emits no cap lint
ok 1446 - cap equality still emits no cap lint
  ---
  duration_ms: 2.349757
  ...
# Subtest: lane DOM keeps exactly one tone through transitions and unavailability
ok 1447 - lane DOM keeps exactly one tone through transitions and unavailability
  ---
  duration_ms: 6.96373
  ...
# Subtest: READY DOM keeps exactly one tone and daily/dashboard models agree
ok 1448 - READY DOM keeps exactly one tone and daily/dashboard models agree
  ---
  duration_ms: 1.232685
  ...
# SKIP dashboard integration: BOB_DASHBOARD_FILE is not set
# SKIP dashboard fallback integration: BOB_DASHBOARD_FILE is not set
# SKIP dash CSS contract: BOB_DASHBOARD_FILE is not set
# Subtest: daily TODAY chip uses the theme-overflow tone
ok 1449 - daily TODAY chip uses the theme-overflow tone
  ---
  duration_ms: 18.84695
  ...
# Subtest: dashboard integration uses Work tones, TODAY override, and keeps Work order
ok 1450 - dashboard integration uses Work tones, TODAY override, and keeps Work order
  ---
  duration_ms: 0.556183
  ...
# Subtest: dashboard fallbacks keep Work tones without plugin renderers or colors
ok 1451 - dashboard fallbacks keep Work tones without plugin renderers or colors
  ---
  duration_ms: 0.316254
  ...
# Subtest: Work tone CSS covers each tone and uses the shared magenta value
ok 1452 - Work tone CSS covers each tone and uses the shared magenta value
  ---
  duration_ms: 0.954913
  ...
# Subtest: RBW6 mergeTargetPreparations keeps one write at the strongest lane
ok 1453 - RBW6 mergeTargetPreparations keeps one write at the strongest lane
  ---
  duration_ms: 1.774458
  ...
# Subtest: §15.7 notices use curly quotes and the Ready → Blocked copy
ok 1454 - §15.7 notices use curly quotes and the Ready → Blocked copy
  ---
  duration_ms: 0.395536
  ...
# Subtest: RBP1 same-note add is one transaction and matches forward bytes
ok 1455 - RBP1 same-note add is one transaction and matches forward bytes
  ---
  duration_ms: 17.640609
  ...
# Subtest: RBP2 background-leaf T matches forward bytes
ok 1456 - RBP2 background-leaf T matches forward bytes
  ---
  duration_ms: 4.701708
  ...
# Subtest: RBP3 closed T is written through vault.process and matches forward bytes
ok 1457 - RBP3 closed T is written through vault.process and matches forward bytes
  ---
  duration_ms: 3.068309
  ...
# Subtest: RBP4 ordinary transfer; a ^prj N is never raised
ok 1458 - RBP4 ordinary transfer; a ^prj N is never raised
  ---
  duration_ms: 11.640983
  ...
# Subtest: RBP5 consumed Pomodoro link matches forward bytes
ok 1459 - RBP5 consumed Pomodoro link matches forward bytes
  ---
  duration_ms: 4.630212
  ...
# Subtest: RBP6 project T with residents and a sub-project matches forward bytes
ok 1460 - RBP6 project T with residents and a sub-project matches forward bytes
  ---
  duration_ms: 18.441197
  ...
# Subtest: RBP7 two dependents in different lanes prepare N once at [/]
ok 1461 - RBP7 two dependents in different lanes prepare N once at [/]
  ---
  duration_ms: 4.993406
  ...
# Subtest: RBP8 counted sources N1 and N2 match forward(T + N1, N2)
ok 1462 - RBP8 counted sources N1 and N2 match forward(T + N1, N2)
  ---
  duration_ms: 3.146058
  ...
# Subtest: RBP9 blocks_lines false writes no BLOCKS and still ids N
ok 1463 - RBP9 blocks_lines false writes no BLOCKS and still ids N
  ---
  duration_ms: 1.47669
  ...
# Subtest: RBP10 removing the last reason matches forward removal
ok 1464 - RBP10 removing the last reason matches forward removal
  ---
  duration_ms: 3.023373
  ...
# Subtest: RBW1 a changed source note writes nothing
ok 1465 - RBW1 a changed source note writes nothing
  ---
  duration_ms: 1.271458
  ...
# Subtest: RBW2 one changed T note still lands the others and omits it from BLOCKS
ok 1466 - RBW2 one changed T note still lands the others and omits it from BLOCKS
  ---
  duration_ms: 1.433808
  ...
# Subtest: RBW3 already-present picks write nothing
ok 1467 - RBW3 already-present picks write nothing
  ---
  duration_ms: 1.082377
  ...
# Subtest: RBW4 cleanup runs for T's that committed when N lives in today's daily note
ok 1468 - RBW4 cleanup runs for T's that committed when N lives in today's daily note
  ---
  duration_ms: 2.306103
  ...
# Subtest: RBW6 counted forward two-lane dependents prepare N once
ok 1469 - RBW6 counted forward two-lane dependents prepare N once
  ---
  duration_ms: 8.427306
  ...
# Subtest: A1 N above two T's in one note matches forward (open and closed note)
ok 1470 - A1 N above two T's in one note matches forward (open and closed note)
  ---
  duration_ms: 14.762591
  ...
# Subtest: A1 N below two T's matches forward bytes
ok 1471 - A1 N below two T's matches forward bytes
  ---
  duration_ms: 3.678243
  ...
# Subtest: A2 forward stamps the dependent when a prerequisite above gains BLOCKS
ok 1472 - A2 forward stamps the dependent when a prerequisite above gains BLOCKS
  ---
  duration_ms: 1.059493
  ...
# Subtest: A1 mixed same-note and cross-note picks keep N's lane rise (RBP7 variant)
ok 1473 - A1 mixed same-note and cross-note picks keep N's lane rise (RBP7 variant)
  ---
  duration_ms: 2.594634
  ...
# Subtest: A1 RBP1 with N truly lacking ^id is prompted an id and matches forward
ok 1474 - A1 RBP1 with N truly lacking ^id is prompted an id and matches forward
  ---
  duration_ms: 1.401246
  ...
# Subtest: A1 N lacking ^id in a closed note above T keeps its BLOCKS line under N
ok 1475 - A1 N lacking ^id in a closed note above T keeps its BLOCKS line under N
  ---
  duration_ms: 0.875071
  ...
# Subtest: A3 mirror lists the committed T's by identity (N above T1, X, T2)
ok 1476 - A3 mirror lists the committed T's by identity (N above T1, X, T2)
  ---
  duration_ms: 1.532476
  ...
# Subtest: A4 notices name T, not N (add, remove, project, counted)
ok 1477 - A4 notices name T, not N (add, remove, project, counted)
  ---
  duration_ms: 7.887545
  ...
# Subtest: A5 the writer's stale notice is returned once and never shown by the writer
ok 1478 - A5 the writer's stale notice is returned once and never shown by the writer
  ---
  duration_ms: 0.388472
  ...
# Subtest: A6 a changed T row (rawLine) is refused before any write
ok 1479 - A6 a changed T row (rawLine) is refused before any write
  ---
  duration_ms: 0.264295
  ...
# Subtest: A7 RBW2 keeps the failed T's Pomodoro link and consumes the committed one
ok 1480 - A7 RBW2 keeps the failed T's Pomodoro link and consumes the committed one
  ---
  duration_ms: 2.453685
  ...
# Subtest: A8 closed-note T guards run when the gesture is applied
ok 1481 - A8 closed-note T guards run when the gesture is applied
  ---
  duration_ms: 3.648617
  ...
# Subtest: A9 a ^prj T's residents recover with [unblocked::] when N lives in a daily note
ok 1482 - A9 a ^prj T's residents recover with [unblocked::] when N lives in a daily note
  ---
  duration_ms: 18.420517
  ...
# Subtest: A5 a preparation no write can carry fails the plan instead of being dropped
ok 1483 - A5 a preparation no write can carry fails the plan instead of being dropped
  ---
  duration_ms: 0.873528
  ...
# Subtest: applyDependencyEdit adding a first cross-note prerequisite keeps the dependent's cursor
ok 1484 - applyDependencyEdit adding a first cross-note prerequisite keeps the dependent's cursor
  ---
  duration_ms: 1.836628
  ...
# Subtest: applyBlocksEdit giving a source its first BLOCKS line keeps the source's cursor
ok 1485 - applyBlocksEdit giving a source its first BLOCKS line keeps the source's cursor
  ---
  duration_ms: 6.043741
  ...
# Subtest: nav BK1–BK2 accept canonical BLOCKS lines
ok 1486 - nav BK1–BK2 accept canonical BLOCKS lines
  ---
  duration_ms: 3.159874
  ...
# Subtest: nav BK3–BK11 canonicalise
ok 1487 - nav BK3–BK11 canonicalise
  ---
  duration_ms: 0.762586
  ...
# Subtest: nav BK12 empty, BK13–BK15 malformed
ok 1488 - nav BK12 empty, BK13–BK15 malformed
  ---
  duration_ms: 0.264415
  ...
# Subtest: nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse
ok 1489 - nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse
  ---
  duration_ms: 0.467382
  ...
# Subtest: nav BK21 code-point sort and writer format
ok 1490 - nav BK21 code-point sort and writer format
  ---
  duration_ms: 0.369456
  ...
# Subtest: nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS
ok 1491 - nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS
  ---
  duration_ms: 0.795549
  ...
# Subtest: nav BW18 conversion drops BLOCKS like Sub-projects
ok 1492 - nav BW18 conversion drops BLOCKS like Sub-projects
  ---
  duration_ms: 1.300684
  ...
# Subtest: nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner
ok 1493 - nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner
  ---
  duration_ms: 0.992375
  ...
# Subtest: nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists
ok 1494 - nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists
  ---
  duration_ms: 2.104871
  ...
# Subtest: nav MC1/MC2 deferred Pomodoro cleanup skips managed lines
ok 1495 - nav MC1/MC2 deferred Pomodoro cleanup skips managed lines
  ---
  duration_ms: 0.510074
  ...
# Subtest: showBlocksStage opens from a task with reverse CURRENT and RESULTS
ok 1496 - showBlocksStage opens from a task with reverse CURRENT and RESULTS
  ---
  duration_ms: 14.829391
  ...
# Subtest: showBlocksStage opens from a counted session
ok 1497 - showBlocksStage opens from a counted session
  ---
  duration_ms: 1.535452
  ...
# Subtest: showBlocksStage opens on a Task Link target note
ok 1498 - showBlocksStage opens on a Task Link target note
  ---
  duration_ms: 1.236331
  ...
# Subtest: RBU1 empty query uses today-first then In Progress, Next, same-note, rest
ok 1499 - RBU1 empty query uses today-first then In Progress, Next, same-note, rest
  ---
  duration_ms: 1.598823
  ...
# Subtest: RBU2 today-linked rows carry 🍅 running and strip names the entry
ok 1500 - RBU2 today-linked rows carry 🍅 running and strip names the entry
  ---
  duration_ms: 0.885822
  ...
# Subtest: RBU3 CURRENT 🔑 only when N is the last reason
ok 1501 - RBU3 CURRENT 🔑 only when N is the last reason
  ---
  duration_ms: 1.398791
  ...
# Subtest: RBU4 footer verbs are block, remove, and apply N
ok 1502 - RBU4 footer verbs are block, remove, and apply N
  ---
  duration_ms: 1.310152
  ...
# Subtest: RBU5 subtitle at rest, with marks, and names this task first
ok 1503 - RBU5 subtitle at rest, with marks, and names this task first
  ---
  duration_ms: 1.41392
  ...
# Subtest: RBG1 N itself is excluded from RESULTS
ok 1504 - RBG1 N itself is excluded from RESULTS
  ---
  duration_ms: 1.04743
  ...
# Subtest: RBG2 a cycle disables the row with path tooltip copy
ok 1505 - RBG2 a cycle disables the row with path tooltip copy
  ---
  duration_ms: 0.944123
  ...
# Subtest: RBG3 ^prj T with N inside the project is inside this project
ok 1506 - RBG3 ^prj T with N inside the project is inside this project
  ---
  duration_ms: 1.87982
  ...
# Subtest: RBG3 descendant N disables the parent project as a sub-project
ok 1507 - RBG3 descendant N disables the parent project as a sub-project
  ---
  duration_ms: 1.269645
  ...
# Subtest: RBG4 a malformed or second Depends-On line is guarded
ok 1508 - RBG4 a malformed or second Depends-On line is guarded
  ---
  duration_ms: 2.267691
  ...
# Subtest: RBG5 stale refuse reopens in the Blocks direction
ok 1509 - RBG5 stale refuse reopens in the Blocks direction
  ---
  duration_ms: 2.322866
  ...
# Subtest: RBG5 for T: a T changed after stage open refuses once and writes nothing
ok 1510 - RBG5 for T: a T changed after stage open refuses once and writes nothing
  ---
  duration_ms: 2.830746
  ...
# Subtest: today's links survive a pool refresh that lands while the daily note loads
ok 1511 - today's links survive a pool refresh that lands while the daily note loads
  ---
  duration_ms: 32.399764
  ...
# Subtest: RBG8 Esc from the stage or the block-ID prompt writes nothing
ok 1512 - RBG8 Esc from the stage or the block-ID prompt writes nothing
  ---
  duration_ms: 2.144646
  ...
# Subtest: missing source ^id opens the block-ID prompt and Esc allocates none
ok 1513 - missing source ^id opens the block-ID prompt and Esc allocates none
  ---
  duration_ms: 1.074141
  ...
# Subtest: RBP11 inbox route runs first then the Blocks write
ok 1514 - RBP11 inbox route runs first then the Blocks write
  ---
  duration_ms: 0.875051
  ...
# Subtest: RBW5 review walk stays unless the commit takes N out of today's walk
ok 1515 - RBW5 review walk stays unless the commit takes N out of today's walk
  ---
  duration_ms: 5.789395
  ...
# Subtest: marks commit add and remove together; counted uses k/n block
ok 1516 - marks commit add and remove together; counted uses k/n block
  ---
  duration_ms: 3.052379
  ...
# Subtest: strip text covers RESULTS, BLOCKED, CURRENT, disabled, marks, and ^prj
ok 1517 - strip text covers RESULTS, BLOCKED, CURRENT, disabled, marks, and ^prj
  ---
  duration_ms: 0.371379
  ...
# Subtest: counted subtitle drops the ⇥ hint because marks are off in counted sessions
ok 1518 - counted subtitle drops the ⇥ hint because marks are off in counted sessions
  ---
  duration_ms: 0.810929
  ...
# Subtest: 🔑 tooltip and 🍅 tooltip render on badges
ok 1519 - 🔑 tooltip and 🍅 tooltip render on badges
  ---
  duration_ms: 0.97893
  ...
# Subtest: Tab marks Blocks CURRENT rows and Enter removes both dependents
ok 1520 - Tab marks Blocks CURRENT rows and Enter removes both dependents
  ---
  duration_ms: 12.342181
  ...
# Subtest: SB1-SB9 dependent IDs match the successor mint vectors
ok 1521 - SB1-SB9 dependent IDs match the successor mint vectors
  ---
  duration_ms: 2.029957
  ...
# Subtest: BW1 same-note add mints and writes BLOCKS in the dependent's single transaction
ok 1522 - BW1 same-note add mints and writes BLOCKS in the dependent's single transaction
  ---
  duration_ms: 10.108793
  ...
# Subtest: BW2 cross-note add follows the dependent commit and writes the target note
ok 1523 - BW2 cross-note add follows the dependent commit and writes the target note
  ---
  duration_ms: 2.286285
  ...
# Subtest: BW4 cross-note target preparation precedes the reverse-line preimage
ok 1524 - BW4 cross-note target preparation precedes the reverse-line preimage
  ---
  duration_ms: 1.555841
  ...
# Subtest: BW3 stale cross-note preimage leaves the forward write standing and shows the suffix
ok 1525 - BW3 stale cross-note preimage leaves the forward write standing and shows the suffix
  ---
  duration_ms: 1.245197
  ...
# Subtest: BW5 removal deletes the reverse line when its last dependent leaves
ok 1526 - BW5 removal deletes the reverse line when its last dependent leaves
  ---
  duration_ms: 2.906811
  ...
# Subtest: BW6 an already mirrored edge is a byte-identical no-op
ok 1527 - BW6 an already mirrored edge is a byte-identical no-op
  ---
  duration_ms: 0.653407
  ...
# Subtest: BW7 closed owners stay frozen
ok 1528 - BW7 closed owners stay frozen
  ---
  duration_ms: 1.326443
  ...
# Subtest: BW8 malformed reverse lines stay untouched and report the failed mirror
ok 1529 - BW8 malformed reverse lines stay untouched and report the failed mirror
  ---
  duration_ms: 1.535633
  ...
# Subtest: BW15 config defaults on, honors false, and invalid values fall back on
ok 1530 - BW15 config defaults on, honors false, and invalid values fall back on
  ---
  duration_ms: 0.611057
  ...
# Subtest: BW17 planner output follows BK21 Unicode code-point ordering
ok 1531 - BW17 planner output follows BK21 Unicode code-point ordering
  ---
  duration_ms: 0.52889
  ...
# Subtest: duplicate BLOCKS children merge their known dependents and preserve CRLF
ok 1532 - duplicate BLOCKS children merge their known dependents and preserve CRLF
  ---
  duration_ms: 0.431535
  ...
# Subtest: BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270)
ok 1533 - BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270)
  ---
  duration_ms: 3.480427
  ...
# Subtest: counted remove-from-all drops every dependent from the same-note BLOCKS line (420)
ok 1534 - counted remove-from-all drops every dependent from the same-note BLOCKS line (420)
  ---
  duration_ms: 2.349918
  ...
# Subtest: vault counted add composes cross-note follow-ups for every source (420)
ok 1535 - vault counted add composes cross-note follow-ups for every source (420)
  ---
  duration_ms: 0.878057
  ...
# Subtest: marked batch add writes every same-note target onto BLOCKS in one plan (430)
ok 1536 - marked batch add writes every same-note target onto BLOCKS in one plan (430)
  ---
  duration_ms: 0.557564
  ...
# Subtest: counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600)
ok 1537 - counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600)
  ---
  duration_ms: 4.271537
  ...
# Subtest: BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves
ok 1538 - BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves
  ---
  duration_ms: 2.065905
  ...
# Subtest: BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS
ok 1539 - BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS
  ---
  duration_ms: 2.124216
  ...
# Subtest: hand-edit clear path routes through the BLOCKS seam (600)
ok 1540 - hand-edit clear path routes through the BLOCKS seam (600)
  ---
  duration_ms: 0.525484
  ...
# Subtest: BW18 conversion never copies a BLOCKS line as a user child
ok 1541 - BW18 conversion never copies a BLOCKS line as a user child
  ---
  duration_ms: 0.546293
  ...
# Subtest: BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it
ok 1542 - BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it
  ---
  duration_ms: 3.38826
  ...
# Subtest: review checklist group helpers format exact completion and close notices
ok 1543 - review checklist group helpers format exact completion and close notices
  ---
  duration_ms: 2.472301
  ...
# Subtest: claim declines without a current exact PRE/POST walk landing
ok 1544 - claim declines without a current exact PRE/POST walk landing
  ---
  duration_ms: 10.45784
  ...
# Subtest: a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
ok 1545 - a real [S landing lets Ctrl+Enter complete and land on the next live PRE row
  ---
  duration_ms: 3.55069
  ...
# Subtest: checklist Ctrl+Enter holds its landing through the actual successor picker
ok 1546 - checklist Ctrl+Enter holds its landing through the actual successor picker
  ---
  duration_ms: 11.619141
  ...
# Subtest: seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
ok 1547 - seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode
  ---
  duration_ms: 19.094975
  ...
# Subtest: a landed [?] checklist chore is claimed and completed
ok 1548 - a landed [?] checklist chore is claimed and completed
  ---
  duration_ms: 3.321815
  ...
# Subtest: ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
ok 1549 - ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count
  ---
  duration_ms: 2.649711
  ...
# Subtest: live successor filtering skips a stale completed row
ok 1550 - live successor filtering skips a stale completed row
  ---
  duration_ms: 0.842799
  ...
# Subtest: live group filtering reads each cross-note path once
ok 1551 - live group filtering reads each cross-note path once
  ---
  duration_ms: 0.606288
  ...
# Subtest: Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
ok 1552 - Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW
  ---
  duration_ms: 3.490285
  ...
# Subtest: POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
ok 1553 - POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays
  ---
  duration_ms: 1.668506
  ...
# Subtest: ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
ok 1554 - ]S and Ctrl+Enter close the final Morning review; earlier POST rows stay counted
  ---
  duration_ms: 0.67016
  ...
# Subtest: completion failure preserves cursor and landing and reports the Tasks failure
ok 1555 - completion failure preserves cursor and landing and reports the Tasks failure
  ---
  duration_ms: 0.32458
  ...
# Subtest: reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
ok 1556 - reviewLineChecklistKind matches exact \#gtd \#pre/\#post tokens
  ---
  duration_ms: 1.238686
  ...
# Subtest: Alt+F on PRE stays with remaining PRE count and never stamps
ok 1557 - Alt+F on PRE stays with remaining PRE count and never stamps
  ---
  duration_ms: 5.553867
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a stale cache
ok 1558 - Ctrl+Alt+F completes seven PRE rows from a stale cache
  ---
  duration_ms: 10.491444
  ...
# Subtest: Ctrl+Alt+F completes seven PRE rows from a refreshed cache
ok 1559 - Ctrl+Alt+F completes seven PRE rows from a refreshed cache
  ---
  duration_ms: 11.819864
  ...
# Subtest: POST stays put with the closing notice
ok 1560 - POST stays put with the closing notice
  ---
  duration_ms: 1.006442
  ...
# Subtest: manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
ok 1561 - manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE
  ---
  duration_ms: 1.341422
  ...
# Subtest: manual Ctrl+Enter then ]s from a stale cache uses text-first identity
ok 1562 - manual Ctrl+Enter then ]s from a stale cache uses text-first identity
  ---
  duration_ms: 0.828613
  ...
# Subtest: counted Alt+F skips checklist rows with the skip tail
ok 1563 - counted Alt+F skips checklist rows with the skip tail
  ---
  duration_ms: 3.303619
  ...
# Subtest: missing cycler gate on a PRE row writes nothing
ok 1564 - missing cycler gate on a PRE row writes nothing
  ---
  duration_ms: 0.669709
  ...
# Subtest: missing ledger checklist gate on a tagged line writes nothing
ok 1565 - missing ledger checklist gate on a tagged line writes nothing
  ---
  duration_ms: 0.647696
  ...
# Subtest: a tagged line that is not a queue match falls through to recurring refusal
ok 1566 - a tagged line that is not a queue match falls through to recurring refusal
  ---
  duration_ms: 0.368023
  ...
# Subtest: formatFreshStampChecklistSkipTail names the skipped count
ok 1567 - formatFreshStampChecklistSkipTail names the skipped count
  ---
  duration_ms: 0.113467
  ...
# Subtest: partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
ok 1568 - partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch
  ---
  duration_ms: 0.171186
  ...
# Subtest: Task Link Alt+F skips a PRE target with the skip notice
ok 1569 - Task Link Alt+F skips a PRE target with the skip notice
  ---
  duration_ms: 2.140999
  ...
# Subtest: P0 at interval 7 enters P2 with a previewed decay date and kept tail
ok 1570 - P0 at interval 7 enters P2 with a previewed decay date and kept tail
  ---
  duration_ms: 3.248344
  ...
# Subtest: P0 at interval 30 enters P3
ok 1571 - P0 at interval 30 enters P3
  ---
  duration_ms: 0.464226
  ...
# Subtest: fixed enter overrides the interval scan
ok 1572 - fixed enter overrides the interval scan
  ---
  duration_ms: 0.421455
  ...
# Subtest: unknown enter disables Not now without disabling Keep/Reword
ok 1573 - unknown enter disables Not now without disabling Keep/Reword
  ---
  duration_ms: 0.388351
  ...
# Subtest: P0 with no suitable level stays unavailable and never shortens the lease
ok 1574 - P0 with no suitable level stays unavailable and never shortens the lease
  ---
  duration_ms: 0.334879
  ...
# Subtest: custom level order resolves entry in ladder order
ok 1575 - custom level order resolves entry in ladder order
  ---
  duration_ms: 0.283752
  ...
# Subtest: unknown priority value disables Not now only
ok 1576 - unknown priority value disables Not now only
  ---
  duration_ms: 0.324569
  ...
# Subtest: prioritized P2 below its roll limit stays on the same level
ok 1577 - prioritized P2 below its roll limit stays on the same level
  ---
  duration_ms: 0.536104
  ...
# Subtest: P2 at its roll limit decays to P3
ok 1578 - P2 at its roll limit decays to P3
  ---
  duration_ms: 0.765271
  ...
# Subtest: P2 streak derives from the task Schedule Log
ok 1579 - P2 streak derives from the task Schedule Log
  ---
  duration_ms: 3.746975
  ...
# Subtest: configured decay:false keeps rolling past the limit
ok 1580 - configured decay:false keeps rolling past the limit
  ---
  duration_ms: 0.391347
  ...
# Subtest: per-level rolls:0 decays immediately
ok 1581 - per-level rolls:0 decays immediately
  ---
  duration_ms: 0.316735
  ...
# Subtest: terminal cancel substitutes a truthful same-level card roll
ok 1582 - terminal cancel substitutes a truthful same-level card roll
  ---
  duration_ms: 0.305914
  ...
# Subtest: no future date in the window refuses Not now
ok 1583 - no future date in the window refuses Not now
  ---
  duration_ms: 0.196104
  ...
# Subtest: Less often steps 7/14/30 to the next preset with a decision reason
ok 1584 - Less often steps 7/14/30 to the next preset with a decision reason
  ---
  duration_ms: 0.550822
  ...
# Subtest: Less often at 90+ opens the constrained custom picker; 365 is unavailable
ok 1585 - Less often at 90+ opens the constrained custom picker; 365 is unavailable
  ---
  duration_ms: 0.331543
  ...
# Subtest: previewed dates are stable for one random draw
ok 1586 - previewed dates are stable for one random draw
  ---
  duration_ms: 0.307517
  ...
# Subtest: Keep saturates at 999 and Drop preserves keeps history
ok 1587 - Keep saturates at 999 and Drop preserves keeps history
  ---
  duration_ms: 0.413148
  ...
# Subtest: kept tails preserve roll classification; decisions break it deliberately
ok 1588 - kept tails preserve roll classification; decisions break it deliberately
  ---
  duration_ms: 1.025138
  ...
# Subtest: invalid priority config offers no priority-changing action
ok 1589 - invalid priority config offers no priority-changing action
  ---
  duration_ms: 0.265106
  ...
# Subtest: decay off disables Not now but keeps counting
ok 1590 - decay off disables Not now but keeps counting
  ---
  duration_ms: 0.243374
  ...
# Subtest: explicit level picks cover the ladder with previewed rolls
ok 1591 - explicit level picks cover the ladder with previewed rolls
  ---
  duration_ms: 0.96333
  ...
# Subtest: card model is deeply frozen
ok 1592 - card model is deeply frozen
  ---
  duration_ms: 0.236601
  ...
# Subtest: single Alt+F on an at-limit task opens the card and writes nothing
ok 1593 - single Alt+F on an at-limit task opens the card and writes nothing
  ---
  duration_ms: 11.241307
  ...
# Subtest: dismissing the card writes nothing and does not advance
ok 1594 - dismissing the card writes nothing and does not advance
  ---
  duration_ms: 2.029997
  ...
# Subtest: early dates open the card and write nothing
ok 1595 - early dates open the card and write nothing
  ---
  duration_ms: 1.58116
  ...
# Subtest: namespace v5 with decide true stamps counted and opens no card
ok 1596 - namespace v5 with decide true stamps counted and opens no card
  ---
  duration_ms: 3.816378
  ...
# Subtest: stale task-line change writes nothing
ok 1597 - stale task-line change writes nothing
  ---
  duration_ms: 1.425352
  ...
# Subtest: stale local-day change writes nothing
ok 1598 - stale local-day change writes nothing
  ---
  duration_ms: 1.242573
  ...
# Subtest: stale decay-config change writes nothing
ok 1599 - stale decay-config change writes nothing
  ---
  duration_ms: 1.284413
  ...
# Subtest: stale priority-ladder config writes nothing
ok 1600 - stale priority-ladder config writes nothing
  ---
  duration_ms: 1.971054
  ...
# Subtest: stale child Schedule Log writes nothing
ok 1601 - stale child Schedule Log writes nothing
  ---
  duration_ms: 2.19435
  ...
# Subtest: Not now stamps, clears keeps, and advances exactly once
ok 1602 - Not now stamps, clears keeps, and advances exactly once
  ---
  duration_ms: 4.95936
  ...
# Subtest: Keep counts once and saturates at 999 without reset
ok 1603 - Keep counts once and saturates at 999 without reset
  ---
  duration_ms: 3.061185
  ...
# Subtest: Keep with a reason logs that reason in the Rotten Log entry
ok 1604 - Keep with a reason logs that reason in the Rotten Log entry
  ---
  duration_ms: 1.367942
  ...
# Subtest: Keep carries the logged history and preview keeps in its context
ok 1605 - Keep carries the logged history and preview keeps in its context
  ---
  duration_ms: 1.225971
  ...
# Subtest: Keep with a stale child log during the stage refuses and rebuilds
ok 1606 - Keep with a stale child log during the stage refuses and rebuilds
  ---
  duration_ms: 0.935226
  ...
# Subtest: Keep with advance commits once and advances exactly once
ok 1607 - Keep with advance commits once and advances exactly once
  ---
  duration_ms: 3.814425
  ...
# Subtest: Reword stamps, clears, logs, and never advances
ok 1608 - Reword stamps, clears, logs, and never advances
  ---
  duration_ms: 1.482993
  ...
# Subtest: Drop cancels with the dropped-after-keeps reason and keeps history
ok 1609 - Drop cancels with the dropped-after-keeps reason and keeps history
  ---
  duration_ms: 0.931159
  ...
# Subtest: Less often at 90+ opens the picker and dismiss writes nothing
ok 1610 - Less often at 90+ opens the picker and dismiss writes nothing
  ---
  duration_ms: 0.836518
  ...
# Subtest: counted session skips at-limit and counts below-limit
ok 1611 - counted session skips at-limit and counts below-limit
  ---
  duration_ms: 1.369425
  ...
# Subtest: counted session skips at-limit on an early date
ok 1612 - counted session skips at-limit on an early date
  ---
  duration_ms: 1.066517
  ...
# Subtest: counted session with every target skipped writes nothing
ok 1613 - counted session with every target skipped writes nothing
  ---
  duration_ms: 0.528018
  ...
# Subtest: opening the card writes nothing and shows the Keep row detail
ok 1614 - opening the card writes nothing and shows the Keep row detail
  ---
  duration_ms: 11.86641
  ...
# Subtest: Esc on the rows closes the card and writes nothing
ok 1615 - Esc on the rows closes the card and writes nothing
  ---
  duration_ms: 2.345609
  ...
# Subtest: Keep swaps the rows for the reason stage without closing
ok 1616 - Keep swaps the rows for the reason stage without closing
  ---
  duration_ms: 2.593422
  ...
# Subtest: repeat Alt+F never enters or submits the stage
ok 1617 - repeat Alt+F never enters or submits the stage
  ---
  duration_ms: 1.600877
  ...
# Subtest: Esc in the stage returns to the rows; a second Esc writes nothing
ok 1618 - Esc in the stage returns to the rows; a second Esc writes nothing
  ---
  duration_ms: 1.634652
  ...
# Subtest: Keep stage Enter logs the reason with one transaction; one undo restores
ok 1619 - Keep stage Enter logs the reason with one transaction; one undo restores
  ---
  duration_ms: 15.746783
  ...
# Subtest: blank Keep stage Enter logs no reason given
ok 1620 - blank Keep stage Enter logs no reason given
  ---
  duration_ms: 16.173166
  ...
# Subtest: a double Enter submits once
ok 1621 - a double Enter submits once
  ---
  duration_ms: 15.754316
  ...
# Subtest: IME Enter never submits the stage
ok 1622 - IME Enter never submits the stage
  ---
  duration_ms: 2.493171
  ...
# Subtest: the card header shows the logged count and last reason
ok 1623 - the card header shows the logged count and last reason
  ---
  duration_ms: 2.390124
  ...
# Subtest: an unreadable log shows the header even with no countable entries
ok 1624 - an unreadable log shows the header even with no countable entries
  ---
  duration_ms: 0.206384
  ...
# Subtest: the decay card Keep stage uses the reviews streak copy
ok 1625 - the decay card Keep stage uses the reviews streak copy
  ---
  duration_ms: 0.212446
  ...
# Subtest: ambiguous Rotten Logs refuse the Keep write
ok 1626 - ambiguous Rotten Logs refuse the Keep write
  ---
  duration_ms: 1.252692
  ...
# Subtest: availability: decay on (or absent) may ask; decay off never asks
ok 1627 - availability: decay on (or absent) may ask; decay off never asks
  ---
  duration_ms: 0.986714
  ...
# Subtest: trigger: only an explicit decide row decides
ok 1628 - trigger: only an explicit decide row decides
  ---
  duration_ms: 0.191566
  ...
# Subtest: partition: exact at-limit rows skip, everything else stamps
ok 1629 - partition: exact at-limit rows skip, everything else stamps
  ---
  duration_ms: 0.697191
  ...
# Subtest: partition: empty and malformed input stamps nothing and skips nothing
ok 1630 - partition: empty and malformed input stamps nothing and skips nothing
  ---
  duration_ms: 0.147301
  ...
# Subtest: partition: enabled false stamps decision rows (older namespace fallback)
ok 1631 - partition: enabled false stamps decision rows (older namespace fallback)
  ---
  duration_ms: 0.163372
  ...
# Subtest: skip wording: singular, plural, and all-skipped notices
ok 1632 - skip wording: singular, plural, and all-skipped notices
  ---
  duration_ms: 0.187808
  ...
# Subtest: reword cursor: lands at the end of the task body before metadata
ok 1633 - reword cursor: lands at the end of the task body before metadata
  ---
  duration_ms: 0.374225
  ...
# Subtest: captured age: optional context ages, null when created is missing
ok 1634 - captured age: optional context ages, null when created is missing
  ---
  duration_ms: 0.411045
  ...
# Subtest: rows: P0 entry shows the recommended Not now with a clean window
ok 1635 - rows: P0 entry shows the recommended Not now with a clean window
  ---
  duration_ms: 2.881713
  ...
# Subtest: rows: invalid priority config disables Not now and levels, keeps safe rows
ok 1636 - rows: invalid priority config disables Not now and levels, keeps safe rows
  ---
  duration_ms: 0.612059
  ...
# Subtest: rows: picker-mode Less often and 365-day cap
ok 1637 - rows: picker-mode Less often and 365-day cap
  ---
  duration_ms: 0.940366
  ...
# Subtest: rows: terminal ladder keeps Enter available and never cancels
ok 1638 - rows: terminal ladder keeps Enter available and never cancels
  ---
  duration_ms: 0.602531
  ...
# Subtest: modal: Enter approves once; later keys cannot approve again
ok 1639 - modal: Enter approves once; later keys cannot approve again
  ---
  duration_ms: 0.568556
  ...
# Subtest: modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
ok 1640 - modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click
  ---
  duration_ms: 0.404412
  ...
# Subtest: modal: key repeat and modified keys never approve
ok 1641 - modal: key repeat and modified keys never approve
  ---
  duration_ms: 0.221433
  ...
# Subtest: modal: Esc changes nothing — dismiss without a choice
ok 1642 - modal: Esc changes nothing — dismiss without a choice
  ---
  duration_ms: 0.135879
  ...
# Subtest: modal: unavailable actions cannot be chosen
ok 1643 - modal: unavailable actions cannot be chosen
  ---
  duration_ms: 0.14689
  ...
# Subtest: modal: a double callback applies once
ok 1644 - modal: a double callback applies once
  ---
  duration_ms: 0.101263
  ...
# Subtest: capability: the nav api exposes the card while loaded
ok 1645 - capability: the nav api exposes the card while loaded
  ---
  duration_ms: 0.426355
  ...
# Subtest: capability: unload drops the card so marks stop promising it
ok 1646 - capability: unload drops the card so marks stop promising it
  ---
  duration_ms: 0.145999
  ...
# Subtest: ladder lookup: the first priority property wins, null without one
ok 1647 - ladder lookup: the first priority property wins, null without one
  ---
  duration_ms: 0.15182
  ...
# Subtest: stage entry resolves the line itself and refuses prose
ok 1648 - stage entry resolves the line itself and refuses prose
  ---
  duration_ms: 3.447262
  ...
# Subtest: Ctrl+Shift+P on a BLOCKS line opens the owner's Blocks stage directly
ok 1649 - Ctrl+Shift+P on a BLOCKS line opens the owner's Blocks stage directly
  ---
  duration_ms: 1.292899
  ...
# Subtest: Ctrl+Shift+P hotkey path on a BLOCKS line opens the owner's Blocks stage directly
ok 1650 - Ctrl+Shift+P hotkey path on a BLOCKS line opens the owner's Blocks stage directly
  ---
  duration_ms: 0.763377
  ...
# Subtest: Ctrl+Shift+Alt+B on a BLOCKS or Depends-On line opens the owner's Blocks stage
ok 1651 - Ctrl+Shift+Alt+B on a BLOCKS or Depends-On line opens the owner's Blocks stage
  ---
  duration_ms: 0.462874
  ...
# Subtest: Ctrl+Shift+P on a Depends-On line is unchanged forward behavior
ok 1652 - Ctrl+Shift+P on a Depends-On line is unchanged forward behavior
  ---
  duration_ms: 0.430392
  ...
# Subtest: Ctrl+Shift+P on a plain child bullet and a nested Task Link are unchanged (3e359a6)
ok 1653 - Ctrl+Shift+P on a plain child bullet and a nested Task Link are unchanged (3e359a6)
  ---
  duration_ms: 7.401334
  ...
# Subtest: forward counted mixed row in BLOCKED keeps the waits-on badge (3e359a6 order)
ok 1654 - forward counted mixed row in BLOCKED keeps the waits-on badge (3e359a6 order)
  ---
  duration_ms: 2.459968
  ...
# Subtest: api.blocks opens the stage and removes only a listed dependent
ok 1655 - api.blocks opens the stage and removes only a listed dependent
  ---
  duration_ms: 2.03162
  ...
# Subtest: api.blocks removeDependent on an owner with no ^id is not-a-dependent
ok 1656 - api.blocks removeDependent on an owner with no ^id is not-a-dependent
  ---
  duration_ms: 0.472953
  ...
# Subtest: stage canonical order ranks \#hide last ahead of the lane
ok 1657 - stage canonical order ranks \#hide last ahead of the lane
  ---
  duration_ms: 0.477662
  ...
# Subtest: stage empty query shows same-note plus In Progress and Next only
ok 1658 - stage empty query shows same-note plus In Progress and Next only
  ---
  duration_ms: 2.650852
  ...
# Subtest: stage cap appends a type-to-search-more hint row
ok 1659 - stage cap appends a type-to-search-more hint row
  ---
  duration_ms: 2.825045
  ...
# Subtest: stage BLOCKED rows carry waits-on counts and short guard reasons
ok 1660 - stage BLOCKED rows carry waits-on counts and short guard reasons
  ---
  duration_ms: 1.412547
  ...
# Subtest: stage removal notices name the task description, not the block id
ok 1661 - stage removal notices name the task description, not the block id
  ---
  duration_ms: 0.562534
  ...
# Subtest: stage Task Link batches keep Depends on without refusal
ok 1662 - stage Task Link batches keep Depends on without refusal
  ---
  duration_ms: 0.561833
  ...
# Subtest: stage batch cycle check runs on the post-batch graph
ok 1663 - stage batch cycle check runs on the post-batch graph
  ---
  duration_ms: 0.645382
  ...
# Subtest: stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
ok 1664 - stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke
  ---
  duration_ms: 48.219216
  ...
# Subtest: stage stale single add refuses and reopens
ok 1665 - stage stale single add refuses and reopens
  ---
  duration_ms: 1.866805
  ...
# Subtest: Task Link Depends on focuses a linked note open in a background tab
ok 1666 - Task Link Depends on focuses a linked note open in a background tab
  ---
  duration_ms: 0.874821
  ...
# Subtest: Task Link Blocks focuses the linked note and opens Blocks directly
ok 1667 - Task Link Blocks focuses the linked note and opens Blocks directly
  ---
  duration_ms: 0.674277
  ...
# Subtest: Task Link Depends on refuses clearly when the linked note cannot be focused
    # Subtest: focus reports success but the active view stays elsewhere
    ok 1 - focus reports success but the active view stays elsewhere
      ---
      duration_ms: 0.217765
      ...
    # Subtest: focus reports failure
    ok 2 - focus reports failure
      ---
      duration_ms: 0.156619
      ...
    1..2
ok 1668 - Task Link Depends on refuses clearly when the linked note cannot be focused
  ---
  duration_ms: 0.728321
  ...
# Subtest: stage mirror burst keeps the baseline owner across an insertion above
ok 1669 - stage mirror burst keeps the baseline owner across an insertion above
  ---
  duration_ms: 1006.608835
  ...
# Subtest: stage mirror burst clears on a text-only line deletion
ok 1670 - stage mirror burst clears on a text-only line deletion
  ---
  duration_ms: 1002.878231
  ...
# Subtest: stage mirror vim dd clears the deleted line's owner
ok 1671 - stage mirror vim dd clears the deleted line's owner
  ---
  duration_ms: 1003.622973
  ...
# Subtest: stage badge counts open prerequisites without a block id
ok 1672 - stage badge counts open prerequisites without a block id
  ---
  duration_ms: 5.762874
  ...
# Subtest: stage badge names the future scheduled date with no open prerequisite
ok 1673 - stage badge names the future scheduled date with no open prerequisite
  ---
  duration_ms: 1.8275
  ...
# Subtest: stage badge reads blocked with nothing waiting and no schedule
ok 1674 - stage badge reads blocked with nothing waiting and no schedule
  ---
  duration_ms: 1.122814
  ...
# Subtest: stage vault batch with a stale row refuses and reopens
ok 1675 - stage vault batch with a stale row refuses and reopens
  ---
  duration_ms: 8.820324
  ...
# Subtest: stage opening builds 200/400/1000-task notes without cubic growth
ok 1676 - stage opening builds 200/400/1000-task notes without cubic growth
  ---
  duration_ms: 68.601429
  ...
# Subtest: stage snapshots match standalone parsing across grammar vectors
ok 1677 - stage snapshots match standalone parsing across grammar vectors
  ---
  duration_ms: 7.37845
  ...
# Subtest: stage Warm-empty cache is ready without a vault fallback
ok 1678 - stage Warm-empty cache is ready without a vault fallback
  ---
  duration_ms: 0.758058
  ...
# Subtest: stage opening renders cross-note results with zero writes and cap
ok 1679 - stage opening renders cross-note results with zero writes and cap
  ---
  duration_ms: 47.749528
  ...
# Subtest: stage CURRENT covers same-note, cross-note, blocked, and counted parents
ok 1680 - stage CURRENT covers same-note, cross-note, blocked, and counted parents
  ---
  duration_ms: 2.600215
  ...
# Subtest: stage collections reuse one snapshot per parent
ok 1681 - stage collections reuse one snapshot per parent
  ---
  duration_ms: 0.528429
  ...
# Subtest: stage cold refresh yields, preserves state, and performs no search reads
ok 1682 - stage cold refresh yields, preserves state, and performs no search reads
  ---
  duration_ms: 118.303453
  ...
# Subtest: stage cold refresh abandons after dismissal or replacement
ok 1683 - stage cold refresh abandons after dismissal or replacement
  ---
  duration_ms: 54.956441
  ...
# Subtest: stage 400-task opening finishes in a child process before the parent timeout
ok 1684 - stage 400-task opening finishes in a child process before the parent timeout
  ---
  duration_ms: 111.450758
  ...
# Subtest: stage ranker passes the DK contract vectors verbatim
ok 1685 - stage ranker passes the DK contract vectors verbatim
  ---
  duration_ms: 4.014617
  ...
# Subtest: stage ranker tiers match the capture ranker tier order
ok 1686 - stage ranker tiers match the capture ranker tier order
  ---
  duration_ms: 0.883868
  ...
# Subtest: stage pool excludes daily notes, done, templates, and dot-dirs
ok 1687 - stage pool excludes daily notes, done, templates, and dot-dirs
  ---
  duration_ms: 0.614664
  ...
# Subtest: stage pool collects open vault tasks with buffers as given
ok 1688 - stage pool collects open vault tasks with buffers as given
  ---
  duration_ms: 3.466119
  ...
# Subtest: stage CURRENT resolves same-note, missing, closed, and non-task targets
ok 1689 - stage CURRENT resolves same-note, missing, closed, and non-task targets
  ---
  duration_ms: 2.520944
  ...
# Subtest: stage cycle guard reports the path back to the dependent
ok 1690 - stage cycle guard reports the path back to the dependent
  ---
  duration_ms: 1.017132
  ...
# Subtest: stage view groups CURRENT, RESULTS, and BLOCKED with guards
ok 1691 - stage view groups CURRENT, RESULTS, and BLOCKED with guards
  ---
  duration_ms: 3.174432
  ...
# Subtest: stage view disables cycles and unencodable targets, keeps +id rows
ok 1692 - stage view disables cycles and unencodable targets, keeps +id rows
  ---
  duration_ms: 1.199741
  ...
# Subtest: stage cache tasks normalize across Tasks shapes, buffers win
ok 1693 - stage cache tasks normalize across Tasks shapes, buffers win
  ---
  duration_ms: 0.94766
  ...
# Subtest: stage Task Link mode shows Depends on for one link and batches
ok 1694 - stage Task Link mode shows Depends on for one link and batches
  ---
  duration_ms: 3.001783
  ...
# Subtest: stage mark keys never collide across notes
ok 1695 - stage mark keys never collide across notes
  ---
  duration_ms: 0.262401
  ...
# Subtest: stage display-text locating matches one open task
ok 1696 - stage display-text locating matches one open task
  ---
  duration_ms: 0.343145
  ...
# Subtest: stage selection refusal spans tasks only
ok 1697 - stage selection refusal spans tasks only
  ---
  duration_ms: 0.264285
  ...
# Subtest: stage builder composes pool, current, guards, and pill title
ok 1698 - stage builder composes pool, current, guards, and pill title
  ---
  duration_ms: 2.508732
  ...
# Subtest: stage counted vault add with a stale target refuses and reopens
ok 1699 - stage counted vault add with a stale target refuses and reopens
  ---
  duration_ms: 10.999905
  ...
# Subtest: stage vault commit with a stale write notifies once and reopens
ok 1700 - stage vault commit with a stale write notifies once and reopens
  ---
  duration_ms: 8.090872
  ...
# Subtest: commitVaultRefs refuses a cycle through implicit resident edges
ok 1701 - commitVaultRefs refuses a cycle through implicit resident edges
  ---
  duration_ms: 2.253234
  ...
# Subtest: stage single remove with a stale write notifies once and reopens
ok 1702 - stage single remove with a stale write notifies once and reopens
  ---
  duration_ms: 2.876683
  ...
# Subtest: stage vault single +id guard refuses a stale target
ok 1703 - stage vault single +id guard refuses a stale target
  ---
  duration_ms: 1.382079
  ...
# Subtest: stage vault counted +id guard refuses a stale target
ok 1704 - stage vault counted +id guard refuses a stale target
  ---
  duration_ms: 1.055094
  ...
# Subtest: stage single +id guard refuses a stale target
ok 1705 - stage single +id guard refuses a stale target
  ---
  duration_ms: 0.99504
  ...
# Subtest: stage counted remove with a stale write refuses and reopens
ok 1706 - stage counted remove with a stale write refuses and reopens
  ---
  duration_ms: 3.510464
  ...
# Subtest: stage counted remove counts only changed sources
ok 1707 - stage counted remove counts only changed sources
  ---
  duration_ms: 5.031769
  ...
# Subtest: counted local add on [?] sources reads zero extra notes
ok 1708 - counted local add on [?] sources reads zero extra notes
  ---
  duration_ms: 6.495715
  ...
# Subtest: counted local toggle-off on a Pomodoro-linked [?] source recovers
ok 1709 - counted local toggle-off on a Pomodoro-linked [?] source recovers
  ---
  duration_ms: 7.068461
  ...
# Subtest: stage counted vault add counts only changed sources
ok 1710 - stage counted vault add counts only changed sources
  ---
  duration_ms: 3.369435
  ...
# Subtest: stage counted vault remove counts only changed sources
ok 1711 - stage counted vault remove counts only changed sources
  ---
  duration_ms: 2.230139
  ...
# Subtest: vault counted same-note add follows BLOCKS shifts with post-plan stamps
ok 1712 - vault counted same-note add follows BLOCKS shifts with post-plan stamps
  ---
  duration_ms: 2.539289
  ...
# Subtest: vault counted same-note remove follows BLOCKS deletions
ok 1713 - vault counted same-note remove follows BLOCKS deletions
  ---
  duration_ms: 3.194079
  ...
# Subtest: vault counted cross-note add keeps follow-up behavior
ok 1714 - vault counted cross-note add keeps follow-up behavior
  ---
  duration_ms: 2.247552
  ...
# Subtest: stage +id row prompts without writing
ok 1715 - stage +id row prompts without writing
  ---
  duration_ms: 10.938371
  ...
# Subtest: stage dismissal writes no bytes and drops the batch
ok 1716 - stage dismissal writes no bytes and drops the batch
  ---
  duration_ms: 1.546132
  ...
# Subtest: stage same-note batch commits in one undo group
ok 1717 - stage same-note batch commits in one undo group
  ---
  duration_ms: 13.007108
  ...
# Subtest: stage batch with a stale row refuses and reopens
ok 1718 - stage batch with a stale row refuses and reopens
  ---
  duration_ms: 1.451071
  ...
# Subtest: stage counted add applies to every source task
ok 1719 - stage counted add applies to every source task
  ---
  duration_ms: 38.709446
  ...
# Subtest: stage batch cycle rows stay guarded and write nothing
ok 1720 - stage batch cycle rows stay guarded and write nothing
  ---
  duration_ms: 29.884971
  ...
# Subtest: stage edit-task-dependencies registers with no default hotkey
ok 1721 - stage edit-task-dependencies registers with no default hotkey
  ---
  duration_ms: 2.140407
  ...
# Subtest: task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row
ok 1722 - task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row
  ---
  duration_ms: 9.570796
  ...
# Subtest: task-card-blocks registers Ctrl+Shift+Alt+B and opens the Blocks row
ok 1723 - task-card-blocks registers Ctrl+Shift+Alt+B and opens the Blocks row
  ---
  duration_ms: 1.013736
  ...
# Subtest: stage waits-on badge counts open prerequisites only
ok 1724 - stage waits-on badge counts open prerequisites only
  ---
  duration_ms: 2.651122
  ...
# Subtest: stage cycle tooltip shows task descriptions
ok 1725 - stage cycle tooltip shows task descriptions
  ---
  duration_ms: 2.060825
  ...
# Subtest: stage same-note single add stamps the dependent and keeps its cursor
ok 1726 - stage same-note single add stamps the dependent and keeps its cursor
  ---
  duration_ms: 9.088979
  ...
# Subtest: stage same-note marked batch stamps the dependent and keeps its cursor
ok 1727 - stage same-note marked batch stamps the dependent and keeps its cursor
  ---
  duration_ms: 7.82904
  ...
# Subtest: Tab marks a same-note CURRENT row and Enter removes it
ok 1728 - Tab marks a same-note CURRENT row and Enter removes it
  ---
  duration_ms: 32.59713
  ...
# Subtest: Tab twice unmarks a CURRENT row
ok 1729 - Tab twice unmarks a CURRENT row
  ---
  duration_ms: 28.314241
  ...
# Subtest: Tab mixed CURRENT removal and RESULTS add apply in one commit
ok 1730 - Tab mixed CURRENT removal and RESULTS add apply in one commit
  ---
  duration_ms: 29.95232
  ...
# Subtest: Tab marks a missing CURRENT target and the batch removes it
ok 1731 - Tab marks a missing CURRENT target and the batch removes it
  ---
  duration_ms: 31.353987
  ...
# Subtest: Tab same-note and cross-note CURRENT removals apply in one vault batch
ok 1732 - Tab same-note and cross-note CURRENT removals apply in one vault batch
  ---
  duration_ms: 32.53436
  ...
# Subtest: cross-note add awaits preparation before the one commit
ok 1733 - cross-note add awaits preparation before the one commit
  ---
  duration_ms: 23.393783
  ...
# Subtest: a failed async preparation leaves the dependent untouched
ok 1734 - a failed async preparation leaves the dependent untouched
  ---
  duration_ms: 8.027402
  ...
# Subtest: links to unloaded notes tolerate add, remove, and deleted targets
ok 1735 - links to unloaded notes tolerate add, remove, and deleted targets
  ---
  duration_ms: 5.26815
  ...
# Subtest: Pomodoro-linked dependents recover through the plugin vault read
ok 1736 - Pomodoro-linked dependents recover through the plugin vault read
  ---
  duration_ms: 8.568432
  ...
# Subtest: same-note batch +id stamps the target and links in one undo group
ok 1737 - same-note batch +id stamps the target and links in one undo group
  ---
  duration_ms: 12.259363
  ...
# Subtest: confirmBatchBlockId collects the id and executes the batch
ok 1738 - confirmBatchBlockId collects the id and executes the batch
  ---
  duration_ms: 3.587311
  ...
# Subtest: commitMarkedDependencies executes ready additions at once
ok 1739 - commitMarkedDependencies executes ready additions at once
  ---
  duration_ms: 3.904556
  ...
# Subtest: counted vault add links two siblings bottom-up
ok 1740 - counted vault add links two siblings bottom-up
  ---
  duration_ms: 6.165393
  ...
# Subtest: counted CURRENT rows without a line remove from every source
ok 1741 - counted CURRENT rows without a line remove from every source
  ---
  duration_ms: 9.286185
  ...
# Subtest: a stale editor between await and commit refuses
ok 1742 - a stale editor between await and commit refuses
  ---
  duration_ms: 2.159815
  ...
# Subtest: removeDependencyByRef refuses targets that are not on the line
ok 1743 - removeDependencyByRef refuses targets that are not on the line
  ---
  duration_ms: 2.06258
  ...
# Subtest: kept unloaded links resolve the field id by line position
ok 1744 - kept unloaded links resolve the field id by line position
  ---
  duration_ms: 3.050605
  ...
# Subtest: pendingTargetLine commits the same-note target id with the link
ok 1745 - pendingTargetLine commits the same-note target id with the link
  ---
  duration_ms: 2.486248
  ...
# Subtest: counted vault add commits every source in one transaction
ok 1746 - counted vault add commits every source in one transaction
  ---
  duration_ms: 3.472832
  ...
# Subtest: field-only clears snapshot the vault and recover
ok 1747 - field-only clears snapshot the vault and recover
  ---
  duration_ms: 2.101763
  ...
# Subtest: adds without recovery read zero extra vault notes
ok 1748 - adds without recovery read zero extra vault notes
  ---
  duration_ms: 1.054834
  ...
# Subtest: hand-edit clear recovers Pomodoro-linked dependents to Next
ok 1749 - hand-edit clear recovers Pomodoro-linked dependents to Next
  ---
  duration_ms: 4.49857
  ...
# Subtest: hand-edit clear on a non-Blocked parent reads zero extra notes
ok 1750 - hand-edit clear on a non-Blocked parent reads zero extra notes
  ---
  duration_ms: 0.608082
  ...
# Subtest: writer keeps the full route for duplicate basenames
ok 1751 - writer keeps the full route for duplicate basenames
  ---
  duration_ms: 1.004888
  ...
# Subtest: adds on Blocked parents and non-Blocked mirror touches read nothing
ok 1752 - adds on Blocked parents and non-Blocked mirror touches read nothing
  ---
  duration_ms: 1.122944
  ...
# Subtest: counted vault add loads each source's existing links
ok 1753 - counted vault add loads each source's existing links
  ---
  duration_ms: 3.600606
  ...
# Subtest: counted Ctrl+D on a blockquoted task refuses with the blockquote notice
ok 1754 - counted Ctrl+D on a blockquoted task refuses with the blockquote notice
  ---
  duration_ms: 0.676041
  ...
# Subtest: single Ctrl+D on a quoted task without a field refuses as a blockquote
ok 1755 - single Ctrl+D on a quoted task without a field refuses as a blockquote
  ---
  duration_ms: 0.226753
  ...
# Subtest: confirmSingleBlockId folds the target id into one transaction
ok 1756 - confirmSingleBlockId folds the target id into one transaction
  ---
  duration_ms: 2.320122
  ...
# Subtest: chooseTaskDependency folds a missing target id into one transaction
ok 1757 - chooseTaskDependency folds a missing target id into one transaction
  ---
  duration_ms: 1.971225
  ...
# Subtest: counted remove commits every source in one transaction
ok 1758 - counted remove commits every source in one transaction
  ---
  duration_ms: 3.280786
  ...
# Subtest: DP parse vectors accept, empty, malformed, and not-a-line
ok 1759 - DP parse vectors accept, empty, malformed, and not-a-line
  ---
  duration_ms: 3.502688
  ...
# Subtest: DP30 attributes a Work-Log-nested Depends-On line to the inner task
ok 1760 - DP30 attributes a Work-Log-nested Depends-On line to the inner task
  ---
  duration_ms: 2.813974
  ...
# Subtest: fenced lines never collect as Depends-On lines
ok 1761 - fenced lines never collect as Depends-On lines
  ---
  duration_ms: 0.404002
  ...
# Subtest: DW1 creates the line as the first child
ok 1762 - DW1 creates the line as the first child
  ---
  duration_ms: 5.419329
  ...
# Subtest: DW2 creates the line after a Cancel Log
ok 1763 - DW2 creates the line after a Cancel Log
  ---
  duration_ms: 1.200943
  ...
# Subtest: DW3-DW5 append, remove the middle, and delete on the last link
ok 1764 - DW3-DW5 append, remove the middle, and delete on the last link
  ---
  duration_ms: 5.165846
  ...
# Subtest: DW6-DW7 re-add moves to the end and the field mirrors the line
ok 1765 - DW6-DW7 re-add moves to the end and the field mirrors the line
  ---
  duration_ms: 0.612129
  ...
# Subtest: DW8 tab parents deepen the child by one tab
ok 1766 - DW8 tab parents deepen the child by one tab
  ---
  duration_ms: 1.084331
  ...
# Subtest: DW9 space parents reuse the existing child indent
ok 1767 - DW9 space parents reuse the existing child indent
  ---
  duration_ms: 0.904938
  ...
# Subtest: DW10-DW11 CRLF and final-newline state survive
ok 1768 - DW10-DW11 CRLF and final-newline state survive
  ---
  duration_ms: 0.916159
  ...
# Subtest: DW12-DW14 link form is the shortest unambiguous form
ok 1769 - DW12-DW14 link form is the shortest unambiguous form
  ---
  duration_ms: 0.287088
  ...
# Subtest: archive targets keep the explicit done/ path form
ok 1770 - archive targets keep the explicit done/ path form
  ---
  duration_ms: 0.201585
  ...
# Subtest: DW15 an existing id is never rewritten
ok 1771 - DW15 an existing id is never rewritten
  ---
  duration_ms: 0.349547
  ...
# Subtest: DW16 an unencodable path without an id refuses
ok 1772 - DW16 an unencodable path without an id refuses
  ---
  duration_ms: 0.263042
  ...
# Subtest: DW17 field placement follows fresh and precedes the block id
ok 1773 - DW17 field placement follows fresh and precedes the block id
  ---
  duration_ms: 0.307206
  ...
# Subtest: DW18 legacy children fold into the line
ok 1774 - DW18 legacy children fold into the line
  ---
  duration_ms: 0.828302
  ...
# Subtest: DW19 variants canonicalise to the writer form
ok 1775 - DW19 variants canonicalise to the writer form
  ---
  duration_ms: 1.40341
  ...
# Subtest: adding an open prerequisite blocks the dependent
ok 1776 - adding an open prerequisite blocks the dependent
  ---
  duration_ms: 0.363434
  ...
# Subtest: adding transfers Next and In Progress commitment to the open target
ok 1777 - adding transfers Next and In Progress commitment to the open target
  ---
  duration_ms: 1.737057
  ...
# Subtest: removing the last open prerequisite recovers immediately
ok 1778 - removing the last open prerequisite recovers immediately
  ---
  duration_ms: 0.9062
  ...
# Subtest: removal stays Blocked while another prerequisite is open
ok 1779 - removal stays Blocked while another prerequisite is open
  ---
  duration_ms: 0.464948
  ...
# Subtest: removal stays Blocked with a future schedule
ok 1780 - removal stays Blocked with a future schedule
  ---
  duration_ms: 0.423849
  ...
# Subtest: one gesture commits the dependent note in a single transaction
ok 1781 - one gesture commits the dependent note in a single transaction
  ---
  duration_ms: 1.975492
  ...
# Subtest: a failed preparation leaves the dependent untouched
ok 1782 - a failed preparation leaves the dependent untouched
  ---
  duration_ms: 0.475939
  ...
# Subtest: recovery references follow the line plus covered legacy children
ok 1783 - recovery references follow the line plus covered legacy children
  ---
  duration_ms: 0.537948
  ...
# Subtest: task-block helpers find owners, lines, and insertion points
ok 1784 - task-block helpers find owners, lines, and insertion points
  ---
  duration_ms: 0.422437
  ...
# Subtest: dependency notices follow the contract shapes
ok 1785 - dependency notices follow the contract shapes
  ---
  duration_ms: 0.179433
  ...
# Subtest: nav api v3 resolves results and never throws
ok 1786 - nav api v3 resolves results and never throws
  ---
  duration_ms: 1.516125
  ...
# Subtest: getDependencyInsertLine lands after a Cancel Log subtree
ok 1787 - getDependencyInsertLine lands after a Cancel Log subtree
  ---
  duration_ms: 0.33505
  ...
# Subtest: planner: an ordinary dependent with a block id plus an open add yields one target
ok 1788 - planner: an ordinary dependent with a block id plus an open add yields one target
  ---
  duration_ms: 6.944081
  ...
# Subtest: planner: adding only a closed target yields none
ok 1789 - planner: adding only a closed target yields none
  ---
  duration_ms: 0.962407
  ...
# Subtest: planner: no block id yields none
ok 1790 - planner: no block id yields none
  ---
  duration_ms: 0.585758
  ...
# Subtest: planner: a dependent already [?] with an open add yields a target
ok 1791 - planner: a dependent already [?] with an open add yields a target
  ---
  duration_ms: 1.964592
  ...
# Subtest: planner: a removal yields none
ok 1792 - planner: a removal yields none
  ---
  duration_ms: 1.007464
  ...
# Subtest: planner: mirrorTouch emits no ordinary consumption target
ok 1793 - planner: mirrorTouch emits no ordinary consumption target
  ---
  duration_ms: 0.437766
  ...
# Subtest: planner: ^prj keeps project targets and a deduplicated union
ok 1794 - planner: ^prj keeps project targets and a deduplicated union
  ---
  duration_ms: 2.252762
  ...
# Subtest: suffix helper names the removed count and the failed follow-up
ok 1795 - suffix helper names the removed count and the failed follow-up
  ---
  duration_ms: 0.156268
  ...
# Subtest: applyDependencyEdit cross-file consumes live links and emptied entries
ok 1796 - applyDependencyEdit cross-file consumes live links and emptied entries
  ---
  duration_ms: 10.071153
  ...
# Subtest: applyDependencyEdit removes one live link and reports it
ok 1797 - applyDependencyEdit removes one live link and reports it
  ---
  duration_ms: 3.290605
  ...
# Subtest: applyDependencyEdit keeps the dependent write when the daily preimage changes
ok 1798 - applyDependencyEdit keeps the dependent write when the daily preimage changes
  ---
  duration_ms: 2.151269
  ...
# Subtest: same-file fold lands the dependency and the cleanup in one undo group
ok 1799 - same-file fold lands the dependency and the cleanup in one undo group
  ---
  duration_ms: 2.54539
  ...
# Subtest: setLocalTaskDependencyLink stays synchronous and folds same-file cleanup
ok 1800 - setLocalTaskDependencyLink stays synchronous and folds same-file cleanup
  ---
  duration_ms: 3.751905
  ...
# Subtest: setLocalTaskDependencyLink cross-file continuation removes the live link
ok 1801 - setLocalTaskDependencyLink cross-file continuation removes the live link
  ---
  duration_ms: 14.161283
  ...
# Subtest: same-note marked batch consumes every newly Blocked source
ok 1802 - same-note marked batch consumes every newly Blocked source
  ---
  duration_ms: 9.792713
  ...
# Subtest: counted same-note writer consumes every newly Blocked source
ok 1803 - counted same-note writer consumes every newly Blocked source
  ---
  duration_ms: 6.349034
  ...
# Subtest: counted vault writer consumes every newly Blocked source
ok 1804 - counted vault writer consumes every newly Blocked source
  ---
  duration_ms: 5.389261
  ...
# Subtest: counted ^prj source consumes its project targets
ok 1805 - counted ^prj source consumes its project targets
  ---
  duration_ms: 5.595165
  ...
# Subtest: a dependent without a block id does zero cachedReads even when today's daily exists
ok 1806 - a dependent without a block id does zero cachedReads even when today's daily exists
  ---
  duration_ms: 2.520705
  ...
# Subtest: alignment key ignores fields, the block id, the status and trailing space
ok 1807 - alignment key ignores fields, the block id, the status and trailing space
  ---
  duration_ms: 1.405293
  ...
# Subtest: insertion after a modified line edits that line and inserts after it
ok 1808 - insertion after a modified line edits that line and inserts after it
  ---
  duration_ms: 1.522858
  ...
# Subtest: adjacent prerequisite and parent both change while two lines insert
ok 1809 - adjacent prerequisite and parent both change while two lines insert
  ---
  duration_ms: 0.547897
  ...
# Subtest: deletion at the end of the document
ok 1810 - deletion at the end of the document
  ---
  duration_ms: 0.477401
  ...
# Subtest: insertion at the top and at the end of the document
ok 1811 - insertion at the top and at the end of the document
  ---
  duration_ms: 0.399964
  ...
# Subtest: empty documents align and apply
ok 1812 - empty documents align and apply
  ---
  duration_ms: 0.254516
  ...
# Subtest: CRLF documents insert and delete with CRLF
ok 1813 - CRLF documents insert and delete with CRLF
  ---
  duration_ms: 0.295614
  ...
# Subtest: equal-count shifted edits take the aligned path
ok 1814 - equal-count shifted edits take the aligned path
  ---
  duration_ms: 0.56587
  ...
# Subtest: pure in-place edits keep the line-bounded change shapes
ok 1815 - pure in-place edits keep the line-bounded change shapes
  ---
  duration_ms: 0.740223
  ...
# Subtest: an unchanged document writes nothing
ok 1816 - an unchanged document writes nothing
  ---
  duration_ms: 0.409873
  ...
# Subtest: an explicit final cursor wins over the mapped cursor
ok 1817 - an explicit final cursor wins over the mapped cursor
  ---
  duration_ms: 0.259736
  ...
# Subtest: the machine-write annotation still reaches the transaction
ok 1818 - the machine-write annotation still reaches the transaction
  ---
  duration_ms: 0.173351
  ...
# Subtest: an editor without transaction falls back to bottom-up replaceRange
ok 1819 - an editor without transaction falls back to bottom-up replaceRange
  ---
  duration_ms: 0.322766
  ...
# Subtest: positions map through aligned, changed, gap and deleted lines
ok 1820 - positions map through aligned, changed, gap and deleted lines
  ---
  duration_ms: 0.410935
  ...
# Subtest: a deletion at the end of the document maps to the last line
ok 1821 - a deletion at the end of the document maps to the last line
  ---
  duration_ms: 0.133064
  ...
# Subtest: a gap with new lines maps by offset and clamps to its last line
ok 1822 - a gap with new lines maps by offset and clamps to its last line
  ---
  duration_ms: 0.17761
  ...
# Subtest: seeded property: planned changes rebuild the new text and map unchanged lines
ok 1823 - seeded property: planned changes rebuild the new text and map unchanged lines
  ---
  duration_ms: 53.702666
  ...
# Subtest: a diff past the edit cap becomes one unaligned gap
ok 1824 - a diff past the edit cap becomes one unaligned gap
  ---
  duration_ms: 107.826547
  ...
# Subtest: the CM6 double reproduces the whole-document replacement jump
ok 1825 - the CM6 double reproduces the whole-document replacement jump
  ---
  duration_ms: 0.755112
  ...
# Subtest: first cross-note prerequisite keeps the cursor and the viewport
ok 1826 - first cross-note prerequisite keeps the cursor and the viewport
  ---
  duration_ms: 8.299869
  ...
# Subtest: same-note prerequisite directly above keeps the dependent's line
ok 1827 - same-note prerequisite directly above keeps the dependent's line
  ---
  duration_ms: 3.981584
  ...
# Subtest: removing the last prerequisite keeps the dependent's line
ok 1828 - removing the last prerequisite keeps the dependent's line
  ---
  duration_ms: 4.331774
  ...
# Subtest: a Blocks source gaining its first BLOCKS line keeps its line
ok 1829 - a Blocks source gaining its first BLOCKS line keeps its line
  ---
  duration_ms: 0.49197
  ...
# Subtest: missing ledger-tools api refuses the review namespace
ok 1830 - missing ledger-tools api refuses the review namespace
  ---
  duration_ms: 2.069873
  ...
# Subtest: review jump on an empty queue
ok 1831 - review jump on an empty queue
  ---
  duration_ms: 1.263754
  ...
# Subtest: review jump from a queued task goes to the neighbor
ok 1832 - review jump from a queued task goes to the neighbor
  ---
  duration_ms: 0.830285
  ...
# Subtest: review jump wraps at the ends
ok 1833 - review jump wraps at the ends
  ---
  duration_ms: 0.392871
  ...
# Subtest: review jump from elsewhere goes to the first or last entry
ok 1834 - review jump from elsewhere goes to the first or last entry
  ---
  duration_ms: 0.226021
  ...
# Subtest: review jump matches a moved cursor task by text
ok 1835 - review jump matches a moved cursor task by text
  ---
  duration_ms: 0.191937
  ...
# Subtest: review jump from a just-stamped rank goes to the entry after it
ok 1836 - review jump from a just-stamped rank goes to the entry after it
  ---
  duration_ms: 0.295324
  ...
# Subtest: review jump skips just-stamped keys the lagging cache still shows
ok 1837 - review jump skips just-stamped keys the lagging cache still shows
  ---
  duration_ms: 0.149846
  ...
# Subtest: review jump after stamping everything reports empty or wraps
ok 1838 - review jump after stamping everything reports empty or wraps
  ---
  duration_ms: 0.490447
  ...
# Subtest: review queue line resolves at the entry line
ok 1839 - review queue line resolves at the entry line
  ---
  duration_ms: 0.593493
  ...
# Subtest: review queue line follows a moved line to its unique match
ok 1840 - review queue line follows a moved line to its unique match
  ---
  duration_ms: 0.416275
  ...
# Subtest: review queue line goes stale on duplicates or a missing line
ok 1841 - review queue line goes stale on duplicates or a missing line
  ---
  duration_ms: 0.210522
  ...
# Subtest: review jump notices name the state
ok 1842 - review jump notices name the state
  ---
  duration_ms: 0.419151
  ...
# Subtest: fresh stamp targets refuse closed and recurring tasks
ok 1843 - fresh stamp targets refuse closed and recurring tasks
  ---
  duration_ms: 0.646024
  ...
# Subtest: fresh stamp batch stamps every target and nothing else
ok 1844 - fresh stamp batch stamps every target and nothing else
  ---
  duration_ms: 0.707922
  ...
# Subtest: one refusal refuses the whole fresh stamp batch
ok 1845 - one refusal refuses the whole fresh stamp batch
  ---
  duration_ms: 0.439469
  ...
# Subtest: a throwing stamper refuses the fresh stamp batch
ok 1846 - a throwing stamper refuses the fresh stamp batch
  ---
  duration_ms: 0.163442
  ...
# Subtest: fresh stamp plus Work Log prepends only stamped Pending targets
ok 1847 - fresh stamp plus Work Log prepends only stamped Pending targets
  ---
  duration_ms: 1.325781
  ...
# Subtest: blank Work Log summary and stamp refusal never create a log marker
ok 1848 - blank Work Log summary and stamp refusal never create a log marker
  ---
  duration_ms: 0.292298
  ...
# Subtest: fresh stamp notices adjust the pre-write counts
ok 1849 - fresh stamp notices adjust the pre-write counts
  ---
  duration_ms: 0.228085
  ...
# Subtest: today detection only matches today's fresh field
ok 1850 - today detection only matches today's fresh field
  ---
  duration_ms: 0.190203
  ...
# Subtest: stamped refs match the pre-write queue by line or text
ok 1851 - stamped refs match the pre-write queue by line or text
  ---
  duration_ms: 0.426835
  ...
# Subtest: review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
ok 1852 - review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance
  ---
  duration_ms: 0.286167
  ...
# Subtest: tier-aware jump notices name each tier
ok 1853 - tier-aware jump notices name each tier
  ---
  duration_ms: 0.619904
  ...
# Subtest: projects tier walks with commitment rank and empty-project notice
ok 1854 - projects tier walks with commitment rank and empty-project notice
  ---
  duration_ms: 0.238085
  ...
# Subtest: references tier walks with commitment rank and reference notice
ok 1855 - references tier walks with commitment rank and reference notice
  ---
  duration_ms: 0.56548
  ...
# Subtest: jump notices use reviewEntryView when provided and keep the fallback
ok 1856 - jump notices use reviewEntryView when provided and keep the fallback
  ---
  duration_ms: 0.354357
  ...
# Subtest: tier notices fall back without tier ranks and wrap on the last line
ok 1857 - tier notices fall back without tier ranks and wrap on the last line
  ---
  duration_ms: 0.203419
  ...
# Subtest: boundary notice names commitments done and rotten next
ok 1858 - boundary notice names commitments done and rotten next
  ---
  duration_ms: 0.162881
  ...
# Subtest: walk anchor records handled keys with their neighbors
ok 1859 - walk anchor records handled keys with their neighbors
  ---
  duration_ms: 0.606178
  ...
# Subtest: cursor on a live entry wins over a lagging anchor
ok 1860 - cursor on a live entry wins over a lagging anchor
  ---
  duration_ms: 0.365448
  ...
# Subtest: [s after a stamp goes backwards from the anchor
ok 1861 - [s after a stamp goes backwards from the anchor
  ---
  duration_ms: 0.63394
  ...
# Subtest: release-then-]s continues from the anchor successor
ok 1862 - release-then-]s continues from the anchor successor
  ---
  duration_ms: 0.281117
  ...
# Subtest: non-contiguous counted stamp advances past the last handled rank
ok 1863 - non-contiguous counted stamp advances past the last handled rank
  ---
  duration_ms: 0.389093
  ...
# Subtest: anchor wraps at both ends
ok 1864 - anchor wraps at both ends
  ---
  duration_ms: 0.398932
  ...
# Subtest: advance across NEXT to TICKLER to ROTTEN lands the boundary
ok 1865 - advance across NEXT to TICKLER to ROTTEN lands the boundary
  ---
  duration_ms: 0.458716
  ...
# Subtest: tier capability gates on the freshness namespace version
ok 1866 - tier capability gates on the freshness namespace version
  ---
  duration_ms: 0.159725
  ...
# Subtest: empty queue notice reads the upkeep meter
ok 1867 - empty queue notice reads the upkeep meter
  ---
  duration_ms: 0.139977
  ...
# Subtest: refresh row reads lane intervals from the api with the once-Ready return
ok 1868 - refresh row reads lane intervals from the api with the once-Ready return
  ---
  duration_ms: 1.333707
  ...
# Subtest: endpoint jumps select the queue ends with full rank and total
ok 1869 - endpoint jumps select the queue ends with full rank and total
  ---
  duration_ms: 0.389604
  ...
# Subtest: endpoint jumps ignore cursor, anchor, and direction
ok 1870 - endpoint jumps ignore cursor, anchor, and direction
  ---
  duration_ms: 0.261901
  ...
# Subtest: endpoint jumps on empty and one-entry queues
ok 1871 - endpoint jumps on empty and one-entry queues
  ---
  duration_ms: 0.236822
  ...
# Subtest: a visited endpoint is still due under its own anchor
ok 1872 - a visited endpoint is still due under its own anchor
  ---
  duration_ms: 0.192207
  ...
# Subtest: lowercase steps continue from an endpoint anchor
ok 1873 - lowercase steps continue from an endpoint anchor
  ---
  duration_ms: 0.363244
  ...
# Subtest: counted review jump repeat 1 matches omitted repeat
ok 1874 - counted review jump repeat 1 matches omitted repeat
  ---
  duration_ms: 0.729463
  ...
# Subtest: counted review jump from the first entry lands N steps ahead
ok 1875 - counted review jump from the first entry lands N steps ahead
  ---
  duration_ms: 0.288641
  ...
# Subtest: counted review jump from the last entry wraps past the start
ok 1876 - counted review jump from the last entry wraps past the start
  ---
  duration_ms: 0.149957
  ...
# Subtest: counted review jump larger than the queue wraps once
ok 1877 - counted review jump larger than the queue wraps once
  ---
  duration_ms: 0.16738
  ...
# Subtest: counted review jump on a one-entry queue stays there
ok 1878 - counted review jump on a one-entry queue stays there
  ---
  duration_ms: 0.168922
  ...
# Subtest: counted review jump with no origin lands on the Nth entry
ok 1879 - counted review jump with no origin lands on the Nth entry
  ---
  duration_ms: 0.171177
  ...
# Subtest: counted review jump from a shaped anchor takes N surviving successors
ok 1880 - counted review jump from a shaped anchor takes N surviving successors
  ---
  duration_ms: 0.219098
  ...
# Subtest: counted review jump does not change endpoint selection
ok 1881 - counted review jump does not change endpoint selection
  ---
  duration_ms: 0.191977
  ...
# Subtest: a stamped endpoint that moved is stale and cannot land from old text
ok 1882 - a stamped endpoint that moved is stale and cannot land from old text
  ---
  duration_ms: 0.224719
  ...
# Subtest: stale endpoint target reselects the same endpoint in the new queue
ok 1883 - stale endpoint target reselects the same endpoint in the new queue
  ---
  duration_ms: 2.019045
  ...
# Subtest: endpoint retry is bounded and failures preserve the anchor
ok 1884 - endpoint retry is bounded and failures preserve the anchor
  ---
  duration_ms: 0.517678
  ...
# Subtest: endpoint jump to ROTTEN carries no boundary preamble
ok 1885 - endpoint jump to ROTTEN carries no boundary preamble
  ---
  duration_ms: 0.886613
  ...
# Subtest: endpoint notices keep v4 tier details and legacy v3 text
ok 1886 - endpoint notices keep v4 tier details and legacy v3 text
  ---
  duration_ms: 0.157591
  ...
# Subtest: onload registers first/last commands routed to the shared jump
ok 1887 - onload registers first/last commands routed to the shared jump
  ---
  duration_ms: 5.326523
  ...
# Subtest: jumpToDueTask consumes a pending Vim prefix as N review steps
ok 1888 - jumpToDueTask consumes a pending Vim prefix as N review steps
  ---
  duration_ms: 1.430352
  ...
# Subtest: registered next-due-task callback reads the pending Vim prefix
ok 1889 - registered next-due-task callback reads the pending Vim prefix
  ---
  duration_ms: 1.1305
  ...
# Subtest: explicit jumpToDueTask repeat skips the Vim prefix
ok 1890 - explicit jumpToDueTask repeat skips the Vim prefix
  ---
  duration_ms: 0.398561
  ...
# Subtest: non-normal editor with a pending prefix still jumps one entry
ok 1891 - non-normal editor with a pending prefix still jumps one entry
  ---
  duration_ms: 0.358805
  ...
# Subtest: stale counted replan reuses the captured repeat
ok 1892 - stale counted replan reuses the captured repeat
  ---
  duration_ms: 0.377501
  ...
# Subtest: endpoint jump with a pending prefix still lands on the endpoint
ok 1893 - endpoint jump with a pending prefix still lands on the endpoint
  ---
  duration_ms: 0.307297
  ...
# Subtest: counted forward landing on ROTTEN keeps the boundary preamble
ok 1894 - counted forward landing on ROTTEN keeps the boundary preamble
  ---
  duration_ms: 0.627127
  ...
# Subtest: PRE and POST are machine tiers; PRE is a commitment
ok 1895 - PRE and POST are machine tiers; PRE is a commitment
  ---
  duration_ms: 0.305063
  ...
# Subtest: fallback notices name PRE checklist and POST closeout
ok 1896 - fallback notices name PRE checklist and POST closeout
  ---
  duration_ms: 0.328527
  ...
# Subtest: text-first cursor matching does not skip Pills after an above-insert
ok 1897 - text-first cursor matching does not skip Pills after an above-insert
  ---
  duration_ms: 0.206294
  ...
# Subtest: day-scoped anchors from another day are ignored
ok 1898 - day-scoped anchors from another day are ignored
  ---
  duration_ms: 0.322505
  ...
# Subtest: boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
ok 1899 - boundary into ROTTEN appends ]S when POST remains; into POST names commitments done
  ---
  duration_ms: 0.26697
  ...
# Subtest: ]S reaches POST with 77 ROTTEN rows and a null budget
ok 1900 - ]S reaches POST with 77 ROTTEN rows and a null budget
  ---
  duration_ms: 0.845905
  ...
# Subtest: nav normalizes a legacy v7 returned tier to tickler
ok 1901 - nav normalizes a legacy v7 returned tier to tickler
  ---
  duration_ms: 0.145157
  ...
# Subtest: RECURRING is a machine tier, a commitment, and a v9 capability
ok 1902 - RECURRING is a machine tier, a commitment, and a v9 capability
  ---
  duration_ms: 0.178491
  ...
# Subtest: RECURRING counts in reviewWalkRemaining and gates the boundary
ok 1903 - RECURRING counts in reviewWalkRemaining and gates the boundary
  ---
  duration_ms: 0.197517
  ...
# Subtest: matchReviewRecurringCursor is text-first like the checklist matcher
ok 1904 - matchReviewRecurringCursor is text-first like the checklist matcher
  ---
  duration_ms: 0.226593
  ...
# Subtest: fallback notices name RECURRING due detail with the reschedule hint
ok 1905 - fallback notices name RECURRING due detail with the reschedule hint
  ---
  duration_ms: 0.199531
  ...
# Subtest: Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
ok 1906 - Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired
  ---
  duration_ms: 0.155698
  ...
# Subtest: bobLineDigest matches the shared bob-cli vectors
ok 1907 - bobLineDigest matches the shared bob-cli vectors
  ---
  duration_ms: 6.322844
  ...
# Subtest: parseGoToTaskParams accepts a complete v1 link and ignores extra keys
ok 1908 - parseGoToTaskParams accepts a complete v1 link and ignores extra keys
  ---
  duration_ms: 1.105381
  ...
# Subtest: parseGoToTaskParams treats ref and block as optional
ok 1909 - parseGoToTaskParams treats ref and block as optional
  ---
  duration_ms: 0.197457
  ...
# Subtest: parseGoToTaskParams rejects each malformed field
ok 1910 - parseGoToTaskParams rejects each malformed field
  ---
  duration_ms: 0.334719
  ...
# Subtest: vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
ok 1911 - vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base
  ---
  duration_ms: 0.399613
  ...
# Subtest: refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
ok 1912 - refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources
  ---
  duration_ms: 2.066767
  ...
# Subtest: handleGoToTaskUri notices each malformed parameter
ok 1913 - handleGoToTaskUri notices each malformed parameter
  ---
  duration_ms: 1.803604
  ...
# Subtest: handleGoToTaskUri notices a path outside the vault
ok 1914 - handleGoToTaskUri notices a path outside the vault
  ---
  duration_ms: 0.65966
  ...
# Subtest: handleGoToTaskUri notices a missing file inside the vault
ok 1915 - handleGoToTaskUri notices a missing file inside the vault
  ---
  duration_ms: 0.679538
  ...
# Subtest: handleGoToTaskUri maps a trailing-slash vault base
ok 1916 - handleGoToTaskUri maps a trailing-slash vault base
  ---
  duration_ms: 2.523418
  ...
# Subtest: handleGoToTaskUri prefers the open buffer over cachedRead
ok 1917 - handleGoToTaskUri prefers the open buffer over cachedRead
  ---
  duration_ms: 1.097276
  ...
# Subtest: handleGoToTaskUri re-finds by block id after an insert above the task
ok 1918 - handleGoToTaskUri re-finds by block id after an insert above the task
  ---
  duration_ms: 0.684507
  ...
# Subtest: handleGoToTaskUri re-finds a unique digest after a shift with no block
ok 1919 - handleGoToTaskUri re-finds a unique digest after a shift with no block
  ---
  duration_ms: 1.072478
  ...
# Subtest: handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
ok 1920 - handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice
  ---
  duration_ms: 0.559498
  ...
# Subtest: handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
ok 1921 - handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent
  ---
  duration_ms: 0.641936
  ...
# Subtest: handleGoToTaskUri reuses a leaf that already shows the note
ok 1922 - handleGoToTaskUri reuses a leaf that already shows the note
  ---
  duration_ms: 0.891613
  ...
# Subtest: handleGoToTaskUri switches a Reading-view leaf to editing
ok 1923 - handleGoToTaskUri switches a Reading-view leaf to editing
  ---
  duration_ms: 0.816139
  ...
# Subtest: handleGoToTaskUri records a jump from the prior cursor and none without one
ok 1924 - handleGoToTaskUri records a jump from the prior cursor and none without one
  ---
  duration_ms: 1.176056
  ...
# Subtest: handleGoToTaskUri never writes the vault or advances the walk
ok 1925 - handleGoToTaskUri never writes the vault or advances the walk
  ---
  duration_ms: 0.539541
  ...
# Subtest: handleGoToTaskUri reports when the note cannot be opened
ok 1926 - handleGoToTaskUri reports when the note cannot be opened
  ---
  duration_ms: 0.500255
  ...
# Subtest: focusTaskMoveDestination still lands without switching Reading view
ok 1927 - focusTaskMoveDestination still lands without switching Reading view
  ---
  duration_ms: 0.537537
  ...
# Subtest: onload registers both read-only navigation protocols when available
ok 1928 - onload registers both read-only navigation protocols when available
  ---
  duration_ms: 1.777504
  ...
# Subtest: onload skips protocol registration when the API is missing
ok 1929 - onload skips protocol registration when the API is missing
  ---
  duration_ms: 0.483734
  ...
# Subtest: registered protocol handler forwards params to handleGoToTaskUri
ok 1930 - registered protocol handler forwards params to handleGoToTaskUri
  ---
  duration_ms: 0.463776
  ...
# Subtest: handleGoToTaskUri maps a path through realpath when prefixes differ
ok 1931 - handleGoToTaskUri maps a path through realpath when prefixes differ
  ---
  duration_ms: 3.643287
  ...
# Subtest: cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
ok 1932 - cancel log grammar recognizes the marker, FE0F, and emoji-less spellings
  ---
  duration_ms: 2.719433
  ...
# Subtest: findCancelLogParent finds a direct child but ignores a grandchild
ok 1933 - findCancelLogParent finds a direct child but ignores a grandchild
  ---
  duration_ms: 0.652125
  ...
# Subtest: getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
ok 1934 - getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab
  ---
  duration_ms: 0.214519
  ...
# Subtest: formatCancelLogEntryText renders the exact preview text
ok 1935 - formatCancelLogEntryText renders the exact preview text
  ---
  duration_ms: 0.164835
  ...
# Subtest: planCancelLogEntry inserts a first-child log with tabs or spaces
ok 1936 - planCancelLogEntry inserts a first-child log with tabs or spaces
  ---
  duration_ms: 0.760954
  ...
# Subtest: planCancelLogEntry prepends under an existing log wherever it sits
ok 1937 - planCancelLogEntry prepends under an existing log wherever it sits
  ---
  duration_ms: 0.286467
  ...
# Subtest: planCancelLogEntry uses the fallback only when a marker exists
ok 1938 - planCancelLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.349868
  ...
# Subtest: isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
ok 1939 - isRecurringTaskLine and getTaskCancelStatusLabel cover the contract
  ---
  duration_ms: 0.30362
  ...
# Subtest: describeCancelTaskRow covers single, counted, link, recurring, and hidden
ok 1940 - describeCancelTaskRow covers single, counted, link, recurring, and hidden
  ---
  duration_ms: 1.991674
  ...
# Subtest: planTaskCancelBatch cancels a single task with a first-child log
ok 1941 - planTaskCancelBatch cancels a single task with a first-child log
  ---
  duration_ms: 1.841457
  ...
# Subtest: planTaskCancelBatch upserts cancelled before the block id and preserves fields
ok 1942 - planTaskCancelBatch upserts cancelled before the block id and preserves fields
  ---
  duration_ms: 0.456562
  ...
# Subtest: planTaskCancelBatch records id-field task identities
ok 1943 - planTaskCancelBatch records id-field task identities
  ---
  duration_ms: 0.259265
  ...
# Subtest: planTaskCancelBatch skips closed targets and stays bottom-up
ok 1944 - planTaskCancelBatch skips closed targets and stays bottom-up
  ---
  duration_ms: 0.412017
  ...
# Subtest: planTaskCancelBatch refuses recurring targets in all three syntaxes
ok 1945 - planTaskCancelBatch refuses recurring targets in all three syntaxes
  ---
  duration_ms: 0.457634
  ...
# Subtest: planTaskCancelBatch handles empty reasons and stale preimages
ok 1946 - planTaskCancelBatch handles empty reasons and stale preimages
  ---
  duration_ms: 0.389303
  ...
# Subtest: planTaskCancelBatch preserves CRLF line endings
ok 1947 - planTaskCancelBatch preserves CRLF line endings
  ---
  duration_ms: 0.260918
  ...
# Subtest: cancel project conversion carries the log and reports it
ok 1948 - cancel project conversion carries the log and reports it
  ---
  duration_ms: 3.792241
  ...
# Subtest: getCancelTaskRowTitle names single, counted, and link sessions
ok 1949 - getCancelTaskRowTitle names single, counted, and link sessions
  ---
  duration_ms: 1.143243
  ...
# Subtest: getCancelReasonHints labels Enter per state and Esc as Keep open
ok 1950 - getCancelReasonHints labels Enter per state and Esc as Keep open
  ---
  duration_ms: 0.930527
  ...
# Subtest: the Cancel property item and the card's cancel row describe an open task
ok 1951 - the Cancel property item and the card's cancel row describe an open task
  ---
  duration_ms: 13.481013
  ...
# Subtest: Cancel row hides on closed tasks, plain bullets, and all-closed sessions
ok 1952 - Cancel row hides on closed tasks, plain bullets, and all-closed sessions
  ---
  duration_ms: 6.900729
  ...
# Subtest: Cancel row reports skipped closed targets in a counted session
ok 1953 - Cancel row reports skipped closed targets in a counted session
  ---
  duration_ms: 1.713994
  ...
# Subtest: the card refuses the cancel row on a recurring task and stays on the card
ok 1954 - the card refuses the cancel row on a recurring task and stays on the card
  ---
  duration_ms: 2.672725
  ...
# Subtest: cancel reason stage previews the typed, empty, fallback, and :: cases
ok 1955 - cancel reason stage previews the typed, empty, fallback, and :: cases
  ---
  duration_ms: 3.573223
  ...
# Subtest: cancel reason footer flips between plain, log, and fallback labels
ok 1956 - cancel reason footer flips between plain, log, and fallback labels
  ---
  duration_ms: 6.678143
  ...
# Subtest: Esc from the cancel reason stage writes nothing
ok 1957 - Esc from the cancel reason stage writes nothing
  ---
  duration_ms: 3.924734
  ...
# Subtest: single cancel writes [-], stamp, and first-child log in one transaction
ok 1958 - single cancel writes [-], stamp, and first-child log in one transaction
  ---
  duration_ms: 6.018332
  ...
# Subtest: empty reason writes no log unless one already exists
ok 1959 - empty reason writes no log unless one already exists
  ---
  duration_ms: 5.119227
  ...
# Subtest: stale single preimage refuses with nothing written
ok 1960 - stale single preimage refuses with nothing written
  ---
  duration_ms: 1.34557
  ...
# Subtest: cancel writes [-] with no NOW chip
ok 1961 - cancel writes [-] with no NOW chip
  ---
  duration_ms: 1.543888
  ...
# Subtest: TSC recovery runs with cancelled identities; a missing API still succeeds
ok 1962 - TSC recovery runs with cancelled identities; a missing API still succeeds
  ---
  duration_ms: 8.015808
  ...
# Subtest: a throwing TSC API is skipped silently with no chip
ok 1963 - a throwing TSC API is skipped silently with no chip
  ---
  duration_ms: 3.020037
  ...
# Subtest: counted cancel skips closed targets and reports them
ok 1964 - counted cancel skips closed targets and reports them
  ---
  duration_ms: 3.28328
  ...
# Subtest: same-file cancel folds today's Pomodoro prune into one transaction
ok 1965 - same-file cancel folds today's Pomodoro prune into one transaction
  ---
  duration_ms: 5.093497
  ...
# Subtest: link session cancels the target and removes the invoking link bullet
ok 1966 - link session cancels the target and removes the invoking link bullet
  ---
  duration_ms: 8.921388
  ...
# Subtest: buildCancelNoticeModel text covers every chip
ok 1967 - buildCancelNoticeModel text covers every chip
  ---
  duration_ms: 0.420022
  ...
# Subtest: renderCancelNoticeFragment builds the is-cancel card
ok 1968 - renderCancelNoticeFragment builds the is-cancel card
  ---
  duration_ms: 1.009859
  ...
# Subtest: Ctrl+0 loads and focuses a deferred pinned dash tab without jumping or restoring
ok 1969 - Ctrl+0 loads and focuses a deferred pinned dash tab without jumping or restoring
  ---
  duration_ms: 4.112673
  ...
# Subtest: Ctrl+0 from an unpinned dash copy switches to the pinned home tab
ok 1970 - Ctrl+0 from an unpinned dash copy switches to the pinned home tab
  ---
  duration_ms: 0.578585
  ...
# Subtest: Ctrl+0 stays on the pinned dash tab when an unpinned copy exists
ok 1971 - Ctrl+0 stays on the pinned dash tab when an unpinned copy exists
  ---
  duration_ms: 0.30398
  ...
# Subtest: Ctrl+0 keeps the active dash tab when equal-ranked copies exist
ok 1972 - Ctrl+0 keeps the active dash tab when equal-ranked copies exist
  ---
  duration_ms: 0.318849
  ...
# Subtest: a pinned dash tab wins over an earlier unpinned tab
ok 1973 - a pinned dash tab wins over an earlier unpinned tab
  ---
  duration_ms: 0.38232
  ...
# Subtest: a main-area dash tab wins over a pinned sidebar tab
ok 1974 - a main-area dash tab wins over a pinned sidebar tab
  ---
  duration_ms: 0.25143
  ...
# Subtest: a deferred sidebar dash tab is reused when there is no main-area match
ok 1975 - a deferred sidebar dash tab is reused when there is no main-area match
  ---
  duration_ms: 0.360528
  ...
# Subtest: a markdown saved state is considered even when the leaf is not deferred
ok 1976 - a markdown saved state is considered even when the leaf is not deferred
  ---
  duration_ms: 0.253995
  ...
# Subtest: Ctrl+0 opens dash in the current tab when no matching tab exists
ok 1977 - Ctrl+0 opens dash in the current tab when no matching tab exists
  ---
  duration_ms: 0.651985
  ...
# Subtest: Ctrl+0 leaves an already active dash tab alone
ok 1978 - Ctrl+0 leaves an already active dash tab alone
  ---
  duration_ms: 0.647586
  ...
# Subtest: isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
ok 1979 - isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines
  ---
  duration_ms: 1.629982
  ...
# Subtest: findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
ok 1980 - findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading
  ---
  duration_ms: 1.77509
  ...
# Subtest: collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
ok 1981 - collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs
  ---
  duration_ms: 0.665851
  ...
# Subtest: planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
ok 1982 - planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed
  ---
  duration_ms: 1.234097
  ...
# Subtest: planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
ok 1983 - planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched
  ---
  duration_ms: 1.137662
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
ok 1984 - planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children
  ---
  duration_ms: 1.166397
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
ok 1985 - planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links
  ---
  duration_ms: 0.792103
  ...
# Subtest: planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
ok 1986 - planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses
  ---
  duration_ms: 0.295554
  ...
# Subtest: planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
ok 1987 - planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing
  ---
  duration_ms: 0.93197
  ...
# Subtest: planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
ok 1988 - planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion
  ---
  duration_ms: 0.901612
  ...
# Subtest: planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
ok 1989 - planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code
  ---
  duration_ms: 0.758138
  ...
# Subtest: planDeferredPomodoroLinkCleanup preserves CRLF line endings
ok 1990 - planDeferredPomodoroLinkCleanup preserves CRLF line endings
  ---
  duration_ms: 0.3719
  ...
# Subtest: deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
ok 1991 - deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none
  ---
  duration_ms: 0.396057
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks\#^x]] \#
ok 1992 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks\#^x]] \#
  ---
  duration_ms: 0.362813
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks\#^x|alias]] \#
ok 1993 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks\#^x|alias]] \#
  ---
  duration_ms: 0.266409
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks\#^x]]
ok 1994 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks\#^x]]
  ---
  duration_ms: 0.270436
  ...
# Subtest: cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks\#^x]]
ok 1995 - cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks\#^x]]
  ---
  duration_ms: 0.21464
  ...
# Subtest: dedicated decoration check accepts paired strikes but cleanup never removes struck links
ok 1996 - dedicated decoration check accepts paired strikes but cleanup never removes struck links
  ---
  duration_ms: 0.448397
  ...
# Subtest: cleanup deletes only touched childless entries, preserving prose, placeholders and closed history
ok 1997 - cleanup deletes only touched childless entries, preserving prose, placeholders and closed history
  ---
  duration_ms: 0.4556
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\n", final newline false)
ok 1998 - cleanup handles adjacent EOF entries ("\\n", final newline false)
  ---
  duration_ms: 0.299452
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\n", final newline true)
ok 1999 - cleanup handles adjacent EOF entries ("\\n", final newline true)
  ---
  duration_ms: 0.279814
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\r\\n", final newline false)
ok 2000 - cleanup handles adjacent EOF entries ("\\r\\n", final newline false)
  ---
  duration_ms: 0.236802
  ...
# Subtest: cleanup handles adjacent EOF entries ("\\r\\n", final newline true)
ok 2001 - cleanup handles adjacent EOF entries ("\\r\\n", final newline true)
  ---
  duration_ms: 0.252883
  ...
# Subtest: counted dependencies converge mixed sources and maintain one link per parent
ok 2002 - counted dependencies converge mixed sources and maintain one link per parent
  ---
  duration_ms: 12.291525
  ...
# Subtest: counted and single dependency gestures refuse inside a blockquote (DP29)
ok 2003 - counted and single dependency gestures refuse inside a blockquote (DP29)
  ---
  duration_ms: 0.471471
  ...
# Subtest: counted dependency candidates exclude every source and expose mixed state
ok 2004 - counted dependency candidates exclude every source and expose mixed state
  ---
  duration_ms: 0.972317
  ...
# Subtest: counted dependency block-ID prompting is planned atomically
ok 2005 - counted dependency block-ID prompting is planned atomically
  ---
  duration_ms: 2.133965
  ...
# Subtest: counted dependency runtime applies target, parents, and navigation in one undo group
ok 2006 - counted dependency runtime applies target, parents, and navigation in one undo group
  ---
  duration_ms: 6.829602
  ...
# Subtest: counted Depends-on removal recovers residents with [unblocked::]
ok 2007 - counted Depends-on removal recovers residents with [unblocked::]
  ---
  duration_ms: 4.518077
  ...
# Subtest: counted Depends-on removal writes [unblocked::] through the wired freshness API
ok 2008 - counted Depends-on removal writes [unblocked::] through the wired freshness API
  ---
  duration_ms: 6.965935
  ...
# Subtest: cross-file toggle changes only the source link
ok 2009 - cross-file toggle changes only the source link
  ---
  duration_ms: 1.959953
  ...
# Subtest: cross-file write failure still toggles only the source link
ok 2010 - cross-file write failure still toggles only the source link
  ---
  duration_ms: 0.694827
  ...
# Subtest: line-local fallback applies bottom-up and preserves CRLF
ok 2011 - line-local fallback applies bottom-up and preserves CRLF
  ---
  duration_ms: 0.836477
  ...
# Subtest: source line-count invariant rejects embedded newline changes
ok 2012 - source line-count invariant rejects embedded newline changes
  ---
  duration_ms: 0.227625
  ...
# Subtest: pure toggle refuses when the source changed under it
ok 2013 - pure toggle refuses when the source changed under it
  ---
  duration_ms: 0.150137
  ...
# Subtest: counted transclusion toggle evaluates each line independently
ok 2014 - counted transclusion toggle evaluates each line independently
  ---
  duration_ms: 0.402498
  ...
# Subtest: transclusion toggle is refused on Depends-On lines
ok 2015 - transclusion toggle is refused on Depends-On lines
  ---
  duration_ms: 0.513591
  ...
# Subtest: transclusion toggles refuse generated BLOCKS lines with their notice
ok 2016 - transclusion toggles refuse generated BLOCKS lines with their notice
  ---
  duration_ms: 0.733821
  ...
# Subtest: legacy sole-link children toggle purely, without field or status writes
ok 2017 - legacy sole-link children toggle purely, without field or status writes
  ---
  duration_ms: 0.619493
  ...
# Subtest: Ctrl+D on the Depends on row clears the line, field, and legacy children
ok 2018 - Ctrl+D on the Depends on row clears the line, field, and legacy children
  ---
  duration_ms: 4.28911
  ...
# Subtest: Ctrl+D clears a field-only dependency without a line
ok 2019 - Ctrl+D clears a field-only dependency without a line
  ---
  duration_ms: 1.771663
  ...
# Subtest: counted Ctrl+D on the Depends on row clears every targeted task
ok 2020 - counted Ctrl+D on the Depends on row clears every targeted task
  ---
  duration_ms: 4.103736
  ...
# Subtest: findRemovedLineText reports deleted lines
ok 2021 - findRemovedLineText reports deleted lines
  ---
  duration_ms: 0.271759
  ...
# Subtest: hand-edit mirror projects an edited line into the field
ok 2022 - hand-edit mirror projects an edited line into the field
  ---
  duration_ms: 2.39321
  ...
# Subtest: hand-edit mirror canonicalises a hand-written line variant
ok 2023 - hand-edit mirror canonicalises a hand-written line variant
  ---
  duration_ms: 1.022392
  ...
# Subtest: hand-edit mirror drops a linkless line and the field
ok 2024 - hand-edit mirror drops a linkless line and the field
  ---
  duration_ms: 1.281728
  ...
# Subtest: hand-edit mirror clears the field after the line is deleted
ok 2025 - hand-edit mirror clears the field after the line is deleted
  ---
  duration_ms: 1.177899
  ...
# Subtest: hand-edit mirror leaves malformed lines alone
ok 2026 - hand-edit mirror leaves malformed lines alone
  ---
  duration_ms: 0.330461
  ...
# Subtest: hand-edit mirror leaves legacy-only children for the hooks
ok 2027 - hand-edit mirror leaves legacy-only children for the hooks
  ---
  duration_ms: 0.419962
  ...
# Subtest: hand-edit mirror blocks when an open prerequisite is added by hand
ok 2028 - hand-edit mirror blocks when an open prerequisite is added by hand
  ---
  duration_ms: 0.955976
  ...
# Subtest: hand-edit mirror never transfers commitment to the target
ok 2029 - hand-edit mirror never transfers commitment to the target
  ---
  duration_ms: 1.006532
  ...
# Subtest: hand-edit mirror recovers when the last open prerequisite is removed by hand
ok 2030 - hand-edit mirror recovers when the last open prerequisite is removed by hand
  ---
  duration_ms: 1.159194
  ...
# Subtest: hand-edit mirror leaves a half-typed link alone
ok 2031 - hand-edit mirror leaves a half-typed link alone
  ---
  duration_ms: 0.34556
  ...
# Subtest: hand-edit mirror clears the owning task when its last-child line is deleted
ok 2032 - hand-edit mirror clears the owning task when its last-child line is deleted
  ---
  duration_ms: 1.037121
  ...
# Subtest: counted add below a prerequisite follows BLOCKS shifts (bob-cli-95)
ok 2033 - counted add below a prerequisite follows BLOCKS shifts (bob-cli-95)
  ---
  duration_ms: 5.930186
  ...
# Subtest: counted remove follows BLOCKS deletions above the sources
ok 2034 - counted remove follows BLOCKS deletions above the sources
  ---
  duration_ms: 1.842338
  ...
# Subtest: counted runtime commits once with the mapped first-source cursor
ok 2035 - counted runtime commits once with the mapped first-source cursor
  ---
  duration_ms: 1.960835
  ...
# Subtest: mirror scheduler debounces at the contract interval
ok 2036 - mirror scheduler debounces at the contract interval
  ---
  duration_ms: 1.379083
  ...
# Subtest: mirror scheduler seeds the baseline from the update start state
ok 2037 - mirror scheduler seeds the baseline from the update start state
  ---
  duration_ms: 2.203538
  ...
# Subtest: mirror scheduler keeps the first baseline and maps the owner across a burst
ok 2038 - mirror scheduler keeps the first baseline and maps the owner across a burst
  ---
  duration_ms: 0.662475
  ...
# Subtest: mirror listener runs clear-field for a first-edit deletion with a following sibling
ok 2039 - mirror listener runs clear-field for a first-edit deletion with a following sibling
  ---
  duration_ms: 16.71907
  ...
# Subtest: mirror fire re-arms while the cursor stays on the edited line
ok 2040 - mirror fire re-arms while the cursor stays on the edited line
  ---
  duration_ms: 3.077868
  ...
# Subtest: mirror scheduler reads changed ranges from the CM6 update
ok 2041 - mirror scheduler reads changed ranges from the CM6 update
  ---
  duration_ms: 0.32488
  ...
# Subtest: mirror scheduler skips IME composition
ok 2042 - mirror scheduler skips IME composition
  ---
  duration_ms: 0.235499
  ...
# Subtest: mirror scheduler skips open modals
ok 2043 - mirror scheduler skips open modals
  ---
  duration_ms: 0.217455
  ...
# Subtest: counted Ctrl+D clears every targeted task in one transaction with one notice
ok 2044 - counted Ctrl+D clears every targeted task in one transaction with one notice
  ---
  duration_ms: 5.47275
  ...
# Subtest: counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
ok 2045 - counted N! refuses Depends-On lines with the Ctrl+Shift+P notice
  ---
  duration_ms: 2.032772
  ...
# Subtest: counted N! on only a Depends-On line refuses without writing
ok 2046 - counted N! on only a Depends-On line refuses without writing
  ---
  duration_ms: 0.375237
  ...
# Subtest: promotion targets enumerate real tasks and assign stable IDs
ok 2047 - promotion targets enumerate real tasks and assign stable IDs
  ---
  duration_ms: 5.41352
  ...
# Subtest: promotion file planner expands live links and preserves history
ok 2048 - promotion file planner expands live links and preserves history
  ---
  duration_ms: 5.800747
  ...
# Subtest: promotion file planner handles forms, whitespace, and subtrees
ok 2049 - promotion file planner handles forms, whitespace, and subtrees
  ---
  duration_ms: 1.109799
  ...
# Subtest: promotion file planner keeps compatibility for non-live references
ok 2050 - promotion file planner keeps compatibility for non-live references
  ---
  duration_ms: 1.087797
  ...
# Subtest: forward promotion expands live links, persists anchors, and removes the source
ok 2051 - forward promotion expands live links, persists anchors, and removes the source
  ---
  duration_ms: 9.814641
  ...
# Subtest: forward promotion preserves a concurrent frontmatter write before anchoring
ok 2052 - forward promotion preserves a concurrent frontmatter write before anchoring
  ---
  duration_ms: 1.488232
  ...
# Subtest: forward promotion rebases anchors in an open project editor
ok 2053 - forward promotion rebases anchors in an open project editor
  ---
  duration_ms: 2.286076
  ...
# Subtest: forward promotion refuses a concurrent edit to a task line being anchored
ok 2054 - forward promotion refuses a concurrent edit to a task line being anchored
  ---
  duration_ms: 1.507238
  ...
# Subtest: forward promotion uses zero-task fallback and keeps reverse one-to-one
ok 2055 - forward promotion uses zero-task fallback and keeps reverse one-to-one
  ---
  duration_ms: 1.345049
  ...
# Subtest: forward promotion retains the source on ambiguous, stale, and write failures
ok 2056 - forward promotion retains the source on ambiguous, stale, and write failures
  ---
  duration_ms: 2.07299
  ...
# Subtest: forward promotion discovers live links without a backlink cache and uses one open-editor write
ok 2057 - forward promotion discovers live links without a backlink cache and uses one open-editor write
  ---
  duration_ms: 1.85339
  ...
# Subtest: forward conversion carries a Depends-On line and reverse restores it
ok 2058 - forward conversion carries a Depends-On line and reverse restores it
  ---
  duration_ms: 22.938374
  ...
# Subtest: reverse conversion re-keys a cross-note prerequisite BLOCKS link
ok 2059 - reverse conversion re-keys a cross-note prerequisite BLOCKS link
  ---
  duration_ms: 6.797283
  ...
# Subtest: planTaskLaneBatch commits every Ready target to Next
ok 2060 - planTaskLaneBatch commits every Ready target to Next
  ---
  duration_ms: 3.204219
  ...
# Subtest: planTaskLaneBatch releases Next and In Progress to Ready
ok 2061 - planTaskLaneBatch releases Next and In Progress to Ready
  ---
  duration_ms: 0.61264
  ...
# Subtest: planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
ok 2062 - planTaskLaneBatch logs a nonblank summary on released In Progress tasks only
  ---
  duration_ms: 1.01595
  ...
# Subtest: planTaskLaneBatch skips Blocked and refuses stale preimages
ok 2063 - planTaskLaneBatch skips Blocked and refuses stale preimages
  ---
  duration_ms: 0.374255
  ...
# Subtest: buildLaneToggleNotice reports commit and release with and without budgets
ok 2064 - buildLaneToggleNotice reports commit and release with and without budgets
  ---
  duration_ms: 0.458796
  ...
# Subtest: describeLaneRow covers task, counted, and link sessions
ok 2065 - describeLaneRow covers task, counted, and link sessions
  ---
  duration_ms: 0.521776
  ...
# Subtest: toggleTaskLane commits Ready to Next and reports lane budgets
ok 2066 - toggleTaskLane commits Ready to Next and reports lane budgets
  ---
  duration_ms: 3.275476
  ...
# Subtest: toggleTaskLane releases to Ready without the api
ok 2067 - toggleTaskLane releases to Ready without the api
  ---
  duration_ms: 1.112154
  ...
# Subtest: toggleTaskLane release logs the summary on In Progress tasks
ok 2068 - toggleTaskLane release logs the summary on In Progress tasks
  ---
  duration_ms: 1.314831
  ...
# Subtest: toggleTaskLane skips Blocked targets
ok 2069 - toggleTaskLane skips Blocked targets
  ---
  duration_ms: 0.89505
  ...
# Subtest: counted toggleTaskLane covers the current task plus the next N tasks
ok 2070 - counted toggleTaskLane covers the current task plus the next N tasks
  ---
  duration_ms: 0.578054
  ...
# Subtest: toggleTaskLane on a Task Link writes through the open buffer
ok 2071 - toggleTaskLane on a Task Link writes through the open buffer
  ---
  duration_ms: 3.780409
  ...
# Subtest: toggleTaskLane on Task Links releases across notes
ok 2072 - toggleTaskLane on Task Links releases across notes
  ---
  duration_ms: 1.179072
  ...
# Subtest: toggleTaskLane refuses when a preimage changed
ok 2073 - toggleTaskLane refuses when a preimage changed
  ---
  duration_ms: 0.248916
  ...
# Subtest: Ctrl+Shift+P shows a pinned lane row that commits immediately
ok 2074 - Ctrl+Shift+P shows a pinned lane row that commits immediately
  ---
  duration_ms: 12.673751
  ...
# Subtest: Ctrl+Shift+P link mode shows the lane row with release detail
ok 2075 - Ctrl+Shift+P link mode shows the lane row with release detail
  ---
  duration_ms: 4.93806
  ...
# Subtest: Ctrl+Shift+P lane release with In Progress goes through the reason stage
ok 2076 - Ctrl+Shift+P lane release with In Progress goes through the reason stage
  ---
  duration_ms: 5.615885
  ...
# Subtest: getLinkPickerSessionSubtitle keeps the clamp for a single link
ok 2077 - getLinkPickerSessionSubtitle keeps the clamp for a single link
  ---
  duration_ms: 0.221463
  ...
# Subtest: link-mode priority notice keeps via Task Links visible
ok 2078 - link-mode priority notice keeps via Task Links visible
  ---
  duration_ms: 0.994129
  ...
# Subtest: already-handled Alt+N leaves Vim state alone
ok 2079 - already-handled Alt+N leaves Vim state alone
  ---
  duration_ms: 0.442385
  ...
# Subtest: Alt+N fallback still dispatches once with the Vim count
ok 2080 - Alt+N fallback still dispatches once with the Vim count
  ---
  duration_ms: 0.968129
  ...
# Subtest: lane release deletes an emptied entry (cross-file, Alt+N)
ok 2081 - lane release deletes an emptied entry (cross-file, Alt+N)
  ---
  duration_ms: 2.80133
  ...
# Subtest: lane release deletes an emptied entry (cross-file, card)
ok 2082 - lane release deletes an emptied entry (cross-file, card)
  ---
  duration_ms: 2.689015
  ...
# Subtest: lane release deletes an emptied entry (same-file, Alt+N)
ok 2083 - lane release deletes an emptied entry (same-file, Alt+N)
  ---
  duration_ms: 0.881323
  ...
# Subtest: lane release deletes an emptied entry (same-file, card)
ok 2084 - lane release deletes an emptied entry (same-file, card)
  ---
  duration_ms: 2.872034
  ...
# Subtest: Task Link release deletes its entry in one undo group (separate, Alt+N)
ok 2085 - Task Link release deletes its entry in one undo group (separate, Alt+N)
  ---
  duration_ms: 1.411205
  ...
# Subtest: Task Link release deletes its entry in one undo group (separate, card)
ok 2086 - Task Link release deletes its entry in one undo group (separate, card)
  ---
  duration_ms: 2.630874
  ...
# Subtest: Task Link release deletes its entry in one undo group (folded, Alt+N)
ok 2087 - Task Link release deletes its entry in one undo group (folded, Alt+N)
  ---
  duration_ms: 0.887164
  ...
# Subtest: Task Link release deletes its entry in one undo group (folded, card)
ok 2088 - Task Link release deletes its entry in one undo group (folded, card)
  ---
  duration_ms: 6.679344
  ...
# Subtest: parseLinkPickerTaskLink recognizes dedicated Task Link bullets
ok 2089 - parseLinkPickerTaskLink recognizes dedicated Task Link bullets
  ---
  duration_ms: 2.088139
  ...
# Subtest: discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
ok 2090 - discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end
  ---
  duration_ms: 1.091976
  ...
# Subtest: discoverLinkPickerTargets leaves \#task lines to the regular picker
ok 2091 - discoverLinkPickerTargets leaves \#task lines to the regular picker
  ---
  duration_ms: 0.353565
  ...
# Subtest: findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
ok 2092 - findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets
  ---
  duration_ms: 0.484105
  ...
# Subtest: createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
ok 2093 - createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values
  ---
  duration_ms: 1.728731
  ...
# Subtest: getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
ok 2094 - getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles
  ---
  duration_ms: 0.606628
  ...
# Subtest: bare link mode edits the task behind a Task Link through the open buffer
ok 2095 - bare link mode edits the task behind a Task Link through the open buffer
  ---
  duration_ms: 16.029119
  ...
# Subtest: counted link mode writes across notes through both the open buffer and the vault
ok 2096 - counted link mode writes across notes through both the open buffer and the vault
  ---
  duration_ms: 4.776101
  ...
# Subtest: Task Link scheduled delete recovers a Blocked task through the wired freshness API
ok 2097 - Task Link scheduled delete recovers a Blocked task through the wired freshness API
  ---
  duration_ms: 7.496208
  ...
# Subtest: link mode refuses the whole operation when a linked note changed
ok 2098 - link mode refuses the whole operation when a linked note changed
  ---
  duration_ms: 3.651453
  ...
# Subtest: link mode reports a closed target and changes nothing
ok 2099 - link mode reports a closed target and changes nothing
  ---
  duration_ms: 1.674929
  ...
# Subtest: link mode defers to a future date, blocks the task, and prunes today
ok 2100 - link mode defers to a future date, blocks the task, and prunes today
  ---
  duration_ms: 10.677479
  ...
# Subtest: bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
ok 2101 - bare Ctrl+Shift+P on a \#task line keeps the existing task behavior
  ---
  duration_ms: 4.434358
  ...
# Subtest: Task Link scheduled write deletes its entry (separate)
ok 2102 - Task Link scheduled write deletes its entry (separate)
  ---
  duration_ms: 8.554398
  ...
# Subtest: Task Link scheduled write deletes its entry (folded)
ok 2103 - Task Link scheduled write deletes its entry (folded)
  ---
  duration_ms: 6.044242
  ...
# Subtest: folded Task Link scheduling maps the cursor past logs inserted before the emptied entry
ok 2104 - folded Task Link scheduling maps the cursor past logs inserted before the emptied entry
  ---
  duration_ms: 5.030606
  ...
# Subtest: dash restore suppresses editor notice after deliberate navigation
ok 2105 - dash restore suppresses editor notice after deliberate navigation
  ---
  duration_ms: 22.754104
  ...
# Subtest: open-task dispatch timeout is registered for plugin cleanup
ok 2106 - open-task dispatch timeout is registered for plugin cleanup
  ---
  duration_ms: 1.095102
  ...
# Subtest: jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
ok 2107 - jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination
  ---
  duration_ms: 6.255435
  ...
# Subtest: jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
ok 2108 - jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group
  ---
  duration_ms: 1.642957
  ...
# Subtest: jumpToOpenObsidianTask keeps current-swap transaction failures local
ok 2109 - jumpToOpenObsidianTask keeps current-swap transaction failures local
  ---
  duration_ms: 0.872457
  ...
# Subtest: jumpToOpenObsidianTask refuses current-up without jumping or mutating
ok 2110 - jumpToOpenObsidianTask refuses current-up without jumping or mutating
  ---
  duration_ms: 0.564668
  ...
# Subtest: jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
ok 2111 - jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line
  ---
  duration_ms: 2.795378
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
ok 2112 - Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press
  ---
  duration_ms: 1.158482
  ...
# Subtest: Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
ok 2113 - Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press
  ---
  duration_ms: 1.088108
  ...
# Subtest: counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
ok 2114 - counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group
  ---
  duration_ms: 1.397419
  ...
# Subtest: an impossible counted Pomodoro move refuses without jumping or mutating
ok 2115 - an impossible counted Pomodoro move refuses without jumping or mutating
  ---
  duration_ms: 0.59167
  ...
# Subtest: counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
ok 2116 - counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts
  ---
  duration_ms: 0.910589
  ...
# Subtest: counted open-task jump on a sole current target keeps the existing notice
ok 2117 - counted open-task jump on a sole current target keeps the existing notice
  ---
  duration_ms: 0.228467
  ...
# Subtest: dispatch guard allows exactly one counted Pomodoro move when the command route also fires
ok 2118 - dispatch guard allows exactly one counted Pomodoro move when the command route also fires
  ---
  duration_ms: 0.935317
  ...
# Subtest: bullet property picker reconciles duplicate bare and counted opens
ok 2119 - bullet property picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 23.193171
  ...
# Subtest: bullet property picker close lifecycle clears tracking for fresh sessions
ok 2120 - bullet property picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 13.277719
  ...
# Subtest: task move picker reconciles duplicate bare and counted opens
ok 2121 - task move picker reconciles duplicate bare and counted opens
  ---
  duration_ms: 9.779395
  ...
# Subtest: task move picker close lifecycle clears tracking for fresh sessions
ok 2122 - task move picker close lifecycle clears tracking for fresh sessions
  ---
  duration_ms: 1.721417
  ...
# Subtest: Pomodoro bullet move picker opens sessions and clears the shared move picker slot
ok 2123 - Pomodoro bullet move picker opens sessions and clears the shared move picker slot
  ---
  duration_ms: 8.194399
  ...
# Subtest: Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
ok 2124 - Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries
  ---
  duration_ms: 0.850925
  ...
# Subtest: move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
ok 2125 - move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher
  ---
  duration_ms: 1.424531
  ...
# Subtest: commitPomodoroBulletMoveSession applies one guarded same-file transaction
ok 2126 - commitPomodoroBulletMoveSession applies one guarded same-file transaction
  ---
  duration_ms: 2.47625
  ...
# Subtest: Pomodoro bullet move picker confirms = through the actual picker callback
ok 2127 - Pomodoro bullet move picker confirms = through the actual picker callback
  ---
  duration_ms: 1.686771
  ...
# Subtest: Pomodoro bullet move picker reserves =NAME for peeling a named merged component
ok 2128 - Pomodoro bullet move picker reserves =NAME for peeling a named merged component
  ---
  duration_ms: 1.252702
  ...
# Subtest: Pomodoro bullet move picker confirms =email through the actual picker callback
ok 2129 - Pomodoro bullet move picker confirms =email through the actual picker callback
  ---
  duration_ms: 1.526536
  ...
# Subtest: Pomodoro bullet move picker confirms = review through the actual picker callback
ok 2130 - Pomodoro bullet move picker confirms = review through the actual picker callback
  ---
  duration_ms: 0.765712
  ...
# Subtest: Pomodoro bullet move picker confirms =focus by unnaming a single-name source
ok 2131 - Pomodoro bullet move picker confirms =focus by unnaming a single-name source
  ---
  duration_ms: 0.694396
  ...
# Subtest: Pomodoro bullet split stale-content guard does not write
ok 2132 - Pomodoro bullet split stale-content guard does not write
  ---
  duration_ms: 0.336844
  ...
# Subtest: Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
ok 2133 - Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write
  ---
  duration_ms: 0.669448
  ...
# Subtest: native isOpen regression: pickers attach, close clears slot, reopen works
ok 2134 - native isOpen regression: pickers attach, close clears slot, reopen works
  ---
  duration_ms: 7.74519
  ...
# Subtest: stale registered pickers fail open on the next key
ok 2135 - stale registered pickers fail open on the next key
  ---
  duration_ms: 3.788394
  ...
# Subtest: Task Card onClose clears card classes and resolving flags
ok 2136 - Task Card onClose clears card classes and resolving flags
  ---
  duration_ms: 0.910639
  ...
# Subtest: planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
ok 2137 - planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source
  ---
  duration_ms: 4.659308
  ...
# Subtest: planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
ok 2138 - planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree
  ---
  duration_ms: 0.564879
  ...
# Subtest: planPomodoroBulletMove preserves the source when only some siblings move out
ok 2139 - planPomodoroBulletMove preserves the source when only some siblings move out
  ---
  duration_ms: 0.327826
  ...
# Subtest: planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
ok 2140 - planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants
  ---
  duration_ms: 0.362392
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
ok 2141 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry)
  ---
  duration_ms: 0.651615
  ...
# Subtest: planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
ok 2142 - planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries
  ---
  duration_ms: 0.780891
  ...
# Subtest: planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
ok 2143 - planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section)
  ---
  duration_ms: 0.428127
  ...
# Subtest: planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
ok 2144 - planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source
  ---
  duration_ms: 0.313709
  ...
# Subtest: planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
ok 2145 - planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source
  ---
  duration_ms: 0.505946
  ...
# Subtest: planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
ok 2146 - planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name
  ---
  duration_ms: 1.174373
  ...
# Subtest: planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
ok 2147 - planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate
  ---
  duration_ms: 0.368704
  ...
# Subtest: planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
ok 2148 - planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source
  ---
  duration_ms: 0.251992
  ...
# Subtest: planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
ok 2149 - planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically
  ---
  duration_ms: 0.42939
  ...
# Subtest: planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
ok 2150 - planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source
  ---
  duration_ms: 0.384124
  ...
# Subtest: planPomodoroBulletMove deletes both open and closed source entries the same way
ok 2151 - planPomodoroBulletMove deletes both open and closed source entries the same way
  ---
  duration_ms: 0.417017
  ...
# Subtest: planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
ok 2152 - planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure
  ---
  duration_ms: 0.328848
  ...
# Subtest: planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
ok 2153 - planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source
  ---
  duration_ms: 0.368844
  ...
# Subtest: planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
ok 2154 - planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source
  ---
  duration_ms: 0.487772
  ...
# Subtest: planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
ok 2155 - planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed
  ---
  duration_ms: 0.301707
  ...
# Subtest: planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
ok 2156 - planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent
  ---
  duration_ms: 2.296225
  ...
# Subtest: planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
ok 2157 - planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct
  ---
  duration_ms: 0.427336
  ...
# Subtest: planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
ok 2158 - planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted
  ---
  duration_ms: 0.416195
  ...
# Subtest: planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
ok 2159 - planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away
  ---
  duration_ms: 0.327626
  ...
# Subtest: planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
ok 2160 - planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry
  ---
  duration_ms: 0.796341
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
ok 2161 - planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard
  ---
  duration_ms: 0.448296
  ...
# Subtest: planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
ok 2162 - planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination
  ---
  duration_ms: 0.59643
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
ok 2163 - planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state
  ---
  duration_ms: 2.519052
  ...
# Subtest: planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
ok 2164 - planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones
  ---
  duration_ms: 0.522699
  ...
# Subtest: navigation Pomodoro picker renders theme accents and Ctrl+D only changes Recent suggestions
ok 2165 - navigation Pomodoro picker renders theme accents and Ctrl+D only changes Recent suggestions
  ---
  duration_ms: 31.449529
  ...
# Subtest: Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
ok 2166 - Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot
  ---
  duration_ms: 1.87981
  ...
# Subtest: commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
ok 2167 - commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction
  ---
  duration_ms: 2.437554
  ...
# Subtest: commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
ok 2168 - commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing
  ---
  duration_ms: 0.807562
  ...
# Subtest: commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
ok 2169 - commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice
  ---
  duration_ms: 0.667996
  ...
# Subtest: commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
ok 2170 - commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed
  ---
  duration_ms: 0.301185
  ...
# Subtest: Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
ok 2171 - Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing
  ---
  duration_ms: 6.351308
  ...
# Subtest: Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
ok 2172 - Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing
  ---
  duration_ms: 0.763247
  ...
# Subtest: Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
ok 2173 - Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges
  ---
  duration_ms: 1.242714
  ...
# Subtest: Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
ok 2174 - Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker
  ---
  duration_ms: 1.293591
  ...
# Subtest: task move picker closes before commit while other pickers retain delayed close
ok 2175 - task move picker closes before commit while other pickers retain delayed close
  ---
  duration_ms: 0.709234
  ...
# Subtest: parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
ok 2176 - parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes
  ---
  duration_ms: 2.147952
  ...
# Subtest: normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
ok 2177 - normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length
  ---
  duration_ms: 0.461712
  ...
# Subtest: formatPomodoroEntryLine emits a placeholder entry with or without a name
ok 2178 - formatPomodoroEntryLine emits a placeholder entry with or without a name
  ---
  duration_ms: 0.138695
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
ok 2179 - createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows
  ---
  duration_ms: 2.791772
  ...
# Subtest: Pomodoro move pickers place recent themes around typed names and exclude today's themes
ok 2180 - Pomodoro move pickers place recent themes around typed names and exclude today's themes
  ---
  duration_ms: 17.767532
  ...
# Subtest: createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
ok 2181 - createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only
  ---
  duration_ms: 1.007053
  ...
# Subtest: createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
ok 2182 - createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources
  ---
  duration_ms: 1.132403
  ...
# Subtest: createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
ok 2183 - createPomodoroBulletMovePickerRows formats titles, metadata, and query matches
  ---
  duration_ms: 0.781823
  ...
# Subtest: buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
ok 2184 - buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes
  ---
  duration_ms: 0.532176
  ...
# Subtest: buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
ok 2185 - buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case
  ---
  duration_ms: 0.444038
  ...
# Subtest: createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
ok 2186 - createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names
  ---
  duration_ms: 0.420332
  ...
# Subtest: createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
ok 2187 - createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument
  ---
  duration_ms: 0.309331
  ...
# Subtest: createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
ok 2188 - createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row
  ---
  duration_ms: 0.343636
  ...
# Subtest: collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
ok 2189 - collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections
  ---
  duration_ms: 0.417036
  ...
# Subtest: findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
ok 2190 - findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines
  ---
  duration_ms: 0.656414
  ...
# Subtest: findPomodoroBulletContext leaves plain \#task lines on the task-move route
ok 2191 - findPomodoroBulletContext leaves plain \#task lines on the task-move route
  ---
  duration_ms: 0.402348
  ...
# Subtest: discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
ok 2192 - discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths
  ---
  duration_ms: 0.974881
  ...
# Subtest: findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
ok 2193 - findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines
  ---
  duration_ms: 1.186876
  ...
# Subtest: discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
ok 2194 - discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry
  ---
  duration_ms: 1.143012
  ...
# Subtest: isMovablePomodoroEntryContext matches open current and future Pomodoro entries
ok 2195 - isMovablePomodoroEntryContext matches open current and future Pomodoro entries
  ---
  duration_ms: 3.4665
  ...
# Subtest: planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
ok 2196 - planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder
  ---
  duration_ms: 0.862728
  ...
# Subtest: planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
ok 2197 - planPomodoroEntryReorder promotes a future Pomodoro up into the current slot
  ---
  duration_ms: 0.340931
  ...
# Subtest: planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
ok 2198 - planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps
  ---
  duration_ms: 0.645333
  ...
# Subtest: planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
ok 2199 - planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace
  ---
  duration_ms: 0.562665
  ...
# Subtest: planPomodoroEntryReorder handles counted current swaps and their inverses
ok 2200 - planPomodoroEntryReorder handles counted current swaps and their inverses
  ---
  duration_ms: 0.553347
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
ok 2201 - planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder
  ---
  duration_ms: 0.253063
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
ok 2202 - planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder
  ---
  duration_ms: 0.233807
  ...
# Subtest: planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
ok 2203 - planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content
  ---
  duration_ms: 0.520735
  ...
# Subtest: planPomodoroEntryReorder round-trips a future-up swap across the current open entry
ok 2204 - planPomodoroEntryReorder round-trips a future-up swap across the current open entry
  ---
  duration_ms: 0.607691
  ...
# Subtest: planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
ok 2205 - planPomodoroEntryReorder refuses moving up past a closed or cancelled entry
  ---
  duration_ms: 0.756655
  ...
# Subtest: planPomodoroEntryReorder refuses moving down past the last placeholder in the section
ok 2206 - planPomodoroEntryReorder refuses moving down past the last placeholder in the section
  ---
  duration_ms: 0.226663
  ...
# Subtest: planPomodoroEntryReorder refuses both directions for a lone placeholder
ok 2207 - planPomodoroEntryReorder refuses both directions for a lone placeholder
  ---
  duration_ms: 0.190173
  ...
# Subtest: planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
ok 2208 - planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap
  ---
  duration_ms: 0.171888
  ...
# Subtest: planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
ok 2209 - planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources
  ---
  duration_ms: 0.305764
  ...
# Subtest: planPomodoroEntryReorder refuses illegal current/future spans atomically
ok 2210 - planPomodoroEntryReorder refuses illegal current/future spans atomically
  ---
  duration_ms: 0.673577
  ...
# Subtest: planPomodoroEntryReorder rejects a stale source line
ok 2211 - planPomodoroEntryReorder rejects a stale source line
  ---
  duration_ms: 0.211734
  ...
# Subtest: planPomodoroEntryReorder round-trips CRLF content
ok 2212 - planPomodoroEntryReorder round-trips CRLF content
  ---
  duration_ms: 0.343055
  ...
# Subtest: planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
ok 2213 - planPomodoroEntryReorder leaves content outside the two swapped blocks untouched
  ---
  duration_ms: 0.250489
  ...
# Subtest: planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
ok 2214 - planPomodoroEntryReorder moves a named placeholder down three positions with its subtree
  ---
  duration_ms: 0.371991
  ...
# Subtest: planPomodoroEntryReorder moves a placeholder up three positions and round-trips
ok 2215 - planPomodoroEntryReorder moves a placeholder up three positions and round-trips
  ---
  duration_ms: 0.584797
  ...
# Subtest: planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
ok 2216 - planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate
  ---
  duration_ms: 0.280686
  ...
# Subtest: planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
ok 2217 - planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary
  ---
  duration_ms: 0.567794
  ...
# Subtest: planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
ok 2218 - planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts
  ---
  duration_ms: 1.934745
  ...
# Subtest: planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
ok 2219 - planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes
  ---
  duration_ms: 0.390516
  ...
# Subtest: peelPomodoroMergedName removes every matching canonical plus component
ok 2220 - peelPomodoroMergedName removes every matching canonical plus component
  ---
  duration_ms: 3.052358
  ...
# Subtest: planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
ok 2221 - planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source
  ---
  duration_ms: 4.804534
  ...
# Subtest: planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
ok 2222 - planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings
  ---
  duration_ms: 0.979801
  ...
# Subtest: planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
ok 2223 - planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries
  ---
  duration_ms: 0.975413
  ...
# Subtest: planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
ok 2224 - planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation
  ---
  duration_ms: 1.210251
  ...
# Subtest: planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
ok 2225 - planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel
  ---
  duration_ms: 2.199731
  ...
# Subtest: planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
ok 2226 - planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent
  ---
  duration_ms: 1.375166
  ...
# Subtest: planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
ok 2227 - planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers
  ---
  duration_ms: 1.755523
  ...
# Subtest: Pomodoro bullet move picker typing =NAME or Escape does not write
ok 2228 - Pomodoro bullet move picker typing =NAME or Escape does not write
  ---
  duration_ms: 4.034205
  ...
# Subtest: planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
ok 2229 - planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries
  ---
  duration_ms: 0.682343
  ...
# Subtest: planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
ok 2230 - planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names
  ---
  duration_ms: 5.102264
  ...
# Subtest: planPomodoroEntryRename reports unchanged when the normalized name matches the current name
ok 2231 - planPomodoroEntryRename reports unchanged when the normalized name matches the current name
  ---
  duration_ms: 0.412607
  ...
# Subtest: planPomodoroEntryRename rejects unsupported trailing content and a stale source line
ok 2232 - planPomodoroEntryRename rejects unsupported trailing content and a stale source line
  ---
  duration_ms: 0.202277
  ...
# Subtest: planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
ok 2233 - planPomodoroEntryRename renames closed and cancelled entries the same way as open ones
  ---
  duration_ms: 1.608942
  ...
# Subtest: planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
ok 2234 - planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names
  ---
  duration_ms: 2.590947
  ...
# Subtest: planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
ok 2235 - planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit
  ---
  duration_ms: 1.181737
  ...
# Subtest: planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
ok 2236 - planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation
  ---
  duration_ms: 0.621387
  ...
# Subtest: manager relative dates label today, yesterday, and older days
ok 2237 - manager relative dates label today, yesterday, and older days
  ---
  duration_ms: 1.106433
  ...
# Subtest: manager duplicate pairs follow the near-duplicate rule
ok 2238 - manager duplicate pairs follow the near-duplicate rule
  ---
  duration_ms: 0.57619
  ...
# Subtest: manager rows separate views, hints, and reappeared flags
ok 2239 - manager rows separate views, hints, and reappeared flags
  ---
  duration_ms: 1.343726
  ...
# Subtest: manager rename input rejects empty names and composites
ok 2240 - manager rename input rejects empty names and composites
  ---
  duration_ms: 0.268873
  ...
# Subtest: manager rename preview formats files, entries, and state notes
ok 2241 - manager rename preview formats files, entries, and state notes
  ---
  duration_ms: 0.372882
  ...
# Subtest: manager occurrences scan skips fences and non-Pomodoro bullets
ok 2242 - manager occurrences scan skips fences and non-Pomodoro bullets
  ---
  duration_ms: 0.480648
  ...
# Subtest: manager opens, cycles views, filters, and hides through the stubbed api
ok 2243 - manager opens, cycles views, filters, and hides through the stubbed api
  ---
  duration_ms: 10.946497
  ...
# Subtest: manager refuses without the desktop api
ok 2244 - manager refuses without the desktop api
  ---
  duration_ms: 0.616097
  ...
# Subtest: color modal pins hues and Auto through the stubbed api
ok 2245 - color modal pins hues and Auto through the stubbed api
  ---
  duration_ms: 5.343374
  ...
# Subtest: action modal jumps to actions with single keys when the filter is empty
ok 2246 - action modal jumps to actions with single keys when the filter is empty
  ---
  duration_ms: 1.94785
  ...
# Subtest: rename modal previews the dry run and applies one merge commit
ok 2247 - rename modal previews the dry run and applies one merge commit
  ---
  duration_ms: 1.690258
  ...
# Subtest: rename apply saves touched notes and refuses on a failed save
ok 2248 - rename apply saves touched notes and refuses on a failed save
  ---
  duration_ms: 0.505335
  ...
# Subtest: occurrences modal lists daily notes and opens the entry
ok 2249 - occurrences modal lists daily notes and opens the entry
  ---
  duration_ms: 2.226592
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: priority notice relative day helpers handle offsets ranges and icons
ok 2250 - priority notice relative day helpers handle offsets ranges and icons
  ---
  duration_ms: 1.352964
  ...
# Subtest: priority notice model summarizes single counted and project writes
ok 2251 - priority notice model summarizes single counted and project writes
  ---
  duration_ms: 3.21961
  ...
# Subtest: priority notice renderer builds an accessible fragment
ok 2252 - priority notice renderer builds an accessible fragment
  ---
  duration_ms: 2.064884
  ...
# Subtest: priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
ok 2253 - priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens
  ---
  duration_ms: 10.340025
  ...
# Subtest: priority notice falls back to one plain notice without a DOM
ok 2254 - priority notice falls back to one plain notice without a DOM
  ---
  duration_ms: 0.729383
  ...
# Subtest: priority notice falls back to plain text when fragment rendering fails
ok 2255 - priority notice falls back to plain text when fragment rendering fails
  ---
  duration_ms: 0.516647
  ...
# Subtest: priority scheduling rolls inclusively and clamps a random value of one
ok 2256 - priority scheduling rolls inclusively and clamps a random value of one
  ---
  duration_ms: 0.753559
  ...
# Subtest: priority value rows preserve config order and expose labels ranges and current state
ok 2257 - priority value rows preserve config order and expose labels ranges and current state
  ---
  duration_ms: 1.124777
  ...
# Subtest: priority picker writes priority then rolled schedule in one guarded edit
ok 2258 - priority picker writes priority then rolled schedule in one guarded edit
  ---
  duration_ms: 17.663453
  ...
# Subtest: priority picker writes lowest priority with a wide rolled schedule
ok 2259 - priority picker writes lowest priority with a wide rolled schedule
  ---
  duration_ms: 2.836817
  ...
# Subtest: priority picker replaces both existing values without duplicating fields
ok 2260 - priority picker replaces both existing values without duplicating fields
  ---
  duration_ms: 6.807629
  ...
# Subtest: counted priority writes keep the rolled date right of the priority
ok 2261 - counted priority writes keep the rolled date right of the priority
  ---
  duration_ms: 5.374412
  ...
# Subtest: priority picker writes project priority and schedule inline atomically
ok 2262 - priority picker writes project priority and schedule inline atomically
  ---
  duration_ms: 5.707832
  ...
# Subtest: counted priority picker rolls an independent schedule for every task
ok 2263 - counted priority picker rolls an independent schedule for every task
  ---
  duration_ms: 3.840655
  ...
# Subtest: counted priority planning keeps project schedules inline
ok 2264 - counted priority planning keeps project schedules inline
  ---
  duration_ms: 1.192367
  ...
# Subtest: counted priority planning evaluates Blocked recovery per rolled date
ok 2265 - counted priority planning evaluates Blocked recovery per rolled date
  ---
  duration_ms: 1.519251
  ...
# Subtest: a counted priority batch writes one entry per task using each task's own previous level
ok 2266 - a counted priority batch writes one entry per task using each task's own previous level
  ---
  duration_ms: 1.115129
  ...
# Subtest: priority notice models carry the stored level value for the glyph
ok 2267 - priority notice models carry the stored level value for the glyph
  ---
  duration_ms: 0.572944
  ...
# Subtest: ledger priority mark lookup guards version and render
ok 2268 - ledger priority mark lookup guards version and render
  ---
  duration_ms: 0.191545
  ...
# Subtest: priority notice header reuses the shared mark when available
ok 2269 - priority notice header reuses the shared mark when available
  ---
  duration_ms: 0.488743
  ...
# Subtest: priority notice keeps the Lucide icon without a usable mark api
ok 2270 - priority notice keeps the Lucide icon without a usable mark api
  ---
  duration_ms: 1.718982
  ...
# Subtest: a counted priority batch skips a task whose rolled date equals its current date
ok 2271 - a counted priority batch skips a task whose rolled date equals its current date
  ---
  duration_ms: 6.814883
  ...
# Subtest: counted priority runtime aborts a stale session without rolling writes
ok 2272 - counted priority runtime aborts a stale session without rolling writes
  ---
  duration_ms: 2.983016
  ...
# Subtest: scheduled picker pins a priority roll only for configured current priorities
ok 2273 - scheduled picker pins a priority roll only for configured current priorities
  ---
  duration_ms: 23.048036
  ...
# Subtest: Ctrl+R replaces only the pinned priority roll and keeps it selected
ok 2274 - Ctrl+R replaces only the pinned priority roll and keeps it selected
  ---
  duration_ms: 10.088916
  ...
# Subtest: choosing a priority roll writes immediately with a deterministic reason instead of prompting
ok 2275 - choosing a priority roll writes immediately with a deterministic reason instead of prompting
  ---
  duration_ms: 6.491167
  ...
# Subtest: counted scheduled picker requires one shared configured priority
ok 2276 - counted scheduled picker requires one shared configured priority
  ---
  duration_ms: 9.430519
  ...
# Subtest: buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
ok 2277 - buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items
  ---
  duration_ms: 3.323537
  ...
# Subtest: buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
ok 2278 - buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items
  ---
  duration_ms: 0.323036
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
ok 2279 - buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task
  ---
  duration_ms: 0.438297
  ...
# Subtest: buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
ok 2280 - buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order
  ---
  duration_ms: 0.279093
  ...
# Subtest: buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
ok 2281 - buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths
  ---
  duration_ms: 0.462773
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
ok 2282 - buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task
  ---
  duration_ms: 0.173772
  ...
# Subtest: buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
ok 2283 - buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output
  ---
  duration_ms: 0.235871
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
ok 2284 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log
  ---
  duration_ms: 0.38745
  ...
# Subtest: buildProjectSeedFromChildBullets moves a direct-child work log under the project task
ok 2285 - buildProjectSeedFromChildBullets moves a direct-child work log under the project task
  ---
  duration_ms: 0.33521
  ...
# Subtest: buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
ok 2286 - buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte
  ---
  duration_ms: 2.654811
  ...
# Subtest: buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
ok 2287 - buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths
  ---
  duration_ms: 0.293391
  ...
# Subtest: buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
ok 2288 - buildProjectSeedFromChildBullets leaves a nested work log under the converted child task
  ---
  duration_ms: 0.164083
  ...
# Subtest: buildProjectSeedFromChildBullets moves an empty work log without forcing task output
ok 2289 - buildProjectSeedFromChildBullets moves an empty work log without forcing task output
  ---
  duration_ms: 0.116542
  ...
# Subtest: buildProjectSeedFromChildBullets moves managed logs in source order without sorting by kind
ok 2290 - buildProjectSeedFromChildBullets moves managed logs in source order without sorting by kind
  ---
  duration_ms: 0.138304
  ...
# Subtest: buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
ok 2291 - buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs
  ---
  duration_ms: 0.269325
  ...
# Subtest: parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
ok 2292 - parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text
  ---
  duration_ms: 0.29326
  ...
# Subtest: Rotten Log markers, history reading, formatting, and generic insertion
ok 2293 - Rotten Log markers, history reading, formatting, and generic insertion
  ---
  duration_ms: 1.469678
  ...
# Subtest: parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
ok 2294 - parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker
  ---
  duration_ms: 0.165446
  ...
# Subtest: parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
ok 2295 - parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it
  ---
  duration_ms: 0.213157
  ...
# Subtest: normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
ok 2296 - normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation
  ---
  duration_ms: 0.091815
  ...
# Subtest: parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
ok 2297 - parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code
  ---
  duration_ms: 0.126652
  ...
# Subtest: formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
ok 2298 - formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace
  ---
  duration_ms: 0.131922
  ...
# Subtest: insertProjectSectionNotes fills an empty existing section with a blank line then the notes
ok 2299 - insertProjectSectionNotes fills an empty existing section with a blank line then the notes
  ---
  duration_ms: 0.61811
  ...
# Subtest: insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
ok 2300 - insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched
  ---
  duration_ms: 0.185224
  ...
# Subtest: insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
ok 2301 - insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing
  ---
  duration_ms: 0.13585
  ...
# Subtest: insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
ok 2302 - insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline
  ---
  duration_ms: 0.238355
  ...
# Subtest: insertProjectSectionNotes does not add a trailing newline when the original content had none
ok 2303 - insertProjectSectionNotes does not add a trailing newline when the original content had none
  ---
  duration_ms: 0.143714
  ...
# Subtest: insertProjectSectionNotes preserves CRLF line endings for an existing section
ok 2304 - insertProjectSectionNotes preserves CRLF line endings for an existing section
  ---
  duration_ms: 0.205753
  ...
# Subtest: insertProjectSectionNotes creates a new section using the document's CRLF line ending
ok 2305 - insertProjectSectionNotes creates a new section using the document's CRLF line ending
  ---
  duration_ms: 0.137803
  ...
# Subtest: buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
ok 2306 - buildProjectSeedFromChildBullets merges section bullets with equally-normalized titles in source order
  ---
  duration_ms: 0.228837
  ...
# Subtest: buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
ok 2307 - buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim
  ---
  duration_ms: 0.337595
  ...
# Subtest: buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
ok 2308 - buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks
  ---
  duration_ms: 0.129467
  ...
# Subtest: buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
ok 2309 - buildProjectContentFromTask appends a TASKS section bullet's notes after the converted child tasks
  ---
  duration_ms: 1.503791
  ...
# Subtest: project conversion accepts blocked sources and extracts their managed dependency child
ok 2310 - project conversion accepts blocked sources and extracts their managed dependency child
  ---
  duration_ms: 2.974009
  ...
# Subtest: project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
ok 2311 - project seeding keeps the inline date and identity on ^prj and tags open residents when blocked
  ---
  duration_ms: 1.276558
  ...
# Subtest: buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
ok 2312 - buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task
  ---
  duration_ms: 0.362212
  ...
# Subtest: buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
ok 2313 - buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task
  ---
  duration_ms: 0.23047
  ...
# Subtest: buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
ok 2314 - buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding
  ---
  duration_ms: 0.207727
  ...
# Subtest: insertProjectManagedLogLines preserves CRLF line endings
ok 2315 - insertProjectManagedLogLines preserves CRLF line endings
  ---
  duration_ms: 0.16764
  ...
# Subtest: findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
ok 2316 - findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks
  ---
  duration_ms: 0.221363
  ...
# Subtest: getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
ok 2317 - getProjectFromTaskNoticeText reports a singular/plural section count like the link chip
  ---
  duration_ms: 0.202035
  ...
# Subtest: getProjectFromTaskNoticeText reports moved log kinds in a fixed order
ok 2318 - getProjectFromTaskNoticeText reports moved log kinds in a fixed order
  ---
  duration_ms: 0.109399
  ...
# Subtest: forward conversion leaves the project Ready when only the source status was Blocked
ok 2319 - forward conversion leaves the project Ready when only the source status was Blocked
  ---
  duration_ms: 0.373573
  ...
# Subtest: buildTaskBlockFromProjectNote restores the worked example and round-trips
ok 2320 - buildTaskBlockFromProjectNote restores the worked example and round-trips
  ---
  duration_ms: 8.880999
  ...
# Subtest: project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
ok 2321 - project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects
  ---
  duration_ms: 2.324919
  ...
# Subtest: buildTaskLineFromProjectNote preserves status, tags, and fields
ok 2322 - buildTaskLineFromProjectNote preserves status, tags, and fields
  ---
  duration_ms: 1.834954
  ...
# Subtest: getProjectReversalBlockId inverts the forward basename helper
ok 2323 - getProjectReversalBlockId inverts the forward basename helper
  ---
  duration_ms: 0.156258
  ...
# Subtest: formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
ok 2324 - formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones
  ---
  duration_ms: 0.151349
  ...
# Subtest: splitProjectNoteForReversal treats TASKS as the task section and keeps section order
ok 2325 - splitProjectNoteForReversal treats TASKS as the task section and keeps section order
  ---
  duration_ms: 0.96335
  ...
# Subtest: indentProjectReversalLine preserves relative depth and drops blanks
ok 2326 - indentProjectReversalLine preserves relative depth and drops blanks
  ---
  duration_ms: 0.456562
  ...
# Subtest: buildTaskBlockFromProjectNote reports structure and frontmatter errors
ok 2327 - buildTaskBlockFromProjectNote reports structure and frontmatter errors
  ---
  duration_ms: 1.28863
  ...
# Subtest: buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
ok 2328 - buildTaskBlockFromProjectNote keeps CRLF notes reconstructable
  ---
  duration_ms: 1.058992
  ...
# Subtest: rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
ok 2329 - rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj
  ---
  duration_ms: 0.531144
  ...
# Subtest: collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
ok 2330 - collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs
  ---
  duration_ms: 0.622138
  ...
# Subtest: getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
ok 2331 - getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback
  ---
  duration_ms: 0.199271
  ...
# Subtest: convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
ok 2332 - convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note
  ---
  duration_ms: 5.961286
  ...
# Subtest: project reversal recovers tagged residents when they leave a blocked project
ok 2333 - project reversal recovers tagged residents when they leave a blocked project
  ---
  duration_ms: 4.913594
  ...
# Subtest: convertProjectNoteToTask separates the restored task from a count-only parent section
ok 2334 - convertProjectNoteToTask separates the restored task from a count-only parent section
  ---
  duration_ms: 1.614493
  ...
# Subtest: createProjectNoteFromTask dispatches reverse only on a real ^prj line
ok 2335 - createProjectNoteFromTask dispatches reverse only on a real ^prj line
  ---
  duration_ms: 5.125598
  ...
# Subtest: convertProjectNoteToTask refusals leave every file untouched
ok 2336 - convertProjectNoteToTask refusals leave every file untouched
  ---
  duration_ms: 4.003385
  ...
# Subtest: planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
ok 2337 - planBlockIdLinkContentRewrites plans parent \#^prj rewrites in memory
  ---
  duration_ms: 0.222444
  ...
# Subtest: convertProjectNoteToTask writes the parent first when it links to \#^prj
ok 2338 - convertProjectNoteToTask writes the parent first when it links to \#^prj
  ---
  duration_ms: 1.458916
  ...
# Subtest: convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
ok 2339 - convertProjectNoteToTask removes today's live \#^prj Pomodoro link when the parent is blocked
  ---
  duration_ms: 3.427315
  ...
# Subtest: convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
ok 2340 - convertProjectNoteToTask leaves every file unchanged when a \#^prj rewrite target is missing
  ---
  duration_ms: 1.442325
  ...
# Subtest: convertProjectNoteToTask reports post-write failures without rolling back
ok 2341 - convertProjectNoteToTask reports post-write failures without rolling back
  ---
  duration_ms: 1.887825
  ...
# Subtest: convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
ok 2342 - convertProjectNoteToTask keeps the project note when a link rewrite finds changed content
  ---
  duration_ms: 1.279113
  ...
# Subtest: convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
ok 2343 - convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails
  ---
  duration_ms: 1.656094
  ...
# Subtest: v2 reading task opens its source_pdf in Highlights without writes
ok 2344 - v2 reading task opens its source_pdf in Highlights without writes
  ---
  duration_ms: 3.460788
  ...
# Subtest: every reading-task lane and \#REF casing opens
ok 2345 - every reading-task lane and \#REF casing opens
  ---
  duration_ms: 1.417557
  ...
# Subtest: v1 tracker resolves a PDF link or falls back to its own source_pdf
ok 2346 - v1 tracker resolves a PDF link or falls back to its own source_pdf
  ---
  duration_ms: 0.546344
  ...
# Subtest: plain, embedded, struck, and 🍅 Task Links resolve reading tasks
ok 2347 - plain, embedded, struck, and 🍅 Task Links resolve reading tasks
  ---
  duration_ms: 1.908264
  ...
# Subtest: bare managed embed in a reference note resolves its embedded task
ok 2348 - bare managed embed in a reference note resolves its embedded task
  ---
  duration_ms: 0.428628
  ...
# Subtest: ordinary lines, unresolved Task Links, fences, and outside focus delegate once
ok 2349 - ordinary lines, unresolved Task Links, fences, and outside focus delegate once
  ---
  duration_ms: 0.792433
  ...
# Subtest: identified reading tasks show notices without delegating
ok 2350 - identified reading tasks show notices without delegating
  ---
  duration_ms: 0.496518
  ...
# Subtest: unsafe source_pdf values are refused
ok 2351 - unsafe source_pdf values are refused
  ---
  duration_ms: 0.225391
  ...
# Subtest: bundle launch retries with the app name, and reports stderr on total failure
ok 2352 - bundle launch retries with the app name, and reports stderr on total failure
  ---
  duration_ms: 0.72252
  ...
# Subtest: off macOS shows the selected notice and managed ref-note prose delegates
ok 2353 - off macOS shows the selected notice and managed ref-note prose delegates
  ---
  duration_ms: 0.543598
  ...
# Subtest: pure helpers normalize and parse reference PDF paths
ok 2354 - pure helpers normalize and parse reference PDF paths
  ---
  duration_ms: 0.25682
  ...
# Subtest: command registration is custom-hotkey only
ok 2355 - command registration is custom-hotkey only
  ---
  duration_ms: 0.328237
  ...
# Subtest: nav api openReferencePdf hands a source_pdf to Highlights without version or vault writes
ok 2356 - nav api openReferencePdf hands a source_pdf to Highlights without version or vault writes
  ---
  duration_ms: 0.783537
  ...
# Subtest: nav api openReferencePdf settles to a reason instead of throwing
ok 2357 - nav api openReferencePdf settles to a reason instead of throwing
  ---
  duration_ms: 0.360398
  ...
# Subtest: reading tasks read with the book prefix, plain tasks unchanged
ok 2358 - reading tasks read with the book prefix, plain tasks unchanged
  ---
  duration_ms: 1.51855
  ...
# Subtest: near-miss spellings never pair and never prefix
ok 2359 - near-miss spellings never pair and never prefix
  ---
  duration_ms: 0.334098
  ...
# Subtest: picker rows carry the book prefix in displayText
ok 2360 - picker rows carry the book prefix in displayText
  ---
  duration_ms: 0.928393
  ...
# Subtest: managed reference rename modal and submit are refused
ok 2361 - managed reference rename modal and submit are refused
  ---
  duration_ms: 1.594965
  ...
# Subtest: legacy ref notes and non-ref notes still rename
ok 2362 - legacy ref notes and non-ref notes still rename
  ---
  duration_ms: 1.283291
  ...
# Subtest: managed reference predicate checks path and non-empty source_pdf
ok 2363 - managed reference predicate checks path and non-empty source_pdf
  ---
  duration_ms: 0.269956
  ...
# Subtest: planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
ok 2364 - planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch
  ---
  duration_ms: 5.595625
  ...
# Subtest: planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
ok 2365 - planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line
  ---
  duration_ms: 2.259014
  ...
# Subtest: runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
ok 2366 - runtime: a future scheduled write prunes the task's live link from today's open Pomodoro
  ---
  duration_ms: 5.347292
  ...
# Subtest: runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
ok 2367 - runtime: a due (non-future) scheduled write does not touch today's Pomodoro links
  ---
  duration_ms: 3.271929
  ...
# Subtest: runtime: no daily note today still writes the schedule with no Pomodoro chip
ok 2368 - runtime: no daily note today still writes the schedule with no Pomodoro chip
  ---
  duration_ms: 0.512499
  ...
# Subtest: runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
ok 2369 - runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed
  ---
  duration_ms: 1.205884
  ...
# Subtest: runtime: vault.process throwing during the daily-note write is reported without throwing
ok 2370 - runtime: vault.process throwing during the daily-note write is reported without throwing
  ---
  duration_ms: 0.777816
  ...
# Subtest: runtime: the daily note open in another editor is written through that editor in its own transaction
ok 2371 - runtime: the daily note open in another editor is written through that editor in its own transaction
  ---
  duration_ms: 1.613642
  ...
# Subtest: runtime: re-running the same deferral gesture is idempotent
ok 2372 - runtime: re-running the same deferral gesture is idempotent
  ---
  duration_ms: 0.842699
  ...
# Subtest: runtime: a counted scheduled batch prunes exactly the targets that land on a future date
ok 2373 - runtime: a counted scheduled batch prunes exactly the targets that land on a future date
  ---
  duration_ms: 2.676781
  ...
# Subtest: runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
ok 2374 - runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself
  ---
  duration_ms: 2.541313
  ...
# Subtest: runtime: the source note being today's daily note folds the prune into a single editor transaction
ok 2375 - runtime: the source note being today's daily note folds the prune into a single editor transaction
  ---
  duration_ms: 0.739082
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: bare future scheduled writes block only real supported open inline tasks
ok 2376 - bare future scheduled writes block only real supported open inline tasks
  ---
  duration_ms: 6.237691
  ...
# Subtest: single runtime transclusion toggle preserves viewport in one line transaction
ok 2377 - single runtime transclusion toggle preserves viewport in one line transaction
  ---
  duration_ms: 2.776031
  ...
# Subtest: same-file runtime toggle changes only markers, never fields or statuses
ok 2378 - same-file runtime toggle changes only markers, never fields or statuses
  ---
  duration_ms: 0.955555
  ...
# Subtest: pure toggle leaves a cursor moved during the toggle where it landed
ok 2379 - pure toggle leaves a cursor moved during the toggle where it landed
  ---
  duration_ms: 0.394113
  ...
# Subtest: counted runtime transclusion toggle preserves viewport and caret
ok 2380 - counted runtime transclusion toggle preserves viewport and caret
  ---
  duration_ms: 1.060085
  ...
# Subtest: counted property runtime uses one transaction and preserves caret and viewport
ok 2381 - counted property runtime uses one transaction and preserves caret and viewport
  ---
  duration_ms: 3.642478
  ...
# Subtest: bare due schedule recovery is guarded and can change only task status
ok 2382 - bare due schedule recovery is guarded and can change only task status
  ---
  duration_ms: 2.571972
  ...
# Subtest: counted due recovery applies Ready Next and In Progress in one transaction
ok 2383 - counted due recovery applies Ready Next and In Progress in one transaction
  ---
  duration_ms: 5.981903
  ...
# Subtest: scheduled recovery aborts after an asynchronous source change
ok 2384 - scheduled recovery aborts after an asynchronous source change
  ---
  duration_ms: 0.932661
  ...
# Subtest: counted property runtime aborts a stale batch without a transaction
ok 2385 - counted property runtime aborts a stale batch without a transaction
  ---
  duration_ms: 0.532617
  ...
# Subtest: counted project scheduling writes an inline date and blocks tagged residents
ok 2386 - counted project scheduling writes an inline date and blocks tagged residents
  ---
  duration_ms: 2.935015
  ...
# Subtest: future project scheduling prunes resident links and an emptied Pomodoro
ok 2387 - future project scheduling prunes resident links and an emptied Pomodoro
  ---
  duration_ms: 3.57651
  ...
# Subtest: single project scheduling recovers due residents through the gate
ok 2388 - single project scheduling recovers due residents through the gate
  ---
  duration_ms: 2.842839
  ...
# Subtest: single project schedule deletion removes propagated copies and recovers
ok 2389 - single project schedule deletion removes propagated copies and recovers
  ---
  duration_ms: 1.913714
  ...
# Subtest: formatPriorityRollScheduleReason covers all four shapes
ok 2390 - formatPriorityRollScheduleReason covers all four shapes
  ---
  duration_ms: 1.343135
  ...
# Subtest: the priority-roll picker row keeps range detail and stores the exact roll
ok 2391 - the priority-roll picker row keeps range detail and stores the exact roll
  ---
  duration_ms: 0.611157
  ...
# Subtest: buildPriorityRollScheduleLog returns null when the roll does not move the date
ok 2392 - buildPriorityRollScheduleLog returns null when the roll does not move the date
  ---
  duration_ms: 0.735364
  ...
# Subtest: getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
ok 2393 - getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values
  ---
  duration_ms: 0.758007
  ...
# Subtest: a priority roll onto the current date writes the date but no log
ok 2394 - a priority roll onto the current date writes the date but no log
  ---
  duration_ms: 17.204426
  ...
# Subtest: a typed reason on an unchanged date is still written
ok 2395 - a typed reason on an unchanged date is still written
  ---
  duration_ms: 0.807722
  ...
# Subtest: schedule log bullet formatting and parsing round-trip with and without a previous value
ok 2396 - schedule log bullet formatting and parsing round-trip with and without a previous value
  ---
  duration_ms: 0.995641
  ...
# Subtest: formatScheduleLogEntryText renders entry text without indent or marker
ok 2397 - formatScheduleLogEntryText renders entry text without indent or marker
  ---
  duration_ms: 0.126431
  ...
# Subtest: schedule reason text normalization trims, collapses whitespace, and flags inline fields
ok 2398 - schedule reason text normalization trims, collapses whitespace, and flags inline fields
  ---
  duration_ms: 0.352273
  ...
# Subtest: findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
ok 2399 - findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's
  ---
  duration_ms: 0.751936
  ...
# Subtest: getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
ok 2400 - getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab
  ---
  duration_ms: 0.233876
  ...
# Subtest: planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
ok 2401 - planScheduleLogEntry creates, prepends, guards, and preserves blockquote context
  ---
  duration_ms: 0.493453
  ...
# Subtest: planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
ok 2402 - planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker
  ---
  duration_ms: 0.195353
  ...
# Subtest: planScheduleLogEntry uses the fallback only when a marker exists
ok 2403 - planScheduleLogEntry uses the fallback only when a marker exists
  ---
  duration_ms: 0.209891
  ...
# Subtest: a typed reason wins over the fallback
ok 2404 - a typed reason wins over the fallback
  ---
  duration_ms: 0.144446
  ...
# Subtest: the fallback is suppressed on an unchanged date
ok 2405 - the fallback is suppressed on an unchanged date
  ---
  duration_ms: 0.12065
  ...
# Subtest: no reason and no fallback still guards empty-reason
ok 2406 - no reason and no fallback still guards empty-reason
  ---
  duration_ms: 0.103547
  ...
# Subtest: getScheduleLogWriteOutcome maps plan outcomes for writers
ok 2407 - getScheduleLogWriteOutcome maps plan outcomes for writers
  ---
  duration_ms: 0.136591
  ...
# Subtest: hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
ok 2408 - hasScheduleLogReasonInput detects a typed reason or a fallback-only payload
  ---
  duration_ms: 0.117024
  ...
# Subtest: counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
ok 2409 - counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks
  ---
  duration_ms: 1.781472
  ...
# Subtest: empty reason through the counted planner writes no schedule log entries
ok 2410 - empty reason through the counted planner writes no schedule log entries
  ---
  duration_ms: 0.533509
  ...
# Subtest: a counted scheduled session logs only the tasks that already keep a log
ok 2411 - a counted scheduled session logs only the tasks that already keep a log
  ---
  duration_ms: 0.58652
  ...
# Subtest: the counted notice wording distinguishes a fallback batch from a typed-reason batch
ok 2412 - the counted notice wording distinguishes a fallback batch from a typed-reason batch
  ---
  duration_ms: 3.949061
  ...
# Subtest: setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
ok 2413 - setBulletPropertyValue writes an inline scheduled date plus a schedule log entry
  ---
  duration_ms: 0.37167
  ...
# Subtest: setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
ok 2414 - setProjectNoteScheduledValue writes a schedule log entry under the ^prj task
  ---
  duration_ms: 3.202966
  ...
# Subtest: priority bullet property config normalizes frozen levels and preserves existing shapes
ok 2415 - priority bullet property config normalizes frozen levels and preserves existing shapes
  ---
  duration_ms: 3.22049
  ...
# Subtest: priority bullet property config rejects each invalid schema category once
ok 2416 - priority bullet property config rejects each invalid schema category once
  ---
  duration_ms: 1.393892
  ...
# Subtest: project scheduling targets the inline ^prj field
ok 2417 - project scheduling targets the inline ^prj field
  ---
  duration_ms: 2.595305
  ...
# Subtest: local task properties are addable only on valid tasks but invalid metadata stays removable
ok 2418 - local task properties are addable only on valid tasks but invalid metadata stays removable
  ---
  duration_ms: 0.43991
  ...
# Subtest: dependency parent write validation rejects stale, Pomodoro, and fenced parents
ok 2419 - dependency parent write validation rejects stale, Pomodoro, and fenced parents
  ---
  duration_ms: 0.651865
  ...
# Subtest: counted property targets mean current plus N real tasks without wrapping
ok 2420 - counted property targets mean current plus N real tasks without wrapping
  ---
  duration_ms: 0.95296
  ...
# Subtest: counted property metadata distinguishes absent, common, and mixed values
ok 2421 - counted property metadata distinguishes absent, common, and mixed values
  ---
  duration_ms: 0.892956
  ...
# Subtest: counted priority metadata reports labels for common and mixed values
ok 2422 - counted priority metadata reports labels for common and mixed values
  ---
  duration_ms: 0.784147
  ...
# Subtest: counted scheduled planning updates the motivating three tasks atomically
ok 2423 - counted scheduled planning updates the motivating three tasks atomically
  ---
  duration_ms: 3.415352
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: project schedule validation accepts only real YYYY-MM-DD dates
ok 2424 - project schedule validation accepts only real YYYY-MM-DD dates
  ---
  duration_ms: 1.194151
  ...
# Subtest: source task schedule is extracted without losing task metadata
ok 2425 - source task schedule is extracted without losing task metadata
  ---
  duration_ms: 1.541624
  ...
# Subtest: source task schedule errors are focused and ambiguous fields fail
ok 2426 - source task schedule errors are focused and ambiguous fields fail
  ---
  duration_ms: 0.454608
  ...
# Subtest: project creation frontmatter never stores the task schedule
ok 2427 - project creation frontmatter never stores the task schedule
  ---
  duration_ms: 0.173963
  ...
# Subtest: future schedule labels use local date-only boundaries
ok 2428 - future schedule labels use local date-only boundaries
  ---
  duration_ms: 0.610336
  ...
# Subtest: scheduled recovery selects current and newest earlier daily across gaps
ok 2429 - scheduled recovery selects current and newest earlier daily across gaps
  ---
  duration_ms: 0.575379
  ...
# Subtest: scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
ok 2430 - scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph
  ---
  duration_ms: 9.01797
  ...
# Subtest: scheduled recovery defers incompatible status settings and ambiguous identities
ok 2431 - scheduled recovery defers incompatible status settings and ambiguous identities
  ---
  duration_ms: 0.568956
  ...
# Subtest: scheduled recovery honors custom open and closed Tasks status types
ok 2432 - scheduled recovery honors custom open and closed Tasks status types
  ---
  duration_ms: 0.676001
  ...
# Subtest: scheduled recovery honors the configured Tasks global filter
ok 2433 - scheduled recovery honors the configured Tasks global filter
  ---
  duration_ms: 0.558236
  ...
# Subtest: child picker schedule metadata reads the inline ^prj date
ok 2434 - child picker schedule metadata reads the inline ^prj date
  ---
  duration_ms: 0.920198
  ...
# Subtest: task move destination schedule hydration reads cached ^prj content
ok 2435 - task move destination schedule hydration reads cached ^prj content
  ---
  duration_ms: 0.544089
  ...
# Subtest: project lifecycle task classification requires unfenced \#task with trailing ^prj
ok 2436 - project lifecycle task classification requires unfenced \#task with trailing ^prj
  ---
  duration_ms: 0.169734
  ...
# Subtest: valid Obsidian tasks require a standalone \#task checkbox in real note content
ok 2437 - valid Obsidian tasks require a standalone \#task checkbox in real note content
  ---
  duration_ms: 0.150127
  ...
# Subtest: choosing a scheduled date enters the combined review without writing anything
ok 2438 - choosing a scheduled date enters the combined review without writing anything
  ---
  duration_ms: 12.460244
  ...
# Subtest: choosing a priority level does not enter the schedule review
ok 2439 - choosing a priority level does not enter the schedule review
  ---
  duration_ms: 12.459332
  ...
# Subtest: confirming an empty reason on a task with an existing schedule log appends an unexplained entry
ok 2440 - confirming an empty reason on a task with an existing schedule log appends an unexplained entry
  ---
  duration_ms: 7.213217
  ...
# Subtest: confirming an empty reason on a task with no schedule log writes only the date
ok 2441 - confirming an empty reason on a task with no schedule log writes only the date
  ---
  duration_ms: 3.458504
  ...
# Subtest: review stage getFilteredItems always returns exactly one synthetic preview item
ok 2442 - review stage getFilteredItems always returns exactly one synthetic preview item
  ---
  duration_ms: 2.994588
  ...
# Subtest: the review preview row previews the entry it will write
ok 2443 - the review preview row previews the entry it will write
  ---
  duration_ms: 3.256008
  ...
# Subtest: the review footer flips between Skip optional logs and Apply schedule as the Reason changes
ok 2444 - the review footer flips between Skip optional logs and Apply schedule as the Reason changes
  ---
  duration_ms: 1.486959
  ...
# Subtest: closing the picker during the review clears pending schedule state and writes nothing
ok 2445 - closing the picker during the review clears pending schedule state and writes nothing
  ---
  duration_ms: 1.170606
  ...
# Subtest: scheduling Work Log eligibility requires Pending or Next \#task lines
ok 2446 - scheduling Work Log eligibility requires Pending or Next \#task lines
  ---
  duration_ms: 1.496016
  ...
# Subtest: single Pending explicit date opens one review and writes both logs
ok 2447 - single Pending explicit date opens one review and writes both logs
  ---
  duration_ms: 26.010943
  ...
# Subtest: single Next blank and whitespace summaries schedule without a Work Log
ok 2448 - single Next blank and whitespace summaries schedule without a Work Log
  ---
  duration_ms: 6.688412
  ...
# Subtest: Escape at the review writes nothing, with or without typed text
ok 2449 - Escape at the review writes nothing, with or without typed text
  ---
  duration_ms: 7.400091
  ...
# Subtest: Ready and Blocked explicit dates review the Reason with no Work summary field
ok 2450 - Ready and Blocked explicit dates review the Reason with no Work summary field
  ---
  duration_ms: 5.884319
  ...
# Subtest: future scheduling on Pending marks Blocked but still writes the Work Log
ok 2451 - future scheduling on Pending marks Blocked but still writes the Work Log
  ---
  duration_ms: 6.62384
  ...
# Subtest: today date on Pending still offers the Work Log
ok 2452 - today date on Pending still offers the Work Log
  ---
  duration_ms: 3.650821
  ...
# Subtest: priority pick on Pending freezes its roll and offers the Work Log
ok 2453 - priority pick on Pending freezes its roll and offers the Work Log
  ---
  duration_ms: 5.199689
  ...
# Subtest: counted mixed statuses share one summary only on Pending and Next
ok 2454 - counted mixed statuses share one summary only on Pending and Next
  ---
  duration_ms: 6.902631
  ...
# Subtest: counted planner composes Schedule and Work Logs bottom-up above later targets
ok 2455 - counted planner composes Schedule and Work Logs bottom-up above later targets
  ---
  duration_ms: 1.106935
  ...
# Subtest: counted planner writes a Work Log even when the date is unchanged
ok 2456 - counted planner writes a Work Log even when the date is unchanged
  ---
  duration_ms: 0.324681
  ...
# Subtest: scheduling Work Log ownership keeps nested logs and CRLF endings
ok 2457 - scheduling Work Log ownership keeps nested logs and CRLF endings
  ---
  duration_ms: 0.867227
  ...
# Subtest: scheduling Work Log warns on :: and preserves Markdown
ok 2458 - scheduling Work Log warns on :: and preserves Markdown
  ---
  duration_ms: 2.247133
  ...
# Subtest: stale task while reviewing refuses with no scheduling or log writes
ok 2459 - stale task while reviewing refuses with no scheduling or log writes
  ---
  duration_ms: 1.808815
  ...
# Subtest: scheduling prompts never leak into lane or cancel stages
ok 2460 - scheduling prompts never leak into lane or cancel stages
  ---
  duration_ms: 2.855824
  ...
# api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
# Subtest: Pomodoro-marked links are not managed dependency bullets
ok 2461 - Pomodoro-marked links are not managed dependency bullets
  ---
  duration_ms: 1.536715
  ...
# Subtest: deleting inline scheduled metadata recovers Blocked targets by snapshot rank
ok 2462 - deleting inline scheduled metadata recovers Blocked targets by snapshot rank
  ---
  duration_ms: 3.837518
  ...
# Subtest: counted future scheduling blocks only supported open inline task statuses
ok 2463 - counted future scheduling blocks only supported open inline task statuses
  ---
  duration_ms: 1.787884
  ...
# Subtest: counted property planning rejects any stale source with no partial result
ok 2464 - counted property planning rejects any stale source with no partial result
  ---
  duration_ms: 0.291878
  ...
# Subtest: counted project scheduling writes the ^prj inline date and blocks tagged residents
ok 2465 - counted project scheduling writes the ^prj inline date and blocks tagged residents
  ---
  duration_ms: 1.862928
  ...
# Subtest: moving a project schedule earlier replaces only exact old-date copies
ok 2466 - moving a project schedule earlier replaces only exact old-date copies
  ---
  duration_ms: 0.416646
  ...
# Subtest: future project schedules block every open resident and consume review status
ok 2467 - future project schedules block every open resident and consume review status
  ---
  duration_ms: 0.606839
  ...
# Subtest: due project dates recover residents through the gate and write unblocked markers
ok 2468 - due project dates recover residents through the gate and write unblocked markers
  ---
  duration_ms: 0.593393
  ...
# Subtest: schedule deletion removes only exact project-date copies and recovers residents
ok 2469 - schedule deletion removes only exact project-date copies and recovers residents
  ---
  duration_ms: 0.885311
  ...
# Subtest: dependency lines render one canonical Depends-On line per parent
ok 2470 - dependency lines render one canonical Depends-On line per parent
  ---
  duration_ms: 0.690909
  ...
# Subtest: dependency IDs encode root and nested Markdown paths deterministically
ok 2471 - dependency IDs encode root and nested Markdown paths deterministically
  ---
  duration_ms: 0.9164
  ...
# Subtest: prompted block IDs truthfully replace legacy id fields
ok 2472 - prompted block IDs truthfully replace legacy id fields
  ---
  duration_ms: 0.162069
  ...
# Subtest: dependency navigation identity includes note path and folds legacy children
ok 2473 - dependency navigation identity includes note path and folds legacy children
  ---
  duration_ms: 0.886343
  ...
# Subtest: retired dependency bullets are excluded from single and counted toggles
ok 2474 - retired dependency bullets are excluded from single and counted toggles
  ---
  duration_ms: 1.209621
  ...
# Subtest: dependsOn replacement accepts spaces around field name and separator
ok 2475 - dependsOn replacement accepts spaces around field name and separator
  ---
  duration_ms: 0.270918
  ...
# Subtest: task status helpers keep Blocked open but rankless
ok 2476 - task status helpers keep Blocked open but rankless
  ---
  duration_ms: 0.290424
  ...
# Subtest: a due project date with only closed Depends-On history strips the tag
ok 2477 - a due project date with only closed Depends-On history strips the tag
  ---
  duration_ms: 0.751796
  ...
# Subtest: Ctrl+D with only closed Depends-On history strips the tag
ok 2478 - Ctrl+D with only closed Depends-On history strips the tag
  ---
  duration_ms: 0.373754
  ...
# Subtest: Ctrl+D with an open Depends-On link remaining keeps the tag
ok 2479 - Ctrl+D with an open Depends-On link remaining keeps the tag
  ---
  duration_ms: 0.296787
  ...
# Subtest: counted ^prj schedule sessions write [unblocked::] when the writer is passed
ok 2480 - counted ^prj schedule sessions write [unblocked::] when the writer is passed
  ---
  duration_ms: 0.48163
  ...
# Subtest: a due project date keeps the tag while ^prj holds Depends-On links
ok 2481 - a due project date keeps the tag while ^prj holds Depends-On links
  ---
  duration_ms: 0.288931
  ...
# Subtest: a due project date strips the tag while a resident with its own reason stays Blocked
ok 2482 - a due project date strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.265888
  ...
# Subtest: Ctrl+D strips the tag while a resident with its own reason stays Blocked
ok 2483 - Ctrl+D strips the tag while a resident with its own reason stays Blocked
  ---
  duration_ms: 0.322486
  ...
# Subtest: counted scheduled deletes recover with [unblocked::] when the writer is passed
ok 2484 - counted scheduled deletes recover with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.220902
  ...
# Subtest: section-header navigation moves normally and cycles at boundaries
ok 2485 - section-header navigation moves normally and cycles at boundaries
  ---
  duration_ms: 1.926881
  ...
# Subtest: section-header navigation wraps from beyond document boundaries
ok 2486 - section-header navigation wraps from beyond document boundaries
  ---
  duration_ms: 0.202346
  ...
# Subtest: section-header navigation handles single-header and no-header notes
ok 2487 - section-header navigation handles single-header and no-header notes
  ---
  duration_ms: 0.27219
  ...
# Subtest: open-task navigation scan includes Ready In Progress and Next and excludes Blocked
ok 2488 - open-task navigation scan includes Ready In Progress and Next and excludes Blocked
  ---
  duration_ms: 0.551914
  ...
# Subtest: open-task navigation keeps existing Pomodoro ledger targets
ok 2489 - open-task navigation keeps existing Pomodoro ledger targets
  ---
  duration_ms: 0.532096
  ...
# Subtest: next and previous jumps skip Blocked tasks and wrap to an allowed task
ok 2490 - next and previous jumps skip Blocked tasks and wrap to an allowed task
  ---
  duration_ms: 0.324439
  ...
# Subtest: blocked-only notes and a sole current allowed task have no jump target
ok 2491 - blocked-only notes and a sole current allowed task have no jump target
  ---
  duration_ms: 0.153342
  ...
# Subtest: counted open-task jumps select the Nth eligible target and wrap modulo the list
ok 2492 - counted open-task jumps select the Nth eligible target and wrap modulo the list
  ---
  duration_ms: 0.280435
  ...
# Subtest: counted open-task jumps keep sole-target and invalid-repeat behavior
ok 2493 - counted open-task jumps keep sole-target and invalid-repeat behavior
  ---
  duration_ms: 0.468836
  ...
# Subtest: tab pin Vim action registers once and toggles only the active leaf once
ok 2494 - tab pin Vim action registers once and toggles only the active leaf once
  ---
  duration_ms: 2.587391
  ...
# Subtest: tab pin toggle fails safely without a supported active leaf
ok 2495 - tab pin toggle fails safely without a supported active leaf
  ---
  duration_ms: 0.20958
  ...
# Subtest: close tabs left preserves pinned sibling tabs and refocuses active tab
ok 2496 - close tabs left preserves pinned sibling tabs and refocuses active tab
  ---
  duration_ms: 0.675981
  ...
# Subtest: close tabs right preserves pinned siblings and ignores the left side
ok 2497 - close tabs right preserves pinned siblings and ignores the left side
  ---
  duration_ms: 0.282008
  ...
# Subtest: close other tabs preserves pinned siblings on both sides
ok 2498 - close other tabs preserves pinned siblings on both sides
  ---
  duration_ms: 0.243645
  ...
# Subtest: close sibling tabs is a silent no-op when the scoped range is all pinned
ok 2499 - close sibling tabs is a silent no-op when the scoped range is all pinned
  ---
  duration_ms: 0.195273
  ...
# Subtest: close sibling tabs honors every pinned leaf representation
ok 2500 - close sibling tabs honors every pinned leaf representation
  ---
  duration_ms: 0.244777
  ...
# Subtest: close sibling tabs treats throwing view state as unpinned
ok 2501 - close sibling tabs treats throwing view state as unpinned
  ---
  duration_ms: 0.353726
  ...
# Subtest: tab pin Vim registration retries after adapter availability
ok 2502 - tab pin Vim registration retries after adapter availability
  ---
  duration_ms: 0.782515
  ...
# Subtest: isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
ok 2503 - isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry
  ---
  duration_ms: 4.367931
  ...
# Subtest: isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
ok 2504 - isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths
  ---
  duration_ms: 0.835285
  ...
# Subtest: isPomodoroTaskLinkLine refuses Depends-On lines and prose links
ok 2505 - isPomodoroTaskLinkLine refuses Depends-On lines and prose links
  ---
  duration_ms: 0.24085
  ...
# Subtest: decideTaskLinkLaneMode starts when any target is Next
ok 2506 - decideTaskLinkLaneMode starts when any target is Next
  ---
  duration_ms: 0.237162
  ...
# Subtest: taskLinkLaneRefusalFor renders every D5 refusal
ok 2507 - taskLinkLaneRefusalFor renders every D5 refusal
  ---
  duration_ms: 0.174633
  ...
# Subtest: planTaskLinkLaneBatch starts Next targets and leaves the rest alone
ok 2508 - planTaskLinkLaneBatch starts Next targets and leaves the rest alone
  ---
  duration_ms: 1.443116
  ...
# Subtest: planTaskLinkLaneBatch pauses with one shared Work Log entry
ok 2509 - planTaskLinkLaneBatch pauses with one shared Work Log entry
  ---
  duration_ms: 0.788376
  ...
# Subtest: planTaskLinkLaneBatch applies the freshness stamp last
ok 2510 - planTaskLinkLaneBatch applies the freshness stamp last
  ---
  duration_ms: 0.470739
  ...
# Subtest: planTaskLinkLaneBatch dedupes lines and refuses stale preimages
ok 2511 - planTaskLinkLaneBatch dedupes lines and refuses stale preimages
  ---
  duration_ms: 0.536314
  ...
# Subtest: buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
ok 2512 - buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets
  ---
  duration_ms: 0.734362
  ...
# Subtest: taskLinkLanePromptState drives the Move to Next prompt
ok 2513 - taskLinkLanePromptState drives the Move to Next prompt
  ---
  duration_ms: 0.31423
  ...
# Subtest: TaskLinkLanePromptModal submits, previews live, and cancels silently
ok 2514 - TaskLinkLanePromptModal submits, previews live, and cancels silently
  ---
  duration_ms: 1.513912
  ...
# Subtest: TaskLinkLanePromptModal renders the batch context card
ok 2515 - TaskLinkLanePromptModal renders the batch context card
  ---
  duration_ms: 0.369475
  ...
# Subtest: findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
ok 2516 - findUniqueLinkPickerTargetLine allowClosed resolves closed tasks
  ---
  duration_ms: 0.304532
  ...
# Subtest: L1: toggle starts a Next link, stamps, hints, and notices
ok 2517 - L1: toggle starts a Next link, stamps, hints, and notices
  ---
  duration_ms: 3.598804
  ...
# Subtest: L2/L3: toggle pauses through the prompt, logging one shared entry
ok 2518 - L2/L3: toggle pauses through the prompt, logging one shared entry
  ---
  duration_ms: 12.493288
  ...
# Subtest: L4: cancelling the prompt writes nothing and shows no Notice
ok 2519 - L4: cancelling the prompt writes nothing and shows no Notice
  ---
  duration_ms: 1.148342
  ...
# Subtest: L5: both directions run the same toggle twice for a round trip
ok 2520 - L5: both directions run the same toggle twice for a round trip
  ---
  duration_ms: 1.630754
  ...
# Subtest: L6: Ready, Blocked, done, and cancelled targets are refused
ok 2521 - L6: Ready, Blocked, done, and cancelled targets are refused
  ---
  duration_ms: 1.65967
  ...
# Subtest: L6: missing targets keep the existing resolver error
ok 2522 - L6: missing targets keep the existing resolver error
  ---
  duration_ms: 0.263894
  ...
# Subtest: L7: a counted start flips every Next sibling and leaves In Progress alone
ok 2523 - L7: a counted start flips every Next sibling and leaves In Progress alone
  ---
  duration_ms: 0.749872
  ...
# Subtest: L8: a counted pause prompts once and skips Blocked with a count
ok 2524 - L8: a counted pause prompts once and skips Blocked with a count
  ---
  duration_ms: 2.01622
  ...
# Subtest: L9: an over-long count clamps at the entry end without error
ok 2525 - L9: an over-long count clamps at the entry end without error
  ---
  duration_ms: 0.662284
  ...
# Subtest: L10: a closed-entry history line toggles the task and keeps the line
ok 2526 - L10: a closed-entry history line toggles the task and keeps the line
  ---
  duration_ms: 0.420413
  ...
# Subtest: L11: a target edited while the prompt is open refuses stale
ok 2527 - L11: a target edited while the prompt is open refuses stale
  ---
  duration_ms: 1.886753
  ...
# Subtest: L12: an embedded Pomodoro link takes the two-state toggle
ok 2528 - L12: an embedded Pomodoro link takes the two-state toggle
  ---
  duration_ms: 0.561963
  ...
# Subtest: L14: the same task linked twice in a batch is written once
ok 2529 - L14: the same task linked twice in a batch is written once
  ---
  duration_ms: 4.043053
  ...
# Subtest: L15: a second toggle while one is in flight is swallowed as busy
ok 2530 - L15: a second toggle while one is in flight is swallowed as busy
  ---
  duration_ms: 1.065565
  ...
# Subtest: toggle on a non-link line refuses without writing
ok 2531 - toggle on a non-link line refuses without writing
  ---
  duration_ms: 0.262041
  ...
# Subtest: api.taskLinkLane is a frozen v1 namespace that never throws
ok 2532 - api.taskLinkLane is a frozen v1 namespace that never throws
  ---
  duration_ms: 1.018525
  ...
# Subtest: the progressMarks hint is a no-op without the ledger-tools api
ok 2533 - the progressMarks hint is a no-op without the ledger-tools api
  ---
  duration_ms: 0.317496
  ...
# Subtest: task move records one Vim jump and round-trips without extra writes
ok 2534 - task move records one Vim jump and round-trips without extra writes
  ---
  duration_ms: 10.536511
  ...
# Subtest: counted task move records a single jump to the first moved task
ok 2535 - counted task move records a single jump to the first moved task
  ---
  duration_ms: 1.731096
  ...
# Subtest: deferred task landing re-anchors and records the resolved cursor once
ok 2536 - deferred task landing re-anchors and records the resolved cursor once
  ---
  duration_ms: 5.035607
  ...
# Subtest: failed task move preserves seeded history including the forward branch
ok 2537 - failed task move preserves seeded history including the forward branch
  ---
  duration_ms: 0.617398
  ...
# Subtest: post-commit open failure keeps the move committed with no jump
ok 2538 - post-commit open failure keeps the move committed with no jump
  ---
  duration_ms: 1.191825
  ...
# Subtest: a newer move supersedes a pending landing without stale placement
ok 2539 - a newer move supersedes a pending landing without stale placement
  ---
  duration_ms: 10.753675
  ...
# Subtest: shared destination helper without a move context records no jump
ok 2540 - shared destination helper without a move context records no jump
  ---
  duration_ms: 0.769399
  ...
# Subtest: task moves carry the Depends-On line and repath stranded same-note links
ok 2541 - task moves carry the Depends-On line and repath stranded same-note links
  ---
  duration_ms: 7.911066
  ...
# Subtest: task moves keep pathless links when the target moves along
ok 2542 - task moves keep pathless links when the target moves along
  ---
  duration_ms: 1.518239
  ...
# Subtest: counted task moves discover movable tasks without wrapping or examples
ok 2543 - counted task moves discover movable tasks without wrapping or examples
  ---
  duration_ms: 1.360198
  ...
# Subtest: task move ranges preserve quoted subtrees and collapse overlapping selections
ok 2544 - task move ranges preserve quoted subtrees and collapse overlapping selections
  ---
  duration_ms: 0.702481
  ...
# Subtest: task move removal handles disjoint ranges, blank seams, and CRLF
ok 2545 - task move removal handles disjoint ranges, blank seams, and CRLF
  ---
  duration_ms: 0.460289
  ...
# Subtest: task move destinations include areas and only open projects
ok 2546 - task move destinations include areas and only open projects
  ---
  duration_ms: 0.745614
  ...
# Subtest: moves into a blocked project leave closed tagged lines alone
ok 2547 - moves into a blocked project leave closed tagged lines alone
  ---
  duration_ms: 3.017453
  ...
# Subtest: moves into a blocked project promote open prerequisites to the moved lane
ok 2548 - moves into a blocked project promote open prerequisites to the moved lane
  ---
  duration_ms: 3.371889
  ...
# Subtest: task move insertion preserves exact task and section spacing
ok 2549 - task move insertion preserves exact task and section spacing
  ---
  duration_ms: 2.881262
  ...
# Subtest: task move planning migrates identities and links across every affected note
ok 2550 - task move planning migrates identities and links across every affected note
  ---
  duration_ms: 4.444637
  ...
# Subtest: task move planning exposes a destination anchor for area destinations and counted moves
ok 2551 - task move planning exposes a destination anchor for area destinations and counted moves
  ---
  duration_ms: 0.849572
  ...
# Subtest: task move into a blocked project tags the moved task and consumes today's live Pomodoro link
ok 2552 - task move into a blocked project tags the moved task and consumes today's live Pomodoro link
  ---
  duration_ms: 3.42488
  ...
# Subtest: task move out of a blocked project recovers through the shared gate and writes the unblocked mark
ok 2553 - task move out of a blocked project recovers through the shared gate and writes the unblocked mark
  ---
  duration_ms: 3.777053
  ...
# Subtest: move promotion walks through a ^prj target without raising it
ok 2554 - move promotion walks through a ^prj target without raising it
  ---
  duration_ms: 2.733349
  ...
# Subtest: move promotion walks through a [?] ^prj to its open prerequisite
ok 2555 - move promotion walks through a [?] ^prj to its open prerequisite
  ---
  duration_ms: 1.297278
  ...
# Subtest: move promotion uses each open task's own lane, not the strongest moved lane
ok 2556 - move promotion uses each open task's own lane, not the strongest moved lane
  ---
  duration_ms: 1.524823
  ...
# Subtest: move promotion skips Depends-On lines of closed tasks
ok 2557 - move promotion skips Depends-On lines of closed tasks
  ---
  duration_ms: 0.84831
  ...
# Subtest: task move planning rejects destination collisions and malformed identities
ok 2558 - task move planning rejects destination collisions and malformed identities
  ---
  duration_ms: 0.601739
  ...
# Subtest: resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
ok 2559 - resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks
  ---
  duration_ms: 0.746516
  ...
# Subtest: focusTaskMoveDestination opens the destination file and anchors the cursor
ok 2560 - focusTaskMoveDestination opens the destination file and anchors the cursor
  ---
  duration_ms: 1.220041
  ...
# Subtest: focusTaskMoveDestination returns false without moving the cursor when the open fails
ok 2561 - focusTaskMoveDestination returns false without moving the cursor when the open fails
  ---
  duration_ms: 0.286007
  ...
# Subtest: focusTaskMoveDestination re-anchors by block ID when the destination content drifted
ok 2562 - focusTaskMoveDestination re-anchors by block ID when the destination content drifted
  ---
  duration_ms: 0.290184
  ...
# Subtest: physical task move chord declines auto-repeat and consumes Vim normal input once
ok 2563 - physical task move chord declines auto-repeat and consumes Vim normal input once
  ---
  duration_ms: 0.972156
  ...
# Subtest: counted task move dispatch keeps its count through cold async destinations
ok 2564 - counted task move dispatch keeps its count through cold async destinations
  ---
  duration_ms: 19.471632
  ...
# Subtest: counted task move dispatch with warm async destinations opens one counted picker
ok 2565 - counted task move dispatch with warm async destinations opens one counted picker
  ---
  duration_ms: 6.512547
  ...
# Subtest: bare task move command ignores stale Vim count outside normal mode
ok 2566 - bare task move command ignores stale Vim count outside normal mode
  ---
  duration_ms: 1.289573
  ...
# Subtest: bare task move command opens one uncounted target in Vim normal mode
ok 2567 - bare task move command opens one uncounted target in Vim normal mode
  ---
  duration_ms: 0.687203
  ...
# Subtest: already handled task move event leaves pending Vim state alone
ok 2568 - already handled task move event leaves pending Vim state alone
  ---
  duration_ms: 0.244758
  ...
# Subtest: counted task move command dispatch counts Pomodoro sub-bullets once
ok 2569 - counted task move command dispatch counts Pomodoro sub-bullets once
  ---
  duration_ms: 4.522247
  ...
# Subtest: physical transclusion toggle owns bare and counted Vim normal input
ok 2570 - physical transclusion toggle owns bare and counted Vim normal input
  ---
  duration_ms: 2.464696
  ...
# Subtest: runtime task move writes destination before source and rolls back source failures
ok 2571 - runtime task move writes destination before source and rolls back source failures
  ---
  duration_ms: 3.771893
  ...
# Subtest: runtime task move groups open-editor source and destination changes
ok 2572 - runtime task move groups open-editor source and destination changes
  ---
  duration_ms: 2.539139
  ...
# Subtest: runtime task move guards destination, auxiliary, and rollback failures
ok 2573 - runtime task move guards destination, auxiliary, and rollback failures
  ---
  duration_ms: 2.652696
  ...
# Subtest: task move insertion separates the section's first task from preamble and placeholders
ok 2574 - task move insertion separates the section's first task from preamble and placeholders
  ---
  duration_ms: 0.557254
  ...
# Subtest: task move insertion keeps populated sections compact and second moves stable
ok 2575 - task move insertion keeps populated sections compact and second moves stable
  ---
  duration_ms: 0.254005
  ...
# Subtest: task move planning separates a counted move into a count-only section
ok 2576 - task move planning separates a counted move into a count-only section
  ---
  duration_ms: 0.519241
  ...
# Subtest: runtime counted move into a count-only section focuses the first moved task
ok 2577 - runtime counted move into a count-only section focuses the first moved task
  ---
  duration_ms: 1.341512
  ...
# Subtest: absent local key with folder template writes the trigger and one notice
ok 2578 - absent local key with folder template writes the trigger and one notice
  ---
  duration_ms: 2.444397
  ...
# Subtest: existing local object keeps other keys and only adds the trigger
ok 2579 - existing local object keeps other keys and only adds the trigger
  ---
  duration_ms: 0.435692
  ...
# Subtest: stored true is already-enabled with no write and no notice
ok 2580 - stored true is already-enabled with no write and no notice
  ---
  duration_ms: 0.328397
  ...
# Subtest: stored false is device-opt-out with no write and no notice
ok 2581 - stored false is device-opt-out with no write and no notice
  ---
  duration_ms: 0.20983
  ...
# Subtest: mode none and blank folder templates skip as no-creation-templates
ok 2582 - mode none and blank folder templates skip as no-creation-templates
  ---
  duration_ms: 0.357533
  ...
# Subtest: regex mode with a non-empty file template enables
ok 2583 - regex mode with a non-empty file template enables
  ---
  duration_ms: 0.264715
  ...
# Subtest: legacy settings without a mode key skip as legacy-templater
ok 2584 - legacy settings without a mode key skip as legacy-templater
  ---
  duration_ms: 0.250759
  ...
# Subtest: missing Templater plugin or settings skip as no-templater without throwing
ok 2585 - missing Templater plugin or settings skip as no-templater without throwing
  ---
  duration_ms: 0.364316
  ...
# Subtest: missing loadLocalStorage or saveLocalStorage returns without throwing
ok 2586 - missing loadLocalStorage or saveLocalStorage returns without throwing
  ---
  duration_ms: 0.445471
  ...
# Subtest: string or array stored local values skip as unknown-local-shape
ok 2587 - string or array stored local values skip as unknown-local-shape
  ---
  duration_ms: 0.54987
  ...
# Subtest: saveLocalStorage throw shows one failure notice and does not escape
ok 2588 - saveLocalStorage throw shows one failure notice and does not escape
  ---
  duration_ms: 0.31376
  ...
# Subtest: planTemplaterLocalTrigger covers helper cases and never adds extra keys
ok 2589 - planTemplaterLocalTrigger covers helper cases and never adds extra keys
  ---
  duration_ms: 0.291336
  ...
# Subtest: unblocked model returns null when there is nothing to show
ok 2590 - unblocked model returns null when there is nothing to show
  ---
  duration_ms: 2.080343
  ...
# Subtest: unblocked card renders a single linked row with receipt and chips
ok 2591 - unblocked card renders a single linked row with receipt and chips
  ---
  duration_ms: 2.511326
  ...
# Subtest: unblocked card renders several linked rows with one entry
ok 2592 - unblocked card renders several linked rows with one entry
  ---
  duration_ms: 0.5972
  ...
# Subtest: unblocked card renders a created continuation with next up
ok 2593 - unblocked card renders a created continuation with next up
  ---
  duration_ms: 0.55521
  ...
# Subtest: unblocked card renders recovered-only and still-blocked rows
ok 2594 - unblocked card renders recovered-only and still-blocked rows
  ---
  duration_ms: 1.090483
  ...
# Subtest: current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
ok 2595 - current offer summaries report pulled-in, unselected, mixed destinations, and new reasons
  ---
  duration_ms: 1.273964
  ...
# Subtest: project pull-in rows label empty projects and preserve project blocking reasons
ok 2596 - project pull-in rows label empty projects and preserve project blocking reasons
  ---
  duration_ms: 1.394514
  ...
# Subtest: unblocked card caps visible rows with +N more
ok 2597 - unblocked card caps visible rows with +N more
  ---
  duration_ms: 0.458054
  ...
# Subtest: unblocked card renders the breaker variant
ok 2598 - unblocked card renders the breaker variant
  ---
  duration_ms: 0.736567
  ...
# Subtest: unblocked card renders the failure variant
ok 2599 - unblocked card renders the failure variant
  ---
  duration_ms: 0.755634
  ...
# Subtest: unblocked rows open their task without dismissing the notice
ok 2600 - unblocked rows open their task without dismissing the notice
  ---
  duration_ms: 1.56036
  ...
# Subtest: unblocked row without a block id opens the note path
ok 2601 - unblocked row without a block id opens the note path
  ---
  duration_ms: 0.372662
  ...
# Subtest: unblocked card omits the plan chip when daily content is null
ok 2602 - unblocked card omits the plan chip when daily content is null
  ---
  duration_ms: 0.297338
  ...
# Subtest: unblocked notice shows one card with duration through showNotice
ok 2603 - unblocked notice shows one card with duration through showNotice
  ---
  duration_ms: 0.480809
  ...
# Subtest: unblocked notice falls back to plain text without a DOM
ok 2604 - unblocked notice falls back to plain text without a DOM
  ---
  duration_ms: 0.217626
  ...
# Subtest: unblocked text truncates to 48 characters with an ellipsis
ok 2605 - unblocked text truncates to 48 characters with an ellipsis
  ---
  duration_ms: 0.188871
  ...
# Subtest: nav api exposes additive notice v1 and keeps version 3
ok 2606 - nav api exposes additive notice v1 and keeps version 3
  ---
  duration_ms: 0.657215
  ...
# Subtest: unblocked stylesheet scopes notice overrides and uses task tokens
ok 2607 - unblocked stylesheet scopes notice overrides and uses task tokens
  ---
  duration_ms: 0.79071
  ...
# Subtest: physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
ok 2608 - physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route
  ---
  duration_ms: 3.166998
  ...
# Subtest: open-task command ids omit repeat so the shared route resolves the pending Vim count
ok 2609 - open-task command ids omit repeat so the shared route resolves the pending Vim count
  ---
  duration_ms: 1.474015
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
ok 2610 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move
  ---
  duration_ms: 5.750982
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
ok 2611 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap
  ---
  duration_ms: 0.823774
  ...
# Subtest: command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
ok 2612 - command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump
  ---
  duration_ms: 1.442434
  ...
# Subtest: dispatch guard applies a command-route Vim count when the capture route fires second
ok 2613 - dispatch guard applies a command-route Vim count when the capture route fires second
  ---
  duration_ms: 1.305783
  ...
# Subtest: dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
ok 2614 - dispatch guard leaves pending Vim state untouched when the capture route already consumed the count
  ---
  duration_ms: 0.974461
  ...
# Subtest: command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
ok 2615 - command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state
  ---
  duration_ms: 0.836547
  ...
# Subtest: command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
ok 2616 - command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors
  ---
  duration_ms: 2.800367
  ...
# Subtest: command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
ok 2617 - command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane
  ---
  duration_ms: 1.298791
  ...
# Subtest: explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
ok 2618 - explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count
  ---
  duration_ms: 1.910709
  ...
# Subtest: getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
ok 2619 - getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent
  ---
  duration_ms: 0.370046
  ...
# Subtest: physical counted property chord consumes only explicit normal-mode Vim counts
ok 2620 - physical counted property chord consumes only explicit normal-mode Vim counts
  ---
  duration_ms: 0.575208
  ...
# Subtest: physical counted relation and dependency chords route or refuse by direction
ok 2621 - physical counted relation and dependency chords route or refuse by direction
  ---
  duration_ms: 0.654781
  ...
# Subtest: onload registers the palette command without a default hotkey
ok 2622 - onload registers the palette command without a default hotkey
  ---
  duration_ms: 1.939785
  ...
# Subtest: an embed and a plain image link open the resolved vault resource
ok 2623 - an embed and a plain image link open the resolved vault resource
  ---
  duration_ms: 3.850204
  ...
# Subtest: no image, a missing image, and Reading view show notices without opening
ok 2624 - no image, a missing image, and Reading view show notices without opening
  ---
  duration_ms: 0.532417
  ...
# Subtest: a second command invocation is ignored while the viewer is open
ok 2625 - a second command invocation is ignored while the viewer is open
  ---
  duration_ms: 0.407307
  ...
# Subtest: closing restores focus and leaves an unchanged selection and scroll alone
ok 2626 - closing restores focus and leaves an unchanged selection and scroll alone
  ---
  duration_ms: 0.433979
  ...
# Subtest: closing restores moved selection and scroll only while the source view is active
ok 2627 - closing restores moved selection and scroll only while the source view is active
  ---
  duration_ms: 0.853279
  ...
# Subtest: unload closes the active viewer without restoring editor focus
ok 2628 - unload closes the active viewer without restoring editor focus
  ---
  duration_ms: 0.612529
  ...
# Subtest: parser finds vault embed with size hint
ok 2629 - parser finds vault embed with size hint
  ---
  duration_ms: 2.536544
  ...
# Subtest: parser finds plain image wikilink and blockquoted embed
ok 2630 - parser finds plain image wikilink and blockquoted embed
  ---
  duration_ms: 0.52391
  ...
# Subtest: parser ignores callout bracket and finds the embed
ok 2631 - parser ignores callout bracket and finds the embed
  ---
  duration_ms: 0.571802
  ...
# Subtest: parser ignores image links inside single and double backticks
ok 2632 - parser ignores image links inside single and double backticks
  ---
  duration_ms: 1.148463
  ...
# Subtest: non-image wiki targets are recognized but not candidates
ok 2633 - non-image wiki targets are recognized but not candidates
  ---
  duration_ms: 0.483834
  ...
# Subtest: parser finds two image refs and lines with no refs
ok 2634 - parser finds two image refs and lines with no refs
  ---
  duration_ms: 0.366661
  ...
# Subtest: parser handles Markdown angle, title, and balanced parens
ok 2635 - parser handles Markdown angle, title, and balanced parens
  ---
  duration_ms: 0.641786
  ...
# Subtest: picker uses containing, next, then previous rule
ok 2636 - picker uses containing, next, then previous rule
  ---
  duration_ms: 0.541333
  ...
# Subtest: resolution records sourcePath and resolves duplicate basenames
ok 2637 - resolution records sourcePath and resolves duplicate basenames
  ---
  duration_ms: 1.409101
  ...
# Subtest: resolution handles relative, unicode, and space names
ok 2638 - resolution handles relative, unicode, and space names
  ---
  duration_ms: 0.605856
  ...
# Subtest: missing file, non-image cursor, and fenced lines show exact notices
ok 2639 - missing file, non-image cursor, and fenced lines show exact notices
  ---
  duration_ms: 0.339188
  ...
# Subtest: vault resolution calls getResourcePath with the resolved file
ok 2640 - vault resolution calls getResourcePath with the resolved file
  ---
  duration_ms: 0.406255
  ...
# Subtest: http embed passes through and non-image urls are not candidates
ok 2641 - http embed passes through and non-image urls are not candidates
  ---
  duration_ms: 0.566332
  ...
# Subtest: remote URLs keep original bytes while titles decode once
ok 2642 - remote URLs keep original bytes while titles decode once
  ---
  duration_ms: 0.76948
  ...
# Subtest: escaped Markdown parentheses resolve to the unescaped vault file
ok 2643 - escaped Markdown parentheses resolve to the unescaped vault file
  ---
  duration_ms: 0.317407
  ...
# Subtest: vault percent escapes decode exactly once
ok 2644 - vault percent escapes decode exactly once
  ---
  duration_ms: 0.296456
  ...
# Subtest: extensionless http(s) needs Markdown image syntax
ok 2645 - extensionless http(s) needs Markdown image syntax
  ---
  duration_ms: 0.334389
  ...
# Subtest: fit never exceeds 1 and respects padding for landscape, portrait, and tiny images
ok 2646 - fit never exceeds 1 and respects padding for landscape, portrait, and tiny images
  ---
  duration_ms: 1.339578
  ...
# Subtest: min and max bounds follow fit, 1:1, and the max factor
ok 2647 - min and max bounds follow fit, 1:1, and the max factor
  ---
  duration_ms: 0.219589
  ...
# Subtest: stepping clamps at both bounds
ok 2648 - stepping clamps at both bounds
  ---
  duration_ms: 0.432907
  ...
# Subtest: zoom-at-point keeps the point fixed
ok 2649 - zoom-at-point keeps the point fixed
  ---
  duration_ms: 0.150999
  ...
# Subtest: clamp centres small axes and limits large ones
ok 2650 - clamp centres small axes and limits large ones
  ---
  duration_ms: 0.265928
  ...
# Subtest: key Escape → close
ok 2651 - key Escape → close
  ---
  duration_ms: 0.653859
  ...
# Subtest: key q → close
ok 2652 - key q → close
  ---
  duration_ms: 0.152682
  ...
# Subtest: key Q → close
ok 2653 - key Q → close
  ---
  duration_ms: 0.09409
  ...
# Subtest: key Ctrl+[ → close
ok 2654 - key Ctrl+[ → close
  ---
  duration_ms: 0.326012
  ...
# Subtest: key Z → close
ok 2655 - key Z → close
  ---
  duration_ms: 0.487952
  ...
# Subtest: key + → zoomIn
ok 2656 - key + → zoomIn
  ---
  duration_ms: 0.200683
  ...
# Subtest: key = → zoomIn
ok 2657 - key = → zoomIn
  ---
  duration_ms: 0.127904
  ...
# Subtest: key Shift+= → zoomIn
ok 2658 - key Shift+= → zoomIn
  ---
  duration_ms: 0.102947
  ...
# Subtest: key Shift++ → zoomIn
ok 2659 - key Shift++ → zoomIn
  ---
  duration_ms: 0.164655
  ...
# Subtest: key - → zoomOut
ok 2660 - key - → zoomOut
  ---
  duration_ms: 0.100362
  ...
# Subtest: key 0 → fit
ok 2661 - key 0 → fit
  ---
  duration_ms: 0.158523
  ...
# Subtest: key 1 → actual
ok 2662 - key 1 → actual
  ---
  duration_ms: 0.097005
  ...
# Subtest: key h → pan:left
ok 2663 - key h → pan:left
  ---
  duration_ms: 0.118557
  ...
# Subtest: key j → pan:down
ok 2664 - key j → pan:down
  ---
  duration_ms: 0.089341
  ...
# Subtest: key k → pan:up
ok 2665 - key k → pan:up
  ---
  duration_ms: 0.085183
  ...
# Subtest: key l → pan:right
ok 2666 - key l → pan:right
  ---
  duration_ms: 0.087888
  ...
# Subtest: key Shift+H → pan:left
ok 2667 - key Shift+H → pan:left
  ---
  duration_ms: 0.103107
  ...
# Subtest: key Shift+J → pan:down
ok 2668 - key Shift+J → pan:down
  ---
  duration_ms: 0.097436
  ...
# Subtest: key Shift+K → pan:up
ok 2669 - key Shift+K → pan:up
  ---
  duration_ms: 0.098829
  ...
# Subtest: key Shift+L → pan:right
ok 2670 - key Shift+L → pan:right
  ---
  duration_ms: 0.102956
  ...
# Subtest: key ArrowLeft → pan:left
ok 2671 - key ArrowLeft → pan:left
  ---
  duration_ms: 0.10469
  ...
# Subtest: key ArrowDown → pan:down
ok 2672 - key ArrowDown → pan:down
  ---
  duration_ms: 0.102195
  ...
# Subtest: key ArrowUp → pan:up
ok 2673 - key ArrowUp → pan:up
  ---
  duration_ms: 0.114038
  ...
# Subtest: key ArrowRight → pan:right
ok 2674 - key ArrowRight → pan:right
  ---
  duration_ms: 0.120089
  ...
# Subtest: key Shift+ArrowLeft → pan:left
ok 2675 - key Shift+ArrowLeft → pan:left
  ---
  duration_ms: 0.187828
  ...
# Subtest: key Ctrl+q → ignore
ok 2676 - key Ctrl+q → ignore
  ---
  duration_ms: 0.136992
  ...
# Subtest: key Meta+z → ignore
ok 2677 - key Meta+z → ignore
  ---
  duration_ms: 0.135689
  ...
# Subtest: key Meta+Z → ignore
ok 2678 - key Meta+Z → ignore
  ---
  duration_ms: 0.209379
  ...
# Subtest: key a composing → ignore
ok 2679 - key a composing → ignore
  ---
  duration_ms: 0.128596
  ...
# Subtest: key a keyCode 229 → ignore
ok 2680 - key a keyCode 229 → ignore
  ---
  duration_ms: 0.107947
  ...
# Subtest: key x → ignore
ok 2681 - key x → ignore
  ---
  duration_ms: 0.102486
  ...
# Subtest: keys before arming are ignored
ok 2682 - keys before arming are ignored
  ---
  duration_ms: 1.621136
  ...
# Subtest: Z closes after arming, and a repeated Z does not
ok 2683 - Z closes after arming, and a repeated Z does not
  ---
  duration_ms: 0.608232
  ...
# Subtest: load sets fit state and dimensions
ok 2684 - load sets fit state and dimensions
  ---
  duration_ms: 0.715386
  ...
# Subtest: a load error shows a notice, closes, and calls onClosed once
ok 2685 - a load error shows a notice, closes, and calls onClosed once
  ---
  duration_ms: 0.416586
  ...
# Subtest: Escape closes once, unregisters the scope handler, and aborts the signal
ok 2686 - Escape closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.322887
  ...
# Subtest: q closes once, unregisters the scope handler, and aborts the signal
ok 2687 - q closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.318368
  ...
# Subtest: Q closes once, unregisters the scope handler, and aborts the signal
ok 2688 - Q closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.241872
  ...
# Subtest: Ctrl+[ closes once, unregisters the scope handler, and aborts the signal
ok 2689 - Ctrl+[ closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 1.05284
  ...
# Subtest: Z closes once, unregisters the scope handler, and aborts the signal
ok 2690 - Z closes once, unregisters the scope handler, and aborts the signal
  ---
  duration_ms: 0.379815
  ...
# Subtest: a stray x key changes nothing
ok 2691 - a stray x key changes nothing
  ---
  duration_ms: 0.358274
  ...
# Subtest: the app's vault stubs throw and are never called
ok 2692 - the app's vault stubs throw and are never called
  ---
  duration_ms: 0.325662
  ...
# Subtest: task-card-gate arms only on open inbox tasks
ok 2693 - task-card-gate arms only on open inbox tasks
  ---
  duration_ms: 3.659739
  ...
# Subtest: task-card-gate header shows the Inbox chip only when armed
ok 2694 - task-card-gate header shows the Inbox chip only when armed
  ---
  duration_ms: 6.515515
  ...
# Subtest: task-card-gate priority: cancel writes nothing
ok 2695 - task-card-gate priority: cancel writes nothing
  ---
  duration_ms: 1.189331
  ...
# Subtest: task-card-gate priority: stay runs today's write
ok 2696 - task-card-gate priority: stay runs today's write
  ---
  duration_ms: 0.258273
  ...
# Subtest: task-card-gate priority: move writes then moves
ok 2697 - task-card-gate priority: move writes then moves
  ---
  duration_ms: 0.552305
  ...
# Subtest: task-card-gate scheduled: cancel writes nothing
ok 2698 - task-card-gate scheduled: cancel writes nothing
  ---
  duration_ms: 0.160977
  ...
# Subtest: task-card-gate scheduled: stay runs today's write
ok 2699 - task-card-gate scheduled: stay runs today's write
  ---
  duration_ms: 0.148073
  ...
# Subtest: task-card-gate scheduled: move writes then moves
ok 2700 - task-card-gate scheduled: move writes then moves
  ---
  duration_ms: 0.197387
  ...
# Subtest: task-card-gate generic-property: cancel writes nothing
ok 2701 - task-card-gate generic-property: cancel writes nothing
  ---
  duration_ms: 0.349918
  ...
# Subtest: task-card-gate generic-property: stay runs today's write
ok 2702 - task-card-gate generic-property: stay runs today's write
  ---
  duration_ms: 0.427476
  ...
# Subtest: task-card-gate generic-property: move writes then moves
ok 2703 - task-card-gate generic-property: move writes then moves
  ---
  duration_ms: 0.296026
  ...
# Subtest: task-card-gate refresh-interval: cancel writes nothing
ok 2704 - task-card-gate refresh-interval: cancel writes nothing
  ---
  duration_ms: 0.16767
  ...
# Subtest: task-card-gate refresh-interval: stay runs today's write
ok 2705 - task-card-gate refresh-interval: stay runs today's write
  ---
  duration_ms: 0.125239
  ...
# Subtest: task-card-gate refresh-interval: move writes then moves
ok 2706 - task-card-gate refresh-interval: move writes then moves
  ---
  duration_ms: 0.138134
  ...
# Subtest: task-card-gate refresh-custom: cancel writes nothing
ok 2707 - task-card-gate refresh-custom: cancel writes nothing
  ---
  duration_ms: 0.098148
  ...
# Subtest: task-card-gate refresh-custom: stay runs today's write
ok 2708 - task-card-gate refresh-custom: stay runs today's write
  ---
  duration_ms: 0.110722
  ...
# Subtest: task-card-gate refresh-custom: move writes then moves
ok 2709 - task-card-gate refresh-custom: move writes then moves
  ---
  duration_ms: 0.333356
  ...
# Subtest: task-card-gate clear-priority: cancel writes nothing
ok 2710 - task-card-gate clear-priority: cancel writes nothing
  ---
  duration_ms: 0.137102
  ...
# Subtest: task-card-gate clear-priority: stay runs today's write
ok 2711 - task-card-gate clear-priority: stay runs today's write
  ---
  duration_ms: 0.112946
  ...
# Subtest: task-card-gate clear-priority: move writes then moves
ok 2712 - task-card-gate clear-priority: move writes then moves
  ---
  duration_ms: 0.147491
  ...
# Subtest: task-card-gate recommended-roll: cancel writes nothing
ok 2713 - task-card-gate recommended-roll: cancel writes nothing
  ---
  duration_ms: 0.094901
  ...
# Subtest: task-card-gate recommended-roll: stay runs today's write
ok 2714 - task-card-gate recommended-roll: stay runs today's write
  ---
  duration_ms: 0.100702
  ...
# Subtest: task-card-gate recommended-roll: move writes then moves
ok 2715 - task-card-gate recommended-roll: move writes then moves
  ---
  duration_ms: 0.121562
  ...
# Subtest: task-card-gate recommended-decay: cancel writes nothing
ok 2716 - task-card-gate recommended-decay: cancel writes nothing
  ---
  duration_ms: 0.095042
  ...
# Subtest: task-card-gate recommended-decay: stay runs today's write
ok 2717 - task-card-gate recommended-decay: stay runs today's write
  ---
  duration_ms: 0.095482
  ...
# Subtest: task-card-gate recommended-decay: move writes then moves
ok 2718 - task-card-gate recommended-decay: move writes then moves
  ---
  duration_ms: 0.114559
  ...
# Subtest: task-card-gate counted-roll: cancel writes nothing
ok 2719 - task-card-gate counted-roll: cancel writes nothing
  ---
  duration_ms: 0.138885
  ...
# Subtest: task-card-gate counted-roll: stay runs today's write
ok 2720 - task-card-gate counted-roll: stay runs today's write
  ---
  duration_ms: 0.139446
  ...
# Subtest: task-card-gate counted-roll: move writes then moves
ok 2721 - task-card-gate counted-roll: move writes then moves
  ---
  duration_ms: 0.21479
  ...
# Subtest: task-card-gate lane-toggle: cancel writes nothing
ok 2722 - task-card-gate lane-toggle: cancel writes nothing
  ---
  duration_ms: 0.105081
  ...
# Subtest: task-card-gate lane-toggle: stay runs today's write
ok 2723 - task-card-gate lane-toggle: stay runs today's write
  ---
  duration_ms: 0.105121
  ...
# Subtest: task-card-gate lane-toggle: move writes then moves
ok 2724 - task-card-gate lane-toggle: move writes then moves
  ---
  duration_ms: 0.164744
  ...
# Subtest: task-card-gate dependency-single: cancel writes nothing
ok 2725 - task-card-gate dependency-single: cancel writes nothing
  ---
  duration_ms: 0.097927
  ...
# Subtest: task-card-gate dependency-single: stay runs today's write
ok 2726 - task-card-gate dependency-single: stay runs today's write
  ---
  duration_ms: 0.091235
  ...
# Subtest: task-card-gate dependency-single: move writes then moves
ok 2727 - task-card-gate dependency-single: move writes then moves
  ---
  duration_ms: 0.395355
  ...
# Subtest: task-card-gate dependency-marked: cancel writes nothing
ok 2728 - task-card-gate dependency-marked: cancel writes nothing
  ---
  duration_ms: 0.089601
  ...
# Subtest: task-card-gate dependency-marked: stay runs today's write
ok 2729 - task-card-gate dependency-marked: stay runs today's write
  ---
  duration_ms: 0.089662
  ...
# Subtest: task-card-gate dependency-marked: move writes then moves
ok 2730 - task-card-gate dependency-marked: move writes then moves
  ---
  duration_ms: 0.103348
  ...
# Subtest: task-card-gate dependency-vault: cancel writes nothing
ok 2731 - task-card-gate dependency-vault: cancel writes nothing
  ---
  duration_ms: 0.087427
  ...
# Subtest: task-card-gate dependency-vault: stay runs today's write
ok 2732 - task-card-gate dependency-vault: stay runs today's write
  ---
  duration_ms: 0.087948
  ...
# Subtest: task-card-gate dependency-vault: move writes then moves
ok 2733 - task-card-gate dependency-vault: move writes then moves
  ---
  duration_ms: 0.105572
  ...
# Subtest: task-card-gate dependency-counted: cancel writes nothing
ok 2734 - task-card-gate dependency-counted: cancel writes nothing
  ---
  duration_ms: 0.099229
  ...
# Subtest: task-card-gate dependency-counted: stay runs today's write
ok 2735 - task-card-gate dependency-counted: stay runs today's write
  ---
  duration_ms: 1.526024
  ...
# Subtest: task-card-gate dependency-counted: move writes then moves
ok 2736 - task-card-gate dependency-counted: move writes then moves
  ---
  duration_ms: 0.102787
  ...
# Subtest: task-card-gate negative rows never prompt
ok 2737 - task-card-gate negative rows never prompt
  ---
  duration_ms: 0.730224
  ...
# Subtest: task-card-gate counted sessions capture N targets
ok 2738 - task-card-gate counted sessions capture N targets
  ---
  duration_ms: 0.275466
  ...
# Subtest: task-card-gate walk: move advances once with Moved first
ok 2739 - task-card-gate walk: move advances once with Moved first
  ---
  duration_ms: 0.205592
  ...
# Subtest: task-card-gate walk: move failure falls back to card with partial
ok 2740 - task-card-gate walk: move failure falls back to card with partial
  ---
  duration_ms: 0.398952
  ...
# Subtest: task-card-gate walk: exactly one settle per origin
ok 2741 - task-card-gate walk: exactly one settle per origin
  ---
  duration_ms: 23.471854
  ...
# Subtest: task-card-gate route outcome resolves like lane and link-today
ok 2742 - task-card-gate route outcome resolves like lane and link-today
  ---
  duration_ms: 0.363364
  ...
# Subtest: inbox classifier covers the inbox contract
ok 2743 - inbox classifier covers the inbox contract
  ---
  duration_ms: 1.658126
  ...
# Subtest: isInboxNotePath matches the inbox contract through the vault
ok 2744 - isInboxNotePath matches the inbox contract through the vault
  ---
  duration_ms: 1.18384
  ...
# Subtest: isInboxNotePath is false without an inbox note and never throws
ok 2745 - isInboxNotePath is false without an inbox note and never throws
  ---
  duration_ms: 0.153704
  ...
# Subtest: route destinations drop every inbox note, the source, and templates
ok 2746 - route destinations drop every inbox note, the source, and templates
  ---
  duration_ms: 0.791602
  ...
# Subtest: route preflight accepts a live area destination
ok 2747 - route preflight accepts a live area destination
  ---
  duration_ms: 4.108435
  ...
# Subtest: route preflight refuses stale and colliding destinations
ok 2748 - route preflight refuses stale and colliding destinations
  ---
  duration_ms: 1.568535
  ...
# Subtest: route picker resolves move, stay, cancel, and close exactly once
ok 2749 - route picker resolves move, stay, cancel, and close exactly once
  ---
  duration_ms: 3.376738
  ...
# Subtest: route picker footer names the move, the hatch, and the way back
ok 2750 - route picker footer names the move, the hatch, and the way back
  ---
  duration_ms: 0.527637
  ...
# Subtest: route picker preflight refusal keeps the picker open with a notice
ok 2751 - route picker preflight refusal keeps the picker open with a notice
  ---
  duration_ms: 9.556381
  ...
# Subtest: route picker honors the shared move-picker guard
ok 2752 - route picker honors the shared move-picker guard
  ---
  duration_ms: 2.314551
  ...
# Subtest: promptInboxRoute moves, stays, and cancels with suspend pairing
ok 2753 - promptInboxRoute moves, stays, and cancels with suspend pairing
  ---
  duration_ms: 2.58159
  ...
# Subtest: commitInboxRoute moves the verified task with its children
ok 2754 - commitInboxRoute moves the verified task with its children
  ---
  duration_ms: 3.654368
  ...
# Subtest: commitInboxRoute into a blocked project tags the moved task
ok 2755 - commitInboxRoute into a blocked project tags the moved task
  ---
  duration_ms: 1.862045
  ...
# Subtest: commitInboxRoute moves a counted run and refuses on identity drift
ok 2756 - commitInboxRoute moves a counted run and refuses on identity drift
  ---
  duration_ms: 1.443086
  ...
# Subtest: reviewOutcomeResolves treats route like lane and link-today
ok 2757 - reviewOutcomeResolves treats route like lane and link-today
  ---
  duration_ms: 0.249897
  ...
# Subtest: nav api inboxRoute v1 delegates, shapes, and never throws
ok 2758 - nav api inboxRoute v1 delegates, shapes, and never throws
  ---
  duration_ms: 1.263462
  ...
# Subtest: history records ordered locations with file identity and dedupes adjacent repeats
ok 2759 - history records ordered locations with file identity and dedupes adjacent repeats
  ---
  duration_ms: 1.611928
  ...
# Subtest: transition records origin then destination and truncates forward only on success
ok 2760 - transition records origin then destination and truncates forward only on success
  ---
  duration_ms: 1.025288
  ...
# Subtest: history retains at most 100 locations and refreshes the live tip
ok 2761 - history retains at most 100 locations and refreshes the live tip
  ---
  duration_ms: 0.736356
  ...
# Subtest: rename updates paths and delete prunes without corrupting the index
ok 2762 - rename updates paths and delete prunes without corrupting the index
  ---
  duration_ms: 0.288401
  ...
# Subtest: bridge wraps add once, mirrors native jumps, and preserves the original call
ok 2763 - bridge wraps add once, mirrors native jumps, and preserves the original call
  ---
  duration_ms: 1.867716
  ...
# Subtest: bridge without a jump list preserves keys and emits one compatibility diagnostic
ok 2764 - bridge without a jump list preserves keys and emits one compatibility diagnostic
  ---
  duration_ms: 0.348085
  ...
# Subtest: registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
ok 2765 - registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone
  ---
  duration_ms: 0.346973
  ...
# Subtest: Enter A->B round-trips with Ctrl+O and Ctrl+I
ok 2766 - Enter A->B round-trips with Ctrl+O and Ctrl+I
  ---
  duration_ms: 22.720219
  ...
# Subtest: counted Enter returns to the original cursor, not the counted link line
ok 2767 - counted Enter returns to the original cursor, not the counted link line
  ---
  duration_ms: 21.198974
  ...
# Subtest: picker choice records one jump and cancellation records none
ok 2768 - picker choice records one jump and cancellation records none
  ---
  duration_ms: 22.430273
  ...
# Subtest: stale picker origin is rejected and failed opens record nothing
ok 2769 - stale picker origin is rejected and failed opens record nothing
  ---
  duration_ms: 22.022246
  ...
# Subtest: Backspace shares the link path and no-link lines fall through
ok 2770 - Backspace shares the link path and no-link lines fall through
  ---
  duration_ms: 21.75723
  ...
# Subtest: counted traversal honors boundaries and new jumps replace the forward branch
ok 2771 - counted traversal honors boundaries and new jumps replace the forward branch
  ---
  duration_ms: 0.718873
  ...
# Subtest: ordinary motion before back is preserved for forward restore
ok 2772 - ordinary motion before back is preserved for forward restore
  ---
  duration_ms: 0.319109
  ...
# Subtest: deleted entries are skipped and heading links settle before recording
ok 2773 - deleted entries are skipped and heading links settle before recording
  ---
  duration_ms: 21.949658
  ...
# Subtest: native fallback runs with empty history and boundaries never replay natives
ok 2774 - native fallback runs with empty history and boundaries never replay natives
  ---
  duration_ms: 0.890211
  ...
# Subtest: unload restores the native add and keeps a foreign later mapping
ok 2775 - unload restores the native add and keeps a foreign later mapping
  ---
  duration_ms: 0.614243
  ...
# Subtest: exact eligibility authorizes one due-Ready ROTTEN row
ok 2776 - exact eligibility authorizes one due-Ready ROTTEN row
  ---
  duration_ms: 1.385115
  ...
# Subtest: exact eligibility authorizes a TICKLER row
ok 2777 - exact eligibility authorizes a TICKLER row
  ---
  duration_ms: 0.188019
  ...
# Subtest: exact eligibility refuses every stale-cache shape
ok 2778 - exact eligibility refuses every stale-cache shape
  ---
  duration_ms: 0.477121
  ...
# Subtest: exact eligibility refuses non-Ready and non-due rows
ok 2779 - exact eligibility refuses non-Ready and non-due rows
  ---
  duration_ms: 0.257772
  ...
# Subtest: legacy refs still match line-only while exact refuses
ok 2780 - legacy refs still match line-only while exact refuses
  ---
  duration_ms: 0.534661
  ...
# Subtest: keeps support needs namespace v5 with keepLine
ok 2781 - keeps support needs namespace v5 with keepLine
  ---
  duration_ms: 0.164273
  ...
# Subtest: decay decisions need namespace v6 with keepLine
ok 2782 - decay decisions need namespace v6 with keepLine
  ---
  duration_ms: 0.195052
  ...
# Subtest: batch forwards per-target counted decisions to the stamper
ok 2783 - batch forwards per-target counted decisions to the stamper
  ---
  duration_ms: 1.211304
  ...
# Subtest: batch keeps legacy index targets uncounted
ok 2784 - batch keeps legacy index targets uncounted
  ---
  duration_ms: 0.387961
  ...
# Subtest: a throwing stamper refuses the batch with no partial write
ok 2785 - a throwing stamper refuses the batch with no partial write
  ---
  duration_ms: 0.528048
  ...
# Subtest: parseKeepsCount reads the first valid value only
ok 2786 - parseKeepsCount reads the first valid value only
  ---
  duration_ms: 0.313759
  ...
# Subtest: countFreshStampKept measures actual increments only
ok 2787 - countFreshStampKept measures actual increments only
  ---
  duration_ms: 0.184703
  ...
# Subtest: fresh stamp notice tails kept increments without promises
ok 2788 - fresh stamp notice tails kept increments without promises
  ---
  duration_ms: 0.212636
  ...
# Subtest: duplicate source targets dedupe to one write
ok 2789 - duplicate source targets dedupe to one write
  ---
  duration_ms: 0.174443
  ...
# Subtest: single Alt+F increments an exact due-Ready ROTTEN task
ok 2790 - single Alt+F increments an exact due-Ready ROTTEN task
  ---
  duration_ms: 7.85014
  ...
# Subtest: single Alt+F preserves NEW, lane, and early tasks without counting
ok 2791 - single Alt+F preserves NEW, lane, and early tasks without counting
  ---
  duration_ms: 2.175535
  ...
# Subtest: same-day repeat stays identical and counts nothing
ok 2792 - same-day repeat stays identical and counts nothing
  ---
  duration_ms: 0.547566
  ...
# Subtest: Pending Alt+F writes its summary with the stamp in one edit
ok 2793 - Pending Alt+F writes its summary with the stamp in one edit
  ---
  duration_ms: 1.007144
  ...
# Subtest: counted Pending refresh shares one summary only with Pending targets
ok 2794 - counted Pending refresh shares one summary only with Pending targets
  ---
  duration_ms: 0.950675
  ...
# Subtest: a refusing counted target refuses before the Pending Work Log prompt
ok 2795 - a refusing counted target refuses before the Pending Work Log prompt
  ---
  duration_ms: 0.352734
  ...
# Subtest: blank Pending refresh advances; cancelled or stale prompts write nothing
ok 2796 - blank Pending refresh advances; cancelled or stale prompts write nothing
  ---
  duration_ms: 1.429821
  ...
# Subtest: stale queue match stamps uncounted and never inflates
ok 2797 - stale queue match stamps uncounted and never inflates
  ---
  duration_ms: 0.606388
  ...
# Subtest: counted Alt+F increments every exact target once
ok 2798 - counted Alt+F increments every exact target once
  ---
  duration_ms: 1.829014
  ...
# Subtest: stale editor source refuses with no write
ok 2799 - stale editor source refuses with no write
  ---
  duration_ms: 0.379635
  ...
# Subtest: single-note write lands in one editor transaction and keeps CRLF
ok 2800 - single-note write lands in one editor transaction and keeps CRLF
  ---
  duration_ms: 0.716499
  ...
# Subtest: v5 without keepLine fails without writing
ok 2801 - v5 without keepLine fails without writing
  ---
  duration_ms: 0.16267
  ...
# Subtest: throwing v5 keepLine refuses the batch with no partial write
ok 2802 - throwing v5 keepLine refuses the batch with no partial write
  ---
  duration_ms: 0.411576
  ...
# Subtest: pre-v5 ledger stamps uncounted through the old stamper
ok 2803 - pre-v5 ledger stamps uncounted through the old stamper
  ---
  duration_ms: 0.485838
  ...
# Subtest: Task Link session skips an at-limit decide target
ok 2804 - Task Link session skips an at-limit decide target
  ---
  duration_ms: 2.385956
  ...
# Subtest: Task Link refresh counts one exact target
ok 2805 - Task Link refresh counts one exact target
  ---
  duration_ms: 1.528609
  ...
# Subtest: duplicate Task Links to one target stamp and count once
ok 2806 - duplicate Task Links to one target stamp and count once
  ---
  duration_ms: 3.318106
  ...
# Subtest: counted Task Link sessions combine Pending work and Rotten keep logs
ok 2807 - counted Task Link sessions combine Pending work and Rotten keep logs
  ---
  duration_ms: 2.012152
  ...
# Subtest: counted Task Links dedupe targets and log only the Pending target
ok 2808 - counted Task Links dedupe targets and log only the Pending target
  ---
  duration_ms: 1.138163
  ...
# Subtest: multi-note stale preimage refuses with no writes
ok 2809 - multi-note stale preimage refuses with no writes
  ---
  duration_ms: 0.767896
  ...
# Subtest: a linked note changed during the Keep prompt refuses before any write
ok 2810 - a linked note changed during the Keep prompt refuses before any write
  ---
  duration_ms: 0.682984
  ...
# Subtest: multi-note write failure rolls back the first note
ok 2811 - multi-note write failure rolls back the first note
  ---
  duration_ms: 1.737638
  ...
# Subtest: partial rollback is reported and a same-day retry does not duplicate the logged keep
ok 2812 - partial rollback is reported and a same-day retry does not duplicate the logged keep
  ---
  duration_ms: 2.851515
  ...
# Subtest: one physical key through two routes stamps once
ok 2813 - one physical key through two routes stamps once
  ---
  duration_ms: 1.470918
  ...
# Subtest: Ctrl+Alt+F capture advances once and consumes a Vim prefix
ok 2814 - Ctrl+Alt+F capture advances once and consumes a Vim prefix
  ---
  duration_ms: 0.951417
  ...
# Subtest: obsolete and extra-modifier F chords stay unconsumed
ok 2815 - obsolete and extra-modifier F chords stay unconsumed
  ---
  duration_ms: 0.255087
  ...
# Subtest: live Ctrl+Alt+F double dispatch asks once on a Pending task
ok 2816 - live Ctrl+Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.559349
  ...
# Subtest: live Alt+F double dispatch asks once on a Pending task
ok 2817 - live Alt+F double dispatch asks once on a Pending task
  ---
  duration_ms: 0.559107
  ...
# Subtest: already-handled refresh keydown leaves Vim state alone
ok 2818 - already-handled refresh keydown leaves Vim state alone
  ---
  duration_ms: 0.196355
  ...
# Subtest: parseBobOpenNotesParams accepts indexed entries and ignores unknown keys
ok 2819 - parseBobOpenNotesParams accepts indexed entries and ignores unknown keys
  ---
  duration_ms: 2.442434
  ...
# Subtest: parseBobOpenNotesParams rejects every malformed URI field
ok 2820 - parseBobOpenNotesParams rejects every malformed URI field
  ---
  duration_ms: 0.547706
  ...
# Subtest: invalid batches show one notice and open nothing
ok 2821 - invalid batches show one notice and open nothing
  ---
  duration_ms: 1.334269
  ...
# Subtest: path mapping follows a symlink realpath into the vault
ok 2822 - path mapping follows a symlink realpath into the vault
  ---
  duration_ms: 3.982617
  ...
# Subtest: new-tab policy reuses existing tabs and the active empty tab, keeping order and primary active
ok 2823 - new-tab policy reuses existing tabs and the active empty tab, keeping order and primary active
  ---
  duration_ms: 1.718933
  ...
# Subtest: an absent or outside entry fails independently and a PDF opens without landing
ok 2824 - an absent or outside entry fails independently and a PDF opens without landing
  ---
  duration_ms: 2000.392146
  ...
# Subtest: a resolved note that is not open waits until its captured digest is cached
ok 2825 - a resolved note that is not open waits until its captured digest is cached
  ---
  duration_ms: 63.207245
  ...
# Subtest: a per-entry open failure does not prevent later notes from opening
ok 2826 - a per-entry open failure does not prevent later notes from opening
  ---
  duration_ms: 0.777454
  ...
# Subtest: waits for a newly created vault file and a late visible line digest
ok 2827 - waits for a newly created vault file and a late visible line digest
  ---
  duration_ms: 61.001644
  ...
# Subtest: re-finds a moved digest on any line, including prose and Pomodoro rows
ok 2828 - re-finds a moved digest on any line, including prose and Pomodoro rows
  ---
  duration_ms: 0.890871
  ...
# Subtest: deadline fallback opens near the planned line and reports a changed capture
ok 2829 - deadline fallback opens near the planned line and reports a changed capture
  ---
  duration_ms: 2001.250085
  ...
# Subtest: truncation reports how many of the full list opened
ok 2830 - truncation reports how many of the full list opened
  ---
  duration_ms: 0.816569
  ...
# Subtest: serializes quick URLs and leaves the later URL active
ok 2831 - serializes quick URLs and leaves the later URL active
  ---
  duration_ms: 1.975113
  ...
# Subtest: primary landing flashes briefly, secondary landings do not, and the handler is read-only
ok 2832 - primary landing flashes briefly, secondary landings do not, and the handler is read-only
  ---
  duration_ms: 17.423512
  ...
# Subtest: onload registers bob-open-notes beside bob-goto-task
ok 2833 - onload registers bob-open-notes beside bob-goto-task
  ---
  duration_ms: 1.681381
  ...
# Subtest: a non-file sidebar view is not reused as an empty tab
ok 2834 - a non-file sidebar view is not reused as an empty tab
  ---
  duration_ms: 0.635925
  ...
# Subtest: a true empty tab is reused for the first entry
ok 2835 - a true empty tab is reused for the first entry
  ---
  duration_ms: 0.304441
  ...
# Subtest: three new tabs follow entry order in the tab strip
ok 2836 - three new tabs follow entry order in the tab strip
  ---
  duration_ms: 0.592472
  ...
# Subtest: two tabs of the same note reuse the first matching leaf
ok 2837 - two tabs of the same note reuse the first matching leaf
  ---
  duration_ms: 0.297338
  ...
# Subtest: a missing file does not scan vault lists when getAbstractFileByPath exists
ok 2838 - a missing file does not scan vault lists when getAbstractFileByPath exists
  ---
  duration_ms: 2000.668974
  ...
# Subtest: new tabs append at the far right when the middle tab is active
ok 2839 - new tabs append at the far right when the middle tab is active
  ---
  duration_ms: 0.889649
  ...
# Subtest: a reused tab stays put while a new one is appended
ok 2840 - a reused tab stays put while a new one is appended
  ---
  duration_ms: 0.369555
  ...
# Subtest: a deferred tab is reused and findMarkdownLeafByPath sees it
ok 2841 - a deferred tab is reused and findMarkdownLeafByPath sees it
  ---
  duration_ms: 0.47645
  ...
# Subtest: a deferred sidebar leaf whose saved state names the note is not reused
ok 2842 - a deferred sidebar leaf whose saved state names the note is not reused
  ---
  duration_ms: 0.451403
  ...
# Subtest: a loaded main-area match beats an earlier loaded sidebar match
ok 2843 - a loaded main-area match beats an earlier loaded sidebar match
  ---
  duration_ms: 0.25662
  ...
# Subtest: a new tab goes to the end of the main group when a sidebar leaf is active
ok 2844 - a new tab goes to the end of the main group when a sidebar leaf is active
  ---
  duration_ms: 0.285726
  ...
# Subtest: falling back without createLeafInParent still opens a new tab
ok 2845 - falling back without createLeafInParent still opens a new tab
  ---
  duration_ms: 0.279584
  ...
# Subtest: falling back when createLeafInParent throws still opens a new tab
ok 2846 - falling back when createLeafInParent throws still opens a new tab
  ---
  duration_ms: 0.307758
  ...
# Subtest: collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
ok 2847 - collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks
  ---
  duration_ms: 3.682372
  ...
# Subtest: getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
ok 2848 - getProjectBlockState recognizes a project from type/status and ignores YAML scheduled
  ---
  duration_ms: 3.25747
  ...
# Subtest: getProjectBlockState reports an open external prerequisite
ok 2849 - getProjectBlockState reports an open external prerequisite
  ---
  duration_ms: 0.900379
  ...
# Subtest: getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
ok 2850 - getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled
  ---
  duration_ms: 0.805448
  ...
# Subtest: getProjectBlockState scheduledValue override is the inline date, not frontmatter
ok 2851 - getProjectBlockState scheduledValue override is the inline date, not frontmatter
  ---
  duration_ms: 0.556884
  ...
# Subtest: getProjectBlockState skips internal and archive Depends-On links
ok 2852 - getProjectBlockState skips internal and archive Depends-On links
  ---
  duration_ms: 0.43499
  ...
# Subtest: getProjectBlockState is a no-op for terminal, daily, and non-project notes
ok 2853 - getProjectBlockState is a no-op for terminal, daily, and non-project notes
  ---
  duration_ms: 0.789768
  ...
# Subtest: projectLooksBlockedByPrjShortcut is the single [?] ^prj row
ok 2854 - projectLooksBlockedByPrjShortcut is the single [?] ^prj row
  ---
  duration_ms: 0.303971
  ...
# Subtest: taskHasProjectBlockedTag is token-bounded and does not match \#prj
ok 2855 - taskHasProjectBlockedTag is token-bounded and does not match \#prj
  ---
  duration_ms: 0.49732
  ...
# Subtest: setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
ok 2856 - setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips
  ---
  duration_ms: 1.129377
  ...
# Subtest: reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
ok 2857 - reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries
  ---
  duration_ms: 0.60712
  ...
# Subtest: reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
ok 2858 - reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending
  ---
  duration_ms: 0.371048
  ...
# Subtest: reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
ok 2859 - reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing
  ---
  duration_ms: 0.238225
  ...
# Subtest: ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
ok 2860 - ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps
  ---
  duration_ms: 7.12591
  ...
# Subtest: recovery gate keeps a resident of a blocked project blocked after own deps close
ok 2861 - recovery gate keeps a resident of a blocked project blocked after own deps close
  ---
  duration_ms: 2.692682
  ...
# Subtest: recovery gate blocks residents on a future inline project date with no deps
ok 2862 - recovery gate blocks residents on a future inline project date with no deps
  ---
  duration_ms: 0.426194
  ...
# Subtest: planDeferredPomodoroLinkCleanup always deletes a last-child open entry
ok 2863 - planDeferredPomodoroLinkCleanup always deletes a last-child open entry
  ---
  duration_ms: 1.608211
  ...
# Subtest: TICKLER notice uses unblocked <date> when returnedBy is unblocked
ok 2864 - TICKLER notice uses unblocked <date> when returnedBy is unblocked
  ---
  duration_ms: 0.426264
  ...
# Subtest: recognition: a `^prj` parent in a project note carries its residents
ok 2865 - recognition: a `^prj` parent in a project note carries its residents
  ---
  duration_ms: 3.89049
  ...
# Subtest: recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
ok 2866 - recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits
  ---
  duration_ms: 0.597993
  ...
# Subtest: add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
ok 2867 - add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7)
  ---
  duration_ms: 7.645631
  ...
# Subtest: add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
ok 2868 - add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11)
  ---
  duration_ms: 4.26803
  ...
# Subtest: guards: a same-note add to `^prj` refuses, including mixed batches
ok 2869 - guards: a same-note add to `^prj` refuses, including mixed batches
  ---
  duration_ms: 1.267009
  ...
# Subtest: guards: the stage disables same-note rows for `^prj` with `inside this project`
ok 2870 - guards: the stage disables same-note rows for `^prj` with `inside this project`
  ---
  duration_ms: 1.768507
  ...
# Subtest: guards: cycle detection includes the implicit resident edges (§13.6)
ok 2871 - guards: cycle detection includes the implicit resident edges (§13.6)
  ---
  duration_ms: 2.041369
  ...
# Subtest: removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
ok 2872 - removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4)
  ---
  duration_ms: 5.757696
  ...
# Subtest: removal: a resident with its own reason stays `[?]` without the tag (PDB3)
ok 2873 - removal: a resident with its own reason stays `[?]` without the tag (PDB3)
  ---
  duration_ms: 2.328888
  ...
# Subtest: removal without a registry defers to reconcile: residents keep `[?]` and the tag
ok 2874 - removal without a registry defers to reconcile: residents keep `[?]` and the tag
  ---
  duration_ms: 1.794748
  ...
# Subtest: writer: one gesture commits `^prj` and its residents in a single undo group
ok 2875 - writer: one gesture commits `^prj` and its residents in a single undo group
  ---
  duration_ms: 1.378252
  ...
# Subtest: writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
ok 2876 - writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries
  ---
  duration_ms: 3.261498
  ...
# Subtest: notices: the project strings name the task, the flips, and the Pomodoro cleanup
ok 2877 - notices: the project strings name the task, the flips, and the Pomodoro cleanup
  ---
  duration_ms: 0.623491
  ...
# Subtest: mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
ok 2878 - mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces
  ---
  duration_ms: 0.325982
  ...
# Subtest: api v3: removeDependencyByRef delegates removals to the single-transaction writer
ok 2879 - api v3: removeDependencyByRef delegates removals to the single-transaction writer
  ---
  duration_ms: 0.963901
  ...
# Subtest: api v3: openDependencyStageForRef opens the Depends on stage on the owning task
ok 2880 - api v3: openDependencyStageForRef opens the Depends on stage on the owning task
  ---
  duration_ms: 0.333497
  ...
# Subtest: internal links stay on the line but leave the field (PDR7)
ok 2881 - internal links stay on the line but leave the field (PDR7)
  ---
  duration_ms: 0.913614
  ...
# Subtest: removal from an unblocked ^prj never recovers own-reason residents (§13.10)
ok 2882 - removal from an unblocked ^prj never recovers own-reason residents (§13.10)
  ---
  duration_ms: 0.524472
  ...
# Subtest: resident recovery touches only tagged residents (§13.10)
ok 2883 - resident recovery touches only tagged residents (§13.10)
  ---
  duration_ms: 2.499303
  ...
# Subtest: stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
ok 2884 - stage guard refuses a candidate that closes a cycle through a resident edge (§13.10)
  ---
  duration_ms: 0.909928
  ...
# Subtest: projectDependentResidentKeys lists open residents with block ids
ok 2885 - projectDependentResidentKeys lists open residents with block ids
  ---
  duration_ms: 0.406947
  ...
# Subtest: navNoteScopeFlags marks daily notes; a missing writer stays null
ok 2886 - navNoteScopeFlags marks daily notes; a missing writer stays null
  ---
  duration_ms: 0.289322
  ...
# Subtest: reconcileBlockedScheduledTaskLine forwards scope flags to the writer
ok 2887 - reconcileBlockedScheduledTaskLine forwards scope flags to the writer
  ---
  duration_ms: 0.199601
  ...
# Subtest: parseProjectNoteFrontmatter ignores leftover scheduled keys
ok 2888 - parseProjectNoteFrontmatter ignores leftover scheduled keys
  ---
  duration_ms: 0.594656
  ...
# Subtest: formatTaskMoveProjectCountsNotice names blocked and recovered counts
ok 2889 - formatTaskMoveProjectCountsNotice names blocked and recovered counts
  ---
  duration_ms: 0.175906
  ...
# Subtest: PDS15: projectParentTarget keeps the path and drops alias and heading
ok 2890 - PDS15: projectParentTarget keeps the path and drops alias and heading
  ---
  duration_ms: 1.190203
  ...
# Subtest: PDS6: list-form, missing, and non-wikilink parents yield none
ok 2891 - PDS6: list-form, missing, and non-wikilink parents yield none
  ---
  duration_ms: 0.46613
  ...
# Subtest: PDS15: resolveProjectParentPath accepts alias, path, and heading forms
ok 2892 - PDS15: resolveProjectParentPath accepts alias, path, and heading forms
  ---
  duration_ms: 0.436704
  ...
# Subtest: PDS6: self, unresolved, and ambiguous basenames yield no parent
ok 2893 - PDS6: self, unresolved, and ambiguous basenames yield no parent
  ---
  duration_ms: 0.169824
  ...
# Subtest: buildProjectChildrenMap and descendants BFS skip cycles and cap depth
ok 2894 - buildProjectChildrenMap and descendants BFS skip cycles and cap depth
  ---
  duration_ms: 2.565318
  ...
# Subtest: PDS6: area, terminal, daily, and self-parent notes are not children
ok 2895 - PDS6: area, terminal, daily, and self-parent notes are not children
  ---
  duration_ms: 0.378904
  ...
# Subtest: PDG8: planner blocks child and grandchild ^prj and residents
ok 2896 - PDG8: planner blocks child and grandchild ^prj and residents
  ---
  duration_ms: 2.673425
  ...
# Subtest: PDG9: planner recovers tagged descendants with [unblocked::]
ok 2897 - PDG9: planner recovers tagged descendants with [unblocked::]
  ---
  duration_ms: 1.480788
  ...
# Subtest: PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
ok 2898 - PDG10: child with its own open target keeps residents tagged; grandchild stays inherited
  ---
  duration_ms: 1.929634
  ...
# Subtest: PDG11: a tagged root re-asserts descendant tags and recovers nothing
ok 2899 - PDG11: a tagged root re-asserts descendant tags and recovers nothing
  ---
  duration_ms: 0.893937
  ...
# Subtest: tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
ok 2900 - tag proxy: getProjectBlockState reports project_parent when ^prj is tagged
  ---
  duration_ms: 0.279113
  ...
# Subtest: tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
ok 2901 - tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj
  ---
  duration_ms: 1.700317
  ...
# Subtest: tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
ok 2902 - tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj
  ---
  duration_ms: 0.219469
  ...
# Subtest: tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
ok 2903 - tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents
  ---
  duration_ms: 2.127883
  ...
# Subtest: PDG13: failProjectPrjInternalAdd refuses descendant targets
ok 2904 - PDG13: failProjectPrjInternalAdd refuses descendant targets
  ---
  duration_ms: 0.263774
  ...
# Subtest: PDG13: planDependencyEdit refuses a descendant add from the files map
ok 2905 - PDG13: planDependencyEdit refuses a descendant add from the files map
  ---
  duration_ms: 1.61297
  ...
# Subtest: PDG13: the stage disables descendant rows
ok 2906 - PDG13: the stage disables descendant rows
  ---
  duration_ms: 1.262029
  ...
# Subtest: reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
ok 2907 - reversal: parseProjectLifecycleTaskBody strips \#prj_is_blocked
  ---
  duration_ms: 0.35596
  ...
# Subtest: tag proxy: removing the last own dep of a tagged ^prj recovers nobody
ok 2908 - tag proxy: removing the last own dep of a tagged ^prj recovers nobody
  ---
  duration_ms: 2.771954
  ...
# Subtest: PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
ok 2909 - PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links
  ---
  duration_ms: 29.721389
  ...
# Subtest: PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
ok 2910 - PDG9: removing the last open Depends on target recovers descendants with unblocked stamps
  ---
  duration_ms: 8.244223
  ...
# Subtest: PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
ok 2911 - PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged
  ---
  duration_ms: 5.361879
  ...
# Subtest: PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
ok 2912 - PDG11: a tagged root gesture reasserts descendant tags and recovers nothing
  ---
  duration_ms: 5.080202
  ...
# Subtest: PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
ok 2913 - PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links
  ---
  duration_ms: 7.341782
  ...
# Subtest: PDG12: moving the project date due recovers descendants
ok 2914 - PDG12: moving the project date due recovers descendants
  ---
  duration_ms: 7.661099
  ...
# Subtest: PDG12: deleting the project date recovers descendants
ok 2915 - PDG12: deleting the project date recovers descendants
  ---
  duration_ms: 4.869749
  ...
# Subtest: PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
ok 2916 - PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes
  ---
  duration_ms: 6.936827
  ...
# Subtest: PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
ok 2917 - PDG14: a stale descendant is skipped, the root write stands, and the notice reports it
  ---
  duration_ms: 4.069463
  ...
# Subtest: Task Link Depends on writer preserves the internal-target guard on a project task
ok 2918 - Task Link Depends on writer preserves the internal-target guard on a project task
  ---
  duration_ms: 0.872086
  ...
# Subtest: api v3 removeDependencyByRef runs the recovery cascade for a linked project task
ok 2919 - api v3 removeDependencyByRef runs the recovery cascade for a linked project task
  ---
  duration_ms: 3.982856
  ...
# Subtest: counted Schedule writer cascades a future date through descendants
ok 2920 - counted Schedule writer cascades a future date through descendants
  ---
  duration_ms: 4.568063
  ...
# Subtest: counted subtree roots are ancestor-first and each descendant note is planned once
ok 2921 - counted subtree roots are ancestor-first and each descendant note is planned once
  ---
  duration_ms: 2.015739
  ...
# Subtest: Ctrl+D on the Depends on row removes the line and recovers the subtree
ok 2922 - Ctrl+D on the Depends on row removes the line and recovers the subtree
  ---
  duration_ms: 3.557634
  ...
# Subtest: a ^prj with no children reads no other note
ok 2923 - a ^prj with no children reads no other note
  ---
  duration_ms: 0.232595
  ...
# Subtest: single seeds from raw text, not display decorations
ok 2924 - single seeds from raw text, not display decorations
  ---
  duration_ms: 10.514859
  ...
# Subtest: legacy valid free wins; invalid and taken fall through
ok 2925 - legacy valid free wins; invalid and taken fall through
  ---
  duration_ms: 1.441483
  ...
# Subtest: batch reserves suffixes for two same-text tasks
ok 2926 - batch reserves suffixes for two same-text tasks
  ---
  duration_ms: 0.896062
  ...
# Subtest: counted-source, vault-single, and vault-counted seed per mode
ok 2927 - counted-source, vault-single, and vault-counted seed per mode
  ---
  duration_ms: 1.102165
  ...
# Subtest: cross-note uses the target note, never the dependent fallback
ok 2928 - cross-note uses the target note, never the dependent fallback
  ---
  duration_ms: 1.196916
  ...
# Subtest: staging writes nothing until confirmed
ok 2929 - staging writes nothing until confirmed
  ---
  duration_ms: 0.713072
  ...
# Subtest: the shared planner matches the Task Card recommendation
ok 2930 - the shared planner matches the Task Card recommendation
  ---
  duration_ms: 31.579126
  ...
# Subtest: the preview table strings are exact
ok 2931 - the preview table strings are exact
  ---
  duration_ms: 1.109689
  ...
# Subtest: checklist tiers and unpreviewable rows report ok:false
ok 2932 - checklist tiers and unpreviewable rows report ok:false
  ---
  duration_ms: 0.469607
  ...
# Subtest: a silent config failure reports ok:false with no Notice
ok 2933 - a silent config failure reports ok:false with no Notice
  ---
  duration_ms: 0.148323
  ...
# Subtest: landing toasts append the preview after tails
ok 2934 - landing toasts append the preview after tails
  ---
  duration_ms: 0.903445
  ...
# Subtest: api.quickRoll has the v1 shape and never throws
ok 2935 - api.quickRoll has the v1 shape and never throws
  ---
  duration_ms: 1.42434
  ...
# Subtest: the preview matches what Alt+P then writes
ok 2936 - the preview matches what Alt+P then writes
  ---
  duration_ms: 18.813579
  ...
# Subtest: Alt+P matches Ctrl+Enter for roll, decay, project, and counted task writes
ok 2937 - Alt+P matches Ctrl+Enter for roll, decay, project, and counted task writes
  ---
  duration_ms: 53.992109
  ...
# Subtest: Alt+P matches Ctrl+Enter for a counted Task Link batch
ok 2938 - Alt+P matches Ctrl+Enter for a counted Task Link batch
  ---
  duration_ms: 16.75067
  ...
# Subtest: Task Link resolution keeps the outer modal hidden until its targets are ready
ok 2939 - Task Link resolution keeps the outer modal hidden until its targets are ready
  ---
  duration_ms: 5.020216
  ...
# Subtest: Alt+P hides immediate rolls and reveals the optional Next Work summary
ok 2940 - Alt+P hides immediate rolls and reveals the optional Next Work summary
  ---
  duration_ms: 12.602325
  ...
# Subtest: a cancel recommendation waits for the visible card and the second Alt+P cancels
ok 2941 - a cancel recommendation waits for the visible card and the second Alt+P cancels
  ---
  duration_ms: 6.502961
  ...
# Subtest: no priority and unavailable recurring tasks reveal the card without writing
ok 2942 - no priority and unavailable recurring tasks reveal the card without writing
  ---
  duration_ms: 2.707231
  ...
# Subtest: inbox routing is shown before the write and a managed line redirects to its owner
ok 2943 - inbox routing is shown before the write and a managed line redirects to its owner
  ---
  duration_ms: 7.292967
  ...
# Subtest: a landed review row advances once after Alt+P writes
ok 2944 - a landed review row advances once after Alt+P writes
  ---
  duration_ms: 4.277929
  ...
# Subtest: the card alias uses the physical Alt+P code and ignores repeats
ok 2945 - the card alias uses the physical Alt+P code and ignores repeats
  ---
  duration_ms: 2.617388
  ...
# Subtest: a throwing one-shot dispatch always reveals the still-open card
ok 2946 - a throwing one-shot dispatch always reveals the still-open card
  ---
  duration_ms: 3.163171
  ...
# Subtest: the registered command owns Alt+P and a Vim count is consumed once
ok 2947 - the registered command owns Alt+P and a Vim count is consumed once
  ---
  duration_ms: 2.979259
  ...
# Subtest: quick-roll visibility CSS disables the modal entrance animation
ok 2948 - quick-roll visibility CSS disables the modal entrance animation
  ---
  duration_ms: 0.855794
  ...
# Subtest: Less often picker renders actual rows from 90 days and Escape writes nothing
ok 2949 - Less often picker renders actual rows from 90 days and Escape writes nothing
  ---
  duration_ms: 7.948159
  ...
# Subtest: Less often picker renders actual rows from 120 days and Escape writes nothing
ok 2950 - Less often picker renders actual rows from 120 days and Escape writes nothing
  ---
  duration_ms: 0.894779
  ...
# Subtest: Less often picker renders actual rows from 180 days and Escape writes nothing
ok 2951 - Less often picker renders actual rows from 180 days and Escape writes nothing
  ---
  duration_ms: 0.505496
  ...
# Subtest: renderFooter skips malformed hints and retains valid structured hints
ok 2952 - renderFooter skips malformed hints and retains valid structured hints
  ---
  duration_ms: 0.269255
  ...
# Subtest: Pending refresh modal previews the dated Work Log and confirms once
ok 2953 - Pending refresh modal previews the dated Work Log and confirms once
  ---
  duration_ms: 1.561042
  ...
# Subtest: dismissing the Pending refresh modal cancels without a summary
ok 2954 - dismissing the Pending refresh modal cancels without a summary
  ---
  duration_ms: 0.324489
  ...
# Subtest: nav LK1–LK18 parse relation grammar and reject the other relation parser
ok 2955 - nav LK1–LK18 parse relation grammar and reject the other relation parser
  ---
  duration_ms: 4.260916
  ...
# Subtest: nav LK14–LK19 context and cross-parse rules
ok 2956 - nav LK14–LK19 context and cross-parse rules
  ---
  duration_ms: 0.880762
  ...
# Subtest: nav MC5 refuses relation embeds and MC16 keeps LINKS while dropping LINKED FROM
ok 2957 - nav MC5 refuses relation embeds and MC16 keeps LINKS while dropping LINKED FROM
  ---
  duration_ms: 2.022242
  ...
# Subtest: nav MC15 hands LINKS edits to the relation mirror and notices generated lines once
ok 2958 - nav MC15 hands LINKS edits to the relation mirror and notices generated lines once
  ---
  duration_ms: 4.354627
  ...
# Subtest: LG3: typed relation labels commit their text through the relation field
    # Subtest: add writes the typed label and mirror
    ok 1 - add writes the typed label and mirror
      ---
      duration_ms: 9.880288
      ...
    # Subtest: typed text is normalized before commit
    ok 2 - typed text is normalized before commit
      ---
      duration_ms: 1.483172
      ...
    # Subtest: relabel replaces an existing label and its mirror
    ok 3 - relabel replaces an existing label and its mirror
      ---
      duration_ms: 6.454976
      ...
    # Subtest: Linked from labels the other task's LINKS line
    ok 4 - Linked from labels the other task's LINKS line
      ---
      duration_ms: 2.412106
      ...
    # Subtest: suggestion, plain, and raw-input paths remain supported
    ok 5 - suggestion, plain, and raw-input paths remain supported
      ---
      duration_ms: 3.509343
      ...
    1..5
ok 2959 - LG3: typed relation labels commit their text through the relation field
  ---
  duration_ms: 25.177882
  ...
# Subtest: Linked from Shift+Enter goes through the relation field and labels the source
ok 2960 - Linked from Shift+Enter goes through the relation field and labels the source
  ---
  duration_ms: 1.863279
  ...
# Subtest: Linked from Shift+Enter relabels a CURRENT source
ok 2961 - Linked from Shift+Enter relabels a CURRENT source
  ---
  duration_ms: 2.724844
  ...
# Subtest: Linked from prompts for the owner's id then links
    # Subtest: plain Enter writes the owner id and the reverse link
    ok 1 - plain Enter writes the owner id and the reverse link
      ---
      duration_ms: 5.432704
      ...
    # Subtest: Shift+Enter labels the source after the owner id prompt
    ok 2 - Shift+Enter labels the source after the owner id prompt
      ---
      duration_ms: 2.176666
      ...
    1..2
ok 2962 - Linked from prompts for the owner's id then links
  ---
  duration_ms: 8.537934
  ...
# Subtest: Links to prompts for the selected task's id then links
ok 2963 - Links to prompts for the selected task's id then links
  ---
  duration_ms: 1.195303
  ...
# Subtest: Linked-from toasts name the source task
ok 2964 - Linked-from toasts name the source task
  ---
  duration_ms: 4.232713
  ...
# Subtest: links-to row follows blocks with N, first label, cut target, and +K
ok 2965 - links-to row follows blocks with N, first label, cut target, and +K
  ---
  duration_ms: 7.607729
  ...
# Subtest: links-to row stays available on closed tasks and empty LINKS lines
ok 2966 - links-to row stays available on closed tasks and empty LINKS lines
  ---
  duration_ms: 1.948993
  ...
# Subtest: links-to row refuses non-tasks and read-only notes
ok 2967 - links-to row refuses non-tasks and read-only notes
  ---
  duration_ms: 0.914557
  ...
# Subtest: card keycap l opens Links to; input focus keeps it quiet
ok 2968 - card keycap l opens Links to; input focus keeps it quiet
  ---
  duration_ms: 0.972497
  ...
# Subtest: card ⇧L shows live incoming detail and routes Ctrl+D by direction
ok 2969 - card ⇧L shows live incoming detail and routes Ctrl+D by direction
  ---
  duration_ms: 1.969923
  ...
# Subtest: index-only Linked-from rows convert 1-based edges into nav records
ok 2970 - index-only Linked-from rows convert 1-based edges into nav records
  ---
  duration_ms: 0.585128
  ...
# Subtest: card ⇧L detail cleans a raw index task line
ok 2971 - card ⇧L detail cleans a raw index task line
  ---
  duration_ms: 0.700858
  ...
# Subtest: Linked-from scans source LINKS, reverses built-in phrases, and ignores stored mirrors
ok 2972 - Linked-from scans source LINKS, reverses built-in phrases, and ignores stored mirrors
  ---
  duration_ms: 1.17275
  ...
# Subtest: LG7: reverse-stage Enter writes the source's LINKS and target mirror
ok 2973 - LG7: reverse-stage Enter writes the source's LINKS and target mirror
  ---
  duration_ms: 0.788967
  ...
# Subtest: LG12: counted Links to applies the chosen labelled target to every source
ok 2974 - LG12: counted Links to applies the chosen labelled target to every source
  ---
  duration_ms: 1.485526
  ...
# Subtest: LG8: Ctrl+Shift+P on a LINKS line resolves to the owner's stage
ok 2975 - LG8: Ctrl+Shift+P on a LINKS line resolves to the owner's stage
  ---
  duration_ms: 0.745263
  ...
# Subtest: pool keeps closed tasks and done/ archives, drops dailies and templates
ok 2976 - pool keeps closed tasks and done/ archives, drops dailies and templates
  ---
  duration_ms: 0.460198
  ...
# Subtest: stage lists CURRENT in authored order, then RESULTS, then CLOSED
ok 2977 - stage lists CURRENT in authored order, then RESULTS, then CLOSED
  ---
  duration_ms: 1.975953
  ...
# Subtest: LG4: missing CURRENT targets stay removable; malformed lines refuse
ok 2978 - LG4: missing CURRENT targets stay removable; malformed lines refuse
  ---
  duration_ms: 0.427747
  ...
# Subtest: prerequisite targets badge; id-less rows prompt
ok 2979 - prerequisite targets badge; id-less rows prompt
  ---
  duration_ms: 1.394764
  ...
# Subtest: subtitle, consequence strip, live sentence, and label refusal copy
ok 2980 - subtitle, consequence strip, live sentence, and label refusal copy
  ---
  duration_ms: 0.38229
  ...
# Subtest: LG15: marked rows plan one commit with adds and unlinks split
ok 2981 - LG15: marked rows plan one commit with adds and unlinks split
  ---
  duration_ms: 0.231312
  ...
# Subtest: LG1: stage link writes LINKS, mirror, and mint in one transaction
ok 2982 - LG1: stage link writes LINKS, mirror, and mint in one transaction
  ---
  duration_ms: 1.011001
  ...
# Subtest: LG2: cross-note mirror follows; a changed target suffixes the notice
ok 2983 - LG2: cross-note mirror follows; a changed target suffixes the notice
  ---
  duration_ms: 4.013945
  ...
# Subtest: LG4: CURRENT unlink removes the entry and its mirror entry
ok 2984 - LG4: CURRENT unlink removes the entry and its mirror entry
  ---
  duration_ms: 1.045857
  ...
# Subtest: LG6: archived targets link with the live-only suffix and no mirror
ok 2985 - LG6: archived targets link with the live-only suffix and no mirror
  ---
  duration_ms: 0.352814
  ...
# Subtest: LG13: linking never stamps, routes, or touches Depends-On lines
ok 2986 - LG13: linking never stamps, routes, or touches Depends-On lines
  ---
  duration_ms: 1.123625
  ...
# Subtest: LG15: two targets link in one gesture with one notice
ok 2987 - LG15: two targets link in one gesture with one notice
  ---
  duration_ms: 0.613902
  ...
# Subtest: LG5: id-less targets refuse at the writer, so the stage prompts first
ok 2988 - LG5: id-less targets refuse at the writer, so the stage prompts first
  ---
  duration_ms: 0.261149
  ...
# Subtest: LG7: Ctrl+Shift+P resolves LINKED FROM to its owner's reverse stage
ok 2989 - LG7: Ctrl+Shift+P resolves LINKED FROM to its owner's reverse stage
  ---
  duration_ms: 0.197427
  ...
# Subtest: api.relations openStage opens both directions at v1
ok 2990 - api.relations openStage opens both directions at v1
  ---
  duration_ms: 0.448596
  ...
# Subtest: relation-label stage Tab, Ctrl+D, pipe, and Ctrl+H mirror the card
ok 2991 - relation-label stage Tab, Ctrl+D, pipe, and Ctrl+H mirror the card
  ---
  duration_ms: 23.018489
  ...
# Subtest: relation-label rename preview reports done/ impact and checks affected editors
ok 2992 - relation-label rename preview reports done/ impact and checks affected editors
  ---
  duration_ms: 1.097465
  ...
# Subtest: relation-label rename modal re-previews, saves the active note, and confirms merges
ok 2993 - relation-label rename modal re-previews, saves the active note, and confirms merges
  ---
  duration_ms: 1.564738
  ...
# Subtest: Bob: Relation labels manager keeps hidden labels visible and delegates hide and unhide
ok 2994 - Bob: Relation labels manager keeps hidden labels visible and delegates hide and unhide
  ---
  duration_ms: 0.864681
  ...
# Subtest: one-off labels hide through bob only after the relation commit succeeds
ok 2995 - one-off labels hide through bob only after the relation commit succeeds
  ---
  duration_ms: 1.509993
  ...
# Subtest: LW1 inserts an unlabelled LINKS line in the empty slot
ok 2996 - LW1 inserts an unlabelled LINKS line in the empty slot
  ---
  duration_ms: 3.776551
  ...
# Subtest: LW2 appends a labelled entry and LW3 is a byte-identical no-op
ok 2997 - LW2 appends a labelled entry and LW3 is a byte-identical no-op
  ---
  duration_ms: 1.766423
  ...
# Subtest: LW4 relabels in place and LW5/LW6 remove entries
ok 2998 - LW4 relabels in place and LW5/LW6 remove entries
  ---
  duration_ms: 0.994339
  ...
# Subtest: LW7 places LINKS after Sub-projects and LINKED FROM after LINKS
ok 2999 - LW7 places LINKS after Sub-projects and LINKED FROM after LINKS
  ---
  duration_ms: 2.438086
  ...
# Subtest: LW8 inserts LINKS as the first child when only user children exist
ok 3000 - LW8 inserts LINKS as the first child when only user children exist
  ---
  duration_ms: 0.566471
  ...
# Subtest: LW9 merges duplicate LINKS lines with first label winning
ok 3001 - LW9 merges duplicate LINKS lines with first label winning
  ---
  duration_ms: 0.542396
  ...
# Subtest: LW10 refuses a malformed LINKS line
ok 3002 - LW10 refuses a malformed LINKS line
  ---
  duration_ms: 0.297097
  ...
# Subtest: LW11 normalises and refuses labels
ok 3003 - LW11 normalises and refuses labels
  ---
  duration_ms: 0.896022
  ...
# Subtest: LW12 reuses a 4-space child indent
ok 3004 - LW12 reuses a 4-space child indent
  ---
  duration_ms: 0.461441
  ...
# Subtest: LW13 canonical link forms match Rust
ok 3005 - LW13 canonical link forms match Rust
  ---
  duration_ms: 0.992857
  ...
# Subtest: LW14 / LK20 LINKED FROM sort is byte-identical to Rust
ok 3006 - LW14 / LK20 LINKED FROM sort is byte-identical to Rust
  ---
  duration_ms: 0.595728
  ...
# Subtest: Rule 6 LINKED FROM planner table
ok 3007 - Rule 6 LINKED FROM planner table
  ---
  duration_ms: 1.638649
  ...
# Subtest: linkedFromDesiredAfterDelta keeps labels and sorts
ok 3008 - linkedFromDesiredAfterDelta keeps labels and sorts
  ---
  duration_ms: 0.516546
  ...
# Subtest: LG14 kill switch defaults on, honors false, and invalid values fall back on
ok 3009 - LG14 kill switch defaults on, honors false, and invalid values fall back on
  ---
  duration_ms: 1.47115
  ...
# Subtest: LG1 same-note add mints and writes LINKS plus LINKED FROM in one transaction
ok 3010 - LG1 same-note add mints and writes LINKS plus LINKED FROM in one transaction
  ---
  duration_ms: 6.342221
  ...
# Subtest: LG2 cross-note T follows the source commit; a changed target suffixes the notice
ok 3011 - LG2 cross-note T follows the source commit; a changed target suffixes the notice
  ---
  duration_ms: 2.327174
  ...
# Subtest: LG4 unlinks and relabels in place with the mirror
ok 3012 - LG4 unlinks and relabels in place with the mirror
  ---
  duration_ms: 3.211693
  ...
# Subtest: LG6 archived targets write LINKS without a mirror
ok 3013 - LG6 archived targets write LINKS without a mirror
  ---
  duration_ms: 0.901221
  ...
# Subtest: LG13 relation writes never stamp or change status
ok 3014 - LG13 relation writes never stamp or change status
  ---
  duration_ms: 0.899959
  ...
# Subtest: LG14 kill switch writes LINKS without a mirror or source mint
ok 3015 - LG14 kill switch writes LINKS without a mirror or source mint
  ---
  duration_ms: 0.432195
  ...
# Subtest: api.relations v1: removeLink works and openStage settles false without a plugin
ok 3016 - api.relations v1: removeLink works and openStage settles false without a plugin
  ---
  duration_ms: 2.363533
  ...
# Subtest: createDependencyNavApi mounts relations beside blocks
ok 3017 - createDependencyNavApi mounts relations beside blocks
  ---
  duration_ms: 0.63372
  ...
# Subtest: LG10: hand-edited LINKS mirrors to LINKED FROM and re-fires after undo
ok 3018 - LG10: hand-edited LINKS mirrors to LINKED FROM and re-fires after undo
  ---
  duration_ms: 5.258692
  ...
# Subtest: LG11: hand-editing generated LINKED FROM only shows its notice
ok 3019 - LG11: hand-editing generated LINKED FROM only shows its notice
  ---
  duration_ms: 0.50261
  ...
# Subtest: LG9: Ctrl+D's writer clears outgoing links and their generated mirrors
ok 3020 - LG9: Ctrl+D's writer clears outgoing links and their generated mirrors
  ---
  duration_ms: 1.705768
  ...
# relations.linked_from_lines is invalid; treating as true
# Subtest: Alt+N release from a NEXT landing advances with one composed toast
ok 3021 - Alt+N release from a NEXT landing advances with one composed toast
  ---
  duration_ms: 32.575759
  ...
# Subtest: counted Alt+N lands past every handled key in one jump
ok 3022 - counted Alt+N lands past every handled key in one jump
  ---
  duration_ms: 12.099846
  ...
# Subtest: a cancelled Alt+N release prompt stays and frees the lock
ok 3023 - a cancelled Alt+N release prompt stays and frees the lock
  ---
  duration_ms: 13.084439
  ...
# Subtest: Alt+N on a checklist landing stays with the plain notice
ok 3024 - Alt+N on a checklist landing stays with the plain notice
  ---
  duration_ms: 12.219464
  ...
# Subtest: Alt+N off a landing behaves exactly as today
ok 3025 - Alt+N off a landing behaves exactly as today
  ---
  duration_ms: 12.86522
  ...
# Subtest: Alt+N while the gesture lock is held is swallowed
ok 3026 - Alt+N while the gesture lock is held is swallowed
  ---
  duration_ms: 9.464815
  ...
# Subtest: a Task Card priority commit on NEXT advances, landing after the rich card
ok 3027 - a Task Card priority commit on NEXT advances, landing after the rich card
  ---
  duration_ms: 36.480566
  ...
# Subtest: dismissing the Task Card stays and frees the lock
ok 3028 - dismissing the Task Card stays and frees the lock
  ---
  duration_ms: 12.20547
  ...
# Subtest: a frontmatter-only project edit from the card stays
ok 3029 - a frontmatter-only project edit from the card stays
  ---
  duration_ms: 11.614509
  ...
# Subtest: a same-day priority schedule on a checklist row stays
ok 3030 - a same-day priority schedule on a checklist row stays
  ---
  duration_ms: 13.772792
  ...
# Subtest: a future schedule on a checklist row advances
ok 3031 - a future schedule on a checklist row advances
  ---
  duration_ms: 17.092041
  ...
# Subtest: a Task Card cancel on a checklist row advances with the cancel card first
ok 3032 - a Task Card cancel on a checklist row advances with the cancel card first
  ---
  duration_ms: 15.242189
  ...
# Subtest: Ctrl+Shift+M from a landing follows the task and never advances
ok 3033 - Ctrl+Shift+M from a landing follows the task and never advances
  ---
  duration_ms: 15.684841
  ...
# Subtest: Ctrl+Shift+M from a checklist landing keeps the destination focus
ok 3034 - Ctrl+Shift+M from a checklist landing keeps the destination focus
  ---
  duration_ms: 11.49833
  ...
# Subtest: ]s after a landed move resumes at the successor despite the line shift
ok 3035 - ]s after a landed move resumes at the successor despite the line shift
  ---
  duration_ms: 33.367321
  ...
# Subtest: [s after a landed move resumes at the predecessor
ok 3036 - [s after a landed move resumes at the predecessor
  ---
  duration_ms: 11.092723
  ...
# Subtest: a counted move from a landing resumes past every moved target
ok 3037 - a counted move from a landing resumes past every moved target
  ---
  duration_ms: 11.466569
  ...
# Subtest: counted Ctrl+Shift+M command dispatch preserves a landed move count
ok 3038 - counted Ctrl+Shift+M command dispatch preserves a landed move count
  ---
  duration_ms: 20.078522
  ...
# Subtest: a stale landing is not parked
ok 3039 - a stale landing is not parked
  ---
  duration_ms: 9.616175
  ...
# Subtest: Ctrl+Shift+M while the gesture lock is held is swallowed
ok 3040 - Ctrl+Shift+M while the gesture lock is held is swallowed
  ---
  duration_ms: 0.632268
  ...
# Subtest: dismissing the move picker stays and frees the lock
ok 3041 - dismissing the move picker stays and frees the lock
  ---
  duration_ms: 10.10094
  ...
# Subtest: Ctrl+Shift+M off a landing behaves exactly as today
ok 3042 - Ctrl+Shift+M off a landing behaves exactly as today
  ---
  duration_ms: 8.935033
  ...
# Subtest: answer, move, answer stays in queue order past an accumulator alias
ok 3043 - answer, move, answer stays in queue order past an accumulator alias
  ---
  duration_ms: 4.061055
  ...
# Subtest: a move park ignores a stale accumulator alias
ok 3044 - a move park ignores a stale accumulator alias
  ---
  duration_ms: 0.556773
  ...
# Subtest: a re-indexed origin still advances from the landed row
ok 3045 - a re-indexed origin still advances from the landed row
  ---
  duration_ms: 1.022964
  ...
# Subtest: a landed move park clears the current review task
ok 3046 - a landed move park clears the current review task
  ---
  duration_ms: 0.42958
  ...
# Subtest: review settle follows the task through a BLOCKS insertion above (bob-cli-94)
ok 3047 - review settle follows the task through a BLOCKS insertion above (bob-cli-94)
  ---
  duration_ms: 19.898851
  ...
# Subtest: review settle follows a BLOCKS deletion above without advancing on a non-resolving edit
ok 3048 - review settle follows a BLOCKS deletion above without advancing on a non-resolving edit
  ---
  duration_ms: 11.494282
  ...
# Subtest: review settle never substitutes the cursor line and shares the inbox fallback reader
ok 3049 - review settle never substitutes the cursor line and shares the inbox fallback reader
  ---
  duration_ms: 2.148944
  ...
# Subtest: predicate: reviewOutcomeResolves across tiers and kinds
ok 3050 - predicate: reviewOutcomeResolves across tiers and kinds
  ---
  duration_ms: 3.244106
  ...
# Subtest: findReviewResumeIndex identifies rows by path and text
ok 3051 - findReviewResumeIndex identifies rows by path and text
  ---
  duration_ms: 0.712591
  ...
# Subtest: buildReviewMoveAnchor parks text-identified resume neighbours
ok 3052 - buildReviewMoveAnchor parks text-identified resume neighbours
  ---
  duration_ms: 1.274884
  ...
# Subtest: planReviewJump with a move anchor resumes at the walk neighbour
ok 3053 - planReviewJump with a move anchor resumes at the walk neighbour
  ---
  duration_ms: 2.16842
  ...
# Subtest: capture: null off a landing
ok 3054 - capture: null off a landing
  ---
  duration_ms: 9.14877
  ...
# Subtest: capture: frozen origin shape, BUSY while locked, expiry
ok 3055 - capture: frozen origin shape, BUSY while locked, expiry
  ---
  duration_ms: 1.159313
  ...
# Subtest: successor picker keeps a captured completion locked through selection and one walk toast
ok 3056 - successor picker keeps a captured completion locked through selection and one walk toast
  ---
  duration_ms: 25.954806
  ...
# Subtest: continue: refuses stale origins, showing the notice once
ok 3057 - continue: refuses stale origins, showing the notice once
  ---
  duration_ms: 8.833027
  ...
# Subtest: continue: stays on null and non-resolving outcomes
ok 3058 - continue: stays on null and non-resolving outcomes
  ---
  duration_ms: 3.108757
  ...
# Subtest: continue: stays for lane answers and mixed-version completes on checklist rows
ok 3059 - continue: stays for lane answers and mixed-version completes on checklist rows
  ---
  duration_ms: 4.3558
  ...
# Subtest: continue: a resolving lane answer advances exactly once with one composed toast
ok 3060 - continue: a resolving lane answer advances exactly once with one composed toast
  ---
  duration_ms: 2.540743
  ...
# Subtest: continue: counted handled refs land past every handled key in one jump
ok 3061 - continue: counted handled refs land past every handled key in one jump
  ---
  duration_ms: 3.63988
  ...
# Subtest: continue: wrap is announced and the empty queue composes the empty notice
ok 3062 - continue: wrap is announced and the empty queue composes the empty notice
  ---
  duration_ms: 5.352662
  ...
# Subtest: continue: anchor-only planning survives cursor drift and lagging queues
ok 3063 - continue: anchor-only planning survives cursor drift and lagging queues
  ---
  duration_ms: 3.65019
  ...
# Subtest: continue: POST origins never wrap
ok 3064 - continue: POST origins never wrap
  ---
  duration_ms: 3.149785
  ...
# Subtest: complete: the last lane row before POST stays with the next-step toast
ok 3065 - complete: the last lane row before POST stays with the next-step toast
  ---
  duration_ms: 2.784918
  ...
# Subtest: complete: a wrap onto a skipped PRE row stays
ok 3066 - complete: a wrap onto a skipped PRE row stays
  ---
  duration_ms: 1.865884
  ...
# Subtest: complete: a step into ROTTEN shows the boundary line
ok 3067 - complete: a step into ROTTEN shows the boundary line
  ---
  duration_ms: 1.991523
  ...
# Subtest: busy: walk keys, refresh, claim, and capture are swallowed in the settle window
ok 3068 - busy: walk keys, refresh, claim, and capture are swallowed in the settle window
  ---
  duration_ms: 4.265758
  ...
# Subtest: advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
ok 3069 - advance: Ctrl+Alt+F stamps through the shared tail with one composed toast
  ---
  duration_ms: 5.506646
  ...
# Subtest: advance: decay choices advance except reword, with no preamble of their own
ok 3070 - advance: decay choices advance except reword, with no preamble of their own
  ---
  duration_ms: 0.845685
  ...
# Subtest: jump history: same-note and cross-note auto-advances record, and <C-o> returns
ok 3071 - jump history: same-note and cross-note auto-advances record, and <C-o> returns
  ---
  duration_ms: 10.13323
  ...
# Subtest: jump history: a manual ]s also records its landing
ok 3072 - jump history: a manual ]s also records its landing
  ---
  duration_ms: 2.388361
  ...
# Subtest: api: reviewWalk v3 is frozen with version 1, degrades null, never throws
ok 3073 - api: reviewWalk v3 is frozen with version 1, degrades null, never throws
  ---
  duration_ms: 1.25669
  ...
# Subtest: walk identity: a stale accumulator key never moves the anchor
ok 3074 - walk identity: a stale accumulator key never moves the anchor
  ---
  duration_ms: 0.396437
  ...
# Subtest: walk identity: a lagging answered row stays excluded
ok 3075 - walk identity: a lagging answered row stays excluded
  ---
  duration_ms: 0.220541
  ...
# Subtest: walk identity: a line-shifting answer lands on the true successor by text
ok 3076 - walk identity: a line-shifting answer lands on the true successor by text
  ---
  duration_ms: 1.925798
  ...
# Subtest: walk identity: legacy anchors without text resolve as before
ok 3077 - walk identity: legacy anchors without text resolve as before
  ---
  duration_ms: 0.491449
  ...
# Subtest: walk identity: matchFreshStampRefs prefers text over line
ok 3078 - walk identity: matchFreshStampRefs prefers text over line
  ---
  duration_ms: 0.209531
  ...
# Subtest: walk identity: collectReviewAnswerKeys separates position from exclusion
ok 3079 - walk identity: collectReviewAnswerKeys separates position from exclusion
  ---
  duration_ms: 0.699166
  ...
# Subtest: return: planReviewWalkReturn pure decisions
ok 3080 - return: planReviewWalkReturn pure decisions
  ---
  duration_ms: 0.472211
  ...
# Subtest: return: same-note ]s returns then steps, both directions
ok 3081 - return: same-note ]s returns then steps, both directions
  ---
  duration_ms: 2.222505
  ...
# Subtest: return: a different due row returns instead of stepping from there
ok 3082 - return: a different due row returns instead of stepping from there
  ---
  duration_ms: 0.763739
  ...
# Subtest: return: cross-note return re-arms and records <C-o>
ok 3083 - return: cross-note return re-arms and records <C-o>
  ---
  duration_ms: 5.235839
  ...
# Subtest: return: a count is consumed and ignored
ok 3084 - return: a count is consumed and ignored
  ---
  duration_ms: 0.84309
  ...
# Subtest: return: endpoints never return
ok 3085 - return: endpoints never return
  ---
  duration_ms: 0.974952
  ...
# Subtest: return: its own stamp ends it
ok 3086 - return: its own stamp ends it
  ---
  duration_ms: 1.279183
  ...
# Subtest: return: a stamp elsewhere does not end it
ok 3087 - return: a stamp elsewhere does not end it
  ---
  duration_ms: 0.879168
  ...
# Subtest: return: answers move the current task, a stopped Ctrl+Enter clears it
ok 3088 - return: answers move the current task, a stopped Ctrl+Enter clears it
  ---
  duration_ms: 2.923293
  ...
# Subtest: return: a stale landing falls through in the same press
ok 3089 - return: a stale landing falls through in the same press
  ---
  duration_ms: 0.336563
  ...
# Subtest: return: a day change never returns
ok 3090 - return: a day change never returns
  ---
  duration_ms: 0.553658
  ...
# Subtest: predicate: reviewOutcomeResolves for the RECURRING resolution table
ok 3091 - predicate: reviewOutcomeResolves for the RECURRING resolution table
  ---
  duration_ms: 0.483804
  ...
# Subtest: recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
ok 3092 - recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row
  ---
  duration_ms: 0.200664
  ...
# Subtest: return: a RECURRING landing rearms the current-task return
ok 3093 - return: a RECURRING landing rearms the current-task return
  ---
  duration_ms: 0.390896
  ...
# Subtest: Ctrl+Alt+F after a Rotten Log insertion lands on the shifted successor exactly once
ok 3094 - Ctrl+Alt+F after a Rotten Log insertion lands on the shifted successor exactly once
  ---
  duration_ms: 2.973007
  ...
# Subtest: review answer outcome vectors map to the schema vocabulary
ok 3095 - review answer outcome vectors map to the schema vocabulary
  ---
  duration_ms: 1.589345
  ...
# Subtest: event builder uses the walk row key and its tier, once per distinct key
ok 3096 - event builder uses the walk row key and its tier, once per distinct key
  ---
  duration_ms: 1.264244
  ...
# Subtest: journal appends are queued and failures retain events without failing answers
ok 3097 - journal appends are queued and failures retain events without failing answers
  ---
  duration_ms: 6.403207
  ...
# Subtest: card after-line outcomes map done, drop, defer, sequence, and card
ok 3098 - card after-line outcomes map done, drop, defer, sequence, and card
  ---
  duration_ms: 1.590167
  ...
# Subtest: journal events carry plugin@manifest version with a 2.x fallback
ok 3099 - journal events carry plugin@manifest version with a 2.x fallback
  ---
  duration_ms: 1.56574
  ...
# Subtest: write failures show one notice per burst and a recovery notice
ok 3100 - write failures show one notice per burst and a recovery notice
  ---
  duration_ms: 1.349768
  ...
# Subtest: missing api.stats shows one session notice and later delivers retained events
ok 3101 - missing api.stats shows one session notice and later delivers retained events
  ---
  duration_ms: 1.545451
  ...
# Subtest: validation rejects drop the event and continue the drain
ok 3102 - validation rejects drop the event and continue the drain
  ---
  duration_ms: 1.109709
  ...
# Subtest: pending journal events cap at 500 and warn once per burst
ok 3103 - pending journal events cap at 500 and warn once per burst
  ---
  duration_ms: 3.21042
  ...
# Subtest: decay config defaults to enabled with one roll per level
ok 3104 - decay config defaults to enabled with one roll per level
  ---
  duration_ms: 3.783164
  ...
# Subtest: decay:false disables decay and level rolls are accepted but ignored
ok 3105 - decay:false disables decay and level rolls are accepted but ignored
  ---
  duration_ms: 0.75959
  ...
# Subtest: decay.rolls sets the limit and levels[].rolls overrides it
ok 3106 - decay.rolls sets the limit and levels[].rolls overrides it
  ---
  duration_ms: 0.313318
  ...
# Subtest: decay config rejects bad rolls, unknown keys and non-priority use
ok 3107 - decay config rejects bad rolls, unknown keys and non-priority use
  ---
  duration_ms: 0.7332
  ...
# Subtest: classifyScheduleLogRollReason sorts automatic heads from deliberate ones
ok 3108 - classifyScheduleLogRollReason sorts automatic heads from deliberate ones
  ---
  duration_ms: 0.933954
  ...
# Subtest: conformance vectors 1-10: streaks at P2 with the default limit
ok 3109 - conformance vectors 1-10: streaks at P2 with the default limit
  ---
  duration_ms: 3.940405
  ...
# Subtest: conformance vectors 11-15: custom limits, disabled decay and edges
ok 3110 - conformance vectors 11-15: custom limits, disabled decay and edges
  ---
  duration_ms: 0.865333
  ...
# Subtest: the streak reader follows log grammar: legacy labels, nesting and stops
ok 3111 - the streak reader follows log grammar: legacy labels, nesting and stops
  ---
  duration_ms: 0.7644
  ...
# Subtest: rollPriorityRecommendationDate avoids the current date when the window has room
ok 3112 - rollPriorityRecommendationDate avoids the current date when the window has room
  ---
  duration_ms: 0.999939
  ...
# Subtest: decay and cancel reason formatters use the exact ladder copy
ok 3113 - decay and cancel reason formatters use the exact ladder copy
  ---
  duration_ms: 0.687142
  ...
# Subtest: the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
ok 3114 - the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel
  ---
  duration_ms: 0.499845
  ...
# Subtest: the planner returns null without a configured priority
ok 3115 - the planner returns null without a configured priority
  ---
  duration_ms: 0.174614
  ...
# Subtest: buildPriorityRollPreviewModel carries the row copy for every kind
ok 3116 - buildPriorityRollPreviewModel carries the row copy for every kind
  ---
  duration_ms: 0.741566
  ...
# Subtest: picker-single recognizes the recommended-roll keypress
ok 3117 - picker-single recognizes the recommended-roll keypress
  ---
  duration_ms: 0.184382
  ...
# Subtest: picker-single stage-two footers carry the recommended-roll hints
ok 3118 - picker-single stage-two footers carry the recommended-roll hints
  ---
  duration_ms: 0.402939
  ...
# Subtest: picker-single shares one roll between the preview and the pinned row
ok 3119 - picker-single shares one roll between the preview and the pinned row
  ---
  duration_ms: 0.428959
  ...
# Subtest: picker-single plans the next-roll hint for the notice chips
ok 3120 - picker-single plans the next-roll hint for the notice chips
  ---
  duration_ms: 0.587402
  ...
# Subtest: picker-single notice cards name the roll, decay and next press
ok 3121 - picker-single notice cards name the roll, decay and next press
  ---
  duration_ms: 1.574007
  ...
# Subtest: picker-single decay payload and preview-target comparison
ok 3122 - picker-single decay payload and preview-target comparison
  ---
  duration_ms: 0.325352
  ...
# Subtest: picker-counted plans one recommendation per target with skips
ok 3123 - picker-counted plans one recommendation per target with skips
  ---
  duration_ms: 1.788656
  ...
# Subtest: picker-counted batch preview, footer and notice copy
ok 3124 - picker-counted batch preview, footer and notice copy
  ---
  duration_ms: 1.660091
  ...
# Subtest: picker-counted composes cancel then set-priority into one postimage
ok 3125 - picker-counted composes cancel then set-priority into one postimage
  ---
  duration_ms: 3.652454
  ...
# Subtest: picker-counted refuses a recurring cancel as one batch
ok 3126 - picker-counted refuses a recurring cancel as one batch
  ---
  duration_ms: 0.359226
  ...
# Subtest: recommended roll recovers with [unblocked::] when the writer is passed
ok 3127 - recommended roll recovers with [unblocked::] when the writer is passed
  ---
  duration_ms: 0.789357
  ...
# Subtest: picker-counted stale lines refuse and new options stay byte-identical
ok 3128 - picker-counted stale lines refuse and new options stay byte-identical
  ---
  duration_ms: 1.100902
  ...
# Subtest: picker-links aggregates one recommendation per note
ok 3129 - picker-links aggregates one recommendation per note
  ---
  duration_ms: 1.076425
  ...
# Subtest: picker-links refuses a recurring cancel as one batch
ok 3130 - picker-links refuses a recurring cancel as one batch
  ---
  duration_ms: 0.351451
  ...
# Subtest: picker-links takes a single recommended roll with Ctrl+Enter
ok 3131 - picker-links takes a single recommended roll with Ctrl+Enter
  ---
  duration_ms: 40.382227
  ...
# Subtest: picker-links shows no pinned roll row in stage two
ok 3132 - picker-links shows no pinned roll row in stage two
  ---
  duration_ms: 12.747626
  ...
# Subtest: picker-links decays and cancels a single Task Link
ok 3133 - picker-links decays and cancels a single Task Link
  ---
  duration_ms: 9.509329
  ...
# Subtest: picker-links applies a mixed batch across two notes
ok 3134 - picker-links applies a mixed batch across two notes
  ---
  duration_ms: 5.416353
  ...
# Subtest: picker-links refuses the whole batch when a linked note changed
ok 3135 - picker-links refuses the whole batch when a linked note changed
  ---
  duration_ms: 2.134787
  ...
# Subtest: picker-links prunes today's open Pomodoro links
ok 3136 - picker-links prunes today's open Pomodoro links
  ---
  duration_ms: 4.962698
  ...
# Subtest: picker-single Ctrl+Enter rolls a P2 task in one undo group
ok 3137 - picker-single Ctrl+Enter rolls a P2 task in one undo group
  ---
  duration_ms: 21.263316
  ...
# Subtest: picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
ok 3138 - picker-single opens on scheduled so Ctrl+Enter rolls with no navigation
  ---
  duration_ms: 12.3154
  ...
# Subtest: picker-single opens a ^prj task on inline scheduled for an immediate roll
ok 3139 - picker-single opens a ^prj task on inline scheduled for an immediate roll
  ---
  duration_ms: 14.111797
  ...
# Subtest: picker-counted opens on scheduled for an immediate mixed batch
ok 3140 - picker-counted opens on scheduled for an immediate mixed batch
  ---
  duration_ms: 15.638526
  ...
# Subtest: picker-links opens on scheduled for an immediate roll
ok 3141 - picker-links opens on scheduled for an immediate roll
  ---
  duration_ms: 12.711344
  ...
# Subtest: picker-single Ctrl+Enter decays a P2 task in one undo group
ok 3142 - picker-single Ctrl+Enter decays a P2 task in one undo group
  ---
  duration_ms: 13.114405
  ...
# Subtest: picker-single Ctrl+Enter cancels a P4 task in one undo group
ok 3143 - picker-single Ctrl+Enter cancels a P4 task in one undo group
  ---
  duration_ms: 13.43713
  ...
# Subtest: picker-single Ctrl+Enter in stage two writes the recommended roll
ok 3144 - picker-single Ctrl+Enter in stage two writes the recommended roll
  ---
  duration_ms: 13.050743
  ...
# Subtest: picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
ok 3145 - picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation
  ---
  duration_ms: 3.065796
  ...
# Subtest: picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
ok 3146 - picker-single P0 and closed tasks have no preview and Ctrl+Enter writes nothing
  ---
  duration_ms: 7.990619
  ...
# Subtest: picker-single recurring P4 past the limit refuses and keeps the picker open
ok 3147 - picker-single recurring P4 past the limit refuses and keeps the picker open
  ---
  duration_ms: 11.513887
  ...
# Subtest: picker-single stale tasks refuse and re-render the decay preview
ok 3148 - picker-single stale tasks refuse and re-render the decay preview
  ---
  duration_ms: 11.174612
  ...
# Subtest: picker-single Ctrl+R on the card re-rolls the recommendation date
ok 3149 - picker-single Ctrl+R on the card re-rolls the recommendation date
  ---
  duration_ms: 3.41957
  ...
# Subtest: picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
ok 3150 - picker-single Ctrl+R in stage two keeps the pinned row and recommendation together
  ---
  duration_ms: 1.887414
  ...
# Subtest: picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
ok 3151 - picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group
  ---
  duration_ms: 11.348831
  ...
# Subtest: picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
ok 3152 - picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group
  ---
  duration_ms: 11.452082
  ...
# Subtest: picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
ok 3153 - picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group
  ---
  duration_ms: 11.888602
  ...
# Subtest: picker-counted Ctrl+Enter refuses when a target line changed
ok 3154 - picker-counted Ctrl+Enter refuses when a target line changed
  ---
  duration_ms: 11.01279
  ...
# Subtest: picker-counted Ctrl+Enter refuses a recurring cancel batch
ok 3155 - picker-counted Ctrl+Enter refuses a recurring cancel batch
  ---
  duration_ms: 11.551932
  ...
# Subtest: recommended roll on Pending offers a Work Log with the frozen date
ok 3156 - recommended roll on Pending offers a Work Log with the frozen date
  ---
  duration_ms: 1015.730734
  ...
# Subtest: recommended roll blank summary skips the Work Log without a fallback
ok 3157 - recommended roll blank summary skips the Work Log without a fallback
  ---
  duration_ms: 1017.107273
  ...
# Subtest: Ctrl+Enter in the Work Log stage confirms instead of re-rolling
ok 3158 - Ctrl+Enter in the Work Log stage confirms instead of re-rolling
  ---
  duration_ms: 1029.754247
  ...
# Subtest: counted recommended mixed batch logs only eligible roll and decay targets
ok 3159 - counted recommended mixed batch logs only eligible roll and decay targets
  ---
  duration_ms: 1034.846
  ...
# Subtest: Task Link recommended roll deletes the emptied Pomodoro in the same daily write
ok 3160 - Task Link recommended roll deletes the emptied Pomodoro in the same daily write
  ---
  duration_ms: 3.557754
  ...
# Subtest: single keep logs still the primer with stamp in one undo
ok 3161 - single keep logs still the primer with stamp in one undo
  ---
  duration_ms: 16.573358
  ...
# Subtest: single keep logs blank with stamp in one undo
ok 3162 - single keep logs blank with stamp in one undo
  ---
  duration_ms: 2.865181
  ...
# Subtest: Esc retains the document and walk anchor; repeat command cannot open another prompt
ok 3163 - Esc retains the document and walk anchor; repeat command cannot open another prompt
  ---
  duration_ms: 1.257381
  ...
# Subtest: same-day repeat never prompts or appends, including saturated 999
ok 3164 - same-day repeat never prompts or appends, including saturated 999
  ---
  duration_ms: 4.809697
  ...
# Subtest: counted predicate: scheduled tickler
ok 3165 - counted predicate: scheduled tickler
  ---
  duration_ms: 0.482542
  ...
# Subtest: counted predicate: unblock tickler
ok 3166 - counted predicate: unblock tickler
  ---
  duration_ms: 0.254226
  ...
# Subtest: counted predicate: new
ok 3167 - counted predicate: new
  ---
  duration_ms: 0.239137
  ...
# Subtest: counted predicate: Pending
ok 3168 - counted predicate: Pending
  ---
  duration_ms: 0.166769
  ...
# Subtest: counted predicate: Next
ok 3169 - counted predicate: Next
  ---
  duration_ms: 0.398081
  ...
# Subtest: counted predicate: PROJECTS
ok 3170 - counted predicate: PROJECTS
  ---
  duration_ms: 0.51304
  ...
# Subtest: counted predicate: recurring
ok 3171 - counted predicate: recurring
  ---
  duration_ms: 0.255609
  ...
# Subtest: counted predicate: checklist
ok 3172 - counted predicate: checklist
  ---
  duration_ms: 0.124548
  ...
# Subtest: counted predicate: closed
ok 3173 - counted predicate: closed
  ---
  duration_ms: 0.12063
  ...
# Subtest: counted predicate: early
ok 3174 - counted predicate: early
  ---
  duration_ms: 0.12
  ...
# Subtest: scheduled tickler logs; unblocked and legacy keeps never prompt
ok 3175 - scheduled tickler logs; unblocked and legacy keeps never prompt
  ---
  duration_ms: 3.585056
  ...
# Subtest: Pending retains its Work summary prompt
ok 3176 - Pending retains its Work summary prompt
  ---
  duration_ms: 1.895109
  ...
# Subtest: counted mixed sessions use one Work-first prompt and route each answer to its log
ok 3177 - counted mixed sessions use one Work-first prompt and route each answer to its log
  ---
  duration_ms: 3.107103
  ...
# Subtest: counted at-limit Rotten targets skip without opening a prompt or logging
ok 3178 - counted at-limit Rotten targets skip without opening a prompt or logging
  ---
  duration_ms: 0.799847
  ...
# Subtest: unavailable decay card falls through the reason planner
ok 3179 - unavailable decay card falls through the reason planner
  ---
  duration_ms: 1.564247
  ...
# Subtest: document changes while prompt is open refuse the entire keep
ok 3180 - document changes while prompt is open refuse the entire keep
  ---
  duration_ms: 4.316222
  ...
# Subtest: day changes while prompt is open refuse the entire keep
ok 3181 - day changes while prompt is open refuse the entire keep
  ---
  duration_ms: 1.12082
  ...
# Subtest: prediction changes while prompt is open refuse the entire keep
ok 3182 - prediction changes while prompt is open refuse the entire keep
  ---
  duration_ms: 1.122604
  ...
# Subtest: guard changes while prompt is open refuse the entire keep
ok 3183 - guard changes while prompt is open refuse the entire keep
  ---
  duration_ms: 0.736196
  ...
# Subtest: ambiguous Rotten markers disable the prompt and refuse even a bypass
ok 3184 - ambiguous Rotten markers disable the prompt and refuse even a bypass
  ---
  duration_ms: 2.10965
  ...
# Subtest: combined planner inserts nested targets bottom-up and preserves CRLF
ok 3185 - combined planner inserts nested targets bottom-up and preserves CRLF
  ---
  duration_ms: 1.059283
  ...
# Subtest: prompt copy separates streak from history and previews exact formatter output
ok 3186 - prompt copy separates streak from history and previews exact formatter output
  ---
  duration_ms: 0.474717
  ...
# Subtest: keep stage warns for inline fields, ignores IME Enter, and swallows both keep chords
ok 3187 - keep stage warns for inline fields, ignores IME Enter, and swallows both keep chords
  ---
  duration_ms: 1.224348
  ...
# Subtest: marker vectors match the Rust Rotten cases
ok 3188 - marker vectors match the Rust Rotten cases
  ---
  duration_ms: 1.630273
  ...
# Subtest: entry parsing accepts valid entries and rejects bad counts
ok 3189 - entry parsing accepts valid entries and rejects bad counts
  ---
  duration_ms: 0.394242
  ...
# Subtest: readRottenLog statuses cover missing, empty, ok, and unknown
ok 3190 - readRottenLog statuses cover missing, empty, ok, and unknown
  ---
  duration_ms: 0.84348
  ...
# Subtest: planManagedTaskLogEntry creates the log last and prepends entries
ok 3191 - planManagedTaskLogEntry creates the log last and prepends entries
  ---
  duration_ms: 0.851446
  ...
# Subtest: Work Log writes never file under the Rotten marker
ok 3192 - Work Log writes never file under the Rotten marker
  ---
  duration_ms: 0.556082
  ...
# Subtest: freshness delegation guards reject Pomodoro ledger rows before injected writers
ok 3193 - freshness delegation guards reject Pomodoro ledger rows before injected writers
  ---
  duration_ms: 4.168039
  ...
# Subtest: refresh picker refuses a legacy Pomodoro heading before its refresher runs
ok 3194 - refresh picker refuses a legacy Pomodoro heading before its refresher runs
  ---
  duration_ms: 0.7853
  ...
# Subtest: lane commit stamps an open Ready task
ok 3195 - lane commit stamps an open Ready task
  ---
  duration_ms: 3.895078
  ...
# Subtest: lane release stamps an open Next task
ok 3196 - lane release stamps an open Next task
  ---
  duration_ms: 0.566452
  ...
# Subtest: lane without a stamper leaves lines as they were
ok 3197 - lane without a stamper leaves lines as they were
  ---
  duration_ms: 0.34588
  ...
# Subtest: counted property set stamps every rewritten open task
ok 3198 - counted property set stamps every rewritten open task
  ---
  duration_ms: 3.330019
  ...
# Subtest: counted delete-property stamps the rewritten task
ok 3199 - counted delete-property stamps the rewritten task
  ---
  duration_ms: 0.741095
  ...
# Subtest: stamp lands before the suffix after a priority edit on a stamped line
ok 3200 - stamp lands before the suffix after a priority edit on a stamped line
  ---
  duration_ms: 0.692523
  ...
# Subtest: recurring tasks are never stamped
ok 3201 - recurring tasks are never stamped
  ---
  duration_ms: 0.679388
  ...
# Subtest: cancel never stamps
ok 3202 - cancel never stamps
  ---
  duration_ms: 2.016902
  ...
# Subtest: fresh and refresh never go through the end-append writers
ok 3203 - fresh and refresh never go through the end-append writers
  ---
  duration_ms: 0.379836
  ...
# Subtest: counted dependency edit stamps the rewritten parent
ok 3204 - counted dependency edit stamps the rewritten parent
  ---
  duration_ms: 7.405903
  ...
# Subtest: moved tasks are stamped at their destination
ok 3205 - moved tasks are stamped at their destination
  ---
  duration_ms: 3.455238
  ...
# Subtest: move without a stamper leaves lines as they were
ok 3206 - move without a stamper leaves lines as they were
  ---
  duration_ms: 0.570469
  ...
# Subtest: refresh row shows the effective interval in task mode
ok 3207 - refresh row shows the effective interval in task mode
  ---
  duration_ms: 0.805187
  ...
# Subtest: refresh row hides without the api and on closed tasks
ok 3208 - refresh row hides without the api and on closed tasks
  ---
  duration_ms: 0.151048
  ...
# Subtest: refresh row covers counted and link modes, including mixed
ok 3209 - refresh row covers counted and link modes, including mixed
  ---
  duration_ms: 0.35601
  ...
# Subtest: refresh value items offer presets and use default
ok 3210 - refresh value items offer presets and use default
  ---
  duration_ms: 0.862988
  ...
# Subtest: setRefreshLine stamps and sets or clears the interval
ok 3211 - setRefreshLine stamps and sets or clears the interval
  ---
  duration_ms: 0.448666
  ...
# Subtest: 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
ok 3212 - 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys
  ---
  duration_ms: 9.527694
  ...
# Subtest: Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
ok 3213 - Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows
  ---
  duration_ms: 5.78124
  ...
# Subtest: filtering expands matches, collapse state survives clearing, and hidden marks still submit
ok 3214 - filtering expands matches, collapse state survives clearing, and hidden marks still submit
  ---
  duration_ms: 4.089099
  ...
# Subtest: group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
ok 3215 - group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed
  ---
  duration_ms: 4.437035
  ...
# Subtest: Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
ok 3216 - Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed
  ---
  duration_ms: 0.837018
  ...
# Subtest: Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
ok 3217 - Escape, outside close, repeat close, concurrent calls, and unusable models settle safely
  ---
  duration_ms: 1.194913
  ...
# Subtest: the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
ok 3218 - the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner
  ---
  duration_ms: 0.610245
  ...
# Subtest: destination override shapes normalize and label
ok 3219 - destination override shapes normalize and label
  ---
  duration_ms: 0.226863
  ...
# Subtest: destination picker detection needs block-id-prompt api v1 with pick
ok 3220 - destination picker detection needs block-id-prompt api v1 with pick
  ---
  duration_ms: 0.406867
  ...
# Subtest: Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks
ok 3221 - Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks
  ---
  duration_ms: 2.268291
  ...
# Subtest: Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked
ok 3222 - Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked
  ---
  duration_ms: 1.255357
  ...
# Subtest: a cancelled destination pick and a missing picker leave rows untouched
ok 3223 - a cancelled destination pick and a missing picker leave rows untouched
  ---
  duration_ms: 1.75461
  ...
# Subtest: unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
ok 3224 - unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up
  ---
  duration_ms: 0.874129
  ...
# Subtest: card model builds stable rows, scope metadata, and an existing recommendation
ok 3225 - card model builds stable rows, scope metadata, and an existing recommendation
  ---
  duration_ms: 9.396403
  ...
# Subtest: explicit preview builder matches writer rolls and deduplicates linked targets
ok 3226 - explicit preview builder matches writer rolls and deduplicates linked targets
  ---
  duration_ms: 0.958851
  ...
# Subtest: counted and linked card models report real target counts and mixed values
ok 3227 - counted and linked card models report real target counts and mixed values
  ---
  duration_ms: 4.978847
  ...
# Subtest: priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
ok 3228 - priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents
  ---
  duration_ms: 2.760481
  ...
# Subtest: Escape, bare q, and Ctrl+[ close the card; nothing else does
ok 3229 - Escape, bare q, and Ctrl+[ close the card; nothing else does
  ---
  duration_ms: 0.985412
  ...
# Subtest: close keys never fire during composition or inside a text field
ok 3230 - close keys never fire during composition or inside a text field
  ---
  duration_ms: 1.380136
  ...
# Subtest: unavailable actions, input composition, and repeats stay safe
ok 3231 - unavailable actions, input composition, and repeats stay safe
  ---
  duration_ms: 2.090913
  ...
# Subtest: Blocks row summarizes warm-cache dependents and their last open reason
ok 3232 - Blocks row summarizes warm-cache dependents and their last open reason
  ---
  duration_ms: 1.117685
  ...
# Subtest: Blocks row refuses closed tasks and unencodable paths without an id
ok 3233 - Blocks row refuses closed tasks and unencodable paths without an id
  ---
  duration_ms: 2.208959
  ...
# Subtest: key resolver table covers lane state, API availability, and modifier guards
ok 3234 - key resolver table covers lane state, API availability, and modifier guards
  ---
  duration_ms: 2.904176
  ...
# Subtest: recurring cancellation and blocked lanes expose reasons instead of writes
ok 3235 - recurring cancellation and blocked lanes expose reasons instead of writes
  ---
  duration_ms: 0.743069
  ...
# Subtest: identity keys distinguish linked notes that share a line number
ok 3236 - identity keys distinguish linked notes that share a line number
  ---
  duration_ms: 1.77511
  ...
# Subtest: planScheduleReview opens for a bare date and skips when reason is known without Work Log
ok 3237 - planScheduleReview opens for a bare date and skips when reason is known without Work Log
  ---
  duration_ms: 1.156518
  ...
# Subtest: planScheduleReview counts unique tasks when Task Links repeat a target
ok 3238 - planScheduleReview counts unique tasks when Task Links repeat a target
  ---
  duration_ms: 0.728821
  ...
# Subtest: bare date on Ready opens a reason-only review and writes nothing until Enter
ok 3239 - bare date on Ready opens a reason-only review and writes nothing until Enter
  ---
  duration_ms: 30.434491
  ...
# Subtest: typed reason and blank reason on an existing Schedule Log keep per-target rules
ok 3240 - typed reason and blank reason on an existing Schedule Log keep per-target rules
  ---
  duration_ms: 9.133082
  ...
# Subtest: Ready vs Next vs Pending: only Next/Pending show Work summary
ok 3241 - Ready vs Next vs Pending: only Next/Pending show Work summary
  ---
  duration_ms: 12.174018
  ...
# Subtest: inline reason on Ready dispatches immediately; on Next it still reviews Work summary
ok 3242 - inline reason on Ready dispatches immediately; on Next it still reviews Work summary
  ---
  duration_ms: 7.855811
  ...
# Subtest: Tab moves from Reason to Work summary and Enter commits from either field
ok 3243 - Tab moves from Reason to Work summary and Enter commits from either field
  ---
  duration_ms: 4.459606
  ...
# Subtest: Back and Escape at both review fields write nothing
ok 3244 - Back and Escape at both review fields write nothing
  ---
  duration_ms: 5.176567
  ...
# Subtest: a target changed during review refuses with no write
ok 3245 - a target changed during review refuses with no write
  ---
  duration_ms: 3.538107
  ...
# Subtest: counted mixed targets share one review and one adapter call
ok 3246 - counted mixed targets share one review and one adapter call
  ---
  duration_ms: 4.380716
  ...
# Subtest: linked notes with equal line numbers both qualify
ok 3247 - linked notes with equal line numbers both qualify
  ---
  duration_ms: 3.668836
  ...
# Subtest: project lifecycle review names propagation and still writes once
ok 3248 - project lifecycle review names propagation and still writes once
  ---
  duration_ms: 3.983808
  ...
# Subtest: priority picks still skip the combined review and keep Work Log-only prompts
ok 3249 - priority picks still skip the combined review and keep Work Log-only prompts
  ---
  duration_ms: 2.255347
  ...
# Subtest: a typed date from the card's schedule row uses the combined review
ok 3250 - a typed date from the card's schedule row uses the combined review
  ---
  duration_ms: 5.233004
  ...
# Subtest: scheduling a Pending task goes straight to the combined review, never serial prompts
ok 3251 - scheduling a Pending task goes straight to the combined review, never serial prompts
  ---
  duration_ms: 2.406847
  ...
# Subtest: classic parser keeps ISO, M/D, and signed units and ignores concise forms
ok 3252 - classic parser keeps ISO, M/D, and signed units and ignores concise forms
  ---
  duration_ms: 1.399813
  ...
# Subtest: typed schedule resolver covers bare days, units, weekdays, and inline reasons
ok 3253 - typed schedule resolver covers bare days, units, weekdays, and inline reasons
  ---
  duration_ms: 1.24646
  ...
# Subtest: weekdays resolve to the next occurrence strictly after today
ok 3254 - weekdays resolve to the next occurrence strictly after today
  ---
  duration_ms: 0.156168
  ...
# Subtest: invalid leap dates, end-of-month offsets, and December rollover
ok 3255 - invalid leap dates, end-of-month offsets, and December rollover
  ---
  duration_ms: 0.39837
  ...
# Subtest: negative, overflow, malformed, and preset-filter queries are rejected without dates
ok 3256 - negative, overflow, malformed, and preset-filter queries are rejected without dates
  ---
  duration_ms: 0.225661
  ...
# Subtest: DST local-calendar arithmetic stays on calendar days in America/New_York
ok 3257 - DST local-calendar arithmetic stays on calendar days in America/New_York
  ---
  duration_ms: 117.213733
  ...
# Subtest: Task Card date stage previews weekday, ISO, relative distance, and rollover year
ok 3258 - Task Card date stage previews weekday, ISO, relative distance, and rollover year
  ---
  duration_ms: 15.285012
  ...
# Subtest: inline reason is preserved on the preview and skips the reason stage
ok 3259 - inline reason is preserved on the preview and skips the reason stage
  ---
  duration_ms: 13.274098
  ...
# Subtest: Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
ok 3260 - Shift+Enter skips the reason by the blank-reason rule and still offers Work Log
  ---
  duration_ms: 6.826669
  ...
# Subtest: Shift+Enter on a Ready task commits in four gestures without a Work Log
ok 3261 - Shift+Enter on a Ready task commits in four gestures without a Work Log
  ---
  duration_ms: 5.48288
  ...
# Subtest: invalid typed dates render an error preview and do not write
ok 3262 - invalid typed dates render an error preview and do not write
  ---
  duration_ms: 3.58156
  ...
# Subtest: the card's schedule stage always uses the concise resolver
ok 3263 - the card's schedule stage always uses the concise resolver
  ---
  duration_ms: 2.291075
  ...
# Subtest: tomorrow stays a preset filter and is not stolen as a typed date
ok 3264 - tomorrow stays a preset filter and is not stolen as a typed date
  ---
  duration_ms: 1.802632
  ...
# Subtest: mixed Task Links preview one date and freeze that action with the inline reason
ok 3265 - mixed Task Links preview one date and freeze that action with the inline reason
  ---
  duration_ms: 5.553325
  ...
# Subtest: Ctrl+Enter still takes the recommended roll from the Task Card date stage
ok 3266 - Ctrl+Enter still takes the recommended roll from the Task Card date stage
  ---
  duration_ms: 5.415493
  ...
# Subtest: Modal harness models Obsidian 1.14 attachment and idempotent close
ok 3267 - Modal harness models Obsidian 1.14 attachment and idempotent close
  ---
  duration_ms: 1.835204
  ...
# Subtest: styles share key-card tokens and compact Task Card dimensions
ok 3268 - styles share key-card tokens and compact Task Card dimensions
  ---
  duration_ms: 0.37715
  ...
# Subtest: card renderer paints header, banner, strip, stable rows, more, and footer from the model
ok 3269 - card renderer paints header, banner, strip, stable rows, more, and footer from the model
  ---
  duration_ms: 11.141098
  ...
# Subtest: renderer does not consume randomness or invent recommendation data
ok 3270 - renderer does not consume randomness or invent recommendation data
  ---
  duration_ms: 1.934103
  ...
# Subtest: no-recommendation, cancel, mixed, long text, missing API, and error states render
ok 3271 - no-recommendation, cancel, mixed, long text, missing API, and error states render
  ---
  duration_ms: 9.166023
  ...
# Subtest: counted and linked cards disclose mixed values and Task Link notes
ok 3272 - counted and linked cards disclose mixed values and Task Link notes
  ---
  duration_ms: 4.616546
  ...
# Subtest: Ctrl+Shift+P always opens the Task Card, never the classic property list
ok 3273 - Ctrl+Shift+P always opens the Task Card, never the classic property list
  ---
  duration_ms: 3.683625
  ...
# Subtest: the plugin carries no Task Card pilot setting, date gate, or classic preference
ok 3274 - the plugin carries no Task Card pilot setting, date gate, or classic preference
  ---
  duration_ms: 22.360752
  ...
# Subtest: a leftover persisted taskCard flag is ignored and never rewritten
ok 3275 - a leftover persisted taskCard flag is ignored and never rewritten
  ---
  duration_ms: 9.820847
  ...
# Subtest: palette command is named Task card (set properties)
ok 3276 - palette command is named Task card (set properties)
  ---
  duration_ms: 10.925834
  ...
# Subtest: Task Card opens the compact card with dialog semantics and a close control
ok 3277 - Task Card opens the compact card with dialog semantics and a close control
  ---
  duration_ms: 1.627548
  ...
# Subtest: a More row opens that property's value stage, never a filter list, and Back restores the card
ok 3278 - a More row opens that property's value stage, never a filter list, and Back restores the card
  ---
  duration_ms: 3.42469
  ...
# Subtest: after open the actions list, not the Close button, has focus
ok 3279 - after open the actions list, not the Close button, has focus
  ---
  duration_ms: 9.91271
  ...
# Subtest: clicking card text keeps the card key router active exactly once
ok 3280 - clicking card text keeps the card key router active exactly once
  ---
  duration_ms: 20.902809
  ...
# Subtest: Ready card writes close from a key, P1 click, recommendations, and Alt+N
ok 3281 - Ready card writes close from a key, P1 click, recommendations, and Alt+N
  ---
  duration_ms: 7.028532
  ...
# Subtest: Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
ok 3282 - Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing
  ---
  duration_ms: 4.620885
  ...
# Subtest: Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
ok 3283 - Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage
  ---
  duration_ms: 10.789894
  ...
# Subtest: Ctrl+R recomputes and repaints the card recommendation
ok 3284 - Ctrl+R recomputes and repaints the card recommendation
  ---
  duration_ms: 1.59216
  ...
# Subtest: Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
ok 3285 - Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages
  ---
  duration_ms: 19.881068
  ...
# Subtest: Task Link opens focused while resolving and consumes keys without replay
ok 3286 - Task Link opens focused while resolving and consumes keys without replay
  ---
  duration_ms: 3.622207
  ...
# Subtest: Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card
ok 3287 - Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card
  ---
  duration_ms: 1.796811
  ...
# Subtest: Ctrl+Shift+Alt+B on a Task Link opens the linked Blocks stage
ok 3288 - Ctrl+Shift+Alt+B on a Task Link opens the linked Blocks stage
  ---
  duration_ms: 1.1522
  ...
# Subtest: Task Link count replacement and source edits invalidate old resolutions
ok 3289 - Task Link count replacement and source edits invalidate old resolutions
  ---
  duration_ms: 1.259185
  ...
# Subtest: Task Link resolution failure and plugin unload close their shells
ok 3290 - Task Link resolution failure and plugin unload close their shells
  ---
  duration_ms: 1.803754
  ...
# Subtest: direct Depends on entry opens the dependency stage without painting the card or the list
ok 3291 - direct Depends on entry opens the dependency stage without painting the card or the list
  ---
  duration_ms: 0.997064
  ...
# Subtest: a direct stage for an unconfigured property closes instead of leaving an empty modal
ok 3292 - a direct stage for an unconfigured property closes instead of leaving an empty modal
  ---
  duration_ms: 0.304121
  ...
# Subtest: a refused direct stage closes instead of landing on a card or a list
ok 3293 - a refused direct stage closes instead of landing on a card or a list
  ---
  duration_ms: 0.692492
  ...
# Subtest: Ctrl+Shift+B lands on the Depends on stage with the same intent as card b
ok 3294 - Ctrl+Shift+B lands on the Depends on stage with the same intent as card b
  ---
  duration_ms: 2.506827
  ...
# Subtest: Ctrl+Shift+B Back returns to the card without re-dispatching
ok 3295 - Ctrl+Shift+B Back returns to the card without re-dispatching
  ---
  duration_ms: 1.095813
  ...
# Subtest: Ctrl+Shift+B on a plain bullet notices and closes the card
ok 3296 - Ctrl+Shift+B on a plain bullet notices and closes the card
  ---
  duration_ms: 0.78048
  ...
# Subtest: Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch
ok 3297 - Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch
  ---
  duration_ms: 3.67055
  ...
# Subtest: Ctrl+Shift+Alt+B on Depends-On and BLOCKS lines opens the owner's stage directly
ok 3298 - Ctrl+Shift+Alt+B on Depends-On and BLOCKS lines opens the owner's stage directly
  ---
  duration_ms: 2.265868
  ...
# Subtest: Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not
ok 3299 - Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not
  ---
  duration_ms: 4.852618
  ...
# Subtest: priority gesture writes the frozen date and duplicate dispatch is single-flight
ok 3300 - priority gesture writes the frozen date and duplicate dispatch is single-flight
  ---
  duration_ms: 6.181825
  ...
# Subtest: pending priority action passes its card preview through the Work Log adapter
ok 3301 - pending priority action passes its card preview through the Work Log adapter
  ---
  duration_ms: 1.358414
  ...
# Subtest: Task Link priority action refuses a stale cross-note preflight before writes
ok 3302 - Task Link priority action refuses a stale cross-note preflight before writes
  ---
  duration_ms: 4.593321
  ...
# Subtest: Task Link priority action rolls back earlier note writes after a later write fails
ok 3303 - Task Link priority action rolls back earlier note writes after a later write fails
  ---
  duration_ms: 1.951878
  ...
# Subtest: Task Link transaction reports a cleanup failure without implying global undo
ok 3304 - Task Link transaction reports a cleanup failure without implying global undo
  ---
  duration_ms: 1.034255
  ...
# Subtest: selected-property deletion uses the existing writer; other card rows stay non-deletable
ok 3305 - selected-property deletion uses the existing writer; other card rows stay non-deletable
  ---
  duration_ms: 7.048412
  ...
# Subtest: failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
ok 3306 - failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing
  ---
  duration_ms: 1.502018
  ...
# Subtest: a refused deletion rebuilds the card from the refreshed line
ok 3307 - a refused deletion rebuilds the card from the refreshed line
  ---
  duration_ms: 1.404122
  ...
# Subtest: 0 deletes only priority and keeps the scheduled field byte-for-byte
ok 3308 - 0 deletes only priority and keeps the scheduled field byte-for-byte
  ---
  duration_ms: 1.299201
  ...
# Subtest: card keys pressed on a priority radio or the banner reach the resolver exactly once
ok 3309 - card keys pressed on a priority radio or the banner reach the resolver exactly once
  ---
  duration_ms: 2.431804
  ...
# Subtest: held or composing Enter on a radio or the banner never writes
ok 3310 - held or composing Enter on a radio or the banner never writes
  ---
  duration_ms: 0.935176
  ...
# Subtest: Escape, q, Q, and Ctrl+[ close the card without writing
ok 3311 - Escape, q, Q, and Ctrl+[ close the card without writing
  ---
  duration_ms: 3.0844
  ...
# Subtest: Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
ok 3312 - Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card
  ---
  duration_ms: 0.627318
  ...
# Subtest: repeated close keys and a second close() are harmless
ok 3313 - repeated close keys and a second close() are harmless
  ---
  duration_ms: 0.919155
  ...
# Subtest: composition never closes the card or a stage
ok 3314 - composition never closes the card or a stage
  ---
  duration_ms: 0.876975
  ...
# Subtest: q typed into a stage's text field never closes the modal
ok 3315 - q typed into a stage's text field never closes the modal
  ---
  duration_ms: 0.813874
  ...
# Subtest: Ctrl+[ closes from a focused date field without writing
ok 3316 - Ctrl+[ closes from a focused date field without writing
  ---
  duration_ms: 1.012333
  ...
# Subtest: Ctrl+[ closes the schedule review from its Reason and Work summary fields
ok 3317 - Ctrl+[ closes the schedule review from its Reason and Work summary fields
  ---
  duration_ms: 5.075522
  ...
# Subtest: Ctrl+[ closes the summary-only schedule-work-log stage without writing
ok 3318 - Ctrl+[ closes the summary-only schedule-work-log stage without writing
  ---
  duration_ms: 1.093979
  ...
# Subtest: Ctrl+[ closes the lane-release Work summary without writing
ok 3319 - Ctrl+[ closes the lane-release Work summary without writing
  ---
  duration_ms: 1.118947
  ...
# Subtest: q closes from a focused More row and from the Close button
ok 3320 - q closes from a focused More row and from the Close button
  ---
  duration_ms: 2.081124
  ...
# Subtest: Ctrl+[ closes from focused card controls, the Back button, and the modal frame
ok 3321 - Ctrl+[ closes from focused card controls, the Back button, and the modal frame
  ---
  duration_ms: 2.784006
  ...
# Subtest: a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
ok 3322 - a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape
  ---
  duration_ms: 6.322847
  ...
# Subtest: a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
ok 3323 - a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key
  ---
  duration_ms: 6.659077
  ...
# Subtest: a direct dependency stage closes on Ctrl+[ but keeps q as typed text
ok 3324 - a direct dependency stage closes on Ctrl+[ but keeps q as typed text
  ---
  duration_ms: 0.648459
  ...
# Subtest: q and Ctrl+[ are not global closes: other modals and the decay card ignore them
ok 3325 - q and Ctrl+[ are not global closes: other modals and the decay card ignore them
  ---
  duration_ms: 0.888657
  ...
# Subtest: missing freshness API disables Review every with an honest reason
ok 3326 - missing freshness API disables Review every with an honest reason
  ---
  duration_ms: 0.696169
  ...
# Subtest: child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
ok 3327 - child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions
  ---
  duration_ms: 1.213107
  ...
# Subtest: decay card keeps its classes and shares key-card tokens
ok 3328 - decay card keeps its classes and shares key-card tokens
  ---
  duration_ms: 0.141971
  ...
# Subtest: decay card footer always names the X drop alias; the trial date is not this gate
ok 3329 - decay card footer always names the X drop alias; the trial date is not this gate
  ---
  duration_ms: 0.306245
  ...
# Subtest: task card level chips reuse the shared priority mark when available
ok 3330 - task card level chips reuse the shared priority mark when available
  ---
  duration_ms: 1.040427
  ...
# Subtest: task card labels are unchanged without the priority mark api
ok 3331 - task card labels are unchanged without the priority mark api
  ---
  duration_ms: 3.371578
  ...
# Subtest: manifest order is authoritative and fragments share one lexical scope
ok 3332 - manifest order is authoritative and fragments share one lexical scope
  ---
  duration_ms: 122.127315
  ...
# Subtest: builds are deterministic and build:check is read-only on success
ok 3333 - builds are deterministic and build:check is read-only on success
  ---
  duration_ms: 177.032197
  ...
# Subtest: read-only check rejects changed fragments and edited generated output
ok 3334 - read-only check rejects changed fragments and edited generated output
  ---
  duration_ms: 179.939549
  ...
# Subtest: check rejects a missing generated bundle without writing it
ok 3335 - check rejects a missing generated bundle without writing it
  ---
  duration_ms: 54.962882
  ...
# Subtest: fragment line limit is enforced before writing output
ok 3336 - fragment line limit is enforced before writing output
  ---
  duration_ms: 3.367551
  ...
# Subtest: fragment syntax errors are rejected before writing output
ok 3337 - fragment syntax errors are rejected before writing output
  ---
  duration_ms: 38.254194
  ...
# Subtest: malformed, empty, duplicate, and traversal manifests are rejected read-only
    # Subtest: invalid JSON
    ok 1 - invalid JSON
      ---
      duration_ms: 0.733912
      ...
    # Subtest: empty manifest
    ok 2 - empty manifest
      ---
      duration_ms: 0.597081
      ...
    # Subtest: non-array manifest
    ok 3 - non-array manifest
      ---
      duration_ms: 0.598954
      ...
    # Subtest: duplicate entries
    ok 4 - duplicate entries
      ---
      duration_ms: 25.698346
      ...
    # Subtest: traversal entry
    ok 5 - traversal entry
      ---
      duration_ms: 0.627379
      ...
    # Subtest: absolute entry
    ok 6 - absolute entry
      ---
      duration_ms: 0.437065
      ...
    1..6
ok 3338 - malformed, empty, duplicate, and traversal manifests are rejected read-only
  ---
  duration_ms: 29.654071
  ...
# Subtest: missing and omitted fragments are rejected read-only
    # Subtest: missing manifest entry
    ok 1 - missing manifest entry
      ---
      duration_ms: 0.564157
      ...
    # Subtest: unlisted JavaScript source
    ok 2 - unlisted JavaScript source
      ---
      duration_ms: 25.647508
      ...
    1..2
ok 3339 - missing and omitted fragments are rejected read-only
  ---
  duration_ms: 26.537979
  ...
# Subtest: escaping fragment symlinks are rejected read-only
ok 3340 - escaping fragment symlinks are rejected read-only
  ---
  duration_ms: 1.608873
  ...
# Subtest: parity comparator identifies changed helper and plugin methods
ok 3341 - parity comparator identifies changed helper and plugin methods
  ---
  duration_ms: 17.731861
  ...
# Subtest: parity comparator accepts a mixin-split helper class but not a changed method or superclass
ok 3342 - parity comparator accepts a mixin-split helper class but not a changed method or superclass
  ---
  duration_ms: 0.687412
  ...
# Subtest: snapshot commands are available only for active Markdown files
ok 3343 - snapshot commands are available only for active Markdown files
  ---
  duration_ms: 1.676451
  ...
# Subtest: commands run bob ref create on the active path, with -C for closed tasks
ok 3344 - commands run bob ref create on the active path, with -C for closed tasks
  ---
  duration_ms: 4.85852
  ...
# Subtest: bob spawn uses the resolved path, vault environment, timeout, and NO_COLOR
ok 3345 - bob spawn uses the resolved path, vault environment, timeout, and NO_COLOR
  ---
  duration_ms: 1.755513
  ...
# Subtest: failure notices retain bob error and hint lines verbatim
ok 3346 - failure notices retain bob error and hint lines verbatim
  ---
  duration_ms: 0.453767
  ...
# Subtest: snapshot runs through api.commandMode when version 1 is available
ok 3347 - snapshot runs through api.commandMode when version 1 is available
  ---
  duration_ms: 2.674256
  ...
# Subtest: snapshot falls back to the legacy spawn without command mode
ok 3348 - snapshot falls back to the legacy spawn without command mode
  ---
  duration_ms: 0.445551
  ...
# Subtest: snapshot falls back to the legacy spawn when command mode is older than v1
ok 3349 - snapshot falls back to the legacy spawn when command mode is older than v1
  ---
  duration_ms: 0.27777
  ...
# Subtest: a refused command-mode run keeps the legacy error notice and never spawns
ok 3350 - a refused command-mode run keeps the legacy error notice and never spawns
  ---
  duration_ms: 0.264145
  ...
# Subtest: off desktop, bob spawning is refused with the desktop-app explanation
ok 3351 - off desktop, bob spawning is refused with the desktop-app explanation
  ---
  duration_ms: 0.314591
  ...
# Subtest: both prompt copies pass the shared fixture table identically
ok 3352 - both prompt copies pass the shared fixture table identically
  ---
  duration_ms: 9.528196
  ...
# Subtest: suggestion is valid, compact, and collision-aware
ok 3353 - suggestion is valid, compact, and collision-aware
  ---
  duration_ms: 0.900139
  ...
# Subtest: rename excludes exactly one old-ID occurrence
ok 3354 - rename excludes exactly one old-ID occurrence
  ---
  duration_ms: 0.276819
  ...
# Subtest: dependency legacy [id::] reuses only valid free IDs
ok 3355 - dependency legacy [id::] reuses only valid free IDs
  ---
  duration_ms: 0.582232
  ...
# Subtest: project conversion keeps the existing suggestBlockIdFromTask
ok 3356 - project conversion keeps the existing suggestBlockIdFromTask
  ---
  duration_ms: 1.195433
  ...
# Subtest: successor SB vectors are unchanged
ok 3357 - successor SB vectors are unchanged
  ---
  duration_ms: 1.307026
  ...
# Subtest: Linked-from CURRENT lists every checkbox status from the live index
ok 3358 - Linked-from CURRENT lists every checkbox status from the live index
  ---
  duration_ms: 25.164927
  ...
# Subtest: option-bracket ring reads Blocked as a source-only slot ahead of Ready
ok 3359 - option-bracket ring reads Blocked as a source-only slot ahead of Ready
  ---
  duration_ms: 1.441673
  ...
# Subtest: isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
ok 3360 - isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it
  ---
  duration_ms: 0.355098
  ...
# Subtest: option-bracket refuses to change a member while its project is Blocked
ok 3361 - option-bracket refuses to change a member while its project is Blocked
  ---
  duration_ms: 2.623089
  ...
# Subtest: tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
ok 3362 - tagged inherited ^prj remains Blocked, refuses cycling, and names its parent
  ---
  duration_ms: 1.70199
  ...
# Subtest: project resident notice reads the inline ^prj date and ignores frontmatter scheduled
ok 3363 - project resident notice reads the inline ^prj date and ignores frontmatter scheduled
  ---
  duration_ms: 0.526556
  ...
# Subtest: findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
ok 3364 - findSingleFutureScheduledField validates form, field order, and the strictly-future boundary
  ---
  duration_ms: 0.305494
  ...
# Subtest: field removal collapses only the exposed span and preserves the rest of the line
ok 3365 - field removal collapses only the exposed span and preserves the rest of the line
  ---
  duration_ms: 0.268643
  ...
# Subtest: vault-path retirement preserves CRLF and a missing final newline
ok 3366 - vault-path retirement preserves CRLF and a missing final newline
  ---
  duration_ms: 0.91632
  ...
# Subtest: Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
ok 3367 - Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker
  ---
  duration_ms: 0.627638
  ...
# Subtest: Schedule Log discovery ignores a marker owned by a nested grandchild
ok 3368 - Schedule Log discovery ignores a marker owned by a nested grandchild
  ---
  duration_ms: 0.406466
  ...
# Subtest: Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
ok 3369 - Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries
  ---
  duration_ms: 0.486369
  ...
# Subtest: a task with no Schedule Log gets its field retired without any insertion or new marker
ok 3370 - a task with no Schedule Log gets its field retired without any insertion or new marker
  ---
  duration_ms: 0.14121
  ...
# Subtest: Schedule Log entry uses the canonical arrow, dash, and lock bytes
ok 3371 - Schedule Log entry uses the canonical arrow, dash, and lock bytes
  ---
  duration_ms: 0.101834
  ...
# Subtest: retirement stays a no-op for shapes that are not proof of a blocking date
ok 3372 - retirement stays a no-op for shapes that are not proof of a blocking date
  ---
  duration_ms: 0.175626
  ...
# Subtest: cycling Blocked backward to Cancelled retires the date and logs, matching forward
ok 3373 - cycling Blocked backward to Cancelled retires the date and logs, matching forward
  ---
  duration_ms: 4.219198
  ...
# Subtest: single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
ok 3374 - single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write
  ---
  duration_ms: 1.175155
  ...
# Subtest: counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
ok 3375 - counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker
  ---
  duration_ms: 1.65979
  ...
# Subtest: counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
ok 3376 - counted range accounts for a cursor-line Tasks-command insertion when targeting later lines
  ---
  duration_ms: 0.73837
  ...
# Subtest: transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
ok 3377 - transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note
  ---
  duration_ms: 2.070895
  ...
# Subtest: pressing again after Blocked retirement performs an ordinary transition with no further changes
ok 3378 - pressing again after Blocked retirement performs an ordinary transition with no further changes
  ---
  duration_ms: 0.305774
  ...
# Subtest: Alt+] on a date-blocked ^prj recovers open residents in step
ok 3379 - Alt+] on a date-blocked ^prj recovers open residents in step
  ---
  duration_ms: 18.201958
  ...
# Subtest: Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
ok 3380 - Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains
  ---
  duration_ms: 1.887344
  ...
# Subtest: planProjectResidentRecoveryEdits recovers when a cross-note id is not open
ok 3381 - planProjectResidentRecoveryEdits recovers when a cross-note id is not open
  ---
  duration_ms: 0.631376
  ...
# Subtest: Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
ok 3382 - Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed
  ---
  duration_ms: 2.049715
  ...
# Subtest: Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
ok 3383 - Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason
  ---
  duration_ms: 1.500837
  ...
# Subtest: Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
ok 3384 - Alt+[ on a [?] ^prj to Cancelled recovers tagged residents
  ---
  duration_ms: 2.25145
  ...
# Subtest: cycling a transcluded ^prj recovers residents in the source note
ok 3385 - cycling a transcluded ^prj recovers residents in the source note
  ---
  duration_ms: 1.238796
  ...
# Subtest: cycler BK1–BK12 accept and empty
ok 3386 - cycler BK1–BK12 accept and empty
  ---
  duration_ms: 1.554699
  ...
# Subtest: cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded
ok 3387 - cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded
  ---
  duration_ms: 0.866826
  ...
# Subtest: cycler MC4 strike/restore skip BLOCKS lines
ok 3388 - cycler MC4 strike/restore skip BLOCKS lines
  ---
  duration_ms: 1.185825
  ...
# Subtest: cycler MC3 tree close skips BLOCKS embeds
ok 3389 - cycler MC3 tree close skips BLOCKS embeds
  ---
  duration_ms: 1.160987
  ...
# Subtest: cycler MC1/MC2 Pomodoro and successor scanners skip managed lines
ok 3390 - cycler MC1/MC2 Pomodoro and successor scanners skip managed lines
  ---
  duration_ms: 1.54453
  ...
# Subtest: cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS
ok 3391 - cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS
  ---
  duration_ms: 0.304692
  ...
# Subtest: range planner preserves every single-item mode without an effective count
ok 3392 - range planner preserves every single-item mode without an effective count
  ---
  duration_ms: 9.831988
  ...
# Subtest: item counts carry children, skip blank lines and loose continuations, and clamp
ok 3393 - item counts carry children, skip blank lines and loose continuations, and clamp
  ---
  duration_ms: 0.399883
  ...
# Subtest: range stops at headings, shallower lines, same-level paragraphs and fences
ok 3394 - range stops at headings, shallower lines, same-level paragraphs and fences
  ---
  duration_ms: 0.232975
  ...
# Subtest: siblings require the exact whitespace and blockquote prefix
ok 3395 - siblings require the exact whitespace and blockquote prefix
  ---
  duration_ms: 0.203648
  ...
# Subtest: counted demotion moves four complete blocks to one existing section
ok 3396 - counted demotion moves four complete blocks to one existing section
  ---
  duration_ms: 4.545239
  ...
# Subtest: counted demotion creates a typed section or one default Requirements section
ok 3397 - counted demotion creates a typed section or one default Requirements section
  ---
  duration_ms: 2.476559
  ...
# Subtest: bottom-up removal splices blank seams and maps destinations before the source
ok 3398 - bottom-up removal splices blank seams and maps destinations before the source
  ---
  duration_ms: 0.495396
  ...
# Subtest: counted promotion Enter appends tasks in order and removes an emptied source section
ok 3399 - counted promotion Enter appends tasks in order and removes an emptied source section
  ---
  duration_ms: 1.207325
  ...
# Subtest: counted promotion to existing or new non-Tasks destinations keeps all bullets plain
ok 3400 - counted promotion to existing or new non-Tasks destinations keeps all bullets plain
  ---
  duration_ms: 0.517428
  ...
# Subtest: same-source Tasks promotion rewrites all selected lines in place
ok 3401 - same-source Tasks promotion rewrites all selected lines in place
  ---
  duration_ms: 1.155536
  ...
# Subtest: counted demotion outside Tasks moves to the next section in one write
ok 3402 - counted demotion outside Tasks moves to the next section in one write
  ---
  duration_ms: 0.430863
  ...
# Subtest: in-place ranges write once without centering for nested, non-dash, and unrouted items
ok 3403 - in-place ranges write once without centering for nested, non-dash, and unrouted items
  ---
  duration_ms: 1.000852
  ...
# Subtest: mixed demotion ranges count unchanged siblings and only move top-level dash tasks
ok 3404 - mixed demotion ranges count unchanged siblings and only move top-level dash tasks
  ---
  duration_ms: 0.429931
  ...
# Subtest: mixed promotion preserves existing tasks and a nonempty source section
ok 3405 - mixed promotion preserves existing tasks and a nonempty source section
  ---
  duration_ms: 0.23033
  ...
# Subtest: Vim action consumes explicit additional-item counts and preserves bare behavior
ok 3406 - Vim action consumes explicit additional-item counts and preserves bare behavior
  ---
  duration_ms: 7.130207
  ...
# Subtest: command checking preserves pending count; execution consumes it once and resets Vim
ok 3407 - command checking preserves pending count; execution consumes it once and resets Vim
  ---
  duration_ms: 1.318689
  ...
# Subtest: command route stays single without normal-mode explicit count and supports in-place ranges
ok 3408 - command route stays single without normal-mode explicit count and supports in-place ranges
  ---
  duration_ms: 0.58127
  ...
# Subtest: picker displays at most five preview rows plus overflow; single picker is unchanged
ok 3409 - picker displays at most five preview rows plus overflow; single picker is unchanged
  ---
  duration_ms: 2.212696
  ...
# Subtest: stale counted picker and cancelled picker never write
ok 3410 - stale counted picker and cancelled picker never write
  ---
  duration_ms: 1.224198
  ...
# Subtest: counted moves round-trip CRLF and preserve the presence or absence of a final newline
ok 3411 - counted moves round-trip CRLF and preserve the presence or absence of a final newline
  ---
  duration_ms: 3.088168
  ...
# Subtest: direct open/done transitions include incomplete statuses without broadening excluded statuses
ok 3412 - direct open/done transitions include incomplete statuses without broadening excluded statuses
  ---
  duration_ms: 1.374545
  ...
# Subtest: Ctrl+Enter block-link selection recognizes live and retired forms
ok 3413 - Ctrl+Enter block-link selection recognizes live and retired forms
  ---
  duration_ms: 2.266488
  ...
# Subtest: Pomodoro child ownership is status-neutral and bounded by contiguous list structure
ok 3414 - Pomodoro child ownership is status-neutral and bounded by contiguous list structure
  ---
  duration_ms: 1.199621
  ...
# Subtest: daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
ok 3415 - daily-note paths follow the canonical YYYY/YYYYMMDD.md layout
  ---
  duration_ms: 0.312526
  ...
# Subtest: parsePomodoroEntryLineParts reads placeholder and range names conservatively
ok 3416 - parsePomodoroEntryLineParts reads placeholder and range names conservatively
  ---
  duration_ms: 0.850624
  ...
# Subtest: formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
ok 3417 - formatPomodoroPlaceholderLine keeps unnamed placeholders canonical
  ---
  duration_ms: 0.168091
  ...
# Subtest: Pomodoro bullet toggle accepts empty indented list items
ok 3418 - Pomodoro bullet toggle accepts empty indented list items
  ---
  duration_ms: 0.295404
  ...
# Subtest: Pomodoro bullet toggle rejects non-empty or out-of-section bullets
ok 3419 - Pomodoro bullet toggle rejects non-empty or out-of-section bullets
  ---
  duration_ms: 0.216253
  ...
# Subtest: Pomodoro bullet toggle reverses only empty open childless placeholders
ok 3420 - Pomodoro bullet toggle reverses only empty open childless placeholders
  ---
  duration_ms: 0.486599
  ...
# Subtest: Pomodoro bullet toggle reverses named empty open childless placeholders
ok 3421 - Pomodoro bullet toggle reverses named empty open childless placeholders
  ---
  duration_ms: 0.385947
  ...
# Subtest: Pomodoro bullet toggle round trips and normalizes child indentation
ok 3422 - Pomodoro bullet toggle round trips and normalizes child indentation
  ---
  duration_ms: 0.257913
  ...
# Subtest: Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
ok 3423 - Pomodoro bullet toggle changes only the eligible line in a realistic daily shape
  ---
  duration_ms: 0.152742
  ...
# Subtest: Pomodoro toggle key gate does not shadow bare Option bracket cycling
ok 3424 - Pomodoro toggle key gate does not shadow bare Option bracket cycling
  ---
  duration_ms: 0.187899
  ...
# Subtest: Pomodoro toggle command is daily-only and places the cursor for both directions
ok 3425 - Pomodoro toggle command is daily-only and places the cursor for both directions
  ---
  duration_ms: 0.765311
  ...
# Subtest: Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
ok 3426 - Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through
  ---
  duration_ms: 0.357222
  ...
# Subtest: Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
ok 3427 - Vim Ctrl+Enter dispatches task transitions and restores a reopened identity
  ---
  duration_ms: 2.435101
  ...
# Subtest: Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
ok 3428 - Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents
  ---
  duration_ms: 25.406168
  ...
# Subtest: Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
ok 3429 - Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references
  ---
  duration_ms: 1.867867
  ...
# Subtest: Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
ok 3430 - Ctrl+Enter reopening the local line over an already-open target does not accidentally close it
  ---
  duration_ms: 2.12524
  ...
# Subtest: Ctrl+Enter closing the local line over an already-closed target does not write it a second time
ok 3431 - Ctrl+Enter closing the local line over an already-closed target does not write it a second time
  ---
  duration_ms: 0.819956
  ...
# Subtest: Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
ok 3432 - Ctrl+Enter hands off a claimed walk landing before Pomodoro handling
  ---
  duration_ms: 0.71709
  ...
# Subtest: Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
ok 3433 - Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws
  ---
  duration_ms: 1.745874
  ...
# Subtest: Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
ok 3434 - Ctrl+Enter consumes a rejected nav claim without an unhandled rejection
  ---
  duration_ms: 0.600477
  ...
# Subtest: Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
ok 3435 - Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error
  ---
  duration_ms: 0.762266
  ...
# Subtest: Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
ok 3436 - Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line
  ---
  duration_ms: 0.95313
  ...
# Subtest: Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
ok 3437 - Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion
  ---
  duration_ms: 0.821298
  ...
# Subtest: getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
ok 3438 - getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws
  ---
  duration_ms: 0.404773
  ...
# Subtest: Ctrl+Enter close continues the walk with complete after finalize ran
ok 3439 - Ctrl+Enter close continues the walk with complete after finalize ran
  ---
  duration_ms: 15.559001
  ...
# Subtest: Ctrl+Enter close continues only after transclusion propagation landed
ok 3440 - Ctrl+Enter close continues only after transclusion propagation landed
  ---
  duration_ms: 13.731956
  ...
# Subtest: Ctrl+Enter reopen settles the walk with null
ok 3441 - Ctrl+Enter reopen settles the walk with null
  ---
  duration_ms: 11.584101
  ...
# Subtest: Ctrl+Enter swallows the key with no write while the walk is busy
ok 3442 - Ctrl+Enter swallows the key with no write while the walk is busy
  ---
  duration_ms: 11.192977
  ...
# Subtest: Ctrl+Enter with a null capture behaves exactly like today
ok 3443 - Ctrl+Enter with a null capture behaves exactly like today
  ---
  duration_ms: 11.575534
  ...
# Subtest: Ctrl+Enter with nav v2 or no nav keeps today's behavior
ok 3444 - Ctrl+Enter with nav v2 or no nav keeps today's behavior
  ---
  duration_ms: 20.759916
  ...
# Subtest: Ctrl+Enter lets the checklist claim win before capturing
ok 3445 - Ctrl+Enter lets the checklist claim win before capturing
  ---
  duration_ms: 0.581952
  ...
# Subtest: Ctrl+Enter settles the walk with null when the toggle rejects
ok 3446 - Ctrl+Enter settles the walk with null when the toggle rejects
  ---
  duration_ms: 12.4685
  ...
# Subtest: Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
ok 3447 - Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write
  ---
  duration_ms: 2.897172
  ...
# Subtest: eligible Tasks demotions prompt in project and non-project notes
ok 3448 - eligible Tasks demotions prompt in project and non-project notes
  ---
  duration_ms: 3.643588
  ...
# Subtest: selectable headings skip YAML, fences, empty titles, and Tasks
ok 3449 - selectable headings skip YAML, fences, empty titles, and Tasks
  ---
  duration_ms: 1.278301
  ...
# Subtest: duplicate heading identities stay distinct and route to the chosen occurrence
ok 3450 - duplicate heading identities stay distinct and route to the chosen occurrence
  ---
  duration_ms: 1.349357
  ...
# Subtest: demotion picker defaults and typed names resolve without synthetic duplicates
ok 3451 - demotion picker defaults and typed names resolve without synthetic duplicates
  ---
  duration_ms: 2.491207
  ...
# Subtest: picker keyboard state wraps, clamps, and refuses invalid Enter
ok 3452 - picker keyboard state wraps, clamps, and refuses invalid Enter
  ---
  duration_ms: 0.459528
  ...
# Subtest: new-section formatting keeps extra blanks, final newlines, and nested children
ok 3453 - new-section formatting keeps extra blanks, final newlines, and nested children
  ---
  duration_ms: 1.001122
  ...
# Subtest: existing-section insertion works before and after the source on CRLF-backed editors
ok 3454 - existing-section insertion works before and after the source on CRLF-backed editors
  ---
  duration_ms: 4.12121
  ...
# Subtest: command opens one picker, writes only on accept, and restores cursor plus center
ok 3455 - command opens one picker, writes only on accept, and restores cursor plus center
  ---
  duration_ms: 1.24614
  ...
# Subtest: pointer activation, Escape, and double-submit protection leave a consistent note
ok 3456 - pointer activation, Escape, and double-submit protection leave a consistent note
  ---
  duration_ms: 1.598322
  ...
# Subtest: stale document, changed editor, or missing heading notice without writing
ok 3457 - stale document, changed editor, or missing heading notice without writing
  ---
  duration_ms: 4.494584
  ...
# Subtest: dependency normalizer writes path-qualified IDs and is idempotent
ok 3458 - dependency normalizer writes path-qualified IDs and is idempotent
  ---
  duration_ms: 3.053
  ...
# Subtest: Tasks-generated IDs become local block IDs when none exists
ok 3459 - Tasks-generated IDs become local block IDs when none exists
  ---
  duration_ms: 1.007334
  ...
# Subtest: note rename rewrites target IDs and yields exact propagation mappings
ok 3460 - note rename rewrites target IDs and yields exact propagation mappings
  ---
  duration_ms: 0.310253
  ...
# Subtest: note rename also rewrites same-file dependsOn references
ok 3461 - note rename also rewrites same-file dependsOn references
  ---
  duration_ms: 0.255978
  ...
# Subtest: dependency normalization skips unsupported paths and fenced examples
ok 3462 - dependency normalization skips unsupported paths and fenced examples
  ---
  duration_ms: 0.376288
  ...
# Subtest: blocked-dependent planner matches the CLI dependency truth table
ok 3463 - blocked-dependent planner matches the CLI dependency truth table
  ---
  duration_ms: 3.778906
  ...
# Subtest: blocked-dependent edits preserve EOLs and skip stale lines idempotently
ok 3464 - blocked-dependent edits preserve EOLs and skip stale lines idempotently
  ---
  duration_ms: 1.161809
  ...
# Subtest: project recovery strips resident tags and works without freshness v12
ok 3465 - project recovery strips resident tags and works without freshness v12
  ---
  duration_ms: 1.672594
  ...
# Subtest: recovery passes daily-note and Today skip flags to ledger freshness
ok 3466 - recovery passes daily-note and Today skip flags to ledger freshness
  ---
  duration_ms: 0.464547
  ...
# Subtest: normalization mappings propagate to every dependent file
ok 3467 - normalization mappings propagate to every dependent file
  ---
  duration_ms: 1.258202
  ...
# Subtest: runtime normalizer skips unsupported paths with one informative notice
ok 3468 - runtime normalizer skips unsupported paths with one informative notice
  ---
  duration_ms: 0.722319
  ...
# Subtest: rename reconciliation rewrites the target and every dependent
ok 3469 - rename reconciliation rewrites the target and every dependent
  ---
  duration_ms: 0.602992
  ...
# Subtest: editor dependency normalization abandons and reschedules stale snapshots
ok 3470 - editor dependency normalization abandons and reschedules stale snapshots
  ---
  duration_ms: 0.523399
  ...
# Subtest: rename reconciliation abandons and reschedules stale editor snapshots
ok 3471 - rename reconciliation abandons and reschedules stale editor snapshots
  ---
  duration_ms: 0.263383
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 3472 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.839604
  ...
# Subtest: close-time retirement skips Depends-On lines
ok 3473 - close-time retirement skips Depends-On lines
  ---
  duration_ms: 1.234257
  ...
# Subtest: reopen restoration skips Depends-On lines instead of re-embedding them
ok 3474 - reopen restoration skips Depends-On lines instead of re-embedding them
  ---
  duration_ms: 0.610075
  ...
# Subtest: embedded-tree close collection ignores Depends-On lines
ok 3475 - embedded-tree close collection ignores Depends-On lines
  ---
  duration_ms: 0.313038
  ...
# Subtest: Alt-bracket bullet formatting never applies to Depends-On lines
ok 3476 - Alt-bracket bullet formatting never applies to Depends-On lines
  ---
  duration_ms: 0.537777
  ...
# Subtest: Ctrl+Enter on a dependency link closes only the target and runs the recovery
ok 3477 - Ctrl+Enter on a dependency link closes only the target and runs the recovery
  ---
  duration_ms: 1.710036
  ...
# Subtest: Ctrl+Enter on a dependency link reopens only the target, root-only
ok 3478 - Ctrl+Enter on a dependency link reopens only the target, root-only
  ---
  duration_ms: 1.194261
  ...
# Subtest: single and counted Alt-bracket cycle the dependency target under the cursor
ok 3479 - single and counted Alt-bracket cycle the dependency target under the cursor
  ---
  duration_ms: 16.212741
  ...
# Subtest: single and counted Alt-bracket report when the cursor is off every dependency link
ok 3480 - single and counted Alt-bracket report when the cursor is off every dependency link
  ---
  duration_ms: 0.649971
  ...
# Subtest: Ctrl+Enter candidate resolution finds plain links on Depends-On lines
ok 3481 - Ctrl+Enter candidate resolution finds plain links on Depends-On lines
  ---
  duration_ms: 0.208268
  ...
# Subtest: dependency-id normalisation never edits Depends-On lines
ok 3482 - dependency-id normalisation never edits Depends-On lines
  ---
  duration_ms: 0.283962
  ...
# Subtest: note rename rewrites fields while leaving Depends-On lines alone
ok 3483 - note rename rewrites fields while leaving Depends-On lines alone
  ---
  duration_ms: 0.175125
  ...
# Subtest: recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
ok 3484 - recoverBlockedDependents leaves a closed tagged resident untouched (PDT7)
  ---
  duration_ms: 1.836306
  ...
# Subtest: cycler freshness: local-fallback rewrite stamps last via injected stamper
ok 3485 - cycler freshness: local-fallback rewrite stamps last via injected stamper
  ---
  duration_ms: 2.473895
  ...
# Subtest: cycler freshness: rewrites without a stamper are unchanged (identity default)
ok 3486 - cycler freshness: rewrites without a stamper are unchanged (identity default)
  ---
  duration_ms: 0.513381
  ...
# Subtest: cycler freshness: a throwing stamper leaves the rewritten line intact
ok 3487 - cycler freshness: a throwing stamper leaves the rewritten line intact
  ---
  duration_ms: 0.341172
  ...
# Subtest: cycler line guard skips Pomodoro signatures before injected stampers
ok 3488 - cycler line guard skips Pomodoro signatures before injected stampers
  ---
  duration_ms: 0.422426
  ...
# Subtest: cycler skips legacy Pomodoro headlines in local and Tasks-command writes
ok 3489 - cycler skips legacy Pomodoro headlines in local and Tasks-command writes
  ---
  duration_ms: 2.029396
  ...
# Subtest: cycler freshness: transcluded rewrite stamps last via injected stamper
ok 3490 - cycler freshness: transcluded rewrite stamps last via injected stamper
  ---
  duration_ms: 0.252923
  ...
# Subtest: cycler freshness: cycling a plain line stamps through the follow-up edit
ok 3491 - cycler freshness: cycling a plain line stamps through the follow-up edit
  ---
  duration_ms: 0.464557
  ...
# Subtest: cycler freshness: Tasks-command rewrite with the expected status is stamped
ok 3492 - cycler freshness: Tasks-command rewrite with the expected status is stamped
  ---
  duration_ms: 0.394905
  ...
# Subtest: cycler freshness: Tasks command that inserts a line never stamps
ok 3493 - cycler freshness: Tasks command that inserts a line never stamps
  ---
  duration_ms: 0.534991
  ...
# Subtest: cycler freshness: Tasks command that deletes the line never stamps the next task
ok 3494 - cycler freshness: Tasks command that deletes the line never stamps the next task
  ---
  duration_ms: 0.453206
  ...
# Subtest: cycler freshness: Tasks command that leaves a different status never stamps
ok 3495 - cycler freshness: Tasks command that leaves a different status never stamps
  ---
  duration_ms: 0.257692
  ...
# Subtest: cycler freshness: cycling without ledger-tools writes no stamp
ok 3496 - cycler freshness: cycling without ledger-tools writes no stamp
  ---
  duration_ms: 0.171508
  ...
# Subtest: cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
ok 3497 - cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
  ---
  duration_ms: 0.128655
  ...
# Subtest: Pomodoro marker helpers normalize every block link and preserve fences and EOLs
ok 3498 - Pomodoro marker helpers normalize every block link and preserve fences and EOLs
  ---
  duration_ms: 3.432545
  ...
# Subtest: completed Pomodoro markers are normalized per occurrence
ok 3499 - completed Pomodoro markers are normalized per occurrence
  ---
  duration_ms: 0.659951
  ...
# Subtest: move-only Pomodoro links require a strict immediate hash directive
ok 3500 - move-only Pomodoro links require a strict immediate hash directive
  ---
  duration_ms: 3.001553
  ...
# Subtest: Pomodoro move-only planner toggles links across additional physical lines
ok 3501 - Pomodoro move-only planner toggles links across additional physical lines
  ---
  duration_ms: 1.39258
  ...
# Subtest: Pomodoro move-only planner round trips exact text and rejects strict non-matches
ok 3502 - Pomodoro move-only planner round trips exact text and rejects strict non-matches
  ---
  duration_ms: 0.582212
  ...
# Subtest: bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
ok 3503 - bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor
  ---
  duration_ms: 1.951818
  ...
# Subtest: Pomodoro move-only runtime removes locally and validates additions independently
ok 3504 - Pomodoro move-only runtime removes locally and validates additions independently
  ---
  duration_ms: 1.262661
  ...
# Subtest: Pomodoro move-only runtime protects live lines after asynchronous failures
ok 3505 - Pomodoro move-only runtime protects live lines after asynchronous failures
  ---
  duration_ms: 0.498341
  ...
# Subtest: Pomodoro hash Vim mapping distinguishes bare and explicit repeats
ok 3506 - Pomodoro hash Vim mapping distinguishes bare and explicit repeats
  ---
  duration_ms: 13.205547
  ...
# Subtest: Pomodoro completion marks originals and carries clean live copies
ok 3507 - Pomodoro completion marks originals and carries clean live copies
  ---
  duration_ms: 2.438736
  ...
# Subtest: Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
ok 3508 - Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro
  ---
  duration_ms: 1.247282
  ...
# Subtest: Pomodoro completion carries the closed Pomodoro name onto created entries
ok 3509 - Pomodoro completion carries the closed Pomodoro name onto created entries
  ---
  duration_ms: 0.613461
  ...
# Subtest: buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
ok 3510 - buildPomodoroCompletionPlan groups a \#-marked bullet above several unmarked bullets
  ---
  duration_ms: 0.612039
  ...
# Subtest: buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
ok 3511 - buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet
  ---
  duration_ms: 0.399192
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is marked
ok 3512 - buildPomodoroCompletionPlan keeps source order when every carried link is marked
  ---
  duration_ms: 0.25654
  ...
# Subtest: buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
ok 3513 - buildPomodoroCompletionPlan keeps source order when every carried link is unmarked
  ---
  duration_ms: 0.279805
  ...
# Subtest: Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
ok 3514 - Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place
  ---
  duration_ms: 7.464547
  ...
# Subtest: deferred-only close deletes the emptied entry and carries stripped links
ok 3515 - deferred-only close deletes the emptied entry and carries stripped links
  ---
  duration_ms: 0.655362
  ...
# Subtest: deferred-only close at EOF leaves no dangling newline
ok 3516 - deferred-only close at EOF leaves no dangling newline
  ---
  duration_ms: 0.286567
  ...
# Subtest: a close with a remaining copyable link keeps the [x] entry
ok 3517 - a close with a remaining copyable link keeps the [x] entry
  ---
  duration_ms: 0.335791
  ...
# Subtest: a prose sibling keeps the closed entry on a deferred close
ok 3518 - a prose sibling keeps the closed entry on a deferred close
  ---
  duration_ms: 0.39273
  ...
# Subtest: Ctrl+Enter deferred-only close deletes the entry in one gesture
ok 3519 - Ctrl+Enter deferred-only close deletes the entry in one gesture
  ---
  duration_ms: 4.653055
  ...
# Subtest: deferred-only close keeps a separated prose child and deletes fence-only leftovers whole
ok 3520 - deferred-only close keeps a separated prose child and deletes fence-only leftovers whole
  ---
  duration_ms: 1.009838
  ...
# Subtest: deferred-only successor relocation uses the inserted placeholder
ok 3521 - deferred-only successor relocation uses the inserted placeholder
  ---
  duration_ms: 0.279694
  ...
# Subtest: selected Done Pomodoro transclusion reopens only its cross-file root
ok 3522 - selected Done Pomodoro transclusion reopens only its cross-file root
  ---
  duration_ms: 8.447822
  ...
# Subtest: selected same-file Done target reopens root-only in the live editor
ok 3523 - selected same-file Done target reopens root-only in the live editor
  ---
  duration_ms: 1.938462
  ...
# Subtest: selected retired link reopens its root and restores the historical occurrence
ok 3524 - selected retired link reopens its root and restores the historical occurrence
  ---
  duration_ms: 1.406186
  ...
# Subtest: incomplete selected Pomodoro transclusion still closes recursively
ok 3525 - incomplete selected Pomodoro transclusion still closes recursively
  ---
  duration_ms: 2.038293
  ...
# Subtest: Done Pomodoro reopens direct roots and clears only its block-link markers
ok 3526 - Done Pomodoro reopens direct roots and clears only its block-link markers
  ---
  duration_ms: 3.274994
  ...
# Subtest: reopening timed, placeholder, and legacy ledger rows never stamps the headline
ok 3527 - reopening timed, placeholder, and legacy ledger rows never stamps the headline
  ---
  duration_ms: 3.052269
  ...
# Subtest: Done Pomodoro reopen restores its own block reference after reopening direct roots
ok 3528 - Done Pomodoro reopen restores its own block reference after reopening direct roots
  ---
  duration_ms: 1.142081
  ...
# Subtest: Done Pomodoro markers remain when the Todo transition does not occur
ok 3529 - Done Pomodoro markers remain when the Todo transition does not occur
  ---
  duration_ms: 0.280416
  ...
# Subtest: registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
ok 3530 - registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
  ---
  duration_ms: 12.510179
  ...
# Subtest: registered Ctrl+Enter immediately recovers a same-file dependent
ok 3531 - registered Ctrl+Enter immediately recovers a same-file dependent
  ---
  duration_ms: 9.771022
  ...
# Subtest: registered Ctrl+Enter immediately recovers a cross-file dependent
ok 3532 - registered Ctrl+Enter immediately recovers a cross-file dependent
  ---
  duration_ms: 2.244616
  ...
# Subtest: child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
ok 3533 - child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
  ---
  duration_ms: 2.355738
  ...
# Subtest: Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
ok 3534 - Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
  ---
  duration_ms: 1.357683
  ...
# Subtest: selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
ok 3535 - selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
  ---
  duration_ms: 2.599704
  ...
# Subtest: selected unresolved or excluded embedded children are consumed as no-ops
ok 3536 - selected unresolved or excluded embedded children are consumed as no-ops
  ---
  duration_ms: 1.484404
  ...
# Subtest: Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
ok 3537 - Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
  ---
  duration_ms: 2.662424
  ...
# Subtest: Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
ok 3538 - Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies
  ---
  duration_ms: 2.693203
  ...
# Subtest: Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
ok 3539 - Pomodoro Work Log descendant tree keeps relative depth and drops blank lines
  ---
  duration_ms: 0.866895
  ...
# Subtest: Pomodoro Work Log note-group collection scopes to direct children and requires descendants
ok 3540 - Pomodoro Work Log note-group collection scopes to direct children and requires descendants
  ---
  duration_ms: 0.819755
  ...
# Subtest: Work Log entry body formats as *date* — summary
ok 3541 - Work Log entry body formats as *date* — summary
  ---
  duration_ms: 0.142261
  ...
# Subtest: buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
ok 3542 - buildWorkLogEntryLines dates depth-1 entries and drops an empty-bodied entry's whole subtree
  ---
  duration_ms: 0.22548
  ...
# Subtest: planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
ok 3543 - planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task
  ---
  duration_ms: 0.358374
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
ok 3544 - planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker
  ---
  duration_ms: 0.312577
  ...
# Subtest: planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
ok 3545 - planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling
  ---
  duration_ms: 0.183641
  ...
# Subtest: planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
ok 3546 - planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task
  ---
  duration_ms: 0.364025
  ...
# Subtest: planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
ok 3547 - planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs
  ---
  duration_ms: 0.385055
  ...
# Subtest: full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
ok 3548 - full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs
  ---
  duration_ms: 6.935884
  ...
# Subtest: full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
ok 3549 - full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion
  ---
  duration_ms: 1.84845
  ...
# Subtest: full Pomodoro completion keeps two same-task Work Log note sets in source order
ok 3550 - full Pomodoro completion keeps two same-task Work Log note sets in source order
  ---
  duration_ms: 1.263313
  ...
# Subtest: full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
ok 3551 - full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF
  ---
  duration_ms: 0.869691
  ...
# Subtest: full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
ok 3552 - full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing
  ---
  duration_ms: 0.852659
  ...
# Subtest: full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
ok 3553 - full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets
  ---
  duration_ms: 1.255648
  ...
# Subtest: PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
ok 3554 - PP22 pins \#hide bytes to normalize_task_hide_tag(line, false, true)
  ---
  duration_ms: 1.590677
  ...
# Subtest: PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
ok 3555 - PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules
  ---
  duration_ms: 0.853941
  ...
# Subtest: PP1 links the emptied project's ^prj as Next and strips \#hide
ok 3556 - PP1 links the emptied project's ^prj as Next and strips \#hide
  ---
  duration_ms: 11.852156
  ...
# Subtest: PP29 closing a child ^prj pulls in its empty parent project
ok 3557 - PP29 closing a child ^prj pulls in its empty parent project
  ---
  duration_ms: 2.410964
  ...
# Subtest: PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
ok 3558 - PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text
  ---
  duration_ms: 1.189261
  ...
# Subtest: PP30 keeps the parent untouched while another child or task remains
ok 3559 - PP30 keeps the parent untouched while another child or task remains
  ---
  duration_ms: 0.943191
  ...
# Subtest: PP31 skips missing, ambiguous, and non-project parents
ok 3560 - PP31 skips missing, ambiguous, and non-project parents
  ---
  duration_ms: 1.584205
  ...
# Subtest: PP33 cancellation surfaces the parent without linking it
ok 3561 - PP33 cancellation surfaces the parent without linking it
  ---
  duration_ms: 2.602429
  ...
# Subtest: PP2 and PP3 leave a project with remaining work alone
ok 3562 - PP2 and PP3 leave a project with remaining work alone
  ---
  duration_ms: 1.535472
  ...
# Subtest: PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
ok 3563 - PP4 hidden leftover still pulls in; PP5 fences vs remaining marks
  ---
  duration_ms: 3.342714
  ...
# Subtest: PP6 Sub-projects marker states match display_for_wikilink
ok 3564 - PP6 Sub-projects marker states match display_for_wikilink
  ---
  duration_ms: 1.467212
  ...
# Subtest: PP7 and PP28 keep a future-scheduled ^prj byte-identical
ok 3565 - PP7 and PP28 keep a future-scheduled ^prj byte-identical
  ---
  duration_ms: 0.967207
  ...
# Subtest: PP8 still-blocks a ^prj that waits on another open prerequisite
ok 3566 - PP8 still-blocks a ^prj that waits on another open prerequisite
  ---
  duration_ms: 0.695378
  ...
# Subtest: PP9 already-planned ^prj raises to Next without a new link
ok 3567 - PP9 already-planned ^prj raises to Next without a new link
  ---
  duration_ms: 0.643659
  ...
# Subtest: PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
ok 3568 - PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19)
  ---
  duration_ms: 2.736146
  ...
# Subtest: PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
ok 3569 - PP12 keeps In Progress; PP13 is silent for a visible already-linked Next
  ---
  duration_ms: 0.878047
  ...
# Subtest: PP14 an id-less last task still pulls in
ok 3570 - PP14 an id-less last task still pulls in
  ---
  duration_ms: 0.470458
  ...
# Subtest: PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
ok 3571 - PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired)
  ---
  duration_ms: 10.079919
  ...
# Subtest: PP17 one pull-in row wins over project_task
ok 3572 - PP17 one pull-in row wins over project_task
  ---
  duration_ms: 0.662835
  ...
# Subtest: PP18 cancel recovers only
ok 3573 - PP18 cancel recovers only
  ---
  duration_ms: 0.437886
  ...
# Subtest: PP20 unrecognised or unplannable notes never pull in
ok 3574 - PP20 unrecognised or unplannable notes never pull in
  ---
  duration_ms: 1.189161
  ...
# Subtest: PP24 closing an external prerequisite pulls in only when N is empty
ok 3575 - PP24 closing an external prerequisite pulls in only when N is empty
  ---
  duration_ms: 0.956156
  ...
# Subtest: PP25 cascades project_member recovery after a [?] pull-in
ok 3576 - PP25 cascades project_member recovery after a [?] pull-in
  ---
  duration_ms: 1.024787
  ...
# Subtest: PP26 dated recount treats a hidden leftover as remaining work
ok 3577 - PP26 dated recount treats a hidden leftover as remaining work
  ---
  duration_ms: 1.546534
  ...
# Subtest: PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
ok 3578 - PP27 implicit offer after \#hide strip; unpicked keeps WRITE rule (SO14/SO20)
  ---
  duration_ms: 1.055024
  ...
# Subtest: successorNoticeText uses the §12.6 pull-in and surfaced copy
ok 3579 - successorNoticeText uses the §12.6 pull-in and surfaced copy
  ---
  duration_ms: 0.475908
  ...
# Subtest: Ctrl+Enter on the last task link inserts the ^prj and rewrites R
ok 3580 - Ctrl+Enter on the last task link inserts the ^prj and rewrites R
  ---
  duration_ms: 11.286292
  ...
# Subtest: PP29 runtime close and reopen use the parent pull-in receipt
ok 3581 - PP29 runtime close and reopen use the parent pull-in receipt
  ---
  duration_ms: 5.656464
  ...
# Subtest: PP18 Alt+[ cancel of the last task surfaces R without linking
ok 3582 - PP18 Alt+[ cancel of the last task surfaces R without linking
  ---
  duration_ms: 19.388574
  ...
# Subtest: PP19 same-day reopen restores R byte-for-byte and takes back the link
ok 3583 - PP19 same-day reopen restores R byte-for-byte and takes back the link
  ---
  duration_ms: 3.168241
  ...
# Subtest: a close in a project that still has work stays inside the gate
ok 3584 - a close in a project that still has work stays inside the gate
  ---
  duration_ms: 1.059203
  ...
# Subtest: P1 path-qualified skip keys: same ^review in another note does not suppress
ok 3585 - P1 path-qualified skip keys: same ^review in another note does not suppress
  ---
  duration_ms: 0.495727
  ...
# Subtest: P3 id-less cascade: stale [?] R recovers resident without [id::]
ok 3586 - P3 id-less cascade: stale [?] R recovers resident without [id::]
  ---
  duration_ms: 0.482913
  ...
# Subtest: P4 frontmatter scheduled validity mirrors Rust
ok 3587 - P4 frontmatter scheduled validity mirrors Rust
  ---
  duration_ms: 0.50829
  ...
# Subtest: P5 recognition mirrors Rust (status/type/prj line)
ok 3588 - P5 recognition mirrors Rust (status/type/prj line)
  ---
  duration_ms: 1.62799
  ...
# Subtest: P6 SUBOPEN blank line stops the marker scan (PP6)
ok 3589 - P6 SUBOPEN blank line stops the marker scan (PP6)
  ---
  duration_ms: 0.582613
  ...
# Subtest: promotion prompts default to Tasks in ordinary and project notes
ok 3590 - promotion prompts default to Tasks in ordinary and project notes
  ---
  duration_ms: 4.305914
  ...
# Subtest: promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
ok 3591 - promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections
  ---
  duration_ms: 1.104821
  ...
# Subtest: promotion command writes only on accept and Enter selects Tasks
ok 3592 - promotion command writes only on accept and Enter selects Tasks
  ---
  duration_ms: 3.414882
  ...
# Subtest: promotion removes only genuinely empty source sections
ok 3593 - promotion removes only genuinely empty source sections
  ---
  duration_ms: 1.564829
  ...
# Subtest: promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
ok 3594 - promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing
  ---
  duration_ms: 1.488412
  ...
# Subtest: Tasks-only preamble promotions prompt and blank Enter moves into Tasks
ok 3595 - Tasks-only preamble promotions prompt and blank Enter moves into Tasks
  ---
  duration_ms: 1.036068
  ...
# Subtest: plain bullets already in Tasks prompt and blank Enter promotes in place
ok 3596 - plain bullets already in Tasks prompt and blank Enter promotes in place
  ---
  duration_ms: 1.080654
  ...
# Subtest: promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
ok 3597 - promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections
  ---
  duration_ms: 0.530202
  ...
# Subtest: always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
ok 3598 - always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation
  ---
  duration_ms: 4.03755
  ...
# Could not restore all reopened task references [ 'Broken.md: unreadable' ]
# Could not recover all blocked dependents [
#   'BrokenRead.md: read failed',
#   'Stale.md: line 1 changed before recovery',
#   'BrokenWrite.md: write failed'
# ]
# Subtest: direct Done Tasks task reopens through the metadata-aware fallback
ok 3599 - direct Done Tasks task reopens through the metadata-aware fallback
  ---
  duration_ms: 2.292077
  ...
# Subtest: recursive completion status policy includes Next without broadening excluded statuses
ok 3600 - recursive completion status policy includes Next without broadening excluded statuses
  ---
  duration_ms: 0.252222
  ...
# Subtest: recursive completion closes a Next root and its nested Next descendant
ok 3601 - recursive completion closes a Next root and its nested Next descendant
  ---
  duration_ms: 4.109248
  ...
# Subtest: recursive completion traverses Done parents and skips excluded siblings
ok 3602 - recursive completion traverses Done parents and skips excluded siblings
  ---
  duration_ms: 1.189693
  ...
# Subtest: closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
ok 3603 - closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent
  ---
  duration_ms: 1.553737
  ...
# Subtest: reopened-reference restoration is ancestry-aware, conservative, and idempotent
ok 3604 - reopened-reference restoration is ancestry-aware, conservative, and idempotent
  ---
  duration_ms: 1.512789
  ...
# Subtest: retirement preserves task-tree markers and unmarks Pomodoro embeds
ok 3605 - retirement preserves task-tree markers and unmarks Pomodoro embeds
  ---
  duration_ms: 0.373373
  ...
# Subtest: done Pomodoro retirement removes only the matching embedded marker
ok 3606 - done Pomodoro retirement removes only the matching embedded marker
  ---
  duration_ms: 0.249797
  ...
# Subtest: retirement stops at prose boundaries and pairs strikethrough spans
ok 3607 - retirement stops at prose boundaries and pairs strikethrough spans
  ---
  duration_ms: 0.43483
  ...
# Subtest: retired Pomodoro links are not copied into the next Pomodoro
ok 3608 - retired Pomodoro links are not copied into the next Pomodoro
  ---
  duration_ms: 1.354186
  ...
# Subtest: retirement coordinator rewrites active editor and vault notes together
ok 3609 - retirement coordinator rewrites active editor and vault notes together
  ---
  duration_ms: 1.015278
  ...
# Subtest: restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
ok 3610 - restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures
  ---
  duration_ms: 1.367581
  ...
# Subtest: close and reopen reference mutations share one serialized queue
ok 3611 - close and reopen reference mutations share one serialized queue
  ---
  duration_ms: 0.308408
  ...
# Subtest: post-close finalizer runs one gated plan before reference retirement
ok 3612 - post-close finalizer runs one gated plan before reference retirement
  ---
  duration_ms: 0.544891
  ...
# Subtest: dependent recovery uses live editor buffers and preserves the cursor
ok 3613 - dependent recovery uses live editor buffers and preserves the cursor
  ---
  duration_ms: 3.051377
  ...
# Subtest: dependent recovery preserves successful siblings across stale and failed notes
ok 3614 - dependent recovery preserves successful siblings across stale and failed notes
  ---
  duration_ms: 1.467122
  ...
# Subtest: no-op vault transforms and irrelevant retirement files avoid process writes
ok 3615 - no-op vault transforms and irrelevant retirement files avoid process writes
  ---
  duration_ms: 0.298821
  ...
# Subtest: ambiguity scans and notices are cached while dependency identity lines stay stable
ok 3616 - ambiguity scans and notices are cached while dependency identity lines stay stable
  ---
  duration_ms: 0.536655
  ...
# Subtest: non-Vim open/done command finalizes the closed task identity
ok 3617 - non-Vim open/done command finalizes the closed task identity
  ---
  duration_ms: 0.417187
  ...
# Subtest: non-Vim open/done command restores the reopened task identity
ok 3618 - non-Vim open/done command restores the reopened task identity
  ---
  duration_ms: 1.056227
  ...
# Subtest: full Pomodoro completion retires embeds only after carry-forward planning
ok 3619 - full Pomodoro completion retires embeds only after carry-forward planning
  ---
  duration_ms: 5.206132
  ...
# Subtest: full Pomodoro completion recovers after a deduplicated multi-target batch
ok 3620 - full Pomodoro completion recovers after a deduplicated multi-target batch
  ---
  duration_ms: 7.020619
  ...
# Subtest: full Pomodoro completion moves a marked same-note link without history
ok 3621 - full Pomodoro completion moves a marked same-note link without history
  ---
  duration_ms: 0.703644
  ...
# Subtest: closed-reference retirement never duplicates a daily Task Link into the completed fallback (bob-cli-2l)
ok 3622 - closed-reference retirement never duplicates a daily Task Link into the completed fallback (bob-cli-2l)
  ---
  duration_ms: 0.318027
  ...
# Subtest: cycler LK1–LK19 recognises only relation line shapes
ok 3623 - cycler LK1–LK19 recognises only relation line shapes
  ---
  duration_ms: 1.892984
  ...
# Subtest: cycler MC10, MC11, MC12 and MC14 keep relations inert while allowing root-only gestures
ok 3624 - cycler MC10, MC11, MC12 and MC14 keep relations inert while allowing root-only gestures
  ---
  duration_ms: 2.706138
  ...
# Subtest: SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
ok 3625 - SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header)
  ---
  duration_ms: 21.73111
  ...
# Subtest: SO2–SO5 fan-outs with explicit selection (SO32 twenty)
ok 3626 - SO2–SO5 fan-outs with explicit selection (SO32 twenty)
  ---
  duration_ms: 8.16379
  ...
# Subtest: SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
ok 3627 - SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref)
  ---
  duration_ms: 1.142211
  ...
# Subtest: SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
ok 3628 - SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel)
  ---
  duration_ms: 1.218607
  ...
# Subtest: SO stable keys survive insertions/status changes; ambiguous rebinding refused
ok 3629 - SO stable keys survive insertions/status changes; ambiguous rebinding refused
  ---
  duration_ms: 2.150127
  ...
# Subtest: SO picker model, pick normalization, and API detection
ok 3630 - SO picker model, pick normalization, and API detection
  ---
  duration_ms: 0.693785
  ...
# Subtest: SO notice copy for offers (SO20, mixed, failure)
ok 3631 - SO notice copy for offers (SO20, mixed, failure)
  ---
  duration_ms: 0.510866
  ...
# Subtest: destination override to an existing entry inserts as its child
ok 3632 - destination override to an existing entry inserts as its child
  ---
  duration_ms: 2.415955
  ...
# Subtest: destination override with a stale preimage skips loudly
ok 3633 - destination override with a stale preimage skips loudly
  ---
  duration_ms: 0.97918
  ...
# Subtest: destination override with a closed entry skips loudly
ok 3634 - destination override with a closed entry skips loudly
  ---
  duration_ms: 0.927351
  ...
# Subtest: destination override with a new name creates one placeholder after the running entry
ok 3635 - destination override with a new name creates one placeholder after the running entry
  ---
  duration_ms: 0.958962
  ...
# Subtest: destination override with a new name racing an open entry joins it
ok 3636 - destination override with a new name racing an open entry joins it
  ---
  duration_ms: 0.770331
  ...
# Subtest: reopen takes back the untouched successor link and restores status
ok 3637 - reopen takes back the untouched successor link and restores status
  ---
  duration_ms: 26.950665
  ...
# Subtest: an edited successor bullet survives while its status still restores
ok 3638 - an edited successor bullet survives while its status still restores
  ---
  duration_ms: 4.098538
  ...
# Subtest: an edited successor status line survives while its link is taken back
ok 3639 - an edited successor status line survives while its link is taken back
  ---
  duration_ms: 5.376607
  ...
# Subtest: reopen on a different day leaves successor links alone
ok 3640 - reopen on a different day leaves successor links alone
  ---
  duration_ms: 3.115218
  ...
# Subtest: reopening a task closed without a pass shows no take-back
ok 3641 - reopening a task closed without a pass shows no take-back
  ---
  duration_ms: 1.69156
  ...
# Subtest: Alt+] on a planned prerequisite links its successor
ok 3642 - Alt+] on a planned prerequisite links its successor
  ---
  duration_ms: 12.379841
  ...
# Subtest: take-back deletes a pre-existing entry it empties
ok 3643 - take-back deletes a pre-existing entry it empties
  ---
  duration_ms: 3.823864
  ...
# Subtest: take-back deletes a stub-replaced entry through the vault
ok 3644 - take-back deletes a stub-replaced entry through the vault
  ---
  duration_ms: 0.501317
  ...
# Subtest: take-back keeps entries that are closed or keep another child
ok 3645 - take-back keeps entries that are closed or keep another child
  ---
  duration_ms: 0.512389
  ...
# Subtest: closing-entry relocation finds a deferred-only placeholder
ok 3646 - closing-entry relocation finds a deferred-only placeholder
  ---
  duration_ms: 0.588715
  ...
# Subtest: Alt+[ into Cancelled recovers its dependents without linking
ok 3647 - Alt+[ into Cancelled recovers its dependents without linking
  ---
  duration_ms: 3.966976
  ...
# Subtest: take-back keeps an entry whose prose survives across a blank line (both paths)
ok 3648 - take-back keeps an entry whose prose survives across a blank line (both paths)
  ---
  duration_ms: 0.733521
  ...
# Subtest: take-back deletes a whole block with continuation/fence leftovers (LF/CRLF, final newline)
ok 3649 - take-back deletes a whole block with continuation/fence leftovers (LF/CRLF, final newline)
  ---
  duration_ms: 1.150117
  ...
# Subtest: link close links the unblocked successor into the slot and shows the nav card
ok 3650 - link close links the unblocked successor into the slot and shows the nav card
  ---
  duration_ms: 22.777267
  ...
# Subtest: close with no [id::] performs zero vault reads and shows nothing
ok 3651 - close with no [id::] performs zero vault reads and shows nothing
  ---
  duration_ms: 1.291486
  ...
# Subtest: Warm finalize reads no unrelated note bodies on the real close path
ok 3652 - Warm finalize reads no unrelated note bodies on the real close path
  ---
  duration_ms: 3.576129
  ...
# Subtest: cold fallback still recovers and links without a Tasks cache
ok 3653 - cold fallback still recovers and links without a Tasks cache
  ---
  duration_ms: 4.884859
  ...
# Subtest: recovered-only close reports unblocked without linking (SO4 Esc)
ok 3654 - recovered-only close reports unblocked without linking (SO4 Esc)
  ---
  duration_ms: 1.966897
  ...
# Subtest: walk landing composes a single toast and shows no card
ok 3655 - walk landing composes a single toast and shows no card
  ---
  duration_ms: 8.841324
  ...
# Subtest: nav absent falls back to a plain Notice with no link (SO missing picker)
ok 3656 - nav absent falls back to a plain Notice with no link (SO missing picker)
  ---
  duration_ms: 2.763858
  ...
# Subtest: stale cache heals via re-plan from fresh text (SO30)
ok 3657 - stale cache heals via re-plan from fresh text (SO30)
  ---
  duration_ms: 2.303248
  ...
# Subtest: Pomodoro-line close appends the successor to the created continuation
ok 3658 - Pomodoro-line close appends the successor to the created continuation
  ---
  duration_ms: 6.04835
  ...
# Subtest: Pomodoro-line close keeps the closing anchor after the picker re-plan
ok 3659 - Pomodoro-line close keeps the closing anchor after the picker re-plan
  ---
  duration_ms: 4.163822
  ...
# Subtest: completeTaskAtCursor returns the notice and shows nothing itself
ok 3660 - completeTaskAtCursor returns the notice and shows nothing itself
  ---
  duration_ms: 2.880031
  ...
# Subtest: successor apply recovers project residents without ledger v12
ok 3661 - successor apply recovers project residents without ledger v12
  ---
  duration_ms: 14.056133
  ...
# Subtest: SB vectors pin the successor mint pipeline
ok 3662 - SB vectors pin the successor mint pipeline
  ---
  duration_ms: 2.567584
  ...
# Subtest: successor suggester ports the Rust candidate and suffix rules
ok 3663 - successor suggester ports the Rust candidate and suffix rules
  ---
  duration_ms: 0.666012
  ...
# Subtest: successor link form names unique basenames short and the day file always
ok 3664 - successor link form names unique basenames short and the day file always
  ---
  duration_ms: 0.419321
  ...
# Subtest: tasksFromDocuments normalizes vault lines to pool shape
ok 3665 - tasksFromDocuments normalizes vault lines to pool shape
  ---
  duration_ms: 1.453035
  ...
# Subtest: normalizeTasksCacheTask ports every known Tasks shape
ok 3666 - normalizeTasksCacheTask ports every known Tasks shape
  ---
  duration_ms: 0.514883
  ...
# Subtest: buildDependentsIndex keeps first task IDs and groups dependents
ok 3667 - buildDependentsIndex keeps first task IDs and groups dependents
  ---
  duration_ms: 0.208749
  ...
# Subtest: findLiveLinks counts plain, embedded, and deferred links under open entries only
ok 3668 - findLiveLinks counts plain, embedded, and deferred links under open entries only
  ---
  duration_ms: 2.596288
  ...
# Subtest: computeSuccessorAnchors implements closing, slot, inherit, and none
ok 3669 - computeSuccessorAnchors implements closing, slot, inherit, and none
  ---
  duration_ms: 1.019307
  ...
# Subtest: SL1 links the successor right after the predecessor bullet
ok 3670 - SL1 links the successor right after the predecessor bullet
  ---
  duration_ms: 5.71826
  ...
# Subtest: SL3 still-blocked rows count the open prerequisites left
ok 3671 - SL3 still-blocked rows count the open prerequisites left
  ---
  duration_ms: 0.917663
  ...
# Subtest: SL4 future-scheduled dependents stay Blocked with the date row
ok 3672 - SL4 future-scheduled dependents stay Blocked with the date row
  ---
  duration_ms: 0.621697
  ...
# Subtest: SL5 already-planned dependents recover without a duplicate link
ok 3673 - SL5 already-planned dependents recover without a duplicate link
  ---
  duration_ms: 0.971585
  ...
# Subtest: SL6 struck and closed-entry links do not count as planned
ok 3674 - SL6 struck and closed-entry links do not count as planned
  ---
  duration_ms: 1.453155
  ...
# Subtest: SL7 closing anchors create the continuation placeholder
ok 3675 - SL7 closing anchors create the continuation placeholder
  ---
  duration_ms: 1.023515
  ...
# Subtest: SL8 closing anchors append after carried lines in the continuation
ok 3676 - SL8 closing anchors append after carried lines in the continuation
  ---
  duration_ms: 0.826558
  ...
# Subtest: SL9 unplanned predecessors offer at the implicit destination (SO14)
ok 3677 - SL9 unplanned predecessors offer at the implicit destination (SO14)
  ---
  duration_ms: 1.252382
  ...
# Subtest: SL10 missing block IDs mint through the SB rule
ok 3678 - SL10 missing block IDs mint through the SB rule
  ---
  duration_ms: 0.540552
  ...
# Subtest: SL11 project and hidden tasks recover but never link
ok 3679 - SL11 project and hidden tasks recover but never link
  ---
  duration_ms: 9.012182
  ...
# Subtest: PDC1 leaves a dependency-ready resident Blocked while its project still waits
ok 3680 - PDC1 leaves a dependency-ready resident Blocked while its project still waits
  ---
  duration_ms: 1.966146
  ...
# Subtest: PDC2 residents are offered under the project group (SO1)
ok 3681 - PDC2 residents are offered under the project group (SO1)
  ---
  duration_ms: 1.438878
  ...
# Subtest: PDC3 keeps a project resident Blocked when its own prerequisite remains open
ok 3682 - PDC3 keeps a project resident Blocked when its own prerequisite remains open
  ---
  duration_ms: 0.906591
  ...
# Subtest: PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
ok 3683 - PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile
  ---
  duration_ms: 2.273421
  ...
# Subtest: SL12 one gesture closing two prerequisites links once with both causes
ok 3684 - SL12 one gesture closing two prerequisites links once with both causes
  ---
  duration_ms: 0.476049
  ...
# Subtest: SL13 chains do not recurse: the dependent's own dependents wait
ok 3685 - SL13 chains do not recurse: the dependent's own dependents wait
  ---
  duration_ms: 0.31411
  ...
# Subtest: SL14 ambiguous basenames link long
ok 3686 - SL14 ambiguous basenames link long
  ---
  duration_ms: 0.31406
  ...
# Subtest: SL15 stale open dependents link and become Next
ok 3687 - SL15 stale open dependents link and become Next
  ---
  duration_ms: 0.324479
  ...
# Subtest: SL16 gates on [id::]: no identity means no lookup and empty rows
ok 3688 - SL16 gates on [id::]: no identity means no lookup and empty rows
  ---
  duration_ms: 0.222535
  ...
# Subtest: SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
ok 3689 - SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired)
  ---
  duration_ms: 1.208598
  ...
# Subtest: SL18 the kill switch recovers without linking or minting
ok 3690 - SL18 the kill switch recovers without linking or minting
  ---
  duration_ms: 0.341161
  ...
# Subtest: SL19 re-applied closes write nothing and report nothing
ok 3691 - SL19 re-applied closes write nothing and report nothing
  ---
  duration_ms: 0.241982
  ...
# Subtest: SL23 subtasks anchor at their root's link
ok 3692 - SL23 subtasks anchor at their root's link
  ---
  duration_ms: 0.396657
  ...
# Subtest: SL24 later same-name entries take the closing successors
ok 3693 - SL24 later same-name entries take the closing successors
  ---
  duration_ms: 0.486629
  ...
# Subtest: SL25 already-Next planned dependents produce no row
ok 3694 - SL25 already-Next planned dependents produce no row
  ---
  duration_ms: 0.563506
  ...
# Subtest: SL26 inbox successors carry the inbox flag
ok 3695 - SL26 inbox successors carry the inbox flag
  ---
  duration_ms: 0.312417
  ...
# Subtest: SL27 dropped links are never re-linked and recover to Ready
ok 3696 - SL27 dropped links are never re-linked and recover to Ready
  ---
  duration_ms: 0.40816
  ...
# Subtest: SL28 day-file successors name the note, never the bare link
ok 3697 - SL28 day-file successors name the note, never the bare link
  ---
  duration_ms: 0.302608
  ...
# Subtest: slot insertions land after the anchor subtree with its indent
ok 3698 - slot insertions land after the anchor subtree with its indent
  ---
  duration_ms: 0.311696
  ...
# Subtest: closing insertions replace a lone stub child
ok 3699 - closing insertions replace a lone stub child
  ---
  duration_ms: 0.521165
  ...
# Subtest: insertions skip placements with no valid target
ok 3700 - insertions skip placements with no valid target
  ---
  duration_ms: 0.155948
  ...
# Subtest: successorNoticeText implements the §12.6 table
ok 3701 - successorNoticeText implements the §12.6 table
  ---
  duration_ms: 0.522297
  ...
# Subtest: parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
ok 3702 - parseSuccessorLinkUnblocked reads block and flow styles, defaulting true
  ---
  duration_ms: 0.37167
  ...
# Subtest: loadLinkUnblocked stat-caches the config read
ok 3703 - loadLinkUnblocked stat-caches the config read
  ---
  duration_ms: 0.966856
  ...
# Subtest: loadLinkUnblocked treats missing or unreadable config as true
ok 3704 - loadLinkUnblocked treats missing or unreadable config as true
  ---
  duration_ms: 0.543638
  ...
# Subtest: successorPlanConfigPath honors XDG_CONFIG_HOME
ok 3705 - successorPlanConfigPath honors XDG_CONFIG_HOME
  ---
  duration_ms: 0.188831
  ...
# Subtest: todayDailyPath mirrors the ledger daily path
ok 3706 - todayDailyPath mirrors the ledger daily path
  ---
  duration_ms: 0.524762
  ...
# Subtest: normalizeClosedTaskIdentities keeps the anchor root off the match gate
ok 3707 - normalizeClosedTaskIdentities keeps the anchor root off the match gate
  ---
  duration_ms: 0.20394
  ...
# Subtest: ID-less planned roots anchor ID-bearing children without minting IDs
ok 3708 - ID-less planned roots anchor ID-bearing children without minting IDs
  ---
  duration_ms: 0.703163
  ...
# Subtest: successor anchors never guess across roots
ok 3709 - successor anchors never guess across roots
  ---
  duration_ms: 0.411095
  ...
# Subtest: a child with its own live link keeps its own slot
ok 3710 - a child with its own live link keeps its own slot
  ---
  duration_ms: 0.504603
  ...
# Subtest: getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
ok 3711 - getSuccessorIsInbox prefers the versioned nav API with safe fallbacks
  ---
  duration_ms: 0.558276
  ...
# Subtest: countSuccessorBasenames walks the vault set, not the task set
ok 3712 - countSuccessorBasenames walks the vault set, not the task set
  ---
  duration_ms: 0.456041
  ...
# Subtest: the pass threads a richer isInbox into unblocked rows
ok 3713 - the pass threads a richer isInbox into unblocked rows
  ---
  duration_ms: 0.697592
  ...
# Subtest: getTaskLinkLaneApi returns the lane only when version and both functions exist
ok 3714 - getTaskLinkLaneApi returns the lane only when version and both functions exist
  ---
  duration_ms: 1.111192
  ...
# Subtest: isTaskLinkLaneLine passes content, line, and path and never throws
ok 3715 - isTaskLinkLaneLine passes content, line, and path and never throws
  ---
  duration_ms: 1.166447
  ...
# Subtest: single Alt+] on a Task Link delegates with exactly { editor, view }
ok 3716 - single Alt+] on a Task Link delegates with exactly { editor, view }
  ---
  duration_ms: 0.532407
  ...
# Subtest: Alt+[ and Alt+] delegate identically; direction is ignored
ok 3717 - Alt+[ and Alt+] delegate identically; direction is ignored
  ---
  duration_ms: 0.325992
  ...
# Subtest: embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
ok 3718 - embedded Pomodoro link routes to the lane toggle, not the full-ring cycle
  ---
  duration_ms: 0.371479
  ...
# Subtest: entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
ok 3719 - entry, task, Depends-On, and non-Pomodoro lines keep today's behavior
  ---
  duration_ms: 3.025938
  ...
# Subtest: counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
ok 3720 - counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat
  ---
  duration_ms: 0.693164
  ...
# Subtest: counted dispatch without an explicit repeat leaves the key alone
ok 3721 - counted dispatch without an explicit repeat leaves the key alone
  ---
  duration_ms: 0.218848
  ...
# Subtest: counted range starting elsewhere skips Task Link lines
ok 3722 - counted range starting elsewhere skips Task Link lines
  ---
  duration_ms: 1.907082
  ...
# Subtest: legacy fallback with no api keeps today's behavior
ok 3723 - legacy fallback with no api keeps today's behavior
  ---
  duration_ms: 0.857598
  ...
# Subtest: plain Task Link in an open Pomodoro closes the task root-only and strikes the link
ok 3724 - plain Task Link in an open Pomodoro closes the task root-only and strikes the link
  ---
  duration_ms: 14.099334
  ...
# Subtest: marked plain Task Link drops its marker when struck under Pomodoro ancestry
ok 3725 - marked plain Task Link drops its marker when struck under Pomodoro ancestry
  ---
  duration_ms: 1.516276
  ...
# Subtest: plain Pomodoro Task Link closes root-only while embedded closes recursively
ok 3726 - plain Pomodoro Task Link closes root-only while embedded closes recursively
  ---
  duration_ms: 2.200001
  ...
# Subtest: embedded Pomodoro Task Link still closes recursively and retires to struck form
ok 3727 - embedded Pomodoro Task Link still closes recursively and retires to struck form
  ---
  duration_ms: 2.637016
  ...
# Subtest: Ctrl+Enter toggles a struck plain Pomodoro link back to open
ok 3728 - Ctrl+Enter toggles a struck plain Pomodoro link back to open
  ---
  duration_ms: 1.78559
  ...
# Subtest: same-file plain Task Link closes and strikes the correct line
ok 3729 - same-file plain Task Link closes and strikes the correct line
  ---
  duration_ms: 1.190403
  ...
# Subtest: cursor selects which of several Task Links closes and strikes
ok 3730 - cursor selects which of several Task Links closes and strikes
  ---
  duration_ms: 1.354848
  ...
# Subtest: plain links to Blocked or non-task blocks still complete the Pomodoro
ok 3731 - plain links to Blocked or non-task blocks still complete the Pomodoro
  ---
  duration_ms: 3.672123
  ...
# Subtest: strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
ok 3732 - strike and unstrike helpers are idempotent, alias-preserving, and marker-aware
  ---
  duration_ms: 0.532297
  ...
# Subtest: completeTaskAtCursor closes each open symbol through the Tasks command
ok 3733 - completeTaskAtCursor closes each open symbol through the Tasks command
  ---
  duration_ms: 1.67566
  ...
# Subtest: completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
ok 3734 - completeTaskAtCursor insert-above reports lineDelta 1 and never stamps
  ---
  duration_ms: 0.360509
  ...
# Subtest: completeTaskAtCursor refuses closed, cancelled, and non-task lines
ok 3735 - completeTaskAtCursor refuses closed, cancelled, and non-task lines
  ---
  duration_ms: 0.394182
  ...
# Subtest: completeTaskAtCursor refuses a missing Tasks command with no write
ok 3736 - completeTaskAtCursor refuses a missing Tasks command with no write
  ---
  duration_ms: 0.172339
  ...
# Subtest: Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
ok 3737 - Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it
  ---
  duration_ms: 0.516246
  ...
# Subtest: completeTaskAtCursor reports not-closed when Tasks does not write [x]
ok 3738 - completeTaskAtCursor reports not-closed when Tasks does not write [x]
  ---
  duration_ms: 0.191886
  ...
# Subtest: recovery api is frozen at version 2 and recovers without striking references
ok 3739 - recovery api is frozen at version 2 and recovers without striking references
  ---
  duration_ms: 2.572212
  ...
# Subtest: recovery api never throws and reports failures
ok 3740 - recovery api never throws and reports failures
  ---
  duration_ms: 0.219129
  ...
# Subtest: future-scheduled dependents stay Blocked on the planner, api, and close paths
ok 3741 - future-scheduled dependents stay Blocked on the planner, api, and close paths
  ---
  duration_ms: 15.950881
  ...
# Subtest: Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
ok 3742 - Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open
  ---
  duration_ms: 3.700298
  ...
# Subtest: every printable non-space ASCII key resolves to a surround pair
ok 3743 - every printable non-space ASCII key resolves to a surround pair
  ---
  duration_ms: 3.961525
  ...
# Subtest: visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
ok 3744 - visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically
  ---
  duration_ms: 0.614503
  ...
# Subtest: non-visible, combining, multi-character, and multi-code-unit values are rejected
ok 3745 - non-visible, combining, multi-character, and multi-code-unit values are rejected
  ---
  duration_ms: 0.241421
  ...
# Subtest: ys adds broad symmetric delimiters through pending keydown
ok 3746 - ys adds broad symmetric delimiters through pending keydown
  ---
  duration_ms: 1.218937
  ...
# Subtest: rejected keydown input never edits or leaks into a pending ys
ok 3747 - rejected keydown input never edits or leaks into a pending ys
  ---
  duration_ms: 0.375497
  ...
# Subtest: Escape cancels ys, cs, and ds pending state without editing
ok 3748 - Escape cancels ys, cs, and ds pending state without editing
  ---
  duration_ms: 0.262973
  ...
# Subtest: cs accepts broad target and replacement characters independently
ok 3749 - cs accepts broad target and replacement characters independently
  ---
  duration_ms: 2.213447
  ...
# Subtest: cs preserves structural alias and padding rules
ok 3750 - cs preserves structural alias and padding rules
  ---
  duration_ms: 0.726137
  ...
# Subtest: cs replaces repeated symmetric runs exactly once on each side
ok 3751 - cs replaces repeated symmetric runs exactly once on each side
  ---
  duration_ms: 0.549559
  ...
# Subtest: ds removes representative broad symmetric delimiters
ok 3752 - ds removes representative broad symmetric delimiters
  ---
  duration_ms: 0.783136
  ...
# Subtest: ds preserves structural alias and padding rules
ok 3753 - ds preserves structural alias and padding rules
  ---
  duration_ms: 0.336543
  ...
# Subtest: ds removes one pair from repeated runs, including the reported block link
ok 3754 - ds removes one pair from repeated runs, including the reported block link
  ---
  duration_ms: 1.13643
  ...
# Subtest: consecutive ds commands peel a triple symmetric surround
ok 3755 - consecutive ds commands peel a triple symmetric surround
  ---
  duration_ms: 0.230781
  ...
# Subtest: symmetric discovery uses deterministic sequential same-line run pairs
ok 3756 - symmetric discovery uses deterministic sequential same-line run pairs
  ---
  duration_ms: 0.149135
  ...
# Subtest: symmetric discovery includes every character in repeated boundaries
ok 3757 - symmetric discovery includes every character in repeated boundaries
  ---
  duration_ms: 0.322796
  ...
# Subtest: unpaired and unequal symmetric runs are safe no-ops
ok 3758 - unpaired and unequal symmetric runs are safe no-ops
  ---
  duration_ms: 0.220441
  ...
# Subtest: ordinary normal-mode keys remain untouched outside pending state
ok 3759 - ordinary normal-mode keys remain untouched outside pending state
  ---
  duration_ms: 0.194962
  ...
# Subtest: dot while a surround is pending is a literal delimiter, not repeat
ok 3760 - dot while a surround is pending is a literal delimiter, not repeat
  ---
  duration_ms: 0.155066
  ...
# Subtest: dot-repeat records and replays broad-character ys
ok 3761 - dot-repeat records and replays broad-character ys
  ---
  duration_ms: 0.315573
  ...
# Subtest: dot-repeat records and replays broad-character cs
ok 3762 - dot-repeat records and replays broad-character cs
  ---
  duration_ms: 0.220701
  ...
# Subtest: dot-repeat records and replays broad-character ds
ok 3763 - dot-repeat records and replays broad-character ds
  ---
  duration_ms: 0.189222
  ...
# Subtest: dot-repeat replays cs against repeated symmetric runs
ok 3764 - dot-repeat replays cs against repeated symmetric runs
  ---
  duration_ms: 0.203278
  ...
# Subtest: dot-repeat replays ds against repeated symmetric runs
ok 3765 - dot-repeat replays ds against repeated symmetric runs
  ---
  duration_ms: 0.213258
  ...
# Subtest: consecutive dot-repeats peel a triple symmetric surround
ok 3766 - consecutive dot-repeats peel a triple symmetric surround
  ---
  duration_ms: 0.235991
  ...
1..3766
# tests 3783
# suites 0
# pass 3782
# fail 1
# cancelled 0
# skipped 0
# todo 0
# duration_ms 7361.97706

=== EXIT bob-plugins test: 1 ===

=== bob-plugins validate ===

> bob-plugins@0.1.0 validate
> node scripts/build-plugins.mjs --check && npm run docs:inventory:check && node scripts/validate-manifests.mjs

  checked   block-id-prompt
  checked   bob-articles
  checked   bob-command-mode
  checked   bob-ledger-tools
  checked   bob-navigation-hotkeys
  checked   task-status-cycler

> bob-plugins@0.1.0 docs:inventory:check
> node scripts/docs-inventory.mjs --check

Plugin documentation inventory is up to date.
  ok    block-id-prompt
  ok    bob-articles
  ok    bob-command-mode
  ok    bob-ledger-tools
  ok    bob-navigation-hotkeys
  ok    bob-project-tasks
  ok    bob-vim-surround
  ok    task-status-cycler

8/8 plugin(s) valid

=== EXIT bob-plugins validate: 0 ===

=== bob-plugins docs:check ===

> bob-plugins@0.1.0 docs:check
> bash scripts/docs-check.sh

HEAD is now at c048955 feat(day-strip): document bars switch and update glossary
docs-check: using bob-cli /home/bryan/.cache/bob-plugins-docs/bob-cli with BOB_DOCS_BOB_PLUGINS_DIR=/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins

✅  DOCS CHECK
────────────────────────────────────────────────
uv run --project tools/docs bob-docs check
docs-check: assemble and validate source context

docs-check: lint
src/native/highlights_ref/source_store.rs:194: environment: undocumented production environment name BOB_TEST_FIXTURE_PDF; document it in docs/reference/configuration.md or add a reasoned exact exception
bob-docs lint: 1 error(s)
docs-check: FAILED (lint, exit 1)
error: recipe `docs-check` failed on line 208 with exit code 1

=== EXIT bob-plugins docs:check: 1 ===

FAILED GATES: just check:1,just docs-check:1,bob-plugins test:1,bob-plugins docs:check:1
failed  exit=1  duration=53234ms

