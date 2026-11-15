# Chat History - ace-run (1cq--code)

- **TIMESTAMP:** 2026-11-15 14:09:39 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** 1cq--code

## Prompt

%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202611/drawer_title_punctuation.md

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false
Reviewer decisions for this plan (final · reviewer via ACE):
- punctuation = sentence (planner default: sentence). Implement the "punctuation = sentence" branch; ignore "punctuation = question_bang", "punctuation = broad". Context: "Which new punctuation should a drawer title accept?".
- slug_reach = exact (planner default: exact). Implement the "slug_reach = exact" branch; ignore "slug_reach = punctuation_blind". Context: "Should typing the slug #what-is-sase also select the punctuated drawer WHAT IS SASE?".
Implement only the branches selected above.
%macros_enabled:true


## Response

Implemented the approved `punctuation = sentence` + `slug_reach = exact` branches.

Drawer titles now accept `?`, `!`, `;` after the lead and `:` only as the final character. `WHAT IS SASE?`, `WOW!`, `OPTIONS:`, and `WHAT NEXT:` qualify; `?WHY`, `NOTE: X`, `KEY:: VALUE`, `OPTIONS::`, `C++`, and `PHONE: (609) 597-4111` do not. Pomodoro names still allow `+` and never take the new punctuation. Slug selectors stay exact, so `#what-is-sase` refuses with a quoted suggestion.

Changed in bob-cli:
- [capture_drawers.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/src/native/capture_drawers.rs): split `is_title` into `TitleGrammar::Drawer` / `PomodoroName`, added `is_drawer_rest` / `is_pomodoro_rest`, bumped `DRAWER_CATALOG_VERSION` to 2, fixed the near-duplicate suggestion to quote invalid slugs.
- [capture_project_note.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/src/native/capture_project_note.rs): `is_project_section_title` now delegates to `is_drawer_title`.
- Tests: new `sentence_punctuation_drawer_titles_qualify`, `near_duplicate_suggests_quoted_title_when_slug_is_invalid`, updated `section_title_shape_allows_sentence_punctuation`, new `punctuated_drawer_reports_a_drawer_bullet_span`, new `punctuated_drawer_lists_under_task_with_exact_slug_reach`, new `punctuated_drawer_merges_into_the_existing_drawer`, new `punctuated_drawer_shaped_lines_render_bold`, new `SP31` in [vectors.json](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/tests/fixtures/task_split/vectors.json) plus [README](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/tests/fixtures/task_split/README.md) and [task-split.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/docs/task-split.md) rows.

Changed in bob-plugins:
- [256-task-split-plan.js](< /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/256-task-split-plan.js>): same sentence rule with trailing-`:` position check.
- [100-yank-and-paths.js](< /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/100-yank-and-paths.js>): `formatProjectReversalSectionTitle` now calls `isTaskSplitDrawerTitle`.
- [010-requires-and-config.js](< /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/010-requires-and-config.js>): removed `PROJECT_SECTION_TITLE_RE`.
- Copied [vectors.json](< /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/scripts/fixtures/task_split/vectors.json>) byte-for-byte, added `WHAT IS SASE?` promotion/reversal tests.

Changed docs:
- [capture.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/docs/capture.md): stated the drawer grammar once with `WHAT IS SASE?`, fixed project-note, Pomodoro selector, and `capture-pomodoro-name` charsets, documented the quoted `#"WHAT IS SASE?"` reach.

Verification observed:
- `cargo fmt --check` passes after formatting.
- `just lint` passes.
- `just test` passes (full workspace).
- Plugin `npm run build` passes, `build:check` passes, `docs:inventory:check` passes.
- Targeted plugin suites pass: vectors 2/2, project-from-task 45/45, project-reversal 26/26.
- Full plugin `test:unit` showed 3 perf-budget flakes in `test-ledger-tools-frees-marks.cjs`; that file alone passes 17/17 on rerun.
- `just docs-check` still fails on `docs/reference/configuration.md` word budget (6009/6000); that file is untouched, so the failure is pre-existing.
- E2E with the debug build against a throwaway vault passed: `capture-complete` lists `WHAT IS SASE?` unrefused, dry-run previews one entry with `created: false`, `capture-parse` reports a `drawer_bullet` span titled `WHAT IS SASE?`.
- Did not bump `GRAMMAR_REVISION`; made no `bob-mac-capture` change.

Vault audit (read-only, left for Bryan):
- `sase_better_llm_disable.md:24` `OPTIONS:` and `needs_attn_tasks.md:28` `NOTES:` newly qualify under `sentence`.
- `done/body_done.md:31` `PHONE: (609) 597-4111` stays excluded under `sentence` (would qualify only under `broad`).
- Left Bryan’s own `WHAT IS SASE` rename to him.
