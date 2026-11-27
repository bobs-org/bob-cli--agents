# Chat History - ace-run (research.6p.cld)

- **TIMESTAMP:** 2026-11-27 13:56:57 EST
- **MODEL:** claude/opus
- **AGENT:** research.6p.cld
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261127_134153.md`

## Prompt

%id(cld, clan=research.6p)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.6p.cdx`, `research.6p.grk`, `research.6p.mus`, `research.6p.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add configurable task type expansion that is triggered when certain task
types are expanded (by selecting an entry offered by `#` completion in the capture
panel) at the start of the capture.

- `#fix`, `#build`, `#plan`, `#read`, and `#write` should all by configured (in my
  chezmoi repo) to auto-complete the corresponding word when expanded at the start of a
  capture.
- For example, after this change is implemented, when I type `#f` in an empty capture
  panel and then select the `#fix` task type, I would expect `#fix Fix ` to be expanded.
- The goal of this change is to reduce the amount of typing I need to do in some common
  cases when specifying task types in captures.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
First run `sase repo open research -r "Write this research report"` and use the path it prints as `<research checkout>`. Write this research to a new markdown file under `<research checkout>/202611/`.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__cld` suffix, i.e. `<stem>__cld.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path under the opened research checkout and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

Opened the research checkout and read the governing decisions; now digging into the task-type docs and the `#` completion code in bob-cli.

Reading bob-cli's `#` task-type completion code (candidate replacement + leading-space logic) to see where an expansion would slot in.

Opened the Mac Capture, plugins, and chezmoi repos; now checking how the Mac panel applies `#` completions and where the `types:` config lives.

Reading the Mac panel's task-type menu code to see how it applies the accepted row and handles Undo.

Confirmed the Mac applies Bob's `replacement`/`cursor_after` verbatim for `#` rows; now checking the Mac docs for the task-type menu's Tab/Return/Space semantics.

Probing the live `bob capture-complete` output for `#f` to ground the wire design.

Research is complete; checking the output filename is free before writing the report.

The report is written to `202611/capture_type_leads__cld.md` in the research repo and registered as `research:202611/capture_type_leads__cld.md`. The research repo commit is declared and lands after this turn.

**Verdict: build it, as a small "type lead".** After you accept a type from the `#` menu at the start of an empty new-task item, the Mac panel types the lead text (`#f` ⇥ → `#fix Fix ▌`). Bob decides when that happens and what the text is. You can see it before you capture, one key removes it, and `bob capture` never adds it at write time.

**How often your tasks already start with the verb.** I counted this read-only across the vault, using tasks with an explicit type field:

| Type | Tasks starting with the verb |
| --- | --- |
| FIX | 51% (94 of 184) |
| PLAN | 16% (3 of 19) |
| BUILD | 0 of 4 |

Across all 5,757 tasks, none starts with "Build", while "Add" starts 708. A correct lead saves about 5 keystrokes and a wrong one costs about 1, so a lead pays off if it's right more than roughly 1 time in 5. That only holds if removing it really is a single key.

**Changes to your request:**
1. **Where it applies:** the start of any empty new-task item, not just the first line of the capture. That includes later items in a multi-item draft and items that begin with a route (`@cash #f`). It never applies when retyping an existing task, to a marker at the end of the line, on `- #` bullets, or when text already follows.
2. **Which keys trigger it:** Tab, Return and click add the lead. ⌃↩ / ⌘↩ (accept and capture) don't, because otherwise `#f⌃↩` would quietly create a one-word "Fix" task. Typing `#fix` in full and then Space gives you just the type.
3. **Where the config lives:** a new `capture.type_leads` block, not `types:`. Any older bob drops your whole `types:` vocabulary if one value is a mapping like `FIX: {color: red, lead: Fix}`. Older bob ignores unknown `capture:` keys, so the chezmoi change can land first.
4. **The name:** "lead" rather than "expansion", because `%` already means "expands" in Bob's grammar.
5. **The values:** explicit strings rather than the type name in title case, so a type like MEET could later use "Meet with".
6. **BUILD (and PLAN):** keep them as you asked, but re-check after about two weeks, since your history predicts they'll be the misses.

**Design:**
- **Bob's side:** `bob capture-complete` adds an optional `lead` object to each `#` row. What gets inserted today for the type marker doesn't change.
- **Menu:** each row shows the lead dimmed after the type, e.g. `◆ FIX  Fix…`, so you see the result before you accept.
- **Insertion:** the lead goes in as its own undoable edit.
- **Removing it:** Backspace right after an untouched lead deletes the whole lead, the same way the panel already removes the auto-inserted `****` and `,<digit>` text. ⌘Z also removes just the lead.

**Alternatives I rejected:**
- Putting the lead into the existing completion text: it would ship without a Mac change, but you couldn't see it in the menu beforehand or undo it separately, and ⌃↩ would create junk tasks.
- Adding the verb when the task is written: you'd never see it before it lands.
- Guessing the type from a verb you typed: it goes against Bob's rule that a task's type field is only set by an explicit choice.
- Dim placeholder text that Tab accepts: it only wins if the lead is usually wrong.

**Rollout:** the chezmoi config block (safe to land first), then bob-cli (an additive feature on the daily release train), then the Mac app (gated on macOS CI). The report also proposes a decision record ("Type leads are editor text") and a "Type Lead" glossary term.

One thing to check first: the current Mac code may not let ⌘Z undo accepting a `#` row. That doesn't block this feature, but the lead itself must go in as its own undo step.
