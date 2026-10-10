%queue(weight=1)
#fork:bob-cli-5y.10--1
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
| **Started** | 2026-10-10T01:01:23.639218+00:00 |
| **Finished** | 2026-10-10T01:02:07.066510+00:00 |
| **Elapsed** | 42s of a 1h 0m 0s budget |
| **Output** | 407 KiB · evidence refs: `file:monitor-diagnostic-manifest:7aj3ee6y3nnq`, `file:monitor-retained-log:7aj3ee6y3nnq` · raw output omitted: `facts_only` · full log: `sase monitor show 7aj3ee6y3nnq --all-lines` |
| **Tool run** | sase tool show bca754ff0868386b2fa4e76a8dc27fc8 |

**Why this was monitored:** Verify before host completion

## Your next action

Diagnose failures or stale verification, then finish the requested change.
%macros_enabled:true