---
title: Information Extraction
tags: [azure, ai, ai-900, document-intelligence]
up: "[[azure]]"
---

# Information Extraction

Extracting useful information from text, images, audio, and video — converting unstructured data into structured, searchable, useful information. One of the workloads in [[ai-workloads]].

## By source type

| Source | Technique |
| --- | --- |
| Text | NLP techniques — see [[text-analysis-nlp]] |
| Images | OCR, object detection, image classification — see [[computer-vision]] |
| Audio | Transcription then analysis — see [[speech-ai]] |
| Video | Frame analysis plus audio track |
| Documents | Azure AI Document Intelligence, below |

## Azure AI Document Intelligence

The goal is to convert document data into structured information that can be stored in databases or business systems.

**Prebuilt models** are available for common document types:

- Invoices.
- Receipts.
- ID cards.
- Business cards.

**Custom models** can be trained to extract information from organization-specific forms.

## Related

- [[microsoft-foundry]] — Document Intelligence is one of the Foundry Tools.
- [[azure-cosmos-db]] / [[azure-storage]] — where the extracted structured output usually lands.
