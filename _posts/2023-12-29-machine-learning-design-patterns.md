---
layout: post
title: "More design patterns for machine learning systems"
author: Eugene Yan
date: 2023-04-27
categories: [data, ml/ai/nlp]
tags: best-practice
---

[https://eugeneyan.com/writing/more-patterns/](https://eugeneyan.com/writing/more-patterns/)

> Process Raw Data Only Once: To reduce redundancy
> The natural extension of this pattern is the feature store pattern which centralizes feature computation and storage. Feature stores enable feature reuse and consistency across applications, and reduce duplicate effort, compute, and storage.

> Human-In-The-Loop: To collect explicit labels
> That said, we may not require as much HITL in the future. Recent studies have found large language models (LLMs) to perform on par, or better than, people at labeling ground truth.

> Data Augmentation: To increase data size and diversity
> Besides data augmentation, another way to expand the dataset is by creating synthetic data. For example, Cloudflare generated synthetic data to increase the diversity of their training data that is used to train models to classify malicious HTTP requests.

> Hard Negative Mining: To get difficult samples
> One approach to hard mining is to analyze model predictions for misclassified or low-confidence examples, find similar examples (e.g., nearest neighbors), and emphasize them in subsequent training. This forces the model to learn from its mistakes and improve.
> Another approach is to blend hard negatives in curriculum learning, where the training data is sorted to gradually increase sample difficulty. The model starts learning from easy samples before progressively tackling harder samples as it becomes more capable.

> Reframing: To simplify the problem or label
> Another example of reframing is Shopify’s product classifier. To simplify the problem of classifying items into a 5,000 class, hierarchical taxonomy, they converted n one-vs-all classifiers into a single binary classifier. They did this by exploding the training data to create a row for each category for each product, and then appending the category to the features. Finally, if the product-category pair is valid, it gets a label of 1, and 0 otherwise. They also considered hierarchy by giving parents of a valid category a label of 1.    --> This allowed them to train a single logistic regression model instead of n  individual classifiers, reducing computation cost and keeping the system simple. Accounting for parent-child relationships also enabled them to learn from the taxonomy structure.
> A final example is the reframing of recommendations from the co-occurrence problem (e.g., matrix factorization) into a sequential problem (e.g., RNNs, Transformers). One of the earliest papers to do this applied GRUs for session-level recommendations. It was motivated by the need to learn from short, session-level data due to the lack of long user histories (such as those that Amazon or Netflix has).

> Cascade: To split a problem into smaller problems
> Twitter’s recently open-sourced recsys follows this pattern (image above). Their recsys is a cascade of (i) candidate sourcing (aka retrieval), (ii) heavy ranking, (iii) heuristics and filtering, and (iv) ads blending. Multiple components contribute to retrieval before the heavy ranker (a parallel masknet) does the ranking. Finally, business rules are layered on.

> Data Flywheel: To continuously improve & build a moat
> The data flywheel pattern revolves (pun intended) around continuously collecting data which then improves models which then improves user experience. This leads to more usage, which leads to more data to further improve models, creating a virtuous cycle.

> Business Rules Layer: To augment or override outputs
> Also, if you’ve been using ChatGPT, you may have experienced its rules layer. These constraints ensure that its responses align with ethical guidelines and is safe for users.

> Evaluate before Deploy: For safety and reliability
> To adopt this pattern, simply have a validation hold-out when (re)training models. Given the strong temporal aspect in most production systems, the validation set should typically be split by time; using a random split or cross-validation could lead to overly optimistic evaluation metrics, especially if future data leaks into the training set.