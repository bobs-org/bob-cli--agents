# Chat History - ace-run (research.35.cld)

- **TIMESTAMP:** 2026-10-01 11:34:17 EDT
- **MODEL:** claude/opus
- **AGENT:** research.35.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261001_112023.md`

## Prompt

%id(cld, clan=research.35)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.35.cdx`, `research.35.grk`, `research.35.mus`, `research.35.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

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

Reading the freshness spec and decision records done; now inspecting the live `dash.md`, the review note, and the hooks code.

Simulating how the freshly seeded pool will rot over the next two weeks to size the proposed sections.

Now reading the ledger-tools public `api.freshness` namespace and the READY badge model.

Reading the READY backlog contract in `docs/plan.md` and how the ledger-tools READY badge counts.

Research is done; writing the report now.

Registered. Now the final declaration.

I've written the report to `sase/repos/research/202610/rotten_new_ready_gating__cld.md` and registered it as `research:202610/rotten_new_ready_gating__cld.md`.

**Verdict: do it, but compute "new" and "rotten" when the dash is drawn. Don't store a `#rotten` tag, and don't add a preprocessing step to `bob task-status-hooks`.**

**Why not the tag:**
- **Nothing needs preprocessing.** `bob-ledger-tools` already has a function that tells a Tasks query whether a task is new, stale or fresh. It already refreshes open queries at midnight, and `~/bob/freshness.md` already uses it.
- **The project already rejected this exact pattern.** The `today-is-read-from-the-ledger` decision turned down a `#today` tag written by the hooks for churn, races and staleness. The freshness spec says the state is "computed at read time, never stored".
- **The tag would often be wrong.** The hooks run only on the MacBook, every 15 minutes, by cron. After an Alt+F a task would stay tagged, and so hidden from READY, until the Mac next runs. If the Mac is asleep while you work on apollo, that could be indefinitely.
- **Fixing that spreads the problem.** Every stamp would have to strip the tag, which means changing the stamp placement rules and their tests in both Rust and JS.

**Is it a good idea?** Yes, with one caveat. Each visible, non-Today Ready task lands in exactly one of NEW, READY or ROTTEN. So the dash sections still don't overlap, which was the only reason the earlier freshness research rejected dash sections. The cost is a new obligation: a task stays visible only if you re-confirm it each week. I simulated the live vault: the 199 seeded tasks rot at 15–48 a day starting tomorrow. With no reviews, READY is down to about 11 recurring tasks by 2026-10-08.

**Changes to your requirements (marked ADJ in the report):**
1. **"WIP" is now PENDING.** It was renamed on 2026-09-30, so NEW goes between TODAY and PENDING.
2. **Returning deferrals go in NEW, not ROTTEN.** These are tasks whose `scheduled` date has arrived. Putting them in rotten.md would take every P-level deferral off the dash and break `blocked.md`'s promise that they "land on the Dashboard tomorrow". Show them as a "↩ RETURNED" sub-group.
3. **Rename `freshness.md` to `rotten.md`** (keeping the old aliases), and replace the REVIEW chip with NEW and ROTTEN chips. Otherwise you'd have two review notes and three overlapping chips.
4. **Rename stale → rotten everywhere,** including the code, JSON output and config key, not just the labels. Freshness landed today, so it's cheap now. Do it after the freshness-mark epic `bob-cli-3a` lands, since that work is editing the same files.
5. **Use one new ledger-tools function, `api.freshness.bucket(task)`, for every view.** The READY chip, the daily READY badge and the READY section would all use it so their counts match. If the plugin isn't loaded, READY falls back to showing what it shows today.
6. **Make the ROTTEN chip escalate.** It turns red once any task has gone a full interval without review.
7. **Treat tasks whose blocking dependency just closed as RETURNED.** Otherwise they rot off the dash at the moment they become actionable. 14 open tasks currently have dependencies.

The report closes with the full recommended design and rollout order. It includes the proposed `dash.md` and `rotten.md` queries and a two-week trial with keep rules. It also covers the memory updates the implementation plan should include: the glossary entry and a new decision record. I didn't edit any memory.
