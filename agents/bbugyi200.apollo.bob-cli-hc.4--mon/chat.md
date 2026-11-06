# Chat History - ace-run (bob-cli-hc.4--mon)

- **TIMESTAMP:** 2026-11-05 11:57:15 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-hc.4--mon

## Prompt

sase monitor start --command 'npm test && bob plugins sync' --reason 'Run the full bob-plugins test suite and deploy the verified plugins'

## Response

sase tool run 5d8e560e7133909397bfdc739d0127ac

> bob-plugins@0.1.0 test
> node scripts/build-plugins.mjs --check && npm run docs:inventory:check && node --test scripts/test-navigation-leaf-switch-guard.cjs scripts/test-project-tasks-snapshot.cjs scripts/test-bob-articles.cjs scripts/test-command-mode-resolver-env.cjs scripts/test-command-mode-catalog.cjs scripts/test-command-mode-runner.cjs scripts/test-command-mode-outcomes-api.cjs scripts/test-command-mode-pager.cjs scripts/test-command-mode-args-vim.cjs scripts/test-command-mode-sheet.cjs scripts/test-command-mode-sheet-keys.cjs scripts/test-command-mode-sheet-sequence.cjs scripts/test-command-mode-sheet-sequence-dom.cjs scripts/test-command-mode-status-chip.cjs scripts/test-command-mode-sequence-engine.cjs scripts/test-command-mode-sequence-feedback.cjs scripts/test-navigation-hotkeys-section-nav.cjs scripts/test-navigation-hotkeys-rename.cjs scripts/test-navigation-hotkeys-ref-pdf.cjs scripts/test-navigation-hotkeys-templater-trigger.cjs scripts/test-navigation-hotkeys-schedule-recovery.cjs scripts/test-navigation-hotkeys-schedule-properties.cjs scripts/test-navigation-hotkeys-schedule-writes.cjs scripts/test-navigation-hotkeys-runtime-schedule.cjs scripts/test-navigation-hotkeys-dependencies.cjs scripts/test-navigation-blocks-guards.cjs scripts/test-navigation-blocks-writers.cjs scripts/test-navigation-blocks-edit.cjs scripts/test-navigation-blocks-stage-view.cjs scripts/test-navigation-hotkeys-dependency-mirror.cjs scripts/test-navigation-hotkeys-task-move-plan.cjs scripts/test-navigation-hotkeys-priority-notice.cjs scripts/test-navigation-successor-picker.cjs scripts/test-navigation-image-zoom-viewer.cjs scripts/test-navigation-image-zoom-origin.cjs scripts/test-navigation-image-zoom-path.cjs scripts/test-navigation-hotkeys-unblocked-notice.cjs scripts/test-navigation-project-blocking.cjs scripts/test-navigation-project-dependency-stage.cjs scripts/test-navigation-project-subprojects.cjs scripts/test-navigation-project-subtree-gestures.cjs scripts/test-navigation-hotkeys-priority-picker.cjs scripts/test-navigation-hotkeys-picker-lifecycle.cjs scripts/test-navigation-hotkeys-ref-picker-text.cjs scripts/test-navigation-hotkeys-pomodoro-move-pickers.cjs scripts/test-navigation-inbox-route.cjs scripts/test-navigation-inbox-route-card.cjs scripts/test-navigation-hotkeys-task-move.cjs scripts/test-navigation-open-notes-uri.cjs scripts/test-navigation-parent-change.cjs scripts/test-navigation-hotkeys-dash-open.cjs scripts/test-navigation-goto-task-uri.cjs scripts/test-navigation-hotkeys-open-task-jump.cjs scripts/test-navigation-hotkeys-vim-counts.cjs scripts/test-navigation-hotkeys-tab-pin.cjs scripts/test-navigation-hotkeys-schedule-log.cjs scripts/test-navigation-hotkeys-schedule-review.cjs scripts/test-navigation-hotkeys-deferred-pomodoro.cjs scripts/test-navigation-hotkeys-pomodoro-parse.cjs scripts/test-navigation-hotkeys-pomodoro-bullet-move.cjs scripts/test-navigation-hotkeys-pomodoro-split-rename.cjs scripts/test-navigation-hotkeys-pomodoro-split.cjs scripts/test-navigation-hotkeys-pomodoro-themes-manager.cjs scripts/test-navigation-hotkeys-pomodoro-reorder.cjs scripts/test-navigation-hotkeys-runtime-prune.cjs scripts/test-navigation-hotkeys-project-from-task.cjs scripts/test-navigation-hotkeys-project-reversal.cjs scripts/test-navigation-hotkeys-link-picker.cjs scripts/test-navigation-hotkeys-lane-toggle.cjs scripts/test-navigation-hotkeys-task-link-lane.cjs scripts/test-navigation-hotkeys-cancel-log.cjs scripts/test-navigation-hotkeys-cancel-task.cjs scripts/test-navigation-hotkeys-forward-promotion.cjs scripts/test-navigation-hotkeys-schedule-work-log.cjs scripts/test-navigation-hotkeys-work-log-stamp-closeout.cjs scripts/test-navigation-hotkeys-task-move-history.cjs scripts/test-navigation-jump-history.cjs scripts/test-navigation-dependencies.cjs scripts/test-navigation-editor-line-diff.cjs scripts/test-navigation-quick-roll.cjs scripts/test-navigation-quick-roll-preview.cjs scripts/test-navigation-roll-decay.cjs scripts/test-navigation-decay-planner.cjs scripts/test-navigation-task-card-model.cjs scripts/test-navigation-task-card-view.cjs scripts/test-navigation-task-card-theme-edit.cjs scripts/test-navigation-task-card-schedule.cjs scripts/test-navigation-task-card-review.cjs scripts/test-navigation-decision-card.cjs scripts/test-navigation-decision-card-handlers.cjs scripts/test-navigation-decision-card-keep.cjs scripts/test-navigation-refresh-modal.cjs scripts/test-navigation-freshness.cjs scripts/test-navigation-review-groups.cjs scripts/test-navigation-stamps.cjs scripts/test-navigation-keep-counting.cjs scripts/test-navigation-rotten-keep.cjs scripts/test-navigation-rotten-log.cjs scripts/test-navigation-checklist.cjs scripts/test-navigation-review-advance.cjs scripts/test-navigation-review-advance-gestures.cjs scripts/test-navigation-checklist-ctrl-enter.cjs scripts/test-ledger-tools-navigation.cjs scripts/test-ledger-tools-plan-budget.cjs scripts/test-ledger-tools-plan-budget-off-clock.cjs scripts/test-ledger-tools-plan-today-roots.cjs scripts/test-ledger-tools-ready-badge.cjs scripts/test-ledger-tools-note-ready.cjs scripts/test-ledger-tools-note-ready-views.cjs scripts/test-ledger-tools-dashboard-parity.cjs scripts/test-ledger-tools-work-badge-tone.cjs scripts/test-ledger-tools-dashboard-collections.cjs scripts/test-ledger-tools-today.cjs scripts/test-ledger-tools-period-notes.cjs scripts/test-ledger-tools-gcal-events.cjs scripts/test-ledger-tools-event-link-times.cjs scripts/test-ledger-tools-meet-event-run.cjs scripts/test-ledger-tools-pomodoro-clock.cjs scripts/test-ledger-tools-freshness-placement.cjs scripts/test-ledger-tools-freshness-states.cjs scripts/test-ledger-tools-freshness-namespace.cjs scripts/test-ledger-tools-freshness-review-model.cjs scripts/test-ledger-tools-freshness-queue.cjs scripts/test-ledger-tools-freshness-tracking.cjs scripts/test-ledger-tools-freshness-footer.cjs scripts/test-ledger-tools-keep-inbox.cjs scripts/test-ledger-tools-freshness-recurring.cjs scripts/test-ledger-tools-freshness-mark.cjs scripts/test-ledger-tools-freshness-mark-surfaces.cjs scripts/test-ledger-tools-priority-marks.cjs scripts/test-ledger-tools-block-marks.cjs scripts/test-ledger-tools-block-marks-contrast.cjs scripts/test-ledger-tools-block-marks-editor.cjs scripts/test-ledger-tools-block-marks-reading.cjs scripts/test-ledger-tools-task-tag-marks.cjs scripts/test-ledger-tools-task-link-marks.cjs scripts/test-ledger-tools-task-link-marks-live.cjs scripts/test-ledger-tools-task-link-marks-reading.cjs scripts/test-ledger-tools-task-type-identity.cjs scripts/test-ledger-tools-today-marks.cjs scripts/test-ledger-tools-today-marks-reading.cjs scripts/test-ledger-tools-unblocked-glyph.cjs scripts/test-ledger-tools-frees-marks.cjs scripts/test-ledger-tools-off-clock-link-chips.cjs scripts/test-ledger-tools-progress-marks.cjs scripts/test-ledger-tools-date-marks.cjs scripts/test-ledger-tools-recurrence-marks.cjs scripts/test-ledger-tools-date-marks-tasks.cjs scripts/test-ledger-tools-freshness-keeps.cjs scripts/test-ledger-tools-freshness-unblocked.cjs scripts/test-ledger-tools-freshness-decision-card.cjs scripts/test-ledger-tools-dependency-chips.cjs scripts/test-ledger-tools-blocks-chips.cjs scripts/test-ledger-tools-command-mode-refresh.cjs scripts/test-ledger-tools-snippets.cjs scripts/test-ledger-tools-vim-mappings.cjs scripts/test-task-status-cycler-dependencies.cjs scripts/test-task-status-cycler-blocks-guards.cjs scripts/test-task-status-cycler-complete-vectors.cjs scripts/test-task-status-cycler-ctrl-enter.cjs scripts/test-task-status-cycler-event-task-close.cjs scripts/test-task-status-cycler-reference-lifecycle.cjs scripts/test-task-status-cycler-pomodoro-completion.cjs scripts/test-task-status-cycler-pomodoro-clock.cjs scripts/test-task-status-cycler-pomodoro-work-log.cjs scripts/test-task-status-cycler-pomodoro-reopen.cjs scripts/test-task-status-cycler-blocked-schedule.cjs scripts/test-task-status-cycler-demotion-picker.cjs scripts/test-task-status-cycler-event-ledger-guard.cjs scripts/test-task-status-cycler-promotion.cjs scripts/test-task-status-cycler-counted-toggle.cjs scripts/test-task-status-cycler-successors.cjs scripts/test-task-status-cycler-successor-wiring.cjs scripts/test-task-status-cycler-successor-polish.cjs scripts/test-task-status-cycler-keep-moving.cjs scripts/test-task-status-cycler-relation-successors.cjs scripts/test-task-status-cycler-parked-successors.cjs scripts/test-task-status-cycler-successor-offers.cjs scripts/test-task-status-cycler-successor-theme-write.cjs scripts/test-task-status-cycler-project-pull-in.cjs scripts/test-task-status-cycler-task-links-api.cjs scripts/test-task-status-cycler-task-link-lane.cjs scripts/test-task-status-cycler-freshness.cjs scripts/test-block-id-prompt-dependencies.cjs scripts/test-block-id-prompt-blocks-guards.cjs scripts/test-block-id-prompt-ref-picker-text.cjs scripts/test-block-id-prompt-markers.cjs scripts/test-block-id-prompt-pomodoro-context.cjs scripts/test-block-id-prompt-target-update.cjs scripts/test-block-id-prompt-pomodoro-insertion.cjs scripts/test-block-id-prompt-pomodoro-targets.cjs scripts/test-block-id-prompt-pomodoro-picker-view.cjs scripts/test-block-id-prompt-pomodoro-picker-runtime.cjs scripts/test-block-id-prompt-work-log.cjs scripts/test-block-id-prompt-pomodoro-link-runtime.cjs scripts/test-block-id-prompt-pomodoro-theme-write.cjs scripts/test-block-id-prompt-pomodoro-link-picker-api.cjs scripts/test-block-id-prompt-pomodoro-unlink-runtime.cjs scripts/test-block-id-prompt-parked-successors.cjs scripts/test-block-id-prompt-task-link-deletion.cjs scripts/test-block-id-prompt-task-wikilink-model.cjs scripts/test-block-id-prompt-task-wikilink-token.cjs scripts/test-block-id-prompt-task-wikilink-index.cjs scripts/test-block-id-prompt-task-wikilink-index-performance.cjs scripts/test-block-id-prompt-task-wikilink-picker-view.cjs scripts/test-block-id-prompt-task-wikilink-picker-runtime.cjs scripts/test-block-id-prompt-task-wikilink-naming.cjs scripts/test-block-id-prompt-task-wikilink-pomodoro.cjs scripts/test-block-id-prompt-plan-budget-and-freshness.cjs scripts/test-prompt-block-id-naming.cjs scripts/test-block-id-prompt-prefill.cjs scripts/test-vim-surround.cjs scripts/test-navigation-dependencies-stage-ranker-and-pool.cjs scripts/test-navigation-dependencies-stage-entry-and-view.cjs scripts/test-navigation-dependencies-stage-writes.cjs scripts/test-navigation-dependencies-stage-mirror-and-badge.cjs scripts/test-navigation-dependencies-stage-stale-guards.cjs scripts/test-navigation-dependencies-stage-performance.cjs scripts/test-navigation-prompt-block-id-stage.cjs scripts/test-navigation-dependencies-writer.cjs scripts/test-navigation-dependency-link-consumption.cjs scripts/test-plugin-build.cjs scripts/test-ledger-tools-stats-journal.cjs scripts/test-ledger-tools-stats-clocks.cjs scripts/test-ledger-tools-stats-data.cjs scripts/test-ledger-tools-stats-block.cjs scripts/test-ledger-tools-stats-charts.cjs scripts/test-ledger-tools-stats-clock-charts.cjs scripts/test-navigation-review-journal.cjs scripts/test-ledger-tools-stats-panels.cjs scripts/test-ledger-tools-stats-lanes.cjs scripts/test-ledger-tools-reading-board-data.cjs scripts/test-ledger-tools-reading-board-models.cjs scripts/test-ledger-tools-reading-board-block.cjs scripts/test-ledger-tools-pomodoro-home-chips.cjs scripts/test-ledger-tools-pomodoro-themes.cjs scripts/test-ledger-tools-task-theme-marks.cjs scripts/test-ledger-tools-task-theme-rendered.cjs scripts/test-navigation-image-zoom-target.cjs scripts/test-navigation-image-zoom-command.cjs scripts/test-docs-inventory.mjs scripts/test-docs-check.mjs scripts/test-navigation-relation-lines.cjs scripts/test-navigation-relation-mentions.cjs scripts/test-navigation-relation-writer.cjs scripts/test-navigation-task-cancel-vectors.cjs scripts/test-navigation-task-split-vectors.cjs scripts/test-navigation-task-split-gesture.cjs scripts/test-navigation-relation-cancel-writer.cjs scripts/test-navigation-relation-complete-writer.cjs scripts/test-navigation-relation-complete-vectors.cjs scripts/test-navigation-relation-links-stage.cjs scripts/test-navigation-relation-merge.cjs scripts/test-navigation-relation-successor-vectors.cjs scripts/test-navigation-relation-stage-render.cjs scripts/test-relation-index-linked-from-stage.cjs scripts/test-ledger-tools-relations.cjs scripts/test-ledger-tools-task-merge.cjs scripts/test-ledger-tools-relation-index.cjs scripts/test-ledger-tools-attachments-api.cjs scripts/test-ledger-tools-relation-mentions.cjs scripts/test-ledger-tools-relation-chips.cjs scripts/test-task-status-cycler-relations.cjs scripts/test-block-id-prompt-relations.cjs scripts/test-ledger-tools-day-strip.cjs scripts/test-ledger-tools-day-strip-themes.cjs scripts/test-ledger-tools-day-strip-plan-host.cjs scripts/test-ledger-tools-period-strip.cjs scripts/test-ledger-tools-period-parts.cjs scripts/test-ledger-tools-fakenode-inspect.cjs scripts/test-ledger-tools-day-strip-lanes.cjs scripts/test-ledger-tools-day-strip-hosts.cjs scripts/test-obsidian-startup-smoke.cjs scripts/test-obsidian-task-wikilink-e2e.cjs scripts/test-obsidian-task-link-marks-e2e.cjs scripts/test-obsidian-block-marks-e2e.cjs scripts/test-obsidian-frees-marks-e2e.cjs scripts/test-obsidian-off-clock-link-chips-e2e.cjs scripts/test-obsidian-event-link-times-e2e.cjs scripts/test-obsidian-decay-ladder-e2e.cjs scripts/test-obsidian-quick-roll-e2e.cjs scripts/test-task-link-marks-motion.cjs scripts/test-ledger-tools-lane-walk.cjs scripts/test-navigation-lane-walk.cjs scripts/test-ledger-tools-root-marks.cjs scripts/test-navigation-bracket-repeat.cjs scripts/test-navigation-period-links.cjs scripts/test-navigation-bracket-mode-indicator.cjs scripts/test-navigation-lane-inbox-route.cjs scripts/test-navigation-review-due-row.cjs

  checked   block-id-prompt
  checked   bob-articles
  checked   bob-command-mode
  checked   bob-ledger-tools
  checked   bob-navigation-hotkeys
  checked   task-status-cycler

> bob-plugins@0.1.0 docs:inventory:check
> node scripts/docs-inventory.mjs --check

Plugin documentation inventory is up to date.
✔ bip BK1–BK12 accept and empty (8.996233ms)
✔ bip BK13–BK15 malformed split mirrors the Depends-On twin (1.067485ms)
✔ bip MC5 Ctrl+Shift+Enter refuses BLOCKS with the generated notice (0.289507ms)
✔ bip MC1/MC2 Pomodoro scanners skip managed lines (8.795064ms)
✔ explicit task IDs exclusively own dependency lookup (6.843963ms)
✔ legacy tasks without an id field still fall back to their block ID (0.61065ms)
✔ blocked-link consumption raises open prerequisites and leaves the dependent blocked (2.355827ms)
✔ project-blocked member consumption promotes the project's open prerequisite (1.69514ms)
✔ project-blocked resident consumption promotes the project's open prerequisite (0.871526ms)
✔ a tagged inherited ^prj target is refused with its parent named (0.805414ms)
✔ project schedule blocks residents without promotion, while a task's own schedule stays pull-forward eligible (3.075518ms)
✔ project date refusal applies only when the date is the sole project reason (0.985945ms)
✔ a project-blocked tag is token-bounded and ignored on lookalike tags (2.054438ms)
✔ task picker includes Blocked tasks and excludes closed, hidden, and untagged lines (0.952543ms)
✔ task blocked state unifies status and dependency reasons (0.69548ms)
✔ task picker partition sinks blocked tasks while preserving group order (13.904239ms)
✔ blocked chip labels show useful unmet dependency counts (0.41034ms)
✔ blocked tooltips explain dependency and status-only reasons (0.651351ms)
✔ task status classes cover every open task status (0.243091ms)
✔ Blocked tasks remain unmet dependency targets (0.480594ms)
✔ blocked task count covers both reasons without double-counting (0.418888ms)
✔ single caret relocation preserves embedding and removes aliases (17.31632ms)
✔ single caret relocation resets aliased block links (0.509331ms)
✔ single caret relocation strips heading and block subpaths (7.703668ms)
✔ task picker normalizes every supported wiki block-link form (1.502628ms)
✔ three or more carets never trigger the task picker (0.461173ms)
✔ rapid aliased task picker completion preserves the alias (21.914394ms)
✔ task picker recognition is independent of Markdown source context (5.168332ms)
✔ task picker recognition respects cursor proximity and fenced code (0.696881ms)
✔ SA33 settled Unlink task prompt offers parked successors with the removed slot (47.821058ms)
✔ SA33 Esc on Unlink task offers nothing (4.001179ms)
✔ non-Pending unlink stays silent even with a live cycler (1.398711ms)
✔ older cycler api v3 is silence (3.672869ms)
✔ In Progress unlink with no removed links does not offer (0.793662ms)
✔ Task Link Unlink of a Pending target offers parked successors (16.150035ms)
✔ plan budget suffix: link Notice appends the meter computed on post-write daily content (17.681327ms)
✔ plan budget suffix: link Notice omits the meter when the ledger-tools API is missing (2.260579ms)
✔ plan budget suffix: unlink Notice marks an over-cap plan with 🔴 (5.068347ms)
✔ plan budget suffix: Next task without a block ID prompts for one and omits the meter (0.992929ms)
✔ plan budget suffix: Task Link Notice appends the meter from post-write daily content (18.340617ms)
✔ plan budget suffix: Task Link Notice omits the meter when no daily note takes part (7.740943ms)
✔ planTargetTaskUpdate stamps the rewritten line last via injected stamper (7.071213ms)
✔ planTargetTaskUpdate without a stamper never stamps (identity default) (0.428869ms)
✔ planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper (0.462447ms)
✔ planTargetTaskUpdate stamps a Next task that gains a block ID (0.813769ms)
✔ planTargetTaskUpdate tolerates a throwing stamper (10.961055ms)
✔ Depends-On line recogniser covers the contract DP vectors (1.016346ms)
✔ dedicated-link helpers reject Depends-On lines (4.962142ms)
✔ Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything (4.024908ms)
✔ malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token (0.313001ms)
✔ Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal (0.657638ms)
✔ Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything (0.389789ms)
✔ readPlanBudgetMeter ignores stale theme meters and follows links only (0.299654ms)
✔ readPlanBudgetMeter marks an over-link plan red (6.430373ms)
✔ block-id-prompt freshness accessors degrade without ledger-tools (0.776013ms)
✔ block-id-prompt refuses Pomodoro ledger lines before calling a stamper (0.659741ms)
✔ list item body bounds trim whitespace and reject empty bullets (8.542534ms)
✔ Pomodoro activation eligibility requires a sole-content sub-bullet (12.02662ms)
✔ Pomodoro activation eligibility requires an open owner, rejecting completed and canceled history (0.860751ms)
✔ Pomodoro source context distinguishes ledger ancestry and open state (5.13534ms)
✔ the open-Pomodoro task-link gate recognizes both ^^ and (( sources (8.565343ms)
✔ future cleanup touches only later open Pomodoros and counts duplicates (7.589836ms)
✔ cleanup resolves aliases, embeds, same-note links, and alternate paths (5.435585ms)
✔ dedicated bullet subtree cleanup preserves CRLF line endings (0.79806ms)
✔ existing-ID task completion prunes future links in the source editor (20.030366ms)
✔ new-ID same-file completion plans cleanup after the task edit (16.548592ms)
✔ findDirectPomodoroLinkTask includes a #hide project task, unlike the task-picker's own listing (13.79811ms)
✔ findDirectPomodoroLinkTask rejects closed/canceled tasks and non-task lines (0.448467ms)
✔ findDirectPomodoroLinkTask accepts every open status and carries the existing block ID (0.516074ms)
✔ todayDailyPath formats the default YYYY/YYYYMMDD layout under the configured folder (7.353523ms)
✔ todayDailyPath honors a custom Daily Notes format and an empty folder (0.657ms)
✔ formatDailyDate resolves bracketed literal text alongside date tokens (0.372243ms)
✔ getDailyNotesOptions reads the daily-notes core plugin's configured options (11.955285ms)
✔ computeFencedLineFlags marks opening and closing fence lines and everything between (0.952106ms)
✔ selectPomodoroInsertionTarget prefers the single open timed entry over a placeholder (11.666783ms)
✔ selectPomodoroInsertionTarget falls back to the first open placeholder when nothing is timed (0.728417ms)
✔ selectPomodoroInsertionTarget rejects more than one open timed entry (7.311295ms)
✔ selectPomodoroInsertionTarget ignores fenced and nested entries and picks the remaining eligible one (0.516055ms)
✔ findPomodoroChildIndentation reuses existing child indentation before falling back to a tab (0.493795ms)
✔ planPomodoroLinkInsertion inserts under the selected entry using an existing child's indentation (6.584751ms)
✔ planPomodoroLinkInsertion is idempotent and prunes a matching link from a later open Pomodoro (17.051461ms)
✔ planPomodoroLinkInsertion reports no-section, no-eligible-entry, and multiple-open-timed without any edits (0.504874ms)
✔ planPomodoroLinkInsertion inserts before trailing separators, preserving LF endings (7.339859ms)
✔ planPomodoroLinkInsertion inserts before trailing separators, preserving CRLF endings (1.325839ms)
✔ planPomodoroLinkInsertion covers empty destinations, indentation, and nested subtrees (2.817484ms)
✔ planPomodoroLinkInsertion inserts before the separator preceding later content (0.775327ms)
✔ planPomodoroLinkInsertion repeats as a no-op and keeps two distinct links adjacent (0.58047ms)
✔ planPomodoroLinkInsertion before separators composes with future cleanup, preserving history (0.994024ms)
✔ existing-ID Pomodoro link runtime keeps terminal-newline separators adjacent (cross-note) (19.771355ms)
✔ same-note Pomodoro link runtime composes the task update with adjacent insertion (12.528423ms)
✔ new-ID Pomodoro link runtime keeps terminal-newline separators adjacent (1.587587ms)
✔ planFuturePomodoroLinkCleanup accepts a direct ownerLine/section context, bypassing findPomodoroSourceContext (0.479216ms)
✔ all-open cleanup removes current and future links while preserving history and unresolved links (7.685935ms)
✔ all-open cleanup removes decorated dedicated bullets whole and deletes the entries it empties (6.043847ms)
✔ all-open cleanup deletes an emptied entry under CRLF without disturbing line endings (0.531161ms)
✔ all-open cleanup treats missing section, no open entries, and no matches as no-op successes (0.454606ms)
✔ composeInsertionWithLinkCleanup preserves an insertion at a deletion boundary (EOF and neighbour) (0.4882ms)
✔ pomodoro link picker choices normalize to existing/new or null (10.00101ms)
✔ pomodoroLinkPicker api never rejects and validates choices (1.025666ms)
✔ destination pick refuses without a prompt when busy, noteless, unreadable, or sectionless (4.68329ms)
✔ destination pick with a section releases its guards when the modal cannot open (32.190793ms)
✔ public pick accepts one-based full-note task context and suggests once (11.21266ms)
✔ public pick without task context stays generic; missing themes degrades safely (5.132063ms)
✔ plugin lifecycle installs the api and drops it on unload (1.537181ms)
✔ task-aware choices retain a valid themeIntent; absent intent keeps the legacy shape (0.583878ms)
✔ malformed themeIntent is dropped so it can never enable a write (0.844487ms)
✔ taskLineTextAt reads one-based lines and degrades to empty (4.290303ms)
✔ public pick tolerates an out-of-range task line and releases its guards (6.952283ms)
✔ Ctrl+Shift+Enter is registered as the link-task-to-pomodoro command (5.542456ms)
✔ resolvePomodoroLinkTaskFromEditor requires a single cursor (0.803638ms)
✔ resolvePomodoroLinkTaskFromEditor rejects a cursor inside a fenced code block (1.03783ms)
✔ resolvePomodoroLinkTaskFromEditor rejects a non-task line and a closed task (1.073536ms)
✔ resolvePomodoroLinkTaskFromEditor accepts a #hide project task directly under the cursor (1.806223ms)
✔ blocked-link consumption reports dependency reasons before the project date (5.996391ms)
✔ Pomodoro link checks do not read other notes for a non-Blocked task (0.783794ms)
✔ resolvePomodoroLinkTaskFromEditor rejects a block ID duplicated elsewhere in the same note (1.0797ms)
✔ task-mode toggle decides on link presence: linked In Progress prompts, unlinked links and stays In Progress (16.362899ms)
✔ task-mode toggle: linked Next unlinks and stays Next; unlinked Next links and stays Next (5.726843ms)
✔ task-mode toggle: linked only under a completed Pomodoro links again (1.67021ms)
✔ task-mode toggle: a task without a block ID is never linked and prompts for one (0.96867ms)
✔ existing-ID Pomodoro link runtime: cross-note guarded write, canonical link, forced Next, and success notice (3.645142ms)
✔ forceNext consumes a dependency-blocked target, promotes its prerequisite, and creates no link (7.717369ms)
✔ new-ID Pomodoro link runtime: cross-note guarded write, appended ID stays final, forced Next for a Ready task (1.346449ms)
✔ submitPomodoroTaskLinkBlockId rejects a newly duplicated ID discovered at submit time (0.312945ms)
✔ submitPomodoroTaskLinkBlockId aborts when the task text changed while the modal was open (0.263843ms)
✔ same-note Pomodoro link runtime: task and ledger edits merge into one transaction (3.139816ms)
✔ linking an already-linked Ready task raises it to Next without duplicating the link (0.903454ms)
✔ Next task without a block ID preflights the picker before prompting (1.124876ms)
✔ Pomodoro link stops before any mutation when today's daily note is missing (0.365969ms)
✔ Pomodoro link stops before any task mutation when the daily note has no Pomodoros section (0.716246ms)
✔ Pomodoro link stops before any task mutation when the daily note has multiple open timed Pomodoros (0.516539ms)
✔ Pomodoro link aborts without any write when the task line changed since it was selected (0.259085ms)
✔ Pomodoro link reports the exact partial result when the daily note write fails after the task write succeeds (5.378666ms)
✔ canceling the Pomodoro block-ID modal leaves the note untouched (0.497536ms)
✔ review-walk: existing-ID link hands its Linked notice to continue with no separate notice (2.035019ms)
✔ review-walk: prompted-ID link continues after submit (1.611358ms)
✔ review-walk: prompt cancel settles with null (0.292521ms)
✔ review-walk: BUSY swallows the key with no write (0.433003ms)
✔ review-walk: failed link keeps its notice and settles with null (0.507289ms)
✔ review-walk: partial link keeps its notice and never continues with an outcome (1.828452ms)
✔ inbox-route: getInboxRouteApi detects the v1 namespace and rejects partial shapes (0.527727ms)
✔ inbox-route: non-inbox notes and task-link mode never prompt (1.445713ms)
✔ inbox-route: cancel writes nothing and settles once (0.760693ms)
✔ inbox-route: stay matches today (1.539635ms)
✔ inbox-route: move links, then moves, with one composed toast and a route continue (1.874188ms)
✔ inbox-route: a new block ID goes through the route, then the picker, then the ID prompt (1.823314ms)
✔ inbox-route: a submitted ID that already exists in the destination keeps the prompt open (0.941752ms)
✔ inbox-route: a move failure gives the partial notice plus a link-today continue (1.07198ms)
✔ review-walk: no nav or nav v2 keeps today's notices (1.428974ms)
✔ inbox-route: source drift during route prompt refuses without writes (0.613404ms)
✔ inbox-route: route cancel up front writes nothing, opens no ID prompt, and settles null once (0.506931ms)
✔ inbox-route: link no-op with move never commits (0.434075ms)
✔ picker opens only on the link direction, never on unlink (72.274954ms)
✔ picker never opens in task-link mode (8.48266ms)
✔ Depends-On refusals never open the picker (3.809838ms)
✔ preflight refusals open nothing (3.030686ms)
✔ direct picker captures one task suggestion with a one-based line and live note text (12.90436ms)
✔ missing task-theme APIs leave the direct picker on its existing default (3.172712ms)
✔ picking a non-default entry links there (3.84654ms)
✔ cancel writes nothing with no Notice and settles the walk null (1.896708ms)
✔ a no-ID task gets picker, then the block-ID prompt with the target carried (2.974095ms)
✔ inbox order is route, then picker, then write (2.945909ms)
✔ a route cancel never opens the picker and writes nothing (2.068846ms)
✔ a routed move suggests from the destination with a one-line virtual note (1.308736ms)
✔ a routed stay suggests from the inbox path (7.15018ms)
✔ a routed move carries the destination chip and a stay carries none (2.437001ms)
✔ a review-walk landing continues with link-today and the new text (3.372502ms)
✔ an all-closed ledger creates a new entry after the last completed block (8.469157ms)
✔ several running entries allow an explicit pick (3.195719ms)
✔ a target that changed before commit refuses with no writes (1.032027ms)
✔ a target that closed before commit refuses with no writes (1.891882ms)
✔ the task note being the daily note uses one editor transaction (2.613322ms)
✔ promptOpen blocks re-entry while the picker is open (58.908677ms)
✔ direct picker request carries the task line text for the footer (1.529511ms)
✔ direct picker stays task-aware when the live note text is unavailable (0.572417ms)
✔ header shows title, subtitle, lane chip per status, and block-ID chip (35.637989ms)
✔ rows render in document order with the default selected (2.161293ms)
✔ recent theme rows follow today's rows and render component swatches (327.176945ms)
✔ exact recent themes suppress generic creation and preserve catalog spelling (16.568815ms)
✔ Ctrl+D hides a Recent suggestion as an undoable ghost and leaves Today unchanged (72.863344ms)
✔ new-name rows show near-duplicate and hidden-theme hints (14.190679ms)
✔ running row shows progress fraction and minutes-left meta (1.898296ms)
✔ unnamed entries render muted italic (0.803204ms)
✔ filtering ranks, highlights, and clearing restores the default (6.052684ms)
✔ create row meta and divider (8.930624ms)
✔ exact open names suppress the create row; prefix matches keep it (7.814317ms)
✔ create rows have no type budget badge (1.116171ms)
✔ invalid rows explain the grammar and are inert on Enter (13.211254ms)
✔ multiple running entries show the banner, no pills, and block creation (7.086503ms)
✔ navigation wraps and skips non-selectable rows (2.455029ms)
✔ empty state invites planning a Pomodoro (0.456514ms)
✔ footer hints and plan meter (2.163697ms)
✔ Enter chooses the selected row; click chooses that row (1.489856ms)
✔ Shift+Enter creates; an exact open name links there instead (2.000035ms)
✔ Ctrl+Shift+Enter commits exactly like Enter (0.722643ms)
✔ Escape and Ctrl+[ cancel with no choice; settle-once holds (1.941171ms)
✔ done-today themes stay in Recent while open Today themes stay excluded (1.73201ms)
✔ configured theme menu vectors scope Recent, preserve config order, and flag new names (6.053833ms)
✔ configured empty-query picker shows up to twelve configured themes (0.592744ms)
✔ link success notice names an unconfigured theme after creating its Pomodoro (0.781817ms)
✔ typing done shows only the Recent DONE row and keeps catalog spelling (6.880907ms)
✔ Today exclusions apply before query filtering; cancelled themes stay Recent (6.637667ms)
✔ suggested entry rows render the reason, dot, theme pill, and accessible label (4.568792ms)
✔ reading and note suggestions render their own reasons and footer phrases (8.674616ms)
✔ footer previews the default merge and the explicit retype with suggestion context (5.936276ms)
✔ footer hides without task context or theme APIs (1.291897ms)
✔ footer states a keep consequence when the destination already agrees (2.505078ms)
✔ footer previews PLAN, LATER, and Tab cycling on a composite (3.200645ms)
✔ footer refreshes on selection moves and hides on inert rows (7.757405ms)
✔ untouched refresh preserves a still-eligible suggested entry; arrivals adopt a first default (28.72757ms)
✔ refresh after typing preserves the user's position and initial key (9.324193ms)
✔ removed rows fall back deterministically without clearing interaction (8.658732ms)
✔ clearing a query keeps interaction but returning home is not deliberate (1.824467ms)
✔ suggestion never recomputes on refresh and survives API changes (4.218754ms)
✔ deferred fetch makes an unknown suggestion eligible and settles the untouched default (5.59313ms)
✔ onChange adopts a newly eligible existing match only before interaction (2.898909ms)
✔ refresh after arrows and after typing then clearing keeps the settled user key (2.829966ms)
✔ typed theme suggestion decorates the final Recent row without changing PT7 order (9.059001ms)
✔ Alt+Enter explicitly requests retype; plain commits keep the default merge (1.429015ms)
✔ Enter, click, and Ctrl+Shift+Enter share the deliberate rule (4.654783ms)
✔ Shift+Enter named commits are always deliberate (4.856123ms)
✔ cancellation writes nothing even when task-aware (11.815511ms)
✔ Ctrl+D on the suggested create row is consumed without writes (20.106722ms)
✔ canonicalizePomodoroLinkName collapses whitespace, uppercases, and validates (4.135822ms)
✔ canonicalizePomodoroLinkName rejects leading symbols, letterless names, and non-ASCII (0.883965ms)
✔ pomodoroLinkSelectorSlug mirrors capture slugs (0.486006ms)
✔ parsePomodoroEntryParts reads canonical and legacy entry lines (1.878302ms)
✔ collectPomodoroLinkEntries skips fenced, nested, completed, and cancelled lookalikes (3.201858ms)
✔ collectPomodoroLinkEntries detects running, next-up, default, and ambiguity (2.175326ms)
✔ collectPomodoroLinkEntries counts links but excludes struck references (1.110656ms)
✔ collectPomodoroLinkEntries falls back to range text and position titles (0.706918ms)
✔ pomodoroRunProgress reports fractions, overtime, and midnight wrap (0.580485ms)
✔ buildPomodoroLinkPickerRows ranks exact slugs before prefix hits (2.102127ms)
✔ buildPomodoroLinkPickerRows keeps the create row for prefix matches (2.347854ms)
✔ buildPomodoroLinkPickerRows marks completed-only names as again (0.563264ms)
✔ buildPomodoroLinkPickerRows shows invalid and blocked rows with no selection (1.920116ms)
✔ buildPomodoroLinkPickerRows matches times, positions, and block IDs (1.174998ms)
✔ resolvePomodoroLinkCreateIntent prefers exact opens and refuses blocked creates (5.662825ms)
✔ defaultPomodoroLinkChoice returns the default entry or null (0.967489ms)
✔ planExplicitPomodoroLinkInsertion links under a chosen existing entry (6.384772ms)
✔ planExplicitPomodoroLinkInsertion re-resolves a shifted line but refuses edits and closes (1.073341ms)
✔ planExplicitPomodoroLinkInsertion is idempotent and cleans other opens (7.957701ms)
✔ planExplicitPomodoroLinkInsertion lands the link in the chosen entry when it ties an emptied neighbour deletion (1.138638ms)
✔ planExplicitPomodoroLinkInsertion creates after the running entry (8.586811ms)
✔ planExplicitPomodoroLinkInsertion creates after completed, before first open, and at section top (1.326904ms)
✔ planExplicitPomodoroLinkInsertion links into a raced open name without duplicating (0.45183ms)
✔ planExplicitPomodoroLinkInsertion refuses crowded creates and bad targets (3.655272ms)
✔ planExplicitPomodoroLinkInsertion preserves CRLF and a missing final newline (0.777937ms)
✔ buildPomodoroLinkPickerRows suppresses creates for mixed-case exact names (0.369671ms)
✔ buildPomodoroLinkPickerRows keeps againOf for completed mixed-case names (0.350481ms)
✔ planExplicitPomodoroLinkInsertion matches mixed-case raced open names (0.371643ms)
✔ buildPomodoroLinkPickerRows bounds #N position matches (5.043531ms)
✔ planPomodoroLinkInsertion without a target keeps today's behavior and shape (0.931639ms)
✔ buildPomodoroLinkPickerRows keeps a done-only theme in Recent (3.223144ms)
✔ shared task-theme preselection vectors match the bob-cli model (80.603044ms)
✔ task-theme preselection normalizes exemptions without a type cap (0.535575ms)
✔ task-aware rows preselect an existing match when creation is blocked (0.946981ms)
✔ task-aware typed queries keep PT7 order and only annotate the matching row (3.940679ms)
✔ suggested creation uses catalog spelling and removes its duplicate Recent row (5.905252ms)
✔ theme suggestion identity ignores decorative hue and catalog flags (6.130455ms)
✔ theme suggestion identity treats a changed declaring note as a different suggestion (0.47892ms)
✔ current exempt keys distinguish valid empty configuration from unavailable caps (5.978713ms)
✔ planTargetTaskUpdate applies themeEdit after lane changes and before a new block ID (5.506323ms)
✔ planTargetTaskUpdate theme-only Next task never stamps freshness (0.78619ms)
✔ planTargetTaskUpdate stamps a lane rewrite after the theme field is in place (0.86963ms)
✔ planTargetTaskUpdate without themeEdit preserves an authored theme field (0.388309ms)
✔ planTargetTaskUpdate clears a theme field and keeps CRLF plus a trailing block ID (6.715113ms)
✔ a named destination retypes the task in the same cross-note write (34.917308ms)
✔ unavailable current caps still retype the task and retain lane, ID, and freshness edits (29.493905ms)
✔ real Ledger Tools planner writes with an empty exempt list and custom exemptions (3.536388ms)
✔ a Ready scheduled task sets Next, logs the date, and remembers the theme (12.889762ms)
✔ choosing the inherited destination clears an existing task theme (4.333228ms)
✔ a theme-only Next task with a new block ID still stamps because the ID rewrote the line (1.016638ms)
✔ duplicate and paren theme fields repair only on an eligible deliberate write (5.873261ms)
✔ a stale shown suggestion links and skips the theme edit (1.085585ms)
✔ decorative catalog metadata on a live suggestion does not skip the write (0.863023ms)
✔ Enter merges the current type into the destination name (4.083868ms)
✔ a container keeps the type on the default landing (0.977512ms)
✔ untouched default (not deliberate) links without storing a field (0.864121ms)
✔ absent theme APIs leave the picker write path usable without a field (4.170084ms)
✔ a blocked dependency consumption never writes a theme field (7.20019ms)
✔ same-note combined edit writes the theme and the link in one editor transaction (4.323475ms)
✔ a failed daily write after a saved theme reports the theme and the link failure (1.019402ms)
✔ catalog spelling wins over a canonical landing name (0.718224ms)
✔ a routed inbox task retypes from the destination suggestion (4.319437ms)
✔ the inbox and the destination inherit different types, and the user picks the destination's suggested Pomodoro (4.051046ms)
✔ a routed link that picks a different type writes the field (0.92871ms)
✔ malformed themeIntent never enables a write (0.562559ms)
✔ themeIntent survives normalizePomodoroLinkPickerChoice for a later consumer (0.439158ms)
✔ Tab pick chooses that type component of a composite destination (4.952388ms)
✔ unlink preserves an authored task theme (15.470481ms)
✔ direct unlink without a daily note keeps the Next lane and reports it (12.866687ms)
✔ In Progress unlink with blank summary keeps the lane without a Work Log or daily-note lookup when no block ID exists (1.281578ms)
✔ In Progress unlink with a summary keeps the lane and creates a Work Log (6.022449ms)
✔ In Progress unlink revalidates task text and block-ID uniqueness at confirmation (3.971229ms)
✔ Next task unlink removes current and future links and keeps the Next lane (16.971559ms)
✔ In Progress unlink removes cross-note Pomodoro links and logs work without changing the lane (2.044412ms)
✔ same-note Next unlink merges the Work Log and all-open cleanup in the active editor (5.080357ms)
✔ same-note In Progress unlink merges cleanup and Work Log in the active editor (5.194344ms)
✔ Next unlink stops before any write when daily cleanup write is stale (1.20689ms)
✔ Next unlink reports retryable partial failure when cleanup succeeds but the Work Log write is stale (5.174828ms)
✔ In Progress unlink reports retryable partial failure when cleanup succeeds but logging is stale (1.573804ms)
✔ review-walk: unlink settles with null and keeps its notice (8.228338ms)
✔ inbox-route: unlink cancel writes nothing (1.172074ms)
✔ inbox-route: unlink stay matches today and never commits (1.222145ms)
✔ inbox-route: unlink move unlinks, then moves, with one composed toast and a route continue (3.758799ms)
✔ inbox-route: In Progress unlink with a Work summary routes (5.512302ms)
✔ inbox-route: unlink move failure gives the partial notice and stays (2.515667ms)
✔ inbox-route: non-inbox unlink never prompts (4.095406ms)
✔ review-walk: Work-summary unlink path retains origin until submit (0.72621ms)
✔ inbox-route: unlink source drift during route prompt refuses without writes (0.576242ms)
✔ inbox-route: Work-summary route cancel returns sentinel and settles null once (4.106869ms)
✔ inbox-route: unlink no-op with move never commits (0.537004ms)
✔ same-note unlink maps a task below removed entries through Work-summary inserts (1.593333ms)
✔ the unlink preview shows the write-instant stamp and re-renders on the clock (4.45969ms)
✔ a prompt opened at 23:59 and committed at 00:01 stamps the commit instant (1.00155ms)
✔ direct-add seeds from the task headline, not non-task blocks (69.96708ms)
✔ link-task-complete seeds from the target, prefers open buffers (2.425135ms)
✔ link-task-complete reports stale and unreadable targets (3.490967ms)
✔ pomodoro link seeds after the choice from the cursor task (0.718162ms)
✔ marker rename suggests from the unique task, never hiding ambiguity (1.440187ms)
✔ modal seeds the value, selects once, and never overwrites typing (3.289444ms)
✔ modal disables Save while loading and survives close/reopen (7.168108ms)
✔ submit revalidates: occupied IDs and stale tasks fail editable (3.296017ms)
✔ cancelling writes no ID and explicit renames keep the current ID (1.430945ms)
✔ the task picker drops the paired #ref and prefixes the book (6.849422ms)
✔ near-miss spellings never pair and never prefix (0.819332ms)
✔ block-id-prompt LK1–LK19 recognises only relation line shapes (3.156501ms)
✔ block-id-prompt MC10 skips relations in Pomodoro cleanup and MC13 refuses both relation gestures (2.567327ms)
✔ block-id-prompt MC13 refuses Ctrl+Shift+Enter on either relation line (7.463445ms)
✔ calendar date parsing rejects malformed width and impossible dates (4.993283ms)
✔ future scheduled field detection respects the yesterday/today/tomorrow boundary (1.049854ms)
✔ scheduled field recognition covers bracket and paren forms in any position and on quoted/numbered lines (0.365661ms)
✔ planTargetTaskUpdate removes a future schedule and promotes Ready/Blocked to Next (2.046422ms)
✔ planTargetTaskUpdate unschedules a future task while preserving Next/In-Progress status (0.633088ms)
✔ planTargetTaskUpdate keeps the legacy unscheduled Ready promotion and Blocked non-promotion (1.977938ms)
✔ planTargetTaskUpdate leaves an already Next or In-Progress task alone when there is no future schedule (0.524221ms)
✔ planTargetTaskUpdate leaves today and past schedules untouched (0.817392ms)
✔ planTargetTaskUpdate never touches status or schedule when the source is not activation-eligible (0.625557ms)
✔ two or more recognized scheduled fields are ambiguous and never touch the Schedule Log, even when a marker exists (3.020437ms)
✔ a malformed single scheduled field is never treated as future (0.372761ms)
✔ an ambiguous scheduled field does not block the legacy Ready promotion (0.650902ms)
✔ planTargetTaskUpdate activation works on quoted and numbered task lines and preserves unrelated fields (0.369314ms)
✔ Schedule Log marker recognition covers canonical, emoji-less, and legacy forms, and ignores nested grandchildren (1.19216ms)
✔ Schedule Log entry indentation reuses an existing entry or falls back to marker indent plus a tab (0.419301ms)
✔ planTargetTaskUpdate prepends a newest-first Schedule Log entry when a marker already exists (0.578208ms)
✔ planTargetTaskUpdate creates the first entry using marker indent plus a tab when the marker has none yet (0.231614ms)
✔ planTargetTaskUpdate never creates a Schedule Log for a task that keeps none (0.180149ms)
✔ planTargetTaskUpdate preserves CRLF line endings, inheriting the marker's line ending for the new entry (0.245376ms)
✔ planTargetTaskUpdate preserves a missing trailing newline when the log lands at end of file (0.219445ms)
✔ planTargetTaskUpdate preserves a trailing newline when one was already present (0.29995ms)
✔ planTargetTaskUpdate never mutates the exact whitespace of a scheduled field it does not remove (0.243217ms)
✔ planTargetTaskUpdate keeps a new block ID as the final token after unschedule, status, and log changes (0.374307ms)
✔ planTargetTaskUpdate never duplicates an existing block ID on the existing-ID path (0.27271ms)
✔ existing-ID activation runtime: cross-note guarded write, canonical link, and success notice (8.102406ms)
✔ new-ID activation runtime: cross-note guarded write, appended ID stays final, and success notice (2.075328ms)
✔ activation runtime aborts without any write when the target preimage goes stale (0.970104ms)
✔ same-note activation shifts the Pomodoro source line when the Schedule Log entry lands before it (9.276313ms)
✔ same-note activation leaves the Pomodoro source line untouched when the Schedule Log entry lands after it (6.322419ms)
✔ a source marker edited after a successful existing-ID target write reports an accurate partial notice (1.059671ms)
✔ a source marker edited after a successful new-ID target write reports an accurate partial notice (1.071244ms)
✔ planTargetTaskUpdate forceNext raises Ready/Blocked to Next and never lowers Next or In Progress (0.313789ms)
✔ planTargetTaskUpdate without forceNext leaves an In Progress task and an unscheduled Blocked task alone (0.350366ms)
✔ planTargetTaskUpdate forceNext still removes a uniquely future schedule and logs it against an existing Schedule Log (0.310943ms)
✔ Pomodoro forceNext stamps the pulled-forward Ready task before its block ID (0.823311ms)
✔ planTargetTaskUpdate forceNext never creates a Schedule Log for a task that keeps none (0.201226ms)
✔ direct Task Links raise ^prj while never pulling its date forward (0.222511ms)
✔ task-link selection: one link is selectable from any column, several are chosen by cursor (6.463166ms)
✔ task-link selection ignores picker/rename markers, plain links, and Markdown-style links (0.899639ms)
✔ dedicated Task Link bullet detection covers checkbox, marker, embed, strike, and move-only forms (1.700811ms)
✔ inline Task Link deletion removes the token with its decoration and collapses whitespace (1.405964ms)
✔ dedicated Task Link bullet deletion removes the item with its subtree and stops at the Pomodoro (2.079285ms)
✔ mergeCoveringEdits keeps the covering edit and the earlier of identical edits (0.559891ms)
✔ dependency transclusion detection needs an embedded sole-content child of a #task line (0.966437ms)
✔ Task Link on a Next target: keeps Next, deletes the link subtree, cleans other open Pomodoro links (13.787185ms)
✔ Task Link on a Next target works from an embedded aliased link outside any Pomodoro (4.558669ms)
✔ same-note Task Link: one merged editor write, overlapping edits deduped, cursor restored (2.258128ms)
✔ same-note Task Link deletion clamps the restored cursor to the shortened note (3.266151ms)
✔ a cleanup subtree that covers a nested selected link wins and links are not double counted (6.010523ms)
✔ same-note Task Link in a closed entry deletes the closed entry it empties (5.780363ms)
✔ Task Link in another day's note deletes the emptied entry there and in today's note (2.734694ms)
✔ Task Link on an In Progress target prompts, then keeps the lane with a Work Log entry on submit (6.96168ms)
✔ Task Link on an In Progress target with a blank summary logs nothing (1.985956ms)
✔ canceling the In Progress Task Link prompt leaves everything untouched (0.766366ms)
✔ canceling the In Progress unlink prompt in task mode leaves everything untouched (1.206884ms)
✔ In Progress Task Link submit revalidates the link line and the target task (1.215837ms)
✔ Task Link on an Open target keeps it Ready, and on a Blocked target keeps it Blocked (1.608274ms)
✔ Task Link on a Done or Cancelled target is refused without edits (0.888953ms)
✔ Task Link with an unresolvable, missing, duplicated, or non-task target is refused without edits (1.7048ms)
✔ precedence: any #task line keeps the task-line behavior; other lines fall to task-link mode or the notice (4.55132ms)
✔ Task Link mode keeps the single-cursor and code-fence notices and reports ambiguity (0.882112ms)
✔ Task Link that is a sub-task dependency transclusion is refused without edits (0.396368ms)
✔ Task Link partial failure after the daily write is retryable (4.014378ms)
✔ Task Link stops before any write when the target note changes after planning (1.047843ms)
✔ Task Link with a missing daily note skips cleanup, and an unreadable daily note blocks (0.860632ms)
✔ Task Link subtree deletion removes a nested target task without any status write (0.625791ms)
✔ whole-entry deletion at EOF preserves final-newline state (LF/CRLF) (1.281297ms)
✔ selected-link deletion maps a cursor inside a removed entry to its former start (1.16026ms)
✔ cold build of 6,500 notes / 5,000 tasks fits 1.5 s in chunks of at most 16 ms (1245.34344ms)
✔ warm snapshot plus order takes at most 50 ms (1147.615419ms)
✔ one keystroke rank of 5,000 rows takes at most 12 ms (516.856232ms)
✔ no vault reads happen while filtering (596.269331ms)
✔ cold build growth stays near-linear over a 6x step (599.453386ms)
✔ cache prefilter skips taskless files without reading, reads cacheless files (19.179013ms)
✔ a throwing file cache falls back to reading (1.008094ms)
✔ non-note and excluded paths never enter the store (4.053433ms)
✔ unreadable files produce bounded warnings and a quiet footer note (5.572106ms)
✔ blockIdsFor exposes the note id set for the detail strip preview (0.810374ms)
✔ taskBearingDocuments reads fresh text on demand (1.259582ms)
✔ metadataCache changed re-parses from event data with no extra read (4.270661ms)
✔ vault rename re-keys rows and recomputes the basename index (7.587295ms)
✔ renaming onto an excluded path drops the note (0.521388ms)
✔ vault delete drops rows (5.039124ms)
✔ open-time mtime validation queues changed files for background re-parse (2.381644ms)
✔ a vanished file is removed when the reparse queue drains (0.750473ms)
✔ live overlays win over disk and never persist (0.669348ms)
✔ snapshot returns ordered rows, progress, and a live subscription (3.780915ms)
✔ filtering performs no vault reads (0.835667ms)
✔ refreshPaths applies post-write content and recomputes locators (0.672036ms)
✔ refreshPathsFromVault re-reads named paths (0.601576ms)
✔ collectEditorOverlays reads every open markdown editor (6.984513ms)
✔ attachLiveUpdates without a host is a safe no-op (0.277345ms)
✔ custom settings narrow the parsed pool (0.470294ms)
✔ task wikilink fixture mirrors bob-cli byte for byte (5.23651ms)
✔ every vector ranks the same rows bob serves (23.141918ms)
✔ frontmatter tasks never parse, unclosed fences stay open (4.022941ms)
✔ task grammar mirrors bob: dashes only, exact filter token (11.013696ms)
✔ trailing IDs need whitespace and clean bytes; every line counts (0.603681ms)
✔ hide and project-block tags are exact tokens (0.477325ms)
✔ search text drops filters, fields, and the block ID (0.768314ms)
✔ sections track headings and depth counts indentation (3.659638ms)
✔ note paths, locators, and archive targets (0.591156ms)
✔ match tiers, AND terms, and empty queries (7.088372ms)
✔ previous daily is the latest daily before the anchor (0.448088ms)
✔ guards mirror bob, minus the read-only check (0.446312ms)
✔ fused scorer matches the layered scorer across randomized rows and queries (144.801303ms)
✔ ID-less task identity relocates only to one exact line (2.937499ms)
✔ wikilink naming validates closed tasks and rejects duplicate target IDs (1.872981ms)
✔ wikilink naming adds an ID to a moved closed task and links the original token (3.299922ms)
✔ ^^ naming preserves a cross-note target and alias through the final link (5.532501ms)
✔ auto-open only on a written second paren, including auto-pair and closed shapes (163.216407ms)
✔ caret-only, undo, and programmatic edits never auto-open (1.225635ms)
✔ query seeds from the token and keys move, accept, escape, and backspace (32.218263ms)
✔ Backspace undoes closed ((q)) to () and unclosed ((q to ( (11.221938ms)
✔ identified accept splices one transaction, caret after ]], no notice (11.87528ms)
✔ stale target paths keep the picker open with a Notice (8.070479ms)
✔ command opens on a token, a selection, or the caret (5.800877ms)
✔ managed-line (( shows that line's guard notice and never opens (3.750275ms)
✔ command in an excluded context shows Task wikilinks can't go here (6.961248ms)
✔ ^^ marker still opens the per-note picker when (( is absent (1.398405ms)
✔ ID-less Enter opens naming mode with the picker state (37.284711ms)
✔ Page Down clamps at the final selectable row instead of wrapping (32.648745ms)
✔ naming cancel paths restore query, selection, row limit, and scroll (3.351795ms)
✔ a scan that exits early clears old written ranges before a later scan (0.663238ms)
✔ identified accept dispatches one isolated CodeMirror completion event (1.455218ms)
✔ guarded rows never open the naming prompt (3.281729ms)
✔ cheap Pomodoro guards disable non-selected duplicate rows (7.985758ms)
✔ stale Backspace closes with a notice and leaves the changed token alone (1.563362ms)
✔ onEscapeKey clears a non-empty filter first and closes on an empty one (2.55412ms)
✔ empty filter groups This note, In progress, Next, Other open, Hidden, Completed (87.608913ms)
✔ per-note headers expose sticky data, kind icons, and count pills (1.363843ms)
✔ row anatomy, locator parts, and action lines cover identified, id-less, and guarded (5.647285ms)
✔ title parts render code, wikilinks, markdown labels, and URL hosts (1.097642ms)
✔ counts, empty states, indexing, and footer hints (2.419345ms)
✔ windowing emits 100-row windows and renderAll exhausts (41.712329ms)
✔ narrow layout keeps basename plus id and drops the backspace hint (0.822942ms)
✔ filtered list is flat with a Completed history divider (0.909465ms)
✔ caret-task and unlinkable-path guards disable the row (0.86722ms)
✔ card DOM helpers are exported for Chromium previews (0.378615ms)
✔ Pomodoro (( picker limits the pool to open tasks and shows commit consequences (48.909626ms)
✔ ^^ under an open Pomodoro raises blocked prerequisites, leaves the task unlinked, and reverts the marker (15.081721ms)
✔ ^^ refuses a project-blocked task without consuming its prerequisites (2.292459ms)
✔ ^^ refuses a closed target under an open Pomodoro (1.609533ms)
✔ (( refuses a #prj_is_blocked resident without consuming prerequisites (3.599949ms)
✔ (( refuses a task inherited-blocked by its #prj_is_blocked project (2.607169ms)
✔ (( refuses a ^prj whose own future date is the sole remaining reason (1.929035ms)
✔ ^^ links and promotes an existing-ID task under an open Pomodoro (4.893911ms)
✔ ID-less ^^ names, links, and retains its target alias in Pomodoro mode (3.561969ms)
✔ an unrelated unreadable note does not block a Ready Pomodoro target (5.3633ms)
✔ a ^prj blocked only by its own prerequisite raises that prerequisite (1.973283ms)
✔ Pomodoro prerequisite raise pins every promoted task and selects the first (8.31602ms)
✔ the task wikilink Pomodoro preview omits type text when the themes API is absent (0.713194ms)
✔ Pomodoro commit rechecks the selected task before writing (0.651592ms)
✔ ID-less (( selection names the task and completes through the shared Pomodoro commit (3.402536ms)
✔ Pomodoro commit merges the task type into the Pomodoro, pulls a future schedule forward, and includes notices (3.197164ms)
✔ task-wikilink trigger vectors match bob's shared core (5.392321ms)
✔ task-wikilink context vectors allow prose and exclude note-only spans (9.311016ms)
✔ task-wikilink written-second-paren vectors gate auto-open on user input (0.742402ms)
✔ findTaskWikilinkToken rejects unusable caret positions (0.331892ms)
✔ taskWikilinkContextAt rejects unusable positions (0.3802ms)
✔ addTaskWikilinkChanges records insertions and maps earlier ranges forward (1.191472ms)
✔ addTaskWikilinkChanges accepts the wrapper and CodeMirror spellings (0.490386ms)
✔ mapTaskWikilinkRanges maps without recording (0.547393ms)
✔ mapTaskWikilinkRanges tolerates array ranges and empty sets (0.490048ms)
✔ work summary normalization trims, collapses whitespace, preserves Markdown, and flags Dataview fields (4.031049ms)
✔ formatWorkLogStamp matches the shared conformance vectors (0.696523ms)
✔ work log stamps use local wall-clock components (0.409622ms)
✔ planWorkLogInsertion stamps the injected clock when no stamp is given (3.1139ms)
✔ workSummaryPromptState previews the clock at render time (0.402904ms)
✔ planWorkLogInsertion creates tab-indented Work Log children for column-0 tasks without children (0.833183ms)
✔ planWorkLogInsertion inherits an existing space-indented child prefix (0.830717ms)
✔ planWorkLogInsertion inherits an existing tab-indented child prefix (0.557299ms)
✔ planWorkLogInsertion prepends newest-first entries into existing marker spellings (1.031694ms)
✔ planWorkLogInsertion ignores nested child-task markers and preserves CRLF (0.950494ms)
✔ planWorkLogInsertion treats blank summaries as no-op structural edits (0.347919ms)
✔ the Open-reset planner is removed: unlink plans only a Work Log insertion (0.259724ms)
✔ unlink Work Log plan keeps the In Progress checkbox and appends one entry (0.31339ms)
✔ article detection accepts scalar and list frontmatter values (2.513392ms)
✔ bob resolution prefers its setting, then known install paths, then PATH (2.074962ms)
✔ plan decoder accepts v1 and rejects a foreign schema version (1.358267ms)
✔ bob stdin spawn passes the article contract and vault environment (4.700097ms)
✔ bob plan stdout decodes UTF-8 split across chunks (1.552235ms)
✔ early bob exit on stdin reports EPIPE as a run failure (1.478184ms)
✔ line hunks become minimal cursor-preserving changes (1.468081ms)
✔ insert, multi-line replace, and deletion hunks reproduce the formatted note (4.14411ms)
✔ notice shows bob's text and at most two warning findings (0.605338ms)
✔ inbound changes apply only when their target line still matches the preimage (2.121715ms)
✔ undo guard blocks a reformat until a fresh input or delete event (1.575378ms)
✔ leave formatting observes the undo guard before saving or reading (0.675231ms)
✔ Convert shows bob's refusal on every invocation (0.759458ms)
✔ old bob's non-JSON article response gets one update notice per session (0.430367ms)
✔ format drops its response if the editor changed while bob was running (0.745116ms)
✔ decoration ranges mark written section numbers from the outline (1.784985ms)
✔ a new outline rerenders each open Reading view once for that generation (1.036884ms)
✔ section at a given line uses the innermost outline range (0.620545ms)
✔ stale-hint debounce and in-flight state machine (0.611339ms)
✔ reading-view wrapping puts the leading number token in span.bob-secno (1.449595ms)
✔ applied plans remap outline lines onto the formatted buffer (0.361406ms)
✔ article styles scope the reading look under .bob-article (1.152509ms)
✔ look settings default to serif typeface and stale-number hints (0.588332ms)
✔ typed argv tokenizer handles quotes, escapes, literal shell syntax, and errors (4.576757ms)
✔ typed argv resolves aliases to the longest catalog entry and refuses excluded paths (1.907981ms)
✔ the list pins typed metadata, disabled exclusions, and the explicit Vim fallback (24.469535ms)
✔ Vim-shaped input follows the agreed positive and negative rules (0.551286ms)
✔ vimrc parser finds recursive colon mappings and exmap names (1.179628ms)
✔ argument completion passes the entry path, fixed args, and current tokens to bob (13.4427ms)
✔ completion directives group candidates, preserve prefixes, and expand vault paths (23.325968ms)
✔ stale completion replies are discarded and Enter reports missing required positionals (23.494041ms)
✔ argument completion requests debounce edits by 60 ms (91.637363ms)
✔ Vim ex dispatch restores and targets the editor captured when the sheet opened (16.790356ms)
✔ double colon enters Vim stage and Escape returns to the list (20.909781ms)
✔ vimrc lint reads the configured file and shows only one session notice (4.544228ms)
✔ fingerprints compare path, mtime, and size (14.501902ms)
✔ validation accepts the fixture and rejects malformed catalogs (0.832313ms)
✔ refresh fetches and validates through the real protocol (280.064269ms)
✔ lookup resolves entries, aliases of entries, and excluded paths (0.807748ms)
✔ argv assembly puts preview args before fixed args (4.784826ms)
✔ cmRecordArgs strips a leading bob binary and leaves queued argv (1.052204ms)
✔ cmReplayRun is the inverse of cmAssembleArgv (6.199524ms)
✔ palette entries need policy run and all-optional positionals (0.530306ms)
✔ classification order: stop, spawn, timeout, signal (10.533683ms)
✔ lock phrase wins over exit codes and adapters (0.451034ms)
✔ exit-code hints beat the generic rule; unknown ids are ignored (0.290195ms)
✔ adapters adjust the result; failures stay honest (1.275551ms)
✔ gcal-sync summarizes added Event Tasks, context, and MEET links (2.728665ms)
✔ gcal-sync reports unchanged and waiting outcomes (0.503633ms)
✔ api.commandMode settles, never rejects, and fires the workspace event (522.618327ms)
✔ plugin onload registers run-* commands and exposes the frozen api (161.634031ms)
✔ plugin reports missing-bob when the binary is absent (6.940233ms)
✔ runner notifies with a plain summary after each finish (7.181131ms)
✔ catalog outcome adapters cover command-specific results and actions (7.410992ms)
✔ toast classes have distinct timing and newer failures replace older cards (7.150466ms)
✔ status chip waits 400 ms, tracks multiple runs, and marks overdue writers (9.058096ms)
✔ OS notifications only fire for long runs while Obsidian is unfocused (0.739779ms)
✔ rerun-last preserves arguments and preview mode; Apply carries the replay seed (1.068582ms)
✔ commandModeRerun retries an applied preview-first run and Apply carries the seed (1597.422178ms)
✔ ANSI parsing keeps SGR that splits across chunks (5.680415ms)
✔ linkify positives resolve and negatives stay plain (2.61347ms)
✔ JSON pretty-print mutes keys on a single document (1.295305ms)
✔ interleave replay preserves arrival order for copy (1.159937ms)
✔ stamped sequence runs add a step label to the pager header (3.805387ms)
✔ pager keys: scroll, wrap, search, copy, history, stop, close (1.289559ms)
✔ history stepping is newest-first (0.435903ms)
✔ search matches are exact and advance (0.507758ms)
✔ status pill covers running, outcomes, and queued-behind (3.119651ms)
✔ plugin pager opens from Output, show-last-output, history, copy, and stop (41.822002ms)
✔ writer stop needs confirmation; reads stop immediately (4.803857ms)
✔ watching a run skips the toast (6.90677ms)
✔ pretty JSON and ANSI land in the pager body (2.748868ms)
✔ resolver prefers the explicit setting and expands home (6.418738ms)
✔ resolver consults ledger-tools before the candidates (0.444989ms)
✔ resolver walks candidates, records every path tried, then PATH (0.591884ms)
✔ child env points at the vault, honors features, and drops completion vars (0.77985ms)
✔ inherited NO_COLOR wins; without the color feature NO_COLOR is set (0.925896ms)
✔ vault base requires a local folder (0.357055ms)
✔ ansi stripping, quoting, durations, and run ids (1.448372ms)
✔ completed read writes files, receipt, and an honest record (610.362212ms)
✔ child env carries vault, features, receipt, and tool paths (478.562559ms)
✔ literal args with spaces, quotes, and $() stay literal (283.085543ms)
✔ split multi-byte characters survive and big output stays intact (859.787588ms)
✔ in-memory text truncates past the cap while files keep everything (96.999671ms)
✔ a double run is one run: duplicates share the settlement (650.814833ms)
✔ writers serialize FIFO while reads run in parallel (1192.71768ms)
✔ a failed save refuses the writer (8.114155ms)
✔ read budgets kill; writer budgets mark overdue; stop stops (3093.42761ms)
✔ failures classify: non-zero, signals, lock, and missing bob (1617.250942ms)
✔ policy and entry guards refuse with reasons (656.129145ms)
✔ retention keeps the newest fifty and never an unfinished run (484.959926ms)
✔ adoption finalizes from receipts and reports unknown without one (12.663313ms)
✔ cmNewRecord copies a sanitized sequence stamp and omits the field otherwise (4.661959ms)
✔ step display, title, copy text, guards, continues, and focus run (4.338131ms)
✔ history groups by id, newest record per index wins, and states include interrupted (6.148171ms)
✔ cmRunSequence runs reads in order, stamps every record, and survives throwing hooks (1442.499896ms)
✔ a failing step 2 halts the sequence and skips later steps (658.083381ms)
✔ attention continues the sequence (1154.668588ms)
✔ an early saveAllMarkdown refusal halts with its reason (504.559656ms)
✔ a stale entry_id falls back to argv (398.733875ms)
✔ resume reuses the id and history folds into one group (1827.475531ms)
✔ cancelled() stops before the next step (398.845733ms)
✔ plugin suppresses per-step toasts and skips chip settle for an active sequence (850.378082ms)
✔ duplicate signatures are refused and rerun-last replays a stamped newest record (1917.028382ms)
✔ rerun-last command callback points at commandModeRerunLast (35.866945ms)
✔ summary model covers completed, attention, halted, and stopped sequences (18.291746ms)
✔ summary card renders accessible rows and routes the body to its focus run (2.792929ms)
✔ resume keeps the sequence id and skips completed steps; rerun gets a new id (10.893979ms)
✔ Output opens the focus run and Copy writes the sequence shell line (1.229417ms)
✔ a repeated sticky sequence card replaces the previous card by signature (4.857683ms)
✔ three Ctrl+N presses move three rows, keep focus, and wrap (53.299506ms)
✔ Caps Lock and layout variants navigate; Ctrl+Shift+N does not (20.673794ms)
✔ Ctrl+[ matches Escape in list, args, vim, confirm, and output (16.552799ms)
✔ standalone pager Ctrl+[ behaves like Escape (2.930257ms)
✔ focus and caret survive re-renders with scroll preserved on same query (10.830548ms)
✔ argument mode walks rendered order and Tab accepts the visible first row (6.027026ms)
✔ row mousedown is defaultPrevented and scope fallback routes body keys once (9.828582ms)
✔ Ctrl+M marks with Caps Lock and layout; Ctrl+Shift+M is ignored (29.473184ms)
✔ Ctrl+[ clears pending marks like Escape (9.35606ms)
✔ empty query walks every row with unique keys and survives a type-and-clear (414.749583ms)
﹣ production sheet render and clicks use real DOM APIs (54.461484ms) # Chromium is not installed; set CHROMIUM_PATH to run production DOM coverage.
✔ marking, toggling, and renumbering (45.502233ms)
✔ the badge and tray text (28.447188ms)
✔ query select-all after a mark (10.496093ms)
✔ each refusal reason (10.881956ms)
✔ Ctrl+M into argument mode, then marking from it (13.783768ms)
✔ argument mode Ctrl+M with incomplete args shows Needs (8.595963ms)
✔ Backspace pops the last step (34.482733ms)
✔ Esc first clears marks, second closes (22.673082ms)
✔ click and Ctrl+click toggles (28.888738ms)
✔ Shift+Enter with marks runs nothing (17.447288ms)
✔ one mark activates like Enter (441.37028ms)
✔ one confirm mark opens its card (15.881777ms)
✔ Enter with unguarded steps closes and runs (43.786767ms)
✔ Enter with guards shows the review card (58.575043ms)
✔ Ctrl+Enter skips the card (50.976794ms)
✔ argument-mode add and run (48.568064ms)
✔ the already-running hint (49.504677ms)
✔ RECENT grouping folds one sequence into one row (6.305138ms)
✔ RECENT dedupe, limit, interrupted glyph, and about lines (2.253473ms)
✔ RECENT Enter reruns all steps and Ctrl+M loads and unloads them (92.085458ms)
✔ clicking a descendant toggles while marks are pending (36.675135ms)
✔ no-mark argument Shift+Enter still previews (9.123168ms)
✔ marked argument Ctrl+Enter with a highlighted completion adds and runs now (56.735662ms)
✔ incomplete marked arguments leave marks and show the missing positional (34.737102ms)
✔ a RECENT sequence reduced to one report uses the normal activation chain (342.266698ms)
✔ a RECENT sequence reduced to one confirm opens its card (17.84109ms)
✔ a RECENT sequence reduced to one preview-first command previews (485.589218ms)
✔ rebuildRows passes live sequence ids so a running sequence shows ⟳ (11.133139ms)
✔ an active sequence refuses a duplicate rerun without closing the sheet (18.25521ms)
✔ an incomplete sequence with no active id stays interrupted after reload (0.528135ms)
✔ fuzzy ranking matches every token and prefers paths, prefixes, and keywords (9.418134ms)
✔ bare capture has no row but named capture rows keep theirs (0.998401ms)
✔ unavailable rows stay visible with reasons (1.171402ms)
✔ frecency weights recent runs and the last-ten window (2.043877ms)
✔ context rows fill For this note and From clipboard (1.68463ms)
✔ note kinds follow frontmatter type with the article rule (0.570667ms)
✔ empty query groups RECENT, note, clipboard, then catalog sections (1.262481ms)
✔ list keys map to intents and plain text stays unhandled (0.796628ms)
✔ help argv targets the selected row or bare bob (4.006704ms)
✔ median duration hides fast rows under the two-second floor (0.938622ms)
✔ the open command focuses an already-open sheet (27.745473ms)
✔ Enter on a report row streams it in the sheet output stage (422.38898ms)
✔ report footer shows its running line until the output opens (39.369159ms)
✔ preview footer shows a running line while the preview is pending (49.428986ms)
✔ help start failure replaces its running line with the warning hint (19.40064ms)
✔ a rejected sheet run clears the running line before propagating (30.329715ms)
✔ confirm rows need Ctrl+Enter and run confirmed (372.591527ms)
✔ Shift+Enter previews first and Apply reruns without the preview flag (830.833271ms)
✔ api.preview opens the sheet into a preview-first row's preview stage (369.894421ms)
✔ api.preview opens a report row in the output stage (373.028641ms)
✔ api.preview refuses excluded, unknown, unapplied-write, and unavailable rows (9.56507ms)
✔ api.preview focuses an already-open sheet and replaces its stage (448.691661ms)
✔ missing positionals enter argument mode instead of running (36.168333ms)
✔ a trailing ? runs help for the selected row in the output stage (368.375565ms)
✔ watching the sheet output suppresses the finish toast (385.983311ms)
✔ unavailable rows never activate (13.334808ms)
✔ RECENT rows drop the bob binary and keep unique keys (1.580971ms)
✔ RECENT vault-sync reruns without doubling the path (1447.510015ms)
✔ two RECENT rows for one entry select one at a time (736.871958ms)
✔ RECENT preview-first and confirm rows honor their guards (3247.243286ms)
✔ in-sheet r reruns vault-sync without doubling the path (742.700159ms)
✔ hidden below 400 ms, and never settles for such runs (5.855266ms)
✔ running keeps one mark element, brand label, tabular clock, and native tooltip (3.370204ms)
✔ two runs show count, longest clock, and click opens the newest (1.944895ms)
✔ queued-only gives is-queued and overdue writer gives is-overdue with budget tooltip (1.237295ms)
✔ settle shows outcome glyph for 1600 ms, then leaving, then hidden (1.077219ms)
✔ sequence model shows step, sequence clock, tooltip, and between-step visibility (3.436484ms)
✔ sequence chip lazily inserts step and title before the clock and hides them when idle (6.942714ms)
✔ sequence settle displays its final step and opens the focus run (0.852868ms)
✔ a new run during a settle shows running at once and click opens the settled run (1.212751ms)
✔ adopted unfinished runs appear flagged and all triggers light the indicator (1.350846ms)
✔ first visible paint uses HTMLCollection semantics and preserves existing classes (0.991167ms)
✔ DOM-like repaints keep the mark and anatomy idempotent (0.904934ms)
✔ DOM-like settle paint shows its outcome, then hides after the settle window (0.739668ms)
✔ plugin status-chip path paints an HTMLCollection-like status item (8.124369ms)
✔ BOB_CLI_DIR wins over a sibling checkout and a cache (58.119637ms)
✔ sibling bob-cli is used when BOB_CLI_DIR is unset (36.522131ms)
✔ an invalid BOB_CLI_DIR does not fall through (24.565358ms)
✔ cache clone is used when no user-owned checkout exists (60.483217ms)
✔ refreshing an existing cache keeps git chatter off stdout and forwards exact paths (78.464363ms)
✔ a cache clone with a foreign origin fails before fetch or reset (56.48176ms)
✔ a justfile alone is rejected as an explicit bob-cli checkout (33.712607ms)
✔ just failures propagate (46.572111ms)
✔ scans multiline, one-line, and guarded literal registrations (17.647527ms)
✔ scans an optional addCommand call (0.64798ms)
✔ allows addCommand references only in a typeof guard (0.66804ms)
✔ rejects bind, call, and aliased addCommand references with source locations (1.4341ms)
✔ expands literal command data from a constant-array forEach across source files (9.854924ms)
✔ balances nested callback syntax and ignores misleading comments, strings, templates, and regexes (1.389722ms)
✔ decodes escaped string metadata and literal default hotkeys (1.021802ms)
✔ returns no commands for a plugin without registrations (6.584633ms)
✔ fails with source locations for dynamic metadata, hotkeys, and malformed tables (1.871644ms)
✔ fails duplicate command ids with both registration locations (2.678177ms)
✔ checks drift without writes, preserves prose, and generates deterministically (43.347659ms)
✔ code-span table cells preserve backslashes and use a safe backtick fence (4.132804ms)
✔ does not write any output when source validation fails (6.142406ms)
✔ api.attachments v1 sends origin and import requests to bob (3.22256ms)
✔ origin and import decoders validate schema and payload shape (0.787229ms)
✔ attachment API preserves bob payloads through bobSpawnJson (4.00069ms)
✔ attachment API passes bob JSON failures through (2.497513ms)
✔ attachment API refuses mobile calls and never rejects (0.595144ms)
✔ render appends one listener-free miniature with row-identical attributes (7.786711ms)
✔ render decorative miniatures hide from assistive tech (0.418907ms)
✔ render accepts a synthetic digit model with no source task (0.372368ms)
✔ render uses the host ownerDocument, never a foreign one (0.381581ms)
✔ render returns null for bad input, a disabled gate, or no DOM (3.843511ms)
✔ api.blockMarks v1 keeps model and adds a gated render (0.702881ms)
✔ paint covers miniature, Live Preview, and reading rows under one gate (6.832004ms)
✔ chip-box fallback rules are body-gated and never !important (5.384444ms)
✔ every paint rule except the token block and motion query carries the gate (7.305346ms)
✔ paint keeps pip geometry, reduced motion, and the 120ms budget (2.717895ms)
✔ shipped mixes match the calibrated contract ramp (2.760416ms)
✔ waiting glyphs meet 4.5:1 on their washed rows, both themes (2.510902ms)
✔ white on the darkened held fill meets 4.5:1, both themes (2.638426ms)
✔ row tint and rail percentages ship in the gated rules (3.116947ms)
✔ helpers never throw on bad input (0.418895ms)
✔ Live Preview emits own-row line attributes once across visible ranges (26.309399ms)
✔ neutral rows, inline code, and fenced content stay unmarked (2.300388ms)
✔ current unsaved document text changes or removes the visible mark (1.792496ms)
✔ rebuilds on document, viewport, live-preview, path, and refresh effect, never selection alone (0.873258ms)
✔ hot model calls use the in-memory ladder and project lookup is memoized per path (7.179428ms)
✔ capture-phase tooltip attaches to the existing checkbox and restores owned attributes (5.146504ms)
✔ runBlockMarksRefresh rebuilds dependency chip editors (0.469961ms)
✔ toggle is reversible, refreshes views, rerenders Tasks, and shows exact Notices (0.442548ms)
✔ ladder invalidation compares semantic content and resume registers each editor document (6.392492ms)
✔ setup owns the gate and plugin-registered unload cleanup (1.614003ms)
✔ requestMeasure write-pass attaches tooltips after rebuild (4.580529ms)
✔ unscanned collect does not restore mouseover tooltip bindings (1.15971ms)
✔ prj rows fold the project tag; dep-over-prj keeps it; selection reveals (9.074336ms)
✔ registers the reading processor before field-transforming marks (2.982709ms)
✔ maps every family and pip from exact section source (18.130251ms)
✔ section-only text uses data-line offsets; full-note text adds lineStart (1.502509ms)
✔ quoted tasks and nested children classify independently (1.306825ms)
✔ cold cache stays unmarked until Tasks is ready, then sweep paints (1.414727ms)
✔ removed fields and recycled rows invalidate the retained mapping (1.251508ms)
✔ mismatched status or origin stays unmarked (0.585708ms)
✔ own-text fallback accepts raw fields and rejects transformed pills (1.874487ms)
✔ fallback never manufactures stale from lost field information (1.023845ms)
✔ Dataview delayed rows use proven origin and never the query note stem (2.461655ms)
✔ query result indexes are not read as source lines (0.911915ms)
✔ Tasks query rows stay excluded (0.764039ms)
✔ source-note lis Tasks also classifies still take JS marks (0.728259ms)
✔ tooltip attributes restore when the mark leaves or the toggle turns off (1.149578ms)
✔ toggle off and on reclassifies tracked hosts in place (1.958753ms)
✔ detached hosts dispose observers and drop owned attributes (1.102122ms)
✔ retained canonical text survives later field-transforming processors (0.831494ms)
✔ landing: recycled fallback row must drop the old scheduled reason (0.799547ms)
✔ landing: off-state sweep must preserve a later external tooltip (0.668344ms)
✔ landing: a Tasks row used as processor root must stay excluded (0.400119ms)
✔ landing: Dataview without proven origin must remain neutral (0.518502ms)
✔ Dataview transformed rows recover canonical text from the Tasks cache (2.561226ms)
✔ Dataview file links prove origin without data-task-path (0.879053ms)
✔ code and pre processor roots stay excluded like Tasks roots (0.502581ms)
✔ source-note fallback still paints when section mapping is absent (0.638147ms)
✔ query origin-loss and same-status origin-change invalidate retained marks (1.071249ms)
✔ repeated off sweeps, unload, and toggle after an external aria edit (1.491631ms)
✔ replacement checkbox nodes do not inherit the previous node's attributes (1.097116ms)
✔ neutral status transition releases owned tooltip attributes (0.658311ms)
✔ BM7 folds the project tag; BM19 keeps it (1.220198ms)
✔ source-note lis Tasks also classifies still fold BM7 and keep BM19 (0.745526ms)
✔ BM1–BM27 model vectors pass verbatim except Tasks-only BM24 (34.297033ms)
✔ BM tooltip wording and losing-reason order match the contract (1.708758ms)
✔ pure helpers preserve canonical eligibility, ids, digits, and decisions (4.999494ms)
✔ memo-local open-ID index keeps duplicate task IDs and project reasons one hop (6.4598ms)
✔ api.blockMarks v1 model is synchronous, frozen, toggle-aware, and neutral while cold (8.079578ms)
✔ model keys are stable for equal results and change with a changed mark (0.720261ms)
✔ fold helpers: digit keys, BM1/BM8/BM9 bars, BM7/BM19 pills (5.527756ms)
✔ BM24 Tasks CSS cascade: digit from future scheduled + medium, no project tag (9.654125ms)
✔ BK1-BK21 BLOCKS grammar, tolerance, and canonical ordering (7.251645ms)
✔ reverse index and 🔑 last-blocker rules (BC1-BC7, BC11, BC13) (6.266949ms)
✔ stale, missing, canonical append, and frozen-owner models (BC8-BC10) (1.284518ms)
✔ Live Preview, Reading view, shared toggle, and malformed rows (BC12, BC14, BC15) (19.490959ms)
✔ Reading BLOCKS chips map when the post-processor root is the nested list (3.46046ms)
✔ budget link counter ignores Depends-On and BLOCKS rows (MC1/MC2) (4.113222ms)
✔ chip builder includes the 🔑 badge and has no edit controls (1.853103ms)
✔ BLOCKS chip box covers prj, p2, stale miniatures and a throwing render (1.603892ms)
✔ RBC1 open owner with api.blocks shows ＋ and openStage gets the 0-based line (3.156431ms)
✔ RBC2 hover × on a live chip calls removeDependent; notice is nav's (1.372938ms)
✔ RBC3 frozen, stale, and no api.blocks stay navigation-only (1.480686ms)
✔ RBC4 Reading view matches Live Preview ＋ / × (4.766352ms)
✔ setup subscribes to the command-mode run-finished workspace event (1.702275ms)
✔ each invalidates tag refreshes its ledger cache and unknown tags are ignored (1.90809ms)
✔ duplicate tags refresh once and a failing hook never blocks the others (0.566763ms)
✔ payloads without invalidates and setups without a workspace never throw (0.565988ms)
✔ collections namespace version is additive v1 (3.321148ms)
✔ collection chip classes stay collection-specific through paint and refresh (5.491292ms)
✔ projects: scalar resolved links count, lists never widen (0.598468ms)
✔ projects: templates, status, and containsAny edges (0.695511ms)
✔ references: exact prefix, md only, exact scalar status (4.050907ms)
✔ base contracts: accept current files, reject drift, tolerate presentation (1.299589ms)
✔ entries: true zero vs unavailable with reason, failure isolation (0.557914ms)
✔ snapshot counts both collections once, true zero stays clickable (0.663148ms)
✔ snapshot never presents partial counts as final (0.548412ms)
✔ changed definitions fail closed per collection, never stale (0.864011ms)
✔ renderChip links, labels, and cleans up per component (1.06269ms)
✔ PENDING section excludes TODAY while the whole lane keeps it (7.992446ms)
✔ NEXT section excludes TODAY while the whole lane keeps it (1.201374ms)
✔ NEXT uses symbol *, not name matching (0.765777ms)
✔ READY badge and query agree on hide and path case variants (2.158972ms)
✔ blocked uses the full list even outside the visible subset (0.610954ms)
✔ duplicate block IDs, missing IDs, and reused objects stay per-row (0.831837ms)
✔ READY gating keeps exempt rows and drops NEW/ROTTEN (1.404856ms)
✔ throwing Today degrades to unavailable, never zero (47.052429ms)
✔ dashboard badges color the displayed section count and label whole-lane pressure (1.402546ms)
✔ dashboard section warning boundaries ignore TODAY-only whole-lane excess (1.695187ms)
✔ dashboard lane badge keeps unavailable data neutral (0.70102ms)
✔ dashboard lane paint and refresh keep color aligned with the visible section (13.360007ms)
✔ dashboard lane widgets refresh together and prune on unload (9.106215ms)
✔ daily paint matches dashboard section badges on screenshot fixtures (52.370107ms)
✔ daily paint lane lint matches a red badge section count (9.646739ms)
✔ daily and dashboard membership agree for exclusions and custom IN_PROGRESS (13.831858ms)
✔ daily paint refreshes with dashboard when Today, lane, and cap change (26.658241ms)
✔ older daily notes follow today's dashboard lanes (13.410136ms)
✔ daily lane anchors keep shared navigation and reject stale paints (13.679921ms)
✔ daily paint stays unavailable until Tasks and Today are ready (7.935865ms)
✔ work tones: dashboard lane models carry section tones (0.613399ms)
✔ T1 scheduled full-mode row gets a Fri mark inside the span (6.697071ms)
✔ T2 done row maps to a completion Oct 5 mark (1.898718ms)
✔ T3 short-mode created span is left untouched by JS (0.556142ms)
✔ T4 pending row decorates once data-task appears; exhausted rows stay native (2.516772ms)
✔ T5 a second pass adds nothing (0.797622ms)
✔ T6 task-due and task-start spans are untouched (0.743228ms)
✔ T7 an invalid date is untouched (0.476677ms)
✔ T8 nothing is scheduled with marks off or for connected non-Tasks elements (0.582195ms)
✔ T9 a Tasks-host Fri mark relabels to tomorrow on rollover (1.645439ms)
✔ renderDateMarksIn schedules one shared frame for every row (6.871892ms)
✔ the Tasks pass never throws on hostile input (1.447498ms)
✔ T10 real-DOM NodeList children decorate via direct and queued passes (3.041269ms)
✔ T11 toggling off before a queued frame runs writes nothing (1.153934ms)
✔ T12 a pending-row retry followed by disabling writes nothing (1.066797ms)
✔ T13 unloading before a callback runs writes nothing (3.340792ms)
✔ RT1 full-mode recurring result gets a daily mark and stays idempotent (2.147639ms)
✔ RT2 recurring labels use the shared cadence grammar (2.505579ms)
✔ RT2a unknown inherited-name rules stay readable in Tasks results (0.797274ms)
✔ RT3 short-mode recurring spans stay native to JS and use the CSS loop (1.944921ms)
✔ RT4 open checklist members keep recurrence pills without `when done` (0.787649ms)
✔ RT5 invalid recurrence stays native and incomplete rows are retried (0.732074ms)
✔ styles.css covers the Tasks hosts: hide, toggle-off, and short-mode glyphs (2.369188ms)
✔ DATE_MARK_FIELDS lists the four dates with verbs (4.266695ms)
✔ DM1 created today: label, tooltip, fold, quiet field (9.451564ms)
✔ DM2 created yesterday without space after the colons (1.352103ms)
✔ DM3-DM6 scheduled tomorrow, weekday, and month/day labels (0.578842ms)
✔ DM7 scheduled today reads with emphasis timing (0.418144ms)
✔ DM8 past scheduled uses month/day, never a weekday (1.425273ms)
✔ DM9 completion on a closed task keeps the timeline grammar (0.361002ms)
✔ DM10 cancelled across years appends the year (0.398262ms)
✔ DM11 next-year date appends the year (0.399458ms)
✔ DM12 the weekday rule wins across the year boundary (2.750349ms)
✔ DM13 two marks in order with folds 1 and 2 (1.120046ms)
✔ DM14 created and scheduled ranges stay disjoint from the fresh mark (0.859743ms)
✔ DM15-DM16 paren and padded brackets are canonical (0.423524ms)
✔ DM17-DM21 line shapes: bullets, quotes, and paragraphs mark (2.073613ms)
✔ DM22 code still parses pure but decorates nothing (see Live Preview) (0.286283ms)
✔ DM23 rescheduled is untouched and never a duplicate (0.291521ms)
✔ DN1-DN9 non-canonical fields get no mark (0.535202ms)
✔ dateMarkContentStart finds content on list, quoted, and plain lines (0.221833ms)
✔ dateMarkRelativePhrase covers the exact-day phrases (0.192885ms)
✔ dateMarkModel rejects unknown fields and bad dates, and falls back on bad today (0.635043ms)
✔ no model output contains a double colon (4.245874ms)
✔ a new day always changes the widget key (0.44757ms)
✔ element structure and the decorative/inheritColor/rendered options (1.037706ms)
✔ Live Preview emits several decorations in ascending order (3.053911ms)
✔ Live Preview reveals per field, never the whole line (0.708873ms)
✔ Live Preview refuses source mode, code, and disabled marks (1.350212ms)
✔ widget mousedown anchors at the field start for folds 0, 1, and 2 (1.903132ms)
✔ DM24 a cursor in the folded run unfolds the mark (vim cw) (0.551094ms)
✔ DM25 a cursor in Tasks double space unfolds only that field (0.423254ms)
✔ a selection ending inside the run unfolds; ending at its start keeps the fold (0.371585ms)
✔ no emitted decoration ever hides a cursor, and reveal still means field overlap (16.972212ms)
✔ dateMarkSelectionFold: reveal, unfold, fold, and garbage input (0.439212ms)
✔ mousedown on an unfolded (fold-0) widget anchors at the field start (0.694699ms)
✔ rendered views split several fields in one node (3.661473ms)
✔ rendered views skip exclusions and duplicates (1.340167ms)
✔ RO1 rendered marks relabel in place across midnight (1.354084ms)
✔ rollover dispatches once per day change and never touches widgets (3.168475ms)
✔ api.dateMarks v1 is additive, sync, and never throwing (1.29698ms)
✔ session toggle and onload wiring (23.720334ms)
✔ mark gate holds in popout windows for both toggle states (0.96427ms)
✔ styles.css contract: masks, tones, repair flag, resting (3.311349ms)
✔ day identity follows the canonical path, never the tab or mtime (3.589555ms)
✔ fence day parsing accepts YAML mappings and plain lines, nothing else (1.273628ms)
✔ report selection reads the default entry, an 8-day range, or nothing (24.492953ms)
✔ report window checks keep the page window only when it shows D (7.40803ms)
✔ week-grouped default never covers D, and a cold-cache today re-selects once (98.031444ms)
✔ a report that differs only in typical repaints (66.559196ms)
✔ paint from cache costs one frame and zero spawns (47.297918ms)
✔ off-screen and hidden-tab strips spawn nothing (155.357691ms)
✔ clean fresh entries never refetch, whatever changes (139.585803ms)
✔ visible changing strips spawn at most once per 30 s (247.133631ms)
✔ the 10-minute age rule refetches today without any change (87.144913ms)
✔ past days wait out the 10-minute gate (108.488976ms)
✔ several strips and the page share one spawn per key (70.553643ms)
✔ strips repaint for free when the page refreshes the shared key (104.382445ms)
✔ rollover re-keys today to a past day and refetches (120.455071ms)
✔ a stale-across-midnight report is never shown as so far (93.069236ms)
✔ window-edge days fetch the 8-day range (75.472656ms)
✔ future days render nothing and spawn nothing (22.477937ms)
✔ a failed refresh keeps the frame and shows the stale dot (107.739635ms)
✔ a failure with nothing cached shows the one-line error and Retry (135.784247ms)
✔ bob-not-found with nothing cached names stats.bob_path (68.029416ms)
✔ the fence parses day:, falls back to the note date, or explains itself (98.846078ms)
✔ the fence skips hover popovers and embeds, and unregisters on unload (15.948716ms)
✔ openStatsForDay pins the day, focuses the metric, and opens a new tab (4.640958ms)
✔ openStatsForDay opens a new tab when Stats is already open (2.440514ms)
✔ openStatsForDay keeps the page window when it already shows D (92.235037ms)
✔ openStatsForDay panel themes selects the Themes view (82.417994ms)
✔ openStatsForDay Notices when Stats cannot open (2.296101ms)
✔ the page honours a pinned day on its first paint (66.216897ms)
✔ renderStatsResult consumes the one-shot revealPanel (16.78683ms)
✔ every strip paints facts and links with no buttons and no vault writes (86.397429ms)
✔ change bursts coalesce behind one trailing quiet window (119.495562ms)
✔ mobile and spawn-less hosts render nothing and spawn nothing (35.624468ms)
✔ rollover synchronously skeletons visible and offscreen fences; visible refetch resolves as past (203.975566ms)
✔ fit observer registers once, refits on width change, and releases (6.934537ms)
✔ missing ResizeObserver is harmless (0.59534ms)
✔ openStatsForDay explicit clock selects the lens, pins the day, and persists the preference (7.511021ms)
✔ openStatsForDay explicit worked survives a remembered off-clock preference (2.810129ms)
✔ lane view sanitizes and cycles both -> roots -> themes -> both (6.134305ms)
✔ layout matrix: availability, skeleton, and hidden states (6.823423ms)
✔ layout copy uses areas under the area fallback with exact strings (0.57797ms)
✔ painter per view: order, first-row meta and switch, themes-first (43.206149ms)
✔ switch attributes, marks, and skeleton placeholder (19.646335ms)
✔ switch activation: click, Enter, Space call cycleLanes once with focus (6.000919ms)
✔ group aria-label names only the shown lanes (3.293371ms)
✔ lane-enter class appears only on a same-day view change (17.948237ms)
✔ registry: a switch repaints every record without a spawn, dedupes, and restores focus (111.897503ms)
✔ command Cycle Day stats bars is registered with its Notice copy (16.980324ms)
✔ persistence remember = device: setup loads, saves, and tolerates missing storage (40.112457ms)
✔ require time adds no eager StateEffect.define() (8.570811ms)
✔ renderPlanBlock puts exactly one host first with .bob-plan after it on canonical days (212.874826ms)
✔ non-daily, future, dashboard, mobile, spawn-less, and excluded blocks get no host (232.462443ms)
✔ paintPlanBlock keeps the same host node first with .bob-plan after it and no strip repaint or spawn (294.58592ms)
✔ toggle and stats.day_strip remove the host and class, re-enabling restores them (144.043064ms)
✔ unload releases the record and its observer (56.646555ms)
✔ rollover attaches future blocks and repaints today as a past day (105.752661ms)
✔ rollover skeletons a visible automatic today host synchronously; it resolves as past (239.354406ms)
✔ plan hosts never write the vault or journals (129.16024ms)
✔ cold plan host waits for visibility: no spawn before callback, false stays zero, true fetches once (165.039169ms)
✔ plan host paints synchronously from cache with zero spawn before visibility (53.488953ms)
✔ detached excluded blocks get no host; detached ordinary blocks attach synchronously (195.976061ms)
✔ no-observer fallback attaches detached, fetches on check after connect, releases excluded (290.694643ms)
✔ excluded after attach releases on the first observer callback (212.843552ms)
✔ excluded processor container gets no host (36.84159ms)
✔ reading-view order attaches detached, virtualized stays quiet until attach (173.145162ms)
✔ today host shows so far HH:MM from the fetch stamp (123.643669ms)
✔ failed refresh over a cached report names the HH:MM it shows (185.89491ms)
✔ placeholder finds .bob-plan by class and toggle-off restores it first (78.153322ms)
✔ statsThemeRef prefers theme_hues names and hues, with gray fallbacks (8.880185ms)
✔ theme mix orders coloured by minutes then gray, with unnamed last (36.304327ms)
✔ same-hue coloured themes take shade 0 then 1 then 2; gray is never shaded (1.973637ms)
✔ theme mix labels, ranks, overflow, titles, and aria follow the report (6.980402ms)
✔ theme lane is omitted for zero days, missing parts, and redefined worked (7.656833ms)
✔ fallback hue uses context.themeHueFor and stays gray without it (0.614096ms)
✔ painter uses swatches, shades, data-lane, and no buttons on the theme lane (3.790282ms)
✔ theme legend and bar open Stats on the Themes view (11.673975ms)
✔ fitter fits both legends independently and returns the roots result (6.080068ms)
✔ date words and day shifts use calendar integers, including leap day (3.550325ms)
✔ fact displays are selected from the exact day point, even with null headline and grouped input (12.708614ms)
✔ honest states carry meta text for today, past, stale today, and stale past (4.913539ms)
✔ time mix reuses Stats area ordering and hues, with buckets last and a tooltip title (37.307879ms)
✔ root_parent is preferred with an honest area fallback (1.79245ms)
✔ zero worked renders no Pomodoros and redefined worked omits its mix (3.276789ms)
✔ aria label carries the date, values, provisional state, and area names (1.089602ms)
✔ skeleton carries placeholder text per fact and the same tag and class sequence (9.477736ms)
✔ painter repaints in place, emits no buttons, and shows unavailable controls (7.283073ms)
✔ facts, mix, and Retry preserve day, focus, and new-leaf modifiers (3.99969ms)
✔ future and hidden models paint no children (0.547326ms)
✔ strip paints facts, legend row, then full-width bar with no buttons (3.216995ms)
✔ bar click opens Stats homes with day and new-leaf modifiers (3.729176ms)
✔ same-area roots get distinct hues and legend dots match their segments (5.093134ms)
✔ dayStripValueRuns splits numerals from units and keeps words whole (1.396942ms)
✔ facts stack a label head over a faithful value with warnings in the head (66.032364ms)
✔ root-parent labels use Bob's full home label (2.327283ms)
✔ unfiled root paints its label in gray after real roots (2.465565ms)
✔ area roots paint the bare label with a project_label tooltip (1.496422ms)
✔ case-insensitive legend labels keep their full root names (1.839746ms)
✔ dayStripLegendFit fits every root, reserves the counter, and handles empty (0.619744ms)
✔ names mode wins only when it names strictly more roots (0.224653ms)
✔ DOM glue hides overflow, writes the counter, and toggles names mode (3.932158ms)
✔ dayStripMarkState maps bool points from the bob point, never the word (1.392956ms)
✔ boolean facts paint an aria-hidden mark with hidden display text (5.469998ms)
✔ docs without createElementNS keep word runs (5.627463ms)
✔ bool skeleton paints a round placeholder and no svg (2.13359ms)
✔ pending mark tooltip drops so far; numeric provisional keeps it (0.814186ms)
✔ pending to met on the same host and day draws the check once (4.822251ms)
✔ arrive class stays off for other mark transitions (24.009518ms)
✔ stroke-dashoffset lives only inside keyframes (7.440529ms)
✔ dayStripRef classifies bob's typical without computing it (0.449875ms)
✔ typical line covers every States-table row (8.241837ms)
✔ typical line is aria-hidden, reserved, and never a tab stop (58.925934ms)
✔ off-clock hint prefers Bob's display and falls back to raw Nm without arithmetic (12.757733ms)
✔ hint renders below WORKED beside the typical line as its own activation target (13.159315ms)
✔ lane legends and bars keep Worked meaning while the hint opens Off-clock (1.724766ms)
✔ DP parse vectors (13.646599ms)
✔ DC chip model vectors (13.27775ms)
✔ decoration builds one widget, reveals on cursor, skips code and ranges (65.951335ms)
✔ decoration skips paragraphs, grandchildren, and Work Log lines (1.670061ms)
✔ decoration renders chips on DP30 and still skips DP20 (14.150226ms)
✔ ownership check reads O(depth) lines, not the whole note (14.04478ms)
✔ widget identity covers the line and the interactive flag (11.086268ms)
✔ element hides actions without nav api v1 (6.759303ms)
✔ nav api feature detection gates actions (0.626683ms)
✔ reading view decorates only the Depends-On row, hides chrome, stays idempotent (13.688893ms)
✔ reading view blocked chips draw a miniature and reason line (6.357323ms)
✔ reading view collapses more than three Done targets to one chip (6.893174ms)
✔ DC chip model vectors by id: DC2, DC5, DC6, DC9 (0.586877ms)
✔ chip actions send the 0-based line index through nav api v1 (6.709605ms)
✔ chip hover passes the chip element and its row to the preview (0.532254ms)
✔ chip lookup index lives on the freshness memo (1.15838ms)
✔ reading view hides actions when the line cannot be derived (41.898294ms)
✔ reading view actions carry the derived 0-based line (14.220093ms)
✔ reading view renders no chips on malformed, grandchild, Work Log, or blockquoted rows (1.20931ms)
✔ reading view renders chips on DP30 (owner is a task under a Work Log entry) (5.701673ms)
✔ reading view DP30 row actions send the owned Depends-On line (8.666965ms)
✔ reading view second-row remove sends the second line when two tasks share a prerequisite (6.354943ms)
✔ chip lookup index builds once per freshness memo (0.978322ms)
✔ decoration evaluates ownership without copying the note (4.072313ms)
✔ blockMarkReasonLine keeps only the first tooltip line (0.257721ms)
✔ chip box fill keeps a CSS fallback glyph beside the miniature (0.975273ms)
✔ toggle flips the body class and onload wires chips (49.002101ms)
event-link-times build: 7.4 ms
✔ EL — ledger rows qualify exactly per the contract (41.289059ms)
✔ EL18 — a fenced ledger row gets no pill (0.894309ms)
✔ EL19 — a non-daily note gets no pills (8.595697ms)
✔ EL16 — the previous day's ledger pills without state (9.214904ms)
✔ ES — the shared clock answers the contract states (4.073128ms)
✔ ER — resolution matches the Events pill inputs (19.487215ms)
✔ ER — non-events, duplicates, and cross-note links resolve to no pill (0.723779ms)
✔ ER5 — Live Preview reads the live document, unsaved edits included (19.284418ms)
✔ ER6 — Live Preview dashes an unsaved off-clock tag on the same frame (9.299907ms)
✔ ER7 — the inner pill carries the Events pill attributes, minus title (13.786839ms)
✔ ET — tooltips name the event and its pill state (5.801124ms)
✔ EP1 — Live Preview places the pill at the link start, side -3 (8.073229ms)
✔ EP4 — selection alone never rebuilds the pills (6.966642ms)
✔ EP2/EP5 — Reading view orders the pill before progress marks and keeps the ledger context (18.622889ms)
✔ EP3 — the pill lands before the link container beside a trailing chip (4.451941ms)
✔ EP3/OC — Reading sweeps preserve pill/link/marks/chip order and clock parity (28.134495ms)
✔ EP7 — a struck link keeps the pill outside the strike (14.765058ms)
✔ EL20 — either toggle off hides every pill, in JS and CSS (2.49061ms)
✔ setup — toggle command, popout gates, and clock repaint wiring (6.506679ms)
✔ liveness — metadata and vault events coalesce into one refresh (0.985482ms)
✔ liveness — a source-text fill refreshes link pills (1.398607ms)
✔ perf — one build over a 200-link ledger stays under 25 ms (20.009218ms)
✔ widget — identity follows time, state, clock, buffer, and tooltip (1.432406ms)
✔ regression FakeNode hides the plan-host cycles and builds 85 nodes (12.901568ms)
✔ failing assert.equal and assert.deepEqual report under a 1024MB cap (229.689965ms)
✔ every ledger-tools FakeNode-style fake has a descriptor and hides its cyclic fields (23.926387ms)
✔ FL1-FL16: the ledger link gates match the display contract (23.054105ms)
✔ motion identity is the resolved owner path and block ID (5.308172ms)
✔ duplicate and aliased links resolve and count once per owner per build (2.849593ms)
✔ offscreen ledger targets do no resolution or count work until visible (0.770819ms)
✔ 200-link / 2000-task build stays within the 25 ms budget (44.846225ms)
✔ FC1-FC17: counts follow the BLOCKS last-blocker set (13.808155ms)
✔ FT1-FT6: tooltips use BLOCKS order, clean titles, and waiting count (2.468729ms)
✔ FC7-FC8: project and hidden labels follow the contract (0.690267ms)
✔ FP1-FP2: Live Preview places the widget after the link with side 2 (2.893401ms)
✔ FP3-FP4: Reading view inserts after the link or after 🔓 (3.41129ms)
✔ Reading view inserts beside a task-link-mark sibling and through one wrapping p (2.637962ms)
✔ pinned midnight invalidates yesterday and gives today's editor a silent first paint (2.585435ms)
✔ FT element and widget keep accessible attributes without a title (1.707432ms)
✔ Live Preview tick LRU tracks 0 → N, count changes, and the 2000-key bound (3.198398ms)
✔ viewport-only rebuilds update visible count history without animating scroll-in (1.566254ms)
✔ toggle, refresh effect, and modifier navigation are wired (2.151097ms)
✔ setup is idempotent and teardown clears the rollover interval (0.583948ms)
✔ capability: nav card v2 is capable (2.493761ms)
✔ capability: nav card v1 is not capable (0.372845ms)
✔ capability: absent nav, missing api, and old versions are not capable (0.342829ms)
✔ capability: a throwing app never throws (0.342619ms)
✔ lane capability: nav card v3 is lane-capable, v2 is not (0.429895ms)
✔ leaf: active capable due choice replaces refresh with a leaf (7.193464ms)
✔ leaf: the same row without the card keeps refresh and counting words (0.86289ms)
✔ leaf: early dates still leaf when capable (0.774099ms)
✔ leaf: decay-off rows never leaf even when capable (0.671874ms)
✔ leaf: below-threshold rows never leaf (0.86727ms)
✔ leaf: threshold zero asks on every due re-confirmation when capable (0.685308ms)
✔ leaf: overflow renders capped dots with +N and the exact count in text (0.651725ms)
✔ leaf: out-of-scope and closed tasks show dots quietly, never a leaf (1.408199ms)
✔ leaf: unresolved marks show dots quietly with counting-only wording (0.533678ms)
✔ element: leaf marks carry data-decide true and a leaf path (1.105357ms)
✔ element: non-decision marks carry data-decide false (3.642019ms)
✔ lane leaf: an at-limit Next row leaves only with the v3 card (0.484476ms)
✔ lane leaf: the same row with only the v2 card keeps counting pips (0.406682ms)
✔ lane leaf: an at-limit WIP row leaves only with the v3 card (0.43274ms)
✔ lane leaf: a false rung counts and displays but never asks (0.388111ms)
✔ lane leaf: a per-rung limit drives the keeps wording (0.444101ms)
✔ footer groups omit every zero tier and keep walk order (19.060009ms)
✔ PRE and POST groups bracket the nine-tier queue and expose completion hints (4.469716ms)
✔ a NEW-state project appears only in its walk tier (0.437994ms)
✔ empty queue hides the footer even with upkeep or a met budget (0.484222ms)
✔ unavailable or missing data never render false counts (0.309816ms)
✔ generic summary names due, commitments, and nonempty groups (5.885784ms)
✔ current-task context uses shared ranks and compact wording (1.608308ms)
✔ only ROTTEN remaining names commitments done or a met budget (0.54341ms)
✔ NEW and commitments take precedence over a met budget (4.105548ms)
✔ reviewEntryView compact and detail cover the original freshness tiers (4.783691ms)
✔ cursor matching requires a unique verified identity (1.256035ms)
✔ footer paint hides the host and keeps a stable button (2.404019ms)
✔ groups paint as tier-keyed tokens and repaint without stale nodes (8.21379ms)
✔ group boundary marks only the commitments-to-upkeep cut (1.025808ms)
✔ context ink follows supported current tiers and clears on other views (1.167337ms)
✔ progressive fit sheds tail groups, then detail, hint, and meter (6.207267ms)
✔ the footer stylesheet defines every tier ink and removes NEW accent overrides (2.21469ms)
✔ status bar 0-1-0 transitions hide without a reload (83.293716ms)
✔ cursor-only updates reuse a warm memo (16.806075ms)
✔ unload disconnects the observer and click handler (10.098048ms)
✔ queue-built ranks agree with the footer current entry (8.444147ms)
✔ footer short labels map every tier (0.244382ms)
✔ current-row footer context uses short labels while entry views keep full labels (0.55803ms)
✔ legend line lists only current abbreviated tiers (0.552371ms)
✔ queue-row quickRoll preview takes the hint slot, tooltip, and aria (5.066862ms)
✔ quickRoll detail sits next to the action hint on lane rows (0.593974ms)
✔ missing or failed quickRoll leaves a queue-row footer byte-identical (4.824732ms)
✔ off-walk prioritized preview replaces ]s next (0.660059ms)
✔ off-walk assign or kind-less preview keeps ]s next (0.3784ms)
✔ empty queue with a prioritized preview paints a hint-only footer (0.453923ms)
✔ PRE rows stay unchanged under the nav checklist-tier contract (0.369059ms)
✔ status bar wires nav api.quickRoll into the hint slot (11.567023ms)
✔ empty-queue status bar previews only a checkbox task line (8.595038ms)
✔ off-walk task preview works with a queue and survives its 1-to-0 transition (12.047686ms)
✔ status bar ignores missing, v0, or throwing quickRoll namespaces (28.165847ms)
✔ K1 absent: no keeps means 0 with no lints (12.399942ms)
✔ K8 misplaced: keeps inside the Tasks suffix reads with a lint (3.865279ms)
✔ K9 duplicates and invalid values: first valid wins, else 0 (1.025477ms)
✔ K10 ceiling and NEW: 999 reads, never-confirmed reads 0 (0.434042ms)
✔ K13 exact keys: near-miss keys are not keeps; parens read (0.373883ms)
✔ keeps value parser accepts only decimal 1-999 (0.411123ms)
✔ K2 first valid canonical: uncounted keep preserves and repairs (5.10048ms)
✔ K3 refresh/keeps order canonicalizes to fresh, refresh, keeps (1.178085ms)
✔ K4 same-day preserve noop: canonical kept line is byte-identical (0.744813ms)
✔ K5 generic stamp clears, even same-day (0.647926ms)
✔ K6 set-refresh clears keeps (0.479767ms)
✔ K7 stale stamp clears keeps (0.243911ms)
✔ K8b misplaced keeps repaired to canonical order by a keep (7.609795ms)
✔ K11 refusals preserve: closed and recurring lines never write (0.538176ms)
✔ Pomodoro ledger rows are refused byte-for-byte by counted and uncounted keep (0.696384ms)
✔ counted keep increments a stale streak once in the same write (0.394216ms)
✔ first counted keep on a streakless due task writes keeps 1 (0.282172ms)
✔ counted keep saturates at 999 and never wraps (0.367415ms)
✔ counted keep needs a valid prior fresh before today (5.63548ms)
✔ counted keep repairs malformed and duplicate placement (0.514176ms)
✔ uncounted keep preserves the valid value while canonicalizing (0.443961ms)
✔ UB13 keep on an unblock TICKLER preserves the streak and skips the card (9.906058ms)
✔ a scheduled tickler still counts when schedule wins an unblock tie (0.866043ms)
✔ decay normalization: absent, null, true, and {} enable with 3 (1.315851ms)
✔ decay false counts and displays but never asks (5.502879ms)
✔ decay keeps 0 and fixed entry normalize (0.351391ms)
✔ C14 pending override resolves while other rungs fall back (0.262848ms)
✔ C15 fallback plus next override (0.237314ms)
✔ C16 zero, false, and 999 rungs (0.31094ms)
✔ C17 null rung falls back to keeps (0.474549ms)
✔ rung limit helper resolves numbers, false, and fallbacks (0.191683ms)
✔ invalid decay shapes fail the freshness config contract (3.065311ms)
✔ B: at-limit Ready due rows decide on every local day (1.32665ms)
✔ D1 early date: an at-limit Ready due row decides (0.312576ms)
✔ D2 at limit decides; D3 below limit stamps without a card (0.330862ms)
✔ D4 tickler counts as due; D5 NEW never decides (0.247401ms)
✔ D6 zero limit asks on every due Ready re-confirmation (0.183986ms)
✔ D7 off never asks; D8 an at-limit Next due row decides (0.197727ms)
✔ D9 pending at limit decides; D10-D11 below limit stay quiet (4.341541ms)
✔ D12 next_keeps false never asks; D13 pending_keeps 0 always asks (0.482854ms)
✔ D14 today-linked lane rows never decide (0.354121ms)
✔ D15 projects never decide; D16 unblock ticklers never decide (0.260481ms)
✔ D17-D18 next_keeps override of 5 decides at 5, quiet at 4 (0.305114ms)
✔ lane rows decide through the evaluator, queue, and counts (1.650599ms)
✔ evaluator, queue, and counts carry keeps and decide (1.748577ms)
✔ no keeps: the existing mark is unchanged (9.102048ms)
✔ aging with two keeps: faint pips plus a counting-only line (0.622808ms)
✔ confirmed today with two keeps: check glyph, faint dots (0.446311ms)
✔ due below threshold: orange capsule keeps its glyph, adds dots (7.039945ms)
✔ resting marks show historical dots quietly and never decide (0.667824ms)
✔ active decision due: data stays truthful, leaf stays gated (0.648149ms)
✔ dot caps follow the threshold with +N overflow (0.711786ms)
✔ keeps tooltip wording: singulars, zero threshold, off state (0.26097ms)
✔ noncanonical keeps never fold but keep their repair pill (3.893379ms)
✔ quoted lines fold; rendered fragments fold without task checks (0.722538ms)
✔ unresolved marks show the line's own pips quietly and never decide (0.473231ms)
✔ consensus sees count and decision eligibility: ambiguity stays neutral (1.070356ms)
✔ pips render as one aria-hidden span with the count in the label (5.636202ms)
✔ Live Preview decorates the folded range including space and refresh (10.646709ms)
✔ Live Preview reveals the raw field when the cursor overlaps either edge (2.205504ms)
✔ Live Preview skips codeblock and inline code spans (1.356802ms)
✔ source mode and marks-off yield no decorations (0.403564ms)
✔ update rebuilds on the refresh effect and widget eq is stable (2.112954ms)
✔ widget click reveals the field at the folded offset (1.867679ms)
✔ line resolver prefers exact, then consensus, then unresolved (2.338532ms)
✔ decoration builds reuse the snapshot without touching the loader (1.157932ms)
✔ rendered views split text nodes and skip excluded ancestors (4.655281ms)
✔ rendered views stay idempotent (1.145942ms)
✔ text resolver reaches consensus and degrades to neutral (1.339776ms)
✔ session toggle flips the body class and notifies (2.396524ms)
✔ Live Preview reads only the child block and never calls doc.toString (3.614973ms)
✔ Live Preview stops at the first nonblank line at or above the task (0.813971ms)
✔ Live Preview performance stays bounded on a large child block (3075.792347ms)
✔ reading view shows the rotten line and excludes Tasks and Dataview rows (1.196137ms)
✔ reading-view DOM history counts a Next lane entry (1.865666ms)
✔ query-row consensus stays byte-identical with and without a Rotten Log (0.793193ms)
✔ onload registers the toggle, extension, and post-processor (25.266057ms)
✔ mark gate holds in popout windows for both toggle states (1.171514ms)
✔ shared grammar fixture round-trips parse vectors and tallies (18.561604ms)
✔ M1 today: check glyph, today label, full ring (23.128561ms)
✔ M2 aging: ring glyph, 3d label, draining lease (8.15112ms)
✔ M3 boundary: ROTTEN due capsule with Alt+F hint (0.760135ms)
✔ checklist marks replace stamp hints with their completion tier (5.537863ms)
✔ M4 yesterday uses the yesterday relative (0.650894ms)
✔ M5 folded refresh shows the /14d suffix (1.112993ms)
✔ M6 refresh today: today tone hides the interval suffix (3.947026ms)
✔ M7 note interval stays tooltip-only (0.751227ms)
✔ M8 resurfaced: due tone on the scheduled return (0.897583ms)
✔ M9 due NEXT lane with keep/release/today keys (3.974139ms)
✔ M10 NEXT lane stamped today (0.564686ms)
✔ M19 disabled Next lane rests (0.61339ms)
✔ M20 PENDING lane folds refresh without the suffix (0.564483ms)
✔ M11 closed: resting beats age 0 (3.964842ms)
✔ M12 unresolved running and M13 unresolved lease over (0.657882ms)
✔ M14 linked today rests with its reason (0.516832ms)
✔ M15 other year shows the year and the 282d age (0.317383ms)
✔ M16 quoted line keeps foldSpace (0.361129ms)
✔ M17 invalid refresh is not folded; M18 non-adjacent keeps no suffix (0.795962ms)
✔ N1-N6 non-canonical lines get no mark (3.569464ms)
✔ C1-C3 consensus is exact or unresolved (1.241179ms)
✔ freshnessMarkResolution treats evaluator new as unresolved (0.31435ms)
✔ freshnessMarkSourceInText covers rendered fragments (0.42331ms)
✔ tone order: closed, then due, then age 0, then out of scope (4.519392ms)
✔ no tooltip ever contains a double colon (1.687675ms)
✔ freshnessShortDate pins English names and the year rule (0.263348ms)
✔ DOM builder structure, attributes, and ring geometry (11.574073ms)
✔ every mark helper is synchronous and never throws on bad input (0.322816ms)
✔ rotten line wording covers 0, 1, and many entries (0.88425ms)
✔ rotten line date format includes the year only when it differs (0.33074ms)
✔ rotten line truncates the reason to 48 code points without splitting emoji (4.519897ms)
✔ rotten history rejects ambiguous, invalid, and nested entries (2.596322ms)
✔ rotten marker vectors reject mismatched emoji and missing spaces (1.641751ms)
✔ rotten line splices before the action line and reaches aria-label (4.959398ms)
✔ freshness namespace v13 exposes per-rung decay plus unblock TICKLER writers (39.151214ms)
✔ freshness state and count API expose an unblock return source (4.325234ms)
✔ checklist rows report tier and rank while keeping the READY bucket null (3.732424ms)
✔ tier, isDue, and rank cover lane rows (10.094631ms)
✔ memo invalidates on a new tasks array, rollover, and frontmatter (30.200469ms)
✔ the reload event fires only when the due key set changes (19.655102ms)
✔ status bar text covers every state, and a missing host stays quiet (18.590148ms)
✔ status bar clicks through, falling back to rotten (37.537433ms)
✔ every freshness api member is synchronous and never throws (9.828613ms)
✔ placement vectors P1-P11, P14-P16, P18 stamp canonically (8.015814ms)
✔ P12 set and clear refresh stamps alongside (0.687657ms)
✔ P13 recurring and P17 done tasks are refused unchanged (0.423927ms)
✔ Pomodoro ledger rows are refused byte-for-byte by every fresh writer (1.187431ms)
✔ a time range later in task prose remains eligible for freshness (0.425719ms)
✔ U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode (1.595567ms)
✔ reader reports misplaced and duplicate fields (0.826113ms)
✔ Q1 Bryan's example orders A, D, C, B by interval, lateness, newest created (11.922173ms)
✔ Q2 tier order beats path order (5.999659ms)
✔ L1 lane due and stamped today (0.829367ms)
✔ L2 lane overrides refresh (0.498922ms)
✔ L3 lane exclusions have no tier (0.734287ms)
✔ L4 lane off switch and null default (3.93531ms)
✔ L5 lane order never stamped first (1.007757ms)
✔ R1 TICKLER beats older ROTTEN (4.69092ms)
✔ R2 tickler orders by due date then path and line (0.874223ms)
✔ missing created sorts after dated peers (1.09162ms)
✔ B1 upkeep counts outside the lanes (10.654859ms)
✔ review model meter uses upkeep and exposes refreshed (0.841829ms)
✔ RC1 arrived: past scheduled walks RECURRING with lane and null state (6.277905ms)
✔ RC2 arrives today: due today with zero days overdue (0.635057ms)
✔ RC3 not yet: future scheduled walks nowhere (0.434334ms)
✔ RC4 due only, past: the due date is the occurrence (0.443349ms)
✔ RC5 due only, future: walks nowhere (0.380697ms)
✔ RC6 earliest date wins across start and due (0.435616ms)
✔ RC7 undated: no occurrence, no tier (0.514461ms)
✔ RC8 lanes: recurring lane rows keep their lane with null state (0.85758ms)
✔ RC9 exclusions: Today, daily note, hidden, blocked, templates, [?] stay out (2.317828ms)
✔ RC10 checklist wins: a recurring chore stays in its checklist tier (0.489052ms)
✔ RC11 a stray stamp is ignored: recurring with null state (0.422735ms)
✔ RC12 order and counts: due_on, then path, then line; recurring adds no due (2.847183ms)
✔ recurring rows adapt due and start from Tasks fields and inline fallbacks (8.001066ms)
✔ status view counts RECURRING as a due commitment tier (0.828017ms)
✔ footer groups, entry view, and legend cover RECURRING (1.920229ms)
✔ a stale-stamped recurring row marks due with the resolve hint (5.234057ms)
✔ freshness namespace v13 keeps recurring and removes reference capabilities (43.928433ms)
✔ hidden recurring ^ref keeps ordinary visibility (Rust parity) (3.033134ms)
✔ bucket partition vectors: S1 new, S3/S4/S11 rotten, the rest null (13.9016ms)
✔ day numbers stay calendar-local across a DST boundary (0.928827ms)
✔ reviewModel shares counts, meter, tooltip, and severity (1.008764ms)
✔ memo serves warm map hits and misses use the per-row evaluator (25.411492ms)
✔ config snapshot caches the parse and invalidates explicitly (3.963996ms)
✔ review chips share the model with severity classes (2.121243ms)
✔ warm lookups reuse one snapshot without re-reading config (4.004275ms)
✔ same-array cache updates and Today changes rebuild the memo (10.190711ms)
✔ duplicate block IDs keep each row's own classification (36.180239ms)
✔ line identity separates same-path rows without block IDs (24.056602ms)
✔ interval lookup serves the cached interval with one memo acquisition (14.255837ms)
✔ S1 new through S4 overdue (7.138144ms)
✔ S5 task beats note, S6 note beats config, S7 config (1.201578ms)
✔ S8 invalid overrides fall through with lints (0.739676ms)
✔ S9 malformed and S10 future stamps read as new (0.515488ms)
✔ S11 resurfaced beats rotten, S12 scheduled-equals-fresh stays fresh (0.616704ms)
✔ S13 out-of-scope rows read null (0.716172ms)
✔ S14 queue order (rewritten): NEW then TICKLER beats ROTTEN (2.68817ms)
✔ S15 counts (updated): upkeep outside the lanes drives the budget (2.547251ms)
✔ config coercion keeps defaults, flags invalid, ignores unknown keys (2.787799ms)
✔ loadFreshnessConfig reads the block with plan-style injectables (1.645725ms)
✔ interval precedence is task, note, config, default (0.473397ms)
✔ intervalForLine covers every source with its Ready fallback (1.432411ms)
✔ project tracking stays special while reference tasks use ordinary Ready freshness (24.299151ms)
✔ reference tasks match ordinary interval precedence and lane behavior (11.022635ms)
✔ obsolete reference interval keys are ignored and project config still validates (8.511548ms)
✔ references use ordinary keep decisions and the nine-tier queue shape (11.511191ms)
✔ CL1-CL7: exact checklist scope, precedence, and unchanged state buckets (20.112346ms)
✔ CL8-CL12: nine tier order, checklist-only due counts, and completion semantics (18.889783ms)
✔ freshness namespace v13 retains the tracker capability contract (41.637385ms)
✔ UB1 marks an in-scope Ready recovery and evaluates it as a TICKLER (6.689118ms)
✔ UB2-UB6 skip NEW, scheduled, lane, recurring, hidden, and Today rows (0.931116ms)
✔ UB9 fresh equal to unblocked resurfaces; UB10 chooses the latest return date (0.681346ms)
✔ UB11 scheduled wins a tie with the unblock date (0.723387ms)
✔ unblocked reader takes the latest valid duplicate and reports malformed values (0.727731ms)
✔ UB12 unblocked remains outside the Tasks suffix before scheduled/dependency fields (0.767591ms)
✔ UB14 TICKLERs with the same due date sort only by path and line (3.271445ms)
✔ UB15 a scheduled ^prj resurfaces in PROJECTS (0.390177ms)
✔ calendar scan stays within an unfenced Events section (7.958935ms)
✔ calendar scan finds same-day and dated Events stamps and ignores lookalikes (2.018487ms)
✔ stamp state stays fresh on change, including old, future, and dated stamps (0.698666ms)
✔ event clock state distinguishes future, running, and past (0.397015ms)
✔ afternoon and evening spans stay future until they start (ES1-ES10) (0.702267ms)
✔ a buffer delays past fade and lights lead-in / lead-out wings (0.317535ms)
✔ calendar scan reads [buffer::] and exposes wing data (1.92228ms)
✔ Reading view inserts hatched buffer wings beside the time pill (1.235017ms)
✔ sync-on-create gate only accepts today's canonical daily note (1.444067ms)
✔ create listener runs once for today's note after layout readiness (1.365549ms)
✔ sync-on-create waits for Templater's Pomodoros section, then stops at its deadline (0.96498ms)
✔ calendar paint teardown clears the clock refresh interval (0.748965ms)
✔ off-clock Live Preview paints one chip widget and no split marks (4.549023ms)
✔ off-clock chip preserves alias spelling and case (2.03363ms)
✔ off-clock chip reveals the raw tag while the cursor is on the line (0.806041ms)
✔ buffer and off-clock decorations stay sorted and disjoint (1.476806ms)
✔ a selection-only update reuses the cached scan (1.758875ms)
✔ the off-clock chip DOM carries the class, marker, and title (0.387459ms)
✔ scan treats #on as on-clock even beside an off spelling (0.402487ms)
✔ inherited off-clock Event Tasks dash the pill with a from-note tooltip (5.662711ms)
✔ Live Preview dashes inherited rows and keeps #off chips (1.854381ms)
✔ Reading view dashes inherited pills and tooltips #on overrides (0.832114ms)
✔ gcalEventsDecodeSync treats missing deprecations as empty (0.470725ms)
✔ gcalEventsDecodeSync keeps additive deprecations[] (0.630687ms)
✔ deprecation Notice fires once per day from a successful auto-sync (0.636328ms)
✔ decode accepts schema 1 and marks the rest unsupported (7.47525ms)
✔ parity fixture counts 5 open top-level tasks (4.323199ms)
✔ inbox tree membership walks area notes under inbox.md (7.439535ms)
✔ keepInboxTreeCounts skips nested done cancelled and non-members (7.76786ms)
✔ hidden before the first read and when unconfigured (0.893321ms)
✔ unverified hides Keep but keeps a live inbox (1.015932ms)
✔ fresh, stale, and signin tones (6.470545ms)
✔ each segment hides at zero and the item hides when both are empty (5.029517ms)
✔ old verified ok counts hide Keep until checked again (0.609069ms)
✔ unsupported hides Keep and lives only with a positive inbox count (0.88105ms)
✔ tasks-not-ready hides the inbox even when bob's inbox.open is positive (0.627176ms)
✔ tooltip and aria copy with a fixed now (0.47768ms)
✔ inbox tooltip lists the tree breakdown and names the click target (4.427967ms)
✔ paint draws Lucide icons from the obsidian setIcon export (6.680746ms)
✔ paint hides the item when both counts are zero and restores it (1.05882ms)
✔ paint key is stable and paint skips unchanged frames (0.547796ms)
✔ spawn wiring uses cache-only status with the Keep decoder (5.41196ms)
✔ gkeep command-mode tag routes to the Keep inbox refresh (0.773801ms)
✔ automatic checks require attention and a deferred timer fires on input (7.960091ms)
✔ status timers clamp to one minute through two hours and null cancels (0.393426ms)
✔ layout schedules its first automatic check after fifteen seconds (4.913378ms)
✔ focus triggers coalesce to one refresh per fifteen seconds (7.040714ms)
✔ unattended focus reads cached status without refreshing Keep (5.075115ms)
✔ unconfigured focus cache reads are throttled for ten minutes (6.901996ms)
✔ single flight queues one request and upgrades it from cache to forced (6.280324ms)
✔ forced check feedback follows the bob refresh result (80.138386ms)
✔ bulb clicks route by tone and missing Command Mode gives a preview hint (1.048387ms)
✔ context menus omit Command Mode actions when its preview API is unavailable (4.047661ms)
✔ turning the indicator off prevents all new automatic and forced checks (0.453538ms)
✔ keepInboxRecountNow stores the inbox-tree total and notes (4.262196ms)
✔ inbox click opens the note with the most open tasks (2.340078ms)
✔ context menu Open gkeep_inbox.md still opens the Keep target (0.768319ms)
✔ verified transition to auth shows one sign-in notice per session (3.538024ms)
✔ membership: pending/next/ready in, exclusions counted, today dropped (6.986713ms)
✔ membership: review-bucket Ready tasks are excluded and counted as reviewReady (2.628825ms)
✔ parity: pending/next match the dash section; ready matches readyCountFromTasks (3.546999ms)
✔ order: pending, then next, then ready, path then line inside each lane (1.372128ms)
✔ ranks: rank/total plus per-lane laneRank/laneTotal (0.652594ms)
✔ identity: keys match freshnessRowKey (0.608785ms)
✔ unavailable: throwing isToday propagates to the caller (0.505803ms)
✔ mixin: memo hits and invalidates; version 2; ready matches the chip (3.146306ms)
✔ mixin: unavailable reasons for tasks, today, and error (0.475066ms)
✔ shape: the result and its entries are frozen (0.597876ms)
✔ shared vector: back-to-back-worked-run (28.751446ms)
✔ shared vector: off-clock-event-stamps-key (1.778274ms)
✔ shared vector: off-clock-run-breaks-at-worked-event (1.010851ms)
✔ shared vector: worked-run-breaks-at-off-clock-event (2.136793ms)
✔ shared vector: overlapping-events-share-a-run (0.989738ms)
✔ shared vector: late-join-clamps-to-closed-session (1.051687ms)
✔ shared vector: running-event-starts-at-its-own-start (0.641288ms)
✔ shared vector: early-start-writes-future-start (9.301154ms)
✔ shared vector: far-run-warns-with-escape-hatch (1.457766ms)
✔ shared vector: ended-done-and-cancelled-events-are-skipped (1.412477ms)
✔ shared vector: no-lineup-events-keeps-the-default-pomodoro (8.590783ms)
✔ shared vector: counted-suffix-keeps-clock-classification (0.941619ms)
✔ shared vector: restart-rederives-the-run (0.552554ms)
✔ shared vector (capture-only): drop-removes-an-event-from-the-run (0.265338ms)
✔ shared vector (capture-only): kept-swap-into-off-clock-meet-moves-key (0.109144ms)
✔ shared vector (capture-only): kept-swap-out-of-off-clock-meet-restores-worked-key (0.093281ms)
✔ shared vector: named-meet-start-uses-the-run (0.438468ms)
✔ shared vector: non-meet-lineup-follows-counted-links (1.318099ms)
✔ shared vector: pre-buffer-starts-the-run-early (1.244234ms)
✔ shared vector: post-buffer-bridges-to-the-next-event (3.895736ms)
✔ shared vector: buffer-never-bridges-trackedness (0.574593ms)
✔ shared vector: now-inside-a-lead-out-keeps-the-run (0.402376ms)
✔ shared vector: buffered-far-run-warns-from-the-buffered-start (0.59037ms)
✔ shared vector: inherited-root-event-is-off-clock (7.521628ms)
✔ every vector is either mirrored or listed as capture-only (0.289039ms)
✔ off-clock tag detection mirrors bob's Rust rules for every spelling (4.148441ms)
✔ clean titles strip every off-clock spelling and its sentence punctuation (0.347692ms)
✔ Event rows carry status, clock, ids, and clean titles (0.833941ms)
✔ N\p and N\P keep the row's key; a bare span is stamped [off::]; a conflict resolves to [t::] (3.832155ms)
✔ N\o and N\O keep every key and field byte-for-byte (0.391556ms)
✔ pomodoroSessionClock reads all five row shapes like Rust session_clock (0.797527ms)
✔ setPomodoroLineClock moves the recorded minutes between keys like Rust set_ledger_clock (0.688649ms)
✔ a non-MEET se<X> start warns when it newly crosses an open event (1.913729ms)
✔ a counted start that fits ends before the event and stays silent (0.668634ms)
✔ a start with no fitting count omits the fit draft (0.914074ms)
✔ MEET sessions, own-lineup events, and done events never warn (0.923904ms)
✔ \p and \o warn on new crossings only; \P never warns (1.112302ms)
✔ event_buffer row vectors: parse, buffered span, clean title, field, label (1.619614ms)
✔ event_buffer conflict vectors: shared predicate (1.827794ms)
✔ event_buffer description vectors stay bob-cli's HTML reader (0.201154ms)
✔ a buffered se<X> start warns into the lead-in and fits at the buffered start (0.618283ms)
✔ a start that runs through the meeting names the event plus its buffer label (0.495131ms)
✔ a lead-out start names the after buffer and offers no fit (0.648335ms)
✔ an Event Task with a typed off-clock tag is painted by the Event scan (2.016302ms)
✔ an off-clock session's home chip is dashed, shows its minutes, and says so (0.812488ms)
✔ Reading view marks the off-clock tag link and dashes the row's time pill (0.986174ms)
✔ Reading view marks every off-clock tag spelling and nothing else (0.727314ms)
✔ an active-note Pomodoro target still jumps and centers immediately (77.597595ms)
✔ Ctrl+9 from an unpinned daily copy switches to the pinned home tab (19.09919ms)
✔ Ctrl+9 on the pinned daily tab jumps in place when a copy exists (10.80573ms)
✔ Ctrl+9 switches daily copies without a Pomodoros section and stays quiet (8.719653ms)
✔ Ctrl+9 keeps the active daily tab when equal-ranked copies exist (12.884331ms)
✔ Ctrl+9 from a sidebar daily copy switches to a main-area home tab (22.112831ms)
✔ the first fallback press only opens daily and the second press jumps (18.987205ms)
✔ a daily note with no target defers its notice until the second press (11.511805ms)
✔ an already-open daily leaf retains its live cursor and viewport (4.719373ms)
✔ a second press after reused-leaf fallback performs the Pomodoro jump (22.90575ms)
✔ the standalone daily-note command activates a reused daily leaf (6.033559ms)
✔ Ctrl+9 loads and reuses a deferred pinned daily tab before falling back (7.148736ms)
✔ pinned daily tabs win over earlier unpinned tabs (7.380552ms)
✔ a deferred sidebar daily tab is reused only without a main-area match (9.587515ms)
✔ a deferred sidebar daily tab is reused when there is no main-area match (2.311485ms)
✔ a deferred non-Markdown daily path is ignored and uses the daily-note fallback (6.333446ms)
✔ the standalone daily-note command reuses a deferred pinned tab (13.142912ms)
✔ Ctrl+9 opens the pinned daily tab from a non-Markdown active leaf (6.26608ms)
✔ a closed then reopened daily note restores its in-session location (7.371088ms)
✔ different-path and invalid locations do not leak into a daily note (11.348034ms)
✔ out-of-range remembered coordinates are clamped safely (3.56715ms)
✔ a rapid second press cancels an older fallback restore (2.77942ms)
✔ navigation and unload clean up daily scroll listeners and deferred work (2.476775ms)
✔ crowded chip: over count is red with tooltip, aria, and names (2.796322ms)
✔ crowded chip: calm zero and unavailable dash (0.545436ms)
✔ crowded chip: names at most five notes (0.607952ms)
✔ crowded chip: classes, text, aria, and arrow (3.408421ms)
✔ crowded chip: refresh in place keeps the anchor, unload drops it (1.671382ms)
✔ anchor helper keeps READY, PENDING, NEXT, and CROWDED classes (0.874262ms)
✔ ready-notes summary: crowded, calm, and unavailable (1.94908ms)
✔ ready-notes bar: cap tick and red overflow within 30 cells (0.492272ms)
✔ ready-notes block: model and render with grid, pills, and footer (2.694514ms)
✔ ready-notes block: unavailable renders a dash line (0.638548ms)
✔ heading matcher: fences, level, case, and first-only (0.776701ms)
✔ heading chip copy: room, full, crowded, exempt, unavailable (1.852678ms)
✔ heading chip key is stable for equal models (0.35309ms)
✔ reading view: appends the chip to the matching h2 only (3.527057ms)
✔ reading view: no chip for ineligible notes (0.30006ms)
✔ one live-refresh fan-out reaches every family (3.075879ms)
✔ ledger-tools CSS is theme-safe for the new views (2.084692ms)
✔ maxReadyPerNote defaults to 5 and validates 1–999 (8.811042ms)
✔ loadPlanCaps caches on a stat key and detects edits (4.387612ms)
✔ loadPlanCaps handles deletion, invalid edits, and recovery (4.382723ms)
✔ loadPlanCaps without statSync reads through uncached (0.690926ms)
✔ noteFrontmatter resolves through getFileCache, not getCache (4.847897ms)
✔ task_refresh applies through the shared reader (39.414194ms)
✔ noteReadyKindFromType covers every R11 form (4.678113ms)
✔ noteReadyStatusLabel mirrors ProjectStatus::parse (0.605408ms)
✔ noteReadyParentStem strips alias, heading, and path (0.499768ms)
✔ parseNoteReadyCap covers every R8 form (4.214399ms)
✔ R1: 6 tasks at the default cap are crowded with over_by 1 (35.379017ms)
✔ R2: 5 tasks are full with no lint (10.622708ms)
✔ R3: hidden, future, blocked, and non-TODO rows never count (10.952525ms)
✔ R4: make-up splits 1 ready + 1 new + 1 rotten (7.595585ms)
✔ R5: recurring rows are excluded but tallied (11.103027ms)
✔ R6: a visible ^prj task never counts (6.262197ms)
✔ R7: daily, untyped, template, done, and dash rows are absent (14.515131ms)
✔ R8: ready_cap forms map to cap, exempt, or lint-then-default (18.343395ms)
✔ R9: a parent with two children counts 3 (6.894702ms)
✔ R10: terminal projects are not capped and lint once (12.473665ms)
✔ R11: every type form and nested folders are eligible (7.114441ms)
✔ R12: stamping a NEW task keeps the count and moves the make-up (38.161264ms)
✔ R13: a Today-linked task still counts (9.476386ms)
✔ R14: max_ready_per_note 3 caps others while ready_cap 8 holds (20.624417ms)
✔ api.noteReady is frozen at version 1 under api v3 (1.701715ms)
✔ counted and inCrowdedNote resolve per task (27.603417ms)
✔ groupLabel ranks crowded notes by excess (30.016902ms)
✔ snapshot sorts crowded, full, room, empty, exempt and splits totals (25.078524ms)
✔ missing Tasks data and a cold cache are unavailable, never zero (12.786527ms)
✔ throwing Tasks guards never throw (9.956884ms)
✔ snapshot reuses the memo without reparsing or re-walking (9.710046ms)
✔ a task edit rebuilds through the cache-update handler (11.540178ms)
✔ a ready_cap edit rebuilds and fires the query-refresh trigger (6.700271ms)
✔ rename and delete move the eligibility entry (11.154013ms)
✔ day rollover rebuilds the snapshot date (6.998444ms)
✔ a config edit flows through the stat cache (63.25786ms)
✔ untyped and non-markdown vault events are no-ops (22.087357ms)
✔ memo hits never re-walk the vault (200.889886ms)
✔ the startup storm is linear (57.348273ms)
✔ the first resolved event forces one rebuild and later ones do not (8.78819ms)
✔ noteReadyEvaluate is pure and mirrors the Rust totals (1.063221ms)
✔ OC: only exact ledger Task Link rows in canonical daily Pomodoros qualify (18.710559ms)
✔ OC10 and OC15: history is included and toggle-off is a CSS and JavaScript gate (6.028531ms)
✔ OV parity with the se<X> writer: unlinked-stays-on-the-clock (5.662746ms)
✔ OV parity with the se<X> writer: all-off-clock-non-meet (6.026359ms)
✔ OV parity with the se<X> writer: mixed-stays-on-the-clock (2.630113ms)
✔ OV parity with the se<X> writer: unresolved-stays-on-the-clock (0.739276ms)
✔ OV parity with the se<X> writer: alias-off-clock (0.663478ms)
✔ OV parity with the se<X> writer: nested-tag-rejected (1.475278ms)
✔ OV excluded: meet-run-ignores-future-off-clock-queue (0.982323ms)
✔ OV excluded: close-defers-not-started-off-clock (0.858295ms)
✔ OV excluded: close-mixed-after-dropping-on-clock (0.2136ms)
✔ OV excluded: kept-ledger-swap-switches-key (0.130623ms)
✔ OV excluded: bare-row-restamped-at-close (0.097815ms)
✔ OV excluded: conflict-row-at-close (0.107942ms)
✔ OV excluded: running-link-restamps (0.087744ms)
✔ OV parity with the se<X> writer: love-default-untagged-child-is-off-clock (2.333188ms)
✔ OV parity with the se<X> writer: event-task-root-abby-inherits-love (7.877359ms)
✔ OV parity with the se<X> writer: false-child-true-grandchild-is-off-clock (4.104947ms)
✔ OV parity with the se<X> writer: untyped-dog-passes-inheritance-through (0.666337ms)
✔ OV parity with the se<X> writer: on-tag-under-love-stays-worked (0.458752ms)
✔ OV parity with the se<X> writer: on-off-conflict-stays-worked (0.2358ms)
✔ OV parity with the se<X> writer: invalid-note-offclock-stays-worked (5.662664ms)
✔ OV parity with the se<X> writer: invalid-root-on-daily-stays-worked (1.111494ms)
✔ OV parity with the se<X> writer: love-plus-job-stays-worked-mixed (0.3994ms)
✔ OV parity with the se<X> writer: explicit-off-beats-false-child (0.387159ms)
✔ OV parity with the se<X> writer: type-list-meet-at-love-child-is-off-clock (3.334088ms)
✔ OV parity with the se<X> writer: type-list-chore-at-love-child-is-worked (0.57131ms)
✔ OV parity with the se<X> writer: type-list-meet-plus-chore-is-mixed (0.520209ms)
✔ OV parity with the se<X> writer: child-list-narrows-parent-true (0.454908ms)
✔ OV parity with the se<X> writer: child-false-under-parent-list-is-worked (4.198377ms)
✔ OV parity with the se<X> writer: dual-key-list-wins-without-capture-warning (0.536239ms)
✔ OV parity with the se<X> writer: scalar-type-list-is-one-item-list (0.277079ms)
✔ OV parity with the se<X> writer: empty-type-list-blank-inherits-true (0.403634ms)
✔ OV parity with the se<X> writer: empty-type-list-flow-empty-inherits-true (2.111469ms)
✔ OV parity with the se<X> writer: empty-type-list-null-inherits-true (1.813782ms)
✔ OV parity with the se<X> writer: empty-type-list-lone-dash-inherits-true (0.655436ms)
✔ OV parity with the se<X> writer: invalid-type-list-item-stays-worked (3.778986ms)
✔ OV parity with the se<X> writer: type-list-on-note-is-ignored (0.437068ms)
✔ OV parity with the se<X> writer: on-tag-on-meet-stays-worked (0.183924ms)
✔ OV parity with the se<X> writer: off-tag-on-chore-is-off-clock (0.28239ms)
✔ OV parity with the se<X> writer: meet-from-note-task-type-default-is-off-clock (3.312544ms)
✔ OV parity with the se<X> writer: closed-untyped-link-under-type-list-is-worked (1.059252ms)
✔ OV parity with the se<X> writer: chore-from-config-default-type-is-off-clock (0.666701ms)
✔ OV parity with the se<X> writer: reading-task-with-ref-block-is-off-clock (5.523102ms)
✔ OV parity with the se<X> writer: task-type-off-with-configured-default-is-off-clock (0.807321ms)
✔ OV exclusions account for every vector omitted from link-level parity (0.329348ms)
✔ OR/OT: target line facts select tagged and inherited clocks with canonical tooltip text (6.69145ms)
✔ OT and OP3: builder uses one listener-free accessible host with no title (0.650534ms)
✔ OP1, OP2, and OP4: widget placement is side 3, after other chips, and selection-only updates do not rebuild (1.860648ms)
✔ OP1/interaction: plain mousedown restores the caret; Mod-click opens the task (0.923386ms)
✔ writer delegation and metadata-cache freshness preserve path-aware resolution (1.755377ms)
✔ toggle refreshes both surfaces and the Reading context allow-list recognizes the chip (0.777808ms)
✔ setup registers the default-on command, Live Preview extension, Reading processor, and source listeners (1.489958ms)
✔ 200-link / 50-target Live Preview build memoizes targets and stays near the 25 ms budget (16.704985ms)
✔ Reading sweep handles closed daily ledger rows and reconciles the chip after its anchor (2.532245ms)
✔ Event Task CSS keeps one shared chip appearance while link chips are independent (3.144589ms)
✔ week note paths follow the ISO week-year golden facts (24.918199ms)
✔ ensure argv, adoption path, and timing constants match the contract (0.570717ms)
✔ adoption gate keeps ensure inert without all_time.md (0.987461ms)
✔ create trigger reuses the daily-note file test and fires once per path (57.326874ms)
✔ create trigger shares the gcal file test (1.650205ms)
✔ layout-ready and midnight ticks share one once-per-day slot (21.636777ms)
✔ decode maps ensure JSON and failure shapes (1.655257ms)
✔ older bob warns once per session and never notices (0.625578ms)
✔ lock_busy retries once, then surfaces the second outcome (7.244212ms)
✔ other failures notice once per local day (1.255011ms)
✔ open-this-weeks-note honors the gate and the missing note (4.358452ms)
✔ setup registers the open-week command and teardown clears the retry timer (0.595022ms)
✔ period paths map to the date bob periods ensure -d needs (0.671419ms)
✔ unfilled period notes are blank or a frontmatter-only Templater stub (0.422758ms)
✔ a stubbed period note is filled once through ensure -d; bob scaffolds never cascade (43.580749ms)
✔ api.periodNotes.ensureNote creates a missing period note through bob, never a template (4.077812ms)
✔ the midnight ticker starts only on hosts that can register it (0.500576ms)
✔ quarter parts render week columns, month ticks, review marks, and future ghosts (16.127006ms)
✔ year parts group 53 weeks by quarter and keep a four-quarter narrow fallback (6.727288ms)
✔ all-time parts group quarters by year and keep year captions (4.27954ms)
✔ parts table uses live internal links, Headline or mostly, review states, and day closeout rows (5.003341ms)
✔ table future rows stop at Child and Dates; not-tracked years and missing pre-adoption links are clear (2.415725ms)
✔ shared report command remains keyed once by the period id (0.353027ms)
✔ period ids classify week, quarter, year, all time, day, and junk (11.927342ms)
✔ fence parsing selects period, day, or the muted line (1.6038ms)
✔ week model maps bob facts with typical marks only when closed (21.37421ms)
✔ week meta covers open, closed gaps, and future (3.170856ms)
✔ lanes and columns share one hue per root (1.161019ms)
✔ week columns carry closed, current, future, and missing states (1.431756ms)
✔ states: skeleton, unavailable, older-bob, and hidden (1.219097ms)
✔ paint renders facts, lanes, and the seven-day parts row with no buttons (9.649732ms)
✔ parts row is one roving-tabindex group with tooltips (10.55791ms)
✔ clicks reach the day note and Stats hand-offs, never a spawn on future (13.878868ms)
✔ period show args are one audited call per period (0.514278ms)
✔ onload registers the bob-stats-strip and bob-period-parts fences (33.892515ms)
✔ period-note fences fetch once per period and paint the strip and the parts table (55.987465ms)
✔ plan off-clock vectors: tag-off-link-uncapped (14.145352ms)
✔ plan off-clock vectors: alias-off-link-uncapped (2.276056ms)
✔ plan off-clock vectors: note-default-off (3.149798ms)
✔ plan off-clock vectors: on-overrides-note-default (0.81254ms)
✔ plan off-clock vectors: root-field-inherits-off (2.951578ms)
✔ plan off-clock vectors: event-task-same-note (2.484513ms)
✔ plan off-clock vectors: unresolved-stays-counted (1.004831ms)
✔ plan off-clock vectors: mixed-session-counts-only-on-clock (0.721515ms)
✔ plan off-clock vectors: off-clock-never-over (0.951611ms)
✔ plan off-clock vectors: on-clock-still-over (1.076909ms)
✔ plan off-clock vectors: dedupe-across-entries (0.884587ms)
✔ plan off-clock vectors: exempt-entry-unchanged (0.592255ms)
✔ plan off-clock vectors: done-off-clock-task (1.678834ms)
✔ plan budget predicate honors shared clock config: type-list-meet-at-love-child-is-off-clock (4.096619ms)
✔ plan budget predicate honors shared clock config: type-list-chore-at-love-child-is-worked (1.519125ms)
✔ plan budget predicate honors shared clock config: type-list-meet-plus-chore-is-mixed (1.208979ms)
✔ plan budget predicate honors shared clock config: child-list-narrows-parent-true (1.883584ms)
✔ plan budget predicate honors shared clock config: child-false-under-parent-list-is-worked (0.811067ms)
✔ plan budget predicate honors shared clock config: dual-key-list-wins-without-capture-warning (0.512476ms)
✔ plan budget predicate honors shared clock config: scalar-type-list-is-one-item-list (0.401422ms)
✔ plan budget predicate honors shared clock config: empty-type-list-blank-inherits-true (0.426354ms)
✔ plan budget predicate honors shared clock config: empty-type-list-flow-empty-inherits-true (0.436954ms)
✔ plan budget predicate honors shared clock config: empty-type-list-null-inherits-true (0.373846ms)
✔ plan budget predicate honors shared clock config: empty-type-list-lone-dash-inherits-true (0.563925ms)
✔ plan budget predicate honors shared clock config: invalid-type-list-item-stays-worked (0.384818ms)
✔ plan budget predicate honors shared clock config: type-list-on-note-is-ignored (0.357706ms)
✔ plan budget predicate honors shared clock config: on-tag-on-meet-stays-worked (0.21379ms)
✔ plan budget predicate honors shared clock config: off-tag-on-chore-is-off-clock (0.250831ms)
✔ plan budget predicate honors shared clock config: meet-from-note-task-type-default-is-off-clock (2.883515ms)
✔ plan budget predicate honors shared clock config: closed-untyped-link-under-type-list-is-worked (1.154437ms)
✔ plan budget predicate honors shared clock config: chore-from-config-default-type-is-off-clock (0.910805ms)
✔ plan budget predicate honors shared clock config: reading-task-with-ref-block-is-off-clock (0.737821ms)
✔ plan budget predicate honors shared clock config: task-type-off-with-configured-default-is-off-clock (1.036679ms)
✔ conformance: merged name with duplicate (18.421316ms)
✔ conformance: link forms and exclusions (1.383811ms)
✔ conformance: unnamed placeholders (3.919764ms)
✔ plan block mirrors Bob's unconfigured-theme lint and suppresses it without a vocabulary (8.477359ms)
✔ conformance: subheading in the section (0.683541ms)
✔ conformance: open inventory label (0.559353ms)
✔ conformance: many types do not put the plan over budget (3.830374ms)
✔ conformance: cancelled and completed entries (0.551524ms)
✔ type count does not affect budget status (0.478863ms)
✔ no Pomodoros section degrades to an empty budget (0.713786ms)
✔ fenced code never counts (3.686312ms)
✔ highlight is the first open non-exempt entry; running is the timed one (0.896117ms)
✔ coercePlanCaps ignores retired plan keys instead of failing (0.738726ms)
✔ parsePlanCaps defaults, overrides, and invalid fallbacks (0.64973ms)
✔ reading theme config defaults to READ, accepts off, and rejects invalid values (3.637802ms)
✔ reading_type is canonical with reading_theme as the legacy alias (0.527824ms)
✔ default_type config stays null without a name and rejects invalid values (0.41946ms)
✔ loadPlanCaps falls back to defaults without fs (5.264246ms)
✔ loadPlanCaps falls back to defaults on mobile (0.515674ms)
✔ loadPlanCaps reads plan: and flags invalid values (1.00222ms)
✔ planBlockTargetPath prefers the containing daily note (0.640385ms)
✔ planBlockModel degrades to placeholders, never an error (0.455814ms)
✔ planBlockModel renders chips, themes, and lints (9.484651ms)
✔ planBlockModel adds lane cap lints when a lane is over (1.719923ms)
✔ plugin exposes the versioned api and registers the bob-plan block (50.453195ms)
✔ invalid plan block falls back to full defaults (0.393011ms)
✔ entries require column-0 dash-space with one status char (3.539629ms)
✔ crlf line endings split like lf (0.501459ms)
✔ conformance: empty target means the daily note (0.372646ms)
✔ lane predicate matches hide subtags, case, and non-task (0.477932ms)
✔ planBlockModel daily badges follow dashboard section counts (15.7327ms)
✔ planBlockModel keeps a supplied unavailable dashboard budget (0.890477ms)
✔ work tones: TODAY override and unavailable stay neutral in planBlockModel (7.399578ms)
✔ plan budget off-clock: pure option semantics (1.249622ms)
✔ planBlockModel tooltip names off-clock links (5.507547ms)
✔ api.planBudget budgets content with the off-clock predicate (0.896132ms)
✔ today_roots vector: counts-and-tie-order (24.985352ms)
✔ today_roots vector: root-fields-win (11.107673ms)
✔ today_roots vector: root-true-and-subprojects (4.359639ms)
✔ today_roots vector: archive-and-ref-notes (3.690103ms)
✔ today_roots vector: open-statuses-only (1.595175ms)
✔ today_roots vector: exempt-and-unnamed-entries-count (1.226195ms)
✔ today_roots vector: dead-links-do-not-count (1.089892ms)
✔ today_roots vector: duplicate-links-count-once (0.996775ms)
✔ today_roots vector: unfiled-is-always-last (4.504052ms)
✔ today_roots vector: area-hues (1.619768ms)
✔ today_roots vector: no-section-is-empty (0.584651ms)
✔ today_roots vector: empty-section-is-empty (0.46149ms)
✔ planTodayRoots returns null when Tasks is unavailable (0.279912ms)
✔ planTodayRoots never throws on garbage input (0.304633ms)
✔ planBlockModel todayRoots is empty without a Pomodoros section (5.294674ms)
✔ planBlockModel todayRoots is null when Tasks is unavailable (3.39589ms)
✔ paintPlanTodayRoots paints hue, counts, unfiled, aria, and click (2.038403ms)
✔ paintPlanTodayRoots paints no line when roots are empty (0.248049ms)
✔ shared vector: unlinked-stays-on-the-clock (28.270696ms)
✔ shared vector: all-off-clock-non-meet (8.453518ms)
✔ shared vector: mixed-stays-on-the-clock (2.798686ms)
✔ shared vector: unresolved-stays-on-the-clock (1.217691ms)
✔ shared vector: alias-off-clock (3.053573ms)
✔ shared vector: nested-tag-rejected (0.980414ms)
✔ shared vector: meet-run-ignores-future-off-clock-queue (7.882939ms)
✔ shared vector (elsewhere): close-defers-not-started-off-clock (3.394862ms)
✔ shared vector (elsewhere): close-mixed-after-dropping-on-clock (0.381503ms)
✔ shared vector (elsewhere): kept-ledger-swap-switches-key (0.520569ms)
✔ shared vector (elsewhere): bare-row-restamped-at-close (0.252497ms)
✔ shared vector (elsewhere): conflict-row-at-close (0.157949ms)
✔ shared vector (elsewhere): running-link-restamps (0.08425ms)
✔ shared vector: love-default-untagged-child-is-off-clock (5.136514ms)
✔ shared vector: event-task-root-abby-inherits-love (11.59698ms)
✔ shared vector: false-child-true-grandchild-is-off-clock (0.986108ms)
✔ shared vector: untyped-dog-passes-inheritance-through (8.216943ms)
✔ shared vector: on-tag-under-love-stays-worked (0.631439ms)
✔ shared vector: on-off-conflict-stays-worked (0.425271ms)
✔ shared vector: invalid-note-offclock-stays-worked (0.59904ms)
✔ shared vector: invalid-root-on-daily-stays-worked (1.383472ms)
✔ shared vector: love-plus-job-stays-worked-mixed (0.609144ms)
✔ shared vector: explicit-off-beats-false-child (0.549231ms)
✔ shared vector: type-list-meet-at-love-child-is-off-clock (6.14998ms)
✔ shared vector: type-list-chore-at-love-child-is-worked (3.638538ms)
✔ shared vector: type-list-meet-plus-chore-is-mixed (2.224261ms)
✔ shared vector: child-list-narrows-parent-true (0.667827ms)
✔ shared vector: child-false-under-parent-list-is-worked (0.454121ms)
✔ shared vector: dual-key-list-wins-without-capture-warning (4.666125ms)
✔ shared vector: scalar-type-list-is-one-item-list (0.548581ms)
✔ shared vector: empty-type-list-blank-inherits-true (0.4606ms)
✔ shared vector: empty-type-list-flow-empty-inherits-true (0.451068ms)
✔ shared vector: empty-type-list-null-inherits-true (0.449317ms)
✔ shared vector: empty-type-list-lone-dash-inherits-true (0.599381ms)
✔ shared vector: invalid-type-list-item-stays-worked (0.473851ms)
✔ shared vector: type-list-on-note-is-ignored (3.610926ms)
✔ shared vector: on-tag-on-meet-stays-worked (0.264982ms)
✔ shared vector: off-tag-on-chore-is-off-clock (3.508007ms)
✔ shared vector: meet-from-note-task-type-default-is-off-clock (6.135975ms)
✔ shared vector: closed-untyped-link-under-type-list-is-worked (1.302764ms)
✔ shared vector: chore-from-config-default-type-is-off-clock (0.731767ms)
✔ shared vector: reading-task-with-ref-block-is-off-clock (0.624405ms)
✔ shared vector: task-type-off-with-configured-default-is-off-clock (2.347127ms)
✔ every vector is either mirrored here or listed as handled elsewhere (0.472606ms)
✔ closed tasks use their own line type without changing the closed suggestion result (3.149375ms)
✔ offclock_types follows the empty, scalar, list, and invalid YAML value rules (0.71725ms)
✔ an invalid type-list warning names offclock_types (0.741303ms)
✔ the verdict needs a resolved, nonempty, all-off-clock lineup (0.297551ms)
✔ counted links are the direct-child dedicated bullets: plain, struck, marked, or embedded (0.533242ms)
✔ the lineup clock reads same-note tasks and Event Tasks, and resolves other notes through the callback (2.686158ms)
✔ a MEET with no event run takes the clock of its whole lineup (0.548315ms)
✔ a counted suffix keeps its span and still takes the lineup clock (0.343811ms)
✔ taskEffectiveOffClock inherits offclock: from the nearest area or project (0.898629ms)
✔ taskEffectiveOffClock follows [root::] off a daily note (0.953165ms)
✔ #on wins over #off and #off does not match #offclock (3.506238ms)
✔ shared vector: subproject-archive-homes (16.589235ms)
✔ shared vector: session-names-never-home (10.589511ms)
✔ shared vector: named-sessions-use-task-homes (2.243241ms)
✔ shared vector: resolution-and-lints (2.967127ms)
✔ shared vector: chips, forecast shares, empty forecasts, and session identity (1.990518ms)
✔ shared vector: split-rounding-and-duration (1.066713ms)
✔ shared vector: off-clock-real-minutes (0.656667ms)
✔ shared vector: off-clock-bare-span (3.850835ms)
✔ shared vector: clock-conflict-worked (0.773265ms)
✔ shared vector: share-rounding (2.810903ms)
✔ shared vector: gtd-root-across-days (1.196507ms)
✔ shared vector: depth-and-parent-shapes (1.676155ms)
✔ shared vector: unresolved-and-closed-zero (1.060692ms)
✔ shared vector: parent-scalar-shapes (0.66868ms)
✔ shared vector: daily-note-task-home (0.529757ms)
✔ shared vector: root-fields (5.474232ms)
✔ shared vector: root-parent-chips (1.711836ms)
✔ root-fields keeps home state, root, and hue in parity with root marks (7.959654ms)
✔ home chips refresh after a linked task source read supplies its root field (25.408295ms)
✔ dedicated link parser keeps embeds and one struck link, but rejects prose (0.523183ms)
✔ FNV-1a fallback for job maps to the pinned magenta slot (0.2101ms)
✔ area-color lints are reported once per note (1.152752ms)
✔ a leftover rollup key neither regroups nor warns (0.749257ms)
✔ chip DOM exposes forecast, hue, accessible text, and tooltip (0.626414ms)
✔ Reading view appends a forecast chip before its Task Link list (11.785628ms)
✔ Live Preview places a chip widget at the end of the Pomodoro line (1.500305ms)
✔ Live Preview skips chips in Source mode (0.40263ms)
✔ Reading view finds embedded Task Links via src (1.122742ms)
✔ Obsidian frontmatter shapes unwrap nested wikilink arrays (0.384256ms)
✔ the root flag accepts a boolean true or a string that trims to true (0.438731ms)
✔ the tooltip has one line per root parent in label order; parts stay per home (2.093953ms)
✔ a session linking a project and its sub-project reads as the root parent only (1.57001ms)
✔ root marks and chips resolve the same root parent (2.218079ms)
✔ an Off-Clock Pomodoro's home model carries its real minutes and an off-the-clock tooltip (2.107138ms)
✔ an off-clock chip shows its minutes only when they are recorded (0.589338ms)
✔ Reading view rebuilds Dataview inline fields and flags only an explicit [off::] (0.863534ms)
✔ root and Ledger Tools vector copies stay byte-identical (4.103897ms)
✔ theme vectors: components split and key like bob (2.491702ms)
✔ theme vectors: hue rule includes configured colors and unconfigured mute (4.172431ms)
✔ theme vectors: journal fold is last writer wins with rename moves (1.763736ms)
✔ theme vectors: history rank is exact, prefix, then substring (2.092712ms)
✔ theme hash hues match the known collisions (0.284632ms)
✔ theme similar keys follow the near-duplicate rule (0.972426ms)
✔ theme decode accepts a schema 1 report and rejects the rest (4.460024ms)
✔ theme decode keeps configured vocabulary and row flags (0.713139ms)
✔ themes API reports vocabulary membership and returns null without a configured block (1.021402ms)
✔ themes API Recent rows include configured never-used names in config order and omit strays (3.522845ms)
✔ theme write decode maps refusals and pre-writer bob output (0.515262ms)
✔ theme components carry byte offsets excluding quotes and plus (0.380309ms)
✔ theme pill models mark exempt components muted (0.357725ms)
✔ theme pill models mark unconfigured components muted and outlined (0.30118ms)
✔ Live Preview waits until the cursor leaves an unconfigured theme name (3.111738ms)
✔ theme name offsets anchor at the em dash of a ledger line (0.658745ms)
✔ theme fixture preserves preselect vectors from bob-cli (0.201853ms)
✔ theme task-field vectors execute parse, byte-preserving setters, and clear (6.599492ms)
✔ type vectors: agreement answers the D5 invariant (1.359332ms)
✔ type vectors: landing mirrors the R2 merge/retype rule (8.145212ms)
✔ type vectors: merged names dedupe components in first-spelling order (0.49163ms)
✔ type vectors: shed removes only types whose final link left (0.650795ms)
✔ type vectors: close narrows to worked types while preserving labels and order (0.568788ms)
✔ type vectors: split partitions a merged Pomodoro by type (6.633768ms)
✔ type vectors: placement picks the Pomodoro for a type (1.041942ms)
✔ type vectors: relocation moves the live link with a type (1.275313ms)
✔ theme suggestion vectors execute Rust precedence, origins, diagnostics, and live names (16.338793ms)
✔ task-theme API is additive, synchronous, path-bound, and read-only (5.563327ms)
✔ note defaults read task_type first with a conflict warning (0.518996ms)
✔ suggestion cascade falls through to plan.default_type (1.201126ms)
✔ themes routing API answers agreement, landing, merge, shed, placement, and relocation (3.193503ms)
✔ effectiveTypeFor runs the suggest cascade for a task line (2.099577ms)
✔ muted exempt pill is gray while unconfigured stays transparent (2.129007ms)
✔ parser accepts the PM1-PM5 conformance vectors verbatim (4.748693ms)
✔ parser rejects the PM7-PM12 conformance vectors verbatim (0.672817ms)
✔ PM6 with the ladder unknown omits P-labels instead of guessing (0.352567ms)
✔ PM13-PM17 ladder and line variants hold (0.677506ms)
✔ no model output contains a double colon (2.176347ms)
✔ element structure and the decorative/inheritColor options (6.249456ms)
✔ Live Preview decorations fold space, reveal, and refuse (10.699529ms)
✔ a line with fresh and priority fields gets a disjoint decoration (1.400536ms)
✔ PM18/PM19 digit rows fold only while block marks are on (3.167265ms)
✔ widget mousedown reveals the field at the folded offset (2.01053ms)
✔ rendered views split task nodes and skip exclusions (2.327268ms)
✔ ladder coercion is lenient: valid, partial, and unknown (4.501174ms)
✔ ladder snapshot reads the file and reuses the cache (2.893296ms)
✔ ladder snapshot degrades on missing files and parse errors (1.593174ms)
✔ ladder snapshot is unknown on mobile (85.236325ms)
✔ api.priorityMarks v1 is additive, sync, and never throwing (25.518523ms)
✔ session toggle and onload wiring (3.604985ms)
✔ styles.css contract: masks, both hosts, repair flag, resting (2.688156ms)
✔ mark gate holds in popout windows for both toggle states (1.302034ms)
✔ P1/P3/P4: open entries mark plain and aliased links (7.871757ms)
✔ P2/P12: Next, Ready, Blocked, done, and cancelled targets get no mark (5.177925ms)
✔ P5: closed entries never mark, even with 🍅 history (2.55213ms)
✔ P6/P7: embedded and struck links never mark (0.547875ms)
✔ P8: both trailing-# move-only forms mark (0.677041ms)
✔ P9: nested and prose-mixed links never mark (0.369834ms)
✔ P10: fenced, off-section, and off-note links never mark (1.208047ms)
✔ P11: unresolved targets and non-task blocks get no mark (2.695046ms)
✔ P13: a same-note target reads the live doc (1.972528ms)
✔ P14: expect() wins until the cache agrees or 4 s pass (2.678553ms)
✔ tooltip, element structure, and eq (1.123411ms)
✔ Live Preview places one widget at each In Progress link (2.136636ms)
✔ widget mousedown places the cursor at the link start (4.412039ms)
✔ rebuild triggers skip the cursor but take doc, viewport, and refresh (1.708834ms)
✔ Reading view marks In Progress rows and dedupes (4.3851ms)
✔ Reading view refuses every non-mark row (9.160341ms)
✔ Reading view allows the 🍅 prefix and the trailing # marker (0.796105ms)
✔ Reading context ignores display-only ledger marks and one wrapping p (2.46156ms)
✔ api.progressMarks v1 is additive, sync, and never throwing (2.932587ms)
✔ session toggle, onload wiring, and refresh fan-out (4.819622ms)
✔ mark gate holds in popout windows for both toggle states (1.459907ms)
✔ changed-file and rollover refreshes (1.819491ms)
✔ the refresh effect stays lazy: one eager define (0.238897ms)
✔ styles.css contract: glyph, box, motion, toggle, calm (2.830673ms)
✔ the board registers its code block processor and the Open Reading Board command (84.313232ms)
✔ four lanes render with counts, list and listitem roles, and one hint (48.527293ms)
✔ awake cards show kind, topic, added mark, counts, priority, and the pending-sync star (10.860033ms)
✔ a path-valued Bob audio field produces exactly one visible music marker (11.30406ms)
✔ Snoozed shows Waking, date groups, and Waiting-on rows with their reasons (13.662494ms)
✔ TODAY pills float linked cards first, and never appear without a ready Today cache (21.927109ms)
✔ the PDF button needs the nav member, macOS, and a source_pdf (43.290876ms)
✔ click, modifier-click, middle-click, and the Task button route to openLinkText (6.388534ms)
✔ the board is one Tab stop and every key moves or acts (57.227569ms)
✔ movement targets stay inside the lanes that show cards (0.910657ms)
✔ hovering a Waiting-on row outlines its prerequisite card on the board (6.593818ms)
✔ the board never calls a vault write API, in the source or in any gesture (25.352923ms)
✔ a repaint keeps focus by note path and each lane's scroll position (13.528989ms)
✔ a task move and topic/type update repaint handlers while preserving focus and scroll (14.572832ms)
✔ prerequisite identity changes repaint highlighting even when reason text is unchanged (14.267695ms)
✔ an unchanged board is not repainted; only the data time updates in place (8.861864ms)
✔ a Today cache change repaints boards from cached data without spawning bob (17.3136ms)
✔ first paint is a skeleton in the real grid, then the board without a layout jump (10.617817ms)
✔ failures without a frame render an actionable card with Retry (63.852345ms)
✔ a failed manual refresh keeps the last frame and says why with Retry (22.714148ms)
✔ metadata revalidation delivers a silent stale-frame error and recovery updates freshness (43.573019ms)
✔ stale-cache mount refresh failures reach the mounted view (14.316304ms)
✔ unload during a fetch prevents late repaint and queued spawns (7.968345ms)
✔ in-flight edits and forced refreshes coalesce without dropping mounted fences (36.582728ms)
✔ manual refresh shows a busy state until the result lands, then announces it (8.769246ms)
✔ an older bob without blocked_by falls back to Waiting-on with one lint line (7.759584ms)
✔ an empty queue shows bob's own phrase instead of lanes (4.044923ms)
✔ fence options reach the fetch and bad options show as muted lint lines (11.201647ms)
✔ Snoozed collapses per source path, leaves the key order, and survives repaints (25.99527ms)
✔ unloading a block releases its view, and teardown clears the session state (6.012996ms)
✔ reading board stylesheet contract: selectors, layout, tabular-nums, motion, colors (3.808493ms)
✔ Reading Board argv carries bob's fixed queue and optional fence filters (3.584587ms)
✔ Reading Board decoder accepts the shared bob fixture and normalizes optional fields (0.569453ms)
✔ Reading Board audio presence survives raw JSON decoding and model construction (10.256006ms)
✔ Reading Board decoder rejects malformed JSON, shapes, schema, and bob errors (0.733047ms)
✔ shared bob spawn passes the vault environment, timeout, and buffer (24.397101ms)
✔ shared bob spawn maps missing binary and timeout failures (6.050202ms)
✔ Reading Board error cards explain not-found, timeout, schema, and bob errors (0.964755ms)
✔ Reading Board cache returns stale data while revalidating and keeps a four-entry LRU (8.612718ms)
✔ Reading Board shares identical flights and coalesces one different follow-up (4.398829ms)
✔ Reading Board refresh is mounted-only, debounced, and reacts to rollover and stale active leaves (1.339383ms)
✔ the shared bob output builds the expected four lanes and preserves bob order (10.46563ms)
✔ each status uses its awake lane and every blocked status uses Snoozed (1.142257ms)
✔ Today floats cards by ledger rank only when the cache is ready (2.690904ms)
✔ Snoozed groups show waking, schedule, dependency, project, return lane, and mark models (1.702528ms)
✔ schedule groups follow Monday-start weeks through Sunday across month and year ends (0.638394ms)
✔ older bob output remains visible in Waiting on and explains the missing reasons (2.25875ms)
✔ fence options accept parent and type lists while turning bad input into lints (3.151146ms)
✔ kind names, title code spans, and render signatures are deterministic (6.740645ms)
✔ max_ready defaults to 100 for missing, absent, and null values (6.542296ms)
✔ max_ready accepts a custom positive cap (0.673392ms)
✔ max_ready rejects zero, negative, fractions, strings, booleans, and overflow (2.182671ms)
✔ old configurations and legacy max_now still load (0.432119ms)
✔ READY boundary: only a strict excess turns red (4.620269ms)
✔ READY custom-cap boundary (0.716052ms)
✔ READY over is independent of type count and the PLAN ledger status (15.554569ms)
✔ READY predicate: statuses, custom TODO symbols, and non-tasks (1.003223ms)
✔ READY predicate: blocked uses the full list, even outside the queue (1.046515ms)
✔ READY predicate: past, today, and future schedules (1.525154ms)
✔ READY predicate: dash self-exclusion, daily files, templates, conflicts, hide (0.916832ms)
✔ READY predicate: Today exclusion (3.75926ms)
✔ readyTaskVisible excludes hide variants like Tasks (0.378909ms)
✔ daily and dashboard share the READY element contract (37.244267ms)
✔ READY placeholder keeps the limit in its tooltip (0.318475ms)
✔ READY keyboard and modifier-key navigation (3.33762ms)
✔ READY unavailable without Tasks, on Cold/Initializing, or before Today (9.117943ms)
✔ READY counts a valid empty queue as zero, not unavailable (2.674352ms)
✔ READY stays compatible with hosts exposing only getTasks() (4.072414ms)
✔ READY degrades to unavailable when the Today predicate throws (1.279054ms)
✔ READY renders label/value spans for every budget state (8.435109ms)
✔ READY live refresh keeps the anchor, spans, and handlers (3.923506ms)
✔ READY refresh crosses the over-cap boundary and back (2.167655ms)
✔ READY refresh crosses the unavailable boundary and back (1.758431ms)
✔ READY never assigns the Obsidian text setter (3.019945ms)
✔ READY gating excludes review buckets and keeps the partition (0.677915ms)
✔ gated READY tooltip carries total lane pressure (0.259293ms)
✔ planBlockModel gates READY and shares the lane tooltip (1.218522ms)
✔ READY lint appears only on a strict excess (6.671479ms)
✔ READY lint uses a custom cap (1.039897ms)
✔ lane lints appear in NEXT, PENDING, READY order (4.508237ms)
✔ READY lint uses the gated count (4.377775ms)
✔ READY lint stays silent while unavailable (1.487656ms)
✔ READY speaks each host's chip language (daily single-tone, dash two-tone) (11.83451ms)
✔ daily paint carries lane pressure to the shared READY renderer (102.768732ms)
✔ daily paint degrades to the legacy tooltip without freshness (26.32599ms)
✔ work tones: READY model carries the displayed-count tone (5.0604ms)
✔ recurrence helpers are exported and frozen where shaped (5.469944ms)
✔ RM1 daily with when done: fold, label, tooltip (3.16455ms)
✔ RM2 non-checklist row without when done still marks (1.992114ms)
✔ RM3 weekday plurals keep the full name (1.159486ms)
✔ RM4 monthly ordinals use the written token (0.936195ms)
✔ RM5 every N days stays verbatim with its count (0.407623ms)
✔ RM6 weekly, N-week, and yearly forms (1.125413ms)
✔ RM7 week lists join with Tue, Fri and weekday alone (0.585255ms)
✔ RM8 unknown rules stay verbatim (1.127603ms)
✔ RM9 parens and padded brackets are canonical (1.281412ms)
✔ RM10 case is preserved in the rule and tooltip (1.915796ms)
✔ RM11 cursor in the field reveals it, RM12 closed rows still mark (0.731458ms)
✔ RN1 unreadable rules get no mark (2.206101ms)
✔ RN2 the checklist guard follows membership, not the glyph slot (0.557421ms)
✔ RN3 code still parses pure but decorates nothing (0.778478ms)
✔ element anatomy: repeat host, rule, quiet tone, no date (1.46783ms)
✔ family dispatch keeps dates working and sorts adds (1.937377ms)
✔ Live Preview decorates repeat and respects the guard and code (2.379203ms)
✔ RR1 reading view honors the guard, RO2 rollover skips repeat (6.4429ms)
✔ RA1 api.dateMarks stays dates-only and tooltips never contain :: (1.219652ms)
✔ styles.css contract: repeat glyph, ink, resting, repair flag (2.41223ms)
✔ LC1 one unlabelled open target renders links-to arrow chip (6.608619ms)
✔ LC2 labelled target carries a pill (1.275219ms)
✔ LC3 closed and archived targets dim without strike; #hide mutes (5.052849ms)
✔ LC4 unresolvable target is a dashed missing chip (1.025351ms)
✔ LC5 LINKED FROM shows the derived inverse phrase (11.134503ms)
✔ LC6 LINKED FROM with an unknown label reads chip, label, this (0.940298ms)
✔ LC7 live edges missing from the text append in canonical order (1.049125ms)
✔ LC8 stored entries that are no longer live are dashed and uncounted (0.717972ms)
✔ LC9 three or more closed chips collapse to ✓×N and expand (2.095115ms)
✔ LC10 labelled rows wrap one entry per visual row (1.636015ms)
✔ LC11 controls need api.relations v1; linked_from_remove calls removeLink(S, T) (2.876504ms)
✔ LC12 toggle-dependency-chips covers both relation rows (1.561545ms)
✔ LC13 malformed and not-a-line rows have no model (0.432893ms)
✔ LC14 unsaved editor text refreshes the live model (37.626485ms)
✔ Live Preview decorates relation rows from the index (9.243707ms)
✔ Reading view decorates stored anchors and appends live edges (7.577723ms)
✔ Reading view groups mention rows, renders the quote, omits ×, and jumps to the source occurrence (23.750377ms)
✔ mention card hover waits, and moving the pointer onto the card keeps it open (924.293126ms)
✔ Reading view hides only host-note embedded mentions inside a transclusion (12.704214ms)
✔ Reading view with api.relations v1 shows ＋ and × (9.290232ms)
✔ MN row model separates relations and mentions, marks mixed pairs, and quotes the first prose occurrence (2.156178ms)
✔ MN quote rules omit title/embed excerpts and fit Unicode around the highlighted token (0.637546ms)
✔ MN stale mention rows keep the mention-specific dashed tooltip (0.714131ms)
✔ MN seven open mentions collapse after five and expand with +N more (3.678056ms)
✔ MN linkedFrom v2 feeds mention rows and relationIndex v1 remains a fallback (1.890191ms)
✔ SA22 LINKED FROM renders the starts-after display inverse (0.380131ms)
✔ MN click opens the source at its occurrence line and column, with Mod-click using a new pane (16.504088ms)
✔ ledger parser agrees with shared LK vectors and parses source task children (14.691814ms)
✔ relationIndex scans done sources, resolves both directions, and orders label suggestions (25.576021ms)
✔ relationIndex applies changed, delete, rename, and unsaved editor overlays (24.71144ms)
✔ relationIndex registers after layout-ready and never reads non-markdown during startup replay (62.091522ms)
✔ relationIndex ignores non-markdown live events (31.657279ms)
✔ relationIndex layout-ready after unload registers nothing (32.761014ms)
✔ parseTaskRelationFile indexes every checkbox status as a task (1.370289ms)
✔ relationIndex incoming and suggestions include Next and Blocked sources (7.336587ms)
✔ relation-label JS mirrors match the shared bob-cli vectors (9.090594ms)
✔ api.relationLabels reads folded preferences and delegates desktop writes to bob (2.703152ms)
{"relation_index_storm":{"events":40,"uncoalesced_publish_ms":117.47,"coalesced_event_stack_ms":5.31,"coalesced_turn_ms":8.11,"publishes":1,"memo_builds":1}}
✔ relationIndex coalesces a metadata storm to one publish and one task memo (158.087209ms)
✔ relationIndex v1 reads flush a pending publish (8.45956ms)
✔ task_mentions fixture copies byte-for-byte and carries version 1 (16.905598ms)
✔ mention scanner agrees with every shared MN vector (MN22 on the JS side) (51.031024ms)
✔ mention scanner reports UTF-16 columns past Unicode (MN22) (0.587429ms)
✔ reserved 💬 labels are refused (MN15) and LINKED FROM mentions are typed (MN16) (0.553576ms)
✔ relationIndex v2 keeps incoming/outgoing relations-only with typed linkedFrom (33.786629ms)
✔ relationIndex publishes mention rows and omits dependency-joined pairs (M7) (117.328285ms)
✔ relationIndex overlay updates mention rows from unsaved editor text (3.867562ms)
✔ scanMentions returns resolved pairs when on and [] when off (10.233325ms)
✔ ledger LK1–LK19 recognises relation shapes and keeps them out of plan links (5.206871ms)
✔ root field state and the hue-dot model cover set, compact, roll-up, and repair (18.511198ms)
✔ root mark element exposes the accessible state and compact DOM shape (1.873529ms)
✔ Live Preview replaces the field, respects selection reveal, and the session toggle is wired (8.131773ms)
✔ Reading and Tasks rows wrap root text without losing it and restore on unload (8.461111ms)
✔ the root-mark stylesheet has light/dark, state, and gate rules (5.916083ms)
✔ parseTrigger parses D[-]<N> dated-entry triggers with offset and span (5.72196ms)
✔ computeSnippetExpansion formats D[-]<N> with markdown emphasis, em dash, trailing space, and cursor offset (1.378165ms)
✔ expandLineAtCursor expands D[-]<N> in place and places cursor at the terminal stop without $1 notation (1.14597ms)
✔ findExpansion and parseTrigger reject bare, malformed, and identifier-embedded D triggers (1.126548ms)
✔ compatibility: existing snippets remain unchanged and uppercase T/DT remain unsupported (0.559871ms)
✔ parseEmDashTrigger parses exact `-` at column zero and after prose with exact spans (0.344002ms)
✔ computeSnippetExpansion computes exactly one U+2014 plus trailing U+0020 replacement for emDash triggers (0.362371ms)
✔ findExpansion/expandLineAtCursor expand `-` in whole-line and inline positions, preserving prefix/suffix (0.434893ms)
✔ findExpansion refuses `--`, `---`, and longer hyphen runs at the end or between hyphens (3.615861ms)
✔ expandFromEditor replaces exactly the `-` trigger, sets cursor after it, and returns true (1.317379ms)
✔ regression: existing snippet triggers still parse/expand unchanged alongside the new emDash trigger (0.865048ms)
✔ expandFromEditor replaces D0 trigger in editor and sets cursor to trailing position (5.350599ms)
✔ stats fence body sets defaults only and ignores the rest (4.227422ms)
✔ stats tile models cover every unit and every quality (1.562415ms)
✔ stats spark bars mark null gaps, zero ticks, and hollow today (0.933569ms)
✔ stats table rows and CSV share the same points (1.595792ms)
✔ stats overview ids prefer the fence, then config, then report order (1.825352ms)
✔ stats window label always states today and tracking start (0.463882ms)
✔ stats view state is session-only and per source path (21.082533ms)
✔ stats block renders header, tiles, table, and footer from JSON (51.023602ms)
✔ stats block shows an actionable card with Retry when bob fails (46.302406ms)
✔ stats block registers the processor and the Open Stats command (4.93555ms)
✔ stats revalidation gates on visibility: hidden views never spawn (106.217427ms)
✔ stats background tabs never spawn until the tab is visible again (87.533412ms)
✔ stats cache subscriber repaints only shown views reading the key (32.986047ms)
✔ stats local-date rollover bumps the change generation once per day (3.044907ms)
✔ stats stylesheet contract: selectors, tabular-nums, motion, colors (4.145489ms)
✔ Stats chart geometry stays finite across empty, constant, signed, and narrow inputs (11.774937ms)
✔ prior buckets align by elapsed position and omit invalid and provisional points (5.396775ms)
✔ chart renders SVG safely and keeps secondary focus metrics selectable (56.905489ms)
✔ grouped chart pins honest buckets, bounds daily detail, and opens validated notes (20.771129ms)
✔ local focus, table, pin, and definition changes reuse the retained report (31.401796ms)
✔ keyboard moves the daily cursor, cycles metrics, exempts controls, and fetches only shifts (53.862818ms)
✔ schema-1 fallback keeps day quartiles and never invents grouped daily history (11.747341ms)
✔ ResizeObserver redraws cached data and disconnects across rerenders and unload (138.451266ms)
✔ clock lenses update Pomodoro chart marks and leave older reports and task charts alone (81.243203ms)
✔ clock bar parts split Total, outline Off-clock, and never invent a missing tail (2.37623ms)
✔ spark bars keep clock detail for mixed, zero, null, and provisional cases (1.237073ms)
✔ tile headlines stay Bob's headline and Off-clock/Total comparisons stay neutral (4.295849ms)
✔ spoken Total points use Bob's displays and grouped buckets keep their span (3.785585ms)
✔ empty Off-clock windows are distinct from pre-adoption not_tracked points (1.976862ms)
✔ value-mark specs draw dashed Off-clock, mixed Total tails, and leave task metrics solid (5.748714ms)
✔ clock helpers preserve only canonical values and supplied display detail (4.225034ms)
✔ effective clock honors a pinned Pomodoro and leaves other metric families alone (0.625086ms)
✔ shared synthetic clock reports keep scalar, part, and summary splits consistent (126.462279ms)
✔ clock flags add only nondefault lenses and leave the Day strip key unchanged (2.369815ms)
✔ stored clock loads once, waits for a capable Worked bootstrap, then applies (25.797574ms)
✔ clockless and no-adoption reports fall back to Worked without erasing preference (3.232139ms)
✔ clock radio group is report-driven, native, labeled, and persists selection (7.265777ms)
✔ storage failures keep an in-memory clock choice operational (16.104178ms)
✔ c cycles clocks only from the free dash surface and preserves native guards (2.802428ms)
✔ clean cached Worked paints synchronously and switching back does not spawn (3.160639ms)
✔ a failed nondefault-lens fetch falls back to Worked once and never loops (16.80821ms)
✔ cache notifications do not interrupt a foreground paint or recursively prefetch (3.144679ms)
✔ idle lens prefetch deduplicates, skips fresh keys, and cancels on unload (5.911955ms)
✔ foreground queue entries outrank and promote queued idle prefetches (3.663226ms)
✔ stats resolution prefers stats.bob_path, then candidates, then PATH (4.543498ms)
✔ stats home expansion and range/offset normalization (1.906549ms)
✔ stats fetch always runs show -a -f json plus the chosen flags (0.868555ms)
✔ stats group emits -g before metric ids and rejects the rest (0.481823ms)
✔ stats request resolves one shared key for the page and strip defaults (2.229366ms)
✔ stats spawn passes vault env, NO_COLOR, timeout, and a large buffer (27.067485ms)
✔ stats spawn maps ENOENT, timeouts, and stderr to named errors (6.211002ms)
✔ stats decode accepts schema 1 and rejects the rest defensively (0.446104ms)
✔ stats error cards name the cause and the stats.bob_path fix (0.802857ms)
✔ stats fetch shares one flight per key and queues distinct keys FIFO (26.80933ms)
✔ stats fetch never loses waiters: A in flight, B then C settle with own reports (4.467184ms)
✔ stats queue caps at 8 distinct pending keys with explicit cancellation (4.700139ms)
✔ stats cache is a 16-entry LRU keyed by the argument list (5.361606ms)
✔ stats warm remount with a clean fresh entry spawns nothing (2.565591ms)
✔ stats change bump makes the next hit spawn exactly once (2.970748ms)
✔ stats change during a flight leaves the stored entry dirty (3.147677ms)
✔ stats entries older than the max clean age read dirty (3.616259ms)
✔ stats revalidate never skips a miss but skips dirty hits (3.166021ms)
✔ stats peek reads synchronously and listeners fire per store (2.703828ms)
✔ stats unload settles every waiter with cancellation (2.018931ms)
✔ stats spawn counters record each spawn (2.06012ms)
✔ stats block views count as shown without a visibility host (0.371234ms)
✔ stats api v2 keeps append and adds fetch plus bobPath (2.131732ms)
✔ statsHomeDir defaults to the real home and strips a trailing slash (0.262318ms)
✔ stats mac regression: un-injected resolution probes the real home first (1.673848ms)
✔ stats absolute candidates are probed verbatim with no doubled slashes (0.288515ms)
✔ stats with no home probes only absolute candidates (0.336801ms)
✔ stats tilde config expands against the real home (0.250794ms)
✔ stats candidate and tried lists share one source of truth (0.219546ms)
✔ stats spawn bob-not-found tried list uses the real home (2.885504ms)
✔ stats unload clears views, timers, cache, flights, and queues (2.739007ms)
✔ stats queue outcomes carry fetchedAt (3.299538ms)
✔ stats namespace v1 serializes versioned review answer JSONL (32.507207ms)
✔ stats journal rejects invalid calendar days and outcomes (4.64414ms)
✔ statsReviewHost lowercases, cuts at the first dot, and never throws (0.459317ms)
✔ stats journal plugin passthrough keeps a semver writer and falls back otherwise (4.52541ms)
✔ window lanes model matches panel root order and distinct hues (30.689852ms)
✔ legend labels use the root note name for daily review tasks (1.916905ms)
✔ tones mark unattributed none, muted gray, and hashed other/unnamed as gray (2.105209ms)
✔ theme order is coloured, gray, other, unnamed, with same-hue shades (3.016723ms)
✔ ranks, overflow, titles, meta, and area fallback (3.96468ms)
✔ clock lane and home models retain report splits and use the exact selected point (4.041227ms)
✔ clock labels keep count units and absent detail never invents a split (0.855956ms)
✔ Total lane paint draws the supplied tail and same-window clock changes morph (8.910242ms)
✔ omitted and empty states, and a pin never changes the model (4.330293ms)
✔ lanes render after the header and before the tiles (50.144416ms)
✔ legend is a keyboard stop, bar is aria-hidden, and activation does not fetch (50.015025ms)
✔ hover dims other keys, +N lights hidden keys, and leaving clears (5.899847ms)
✔ skeleton paints two empty tracks, morph only on a window change (24.380181ms)
✔ releasing the chart view also releases the lanes fit observer (12.865209ms)
✔ Themes panel caps at 8 with N more / Show fewer unless other is present (28.217733ms)
✔ stats window lanes stylesheet contract (2.132819ms)
✔ panel dispatch covers every family, custom kinds, and the net exception (2.183711ms)
✔ pomodoro panel shows the supplied total, shares, hue, and safe text (47.840533ms)
✔ home parts use the report catalog for labels, hue slots, and pinned values (21.817186ms)
✔ session drill-down labels off-clock rows and prefers the current session flag (4.974446ms)
✔ Total home and type panels render supplied worked spans and dashed tails (9.305901ms)
✔ roots panel toggles Themes, pins spans, discloses sub-projects, and opens home links (61.472596ms)
✔ a stale areas view maps to Root parents, and old bob falls back with copy (28.050938ms)
✔ Themes panel prefers report.theme_hues names and hues over the api lookup (6.462729ms)
✔ chart pin refreshes Where the time went and Themes honor the pinned span (17.0956ms)
✔ root-field homes keep their area hue and a missing homes report keeps the saved view (11.394205ms)
✔ task home table uses catalog labels and keeps hue dots and mini-bars (13.754009ms)
✔ task flow stacks signed values, keeps missing constituents missing, and labels series (10.676457ms)
✔ absent companions are named, custom filters are labeled overall, and net splits breakdowns (14.149462ms)
✔ journal panels pair answers with review time and a gapped keep chart under 90% (19.259075ms)
✔ checklist calendar aligns Monday weeks with states, reasons, and provisional today (10.483206ms)
✔ grouped calendars reuse daily points and old schemas fall back with a label (6.334188ms)
✔ ISO year boundaries stay in one Monday week and chore dots expose text (5.980505ms)
✔ panel day selection pins the shared day and never fetches (11.412783ms)
✔ field and formula metrics keep only the focus chart and table (4.740332ms)
✔ statsPanelDistinctHues gives every root its own colour (0.534646ms)
✔ statsPanelDistinctHues does not depend on input order (0.320048ms)
✔ statsPanelDistinctHues keeps different area hues and greys buckets (1.156206ms)
✔ statsPanelDistinctHues never throws past eight coloured roots (0.426765ms)
✔ root bar gives same-area roots distinct hues and gtd_daily stays coloured (6.958893ms)
✔ root rows and their sub-project leaves share the mapped hue (12.070093ms)
✔ TC vectors verbatim through the decoration builder (41.546706ms)
✔ TC14-TC18 vectors through the decoration builder (bob-cli-f5) (11.365813ms)
✔ the builder honors the other eligibility rules (5.523405ms)
✔ dim_closed_links = no: a closed link gets only the ring widget (2.42138ms)
✔ TR1-TR6 by checkbox symbol through the Tasks memo (7.872074ms)
✔ TR1-TR6 by checkbox symbol through the metadata cache (3.935303ms)
✔ TR7 falls back to the Tasks status type (7.319553ms)
✔ TR8-TR12 and TR14 give no ring, through every source (4.198674ms)
✔ TR13 a duplicate id is neutral in the memo, the live doc, and nowhere guessed (2.332926ms)
✔ TR15 same-note live document shows an unsaved status change on the same frame (0.871834ms)
✔ TR16 falls back to the metadata cache without a title (1.649784ms)
✔ TR17 ^prj, #ref, and Event Tasks ring by status (2.951647ms)
✔ source precedence: live doc, then Tasks memo, then metadata cache (2.971113ms)
✔ render never reads from disk, and resolves each unique link once per build (2.3534ms)
✔ TT vectors through the widget DOM (5.634064ms)
✔ buildTaskLinkMarkElement is a listener-free host and rejects bad states (0.62467ms)
✔ plain click places the caret before the link and never navigates (2.246157ms)
✔ Mod+click opens the link exactly like Mod+clicking the link text (2.263385ms)
✔ widget eq compares key, state, tooltip, swap, and the click target (0.365631ms)
✔ the ring is always last at a shared offset (4.379745ms)
✔ setup registers the toggle command, the gate, the extension, and the listeners (0.732824ms)
✔ the toggle flips the flag and gate, clears the rings, and notices (4.545626ms)
✔ the toggle also mirrors the gate into popout documents (0.807195ms)
✔ every trigger schedules one coalesced refresh that rebuilds all editors (1.691686ms)
✔ the refresh reaches leaf editors the extension has not tracked (0.433626ms)
✔ setup hands off to the Reading-view phase through guarded hooks (0.343381ms)
✔ the lifecycle calls one setupMarkFamilies and stays within the fragment limit (3.528977ms)
✔ rebuild reasons: refresh, doc, mode, viewport, and never selection alone (1.996458ms)
✔ the view plugin rebuilds on refresh and doc changes, keeps decorations on selection-only updates (2.910805ms)
✔ swap rule: never on first paint, once on a state change, never on scroll (8.468713ms)
✔ swap rule: every editor animates its own change, new editors do not (5.219025ms)
✔ swap rule: a same-note live edit swaps on the doc rebuild; a toggle resets it (1.906202ms)
✔ taskLinkMarkSwapFor keeps a bounded LRU of painted keys (8.520328ms)
✔ the live document model indexes ids and survives bad input (0.486333ms)
✔ the document model is memoised per document version (0.477433ms)
✔ a viewport-limited build over a 1,000-line note stays fast (324.363391ms)
✔ the Tasks snapshot is read once per memo generation, not once per link (6.5032ms)
✔ Reading post-processor stamps source paths and inserts the shared ring host (8.113503ms)
✔ daily-note view wrapper does not suppress prose links (1.415523ms)
✔ embeds render, while embed headers, metadata, plugin chips, and managed edge rows stay raw (4.253815ms)
✔ TC19-TC20 vectors: ordinary prose starting with a managed label word still rings (bob-cli-f5) (2.203479ms)
✔ TC20 vector: a bold managed label owns the row, with or without a task checkbox (2.042064ms)
✔ closeout: a managed label later in a row does not suppress it (1.917395ms)
✔ closeout: a rendered Reading section that Obsidian detached still updates, and never swaps (bob-cli-f5) (2.658143ms)
✔ closeout: detached-anchor tracking is weak and bounded (7.19236ms)
✔ Pomodoro ledger links stay unmarked; mixed and deeper rows remain eligible (4.05187ms)
✔ query-row retry sees links added after the Markdown post-processor (2.824794ms)
✔ a Tasks query row resolves against its own task path; unknown query paths stay neutral (1.022579ms)
✔ a Tasks description render uses ctx.sourcePath when the query row has no origin path (0.694778ms)
✔ a Tasks row pass does not stamp nested DEPENDS ON or LINKS children (2.170292ms)
✔ sweep stamps Tasks query rows that appear after the Markdown post-processor (0.652997ms)
✔ stamped-anchor sweep updates in place and removes marks when targets stop resolving (0.722051ms)
✔ the session toggle sweep removes and restores Reading rings (0.55914ms)
✔ plain ring mousedown does nothing and Mod+click opens the linked task (1.425538ms)
✔ TS vectors verbatim: block-link scanner (5.03103ms)
✔ TS16-TS17 vectors verbatim: code delimiters and comment text (0.576945ms)
✔ TC vectors verbatim: document-level line eligibility (8.623213ms)
✔ TC14-TC15 vectors: a closing fence matches its opener (0.748857ms)
✔ TC16-TC17 vectors: code delimiters never open comments (0.507667ms)
✔ TC18 vector: real multi-line comments exclude only the comment (0.818634ms)
✔ TC19 vector: the managed row source fallback is anchored at the row start (2.232105ms)
✔ pure TR vectors verbatim: parser plus state model (2.273353ms)
✔ TT vectors verbatim: tooltip model (1.693901ms)
✔ TG vectors verbatim: styles.css ring family (2.414862ms)
✔ taskMergeDecodeReport accepts the bob task merge schema (3.024648ms)
✔ taskMergeDecodeReport surfaces bob errors, versions, and shapes (0.73697ms)
✔ taskMergeLocatorText builds note:block-id locators (1.364951ms)
✔ apiTaskMergePreview plans with --dry-run and dedupes sources (0.763732ms)
✔ apiTaskMergePreview refuses without sources or target (0.449797ms)
✔ apiTaskMergeApply passes picks and skips -p when unpicked (0.883103ms)
✔ the taskMerge api shape carries version 1 with preview and apply (0.483761ms)
✔ TT vectors verbatim: task-line gate plus boundary tokens (14.628568ms)
✔ TT13-TT14 cursor reveal is inclusive (8.474837ms)
✔ TT16 coexistence: task tag range is disjoint from priority and date marks (3.260516ms)
✔ tooltip is exact and never contains a double colon (0.537194ms)
✔ element structure: empty widget span with tooltip attributes (1.396806ms)
✔ Live Preview decorations cover exactly the tag and respect reveal and code (3.190843ms)
✔ widget mousedown reveals the tag start (1.496385ms)
✔ TR vectors verbatim: rendered views annotate eligible anchors in place (5.815648ms)
✔ TR9 toggle strips document-wide and re-annotates on enable (3.652209ms)
✔ annotate and strip helpers are idempotent and defensive (0.831131ms)
✔ session toggle and onload wiring (106.81104ms)
✔ styles.css contract: teal identity ink, glyph, both hosts, hover, hide in Tasks, resting, print, motion (3.433297ms)
✔ TT20-TT28 verbatim: the #task #ref pair yields one ref range spanning both tokens (2.986762ms)
✔ Live Preview ref decorations replace the whole pair and reveal both tags at once (5.722771ms)
✔ ref element structure: book classes, reference label, and tooltip (0.595496ms)
✔ TR10 verbatim: the #task anchor becomes the book and the adjacent #ref anchor hides (7.523255ms)
✔ TR11 verbatim: #task #references and reversed order keep the hash only (2.943932ms)
✔ TR12 verbatim: Tasks rows never annotate (the #ref book is CSS-only) (0.495225ms)
✔ TR13 toggle covers the new classes: off strips the book and reveals #ref, on restores both (2.634686ms)
✔ styles.css contract for reference reading tasks: glyph, variant, resting, hidden partner, Tasks book (4.311712ms)
✔ CK vectors: canonical PRE/POST checklist runs share membership semantics (1.984235ms)
✔ CK live preview and widget vectors: one stable glyph replaces the full run (2.289388ms)
✔ CR vectors: rendered checklist anchors annotate in place, conflict stays native (3.776013ms)
✔ CR3 toggle restores all checklist pills and re-annotates them (1.838547ms)
✔ CR4 Today reading-view anchor follows the second checklist tag (1.001035ms)
✔ checklist task mark CSS contract covers glyphs, conflict gates, Tasks rows, and resting (3.068083ms)
✔ mark gate holds in popout windows for both toggle states (1.970017ms)
✔ bracket and paren fields parse with UTF-16 offsets (7.454141ms)
✔ duplicates and invalids are repair, never a pill (2.146743ms)
✔ no inherited ghost pill and closed history (0.58658ms)
✔ unknown and known hues (0.957413ms)
✔ tooltip copy, reason phrases, and no double-colons (0.844874ms)
✔ Live Preview folds, reveals, and refuses code (8.898139ms)
✔ fallback fold mirrors the selection rule (0.766978ms)
✔ widget click reveals the field at the folded offset (1.216753ms)
✔ session toggle, gates, and onload wiring (5.663767ms)
✔ mark gates hold in popout windows for both toggles (9.83053ms)
✔ lazy hover enriches only the hovered pill (1.546955ms)
✔ styles.css contract for task theme pills (3.788577ms)
✔ helpers never throw on bad input (4.067591ms)
✔ canonical daily paths require matching directory and filename years (0.89106ms)
✔ repair tooltips use the raw value, never the whole field span (0.37777ms)
✔ setup wires theme and metadata refresh; unload removes editor hover (2.893035ms)
✔ taskThemeMarkSourcesInText finds bracket, paren, duplicate, and invalid (5.101653ms)
✔ rendered views wrap a single-node explicit field and keep surrounding text (8.671296ms)
✔ rendered views join a field split across adjacent text nodes (1.499677ms)
✔ paren delimiter, unknown, duplicate repair, and invalid repair (2.262659ms)
✔ code, prose, nested rows, existing pills, and table cells stay raw (1.293916ms)
✔ Dataview inline-field chips on task rows become pills; page fields do not (1.288859ms)
✔ rendered views fold an explicit [type::] field the same way as [theme::] (0.753369ms)
✔ query rows keep the originating note, never the dashboard path (1.220873ms)
✔ without provenance a dashboard query does not invent an origin (0.498387ms)
✔ idempotent re-render, clone, lazy hover, toggle, and unload restore (2.485527ms)
✔ detached and pending Tasks rows retry then drop on disable (1.441459ms)
✔ setup registers the Reading-view postprocessor; helpers never throw (28.219302ms)
✔ missing data-line stays absent; zero-based line zero becomes line 1 (0.493054ms)
✔ duplicate native chips and mixed native/raw fields share one repair (1.631317ms)
✔ rendered hover supplies source text and skips unresolved enrichment (2.312783ms)
✔ native wrappers stay accessible when the marks gate is off (0.982594ms)
✔ setup refresh and hover teardown cover rendered roots (2.778572ms)
✔ stylesheet custom properties do not reference themselves (17.58741ms)
✔ explicit and legacy fields, repair, and none (2.971482ms)
✔ taskTagMarkRanges attach the explicit type without changing offsets (10.818003ms)
✔ identity kind: repair, unconfigured, muted, inherited, explicit (0.673991ms)
✔ explicit identity tooltip, aria, shown, and no double-colons (3.188141ms)
✔ inherited identity is tooltip-only until the toggle is on (2.988605ms)
✔ unconfigured explicit type keeps the name and drops the hue (0.617139ms)
✔ repair identity is always shown as #? (0.433312ms)
✔ applyTaskTagTypeAttrs writes and clears data-bob-type (4.118122ms)
✔ stale or missing identity is a generic glyph (0.720587ms)
✔ ledger disagreement and composite quiet prefix (4.692088ms)
✔ ledgerTypeMarkLinks find dedicated Task Links and keep the entry name (6.898802ms)
✔ buildLedgerTypeMarkElement paints disagree and composite (0.686614ms)
✔ inherited toggle is off by default and the command is registered (4.621962ms)
✔ D11 contrast: 8 slots × {plain, Blocked, In Progress, Next} × {light, dark} ≥ 4.5:1 (7.546085ms)
✔ muted type ink contrast: plain and lane tints at 7% and 14% × light/dark ≥ 4.5:1 (10.134878ms)
✔ exempt PLAN identity stays muted and omits its hue attribute (0.46957ms)
✔ styles.css defines type ink, identity ::after, and ledger marks (6.077849ms)
✔ helpers never throw on bad input (0.541414ms)
✔ section info null stays neutral (TM19) (7.123901ms)
✔ data-line mapping stamps and marks an exact Today row (11.059458ms)
✔ data-line mapping rejects a status mismatch (0.779436ms)
✔ row-index fallback maps when counts agree and refuses when they disagree (7.136982ms)
✔ Tasks result rows and code are skipped (7.256128ms)
✔ a daily-note sourcePath is skipped (0.586815ms)
✔ duplicate ids stay neutral (1.005336ms)
✔ insertion points: #task anchor, #ref pair, checkbox, whitespace split (8.687834ms)
✔ identity-proven non-Today rows are stamped without a mark (3.725786ms)
✔ sweep adds on link, removes on unlink or completion, updates tooltip, respects toggle, skips daily ancestors (2.703226ms)
✔ daily-view class is set on open daily leaves and cleared on switch (0.794938ms)
✔ delegated Mod+click jumps; plain click does not (2.826901ms)
✔ setupTodayMarks registers the reading post-processor at order 60 (1.422066ms)
✔ styles.css daily-view suppression is present (4.075987ms)
✔ Live Preview marks do not double-jump in Reading view (1.165493ms)
✔ mid-body #task goes at the body start (1.470778ms)
✔ #task inside inline code stays neutral (0.717026ms)
✔ re-render with a new path refreshes the mark key (0.683777ms)
✔ one duplicate scan per render (1.184004ms)
✔ row-index fallback uses every list item (0.671967ms)
✔ open statuses are exactly space, star, slash, and question (4.644724ms)
✔ trailing-id rules: leading space, trailing-only, valid charset (1.057255ms)
✔ candidate: TM9 closed stays null, TM10 open statuses pass (4.686484ms)
✔ candidate: TM11 needs an exact #task tag and a trailing id (3.900138ms)
✔ candidate: TM21 code is left for the call-site code check (0.845113ms)
✔ insert offset: #task first lands before the title (0.436147ms)
✔ insert offset: TM16 #task #ref spans the pair, #prj sits between (0.498424ms)
✔ insert offset: mid-body #task falls back to the body start (0.328788ms)
✔ insert offset: blockquote, spaces, numbered, empty title, emoji (5.67825ms)
✔ duplicates: TM15 marks neither line (2.149457ms)
✔ session text: named, home label, range-only, unnamed (0.79674ms)
✔ tooltip: TM1 running, TM2 queued, and the platform variants (0.648996ms)
✔ tooltip: running wins as primary with a +N more suffix (2.488077ms)
✔ tooltip: empty input yields Today and output never has :: (0.580044ms)
✔ entering window: 600 ms after join, never before or at load (0.345923ms)
✔ modifier: primary button with meta on mac, ctrl elsewhere (0.341906ms)
✔ element: empty span with tooltip attributes and no listeners (0.880532ms)
✔ widget: eq ignores entering and the callback (0.408857ms)
✔ widget: plain mousedown moves the cursor, Mod mousedown jumps (1.232523ms)
✔ refresh effect is lazy and stable (0.248815ms)
✔ styles.css implements the glyph anatomy contract (2.410906ms)
✔ Live Preview applies the TM1-TM22 line, cache, and refresh vectors (141.27847ms)
✔ Today mark lifecycle registers the toggle, keyboard command, and reading processor (176.769063ms)
✔ keyboard jump uses the task under the cursor and reports non-membership (113.934736ms)
✔ Mod-click and keyboard jumps land on the current running Task Link (73.910005ms)
✔ reduced motion stops the entrance pop (2.245336ms)
✔ tooltips never contain :: (0.380809ms)
✔ todayMarkPosInInlineCode: single, double, unmatched, positions (0.556877ms)
✔ builder gates on Today ids without touching doc lines (90.285861ms)
✔ two rebuilds on the same doc compute duplicates once (140.309988ms)
✔ todayMarksNow override drives readiness (168.413628ms)
✔ refresh dispatches only to non-daily leaves and uses 16 ms (89.236633ms)
✔ keyboard command gates closed status and daily notes (50.442983ms)
✔ TM14 rollover: day N+1 shows no decoration (51.702119ms)
✔ TM17 widget sits at line.from + insertCh with side -1 (110.511129ms)
✔ TM18 entering: new key pops then settles (73.919055ms)
✔ TM20 toggle flips class, notice, and refreshes non-daily leaves (65.73016ms)
✔ rebuild triggers: doc, viewport, LP field, file switch rebuild; selection alone does not (48.988979ms)
✔ jump guards in-flight, prefers cached ledgerLine over later match (84.539851ms)
✔ jump with no open daily leaf attempts the daily open (110.073323ms)
✔ home labels: unnamed timed entry uses derived label and 1-based entryLine (127.898393ms)
✔ mark gate holds in popout windows for both toggle states (116.720186ms)
✔ T1 GTD: empty target resolves to the daily note (6.319679ms)
✔ T2 markers: pomodoro mark counts, struck drops, embed counts (1.384994ms)
✔ T3 closed entries: links under completed/cancelled entries drop (0.570264ms)
✔ T4 shapes: mixed text and deeper descendants drop (1.003214ms)
✔ T5 dedupe: same task twice keeps the first position (0.602245ms)
✔ T6 fenced: links inside fenced blocks drop (0.463231ms)
✔ T7 status: the link layer lists every dedicated link (0.791022ms)
✔ T8 unresolved: missing notes give no key (0.454541ms)
✔ T9 alias: aliased links count under their target (3.931777ms)
✔ laneBudgetFromTasks counts the whole Next lane, Today included (2.754437ms)
✔ laneBudgetFromTasks counts Pending by type and flags over-cap (1.000402ms)
✔ lane caps come from max_next/max_pending; legacy max_now is ignored (0.386878ms)
✔ reload event name matches the Tasks bundle subscription (0.221483ms)
✔ api v2 shape: Today and lane budgets, no nowBudget (25.591329ms)
✔ cache rebuild answers isToday/todayRank in ledger order (8.679072ms)
✔ refresh fires only when the key set changes (5.055415ms)
✔ unready to ready with empty TODAY still refreshes open badges (3.316691ms)
✔ cache rebuilds on the daily changed event with the event content (3.221269ms)
✔ cache rebuilds once on resolved and at midnight rollover (5.51474ms)
✔ computeTodayLinks records entry range and placeholder (1.029163ms)
✔ todayOpenEntries and todayRunningEntryLine follow the unique timed rule (0.711574ms)
✔ resolveTodayLinkKeys keeps duplicates; resolveTodayKeys is first-occurrence (0.948406ms)
✔ todayLinkDetails: named running, placeholder, unnamed home, unnamed none (0.571046ms)
✔ todayLinkDetails orders running first and keeps one detail per key+entry (0.394346ms)
✔ todayKeyParts splits at the last hash; idsByPath groups block ids (0.313262ms)
✔ todayDetailsSignature changes only when details change (0.423258ms)
✔ idsByPath and details accessors follow the rebuilt cache (9.37811ms)
✔ details-only change refreshes marks without a Tasks reload (3.909321ms)
✔ entered stamps only when the cache was already ready, then prune (3.781318ms)
✔ generation guard: reverse-order async reads keep the newer (3.951406ms)
✔ generation guard: a sync rebuild wins over an in-flight async read (2.827351ms)
✔ revalidateTodayCache is throttled and refreshes when not ready (3.825848ms)
✔ revalidateTodayCache respects layoutReady and backwards clock steps (8.864935ms)
✔ a done-today prerequisite shows the glyph (15.311625ms)
✔ done yesterday does not show the glyph (1.197212ms)
✔ a struck link does not show the glyph (0.487855ms)
✔ a closed entry does not show the glyph (4.669276ms)
✔ several prerequisites give +N (1.330517ms)
✔ the model refuses every non-glyph shape (4.816458ms)
✔ unblockedGlyphDoneToday needs DONE plus a today done date (4.784424ms)
✔ tooltip names one prerequisite and counts several (0.786191ms)
✔ Live Preview places one glyph after each unblocked link (8.684431ms)
✔ Live Preview draws nothing without a warm cache or a live link (1.126071ms)
✔ widget mousedown places the cursor past the link (5.141326ms)
✔ rebuild triggers skip the cursor but take doc, viewport, and refresh (6.271587ms)
✔ Reading view glyphs unblocked rows and dedupes (7.576529ms)
✔ Reading view refuses every non-glyph row (7.709244ms)
✔ api.unblockedGlyph v1 is additive, sync, and never throwing (6.557516ms)
✔ session toggle, onload wiring, and refresh fan-out (10.476465ms)
✔ mark gate holds in popout windows for both toggle states (1.98796ms)
✔ changed-file and rollover refreshes (1.323105ms)
✔ the refresh effect stays lazy: one eager define (0.273205ms)
✔ styles.css contract: faint glyph, Done token, toggle (2.551733ms)
✔ Ledger Vim mappings restore \p and retain the other normal-mode actions (4.23706ms)
✔ workBadgeTone boundary vectors at cap 100 use exact comparisons (2.372638ms)
✔ workBadgeTone at cap 15 has no percentage rounding (0.394427ms)
✔ workBadgeTone default caps, small caps, and cap changes (0.33907ms)
✔ workBadgeTone never coerces invalid input to zero (2.111052ms)
✔ TODAY tone follows the Task Link meter (0.606085ms)
✔ type count never forces TODAY red (0.410194ms)
✔ TODAY unavailable stays neutral, empty section is grey (3.196637ms)
✔ PENDING/NEXT models color the section, READY its gated count (1.179693ms)
✔ READY uses its gated count even when the total lane is larger (0.435737ms)
✔ cap equality still emits no cap lint (10.763946ms)
✔ lane DOM keeps exactly one tone through transitions and unavailability (31.646112ms)
✔ READY DOM keeps exactly one tone and daily/dashboard models agree (3.687388ms)
SKIP dashboard integration: BOB_DASHBOARD_FILE is not set
SKIP dashboard fallback integration: BOB_DASHBOARD_FILE is not set
SKIP dash CSS contract: BOB_DASHBOARD_FILE is not set
✔ daily TODAY chip follows links when type count is high (102.56287ms)
✔ dashboard integration uses Work tones, TODAY override, and keeps Work order (6.675392ms)
✔ dashboard fallbacks keep Work tones without plugin renderers or colors (3.898032ms)
✔ Work tone CSS covers each tone and uses the shared magenta value (3.246766ms)
✔ RBW6 mergeTargetPreparations keeps one write at the strongest lane (8.852895ms)
✔ §15.7 notices use curly quotes and the Ready → Blocked copy (7.137063ms)
✔ RBP1 same-note add is one transaction and matches forward bytes (98.35638ms)
✔ RBP2 background-leaf T matches forward bytes (24.553015ms)
✔ RBP3 closed T is written through vault.process and matches forward bytes (42.401272ms)
✔ RBP4 ordinary transfer; a ^prj N is never raised (42.023517ms)
✔ RBP5 consumed Pomodoro link matches forward bytes (25.091611ms)
✔ RBP6 project T with residents and a sub-project matches forward bytes (71.710321ms)
✔ RBP7 two dependents in different lanes prepare N once at [/] (23.912073ms)
✔ RBP8 counted sources N1 and N2 match forward(T + N1, N2) (13.306772ms)
✔ RBP9 blocks_lines false writes no BLOCKS and still ids N (5.968057ms)
✔ RBP10 removing the last reason matches forward removal (16.224683ms)
✔ RBW1 a changed source note writes nothing (5.950212ms)
✔ RBW2 one changed T note still lands the others and omits it from BLOCKS (10.116529ms)
✔ RBW3 already-present picks write nothing (2.30281ms)
✔ RBW4 cleanup runs for T's that committed when N lives in today's daily note (6.529899ms)
✔ RBW6 counted forward two-lane dependents prepare N once (40.018572ms)
✔ A1 N above two T's in one note matches forward (open and closed note) (65.42588ms)
✔ A1 N below two T's matches forward bytes (12.227992ms)
✔ A2 forward stamps the dependent when a prerequisite above gains BLOCKS (1.900471ms)
✔ A1 mixed same-note and cross-note picks keep N's lane rise (RBP7 variant) (12.325866ms)
✔ A1 RBP1 with N truly lacking ^id is prompted an id and matches forward (6.61793ms)
✔ A1 N lacking ^id in a closed note above T keeps its BLOCKS line under N (4.623711ms)
✔ A3 mirror lists the committed T's by identity (N above T1, X, T2) (3.739334ms)
✔ A4 notices name T, not N (add, remove, project, counted) (9.562913ms)
✔ A5 the writer's stale notice is returned once and never shown by the writer (0.492168ms)
✔ A6 a changed T row (rawLine) is refused before any write (0.425474ms)
✔ A7 RBW2 keeps the failed T's Pomodoro link and consumes the committed one (6.906356ms)
✔ A8 closed-note T guards run when the gesture is applied (22.765902ms)
✔ A9 a ^prj T's residents recover with [unblocked::] when N lives in a daily note (24.213078ms)
✔ A5 a preparation no write can carry fails the plan instead of being dropped (1.251987ms)
✔ applyDependencyEdit adding a first cross-note prerequisite keeps the dependent's cursor (6.336141ms)
✔ applyBlocksEdit giving a source its first BLOCKS line keeps the source's cursor (6.464478ms)
✔ nav BK1–BK2 accept canonical BLOCKS lines (5.283937ms)
✔ nav BK3–BK11 canonicalise (1.197123ms)
✔ nav BK12 empty, BK13–BK15 malformed (0.76642ms)
✔ nav BK16–BK18 not-a-line, BK19 slot-free, BK20 cross-parse (0.926623ms)
✔ nav BK21 code-point sort and writer format (0.573479ms)
✔ nav MC5 ! refuses BLOCKS lines; MC7 Sub-projects never claims BLOCKS (1.011615ms)
✔ nav BW18 conversion drops BLOCKS like Sub-projects (2.52743ms)
✔ nav Rule 8 Ctrl+Shift+P on BLOCKS routes to the owner (2.006528ms)
✔ nav BW12 BLOCKS-only hand edit reports blocks-only; Rule 7 annotation exists (2.948833ms)
✔ nav MC1/MC2 deferred Pomodoro cleanup skips managed lines (0.710769ms)
✔ showBlocksStage opens from a task with reverse CURRENT and RESULTS (79.919233ms)
✔ showBlocksStage opens from a counted session (4.862179ms)
✔ showBlocksStage opens on a Task Link target note (8.180499ms)
✔ RBU1 empty query uses today-first then In Progress, Next, same-note, rest (6.930016ms)
✔ RBU2 today-linked rows carry 🍅 running and strip names the entry (2.149932ms)
✔ RBU3 CURRENT 🔑 only when N is the last reason (6.591466ms)
✔ RBU4 footer verbs are block, remove, and apply N (9.194198ms)
✔ RBU5 subtitle at rest, with marks, and names this task first (28.661549ms)
✔ RBG1 N itself is excluded from RESULTS (1.254912ms)
✔ RBG2 a cycle disables the row with path tooltip copy (4.817526ms)
✔ RBG3 ^prj T with N inside the project is inside this project (6.58014ms)
✔ RBG3 descendant N disables the parent project as a sub-project (7.414848ms)
✔ RBG4 a malformed or second Depends-On line is guarded (4.765805ms)
✔ RBG5 stale refuse reopens in the Blocks direction (7.779395ms)
✔ RBG5 for T: a T changed after stage open refuses once and writes nothing (13.318136ms)
✔ today's links survive a pool refresh that lands while the daily note loads (35.775448ms)
✔ RBG8 Esc from the stage or the block-ID prompt writes nothing (3.307502ms)
✔ missing source ^id opens the block-ID prompt and Esc allocates none (5.716373ms)
✔ RBP11 inbox route runs first then the Blocks write (2.007277ms)
✔ RBW5 review walk stays unless the commit takes N out of today's walk (6.510711ms)
✔ marks commit add and remove together; counted uses k/n block (5.454239ms)
✔ strip text covers RESULTS, BLOCKED, CURRENT, disabled, marks, and ^prj (0.536371ms)
✔ counted subtitle drops the ⇥ hint because marks are off in counted sessions (1.295076ms)
✔ 🔑 tooltip and 🍅 tooltip render on badges (3.628668ms)
✔ Tab marks Blocks CURRENT rows and Enter removes both dependents (24.930145ms)
✔ SB1-SB9 dependent IDs match the successor mint vectors (12.846122ms)
✔ BW1 same-note add mints and writes BLOCKS in the dependent's single transaction (30.802263ms)
✔ BW2 cross-note add follows the dependent commit and writes the target note (5.910867ms)
✔ BW4 cross-note target preparation precedes the reverse-line preimage (3.350338ms)
✔ BW3 stale cross-note preimage leaves the forward write standing and shows the suffix (2.343298ms)
✔ BW5 removal deletes the reverse line when its last dependent leaves (7.869138ms)
✔ BW6 an already mirrored edge is a byte-identical no-op (1.435094ms)
✔ BW7 closed owners stay frozen (2.343205ms)
✔ BW8 malformed reverse lines stay untouched and report the failed mirror (2.765006ms)
✔ BW15 config defaults on, honors false, and invalid values fall back on (1.05632ms)
✔ BW17 planner output follows BK21 Unicode code-point ordering (11.029147ms)
✔ duplicate BLOCKS children merge their known dependents and preserve CRLF (0.833424ms)
✔ BW9 counted same-note add-to-all lists every dependent on one sorted BLOCKS line (570/270) (6.018098ms)
✔ counted remove-from-all drops every dependent from the same-note BLOCKS line (420) (2.300761ms)
✔ vault counted add composes cross-note follow-ups for every source (420) (1.599708ms)
✔ marked batch add writes every same-note target onto BLOCKS in one plan (430) (1.082802ms)
✔ counted Ctrl+D clears same-note BLOCKS when the last dependents leave (600) (8.811419ms)
✔ BW10 hand-edit add mirrors the new target onto BLOCKS when the cursor leaves (7.308764ms)
✔ BW10 hand-edit remove and BW11 undo re-fire drop the dependent from BLOCKS (5.852548ms)
✔ hand-edit clear path routes through the BLOCKS seam (600) (3.450232ms)
✔ BW18 conversion never copies a BLOCKS line as a user child (1.361071ms)
✔ BW19 Ctrl+Shift+M moves the owner's BLOCKS line with rebased links and never duplicates it (9.747654ms)
✔ family table is frozen and ordered s, w, n (3.498311ms)
✔ view model covers s, w, n, null, and garbage (1.248857ms)
✔ desktop mount creates exactly one item with three letters and none on cold device (10.147258ms)
✔ mobile, non-desktop, or missing status bar mounts nothing and keeps type undefined (1.785479ms)
✔ a second setup does not add a second item (1.122919ms)
✔ startup restores the stored mode with no key press; invalid stays none (1.805515ms)
✔ family commands repaint to their family and reuse the same DOM nodes (5.510294ms)
✔ same-family commands skip DOM writes because the paint key is unchanged (1.42248ms)
✔ is-instant applies on first appearance and none to family, not family to family (2.231296ms)
✔ ensureBracketModeDom is idempotent and paint skips unchanged keys (6.960893ms)
✔ repeat flashes forward and backward, delegates with args, and returns the result (1023.417183ms)
✔ cold repeat flashes empty, shows the notice, and returns false (713.910548ms)
✔ a throwing indicator never changes delegation, storage, or notices (1.703946ms)
✔ clicking a letter selects the family, persists it, and never walks (5.170255ms)
✔ mousedown on a letter keeps editor focus and registerDomEvent is preferred (1.750082ms)
✔ onunload clears flash and instant timers (4.753131ms)
✔ pure helpers accept only s, w, and n and return frozen direction plans (4.311592ms)
✔ registration adds repeat commands and keeps all bracket family commands (4.132459ms)
✔ each family callback records its family and preserves its original arguments (1.627747ms)
✔ repeat delegates every type in both directions with key-owned direction (0.894863ms)
✔ a review direction key followed by ]] repeats forward; the last family wins (4.454156ms)
✔ cold start and invalid stored values show the empty notice without moving (1.821094ms)
✔ a fresh instance lazily restores its stored type (0.535907ms)
✔ missing or throwing local storage keeps repeat state in memory (0.819997ms)
✔ repeat delegates synchronously so the real lane walk consumes Vim count before landing (9.509897ms)
✔ other navigation, internal advances, and blank-line commands do not record (2.500303ms)
✔ review checklist group helpers format exact completion and close notices (4.595086ms)
✔ claim declines without a current exact PRE/POST walk landing (19.526622ms)
✔ an internal first-endpoint landing lets Ctrl+Enter complete and land on the next live PRE row (6.321334ms)
✔ checklist Ctrl+Enter holds its landing through the actual successor picker (30.568329ms)
✔ seven Ctrl+Enter presses walk PRE with stale queues and either recurrence insertion mode (24.523858ms)
✔ a landed [?] checklist chore is claimed and completed (0.953403ms)
✔ ]s skips two PRE chores; Ctrl+Enter finishes PRE with the skipped count (2.817582ms)
✔ live successor filtering skips a stale completed row (0.989702ms)
✔ live group filtering reads each cross-note path once (0.579905ms)
✔ Ctrl+Enter stays in PRE while Ctrl+Alt+F still crosses into NEW (6.75927ms)
✔ POST completion walks multiple rows for Ctrl+Enter and Ctrl+Alt+F, while Alt+F stays (3.644346ms)
✔ completing the last POST row closes the final Morning review; earlier POST rows stay counted (1.228072ms)
✔ ]S from ROTTEN lands on POST row one (1.684415ms)
✔ completion failure preserves cursor and landing and reports the Tasks failure (0.634332ms)
✔ a keep-moving picker holds the checklist landing and its ⏭ notice joins the single walk toast (40.996394ms)
✔ reviewLineChecklistKind matches exact #gtd #pre/#post tokens (3.207268ms)
✔ Alt+F on PRE stays with remaining PRE count and never stamps (19.607127ms)
✔ Ctrl+Alt+F completes seven PRE rows from a stale cache (62.327469ms)
✔ Ctrl+Alt+F completes seven PRE rows from a refreshed cache (28.304162ms)
✔ POST stays put with the closing notice (2.216378ms)
✔ manual Ctrl+Enter then ]s from a refreshed cache lands on the next PRE (3.309384ms)
✔ manual Ctrl+Enter then ]s from a stale cache uses text-first identity (1.109499ms)
✔ counted Alt+F skips checklist rows with the skip tail (7.611823ms)
✔ missing cycler gate on a PRE row writes nothing (6.556949ms)
✔ missing ledger checklist gate on a tagged line writes nothing (1.082074ms)
✔ a tagged line that is not a queue match falls through to recurring refusal (2.166173ms)
✔ formatFreshStampChecklistSkipTail names the skipped count (0.222116ms)
✔ partitionFreshStampChecklistSkips pulls PRE/POST out of a mixed batch (0.313867ms)
✔ Task Link Alt+F skips a PRE target with the skip notice (12.623273ms)
✔ opened decay modal and its modal container are adopted into the active workspace document (3.135523ms)
✔ P0 at interval 3 on Bryan's ladder enters P1 (7.682368ms)
✔ P0 at interval 7 still enters P2 on the default 2–7 / 8–30 ladder (0.594968ms)
✔ P0 at interval 7 enters P2 with a previewed decay date and kept tail (1.204807ms)
✔ P0 at interval 30 enters P3 (7.00925ms)
✔ fixed enter overrides the interval scan (1.087956ms)
✔ unknown enter disables Not now without disabling Keep/Reword (4.521034ms)
✔ P0 with no suitable level stays unavailable and never shortens the lease (1.038593ms)
✔ custom level order resolves entry in ladder order (0.925971ms)
✔ unknown priority value disables Not now only (3.636611ms)
✔ prioritized P2 below its roll limit stays on the same level (1.565094ms)
✔ P2 at its roll limit decays to P3 (0.899689ms)
✔ P2 streak derives from the task Schedule Log (7.480373ms)
✔ configured decay:false keeps rolling past the limit (0.752622ms)
✔ per-level rolls:0 decays immediately (0.663908ms)
✔ terminal cancel substitutes a truthful same-level card roll (0.982137ms)
✔ no future date in the window refuses Not now (2.274883ms)
✔ card Step moves one rung and terminal priority rolls in place (2.51547ms)
✔ every configured P-level label uses the Ready keep allowance (0.702133ms)
✔ Less often steps 7/14/30 to the next preset with a decision reason (18.316283ms)
✔ Less often at 90+ opens the constrained custom picker; 365 is unavailable (0.59517ms)
✔ previewed dates are stable for one random draw (0.727552ms)
✔ Keep saturates at 999 and Drop preserves keeps history (0.601337ms)
✔ kept tails preserve roll classification; decisions break it deliberately (2.274705ms)
✔ invalid priority config offers no priority-changing action (0.453222ms)
✔ decay off disables Not now but keeps counting (0.645408ms)
✔ explicit level picks cover the ladder with previewed rolls (1.874362ms)
✔ card model is deeply frozen (0.411262ms)
✔ priority snapshot reports distinct load errors (1.120897ms)
✔ single Alt+F on an at-limit task opens the card and writes nothing (28.394766ms)
✔ dismissing the card writes nothing and does not advance (3.906221ms)
✔ early dates open the card and write nothing (2.866855ms)
✔ namespace v5 with decide true stamps counted and opens no card (8.543195ms)
✔ stale task-line change writes nothing (3.441294ms)
✔ stale local-day change writes nothing (11.534011ms)
✔ stale decay-config change writes nothing (3.027737ms)
✔ stale priority-ladder config writes nothing (4.439749ms)
✔ stale child Schedule Log writes nothing (9.873355ms)
✔ Not now stamps, clears keeps, and advances exactly once (15.093989ms)
✔ Keep counts once and saturates at 999 without reset (7.854676ms)
✔ Keep with a reason logs that reason in the Rotten Log entry (2.820255ms)
✔ Stay stamps the task, clears keeps, and records the prior rung count once (4.836929ms)
✔ WIP Step releases to Next and logs the transition in one transaction (2.262563ms)
✔ Ready Step writes priority, Schedule Log, and Rotten Log in one transaction (3.02312ms)
✔ Keep carries the logged history and preview keeps in its context (2.704915ms)
✔ Keep with a stale child log during the stage refuses and rebuilds (2.108463ms)
✔ Keep with advance commits once and advances exactly once (2.454355ms)
✔ Reword stamps, clears, logs, and never advances (2.737588ms)
✔ Drop cancels with the dropped-after-keeps reason and keeps history (3.868635ms)
✔ Drop writes Cancel Log and Rotten Log in one transaction (13.76267ms)
✔ Less often at 90+ opens the picker and dismiss writes nothing (9.231572ms)
✔ counted session skips at-limit and counts below-limit (8.831976ms)
✔ counted session skips at-limit on an early date (5.866527ms)
✔ counted session with every target skipped writes nothing (1.648332ms)
✔ real config loader offers P1 for Bryan's ladder without plugin.config (6.097413ms)
✔ missing config file disables Step and recommends Stay (7.683474ms)
✔ unreadable config file uses distinct copy (5.33789ms)
✔ malformed config uses distinct copy (2.251329ms)
✔ config without a priority property uses distinct copy (1.264563ms)
✔ opening the card writes nothing and shows the Stay row detail (27.826345ms)
✔ Esc on the rows closes the card and writes nothing (22.85835ms)
✔ Stay swaps the rows for the reason stage without closing (6.158856ms)
✔ repeat Alt+F never enters or submits the stage (3.341145ms)
✔ Esc in the stage returns to the rows; a second Esc writes nothing (4.255763ms)
✔ Stay stage Enter logs the reason with one transaction; one undo restores (30.173576ms)
✔ blank Stay stage Enter logs no reason given (17.234179ms)
✔ a double Enter submits once (16.404782ms)
✔ IME Enter never submits the stage (11.421164ms)
✔ the card header shows the logged count and last reason (5.842872ms)
✔ an unreadable log shows the header even with no countable entries (0.284092ms)
✔ the decay card Stay stage explains that the count restarts (0.557446ms)
✔ ambiguous Rotten Logs refuse the Stay write (4.244821ms)
✔ availability: decay on (or absent) may ask; decay off never asks (6.318335ms)
✔ trigger: only an explicit decide row decides (0.46693ms)
✔ partition: exact at-limit rows skip, everything else stamps (4.963817ms)
✔ partition: empty and malformed input stamps nothing and skips nothing (0.44947ms)
✔ partition: enabled false stamps decision rows (older namespace fallback) (0.464738ms)
✔ skip wording: singular, plural, and all-skipped notices (4.067173ms)
✔ reword cursor: lands at the end of the task body before metadata (16.720978ms)
✔ captured age: optional context ages, null when created is missing (0.958736ms)
✔ rows: Ready offers Step, Stay, Reword, Drop, Less often, and level picks (10.850721ms)
✔ rows: unavailable Step recommends Stay (1.399809ms)
✔ footer omits 1–4 when no level rows exist (0.426223ms)
✔ rows: invalid priority config disables Step and levels, keeps safe rows (1.947468ms)
✔ rows: picker-mode Less often and 365-day cap (1.924279ms)
✔ rows: terminal ladder steps with a same-level roll (1.46008ms)
✔ rows: lane and priority cards keep lane-only choices off the row set (1.891089ms)
✔ modal: Enter approves once; later keys cannot approve again (2.137545ms)
✔ modal: Enter follows the recommended Stay row when Step is unavailable (0.417436ms)
✔ modal: letter keys, Alt+F, Ctrl+Alt+F, and 1-4 activate the same actions as click (1.023448ms)
✔ modal: key repeat and modified keys never approve (1.510913ms)
✔ modal: the opening chord must be fully released before approval (0.497297ms)
✔ modal: Esc changes nothing — dismiss without a choice (0.263697ms)
✔ modal: unavailable actions cannot be chosen (0.288139ms)
✔ modal: a double callback applies once (0.440108ms)
✔ capability: the nav api exposes the card while loaded (1.118108ms)
✔ capability: unload drops the card so marks stop promising it (0.329732ms)
✔ ladder lookup: the first priority property wins, null without one (0.469873ms)
✔ stage entry resolves the line itself and refuses prose (55.328594ms)
✔ Ctrl+Shift+P on a BLOCKS line opens the owner's Blocks stage directly (9.933093ms)
✔ Ctrl+Shift+P hotkey path on a BLOCKS line opens the owner's Blocks stage directly (1.823926ms)
✔ Ctrl+Shift+Alt+B on a BLOCKS or Depends-On line opens the owner's Blocks stage (1.33127ms)
✔ Ctrl+Shift+P on a Depends-On line is unchanged forward behavior (0.694879ms)
✔ Ctrl+Shift+P on a plain child bullet and a nested Task Link are unchanged (3e359a6) (38.037669ms)
✔ forward counted mixed row in BLOCKED keeps the waits-on badge (3e359a6 order) (5.783302ms)
✔ api.blocks opens the stage and removes only a listed dependent (4.752816ms)
✔ api.blocks removeDependent on an owner with no ^id is not-a-dependent (0.818695ms)
✔ stage canonical order ranks #hide last ahead of the lane (0.879528ms)
✔ stage empty query shows same-note plus In Progress and Next only (11.187742ms)
✔ stage cap appends a type-to-search-more hint row (29.673849ms)
✔ stage BLOCKED rows carry waits-on counts and short guard reasons (5.668503ms)
✔ stage removal notices name the task description, not the block id (1.06857ms)
✔ stage Task Link batches keep Depends on without refusal (4.734206ms)
✔ stage batch cycle check runs on the post-batch graph (2.72925ms)
✔ stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke (153.910489ms)
✔ stage stale single add refuses and reopens (5.712258ms)
✔ Task Link Depends on focuses a linked note open in a background tab (0.889292ms)
✔ Task Link Blocks focuses the linked note and opens Blocks directly (7.984755ms)
✔ Task Link relation stages focus the linked note and open the requested direction (1.269957ms)
✔ LG21: L chords on Depends-On and BLOCKS lines open the owner's relation stage (8.316585ms)
✔ LG22: B chords on relation lines open the owner's Depends on or Blocks stage (1.312104ms)
▶ Task Link Depends on refuses clearly when the linked note cannot be focused
  ✔ focus reports success but the active view stays elsewhere (6.468722ms)
  ✔ focus reports failure (1.281489ms)
✔ Task Link Depends on refuses clearly when the linked note cannot be focused (8.821096ms)
✔ stage mirror burst keeps the baseline owner across an insertion above (1018.914882ms)
✔ stage mirror burst clears on a text-only line deletion (1009.999472ms)
✔ stage mirror vim dd clears the deleted line's owner (1005.570269ms)
✔ stage badge counts open prerequisites without a block id (28.705951ms)
✔ stage badge names the future scheduled date with no open prerequisite (7.319031ms)
✔ stage badge reads blocked with nothing waiting and no schedule (8.135576ms)
✔ stage vault batch with a stale row refuses and reopens (39.52851ms)
✔ stage opening builds 200/400/1000-task notes without cubic growth (84.344162ms)
✔ stage snapshots match standalone parsing across grammar vectors (10.699926ms)
✔ stage Warm-empty cache is ready without a vault fallback (1.340952ms)
✔ stage opening renders cross-note results with zero writes and cap (88.090866ms)
✔ stage CURRENT covers same-note, cross-note, blocked, and counted parents (2.833ms)
✔ stage collections reuse one snapshot per parent (0.957665ms)
✔ stage cold refresh yields, preserves state, and performs no search reads (159.658946ms)
✔ stage cold refresh abandons after dismissal or replacement (60.524516ms)
✔ stage 400-task opening finishes in a child process before the parent timeout (273.748062ms)
✔ stage ranker passes the DK contract vectors verbatim (7.32421ms)
✔ stage ranker tiers match the capture ranker tier order (0.800152ms)
✔ stage pool excludes daily notes, done, templates, and dot-dirs (0.856668ms)
✔ stage pool collects open vault tasks with buffers as given (7.288872ms)
✔ stage CURRENT resolves same-note, missing, closed, and non-task targets (5.808696ms)
✔ stage cycle guard reports the path back to the dependent (1.720227ms)
✔ stage view groups CURRENT, RESULTS, and BLOCKED with guards (5.814864ms)
✔ stage view disables cycles and unencodable targets, keeps +id rows (2.476557ms)
✔ stage cache tasks normalize across Tasks shapes, buffers win (2.403841ms)
✔ stage Task Link mode shows Depends on for one link and batches (1.705843ms)
✔ stage mark keys never collide across notes (0.376031ms)
✔ stage display-text locating matches one open task (0.593923ms)
✔ stage selection refusal spans tasks only (0.602913ms)
✔ stage builder composes pool, current, guards, and pill title (4.709976ms)
✔ stage counted vault add with a stale target refuses and reopens (56.596987ms)
✔ stage vault commit with a stale write notifies once and reopens (45.519031ms)
✔ commitVaultRefs refuses a cycle through implicit resident edges (12.715575ms)
✔ stage single remove with a stale write notifies once and reopens (17.493216ms)
✔ stage vault single +id guard refuses a stale target (6.11307ms)
✔ stage vault counted +id guard refuses a stale target (2.545248ms)
✔ stage single +id guard refuses a stale target (7.967161ms)
✔ stage counted remove with a stale write refuses and reopens (12.82372ms)
✔ stage counted remove counts only changed sources (32.736825ms)
✔ counted local add on [?] sources reads zero extra notes (24.086167ms)
✔ counted local toggle-off on a Pomodoro-linked [?] source recovers (27.843267ms)
✔ stage counted vault add counts only changed sources (16.560237ms)
✔ stage counted vault remove counts only changed sources (7.99778ms)
✔ vault counted same-note add follows BLOCKS shifts with post-plan stamps (9.123845ms)
✔ vault counted same-note remove follows BLOCKS deletions (16.379522ms)
✔ vault counted cross-note add keeps follow-up behavior (12.139682ms)
✔ stage +id row prompts without writing (36.644762ms)
✔ stage dismissal writes no bytes and drops the batch (5.473078ms)
✔ stage same-note batch commits in one undo group (26.929542ms)
✔ stage batch with a stale row refuses and reopens (3.570945ms)
✔ stage counted add applies to every source task (48.585864ms)
✔ stage batch cycle rows stay guarded and write nothing (31.813709ms)
✔ stage edit-task-dependencies registers with no default hotkey (3.753594ms)
✔ task-card-depends-on registers Ctrl+Shift+B and opens the Depends on row (3.189447ms)
✔ task-card-blocks registers Ctrl+Shift+Alt+B and opens the Blocks row (1.107848ms)
✔ stage waits-on badge counts open prerequisites only (4.179852ms)
✔ stage cycle tooltip shows task descriptions (6.550549ms)
✔ stage same-note single add stamps the dependent and keeps its cursor (12.05362ms)
✔ stage same-note marked batch stamps the dependent and keeps its cursor (9.277221ms)
✔ Tab marks a same-note CURRENT row and Enter removes it (38.882978ms)
✔ Tab twice unmarks a CURRENT row (29.662056ms)
✔ Tab mixed CURRENT removal and RESULTS add apply in one commit (36.955919ms)
✔ Tab marks a missing CURRENT target and the batch removes it (50.113037ms)
✔ Tab same-note and cross-note CURRENT removals apply in one vault batch (57.377711ms)
✔ cross-note add awaits preparation before the one commit (41.909151ms)
✔ a failed async preparation leaves the dependent untouched (11.503129ms)
✔ links to unloaded notes tolerate add, remove, and deleted targets (6.894332ms)
✔ Pomodoro-linked dependents recover through the plugin vault read (10.072415ms)
✔ same-note batch +id stamps the target and links in one undo group (19.165952ms)
✔ confirmBatchBlockId collects the id and executes the batch (3.928203ms)
✔ commitMarkedDependencies executes ready additions at once (4.247791ms)
✔ counted vault add links two siblings bottom-up (7.714446ms)
✔ counted CURRENT rows without a line remove from every source (10.851034ms)
✔ a stale editor between await and commit refuses (1.910657ms)
✔ removeDependencyByRef refuses targets that are not on the line (2.2738ms)
✔ kept unloaded links resolve the field id by line position (4.453852ms)
✔ pendingTargetLine commits the same-note target id with the link (4.644203ms)
✔ counted vault add commits every source in one transaction (8.29336ms)
✔ field-only clears snapshot the vault and recover (2.729636ms)
✔ adds without recovery read zero extra vault notes (1.679852ms)
✔ hand-edit clear recovers Pomodoro-linked dependents to Next (2.229182ms)
✔ hand-edit clear on a non-Blocked parent reads zero extra notes (1.054804ms)
✔ writer keeps the full route for duplicate basenames (5.708646ms)
✔ adds on Blocked parents and non-Blocked mirror touches read nothing (2.661221ms)
✔ counted vault add loads each source's existing links (7.493661ms)
✔ counted Ctrl+D on a blockquoted task refuses with the blockquote notice (1.240583ms)
✔ single Ctrl+D on a quoted task without a field refuses as a blockquote (0.409316ms)
✔ confirmSingleBlockId folds the target id into one transaction (4.354555ms)
✔ chooseTaskDependency folds a missing target id into one transaction (4.028698ms)
✔ counted remove commits every source in one transaction (6.725247ms)
✔ DP parse vectors accept, empty, malformed, and not-a-line (6.147557ms)
✔ DP30 attributes a Work-Log-nested Depends-On line to the inner task (3.978145ms)
✔ fenced lines never collect as Depends-On lines (2.703418ms)
✔ DW1 creates the line as the first child (10.772217ms)
✔ DW2 creates the line after a Cancel Log (2.022925ms)
✔ DW3-DW5 append, remove the middle, and delete on the last link (7.381394ms)
✔ DW6-DW7 re-add moves to the end and the field mirrors the line (1.077856ms)
✔ DW8 tab parents deepen the child by one tab (1.547216ms)
✔ DW9 space parents reuse the existing child indent (1.190399ms)
✔ DW10-DW11 CRLF and final-newline state survive (4.420473ms)
✔ DW12-DW14 link form is the shortest unambiguous form (0.582203ms)
✔ archive targets keep the explicit done/ path form (0.369847ms)
✔ DW15 an existing id is never rewritten (1.940463ms)
✔ DW16 an unencodable path without an id refuses (0.909225ms)
✔ DW17 field placement follows fresh and precedes the block id (0.739217ms)
✔ dependency edits leave child links outside the managed line alone (6.784023ms)
✔ DW19 variants canonicalise to the writer form (2.446137ms)
✔ adding an open prerequisite blocks the dependent (3.503922ms)
✔ adding transfers Next and In Progress commitment to the open target (1.338593ms)
✔ removing the last open prerequisite recovers immediately (1.487149ms)
✔ removal stays Blocked while another prerequisite is open (0.551474ms)
✔ removal stays Blocked with a future schedule (0.42539ms)
✔ one gesture commits the dependent note in a single transaction (21.781913ms)
✔ a failed preparation leaves the dependent untouched (0.941922ms)
✔ recovery references ignore child links outside the managed line (0.43258ms)
✔ task-block helpers find owners, lines, and insertion points (0.652366ms)
✔ dependency notices follow the contract shapes (0.263818ms)
✔ nav api v3 resolves results and never throws (2.578596ms)
✔ getDependencyInsertLine lands after a Cancel Log subtree (0.563313ms)
✔ planner: an ordinary dependent with a block id plus an open add yields one target (18.866567ms)
✔ planner: adding only a closed target yields none (2.271127ms)
✔ planner: no block id yields none (1.171261ms)
✔ planner: a dependent already [?] with an open add yields a target (3.837551ms)
✔ planner: a removal yields none (2.314768ms)
✔ planner: mirrorTouch emits no ordinary consumption target (1.193682ms)
✔ planner: ^prj keeps project targets and a deduplicated union (14.487381ms)
✔ suffix helper names the removed count and the failed follow-up (0.411289ms)
✔ applyDependencyEdit cross-file consumes live links and emptied entries (21.417082ms)
✔ applyDependencyEdit removes one live link and reports it (5.533391ms)
✔ applyDependencyEdit keeps the dependent write when the daily preimage changes (11.944942ms)
✔ same-file fold lands the dependency and the cleanup in one undo group (3.697129ms)
✔ setLocalTaskDependencyLink stays synchronous and folds same-file cleanup (6.326881ms)
✔ setLocalTaskDependencyLink cross-file continuation removes the live link (17.396963ms)
✔ same-note marked batch consumes every newly Blocked source (22.168533ms)
✔ counted same-note writer consumes every newly Blocked source (11.10669ms)
✔ counted vault writer consumes every newly Blocked source (12.380756ms)
✔ counted ^prj source consumes its project targets (15.532168ms)
✔ a dependent without a block id does zero cachedReads even when today's daily exists (3.868517ms)
✔ alignment key ignores fields, the block id, the status and trailing space (2.925763ms)
✔ insertion after a modified line edits that line and inserts after it (3.940607ms)
✔ adjacent prerequisite and parent both change while two lines insert (0.984646ms)
✔ deletion at the end of the document (0.9764ms)
✔ insertion at the top and at the end of the document (0.80296ms)
✔ empty documents align and apply (0.571917ms)
✔ CRLF documents insert and delete with CRLF (0.505517ms)
✔ equal-count shifted edits take the aligned path (1.322088ms)
✔ pure in-place edits keep the line-bounded change shapes (1.229004ms)
✔ an unchanged document writes nothing (4.048655ms)
✔ an explicit final cursor wins over the mapped cursor (0.772674ms)
✔ the machine-write annotation still reaches the transaction (0.476386ms)
✔ an editor without transaction falls back to bottom-up replaceRange (0.876292ms)
✔ positions map through aligned, changed, gap and deleted lines (0.555262ms)
✔ a deletion at the end of the document maps to the last line (2.614651ms)
✔ a gap with new lines maps by offset and clamps to its last line (0.947078ms)
✔ seeded property: planned changes rebuild the new text and map unchanged lines (84.593843ms)
✔ a diff past the edit cap becomes one unaligned gap (196.659859ms)
✔ the CM6 double reproduces the whole-document replacement jump (1.295313ms)
✔ first cross-note prerequisite keeps the cursor and the viewport (12.915251ms)
✔ same-note prerequisite directly above keeps the dependent's line (7.537485ms)
✔ removing the last prerequisite keeps the dependent's line (8.46554ms)
✔ a Blocks source gaining its first BLOCKS line keeps its line (1.638766ms)
✔ missing ledger-tools api refuses the review namespace (7.313668ms)
✔ review jump on an empty queue (2.112823ms)
✔ review jump from a queued task goes to the neighbor (4.703672ms)
✔ review jump wraps at the ends (0.539554ms)
✔ review jump from elsewhere goes to the first or last entry (0.535722ms)
✔ review jump matches a moved cursor task by text (3.402105ms)
✔ review jump from a just-stamped rank goes to the entry after it (0.472196ms)
✔ review jump skips just-stamped keys the lagging cache still shows (0.370138ms)
✔ review jump after stamping everything reports empty or wraps (0.416574ms)
✔ review queue line resolves at the entry line (0.809733ms)
✔ review queue line follows a moved line to its unique match (7.105473ms)
✔ review queue line goes stale on duplicates or a missing line (0.537218ms)
✔ review jump notices name the state (0.912996ms)
✔ fresh stamp targets refuse closed and recurring tasks (4.377969ms)
✔ fresh stamp batch stamps every target and nothing else (1.667998ms)
✔ one refusal refuses the whole fresh stamp batch (1.714795ms)
✔ a throwing stamper refuses the fresh stamp batch (0.44377ms)
✔ fresh stamp ignores the legacy Work Log summary (1.386787ms)
✔ blank Work Log summary and stamp refusal never create a log marker (2.321575ms)
✔ fresh stamp notices adjust the pre-write counts (0.498746ms)
✔ today detection only matches today's fresh field (0.629976ms)
✔ stamped refs match the pre-write queue by line or text (0.735333ms)
✔ review refresh keydown matches Alt+F in place and Ctrl+Alt+F to advance (0.487359ms)
✔ tier-aware jump notices name each tier (1.158017ms)
✔ projects tier walks with commitment rank and empty-project notice (4.929028ms)
✔ references tier walks with commitment rank and reference notice (1.308977ms)
✔ jump notices use reviewEntryView when provided and keep the fallback (0.682005ms)
✔ tier notices fall back without tier ranks and wrap on the last line (0.402999ms)
✔ boundary notice names commitments done and rotten next (0.30926ms)
✔ walk anchor records handled keys with their neighbors (1.371269ms)
✔ cursor on a live entry wins over a lagging anchor (0.516354ms)
✔ [s after a stamp goes backwards from the anchor (1.090031ms)
✔ release-then-]s continues from the anchor successor (0.480523ms)
✔ non-contiguous counted stamp advances past the last handled rank (0.572042ms)
✔ anchor wraps at both ends (0.688964ms)
✔ advance across NEXT to TICKLER to ROTTEN lands the boundary (0.797418ms)
✔ tier capability gates on the freshness namespace version (0.360009ms)
✔ empty queue notice reads the upkeep meter (0.206082ms)
✔ refresh row reads lane intervals from the api with the once-Ready return (4.096213ms)
✔ endpoint jumps select the queue ends with full rank and total (0.78883ms)
✔ endpoint jumps ignore cursor, anchor, and direction (0.573165ms)
✔ endpoint jumps on empty and one-entry queues (0.405355ms)
✔ a visited endpoint is still due under its own anchor (0.397368ms)
✔ lowercase steps continue from an endpoint anchor (10.068496ms)
✔ counted review jump repeat 1 matches omitted repeat (1.18934ms)
✔ counted review jump from the first entry lands N steps ahead (0.599345ms)
✔ counted review jump from the last entry wraps past the start (0.263489ms)
✔ counted review jump larger than the queue wraps once (0.271864ms)
✔ counted review jump on a one-entry queue stays there (0.300812ms)
✔ counted review jump with no origin lands on the Nth entry (0.275493ms)
✔ counted review jump from a shaped anchor takes N surviving successors (0.410538ms)
✔ counted review jump does not change endpoint selection (0.324509ms)
✔ a stamped endpoint that moved is stale and cannot land from old text (0.335567ms)
✔ stale endpoint target reselects the same endpoint in the new queue (3.490934ms)
✔ endpoint retry is bounded and failures preserve the anchor (1.025449ms)
✔ endpoint jump to ROTTEN carries no boundary preamble (1.495415ms)
✔ endpoint notices keep v4 tier details and legacy v3 text (2.48463ms)
✔ onload registers first/last commands routed to the shared jump (4.343451ms)
✔ jumpToDueTask consumes a pending Vim prefix as N review steps (2.20755ms)
✔ registered next-due-task callback reads the pending Vim prefix (1.96458ms)
✔ explicit jumpToDueTask repeat skips the Vim prefix (1.099713ms)
✔ non-normal editor with a pending prefix still jumps one entry (0.663117ms)
✔ stale counted replan reuses the captured repeat (0.603795ms)
✔ endpoint jump with a pending prefix still lands on the endpoint (0.483508ms)
✔ counted forward landing on ROTTEN keeps the boundary preamble (0.700251ms)
✔ PRE and POST are machine tiers; PRE is a commitment (0.404326ms)
✔ fallback notices name PRE checklist and POST closeout (0.456598ms)
✔ text-first cursor matching does not skip Pills after an above-insert (0.281388ms)
✔ day-scoped anchors from another day are ignored (0.432397ms)
✔ boundary into ROTTEN appends ]S when POST remains; into POST names commitments done (0.547524ms)
✔ ]S from ROTTEN reaches POST row one with 77 ROTTEN rows and a null budget (2.272344ms)
✔ nav normalizes a legacy v7 returned tier to tickler (0.186711ms)
✔ RECURRING is a machine tier, a commitment, and a v9 capability (0.255695ms)
✔ RECURRING counts in reviewWalkRemaining and gates the boundary (0.305364ms)
✔ matchReviewRecurringCursor is text-first like the checklist matcher (0.295363ms)
✔ fallback notices name RECURRING due detail with the reschedule hint (3.380461ms)
✔ Alt+F and Ctrl+Alt+F share the recurring refusal; Alt+Shift+F stays retired (0.264774ms)
✔ bobLineDigest matches the shared bob-cli vectors (13.654356ms)
✔ parseGoToTaskParams accepts a complete v1 link and ignores extra keys (2.138008ms)
✔ parseGoToTaskParams treats ref and block as optional (0.479151ms)
✔ parseGoToTaskParams rejects each malformed field (0.622628ms)
✔ vaultPathFromAbsolute maps inside the vault and strips a trailing slash on the base (0.575223ms)
✔ refindGoToTaskLine uses planned, block-id, unique digest, and clamped sources (3.341771ms)
✔ handleGoToTaskUri notices each malformed parameter (2.455013ms)
✔ handleGoToTaskUri notices a path outside the vault (1.47938ms)
✔ handleGoToTaskUri notices a missing file inside the vault (3.272211ms)
✔ handleGoToTaskUri maps a trailing-slash vault base (3.63026ms)
✔ handleGoToTaskUri prefers the open buffer over cachedRead (1.495389ms)
✔ handleGoToTaskUri re-finds by block id after an insert above the task (1.156277ms)
✔ handleGoToTaskUri re-finds a unique digest after a shift with no block (0.839472ms)
✔ handleGoToTaskUri clamps a duplicate digest and shows the changed-task notice (0.875265ms)
✔ handleGoToTaskUri clamps an out-of-range line without a notice when ref is absent (9.504761ms)
✔ handleGoToTaskUri reuses a leaf that already shows the note (6.382114ms)
✔ handleGoToTaskUri switches a Reading-view leaf to editing (4.113515ms)
✔ handleGoToTaskUri records a jump from the prior cursor and none without one (1.467291ms)
✔ handleGoToTaskUri never writes the vault or advances the walk (0.973994ms)
✔ handleGoToTaskUri reports when the note cannot be opened (0.591891ms)
✔ focusTaskMoveDestination still lands without switching Reading view (0.853594ms)
✔ onload registers both read-only navigation protocols when available (3.93309ms)
✔ onload skips protocol registration when the API is missing (0.943561ms)
✔ registered protocol handler forwards params to handleGoToTaskUri (0.823197ms)
✔ handleGoToTaskUri maps a path through realpath when prefixes differ (3.196988ms)
✔ cancel log grammar recognizes the marker, FE0F, and emoji-less spellings (5.276371ms)
✔ findCancelLogParent finds a direct child but ignores a grandchild (1.758898ms)
✔ getCancelLogEntryIndent reuses an entry indent or falls back to marker plus tab (0.555915ms)
✔ formatCancelLogEntryText renders the exact preview text (0.388286ms)
✔ planCancelLogEntry inserts a first-child log with tabs or spaces (3.376314ms)
✔ planCancelLogEntry prepends under an existing log wherever it sits (0.771763ms)
✔ planCancelLogEntry uses the fallback only when a marker exists (2.131723ms)
✔ isRecurringTaskLine and getTaskCancelStatusLabel cover the contract (0.925534ms)
✔ describeCancelTaskRow covers single, counted, link, recurring, and hidden (7.024889ms)
✔ planTaskCancelBatch cancels a single task with a first-child log (5.67217ms)
✔ planTaskCancelBatch upserts cancelled before the block id and preserves fields (1.240853ms)
✔ planTaskCancelBatch records id-field task identities (2.032677ms)
✔ planTaskCancelBatch skips closed targets and stays bottom-up (1.207185ms)
✔ planTaskCancelBatch refuses recurring targets in all three syntaxes (0.970289ms)
✔ planTaskCancelBatch handles empty reasons and stale preimages (0.969284ms)
✔ planTaskCancelBatch preserves CRLF line endings (1.010292ms)
✔ cancel project conversion carries the log and reports it (8.803834ms)
✔ getCancelTaskRowTitle names single, counted, and link sessions (2.517384ms)
✔ getCancelReasonHints labels Enter per state and Esc as Keep open (1.812219ms)
✔ the Cancel property item and the card's cancel row describe an open task (47.102626ms)
✔ Cancel row hides on closed tasks, plain bullets, and all-closed sessions (19.25978ms)
✔ Cancel row reports skipped closed targets in a counted session (3.729118ms)
✔ the card refuses the cancel row on a recurring task and stays on the card (7.885546ms)
✔ cancel reason stage previews the typed, empty, fallback, and :: cases (8.322234ms)
✔ cancel reason footer flips between plain, log, and fallback labels (2.191675ms)
✔ Esc from the cancel reason stage writes nothing (7.685627ms)
✔ single cancel writes [-], stamp, and first-child log in one transaction (24.23286ms)
✔ empty reason writes no log unless one already exists (14.281794ms)
✔ stale single preimage refuses with nothing written (9.252508ms)
✔ cancel writes [-] with no NOW chip (3.367677ms)
✔ TSC recovery runs with cancelled identities; a missing API still succeeds (19.809872ms)
✔ a throwing TSC API is skipped silently with no chip (6.724541ms)
✔ counted cancel skips closed targets and reports them (11.698232ms)
✔ same-file cancel folds today's Pomodoro prune into one transaction (20.05396ms)
✔ link session cancels the target and removes the invoking link bullet (12.792624ms)
✔ buildCancelNoticeModel text covers every chip (0.605762ms)
✔ renderCancelNoticeFragment builds the is-cancel card (1.443469ms)
✔ Ctrl+0 loads and focuses a deferred pinned dash tab without jumping or restoring (5.846589ms)
✔ Ctrl+0 from an unpinned dash copy switches to the pinned home tab (0.712966ms)
✔ Ctrl+0 stays on the pinned dash tab when an unpinned copy exists (0.596355ms)
✔ Ctrl+0 keeps the active dash tab when equal-ranked copies exist (0.439506ms)
✔ a pinned dash tab wins over an earlier unpinned tab (0.85289ms)
✔ a main-area dash tab wins over a pinned sidebar tab (0.513738ms)
✔ a deferred sidebar dash tab is reused when there is no main-area match (0.607122ms)
✔ a markdown saved state is considered even when the leaf is not deferred (0.557727ms)
✔ Ctrl+0 opens dash in the current tab when no matching tab exists (1.449174ms)
✔ Ctrl+0 leaves an already active dash tab alone (0.949482ms)
✔ isOpenPomodoroLedgerEntryLine recognizes every open status and rejects closed/indented/non-checkbox lines (2.455166ms)
✔ findPomodorosSectionRange excludes frontmatter and fenced headings and stops at the next heading (3.113955ms)
✔ collectPomodoroBlockLinkOccurrences captures embeds, aliases, same-note links, struck spans, and marker runs (1.131129ms)
✔ planDeferredPomodoroLinkCleanup is a clean no-op with no section, no open entries, or every entry closed (2.080386ms)
✔ planDeferredPomodoroLinkCleanup leaves entry lines, bullets outside the section, and struck links untouched (1.914533ms)
✔ planDeferredPomodoroLinkCleanup removes a dedicated link bullet and its nested children (2.027654ms)
✔ planDeferredPomodoroLinkCleanup removes an embed and resolves same-note and explicit-path-vs-basename links (1.132007ms)
✔ planDeferredPomodoroLinkCleanup skips an ambiguous basename as unresolved and never guesses (0.556468ms)
✔ planDeferredPomodoroLinkCleanup removes only the matched token on a mixed-content bullet and normalizes spacing (0.707739ms)
✔ planDeferredPomodoroLinkCleanup treats two matched links on one bullet as a single dedicated subtree deletion (3.092026ms)
✔ planDeferredPomodoroLinkCleanup consumes a stray Pomodoro marker with its link and skips fenced code (1.365678ms)
✔ planDeferredPomodoroLinkCleanup preserves CRLF line endings (0.649948ms)
✔ deferredPomodoroTargetsFromLines resolves block IDs and skips lines with none (0.659371ms)
✔ cleanup deletes a decorated dedicated bullet without leaving a stub:   - [ ] [[Tasks#^x]] # (0.536352ms)
✔ cleanup deletes a decorated dedicated bullet without leaving a stub:   - [/] 🍅 🍅 ![[Tasks#^x|alias]] # (2.249682ms)
✔ cleanup deletes a decorated dedicated bullet without leaving a stub:   - ![[Tasks#^x]] (0.384436ms)
✔ cleanup deletes a decorated dedicated bullet without leaving a stub:   - 🍅 [[Tasks#^x]] (0.410591ms)
✔ dedicated decoration check accepts paired strikes but cleanup never removes struck links (0.714947ms)
✔ cleanup deletes only touched childless entries, preserving prose, placeholders and closed history (0.839698ms)
✔ cleanup handles adjacent EOF entries ("\n", final newline false) (0.512161ms)
✔ cleanup handles adjacent EOF entries ("\n", final newline true) (0.444885ms)
✔ cleanup handles adjacent EOF entries ("\r\n", final newline false) (0.31471ms)
✔ cleanup handles adjacent EOF entries ("\r\n", final newline true) (0.260213ms)
✔ counted dependencies converge mixed sources and maintain one link per parent (36.139327ms)
✔ counted and single dependency gestures refuse inside a blockquote (DP29) (1.571421ms)
✔ counted dependency candidates exclude every source and expose mixed state (2.714212ms)
✔ counted dependency block-ID prompting is planned atomically (4.553782ms)
✔ counted dependency runtime applies target, parents, and navigation in one undo group (26.832938ms)
✔ counted Depends-on removal recovers residents with [unblocked::] (12.336959ms)
✔ counted Depends-on removal writes [unblocked::] through the wired freshness API (13.166551ms)
✔ cross-file toggle changes only the source link (3.844954ms)
✔ cross-file write failure still toggles only the source link (1.257485ms)
✔ line-local fallback applies bottom-up and preserves CRLF (2.061679ms)
✔ source line-count invariant rejects embedded newline changes (0.675504ms)
✔ pure toggle refuses when the source changed under it (0.512486ms)
✔ counted transclusion toggle evaluates each line independently (1.122694ms)
✔ transclusion toggle is refused on Depends-On lines (0.891467ms)
✔ transclusion toggles refuse generated BLOCKS lines with their notice (1.778321ms)
✔ task child links toggle as transclusions without dependency writes (0.959746ms)
✔ Ctrl+D on the Depends on row leaves unrelated child links as content (7.462228ms)
✔ Ctrl+D clears a field-only dependency without a line (2.431438ms)
✔ counted Ctrl+D on the Depends on row clears every targeted task (12.128817ms)
✔ findRemovedLineText reports deleted lines (0.379697ms)
✔ hand-edit mirror projects an edited line into the field (4.013645ms)
✔ hand-edit mirror canonicalises a hand-written line variant (2.121221ms)
✔ hand-edit mirror drops a linkless line and the field (2.247748ms)
✔ hand-edit mirror clears the field after the line is deleted (2.809483ms)
✔ hand-edit mirror leaves malformed lines alone (0.58306ms)
✔ hand-edit mirror ignores child links outside the managed line (1.136094ms)
✔ hand-edit mirror blocks when an open prerequisite is added by hand (2.378025ms)
✔ hand-edit mirror never transfers commitment to the target (3.308962ms)
✔ hand-edit mirror recovers when the last open prerequisite is removed by hand (3.183527ms)
✔ hand-edit mirror leaves a half-typed link alone (0.865205ms)
✔ hand-edit mirror clears the owning task when its last-child line is deleted (2.064557ms)
✔ counted add below a prerequisite follows BLOCKS shifts (bob-cli-95) (9.1043ms)
✔ counted remove follows BLOCKS deletions above the sources (12.217846ms)
✔ counted runtime commits once with the mapped first-source cursor (4.244284ms)
✔ mirror scheduler debounces at the contract interval (5.29477ms)
✔ mirror scheduler seeds the baseline from the update start state (12.93524ms)
✔ mirror scheduler keeps the first baseline and maps the owner across a burst (8.921215ms)
✔ mirror listener runs clear-field for a first-edit deletion with a following sibling (80.385231ms)
✔ mirror fire re-arms while the cursor stays on the edited line (19.693811ms)
✔ mirror scheduler reads changed ranges from the CM6 update (0.776473ms)
✔ mirror scheduler skips IME composition (0.425259ms)
✔ mirror scheduler skips open modals (0.504522ms)
✔ counted Ctrl+D clears every targeted task in one transaction with one notice (34.011632ms)
✔ counted N! refuses Depends-On lines with the Ctrl+Shift+P notice (5.506457ms)
✔ counted N! on only a Depends-On line refuses without writing (0.754074ms)
✔ promotion successor rows enumerate, classify, and key offers (39.311272ms)
✔ promotion successor keys disambiguate duplicate digests (1.039303ms)
✔ promotion planned links find the anchor in ledger order (3.679209ms)
✔ promotion picker model carries title, predecessor, group, and keys (0.879573ms)
✔ promotion notice line 2 covers every row of the table (1.175459ms)
✔ promotion history rewrites references one-to-one to #^prj (2.144023ms)
✔ PS1 promotion offers the new tasks and links only the pick (21.607366ms)
✔ PS3 Esc consumes the anchor without linking (4.249197ms)
✔ PS4 template placeholder consumes without a picker (3.516379ms)
✔ PS5 blocked project offers nothing and consumes links (3.909896ms)
✔ PS6 no planned link leaves children untouched (1.980988ms)
✔ PS7 struck, closed, prose, past, and later links are handled (13.042756ms)
✔ PS9 lagging open editor completes with open:false and late open (3.277645ms)
✔ PS11 source change during pick trashes the note (2.353329ms)
✔ PS13 lossy children and unresolvable Depends-On create nothing (3.699446ms)
✔ PS2 picking both keeps the sub-bullet under the first (2.956478ms)
✔ PS10 concurrent note edits still apply picks by key (4.307632ms)
✔ PS12 deleted pick applies the rest with a refusal suffix (4.942511ms)
✔ PS14 picker model shape and retarget off (2.742264ms)
✔ planTaskLaneBatch commits every Ready target to Next (5.594366ms)
✔ planTaskLaneBatch releases Next and In Progress to Ready (1.087875ms)
✔ planTaskLaneBatch logs a nonblank summary on released In Progress tasks only (3.419833ms)
✔ planTaskLaneBatch skips Blocked and refuses stale preimages (0.757864ms)
✔ buildLaneToggleNotice reports commit and release with and without budgets (0.861094ms)
✔ describeLaneRow covers task, counted, and link sessions (1.240118ms)
✔ toggleTaskLane commits Ready to Next and reports lane budgets (8.721199ms)
✔ toggleTaskLane releases to Ready without the api (4.064657ms)
✔ toggleTaskLane release logs the summary on In Progress tasks (2.664697ms)
✔ toggleTaskLane skips Blocked targets (1.719298ms)
✔ counted toggleTaskLane covers the current task plus the next N tasks (1.472146ms)
✔ toggleTaskLane on a Task Link writes through the open buffer (18.45208ms)
✔ toggleTaskLane on Task Links releases across notes (7.048205ms)
✔ toggleTaskLane refuses when a preimage changed (0.568873ms)
✔ Ctrl+Shift+P shows a pinned lane row that commits immediately (44.438912ms)
✔ Ctrl+Shift+P link mode shows the lane row with release detail (12.386226ms)
✔ Ctrl+Shift+P lane release with In Progress goes through the reason stage (6.634639ms)
✔ getLinkPickerSessionSubtitle keeps the clamp for a single link (1.069929ms)
✔ link-mode priority notice keeps via Task Links visible (1.673219ms)
✔ already-handled Alt+N leaves Vim state alone (1.435723ms)
✔ Alt+N fallback still dispatches once with the Vim count (2.431311ms)
✔ lane release deletes an emptied entry (cross-file, Alt+N) (7.395602ms)
✔ lane release deletes an emptied entry (cross-file, card) (7.037699ms)
✔ lane release deletes an emptied entry (same-file, Alt+N) (1.733745ms)
✔ lane release deletes an emptied entry (same-file, card) (5.009075ms)
✔ Task Link release deletes its entry in one undo group (separate, Alt+N) (7.989242ms)
✔ Task Link release deletes its entry in one undo group (separate, card) (4.228711ms)
✔ Task Link release deletes its entry in one undo group (folded, Alt+N) (1.612578ms)
✔ Task Link release deletes its entry in one undo group (folded, card) (6.337402ms)
✔ parseLinkPickerTaskLink recognizes dedicated Task Link bullets (13.670398ms)
✔ discoverLinkPickerTargets covers counted siblings and clamps at the Pomodoro end (4.623025ms)
✔ discoverLinkPickerTargets leaves #task lines to the regular picker (0.942891ms)
✔ findUniqueLinkPickerTargetLine vets missing, duplicated, non-task, and closed targets (3.403799ms)
✔ createLinkPickerPropertyItems shows dependsOn and aggregates common and mixed values (5.03257ms)
✔ getLinkPickerSessionSubtitle formats single, batch, and clamped subtitles (1.881613ms)
✔ bare link mode edits the task behind a Task Link through the open buffer (73.498486ms)
✔ counted link mode writes across notes through both the open buffer and the vault (16.962331ms)
✔ Task Link scheduled delete recovers a Blocked task through the wired freshness API (16.044144ms)
✔ link mode refuses the whole operation when a linked note changed (11.148066ms)
✔ link mode reports a closed target and changes nothing (5.260902ms)
✔ link mode defers to a future date, blocks the task, and prunes today (20.69039ms)
✔ bare Ctrl+Shift+P on a #task line keeps the existing task behavior (6.722292ms)
✔ Task Link scheduled write deletes its entry (separate) (13.475774ms)
✔ Task Link scheduled write deletes its entry (folded) (21.962484ms)
✔ folded Task Link scheduling maps the cursor past logs inserted before the emptied entry (15.955492ms)
✔ dash restore suppresses editor notice after deliberate navigation (23.73806ms)
✔ open-task dispatch timeout is registered for plugin cleanup (1.469648ms)
✔ jumpToOpenObsidianTask moves a placeholder Pomodoro entry in one undo group and reports the destination (9.916258ms)
✔ jumpToOpenObsidianTask swaps current and future Pomodoros in one undo group (2.769071ms)
✔ jumpToOpenObsidianTask keeps current-swap transaction failures local (1.617995ms)
✔ jumpToOpenObsidianTask refuses current-up without jumping or mutating (0.893875ms)
✔ jumpToOpenObsidianTask still jumps normally off past/cancelled Pomodoro entries, a sub-bullet, and a plain task line (3.348119ms)
✔ Ctrl+Shift+J/K dispatch guard performs exactly one Pomodoro move per physical press (6.105635ms)
✔ Ctrl+Shift+J/K dispatch guard performs exactly one current Pomodoro swap per physical press (1.547405ms)
✔ counted jumpToOpenObsidianTask moves a planned Pomodoro N positions in one undo group (3.410637ms)
✔ an impossible counted Pomodoro move refuses without jumping or mutating (8.911848ms)
✔ counted jumpToOpenObsidianTask still jumps off non-movable cursor contexts (1.473496ms)
✔ counted open-task jump on a sole current target keeps the existing notice (0.387615ms)
✔ dispatch guard allows exactly one counted Pomodoro move when the command route also fires (1.523128ms)
✔ bullet property picker reconciles duplicate bare and counted opens (40.344213ms)
✔ bullet property picker close lifecycle clears tracking for fresh sessions (25.107523ms)
✔ task move picker reconciles duplicate bare and counted opens (8.768084ms)
✔ task move picker close lifecycle clears tracking for fresh sessions (1.895808ms)
✔ Pomodoro bullet move picker opens sessions and clears the shared move picker slot (10.689615ms)
✔ Ctrl+Shift+M dispatcher preserves task moves and routes Pomodoro sub-bullets and entries (1.654231ms)
✔ move task command keeps Ctrl+Shift+M binding and calls the combined dispatcher (3.910927ms)
✔ commitPomodoroBulletMoveSession applies one guarded same-file transaction (6.153784ms)
✔ Pomodoro move notice identifies a newly created unconfigured theme (2.163219ms)
✔ Pomodoro bullet move picker confirms = through the actual picker callback (5.312643ms)
✔ Pomodoro bullet move picker reserves =NAME for peeling a named merged component (2.56034ms)
✔ Pomodoro bullet move picker confirms =email through the actual picker callback (2.916217ms)
✔ Pomodoro bullet move picker confirms = review through the actual picker callback (3.972214ms)
✔ Pomodoro bullet move picker confirms =focus by unnaming a single-name source (1.934927ms)
✔ Pomodoro bullet split stale-content guard does not write (0.876253ms)
✔ Pomodoro bullet move picker = cancellation, invalid rows, and stale-content guards do not write (1.739553ms)
✔ native isOpen regression: pickers attach, close clears slot, reopen works (5.405206ms)
✔ stale registered pickers fail open on the next key (7.466628ms)
✔ Task Card onClose clears card classes and resolving flags (1.566227ms)
✔ planPomodoroBulletMove appends one bullet last in an existing open Pomodoro, deleting the emptied source (13.036622ms)
✔ configured theme menu vectors scope Recent, preserve config order, and flag new names (51.447827ms)
✔ configured empty-query picker shows up to twelve configured themes (1.061566ms)
✔ planPomodoroBulletMove deletes the source when a counted move consumes every sibling, including a nested subtree (1.515147ms)
✔ planPomodoroBulletMove preserves the source when only some siblings move out (0.91848ms)
✔ planPomodoroBulletMove promotes a nested grandchild to the destination's child depth with its descendants (0.991397ms)
✔ planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (middle entry) (1.312633ms)
✔ planPomodoroBulletMove creates a fresh same-name destination from the = row without merging same-name entries (1.920747ms)
✔ planPomodoroBulletMove creates a new named Pomodoro at the deleted source's former position (only Pomodoro in section) (0.946404ms)
✔ planPomodoroBulletMove replaces a lone empty placeholder child and deletes the emptied source (5.916677ms)
✔ planPomodoroBulletMove merges an exact-duplicate single line, keeps a near-match distinct, and deletes the emptied source (3.831743ms)
✔ planPomodoroBulletMove reports a stale target, an unresolved destination, and an invalid new name (1.777147ms)
✔ planPomodoroBulletMove deletes the emptied source when the moved bullet merges away as a duplicate (0.765111ms)
✔ planPomodoroBulletMove leaves a destination's lone placeholder intact and still deletes the emptied source (2.117047ms)
✔ planPomodoroBulletMove moving a bullet out and back cannot restore a deleted source automatically (1.139761ms)
✔ planPomodoroBulletMove re-resolves an existing destination that sits before the deleted source (0.793249ms)
✔ planPomodoroBulletMove deletes both open and closed source entries the same way (0.80935ms)
✔ planPomodoroBulletMove deletes the first, a middle, and the last Pomodoro entry while preserving structure (0.649086ms)
✔ planPomodoroBulletMove preserves trailing-newline state and CRLF line endings when deleting the source (0.766779ms)
✔ planPomodoroBulletMove scope 'entry' appends every bullet in source order after a later destination's last child, deleting the source (0.977531ms)
✔ planPomodoroBulletMove scope 'entry' re-resolves an earlier destination after the source is removed (0.594317ms)
✔ planPomodoroBulletMove scope 'entry' carries a bullet's descendants and rebases them onto the destination's child indent (0.918387ms)
✔ planPomodoroBulletMove scope 'entry' merges an exact duplicate and keeps a near-match distinct (0.538943ms)
✔ planPomodoroBulletMove scope 'entry' replaces a destination's lone empty placeholder when something is inserted (0.506194ms)
✔ planPomodoroBulletMove scope 'entry' leaves a destination's lone placeholder intact when a forced target merges away (0.439361ms)
✔ planPomodoroBulletMove scope 'entry' plans a pure deletion for a childless entry and a placeholder-only entry (1.064611ms)
✔ planPomodoroBulletMove scope 'entry' rejects an unmoved non-blank line with the no-silent-loss guard (0.496941ms)
✔ planPomodoroBulletMove scope 'entry' rejects stale source/target lines, a same-entry destination, an unresolvable destination, and a 'new' destination (0.77365ms)
✔ planPomodoroBulletMove scope 'entry' deletes the first, a middle, and the last entry, preserving structure across LF/CRLF and trailing-newline state (3.318465ms)
✔ planPomodoroBulletMove scope 'entry' deletes closed and cancelled source entries the same way as open ones (0.930533ms)
✔ done-today themes stay Recent in bullet-move and entry pickers (46.813261ms)
✔ entry mode excludes a done source entry's own theme; bullets mode keeps it (3.781903ms)
✔ navigation Pomodoro picker renders theme accents and Ctrl+D only changes Recent suggestions (58.994501ms)
✔ Pomodoro entry move picker opens sessions, ignores counts, and clears the shared move picker slot (8.460458ms)
✔ commitPomodoroEntryMoveSession on an existing row applies one guarded move transaction (5.465555ms)
✔ commitPomodoroEntryMoveSession on a rename row applies one guarded transaction; unchanged writes nothing (1.832963ms)
✔ commitPomodoroEntryMoveSession on an empty-source move emits the deleted-Pomodoro notice (1.097182ms)
✔ commitPomodoroEntryMoveSession rejects a session whose editor content drifted or whose active view changed (0.663968ms)
✔ Pomodoro entry picker Ctrl+X merges the highlighted existing row and closes before committing (15.821025ms)
✔ Pomodoro entry picker Ctrl+X refuses rename and empty selections without closing or writing (1.600694ms)
✔ Pomodoro entry picker Ctrl+X uses the shared opening latch against reentrant merges (5.098868ms)
✔ Ctrl+X remains entry-specific and does not run from the Pomodoro bullet picker (8.001484ms)
✔ task move picker closes before commit while other pickers retain delayed close (1.791341ms)
✔ Pomodoro move picker previews the default merge, retype alternative, and Tab component live (40.405758ms)
✔ Pomodoro move Enter merges the type into the destination without a task-field write (11.29852ms)
✔ Pomodoro move Enter merges missing task types in move order and leaves fields alone (9.006625ms)
✔ moving the last linked merged-in type sheds it from the source Pomodoro (5.6583ms)
✔ Pomodoro move Alt+Enter applies a multi-bullet retype in one closed-note write (6.1508ms)
✔ Pomodoro move refuses a linked-note buffer changed after the footer preview (12.089006ms)
✔ Pomodoro move preserves types under labels and unnamed containers, and allows PLAN (4.313955ms)
✔ Pomodoro move landing in MEET retypes even on the default Enter path (1.587398ms)
✔ Pomodoro move to a new named entry merges by default (1.579188ms)
✔ Pomodoro move clears an explicit type that matches the inherited destination (1.220758ms)
✔ parsePomodoroEntryLine parses named/unnamed, placeholder/range, and open/closed shapes (4.472498ms)
✔ normalizePomodoroName uppercases, collapses whitespace, strips em dashes, and rejects empty/over-length (0.788515ms)
✔ formatPomodoroEntryLine emits a placeholder entry with or without a name (0.334786ms)
✔ createPomodoroBulletMovePickerRows excludes ineligible entries and handles create/invalid rows (6.590599ms)
✔ Pomodoro move pickers place recent themes around typed names and exclude today's themes (35.572837ms)
✔ createPomodoroBulletMovePickerRows maps = to a fresh source-name Pomodoro in bullet mode only (2.284501ms)
✔ createPomodoroBulletMovePickerRows = shortcut resolves named closed sources and rejects unnamed, missing, and invalid sources (2.702959ms)
✔ createPomodoroBulletMovePickerRows formats titles, metadata, and query matches (1.480489ms)
✔ buildPomodoroBulletMoveNotice formats counts, destinations, and suffixes (1.077397ms)
✔ buildPomodoroEntryMoveNotice formats moved/merged counts and the deleted-empty case (0.726491ms)
✔ createPomodoroBulletMovePickerRows 'entry' mode emits rename rows for novel/self names and existing-destination rows for other names (0.940828ms)
✔ createPomodoroBulletMovePickerRows 'bullets' mode is unchanged by the new options argument (0.704999ms)
✔ createPomodoroBulletMovePickerRows excludes the source and closed entries from destination rows in both modes, sharing the invalid row (0.941084ms)
✔ collectPomodoroEntries reports positions, open/name, child ranges, previews, and skips fenced/absent sections (1.058428ms)
✔ findPomodoroBulletContext resolves owning entries and rejects entry/blank/outside-section lines (8.46237ms)
✔ findPomodoroBulletContext leaves plain #task lines on the task-move route (0.867433ms)
✔ discoverMovablePomodoroBulletTargets collects bare/counted siblings, clamps, and isolates subtree and grandchild depths (1.656167ms)
✔ findPomodoroEntryContext resolves entry lines and rejects sub-bullet/heading/blank/outside-section lines (1.187969ms)
✔ discoverPomodoroEntryMoveTargets collects top-level children, drops empty placeholders, and allows a childless entry (1.770939ms)
✔ isMovablePomodoroEntryContext matches open current and future Pomodoro entries (8.054374ms)
✔ planPomodoroEntryReorder swaps the current Pomodoro down with the next future placeholder (1.990885ms)
✔ planPomodoroEntryReorder promotes a future Pomodoro up into the current slot (0.690966ms)
✔ planPomodoroEntryReorder preserves exact range text, status prefixes, and subtree ownership across current swaps (0.932247ms)
✔ planPomodoroEntryReorder preserves compact ranges, embedded metadata dashes, and placeholder whitespace (1.143804ms)
✔ planPomodoroEntryReorder handles counted current swaps and their inverses (1.036338ms)
✔ planPomodoroEntryReorder moves a named placeholder down, swapping with the next placeholder (0.751671ms)
✔ planPomodoroEntryReorder moves a placeholder up, swapping with the previous placeholder (0.574512ms)
✔ planPomodoroEntryReorder round-trips unequal-size blocks: down then up restores the original content (0.759288ms)
✔ planPomodoroEntryReorder round-trips a future-up swap across the current open entry (1.085433ms)
✔ planPomodoroEntryReorder refuses moving up past a closed or cancelled entry (1.175762ms)
✔ planPomodoroEntryReorder refuses moving down past the last placeholder in the section (0.552839ms)
✔ planPomodoroEntryReorder refuses both directions for a lone placeholder (0.807207ms)
✔ planPomodoroEntryReorder keeps a blank separator between two placeholders after the swap (0.35482ms)
✔ planPomodoroEntryReorder accepts the current timed entry but refuses closed or cancelled sources (0.547646ms)
✔ planPomodoroEntryReorder refuses illegal current/future spans atomically (1.27658ms)
✔ planPomodoroEntryReorder rejects a stale source line (0.441979ms)
✔ planPomodoroEntryReorder round-trips CRLF content (0.642713ms)
✔ planPomodoroEntryReorder leaves content outside the two swapped blocks untouched (7.538718ms)
✔ planPomodoroEntryReorder moves a named placeholder down three positions with its subtree (0.619127ms)
✔ planPomodoroEntryReorder moves a placeholder up three positions and round-trips (0.653995ms)
✔ planPomodoroEntryReorder keeps unequal gaps in their slots during a counted rotate (0.416732ms)
✔ planPomodoroEntryReorder refuses a counted move atomically at the planned-run boundary (4.45747ms)
✔ planPomodoroEntryReorder repeat 1 matches the uncounted plan and normalizes invalid counts (1.304545ms)
✔ planPomodoroEntryReorder counted plans preserve CRLF, line count, and outside bytes (0.572016ms)
✔ peelPomodoroMergedName removes every matching canonical plus component (5.822368ms)
✔ planPomodoroBulletSplit peels selected bullets into a new placeholder and preserves the source (12.846827ms)
✔ planPomodoroBulletSplit trusts non-trailing selections, keeps duplicates, and rebases nested siblings (1.904644ms)
✔ planPomodoroBulletSplit preserves closed source status, CRLF, trailing newline, and empty source entries (1.673382ms)
✔ planPomodoroBulletSplit refuses invalid, stale, unsupported, and missing-component sources without mutation (2.538614ms)
✔ planPomodoroBulletSplit peels first, middle, and last components and unnames a whole-name peel (6.103385ms)
✔ planPomodoroBulletSplit peels C++ components, clamps counted selections, and preserves mixed indent (2.282007ms)
✔ planPomodoroBulletSplit preserves ledger position, newlines, and future/timed/cancelled headers (12.42203ms)
✔ Pomodoro bullet move picker typing =NAME or Escape does not write (12.976638ms)
✔ planPomodoroEntryRename renames a named entry and names unnamed placeholder/timespan entries (0.956499ms)
✔ planPomodoroEntryRename normalizes the typed name and rejects empty/over-length names (0.591783ms)
✔ planPomodoroEntryRename reports unchanged when the normalized name matches the current name (2.373778ms)
✔ planPomodoroEntryRename rejects unsupported trailing content and a stale source line (0.488719ms)
✔ planPomodoroEntryRename renames closed and cancelled entries the same way as open ones (0.393331ms)
✔ Pomodoro rename preview counts retyped tasks and reports containers (3.008434ms)
✔ Pomodoro entry rename refuses a buffer changed after preview (1.520654ms)
✔ planPomodoroEntryMerge resolves all direction-table cases with survivor-first bullets and names (6.17031ms)
✔ planPomodoroEntryMerge handles empty placeholders, unnamed entries, equal names, plus names, and the name limit (3.067445ms)
✔ planPomodoroEntryMerge refuses stale, ineligible, two-timed, unsupported, and lossy merges without mutation (0.951385ms)
✔ planPomodoroTypeSplit moves the right type below the source in name order (12.013729ms)
✔ planPomodoroTypeSplit splits every merged-in type and carries nested subtrees (1.678637ms)
✔ planPomodoroTypeSplit keeps labels and still creates empty type slots (0.896365ms)
✔ planPomodoroTypeSplit refuses stale and malformed splits without editing (0.510615ms)
✔ mapPomodoroSplitCursor follows a moved bullet and keeps other lines (1.319347ms)
✔ split refusals teach without editing (0.515192ms)
✔ two-type notice names the split, count, and destination (0.421936ms)
✔ split picker offers All plus each merged-in type with counts, never the base (1.012608ms)
✔ Ctrl+S dispatch acts only on exactly Ctrl+S inside a Pomodoro block (1.713961ms)
✔ manager relative dates label today, yesterday, and older days (10.153992ms)
✔ manager duplicate pairs follow the near-duplicate rule (1.391486ms)
✔ manager rows separate views, hints, and reappeared flags (8.473335ms)
✔ manager rename input rejects empty names and composites (4.713429ms)
✔ manager badges unconfigured themes and disables config-owned pin colors (6.201284ms)
✔ manager rename preview formats files, entries, and state notes (0.989557ms)
✔ manager occurrences scan skips fences and non-Pomodoro bullets (1.412751ms)
✔ manager opens, cycles views, filters, and hides through the stubbed api (42.780041ms)
✔ manager refuses without the desktop api (0.604557ms)
✔ color modal pins hues and Auto through the stubbed api (3.465814ms)
✔ action modal jumps to actions with single keys when the filter is empty (8.466356ms)
✔ rename modal previews the dry run and applies one merge commit (2.784532ms)
✔ rename apply saves touched notes and refuses on a failed save (1.114603ms)
✔ occurrences modal lists daily notes and opens the entry (5.06733ms)
api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
✔ priority notice relative day helpers handle offsets ranges and icons (2.904577ms)
✔ priority notice model summarizes single counted and project writes (8.013364ms)
✔ priority notice renderer builds an accessible fragment (4.829053ms)
✔ priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens (28.317ms)
✔ priority notice falls back to one plain notice without a DOM (2.029808ms)
✔ priority notice falls back to plain text when fragment rendering fails (1.087557ms)
✔ priority scheduling rolls inclusively and clamps a random value of one (1.459132ms)
✔ priority value rows preserve config order and expose labels ranges and current state (2.253085ms)
✔ priority picker writes priority then rolled schedule in one guarded edit (49.349125ms)
✔ priority picker writes lowest priority with a wide rolled schedule (6.667942ms)
✔ priority picker replaces both existing values without duplicating fields (7.171816ms)
✔ counted priority writes keep the rolled date right of the priority (12.235205ms)
✔ priority picker writes project priority and schedule inline atomically (12.950817ms)
✔ counted priority picker rolls an independent schedule for every task (38.70149ms)
✔ counted priority planning keeps project schedules inline (14.519803ms)
✔ counted priority planning evaluates Blocked recovery per rolled date (13.645135ms)
✔ a counted priority batch writes one entry per task using each task's own previous level (16.753923ms)
✔ priority notice models carry the stored level value for the glyph (0.991999ms)
✔ ledger priority mark lookup guards version and render (0.380759ms)
✔ priority notice header reuses the shared mark when available (3.951274ms)
✔ priority notice keeps the Lucide icon without a usable mark api (6.384499ms)
✔ batch priority notice carries an assign chip (0.848377ms)
✔ a counted priority batch skips a task whose rolled date equals its current date (9.135926ms)
✔ counted priority runtime aborts a stale session without rolling writes (5.001413ms)
✔ scheduled picker pins a priority roll only for configured current priorities (57.101831ms)
✔ Ctrl+R replaces only the pinned priority roll and keeps it selected (18.209389ms)
✔ choosing a priority roll writes immediately with a deterministic reason instead of prompting (15.844134ms)
✔ counted scheduled picker requires one shared configured priority (24.70598ms)
✔ buildProjectSeedFromChildBullets: an ALL-CAPS bullet becomes a section only when it has nested list items (7.468936ms)
✔ buildProjectSeedFromChildBullets: a checked ALL-CAPS bullet stays a task even with nested list items (0.736477ms)
✔ buildProjectSeedFromChildBullets moves a direct-child schedule log under the project task (0.757563ms)
✔ buildProjectSeedFromChildBullets preserves schedule-log marker spellings and source order (0.533362ms)
✔ buildProjectSeedFromChildBullets keeps schedule-log boundary cases on the existing paths (3.384133ms)
✔ buildProjectSeedFromChildBullets leaves a nested schedule log under the converted child task (0.468986ms)
✔ buildProjectSeedFromChildBullets moves empty and deeply nested schedule logs without forcing task output (0.472896ms)
✔ buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and the schedule log (0.53644ms)
✔ buildProjectSeedFromChildBullets moves a direct-child work log under the project task (0.394631ms)
✔ buildProjectSeedFromChildBullets preserves work-log marker spellings byte-for-byte (0.565411ms)
✔ buildProjectSeedFromChildBullets keeps work-log boundary cases on the existing paths (0.74089ms)
✔ buildProjectSeedFromChildBullets leaves a nested work log under the converted child task (0.388546ms)
✔ buildProjectSeedFromChildBullets moves an empty work log without forcing task output (0.23677ms)
✔ buildProjectSeedFromChildBullets moves managed logs in source order without sorting by kind (0.344764ms)
✔ buildProjectSeedFromChildBullets routes mixed child blocks to tasks, sections, and both logs (0.409864ms)
✔ parseManagedTaskLogParentBullet accepts sixteen spellings, blockquotes, and rejects trailing text (0.509367ms)
✔ Rotten Log markers, history reading, formatting, and generic insertion (4.9527ms)
✔ parseManagedTaskLogParentBullet rejects emoji/label mismatches like parse_managed_task_log_marker (0.365535ms)
✔ parseScheduleLogParentBullet ignores a work-log marker so Ctrl+Shift+P cannot write into it (0.606903ms)
✔ normalizeProjectManagedLogLine falls back to one extra tab for mixed indentation (0.175158ms)
✔ parseProjectSectionBulletTitle rejects wikilinks, tags, block IDs, mixed case, snake_case, and inline code (0.234165ms)
✔ formatProjectSectionTitle title-cases without preserving acronyms and collapses whitespace (0.277725ms)
✔ insertProjectSectionNotes fills an empty existing section with a blank line then the notes (1.256993ms)
✔ insertProjectSectionNotes appends after the last nonblank line of a non-empty existing section, leaving trailing blanks and the header untouched (0.361831ms)
✔ insertProjectSectionNotes matches an existing header case-insensitively and keeps its casing (0.341538ms)
✔ insertProjectSectionNotes appends new sections at EOF in source order and preserves a trailing newline (0.43408ms)
✔ insertProjectSectionNotes does not add a trailing newline when the original content had none (0.322685ms)
✔ insertProjectSectionNotes preserves CRLF line endings for an existing section (0.346369ms)
✔ insertProjectSectionNotes creates a new section using the document's CRLF line ending (0.26107ms)
✔ buildProjectSeedFromChildBullets merges drawers with equally-normalized titles in source order (0.399998ms)
✔ a Bob-written drawer promotes to a title-case section and reverses to the same drawer key (17.64318ms)
✔ buildProjectSeedFromChildBullets splits a mixed child block into tasks and sections, preserving relative note depth verbatim (0.619597ms)
✔ buildProjectSeedFromChildBullets marks lossless false for content that fits neither a task nor a section, without losing the other tasks (0.25151ms)
✔ buildProjectContentFromTask appends TASKS drawer notes after the converted child tasks (1.057579ms)
✔ project conversion accepts blocked sources and extracts their managed dependency child (3.619604ms)
✔ project seeding keeps the inline date and identity on ^prj and tags open residents when blocked (2.07278ms)
✔ buildProjectContentFromTask inserts schedule-log lines directly under the project lifecycle task (0.856267ms)
✔ buildProjectContentFromTask inserts both managed logs directly under the project lifecycle task (0.469999ms)
✔ buildProjectContentFromTask reports managed-log insertion failure without blocking other seeding (0.283503ms)
✔ insertProjectManagedLogLines preserves CRLF line endings (0.202065ms)
✔ findProjectLifecycleTaskIndex skips frontmatter and fenced code blocks (0.38937ms)
✔ getProjectFromTaskNoticeText reports a singular/plural section count like the link chip (0.379795ms)
✔ getProjectFromTaskNoticeText reports moved log kinds in a fixed order (0.202323ms)
✔ forward conversion leaves the project Ready when only the source status was Blocked (0.769811ms)
✔ buildTaskBlockFromProjectNote restores the worked example and round-trips (20.890806ms)
✔ project reversal puts Depends-On first, keeps the inline date, and drops Sub-projects (7.035714ms)
✔ buildTaskLineFromProjectNote preserves status, tags, and fields (3.373575ms)
✔ getProjectReversalBlockId inverts the forward basename helper (0.546118ms)
✔ formatProjectReversalSectionTitle uppercases titles and rejects unsafe ones (0.585536ms)
✔ splitProjectNoteForReversal treats TASKS as the task section and keeps section order (1.641375ms)
✔ indentProjectReversalLine preserves relative depth and drops blanks (0.949631ms)
✔ buildTaskBlockFromProjectNote reports structure and frontmatter errors (3.003217ms)
✔ buildTaskBlockFromProjectNote keeps CRLF notes reconstructable (2.194805ms)
✔ rewriteBlockIdLinkOriginal accepts a target block ID and defaults to prj (2.065339ms)
✔ collectProjectNoteBacklinkClassification separates ^prj rewrites from other refs (1.327656ms)
✔ getProjectNoteToTaskNoticeText omits zero chips and uses no-child fallback (0.481058ms)
✔ convertProjectNoteToTask restores the parent task, rewrites links, and trashes the note (35.838574ms)
✔ project reversal recovers tagged residents when they leave a blocked project (12.756692ms)
✔ convertProjectNoteToTask separates the restored task from a count-only parent section (2.678801ms)
✔ createProjectNoteFromTask dispatches reverse only on a real ^prj line (8.59699ms)
✔ convertProjectNoteToTask refusals leave every file untouched (22.824269ms)
✔ planBlockIdLinkContentRewrites plans parent #^prj rewrites in memory (0.410176ms)
✔ convertProjectNoteToTask writes the parent first when it links to #^prj (13.565436ms)
✔ convertProjectNoteToTask removes today's live #^prj Pomodoro link when the parent is blocked (17.40659ms)
✔ convertProjectNoteToTask leaves every file unchanged when a #^prj rewrite target is missing (8.889826ms)
✔ convertProjectNoteToTask reports post-write failures without rolling back (2.489138ms)
✔ convertProjectNoteToTask keeps the project note when a link rewrite finds changed content (8.767299ms)
✔ convertProjectNoteToTask keeps the Pomodoro suffix when the daily rewrite fails (16.835741ms)
✔ v2 reading task opens its source_pdf in Highlights without writes (33.328614ms)
✔ every reading-task lane and #REF casing opens (18.744737ms)
✔ v1 tracker resolves a PDF link or falls back to its own source_pdf (10.699785ms)
✔ plain, embedded, struck, and 🍅 Task Links resolve reading tasks (20.101256ms)
✔ bare managed embed in a reference note resolves its embedded task (1.105361ms)
✔ ordinary lines, unresolved Task Links, fences, and outside focus delegate once (13.9847ms)
✔ identified reading tasks show notices without delegating (1.159884ms)
✔ unsafe source_pdf values are refused (12.750996ms)
✔ bundle launch retries with the app name, and reports stderr on total failure (1.471152ms)
✔ off macOS shows the selected notice and managed ref-note prose delegates (10.735753ms)
✔ pure helpers normalize and parse reference PDF paths (0.724599ms)
✔ command registration is custom-hotkey only (0.856447ms)
✔ nav api openReferencePdf hands a source_pdf to Highlights without version or vault writes (4.89217ms)
✔ nav api openReferencePdf settles to a reason instead of throwing (1.082541ms)
✔ reading tasks read with the book prefix, plain tasks unchanged (2.940233ms)
✔ near-miss spellings never pair and never prefix (0.470915ms)
✔ picker rows carry the book prefix in displayText (1.598302ms)
✔ managed reference rename modal and submit are refused (7.358173ms)
✔ legacy ref notes and non-ref notes still rename (4.073589ms)
✔ managed reference predicate checks path and non-empty source_pdf (0.458232ms)
✔ planCountedBulletPropertyBatch reports futureScheduledTaskLines for a mixed priority-roll batch (12.353041ms)
✔ planProjectTaskSchedules and planProjectScheduledUpdate report futureScheduledTaskLines including the ^prj line (3.025525ms)
✔ runtime: a future scheduled write prunes the task's live link from today's open Pomodoro (8.027095ms)
✔ runtime: a due (non-future) scheduled write does not touch today's Pomodoro links (5.028716ms)
✔ runtime: no daily note today still writes the schedule with no Pomodoro chip (0.803337ms)
✔ runtime: daily note preimage changed under the snapshot keeps the schedule and reports not removed (1.616854ms)
✔ runtime: vault.process throwing during the daily-note write is reported without throwing (2.166545ms)
✔ runtime: the daily note open in another editor is written through that editor in its own transaction (2.77467ms)
✔ runtime: re-running the same deferral gesture is idempotent (1.595ms)
✔ runtime: a counted scheduled batch prunes exactly the targets that land on a future date (14.368434ms)
✔ runtime: a ^prj project schedule prunes the propagated tasks and the ^prj link itself (10.727081ms)
✔ runtime: the source note being today's daily note folds the prune into a single editor transaction (5.446585ms)
api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
✔ bare future scheduled writes block only real supported open inline tasks (11.732166ms)
✔ single runtime transclusion toggle preserves viewport in one line transaction (4.728457ms)
✔ same-file runtime toggle changes only markers, never fields or statuses (1.219781ms)
✔ pure toggle leaves a cursor moved during the toggle where it landed (0.702773ms)
✔ counted runtime transclusion toggle preserves viewport and caret (3.72796ms)
✔ counted property runtime uses one transaction and preserves caret and viewport (7.567697ms)
✔ bare due schedule recovery is guarded and can change only task status (5.864529ms)
✔ counted due recovery applies Ready Next and In Progress in one transaction (20.918636ms)
✔ scheduled recovery aborts after an asynchronous source change (2.257294ms)
✔ counted property runtime aborts a stale batch without a transaction (0.856912ms)
✔ counted project scheduling writes an inline date and blocks tagged residents (8.52405ms)
✔ future project scheduling prunes resident links and an emptied Pomodoro (14.532822ms)
✔ single project scheduling recovers due residents through the gate (3.57345ms)
✔ single project schedule deletion removes propagated copies and recovers (3.01267ms)
✔ formatPriorityRollScheduleReason covers all four shapes (3.459012ms)
✔ the priority-roll picker row keeps range detail and stores the exact roll (2.558886ms)
✔ buildPriorityRollScheduleLog returns null when the roll does not move the date (1.793091ms)
✔ getPriorityRollFromLevelLabel resolves configured, absent, and unconfigured values (1.807551ms)
✔ a priority roll onto the current date writes the date but no log (39.836597ms)
✔ a typed reason on an unchanged date is still written (2.056285ms)
✔ schedule log bullet formatting and parsing round-trip with and without a previous value (2.161159ms)
✔ formatScheduleLogEntryText renders entry text without indent or marker (2.520809ms)
✔ schedule reason text normalization trims, collapses whitespace, and flags inline fields (0.557756ms)
✔ findScheduleLogParent finds a direct-child marker but ignores a nested grandchild's (2.26212ms)
✔ getScheduleLogEntryIndent reuses an existing entry indent or falls back to marker indent plus a tab (0.495327ms)
✔ planScheduleLogEntry creates, prepends, guards, and preserves blockquote context (1.689ms)
✔ planScheduleLogEntry extends a legacy on-disk log whose one existing entry is a sibling of the marker (2.390933ms)
✔ planScheduleLogEntry uses the fallback only when a marker exists (0.668386ms)
✔ a typed reason wins over the fallback (0.363023ms)
✔ the fallback is suppressed on an unchanged date (0.369661ms)
✔ no reason and no fallback still guards empty-reason (0.392177ms)
✔ getScheduleLogWriteOutcome maps plan outcomes for writers (0.36787ms)
✔ hasScheduleLogReasonInput detects a typed reason or a fallback-only payload (0.287047ms)
✔ counted scheduled reason logs one entry per changed task, prepends above an existing log, and skips unchanged tasks (4.026516ms)
✔ empty reason through the counted planner writes no schedule log entries (11.81908ms)
✔ a counted scheduled session logs only the tasks that already keep a log (0.840788ms)
✔ the counted notice wording distinguishes a fallback batch from a typed-reason batch (9.784982ms)
✔ setBulletPropertyValue writes an inline scheduled date plus a schedule log entry (0.890449ms)
✔ setProjectNoteScheduledValue writes a schedule log entry under the ^prj task (7.133851ms)
✔ priority bullet property config normalizes frozen levels and preserves existing shapes (5.1082ms)
✔ priority bullet property config rejects each invalid schema category once (2.195859ms)
✔ project scheduling targets the inline ^prj field (4.177406ms)
✔ local task properties are addable only on valid tasks but invalid metadata stays removable (0.880715ms)
✔ dependency parent write validation rejects stale, Pomodoro, and fenced parents (1.29504ms)
✔ counted property targets mean current plus N real tasks without wrapping (1.544064ms)
✔ counted property metadata distinguishes absent, common, and mixed values (1.569581ms)
✔ counted priority metadata reports labels for common and mixed values (1.263765ms)
✔ counted scheduled planning updates the motivating three tasks atomically (5.062757ms)
api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
✔ project schedule validation accepts only real YYYY-MM-DD dates (2.362791ms)
✔ source task schedule is extracted without losing task metadata (4.186059ms)
✔ source task schedule errors are focused and ambiguous fields fail (0.939531ms)
✔ project creation frontmatter never stores the task schedule (0.68322ms)
✔ future schedule labels use local date-only boundaries (1.482848ms)
✔ scheduled recovery selects current and newest earlier daily across gaps (1.314405ms)
✔ scheduled recovery ranks Blocked tasks from both ledgers and transclusion graph (26.513036ms)
✔ scheduled recovery defers incompatible status settings and ambiguous identities (1.143096ms)
✔ scheduled recovery honors custom open and closed Tasks status types (1.063524ms)
✔ scheduled recovery honors the configured Tasks global filter (0.988581ms)
✔ child picker schedule metadata reads the inline ^prj date (1.939091ms)
✔ task move destination schedule hydration reads cached ^prj content (1.125739ms)
✔ project lifecycle task classification requires unfenced #task with trailing ^prj (4.636853ms)
✔ valid Obsidian tasks require a standalone #task checkbox in real note content (0.420308ms)
✔ choosing a scheduled date enters the combined review without writing anything (67.777964ms)
✔ choosing a priority level does not enter the schedule review (50.021339ms)
✔ confirming an empty reason on a task with an existing schedule log appends an unexplained entry (38.304073ms)
✔ confirming an empty reason on a task with no schedule log writes only the date (12.92314ms)
✔ review stage getFilteredItems always returns exactly one synthetic preview item (6.426172ms)
✔ the review preview row previews the entry it will write (16.639577ms)
✔ the review footer flips between Skip optional logs and Apply schedule as the Reason changes (2.825013ms)
✔ closing the picker during the review clears pending schedule state and writes nothing (9.655835ms)
✔ scheduling Work Log eligibility requires Pending or Next #task lines (4.076743ms)
✔ single Pending explicit date opens one review and writes both logs (69.466846ms)
✔ single Next blank and whitespace summaries schedule without a Work Log (21.362575ms)
✔ Escape at the review writes nothing, with or without typed text (10.990225ms)
✔ Ready and Blocked explicit dates review the Reason with no Work summary field (11.758968ms)
✔ future scheduling on Pending marks Blocked but still writes the Work Log (8.057877ms)
✔ tomorrow date on Pending still offers the Work Log (7.649048ms)
✔ priority pick on Pending freezes its roll and offers the Work Log (16.4956ms)
✔ counted mixed statuses share one summary only on Pending and Next (30.513057ms)
✔ counted planner composes Schedule and Work Logs bottom-up above later targets (3.40108ms)
✔ counted planner writes a Work Log even when the date is unchanged (4.346147ms)
✔ scheduling Work Log ownership keeps nested logs and CRLF endings (4.321581ms)
✔ scheduling Work Log warns on :: and preserves Markdown (7.611292ms)
✔ stale task while reviewing refuses with no scheduling or log writes (6.414294ms)
✔ scheduling prompts never leak into lane or cancel stages (7.732896ms)
✔ nav-stamp: batch write shares one stamp across every target (15.656481ms)
✔ nav-stamp: prompt opened at 23:59 commits at 00:01 with the new date (7.007617ms)
api.freshness.markUnblockedLine is unavailable; recovered without [unblocked::]
✔ Pomodoro-marked links are not managed dependency bullets (3.241647ms)
✔ deleting inline scheduled metadata recovers Blocked targets by snapshot rank (9.033232ms)
✔ counted future scheduling blocks only supported open inline task statuses (3.920526ms)
✔ counted property planning rejects any stale source with no partial result (0.53769ms)
✔ counted project scheduling writes the ^prj inline date and blocks tagged residents (3.733733ms)
✔ moving a project schedule earlier replaces only exact old-date copies (0.86327ms)
✔ future project schedules block every open resident and consume review status (1.325303ms)
✔ due project dates recover residents through the gate and write unblocked markers (1.890751ms)
✔ schedule deletion removes only exact project-date copies and recovers residents (1.581637ms)
✔ dependency lines render one canonical Depends-On line per parent (2.212913ms)
✔ dependency IDs encode root and nested Markdown paths deterministically (4.160685ms)
✔ prompted block IDs truthfully replace legacy id fields (0.378596ms)
✔ dependency navigation identity comes from the managed line only (3.092386ms)
✔ retired dependency bullets are excluded from single and counted toggles (5.449431ms)
✔ dependsOn replacement accepts spaces around field name and separator (0.738519ms)
✔ task status helpers keep Blocked open but rankless (1.422243ms)
✔ a due project date with only closed Depends-On history strips the tag (1.920333ms)
✔ Ctrl+D with only closed Depends-On history strips the tag (0.900319ms)
✔ Ctrl+D with an open Depends-On link remaining keeps the tag (0.770554ms)
✔ counted ^prj schedule sessions write [unblocked::] when the writer is passed (1.063902ms)
✔ a due project date keeps the tag while ^prj holds Depends-On links (0.81988ms)
✔ a due project date strips the tag while a resident with its own reason stays Blocked (0.614023ms)
✔ Ctrl+D strips the tag while a resident with its own reason stays Blocked (0.605237ms)
✔ counted scheduled deletes recover with [unblocked::] when the writer is passed (0.50579ms)
✔ section-header navigation moves normally and cycles at boundaries (4.833978ms)
✔ section-header navigation wraps from beyond document boundaries (1.681637ms)
✔ section-header navigation handles single-header and no-header notes (3.717278ms)
✔ open-task navigation scan includes Ready In Progress and Next and excludes Blocked (1.240506ms)
✔ open-task navigation keeps existing Pomodoro ledger targets (1.150344ms)
✔ next and previous jumps skip Blocked tasks and wrap to an allowed task (3.793983ms)
✔ blocked-only notes and a sole current allowed task have no jump target (0.43394ms)
✔ counted open-task jumps select the Nth eligible target and wrap modulo the list (0.535854ms)
✔ counted open-task jumps keep sole-target and invalid-repeat behavior (0.616943ms)
✔ tab pin Vim action registers once and toggles only the active leaf once (14.384144ms)
✔ tab pin toggle fails safely without a supported active leaf (1.823468ms)
✔ close tabs left preserves pinned sibling tabs and refocuses active tab (1.292042ms)
✔ close tabs right preserves pinned siblings and ignores the left side (0.522138ms)
✔ close other tabs preserves pinned siblings on both sides (3.785233ms)
✔ close sibling tabs is a silent no-op when the scoped range is all pinned (0.708031ms)
✔ close sibling tabs honors every pinned leaf representation (0.558942ms)
✔ close sibling tabs treats throwing view state as unpinned (0.514048ms)
✔ tab pin Vim registration retries after adapter availability (3.338526ms)
✔ isPomodoroTaskLinkLine matches dedicated links under any Pomodoro entry (21.931307ms)
✔ isPomodoroTaskLinkLine refuses task lines, fences, and non-daily paths (1.705578ms)
✔ isPomodoroTaskLinkLine refuses Depends-On lines and prose links (4.10052ms)
✔ decideTaskLinkLaneMode starts when any target is Next (0.551758ms)
✔ taskLinkLaneRefusalFor renders every D5 refusal (3.397066ms)
✔ planTaskLinkLaneBatch starts Next targets and leaves the rest alone (3.619405ms)
✔ planTaskLinkLaneBatch pauses with one shared Work Log entry (2.131421ms)
✔ planTaskLinkLaneBatch applies the freshness stamp last (2.2377ms)
✔ planTaskLinkLaneBatch dedupes lines and refuses stale preimages (0.845175ms)
✔ buildTaskLinkLaneNotice renders start, pause, logs, skips, and budgets (1.798638ms)
✔ taskLinkLanePromptState drives the Move to Next prompt (0.606819ms)
✔ TaskLinkLanePromptModal submits, previews live, and cancels silently (4.153011ms)
✔ TaskLinkLanePromptModal renders the batch context card (1.443784ms)
✔ findUniqueLinkPickerTargetLine allowClosed resolves closed tasks (0.764203ms)
✔ L1: toggle starts a Next link, stamps, hints, and notices (8.221555ms)
✔ L2/L3: toggle pauses through the prompt, logging one shared entry (31.020403ms)
✔ L4: cancelling the prompt writes nothing and shows no Notice (1.803764ms)
✔ L5: both directions run the same toggle twice for a round trip (3.037656ms)
✔ L6: Ready, Blocked, done, and cancelled targets are refused (7.592589ms)
✔ L6: missing targets keep the existing resolver error (0.656347ms)
✔ L7: a counted start flips every Next sibling and leaves In Progress alone (4.128993ms)
✔ L8: a counted pause prompts once and skips Blocked with a count (4.793723ms)
✔ L9: an over-long count clamps at the entry end without error (5.084083ms)
✔ L10: a closed-entry history line toggles the task and keeps the line (1.34356ms)
✔ L11: a target edited while the prompt is open refuses stale (6.676873ms)
✔ L12: an embedded Pomodoro link takes the two-state toggle (1.334049ms)
✔ L14: the same task linked twice in a batch is written once (2.255358ms)
✔ L15: a second toggle while one is in flight is swallowed as busy (1.373557ms)
✔ toggle on a non-link line refuses without writing (1.881011ms)
✔ api.taskLinkLane is a frozen v1 namespace that never throws (10.467282ms)
✔ the progressMarks hint is a no-op without the ledger-tools api (0.796628ms)
✔ task move records one Vim jump and round-trips without extra writes (40.23869ms)
✔ counted task move records a single jump to the first moved task (2.974116ms)
✔ deferred task landing re-anchors and records the resolved cursor once (16.331378ms)
✔ failed task move preserves seeded history including the forward branch (4.319895ms)
✔ post-commit open failure keeps the move committed with no jump (3.210721ms)
✔ a newer move supersedes a pending landing without stale placement (12.593996ms)
✔ shared destination helper without a move context records no jump (1.098932ms)
✔ task moves carry the Depends-On line and repath stranded same-note links (21.539588ms)
✔ task moves keep pathless links when the target moves along (2.009562ms)
✔ counted task moves discover movable tasks without wrapping or examples (2.249ms)
✔ task move ranges preserve quoted subtrees and collapse overlapping selections (1.102421ms)
✔ task move removal handles disjoint ranges, blank seams, and CRLF (2.435647ms)
✔ task move destinations include areas and only open projects (2.387178ms)
✔ moves into a blocked project leave closed tagged lines alone (12.508109ms)
✔ moves into a blocked project promote open prerequisites to the moved lane (8.135777ms)
✔ task move insertion preserves exact task and section spacing (6.568497ms)
✔ task move planning migrates identities and links across every affected note (9.024575ms)
✔ task move planning exposes a destination anchor for area destinations and counted moves (1.778603ms)
✔ task move into a blocked project tags the moved task and consumes today's live Pomodoro link (7.188429ms)
✔ task move out of a blocked project recovers through the shared gate and writes the unblocked mark (7.018633ms)
✔ move promotion walks through a ^prj target without raising it (4.631806ms)
✔ move promotion walks through a [?] ^prj to its open prerequisite (1.756065ms)
✔ move promotion uses each open task's own lane, not the strongest moved lane (2.544519ms)
✔ move promotion skips Depends-On lines of closed tasks (2.514019ms)
✔ task move planning rejects destination collisions and malformed identities (0.950122ms)
✔ resolveTaskMoveDestinationLine resolves via planned, block-id, text, and clamped fallbacks (1.716897ms)
✔ focusTaskMoveDestination opens the destination file and anchors the cursor (2.664718ms)
✔ focusTaskMoveDestination returns false without moving the cursor when the open fails (2.690807ms)
✔ focusTaskMoveDestination re-anchors by block ID when the destination content drifted (0.661546ms)
✔ physical task move chord declines auto-repeat and consumes Vim normal input once (1.883374ms)
✔ counted task move dispatch keeps its count through cold async destinations (40.426398ms)
✔ counted task move dispatch with warm async destinations opens one counted picker (7.427762ms)
✔ bare task move command ignores stale Vim count outside normal mode (1.438938ms)
✔ bare task move command opens one uncounted target in Vim normal mode (0.638653ms)
✔ already handled task move event leaves pending Vim state alone (0.271949ms)
✔ counted task move command dispatch counts Pomodoro sub-bullets once (16.420977ms)
✔ physical transclusion toggle owns bare and counted Vim normal input (3.539474ms)
✔ runtime task move writes destination before source and rolls back source failures (6.150597ms)
✔ runtime task move groups open-editor source and destination changes (4.039126ms)
✔ Ctrl+Shift+M runtime move preserves bracket and parenthesis theme fields (5.729554ms)
✔ runtime task move guards destination, auxiliary, and rollback failures (5.88984ms)
✔ task move insertion separates the section's first task from preamble and placeholders (1.33246ms)
✔ task move insertion keeps populated sections compact and second moves stable (0.420074ms)
✔ task move planning separates a counted move into a count-only section (0.818883ms)
✔ runtime counted move into a count-only section focuses the first moved task (2.859967ms)
✔ absent local key with folder template writes the trigger and one notice (4.31877ms)
✔ existing local object keeps other keys and only adds the trigger (0.649504ms)
✔ stored true is already-enabled with no write and no notice (0.84787ms)
✔ stored false is device-opt-out with no write and no notice (0.397294ms)
✔ mode none and blank folder templates skip as no-creation-templates (0.475217ms)
✔ regex mode with a non-empty file template enables (0.456222ms)
✔ legacy settings without a mode key skip as legacy-templater (0.319932ms)
✔ missing Templater plugin or settings skip as no-templater without throwing (0.374419ms)
✔ missing loadLocalStorage or saveLocalStorage returns without throwing (1.416755ms)
✔ string or array stored local values skip as unknown-local-shape (0.763811ms)
✔ saveLocalStorage throw shows one failure notice and does not escape (0.879127ms)
✔ planTemplaterLocalTrigger covers helper cases and never adds extra keys (0.489751ms)
✔ unblocked model returns null when there is nothing to show (6.540869ms)
✔ unblocked card renders a single linked row with receipt and chips (7.967543ms)
✔ unblocked card renders several linked rows with one entry (1.057986ms)
✔ unblocked card renders a created continuation with next up (0.970948ms)
✔ unblocked card renders recovered-only and still-blocked rows (1.998602ms)
✔ current offer summaries report pulled-in, unselected, mixed destinations, and new reasons (5.436973ms)
✔ project pull-in rows label empty projects and preserve project blocking reasons (5.376591ms)
✔ unblocked card caps visible rows with +N more (4.072352ms)
✔ unblocked card renders the breaker variant (7.656686ms)
✔ unblocked card renders the failure variant (0.792502ms)
✔ unblocked rows open their task without dismissing the notice (11.093586ms)
✔ unblocked row without a block id opens the note path (1.957075ms)
✔ unblocked card omits the plan chip when daily content is null (0.620444ms)
✔ unblocked notice shows one card with duration through showNotice (0.644892ms)
✔ unblocked notice falls back to plain text without a DOM (2.530548ms)
✔ unblocked text truncates to 48 characters with an ellipsis (0.281051ms)
✔ nav api exposes additive notice v3 and keeps version 3 (4.159173ms)
✔ unblocked stylesheet scopes notice overrides and uses task tokens (1.79933ms)
✔ keep-moving card: one pick reads as a Keep ‹N› moving card with ⏭, the lane, and no 🔓 or 'unblocked' (5.6396ms)
✔ keep-moving card: several picks, created sessions, several destinations, and several projects (3.165774ms)
✔ keep-moving lane names come from the status symbol: Pending, Next, Ready, Blocked (0.281899ms)
✔ keep-moving notices are silent when nothing was picked, and unpicked rows never render (0.427272ms)
✔ a mixed card keeps the 🔓 forms, counts keep-moving picks as linked, and renders them last with the chip (2.051127ms)
✔ a keep-moving failure keeps the failure text and an older model without keep_moving is unchanged (4.582687ms)
✔ keep-moving notice falls back to its plain ⏭ line without a DOM (0.597043ms)
✔ pull_in counts that include keep-moving offers never bring back the 🔓 forms on a keep-moving card (0.500012ms)
✔ keep-moving title and suffix helpers follow the copy table (0.266414ms)
✔ keep-moving stylesheet uses only existing tokens inside the scoped notice and picker blocks (1.446987ms)
✔ relation card: one pick reads as a ‹Label› “‹T›” card with 🪢 and no 🔓 or 'unblocked' (2.506206ms)
✔ relation card: several picks, parked receipt, and mixed 🔓 forms with a chip (4.353861ms)
✔ relation notices are silent when nothing was picked, and held/uncertainty use muted copy (1.021491ms)
✔ an older model without relation_successors is unchanged under notice v3 (0.3924ms)
✔ relation stylesheet uses only existing tokens and no new hex values (6.130172ms)
✔ physical Ctrl+Shift+J/K consume a Vim count once and pass it to the shared route (14.966215ms)
✔ open-task command ids omit repeat so the shared route resolves the pending Vim count (4.193317ms)
✔ command-route jumpToOpenObsidianTask consumes a pending Vim count for a planned Pomodoro move (10.895833ms)
✔ command-route jumpToOpenObsidianTask consumes a pending Vim count for a current Pomodoro swap (1.622408ms)
✔ command-route jumpToOpenObsidianTask consumes a pending Vim count for a circular jump (2.578733ms)
✔ dispatch guard applies a command-route Vim count when the capture route fires second (2.178776ms)
✔ dispatch guard leaves pending Vim state untouched when the capture route already consumed the count (1.887396ms)
✔ command-route jumpToOpenObsidianTask without a pending count moves one step and does not reset Vim state (7.064802ms)
✔ command-route jumpToOpenObsidianTask keeps repeat 1 for non-Vim and wrong-mode editors (16.527731ms)
✔ command-route jumpToOpenObsidianTask resolves the count from the passed editor, not a foreign pane (2.6804ms)
✔ explicit jumpToOpenObsidianTask repeat wins over a different pending Vim count (7.798429ms)
✔ getPendingVimRepeat falls back to prefixRepeat and motionRepeat when getRepeat is absent (1.053091ms)
✔ physical counted property chord consumes only explicit normal-mode Vim counts (1.331164ms)
✔ counted Ctrl+Shift+L on a Task Link reaches the relation opener (2.66191ms)
✔ physical counted relation and dependency chords route or refuse by direction (1.16662ms)
✔ Alt+N release samples the commit clock after the summary prompt (31.063526ms)
✔ linked release shares one commit stamp across notes (1.242326ms)
✔ Move to Next samples the commit clock after its prompt and previews live (41.991342ms)
✔ Task Card lane release preview and commit sample live clocks (25.399602ms)
✔ scheduling Work Log preview samples the render-time clock (7.808437ms)
✔ inbox route gate delayed across a minute writes the post-route stamp (2.227803ms)
✔ blank and cancelled summaries write no Work Log (1.951679ms)
✔ onload registers the palette command without a default hotkey (11.700427ms)
✔ an embed and a plain image link open the resolved vault resource (9.530039ms)
✔ vault image viewer receives origin lookup and a guarded restore snapshot (1.430035ms)
✔ no image, a missing image, and Reading view show notices without opening (1.219078ms)
✔ a second command invocation is ignored while the viewer is open (0.980844ms)
✔ closing restores focus and leaves an unchanged selection and scroll alone (1.133612ms)
✔ closing restores moved selection and scroll only while the source view is active (1.872915ms)
✔ unload closes the active viewer without restoring editor focus (1.418766ms)
✔ origin copy uses the tilde display path in every recorded state (10.43903ms)
✔ copy falls back to the absolute vault path or URL (1.365066ms)
✔ y waits for origin lookup before writing the clipboard, even before image load (5.395368ms)
✔ r does not restore or notify after the viewer closes during origin lookup (1.807269ms)
✔ y does not write the clipboard or show UI after the viewer closes during origin lookup (0.836492ms)
✔ a clipboard write finishing after close does not recreate toast UI or timers (1.095773ms)
✔ r restores from a deferred origin while the viewer stays open (1.195096ms)
✔ copy failure shows an orange refusal pill without raising a Notice (12.293318ms)
✔ r reports each unavailable origin state in the viewer pill (5.100044ms)
✔ fixed attachments API response renders origin and restores the image link (7.02109ms)
✔ lookup failures stay distinct from a missing origin (3.940365ms)
✔ image zoom key chips override built-in kbd backgrounds (43.611766ms)
✔ successful r replaces only the picked link in one undoable transaction (0.761993ms)
✔ r refuses a changed line and does not edit (0.514535ms)
✔ restore chip only appears for a present origin and toast pills replace one another (0.589198ms)
✔ origin line renders each recorded state below the title (0.879766ms)
✔ imported viewer shows the longer import pill (0.418494ms)
✔ detection accepts every bullet marker, plain lines, and nesting (8.457068ms)
✔ detection accepts wrappers, file://, spaces, and uppercase extensions (0.593871ms)
✔ detection rejects checkboxes, prose, and non-path lines (0.345226ms)
✔ detection raises Not an image for a path-only bullet with a non-image extension (4.077796ms)
✔ Z on an image-path bullet imports through bob with via zoom (66.872837ms)
✔ Z in a fence never imports and keeps the no-image notice (5.267234ms)
✔ Z on a line with both an embed and a path opens the embed (7.54522ms)
✔ Z on a non-image path bullet raises its notice without importing (9.835733ms)
✔ import success rewrites the bullet in one transaction and opens the viewer (7.403982ms)
✔ import of a reused file links the existing viewer pill (1.760369ms)
✔ import without the ledger-tools api raises its notice and edits nothing (0.479456ms)
✔ import failure raises Couldn't import with bob's message (0.418479ms)
✔ import of a non-image kind raises Not an image (0.345041ms)
✔ import refuses a changed line and names the saved file (0.548127ms)
✔ a second Z while importing is ignored (4.967065ms)
✔ Z then r round-trips the bullet back to its display path (14.01653ms)
✔ parser finds vault embed with size hint (3.336648ms)
✔ resolved target preserves the picked source span for the restore gesture (1.742638ms)
✔ parser finds plain image wikilink and blockquoted embed (0.363623ms)
✔ parser ignores callout bracket and finds the embed (0.46777ms)
✔ parser ignores image links inside single and double backticks (1.536663ms)
✔ non-image wiki targets are recognized but not candidates (0.398721ms)
✔ parser finds two image refs and lines with no refs (0.507189ms)
✔ parser handles Markdown angle, title, and balanced parens (0.719365ms)
✔ picker uses containing, next, then previous rule (0.798723ms)
✔ resolution records sourcePath and resolves duplicate basenames (1.749418ms)
✔ resolution handles relative, unicode, and space names (0.640144ms)
✔ missing file, non-image cursor, and fenced lines show exact notices (0.62926ms)
✔ vault resolution calls getResourcePath with the resolved file (0.366678ms)
✔ http embed passes through and non-image urls are not candidates (0.764412ms)
✔ remote URLs keep original bytes while titles decode once (1.08118ms)
✔ escaped Markdown parentheses resolve to the unescaped vault file (0.502056ms)
✔ vault percent escapes decode exactly once (0.393019ms)
✔ extensionless http(s) needs Markdown image syntax (1.937897ms)
✔ fit never exceeds 1 and respects padding for landscape, portrait, and tiny images (3.591297ms)
✔ min and max bounds follow fit, 1:1, and the max factor (0.667749ms)
✔ stepping clamps at both bounds (1.701441ms)
✔ zoom-at-point keeps the point fixed (0.449694ms)
✔ clamp centres small axes and limits large ones (0.534751ms)
✔ key Escape → close (1.762286ms)
✔ key q → close (1.923503ms)
✔ key Q → close (0.375864ms)
✔ key Ctrl+[ → close (0.751222ms)
✔ key Z → close (0.570376ms)
✔ key y → copySource (0.519692ms)
✔ key r → restoreSource (0.193655ms)
✔ key Shift+Y → ignore (0.213949ms)
✔ key Ctrl+y → ignore (0.214586ms)
✔ key Meta+y → ignore (0.238472ms)
✔ key r → ignore (0.34787ms)
✔ key r → ignore (0.260193ms)
✔ key + → zoomIn (0.249092ms)
✔ key = → zoomIn (0.121049ms)
✔ key Shift+= → zoomIn (0.163188ms)
✔ key Shift++ → zoomIn (0.183964ms)
✔ key - → zoomOut (0.398343ms)
✔ key 0 → fit (0.25199ms)
✔ key 1 → actual (0.149665ms)
✔ key h → pan:left (0.214853ms)
✔ key j → pan:down (0.152994ms)
✔ key k → pan:up (0.107247ms)
✔ key l → pan:right (0.087096ms)
✔ key Shift+H → pan:left (0.11659ms)
✔ key Shift+J → pan:down (0.604169ms)
✔ key Shift+K → pan:up (0.168036ms)
✔ key Shift+L → pan:right (0.118026ms)
✔ key ArrowLeft → pan:left (0.153246ms)
✔ key ArrowDown → pan:down (0.14495ms)
✔ key ArrowUp → pan:up (0.1249ms)
✔ key ArrowRight → pan:right (0.259907ms)
✔ key Shift+ArrowLeft → pan:left (0.153082ms)
✔ key Ctrl+q → ignore (0.177168ms)
✔ key Meta+z → ignore (6.735174ms)
✔ key Meta+Z → ignore (0.178465ms)
✔ key a composing → ignore (0.09926ms)
✔ key a keyCode 229 → ignore (0.108217ms)
✔ key x → ignore (0.165014ms)
✔ keys before arming are ignored (3.937655ms)
✔ Z closes after arming, and a repeated Z does not (1.112699ms)
✔ load sets fit state and dimensions (1.164048ms)
✔ a load error shows a notice, closes, and calls onClosed once (0.69234ms)
✔ Escape closes once, unregisters the scope handler, and aborts the signal (0.514599ms)
✔ q closes once, unregisters the scope handler, and aborts the signal (0.359206ms)
✔ Q closes once, unregisters the scope handler, and aborts the signal (0.388624ms)
✔ Ctrl+[ closes once, unregisters the scope handler, and aborts the signal (0.331354ms)
✔ Z closes once, unregisters the scope handler, and aborts the signal (0.371777ms)
✔ a stray x key changes nothing (0.581114ms)
✔ the app's vault stubs throw and are never called (0.90682ms)
✔ task-card-gate arms only on open inbox tasks (7.529405ms)
✔ task-card-gate header shows the Inbox chip only when armed (17.30597ms)
✔ task-card-gate priority: cancel writes nothing (2.365379ms)
✔ task-card-gate priority: stay runs today's write (0.616869ms)
✔ task-card-gate priority: move writes then moves (1.218485ms)
✔ task-card-gate scheduled: cancel writes nothing (0.416369ms)
✔ task-card-gate scheduled: stay runs today's write (1.441182ms)
✔ task-card-gate scheduled: move writes then moves (0.443603ms)
✔ task-card-gate generic-property: cancel writes nothing (1.016686ms)
✔ task-card-gate generic-property: stay runs today's write (0.558545ms)
✔ task-card-gate generic-property: move writes then moves (0.400216ms)
✔ task-card-gate refresh-interval: cancel writes nothing (0.38463ms)
✔ task-card-gate refresh-interval: stay runs today's write (0.298056ms)
✔ task-card-gate refresh-interval: move writes then moves (0.267701ms)
✔ task-card-gate refresh-custom: cancel writes nothing (0.312718ms)
✔ task-card-gate refresh-custom: stay runs today's write (0.27479ms)
✔ task-card-gate refresh-custom: move writes then moves (0.302407ms)
✔ task-card-gate clear-priority: cancel writes nothing (0.25898ms)
✔ task-card-gate clear-priority: stay runs today's write (0.239905ms)
✔ task-card-gate clear-priority: move writes then moves (0.293064ms)
✔ task-card-gate recommended-roll: cancel writes nothing (0.359198ms)
✔ task-card-gate recommended-roll: stay runs today's write (0.211589ms)
✔ task-card-gate recommended-roll: move writes then moves (0.384237ms)
✔ task-card-gate recommended-decay: cancel writes nothing (0.195808ms)
✔ task-card-gate recommended-decay: stay runs today's write (0.281646ms)
✔ task-card-gate recommended-decay: move writes then moves (0.254802ms)
✔ task-card-gate counted-roll: cancel writes nothing (0.200675ms)
✔ task-card-gate counted-roll: stay runs today's write (0.302737ms)
✔ task-card-gate counted-roll: move writes then moves (0.259675ms)
✔ task-card-gate lane-toggle: cancel writes nothing (0.184831ms)
✔ task-card-gate lane-toggle: stay runs today's write (0.210485ms)
✔ task-card-gate lane-toggle: move writes then moves (1.350503ms)
✔ task-card-gate dependency-single: cancel writes nothing (0.27642ms)
✔ task-card-gate dependency-single: stay runs today's write (0.15991ms)
✔ task-card-gate dependency-single: move writes then moves (0.280015ms)
✔ task-card-gate dependency-marked: cancel writes nothing (0.147126ms)
✔ task-card-gate dependency-marked: stay runs today's write (0.153609ms)
✔ task-card-gate dependency-marked: move writes then moves (0.168565ms)
✔ task-card-gate dependency-vault: cancel writes nothing (0.1126ms)
✔ task-card-gate dependency-vault: stay runs today's write (0.472769ms)
✔ task-card-gate dependency-vault: move writes then moves (0.197352ms)
✔ task-card-gate dependency-counted: cancel writes nothing (0.160342ms)
✔ task-card-gate dependency-counted: stay runs today's write (0.175478ms)
✔ task-card-gate dependency-counted: move writes then moves (0.296486ms)
✔ task-card-gate negative rows never prompt (1.185732ms)
✔ task-card-gate counted sessions capture N targets (0.562244ms)
✔ task-card-gate walk: move advances once with Moved first (0.349662ms)
✔ task-card-gate walk: move failure falls back to card with partial (0.764836ms)
✔ task-card-gate walk: exactly one settle per origin (33.66094ms)
✔ task-card-gate route outcome resolves like lane and link-today (0.513237ms)
✔ inbox classifier covers the inbox contract (3.93926ms)
✔ isInboxNotePath matches the inbox contract through the vault (2.672467ms)
✔ isInboxNotePath is false without an inbox note and never throws (0.422807ms)
✔ route destinations drop every inbox note, the source, and templates (1.902807ms)
✔ inbox-route destinations omit vault-sync conflict copies (0.860111ms)
✔ route preflight accepts a live area destination (9.898442ms)
✔ route preflight refuses stale and colliding destinations (4.725787ms)
✔ route picker resolves move, stay, cancel, and close exactly once (12.17011ms)
✔ route picker footer names the move, the hatch, and the way back (2.550839ms)
✔ route picker preflight refusal keeps the picker open with a notice (32.129337ms)
✔ route picker honors the shared move-picker guard (6.319061ms)
✔ promptInboxRoute moves, stays, and cancels with suspend pairing (6.822049ms)
✔ commitInboxRoute moves the verified task with its children (16.077588ms)
✔ commitInboxRoute into a blocked project tags the moved task (5.810061ms)
✔ commitInboxRoute moves a counted run and refuses on identity drift (3.839193ms)
✔ reviewOutcomeResolves treats route like lane and link-today (0.512676ms)
✔ nav api inboxRoute v1 delegates, shapes, and never throws (2.900616ms)
✔ history records ordered locations with file identity and dedupes adjacent repeats (6.993194ms)
✔ transition records origin then destination and truncates forward only on success (5.877281ms)
✔ history retains at most 100 locations and refreshes the live tip (1.154268ms)
✔ rename updates paths and delete prunes without corrupting the index (1.860517ms)
✔ bridge wraps add once, mirrors native jumps, and preserves the original call (2.648592ms)
✔ bridge without a jump list preserves keys and emits one compatibility diagnostic (0.58682ms)
✔ registration maps Ctrl+O and Ctrl+I in normal mode only and leaves Tab alone (5.025423ms)
✔ Enter A->B round-trips with Ctrl+O and Ctrl+I (37.030922ms)
✔ counted Enter returns to the original cursor, not the counted link line (21.595052ms)
✔ picker choice records one jump and cancellation records none (26.246638ms)
✔ stale picker origin is rejected and failed opens record nothing (23.912153ms)
✔ Backspace shares the link path and no-link lines fall through (21.194833ms)
✔ counted traversal honors boundaries and new jumps replace the forward branch (1.265576ms)
✔ ordinary motion before back is preserved for forward restore (0.786999ms)
✔ deleted entries are skipped and heading links settle before recording (30.764343ms)
✔ native fallback runs with empty history and boundaries never replay natives (1.142283ms)
✔ unload restores the native add and keeps a foreign later mapping (0.922851ms)
✔ exact eligibility authorizes one due-Ready ROTTEN row (3.372599ms)
✔ exact eligibility authorizes a TICKLER row (0.349137ms)
✔ exact eligibility refuses every stale-cache shape (1.130081ms)
✔ exact eligibility authorizes due rows on every rung and refuses the rest (0.602194ms)
✔ legacy refs still match line-only while exact refuses (1.473343ms)
✔ keeps support needs namespace v5 with keepLine (0.333081ms)
✔ decay decisions need namespace v6 with keepLine (2.136164ms)
✔ batch forwards per-target counted decisions to the stamper (2.814986ms)
✔ batch keeps legacy index targets uncounted (0.449087ms)
✔ a throwing stamper refuses the batch with no partial write (1.561181ms)
✔ parseKeepsCount reads the first valid value only (0.54974ms)
✔ countFreshStampKept measures actual increments only (0.738517ms)
✔ fresh stamp notice tails kept increments without promises (0.529594ms)
✔ duplicate source targets dedupe to one write (0.348682ms)
✔ single Alt+F increments an exact due-Ready ROTTEN task (18.162266ms)
✔ single Alt+F preserves NEW, lane, and early tasks without counting (5.925683ms)
✔ same-day repeat stays identical and counts nothing (1.514057ms)
✔ WIP Alt+F without prior fresh stamps with no Work Log prompt (1.517259ms)
✔ uncounted lane refresh stamps quietly with no Work Log (1.922294ms)
✔ a refusing counted target refuses before the Rotten Log prompt (1.271135ms)
✔ quiet WIP refresh advances; cancelled or stale keep prompts write nothing (4.781921ms)
✔ stale queue match stamps uncounted and never inflates (2.116875ms)
✔ counted Alt+F increments every exact target once (12.358766ms)
✔ stale editor source refuses with no write (2.045766ms)
✔ single-note write lands in one editor transaction and keeps CRLF (2.311591ms)
✔ v5 without keepLine fails without writing (0.479158ms)
✔ throwing v5 keepLine refuses the batch with no partial write (1.305299ms)
✔ pre-v5 ledger stamps uncounted through the old stamper (1.243174ms)
✔ Task Link session skips an at-limit decide target (6.412223ms)
✔ Task Link refresh counts one exact target (3.696778ms)
✔ duplicate Task Links to one target stamp and count once (2.242544ms)
✔ counted Task Link sessions route Pending, counted, and Next answers to separate logs (3.877175ms)
✔ counted Task Links dedupe targets and stamp with no Work Log prompt (2.077007ms)
✔ multi-note stale preimage refuses with no writes (2.150865ms)
✔ a linked note changed during the Keep prompt refuses before any write (1.910709ms)
✔ multi-note write failure rolls back the first note (3.271711ms)
✔ partial rollback is reported and a same-day retry does not duplicate the logged keep (7.973367ms)
✔ one physical key through two routes stamps once (3.890372ms)
✔ Ctrl+Alt+F capture advances once and consumes a Vim prefix (2.137256ms)
✔ obsolete and extra-modifier F chords stay unconsumed (0.81088ms)
✔ live Ctrl+Alt+F double dispatch asks once on a due WIP task (2.135808ms)
✔ live Alt+F double dispatch asks once on a due WIP task (1.76654ms)
✔ already-handled refresh keydown leaves Vim state alone (0.536036ms)
✔ formatLaneRouteActionLabel maps the lane mode (2.603968ms)
✔ Task Card inbox lane labels: Ready commits, Next and Pending release (5.887655ms)
✔ Task Card counted lane labels follow the batch probe (4.000429ms)
✔ a commit on an inbox Ready task routes with the picker title and moves on Enter (34.925735ms)
✔ a release on an inbox Next task labels release to Ready, then moves (4.79423ms)
✔ a Pending release prompts for the Work Log first, then routes (6.047119ms)
✔ Esc on the Pending Work Log prompt opens no picker and writes nothing (2.17595ms)
✔ route Esc writes nothing and shows no notice (3.234782ms)
✔ Shift+Enter gives today's in-place write with no move (1.983259ms)
✔ a counted run routes N tasks with one composed toast (16.149072ms)
✔ a counted route picker subtitles N tasks (3.039252ms)
✔ a failed move after the lane write settles lane plus the partial notice (6.248415ms)
✔ a routed commit settles route through a walk origin (2.495766ms)
✔ a non-inbox note writes today's bytes with no prompt (1.502293ms)
✔ a project filed under an inbox never prompts (1.139722ms)
✔ closed and Blocked-only tasks keep today's refusal with no prompt (3.996118ms)
✔ Alt+N on a Task Link line never prompts (6.362017ms)
✔ planner: cursor on an entry steps ±1 (8.503337ms)
✔ planner: duplicate-text rows resolve by proximity (3.807616ms)
✔ planner: anchor whose key survives steps from it (0.731748ms)
✔ planner: anchored task that left the walk continues by tuple insertion (1.361214ms)
✔ planner: yesterday anchor is ignored (0.479275ms)
✔ planner: no origin lands on first/last, wrap sets wrapped (2.278131ms)
✔ planner: counts work including wrap during a count (0.670714ms)
✔ planner: empty list returns empty (0.336254ms)
✔ planner: ]w from the last NEXT entry lands on READY 1 (2.439426ms)
✔ planner: last READY wraps to PENDING 1 (0.91025ms)
✔ planner: READY tuple insertion continues from the gap (0.548777ms)
✔ planner: lane-change from a released NEXT task stays in NEXT (0.635684ms)
✔ planner: lane-change uses tuple insertion when the key is listed in another lane (0.497032ms)
✔ planner: a cursor on a different live entry still wins over lane-change (2.519514ms)
✔ lane jump: ]W PENDING → NEXT 1, NEXT → READY 1, READY → PENDING 1 wrapped (4.891922ms)
✔ lane jump: [W reverse, including PENDING → READY 1 wrapped (0.424097ms)
✔ lane jump: from mid-lane [W lands on the previous lane's first task (0.331913ms)
✔ lane jump: empty lanes are skipped (0.274013ms)
✔ lane jump: one non-empty lane lands on its first task, wrapped (0.372086ms)
✔ lane jump: an emptied origin lane steps to its neighbours (0.394017ms)
✔ lane jump: no origin lands on the first / last non-empty lane (0.298791ms)
✔ lane jump: counts cycle along occupied lanes (0.314473ms)
✔ lane jump: lane-change origin uses the anchor's lane (0.29981ms)
✔ lane jump: yesterday anchor is ignored (0.246622ms)
✔ lane jump: empty list returns empty (3.39941ms)
✔ runtime: same-note landing places cursor and leaves review state untouched (9.610632ms)
✔ runtime: three queued presses land three different entries in order (4.499276ms)
✔ runtime: stale line re-reads once, then shows the changed notice (0.556897ms)
✔ runtime: review lock swallows the press silently (0.342792ms)
✔ runtime: missing or old api shows the required notice (0.492353ms)
✔ runtime: unavailable reasons show their notices and never the empty card (2.505794ms)
✔ runtime: no vault write happens (0.522314ms)
✔ runtime: jump-to-next-lane / jump-to-prev-lane are registered; first/last are gone (7.193685ms)
✔ runtime: counted ]W consumes the count before any await (4.028678ms)
✔ runtime: lane jumps use the lane planner on stale retry (0.611765ms)
✔ runtime: unknown-lane entries are dropped (0.533926ms)
✔ toast: model and text for pending, next, wrapped, work log, created (0.725526ms)
✔ toast: READY model uses the Alt+N next hint (0.304796ms)
✔ toast: ambiguous or malformed work log means no chip (1.919933ms)
✔ toast: rail switches past 30 entries and empty variants read correctly (0.772223ms)
✔ toast: renderer emits is-ready with an empty box, gaps, and current-lane (1.6869ms)
✔ toast: bar mode has three segments, current-lane class, caret in the current segment (3.189246ms)
✔ toast: empty variants render review, today-only, and none (0.871107ms)
✔ toast: previous lane-walk notice is hidden and fallback text is used (0.421793ms)
✔ identity: lane keys match the queue key helper (0.248034ms)
✔ nav-stamp: readLatestWorkLog parses stamped and legacy entries (0.884693ms)
✔ nav-stamp: laneWalkWorkLogLabel renders chip with and without time (0.202133ms)
✔ nav-stamp: formatWorkLogStamp truncates seconds and zero-pads (5.319309ms)
✔ cross-note open saves and verifies editor text before opening, then cancels the debounce (14.947586ms)
✔ the navigation API gives ledger-tools the same guarded active-leaf open (5.059367ms)
✔ a rejected save keeps the source note open and stops navigation (0.974381ms)
✔ a disk/editor mismatch keeps the source note open and stops navigation (3.721114ms)
✔ a landing with the source text raises the clobber warning and stops (0.633202ms)
✔ the delayed tripwire catches a disk overwrite after a clean landing (33.427895ms)
✔ an open that lands in another leaf skips the landing clobber check (2.387181ms)
✔ a dropped open skips the landing clobber check (0.436686ms)
✔ same-note opens and activation of an existing leaf never save (5.833777ms)
✔ parseBobOpenNotesParams accepts indexed entries and ignores unknown keys (6.971667ms)
✔ parseBobOpenNotesParams rejects every malformed URI field (1.12514ms)
✔ invalid batches show one notice and open nothing (6.416493ms)
✔ path mapping follows a symlink realpath into the vault (16.017345ms)
✔ new-tab policy reuses existing tabs and the active empty tab, keeping order and primary active (9.472595ms)
✔ an absent or outside entry fails independently and a PDF opens without landing (2006.167339ms)
✔ a resolved note that is not open waits until its captured digest is cached (75.333003ms)
✔ a per-entry open failure does not prevent later notes from opening (1.569134ms)
✔ waits for a newly created vault file and a late visible line digest (64.892207ms)
✔ re-finds a moved digest on any line, including prose and Pomodoro rows (5.029532ms)
✔ deadline fallback opens near the planned line and reports a changed capture (2004.444881ms)
✔ truncation reports how many of the full list opened (0.877405ms)
✔ serializes quick URLs and leaves the later URL active (2.518937ms)
✔ primary landing flashes briefly, secondary landings do not, and the handler is read-only (16.851083ms)
✔ onload registers bob-open-notes beside bob-goto-task (10.542278ms)
✔ a non-file sidebar view is not reused as an empty tab (0.951483ms)
✔ a true empty tab is reused for the first entry (0.68233ms)
✔ three new tabs follow entry order in the tab strip (0.92843ms)
✔ two tabs of the same note reuse the first matching leaf (4.896632ms)
✔ a missing file does not scan vault lists when getAbstractFileByPath exists (2000.608857ms)
✔ new tabs append at the far right when the middle tab is active (1.672358ms)
✔ a reused tab stays put while a new one is appended (1.710747ms)
✔ a deferred tab is reused and findMarkdownLeafByPath sees it (1.554298ms)
✔ a deferred sidebar leaf whose saved state names the note is not reused (0.962312ms)
✔ a loaded main-area match beats an earlier loaded sidebar match (6.761034ms)
✔ a new tab goes to the end of the main group when a sidebar leaf is active (1.422942ms)
✔ falling back without createLeafInParent still opens a new tab (0.828482ms)
✔ falling back when createLeafInParent throws still opens a new tab (5.364788ms)
✔ planner replaces quoted, single-quoted, and unquoted parent wikilinks (6.157244ms)
✔ planner reports previousTarget before the alias and keeps trailing comments (0.874112ms)
✔ planner collapses a block list parent and keeps the next key (0.932015ms)
✔ planner inserts a missing key, creates frontmatter, and keeps CRLF (0.917233ms)
✔ planner refuses unclosed, duplicate, stale, and unquotable values (0.616462ms)
✔ planner ignores indented, similarly named, and body parent lines (0.686778ms)
✔ planner replaces a Templater parent value and no-ops the same link (0.504174ms)
✔ ranking uses exact > prefix > word-start > substring > path > fuzzy (2.369084ms)
✔ ranking prefers the current parent, kind weight, children, and recency (19.390111ms)
✔ isConflictsNotePath matches an exact _conflicts path segment (1.983382ms)
✔ ranking excludes self, descendants, and _conflicts, and caps at 50 (1.417929ms)
✔ empty-query order is current, up a level, recent, then popular (0.803285ms)
✔ ancestry stops at 16 hops and on repeats, breadcrumbs collapse at 5 (1.107884ms)
✔ excluded-only matches use the cycle empty-state text (0.591165ms)
✔ unquoted parent cycles are detected at commit time (0.573665ms)
✔ collectChildNotes hides _conflicts copies and _generated notes (2.889806ms)
✔ change-parent-note is registered with Ctrl+Shift+- (4.182694ms)
✔ opening the panel pre-fills the parent name, selects it, and shows ancestry (22.244384ms)
✔ vault.process commit writes the canonical parent and notices the change (4.293837ms)
✔ editor commit issues one transaction and does not call vault.process (5.218734ms)
✔ choosing the current parent is a no-op (1.547121ms)
✔ a commit-time cycle is refused after the tree changes (2.190364ms)
✔ a stale expectedRaw is refused (2.451757ms)
✔ a second command press focuses the open panel (1.165256ms)
✔ no active markdown file uses the existing notice (0.389461ms)
✔ footer hints and empty-state copy match the spec (0.296072ms)
✔ prev labels are exact or open with ‹ / <; next labels are exact or carry › / > at either end (2.055834ms)
✔ ]n / [n find the period nav links and keep the daily prev / next links (3.021865ms)
✔ period-note creation paths are weeks, quarters, years, and all_time (0.887544ms)
✔ a missing period note is created through bob-ledger-tools api.periodNotes, never a template (2.340374ms)
✔ without bob-ledger-tools, or when ensure fails, a period link explains and creates nothing (0.895657ms)
✔ collectProjectNoteTaskRows splits ^prj from open residents and skips closed, fenced, quoted, and frontmatter tasks (12.90602ms)
✔ getProjectBlockState recognizes a project from type/status and ignores YAML scheduled (6.65561ms)
✔ getProjectBlockState reports an open external prerequisite (1.61053ms)
✔ getProjectBlockState reports a future inline [scheduled::] and ignores YAML scheduled (1.551854ms)
✔ getProjectBlockState scheduledValue override is the inline date, not frontmatter (0.858223ms)
✔ getProjectBlockState skips internal and archive Depends-On links (0.850484ms)
✔ getProjectBlockState is a no-op for terminal, daily, and non-project notes (1.906728ms)
✔ projectLooksBlockedByPrjShortcut is the single [?] ^prj row (0.606016ms)
✔ taskHasProjectBlockedTag is token-bounded and does not match #prj (2.457038ms)
✔ setProjectBlockedTag adds one tag before the trailing ^id, is a no-op at one, and strips (1.598525ms)
✔ reconcileBlockedScheduledTaskLine strips the tag and writes [unblocked::] on other-line Ready recoveries (1.40178ms)
✔ reconcileBlockedScheduledTaskLine skips [unblocked::] on the gesture's own line and on Next/Pending (0.810415ms)
✔ reconcileBlockedScheduledTaskLine warns and skips the field when markUnblockedLine is missing (0.504106ms)
✔ ADJ-11 planDependencyEdit never raises a ^prj target and walks through to that project's deps (18.598575ms)
✔ recovery gate keeps a resident of a blocked project blocked after own deps close (8.699125ms)
✔ recovery gate blocks residents on a future inline project date with no deps (4.499121ms)
✔ planDeferredPomodoroLinkCleanup always deletes a last-child open entry (7.687704ms)
✔ TICKLER notice uses unblocked <date> when returnedBy is unblocked (1.405766ms)
✔ recognition: a `^prj` parent in a project note carries its residents (7.12685ms)
✔ recognition: ordinary tasks, non-projects, terminal, daily, and twin-`^prj` notes are not project edits (1.252695ms)
✔ add: residents block with exactly one tag; closed and fenced lines are untouched (PDB1, PDT1, PDT6, PDT7) (12.393383ms)
✔ add: commitment transfers the strongest resident lane, never onto a `^prj` target (Design §5, ADJ-11) (6.333679ms)
✔ guards: a same-note add to `^prj` refuses, including mixed batches (1.822675ms)
✔ guards: the stage disables same-note rows for `^prj` with `inside this project` (2.775851ms)
✔ guards: cycle detection includes the implicit resident edges (§13.6) (3.034908ms)
✔ removal: the last reason recovers everyone with `[unblocked::]` (PDT2, Design §4) (8.360083ms)
✔ removal: a resident with its own reason stays `[?]` without the tag (PDB3) (2.313483ms)
✔ removal without a registry defers to reconcile: residents keep `[?]` and the tag (1.489112ms)
✔ writer: one gesture commits `^prj` and its residents in a single undo group (5.493186ms)
✔ writer: Pomodoro links of `^prj` and its residents are consumed with emptied entries (16.01048ms)
✔ notices: the project strings name the task, the flips, and the Pomodoro cleanup (0.492921ms)
✔ mapLineThroughStructural mirrors the assembly across deletes, inserts, and replaces (3.395725ms)
✔ api v3: removeDependencyByRef delegates removals to the single-transaction writer (2.092018ms)
✔ api v3: openDependencyStageForRef opens the Depends on stage on the owning task (0.692943ms)
✔ internal links stay on the line but leave the field (PDR7) (1.326908ms)
✔ removal from an unblocked ^prj never recovers own-reason residents (§13.10) (1.131634ms)
✔ resident recovery touches only tagged residents (§13.10) (3.397484ms)
✔ stage guard refuses a candidate that closes a cycle through a resident edge (§13.10) (1.48872ms)
✔ projectDependentResidentKeys lists open residents with block ids (0.45363ms)
✔ navNoteScopeFlags marks daily notes; a missing writer stays null (0.428941ms)
✔ reconcileBlockedScheduledTaskLine forwards scope flags to the writer (0.293769ms)
✔ parseProjectNoteFrontmatter ignores leftover scheduled keys (1.155833ms)
✔ formatTaskMoveProjectCountsNotice names blocked and recovered counts (0.280827ms)
✔ PDS15: projectParentTarget keeps the path and drops alias and heading (5.772376ms)
✔ PDS6: list-form, missing, and non-wikilink parents yield none (7.316279ms)
✔ PDS15: resolveProjectParentPath accepts alias, path, and heading forms (0.939088ms)
✔ PDS6: self, unresolved, and ambiguous basenames yield no parent (0.432535ms)
✔ buildProjectChildrenMap and descendants BFS skip cycles and cap depth (15.538182ms)
✔ buildProjectChildrenMap skips vault-sync conflict copies (3.8191ms)
✔ PDS6: area, terminal, daily, and self-parent notes are not children (0.889872ms)
✔ PDG8: planner blocks child and grandchild ^prj and residents (11.747758ms)
✔ PDG9: planner recovers tagged descendants with [unblocked::] (6.521229ms)
✔ PDG10: child with its own open target keeps residents tagged; grandchild stays inherited (13.123601ms)
✔ PDG11: a tagged root re-asserts descendant tags and recovers nothing (4.489917ms)
✔ tag proxy: getProjectBlockState reports project_parent when ^prj is tagged (7.346242ms)
✔ tag proxy: applyProjectRecoveryEdges blocks residents of a tagged ^prj (5.832666ms)
✔ tag proxy: shouldRecoverProjectResidents is false for a tagged ^prj (0.396805ms)
✔ tag proxy: Schedule keeps a tagged ^prj blocked and does not recover residents (10.547304ms)
✔ PDG13: failProjectPrjInternalAdd refuses descendant targets (0.656316ms)
✔ PDG13: planDependencyEdit refuses a descendant add from the files map (6.028654ms)
✔ PDG13: the stage disables descendant rows (6.003137ms)
✔ reversal: parseProjectLifecycleTaskBody strips #prj_is_blocked (4.634057ms)
✔ tag proxy: removing the last own dep of a tagged ^prj recovers nobody (14.733691ms)
✔ PDG8: Depends on blocks the project subtree, transfers the strongest lane, and consumes live links (55.764134ms)
✔ PDG9: removing the last open Depends on target recovers descendants with unblocked stamps (21.124135ms)
✔ PDG10: a child's own open target keeps its project Blocked while inherited residents stay tagged (9.037032ms)
✔ PDG11: a tagged root gesture reasserts descendant tags and recovers nothing (16.281011ms)
✔ PDG12: setting a future project date cascades to descendants and consumes their Pomodoro links (9.221664ms)
✔ PDG12: moving the project date due recovers descendants (6.704216ms)
✔ PDG12: deleting the project date recovers descendants (5.641836ms)
✔ PDG12: a tagged project task keeps its tag through future, due, and delete Schedule writes (9.596688ms)
✔ PDG14: a stale descendant is skipped, the root write stands, and the notice reports it (6.488758ms)
✔ Task Link Depends on writer preserves the internal-target guard on a project task (1.518082ms)
✔ api v3 removeDependencyByRef runs the recovery cascade for a linked project task (6.614915ms)
✔ counted Schedule writer cascades a future date through descendants (7.26602ms)
✔ counted subtree roots are ancestor-first and each descendant note is planned once (5.143227ms)
✔ Ctrl+D on the Depends on row removes the line and recovers the subtree (9.627095ms)
✔ a ^prj with no children reads no other note (0.471688ms)
✔ single seeds from raw text, not display decorations (26.795588ms)
✔ legacy valid free wins; invalid and taken fall through (3.5301ms)
✔ batch reserves suffixes for two same-text tasks (2.519127ms)
✔ counted-source, vault-single, and vault-counted seed per mode (2.873134ms)
✔ cross-note uses the target note, never the dependent fallback (2.037195ms)
✔ staging writes nothing until confirmed (1.406007ms)
✔ the shared planner matches the Task Card recommendation (149.426261ms)
✔ the preview table strings are exact (5.613827ms)
✔ checklist tiers and unpreviewable rows report ok:false (0.834242ms)
✔ a silent config failure reports ok:false with no Notice (0.298342ms)
✔ landing toasts append the preview after tails (2.308255ms)
✔ api.quickRoll has the v1 shape and never throws (12.589532ms)
✔ the preview matches what Alt+P then writes (69.540298ms)
✔ Alt+P matches Ctrl+Enter for roll, decay, project, and counted task writes (257.881219ms)
✔ Task Card Ctrl+Enter and Alt+P roll preserve bracket and parenthesis theme fields (13.600679ms)
✔ Alt+P matches Ctrl+Enter for a counted Task Link batch (21.46212ms)
✔ Task Link resolution keeps the outer modal hidden until its targets are ready (15.543087ms)
✔ Alt+P hides immediate rolls and reveals the optional Next Work summary (10.268528ms)
✔ a cancel recommendation waits for the visible card and the second Alt+P cancels (9.63713ms)
✔ Alt+P assigns P1 on a task with no priority (4.391474ms)
✔ Alt+P assign matches Ctrl+Enter on the visible card (7.522132ms)
✔ Alt+P assign matches Task Card key 1 on Ready rows (14.125077ms)
✔ Alt+P assign routes through inbox and Next work summary (22.147509ms)
✔ Alt+P on an unusable P1 level reveals the card without writing (2.304286ms)
✔ unavailable recurring tasks reveal the card without writing (2.299413ms)
✔ a landed review row advances once after Alt+P assigns P1 (7.630612ms)
✔ inbox routing is shown before the write and a managed line redirects to its owner (7.967514ms)
✔ a landed review row advances once after Alt+P writes (4.653323ms)
✔ the card alias uses the physical Alt+P code and ignores repeats (5.153764ms)
✔ a throwing one-shot dispatch always reveals the still-open card (8.465699ms)
✔ a refused one-shot write reveals both modal elements and leaves the card open (7.446411ms)
✔ Alt+P and Task Card keys show feedback while the review walk settles (1.817549ms)
✔ the registered command owns Alt+P and a Vim count is consumed once (9.585594ms)
✔ quick-roll visibility CSS disables the modal entrance animation and reveal clears its targets (10.591466ms)
✔ Less often picker renders actual rows from 90 days and Escape writes nothing (15.158619ms)
✔ Less often picker renders actual rows from 120 days and Escape writes nothing (2.033189ms)
✔ Less often picker renders actual rows from 180 days and Escape writes nothing (1.112549ms)
✔ renderFooter skips malformed hints and retains valid structured hints (0.59785ms)
✔ prompt with no keep target closes without writing (1.888272ms)
✔ dismissing a keep batch cancels without an entry (3.225008ms)
✔ shared prompt planner routes counted and lane target combinations (0.992383ms)
✔ single Next prompt always logs and gates unreadable history (3.509761ms)
✔ Next batch preview always logs one entry per target (1.161976ms)
✔ same-note cancel is one transaction and undo restores LINKS/status/log (30.047992ms)
✔ same-note cancel follows an id-less source after a mirror is inserted above it (7.317834ms)
✔ same-note cancel leaves the task above an id-less source untouched (5.738271ms)
✔ counted same-note cancels skip bystanders while each mirror shifts later sources (66.466236ms)
✔ same-note cancel follows an id-less source after two mirrors are inserted above it (19.916485ms)
✔ cross-note sources cancel the source and follow up the target (8.641522ms)
✔ all open statuses cancel; closed statuses keep their date (19.257571ms)
✔ recurring refusal writes nothing in a multi-source batch (5.243106ms)
✔ relabel into a cancel key cancels; same-key retry does not (7.259121ms)
✔ two cancel edges produce one fallback log entry (5.061427ms)
✔ hidden and one-off cancel labels still match configured keys (1.375552ms)
✔ no-id sources and linked_from_lines false still cancel (1.288921ms)
✔ unlink and empty policy never cancel (2.053716ms)
✔ hand-edit mirror never calls the cancel planner (7.252137ms)
✔ source on today's daily folds prune into the same write (13.482621ms)
✔ absent daily is zero cleanup; unreadable daily refuses before writes (7.854844ms)
✔ recovery receives cancelled identities and never offers successors (6.493217ms)
✔ stale expected effects and midnight/config replans write nothing (3.062219ms)
✔ Linked-from sources cancel; applyRelationCancelStaleToPicker keeps the stage open (6.713584ms)
✔ multiple sources in one note relocate after a log insert (6.010871ms)
✔ failed prune reports the chip and never claims a count (6.60405ms)
✖ cycler recovers ordinary dependents, keeps extra-prereq blocked, and reopens project residents (350.206367ms)
✔ writer never settles the walk; a cancelled source still emits the composed notice (1.663428ms)
✔ complete rule vectors share the explicit relation edge planner (15.055131ms)
✔ complete key vectors use the cancel writer's Unicode label key (0.461878ms)
✔ config vectors load both effective policies and keep linked-from warnings independent (13.157585ms)
✔ close-label config refreshes by mtime/size and clears on read failure (1.021142ms)
✔ unchanged malformed close config warns once and overlap removes both policies (0.939373ms)
✔ same-note completion and LINKS write share one undo transaction; post-Done waits (103.653299ms)
✔ same-note completion follows an id-less source after a mirror shifts it (8.479388ms)
✔ all four open statuses complete with the real cycler line rewrite (16.264962ms)
✔ ^prj completion touches its line and leaves resident tasks open (12.614047ms)
✔ closed sources retain their dates while the relation edit still commits (2.085694ms)
✔ recurring sources and old cycler APIs refuse before any write (4.217658ms)
✔ refused and legacy cycler results write nothing (5.62704ms)
✔ id-less cross-note source completes without a mirror or freshness side effects (5.572799ms)
✔ unchanged and spelling-only retries never complete (7.260898ms)
✔ two complete edges deduplicate to one line rewrite and one post-Done identity (49.000399ms)
✔ cancel and complete triggers on one source refuse the whole gesture (11.200133ms)
✔ changed close config, cycler API, and day make the commit stale without writes (6.287206ms)
✔ shared close preview derives exact pending edges for Links and Linked-from (5.52519ms)
✔ completed source closes the relation modal before awaiting post-Done and settles once (22.04569ms)
✔ nav LK1–LK18 parse relation grammar and reject the other relation parser (14.576145ms)
✔ nav LK14–LK19 context and cross-parse rules (1.46632ms)
✔ nav MC5 refuses relation embeds and MC16 keeps LINKS while dropping LINKED FROM (3.538243ms)
✔ nav MC15 hands LINKS edits to the relation mirror and notices generated lines once (5.846386ms)
▶ LG3: typed relation labels commit their text through the relation field
  ✔ add writes the typed label and mirror (65.982976ms)
  ✔ typed text is normalized before commit (8.610808ms)
  ✔ relabel replaces an existing label and its mirror (21.210411ms)
  ✔ Linked from labels the other task's LINKS line (13.329971ms)
  ✔ suggestion, plain, and raw-input paths remain supported (20.055155ms)
✔ LG3: typed relation labels commit their text through the relation field (132.564902ms)
✔ Linked from Shift+Enter goes through the relation field and labels the source (6.022767ms)
✔ Linked from Shift+Enter relabels a CURRENT source (7.370408ms)
▶ Linked from prompts for the owner's id then links
  ✔ plain Enter writes the owner id and the reverse link (5.776701ms)
  ✔ Shift+Enter labels the source after the owner id prompt (3.742894ms)
✔ Linked from prompts for the owner's id then links (10.780097ms)
✔ Linked-from cancel label follows the source after the owner mirror shifts it (12.194578ms)
✔ Links to prompts for the selected task's id then links (2.382137ms)
✔ Linked-from toasts name the source task (10.156587ms)
✔ links-to row follows blocks with N, first label, cut target, and +K (19.793812ms)
✔ links-to row stays available on closed tasks and empty LINKS lines (5.623001ms)
✔ links-to row refuses non-tasks and read-only notes (4.973402ms)
✔ card keycap l opens Links to; input focus keeps it quiet (3.05713ms)
✔ card ⇧L shows live incoming detail and routes Ctrl+D by direction (5.485958ms)
✔ index-only Linked-from rows convert 1-based edges into nav records (1.244978ms)
✔ card ⇧L detail cleans a raw index task line (4.213176ms)
✔ Linked-from scans source LINKS, reverses built-in phrases, and ignores stored mirrors (8.499446ms)
✔ LG7: reverse-stage Enter writes the source's LINKS and target mirror (2.521172ms)
✔ LG12: counted Links to applies the chosen labelled target to every source (23.040598ms)
✔ LG8: Ctrl+Shift+P on a LINKS line resolves to the owner's stage (2.829819ms)
✔ pool keeps closed tasks and done/ archives, drops dailies and templates (0.991335ms)
✔ stage lists CURRENT in authored order, then RESULTS, then CLOSED (5.224245ms)
✔ LG4: missing CURRENT targets stay removable; malformed lines refuse (1.298859ms)
✔ prerequisite targets badge; id-less rows prompt (3.633189ms)
✔ subtitle, consequence strip, live sentence, and label refusal copy (2.438062ms)
✔ cancel labels overlay at zero uses and render the live source cue (3.114702ms)
✔ recurring cancel rows are disabled and a multi-source cancel needs a second Return (5.247767ms)
✔ complete labels overlay at zero uses and render the live source cue (3.125305ms)
✔ complete labels keep used-count meta, hide overlay, and stay inert without config (4.628194ms)
✔ complete-label copy covers verdicts, inverse hint, cancelled target, and cycler disable (4.105989ms)
✔ recurring complete rows are disabled and a multi-source complete needs a second Return (11.291368ms)
✔ mixed closing banner and footer name both effects (0.334935ms)
✔ LG15: marked rows plan one commit with adds and unlinks split (0.627575ms)
✔ LG1: stage link writes LINKS, mirror, and mint in one transaction (2.741797ms)
✔ LG2: cross-note mirror follows; a changed target suffixes the notice (2.452312ms)
✔ LG4: CURRENT unlink removes the entry and its mirror entry (1.752768ms)
✔ LG6: archived targets link with the live-only suffix and no mirror (2.703302ms)
✔ LG13: linking never stamps, routes, or touches Depends-On lines (4.446185ms)
✔ LG15: two targets link in one gesture with one notice (6.570064ms)
✔ LG5: id-less targets refuse at the writer, so the stage prompts first (0.802876ms)
✔ LG7: Ctrl+Shift+P resolves LINKED FROM to its owner's reverse stage (0.341021ms)
✔ api.relations openStage opens both directions at v1 (2.18698ms)
✔ relation-label stage Tab, Ctrl+D, pipe, and Ctrl+H mirror the card (77.826948ms)
✔ relation-label rename preview reports done/ impact and checks affected editors (1.596361ms)
✔ relation-label rename modal re-previews, saves the active note, and confirms merges (2.667081ms)
✔ Bob: Relation labels manager keeps hidden labels visible and delegates hide and unhide (4.926886ms)
✔ one-off labels hide through bob only after the relation commit succeeds (7.11301ms)
✔ LG16: ~ flips Links to Linked from in place, keeping the filter (11.545525ms)
✔ LG16: mid-query caret survives the flip and a second ~ flips back (3.42325ms)
✔ LG16: a ~ keydown flips through handleKeydown and never types (5.31163ms)
✔ LG16: counted sessions refuse the flip to Linked from (1.308412ms)
✔ LG16: modified, composing, repeat, and busy ~ keydowns do not flip (7.894673ms)
✔ LG16: ~ in the relation-label stage is not intercepted (1.951287ms)
✔ LG16: a stale refresh for the old direction never replaces the new stage (3.642894ms)
✔ LG16: footer offers ~ flip direction in single sessions only (2.415385ms)
✔ SA22/SA30: successor labels overlay as configured with offers row meta and caveats (0.884679ms)
✔ merge label prompts for the missing source ID then previews with Current:current (7.875781ms)
relations.linked_from_mentions is invalid; treating as true
✔ MN15: 💬-first labels are reserved in every nav label path (5.473633ms)
✔ MN15/MN16: LINKS rejects 💬 labels; LINKED FROM keeps only 💬 mentions (4.222453ms)
✔ MN15: planLinksEdit refuses 💬 labels as reserved (2.256196ms)
✔ MN15: applyRelationEdit surfaces the reserved-label message (8.071421ms)
✔ mentions kill switch defaults on, honors false, and warns invalid (2.45351ms)
✔ Task Card count: relations-only keeps N · first name (2.120006ms)
✔ Task Card count: v1 index keeps N · first name (2.241274ms)
✔ Task Card count: mentions-only reads M 💬 · first name (0.532783ms)
✔ Task Card count: both reads N · R relation(s) · M 💬 (0.625891ms)
✔ Linked-from stage: v2 rows map to relation + mention CURRENT rows (3.026514ms)
✔ Linked-from stage: view keeps mention rows CURRENT and already linked (1.609883ms)
✔ Linked-from stage: decorate prefers linkedFrom v2 over incoming (6.289034ms)
✔ Linked-from stage: footer hints follow the mention row kind (2.081348ms)
✔ Linked-from stage: consequence strip names the mention gesture (2.197858ms)
✔ MN19: ↵ on a mention row opens the source at the occurrence (0.776752ms)
✔ Linked-from stage: ⇧↵ on a mention row adds a relation for the source (2.670959ms)
✔ Linked-from stage: toggling a mention row is refused with the notice (1.196601ms)
✔ MN18: courtesy write mints the source and mirrors same-note (💬 mentions) (11.559669ms)
✔ MN18: courtesy write mirrors cross-note targets through a follow-up (8.722084ms)
✔ MN18: courtesy write removes the entry when the link is deleted (9.665171ms)
✔ M7: courtesy write suppresses the mention when a dependency joins the pair (2.56271ms)
✔ MN7/MN16: relation wins — courtesy write replaces a stale mention entry (17.194282ms)
✔ courtesy write keeps existing entries on uncertainty and writes nothing (1.296676ms)
✔ courtesy write skips without a v2 index or with the switch off (0.354837ms)
✔ hand-edit LINKS removal downgrades via the touched-source path (1.256144ms)
✔ fireDependencyHandEditMirror runs the mention convergence after mirrors (12.299511ms)
✔ unlink downgrade: removeLink keeps (💬 mentions) with the unlink notice (17.195185ms)
✔ unlink without a mention removes the entry with the plain notice (5.195222ms)
✔ Links-to Ctrl+D downgrades the mentioned target and removes the other (6.087525ms)
✔ verify-only: task-status-cycler still treats a mention row as managed (73.781025ms)
✔ verify-only: block-id-prompt still treats a mention row as managed (61.079637ms)
✔ merge labels classify as the merge effect (6.250421ms)
✔ a merge-involved overlap drops every list and names merge_labels (1.341888ms)
✔ cancel+complete overlaps keep their legacy copy without merge (0.918727ms)
✔ successor overlaps keep the three-list copy without merge (1.214301ms)
✔ an invalid merge_labels list warns and merges nothing (0.624505ms)
✔ configured merge labels overlay suggestions with the merges meta (0.915128ms)
✔ the merge strip reads the preview record verbatim (1.927754ms)
✔ the merge strip counts several sources and omits empty parts (0.862509ms)
✔ merge targets resolve with one destination and refuse several (0.974813ms)
✔ already-closed detection needs every source closed (1.07586ms)
✔ merge offer rows reuse the hand_off group with merged-from reasons (2.313055ms)
✔ an already-closed source takes the plain relation with link only (2.968128ms)
✔ an id-less source starts the block-ID prompt with no notice (1.213495ms)
✔ links-to refuses several picked targets (0.832364ms)
✔ mobile resolves the desktop refusal and writes nothing (1.119963ms)
✔ a preview refusal notifies and never applies (1.642114ms)
✔ one source without offers applies and offers Undo merge (3.122904ms)
✔ offers open the successor picker and ride -p into apply (1.668678ms)
✔ dismissing the offer picker applies unpicked (1.103956ms)
✔ a counted batch arms the banner and commits on the second Return (2.364221ms)
✔ linked-from merges the picked task into the cursor task (1.666271ms)
✔ an unchanged re-run writes nothing and stays quiet (0.565003ms)
✔ missing-ID queue orders sources then target and dedupes (0.423387ms)
✔ an already-closed id-less source links only with no merge prompt (0.376884ms)
✔ a resumed commit without IDs refuses without prompting again (0.323419ms)
✔ an abandoned queue triggers no preview and no apply (0.208467ms)
✔ a non-active open editor is saved before preview (0.875848ms)
✔ merge block-ID copy pins subtitle and footer labels (0.56741ms)
✔ score wins over status; no blocked section (11.633787ms)
✔ blocked rows are not hidden behind the cap (10.107471ms)
✔ render matches the relation planner in both directions (5.450711ms)
✔ other stages still use their own planners (6.166395ms)
✔ peer tie order: In Progress, Next, then Ready and Blocked together (0.649465ms)
✔ successor config vectors: three-list one-effect rule (SA23) (13.580569ms)
✔ successor key vectors: match, effect, and inverse hint (SA22) (1.476516ms)
✔ successor copy vectors: row meta, verdict, caveats, hint, rename (SA30) (0.988784ms)
✔ successor consequence strip shows offers, caveat, and hint (0.691389ms)
✔ successor suggestions overlay zero-use rows as configured (1.018714ms)
relations.linked_from_lines is invalid; treating as true
✔ LW1 inserts an unlabelled LINKS line in the empty slot (15.28459ms)
✔ LW2 appends a labelled entry and LW3 is a byte-identical no-op (3.699564ms)
✔ LW4 relabels in place and LW5/LW6 remove entries (2.363602ms)
✔ LW7 places LINKS after Sub-projects and LINKED FROM after LINKS (5.900628ms)
✔ LW8 inserts LINKS as the first child when only user children exist (1.34091ms)
✔ LW9 merges duplicate LINKS lines with first label winning (0.80983ms)
✔ LW10 refuses a malformed LINKS line (0.682513ms)
✔ LW11 normalises and refuses labels (1.566679ms)
✔ LW12 reuses a 4-space child indent (0.439668ms)
✔ LW13 canonical link forms match Rust (3.458162ms)
✔ LW14 / LK20 LINKED FROM sort is byte-identical to Rust (1.076743ms)
✔ Rule 6 LINKED FROM planner table (2.708627ms)
✔ linkedFromDesiredAfterDelta keeps labels and sorts (2.856866ms)
✔ LG14 kill switch defaults on, honors false, and invalid values fall back on (2.116258ms)
✔ LG1 same-note add mints and writes LINKS plus LINKED FROM in one transaction (31.451822ms)
✔ LG2 cross-note T follows the source commit; a changed target suffixes the notice (18.040845ms)
✔ LG4 unlinks and relabels in place with the mirror (11.173457ms)
✔ LG6 archived targets write LINKS without a mirror (1.879409ms)
✔ LG13 relation writes never stamp or change status (1.816855ms)
✔ LG14 kill switch writes LINKS without a mirror or source mint (1.276716ms)
✔ api.relations v1: removeLink works and openStage settles false without a plugin (3.630666ms)
✔ createDependencyNavApi mounts relations beside blocks (0.852662ms)
✔ LG10: hand-edited LINKS mirrors to LINKED FROM and re-fires after undo (6.139775ms)
✔ LG11: hand-editing generated LINKED FROM only shows its notice (0.824375ms)
✔ LG9: Ctrl+D's writer clears outgoing links and their generated mirrors (4.669934ms)
✔ Alt+N release from a NEXT landing advances with one composed toast (73.015346ms)
✔ counted Alt+N lands past every handled key in one jump (16.74438ms)
✔ a cancelled Alt+N release prompt stays and frees the lock (14.647907ms)
✔ Alt+N on a checklist landing stays with the plain notice (18.214854ms)
✔ Alt+N off a landing on a task that is not due behaves exactly as today (20.223799ms)
✔ Alt+N while the gesture lock is held is swallowed (19.344246ms)
✔ a Task Card priority commit on NEXT advances, landing after the rich card (128.514223ms)
✔ dismissing the Task Card stays and frees the lock (31.523425ms)
✔ a frontmatter-only project edit from the card stays (21.694858ms)
✔ a same-day priority schedule on a checklist row stays (27.130594ms)
✔ a future schedule on a checklist row advances (35.006681ms)
✔ a Task Card cancel on a checklist row advances with the cancel card first (29.655649ms)
✔ Ctrl+Shift+M from a landing follows the task and never advances (40.547985ms)
✔ Ctrl+Shift+M from a checklist landing keeps the destination focus (20.018451ms)
✔ ]s after a landed move resumes at the successor despite the line shift (55.861543ms)
✔ [s after a landed move resumes at the predecessor (19.611134ms)
✔ a counted move from a landing resumes past every moved target (16.726353ms)
✔ counted Ctrl+Shift+M command dispatch preserves a landed move count (34.872561ms)
✔ a stale landing is not parked (15.050895ms)
✔ Ctrl+Shift+M while the gesture lock is held is swallowed (1.377965ms)
✔ dismissing the move picker stays and frees the lock (27.064286ms)
✔ Ctrl+Shift+M off a landing behaves exactly as today (29.796701ms)
✔ answer, move, answer stays in queue order past an accumulator alias (36.749005ms)
✔ a move park ignores a stale accumulator alias (1.6033ms)
✔ a re-indexed origin still advances from the landed row (2.279944ms)
✔ a landed move park clears the current review task (4.583433ms)
✔ review settle follows the task through a BLOCKS insertion above (bob-cli-94) (32.471669ms)
✔ review settle follows a BLOCKS deletion above without advancing on a non-resolving edit (22.086456ms)
✔ review settle never substitutes the cursor line and shares the inbox fallback reader (8.586675ms)
✔ predicate: reviewOutcomeResolves across tiers and kinds (5.506041ms)
✔ findReviewResumeIndex identifies rows by path and text (1.149457ms)
✔ buildReviewMoveAnchor parks text-identified resume neighbours (3.546372ms)
✔ planReviewJump with a move anchor resumes at the walk neighbour (3.585195ms)
✔ capture: null off a landing (16.154392ms)
✔ capture: frozen origin shape, BUSY while locked, expiry (3.273028ms)
✔ successor picker keeps a captured completion locked through selection and one walk toast (58.790374ms)
✔ continue: refuses stale origins, showing the notice once (16.205604ms)
✔ continue: stays on null and non-resolving outcomes (3.01063ms)
✔ continue: stays for lane answers and mixed-version completes on checklist rows (2.909858ms)
✔ continue: a resolving lane answer advances exactly once with one composed toast (3.031097ms)
✔ continue: counted handled refs land past every handled key in one jump (1.930629ms)
✔ continue: wrap is announced and the empty queue composes the empty notice (7.488092ms)
✔ continue: anchor-only planning survives cursor drift and lagging queues (3.913464ms)
✔ continue: POST origins never wrap (3.700046ms)
✔ complete: the last lane row before POST stays with the next-step toast (3.228616ms)
✔ complete: a wrap onto a skipped PRE row stays (2.903853ms)
✔ complete: a step into ROTTEN shows the boundary line (2.194056ms)
✔ busy: walk keys, refresh, claim, and capture are swallowed in the settle window (10.567036ms)
✔ advance: Ctrl+Alt+F stamps through the shared tail with one composed toast (23.533873ms)
✔ advance: cross-note landing saves the edited source and cancels its pending save (11.634001ms)
✔ advance: decay choices advance except reword, with no preamble of their own (1.918397ms)
✔ jump history: same-note and cross-note auto-advances record, and <C-o> returns (18.453612ms)
✔ jump history: a manual ]s also records its landing (1.937564ms)
✔ api: reviewWalk v3 is frozen with version 1, degrades null, never throws (10.926959ms)
✔ walk identity: a stale accumulator key never moves the anchor (0.847069ms)
✔ walk identity: a lagging answered row stays excluded (0.399965ms)
✔ walk identity: a line-shifting answer lands on the true successor by text (0.542808ms)
✔ walk identity: legacy anchors without text resolve as before (3.70261ms)
✔ walk identity: matchFreshStampRefs prefers text over line (0.708132ms)
✔ walk identity: collectReviewAnswerKeys separates position from exclusion (1.081165ms)
✔ return: planReviewWalkReturn pure decisions (0.710019ms)
✔ return: same-note ]s returns then steps, both directions (6.120708ms)
✔ return: a different due row returns instead of stepping from there (7.075485ms)
✔ return: cross-note return re-arms and records <C-o> (10.753983ms)
✔ return: a count is consumed and ignored (3.690002ms)
✔ return: internal endpoints never return (2.679953ms)
✔ return: group jumps never return; lowercase continues from the landed group (4.18518ms)
✔ return: its own stamp ends it (2.421844ms)
✔ return: a stamp elsewhere does not end it (1.974107ms)
✔ return: answers move the current task, a stopped Ctrl+Enter clears it (6.267597ms)
✔ return: a stale landing falls through in the same press (0.975508ms)
✔ return: a day change never returns (1.185416ms)
✔ predicate: reviewOutcomeResolves for the RECURRING resolution table (0.789976ms)
✔ recurring Ctrl+Enter: a fixed-cadence insert above never skips the next due row (0.430218ms)
✔ return: a RECURRING landing rearms the current-task return (0.882367ms)
✔ Ctrl+Alt+F after a Rotten Log insertion lands on the shifted successor exactly once (8.167984ms)
✔ an off-landing Alt+N commit on a due NEW row advances with one composed toast (50.053019ms)
✔ a reworded landed row whose new text is in the queue advances (26.620774ms)
✔ a task that is not due keeps today's behavior with no advance (14.427611ms)
✔ an off-landing PRE row stays and frees the lock (11.465744ms)
✔ an off-landing RECURRING row stays (14.73756ms)
✔ a landing elsewhere does not block an off-landing answer (14.795642ms)
✔ a new landing between capture and continue does not advance (15.311511ms)
✔ an off-landing capture while busy swallows the key (11.796698ms)
✔ counted Alt+N off a landing advances past every handled key (24.516358ms)
✔ the public api capture stays landing-only off a landing (1.781606ms)
✔ a Task Card commit off a landing still stays (130.788887ms)
✔ a routed Alt+N on a due inbox row advances with a route toast and journals route (51.833965ms)
✔ canonical group order includes legacy references between tickler and rotten (3.24178ms)
✔ nine current tiers: both directions from first, middle, and last rows land on group row one (4.92195ms)
✔ empty tiers are skipped; wrap uses occupied ends (0.596683ms)
✔ absent PRE and POST wrap at occupied ends (0.48312ms)
✔ one occupied group cycles to its first row, including from that row (0.628419ms)
✔ one-row queue and empty queue (0.4637ms)
✔ counted jumps wrap with modular arithmetic, including multiple circuits (3.904468ms)
✔ no origin: ]S first occupied, [S last occupied, initial entry is not a wrap (0.622379ms)
✔ origin prefers a live cursor row over the previous landing (1.603066ms)
✔ off-queue cursor uses a live same-day current task (5.935748ms)
✔ emptied origin group uses the same-day anchor tier and skips that group (0.996746ms)
✔ a landing anchor does not hide its row on the next circuit (0.44352ms)
✔ answeredKeys exclude only identity-verified same-day rows (0.677444ms)
✔ old-day anchors and current refs cannot supply an origin (0.420785ms)
✔ duplicate text prefers the cursor line; a reused line number is not enough (1.668359ms)
✔ legacy returned, resurfaced, supported REFERENCES, and unknown tiers (0.634021ms)
✔ pinned origin on retry recomputes from the original group, not the failed target (0.369841ms)
✔ rank and total count remaining unanswered rows, including visited ones (0.504287ms)
✔ jumpToDueTask groupJump lands once, records a landing anchor, and never writes (4.078037ms)
✔ groupJump bypasses return-to-current and wins over endpoint (0.922599ms)
✔ stale group retry pins the original origin; a vanished target recomputes from it (1.04739ms)
✔ empty reread, repeated staleness, hard failure, missing API, and busy lock (1.643243ms)
✔ groupJump consumes a Vim count before the first await (2.235849ms)
✔ registered uppercase commands reverse directions and keep family s (15.758246ms)
✔ ]S from ROTTEN lands on POST row one with remaining counts and no skip-complete claim (0.998757ms)
✔ lowercase ]s continues from a group landing; a landing is not an answer (2.081284ms)
✔ review answer outcome vectors map to the schema vocabulary (3.003247ms)
✔ event builder uses the walk row key and its tier, once per distinct key (3.160729ms)
✔ journal appends are queued and failures retain events without failing answers (23.396405ms)
✔ card after-line outcomes map done, drop, defer, sequence, and card (2.201932ms)
✔ journal events carry plugin@manifest version with a 2.x fallback (6.158513ms)
✔ write failures show one notice per burst and a recovery notice (5.574559ms)
✔ missing api.stats shows one session notice and later delivers retained events (6.28056ms)
✔ validation rejects drop the event and continue the drain (1.772682ms)
✔ pending journal events cap at 500 and warn once per burst (5.611652ms)
✔ decay config defaults to enabled with one roll per level (17.928156ms)
✔ decay:false disables decay and level rolls are accepted but ignored (2.631597ms)
✔ decay.rolls sets the limit and levels[].rolls overrides it (0.678439ms)
✔ decay config rejects bad rolls, unknown keys and non-priority use (1.181628ms)
✔ classifyScheduleLogRollReason sorts automatic heads from deliberate ones (1.912875ms)
✔ conformance vectors 1-10: streaks at P2 with the default limit (12.341654ms)
✔ conformance vectors 11-15: custom limits, disabled decay and edges (1.708225ms)
✔ the streak reader follows log grammar: legacy labels, nesting and stops (4.382816ms)
✔ rollPriorityRecommendationDate avoids the current date when the window has room (0.991911ms)
✔ decay and cancel reason formatters use the exact ladder copy (1.959738ms)
✔ the default ladder walks P2 roll, decay, P3 roll, decay, P4 roll, cancel (0.710834ms)
✔ the planner returns null without a configured priority (0.465761ms)
✔ buildPriorityRollPreviewModel carries the row copy for every kind (1.126422ms)
✔ picker-single recognizes the recommended-roll keypress (0.292884ms)
✔ picker-single stage-two footers carry the recommended-roll hints (0.625804ms)
✔ picker-single shares one roll between the preview and the pinned row (0.789818ms)
✔ picker-single plans the next-roll hint for the notice chips (4.507021ms)
✔ picker-single notice cards name the roll, decay and next press (6.673376ms)
✔ picker-single decay payload and preview-target comparison (0.784078ms)
✔ picker-counted plans one recommendation per target with skips (5.881766ms)
✔ picker-counted batch preview, footer and notice copy (3.515577ms)
✔ picker-counted composes cancel then set-priority into one postimage (8.473191ms)
✔ picker-counted assigns P1 alongside roll and decay in one transaction (4.978913ms)
✔ picker-counted keeps an unconfigured value skipped (16.958053ms)
✔ freshness decay card output is unchanged for P0 (5.830071ms)
✔ picker-counted refuses a recurring cancel as one batch (1.063075ms)
✔ recommended roll recovers with [unblocked::] when the writer is passed (2.334ms)
✔ picker-counted stale lines refuse and new options stay byte-identical (6.602435ms)
✔ picker-links aggregates one recommendation per note (2.24343ms)
✔ picker-links refuses a recurring cancel as one batch (0.821567ms)
✔ picker-links takes a single recommended roll with Ctrl+Enter (103.77025ms)
✔ picker-links shows no pinned roll row in stage two (21.772761ms)
✔ picker-links decays and cancels a single Task Link (21.469059ms)
✔ picker-links applies a mixed batch across two notes (9.617366ms)
✔ picker-links refuses the whole batch when a linked note changed (9.387833ms)
✔ picker-links prunes today's open Pomodoro links (14.002411ms)
✔ picker-single Ctrl+Enter rolls a P2 task in one undo group (39.424876ms)
✔ picker-single opens on scheduled so Ctrl+Enter rolls with no navigation (22.870894ms)
✔ picker-single opens a ^prj task on inline scheduled for an immediate roll (59.745434ms)
✔ picker-counted opens on scheduled for an immediate mixed batch (37.371216ms)
✔ picker-links opens on scheduled for an immediate roll (25.386208ms)
✔ picker-single Ctrl+Enter decays a P2 task in one undo group (20.016604ms)
✔ picker-single Ctrl+Enter cancels a P4 task in one undo group (25.44631ms)
✔ picker-single Ctrl+Enter in stage two writes the recommended roll (17.633581ms)
✔ picker-single Enter opens the date stage; Ctrl+Enter takes the recommendation (11.19784ms)
✔ picker-single P0 assigns P1 and closed tasks have no preview (37.843278ms)
✔ picker-single recurring P4 past the limit refuses and keeps the picker open (17.823213ms)
✔ picker-single stale tasks refuse and re-render the decay preview (19.2015ms)
✔ picker-single Ctrl+R on the card re-rolls the recommendation date (12.75812ms)
✔ picker-single Ctrl+R in stage two keeps the pinned row and recommendation together (7.020297ms)
✔ picker-single Ctrl+Enter rolls a ^prj task through its inline date in one undo group (24.989018ms)
✔ picker-single Ctrl+Enter decays a ^prj task through its inline date in one undo group (15.698008ms)
✔ picker-counted Ctrl+Enter applies a mixed roll/decay/cancel batch in one undo group (24.106329ms)
✔ picker-counted Ctrl+Enter refuses when a target line changed (31.258126ms)
✔ picker-counted Ctrl+Enter refuses a recurring cancel batch (18.207326ms)
✔ recommended roll on Pending offers a Work Log with the write stamp (1106.392731ms)
✔ recommended roll blank summary skips the Work Log without a fallback (1097.982529ms)
✔ Ctrl+Enter in the Work Log stage confirms instead of re-rolling (1103.104265ms)
✔ counted recommended mixed batch logs only eligible roll and decay targets (1092.167119ms)
✔ Task Link recommended roll deletes the emptied Pomodoro in the same daily write (4.402019ms)
✔ single keep logs still the primer with stamp in one undo (73.084821ms)
✔ single keep logs blank with stamp in one undo (9.823751ms)
✔ Esc retains the document and walk anchor; repeat command cannot open another prompt (6.900461ms)
✔ same-day repeat never prompts or appends, including saturated 999 (18.627752ms)
✔ counted predicate: scheduled tickler (0.919505ms)
✔ counted predicate: unblock tickler (0.301767ms)
✔ counted predicate: new (0.336348ms)
✔ counted predicate: Pending (4.335987ms)
✔ counted predicate: Next (0.678349ms)
✔ counted predicate: PROJECTS (0.371576ms)
✔ counted predicate: recurring (0.282013ms)
✔ counted predicate: checklist (1.094049ms)
✔ counted predicate: closed (0.210411ms)
✔ counted predicate: early (0.231947ms)
✔ scheduled tickler logs; unblocked and legacy keeps never prompt (17.582779ms)
✔ due WIP keep asks why and logs a WIP entry with the stamp in one undo (3.197187ms)
✔ blank WIP keep logs 🤷 with its rung tail (4.75324ms)
✔ single Next keep with a blank reason counts and always logs (8.796562ms)
✔ single Next keep still useful in Next counts and always logs (3.779002ms)
✔ early Next task stamps quietly with no prompt; Ctrl+Alt+F logs then advances (8.044284ms)
✔ Esc on a Next keep writes nothing and does not advance (1.364342ms)
✔ counted mixed sessions use one Rotten prompt and log each rung tail (11.615587ms)
✔ counted at-limit Rotten targets skip without opening a prompt or logging (1.285641ms)
✔ unavailable decay card falls through the reason planner (6.027127ms)
✔ document changes while prompt is open refuse the entire keep (4.704281ms)
✔ day changes while prompt is open refuse the entire keep (1.789247ms)
✔ prediction changes while prompt is open refuse the entire keep (6.178715ms)
✔ guard changes while prompt is open refuse the entire keep (4.699308ms)
✔ ambiguous Rotten markers disable the prompt and refuse even a bypass (6.964722ms)
✔ combined planner inserts nested targets bottom-up and preserves CRLF (5.001881ms)
✔ lane keeps always log with their rung tail and refuse ambiguous markers (10.011969ms)
✔ rung classification follows status, lane, and priority (0.936812ms)
✔ P-level keep classification, prompt, and batch log use configured labels (1.461543ms)
✔ decay card Rotten Log bodies use configured P-level labels (0.452969ms)
✔ prompt copy shows the rung question, allowance, and tallies (4.104572ms)
✔ Next keep model always logs with its rung tail and gates unreadable history (0.856003ms)
✔ keep stage warns for inline fields, ignores IME Enter, and swallows both keep chords (5.827309ms)
✔ marker vectors match the Rust Rotten cases (3.175382ms)
✔ shared grammar fixture round-trips format and parse vectors (4.156743ms)
✔ entry parsing accepts legacy entries and per-rung tallies (1.085902ms)
✔ decay-card Step, Stay, and Drop bodies parse as rung history (0.784312ms)
✔ readRottenLog statuses cover missing, empty, ok, and unknown (1.759942ms)
✔ planManagedTaskLogEntry creates the log last and prepends entries (1.794736ms)
✔ Work Log writes never file under the Rotten marker (1.091858ms)
✔ freshness delegation guards reject Pomodoro ledger rows before injected writers (6.495942ms)
✔ refresh picker refuses a legacy Pomodoro heading before its refresher runs (1.103097ms)
✔ lane commit stamps an open Ready task (3.965336ms)
✔ lane release stamps an open Next task (1.362231ms)
✔ lane without a stamper leaves lines as they were (0.747933ms)
✔ counted property set stamps every rewritten open task (6.003857ms)
✔ counted delete-property stamps the rewritten task (1.280544ms)
✔ stamp lands before the suffix after a priority edit on a stamped line (0.850418ms)
✔ recurring tasks are never stamped (0.893189ms)
✔ cancel never stamps (3.804048ms)
✔ fresh and refresh never go through the end-append writers (0.790371ms)
✔ counted dependency edit stamps the rewritten parent (16.898792ms)
✔ moved tasks are stamped at their destination (8.162739ms)
✔ move without a stamper leaves lines as they were (1.752145ms)
✔ refresh row shows the effective interval in task mode (1.881962ms)
✔ refresh row hides without the api and on closed tasks (1.380928ms)
✔ refresh row covers counted and link modes, including mixed (2.042614ms)
✔ refresh value items offer presets and use default (1.865759ms)
✔ setRefreshLine stamps and sets or clears the interval (0.850363ms)
✔ 1, 6, 11, and 20 offers start unmarked and retain supplied opaque keys (20.005924ms)
✔ Tab marks a subset, returns model order, and group Ctrl+A includes collapsed offers but excludes muted rows (9.258309ms)
✔ filtering expands matches, collapse state survives clearing, and hidden marks still submit (9.347057ms)
✔ group headers, folded counts, destinations, IDs, and budget meter render with over-budget picks allowed (4.231861ms)
✔ Enter modifiers, repeats, and the deterministic 349/350 ms guard are consumed (4.065788ms)
✔ Escape, outside close, repeat close, concurrent calls, and unusable models settle safely (4.957046ms)
✔ the review-walk hold survives the 3000 ms timeout and releases with the matching completion owner (1.718062ms)
✔ destination override shapes normalize and label (0.648871ms)
✔ destination picker detection needs block-id-prompt api v1 with pick (1.815913ms)
✔ Ctrl+Shift+Enter retargets marked rows, shows the override, and returns it with the picks (7.144393ms)
✔ Ctrl+Shift+Enter keypress retargets the highlighted row when nothing is marked (4.246074ms)
✔ a cancelled destination pick and a missing picker leave rows untouched (9.85091ms)
✔ unload closes a pending modal, settles old and replacement APIs to null, and open failure cleans up (2.56983ms)
✔ themeIntent and preserveSpelling survive both destination normalizers (0.802148ms)
✔ malformed themeIntent is dropped without rejecting a valid destination (0.571899ms)
✔ the picker model carries validated task context and drops malformed task objects (0.803302ms)
✔ task-aware retargets pass each successor's context, including a non-first line (4.400978ms)
✔ old rows retarget without a task request and cannot acquire theme permission (1.993386ms)
✔ Alt+Enter retype and untouched default merge keep validated intent (2.956236ms)
✔ a changed or missing source refuses the retarget and leaves overrides untouched (2.390159ms)
✔ an intermediate cancel and a close while awaiting leave previous overrides (7.805824ms)
✔ open-editor text wins the refresh and reentry is refused while awaiting (1.771877ms)
✔ retarget:false hides the hint, ignores Ctrl+Shift+Enter, and drops destinations (6.533982ms)
✔ picker API v2 renders a keep_moving group: title, caption, tag, lanes, fold line, and the skip-forward icon (5.042792ms)
✔ a keep_moving fold line omits zero parts and orders blocked, scheduled later, hidden (0.733918ms)
✔ picker titles follow the keep_moving copy table; an explicit title always wins (0.685546ms)
✔ a mixed picker keeps the generic icon and renders keep_moving last with the same heading (5.847609ms)
✔ v1 models render exactly as before: no caption, tag, or titlebar, and rows keep their v1 details (5.388483ms)
✔ legacy groups render the additive blocked and scheduled folds as their own lines (0.419467ms)
✔ rows show lane names for every group and never a raw status symbol (0.561736ms)
✔ unknown groups are still dropped and a keep_moving-only model with no selectable row is unusable (0.551331ms)
✔ the filter reaches keep_moving groups by caption, tag, and lane (5.441351ms)
✔ keep_moving picks reuse the normal pick/retarget paths: keys and destinations round-trip (24.461549ms)
✔ cycler keep-moving model survives nav normalization with identical copy (159.50455ms)
✔ picker API v3 renders a relation group: header, caption, tag, fold, title, and link-2 icon (1.857086ms)
✔ a mixed picker keeps the generic title and icon and renders relation with caption and tag (0.955581ms)
✔ v1 and v2 models still render as before under picker API v3 (1.12075ms)
✔ unknown groups are still dropped and a relation-only model with no selectable row is unusable (0.646818ms)
✔ the filter reaches relation groups by caption, tag, fold, suffix, and second reason (1.851938ms)
✔ relation-only titles follow the copy table; an explicit title always wins (0.671932ms)
✔ relation successor copy vectors drive every copy-table string (3.28505ms)
✔ cancel vectors drive planTaskCancelBatch (9.082392ms)
✔ prune vectors drive planDeferredPomodoroLinkCleanup (7.02084ms)
✔ rule vectors drive planRelationCancelEffects (3.393576ms)
✔ key vectors pin relationCancelLabelKey matching (0.495671ms)
✔ config vectors drive loadRelationsCancelLabels (10.538192ms)
✔ card model builds stable rows, scope metadata, and an existing recommendation (30.070824ms)
✔ Task Card type projection distinguishes explicit themes and inherited note defaults (8.473607ms)
✔ Task Card theme projection labels reading, note defaults, and no-default suggestions (8.676292ms)
✔ Task Card theme projection preserves repair and unknown states with or without a default (11.914493ms)
✔ Task Card theme projection resolves linked task identity, deduplicates targets, and uses full target notes (14.35225ms)
✔ Task Card theme batches report mixed values and missing APIs without guessing (9.555072ms)
✔ Task Card theme runtime adapter supplies active and resolved live note snapshots (0.842772ms)
✔ explicit preview builder matches writer rolls and deduplicates linked targets (7.896163ms)
✔ counted and linked card models report real target counts and mixed values (5.552448ms)
✔ priority, recommendation, navigation, action, deletion, and search keys resolve to typed intents (3.693868ms)
✔ Escape, bare q, and Ctrl+[ close the card; nothing else does (1.870656ms)
✔ close keys never fire during composition or inside a text field (1.742486ms)
✔ unavailable actions, input composition, and repeats stay safe (3.16686ms)
✔ Blocks row summarizes warm-cache dependents and their last open reason (6.123361ms)
✔ Blocks row refuses closed tasks and unencodable paths without an id (5.488667ms)
✔ key resolver table covers lane state, API availability, and modifier guards (2.823626ms)
✔ recurring cancellation and blocked lanes expose reasons instead of writes (1.29521ms)
✔ unprioritized single task recommends assign P1 with dated preview (2.594859ms)
✔ task card header stores the block mark and reason lines for each family (4.031283ms)
✔ task card header caps the prerequisite reason lines with a +N overflow (0.737049ms)
✔ task card header keeps a null block mark for batches, other lanes, and fallback (1.970014ms)
✔ identity keys distinguish linked notes that share a line number (3.459997ms)
✔ planScheduleReview opens for a bare date and skips when reason is known without Work Log (2.154674ms)
✔ planScheduleReview counts unique tasks when Task Links repeat a target (0.734253ms)
✔ bare date on Ready opens a reason-only review and writes nothing until Enter (62.831301ms)
✔ typed reason and blank reason on an existing Schedule Log keep per-target rules (16.600438ms)
✔ Ready vs Next vs Pending: only Next/Pending show Work summary (16.815579ms)
✔ inline reason on Ready dispatches immediately; on Next it still reviews Work summary (12.576337ms)
✔ Tab moves from Reason to Work summary and Enter commits from either field (7.635797ms)
✔ Back and Escape at both review fields write nothing (15.413887ms)
✔ a target changed during review refuses with no write (4.186051ms)
✔ counted mixed targets share one review and one adapter call (8.19498ms)
✔ linked notes with equal line numbers both qualify (8.567766ms)
✔ project lifecycle review names propagation and still writes once (8.783886ms)
✔ priority picks still skip the combined review and keep Work Log-only prompts (5.808634ms)
✔ a typed date from the card's schedule row uses the combined review (14.212043ms)
✔ scheduling a Pending task goes straight to the combined review, never serial prompts (2.764477ms)
✔ classic parser keeps ISO, M/D, and signed units and ignores concise forms (3.810068ms)
✔ typed schedule resolver covers bare days, units, weekdays, and inline reasons (2.762559ms)
✔ weekdays resolve to the next occurrence strictly after today (0.369628ms)
✔ invalid leap dates, end-of-month offsets, and December rollover (0.866585ms)
✔ negative, overflow, malformed, and preset-filter queries are rejected without dates (0.371972ms)
✔ DST local-calendar arithmetic stays on calendar days in America/New_York (392.70967ms)
✔ Task Card date stage previews weekday, ISO, relative distance, and rollover year (44.21075ms)
✔ inline reason is preserved on the preview and skips the reason stage (34.542187ms)
✔ Shift+Enter skips the reason by the blank-reason rule and still offers Work Log (11.497352ms)
✔ Shift+Enter on a Ready task commits in four gestures without a Work Log (6.66123ms)
✔ invalid typed dates render an error preview and do not write (5.925211ms)
✔ the card's schedule stage always uses the concise resolver (4.232125ms)
✔ tomorrow stays a preset filter and is not stolen as a typed date (3.500661ms)
✔ mixed Task Links preview one date and freeze that action with the inline reason (15.639821ms)
✔ Ctrl+Enter still takes the recommended roll from the Task Card date stage (6.803395ms)
✔ Schedule stage defaults to Tomorrow with no Today row (5.070966ms)
✔ Enter on the default picks Tomorrow and Shift+Enter commits it (17.286785ms)
✔ Today stays reachable by typing 0 (2.049852ms)
✔ priority task keeps the pinned roll preselected with no Today row (2.776145ms)
✔ date helper scope: scheduled drops Today, other date properties keep it (0.543718ms)
✔ t and Enter open the theme stage; Ctrl+D clears to default (39.900542ms)
✔ Use default clears every target including none, exempt, repair, and mixed (15.352945ms)
✔ selecting inherited clears; other choices set with catalog spelling including PLAN (4.09022ms)
✔ new theme with no suggestion sets; same-key is a plan no-op (4.010358ms)
✔ stage dedupes by key, preserves query, and keeps unknown inherited selectable (10.75375ms)
✔ known inherited theme remains in Today or Recent; unknown inherited row is not preselected (20.342863ms)
✔ type sets need no caps gate; default clears (44.908646ms)
✔ stale line and changed default refuse; cancellation writes nothing (1.791612ms)
✔ persisted post-images preserve status, links, root, and freshness bytes (1.892703ms)
✔ linked and mixed counted plans carry per-target identity without guessing (3.803071ms)
✔ theme notices explain every single-target no-op source and default (4.588215ms)
✔ theme no-op batches distinguish shared sources, different sources, explicit fields, and defaults (0.656706ms)
✔ theme save notices distinguish removed overrides, repaired fields, and default sources (0.750339ms)
✔ stage rows keep subtitle and search fields while marking only a single inherited choice (1.134708ms)
✔ Use default names the default type source without from (0.289236ms)
✔ task-card-relocate: unlinked backlog retype is field-only (5.032314ms)
✔ task-card-relocate: live link identity uses open entry, vault path, and block ID (1.032862ms)
✔ task-card-relocate: planned link moves into existing planned BUILD (5.350801ms)
✔ task-card-relocate: sole placeholder renames in place (1.657186ms)
✔ task-card-relocate: crowded placeholder creates below the source (1.324554ms)
✔ task-card-relocate: running sole renames, running crowded appends (0.694355ms)
✔ task-card-relocate: already under copy (0.322907ms)
✔ task-card-relocate: daily write is one undo with preimage guard (2.89068ms)
✔ Modal harness models Obsidian 1.14 attachment and idempotent close (9.304535ms)
✔ styles share key-card tokens and compact Task Card dimensions (0.903644ms)
✔ card renderer paints header, banner, strip, stable rows, more, and footer from the model (36.535194ms)
✔ Task Card type header shows unknown and repair signals without invoking setters (8.167814ms)
✔ renderer does not consume randomness or invent recommendation data (4.396916ms)
✔ no-recommendation, cancel, mixed, long text, missing API, and error states render (15.230603ms)
✔ counted and linked cards disclose mixed values and Task Link notes (25.94219ms)
✔ Task Link relation rows use the linked task's content and index (27.820275ms)
✔ Task Link Task Card relation actions focus resolved tasks and clear by ref (79.658728ms)
✔ Ctrl+Shift+P always opens the Task Card, never the classic property list (4.542977ms)
✔ the plugin carries no Task Card pilot setting, date gate, or classic preference (66.572515ms)
✔ a leftover persisted taskCard flag is ignored and never rewritten (45.158161ms)
✔ palette command is named Task card (set properties) (85.570046ms)
✔ Task Card opens the compact card with dialog semantics and a close control (11.154571ms)
✔ Type property row is selectable while its editor remains read-only (10.083217ms)
✔ Task Card theme stage shows a typed new theme on input and commits the real Enter callback (66.450536ms)
✔ Task Card theme row click and Ctrl+D use real setters and keep repair history safe (41.989062ms)
✔ Task Card theme catalog repaint keeps query and keyboard selection; changed defaults refuse (34.683918ms)
✔ counted Task Card theme edits use one editor transaction for all selected tasks (24.984811ms)
✔ linked Task Card theme edits recompute full-note inheritance and write two targets in one note (23.6423ms)
✔ linked Task Card theme writes report a later-note failure as a partial save (16.589109ms)
✔ closing a linked theme stage during note reads cancels the pending write and duplicate Enter (12.935933ms)
✔ a More row opens that property's value stage, never a filter list, and Back restores the card (12.497381ms)
✔ after open the actions list, not the Close button, has focus (16.274424ms)
✔ clicking card text keeps the card key router active exactly once (14.292554ms)
✔ Ready card writes close from a key, P1 click, recommendations, and Alt+N (29.191955ms)
✔ Next and Pending priority gestures open a focused Work summary; Enter writes once and Escape writes nothing (19.554949ms)
✔ Ctrl+Enter on overdue Next and counted tasks paints the Work summary stage (10.83929ms)
✔ Ctrl+R recomputes and repaints the card recommendation (10.728512ms)
✔ Task Card action keys enter the retained property, refresh, dependency, cancel, and lane stages (67.114989ms)
✔ Task Link opens focused while resolving and consumes keys without replay (14.816839ms)
✔ Ctrl+Shift+B on a Task Link opens the linked Depends on stage and closes the card (6.284678ms)
✔ Ctrl+Shift+Alt+B on a Task Link opens the linked Blocks stage (7.173373ms)
✔ LG18-LG20: Task Link relation chords resolve, guard, and open the selected target (6.155046ms)
✔ Task Link count replacement and source edits invalidate old resolutions (3.2929ms)
✔ Task Link resolution failure and plugin unload close their shells (8.512017ms)
✔ direct Depends on entry opens the dependency stage without painting the card or the list (6.082122ms)
✔ a direct stage for an unconfigured property closes instead of leaving an empty modal (1.203017ms)
✔ a refused direct stage closes instead of landing on a card or a list (2.295458ms)
✔ Ctrl+Shift+B lands on the Depends on stage with the same intent as card b (6.3532ms)
✔ Ctrl+Shift+B Back returns to the card without re-dispatching (7.951252ms)
✔ Ctrl+Shift+B on a plain bullet notices and closes the card (2.370193ms)
✔ Ctrl+Shift+B on a Depends-On line opens the direct stage without auto-dispatch (6.395869ms)
✔ Ctrl+Shift+Alt+B on Depends-On and BLOCKS lines opens the owner's stage directly (5.690711ms)
✔ Ctrl+Shift+B captures review origin like Ctrl+Shift+P; a direct stage does not (7.045941ms)
✔ priority gesture writes the frozen date and duplicate dispatch is single-flight (15.932464ms)
✔ pending priority action passes its card preview through the Work Log adapter (6.914593ms)
✔ Task Link priority action refuses a stale cross-note preflight before writes (12.927162ms)
✔ Task Link priority action rolls back earlier note writes after a later write fails (5.483707ms)
✔ Task Link transaction reports a cleanup failure without implying global undo (3.467962ms)
✔ selected-property deletion uses the existing writer; other card rows stay non-deletable (10.731266ms)
✔ failed deletions keep the card: 0 on unprioritized and Ctrl+D on unscheduled write nothing (32.827323ms)
✔ a refused deletion rebuilds the card from the refreshed line (8.052999ms)
✔ 0 deletes only priority and keeps the scheduled field byte-for-byte (9.246696ms)
✔ card keys pressed on a priority radio or the banner reach the resolver exactly once (22.385793ms)
✔ held or composing Enter on a radio or the banner never writes (11.665387ms)
✔ Escape, q, Q, and Ctrl+[ close the card without writing (24.748369ms)
✔ Ctrl+Q, Meta+Q, Alt+Q, and Ctrl+] do not close the card (5.388527ms)
✔ repeated close keys and a second close() are harmless (8.367046ms)
✔ composition never closes the card or a stage (6.653429ms)
✔ q typed into a stage's text field never closes the modal (6.919974ms)
✔ Ctrl+[ closes from a focused date field without writing (6.764511ms)
✔ Ctrl+[ closes the schedule review from its Reason and Work summary fields (35.906812ms)
✔ Ctrl+[ closes the summary-only schedule-work-log stage without writing (7.063413ms)
✔ Ctrl+[ closes the lane-release Work summary without writing (10.471637ms)
✔ q closes from a focused More row and from the Close button (17.353663ms)
✔ Ctrl+[ closes from focused card controls, the Back button, and the modal frame (20.151528ms)
✔ a More stage, a refresh stage, a cancel stage, and a dependency field close on Ctrl+[ and Escape (49.61096ms)
✔ a resolving Task Link closes on Escape, q, and Ctrl+[ and swallows every other key (19.826713ms)
✔ a direct dependency stage closes on Ctrl+[ but keeps q as typed text (3.24995ms)
✔ q and Ctrl+[ are not global closes: other modals and the decay card ignore them (6.738078ms)
✔ missing freshness API disables Review every with an honest reason (6.33461ms)
✔ child-note, task-move, and Pomodoro pickers keep generic bob-cnp-modal dimensions (12.412747ms)
✔ decay card keeps its classes and shares key-card tokens (0.598982ms)
✔ decay card footer always names the X drop alias; the trial date is not this gate (0.884504ms)
✔ task card level chips reuse the shared priority mark when available (5.805005ms)
✔ task card labels are unchanged without the priority mark api (13.227994ms)
✔ job.md inherited theme no-op explains the source, writes nothing, and closes (49.339215ms)
✔ choosing the inherited theme removes an override and reports its source (11.306107ms)
✔ Ctrl+D with no override and selecting the explicit theme explain unchanged tasks (15.978362ms)
✔ counted and linked unchanged batches explain the inherited source without writes (18.78567ms)
✔ a single linked theme edit uses fresh source-specific no-op and saved notices (14.1705ms)
✔ theme menu uses colored pills, grey PLAN, source markers, and distinct kind badges (8.090576ms)
✔ theme menu stays grey when hueFor is missing or throws, and header matches null hues (11.762699ms)
✔ assign batch preview carries set P1 for the banner (0.784888ms)
✔ task card BLOCKED chip renders the miniature mark with a reason list (31.06738ms)
✔ task card stale chip renders the dashed mark with no reason list (2.574049ms)
✔ task card lists up to three prerequisites then a +N overflow line (3.373045ms)
✔ task card mixed counted batch keeps the plain BLOCKED chip (4.173415ms)
✔ task card teaching digit sits beside each P1-P4 level's bars (3.653436ms)
✔ task card resolves the block api from options.app (3.236312ms)
✔ task card is unchanged without the block marks api (13.689302ms)
✔ cursor on a note splits that bullet (16.819372ms)
✔ cursor on a nested line splits its first-level note (2.253385ms)
✔ cursor on a drawer entry stays inside its drawer (1.571901ms)
✔ counted split takes the bullet plus the next siblings (1.733802ms)
✔ a clamped count splits what exists and says so (8.551409ms)
✔ a visual selection splits every touched head line (2.447361ms)
✔ a selection crossing owners is refused (0.500288ms)
✔ a managed line explains why nothing is written (8.054274ms)
✔ a task line gets the already-a-task teaching notice (0.929035ms)
✔ task lines open an unmarked picker over all splittable notes (5.349855ms)
✔ drawer titles open a picker scoped to that drawer (1.036386ms)
✔ section bullets promote into the same note's Tasks intake (1.488795ms)
✔ Tab marks candidates and Enter splits marks or the highlighted row (18.142171ms)
✔ guarded Undo restores all postimages or refuses before writing (4.824291ms)
✔ daily-note split writes destination first, guards both notes, and lands on the new task (11.718425ms)
✔ daily-note split rolls back the destination when the source went stale (1.496801ms)
✔ a same-note split applies in one undoable transaction (7.62527ms)
✔ task-split vectors pin planSplitBullets byte-for-byte (49.110955ms)
✔ task-split candidates list splittable bullets in order (1.132428ms)
✔ obsidian-block-marks-e2e --self-test (418.601175ms)
✔ obsidian-decay-ladder-e2e --self-test (324.324561ms)
✔ obsidian-event-link-times-e2e --self-test (359.227094ms)
✔ obsidian-frees-marks-e2e --self-test (287.593311ms)
✔ obsidian-off-clock-link-chips-e2e --self-test (282.467322ms)
✔ obsidian-quick-roll-e2e --self-test (132.138097ms)
✔ a complete passing observation passes (7.123761ms)
✔ layout-ready timeout fails without relaxing the threshold (4.901462ms)
✔ absent instrumentation fails instead of passing on zero counters (0.447956ms)
✔ late instrumentation fails (0.48125ms)
✔ empty-index pass is inadequate (0.486371ms)
✔ missing plugin and wrong plugin version fail (2.337073ms)
✔ early and non-Markdown ledger reads fail (4.493199ms)
✔ high, missing, and empty heap samples fail (0.716203ms)
✔ each editor case is required (3.849814ms)
✔ wrong mode, wrong path, and disconnected editors fail (0.948989ms)
✔ swallowed mount errors, async exceptions, and crashes fail (2.744124ms)
✔ deploy rows fail on malformed, missing, and drifting rows despite ok:true (4.747151ms)
✔ wrong-vault renderers are rejected (0.415024ms)
✔ bounded RPC failures reject instead of hanging (29.430547ms)
✔ cleanup removes only run-owned temporary paths (0.801319ms)
✔ CLI options have short aliases and alphabetized help (0.946062ms)
✔ Markdown filter matches the lifecycle rule (0.394067ms)
✔ obsidian-task-link-marks-e2e --self-test (254.567615ms)
✔ obsidian-task-wikilink-e2e --self-test (217.489292ms)
✔ manifest order is authoritative and fragments share one lexical scope (492.778231ms)
✔ builds are deterministic and build:check is read-only on success (690.614662ms)
✔ read-only check rejects changed fragments and edited generated output (1092.273471ms)
✔ check rejects a missing generated bundle without writing it (273.301705ms)
✔ fragment line limit is enforced before writing output (7.04493ms)
✔ fragment syntax errors are rejected before writing output (96.620444ms)
▶ malformed, empty, duplicate, and traversal manifests are rejected read-only
  ✔ invalid JSON (3.314066ms)
  ✔ empty manifest (1.496638ms)
  ✔ non-array manifest (10.132237ms)
  ✔ duplicate entries (83.838204ms)
  ✔ traversal entry (7.155212ms)
  ✔ absolute entry (1.621035ms)
✔ malformed, empty, duplicate, and traversal manifests are rejected read-only (116.041258ms)
▶ missing and omitted fragments are rejected read-only
  ✔ missing manifest entry (1.80866ms)
  ✔ unlisted JavaScript source (97.013364ms)
✔ missing and omitted fragments are rejected read-only (102.237761ms)
✔ escaping fragment symlinks are rejected read-only (2.97134ms)
✔ parity comparator identifies changed helper and plugin methods (1.330097ms)
✔ parity comparator accepts a mixin-split helper class but not a changed method or superclass (1.099722ms)
✔ every committed plugin installs each mixin class its fragments define (82.804936ms)
✔ snapshot commands are available only for active Markdown files (4.332584ms)
✔ commands run bob ref create on the active path, with -C for closed tasks (23.332905ms)
✔ bob spawn uses the resolved path, vault environment, timeout, and NO_COLOR (5.049328ms)
✔ failure notices retain bob error and hint lines verbatim (1.146554ms)
✔ snapshot runs through api.commandMode when version 1 is available (16.232794ms)
✔ snapshot falls back to the legacy spawn without command mode (1.034266ms)
✔ snapshot falls back to the legacy spawn when command mode is older than v1 (0.599886ms)
✔ a refused command-mode run keeps the legacy error notice and never spawns (2.502895ms)
✔ off desktop, bob spawning is refused with the desktop-app explanation (0.602297ms)
✔ both prompt copies pass the shared fixture table identically (15.92154ms)
✔ suggestion is valid, compact, and collision-aware (1.406299ms)
✔ rename excludes exactly one old-ID occurrence (0.533807ms)
✔ dependency legacy [id::] reuses only valid free IDs (0.962966ms)
✔ project conversion keeps the existing suggestBlockIdFromTask (1.972436ms)
✔ successor SB vectors are unchanged (2.230539ms)
✔ Linked-from CURRENT lists every checkbox status from the live index (70.902418ms)
✔ checkMotionRings judges computed motion (offline) (9.44873ms)
✔ production CSS computes no animation or transition under reduced motion (5174.338757ms)
✔ option-bracket ring reads Blocked as a source-only slot ahead of Ready (6.117651ms)
✔ isCyclableTaskStatus accepts Blocked while Ctrl+Enter predicates still reject it (4.010567ms)
✖ option-bracket refuses to change a member while its project is Blocked (7.458401ms)
✖ tagged inherited ^prj remains Blocked, refuses cycling, and names its parent (12.51883ms)
✔ project resident notice reads the inline ^prj date and ignores frontmatter scheduled (1.553723ms)
✔ findSingleFutureScheduledField validates form, field order, and the strictly-future boundary (0.976317ms)
✔ field removal collapses only the exposed span and preserves the rest of the line (0.977492ms)
✔ vault-path retirement preserves CRLF and a missing final newline (6.748199ms)
✔ Schedule Log insertion recognizes all three marker spellings and lands directly beneath the marker (5.090307ms)
✔ Schedule Log discovery ignores a marker owned by a nested grandchild (0.862767ms)
✔ Schedule Log entry falls back to marker indent plus one tab and reuses the marker's own bullet when the log has no entries (1.100099ms)
✔ a task with no Schedule Log gets its field retired without any insertion or new marker (0.410754ms)
✔ Schedule Log entry uses the canonical arrow, dash, and lock bytes (0.216538ms)
✔ retirement stays a no-op for shapes that are not proof of a blocking date (0.430174ms)
✖ cycling Blocked backward to Cancelled retires the date and logs, matching forward (3.889556ms)
✖ single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write (0.797209ms)
✔ counted range cycling maps editor coordinates through Schedule Log insertions, including a nested child task above the marker (17.889194ms)
✔ counted range accounts for a cursor-line Tasks-command insertion when targeting later lines (36.88628ms)
✔ transcluded Blocked cycling retires the target's schedule and logs it, in another note and in the active note (12.73403ms)
✖ pressing again after Blocked retirement performs an ordinary transition with no further changes (3.927556ms)
✖ Alt+] on a date-blocked ^prj recovers open residents in step (1.287445ms)
✖ Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains (1.003561ms)
✔ planProjectResidentRecoveryEdits recovers when a cross-note id is not open (1.951902ms)
✖ Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed (4.08221ms)
✖ Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason (1.03625ms)
✖ Alt+[ on a [?] ^prj to Cancelled recovers tagged residents (1.077282ms)
✔ cycling a transcluded ^prj recovers residents in the source note (10.849207ms)
✔ cycler BK1–BK12 accept and empty (5.415962ms)
✔ cycler BK13–BK15 malformed stay guarded, BK16–BK18 unguarded (2.073371ms)
✔ cycler MC4 strike/restore skip BLOCKS lines (2.732002ms)
✔ cycler MC3 tree close skips BLOCKS embeds (2.789438ms)
✔ cycler MC1/MC2 Pomodoro and successor scanners skip managed lines (3.648997ms)
✔ cycler Rule 8 Ctrl+Enter is root-only and Alt+]/Alt+[ never reformat BLOCKS (0.70833ms)
✔ cycler api v4 exposes the Done line rewrite, post-Done pass, and parked offers frozen (2.830308ms)
✔ done vectors pin completeTaskLineText (4.080552ms)
✔ Ctrl+Enter local fallback shares the api Done bytes (1.364999ms)
✔ range planner preserves every single-item mode without an effective count (15.617951ms)
✔ item counts carry children, skip blank lines and loose continuations, and clamp (0.857846ms)
✔ range stops at headings, shallower lines, same-level paragraphs and fences (0.519825ms)
✔ siblings require the exact whitespace and blockquote prefix (0.312521ms)
✔ counted demotion moves four complete blocks to one existing section (9.864547ms)
✔ counted demotion creates a typed section or one default Requirements section (3.762174ms)
✔ bottom-up removal splices blank seams and maps destinations before the source (0.857692ms)
✔ counted promotion Enter appends tasks in order and removes an emptied source section (2.023806ms)
✔ counted promotion to existing or new non-Tasks destinations keeps all bullets plain (1.027375ms)
✔ same-source Tasks promotion rewrites all selected lines in place (1.730319ms)
✔ counted demotion outside Tasks moves to the next section in one write (2.331731ms)
✔ in-place ranges write once without centering for nested, non-dash, and unrouted items (5.456274ms)
✔ mixed demotion ranges count unchanged siblings and only move top-level dash tasks (0.966229ms)
✔ mixed promotion preserves existing tasks and a nonempty source section (0.730474ms)
✔ Vim action consumes explicit additional-item counts and preserves bare behavior (4.086244ms)
✖ command checking preserves pending count; execution consumes it once and resets Vim (2.182041ms)
✖ command route stays single without normal-mode explicit count and supports in-place ranges (0.623674ms)
✔ picker displays at most five preview rows plus overflow; single picker is unchanged (3.951098ms)
✔ stale counted picker and cancelled picker never write (2.103983ms)
✔ counted moves round-trip CRLF and preserve the presence or absence of a final newline (9.727556ms)
✔ direct open/done transitions include incomplete statuses without broadening excluded statuses (12.897614ms)
✔ Ctrl+Enter block-link selection recognizes live and retired forms (13.537145ms)
✔ Pomodoro child ownership is status-neutral and bounded by contiguous list structure (1.730202ms)
✔ daily-note paths follow the canonical YYYY/YYYYMMDD.md layout (4.73124ms)
✔ parsePomodoroEntryLineParts reads placeholder and range names conservatively (1.847742ms)
✔ formatPomodoroPlaceholderLine keeps unnamed placeholders canonical (6.670955ms)
✔ Pomodoro bullet toggle accepts empty indented list items (0.887373ms)
✔ Pomodoro bullet toggle rejects non-empty or out-of-section bullets (0.39468ms)
✔ Pomodoro bullet toggle reverses only empty open childless placeholders (0.884302ms)
✔ Pomodoro bullet toggle reverses named empty open childless placeholders (9.545485ms)
✔ Pomodoro bullet toggle round trips and normalizes child indentation (0.567458ms)
✔ Pomodoro bullet toggle changes only the eligible line in a realistic daily shape (0.427683ms)
✔ Pomodoro toggle key gate does not shadow bare Option bracket cycling (0.595115ms)
✖ Pomodoro toggle command is daily-only and places the cursor for both directions (6.49252ms)
✔ Pomodoro Vim fallback consumes eligible keydowns once and lets others fall through (3.096419ms)
✖ Vim Ctrl+Enter dispatches task transitions and restores a reopened identity (10.93087ms)
✖ Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents (4.956161ms)
✖ Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references (0.813443ms)
✖ Ctrl+Enter reopening the local line over an already-open target does not accidentally close it (0.835737ms)
✖ Ctrl+Enter closing the local line over an already-closed target does not write it a second time (4.159875ms)
✖ Ctrl+Enter hands off a claimed walk landing before Pomodoro handling (1.051328ms)
✖ Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws (3.98916ms)
✖ Ctrl+Enter consumes a rejected nav claim without an unhandled rejection (1.103123ms)
✖ Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error (0.796555ms)
✖ Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line (1.941215ms)
✖ Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion (0.828526ms)
✔ getReviewWalkApi only accepts nav api v3 with a well-formed reviewWalk and never throws (0.785111ms)
✖ Ctrl+Enter close continues the walk with complete after finalize ran (6.142411ms)
✖ Ctrl+Enter close continues only after transclusion propagation landed (1.187626ms)
✖ Ctrl+Enter reopen settles the walk with null (0.670383ms)
✖ Ctrl+Enter swallows the key with no write while the walk is busy (0.65254ms)
✖ Ctrl+Enter with a null capture behaves exactly like today (0.627886ms)
✖ Ctrl+Enter with nav v2 or no nav keeps today's behavior (0.686242ms)
✖ Ctrl+Enter lets the checklist claim win before capturing (0.604923ms)
✖ Ctrl+Enter settles the walk with null when the toggle rejects (0.490329ms)
✖ Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write (4.063471ms)
✔ eligible Tasks demotions prompt in project and non-project notes (6.336356ms)
✔ selectable headings skip YAML, fences, empty titles, and Tasks (2.633882ms)
✔ duplicate heading identities stay distinct and route to the chosen occurrence (2.430515ms)
✔ demotion picker defaults and typed names resolve without synthetic duplicates (4.438231ms)
✔ picker keyboard state wraps, clamps, and refuses invalid Enter (0.801201ms)
✔ new-section formatting keeps extra blanks, final newlines, and nested children (1.382524ms)
✖ existing-section insertion works before and after the source on CRLF-backed editors (2.716124ms)
✖ command opens one picker, writes only on accept, and restores cursor plus center (0.799189ms)
✖ pointer activation, Escape, and double-submit protection leave a consistent note (0.707896ms)
✖ stale document, changed editor, or missing heading notice without writing (0.704504ms)
✔ dependency normalizer writes path-qualified IDs and is idempotent (10.295884ms)
✔ Tasks-generated IDs become local block IDs when none exists (6.655226ms)
✔ note rename rewrites target IDs and yields exact propagation mappings (0.806565ms)
✔ note rename also rewrites same-file dependsOn references (5.093582ms)
✔ dependency normalization skips unsupported paths and fenced examples (1.050322ms)
✔ blocked-dependent planner matches the CLI dependency truth table (11.967725ms)
✔ blocked-dependent edits preserve EOLs and skip stale lines idempotently (5.532313ms)
✔ project recovery strips resident tags and works without freshness v12 (6.865953ms)
✔ recovery passes daily-note and Today skip flags to ledger freshness (8.065685ms)
✔ normalization mappings propagate to every dependent file (5.050195ms)
✔ runtime normalizer skips unsupported paths with one informative notice (6.849594ms)
✔ rename reconciliation rewrites the target and every dependent (1.399389ms)
✔ editor dependency normalization abandons and reschedules stale snapshots (1.555125ms)
✔ rename reconciliation abandons and reschedules stale editor snapshots (3.96069ms)
✔ Depends-On line recogniser covers the contract DP vectors (1.793664ms)
✔ close-time retirement skips Depends-On lines (6.019584ms)
✔ reopen restoration skips Depends-On lines instead of re-embedding them (4.007059ms)
✔ embedded-tree close collection ignores Depends-On lines (0.881003ms)
✔ Alt-bracket bullet formatting never applies to Depends-On lines (5.475592ms)
✔ Ctrl+Enter on a dependency link closes only the target and runs the recovery (7.220868ms)
✔ Ctrl+Enter on a dependency link reopens only the target, root-only (9.685375ms)
✖ single and counted Alt-bracket cycle the dependency target under the cursor (2.736525ms)
✖ single and counted Alt-bracket report when the cursor is off every dependency link (0.817223ms)
✔ Ctrl+Enter candidate resolution finds plain links on Depends-On lines (0.612698ms)
✔ dependency-id normalisation never edits Depends-On lines (6.923989ms)
✔ note rename rewrites fields while leaving Depends-On lines alone (0.528434ms)
✖ recoverBlockedDependents leaves a closed tagged resident untouched (PDT7) (9.285029ms)
✔ task demotion refuses the Pomodoros destination (6.0954ms)
✔ task demotion may still move into other sections (1.156275ms)
✔ counted demotion refuses a Pomodoros destination if any moved row is a task (1.046134ms)
✔ event clock spans parse the documented grammar (12.648296ms)
✔ event clock classifier matches the shared vectors (0.938123ms)
✔ event clock pre-pass mirrors the shared close vectors (25.305065ms)
✔ Ctrl+Enter completes ended meetings and carries the rest (101.688349ms)
✔ Ctrl+Enter without a clock keeps the ordinary close behavior (11.854379ms)
✔ cycler freshness: local-fallback rewrite stamps last via injected stamper (4.099739ms)
✔ cycler freshness: rewrites without a stamper are unchanged (identity default) (2.041993ms)
✔ cycler freshness: a throwing stamper leaves the rewritten line intact (1.116011ms)
✔ cycler line guard skips Pomodoro signatures before injected stampers (0.595329ms)
✔ cycler skips legacy Pomodoro headlines in local and Tasks-command writes (3.77352ms)
✔ cycler freshness: transcluded rewrite stamps last via injected stamper (0.556254ms)
✔ cycler freshness: cycling a plain line stamps through the follow-up edit (0.920115ms)
✔ cycler freshness: Tasks-command rewrite with the expected status is stamped (0.756114ms)
✔ cycler freshness: Tasks command that inserts a line never stamps (0.795583ms)
✔ cycler freshness: Tasks command that deletes the line never stamps the next task (0.90751ms)
✔ cycler freshness: Tasks command that leaves a different status never stamps (0.498232ms)
✔ cycler freshness: cycling without ledger-tools writes no stamp (0.389399ms)
✔ cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old (0.264492ms)
✔ KM1/K9/K11: keep-moving uses the baseline predecessor link, lane order, and shared row indexes (46.3266ms)
✔ KM1: an explicit pick reuses the writer, raises Ready, mints, stamps, and places after the predecessor (8.861728ms)
✔ KM2-K8/K10/K12: only the pre-close own link behind the last live project link triggers (13.731943ms)
✔ KM6/K7/K14/K16/K19/K20/K29: root, project-group, empty, blocked, disabled, and cancel exclusions (13.109351ms)
✔ KM13/KM17/KM18/KM31: blocked, scheduled, hidden, ref, nested, and due rows classify with precedence (4.763253ms)
✔ KM15/KM22/KM23: hand-offs win dedup, projects sort by anchor, and task root fields do not change leafness (3.895728ms)
✔ KM22/KM23: multiple leaf-project groups order by ledger anchor before path (6.123397ms)
✔ LP1-LP12: R2 leaf walk handles roots, wrappers, ambiguous/missing parents, cycles, and depth (4.258619ms)
✔ KM copy, folds, title, lane labels, notices, and config parser/cache match the accepted API (17.759838ms)
✖ KM24/KM28: real close wiring offers once, applies a pick, and same-day reopen takes it back (18.087317ms)
✖ KM24: a keep-moving pick that becomes Blocked while the picker is open is refused (6.214356ms)
✔ KM19/KM32: picker v1 and a failed G3 day-byte gate add no keep-moving planning work (9.075008ms)
✖ KM1: Obsidian daily-note link close offers keep-moving and links after the struck predecessor (58.209289ms)
✖ KM26: own-note Ctrl+Enter offers keep-moving with notice v2 card and v1 plain text (7.738198ms)
✖ KM26: Alt+] into Done offers keep-moving and links the resident (1.788928ms)
✖ KM27: walk landing awaits the picker and returns the plain text with no card (2.921734ms)
✖ KM25: Esc leaves the resident and the day byte-identical with no notice (6.637844ms)
✔ notice-form parity: one, several, mixed, and failure copy matches nav v2 (4.733095ms)
✔ cycler api v4 offerParkedSuccessors is frozen and never throws (5.48998ms)
✖ offerParkedSuccessors offers a starts-after source at the parked slot (12.02173ms)
✔ offerParkedSuccessors stays silent when the target is still live-linked today (3.093926ms)
✔ offerParkedSuccessors stays silent when the target is not Pending (1.426804ms)
✖ offerParkedSuccessors Esc on the picker offers without picking (1.425089ms)
✔ offerParkedSuccessors plans no relation group when nav successors is below v3 (1.365427ms)
✔ offerParkedSuccessors resolves quiet on empty identities and never throws (0.943618ms)
✔ shared vector (elsewhere): unlinked-stays-on-the-clock (4.329552ms)
✔ shared vector (elsewhere): all-off-clock-non-meet (0.34133ms)
✔ shared vector (elsewhere): mixed-stays-on-the-clock (0.981687ms)
✔ shared vector (elsewhere): unresolved-stays-on-the-clock (0.19806ms)
✔ shared vector (elsewhere): alias-off-clock (0.489492ms)
✔ shared vector (elsewhere): nested-tag-rejected (0.226088ms)
✔ shared vector (elsewhere): meet-run-ignores-future-off-clock-queue (0.180611ms)
✔ shared vector: close-defers-not-started-off-clock (19.810541ms)
✔ shared vector (elsewhere): close-mixed-after-dropping-on-clock (0.311411ms)
✔ shared vector (elsewhere): kept-ledger-swap-switches-key (0.320846ms)
✔ shared vector: bare-row-restamped-at-close (8.139644ms)
✔ shared vector: conflict-row-at-close (3.528811ms)
✔ shared vector (elsewhere): running-link-restamps (0.166996ms)
✔ shared vector (elsewhere): love-default-untagged-child-is-off-clock (0.11402ms)
✔ shared vector (elsewhere): event-task-root-abby-inherits-love (0.174256ms)
✔ shared vector (elsewhere): false-child-true-grandchild-is-off-clock (0.115905ms)
✔ shared vector (elsewhere): untyped-dog-passes-inheritance-through (0.135139ms)
✔ shared vector (elsewhere): on-tag-under-love-stays-worked (0.079914ms)
✔ shared vector (elsewhere): on-off-conflict-stays-worked (0.068305ms)
✔ shared vector (elsewhere): invalid-note-offclock-stays-worked (0.063972ms)
✔ shared vector (elsewhere): invalid-root-on-daily-stays-worked (0.065134ms)
✔ shared vector (elsewhere): love-plus-job-stays-worked-mixed (0.136194ms)
✔ shared vector (elsewhere): explicit-off-beats-false-child (0.073253ms)
✔ shared vector (elsewhere): type-list-meet-at-love-child-is-off-clock (0.085723ms)
✔ shared vector (elsewhere): type-list-chore-at-love-child-is-worked (0.157283ms)
✔ shared vector (elsewhere): type-list-meet-plus-chore-is-mixed (0.117055ms)
✔ shared vector (elsewhere): child-list-narrows-parent-true (0.109427ms)
✔ shared vector (elsewhere): child-false-under-parent-list-is-worked (0.08426ms)
✔ shared vector (elsewhere): dual-key-list-wins-without-capture-warning (0.088919ms)
✔ shared vector (elsewhere): scalar-type-list-is-one-item-list (0.101157ms)
✔ shared vector (elsewhere): empty-type-list-blank-inherits-true (0.121584ms)
✔ shared vector (elsewhere): empty-type-list-flow-empty-inherits-true (0.092063ms)
✔ shared vector (elsewhere): empty-type-list-null-inherits-true (0.080942ms)
✔ shared vector (elsewhere): empty-type-list-lone-dash-inherits-true (0.154395ms)
✔ shared vector (elsewhere): invalid-type-list-item-stays-worked (0.120871ms)
✔ shared vector (elsewhere): type-list-on-note-is-ignored (0.159987ms)
✔ shared vector (elsewhere): on-tag-on-meet-stays-worked (0.219035ms)
✔ shared vector (elsewhere): off-tag-on-chore-is-off-clock (4.531162ms)
✔ shared vector (elsewhere): meet-from-note-task-type-default-is-off-clock (0.147524ms)
✔ shared vector (elsewhere): closed-untyped-link-under-type-list-is-worked (0.134829ms)
✔ shared vector (elsewhere): chore-from-config-default-type-is-off-clock (0.091592ms)
✔ shared vector (elsewhere): reading-task-with-ref-block-is-off-clock (0.068189ms)
✔ shared vector (elsewhere): task-type-off-with-configured-default-is-off-clock (0.123528ms)
✔ every close vector is either mirrored here or listed as handled elsewhere (1.909045ms)
✔ a worked row closes off the clock when every kept link is #offclock (4.191269ms)
✔ a close uses ledger-tools' effective task clock API when available (2.005873ms)
✔ a close still accepts a boolean from the effective clock API (2.08666ms)
✔ a close without the clock API keeps an untagged inherited task on the clock (1.451082ms)
✔ an off-clock row closes back onto the clock when it also links a worked task (2.168253ms)
✔ an unresolved link keeps the session worked and names itself in the notice (2.129742ms)
✔ a struck or embedded #offclock link still counts at close (1.801307ms)
✔ a link the close defers does not count: a mixed session leaves its on-clock link behind (1.442385ms)
✔ an untimed placeholder close has no key to stamp (0.870641ms)
✔ the completion plan stamps the key only when a session clock is given (1.418965ms)
✔ counted links are the direct-child dedicated bullets: plain, struck, marked, or embedded (0.732966ms)
✔ the off-clock tag follows bob's rules for every spelling (0.734169ms)
✔ setPomodoroLineClock moves the recorded minutes between keys like Rust set_ledger_clock (0.529392ms)
✔ planPomodoroCloseClock follows the verdict over resolved, unresolved, and absent links (1.010969ms)
✔ Pomodoro marker helpers normalize every block link and preserve fences and EOLs (20.288514ms)
✔ completed Pomodoro markers are normalized per occurrence (2.723424ms)
✔ move-only Pomodoro links require a strict immediate hash directive (11.503628ms)
✔ Pomodoro move-only planner toggles links across additional physical lines (7.428378ms)
✔ Pomodoro move-only planner round trips exact text and rejects strict non-matches (1.170296ms)
✔ bare Pomodoro move-only toggle round trips a valid alias and preserves the cursor (10.72061ms)
✔ Pomodoro move-only runtime removes locally and validates additions independently (6.330266ms)
✔ Pomodoro move-only runtime protects live lines after asynchronous failures (0.770381ms)
✔ Pomodoro hash Vim mapping distinguishes bare and explicit repeats (20.962582ms)
✔ Pomodoro completion marks originals and carries clean live copies (4.517101ms)
✔ Pomodoro completion groups worked-on links before deferred marked links before a later Pomodoro (2.398597ms)
✔ Pomodoro completion carries the closed Pomodoro name onto created entries (1.476118ms)
✔ buildPomodoroCompletionPlan groups a #-marked bullet above several unmarked bullets (0.944067ms)
✔ buildPomodoroCompletionPlan carries a duplicate target as both an ordinary and a marked bullet (0.594505ms)
✔ buildPomodoroCompletionPlan keeps source order when every carried link is marked (0.933852ms)
✔ buildPomodoroCompletionPlan keeps source order when every carried link is unmarked (0.598609ms)
✖ Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place (8.328ms)
✔ deferred-only close keeps the [x] entry and carries stripped links (0.91352ms)
✔ deferred-only close at EOF keeps the [x] entry and leaves no dangling newline (0.481163ms)
✔ a close with a remaining copyable link keeps the [x] entry (0.474152ms)
✔ a prose sibling keeps the closed entry on a deferred close (0.383136ms)
✖ Ctrl+Enter deferred-only close keeps the [x] entry in one gesture (0.852673ms)
✔ deferred-only close keeps the entry: prose, fences, and continuations stay (1.1327ms)
✔ successor relocation finds the kept closed entry by its restamped headline (0.450927ms)
✔ the completion plan leaves a timed headline's key and span alone unless a session clock is given (0.423378ms)
✔ Ctrl+Enter close names use pre-close Task Link types and R6 outcomes (2.327107ms)
✔ MEET close names are passed through without resolving or shedding types (0.370117ms)
✔ Ctrl+Enter applies narrowed closed and shed continuation names (5.197182ms)
✔ MEET continuations follow the last open block and keep the cursor on next work (1.221039ms)
✔ deferred-only MEET continuations go last and successor relocation finds the kept entry (0.757154ms)
✔ MEET without an open entry below and non-MEET closes keep the immediate slot (0.637674ms)
✔ MEET continuations ignore fenced candidates and insert before the fence (0.521615ms)
✔ MEET continuations ignore tilde fences and indented fakes (0.708983ms)
✔ MEET continuations trim trailing blanks and keep interior content (0.77609ms)
✔ kept MEET successor lands under the created continuation, not the older MEET (4.289678ms)
✔ retained MEET successor beats same-name reuse and keeps case 3 below the close (1.964275ms)
✔ selected Done Pomodoro transclusion reopens only its cross-file root (38.106631ms)
✔ selected same-file Done target reopens root-only in the live editor (3.344371ms)
✔ selected retired link reopens its root and restores the historical occurrence (9.507694ms)
✔ incomplete selected Pomodoro transclusion still closes recursively (12.522303ms)
✔ Done Pomodoro reopens direct roots and clears only its block-link markers (18.026784ms)
✔ reopening timed, placeholder, and legacy ledger rows never stamps the headline (13.939463ms)
✔ Done Pomodoro reopen restores its own block reference after reopening direct roots (5.183101ms)
✔ Done Pomodoro markers remain when the Todo transition does not occur (0.616664ms)
✖ registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape (12.379205ms)
✖ registered Ctrl+Enter immediately recovers a same-file dependent (4.460165ms)
✖ registered Ctrl+Enter immediately recovers a cross-file dependent (0.996708ms)
✖ child-line Ctrl+Enter produces the same rollover and cursor target as parent completion (4.009895ms)
✖ Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start (0.905463ms)
✖ selected embedded Pomodoro children keep recursive close and root-only reopen dispatch (0.941983ms)
✖ selected unresolved or excluded embedded children are consumed as no-ops (4.004518ms)
✖ Ctrl+Enter behavior stays generic outside open Pomodoro child ranges (1.06857ms)
✔ Pomodoro Work Log Task Link recognition accepts every link shape and rejects ambiguous bodies (5.131629ms)
✔ Pomodoro Work Log descendant tree keeps relative depth and drops blank lines (2.901283ms)
✔ Pomodoro Work Log note-group collection scopes to direct children and requires descendants (2.306368ms)
✔ Work Log entry body formats as *stamp* — summary (0.43483ms)
✔ buildWorkLogEntryLines stamps depth-1 entries and drops an empty-bodied entry's whole subtree (0.554745ms)
✔ planPomodoroWorkLogGroupInsertion creates a fresh tab-indented marker for a childless task (0.773425ms)
✔ planPomodoroWorkLogGroupInsertion prepends under an existing canonical marker (0.781055ms)
✔ planPomodoroWorkLogGroupInsertion prepends under the legacy 'Work log' spelling (0.597601ms)
✔ planPomodoroWorkLogGroupInsertion ignores a Work Log marker belonging to a nested child task (0.837754ms)
✔ planPomodoroWorkLogGroupInsertion inherits an existing two-space entry indent without mixing tabs (0.59ms)
✔ full Pomodoro completion copies Task Link sub-bullet notes into linked tasks' Work Logs (28.638986ms)
✔ full Pomodoro completion adjusts the created-Pomodoro cursor for a same-note Work Log insertion (5.752951ms)
✔ full Pomodoro completion keeps two same-task Work Log note sets in source order (2.877464ms)
✔ full Pomodoro completion prepends new Work Log entries above an existing one and preserves CRLF (2.484629ms)
✔ full Pomodoro completion skips an unresolvable link and a link to a non-task block without failing (1.689054ms)
✔ full Pomodoro completion does not start a Work Log for a Task Link with no sub-sub-bullets (3.264469ms)
✔ formatWorkLogStamp matches the shared conformance vectors (0.459281ms)
✔ full Pomodoro completion gives every Task Link of one close a single clock read and stamp (2.513904ms)
✔ closing yesterday's daily note stamps the write instant, not the note's filename date (2.232139ms)
✔ PP22 pins #hide bytes to normalize_task_hide_tag(line, false, true) (5.247199ms)
✔ PDS6/PDS15 resolve only one scalar project parent with NoteIndex rules (2.306988ms)
✔ PP1 links the emptied project's ^prj as Next and strips #hide (28.512649ms)
✔ PP29 closing a child ^prj pulls in its empty parent project (5.802115ms)
✔ PP32/PP36 leave a parent-tagged ^prj blocked and hide the tag in row text (3.072785ms)
✔ PP30 keeps the parent untouched while another child or task remains (2.897944ms)
✔ PP31 skips missing, ambiguous, and non-project parents (2.595057ms)
✔ PP33 cancellation surfaces the parent without linking it (5.838029ms)
✔ PP2 and PP3 leave a project with remaining work alone (7.09854ms)
✔ PP4 hidden leftover still pulls in; PP5 fences vs remaining marks (7.451283ms)
✔ PP6 Sub-projects marker states match display_for_wikilink (3.140384ms)
✔ PP7 and PP28 keep a future-scheduled ^prj byte-identical (2.525432ms)
✔ PP8 still-blocks a ^prj that waits on another open prerequisite (2.12309ms)
✔ PP9 already-planned ^prj raises to Next without a new link (1.727379ms)
✔ PP10 implicit destination for unplanned ^prj; PP11 reports disabled (SO14/SO19) (4.456816ms)
✔ PP12 keeps In Progress; PP13 is silent for a visible already-linked Next (2.749488ms)
✔ PP14 an id-less last task still pulls in (1.827828ms)
✔ PP15 dependent and pull-in are both offered with no cap (SO2, breaker retired) (26.898015ms)
✔ PP17 one pull-in row wins over project_task (2.009738ms)
✔ PP18 cancel recovers only (1.572201ms)
✔ PP20 unrecognised or unplannable notes never pull in (3.584481ms)
✔ PP24 closing an external prerequisite pulls in only when N is empty (2.847157ms)
✔ PP25 cascades project_member recovery after a [?] pull-in (3.339652ms)
✔ PP26 dated recount treats a hidden leftover as remaining work (2.496637ms)
✔ PP27 implicit offer after #hide strip; unpicked keeps WRITE rule (SO14/SO20) (3.515436ms)
✔ successorNoticeText uses the §12.6 pull-in and surfaced copy (2.261957ms)
✖ Ctrl+Enter on the last task link inserts the ^prj and rewrites R (29.506674ms)
✖ PP29 runtime close and reopen use the parent pull-in receipt (5.076003ms)
✖ PP18 Alt+[ cancel of the last task surfaces R without linking (1.22015ms)
✖ PP19 same-day reopen restores R byte-for-byte and takes back the link (7.434148ms)
✔ a close in a project that still has work stays inside the gate (3.604911ms)
✔ P1 path-qualified skip keys: same ^review in another note does not suppress (2.162147ms)
✔ P3 id-less cascade: stale [?] R recovers resident without [id::] (1.548923ms)
✔ P4 frontmatter scheduled validity mirrors Rust (1.742643ms)
✔ P5 recognition mirrors Rust (status/type/prj line) (3.871376ms)
✔ P6 SUBOPEN blank line stops the marker scan (PP6) (1.351206ms)
✔ promotion prompts default to Tasks in ordinary and project notes (22.942332ms)
✔ promotion routes plain bullets to existing, typed, and duplicate non-Tasks sections (2.427799ms)
✖ promotion command writes only on accept and Enter selects Tasks (5.629193ms)
✔ promotion removes only genuinely empty source sections (6.082162ms)
✔ promotions, out-of-Tasks demotions, and ineligible shapes keep prior routing (6.449759ms)
✖ Tasks-only preamble promotions prompt and blank Enter moves into Tasks (4.473521ms)
✖ plain bullets already in Tasks prompt and blank Enter promotes in place (1.637736ms)
✔ promotion from Tasks-only or Tasks body can choose existing or typed non-Tasks sections (4.597085ms)
✖ always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation (5.683061ms)
Could not restore all reopened task references [ 'Broken.md: unreadable' ]
Could not recover all blocked dependents [
  'BrokenRead.md: read failed',
  'Stale.md: line 1 changed before recovery',
  'BrokenWrite.md: write failed'
]
✔ direct Done Tasks task reopens through the metadata-aware fallback (10.801305ms)
✔ recursive completion status policy includes Next without broadening excluded statuses (0.656916ms)
✔ recursive completion closes a Next root and its nested Next descendant (26.072835ms)
✔ recursive completion traverses Done parents and skips excluded siblings (2.514516ms)
✔ closed-reference retirement is ancestry-aware, resolved, fenced, and idempotent (9.544467ms)
✔ reopened-reference restoration is ancestry-aware, conservative, and idempotent (6.494036ms)
✔ retirement preserves task-tree markers and unmarks Pomodoro embeds (0.898188ms)
✔ done Pomodoro retirement removes only the matching embedded marker (0.515049ms)
✔ retirement stops at prose boundaries and pairs strikethrough spans (3.746023ms)
✔ retired Pomodoro links are not copied into the next Pomodoro (6.41784ms)
✔ retirement coordinator rewrites active editor and vault notes together (5.499255ms)
✔ restoration coordinator rewrites active and vault notes, preserves the cursor, and isolates failures (6.376722ms)
✔ close and reopen reference mutations share one serialized queue (0.725814ms)
✔ post-close finalizer runs one gated plan before reference retirement (4.756811ms)
✖ dependent recovery uses live editor buffers and preserves the cursor (13.707821ms)
✔ dependent recovery preserves successful siblings across stale and failed notes (9.584697ms)
✔ no-op vault transforms and irrelevant retirement files avoid process writes (0.81496ms)
✔ ambiguity scans and notices are cached while dependency identity lines stay stable (1.63871ms)
✖ non-Vim open/done command finalizes the closed task identity (0.963012ms)
✖ non-Vim open/done command restores the reopened task identity (0.654706ms)
✔ full Pomodoro completion retires embeds only after carry-forward planning (20.929194ms)
✔ full Pomodoro completion recovers after a deduplicated multi-target batch (24.191233ms)
✔ full Pomodoro completion moves a marked same-note link without history (10.156392ms)
✔ closed-reference retirement never duplicates a daily Task Link into the completed fallback (bob-cli-2l) (0.907293ms)
SA14: classifier offers relation; merged hand_off deferred
SA18: classifier relation-only; merged order hand_off > relation deferred
SA20: cycler-applicable no-replay is empty groups; warning relation_successor_already_released is capture authoring (covered by copy SU-P27)
SA18: merged group_order ["hand_off","relation"] checked in SA18 test
SA20: merged no-replay empty; warning relation_successor_already_released is capture authoring (copy SU-P27)
✔ cycler relation successor vectors.json is byte-identical to bob-cli (154.561776ms)
✔ successor config vectors: three-list one-effect rule (25.877871ms)
✔ successor label policy caches by path/stat and never throws (1.353814ms)
✔ successor key vectors: match, effect, and inverse hint (1.096697ms)
✔ relation successor copy vectors drive every copy-table string (11.147909ms)
✔ independent R1-R7 classifier covers every rule vector (155.879855ms)
✔ disabled runtime planSuccessors is unchanged (no relation offers) (23.694336ms)
✔ merged pipeline executes every rule vector (offer_pipeline, no silent skipping) (129.091383ms)
✔ merged SA14 keeps hand_off with relation second reason; parking leaves Blocked (SA14-P) (6.971573ms)
✔ merged SA15 moves a recovered resident into relation_successors with recovery retained (5.311931ms)
✔ merged SA18 orders hand_off before relation in one picker (12.303387ms)
✔ merged beyond-vector: multiple relation groups, Next/Ready ordering, missing IDs, and multiple reasons (60.394133ms)
✔ merged real dependency recovery plus relation selection reuses the hand-off writer (5.502306ms)
✔ merged Esc (empty selection) writes nothing for relation-only rows; display-only plans create no placeholders (6.9433ms)
✔ merged destinations validate slot, closing, implicit, and overrides (12.391015ms)
✔ merged picker v3 carries relation groups, held counts, and second reasons with complete vector coverage (5.836953ms)
✔ fake relationIndex uses the public edge shape and never returns verdicts (4.033746ms)
✔ cycler LK1–LK19 recognises only relation line shapes (3.250068ms)
✔ cycler MC10, MC11, MC12 and MC14 keep relations inert while allowing root-only gestures (6.080281ms)
✔ SO1 project residents offered with ^prj header; pick mints/raises/stamps/links (SO7 dedup, SO8 unchanged, SO11 header) (55.058414ms)
✔ SO2–SO5 fan-outs with explicit selection (SO32 twenty) (17.9134ms)
✔ SO9–SO11 muted/folded/stale residents (SO24 counts, SO31 inbox/ref) (2.552642ms)
✔ SO14–SO19 implicit and no-destination (SO28–SO30 pull-ins, kill/cancel) (2.877692ms)
✔ SO stable keys survive insertions/status changes; ambiguous rebinding refused (11.395599ms)
✔ SO picker model, pick normalization, and API detection (3.640685ms)
✔ picker rows carry one-based task context from the matching note snapshot (0.7117ms)
✔ plan offers attach the live note snapshot so the picker can refresh (1.339154ms)
✔ themeIntent and preserveSpelling survive cycler pick normalization (0.724501ms)
✔ SO notice copy for offers (SO20, mixed, failure) (2.743973ms)
✔ destination override to an existing entry inserts as its child (8.946099ms)
✔ destination override with a stale preimage skips loudly (2.348713ms)
✔ destination override with a closed entry skips loudly (1.979275ms)
✔ destination override with a new name creates one placeholder after the running entry (2.645699ms)
✔ destination override with a new name racing an open entry joins it (2.06011ms)
✖ reopen takes back the untouched successor link and restores status (54.056222ms)
✖ an edited successor bullet survives while its status still restores (9.136268ms)
✖ an edited successor status line survives while its link is taken back (3.794586ms)
✖ reopen on a different day leaves successor links alone (4.052961ms)
✔ reopening a task closed without a pass shows no take-back (6.49149ms)
✖ Alt+] on a planned prerequisite links its successor (1.16615ms)
✖ take-back deletes a pre-existing entry it empties (3.657063ms)
✔ take-back deletes a stub-replaced entry through the vault (5.49386ms)
✔ take-back keeps entries that are closed or keep another child (0.841381ms)
✔ closing-entry relocation finds the kept closed entry (0.805606ms)
✖ Alt+[ into Cancelled recovers its dependents without linking (0.877178ms)
✖ take-back keeps an entry whose prose survives across a blank line (both paths) (1.984947ms)
✔ take-back deletes a whole block with continuation/fence leftovers (LF/CRLF, final newline) (2.261908ms)
✔ successor default placement follows the effective task type (20.436235ms)
✔ successor default placement creates a typed entry when needed (2.305523ms)
✔ successor retarget Enter merges the task type into the destination (7.800622ms)
✔ successor retarget to existing FIX writes [type:: FIX] (3.887979ms)
✔ successor retarget selecting the inherited key clears the field (4.17113ms)
✔ same-key successor retarget is a byte-preserving no-op (1.975304ms)
✔ invalid theme field repairs to the retarget destination (2.086474ms)
✔ successor retarget to a new WRITE bucket writes the new name (1.861214ms)
✔ PLAN+BUILD retarget writes BUILD (PLAN is exempt) (1.554047ms)
✔ unnamed, all-exempt, and composite destinations never write a theme (4.561762ms)
✔ two retargeted successors remember different themes (24.289272ms)
✔ no suggestion, missing API, and guard refusals never write (7.38069ms)
✔ stale task, suggestion, and destination skip the theme edit (7.213096ms)
✔ theme edit persists when the daily insertion later fails (2.265188ms)
✔ daily-note successors use the daily snapshot for suggestFor (3.209989ms)
✔ [theme:: FIX] and (theme:: FIX) survive close and recovery writers (0.934877ms)
✔ Ctrl+Shift+M move preserves exact theme bytes (318.503788ms)
✖ link close links the unblocked successor into the slot and shows the nav card (47.621597ms)
✖ Ctrl+Enter close preserves bracket and parenthesis theme fields (1.784592ms)
✖ Ctrl+Enter carries per-task theme intents through both pick normalizers and saves them with successor links (1.656195ms)
✖ successor retarget Enter merges the destination header and preserves the task field (1.465887ms)
✖ default placement and a changed suggestion still link selected successors without retargeting themes (1.07015ms)
✖ project-finished successor writes its selected theme with real task-theme transforms (5.21717ms)
✖ successor theme save remains truthful when the later daily-link write fails (1.189833ms)
✔ close with no [id::] performs zero vault reads and shows nothing (4.626374ms)
✖ Warm finalize reads no unrelated note bodies on the real close path (15.130834ms)
✖ cold fallback still recovers and links without a Tasks cache (5.438176ms)
✖ recovered-only close reports unblocked without linking (SO4 Esc) (3.947912ms)
✖ walk landing composes a single toast and shows no card (41.804433ms)
✖ nav absent falls back to a plain Notice with no link (SO missing picker) (4.075337ms)
✖ stale cache heals via re-plan from fresh text (SO30) (6.154122ms)
✖ Pomodoro-line close appends the successor to the created continuation (16.326499ms)
✖ Pomodoro-line close keeps the closing anchor after the picker re-plan (11.278583ms)
✖ completeTaskAtCursor returns the notice and shows nothing itself (4.32774ms)
✖ successor apply recovers project residents without ledger v12 (2.91094ms)
✖ managed Done offers an idless relation source through picker and records a reopen receipt (10.113246ms)
✖ managed Done composes ordinary and relation successors in one v3 picker (4.182615ms)
✔ a positive relation-index candidate is revalidated against the open editor after picker (20.680155ms)
✔ no incoming relation edge performs no extra relation-source note read (3.692832ms)
✔ missing or malformed relation index reports uncertainty and falls back below notice v3 (7.530521ms)
✖ an edited successor line keeps its edits when the reopen receipt is consumed (3.130734ms)
✔ relation close honors the link_unblocked kill switch and cancellation without querying the index (6.641627ms)
✖ Esc after a relation picker suppresses held-only notices (4.439659ms)
✖ actual recovered dependent retains its relation reason (3.298088ms)
✖ idless predecessor with a satisfied dependent source uses an available snapshot (2.497872ms)
✖ relation-only successful result returns current daily content (4.995996ms)
✖ warm dependency snapshot holds a source with an open own prerequisite (3.673391ms)
✖ unreconciled Ready resident of a blocked project is held (4.017351ms)
✖ real project recovery stays independent when relation successor is picked or dismissed (3.452824ms)
✖ post-picker revalidation refreshes relation state without opening a second picker (3.602801ms)
✖ post-picker replan refuses stale picks individually and leaves new offers unselected (2.996944ms)
✔ review walk holds the pending picker lock and advances once after relation selection (105.458617ms)
✔ SB vectors pin the successor mint pipeline (7.638596ms)
✔ successor suggester ports the Rust candidate and suffix rules (4.330008ms)
✔ successor link form names unique basenames short and the day file always (1.099609ms)
✔ tasksFromDocuments normalizes vault lines to pool shape (3.261966ms)
✔ normalizeTasksCacheTask ports every known Tasks shape (1.474251ms)
✔ buildDependentsIndex keeps first task IDs and groups dependents (0.6528ms)
✔ findLiveLinks counts plain, embedded, and deferred links under open entries only (7.040524ms)
✔ computeSuccessorAnchors implements closing, slot, inherit, and none (2.378554ms)
✔ SL1 links the successor right after the predecessor bullet (26.060466ms)
✔ SL3 still-blocked rows count the open prerequisites left (2.079093ms)
✔ SL4 future-scheduled dependents stay Blocked with the date row (1.526926ms)
✔ SL5 already-planned dependents recover without a duplicate link (2.504182ms)
✔ SL6 struck and closed-entry links do not count as planned (2.053945ms)
✔ SL7 closing anchors create the continuation placeholder (2.384282ms)
✔ SL8 closing anchors append after carried lines in the continuation (2.045177ms)
✔ SL9 unplanned predecessors offer at the implicit destination (SO14) (2.771303ms)
✔ SL10 missing block IDs mint through the SB rule (1.731616ms)
✔ SL11 project and hidden tasks recover but never link (25.047557ms)
✔ PDC1 leaves a dependency-ready resident Blocked while its project still waits (7.61525ms)
✔ PDC2 residents are offered under the project group (SO1) (5.908808ms)
✔ PDC3 keeps a project resident Blocked when its own prerequisite remains open (4.675483ms)
✔ PDC4/PDC5/PDC6 leave inherited child-project rows for reconcile (4.241802ms)
✔ SL12 one gesture closing two prerequisites links once with both causes (1.636904ms)
✔ SL13 chains do not recurse: the dependent's own dependents wait (1.724023ms)
✔ SL14 ambiguous basenames link long (1.060193ms)
✔ SL15 stale open dependents link and become Next (1.13228ms)
✔ SL16 gates on [id::]: no identity means no lookup and empty rows (0.712496ms)
✔ SO2 11-way fan-out has no cap; all offered, none pre-checked (SL17 retired) (4.00063ms)
✔ SL18 the kill switch recovers without linking or minting (1.241842ms)
✔ SL19 re-applied closes write nothing and report nothing (0.711783ms)
✔ SL23 subtasks anchor at their root's link (1.805468ms)
✔ SL24 later same-name entries take the closing successors (1.744817ms)
✔ SL25 already-Next planned dependents produce no row (1.294979ms)
✔ SL26 inbox successors carry the inbox flag (1.168851ms)
✔ SL27 dropped links are never re-linked and recover to Ready (5.595785ms)
✔ SL28 day-file successors name the note, never the bare link (1.276281ms)
✔ slot insertions land after the anchor subtree with its indent (0.940996ms)
✔ closing insertions replace a lone stub child (1.009989ms)
✔ insertions skip placements with no valid target (0.470112ms)
✔ successorNoticeText implements the §12.6 table (2.591446ms)
✔ parseSuccessorLinkUnblocked reads block and flow styles, defaulting true (1.269717ms)
✔ loadLinkUnblocked stat-caches the config read (2.157066ms)
✔ loadLinkUnblocked treats missing or unreadable config as true (1.81811ms)
✔ successorPlanConfigPath honors XDG_CONFIG_HOME (0.627961ms)
✔ todayDailyPath mirrors the ledger daily path (2.516019ms)
✔ normalizeClosedTaskIdentities keeps the anchor root off the match gate (0.690025ms)
✔ ID-less planned roots anchor ID-bearing children without minting IDs (1.463899ms)
✔ successor anchors never guess across roots (2.945855ms)
✔ a child with its own live link keeps its own slot (1.190549ms)
✔ getSuccessorIsInbox prefers the versioned nav API with safe fallbacks (0.580788ms)
✔ countSuccessorBasenames walks the vault set, not the task set (0.800721ms)
✔ the pass threads a richer isInbox into unblocked rows (1.741373ms)
✔ getTaskLinkLaneApi returns the lane only when version and both functions exist (2.714528ms)
✔ isTaskLinkLaneLine passes content, line, and path and never throws (3.177646ms)
✖ single Alt+] on a Task Link delegates with exactly { editor, view } (2.465216ms)
✖ Alt+[ and Alt+] delegate identically; direction is ignored (0.810041ms)
✖ embedded Pomodoro link routes to the lane toggle, not the full-ring cycle (0.72179ms)
✖ entry, task, Depends-On, and non-Pomodoro lines keep today's behavior (0.649175ms)
✖ counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat (7.138502ms)
✖ counted dispatch without an explicit repeat leaves the key alone (1.002951ms)
✔ counted range starting elsewhere skips Task Link lines (5.700814ms)
✖ legacy fallback with no api keeps today's behavior (1.063891ms)
✖ plain Task Link in an open Pomodoro closes the task root-only and strikes the link (7.275394ms)
✖ marked plain Task Link drops its marker when struck under Pomodoro ancestry (1.155507ms)
✖ plain Pomodoro Task Link closes root-only while embedded closes recursively (1.081282ms)
✖ embedded Pomodoro Task Link still closes recursively and retires to struck form (0.683107ms)
✖ Ctrl+Enter toggles a struck plain Pomodoro link back to open (0.699249ms)
✖ same-file plain Task Link closes and strikes the correct line (0.785694ms)
✖ cursor selects which of several Task Links closes and strikes (0.788796ms)
✖ plain links to Blocked or non-task blocks still complete the Pomodoro (1.968576ms)
✔ strike and unstrike helpers are idempotent, alias-preserving, and marker-aware (3.362356ms)
✔ completeTaskAtCursor closes each open symbol through the Tasks command (5.548087ms)
✔ completeTaskAtCursor insert-above reports lineDelta 1 and never stamps (1.041522ms)
✔ completeTaskAtCursor refuses closed, cancelled, and non-task lines (0.638692ms)
✔ completeTaskAtCursor refuses a missing Tasks command with no write (0.873409ms)
✔ Ctrl+Enter still refuses [?] while completeTaskAtCursor closes it (11.694803ms)
✔ completeTaskAtCursor reports not-closed when Tasks does not write [x] (0.637114ms)
✔ recovery api is frozen at version 3 and recovers without striking references (7.826819ms)
✔ recovery api never throws and reports failures (0.874504ms)
✔ future-scheduled dependents stay Blocked on the planner, api, and close paths (62.233044ms)
✖ Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open (2.896471ms)
✔ every printable non-space ASCII key resolves to a surround pair (6.035315ms)
✔ visible one-code-unit BMP letters, numbers, punctuation, and symbols resolve symmetrically (1.503839ms)
✔ non-visible, combining, multi-character, and multi-code-unit values are rejected (1.816852ms)
✔ ys adds broad symmetric delimiters through pending keydown (3.000859ms)
✔ rejected keydown input never edits or leaks into a pending ys (0.892803ms)
✔ Escape cancels ys, cs, and ds pending state without editing (1.026206ms)
✔ cs accepts broad target and replacement characters independently (3.515285ms)
✔ cs preserves structural alias and padding rules (3.165754ms)
✔ cs replaces repeated symmetric runs exactly once on each side (0.922535ms)
✔ ds removes representative broad symmetric delimiters (2.257002ms)
✔ ds preserves structural alias and padding rules (0.926552ms)
✔ ds removes one pair from repeated runs, including the reported block link (5.659121ms)
✔ consecutive ds commands peel a triple symmetric surround (0.624822ms)
✔ symmetric discovery uses deterministic sequential same-line run pairs (0.394054ms)
✔ symmetric discovery includes every character in repeated boundaries (0.947978ms)
✔ unpaired and unequal symmetric runs are safe no-ops (0.548658ms)
✔ ordinary normal-mode keys remain untouched outside pending state (0.4757ms)
✔ dot while a surround is pending is a literal delimiter, not repeat (0.312989ms)
✔ dot-repeat records and replays broad-character ys (0.623743ms)
✔ dot-repeat records and replays broad-character cs (0.713023ms)
✔ dot-repeat records and replays broad-character ds (0.497959ms)
✔ dot-repeat replays cs against repeated symmetric runs (0.55286ms)
✔ dot-repeat replays ds against repeated symmetric runs (0.473494ms)
✔ consecutive dot-repeats peel a triple symmetric surround (0.540709ms)
ℹ tests 5564
ℹ suites 0
ℹ pass 5439
ℹ fail 124
ℹ cancelled 0
ℹ skipped 1
ℹ todo 0
ℹ duration_ms 31404.85575

✖ failing tests:

test at scripts/test-navigation-relation-cancel-writer.cjs:698:1
✖ cycler recovers ordinary dependents, keeps extra-prereq blocked, and reopens project residents (350.206367ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.getOpenMarkdownEditors (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:17174:25)
      at TaskStatusCyclerPlugin.recoverBlockedDependentsNow (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:17212:30)
      at async TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-navigation-relation-cancel-writer.cjs:714:26)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-blocked-schedule.cjs:51:1
✖ option-bracket refuses to change a member while its project is Blocked (7.458401ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-blocked-schedule.cjs:85:12)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-blocked-schedule.cjs:93:1
✖ tagged inherited ^prj remains Blocked, refuses cycling, and names its parent (12.51883ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-blocked-schedule.cjs:145:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-blocked-schedule.cjs:376:1
✖ cycling Blocked backward to Cancelled retires the date and logs, matching forward (3.889556ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-blocked-schedule.cjs:388:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-blocked-schedule.cjs:399:1
✖ single-press Blocked retirement matches with and without an existing Schedule Log, and with the Tasks command handling the write (0.797209ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-blocked-schedule.cjs:410:12)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-blocked-schedule.cjs:601:1
✖ pressing again after Blocked retirement performs an ordinary transition with no further changes (3.927556ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-blocked-schedule.cjs:615:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-blocked-schedule.cjs:626:1
✖ Alt+] on a date-blocked ^prj recovers open residents in step (1.287445ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-blocked-schedule.cjs:652:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-blocked-schedule.cjs:670:1
✖ Alt+] on a ^prj keeps residents tagged while an open Depends-On target remains (1.003561ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-blocked-schedule.cjs:694:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-blocked-schedule.cjs:728:1
✖ Alt+] on a ^prj recovers residents when the remaining Depends-On target is closed (4.08221ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-blocked-schedule.cjs:752:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-blocked-schedule.cjs:764:1
✖ Alt+] recovers a resident whose own closed cross-note prerequisite was the last reason (1.03625ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-blocked-schedule.cjs:788:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-blocked-schedule.cjs:800:1
✖ Alt+[ on a [?] ^prj to Cancelled recovers tagged residents (1.077282ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-blocked-schedule.cjs:821:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-counted-toggle.cjs:362:1
✖ command checking preserves pending count; execution consumes it once and resets Vim (2.182041ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-counted-toggle.cjs:365:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-counted-toggle.cjs:383:1
✖ command route stays single without normal-mode explicit count and supports in-place ranges (0.623674ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-counted-toggle.cjs:389:12)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:475:1
✖ Pomodoro toggle command is daily-only and places the cursor for both directions (6.49252ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:487:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:560:1
✖ Vim Ctrl+Enter dispatches task transitions and restores a reopened identity (10.93087ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:597:18)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:625:54)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:646:1
✖ Ctrl+Enter on a task line wrapping an embedded transclusion closes the source task and recovers its dependents (4.956161ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:662:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:675:1
✖ Ctrl+Enter reopen restores both the local line and the transcluded source, un-retiring references (0.813443ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:691:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:703:1
✖ Ctrl+Enter reopening the local line over an already-open target does not accidentally close it (0.835737ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:717:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:725:1
✖ Ctrl+Enter closing the local line over an already-closed target does not write it a second time (4.159875ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:744:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:753:1
✖ Ctrl+Enter hands off a claimed walk landing before Pomodoro handling (1.051328ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:778:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:787:1
✖ Ctrl+Enter falls through unchanged when nav declines, is old, missing, or throws (3.98916ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:812:5)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:823:1
✖ Ctrl+Enter consumes a rejected nav claim without an unhandled rejection (1.103123ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:842:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:849:1
✖ Ctrl+Enter on an unresolvable embedded transclusion still closes the local line without error (0.796555ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:858:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:865:1
✖ Ctrl+Enter on a task line with two embeds and the cursor outside both toggles only the local line (1.941215ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:880:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:889:1
✖ Ctrl+Enter on a task line inside a fenced code block does not propagate to its embedded transclusion (0.828526ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:906:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:1070:1
✖ Ctrl+Enter close continues the walk with complete after finalize ran (6.142411ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:1096:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:1106:1
✖ Ctrl+Enter close continues only after transclusion propagation landed (1.187626ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:1136:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:1155:1
✖ Ctrl+Enter reopen settles the walk with null (0.670383ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:1166:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:1175:1
✖ Ctrl+Enter swallows the key with no write while the walk is busy (0.65254ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:1185:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:1193:1
✖ Ctrl+Enter with a null capture behaves exactly like today (0.627886ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:1203:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:1212:1
✖ Ctrl+Enter with nav v2 or no nav keeps today's behavior (0.686242ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:1236:5)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:1244:1
✖ Ctrl+Enter lets the checklist claim win before capturing (0.604923ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:1279:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:1288:1
✖ Ctrl+Enter settles the walk with null when the toggle rejects (0.490329ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:1301:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-ctrl-enter.cjs:1310:1
✖ Ctrl+Enter with a transcluded task line still uses the Tasks-plugin command for the local write (4.063471ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:1343:18)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-ctrl-enter.cjs:1358:54)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-demotion-picker.cjs:463:1
✖ existing-section insertion works before and after the source on CRLF-backed editors (2.716124ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-demotion-picker.cjs:489:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-demotion-picker.cjs:504:1
✖ command opens one picker, writes only on accept, and restores cursor plus center (0.799189ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-demotion-picker.cjs:513:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-demotion-picker.cjs:551:1
✖ pointer activation, Escape, and double-submit protection leave a consistent note (0.707896ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-demotion-picker.cjs:554:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-demotion-picker.cjs:579:1
✖ stale document, changed editor, or missing heading notice without writing (0.704504ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-demotion-picker.cjs:583:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-dependencies.cjs:558:1
✖ single and counted Alt-bracket cycle the dependency target under the cursor (2.736525ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-dependencies.cjs:573:12)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-dependencies.cjs:592:1
✖ single and counted Alt-bracket report when the cursor is off every dependency link (0.817223ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-dependencies.cjs:609:12)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-dependencies.cjs:684:1
✖ recoverBlockedDependents leaves a closed tagged resident untouched (PDT7) (9.285029ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.getOpenMarkdownEditors (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:17174:25)
      at TaskStatusCyclerPlugin.recoverBlockedDependentsNow (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:17212:30)
      at async TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-dependencies.cjs:701:18)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-keep-moving.cjs:442:1
✖ KM24/KM28: real close wiring offers once, applies a pick, and same-day reopen takes it back (18.087317ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-keep-moving.cjs:464:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-keep-moving.cjs:478:1
✖ KM24: a keep-moving pick that becomes Blocked while the picker is open is refused (6.214356ms)
  AssertionError [ERR_ASSERTION]: The input did not match the regular expression /\[\?\] #task Ship the badge renderer \^renderer/. Input:
  
  '---\n' +
    'type: "[[project]]"\n' +
    'status: wip\n' +
    'parent: [[sase]]\n' +
    '---\n' +
    '- [ ] #task Badge project ^prj\n' +
    '- [x] #task Draft the badge spec ^spec\n' +
    '- [ ] #task Ship the badge renderer ^renderer'
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-keep-moving.cjs:503:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '---\ntype: "[[project]]"\nstatus: wip\nparent: [[sase]]\n---\n- [ ] #task Badge project ^prj\n- [x] #task Draft the badge spec ^spec\n- [ ] #task Ship the badge renderer ^renderer',
    expected: /\[\?\] #task Ship the badge renderer \^renderer/,
    operator: 'match',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-keep-moving.cjs:539:1
✖ KM1: Obsidian daily-note link close offers keep-moving and links after the struck predecessor (58.209289ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-keep-moving.cjs:553:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-keep-moving.cjs:565:1
✖ KM26: own-note Ctrl+Enter offers keep-moving with notice v2 card and v1 plain text (7.738198ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-keep-moving.cjs:582:12)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-keep-moving.cjs:601:1
✖ KM26: Alt+] into Done offers keep-moving and links the resident (1.788928ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-keep-moving.cjs:617:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-keep-moving.cjs:626:1
✖ KM27: walk landing awaits the picker and returns the plain text with no card (2.921734ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-keep-moving.cjs:647:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-keep-moving.cjs:653:1
✖ KM25: Esc leaves the resident and the day byte-identical with no notice (6.637844ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-keep-moving.cjs:671:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-parked-successors.cjs:185:1
✖ offerParkedSuccessors offers a starts-after source at the parked slot (12.02173ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-parked-successors.cjs:194:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-parked-successors.cjs:247:1
✖ offerParkedSuccessors Esc on the picker offers without picking (1.425089ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-parked-successors.cjs:258:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-pomodoro-completion.cjs:693:1
✖ Ctrl+Enter groups worked-on links above deferred marked links, keeping a note bullet in place (8.328ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-pomodoro-completion.cjs:710:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-pomodoro-completion.cjs:859:1
✖ Ctrl+Enter deferred-only close keeps the [x] entry in one gesture (0.852673ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-pomodoro-completion.cjs:873:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-pomodoro-reopen.cjs:324:1
✖ registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape (12.379205ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-pomodoro-reopen.cjs:372:5)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-pomodoro-reopen.cjs:382:1
✖ registered Ctrl+Enter immediately recovers a same-file dependent (4.460165ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-pomodoro-reopen.cjs:395:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-pomodoro-reopen.cjs:403:1
✖ registered Ctrl+Enter immediately recovers a cross-file dependent (0.996708ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-pomodoro-reopen.cjs:417:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-pomodoro-reopen.cjs:426:1
✖ child-line Ctrl+Enter produces the same rollover and cursor target as parent completion (4.009895ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at runCompletion (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-pomodoro-reopen.cjs:446:5)
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-pomodoro-reopen.cjs:451:30)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-pomodoro-reopen.cjs:475:1
✖ Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start (0.905463ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-pomodoro-reopen.cjs:499:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-pomodoro-reopen.cjs:514:1
✖ selected embedded Pomodoro children keep recursive close and root-only reopen dispatch (0.941983ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-pomodoro-reopen.cjs:539:5)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-pomodoro-reopen.cjs:589:1
✖ selected unresolved or excluded embedded children are consumed as no-ops (4.004518ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-pomodoro-reopen.cjs:613:5)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-pomodoro-reopen.cjs:628:1
✖ Ctrl+Enter behavior stays generic outside open Pomodoro child ranges (1.06857ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-pomodoro-reopen.cjs:635:40)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-project-pull-in.cjs:1053:1
✖ Ctrl+Enter on the last task link inserts the ^prj and rewrites R (29.506674ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  + actual - expected
  
  + ''
  - '\t- [[ship#^prj]]'
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-project-pull-in.cjs:1076:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '',
    expected: '\t- [[ship#^prj]]',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-project-pull-in.cjs:1088:1
✖ PP29 runtime close and reopen use the parent pull-in receipt (5.076003ms)
  AssertionError [ERR_ASSERTION]: The input did not match the regular expression /^- \[\*\] #task #prj Parent project \^prj$/m. Input:
  
  '---\n' +
    'type: "[[project]]"\n' +
    'status: wip\n' +
    '---\n' +
    '- [ ] #task #prj Parent project #hide ^prj\n' +
    '  - 🧩 **Sub-projects:** [[projects/child|Child]]'
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-project-pull-in.cjs:1122:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '---\ntype: "[[project]]"\nstatus: wip\n---\n- [ ] #task #prj Parent project #hide ^prj\n  - 🧩 **Sub-projects:** [[projects/child|Child]]',
    expected: /^- \[\*\] #task #prj Parent project \^prj$/m,
    operator: 'match',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-project-pull-in.cjs:1143:1
✖ PP18 Alt+[ cancel of the last task surfaces R without linking (1.22015ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-project-pull-in.cjs:1162:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-project-pull-in.cjs:1175:1
✖ PP19 same-day reopen restores R byte-for-byte and takes back the link (7.434148ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  + actual - expected
  
  + ''
  - '\t- [[ship#^prj]]'
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-project-pull-in.cjs:1194:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '',
    expected: '\t- [[ship#^prj]]',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-promotion.cjs:158:1
✖ promotion command writes only on accept and Enter selects Tasks (5.629193ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-promotion.cjs:166:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-promotion.cjs:385:1
✖ Tasks-only preamble promotions prompt and blank Enter moves into Tasks (4.473521ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-promotion.cjs:426:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-promotion.cjs:444:1
✖ plain bullets already in Tasks prompt and blank Enter promotes in place (1.637736ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-promotion.cjs:521:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-promotion.cjs:670:1
✖ always-prompt promotions keep reuse, duplicates, cleanup, CRLF, and cancellation (5.683061ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-promotion.cjs:823:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-reference-lifecycle.cjs:498:1
✖ dependent recovery uses live editor buffers and preserves the cursor (13.707821ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-reference-lifecycle.cjs:514:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-reference-lifecycle.cjs:616:1
✖ non-Vim open/done command finalizes the closed task identity (0.963012ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-reference-lifecycle.cjs:632:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-reference-lifecycle.cjs:637:1
✖ non-Vim open/done command restores the reopened task identity (0.654706ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-reference-lifecycle.cjs:655:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-polish.cjs:136:1
✖ reopen takes back the untouched successor link and restores status (54.056222ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  + actual - expected
  
  + ''
  - '\t- [[sase#^relaunch-failed]]'
  
      at closePlannedPredecessor (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-polish.cjs:122:10)
      at async TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-polish.cjs:138:39)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async startSubtestAfterBootstrap (node:internal/test_runner/harness:385:3) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '',
    expected: '\t- [[sase#^relaunch-failed]]',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-polish.cjs:160:1
✖ an edited successor bullet survives while its status still restores (9.136268ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  + actual - expected
  
  + ''
  - '\t- [[sase#^relaunch-failed]]'
  
      at closePlannedPredecessor (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-polish.cjs:122:10)
      at async TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-polish.cjs:162:39)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '',
    expected: '\t- [[sase#^relaunch-failed]]',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-polish.cjs:193:1
✖ an edited successor status line survives while its link is taken back (3.794586ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  + actual - expected
  
  + ''
  - '\t- [[sase#^relaunch-failed]]'
  
      at closePlannedPredecessor (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-polish.cjs:122:10)
      at async TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-polish.cjs:195:39)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '',
    expected: '\t- [[sase#^relaunch-failed]]',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-polish.cjs:221:1
✖ reopen on a different day leaves successor links alone (4.052961ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  + actual - expected
  
  + ''
  - '\t- [[sase#^relaunch-failed]]'
  
      at closePlannedPredecessor (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-polish.cjs:122:10)
      at async TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-polish.cjs:223:39)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '',
    expected: '\t- [[sase#^relaunch-failed]]',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-polish.cjs:273:1
✖ Alt+] on a planned prerequisite links its successor (1.16615ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-polish.cjs:289:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-polish.cjs:305:1
✖ take-back deletes a pre-existing entry it empties (3.657063ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  + actual - expected
  
  + ''
  - '\t- [[sase#^relaunch-failed]]'
  
      at closePlannedPredecessor (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-polish.cjs:122:10)
      at async TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-polish.cjs:307:39)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '',
    expected: '\t- [[sase#^relaunch-failed]]',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-polish.cjs:449:1
✖ Alt+[ into Cancelled recovers its dependents without linking (0.877178ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-polish.cjs:467:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-polish.cjs:484:1
✖ take-back keeps an entry whose prose survives across a blank line (both paths) (1.984947ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-polish.cjs:527:12)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:243:1
✖ link close links the unblocked successor into the slot and shows the nav card (47.621597ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  + actual - expected
  
  + ''
  - '\t- [[sase#^relaunch-failed]]'
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:264:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async startSubtestAfterBootstrap (node:internal/test_runner/harness:385:3) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '',
    expected: '\t- [[sase#^relaunch-failed]]',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:288:1
✖ Ctrl+Enter close preserves bracket and parenthesis theme fields (1.784592ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at pressCtrlEnterAndSettle (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:189:3)
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:297:11)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:304:1
✖ Ctrl+Enter carries per-task theme intents through both pick normalizers and saves them with successor links (1.656195ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at pressCtrlEnterAndSettle (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:189:3)
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:390:9)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:409:1
✖ successor retarget Enter merges the destination header and preserves the task field (1.465887ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at pressCtrlEnterAndSettle (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:189:3)
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:456:9)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:467:1
✖ default placement and a changed suggestion still link selected successors without retargeting themes (1.07015ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at pressCtrlEnterAndSettle (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:189:3)
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:529:9)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:546:1
✖ project-finished successor writes its selected theme with real task-theme transforms (5.21717ms)
  AssertionError [ERR_ASSERTION]: The input did not match the regular expression /^- \[\*\] #task #prj Parent project \[type:: BUILD\] \^prj$/m. Input:
  
  '---\n' +
    'type: "[[project]]"\n' +
    'status: wip\n' +
    'theme: WRITE\n' +
    '---\n' +
    '- [ ] #task #prj Parent project #hide ^prj\n' +
    '  - 🧩 **Sub-projects:** [[projects/child|Child]]'
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:608:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '---\ntype: "[[project]]"\nstatus: wip\ntheme: WRITE\n---\n- [ ] #task #prj Parent project #hide ^prj\n  - 🧩 **Sub-projects:** [[projects/child|Child]]',
    expected: /^- \[\*\] #task #prj Parent project \[type:: BUILD\] \^prj$/m,
    operator: 'match',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:617:1
✖ successor theme save remains truthful when the later daily-link write fails (1.189833ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at pressCtrlEnterAndSettle (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:189:3)
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:671:9)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:715:1
✖ Warm finalize reads no unrelated note bodies on the real close path (15.130834ms)
  AssertionError [ERR_ASSERTION]: The expression evaluated to a falsy value:
  
    assert.ok(model)
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:766:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: null,
    expected: true,
    operator: '==',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:796:1
✖ cold fallback still recovers and links without a Tasks cache (5.438176ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  + actual - expected
  
    '- [x] #task Fix apollo machine! [id:: sase__fix-apollo]  [completion:: 2026-11-05] ^fix-apollo\n' +
  +   '- [?] #task Re-launch all failed agents on apollo! [dependsOn:: sase__fix-apollo] ^relaunch-failed'
  -   '- [*] #task Re-launch all failed agents on apollo! [dependsOn:: sase__fix-apollo] ^relaunch-failed'
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:813:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '- [x] #task Fix apollo machine! [id:: sase__fix-apollo]  [completion:: 2026-11-05] ^fix-apollo\n- [?] #task Re-launch all failed agents on apollo! [dependsOn:: sase__fix-apollo] ^relaunch-failed',
    expected: '- [x] #task Fix apollo machine! [id:: sase__fix-apollo]  [completion:: 2026-11-05] ^fix-apollo\n- [*] #task Re-launch all failed agents on apollo! [dependsOn:: sase__fix-apollo] ^relaunch-failed',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:821:1
✖ recovered-only close reports unblocked without linking (SO4 Esc) (3.947912ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:849:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:867:1
✖ walk landing composes a single toast and shows no card (41.804433ms)
  AssertionError [ERR_ASSERTION]: The input did not match the regular expression /🔓/. Input:
  
  ''
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:915:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '',
    expected: /🔓/,
    operator: 'match',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:920:1
✖ nav absent falls back to a plain Notice with no link (SO missing picker) (4.075337ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  + actual - expected
  
  + '- [?] #task Re-launch all failed agents on apollo! [dependsOn:: sase__fix-apollo] ^relaunch-failed'
  - '- [ ] #task Re-launch all failed agents on apollo! [unblocked:: 2026-11-05] [dependsOn:: sase__fix-apollo] ^relaunch-failed'
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:938:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '- [?] #task Re-launch all failed agents on apollo! [dependsOn:: sase__fix-apollo] ^relaunch-failed',
    expected: '- [ ] #task Re-launch all failed agents on apollo! [unblocked:: 2026-11-05] [dependsOn:: sase__fix-apollo] ^relaunch-failed',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:946:1
✖ stale cache heals via re-plan from fresh text (SO30) (6.154122ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:990:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1006:1
✖ Pomodoro-line close appends the successor to the created continuation (16.326499ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  + actual - expected
  
    '- [x] #task Fix apollo machine! [id:: sase__fix-apollo]  [completion:: 2026-11-05] ^fix-apollo\n' +
  +   '- [?] #task Re-launch all failed agents on apollo! [dependsOn:: sase__fix-apollo] ^relaunch-failed'
  -   '- [*] #task Re-launch all failed agents on apollo! [dependsOn:: sase__fix-apollo] ^relaunch-failed'
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1031:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '- [x] #task Fix apollo machine! [id:: sase__fix-apollo]  [completion:: 2026-11-05] ^fix-apollo\n- [?] #task Re-launch all failed agents on apollo! [dependsOn:: sase__fix-apollo] ^relaunch-failed',
    expected: '- [x] #task Fix apollo machine! [id:: sase__fix-apollo]  [completion:: 2026-11-05] ^fix-apollo\n- [*] #task Re-launch all failed agents on apollo! [dependsOn:: sase__fix-apollo] ^relaunch-failed',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1049:1
✖ Pomodoro-line close keeps the closing anchor after the picker re-plan (11.278583ms)
  AssertionError [ERR_ASSERTION]: The input did not match the regular expression /^- \[x\] \(\*\*09:00-09:25\*\* \[t:: 25m\]\) — FIX\n\t- .*\n- \[ \] \(\) — FIX\n\t- \[\[sase#\^relaunch-failed\]\]\n- \[ \] \(10:00-10:25\) — OTHER\n\t- $/m. Input:
  
  '# 2026-11-05\n' +
    '\n' +
    '## Pomodoros\n' +
    '- [x] (**09:00-09:25** [t:: 25m]) — FIX\n' +
    '\t- ~~[[sase#^fix-apollo]]~~\n' +
    '- [ ] (10:00-10:25) — OTHER\n' +
    '\t- '
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1082:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '# 2026-11-05\n\n## Pomodoros\n- [x] (**09:00-09:25** [t:: 25m]) — FIX\n\t- ~~[[sase#^fix-apollo]]~~\n- [ ] (10:00-10:25) — OTHER\n\t- ',
    expected: /^- \[x\] \(\*\*09:00-09:25\*\* \[t:: 25m\]\) — FIX\n\t- .*\n- \[ \] \(\) — FIX\n\t- \[\[sase#\^relaunch-failed\]\]\n- \[ \] \(10:00-10:25\) — OTHER\n\t- $/m,
    operator: 'match',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1092:1
✖ completeTaskAtCursor returns the notice and shows nothing itself (4.32774ms)
  AssertionError [ERR_ASSERTION]: The input did not match the regular expression /🔓/. Input:
  
  ''
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1114:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '',
    expected: /🔓/,
    operator: 'match',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1119:1
✖ successor apply recovers project residents without ledger v12 (2.91094ms)
  AssertionError [ERR_ASSERTION]: The input did not match the regular expression /^- \[ \] #task #prj Release .* \^prj$/m. Input:
  
  '---\n' +
    'type: "[[project]]"\n' +
    'status: wip\n' +
    '---\n' +
    '- [?] #task #prj Release [id:: project__prj] [dependsOn:: sase__fix-apollo] ^prj\n' +
    '- [?] #task Prepare the release #prj_is_blocked ^release-notes\n' +
    '- [x] #task Already done #prj_is_blocked ✅ 2026-10-01 ^done'
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1168:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '---\ntype: "[[project]]"\nstatus: wip\n---\n- [?] #task #prj Release [id:: project__prj] [dependsOn:: sase__fix-apollo] ^prj\n- [?] #task Prepare the release #prj_is_blocked ^release-notes\n- [x] #task Already done #prj_is_blocked ✅ 2026-10-01 ^done',
    expected: /^- \[ \] #task #prj Release .* \^prj$/m,
    operator: 'match',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1261:1
✖ managed Done offers an idless relation source through picker and records a reopen receipt (10.113246ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  + actual - expected
  
  + 'unavailable'
  - 'checked'
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1272:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: 'unavailable',
    expected: 'checked',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1291:1
✖ managed Done composes ordinary and relation successors in one v3 picker (4.182615ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1307:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1397:1
✖ an edited successor line keeps its edits when the reopen receipt is consumed (3.130734ms)
  AssertionError [ERR_ASSERTION]: The expression evaluated to a falsy value:
  
    assert.ok(consumed)
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1420:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: null,
    expected: true,
    operator: '==',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1464:1
✖ Esc after a relation picker suppresses held-only notices (4.439659ms)
  AssertionError [ERR_ASSERTION]: Esc is silent after the picker showed the held fold
  + actual - expected
  
  + [
  +   "🪢 Couldn't check starts after links · nothing offered"
  + ]
  - []
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1480:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: false,
    code: 'ERR_ASSERTION',
    actual: [ "🪢 Couldn't check starts after links · nothing offered", 'Closed tasks, but blocked dependents could not be checked.' ],
    expected: [],
    operator: 'deepStrictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1483:1
✖ actual recovered dependent retains its relation reason (3.298088ms)
  AssertionError [ERR_ASSERTION]: dependency recovery should still link when picked
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1495:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: false,
    code: 'ERR_ASSERTION',
    actual: undefined,
    expected: true,
    operator: '==',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1499:1
✖ idless predecessor with a satisfied dependent source uses an available snapshot (2.497872ms)
  AssertionError [ERR_ASSERTION]: null
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1525:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: false,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1528:1
✖ relation-only successful result returns current daily content (4.995996ms)
  AssertionError [ERR_ASSERTION]: The input did not match the regular expression /\[\[source#\^followup\]\]/. Input:
  
  ''
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1534:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: '',
    expected: /\[\[source#\^followup\]\]/,
    operator: 'match',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1537:1
✖ warm dependency snapshot holds a source with an open own prerequisite (3.673391ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  + actual - expected
  
  + undefined
  - 'blocked'
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1552:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: undefined,
    expected: 'blocked',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1555:1
✖ unreconciled Ready resident of a blocked project is held (4.017351ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  + actual - expected
  
  + undefined
  - 'blocked'
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1571:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: undefined,
    expected: 'blocked',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1574:1
✖ real project recovery stays independent when relation successor is picked or dismissed (3.452824ms)
  AssertionError [ERR_ASSERTION]: {"version":1,"predecessors":[{"note_path":"done.md","block_id":"finish","text":""}],"unblocked":[],"keep_moving":[],"still_blocked":[],"relation_successors":[],"relation_held":[],"relation_check":"unavailable","relation_labels":["starts after"],"relation_picker_opened":false,"daily_path":"2026/20261105.md","daily_content":null,"failure":null}
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1594:12)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: false,
    code: 'ERR_ASSERTION',
    actual: undefined,
    expected: true,
    operator: '==',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1604:1
✖ post-picker revalidation refreshes relation state without opening a second picker (3.602801ms)
  AssertionError [ERR_ASSERTION]: own-prerequisite: one picker only
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1720:12)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: false,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-successor-wiring.cjs:1735:1
✖ post-picker replan refuses stale picks individually and leaves new offers unselected (2.996944ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  0 !== 1
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-successor-wiring.cjs:1781:10)
      at async Test.run (node:internal/test_runner/test:1208:7)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: 0,
    expected: 1,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-link-lane.cjs:166:1
✖ single Alt+] on a Task Link delegates with exactly { editor, view } (2.465216ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-link-lane.cjs:170:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-link-lane.cjs:183:1
✖ Alt+[ and Alt+] delegate identically; direction is ignored (0.810041ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-link-lane.cjs:188:12)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-link-lane.cjs:196:1
✖ embedded Pomodoro link routes to the lane toggle, not the full-ring cycle (0.72179ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-link-lane.cjs:205:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-link-lane.cjs:213:1
✖ entry, task, Depends-On, and non-Pomodoro lines keep today's behavior (0.649175ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-link-lane.cjs:219:12)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-link-lane.cjs:293:1
✖ counted Alt+] on a Task Link delegates with countExplicit and the Vim repeat (7.138502ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.getFocusedMarkdownEditorView (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:22667:21)
      at TaskStatusCyclerPlugin.dispatchCountedTaskCycleEvent (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:22291:23)
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-link-lane.cjs:297:23)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-link-lane.cjs:313:1
✖ counted dispatch without an explicit repeat leaves the key alone (1.002951ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.getFocusedMarkdownEditorView (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:22667:21)
      at TaskStatusCyclerPlugin.dispatchCountedTaskCycleEvent (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:22291:23)
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-link-lane.cjs:322:23)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-link-lane.cjs:355:1
✖ legacy fallback with no api keeps today's behavior (1.063891ms)
  AssertionError [ERR_ASSERTION]: Expected values to be strictly equal:
  
  false !== true
  
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-link-lane.cjs:361:10)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    actual: false,
    expected: true,
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-links-api.cjs:17:1
✖ plain Task Link in an open Pomodoro closes the task root-only and strikes the link (7.275394ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-links-api.cjs:35:5)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.start (node:internal/test_runner/test:1096:17)
      at startSubtestAfterBootstrap (node:internal/test_runner/harness:385:17) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-links-api.cjs:46:1
✖ marked plain Task Link drops its marker when struck under Pomodoro ancestry (1.155507ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-links-api.cjs:63:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async startSubtestAfterBootstrap (node:internal/test_runner/harness:385:3) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-links-api.cjs:72:1
✖ plain Pomodoro Task Link closes root-only while embedded closes recursively (1.081282ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-links-api.cjs:90:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-links-api.cjs:100:1
✖ embedded Pomodoro Task Link still closes recursively and retires to struck form (0.683107ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-links-api.cjs:118:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-links-api.cjs:128:1
✖ Ctrl+Enter toggles a struck plain Pomodoro link back to open (0.699249ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-links-api.cjs:140:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-links-api.cjs:149:1
✖ same-file plain Task Link closes and strikes the correct line (0.785694ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-links-api.cjs:164:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-links-api.cjs:173:1
✖ cursor selects which of several Task Links closes and strikes (0.788796ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-links-api.cjs:196:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-links-api.cjs:206:1
✖ plain links to Blocked or non-task blocks still complete the Pomodoro (1.968576ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-links-api.cjs:229:5)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }

test at scripts/test-task-status-cycler-task-links-api.cjs:543:1
✖ Ctrl+Enter on a Task Link to a Cancelled task leaves the Pomodoro open (2.896471ms)
  AssertionError [ERR_ASSERTION]: Expected "actual" to be reference-equal to "expected":
  + actual - expected
  
  + [class MarkdownView]
  - [class MarkdownView]
  
      at Object.getActiveViewOfType (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/task-status-cycler-harness.cjs:384:14)
      at TaskStatusCyclerPlugin.handleVimTaskToggleOpenDone (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21122:37)
      at /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/plugins/task-status-cycler/main.js:21008:12
      at TestContext.<anonymous> (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/sase/repos/linked/bob-plugins/scripts/test-task-status-cycler-task-links-api.cjs:561:3)
      at Test.runInAsyncScope (node:async_hooks:227:14)
      at Test.run (node:internal/test_runner/test:1201:25)
      at Test.processPendingSubtests (node:internal/test_runner/test:831:18)
      at Test.postRun (node:internal/test_runner/test:1330:19)
      at Test.run (node:internal/test_runner/test:1258:12)
      at async Test.processPendingSubtests (node:internal/test_runner/test:831:7) {
    generatedMessage: true,
    code: 'ERR_ASSERTION',
    operator: 'strictEqual',
    diff: 'simple'
  }
failed  exit=1  duration=75300ms

