%queue(weight=1)
#fork:bob-cli-hz.2--plan
%model:gpt-6-luna
%effort:xhigh

%macros_enabled:false
# Monitored command finished

**Command:**

```text
just check
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-11-06T18:27:35.789273+00:00 |
| **Finished** | 2026-11-06T18:37:25.909249Z |
| **Elapsed** | 8m 17s of a 1h 0m 0s budget |
| **Output** | 1,169 KiB · evidence refs: `file:monitor-diagnostic-manifest:tq10trm99zt1`, `file:monitor-retained-log:tq10trm99zt1` · raw output omitted: `facts_only` · full log: `sase monitor show tq10trm99zt1 --all-lines` |
| **Tool run** | sase tool show 23a2a1aa5149111404b2db4c763c1c4b |

**Why this was monitored:** Verify bob-cli-hz.2 before host commit and close

## Failure triage

verdict: pass

KNOWN 0; FLAKY 0

sase tool show 23a2a1aa5149111404b2db4c763c1c4b -j

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