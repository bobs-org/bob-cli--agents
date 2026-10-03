# Chat History - ace-run (research.v.grk)

- **TIMESTAMP:** 2026-09-30 18:26:21 EDT
- **MODEL:** grok/grok-4.6
- **AGENT:** research.v.grk
- **PROMPT:** `~/.sase/multi_prompts/202609/gh_bobs_org__bob_cli-multiprompt-260930_181054.md`

## Prompt

%id(grk, clan=research.v)
%m:grok/grok-4.6@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher grk in a 5-researcher swarm.
The other researchers, `research.v.cdx`, `research.v.cld`, `research.v.mus`, `research.v.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__mus.md` and `__gem.md`. Your report will end in `__grk.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I'm
currently re-designing my GTD process a bit (see the bob-cli-2y epic bead for context),
but there is still one major requirement that is unmet.

- Namely, it is important that I at least glance at every task that I captured the
  previous day in case something is in there that should really get addressed today. For
  example, what if my wife and I are speed walking and she asks me to pick up our
  daughter in the morning? I'll add it to my Google Keep and sync that with my Obsidian
  the next morning using the `bob gkeep pull` command, but if I don't glance at that
  task, it does me no good.
- This is why I used to review the Ready section in the ~/bob/dash.md file every
  morning. This habit, where I would review every task in that section and attempt to
  reduce the number of ready tasks for each project to <=5, forced me to glance at inbox
  items every morning.
- The problem with this approach was that I was reviewing some tasks way more often than
  necessary, which wasted time and introduced friction into the process.
- I think we can solve this by using a new concept named "task freshness" (aka
  "freshness"), which should be added to the glossary memory web.
- This new policy/process will require that every ready task have some new property, say
  `fresh`, that has a date as a value. That date is meant to indicate the last time a
  human being looked at that task and confirmed it still needs to be done and should
  still look the way it does (e.g. same priority, description, parent project, etc...).
- By default, we should use 7 days as our task refresh interval, but tasks should be
  able to override this with a dataview property. Also, we should be able to
  configure/override the refresh interval for every task in a project by adding an
  appropriate frontmatter property to that project note file.
- Making any changes (e.g. via Obsidian keymaps we support--we do not need to actually
  monitor for manual task changes) to a ready task (including making it ready--going
  from blocked to ready, for example) should result in the freshness date being updated
  for that task automatically.
- Any task that is past due for a refresh should show up in my new freshness review
  process, which you should help me flesh out.
  - I should be able to see how many of my tasks our out-of-date as well as how many
    tasks I have refreshed today at a glance somehow during this review process.
  - I should have keymaps that allow me to easily jump to the next/previous out-of-date
    task. I should also have a keymap that allows me to refresh the currently selected
    task without making any other changes to it.
- This solution addresses the problem of me needing to glance at inbox tasks every
  morning (these should be out-of-date by default since they have never been marked as
  fresh), but it also minimizes the amount of work that I need to do during any kind of
  weekly review (which is not something that I currently do).
- It's possible that even this becomes too much work every morning but, if that becomes
  a problem, I can always limit myself to reviewing N out-of-date tasks per day (and
  then introduce a weekly review where I refresh all out-of-date tasks).

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

I'll research the freshness-review design independently: first the SASE/research constraints and the bob-cli-2y epic, then the current GTD/inbox flow so the recommendation is grounded.

I'll record the research skills, then pull the epic, glossary, and current GTD/inbox machinery in parallel.

The research repo is linked under this workspace; I'll open it and pull the epic, glossary, and GTD sources next.

Glossary came back thin; I’ll pull the epic plan, GTD/task strands, and the research-repo layout next.

I’ll inspect dash/GTD chores, task properties, and the plugin keymap surface so the freshness design matches how the vault actually works.

Inbox tasks already sit as never-reviewed Ready items; next I’ll count the vault and inspect how properties and jump keymaps work today.

I have the vault numbers, the Tasks parser constraint, and the @FRESHNESS lineage. Next I’ll write the independent report and register it.

Build **task freshness**. Treat it as a review queue, not a new lane.

Yesterday’s Keep captures need a next-morning glance; rereading all of READY is the wrong tool. On 2026-09-30 the dash shows **186 Ready** tasks, **65 of them in `gkeep_inbox.md`**. A last-confirmed date plus an interval is the right primitive. Several of the original requirements should change.

**Recommended design**

- **Inbox is daily and path-based.** `gkeep_inbox.md` / `mac_inbox.md` stay in INBOX until the task leaves that note. A 7-day stamp must not hide pickup-daughter.
- **Filed Ready** gets a last-confirmed date and a 7-day default interval (project and task can override). Missing confirmation means stale.
- **Store it on a managed child** (`🌱 **FRESH** [on:: YYYY-MM-DD]`), not on the `#task` line. Obsidian Tasks peels unknown `[key::]` fields right-to-left and would stop parsing `created` / `scheduled` / `priority`.
- **Morning walk:** INBOX → PENDING → NEXT → STALE. READY stays the pull inventory.
- **Keymaps:** vault-wide next/prev stale (`Ctrl+Alt+J/K`) plus refresh-only (`Ctrl+Alt+R` and a `Ctrl+Shift+P` row). Human Ready-editing keymaps stamp; hooks, capture, and `bob gkeep pull` do not.
- **Cutover:** seed filed Ready (optionally stagger over 7 days); leave inbox unseeded.

The full analysis, glossary draft, dash/API sketch, and trial criteria are in:

`sase/repos/research/202609/gtd_ready_task_freshness/gtd_ready_task_freshness__grk.md`

Durable snapshot: `file:explicit:6f3d8a6f129a4101477d8506` (label `research:202609/gtd_ready_task_freshness/gtd_ready_task_freshness__grk.md`). The source file remains in the research repo.
