# Agent: bob-cli-ms.8.3.1.2--d

[Agent Hoods](../../README.md) / [bbugyi200](../../users/bbugyi200/README.md) / [apollo](../../users/bbugyi200/machines/apollo/README.md) / [bob-cli-ms](../../users/bbugyi200/machines/apollo/hoods/bob-cli-ms/README.md) / [bob-cli-ms.8.3.1.2](../../sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.2.md) / bob-cli-ms.8.3.1.2--d

**Global name:** `bbugyi200.apollo.bob-cli-ms.8.3.1.2--d` · **State:** completed · **Source run:** `run-ebb64a905edd24c33d50396492387375`

**Owner:** `bbugyi200.apollo` · **Project:** bob-cli · **Hood:** bob-cli-ms

## Summary

- Bead: [bob-cli-ms.8.3.1.2](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ms/bob-cli-ms.8.3.1.2.md)
- Model: gpt-6-astra
- Provider: codex
- Timing: 2026-11-19T05:30:28.261978+00:00 → 2026-11-19T05:39:31.229955+00:00
- Commits: 0
- Variables: [1](#variables)

## Files

[Chat](chat.md) · [Prompt](prompt.md)

## Variables

| Variable | Value |
|---|---|
| `artifacts` | \[{kind: file, label: Record Card run12 full evidence and Cargo isolation repair, path: /home/bryan/.sase/artifacts/agents/gh\_bobs-org\_\_bob-cli/20261119002945/twelfth-evidence.tar-bfc52f92c04f.gz, ref… |

#### artifacts

```yaml
- kind: file
  label: Record Card run12 full evidence and Cargo isolation repair
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261119002945/twelfth-evidence.tar-bfc52f92c04f.gz
  ref: file:explicit:58417e2218334d940ee2b4b3
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/twelfth-evidence.tar.gz
- kind: file
  label: Record Card run12 raw summary
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261119002945/summary-74ddb04db7a6.json
  ref: file:explicit:48f3d0ee1ffbd155cd39106e
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/run-20261119-044338/summary.json
- kind: file
  label: Record Card run12 identical 12 tick failure signatures
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261119002945/cli-failure-comparison-9cfad87ca65a.json
  ref: file:explicit:82b63063f3a7f2b618b7ef1a
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/run-20261119-044338/cli-failure-comparison.json
- kind: file
  label: Record Card run12 Cargo isolation repair summary
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261119002945/repair-summary-e87eae8b7d36.json
  ref: file:explicit:ce98fc7f4a450cc0b5adc8fe
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/run-20261119-044338/repair-summary.json
- kind: file
  label: Record Card real Cargo isolation regression
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261119002945/cargo-isolation-regression-82f75310c2c8.log
  ref: file:explicit:ff498b794e822c243eca8ec5
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/run-20261119-044338/cargo-isolation-regression.log
- kind: file
  label: Record Card run12 complete evidence index
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261119002945/twelfth-complete-evidence-index-257094f1c250.json
  ref: file:explicit:020c13291f70e570bac10cc7
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/twelfth-complete-evidence-index.json
```

Values are truncated for display; see [meta.json](meta.json) for the full values.

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-ms.8.3](../../sessions/bbugyi200.apollo.bob-cli-ms.8.3.md) (session · 3) | ancestor | active 1, completed 2 |
| [bob-cli-ms.8.3.1.1](../../sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.1.md) (session · 25) | bob-cli-ms.8.3.1 hood | active 1, completed 12, failed 12 |
| [bob-cli-ms.8.3.1.3](../../sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.3.md) (session · 7) | bob-cli-ms.8.3.1 hood | completed 5, failed 2 |
| [bob-cli-ms.8.3.1.land](../bbugyi200.apollo.bob-cli-ms.8.3.1.land/README.md) | bob-cli-ms.8.3.1 hood | waiting |
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
| [bob-cli-ms.land](../../sessions/bbugyi200.apollo.bob-cli-ms.land.md) (session · 3) | bob-cli-ms hood | active 1, completed 2 |
| [bob-cli-ms.land](../bbugyi200.apollo.bob-cli-ms.land/README.md) | bob-cli-ms hood | completed |
