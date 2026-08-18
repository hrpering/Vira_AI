# Open-source model families

This is an ecosystem reference, not a live Vira model catalog. The table records real model families and the upstream sources that define their licenses and usage terms. “Vira availability” is intentionally separate from ecosystem presence: an upstream model can be important to the open ecosystem without being enabled for a particular Vira account, plan, region, or runtime.

| Model family | Developer | Official source | License / type | Open-source vs open-weight distinction | Typical task | Vira availability |
| --- | --- | --- | --- | --- | --- | --- |
| Qwen | Alibaba Cloud / Qwen team | [QwenLM/Qwen](https://github.com/QwenLM/Qwen) | Repository code: Apache-2.0; model releases may use separate Tongyi Qianwen terms | Check the exact checkpoint and its model license; repository code and weights are not automatically governed by one identical term | Multilingual chat, reasoning, coding, tool use | Ecosystem reference; do not infer current account availability |
| Gemma | Google DeepMind | [google-deepmind/gemma](https://github.com/google-deepmind/gemma) | Apache-2.0 repository; model terms must be checked for the exact release | Official materials describe Gemma as open-weight; “open-weight” does not by itself mean every training artifact is open-source | Chat, summarization, local experimentation, multimodal or text tasks depending on release | Ecosystem reference; do not infer current account availability |
| Llama | Meta | [meta-llama/llama](https://github.com/meta-llama/llama) and [llama-models](https://github.com/meta-llama/llama-models) | Llama Community License / use policy varies by model generation | Llama releases are commonly described as open-weight or openly released, but the Community License is not the same as an OSI-approved open-source license | General chat, multilingual generation, summarization, agentic applications depending on release | Ecosystem reference; do not infer current account availability |

## How to read this table

- **Developer** identifies the upstream organization, not Vira.
- **Official source** is the place to verify the current model card, release, license, and safety policy.
- **License / type** is deliberately version-sensitive. A family name is not enough for a legal decision.
- **Vira availability** is a runtime/account fact and belongs in a live catalog, not in this static ecosystem list.

## Recommended record shape

When adding a model, include the exact family and checkpoint, upstream URL, model-card URL, license URL, capabilities, languages, known limitations, last verification date, and a separate runtime availability field. Do not turn an ecosystem reference into a product promise.
