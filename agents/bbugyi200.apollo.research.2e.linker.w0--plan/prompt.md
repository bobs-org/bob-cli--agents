#gh:gh_bobs-org__bob-cli The bob-mac-capture app's relation card's tab-completion doesn't work, right.
It seems to just complete the first (or nth if you hit `<tab>` fast enough I think)
relation description and then when you hit `<tab>` again nothing happens (see the
~/tmp/screenshots/20261024_093115.png screenshot for an example of what this looks like
now). I would like to fix this and improve the relation card in general. Can you help me
implement this?

- We should start using the `<ctrl+n/p>` keymaps to reliably navigate to the different
  completion menu entries (which are previous relation descriptions) that have not been
  disabled/hidden.
- We need to add the ability to disable/hide relation descriptions (maybe via a new
  `<ctrl+d>` keymap on the relation card?). This will be used to support temporary /
  one-off relationships.
- Make sure we also have a keymap to show all relation descriptions (even disabled ones)
  and a way to re-enable/unhide a relation description.
- We also need to the ability to reliably rename a relation description from the
  relation card (and from the command-line and Obsidian) such that all tasks with that
  same relation description are updated appropriately.
- The new `~file:id||<desc>` capture syntax (note the double `|`) should be supported to
  allow relation descriptions to be specified as hidden when they are created. Make sure
  we display some kind of warning to the user (e.g. in bob-mac-capture) if they attempt
  to hide a relation description that already exists using this capture syntax (this
  should be supported, but it should be clear to the user when this will be done).
- Review the relation_card_label_vocabulary.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %auto %w:research.2e.linker