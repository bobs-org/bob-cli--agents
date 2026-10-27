%id(image, clan=research.2e) %m:gpt-6-astra
%wait:research.2e.final %q(1.5x, w=0.25) #gh:gh_bobs-org__bob-cli #fork:research.2e.final #research/image

The lead researcher's registered report:

{% for a in wait.artifacts if a.kind == "markdown" and a.label and a.label.startswith("research:") %}
- wait_name={{ a.wait_name }} label={{ a.label }} source_path={{ a.source_path }} path={{ a.path }} ref={{ a.ref }}
{% endfor %}

#research/diagrams