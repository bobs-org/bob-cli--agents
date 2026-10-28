# Session: bob-cli-df.2.1.3

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-df](../users/bbugyi200/machines/athena/hoods/bob-cli-df/README.md) / bob-cli-df.2.1.3

Owner: `bbugyi200.athena` · Hood: `bob-cli-df` · Members: 9 · Bead: [bob-cli-df.2.1.3](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-df/bob-cli-df.2.1.3.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-df.2.1.3--plan [completed]"]
  n1["bob-cli-df.2.1.3--mon-2 [failed]"]
  n0 --> n1
  n2["bob-cli-df.2.1.3--mon-0 [failed]"]
  n0 --> n2
  n3["bob-cli-df.2.1.3--2 [completed]"]
  n0 --> n3
  n4["bob-cli-df.2.1.3--1 [completed]"]
  n0 --> n4
  n5["bob-cli-df.2.1.3--4 [completed]"]
  n0 --> n5
  n6["bob-cli-df.2.1.3--mon [failed]"]
  n0 --> n6
  n7["bob-cli-df.2.1.3--3 [completed]"]
  n0 --> n7
  n8["bob-cli-df.2.1.3--mon-1 [failed]"]
  n0 --> n8
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-plan"></a>plan | bob-cli-df.2.1.3--plan | completed | gpt-6-luna / codex | 2026-10-28T04:15:25.846303+00:00 → 2026-10-28T04:35:46.841133+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-df.2.1.3--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.3--plan/chat.md) |
| <a id="member-mon-2"></a>mon-2 | bob-cli-df.2.1.3--mon-2 | failed | gpt-6-luna / codex | 2026-10-28T05:24:13.504350+00:00 → 2026-10-28T05:31:44.333606+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.3--mon-2/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-df.2.1.3--mon-0 | failed | gpt-6-luna / codex | 2026-10-28T04:43:56.440695+00:00 → 2026-10-28T05:07:18.721590+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.3--mon-0/chat.md) |
| <a id="member-2"></a>2 | bob-cli-df.2.1.3--2 | completed | gpt-6-luna / codex | 2026-10-28T05:09:50.781142+00:00 → 2026-10-28T05:16:06.247929+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-df.2.1.3--2/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.3--2/chat.md) |
| <a id="member-1"></a>1 | bob-cli-df.2.1.3--1 | completed | gpt-6-luna / codex | 2026-10-28T04:37:27.129592+00:00 → 2026-10-28T04:44:28.878631+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-df.2.1.3--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.3--1/chat.md) |
| <a id="member-4"></a>4 | bob-cli-df.2.1.3--4 | completed | gpt-6-luna / codex | 2026-10-28T05:33:11.484606+00:00 → 2026-10-28T05:45:01.603115+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-df.2.1.3--4/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.3--4/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-df.2.1.3--mon | failed | gpt-6-luna / codex | 2026-10-28T04:34:00.456517+00:00 → 2026-10-28T04:37:21.310942+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.3--mon/chat.md) |
| <a id="member-3"></a>3 | bob-cli-df.2.1.3--3 | completed | gpt-6-luna / codex | 2026-10-28T05:19:13.378265+00:00 → 2026-10-28T05:25:01.795684+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-df.2.1.3--3/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.3--3/chat.md) |
| <a id="member-mon-1"></a>mon-1 | bob-cli-df.2.1.3--mon-1 | failed | gpt-6-luna / codex | 2026-10-28T05:14:27.342284+00:00 → 2026-10-28T05:17:40.756100+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.3--mon-1/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-df.2](bbugyi200.athena.bob-cli-df.2.md) (session · 3) | ancestor | failed 3 |
| [bob-cli-df.2.1.1](../agents/bbugyi200.athena.bob-cli-df.2.1.1/README.md) | bob-cli-df.2.1 hood | completed |
| [bob-cli-df.2.1.2](../agents/bbugyi200.athena.bob-cli-df.2.1.2/README.md) | bob-cli-df.2.1 hood | completed |
| [bob-cli-df.2.1.4.1](bbugyi200.athena.bob-cli-df.2.1.4.1.md) (session · 11) | bob-cli-df.2.1 hood | completed 6, failed 5 |
| [bob-cli-df.2.1.4.2](bbugyi200.athena.bob-cli-df.2.1.4.2.md) (session · 3) | bob-cli-df.2.1 hood | completed 2, failed 1 |
| [bob-cli-df.2.1.4.3.1](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.1/README.md) | bob-cli-df.2.1 hood | active |
| [bob-cli-df.2.1.4.3.2](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.2/README.md) | bob-cli-df.2.1 hood | waiting |
| [bob-cli-df.2.1.4.3.land](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.land/README.md) | bob-cli-df.2.1 hood | waiting |
| [bob-cli-df.2.1.4.land](bbugyi200.athena.bob-cli-df.2.1.4.land.md) (session · 3) | bob-cli-df.2.1 hood | failed 3 |
| [bob-cli-df.2.1.land](bbugyi200.athena.bob-cli-df.2.1.land.md) (session · 3) | bob-cli-df.2.1 hood | failed 3 |
| [bob-cli-df.1](../agents/bbugyi200.athena.bob-cli-df.1/README.md) | bob-cli-df hood | completed |
| [bob-cli-df.3](../agents/bbugyi200.athena.bob-cli-df.3/README.md) | bob-cli-df hood | completed |
| [bob-cli-df.4](bbugyi200.athena.bob-cli-df.4.md) (session · 3) | bob-cli-df hood | failed 3 |
| [bob-cli-df.4.1.1](bbugyi200.athena.bob-cli-df.4.1.1.md) (session · 3) | bob-cli-df hood | completed 2, failed 1 |
| [bob-cli-df.4.1.2](bbugyi200.athena.bob-cli-df.4.1.2.md) (session · 3) | bob-cli-df hood | completed 2, failed 1 |
| [bob-cli-df.4.1.3](../agents/bbugyi200.athena.bob-cli-df.4.1.3/README.md) | bob-cli-df hood | completed |
| [bob-cli-df.4.1.4](bbugyi200.athena.bob-cli-df.4.1.4.md) (session · 3) | bob-cli-df hood | completed 2, failed 1 |
| [bob-cli-df.4.1.land](bbugyi200.athena.bob-cli-df.4.1.land.md) (session · 3) | bob-cli-df hood | completed 2, failed 1 |
| [bob-cli-df.land](../agents/bbugyi200.athena.bob-cli-df.land/README.md) | bob-cli-df hood | waiting |
