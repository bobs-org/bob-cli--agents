#gh:gh_bobs-org__bob-cli I would like to add support for syncing my Google Calendar events to my
Obsidian vault as tasks. Can you help me implement this?

- I was thinking we could accomplish this by adding a new `bob gcal` command, which
  support various sub-commands (think hard about which sub-commands we should add).
- These tasks should be rendered in a new "Events" H2 section above the "Pomodoros"
  section in my daily file.
- We should also auto-create a new pomodoro using the MEET theme, which should contain
  task links that correspond with all of the events added to the "Events" section (which
  should be all of the events that I have RSVPed to for that day in Google Calendar).
- Make sure setting up the authentication / login for Google Calendar is easy and
  intuitive.
- We should use the recently added `[root::<root>]` task property to specify that the
  task should use `<root>` as its root parent.
  - We should default to using "meet" to link to the ~/bob/meet.md file as the root
    parent, which should be modernized and turned into a proper area note file as a part
    of this change.
  - We should also support a way for the user to specify in the Google Calendar event
    which parent root to use (think hard about the best way to do this).
- Review the bob_gcal_daily_events.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.2w.linker %auto