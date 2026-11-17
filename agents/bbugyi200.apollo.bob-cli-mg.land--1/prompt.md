#fork:bob-cli-mg.land
%model:gpt-6-luna
%effort:xhigh

%macros_enabled:false
# Gate answered

**Decision:** May I overwrite the deployed bob-ledger-tools bundle with the current source and

| | |
| --- | --- |
| **Outcome** | ANSWERED — Submit answers |
| **Answered via** | tui |
| **Opened** | 2026-11-17T01:42:25Z |
| **Answered** | 2026-11-17T01:52:18Z |
| **Commands** | 1 of 1 completed |
| **Gate** | question/f5589f1b-8f94-4f54-9d13-be84ef3223fe |

## Results

### submit — `commands/submit`

```json
{
  "answers": [
    {
      "custom_feedback": null,
      "question": "May I overwrite the deployed bob-ledger-tools bundle with the current source and discard any unpublished differences in that bundle? The protected bundle was built on commit 866bb77, which added album arrangement editing and one-envelope save; the current source also includes the approved Bank Period balance readout. The deployment stamp cannot be matched to any reachable commit. Overwriting completes the approved plugin repair; keeping the bundle leaves plugin deployment unfinished.",
      "selected": [
        "Overwrite bundle"
      ]
    }
  ],
  "global_note": ""
}
```

## Your next action

%model:@medium
#gh:gh_bobs-org__bob-cli
@plan:202611/wf_closing_landing_repairs.md

The above plan has been reviewed and approved. Implement it now.


### Questions and Answers

#### Q1: Plugin deployment

> May I overwrite the deployed bob-ledger-tools bundle with the current source and discard any unpublished differences in that bundle? The protected bundle was built on commit 866bb77, which added album arrangement editing and one-envelope save; the current source also includes the approved Bank Period balance readout. The deployment stamp cannot be matched to any reachable commit. Overwriting completes the approved plugin repair; keeping the bundle leaves plugin deployment unfinished.

- [x] **Overwrite bundle** — Replace the protected deployment with the current source and finish the repair.
- [ ] **Keep installed bundle** — Preserve it and stop before plugin deployment.

%macros_enabled:true