# Session: bob-cli-go.land

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [bob-cli-go](../users/bbugyi200/machines/apollo/hoods/bob-cli-go/README.md) / bob-cli-go.land

Owner: `bbugyi200.apollo` · Hood: `bob-cli-go` · Members: 7 · Bead: [bob-cli-go](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-go/README.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-go.land--mon-0 [dismissed]"]
  n1["bob-cli-go.land--mon [failed]"]
  n0 --> n1
  n2["bob-cli-go.land--gate [dismissed]"]
  n0 --> n2
  n3["bob-cli-go.land--code [completed]"]
  n0 --> n3
  n4["bob-cli-go.land--plan [dismissed]"]
  n0 --> n4
  n5["bob-cli-go.land--1 [dismissed]"]
  n0 --> n5
  n6["bob-cli-go.land--2 [active]"]
  n0 --> n6
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-mon-0"></a>mon-0 | bob-cli-go.land--mon-0 | dismissed | gpt-6-luna / codex | 2026-11-04T13:41:42.223221 → 2026-11-04T13:55:32.599071 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-go.land--mon-0/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-go.land--mon | failed | gpt-6-luna / codex | 2026-11-04T18:28:49.856886+00:00 → 2026-11-04T18:32:13.398371+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-go.land--mon/chat.md) |
| <a id="member-gate"></a>gate | bob-cli-go.land--gate | dismissed | opus / claude | 2026-11-04T12:55:04.097420 → 2026-11-04T12:55:17 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-go.land--gate/chat.md) |
| <a id="member-code"></a>code | bob-cli-go.land--code | completed | gpt-6-luna / codex | 2026-11-04T17:55:57.946926+00:00 → 2026-11-04T18:30:04.140200+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-go.land--code/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-go.land--plan | dismissed | opus / claude | 2026-11-04T12:29:50.277996 → 2026-11-04T13:30:04.555506 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-go.land--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-go.land--plan/chat.md) |
| <a id="member-1"></a>1 | bob-cli-go.land--1 | dismissed | gpt-6-luna / codex | 2026-11-04T13:32:23.050517 → 2026-11-04T13:42:50.947237 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-go.land--1/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-go.land--1/chat.md) |
| <a id="member-2"></a>2 | bob-cli-go.land--2 | active | gpt-6-luna / codex | 2026-11-04T18:56:53.882896+00:00 | [1](../agents/bbugyi200.apollo.bob-cli-go.land--2/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.bob-cli-go.land--2/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-go.land--2/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| 2 | — | `3e33c5c` | feat(capture): support transfer task picker | 2026-11-04 14:21:04 EST |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-go.1](../agents/bbugyi200.apollo.bob-cli-go.1/README.md) | bob-cli-go hood | dismissed |
| [bob-cli-go.10](bbugyi200.apollo.bob-cli-go.10.md) (session · 3) | bob-cli-go hood | active 1, dismissed 2 |
| [bob-cli-go.10.1.1](../agents/bbugyi200.apollo.bob-cli-go.10.1.1/README.md) | bob-cli-go hood | active |
| [bob-cli-go.10.1.2](../agents/bbugyi200.apollo.bob-cli-go.10.1.2/README.md) | bob-cli-go hood | active |
| [bob-cli-go.10.1.3](../agents/bbugyi200.apollo.bob-cli-go.10.1.3/README.md) | bob-cli-go hood | active |
| [bob-cli-go.10.1.4](bbugyi200.apollo.bob-cli-go.10.1.4.md) (session · 3) | bob-cli-go hood | active 3 |
| [bob-cli-go.10.1.5](../agents/bbugyi200.apollo.bob-cli-go.10.1.5/README.md) | bob-cli-go hood | active |
| [bob-cli-go.10.1.land](../agents/bbugyi200.apollo.bob-cli-go.10.1.land/README.md) | bob-cli-go hood | active |
| [bob-cli-go.11](../agents/bbugyi200.apollo.bob-cli-go.11/README.md) | bob-cli-go hood | dismissed |
| [bob-cli-go.12](bbugyi200.apollo.bob-cli-go.12.md) (session · 5) | bob-cli-go hood | active 1, dismissed 4 |
| [bob-cli-go.13](../agents/bbugyi200.apollo.bob-cli-go.13/README.md) | bob-cli-go hood | dismissed |
| [bob-cli-go.2](bbugyi200.apollo.bob-cli-go.2.md) (session · 9) | bob-cli-go hood | active 2, dismissed 7 |
| [bob-cli-go.3](bbugyi200.apollo.bob-cli-go.3.md) (session · 15) | bob-cli-go hood | dismissed 15 |
| [bob-cli-go.4](bbugyi200.apollo.bob-cli-go.4.md) (session · 3) | bob-cli-go hood | active 1, dismissed 2 |
| [bob-cli-go.4.1.1](bbugyi200.apollo.bob-cli-go.4.1.1.md) (session · 5) | bob-cli-go hood | active 5 |
| [bob-cli-go.4.1.2](../agents/bbugyi200.apollo.bob-cli-go.4.1.2/README.md) | bob-cli-go hood | active |
| [bob-cli-go.4.1.3](bbugyi200.apollo.bob-cli-go.4.1.3.md) (session · 9) | bob-cli-go hood | active 9 |
| [bob-cli-go.4.1.land](bbugyi200.apollo.bob-cli-go.4.1.land.md) (session · 5) | bob-cli-go hood | active 3, completed 1, failed 1 |
| [bob-cli-go.5](../agents/bbugyi200.apollo.bob-cli-go.5/README.md) | bob-cli-go hood | dismissed |
| [bob-cli-go.6](../agents/bbugyi200.apollo.bob-cli-go.6/README.md) | bob-cli-go hood | dismissed |
| [bob-cli-go.7](../agents/bbugyi200.apollo.bob-cli-go.7/README.md) | bob-cli-go hood | dismissed |
| [bob-cli-go.8](../agents/bbugyi200.apollo.bob-cli-go.8/README.md) | bob-cli-go hood | dismissed |
| [bob-cli-go.9](../agents/bbugyi200.apollo.bob-cli-go.9/README.md) | bob-cli-go hood | dismissed |
