# Chat History - ace-run (et--plan)

- **TIMESTAMP:** 2026-11-17 18:09:59 EST
- **MODEL:** claude/opus
- **AGENT:** et--plan

**Plan:** /home/bryan/.sase/plans/202611/capture_and_ref_panel_glossary_terms.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/capture_and_ref_panel_glossary_terms.md`

> # Add Capture Panel And Ref Panel Glossary Terms
> ## Goal
> Add two glossary terms to the `glossary` memory web: **Capture Panel** for the capture
> window in Bob Mac Capture (the `bob-mac-capture` linked repo) and **Ref Panel** for its
> reference-library window, which the app calls **Bob Refs**. Each definition says what
> the panel is, how it opens, what it shows, what it is allowed to write (always through
> `bob`), how the two panels relate, and what it is not. The published glossary page is
> regenerated to match.
> ## Context (verified while planning)
> - Strands live at `sase/memory/glossary/<slug>.md`. Frontmatter holds `keyword:` and an

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me add excellent new "capture panel" and "ref panel" terms to the
glossary that specify the bob-mac-capture app's capture panel and its ref panel,
respectively? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm exploring the bob-mac-capture repo to see how its capture panel and ref panel actually work before I write the glossary plan.

I'm reading the docs memory note and the glossary generator, since new strands also regenerate the docs glossary page.

I'm checking how glossary link closure works, since links in the new strands decide how much text each read pulls in.

Still researching: I'm testing how glossary mentions resolve, so the new terms' aliases don't pull in unrelated definitions.

I'm checking SASE's mention-matching code to confirm which words in the new definitions pull in other terms.

I'm running a small read-only test of the phrase matcher on draft wording, then I'll write the plan.

I have enough on matching behavior. Next I'm reading the pickers, idle agenda, and keyboard docs to get the capture panel's parts right.

Checking a past commit that added a glossary term, to list exactly which files change together.

Drafting both definitions now and running them through the phrase matcher to see which other terms they would pull in.

Ref Panel's only stray mention is "capture draft", and Capture Panel's is "keeps". I'm fixing both and re-testing.

Drafts are clean: a Ref Panel read is about 540 words, Annotation Section grows from 258 to about 780 words, and Capture reads are unchanged. Writing the plan file now.

The validator wants `title`/`goal` plus memory toggles (a `memory:` selector list, no choices or `why`). Fixing the frontmatter.

The plan reads correctly. Cleaning up the scratch files and proposing.

I've written the plan for the two new glossary terms, it passes validation, and I've proposed it. Nothing in the repo has changed yet: the plan is staged, and once you approve it a coder will make the changes.

**What the plan adds** (a single small task; the full text of both definitions is in the plan):
- **Capture Panel**: Bob Mac Capture's capture window. It covers:
  - how it opens: Ctrl-Shift-Cmd-I, ``Cmd-\``, or the menu-bar Capture row
  - the editor, the area below it, and the footer
  - the idle agenda and live preview
  - submitting the whole draft as exactly one capture, and hiding only when `bob` reports success
  - what happens to the draft on Escape, Ctrl+Tab, Discard, or a stash
  - Go To and event-note mode
  - the rule that only one of the two panels shows at a time

  It also says the app's menus call this panel "Capture", while in the glossary a capture is one `bob capture` run. It ends with what the panel is not: Command Mode, the app's menu-bar item or Settings window, or the Hammerspoon Pomodoro indicator.
- **Ref Panel** (aliases **Bob Refs** and **refs panel**): the reference-library window. It covers:
  - how it opens, including the Cmd-O / Cmd-T / Cmd-Y keys while Highlights is in front
  - its rows and sections, the Newest and Tabs views, and the inspector
  - Return opening the PDF without changing the vault
  - the Copy, Rename (`bob ref rename`) and Link to Today (`bob ref today`) cards
  - ⌘S running `bob ref scan -a -w`
  - its NEW marks living only in the app, separate from the review walk's NEW tier

**Keeping glossary reads short.** I tested on a scratch copy of the memory notes. Reading a glossary term also prints in full every other term its text mentions by name, and mentions inside those, recursively. Writing "Bob Mac Capture" or "Pomodoro" (even inside a `[[pomodoro]]` link) pulls in about 4,300 words. The plural "Refs panel" doesn't match "Ref Panel", which is why it needs to be an alias. So:
- Ref Panel names the app as `bob-mac-capture` in code formatting and points to other terms only through hyphenated links, which aren't printed in full. Reading it costs about 540 words.
- The "refs panel" alias means Annotation Section's existing phrase "the Mac Refs panel" now pulls in Ref Panel, growing that read from 258 to about 780 words without editing that note.
- Reading Capture Panel also prints the Capture definition in full (about 4,650 words total). That's intended, since every submit from the panel is one Capture.

**Your decisions at approval:**
- Add Capture Panel: on (you asked for it).
- Add Ref Panel: on (you asked for it).
- Make the Capture term's "Bob Mac Capture's panel" phrase link to the new term: off by default, since you didn't ask for it. It costs about 3 words per read.

The coder will also re-check every fact against the current bob-mac-capture docs and update the generated glossary files and the published glossary page. Checks include `just docs-check` and confirming the read sizes above.

The validator shows two warnings that the new term files aren't covered by a decision. Neither selector format I tried cleared them, even though the decisions are attached. They look like false alarms for terms that don't exist yet. I didn't file a bead for this; tell me if you want one.
