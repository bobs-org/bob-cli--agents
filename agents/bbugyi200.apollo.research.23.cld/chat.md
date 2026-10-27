# Chat History - ace-run (research.23.cld)

- **TIMESTAMP:** 2026-10-18 11:49:58 EDT
- **MODEL:** claude/opus
- **AGENT:** research.23.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261018_112744.md`

## Prompt

%id(cld, clan=research.23)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 4-researcher swarm.
The other researchers, `research.23.cdx`, `research.23.grk`, `research.23.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

Can you help me review recent changes to Obsidian (see the
https://obsidian.md/changelog/ ChangeLog) that I just got access to by upgrading
Obsidian on my macbook (I think I went from v1.12 to v.1.14?)? Think hard about what I
would actually find useful based on my setup. End your analysis with a ranked list of
new features that you think I should be aware of / consider adopting in some way. 
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

I've pulled the full 1.12–1.14 changelog and I'm now mapping it against your vault config and plugins to see what's actually relevant.

Mapping your plugins next: they register custom `obsidian://` URI handlers and shell out to `bob`, so I'm finding out which callers depend on them.

Checking how `bob plugins sync` currently restarts Obsidian. The new CLI's `plugin:reload` might let it skip the full restart.

Looking at how ref `status` syncs, to decide whether a Bases kanban could safely let you drag cards to change it.

Found Obsidian Headless docs, which could matter a lot for your Linux servers. Reading them now.

Checking whether your old Obsidian Sync setup used the `ob` headless client. Then I'll move on to the Mac-side details.

The Obsidian CLI works over SSH from this server to your Mac. I'll run a few read-only checks (error log, help listing) to see how your plugins are doing on 1.14.4.

Nearly done gathering facts. Checking two last help pages (opening files outside the vault, and the image viewer/Vim commands), then I'll write the report.

Writing the report now. First, one quick check of the exact Bases YAML for kanban views so the example snippet is accurate.

Writing the report file now.

Report written. Registering it as a SASE artifact.

I've written the report and registered it as a snapshot (`research:202610/obsidian_1_12_to_1_14_upgrade_review__cld.md`).

**Your version.** Your Mac is on Obsidian 1.14.4 (installer 1.14.4) on macOS 26.5. The Obsidian command-line tool's (CLI's) link was created May 28, and the binary it points to first shipped in 1.12.7. So you've had the CLI since late May. I can't tell whether any 1.13.x version ran in between, so I treated all of 1.13.0–1.14.4 as new.

**Main findings:**
- **Bases Kanban (1.14) fits you best.** `projects.base` and `refs.base` already group by `status`, so a board is a few lines of YAML (example in the report). The catch is that bob owns `status` in two places:
  - **Projects:** dragging a card to `done` gets undone by `bob projects sync`. Limit the board to `wip` and `waiting`.
  - **Refs:** dragging changes status without the reading task, and `bob ref sync` reports that as a conflict. Use that board only for viewing.
  - **Everywhere:** don't group by folder, because dragging would move the note. Don't use the board's "New" buttons either; they create notes without `parent` frontmatter.
- **The Obsidian CLI works over SSH from apollo to your Mac.** `ssh mac obsidian version`, `plugins:enabled` and `dev:errors` all worked. That gives agents a way to check `bob-plugins` changes in the real app (reload a plugin, then read errors). It could also replace the AppleScript quit-and-relaunch of Obsidian in `scripts/install_all`. This is a 1.12 feature, but it's the most useful thing I found.
- **The upgrade looks low-risk for your plugins.** The app's underlying Electron and CodeMirror engines both got major upgrades. Still, `dev:errors` shows nothing with all 16 community plugins enabled, and none of the breaking changes touch your snippets or plugins.

**Ranked list:**
1. **Bases Kanban, Group menu and collapsible groups (1.14):** adopt, with the limits above.
2. **CLI over SSH as an agent check loop:** adopt. Not new in this upgrade, but the highest leverage.
3. **Fixes for a vault written from outside Obsidian (1.13.4–1.14.4):** be aware. These include a race that could leave files stuck unsaved, settings files now fully saved on quit (yours are git-synced), lag from background property updates, and a memory leak.
4. **Vim and keyboard:**
   - Ctrl-N/Ctrl-P now move through all built-in suggestion lists, matching your bob pickers. The successor picker is the one that doesn't support them yet.
   - Settings can be navigated with Vim keys.
   - Images can be edited from the keyboard, with new `:image grow`, `:image shrink` and `:image reset` commands.
5. **Open `.md` files from outside the vault, plus Quick Look (1.14):** handy for reading research reports and plans without importing them into `~/bob`.
6. **Plugin API changes:** mostly be aware. Test your Vim mappings by hand once. Optionally move bob-articles' 5 settings to the new declarative settings API so they show up in Settings search.
7. **Search:** better ranking for matches at the start of words, full-path matching, and `-folder` exclusion.
8. **Image viewer and resizing.**
9. **Font size is now per-device,** plus new font-size commands.
10. **Highlight colors `==🟡…==`:** be aware only. You barely use `==`.

**Skip:** iOS Quick Capture (no iOS device writes to your vault), Mermaid being off by default (no Mermaid blocks in the vault), and the link-confirmation dialog for `obsidian://` URIs (removed in 1.13.6).

All my checks on the Mac were read-only. I didn't test:
- whether `plugin:reload` cleanly re-registers your Vim mappings;
- `dev:screenshot` over SSH;
- what the delete-attachments setting defaults to;
- whether `highlights://` links now ask for confirmation.

Files are in `sase/repos/research/202610`:
- obsidian_1_12_to_1_14_upgrade_review__cld.md
