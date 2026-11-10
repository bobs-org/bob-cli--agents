# Session: ct.f0.f0.f1

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [ct](../users/bbugyi200/machines/apollo/hoods/ct/README.md) / ct.f0.f0.f1

Owner: `bbugyi200.apollo` · Hood: `ct` · Members: 3

## Lineage

```mermaid
flowchart TD
  n0["ct.f0.f0.f1--gate [completed]"]
  n1["ct.f0.f0.f1--1 [completed]"]
  n0 --> n1
  n2["ct.f0.f0.f1--0 [completed]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-gate"></a>gate | ct.f0.f0.f1--gate | completed | opus / claude | 2026-11-07T09:52:53.634870+00:00 → 2026-11-07T09:53:18.563358+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.ct.f0.f0.f1--gate/chat.md) |
| <a id="member-1"></a>1 | ct.f0.f0.f1--1 | completed | opus / claude | 2026-11-07T09:54:03.324946+00:00 → 2026-11-07T10:31:09.861521+00:00 | [1](../agents/bbugyi200.apollo.ct.f0.f0.f1--1/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.ct.f0.f0.f1--1/prompt.md) | [Chat](../agents/bbugyi200.apollo.ct.f0.f0.f1--1/chat.md) |
| <a id="member-0"></a>0 | ct.f0.f0.f1--0 | completed | opus / claude | 2026-11-07T09:11:20.016176+00:00 → 2026-11-07T09:45:02.845089+00:00 | [1](../agents/bbugyi200.apollo.ct.f0.f0.f1--0/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.ct.f0.f0.f1--0/prompt.md) | [Chat](../agents/bbugyi200.apollo.ct.f0.f0.f1--0/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| 0 | — | `ce81e2a` | fix(gmail): add compose to a read-only grant and parse empty headers | 2026-11-07 04:44:30 EST |
| 1 | — | `dbd30ec` | fix(gmail): read back gog 0.47.1 drafts and reply to your own sent mail | 2026-11-07 05:30:58 EST |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [ct.f0.f0](bbugyi200.apollo.ct.f0.f0.md) (session · 5) | ancestor | completed 5 |
| [ct.f0.f0.f0](../agents/bbugyi200.apollo.ct.f0.f0.f0/README.md) | ct.f0.f0 hood | dismissed |
