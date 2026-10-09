- **PLAN:**
  [202610/mac_capture_close_list_auto_comma.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_capture_close_list_auto_comma.md)
- **AGENTS:**
  - [bbugyi200.apollo.61.w1--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.61.w1.md)

  Can you help me improve the bob-mac-capture app so the user doesn't need to manually
  type commas when specifying task link indexes using the `=x`, `=!`, or `=*` syntaxes?

- Namely, if there is less than 10 task links in the current pomodoro (which is normally
  the case), then we should auto-insert a comma when the user presses a `1-9` key if one
  or more indexes for that group (keep in mind multiple groups are supported--e.g.
  `=x2!1,4*3`) have already been typed.
- If there are >=10 task links in the current pomodoro, then we should not do this.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
