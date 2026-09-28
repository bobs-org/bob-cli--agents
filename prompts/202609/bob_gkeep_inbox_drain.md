- **PLAN:**
  [202609/bob_gkeep_inbox_drain.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/bob_gkeep_inbox_drain.md)
- **AGENTS:**
  - [bbugyi200.apollo.2t--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2t.md)

I want to implement a new `bob gkeep` command. Can you help me implement this?

- This command will have a sub-command that migrates all of my current Google Keep inbox
  items (which I can see by going to https://keep.google.com/#home) to Obsidian tasks in
  the ~/bob/gkeep_inbox.md file.
- These Google Keep items should be archived in Google Keep once we are sure the
  migration was successful.
- This command should also have a sub-command that allows me to list all items in my
  Google Keep and/or Obsidian tasks in the ~/bob/gkeep_inbox.md file.
- Review the bob_gkeep_inbox_drain.md file in the research sidecar repo for context and
  inspiration before planning.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
