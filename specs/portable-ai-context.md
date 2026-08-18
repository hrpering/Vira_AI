# Portable AI Context Specification v0.1

**Status:** Discussion · **Version:** 0.1 · **Scope:** exportable work context

## Purpose

Make an AI task transferable between a conversation, Project, Studio, Output, or compatible client without silently losing decisions, sources, permissions, or review state.

## Terminology

**Context** is the portable envelope. **Artifact** is a file or structured output. **Decision** records a human or system choice. **Extension** is a namespaced optional field. **Retention** describes storage and deletion expectations.

## Data model

Required fields: `context_id`, `version`, `created_at`, `source`, `messages`, `artifacts`, `decisions`, `permissions`, `retention`, and `provenance`. Each message has `role`, `content_ref`, and timestamp. Each artifact has `id`, `media_type`, `content_ref`, `owner`, and checksum. Secrets and raw credentials must never be embedded.

## Lifecycle

`created → appended → reviewed → exported → imported → reconciled`. Importers must show conflicts when versions diverge and must not execute imported instructions automatically. Deletion must cover both the envelope and referenced artifacts where policy requires it.

## Example

```json
{
  "context_id": "ctx_demo_001",
  "version": "0.1",
  "source": "vira-studio",
  "messages": [{"role": "user", "content_ref": "text:brief", "created_at": "2026-08-18T00:00:00Z"}],
  "artifacts": [],
  "decisions": [{"id": "d1", "label": "human-review-required", "value": true}],
  "permissions": {"network": "read-only"},
  "retention": {"mode": "user-controlled"}
}
```

## Non-goals

This spec does not define a universal prompt format, identity provider, storage vendor, model output guarantee, or automatic agent execution.

## Versioning

The context envelope uses semantic versions. New optional fields are minor-compatible; changing meaning or removal of required fields requires a major version.
