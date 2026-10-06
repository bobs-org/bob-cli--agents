# Chat History - ace-run (research.3s.mus)

- **TIMESTAMP:** 2026-10-06 15:06:02 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** research.3s.mus
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261006_145643.md`

## Prompt

%id(mus, clan=research.3s)
%m:muse/muse-spark-1.3-contributor@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher mus in a 5-researcher swarm.
The other researchers, `research.3s.cdx`, `research.3s.cld`, `research.3s.grk`, `research.3s.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__gem.md`. Your report will end in `__mus.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to migrate the `bob highlights` command to a new `bob ref` command that
supports all of the same commands that the `bob highlights` command currently does but
also adds new commands that make it easy for agents (and myself) to see what references
I have read, which I am tracking / plan to read, which I've finished reading, etc...

- The main use-case for this command would be for agents that are recommending new
  reading material for me (these agents would find it useful to know what articles /
  papers I have already read).
- With that said, I also think it would be useful to be able to read the annotations
  that I left on these reference PDFs (using the Highlights app on my macbook). These
  are automatically written to markdown files in the ~/bob/ref/ directory.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__mus` suffix, i.e. `<stem>__mus.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example `research:202609/topic__a.md`), including any subdirectory the steps above
put it in. Do not derive the label from the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

Top finding: yes, do the rename — but as an alias-promotion plus three read-only views, not a migration with new state.

Report written to `sase/repos/research/202610/bob_ref_command_migration__mus.md` and registered as durable snapshot `explicit:106e057d33d72d090a88c3ac` (`research:202610/bob_ref_command_migration__mus.md`).

Key evidence behind the recommendation:

- `bob highlights` is six subcommands (`clip, create, doctor, marker, scan, sync`) in `src/native/highlights_ref/`, with config (`BOB_HIGHLIGHTS_*`, `highlights:` keys) and a MacBook cron job invoking it by name — all of which must keep working untouched.
- Project CLI rules require the old spelling to survive as a permanent hidden alias with byte-identical behavior, so "migrate" means promote `bob ref` to canonical, not remove `highlights`.
- Live vault has 590 `ref/` notes (`read` 285, `legacy` 282, rest tiny) — so new commands must tolerate legacy frontmatter, and the tracking states (`ready`/`next`/`wip`/`read`) already exist; the new surface should be read-only views, not new state or a parallel query engine (`bob query` already covers ad-hoc queries).
- Annotations already sync into the note's managed region, so the annotations command should render from the note, never re-parse the sidecar.

Recommended solution: canonical `bob ref` + hidden `highlights` alias, all six subcommands unchanged (no config/env/frontmatter renames), three new read-only subcommands (`list`, `show`, `annotations`) with `--format json` for agents, and document the `ready→next→wip→read` tracking workflow through the existing `^ref` checkbox instead of building state-changing commands.

Declaration submitted; research report commit authorized.
