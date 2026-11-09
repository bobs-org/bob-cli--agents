# Chat History - ace-run (research.3y.cld)

- **TIMESTAMP:** 2026-11-09 11:22:05 EST
- **MODEL:** claude/opus
- **AGENT:** research.3y.cld
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261109_110046.md`

## Prompt

%id(cld, clan=research.3y)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.3y.cdx`, `research.3y.grk`, `research.3y.mus`, `research.3y.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to display a little hint to the user in the bob-mac-capture app when they
type a character that they could have used a capture alias for.

- For example, if they press `@` to select an area/project note, we should show a hint
  teaching them about the `.` alias.
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

Reading the capture alias rules and decisions; next I'll look at how bob-cli and bob-mac-capture implement aliases today.

Mapping how the Mac app triggers bob's rewrite/completion calls; I'll delegate the large-codebase sweep and read the bob-side alias code myself.

Checking published research and other apps that teach shortcuts, so the hint design follows evidence.

The paper PDFs won't extract here, so I'll cite them cautiously. Next I'm checking bob's CLI conventions, then writing the report.

Prior alias research flagged discoverability as a gap, which supports this feature. Checking one last UI detail (the existing alias-opened picker subtitle), then writing.

Rendering the one diagram for the report (fixing a shell quoting issue), then writing the report.

Still tuning the diagram width; one more pass, then I'll write the report.

Research is done; writing the report now.

Report written and registered. Finishing the turn with the SASE final declaration.

The report is written and registered as an artifact under the label `research:202611/capture_alias_tips__cld.md`.

**Verdict: build it, but not as a lookup table from character to alias.** Each alias only works in certain spots, and your own example breaks for routes typed first: `.` stays literal at the start of an item (so `.bashrc` survives), so `@errands Buy milk` must never get a `.` hint. One wrong hint teaches a habit that later leaves stray `.`, `/` or `,` in captures.

**What I recommend:**
- **bob checks every hint before it shows.** It swaps the sigil you typed back to its alias key and runs the real alias rewrite on that draft. The hint shows only if the alias would have produced exactly the same draft and caret. This comes back as a new optional field, `alias_hint`, on `capture-rewrite --cursor`. A test ties every existing alias test case to its hint, so the two can't drift apart.
- **Trigger:** only a sigil typed with Shift (`@ ^ : + # ~ ! *`), since the point of every alias is to save a Shift. The app checks this on its own background call, which never delays the picker, the preview or Return. It stays out of the rewrite path, which has had several timing bugs recently.
- **Placement:** the hint sits in whatever the sigil opened: the route list, the picker footer, or the Close card caption. It appears when that opens or not at all, and goes away when it closes. No toasts and no status-line takeover.
- **Look:** one quiet line, `Next time  [.] → @  after a word`. It uses the panel's usual keycap style, tinted in the same color the editor gives that sigil. "Next time" makes clear it isn't a key to press now.
- **Frequency:** at most one hint per capture. Hints are frequent at first, space out if ignored, stop once you use an alias at least 75% of the time, and come back if you slip. There's a Settings switch (on by default) and a reset button.

**Changes to your requirements:**
- Hints only fire for a Shift-typed sigil that bob confirms, never for paste, picker inserts, Undo, or a sigil the alias itself produced.
- The `@` hint applies only after body text and a space, never to a leading route.
- Hint text says where the alias works, not what it's for. A lone `+` at the start of an item opens the parent-task picker but also starts `+2`, so "for a parent task" would mislead.
- I dropped hints for the `~~` flip and the `- ^^` move choice in v1. Teaching "`=` after `~`" invites a fast `==`, which types a literal `=`.
- I dropped a hint for the blank-draft `\` → `/` (Go To) alias, since neither key needs Shift.
- With an older bob, no hints show and there's no "update bob" message.

**Open questions for you:**
- For `#`, should the hint show only `/` or both `/` and `\`?
- Are the 75% "learned" bar and the spacing right? I picked them by judgment, with no data behind them.
- If most of your routes lead the item, the `@` hint will rarely fire because no alias exists there. Do you want that gap in the alias rules reopened?

I couldn't extract the text of the hotkey-learning paper PDFs on this host, so the report quotes only their abstract-level claims. The Superhuman help page refused automated fetches, so that example rests on search-result summaries.

The report is committed to the research repo as part of this turn.

Files are in `sase/repos/research/202611`:
- capture_alias_tips__cld.md
