%queue(weight=1)
#fork:bob-cli-5s.10.land--code
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
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-10-09T16:09:16.861296+00:00 |
| **Finished** | 2026-10-09T16:11:59.695986+00:00 |
| **Elapsed** | 2m 41s of a 1h 0m 0s budget |
| **Output** | 356 KiB · evidence refs: `file:monitor-diagnostic-manifest:7q8zn06n6e2h`, `file:monitor-retained-log:7q8zn06n6e2h` · raw output omitted: `facts_only` · full log: `sase monitor show 7q8zn06n6e2h --all-lines` |
| **Tool run** | sase tool show f52ce09e9d31e7c5c26ff7fd54270f09 |

**Why this was monitored:** Verify before host completion

## Your next action

Diagnose failures or stale verification, then finish the requested change.
%macros_enabled:true