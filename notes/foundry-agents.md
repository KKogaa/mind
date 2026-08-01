---
title: Foundry Agents
tags: [azure, ai, ai-102, foundry, agents]
up: "[[azure]]"
---

# Foundry Agents

Creating and testing a single-agent solution in [[microsoft-foundry]]. Agentic AI is the workload that automates multi-step tasks by combining reasoning, tools, and decision-making — see [[ai-workloads]].

## Create an agent in the portal

In Foundry, go to **Agents → Create agent**.

![[Pasted image 20260728144629.png]]

From there you select the model, the system prompt, and the tools the agent can use. The system prompt is what defines the agent's behavior and boundaries — see [[prompt-engineering]].

![[Pasted image 20260728144711.png]]

## Attaching tools

Tools are what turn a model into an agent. Example: attaching Google Drive as a tool the model can call.

![[Pasted image 20260728144938.png]]

## Lightweight client application for an agent

Using the Azure AI project client — see [[foundry-sdk]] for which client type to reach for.

![[Pasted image 20260728145152.png]]

![[Pasted image 20260728145232.png]]

![[Pasted image 20260728145258.png]]

![[Pasted image 20260728145331.png]]

## Related

- [[responsible-ai]] — accountability matters more once the model can take actions, not just produce text.
