# Chat History - ace-run (0uq--code)

- **TIMESTAMP:** 2026-10-01 02:50:57 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** 0uq--code

## Linked Chats

- 1. --plan — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-0uq__plan-261001_021230.md`
- **2. --code** — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-0uq__code-261001_021230.md`

## Prompt

%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202610/ready_badge.md

The above plan has been reviewed and approved. Implement it now.


## Response

Implemented the approved READY badge plan end to end: daily notes and `dash.md` now share one live `READY n/cap` backlog badge (blue normally, red only on strict excess, `READY –` when unavailable) that opens `dash#READY Tasks`.

What changed:

- `bob-cli`: `plan.max_ready` (default 100, integers 1–`u32::MAX`, null/missing default) in [plan.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/src/native/config/plan.rs), additive `caps.max_ready` in the plan report (schema stays 2) in [mod.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/src/native/plan_budget/mod.rs), plus `docs/plan.md` backlog definition and updated CLI test expectations.
- `bob-plugins` (ledger-tools 1.8.0 → 1.9.0): shared predicate (`TODO` type incl. custom symbols; `dash.md` self-exclusion; exact `#hide`; explicit `_conflicts`; full-list `isBlocked`; scheduled ≤ today; `isToday` excluded), `api.readyBudget()` (`{count, cap, over}`, `count: null` when Tasks missing, cache not `Warm`, Today not built, or evaluation throws) and `api.renderReadyBadge(parent, {sourcePath, component})`, one element renderer/CSS for both surfaces, daily row `READY` after NEXT with async-paint guards, debounced refresh on Tasks updates/Today rebuilds/rollover plus 60s cap/day check.
- Vault `dash.md`: READY renders between NEXT and BLOCKED via the new API (`dv.current().file.path`, `dv.component`); fallback keeps the old inline count with `caps().maxReady` or 100 and existing chip style. READY Tasks section untouched.
- `chezmoi` config gains `max_ready: 100`; legacy `max_now` preserved untouched.

Verified (all observed this turn): new `test-ledger-tools-ready-badge.cjs` 20/20; `npm test` 1025/1025 and `npm run validate` 6/6; `cargo test` all suites green; `cargo fmt --check` clean; `clippy` shows only pre-existing warnings; stubbed dash execution gives API path rendered / fallback single chip, no duplicate slot; live `bob plan -f json` reports `"max_ready": 100`, `schema_version: 2`. Deployed: `bob plugins sync --plugin bob-ledger-tools` (3 copied), installed binary rebuilt via `cargo install`, vault reconciled via `bob vault-sync run` (open checkout committed/pushed; `~/bob` fast-forwarded, status clean).

Two follow-ups, both expected: run `chezmoi update -a --force` after the host lands the chezmoi commit (review `chezmoi diff` first; it is empty right now because the change is still uncommitted). No Obsidian UI is reachable from here, so live rendering was not visually tested — short checklist for you: open a daily note and `dash.md` side by side in Reading and Live Preview, light and dark, plus a narrow pane; confirm label/value balance and wrapping, red `READY 101/100` vs `READY 100/100`, muted `READY –` with the limit in its tooltip, visible focus, hover preview to `dash#READY Tasks`, and Ctrl/Cmd-click opening a new leaf.
