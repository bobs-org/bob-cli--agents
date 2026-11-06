# Agent: bob-cli-hg.6.1.land--plan

[Agent Hoods](../../README.md) / [bbugyi200](../../users/bbugyi200/README.md) / [apollo](../../users/bbugyi200/machines/apollo/README.md) / [bob-cli-hg](../../users/bbugyi200/machines/apollo/hoods/bob-cli-hg/README.md) / [bob-cli-hg.6.1.land](../../sessions/bbugyi200.apollo.bob-cli-hg.6.1.land.md) / bob-cli-hg.6.1.land--plan

**Global name:** `bbugyi200.apollo.bob-cli-hg.6.1.land--plan` · **State:** completed · **Source run:** `run-a3f49f587051b37690ae6305d6db36d9`

**Owner:** `bbugyi200.apollo` · **Project:** bob-cli · **Hood:** bob-cli-hg

## Summary

- Bead: [bob-cli-hg.6.1](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-hg/bob-cli-hg.6.1.md)
- Model: gpt-6-astra
- Provider: codex
- Timing: 2026-11-06T10:08:37.713889+00:00 → 2026-11-06T11:40:25.823692+00:00
- Commits: 0
- Variables: [1](#variables)

## Files

[Chat](chat.md) · [Prompt](prompt.md)

## Variables

| Variable | Value |
|---|---|
| `artifacts` | \[{bead: bob-cli-hg.6.1, kind: file, label: Gmail landing synthetic reproducer, path: /home/bryan/.sase/artifacts/agents/gh\_bobs-org\_\_bob-cli/20261105234839/gmail-land-repro-27da8d1ec6d1.py, ref: file… |

#### artifacts

```yaml
- bead: bob-cli-hg.6.1
  kind: file
  label: Gmail landing synthetic reproducer
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261105234839/gmail-land-repro-27da8d1ec6d1.py
  ref: file:explicit:e7aea0b4b642b917e1e2d9f7
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_23/.git/gmail-land-repro.py
- bead: bob-cli-hg.6.1
  kind: file
  label: Gmail landing reproduced defects on fcc4efa5
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261105234839/gmail-land-repro-6a3ed50ec51a.jsonl
  ref: file:explicit:18705a7c72a5c9d067cf6be1
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_23/.git/gmail-land-repro.jsonl
```

Values are truncated for display; see [meta.json](meta.json) for the full values.

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-hg.6](../../sessions/bbugyi200.apollo.bob-cli-hg.6.md) (session · 3) | ancestor | active 1, completed 2 |
| [bob-cli-hg.6.1.1](../../sessions/bbugyi200.apollo.bob-cli-hg.6.1.1.md) (session · 3) | bob-cli-hg.6.1 hood | completed 2, failed 1 |
| [bob-cli-hg.6.1.2](../bbugyi200.apollo.bob-cli-hg.6.1.2/README.md) | bob-cli-hg.6.1 hood | completed |
| [bob-cli-hg.6.1.3](../bbugyi200.apollo.bob-cli-hg.6.1.3/README.md) | bob-cli-hg.6.1 hood | completed |
| [bob-cli-hg.6.1.4](../bbugyi200.apollo.bob-cli-hg.6.1.4/README.md) | bob-cli-hg.6.1 hood | completed |
| [bob-cli-hg.1](../../sessions/bbugyi200.apollo.bob-cli-hg.1.md) (session · 3) | bob-cli-hg hood | completed 3 |
| [bob-cli-hg.10](../../sessions/bbugyi200.apollo.bob-cli-hg.10.md) (session · 13) | bob-cli-hg hood | completed 11, failed 2 |
| [bob-cli-hg.11](../../sessions/bbugyi200.apollo.bob-cli-hg.11.md) (session · 3) | bob-cli-hg hood | completed 2, failed 1 |
| [bob-cli-hg.12](../../sessions/bbugyi200.apollo.bob-cli-hg.12.md) (session · 3) | bob-cli-hg hood | active 1, completed 2 |
| [bob-cli-hg.12.1.1](../bbugyi200.apollo.bob-cli-hg.12.1.1/README.md) | bob-cli-hg hood | completed |
| [bob-cli-hg.12.1.2](../bbugyi200.apollo.bob-cli-hg.12.1.2/README.md) | bob-cli-hg hood | completed |
| [bob-cli-hg.12.1.3](../../sessions/bbugyi200.apollo.bob-cli-hg.12.1.3.md) (session · 7) | bob-cli-hg hood | completed 5, failed 2 |
| [bob-cli-hg.12.1.4](../bbugyi200.apollo.bob-cli-hg.12.1.4/README.md) | bob-cli-hg hood | completed |
| [bob-cli-hg.12.1.5](../../sessions/bbugyi200.apollo.bob-cli-hg.12.1.5.md) (session · 5) | bob-cli-hg hood | completed 4, failed 1 |
| [bob-cli-hg.12.1.6](../bbugyi200.apollo.bob-cli-hg.12.1.6/README.md) | bob-cli-hg hood | completed |
| [bob-cli-hg.12.1.land](../bbugyi200.apollo.bob-cli-hg.12.1.land/README.md) | bob-cli-hg hood | waiting |
| [bob-cli-hg.13](../bbugyi200.apollo.bob-cli-hg.13/README.md) | bob-cli-hg hood | waiting |
| [bob-cli-hg.14](../../sessions/bbugyi200.apollo.bob-cli-hg.14.md) (session · 7) | bob-cli-hg hood | completed 4, failed 3 |
| [bob-cli-hg.2](../bbugyi200.apollo.bob-cli-hg.2/README.md) | bob-cli-hg hood | completed |
| [bob-cli-hg.3](../../sessions/bbugyi200.apollo.bob-cli-hg.3.md) (session · 3) | bob-cli-hg hood | active 1, completed 2 |
| [bob-cli-hg.3.1.1](../bbugyi200.apollo.bob-cli-hg.3.1.1/README.md) | bob-cli-hg hood | active |
| [bob-cli-hg.3.1.2](../bbugyi200.apollo.bob-cli-hg.3.1.2/README.md) | bob-cli-hg hood | active |
| [bob-cli-hg.3.1.3](../bbugyi200.apollo.bob-cli-hg.3.1.3/README.md) | bob-cli-hg hood | active |
| [bob-cli-hg.3.1.4](../bbugyi200.apollo.bob-cli-hg.3.1.4/README.md) | bob-cli-hg hood | active |
| [bob-cli-hg.3.1.land](../../sessions/bbugyi200.apollo.bob-cli-hg.3.1.land.md) (session · 3) | bob-cli-hg hood | active 2, completed 1 |
| [bob-cli-hg.4](../bbugyi200.apollo.bob-cli-hg.4/README.md) | bob-cli-hg hood | completed |
| [bob-cli-hg.5](../bbugyi200.apollo.bob-cli-hg.5/README.md) | bob-cli-hg hood | completed |
| [bob-cli-hg.7](../bbugyi200.apollo.bob-cli-hg.7/README.md) | bob-cli-hg hood | completed |
| [bob-cli-hg.8](../../sessions/bbugyi200.apollo.bob-cli-hg.8.md) (session · 3) | bob-cli-hg hood | completed 2, failed 1 |
| [bob-cli-hg.9](../bbugyi200.apollo.bob-cli-hg.9/README.md) | bob-cli-hg hood | completed |
| [bob-cli-hg.land](../bbugyi200.apollo.bob-cli-hg.land/README.md) | bob-cli-hg hood | waiting |
