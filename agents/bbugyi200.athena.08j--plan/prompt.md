#gh:gh_bobs-org__bob-cli The `<ctrl+shift+]>` Obsidian keymap can be used to convert an Obsidian task
to/from a normal bullet. There is a special case (I think when a "Tasks" section exists
and some other markdown section exists?) where we also move that new task/note to the
"Tasks" section / next markdown section, respectively. In project note files, which have
a `type: [[project]]` field in their frontmatter, we always have a "Tasks" section, but
do not always have other sections. Can you help me start creating a new "Requirements"
H2 section at the bottom of the file (after a blank line) when the `<ctrl+shift+]>`
keymap is used to convert a task to a normal bullet from a project note file that only
contains a "Tasks" section? This bullet should then be moved to this new "Requirements"
section (after a blank line).

#plan