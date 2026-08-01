---
title: Generative AI Models
tags: [azure, ai, ai-900, generative-ai]
up: "[[azure]]"
---

# Generative AI Models

How generative models work, how to pick one, and how to deploy it. One of the workloads in [[ai-workloads]].

## How they work

Generative AI models *create new content* — images, text, audio, or code.

Most modern GenAI models are based on deep learning, particularly neural networks trained on large datasets.

## Identifying an appropriate model

Match the model to the capability the scenario needs — text generation, image generation ([[computer-vision]]), speech ([[speech-ai]]), or embeddings for search. The model card in the [[microsoft-foundry]] portal shows capabilities, pricing, context window, and token limits, which is where this decision is usually made in practice.

## Deployment options

- **Cloud-based service** — send requests and receive responses over the internet.
- **Managed service** (Foundry tools):
	- Simplicity.
	- Speed.
	- Minimal maintenance.
- **Custom environment** (run locally):
	- Control over performance.
	- Control over security.
	- Control over integration.

Things to decide alongside the hosting choice:

- Real time or batch? When do we need the model inference?
- Latency requirements.
- Scalability.
- Content filters and safety settings — see [[responsible-ai]].
- Monitoring and logging.

## Inference configuration parameters

These control how the model behaves during inference, and together they balance **creativity against accuracy**:

- **Temperature** — controls randomness vs deterministic behavior.
- **Max tokens** — caps response length.
- **Top-p** (nucleus sampling) — restricts sampling to the most probable token mass.

## Related

- [[prompt-engineering]] — the other half of controlling model output.
- [[foundry-sdk]] — calling deployed models from code.
