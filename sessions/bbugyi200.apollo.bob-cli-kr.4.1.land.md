# Session: bob-cli-kr.4.1.land

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [apollo](../users/bbugyi200/machines/apollo/README.md) / [bob-cli-kr](../users/bbugyi200/machines/apollo/hoods/bob-cli-kr/README.md) / bob-cli-kr.4.1.land

Owner: `bbugyi200.apollo` · Hood: `bob-cli-kr` · Members: 3 · Bead: [bob-cli-kr.4.1](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-kr/bob-cli-kr.4.1.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-kr.4.1.land--code [active]"]
  n1["bob-cli-kr.4.1.land--plan [active]"]
  n0 --> n1
  n2["bob-cli-kr.4.1.land--gate [completed]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-code"></a>code | bob-cli-kr.4.1.land--code | active | gpt-6-luna / codex | 2026-11-12T23:08:15.053435+00:00 | 0 | — | — |
| <a id="member-plan"></a>plan | bob-cli-kr.4.1.land--plan | active | gpt-6-astra / codex | 2026-11-12T22:47:35.425640+00:00 | 0 | [Prompt](../agents/bbugyi200.apollo.bob-cli-kr.4.1.land--plan/prompt.md) | [Chat](../agents/bbugyi200.apollo.bob-cli-kr.4.1.land--plan/chat.md) |
| <a id="member-gate"></a>gate | bob-cli-kr.4.1.land--gate | completed | gpt-6-astra / codex | 2026-11-12T23:07:29.108285+00:00 → 2026-11-12T23:07:48.172127+00:00 | 0 | — | [Chat](../agents/bbugyi200.apollo.bob-cli-kr.4.1.land--gate/chat.md) |

## Variables

| Role | Variable | Value |
|---|---|---|
| plan | `artifacts` | \[{bead: bob-cli-kr.4.1, kind: file, label: Schema Card landing baseline test failures, path: /home/bryan/.sase/artifacts/agents/gh\_bobs-org\_\_bob-cli/20261112134814/kr41-baseline-a76c2bf7e0e3.log, ref… |

#### artifacts

**Role:** `plan`

```yaml
- bead: bob-cli-kr.4.1
  kind: file
  label: Schema Card landing baseline test failures
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261112134814/kr41-baseline-a76c2bf7e0e3.log
  ref: file:explicit:5b5c41bf3b75a57541e9c4e2
  source_path: /tmp/kr41-baseline.log
- bead: bob-cli-kr.4.1
  kind: file
  label: Schema Card landing focused tests
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261112134814/kr41-focused-e663bcc98f1d.log
  ref: file:explicit:1c7c9eafce8f222b82df1c4d
  source_path: /tmp/kr41-focused.log
```

Values are truncated for display; see each member's agent meta.json for the full values.

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-kr.4](bbugyi200.apollo.bob-cli-kr.4.md) (session · 3) | ancestor | active 1, completed 2 |
| [bob-cli-kr.4.1.1](../agents/bbugyi200.apollo.bob-cli-kr.4.1.1/README.md) | bob-cli-kr.4.1 hood | completed |
| [bob-cli-kr.4.1.2](bbugyi200.apollo.bob-cli-kr.4.1.2.md) (session · 3) | bob-cli-kr.4.1 hood | completed 3 |
| [bob-cli-kr.4.1.3](../agents/bbugyi200.apollo.bob-cli-kr.4.1.3/README.md) | bob-cli-kr.4.1 hood | completed |
| [bob-cli-kr.4.1.4](../agents/bbugyi200.apollo.bob-cli-kr.4.1.4/README.md) | bob-cli-kr.4.1 hood | completed |
| [bob-cli-kr.1](bbugyi200.apollo.bob-cli-kr.1.md) (session · 3) | bob-cli-kr hood | completed 2, failed 1 |
| [bob-cli-kr.2](bbugyi200.apollo.bob-cli-kr.2.md) (session · 3) | bob-cli-kr hood | active 1, completed 2 |
| [bob-cli-kr.2.1.1](../agents/bbugyi200.apollo.bob-cli-kr.2.1.1/README.md) | bob-cli-kr hood | completed |
| [bob-cli-kr.2.1.2](../agents/bbugyi200.apollo.bob-cli-kr.2.1.2/README.md) | bob-cli-kr hood | completed |
| [bob-cli-kr.2.1.3](../agents/bbugyi200.apollo.bob-cli-kr.2.1.3/README.md) | bob-cli-kr hood | completed |
| [bob-cli-kr.2.1.land](bbugyi200.apollo.bob-cli-kr.2.1.land.md) (session · 3) | bob-cli-kr hood | completed 3 |
| [bob-cli-kr.3](bbugyi200.apollo.bob-cli-kr.3.md) (session · 3) | bob-cli-kr hood | completed 3 |
| [bob-cli-kr.land](../agents/bbugyi200.apollo.bob-cli-kr.land/README.md) | bob-cli-kr hood | waiting |
