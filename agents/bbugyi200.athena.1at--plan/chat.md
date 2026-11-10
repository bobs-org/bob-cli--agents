# Chat History - ace-run (1at--plan)

- **TIMESTAMP:** 2026-11-10 07:38:38 EST
- **MODEL:** claude/opus
- **AGENT:** 1at--plan

**Plan:** /home/bryan/.sase/plans/202611/mac_capture_alias_tips_anchor.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/mac_capture_alias_tips_anchor.md`

> # Plan: Make Mac Capture typing tips actually appear
> ## Diagnosis (already established; do not re-investigate)
> Bryan's suspicion is right. The capture alias typing tips ("Next time `.` → `@`") have
> never appeared in the shipped Bob Mac Capture.
> **bob is correct.** `bob capture-rewrite --cursor N -f json` returns a proved
> `sigil_alias_tip` on Bryan's Mac. Examples: `Buy milk @` gives `route_after_text`,
> `@file:` gives `link_after_route`, `@file^` gives `block_id_after_route`, and `@file+`
> gives `parent_task`. The call takes about 10–20 ms there, while `capture-parse` takes
> 10–20 ms and `capture-complete` 70–80 ms. bob-cli needs no change.
> **The Mac drops every proved tip.** Bryan's ledger on the Mac

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Were capture alias hints (shown when the user explicitly typed a character that
they could have used a capture alias for) ever implemented correctly? I'm not seeing
them in the bob-mac-capture app. Can you help me confirm/deny my suspicion, diagnose the
true root cause, and fix the issue?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Checking progress: bob's side works. `bob capture-rewrite --cursor` returns `sigil_alias_tip` for `@`, `#` and `^`. Next I'm opening the bob-mac-capture repo to see how the app consumes the tip.

Still tracing the Mac app's tip path: how a Shift-typed sigil is recorded, then asks bob, then waits for the first list or picker to open.

Still narrowing it down. bob proves the tips correctly, so the drop happens inside the Mac app's admission logic. I'm reading the completion and picker dispatch now.

Writing the plan now. One last check: whether the test fake bob already covers the route-then-`:` sequence, so the plan can say which fixtures to add.

The plan passed validation. Revalidating without `--explain`, then submitting it.

You're right: the alias hints have never shown in Bob Mac Capture. bob does its part correctly; the Mac app throws every hint away. I've staged a plan to fix it, and nothing has been changed yet.

**Evidence**
- **bob works.** On your Mac, `bob capture-rewrite --cursor` answers with the correct hint for each case I tried: `Buy milk @` → `route_after_text`, `@file:` → `link_after_route`, `@file^` → `block_id_after_route`, `@file+` → `parent_task`. It answers in about 10–20 ms.
- **The app drops them all.** Its hint record on your Mac shows 0 shown for every lesson. This week bob proved 30 hints there: 19 `route_after_text`, 8 `link_after_route`, 2 `relation` and 1 `parent_task`. So the app does ask bob and gets answers, then discards them before display.

**Root causes** (both from the follow-up commit `542a37d`, "repair alias tip lifecycle", in bob-mac-capture's `CapturePanelModel.swift`):
1. **Any keystroke after the sigil kills the hint.** The hint is tied to the exact text at the moment you typed the sigil, and any later change throws it away. The list or picker only opens after a 50 ms typing pause plus two bob calls, and each keystroke restarts that pause. When you type `@er` without stopping, the text has changed before the list exists. Even a hint that did show would vanish on the next filter keystroke, which contradicts the original design ("keep it unchanged while the query filters"). This explains the `@` misses.
2. **The previous token's list counts as already open.** When you type `@errands` then `:`, `^` or `+`, the route list for `@errands` is still on screen. The app takes that leftover list as the surface the sigil opened, so the hint arrives "late" and is dropped every time. This explains the picker hints that follow a route.

The existing tests missed both: they never type after the sigil, and the picker tests never start with a route list open.

**The fix (staged plan, medium tale, bob-mac-capture only)**
- **Anchor the hint to the sigil.** Show it on the first list or picker whose replacement range starts at the typed sigil. Typing the rest of the query keeps it. A list left over from the previous token doesn't count. Editing at or before the sigil removes it.
- **Keep the original rules.** It still appears only in the first frame, a late answer from bob is still dropped, and you still get at most one hint per panel session.
- **Add regression tests** that drive the real typing path for both bugs (typing `@er` without a pause, and a route list followed by `:`). Update `docs/typing-tips.md`.
- **One decision for you, `drop_reason_counts` (default yes):** the hint record would also count *why* each hint wasn't shown, so a future failure like this can be diagnosed from that record alone.

After it's installed you can check by hand. Type `Buy milk @er` without pausing: the route list should end with a "Next time `.` → `@`" line that stays while you keep typing. Typing `@<route>:` should show "Next time `;` → `:`" in the picker. Three lessons are already marked fluent in your record and will stay quiet by design: `#`, `^` after a route, and `*`.
