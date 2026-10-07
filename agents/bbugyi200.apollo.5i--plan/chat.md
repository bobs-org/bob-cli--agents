# Chat History - ace-run (5i--plan)

- **TIMESTAMP:** 2026-10-07 09:55:29 EDT
- **MODEL:** claude/opus
- **AGENT:** 5i--plan

**Plan:** /home/bryan/.sase/plans/202610/review_footer_short_labels_tickler.md


## Prompt

#gh:gh_bobs-org__bob-cli Can you help me change the names shown for some of the morning GTD review
groups at the bottom of Obsidian?

- The main goal of this change is to shorten the length of this morning GTD review
  footer by reducing the size of some of the review group names shown within it.
- Let's start showing `REFS` instead of `REFERENCES`.
- Let's start showing `WIP` instead of `PENDING` (making "WIP" an official alias for the
  "Pending" task status).
- Let's rename "Returned" tasks to "Tickler" tasks. Make sure to update all references
  in code and in my Obsidian vault (in the rotten.md file in my Obsidian vault, for
  example). Let's show this as `TICKS` at the bottom of Obsidian though (in the morning
  GTD review footer).
- Let's add a new glossary term for "morning GTD review footer" (aka "review footer").
  Make sure this definition is excellent but concise. Think hard about what the "review
  footer" really is and what it is used for.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %auto

## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202610/review_footer_short_labels_tickler.md`

> # Shorter review footer labels (WIP / TICKS / REFS) and Returned → Tickler
> ## Goal
> Shorten the morning GTD review footer, the bob-ledger-tools item in Obsidian's bottom
> status bar, by giving it compact group labels:
> - `WIP` instead of `PENDING`. WIP becomes an official alias of the Pending (`[/]`, In
>   Progress) task status.
> - `TICKS` instead of `RETURNED`.
> - `REFS` instead of `REFERENCES`.
> Also rename the "Returned" walk tier to **Tickler** everywhere: bob-cli, bob-plugins,
> the Bob vault, and SASE memory. Then add a glossary term for the review footer.

*See full plan file for details.*

