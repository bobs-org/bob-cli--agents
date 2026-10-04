%queue(weight=1)
%auto
#fork:0vg--code
%model:muse-spark-1.3-contributor
%effort:xhigh

%xprompts_enabled:false
# Monitored command finished

**Command:**

```text
just check
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/chezmoi
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-10-02T17:36:33.248729+00:00 |
| **Finished** | 2026-10-02T17:37:35.520520+00:00 |
| **Elapsed** | 1m 1s of a 1h 0m 0s budget |
| **Output** | 42 KiB · evidence refs: `file:monitor-diagnostic-manifest:gq70b6krr0j4`, `file:monitor-retained-log:gq70b6krr0j4` · raw output omitted: `facts_only` · full log: `sase monitor show gq70b6krr0j4 --all-lines` |
| **Tool run** | sase tool show ebaa8bf37fbc3894acdbe88222823d8d |

**Why this was monitored:** run command

## Your next action

Diagnose failures or stale verification, then finish the requested change.
%xprompts_enabled:true