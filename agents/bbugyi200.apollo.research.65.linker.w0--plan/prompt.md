#gh:gh_bobs-org__bob-cli I've been using Wispr Flow to automatically transcribe meeting notes. I would
like to integrate AI meeting notes into event tasks by making it as easy as possible for
users to create excellent ref notes for these meetings that are associated with the
correct area/project and are properly linked to the corresponding event task. Can you
help me implement this?

- As our first use-case for this functionality, I would like to create a ref note from
  the ~/tmp/bryan_derrick_meet_notes.txt file (contains a Wispr Flow meeting transcript)
  and link it to the ^bryan-bugyi-derrick task in the ~/bob/2026/20261123.md file.
- Think hard about what the best UX for this functionality is.
- Review the meeting_notes_event_refs.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- #beau

#plan %m:@xlarge %w:research.65.linker