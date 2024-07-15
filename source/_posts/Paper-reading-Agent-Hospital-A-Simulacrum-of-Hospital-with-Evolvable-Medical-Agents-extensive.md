---
title: >-
  Paper reading: Agent Hospital: A Simulacrum of Hospital with Evolvable Medical
  Agents [extensive reading]
typora-root-url: ./..
typora-copy-images-to: ../medias/${filename}
date: 2024-07-15 15:38:16
categories:
  - Paper Reading
tags:
  - NLP
  - LLMs
  - Paper Reading
---

arXiv 2024, THUNLP

RQ: Could the process of social simulation enhance the performance of LLM agents on specific tasks?

## Strength:

- Very novel and interesting RQ, achieving SOTA on MedQA
- Solid methodology?

## Concerns:

- In the training method – Where is the ‘agent’?
  - There are no triage, registration, … processes involved in their experiment
    - –which is the most important part of simulated agent I think
  - They are just building a new dataset
  - Of course the accuracy will raise
  - **Didn’t answer their RQ at all.**
- They are calling it ‘training’. Are they updating parameters? It seems like they are just constructing a structured database (medical record library and experience base) for RAG.
- No comparison to non-agent baselines (search through all documents in their dataset, or just fine-tuning)
- Very doubtful evaluation (only 72 questions; didn’t talk about how they select questions; select correct questions with GPT-3.5 but evaluate GPT-4, …)
