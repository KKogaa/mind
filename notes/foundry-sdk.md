---
title: Foundry SDK
tags: [azure, ai, ai-102, foundry, sdk]
up: "[[azure]]"
---

# Foundry SDK

Building a lightweight client application against [[microsoft-foundry]].

A Foundry resource provides unified access to models, agents, and tools. The Foundry SDK is a **thin-client SDK** that exposes all of the Foundry project APIs through a single project endpoint. Higher-level SDKs build on it — e.g. the Agent Framework foundry package depends on the Foundry SDK to access Foundry models, tools, and project configuration.

## Choosing your SDK

| Use | When |
| --- | --- |
| **Foundry SDK** | Building apps with agents, evaluations, or Foundry-specific features |
| **Agent Framework** | Hosted agents or multi-agent systems in code |
| **OpenAI SDK** | Maximum OpenAI compatibility or lowest latency, generating embeddings, or using Foundry direct models via Chat Completions |
| **Anthropic SDK** | Working with Anthropic Claude models deployed in Foundry |
| **Foundry Tools SDKs** | Working with specific AI services — prebuilt vision, speech, content safety, and more |

## Install

```bash
pip install "azure-ai-projects>=2.0.0"
```

## The two client types

The Foundry SDK exposes two client types because Foundry and OpenAI have different API shapes:

- **Project client** — for Foundry-native operations where OpenAI has no equivalent. Example: listing connections, retrieving project properties, enabling tracing.
- **OpenAI-compatible client** — for Foundry functionality that builds on OpenAI concepts. The Responses API, agents, evaluations, and fine-tuning all use OpenAI-style request/response patterns.

## Code examples

Foundry SDK:

![[Pasted image 20260728142135.png]]

![[Pasted image 20260728142159.png]]

![[Pasted image 20260728142337.png]]

![[Pasted image 20260728142436.png|691]]

![[Pasted image 20260728144008.png]]

OpenAI SDK:

![[Pasted image 20260728144151.png]]

Anthropic SDK:

![[Pasted image 20260728144234.png]]

## Python-supported Foundry tools

- **Speech** — speech-to-text, text-to-speech, translation, speaker recognition. See [[speech-ai]].
- **Language** — language detection, PII detection, text analytics for health, sentiment analysis, opinion mining, key phrase extraction, summarization, entity linking, CQA, and CLU. See [[text-analysis-nlp]].
- **Translator**.
- **Azure AI Search**.
- **Content Safety** — see [[responsible-ai]].
- **Document Intelligence** — see [[information-extraction]].
- **Vision** — see [[computer-vision]].

## Related

- [[foundry-agents]] — building a client for an agent rather than a raw model.
