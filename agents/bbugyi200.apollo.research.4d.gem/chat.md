# Chat History - ace-run (research.4d.gem)

- **TIMESTAMP:** 2026-11-12 09:46:22 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.4d.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261112_093408.md`

## Prompt

%id(gem, clan=research.4d)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.4d.cdx`, `research.4d.cld`, `research.4d.grk`, `research.4d.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to make it so the `bob gmail sync` command starts archiving emails in gmail
automatically when appropriate.

- Namely, a corresponding email should be archived in gmail iff that email was labeled
  with "bob" and the corresponding task in Obsidian has been closed (indicating that the
  user is done with the task--or at least wants it out of sight).
- We should make it super clear to the user when we do this somehow since archiving an
  email, if done without user consent or knowledge, can be a destructive operation that
  harms their life (a missed email from a recruiter, for example).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

# Research Report: Automated Gmail Archiving for Closed Tasks in `bob gmail sync`

**Researcher:** `research.4d.gem`  
**Report File:** [`sase/repos/research/202611/gmail_sync_closed_task_archive__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/research/202611/gmail_sync_closed_task_archive__gem.md)  
**Registered Artifact:** `explicit:0afb5b43fc2466cc1e45a5d8` (`research:202611/gmail_sync_closed_task_archive__gem.md`)

---

## Executive Summary & Bottom Line

Closing the loop between task resolution in Obsidian and email triage in Gmail is an immensely high-value feature. Today, a user who completes a task in Obsidian must manually navigate to Gmail to archive the corresponding thread, imposing an annoying "double-management tax."

However, **unattended, unconditional background archiving during hourly cron (`bob gmail sync -q`) is extremely hazardous**. Without rigorous safety invariants, a user who closes a task could inadvertently cause an urgent incoming follow-up (such as a rescheduled job interview from a recruiter) to be silently re-archived out of sight every hour.

We have conducted independent research into the Gmail API data model, `gog` CLI mechanics, `bob-cli`'s sync engine, and user-facing CLI/notification aesthetics. We conclude that **this feature is an excellent idea, provided it is implemented with ironclad safety invariants, opt-in policies, and resurgent reply protections.**

---

## Key Critique: The Hidden Failure Modes

1. **The "Recruiter Resurgence" Trap (The Critical Failure Mode)**:
   - When a task in Obsidian is checked `- [x]`, the email is archived (removing Gmail's `INBOX` label).
   - If the counterparty later replies, Gmail naturally restores the thread to `INBOX`.
   - **The Hazard**: If `bob gmail sync` naively checks "is task `[x]`?", it will continuously re-archive that newly arrived reply every hour. The user will never see it!
   - **Mitigation**: Archival must be strictly anchored to the thread's message turn at closure time. Any incoming message beyond that turn invalidates archival, blocks re-archiving, and immediately resurrects the task in Obsidian with an unblocked notice.
2. **The "Silent Cron" Trap**:
   - `bob gmail sync -q` runs hourly in cron.
   - If an accidental checkbox toggle occurs in Obsidian, a thread could vanish from Gmail silently while the user is asleep.
   - **Mitigation**: Cron must never archive silently unless explicitly set to `archive_on_close: auto`. The default should be `ask` (prompting interactively in terminal syncs, skipping in background cron).
3. **The Multi-Task & Partial Closure Hazard**:
   - Multiple tasks in different notes might link the same thread (e.g. "Review proposal" vs "Wire funds").
   - **Mitigation**: A thread is eligible for archival iff **every** active linking task in the vault is closed (`[x]` or `[-]`), with at least one verified closed task present. Deleting a task line must never trigger an archive.
4. **OAuth Scope Escalation**:
   - `bob gmail sync` currently operates under read-only permissions (`gmail.readonly`).
   - Modifying thread labels requires `https://www.googleapis.com/auth/gmail.modify`.
   - `bob gmail login` must cleanly support an explicit consent step (e.g. `bob gmail login -s modify`), keeping the token bucket isolated.

---

## Recommended Refinements to Requirements

| Original Requirement | Proposed Refinement | Rationale |
| :--- | :--- | :--- |
| *Archive iff labeled with `bob`* | **Archive iff thread is enrolled in Bob (`EnrollmentFold`)** | Mobile users or Gmail filters might strip `bob` in Gmail while the task remains open and active in Obsidian. |
| *Archive in Gmail (remove from inbox)* | **Remove `INBOX`, remove `bob`, and apply `bob/done`** | Keeping `bob` indefinitely causes `threads.list q=label:bob` to page thousands of stale IDs every run. `bob/done` provides clean search hygiene and visible proof in Gmail. |
| *Automatic on task close* | **Add a 30-minute hysteresis cooldown + batch cap of 5** | Prevents rapid checking/unchecking from thrashing the Gmail API and stops mass-archiving accidents. |
| *Make it clear to the user* | **Interactive confirmation card + 1-click Undo command** | Provides terminal TTY clarity, OS desktop notifications, and zero-anxiety reversibility (`bob gmail unarchive <note>`). |

---

## User Experience & Visual Design

### 1. Interactive Sync Confirmation Card (`archive_on_close: ask`)
```text
╭─ 📦 Archive Completed Threads in Gmail? ───────────────────────────────────╮
│ The following threads have been closed in Obsidian and are ready to be     │
│ removed from your Gmail inbox:                                             │
│                                                                            │
│   1. ✉️ Staff Engineer Offer · TechCorp                                    │
│      Task:   jobs.md:42 (- [x] #task)                                      │
│      Action: Remove INBOX, bob ➔ Add bob/done                              │
│                                                                            │
│   2. ✉️ Apartment Lease Renewal · Ada                                      │
│      Task:   personal.md:18 (- [x] #task)                                  │
│      Action: Remove INBOX, bob ➔ Add bob/done                              │
│                                                                            │
│ Archive these 2 threads in Gmail? [y/N] y                                  │
╰────────────────────────────────────────────────────────────────────────────╯

✓ Archived 2 threads in Gmail.
  Tip: Run 'bob gmail unarchive <note>' at any time to restore to your inbox.
```

### 2. Resurgent Reply Safety Net Alert
```text
╭─ ⚠️  RESURGENT EMAIL REPLY DETECTED! ──────────────────────────────────────╮
│ An email thread with a closed task received a NEW incoming reply:          │
│                                                                            │
│   Thread: ✉️ Staff Engineer Offer · TechCorp                               │
│   Sender: Sarah Connor <sconnor@techcorp.com>                              │
│   Date:   2026-11-12 14:22 (13 minutes ago)                                │
│   Task:   jobs.md:42 was closed [x] on 2026-11-11                          │
│                                                                            │
│ Safety actions taken:                                                      │
│   ✓ Thread restored to Gmail INBOX (archival blocked)                      │
│   ✓ Reopened task in jobs.md:42:                                           │
│     - [ ] #task [[mail/2026/recruiter|✉️ Offer · TechCorp]] [unblocked:: today] │
╰────────────────────────────────────────────────────────────────────────────╯
```

---

## Recommended Phased Implementation

1. **Phase 1: Tooling & Preview**:
   - Update `scan.rs` to detect closed tasks.
   - Add `bob gmail sync -d` preview showing `would archive` rows.
   - Implement `bob gmail unarchive <note|id>` and `login -s modify`.
2. **Phase 2: Interactive Sync**:
   - Introduce `gmail.sync.archive_on_close: ask` with TTY confirmation cards.
   - Record durable `gmail.archived` events in `.bob/gmail/<host>.jsonl`.
   - Implement `bob` $\to$ `bob/done` label transition.
3. **Phase 3: Automated Cron with Resurgence Safety Net**:
   - Introduce `archive_on_close: auto` with a 30-minute cooldown and a 5-thread circuit breaker.
   - Deploy automated task resurgence for incoming replies on closed threads.

---

*The full detailed report, including complete Mermaid lifecycle diagrams, API payloads, and module blueprints, is preserved in [gmail_sync_closed_task_archive__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/research/202611/gmail_sync_closed_task_archive__gem.md).*
