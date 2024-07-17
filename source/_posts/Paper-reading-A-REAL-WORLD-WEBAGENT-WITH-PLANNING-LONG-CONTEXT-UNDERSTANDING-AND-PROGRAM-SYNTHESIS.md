---
title: >-
  Paper reading: A REAL-WORLD WEBAGENT WITH PLANNING, LONG CONTEXT
  UNDERSTANDING, AND PROGRAM SYNTHESIS
typora-root-url: ./..
typora-copy-images-to: ../medias/${filename}
categories: Paper Reading
tags:
  - NLP
  - LLM
  - Paper Reading
date: 2024-07-16 20:29:36
---

# A REAL-WORLD WEBAGENT WITH PLANNING, LONG CONTEXT UNDERSTANDING, AND PROGRAM SYNTHESIS

Deepmind, ICLR 2024

## Motivation

LLM Agents in real-world websites has still suffered from open domainness, limited context length and lack of inductive bias on HTML.

They introduce WebAgent, an LLM-driven agent that learns from self experience to complete tasks on real websites following natural language instructions.



## Strength

* method:
  * two-model method. 
    * HTML-T5 to predict the next sub-instruction (planning) and generate related HTML snippets (summarization)
    * Flan-U-PaLM prompted to generate Python programs 
  * Action is represented by python programs with selenium driver calls.
    * a large action space
    * flexbility
* Supports any website without predefined action spaces.

## Challenges

* method: a bit complicated
* action representation: safety? Run generated code from LLM is not safe.
* Use a smaller model for planning -- WHY?

