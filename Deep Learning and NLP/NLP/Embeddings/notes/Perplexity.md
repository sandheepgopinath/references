---
tags: [Notebooks/NLP]
title: Perplexity
created: '2022-03-12T09:02:41.170Z'
modified: '2022-03-12T09:20:56.921Z'
---

# Perplexity

- Perplexity is an evaluation matrix
- There are two types of evaluation
  - Extrinsic evaluation 
    - This is when we run a model with an actual task, and look at their final loss or accuracy by looking at the effectiveness of the output. But this process is slow and expensive
  - Intrinsic evaluation
    - Evaluating the language model itself without taking into account any specific tasks it is used for. 
    - It is not as good as extrinsic evaluation as a final metric but is a useful wya of quickly comparing models
    - **Perplexity** is a intrinsic evaluation method


