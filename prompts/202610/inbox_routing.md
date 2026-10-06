- **PLAN:**
  [202610/inbox_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/inbox_routing.md)
- **AGENTS:**
  - [bbugyi200.athena.0xh--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0xh.md)

I would like to add special support to the `<ctrl+shift+p>` and `<ctrl+shift+enter>`
keymaps for any task that lives inside an area file that has the "inbox" area note file
(i.e. the ~/bob/inbox.md file) as its parent. Can you help me implement this?

- Namely, when invoked on a task that lives in one of these files, right before
  performing whatever action was selected by the user, we should prompt the user for a
  file to move the task to (like the `<ctrl+shift+m>` keymap does).
- This makes sense I think since no task should ever live in an inbox note file forever.
- This change also allows us to move these tasks without giving up support for
  auto-jumping to the next review task (during my morning GTD review), since I can just
  use one of the `<ctrl+shift+p>` or `<ctrl+shift+enter>` keymaps directly on these
  tasks now (i.e. without needing to use the `<ctrl+shift+m>` keymap first).
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
