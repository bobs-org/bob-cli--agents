# Chat History - ace-run (research.53.final)

- **TIMESTAMP:** 2026-10-20 07:43:20 EDT
- **MODEL:** claude/opus
- **AGENT:** research.53.final
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261020_065153.md`

## Prompt

%clan(research.53, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I would like to add support for directed links from one Obsidian task to another.

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
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.53.final %m:@xlarge
%wait:research.53.cdx %wait:research.53.cld %wait:research.53.grk %wait:research.53.mus %wait:research.53.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

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

The researchers' registered reports:

{% for a in wait.artifacts if a.kind == "markdown" and a.label and a.label.startswith("research:") %}
- wait_name={{ a.wait_name }} label={{ a.label }} source_path={{ a.source_path }} path={{ a.path }} ref={{ a.ref }}
{% endfor %}

Month directory (create it if missing):

$(sase repo path research --ensure)/$(date +%Y%m)

Steps:

1. From the registered reports above, identify exactly one report per expected suffix
   in cdx, cld, grk, mus, gem, belonging to this
   dispatch's `research.53.cdx`, `research.53.cld`, `research.53.grk`, `research.53.mus`, `research.53.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.53.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.53.linker`, can find it:

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

I've read all five reports. Next I'm checking the facts they disagree on: stored versus virtual backlinks, the `~`/`~~` grammar, emoji collisions, and keybindings.

Confirmed that `~` and `~~` are free today and that the 🔗 claim is only partly right. Now checking Task Card keys, hotkey bindings, and how BLOCKS chips are indexed.

Git sync merges at the line level and `_conflicts/` is empty, so gem's sync-churn argument is overstated. Now spot-checking the vault survey numbers.

The Mac picker's direction enum stores its sigil as a single `Character`, so a two-character `~~` needs a small type change. Next: what `|` and quotes already mean in capture.

Now checking whether any vault-wide rule forbids writing under closed tasks. That would decide whether a stored mirror on a closed target is allowed.

I have what I need. Moving the five reports into the new `task_relation_links/` directory in my research checkout.

The reports are moved. Now writing the consolidated report.

Report written. Registering it as a durable artifact for the linker.

Registered. Now the final declaration.

I merged the five reports and my own checks into one final report. My recommendation is to build the feature, keep links completely passive, and have only one side of each link written by hand.

**The design:**
- **Where links live:** each task keeps its outgoing links on one line, `🪢 **LINKS:** follow-up of [[x#^a]] • [[y#^b]]`. That line is the only place a link is recorded.
- **Backlinks:** the target task gets a `🪢 **LINKED FROM:**` line that Bob writes and nothing ever reads back. Bob's writers update it straight away and `bob task reconcile` repairs it. The chips are drawn from a live index, so what you see in Obsidian is correct even before reconcile runs.
- **Links never change anything:** a link doesn't block, promote, use up a Pomodoro link, change status or freshness, or count as a review answer. Closed and archived tasks are valid targets, because a link records history.
- **Capture:** `~note:id|"label"` means this task links to that one, and `~~note:id` means that task links to this one. They follow the same rules as `&` and `*`. In the Mac picker, typing a second `~` flips the direction, and ⇧↩ opens a card for the label with suggestions.
- **Obsidian:** the Task Card (Ctrl+Shift+P) gets `l` "Links to…" and `⇧L` "Linked from…", plus Ctrl+Shift+L and Ctrl+Shift+Alt+L as shortcuts. This copies the existing `b` / `⇧B` pattern.

**Changes to your requirements:**
- **`LINKED FROM` instead of `BACKLINKS`:** in Obsidian, "backlinks" means every inbound link.
- **"Always correct" is restated so it can be tested:** the display is always correct, and the stored line catches up by the next Bob write or reconcile, which runs every 15 minutes on the Mac.
- **Both directions in the Task Card:** you only asked for the reverse direction there.
- **Labels are free text** and read from the linking task's side ("follow-up of").

**Where the researchers disagreed:** two of the five (cdx, gem) wanted the backlinks to exist only on screen, with nothing written to the target note. I sided with writing the line, because you asked for a sub-bullet, it matches how BLOCKS already works, and vim, `rg` and agents can only see text. A switch turns it off and falls back to on-screen only without losing anything. I also checked several claims myself:
- **`~` and `~~` are free today.** `bob capture-parse` treats them as plain text, while `=~2` and `x~1` still parse as Pomodoro drop operators.
- **`l` and `⇧L` are unused on the Task Card,** and Ctrl+Shift+L isn't bound in the vault's hotkeys.
- **Your vault already has 660 `- LINKS:` lines,** none of them directly under a task, so the parser must only recognise the bold label directly under a `#task`.
- **I chose 🪢 over 🔗.** All four dependency parsers still accept 🔗 as an old dependency glyph, and it looks like ⛓️ at chip size.
- **mus's "no reverse syntax" idea doesn't work** for a newly captured task, because it has no ID to point at yet.
- **The BLOCKS chips read the Tasks plugin's cache, which can't see links,** so links need their own index. The plugin already has a pattern for that.

**Not verified:** whether Obsidian binds Ctrl+Shift+L by default, and cld's count of about 120 informal task-to-task links. No product code was changed and no tests were run.

**Questions for you:**
- Are the names `LINKS` / `LINKED FROM` and the 🪢 glyph okay?
- Should the backlinks line be written to the target note, or shown on screen only?
- Is it acceptable that archived targets get no stored backlinks line?
- Should "Cancel as duplicate of / merged into / superseded by" ship in the first version?
- Do you want backlink chips to show the reverse wording ("merged from")?
- Should your existing hand-written "Merged into" / "See" bullets be offered for conversion?

The five reports and the final report are in `202610/task_relation_links/` in the research repo. The final report is registered for the linker as `research:202610/task_relation_links/task_relation_links__final.md` (ref `file:explicit:bba79ebf1f312b835991d86a`). The research repo commit was declared and is made by the host after this turn.
