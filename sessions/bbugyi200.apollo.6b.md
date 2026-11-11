# Session: 6b

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [6b](../users/bbugyi200/machines/apollo/hoods/6b/README.md) / 6b

Owner: `bbugyi200.apollo` · Hood: `6b` · Members: 3

## Lineage

```mermaid
flowchart TD
  n0["6b--plan [dismissed]"]
  n1["6b--code [completed]"]
  n0 --> n1
  n2["6b--gate [failed]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-plan"></a>plan | 6b--plan | dismissed | gpt-6-astra / codex | 2026-10-10T09:40:18.268624 → 2026-10-10T09:54:45.004976 | 0 | [Prompt](../agents/bbugyi200.apollo.6b--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.6b--plan/chat.md) |
| <a id="member-code"></a>code | 6b--code | completed | grok-4.6 / grok | 2026-10-10T13:44:58.680450+00:00 → 2026-10-10T13:54:44.965937+00:00 | [1](../agents/bbugyi200.apollo.6b--code/README.md#commits) | — | — |
| <a id="member-gate"></a>gate | 6b--gate | failed | gpt-6-astra / codex | 2026-10-10T13:44:32.484325+00:00 → 2026-10-10T13:44:48.550611+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.6b--gate/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| — | — | `5db0e6a` | fix: address review findings across native workflows | 2026-07-11 19:09:56 EDT |
| code | — | `6c1969d` | docs(dashboard): move BLOCKED into the Browse row | 2026-10-10 09:53:08 EDT |
