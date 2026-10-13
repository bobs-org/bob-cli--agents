#gh:gh_bobs-org__bob-cli I would like to add support to the bob-mac-capture app for pressing `/` as the
first key in the input box to trigger a new Obsidian task search. Can you help me
implement this?

- This should work just like when the `:` key is pressed as far as task selection goes.
- When a task is selected, however, we should open the appropriate area note / project
  note file in Obsidian and focus the target Obsidian task.
- Review the slash_task_goto_in_obsidian.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).

#plan %m:@xlarge %w:research.4b.linker