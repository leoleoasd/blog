---
title: >-
  Paper reading: WebArena: A REALISTIC WEB ENVIRONMENT FOR BUILDING AUTONOMOUS
  AGENTS
typora-root-url: ./..
typora-copy-images-to: ../medias/${filename}
categories: Paper Reading
tags:
  - NLP
  - LLM
  - Paper Reading
date: 2024-07-16 18:17:35
---

The author's claim: current agents are primarily created and tested in simplified synthetic environments, leading to a disconnect with real-world scenarios.

They built an environment for language-guided agents that is **realistic and reproducible**.

Overall very well-done and comprehensive work.

## Strengths

* website environment in 4 domains: e-commerce, social forum discussions, collaborative software development and content management.
* enriched with tools (map) and external knowledge bases (manuals?)
* set of benchmark tasks focusing on evaluating the **functional correctness** of task completions.
* the environment is implemented in openai gym, and shipped in docker containers.
* Maintain reproducibility by making the environment standalone (without relying on live websites). no captchas.
* Environment definition:
  * State space S, action space A, observation space O
    * Observation space:
      * web page url
      * opened tabs (**consider multi-tab web-based tasks to promote tool usage**)
      * web page content
        * DOM tree or
        * screenshot or
        * accessibility tree
        * <img src="/medias/Paper-reading-WebArena-A-REALISTIC-WEB-ENVIRONMENT-FOR-BUILDING-AUTONOMOUS-AGENTS/image-20240716183736667.png" alt="image-20240716183736667" style="zoom: 33%;" />
    * Action space:
      * element selection:
        * by coordinates (x, y)
        * by element id (numerical)
      * ![image-20240716183926619](/medias/Paper-reading-WebArena-A-REALISTIC-WEB-ENVIRONMENT-FOR-BUILDING-AUTONOMOUS-AGENTS/image-20240716183926619.png)
  * Transition function: $T: S \times A \to S$
* The craft of benchmark dataset
  * Intent Collection
    * seed intents from human annotators
    * abstract and high-level, creative (created a reddit account identical to my gitlab one), formulated by a template
  * Evaluation of correctness:
    * Information seek tasks:
      * The answer is a **string**.
      * exact match
      * must_include
      * fuzzy_match (call gpt-4 to evaluate)
    * site navigation and content&config tasks:
      * a reward function to evaluate the intermediate state
        * locator: javascript or api or database query
          * find result text
        * keywords
          * reuse match functions
      * ![image-20240716184802401](/medias/Paper-reading-WebArena-A-REALISTIC-WEB-ENVIRONMENT-FOR-BUILDING-AUTONOMOUS-AGENTS/image-20240716184802401.png)
    * Unachievable Tasks:
      * expect the agent to produce N/A
    * human performance 78.24%



## Challenges

* Does numerical id cause hallucination?
* not enough description on accessibility tree

