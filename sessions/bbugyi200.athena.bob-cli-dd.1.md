# Session: bob-cli-dd.1

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-dd](../users/bbugyi200/machines/athena/hoods/bob-cli-dd/README.md) / bob-cli-dd.1

Owner: `bbugyi200.athena` · Hood: `bob-cli-dd` · Members: 9 · Bead: [bob-cli-dd.1](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-dd/bob-cli-dd.1.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-dd.1--3 [completed]"]
  n1["bob-cli-dd.1--1 [completed]"]
  n0 --> n1
  n2["bob-cli-dd.1--mon-1 [failed]"]
  n0 --> n2
  n3["bob-cli-dd.1--code [completed]"]
  n0 --> n3
  n4["bob-cli-dd.1--mon-0 [failed]"]
  n0 --> n4
  n5["bob-cli-dd.1--2 [completed]"]
  n0 --> n5
  n6["bob-cli-dd.1--mon [failed]"]
  n0 --> n6
  n7["bob-cli-dd.1--gate [failed]"]
  n0 --> n7
  n8["bob-cli-dd.1--plan [completed]"]
  n0 --> n8
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-3"></a>3 | bob-cli-dd.1--3 | completed | muse-spark-1.3-contributor / muse | 2026-10-28T00:14:35.026648+00:00 → 2026-10-28T00:19:50.966789+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-dd.1--3/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-dd.1--3/chat.md) |
| <a id="member-1"></a>1 | bob-cli-dd.1--1 | completed | muse-spark-1.3-contributor / muse | 2026-10-27T23:31:23.976048+00:00 → 2026-10-27T23:47:06.291890+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-dd.1--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-dd.1--1/chat.md) |
| <a id="member-mon-1"></a>mon-1 | bob-cli-dd.1--mon-1 | failed | muse-spark-1.3-contributor / muse | 2026-10-27T23:53:45.607097+00:00 → 2026-10-28T00:12:46.310398+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-dd.1--mon-1/chat.md) |
| <a id="member-code"></a>code | bob-cli-dd.1--code | completed | muse-spark-1.3-contributor / muse | 2026-10-27T23:02:28.560626+00:00 → 2026-10-27T23:25:37.487860+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-dd.1--code/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-dd.1--mon-0 | failed | muse-spark-1.3-contributor / muse | 2026-10-27T23:45:35.839576+00:00 → 2026-10-27T23:48:31.792361+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-dd.1--mon-0/chat.md) |
| <a id="member-2"></a>2 | bob-cli-dd.1--2 | completed | muse-spark-1.3-contributor / muse | 2026-10-27T23:50:08.925152+00:00 → 2026-10-27T23:54:44.568342+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-dd.1--2/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-dd.1--2/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-dd.1--mon | failed | muse-spark-1.3-contributor / muse | 2026-10-27T23:24:34.327619+00:00 → 2026-10-27T23:29:57.749856+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-dd.1--mon/chat.md) |
| <a id="member-gate"></a>gate | bob-cli-dd.1--gate | failed | gpt-6-astra / codex | 2026-10-27T23:01:12.215554+00:00 → 2026-10-27T23:01:56.034905+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-dd.1--gate/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-dd.1--plan | completed | gpt-6-astra / codex | 2026-10-27T22:56:30.890931+00:00 → 2026-10-27T23:25:37.487860+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-dd.1--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-dd.1--plan/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-dd.2](../agents/bbugyi200.athena.bob-cli-dd.2/README.md) | bob-cli-dd hood | completed |
| [bob-cli-dd.3](../agents/bbugyi200.athena.bob-cli-dd.3/README.md) | bob-cli-dd hood | completed |
| [bob-cli-dd.land](bbugyi200.athena.bob-cli-dd.land.md) (session · 11) | bob-cli-dd hood | completed 4, failed 7 |
