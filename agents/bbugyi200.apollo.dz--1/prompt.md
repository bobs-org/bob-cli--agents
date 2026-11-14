#fork:dz
%model:opus
%effort:xhigh

%macros_enabled:false
# Gate answered

**Decision:** bob-cli-kx is done except its last phase, kx.5: the live enable on the Mac with 

| | |
| --- | --- |
| **Outcome** | ANSWERED — Submit answers |
| **Answered via** | tui |
| **Opened** | 2026-11-14T14:39:42Z |
| **Answered** | 2026-11-14T14:41:07Z |
| **Commands** | 1 of 1 completed |
| **Gate** | question/e8c14043-00fc-4b09-9336-a347238b8142 |

## Results

### submit — `commands/submit`

```json
{
  "answers": [
    {
      "custom_feedback": null,
      "question": "bob-cli-kx is done except its last phase, kx.5: the live enable on the Mac with you in the loop. kx.5 has been waiting for a published release, but every daily release has failed since v0.5.0. Today I fixed four master blockers (macOS ptsname_r, gcal test l2, bank completion, a Gmail test flake). With those fixed, CI now reaches the macOS tests and finds 15 failures there in unrelated areas: tasks l9 and kl, plus a gcal-ack termios issue noted on epic l5. So a release is probably days away. Your Mac already runs a master build from `just install-all` (9a6013a2, installed 08:04 today) that includes all of the archive work: login -s modify, sync -c/-n, unarchive, and the doctor rows. How should kx.5 proceed?",
      "selected": [
        "Proceed now on the Mac's master build"
      ]
    },
    {
      "custom_feedback": null,
      "question": "Archiving needs a gmail.modify grant that only you can give, through interactive OAuth in a terminal on the Mac: `bob gmail login -s modify`. It has to come BEFORE I turn on `gmail.sync.archive: on`. Otherwise the hourly :07 `bob gmail sync -q` cron fails with exit 2 for the missing scope. If you're proceeding now, you can run it before you answer.",
      "selected": [
        "Done: I ran `bob gmail login -s modify` on the Mac"
      ]
    }
  ],
  "global_note": ""
}
```

## Your next action

#gh:gh_bobs-org__bob-cli Can you help me finish whatever work remains on the bob-cli-kx bead and then close it? %m:@xlarge

### Questions and Answers

#### Q1: kx.5 build

> bob-cli-kx is done except its last phase, kx.5: the live enable on the Mac with you in the loop. kx.5 has been waiting for a published release, but every daily release has failed since v0.5.0. Today I fixed four master blockers (macOS ptsname_r, gcal test l2, bank completion, a Gmail test flake). With those fixed, CI now reaches the macOS tests and finds 15 failures there in unrelated areas: tasks l9 and kl, plus a gcal-ack termios issue noted on epic l5. So a release is probably days away. Your Mac already runs a master build from `just install-all` (9a6013a2, installed 08:04 today) that includes all of the archive work: login -s modify, sync -c/-n, unarchive, and the doctor rows. How should kx.5 proceed?

- [x] **Proceed now on the Mac's master build** — Waive the plan's 'released build only' rule for this enable and record the pinned SHA in the bead. Next, after your modify grant: opt in through chezmoi, run sync -d, approve the exact archive set in a gate, run the confirmed live sync, verify, test unarchive and let-go, then close kx.5 and kx.
- [ ] **Wait for a published release** — kx stays open. A successor stages a release monitor and resumes the same runbook once a release contains the archive receipts commit (610b809f).
- [ ] **Close kx now; track the live enable as a separate task** — Close kx.5 and kx as superseded, with a new task bead for the gated live enable and verification. Nothing in Gmail changes today.

#### Q2: modify grant

> Archiving needs a gmail.modify grant that only you can give, through interactive OAuth in a terminal on the Mac: `bob gmail login -s modify`. It has to come BEFORE I turn on `gmail.sync.archive: on`. Otherwise the hourly :07 `bob gmail sync -q` cron fails with exit 2 for the missing scope. If you're proceeding now, you can run it before you answer.

- [x] **Done: I ran `bob gmail login -s modify` on the Mac** — I'll confirm with `bob gmail doctor` (scopes should include modify) before changing any config.
- [ ] **Not yet** — I'll do everything that doesn't need the grant, then ask again before opting in.
- [ ] **Not applicable** — Waiting for a release or closing kx, so no grant is needed now.

%macros_enabled:true