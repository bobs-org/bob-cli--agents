# Chat History - ace-run (research.0z.grk)

- **TIMESTAMP:** 2026-10-12 07:01:48 EDT
- **MODEL:** grok/grok-4.6
- **AGENT:** research.0z.grk
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261012_064148.md`

## Prompt

%id(grk, clan=research.0z)
%m:grok/grok-4.6@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher grk in a 5-researcher swarm.
The other researchers, `research.0z.cdx`, `research.0z.cld`, `research.0z.mus`, `research.0z.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__mus.md` and `__gem.md`. Your report will end in `__grk.md`.

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
would like to add full support to prj tasks for task dep links.

- You can add a dependency to a prj task now (using the `<ctrl+shift+p>` keymap, for
  example), but the result is not intuitive (see the ~/bob/job_apply_to_databricks.md
  file, which should be auto-fixed by the `bob task reconcile` command after this
  change, for an example).
- When a prj task is given a dep link, it should be added as a `depends_on` frontmatter
  field on that project note, not in a "Depends On" sub-subullet. Make sure to update
  the `<cmd+ctrl+shift+n>` Obsidian keymap to support this change so project notes are
  converted from tasks correctly.
- Most importantly, any task that lives in a blocked project should also be blocked (in
  this case, because the project has an unmet dependency, but whenever a project is
  blocked this rule applies).
- We will need to make sure to update the `<ctrl+shift+p>` keymap so this occurs
  automatically when I add a dependency to a prj task using that keymap.
- Keep in mind that blocked tasks should not have corresponding task links, so those
  should be removed (along with the pomodoro section they live in if it becomes empty)
  if they exist.
- We should also update the `bob task reconcile` command to check for any tasks that
  should be blocked and/or have their corresponding task links removed.
- The "task dep links" glossary memory web term should be updated accordingly.

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
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

I'll research project-task dependency links independently: first the SASE memory, glossary, and skills, then the vault example and current code paths.

I'll load the glossary, decisions, and artifact rules next, then open the research sidecar and the relevant code.

The glossary lookup was ambiguous — I'll retry with exact strand names and pull the remaining decision and repo paths.

I'll inspect the vault example, existing research, and the current dep-link and project-task code next.

The Databricks project note is the bug: `^prj` has a Depends-On child while its Next tasks stay unblocked. I'll map how deps, blocked status, and project frontmatter work today.

I'll read the project and dependency docs, then inspect the plugin keymaps and how blocked tasks currently drop task links.

The `scheduled` frontmatter analog looks like the right model — I'll read that path, child-task inheritance, and the create-project keymap next.

The Sub-projects line already occupies the `^prj` first-child slot, which is why a Depends-On bullet there looks wrong. I'll confirm the convert-from-task path, defer-prune, and any existing project-level `depends_on`.

I have the design picture: one vault example, a Sub-projects collision, and a `scheduled` analog to follow. Next I’ll write the report and register it.

Artifact registration succeeded. I'll load the finalizer context and submit the declaration.

**Build it, with twelve adjustments.** A project-level dependency belongs in YAML next to `scheduled`, not as a Depends-On child of `^prj`. Ordinary tasks in that note should become `[?]` while the project cannot proceed, and those tasks should leave today's ledger.

The report is at `sase/repos/research/202610/prj_task_dep_links/prj_task_dep_links__grk.md`, registered as `research:202610/prj_task_dep_links/prj_task_dep_links__grk.md` (`file:explicit:0cbec591e7693b8e59a1db01`).

## Why this is a good idea

`job_apply_to_databricks.md` is a live failure of the ordinary-task dep-link contract on a lifecycle task:

- `^prj` is `[?]` on LinkedIn; the two CV tasks are still Next and still linked under today's JOB pomodoro.
- The Depends-On child occupies the same first-child slot `bob projects sync` uses for `🧩 **Sub-projects:**`.
- `^prj` is `#hide`, so `blocked.md` never shows the wait.

`scheduled` already works as a project YAML property that cascades Blocked and prunes Pomodoro links. `depends_on` should get that same status. Convert-from-task would currently turn a Depends-On child into a garbage `## Tasks` row.

Vault blast radius today: 86 project notes, **one** `^prj` Depends-On line, 40 ordinary-task dep lines in project notes that stay as they are.

## Adjustments worth making

The request as written would create three new bugs if implemented naively:

1. **Do not copy deps onto children** as lines or `[dependsOn::]` fields. R2 would adopt a Depends-On line onto every child. Derive `[?]` from **residence** only (the project note), not through `parent` ancestry.
2. **Stripping Task Links destroys Next** when the project unblocks. Today's recovery stores no previous-status. Accept that (children return to Ready; Bryan pulls). Making Blocked an overlay is a follow-up, not this change. Do not dump every resident task into the pomodoro on unblock (SL11 analog).
3. **`blocked.md` DEPENDENT queries only `is blocked`** (open `dependsOn` ids). Residence-blocked children with no inherited field would be `[?]` in the note and on the dash BLOCKED chip, and missing from that section. Align it with dash: `(is blocked) OR (status.name includes Blocked)`.

Other justified extras: YAML list of wikilinks (rename-safe, properties pane); derive hidden `[dependsOn::]` on `^prj` so Tasks still indexes the project row; new R-prj rules so that field does not grow a child line; chips on the `^prj` line so YAML is not invisible in Live Preview; a **new** decision record that specializes `task-deps-are-depends-on-links` for `^prj`; capture and Ctrl+Shift+M into a blocked project apply the same cascade.

The keymap in the request is `bob-navigation-hotkeys:create-project-note-from-task` (bound as Alt+Ctrl+Shift+N / docs `<ctrl+shift+option+n>`).

## Recommended mechanics

- Ordinary tasks: Depends-On line stays the source of truth.
- `^prj`: YAML `depends_on` is the source of truth; never a Depends-On child.
- Project-blocked means unmet YAML deps **or** a future `scheduled:` date.
- Ctrl+Shift+P `b` on `^prj` writes YAML, sets `[?]` on `^prj` and ordinary open residents, prunes live links, promotes the prerequisite.
- `bob task reconcile` does the same vault-wide (that is the Databricks auto-fix).
- Convert-from-task reads a source Depends-On child into YAML; convert-back synthesizes an ordinary Depends-On line on the restored task.

Full design, R-prj table, implementation order, and risks are in the report.
