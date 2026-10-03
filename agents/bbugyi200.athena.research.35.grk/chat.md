# Chat History - ace-run (research.35.grk)

- **TIMESTAMP:** 2026-10-01 11:31:40 EDT
- **MODEL:** grok/grok-4.6
- **AGENT:** research.35.grk
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261001_112023.md`

## Prompt

%id(grk, clan=research.35)
%m:grok/grok-4.6@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher grk in a 5-researcher swarm.
The other researchers, `research.35.cdx`, `research.35.cld`, `research.35.mus`, `research.35.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__mus.md` and `__gem.md`. Your report will end in `__grk.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

The point of the
new `[fresh::<date>]` properties that we've added to ready Obsidian tasks is to make it
clearer which of those tasks are really ready.

- A new task or a rotten task (let's start using the term "rotten" instead of "stale")
  should not be shown in the "READY tasks" section of the ~/bob/dash.md file.
- Instead, we should show new tasks either in a new "NEW tasks" section, which should be
  shown above the "WIP tasks" section and show rotten tasks in a new ~/bob/rotten.md
  file (that the ~/bob/dash.md file links to with a new "ROTTEN" badge).
- We may need to preprocess these rotten tasks somehow in order to make this work. My
  first thought was that we could use the `bob task-status-hooks` command to add a
  `#rotten` tag to rotten tasks, but you should think hard about the best way to
  implement this.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__grk` suffix, i.e. `<stem>__grk.md` (double underscore before the
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

I'll research the `[fresh::<date>]` / READY-vs-NEW-vs-ROTTEN design independently, starting with the relevant skills and the current Bob dash/task implementation.

I'll pull freshness docs, task-status-hooks, dash layout, and existing research filenames so the report can sit on the actual system.

The freshness contract is already detailed. Next I’ll inspect dash rendering, vault queries, and plugin surfaces so the recommendation matches how READY is actually built.

A `fresh_mark` plan already exists. I'll open the plugins and research repos, then inspect how dash READY queries and freshness currently interact.

The `#today` decision already rejected write-back tags. I’ll inspect the live dash queries and the ledger-tools `filter by function` path next.

The vault already has a `hide-rotten-tasks` Next item. I’ll pull the dash query source, freshness counts, and how Today is excluded from READY.

I have the architecture and live-vault evidence. Next I’ll write the independent report and register it as a durable snapshot.

The snapshot registered. I’ll get the finalizer context and commit the research repo.

**Split Ready at read time. Do not write a `#rotten` tag.**

READY should become the confirmed backlog. NEW belongs on `dash.md` below TODAY and above PENDING. Rotten (and resurfaced) belong in a query note `~/bob/rotten.md`, reached from a ROTTEN chip that replaces today’s REVIEW chip. `bob task-status-hooks` stays out of this.

The `#rotten` idea is the same design `today-is-read-from-the-ledger` already rejected: a 15-minute cache of a function of today, interval, schedule, and Today membership. It would lag at midnight, race Alt+F, and put a machine tag in the Tasks suffix next to user-owned `#hide`. The plugin already has `api.freshness.state` / `isDue`, and dash already filters TODAY that way.

The idea itself is good **now that `[fresh::]` exists**. The 2026-09-30 research kept READY whole and hung a REVIEW chip off it; that was the right launch. The payoff of the stamp is a READY list you can actually pull from. Bryan already filed that as `bob_gtd#^hide-rotten-tasks`. After today’s seed the queue is empty (199 fresh, 0 new, 0 stale), so this is layout, not a current backlog emergency.

Justified adjustments, called out in the report: read “WIP” as PENDING; send **resurfaced** to `rotten.md` with rotten; keep evaluator/JSON `stale` and use ROTTEN only on the board; exclude `isDue` from `readyBudget` so the chip matches the list; do not expand into Next/Pending or future-scheduled Blocked in this slice.

Report: `research:202610/ready_new_rotten_dash_surfacing__grk.md` (snapshot `file:explicit:5d74d2a9eab5588b4c63a520`).
