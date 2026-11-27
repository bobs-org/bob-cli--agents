#fork:bob-cli-qj.4
%model:opus
%effort:xhigh

%macros_enabled:false
# Gate answered

**Decision:** Sync Bob Prose plugins on athena and the Mac (bob-cli-qj.4 host gate)

| | |
| --- | --- |
| **Outcome** | ANSWERED — Sync on athena, Sync on the Mac |
| **Answered via** | tui |
| **Opened** | 2026-11-27T11:36:22Z |
| **Answered** | 2026-11-27T11:36:56Z |
| **Commands** | 2 of 2 completed |
| **Gate** | custom/custom-6e7c1a95-e9fb-4d69-8944-c61cd0c26276 |

## Results

### athena — `commands/sync_athena`

```json
{
  "head": "c41e07e9 feat(prose): Bob Prose in Obsidian with canonical bob prose calls",
  "host": "athena",
  "plugins": [
    {
      "deployed_has_marker": true,
      "detail": "ok bob-articles  copied main.js   +84 -31 2 copied - 0 skipped - 1 unchanged - backups in /home/bryan/.local/state/bob-cli/plugin-backups/20261127-063652",
      "exit": 0,
      "id": "bob-articles",
      "source_has_marker": true
    },
    {
      "deployed_has_marker": true,
      "detail": "ok bob-command-mode  copied main.js   +19 -12 2 copied - 0 skipped - 1 unchanged - backups in /home/bryan/.local/state/bob-cli/plugin-backups/20261127-063652-1",
      "exit": 0,
      "id": "bob-command-mode",
      "source_has_marker": true
    },
    {
      "deployed_has_marker": true,
      "detail": "ok bob-navigation-hotkeys  copied main.js   +2 -0 2 copied - 0 skipped - 1 unchanged - backups in /home/bryan/.local/state/bob-cli/plugin-backups/20261127-063652-2",
      "exit": 0,
      "id": "bob-navigation-hotkeys",
      "source_has_marker": true
    },
    {
      "deployed_has_marker": true,
      "detail": "ok bob-ledger-tools  copied main.js   +2 -0 2 copied - 0 skipped - 1 unchanged - backups in /home/bryan/.local/state/bob-cli/plugin-backups/20261127-063652-3",
      "exit": 0,
      "id": "bob-ledger-tools",
      "source_has_marker": true
    }
  ],
  "pull": "26 files changed, 452 insertions(+), 155 deletions(-)",
  "status": "synced"
}
```

### mac — `commands/sync_mac`

```json
{
  "head": "c41e07e9 feat(prose): Bob Prose in Obsidian with canonical bob prose calls",
  "host": "mac",
  "plugins": [
    {
      "deployed_has_marker": true,
      "detail": "ok bob-articles  copied main.js   +84 -31 2 copied - 0 skipped - 1 unchanged - backups in /Users/bbugyi/.local/state/bob-cli/plugin-backups/20261127-063654",
      "exit": 0,
      "id": "bob-articles",
      "source_has_marker": true
    },
    {
      "deployed_has_marker": true,
      "detail": "ok bob-command-mode  copied main.js   +19 -12 2 copied - 0 skipped - 1 unchanged - backups in /Users/bbugyi/.local/state/bob-cli/plugin-backups/20261127-063654-1",
      "exit": 0,
      "id": "bob-command-mode",
      "source_has_marker": true
    },
    {
      "deployed_has_marker": true,
      "detail": "ok bob-navigation-hotkeys  copied main.js   +2 -0 2 copied - 0 skipped - 1 unchanged - backups in /Users/bbugyi/.local/state/bob-cli/plugin-backups/20261127-063655",
      "exit": 0,
      "id": "bob-navigation-hotkeys",
      "source_has_marker": true
    },
    {
      "deployed_has_marker": true,
      "detail": "ok bob-ledger-tools  copied main.js   +2 -0 2 copied - 0 skipped - 1 unchanged - backups in /Users/bbugyi/.local/state/bob-cli/plugin-backups/20261127-063655-1",
      "exit": 0,
      "id": "bob-ledger-tools",
      "source_has_marker": true
    }
  ],
  "pull": "25 files changed, 430 insertions(+), 134 deletions(-)",
  "status": "synced"
}
```

## Your next action

Continue bead bob-cli-qj.4, the prose-vault phase of epic bob-cli-qj (plan plan:202611/prose_note_type.md; read the bead and plan again with `sase bead read bob-cli-qj.4 -r ...`). The fenced results above are each host's `bob plugins sync` outcome for bob-articles, bob-command-mode, bob-navigation-hotkeys, and bob-ledger-tools.
1. Open bob-plugins with `sase repo open bob-plugins`, run `git fetch`, and confirm the re-landed Bob Prose commit (marker bob-prose-type-v1, spawn argv ["prose", ...]) is on origin/master. If it is missing, re-land that work before anything else.
2. Rerun the gate: `scripts/dev/bob-host-currency --probe prose-type-read --plugin bob-articles=bob-prose-type-v1 --plugin bob-command-mode=bob-prose-type-v1 --plugin bob-navigation-hotkeys=bob-prose-type-v1 --plugin bob-ledger-tools=bob-prose-type-v1`. If a host still lacks a marker because `bob plugins sync` refused another checkout's deploy, follow the refusal rules in bob-plugins AGENTS.md: never pass -F on your own, wait with /sase_monitor while the named build's author is still running (36 h total bound), and propose any further remote sync through /sase_gate.
3. Once every row passes, store the passing table as a SASE artifact (/sase_artifact). Then do plan step 1, the vault cutover in ~/bob: follow the vault AGENTS.md, inspect git status first, and stage and commit only your files with git add/git commit. Run its verify bullets.
4. Plan steps 2 and 3 are already done. bob-plugins calls `bob prose`, and both memory strands landed in bob-cli 4168e201. Change no other memory.
5. Run `sase bead epic-symbols bob-cli-qj.4`. Then close only bob-cli-qj.4 with `sase bead close bob-cli-qj.4 --note "<what you verified>"`. Never close the parent epic.
%macros_enabled:true