# Agent: research.38.image

[Agent Hoods](../../README.md) / [bbugyi200](../../users/bbugyi200/README.md) / [apollo](../../users/bbugyi200/machines/apollo/README.md) / [research](../../users/bbugyi200/machines/apollo/hoods/research/README.md) / research.38.image

**Global name:** `bbugyi200.apollo.research.38.image` · **State:** active · **Source run:** `run-ac05e2db5b98d66a2854e7062ee477dc`

**Owner:** `bbugyi200.apollo` · **Project:** bob-cli · **Hood:** research

## Summary

- Model: gpt-6-astra
- Provider: codex
- Timing: 2026-11-04T15:22:28.604243+00:00
- Commits: 0
- Variables: [3](#variables)

## Files

[Prompt](prompt.md)

## Variables

| Variable | Value |
|---|---|
| `artifacts` | \[{kind: image, label: image:202611/recording\_past\_pomodoros/recording\_past\_pomodoros\_infographic.png, path: /home/bryan/.sase/artifacts/agents/gh\_bobs-org\_\_bob-cli/20261104093632/recording\_past\_pomod… |
| `diagrams` | {considered: 14, count: 2, manifest: 202611/recording\_past\_pomodoros/recording\_past\_pomodoros.diagrams.md, source\_ref: file:explicit:d4b8ea9c9321005ce552b7e7, status: ready} |
| `infographic` | {path: 202611/recording\_past\_pomodoros/recording\_past\_pomodoros\_infographic.png, prompt: "Use case: infographic-diagram.\\nCreate a polished editorial infographic for a software design research report… |

#### artifacts

```yaml
- kind: image
  label: image:202611/recording_past_pomodoros/recording_past_pomodoros_infographic.png
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261104093632/recording_past_pomodoros_infographic-499a3ce8c99f.png
  ref: file:explicit:f3fd5ef99fb61e44ba69d2e0
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_23/sase/repos/research/202611/recording_past_pomodoros/recording_past_pomodoros_infographic.png
- kind: markdown
  label: diagrams:202611/recording_past_pomodoros/recording_past_pomodoros.diagrams.md
  path: /home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261104093632/recording_past_pomodoros.diagrams-98c5bf060bde.md
  ref: file:explicit:06536db72cde2131922ad9c6
  source_path: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_23/sase/repos/research/202611/recording_past_pomodoros/recording_past_pomodoros.diagrams.md
```

#### diagrams

```yaml
considered: 14
count: 2
manifest: 202611/recording_past_pomodoros/recording_past_pomodoros.diagrams.md
source_ref: file:explicit:d4b8ea9c9321005ce552b7e7
status: ready
```

#### infographic

```yaml
path: 202611/recording_past_pomodoros/recording_past_pomodoros_infographic.png
prompt: |
  Use case: infographic-diagram.
  Create a polished editorial infographic for a software design research report titled "Recording past Pomodoros". It explains a PROPOSED capture feature, not a shipped feature. Portrait layout, roughly 3:4, high resolution, crisp exceptionally legible text. Warm ivory background, dark ink typography, restrained blue, green and amber accents, generous whitespace, thin timeline rules, precise flat geometric illustration. Professional technical magazine feel, no decorative cartoon tomato, no logos or watermark.
  
  Title: "Record past work with x="
  Eyebrow: "RECOMMENDED DESIGN · RESEARCH PROPOSAL"
  Subtitle: "One capture. A truthful timeline."
  
  Use four numbered panels, with the timelines visually dominant. All commands must reproduce the ASCII punctuation exactly. Use monospace for commands. Do not add code examples or facts.
  
  Panel 1, heading "01  One token, two responsibilities"
  Large syntax: "x=<E>[!][=<X>]"
  Under it, distinguish <E> as "Target + duration", the first ! as "Repair permission", and <X> as "Existing close selection".
  Small text: "Repair ! goes before the second =."
  Small footer: "Default: 5 blocks = 25 minutes"
  Keep the brackets visibly optional-notation, with no stray punctuation.
  
  Panel 2, heading "02  Type oldest to newest"
  Command: "x=build@2 x=fix@3"
  Clock label: "Now 09:21 → rounded anchor 09:25"
  Draw a clean horizontal time bar from 09:00 to 09:25, BUILD in blue occupying exactly 10 of 25 minutes (40%), FIX in green occupying exactly 15 of 25 minutes (60%). Boundary tick labels 09:00, 09:10, 09:25.
  In BUILD bar: "BUILD · 10m". In FIX bar: "FIX · 15m".
  Under timeline: "Later tokens push earlier windows backward."
  Secondary line: "Close clocks: BUILD 09:10 · FIX 09:21"
  Small explanation: "Each close uses min(window end, now)."
  Do not imply both windows end at 09:25.
  
  Panel 3, heading "03  Repair only an edge"
  Command: "x=3!"
  Before/after proportional timeline with shared range 08:55–09:25:
  Before: old PLAN spans 08:55–09:20 (25 minutes).
  After: old PLAN spans 08:55–09:10 (15 minutes), new session spans 09:10–09:25 (15 minutes).
  Label the old row "PLAN" and the new row "NEW".
  Clearly show time labels "08:55", "09:10", "09:20", "09:25" without overlap.
  Amber annotation: "10m taken from PLAN"
  Three compact rules: "Never split or erase" · "Running sessions protected" · "Unneeded ! is an error"
  Make clear this is trimming closed history, not permission to alter running sessions.
  
  Panel 4, heading "04  Plan the whole change"
  Three concise statements with small simple icons:
  "Validate the whole stack before edits"
  "Close explicit past rows; preserve task behavior"
  "Preview exact windows and every trim"
  Small explanatory line: "A dedicated operation avoids restarting a live timer."
  Bottom band: "No midnight crossing · No duration offsets · Grammar 11 proposed"
  Final compact note: "Bob computes the plan; the Mac displays it."
  
  Keep every label accurate and readable; no dense body paragraphs. Prioritize clean hierarchy and correct timing relationships over ornament. The image should work as a standalone research overview.
  
ref: file:explicit:f3fd5ef99fb61e44ba69d2e0
source_ref: file:explicit:d4b8ea9c9321005ce552b7e7
status: ready
tool: built-in image_gen
```

Values are truncated for display; see [meta.json](meta.json) for the full values.

## Neighbors

| Agent | Relation | State |
|---|---|---|
| [research.38.cdx](../bbugyi200.apollo.research.38.cdx/README.md) | research.38 hood | active |
| [research.38.cld](../bbugyi200.apollo.research.38.cld/README.md) | research.38 hood | active |
| [research.38.final](../bbugyi200.apollo.research.38.final/README.md) | research.38 hood | active |
| [research.38.gem](../bbugyi200.apollo.research.38.gem/README.md) | research.38 hood | active |
| [research.38.grk](../bbugyi200.apollo.research.38.grk/README.md) | research.38 hood | active |
| [research.38.linker](../bbugyi200.apollo.research.38.linker/README.md) | research.38 hood | active |
| [research.38.linker.w0](../../sessions/bbugyi200.apollo.research.38.linker.w0.md) (session · 3) | research.38 hood | active 1, completed 2 |
| [research.38.mus](../bbugyi200.apollo.research.38.mus/README.md) | research.38 hood | active |
| [research.0.cdx](../bbugyi200.apollo.research.0.cdx/README.md) | research hood | completed |
| [research.0.cld](../bbugyi200.apollo.research.0.cld/README.md) | research hood | completed |
| [research.0.final](../bbugyi200.apollo.research.0.final/README.md) | research hood | completed |
| [research.0.final.f1](../bbugyi200.apollo.research.0.final.f1/README.md) | research hood | completed |
| [research.0.image](../bbugyi200.apollo.research.0.image/README.md) | research hood | completed |
| [research.00.cdx](../bbugyi200.apollo.research.00.cdx/README.md) | research hood | dismissed |
| [research.00.cld](../bbugyi200.apollo.research.00.cld/README.md) | research hood | active |
| [research.00.final](../bbugyi200.apollo.research.00.final/README.md) | research hood | active |
| [research.00.gem](../bbugyi200.apollo.research.00.gem/README.md) | research hood | dismissed |
| [research.00.grk](../bbugyi200.apollo.research.00.grk/README.md) | research hood | active |
| [research.00.image](../bbugyi200.apollo.research.00.image/README.md) | research hood | dismissed |
| [research.00.linker](../bbugyi200.apollo.research.00.linker/README.md) | research hood | dismissed |
| [research.00.mus](../bbugyi200.apollo.research.00.mus/README.md) | research hood | dismissed |
| [research.01.cdx](../bbugyi200.apollo.research.01.cdx/README.md) | research hood | active |
| [research.01.cld](../bbugyi200.apollo.research.01.cld/README.md) | research hood | dismissed |
| [research.01.final](../bbugyi200.apollo.research.01.final/README.md) | research hood | dismissed |
| [research.01.gem](../bbugyi200.apollo.research.01.gem/README.md) | research hood | active |
| [research.01.grk](../bbugyi200.apollo.research.01.grk/README.md) | research hood | active |
| [research.01.image](../bbugyi200.apollo.research.01.image/README.md) | research hood | active |
| [research.01.linker](../bbugyi200.apollo.research.01.linker/README.md) | research hood | active |
| [research.01.mus](../bbugyi200.apollo.research.01.mus/README.md) | research hood | dismissed |
| [research.03.audio](../bbugyi200.apollo.research.03.audio/README.md) | research hood | active |
| [research.03.cdx](../bbugyi200.apollo.research.03.cdx/README.md) | research hood | active |
| [research.03.cld](../bbugyi200.apollo.research.03.cld/README.md) | research hood | active |
| [research.03.final](../bbugyi200.apollo.research.03.final/README.md) | research hood | active |
| [research.03.gem](../bbugyi200.apollo.research.03.gem/README.md) | research hood | dismissed |
| [research.03.grk](../bbugyi200.apollo.research.03.grk/README.md) | research hood | active |
| [research.03.image](../bbugyi200.apollo.research.03.image/README.md) | research hood | dismissed |
| [research.03.linker](../bbugyi200.apollo.research.03.linker/README.md) | research hood | dismissed |
| [research.03.mus](../bbugyi200.apollo.research.03.mus/README.md) | research hood | active |
| [research.04.audio](../bbugyi200.apollo.research.04.audio/README.md) | research hood | active |
| [research.04.cdx](../bbugyi200.apollo.research.04.cdx/README.md) | research hood | active |
| [research.04.cld](../bbugyi200.apollo.research.04.cld/README.md) | research hood | active |
| [research.04.final](../bbugyi200.apollo.research.04.final/README.md) | research hood | dismissed |
| [research.04.gem](../bbugyi200.apollo.research.04.gem/README.md) | research hood | dismissed |
| [research.04.grk](../bbugyi200.apollo.research.04.grk/README.md) | research hood | active |
| [research.04.image](../bbugyi200.apollo.research.04.image/README.md) | research hood | active |
| [research.04.linker](../bbugyi200.apollo.research.04.linker/README.md) | research hood | dismissed |
| [research.04.mus](../bbugyi200.apollo.research.04.mus/README.md) | research hood | active |
| [research.05.audio](../bbugyi200.apollo.research.05.audio/README.md) | research hood | active |
| [research.05.cdx](../bbugyi200.apollo.research.05.cdx/README.md) | research hood | active |
| [research.05.cld](../bbugyi200.apollo.research.05.cld/README.md) | research hood | active |
| [research.05.final](../bbugyi200.apollo.research.05.final/README.md) | research hood | active |
| [research.05.gem](../bbugyi200.apollo.research.05.gem/README.md) | research hood | dismissed |
| [research.05.grk](../bbugyi200.apollo.research.05.grk/README.md) | research hood | dismissed |
| [research.05.image](../bbugyi200.apollo.research.05.image/README.md) | research hood | active |
| [research.05.linker](../bbugyi200.apollo.research.05.linker/README.md) | research hood | dismissed |
| [research.05.linker.w0](../../sessions/bbugyi200.apollo.research.05.linker.w0.md) (session · 3) | research hood | dismissed 1, failed 2 |
| [research.06.audio](../bbugyi200.apollo.research.06.audio/README.md) | research hood | dismissed |
| [research.06.cdx](../bbugyi200.apollo.research.06.cdx/README.md) | research hood | active |
| … and 741 more in the [hood roster](../../users/bbugyi200/machines/apollo/hoods/research/README.md) | research hood | — |
