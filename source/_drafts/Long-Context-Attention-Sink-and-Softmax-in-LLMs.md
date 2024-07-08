---
title: Long Context, Attention Sink and Softmax in LLMs
typora-root-url: ./..
typora-copy-images-to: ../medias/${filename}
date: 2024-03-29 11:11:36
tags:
  - English
  - Thoughts
  - NLP
  - Large Language Models
---

Transformers have a notoriously bad time-complexicity $ O(n^2) $ and memory-complexicity in understanding and generating long text. This creates a number of work on making Transformer model accept longer context window (LongT5, ColT5). I actually have two blogs on ColT5 and a folling work, one in [English](https://leoleoasd.me/2023/10/09/paper-reading-think-before-you-speak-training-language-models-with-pause-tokens/) and one in [Chinese](https://leoleoasd.me/2023/03/26/paper-reading-colt5-faster-long-range-transformers-with-conditional-computation/).

But, this post tries to talk about some other related works in this field. 
