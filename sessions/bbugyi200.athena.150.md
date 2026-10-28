# Session: 150

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [150](../users/bbugyi200/machines/athena/hoods/150/README.md) / 150

Owner: `bbugyi200.athena` · Hood: `150` · Members: 9

## Lineage

```mermaid
flowchart TD
  n0["150--code [completed]"]
  n1["150--1 [completed]"]
  n0 --> n1
  n2["150--gate [failed]"]
  n0 --> n2
  n3["150--3 [active]"]
  n0 --> n3
  n4["150--2 [completed]"]
  n0 --> n4
  n5["150--mon-1 [failed]"]
  n0 --> n5
  n6["150--mon [failed]"]
  n0 --> n6
  n7["150--mon-0 [failed]"]
  n0 --> n7
  n8["150--plan [completed]"]
  n0 --> n8
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-code"></a>code | 150--code | completed | gpt-6-luna / codex | 2026-10-28T11:14:01.341396+00:00 → 2026-10-28T11:24:31.946861+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.150--code/prompt.md) | [Chat](../agents/bbugyi200.athena.150--code/chat.md) |
| <a id="member-1"></a>1 | 150--1 | completed | gpt-6-luna / codex | 2026-10-28T11:39:21.053122+00:00 → 2026-10-28T11:45:38.189551+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.150--1/prompt.md) | [Chat](../agents/bbugyi200.athena.150--1/chat.md) |
| <a id="member-gate"></a>gate | 150--gate | failed | opus / claude | 2026-10-28T11:10:26.036922+00:00 → 2026-10-28T11:12:03.912964+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.150--gate/chat.md) |
| <a id="member-3"></a>3 | 150--3 | active | grok-4.6 / grok | 2026-10-28T12:36:28.386849+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.150--3/prompt.md) | — |
| <a id="member-2"></a>2 | 150--2 | completed | grok-4.6 / grok | 2026-10-28T12:00:57.354563+00:00 → 2026-10-28T12:18:22.542302+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.150--2/prompt.md) | [Chat](../agents/bbugyi200.athena.150--2/chat.md) |
| <a id="member-mon-1"></a>mon-1 | 150--mon-1 | failed | grok-4.6 / grok | 2026-10-28T12:17:22.971614+00:00 → 2026-10-28T12:34:07.825341+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.150--mon-1/chat.md) |
| <a id="member-mon"></a>mon | 150--mon | failed | gpt-6-luna / codex | 2026-10-28T11:23:32.536522+00:00 → 2026-10-28T11:40:50.446981+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.150--mon/chat.md) |
| <a id="member-mon-0"></a>mon-0 | 150--mon-0 | failed | gpt-6-luna / codex | 2026-10-28T11:43:55.436545+00:00 → 2026-10-28T11:58:44.505925+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.150--mon-0/chat.md) |
| <a id="member-plan"></a>plan | 150--plan | completed | opus / claude | 2026-10-28T11:00:30.862418+00:00 → 2026-10-28T11:09:34.055598+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.150--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.150--plan/chat.md) |
