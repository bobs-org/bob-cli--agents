# Chat History - ace-run (1gz--plan)

- **TIMESTAMP:** 2026-11-27 07:40:02 EST
- **MODEL:** claude/opus
- **AGENT:** 1gz--plan

**Plan:** /home/bryan/.sase/plans/202611/bank_note_completion.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/bank_note_completion.md`

> # Plan: Past-note completion in the Bank Category card
> ## Why
> Task `^cmpl-past-bank-notes` ("Add completion for past bank notes!") carries a
> screenshot of the Bank Category card's note stage on a `$41.94 Amazon Reta* Ue4v4` row
> with "Ask Kelly?" typed into the field ("Adds a note · stays on this row"). The vault
> shows why: `bank/2026-11.md` has `— Ask Kelly?` typed by hand on four different
> `Amazon Reta* …` rows. Bank notes repeat by merchant: "ask Kelly", "for Abby",
> "reimbursable". Today every repeat is retyped.
> ## What exists (bob-plugins, `plugins/bob-ledger-tools/src/`)
> - `246a-plugin-bank-note-write.js`: the pure note rules. `bankNoteNormalize` applies the

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me complete the work associated with the ^cmpl-past-bank-notes
task in the ~/bob/bob.md file? I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm looking through the Bank Category card code in bob-plugins and bob-cli to understand how notes on bank rows work today.

I've read the note-stage code. Now checking the note-stage CSS, its tests and docs, and how bob normalizes merchant names, so the suggestions can match "Amazon Reta* Ue4v4" against other Amazon rows.

Now checking whether the plugin already has a merchant-name normalizer (so "Amazon Reta* Ue4v4" and "Amazon Reta* Pd4tc" count as the same merchant).

Next I'm reading the decision records that govern card keys (Tab/Ctrl+N/P precedent and the Esc/q rule) so the plan cites them correctly.

Design is mostly settled. Checking how the bank E2E suite runs and the test scripts, so the plan's verification steps are concrete.

Design is settled; I'm now writing the plan. One quick check first: whether task beads live as repo files, since I want to file the Amazon payee-cleaning bug separately.

Writing the plan now. All changes land in bob-plugins (pure model, card UI, index hook, CSS, tests, docs); bob-cli's code is untouched.

Plan validates cleanly. Rereading it once before proposing.

The plan is staged. Before finishing I'll file the bob import-cleaning bug I found (Amazon's spaced `RETA* CODE` order code is kept) as a separate task.

Creating the bug task now (no duplicate found; the related bead bob-cli-lb is closed and covered a different cleaning gap).

Now finishing the turn through the final declaration.

I've written the plan for `^cmpl-past-bank-notes` and submitted it for your review. It passes validation with no warnings. Nothing has been built yet. The coding agent starts once you approve.

**What I took the task to mean:** autocomplete in the Category card's note field (the box in your screenshot). Your November bank note has `— Ask Kelly?` typed by hand on four different Amazon rows, which is the repetition this removes.

**The experience:** you note one Amazon row. On the next one, Space opens the field with "Ask Kelly?" already showing as faint text inside it. Tab fills it in, Enter saves it. So Space, Tab, Enter instead of retyping.

- **Which notes it offers:** on an empty field, only notes you've written for this merchant. Notes from other merchants appear once you've typed two letters.
- **How it chooses the top one:** notes you use often and recently rank first. A note you used four times beats a newer one-off like "Binoculars for Abby".
- **Amazon rows:** the order codes differ on every row ("Amazon Reta* Ue4v4", "…Pd4tc"), so the plan strips them and treats all of them as one merchant.
- **The list:** at most 4 rows, shown under the field and lined up with your text. Tab fills in the marked row, Ctrl+N/P or ↓/↑ put another one in the field, and clicking a row fills it.
- **Enter only ever saves what's in the field.** The faint text is just a preview of what Tab would fill in. Esc, Ctrl+[ and q behave exactly as they do now.

**Reliability:**
- **Where the suggestions come from:** the notes already on your bank rows across every month, read live. That includes a note you saved seconds ago that isn't on disk yet. Nothing is stored separately, so editing a note off past rows removes it from the suggestions.
- **Safety:** a past note is only offered if it can be written back exactly as shown. Notes with links or fields never appear.

**Choices I made for you (reasons are in the plan):**
- It doesn't ask bob for suggestions. That would mean running bob on every keystroke, and bob wouldn't see the note you just typed until it's saved.
- It doesn't suggest notes when you type `— ` directly in the month note, because the popup would take over Enter, which you use there to start the next row.
- There's no way to hide a suggestion. To get rid of one, edit the note on its rows.

**One question for you at approval:** whether to also add a short design-decision record for this feature to the decisions memory. It defaults to no because you didn't ask for one.

**One bug I filed separately (bob-cli-qx):** bob's import keeps the spaced Amazon order code (`AMAZON RETA* BV5NH`), so every Amazon purchase gets its own payee and bob can never carry a category or cleaned-up name from one Amazon row to the next. The new merchant matching works around it either way.

All the changes go in bob-plugins: a new suggestion layer, small hooks into the existing note field, styling, tests (including the real-Obsidian test run with a screenshot), the plugin docs, and then `bob plugins sync`.
