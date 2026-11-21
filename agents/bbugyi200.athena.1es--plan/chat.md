# Chat History - ace-run (1es--plan)

- **TIMESTAMP:** 2026-11-21 07:41:30 EST
- **MODEL:** claude/opus
- **AGENT:** 1es--plan

**Plan:** /home/bryan/.sase/plans/202611/bracket_n_group_jumps.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/bracket_n_group_jumps.md`

> # `[N` / `]N` group jumps for days, periods, records, and any note
> ## Why this epic exists
> Bryan asked for `[N` / `]N` keymaps once the property-card title block (`bob-cli-o6`) is
> done: dailies jump to the first day of the previous / next week, period notes jump to
> the first same-level note of the previous / next higher period (never on year notes),
> grouped albums walk one group at a time, `[{` / `]}` repeat the jump, the stops render
> at the bottom of property cards and in the walker footer, and a stop whose note does not
> exist yet is visibly, beautifully different. Bryan also asked for it to be configurable
> in any note and asked the planner to lead the design.
> Bryan accepted every requirement the consolidated research recommends, except memory

*See full plan file for details.*

## Prompt

%auto
#gh:gh_bobs-org__bob-cli Once I've completed the work described by the property_card_title_block.md file
in the research sidecar repo, I want to add the new `[N` and `]N` keymaps, which should
be immediately useful for daily files, period notes, and record notes. Can you help me
implement this?

- These should be configurable in any Obsidian note somehow. I was thinking we could
  look for links that start with `<<` or `>>`, respectively, but that's just my first
  thought. Think hard about the best way to implement this.
- For daily files, the << link should point to the first day of the previous week and
  the >> link should point to the first day of the next week.
- For period notes, the << link should point to the first period note of the same level
  (ex: weekly period note if inside a weekly period note currently) in the previous
  period of a level one higher. The >> link should point to the first period note of the
  same level in the next period of a level one higher.
  - For example, this means the ~/bob/2026/2026-W30.md file should have a << link that
    points to the ~/bob/2026/2026-W14.md file and a >> link that points to the
    ~/bob/2026/2026-W40.md file.
  - This also means that yearly period notes should not support this functionality (i.e.
    should not have << or >> links).
  - Make sure that we make it clear (in a visually appealing way) when one of these
    files does not yet exist somehow.
- Album notes should be able to configure a field that its record notes should be
  grouped by in order to support these new keymaps.
  - The `[n` and `]n` keymaps should then start walking through all record notes with
    that field set to the same value in sequence before moving on to the prev/next
    record group (i.e. group of record notes with this field all set to the same value).
  - The `[N` and `]N` keymaps should jump to the first record note of the previous/next,
    respectively, record group.
  - As our first use-cases, I would like to configure the ~/bob/sase_blog_zettel.md
    album note to start using its `section` field to group this walk. Think hard about
    whether or not the other albums in my vault would benefit from configuring a
    grouping field as well (configure the appropriate field for these if so).
- Make sure that the `[{` and `]}` keymaps work properly with these keymaps.
- We should make sure these links render nicely at the bottom of property cards (see the
  bob-cli-nh epic bead for context).
- We should also make sure to add support for appropriate hints to the walker footer for
  these new links.
- Review the bracket_n_group_jumps.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm locating the two research reports in the research sidecar before I design the plan.

I've read the group-jumps research; now reading the prerequisite title-block report and the `bob-cli-nh` epic.

Now checking the bead state: `bob-cli-nh` and any title-block epic this work must follow.

I've read both research reports and the in-flight title-block epic (`bob-cli-o6`). Now surveying the live code in bob-plugins and bob-cli to ground the plan.

I'm reading the plugin code that the new keys hook into, and handing the bob-cli album-walk and period survey to a helper so both run in parallel.

Still surveying: checking the calendar subject model and how `]n` creates missing dailies today.

Now checking the record walk rail and the walker-footer slot renderer, then the nav-hotkeys command registration.

Checking how the walker footer paints link arms and hint slots.

Surveying the live albums so I can judge which ones should group their walks.

Still surveying — confirming how the vault vimrc maps `[n`/`]n` and who owns that file.

I have the code picture. Next: checking for existing beads on this feature, and reading the glossary strands this work would make false.

Glossary check done: the Record Note's "title order" claim and the Walker Footer's links-footer clause become misleading, so those get memory decisions. Now pulling the epic plan schema.

I've mapped the code surfaces. Checking one documented contract that affects note creation from the repeat keys.

Design is settled in my head; verifying the calendar worked examples with Python before writing them into the plan.

Calendar facts confirmed (2026 has 53 ISO weeks, W01's Monday is 2025-12-29, 2027 is adopted, 2025 has no week notes). Writing the epic plan now.

Both glossary strands resolve to one memory note, so I'm merging them into a single `memory_glossary` decision.

Validation passes. The file changed on disk after validation, so I'm checking what the validator rewrote before proposing.

Content is intact. One fix: I used "He" for Bryan in the plan; switching to a pronoun-free phrasing.

Validation passes. Proposing the plan now.

The proposal is staged. Finishing the turn through `/sase_final`.

I've written the plan as an 8-phase epic and submitted it. It validated cleanly and is staged for your approval. Nothing starts until you approve it, and I changed no code.

## The design

**The rule:** lowercase keys step one note; `[N` / `]N` open the first note of the previous / next group.

| Note | `[N` / `]N` open |
|---|---|
| Daily note | Monday of the previous / next week |
| Week | first week of the previous / next quarter (`2026-W30` → `W14` / `W40`) |
| Quarter | Q1 of the previous / next year |
| Year, `all_time` | no jump; a notice explains why |
| Record in a grouped album | first record of the previous / next group, wrapping around with `↺` |
| Any other note | its `«` / `»` links |

Your `<<` / `>>` idea survives as typing shortcuts for `«` / `»`. On any note, those links work only on a line that holds nothing but links, so a clipped article's `Read more »` can't take over the key. That line can also override the automatic answer on daily and period notes. The current `[n` matcher would treat `<< X` as a "previous" link, so I tighten it: doubled arrows never take a single step.

**How the stops are worked out:** on daily notes, period notes and records the stops are computed from the note itself and never written into files. Most of your ~1,196 daily notes have no nav line, so this works everywhere without a migration. As a bonus, `[n` / `]n` start working on the ~1,020 old daily notes where they do nothing today.

**Albums:** a new `walk_by: <choices field>` key. bob rewrites the existing walk lines group by group, so `[n` / `]n` finish one group before entering the next with no new key logic.
- `sase_blog_zettel` walks by `section`.
- `subscriptions` and `eat` walk by `status`.
- `tv` stays unset, because all 23 records are `to_watch`.
- `eat.location` isn't eligible: grouping by a free-text field is left for a later version.

**Missing notes:** a dashed arm with `+` means "not created yet" and creates the note on an explicit press. A dotted, faint arm marked "not in vault" means it will never be created from here.
- Navigation won't create past period notes in a year with no week notes. I also added this guard to the period-creation path itself, because a `[N` from `2026-W01` would otherwise create notes for 2025 and flood `bob periods` with problems. The guard also stops `[n` from doing that today.
- `[{` / `]}` never create notes, so holding the key can't create a chain of notes.

**Property cards:** the rail gains a quieter second row such as `« Q3 · W27   ▮▮■▯▯  week 8 of 14   2027-Q1 · W01 »`. Missing targets in the existing rail row get the same dashed / dotted look. **Walker footer:** `« ‹ · › »` arms plus hints like `]} next week`, and `]n enters W48` at the end of a group.

## Phases
1. **Run in parallel first:**
   - Key grammar and commands in Navigation Hotkeys.
   - The calendar groups in Ledger Tools.
   - `walk_by` in bob.
2. **Then:** grouped record walks in the plugin.
3. **Then, in parallel:** the card group row and the footer.
4. **Then:** turning on `walk_by` for the albums plus a real-Obsidian test.
5. **Last:** glossary updates, only if you accept them.

Phases that touch the cards or footer stop and wait if the title-block epic (`bob-cli-o6`) is still open. Albums are only switched over once every host (athena, apollo, the Mac) runs a bob that understands `walk_by`. Otherwise an older bob would put the walks back in alphabetical order.

## Decisions for you when approving
- **`daily_create`** (default yes): `]N` creates a missing daily note, the same way `]n` does.
- **`walk_more_albums`** (default no): also group `movies` and `podcasts` by status.
- **`memory_glossary`** (default yes): fix the Record Note and Walker Footer glossary entries, which this work would make wrong.
- **`memory_decision_group_stops`** (default no): add a decision record for this design.
