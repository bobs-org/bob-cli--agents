# Chat History - ace-run (1fa.2--plan)

- **TIMESTAMP:** 2026-11-22 18:00:34 EST
- **MODEL:** claude/opus
- **AGENT:** 1fa.2--plan

**Plan:** /home/bryan/.sase/plans/202611/gmail_html_whitespace.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/gmail_html_whitespace.md`

> # Gmail HTML bodies: follow browser whitespace rules
> ## Why
> `bob gmail` saved the Alertmanager email `[athena alert] FIRING MacDiskLow` into the
> vault as a mail note whose conversation card is mostly noise. Here is an excerpt of the
> saved card body:
> ```text
> > &#32;
> > &#32;1 alert for&#32;
> > &#32;alertname=MacDiskLow
> > &#32;

*See full plan file for details.*

## Prompt

%id:@.2
#gh:gh_bobs-org__bob-cli Is this something we can/should fix? If so, use your /sase_plan skill to plan the appropriate changes. See the
^athena-alert-firing-macdisklow task in the ~/bob/dev.md file for context. %m:@xlarge

## Response

Reading the tailnet memory so I can check the Mac's disk usage and the alert runbook.

Mac free space fell from 119 GiB to 67 GiB over the past 15 days (about 3.5 GiB/day), so this alert reflects real growth and isn't noise. Now finding which directories are growing.

Mac disk check is done: the growth comes from outside the areas my account can read, not from bob-cli. Now checking whether the garbled mail note (all the `&#32;` lines) is a bob-cli rendering bug.

Plan scope: the disk alert itself isn't a bob-cli bug, but the garbled mail note is. Checking how mail notes get re-rendered so the plan can cover notes that are already in the vault.

Writing a throwaway reproduction test with Alertmanager's email template to confirm the exact output before planning (I'll revert it afterwards).

Root cause confirmed and the fix is designed. Loading the planning skill.

Writing the plan.

The disk alert is real, but bob-cli didn't cause it and code can't fix it. The garbled mail note behind that task is a bob-cli bug, and I've proposed a plan to fix it.

**The MacDiskLow alert**
- **It's a real trend, not noise.** According to athena's Prometheus, free space on the Mac's Data volume fell from 119 GiB on Nov 7 to 67 GiB today, about 3.5 GiB a day. At that rate the 15% line will keep firing.
- **bob-cli isn't the cause.** Its Mac footprint is about 7.4 GiB of build output in `bob-cli/target` plus the 5.9 GiB vault. That's steady, not 50 GiB of growth.
- **The growth is somewhere I can't see.** The Data volume holds about 370 GB, but my SSH user can read only about 130 GB of it (about 77 GB in your home folder). The other ~240 GB is in root-only system data, the other user accounts (`kellydonnelly`, `shelter`), or app data macOS blocks from SSH. There are no local snapshots on the Data volume holding space.
- **Next step is on the Mac:** check System Settings → General → Storage, or run an elevated `du`. That's cleanup, not a code change, so it isn't in the plan.

**The garbled mail note (planned)**
I reproduced it with a scratch unit test using Alertmanager's email template, then reverted the test. bob's Gmail HTML renderer treats the email's source formatting as content:
- Source newlines and indentation become real Markdown line breaks and `&#32;` lines.
- Whitespace between tags becomes `&#32;`-only paragraphs.
- Mailjet's tracking links, which have no visible text, survive as empty links.

Every templated HTML email hits this: alerts, CI mail, newsletters.

The plan (`sase_plan_gmail_html_whitespace.md`, medium tale) makes HTML bodies follow normal browser whitespace rules:
- Whitespace collapses to one space, and only `<br>` and block boundaries break lines.
- Whitespace-only paragraphs are dropped, and so are links with no visible text.
- It adds a regression test built from the Alertmanager email and a bullet in `docs/gmail.md`.

It has one decision for you, `layout_rows` (default `keep_blocks`). An email's layout table usually has one content cell, and that cell keeps its separate paragraphs. Without this, fixing the whitespace would turn the whole alert into one run-on line.

Notes already in the vault keep their old rendering until rebuilt. Once a release with the fix is installed on the Mac, run `bob gmail save mail/2026/261122_athena_alert_firing_macdisklow.md -R` to rebuild the alert note.
