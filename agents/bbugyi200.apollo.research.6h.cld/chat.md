# Chat History - ace-run (research.6h.cld)

- **TIMESTAMP:** 2026-11-26 09:03:46 EST
- **MODEL:** claude/opus
- **AGENT:** research.6h.cld
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261126_084124.md`

## Prompt

%id(cld, clan=research.6h)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.6h.cdx`, `research.6h.grk`, `research.6h.mus`, `research.6h.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I just canceled the bob-cli-pl and bob-cli-q6 epic beads because I realized I'd made a
mistake that might cause some confusion and an inconsistent conceptual model for
property cards. Namely, the ~/bob/bank.md file should have never been an area note. It
should be a child of the ~/bob/cash.md file (as it is), but is only used for bank row
tracking purposes (it never contains tasks). I would like to complete the work for these
two epics, but only after the bank.md file is no longer an area note and any logic that
was added to support this strange state (which would produce two cards I think, right?:
one bank card and one area card) is removed.

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

Reading the two canceled epics' plans now; next I'll check which phases actually landed and trace the bank.md-as-area code in bob-cli and bob-plugins.

Both sweeps are back. Next I'll read the decisions roster and the related glossary terms, then spot-check the riskiest claims: the album parent rule, the type-name hazards, and vault usage.

Writing the report now.

Registration succeeded. Now finalizing the turn.

Turning bank.md from an area into a plain child of cash is a good idea, and doing that cleanup before finishing the two epics is the right order. My recommendation is below. I didn't change any code or vault notes; this was research only.

**Yes, you get two cards today.** Commit `06c87a06` stopped excluding bank.md from Area/Project cards. On plugin master and on the deployed bob-ledger-tools 1.166.4, the Area Card takes the title slot, foot and frontmatter on bank.md. The Bank card drops into the body with its foot hidden, and a new fragment, `249db-plugin-bank-area-arbitration.js`, decides between them. Separately, bob-cli treats bank.md as a "hybrid" (`contract/settings.rs:82`), so `+` shows AREA SETTINGS on bank.md whichever card mounts.

**Why it's a good idea:**
- The area type was deliberate: the original bank plan wanted bank.md to hold dispute tasks and be an `@bank` capture route. That never happened. Neither bank.md nor any `bank/` month note has ever held a `#task`, and nothing in the vault sets `[root:: bank]`.
- The two-card handling is what made the canceled acceptance runs fail (NO-GO): duplicate feet, a second pane losing the Area Card, and editor timeouts.
- The glossary entries for the Bank Card and Property Card already describe the single-card end state.

**The one real dependency is the subscriptions album.** Albums must have an area or project as parent. If bank.md stops being an area, `subscriptions.md` (parent `[[bank]]`) becomes invalid, and subscription matching turns off with only a warning from `bob bank check`. Everything else that changes is minor: bank leaves the `## Areas` lists in cash.md and area.md, `@bank` stops being a capture target, and bank month notes count under cash in Stats, which changes nothing since no time was ever logged there.

**Recommended approach:**
- **What bank.md becomes:** delete its `type` line and give it no new type. Bank code already finds it by path. A new `[[bank]]` type would make the plugins treat it as a record note, and that would refuse cash as its parent.
- **Subscriptions:** change its parent to `[[cash]]` in the same edit as bank.md, so the album is never invalid in between.
- **Remove the code that only exists for the two-card state:** the props hybrid in bob-cli, and the arbitration in the plugins. Make that a forward deletion rather than reverting the commits, because they're mixed with work worth keeping and with the generated bundle. The report lists every file and line.

**Changes to the requirements (marked [ADJUSTED] in the report):**
1. Accept losing `@bank`; money tasks go to `@cash`.
2. Re-parent subscriptions to cash.
3. Fix bob's starter text for a missing bank.md (`bank/output.rs:636`), which still prints `type: "[[area]]"` and would rebuild the problem.
4. Add a small `bob bank check` warning if bank.md is ever typed as an area again, and put bank.md back on the plugin's exclusion list.
5. Record this as a decisions entry, because an accepted plan and `docs/bank.md` both still say bank is a sub-area.

**Finish the epics re-scoped, not resumed.** Drop the plan to put the Area Card on bank.md, the whole bank/area arbitration sub-epic, and the "area strip" on the bank card. Keep the real-Obsidian acceptance tests, the retired-count cleanup, docs, and glossary work. The earlier glossary approvals have to be asked again with corrected wording, since the old wording put bank.md under its Area Card.

**Plan: one new epic in five phases:**
1. Vault edits.
2. Remove the hybrid from bob-cli (a breaking change, so the commit needs `!`).
3. Remove the arbitration from bob-plugins.
4. Real-Obsidian acceptance tests.
5. Polish, docs and memory.

The first three can run in parallel. I'd do the vault edit first: with the plugin and bob already installed, it immediately gives you one card on bank.md.

Two practical points:
- **Version skew:** plugins deploy at once but bob ships at most daily, so the plugin should stop showing settings for bank.md even when an older bob still sends them.
- **Existing failures:** four existing problems (a takeover self-test fixture, a stale docs inventory, a cursor fixture, and the bob-ledger-tools version drift on athena) need fixing before the acceptance phase can pass.

The report is registered as `research:202611/bank_hub_not_an_area__cld.md` (artifact `file:explicit:32fa5f97fe9eca37557c4d5e`), and the research repo commit is declared.
