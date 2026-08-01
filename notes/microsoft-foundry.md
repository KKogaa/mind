---
title: Microsoft Foundry
tags: [azure, ai, ai-900, ai-102, foundry]
up: "[[azure]]"
---

# Microsoft Foundry

Microsoft Foundry is the platform for AI development on Azure. You *can* provision individual AI resources and build applications that consume them without it, but the project organization, resource management, and AI development capabilities make Foundry the recommended way to build all but the simplest solutions.

Two surfaces:

- The **Foundry portal** — covered below.
- The **Foundry SDK** — see [[foundry-sdk]].

## Projects

In Foundry you manage the resource connections, data, code, and other elements of an AI solution in a **project**. Each project belongs to a single Foundry resource in Azure, which provides compute, data storage, AI tools, and other services.

![[Pasted image 20260523123610.png]]

Projects manage assets such as:

- Models.
- Agents — see [[foundry-agents]].
- Tools.
- Knowledge.

## Foundry Tools

| Tool | What it does | Note |
| --- | --- | --- |
| Azure Language | Entity extraction, sentiment analysis, summarization, conversational language models, question answering | [[text-analysis-nlp]] |
| Azure Speech | Text-to-speech, speech-to-text, real-time live speech for conversational apps and agents | [[speech-ai]] |
| Azure Translator | State-of-the-art models to translate text between a large number of languages | — |
| Azure Document Intelligence | Prebuilt and custom models to extract fields from invoices, receipts, and forms | [[information-extraction]] |
| Azure Content Understanding | Multi-modal analysis to extract data from forms, documents, images, videos, and audio streams | [[information-extraction]] |
| Azure AI Vision | Image and video analysis, OCR, face | [[computer-vision]] |
| Content Safety | Filtering and safety enforcement | [[responsible-ai]] |
| Azure AI Search | Retrieval over indexed knowledge | — |

## Deploy a model and interact with it in the portal

1. Log in to Foundry and create a project (or choose an existing one). A project sets up the workspace where you build, customize, and manage agents, tools, and models.

	![[Pasted image 20260728141109.png]]

	![[Pasted image 20260728141240.png]]

2. Switch to the **Discover** tab and select Models.

	![[Pasted image 20260728141339.png]]

3. Pick a model. The **model card** shows capabilities, pricing, context window, and token limits — this is where the model-selection decision in [[generative-ai-models]] actually gets made.

	![[Pasted image 20260728141519.png|697]]

4. Deploy, then test it in the playground, editing the system prompt directly — see [[prompt-engineering]].

	![[Pasted image 20260728141639.png]]

## Related

- [[azure-ai-103-microsoft-learn]] — AI-102 study hub.
- [[azure-ai-901]] — AI-900 study hub.
