---
layout: post
title: "Three pillars of data science"
author: Cameron Davidson-Pilon
date: 2018-06-20
categories: data
tags: causal-inference
---

[https://dataorigami.net/blogs/napkin-folding/three-pillars-of-data-science](https://dataorigami.net/blogs/napkin-folding/three-pillars-of-data-science)

> **Description**
> Description is what I feel the majority of data scientists in industry focus on. This could be something as simple as mean, a conversion rate, a time series, etc. or something more advanced like a statistical test. Description also includes data mining algorithms like clustering and association rules. 

> **Prediction**
> We spend most of our time thinking, implementing, watching and talking about prediction. Many times a day, a new ML prediction algorithm or article will surface on Hacker News. Contrast where we are today with the previous century: we have lots of compute power, available datasets and accessible technology for prediction. 

> **Causal Inference**
> So why should a data scientist know about causal inference? From my experience, a data scientist gets asked questions that can only be answered with a causal inference lens. Questions like, to use my company Shopify as an example:
> *  What is the impact on sales of merchants who adopt our point-of-sale system?
> *  What is causing merchants to leave our platform?
> *  What is the effect of server latency on checkouts? 
> 
> These questions, because of the complex nature of the system, cannot be answered with traditional summary statistics. Confounders abound, and populations are biased. We require new tools and ideas that come from causal inference. 
>
> Randomised control trials (RCTs) are very common in tech companies. This classical technique is actually generalised in causal inference frameworks. Beyond this, as a data scientist working in industry, you'll have a new perspective on what your observational data can (and cannot!) deliver. 
