%queue(weight=1)
#fork:bob-cli-ly.3--4
%model:gpt-6-luna@xhigh

%macros_enabled:false
# Monitored command finished

**Command:**

```text
git rev-parse HEAD
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-mac-capture
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-11-16T00:20:41.806469+00:00 |
| **Finished** | 2026-11-16T00:22:10.260090Z |
| **Elapsed** | 0.248s of a 10m 0s budget |
| **Output** | 108 bytes · evidence refs: `file:monitor-diagnostic-manifest:8w2q405gc0kp`, `file:monitor-retained-log:8w2q405gc0kp` · raw output omitted: `facts_only` · full log: `sase monitor show 8w2q405gc0kp --all-lines` |

**Why this was monitored:** Read the landed bob-mac-capture commit after host finalization

## Your next action

Report the landed commit SHA from the command output, alongside the successful exact-snapshot CI URL and closed bob-cli-ly.3 status.
%macros_enabled:true