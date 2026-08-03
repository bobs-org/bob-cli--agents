# Family: ad

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [ad](../users/bbugyi200/machines/athena/hoods/ad/README.md) / ad

Owner: `bbugyi200.athena` · Hood: `ad` · Members: 2

## Lineage

```mermaid
flowchart TD
  n0["ad [active]"]
  n1["ad--code [completed]"]
  n0 --> n1
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-root"></a>root | ad | active | gpt-5.6-sol / codex | 2026-07-16T14:39:09.442711+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.ad/prompt.md) | [Chat](../agents/bbugyi200.athena.ad/chat.md) |
| <a id="member-code"></a>code | ad--code | completed | gpt-5.6-sol / codex | 2026-07-16T14:47:41.080869+00:00 | [1](../agents/bbugyi200.athena.ad--code/README.md#commits) | — | [Chat](../agents/bbugyi200.athena.ad--code/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| code | bob-cli | [`fc39562`](https://github.com/bobs-org/bob-cli/commit/fc39562c3d7dc5fb07501a5a139237df8fe9996f) | feat: reconcile dependency-blocked task statuses | 2026-07-16 11:17:03 EDT |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [ad.f0](../agents/bbugyi200.athena.ad.f0/README.md) | descendant | active |
| [ad.f1](../agents/bbugyi200.athena.ad.f1/README.md) | descendant | waiting |
| [ad.f2](bbugyi200.athena.ad.f2.md) (family · 2) | descendant | active 1, completed 1 |
