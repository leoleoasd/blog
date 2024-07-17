---
title: 'Paper reading: MIND2WEB: Towards a Generalist Agent for the Web'
typora-root-url: ./..
typora-copy-images-to: ../medias/${filename}
categories: Paper Reading
tags:
  - NLP
  - LLM
  - Paper Reading
date: 2024-07-16 20:10:52
---

# MIND2WEB: Towards a Generalist Agent for the Web

OSU-NLP, NIPS 2023 Dataset Track

A dataset of real tasks on real-world websites, including tasks and user interaction traces.

![image-20240716201230890](/medias/Paper-reading-MIND2WEB-Towards-a-Generalist-Agent-for-the-Web/image-20240716201230890.png)

## Strength

* Very good project homepage -- https://osu-nlp-group.github.io/Mind2Web/
* annotation process:
  * human-annotated dataset
  * select element then select action
* Method:
  * two-step.
    1. select candidate dom elements
       1. a 0-1 score for **Each Candidate Element**
       2. random negative samples
    2. Generate action
       1. a multi-choice on the candidate element

## Challenges

* a 0-1 score for each candidate element is too complex
  * you need many calls for a single action
  * unfeasible
