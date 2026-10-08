%queue(weight=1)
%auto
#fork:0y4--1
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
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/chezmoi
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-10-08T11:38:27.079136+00:00 |
| **Finished** | 2026-10-08T11:39:37.826698+00:00 |
| **Elapsed** | 1m 10s of a 1h 0m 0s budget |
| **Output** | 47 KiB · evidence refs: `file:monitor-diagnostic-manifest:2z809pzy2k00`, `file:monitor-retained-log:2z809pzy2k00` · raw output omitted: `facts_only` · full log: `sase monitor show 2z809pzy2k00 --all-lines` |
| **Tool run** | sase tool show 2b2aaf8a30b1bcd0e032c10bd211f854 |

**Why this was monitored:** final verification for tmux extended-keys-format compat plan

## Your next action

Diagnose failures or stale verification, then finish the requested change.
%macros_enabled:true