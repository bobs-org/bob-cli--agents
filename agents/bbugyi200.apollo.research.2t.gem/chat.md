# Chat History - ace-run (research.2t.gem)

- **TIMESTAMP:** 2026-10-29 14:38:32 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.2t.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261029_142426.md`

## Prompt

%id(gem, clan=research.2t)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.2t.cdx`, `research.2t.cld`, `research.2t.grk`, `research.2t.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I recently came to the realization that pomodoro themes are really just "task types" in
disguise. I think we should make this more explicit and improve / automate the
experience of working with task types a bit more.

- We should rename the "pomodoro theme" glossary entry to "task type" and update it
  accordingly.
- MOTIVATION:
  - Even though I would like to continue to support ad-hoc themes (with a warning) and
    themes recommended by productivity research, I think this is still supported well
    after this change. For example, using projects like we use "themes" today by putting
    all tasks for a specific project in their own task type pomodoros and then merging
    those pomodoros (the project name then renders on the pomodoro line). We will want
    to add better support for duplicate task type pomodoros for this use-case, but that
    can be considered out-of-scope for now.
  - The name "task types" also just seems to be a good match for this feature (tasks are
    like issues in an issue tracker, most of which support types, and the themes I
    currently use look a lot like types).
- IMPROVEMENTS:
  - Let's start giving every task a type by default. This should be configurable
    (configure mine to be `CHORE` in my chezmoi repo).
  - We need to make sure that a task's type (implicit or explicit) is always consistent
    with any current / future task links associated with that task. Namely:
    - When we update the task type via the Obsidian task card, we should move any task
      links for that task to existing task type pomodoros for that type if any exist in
      the current daily file; otherwise, we should create a new task type pomodoro for
      that type and add the task to that pomodoro.
    - When moving a task link to a different pomodoro (via the `<ctrl+shift+m>` Obsidian
      keymap or the bob-mac-capture app, for example), if that pomodoro has a different
      type than the task that is being moved, we should update the `type` task property
      for that task appropriately.
  - When adding new task links via the bob-mac-capture app , we should always use the
    suggested task type for that task by default (we currently always add the task link
    to the current/next pomodoro). If the `#type` suffix syntax is used to specify the
    `type` pomodoro block, we should update the `task` property for that task if
    necessary.
  - We should start allowing users to explicitly set exempt task types. I sometimes use
    the `PLAN` task type, for example, in the middle of the day to work a planning task
    that breaks down a project more. I should be allowed to give that task a
    `[type::PLAN]` property.
  - I don't like the way that we currently render the `type` task property in Obsidian
    (as a chip). Instead, let's start altering the `#` symbol that we render for `#task`
    to `#<type>` when the task has the `type` property (e.g. `#BUILD`). This tag should
    be colored appropriately.
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

# Research Summary: Unifying Pomodoro Themes into Task Types

**Researcher:** `research.2t.gem` (`gem`)  
**Report Path:** [`task_types_unification_and_automation__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/task_types_unification_and_automation__gem.md)  
**Registered Artifact:** `research:202610/task_types_unification_and_automation__gem.md`  
- **Artifact ID:** `explicit:0fc42e65474cde74b035bf09`  
- **Storage Snapshot:** `/home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261029142431/task_types_unification_and_automation__gem-6c983d80e8a5.md`

---

### Core Verdict & Architectural Findings

Your intuition is spot on: **Pomodoro themes were task types in disguise all along.** In your live vault, the active vocabulary (`BUILD`, `CHORE`, `FIX`, `MEET`, `PLAN`, `READ`, `WRITE`) comprises standard software engineering work classifications, while 71 out of 77 historical entries were hidden ad-hoc session descriptors.

Inverting the domain ontology—so that **tasks own their type** and **Pomodoros serve as the time containers grouping tasks by type**—simplifies the system, aligns with issue-tracker workflows (GitHub Issues, Linear, SASE beads), and enables cohesive automation across `bob-cli`, `bob-plugins`, `bob-mac-capture`, and dotfiles.

---

### Critical Critique & Plan Adjustments

#### 1. Gating the "Task Card $\rightarrow$ Ledger Relocation" (The Backlog Pollution Hazard)
- **The Hazard:** The prompt suggested: *"When we update the task type via the Obsidian task card, we should move any task links for that task to existing task type pomodoros for that type... otherwise, we should create a new task type pomodoro for that type and add the task to that pomodoro."*
  If applied unconditionally, changing the type of any backlog task in an area or project note (e.g. `sase.md`) would immediately append a new Pomodoro and link it into `YYYYMMDD.md`. This would violate [`decisions:today-is-read-from-the-ledger`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/memory/decisions/today-is-read-from-the-ledger.md) and destroy GTD backlog grooming.
- **The Required Adjustment:** Pomodoro relocation/creation in today's daily file MUST trigger **only if the task already has an active (open) task link in today's ledger**, or if the Task Card was opened directly from a Task Link row. Backlog tasks without active links today simply receive their property update without touching today's daily note.

#### 2. Universal Default Type (`CHORE`) via Dynamic Precedence (No Vault Churn)
- Giving every task a default type (`plan.default_task_type: CHORE`) must be an **evaluator-time fallback in the suggestion ladder**, not a batch write that dirties hundreds of existing notes.
- Explicit `[type:: CHORE]` is written only when overriding a conflicting note default (e.g., in `dev.md`, which defaults to `BUILD`).

#### 3. Moving Task Links (`<ctrl+shift+m>`) $\rightarrow$ Cross-File Property Updates
- Reversing the old "never-writer" policy: moving a task link bullet from `— BUILD` to `— CHORE` updates the task line in its source note.
- If the destination matches the task's inherited default, the explicit `[type:: ...]` override is stripped; if it differs, `[type:: <NEW>]` is written. A toast notice provides transparency for the cross-file write.

#### 4. Bob Mac Capture Routing
- Defaulting task links captured without `#type` to an open Pomodoro matching the task's suggested type (or creating one) eliminates post-capture manual moves.
- Explicit `#type` syntax (e.g. `@sase:id#FIX`) updates the task's intrinsic property. Implementing this in `bob-cli`'s Rust core (`src/native/capture/plan.rs`) automatically updates Bob Mac Capture via its existing JSON contracts without Swift business logic duplication.

#### 5. Exempt Types (`PLAN`)
- Removing the PT13 restriction that banned exempt themes on tasks. Planning is legitimate work; tasks can carry `[type:: PLAN]` (rendered in muted gray) while the `— PLAN` Pomodoro session remains exempt from daily theme budget caps (`plan.max_themes`).

#### 6. Obsidian Visual Redesign: `#<type>` Tag Mark
- Eliminating trailing `[theme:: ...]` chips and altering the `#task` mark into a colored `#<type>` tag (e.g., `#BUILD` in yellow, `#FIX` in red, `#CHORE` in magenta) brings critical context to the front of the line and eliminates trailing visual clutter.
- The raw `[type:: ...]` field is folded away in rendered views.
- Untyped base chores retain the quiet teal `#` glyph by default, allowing explicit and specialized types (`#BUILD`, `#FIX`, `#WRITE`, `#PLAN`) to stand out cleanly.

---

### Recommended Phased Roadmap

1. **Phase 1: SASE Memory & Glossary:** Rename `sase/memory/glossary/pomodoro-theme.md` to `task-type.md` and document the unified specification in `docs/task-types.md`.
2. **Phase 2: Rust Engine (`bob-cli`):** Add `plan.default_task_type`, support `[type:: ...]` syntax, allow exempt types (`PLAN`), and implement type-matching default capture destination routing.
3. **Phase 3: Obsidian Visuals (`bob-ledger-tools`):** Replace `#task` with colored `#<type>` marks in `138-task-tag-marks.js` and fold inline type fields.
4. **Phase 4: Task Card & Keymap (`bob-navigation-hotkeys`):** Implement active-link Pomodoro relocation in Task Card commits and cross-file property synchronization on `<ctrl+shift+m>`.
5. **Phase 5: Bob Mac Capture & Dotfiles:** Validate Bob Mac Capture thin-client contracts and configure `default_task_type: CHORE` in `~/.config/bob/config.yml` via `chezmoi`.

*For detailed architectural specifications, CodeMirror/CSS styling models, and edge-case handling, refer directly to the full research report in [`task_types_unification_and_automation__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/task_types_unification_and_automation__gem.md).*
