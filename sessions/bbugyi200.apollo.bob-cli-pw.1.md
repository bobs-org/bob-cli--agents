# Session: bob-cli-pw.1

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [bob-cli-pw](../users/bbugyi200/machines/apollo/hoods/bob-cli-pw/README.md) / bob-cli-pw.1

Owner: `bbugyi200.apollo` · Hood: `bob-cli-pw` · Members: 7 · Bead: [bob-cli-pw.1](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-pw/bob-cli-pw.1.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-pw.1--3 [active]"]
  n1["bob-cli-pw.1--2 [completed]"]
  n0 --> n1
  n2["bob-cli-pw.1--mon-1 [completed]"]
  n0 --> n2
  n3["bob-cli-pw.1--mon [failed]"]
  n0 --> n3
  n4["bob-cli-pw.1--mon-0 [failed]"]
  n0 --> n4
  n5["bob-cli-pw.1--1 [completed]"]
  n0 --> n5
  n6["bob-cli-pw.1--plan [completed]"]
  n0 --> n6
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-3"></a>3 | bob-cli-pw.1--3 | active | gpt-6-luna / codex | 2026-11-24T17:07:59.367049+00:00 | [1](../agents/bbugyi200.apollo.bob-cli-pw.1--3/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.bob-cli-pw.1--3/prompt.md) | — |
| <a id="member-2"></a>2 | bob-cli-pw.1--2 | completed | gpt-6-luna / codex | 2026-11-24T16:36:26.398085+00:00 → 2026-11-24T16:54:05.500186+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-pw.1--2/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-pw.1--2/chat.md) |
| <a id="member-mon-1"></a>mon-1 | bob-cli-pw.1--mon-1 | completed | gpt-6-luna / codex | 2026-11-24T16:51:20.160508+00:00 → 2026-11-24T17:06:07.659266+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-pw.1--mon-1/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-pw.1--mon | failed | gpt-6-luna / codex | 2026-11-24T16:10:04.828404+00:00 → 2026-11-24T16:14:15.764868+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-pw.1--mon/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-pw.1--mon-0 | failed | gpt-6-luna / codex | 2026-11-24T16:28:01.820803+00:00 → 2026-11-24T16:36:26.458681+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-pw.1--mon-0/chat.md) |
| <a id="member-1"></a>1 | bob-cli-pw.1--1 | completed | gpt-6-luna / codex | 2026-11-24T16:14:15.369272+00:00 → 2026-11-24T16:29:26.539482+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-pw.1--1/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-pw.1--1/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-pw.1--plan | completed | gpt-6-luna / codex | 2026-11-24T15:47:27.406886+00:00 → 2026-11-24T16:12:31.198233+00:00 | [1](../agents/bbugyi200.apollo.bob-cli-pw.1--plan/README.md#commits) | [Prompt](../agents/bbugyi200.apollo.bob-cli-pw.1--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-pw.1--plan/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| plan | bob-cli | [`dbf405e`](https://github.com/bobs-org/bob-cli/commit/dbf405e397b7081c5c5531590608637346e49dfc) | feat(meetings): add notes normalization and rendering | 2026-11-24 11:11:34 EST |
| 3 | bob-cli | [`b832e58`](https://github.com/bobs-org/bob-cli/commit/b832e58df449d9d422a488f1d8f3bf0828a93487) | feat(meetings): add read-only meeting resolver and agenda wiring | 2026-11-24 12:52:20 EST |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-pw.2](../agents/bbugyi200.apollo.bob-cli-pw.2/README.md) | bob-cli-pw hood | completed |
| [bob-cli-pw.3](../agents/bbugyi200.apollo.bob-cli-pw.3/README.md) | bob-cli-pw hood | waiting |
| [bob-cli-pw.4](../agents/bbugyi200.apollo.bob-cli-pw.4/README.md) | bob-cli-pw hood | waiting |
| [bob-cli-pw.5](../agents/bbugyi200.apollo.bob-cli-pw.5/README.md) | bob-cli-pw hood | waiting |
| [bob-cli-pw.6](../agents/bbugyi200.apollo.bob-cli-pw.6/README.md) | bob-cli-pw hood | waiting |
| [bob-cli-pw.7](../agents/bbugyi200.apollo.bob-cli-pw.7/README.md) | bob-cli-pw hood | waiting |
| [bob-cli-pw.8](../agents/bbugyi200.apollo.bob-cli-pw.8/README.md) | bob-cli-pw hood | waiting |
| [bob-cli-pw.land](../agents/bbugyi200.apollo.bob-cli-pw.land/README.md) | bob-cli-pw hood | waiting |
