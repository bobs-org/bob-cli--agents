# Chat History - ace-run (bob-cli-6u.9)

- **TIMESTAMP:** 2026-10-12 16:53:48 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-6u.9

## Prompt

%id(9, clan=bob-cli-6u, bead=bob-cli-6u.9)
%auto
#gh:gh_bobs-org__bob-cli
%model:@medium
%w(bob-cli-6u.4,bob-cli-6u.8, for_epic=false)
%w(bead=bob-cli-6u.4)
%w(bead=bob-cli-6u.8)
Can you complete the work for bead bob-cli-6u.9? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-6u.9 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-6u.9 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-6u.9`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-6u.9 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

## Response

Bead bob-cli-6u.9 is done and closed.

Top finding: capture never creates a live link to a Blocked task now — the staged-graph link guard consumes at all four `plan_task_link` callers, refuses date-only `^prj`, and leaves Blocked new tasks unlinked, with an additive `link_guard` report everywhere.

What landed in this turn:
- New `src/native/capture/link_guard.rs`: `assess_link_target` (PDG1/PDG2/PDG3/PDG6 gesture rule from staged graph reasons, never the `[?]` cache), `assess_destination_project`, `promote_consume_plan`, and the `[?]`+tag flip helper, with unit tests.
- Guard threaded through toggle (`@r+id!`), ensure-next, `@r:id` (plus start combo, which skips the start and reports), and link-then-close (history link kept, no Next flip). Old `[dependsOn::` text warnings replaced by structured `link_guard` (`reasons`, `promoted`, `detail`) plus a human trailer.
- New `:` tasks unlinked when Blocked (future `s:N`, open `&`, or blocked project); `+` projects tag and unlink `:` tasks when P is future. JSON stays additive (verified by the placement shape test); no Mac Capture follow-up needed.
- `docs/capture.md` rows for `:`, `+`, `@r+id!`, `@route:block-id`, and close.
- Tests: 8 new CLI tests (PDG1/PDG3/PDG6 toggles, ensure-next, `@r:id`, close-link history, `:`+`&`, plain-into-blocked-project) plus unit tests; 5 stale-behavior tests updated to the new contract.

Verification: `cargo fmt` clean, `cargo clippy` zero errors, lib 2431 passed, CLI 1388 passed. The only 4 failures reproduce byte-identically on clean master (2 `r#ref` listen-helper env failures tracked by bob-cli-6m; 2 wall-clock-rotted July fixtures), recorded as `PROPOSED FOLLOW-UP` notes. `epic-symbols` clean.
