---
layout: post
title: "The First Rule of Machine Learning: Start without Machine Learning"
author: Eugene Yan
date: 2021-09-21
categories: ml/ai/nlp
tags: [mlops, best-practice]
---
[https://eugeneyan.com/writing/first-rule-of-ml/](https://eugeneyan.com/writing/first-rule-of-ml/)

> Guess what’s Rule #1 in Google’s 43 [Rules of Machine Learning](https://developers.google.com/machine-learning/guides/rules-of-ml)?
>
> > **Rule #1: Don’t be afraid to launch a product without machine learning.**
> >
> > Machine learning is cool, but it requires data. Theoretically, you can take data from a different problem and then tweak the model for a new product, but this will likely underperform basic heuristics. If you think that machine learning will give you a 100% boost, then a heuristic will get you 50% of the way there.

> With an understanding of the data, we can then **start by solving the problem with heuristics.** Here are some examples of using heuristics to solve common problems (you’ll be surprised how difficult they are to beat):
>
> - **Recommendations**: Recommend top-performing items from the previous period; can also be segmented by categories (e.g., genres, brands). If you have customer behavior, you can compute aggregated statistics on co-interactions to calculate item similarity for i2i recommendations (see Alibaba’s Swing Algorithm [here](https://eugeneyan.com/writing/real-time-recommendations/#industry-examples-of-real-time-recommendations)).
> - **Product classification**: Regex-based rules on product titles. Here’s an example from [Walmart’s product classifier (Section 4.5)](https://dl.acm.org/doi/10.14778/2733004.2733024): If product title contains “ring”, “wedding band”, “diamond. *bridal”, etc., classify it in the ring category.
> - **Review spam identification**: Rules based on the count of reviews from the same IP, time the review was made (e.g., odd timing like 3 am), similarity (e.g., edit distance) between the current review and other reviews made on the same day.

> ## When should we use machine learning then?
>
> **After you have a non-ML baseline that performs reasonably well**, and the effort of maintaining and improving that baseline outweighs the effort of building and deploying an ML-based system. It’s hard to pinpoint exactly when this happens, but if your 195 handcrafted rules become impossible to update without something breaking, it’s a sign that you should consider machine learning. Here’s Rule #3 from Google’s Rules of ML.
>
> > **Rule #3: Choose machine learning over a complex heuristic.**
> >
> > A simple heuristic can get your product out the door. A complex heuristic is unmaintainable. Once you have data and a basic idea of what you are trying to accomplish, move on to machine learning… and you will find that the machine­-learned model is easier to update and maintain.
>
> **Having robust data pipelines and high-quality data labels also suggests you’re ready for machine learning.** Before this happens, your existing data might not be good enough for machine learning. Say you want to reduce fraud on your platform, but you don’t even know how fraud looks like, let alone have any labels.
