# Chat History - ace-run (research.6l.mus)

- **TIMESTAMP:** 2026-11-26 12:49:39 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** research.6l.mus
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261126_124105.md`

## Prompt

%id(mus, clan=research.6l)
%m:muse/muse-spark-1.3-contributor@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher mus in a 5-researcher swarm.
The other researchers, `research.6l.cdx`, `research.6l.cld`, `research.6l.grk`, `research.6l.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__gem.md`. Your report will end in `__mus.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to implement "ref cards", a new type of property card for ref notes.

- See how other property cards are implemented and the bob-cli-qm epic bead, which is
  in-progress and implements notebook cards and prose cards, for context and
  inspiration.
- We should implement this work in parallel (think hard about the best way to do this
  and whether or not coordination is even needed) with the in-progress bob-cli-qm epic.
- Think hard about how this card should look. It should contain as much genuinely useful
  information about the reference as possible without cluttering the card.
- Also, think hard about whether or not ref cards should support the `==` keymap and, if
  so, what kinds of operations the schema editor that is triggered should support.
- As a part of this change, we should add an excellent new glossary term for "ref card".
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
First run `sase repo open research -r "Write this research report"` and use the path it prints as `<research checkout>`. Write this research to a new markdown file under `<research checkout>/202611/`.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__mus` suffix, i.e. `<stem>__mus.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path under the opened research checkout and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

Research complete. My report is written to [202611/ref_property_cards__mus.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/research/202611/ref_property_cards__mus.md) in the research checkout and registered as a durable snapshot (`research:202611/ref_property_cards__mus.md`, artifact `explicit:12ae0045e070f05ee4b27087`).

Key conclusions:

- **Yes, build ref cards** as a third species on the existing Property Card kit in `bob-plugins`, in a sibling epic to `bob-cli-qm` with a single gate on `qm.1` (kit: species registry, precedence, focus-or-add, preview gate). No other coordination is needed; no CLI, wire, or Rust change is required since `NoteKind::Reference` already exists on the props wire — strictly easier than prose.
- **Card design:** compact expanded-by-default card with a new `bookmark` tile and `REF` kicker — title, author/published byline, derived reading-state chip plus blocked pill, and a measure row (annotation counts, PDF/audio/version marks). Everything content-gated; the managed embed and reading task are linked to, never touched.
- **`==`:** yes, register the `ref` kind, but v1 should only focus-or-add `title` — status is derived (task wins) and `parent` is projected, so a raw schema editor would fight sync. A dedicated ref editor with locked derived rows and jump-to-task is the correct v2.
- Includes a draft `glossary:ref-card` term and a 5-phase delivery plan with acceptance criteria.
