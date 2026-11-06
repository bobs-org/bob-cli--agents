#gh:gh_bobs-org__bob-cli I would like to make it so that, when the `@foo[:^]bar@` capture syntax is used
to create a new project note, child tasks can be easily pulled in from the parent
project (the ~/bob/foo.md file in our example). Can you help me implement this?

- I think we can achieve this by usig a `^some-id` reference on a bullet line by itself
  (i.e. with no other text) to specify that we should move the `^some-id` task from the
  parent project file into the new project note that we create with this capture.
- Make sure that pressing `^` in this case (i.e. after a `- ` when the `@foo[:^]bar@`
  syntax has been used somewhere in this capture) triggers good completion from the
  bob-mac-capture app.
- Review the parent_task_move_bullets.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.35.linker