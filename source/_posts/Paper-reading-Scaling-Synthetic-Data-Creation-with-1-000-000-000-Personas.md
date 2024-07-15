---
title: 'Paper reading: Scaling Synthetic Data Creation with 1,000,000,000 Personas'
typora-root-url: ./..
typora-copy-images-to: ../medias/${filename}
categories: Paper Reading
tags:
  - NLP
  - LLM
  - Paper Reading
date: 2024-07-15 16:19:28
---

Create 1B personas, open-sourced 200k of them

Target: synthetic data for better LLM training

Persona -> task

Beats 70b open-source model with 7b compact model

* Text-to-persona: use any text as input to obtain corresponding personas just by prompting the LLM “Who is likely to [read|write|like|dislike|...] the text?”

* Persona-to-Persona: persona relationship expansion

```json
{
 "input persona": "A software engineer who disagrees with the established computer scientist's methodologies and approaches",
 "synthesized text": "The software engineer, John, is working on a project where he needs to calculate the time complexity of his newly developed algorithm. He disagrees with the established computer scientist's methodologies and approaches and wants to use his own method. \n\nJohn's algorithm is a recursive function that calls itself twice for each level of recursion. The base case (when the recursion stops) occurs when the input size is 1. \n\nGiven that the time taken by the algorithm when the input size is 1 is C (a constant), John needs to express the time complexity T(n) of his algorithm as a recurrence relation. \n\nWhat is the recurrence relation for the time complexity of John's algorithm?",
 "description": "math problem"
}
```



Concerns

- May not be that related to our use-case?
  - They are trying to synthetic more high-quality training data for LLM pre-training
