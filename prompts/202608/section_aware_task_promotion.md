- **PLAN:**
  [202608/section_aware_task_promotion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/section_aware_task_promotion.md)
- **AGENTS:**
  - [bbugyi200.athena.08j.f0.f0.w0--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.08j.f0.f0.w0.md)

  Can you help me start deleting the current bullet's section if it is the last bullet
  in that section and we use the `<ctrl+shift+]>` Obsidian keymap to convert the bullet
  to a task?

- On a somewhat related note (though we should do this regardless of whether the current
  section has any more bullets or not), if there are other sections in the file besides
  "Tasks", let's start prompting the user to select a section.
- If they select any section except for "Tasks", the bullet should NOT be converted to
  an Obsidian task. Instead, we should just move that bullet to the selected section
  (and delete the current section if this is the last bullet in that section).
- If they just hit `<enter>` when prompted, we should default to selecting the "Tasks"
  section and the bullet should be converted to an Obsidian task.
- Finally, let's start making this functionality (section prompting/creation/moving for
  the `<ctrl+shift+]>` keymap) work for any Obsidian note file containing a "Tasks"
  section (I think we maybe only support project note files at the moment).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
