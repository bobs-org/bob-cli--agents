# Session: bob-cli-fb.2.1.1

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [bob-cli-fb](../users/bbugyi200/machines/apollo/hoods/bob-cli-fb/README.md) / bob-cli-fb.2.1.1

Owner: `bbugyi200.apollo` · Hood: `bob-cli-fb` · Members: 3 · Bead: [bob-cli-fb.2.1.1](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-fb/bob-cli-fb.2.1.1.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-fb.2.1.1--plan [active]"]
  n1["bob-cli-fb.2.1.1--1 [active]"]
  n0 --> n1
  n2["bob-cli-fb.2.1.1--mon [active]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-plan"></a>plan | bob-cli-fb.2.1.1--plan | active | grok-4.6 / grok | 2026-11-01T18:01:53.687068+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-fb.2.1.1--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-fb.2.1.1--plan/chat.md) |
| <a id="member-1"></a>1 | bob-cli-fb.2.1.1--1 | active | grok-4.6 / grok | 2026-11-01T19:20:30.703326+00:00 | [1](../agents/bbugyi200.apollo.bob-cli-fb.2.1.1--1/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.bob-cli-fb.2.1.1--1/prompt.md) | — |
| <a id="member-mon"></a>mon | bob-cli-fb.2.1.1--mon | active | grok-4.6 / grok | 2026-11-01T18:41:59.277833+00:00 | 0 | — | — |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| 1 | bob-cli | [`f6d3084`](https://github.com/bobs-org/bob-cli/commit/f6d3084bb7796b56292f820f62b0cea5bedab472) | feat(task-complete): add leaf-project keep-moving successor engine | 2026-11-01 14:31:46 EST |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-fb.2](bbugyi200.apollo.bob-cli-fb.2.md) (session · 3) | ancestor | active 3 |
| [bob-cli-fb.2.1.2](../agents/bbugyi200.apollo.bob-cli-fb.2.1.2/README.md) | bob-cli-fb.2.1 hood | active |
| [bob-cli-fb.2.1.3](../agents/bbugyi200.apollo.bob-cli-fb.2.1.3/README.md) | bob-cli-fb.2.1 hood | active |
| [bob-cli-fb.2.1.land](bbugyi200.apollo.bob-cli-fb.2.1.land.md) (session · 5) | bob-cli-fb.2.1 hood | active 3, completed 1, failed 1 |
| [bob-cli-fb.1](../agents/bbugyi200.apollo.bob-cli-fb.1/README.md) | bob-cli-fb hood | active |
| [bob-cli-fb.3](../agents/bbugyi200.apollo.bob-cli-fb.3/README.md) | bob-cli-fb hood | active |
| [bob-cli-fb.4](bbugyi200.apollo.bob-cli-fb.4.md) (session · 5) | bob-cli-fb hood | active 2, completed 2, failed 1 |
| [bob-cli-fb.5](bbugyi200.apollo.bob-cli-fb.5.md) (session · 15) | bob-cli-fb hood | active 5, completed 8, failed 2 |
| [bob-cli-fb.land](bbugyi200.apollo.bob-cli-fb.land.md) (session · 3) | bob-cli-fb hood | active 2, completed 1 |
