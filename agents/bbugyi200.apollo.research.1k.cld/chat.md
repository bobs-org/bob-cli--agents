# Chat History - ace-run (research.1k.cld)

- **TIMESTAMP:** 2026-10-15 14:30:51 EDT
- **MODEL:** claude/opus
- **AGENT:** research.1k.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261015_140531.md`

## Prompt

%id(cld, clan=research.1k)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 4-researcher swarm.
The other researchers, `research.1k.cdx`, `research.1k.grk`, `research.1k.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I
would like to add a new `bob ref rename` command and a corresponding keymap in the
bob-mac-capture app's ref panel that allows you to rename the currently selected
reference. For example, I would like to use this to rename the
442a6bf555914893e9891c11519de94f.pdf file, which was clearly misnamed.

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

I'm reading the `bob ref` docs and source. Next I'll find the misnamed PDF in the vault and look at the Mac app's Refs panel.

Three exploration agents reported back. I'm now checking their key claims directly in the source: stem naming, `^h-` ID hashing, path pairing, the dirty guard, and the CLI layout.

I've checked the lock semantics. Last verifications: whether vault-sync calls scan (this decides lock order), the annotation counts on the candidate notes, and the Name Pomodoro prompt.

Still testing the rename scenarios in the scratch vault. The bob binary isn't where I expected, so I'm locating it first.

The full rename verified clean: `writes: none`, the reading task was still found, there were no diagnostics, and the old id still resolves. Next I'll test the failure modes.

I'm on the last experiment, renaming an annotated reference in scratch. The sync tombstoned its highlights, and I'm now counting exactly which IDs changed.

The report is written. Now I'm registering it as an artifact and cleaning up the scratch vault.

I wrote the report and registered it as an artifact (id `explicit:df30b26930496941102456db`, label `research:202610/bob_ref_rename__cld.md`). The research repo commit is declared and lands when this turn ends.

**Report:** `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/sase/repos/research/202610/bob_ref_rename__cld.md`

**Is it a good idea?** Yes for the `bob ref rename` command, mainly as a safety tool. I copied the real gist note, PDF and `sase.md` into a throwaway git vault and tried each way of renaming by hand. Every shortcut damaged the vault:
- **Obsidian's rename** (⌃⇧6, note only): the next scan recreates the old note and adds a second reading task, `^ref-…-2`.
- **A bare `mv`:** the reading task is orphaned (`open_ref_without_task`).
- **An uncommitted rename:** later writing scans refuse to touch the renamed note.
- **Renaming a reference with highlights:** every `^h-` ID changes, because the IDs are hashed from the PDF path. All 8 highlights in my test got new IDs, and the 8 old ones became "Removed highlight" stubs.

The rename that worked moves the files, rewrites the incoming links, updates `source_pdf`, and keeps the frontmatter `id` and the `^ref-…` block ID unchanged. After that, `bob ref sync --dry-run` plans no work, the reading task is still found, and `bob ref find <old id>` still resolves.

**Critique:**
- **It will rarely be needed.** Of 426 modern ref notes, only 1 has an opaque name (this gist) and 3 have generic ones (`README`, `AGENTS`, `demo`). None of the four has any highlights.
- **The real cause is the namer.** `stem_from_url` takes the last URL path segment and nothing stops a hex ID. The multi-URL collection namer already trims hex IDs; the single-URL namer doesn't. Fixing that prevents new cases.
- **The panel key costs the most and should come second.** The Refs panel has no text input besides search, and selection and history are keyed by note path.

**Requirement changes I'm proposing:**
1. "Rename" changes the filename stem only, within the same type folder, for PDF-backed references. Changing the title is separate and can already be done by editing the frontmatter and running `bob ref sync <pdf> -p frontmatter -w`.
2. `id` and `^ref-<slug>` stay unchanged.
3. Version 1 refuses references that have highlights. Re-keying them is a later phase, designed in the report.
4. The command refuses unless the reference is in sync, then makes one revertible commit under the sync and scan locks, and checks afterwards that a dry-run sync plans nothing.
5. Names follow the same rule as `create -N` and must not match any other note's filename anywhere in the vault.
6. The panel key is ⌘E plus a "Rename…" item in the ⌘K menu. Bare letters type into search, Return opens and ⌘R refreshes, so those won't work.
7. The namer fix ships in the same epic.

**Recommended order:**
1. Fix the namer.
2. Add `bob ref rename` with dry-run, JSON output and the checks above.
3. Add the Mac rename card: it runs `bob ref rename -f json`, selects the new path afterwards, and shows bob's errors inline.
4. Add highlight re-keying once you actually need to rename an annotated reference.

**Untested risk:** the PDF being renamed is often open in Highlights. I couldn't find an authoritative answer on what a macOS document app does after another process moves its file. It might write back to the old path and create a duplicate, so the report lists this as an acceptance test on the Mac.

To fix the gist today, Appendix A has a manual recipe I tested in the scratch vault.

Sources:
- [Apple: NSFileCoordinator item(at:didMoveTo:)](https://developer.apple.com/documentation/foundation/nsfilecoordinator/item(at:didmoveto:).md)
- [NSFilePresenter.h (10.8 SDK)](https://jenkins.heirloomcomputing.com/downloads/MacOSX10.8.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFilePresenter.h)
- [Cocoa-dev: moved files, path vs inode](https://lists.apple.com/archives/Cocoa-dev/2006/Jul/msg01768.html)
- [MPU forum: Highlights sidecar Markdown export](https://talk.macpowerusers.com/t/batch-process-annotations-from-pdfs-out-to-obsidian/24470)
- [Highlights on the App Store](https://apps.apple.com/app/id1498912833)
