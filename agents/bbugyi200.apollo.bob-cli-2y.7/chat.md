# Chat History - ace-run (bob-cli-2y.7)

- **TIMESTAMP:** 2026-09-30 17:49:01 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-2y.7

## Prompt

#gh:gh_bobs-org__bob-cli
%id(7, clan=bob-cli-2y, bead=bob-cli-2y.7)
%model:@medium
%auto
%w:bob-cli-2y.5
%w(bead=bob-cli-2y.5)
Can you complete the work for bead bob-cli-2y.7? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-2y.7 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-2y.7 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-2y.7`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-2y.7 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Bead bob-cli-2y.7 (ledger-today-api) is done and closed.

What shipped, in `bob-plugins` (`plugins/bob-ledger-tools/`, v1.6.0 → 1.7.0):

- **api v2** (frozen): `caps`, `planBudget`, `todayKeys`, `isToday`, `todayRank`, `nextBudget`, `pendingBudget`. `nowBudget`, `hasNowTag`, `PLAN_NOW_TAG_RE`, and `PLAN_LINT_NOW_CAP` are deleted.
- **Synchronous Today cache** (`{date, dailyPath, keys, rank}`): built on layout-ready, `metadataCache` `resolved`, `changed` for the daily path (using the event's content), daily-note create/delete/rename, and a 1-minute midnight-rollover check. `isToday` is `false` before the first build and on missing fields; `todayRank` falls back to `Number.MAX_SAFE_INTEGER`. On key change it fires the pinned `obsidian-tasks-plugin:reload-open-search-results` event (verified against the installed Tasks bundle's `TasksEvents` subscription) and re-renders bob-plan blocks debounced.
- **Faithful mirrors** of `list_queued_links` (`computeTodayLinks`) and lane visibility (`laneBudgetFromTasks`: Next = symbol `*`, Pending = type `IN_PROGRESS`; whole lane, Today included). Config uses `max_next`/`max_pending`; a legacy `max_now` loads without error.
- **bob-plan block**: `PLAN`, `TODAY`, `PENDING → dash#PENDING Tasks`, `NEXT → dash#NEXT Tasks` chips (red when over), `next_cap_exceeded` / `pending_cap_exceeded` lints, new today/pending/next CSS accents; README documents api v2.

Verified: new `scripts/test-ledger-tools-today.cjs` covers the `docs/plan.md` T1–T9 vectors verbatim plus lanes, caps, api shape, cache rebuild paths, change-only refresh, and the event-name pin. Full gate green: `npm test` 870 pass, `npm run validate` 6/6. Deployed to the vault via `bob plugins sync` (1.7.0 confirmed in the vault manifest). `sase bead epic-symbols` shows no leftovers. No follow-ups discovered.
