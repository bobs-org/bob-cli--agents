# Chat History - ace-run (eh--plan)

- **TIMESTAMP:** 2026-11-16 12:00:39 EST
- **MODEL:** claude/opus
- **AGENT:** eh--plan

**Plan:** /home/bryan/.sase/plans/202611/selector_attention_dots.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/selector_attention_dots.md`

> # Attention dots for `w` (lanes over limit) and `b` (bank rows waiting)
> ## Goal
> The status bar's `[[ s w n b ]]` bracket selector (bob-navigation-hotkeys) already puts
> a small dot on the `s` letter while review commitments are due and another walk is
> selected. Extend the same language to two more letters:
> - **`w`**: a red dot whenever any PENDING, NEXT, or READY badge would be red. That is, a
>   lane's count is over its limit, exactly as the dash and daily `bob-plan` badges judge
>   it.
> - **`b`**: a dot whenever any bank row is unticked (waiting). This dot already exists
>   (amber, nav `api.walkMode` v4, ledger `walkerFooterPushBankAttention`), but a

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli We already show a little red dot next to the `s` in the Obsidian footer when
the GTD review walk has tasks in it. Can you now help me do something similar for the
`b` (unticked bank rows) and `w` (if any of the pending/next/ready limits are currently
exceeded--i.e. if any of the PENDING/NEXT/READY badges are red) characters in the
footer? I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful! 

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Opened the bob-plugins repo; now locating the footer code that paints the `s` review-walk dot.

Found the footer: it's the `[[ s w n b ]]` bracket-mode indicator in bob-navigation-hotkeys, which already has an "attention" channel. Reading how the `s` dot is fed.

Status: a `b` attention hook already exists in code (landed 11-14, keyed on "waiting" bank rows). Checking whether it's actually deployed and working, and how the CSS paints the dot.

Status: likely found a real bug — the footer's bank-change subscription is registered before `setupBankWalk()` runs, and setup replaces the listener set, wiping it. Verifying.

Status: reading the PENDING/NEXT/READY badge models so the `w` dot can reuse the exact same "red" test.

Status: reading the earlier walker-footers epic plan to understand why the dots were designed as they are, so the new `w` dot fits.

Status: design is taking shape. Checking which docs and memory notes describe the dots today so the plan keeps them truthful.

Fixing the frontmatter: adding title/goal and converting the memory decision to a `memory:` toggle.

Plan validates. Submitting it.

I've submitted a plan for the footer dots; nothing is implemented yet. It's sized as a single medium task, and it starts once you approve it in review.

**The `b` dot already exists but is unreliable.** An amber dot for unticked bank rows was added on 11-14. You probably haven't seen it because the vault has 0 unticked rows right now, and because of a startup ordering bug in bob-ledger-tools. The footer subscribes to bank changes before the bank index is set up, and the setup then replaces the listener list, so the subscription is lost. As a result, the dot misses startup and on-disk `bob bank import` updates until something unrelated, like a cursor move, repaints the footer. The plan fixes this and adds a regression test that subscribes in the same order the plugin loads.

**How the three dots will behave:**

| Letter | Lights while | Color | Tooltip |
|---|---|---|---|
| `s` | review commitments are due (unchanged) | color of the first due review group | `Review: 9 due · 5 commitments — PRE first…` |
| `w` | any PENDING/NEXT/READY count is over its limit | the same red as the badges | `Lanes over limit: WIP 12/10 · READY 104/100 — click to show` |
| `b` | at least one bank row is unticked | amber, matching the bank badge's "waiting" color | `Bank: 3 waiting · oldest Nov 14 — click to show` |

- **One rule for every dot:** it shows only while you're on a different walk, clears as soon as its condition clears, and never lights while data is still loading.
- **The `w` dot can't disagree with the badges:** it decides "over" with the same function that turns a badge red, so a count exactly at its limit doesn't light it. A test checks the dot against the real PENDING/NEXT/READY badge results on the same tasks.
- **The signal stays visible after you click `w`.** The dot hides once `w` is selected, so the `w` panel shows each over-limit lane as a red count like `WIP 12/10`. Today that lane drops out of the panel while you're walking it; with this change an over-limit lane always stays visible. As you release tasks with Alt+N, the red count ticks down and disappears once you're back within the limit.
- **It doesn't flag lanes just for having tasks.** The original footer design rejected a `w` dot that lit whenever lanes had tasks, because it would never go away. This one lights only when a lane is over its limit, a state the dashboard already shows in red.
- **Out of scope:** the TODAY badge and the per-note Ready limits don't trigger the `w` dot.

The plan also covers screenshot previews in light and dark (including a text-contrast check), an extended real-Obsidian test, docs, version bumps, and `bob plugins sync`. There's no Obsidian binary on this machine, so that real-Obsidian test will be reported as skipped unless the implementer runs on one that has it.

**Three decisions for you in review:**
- **`b` dot color:** stays amber by default. Amber already means "waiting" on the bank badge, which keeps red for "over limit".
- **`s` dot colors:** stay as they are by default. I found that they don't match the review footer's group colors: a PRE dot is red, but the PRE group it opens is cyan. Choosing "match" fixes that, but the morning PRE dot turns cyan.
- **Glossary update:** on by default. The walker-footer glossary entry names only the `s` and `b` dots, so it would read as if `w` never gets one.
