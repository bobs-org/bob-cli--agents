# Chat History - ace-run (g1)

- **TIMESTAMP:** 2026-11-24 16:29:32 EST
- **MODEL:** claude/opus
- **AGENT:** g1

## Prompt

#gh:gh_bobs-org__bob-cli Is there any way to progress on the work described by the bob-cli-ph epic bead
without waiting for a release? These only happen daily, I think, so it's not ideal to
block a single agent's work on a release.

Make sure your report is concise, easy to understand, and contains great visuals.

First run `sase repo open research -r "Write this research report"` and use the path it prints as `<research checkout>`. Write this research to a new markdown file under `<research checkout>/202611/`.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path under the opened research checkout and its path relative to the research repo root
(for example
`research:202609/topic.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete. %m:@xlarge %q(1.5x,w=0.3)

## Response

Reading the epic's plan to find what exactly the release gate protects. Next: sections 3 and 9 (dual-read and rollout gates).

Nearly done researching. A scheduled release run is in flight right now; checking its status, then writing the report.

Both figures render cleanly. Writing the report now.

Report written and registered. Finishing the turn with the SASE final declaration.

**Yes. What the release gate is waiting for is already true, so the drawer epic doesn't need to wait for a release.**

## What I found

- **The gate exists to prove one thing.** Phase `ph.3` holds back every writer phase until each host's `bob` can read bold drawers (`- **Title**`). I ran a read-only test against a throwaway vault on athena, apollo, and the Mac. All three read the bold drawer correctly (`"marker":"bold"`). The Obsidian plugin readers were already up to date on all three.
- **The gate checks the wrong thing.** `scripts/dev/bob-host-currency` asks whether a release containing the reader commits is installed. But every host builds `bob` from a master checkout (`just install-all` runs `cargo install --path`). Those builds always print `bob 0.6.0`, whatever commit they came from. So the script calls hosts "behind" when they are actually a day ahead of the newest release.
- **Releases don't prevent the problem the gate guards against.** The risk is one host writing bold drawers before another can read them. That starts when a host installs new code, and hosts install from master, not from releases.
- **A release wouldn't turn the gate green either.** Today's scheduled release run is in progress, with only the macOS test left. Even if it publishes, all three hosts, Mac included, would still need to reinstall before the version check passes.
- **The same check appears twice.** It also guards the writer check in `ph.9` (vault migration). That's two waits of about a day each on the epic's critical path.

## What I recommend

1. Approve dropping the plan's "wait for the release" rule (§9) in favor of testing the hosts directly. It's a change to the approved plan, so it needs your OK.
2. In `bob-host-currency`, replace the release check with the per-host test. The report includes the exact snippet.
3. Re-run the script, store the passing table, and close `ph.3`. Stop monitor `yze12k21fh57`, which is waiting for a release, so its follow-up doesn't close the phase a second time.
4. Start `ph.4` (writers) today. Add a matching writer test for the `ph.9` check.
5. Later, optionally: have `bob --version` include the commit it was built from, so future checks don't need a custom test per feature.

The report also compares four other options and notes two risks: a host could later install an older build, and the Mac is only reachable when it's awake.

I didn't change any beads, monitors, or code.

## Files

- Report: `202611/drawer_reader_gate_without_release.md` in the research repo, with two diagrams (rendered and checked) and a table of the per-host results. The host will commit it after this turn.
- Saved as a durable snapshot: `file:explicit:561d0b66f8faf13282515d16`, label `research:202611/drawer_reader_gate_without_release.md`.
