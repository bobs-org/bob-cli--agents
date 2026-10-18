# Session: 11d

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [11d](../users/bbugyi200/machines/athena/hoods/11d/README.md) / 11d

Owner: `bbugyi200.athena` · Hood: `11d` · Members: 15

## Lineage

```mermaid
flowchart TD
  n0["11d--mon-4 [failed]"]
  n1["11d--code [completed]"]
  n0 --> n1
  n2["11d--mon-3 [failed]"]
  n0 --> n2
  n3["11d--3 [completed]"]
  n0 --> n3
  n4["11d--1 [completed]"]
  n0 --> n4
  n5["11d--5 [completed]"]
  n0 --> n5
  n6["11d--4 [completed]"]
  n0 --> n6
  n7["11d--plan [completed]"]
  n0 --> n7
  n8["11d--mon-0 [failed]"]
  n0 --> n8
  n9["11d--mon-2 [failed]"]
  n0 --> n9
  n10["11d--2 [completed]"]
  n0 --> n10
  n11["11d--mon [failed]"]
  n0 --> n11
  n12["11d--6 [active]"]
  n0 --> n12
  n13["11d--gate [failed]"]
  n0 --> n13
  n14["11d--mon-1 [failed]"]
  n0 --> n14
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-mon-4"></a>mon-4 | 11d--mon-4 | failed | gpt-6-luna / codex | 2026-10-18T18:17:32.253893+00:00 → 2026-10-18T18:20:13.958819+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.11d--mon-4/chat.md) |
| <a id="member-code"></a>code | 11d--code | completed | gpt-6-luna / codex | 2026-10-18T17:05:00.225807+00:00 → 2026-10-18T17:17:39.965031+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.11d--code/chat.md) |
| <a id="member-mon-3"></a>mon-3 | 11d--mon-3 | failed | gpt-6-luna / codex | 2026-10-18T17:56:44.403518+00:00 → 2026-10-18T18:04:17.900563+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.11d--mon-3/chat.md) |
| <a id="member-3"></a>3 | 11d--3 | completed | gpt-6-luna / codex | 2026-10-18T17:40:18.003466+00:00 → 2026-10-18T17:45:20.041863+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.11d--3/prompt.md) | [Chat](../agents/bbugyi200.athena.11d--3/chat.md) |
| <a id="member-1"></a>1 | 11d--1 | completed | gpt-6-luna / codex | 2026-10-18T17:20:39.173276+00:00 → 2026-10-18T17:25:44.749117+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.11d--1/prompt.md) | [Chat](../agents/bbugyi200.athena.11d--1/chat.md) |
| <a id="member-5"></a>5 | 11d--5 | completed | gpt-6-luna / codex | 2026-10-18T18:04:59.791426+00:00 → 2026-10-18T18:18:31.832204+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.11d--5/prompt.md) | [Chat](../agents/bbugyi200.athena.11d--5/chat.md) |
| <a id="member-4"></a>4 | 11d--4 | completed | gpt-6-luna / codex | 2026-10-18T17:51:13.401385+00:00 → 2026-10-18T17:57:42.406779+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.11d--4/prompt.md) | [Chat](../agents/bbugyi200.athena.11d--4/chat.md) |
| <a id="member-plan"></a>plan | 11d--plan | completed | opus / claude | 2026-10-18T16:22:39.686190+00:00 → 2026-10-18T17:17:39.965031+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.11d--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.11d--plan/chat.md) |
| <a id="member-mon-0"></a>mon-0 | 11d--mon-0 | failed | gpt-6-luna / codex | 2026-10-18T17:25:01.896957+00:00 → 2026-10-18T17:30:38.231127+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.11d--mon-0/chat.md) |
| <a id="member-mon-2"></a>mon-2 | 11d--mon-2 | failed | gpt-6-luna / codex | 2026-10-18T17:44:46.488675+00:00 → 2026-10-18T17:50:37.165343+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.11d--mon-2/chat.md) |
| <a id="member-2"></a>2 | 11d--2 | completed | gpt-6-luna / codex | 2026-10-18T17:31:22.262284+00:00 → 2026-10-18T17:37:43.431033+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.11d--2/prompt.md) | [Chat](../agents/bbugyi200.athena.11d--2/chat.md) |
| <a id="member-mon"></a>mon | 11d--mon | failed | gpt-6-luna / codex | 2026-10-18T17:16:52.562908+00:00 → 2026-10-18T17:19:50.743591+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.11d--mon/chat.md) |
| <a id="member-6"></a>6 | 11d--6 | active | gpt-6-luna / codex | 2026-10-18T18:20:59.568207+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.11d--6/prompt.md) | — |
| <a id="member-gate"></a>gate | 11d--gate | failed | opus / claude | 2026-10-18T17:04:12.828034+00:00 → 2026-10-18T17:04:39.606654+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.11d--gate/chat.md) |
| <a id="member-mon-1"></a>mon-1 | 11d--mon-1 | failed | gpt-6-luna / codex | 2026-10-18T17:36:56.039537+00:00 → 2026-10-18T17:39:39.207849+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.11d--mon-1/chat.md) |
