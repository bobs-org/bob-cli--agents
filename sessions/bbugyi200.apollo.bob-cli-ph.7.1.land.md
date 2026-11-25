# Session: bob-cli-ph.7.1.land

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [bob-cli-ph](../users/bbugyi200/machines/apollo/hoods/bob-cli-ph/README.md) / bob-cli-ph.7.1.land

Owner: `bbugyi200.apollo` · Hood: `bob-cli-ph` · Members: 6 · Bead: [bob-cli-ph.7.1](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ph/bob-cli-ph.7.1.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-ph.7.1.land--mon-0 [active]"]
  n1["bob-cli-ph.7.1.land--code [completed]"]
  n0 --> n1
  n2["bob-cli-ph.7.1.land--mon [failed]"]
  n0 --> n2
  n3["bob-cli-ph.7.1.land--gate [completed]"]
  n0 --> n3
  n4["bob-cli-ph.7.1.land--plan [completed]"]
  n0 --> n4
  n5["bob-cli-ph.7.1.land--1 [completed]"]
  n0 --> n5
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-mon-0"></a>mon-0 | bob-cli-ph.7.1.land--mon-0 | active | gpt-6-luna / codex | 2026-11-25T19:07:39.987908+00:00 | 0 | — | — |
| <a id="member-code"></a>code | bob-cli-ph.7.1.land--code | completed | gpt-6-luna / codex | 2026-11-25T18:18:28.188551+00:00 → 2026-11-25T18:51:06.889333+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-ph.7.1.land--code/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-ph.7.1.land--mon | failed | gpt-6-luna / codex | 2026-11-25T18:48:19.179264+00:00 → 2026-11-25T18:52:42.685963+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-ph.7.1.land--mon/chat.md) |
| <a id="member-gate"></a>gate | bob-cli-ph.7.1.land--gate | completed | gpt-6-astra / codex | 2026-11-25T18:17:38.412891+00:00 → 2026-11-25T18:17:48.258626+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-ph.7.1.land--gate/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-ph.7.1.land--plan | completed | gpt-6-astra / codex | 2026-11-25T18:06:31.261069+00:00 → 2026-11-25T18:51:06.889333+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-ph.7.1.land--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-ph.7.1.land--plan/chat.md) |
| <a id="member-1"></a>1 | bob-cli-ph.7.1.land--1 | completed | gpt-6-luna / codex | 2026-11-25T18:52:42.552717+00:00 → 2026-11-25T19:10:02.376594+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-ph.7.1.land--1/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-ph.7.1.land--1/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-ph.7](bbugyi200.apollo.bob-cli-ph.7.md) (session · 3) | ancestor | active 1, completed 2 |
| [bob-cli-ph.7.1.1](../agents/bbugyi200.apollo.bob-cli-ph.7.1.1/README.md) | bob-cli-ph.7.1 hood | completed |
| [bob-cli-ph.7.1.2](bbugyi200.apollo.bob-cli-ph.7.1.2.md) (session · 9) | bob-cli-ph.7.1 hood | completed 6, failed 3 |
| [bob-cli-ph.7.1.3](../agents/bbugyi200.apollo.bob-cli-ph.7.1.3/README.md) | bob-cli-ph.7.1 hood | completed |
| [bob-cli-ph.7.1.4](../agents/bbugyi200.apollo.bob-cli-ph.7.1.4/README.md) | bob-cli-ph.7.1 hood | completed |
| [bob-cli-ph.1](bbugyi200.apollo.bob-cli-ph.1.md) (session · 31) | bob-cli-ph hood | completed 20, failed 11 |
| [bob-cli-ph.10](../agents/bbugyi200.apollo.bob-cli-ph.10/README.md) | bob-cli-ph hood | waiting |
| [bob-cli-ph.11](../agents/bbugyi200.apollo.bob-cli-ph.11/README.md) | bob-cli-ph hood | waiting |
| [bob-cli-ph.2](bbugyi200.apollo.bob-cli-ph.2.md) (session · 7) | bob-cli-ph hood | active 1, completed 5, failed 1 |
| [bob-cli-ph.3](bbugyi200.apollo.bob-cli-ph.3.md) (session · 2) | bob-cli-ph hood | active 1, completed 1 |
| [bob-cli-ph.3](../agents/bbugyi200.apollo.bob-cli-ph.3/README.md) | bob-cli-ph hood | completed |
| [bob-cli-ph.4](../agents/bbugyi200.apollo.bob-cli-ph.4/README.md) | bob-cli-ph hood | completed |
| [bob-cli-ph.5](bbugyi200.apollo.bob-cli-ph.5.md) (session · 3) | bob-cli-ph hood | completed 3 |
| [bob-cli-ph.6](bbugyi200.apollo.bob-cli-ph.6.md) (session · 3) | bob-cli-ph hood | active 1, completed 2 |
| [bob-cli-ph.6.1.1](../agents/bbugyi200.apollo.bob-cli-ph.6.1.1/README.md) | bob-cli-ph hood | completed |
| [bob-cli-ph.6.1.2](../agents/bbugyi200.apollo.bob-cli-ph.6.1.2/README.md) | bob-cli-ph hood | completed |
| [bob-cli-ph.6.1.3](../agents/bbugyi200.apollo.bob-cli-ph.6.1.3/README.md) | bob-cli-ph hood | completed |
| [bob-cli-ph.6.1.4](../agents/bbugyi200.apollo.bob-cli-ph.6.1.4/README.md) | bob-cli-ph hood | waiting |
| [bob-cli-ph.6.1.5](../agents/bbugyi200.apollo.bob-cli-ph.6.1.5/README.md) | bob-cli-ph hood | waiting |
| [bob-cli-ph.6.1.land](../agents/bbugyi200.apollo.bob-cli-ph.6.1.land/README.md) | bob-cli-ph hood | waiting |
| [bob-cli-ph.8](../agents/bbugyi200.apollo.bob-cli-ph.8/README.md) | bob-cli-ph hood | waiting |
| [bob-cli-ph.9](../agents/bbugyi200.apollo.bob-cli-ph.9/README.md) | bob-cli-ph hood | waiting |
| [bob-cli-ph.land](../agents/bbugyi200.apollo.bob-cli-ph.land/README.md) | bob-cli-ph hood | waiting |
