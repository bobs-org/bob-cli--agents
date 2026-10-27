# Chat History - ace-run (research.1k.final)

- **TIMESTAMP:** 2026-10-15 14:46:23 EDT
- **MODEL:** claude/opus
- **AGENT:** research.1k.final
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261015_140531.md`

## Prompt

%clan(research.1k, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I
would like to add a new `bob ref rename` command and a corresponding keymap in the
bob-mac-capture app's ref panel that allows you to rename the currently selected
reference. For example, I would like to use this to rename the
442a6bf555914893e9891c11519de94f.pdf file, which was clearly misnamed.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.1k.final %m:@xlarge
%wait:research.1k.cdx %wait:research.1k.cld %wait:research.1k.grk %wait:research.1k.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 4 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I
would like to add a new `bob ref rename` command and a corresponding keymap in the
bob-mac-capture app's ref panel that allows you to rename the currently selected
reference. For example, I would like to use this to rename the
442a6bf555914893e9891c11519de94f.pdf file, which was clearly misnamed.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.

The researchers' registered reports:

{% for a in wait.artifacts if a.kind == "markdown" and a.label and a.label.startswith("research:") %}
- wait_name={{ a.wait_name }} label={{ a.label }} source_path={{ a.source_path }} path={{ a.path }} ref={{ a.ref }}
{% endfor %}

Month directory (create it if missing):

$(sase repo path research --ensure)/$(date +%Y%m)

Steps:

1. From the registered reports above, identify exactly one report per expected suffix
   in cdx, cld, grk, gem, belonging to this
   dispatch's `research.1k.cdx`, `research.1k.cld`, `research.1k.grk`, `research.1k.gem` dependencies, matching by `wait_name` and the canonical research
   label's existing `__<suffix>.md` suffix. Never reassign suffixes from list order.
   Open the research repo with `/sase_repo`, then read each report through its canonical
   research reference (or the `ref` field's `file:<id>` reference if the original has
   moved) using `sase artifact read`. Do not read predecessor chat transcripts. If the
   records above do not identify exactly one report per expected suffix, stop and report
   the missing or ambiguous input instead of guessing.
2. Research the request yourself, prioritizing gaps, weak evidence, and disagreements
   between the reports.
3. Pick a descriptive stem `<name>` that collides with nothing in the month directory
   (do NOT end the name with `_consolidated` or `_<YYYYmmdd>` or anything similar unless
   it relates to the research topic), create `<month-dir>/<name>/`, and move each report
   inside it as `<name>__<suffix>.md`, preserving its existing suffix. Each report's
   `source_path` is provenance for where it lives in your own opened research checkout;
   resolve its canonical repo-relative path there before moving it. Never modify the
   other agents' checkouts or the stored snapshot recorded at `ref` — only the copy in
   your own checkout moves. Preserve every file and never overwrite: on any collision,
   pick a different stem first.
4. Write the consolidated report to `<name>/<name>__final.md`: merge the strongest findings
   from every report above and your own research, resolve conflicts, cut duplication,
   and add missing critical context without unnecessary length.

   Do not create `<name>/<name>.md`, not even as a placeholder, because the linker
   agent `research.1k.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.1k.linker`, can find it:

   sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

   Use the consolidated report's actual absolute path and its path relative to the
   research repo root, for example `research:202609/<name>/<name>__final.md`. Register
   only the consolidated report, and do not pass `--move`. If registration fails,
   report that failure; do not report the task as fully complete.

Final layout:

```text
<month-dir>/<name>/
├── <name>__cdx.md
├── <name>__cld.md
├── <name>__grk.md
├── <name>__gem.md
└── <name>__final.md
```

## Response

Reading the four researcher reports now (cdx done); next I'll read cld, grk, gem, then verify the key code claims myself.

Now verifying the contested code claims in bob-cli.

The vault matches the reports: the only inbound reference is the `sase.md` reading task, with no daily-note Task Links. Now checking whether any diagnostic ties `id` to the stem.

The Obsidian `rename-current-file` command has no ref-note guard, which is a gap none of the reports proposed closing. Last check: the pre-scan hook's relationship to the locks.

I have what I need. Moving the four reports into the new directory now, then writing the consolidated report.

Report written. Registering it as a durable snapshot for the linker.

Registration succeeded. Submitting the final declaration.

I wrote the consolidated report and registered it for the linker. My recommendation: build `bob ref rename`, but as a safety tool that renames the reference's files while keeping its identity. Fix the naming code that produced the hex filename first, and add the Mac panel second.

**Why it's worth building:** renaming a reference by hand damages the library today. One researcher (cld) reproduced this in a scratch vault, and another (cdx) independently confirmed the highlight problem:
- Renaming the note in Obsidian (the vault's own ⌃⇧6 rename) makes the next scan create a duplicate note and a duplicate reading task.
- A plain `mv` orphans the reading task in `sase.md`.
- On a reference with highlights, every highlight gets a new ID and the old ones are moved to "Removed highlights".

**Changes I'd make to the requirements:**
1. **"Rename" means the filename only.** Keep the frontmatter `id` and the `^ref-442a…` reading-task ID as they are. Two researchers wanted to change them; I sided against that because:
   - Nothing requires `id` to match the filename, and 6 notes already differ.
   - The PDF's embedded marker stores no path, so keeping `id` means the PDF file itself is never rewritten.
   - Today, Task Links and dependencies all point at the `^ref` ID, so keeping it means nothing else needs updating.
   - A full rename that kept both IDs made the next sync plan no work at all.
2. **Fix the namer first.** The gist got a hex name because the URL-based naming doesn't recognise hex IDs. The fix proposed by one report (gem) is wrong: it would name the file `karpathy`, from the previous URL segment, instead of using the title. The report gives the correct rule. Only about 1 in 425 PDFs has this problem, so the fix has more leverage than the rename command.
3. **The first version refuses references that have highlights.** The gist has none, and neither do the other current rename candidates. Supporting them later means adding a small field to the note.
4. **Run it the way `bob task reroll` and `migrate-tasks` already work:** hold the vault-sync lock and the scan lock, make one commit of just the touched files, and sync before and after (`-o` skips the syncs). Without the vault-sync lock, a scheduled sync could commit a half-renamed state, and another machine's scan would then create duplicates.
5. **New: guard Obsidian's rename hotkey for reference notes.** It's the most likely way this damage happens today, and none of the four researchers proposed closing it.
6. **The Mac gesture is a small rename card, not a bare key.** ⌘⇧R or ⌘K → Rename… opens it, with the current filename pre-selected. ⌘⇧R is free in the Refs panel.

**Recommended order:**
1. Namer fix.
2. `bob ref rename` v1.
3. The Obsidian rename guard.
4. The Mac card. Before enabling it, test on the Mac what Highlights does when the PDF is open during a rename. If it later saves to the old filename, the next scan would create a duplicate, and nobody has verified this yet.

For your gist, once the command exists: `bob ref rename 442a6bf555914893e9891c11519de94f karpathy_llm_wiki`. The report's appendix also has a manual `git mv` recipe for fixing it now; that recipe was tested in a scratch vault.

The report is at `202610/bob_ref_rename_command/bob_ref_rename_command__final.md`, alongside the four researcher reports, which I moved into the same folder. The research repo commit is declared and will land when this turn ends.
