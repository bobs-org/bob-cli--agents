# Chat History - ace-run (research.6f.linker.w0--plan)

- **TIMESTAMP:** 2026-11-25 17:48:25 EST
- **MODEL:** claude/opus
- **AGENT:** research.6f.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/plain_link_dependency_ties.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/plain_link_dependency_ties.md`

> # Plan: One tie per task pair — dependencies absorb plain links
> ## Context
> Bryan wants the state "A depends on B **and** A has a relationless link to B" made
> impossible. He agreed to every requirement in the research report
> `research:202611/plain_link_dependency_exclusivity/plain_link_dependency_exclusivity.md`
> (read it with `sase artifact read` before starting any phase). The one exception is
> memory, which changes only through this plan's memory decisions. This plan carries the
> report's adjustments R1–R8. Where the report left room, the plan settles each design
> choice.
> Repositories:

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli When a task, say A, has a dependency on another task, say B, then A should not
also have a relationless link to the same task (in either direction). I would like to
make this invalid/confusing state impossible. Can you help me implement this?

- When adding a relationless link to a task B, we should remove any existing dependency
  to task B from the current task. Similarly, when adding a dependency to a task B, we
  should remove any existing relationless link to task B from the current task.
- We should add the `<ctrl+b>` keymap to the link panel in Obsidian, which should be
  able to be used to mark the task as a dependency instead of linking to it. We should
  also be able to do the reverse (make a dependency a relationless link) from the
  dependency panel in Obsidian.
- Make sure it is clear when looking at the dependency/link panels in Obsidian if the
  task already has a relationless link/dependency, respectively.
- Review the plain_link_dependency_exclusivity.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.6f.linker

## Response

Reading the research report now, then I'll explore the bob-cli and bob-plugins code.

Exploration done across all three repos. Now reading the current stage copy and footers to design consistent UI text.

Code is mapped. Now checking the memory-write rules, since the plan may include a decision record and glossary strand that need your approval.

Design is taking shape. Checking the epic plan schema before writing the file.

I have what I need. Writing the epic plan now (9 phases across bob-cli, bob-plugins, and bob-mac-capture).

Validation passed. One fix before proposing: the memory callout suggested touching an existing decision record that the memory decision doesn't cover. Removing that.

Valid. Proposing the plan.

I wrote a 9-phase epic plan and proposed it; it's waiting for your approval and nothing has been implemented yet. It follows the research report's recommendations throughout.

**The rule.** A pair of tasks can be tied by a dependency or by a plain (unlabelled) link, never both, in either direction. Labelled relations can still sit beside a dependency.
- Adding a dependency removes the plain link from every writer, since nothing is lost.
- Turning a dependency back into a plain link can unblock a task, so only a deliberate Obsidian gesture does it, and only after its effect is on screen.
- Capture, agents, hand edits and reconcile never remove a dependency.
- `bob task reconcile` cleans up hand-made overlaps, and the dependency always wins.

**In Obsidian.** Inside any of the four panels (Depends on, Blocks, Links, Linked from), Ctrl plus the Task Card key sets the highlighted pair's tie:
- **⌃B**: this task waits on it.
- **⌃⇧B**: it waits on this task.
- **⌃L**: make it a plain link.

The chords set a target state, so pressing one twice never flips it back. Making a pair a plain link with a chord commits on one press. Doing it with ↵ in the Links panel takes a second ↵ to confirm, because ↵ is the key you'd hit out of habit. Batches and counted sessions refuse these conversions.

**Making the existing tie clear:**
- Rows in all four panels get small labels in both directions (`⛓ prerequisite`, `🧱 dependent`, `🪢 linked`, `🪢 links here`).
- A `⇄` badge marks rows where ↵ would convert the tie rather than add one.
- With an empty filter, a "TIED BY A DEPENDENCY" or "PLAIN LINKS" section lists the other kind of tie.
- Panel subtitles count it.
- The Depends-on panel gets the line describing what ↵ will do, which it lacks today.
- Notices say what was replaced, e.g. `⛓ Now waits on "X" · replaced the 🪢 link · Blocked`.

**Phases:**
1. Contract docs, shared test vectors, and Rust helpers.
2. Reconcile cleanup plus `bob task merge`, with a read-only dry run against the live vault. The research expects exactly one overlap, in `bob.md`.
3. Capture: `&` and `*` absorb plain links; a plain `~` over a dependency is a reported no-op; `&T ~T` in one item is an error that explains the fix.
4. New `capture-complete` fields saying whether a candidate is already a prerequisite, a dependent or plain-linked.
5. Obsidian phases 5–8, run one after another to avoid deploy collisions: the core planning logic, the visual changes, the writer that does the conversions, then the keys.
6. Bob Mac Capture (phase 9): show the new labels and report rows, then watch macOS CI to green.

Phase 5 lands three things the research found: `isCtrlKey` currently also matches Ctrl+Shift, a stale-conflict reopen opens the wrong panel, and the badge text gets clipped.

**Decisions for you at approval:**
- **⌃⇧L** (on by default): it makes "it links to this" a fourth chord so every Task Card relationship key works with Ctrl. This is my addition beyond the report's three chords.
- **Memory changes** (two toggles, both off by default as you asked): a new decision record for this policy, and one sentence added to the Task Relation glossary entry.
