# Chat History - ace-run (1hr--plan)

- **TIMESTAMP:** 2026-11-28 08:32:08 EST
- **MODEL:** claude/opus
- **AGENT:** 1hr--plan

**Plan:** /home/bryan/.sase/plans/202611/task_headline_keys.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/task_headline_keys.md`

> # Plan: Ctrl+Shift+O files task notes at the note home; `o` on a headline opens a req
> ## Goal
> Bryan's three asks:
> - **Ctrl+Shift+O on a task headline.** It always opens a note bullet _in that task_. The
>   note lands below every Depends-On, BLOCKS, LINKS, and LINKED FROM line, and inside the
>   task's `Notes` drawer whenever one exists.
> - **`o` on a task headline.** It opens a new requirement (req) for that task instead of
>   a new task. Bryan creates tasks through the capture panel, so the old `o` behavior
>   sees little use.
> - **`O`.** It opens a new req only when the cursor is on a req (directly above it). On a

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli The `<ctrl+shift+o>` keymap in Obsidian should always insert a note bullet into
a task when a task's headline (i.e. first line) is selected, which should always be
below any links/deps and should always be inside the "Notes" drawer if one currently
exists for the selected task. See the ~/tmp/screencasts/20261128_073223.mp4 screencast
for context. Can you help me fix this?

- As a part of this change, let's also change the `o` keymap so it creates a new task
  req for the current task, assuming that task's headline is selected.
- I rarely create tasks by hand in Obsidian (I use the capture panel), so the current
  functionality of the `o` keymap doesn't get much use.
- The `O` keymap should support this functionality only when a task req is currently
  selected.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I've pulled the keystrokes from the screencast (⌃⇧O, ⌃[, k, j, dd). Next I'll look at the frames, then find the keymap code in bob-plugins.

The keymaps live in bob-plugins' `task-status-cycler`. I'm reading its Ctrl+Shift+O and `o`/`O` code paths and their docs now.

Still checking the screencast. A cropped strip of the middle frames should show what Ctrl+Shift+O left behind before `dd`.

The planner code says this task's note should land before WORK LOG, not under the headline. I'm going to run it against the real `bob.md` block to find out why the screencast shows otherwise.

Next I'm checking how reqs are typed today, especially the "first req moves loose notes into Notes" step. A new `o`-on-headline req has to follow the same rule.

The epic that added the note command (`bob-cli-q4`) says Ctrl+Shift+O was meant to open at the task's note home. I'm reading its plan for the intended contract.

I'm reading the note-home contract in `docs/task-requirements.md` to decide whether the "use an existing Notes drawer" rule belongs in the keymap only or in shared bob-cli logic.

I have the full picture. Now I'm checking the test and e2e harness conventions in bob-plugins so the plan's verification steps are concrete.

The plan is mostly settled. One last check: where a new req would land on a `^prj` project line, since that case is a reviewer decision.

I have what I need. Writing the plan now: Ctrl+Shift+O root cause and fix, `o` on a headline creating a req, `O` unchanged, plus tests, docs, and deploy.

Validation passed. Submitting the plan.

I found why Ctrl+Shift+O misbehaves and submitted a fix plan for your approval. Nothing is changed yet.

**Why it happens.** Vim swallows Ctrl+Shift+O in normal mode before Obsidian's "Open note in task" hotkey can run. An older keydown listener in `task-status-cycler` catches the key instead. That listener just adds a child bullet on the line below the cursor, which put the bullet above the BLOCKS and LINKED FROM lines in your screencast. It also never removes an empty bullet, which is why you needed `dd`. The intended note logic only ran in insert mode. Its tests called that logic directly and never pressed the real key.

There is a second problem. For a task with no reqs, the note logic ignores an existing `Notes` drawer. Run on your `^snoozed-tasks` block, it puts the note after `**The Goal**`, not inside `**Notes**`.

**What the plan does** (all changes in bob-plugins, plus one bob-cli doc edit):
- **Ctrl+Shift+O on a task headline:**
  - One note planner serves normal mode and insert mode alike.
  - The note goes inside the task's `Notes` drawer whenever one exists, even with no reqs.
  - Otherwise it uses today's placement, which is always below the Depends-On, BLOCKS, LINKS and LINKED FROM lines.
  - Leaving the new bullet empty removes it.
  - Capture's own note placement is unchanged.
- **Ctrl+Shift+O on a line outside any task:** it still opens a child bullet, so the Ctrl+Shift+O then `^^` way of linking a task under a Pomodoro keeps working. In insert mode this now works too, where today it refuses.
- **`o` on a headline:** opens a new `- [ ] ` req right after the task's other reqs, or right after the links/deps if it has none. If it's the task's first req, any loose notes move into `Notes` in the same undo step, like Ctrl+] does. Leaving the req empty undoes all of it.
- **`O`:** on a req it still opens a req above. On a headline it still opens a new task. So `O` only creates reqs from a req.
- **Tests:** existing tests that expect the old behavior get updated. New tests go through the actual Ctrl+Shift+O key path, including a test in real Obsidian with a block shaped like your screencast.

**Two choices for you when you review the plan** (each has a default):
1. **Ctrl+Shift+O on a req, drawer header or note line:** by default it adds a child after that line's existing children, as the earlier Ctrl+Shift+O plan intended. The alternative sends those lines to the task's note home too.
2. **`o` on a `^prj` project line:** by default it adds a req, the same as any other headline. The alternative keeps today's behavior of opening a new task in `## Tasks`. None of your 116 project notes currently have reqs under the `^prj` line.

I left one thing out on purpose: making capture also file notes into an existing `Notes` drawer on tasks with no reqs. That changes capture's documented rules in bob-cli and the plugins, so it belongs in its own change if you want it.
