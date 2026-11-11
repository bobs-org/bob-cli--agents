# Chat History - ace-run (research.44.gem)

- **TIMESTAMP:** 2026-11-11 06:56:06 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.44.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261111_064505.md`

## Prompt

%id(gem, clan=research.44)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.44.cdx`, `research.44.cld`, `research.44.grk`, `research.44.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We already show a little key with a count next to task links that would free dependents.
I would now like to start adding a similar icon that hows how many other
ready/pending/next tasks exist in that task's leaf project which do not currently have
task links associated with them in today's daily file (so I know how many tasks will
appear in the successor offer when completing that task).

- This icon should only be shown for task links that correspond with tasks that live in
  leaf projects.
- For example, in the ~/tmp/screenshots/20261111_063929.png screenshot of the
  ~/bob/2026/20261111.md file, the `[[job_email_recruiters#^bryan-stephen-luzern-risk]]`
  task link should show this icon with a 4 next to it, since the
  ~/bob/job_email_recruiters.md file contains 4 next tasks that have no task links in
  today's daily file associated with them.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

# Research Findings & Design Blueprint: Leaf Project Successor Marks

**Researcher:** `research.44.gem` (Antigravity)  
**Report Document:** [`leaf_project_keep_moving_marks__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/research/202611/leaf_project_keep_moving_marks__gem.md)  
**Registered Artifact:** `research:202611/leaf_project_keep_moving_marks__gem.md` (`file:explicit:0bdf4beffec53135fa1de7ef`)

---

## Executive Summary & Plan Critique

Surfacing the count of upcoming unlinked tasks from a task's leaf project directly on task links in today's daily file is a **high-leverage, ergonomic enhancement**. It provides complete forward visibility into whether completing a planned task will conclude work on that project for the day or immediately unlock a queue of ready project work in the keep-moving successor offer.

However, an uncritical implementation of the initial proposal harbors **one critical flaw**:

### The K4 "Last Planned Task" Invariant Violation
The prompt states: *"so I know how many tasks will appear in the successor offer when completing that task"*.
Under Bob's accepted keep-moving engine ([`docs/task-dependencies.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/docs/task-dependencies.md#L2663-L2725) §12.15, rule **K4**):
> **Rule K4:** *Keep-moving successor offers ONLY trigger when the task being completed is the LAST live planned task for that leaf project today.*

If Bryan plans two tasks from the same leaf project today (e.g. `job_email_recruiters#^taskA` and `job_email_recruiters#^taskB`), completing `taskA` will produce **0 successor offers**, because `taskB` is still planned! If the UI were to show a badge promising `4` successors on `taskA`, completing `taskA` would produce silence, breaking user trust and violating Bob's truth-in-advertising principle.

---

## Key Requirements Adjustments

1. **Strict K4 Gating (Truth in Advertising):**
   - The successor mark should **only be displayed when the task link is currently the sole remaining live open link** for that leaf project in today's daily file.
   - If multiple open tasks from the project are planned today, the mark is withheld. As soon as all preceding tasks are completed, the final remaining open task link immediately lights up with the badge.
2. **True Candidate Set Filtering:**
   The count must strictly match §12.15 offer eligibility, not raw tasks:
   - Exclude the project header line (`^prj`).
   - Exclude tasks tagged `#hide`.
   - Exclude future-scheduled tasks (`scheduled > today`).
   - Exclude dependency-blocked tasks (`[?]`, open `[dependsOn::]`, or `#prj_is_blocked`).
   - Exclude tasks already planned in today's file (open or closed).
   - Gate on the project itself being unblocked (if `^prj` is blocked, count is 0).

---

## Visual Design: Intuitive, Reliable, and Beautiful

### 1. Iconography: Use Canonical `⏭`
Rather than introducing a folder (`📁`) or document emoji, use **`⏭`** (`\u23ED` / Lucide `skip-forward` / SF Symbol `forward.end.fill`).
- **Semantic Harmony:** `⏭` is already the universal glyph throughout Bob's design system for keep-moving successor offers ([`docs/task-dependencies.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/docs/task-dependencies.md#L2839-L2846) §12.15).
- When Bryan sees `⏭ 4` on `[[job_email_recruiters#^bryan-stephen-luzern-risk]]`, pressing `Ctrl+Enter` opens the modal titled `⏭ Keep job_email_recruiters moving` offering those 4 tasks, followed by a notice `⏭ Next in WRITE: ... · keeps job_email_recruiters moving`. The visual identity is 100% unified.

### 2. Color & Styling
- **Color Token:** Uses the **Next** status color token (`--color-blue` / cyan-blue).
  - Resting state: Quiet muted text with a subtle cool hue (`color-mix(in srgb, var(--color-blue) 45%, var(--text-muted))`).
  - Hover state: Brightens to `var(--color-blue)` with a soft background wash (`color-mix(in srgb, var(--color-blue) 12%, transparent)`).
  - Contrasts clearly with the amber/warm hue of `🔑 N` frees marks.
- **Micro-interaction:** 180ms subtle scale tick when counts change, respecting `prefers-reduced-motion`.

### 3. Layout Order on the Ledger Line
Adjacent decorations at CodeMirror 6 `Decoration.widget` positions:
```text
[[target#^blockId]]  [Progress Ring]  [Unblocked 🔓]  [Frees 🔑 N]  [Keep Moving ⏭ N]  [Off-Clock Chip]  [Mail/Event Pill]
  (anchor text)         (side: 1)       (side: 2)       (side: 2)         (side: 2)          (side: 3)          (side: 4)
```
`🔑 N` (causal unblocking) precedes `⏭ N` (project continuity).

### 4. Rich Tooltip
Hovering reveals a structured preview matching `freesMarkTooltip`:
```text
Keep job_email_recruiters moving · 4 successors
• ✉️ Founding Engineer at EcoGPT · Roej Hollon-Calaguas [Next]
• ✉️ 🔥 Bryan — your Python/release tooling made me circle back [Next]
• ✉️ Product Engineer · Dan Dowd [Next]
+1 more
Offers when this last planned task is completed
```

---

## Implementation Architecture

The feature belongs entirely in [`bob-plugins`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins), specifically [`plugins/bob-ledger-tools`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools), mirroring `141b-frees-marks.js`:
- **`src/141d-keep-moving-marks.js`**: Pure data model, candidate classification, and `buildKeepMovingMarkElement`.
- **`src/271d-plugin-keep-moving-marks.js`**: Live Preview `ViewPlugin` and Reading view postprocessor with session toggle command (`Toggle Task Link keep-moving marks`).
- **`styles.css`**: Rules for `.bob-keep-moving-mark`.
- **Zero I/O overhead**: Feeds directly from the in-memory `freshnessEnsureMemo()` and `todayCache`.

The full report with complete code specifications, test vectors, and Mermaid architecture diagrams has been committed and registered as an audited artifact.
