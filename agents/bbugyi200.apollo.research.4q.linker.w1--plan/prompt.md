#gh:gh_bobs-org__bob-cli I use a different Google Calendar (under the same bryanbugyi34@gmail.com
account) to track birthdays. See the ~/tmp/screenshots/20261115_105604.png screenshot
for context. I would like the `bob gcal sync` command to support syncing multiple
calendars from the same account starting with this "Birthdays" calendar. Can you help me
implement this?

- It should always be clear which event task came from which Google Calendar.
- Once you're confident in the implementation, you should run the
  `bob gcal sync -D yesterday` command with the updated `bob` binary to ensure that this
  worked (Ava's birthday should be added as an all-day bullet).
- Review the gcal_multi_calendar_sync.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.4q.linker