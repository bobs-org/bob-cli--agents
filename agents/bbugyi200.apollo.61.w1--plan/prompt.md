#gh:gh_bobs-org__bob-cli %w:61 Can you help me improve the bob-mac-capture app so the user doesn't need
to manually type commas when specifying task link indexes using the `=x`, `=!`, or `=*`
syntaxes?

- Namely, if there is less than 10 task links in the current pomodoro (which is normally
  the case), then we should auto-insert a comma when the user presses a `1-9` key if one
  or more indexes for that group (keep in mind multiple groups are supported--e.g.
  `=x2!1,4*3`) have already been typed.
- If there are >=10 task links in the current pomodoro, then we should not do this.

#plan %m:@xlarge %auto