# Chat History - ace-run (research.4y.cld)

- **TIMESTAMP:** 2026-11-16 10:04:51 EST
- **MODEL:** claude/opus
- **AGENT:** research.4y.cld
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261116_093546.md`

## Prompt

%id(cld, clan=research.4y)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.4y.cdx`, `research.4y.grk`, `research.4y.mus`, `research.4y.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

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
`__cld` suffix, i.e. `<stem>__cld.md` (double underscore before the
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

Reading the Ctrl+W epic's plan and prior research first, then I'll look at the plugin code in bob-plugins.

Reading the shipped window-prefix fragments in bob-navigation-hotkeys now.

Checking the vault's vimrc and existing tab maps, then I'll look at prior art (Obsidian's native Go-to-tab, jump-to-link hints).

Still researching: I'll render the shipped hint with the repo's preview harness so I can design the tab badges to match it.

Rendered the shipped card for reference. Now reading the window-prefix CSS so the tab badges can reuse its tokens.

Pulling Obsidian 1.15.1's own `app.css` from athena to get the real tab-header DOM and metrics.

Running a short real-Obsidian probe on athena next (tab-header DOM, native "Go to tab" scope, mock badge screenshots) — reading the harness helpers first.

Fetched the real-Obsidian acceptance shots. Next: checking the m0.1 spike verdict for facts I can reuse (deferred leaves, focus behavior) before writing my own athena probe.

Spike facts confirm `loadIfDeferred` exists and that `selectTab` resets scroll after a reparent. Next I'm writing a short probe and running it against real Obsidian on athena.

Probe ran cleanly against real Obsidian (nav 2.83.1). Reviewing the screenshots now.

Tab-bar comparison strips look good in both themes. Checking the many-tabs and stacked-tab shots next.

Many-tab and stacked layouts both hold up; numerals stay visible after titles collapse. Adding one more probe pass that mocks the card changes and the jump flash in real Obsidian.

Real-Obsidian evidence is in: the mock card, the jump frame, and confirmation that native Go-to-tab is group-local. Checking the research repo's conventions for image assets before I write.

Found direct prior art: an Obsidian "Tab Numbers" plugin. Opening its repo to see how it renders the badges.

Prior art confirmed (hold-modifier inline badges, per-split, 1–8). Cleaning up the athena scratch run, then preparing the report figures.

Figures are composed and reviewed. Quick check of fragment numbering so the implementation guidance names real slots.

Facts confirmed (Go-to-tab #3 from the right split lands on the right split's 3rd tab, not the global 3rd). Writing the report and its figures now.

Writing the report file now.

Two phrases in the draft are muddled (the `g1…` aside in Adjustment 5, and a confusing clause in alternative D). Fixing both.

Report written (~6.2k words, 4 figures). Reading the artifacts reference memory before registering it.

Registered as `file:explicit:a509adf38b97c54a171251d2`. Now adding the `DISCOVERED ISSUE` note to the in-progress epic.

Note added. Finishing the turn through `/sase_final`.

I wrote the report, registered it, and declared it for commit. My recommendation is to build `Ctrl+W 1`–`9`, with two changes to what you asked for: the tab numbers stay visible all the time as quiet digits, and only the first nine tabs get one.

I tested the details in real Obsidian 1.15.1 on athena, using a throwaway vault (never `~/bob`), and took the report's four figures from that run.

**Is it a good idea?** Yes. It fills the one gap the window prefix left open:
- **Obsidian's own Go-to-tab is per-split.** I confirmed `Cmd+1…8` and `Cmd+9` only count tabs in the focused split. From the right split, `goto-tab-3` lands on that split's 3rd tab, not the 3rd tab overall.
- **Nothing reaches an unselected tab in the other split in one gesture today.** `Ctrl+W 5` would.
- **It's also Vim's own idea.** Vim's `N CTRL-W w` jumps to window N, numbered top-left to bottom-right, and an Obsidian tab is the closest thing to a Vim window.

**Recommended design:**
- **Numbering:** one global sequence. Splits go in the same order `Ctrl+W w` already cycles, then tabs left to right within each split. Only 1–9 get a number; `0` is reserved.
- **The hint:** a quiet digit in front of each file name, in the tab's normally hidden icon slot. It turns into an accent key cap when the `Ctrl+W` card appears, and the tab you're on gets a hollow cap. It's drawn with pure CSS, so the tab bar never shifts.
- **The jump:** the tab is selected inside its own split and focused there; it never moves. I confirmed the tab stays in its split, the other split keeps its tab, the editor gets focus, and scroll is kept (3028 px before and after). The ring pulses on that split and the number flashes for 220 ms.
- **Edge cases:** pressing your current tab's number just pulses. A number with no tab keeps the prefix armed and says "No tab 7 · 6 tabs".
- **The card:** each split pill shows its range of numbers (`1–3`, `4–6`) instead of a bare tab count; the probe showed a bare `3` reads as tab 3. One new row says `1–6 # jump to that tab · it stays in its split`.

**Changes to your requirements (all called out in the report):**
- **Always-visible numbers instead of showing them only while armed.** Showing them only on `Ctrl+W` slides every title 21 px on every press, including a plain `Ctrl+W l`, and you can't pick a target before pressing. The cost is 21 px of title per tab.
- **Digits now mean tabs.** The original Ctrl+W plan had reserved them for "numbered splits"; `h`/`l`/`w` already reach any split quickly.
- **Numbers are hidden where they can't work:** on Linux while `Ctrl+W` stays Close tab, when there's only one tab, and in sidebars and popouts.
- **`Ctrl+W ⇧N` ("bring tab N here") is reserved for later.** It matches `h`/`H`, but you wanted the tab to stay put, so it's not in v1.
- **Optional palette commands "Focus tab 1–9"**, with no default hotkeys.

**Side finding:** in Obsidian 1.15.1 `selectedTab` doesn't exist on a tab group (`currentTab` is a number). Because of that, the shipped `Ctrl+W` code never puts the other split's previously selected tab back after a failed move. It's low impact, failure path only. I added this as a `DISCOVERED ISSUE` note on the `bob-cli-m0` epic rather than filing a new task bead, because the bug is in that epic's code.

**Questions for you:**
- Do you want always-visible numbers (I recommend this) or numbers that appear only after `Ctrl+W`?
- Should the caps light up with the card after 300 ms (I recommend this) or immediately?
- Should `0` stay reserved, or mean the 10th tab or the previous tab?
- Should `Cmd+1–9` be rebound to the global numbering? I'd keep the native behaviour.

The registered snapshot is `file:explicit:a509adf38b97c54a171251d2`. The host will commit the report and its four PNG figures after this turn ends.

Files are in `sase/repos/research/202611/`:
- `obsidian_ctrl_w_tab_numbers__cld.md`
- `obsidian_ctrl_w_tab_numbers__cld_tabbar.png`
- `obsidian_ctrl_w_tab_numbers__cld_card.png`
- `obsidian_ctrl_w_tab_numbers__cld_jump.png`
- `obsidian_ctrl_w_tab_numbers__cld_crowded.png`

Sources:
- [emacs-winum](https://github.com/deb0ch/emacs-winum) and its [MELPA readme](https://melpa.mirrorservice.org/winum-readme.txt)
- [nvim-window-picker README](https://github.com/s1n7ax/nvim-window-picker/blob/main/README.md)
- [Tab Numbers community plugin listing](https://community.obsidian.md/plugins/tab-numbers)
