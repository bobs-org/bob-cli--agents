- **PLAN:**
  [202610/capture_task_dependencies.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_task_dependencies.md)
- **AGENTS:**
  - [bbugyi200.apollo.4m--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4m.md)

Can you help me add support for a new `&foo:bar` syntax to the `bob capture` command and
its corresponding bob-mac-capture app that adds a task dep link for the task specified
by `foo:bar` (e.g. `[[foo#%^bar]]`)?

- The target task should be either the task that we are capturing (if the capture text
  looks like a task capture) or an explicitly targeted pre-existing task by using the
  `@file+id` syntax to specify that task.
- For example, `Buy Groceries! &foo:bar` will create a new `Buy Groceries!` task with a
  dep link to `[[foo#^bar]]`, whereas `&foo:bar @body:excercise` would add that dep link
  to the existing `^excercise` task in the ~/bob/body.md file.
- Pressing `&` at the beginning of a capture or after a space at the end of a line in
  the bob-mac-capture app should trigger an excellent completion menu that allows the
  user to fuzzy search for any task in their Obsidian vault. See how we do this when `:`
  is typed at the beginning of a capture for context and inspiration.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
