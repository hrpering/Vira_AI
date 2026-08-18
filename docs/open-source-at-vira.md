# Open source at Vira

Open source is a property of a particular artifact, not a label that automatically applies to an entire product stack. A model family, an inference library, an agent framework, a hosted platform, and a documentation repository can all have different ownership and license boundaries.

## The four boundaries

| Layer | What it means | Public source of truth | Vira’s relationship |
| --- | --- | --- | --- |
| Open-source models | Model code, weights, model cards, or related artifacts released under terms that must be checked per family and version | The model developer’s official repository and model card | Vira can make suitable models easier to discover or use; Vira does not own or relicense them |
| Open-source projects | Third-party software such as agent frameworks, workflow engines, or inference tools | The project’s official repository and license | Vira can connect suitable projects to a user-facing workflow; Vira does not claim authorship |
| Public Vira documentation | Public explanations and high-level product concepts maintained for the ecosystem | [This repository](https://github.com/hrpering/Vira_AI) | Public reference material for the Vira ecosystem |
| Hosted Vira platform | The operated product, services, account layer, infrastructure, and hosted user experience | [Vira website](https://www.tryvira.xyz/) and live product configuration | Operated separately from this public reference repository |

## Open-source versus open-weight

“Open-source” and “open-weight” are not interchangeable. Some model families publish weights with a separate model license while keeping parts of training data, evaluation, or infrastructure proprietary. Others publish source code under one license and weights under another. Qwen, Gemma, and Llama are useful examples of why the exact family, release, license, and usage policy must be checked at the upstream source.

Vira therefore uses precise language: a model may be described as open-source, open-weight, or source-available only when the relevant upstream materials support that description. The ecosystem list is not a promise of Vira availability. Current availability must be checked in the live Vira catalog or account configuration.

## What this repository publishes

This repository publishes public documentation, specifications, examples, and RFCs. It does not publish private application code, credentials, customer data, or a copy of the complete hosted Vira platform. Read [`ecosystem/models.md`](../ecosystem/models.md) and [`ecosystem/projects.md`](../ecosystem/projects.md) for entity-level references.

## Practical rule

When evaluating a Vira workflow, check four things separately: the upstream artifact and its license; whether Vira currently exposes it; what data the workflow can access; and where the final output is stored. This separation protects users from confusing ecosystem participation with a blanket open-source claim.
