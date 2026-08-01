---
title: AI Workloads
tags: [azure, ai, ai-900]
up: "[[azure]]"
---

# AI Workloads

Identifying which kind of AI workload a scenario calls for. This is the routing note for [[azure-ai-901]] — each workload below has its own atomic note.

| Workload | Use when | Note |
| --- | --- | --- |
| Generative AI | You need new human-like content created | [[generative-ai-models]] |
| Agentic AI | You need multi-step tasks automated | [[foundry-agents]] |
| Text analysis (NLP) | You have existing text to extract meaning from | [[text-analysis-nlp]] |
| Speech AI | You have audio input or output | [[speech-ai]] |
| Computer vision | You have existing images or video | [[computer-vision]] |
| Information extraction | You need structured data out of unstructured documents | [[information-extraction]] |

## Generative AI

The goal is to create new human-like content, such as writing text, generating images, or producing code.

## Agentic AI

The goal is to automate multi-step tasks by combining reasoning, tools, and decision-making.

## Text analysis (NLP)

When working with existing text to extract meaning or insights.
Example: sentiment analysis on customer reviews.

## Speech AI

When working with audio input or output.
Example: transcribe an online meeting.

## Computer vision

When working with existing images and video.
Example: detecting objects in images.

## Information extraction

When you need to pull structured data from unstructured documents.
Example: entering data from paper/PDF invoices from an external vendor into the accounting system.

## Choosing between them

It's common for a production workload to chain **multiple** services together — a single scenario rarely maps to exactly one box above.

When picking, weigh:

- Latency.
- Accuracy.
- Cost.
- [[responsible-ai]] considerations.
