# Session: bob-cli-hl.3.1.3

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-hl](../users/bbugyi200/machines/athena/hoods/bob-cli-hl/README.md) / bob-cli-hl.3.1.3

Owner: `bbugyi200.athena` · Hood: `bob-cli-hl` · Members: 4 · Bead: [bob-cli-hl.3.1.3](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-hl/bob-cli-hl.3.1.3.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-hl.3.1.3--mon [failed]"]
  n1["bob-cli-hl.3.1.3--mon-0 [active]"]
  n0 --> n1
  n2["bob-cli-hl.3.1.3--1 [completed]"]
  n0 --> n2
  n3["bob-cli-hl.3.1.3--plan [completed]"]
  n0 --> n3
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-mon"></a>mon | bob-cli-hl.3.1.3--mon | failed | gpt-6-luna / codex | 2026-11-06T02:44:03.421350+00:00 → 2026-11-06T02:48:40.668013+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-hl.3.1.3--mon/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-hl.3.1.3--mon-0 | active | gpt-6-luna / codex | 2026-11-06T03:02:40.796669+00:00 | 0 | — | — |
| <a id="member-1"></a>1 | bob-cli-hl.3.1.3--1 | completed | gpt-6-luna / codex | 2026-11-06T02:50:57.795618+00:00 → 2026-11-06T03:03:18.892525+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-hl.3.1.3--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-hl.3.1.3--1/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-hl.3.1.3--plan | completed | gpt-6-luna / codex | 2026-11-06T02:16:34.275050+00:00 → 2026-11-06T02:44:49.378226+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-hl.3.1.3--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-hl.3.1.3--plan/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-hl.3](bbugyi200.athena.bob-cli-hl.3.md) (session · 3) | ancestor | active 1, completed 2 |
| [bob-cli-hl.3.1.1](bbugyi200.athena.bob-cli-hl.3.1.1.md) (session · 5) | bob-cli-hl.3.1 hood | completed 3, failed 2 |
| [bob-cli-hl.3.1.2](../agents/bbugyi200.athena.bob-cli-hl.3.1.2/README.md) | bob-cli-hl.3.1 hood | completed |
| [bob-cli-hl.3.1.4](../agents/bbugyi200.athena.bob-cli-hl.3.1.4/README.md) | bob-cli-hl.3.1 hood | completed |
| [bob-cli-hl.3.1.5](../agents/bbugyi200.athena.bob-cli-hl.3.1.5/README.md) | bob-cli-hl.3.1 hood | waiting |
| [bob-cli-hl.3.1.land](../agents/bbugyi200.athena.bob-cli-hl.3.1.land/README.md) | bob-cli-hl.3.1 hood | waiting |
| [bob-cli-hl.1](../agents/bbugyi200.athena.bob-cli-hl.1/README.md) | bob-cli-hl hood | completed |
| [bob-cli-hl.2](bbugyi200.athena.bob-cli-hl.2.md) (session · 3) | bob-cli-hl hood | completed 3 |
| [bob-cli-hl.4](../agents/bbugyi200.athena.bob-cli-hl.4/README.md) | bob-cli-hl hood | completed |
| [bob-cli-hl.5](../agents/bbugyi200.athena.bob-cli-hl.5/README.md) | bob-cli-hl hood | waiting |
| [bob-cli-hl.6](../agents/bbugyi200.athena.bob-cli-hl.6/README.md) | bob-cli-hl hood | waiting |
| [bob-cli-hl.land](../agents/bbugyi200.athena.bob-cli-hl.land/README.md) | bob-cli-hl hood | waiting |
