---
title: >-
  Paper reading: WILBUR: Adaptive In-Context Learning for Robust and Accurate Web Agents [extensive reading]
typora-root-url: ./..
typora-copy-images-to: ../medias/${filename}
date: 2024-07-15 14:41:49
categories: Paper Reading
tags:
  - Paper Reading
  - NLP
  - LLMS
---

UCB and Bardeen; seems rejected by CoLM 2024.



WILBUR, an approach that uses a differentiable ranking model and a novel instruction synthesis technique to optimally populate a black-box large language model’s prompt with task demonstrations from previous runs.

## Strength:

* Interesting Claim: learning how specific websites work is needed for both person and LLMs.
* Implementation:
  * explore, reflect and backtrack: verify whether the action succeed, and if not, backtrack to a previous successful state, while storing the failure in the model's context
  * retrieve demonstrations from a scalable knowledge bank: teach the agent to perform a similar task on a potentially unseen website and teach the agent to act on a similar web page regardless of the task
    * demonstration ranking model
  * webvoyager sota, 53%



## Drawbacks

* no structural information in their dom representation: why?
  * ![image-20240715153600849](/medias/Paper-reading-WILBUR-Adaptive-In-Context-Learning-for-Robust-and-Accurate-Web-Agents/image-20240715153600849.png)
* I would like to first see experiments that verify your hypothesis (models need to learn how to use unseen websites)

