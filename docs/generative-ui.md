# Generative UI

Generative UI turns a structured model response into a task-specific interactive surface instead of leaving the result as a paragraph in chat. A recipe has ingredients and steps; a comparison has criteria and evidence; a plan has dates and dependencies; a research brief has findings, sources, and uncertainty.

A useful Generative UI result makes its provenance, editable fields, state, export path, and user confirmation visible. Actions must be explicit and must not run merely because a model included an action name in a payload.

The public envelope is defined in [`specs/generative-ui.md`](../specs/generative-ui.md), with JSON examples under [`examples/generative-ui/`](../examples/generative-ui/).
