# Session: bob-cli-df.2.1.4.3.2

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-df](../users/bbugyi200/machines/athena/hoods/bob-cli-df/README.md) / bob-cli-df.2.1.4.3.2

Owner: `bbugyi200.athena` · Hood: `bob-cli-df` · Members: 5 · Bead: [bob-cli-df.2.1.4.3.2](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-df/bob-cli-df.2.1.4.3.2.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-df.2.1.4.3.2--mon [failed]"]
  n1["bob-cli-df.2.1.4.3.2--mon-0 [failed]"]
  n0 --> n1
  n2["bob-cli-df.2.1.4.3.2--1 [completed]"]
  n0 --> n2
  n3["bob-cli-df.2.1.4.3.2--2 [completed]"]
  n0 --> n3
  n4["bob-cli-df.2.1.4.3.2--plan [completed]"]
  n0 --> n4
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-mon"></a>mon | bob-cli-df.2.1.4.3.2--mon | failed | grok-4.6 / grok | 2026-10-28T10:04:16.796393+00:00 → 2026-10-28T10:07:12.693743+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.2--mon/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-df.2.1.4.3.2--mon-0 | failed | grok-4.6 / grok | 2026-10-28T10:15:04.334076+00:00 → 2026-10-28T10:23:21.625594+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.2--mon-0/chat.md) |
| <a id="member-1"></a>1 | bob-cli-df.2.1.4.3.2--1 | completed | grok-4.6 / grok | 2026-10-28T10:08:23.206488+00:00 → 2026-10-28T10:15:40.637354+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.2--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.2--1/chat.md) |
| <a id="member-2"></a>2 | bob-cli-df.2.1.4.3.2--2 | completed | grok-4.6 / grok | 2026-10-28T10:24:27.611869+00:00 → 2026-10-28T10:42:53.574850+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.2--2/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.2--2/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-df.2.1.4.3.2--plan | completed | grok-4.6 / grok | 2026-10-28T09:20:47.110151+00:00 → 2026-10-28T10:05:11.170244+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.2--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.2--plan/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-df.2](bbugyi200.athena.bob-cli-df.2.md) (session · 3) | ancestor | failed 3 |
| [bob-cli-df.2.1.4.3.1](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.1/README.md) | bob-cli-df.2.1.4.3 hood | completed |
| [bob-cli-df.2.1.4.3.3.1](bbugyi200.athena.bob-cli-df.2.1.4.3.3.1.md) (session · 7) | bob-cli-df.2.1.4.3 hood | completed 4, failed 3 |
| [bob-cli-df.2.1.4.3.3.2](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.3.2/README.md) | bob-cli-df.2.1.4.3 hood | active |
| [bob-cli-df.2.1.4.3.3.land](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.3.land/README.md) | bob-cli-df.2.1.4.3 hood | waiting |
| [bob-cli-df.2.1.4.3.land](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.land/README.md) | bob-cli-df.2.1.4.3 hood | completed |
| [bob-cli-df.2.1.4.1](bbugyi200.athena.bob-cli-df.2.1.4.1.md) (session · 11) | bob-cli-df.2.1.4 hood | active 11 |
| [bob-cli-df.2.1.4.2](bbugyi200.athena.bob-cli-df.2.1.4.2.md) (session · 3) | bob-cli-df.2.1.4 hood | active 3 |
| [bob-cli-df.2.1.4.land](bbugyi200.athena.bob-cli-df.2.1.4.land.md) (session · 3) | bob-cli-df.2.1.4 hood | active 3 |
| [bob-cli-df.2.1.1](../agents/bbugyi200.athena.bob-cli-df.2.1.1/README.md) | bob-cli-df.2.1 hood | active |
| [bob-cli-df.2.1.2](../agents/bbugyi200.athena.bob-cli-df.2.1.2/README.md) | bob-cli-df.2.1 hood | active |
| [bob-cli-df.2.1.3](bbugyi200.athena.bob-cli-df.2.1.3.md) (session · 9) | bob-cli-df.2.1 hood | active 9 |
| [bob-cli-df.2.1.land](bbugyi200.athena.bob-cli-df.2.1.land.md) (session · 3) | bob-cli-df.2.1 hood | active 3 |
| [bob-cli-df.1](../agents/bbugyi200.athena.bob-cli-df.1/README.md) | bob-cli-df hood | completed |
| [bob-cli-df.3](../agents/bbugyi200.athena.bob-cli-df.3/README.md) | bob-cli-df hood | completed |
| [bob-cli-df.4](bbugyi200.athena.bob-cli-df.4.md) (session · 3) | bob-cli-df hood | failed 3 |
| [bob-cli-df.4.1.1](bbugyi200.athena.bob-cli-df.4.1.1.md) (session · 3) | bob-cli-df hood | active 3 |
| [bob-cli-df.4.1.2](bbugyi200.athena.bob-cli-df.4.1.2.md) (session · 3) | bob-cli-df hood | active 3 |
| [bob-cli-df.4.1.3](../agents/bbugyi200.athena.bob-cli-df.4.1.3/README.md) | bob-cli-df hood | active |
| [bob-cli-df.4.1.4](bbugyi200.athena.bob-cli-df.4.1.4.md) (session · 3) | bob-cli-df hood | active 3 |
| [bob-cli-df.4.1.land](bbugyi200.athena.bob-cli-df.4.1.land.md) (session · 3) | bob-cli-df hood | active 2, completed 1 |
| [bob-cli-df.land](../agents/bbugyi200.athena.bob-cli-df.land/README.md) | bob-cli-df hood | waiting |
