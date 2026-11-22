# Chat History - ace-run (research.5x.linker.w0--plan)

- **TIMESTAMP:** 2026-11-22 17:33:10 EST
- **MODEL:** claude/opus
- **AGENT:** research.5x.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/true_case_drawers.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/true_case_drawers.md`

> # Plan: True-case drawers
> ## Context
> Bryan wants drawers to stop needing capitals, so a drawer can keep the real
> capitalization of its section name (`API Design`, `iOS / OAuth 2.0`, `C++ Notes`,
> `Café`). This is a stepping stone toward giving every project note a distinct, lossless
> task representation (`^task-to-project`): today promotion turns `API DESIGN` into
> `## Api Design` and reversal uppercases `## Future Work` and refuses `## C++ Notes`
> outright, so no round trip can be lossless.
> Read `research:202611/true_case_drawers/true_case_drawers.md` (with
> `sase artifact read`) before starting any phase. Bryan endorsed every requirement it

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to make it so drawers no longer need to be capitalized. Can you
help me implement this?

- You should make sure that this work does not conflict with the (wip) bob-cli-on epic
  bead.
- We will need some other way to mark these sub-bullets as special without marking the
  task in the same way (I think this rules out `#foo` tags, right?).
  - Think hard about the best way to do this.
  - Regardless of what we store on disk, we should make sure to render these drawer
    sub-bullets in a distinct (and easily recognizable) way.
- I think we will need to fix the capture syntax we use for drawers to support this
  change. We already support targeting generic H2 sections when capturing to notebooks,
  so that logic should be re-used if possible/desirable.
- Goals of this Change
  - This change will allow us to represent the true/intended capitalization of the
    section name in drawers.
  - This task is a stepping stone towards the larger goal of giving every project note a
    distinct, lossless task representation (i.e. a way to convert it to/from a task
    without any data loss).
- Review the true_case_drawers.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.5x.linker

## Response

Reading the true-case drawers research report from the research sidecar, then I'll survey the drawer code and the bob-cli-on epic.

Research read — it recommends bold-header drawers (`- **Title**`), a shared place resolver, quiet glyph rendering, and a gated dual-read cutover. Now checking the bob-cli-on epic's current state.

Epic status: `.11`, `.12`, `.15`, `.17` still in progress (`.11`/`.15` are child epics). Now surveying the drawer code in bob-cli.

Core recognizer read (`is_drawer_title`, resolver, catalog). Now looking at the capture-language drawer/section bullet code and the notebook section machinery.

Now reading the governing memory records (decisions + glossary) that this change touches.

Memory read. Now opening bob-plugins and bob-mac-capture to locate their drawer surfaces (predicate twins, promotion casing, `.uppercased()` sites).

Mapping the shared vector fixtures and the task-block layout (NOTES drawer) code next.

Mac preview lines are raw strings today; I'll plan an additive per-line `drawer` annotation from bob so the Mac never sniffs `**`. Checking bob's preview line model and docs layout.

I have the bob-cli surface mapped. Checking how the bob-cli-on plan structured its own reviewed vault migration (phase .16) so this plan can mirror a proven gating pattern.

Good pattern to mirror. Now checking the epic plan schema (phase frontmatter, external dependencies) before authoring.

No external-bead dependency field in the epic schema. Checking whether a cross-epic bead dependency is possible and how epic launch mode works, so the new epic can't start before bob-cli-on finishes.

The epic is nearly done (`.11.1.6`, `.12`, `.15.1.4–5`, `.17` remain). Reading the beads reference memory to confirm whether a phase may add a dependency edge on bob-cli-on.

`sase plan approve --wait bead=<id>` exists, so the approved epic can be held until bob-cli-on closes. Checking whether the `^prj` NOTES-home bug from the epic's notes already has a task bead.

Gates support a `next` successor, so the migration phase can verify its own approved run before closing. Checking bob-cli's justfile gates to cite exact commands in the plan.

I have the full picture. Two quick checks before writing: the existing error code for an empty drawer bullet (to reuse it), and the twin-copy check script name in bob-plugins.

Existing code `empty_drawer_bullet` will be reused, and bob-plugins has twin-copy and real-Obsidian e2e precedents for reqs to mirror. Writing the epic plan now.

The validator resolves both glossary strands to the same web note, so I'll merge them into one glossary memory decision.

Validation passes. A quick polish pass on one awkward phrase in the glyph callout, then revalidate.

The file was reformatted on disk (now 925 lines); skimming it to make sure that change didn't mangle the content.

Content is intact. Submitting the validated plan.

The proposal is staged. Finishing the turn through `/sase_final`.

I've written the true-case drawers plan as an 11-phase epic. It passed validation and is staged for your approval; nothing in the repos has changed yet.

**Approve it with a wait on bob-cli-on** (`sase plan approve <plan> --kind epic --wait bead=bob-cli-on`, or the same wait in the approval gate). That epic still has `.11.1.6`, `.12`, `.15.1.4–5` and `.17` open, and they edit the same promotion code, shared test vectors, Mac fixtures and Task Drawer glossary entry. So no phase starts until it closes, and the first phase checks again before touching anything.

**The design:**
- **Marker:** a drawer is a bullet whose whole text is bold, `- **Future Work**`, directly under a task. You're right that `#foo` tags are out: they can't hold spaces, they'd show up in the vault-wide tag pane, and they'd mark the task too. The title is stored exactly as typed. Identity still ignores case, so `Notes`, `NOTES` and `notes` are one drawer.
- **What isn't a drawer:** `- **Note:** …` and anything ending in `:` stays a note. `__Title__` is the escape for a bold note that isn't a drawer. Empty drawers are recognized, but capture never creates one.
- **Imported text:** calendar, Keep, Gmail, highlights and clipboard text that would look like a drawer gets written as `__…__` instead.
- **Capture:** drawers, project sections and notebook sections share one section-targeting resolver, reused from the notebook H2 logic. `- #future-work` stays as a shortcut, and accepting a menu row writes `- **Future Work**`.
- **Typing:** your `*` → `**|**` expansion fires only where a drawer can start. Enter at the end of the title steps out into a nested bullet, Backspace removes all four stars at once, and Undo gives back a plain `*`.
- **Rendering:** a small glyph replaces the bullet, drawn in the owning task's colour (the same ink requirements use), with a semibold title. The words are never uppercased. Folded drawers show a note count, empty ones are dashed, and drawers under closed tasks are muted. On the Mac the `**` is dimmed rather than hidden. With plugins off, it reads as a plain bold header.
- **Promotion and reversal:** `- **API Design**` ⇄ `## API Design` round-trips exactly. Headings that can't become drawers are refused with a reason instead of being dropped.

**Where I departed from the research:**
- **Readers before writers.** The research flips readers and writers in one release. But athena, apollo and the Mac update bob separately, so a host that updated first would write bold drawers that a lagging host misreads, adding a duplicate `NOTES`. A gate phase confirms every host and the deployed plugins read bold before anything writes it.
- **ALL-CAPS drafts are refused, not saved as notes.** The research says `- FUTURE WORK` with nested notes becomes a note with a warning. But while old ALL-CAPS drawers are still read, that "note" would land as a drawer, and in project-note capture it would silently become a task row. Capture refuses it until the final cleanup phase and suggests the right spelling. After that it's ordinary text.
- **Old spellings never seed new titles.** New titles never copy an all-caps spelling that only exists on old drawers.
- **Each old drawer is renamed or released.** In the migration, you give each old ALL-CAPS drawer a spelling or "release" it to become a plain note. Something like `DONE` then costs no edits.

**Your choices at approval:**
- **Glyph:** an open tray (my default) or a drawer front.
- **Two memory decisions, both on by default:** a new "Drawers Keep Their Real Names" decision record, plus updates to the Task Drawer and Project Note Capture glossary entries. They default on because this work makes their ALL-CAPS wording false. Turn them off and no memory is edited. The validator made me merge the two glossary entries into one decision.

The research suggested sending the `.12` promotion phase a coordination note now. I didn't add one, because waiting for the whole epic to close makes it unnecessary.
