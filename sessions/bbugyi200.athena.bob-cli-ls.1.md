# Session: bob-cli-ls.1

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-ls](../users/bbugyi200/machines/athena/hoods/bob-cli-ls/README.md) / bob-cli-ls.1

Owner: `bbugyi200.athena` · Hood: `bob-cli-ls` · Members: 3 · Bead: [bob-cli-ls.1](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ls/bob-cli-ls.1.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-ls.1--gate [completed]"]
  n1["bob-cli-ls.1--1 [completed]"]
  n0 --> n1
  n2["bob-cli-ls.1--plan [completed]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-gate"></a>gate | bob-cli-ls.1--gate | completed | gpt-6-astra / codex | 2026-11-15T19:33:54.792850+00:00 → 2026-11-15T19:34:22.691629+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-ls.1--gate/chat.md) |
| <a id="member-1"></a>1 | bob-cli-ls.1--1 | completed | gpt-6-astra / codex | 2026-11-15T19:36:07.458762+00:00 → 2026-11-15T19:44:32.330113+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-ls.1--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-ls.1--1/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-ls.1--plan | completed | gpt-6-astra / codex | 2026-11-15T18:37:27.773901+00:00 → 2026-11-15T18:47:54.376306+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-ls.1--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-ls.1--plan/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-ls.10](../agents/bbugyi200.athena.bob-cli-ls.10/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.2](bbugyi200.athena.bob-cli-ls.2.md) (session · 3) | bob-cli-ls hood | active 1, completed 2 |
| [bob-cli-ls.2.1.1](bbugyi200.athena.bob-cli-ls.2.1.1.md) (session · 5) | bob-cli-ls hood | completed 4, failed 1 |
| [bob-cli-ls.2.1.2](bbugyi200.athena.bob-cli-ls.2.1.2.md) (session · 5) | bob-cli-ls hood | completed 4, failed 1 |
| [bob-cli-ls.2.1.3](../agents/bbugyi200.athena.bob-cli-ls.2.1.3/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.2.1.land](bbugyi200.athena.bob-cli-ls.2.1.land.md) (session · 3) | bob-cli-ls hood | completed 3 |
| [bob-cli-ls.3](../agents/bbugyi200.athena.bob-cli-ls.3/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.4](../agents/bbugyi200.athena.bob-cli-ls.4/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.5](bbugyi200.athena.bob-cli-ls.5.md) (session · 2) | bob-cli-ls hood | active 1, completed 1 |
| [bob-cli-ls.6](../agents/bbugyi200.athena.bob-cli-ls.6/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.7](../agents/bbugyi200.athena.bob-cli-ls.7/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.8](../agents/bbugyi200.athena.bob-cli-ls.8/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.9](../agents/bbugyi200.athena.bob-cli-ls.9/README.md) | bob-cli-ls hood | waiting |
| [bob-cli-ls.land](../agents/bbugyi200.athena.bob-cli-ls.land/README.md) | bob-cli-ls hood | waiting |
