# Chat History - ace-run (179--plan)

- **TIMESTAMP:** 2026-11-03 09:29:27 EST
- **MODEL:** claude/opus
- **AGENT:** 179--plan

**Plan:** /home/bryan/.sase/plans/202611/fix_sase_readout_marker_audit.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/fix_sase_readout_marker_audit.md`

> # Fix sase Master Gate: review the split readout contexts in the marker path-passing audit
> ## Problem
> The sase repo's (`sase-org/sase`) `Master Gate` workflow is red on `master` at
> `323a91d69f refactor(instructions): split readout.py into focused submodules` (run
> 41647853290, job `test (5)`, step "Run sharded fast suite"). Every other job (lint,
> docs, core-wheel, test shards 1-4 and 6-8) passed. The single failure is deterministic,
> not a flake:
> ```
> FAILED tests/test_agent_artifact_marker_path_passing_audit.py::test_tracked_marker_path_passing_sites_are_reviewed
>   Extra items in the left set:

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli GitHub Actions is failing for the sase repo. Can you run the `actstat` command to get more information about
the failing jobs, diagnose the root cause of these failures, and then fix them? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I opened the sase repo. Its latest Master Gate run fails one audit test after the `readout.py` split. Now I'm reading that test and the split to find the root cause.

The plan passes validation. Submitting it.

I've submitted a plan to fix the sase-org/sase CI failure. It's staged for your approval and no code has changed yet.

**What's failing:** sase's Master Gate run on `master` fails in a single job, `test (5)`, at commit `323a91d69f` ("split readout.py into focused submodules"). The other test shards plus lint, docs and core-wheel all passed. It's a real failure, not a flake: one test fails every time.

```
FAILED tests/test_agent_artifact_marker_path_passing_audit.py::test_tracked_marker_path_passing_sites_are_reviewed
  Extra: _readout_classify.py:classify_artifact_dir, _readout_build.py:build_readout
```

**Root cause:** The split renamed the private helper `_read_json` to a public `read_json` in `_readout_shared.py`.
- This test checks every function that passes a tracked file path like `agent_meta.json` to another function. Each one must have a hand-written review entry, unless the function it calls is on a "safe" list.
- `_read_json` is on that list and `read_json` isn't, so two functions that only read files now count as unreviewed.
- The split updated `test_readout.py` but not this test.

I reproduced the mismatch locally: exactly those two extra entries, nothing missing.

**The fix (tale plan, size `small`):** Add two review entries to `tests/test_agent_artifact_marker_path_passing_audit.py`, each noting the function only reads files. No source code changes. Checks are `just fmt`, `sase tool run check`, and the two affected test files.

I ruled out the shortcut of adding `read_json` to the safe list. Many unrelated sase modules have their own `read_json`, and the test matches by name alone. A simulation showed the shortcut would hide 9 functions that are already reviewed, including `healer_relaunch.py:_write_evidence`, which writes a copy of `done.json`. Adding one entry per function is also how this test was handled after an earlier split (`82cf081fc4`).

`actstat` also showed failures in other repos that the plan doesn't cover:
- **bob-cli:** `test (macos-latest)` was cancelled at about 45 minutes on the last 3 master commits, probably a job timeout.
- **sase-core:** the macOS `cargo test` job is failing.
- **bob-mac-capture:** SwiftPM build and test are failing.
- **bobs-org.github.io:** the weekly external link check is failing.

I can plan fixes for any of these if you want.
