%queue(weight=1)
#fork:bob-cli-q5.8.1.4--6
%model:gpt-6-luna@xhigh

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
| **Started** | 2026-11-26T23:46:58.548317+00:00 |
| **Finished** | 2026-11-27T00:14:19.593786Z |
| **Elapsed** | 26m 49s of a 1h 30m 0s budget |
| **Output** | 12 KiB · evidence refs: `file:monitor-diagnostic-manifest:m34fem1rk35x`, `file:monitor-retained-log:m34fem1rk35x` · raw output omitted: `facts_only` · full log: `sase monitor show m34fem1rk35x --all-lines` |
| **Tool run** | sase tool show 9e564033e65594e04d376aeeae72f2d7 |

**Why this was monitored:** Verify the snooze wake HUD fix on exact-SHA macOS CI

## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-857cdd579ae5496d.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "Scripts/macos-ci-check",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-mac-capture",
    "member_agent_name": "bob-cli-q5.8.1.4--mon-5",
    "monitor_id": "m34fem1rk35x",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261126184302:24b8645e551d8a04"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:f9b43b75b4c12523d24c05e9e96cc613b7d3a170d60eaa9a49a73da9625d56dc",
    "starter_agent": "bob-cli-q5.8.1.4--6",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/26/20261126184302"
  },
  "recorded_at_epoch": 1795736850.7452254,
  "schema_version": 1
}
```


## Your next action

Inspect the exact-SHA result. If green, run `sase bead epic-symbols bob-cli-q5.8.1.4`, resolve or re-key remaining symbols, then close only `bob-cli-q5.8.1.4` with a concise verified note; keep its parent epic open. If CI fails because of this phase, diagnose and fix it, rerun the Mac scratch compile (format lint, bundle build, and test typecheck), then rerun this exact-SHA gate with a 90-minute verify monitor and continue until green. Keep the phase bead open while any verification or phase-scope work remains.
%macros_enabled:true