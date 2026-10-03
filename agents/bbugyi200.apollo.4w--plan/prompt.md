#gh:gh_bobs-org__bob-cli The review indicators that we show in Obsidian on the bottom right (shown in
the ~/tmp/screenshots/20261003_172431.png screenshot) are useful, but I'd like to make
some improvements. Can you help me implement these?

- We should only show a review group if there are 1 or more tasks in that group. For
  example, in the ~/tmp/screenshots/20261003_172431.png screenshot, `projects 0` should
  not be shown.
- The toast that is shown by the `]s` keymap is nice, but it would be better if a
  condensed form of that information was always visible while there are still tasks to
  review. Let's start showing it on the bottom of Obsidian somewhere, but only if there
  are tasks to review. Otherwise, we should not show it or any of these counts.
- #beau

#plan %auto