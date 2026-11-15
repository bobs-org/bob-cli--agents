- **AGENTS:**
  - [bbugyi200.apollo.bob-cli-ln.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ln.2.md)

%queue(weight=1) #fork:bob-cli-ln.2--2 %model:muse-spark-1.3-contributor %effort:xhigh

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

|              |                                                                                                                                                                                                                  |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Outcome**  | COMPLETED — exit 0                                                                                                                                                                                               |
| **Started**  | 2026-11-14T23:33:35.350854+00:00                                                                                                                                                                                 |
| **Finished** | 2026-11-14T23:49:58.328245Z                                                                                                                                                                                      |
| **Elapsed**  | 8m 47s of a 1h 0m 0s budget                                                                                                                                                                                      |
| **Output**   | 1,481 KiB · evidence refs: `file:monitor-diagnostic-manifest:pb3p266xg2vc`, `file:monitor-retained-log:pb3p266xg2vc` · raw output omitted: `facts_only` · full log: `sase monitor show pb3p266xg2vc --all-lines` |
| **Tool run** | sase tool show 20d149796c5fe1f8b9a0c6c05e96fc9c                                                                                                                                                                  |

**Why this was monitored:** Verify areas-graph fix before host completion

## Failure triage

verdict: pass

KNOWN 0; FLAKY 0

sase tool show 20d149796c5fe1f8b9a0c6c05e96fc9c -j

## Host completion

Verification COMPLETED — exit 0, but host completion did not land the change.

- `missing_required_stage:formatting` — the check produced no matching stage evidence
  for 'formatting' — re-running the same check cannot fix this; run the verification
  inline, then `sase final submit` the same wrapper file.
- `missing_required_stage:ruff` — the check produced no matching stage evidence for
  'ruff' — re-running the same check cannot fix this; run the verification inline, then
  `sase final submit` the same wrapper file.
- `missing_required_stage:mypy` — the check produced no matching stage evidence for
  'mypy' — re-running the same check cannot fix this; run the verification inline, then
  `sase final submit` the same wrapper file.
- `missing_required_stage:validation` — the check produced no matching stage evidence
  for 'validation' — re-running the same check cannot fix this; run the verification
  inline, then `sase final submit` the same wrapper file.
- `missing_required_stage:scoped_tests` — the check produced no matching stage evidence
  for 'scoped_tests' — re-running the same check cannot fix this; run the verification
  inline, then `sase final submit` the same wrapper file.

## Your next action

Diagnose failures or stale verification, then finish the requested change.
%macros_enabled:true
