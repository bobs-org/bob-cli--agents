# Chat History - ace-run (research.4y.gem)

- **TIMESTAMP:** 2026-11-16 09:54:16 EST
- **MODEL:** agy/gemini-4-hydrogen-xhigh
- **AGENT:** research.4y.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261116_093546.md`

## Prompt

%id(gem, clan=research.4y)
%m:agy/gemini-4-hydrogen-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.4y.cdx`, `research.4y.cld`, `research.4y.grk`, `research.4y.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I recently added support for keymaps that are prefixed with `<ctrl+w>` to make it easier
to manage split windows in Obsidian (see the bob-cli-m0 epic bead for context). I would
now like to add support for the new `<ctrl+w>N` keymaps, which should trigger a jump to
the `N`th Obsidian tab.

- `N` should be determined by a hint that is rendered next to each file's name in
  Obsidian's tab title bar.
- The tab that we jump to should remaining in the same vertical window that it was in
  before invoking the `<ctrl+w>N` keymap.
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

Independent research on `<ctrl+w>N` tab jumping and tab-bar hints is complete, written to [obsidian_ctrl_w_tab_jump_hints__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202611/obsidian_ctrl_w_tab_jump_hints__gem.md), and registered as a durable SASE artifact snapshot.

### Artifact Registration
- **Report path:** [obsidian_ctrl_w_tab_jump_hints__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202611/obsidian_ctrl_w_tab_jump_hints__gem.md)
- **Label:** `research:202611/obsidian_ctrl_w_tab_jump_hints__gem.md`
- **Artifact ref / ID:** `file:explicit:7f64d1ba4c88f48b2b5ee876`
- **Stored snapshot path:** [obsidian_ctrl_w_tab_jump_hints__gem-03ed4a1c2ca6.md](file:///home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261116093551/obsidian_ctrl_w_tab_jump_hints__gem-03ed4a1c2ca6.md)
- **Finalizer declaration:** Submitted and accepted (`repo-0965d82c147f` / `sdd:research`).

---

### Summary of Critique & Findings

- **Verdict — good idea:** `bob-cli-m0` (`bob-navigation-hotkeys` v2.83.1) added split focus (`Ctrl+W h`/`l`/`w`), live tab reparenting (`H`/`L`), and vertical split duplication (`v`), but `h`/`l`/`w` can only reach a neighbouring split's *currently selected* tab, while Obsidian's built-in `Cmd+1..9` is unbadged and scoped solely to the active split. Global cross-split `<ctrl+w>N` turns jumping to any background tab in another split (such as `20261115` or `dash` from `sase_blog_contents` in [20261115_171818.png](file:///home/bryan/tmp/screenshots/20261115_171818.png)) into one fluid chord while preserving the split layout.
- **Key risks identified in the codebase and Obsidian internals:**
  1. **Index drift:** Using CSS counters in the tab bar while resolving `<ctrl+w>N` via `workspace.iterateRootLeaves()` can disagree after split creation/reordering; one pure reading-order model must drive both.
  2. **Reflow & forced pauses:** Armed-only badges either force a stop-and-read pause after `Ctrl+W` or shift tab headers horizontally when toggled (`display: none` → `inline-flex`, as seen in `obsidian-tab-numbers`).
  3. **Date-title & flex-layout collision:** Tab 1 in [20261115_171818.png](file:///home/bryan/tmp/screenshots/20261115_171818.png) is named `20261115` (numeric prefix collides with unstyled `1 20261115`), while trailing placement runs into Obsidian's `margin-right: auto` title spacing on short names (`dash`) or crowds `×`.
  4. **Multi-digit `10+` Vim lag:** Waiting to disambiguate `1` vs `10` holds the catch-all keymap `Scope` open and eats or lags follow-up Vim motions like `<ctrl+w>1j`.
  5. **Sidebar focus & deferred tabs:** [267-window-prefix-actions.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/267-window-prefix-actions.js#L439-L510) returns `null` from `snapshotWindowPrefixLayout()` when focus visits a sidebar, and `focusWindowPrefixLeaf()` does not handle `leaf.isDeferred` / `loadIfDeferred()` / `revealLeaf()` the way `activateWorkspaceLeaf()` does in [620-plugin-dash-and-vim-jumps.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/620-plugin-dash-and-vim-jumps.js#L83-L128).

### Justified Requirement Adjustments

1. **Global main-area `1`–`9` in reading order** (`windowPrefixReadingOrder(splits)` + `group.children` left-to-right), excluding sidebars and popout windows — resolving the `"Nth tab"` vs [bob.md](file:///home/bryan/bob/bob.md#L67) `"Nth panel"` ambiguity.
2. **Single-digit `1–9` only** (tabs `10+` stay unbadged; `9` always means tab 9, never "last tab") to keep every jump `0 ms` instant without swallowing `<ctrl+w>1j`.
3. **Whisper-quiet persistent badges that elevate to `--interactive-accent` keycaps at `0 ms` on `Ctrl+W`** (gated on `totalMainAreaTabs >= 2`) for zero reflow and fluent pre-read speed.
4. **Leading-edge micro-keycap inside `.workspace-tab-header-inner`** (`order: -2`, `tabular-nums`, `flex: 0 0 auto`, `pointer-events: none`) so `[1] 📌 20261115` stays legible and separated from numeric filenames and `×`.
5. **In-place lossless activation** (`loadIfDeferred` + `revealLeaf` + `setActiveLeaf(..., { focus: true })` + `scrollIntoView` + scroll preservation, never calling `recordJump`, verifying `leaf.parent` stays unchanged).
6. **Decoupled main-area snapshot** (`snapshotWindowPrefixMainArea`) so tab numbers remain steady when focus temporarily visits a sidebar.
7. **Compact Tier-2 card integration** via split tab-range pills (`1–3`, `4`) and a footer hint (`1–4 jump tab · esc · q cancel`) rather than expanding the 6-row key grid, plus `"Only K tabs (1–K)"` / `"Already on tab N"` nudges.
8. **Held-Ctrl digit acceptance (`Ctrl+W Ctrl+N`) and unhotkeyed palette commands** (`window-focus-tab-1`..`9`), explicitly noting that `<ctrl+w>1..9` claims `digits` reserved in `bob-cli-m0` away from post-prefix Vim counts.

### Recommended Solution

Implement `<ctrl+w>N` inside `plugins/bob-navigation-hotkeys` in `bob-plugins` by extending [266-window-prefix-model.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/266-window-prefix-model.js), [267-window-prefix-actions.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/267-window-prefix-actions.js), [473-window-hint-view.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/473-window-hint-view.js), [687-plugin-window-prefix.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/687-plugin-window-prefix.js), [688-plugin-window-prefix-commands.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/688-plugin-window-prefix-commands.js), and [styles.css](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/styles.css), plus a new `474-window-tab-hints-view.js` pure DOM reconciler (keeping every fragment ≤ 1,000 lines), verified with unit parity tests, light/dark Chromium previews, and real-Obsidian CDP E2E tests on `athena`.
