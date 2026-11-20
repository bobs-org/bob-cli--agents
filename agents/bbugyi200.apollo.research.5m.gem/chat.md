# Chat History - ace-run (research.5m.gem)

- **TIMESTAMP:** 2026-11-20 15:58:29 EST
- **MODEL:** agy/gemini-4-hydrogen-xhigh
- **AGENT:** research.5m.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261120_154428.md`

## Prompt

%id(gem, clan=research.5m)
%m:agy/gemini-4-hydrogen-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5m.cdx`, `research.5m.cld`, `research.5m.grk`, `research.5m.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add a new `<ctrl+j>` keymap to the successor panel shown in Obsidian and
in the capture panel.

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
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
First run `sase repo open research -r "Write this research report"` and use the path it prints as `<research checkout>`. Write this research to a new markdown file under `<research checkout>/202611/`.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path under the opened research checkout and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

I have completed the independent design research and written the full report to [successor_panel_ctrl_j_jump_design__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/research/202611/successor_panel_ctrl_j_jump_design__gem.md).

- **Artifact snapshot registered:** `file:explicit:d05130ee53e48d2ba2a360ce` (`research:202611/successor_panel_ctrl_j_jump_design__gem.md`) at [successor_panel_ctrl_j_jump_design__gem-73e121c26a25.md](file:///home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261120154434/successor_panel_ctrl_j_jump_design__gem-73e121c26a25.md).
- **Final declaration submitted:** `commit` accepted for `sdd:research`.

---

## Critique & Verdict

**Yes — adding `<ctrl+j>` as an orthogonal single-slot jump target (`jumpKey`) is the right design.**
Today Bob pairs *"leave unlinked"* with *"stay on the predecessor / advance `]s`"* and pairs *"pull into Today"* with *"navigate to the successor manually."* Making `<ctrl+j>` toggle an orthogonal single-slot flag rather than an instant-commit shortcut or a 5th mutually exclusive state allows full composition with all four per-offer outcomes (*Leave Open*, *Pull In*, *Done*, *Cancel*) while keeping `Enter`/`Return` as the single commit gesture.

Both successor pickers leave `Ctrl+J` unbound today:
- Obsidian [206-successor-picker-modal.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/206-successor-picker-modal.js) does not bind `Ctrl+J`.
- Mac Capture [`pullInChoiceCommand`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/CaptureKeyCommandRouter.swift#L837-L933) leaves `KeyCode.j` + `.control` unbound (its existing `Ctrl+J` binding is scoped to the main draft editor and Bob Refs).

---

## Justified Adjustments to Requirements

Inspection across [bob-cli](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/capture/cli.rs), [bob-plugins](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/206-successor-picker-modal.js), and [bob-mac-capture](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/CapturePullInChoice.swift) revealed six subtle interactions where a literal implementation would silently pull in unintended tasks, fight `]s`, or land on stale lines:

1. **Fix `0` pull-in + `1` jump commit semantics:** Today `Enter` with `0` marks and `0` verdicts falls back to **pulling in** the highlighted row, and [`createSuccessorPickerApi`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/206-successor-picker-modal.js#L778) rejects `{ picks: [], closes: [] }` as `null`. When `jumpKey` is set, **suppress the `Enter`/`Return` highlight-fallback** (mirroring §12.22 verdicts) and allow `{ picks: [], closes: [], jumpKey }` (`Leave Open & Jump`) as a valid commit.
2. **Capture submit keys (`Cmd+Return`, `Ctrl+Return`, `Return`, `Shift+Return`):** Both `Cmd+Return` and `Ctrl+Return` in the draft set `openAfterCapture = true` (and `Ctrl+Return` inside the Pull-In card does too). Setting `jumpKey` should open Obsidian even on plain **`Return`**, **override `open_notes`** whenever `openAfterCapture` was armed (`Cmd+Return` or `Ctrl+Return`), and keep `Shift+Return` (`Skip`) clear as *"no pull-in, no jump"*.
3. **Park (never auto-advance) Obsidian `]s` review walk:** Closing a `]s` walk landing currently calls [`settleReviewOrigin`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/task-status-cycler/src/140-plugin-vim.js) -> `advanceReviewWalkAfterAnswer`. Following `decisions:task-move-never-advances-the-walk`, call [`parkReviewWalkAfterMove`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/537-plugin-review-move-park.js#L200) *before* focusing the jump target and capture Vim `<C-o>` history so `]s` doesn't yank focus away.
4. **Caller scope & muted rows:** Support `<ctrl+j>` in [task-status-cycler](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/task-status-cycler/src/137-plugin-successor-project.js), parked unlinks ([139-plugin-successor-parked.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/task-status-cycler/src/139-plugin-successor-parked.js)), and [project promotion](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/122-project-promotion-successors.js) (forwarding `line`/`rawLine`/`blockId`), while passing `allowJump: false` in [relation merge](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/429a-relation-merge-commit.js) where rows represent Pomodoro hand-off slots rather than successor tasks.
5. **Single-step `Esc` stays intact:** Unlike `Done`/`Cancel` verdicts, staging only `jumpKey` makes zero vault edits, so it should **not** trigger two-step `Esc` confirmation (`escArmed` / `isEscArmed`).
6. **Input scoping & refusal recovery:** Toggle `Ctrl+J` even when the picker's filter input has focus (`event.preventDefault()` in Obsidian; allowed via [`CapturePanelController`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/CapturePanelController.swift#L3226-L3239) in Mac), ignore `Ctrl+J` inside the inline Cancel Reason editor (`reasonEditKey` / `pullInReasonFocused`), and preserve/prune `jumpKey` in `CapturePullInOutcomes.refresh(offers:)`.

---

## Recommended Solution Summary

1. **`bob-cli` (`-j / --jump-offer <N|KEY>`):** Add `-j / --jump-offer` (unused `-j`, matching `cli_rules.md`) in [`cli.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/capture/cli.rs), resolve the offer probe across *Leave / Pull In / Done / Cancel* in [`pull_in.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/capture/pull_in.rs) and [`offer_verdicts.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/capture/offer_verdicts.rs), and override [`build_open_notes`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/capture/open_notes.rs) post-write with the single destination's final path, line, minted `block_id`, and `<line>:<digest>` `ref` (handling `--inbox-route` relocation automatically).
2. **`bob-mac-capture`:** Track `jumpKey` on [`CapturePullInOutcomes`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-mac-capture/Sources/CaptureCore/CapturePullInOutcomes.swift#L63), update [`CapturePullInChoiceState`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/CapturePullInChoice.swift#L559) commit rules and dynamic footer copy (`"Leave Open & Jump ↩"` / `"Pull In N & Jump ↩"` + lit `arrow.up.forward`), pass `--jump-offer` through [`CapturePanelModel`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift#L4165) (including across `InboxRouteChoice`), and let [`CaptureOpenPlan`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-mac-capture/Sources/CaptureCore/CaptureOpenPlan.swift) + [`NotificationService`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/NotificationService.swift#L219) open `obsidian://bob-open-notes` to the authoritative target.
3. **`bob-plugins`:** Extend [`SuccessorOfferPickerModal`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/206-successor-picker-modal.js) (`v5`), expose post-write focus + [`flashBobOpenNotesLandingLine`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/676-plugin-open-notes-uri.js#L500) (`.bob-landing-flash` in [`styles.css`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/styles.css#L129-L150)) + walk parking on [`createDependencyNavApi`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/480-review-jump-and-nav-api.js), and resolve post-edit line positions in [`planAndApplySuccessorsNow`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/task-status-cycler/src/137-plugin-successor-project.js) after all link/verdict mutations finish.
4. **UI Polish:** Keep action glyphs (`□` / `☑` / `✓` / `⊘`) on the left, render a right-side accent `↗ Jump` capsule + 2px leading accent rail, show an off-filter warning in the status strip if the jump target is filtered out, and flash the focused line upon arrival in Obsidian.

See [successor_panel_ctrl_j_jump_design__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/research/202611/successor_panel_ctrl_j_jump_design__gem.md) for the complete cross-repo design, visual state matrix, and verification plan.
