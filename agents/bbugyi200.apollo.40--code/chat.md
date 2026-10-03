# Chat History - ace-run (40--code)

- **TIMESTAMP:** 2026-10-01 15:57:20 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** 40--code

## Linked Chats

- 1. --plan — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-40__plan-261001_152428.md`
- **2. --code** — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-40__code-261001_152428.md`

## Prompt

%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202610/dashboard_badge_parity.md

The above plan has been reviewed and approved. Implement it now.


## Response

Implemented the approved `202610/dashboard_badge_parity` plan.

**What changed**

- `bob-plugins` (`plugins/bob-ledger-tools/main.js`, bumped to 1.14.0): new additive `dashboardLaneBudget("pending"|"next")` API returning `{section, lane, cap, over, today}` — the section count excludes TODAY (and `dash.md`), while `pendingBudget()`/`nextBudget()` keep whole-lane semantics for all non-dashboard callers. New `renderDashboardLaneBadge` with lifecycle-owned refresh (Tasks-cache, TODAY, rollover, caps) reusing the existing debounce/disposal pattern. Fixed `readyTaskVisible` to match Tasks semantics: `#hide` is a case-insensitive substring match (`#hide/x`, `#Hide` now excluded) and `_templates`/`_conflicts`/`dash.md` checks are case-insensitive, all shared through one `dashboardSectionBaseVisible` predicate.
- `dash.md` (live vault): badges show the section count (e.g. PENDING 49) with `49 in this section; whole lane 50/10; 1 in TODAY` in tooltip/aria; NEXT section now uses `status.symbol is *`; fallback visibility matches the same base rules; unavailable stays `–`, never zero.
- New regression suite `scripts/test-ledger-tools-dashboard-parity.cjs` (wired into `npm test`) comparing badge models against an independent query simulation by identities and counts; corrected the two READY fixtures that pinned the old hide behavior.
- `docs/plan.md` and plugin README document the section-vs-lane split, visibility rules, and fallback behavior. No Rust changes.

**Verification (observed)**

- `npm test`: 1099 pass, 0 fail. `npm run validate`: 6/6 plugins valid.
- Deployed via `bob plugins sync` — vault has 1.14.0. Vault `dash.md` change auto-synced (`2357e5eb`, working tree clean, local/remote SHAs match).

**Limitation**: the live Obsidian UI comparison (settled badge vs. actual Tasks results on the Mac runtime) could not be performed from this Linux workspace, so per the plan I report that rather than claiming UI parity — headless suites are green but are not proof of rendered parity.
