# Chat History - ace-run (bob-cli-2o.land--code)

- **TIMESTAMP:** 2026-09-29 23:29:25 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-2o.land--code

## Linked Chats

- 1. --plan — `~/.sase/chats/202609/gh_bobs_org__bob_cli-ace_run-bob_cli_2o_land__plan-260929_181026.md`
- **2. --code** — `~/.sase/chats/202609/gh_bobs_org__bob_cli-ace_run-bob_cli_2o_land__code-260929_181026.md`

## Prompt

%model:@medium
#gh:gh_bobs-org__bob-cli
@plan:202609/plan_budget_land_closeout.md

The above plan has been reviewed and approved. Implement it now.


## Response

Implemented the approved `202609/plan_budget_land_closeout.md` tale. Final declaration accepted (4 repos commit; `bead_action: close` on bob-cli for epic `bob-cli-2o`).

**Part A — bob-cli** (all in workspace):
- Config isolation: `plan:` is now untyped `Value` in `RawConfig`; typing lives in new `src/native/config/plan.rs` (`config.rs` → `config/mod.rs`, now 1358 lines). Other loaders ignore mistyped plan blocks; `bob plan` still exits 2. Tests for all three loaders + plan rejection.
- `bob plan` header from ledger `has_section` (placeholder-only keeps daily-file header). New CLI test.
- Status follows rule 8 (NOW never flips status); engine tests for `now_cap_exceeded`+`ok` and `plan_link_cap_exceeded`.
- Empty link target = daily note (`compute_for_daily` + canonicalization); callers pass daily key (`bob plan`, hooks, tmux, capture, complete). Conformance example 8 in `docs/plan.md` + unit test.
- Capture attaches `plan_budget` only when the Pomodoros section text differs; config loads after the check. Two CLI tests.
- Create-row preview splits `+` components, skips exempt/existing, uses `.contains()` (removes this epic's clippy warning). Unit + both-row tests.
- `#now` completion only where execution accepts it (rejects `=x #n`, `@r:id #n`, bare `#n`). Test added.
- Human layout: time column fits `exempt`; exempt rows stay dimmed past inner reset; docs example fixed to `0 links`.
- Docs/help: Surfaces final (no Phase col, real tmux/capture/hook strings); `pomodoro_close_drop` span; `=x0~2` hint + docs; `~` capture example; `now_tag` in capture-parse Needs; `BOB_CONFIG_FILE` in tmux help; hooks docs (plan line order + `plan_budget` JSON).
- Missing CLI tests: strict project-note/toggle refusals, `^r:id=x~K` / `Text @r:id=x~K` closes, `#now` e2e task line.
- Split `parse_pomodoro.rs` (992 lines) + new `parse_pomodoro_close.rs` (639), registered.

**Part B — bob-plugins** (`sase/repos/linked/bob-plugins`):
- `renderPlanBlock` uses `MarkdownRenderChild` + guarded fallback; Tasks `cache-update` event, interval only when plugin absent, `changed` filtered to rendered targets; invalid config → full defaults; entry regex exact (`- [c]`, no tab/empty/multi), CRLF normalized, example-8 daily path; NOW predicate (`#hide/x`, `#Hide`, case-insensitive paths, NON_TASK done); `removeNowTagFromLine` preserves `[why:: a  b]`; clamp subtitle on singletons; `via Task Links` in visible countPill; pinned `#now` detail once; NUL → `\u0000`; block-id-prompt manifest mentions plan-budget suffix.
- Versions bumped (ledger 1.6.0, hotkeys 1.40.0, block-id 1.14.0); `npm test` 808/808; `npm run validate` 6/6; synced all three to `~/bob` via `bob plugins sync -n`.

**Part C:** `~/bob/dash.md` NOW chip uses `nowBudget().cap/.over` with 15 fallback; `bob vault-sync` pushed, status clean. Mac README destination-row sentence corrected to ``→ NAME``.

**Gates:** `cargo fmt --check` clean; `cargo test` green (1277 lib, 603 CLI); clippy shows only the pre-existing `bob-cli-28` deny at `pomodoro_name.rs:808` plus its pre-existing warning; `cargo install --locked --force` done; spot-checks (`bob plan`, `-f json`, `tmux-pomodoro` on 20260929) pass. README needed no changes (capture ledger wording already matched). No `symvision` recipe (as expected). `epic-symbols` lists none. Mac fixtures: analyzed — no fixture covers the changed edges (GTD/merged preview, NOW-only over, empty-target, non-ledger gating), so nothing regenerated and macOS CI was not run; follow-up triage untouched per plan.

**Rollout checklist (Bryan's steps):** add `#now` to ≤15 tasks (before fields, Alt+N, or picker `#now` row); from 2026-09-30 carry ≤3 open entries by hand; daily note = GTD + ≤3 themes, highlight first; on MacBook + athena reinstall `bob`, rebuild/install Bob Mac Capture, run `bob plugins sync`; consider `plan.strict: true` if red most days after a week.

Also: the two new `gtd_daily.md` chores ("Pick today…", "Weekly review…") were flipped to `[?]` by a MacBook sync after creation — confirm that was intended. `bob-cli-2q` tracks the evening day-flip (UTC host).
