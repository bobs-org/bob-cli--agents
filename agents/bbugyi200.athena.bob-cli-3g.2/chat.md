# Chat History - ace-run (bob-cli-3g.2)

- **TIMESTAMP:** 2026-10-01 19:31:40 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-3g.2

## Prompt

#gh:gh_bobs-org__bob-cli
%id(2, clan=bob-cli-3g, bead=bob-cli-3g.2)
%model:@medium
%auto
%w:bob-cli-3g.1
%w(bead=bob-cli-3g.1)
Can you complete the work for bead bob-cli-3g.2? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-3g.2 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-3g.2 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-3g.2`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-3g.2 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Bead bob-cli-3g.2 is done and closed.

What landed (bob-plugins, bumped to 1.17.0 since 1.16.0 was taken by the 3f.4 CROWDED-chip commit that landed mid-turn — I rebased onto it rather than clobber it):

- Tiered evaluator in `plugins/bob-ledger-tools/main.js`: lane-aware intervals (`pending_interval`/`next_interval`, `false` off-switch), `tier`/`lane` on every evaluation, tier-ordered queue (NEW → PENDING → NEXT → RETURNED → ROTTEN) with per-tier comparators and `tierRank`/`tierTotal`, new counts (`pendingDue`, `nextDue`, `walk`, `upkeepToday`, budget on upkeep).
- Freshness namespace v4 (top-level api stays v3) with machine `tier()`, tier-based `isDue()`, lane-covering `rank()`, and new pure `intervalForLine()` for nav's refresh row.
- Status bar (`⟳ N new · N pending · N next · N rotten · ✓ N today`, walk-order tooltip, new/due/commitment/budget/clear/due modes) and review model meter on upkeep, plus lane marks (M9 due-lane tooltip with keep/release/today keys, M10 stamped-today, M19 disabled-lane resting, M20 no `/30d` suffix).
- Tests carry all walk vectors verbatim (Q1, Q2, L1–L5, R1, R2, rewritten S14, updated S15, B1) plus config, `intervalForLine`, tier/rank, and status-bar mode coverage.

Verified: `npm test` 1172/1172 green, `npm run validate` 6/6, deployed via `bob plugins sync` (vault shows 1.17.0). `sase bead epic-symbols` shows no leftover symbols; primary checkout untouched.
