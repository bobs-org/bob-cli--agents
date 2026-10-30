#gh:gh_bobs-org__bob-cli When I just attempted to promote a task to a project using the
`<cmd+ctrl+shift+n>` keymap in Obsidian, the source task was not deleted for some
reason. I'm thinking this was probably because the task had a corresponding task link in
today's daily file? We should fix this, but it has made me aware of another issue.
Namely, when we promote a task to a project and that task has a task link in today's
daily file, the prj task would wind up having a task link associated with it. This is
not correct. Instead, in such a case, we should treat all child tasks created in the new
project note the same as we do task successors when a task with dependents is closed.
Can you help me implement this?

- See the ~/tmp/screenshots/20261030_160413.png screenshot for some context behind the
  task that I just tried to promote to a project.
- As a part of this change, let's add a new "task successor" (aka "successor") glossary
  term.
- #beau

#plan %m:@xlarge