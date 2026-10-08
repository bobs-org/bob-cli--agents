%queue(weight=1)
%auto
#fork:0y9--code
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
| **Started** | 2026-10-08T14:17:15.155226+00:00 |
| **Finished** | 2026-10-08T14:19:11.530415+00:00 |
| **Elapsed** | 1m 54s of a 1h 0m 0s budget |
| **Output** | 346 KiB · evidence refs: `file:monitor-diagnostic-manifest:1mqje91dr1fz`, `file:monitor-retained-log:1mqje91dr1fz` · raw output omitted: `facts_only` · full log: `sase monitor show 1mqje91dr1fz --all-lines` |
| **Tool run** | sase tool show b622222144d2340c4917bfacb3e258fc |

**Why this was monitored:** Verify before host completion

## Your next action

Diagnose failures or stale verification, then finish the requested change.
%macros_enabled:true