# Chat History - ace-run (bob-cli-3f.2)

- **TIMESTAMP:** 2026-10-01 18:48:29 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-3f.2

## Prompt

#gh:gh_bobs-org__bob-cli
%id(2, clan=bob-cli-3f, bead=bob-cli-3f.2)
%model:@medium
%auto
%w:bob-cli-3f.1
%w(bead=bob-cli-3f.1)
Can you complete the work for bead bob-cli-3f.2? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-3f.2 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-3f.2 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-3f.2`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-3f.2 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Done. Bead **bob-cli-3f.2** (`bob ready` command) is implemented and closed.

What shipped:

- **`bob ready [NOTE]`** — read-only per-note Ready-cap view: colored CROWDED/FULL/ROOM bar overview, per-note worklist in file order with `path:line` refs and `new`/`rotten Nd`/`fresh Nd` labels, schema-1 JSON for both, `--check` (exit 3), `--cap N` preview (source `preview`, overrides/exemptions intact), `--all`, and forgiving resolution (vault path → exact stem → case-insensitive stem; ambiguous lists candidates, unknown suggests up to 3 names, exit 2).
- **Scan** (`scan.rs`): `--cap` preview support, worklist row details plus NEXT/PENDING/BLOCKED per-note counts. The overview skips those extra lane passes, so it costs one freshness scan plus the typed-note walk.
- **Wiring**: `NativeCommand::Ready`, `SUBCOMMANDS` entry after `randomize`, top-level help example, `justfile` smoke entry.
- **Tests**: 19 integration tests (`tests/cli/ready.rs`: JSON totals/order, human sections, all-clear, `-a` + LINTS, preview, `--check` 0/3, worklist order/labels/`also here`, resolution errors, invalid config, help) plus 5 render unit tests (color on/off); help cases and ordering updated.
- **Docs**: `docs/plan.md` `## bob ready` + Surfaces row; README table row + Ready cap section.

Verified: `cargo fmt --check` clean, clippy clean for all touched files (one pre-existing `TypedNote` warning left alone), full `cargo test` green (1461 lib + 718 CLI, 0 failures). Live-vault timing: `bob ready` overview ~7.0s vs `bob freshness list` ~7.8s — comparable, no per-note rescans. `epic-symbols` showed no leftovers. One observation for the rollout phase: the live vault currently shows `gkeep_inbox` crowded 65/5, which 3f.5's inbox exemptions will resolve.

Declaration submitted: `commit` accepted with `bead_action: close` for bead bob-cli-3f.2.
