# Chat History - ace-run (research.4b.linker.w0--plan)

- **TIMESTAMP:** 2026-11-12 06:58:43 EST
- **MODEL:** claude/claude-fable-5
- **AGENT:** research.4b.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/album_schema_render_and_edit.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/album_schema_render_and_edit.md`

> # Album record schema: render in the header, edit through bob
> ## Scope and completion owner
> The `record` frontmatter mapping on album notes (`eat.md`, `podcasts.md`, `tv.md`,
> `movies.md`) renders in Obsidian's Properties panel as a truncated JSON string behind an
> unknown-type `?` icon, and editing it means hand-editing nested YAML. Obsidian's
> Properties engine supports only flat scalars and string lists, exposes no public
> property-widget API, and its unknown-type widget has corrupted nested mappings before
> (bob ships `recover_album_noun` in `src/native/records/schema.rs` precisely because a
> stringified record has leaked). The fix is therefore not a prettier Properties row: the
> schema renders as bob-owned album-header chrome, and every common edit goes through a

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to make the `record` frontmatter field render properly in
Obsidian. Can you help me implement this?

- It also needs to be very easy for the user to modify this field somehow (think hard
  about what the best UX for this looks like).
- See the ~/tmp/screenshots/20261112_054646.png screenshot for an example of what this
  looks like now.
- See the bob-cli-k3 epic bead for context on the `record` frontmatter field.
- Review the album_record_schema_ux.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:claude-fable-5 %w:research.4b.linker

## Response

I'll start by gathering context: the screenshot, the epic bead, and the research file. First, let me look at the screenshot and load the required memory notes.

Now let me read the epic bead and the research artifact.

The research sidecar isn't checked out here. Let me open it with the `/sase_repo` skill.

The research references the in-flight child epic `bob-cli-k3.7.1` (phases album-data through album-navigation). Let me check its current phase statuses to know where slice A fits.

Now let me ground the plan in the actual code — the albums module, the report JSON, the records update precedent, and what's landed in bob-plugins.

The schema is clear. Now I'll author the full epic plan.

The plan validates cleanly with zero warnings on the first full pass. Now I'll propose it.

Staged. Now the coordination note on the in-flight header phase, as the research recommends and my plan references.

All work is complete. Now I'll finish through `/sase_final` as required.

The plan is proposed and staged, and no final declaration was required (the host will adopt the staged plan handoff when this turn ends).

## What I did

**The problem** (from your screenshot): on `eat.md`, the `record` frontmatter mapping renders in Obsidian's Properties panel as a truncated orange JSON string behind an unknown-type `?` icon — and worse, that native row is a known corruption hazard, since Obsidian's unknown-type widget has written nested mappings back as strings before (that's why `recover_album_noun` exists in `schema.rs`).

**Context gathered**: I read the `bob-cli-k3` epic bead, the full consolidated research report (plus the in-flight `plan:202611/album_plugin_ui.md` child epic spec), and verified the key code claims myself against bob-cli master — the lossy `AlbumField::to_json`, the missing `dated_notes`/`legacy`/fingerprint in list JSON, the `bob records update` span-editing precedent, and the serde-style unindented `legacy:` sequences that break the "Properties re-serialize is a no-op" claim.

**The plan** — `sase_plan_album_schema_render_and_edit.md`, epic tier, validated with zero warnings and proposed (**Staged**). It follows the research's design, which you endorsed: hide the native row on album notes only, render the schema as a collapsed-by-default header summary line that expands into a chip view, and edit through a keyboard-first Schema Card whose every write goes through a new `bob albums update` writer (dry-run consequence lines, fingerprint guard, Rust validation, span-preserving Obsidian-style YAML emit, one scoped commit with index rebuild, inverse-ops Undo). YAML stays first-class via `y` jumps and lint marks. Four phases:

1. **report-additions** (bob-cli, medium) — additive list-JSON fields (`suggest`, `default`, bounds, `line`, `filled`, per-choice counts, `dated_notes`, `legacy`, a semantic `schema_fingerprint`) plus the Obsidian-style emitter fix.
2. **schema-writer** (bob-cli, large) — `bob albums update` with the ops envelope, typed refusals for data-stranding edits (key renames, used removals, noun/kind changes), and the seven-point correctness contract.
3. **header-reshape** (bob-plugins, medium) — collapsed summary, chip view, read-only Schema Card, YAML jump + lint marks; builds on whatever `k3.7.1.4` lands.
4. **card-editor** (bob-plugins, large) — the editable card gestures, consequences, Undo, and palette/Command Mode/record-note entry points.

**Four reviewer decisions** are embedded for you at the approval gate: commit granularity (default: one commit per gesture), mobile fallback (default: read-only degrade), overloading `Ctrl+Shift+P` on album notes (default: yes), and the `album-schemas-edited-through-bob` memory decision record (default: off, since the research marked it as needing your explicit yes).

**Coordination**: since all of `bob-cli-k3.7.1`'s header phases are in flight *right now*, I left a note on `bob-cli-k3.7.1.4` steering it toward collapsed-by-default if its header hasn't painted yet, and the plan hard-gates its two plugin phases on that child epic closing — the two bob-cli phases can start immediately either way. One timing consideration for you: approving this epic is safe at any point, but its plugin phases will wait on `k3.7.1` landing.
