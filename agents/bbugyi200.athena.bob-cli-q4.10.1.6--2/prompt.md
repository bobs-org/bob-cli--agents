%queue(weight=1)
#fork:bob-cli-q4.10.1.6--1
%model:gpt-6-astra@xhigh

%macros_enabled:false
# Monitored command finished

**Command:**

```text
python3 .git/nav-acceptance-deploy.py
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-11-26T09:10:46.461792+00:00 |
| **Finished** | 2026-11-26T09:25:00.953623Z |
| **Elapsed** | 1m 46s of a 20m 0s budget |
| **Output** | 20 KiB · evidence refs: `file:monitor-diagnostic-manifest:waj617neh6gj`, `file:monitor-retained-log:waj617neh6gj` · raw output omitted: `facts_only` · full log: `sase monitor show waj617neh6gj --all-lines` |
| **Tool run** | sase tool show d30aa131e3470cb5ac97fa46998e45aa |

**Why this was monitored:** Finish navigation-only deployment with isolated source and actual-deployed Obsidian smoke evidence

## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-7a51c476c477e474.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "python3 .git/nav-acceptance-deploy.py",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15",
    "member_agent_name": "bob-cli-q4.10.1.6--mon-0",
    "monitor_id": "waj617neh6gj",
    "next_output": "auto",
    "parent_node_ids": [
      "agent-delta:20261126035939:ee77325b2bd3afd5"
    ],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:6a628ab8829d6b665fbae0d84cc9bdb031835f204328be6d968f19c97196c8c9",
    "starter_agent": "bob-cli-q4.10.1.6--1",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202611/26/20261126035939"
  },
  "recorded_at_epoch": 1795684994.471223,
  "schema_version": 1
}
```


## Your next action

Complete bob-cli-q4.10.1.6. Read .git/nav-acceptance-verification/deployment-summary.json and navigation-deployment-evidence.json plus each smoke report/log. The script builds/checks, runs source isolation, syncs ONLY bob-navigation-hotkeys, verifies version 2.107.11 and SHA256 managed-file equality, runs the unchanged full-vault post-sync gate, and tests a snapshot of the actual deployed managed plugin combination in isolated Obsidian. The source full-vault gate is EXPECTED to fail only for block-id-prompt, bob-ledger-tools and task-status-cycler drift: this exact refusal was reproduced on clean e82bd932 and recorded on the bead and file:explicit:161491026097b312bac5b238. Do not deploy those other plugins or weaken the gate. A successful snapshot check is supplementary actual-deployed compatibility evidence, not a claim that the source gate passed. All implementation/tests/docs are done. Explicit /sase_final commit declaration was submitted before this monitor so the plugin source should now be committed. The earlier full npm run had 9833 pass, 2 clean-base date failures, 4 skips; CLI ToolRun e13343e2c3964b239f50decd35db85a9 finished with 98 failures on clean 1c23bce7 before/after, no escalation. All those failures are already recorded as PROPOSED FOLLOW-UP on this phase; do not rerun full gates or rebuild CLI merely for the known failures. Both docs gates and real Obsidian nav lane/annotated-dependency one-step Undo passed; detailed inventory and counts are already on the phase. If this monitor has new failures, fix or reproduce on the clean base; follow protected-sync recovery without force if needed. Once source smoke and actual-deployed snapshot smoke pass and nav version/hashes match, record final source SHA, deployment stamp/hash and reports as an artifact and bead note, retaining the full-vault gate limitation. Run sase bead epic-symbols bob-cli-q4.10.1.6 and close ONLY this phase with verified evidence. No ancestor closure, no task beads. End through /sase_final; declare commit for any repositories changed in recovery. Remaining work is final evidence and closure; no child epic needed.
%macros_enabled:true