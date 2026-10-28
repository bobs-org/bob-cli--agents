# Session: bob-cli-dp.4

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-dp](../users/bbugyi200/machines/athena/hoods/bob-cli-dp/README.md) / bob-cli-dp.4

Owner: `bbugyi200.athena` · Hood: `bob-cli-dp` · Members: 3 · Bead: [bob-cli-dp.4](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-dp/bob-cli-dp.4.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-dp.4--gate [failed]"]
  n1["bob-cli-dp.4--code [active]"]
  n0 --> n1
  n2["bob-cli-dp.4--plan [active]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-gate"></a>gate | bob-cli-dp.4--gate | failed | gpt-6-astra / codex | 2026-10-28T15:34:28.087289+00:00 → 2026-10-28T15:35:51.480759+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-dp.4--gate/chat.md) |
| <a id="member-code"></a>code | bob-cli-dp.4--code | active | gpt-6-luna / codex | 2026-10-28T15:36:32.593975+00:00 | 0 | — | — |
| <a id="member-plan"></a>plan | bob-cli-dp.4--plan | active | gpt-6-astra / codex | 2026-10-28T15:28:45.904175+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-dp.4--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-dp.4--plan/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-dp.1](../agents/bbugyi200.athena.bob-cli-dp.1/README.md) | bob-cli-dp hood | failed |
| [bob-cli-dp.2](../agents/bbugyi200.athena.bob-cli-dp.2/README.md) | bob-cli-dp hood | active |
| [bob-cli-dp.3](../agents/bbugyi200.athena.bob-cli-dp.3/README.md) | bob-cli-dp hood | active |
| [bob-cli-dp.land](../agents/bbugyi200.athena.bob-cli-dp.land/README.md) | bob-cli-dp hood | waiting |
