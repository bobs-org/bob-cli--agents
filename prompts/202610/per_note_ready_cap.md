- **PLAN:**
  [202610/per_note_ready_cap.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/per_note_ready_cap.md)
- **AGENTS:**
  - [bbugyi200.athena.0v5--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0v5.md)

One of my goals while reviewing my Obsidian tasks during my morning GTD is to make sure
that no area/project note file contains more than N ready tasks (this number should be
configurable, but should default to 5).

- The idea is that if I have more than N ready tasks in a area/project, then I should
  probably look into creating a new project from some of those tasks and/or
  de-prioritizing (using the `<ctrl+shift+p>` keymap, for example) some tasks in that
  area/project note file.
- I would like to make it clearer which project files have more ready tasks than they
  should.
- We should show some kind of notification / toast in Obsidian anytime we use any one of
  the Obsidian keymaps that would cause this constraint to be violated (for example,
  when moving a task to a project note file that already has >=N ready tasks).
- We should show a badge and/or diagnostics in the ~/bob/dash.md file and/or in project
  note files that makes it clear how many area/projects violate this contraint currently
  (and which ones).
- I should also have the ability to view this information from the command-line. Namely,
  I should have the ability to review the number of ready tasks in each area/project
  note file from the command-line and should be able to see (in some visually appealing
  way) when this constraint is being violated (and in which area/project note files).
- Review the per_note_ready_cap.md file in the research sidecar repo for context and
  inspiration before planning. I agree with all of the recommendations made by that
  research file.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Can you help me implement this? Think this through thoroughly and create a plan using
your `/sase_plan` skill. Choose and author the appropriate tier, validate and revalidate
until it passes, then submit it with `sase plan propose` (as the skill instructs) before
making any file changes.
