- **PLAN:**
  [202611/gcal_event_buffers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_event_buffers.md)
- **AGENTS:**
  - [bbugyi200.apollo.c5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c5.md)

Can you help me add support for adding `-<N>` and/or `+<M>`, where `<N>` and `<M>` are
expected to be integers and specify a number of minutes, to Google Calendar event
descriptions to specify that a pre-event buffer (in the case of `-<N>`) and/or a
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
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
