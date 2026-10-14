# Chat History - ace-run (research.4g.cld)

- **TIMESTAMP:** 2026-10-14 10:30:07 EDT
- **MODEL:** claude/opus
- **AGENT:** research.4g.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261014_100238.md`

## Prompt

%id(cld, clan=research.4g)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 4-researcher swarm.
The other researchers, `research.4g.cdx`, `research.4g.grk`, `research.4g.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I
would like to add support to the `bob capture` command and the corresponding
bob-mac-capture app for a new `*` syntax.

- This syntax should work a lot like the `&` syntax, which allows the user to specify
  that the new task should have a task dep link to a different task.
- This new syntax, however, should allow the user to specify that the new task blocks
  the specified task (i.e. specify a task dependency in the opposite direction).
- When we block a task that has a corresponding task link in today's daily file using
  this method, we should remove that task link (and the pomodoro iff that pomodoro
  section becomes empty after removing that task link).

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

I'm reading decision records and the capture/dependency docs to see how `&` works today before I write the `*` analysis.

I've confirmed that the `&` contract already removes a blocked dependent's live Task Links and any Pomodoro left empty. Next I'm mapping the Rust `&` implementation and the Mac app's handling of it.

Still researching: I'm checking whether reconcile already deletes every childless Pomodoro, which decides if "delete the Pomodoro iff it becomes empty" is new behavior or existing behavior.

Next I'm doing a read-only dry run of today's `&` against the real vault, to see how removing a link from the running Pomodoro shows up in the output.

I'm building a small throwaway vault to check whether a running Pomodoro's deletion appears in the capture preview.

I have what I need from the code and memory. One last check on how `capture-task-id` builds its `&` replacement, then I'll write the report.

I've confirmed the key behaviors by experiment. Writing the report now.

Report written and registered. I also found two pre-existing `&` bugs, which I'll file as task beads per project rules.

No in-progress epic is causally linked to either bug. I'll check the leading-run root cause so I can size the second bead accurately.

I filed both bugs as beads (bob-cli-7l, bob-cli-7m). Now I'm adding their IDs to the report and re-registering it; the same label replaces the earlier snapshot.

Now the final declaration.

I've written the report and registered it as a snapshot. My recommendation is to build `*` as `&` with the roles swapped, with a few adjustments I've marked clearly.

**Report:** `sase/repos/research/202610/capture_star_blocks_syntax__cld.md`, registered as `research:202610/capture_star_blocks_syntax__cld.md` (`file:explicit:42c32b47aa19f70256512305`). I added two bead IDs to it after the first registration, so I registered it again under the same label; that replaced the earlier snapshot.

**Is it a good idea?** Yes:
- **Right moment.** You usually notice a blocker while you're working on the blocked task, and `*` lets you record it right then.
- **No new data model.** The link still lives only on the blocked task's `⛓️ DEPENDS ON` line, and the `🧱 BLOCKS` line on the new task is still generated from it.
- **The return trip already works.** I closed the new task in a dry run and Bob offered the blocked task back as a hand-off.
- **Today's workaround is clumsy.** It takes a two-item draft with a block ID you make up, and it can't reach tasks in nested notes at all.

**What I found:**
- **Your third requirement already happens.** When `&` blocks a task, Bob removes its links from today's open Pomodoros and deletes any Pomodoro left with no child lines. `bob task reconcile` does the same within 15 minutes anyway. So `*` should reuse that code, not get its own rule.
- **That removal can delete the running Pomodoro without saying so.** I reproduced this in a throwaway vault, and a dry run on your real vault shows the same: blocking `do-cleanup-tasks` would delete today's running 10:10–10:35 JOB session. The only output is "removed 1 live Pomodoro link(s)", and the JSON lists no removed Pomodoro, so the Mac preview can't show it either. With `*` this will be the common case, so the reporting needs fixing first.
- **The Rust code is mostly reusable.** The `&` lexer already takes the sigil as a parameter, and the function that adds a dependency to an existing task handles everything once the roles are swapped. The Mac app routes on what `bob` sends rather than reading `&` itself.
- **`*` is a safe choice of character, with guards.** None of your 3,618 task lines has a word starting with `*`, and Obsidian note names can't contain it. But copying the `&` rules as-is would break `*urgent*`, `**bold**` and `* bullet`, so `*` needs Markdown guards that `&` never needed. `?` is my runner-up, since the blocked task ends up as `[?]`.

**Adjustments to your requirements (each is in the report's adjustments table):**
- **A1–A2:** Reuse the existing link removal, but report removed links and Pomodoros clearly, and say when a Pomodoro is the running one.
- **A3:** Write the new task's link before removing the blocked task's link. Then `New @inbox:id *T` puts the new task in T's place and the running session survives. No auto-linking by default.
- **A4:** The new task gets T's lane, capped at Next, so it's never created already `[/]`. Today `&` would make it `[/]` if T was `[/]`.
- **A5–A8:**
  - also allow `*` on an existing task (`@route+id`), and allow `&` and `*` on the same item;
  - allow targets in nested notes, but refuse closed, archived or previous-daily targets;
  - allow `^prj` targets, but show the whole blocked project in the preview;
  - always mint the new task's block ID.
- **Mac side:** use separate names for the new picker context and fields rather than adding a direction flag to the `&` ones. Otherwise an older app's add-ID flow would insert `&note:id` and silently reverse the dependency.

**Open questions for you:** the Next cap versus matching `&` exactly, whether to accept deleting the running Pomodoro for v1, `*` versus `?`, and keeping the inbox as the default route.

I also found two existing `&` bugs and filed them as ready beads:
- **bob-cli-7l:** removed links and deleted Pomodoros aren't reported.
- **bob-cli-7m:** `@cash &foo:bar Buy milk` silently saves `&foo:bar` as task text instead of adding the dependency.

The commits for the report and the two beads are declared; the host makes them after this turn ends.
