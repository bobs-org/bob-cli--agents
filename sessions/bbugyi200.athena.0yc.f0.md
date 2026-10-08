# Session: 0yc.f0

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [0yc](../users/bbugyi200/machines/athena/hoods/0yc/README.md) / 0yc.f0

Owner: `bbugyi200.athena` · Hood: `0yc` · Members: 5

## Lineage

```mermaid
flowchart TD
  n0["0yc.f0--code [completed]"]
  n1["0yc.f0--mon [active]"]
  n0 --> n1
  n2["0yc.f0--plan [completed]"]
  n0 --> n2
  n3["0yc.f0--1 [active]"]
  n0 --> n3
  n4["0yc.f0--gate [failed]"]
  n0 --> n4
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-code"></a>code | 0yc.f0--code | completed | muse-spark-1.3-contributor / muse | 2026-10-08T16:57:02.053632+00:00 → 2026-10-08T17:00:57.389470+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.0yc.f0--code/chat.md) |
| <a id="member-mon"></a>mon | 0yc.f0--mon | active | muse-spark-1.3-contributor / muse | 2026-10-08T17:00:21.948573+00:00 | 0 | — | — |
| <a id="member-plan"></a>plan | 0yc.f0--plan | completed | grok-4.7 / grok | 2026-10-08T16:49:49.909421+00:00 → 2026-10-08T17:00:57.389470+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.0yc.f0--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.0yc.f0--plan/chat.md) |
| <a id="member-1"></a>1 | 0yc.f0--1 | active | muse-spark-1.3-contributor / muse | 20261008130338 | 0 | [Prompt](../agents/bbugyi200.athena.0yc.f0--1/prompt.md) | — |
| <a id="member-gate"></a>gate | 0yc.f0--gate | failed | grok-4.7 / grok | 2026-10-08T16:56:24.226750+00:00 → 2026-10-08T16:56:45.672271+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.0yc.f0--gate/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [0yc](bbugyi200.athena.0yc.md) (session · 3) | ancestor | completed 2, failed 1 |
