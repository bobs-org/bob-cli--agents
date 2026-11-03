# Session: bob-cli-gh.3

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-gh](../users/bbugyi200/machines/athena/hoods/bob-cli-gh/README.md) / bob-cli-gh.3

Owner: `bbugyi200.athena` · Hood: `bob-cli-gh` · Members: 9 · Bead: [bob-cli-gh.3](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-gh/bob-cli-gh.3.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-gh.3--mon-1 [failed]"]
  n1["bob-cli-gh.3--3 [completed]"]
  n0 --> n1
  n2["bob-cli-gh.3--mon [failed]"]
  n0 --> n2
  n3["bob-cli-gh.3--mon-2 [completed]"]
  n0 --> n3
  n4["bob-cli-gh.3--mon-0 [failed]"]
  n0 --> n4
  n5["bob-cli-gh.3--2 [completed]"]
  n0 --> n5
  n6["bob-cli-gh.3--plan [completed]"]
  n0 --> n6
  n7["bob-cli-gh.3--4 [completed]"]
  n0 --> n7
  n8["bob-cli-gh.3--1 [completed]"]
  n0 --> n8
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-mon-1"></a>mon-1 | bob-cli-gh.3--mon-1 | failed | gpt-6-luna / codex | 2026-11-03T17:52:55.019874+00:00 → 2026-11-03T18:02:51.422039+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-gh.3--mon-1/chat.md) |
| <a id="member-3"></a>3 | bob-cli-gh.3--3 | completed | gpt-6-luna / codex | 2026-11-03T18:04:01.838135+00:00 → 2026-11-03T18:10:49.901557+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-gh.3--3/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-gh.3--3/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-gh.3--mon | failed | gpt-6-luna / codex | 2026-11-03T17:29:22.410280+00:00 → 2026-11-03T17:32:48.292960+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-gh.3--mon/chat.md) |
| <a id="member-mon-2"></a>mon-2 | bob-cli-gh.3--mon-2 | completed | gpt-6-luna / codex | 2026-11-03T18:10:15.155335+00:00 → 2026-11-03T18:19:23.278628+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-gh.3--mon-2/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-gh.3--mon-0 | failed | gpt-6-luna / codex | 2026-11-03T17:38:01.586215+00:00 → 2026-11-03T17:47:54.730236+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-gh.3--mon-0/chat.md) |
| <a id="member-2"></a>2 | bob-cli-gh.3--2 | completed | gpt-6-luna / codex | 2026-11-03T17:49:30.892336+00:00 → 2026-11-03T17:53:33.522951+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-gh.3--2/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-gh.3--2/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-gh.3--plan | completed | gpt-6-luna / codex | 2026-11-03T17:00:07.929355+00:00 → 2026-11-03T17:29:55.417799+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-gh.3--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-gh.3--plan/chat.md) |
| <a id="member-4"></a>4 | bob-cli-gh.3--4 | completed | gpt-6-luna / codex | 2026-11-03T18:20:16.041994+00:00 → 2026-11-03T18:37:55.827557+00:00 | [1](../agents/bbugyi200.athena.bob-cli-gh.3--4/README.md#commits) | [Prompt](../agents/bbugyi200.athena.bob-cli-gh.3--4/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-gh.3--4/chat.md) |
| <a id="member-1"></a>1 | bob-cli-gh.3--1 | completed | gpt-6-luna / codex | 2026-11-03T17:33:30.750712+00:00 → 2026-11-03T17:40:11.481251+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-gh.3--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-gh.3--1/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| 4 | bob-cli | [`9f88a86`](https://github.com/bobs-org/bob-cli/commit/9f88a861ffa3444058c449b5bdd7218a184e8142) | feat(periods): add period reports and stats ranges | 2026-11-03 13:37:09 EST |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-gh.1](bbugyi200.athena.bob-cli-gh.1.md) (session · 3) | bob-cli-gh hood | completed 3 |
| [bob-cli-gh.2](../agents/bbugyi200.athena.bob-cli-gh.2/README.md) | bob-cli-gh hood | completed |
| [bob-cli-gh.4](../agents/bbugyi200.athena.bob-cli-gh.4/README.md) | bob-cli-gh hood | completed |
| [bob-cli-gh.5](../agents/bbugyi200.athena.bob-cli-gh.5/README.md) | bob-cli-gh hood | waiting |
| [bob-cli-gh.6](../agents/bbugyi200.athena.bob-cli-gh.6/README.md) | bob-cli-gh hood | completed |
| [bob-cli-gh.7](../agents/bbugyi200.athena.bob-cli-gh.7/README.md) | bob-cli-gh hood | waiting |
| [bob-cli-gh.8](../agents/bbugyi200.athena.bob-cli-gh.8/README.md) | bob-cli-gh hood | waiting |
| [bob-cli-gh.9](../agents/bbugyi200.athena.bob-cli-gh.9/README.md) | bob-cli-gh hood | waiting |
| [bob-cli-gh.land](../agents/bbugyi200.athena.bob-cli-gh.land/README.md) | bob-cli-gh hood | waiting |
