# Session: bob-cli-87.13.2

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-87](../users/bbugyi200/machines/athena/hoods/bob-cli-87/README.md) / bob-cli-87.13.2

Owner: `bbugyi200.athena` · Hood: `bob-cli-87` · Members: 9 · Bead: [bob-cli-87.13.2](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-87/bob-cli-87.13.2.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-87.13.2--mon-2 [failed]"]
  n1["bob-cli-87.13.2--plan [completed]"]
  n0 --> n1
  n2["bob-cli-87.13.2--2 [completed]"]
  n0 --> n2
  n3["bob-cli-87.13.2--mon [failed]"]
  n0 --> n3
  n4["bob-cli-87.13.2--4 [completed]"]
  n0 --> n4
  n5["bob-cli-87.13.2--3 [completed]"]
  n0 --> n5
  n6["bob-cli-87.13.2--mon-1 [failed]"]
  n0 --> n6
  n7["bob-cli-87.13.2--mon-0 [failed]"]
  n0 --> n7
  n8["bob-cli-87.13.2--1 [completed]"]
  n0 --> n8
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-mon-2"></a>mon-2 | bob-cli-87.13.2--mon-2 | failed | grok-4.6 / grok | 2026-10-17T15:22:05.652754+00:00 → 2026-10-17T15:26:41.397950+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-87.13.2--mon-2/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-87.13.2--plan | completed | gpt-6-luna / codex | 2026-10-17T14:14:51.943445+00:00 → 2026-10-17T14:36:52.779001+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-87.13.2--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-87.13.2--plan/chat.md) |
| <a id="member-2"></a>2 | bob-cli-87.13.2--2 | completed | gpt-6-luna / codex | 2026-10-17T14:54:43.520000+00:00 → 2026-10-17T15:04:32.862289+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-87.13.2--2/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-87.13.2--2/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-87.13.2--mon | failed | gpt-6-luna / codex | 2026-10-17T14:36:08.993931+00:00 → 2026-10-17T14:40:10.363948+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-87.13.2--mon/chat.md) |
| <a id="member-4"></a>4 | bob-cli-87.13.2--4 | completed | grok-4.6 / grok | 2026-10-17T15:27:24.013717+00:00 → 2026-10-17T15:31:43.684748+00:00 | [1](../agents/bbugyi200.athena.bob-cli-87.13.2--4/README.md#commits) | [Prompt](../agents/bbugyi200.athena.bob-cli-87.13.2--4/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-87.13.2--4/chat.md) |
| <a id="member-3"></a>3 | bob-cli-87.13.2--3 | completed | grok-4.6 / grok | 2026-10-17T15:09:45.950307+00:00 → 2026-10-17T15:22:37.773018+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-87.13.2--3/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-87.13.2--3/chat.md) |
| <a id="member-mon-1"></a>mon-1 | bob-cli-87.13.2--mon-1 | failed | gpt-6-luna / codex | 2026-10-17T14:59:48.352225+00:00 → 2026-10-17T15:08:46.654505+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-87.13.2--mon-1/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-87.13.2--mon-0 | failed | gpt-6-luna / codex | 2026-10-17T14:48:56.080462+00:00 → 2026-10-17T14:53:56.372813+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-87.13.2--mon-0/chat.md) |
| <a id="member-1"></a>1 | bob-cli-87.13.2--1 | completed | gpt-6-luna / codex | 2026-10-17T14:41:06.848227+00:00 → 2026-10-17T14:49:52.551825+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-87.13.2--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-87.13.2--1/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| 4 | bob-cli | [`2ae1251`](https://github.com/bobs-org/bob-cli/commit/2ae1251512e06db6fb0a2c9a1360ac48ec80aa5e) | fix(note-snapshot): hang-indent task rows and hairline image frames | 2026-10-17 11:29:49 EDT |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-87.13.1](bbugyi200.athena.bob-cli-87.13.1.md) (session · 3) | bob-cli-87.13 hood | completed 2, failed 1 |
| [bob-cli-87.13.3](bbugyi200.athena.bob-cli-87.13.3.md) (session · 3) | bob-cli-87.13 hood | completed 2, failed 1 |
| [bob-cli-87.13.4](bbugyi200.athena.bob-cli-87.13.4.md) (session · 37) | bob-cli-87.13 hood | completed 19, failed 18 |
| [bob-cli-87.13.land](bbugyi200.athena.bob-cli-87.13.land.md) (session · 3) | bob-cli-87.13 hood | active 2, failed 1 |
| [bob-cli-87.1](../agents/bbugyi200.athena.bob-cli-87.1/README.md) | bob-cli-87 hood | active |
| [bob-cli-87.10](../agents/bbugyi200.athena.bob-cli-87.10/README.md) | bob-cli-87 hood | active |
| [bob-cli-87.11](bbugyi200.athena.bob-cli-87.11.md) (session · 7) | bob-cli-87 hood | active 7 |
| [bob-cli-87.12](bbugyi200.athena.bob-cli-87.12.md) (session · 8) | bob-cli-87 hood | active 1, completed 2, failed 5 |
| [bob-cli-87.12](../agents/bbugyi200.athena.bob-cli-87.12/README.md) | bob-cli-87 hood | waiting |
| [bob-cli-87.12--3--1](../agents/bbugyi200.athena.bob-cli-87.12--3--1/README.md) | bob-cli-87 hood | active |
| [bob-cli-87.12--3--2](../agents/bbugyi200.athena.bob-cli-87.12--3--2/README.md) | bob-cli-87 hood | active |
| [bob-cli-87.12--3--4](../agents/bbugyi200.athena.bob-cli-87.12--3--4/README.md) | bob-cli-87 hood | active |
| [bob-cli-87.12--3--5](../agents/bbugyi200.athena.bob-cli-87.12--3--5/README.md) | bob-cli-87 hood | active |
| [bob-cli-87.12--3--6](../agents/bbugyi200.athena.bob-cli-87.12--3--6/README.md) | bob-cli-87 hood | completed |
| [bob-cli-87.12--3--gate](../agents/bbugyi200.athena.bob-cli-87.12--3--gate/README.md) | bob-cli-87 hood | failed |
| [bob-cli-87.12--3--gate-0](../agents/bbugyi200.athena.bob-cli-87.12--3--gate-0/README.md) | bob-cli-87 hood | failed |
| [bob-cli-87.12--3--gate-1](../agents/bbugyi200.athena.bob-cli-87.12--3--gate-1/README.md) | bob-cli-87 hood | failed |
| [bob-cli-87.12--3--gate-2](../agents/bbugyi200.athena.bob-cli-87.12--3--gate-2/README.md) | bob-cli-87 hood | failed |
| [bob-cli-87.12--3--gate-3](../agents/bbugyi200.athena.bob-cli-87.12--3--gate-3/README.md) | bob-cli-87 hood | failed |
| [bob-cli-87.12--3--plan](../agents/bbugyi200.athena.bob-cli-87.12--3--plan/README.md) | bob-cli-87 hood | completed |
| [bob-cli-87.2](bbugyi200.athena.bob-cli-87.2.md) (session · 3) | bob-cli-87 hood | active 3 |
| [bob-cli-87.2.1.1](bbugyi200.athena.bob-cli-87.2.1.1.md) (session · 9) | bob-cli-87 hood | active 9 |
| [bob-cli-87.2.1.2](../agents/bbugyi200.athena.bob-cli-87.2.1.2/README.md) | bob-cli-87 hood | active |
| [bob-cli-87.2.1.3](../agents/bbugyi200.athena.bob-cli-87.2.1.3/README.md) | bob-cli-87 hood | active |
| [bob-cli-87.2.1.4](bbugyi200.athena.bob-cli-87.2.1.4.md) (session · 7) | bob-cli-87 hood | active 7 |
| [bob-cli-87.2.1.land](bbugyi200.athena.bob-cli-87.2.1.land.md) (session · 5) | bob-cli-87 hood | active 3, completed 1, failed 1 |
| [bob-cli-87.3](bbugyi200.athena.bob-cli-87.3.md) (session · 3) | bob-cli-87 hood | active 3 |
| [bob-cli-87.3.1.1](../agents/bbugyi200.athena.bob-cli-87.3.1.1/README.md) | bob-cli-87 hood | active |
| [bob-cli-87.3.1.2](../agents/bbugyi200.athena.bob-cli-87.3.1.2/README.md) | bob-cli-87 hood | active |
| [bob-cli-87.3.1.3](bbugyi200.athena.bob-cli-87.3.1.3.md) (session · 5) | bob-cli-87 hood | active 5 |
| [bob-cli-87.3.1.land](bbugyi200.athena.bob-cli-87.3.1.land.md) (session · 3) | bob-cli-87 hood | active 2, completed 1 |
| [bob-cli-87.4](bbugyi200.athena.bob-cli-87.4.md) (session · 3) | bob-cli-87 hood | active 2, completed 1 |
| [bob-cli-87.5](bbugyi200.athena.bob-cli-87.5.md) (session · 7) | bob-cli-87 hood | active 5, completed 1, failed 1 |
| [bob-cli-87.6](../agents/bbugyi200.athena.bob-cli-87.6/README.md) | bob-cli-87 hood | active |
| [bob-cli-87.7](bbugyi200.athena.bob-cli-87.7.md) (session · 3) | bob-cli-87 hood | active 3 |
| [bob-cli-87.8](bbugyi200.athena.bob-cli-87.8.md) (session · 3) | bob-cli-87 hood | active 3 |
| [bob-cli-87.9](../agents/bbugyi200.athena.bob-cli-87.9/README.md) | bob-cli-87 hood | active |
| [bob-cli-87.land](bbugyi200.athena.bob-cli-87.land.md) (session · 3) | bob-cli-87 hood | active 3 |
