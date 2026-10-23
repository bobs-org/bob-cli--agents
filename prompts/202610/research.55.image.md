- **AGENTS:**
  - [bbugyi200.athena.research.55.image](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.55.image/README.md)

%id(image, clan=research.55) %m:gpt-6-astra %wait:research.55.final %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli #fork:research.55.final #research/image

The lead researcher's registered report:

{% for a in wait.artifacts if a.kind == "markdown" and a.label and a.label.startswith("research:") %}

- wait_name={{ a.wait_name }} label={{ a.label }} source_path={{ a.source_path }}
  path={{ a.path }} ref={{ a.ref }} {% endfor %}

#research/diagrams
