# Session: bob-cli-n7.3

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-n7](../users/bbugyi200/machines/athena/hoods/bob-cli-n7/README.md) / bob-cli-n7.3

Owner: `bbugyi200.athena` · Hood: `bob-cli-n7` · Members: 3 · Bead: [bob-cli-n7.3](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-n7/bob-cli-n7.3.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-n7.3--plan [completed]"]
  n1["bob-cli-n7.3--1 [completed]"]
  n0 --> n1
  n2["bob-cli-n7.3--mon [failed]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-plan"></a>plan | bob-cli-n7.3--plan | completed | muse-spark-1.3-contributor / muse | 2026-11-18T14:01:53.700214+00:00 → 2026-11-18T14:29:24.605169+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-n7.3--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-n7.3--plan/chat.md) |
| <a id="member-1"></a>1 | bob-cli-n7.3--1 | completed | muse-spark-1.3-contributor / muse | 2026-11-18T15:17:48.294325+00:00 → 2026-11-18T15:25:20.014161+00:00 | [1](../agents/bbugyi200.athena.bob-cli-n7.3--1/README.md#commits) | [Prompt](../agents/bbugyi200.athena.bob-cli-n7.3--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-n7.3--1/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-n7.3--mon | failed | muse-spark-1.3-contributor / muse | 2026-11-18T14:24:47.523438+00:00 → 2026-11-18T15:17:48.443912+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-n7.3--mon/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| 1 | bob-cli | [`f0857be`](https://github.com/bobs-org/bob-cli/commit/f0857be8a6d084b9e9548919b27178c1b3bb2511) | fix(subprocess): make detached-grandchild pipe-drain tests deterministic and portable | 2026-11-18 10:24:41 EST |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-n7.1](bbugyi200.athena.bob-cli-n7.1.md) (session · 7) | bob-cli-n7 hood | completed 4, failed 3 |
| [bob-cli-n7.1](../agents/bbugyi200.athena.bob-cli-n7.1/README.md) | bob-cli-n7 hood | completed |
| [bob-cli-n7.2](bbugyi200.athena.bob-cli-n7.2.md) (session · 3) | bob-cli-n7 hood | completed 2, failed 1 |
| [bob-cli-n7.4](bbugyi200.athena.bob-cli-n7.4.md) (session · 3) | bob-cli-n7 hood | completed 2, failed 1 |
| [bob-cli-n7.land](bbugyi200.athena.bob-cli-n7.land.md) (session · 23) | bob-cli-n7 hood | active 1, completed 14, failed 8 |
| [bob-cli-n7.land](../agents/bbugyi200.athena.bob-cli-n7.land/README.md) | bob-cli-n7 hood | completed |
