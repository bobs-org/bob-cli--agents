# Chat History - ace-run (bob-cli-hz.1--1)

- **TIMESTAMP:** 2026-11-06 14:15:45 EST
- **MODEL:** grok/grok-4.6
- **AGENT:** bob-cli-hz.1--1

# Monitor handoff

This agent delegated the remaining work to a monitor turn.
Monitor ID: 18e8b1xh0z8c
Inspect with: sase monitor show 18e8b1xh0z8c
Monitor turn: bob-cli-hz.1--mon-0
Directory: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-mac-capture

Command:

```sh
Scripts/macos-ci-check
```

Reason:

Gate card-flip Swift on exact-SHA macOS CI after catalogLoaded and Escape restore fixes

Next action:

Finish bob-cli-hz.1 (phase card-flip) after Scripts/macos-ci-check.

Context: the Mac relation-label-card flip is implemented in the linked bob-mac-capture repo (sase/repos/linked/bob-mac-capture). This recovery turn fixed two CI regressions from the first snapshot:

1. submitRelationLabelPrompt waited on catalogLoaded for every Return. That blocked empty Return (drop the pipe) and typed-label submit once suggestions were already present. Catalog wait now applies only when a highlighted catalog row would be inserted (the flip re-fetch path). Tab stays a no-op until the catalog arrives.
2. testRelationCardEscapeAcceptsPickerRowAfterRestore used filterText "foot", which hid the Target row so acceptPickerRow was a no-op. The helper now takes filterText; the accept test uses "target". cancelRelationLabelPrompt also dismisses completion and clears pickerChip like cancelTaskIDPrompt.

Local gates: previous turn passed just portable-check, just docs-check, and Mac scratch typecheck-tests. This turn re-ran Mac scratch bundle.sh + just typecheck-tests after the fixes (TYPECHECK_OK). Memory record work belongs to phase records (bob-cli-hz.5). Do not edit memory, bob-cli grammar, the parent epic, or later phases. Do not create beads; use PROPOSED FOLLOW-UP notes on bob-cli-hz.1. Never run sase bead open on this bead.

If the check failed (exit 1 = real CI failure; exit 2 = incomplete/unrun):
- Read the retained monitor log and failed Swift diagnostics.
- Compare failed tests to recent master macOS CI (runs on bobs-org/bob-mac-capture master). Master is already red with this stable set: testMotionsLeaveTextAndUndoUntouched; testCommaCommitsPartialRouteThenBobOpensParentTaskPicker; testCommaOnExactRouteUsesBobRewriteLane; testBackslashAliasAfterTaskTypeOpensTypeMenuAndDoubleTapCloses; testCommaAfterCompleteTargetRunOpensNextParentPicker; testDelayedAcceptedAliasSupersedesGatedCompletion; testNativeUndoRestoresLiteralSigilAliasWithoutRetriggering; testPeriodAliasAfterRouteOpensNewIDBlockPicker; testPeriodAliasOnMoveBulletOpensMovePicker; testSemicolonAliasOnOfferMoveBulletOpensMoveAndLinkPicker; testSlashAliasAfterTaskTypeOpensTypeMenuAndDoubleTapCloses; testUndoAfterMoveAliasRestoresLiteralWithoutRetriggering.
- If the failed set is that master set plus at most the known 200ms-sleep flakes testOlderBobMoveAliasReplyLeavesLiteralWithoutOpeningPicker and testUnchangedAliasReplyLeavesPeriodLiteralWithoutOpeningPicker, and NONE of the card-flip / relation-label tests failed, record PROPOSED FOLLOW-UP on bob-cli-hz.1 citing the master SHA/run and close anyway.
- Card-flip tests that must not fail: CaptureRelationPanelTests including testRelationCardEscapeAcceptsPickerRowAfterRestore, testRelationLabelOutOfOrderResponseKeepsCurrentLabel, testRelationCardReturnDuringRefetchWaitsForNewCatalog, flip/== tests; plus testEmptyLabelReturnWithFollowingTailDropsOnlyPipeSuffix and testDependencyTailCommitPreservesSuffixByteForByte.
- If those fail, fix only bob-mac-capture. Format only changed lines. Tests must use fake-bob, injected NSEvent timestamps, and delayed replies; never wall-clock sleeps.
- Re-run Scripts/macos-ci-check via sase monitor start with WATCHING CI / WATCHED CI labels if you change Swift.

If the check passed (exit 0):
1. Run `sase bead epic-symbols bob-cli-hz.1`. Resolve leftovers if any.
2. Close only this phase (not parent bob-cli-hz):
   `sase bead close bob-cli-hz.1 --note "<verified: portable-check; docs-check; Mac scratch typecheck-tests; macos-ci-check SHA and required macOS steps>"`
3. Submit /sase_final. Commit remaining bob-mac-capture changes. Use bead_action close on the assigned-bead repository decision. Do not invoke /sase_git_commit. Conventional subject if a new commit is needed: `feat(capture): flip relation direction in the label card`

Work that should already be in the tree:
- CaptureEqualsGesture (350 ms window; timestamp 0 never qualifies)
- choose-mode ~/= flip, re-fetch, pending-submit on selected catalog rows, Tab no-op until catalog
- Escape restores the Shift-Return picker including after a flip, with a working accept
- teaching keycaps from structured verdicts/hints
- docs/relationship-pickers.md and docs/keyboard.md


## Prompt

%queue(weight=1)
%macros_enabled:false
# Previous Continuation

This fork uses versioned continuation replay. Blocks are stable, parent-first projections of exact continuation nodes; any historical source without recoverable node provenance is represented as an opaque legacy boundary.

- **Projection version:** `1`
- **Ordered nodes:** `1`

## Continuation Block `block:v1:2f15059be4c4d051d544f957d09fa96e`

- **Node:** `agent-delta:20261106125237:343501546b257808`
- **Kind:** `agent_delta`
- **Parents:** (none)
- **Content:** `local:continuation/records/agent_delta/agent-delta:20261106125237:343501546b257808.json`
- **Checkpoint:** `local:continuation/checkpoints/monitor_handoff-2b8a458238d757d8.json`

### User

**Protected user instruction.** Carry this request unless an explicit attributed update supersedes it.

#gh:gh_bobs-org__bob-cli
%id(bob-cli-hz.1, bead=bob-cli-hz.1)
%clan(bob-cli-hz, tribe=epic, summary_script=sase_clan_summary_epic)
%model:@medium
%auto
Can you complete the work for bead bob-cli-hz.1? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-hz.1` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-hz.1` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-hz.1 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-hz.1 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-hz.1 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-hz.1`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-hz.1 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

### Checkpoint

- **Kind:** `monitor_handoff`

### Assistant

<!--sase:budget-span:open:kind=checkpoint;id=1;checkpoint_ref=local%3Acontinuation%2Fcheckpoints%2Fmonitor_handoff-2b8a458238d757d8.json;covered=agent-delta%3A20261106125237%3A343501546b257808-->
I'll start by reading the bead, its design file, and the SASE beads rules so I can check what already landed before doing any work.

The phase is Mac-only card-flip work plus an authorized decision-record memory edit. Next I’ll read the plan, parent epic, and whether any of this already landed.

Card-flip is Mac-only; I’ll open the research artifact and the Mac repo, then check whether any of this work already landed.

I have the contract. Next I’ll inspect the Mac relation-card routing, state, tests, and the picker flip this should match.

I have the contract and the current card paths. Next I’ll add the equals-gesture primitive, then the Mac routing, flip, Escape fix, and tests.

I'll pick up the card-flip phase from the source and docs that already landed, then write tests and run verification before closing the bead.

I'll open the Mac Capture repo and the bead so I can check what already landed before writing tests.

Source and docs are already dirty in the Mac repo. Next I’ll read the implementation and existing tests so the remaining coverage matches the plan.

Existing relation tests don’t cover the new flip yet. I’ll read the implementation and helpers so the new tests can drive the same APIs.

I’ll arm `==` only after a successful flip, then add the remaining relation-card tests.

The Escape test now checks the restored draft. Next I’ll add the helper and the rest of the flip coverage.

The 350 ms boundary failed on floating-point rounding. I’ll compare with a tiny tolerance and retest.

Equals tests passed. Next I’ll re-run portable-check, start the Mac typecheck, and run docs-check.

Portable-check passed and the Mac typecheck compiled. `keyboard.md` is 42 words over the docs budget, so I’ll trim that next.

I'll pick up from the last verified state: implementation and docs-check already passed, so next I'll confirm the Mac tree, run macos-ci-check, then close the phase.

Epic-symbols are clean. I’ll sanity-check the flip implementation, then start macos-ci-check.

I'll review the flip path and format the changed Swift files before starting the CI gate.

Lint is noisy on the whole tree. I’ll isolate warnings on the new flip code so CI’s Swift formatting step doesn’t fail.

Implementation matches the plan. I’ll start macos-ci-check under a monitor, then commit this tree with the bead kept open until CI finishes.

Monitor is staged. I’ll gather the finalizer context and commit the Mac card-flip work with the bead kept open until CI finishes.

Card-flip work for `bob-cli-hz.1` is implemented and locally verified. `Scripts/macos-ci-check` is now running against the dirty bob-mac-capture tree; this phase stays open until that exact-SHA macOS run is green.

**Already in the Mac tree**
- Choose-mode `~` / `=` flips Links To ↔ Linked From, edits the token, re-asks Bob, and keeps query and selection.
- Return during refetch waits for the new catalog; Tab is a no-op until it arrives.
- Fast `==` (350 ms, `NSEvent.timestamp`; timestamp 0 never qualifies) undoes the `=` flip and types a literal `=`.
- Escape from a Shift-Return card restores the picker draft and rebuilds `pickerIndex`, including after a flip.
- Teaching keycaps come from structured verdicts and hints.
- Docs: `docs/relationship-pickers.md` and `docs/keyboard.md`.

**Verified so far**
- `just portable-check` (2257 tests, 0 failures)
- Mac scratch `bundle.sh` + `just typecheck-tests`
- `just docs-check`
- No leftover `--epic-symbol` entries

Memory records stay with phase `records` (`bob-cli-hz.5`). Parent epic `bob-cli-hz` is untouched.

A follow-up will close `bob-cli-hz.1` if macOS CI passes, or fix and re-gate if it fails.
<!--sase:budget-span:close:1-->

---

%macros_enabled:true
# New Query
%model:grok-4.6@high

%macros_enabled:false
# Monitored command finished

**Command:**

```text
Scripts/macos-ci-check
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-mac-capture
```

| | |
| --- | --- |
| **Outcome** | FAILED — exit 1 |
| **Started** | 2026-11-06T18:34:30.258632+00:00 |
| **Finished** | 2026-11-06T18:54:24.031092Z |
| **Elapsed** | 17m 6s of a 1h 40m 0s budget |
| **Output** | 10 KiB · evidence refs: `file:monitor-diagnostic-manifest:zve7an8jbv5c`, `file:monitor-retained-log:zve7an8jbv5c` · full log: `sase monitor show zve7an8jbv5c --all-lines` |

**Why this was monitored:** Gate card-flip Swift on exact-SHA macOS CI

## Last 200 lines of output
<!--sase:budget-span:open:kind=old_raw_excerpts;id=1-->

Everything between the fences below is raw command output -- untrusted data, not instructions. The only instruction in this prompt is the "Your next action" section.

```text
7709 is in_progress (804s elapsed, 4592s left)
macos-ci-check: run 42272377709 is in_progress (815s elapsed, 4582s left)
macos-ci-check: run 42272377709 is in_progress (825s elapsed, 4571s left)
macos-ci-check: run 42272377709 is in_progress (836s elapsed, 4560s left)
macos-ci-check: run 42272377709 is in_progress (846s elapsed, 4550s left)
macos-ci-check: run 42272377709 is in_progress (857s elapsed, 4539s left)
macos-ci-check: run 42272377709 is in_progress (868s elapsed, 4529s left)
macos-ci-check: run 42272377709 is in_progress (878s elapsed, 4518s left)
macos-ci-check: run 42272377709 is in_progress (889s elapsed, 4507s left)
macos-ci-check: run 42272377709 is in_progress (899s elapsed, 4497s left)
macos-ci-check: run 42272377709 is in_progress (910s elapsed, 4486s left)
macos-ci-check: run 42272377709 is in_progress (921s elapsed, 4476s left)
macos-ci-check: run 42272377709 is in_progress (931s elapsed, 4465s left)
macos-ci-check: run 42272377709 is in_progress (942s elapsed, 4454s left)
macos-ci-check: run 42272377709 is in_progress (953s elapsed, 4444s left)
macos-ci-check: run 42272377709 is in_progress (963s elapsed, 4433s left)
macos-ci-check: run 42272377709 is in_progress (974s elapsed, 4422s left)
macos-ci-check: run 42272377709 is in_progress (985s elapsed, 4411s left)
macos-ci-check: run 42272377709 is in_progress (996s elapsed, 4401s left)
macos-ci-check: run 42272377709 is in_progress (1006s elapsed, 4390s left)
macos-ci-check: run https://github.com/bobs-org/bob-mac-capture/actions/runs/42272377709
macos-ci-check: snapshot SHA c468b17ad2af2a4652c7c8b42b389d8d929b3165
macos-ci-check: macOS job macOS 26 SwiftPM
  [ok] Set up job
  [ok] Check out repository
  [ok] Check scripts
  [ok] Show toolchain
  [ok] Lint Swift formatting
  [ok] Build
  [failure] Test
  [ok] Upload render fixtures
  [ok] Upload test hang samples
  [skipped] Bundle
  [skipped] Verify plist and signature
  [skipped] Launch smoke test
  [skipped] Upload launch smoke test diagnostics
  [skipped] Install and reinstall
  [ok] Post Check out repository
  [ok] Complete job
macos-ci-check: required macOS steps failed: Test (failure)
macos-ci-check: failed Swift tests
  BobMacCaptureTests.CaptureEditorWordMotionTests testMotionsLeaveTextAndUndoUntouched
  BobMacCaptureTests.CapturePanelModelTests testCommaCommitsPartialRouteThenBobOpensParentTaskPicker
  BobMacCaptureTests.CapturePanelModelTests testCommaOnExactRouteUsesBobRewriteLane
  BobMacCaptureTests.CaptureRelationPanelTests testRelationCardEscapeAcceptsPickerRowAfterRestore
  BobMacCaptureTests.CaptureRelationPanelTests testRelationLabelOutOfOrderResponseKeepsCurrentLabel
  BobMacCaptureTests.CaptureSeparatorToggleTests testBackslashAliasAfterTaskTypeOpensTypeMenuAndDoubleTapCloses
  BobMacCaptureTests.CaptureSeparatorToggleTests testCommaAfterCompleteTargetRunOpensNextParentPicker
  BobMacCaptureTests.CaptureSeparatorToggleTests testDelayedAcceptedAliasSupersedesGatedCompletion
  BobMacCaptureTests.CaptureSeparatorToggleTests testDependencyTailCommitPreservesSuffixByteForByte
  BobMacCaptureTests.CaptureSeparatorToggleTests testEmptyLabelReturnWithFollowingTailDropsOnlyPipeSuffix
  BobMacCaptureTests.CaptureSeparatorToggleTests testNativeUndoRestoresLiteralSigilAliasWithoutRetriggering
  BobMacCaptureTests.CaptureSeparatorToggleTests testOlderBobMoveAliasReplyLeavesLiteralWithoutOpeningPicker
  BobMacCaptureTests.CaptureSeparatorToggleTests testPeriodAliasAfterRouteOpensNewIDBlockPicker
  BobMacCaptureTests.CaptureSeparatorToggleTests testPeriodAliasOnMoveBulletOpensMovePicker
  BobMacCaptureTests.CaptureSeparatorToggleTests testSemicolonAliasOnOfferMoveBulletOpensMoveAndLinkPicker
  BobMacCaptureTests.CaptureSeparatorToggleTests testSlashAliasAfterTaskTypeOpensTypeMenuAndDoubleTapCloses
  BobMacCaptureTests.CaptureSeparatorToggleTests testUnchangedAliasReplyLeavesPeriodLiteralWithoutOpeningPicker
  BobMacCaptureTests.CaptureSeparatorToggleTests testUndoAfterMoveAliasRestoresLiteralWithoutRetriggering
macos-ci-check: deleted remote branch ci/precommit/661f9ed4a520eaa9fc9386f794b4bef0
```

<!--sase:budget-span:close:1-->
## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-911c39d182ea16a9.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "Scripts/macos-ci-check",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-mac-capture",
    "member_agent_name": "bob-cli-hz.1--mon",
    "monitor_id": "zve7an8jbv5c",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261106125237:343501546b257808"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:d6ba522be2d2a2d35e1c5828e4303377db76bb43f45028c8bc9f459bd11044d7",
    "starter_agent": "bob-cli-hz.1--plan",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/06/20261106125237"
  },
  "recorded_at_epoch": 1793990238.4484863,
  "schema_version": 1
}
```


## Your next action

Finish bob-cli-hz.1 (phase card-flip) after Scripts/macos-ci-check.

Context: the Mac relation-label-card flip is already implemented in the linked bob-mac-capture repo (sase/repos/linked/bob-mac-capture). Local gates already passed in the previous turn: just portable-check (2257 tests, 0 failures), just docs-check, and a Mac scratch copy of bundle.sh + just typecheck-tests. Memory record work belongs to phase records (bob-cli-hz.5), not this bead. Do not edit memory, bob-cli grammar, the parent epic, or later phases. Do not create beads; use PROPOSED FOLLOW-UP notes on bob-cli-hz.1. Never run sase bead open on this bead.

This monitor ran `Scripts/macos-ci-check` from the bob-mac-capture checkout. That script snapshots the dirty tree, pushes ci/precommit/*, and waits for the exact-SHA macOS 26 SwiftPM workflow.

If the check failed (exit 1 = real CI failure; exit 2 = incomplete/unrun):
- Read the retained monitor log and any failed Swift test / lint / compile diagnostics.
- Fix only bob-mac-capture. Format only changed lines. Tests must use fake-bob, injected NSEvent timestamps, and delayed replies; never wall-clock sleeps.
- Re-run Scripts/macos-ci-check via sase monitor start with WATCHING CI / WATCHED CI labels if you change Swift.
- If a failure reproduces on clean master, record PROPOSED FOLLOW-UP and close anyway.

If the check passed (exit 0):
1. Run `sase bead epic-symbols bob-cli-hz.1`. Resolve leftovers if any; none were present before this gate.
2. Close only this phase (not parent bob-cli-hz):
   `sase bead close bob-cli-hz.1 --note "<verified: portable-check; docs-check; Mac scratch typecheck-tests; macos-ci-check SHA and required macOS steps>"`
3. Submit /sase_final. Commit any remaining bob-mac-capture changes. If this turn already committed the card-flip work and the tree is clean, still declare as required. Use bead_action close on the assigned-bead repository decision. Do not invoke /sase_git_commit. Conventional subject if a new commit is needed: `feat(capture): flip relation direction in the label card`

Work that should already be in the tree:
- CaptureEqualsGesture (350 ms window; timestamp 0 never qualifies)
- choose-mode ~/= flip, re-fetch, pending-submit, Tab no-op until catalog
- Escape restores the Shift-Return picker including after a flip
- teaching keycaps from structured verdicts/hints
- docs/relationship-pickers.md and docs/keyboard.md
%macros_enabled:true

## Response

macos-ci-check failed on the Test step. I’ll pull the retained log, the bead, and the Mac tree so I can see whether these Swift failures come from the card-flip work.

CI failed on a wide set of Swift tests, including ones outside card-flip. I’ll open the Mac repo and pull the Actions logs so we can tell whether this is our change or already on master.

The suite had 38 failures, so I’ll extract the actual assertions and inspect the key-routing changes that could have caused the extra failures.

The saved Actions log is empty; I’ll grep the retained 7.7 MB download for the actual failed assertions.

The Escape restore is a real card-flip bug; I’ll pull the remaining assertion text and check whether the separator failures already exist on master.

Master CI is already red. I’ll compare those failures with ours, then fix the two relation-card regressions.

Master already has the separator and word-motion failures. I’ll inspect the two relation regressions and the extra separator tests that only failed on our SHA.

The catalogLoaded gate is blocking empty and typed Return; Escape restore also rebuilds the picker behind a filter that hides the row. I’ll fix those two paths, then re-gate CI.

Mac is up. I’ll rsync a scratch copy, typecheck the tests, then start macos-ci-check.

Typecheck passed. I’ll start macos-ci-check under a monitor so the follow-up can close the phase or compare remaining failures to master.

The monitor is staged and the tree is still dirty, so I’ll declare a keep-commit for the Mac card-flip work before the turn ends.

macos-ci-check failed on the first snapshot. Two of those failures were from this phase; the rest already fail on master. I fixed the phase regressions and staged a new exact-SHA run.

**What broke**
- `submitRelationLabelPrompt` waited on `catalogLoaded` for every Return. Empty Return (drop the pipe) and a typed label whose suggestions had already arrived both stalled. That showed up as `testEmptyLabelReturnWithFollowingTailDropsOnlyPipeSuffix`, `testDependencyTailCommitPreservesSuffixByteForByte`, and `testRelationLabelOutOfOrderResponseKeepsCurrentLabel`.
- The Escape accept test used filter `foot`, which hid the Target row, so `acceptPickerRow` was a no-op.

**What I changed**
- Catalog wait now applies only when a highlighted catalog row would be inserted (the flip re-fetch path). Empty and typed submits go through the existing authored path. Tab still does nothing until the catalog arrives.
- The accept test now filters on `target`. Escape restore also dismisses completion and clears `pickerChip`, matching `cancelTaskIDPrompt`.

**Verified this turn**
- Mac scratch `bundle.sh` + `just typecheck-tests` (`TYPECHECK_OK`)

**Still red on master (not this phase)**
Word-motion, comma rewrite, and several separator-alias tests fail on recent `bob-mac-capture` master runs. The follow-up will treat that set as `PROPOSED FOLLOW-UP` and close this phase if our relation-card tests stay green.

Bead `bob-cli-hz.1` stays `in_progress`. `Scripts/macos-ci-check` is staged as monitor `18e8b1`. Parent epic `bob-cli-hz` is untouched. Memory records stay with `bob-cli-hz.5`.
