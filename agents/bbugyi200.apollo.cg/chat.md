# Chat History - ace-run (cg)

- **TIMESTAMP:** 2026-11-04 17:26:08 EST
- **MODEL:** claude/opus
- **AGENT:** cg

## Prompt

#gh:gh_bobs-org__bob-cli The `<alt+p>` keymap in Obsidian is supposed to behave like the user pressed
`1` on the task card iff the currently selected task does not have a priority. If the
task does have a priority, we should use the recommendation that is shown in the footer
of Obsidian, which should always be shown for ready tasks with a `priority` field. Do
all of these constraints currently hold? If not, why not? Can we fix this? Should we?
Make sure your research is concise and easy to read (bonus points for adding a good
visual or two). 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete. %m:@xlarge

## Response

Tracing the Alt+P handler (`rollByRecommendation`) through the task card in bob-plugins now.

Found the footer consumer (bob-ledger-tools freshness footer); now checking how it gates the Alt+P preview.

Comparing the `1` key path against Alt+P's "assign" write to see if they're truly equivalent.

Docs confirm the footer hint is scoped to review rows only. Checking the Task Card docs table and the vault config next.

Checking whether the deployed vault copy differs in the Alt+P paths, and the live priority config.

Running the existing Alt+P tests, then a probe comparing Alt+P against an actual `1` keypress.

Got the design rationale for Alt+P → P1; now reading the original plan's footer-scope rationale.

Probe done: Alt+P and `1` write identical lines in every Ready case. Running the existing Alt+P/footer test suites to confirm the current contract.

All 55 tests pass. Now sizing the footer gap against the real vault: Ready P-tasks on vs off today's review queue.

Today's vault: 18 of 21 real Ready P-tasks sit on the queue (hint shows); the other 3 are `#hide` project lines (no hint). Loading the diagram skill before writing the report.

Figure 1 reads well. Figure 2 has a PRE/POST branch that doesn't apply to Ready P-tasks; dropping it and re-rendering.

Writing the report now. First, a small label fix on figure 2 ("kept today" → "kept recently", since a kept task stays off the queue for its whole interval), then a re-render to check it.

Report written. Verifying two evidence claims before registering it: which commit added the footer hint, and that the vault/repo diffs are really unrelated.

Evidence section is correct. Registering the report as a durable artifact.

Registered. Finishing the turn through `/sase_final`.

Two of your three constraints hold today. The third, that the footer always shows the hint, does not, and that is by design rather than a bug. I've written the report with two diagrams and registered it as `research:202611/alt_p_priority_contract/alt_p_priority_contract.md`.

| # | Constraint | Holds? | Why |
|---|---|---|---|
| 1 | No priority → same as pressing `1` | ✅ Yes, for every Ready task | Since commit `14dc9d9` (Oct 30), Alt+P sets the level bound to key `1` (P1) through the same code that writes for `1`. I ran both on test tasks and the writes were identical. |
| 2 | Has a priority → use the footer's recommendation | ✅ Yes | Alt+P and the footer compute their recommendation the same way, on the same cursor line. |
| 3 | Footer always shows it for Ready tasks with a priority | ❌ No | The hint only appears while the cursor is on a row that is due in today's review queue. The whole footer hides once that queue is empty. |

**Why #3 fails:** the original Alt+P plan limited the hint to review rows on purpose, and a test locks that in. A Ready task leaves the queue as soon as you keep it (Alt+F) or roll it (Alt+P), and `#hide` project lines never join it. Today the hint shows on 18 of your 21 real Ready tasks with a priority. Once you finish the morning review the queue is empty, so the footer is hidden and no task shows a hint for the rest of the day.

**Can we fix it?** Yes, with a small change in bob-ledger-tools only. bob-navigation-hotkeys can already preview any line.
- Show the hint when the cursor is on any open task with a priority, even if it isn't in the review queue. It takes the place of the `]s next` hint.
- When the queue is empty, show a footer with just the hint instead of hiding it.
- Tasks without a priority keep `]s next`, since Alt+P there always means P1.

**Should we?** I think yes. Alt+P writes without showing the card, and whether it rolls, steps down a priority (e.g. P2 → P3) or asks to cancel depends on the Schedule Log, which sits in a collapsed bullet you can't see. The footer is the only warning you get, and right now it's gone for most of the day. The cost is that the footer's documented rule ("hides when nothing is due") and its glossary entry would change.

Two edge cases in #1 don't affect Ready tasks, so I'd leave them:
- **Plain bullet:** Alt+P refuses on a bullet that isn't a task, while `1` writes P1.
- **Scheduled date already in P1's window:** this only happens on Blocked tasks. Alt+P always picks a new date; `1` can land on the same one.

One gap worth closing: the test checks Alt+P against the card's Ctrl+Enter, not against `1` itself, so a test pinning Alt+P to `1` would cover your actual contract.

I made no plugin changes. The existing Alt+P and footer test suites pass (55 tests). The report is committed to the research repo; I didn't file a task for the fix, since whether to do it is your call.
