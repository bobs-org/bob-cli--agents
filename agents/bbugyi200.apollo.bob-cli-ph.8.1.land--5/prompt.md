%queue(weight=1)
#fork:bob-cli-ph.8.1.land--4
%model:muse-spark-1.3-contributor@xhigh

%macros_enabled:false
# Monitored command finished

**Command:**

```text
git fetch origin master >/dev/null 2>&1; SHA=$(git rev-parse origin/master); RUN=""; i=0; while [ $i -lt 60 ]; do RUN=$(gh run list --repo bobs-org/bob-mac-capture --branch master --limit 5 --json databaseId,headSha --jq "[.[] | select(.headSha==\"$SHA\")][0].databaseId // empty"); if [ -n "$RUN" ]; then break; fi; i=$((i+1)); sleep 120; done; echo "SHA=$SHA RUN=$RUN"; gh run watch "$RUN" --repo bobs-org/bob-mac-capture --exit-status
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/linked/bob-mac-capture
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-11-26T11:39:52.670087+00:00 |
| **Finished** | 2026-11-26T12:07:51.740560Z |
| **Elapsed** | 23m 40s of a 2h 30m 0s budget |
| **Output** | 186 KiB · evidence refs: `file:monitor-diagnostic-manifest:xf549954ak0r`, `file:monitor-retained-log:xf549954ak0r` · raw output omitted: `facts_only` · full log: `sase monitor show xf549954ak0r --all-lines` |

**Why this was monitored:** Post-push exact-SHA macOS watch for bob-cli-ph.8.1 land commit

## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-1c997c22335bd5df.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "git fetch origin master >/dev/null 2>&1; SHA=$(git rev-parse origin/master); RUN=\"\"; i=0; while [ $i -lt 60 ]; do RUN=$(gh run list --repo bobs-org/bob-mac-capture --branch master --limit 5 --json databaseId,headSha --jq \"[.[] | select(.headSha==\\\"$SHA\\\")][0].databaseId // empty\"); if [ -n \"$RUN\" ]; then break; fi; i=$((i+1)); sleep 120; done; echo \"SHA=$SHA RUN=$RUN\"; gh run watch \"$RUN\" --repo bobs-org/bob-mac-capture --exit-status",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/linked/bob-mac-capture",
    "member_agent_name": "bob-cli-ph.8.1.land--mon-3",
    "monitor_id": "xf549954ak0r",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261126062740:ca854b144610f10d"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:65d4e22cc4ba237e71a669f48c85a2ad23fcfc6658cd9b20ad5a08b270e2ba26",
    "starter_agent": "bob-cli-ph.8.1.land--4",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/26/20261126062740"
  },
  "recorded_at_epoch": 1795693451.761488,
  "schema_version": 1
}
```


## Your next action

This is the post-push exact-SHA macOS watch for the bob-cli-ph.8.1 land (test-harness runloop yield in CaptureDrawerPipelineTests + plan status done). Read the outcome with sase monitor show --all-lines. If the master run is green, reply that the land is fully complete with the run URL and SHA. If red, fix the failures per plan:202611/land_mac_true_case_drawers.md and rerun Scripts/macos-ci-check.
%macros_enabled:true