# Session: bob-cli-ir.10.1.land

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-ir](../users/bbugyi200/machines/athena/hoods/bob-cli-ir/README.md) / bob-cli-ir.10.1.land

Owner: `bbugyi200.athena` · Hood: `bob-cli-ir` · Members: 7 · Bead: [bob-cli-ir.10.1](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ir/bob-cli-ir.10.1.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-ir.10.1.land--gate [completed]"]
  n1["bob-cli-ir.10.1.land--plan [completed]"]
  n0 --> n1
  n2["bob-cli-ir.10.1.land--2 [completed]"]
  n0 --> n2
  n3["bob-cli-ir.10.1.land--mon [failed]"]
  n0 --> n3
  n4["bob-cli-ir.10.1.land--1 [completed]"]
  n0 --> n4
  n5["bob-cli-ir.10.1.land--code [completed]"]
  n0 --> n5
  n6["bob-cli-ir.10.1.land--mon-0 [completed]"]
  n0 --> n6
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-gate"></a>gate | bob-cli-ir.10.1.land--gate | completed | gpt-6-astra / codex | 2026-11-09T12:30:39.798629+00:00 → 2026-11-09T12:31:30.767244+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-ir.10.1.land--gate/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-ir.10.1.land--plan | completed | gpt-6-astra / codex | 2026-11-09T12:15:26.148196+00:00 → 2026-11-09T13:29:22.633072+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-ir.10.1.land--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-ir.10.1.land--plan/chat.md) |
| <a id="member-2"></a>2 | bob-cli-ir.10.1.land--2 | completed | grok-4.6 / grok | 2026-11-09T14:34:26.340791+00:00 → 2026-11-09T14:40:53.983131+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-ir.10.1.land--2/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-ir.10.1.land--2/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-ir.10.1.land--mon | failed | grok-4.6 / grok | 2026-11-09T13:27:42.822103+00:00 → 2026-11-09T13:48:11.636487+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-ir.10.1.land--mon/chat.md) |
| <a id="member-1"></a>1 | bob-cli-ir.10.1.land--1 | completed | grok-4.6 / grok | 2026-11-09T13:49:39.783568+00:00 → 2026-11-09T14:10:59.488015+00:00 | [1](../agents/bbugyi200.athena.bob-cli-ir.10.1.land--1/README.md#commits) | [Prompt](../agents/bbugyi200.athena.bob-cli-ir.10.1.land--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-ir.10.1.land--1/chat.md) |
| <a id="member-code"></a>code | bob-cli-ir.10.1.land--code | completed | grok-4.6 / grok | 2026-11-09T12:32:03.181895+00:00 → 2026-11-09T13:29:22.633072+00:00 | [1](../agents/bbugyi200.athena.bob-cli-ir.10.1.land--code/README.md#commits) | — | [Chat](../agents/bbugyi200.athena.bob-cli-ir.10.1.land--code/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-ir.10.1.land--mon-0 | completed | grok-4.6 / grok | 2026-11-09T14:09:05.102985+00:00 → 2026-11-09T14:33:14.714940+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-ir.10.1.land--mon-0/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| code | bob-cli | [`c09e2bc`](https://github.com/bobs-org/bob-cli/commit/c09e2bcd6538e90c56030374900550a1d6053817) | fix(capture): agree Record Card completion with keyboard acceptance | 2026-11-09 08:28:34 EST |
| 1 | bob-cli | [`eded3b9`](https://github.com/bobs-org/bob-cli/commit/eded3b9ca680244939ec9c69a71dac7484e4b683) | fix(capture): keep Record Return through last-field analysis | 2026-11-09 09:10:10 EST |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-ir.10](bbugyi200.athena.bob-cli-ir.10.md) (session · 3) | ancestor | active 1, completed 2 |
| [bob-cli-ir.10.1.1](../agents/bbugyi200.athena.bob-cli-ir.10.1.1/README.md) | bob-cli-ir.10.1 hood | completed |
| [bob-cli-ir.10.1.2](../agents/bbugyi200.athena.bob-cli-ir.10.1.2/README.md) | bob-cli-ir.10.1 hood | completed |
| [bob-cli-ir.10.1.3](../agents/bbugyi200.athena.bob-cli-ir.10.1.3/README.md) | bob-cli-ir.10.1 hood | completed |
| [bob-cli-ir.10.1.4](bbugyi200.athena.bob-cli-ir.10.1.4.md) (session · 5) | bob-cli-ir.10.1 hood | completed 4, failed 1 |
| [bob-cli-ir.1](../agents/bbugyi200.athena.bob-cli-ir.1/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.11](bbugyi200.athena.bob-cli-ir.11.md) (session · 5) | bob-cli-ir hood | completed 5 |
| [bob-cli-ir.12](../agents/bbugyi200.athena.bob-cli-ir.12/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.13](../agents/bbugyi200.athena.bob-cli-ir.13/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.2](bbugyi200.athena.bob-cli-ir.2.md) (session · 3) | bob-cli-ir hood | active 1, completed 2 |
| [bob-cli-ir.2.1.1](../agents/bbugyi200.athena.bob-cli-ir.2.1.1/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.2.1.2](../agents/bbugyi200.athena.bob-cli-ir.2.1.2/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.2.1.3](../agents/bbugyi200.athena.bob-cli-ir.2.1.3/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.2.1.4](../agents/bbugyi200.athena.bob-cli-ir.2.1.4/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.2.1.land](bbugyi200.athena.bob-cli-ir.2.1.land.md) (session · 3) | bob-cli-ir hood | completed 3 |
| [bob-cli-ir.2.1.land](../agents/bbugyi200.athena.bob-cli-ir.2.1.land/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.3](../agents/bbugyi200.athena.bob-cli-ir.3/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.4](../agents/bbugyi200.athena.bob-cli-ir.4/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.5](bbugyi200.athena.bob-cli-ir.5.md) (session · 3) | bob-cli-ir hood | active 1, completed 2 |
| [bob-cli-ir.5.1.1](../agents/bbugyi200.athena.bob-cli-ir.5.1.1/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.5.1.2](../agents/bbugyi200.athena.bob-cli-ir.5.1.2/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.5.1.3](../agents/bbugyi200.athena.bob-cli-ir.5.1.3/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.5.1.4](bbugyi200.athena.bob-cli-ir.5.1.4.md) (session · 5) | bob-cli-ir hood | completed 4, failed 1 |
| [bob-cli-ir.5.1.land](bbugyi200.athena.bob-cli-ir.5.1.land.md) (session · 3) | bob-cli-ir hood | completed 3 |
| [bob-cli-ir.6](bbugyi200.athena.bob-cli-ir.6.md) (session · 7) | bob-cli-ir hood | completed 6, failed 1 |
| [bob-cli-ir.7](bbugyi200.athena.bob-cli-ir.7.md) (session · 3) | bob-cli-ir hood | active 1, completed 2 |
| [bob-cli-ir.7.1.1](../agents/bbugyi200.athena.bob-cli-ir.7.1.1/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.7.1.2](../agents/bbugyi200.athena.bob-cli-ir.7.1.2/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.7.1.3](../agents/bbugyi200.athena.bob-cli-ir.7.1.3/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.7.1.4](../agents/bbugyi200.athena.bob-cli-ir.7.1.4/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.7.1.5](../agents/bbugyi200.athena.bob-cli-ir.7.1.5/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.7.1.land](bbugyi200.athena.bob-cli-ir.7.1.land.md) (session · 3) | bob-cli-ir hood | completed 3 |
| [bob-cli-ir.8](../agents/bbugyi200.athena.bob-cli-ir.8/README.md) | bob-cli-ir hood | completed |
| [bob-cli-ir.9](bbugyi200.athena.bob-cli-ir.9.md) (session · 5) | bob-cli-ir hood | completed 4, failed 1 |
| [bob-cli-ir.land](../agents/bbugyi200.athena.bob-cli-ir.land/README.md) | bob-cli-ir hood | waiting |
