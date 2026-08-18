# Distributed inference

Distributed inference spreads model-serving capacity across more than one node or serving surface. It can improve capacity, resilience, and placement flexibility, but it also adds operational responsibilities: health, queueing, routing, security, observability, licensing, and data location.

Distributed does not automatically mean more accurate. A trustworthy surface should disclose relevant latency, fallback, serving location, and failure behavior without exposing sensitive infrastructure details. A node should advertise only capabilities and capacity it can actually verify.

See the public [Node Protocol specification](../specs/node-protocol.md) for the draft advertisement, heartbeat, lease, and expiry concepts.
