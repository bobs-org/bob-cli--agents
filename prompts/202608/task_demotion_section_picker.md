- **PLAN:**
  [202608/task_demotion_section_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/task_demotion_section_picker.md)
- **AGENTS:**
  - [bbugyi200.athena.08j.f0--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.08j.f0.md)

%xprompts_enabled:false

# Previous Conversations

You are forking from 1 prior source. Source sections are independent parents, and
section order carries no priority. Members inside an agent family section are
sequential: each member continued the previous member's work. Carry forward relevant
goals, constraints, decisions, and unfinished work with attribution when it matters. The
New Query is the active request and takes precedence over conflicting source
instructions.

## Source 1 of 1 — agent family `08j`

- **Members shown:** 2 of 2 (sequential chain, oldest first)

Family members ran as one sequential chain: each member continued the previous member's
work, and the last member reflects the family's final state. These are transcripts of
prior agents' conversations, not your own — attribute decisions to the named member when
it matters.

### Member 1 of 2 — agent `08j--plan`

- **Outcome:** `completed` · **Model:** `codex/gpt-5.6-sol` · **Launch:**
  `20260820085222`
- **Transcript:**
  `~/.sase/chats/202608/gh_bobs_org__bob_cli-ace_run-08j__plan-260820_085222.md`

**User:**

The `<ctrl+shift+]>` Obsidian keymap can be used to convert an Obsidian task to/from a
normal bullet. There is a special case (I think when a "Tasks" section exists and some
other markdown section exists?) where we also move that new task/note to the "Tasks"
section / next markdown section, respectively. In project note files, which have a
`type: [[project]]` field in their frontmatter, we always have a "Tasks" section, but do
not always have other sections. Can you help me start creating a new "Requirements" H2
section at the bottom of the file (after a blank line) when the `<ctrl+shift+]>` keymap
is used to convert a task to a normal bullet from a project note file that only contains
a "Tasks" section? This bullet should then be moved to this new "Requirements" section
(after a blank line).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.

**Assistant:**

_Plan submitted for review._

**Plan file:** `/home/bryan/.sase/plans/202608/project_requirements_section.md`

> # Create a Requirements section when demoting the only project task section
>
> ## Goal
>
> Extend the `bob-plugins` Task Status Cycler so the `<Ctrl+Shift+]>` / `<Ctrl+}>`
> “Toggle Obsidian task” action handles a project note whose only Markdown section is
> `## Tasks`: when a top-level task in that section is converted to a normal bullet,
> append a new `## Requirements` section to the bottom of the note and move the
> converted bullet block into it. Preserve the existing routing behavior everywhere
> else.
>
> ## Implementation
>
> 1. Open the linked `bob-plugins` repository with `sase repo open bob-plugins` and use
>    the returned checkout path for all work. Re-read its `AGENTS.md` before editing.

_See full plan file for details._

### Member 2 of 2 — agent `08j--code`

- **Outcome:** `completed` · **Model:** `grok/grok-4.6` · **Launch:** `20260820085719`
- **Transcript:**
  `~/.sase/chats/202608/gh_bobs_org__bob_cli-ace_run-08j__code-260820_085222.md`

**User:**

@sase/repos/plans/202608/project_requirements_section.md

The above plan has been reviewed and approved. Implement it now.

**Assistant:**

I'll implement the approved plan by opening the linked `bob-plugins` repo and following
its instructions before touching the Task Status Cycler.

Opening `bob-plugins` and pulling the implementation prompt so I can match the existing
plugin code.

AGENTS.md is short. Next I’ll inspect the cycler, tests, and docs so the fallback
matches current routing.

The toggle planner is the core. I’ll read that path plus the existing tests so the new
fallback doesn’t change other routes.

The prompt and current frontmatter parsing should pin down the exact project-marker
rules.

I have the routing path. Next I’ll add the project-marker check, the Requirements
fallback, tests, and the version bump.

The command path failed only because the probe used a different `MarkdownView`. I’ll add
the tests with the file’s existing stub.

Focused suite is green (113 tests). Next I’ll run the repo-wide checks, review the diff,
and sync the plugin.

Implemented in the linked `bob-plugins` repo. Demoting a top-level `#task` from a
project note whose only real Markdown section is `## Tasks` now creates a bottom-of-file
`## Requirements` section and moves the converted bullet block there.

**Behavior**

- `type: [[project]]` and the quoted form `type: "[[project]]"` (plus `'[[project]]'`)
  are recognized only as a top-level scalar in a closed YAML frontmatter block.
- Nested keys, comments, body text, and unclosed/malformed frontmatter are ignored.
- Fallback runs only when there is no next section under the existing rule, the source
  is a top-level dash task in the direct `## Tasks` body, and `## Tasks` is the
  document’s only real heading.
- Spacing: one blank line before `## Requirements`, one blank line before the moved
  bullet, trailing blanks collapsed, final newline preserved.
- Existing promotion, next-section demotion (including an existing `Requirements`
  section), and in-place conversion are unchanged.

**Version:** Task Status Cycler `1.9.0` → `1.10.0` (manifest + README, including
`<Ctrl+Shift+]>` / `<Ctrl+}>`).

**Validation** | Check | Result | |---|---| |
`node --test scripts/test-task-status-cycler.cjs` | 113 passed | | `npm test` | 525
passed | | `npm run validate` | 6/6 plugins valid | | Diff | 4 files only: `main.js`,
tests, `manifest.json`, `README.md` |

**Deploy:** `bob plugins sync` copied `task-status-cycler` `manifest.json` and `main.js`
into the vault (`2 copied`, backups under
`~/.local/state/bob-cli/plugin-backups/20260820-090730`). Reload the plugin in Obsidian
to pick up 1.10.0.

The implementation is already in the linked `bob-plugins` repo. I’ll read the commit
skill and then commit those four files.

I’ll record the commit-skill use and inspect the `bob-plugins` diff so the message
matches only those four files.

The workspace itself is clean; I’ll inspect the linked `bob-plugins` checkout next.

I’ll write the conventional commit message and commit the four `bob-plugins` files from
that checkout.

The commit ran in the wrong checkout. I’ll recreate the message in `bob-plugins` and
commit from there.

The commit is still running in `bob-plugins`. I’ll wait for it to finish in this turn.

The commit succeeded. I’ll confirm `bob-plugins` is clean and in sync with origin.

Committed the Task Status Cycler work in the linked `bob-plugins` repo.

**Commit:** `f49bc53` —
`feat(task-status-cycler): create Requirements when demoting the only project task`

Included:

- `plugins/task-status-cycler/main.js` — project-marker check and `## Requirements`
  fallback
- `scripts/test-task-status-cycler.cjs` — planner and command-path regressions
- `plugins/task-status-cycler/manifest.json` — `1.9.0` → `1.10.0`
- `README.md` — documented `<Ctrl+Shift+]>` / `<Ctrl+}>` behavior

`bob-plugins` is clean and in sync with `origin/master`. Prompt archive publication was
skipped because `raw_xprompt.md` was unavailable; the commit itself succeeded.

---

%xprompts_enabled:true

# New Query

Can you now help me change this so we prompt the user for the name of the new section
instead (default to "Requirements" if the user just presses `<enter>` without typing
anything)?

- Also, let's always start prompting the user to select a section when using this keymap
  to convert an Obsidian task in a "Tasks" section to a normal bullet, even when there
  is only one section other than the "Tasks" section in that file.
- The user should be able to select from existing sections (other than the "Tasks"
  section) in that file or type in a new section name to create a new section in that
  file (and move the normal bullet to that section).
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
