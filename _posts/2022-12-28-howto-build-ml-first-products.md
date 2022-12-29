---
layout: post
title: "How to build ML-first products"
author: Gaurav Chakravorty
date: 2022-06-24
categories: [ml/ai/nlp, product]
tags: [recsys, strategy]
---

[https://recsysml.substack.com/p/how-to-build-ml-first-products](https://recsysml.substack.com/p/how-to-build-ml-first-products)

> # Problems
>
> ## **#1** Sprinkling ML late in the product does not work well.
>
> > “The problem is that ML takes time and iteration to do well and some product teams continue to think of ML as the last 20% in the 80/20 or the Run in Crawl/Walk/Run and this usually means they are not investing in ML till very late in the product development cycle.”
>
> ## **#2** Expecting too much too soon from ML.
>
> a) ML takes time due to its high dependency on data, computation and iterative nature of learning. At times gains from this “disruptive technology” are “unknowable” in advance (*Innovator’s Dilemma* reference expanded later in the article.)
>
> b) Typically product stakeholders can “bootstrap” rules based solutions to enhance their intuition and get a better understanding of what business objectives / user-inputs would be critical. Product should provide this business intuition to incorporate into the ML solution for a better user experience and higher velocity of development.
>
> ## **#4** ML team should own user-problems and not act as consultants to product teams.
>
> a) In this article we are advocating using ML in products that need ML to deliver a 10X performance. Setting up ML as consultants/platform teams hurts the product and makes ML engineers feel less empowered.
>
> > Successful outcomes come from examples where teams own user-problems and work together across product and ML expertise to solve them as one team.
>
> b) Successful examples in the industry that have done this:
>
> 1. Youtube Home team (ML/backend SWEs + UI SWEs in same team),
> 2. Other examples: TikTok, FB News feed, Twitter Notifications, High Frequency Trading
>
> ## **#5** Building in-house ML infra is expensive and risky.
>
> a) Today, there is state of the art ML infrastructure as a service available at low costs (e.g. [serving](https://cloud.google.com/vertex-ai/docs/featurestore/serving-online), [searching](https://vespa.ai/), [embedding search](https://www.pinecone.io/docs/examples/), [feature store](https://www.featurestore.org/), [model training pipelines](https://www.tensorflow.org/tfx), [recommender systems](https://github.com/tensorflow/recommenders))
>
> b) Some companies who have built infra in house are facing the same transformation that teams inside Google, MSFT, Twitter went through over the last 5 years. Most had built their own infra but chose to sunset them and switch over to centralized solutions.
>
> c) Building infra in house is not only costly but incurs the organizational headwind that makes #4 hard. Internal ML infra will force an org design where ML teams are centralized. They will have to set up ML-enabled services a certain way.
>
> d) For most companies, I recommend using external ML infra and **building only what is uniquely value-adding** to your company.
