---
layout: post
title: "Bandits for recommender systems"
author: Euguen Yan
date: 2022-05-11
categories: ml/ai/nlp
tags: [recsys, adaptive]
---

[https://eugeneyan.com/writing/bandits/](https://eugeneyan.com/writing/bandits/)

> **Bandits address this by modeling uncertainty and exploration.** By acknowledging the uncertainty in the data and deliberately exploring to reduce it, bandits learn about the relevance of unexplored items.
>
> **This is especially applicable when the item set changes quickly**, such as for news, ads, and tweets, **or when the rate of traffic is low.** If new items are constantly added, waiting to collect batch data before retraining the model can be too slow. Bandits are a good fit as they can incrementally update with new data and adaptively focus on items with higher reward. This reduces regret, which is the opportunity cost while recommending suboptimal items.
>
> We’ll briefly discuss three main bandit algorithms before looking at some industrial implementations of each. Here are a few terms I use throughout: (i) **action/arm**: recommendation candidates, (ii) **reward**: customer interaction from a single trial, such as a click or purchase, (iii) **value**: estimated long-term reward of an arm over multiple trials, and (iv) **policy**: algorithm/agent that chooses actions based on learned values.
>
> **ε-greedy is the classic bandit algorithm.** At every trial, it randomly chooses an action with probability ε and greedily chooses the highest value action with probability 1 - ε. We balance the explore-exploit trade-off via the parameter ε. A higher ε leads to more exploration while a lower ε leads to more exploitation. 
>
> **Upper Confidence Bound (UCB) considers the uncertainty** of an arm and selects arms that have the highest potential. Uncertainty is modeled **via confidence bounds** while potential is represented by the upper confidence bound (thus the name of the algorithm). Because of how it works, UCB is often referred to as “optimism in the face of uncertainty”.
>
> **Thomson Sampling models uncertainty by building a probability distribution** from historical rewards and then samples from the distribution when choosing actions. In the simple case where rewards are binary, a Beta distribution is used.

> ## Lessons on applying bandits in industry
>
> **First, UCB and Thompson Sampling [outperform ε-greedy](https://arxiv.org/abs/1003.0146)**. By default, ε-greedy is unguided and chooses actions uniformly at random. In contrast, UCB and Thompson Sampling are guided by confidence bounds and probability distributions that shrink as the action is tried more often. As a result, because UCB and Thompson Sampling smartly explore arms that have higher uncertainty, they have lower regret.
>
> **Second, when feedback is delayed, Thompson Sampling outperforms UCB.** Delayed feedback, where user-item interactions are not processed immediately, is common for most real-world systems due to resource and run-time constraints. In this situation, because UCB selects arms deterministically, it chooses the same action until new feedback is incorporated. In contrast, because Thompson Sampling chooses actions stochastically by sampling from the posterior distribution, it randomizes over actions even without updated rewards. [Yahoo’s evaluation of Thompson Sampling](https://papers.nips.cc/paper/2011/hash/e53a0a2978c28872a4505bdb51db06dc-Abstract.html) and [Deezer’s music bandit](https://arxiv.org/abs/2009.06546) observed that this led to wider exploration and thus better outcomes. ... Overall, this suggests that stochastic policies are more robust to delay as they continue to explore even without updated rewards.
>
> **Third, how the bandit is initialized makes a difference.** [Deezer](https://arxiv.org/abs/2009.06546) found that pessimistic initialization performed better than naive initialization. For Thompson Sampling, they experimented with naive initialization where the prior was Beta(1, 1) and pessimistic initialization where the prior was Beta(1, 99). Similar naive and pessimistic initialization was adopted for UCB. They found that pessimistic initialization performed better due to the lower prior probabilities which were more reflective of real-world reward.

> ## Exploring new items - two options
>
> The few papers that discussed exploration adopted two main approaches: (i) **large exploration on a limited set of users** vs. (ii) **small exploration on all users**.
>
> For the former, [Yahoo uses an exploration bucket](https://arxiv.org/abs/1003.0146) that users are randomly selected into. Users in the exploration bucket are then served news articles uniformly at random. Similarly, [Twitter has a random ad policy](https://arxiv.org/abs/2008.00727) that serves 1% of production traffic.
>
> For the latter, [Netflix tests new artwork on all users](https://netflixtechblog.com/artwork-personalization-c589f074ad76) (“… the regret incurred by exploration is typically very small and is amortized across our large member base with each member implicitly helping provide feedback on artwork for a small portion of the catalog.”) Similarly, Schibsted adds 5% random items to every input of their bandit ranker.

> ## Addressing the curse of dimensionality
>
> We can represent users via features such as gender, age group, location, behavior, etc. However, **one concern with applying bandits conditioned on these features is the curse of dimensionality**. More dimensions leads to less data for each combination of dimensions.
>
> [Yahoo addressed this by applying PCA](https://arxiv.org/abs/1003.0146) for dimensionality reduction before learning a policy via LinUCB. ... For feature reduction, they projected user features onto article features and then clustered users into five groups where users in each group had similar preferences. This reduced the 1.2k user features into five features. Article features were also reduced in a similar manner.
>
> [Deezer compared](https://arxiv.org/abs/2009.06546) between representing users as clusters (semi-personalization) vs. user features (full personalization). For semi-personalization, users were clustered into 100 groups via k-means clustering on past behavior. This resulted in clusters of users with similar musical tastes. They then trained a separate bandit for each cluster. For full personalization, users were represented via a 97-dimension vector which summarizes user preferences for genres, moods, countries, etc. The vector was obtained by factorizing the user-song interaction matrix. They then trained a contextual bandit on these user features.
>
> **The semi-personalized approach outperformed the fully personalized alternative.** Because the semi-personalized bandits were trained on user clusters, each bandit received more feedback and was thus able to learn more effectively and rank playlists faster.

> ## Warm-starting bandits for better user experience
>
> **To ensure our bandits provide a good user experience from the very first interaction**, it’s typical to learn from previously logged user interactions to warm-start the bandit.
>
> [Doordash shared how they warm-start](https://doordash.engineering/2020/01/27/personalized-cuisine-filter/) their cuisine bandits via higher-level regional data. For each cuisine, they learn a bandit policy at multiple levels (i.e., regional, subregional, user). The top-level bandit is initialized at Beta(α=1, β=1). Then, for each lower-level bandit, they update α by adding the average number of orders for the cuisine (at that level) and update β by adding the average number of orders for other cuisines (at that level). Finally, for the user-level bandit, α and β are updated with the user’s order data. As a result, a new user’s cuisine bandit is warm-started with higher-level marketplace data before each new order updates the bandit with their personal preferences.
>
> Another approach is to warm-start user preferences using data collected via a random policy. [Yahoo learned](https://arxiv.org/abs/1003.0146) user-specific CTR estimates (on random data) which were then added to context-free CTR estimates for news recommendations. They found that bandits warm-started with user preferences data were able to beat the context-free bandits.
>
> Data collected via a greedy policy can also be helpful for warm-start. [Twitter warm-started](https://arxiv.org/abs/2008.00727) their bandit on data collected by a greedy policy and found that warm-starting for more epochs (500 vs. 100) led to improved metrics on the test set.

> ## Evaluating bandits via off-policy evaluation
>
> **Several bandit implementations (e.g., Netflix, Yahoo) cite the [replay method by Li et al.](https://arxiv.org/abs/1003.5956)** for off-policy evaluation. Replay assumes that (i) individual events are independently and identically distributed and (ii) the logging policy chose each arm uniformly at random. The paper then states that the latter assumption can be weakened so any randomized policy—not just uniform random—can be used. (My understanding is that randomness is required for sufficient support and thus uniform randomness isn’t strictly necessary.)
>
> During evaluation, replay takes in the new policy (to be evaluated) and the logged policy events. If the new policy chooses the same action as the logged policy, the event is added to the history and the reward is updated. If not, the event is ignored with no reward update. ([Counterfactual evaluation](https://eugeneyan.com/writing/counterfactual-evaluation/) via Inverse Propensity Scoring is another alternative.)
