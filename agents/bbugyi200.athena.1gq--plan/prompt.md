#gh:gh_bobs-org__bob-cli Can you help me remove the `A` (absolute path) option in the copy mode panel
(triggered via the `<cmd+y>` keymap in Obsidian) and add two new options?

- See the ~/tmp/screenshots/20261126_112147.png screenshot for an example of what this
  panel looks like now.
- One of the new options should copy a link to the current file (e.g. `[[foo]]` if the
  current file were the ~/bob/foo.md file).
- The other option should only be shown when a task is selected that has a block ID. It
  should copy a link to that task (e.g. `[[foo#^bar]]` if the `^bar` task in the
  ~/bob/foo.md file is selected).

#plan %m:@xlarge