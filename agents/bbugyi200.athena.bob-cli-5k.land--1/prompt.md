%queue(weight=1)
%auto
#fork:bob-cli-5k.land--code
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
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-10-08T02:14:47.645398+00:00 |
| **Finished** | 2026-10-08T02:15:45.544173+00:00 |
| **Elapsed** | 56s of a 1h 0m 0s budget |
| **Output** | 345 KiB · evidence refs: `file:monitor-diagnostic-manifest:vjy08adq6h9a`, `file:monitor-retained-log:vjy08adq6h9a` · raw output omitted: `facts_only` · full log: `sase monitor show vjy08adq6h9a --all-lines` |
| **Tool run** | sase tool show eccc9ff84fbf18f793310f4088780cce |

**Why this was monitored:** Verify before host completion

## Your next action

Diagnose failures or stale verification, then finish the requested change.
%macros_enabled:true