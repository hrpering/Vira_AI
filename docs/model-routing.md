# Model routing

Routing is the decision that sends a task to an eligible model, provider, or inference surface. A defensible decision considers task type, language, context, cost, latency, capacity, license, and policy boundaries.

Automatic routing should not remove user control. When safe and useful, the selected model, decision reason, fallback trigger, and data boundary should be visible. Hard constraints must be applied before soft preferences such as cost or speed.

This repository intentionally does not publish routing policies, weights, latency limits, region constraints, fallback triggers, or disclosure schemas. Those details belong to the hosted product and live configuration.
