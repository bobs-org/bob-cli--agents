# Chat History - ace-run (research.1j.gem)

- **TIMESTAMP:** 2026-10-15 12:57:19 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.1j.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261015_124457.md`

## Prompt

%id(gem, clan=research.1j)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 4-researcher swarm.
The other researchers, `research.1j.cdx`, `research.1j.cld`, `research.1j.grk`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md`. Your report will end in `__gem.md`.

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
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
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

# Research Findings: Template Expansion for Bulk Capture in `bob capture` and `bob-mac-capture`

**Researcher:** `research.1j.gem`  
**Report Artifact:** `research:202610/bulk_capture_templates__gem.md`  
**Absolute Report Path:** `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/bulk_capture_templates__gem.md`  
**Registered Artifact Ref:** `file:explicit:87ce979356cdb352dc456b56`

---

## 1. Executive Critique: Is This a Good Idea?

**Yes, the concept is high-value, but the naive implementation has critical flaws.**

### What Makes It Compelling
- **Massive Reduction in Repetitive Friction:** Capturing batches of job applications, bug reports, reading lists, or CRM outreach items currently forces you to repeat identical routes (`@job_2026_apply_29`), block ID formatting (`:id`), tags, and markdown sub-bullet boilerplate (`- **URL**: ...`, `- **Role**: ...`) on every single item.
- **Natural Fit with Staged Planning:** Bob’s existing `CaptureBatchPlanner` already stages, validates, and atomically commits multiple items across notes. Template expansion simply acts as an upstream macro/desugaring step.
- **Zero-Friction Live Preview in Bob Mac Capture:** Because Bob Mac Capture is a thin client (Decision 6: `mac-capture-is-a-thin-client`), `CapturePanelView` already iterates over `success.normalizedCaptures` from `bob capture --dry-run`. Once `bob-cli` expands the template, **preview cards for all generated tasks render in the Mac HUD with zero SwiftUI view restructuring!**

### Flaws in the Initial Proposal & Why Adjustments Are Required
1. **The Implicit Activation Trap (False Positives):**
   - Relying solely on `{0}` in the first item to trigger templating breaks on code snippets (e.g. `Fix format("{0}") in logger.rs`), regexes (`[a-z]{0,5}`), and single-item captures containing braces. Furthermore, in a 2-task draft where Task 1 happens to have `{0}`, an implicit parser would consume Task 2 as arguments for Task 1!
   - *Adjustment:* Use an explicit declaration keyword: `@@template` or `@@tmpl`. This matches Bob's existing `@@route` declaration grammar, is 100% deterministic, and guarantees zero false positives.
2. **The Whitespace Delimiter Failure (The Multi-Word Entity Problem):**
   - Naive whitespace splitting works for single words (`Foobar foo http://...`), but immediately breaks on real-world entities: `Goldman Sachs`, `Staff Systems Engineer (Infra)`, or URLs with spaces/encoded params. In `Goldman Sachs gs http://...`, `{0}` becomes `Goldman`, `{1}` becomes `Sachs` (the block ID!), and the URL is displaced or dropped.
   - Forcing shell quotes (`"Goldman Sachs"`) in a quick-capture popup is cumbersome.
   - *Adjustment:* Adopt an automatic 3-tier delimiter resolution per row:
     1. **Tabs (`\t`)** if present: handles direct copy-pastes from Google Sheets, Excel, Notion, Airtable, or HTML tables without any editing.
     2. **Pipes (`|`)** if present: allows typing clean, unquoted multi-word fields (`Goldman Sachs | gs | Senior Quant | https://...`).
     3. **Shell Words (Whitespace + Quotes)** otherwise: handles clean single-word entries or quoted phrases.
3. **Row Delimitation (Dense Table Pasting vs Blank Lines):**
   - Requiring a blank line (`\n\n`) between every single one-line data row destroys the speed benefit when pasting 10–20 rows from a spreadsheet or text list.
   - *Adjustment:* Allow consecutive single-line rows in the data block (no blank lines required), while also allowing blank-line separation when data rows include per-item custom sub-bullets.
4. **Missing Escaping Mechanism:**
   - *Adjustment:* Support standard escaping where `{{` produces literal `{` and `}}` produces literal `}`.
5. **Special Marker Restrictions:**
   - Clipboard markers (`%`) and Pomodoro session operators (`=x`, `+5`, `=3`) must be rejected inside templates with clear diagnostics.

---

## 2. Recommended Syntax Specification

### Example 1: Human Typing with Pipe Delimiters
```markdown
@@template
Apply to {0}! @job_2026_apply_29:{1}
- **URL**: {2}
- **Role**: {3}

Goldman Sachs | gs | https://gs.com/apply | Quantitative Researcher
Two Sigma | ts | https://twosigma.com/apply | Systems Engineer
```
**Instantiates to:**
```markdown
Apply to Goldman Sachs! @job_2026_apply_29:gs
- **URL**: https://gs.com/apply
- **Role**: Quantitative Researcher

Apply to Two Sigma! @job_2026_apply_29:ts
- **URL**: https://twosigma.com/apply
- **Role**: Systems Engineer
```

### Example 2: Pasting Directly from a Spreadsheet (Tab-Separated)
Copying 3 columns from Google Sheets/Excel automatically pastes as tab-separated text:
```markdown
@@template
Apply to {}! @job_2026_apply_29:{}
- **URL**: {}

Foobar	foo	http://foobar.com/job
Bazbuz	baz	http://bazbuz.com/job
```
*(Notice the sequential `{}` placeholders: no numbers required when arguments map in order!)*

### Example 3: Adding Per-Item Custom Sub-Bullets
```markdown
@@template
Apply to {0}! @jobs:{1}
- **URL**: {2}

Acme Corp | acme | http://acme.com
- **Recruiter**: Jane Doe (met at GHC)
- **Status**: Referral submitted

WidgetCo | widget | http://widget.co
```
Child bullets authored directly under a data row automatically append to the template's child bullets!

---

## 3. Implementation Plan Across Repositories

### In `bob-cli`
1. **Draft Splitting & Expansion (`src/native/capture_language/draft.rs`):**
   - Recognize `@@template` and `@@tmpl` in `split_capture_draft`.
   - Implement `expand_template_draft` with the 3-tier delimiter tokenizer (`\t` -> `|` -> `shlex`).
   - Support indexed `{N}` and sequential `{}` placeholders with `{{` / `}}` escaping.
   - Maintain byte-range sourcemaps from the raw input text to the expanded items.
2. **Editor Lexing (`src/native/capture_language/editor_model.rs` & `capture_parse.rs`):**
   - Add new `SpanKind`s: `TemplateMarker`, `TemplatePlaceholder`, `TemplateDelimiter`, `TemplateArg`.
   - Add structured diagnostics: `MissingTemplateArguments`, `TemplateWithoutDataRows`, `MixedPlaceholderSyntax`, `ForbiddenTemplateMarker`.
3. **Execution & Dry-Run (`src/native/capture/plan.rs`):**
   - Feed expanded items into `plan_capture_batch`. Vault planning, note mutations, dry-run previews, and ledger updates handle the expanded items transparently.

### In `bob-mac-capture`
1. **Model Decoding (`Sources/CaptureCore/CaptureModels.swift`):**
   - Add `templateMarker`, `templatePlaceholder`, `templateDelimiter`, `templateArg` to `CaptureSpanKind`.
2. **Syntax Highlighting (`CaptureTextView.swift`):**
   - Highlight placeholders `{0}`, `{}` with accent colors (e.g. orange / teal) and `@@template` with keyword purple.
3. **Preview Cards (`CapturePanelView.swift`):**
   - **No view code changes required!** The existing `previewContent` view already renders `success.normalizedCaptures` with cards and dividers.

---

## 4. Artifact & Finalizer Verification
- **Full Research Report Written to:**  
  `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/bulk_capture_templates__gem.md`
- **Artifact Registered via `sase artifact create`:**  
  `id: explicit:87ce979356cdb352dc456b56`  
  `ref: file:explicit:87ce979356cdb352dc456b56`  
  `label: research:202610/bulk_capture_templates__gem.md`
- **Finalizer Declaration Submitted via `sase final submit`:**  
  Accepted for `sdd:research` commit obligation (`repo-04bb55b100fa`).
