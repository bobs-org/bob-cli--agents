# Session: bob-cli-ls.2.1.2

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-ls](../users/bbugyi200/machines/athena/hoods/bob-cli-ls/README.md) / bob-cli-ls.2.1.2

Owner: `bbugyi200.athena` · Hood: `bob-cli-ls` · Members: 5 · Bead: [bob-cli-ls.2.1.2](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ls/bob-cli-ls.2.1.2.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-ls.2.1.2--mon-0 [completed]"]
  n1["bob-cli-ls.2.1.2--mon [failed]"]
  n0 --> n1
  n2["bob-cli-ls.2.1.2--2 [completed]"]
  n0 --> n2
  n3["bob-cli-ls.2.1.2--plan [completed]"]
  n0 --> n3
  n4["bob-cli-ls.2.1.2--1 [completed]"]
  n0 --> n4
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-mon-0"></a>mon-0 | bob-cli-ls.2.1.2--mon-0 | completed | grok-4.6 / grok | 2026-11-15T20:39:04.038720+00:00 → 2026-11-15T20:50:51.875125+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-ls.2.1.2--mon-0/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-ls.2.1.2--mon | failed | grok-4.6 / grok | 2026-11-15T20:14:48.149275+00:00 → 2026-11-15T20:29:07.592402+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-ls.2.1.2--mon/chat.md) |
| <a id="member-2"></a>2 | bob-cli-ls.2.1.2--2 | completed | grok-4.6 / grok | 2026-11-15T20:51:25.957830+00:00 → 2026-11-15T21:09:19.589552+00:00 | [1](../agents/bbugyi200.athena.bob-cli-ls.2.1.2--2/README.md#commits) | [Prompt](../agents/bbugyi200.athena.bob-cli-ls.2.1.2--2/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-ls.2.1.2--2/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-ls.2.1.2--plan | completed | grok-4.6 / grok | 2026-11-15T19:39:19.789750+00:00 → 2026-11-15T20:16:40.057911+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-ls.2.1.2--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-ls.2.1.2--plan/chat.md) |
| <a id="member-1"></a>1 | bob-cli-ls.2.1.2--1 | completed | grok-4.6 / grok | 2026-11-15T20:29:49.352841+00:00 → 2026-11-15T20:40:42.442514+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-ls.2.1.2--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-ls.2.1.2--1/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| 2 | bob-cli | [`96b35f4`](https://github.com/bobs-org/bob-cli/commit/96b35f41c4d20cecc065e85e2fe5ac1d8d191c2c) | feat(bank): add subscription attribution and ledger | 2026-11-15 16:08:32 EST |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-ls.2](bbugyi200.athena.bob-cli-ls.2.md) (session · 3) | ancestor | active 1, completed 2 |
| [bob-cli-ls.2.1.1](bbugyi200.athena.bob-cli-ls.2.1.1.md) (session · 5) | bob-cli-ls.2.1 hood | completed 4, failed 1 |
| [bob-cli-ls.2.1.3](../agents/bbugyi200.athena.bob-cli-ls.2.1.3/README.md) | bob-cli-ls.2.1 hood | completed |
| [bob-cli-ls.2.1.land](bbugyi200.athena.bob-cli-ls.2.1.land.md) (session · 3) | bob-cli-ls.2.1 hood | completed 3 |
| [bob-cli-ls.1](bbugyi200.athena.bob-cli-ls.1.md) (session · 3) | bob-cli-ls hood | completed 3 |
| [bob-cli-ls.1](../agents/bbugyi200.athena.bob-cli-ls.1/README.md) | bob-cli-ls hood | active |
| [bob-cli-ls.10](../agents/bbugyi200.athena.bob-cli-ls.10/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.3](../agents/bbugyi200.athena.bob-cli-ls.3/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.4](../agents/bbugyi200.athena.bob-cli-ls.4/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.5](bbugyi200.athena.bob-cli-ls.5.md) (session · 2) | bob-cli-ls hood | active 1, completed 1 |
| [bob-cli-ls.6](../agents/bbugyi200.athena.bob-cli-ls.6/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.7](../agents/bbugyi200.athena.bob-cli-ls.7/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.8](../agents/bbugyi200.athena.bob-cli-ls.8/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.9](../agents/bbugyi200.athena.bob-cli-ls.9/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.land](../agents/bbugyi200.athena.bob-cli-ls.land/README.md) | bob-cli-ls hood | waiting |
