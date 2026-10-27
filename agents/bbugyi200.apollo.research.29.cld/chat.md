# Chat History - ace-run (research.29.cld)

- **TIMESTAMP:** 2026-10-21 08:53:17 EDT
- **MODEL:** claude/opus
- **AGENT:** research.29.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261021_083251.md`

## Prompt

%id(cld, clan=research.29)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.29.cdx`, `research.29.grk`, `research.29.mus`, `research.29.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We recently added support for link relations, which are currently always directed. I
would like to start making any relation that does not have a description an undirected
relation instead.

- I was thinking we should just show `links` instead of `links to` and `links from` for
  these.
- Any relation with a description would then become a directed relation (update the
  glossary term and add new ones for "directed" and "undirected" relations).
- Linking another note to the current note (using the `~~` syntax, for example) then
  only makes sense if a relation description is provided (otherwise, it is the same as
  linking to a task directly using `~`, for example).
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

I'm reading the current relation contract (`docs/task-relations.md`, capture docs, and the Rust module) so I can design the undirected/directed split. Next I'll look at the code and the plugin repo.

I've mapped the plugin and Mac Capture relation code. Now I'm reading the vault conventions note and surveying real LINKS lines in the vault (read-only) to see how relations are actually used.

Still researching: I found the vault has just one relation (unlabelled), so the change has almost no migration cost. Now reading the capture relation writer and its terminal output.

I have enough evidence. Now I'll open the research sidecar repo properly and check the target directory for name collisions (filenames only).

Quick check of a possible Mac Capture side bug I noticed, then I'll write the report.

Writing the report now.

Report written. Registering it as a durable artifact.

I wrote the report to `sase/repos/research/202610/undirected_task_relations_design__cld.md` and registered it as `research:202610/undirected_task_relations_design__cld.md` (id `explicit:be894e4d95fcd026b6e58342`).

**Verdict: build it.** For an unlabelled relation, direction carries no meaning, yet you still have to choose it (`~` vs `~~`, `Links to…` vs `Linked from…`). The vault supports the rule:
- It holds only one relation, and it's unlabelled, so nothing needs migrating.
- Your hand-written idioms already split this way: plain "related to [[…]]" has no direction, and the 12 "Merged into [[…]]" lines always carry a phrase.
- Jira ("relates to") and Linear ("Related") make the plain relation two-way in the same way.

**Main critique:** only changing the display text isn't enough. Three current behaviours break the new meaning:
- Re-adding a target without a label strips its existing label (`src/native/task_relations/plan.rs:117`), so a casual `~T` erases meaning.
- The capture picker's "already linked" check only looks one way (`candidates.rs:1309`), so `~T` creates a duplicate reverse link.
- Nothing merges a pair that links both ways, so after the change a task would show the same partner twice.

**Adjustments I'm proposing (each flagged in the report):**
1. **Storage doesn't change.** Each relation is still written once on one task's `LINKS` line and mirrored on the other's generated `LINKED FROM` line, with the same raw line names. For a plain link, which task holds it becomes an internal detail.
2. **One relation per pair of tasks.**
   - A plain link to an already-related task changes nothing and never strips a label.
   - Adding a label upgrades a plain link, moving it to the labelled side if needed. The new entry is written before the old one is removed, so a failure leaves a duplicate rather than losing the relation.
   - Reconcile stops listing a pair twice and warns when hand edits create one.
3. **Direction moves from the row to the entry.** Both rows read `🪢 links`, with the second row drawn as a continuation of the first. Only labelled entries get a label and an arrow.
4. **One Task Card `Links…` row and one stage.** The label field gets a ⇄ swap and a live sentence that goes from `A ↔ B` to `A — label → B` as you type. `⇧L` becomes a shortcut into the reversed label mode.
5. **A bare `~~` counts as an incomplete draft and is refused on submit with an explanation**, rather than being silently rewritten to `~`. In Mac Capture, Return in the `~~` picker goes straight to the label card.
6. **Use "label", not "description".** "Description" already means a task's text in Bob. The report drafts the updated *Task Relation* entry, the new *Undirected Relation* (plain link) and *Directed Relation* (labelled relation) entries, and a decision record. I haven't written any of these into memory.
7. **JSON stays additive** (a new `directed` field, no new enum values). Refusing a bare `~~` is a CLI behaviour change, so its commit needs `!`.

**Rollout:** display copy first, then the bob-cli rules, then the unified Obsidian stage, then the Mac card.

**Possible bug found on the way (not checked by running it; I couldn't run the Mac app here):** Mac Capture's relation card appears to delete any draft text after the relation token when it inserts a label (`CapturePanelModel.swift:6691-6700`). Several Mac and plugin docs are also stale. Both are listed in the report; I didn't file task beads for them, to avoid duplicates across the swarm.

The research repo commit has been declared and the host will make it after this turn.

Sources:
- [Atlassian: Jira issue linking model](https://developer.atlassian.com/cloud/jira/platform/issue-linking-model/)
- [easeSolutions: Jira links for traceability](https://easesolutions.atlassian.net/wiki/spaces/R4JC/pages/3522330706)
- [Atlassian REST: issue link types](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-issue-link-types/)
- [Linear docs: Issue relations](https://linear.app/docs/issue-relations)
- [W3C OWL 2 Primer](https://www.w3.org/TR/owl2-primer/)
- [EmacsConf 2022: org-super-links](https://git.emacsconf.org/emacsconf-wiki/tree/2022/talks/orgsuperlinks.md)
- [Org-roam discourse: org-super-links](https://org-roam.discourse.group/t/org-super-links-with-org-roam/2016)
