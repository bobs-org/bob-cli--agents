# Session: bob-cli-q8.10.3

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [bob-cli-q8](../users/bbugyi200/machines/apollo/hoods/bob-cli-q8/README.md) / bob-cli-q8.10.3

Owner: `bbugyi200.apollo` · Hood: `bob-cli-q8` · Members: 6 · Bead: [bob-cli-q8.10.3](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-q8/bob-cli-q8.10.3.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-q8.10.3--1 [completed]"]
  n1["bob-cli-q8.10.3--mon-0 [failed]"]
  n0 --> n1
  n2["bob-cli-q8.10.3--mon [failed]"]
  n0 --> n2
  n3["bob-cli-q8.10.3--2 [completed]"]
  n0 --> n3
  n4["bob-cli-q8.10.3--plan [completed]"]
  n0 --> n4
  n5["bob-cli-q8.10.3--mon-1 [active]"]
  n0 --> n5
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-1"></a>1 | bob-cli-q8.10.3--1 | completed | gpt-6-luna / codex | 2026-11-26T08:35:58.193859+00:00 → 2026-11-26T08:49:20.520117+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-q8.10.3--1/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-q8.10.3--1/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-q8.10.3--mon-0 | failed | gpt-6-luna / codex | 2026-11-26T08:47:15.358740+00:00 → 2026-11-26T08:54:58.170324+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-q8.10.3--mon-0/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-q8.10.3--mon | failed | gpt-6-luna / codex | 2026-11-26T08:26:12.086555+00:00 → 2026-11-26T08:35:55.711543+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-q8.10.3--mon/chat.md) |
| <a id="member-2"></a>2 | bob-cli-q8.10.3--2 | completed | gpt-6-luna / codex | 2026-11-26T08:55:05.799577+00:00 → 2026-11-26T09:07:16.717315+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-q8.10.3--2/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-q8.10.3--2/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-q8.10.3--plan | completed | gpt-6-luna / codex | 2026-11-26T07:43:30.462246+00:00 → 2026-11-26T08:29:33.936446+00:00 | [1](../agents/bbugyi200.apollo.bob-cli-q8.10.3--plan/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.bob-cli-q8.10.3--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-q8.10.3--plan/chat.md) |
| <a id="member-mon-1"></a>mon-1 | bob-cli-q8.10.3--mon-1 | active | gpt-6-luna / codex | 2026-11-26T08:58:24.628809+00:00 | 0 | — | — |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| plan | bob-cli | [`8cb474b`](https://github.com/bobs-org/bob-cli/commit/8cb474ba818f1e214e38634dce63f8ffb120b11d) | docs(tasks): document navigation tie consequence copy | 2026-11-26 03:27:19 EST |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-q8.10.1](../agents/bbugyi200.apollo.bob-cli-q8.10.1/README.md) | bob-cli-q8.10 hood | completed |
| [bob-cli-q8.10.2](../agents/bbugyi200.apollo.bob-cli-q8.10.2/README.md) | bob-cli-q8.10 hood | completed |
| [bob-cli-q8.10.land](../agents/bbugyi200.apollo.bob-cli-q8.10.land/README.md) | bob-cli-q8.10 hood | waiting |
| [bob-cli-q8.1](../agents/bbugyi200.apollo.bob-cli-q8.1/README.md) | bob-cli-q8 hood | completed |
| [bob-cli-q8.2](../agents/bbugyi200.apollo.bob-cli-q8.2/README.md) | bob-cli-q8 hood | completed |
| [bob-cli-q8.3](../agents/bbugyi200.apollo.bob-cli-q8.3/README.md) | bob-cli-q8 hood | completed |
| [bob-cli-q8.4](../agents/bbugyi200.apollo.bob-cli-q8.4/README.md) | bob-cli-q8 hood | completed |
| [bob-cli-q8.5](../agents/bbugyi200.apollo.bob-cli-q8.5/README.md) | bob-cli-q8 hood | completed |
| [bob-cli-q8.6](bbugyi200.apollo.bob-cli-q8.6.md) (session · 3) | bob-cli-q8 hood | completed 3 |
| [bob-cli-q8.7](../agents/bbugyi200.apollo.bob-cli-q8.7/README.md) | bob-cli-q8 hood | completed |
| [bob-cli-q8.8](../agents/bbugyi200.apollo.bob-cli-q8.8/README.md) | bob-cli-q8 hood | completed |
| [bob-cli-q8.9](../agents/bbugyi200.apollo.bob-cli-q8.9/README.md) | bob-cli-q8 hood | completed |
| [bob-cli-q8.land](bbugyi200.apollo.bob-cli-q8.land.md) (session · 3) | bob-cli-q8 hood | active 1, completed 2 |
