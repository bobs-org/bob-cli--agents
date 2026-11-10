# Chat History - ace-run (1ay--plan)

- **TIMESTAMP:** 2026-11-10 09:50:16 EST
- **MODEL:** claude/opus
- **AGENT:** 1ay--plan

**Plan:** /home/bryan/.sase/plans/202611/tick_alt_p_answer_chip.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/tick_alt_p_answer_chip.md`

> # TICK review rows: show the Alt+P answer as a chip
> ## Goal
> When the cursor is on a task in the **TICK** (TICKLER) review group, the review footer's
> Alt+P preview (today plain muted text like `Alt+P decay P2→P3`, easy to miss between
> `scheduled Nov 10` and `NEW 1`) becomes the most visible element in the footer. It
> renders as a tinted **answer chip** with a keycap, so the eye finds it at once and reads
> what Alt+P will do.
> Why TICK only: for a tickler, "not now" is a priority roll, and Alt+P _is_ that answer
> (`docs/freshness.md`, step 3). TICK rows show no other action hint. On every other tier,
> the Alt+P preview comes second to that tier's own answers (Ctrl+Alt+F keep, Alt+N

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli When a task in the `TICK` GTD review group is selected, can we start making the
hint in the footer that shows the recommended priority decay (this value is used by the
`<alt+p>` keymap, for example) stand out much more? See the
~/tmp/screenshots/20261110_093457.png screenshot for an example of what this looks like
now. I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Opened the bob-plugins repo. Now locating the review footer code that renders the "Alt+P decay" hint.

Found the footer model and paint code in bob-ledger-tools. Now reading the footer CSS and the existing tests.

Still mapping the code: I've read the footer model, painter, CSS, and the nav-side Alt+P preview. Next, checking the tests and docs that cover the footer.

Reading the docs that describe the footer's Alt+P hint, so the plan updates them too.

Bob-cli mounts the plugin docs from bob-plugins, so the docs changes belong there. Checking the priority-mark CSS to see whether the signal-bar glyph can sit inside a status-bar chip.

Got the first prototype screenshot rendering. Checking how it looks.

My added re-fit call used an empty view and hid everything. Fixing the harness.

The version that keeps the "·" separators reads more evenly than the one without them, so I'm keeping them. Checking the narrow 460px bar next.

At 460px the chip stays while the groups and the detail drop, which is what we want. Measuring text contrast on the chip in both themes before committing to the colors.

The script broke on a newline escape inside the template literal. Fixing it.

Contrast stays at 4.67:1 or better even at the flash's peak. Taking a final screenshot of the polished design.

Checking the fake DOM in the footer tests, so the plan's paint approach (spans, no bare text nodes) fits it.

The fake DOM's `textContent` doesn't derive from children, so the plan will have chip tests read text through a descendant-text helper. Reading back the final prototype CSS to embed in the plan.

I have what I need. Writing the plan.

Validation flagged schema issues: missing title/goal, overlong labels, and a memory decision that must be a toggle with `memory:`. Checking the glossary strand's exact text for a verbatim quote.

Validation passes. Proposing the plan.

I wrote the plan and it's waiting for your review: a medium tale, `sase_plan_tick_alt_p_answer_chip.md`. It passed validation and is staged. No repository files were changed.

**The design:** on a TICK row, the Alt+P hint becomes the most visible thing in the footer.

- **A tinted pill in the TICKS blue**, so it visibly belongs to the `TICKS 2/17` label next to it.
- **A solid `Alt+P` keycap** inside the pill, with the text in the status-bar colour. This is what makes it pop, and it reads as "a key you press".
- **The destination in bold:** `decay P2 → P3` puts the weight on P3, where the task ends up. Rolls read `roll P2 2/3` and unprioritized tasks read `set P1`.
- **Red for cancel:** an `Alt+P cancel?` recommendation turns the chip red, because that's the one answer that ends the task.
- **Hovering the chip** shows exactly what the key does, e.g. `Alt+P: decay P2 → P3, 9–31 days out`.
- **On a narrow footer** the chip is the last thing to drop, after the "✓ 12 today" count. Today it disappears before that count.
- **Other groups don't change.** Only TICK rows get the chip, because there Alt+P is the answer for "not now"; on other groups it would compete with that group's own keys. Extending it later is a one-line change.

**Why I expect it to be reliable:**
- The chip's text stays exactly the current hint text, so screen readers, the tooltip and existing tests see the same words.
- The navigation plugin's preview gains a structured breakdown of the hint. The footer uses it only when it rebuilds the exact same text. Otherwise it falls back to splitting off the key, so a mismatch between plugin versions can't make the words differ from today's hint.

I prototyped the chip with the real footer code and stylesheet in headless Chrome, in light and dark themes at 1100, 700 and 460 px. On my first try the light-theme text was too faint (3.3:1), so I darkened it inside the chip. Final contrast is 6.1:1 (light) and 7.6:1 (dark), and it stays at 4.7:1 or better during the landing glow. The screenshots are in `/tmp/bob-footer-proto/`; `final700.png` shows all four kinds.

**Two choices for you when you approve:**
- **`landing_glow`** (default `glow`): the chip's tint fades over 900 ms once each time the review walk lands on a new TICK row. It stays static if your system asks for reduced motion. Pick `still` if you'd rather have no animation.
- **`glossary_review_footer`** (default on): updates the review-footer glossary note. It currently says the meter drops last on narrow bars, which won't be true on TICK rows.

The implementation also updates the plugin docs, `docs/freshness.md` and both plugin manifests, adds tests and preview-harness contrast checks, then runs `bob plugins sync`.
