# Session: bob-cli-on.11.1.3

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-on](../users/bbugyi200/machines/athena/hoods/bob-cli-on/README.md) / bob-cli-on.11.1.3

Owner: `bbugyi200.athena` · Hood: `bob-cli-on` · Members: 5 · Bead: [bob-cli-on.11.1.3](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-on/bob-cli-on.11.1.3.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-on.11.1.3--1 [completed]"]
  n1["bob-cli-on.11.1.3--plan [completed]"]
  n0 --> n1
  n2["bob-cli-on.11.1.3--2 [completed]"]
  n0 --> n2
  n3["bob-cli-on.11.1.3--mon-0 [failed]"]
  n0 --> n3
  n4["bob-cli-on.11.1.3--mon [failed]"]
  n0 --> n4
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-1"></a>1 | bob-cli-on.11.1.3--1 | completed | gpt-6-luna / codex | 2026-11-22T21:39:15.546065+00:00 → 2026-11-22T21:43:49.808221+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-on.11.1.3--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-on.11.1.3--1/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-on.11.1.3--plan | completed | gpt-6-luna / codex | 2026-11-22T20:26:00.582005+00:00 → 2026-11-22T21:37:14.040912+00:00 | [1](../agents/bbugyi200.athena.bob-cli-on.11.1.3--plan/README.md#commits) | [Prompt](../agents/bbugyi200.athena.bob-cli-on.11.1.3--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-on.11.1.3--plan/chat.md) |
| <a id="member-2"></a>2 | bob-cli-on.11.1.3--2 | completed | grok-4.6 / grok | 2026-11-22T21:47:16.282934+00:00 → 2026-11-22T21:57:50.919736+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-on.11.1.3--2/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-on.11.1.3--2/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-on.11.1.3--mon-0 | failed | gpt-6-luna / codex | 2026-11-22T21:43:15.492113+00:00 → 2026-11-22T21:47:16.312356+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-on.11.1.3--mon-0/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-on.11.1.3--mon | failed | gpt-6-luna / codex | 2026-11-22T21:03:53.111184+00:00 → 2026-11-22T21:39:15.935142+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-on.11.1.3--mon/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| plan | bob-cli | [`513ec47`](https://github.com/bobs-org/bob-cli/commit/513ec47889893245cd0aacf7f67895efcc253817) | docs(task-dependencies): mark picker v6 requirement consumer | 2026-11-22 16:04:56 EST |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-on.11](bbugyi200.athena.bob-cli-on.11.md) (session · 3) | ancestor | active 1, completed 2 |
| [bob-cli-on.11.1.1](../agents/bbugyi200.athena.bob-cli-on.11.1.1/README.md) | bob-cli-on.11.1 hood | completed |
| [bob-cli-on.11.1.2](../agents/bbugyi200.athena.bob-cli-on.11.1.2/README.md) | bob-cli-on.11.1 hood | completed |
| [bob-cli-on.11.1.4](../agents/bbugyi200.athena.bob-cli-on.11.1.4/README.md) | bob-cli-on.11.1 hood | completed |
| [bob-cli-on.11.1.5](../agents/bbugyi200.athena.bob-cli-on.11.1.5/README.md) | bob-cli-on.11.1 hood | completed |
| [bob-cli-on.11.1.6](bbugyi200.athena.bob-cli-on.11.1.6.md) (session · 9) | bob-cli-on.11.1 hood | completed 8, failed 1 |
| [bob-cli-on.11.1.7.1](../agents/bbugyi200.athena.bob-cli-on.11.1.7.1/README.md) | bob-cli-on.11.1 hood | completed |
| [bob-cli-on.11.1.7.2](bbugyi200.athena.bob-cli-on.11.1.7.2.md) (session · 12) | bob-cli-on.11.1 hood | active 1, completed 7, failed 4 |
| [bob-cli-on.11.1.7.land](../agents/bbugyi200.athena.bob-cli-on.11.1.7.land/README.md) | bob-cli-on.11.1 hood | waiting |
| [bob-cli-on.11.1.land](bbugyi200.athena.bob-cli-on.11.1.land.md) (session · 3) | bob-cli-on.11.1 hood | active 1, completed 2 |
| [bob-cli-on.1](../agents/bbugyi200.athena.bob-cli-on.1/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.10](bbugyi200.athena.bob-cli-on.10.md) (session · 3) | bob-cli-on hood | active 1, completed 2 |
| [bob-cli-on.10.1.1](../agents/bbugyi200.athena.bob-cli-on.10.1.1/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.10.1.2](../agents/bbugyi200.athena.bob-cli-on.10.1.2/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.10.1.3](../agents/bbugyi200.athena.bob-cli-on.10.1.3/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.10.1.4](../agents/bbugyi200.athena.bob-cli-on.10.1.4/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.10.1.5](../agents/bbugyi200.athena.bob-cli-on.10.1.5/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.10.1.6](../agents/bbugyi200.athena.bob-cli-on.10.1.6/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.10.1.land](bbugyi200.athena.bob-cli-on.10.1.land.md) (session · 3) | bob-cli-on hood | completed 3 |
| [bob-cli-on.12](../agents/bbugyi200.athena.bob-cli-on.12/README.md) | bob-cli-on hood | waiting |
| [bob-cli-on.13](bbugyi200.athena.bob-cli-on.13.md) (session · 5) | bob-cli-on hood | completed 4, failed 1 |
| [bob-cli-on.14](../agents/bbugyi200.athena.bob-cli-on.14/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.15](bbugyi200.athena.bob-cli-on.15.md) (session · 3) | bob-cli-on hood | active 1, completed 2 |
| [bob-cli-on.15.1.1](../agents/bbugyi200.athena.bob-cli-on.15.1.1/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.15.1.2](../agents/bbugyi200.athena.bob-cli-on.15.1.2/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.15.1.3](bbugyi200.athena.bob-cli-on.15.1.3.md) (session · 5) | bob-cli-on hood | completed 4, failed 1 |
| [bob-cli-on.15.1.4](bbugyi200.athena.bob-cli-on.15.1.4.md) (session · 5) | bob-cli-on hood | completed 4, failed 1 |
| [bob-cli-on.15.1.5](bbugyi200.athena.bob-cli-on.15.1.5.md) (session · 9) | bob-cli-on hood | completed 5, failed 4 |
| [bob-cli-on.15.1.land](../agents/bbugyi200.athena.bob-cli-on.15.1.land/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.16](bbugyi200.athena.bob-cli-on.16.md) (session · 9) | bob-cli-on hood | completed 9 |
| [bob-cli-on.17](../agents/bbugyi200.athena.bob-cli-on.17/README.md) | bob-cli-on hood | waiting |
| [bob-cli-on.2](bbugyi200.athena.bob-cli-on.2.md) (session · 5) | bob-cli-on hood | completed 4, failed 1 |
| [bob-cli-on.3](../agents/bbugyi200.athena.bob-cli-on.3/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.4](../agents/bbugyi200.athena.bob-cli-on.4/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.5](../agents/bbugyi200.athena.bob-cli-on.5/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.6](bbugyi200.athena.bob-cli-on.6.md) (session · 3) | bob-cli-on hood | active 1, completed 2 |
| [bob-cli-on.6.1.1](../agents/bbugyi200.athena.bob-cli-on.6.1.1/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.6.1.2](../agents/bbugyi200.athena.bob-cli-on.6.1.2/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.6.1.3](../agents/bbugyi200.athena.bob-cli-on.6.1.3/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.6.1.4](../agents/bbugyi200.athena.bob-cli-on.6.1.4/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.6.1.5](../agents/bbugyi200.athena.bob-cli-on.6.1.5/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.6.1.land](bbugyi200.athena.bob-cli-on.6.1.land.md) (session · 3) | bob-cli-on hood | active 2, completed 1 |
| [bob-cli-on.6.1.land](../agents/bbugyi200.athena.bob-cli-on.6.1.land/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.7](../agents/bbugyi200.athena.bob-cli-on.7/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.8](bbugyi200.athena.bob-cli-on.8.md) (session · 3) | bob-cli-on hood | active 1, completed 2 |
| [bob-cli-on.8.1.1](../agents/bbugyi200.athena.bob-cli-on.8.1.1/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.8.1.2](../agents/bbugyi200.athena.bob-cli-on.8.1.2/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.8.1.3](../agents/bbugyi200.athena.bob-cli-on.8.1.3/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.8.1.4](../agents/bbugyi200.athena.bob-cli-on.8.1.4/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.8.1.5](bbugyi200.athena.bob-cli-on.8.1.5.md) (session · 5) | bob-cli-on hood | completed 4, failed 1 |
| [bob-cli-on.8.1.6](../agents/bbugyi200.athena.bob-cli-on.8.1.6/README.md) | bob-cli-on hood | completed |
| [bob-cli-on.8.1.land](bbugyi200.athena.bob-cli-on.8.1.land.md) (session · 3) | bob-cli-on hood | completed 3 |
| [bob-cli-on.9](bbugyi200.athena.bob-cli-on.9.md) (session · 5) | bob-cli-on hood | completed 5 |
| [bob-cli-on.land](../agents/bbugyi200.athena.bob-cli-on.land/README.md) | bob-cli-on hood | waiting |
