%queue(weight=1)
#fork:bob-cli-df.2.1.4.3.2--1
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
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-10-28T10:15:04.334076+00:00 |
| **Finished** | 2026-10-28T10:22:03.787722Z |
| **Elapsed** | 6m 58s of a 1h 0m 0s budget |
| **Output** | 704 KiB · evidence refs: `file:monitor-diagnostic-manifest:g081k1v3shsh`, `file:monitor-retained-log:g081k1v3shsh` · raw output omitted: `facts_only` · full log: `sase monitor show g081k1v3shsh --all-lines` |
| **Tool run** | sase tool show acaebd491d89acef7452ff58a59f46c2 |

**Why this was monitored:** Verify adapter-recovery before host completion

## Failure triage

verdict: pass

KNOWN 0; FLAKY 0

sase tool show acaebd491d89acef7452ff58a59f46c2 -j

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