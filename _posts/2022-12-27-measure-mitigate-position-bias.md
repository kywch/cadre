---
layout: post
title: "How to measure and mitigate position bias"
author: Eugene Yan
date: 2022-04-21
categories: [ml/ai/nlp]
tags: recsys
---

[https://eugeneyan.com/writing/position-bias](https://eugeneyan.com/writing/position-bias)

> Position bias happens when higher positioned items are more likely to be seen and thus clicked *regardless of their actual relevance*. This leads to lesser engagement on lower ranked items. On Google Search, users click on the first position [10x more than the tenth position](https://www.sistrix.com/blog/why-almost-everything-you-knew-about-google-ctr-is-no-longer-valid/).
>
> Because of position bias, it’s difficult to tell if users are engaging on recommendations because they’re truly relevant, or because the recommended item happens to rank highly. Training our models on biased historical data perpetuates the bias via a self-reinforcing feedback loop. This can lead to suboptimal outcomes where items that are more relevant but are shown in lower positions continue to get lower engagement and thus don’t improve their rank.
>
> ## Measuring position bias via randomness
>
> The straightforward way is to **shuffle (top) results uniformly at random** (*[RandN](https://dl.acm.org/doi/10.1145/2911451.2911537) or RandTopN*). This controls for item relevance by having the same item appear in multiple positions. Thus, any difference in customer engagement can be cleanly attributed to position bias. The downside is that this adversely impacts the customer experience and is usually too costly or out of the question.
>
> Another approach is to **exploit the inherent randomness** in item positions. We see this in historical data when we have multiple rankers in production or when the production ranker is updated frequently. This lets us to [estimate position bias without intrusive interventions](https://arxiv.org/abs/1812.05161) like RandTopN. Nonetheless, unless we’re operating on a large scale with multiple rankers updating frequently, it can be hard to get such data.
>
> Another approach is to **infer position bias via expectation maximization**. One way is to [model clicks via a position bias model](https://dl.acm.org/doi/10.1145/3159652.3159732). In the model, an item is clicked only if it is examined and relevant; examination depends only on the position while relevance depends only on the context and item. Google demonstrated this approach’s effectiveness on search logs from email and file storage services where there was only a single click for most queries. To do this, they represented queries and items via features instead of IDs.
>
> A middle ground is to **add a bit of randomness** into item positions. For example, *[Fair](https://arxiv.org/abs/cs/0605037)[Pairs](https://dl.acm.org/doi/abs/10.1145/1341531.1341545)* swaps items at positions *k* and *k+1* while *[RandPair](https://arxiv.org/abs/1608.04468)* swaps items at positions *1* and *k*. Similar to *RandN*, this keeps item relevance constant so we can measure the difference in customer engagement due to position bias. One downside is that RandPair can degrade customer experience especially if *k* is large.
>
> One way is [Boltzmann exploration](https://arxiv.org/abs/1705.10257) where we (i) normalize/softmax the raw scores into probabilities and then (ii) sample the recommendations (based on these probabilities) as we populate our widget starting from position 1. This gives each recommended item a chance to gain a higher position weighted by recommendation probability (which we can also use in [counterfactual evaluation](https://eugeneyan.com/writing/counterfactual-evaluation/#evaluating-recsys-as-an-interventional-problem)). Unlike *RandTopN*, these approaches anchor each item to its original position before adding randomness, possibly reducing the negative customer impact.
>
> ## Mitigating position bias
>
> If adding randomness is not an option, we can use the measured/learned position bias to debias logged data. For example, the previous Google paper used inferred position bias to train models optimized on [inverse propensity weighted precision](https://dl.acm.org/doi/10.1145/3159652.3159732).
>
> Alternatively, we can account for position bias by including positional features in our models. These positional features help the model learn how position affects reward. Then, during serving, we can set all items to have positional feature = 1 to negate the impact of position. More in Google’s [Rules of Machine Learning](https://developers.google.com/machine-learning/guides/rules-of-ml#rule_36_avoid_feedback_loops_with_positional_features).
