# Session: bob-cli-d2.land

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-d2](../users/bbugyi200/machines/athena/hoods/bob-cli-d2/README.md) / bob-cli-d2.land

Owner: `bbugyi200.athena` · Hood: `bob-cli-d2` · Members: 4 · Bead: [bob-cli-d2](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-d2/README.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-d2.land--code [completed]"]
  n1["bob-cli-d2.land--mon [active]"]
  n0 --> n1
  n2["bob-cli-d2.land--gate [failed]"]
  n0 --> n2
  n3["bob-cli-d2.land--plan [completed]"]
  n0 --> n3
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-code"></a>code | bob-cli-d2.land--code | completed | gpt-6-luna / codex | 2026-10-27T13:25:20.143748+00:00 → 2026-10-27T13:43:07.082917+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-d2.land--code/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-d2.land--mon | active | gpt-6-luna / codex | 2026-10-27T13:42:13.743146+00:00 | 0 | — | — |
| <a id="member-gate"></a>gate | bob-cli-d2.land--gate | failed | gpt-6-astra / codex | 2026-10-27T13:24:32.414858+00:00 → 2026-10-27T13:24:52.570148+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-d2.land--gate/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-d2.land--plan | completed | gpt-6-astra / codex | 2026-10-27T13:03:08.166798+00:00 → 2026-10-27T13:43:07.082917+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-d2.land--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-d2.land--plan/chat.md) |

## Variables

| Role | Variable | Value |
|---|---|---|
| plan | `artifacts` | \[{bead: bob-cli-d2, kind: markdown, label: bob-cli-d2 landing audit and remaining-work reproductions, path: /home/bryan/.sase/artifacts/agents/gh\_bobs-org\_\_bob-cli/20261027074356/bob-cli-d2-land-audi… |

#### artifacts

**Role:** `plan`

```yaml
- bead: bob-cli-d2
  kind: markdown
  label: bob-cli-d2 landing audit and remaining-work reproductions
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261027074356/bob-cli-d2-land-audit-9f8d9f281752.md
  ref: file:explicit:c61a26370b705cae1446a6ed
  source_path: /tmp/bob-cli-d2-land-audit.md
```

Values are truncated for display; see each member's agent meta.json for the full values.

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-d2.1](../agents/bbugyi200.athena.bob-cli-d2.1/README.md) | bob-cli-d2 hood | completed |
| [bob-cli-d2.2](bbugyi200.athena.bob-cli-d2.2.md) (session · 5) | bob-cli-d2 hood | completed 3, failed 2 |
| [bob-cli-d2.3](../agents/bbugyi200.athena.bob-cli-d2.3/README.md) | bob-cli-d2 hood | completed |
