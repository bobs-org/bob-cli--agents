# Chat History - ace-run (bob-cli-3f.3)

- **TIMESTAMP:** 2026-10-01 18:48:13 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-3f.3

## Prompt

#gh:gh_bobs-org__bob-cli
%id(3, clan=bob-cli-3f, bead=bob-cli-3f.3)
%model:@medium
%auto
%w:bob-cli-3f.1
%w(bead=bob-cli-3f.1)
Can you complete the work for bead bob-cli-3f.3? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-3f.3 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-3f.3 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-3f.3`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-3f.3 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Done. Bead bob-cli-3f.3 (ledger-api) is complete and closed.

What shipped in bob-plugins (`bob-ledger-tools` 1.14.1 → 1.15.0, deployed to the vault via `bob plugins sync`):

- `api.noteReady` v1 (frozen, top-level api stays v3): `snapshot`, `forNote`, `counted`, `inCrowdedNote`, `groupLabel`. One memoized O(tasks) pass keyed on tasks identity/generation, date, eligibility fingerprint generation, caps key, and freshness memo identity; crowded-set changes fire the existing `TODAY_RELOAD_EVENT` query refresh without loops.
- `maxReadyPerNote` (default 5, 1–999) in `defaultPlanCaps`/`coercePlanCaps`/`effectivePlanCaps`, with `loadPlanCaps` stat-cached on path+mtime+size (creation, deletion, invalid edits, recovery, and env overrides all re-read; callers without `statSync` read through uncached as before).
- Shared `noteFrontmatter` reader via `getAbstractFileByPath` + `getFileCache`, fixing bob-cli-3e; `task_refresh` and the eligibility walk route through it.
- R1–R14 vectors as `scripts/test-ledger-tools-note-ready.cjs` (37 tests), wired into `npm test`.

Verification observed: new suite 37/37; full `npm test` 1138/1138 (two pre-existing suites needed phase-mandated updates: the freshness stub migrated to string-only `getCache`/object-only `getFileCache`, one plan-budget expectation gained the new caps key); `npm run validate` 6/6; `cargo fmt --check` clean with the bob-cli tree untouched; `sase bead epic-symbols` empty.
