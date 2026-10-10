# Session: 6g.w1

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [6g](../users/bbugyi200/machines/apollo/hoods/6g/README.md) / 6g.w1

Owner: `bbugyi200.apollo` · Hood: `6g` · Members: 7

## Lineage

```mermaid
flowchart TD
  n0["6g.w1--plan [completed]"]
  n1["6g.w1--code [completed]"]
  n0 --> n1
  n2["6g.w1--mon [failed]"]
  n0 --> n2
  n3["6g.w1--2 [completed]"]
  n0 --> n3
  n4["6g.w1--1 [completed]"]
  n0 --> n4
  n5["6g.w1--mon-0 [failed]"]
  n0 --> n5
  n6["6g.w1--gate [failed]"]
  n0 --> n6
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-plan"></a>plan | 6g.w1--plan | completed | gpt-6-astra / codex | 2026-10-10T17:31:16.864983+00:00 → 2026-10-10T17:52:52.772176+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.6g.w1--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.6g.w1--plan/chat.md) |
| <a id="member-code"></a>code | 6g.w1--code | completed | gpt-6-luna / codex | 2026-10-10T17:36:10.046827+00:00 → 2026-10-10T17:52:52.772176+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.6g.w1--code/chat.md) |
| <a id="member-mon"></a>mon | 6g.w1--mon | failed | gpt-6-luna / codex | 2026-10-10T17:51:46.097876+00:00 → 2026-10-10T17:57:26.247186+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.6g.w1--mon/chat.md) |
| <a id="member-2"></a>2 | 6g.w1--2 | completed | gpt-6-luna / codex | 2026-10-10T18:06:11.641788+00:00 → 2026-10-10T18:08:39.096498+00:00 | [1](../agents/bbugyi200.apollo.6g.w1--2/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.6g.w1--2/prompt.md) | [Chat](../agents/bbugyi200.apollo.6g.w1--2/chat.md) |
| <a id="member-1"></a>1 | 6g.w1--1 | completed | gpt-6-luna / codex | 2026-10-10T17:57:25.746859+00:00 → 2026-10-10T18:02:00.680689+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.6g.w1--1/prompt.md) | [Chat](../agents/bbugyi200.apollo.6g.w1--1/chat.md) |
| <a id="member-mon-0"></a>mon-0 | 6g.w1--mon-0 | failed | gpt-6-luna / codex | 2026-10-10T18:01:05.966556+00:00 → 2026-10-10T18:06:12.012005+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.6g.w1--mon-0/chat.md) |
| <a id="member-gate"></a>gate | 6g.w1--gate | failed | gpt-6-astra / codex | 2026-10-10T17:35:41.960247+00:00 → 2026-10-10T17:35:56.860775+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.6g.w1--gate/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| 2 | bob-cli | [`60297c2`](https://github.com/bobs-org/bob-cli/commit/60297c2621478beca362bc0e8b5abe32d92a9147) | feat(capture): add idle agenda budget output | 2026-10-10 14:07:07 EDT |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [6g](bbugyi200.apollo.6g.md) (session · 3) | ancestor | completed 2, failed 1 |
| [6g.w1.w0](bbugyi200.apollo.6g.w1.w0.md) (session · 3) | descendant | completed 2, failed 1 |
| [6g.w1.w0.f0](bbugyi200.apollo.6g.w1.w0.f0.md) (session · 5) | descendant | active 1, completed 2, failed 2 |
| [6g.w1.w0.f0.w0](bbugyi200.apollo.6g.w1.w0.f0.w0.md) (session · 3) | descendant | completed 2, failed 1 |
| [6g.w0](../agents/bbugyi200.apollo.6g.w0/README.md) | 6g hood | active |
