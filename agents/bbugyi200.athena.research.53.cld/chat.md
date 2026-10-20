# Chat History - ace-run (research.53.cld)

- **TIMESTAMP:** 2026-10-20 07:20:26 EDT
- **MODEL:** claude/opus
- **AGENT:** research.53.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261020_065153.md`

## Prompt

%id(cld, clan=research.53)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.53.cdx`, `research.53.grk`, `research.53.mus`, `research.53.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add support for directed links from one Obsidian task to another.

- I was thinking that we could display these links via a new `LINKS` task sub-bullet or
  somethiing like that.
- Tasks should also track their backlinks (via a new `BACKLINKS` sub-bullet?), which
  must always stay consistent and correct (i.e. this field needs to be kept up-to-date
  automatically somehow).
- I need to be able to easily specify links when capturing new tasks in the
  bob-mac-capture app. I was thinking I could use a new `~` syntax for that which
  triggers a completion menu / search interfact for other Obsidian tasks (which we will
  link the current task to).
- We also need a way to specify that another task should link to the current task in
  both Obsidian (via the `<ctrl+shift+p>` keymap?) and in the bob-mac-capture app (via a
  new `~~` syntax maybe?).
- The user should be able to specify an optional relation / link description when adding
  a link from one task to another.
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

Starting by mapping the existing dependency-link machinery (Depends-On/BLOCKS lines, `&`/`*` capture sigils, Ctrl+Shift+P Task Card), since the feature you want lives right next to it.

Good coverage from the five sub-investigations. Now checking a few specifics myself: hotkey availability, archive link rewriting, the footer verb for relationship captures, and the CLI rules memory.

Enough evidence gathered. Spot-checking a few citations before writing the report.

Filename is free. Writing the report.

Report written. Registering it as a durable artifact.

I've written the research report and registered it as artifact `research:202610/task_cross_links_linked_from__cld.md`. The host will commit it to the research repo after this turn.

**Verdict: build it, and keep it inert.** Your vault already shows the need: about 120 hand-written task-to-task links outside dependency lines. That includes 28 "Merged into" / "Merged from" lines, which are two-way links you keep in sync by hand, plus 218 "See [[…]]" lines. Obsidian's native backlinks pane can't stand in for this, because 2,222 Pomodoro links from daily notes drown out everything else. The pattern you need already exists: DEPENDS ON is the line you write, and BLOCKS is a generated copy on the other task that is never read back. LINKS should reuse that machinery rather than become a new subsystem. The main risk is links slowly gaining behaviour; the design forbids them from blocking, promoting, being consumed, or changing any status.

**Changes I recommend to your spec:**
1. **Call the reverse line `LINKED FROM`, not `BACKLINKS`.** In Obsidian, "backlinks" means every inbound link, but this line deliberately excludes Pomodoro links, dependency links and embeds.
2. **Redefine "always consistent".** It can't be met literally with git sync, edits made outside Obsidian, and read-only `done/` archives. Instead:
   - What you see is always live, because the chips are built from an index.
   - The stored line is regenerated from all LINKS lines; every Bob writer updates it immediately, and `bob task reconcile` heals any drift.
   - Mirrors are never written into `done/` or the previous daily note.
3. **One line per task, joined with ` • `**, like DEPENDS ON, rather than one bullet per link. Separate bullets holding a bare link are exactly what the existing Pomodoro link and close/strike handlers would grab.
4. **Use the 🪢 emoji, never 🔗.** All four dependency parsers already accept 🔗 as an old DEPENDS ON variant.
5. **Labels are optional free text, written from the linking task's side.** For example, `follow-up of [[X]]`, which matches how you already write these. Pickers suggest labels you've used before, so the vocabulary doesn't sprawl.
6. **Closed and archived tasks can be link targets**, unlike dependencies, since "follow-up of" and "duplicate of" usually point at finished work.
7. **Ctrl+Shift+P should cover both directions.** Add rows `l` (Links to…) and `⇧L` (Linked from…), plus Ctrl+Shift+L and Ctrl+Shift+Alt+L, mirroring the existing `b` / `⇧B` pair. Neither chord is bound in your vault's `hotkeys.json` or any bob plugin; I haven't checked Obsidian's own defaults.
8. **Capture syntax:** `~note:id|label` means "this task links to that one", and `~~note:id|"multi word"` means "that one links to this". There are guards so `~/path`, `~5m` and `~~strikethrough~~` stay plain text, and `\~` escapes. A standalone `~` doesn't clash with today's grammar: a test draft containing `~work:foo` parsed as plain text. The existing "`~` drops" meaning only applies inside `x` / `=` tokens. No new CLI command is needed, because capture's existing-task mode (`@route+id`) already covers linking two existing tasks.
9. **Next step after the basics:** add "Cancel as duplicate of / merged into / superseded by…" to the Task Card's cancel stage. That's where most of your hand-written links come from today.

**Recommended build order:** write the contract and test vectors first. Then make every parser in bob-cli and the plugins ignore the new lines before anything writes them. Then the Rust core and capture, then chips, the Obsidian keys and the Mac picker. The report includes mock-ups of the vault lines, chips, Task Card, both pickers and the label prompt, plus a table of edge cases. It ends with five questions for you:
- Are you happy with the `LINKED FROM` name?
- Is "no stored copy on archived targets, live chips only" acceptable?
- Should the cancel-stage shortcut ship in the first version?
- Do you want target-side wording on chips, such as "merged from"?
- Should your existing hand-written link bullets be converted, after a dry run?
