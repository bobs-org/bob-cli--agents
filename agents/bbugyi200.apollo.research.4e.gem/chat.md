# Chat History - ace-run (research.4e.gem)

- **TIMESTAMP:** 2026-11-12 11:15:18 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.4e.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261112_110045.md`

## Prompt

%id(gem, clan=research.4e)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.4e.cdx`, `research.4e.cld`, `research.4e.grk`, `research.4e.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We currently always show the GTD review footer. I would like to start making this footer
only show when the GTD review walk is active (i.e. the `s` key is active and will be
triggered by the `[[` and `]]` keymaps).

- As a part of this change, we should add two appropriate new footers that are active
  only when the `w` walk or `n` walk is active.
- The `w` walk should have indicators that show how many pending/next/ready tasks are in
  that walk, for example.
- We should add an excellent new "walker footer" glossary term to describe these footers
  (note that a "review footer" should be considered a type of "walker footer").
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

# Independent Research Report: Mode-Coupled Walker Footers for Obsidian

**Researcher ID:** `research.4e.gem` (Gemini 3.8 Flash)  
**Report File:** [`walker_footers_design_and_evaluation__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/research/202611/walker_footers_design_and_evaluation__gem.md)  
**Artifact Snapshot:** `file:explicit:1c731698482f737f859ed286` (`research:202611/walker_footers_design_and_evaluation__gem.md`)

---

## 1. Executive Summary & Critique of the Proposal

### The Proposal
1. Restrict the Morning GTD Review Footer (`.bob-freshness`) to display **only** when the `s` walk is active (i.e. `s` is selected in `[[ s w n ]]`, meaning `[[` / `]]` trigger `[s` / `]s`).
2. Introduce two new status bar footers active when `w` (Lane Walk) or `n` (Link Walk) is active.
3. Show pending / next / ready indicators for the `w` walk.
4. Establish an authoritative "Walker Footer" glossary strand.

### Critique: Is This a Good Idea?
**Verdict: YES, with high confidence**, provided four critical ergonomic and architectural refinements are included:

1. **Why It Is a Major Win:**
   - **Clutter Elimination:** Currently, the GTD Review Footer is visible 24/7 as long as any task queue exists. Seeing `Review 28 due · Commitments done · Upkeep budget met` during deep afternoon execution is visual debt.
   - **Completes the Mental Model:** Bob has the `[[ s w n ]]` Bracket Mode Indicator, but historically only `s` had a dedicated status bar cockpit, while `w` had only a transient screen toast and `n` had zero ambient presence. Unifying all three walks under a polymorphic "Walker Footer" creates elegant symmetry.

2. **Crucial Pitfalls & Required Adjustments:**
   - **Pitfall 1 (The "Transient Jump" Interruption):** In Bob, typing `]n` or `]w` immediately switches bracket repeat mode. If Bryan is in the middle of morning GTD review and uses `]n` to inspect a referenced note, a naive implementation would immediately hide the Review Footer, hiding remaining commitment counts.  
     *Adjustment:* Add an **Unfinished Commitment Notification Pip** on the `s` segment within `[[ s w n ]]` (e.g. `[[ s• ⟨w⟩ n ]]`). If morning commitments remain due, `s` wears a quiet amber pip, and its tooltip explicitly reminds Bryan that review commitments are still pending.
   - **Pitfall 2 (`Alt+P` Quick Roll Preview Parity):** The current review footer displays `Alt+P` roll/decay previews on any prioritized task even off-walk. Tasks visited in the `w` (Lane) walk are actively prioritized.  
     *Adjustment:* The Lane Walker Footer (`w`) must fully inherit the `Alt+P` Quick Roll preview slot.
   - **Pitfall 3 (Queue vs. Traversal Asymmetry):** `s` and `w` are global queues ($r/N$), but `n` is a document-local relative traversal across body links.  
     *Adjustment:* The Link Walker Footer (`n`) must not attempt to fake a global queue. Instead, it should act as an interactive directional control cockpit showing explicit relative targets (e.g. `‹ 20261111 · 20261113 ›`) with direct click-to-jump affordances.
   - **Pitfall 4 (Inter-Plugin Status Bar Contention):** Multiple plugins creating independent `addStatusBarItem()` elements fighting for `margin-right: auto` causes DOM layout reflows and ordering races in Obsidian.  
     *Adjustment:* Use a **Single Walker Slot Architecture** hosted in `bob-ledger-tools` (which already owns the width-fitting engine, tier colors, and styles), consuming `api.bracketMode` and `api.linkWalk` from `bob-navigation-hotkeys`.

---

## 2. Design Specifications for the Three Walker Footers

### 2.1 The GTD Review Walker Footer (`s`)
* **Scope:** Shared GTD Freshness Queue across the vault (PRE $\to$ NEW $\to$ PROJECTS $\to$ PENDING $\to$ NEXT $\to$ RECURRING $\to$ TICKLER $\to$ ROTTEN $\to$ POST).
* **Wide Display:**  
  `⟳ Review 7 due · 4 commitments   NEW 1 · PENDING 2 · RETURNED 1 · ROTTEN 3   ✓ 0/15 today · ]s next`
* **On-Row Display:**  
  `⟳ Review 2/7 · PENDING 1/2 · confirmed yesterday   NEW 1 · NEXT 2 · ROTTEN 3   ✓ 0/15 today   [Alt+P roll P2]`
* **Primary Click:** Executes `bob-navigation-hotkeys:jump-to-next-due-task` (`]s`).

### 2.2 The Lane Walker Footer (`w`)
* **Scope:** Today's Plan tasks (PENDING / NEXT / READY off today's plan, from `api.laneWalk v2`).
* **Off-Walk Display:**  
  `⤹ Lanes 14 active   2 WIP · 4 Next · 8 Ready   [───▪▪▪▪────────]   ]w next`
* **On-Walk Display (Cursor on a NEXT task):**  
  `⤹ Lanes 3/14 · NEXT 1/4 · ‹proj/bob-cli› Fix memory leak   2 WIP · 8 Ready   [Alt+P roll P2]`
* **Visual Elements:**
  - **Lane Badges:** Warm amber for `WIP` (`is-pending`), vibrant cyan for `NEXT` (`is-next`), quiet violet for `READY` (`is-ready`).
  - **Miniature Lane Rail:** A compact 40px inline micro-bar showing relative lane proportions with an active task cursor pip.
  - **Action Hint:** `Alt+P roll P2` if prioritized, or `Ctrl+Shift+Enter today` / `Alt+N release`.
* **Primary Click:** Executes `bob-navigation-hotkeys:jump-to-next-lane-task` (`]w`). `Shift+Click` executes `]W` (next lane).

### 2.3 The Link Walker Footer (`n`)
* **Scope:** Active Markdown note's body navigation links (`prev` / `next`, `‹ W44` / `W46 ›`).
* **Bidirectional Display (Daily Note):**  
  `⇄ Links   ‹ 20261111   ·   20261113 ›   [n / ]n`
* **Bidirectional Display (Weekly Note):**  
  `⇄ Links   ‹ W45   ·   W47 ›   [n / ]n`
* **Single Direction (Start/End of Series):**  
  `⇄ Links   ‹ (start)   ·   2026-W02 ›   ]n next`
* **Empty / Off-Note:**  
  `⇄ Links: none in note` (or `no active note`).
* **Interactive Affordance:** The left segment (`‹ 20261111`) is a direct click button for `[n`; the right segment (`20261113 ›`) is a direct click button for `]n`.

---

## 3. The New Glossary Strand: "Walker Footer"

Published in full within the research report and ready for `sase/memory/glossary/walker-footer.md`:

```markdown
---
keyword: Walker Footer
aliases:
  - "walker footers"
  - "walk footer"
---

The desktop Obsidian status-bar cockpit that visualizes the currently active bracket-walk family (`s` review, `w` lanes, or `n` links) as selected in the [[bracket-mode-indicator]] (`[[ s w n ]]`). A walker footer keeps the walk's queue progress, current cursor rank, and navigational targets in view without opening modal cards or reading vault files. Exactly one walker footer is active at a time, governed dynamically by `bob-navigation-hotkeys`'s remembered bracket-repeat type:

1. **[[morning-gtd-review-footer|Review Walker Footer]] (`s`):** The GTD review cockpit over the shared [[task-freshness]] queue (`]s` / `[s`), showing remaining due counts, commitment progress, tier breakdowns, and the `Alt+P` roll preview.
2. **Lane Walker Footer (`w`):** The daily plan execution cockpit over Today's PENDING, NEXT, and READY task lanes (`]w` / `[w`), showing active task counts by lane, on-walk queue position (`Lanes r/N · LANE i/M`), lane-tinted indicators, and the `Alt+P` roll preview.
3. **Link Walker Footer (`n`):** The document traversal cockpit over active-note body navigation links (`]n` / `[n`), showing previous and next relative targets (e.g. daily note dates `‹ 20261111 · 20261113 ›` or period weeks `‹ W44 · W46 ›`) with direct click-to-jump controls.

A walker footer is a read-only projection: clicking its main element triggers the forward jump of the active walk (`]s`, `]w`, or `]n`), while tooltips summarize full queue metrics and shortcut keymaps. When the bracket repeat mode is unset (`none`), the footer remains dormant or yields its space; when a walk's queue is clear, the footer presents an unobtrusive clear indicator or ambient priority preview rather than cluttering the status bar. When morning review commitments remain due in the `s` walk while `w` or `n` is active, the `s` segment in the [[bracket-mode-indicator]] wears an accent notification pip so review obligations remain visible throughout the day.
```

---

## 4. Recommended Architectural Implementation

1. **API Contracts in `bob-navigation-hotkeys`:**
   - Expose `api.bracketMode v1`: `{ getMode(), setMode(type), onModeChange(listener) }`.
   - Expose `api.linkWalk v1`: `{ scanCurrentNoteLinks() }` returning `{ prev, next, path }`.
2. **Unified Walker Host in `bob-ledger-tools`:**
   - Retain the existing status bar slot `.bob-freshness` / `.bob-walker-footer` (`margin-right: auto`).
   - Re-render the container via pure view models (`freshnessFooterView`, `laneWalkFooterView`, `linkWalkFooterView`) when `bracketMode` changes or on file/cursor events.
3. **CSS & Aesthetics:**
   - Add `.is-pending` (amber), `.is-next` (cyan), and `.is-ready` (violet) badge classes.
   - Add `.bob-walker-rail` inline micro-progress bar.
   - Maintain full light and dark theme compatibility with `--interactive-accent` and `--font-interface`.

The complete architectural analysis, mockups, state transition diagrams, and testing strategy are preserved in [`walker_footers_design_and_evaluation__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/research/202611/walker_footers_design_and_evaluation__gem.md).
