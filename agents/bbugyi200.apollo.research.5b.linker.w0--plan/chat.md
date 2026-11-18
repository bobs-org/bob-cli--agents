# Chat History - ace-run (research.5b.linker.w0--plan)

- **TIMESTAMP:** 2026-11-18 11:05:26 EST
- **MODEL:** claude/opus
- **AGENT:** research.5b.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/record_walk_ring.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/record_walk_ring.md`

> # Record walk: ‹ › links on every record, N of M painted live
> ## Context
> Bryan wants every record note to carry `<` / `>` links to the previous and next record
> in its album. The walk is alphabetical, cycles at both ends, and works with the `[n` /
> `]n` keymaps. A two-record album gives each record links that both point at the other.
> `N of M` (position and album size) renders near the links. The design brief is
> intuitive, reliable, and beautiful.
> Bryan accepted every recommendation in the consolidated research report. Read it before
> starting any phase. Its evidence appendix gives the line-level citations this plan
> relies on:

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to start automatically adding good `<` and `>` links to all record
notes which point to the previous/next record note in that album. Can you help me
implement this?

- These links should work well with the `[n` and `]n` keymaps.
- This walk should be alphabetical and should cycle around to the next record. For
  example, an album with only two record notes should result in each record containing
  `<` and `>` links that both point to the other record note.
- As a part of this change, we should also start rendering the `N of M` text (or
  something like that) somewhere close to these links where `N` is the current record
  note's index (i.e. position in the walk) and `M` is the total number of record notes
  in that album.
- Review the record_nav_ring.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.5b.linker

## Response

The research sidecar isn't cloned in this workspace yet, so I'll open it and then read the record-nav research note.

Reading the album index planner and sync code now; next the capture record writer and the period-note nav line it should mirror.

Reading the `n` links footer's view model to see where an `N/M` position can go.

Checking the live vault's record notes (read-only) to confirm what bodies look like today before deciding the exact line shape.

Glossary entries for Record Note and the `n` links footer would become incomplete once this ships, so I'm loading the memory-write rules before planning those updates.

Checking how the lane footer shows its `N/M` position, so the links footer can reuse the same slot rather than inventing one.

Back in bob-cli: checking how capture reports `album_files` across a bulk capture, since neighbour walk edits need the same final-overlay treatment.

I have enough to design. Pulling a recent epic plan from the plans sidecar to match house conventions before drafting.

I have what I need. Writing the epic plan now: eight phases across bob-cli and bob-plugins, with a shared contract section so the parallel phases agree on bytes, order, states, and JSON.

The plan validates. Before proposing, I'm spot-checking two claims it leans on: that `records update` can't change `title`, and that `docs/walks.md` describes the `n` family.

`docs/walks.md` covers walk *attention* and explicitly excludes `n`, so it's the wrong home for a record-walk sentence. Finding where `[n` / `]n` are documented instead.

The plan passes validation. Proposing it now.

I've submitted the plan for your review as an epic with eight phases. No code has changed in either repo; implementation starts once you approve it.

**What you'll see**
- **In the note:** bob writes one line as each record's first body line, for example `[[eat/pho_house|‹ Pho House]] · [[eat|↑ Eat]] · [[eat/ramen_ya|Ramen Ya ›]]`.
  - `[n` / `]n` follow it as-is, with no key changes.
  - The order is the same alphabetical order the album's `[!records]` index uses, and it wraps at both ends.
  - With two records, both links point at the other one. With one record, the line is just `↑ Eat`.
- **In Obsidian:** the raw line becomes a rail docked under the record sheet: `‹ Pho House   🍽️ Eat · 3 of 104   Ramen Ya ›`.
  - A thin line in the album's colour, with a dot, shows where you are in the album.
  - The first and last records show a faint `↺` on the arrow that wraps around.
  - In narrow panes the rail shrinks to `‹ 3/104 ›`. When your cursor enters the line, you see the raw Markdown again.
- **In the `n` links footer:** it reads `Links 3/104`.
- **The count is never written into the note.** It's worked out live, so adding a record rewrites 3 files instead of all 104 in eat. If the computed neighbours ever disagree with the written links, the count shows `⟳` instead of a wrong number.

**Where I went beyond the research report**
- **Creating a record touches only nearby records.** It writes the new record plus the neighbours whose line actually changes. Capturing into an album that doesn't have the lines yet still writes only 3 files.
- **Only `bob albums sync` repairs lines.** `bob records tidy` just learns to skip the line, and `records update` never touches it, because it can't change a record's title.
- **The rail shows whenever the line exists in the note.** It doesn't depend on bob reporting support for the feature; that check only decides whether the plugin asks for a repair.
- **`records check` stays quiet.** It reports missing or outdated lines once per album, not once per record.

**Phases**
- **bob-cli, in order:** a shared core first. Then three parallel phases:
  - `albums sync` repairs the lines and `albums list|check` report them;
  - `records show|check|tidy` learn about the line;
  - capture and `records new` update the neighbours in the same write.
- **bob-plugins:** a guard so `[n` / `]n` never create an empty record in an album folder when a link points at a deleted note (starts right away), then the count logic and footer, then the rail with a real-Obsidian test.
- **Wrap-up:** an end-to-end check in a temporary vault, plus a read-only dry run of `bob albums sync` against your real vault. No phase writes to your vault.
- **Backfill:** all 192 records get their lines in one commit on the first real sync after the release ships, from nightly or from the plugin's automatic sync in Obsidian.

**Decisions waiting for you**
1. **Footer text:** `Links 3/104` (default) or `Links · Eat 3/104`.
2. **Decision record "record walks store links, never counts":** defaults to yes, because the research recommends one. You turned down a similar record on an earlier plan, so flip this if you'd rather skip it.
3. **One added sentence on the Record Note glossary entry:** defaults to no, since nothing in that entry becomes wrong.

Left out on purpose: number-aware sorting (so "Part 2" comes before "Part 10"), jumping between status groups, and any change to Bob Mac Capture.
