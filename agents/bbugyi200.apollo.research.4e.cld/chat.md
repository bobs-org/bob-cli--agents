# Chat History - ace-run (research.4e.cld)

- **TIMESTAMP:** 2026-11-12 11:21:41 EST
- **MODEL:** claude/opus
- **AGENT:** research.4e.cld
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261112_110045.md`

## Prompt

%id(cld, clan=research.4e)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.4e.cdx`, `research.4e.grk`, `research.4e.mus`, `research.4e.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We currently always show the GTD review footer. I would like to start making this footer
only show when the GTD review walk is active (i.e. the `s` key is active and will be
triggered by the `[[` and `]]` keymaps).

- As a part of this change, we should add two appropriate new footers that are active
  only when the `w` walk or `n` walk is active.
- The `w` walk should have indicators that show how many pending/next/ready tasks are in
  that walk, for example.
- We should add an excellent new "walker footer" glossary term to describe these footers
  (note that a "review footer" should be considered a type of "walker footer").
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

I'm reading the bob-plugins code to see how the `s`, `w`, and `n` walks and the current review footer work.

I'm still reading code: next up are the bracket-mode indicator and the review footer's model and paint.

I'm now reading the lane-walk model and toast code so the `w` footer can reuse the walk's own data.

I'm reading the footer CSS next to see which colors, tier hues, and motion patterns already exist.

Still researching. I'm checking how the lane-walk data is cached and refreshed so the `w` footer can update live without extra cost.

I'm checking two earlier research reports on status-bar footers so this design stays consistent with decisions already made.

Now checking the ledger-tools docs and decision records that govern the review footer, so I know which existing rules this change touches.

I've finished reading the code. Next I'll pull today's real counts from the vault (read-only) so the mockups use realistic numbers.

I'm building a rendered mockup of the three proposed footers using the production CSS, so the report can show the design rather than only describe it.

The mockup rendered; I'm checking it visually now.

The mockup reads well. I'll fix two rendering glitches: emoji boxes in the stand-in status items, and the sheet width. Then I'll re-render.

The re-render is clean. Next I'll copy it into the research directory and check the test files an implementation would touch.

Bryan's vault uses the default theme, so the right-anchored layout assumption holds. Updating one mockup label to match the recommended lane detail, then saving the image.

The mockup is saved. Now I'll draw the cross-plugin data flow as a Mermaid figure, using the repo's diagram conventions.

The figure renders at 84% fit and reads clearly. I have everything I need, so I'm writing the report now.

Fixing the figure numbering: the mockup appears first in the report, so it should be Figure 1.

The report is written. Registering it as a durable artifact now.

Registered. Now finishing the turn with the SASE final declaration.

I wrote the research report, rendered a mockup of the design, and registered the report as an artifact. My recommendation: build it, but as one "walker footer" that swaps its contents with the active walk, not three separate footers.

- **Report:** `sase/repos/research/202611/walker_footers__cld.md`
- **Mockup:** `walker_footers_mockup__cld.png` in the same folder. It shows the proposed footers in light and dark themes, built from the real footer CSS.
- **Artifact:** registered as `research:202611/walker_footers__cld.md` (`explicit:451741036ece6051eb532253`).
- **Commit:** declared for the research repo; the host commits both files after this turn.

**Is it a good idea?** Yes. The `[[ s w n ]]` indicator already decides what `]]` and `[[` do. Today the review footer ignores it: with `w` lit, the review footer still shows, and the two sit apart in the status bar. A footer that only shows when it's the active walk is also more likely to get noticed than one that's always on.

**Requirement changes I'm recommending:**
- **One footer, three versions.** A single status-bar item in bob-ledger-tools shows the `s` (review), `w` (lane), or `n` (link) version. All three share the review footer's layout, colours and narrowing rules, so switching walks doesn't make the bar jump around.
- **Placed directly left of `[[ s w n ]]`.** Obsidian's status bar grows leftward from the right edge, so the letters never move under your mouse when the footer changes width. I couldn't run Obsidian on apollo, so this needs checking on the Mac.
- **A dot on `s` when the review is hidden but due.** The walk choice persists across days, so if you finished yesterday on `]n`, this morning's review would otherwise vanish. The dot appears only when the parts of the review you're meant to finish (PRE through TICKLER) are due. It's tinted with the first due tier's colour and has no number or animation.
- **The active walk always shows something.** With `s` active and nothing due, it reads `⟳ Review clear · ✓ 29 today` instead of disappearing.
- **Hints say `]] next`.** That's true for every version, since the footer only shows when `]]` repeats it.
- **The `w` counts** are exactly the walk's tasks off today's plan, from the same data as the dash chips. Off a lane row it reads `WIP 10/8 · NEXT 7 · READY 3 · TODAY 12` (rough numbers from today's `bob plan`). A lane shows `/cap` in red only when it's over its cap, which WIP is today.
- **The `n` footer previews where `]]` and `[[` go**, e.g. `‹ Wed Nov 11 · Fri Nov 13 ›`. It uses the same parser as `]n`, so it can't disagree with the keys, and a dashed `+` marks a period note that bob would create.
- **Never switch walks automatically**, and if bob-navigation-hotkeys is missing or older, fall back to exactly today's behaviour.
- **One "Walker Footer" glossary term** (aliases: walk, lane and link footer), with an edit to the review footer term. I drafted both in the report but didn't change any memory files; an optional decision record is drafted too.

**How it fits together:** bob-navigation-hotkeys would expose a small new `api.walkMode` (current walk, select, link preview, set the dot) plus an event when the walk changes. bob-ledger-tools builds only the active footer and redraws immediately when you switch. The report includes a six-phase build plan with tests, a table of failure modes, and the alternatives I rejected and why.

Questions for you:
- Should the dot use the due tier's colour or one neutral colour? I'd use the tier colour, because it tells you which part of the review is waiting.
- Should lanes show `/cap` only when over, or always like the dash chips? I'd show it only when over, to keep the bar quiet until it matters.
- On a device that has never picked a walk, should it show nothing or default to the review footer? I'd show nothing.
- Is "Review clear" the right wording, or would you rather keep "Nothing due"? I picked "Review clear" to match the lane walk's existing "Lanes clear".
- Do you want the decision record?
