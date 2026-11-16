%queue(weight=1)
#fork:bob-cli-mb.3--1
%model:muse-spark-1.3-contributor@xhigh

%macros_enabled:false
# Monitored command finished

**Command:**

```text
gh run watch 43899389310 -R bobs-org/bob-mac-capture --exit-status
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/sase/repos/linked/bob-mac-capture
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-11-16T16:14:06.399601+00:00 |
| **Finished** | 2026-11-16T16:38:23.200946Z |
| **Elapsed** | 22m 25s of a 1h 30m 0s budget |
| **Output** | 177 KiB · evidence refs: `file:monitor-diagnostic-manifest:v0wyackf94sd`, `file:monitor-retained-log:v0wyackf94sd` · raw output omitted: `facts_only` · full log: `sase monitor show v0wyackf94sd --all-lines` |

**Why this was monitored:** Watch exact-SHA master CI rerun for bob-cli-mb.3 Recent group to green

## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-3921632128c4ca4c.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "gh run watch 43899389310 -R bobs-org/bob-mac-capture --exit-status",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/sase/repos/linked/bob-mac-capture",
    "member_agent_name": "bob-cli-mb.3--mon-0",
    "monitor_id": "v0wyackf94sd",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261116111014:bdac21046ff78d2c"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:ead6c9db20f73bb91101657edf3e507505d188717be77d836452b938c1c7f049",
    "starter_agent": "bob-cli-mb.3--1",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/16/20261116111014"
  },
  "recorded_at_epoch": 1794845758.2100146,
  "schema_version": 1
}
```


## Your next action

Exact-SHA master CI rerun (run 43899389310, SHA 61d29a6f3c1978ca78067e235ce98938344d8bf1) for bead bob-cli-mb.3 should now be finished. Check it with: gh run view 43899389310 -R bobs-org/bob-mac-capture --json status,conclusion. If conclusion is success: run sase bead note bob-cli-mb.3 with the SHA and run URL https://github.com/bobs-org/bob-mac-capture/actions/runs/43899389310, then sase bead epic-symbols bob-cli-mb.3 (must be empty), then sase bead close bob-cli-mb.3 --note with what was verified (portable-check 2537 tests 0 failures, docs-check 447 passed, macos-ci-check exit 0, exact-SHA master CI green on rerun; note the first attempt hit one flaky timing failure in CaptureDotRouteAliasTests testFastDoubleDotBeforeReplyCollapsesToOne, unrelated to the Recent-group diff). If the rerun failed again, inspect with gh run view --log-failed, fix forward in sase/repos/linked/bob-mac-capture, and rerun. Never close the parent epic.
%macros_enabled:true