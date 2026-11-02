#gh:gh_bobs-org__bob-cli I would like to add support for a special new "starts after" relation label.
Can you help me implement this?

- This label should be rendered as "starts before" in the mirrored "linked from" bullet.
- The goal of this label is to allow me to trigger a successor prompt for certain tasks
  when another task is marked as wip/pending and moved out of the daily file (an
  operation that is unique to the `x*` capture syntax I believe). This will be useful
  since the tasks that I target with `x*` are often ones that correspond with work that
  I have assigned to an agent and I sometimes have another prompt that I want to think
  through and send out only after I have done the same for some other task (this is the
  one that I plan to target with the "starts after" relation).
- The successor prompt should also be triggered if the target task is closed (this is
  how normal successors work).
- Make sure it is very clear why this successor prompt is being triggered since we have
  various types of successors now.
- Review the starts_after_relation.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.5m.linker