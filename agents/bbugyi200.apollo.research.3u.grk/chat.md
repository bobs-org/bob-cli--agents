# Chat History - ace-run (research.3u.grk)

- **TIMESTAMP:** 2026-11-09 07:21:59 EST
- **MODEL:** grok/grok-4.6
- **AGENT:** research.3u.grk
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261109_070553.md`

## Prompt

%id(grk, clan=research.3u)
%m:grok/grok-4.6@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher grk in a 5-researcher swarm.
The other researchers, `research.3u.cdx`, `research.3u.cld`, `research.3u.mus`, `research.3u.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__mus.md` and `__gem.md`. Your report will end in `__grk.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I like the set up we have now where I ask agents to add useful context to period note
files at the end of that period (an agent just updated the ~/bob/2026/2026-W45.md file
today, for example). I want to improve the agent instructions contained in these files
to try to make the summaries/context produced by agents even more useful, but I'm not
sure what changes to make.

Can you do some research with the goal of helping me decide if this is a good iea and
(if so) what changes to these period note agent instructions would be most useful? 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__grk` suffix, i.e. `<stem>__grk.md` (double underscore before the
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

I'll research the period-note agent instructions independently: first the research and memory skills, then the current notes and how those instructions are used.

I'll record skill use, load period-note memory, and inspect how those agent instructions currently live in the vault and repo.

Period notes already have a folded `[!agent]` callout and `bob periods draft`. Next I’ll open the research sidecar and inspect those instructions plus how they are generated.

The instruction source is `instructions.rs`. I'll read that, the live W45 note, and how review agents actually get launched.

The reviews are formulaic; W44’s edited headline is the useful exception. Next I’ll compare Bryan’s edits, the original callout design, and how these agents actually run.

The W45 agent treated the brief’s ranked list as sacred and packed the word cap. I’ll confirm that in the brief code, then pull literature and Bryan’s library.

I have the evidence I need. Next I’ll draw the two figures, then write the report and register it.

The figures are a little too wide for the PDF box. I’ll tighten spacing and shorten labels, then re-render.

Figures read cleanly. I’ll write the full report next.

**Yes: keep the setup, rewrite the in-file callouts to v2.** The ownership split, `bob periods brief`, `bob periods draft`, the word caps, and the anti-slop rules are already the right machine. The summaries are less useful than they could be because v1’s composition rules reward a stats recitation.

Full report: `research:202611/period_note_review_instructions/period_note_review_instructions__grk.md`  
Registered snapshot: `file:explicit:f70488afb655b33b191eba5a` (source left in place).

### What 19 live drafts show

- **18 of 19 week Headlines** start `A {duration} week, {delta} typical…`. Parent notes display that line, so it becomes the quarter’s memory of the week.
- **The one work-first Headline is W44:** “Shipped command-mode improvements and finished Stripe prep in a 30h 45m week, 55m under typical.” It is also the shortest Review (143 words). W45 packed 239 of 250.
- **Finished copies the brief’s minute-ranked list.** Daily `gtd` rows win on minutes. The W45 agent knew this was ugly and still copied five daily-review rows plus `+240 more`, because swapping tasks would change `+N` and v1 forbids inventing numbers.
- **Questions restate the strip.** A Created/Done/Worked typical-delta is question 1 on most weeks.
- **Every Intentions, Outcomes, Theme, and Reflection is still empty**, including W46 after today’s completed Weekly review POST. v1 says “leave out empty parts,” so the missing bet is invisible. The draft is currently the only narrative of the week.
- W41 and W44 are marked `edited` only because `bob task archive` rewrote links and broke `review_digest`. Bryan did not touch the prose.

### What to change (callout v2)

Replace weak rules; do not add sections or raise caps. Bump `INSTRUCTIONS_VERSION` to 2 and run `bob periods ensure -R`.

1. **Headline names the work.** Hours and shares belong in Where the time went. Show W44 as good and W45 as bad (Anthropic: examples steer better than constraints).
2. **Empty Intentions stay visible:** `_No intentions were set._`
3. **Finished is a curation.** Skip daily `gtd` rows. `+N more` is optional, not a reason to copy the brief’s top 7.
4. **Two questions that are bets** for next week’s Intentions or a keep/drop. A typical-delta already on the strip is not a question.
5. **The cap is a ceiling.** 120–180 words is enough when Intentions were empty.

Leave brief/draft/caps/anti-slop/third-person/all-time-mute alone. Keep automation off until four live Mondays after v2.

### Parallel bob-cli fixes (not callout text)

Stop ranking daily `gtd` rows into Finished, and stop letting archive flip `drafted` to `edited`. Those bugs are why v1 agents feel forbidden to curate.

The report includes a proposed weekly v2 callout body ready to drop into `src/native/periods/instructions.rs`.
