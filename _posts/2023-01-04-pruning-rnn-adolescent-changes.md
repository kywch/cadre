---
layout: post
title: "Pruning recurrent neural networks replicates adolescent changes in working memory and reinforcement learning"
author: Bruno Averbeck
date: 2022-05-27
categories: [research, ml/ai/nlp]
tags: improve-learning
---

[https://www.pnas.org/doi/10.1073/pnas.2121331119](https://www.pnas.org/doi/10.1073/pnas.2121331119)

https://github.com/baverbeck/Pruning-RNNs

> Adolescent development is characterized by an improvement in multiple cognitive processes. While performance on cognitive operations improves during this period, the ability to learn new skills quickly, for example, a new language, decreases. During this time, there is substantial pruning of excitatory synapses in cortex and specifically in prefrontal cortex. 
>
> We have trained a series of recurrent neural networks to solve a working memory task and a reinforcement learning (RL) task. Performance on both of these tasks is known to improve during adolescence. After training, we pruned the networks by removing weak synapses. Pruning was done incrementally, and the networks were retrained during pruning. 
>
> We found that **pruned networks trained on the working memory task were more resistant to distraction**. The **pruned RL networks were able to produce more accurate value estimates and also make optimal choices more consistently**. Both results are consistent with developmental improvements on these tasks. 
>
> **Pruned networks, however, learned some, but not all, new problems more slowly.** 
>
> Thus, improvements in task performance can come at the cost of flexibility. Our results show that overproduction and subsequent pruning of synapses is a computationally advantageous approach to building a competent brain.
