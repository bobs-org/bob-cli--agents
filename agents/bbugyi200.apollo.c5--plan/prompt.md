%auto
#gh:gh_bobs-org__bob-cli Can you help me add support for adding `-<N>` and/or `+<M>`, where `<N>` and
`<M>` are expected to be integers and specify a number of minutes, to Google Calendar
event descriptions to specify that a pre-event buffer (in the case of `-<N>`) and/or a
post-event buffer (in the case of `+<M>`) should be added to the time range that bob
expects the event to occupy?

- Make sure that the `bob gcal sync` command renders these pre/post-event buffers in
  some visually appealing way on the event tasks that it creates.
- Make sure that the capture `=` syntax default time range for MEET pomodoros is updated
  and that we warn users appropriately when they attempt to overlap an event's time
  range (including the pre/post-event buffer).
- Make sure that `@<root>` tags, the `#untracked` tag, and these new `-<N>`/`+<M>` tags
  can all be safely placed on a single line in the Google Calendar event description
  without being missed/skipped by the `bob gcal sync` command. For example,
  `@love #untracked -30` should be valid.
- See the bob-cli-f6 epic bead for some context.
- #beau

#plan %m:@xlarge %wait(bead=bob-cli-f6)