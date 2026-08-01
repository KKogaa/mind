---
title: Responsible AI
tags: [azure, ai, ai-900, ai-102, responsible-ai]
up: "[[azure]]"
---

# Responsible AI

Microsoft's framework for building AI systems that are trustworthy. Examined in both [[azure-ai-901]] (AI-900) and [[azure-ai-103-microsoft-learn]] (AI-102), and a design constraint on every workload in [[ai-workloads]].

## Why it exists: unintended consequences

Without guardrails an AI system can produce decisions that are:

- Wrong.
- Illegal.
- Unexplainable by anybody.
- Harmful to society at large.

> tldr: AI isn't explainable and can go out of control, usually because it was given too many privileges.

## The six principles

| Principle | Core question |
| --- | --- |
| Fairness | Does it treat everyone equally? |
| Reliability and safety | Does it behave consistently, even under stress? |
| Privacy and security | Is user data protected? |
| Inclusiveness | Does everyone benefit from it? |
| Transparency | Can we explain how a decision was made? |
| Accountability | Who is answerable for how it operates? |

### Fairness

AI systems should treat everyone fairly and avoid affecting similarly situated groups of people in different ways.

> tldr: AI should treat everyone equally, with equal opportunity, avoiding discrimination.

### Reliability and safety

To build trust, it's critical that AI systems operate reliably, safely, and consistently under normal circumstances *and* in unexpected conditions.

### Privacy and security

Many countries and regions are developing new standards and laws to protect the data of their citizens. Laws are always slower than technology.

### Inclusiveness

Everyone should benefit from intelligent technology, meaning it must incorporate and address a broad range of human needs and experiences.

e.g. working to make AI voice models comprehend different types of accents — see [[speech-ai]].

### Transparency

When AI systems help inform decisions with large impacts on people's lives, it is critical that people understand how those decisions were made.

e.g. when someone is rejected by an AI system for a job, life insurance, or a bank loan — why were they rejected? If you can't tell them, the system lacks transparency.

### Accountability

The people who design and deploy AI systems must be accountable for how their systems operate.

e.g. AI should not be the "final authority" in any decision with major impact on people's lives (employment, finances, health care, human safety). There should be regular review of how the AI is operating, and regular improvement of the model.

## Considerations for fairness in a solution

An AI system should produce equitable outcomes for all people, regardless of demographic characteristics such as race, gender, age, disability, religion, or socioeconomic status.

Five aspects where fairness needs to be taken into consideration:

- **Training data bias** — the model learns from historical records and predicts from them; if the history is biased, the system inherits that bias.
- **Performance parity** — when splitting training from testing data, verify the system treats e.g. men and women, or different races, equally well.
- **Sensitive feature leakage** — you shouldn't be able to infer protected attributes back out of the training data.
- **Allocation vs quality of service** — the system shouldn't allocate better salaries, or deliver better service quality, based on race.
- **Feedback loops** — feeding AI output back in as AI input to correct errors compounds those errors over time.

## Considerations for reliability and safety in a solution

An AI system must behave consistently, handle unexpected inputs gracefully, and not cause harm — whether through failure, misuse, or adversarial attack.

Practical levers when deploying: content filters and safety settings, plus monitoring and logging. See [[generative-ai-models]] for where these sit in a deployment.

## Related

- [[microsoft-foundry]] — where content filters and evaluations are configured in practice.
- [[prompt-engineering]] — system prompts carry the safety boundaries.
