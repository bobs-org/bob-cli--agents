#gh:gh_bobs-org__bob-cli I would like to add support for embedding video files in task captures and
viewing those videos using the `Z` keymap in Obsidian. Can you help me implement this?

- This functionality should take heavy inspiration from the corresponding functionality
  for image files.
- For example, if `~/tmp/screencasts/20261116_155943.mp4` were the contents of my
  clipboard, I would expect that including the `%c` directive in a task capture would
  trigger that video file to be embedded in the new task as a sub-bullet.
- Review the task_video_capture_z_viewer.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.63.linker