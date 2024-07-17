---
title: >-
  Paper reading: RAP: Retrieval-Augmented Planning with Contextual Memory for
  Multimodal LLM Agents
typora-root-url: ./..
typora-copy-images-to: ../medias/${filename}
categories: Paper Reading
tags:
  - NLP
  - LLM
  - Paper Reading
date: 2024-07-16 19:36:36
---

# RAP: Retrieval-Augmented Planning with Contextual Memory for Multimodal LLM Agents

NUS, arxiv preprint

## Motivation:

Reflecting past experiences in current decision-making processes, an innate human behavior, continues to pose significant challenges. Addressing this, we propose Retrieval-Augmented Planning (RAP) framework, designed to dynamically leverage past experiences corresponding to the current situation and context, thereby enhancing agents’ planning capabilities.

## Strength

* Retrieve related experience as new ICL examples
* ![image-20240716200249688](/medias/Paper-reading-RAP-Retrieval-Augmented-Planning-with-Contextual-Memory-for-Multimodal-LLM-Agents/image-20240716200249688.png)

## Challenges

* lack of comparison between fine-tunning the model on the memory database

