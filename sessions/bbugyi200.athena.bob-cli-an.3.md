# Session: bob-cli-an.3

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-an](../users/bbugyi200/machines/athena/hoods/bob-cli-an/README.md) / bob-cli-an.3

Owner: `bbugyi200.athena` · Hood: `bob-cli-an` · Members: 3 · Bead: [bob-cli-an.3](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-an/bob-cli-an.3.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-an.3--plan [completed]"]
  n1["bob-cli-an.3--1 [active]"]
  n0 --> n1
  n2["bob-cli-an.3--mon [failed]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-plan"></a>plan | bob-cli-an.3--plan | completed | gpt-6-luna / codex | 2026-10-22T10:42:25.895458+00:00 → 2026-10-22T10:53:22.410066+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-an.3--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-an.3--plan/chat.md) |
| <a id="member-1"></a>1 | bob-cli-an.3--1 | active | gpt-6-luna / codex | 2026-10-22T10:56:15.545260+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-an.3--1/prompt.md) | — |
| <a id="member-mon"></a>mon | bob-cli-an.3--mon | failed | gpt-6-luna / codex | 2026-10-22T10:52:33.405714+00:00 → 2026-10-22T10:55:19.548131+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-an.3--mon/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-an.1](bbugyi200.athena.bob-cli-an.1.md) (session · 7) | bob-cli-an hood | completed 4, failed 3 |
| [bob-cli-an.2](bbugyi200.athena.bob-cli-an.2.md) (session · 7) | bob-cli-an hood | completed 4, failed 3 |
| [bob-cli-an.4](../agents/bbugyi200.athena.bob-cli-an.4/README.md) | bob-cli-an hood | active |
| [bob-cli-an.5](../agents/bbugyi200.athena.bob-cli-an.5/README.md) | bob-cli-an hood | completed |
| [bob-cli-an.land](../agents/bbugyi200.athena.bob-cli-an.land/README.md) | bob-cli-an hood | waiting |
