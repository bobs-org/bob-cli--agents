# Session: 6a.f0.f1

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [6a](../users/bbugyi200/machines/apollo/hoods/6a/README.md) / 6a.f0.f1

Owner: `bbugyi200.apollo` · Hood: `6a` · Members: 3

## Lineage

```mermaid
flowchart TD
  n0["6a.f0.f1--gate [failed]"]
  n1["6a.f0.f1--code [active]"]
  n0 --> n1
  n2["6a.f0.f1--plan [active]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-gate"></a>gate | 6a.f0.f1--gate | failed | gpt-6-astra / codex | 2026-10-10T14:33:54.855569+00:00 → 2026-10-10T14:34:09.224198+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.6a.f0.f1--gate/chat.md) |
| <a id="member-code"></a>code | 6a.f0.f1--code | active | grok-4.6 / grok | 2026-10-10T14:34:23.626496+00:00 | 0 | — | — |
| <a id="member-plan"></a>plan | 6a.f0.f1--plan | active | gpt-6-astra / codex | 2026-10-10T14:27:35.378493+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.6a.f0.f1--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.6a.f0.f1--plan/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [6a.f0](bbugyi200.apollo.6a.f0.md) (session · 3) | ancestor | completed 2, failed 1 |
| [6a](bbugyi200.apollo.6a.md) (session · 5) | ancestor | completed 3, failed 2 |
| [6a.f0.f0](bbugyi200.apollo.6a.f0.f0.md) (session · 3) | 6a.f0 hood | active 2, failed 1 |
