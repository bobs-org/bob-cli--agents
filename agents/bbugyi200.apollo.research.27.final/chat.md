# Chat History - ace-run (research.27.final)

- **TIMESTAMP:** 2026-10-20 16:47:09 EDT
- **MODEL:** claude/opus
- **AGENT:** research.27.final

## Prompt

%id(final, clan=research.27)
%m:@xlarge
%wait:research.27.cdx %wait:research.27.cld %wait:research.27.grk %wait:research.27.mus %wait:research.27.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I would love to be able to start showing likely related tasks in the bob-mac-capture
app's preview panel when the capture the user has input will result in one or more new
tasks being created.

- The main benefit of this feature would be that it gives the user a heads up about
  duplicate tasks and/or related tasks that they might want to link to in some way.
- The biggest concern here is performance. The bob-mac-capture app must remain blazing
  fast.
- A secondary concern would be how we fit all of this in the panel without making it too
  cramped or making the user need to scroll too often.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.

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
   dispatch's `research.27.cdx`, `research.27.cld`, `research.27.grk`, `research.27.mus`, `research.27.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.27.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.27.linker`, can find it:

   `sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"`

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

Read the cdx and cld reports; now reading grk, mus, and gem.

Read all five reports. Next I'll do my own research on the points where they disagree: memory decisions, the Mac code, timings, and whether the Mac is reachable.

The Mac is online, which none of the five researchers had. I'll measure real Mac latencies (read-only commands only).

Mac numbers are in: spawn floor ≈4.7 ms, the `:` routable open-task catalog ≈21 ms, vault-wide `&` ≈175 ms. Next I'll verify the code claims the reports disagree on.

Running a quick scorer comparison on the live task catalog (3,901 tasks) to settle the Dice vs TF-IDF vs AND-matcher disagreement.

Scorer comparison done (TF-IDF clearly beats AND matching and catches stemmed duplicates that Dice misses). Now checking the capture grammar for a "merge into existing" action.

Moving the five reports (plus the cld mockup) into a new `capture_similar_tasks_band/` folder, then writing the consolidated report.

Drafting two small figures (lane timing, band lifecycle) and test-rendering them per the Mermaid guide.

The state figure fits. The sequence figure is too wide and its step reference is off by one. Revising it.

Writing the consolidated report now.

Report written. Registering it as an artifact for the linker.

Artifact registered (`file:explicit:bdd44453648ad849f537fca2`). Submitting the final declaration.

I've written the consolidated report and registered it as `research:202610/capture_similar_tasks_band/capture_similar_tasks_band__final.md` (ref `file:explicit:bdd44453648ad849f537fca2`) for the linker. All five reports matched their expected suffixes. They now sit in `202610/capture_similar_tasks_band/`, together with cld's mockup image under its original name so the cld report's image link still works. The research repo is declared for commit.

**Verdict:** build it, but as a duplicate-first **"Similar tasks"** band, not a "related tasks" list. Matching on wording reliably finds the same task captured twice. It can't find prerequisites: in cld's test on 95 real dependency pairs, the true prerequisite ranked in the top 5 only about 20% of the time.

**What I added beyond the five reports:**
- **The Mac was reachable, so I measured on it** (all read-only). No researcher had Mac numbers. Starting `bob` costs 4.7 ms, `capture-parse` 4.8 ms and a dry-run 5.0 ms. Scanning every open task in routable notes takes 21 ms; the vault-wide scan takes 175 ms.
- **This changes the architecture.** Three reports proposed an index held in the app. Instead, v1 calls a new `bob capture-related` command once per typing pause (about 350 ms with no edits), on its own lane that the next keystroke cancels. I estimate 20–30 ms per call; the real command still needs timing. Typing, the preview and Return never wait on it. cld's in-app index becomes the fallback if the Mac's p95 goes over 50 ms.
- **I compared scorers on the live catalog** (3,901 tasks, leave-one-out over ~500 open tasks):
  - TF-IDF that treats code spans and keymaps as whole words beat the alternatives.
  - mus's all-terms picker matcher fired on only 3% and missed obvious paraphrases.
  - Dice scoring missed stemmed duplicates and flagged pairs that differ only inside code spans.
  - Including all closed history tripled how often the band fires.
- **The vault has real open duplicates today**, all in different notes. Examples: "Sell stocks!" vs "Sell stocks now!", and the zensical docs-site task in both `bob.md` and `sase_pre_blog.md`. So matching must not be limited to the destination note.
- **A new "merge" action:** `+` rewrites the item to `@route+id`. Your text becomes a note under the existing task instead of a new task, so nothing you typed is lost.
- **Corrections to the reports:**
  - gem's latency estimates and its `capture-dependency-tasks` command are wrong; that command doesn't exist.
  - gem's ⌥ shortcuts collide with macOS character input.
  - mus's timings came from a debug build.

**Requirement changes (spelled out in the report):**
- Call it "Similar tasks". Show nothing when there's no match, and never a "No duplicates" line.
- Results update only after a pause in typing, never on every keystroke.
- Recently closed tasks (last 30 days) appear only when they're near-identical.
- At most 2 rows per new task, folded to one line before the panel would ever scroll.
- Every action is an edit to the draft that bob previews before anything is written. Return is never blocked.
- `@` (link into today) and `!` (mark done) are deferred. Linking a Blocked task drops its prerequisites, and 84% of open tasks are Blocked.

**Recommended solution:**
- **bob:** `bob capture-related` scores against open tasks plus near-identical tasks closed in the last 30 days. Its `--query` option doubles as the tool for calibrating thresholds.
- **App:** a zero-pixel band when nothing matches. Otherwise a footer inside the new task's preview card with at most 2 rows.
- **Keys:** ⌘1/⌘2 focuses a row and opens a strip of actions keyed by the capture sigils: `~` relate, `+` add as note, `⌫` discard mine, `&` needs it, `*` blocks it, `/` open.
- **Calibration:** you label about 100 fresh pairs before the thresholds are fixed.

**Caveats:**
- The Mac timings ran over SSH with a warm cache, not from inside the app.
- My scorer precision is my own eyeballing, so treat it as directional.
- cld's mockup shows 3 rows and a 7-action strip; the report notes where my recommendation differs.
- I dropped the second diagram (a timing sequence) because it rendered too wide after two revisions; that path is a table instead.

The report ends with five open questions for you. Examples: whether ⌘1/⌘2 conflict with your setup, and whether adding as a note should also mark the existing task as still current (`[fresh:: today]`).
