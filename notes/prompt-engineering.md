---
title: Prompt Engineering
tags: [azure, ai, ai-900, ai-102, generative-ai]
up: "[[azure]]"
---

# Prompt Engineering

Creating effective prompts for generative AI models. Prompts are the instructions or input given to a GenAI model — the other half of output control alongside the inference parameters in [[generative-ai-models]].

Well-designed prompts produce outputs that are more accurate, relevant, consistent, and useful.

## Two types of prompt

### System prompt

Defines the model's overall behavior, role, or rules. Usually hidden from the end user and set by the developer.

Establishes:

- Tone.
- Personality.
- Formatting rules.
- Safety boundaries — the enforcement point for [[responsible-ai]].
- Response style.

![[Pasted image 20260728140553.png]]

On systems like ChatGPT you cannot see the system prompt; in [[microsoft-foundry]] you can edit it.

### User prompt

The direct request entered by the user, describing the task the model should perform, e.g. "Summarize the attached document."

Good user prompts include:

- Context.
- Desired output format.
- Constraints.
- Examples.

## Techniques

- Be specific about the task and expected output.
- Provide context to improve relevance.
- Define the desired format.
- Use examples when possible.
- Break complex tasks into smaller steps for more reliable responses.

## Using prompts in Foundry

In [[microsoft-foundry]], prompts can be tested and refined directly within the development environment. Prompt design is a key skill when building generative AI applications and [[foundry-agents]].
