# Chat History - ace-run (research.3w.final)

- **TIMESTAMP:** 2026-11-09 10:00:28 EST
- **MODEL:** claude/opus
- **AGENT:** research.3w.final
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261109_092439.md`

## Prompt

%clan(research.3w, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I would like to improve the way that we handle done notes with the goal of fixing any
existing bugs, making their management more reliable and intuitive, and making other
improvements where possible and desirable (think hard about what improvements we could
make that I would most likely find useful). I think we use `done/<name>_done.md` files
currently, which works OK I guess. I'm just curious how other systems handle this and
whether there is a better way to approach this problem.

Can you do some research with the goal of helping me with this? End your analysis with a
recommended set of changes that you think I should consider making (or recommend no
changes).]]) %id:research.3w.final %m:@xlarge
%wait:research.3w.cdx %wait:research.3w.cld %wait:research.3w.grk %wait:research.3w.mus %wait:research.3w.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I would like to improve the way that we handle done notes with the goal of fixing any
existing bugs, making their management more reliable and intuitive, and making other
improvements where possible and desirable (think hard about what improvements we could
make that I would most likely find useful). I think we use `done/<name>_done.md` files
currently, which works OK I guess. I'm just curious how other systems handle this and
whether there is a better way to approach this problem.

Can you do some research with the goal of helping me with this? End your analysis with a
recommended set of changes that you think I should consider making (or recommend no
changes).

When you author or carry over Mermaid diagrams, load `/mermaid_diagrams` before
drafting, even when no image or diagrams companion runs. The skill has the shared
figure-selection, styling, and PDF-render review rules. If the provider skill is not
deployed, verify the edited plugin's guide with `sase macro show skill/mermaid_diagrams --format raw` (or
`sase macro show /mermaid_diagrams --format raw`) and use the form this host supports.
This guidance does not enable a companion diagrams agent.

The researchers' registered reports:

{% for a in wait.artifacts if a.kind == "markdown" and a.label and a.label.startswith("research:") %}
- wait_name={{ a.wait_name }} label={{ a.label }} source_path={{ a.source_path }} path={{ a.path }} ref={{ a.ref }}
{% endfor %}

Month directory (create it if missing):

$(sase repo path research --ensure)/$(date +%Y%m)

Steps:

1. From the registered reports above, identify exactly one report per expected suffix
   in cdx, cld, grk, mus, gem, belonging to this
   dispatch's `research.3w.cdx`, `research.3w.cld`, `research.3w.grk`, `research.3w.mus`, `research.3w.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.3w.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.3w.linker`, can find it:

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
├── <name>__mus.md
├── <name>__gem.md
└── <name>__final.md
```

## Response

Reading the five researcher reports; cdx done, now the remaining four.

Read four of five reports; now reading gem, then verifying disputed facts against code and the live vault.

Now my own verification pass, focused on where the reports disagree: the lingering-rows counts, daily-note exposure, open-subtask reachability, and the fence bug.

Still verifying. Key finding so far: grk's "564 stuck notes" is mostly 317 `ref/` notes and 150 daily notes. A naive age rule would archive all of them, so source eligibility has to come first.

Verified the predicate sprawl (7 named + 26 inline checks). Now checking open beads and the period-review docs, then I'll draft.

Confirmed status grouping applies only to area/project notes, which gives a ready-made eligibility rule. A couple more code checks (lock, threshold help) and then I'll write.

Settled the policy questions; running one simulation of the recommended retention rule against the live vault so the report can say what the first run would move.

Writing the figure first and checking that it renders and fits the PDF page.

Too wide (66% fit). Shortening labels and tightening spacing, revision 1 of 2.

Figure passes (825×808 px, 79% fit). Now moving the five reports into the topic directory.

Reports moved (grk's assets kept their original folder name so its image links still resolve unedited). Now writing the consolidated report.

Report written. Registering it as a durable artifact for the linker.

Registration succeeded. Finishing through the SASE final declaration.

I've written the consolidated done-notes report and registered it for the linker (`research:202611/done_notes_archiving/done_notes_archiving__final.md`). The five researcher reports and grk's figure assets are moved into `202611/done_notes_archiving/`; the research repo is committed when this turn ends.

**Recommendation: keep the `done/<stem>_done.md` files, but change the rule that decides what moves into them and make the move safe.** All five researchers reached this independently. It matches Org mode's default design and fits how Bob identifies tasks; a global log, yearly files or in-note `## Archive` sections would cost a migration without fixing anything.

**What's broken:**
- **Wrong notes can be archived.** Nothing stops `bob task archive` from emptying daily notes, `ref/` notes or finished projects; only the count of 10 does. Running `bob task archive -t 1` today (one researcher suggests running it by hand) would sweep in:
  - 317 legacy `^ref` trackers in `ref/` notes;
  - the Event Tasks and `^gtd` row from 150 daily notes, which `bob gcal` would then mark "removed by you";
  - the closed tasks and remaining `^prj` lines of 55 finished projects.
- **Open subtasks get archived with a closed parent** and vanish from every lane. Bob's own close gesture deliberately leaves such subtasks open, so this can happen; no live instances yet.
- **The writer is less safe than Bob's other vault rewriters.** One researcher (cdx) reproduced, in throwaway vaults:
  - a lost concurrent edit;
  - a task duplicated after a failed run was retried;
  - examples inside code blocks being archived as real tasks;
  - a moved link silently pointing at the wrong task.
- **Renaming a note orphans its archive.** One orphan already exists: `done/2026/20260528_day_done.md`.
- **The count-of-10 rule is unpredictable.** Busy notes like `bob.md` lose last evening's work overnight, while 287 closed rows in quieter notes are over 30 days old.
- **Archived `^prj` lines confuse readers.** Two have been archived, and the weekly-review drafts printed stale links for them.
- **There's no way back.** No command restores an archived task, and a task reopened inside `done/` disappears.

**Recommended changes, in order:**
1. **Only active area and project notes feed `done/`.** A finished project is frozen as its own record, so a `^prj` line never moves.
2. **Hold a closed task that still has an open subtask, and skip code blocks and comments.**
3. **Move the archiver onto Bob's shared safe-write path** (locking, stale-file checks, rollback, `--dry-run`, JSON output). Tidy the note's Done section in the same write.
4. **Pair each archive with its note through the frontmatter links**, and rename the archive file when you rename the note.
5. **Replace "flush everything at 10" with "keep the newest 10 closures from the last 7 days."** This is the visible behaviour change and needs a decision record. I simulated it on the vault: the first run would move about 149 tasks out of 37 notes and create 21 new archive files, so preview it with `--dry-run` first.
6. **Group each archive under month headings, add a `bob task restore` command, and add "Open done archive" / "Open source" plugin commands.**

I set aside some researcher claims; the report explains why, including:
- moving finished project notes into an archive folder;
- splitting archives by year;
- nightly commits that only touch frontmatter (none of the last 31 archive runs was one).

**Decisions for you:**
- Is "newest 10 within 7 days" the right window, or should it follow the week (archive anything closed before this week started)?
- Should finished projects keep their 243 closed tasks permanently, or archive them like any other project?
- Should renaming a note also rename its archive file (my pick), or only re-point the link?
