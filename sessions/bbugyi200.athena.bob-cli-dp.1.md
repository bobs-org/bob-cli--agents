# Session: bob-cli-dp.1

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-dp](../users/bbugyi200/machines/athena/hoods/bob-cli-dp/README.md) / bob-cli-dp.1

Owner: `bbugyi200.athena` · Hood: `bob-cli-dp` · Members: 3 · Bead: [bob-cli-dp.1](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-dp/bob-cli-dp.1.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-dp.1--plan [active]"]
  n1["bob-cli-dp.1--code [active]"]
  n0 --> n1
  n2["bob-cli-dp.1--gate [failed]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-plan"></a>plan | bob-cli-dp.1--plan | active | opus / claude | 2026-10-28T17:11:10.510701+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-dp.1--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-dp.1--plan/chat.md) |
| <a id="member-code"></a>code | bob-cli-dp.1--code | active | grok-4.6 / grok | 2026-10-28T17:25:50.693755+00:00 | 0 | — | — |
| <a id="member-gate"></a>gate | bob-cli-dp.1--gate | failed | opus / claude | 2026-10-28T17:23:29.354689+00:00 → 2026-10-28T17:25:04.618350+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-dp.1--gate/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-dp.2](bbugyi200.athena.bob-cli-dp.2.md) (session · 3) | bob-cli-dp hood | completed 2, failed 1 |
| [bob-cli-dp.3](../agents/bbugyi200.athena.bob-cli-dp.3/README.md) | bob-cli-dp hood | completed |
| [bob-cli-dp.4](bbugyi200.athena.bob-cli-dp.4.md) (session · 7) | bob-cli-dp hood | completed 4, failed 3 |
| [bob-cli-dp.land](../agents/bbugyi200.athena.bob-cli-dp.land/README.md) | bob-cli-dp hood | waiting |
