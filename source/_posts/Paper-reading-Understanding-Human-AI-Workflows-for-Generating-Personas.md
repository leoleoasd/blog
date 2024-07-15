---
title: 'Paper reading: Understanding Human-AI Workflows for Generating Personas'
typora-root-url: ./..
typora-copy-images-to: ../medias/${filename}
categories: Paper Reading
tags:
  - NLP
  - LLM
  - Paper Reading
date: 2024-07-15 15:53:32
---

DIS 2024

Generate persona from text, from the perspective of human-ai collaboration

RQ: which persona-generation subtasks should be delegated to user researchers vs. LLMs to produce representative and empathy-evoking personas?

![image-20240715162107072](/medias/Paper-reading-Understanding-Human-AI-Workflows-for-Generating-Personas/image-20240715162107072.png)

## Strength:

- Interesting finding
  - introducing user researcher in identifying key characteristics make the age variance smaller
  - Llm-auto can match the golden truth distribution
  - Llm-summary can generate the most statistically representative personas

## Concerns:

- (somewhat) trivial findings (llm-summary and llm-grouping performs the best):
  - Introducing user researcher in more stages will yield a better performance
  - No-LLM baseline (how does summarizing help?)
  - Human workflow – which part is the most time-consuming?
- How do you define a better “persona”
  - What the usage of personas? Are they going to be processed by LLMs?
  - Will “be more expressive” help?
