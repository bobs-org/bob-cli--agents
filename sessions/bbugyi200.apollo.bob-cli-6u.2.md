# Session: bob-cli-6u.2

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [bob-cli-6u](../users/bbugyi200/machines/apollo/hoods/bob-cli-6u/README.md) / bob-cli-6u.2

Owner: `bbugyi200.apollo` · Hood: `bob-cli-6u` · Members: 5 · Bead: [bob-cli-6u.2](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-6u/bob-cli-6u.2.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-6u.2--2 [completed]"]
  n1["bob-cli-6u.2--mon-0 [failed]"]
  n0 --> n1
  n2["bob-cli-6u.2--1 [completed]"]
  n0 --> n2
  n3["bob-cli-6u.2--mon [failed]"]
  n0 --> n3
  n4["bob-cli-6u.2--plan [completed]"]
  n0 --> n4
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-2"></a>2 | bob-cli-6u.2--2 | completed | gpt-6-luna / codex | 2026-10-12T15:20:33.061581+00:00 → 2026-10-12T15:24:51.135774+00:00 | [1](../agents/bbugyi200.apollo.bob-cli-6u.2--2/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.bob-cli-6u.2--2/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-6u.2--2/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-6u.2--mon-0 | failed | gpt-6-luna / codex | 2026-10-12T15:14:52.382090+00:00 → 2026-10-12T15:20:33.544377+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-6u.2--mon-0/chat.md) |
| <a id="member-1"></a>1 | bob-cli-6u.2--1 | completed | gpt-6-luna / codex | 2026-10-12T15:07:20.348673+00:00 → 2026-10-12T15:15:43.200401+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-6u.2--1/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-6u.2--1/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-6u.2--mon | failed | gpt-6-luna / codex | 2026-10-12T15:00:58.215657+00:00 → 2026-10-12T15:07:20.507298+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-6u.2--mon/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-6u.2--plan | completed | gpt-6-luna / codex | 2026-10-12T14:54:17.643944+00:00 → 2026-10-12T15:01:50.437154+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-6u.2--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-6u.2--plan/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| 2 | bob-cli | [`f6fbd7d`](https://github.com/bobs-org/bob-cli/commit/f6fbd7ddf35e050d635f5c473ff38827458ec462) | refactor(projects): derive blocking from ^prj task line | 2026-10-12 11:22:48 EDT |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-6u.1](../agents/bbugyi200.apollo.bob-cli-6u.1/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.10](../agents/bbugyi200.apollo.bob-cli-6u.10/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.11](../agents/bbugyi200.apollo.bob-cli-6u.11/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.12](../agents/bbugyi200.apollo.bob-cli-6u.12/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.13](../agents/bbugyi200.apollo.bob-cli-6u.13/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.14](../agents/bbugyi200.apollo.bob-cli-6u.14/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.15](../agents/bbugyi200.apollo.bob-cli-6u.15/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.16](bbugyi200.apollo.bob-cli-6u.16.md) (session · 3) | bob-cli-6u hood | completed 2, failed 1 |
| [bob-cli-6u.17](bbugyi200.apollo.bob-cli-6u.17.md) (session · 3) | bob-cli-6u hood | completed 2, failed 1 |
| [bob-cli-6u.18.1](../agents/bbugyi200.apollo.bob-cli-6u.18.1/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.18.2](../agents/bbugyi200.apollo.bob-cli-6u.18.2/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.18.3](../agents/bbugyi200.apollo.bob-cli-6u.18.3/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.18.4](../agents/bbugyi200.apollo.bob-cli-6u.18.4/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.18.5](../agents/bbugyi200.apollo.bob-cli-6u.18.5/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.18.6](../agents/bbugyi200.apollo.bob-cli-6u.18.6/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.18.7.1](bbugyi200.apollo.bob-cli-6u.18.7.1.md) (session · 5) | bob-cli-6u hood | completed 3, failed 2 |
| [bob-cli-6u.18.7.2](bbugyi200.apollo.bob-cli-6u.18.7.2.md) (session · 3) | bob-cli-6u hood | completed 2, failed 1 |
| [bob-cli-6u.18.7.3](../agents/bbugyi200.apollo.bob-cli-6u.18.7.3/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.18.7.4](../agents/bbugyi200.apollo.bob-cli-6u.18.7.4/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.18.7.5](../agents/bbugyi200.apollo.bob-cli-6u.18.7.5/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.18.7.6.1](../agents/bbugyi200.apollo.bob-cli-6u.18.7.6.1/README.md) | bob-cli-6u hood | active |
| [bob-cli-6u.18.7.6.2](../agents/bbugyi200.apollo.bob-cli-6u.18.7.6.2/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.18.7.6.3](../agents/bbugyi200.apollo.bob-cli-6u.18.7.6.3/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.18.7.6.4](../agents/bbugyi200.apollo.bob-cli-6u.18.7.6.4/README.md) | bob-cli-6u hood | waiting |
| [bob-cli-6u.18.7.6.land](../agents/bbugyi200.apollo.bob-cli-6u.18.7.6.land/README.md) | bob-cli-6u hood | waiting |
| [bob-cli-6u.18.7.land](bbugyi200.apollo.bob-cli-6u.18.7.land.md) (session · 3) | bob-cli-6u hood | failed 3 |
| [bob-cli-6u.18.land](bbugyi200.apollo.bob-cli-6u.18.land.md) (session · 3) | bob-cli-6u hood | failed 3 |
| [bob-cli-6u.3](../agents/bbugyi200.apollo.bob-cli-6u.3/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.4](../agents/bbugyi200.apollo.bob-cli-6u.4/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.5](bbugyi200.apollo.bob-cli-6u.5.md) (session · 3) | bob-cli-6u hood | completed 2, failed 1 |
| [bob-cli-6u.6](../agents/bbugyi200.apollo.bob-cli-6u.6/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.7](../agents/bbugyi200.apollo.bob-cli-6u.7/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.8](../agents/bbugyi200.apollo.bob-cli-6u.8/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.9](bbugyi200.apollo.bob-cli-6u.9.md) (session · 6) | bob-cli-6u hood | completed 3, failed 3 |
| [bob-cli-6u.9](../agents/bbugyi200.apollo.bob-cli-6u.9/README.md) | bob-cli-6u hood | completed |
| [bob-cli-6u.land](bbugyi200.apollo.bob-cli-6u.land.md) (session · 3) | bob-cli-6u hood | failed 3 |
