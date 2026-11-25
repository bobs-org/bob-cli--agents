# Chat History - ace-run (research.6f.cld)

- **TIMESTAMP:** 2026-11-25 16:34:00 EST
- **MODEL:** claude/opus
- **AGENT:** research.6f.cld
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261125_161645.md`

## Prompt

%id(cld, clan=research.6f)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.6f.cdx`, `research.6f.grk`, `research.6f.mus`, `research.6f.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

When a task, say A, has a dependency on another task, say B, then A should not also have
a relationless link to the same task (in either direction). I would like to make this
invalid/confusing state impossible.

- When adding a relationless link to a task B, we should remove any existing dependency
  to task B from the current task. Similarly, when adding a dependency to a task B, we
  should remove any existing relationless link to task B from the current task.
- We should add the `<ctrl+b>` keymap to the link panel in Obsidian, which should be
  able to be used to mark the task as a dependency instead of linking to it. We should
  also be able to do the reverse (make a dependency a relationless link) from the
  dependency panel in Obsidian.
- Make sure it is clear when looking at the dependency/link panels in Obsidian if the
  task already has a relationless link/dependency, respectively.
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

Reading the bob-cli relation and dependency contracts now; next I'll look at the Obsidian link/dependency panels in bob-plugins.

Found the Obsidian nav plugin; reading its Depends-on and Links stage code (`300-dependency-stage.js`, `304/426/427` relation stage files) next.

Still mapping the Obsidian stages: the Links stage already has an info-only `⛓ prerequisite` badge; checking how rows, footer, and keys render in both stages.

Next: reading the governing decision records, then measuring how often the dep+link overlap actually occurs in the vault.

Measuring the vault next: a read-only scan of `~/bob` for tasks whose Depends-On and LINKS lines name the same task.

Found a real case: on 2026-11-17, a LINKS entry was added and then a dependency on the same pair 19 seconds later, in the reverse direction. Checking a couple more counts, then the Rust side.

I have the codebase picture. One quick prior-art check (how Linear/Jira model "related" vs "blocks" on the same pair), then I'll write the report.

I have what I need. Writing the report now.

Registered. Now finalizing the turn.

I've written the research report and registered it as an artifact. My view: it's a good idea, but the two rules as written would not have caught either real overlap in your vault, so I've adjusted them.

**What the vault shows.** I scanned `~/bob` read-only (274 dependencies, 321 links) and found only two tasks carrying both a dependency and a relationless link to the same task. In both, the prerequisite links to the task that waits on it. Your rules only act on the current task's own dependency, so neither case matches.
- **Case 1:** on 2026-11-17 a link was added, then 19 seconds later the same pair became a dependency: the linked task waits on the current one. That is the "I meant a dependency" fix Ctrl+B is for, but in the opposite direction from your Ctrl+B.
- **Case 2:** a research task that already blocked another task gained a relationless link to it when it was completed. If "adding a link removes the dependency" applied in both directions, that link would have deleted a dependency nobody meant to drop.

**Changes to your requirements:**
1. **Apply the rule to the pair, in both directions.** If either task depends on the other, neither should have a relationless link to the other.
2. **A dependency replaces a link, but not the other way round by default.** Adding a dependency always removes the relationless link, since that loses nothing. Turning a dependency into a link unblocks a task, so only the Obsidian panels do it, and they show the consequence ("Ready again") before you press ↵. Capture's `~`, hand edits and agents leave the dependency alone and say so. This matters because agents also use `bob capture`.
3. **Ctrl+B needs a twin for direction.** A relationless link doesn't say which task waits on which, and case 1 needed the reverse.
   - ⌃B: this task waits on it.
   - ⌃⇧B: it waits on this task.
   - ⌃L: turn it into a relationless link (the reverse you asked for in the dependency panel).

   These are the Task Card's `b` / `⇧B` / `l` keys with Ctrl, and they work the same in all four panels (Depends on, Blocks, Links, Linked from). On a dependency, ⌃⇧B also reverses its direction.
4. **Links with a label are left alone.** They carry meaning a dependency doesn't (`follow-up of`, `implemented by`), so they can sit beside a dependency.
5. **Completed-task archives aren't rewritten.** Bob never edits `done/` notes or the previous daily note, so case 2 stays as history.

**Making it clear in the panels:**
- Every row gets a badge for any existing tie: `⛓ prerequisite`, `🧱 dependent`, `🪢 linked`.
- A `⇄` mark appears wherever ↵ will convert instead of add.
- With an empty filter, a section lists the other kind ("TIED BY A DEPENDENCY" in Links, "PLAIN LINKS" in Depends on).
- The Depends on panel gets the consequence strip that Links and Blocks already have.
- Notices name what was replaced, for example `⛓ Now waits on "X" · replaced the 🪢 link · Blocked`.
- The Links panel's current tooltip, "linking stays inert", becomes false and needs to go.

**Recommended solution:** adopt the rule "a dependency absorbs a relationless link; only an explicit panel gesture turns it back." `bob task reconcile` removes leftover duplicates across the vault, reusing the either-direction check that already drops a 💬 mention when a dependency joins the pair. Two consequences:
- **Contract changes:** two documented rules need an explicit exception — that relations never change a task's status, and that reconcile never edits a LINKS line.
- **Write order:** a conversion within one task is one transaction (one Ctrl+Z). One that spans two tasks writes the dependency first and the link second, so a partial failure still ends in a valid state.

The report also covers the alternatives I rejected and a four-phase rollout (docs, Rust, Obsidian plugin, Mac app). The smallest useful version is the reconcile cleanup plus the three keys and badges.

Report: `sase/repos/research/202611/plain_links_and_dependencies__cld.md` (registered as `research:202611/plain_links_and_dependencies__cld.md`); the host commits it once this turn ends.
