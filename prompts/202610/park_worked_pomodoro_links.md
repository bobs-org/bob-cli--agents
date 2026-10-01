- **PLAN:**
  [202610/park_worked_pomodoro_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/park_worked_pomodoro_links.md)
- **AGENTS:**
  - [bbugyi200.athena.0un.w0--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0un.w0.md)

  Can you help me add support to the `bob capture` command and the corresponding
  bob-mac-capture app for a new `=x*<N>` syntax that works like the `=x<N>` syntax
  except that the selected task links are not copied over to the new pomodoro that is
  created?

- This will be useful, for example, when we just launched an agent swarm to complete
  some work that we won't be able to verify for another few hours (we don't want that
  task link hanging out in our daily file all day).
- This syntax needs to compose with and work well with the other supported `=x` syntaxes
  (for example, `=x1*2,3!4,5` should work if there are 5 task links in the current
  pomodoro).
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
