# Chat History - ace-run (research.03.cld)

- **TIMESTAMP:** 2026-10-03 09:37:36 EDT
- **MODEL:** claude/opus
- **AGENT:** research.03.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261003_091907.md`

## Prompt

%id(cld, clan=research.03)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.03.cdx`, `research.03.grk`, `research.03.mus`, `research.03.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to start tracking every time an Obsidian task is explicitly refreshed (i.e.
its `fresh` property is updated by using the `<alt+f>` keymap) using a new
`refresh_count` property.

- This property should be rendered as an appropriate icon (like we do with `fresh`).
- The goal of this change is to enable some sort of (user approved--at the time of
  decay) auto-decay for tasks that continue to be manually refreshed, but I haven't got
  that part worked out yet. We already support auto-decay for repeat priority rolls but
  not for repeat rotten task refreshes. Think hard about the best way to do this.
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
(for example `research:202609/topic__a.md`), including any subdirectory the steps above
put it in. Do not derive the label from the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

I'm reading the freshness contract and searching for how priority-roll auto-decay works, which this design should mirror.

Opened the plugins repo; now locating the Alt+F stamping, freshness-mark renderer, and decay-ladder code.

Found the Alt+F handler (it applies to any open status, counted, and via Task Links). Next: the ledger-tools `stampLine` and freshness-mark renderer.

Plugin side is clear (Alt+F → `api.freshness.stampLine`, mark renderer in ledger-tools). Now checking the live vault's review load via the headless CLI, plus the Rust placement code.

Notable finding: 177 of 178 Ready tasks have no priority (implicit P0), so any decay design has to handle P0 as the main case. Checking the mark's CSS so the proposed icon fits.

Data gathered. Checking the vault git-sync cadence (relevant to whether lifetime refresh history can be derived offline instead of stored).

Report written. Checking a few line references and one unverified claim (capture previews) before registering it.

Now registering the report as a durable artifact.

Registered. Now the final declaration.

I've written the research report and registered it (`file:explicit:066f64ab7e8b10b1f924719f`, label `research:202610/refresh_count_keep_streak_decay__cld.md`). The report is at `sase/repos/research/202610/refresh_count_keep_streak_decay__cld.md`.

**Verdict: yes, build it.** Right now nothing stops a task that you keep confirming but never do. Repeated priority rolls decay, but Alt+F ("still right") has no consequence, so it's both the cheapest gesture and the only one with no memory. The live vault makes this worse than it sounds: 177 of the 178 open Ready tasks have no priority (implicit P0). So the existing priority-decay ladder reaches almost none of the Ready backlog.

**Requirement changes I'd make:**
1. **Count a streak, not a lifetime total.** Any real decision clears it. Alt+F is the only stamping gesture whose *only* effect is the stamp; every other one (priority, schedule, lane, move, depends-on, refresh interval, capture) is a decision. So if the existing stamp helpers (`stampLine` and the Rust `stamp_fresh`) clear the count, the reset works with no changes to other plugins or callers.
2. **Only count keeps the review walk asked for:** Alt+F on a due Ready task (ROTTEN or RETURNED), at most once a day. Off-cycle presses leave the count alone. First confirmations of NEW tasks, Next/Pending lane keeps and repeat presses don't count. Lanes stay out because the sticky-lanes decision rejects lane decay.
3. **Name it `[keeps:: N]` instead of `refresh_count`.** `[refresh:: 14]` already means the review interval, and "keep" is already the review word. This is a soft call; nothing else in the design depends on it.
4. **Show it inside the existing freshness mark rather than as a second icon.** Faint pips (`◔ 3d ••`, never green, so it doesn't read as a streak to protect). At the decision point the orange capsule swaps `⟳` for a 🍂 leaf.
5. **Decay is a choice you approve, using the existing priority ladder instead of a second one.** After 3 keeps (configurable), the next due Alt+F opens a small card instead of stamping:
   - **↵ Not now:** P0 tasks enter the ladder at P2 by default (the first level whose shortest deferral is longer than the 7-day review interval). Prioritized tasks take their normal roll/decay/cancel step.
   - **L — less often:** review interval goes to 14, 30 or 90 days.
   - **D — drop:** cancel, logged as `🍂 dropped after 3 keeps`.
   - **Alt+F again — keep anyway:** the count goes up and it asks again at the next review.
   - **Esc** writes nothing. Counted and Task Link batches skip tasks that need a decision.

**Timing and load:**
- **Trial is safe.** A decision needs 3 keeps a week apart, so the first card can't appear before about Oct 27, after the Oct 5–18 trial. Counting can ship now, and that is how the calibration data gets collected.
- **Expect a burst of decisions.** The cutover seed put every Ready task on the same 7-day cycle. If everything gets kept, about 24 decisions a day arrive for one week, roughly 4 weeks after counting starts. Each costs one key, and the P2 deferrals of 8–30 days spread the tasks back out.

The report also has the full gesture table, line placement, conformance vectors, CLI/JSON changes, rejected alternatives, and five open questions: name, limit, P0 entry level, a "Do today" row, and a new decision record.

One thing I didn't check: whether `bob capture` and Mac Capture previews hide inline fields like `keeps`. The report flags it to verify during implementation.
