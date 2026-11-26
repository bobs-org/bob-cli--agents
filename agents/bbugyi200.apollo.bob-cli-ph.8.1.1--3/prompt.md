%queue(weight=1)
#fork:bob-cli-ph.8.1.1--2
%model:gpt-6-luna@high

%macros_enabled:false
# Monitored command finished

**Command:**

```text
Scripts/macos-ci-check
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-mac-capture
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-11-26T03:03:45.450467+00:00 |
| **Finished** | 2026-11-26T03:31:28.356874Z |
| **Elapsed** | 25m 17s of a 2h 0m 0s budget |
| **Output** | 11 KiB · evidence refs: `file:monitor-diagnostic-manifest:2yaj85csysw1`, `file:monitor-retained-log:2yaj85csysw1` · raw output omitted: `facts_only` · full log: `sase monitor show 2yaj85csysw1 --all-lines` |

**Why this was monitored:** Rerun exact-SHA macOS CI after correcting the final fixture expectations

## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-3ae2a872854a7ec1.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "Scripts/macos-ci-check",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-mac-capture",
    "member_agent_name": "bob-cli-ph.8.1.1--mon-1",
    "monitor_id": "2yaj85csysw1",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261125215755:e3ae123c53427a88"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:07a56f398a65730d4d0de9520e1fad8968a7bf485b46061219d88ba225185849",
    "starter_agent": "bob-cli-ph.8.1.1--2",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/25/20261125215755"
  },
  "recorded_at_epoch": 1795662371.1167207,
  "schema_version": 1
}
```


## Your next action

Inspect the exact-SHA result. If green, check portable verification availability, run sase bead epic-symbols bob-cli-ph.8.1.1, resolve any symbols, then close only bob-cli-ph.8.1.1 with verified results. If red, inspect exact failure details, fix, and rerun. Never set bead status by hand.
%macros_enabled:true