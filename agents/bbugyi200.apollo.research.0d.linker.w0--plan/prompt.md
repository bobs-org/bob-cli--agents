#gh:gh_bobs-org__bob-cli I would like to integrate more of my keymaps with my GTD morning review, which
I trigger via the `]s` Obsidian keymap and continue walking through using `]s` until I
have reviewed all items from all review groups. Can you help me implement this?

- I already added support for the `<ctrl+enter>` keymap for the PRE review group, but
  I'm thinking that anytime that we close the current review item using this keymap, we
  should use this behavior (i.e. automatically jump to the next/first review item).
- Also, there are multiple other keymaps that trigger actions which also imply that we
  should iterate to the next review item. The `<ctrl+shift+enter>` and `<ctrl+shift+p>`
  (assuming a task card option is selected that removes the review item from the review
  stack) keymaps, for example, should ideally trigger an automatic jump to the next
  review item.
- You should look for and propose other keymaps / actions that should trigger a jump to
  the next review item when in the middle of a GTD morning review.
- Review the review_walk_answer_auto_advance.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the recommendations made in that research file.
- #beau

#plan %m:@xlarge %auto %w:research.0d.linker