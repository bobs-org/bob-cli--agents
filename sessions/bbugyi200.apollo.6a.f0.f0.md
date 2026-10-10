# Session: 6a.f0.f0

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [6a](../users/bbugyi200/machines/apollo/hoods/6a/README.md) / 6a.f0.f0

Owner: `bbugyi200.apollo` · Hood: `6a` · Members: 3

## Lineage

```mermaid
flowchart TD
  n0["6a.f0.f0--plan [active]"]
  n1["6a.f0.f0--gate [failed]"]
  n0 --> n1
  n2["6a.f0.f0--code [active]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-plan"></a>plan | 6a.f0.f0--plan | active | gpt-6-astra / codex | 2026-10-10T14:17:35.819987+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.6a.f0.f0--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.6a.f0.f0--plan/chat.md) |
| <a id="member-gate"></a>gate | 6a.f0.f0--gate | failed | gpt-6-astra / codex | 2026-10-10T14:24:16.708489+00:00 → 2026-10-10T14:24:30.032267+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.6a.f0.f0--gate/chat.md) |
| <a id="member-code"></a>code | 6a.f0.f0--code | active | gpt-6-luna / codex | 2026-10-10T14:24:39.279632+00:00 | 0 | — | — |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [6a.f0](bbugyi200.apollo.6a.f0.md) (session · 3) | ancestor | completed 2, failed 1 |
| [6a](bbugyi200.apollo.6a.md) (session · 5) | ancestor | completed 3, failed 2 |
| [6a.f0.f1](bbugyi200.apollo.6a.f0.f1.md) (session · 3) | 6a.f0 hood | active 2, failed 1 |
