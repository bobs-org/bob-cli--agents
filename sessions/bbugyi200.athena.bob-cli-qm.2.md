# Session: bob-cli-qm.2

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-qm](../users/bbugyi200/machines/athena/hoods/bob-cli-qm/README.md) / bob-cli-qm.2

Owner: `bbugyi200.athena` · Hood: `bob-cli-qm` · Members: 3 · Bead: [bob-cli-qm.2](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-qm/bob-cli-qm.2.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-qm.2--mon [failed]"]
  n1["bob-cli-qm.2--1 [active]"]
  n0 --> n1
  n2["bob-cli-qm.2--plan [completed]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-mon"></a>mon | bob-cli-qm.2--mon | failed | gpt-6-luna / codex | 2026-11-26T18:43:06.619726+00:00 → 2026-11-26T18:47:31.364212+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-qm.2--mon/chat.md) |
| <a id="member-1"></a>1 | bob-cli-qm.2--1 | active | gpt-6-luna / codex | 2026-11-26T18:47:30.915243+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-qm.2--1/prompt.md) | — |
| <a id="member-plan"></a>plan | bob-cli-qm.2--plan | completed | gpt-6-luna / codex | 2026-11-26T18:09:45.640066+00:00 → 2026-11-26T18:44:46.559584+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-qm.2--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-qm.2--plan/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-qm.1](../agents/bbugyi200.athena.bob-cli-qm.1/README.md) | bob-cli-qm hood | completed |
| [bob-cli-qm.3](bbugyi200.athena.bob-cli-qm.3.md) (session · 3) | bob-cli-qm hood | active 1, completed 2 |
| [bob-cli-qm.4](../agents/bbugyi200.athena.bob-cli-qm.4/README.md) | bob-cli-qm hood | waiting |
| [bob-cli-qm.5](../agents/bbugyi200.athena.bob-cli-qm.5/README.md) | bob-cli-qm hood | waiting |
| [bob-cli-qm.6](../agents/bbugyi200.athena.bob-cli-qm.6/README.md) | bob-cli-qm hood | waiting |
| [bob-cli-qm.7](../agents/bbugyi200.athena.bob-cli-qm.7/README.md) | bob-cli-qm hood | waiting |
| [bob-cli-qm.land](../agents/bbugyi200.athena.bob-cli-qm.land/README.md) | bob-cli-qm hood | waiting |
