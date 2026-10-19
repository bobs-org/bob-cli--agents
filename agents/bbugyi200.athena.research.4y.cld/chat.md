# Chat History - ace-run (research.4y.cld)

- **TIMESTAMP:** 2026-10-19 08:28:12 EDT
- **MODEL:** claude/opus
- **AGENT:** research.4y.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261019_080823.md`

## Prompt

%id(cld, clan=research.4y)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.4y.cdx`, `research.4y.grk`, `research.4y.mus`, `research.4y.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to start rendering some kind of marker on tasks that are in today's daily
file when I view those tasks in Obsidian.

- We already do something similar to this for task links (to show which tasks are
  in-progress and which were unblocked today).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__cld` suffix, i.e. `<stem>__cld.md` (double underscore before the
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

I'm opening the bob-plugins repo to study how the existing task-link markers (in-progress/unblocked) are rendered.

Reading the existing unblocked-glyph and progress-mark sources in bob-ledger-tools.

Still gathering context — now reading the Today definition and the In Progress link-mark contract in `docs/plan.md`.

Surveying the freshness-mark display contract next, since it already shows "linked today" in tooltips.

Found a useful precedent: the Blocks-stage picker already shows a 🍅 badge for "linked under today's Pomodoro". Now checking how ledger-tools computes and refreshes the Today key set.

Checking the vault's CSS snippets for the existing status line tints and checkbox colors, so the new mark's color doesn't collide.

Now verifying the external precedents (Things 3's Today star in project lists, Microsoft To Do's "My Day" indicator).

Checking whether the Ctrl+Shift+Enter "is linked" rule matches the Today rule — a mismatch would make the mark lie about what the toggle does.

I have enough grounding. Collecting a few exact line references before writing the report.

Data check done: the vault has 5–15 Today links per day, spread over 3–8 notes, usually 1–3 per note. Now writing the report.

Writing the report file now.

Registration succeeded. Cleaning up the scratch script, then submitting the final declaration.

I wrote the report to `202610/today_task_marks__cld.md` in the research repo and registered it with `sase artifact create`, under the label `research:202610/today_task_marks__cld.md` (`file:explicit:57bc0fcd45c62125d12c6d55`). The research repo commit is declared and will land when this turn ends.

**Verdict: yes, build it.** It fills a real gap:
- **Next no longer means "today".** Since lanes became sticky, `[*]` means "committed", so a task's own line can't tell you whether it's on today's plan. In `bob.md` today, `^split-highlights` is linked in today's ledger, but two other Next/In Progress ref tasks that aren't linked look exactly the same.
- **Ctrl+Shift+Enter's state is invisible.** It toggles, so pressing it on a task that's already linked unlinks it, and nothing warns you first.

**Recommended design: a display-only "Today mark"** in bob-ledger-tools:
- **Glyph and placement:** a 🍅 right after the `#task` hash, before the title. Sibling lines then show the tomatoes in one clean column. I chose 🍅 because it already means "today's Pomodoros" on the ledger, the Mac menu bar and the Blocks-stage picker.
- **Running session:** tasks in the Pomodoro that's running now get a soft capsule in the line's own status color.
- **Hover and click:** hovering names the Pomodoro (e.g. `Today · BLOG · queued`). A plain click just places the cursor; Mod+click jumps to the link in today's note.
- **Data:** it reads from the Today cache the plugin already keeps, so no new definition or Rust change is needed. Nothing is written to tasks or the ledger.
- **Reliability:** it shows nothing until that cache is ready for today, and nothing when a task's identity is ambiguous. The invariant to test is: mark shown ⇔ the task is a row in dash's TODAY section.

**Requirement changes I made (each one is called out in §6 of the report):**
1. **"Today" means today's plan, not "anywhere in today's daily file".** Only links under today's open Pomodoros count, matching the dash and `bob plan`.
2. **No mark for history or loose mentions.** Links only under closed Pomodoros (🍅) get no mark, and neither do mentions in prose, nested bullets, or struck-through links.
3. **No marks inside daily notes,** since those notes are the ledger itself.
4. **Tasks query results are left out.** Their sections already split on Today, so a mark there would add nothing.
5. **The mark never uses the word "today".** `⧗ today` (scheduled) and `✓ today` (confirmed) already appear on task lines with different meanings.
6. **Pickers, the Task Card and Mac Capture come in a second phase.**

**Open risks:**
- **Ctrl+Shift+Enter disagrees on rare lines.** Its "is linked" check is broader than Today's: it also counts links in prose and in nested bullets. On those rare lines it will unlink even though no mark shows. I recommend documenting this rather than changing the toggle.
- **Link speed not yet confirmed.** I expect the mark to appear within a few hundred ms of a Ctrl+Shift+Enter link, but that needs checking when today's note is open in another pane. If it lags, the fix is an instant "expect this change" hint like the one the ◐ mark uses.
- **Things 3 analogy is from memory.** I used Things' Today star as a comparison but couldn't verify it on the web; Microsoft To Do's "My Day" behaviour is confirmed by Microsoft's docs.

The report also has a draft contract with 24 test vectors, an implementation sketch (about 700–1,000 lines of JS, CSS and tests across two fragments), a check-list to try in Obsidian, and five open questions for you: emoji or custom glyph, whether to keep the running-session capsule, what a plain click does, whether to narrow the Ctrl+Shift+Enter check, and whether to add a faint "worked earlier today" mark.
