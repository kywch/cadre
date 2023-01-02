---
layout: post
title: "RT-1: Robotics transformer"
author: Keerthana Gopalakrishnan, Kanishka Rao, Robotics at Google, Everyday Robots
date: 2022-12-13
categories: ml/ai/nlp
tags: [transformer, large-language-model]
---

[https://ai.googleblog.com/2022/12/rt-1-robotics-transformer-for-real.html](https://ai.googleblog.com/2022/12/rt-1-robotics-transformer-for-real.html)

[https://robotics-transformer.github.io/](https://robotics-transformer.github.io/)

https://github.com/google-research/robotics_transformer

> Several factors contribute to this challenge. First, there’s the lack of large-scale and diverse robotic data, which limits a model’s ability to absorb a broad set of robotic experiences. Data collection is particularly expensive and challenging for robotics because dataset curation requires engineering-heavy [autonomous](https://karolhausman.github.io/mt-opt/) [operation](https://www.deepmind.com/blog/stacking-our-way-to-more-general-robots), or demonstrations [collected using human teleoperations](https://sites.google.com/corp/view/bc-z/home). A second factor is the lack of expressive, scalable, and fast-enough-for-real-time-inference models that can learn from such datasets and generalize effectively.
>
> To address these challenges, we propose the [Robotics Transformer 1](http://robotics-transformer.github.io/assets/rt1.pdf) (RT-1), a multi-task model that [tokenizes](https://en.wikipedia.org/wiki/Lexical_analysis#Tokenization) robot inputs and outputs actions (e.g., camera images, task instructions, and motor commands) to enable efficient inference at runtime, which makes real-time control feasible. This model is trained on a large-scale, real-world robotics dataset of 130k episodes that cover 700+ tasks, collected using a fleet of 13 robots from [Everyday Robots](https://everydayrobots.com/) (EDR) over 17 months. 
> 
> We demonstrate that RT-1 can exhibit significantly improved zero-shot generalization to new tasks, environments and objects compared to prior techniques. Moreover, we carefully evaluate and ablate many of the design choices in the model and training set, analyzing the effects of tokenization, action representation, and dataset composition. Finally, we’re open-sourcing the [RT-1 code](http://github.com/google-research/robotics_transformer), and hope it will provide a valuable resource for future research on scaling up robot learning.
