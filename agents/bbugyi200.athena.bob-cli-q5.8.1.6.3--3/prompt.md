%queue(weight=1)
#fork:bob-cli-q5.8.1.6.3--2
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
| **Started** | 2026-11-27T05:49:28.833836+00:00 |
| **Finished** | 2026-11-27T06:18:01.947366Z |
| **Elapsed** | 26m 19s of a 1h 0m 0s budget |
| **Output** | 12 KiB · evidence refs: `file:monitor-diagnostic-manifest:jd80h23b9kc5`, `file:monitor-retained-log:jd80h23b9kc5` · raw output omitted: `facts_only` · full log: `sase monitor show jd80h23b9kc5 --all-lines` |
| **Tool run** | sase tool show 4e0f5a908aab5294064697979de28d19 |

**Why this was monitored:** macOS CI gate for hud-repair test fix (bob-confirmed day-boundary purge)

## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-3736724bc7204b22.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "Scripts/macos-ci-check",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-mac-capture",
    "member_agent_name": "bob-cli-q5.8.1.6.3--mon-1",
    "monitor_id": "jd80h23b9kc5",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261127004332:3df6e34f9825a1db"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:0bc18f7d4cc0e5b3058bcadddda34a2e5c10fd05a2ff8e5ed1691a6af6188b46",
    "starter_agent": "bob-cli-q5.8.1.6.3--2",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/27/20261127004332"
  },
  "recorded_at_epoch": 1795758702.4359045,
  "schema_version": 1
}
```


## Your next action

Read the full retained log with sase monitor show <id> --all-lines. If macOS CI is green (Lint, Build, Test all ok), record the run ID and artifact names on bead bob-cli-q5.8.1.6.3 with sase bead note, run sase bead epic-symbols bob-cli-q5.8.1.6.3, and close the bead with sase bead close only if it is still open (it may already be closed; never use a conflicting reason). If red, diagnose from the log, fix, and rerun Scripts/macos-ci-check. Do not close the parent epic.
%macros_enabled:true