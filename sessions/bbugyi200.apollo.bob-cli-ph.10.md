# Session: bob-cli-ph.10

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [bob-cli-ph](../users/bbugyi200/machines/apollo/hoods/bob-cli-ph/README.md) / bob-cli-ph.10

Owner: `bbugyi200.apollo` · Hood: `bob-cli-ph` · Members: 6 · Bead: [bob-cli-ph.10](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ph/bob-cli-ph.10.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-ph.10--1 [completed]"]
  n1["bob-cli-ph.10--mon [failed]"]
  n0 --> n1
  n2["bob-cli-ph.10--mon-0 [failed]"]
  n0 --> n2
  n3["bob-cli-ph.10--2 [completed]"]
  n0 --> n3
  n4["bob-cli-ph.10--plan [completed]"]
  n0 --> n4
  n5["bob-cli-ph.10--mon-1 [active]"]
  n0 --> n5
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-1"></a>1 | bob-cli-ph.10--1 | completed | gpt-6-luna / codex | 2026-11-26T02:58:09.435985+00:00 → 2026-11-26T03:23:09.824642+00:00 | [1](../agents/bbugyi200.apollo.bob-cli-ph.10--1/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.bob-cli-ph.10--1/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-ph.10--1/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-ph.10--mon | failed | gpt-6-luna / codex | 2026-11-26T02:50:06.174628+00:00 → 2026-11-26T02:58:09.803094+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-ph.10--mon/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-ph.10--mon-0 | failed | gpt-6-luna / codex | 2026-11-26T03:16:24.217828+00:00 → 2026-11-26T03:28:26.696207+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-ph.10--mon-0/chat.md) |
| <a id="member-2"></a>2 | bob-cli-ph.10--2 | completed | gpt-6-luna / codex | 2026-11-26T03:30:32.022884+00:00 → 2026-11-26T03:38:29.076946+00:00 | [1](../agents/bbugyi200.apollo.bob-cli-ph.10--2/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.bob-cli-ph.10--2/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-ph.10--2/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-ph.10--plan | completed | gpt-6-luna / codex | 2026-11-26T01:53:03.644076+00:00 → 2026-11-26T02:54:28.913904+00:00 | [1](../agents/bbugyi200.apollo.bob-cli-ph.10--plan/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.bob-cli-ph.10--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-ph.10--plan/chat.md) |
| <a id="member-mon-1"></a>mon-1 | bob-cli-ph.10--mon-1 | active | gpt-6-luna / codex | 2026-11-26T03:35:53.996216+00:00 | 0 | — | — |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| plan | bob-cli | [`9573ff8`](https://github.com/bobs-org/bob-cli/commit/9573ff869fbef177ff041e78bcf28ddac85a71be) | feat: retire all-caps task drawer recognition | 2026-11-25 21:51:35 EST |
| 1 | bob-cli | [`46aba67`](https://github.com/bobs-org/bob-cli/commit/46aba67724194df951bf2c23132f15861d2351ec) | fix(drawers): restore rename flow and complete bold-only cutover verification | 2026-11-25 22:21:33 EST |
| 2 | bob-cli | [`5d5509d`](https://github.com/bobs-org/bob-cli/commit/5d5509de4f27f4042eccf52b1c0f6171e43e88d9) | fix(capture): update drawer parser test fixtures | 2026-11-25 22:36:58 EST |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-ph.1](bbugyi200.apollo.bob-cli-ph.1.md) (session · 31) | bob-cli-ph hood | completed 20, failed 11 |
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
| [bob-cli-ph.6.1.4](../agents/bbugyi200.apollo.bob-cli-ph.6.1.4/README.md) | bob-cli-ph hood | completed |
| [bob-cli-ph.6.1.5](bbugyi200.apollo.bob-cli-ph.6.1.5.md) (session · 3) | bob-cli-ph hood | completed 2, failed 1 |
| [bob-cli-ph.6.1.land](../agents/bbugyi200.apollo.bob-cli-ph.6.1.land/README.md) | bob-cli-ph hood | completed |
| [bob-cli-ph.7](bbugyi200.apollo.bob-cli-ph.7.md) (session · 3) | bob-cli-ph hood | active 1, completed 2 |
| [bob-cli-ph.7.1.1](../agents/bbugyi200.apollo.bob-cli-ph.7.1.1/README.md) | bob-cli-ph hood | completed |
| [bob-cli-ph.7.1.2](bbugyi200.apollo.bob-cli-ph.7.1.2.md) (session · 9) | bob-cli-ph hood | completed 6, failed 3 |
| [bob-cli-ph.7.1.3](../agents/bbugyi200.apollo.bob-cli-ph.7.1.3/README.md) | bob-cli-ph hood | completed |
| [bob-cli-ph.7.1.4](../agents/bbugyi200.apollo.bob-cli-ph.7.1.4/README.md) | bob-cli-ph hood | completed |
| [bob-cli-ph.7.1.land](bbugyi200.apollo.bob-cli-ph.7.1.land.md) (session · 17) | bob-cli-ph hood | completed 14, failed 3 |
| [bob-cli-ph.8](bbugyi200.apollo.bob-cli-ph.8.md) (session · 7) | bob-cli-ph hood | active 1, completed 6 |
| [bob-cli-ph.8.1.1](bbugyi200.apollo.bob-cli-ph.8.1.1.md) (session · 9) | bob-cli-ph hood | active 1, completed 6, failed 2 |
| [bob-cli-ph.8.1.2](../agents/bbugyi200.apollo.bob-cli-ph.8.1.2/README.md) | bob-cli-ph hood | waiting |
| [bob-cli-ph.8.1.3](../agents/bbugyi200.apollo.bob-cli-ph.8.1.3/README.md) | bob-cli-ph hood | waiting |
| [bob-cli-ph.8.1.4](../agents/bbugyi200.apollo.bob-cli-ph.8.1.4/README.md) | bob-cli-ph hood | waiting |
| [bob-cli-ph.8.1.5](../agents/bbugyi200.apollo.bob-cli-ph.8.1.5/README.md) | bob-cli-ph hood | waiting |
| [bob-cli-ph.8.1.6](../agents/bbugyi200.apollo.bob-cli-ph.8.1.6/README.md) | bob-cli-ph hood | waiting |
| [bob-cli-ph.8.1.land](../agents/bbugyi200.apollo.bob-cli-ph.8.1.land/README.md) | bob-cli-ph hood | waiting |
| [bob-cli-ph.9](bbugyi200.apollo.bob-cli-ph.9.md) (session · 3) | bob-cli-ph hood | completed 3 |
| [bob-cli-ph.land](../agents/bbugyi200.apollo.bob-cli-ph.land/README.md) | bob-cli-ph hood | waiting |
