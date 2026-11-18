# Agent: bob-cli-mr.3.1.land--plan

[Agent Hoods](../../README.md) / [bbugyi200](../../users/bbugyi200/README.md) / [athena](../../users/bbugyi200/machines/athena/README.md) / [bob-cli-mr](../../users/bbugyi200/machines/athena/hoods/bob-cli-mr/README.md) / [bob-cli-mr.3.1.land](../../sessions/bbugyi200.athena.bob-cli-mr.3.1.land.md) / bob-cli-mr.3.1.land--plan

**Global name:** `bbugyi200.athena.bob-cli-mr.3.1.land--plan` · **State:** completed · **Source run:** `run-e51bcb2617f67c7d46d1f08a2df60824`

**Owner:** `bbugyi200.athena` · **Project:** bob-cli · **Hood:** bob-cli-mr

## Summary

- Bead: [bob-cli-mr.3.1](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-mr/bob-cli-mr.3.1.md)
- Model: gpt-6-astra
- Provider: codex
- Timing: 2026-11-17T20:57:15.701653+00:00 → 2026-11-17T22:25:10.360651+00:00
- Commits: 0
- Variables: [1](#variables)

## Files

[Chat](chat.md) · [Prompt](prompt.md)

## Variables

| Variable | Value |
|---|---|
| `artifacts` | \[{bead: bob-cli-mr.3.1, kind: file, label: Deterministic scan landing reproducer, path: /home/bryan/.sase/artifacts/agents/gh\_bobs-org\_\_bob-cli/20261117121551/mr31\_scan\_repro-547397a411a9.py, ref: fi… |

#### artifacts

```yaml
- bead: bob-cli-mr.3.1
  kind: file
  label: Deterministic scan landing reproducer
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261117121551/mr31_scan_repro-547397a411a9.py
  ref: file:explicit:c5c3f5771f7e66352b19542a
  source_path: /tmp/mr31_scan_repro.py
- bead: bob-cli-mr.3.1
  kind: file
  label: Scan landing reproduction results at 6c409ab2
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261117121551/mr31_scan_repro_result-d19641945e8e.txt
  ref: file:explicit:7aa8ba853d55aee2765444f5
  source_path: /tmp/mr31_scan_repro_result.txt
```

Values are truncated for display; see [meta.json](meta.json) for the full values.

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-mr.3](../../sessions/bbugyi200.athena.bob-cli-mr.3.md) (session · 3) | ancestor | active 1, completed 2 |
| [bob-cli-mr.3.1.1](../bbugyi200.athena.bob-cli-mr.3.1.1/README.md) | bob-cli-mr.3.1 hood | completed |
| [bob-cli-mr.3.1.2](../../sessions/bbugyi200.athena.bob-cli-mr.3.1.2.md) (session · 5) | bob-cli-mr.3.1 hood | completed 4, failed 1 |
| [bob-cli-mr.3.1.3](../../sessions/bbugyi200.athena.bob-cli-mr.3.1.3.md) (session · 3) | bob-cli-mr.3.1 hood | completed 3 |
| [bob-cli-mr.1](../bbugyi200.athena.bob-cli-mr.1/README.md) | bob-cli-mr hood | completed |
| [bob-cli-mr.2](../../sessions/bbugyi200.athena.bob-cli-mr.2.md) (session · 3) | bob-cli-mr hood | completed 3 |
| [bob-cli-mr.land](../../sessions/bbugyi200.athena.bob-cli-mr.land.md) (session · 9) | bob-cli-mr hood | completed 8, failed 1 |
