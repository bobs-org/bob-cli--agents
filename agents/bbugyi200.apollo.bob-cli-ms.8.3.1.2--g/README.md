# Agent: bob-cli-ms.8.3.1.2--g

[Agent Hoods](../../README.md) / [bbugyi200](../../users/bbugyi200/README.md) / [apollo](../../users/bbugyi200/machines/apollo/README.md) / [bob-cli-ms](../../users/bbugyi200/machines/apollo/hoods/bob-cli-ms/README.md) / [bob-cli-ms.8.3.1.2](../../sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.2.md) / bob-cli-ms.8.3.1.2--g

**Global name:** `bbugyi200.apollo.bob-cli-ms.8.3.1.2--g` · **State:** completed · **Source run:** `run-e9fbb24554e69bc468d99b408aed6c49`

**Owner:** `bbugyi200.apollo` · **Project:** bob-cli · **Hood:** bob-cli-ms

## Summary

- Bead: [bob-cli-ms.8.3.1.2](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ms/bob-cli-ms.8.3.1.2.md)
- Model: gpt-6-astra
- Provider: codex
- Timing: 2026-11-19T08:00:59.802214+00:00 → 2026-11-19T08:22:25.276893+00:00
- Commits: 0
- Variables: [1](#variables)

## Files

[Chat](chat.md) · [Prompt](prompt.md)

## Variables

| Variable | Value |
|---|---|
| `artifacts` | \[{bead: bob-cli-ms.8.3.1.2, kind: file, label: Run15 complete Record Card evidence, 91 files and verified manifest, path: /home/bryan/.sase/artifacts/agents/gh\_bobs-org\_\_bob-cli/20261119030019/run15-… |

#### artifacts

```yaml
- bead: bob-cli-ms.8.3.1.2
  kind: file
  label: Run15 complete Record Card evidence, 91 files and verified manifest
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261119030019/run15-complete-evidence.tar-d7226e1a21c1.gz
  ref: file:explicit:b5d9f297d9a1816494117d5c
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/run15-complete-evidence.tar.gz
- bead: bob-cli-ms.8.3.1.2
  kind: file
  label: Run15 raw verification summary
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261119030019/summary-568d1dea248e.json
  ref: file:explicit:d261482c78a83d29fd563381
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/run-20261119-072804/summary.json
- bead: bob-cli-ms.8.3.1.2
  kind: file
  label: Run15 raw real Obsidian report, 140 pass and 4 fail
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261119030019/record-proof-af8ff4ff325a.json
  ref: file:explicit:f4d35aae42abc765e89ee7ed
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/run-20261119-072804/results/record-proof.json
- bead: bob-cli-ms.8.3.1.2
  kind: file
  label: Run15 all 22 inspected PNG verdicts and SHA256 hashes
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261119030019/screenshot-review-d4424b88a82e.json
  ref: file:explicit:5c45e0c873bf93b2fdf765be
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/run-20261119-072804/screenshot-review.json
- bead: bob-cli-ms.8.3.1.2
  kind: file
  label: Run15 settled refusal repair and regression results
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261119030019/recovery-review-ee83681fe80f.json
  ref: file:explicit:cf5f71ee9a86c4b5d6f8453f
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.build/record-workflows/run-20261119-072804/recovery-review.json
```

Values are truncated for display; see [meta.json](meta.json) for the full values.

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-ms.8.3](../../sessions/bbugyi200.apollo.bob-cli-ms.8.3.md) (session · 3) | ancestor | active 1, completed 2 |
| [bob-cli-ms.8.3.1.1](../../sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.1.md) (session · 25) | bob-cli-ms.8.3.1 hood | active 1, completed 12, failed 12 |
| [bob-cli-ms.8.3.1.3](../bbugyi200.apollo.bob-cli-ms.8.3.1.3/README.md) | bob-cli-ms.8.3.1 hood | waiting |
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
