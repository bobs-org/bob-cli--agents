# Chat History - ace-run (17r--plan)

- **TIMESTAMP:** 2026-11-03 17:04:56 EST
- **MODEL:** claude/opus
- **AGENT:** 17r--plan

**Plan:** /home/bryan/.sase/plans/202611/fix_bob_mac_capture_ci_4.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/fix_bob_mac_capture_ci_4.md`

> # Fix bob-mac-capture's red macOS CI
> ## Context
> `bobs-org/bob-mac-capture` has had no green `CI` run on `master` since at least
> 2026-10-30. Its only job, **macOS 26 SwiftPM**, fails at the **Test** step. Every recent
> run fails the same 23 tests (52 assertion failures, out of 3799 tests). Runs checked:
> 41714104187 (b9896cc, the current HEAD), 41692235919, 41676545644, 41570850719, and
> precommit snapshot 41709503302.
> All work happens in the linked repo `bob-mac-capture`. Open it with `/sase_repo`
> (`sase repo open bob-mac-capture -r "..."`), use the printed path, and read its
> `AGENTS.md` first. It requires that Swift is compiled, that `.swift-format` style is

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli GitHub Actions is failing for the bob-mac-capture repo. Can you run the `actstat` command to get more information about
the failing jobs, diagnose the root cause of these failures, and then fix them? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Update: all recent failing runs fail the same 23 tests across 7 test classes. One precommit snapshot (`41666050673`) failed only 1 of them, so I'm comparing it with master to see what it changed.

I have the full diagnosis. Loading the planning skill to write it up.

Update: the first plan validation flagged missing `title`/`goal` and over-long decision labels. Shortening them and adding decision callouts.

Validation passed. Submitting the plan.

I've worked out why bob-mac-capture's CI fails, and the fix plan is staged for your approval. I haven't changed any files yet.

**What's failing:** the only job, `macOS 26 SwiftPM`, fails at the **Test** step on every master push since at least Oct 30. Every recent run fails the same 23 tests, for five separate reasons:

1. **Test data is older than the app's version check (13 tests).** Commit `72daffb` made the app refuse anything from bob older than capture-language version 5. Three real-bob parse fixtures (recorded bob output used as test data) still say 3 or 2, and about 67 hand-written responses in `fake-bob` still say 3. So the app treats them as an outdated bob and skips the clipboard read, polling and submit. That breaks 11 `CaptureClipPreviewHostedTests` and 2 command-accept submit tests.
2. **One test has a timing race (1 test).** In `testTwoClipboardChangesSupersedeOlderPreviewsForTheSameDraft`, the app can kill an in-flight `fake-bob` before it advances its counter file. The next preview then gets the wrong canned response.
3. **One `fake-bob` response contradicts itself (1 test).** The `@file+goog-exit#fix` retype-move response says the task moved to an existing FIX entry, but also `creates_pomodoro: true`.
4. **Pull-In card ordering and caption (3 tests).** Commit `17bd529` changed the code so keep-moving no longer sorts last when bob lists only some groups. It also made bob-supplied copy hide the old "Unblocked by …" caption, which one older test still expects. A third test assumes a recorded fixture has one keep-moving offer; it has three. That test was written in the same commit as the fixture and has never passed.
5. **Outdated expectations in six tests:**
   - Two undo tests use a text view with no window, so there is no undo manager.
   - A lone `+` has opened the parent-task picker since Oct 3, not the active-task picker the test expects.
   - The `#fix Fix it` test puts the cursor at the end, where real bob offers no type menu.
   - The no-visibility-write check fails because other calls create the record file it asserts is absent.
   - The line-case undo test expects a caret position that differs from AppKit's normal undo. `docs/keyboard.md` says the app follows normal undo.

An earlier agent pushed a CI test snapshot (`aceea6ae`) that fixed 22 of the 23, but never landed it. It edited the version number in the recorded fixtures by hand, and its fix for the race test reads the counter with `Int("1\n")`, which is always `nil` in Swift. That bug is why one test still failed.

**The plan:**
- Regenerate the recorded fixtures from the current bob. A trial run in a scratch copy changed 66 files by one line each, with no meaningful content changes.
- Make the fixture generator require the app's minimum version, and add a test that fails if any recorded fixture falls below it.
- Move the 67 hand-written `fake-bob` responses to version 5.
- Fix the race test, the self-contradicting response, and the Pull-In ordering code.
- Update the stale tests and one stale line in `docs/protocol.md`.

The real check is `Scripts/macos-ci-check`, which pushes a temporary branch and waits for the actual macOS CI run.

**Decisions for you when approving** (defaults shown first):
- **Recorded fixtures:** regenerate them, or hand-edit the version number in three files.
- **`fake-bob` responses:** update all 67, or only the two the failing tests use.
- **Pull-In order:** fix the code so keep-moving sorts last again, or change the test to match the new order.
- **Line-case undo:** keep AppKit's normal caret placement after undo, or restore the caret to where it was before the toggle.
