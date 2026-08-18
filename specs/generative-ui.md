# Generative UI Specification v0.1

**Status:** Draft · **Version:** 0.1 · **Scope:** portable structured result recipes

## Purpose

Define a small, renderer-neutral envelope for turning a structured model result into an editable user interface. The specification separates data from presentation and makes actions, state, provenance, and confirmation visible.

## Terminology

- **Recipe:** A structured description of a Generative UI surface.
- **Renderer:** A client that displays a recipe.
- **Action:** A user-triggered transition or export operation.
- **Provenance:** The prompt, model, sources, and generation metadata behind a result.

## Data model

Required top-level fields: `type`, `version`, `id`, `template`, `title`, `data`, `state`, `actions`, and `provenance`. `data` is template-specific. `state` must include `status` (`draft`, `ready`, `review`, `complete`, or `failed`). Actions declare `id`, `label`, `requires_confirmation`, and optional `output`.

## Lifecycle

`created → rendered → edited → reviewed → exported` is the normal path. A renderer must support `failed` and `cancelled` states, preserve the original generated payload, and never execute an action merely because it was present in the recipe.

## Example

See [`examples/generative-ui/recipe.json`](../examples/generative-ui/recipe.json), [`comparison.json`](../examples/generative-ui/comparison.json), and [`research-brief.json`](../examples/generative-ui/research-brief.json).

## Non-goals

This spec does not define a UI framework, model API, authentication scheme, arbitrary code execution, or a guarantee that every client can render every template.

## Versioning

Minor versions may add optional fields. Breaking changes require a new major version. Unknown fields must be preserved when a client can do so and ignored safely when it cannot render them.
