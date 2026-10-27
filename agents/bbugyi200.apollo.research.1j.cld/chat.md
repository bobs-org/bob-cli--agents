# Chat History - ace-run (research.1j.cld)

- **TIMESTAMP:** 2026-10-15 13:05:43 EDT
- **MODEL:** claude/opus
- **AGENT:** research.1j.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261015_124457.md`

## Prompt

%id(cld, clan=research.1j)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 4-researcher swarm.
The other researchers, `research.1j.cdx`, `research.1j.grk`, `research.1j.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__gem.md`. Your report will end in `__cld.md`.

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
want to add support to the `bob capture` command and the corresponding bob-mac-capture
app for defining a template as the first input of a bulk capture.

- Subsequent capture inputs in that bulk capture should then be treated as templates for
  the first capture input.
- For example, consider the following bulk capture using the new syntax that I was
  thinking of using (think hard about what the best syntax is for this functionality):

  ```
  Apply to {0}! @job_2026_apply_29:{1}
  - **URL**: {2}

  Foobar foo http://foobar.com/career/some_foo_job

  Bazbuz baz http://bazbuz.com/career/some_baz_job
  ```

- After this change, that should be equivalent to the following:

  ```
  Apply to Foobar! @job_2026_apply_29:foo
  - **URL**: http://foobar.com/career/some_foo_job

  Apply to Bazbuz! @job_2026_apply_29:baz
  - **URL**: http://bazbuz.com/career/some_baz_job
  ```

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

I'm reading the capture grammar docs and code to see where a template feature would fit. Next I'll look at the parser, the mac app, and `capture-parse`/`capture-rewrite`.

Opening the Mac capture app repo to see how drafts flow through it.

Still mapping the bob-cli parse pipeline: I'm tracing where `bob capture`, `capture-parse`, and `capture-complete` read the draft, so I can see where a template-expansion step would plug in.

Checking an existing `{name}` placeholder convention I found in bob-cli (the listen-command template) so the proposed syntax stays consistent.

Now looking at Bryan's actual vault to see how job-application tasks are captured today (frequency, shape), which tells me how much a template would help.

Quick check of the vault for literal `{N}` text in tasks, to size the backward-compatibility risk of treating `{N}` as a placeholder.

The vault shows Bryan already uses a brace "alternation" syntax (`%{A | B}`) in his SASE xprompts. That's a fan-out precedent worth checking for consistency, so I'll look at it.

Found useful precedent in Bryan's sase macros: legacy `{N}` placeholders there are 1-indexed, and code zones stay literal. Checking whether bob's own grammar already treats inline code as literal.

Checking the research note Bryan used for the last application wave, since its format (table vs list) tells me which row syntax real pastes would use.

I have enough on the design space. Now verifying a few implementation details to cite: the quote parser to reuse, and where completion/rewrite read the draft.

Gathering exact line numbers for the citations in the report.

Writing the report now.

Fixing one inaccurate claim (plan-budget warnings *are* shown, via the Mac budget meter) and verifying the zsh brace claim.

Report written. Registering it as a durable artifact.

I wrote the report and registered it as an artifact (`file:explicit:4c94d3812eb4e34552560eb7`, label `research:202610/bulk_capture_templates__cld.md`). The host commits it to the research repo when this turn ends.

**Report:** `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/sase/repos/research/202610/bulk_capture_templates__cld.md`

**Is it a good idea?** Yes, with some caveats.
- **The need is real.** `job_2026_apply_29.md` has 13 "Apply to <Company>!" tasks from the last two days, and its only open task is "Collect the 7 roles…". Today's "Wave 3: Twelve More Roles" note means another batch is coming.
- **Most of the cost is in the editor, not in `bob capture`.** The Mac app drops all syntax highlighting if any highlight range from `bob capture-parse` doesn't point into the text you actually typed. Expanded text never exists in the editor, so those ranges need special handling.
- **The `:` in your example may not be what you want.** It makes every row a Next task with a Pomodoro link, which means 7–12 links at once and goes over the link cap of 10. Your existing apply tasks use plain `^apply-<slug>` IDs instead. I flagged this rather than changing it.

**Recommended solution:**
- **How it works:** bob expands the template as plain text before parsing. Capturing a template draft is defined to be exactly the same as capturing its expanded draft, all rows or none. The planner, the atomic commit, the duplicate-ID checks and the Mac preview cards don't change. That rule also gives a simple test: compare the dry-run of the template with the dry-run of its expansion.
- **The Mac app needs no required changes**, as long as bob only reports positions in the typed text. Optional polish is colours for placeholders and fields plus a "Template · N rows" header. No grammar goes into Swift.

**Changes I'd make to your requirements:**
1. **Number fields from 1, and let `{0}` mean the whole row.** Your sase macros already number placeholders from `{1}`, and awk does the same (`$0` whole line, `$1` first field). `{0}` makes one-per-line lists with spaces work without quotes, e.g. `{0} @groceries`. A draft written 0-based gets an explanatory error, so it never silently goes wrong.
2. **Make each nonblank line a row.** Blank lines between rows become optional, so your blank-line example still works.
3. **Allow quotes for multi-word fields, and require every row to have the right number of fields.** Splitting on spaces alone breaks real names like "Two Sigma" and "DE Shaw". A strict count turns a forgotten quote into an error instead of silently shifted fields.
4. **Tighten where placeholders apply:**
   - only the first item can hold them;
   - a blank line is required between the template and its rows;
   - `\{` writes a literal brace, and text inside backticks stays literal.

   None of the 3,724 task lines in your vault contain `{N}`, so this breaks nothing.
5. **Treat a `@@route` inside the template as one draft-wide destination.** Otherwise copying it into every row would trigger the duplicate-destination error.
6. **Refuse clipboard markers (`%`) and Pomodoro session commands (`=`, `=x`, `+N`) in templates for now.** Running those once per row is almost never what you'd want.

**Follow-ups, not in the first version:**
- A `{1|slug}` filter. Your block IDs are just the company name slugified, so this would drop a whole column from each row.
- Accepting Markdown table rows (`| a | b |`) so a table from an LLM report can be pasted directly.
- Defaults (`{N:default}`), extra bullets under individual rows, and saved templates.
