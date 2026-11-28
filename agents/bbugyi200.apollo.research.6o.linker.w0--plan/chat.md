# Chat History - ace-run (research.6o.linker.w0--plan)

- **TIMESTAMP:** 2026-11-27 14:56:10 EST
- **MODEL:** claude/opus
- **AGENT:** research.6o.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/tree_note_link_walks.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/tree_note_link_walks.md`

> # Tree-note link walks
> ## Why
> Days, periods, and records already walk with `[n` / `]n` and group with `[N` / `]N`.
> Area, project, notebook, and prose notes do not. Their `parent:` tree is Bryan's main
> way of organizing them, but `]n` there says `No next link found`. This epic makes the
> `n` family work on those four note types. It also makes the link-walk rail the floor of
> every Property Card, below the whole cabinet stack.
> The research report `research:202611/tree_note_link_walks/tree_note_link_walks.md` is
> the evidence base (read it with `sase artifact read`). Bryan accepted all of its
> recommended requirements. Its sase memory edits are the exception: only the reviewer

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to add support to area notes, project notes, notebooks, and prose
notes for the link walks (triggered via the `]n` keymap). Can you help me implement
this?

- We should implement this work in parallel (think hard about the best way to do this
  and whether or not coordination is even needed) with the in-progress bob-cli-qq epic
  bead.
- We should render a nice link walk widget at the bottom of the property card like we do
  for other files that support the link walk. As a part of this change we should make
  sure that the link walk widget is always shown at the very bottom of the property card
  (below all cabinets).
- For each of these new supported note types, the walk should only include notes of the
  same type that share the same parent note.
- We should group the members of this walk by their parent.
- As a part of this change we should add an excellent new glossary term for "link walk".
- For example, assume we are in the bar.md project note, which has the foo.md project
  note as its parent which, in turn, has the pig.md area note as its parent. The `]n`
  keymap would then jump to the baz.md file, assuming that is the next (alphabetically)
  project note that has the foo.md project note as its parent.
- I would like to support the `]N` keymap as well, but I'm not sure how the grouping
  would work. Think hard about this. If you can think of an intuitive way to group this
  walk such that the `]N` keymap works, then we should implement it.
- Review the tree_note_link_walks.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.6o.linker

## Response

I'm reading the research report now, then I'll go through the existing link-walk code and the in-progress bob-cli-qq epic.

I've read the research and the qq epic status; now opening bob-plugins to verify the link-walk code the plan will touch.

Now the core resolver and nav-group dispatch.

Reading how record and day/period cards mount their rails next, and where the cabinet stack lands, so I can design the "rail is always last" rule.

Checking whether the qq phases have notes or dependencies the plan should key off.

Tracing where the foot and cabinet stack get appended, so the plan can name the exact insertion point.

I'm still mapping the plugin code (project open/closed detection, the step-link matcher, the footer) before I write the plan.

I have enough of the code picture. Loading the memory-write skill, since the plan will add a glossary strand and propose other memory edits.

I've worked out the design. Now checking the epic plan schema, in particular whether a phase can depend on an outside bead like `bob-cli-qq.10.5`.

I've settled the design and phase graph. A few last facts before writing: the test-export fragments and how new test scripts get wired into `npm test`.

Last check before writing: the decision-record file format, so the plan's memory step names the right shape.

I've confirmed everything the plan relies on. Writing the epic plan now.

Two validation issues: the new strand selector doesn't resolve, and two decisions resolve to the same note. Switching the strand selectors to explicit note paths.

The file was reformatted on disk since I wrote it, so one replacement missed. Reading the current memory section.

The plan passes validation. Submitting it.

I've written the plan for tree-note link walks as a six-phase epic and submitted it; it's waiting for your approval. Nothing has been built yet. All the code goes in bob-plugins; bob-cli only gets the glossary/memory edits, so nothing rides the release train or touches Mac Capture.

**How the walk works**
- **`]n` / `[n`** step through notes of the same type with the same parent, and wrap around. They never leave that parent. In your example, `bar` → `]n` → `baz`.
- **Order** within a group matches the parent's cabinet: stem for areas and projects, title for notebooks and prose.
- **Projects** walk open with open and closed with closed. Most projects under `sase` are closed, so one mixed list would mostly land on dead work.
- **`]N` / `[N`:** the groups are the parents, so `]N` jumps to the first child of the next parent. "Next" means reading down the full outline of notes, each parent before its children. From `bar`, `]N` goes to `goo`'s first child (`alpha`), `[N` goes to `foo`, and from `foo`, `]N` drops into `foo`'s own children. I chose this over "only parents that share a grandparent" because that version leaves `]N` dead on 10 of your 18 areas. This one works on every note once a second parent with children of that type exists, and it tours every group like `]S`, `]W` and `]B` do.
- **Nothing is written to the vault.** The walk is worked out from `type:` and `parent:` when you press a key. A link you write yourself on a line holding only links still overrides it.

**The widget**
- It reuses the existing rail design: `‹ prev · ↑ parent · next ›` on top, with a row below that names the neighbouring parents and shows where you are among your siblings.
- It's always the card's last element, below every cabinet. Record and day/period cards move to the same spot, which also fixes the record card showing its rail above the cabinets in one view and below them in the other.
- No rail appears when there's nothing to walk; the keys show a short message instead.

**Running beside bob-cli-qq**
- The first three phases (the walk logic, a fix so links inside backticks stop counting, the widget code) share no files with qq and start right away. All eight keys work on all four note types after the first phase.
- Putting the widget on the cards waits until qq.10.5 closes, because it edits the same two files that phase is rewriting.
- The docs and glossary phase waits until qq.10.6 closes, because that phase rewrites the same pages.
- The waits are bead dependencies plus a check at the start of each of those two phases; no other coordination is needed.

**Two decisions for you**
- **Glossary** (default yes): add the new link-walk term (the full text is in the plan) and correct the walker-footer entry, which would otherwise say only days, periods and records have derived stops. These are one decision because the plan checker counts all glossary entries as a single note.
- **Decision record** (default no): add an entry recording this walk design. It's off because you didn't ask for it.

I dropped one extra memory change: adding a "rail sits at the bottom" sentence to six card entries. The link-walk term already says it.

The only open validation warning is that the new link-walk term doesn't exist yet. It clears once the docs phase creates it.
