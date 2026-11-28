%queue(weight=1)
#fork:1hk--code
%model:muse-spark-1.3-contributor
%effort:xhigh

%macros_enabled:false
# Monitored command finished

**Command:**

```text
just check
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-11-28T01:34:50.202049+00:00 |
| **Finished** | 2026-11-28T01:47:22.777775Z |
| **Elapsed** | 11m 13s of a 1h 0m 0s budget |
| **Output** | 1,814 KiB · evidence refs: `file:monitor-diagnostic-manifest:63851r8zk4ny`, `file:monitor-retained-log:63851r8zk4ny` · raw output omitted: `facts_only` · full log: `sase monitor show 63851r8zk4ny --all-lines` |
| **Tool run** | sase tool show 216bfdeb390f582bcc3a9161894f3f5a |

**Why this was monitored:** Verify before host completion

## Failure triage

verdict: pass

KNOWN 0; FLAKY 0

sase tool show 216bfdeb390f582bcc3a9161894f3f5a -j

## Host completion

Verification COMPLETED — exit 0, but host completion did not land the change.

- `missing_required_stage:formatting` — the check produced no matching stage evidence for 'formatting' — re-running the same check cannot fix this; run the verification inline, then `sase final submit` the same wrapper file.
- `missing_required_stage:ruff` — the check produced no matching stage evidence for 'ruff' — re-running the same check cannot fix this; run the verification inline, then `sase final submit` the same wrapper file.
- `missing_required_stage:mypy` — the check produced no matching stage evidence for 'mypy' — re-running the same check cannot fix this; run the verification inline, then `sase final submit` the same wrapper file.
- `missing_required_stage:validation` — the check produced no matching stage evidence for 'validation' — re-running the same check cannot fix this; run the verification inline, then `sase final submit` the same wrapper file.
- `missing_required_stage:scoped_tests` — the check produced no matching stage evidence for 'scoped_tests' — re-running the same check cannot fix this; run the verification inline, then `sase final submit` the same wrapper file.

## Your next action

Diagnose failures or stale verification, then finish the requested change.
%macros_enabled:true