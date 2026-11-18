# Session: bob-cli-mr.land

[Agent Hoods](../README.md) / [bbugyi200](../users/bbugyi200/README.md) / [athena](../users/bbugyi200/machines/athena/README.md) / [bob-cli-mr](../users/bbugyi200/machines/athena/hoods/bob-cli-mr/README.md) / bob-cli-mr.land

Owner: `bbugyi200.athena` · Hood: `bob-cli-mr` · Members: 9 · Bead: [bob-cli-mr](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-mr/README.md)

## Lineage

```mermaid
flowchart TD
  n0["bob-cli-mr.land--gate [completed]"]
  n1["bob-cli-mr.land--mon-1 [active]"]
  n0 --> n1
  n2["bob-cli-mr.land--2 [completed]"]
  n0 --> n2
  n3["bob-cli-mr.land--mon-0 [completed]"]
  n0 --> n3
  n4["bob-cli-mr.land--gate-0 [completed]"]
  n0 --> n4
  n5["bob-cli-mr.land--1 [completed]"]
  n0 --> n5
  n6["bob-cli-mr.land--plan [completed]"]
  n0 --> n6
  n7["bob-cli-mr.land--mon [failed]"]
  n0 --> n7
  n8["bob-cli-mr.land--code [completed]"]
  n0 --> n8
```

The diagram is an optional enhancement; the ordered table below contains the same lineage in accessible text.

| Role | Agent | State | Model / provider | Timing | Commits | Prompt | Chat |
|---|---|---|---|---|---:|---|---|
| <a id="member-gate"></a>gate | bob-cli-mr.land--gate | completed | gpt-6-astra / codex | 2026-11-17T22:36:01.652233+00:00 → 2026-11-17T22:36:09.392368+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-mr.land--gate/chat.md) |
| <a id="member-mon-1"></a>mon-1 | bob-cli-mr.land--mon-1 | active | muse-spark-1.3-contributor / muse | 2026-11-18T00:17:47.781241+00:00 | 0 | — | — |
| <a id="member-2"></a>2 | bob-cli-mr.land--2 | completed | muse-spark-1.3-contributor / muse | 2026-11-18T00:07:44.460644+00:00 → 2026-11-18T00:17:55.225043+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-mr.land--2/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-mr.land--2/chat.md) |
| <a id="member-mon-0"></a>mon-0 | bob-cli-mr.land--mon-0 | completed | grok-4.6 / grok | 2026-11-17T23:54:30.583374+00:00 → 2026-11-18T00:07:44.603696+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-mr.land--mon-0/chat.md) |
| <a id="member-gate-0"></a>gate-0 | bob-cli-mr.land--gate-0 | completed | muse-spark-1.3-contributor / muse | 2026-11-18T00:17:06.513784+00:00 → 2026-11-18T00:17:49.049450+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-mr.land--gate-0/chat.md) |
| <a id="member-1"></a>1 | bob-cli-mr.land--1 | completed | grok-4.6 / grok | 2026-11-17T23:34:50.167599+00:00 → 2026-11-17T23:56:42.369170+00:00 | [1](../agents/bbugyi200.athena.bob-cli-mr.land--1/README.md#commits) | [Prompt](../agents/bbugyi200.athena.bob-cli-mr.land--1/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-mr.land--1/chat.md) |
| <a id="member-plan"></a>plan | bob-cli-mr.land--plan | completed | gpt-6-astra / codex | 2026-11-17T22:22:08.015953+00:00 → 2026-11-17T23:24:26.353241+00:00 | 0 | [Prompt](../agents/bbugyi200.athena.bob-cli-mr.land--plan/prompt.md) | [Chat](../agents/bbugyi200.athena.bob-cli-mr.land--plan/chat.md) |
| <a id="member-mon"></a>mon | bob-cli-mr.land--mon | failed | grok-4.6 / grok | 2026-11-17T23:23:11.308616+00:00 → 2026-11-17T23:34:50.476016+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-mr.land--mon/chat.md) |
| <a id="member-code"></a>code | bob-cli-mr.land--code | completed | grok-4.6 / grok | 2026-11-17T22:36:46.273692+00:00 → 2026-11-17T23:24:26.353241+00:00 | 0 | — | [Chat](../agents/bbugyi200.athena.bob-cli-mr.land--code/chat.md) |

## Commits

| Role | Repo | Commit | Subject | Committed |
|---|---|---|---|---|
| 1 | bob-cli | [`da13fee`](https://github.com/bobs-org/bob-cli/commit/da13fee39e9c8c1dc2f7a12284bdb195ad48b705) | feat(scan): snapshot the full pre-planning read-set | 2026-11-17 18:56:04 EST |

## Variables

| Role | Variable | Value |
|---|---|---|
| plan | `artifacts` | \[{bead: bob-cli-mr, kind: file, label: T1 landing isolated TextBundle read-set race probe, path: /home/bryan/.sase/artifacts/agents/gh\_bobs-org\_\_bob-cli/20261117111759/bob-cli-mr-readset-probe-f913de… |

#### artifacts

**Role:** `plan`

```yaml
- bead: bob-cli-mr
  kind: file
  label: T1 landing isolated TextBundle read-set race probe
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261117111759/bob-cli-mr-readset-probe-f913de4b6c4f.py
  ref: file:explicit:bd831c44f897f151df7fe929
  source_path: /tmp/bob-cli-mr-readset-probe.py
- bead: bob-cli-mr
  kind: file
  label: T1 landing current-commit TextBundle race results
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261117111759/bob-cli-mr-readset-probe-9804cd631a19.log
  ref: file:explicit:1b54ca1c1f7d772c943b7307
  source_path: /tmp/bob-cli-mr-readset-probe.log
- bead: bob-cli-mr
  kind: markdown
  label: Validated T2 draft for the T1 repair coder to propose after closeout
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261117111759/sase_plan_backlog_triage_t2-59d988c38942.md
  ref: file:explicit:e68e1976353c86235b1d0e23
  source_path: /tmp/sase_plan_backlog_triage_t2.md
```

Values are truncated for display; see each member's agent meta.json for the full values.

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [bob-cli-mr.1](../agents/bbugyi200.athena.bob-cli-mr.1/README.md) | bob-cli-mr hood | completed |
| [bob-cli-mr.2](bbugyi200.athena.bob-cli-mr.2.md) (session · 3) | bob-cli-mr hood | completed 3 |
| [bob-cli-mr.3](bbugyi200.athena.bob-cli-mr.3.md) (session · 3) | bob-cli-mr hood | active 1, completed 2 |
| [bob-cli-mr.3.1.1](../agents/bbugyi200.athena.bob-cli-mr.3.1.1/README.md) | bob-cli-mr hood | completed |
| [bob-cli-mr.3.1.2](bbugyi200.athena.bob-cli-mr.3.1.2.md) (session · 5) | bob-cli-mr hood | completed 4, failed 1 |
| [bob-cli-mr.3.1.3](bbugyi200.athena.bob-cli-mr.3.1.3.md) (session · 3) | bob-cli-mr hood | completed 3 |
| [bob-cli-mr.3.1.land](bbugyi200.athena.bob-cli-mr.3.1.land.md) (session · 3) | bob-cli-mr hood | completed 3 |
