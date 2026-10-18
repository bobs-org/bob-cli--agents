# Session: 11g

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [11g](../users/bbugyi200/machines/athena/hoods/11g/README.md) / 11g

Owner: `bbugyi200.athena` · Hood: `11g` · Members: 3

## Lineage

```mermaid
flowchart TD
  n0["11g--code [active]"]
  n1["11g--gate [failed]"]
  n0 --> n1
  n2["11g--plan [active]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-code"></a>code | 11g--code | active | sonnet / claude | 2026-10-18T17:34:59.356911+00:00 | [1](../agents/bbugyi200.athena.11g--code/README.md#commits) | — | — |
| <a id="member-gate"></a>gate | 11g--gate | failed | opus / claude | 2026-10-18T17:34:09.669508+00:00 → 2026-10-18T17:34:36.890201+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.11g--gate/chat.md) |
| <a id="member-plan"></a>plan | 11g--plan | active | opus / claude | 2026-10-18T17:29:46.787078+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.11g--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.11g--plan/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| code | bob-cli | [`674c9f5`](https://github.com/bobs-org/bob-cli/commit/674c9f55bc7a8fe4c536701592396ddcfb5da049) | docs(work-badges): retune color thresholds to 40/60/80 | 2026-10-18 13:39:26 EDT |
