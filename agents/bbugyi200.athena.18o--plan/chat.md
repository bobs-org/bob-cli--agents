# Chat History - ace-run (18o--plan)

- **TIMESTAMP:** 2026-11-05 13:21:32 EST
- **MODEL:** claude/opus
- **AGENT:** 18o--plan

**Plan:** /home/bryan/.sase/plans/202611/close_selection_explicit_mode.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/close_selection_explicit_mode.md`

> # Close selections: any typed task number means "only what I listed"
> ## Problem
> `x[<N>][*<P>][!<M>][~<K>][@<N>]` (whole-item `x`, link suffixes `=x…`, and the `x=E=X`
> past close) decides each numbered Task Link's outcome. Today a close switches into
> "selection mode" (unlisted plain links are **deferred**) only when `<N>` is typed
> (including `0` / `@<N>`) or `*<P>` has numbers. With `!<M>` or `~<K>` alone, every
> unlisted plain link keeps its **ledger default**: In Progress, 🍅 in the closed entry,
> carried, task started.
> So `x*2` counts only task 2, while `x!2` counts task 2 **and** every other plain link.
> In selection mode, unlisted Event Task links also keep their clock defaults: `x2` still

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I suspect that the way (e.g. how and when) we default include task links in the
closed pomodoro when using the `x` and `x=` capture syntaxes is inconsistent and
incorrect.

- Namely, we should only default include a task link if all task links are included
  (i.e. no indices were provided--including indices after `!` and `*`).
- Otherwise, only task links that had their index explicitly referenced should be
  included (what "included" means depends on whether the index was after a `!` or `*`).

Does this make sense and do you agree with this policy? If so, use your /sase_plan skill to plan the appropriate changes. %m:@xlarge

## Response

Reading the close-selection docs and code to see how unlisted links are defaulted today.

Found the outcome resolver (`outcome_for` in `capture_pomodoro_close/selection.rs`); now checking whether the `x=` past-close path resolves outcomes the same way.

Confirmed: the `x=` past path shares the same resolver. Next, mapping every other place that encodes the "selection mode" rule (preview summary, Work Log positions, editor hints).

I have the full picture of the current rule and every copy of it. Loading the memory-write routing next, since the plan will need a decision record.

I have enough to write the plan. Writing it now, with the two genuine judgment calls (`~` lists, Event Task clock defaults) embedded as reviewer decisions.

Validator needs title/goal, shorter asks, non-boolean choice keys, and memory toggles. Fixing the frontmatter and decision references.

Now adding decision callouts and rewriting the memory step to match the single combined toggle.

Plan is staged; checking whether the host needs a final declaration.

Yes, your suspicion is right, and I agree with the policy. I've written a plan for it and submitted it for your review.

**What's inconsistent today.** One function in `src/native/capture_pomodoro_close/selection.rs` decides each Task Link's outcome. The `x=` past closes and the `=x…` link forms use it too, so every close form behaves the same way. The rule itself is the problem.

- **Only some numbers switch modes.** Typing `<N>` (including `0`) or numbers after `*` makes unlisted links defer. Numbers after `!` or `~` don't. So `x*2` counts only task 2, but `x!2` completes 2 and also counts every other plain link: each gets a 🍅, is carried to the next session, and is started. `docs/capture.md` describes this as intended, so it's a policy flaw rather than a stray bug.
- **Meetings ignore the numbers.** Even when you type `x2`, an unlisted Event Task link still gets its clock default. A meeting that ended inside the session is completed, and a running one stays In Progress.
- **The rule is copied in several places**, all with the same `*`-only trigger:
  - the Work Log logic that decides which task an unnumbered log line goes to;
  - the `capture-parse` summary, which shows "defer the rest" only for `<N>` or `*`.

**What I'd keep from today.**
- **Bare `*` and `!`** (no numbers) mean "every remaining link", so `x1*`, `x*!2` and `x!~2` keep their meaning.
- **Hand-written markers** keep their meaning: `[[T]]#` stays deferred and `![[T]]` stays complete. You chose those by hand, so they aren't defaults.
- **`x0` followed by another list** (`x0!2`) becomes the same as `x!2`. It stays valid, and a note-free `x0` is still the reset.

**The plan** is one task of medium size. It:
- defines one shared "were any task numbers typed?" check and uses it in all the places above;
- fixes the "list it / complete it" suggestions so they keep the `!` and `~` lists you typed;
- updates tests, the shared test fixtures and the docs;
- does read-only checks in bob-plugins and bob-mac-capture for test fixtures or pinned text that would break;
- ships as a commit marked breaking (`feat(capture)!`).

**Your answers, which the plan asks for at review:**
- **Does a `~` list alone count as typed numbers?** My default is yes, which follows your wording literally. Then `x~2` drops 2 and defers the rest, and "drop 2, keep working 1 and 3" becomes `x1,3~2`. The alternative keeps `~` as remove-only.
- **Do unlisted meetings also defer once numbers are typed?** My default is yes, because a clock default is still a default include. Then `x!3` defers a meeting that ended during the session, and you'd type `x!1,3` to count it.
- **Memory:** add a new decision record, `close-selections-list-explicitly`, and mark the existing "Event Task links close by the clock" record as partly replaced. That record says unlisted meeting links always follow the clock, which this change would make false. Default is on.
