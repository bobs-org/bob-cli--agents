%queue(weight=1)
%auto
#fork:bob-cli-5k.5--plan
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
| **Started** | 2026-10-07T20:39:17.042443+00:00 |
| **Finished** | 2026-10-07T20:40:52.486182+00:00 |
| **Elapsed** | 1m 34s of a 1h 0m 0s budget |
| **Output** | 338 KiB · evidence refs: `file:monitor-diagnostic-manifest:hntqd893rxw0`, `file:monitor-retained-log:hntqd893rxw0` · raw output omitted: `facts_only` · full log: `sase monitor show hntqd893rxw0 --all-lines` |
| **Tool run** | sase tool show bdefdae86cf22fa5498d558eef3c5792 |

**Why this was monitored:** Verify before host completion

## Your next action

Diagnose failures or stale verification, then finish the requested change.
%macros_enabled:true