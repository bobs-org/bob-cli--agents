# Chat History - ace-run (em--plan)

- **TIMESTAMP:** 2026-11-17 15:12:57 EST
- **MODEL:** claude/opus
- **AGENT:** em--plan

**Plan:** /home/bryan/.sase/plans/202611/record_notes_on_demand.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/record_notes_on_demand.md`

> # Write `## Notes` in record notes only when note bullets exist
> ## Goal
> Today every record note bob writes carries a `## Notes` heading, even when it has no
> note bullets. In the live vault, 105 of 186 record notes have an empty `## Notes`
> section: 42 end with it, and 63 have it directly before a legacy `## Source` block.
> After this change:
> 1. **Create.** `bob records new` and capture `@album/` write `## Notes` only when the
>    new record has at least one ordinary note bullet.
> 2. **Update.** `bob records update -n` and capture `@album/<stem>` create `## Notes` on
>    demand when the first ordinary bullet arrives. It goes in its canonical place, right

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me start only adding the "Notes" section to record notes when note
bullets exist?

- This means that we will need to support conditionally creating this "Notes" section
  when we capture record note changes / new record notes.
- Ideally (if it's not too hard) we should also remove any empty "Notes" sections in
  existing record notes periodically somehow.
- Make sure that your work does not conflict with the bob-cli-ms epic bead (try to
  complete this work in parallel if possible).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Reading the bob-cli-ms epic plan to see which files its phases touch, so this work can run alongside it without conflicts.

Mapping where record notes are written (render, update, capture) and where `## Notes` is assumed.

Checking the remaining record writers (`records init`, album migrations) and readers that rely on `## Notes`.

Now looking at what periodic maintenance already runs (albums sync, cron jobs) to hook the empty-section cleanup into.

Checking how bob-plugins triggers `bob albums sync`, since an auto-triggered cleanup could strip a heading Bryan is mid-typing.

Our change looks bob-cli-only (plugins don't depend on `## Notes`). Checking the in-progress epic phase 2 footprint in bob-cli to avoid file overlap.

Surveying the live vault (read-only) to size the cleanup: how many record notes have an empty `## Notes` section and what shapes occur.

Plugins and Mac Capture don't depend on the heading; the change is bob-cli only. Checking remaining docs and the update-path tests that pin current behavior.

Checking for other open beads that might overlap (record rendering, nightly, Notes).

I have enough context. Writing the plan now: one tale, bob-cli only, avoiding the files the in-flight epic phase is editing wherever possible.

The plan passes validation. Submitting it with `sase plan propose`.

I've written the plan for adding the "Notes" section only when there are note bullets. It passed validation and is now staged for your review. It's a single-agent plan (a "tale", sized medium), and no files have been changed yet.

**What the plan does (bob-cli only):**

1. **New records.** `bob records new` and capture `@album/` will write `## Notes` only when the record has at least one note bullet. A record with no notes ends at its title heading; a record with only a named section gets just that section.
2. **Adding notes to an existing record.** `bob records update -n` and capture `@album/<stem>` create `## Notes` the first time a bullet arrives. It goes right under the title and before any other `##` section. Today it gets added at the end of the file, so it would have landed after the `## Source` blocks. Updates that only change fields never touch the note body.
3. **Cleaning up existing records.** A new `bob records tidy [TYPE] [-b] [-d] [-f human|json]` removes empty `## Notes` sections. `-d` only shows the changes. A real run takes the vault lock and makes one commit, `records: tidy (N notes)`. A section counts as empty only if it holds nothing but blank lines; a subheading or comment keeps it.
4. **Periodic cleanup.** `bob nightly` runs the tidy as a new step after albums and before the final vault-sync. In your vault that's 105 of 186 records: 42 end with the empty section and 63 have it right above `## Source`.

I kept the cleanup out of `bob albums sync`. The Obsidian plugin runs albums sync automatically after property edits, so it could rewrite a record while you're working in it, or collide with the Record Card's saves.

**Avoiding conflicts with bob-cli-ms:** that epic's only remaining bob-cli phase is the `update -i` envelope work (bob-cli-ms.2), and the rest is bob-plugins work.
- The new code goes in new files (`records/tidy.rs`), and the plan avoids editing the files that phase is changing (`records/cli.rs`, `execute_update`, `plan.rs`).
- Field-only updates still leave everything outside the frontmatter untouched, which the epic's design depends on.
- The coder will rebase onto the latest master before the full `just check` gate and adjust any newly landed tests that expect an empty `## Notes`.
- The plugins and Mac Capture don't depend on the heading, so neither needs changes.

**One decision for you (`first_cleanup`):** by default, the coder only previews the tidy against your live vault, and the next nightly run does the real cleanup. Pick `now` if you'd rather the coder run it once right after landing. Nightly runs on athena, so with the default the cleanup only starts once athena's `bob` includes this change.
