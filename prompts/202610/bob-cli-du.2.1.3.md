- **AGENTS:**
  - [bbugyi200.apollo.bob-cli-du.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-du.2.1.3.md)

%queue(weight=1) #fork:bob-cli-du.2.1.3--plan %model:grok-4.6 %effort:high

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

|              |                                                                                                                                                                                                                |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Outcome**  | COMPLETED — exit 0                                                                                                                                                                                             |
| **Started**  | 2026-10-28T21:21:01.844327+00:00                                                                                                                                                                               |
| **Finished** | 2026-10-28T21:25:07.064215Z                                                                                                                                                                                    |
| **Elapsed**  | 4m 3s of a 1h 0m 0s budget                                                                                                                                                                                     |
| **Output**   | 677 KiB · evidence refs: `file:monitor-diagnostic-manifest:qzr4a965ejvd`, `file:monitor-retained-log:qzr4a965ejvd` · raw output omitted: `facts_only` · full log: `sase monitor show qzr4a965ejvd --all-lines` |
| **Tool run** | sase tool show 17d66202a9f4df6d7dbb595d8eb77a25                                                                                                                                                                |

**Why this was monitored:** Verify before host completion

## Failure triage

verdict: pass

KNOWN 0; FLAKY 0

sase tool show 17d66202a9f4df6d7dbb595d8eb77a25 -j

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
