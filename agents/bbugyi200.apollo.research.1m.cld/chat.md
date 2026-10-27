# Chat History - ace-run (research.1m.cld)

- **TIMESTAMP:** 2026-10-15 16:48:25 EDT
- **MODEL:** claude/opus
- **AGENT:** research.1m.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261015_163335.md`

## Prompt

%id(cld, clan=research.1m)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.1m.cdx`, `research.1m.grk`, `research.1m.mus`, `research.1m.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

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
would like to add support for a special mode / filter to the bob-mac-capture app's
reference panel that that only shows reference notes that correspond with PDF files that
are currently opened in the Highlights app. This will allow me to use the reference
panel as a tab-switcher for the Highlights app.

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

I'm reading the tailnet notes so I can check, read-only, which PDFs Highlights actually has open on the Mac.

I'm reading how the refs panel handles scopes, opening, and keys, to see where an "open in Highlights" filter would plug in.

I've got the hotkey plumbing. Next I'm checking which takeover key Bryan actually has set, since that shapes the switcher key I'll recommend.

I have enough evidence. Now I'm writing the report.

The report is written. Now I'm registering it as a durable artifact.

I wrote the report to `sase/repos/research/202610/highlights_tabs_refs_switcher__cld.md` and registered it as `research:202610/highlights_tabs_refs_switcher__cld.md` (id `explicit:b2259202337106eacbd3eaeb`). The commit is declared and happens when this turn ends.

**Verdict: build it.** The Highlights tab bar shows file names, and one of your open tabs is literally `442a6bf5….pdf`, which Bob titles *karpathy/llm-wiki.md*. You already use Bob Refs as a rough tab switcher: 14 of the last 122 opens re-opened a note you had already opened that day. Knowing which PDF is current also puts "act on the PDF I'm reading" one keystroke away, via ⌘Y Copy or ⌘↵ Note.

**How to detect open PDFs.** I tested this read-only on the Mac, with 9 PDFs open in Highlights:
- **Open-file lists won't work.** `lsof` shows no PDFs held open by Highlights, because it reads each file and closes it.
- **AppleScript won't work.** Highlights doesn't support it.
- **Accessibility does.** The visible tab gives its full file path, and the native tab bar lists all 9 tabs by file name, with the selected one marked. The read took 67 ms.
- **Matching tabs to notes is reliable.** All 9 tabs map to exactly one reference note each. Only one file name out of 431 library PDFs appears twice (`harness_engineering.pdf`).

**The real cost is the permission, not the code.** Bob Mac Capture is signed ad hoc and the Mac has no signing certificate. That means every `just install` silently revokes an Accessibility grant, while System Settings still shows it switched on. Fix that first with one long-lived self-signed certificate.

**Changes I'd make to the request:**
- **A "Tabs" scope token, not a separate mode.** ⌘T toggles it in the panel. ⇧⌘O opens it while Highlights is frontmost; that key is free in Highlights. Don't call it "Open": the panel's count already uses that word.
- **Show every open PDF,** including ones with no reference note, as dimmed rows. A switcher that hides tabs can't be trusted.
- **Order like ⌘Tab:** current tab first (with its page number), then most recently used, with the previous tab selected so ↵ flips back.
- **Switch through the existing ↵ open path.** Already-open PDFs get a tab glyph in every scope.
- **Nothing changes reading state.** No `bob-cli` change is needed.
- **Ask for the permission only on first use of Tabs,** never at launch.

**Recommended plan:**
1. Set up stable code signing.
2. Add the matching and ordering logic to the shared core, testable on Linux.
3. Add the Accessibility reader, panel wiring, hotkey, Settings row and README section.
4. Later, optionally: exact recency tracking, and closing tabs from the panel.

**Not verified:** I didn't switch your live tabs, so two things are inferred:
- I assumed re-opening an already-open PDF selects its existing tab rather than opening a duplicate. That is standard macOS document-app behaviour, and your open log is consistent with it.
- I assumed Highlights windows on other Spaces may not be visible to Accessibility; that is commonly reported but untested here.

The report lists a quick check on the Mac for each before merging.
