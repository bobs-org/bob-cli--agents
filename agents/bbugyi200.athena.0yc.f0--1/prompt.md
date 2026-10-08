%queue(weight=1)
%auto
#fork:0yc.f0--code
%model:muse-spark-1.3-contributor
%effort:high

%macros_enabled:false
# Monitored command finished

**Command:**

```text
just check
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-10-08T17:00:21.948573+00:00 |
| **Finished** | 2026-10-08T17:03:04.799275+00:00 |
| **Elapsed** | 2m 41s of a 1h 0m 0s budget |
| **Output** | 355 KiB · evidence refs: `file:monitor-diagnostic-manifest:3bn1c91ahcvj`, `file:monitor-retained-log:3bn1c91ahcvj` · raw output omitted: `facts_only` · full log: `sase monitor show 3bn1c91ahcvj --all-lines` |
| **Tool run** | sase tool show 060cfd69cfdf8da7cb01523d7c495151 |

**Why this was monitored:** Verify before host completion

## Your next action

Diagnose failures or stale verification, then finish the requested change.
%macros_enabled:true