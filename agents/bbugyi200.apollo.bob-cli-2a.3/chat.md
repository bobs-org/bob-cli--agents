# Chat History - ace-run (bob-cli-2a.3)

- **TIMESTAMP:** 2026-09-28 11:42:49 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-2a.3

## Prompt

#gh:gh_bobs-org__bob-cli
%id(3, clan=bob-cli-2a, bead=bob-cli-2a.3)
%model:@medium
%auto
%w:bob-cli-2a.2
%w(bead=bob-cli-2a.2)
Can you complete the work for bead bob-cli-2a.3? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-2a.3 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-2a.3 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-2a.3`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-2a.3 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Done. Bead bob-cli-2a.3 is closed.

Implemented mac_shift in bob-mac-capture ([794f06a](https://github.com/bobs-org/bob-mac-capture/commit/794f06a14b53bd1cd72fb7763cb5b96645800ab4), [CI 36444782814](https://github.com/bobs-org/bob-mac-capture/actions/runs/36444782814) green):

- Tolerant `pomodoro_shift` spec/summary decoding on parse, item, and capture responses including batches; older Bob decodes as nil.
- New pure `CapturePomodoroShiftPresentation` (status/session/destination text, `chevron.forward.2`/`backward.2`, accessibility, notification detail) mirroring CLI wording.
- Preview shift row, Shift/Adjust footer titles, `pomodoro_shift` palette mapping, Shift notifications with day-file subtitle fallback and batch suffixes.
- Smart dashes disabled on the draft `NSTextView` via testable helper; Tab `--`→`—` snippet and smart quotes unchanged, documented in README.
- Real-bob fixtures (later/earlier/bare/no-running/mixed/parse), extended `fake-bob`, new/updated CaptureCore + macOS tests, README grammar updates.

No `PROPOSED FOLLOW-UP` entries; no epic-symbol leftovers.
