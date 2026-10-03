#gh:gh_bobs-org__bob-cli I want to be able to easily select a task to start using the `bob capture`
command and its corresponding bob-mac-capture app with the special `@file:id` syntax.
Can you help me implement this using a new completion menu that is triggered when `:` is
typed at the very start of an input (keep in mind that bulk capture should be supported
with this syntax though)?

- This completion / pop-up menu should allow me to easily fuzzy search through any (not
  completed or canceled) task that lives in any area/project note file in my Obsidian
  vault (i.e. any markdown file in the ~/bob/ directory that has `type: area` or
  `type: project` as a frontmatter field).
- #beau

#plan %m:@xlarge %auto