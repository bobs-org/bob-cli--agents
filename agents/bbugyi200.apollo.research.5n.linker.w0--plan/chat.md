# Chat History - ace-run (research.5n.linker.w0--plan)

- **TIMESTAMP:** 2026-11-20 18:01:16 EST
- **MODEL:** claude/opus
- **AGENT:** research.5n.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/explicit_micro_tasks.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/explicit_micro_tasks.md`

> # Plan: Explicit micro tasks
> ## Context
> Bryan wants explicit micro tasks: steps under a task that must be done before the task
> is done, and that become real tasks when the task becomes a project. Today, project
> promotion (`buildProjectSeedFromChildBullets`, bob-plugins
> `plugins/bob-navigation-hotkeys/src/110-project-seed.js`) turns every non-drawer
> sub-bullet into a `#task` row. A vault scan found that at most about 21% of those
> bullets look like steps, so that implicit rule is wrong most of the time.
> The consolidated research report
> `research:202611/explicit_micro_tasks/explicit_micro_tasks.md` recommends a design.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to add much better (and explicit) support for "micro tasks". Can
you help me implement this?

- A "micro task" is a sub-bullet on an Obsidian task that would be converted to a task
  in the new project file if its parent task were converted to a project (e.g. via the
  `<ctrl+shift+alt+n>` keymap).
- We currently consider any sub-bullet that does not belong to a drawer to be a micro
  task (though we don't use this term yet).
  - We should instead start treating these bullets as if they were placed in a "NOTES"
    drawer and require that micro tasks be marked as such explicitly.
  - Any notes added to a task via captures (using the `@foo+bar` capture syntax, for
    example) should be added to the NOTES drawer by default unless another drawer is
    explicitly specified or a micro task marker is specified in the capture.
- I was thinking that we could either use a `TASK:` or `#task` prefix for these
  sub-bullets to mark them as micro tasks, but this is just my first thought. Think hard
  about the best way to mark these.
- We should support nested micro tasks (i.e. micro tasks with micro task parents).
- Regardless of how we decide to mark micro tasks, the mark should be rendered in a
  consistent and concise way. I was thinking we could render 2 or more `#` characters
  (depending on the micro task nesting level) for this micro task marker.
- It needs to be very easy to specify micro tasks in the capture panel. I was thinking
  that we could use `..` as a capture alias for the micro task marker (so `- ..` would
  be converted to `- #task `, for example) and add a new `<ctrl+g>t` keymap that toggles
  the micro task prefix for the current bullet.
- Top-level (i.e. `##`) micro tasks should show up as successors, which are closed by
  default, when their parent task is closed.
  - The user can decide to open these tasks using the `<ctrl+x>` keymap on the successor
    panel, in which case a new Obsidian task should be created for that micro task. The
    micro task bullet in the original task should be crossed out and an appropriate note
    should be placed next to it that links to the original parent task.
  - After opening a micro task successor, the user can also check it (e.g. using the
    `<space>` or `<tab>` keymaps), in which case the new task that is created should
    have a task link added to today's daily file (i.e. it should be pulled in).
  - The user can also canel a micro task successor using the `<ctrl+shift+x>` keymap, in
    which case the micro task sub-bullet should be striked out after closing the parent
    task (to indicate that it was not complete).
  - All non-top-level micro tasks (e.g. `###`, `####`, etc...) should still show up on
    the successor panel but should not be actionable since their status will be
    deteremined by whatever status we decide to give their parent micro task.
- When we merge a task into another task using one of the configured `merge_labels`, we
  should start creating a new micro task in the target task that represents the source
  task. I think this should just involve adding the microtask marker but there might be
  more work involved.
- As a part of this change, we should add an excellent new glossary term for "micro
  task".
- The Goals of this Change
  - Micro task successors will help me make sure that I've really completed all of the
    work that a task commits to before closing it.
  - I would like to soon make it possible to convert any project (regardless of how
    complex) into an equivalent task. This is out of scope for this research report but
    is a motivating factor, since this change will make it possible to convert
    sub-projects into equivalent micro tasks.
- Review the explicit_micro_tasks.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.5n.linker

## Response

Read the research report; now surveying bob-cli's code and memory to design the phases.

Opening the linked plugin and Mac repos so I can survey all three codebases in parallel.

Survey is back from all three repos. Now verifying a few load-bearing details myself (alias behavior, card contract, flag availability).

Checking plugin conventions and the existing Ctrl+] checkbox toggle in the cycler.

Design is converging. Before writing memory-related plan steps, loading the memory-write skill as required.

Design is settled. Writing a skeleton to get the epic schema from the validator.

I have what I need. Writing the epic plan now.

Validation passes. Tightening one ambiguous spot (the cycler call-site references) before revalidating and proposing.

The proposal is staged. Finishing the turn through `/sase_final`.

I've written the micro tasks plan as a 13-phase epic and submitted it for your review; nothing starts until you approve it. It follows the research report you agreed with, and I made the remaining design calls myself.

**The core design**
- **What a micro task is:** a plain checkbox bullet without `#task` (`- [ ] Write the parser`) whose parent is a task or another micro task. Its checkbox holds its state: `[ ]` open, `[x]` done, `[-]` not done, `[>]` carried (it became its own task). Nesting comes from indentation and is never stored.
- **The `##` look:** each micro task draws `⌗⌗` after its checkbox, and every nesting level adds one more `⌗`. The hashes use the owner task's colour. In the capture panel the `[ ]` is hidden and the hashes show in its place, so typing `- ..` reads `- ⌗⌗`.
- **Everything else is a note.** Unmarked sub-bullets act as an implicit NOTES drawer.
- **Typing them:** `..` at the start of a bullet becomes `[ ] `, and Ctrl+G T in the capture panel toggles the marker. In Obsidian, Ctrl+Enter ticks one off while you work, with no task fields, freshness stamps or successor offers.
- **When the parent closes:** each open top-level micro task is a row at the top of the existing successor card, Done by default.
  - Ctrl+X switches it between Done and Keep open. Keep open makes it a real task, and the old bullet becomes a struck-out `[>]` link to that task, which links back to the parent.
  - Ctrl+Shift+X marks it not done, with an optional reason.
  - Space or Tab keeps it open and adds it to today's Pomodoros in one keystroke, instead of the two-step "open, then check" you described.
  - Deeper micro tasks show under their parent but can't be selected.
- **Merging** a task into a task now writes the source as a micro task. **Promoting** a task to a project turns micro tasks into `## Tasks` rows and notes into a `## Notes` section.

**Calls I made beyond the research**
- **Esc in Obsidian writes nothing to the micro tasks.** The parent is already closed, so reopening it brings the open steps back unchanged. That is your "not done yet" escape. On the Mac, Esc still returns to the unwritten draft.
- **Every card key is undoable by pressing it again.** Space toggles "pull in" separately from the Done / Keep open / Not done choice, so pressing it twice restores whatever the row had before.
- **"Select all" never selects micro tasks,** whether it's Ctrl+A in Obsidian, ⌘A on the Mac, or `-p all` in the CLI.
- **Recurring tasks get no micro rows for now,** because resetting steps for each occurrence is follow-up work.

**A bug the survey found:** `bob projects sync` treats every checkbox in a project note as a task. Once micro tasks exist, it would add schedule dates to them and strip their `#hide`. The first phase fixes it.

**Phases.** Three bob-cli tracks run in parallel with Obsidian-plugin and Mac tracks. The micro-task row work on the close card is a large phase in each of the three places it appears (bob-cli, the Obsidian plugins and the Mac app), so each one plans before coding. One phase scans your vault for existing sub-bullets that look like steps and proposes converting them behind a gate; you approve each one individually. A final small phase writes the memory changes.

**Five decisions to answer when you approve:**
- **`captured_notes`** (default: loose bullets): your prompt asked for captured notes to go into a physical NOTES drawer, but the research recommended against that. I defaulted to the research's answer because you agreed with it; flip this if you want the physical drawer.
- **`obsidian_toggle`** (default: the existing Ctrl+]): Ctrl+] already adds or removes exactly the `[ ] ` marker in Obsidian. The alternative also adds a Ctrl+G T shortcut there to match the capture panel.
- **Memory changes** (all default yes, because each is either requested or corrects a claim this work makes false):
  - add the Micro Task glossary term you asked for;
  - fix the Capture Alias glossary definition so it covers `..`;
  - add a "Micro Tasks Are Checkbox Bullets" decision record and mark "Capture Bullets Mirror The Task Block" as partly superseded, since a first-level `- [ ]` bullet is no longer a note.

Deferred and listed as follow-ups: a "not done yet" abort in Obsidian, a `⌗⌗ 2/4` progress chip, offering to keep micro tasks open when the parent is cancelled, step resets for recurring tasks, and the project-to-task conversion itself.
