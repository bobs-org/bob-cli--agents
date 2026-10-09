# Chat History - ace-run (research.0q.gem)

- **TIMESTAMP:** 2026-10-09 11:04:56 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.0q.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261009_104545.md`

## Prompt

%id(gem, clan=research.0q)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.0q.cdx`, `research.0q.cld`, `research.0q.grk`, `research.0q.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

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
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
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

# Research Report & Architectural Evaluation: Re-Imagining Reference Task Tracking

**Report Location:** [`sase/repos/research/202610/ref_tasks_area_project_residence_reimagining__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/ref_tasks_area_project_residence_reimagining__gem.md)  
**Registered Artifact:** `research:202610/ref_tasks_area_project_residence_reimagining__gem.md` (`file:explicit:a72e1cb1a94b6602e0227c32`)

---

## 1. Executive Summary & Verdict

Your proposal to move reference tasks out of reference note bodies and into the `## Tasks` section of parent Area Notes or Project Notes is **architecturally sound, conceptually unifying, and strongly recommended**.

In Bob's GTD foundation, notes in `ref/` are **knowledge assets** (annotations, highlights, source links), while Area Notes (`dev.md`, `cash.md`) and Project Notes (`bob.md`) are **action centers**. Historically storing `- [ ] #task #ref ... ^ref` inside reference notes created an awkward split where tasks had to be tagged `#hide` and quarantined from standard task pickers, the `^` active task selector in `bob-mac-capture`, and the Pomodoro ledger.

However, to ensure this feature is **intuitive, reliable, and beautiful** without introducing daily friction or breaking invariants, we have analyzed the implementation across all four affected repositories (`bob-cli`, `bob-plugins`, `bob-mac-capture`, `sase`) and formulated **3 essential adjustments** to the requirements:

1. **Intelligent Non-Blocking Default Route on Intake:** Quick captures in `bob-mac-capture` and mobile captures via `bob gkeep pull` must **never hard-fail** or halt non-interactive pipelines if the user doesn't pick a parent. Instead, they should default to the active capture target / inbox area note (e.g., `mac_inbox.md`, `gkeep_inbox.md`), allowing frictionless triage via `Ctrl+Shift+M` later.
2. **Two-Pass Bounded Status Sync with `done/`:** Account for `collect_done` (`bob task archive`) by implementing a deterministic 2-pass lookup: check `<parent>.md` first; if not found, follow `<parent>.md`'s `done_tasks:` frontmatter pointer to `done/<parent>_done.md`.
3. **Harmonized CLI Option Design (`-p` vs `-P`):** In `bob ref create`, `-p` is currently `--published` (date) while `-P` is `--parent` (note). Under SASE `cli_rules.md`, public options must have unique short aliases. We reallocate `-p` and `-P` to `--parent`, moving `--published` to `-D|--published` (Date) or keeping it long-only.

---

## 2. Critique: Is This a Good Idea?

### Merits
- **Ontological Consistency:** Every `#task` in the vault will now live strictly in an Area Note or Project Note. No more exceptions for `ref/` files.
- **Unified GTD Lifecycle:** When you set a reference task to In Progress (`[/]`) or Next (`[*]`), it immediately appears in the `^` picker in `bob-mac-capture` and can be linked under today's open Pomodoro ledger.
- **Removes Quarantine Logic:** Eliminates ad-hoc exceptions in `capture_active_tasks.rs` and `freshness/scan.rs` that had to bypass `#hide` only for exact `^ref` strings.

### Pitfalls & Architectural Trade-offs
- **Cross-File State Split:** Reading state is no longer self-contained in `ref/<type>/<stem>.md`. If a task is moved with `Ctrl+Shift+M` or archived by `collect_done`, `bob ref` lookup must know how to follow the trail.
- **Capture Friction:** Forcing a prompt on every URL capture risks adding cognitive friction when quickly bookmarking articles. The default inbox fallback preserves zero-friction capture.

---

## 3. Core Design Specifications

### 3.1 Syntax and Unique Block IDs
Ref tasks in an Area/Project note under `## Tasks` take the format:
```markdown
- [ ] #task #ref [[ref/papers/attention|Attention Is All You Need]] ^ref-attention
```
- **Block ID Scheme:** `^ref-<slug>`, where `<slug>` is the sanitized stem/id (`[A-Za-z0-9-]`, capped at 48 chars). If a collision occurs within the same parent file, Bob suffixes `-2`, `-3`.
- **Obsidian Visual Styling:** Raw Markdown preserves `#ref`, but Obsidian renders a theme-native, small-caps Lucide book badge via a custom CSS snippet (`ref-task-badge.css`) matching your `task-statuses.css` design system:
  - Reading mode replaces literal `#ref` text with an inlined Lucide `book-open` SVG and `REF` small-caps pill.
  - Live Preview (CodeMirror 6) styles `.cm-hashtag-ref` with matching purple accent background and border.

### 3.2 Two-Pass Status Sync Protocol (Accounting for `done/`)
When `bob ref list`, `bob ref show`, or Highlights sync evaluates `ref/<type>/<stem>.md`:
1. Read `parent: "[[parent_note]]"` from frontmatter.
2. **Pass 1:** Scan `<parent_note>.md` for `^ref-<stem>` (or the wikilink `[[ref/.../stem]]`). If found, derive live status directly from the checkbox mark (`[ ]` -> ready, `[*]` -> next, `[/]` -> wip, `[x]` -> read, `[-]` -> abandoned).
3. **Pass 2:** If not found in `<parent_note>.md`, read `<parent_note>.md`'s frontmatter `done_tasks:` (e.g. `"[[done/<parent_note>_done]]"`). Scan `done/<parent_note>_done.md` for `^ref-<stem>`. If found, status is terminal (`read` or `abandoned`).
4. **Fallback:** If absent in both, fall back to the ref note's frontmatter `status` and emit an `orphan_ref_task` diagnostic.
5. **Bonus:** `collect_done`'s existing `link_repair.rs` already rewrites vault links from `<note>#^id` to `done/<note>_done#^id`, so any cross-links self-heal automatically on archive!

### 3.3 SASE File Hook & `project_name_aliases`
We inspected the `sase` codebase at `sase/file_hooks/runner.py`:
- **Current Behavior:** `runner.py` simply executes `f"{run['command']} {shlex.quote(str(run['abs_path']))}"`. While `run['project']` is already captured in the batch payload, it is never interpolated into the command string.
- **Proposed SASE Enhancement:** 
  1. Add `{project}` template interpolation in `runner.py`:
     ```python
     if "{project}" in raw_command:
         raw_command = raw_command.replace("{project}", shlex.quote(str(run.get("project") or "")))
     ```
  2. Export `SASE_PROJECT=run['project']` in the child process environment.
  3. Configure the `research-highlights` file hook as:
     `bob ref create --include-id -p {project}`.
- **`project_name_aliases` in Bob:**
  In `~/bob/bob.md`:
  ```yaml
  ---
  type: "[[project]]"
  project_name_aliases: ["bob-cli"]
  ---
  ```
  `bob ref create` resolves `-p bob-cli` by checking root files, exact project stems, and then `project_name_aliases`, mapping cleanly to `bob.md`.

### 3.4 Review Walk & Freshness Integration
- **Unifying with Standard Lanes:** Ref tasks in `dev.md` that are marked Next (`[*]`) or In Progress (`[/]`) will now walk in the standard `NEXT` and `PENDING` tiers during morning GTD review, subject to `next_interval` / `pending_interval`.
- **Retiring `Tier::References`:** Absorbs Ready (`[ ]`) ref tasks into the standard `NEW` and `ROTTEN` tiers. This eliminates the artificial segregation between "reading work" and "building work", ensuring your daily capacity limits accurately account for reading bets.

---

## 4. Migration Plan for Existing Open Notes

1. **Census:** There are currently **10 open reference notes** in the vault in `queued` or `started` states (all in `ref/ai/`).
2. **Parent Remapping:** Existing notes with legacy hubs (`agent_ref`, `claude_code_ref`, `ai_ref`, `obsidian_ref`) will be re-parented to canonical Area Notes (e.g. `dev.md`).
3. **Execution Tooling:** Implement `bob ref migrate-tasks --dry-run` to:
   - Extract the `- [ ] #task #ref ... ^ref` line from each open ref note.
   - Reformat it into `- [ ] #task #ref [[ref/...|Title]] ^ref-<slug>`.
   - Append it under `## Tasks` in the mapped Area Note.
   - Update `parent:` in the ref note frontmatter.
   - Remove the old task line from the ref note body.

---

## 5. Artifact & Finalizer Confirmation

- **Research Document:** Written to [`sase/repos/research/202610/ref_tasks_area_project_residence_reimagining__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/ref_tasks_area_project_residence_reimagining__gem.md).
- **Audit Registration:** Registered via `sase artifact create` with ref `file:explicit:a72e1cb1a94b6602e0227c32` (`var: artifacts[0]`).
- **Finalizer Declaration:** Submitted and accepted via `sase final submit` (`commit` requirement fulfilled).
