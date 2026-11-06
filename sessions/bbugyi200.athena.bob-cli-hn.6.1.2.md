# Session: bob-cli-hn.6.1.2

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-hn](../users/bbugyi200/machines/athena/hoods/bob-cli-hn/README.md) / bob-cli-hn.6.1.2

Owner: `bbugyi200.athena` · Hood: `bob-cli-hn` · Members: 7 · Bead: [bob-cli-hn.6.1.2](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-hn/bob-cli-hn.6.1.2.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-hn.6.1.2--1 [completed]"]
  n1["bob-cli-hn.6.1.2--mon-1 [failed]"]
  n0 --> n1
  n2["bob-cli-hn.6.1.2--mon [failed]"]
  n0 --> n2
  n3["bob-cli-hn.6.1.2--3 [completed]"]
  n0 --> n3
  n4["bob-cli-hn.6.1.2--plan [completed]"]
  n0 --> n4
  n5["bob-cli-hn.6.1.2--2 [completed]"]
  n0 --> n5
  n6["bob-cli-hn.6.1.2--mon-0 [failed]"]
  n0 --> n6
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-1"></a>1 | bob-cli-hn.6.1.2--1 | completed | gpt-6-luna / codex | 2026-11-06T02:53:43.643063+00:00 → 2026-11-06T03:02:57.219642+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-hn.6.1.2--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-hn.6.1.2--1/chat.md) |
| <a id="member-mon-1"></a>mon-1 | bob-cli-hn.6.1.2--mon-1 | failed | gpt-6-luna / codex | 2026-11-06T03:12:29.334826+00:00 → 2026-11-06T03:15:04.870022+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-hn.6.1.2--mon-1/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-hn.6.1.2--mon | failed | gpt-6-luna / codex | 2026-11-06T02:48:17.396696+00:00 → 2026-11-06T02:53:08.112556+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-hn.6.1.2--mon/chat.md) |
| <a id="member-3"></a>3 | bob-cli-hn.6.1.2--3 | completed | gpt-6-luna / codex | 2026-11-06T03:16:48.698376+00:00 → 2026-11-06T03:22:09.820315+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-hn.6.1.2--3/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-hn.6.1.2--3/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-hn.6.1.2--plan | completed | gpt-6-luna / codex | 2026-11-06T02:25:58.844571+00:00 → 2026-11-06T02:49:09.233630+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-hn.6.1.2--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-hn.6.1.2--plan/chat.md) |
| <a id="member-2"></a>2 | bob-cli-hn.6.1.2--2 | completed | gpt-6-luna / codex | 2026-11-06T03:07:31.915876+00:00 → 2026-11-06T03:13:18.170360+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-hn.6.1.2--2/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-hn.6.1.2--2/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-hn.6.1.2--mon-0 | failed | gpt-6-luna / codex | 2026-11-06T03:02:14.962382+00:00 → 2026-11-06T03:05:37.510681+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-hn.6.1.2--mon-0/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-hn.6](bbugyi200.athena.bob-cli-hn.6.md) (session · 3) | ancestor | active 1, completed 2 |
| [bob-cli-hn.6.1.1](../agents/bbugyi200.athena.bob-cli-hn.6.1.1/README.md) | bob-cli-hn.6.1 hood | completed |
| [bob-cli-hn.6.1.3](../agents/bbugyi200.athena.bob-cli-hn.6.1.3/README.md) | bob-cli-hn.6.1 hood | waiting |
| [bob-cli-hn.6.1.4](../agents/bbugyi200.athena.bob-cli-hn.6.1.4/README.md) | bob-cli-hn.6.1 hood | waiting |
| [bob-cli-hn.6.1.land](../agents/bbugyi200.athena.bob-cli-hn.6.1.land/README.md) | bob-cli-hn.6.1 hood | waiting |
| [bob-cli-hn.1](../agents/bbugyi200.athena.bob-cli-hn.1/README.md) | bob-cli-hn hood | completed |
| [bob-cli-hn.2](../agents/bbugyi200.athena.bob-cli-hn.2/README.md) | bob-cli-hn hood | completed |
| [bob-cli-hn.3](../agents/bbugyi200.athena.bob-cli-hn.3/README.md) | bob-cli-hn hood | completed |
| [bob-cli-hn.4](../agents/bbugyi200.athena.bob-cli-hn.4/README.md) | bob-cli-hn hood | completed |
| [bob-cli-hn.5](../agents/bbugyi200.athena.bob-cli-hn.5/README.md) | bob-cli-hn hood | completed |
| [bob-cli-hn.7](../agents/bbugyi200.athena.bob-cli-hn.7/README.md) | bob-cli-hn hood | waiting |
| [bob-cli-hn.8](../agents/bbugyi200.athena.bob-cli-hn.8/README.md) | bob-cli-hn hood | completed |
| [bob-cli-hn.9](../agents/bbugyi200.athena.bob-cli-hn.9/README.md) | bob-cli-hn hood | waiting |
| [bob-cli-hn.land](../agents/bbugyi200.athena.bob-cli-hn.land/README.md) | bob-cli-hn hood | waiting |
