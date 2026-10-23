# Chat History - ace-run (research.55.gem)

- **TIMESTAMP:** 2026-10-23 06:44:48 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.55.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261023_063016.md`

## Prompt

%id(gem, clan=research.55)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.55.cdx`, `research.55.cld`, `research.55.grk`, `research.55.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add support for a new "rotten log" (a good glossary entry should be
added for this new term).

- This should work like the work log, but the prompt for an optional rotten log entry
  should occur when a rotten task (during our GTD morning review, for example) is
  refreshed using the `<alt+f>` or `<ctrl+alt+f>` keymaps.
- The goal of this change is to add a visual indication (and an audit trail) that shows
  how many times (and when and why) a task has been manually refreshed.

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

I have completed the independent research investigation on introducing a **Rotten Log** and registered the deliverable as a durable SASE artifact.

The full research report has been written to:
[`rotten_log_and_refresh_audit_trail__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/rotten_log_and_refresh_audit_trail__gem.md)

And registered as:
`research:202610/rotten_log_and_refresh_audit_trail__gem.md` (Artifact ID: `explicit:48396382f3f85bea2b3fa36c`)

---

### Key Findings & Executive Summary

#### 1. Critique: Is This a Good Idea?
**Yes, but not as literally written.**
- **The Core Need is Real:** Today, Bob suffers from the *"amnesia of keeps"*. When a task sits in the backlog and is repeatedly refreshed across several weeks, there is zero memory of *why* Bryan decided not to do it, schedule it, or drop it. When Bob's Approved Decay card eventually triggers at keep 3 (`decisions:rotten-keeps-use-priority-decay`), Bryan must make a high-stakes decision without the historical context of previous reviews.
- **The Morning Review Velocity Threat:** A live vault check reveals that Bryan performed **41 task refreshes today alone**. In a typical morning GTD review walk, 15 to 30 tasks can be in the ROTTEN tier. If `<ctrl+alt+f>` or `<alt+f>` opened an interactive modal dialog on *every single rotten task*, Bryan would face **15–30 modal interruptions every morning**. Even with `Enter` to skip, the visual flicker and doubled keystrokes would destroy the cadence and flow of the review walk (`decisions:answering-advances-the-walk`).
- **The "Counter vs. Optional Prompt" Contradiction:** If the log entry is optional (like `WORK LOG`), pressing `Enter` without typing must write *nothing* to avoid note clutter. But if blank submits write nothing, the count of sub-bullets in the log will *not* reflect how many times the task was refreshed.

#### 2. Justified Requirement Adjustments
1. **Dual-Track Separation of Concerns:**
   - **Quantitative Count ("How many times"):** Governed strictly by `[keeps:: N]` on the task line and visual pips (`◔ 3d ••`) in the freshness mark.
   - **Qualitative Audit ("When and why"):** Governed strictly by `🍂 **ROTTEN LOG**` sub-bullets (`*YYYY-MM-DD* — <reason>`), which are written *only* when a meaningful reason is entered.
2. **Strict "Blank Enter Writes Nothing" Rule:** Pressing `Enter` with an empty prompt stamps `fresh`, increments `[keeps:: N]`, advances the walk (if `<ctrl+alt+f>`), and writes **zero** bullets.
3. **Protect Review Velocity via Progressive Friction:**
   - **Keep 1 (First Rotten Review):** Zero modal interruption (fast 1-keypress keep and advance). Keep 1 is routine backlog aging.
   - **Keep 2+ (Subsequent Rotten Reviews):** Modal prompt appears: *"Why keep this task again? (optional · ↵ to skip)"*.
   *(Alternative: `<ctrl+alt+f>` remains fast unprompted keep-and-advance, while `<alt+f>` stay opens the deliberate annotation modal).*
4. **Decay Limit Integration:** When `keeps` hits the limit (default 3), the existing Approved Decay card opens. Selecting `⌥F Keep anyway` automatically prompts for or writes a Rotten Log entry.
5. **Freshness Mark Tooltip Enrichment:** Display the latest Rotten Log note directly inside the `bob-ledger-tools` hover tooltip (e.g. `Last kept 2026-10-16: "Waiting on upstream PR"`), providing instant visual context during review without expanding child blocks.

---

### SASE Glossary Entry

```markdown
# Rotten Log

*Requested · project*

aka rotten review log, keep log, review log

A task-local history of manual review keeps and deferral rationales, stored as
a `🍂 **ROTTEN LOG**` direct child bullet with newest-first dated sub-bullets
(`*YYYY-MM-DD* — <reason>`). When `<alt+f>` or `<ctrl+alt+f>` refreshes an
exact due-Ready rotten task during the GTD morning review walk, the reviewer
is optionally prompted for an explanation of why the task is being kept
rather than scheduled, delegated, or dropped. A non-empty summary is
prepended under the marker; a blank submit (`Enter`) refreshes the task and
increments `[keeps:: N]` without inserting a bullet. The log provides a
durable, human-readable audit trail that preserves review context across
weeks and informs the Approved Decay decision card when the keep limit is
reached.
```

---

### Technical Blueprint Summary

- **`bob-cli` (Rust Core):**
  - Add `ManagedTaskLogKind::Rotten` and `ROTTEN_LOG_EMOJI = "🍂"` in `src/native/capture/sub_bullet.rs`.
  - Update `MANAGED_TASK_LOG_LABELS` to parse `ROTTEN LOG` and `Rotten log`.
  - Position `ROTTEN LOG` directly before `WORK LOG` in the managed child block ordering.
- **`bob-plugins` (Obsidian Plugins):**
  - **`bob-navigation-hotkeys`:** Implement `FreshnessRottenLogModal` (modeled after `FreshnessRefreshSummaryModal`), `insertLaneRottenLogEntry`, and `planFreshStampBatchWithRottenLogs` in `refreshTaskFreshnessOnTasks`.
  - **`bob-ledger-tools`:** Enrich `freshnessMarkModel` to extract the latest Rotten Log entry and surface it inside the review tooltip.
  - **`block-id-prompt` & `task-status-cycler`:** Update child block boundary regexes to recognize `ROTTEN_LOG_PARENT_RE`.
