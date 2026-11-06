%queue(weight=1)
#fork:bob-cli-ey.1.1.4--1
%model:grok-4.6
%effort:medium

%macros_enabled:false
# Monitored command finished

**Command:**

```text
just check
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-11-01T00:33:21.610708+00:00 |
| **Finished** | 2026-11-01T00:39:17.519505Z |
| **Elapsed** | 5m 53s of a 1h 0m 0s budget |
| **Output** | 772 KiB · evidence refs: `file:monitor-diagnostic-manifest:0vkfp5pj5g96`, `file:monitor-retained-log:0vkfp5pj5g96` · raw output omitted: `facts_only` · full log: `sase monitor show 0vkfp5pj5g96 --all-lines` |
| **Tool run** | sase tool show 7f7dd66a576307cf6db66dcec5ca9755 |

**Why this was monitored:** Verify before host completion

## Failure triage

verdict: pass

KNOWN 0; FLAKY 0

sase tool show 7f7dd66a576307cf6db66dcec5ca9755 -j

## Host completion

Verification COMPLETED — exit 0, but host completion did not land the change.

- `stale_worktree_fingerprint` — the worktree changed after the completion was sealed — re-prepare the completion on the current tree.
- `missing_required_stage:formatting` — the check produced no matching stage evidence for 'formatting' — re-running the same check cannot fix this; run the verification inline, then `sase final submit` the same wrapper file.
- `missing_required_stage:ruff` — the check produced no matching stage evidence for 'ruff' — re-running the same check cannot fix this; run the verification inline, then `sase final submit` the same wrapper file.
- `missing_required_stage:mypy` — the check produced no matching stage evidence for 'mypy' — re-running the same check cannot fix this; run the verification inline, then `sase final submit` the same wrapper file.
- `missing_required_stage:validation` — the check produced no matching stage evidence for 'validation' — re-running the same check cannot fix this; run the verification inline, then `sase final submit` the same wrapper file.
- `missing_required_stage:scoped_tests` — the check produced no matching stage evidence for 'scoped_tests' — re-running the same check cannot fix this; run the verification inline, then `sase final submit` the same wrapper file.

## Your next action

Diagnose failures or stale verification, then finish the requested change.
%macros_enabled:true