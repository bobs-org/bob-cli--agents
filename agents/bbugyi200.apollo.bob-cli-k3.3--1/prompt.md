%queue(weight=1)
#fork:bob-cli-k3.3--plan
%model:grok-4.6
%effort:high

%macros_enabled:false
# Monitored command finished

**Command:**

```text
just check
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-11-11T10:37:39.378675+00:00 |
| **Finished** | 2026-11-11T10:45:40.920332Z |
| **Elapsed** | 6m 51s of a 1h 0m 0s budget |
| **Output** | 1,350 KiB · evidence refs: `file:monitor-diagnostic-manifest:x0w4qv4sm2vt`, `file:monitor-retained-log:x0w4qv4sm2vt` · raw output omitted: `facts_only` · full log: `sase monitor show x0w4qv4sm2vt --all-lines` |
| **Tool run** | sase tool show dc1a1f564abebd22681b81987c76fb73 |

**Why this was monitored:** Verify before host completion

## Failure triage

verdict: pass

KNOWN 0; FLAKY 0

sase tool show dc1a1f564abebd22681b81987c76fb73 -j

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