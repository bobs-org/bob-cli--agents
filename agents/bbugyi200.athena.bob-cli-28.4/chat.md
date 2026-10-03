# Chat History - ace-run (bob-cli-28.4)

- **TIMESTAMP:** 2026-09-27 12:54:08 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-28.4

## Prompt

#gh:gh_bobs-org__bob-cli
%id(4, clan=bob-cli-28, bead=bob-cli-28.4)
%model:@medium
%auto
%w:bob-cli-28.3
%w(bead=bob-cli-28.3)
Can you complete the work for bead bob-cli-28.4? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. Read its
description and design file with `sase bead read bob-cli-28.4 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-28.4 --note "<what you verified>"`. Before closing, run
`sase bead epic-symbols bob-cli-28.4`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-28.4 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open.

## Response

Bead **bob-cli-28.4** is closed. The mac-capture phase is implemented in the linked `bob-mac-capture` checkout (primary `bob-cli` tree untouched).

What landed (12 files, +1266/−35):

- **Decode** ([CaptureModels.swift](//home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-mac-capture/Sources/CaptureCore/CaptureModels.swift)): new tolerant `ActiveTaskPomodoro` (`line/name/time_range/is_current`) on completion candidates; `pomodoro_link` success fields were already present from the toggle work and verified against live `bob` JSON.
- **Gate** (`CapturePanelModel.swift`): `active_task` need + `active_task_route`/`block_id` spans request completion; both kept out of `routeSpanKinds`, so cached route completion never intercepts `^` and Bob's `needs` covers lone `^` with no Swift sniffing. Accept uses the generic replacement path (suffix-safe, no re-open).
- **Picker row** ([CompletionRowContent.swift](//home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-mac-capture/Sources/CaptureCore/CompletionRowContent.swift)): `.activeTask` branch — task text primary with query emphasis, `route:block-id · section` secondary, `Now · NAME HHMM-HHMM` / name / `Planned` / `Not queued` badge, "Active Task" label, distinct In Progress (`play.circle`, green) vs Next (`bookmark`, indigo) glyph+tint.
- **Preview/notifications**: new `CapturePomodoroLinkPresentation` (transition, ledger outcome incl. created destination, `Link`/`Start` footer verb, `Started/Linked to/Moved to/Already in NAME` titles, accessibility summary; reuses toggle endpoint/status/day-file helpers and the start presentation for the session row), wired into preview dispatch, footer, Command-Return day-file gating, and notifications (single + batch + `Link` kind label).
- **Tests**: fake-bob fixtures for `^`, `^dee`, full accept, `#b` name completion, linked/moved+created/already-current/start captures, near-miss error, solo `@sase:deep-fix=`; 8 new presentation tests, 4 row tests, 4 decode tests, 4 notification tests, 5 panel-model tests; README contract/row/notification docs.

Verified: `swift test --filter CaptureCoreTests` → 204/206 pass. The 2 failures (`testCancellationTerminatesProcess`, timeout-termination) reproduce identically on the clean base tree — recorded as a follow-up, not a blocker. App-target files parse-check (they can't compile on Linux).

Two caveats for the land agent (both recorded on the bead): the linked-repo changes are **uncommitted** (no commit authorization in this turn), and the **macOS 26 CI run still needs to be pushed and confirmed** — the app-target compile and full `swift test` can only run on macOS.

Declaration submitted: linked `bob-mac-capture` work committed with `bead_action: keep` (close refused — only the primary repo may close; bead bob-cli-28.4 is already closed).
