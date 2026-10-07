# Chat History - ace-run (research.0k.cld)

- **TIMESTAMP:** 2026-10-07 17:50:50 EDT
- **MODEL:** claude/opus
- **AGENT:** research.0k.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261007_174036.md`

## Prompt

%id(cld, clan=research.0k)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.0k.cdx`, `research.0k.grk`, `research.0k.mus`, `research.0k.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I think that I might be a really good fit to work at Databricks given how much I work on
sase (see the https://github.com/sase-org/sase GitHub repo) and their release of
Omniagent (see https://github.com/omnigent-ai/omnigent). Can you do some research with
the goal of figuring out if they have any job openings that I would be a good match for?
End your analysis with a list of job postings (if any) you think I should consider
applying to. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__cld` suffix, i.e. `<stem>__cld.md` (double underscore before the
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

I've opened the sase and Omnigent repos (Omnigent's contributors are mostly Databricks' MLflow team). Next I'm checking Bryan's background, then searching Databricks job listings.

Pulled Databricks' full live Greenhouse job board (9.8 MB JSON). Now filtering it for engineering roles that match Bryan's profile.

Found strong candidates, including an explicit "Sr. Developer Advocate, Open Source — Omnigent" role and several NYC agent roles. Now reading the full text of each candidate posting.

Still reading candidate postings — next batch covers Agentic Applications, AI Runtime, Genie mobile/desktop, and NYC agent teams.

Confirmed Omnigent is ~80% Python with Matei Zaharia and MLflow engineers as maintainers. Now gathering sase stats to support the fit analysis.

I have enough evidence. Writing the report now.

Registration succeeded. Now submitting the final declaration.

Databricks has no software-engineer opening tied to the Omnigent team right now. Several other openings fit you well, mainly in NYC. I scanned Databricks' full job board as of today (894 postings) and read the 36 relevant ones in full.

The report is `sase/repos/research/202610/databricks_job_fit_sase_omnigent__cld.md`. It's registered as artifact `explicit:fc39a8f9d90e1e3ad42fd8ec` with label `research:202610/databricks_job_fit_sase_omnigent__cld.md`.

**Background:**
- **Omnigent's team:** most of its maintainers are Databricks' MLflow and AI-platform engineers, including Matei Zaharia and Corey Zumar.
- **Hiring:** the only Omnigent postings are a developer advocate role and a designer role. Engineers for it would come through general AI-org postings or referrals.
- **NYC:** Databricks opened a New York research and engineering office in January 2026 focused on AI agents.

**Postings to consider, in priority order:**
1. **Staff Software Engineer, Agent Quality (NYC)** — apply. A new team building tooling to test and measure Databricks' AI agents. It's Python-first and lists dev tools, CI and testing frameworks as nice-to-haves. Base pay $200–265K.
2. **Sr. Software Engineer – Backend, AI Platform (NYC)** — apply. It hires for several teams in the AI org that built Omnigent, and Senior is the safe level for your experience. Base pay $165–220K.
3. **Sr. Developer Advocate, Open Source — Omnigent (SF or Seattle)** — the only job that puts you on Omnigent itself. It means switching from engineering to developer advocacy, lower pay and relocating, so apply only if that appeals.
4. **Staff Security Software Engineer – Agentic Security Engineering (remote anywhere in the US)** — a stretch. Its agent platform needs (sandboxing, human approval, testing agent quality) are close to what sase does.
5. **Staff Software Engineer, Fullstack – AI Product (NYC)** — a stretch, because it asks for 10+ years of web development.
6. **Only if you'd relocate:** Staff Backend Software Engineer (Databricks AI) in SF, Sr Software Engineer – CXI in Mountain View/SF, and Senior Software Engineer – AI/ML Environments in Mountain View.
7. **Fallback and long shot:** Senior Software Engineer – Infrastructure and Tools (SF, other locations considered) is a dev-tools fallback. Staff Software Engineer, Ads Measurement & Orchestration (NYC) is a long shot that uses your Google Ad Manager experience.

**Best move before applying:** Omnigent has an open, triaged "help wanted" issue asking for Meta Muse support (#6083), and it doesn't support Grok Build either. sase already supports both. A merged pull request would put your work in front of the people who'd interview you, and could lead to a referral.

**Weak spots interviewers will probe:**
- **Adoption:** sase has 5 GitHub stars, so it shows design skill but not a user community.
- **Languages:** many Databricks backend roles want Scala or Go, and you have neither.
- **Agent evaluation:** you have no production system for measuring agent quality. Building a small one on top of sase runs would help.
- **Experience bar:** with about 7.5 years, Staff roles asking for 10+ years are a stretch. Expect to be levelled at Senior or Staff.
- **Lines of code:** sell sase's design decisions, not its 2.7M lines.

**Uncertainties:**
- I didn't factor in your Google level or whether you'd relocate. Both could change the ranking.
- Which Databricks team owns Omnigent is my inference from commit history and posting text. No posting states it.
