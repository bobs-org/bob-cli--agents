- **PLAN:**
  [202609/task_link_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_link_picker.md)
- **AGENTS:**
  - [bbugyi200.apollo.3j--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3j.md)

I want to be able to easily select a task to start using the `bob capture` command and
its corresponding bob-mac-capture app with the special `@file:id` syntax. Can you help
me implement this using a new completion menu that is triggered when `:` is typed at the
very start of an input (keep in mind that bulk capture should be supported with this
syntax though)?

- This completion / pop-up menu should allow me to easily fuzzy search through any (not
  completed or canceled) task that lives in any area/project note file in my Obsidian
  vault (i.e. any markdown file in the ~/bob/ directory that has `type: area` or
  `type: project` as a frontmatter field).
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
