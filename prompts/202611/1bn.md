- **AGENTS:**
  - [bbugyi200.athena.1bn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bn.md)

#fork:1bn %model:gpt-6-astra %effort:xhigh

%macros_enabled:false

# Gate answered

**Decision:** Approve replacing the abandoned Bob Ledger Tools 1.110.2 deployment with
the ver

|                  |                                               |
| ---------------- | --------------------------------------------- |
| **Outcome**      | ANSWERED — Submit answers                     |
| **Answered via** | tui                                           |
| **Opened**       | 2026-11-11T21:45:12Z                          |
| **Answered**     | 2026-11-11T22:14:55Z                          |
| **Commands**     | 1 of 1 completed                              |
| **Gate**         | question/d3a7f32f-cfab-412d-9539-ca23592909bb |

## Results

### submit — `commands/submit`

```json
{
  "answers": [
    {
      "custom_feedback": null,
      "question": "Approve replacing the abandoned Bob Ledger Tools 1.110.2 deployment with the verified sub-project-rule build (currently 1.111.1), using bob plugins sync -F with its automatic backup? The old bundle carries keep-moving marks and the existing ledger features; the replacement retains that feature and includes the landed bank APIs and project/hide marks. Normal sync and clean-sync recovery both refused because no fetched commit matches the old uncommitted bundle byte for byte, so any unrecorded differences in it cannot be proven preserved. This approval applies only to the old athena deployment stamped 99ccca1 at 2026-11-11T19:43:12Z; recheck upstream and preserve later landed changes before deploying. The plugin AGENTS.md explicitly says never to use -F independently and to ask when the build is unlanded and abandoned. Task Status Cycler 1.49.1 is already synced; source implementation, Rust checks, and scratch Obsidian verification are complete.",
      "selected": ["Replace the old build"]
    }
  ],
  "global_note": ""
}
```

## Your next action

#gh:gh_bobs-org__bob-cli The 202611/revert_umbrella_leaf_rule.md plan file has been
reviewed and approved. Implement it now. %m:gpt-6-astra

### Questions and Answers

#### Q1: Ledger deploy

> Approve replacing the abandoned Bob Ledger Tools 1.110.2 deployment with the verified
> sub-project-rule build (currently 1.111.1), using bob plugins sync -F with its
> automatic backup? The old bundle carries keep-moving marks and the existing ledger
> features; the replacement retains that feature and includes the landed bank APIs and
> project/hide marks. Normal sync and clean-sync recovery both refused because no
> fetched commit matches the old uncommitted bundle byte for byte, so any unrecorded
> differences in it cannot be proven preserved. This approval applies only to the old
> athena deployment stamped 99ccca1 at 2026-11-11T19:43:12Z; recheck upstream and
> preserve later landed changes before deploying. The plugin AGENTS.md explicitly says
> never to use -F independently and to ask when the build is unlanded and abandoned.
> Task Status Cycler 1.49.1 is already synced; source implementation, Rust checks, and
> scratch Obsidian verification are complete.

- [x] **Replace the old build** — Back up and replace that protected bundle, then run
      the post-sync gate.
- [ ] **Leave deployment pending** — Keep the committed implementation and the currently
      deployed ledger bundle.

%macros_enabled:true
