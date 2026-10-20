# Session: 12k

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [12k](../users/bbugyi200/machines/athena/hoods/12k/README.md) / 12k

Owner: `bbugyi200.athena` · Hood: `12k` · Members: 3

## Lineage

```mermaid
flowchart TD
  n0["12k--code [active]"]
  n1["12k--gate [failed]"]
  n0 --> n1
  n2["12k--plan [active]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-code"></a>code | 12k--code | active | gpt-6-luna / codex | 2026-10-20T17:42:24.040766+00:00 | 0 | — | — |
| <a id="member-gate"></a>gate | 12k--gate | failed | opus / claude | 2026-10-20T17:40:41.183616+00:00 → 2026-10-20T17:41:55.585705+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.12k--gate/chat.md) |
| <a id="member-plan"></a>plan | 12k--plan | active | opus / claude | 2026-10-20T17:34:59.483299+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.12k--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.12k--plan/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [12k.f0](../agents/bbugyi200.athena.12k.f0/README.md) | descendant | waiting |
