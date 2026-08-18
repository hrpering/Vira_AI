# Architecture overview

Vira can be understood as a chain rather than a single model call:

`request → context → model/project selection → routing → work surface → review → durable output`

The model layer generates or transforms content. A Studio or workflow layer manages observable steps. Generative UI turns a structured result into a task-specific surface. Projects and Outputs preserve context and durable artifacts. Distributed inference provides serving capacity and placement options.

Each boundary answers a different question: what can generate, what can orchestrate, what can access data, what can be reviewed, and what remains after the run. Keeping those boundaries visible prevents a model name from being mistaken for the entire product or a project license from being mistaken for the hosted platform’s license.

## Reference flow

1. A user expresses a task and supplies context.
2. The system filters candidates by capability, policy, availability, and data constraints.
3. Routing selects a model or serving surface and records fallback conditions.
4. A chat, Studio, or Generative UI surface exposes progress and review points.
5. The result becomes an Output, Project artifact, export, or an explicit failure.
