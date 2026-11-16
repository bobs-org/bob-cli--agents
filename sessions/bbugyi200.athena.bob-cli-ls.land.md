# Session: bob-cli-ls.land

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-ls](../users/bbugyi200/machines/athena/hoods/bob-cli-ls/README.md) / bob-cli-ls.land

Owner: `bbugyi200.athena` · Hood: `bob-cli-ls` · Members: 7 · Bead: [bob-cli-ls](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ls/README.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-ls.land--plan [completed]"]
  n1["bob-cli-ls.land--code [completed]"]
  n0 --> n1
  n2["bob-cli-ls.land--mon [failed]"]
  n0 --> n2
  n3["bob-cli-ls.land--1 [completed]"]
  n0 --> n3
  n4["bob-cli-ls.land--gate [completed]"]
  n0 --> n4
  n5["bob-cli-ls.land--mon-0 [failed]"]
  n0 --> n5
  n6["bob-cli-ls.land--2 [active]"]
  n0 --> n6
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-plan"></a>plan | bob-cli-ls.land--plan | completed | opus / claude | 2026-11-16T03:20:00.162688+00:00 → 2026-11-16T04:30:11.496965+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-ls.land--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-ls.land--plan/chat.md) |
| <a id="member-code"></a>code | bob-cli-ls.land--code | completed | gpt-6-luna / codex | 2026-11-16T04:00:22.140342+00:00 → 2026-11-16T04:30:11.496965+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-ls.land--code/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-ls.land--mon | failed | gpt-6-luna / codex | 2026-11-16T04:29:00.967993+00:00 → 2026-11-16T04:32:40.929107+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-ls.land--mon/chat.md) |
| <a id="member-1"></a>1 | bob-cli-ls.land--1 | completed | gpt-6-luna / codex | 2026-11-16T04:33:33.799907+00:00 → 2026-11-16T04:50:49.803852+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-ls.land--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-ls.land--1/chat.md) |
| <a id="member-gate"></a>gate | bob-cli-ls.land--gate | completed | opus / claude | 2026-11-16T03:59:34.159518+00:00 → 2026-11-16T03:59:48.781934+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-ls.land--gate/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-ls.land--mon-0 | failed | gpt-6-luna / codex | 2026-11-16T04:49:32.622637+00:00 → 2026-11-16T04:55:45.215730+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-ls.land--mon-0/chat.md) |
| <a id="member-2"></a>2 | bob-cli-ls.land--2 | active | muse-spark-1.3-contributor / muse | 2026-11-16T04:56:32.729649+00:00 | [1](../agents/bbugyi200.athena.bob-cli-ls.land--2/README.md#commits) | [Prompt](../agents/bbugyi200.athena.bob-cli-ls.land--2/prompt.md) | — |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| 2 | bob-cli | [`5dec7c5`](https://github.com/bobs-org/bob-cli/commit/5dec7c52c22729c2a566cb7ea178859943eb2e93) | fix(bank): land subscription gaps from the landing review | 2026-11-16 01:06:31 EST |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-ls.1](bbugyi200.athena.bob-cli-ls.1.md) (session · 3) | bob-cli-ls hood | completed 3 |
| [bob-cli-ls.1](../agents/bbugyi200.athena.bob-cli-ls.1/README.md) | bob-cli-ls hood | active |
| [bob-cli-ls.10](../agents/bbugyi200.athena.bob-cli-ls.10/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.2](bbugyi200.athena.bob-cli-ls.2.md) (session · 3) | bob-cli-ls hood | active 1, completed 2 |
| [bob-cli-ls.2.1.1](bbugyi200.athena.bob-cli-ls.2.1.1.md) (session · 5) | bob-cli-ls hood | completed 4, failed 1 |
| [bob-cli-ls.2.1.2](bbugyi200.athena.bob-cli-ls.2.1.2.md) (session · 5) | bob-cli-ls hood | completed 4, failed 1 |
| [bob-cli-ls.2.1.3](../agents/bbugyi200.athena.bob-cli-ls.2.1.3/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.2.1.land](bbugyi200.athena.bob-cli-ls.2.1.land.md) (session · 3) | bob-cli-ls hood | completed 3 |
| [bob-cli-ls.3](../agents/bbugyi200.athena.bob-cli-ls.3/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.4](../agents/bbugyi200.athena.bob-cli-ls.4/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.5](bbugyi200.athena.bob-cli-ls.5.md) (session · 3) | bob-cli-ls hood | completed 2, failed 1 |
| [bob-cli-ls.6](../agents/bbugyi200.athena.bob-cli-ls.6/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.7](../agents/bbugyi200.athena.bob-cli-ls.7/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.8](bbugyi200.athena.bob-cli-ls.8.md) (session · 5) | bob-cli-ls hood | completed 4, failed 1 |
| [bob-cli-ls.9](../agents/bbugyi200.athena.bob-cli-ls.9/README.md) | bob-cli-ls hood | completed |
