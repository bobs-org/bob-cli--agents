#gh:gh_bobs-org__bob-cli We recently added support to the `<ctrl+shift+m>` keymap in Obsidian for
Pomodoro sub-bullets. Can you now help me add support for using this keymap when the
pomodoro bullet itself is selected?

- If the user selects a different Pomodoro when prompted in this case, we should delete
  the current Pomodoro and move all of its sub-bullets to that Pomodoro.
- If the user types in the name of a new Pomodoro, however, we should just rename the
  current Pomodoro.
- See related git commits from earlier today for more context.

#plan #m_opus