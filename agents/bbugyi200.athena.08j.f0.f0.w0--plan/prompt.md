#gh:gh_bobs-org__bob-cli %w:08j.f0.f0 Can you help me start deleting the current bullet's section if
it is the last bullet in that section and we use the `<ctrl+shift+]>` Obsidian keymap to
convert the bullet to a task?

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

#plan