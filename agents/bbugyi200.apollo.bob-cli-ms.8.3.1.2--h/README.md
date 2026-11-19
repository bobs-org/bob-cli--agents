# Agent: bob-cli-ms.8.3.1.2--h

[Agent Hoods](../../README.md) / [bbugyi200](../../users/bbugyi200/README.md) / [apollo](../../users/bbugyi200/machines/apollo/README.md) / [bob-cli-ms](../../users/bbugyi200/machines/apollo/hoods/bob-cli-ms/README.md) / [bob-cli-ms.8.3.1.2](../../sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.2.md) / bob-cli-ms.8.3.1.2--h

**Global name:** `bbugyi200.apollo.bob-cli-ms.8.3.1.2--h` · **State:** completed · **Source run:** `run-cc193c26ae45ee8c057ef6b9918ef426`

**Owner:** `bbugyi200.apollo` · **Project:** bob-cli · **Hood:** bob-cli-ms

## Summary

- Bead: [bob-cli-ms.8.3.1.2](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ms/bob-cli-ms.8.3.1.2.md)
- Model: gpt-6-astra
- Provider: codex
- Timing: 2026-11-19T08:54:50.568211+00:00 → 2026-11-19T09:11:42.941792+00:00
- Commits: [1](#commits)
- Variables: [1](#variables)

## Files

[Chat](chat.md) · [Prompt](prompt.md)

## Commits

| Repo | Commit | Subject | Committed |
|---|---|---|---|
| — | `e07a26b` | fix(records): preserve literal YAML values in reads and undo | 2026-11-19 04:10:03 EST |

## Variables

| Variable | Value |
|---|---|
| `artifacts` | \[{bead: bob-cli-ms.8.3.1.2, kind: file, label: Record Card run16 complete accepted proof and deployment (115 files), path: /home/bryan/.sase/artifacts/agents/gh\_bobs-org\_\_bob-cli/20261119035409/run16… |

#### artifacts

```yaml
- bead: bob-cli-ms.8.3.1.2
  kind: file
  label: Record Card run16 complete accepted proof and deployment (115 files)
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261119035409/run16-complete-evidence.tar-6896bb7a6664.gz
  ref: file:explicit:5ed730e7dc7e25751c173f79
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/run16-complete-evidence.tar.gz
- bead: bob-cli-ms.8.3.1.2
  kind: file
  label: Record Card run16 final acceptance index, hashes and deployment verdict
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261119035409/run16-evidence-index-306d98704f54.json
  ref: file:explicit:c7152b287d5c14283393fafe
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/run16-evidence-index.json
```

Values are truncated for display; see [meta.json](meta.json) for the full values.

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-ms.8.3](../../sessions/bbugyi200.apollo.bob-cli-ms.8.3.md) (session · 3) | ancestor | active 1, completed 2 |
| [bob-cli-ms.8.3.1.1](../../sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.1.md) (session · 25) | bob-cli-ms.8.3.1 hood | active 1, completed 12, failed 12 |
| [bob-cli-ms.8.3.1.3](../../sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.3.md) (session · 7) | bob-cli-ms.8.3.1 hood | completed 5, failed 2 |
| [bob-cli-ms.8.3.1.land](../../sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.land.md) (session · 3) | bob-cli-ms.8.3.1 hood | completed 3 |
| [bob-cli-ms.8.1](../../sessions/bbugyi200.apollo.bob-cli-ms.8.1.md) (session · 5) | bob-cli-ms.8 hood | completed 4, failed 1 |
| [bob-cli-ms.8.2](../bbugyi200.apollo.bob-cli-ms.8.2/README.md) | bob-cli-ms.8 hood | completed |
| [bob-cli-ms.8.land](../bbugyi200.apollo.bob-cli-ms.8.land/README.md) | bob-cli-ms.8 hood | waiting |
| [bob-cli-ms.1](../../sessions/bbugyi200.apollo.bob-cli-ms.1.md) (session · 7) | bob-cli-ms hood | completed 5, failed 2 |
| [bob-cli-ms.2](../bbugyi200.apollo.bob-cli-ms.2/README.md) | bob-cli-ms hood | completed |
| [bob-cli-ms.3](../../sessions/bbugyi200.apollo.bob-cli-ms.3.md) (session · 5) | bob-cli-ms hood | completed 5 |
| [bob-cli-ms.4](../bbugyi200.apollo.bob-cli-ms.4/README.md) | bob-cli-ms hood | completed |
| [bob-cli-ms.5](../../sessions/bbugyi200.apollo.bob-cli-ms.5.md) (session · 5) | bob-cli-ms hood | completed 5 |
| [bob-cli-ms.6](../../sessions/bbugyi200.apollo.bob-cli-ms.6.md) (session · 5) | bob-cli-ms hood | completed 4, failed 1 |
| [bob-cli-ms.6](../bbugyi200.apollo.bob-cli-ms.6/README.md) | bob-cli-ms hood | completed |
| [bob-cli-ms.7](../bbugyi200.apollo.bob-cli-ms.7/README.md) | bob-cli-ms hood | completed |
| [bob-cli-ms.land](../../sessions/bbugyi200.apollo.bob-cli-ms.land.md) (session · 3) | bob-cli-ms hood | completed 2, dismissed 1 |
| [bob-cli-ms.land](../bbugyi200.apollo.bob-cli-ms.land/README.md) | bob-cli-ms hood | completed |
