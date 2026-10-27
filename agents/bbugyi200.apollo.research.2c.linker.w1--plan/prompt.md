#gh:gh_bobs-org__bob-cli I would like to add much better support for "pomodoro themes" (aka "pomodoro
names", "themes"). Can you help me implement this?

- We should add a new glossary term for this.
- We should start suggesting the names of previously used themes anywhere that themes /
  pomodoro names are shown in a completion menu (including the bob-mac-capture app).
- If existing theme / pomodoro names are listed in the same completion menu (and not
  filtered out by the user's query), those should be prioritized (i.e. shown at the top)
  over previously used themes.
- The user should have the ability to rename themes globally (all daily files that use
  that theme should be updated).
- The user also needs to be able to disable a theme, which should result in it no longer
  appearing in completion menus. Think hard about how/where we should support this
  functionality (via a new `<ctrl+d>` keymap in completion menus maybe?).
- Themes should be given a distinct color somehow, which should be deterministic based
  on the theme name. We should try to use these colors anywhere that themes are shown
  (including in Obsidian itself).
- Review the pomodoro_theme_catalog.md file in the research sidecar repo for context and
  inspiration before planning. I agree with all of the requirements recommended in that
  research file (but keep in mind that you are responsible for planning and splitting up
  this work appropriately).
- #beau

#plan %m:@xlarge %w:research.2c.linker %auto