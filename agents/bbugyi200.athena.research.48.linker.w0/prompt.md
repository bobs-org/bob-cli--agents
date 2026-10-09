#gh:gh_bobs-org__bob-cli I would like to start showing the current pomodoro (if any) and all future
pomodoros in the preview shown by the bob-mac-capture app when no input text has been
typed. Can you help me implement this?

- This preview should therefore load by default when the panel first pops up.
- Since we will load this preview so often, we should make sure to cache it somehow when
  the daily file's contents haven't changed at all. IMPORTANT: The bob-mac-capture app
  MUST be blazing fast.
- For each task associated with a task link in a current or future pomodoro in today's
  daily file, we should always show as much of each task's contents as possible without
  causing the user to need to scroll the preview pane.
- This means that, if it all fits in the preview pane without the user needing to scroll
  (we should expand the height of the window as neccessary), we shoould show the full
  task definition for each task including all of its sub-bullets.
- Otherwise, we should support two folded views, which we will use in this order of
  priority, if necessary, to decrease the size of the contents in the preview pane:
  1. A view of each task that does not show the work log or schedule log for that task,
     but shows all other sub-bullets.
  2. A single-line view of each task.
- Review the idle_capture_pomodoro_agenda.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file.
- #beau

#plan %m:@xlarge %auto %w:research.48.linker