# Session: bob-cli-oj.3.1.land

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-oj](../users/bbugyi200/machines/athena/hoods/bob-cli-oj/README.md) / bob-cli-oj.3.1.land

Owner: `bbugyi200.athena` · Hood: `bob-cli-oj` · Members: 3 · Bead: [bob-cli-oj.3.1](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-oj/bob-cli-oj.3.1.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-oj.3.1.land--gate [completed]"]
  n1["bob-cli-oj.3.1.land--code [active]"]
  n0 --> n1
  n2["bob-cli-oj.3.1.land--plan [active]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-gate"></a>gate | bob-cli-oj.3.1.land--gate | completed | gpt-6-astra / codex | 2026-11-21T15:26:04.545731+00:00 → 2026-11-21T15:26:11.585847+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-oj.3.1.land--gate/chat.md) |
| <a id="member-code"></a>code | bob-cli-oj.3.1.land--code | active | grok-4.6 / grok | 2026-11-21T15:26:45.186939+00:00 | 0 | — | — |
| <a id="member-plan"></a>plan | bob-cli-oj.3.1.land--plan | active | gpt-6-astra / codex | 2026-11-21T15:16:45.384941+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-oj.3.1.land--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-oj.3.1.land--plan/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-oj.3](bbugyi200.athena.bob-cli-oj.3.md) (session · 3) | ancestor | active 1, completed 2 |
| [bob-cli-oj.3.1.1](../agents/bbugyi200.athena.bob-cli-oj.3.1.1/README.md) | bob-cli-oj.3.1 hood | completed |
| [bob-cli-oj.3.1.2](bbugyi200.athena.bob-cli-oj.3.1.2.md) (session · 5) | bob-cli-oj.3.1 hood | completed 4, failed 1 |
| [bob-cli-oj.3.1.3](../agents/bbugyi200.athena.bob-cli-oj.3.1.3/README.md) | bob-cli-oj.3.1 hood | completed |
| [bob-cli-oj.3.1.4](../agents/bbugyi200.athena.bob-cli-oj.3.1.4/README.md) | bob-cli-oj.3.1 hood | completed |
| [bob-cli-oj.1](bbugyi200.athena.bob-cli-oj.1.md) (session · 6) | bob-cli-oj hood | active 1, completed 4, failed 1 |
| [bob-cli-oj.2](../agents/bbugyi200.athena.bob-cli-oj.2/README.md) | bob-cli-oj hood | completed |
| [bob-cli-oj.4](../agents/bbugyi200.athena.bob-cli-oj.4/README.md) | bob-cli-oj hood | waiting |
| [bob-cli-oj.5](../agents/bbugyi200.athena.bob-cli-oj.5/README.md) | bob-cli-oj hood | waiting |
| [bob-cli-oj.6](../agents/bbugyi200.athena.bob-cli-oj.6/README.md) | bob-cli-oj hood | waiting |
| [bob-cli-oj.7](../agents/bbugyi200.athena.bob-cli-oj.7/README.md) | bob-cli-oj hood | waiting |
| [bob-cli-oj.8](../agents/bbugyi200.athena.bob-cli-oj.8/README.md) | bob-cli-oj hood | waiting |
| [bob-cli-oj.land](../agents/bbugyi200.athena.bob-cli-oj.land/README.md) | bob-cli-oj hood | waiting |
