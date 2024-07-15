---
title: 'Paper reading: ChatDev: Communicative Agents for Software Development [extensive reading]'
typora-root-url: ./..
typora-copy-images-to: ../medias/${filename}
date: 2024-07-15 15:47:56
categories:
  - Paper Reading
tags:
  - NLP
  - LLMs
  - Paper Reading
---

# ChatDev: Communicative Agents for Software Development

arXiv 2024, THUNLP

a chat-powered software development framework integrating multiple "software agents" for active involvement in three core phases of the software lifecycle: design, coding, and testing

Communicative De-hallucination

## Strength:

- Novel Communicative De-hallucination
- Agent-based self-consistency?
- Defines dataset, goal, and metric

## Concerns:

- Mainly on evaluation metrics.
- Completeness – Why there will be incomplete code?
- How do you define executability?
  - How much code can be compiled isn’t a good metric
  - Python?
- Consistency – weird definition
  - Semantic embedding of software code with textual requirements
  - WHY?
- Quality:
  - Multiply of completeness, executability, and consistency
  - Okay
