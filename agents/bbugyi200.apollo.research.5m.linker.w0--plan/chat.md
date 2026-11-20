# Chat History - ace-run (research.5m.linker.w0--plan)

- **TIMESTAMP:** 2026-11-20 17:00:53 EST
- **MODEL:** claude/opus
- **AGENT:** research.5m.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/successor_jump_pin.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/successor_jump_pin.md`

> # Plan: Ctrl+J jump pin on the successor card
> Source research (Bryan agreed with its requirements; memory changes only as the
> decisions above allow): `research:202611/successor_jump_pin/successor_jump_pin.md`. This
> plan is the contract every phase implements; where it is more specific than the
> research, this plan wins.
> ## The design in one sentence
> **Jump is where you land, never what happens.** Ctrl+J stages one _jump pin_ on one
> offer of the successor card. The pin sits alongside the four verdicts (Leave, Pull in,
> Done, Cancel), is applied after every write lands, finds the task again by identity, and
> never touches the vault.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to add a new `<ctrl+j>` keymap to the successor panel shown in
Obsidian and in the capture panel. Can you help me implement this?

- This keymap should be able to be used to mark a successor that should be jumped to
  after completing the task (this should override the `<cmd+enter>` keymap in the
  capture panel--if it was used to submit the capture).
- We should be able to mark only a single task as the "jump successor" and that task may
  have any other state (i.e. it can be left open and not be pulled in, be pulled in, be
  closed, or be canceled).
- After the user completes the task close that triggered the successor panel, we should
  jump to the appropriate file in Obsidian and focus the selected jump successor task.
- This is often desirable when we don't want to pull a task in (so we can prioritize it,
  for example) or when we want to pull a task in that needs some changes made to it.
- Review the successor_jump_pin.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.5m.linker

## Response

I've read the jump-pin research report. Next I'm going through the three repos it touches (bob-cli, bob-plugins, bob-mac-capture) so I can design the phases.

I've mapped the cycler close flow, the Mac card, and bob-cli's offer plumbing. Now I'm reading the Obsidian successor picker modal directly so the design fits it.

Still exploring: now tracing how the cycler uses the picker result and settles the review walk, which is where the jump has to happen.

Now the close finalizer and the Vim Ctrl+Enter walk settle:

I'm now reading the relevant project memory (the CLI and docs rules, the walk decisions, and glossary terms) before I write the plan.

Nearly done exploring. I'm checking whether the docs glossary is generated from memory, which decides how the new "Jump Successor" term ships.

Exploration is done. I'm checking two last build details (fragment registration and mixin wiring) before I write the plan.

I have what I need. Writing the epic plan now.

Plan validates with no warnings. Submitting it.

I've submitted a seven-phase epic plan for your review. Nothing has been built yet; implementation starts once you approve it.

**How it works.** Ctrl+J pins one offer on the successor card, either in Obsidian or in Mac Capture. The pinned task can still be left open, pulled in, marked Done, or canceled. After every write from the close or capture has finished, Obsidian opens that task's note, puts the cursor on it and flashes the line. Each combination reads as a sentence, like "leave it, take me there" or "pull it in, take me there".

**Design calls I made:**
- **Look:** Obsidian already uses its accent color for the highlighted row (a leading stripe) and for marked rows (a light tint). So the pin is a solid accent capsule, `↗ Jump`, at the right edge of the row. The landing flash uses the same color.
- **Copy:** Obsidian adds a `↗` hover button and a `Ctrl+J jump` hint. The Enter label changes to say what will happen: "leave open & jump", "pull in & jump" or "apply & jump". The footer always names the pinned task, so a pin hidden by the filter is never a surprise.
- **Mac:** the button labels match ("Leave Open & Jump ↩"), the capsule slides between rows, and there are right-click menu items and VoiceOver announcements.
- **Enter and Cmd+Return:** a pin overrides Cmd+Return as you asked, and also plain Return. While a pin is set, Enter no longer pulls in the highlighted row by default, and pressing Enter with only a pin set is a valid commit.
- **Review walk:** a pinned close from a `]s` landing doesn't advance the walk. It jumps to the pinned task, and the next `]s` resumes where the walk left off, like Ctrl+Shift+M does today.
- **Reliability:**
  - The pin writes nothing to the vault.
  - The task is found again after the writes by its block ID or its text, never by an old line number.
  - If it can't be found, your changes are kept and one notice says so.
- **Mac landing:** the Mac opens the jump through the existing open-notes link with a single entry. That link already waits for Obsidian to see the new file contents, so the Mac half needs no Obsidian plugin change.

**Phases:**
1. `bob capture -j/--jump-offer` and the `jump` JSON output, documented first as §12.24 in `docs/task-dependencies.md`.
2. The pin on the Obsidian card. Its source file is at 998 of the 1000-line limit, so some code moves out first.
3. Obsidian landing, the review-walk park, and a `↗ “S”` line in the receipt notice.
4. task-status-cycler support for every managed Done close.
5. The remaining Obsidian callers: PRE/POST checklist rows, relation-complete, and project promotion (which lands on the pin instead of the new `^prj` line). The relation-merge card deliberately doesn't get Ctrl+J.
6. The Mac card, which depends only on phase 1.
7. Docs and memory.

Phases 1 and 2 can run in parallel.

**Two memory decisions for you to answer when approving:**
- **Walk decision record (default yes):** a new decision record, plus marking `answering-advances-the-walk` and `ctrl-enter-leaves-pre` as partly replaced. This defaults to yes because the feature would otherwise make those records state something false.
- **Glossary term "Jump Successor" (default no):** you didn't ask for it, so it's off unless you turn it on.

Pinning muted rows (still-blocked or scheduled-later tasks) is out of scope; it would need a separate bob change.
