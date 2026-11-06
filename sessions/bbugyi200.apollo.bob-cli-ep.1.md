# Session: bob-cli-ep.1

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [bob-cli-ep](../users/bbugyi200/machines/apollo/hoods/bob-cli-ep/README.md) / bob-cli-ep.1

Owner: `bbugyi200.apollo` · Hood: `bob-cli-ep` · Members: 9 · Bead: [bob-cli-ep.1](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ep/bob-cli-ep.1.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-ep.1--mon-1 [active]"]
  n1["bob-cli-ep.1--plan [active]"]
  n0 --> n1
  n2["bob-cli-ep.1--1 [active]"]
  n0 --> n2
  n3["bob-cli-ep.1--gate [active]"]
  n0 --> n3
  n4["bob-cli-ep.1--3 [active]"]
  n0 --> n4
  n5["bob-cli-ep.1--mon [completed]"]
  n0 --> n5
  n6["bob-cli-ep.1--mon-0 [active]"]
  n0 --> n6
  n7["bob-cli-ep.1--2 [active]"]
  n0 --> n7
  n8["bob-cli-ep.1--code [completed]"]
  n0 --> n8
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-mon-1"></a>mon-1 | bob-cli-ep.1--mon-1 | active | gpt-6-luna / codex | 2026-10-31T12:54:12.389501+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-ep.1--mon-1/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-ep.1--plan | active | opus / claude | 2026-10-31T12:01:40.966683+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-ep.1--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-ep.1--plan/chat.md) |
| <a id="member-1"></a>1 | bob-cli-ep.1--1 | active | gpt-6-luna / codex | 2026-10-31T12:44:46.746450+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-ep.1--1/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-ep.1--1/chat.md) |
| <a id="member-gate"></a>gate | bob-cli-ep.1--gate | active | opus / claude | 2026-10-31T12:16:12.282533+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-ep.1--gate/chat.md) |
| <a id="member-3"></a>3 | bob-cli-ep.1--3 | active | gpt-6-luna / codex | 2026-10-31T13:09:46.210739+00:00 | [1](../agents/bbugyi200.apollo.bob-cli-ep.1--3/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.bob-cli-ep.1--3/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-ep.1--3/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-ep.1--mon | completed | gpt-6-luna / codex | 2026-10-31T12:41:11.744012+00:00 → 2026-10-31T12:44:47.024860+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-ep.1--mon/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-ep.1--mon-0 | active | gpt-6-luna / codex | 2026-10-31T12:47:18.379369+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-ep.1--mon-0/chat.md) |
| <a id="member-2"></a>2 | bob-cli-ep.1--2 | active | gpt-6-luna / codex | 2026-10-31T12:51:14.636883+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-ep.1--2/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-ep.1--2/chat.md) |
| <a id="member-code"></a>code | bob-cli-ep.1--code | completed | gpt-6-luna / codex | 2026-10-31T12:16:36.467977+00:00 → 2026-10-31T12:41:29.575973+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-ep.1--code/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| — | bob-cli | [`4a95e5b`](https://github.com/bobs-org/bob-cli/commit/4a95e5b78cba78d2b1c13201ccda8736087b7f4a) | feat(capture)!: replace t: type markers with #\<type\> | 2026-10-30 19:05:00 EDT |
| 3 | bob-cli | [`d1dd23e`](https://github.com/bobs-org/bob-cli/commit/d1dd23e26711a9d80d9591c9ae6c1fd0eeaa5ec8) | fix(capture): finish attached #\<type\> forms, refusal hints, and docs | 2026-10-31 09:13:37 EDT |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-ep.2](../agents/bbugyi200.apollo.bob-cli-ep.2/README.md) | bob-cli-ep hood | active |
| [bob-cli-ep.land](bbugyi200.apollo.bob-cli-ep.land.md) (session · 3) | bob-cli-ep hood | active 2, completed 1 |
