# Node Protocol Specification v0.1

**Status:** Draft · **Version:** 0.1 · **Scope:** capability and health exchange for inference nodes

## Purpose

Define the minimum public envelope for a node that advertises inference or tool-serving capacity to a routing layer. The protocol is descriptive first; it does not grant a node access to user data.

## Terminology

**Node** is a serving surface. **Heartbeat** is a signed health update. **Capability** is a declared model, tool, or operation. **Lease** is a time-bounded assignment. **Attestation** is evidence about the serving environment.

## Data model

`NodeAdvertisement` contains `node_id`, `protocol_version`, `region`, `capabilities`, `capacity`, `security`, `license_refs`, `observed_at`, `expires_at`, and `signature`. `JobEnvelope` contains `job_id`, `capability_id`, `input_ref`, `policy_ref`, `created_at`, and `expiry`. Payloads should reference protected data rather than embed raw user content.

## Lifecycle

`advertised → eligible → leased → running → completed|expired|revoked`. Heartbeats expire automatically. A node must be removed from eligibility when its signature, capability, health, or policy declaration cannot be verified.

## Example

```yaml
node_id: node-example-01
protocol_version: 0.1
region: eu
capabilities:
  - id: text-generation
    model_ref: account-available-model
capacity:
  status: ready
  max_concurrency: 4
security:
  accepts_raw_user_data: false
```

## Non-goals

No consensus protocol, token exchange, secret transport, arbitrary remote code execution, or claim of hardware trust is defined here.

## Versioning

Messages include `protocol_version`. Receivers must reject incompatible major versions and may ignore unknown optional fields in a compatible minor version.
