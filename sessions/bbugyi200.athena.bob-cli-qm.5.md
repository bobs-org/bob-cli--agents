# Session: bob-cli-qm.5

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-qm](../users/bbugyi200/machines/athena/hoods/bob-cli-qm/README.md) / bob-cli-qm.5

Owner: `bbugyi200.athena` · Hood: `bob-cli-qm` · Members: 7 · Bead: [bob-cli-qm.5](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-qm/bob-cli-qm.5.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-qm.5--mon [completed]"]
  n1["bob-cli-qm.5--1 [completed]"]
  n0 --> n1
  n2["bob-cli-qm.5--2 [completed]"]
  n0 --> n2
  n3["bob-cli-qm.5--mon-0 [failed]"]
  n0 --> n3
  n4["bob-cli-qm.5--mon-1 [completed]"]
  n0 --> n4
  n5["bob-cli-qm.5--plan [completed]"]
  n0 --> n5
  n6["bob-cli-qm.5--3 [completed]"]
  n0 --> n6
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-mon"></a>mon | bob-cli-qm.5--mon | completed | gpt-6-luna / codex | 2026-11-26T19:35:52.782747+00:00 → 2026-11-26T21:00:14.222427+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-qm.5--mon/chat.md) |
| <a id="member-1"></a>1 | bob-cli-qm.5--1 | completed | gpt-6-luna / codex | 2026-11-26T21:00:13.697126+00:00 → 2026-11-26T21:38:25.946321+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-qm.5--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-qm.5--1/chat.md) |
| <a id="member-2"></a>2 | bob-cli-qm.5--2 | completed | gpt-6-luna / codex | 2026-11-26T21:41:02.973477+00:00 → 2026-11-26T21:47:34.221646+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-qm.5--2/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-qm.5--2/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-qm.5--mon-0 | failed | gpt-6-luna / codex | 2026-11-26T21:37:02.175225+00:00 → 2026-11-26T21:41:03.461871+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-qm.5--mon-0/chat.md) |
| <a id="member-mon-1"></a>mon-1 | bob-cli-qm.5--mon-1 | completed | gpt-6-luna / codex | 2026-11-26T21:46:54.922990+00:00 → 2026-11-26T21:49:39.646379+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-qm.5--mon-1/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-qm.5--plan | completed | gpt-6-luna / codex | 2026-11-26T19:30:04.018830+00:00 → 2026-11-26T19:36:59.571585+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-qm.5--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-qm.5--plan/chat.md) |
| <a id="member-3"></a>3 | bob-cli-qm.5--3 | completed | gpt-6-luna / codex | 2026-11-26T21:49:39.494925+00:00 → 2026-11-26T21:54:12.785832+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-qm.5--3/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-qm.5--3/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-qm.1](../agents/bbugyi200.athena.bob-cli-qm.1/README.md) | bob-cli-qm hood | completed |
| [bob-cli-qm.2](bbugyi200.athena.bob-cli-qm.2.md) (session · 5) | bob-cli-qm hood | completed 3, failed 2 |
| [bob-cli-qm.3](bbugyi200.athena.bob-cli-qm.3.md) (session · 9) | bob-cli-qm hood | completed 9 |
| [bob-cli-qm.4](../agents/bbugyi200.athena.bob-cli-qm.4/README.md) | bob-cli-qm hood | completed |
| [bob-cli-qm.6](../agents/bbugyi200.athena.bob-cli-qm.6/README.md) | bob-cli-qm hood | completed |
| [bob-cli-qm.7](bbugyi200.athena.bob-cli-qm.7.md) (session · 4) | bob-cli-qm hood | active 2, completed 2 |
| [bob-cli-qm.land](../agents/bbugyi200.athena.bob-cli-qm.land/README.md) | bob-cli-qm hood | waiting |
