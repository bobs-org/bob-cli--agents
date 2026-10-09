# Chat History - ace-run (research.0q.grk)

- **TIMESTAMP:** 2026-10-09 11:04:03 EDT
- **MODEL:** grok/grok-4.6
- **AGENT:** research.0q.grk
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261009_104545.md`

## Prompt

%id(grk, clan=research.0q)
%m:grok/grok-4.6@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher grk in a 5-researcher swarm.
The other researchers, `research.0q.cdx`, `research.0q.cld`, `research.0q.mus`, `research.0q.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__mus.md` and `__gem.md`. Your report will end in `__grk.md`.

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
would like to re-imagine the way that we track ref tasks.

- I have been treating ref tasks as normal Obsidian tasks in practice, but our
  implementation does not support this well or encourage it.
- Namely, the fact that we store ref tasks inside of ref notes is not intuitive or
  consistent with how we treat other tasks, which all live in either area notes or
  project notes.
- I would like to fix this by requiring that all future and currently open ref notes
  have a project note or area note listed as their parent.
- We should then be able to define the ref task for each ref associated with an
  area/project in the "Tasks" section of the corresponding note file like we do for all
  other Obsidian tasks.
- You should migrate any existing ref notes that are associated with open ref tasks to
  use this new policy and move their ref tasks to the appropriate area/project note
  file.
- This complicates syncing the ref note status with the ref task a bit since we need to
  account for the possibility that the ref task gets moved to a "done" note file in the
  ~/bob/done/ directory at some point.
- Also, I think there is a lot of logic that currently treats ref tasks as special /
  something to filter out. We don't show them when pressing `^` to show today's /
  pending / next tasks in the bob-mac-capture app, for example. Just about all (probably
  all, but think hard about this so we don't break any invariants that I currently rely
  on) of this logic should be removed so we start treating ref tasks like any other
  task.
- This change will also require that we start prompting the user for a project / area
  note file when capturing new ref URLs (via the bob-mac-capture app or the
  `bob gkeep pull` command, for example) so we know which project / area note file to
  use.
- This project / area name should then be passed to the `bob ref create` command's new,
  required `-p|--parent` option.
- I currently use a sase (a GitHub project in the sase-org organization) file hook that
  uses this `bob ref create` command. We will need to start passing in the project name
  (e.g. "sase", "bob-cli") to the `-p|--parent` option.
  - I'm not sure that sase injects the project name into this file hook command string
    right now, so you might need to add support for that.
  - Also note that it is not guaranteed that the project name that gets passed in will
    exactly match the project note's name. For example, the "bob-cli" project name
    should actually map to the ~/bob/bob.md file. To work around this, we should add
    support for a new `project_name_aliases` frontmatter field to project notes that
    allows them to specify alternative names that will be matched by the `bob` command
    when searching for a project by name. We should set this field to `["bob-cli"]` for
    the ~/bob/bob.md project note.
- We will need to start giving ref tasks a different block ID since `^ref` will no
  longer be guaranteed to be unique. In order to make ref tasks stand out a bit more, we
  should also start rendering an appropriate icon/symbol instead of `#ref` when these
  tasks are rendered in Obsidian.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

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

I'll start by reading the research, artifact, and glossary guidance, then map how ref tasks, parent notes, and capture currently work.

I'll load glossary and artifact memory, then open the research sidecar and start mapping how ref tasks actually work today.

Glossary selectors were ambiguous, so I’ll retry with aliases and open the research and linked repos in parallel.

Glossary confirms ref tasks are an explicit residence exception. Next I’ll open the linked repos and map the current ref-task implementation.

Repos are open. I’ll map `bob ref`, capture, hooks, and the places that still treat ref tasks as special.

`bob ref create` already has `-P|--parent`; `-p` is `--published`. I’ll read the parent, sync, and filter paths next.

The current `-P|--parent` is a PDF marker defaulting to `obsidian_ref`, not a GTD parent. I’ll inspect vault parents, sync, the file hook, and how `#hide` keeps ref tasks out of pickers.

The vault already has a `^better-refs` task, and most `parent` values are `*_ref` hubs rather than GTD notes. I’ll census open trackers, hub types, file-hook interpolation, and archive behavior next.

I have a clear design: keep hub `parent` as taxonomy, require the chain to reach an area or project, and put reading work in `## References`. Writing the report next.

I'll write the report from the vault census, CLI contracts, and the special-case map.

I'll verify the report is in place, then register it as a durable snapshot and submit the SASE finalizer.

The report is on disk. Next I’ll follow the artifact skill, read the artifacts memory, then register the snapshot.

I’ll record the skill uses, read artifacts memory through the audited path, and confirm the `sase artifact create` flags before registering.

Artifact registered. I’ll clean up my `/tmp` DQL scratch files, then gather the SASE finalizer context.

Open reading work belongs on a GTD home note. Do not implement the request as written.

The report is `research:202610/ref_task_gtd_residence/ref_task_gtd_residence__grk.md`. Snapshot: `file:explicit:dc5f55e3585344ee420a13be`.

**Verdict:** treat ref tasks as ordinary for action and special for hygiene. Four of the original requirements fight the vault and CLI:

1. Requiring frontmatter `parent` to be only an area/project flattens the `*_ref` hub graph (`obsidian_ref` has 297 children).
2. New `-p|--parent` collides with `-p|--published`. `-P|--parent` already exists.
3. Putting the row in `## Tasks` sends it through `bob task archive` into `done/` and counts it against the Ready cap of 5. Bryan’s own `^better-refs` task already says keep the row permanently on the project note.
4. Removing every `#ref` special-case would empty the REFERENCES walk and break Highlights sync, which still needs one machine-managed lifecycle row per PDF.

**Recommended shape**

- Keep authored `parent` as the hub or home, but require the parent *chain* to resolve to a typed area or project.
- Make existing `-P|--parent` required on `bob ref create`. Do not steal `-p`.
- Put the row in `## References` on the GTD home, not `## Tasks`.
- Identify with `#ref` plus unique `^ref-<id>`. Drop `#hide` so `^` can show Next/Pending reading work.
- Render a bookmark glyph instead of the `#ref` tag.
- Skip archive and the Ready cap for `#ref`.
- Persist parent on ref jobs; prompt in Mac Capture and `bob capture`; pass `--parent` as a batch flag on `bob gkeep pull` (no per-URL prompt).
- Interpolate `{project}` in SASE file-hook commands. Add `project_name_aliases: ["bob-cli"]` on `~/bob/bob.md` (do not reuse Obsidian `aliases`).
- Migrate only the 27 currently open reading notes (default `sase_ref` after confirmation). Leave ~900 closed/legacy notes in place.

That is the design that is intuitive (work lives with work), reliable (create cannot dump on `obsidian_ref`; sync has one identity), and beautiful (bookmark glyph, a References section, hubs still browse).
