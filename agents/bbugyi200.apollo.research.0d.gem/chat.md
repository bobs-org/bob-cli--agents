# Chat History - ace-run (research.0d.gem)

- **TIMESTAMP:** 2026-10-06 05:59:55 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.0d.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261006_054218.md`

## Prompt

%id(gem, clan=research.0d)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.0d.cdx`, `research.0d.cld`, `research.0d.grk`, `research.0d.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to integrate more of my keymaps with my GTD morning review, which I trigger
via the `]s` Obsidian keymap and continue walking through using `]s` until I have
reviewed all items from all review groups.

- I already added support for the `<ctrl+enter>` keymap for the PRE review group, but
  I'm thinking that anytime that we close the current review item using this keymap, we
  should use this behavior (i.e. automatically jump to the next/first review item).
- Also, there are multiple other keymaps that trigger actions which also imply that we
  should iterate to the next review item. The `<ctrl+shift+enter>` and `<ctrl+shift+p>`
  (assuming a task card option is selected that removes the review item from the review
  stack) keymaps, for example, should ideally trigger an automatic jump to the next
  review item.
- You should look for and propose other keymaps / actions that should trigger a jump to
  the next review item when in the middle of a GTD morning review.

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
(for example `research:202609/topic__a.md`), including any subdirectory the steps above
put it in. Do not derive the label from the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

# Research Report: Integrating Keymaps with GTD Morning Review Auto-Advance

**Researcher:** `gem` (5-Researcher Swarm)  
**Report Artifact:** [`research:202610/gtd_review_keymap_auto_advance__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/research/202610/gtd_review_keymap_auto_advance__gem.md)  
**Durable Snapshot Reference:** `file:explicit:1deb5581160754813670db89`  
**Target Repositories:** `bob-plugins` (`bob-navigation-hotkeys`, `task-status-cycler`, `block-id-prompt`, `bob-ledger-tools`), `bob-cli`

---

## 1. Executive Summary & Verdict

The GTD morning review walk triggered via `]s` (`bob-navigation-hotkeys:jump-to-next-due-task`) traverses a strict sequence of tiers:
$$\text{PRE} \to \text{NEW} \to \text{PROJECTS} \to \text{PENDING} \to \text{NEXT} \to \text{RETURNED} \to \text{REFERENCES} \to \text{ROTTEN} \to \text{POST}$$

Currently, a significant asymmetry exists in user ergonomics:
- `Ctrl+Alt+F` ("Refresh task freshness and jump") already executes a combined **action + jump** step.
- `<ctrl+enter>` in `PRE` completes the checklist item and jumps within the group (though it halts at the boundary of `NEW`).
- However, for all other resolution gestures—completing backlog tasks with `<ctrl+enter>`, linking to today's Pomodoro ledger with `<ctrl+shift+enter>`, rolling/cancelling via the Task Card (`<ctrl+shift+p>`), or releasing a lane with `Alt+N`—the system executes the mutation in place and leaves the cursor stranded, forcing the user into an awkward, repetitive two-step motor cadence:
$$\text{[Execute Triage Action]} \longrightarrow \text{[Press } {]s} \text{]}$$

### Verdict
**This is an excellent, highly justified idea.** The GTD morning review is an operational triage conveyor belt, not a deep-work writing session. Forcing an extra `]s` stroke after an unambiguous triage decision breaks flow and creates friction. 

However, **the plan requires specific safeguards**—primarily an instant Vim jump-list escape hatch (`<C-o>`), strict landing validation to prevent runaway jumps during daytime editing, and clear boundary notices when crossing tiers.

---

## 2. Keymap-by-Keymap Feasibility & Behavioral Analysis

### 2.1 `<ctrl+enter>`: Generalizing Task Completion Across All Tiers
- **Current Behavior:** In `task-status-cycler` (`handleVimTaskToggleOpenDone`), `<ctrl+enter>` checks `claimReviewWalkCtrlEnter`. In `bob-navigation-hotkeys` (`535-plugin-review-checklist-walk.js`), this is strictly gated to `tier === "pre" || tier === "post"`. Furthermore, it passes `withinGroup: true`, so when the last PRE item is completed, it stops and posts a notice rather than advancing into `NEW`. Outside of PRE/POST, it falls back to cycler's in-place task toggle.
- **Proposed Behavior:**
  1. Remove the `tier === "pre" || tier === "post"` gate so that any task landed on via `]s` claims completion through `claimReviewWalkCtrlEnter`.
  2. Set `withinGroup: false` so that completing the last PRE checklist row automatically transitions into `NEW` (with boundary notice).
  3. **Strict Directional Guard:** Only trigger auto-advance when transitioning an *open* status (`' '`, `'/'`, `'*'`, `'?'`) into completed (`'x'`). If the user toggles an already-completed task (`[x]` $\to$ `[ ]`), it reopens; **reopening must stay in place**.

### 2.2 `<ctrl+shift+enter>`: Linking to Today's Pomodoro Ledger
- **Current Behavior:** Handled in `block-id-prompt` (`openPomodoroTaskLink`). It links the task to today's Pomodoro in the daily note (assigning a block ID if needed) and sets the task status to Next (`*`). It has no integration with `bob-navigation-hotkeys`.
- **Review Stack Impact:** Under Decision 8 and Decision 11, Today-linked tasks are explicitly excluded from all review tiers. Linking a task to Today permanently removes it from the review backlog for that day.
- **Proposed Behavior:**
  1. Once both the source task note and daily note writes succeed (`reportPomodoroLinkOutcome`), `block-id-prompt` calls `bob-navigation-hotkeys`'s `api.advanceReviewWalkIfLanding(editor, { action: "today" })`.
  2. If the user was on an active `reviewLanding`, the review anchor marks the item handled and jumps to the next due task.
  3. **Linking vs. Unlinking:** Pressing `<ctrl+shift+enter>` on an already-linked task unlinks it (returning it to the backlog). **Unlinking must stay in place**.

### 2.3 `<ctrl+shift+p>`: The Task Card Modal
- **Current Behavior:** Opens `TaskCardModal` in `bob-navigation-hotkeys`. The modal allows rolls, scheduling dates, cancellations, priority adjustments, dependencies, and lane releases.
- **Granular Action Matrix:** An action must trigger auto-advance *if and only if* it removes the item from the review stack:
  - **Recommended Roll / Decay / Cancel (`Ctrl+Enter` on Card):** $\to$ **Auto-Advance.** Future date ($> \text{today}$) or Cancelled (`[-]`) removes it from the walk.
  - **Cancel Task (`cancel` action):** $\to$ **Auto-Advance.** Marks task `[-]` Cancelled.
  - **Schedule Date:** $\to$ **Auto-Advance if $\text{date} > \text{today}$.** (If scheduled for today or past, stay in place).
  - **Priority Selection:** $\to$ **Auto-Advance if the priority ladder rolls the date into the future.** (If set without rolling, stay in place).
  - **Lane Release (`lane` action on Pending/Next):** $\to$ **Auto-Advance.** Demoting Pending or Next to Ready removes it from daily lane review.
  - **Dismiss / Cancel (`Esc`, `q`, `Ctrl+[`):** $\to$ **Stay.** No edits made.
  - **Non-removing properties (dependencies stage, review interval):** $\to$ **Stay.**

---

## 3. Other Candidate Keymaps & Actions

We surveyed the entire keymap and command catalog across `bob-plugins` and propose the following:

### 3.1 HIGH RECOMMENDATION: `Alt+N` (`toggle-task-lane`)
- **Workflow in Morning Review:** In the `PENDING` (`[/]`) and `NEXT` (`[*]`) tiers, the user is performing daily lane review. The three fundamental triage choices are:
  1. *Keep in lane:* `Ctrl+Alt+F` (stamps freshness and advances).
  2. *Commit to Today:* `Ctrl+Shift+Enter` (links to today and advances).
  3. *Release back to Ready:* `Alt+N` (demotes to Ready).
- **Impact:** Releasing a task to Ready removes it from the daily lane review tier. In addition, committing an inbox task in `NEW` to Next stamps freshness today (`stampLine`), dropping it from today's walk.
- **Recommendation:** **Enable auto-advance on `Alt+N` when on a review landing.** Without this, 2 of the 3 lane review options would advance, but `Alt+N` would stall.

### 3.2 MEDIUM RECOMMENDATION: `Ctrl+Shift+]` (`toggle-obsidian-task`)
- **Behavior:** Demotes an Obsidian task (`- [ ]`) to a plain bullet (`- `).
- **Impact:** The item is no longer an actionable task; it drops out of the freshness evaluator completely.
- **Recommendation:** Trigger auto-advance upon demotion.

### 3.3 MEDIUM RECOMMENDATION: `Ctrl+Shift+M` (`move-tasks-to-note`)
- **Behavior:** Moves the task under the cursor to another project/area note.
- **Recommendation:** Trigger auto-advance. The task has been filed away; the cursor is now left on whitespace. Continuing to the next due item maintains flow.

### 3.4 STRONG ANTI-RECOMMENDATION: `Alt+[` / `Alt+]` (Task Status Cycling)
- **Why It Should NOT Auto-Advance:** Status cycling is an exploratory, multi-stroke sequence (` ` $\to$ `/` $\to$ `x` $\to$ `-` $\to$ `?`). If transitioning past `x` immediately yanked the editor to a different note in another folder, it would disrupt multi-keystroke cycling and cause severe disorientation. Status cycling should remain strictly in-place.

---

## 4. Plan Critique, Pitfalls & Required Adjustments

### 4.1 The "Runaway Conveyor Belt" & Loss of Editing Context
- **Risk:** Unlike `Ctrl+Alt+F` (which has `Alt+F` as an explicit "stay" companion), `<ctrl+enter>` and `<ctrl+shift+enter>` have no "stay" variant. If a user completes a task but wanted to add follow-up notes (`o` in Vim) or inspect sibling tasks, an immediate auto-jump tears them away from the file.
- **Adjustment 1 (Vim Jump List Escape Hatch):** Before executing any auto-jump, `bob-navigation-hotkeys` must push the active file and cursor position onto Vim's jump history (`recordVimJump`). If Bryan ever completes an action and realizes *"Wait, I wanted to stay on this note"*, pressing **`<C-o>`** in Vim normal mode instantly returns him to the exact file and line he just acted on.

### 4.2 False Triggers Outside Review Mode
- **Risk:** Accidental jumps occurring during normal daytime editing at 2:00 PM when checking off a task.
- **Adjustment 2 (Bulletproof Landing Validation):** Auto-advance must ONLY fire if:
  1. `this.reviewLanding` is active.
  2. `landing.day === todayText` (same calendar day).
  3. `activeFile.path === landing.path`.
  4. `activeEditor.getLine(cursor.line) === landing.text` (cursor is still on the exact line landed on).
  If the user moved the cursor or switched files, `reviewLanding` is invalidated.

### 4.3 Boundary Blindness & Review Exhaustion
- **Risk:** Silently leaping from PRE habit checklists into backlog triage, or hanging when the last item in the entire review is completed.
- **Adjustment 3 (Tier Boundary Notices):** When crossing a tier boundary (e.g. PRE $\to$ NEW or commitments $\to$ ROTTEN), the landing notice must combine the action completion line with the boundary header:
  ```text
  ✓ Done · Morning habit checklist
  ──────────────────────────────────────
  Commitments next · 14 tasks due
  [1/14] NEW · Personal/Health · Schedule dentist
  ```
- **Adjustment 4 (Review Complete State):** Resolving the final item in the entire queue must cleanly present the canonical review completion banner:
  ```text
  ✓ Done · Final review chore
  ──────────────────────────────────────
  🎉 GTD Morning Review Complete — 0 tasks due
  ```

---

## 5. Technical Implementation Architecture

### 5.1 Centralized Engine in `bob-navigation-hotkeys`
All walk state (`reviewLanding`, `reviewAnchor`, `jumpToDueTask`) lives in `bob-navigation-hotkeys`. It should expose an updated API (`version: 3`):

```javascript
// In bob-navigation-hotkeys/src/480-review-jump-and-nav-api.js
return Object.freeze({
  version: 3,
  isReviewLanding(editor) {
    return plugin.isReviewLandingActive(editor);
  },
  async advanceReviewWalkIfLanding(editor, options = {}) {
    if (!plugin.isReviewLandingActive(editor)) return false;
    return await plugin.advanceReviewWalkFromAction(editor, options);
  },
  claimReviewWalkCompletion(editor) {
    return plugin.claimReviewWalkCompletion(editor);
  }
});
```

### 5.2 Unified Advance Flow (`advanceReviewWalkFromAction`)
In `bob-navigation-hotkeys/src/535-plugin-review-checklist-walk.js`:
1. Build `reviewAnchor` adding the current task's unique key to `handledKeys`.
2. Clear `this.reviewLanding = null`.
3. Push current location to Vim jump list (`recordVimJump`).
4. Call `await this.jumpToDueTask(1, { fromStamp: this.reviewAnchor, actionNotice: options.notice })`.

### 5.3 Cross-Plugin Integration Hooks
1. **`task-status-cycler` (`<ctrl+enter>`):** Remove the `tier === "pre" || tier === "post"` filter in `claimReviewWalkCtrlEnter`. For all tiers, let Hotkeys claim the completion, execute `cycler.completeTaskAtCursor(editor)`, and call `advanceReviewWalkFromAction`.
2. **`block-id-prompt` (`<ctrl+shift+enter>`):** At the end of `applyPomodoroTaskLink`, feature-detect `navApi.version >= 3` and invoke `navApi.advanceReviewWalkIfLanding(source.editor, { action: "today" })`.
3. **`TaskCardModal` (`<ctrl+shift+p>`):** On modal close, check `intentRemovesFromReviewStack(intent)`. If true and on a review landing, invoke `advanceReviewWalkFromAction`.
4. **`toggleTaskLaneOnTasks` (`Alt+N`):** If on a review landing, invoke `advanceReviewWalkFromAction`.

---

## 6. Summary Comparison Matrix

| Keymap / Action | Context | Current Behavior | Proposed New Behavior | Recovery / Escape Hatch |
| :--- | :--- | :--- | :--- | :--- |
| **`<ctrl+enter>`** | On PRE checklist item | Completes row $\to$ jumps within PRE; halts at PRE end | Completes row $\to$ jumps within PRE; **advances to NEW** at PRE end | `<C-o>` jumps back |
| **`<ctrl+enter>`** | On NEW / PENDING / NEXT / ROTTEN | Toggles checkbox in place; stays on task | **Completes task $\to$ auto-jumps to next due task** | `<C-o>` jumps back; reopen (`[x]` $\to$ `[ ]`) stays |
| **`<ctrl+shift+enter>`** | On open task | Links to Today's Pomodoro; stays on task | **Links to Today $\to$ auto-jumps to next due task** | `<C-o>` jumps back; unlinking stays |
| **`<ctrl+shift+p>` $\to$ Roll/Cancel** | On open task | Writes roll/cancel; closes card; stays on task | **Writes roll/cancel $\to$ auto-jumps to next due task** | `<C-o>` jumps back; Esc/q cancels without jump |
| **`<ctrl+shift+p>` $\to$ No-roll property** | On open task | Modifies property; stays on task | **Stays on task** (no jump) | Unchanged |
| **`Alt+N` (toggle lane)** | On Pending/Next or Ready | Releases or commits lane; stays on task | **Releases/commits $\to$ auto-jumps to next due task** | `<C-o>` jumps back |
| **`Ctrl+Alt+F`** | On open task | Keeps task $\to$ jumps to next task | **Keeps task $\to$ jumps to next task** (Already works) | Use `Alt+F` to keep and stay |
| **`Alt+F`** | On open task | Keeps task; stays on task | **Keeps task; stays on task** (Preserved) | Canonical "stay" keymap |
| **`Alt+[` / `Alt+]`** | On open task | Cycles status in place | **Cycles status in place** (No jump) | Explorable, multi-stroke safe |

The full detailed report is written and permanently registered in the research sidecar at [`research:202610/gtd_review_keymap_auto_advance__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/research/202610/gtd_review_keymap_auto_advance__gem.md) (artifact ref `file:explicit:1deb5581160754813670db89`).

Finalizer declaration successfully submitted and accepted for `commit` (`docs(research): add gtd review keymap auto advance investigation report` on `repo-9960e404c77f`).
