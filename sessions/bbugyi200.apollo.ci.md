# Session: ci

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [ci](../users/bbugyi200/machines/apollo/hoods/ci/README.md) / ci

Owner: `bbugyi200.apollo` · Hood: `ci` · Members: 3

## Lineage

```mermaid
flowchart TD
  n0["ci--code [completed]"]
  n1["ci--plan [dismissed]"]
  n0 --> n1
  n2["ci--gate [completed]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-code"></a>code | ci--code | completed | muse-spark-1.3-contributor / muse | 2026-11-04T23:37:21.049728+00:00 → 2026-11-04T23:52:15.953087+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.ci--code/prompt.md) | [Chat](../agents/bbugyi200.apollo.ci--code/chat.md) |
| <a id="member-plan"></a>plan | ci--plan | dismissed | opus / claude | 2026-11-04T18:25:50.896224 → 2026-11-04T18:35:08.185410 | 0 | [Prompt](../agents/bbugyi200.apollo.ci--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.ci--plan/chat.md) |
| <a id="member-gate"></a>gate | ci--gate | completed | opus / claude | 2026-11-04T23:35:47.928909+00:00 → 2026-11-04T23:36:49.676657+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.ci--gate/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| — | — | `c4e1d5e` | feat(capture): normalize flat clipboard lists | 2026-07-17 16:29:15 EDT |
