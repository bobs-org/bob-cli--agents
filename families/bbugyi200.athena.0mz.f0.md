# Family: 0mz.f0

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [0mz](../users/bbugyi200/machines/athena/hoods/0mz/README.md) / 0mz.f0

Owner: `bbugyi200.athena` · Hood: `0mz` · Members: 3

## Lineage

```mermaid
flowchart TD
  n0["0mz.f0--plan [completed]"]
  n1["0mz.f0--code [active]"]
  n0 --> n1
  n2["0mz.f0--gate [failed]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-plan"></a>plan | 0mz.f0--plan | completed | gpt-5.6-sol / codex | 2026-09-18T16:08:45.354893+00:00 → 2026-09-18T16:18:02.629912+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.0mz.f0--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.0mz.f0--plan/chat.md) |
| <a id="member-code"></a>code | 0mz.f0--code | active | grok-4.6 / grok | 2026-09-18T16:20:08.027479+00:00 | [1](../agents/bbugyi200.athena.0mz.f0--code/README.md#commits) | [Prompt](../agents/bbugyi200.athena.0mz.f0--code/prompt.md) | — |
| <a id="member-gate"></a>gate | 0mz.f0--gate | failed | gpt-5.6-sol / codex | 2026-09-18T16:18:46.416939+00:00 → 2026-09-18T16:19:30.838168+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.0mz.f0--gate/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| code | bob-cli | [`a72b355`](https://github.com/bobs-org/bob-cli/commit/a72b3550d1ec8417412082c8625a651b2550627e) | feat(capture): add @route+block-id! force-Next Task Link relocation | 2026-09-18 13:04:27 EDT |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [0mz](bbugyi200.athena.0mz.md) (family · 3) | ancestor | completed 2, failed 1 |
