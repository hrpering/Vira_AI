# Open-source AI projects

This is an ecosystem map, not a claim that every project is currently installed, hosted, or integrated in Vira. The “Status in Vira” column is intentionally explicit so that a public reference does not become an unsupported product promise.

| Project | Official GitHub | License | What it does | What Vira adds | Status in Vira |
| --- | --- | --- | --- | --- | --- |
| CrewAI | [crewAIInc/crewAI](https://github.com/crewAIInc/crewAI) | MIT | Orchestrates role-based AI agents and collaborative task flows | A user-facing Studio surface, run state, approvals, model/context boundaries, and durable outputs | Referenced and represented as a Vira Studio workflow; verify live availability in the product |
| LangGraph | [langchain-ai/langgraph](https://github.com/langchain-ai/langgraph) | MIT | Builds stateful, durable agent workflows as graphs | A potential workflow/product layer with visible inputs, permissions, routing, and outputs | Ecosystem reference; no native Vira integration claim in this repository |
| AutoGen | [microsoft/autogen](https://github.com/microsoft/autogen) | MIT code / CC-BY-4.0 documentation | Framework for multi-agent applications; the upstream repository currently labels AutoGen as maintenance mode | A potential hosted workflow surface and operational controls, subject to upstream lifecycle review | Ecosystem reference only; no native Vira integration claim in this repository |
| vLLM | [vllm-project/vllm](https://github.com/vllm-project/vllm) | Apache-2.0 | High-throughput and memory-efficient inference serving | A potential serving layer behind routing and node capacity | Ecosystem reference; no public deployment claim in this repository |

## What “Vira adds” means

Vira’s product contribution is the layer around a project: discoverability, a task-oriented entry point, input and permission boundaries, model selection or routing, progress visibility, review points, and a durable result. It does not mean Vira rewrites or owns the upstream project. The upstream project remains governed by its own repository, maintainers, release process, and license.

## Status policy

Use one of these statuses for future entries: **Active in Vira**, **Pilot / validation**, **Referenced**, or **Not integrated**. Every “Active” claim should link to a live public product surface or a verifiable release artifact.
