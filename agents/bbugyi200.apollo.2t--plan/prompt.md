#gh:gh_bobs-org__bob-cli I want to implement a new `bob gkeep` command. Can you help me implement this?

- This command will have a sub-command that migrates all of my current Google Keep inbox
  items (which I can see by going to https://keep.google.com/#home) to Obsidian tasks in
  the ~/bob/gkeep_inbox.md file.
- These Google Keep items should be archived in Google Keep once we are sure the
  migration was successful.
- This command should also have a sub-command that allows me to list all items in my
  Google Keep and/or Obsidian tasks in the ~/bob/gkeep_inbox.md file.
- Review the bob_gkeep_inbox_drain.md file in the research sidecar repo for context and
  inspiration before planning.
- #beau

#plan %m:@xlarge %auto