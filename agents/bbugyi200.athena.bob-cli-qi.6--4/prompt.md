%queue(weight=1)
#fork:bob-cli-qi.6--3
%model:gpt-6-luna@xhigh

%macros_enabled:false
# Monitored command finished

**Command:**

```text
xvfb-run -a npm run smoke:obsidian -- --report /tmp/qi6-obsidian-smoke.json
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/linked/bob-plugins
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-11-26T19:46:56.285373+00:00 |
| **Finished** | 2026-11-26T19:48:09.810229Z |
| **Elapsed** | 31s of a 30m 0s budget |
| **Output** | 686 bytes · evidence refs: `file:monitor-diagnostic-manifest:4qkh1bt7pyaa`, `file:monitor-retained-log:4qkh1bt7pyaa` · raw output omitted: `facts_only` · full log: `sase monitor show 4qkh1bt7pyaa --all-lines` |
| **Tool run** | sase tool show 46cdf9e5eb845167c5492003dd43cead |

**Why this was monitored:** Run qi.6 isolated Obsidian startup smoke before the clean deployment

## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-1d534e644c204f57.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "xvfb-run -a npm run smoke:obsidian -- --report /tmp/qi6-obsidian-smoke.json",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/linked/bob-plugins",
    "member_agent_name": "bob-cli-qi.6--mon-2",
    "monitor_id": "4qkh1bt7pyaa",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261126144236:8f7fcb81e61fa746"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:29a81d5edf94cff42d3581a093215729db0d3e1acc81d6e49e1be48c029885d3",
    "starter_agent": "bob-cli-qi.6--3",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/26/20261126144236"
  },
  "recorded_at_epoch": 1795722458.1080132,
  "schema_version": 1
}
```


## Your next action

Read the smoke result and report /tmp/qi6-obsidian-smoke.json. If it failed, fix only qi.6-introduced causes; record exact command, report path, and verdict on qi.6 for any unresolved failure. Then inspect bob plugins sync --repo "$PWD" --no-pull --dry-run from this repo. If sync refuses, follow docs/develop/deployment.md without -F: fetch, inspect git log --oneline HEAD..@{upstream} -- plugins/<id>, and check sase agent list; only proceed when the protected clean build is landed. Run bob plugins sync --repo "$PWD" --no-pull, then mandatory npm run smoke:obsidian -- --deployed-vault /home/bryan/bob --report /tmp/qi6-obsidian-smoke.json. Record exact command, report path, and verdict for any missing prerequisite or failed gate on qi.6. Confirm bob plugins list --format json --no-pull --repo "$PWD" reports drift=0. Before close, run sase bead epic-symbols bob-cli-qi.6 and resolve any leftovers; close only bob-cli-qi.6 with verified results, never parent. Use /sase_final.
%macros_enabled:true