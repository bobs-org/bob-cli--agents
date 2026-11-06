# Session: bob-cli-dl.6

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [bob-cli-dl](../users/bbugyi200/machines/apollo/hoods/bob-cli-dl/README.md) / bob-cli-dl.6

Owner: `bbugyi200.apollo` · Hood: `bob-cli-dl` · Members: 3 · Bead: [bob-cli-dl.6](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-dl/bob-cli-dl.6.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-dl.6--1 [active]"]
  n1["bob-cli-dl.6--mon [completed]"]
  n0 --> n1
  n2["bob-cli-dl.6--plan [active]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-1"></a>1 | bob-cli-dl.6--1 | active | gpt-6-luna / codex | 2026-10-28T14:56:14.545322+00:00 | [1](../agents/bbugyi200.apollo.bob-cli-dl.6--1/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.bob-cli-dl.6--1/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-dl.6--1/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-dl.6--mon | completed | gpt-6-luna / codex | 2026-10-28T14:53:35.405365+00:00 → 2026-10-28T14:56:14.567611+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-dl.6--mon/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-dl.6--plan | active | gpt-6-luna / codex | 2026-10-28T14:18:17.000568+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-dl.6--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-dl.6--plan/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| 1 | bob-cli | [`8f311da`](https://github.com/bobs-org/bob-cli/commit/8f311dabaf225ae9638cdbfd6a933fed90cb7350) | docs(memory): clarify task relation cancel-label exception | 2026-10-28 11:07:44 EDT |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-dl.1](bbugyi200.apollo.bob-cli-dl.1.md) (session · 3) | bob-cli-dl hood | active 2, completed 1 |
| [bob-cli-dl.2](bbugyi200.apollo.bob-cli-dl.2.md) (session · 7) | bob-cli-dl hood | active 3, completed 3, failed 1 |
| [bob-cli-dl.3](../agents/bbugyi200.apollo.bob-cli-dl.3/README.md) | bob-cli-dl hood | active |
| [bob-cli-dl.4](../agents/bbugyi200.apollo.bob-cli-dl.4/README.md) | bob-cli-dl hood | active |
| [bob-cli-dl.5](bbugyi200.apollo.bob-cli-dl.5.md) (session · 3) | bob-cli-dl hood | active 1, completed 2 |
| [bob-cli-dl.7](../agents/bbugyi200.apollo.bob-cli-dl.7/README.md) | bob-cli-dl hood | active |
| [bob-cli-dl.8](../agents/bbugyi200.apollo.bob-cli-dl.8/README.md) | bob-cli-dl hood | active |
| [bob-cli-dl.land](bbugyi200.apollo.bob-cli-dl.land.md) (session · 3) | bob-cli-dl hood | active 1, completed 2 |
