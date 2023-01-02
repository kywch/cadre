---
layout: post
title: "Foundation models: The future isn't happening fast enough -- Better tooling will make it happen faster"
author: Jon Turow, Ishani Ummat, Tim Porter, Palak Goel
date: 2022-10-12
categories: ml/ai/nlp
tags: [strategy, large-language-model]
---

[https://www.madrona.com/foundation-models-create-opportunity-tooling-layer/](https://www.madrona.com/foundation-models-create-opportunity-tooling-layer/)

> The problem developers face today is the heavy friction that makes it difficult to build great applications on top of the foundation models. 
>
> **First, running these models requires specialized hardware such as GPUs and a massive amount of compute.** That imposes operational constraints that severely limit the throughput and concurrency available to developers. It also imposes fees so high that it’s untenable for even basic use cases. Developers try to address this by using older generation models wherever possible, or they’ll try open-source versions of smaller models or train task-specific models of their own. But those approaches undermine the reasons to use foundation models in the first place.
>
> **Second, the models don’t “just work” because they’re meant to be only one component of a broader software stack.** Coaxing the best possible inferences from the foundation models today requires each application developer to take many ancillary steps. For example, GPT-3 finished training in late 2019, meaning that the model does not know today’s weather or stock prices and has never heard of COVID-19. So, developers must invent their own tools for steps such as prompt engineering, fine-tuning, distillation, and assembling and managing pipelines that refer queries to the appropriate endpoint.
>
> **Third, the foundation models demand to be treated with kid gloves because we never quite know what they will say or do.** Generative models, such as DALL-E or GPT-3, are often “right,” but it can be devilishly hard to identify when they’re “wrong.” Still more challenging, training foundation models on data sourced from the open internet means we’re holding up a mirror to society’s darkest corners. [We risk biased, offensive, and tangential results](https://www.wired.com/story/efforts-make-text-ai-less-racist-terrible/). The providers of these models, and the application developers who build on top of them, must accept the responsibility of managing those risks.
