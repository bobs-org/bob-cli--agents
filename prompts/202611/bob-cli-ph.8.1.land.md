- **AGENTS:**
  - [bbugyi200.apollo.bob-cli-ph.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.land.md)

%queue(weight=1) #fork:bob-cli-ph.8.1.land--3 %model:muse-spark-1.3-contributor@xhigh

%macros_enabled:false

# Monitored command finished

**Command:**

```text
Scripts/macos-ci-check
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/linked/bob-mac-capture
```

|              |                                                                                                                                                                                                               |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Outcome**  | COMPLETED — exit 0                                                                                                                                                                                            |
| **Started**  | 2026-11-26T10:55:58.168782+00:00                                                                                                                                                                              |
| **Finished** | 2026-11-26T11:27:16.349868Z                                                                                                                                                                                   |
| **Elapsed**  | 27m 6s of a 1h 0m 0s budget                                                                                                                                                                                   |
| **Output**   | 12 KiB · evidence refs: `file:monitor-diagnostic-manifest:804hgg50cqqf`, `file:monitor-retained-log:804hgg50cqqf` · raw output omitted: `facts_only` · full log: `sase monitor show 804hgg50cqqf --all-lines` |
| **Tool run** | sase tool show 46327e5629e88b0b223231f8dfb307db                                                                                                                                                               |

**Why this was monitored:** Land drawer tests: exact-SHA macOS gate retry for
bob-cli-ph.8.1 (undo runloop yield fix)

## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-cc8682ff43cc3dab.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "Scripts/macos-ci-check",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/linked/bob-mac-capture",
    "member_agent_name": "bob-cli-ph.8.1.land--mon-2",
    "monitor_id": "804hgg50cqqf",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261126054550:a186c74e56c77e92"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:03d1efe30cfdc3c62b09fd60e8fb76b92eee7b9632d435c566495292b4fc75a3",
    "starter_agent": "bob-cli-ph.8.1.land--3",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/26/20261126054550"
  },
  "recorded_at_epoch": 1795690809.5716803,
  "schema_version": 1
}
```

## Your next action

Read the gate result with sase monitor show. If red, fix the failing tests per
plan:202611/land_mac_true_case_drawers.md and rerun the gate. If green, continue the
land tale: reconcile docs (verify), download render-fixtures and inspect drawer-headers
PNGs, register them via sase artifact (read sase_artifacts memory first), attach refs to
bob-cli-ph.8.1.6 and bob-cli-ph.8, run sase bead epic-symbols on bob-cli-ph.8.1 and
bob-cli-ph.8 and resolve entries, close bob-cli-ph.8.1 with verification note (phases,
product vs test fixes, gate URL/SHA, screenshot refs, docs, no Rust/memory/vault
changes), run just symvision from bob-cli checkout, set status done in
plan:202611/finish_mac_true_case_drawers.md frontmatter, close bob-cli-ph.8 only (never
the parent epic), then stage the post-push exact-SHA watch with sase monitor and finish
through sase_final with commit decisions for bob-mac-capture and plans.
%macros_enabled:true
