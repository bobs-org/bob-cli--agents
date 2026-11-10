# Session: bob-cli-dm.6.1.land

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [bob-cli-dm](../users/bbugyi200/machines/apollo/hoods/bob-cli-dm/README.md) / bob-cli-dm.6.1.land

Owner: `bbugyi200.apollo` · Hood: `bob-cli-dm` · Members: 9 · Bead: [bob-cli-dm.6.1](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-dm/bob-cli-dm.6.1.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-dm.6.1.land--gate [completed]"]
  n1["bob-cli-dm.6.1.land--3 [dismissed]"]
  n0 --> n1
  n2["bob-cli-dm.6.1.land--mon-0 [failed]"]
  n0 --> n2
  n3["bob-cli-dm.6.1.land--2 [dismissed]"]
  n0 --> n3
  n4["bob-cli-dm.6.1.land--plan [dismissed]"]
  n0 --> n4
  n5["bob-cli-dm.6.1.land--mon-1 [completed]"]
  n0 --> n5
  n6["bob-cli-dm.6.1.land--1 [dismissed]"]
  n0 --> n6
  n7["bob-cli-dm.6.1.land--code [completed]"]
  n0 --> n7
  n8["bob-cli-dm.6.1.land--mon [completed]"]
  n0 --> n8
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-gate"></a>gate | bob-cli-dm.6.1.land--gate | completed | gpt-6-astra / codex | 2026-10-29T01:42:41.257735+00:00 → 2026-10-29T01:42:50.874966+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-dm.6.1.land--gate/chat.md) |
| <a id="member-3"></a>3 | bob-cli-dm.6.1.land--3 | dismissed | grok-4.6 / grok | 2026-10-28T22:37:24.788541 → 2026-10-28T22:50:21.509521 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-dm.6.1.land--3/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-dm.6.1.land--3/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-dm.6.1.land--mon-0 | failed | gpt-6-luna / codex | 2026-10-29T02:16:38.677067+00:00 → 2026-10-29T02:18:48.100346+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-dm.6.1.land--mon-0/chat.md) |
| <a id="member-2"></a>2 | bob-cli-dm.6.1.land--2 | dismissed | grok-4.6 / grok | 2026-10-28T22:18:47.864114 → 2026-10-28T22:25:38.011409 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-dm.6.1.land--2/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-dm.6.1.land--2/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-dm.6.1.land--plan | dismissed | gpt-6-astra / codex | 2026-10-28T21:31:17.145304 → 2026-10-28T21:58:50.275593 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-dm.6.1.land--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-dm.6.1.land--plan/chat.md) |
| <a id="member-mon-1"></a>mon-1 | bob-cli-dm.6.1.land--mon-1 | completed | grok-4.6 / grok | 2026-10-29T02:24:30.398093+00:00 → 2026-10-29T02:37:25.188989+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-dm.6.1.land--mon-1/chat.md) |
| <a id="member-1"></a>1 | bob-cli-dm.6.1.land--1 | dismissed | gpt-6-luna / codex | 2026-10-28T22:11:17.858167 → 2026-10-28T22:17:33.865860 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-dm.6.1.land--1/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-dm.6.1.land--1/chat.md) |
| <a id="member-code"></a>code | bob-cli-dm.6.1.land--code | completed | gpt-6-luna / codex | 2026-10-29T01:43:03.766147+00:00 → 2026-10-29T01:58:50.251691+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-dm.6.1.land--code/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-dm.6.1.land--mon | completed | gpt-6-luna / codex | 2026-10-29T01:57:51.150837+00:00 → 2026-10-29T02:11:18.021935+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-dm.6.1.land--mon/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-dm.6](bbugyi200.apollo.bob-cli-dm.6.md) (session · 3) | ancestor | completed 1, dismissed 2 |
| [bob-cli-dm.6.1.1](../agents/bbugyi200.apollo.bob-cli-dm.6.1.1/README.md) | bob-cli-dm.6.1 hood | dismissed |
| [bob-cli-dm.6.1.2](../agents/bbugyi200.apollo.bob-cli-dm.6.1.2/README.md) | bob-cli-dm.6.1 hood | dismissed |
| [bob-cli-dm.6.1.3](../agents/bbugyi200.apollo.bob-cli-dm.6.1.3/README.md) | bob-cli-dm.6.1 hood | dismissed |
| [bob-cli-dm.1](bbugyi200.apollo.bob-cli-dm.1.md) (session · 3) | bob-cli-dm hood | completed 1, dismissed 2 |
| [bob-cli-dm.1.1.1](bbugyi200.apollo.bob-cli-dm.1.1.1.md) (session · 3) | bob-cli-dm hood | completed 1, dismissed 2 |
| [bob-cli-dm.1.1.2](bbugyi200.apollo.bob-cli-dm.1.1.2.md) (session · 7) | bob-cli-dm hood | completed 1, dismissed 4, failed 2 |
| [bob-cli-dm.1.1.3](../agents/bbugyi200.apollo.bob-cli-dm.1.1.3/README.md) | bob-cli-dm hood | dismissed |
| [bob-cli-dm.1.1.land](bbugyi200.apollo.bob-cli-dm.1.1.land.md) (session · 3) | bob-cli-dm hood | completed 2, dismissed 1 |
| [bob-cli-dm.2](bbugyi200.apollo.bob-cli-dm.2.md) (session · 3) | bob-cli-dm hood | completed 1, dismissed 2 |
| [bob-cli-dm.3](../agents/bbugyi200.apollo.bob-cli-dm.3/README.md) | bob-cli-dm hood | dismissed |
| [bob-cli-dm.4](bbugyi200.apollo.bob-cli-dm.4.md) (session · 5) | bob-cli-dm hood | completed 2, dismissed 2, failed 1 |
| [bob-cli-dm.5](bbugyi200.apollo.bob-cli-dm.5.md) (session · 3) | bob-cli-dm hood | completed 1, dismissed 2 |
| [bob-cli-dm.5.1.1](../agents/bbugyi200.apollo.bob-cli-dm.5.1.1/README.md) | bob-cli-dm hood | dismissed |
| [bob-cli-dm.5.1.2](../agents/bbugyi200.apollo.bob-cli-dm.5.1.2/README.md) | bob-cli-dm hood | dismissed |
| [bob-cli-dm.5.1.3](../agents/bbugyi200.apollo.bob-cli-dm.5.1.3/README.md) | bob-cli-dm hood | dismissed |
| [bob-cli-dm.5.1.land](bbugyi200.apollo.bob-cli-dm.5.1.land.md) (session · 3) | bob-cli-dm hood | completed 2, dismissed 1 |
| [bob-cli-dm.7](bbugyi200.apollo.bob-cli-dm.7.md) (session · 3) | bob-cli-dm hood | completed 1, dismissed 2 |
| [bob-cli-dm.7.1.1](../agents/bbugyi200.apollo.bob-cli-dm.7.1.1/README.md) | bob-cli-dm hood | dismissed |
| [bob-cli-dm.7.1.2](../agents/bbugyi200.apollo.bob-cli-dm.7.1.2/README.md) | bob-cli-dm hood | dismissed |
| [bob-cli-dm.7.1.3](../agents/bbugyi200.apollo.bob-cli-dm.7.1.3/README.md) | bob-cli-dm hood | dismissed |
| [bob-cli-dm.7.1.4](../agents/bbugyi200.apollo.bob-cli-dm.7.1.4/README.md) | bob-cli-dm hood | dismissed |
| [bob-cli-dm.7.1.land](bbugyi200.apollo.bob-cli-dm.7.1.land.md) (session · 3) | bob-cli-dm hood | completed 2, dismissed 1 |
| [bob-cli-dm.8](../agents/bbugyi200.apollo.bob-cli-dm.8/README.md) | bob-cli-dm hood | dismissed |
| [bob-cli-dm.9](../agents/bbugyi200.apollo.bob-cli-dm.9/README.md) | bob-cli-dm hood | dismissed |
| [bob-cli-dm.land](../agents/bbugyi200.apollo.bob-cli-dm.land/README.md) | bob-cli-dm hood | dismissed |
