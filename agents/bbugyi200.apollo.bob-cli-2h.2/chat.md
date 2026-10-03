# Chat History - ace-run (bob-cli-2h.2)

- **TIMESTAMP:** 2026-09-29 10:04:12 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-2h.2

## Prompt

#gh:gh_bobs-org__bob-cli
%id(2, clan=bob-cli-2h, bead=bob-cli-2h.2)
%model:@medium
%auto
Can you complete the work for bead bob-cli-2h.2? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-2h.2 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-2h.2 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-2h.2`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-2h.2 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Bead bob-cli-2h.2 is closed.

Result: the `^` Active Task Picker in the `bob-mac-capture` checkout is now source-agnostic `CapturePicker*` building blocks, with `^` as the only source (`.activeTask`).

What changed (all in `sase/repos/external/gh/bobs-org/bob-mac-capture`, staged, uncommitted for the land agent):
- New `Sources/CaptureCore/CapturePickerPresentation.swift`: `CapturePickerSource` (all `^` strings/keys), `CapturePickerNeed`, `CapturePickerTaskStatus` (`/ * space ? x/X -` mapping), `CapturePickerGlyph/Availability/SectionKind/Section/Row/Detail/Mode/EmptyState/Presentation/Navigation`.
- `ActiveTaskPickerIndex` kept source-specific, now emits `CapturePickerPresentation`; `ActiveTaskDisplayText` → `TaskDisplayText`.
- Model: `CapturePickerState/ChipState` (+`source`), `CapturePickerIndex` enum, generic ops (`presentPicker`, row-`insertion`-based `acceptPickerRow`, `escapePicker`/`cancelPicker`/`removePickerTrigger` via `source.triggerByte`, `openPickerFromChip`), generic `pickerNeed` quiet-status check.
- Routing (`acceptPickerRow…`, `pickerVisible/FilterIsEmpty/ChipVisible`), `.pickerFilter` focus target, `repairPickerFilterFocusIfNeeded`, per-source filter field (plus the plan-mandated substitution/spelling disabling), `CapturePickerCard/Chip/KeyHints/HeightPolicy/RichText`, `taskStatus(_:)` palette extended per UX spec.
- Tests adapted to new names (values unchanged except `?`→`.task(.blocked)` per the plan's mapping); new `CapturePickerTaskStatus` mapping tests added.

Verification actually performed (no Swift/Xcode toolchain exists on this Linux host — `xcode-swift.sh` fails fast, confirmed): zero stale `ActiveTask*` picker references; normalized diff proves ranking/grouping/count/budget code byte-identical; non-ASCII census matches HEAD; all user strings, announcements, UD key, counts verified identical; every cross-file symbol and model-member reference audited; brace balance clean. Diff review caught and fixed 4 real `guard let picker = picker` shadowing defects the compiler would have rejected.

Caveats for the land agent: macOS `swift build/test` and the before/after `BOB_MAC_CAPTURE_RENDER_DIR` image comparison still need to run — recorded as a `PROPOSED FOLLOW-UP` on the bead. Intended visible deltas (per plan): proper glyphs/names for todo/blocked/done/canceled statuses, the `picker-filter` accessibility identifier, and no em-dash substitution in the filter. `epic-symbols` was clean; parent epic left open.

Declaration accepted. Bead bob-cli-2h.2 work committed (bead_action `keep`, since this external repo is not the primary owner and the bead was already closed); no new edits made this turn.
