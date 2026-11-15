# Session: bob-cli-ls.2.1.1

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-ls](../users/bbugyi200/machines/athena/hoods/bob-cli-ls/README.md) / bob-cli-ls.2.1.1

Owner: `bbugyi200.athena` · Hood: `bob-cli-ls` · Members: 5 · Bead: [bob-cli-ls.2.1.1](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ls/bob-cli-ls.2.1.1.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-ls.2.1.1--1 [completed]"]
  n1["bob-cli-ls.2.1.1--plan [completed]"]
  n0 --> n1
  n2["bob-cli-ls.2.1.1--gate [completed]"]
  n0 --> n2
  n3["bob-cli-ls.2.1.1--2 [completed]"]
  n0 --> n3
  n4["bob-cli-ls.2.1.1--mon [failed]"]
  n0 --> n4
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-1"></a>1 | bob-cli-ls.2.1.1--1 | completed | gpt-6-luna / codex | 2026-11-15T18:50:38.267144+00:00 → 2026-11-15T18:58:09.885968+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-ls.2.1.1--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-ls.2.1.1--1/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-ls.2.1.1--plan | completed | gpt-6-luna / codex | 2026-11-15T18:29:03.695399+00:00 → 2026-11-15T18:45:38.539531+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-ls.2.1.1--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-ls.2.1.1--plan/chat.md) |
| <a id="member-gate"></a>gate | bob-cli-ls.2.1.1--gate | completed | gpt-6-luna / codex | 2026-11-15T19:34:13.528424+00:00 → 2026-11-15T19:35:03.876268+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-ls.2.1.1--gate/chat.md) |
| <a id="member-2"></a>2 | bob-cli-ls.2.1.1--2 | completed | gpt-6-luna / codex | 2026-11-15T19:36:21.760110+00:00 → 2026-11-15T19:38:26.652546+00:00 | [1](../agents/bbugyi200.athena.bob-cli-ls.2.1.1--2/README.md#commits) | [Prompt](../agents/bbugyi200.athena.bob-cli-ls.2.1.1--2/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-ls.2.1.1--2/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-ls.2.1.1--mon | failed | gpt-6-luna / codex | 2026-11-15T18:44:18.921752+00:00 → 2026-11-15T18:50:10.069364+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-ls.2.1.1--mon/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| 2 | bob-cli | [`c59b5b8`](https://github.com/bobs-org/bob-cli/commit/c59b5b805f67d4011b6d7f41cb3d6b187ce925e9) | feat(bank): add subscription registry and matching | 2026-11-15 14:38:05 EST |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-ls.2](bbugyi200.athena.bob-cli-ls.2.md) (session · 3) | ancestor | active 1, completed 2 |
| [bob-cli-ls.2.1.2](bbugyi200.athena.bob-cli-ls.2.1.2.md) (session · 5) | bob-cli-ls.2.1 hood | completed 4, failed 1 |
| [bob-cli-ls.2.1.3](../agents/bbugyi200.athena.bob-cli-ls.2.1.3/README.md) | bob-cli-ls.2.1 hood | completed |
| [bob-cli-ls.2.1.land](bbugyi200.athena.bob-cli-ls.2.1.land.md) (session · 3) | bob-cli-ls.2.1 hood | completed 3 |
| [bob-cli-ls.1](bbugyi200.athena.bob-cli-ls.1.md) (session · 3) | bob-cli-ls hood | completed 3 |
| [bob-cli-ls.1](../agents/bbugyi200.athena.bob-cli-ls.1/README.md) | bob-cli-ls hood | active |
| [bob-cli-ls.10](../agents/bbugyi200.athena.bob-cli-ls.10/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.3](../agents/bbugyi200.athena.bob-cli-ls.3/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.4](../agents/bbugyi200.athena.bob-cli-ls.4/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.5](bbugyi200.athena.bob-cli-ls.5.md) (session · 3) | bob-cli-ls hood | completed 2, failed 1 |
| [bob-cli-ls.6](../agents/bbugyi200.athena.bob-cli-ls.6/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.7](../agents/bbugyi200.athena.bob-cli-ls.7/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.8](../agents/bbugyi200.athena.bob-cli-ls.8/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.9](../agents/bbugyi200.athena.bob-cli-ls.9/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.land](../agents/bbugyi200.athena.bob-cli-ls.land/README.md) | bob-cli-ls hood | waiting |
