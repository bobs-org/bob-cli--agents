# Session: bob-cli-ls.2

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-ls](../users/bbugyi200/machines/athena/hoods/bob-cli-ls/README.md) / bob-cli-ls.2

Owner: `bbugyi200.athena` · Hood: `bob-cli-ls` · Members: 3 · Bead: [bob-cli-ls.2](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-ls/bob-cli-ls.2.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-ls.2--mon [completed]"]
  n1["bob-cli-ls.2--plan [active]"]
  n0 --> n1
  n2["bob-cli-ls.2--gate [completed]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-mon"></a>mon | bob-cli-ls.2--mon | completed | gpt-6-astra / codex | 2026-11-15T18:23:35.310567+00:00 → 2026-11-15T18:27:52.693816+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-ls.2--mon/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-ls.2--plan | active | gpt-6-astra / codex | 2026-11-15T18:14:10.596535+00:00 → 2026-11-15T18:23:49.154038+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-ls.2--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-ls.2--plan/chat.md) |
| <a id="member-gate"></a>gate | bob-cli-ls.2--gate | completed | gpt-6-astra / codex | 2026-11-15T18:23:12.180027+00:00 → 2026-11-15T18:23:38.966316+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-ls.2--gate/chat.md) |

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-ls.2.1.1](bbugyi200.athena.bob-cli-ls.2.1.1.md) (session · 5) | descendant | completed 4, failed 1 |
| [bob-cli-ls.2.1.2](bbugyi200.athena.bob-cli-ls.2.1.2.md) (session · 5) | descendant | completed 4, failed 1 |
| [bob-cli-ls.2.1.3](../agents/bbugyi200.athena.bob-cli-ls.2.1.3/README.md) | descendant | completed |
| [bob-cli-ls.2.1.land](bbugyi200.athena.bob-cli-ls.2.1.land.md) (session · 3) | descendant | completed 3 |
| [bob-cli-ls.1](bbugyi200.athena.bob-cli-ls.1.md) (session · 3) | bob-cli-ls hood | completed 3 |
| [bob-cli-ls.1](../agents/bbugyi200.athena.bob-cli-ls.1/README.md) | bob-cli-ls hood | active |
| [bob-cli-ls.10](../agents/bbugyi200.athena.bob-cli-ls.10/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.3](../agents/bbugyi200.athena.bob-cli-ls.3/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.4](../agents/bbugyi200.athena.bob-cli-ls.4/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.5](bbugyi200.athena.bob-cli-ls.5.md) (session · 3) | bob-cli-ls hood | completed 2, failed 1 |
| [bob-cli-ls.6](../agents/bbugyi200.athena.bob-cli-ls.6/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.7](../agents/bbugyi200.athena.bob-cli-ls.7/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.8](bbugyi200.athena.bob-cli-ls.8.md) (session · 5) | bob-cli-ls hood | completed 4, failed 1 |
| [bob-cli-ls.9](../agents/bbugyi200.athena.bob-cli-ls.9/README.md) | bob-cli-ls hood | completed |
| [bob-cli-ls.land](bbugyi200.athena.bob-cli-ls.land.md) (session · 7) | bob-cli-ls hood | active 1, completed 4, failed 2 |
