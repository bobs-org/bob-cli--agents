# Session: bob-cli-j9.land

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [bob-cli-j9](../users/bbugyi200/machines/apollo/hoods/bob-cli-j9/README.md) / bob-cli-j9.land

Owner: `bbugyi200.apollo` · Hood: `bob-cli-j9` · Members: 3 · Bead: [bob-cli-j9](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-j9/README.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-j9.land--code [active]"]
  n1["bob-cli-j9.land--plan [active]"]
  n0 --> n1
  n2["bob-cli-j9.land--gate [completed]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-code"></a>code | bob-cli-j9.land--code | active | gpt-6-luna / codex | 2026-11-09T21:30:23.271673+00:00 | 0 | — | — |
| <a id="member-plan"></a>plan | bob-cli-j9.land--plan | active | gpt-6-astra / codex | 2026-11-09T21:14:41.197388+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-j9.land--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-j9.land--plan/chat.md) |
| <a id="member-gate"></a>gate | bob-cli-j9.land--gate | completed | gpt-6-astra / codex | 2026-11-09T21:29:46.869832+00:00 → 2026-11-09T21:29:58.338695+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-j9.land--gate/chat.md) |

## Variables

| Role | Variable | Value |
|---|---|---|
| plan | `artifacts` | \[{kind: file, label: j9 landing CI follow-up evidence, path: /home/bryan/.sase/artifacts/agents/gh\_bobs-org\_\_bob-cli/20261109121923/j9\_land\_ci\_evidence-3e288135b236.txt, ref: file:explicit:1d6d71ab02… |

#### artifacts

**Role:** `plan`

```yaml
- kind: file
  label: j9 landing CI follow-up evidence
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261109121923/j9_land_ci_evidence-3e288135b236.txt
  ref: file:explicit:1d6d71ab0242c32754b782ca
```

Values are truncated for display; see each member's agent meta.json for the full values.

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-j9.1](../agents/bbugyi200.apollo.bob-cli-j9.1/README.md) | bob-cli-j9 hood | completed |
| [bob-cli-j9.2](bbugyi200.apollo.bob-cli-j9.2.md) (session · 3) | bob-cli-j9 hood | completed 2, failed 1 |
| [bob-cli-j9.3](bbugyi200.apollo.bob-cli-j9.3.md) (session · 5) | bob-cli-j9 hood | completed 4, failed 1 |
| [bob-cli-j9.4](../agents/bbugyi200.apollo.bob-cli-j9.4/README.md) | bob-cli-j9 hood | completed |
