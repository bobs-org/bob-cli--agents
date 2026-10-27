# Session: an.f0.w0

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [an](../users/bbugyi200/machines/apollo/hoods/an/README.md) / an.f0.w0

Owner: `bbugyi200.apollo` · Hood: `an` · Members: 4

## Lineage

```mermaid
flowchart TD
  n0["an.f0.w0--gate [failed]"]
  n1["an.f0.w0--mon [active]"]
  n0 --> n1
  n2["an.f0.w0--plan [completed]"]
  n0 --> n2
  n3["an.f0.w0--code [completed]"]
  n0 --> n3
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-gate"></a>gate | an.f0.w0--gate | failed | opus / claude | 2026-10-27T18:14:36.747491+00:00 → 2026-10-27T18:14:56.630403+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.an.f0.w0--gate/chat.md) |
| <a id="member-mon"></a>mon | an.f0.w0--mon | active | gpt-6-luna / codex | 2026-10-27T18:24:57.048718+00:00 | 0 | — | — |
| <a id="member-plan"></a>plan | an.f0.w0--plan | completed | opus / claude | 2026-10-27T18:07:25.644546+00:00 → 2026-10-27T18:27:28.278366+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.an.f0.w0--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.an.f0.w0--plan/chat.md) |
| <a id="member-code"></a>code | an.f0.w0--code | completed | gpt-6-luna / codex | 2026-10-27T18:15:39.818656+00:00 → 2026-10-27T18:27:28.278366+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.an.f0.w0--code/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [an.f0](bbugyi200.apollo.an.f0.md) (session · 5) | ancestor | completed 3, failed 2 |
| [an](bbugyi200.apollo.an.md) (session · 9) | ancestor | completed 5, failed 4 |
