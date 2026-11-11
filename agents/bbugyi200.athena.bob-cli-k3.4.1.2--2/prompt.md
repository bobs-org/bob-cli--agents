%queue(weight=1)
#fork:bob-cli-k3.4.1.2--1
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
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-11-11T15:54:51.498120+00:00 |
| **Finished** | 2026-11-11T16:03:25.938783Z |
| **Elapsed** | 7m 37s of a 1h 0m 0s budget |
| **Output** | 1,366 KiB · evidence refs: `file:monitor-diagnostic-manifest:tyjp6x775yz2`, `file:monitor-retained-log:tyjp6x775yz2` · raw output omitted: `facts_only` · full log: `sase monitor show tyjp6x775yz2 --all-lines` |
| **Tool run** | sase tool show a2ca0836e696049f0ce867f5f7139730 |

**Why this was monitored:** Verify records-surface before host completion

## Failure triage

verdict: pass

KNOWN 0; FLAKY 0

sase tool show a2ca0836e696049f0ce867f5f7139730 -j

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