# Agent: bob-cli-mr.land--plan

[Agent Hoods](../../README.md) / [bbugyi200](../../users/bbugyi200/README.md) / [athena](../../users/bbugyi200/machines/athena/README.md) / [bob-cli-mr](../../users/bbugyi200/machines/athena/hoods/bob-cli-mr/README.md) / [bob-cli-mr.land](../../sessions/bbugyi200.athena.bob-cli-mr.land.md) / bob-cli-mr.land--plan

**Global name:** `bbugyi200.athena.bob-cli-mr.land--plan` · **State:** active · **Source run:** `run-e427683778274406a25a1dd840c62143`

**Owner:** `bbugyi200.athena` · **Project:** bob-cli · **Hood:** bob-cli-mr

## Summary

- Bead: [bob-cli-mr](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-mr/README.md)
- Model: gpt-6-astra
- Provider: codex
- Timing: 2026-11-17T22:22:08.015953+00:00
- Commits: 0
- Variables: [1](#variables)

## Files

[Chat](chat.md) · [Prompt](prompt.md)

## Variables

| Variable | Value |
|---|---|
| `artifacts` | \[{bead: bob-cli-mr, kind: file, label: T1 landing isolated TextBundle read-set race probe, path: /home/bryan/.sase/artifacts/agents/gh\_bobs-org\_\_bob-cli/20261117111759/bob-cli-mr-readset-probe-f913de… |

#### artifacts

```yaml
- bead: bob-cli-mr
  kind: file
  label: T1 landing isolated TextBundle read-set race probe
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261117111759/bob-cli-mr-readset-probe-f913de4b6c4f.py
  ref: file:explicit:bd831c44f897f151df7fe929
  source_path: /tmp/bob-cli-mr-readset-probe.py
- bead: bob-cli-mr
  kind: file
  label: T1 landing current-commit TextBundle race results
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261117111759/bob-cli-mr-readset-probe-9804cd631a19.log
  ref: file:explicit:1b54ca1c1f7d772c943b7307
  source_path: /tmp/bob-cli-mr-readset-probe.log
- bead: bob-cli-mr
  kind: markdown
  label: Validated T2 draft for the T1 repair coder to propose after closeout
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261117111759/sase_plan_backlog_triage_t2-59d988c38942.md
  ref: file:explicit:e68e1976353c86235b1d0e23
  source_path: /tmp/sase_plan_backlog_triage_t2.md
```

Values are truncated for display; see [meta.json](meta.json) for the full values.

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-mr.1](../bbugyi200.athena.bob-cli-mr.1/README.md) | bob-cli-mr hood | completed |
| [bob-cli-mr.2](../../sessions/bbugyi200.athena.bob-cli-mr.2.md) (session · 3) | bob-cli-mr hood | completed 3 |
| [bob-cli-mr.3](../../sessions/bbugyi200.athena.bob-cli-mr.3.md) (session · 3) | bob-cli-mr hood | active 1, completed 2 |
| [bob-cli-mr.3.1.1](../bbugyi200.athena.bob-cli-mr.3.1.1/README.md) | bob-cli-mr hood | completed |
| [bob-cli-mr.3.1.2](../../sessions/bbugyi200.athena.bob-cli-mr.3.1.2.md) (session · 5) | bob-cli-mr hood | completed 4, failed 1 |
| [bob-cli-mr.3.1.3](../../sessions/bbugyi200.athena.bob-cli-mr.3.1.3.md) (session · 3) | bob-cli-mr hood | completed 3 |
| [bob-cli-mr.3.1.land](../../sessions/bbugyi200.athena.bob-cli-mr.3.1.land.md) (session · 3) | bob-cli-mr hood | completed 3 |
