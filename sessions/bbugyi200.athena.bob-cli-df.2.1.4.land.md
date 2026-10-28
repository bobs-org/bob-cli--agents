# Session: bob-cli-df.2.1.4.land

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-df](../users/bbugyi200/machines/athena/hoods/bob-cli-df/README.md) / bob-cli-df.2.1.4.land

Owner: `bbugyi200.athena` · Hood: `bob-cli-df` · Members: 3 · Bead: [bob-cli-df.2.1.4](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-df/bob-cli-df.2.1.4.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-df.2.1.4.land--mon [failed]"]
  n1["bob-cli-df.2.1.4.land--gate [failed]"]
  n0 --> n1
  n2["bob-cli-df.2.1.4.land--plan [failed]"]
  n0 --> n2
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-mon"></a>mon | bob-cli-df.2.1.4.land--mon | failed | gpt-6-astra / codex | 2026-10-28T08:35:20.367315+00:00 → 2026-10-28T08:37:38.680995+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.4.land--mon/chat.md) |
| <a id="member-gate"></a>gate | bob-cli-df.2.1.4.land--gate | failed | gpt-6-astra / codex | 2026-10-28T08:34:21.515710+00:00 → 2026-10-28T08:35:21.233186+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.4.land--gate/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-df.2.1.4.land--plan | failed | gpt-6-astra / codex | 2026-10-28T08:16:23.313836+00:00 → 2026-10-28T08:35:31.704479+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-df.2.1.4.land--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-df.2.1.4.land--plan/chat.md) |

## Variables

| Role | Variable | Value |
|---|---|---|
| plan | `artifacts` | \[{bead: bob-cli-df.2.1.4, kind: file, label: Artifact-link remaining-order and quarantine path probes, path: /home/bryan/.sase/artifacts/agents/gh\_bobs-org\_\_bob-cli/20261028020918/sase\_landing\_probe\_… |

#### artifacts

**Role:** `plan`

```yaml
- bead: bob-cli-df.2.1.4
  kind: file
  label: Artifact-link remaining-order and quarantine path probes
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261028020918/sase_landing_probe_df_2_1_4-c350720cefaa.py
  ref: file:explicit:93c39bb2954df550e568ab38
- bead: bob-cli-df.2.1.4
  kind: markdown
  label: Artifact-link repair landing audit and follow-up dispositions
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261028020918/sase_landing_audit_df_2_1_4-a1a80e741322.md
  ref: file:explicit:4ea0ec4a426fca44ad0e64e8
```

Values are truncated for display; see each member's agent meta.json for the full values.

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-df.2](bbugyi200.athena.bob-cli-df.2.md) (session · 3) | ancestor | failed 3 |
| [bob-cli-df.2.1.4.1](bbugyi200.athena.bob-cli-df.2.1.4.1.md) (session · 11) | bob-cli-df.2.1.4 hood | completed 6, failed 5 |
| [bob-cli-df.2.1.4.2](bbugyi200.athena.bob-cli-df.2.1.4.2.md) (session · 3) | bob-cli-df.2.1.4 hood | completed 2, failed 1 |
| [bob-cli-df.2.1.4.3.1](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.1/README.md) | bob-cli-df.2.1.4 hood | completed |
| [bob-cli-df.2.1.4.3.2](bbugyi200.athena.bob-cli-df.2.1.4.3.2.md) (session · 5) | bob-cli-df.2.1.4 hood | active 1, completed 2, failed 2 |
| [bob-cli-df.2.1.4.3.land](../agents/bbugyi200.athena.bob-cli-df.2.1.4.3.land/README.md) | bob-cli-df.2.1.4 hood | waiting |
| [bob-cli-df.2.1.1](../agents/bbugyi200.athena.bob-cli-df.2.1.1/README.md) | bob-cli-df.2.1 hood | completed |
| [bob-cli-df.2.1.2](../agents/bbugyi200.athena.bob-cli-df.2.1.2/README.md) | bob-cli-df.2.1 hood | completed |
| [bob-cli-df.2.1.3](bbugyi200.athena.bob-cli-df.2.1.3.md) (session · 9) | bob-cli-df.2.1 hood | completed 5, failed 4 |
| [bob-cli-df.2.1.land](bbugyi200.athena.bob-cli-df.2.1.land.md) (session · 3) | bob-cli-df.2.1 hood | failed 3 |
| [bob-cli-df.1](../agents/bbugyi200.athena.bob-cli-df.1/README.md) | bob-cli-df hood | completed |
| [bob-cli-df.3](../agents/bbugyi200.athena.bob-cli-df.3/README.md) | bob-cli-df hood | completed |
| [bob-cli-df.4](bbugyi200.athena.bob-cli-df.4.md) (session · 3) | bob-cli-df hood | failed 3 |
| [bob-cli-df.4.1.1](bbugyi200.athena.bob-cli-df.4.1.1.md) (session · 3) | bob-cli-df hood | completed 2, failed 1 |
| [bob-cli-df.4.1.2](bbugyi200.athena.bob-cli-df.4.1.2.md) (session · 3) | bob-cli-df hood | completed 2, failed 1 |
| [bob-cli-df.4.1.3](../agents/bbugyi200.athena.bob-cli-df.4.1.3/README.md) | bob-cli-df hood | completed |
| [bob-cli-df.4.1.4](bbugyi200.athena.bob-cli-df.4.1.4.md) (session · 3) | bob-cli-df hood | completed 2, failed 1 |
| [bob-cli-df.4.1.land](bbugyi200.athena.bob-cli-df.4.1.land.md) (session · 3) | bob-cli-df hood | completed 2, failed 1 |
| [bob-cli-df.land](../agents/bbugyi200.athena.bob-cli-df.land/README.md) | bob-cli-df hood | waiting |
