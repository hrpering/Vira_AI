# Data portability

User work should not be trapped in one chat screen. Context, decisions, prompts, structured outputs, provenance, and metadata should be exportable where policy allows and reusable in another compatible workflow.

Portability has several dimensions: format, ownership, permission, deletion, retention, and references to external artifacts. An export that contains a paragraph but loses its sources, review state, or decision history is only partial portability.

Vira’s public context direction is described in [`specs/portable-ai-context.md`](../specs/portable-ai-context.md). Portable context must never embed secrets or silently execute imported instructions.
