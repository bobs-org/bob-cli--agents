# Chat History - ace-run (dc--plan)

- **TIMESTAMP:** 2026-11-11 14:47:12 EST
- **MODEL:** claude/claude-fable-5
- **AGENT:** dc--plan

**Plan:** /home/bryan/.sase/plans/202611/prj_hide_tag_marks.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/prj_hide_tag_marks.md`

> # Render `#prj` and `#hide` as icon marks (extend the task-tag-marks family)
> ## Goal
> Stop rendering the machine-managed `#prj` and `#hide` tags as loud violet tag pills in
> Obsidian. Instead, extend the existing **task-tag-marks** family (bob-ledger-tools) so
> that:
> 1. The canonical identity pair `#task #prj` on a project lifecycle task renders as **one
>    project glyph** in the identity slot — exactly the way `#task #ref` already renders
>    as one open-book glyph. Teal identity ink; shape says "project task".
> 2. An exact whole-token `#hide` tag on a task line renders as **one quiet eye-off
>    glyph** in place — a metadata mark (like the date/priority marks) that says "hidden

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me start hiding the `#prj` and `#hide` tags in Obsidian, which
have special meanings, in favor of rendering one or more appropriate icons in their
place (you should choose the location of these icons based on what is most intuitive /
what you think is best)? I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:claude-fable-5

## Response

I'll help design this feature. Let me start by gathering context: reading the relevant SASE memory about the vault conventions and the meaning of these tags, then exploring the bob-plugins repo where the Obsidian rendering code lives.

The `bob-ledger-tools` plugin has a family of "marks" fragments, including `264-plugin-task-tag-marks.js`, which sounds like an existing tag-rendering precedent. Let me study it.

Let me read the bob-cli display contract document that owns this mark family.

I have the full implementation picture. Before designing, let me gather real vault counts (like the contract doc's existing "Vault counts" section) to validate eligibility decisions.

Tale at `medium` size fits: one agent, bounded, heavily precedented by the `#ref` book marks. One last structural check — the fragment manifest order — then I'll author the plan.

All research is done. Now I'll author the tale plan in my workspace root.

Validation failed mainly because unquoted `#` in YAML strings starts a comment (gutting several fields), labels exceeded 100 chars, and `title`/`goal` were missing. Let me fix the frontmatter.

Validation passed with zero warnings. Submitting the plan now.

The plan is staged. Finishing the turn through `/sase_final` as instructed.

Done — the plan is authored, validated, and proposed. The staged proposal will reach you for review after this turn ends (no declaration was required; the proposal handoff carries the plan).

## What I designed

**Goal:** stop rendering the machine-managed `#prj` and `#hide` tags as violet tag pills, replacing them with icons — by extending the existing **task-tag-marks** family (the same system that already renders `#task` as a teal hash, `#task #ref` as an open book, and `#task #gtd #pre/#post` as sunrise/flag glyphs). That family already solves every hard problem here: Live Preview replace-and-reveal widgets, in-place Reading-view annotation that survives Dataview's `innerHTML` round trip, CSS-only Tasks-query-row styling, a session toggle, and PDF/mobile support.

**The two marks:**
- **`#task #prj` pair → one project glyph** in the identity slot (default: a stroked target — ring plus dot — in the family's teal identity ink), mirroring the `#ref` book exactly. Touching it reveals both raw tags; tooltip reads `#task #prj · project lifecycle task`.
- **`#hide` → a quiet eye-off glyph** in place, in the grey metadata ink the date marks use. Research showed `#hide` is not project-only: the vault has 385 `#hide` task lines — 64 on `^prj` rows (owned by `bob projects sync`) and ~320 on reference reading tasks — and bob's review predicate hides *any* tagged task, so the mark covers every task line with an exact whole-token `#hide`. Tooltip: `#hide · hidden from review and lanes`.

Eligibility is deliberately conservative (exact tokens, identity-slot adjacency, code exclusion), so `#prj_is_blocked`, `#hidden`, mid-title tags, and non-task lines honestly keep their pills.

**The plan** (`sase_plan_prj_hide_tag_marks.md`, tale, size medium) spans both repos: new sections plus PJ/HD conformance vectors in the bob-cli contract doc `docs/task-tag-marks.md`, and in bob-plugins a new pure-core fragment, range/builder/reading-view wiring, CSS glyphs, tests, a version bump, and `bob plugins sync`. It embeds four reviewer decisions you'll answer at approval: the project glyph shape (target / milestone / folder), the `#hide` ink (grey / teal), the `#hide` scope (all task lines / canonical rows only), and whether to also strip the tags from picker text now or defer that to a follow-up bead.

One fun find along the way: your own `- [/] #task Make #prj and #hide pretty!` task in `bob.md` — this plan is it.
