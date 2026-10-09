# Session: 0yk

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [0yk](../users/bbugyi200/machines/athena/hoods/0yk/README.md) / 0yk

Owner: `bbugyi200.athena` · Hood: `0yk` · Members: 5

## Lineage

```mermaid
flowchart TD
  n0["0yk--1 [active]"]
  n1["0yk--mon [failed]"]
  n0 --> n1
  n2["0yk--code [completed]"]
  n0 --> n2
  n3["0yk--plan [completed]"]
  n0 --> n3
  n4["0yk--gate [failed]"]
  n0 --> n4
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-1"></a>1 | 0yk--1 | active | muse-spark-1.3-contributor / muse | 2026-10-09T12:27:50.866722+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.0yk--1/prompt.md) | — |
| <a id="member-mon"></a>mon | 0yk--mon | failed | muse-spark-1.3-contributor / muse | 2026-10-09T12:23:08.486248+00:00 → 2026-10-09T12:27:22.932213+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.0yk--mon/chat.md) |
| <a id="member-code"></a>code | 0yk--code | completed | muse-spark-1.3-contributor / muse | 2026-10-09T12:06:48.341728+00:00 → 2026-10-09T12:23:48.560618+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.0yk--code/prompt.md) | [Chat](../agents/bbugyi200.athena.0yk--code/chat.md) |
| <a id="member-plan"></a>plan | 0yk--plan | completed | opus / claude | 2026-10-09T06:06:24.643879+00:00 → 2026-10-09T06:21:20.052430+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.0yk--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.0yk--plan/chat.md) |
| <a id="member-gate"></a>gate | 0yk--gate | failed | opus / claude | 2026-10-09T12:05:29.069683+00:00 → 2026-10-09T12:06:06.548731+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.0yk--gate/chat.md) |
