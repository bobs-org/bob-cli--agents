# Agent: bob-cli-ms.8.3.1.2--c

[Agent Hoods](../../README.md) / [bbugyi200](../../users/bbugyi200/README.md) / [apollo](../../users/bbugyi200/machines/apollo/README.md) / [bob-cli-ms](../../users/bbugyi200/machines/apollo/hoods/bob-cli-ms/README.md) / [bob-cli-ms.8.3.1.2](../../sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.2.md) / bob-cli-ms.8.3.1.2--c

**Global name:** `bbugyi200.apollo.bob-cli-ms.8.3.1.2--c` · **State:** completed · **Source run:** `run-92b5e1369b3e939d626919ef34da1c67`

**Owner:** `bbugyi200.apollo` · **Project:** bob-cli · **Hood:** bob-cli-ms

## Summary

- Bead: [bob-cli-ms.8.3.1.2](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ms/bob-cli-ms.8.3.1.2.md)
- Model: gpt-6-astra
- Provider: codex
- Timing: 2026-11-19T04:32:25.973173+00:00 → 2026-11-19T04:43:39.197016+00:00
- Commits: 0
- Variables: [1](#variables)

## Files

[Chat](chat.md) · [Prompt](prompt.md)

## Variables

| Variable | Value |
|---|---|
| `artifacts` | \[{kind: file, label: Record Card run 11 complete logs and provenance repair, path: /home/bryan/.sase/artifacts/agents/gh\_bobs-org\_\_bob-cli/20261118233141/eleventh-evidence.tar-b29a04330e8b.gz, ref: f… |

#### artifacts

```yaml
- kind: file
  label: Record Card run 11 complete logs and provenance repair
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261118233141/eleventh-evidence.tar-b29a04330e8b.gz
  ref: file:explicit:0682f304639382f00cf062fa
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/eleventh-evidence.tar.gz
- kind: file
  label: Record Card run 11 summary
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261118233141/summary-bd421a9743b7.json
  ref: file:explicit:021e29c0f38c9e254766a0ae
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/run-20261119-040102/summary.json
- kind: file
  label: Record Card run 11 record-proof
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261118233141/record-proof-c3877a43607b.json
  ref: file:explicit:44281869de83453d3bb6d8dc
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/run-20261119-040102/results/record-proof.json
- kind: file
  label: Record Card run 11 eleventh-repair-summary
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261118233141/eleventh-repair-summary-0cc6ebb23188.json
  ref: file:explicit:5e46896e45ea2d66251b13b6
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/run-20261119-040102/eleventh-repair-summary.json
- kind: file
  label: Record Card run 11 final complete evidence bundle
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261118233141/eleventh-evidence.tar-11c5124167bf.gz
  ref: file:explicit:c1e7f95c35e3241d737b6f31
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/eleventh-evidence.tar.gz
- kind: file
  label: Record Card run 11 complete evidence index
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261118233141/eleventh-complete-evidence-index-12aaba125eab.json
  ref: file:explicit:6162d7a8b3bdbadc5618eb09
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/eleventh-complete-evidence-index.json
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
