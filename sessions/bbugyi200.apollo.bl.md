# Session: bl

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [bl](../users/bbugyi200/machines/apollo/hoods/bl/README.md) / bl

Owner: `bbugyi200.apollo` · Hood: `bl` · Members: 3

## Lineage

```mermaid
flowchart TD
  n0["bl--code [completed]"]
  n1["bl--gate [completed]"]
  n0 --> n1
  n2["bl--plan [dismissed]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-code"></a>code | bl--code | completed | grok-4.6 / grok | 2026-10-31T01:30:44.482916+00:00 → 2026-10-31T02:26:15.286174+00:00 | [1](../agents/bbugyi200.apollo.bl--code/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.bl--code/prompt.md) | [Chat](../agents/bbugyi200.apollo.bl--code/chat.md) |
| <a id="member-gate"></a>gate | bl--gate | completed | opus / claude | 2026-10-31T01:29:51.293479+00:00 → 2026-10-31T01:30:29.602174+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bl--gate/chat.md) |
| <a id="member-plan"></a>plan | bl--plan | dismissed | opus / claude | 2026-10-30T20:32:01.163939 → 2026-10-30T20:46:29.602316 | 0 | [Prompt](../agents/bbugyi200.apollo.bl--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.bl--plan/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| code | — | `e9c62ae` | feat(gcal): link new Event Tasks under MEET by phase | 2026-10-30 22:25:55 EDT |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bl.w0](bbugyi200.apollo.bl.w0.md) (session · 3) | descendant | completed 2, dismissed 1 |
