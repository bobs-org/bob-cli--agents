# Chat History - ace-run (research.5m.gem)

- **TIMESTAMP:** 2026-11-01 18:13:22 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.5m.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261101_180013.md`

## Prompt

%id(gem, clan=research.5m)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5m.cdx`, `research.5m.cld`, `research.5m.grk`, `research.5m.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add support for a special new "starts after" relation label.

- This label should be rendered as "starts before" in the mirrored "linked from" bullet.
- The goal of this label is to allow me to trigger a successor prompt for certain tasks
  when another task is marked as wip/pending and moved out of the daily file (an
  operation that is unique to the `x*` capture syntax I believe). This will be useful
  since the tasks that I target with `x*` are often ones that correspond with work that
  I have assigned to an agent and I sometimes have another prompt that I want to think
  through and send out only after I have done the same for some other task (this is the
  one that I plan to target with the "starts after" relation).
- The successor prompt should also be triggered if the target task is closed (this is
  how normal successors work).
- Make sure it is very clear why this successor prompt is being triggered since we have
  various types of successors now.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

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

# Architectural Research & Design Report: The "starts after" Relation Label & Successor Trigger

I have completed the independent research investigation for the proposed **`starts after`** relation label and its successor triggering behavior. The full research report has been authored and registered as a durable snapshot in the research repository:

- **Report Path:** [`sase/repos/research/202611/starts_after_relation_successor_design__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202611/starts_after_relation_successor_design__gem.md)
- **Durable Snapshot Ref:** `research:202611/starts_after_relation_successor_design__gem.md` (`file:explicit:850e37396fb1550153b43b61`)

---

## Key Findings & Critical Analysis

### 1. The Core Insight: Asynchronous Agent Delegation Needs "Start-to-Start" Triggers
In standard GTD and project management, dependencies are **Finish-to-Start (FS)**: Task $B$ cannot begin until Task $A$ is marked Done (`[x]`). In Bob, this is handled via managed `Depends-On` lines and `hand_off` successor offers.

When collaborating with autonomous AI agents (such as SASE agents), human labor is front-loaded into **prompt preparation and dispatch**. Once an agent is launched, the human work for that phase is complete, and Bryan parks the task with `x*`, marking it In Progress (`[/]`) and removing it from the active daily Pomodoro ledger. Bryan often has another prompt (Task $B$) that he wants to think through and dispatch **only after Task $A$ has been launched, but long before Task $A$ finishes**.

Bob's successor engine (`docs/task-dependencies.md` §12) currently only triggers when tasks move open $\to$ Done (`[x]`). Rule **SL21** explicitly dictates that `x*` parks *never offer and never link successors*. The proposed feature elegantly solves this gap by introducing a **Start-to-Start (SS)** workflow trigger.

---

### 2. Critique of the Plan: Is Overloading Relations a Good Idea?

#### The Architectural Tension
`docs/task-relations.md` lines 11–14 explicitly states:
> *"Live chips render both ends correctly, and **relations never block, promote, consume, schedule, stamp, or route anything**. The exceptions are the commit-time cancel of §17 and the commit-time complete of §18."*

Relations were conceived as an inert, hypermedia graph (`see also`, `inspired by`, `follow-up of`). If `starts after` triggers an active execution prompt, it bridges relations into workflow orchestration.

#### Evaluation of Alternatives
We evaluated two competing paradigms:

1. **Approach A: True Start-to-Start Dependency (`Depends-On`)**
   - *Model:* Make Task $B$ Blocked (`[?]`) until Task $A$ reaches `[/]` or `[x]`.
   - *Drawback:* **Extremely high blast radius.** Requires modifying `Depends-On` syntax, altering `task-status-hooks`, cyclic dependency resolvers, transitive reductions, and sticky lane logic (`[/]` is sticky). It also locks Task $B$ into `[?]`, preventing Bryan from working on it early if priorities shift.

2. **Approach B: Advisory Relation Trigger (Recommended)**
   - *Model:* Treat `starts after` as an **advisory sequencing trigger** (identical to Bob's existing `keep_moving` successor model).
   - *Behavior:* Task $B$ remains Ready (`[ ]`) or Next (`[*]`) in its home note. It does not become Blocked (`[?]`). When Task $A$ is parked (`x*`) or closed (`x!`), Bob notices the relation and surfaces Task $B$ in the successor prompt.
   - *Advantage:* **Zero distortion of the dependency graph**, low architectural blast radius, and total workflow flexibility.

---

### 3. Grammar, Vocabulary & Inverses

- **Stored Outgoing (Task $B$):** `- 🪢 **LINKS:** [[Task A#^id]] (starts after)`
- **Mirrored Incoming (Task $A$):** `- 🪢 **LINKED FROM:** [[Task B#^id]] (starts before)`
- **Symmetric Reverse Authoring:** If authored on Task $A$ as `LINKS: [[Task B]] (starts before)`, it mirrors onto Task $B$ as `LINKED FROM: [[Task A]] (starts after)`. In both cases, the directed semantic edge is identical: Task $A$ starts before Task $B$.
- **Registration in `NAMED_PAIRS`:**
  Registered in lexicographical order in [`src/native/task_relations/inverse.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/src/native/task_relations/inverse.rs) and its JavaScript twins in `bob-ledger-tools` (`145a`) and `bob-navigation-hotkeys` (`303a`):
  ```rust
  ("starts after", "starts before"),
  ("starts before", "starts after"),
  ```

---

### 4. Successor Engine Taxonomy & Presentation

To make the trigger unmistakably clear amidst existing successor types (`hand_off`, `project`, `project_finished`, `keep_moving`), the feature introduces a 5th formal group: **`OfferGroup::StartsAfter`**.

#### Selection Hierarchy Priority:
$$\text{hand\_off} > \mathbf{starts\_after} > \text{project} > \text{project\_finished} > \text{keep\_moving}$$

#### UI/UX Styling:
- **CLI Header & Row:**
  ```text
  🚀 Starts after “Brief research swarm Agent Alpha” (parked in-progress)
    [1] [*] Draft follow-up prompt for Agent Beta   projects/agent-ops.md:14
  ```
  *(If triggered by closure: `(completed)` instead of `(parked in-progress)`).*
- **Bob Mac Capture Choice Card:**
  - Distinct SF Symbol badge: `play.circle.fill` / `bolt.horizontal.fill` (cyan/blue accent).
  - Clear attribution subtitle: `"Task was marked in-progress & parked"` or `"Task was completed"`.
- **Obsidian Successor Modal:**
  - Group header with small-caps muted pill: `starts-after`.

---

### 5. Multi-Repository Implementation Scope

1. **`bob-cli`:**
   - [`src/native/task_relations/inverse.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/src/native/task_relations/inverse.rs): Add `starts after` $\leftrightarrow$ `starts before` to `NAMED_PAIRS`.
   - [`src/native/capture/pomodoro_close.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/src/native/capture/pomodoro_close.rs): Collect parked tasks (`outcome == "parked"`) alongside closed tasks (`outcome == "complete"`).
   - [`src/native/task_complete/successors.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/src/native/task_complete/successors.rs): Add `OfferGroup::StartsAfter`, scan relation lines, verify candidates are not already planned, and place picked tasks into the next Pomodoro continuation.
   - [`src/native/capture/output.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/src/native/capture/output.rs): Format human headers and JSON schema responses.
2. **`bob-plugins`:**
   - `bob-ledger-tools` & `bob-navigation-hotkeys`: Register the inverse pair in `RELATION_INVERSE_NAMED_PAIRS`.
   - `bob-navigation-hotkeys`: Update `api.successors.pick` modal rendering for `starts_after`.
3. **`bob-mac-capture`:**
   - `CaptureCore`: Decode `starts_after` in `PullInGroup` and render the choice card with dedicated icons and trigger descriptions.
