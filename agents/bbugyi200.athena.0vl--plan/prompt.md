#gh:gh_bobs-org__bob-cli I would like to improve the way that I track Obsidian task dependencies.

- I currently use transcluded links to tasks as sub-bullets on task A when I want to
  treat those tasks as dependencies of task A (i.e. those tasks need to be completed
  before task A is marked as unblocked).
- I want to stop using transcluded task links and instead just use normal task links for
  this. I also want to start listing all dependency task links on a single line in some
  visually appealing way.
- Finally, it needs to be very easy for users to add/remove dependency tasks, which can
  be located in any area/project note file in my Obsidian vault, to/from the currently
  selected task. I was thinking we could use the `<ctrl+shift+p>` keymap for this
  somehow, which already has support for our current dependency solution I think.
  Whatever solution you decide on, keep in mind that we need to support fuzzy searching
  for tasks across my entire Obsidian vault.
- We should add a new "task dependency link" (aka "task dep link") glossary memory web
  term to describe these dependency task links.
- Review the task_dep_link_depends_on_line.md file in the research sidecar repo for
  context and inspiration before planning. I agree with all of the recommendations made
  in that research file.
- #beau

Can you help me implement this? #plan %m:@xlarge %auto