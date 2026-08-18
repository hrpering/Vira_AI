# Distributed inference

Distributed inference spreads model-serving capacity across more than one node or serving surface. It can improve capacity, resilience, and placement flexibility, but it also adds operational responsibilities: health, queueing, routing, security, observability, licensing, and data location.

Distributed does not automatically mean more accurate. A trustworthy surface should disclose relevant latency, fallback, serving location, and failure behavior without exposing sensitive infrastructure details. A node should advertise only capabilities and capacity it can actually verify.

This repository intentionally does not publish a node protocol, node advertisement schema, heartbeat format, lease model, capacity formula, or internal serving contract.
