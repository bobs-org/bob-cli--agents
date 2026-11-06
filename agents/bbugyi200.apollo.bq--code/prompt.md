%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202610/mac_capture_ctrl_g_toggle_case.md

The above plan has been reviewed and approved. Implement it now.

Reviewer decisions for this plan (final · reviewer via ACE):
- case_rule = line (planner default: line). Implement the "case_rule = line" branch; ignore "case_rule = swap". Context: "Should Ctrl-G U set the whole line to one case (UPPER, else lower) instead of swapping each letter?".
- stray_key = beep (planner default: beep). Implement the "stray_key = beep" branch; ignore "stray_key = passthrough". Context: "Should an unbound key pressed right after Ctrl-G be swallowed with a beep instead of acting normally?".
- leader_hint = show (planner default: show). Implement the "leader_hint = show" branch; ignore "leader_hint = hide". Context: "Should the footer status line show a pending-chord hint while Ctrl-G waits for its next key?".
Implement only the branches selected above.
