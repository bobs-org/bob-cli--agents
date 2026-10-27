# Session: an.f0.w0

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [an](../users/bbugyi200/machines/apollo/hoods/an/README.md) / an.f0.w0

Owner: `bbugyi200.apollo` · Hood: `an` · Members: 7

## Lineage

```mermaid
flowchart TD
  n0["an.f0.w0--gate [failed]"]
  n1["an.f0.w0--mon [failed]"]
  n0 --> n1
  n2["an.f0.w0--1 [completed]"]
  n0 --> n2
  n3["an.f0.w0--2 [active]"]
  n0 --> n3
  n4["an.f0.w0--plan [completed]"]
  n0 --> n4
  n5["an.f0.w0--mon-0 [failed]"]
  n0 --> n5
  n6["an.f0.w0--code [completed]"]
  n0 --> n6
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-gate"></a>gate | an.f0.w0--gate | failed | opus / claude | 2026-10-27T18:14:36.747491+00:00 → 2026-10-27T18:14:56.630403+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.an.f0.w0--gate/chat.md) |
| <a id="member-mon"></a>mon | an.f0.w0--mon | failed | gpt-6-luna / codex | 2026-10-27T18:24:57.048718+00:00 → 2026-10-27T18:37:57.531601+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.an.f0.w0--mon/chat.md) |
| <a id="member-1"></a>1 | an.f0.w0--1 | completed | gpt-6-luna / codex | 2026-10-27T18:38:03.630001+00:00 → 2026-10-27T18:42:36.082791+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.an.f0.w0--1/prompt.md) | [Chat](../agents/bbugyi200.apollo.an.f0.w0--1/chat.md) |
| <a id="member-2"></a>2 | an.f0.w0--2 | active | muse-spark-1.3-contributor / muse | 2026-10-27T18:48:08.989612+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.an.f0.w0--2/prompt.md) | — |
| <a id="member-plan"></a>plan | an.f0.w0--plan | completed | opus / claude | 2026-10-27T18:07:25.644546+00:00 → 2026-10-27T18:27:28.278366+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.an.f0.w0--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.an.f0.w0--plan/chat.md) |
| <a id="member-mon-0"></a>mon-0 | an.f0.w0--mon-0 | failed | gpt-6-luna / codex | 2026-10-27T18:41:19.422631+00:00 → 2026-10-27T18:48:00.952080+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.an.f0.w0--mon-0/chat.md) |
| <a id="member-code"></a>code | an.f0.w0--code | completed | gpt-6-luna / codex | 2026-10-27T18:15:39.818656+00:00 → 2026-10-27T18:27:28.278366+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.an.f0.w0--code/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [an.f0](bbugyi200.apollo.an.f0.md) (session · 5) | ancestor | completed 3, failed 2 |
| [an](bbugyi200.apollo.an.md) (session · 9) | ancestor | completed 5, failed 4 |
