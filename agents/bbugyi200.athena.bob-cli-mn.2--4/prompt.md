%queue(weight=1)
#fork:bob-cli-mn.2--3
%model:@small

%macros_enabled:false
# Monitored command finished

**Command:**

```text
BASE=22a95b6425efd7eb560103d574adc3d7689035ac; REPO=bobs-org/bob-mac-capture; until SHA=$(git ls-remote origin refs/heads/master | awk "{print \$1}"); [ -n "$SHA" ] && [ "$SHA" != "$BASE" ]; do sleep 20; done; echo "landed SHA $SHA"; i=0; RID=; while [ "$i" -lt 30 ]; do RID=$(gh run list --repo "$REPO" --commit "$SHA" --json databaseId --jq ".[0].databaseId // empty"); [ -n "$RID" ] && break; i=$((i+1)); sleep 10; done; [ -n "$RID" ] || { echo "no run for $SHA"; exit 2; }; echo "watching run $RID"; gh run watch "$RID" --repo "$REPO" --exit-status
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-mac-capture
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-11-17T15:10:07.878631+00:00 |
| **Finished** | 2026-11-17T15:41:19.995574Z |
| **Elapsed** | 30m 4s of a 1h 30m 0s budget |
| **Output** | 221 KiB · evidence refs: `file:monitor-diagnostic-manifest:ackg1c372yjj`, `file:monitor-retained-log:ackg1c372yjj` · raw output omitted: `facts_only` · full log: `sase monitor show ackg1c372yjj --all-lines` |

**Why this was monitored:** Watch exact-SHA macOS CI after the separator follow-up tip wait lands on bob-mac-capture master

## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-4dd924f55b7f99f3.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "BASE=22a95b6425efd7eb560103d574adc3d7689035ac; REPO=bobs-org/bob-mac-capture; until SHA=$(git ls-remote origin refs/heads/master | awk \"{print \\$1}\"); [ -n \"$SHA\" ] && [ \"$SHA\" != \"$BASE\" ]; do sleep 20; done; echo \"landed SHA $SHA\"; i=0; RID=; while [ \"$i\" -lt 30 ]; do RID=$(gh run list --repo \"$REPO\" --commit \"$SHA\" --json databaseId --jq \".[0].databaseId // empty\"); [ -n \"$RID\" ] && break; i=$((i+1)); sleep 10; done; [ -n \"$RID\" ] || { echo \"no run for $SHA\"; exit 2; }; echo \"watching run $RID\"; gh run watch \"$RID\" --repo \"$REPO\" --exit-status",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-mac-capture",
    "member_agent_name": "bob-cli-mn.2--mon-2",
    "monitor_id": "ackg1c372yjj",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261117095542:1a4270821a260d1d"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:ff1a0fe82f6b6acc002e62f54a4a7be916c88c0dddfd00942cfd6a3077345c39",
    "starter_agent": "bob-cli-mn.2--3",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/17/20261117095542"
  },
  "recorded_at_epoch": 1794928275.4611316,
  "schema_version": 1
}
```


## Your next action

If the macOS CI run failed, diagnose and fix the bob-cli-mn.2 landing in bob-mac-capture. If it passed, the phase is done; do not close parent epic bob-cli-mn.
%macros_enabled:true