# Agent: bob-cli-do.land--plan

[Agent Hoods](../../README.md) / [bbugyi200](../../users/bbugyi200/README.md) / [athena](../../users/bbugyi200/machines/athena/README.md) / [bob-cli-do](../../users/bbugyi200/machines/athena/hoods/bob-cli-do/README.md) / [bob-cli-do.land](../../sessions/bbugyi200.athena.bob-cli-do.land.md) / bob-cli-do.land--plan

**Global name:** `bbugyi200.athena.bob-cli-do.land--plan` · **State:** active · **Source run:** `run-f21a460c4efeadb11596a49639806b93`

**Owner:** `bbugyi200.athena` · **Project:** bob-cli · **Hood:** bob-cli-do

## Summary

- Bead: [bob-cli-do](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-do/README.md)
- Model: gpt-6-astra
- Provider: codex
- Timing: 2026-10-28T17:34:40.121867+00:00
- Commits: 0
- Variables: [1](#variables)

## Files

[Chat](chat.md) · [Prompt](prompt.md)

## Variables

| Variable | Value |
|---|---|
| `artifacts` | \[{bead: bob-cli-do, kind: file, label: bob-cli-do landing clobber reproducer, path: /home/bryan/.sase/artifacts/agents/gh\_bobs-org\_\_bob-cli/20261028104758/repro\_clobber-89308d73062f.py, ref: file:exp… |

#### artifacts

```yaml
- bead: bob-cli-do
  kind: file
  label: bob-cli-do landing clobber reproducer
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261028104758/repro_clobber-89308d73062f.py
  ref: file:explicit:bc73ed9db0392b2a41b250e4
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/land-audit/repro_clobber.py
- bead: bob-cli-do
  kind: file
  label: bob-cli-do landing clobber reproduction results
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261028104758/repro_clobber-577d82092c62.json
  ref: file:explicit:8ba8616a472fa4e32615c8d9
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/land-audit/repro_clobber.json
- bead: bob-cli-do
  kind: file
  label: bob-cli-do false-positive recovery redetection
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261028104758/runbook_repro-cc24cd1e566e.txt
  ref: file:explicit:d761a43e46d85b01f4fe2c1d
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/land-audit/runbook_repro.txt
```

Values are truncated for display; see [meta.json](meta.json) for the full values.

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-do.1](../bbugyi200.athena.bob-cli-do.1/README.md) | bob-cli-do hood | completed |
| [bob-cli-do.2](../bbugyi200.athena.bob-cli-do.2/README.md) | bob-cli-do hood | completed |
| [bob-cli-do.3](../../sessions/bbugyi200.athena.bob-cli-do.3.md) (session · 3) | bob-cli-do hood | completed 2, failed 1 |
| [bob-cli-do.4](../bbugyi200.athena.bob-cli-do.4/README.md) | bob-cli-do hood | completed |
