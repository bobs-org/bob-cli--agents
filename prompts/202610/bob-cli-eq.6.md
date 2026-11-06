- **AGENTS:**
  - [bbugyi200.apollo.bob-cli-eq.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-eq.6.md)

%queue(weight=1) #fork:bob-cli-eq.6--plan %model:muse-spark-1.3-contributor
%effort:xhigh

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

|              |                                                                                                                                                                                                                |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Outcome**  | COMPLETED — exit 0                                                                                                                                                                                             |
| **Started**  | 2026-10-30T23:24:23.908389+00:00                                                                                                                                                                               |
| **Finished** | 2026-10-30T23:34:44.495694Z                                                                                                                                                                                    |
| **Elapsed**  | 10m 18s of a 1h 0m 0s budget                                                                                                                                                                                   |
| **Output**   | 740 KiB · evidence refs: `file:monitor-diagnostic-manifest:m8vc69wjgnt0`, `file:monitor-retained-log:m8vc69wjgnt0` · raw output omitted: `facts_only` · full log: `sase monitor show m8vc69wjgnt0 --all-lines` |
| **Tool run** | sase tool show 374567ec7c4398c7a32396dba0877c12                                                                                                                                                                |

**Why this was monitored:** Verify before host completion

## Failure triage

verdict: pass

KNOWN 0; FLAKY 0

sase tool show 374567ec7c4398c7a32396dba0877c12 -j

## Host completion

Verification COMPLETED — exit 0, but host completion did not land the change.

- `stale_worktree_fingerprint` — the worktree changed after the completion was sealed —
  re-prepare the completion on the current tree.
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
