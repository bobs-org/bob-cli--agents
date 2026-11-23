%queue(weight=1)
#fork:bob-cli-on.15.1.4--1
%model:muse-spark-1.3-contributor@xhigh

%macros_enabled:false
# Monitored command finished

**Command:**

```text
Scripts/macos-ci-check
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-mac-capture
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-11-22T23:45:19.813380+00:00 |
| **Finished** | 2026-11-23T00:11:19.019384Z |
| **Elapsed** | 22m 8s of a 1h 30m 0s budget |
| **Output** | 10 KiB · evidence refs: `file:monitor-diagnostic-manifest:kx5dzsp1dpxh`, `file:monitor-retained-log:kx5dzsp1dpxh` · raw output omitted: `facts_only` · full log: `sase monitor show kx5dzsp1dpxh --all-lines` |
| **Tool run** | sase tool show 2e244b23dfb3adaa9ea3ef09645ab6e6 |

**Why this was monitored:** Re-run macOS CI after fixing requirement scope test expectation for bead bob-cli-on.15.1.4

## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-186b6361b71cc507.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "Scripts/macos-ci-check",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-mac-capture",
    "member_agent_name": "bob-cli-on.15.1.4--mon-0",
    "monitor_id": "kx5dzsp1dpxh",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261122184204:837c0f9c7ec60200"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:3e55bb08e6b1aa130c5a91f0e0745cefb5ae70194de9eb00dd2e029d69094400",
    "starter_agent": "bob-cli-on.15.1.4--1",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/22/20261122184204"
  },
  "recorded_at_epoch": 1795391351.0982733,
  "schema_version": 1
}
```


## Your next action

If macOS CI is green, run sase bead epic-symbols bob-cli-on.15.1.4, record passing portable, scratch typecheck, and exact-SHA macOS CI evidence plus fixture provenance and doc gates on the bead via sase bead note, then close bob-cli-on.15.1.4 with sase bead close. If red, fix the failure or record PROPOSED FOLLOW-UP if it reproduces on clean base, and do not close on a real regression.
%macros_enabled:true