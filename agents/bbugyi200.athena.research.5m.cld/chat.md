# Chat History - ace-run (research.5m.cld)

- **TIMESTAMP:** 2026-11-01 18:18:19 EST
- **MODEL:** claude/opus
- **AGENT:** research.5m.cld
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261101_180013.md`

## Prompt

%id(cld, clan=research.5m)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.5m.cdx`, `research.5m.grk`, `research.5m.mus`, `research.5m.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add support for a special new "starts after" relation label.

- This label should be rendered as "starts before" in the mirrored "linked from" bullet.
- The goal of this label is to allow me to trigger a successor prompt for certain tasks
  when another task is marked as wip/pending and moved out of the daily file (an
  operation that is unique to the `x*` capture syntax I believe). This will be useful
  since the tasks that I target with `x*` are often ones that correspond with work that
  I have assigned to an agent and I sometimes have another prompt that I want to think
  through and send out only after I have done the same for some other task (this is the
  one that I plan to target with the "starts after" relation).
- The successor prompt should also be triggered if the target task is closed (this is
  how normal successors work).
- Make sure it is very clear why this successor prompt is being triggered since we have
  various types of successors now.
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

Reading Bob's relation and successor docs and decision records to ground the design; next I'll trace the `x*` capture path and the successor-offer code.

Now tracing what `x*` "park" actually does to the task (status, links) and how close-time successor offers are computed.

Now checking how inverse labels render on LINKED FROM (stored vs display-only), since the "starts before" requirement hinges on it.

Mac uses the `link` symbol for relations. Last check: how the Obsidian successor picker handles an unknown group, then I'll write the report.

Enough evidence gathered. One last format check on how `x*` close output currently renders parked rows, so my mocks match real output.

Now I'll load the diagram conventions for the one flow figure I plan to include.

Drafting and rendering the one decision-flow figure ("when does a starts-after link offer its source?").

Figure renders cleanly (613×722 px, 100% fit). Now writing the report.

Fixing two small inaccuracies in the report: a stray mock line, and a hand-off "why" caption I presented as if it already exists.

Report written and registered as an artifact. Submitting the final declaration.

I've written the report. It's registered as `research:202611/starts_after_relation_successors__cld.md`, and the research repo commit is declared.

**My recommendation: build it.** A relation is the right tool here because it never blocks the later task (S). It just reminds you at the right moment. It also matches how Bob already defines a successor: a task that takes its predecessor's (T's) place when T leaves the plan. Handing T off to an agent is leaving the plan without finishing it. The rule of thumb I'd put first in the docs:

- **S needs T's result:** use a dependency (`&`). S stays Blocked until T is done.
- **S only needs T out of your hands:** use `starts after`. S is offered when T is handed off or done, and is never blocked.

**Requirement adjustments I'm proposing:**
1. **`x*` isn't the only hand-off.** Obsidian's Ctrl+Shift+Enter on an In Progress task does the same thing, and so does capture's `@route+id!`. So the trigger should be the event: T is now Pending and has no Task Link left in today's open Pomodoros. `x*` and `@route+id!` go in first; Ctrl+Shift+Enter is a small follow-up.
2. **"starts before" should be display-only, not stored text.** A LINKED FROM entry `[[S]] (label)` reads "S ‹label› this task". Storing `(starts before)` there would state the opposite order. Adding `starts after → starts before` to the existing inverse list makes the rendered line show "starts before" while the raw Markdown stays correct.
3. **bob should write each offer group's title and caption.** Bob Mac Capture already shows the existing keep-moving group by its raw internal name with a 🔓 "unblocked" icon. Any new group would be mislabeled the same way. Having bob send the copy fixes both.

The others:
- Cancelling T never offers S.
- If S starts after several tasks, all of them must be released first.
- Every hand-off re-checks, with nothing stored. Your ledger shows a task parked twice (a stash session, then the real send), so firing only on the first park would offer S too early.
- When S can't be offered, a muted row says why.
- Linking to a T that's already Pending gets a warning when you write the link.
- Typing "starts before" gets a hint to flip it.
- The labels live in a config list like cancel and complete labels, with chezmoi turning on `starts after`.

**How it would look:** a new picker group titled **Starts after "T"**, marked with 🪢 (Bob's existing relation glyph). Its caption reads "T went Pending · you set these to start after it" (or "is done"), tagged "your links · not dependents". Nothing is preselected or auto-linked, and a pick is written exactly like any other successor pick.

**Evidence from your vault:**
- `bulk-sub-bullet-capture` already has an unlabelled link to `task-bulk-actions`. It was sent at 13:00 after `task-bulk-actions` went out at 11:45, so it's a "starts after" edge waiting for a label.
- `successor-deps` and `off-tag` show the other case: they're Blocked on tasks you've sent, because they need those results.

**Two caveats:**
- **Coordinate with your Pending `next-task-in-prj-successors` task.** Its agent is working on project-successor prompts in the same close-time code, and that code currently has a rule that `x*` never offers anything.
- **Accept some `x*` slowdown.** Once the label is configured, an `x*` has to check the vault for "starts after" links pointing at T. I estimate 30–55 ms from the documented cost of a similar check; I didn't measure it. That would likely put `x*` previews over their current 40 ms target, so the report says to measure it and record the trade-off.

The report also includes a draft decision record, the JSON additions, 24 test cases, and a 7-phase rollout. Phases 1–6 cover the full request, including "also when closed" in Obsidian.
