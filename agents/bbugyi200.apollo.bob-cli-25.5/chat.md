# Chat History - ace-run (bob-cli-25.5)

- **TIMESTAMP:** 2026-09-20 19:05:48 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-25.5

## Prompt

#gh:gh_bobs-org__bob-cli
%id(5, clan=bob-cli-25, bead=bob-cli-25.5)
%model:@small
%auto
%w:bob-cli-25.1,bob-cli-25.3
%w(bead=bob-cli-25.1)
%w(bead=bob-cli-25.3)
Can you complete the work for bead bob-cli-25.5? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file, do the work, and close only this bead with
`sase bead close bob-cli-25.5 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-25.5`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-25.5 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads.

## Response

Bead bob-cli-25.5 is done and closed.

Work, all in the bob-mac-capture checkout (primary bob-cli tree untouched):

- [CompletionRowContent.swift](…/Sources/CaptureCore/CompletionRowContent.swift): `project_note_marker` maps to `.explicitToggle`, so the `+` sigil highlights yellow like the other sigils.
- [NotificationService.swift](…/Sources/BobMacCapture/NotificationService.swift): `friendlyKindLabel` returns `Project` for `project_note` / `project-note` instead of the generic title-caser.
- Tests: `project_note_marker → .explicitToggle` assertion in `CompletionRowContentTests`, and a `Project captured` single-notification test in `NotificationServiceTests`.
- Confirmed the plan's "deliberately not required" claim by reading the code: `completionSpanKinds` and `routeSpanKinds` already contain the unchanged route/block-ID span kinds, and modes flow through opaquely, so no other changes were needed.

Verification: live `bob capture-parse` reports mode `project_note` with a `project_note_marker` span, and a `--dry-run` JSON capture reports `kind: project_note` with `route_label: cash_goog_exit.md`. No `--epic-symbol` leftovers. One caveat: the Swift suite couldn't run here (no macOS toolchain; the repo tests via `xcode-swift.sh`), so the new assertions are pattern-matched to neighboring cases but unverified by execution.
