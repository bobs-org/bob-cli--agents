# Chat History - ace-run (research.4n.linker.w0--plan)

- **TIMESTAMP:** 2026-11-14 12:21:32 EST
- **MODEL:** claude/opus
- **AGENT:** research.4n.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/bank_walk_family_b.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/bank_walk_family_b.md`

> # Plan: Bank walk family `b` — `]b` / `[b` / `]B` / `[B` with a bank walker-footer panel
> ## Why
> Bank rows are the one Bob-maintained content family with no keyboard walk. They never
> carry `#task`, so every task walk skips them; the Category card files waiting rows but
> "never opens another file"; the badge and queue card are mouse surfaces. Meanwhile the
> bracket grammar — lowercase steps items, uppercase jumps groups, `]]` / `[[` and `]}` /
> `[{` repeat, one selector, one walker-footer host — is already in Bryan's fingers, and
> `[b`, `]b`, `[B`, `]B` are unmapped in the vault vimrc.
> This epic adds **`b` as the fourth bracket family**. The design comes from research
> report `research:202611/bank_walk_family_b/bank_walk_family_b.md` (five independent

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to add the new `[b`, `]b`, `[B`, and `]B` keymaps to Obsidian. Can
you help me implement this?

- These keymaps should be used to traverse the bank transactions that have been saved to
  Obsidian (via the `bob bank import` command).
- These keymaps should have their own walker footer associated with them.
- The `[b` and `]b` keymaps should allow me to jump to the next/previous bank
  transaction, respectively. When there are bank transactions that need review, these
  keymaps should only traverse these bank rows. Otherwise these keymaps should traverse
  all bank rows.
- The `[B` and `]B` keymaps should allow me to navigate to the first bank row in the
  previous/next day, respectively.
- Review the bank_walk_family_b.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.4n.linker

## Response

Reading the bank-walk research report now, then I'll survey the existing walker keymaps and footers in bob-plugins.

Surveying the existing walker code (bracket repeat, mode selector, walker-footer host, bank recognizer) to ground the plan in real touchpoints.

Still mapping touchpoints: now reading the command registrations and the ledger-side walker-footer host.

Reading the footer painter and the bank recognizer (`241i`) next, so the plan names the right seams.

Checking bob-cli's bank grammar so "waiting" in the walk matches exactly what `bob bank list` counts.

Reading the glossary terms the plan will touch (walker footer, bank row/month note, badge) through the audited memory reader.

Checking the plugin docs and API reference that the new family will need to extend, then the existing tests and preview tooling.

Still surveying — now the bank badge/card "open row" path (the landing the walk should share) and the bank marks' hue.

Looking at the prior walker-footers epic plan as a structural precedent, plus the footer CSS.

Nearly done exploring — confirming the editor-overlay precedent, then I'll write the plan.

Exploration done. Writing a skeleton first to get the epic schema from the validator.

Writing the epic plan now.

Validation passes. One refinement before proposing: since `keys` and `footer` can run in parallel, the four-letter integrated preview bar belongs in `handoff` (after both land), not `footer`.

Still valid. Proposing the plan.

Staged. Finishing the turn through the final declaration.

I've written a five-phase epic plan for the bank walk, and it's staged for your review. It passed validation; no code, vault or memory files have changed yet.

**The keys:**
- **Direction:** `]b` and `]B` go *next*, and `[b` and `[B` go *previous*. Your message had `[b` as next; the research flagged that as a slip, since every other bracket family uses `]` for forward.
- **`]b` / `[b`:** step through rows waiting for review (`[ ]`) across all bank months while any exist, and through every bank row once none do.
- **`]B` / `[B`:** jump to the first row of the next or previous day in that same set. They wrap at the ends with a visible `↻`.
- **Repeats:** `]]` / `[[` and `]}` / `[{` repeat them while `b` is the active walk, and counts like `3]b` work.

**Where a key lands:**
- **In a bank month note,** it steps from your cursor.
- **On a daily note** whose date has bank rows, it enters that day.
- **Otherwise** it resumes from where your last walk landed today. With no earlier landing, it goes to the oldest waiting row, or to the newest day when nothing waits.
- The cursor lands at the payee, the same spot the Category card uses, and each jump records one `<C-o>` entry.
- The walk never writes to the vault and never runs `bob`. If a row moved under it, it re-plans once and then says `Bank rows changed — try again` rather than guessing.

**The footer:** a fourth panel on the existing walker footer, and the status-bar selector becomes `[[ s w n b ]]`. It always starts with the scope: amber `WAITING 3/9` or calm `ALL 38/146`.
- It shows clickable previous/next-day buttons, computed by the same code the keys use, so they can't disagree.
- Money appears only for the row your cursor is on.
- It shows `✓ balanced` only when fresh `bob` data says so.
- An amber dot appears on the `b` letter while rows wait and another walk is selected.

**Phases:**
1. **`index`:** the shared bank-row index and walk logic, including unsaved edits, checked against `bob bank list` output.
2. **`keys`:** the commands, the landing message, and the four `obsidian_vimrc.md` lines.
3. **`footer`:** the bank panel and the waiting dot. It can run in parallel with `keys`.
4. **`handoff`:** the Category card and Bank Badge feed the walk, plus a real-Obsidian end-to-end test.
5. **`ship`:** docs, deploy, and checking it on the Mac. It also adds a mention of `]b` to the "Next:" line that `bob bank import` prints, which is a bob-cli change.

**Memory decisions for you to answer when you approve:**
- **Walker-footer glossary update:** on by default, because this work makes its "`s` / `w` / `n`" member list wrong.
- **New decision record** for the bank walk: off by default, since you didn't ask for one.

I dropped the planned one-line addition to the bank-row glossary entry. The plan validator counts both glossary entries as one note, and I didn't want to slip an unrequested addition in alongside the fix. The updated walker-footer entry will link to bank-row instead.
