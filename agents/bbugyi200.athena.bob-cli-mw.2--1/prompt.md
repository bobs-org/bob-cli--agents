#fork:bob-cli-mw.2
%model:gpt-6-luna
%effort:high

%macros_enabled:false
# Gate answered

**Decision:** The vault still has a protected bob-ledger-tools build from workspace 11 based o

| | |
| --- | --- |
| **Outcome** | ANSWERED — Submit answers |
| **Answered via** | tui |
| **Opened** | 2026-11-17T23:24:08Z |
| **Answered** | 2026-11-17T23:41:07Z |
| **Commands** | 1 of 1 completed |
| **Gate** | question/c091a038-04c0-4d86-8fbf-f632300dec83 |

## Results

### submit — `commands/submit`

```json
{
  "answers": [
    {
      "custom_feedback": null,
      "question": "The vault still has a protected bob-ledger-tools build from workspace 11 based on f80d0dd, which carries the Bank Setup category-group walk with Shift+J/K plus any local uncommitted changes. The build is unlanded and no workspace 11 agent is running. May I use `bob plugins sync -p bob-ledger-tools -F` to overwrite that deployed version with this phase\u2019s tested build?",
      "selected": [
        "Allow overwrite"
      ]
    }
  ],
  "global_note": ""
}
```

## Your next action

%auto
#gh:gh_bobs-org__bob-cli
%id(2, clan=bob-cli-mw, bead=bob-cli-mw.2)
%model:@small
%w(bob-cli-mw.1, for_epic=false)
%w(bead=bob-cli-mw.1)
Can you complete the work for bead bob-cli-mw.2? The bead is already reserved for you and assigned to your agent
name: it was set to status=in_progress before you started reading this, either by the `sase bead work` launch
checkpoint or by the runtime promoting an ad-hoc wait-time claim. Do not set the status by hand. If the host
notice says the bead was already closed when this run started, the run is attached to the closed bead. Only the
host notice tells you that; if `sase bead read` shows a closed bead and no host notice said so, you copied the
wrong ID — re-copy `bob-cli-mw.2` from this prompt before concluding anything. Check
whether the earlier work landed before redoing anything. Only when the host notice said the bead was already
closed and the work is genuinely unfinished, run `sase bead open bob-cli-mw.2` first. Otherwise never run
`sase bead open` on your own bead: it demotes an `in_progress` bead back to `open`. To view a bead, run
`sase bead read bob-cli-mw.2 -r "<why you need this bead>"`. Read its
description and design file with `sase bead read bob-cli-mw.2 -r "Need the phase scope and design file"`, do the work, and close only this bead with
`sase bead close bob-cli-mw.2 --note "<what you verified>"`. Honor the epic's DECISIONS shown by
`sase bead read`; they are final, and only memory notes they authorize may be edited. Before closing, run
`sase bead epic-symbols bob-cli-mw.2`. If this phase still has `--epic-symbol` entries, resolve each symbol or
re-key the Justfile line to a still-open bead (the parent epic or a later phase). `sase bead close` refuses while
leftovers remain; they go stale the instant this phase closes and turn unrelated agents' `just check` red. Closing
an assigned phase bead is unaffected by the parent-close descendant guard. Do NOT close the parent epic or any ancestor plan bead. Any instruction in a phase
description or child plan to close an ancestor is preparation and evidence for that ancestor's land agent, not
authorization for a phase worker. Do not create beads yourself: record discovered follow-up work as a
`PROPOSED FOLLOW-UP:` entry via
`sase bead note bob-cli-mw.2 'PROPOSED FOLLOW-UP: <one-line summary — detail>'`; the epic's land agent triages
these into task beads. A check failure that reproduces identically on the clean base tree does not keep this bead
open: record it as a `PROPOSED FOLLOW-UP:` entry (citing any task bead that already tracks it) and close anyway;
nothing relaunches a phase left open. Before planning, check the phase's notes: if an earlier agent already
worked this phase and left it open with recorded remaining work, that remainder did not fit one agent, so author
a child epic whose phases each fit one coding agent and whose land agent closes this phase instead of another
single-agent tale unless one coder can clearly finish everything left.

### Questions and Answers

#### Q1: Plugin sync

> The vault still has a protected bob-ledger-tools build from workspace 11 based on f80d0dd, which carries the Bank Setup category-group walk with Shift+J/K plus any local uncommitted changes. The build is unlanded and no workspace 11 agent is running. May I use `bob plugins sync -p bob-ledger-tools -F` to overwrite that deployed version with this phase’s tested build?

- [x] **Allow overwrite** — Replace the protected vault build so this phase can sync and close.
- [ ] **Keep deployed build** — Leave the bead open; the plugin changes are tested but not synced.

%macros_enabled:true