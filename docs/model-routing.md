# Model routing

Routing is the decision that sends a task to an eligible model, provider, or inference surface. A defensible decision considers task type, language, context, cost, latency, capacity, license, and policy boundaries.

Automatic routing should not remove user control. When safe and useful, the selected model, decision reason, fallback trigger, and data boundary should be visible. Hard constraints must be applied before soft preferences such as cost or speed.

See [`specs/model-routing.md`](../specs/model-routing.md) and the example policy in [`examples/routing/policy.yaml`](../examples/routing/policy.yaml).
