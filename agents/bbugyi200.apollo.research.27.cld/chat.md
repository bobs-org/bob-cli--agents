# Chat History - ace-run (research.27.cld)

- **TIMESTAMP:** 2026-10-20 16:26:20 EDT
- **MODEL:** claude/opus
- **AGENT:** research.27.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261020_155257.md`

## Prompt

%id(cld, clan=research.27)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.27.cdx`, `research.27.grk`, `research.27.mus`, `research.27.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would love to be able to start showing likely related tasks in the bob-mac-capture
app's preview panel when the capture the user has input will result in one or more new
tasks being created.

- The main benefit of this feature would be that it gives the user a heads up about
  duplicate tasks and/or related tasks that they might want to link to in some way.
- The biggest concern here is performance. The bob-mac-capture app must remain blazing
  fast.
- A secondary concern would be how we fit all of this in the panel without making it too
  cramped or making the user need to scroll too often.
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

I'm surveying the Mac capture app and bob-cli capture code to see how previews and task pickers work today, then I'll design the feature.

I've confirmed the timings: parse 6 ms, dry-run 12 ms, the vault-wide `&` task catalog 360 ms. Next I'm checking what the existing task catalogs contain and which real duplicates exist in the vault.

I'm running a replay experiment on the real vault: lexical matching finds only about 20% of existing dependency prerequisites in the top 5. Next I'm checking how well it finds duplicates.

I've worked out a design direction. Next I'm reading the CLI rules memory before proposing a new bob command, and checking whether trigram matching earns its place.

I'm checking how other products handle "similar items while typing" (Stack Overflow, GitHub, Linear) to ground the UX choices, then I'll write the report.

I have the evidence I need. Before writing the report, I'm rendering a visual mockup of the proposed panel states.

The mockup is done. Now I'm writing the report into the research repo.

The report is written and registered. I'm submitting the final declaration now.

I'd build it, but as a "Similar tasks" heads-up rather than a "related tasks" panel. I replayed the vault's real history to test it: matching on wording catches duplicates well, but it rarely finds the tasks you'd actually link as prerequisites.

The report is `202610/capture_similar_tasks_preview__cld.md` in the research repo, with a rendered panel mockup beside it. It's registered as artifact `research:202610/capture_similar_tasks_preview__cld.md`.

**What the experiments showed** (run on apollo against the live vault; the Mac was offline, so there are no macOS timings):
- **Duplicates are common and easy to catch.** I re-ran all 1,490 tasks created between Jul 20 and Oct 20 against the vault as it was at each capture. At the recommended threshold, about 21% of captures would show a suggestion. About 88% of the ones I hand-labelled were useful.
- **Prerequisites can't be found from wording.** Across the vault's 95 real dependency links, the true prerequisite was in the top 5 only about 20% of the time. 65% of prerequisites simply live in the same note. So the feature shouldn't promise "related".
- **Bob's vocabulary is the key detail.** Code spans and keymaps like `<ctrl+shift+m>` caused the worst false matches. Keeping them as whole words improved ranking quality from 0.71 to 0.82–0.84 (AUC, 1.0 = perfect). Embeddings aren't justified for v1.
- **A list that updates on every keystroke flickers.** In a word-by-word typing simulation, 33–51% of captures briefly showed a wrong suggestion. Showing rows only after a pause and keeping them while you type cuts that to 14%.

**Speed: no extra `bob` call per keystroke.**
- Matching inside `bob` on each keystroke would take about 360 ms (one full vault walk per call).
- Instead, `bob` builds a small index of about 1,400 tasks: open tasks plus tasks closed in the last 30 days. A new command, `bob capture-related`, emits it.
- The app keeps the index in memory and refreshes it the way it already refreshes the idle agenda.
- The draft's search terms come from the `capture-parse` call the app already makes on every keystroke (about 6 ms).
- Ranking is a few microseconds of arithmetic in the app. `bob` still decides which tasks qualify, how words are split and weighted, and the match thresholds.

**Fitting it in the panel:**
- No match means no pixels, which is about 79% of captures.
- Otherwise a one-line-per-task band sits at the foot of the new task's preview card: at most 3 rows, or 1 per item in a bulk draft.
- Strong matches to open tasks get a "Likely duplicate" label, and the words that matched are bolded.

**Acting on a match:** ⌘1–⌘3 selects a row, then you press the capture symbol for what you want:
- `⌫` drops your item and keeps the existing task.
- `@` does the existing task now, linking it into today's Pomodoro.
- `!` marks the existing task done.
- `~` relates the two tasks.
- `&` makes the new task need the existing one; `*` makes the existing one wait on the new task.
- `/` opens the existing task in Obsidian.

Every action only edits the draft, so `bob`'s normal preview shows the result before anything is written. The one exception is giving a target task a block ID if it lacks one, which the pickers already do. Return is never blocked.

**Changes to your requirements I'm recommending (the report has the full table):**
- Call the rows "similar" rather than "related", with a separate duplicate label.
- Also search tasks closed in the last 30 days; about half of all matches were recently closed tasks.
- Show nothing below the threshold, and don't update rows mid-word.
- No new subprocess per keystroke, as a hard rule.
- Skip template drafts.
- Thresholds come from `bob`'s output, not app constants.
- Write a new decision record making clear that ranking in the app is allowed under the thin-client rule.
- Build an evaluation command and label a fresh set of matches before fixing thresholds. My precision numbers come from 80 pairs I labelled myself, and I tuned the tokenizer on those same pairs, so they're optimistic.

Five questions are listed at the end of the report for you to decide. The main ones are whether Return on a likely duplicate should default to "drop mine" or "do it now", and whether ⌘1–⌘9 conflicts with anything you use.

The research repo commit, which includes the mockup image, happens automatically after this turn.
