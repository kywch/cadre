---
layout: post
title: "You are probably doing MLOps at a reasonable scale. Embrace it. "
author: neptune.ai
date: 2022-03-23
categories: ml/ai/nlp
tags: mlops
---

[https://thesequence.substack.com/p/-guest-post-you-are-probably-doing](https://thesequence.substack.com/p/-guest-post-you-are-probably-doing)

> Most of the good blog posts, whitepapers, conference talks, and tools are created by people from super-advanced, hyperscale companies. Companies like Google, Uber, and Airbnb, who have hundreds of people working on ML problems that serve trillions of requests a month.
>
> That means most of the best practices you find are naturally biased toward hyperscale. But **99% of companies are not doing production ML at hyperscale**.
>
> Most companies are either not doing any production ML yet or do it at a[ reasonable scale, a term coined last year by Jacopo Tagliabue.](https://towardsdatascience.com/ml-and-mlops-at-a-reasonable-scale-31d2c0782d9c) Reasonable scale as in five ML people, ten models, millions of requests. Reasonable, demanding, but nothing crazy and hyperscale.

> But there are examples of **pragmatic companies achieving great results by embracing reasonable scale MLOps limitations**:
>
> - [Lemonade](https://open.spotify.com/episode/6v1eDLc1PkQPzgzkxzBJXA?si=730b0a3fcda74d7a) generates $100M+ in annual recurring revenue from ML models with just 2 ML engineers serving 20 data scientists.
> - [Coveo](https://open.spotify.com/episode/5AxI8KVtm5PsN8HzprUVG2?si=9951085620314616) leverage tools to deliver recommendation systems to thousands of companies with (almost) no ML infrastructure people.
> - [Hypefactors](https://neptune.ai/customers/hypefactors) runs NLP/CV data enrichment pipelines on the entire social media landscape with a team of just a few people.

>  Some things that are clear(ish) is that **there are five main pillars of MLOps** that you need to implement somehow:
>
> - Data ingestion (and optionally feature store)
> - Pipeline and orchestration
> - Model registry and experiment tracking
> - Model deployment and serving
> - Model monitoring
>
> Each of those **can be solved with a simple script or a full-blown solution depending on your needs.**
>
> The decision boils down to whether you want:
>
> - an end-to-end platform vs a stack of best-in-class point solutions 
> - to buy vs build vs maintain open-source tools (or buy and build and maintain oss).
>
> The answer, as always, is “it depends”.
