# Chat History - ace-run (research.1n.cld)

- **TIMESTAMP:** 2026-10-16 07:26:16 EDT
- **MODEL:** claude/opus
- **AGENT:** research.1n.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261016_070719.md`

## Prompt

%id(cld, clan=research.1n)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.1n.cdx`, `research.1n.grk`, `research.1n.mus`, `research.1n.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We
recently added support to the `bob capture` command and the corresponding
bob-mac-capture app for capture templates (see the bob-cli-7w epic bead for context).
Can you now help me add support for persisting templates to disk automatically when they
are used?

- We should then allow the user to access and modify the templates that have been saved
  in the bob-mac-capture app.
- This should work in a similar way to the capture stash.
  - We should use a new `<ctrl+t>` keymap that allows the user to view/modify saved
    templates.
  - Just like with the stash, we should pop a template when it is selected (it will just
    get re-added when the capture is submitted if the template is used).
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

I'm reading the original templates plan, and next I'll look at how the capture stash is built in bob-cli and bob-mac-capture.

I'm going through the Mac app's stash code (how it's stored and how the picker works) so I can model the templates feature on it.

Still mapping the existing stash UI and the submit path in the Mac app; after that I'll check the bob-cli side.

Now checking the bob-cli side: where bob keeps local state today and how `bob capture` handles templates.

I'm reading the thin-client decision and the CLI rules memory, since the design may add a new bob subcommand.

Next I'm reading the vault conventions memory, since one design option is to store templates in the vault instead of local state.

The installed `bob` predates templates, so I'm building the workspace `bob` to probe the real JSON while I keep reading the code.

Build succeeded (it lives in a shared cache dir); now probing the template parse and expand JSON.

Checking how the Mac editor applies programmatic edits (for undo), then I'll start writing the report.

Performance is a non-issue (~13 ms per debug spawn). I'll quickly check how comparable tools (Raycast clipboard history, org-capture) handle delete/pin, so the report cites real precedents.

I have what I need. Writing the report now.

Cursor offset (57) and line references check out. Registering the artifact now.

I've written the report at `sase/repos/research/202610/saved_capture_templates__cld.md` and registered it as `research:202610/saved_capture_templates__cld.md`.

**Verdict: yes, build it.** The templates plan already listed saved templates as follow-up #5, and your job-application waves bring the same template back every time. A Ctrl-T picker of recently used templates, like the stash, is the right design. I'd change four things, each marked in the report.

**Requirement changes I recommend:**
1. **bob owns the saved templates, not the Mac app.** The stash is Mac-owned because it holds panel drafts. A template is part of the capture language, and the thin-client decision says bob owns that. So:
   - `bob capture` saves the template after each successful real capture to `~/.local/state/bob-cli/capture/templates.json`.
   - A new `bob capture-templates list|show|delete|clear` command serves them. For each template it returns the exact text to insert and its highlighting, so the Mac never parses anything.
   - Captures typed in a terminal get saved too.
2. **Selecting a template hides it instead of deleting it.** It leaves the list while it's in your draft. If the capture succeeds, your edited version replaces it at the top. If you abandon the draft, it comes back unchanged. A literal pop would leave the editor holding the only copy, so a wrong pick, Discard, Ctrl-C, quitting with the draft open, or the planned "Expand template" action (`bob-cli-83`) would silently destroy it.
3. **Deleting is explicit.** Backspace deletes one template and Shift-D deletes all; each needs a second press to confirm, because templates are worth keeping in a way stash drafts aren't.
4. **Ctrl-T also works when you've already pasted rows.** It adds the template on top as one undoable edit. The stash needs an empty editor because restoring replaces the draft; inserting a template only adds text.

**Smaller decisions:**
- **When a template is saved:** only after a successful, non-dry-run capture, and a failed save just warns; it never fails a capture that already wrote the vault.
- **Duplicates:** identical templates merge into one entry automatically.
- **Size:** at most 36 templates, newest first, matching the stash's one-key shortcuts. A `capture.saved_templates` setting can turn saving off.
- **Messages:** right after you insert a template, bob currently says "add a blank line, then one row per capture" even though the blank line is already there. That's the first thing you'd see after every pick, so I propose fixing the wording.
- **Ctrl-T trade-off:** it replaces macOS's transpose-characters shortcut in the editor. `bob-cli-83` should not claim Ctrl-T.

**How it looks:** the picker matches the stash's look, but each row shows the template with bob's own colors: `{0}`, `{1}` and the route in the same colors as the editor, with field count, route, use count and age beside it.

I probed this against a `bob` built from current master (the installed one predates templates). I also compared other designs: a Mac-owned store, keeping templates in the vault, offering them in `@@` completion, and named headers like `@@template:job`. The report explains why each was rejected or deferred. It ends with a two-phase plan (bob first, then the Mac app), edge cases, and the recommended solution.

**Questions for you:**
- **Hide or delete on select?** I recommend hiding, as above. If you'd rather keep "pick, then Discard" as the way to delete a template, a literal pop is simpler, but it loses templates in the cases listed under change 2.
- **Is a shelf on the Mac only enough?** Templates saved on the Mac won't appear in terminals on apollo or athena. Sharing them across machines would mean storing them in the vault, which causes git sync conflicts.
- **Is a 36-template cap fine without pinning?** Pinning (never evicting a template you mark) is listed as a follow-up.
- **Keep "insert on top of pasted rows" in the first version?** It's cheap, but it is an addition to what you asked for.

Sources: [Raycast Clipboard History manual](https://manual.raycast.com/clipboard-history) · [Brett Terpstra on macOS key bindings](https://brettterpstra.com/2023/12/18/macos-keybinding-tricks-the-kill-ring/) · [Apple Cocoa Text Editing guide](https://developer.apple.com/library/mac/documentation/TextFonts/Conceptual/CocoaTextArchitecture/TextEditing/TextEditing.html)
