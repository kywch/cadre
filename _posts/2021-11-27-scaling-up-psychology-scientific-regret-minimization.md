---
layout: post
title: "Scaling up psychology via Scientific Regret Minimization"
author: Mayank Agrawal, Joshua C. Peterson & Thomas L. Griffiths
date: 2020-04-21
categories: [research, ml/ai/nlp, cognitive, statistics]
tags: [best-practice, to-dos]
---

[https://www.pnas.org/content/117/16/8825](https://www.pnas.org/content/117/16/8825)

> Do large datasets provide value to psychologists? Without a systematic methodology for working with such datasets, there is a valid concern that analyses will produce noise artifacts rather than true effects. 
>
> In this paper, we offer a way to enable researchers to systematically build models and identify novel phenomena in large datasets. 
>
> * One traditional approach is to analyze the residuals of models—the biggest errors they make in predicting the data—to discover what might be missing from those models. 
> * However, once a dataset is sufficiently large, machine learning algorithms approximate the true underlying function better than the data, suggesting, instead, that **the predictions of these data-driven models should be used to guide model building.** 
>
> We call this approach “Scientific Regret Minimization” (SRM), as it focuses on minimizing errors for cases that we know should have been predictable. We apply this exploratory method on a subset of the Moral Machine dataset, a public collection of roughly 40 million moral decisions. 
>
> Using SRM, we find that incorporating a set of deontological principles that capture dimensions along which groups of agents can vary (e.g., sex and age) improves a computational model of human moral judgment. Furthermore, we are able to identify and independently validate three interesting moral phenomena: criminal dehumanization, age of responsibility, and asymmetric notions of responsibility.

