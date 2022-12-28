---
layout: post
title: "How (not) to scale deep learning in 6 easy steps"
author: Sean Owen
date: 2019-08-15
categories: ml/ai/nlp
tags: [mlops, databricks, petastorm, horovod]
---

[https://www.databricks.com/blog/2019/08/15/how-not-to-scale-deep-learning-in-6-easy-steps.html](https://www.databricks.com/blog/2019/08/15/how-not-to-scale-deep-learning-in-6-easy-steps.html)

> This blog will instead walk through basic steps to avoid common performance pitfalls in training, and then the right steps, considered in the right order, to scale up by applying more complex tooling and more hardware. Hopefully, you will find your modeling job can move along much faster without reaching immediately for a cluster of extra GPUs.
>
> There are new best practices and pitfalls to know when setting out to train a model. A few of these helped the small image classification problem here achieve the same 78.5% accuracy while reducing runtime over 7x. The first steps in scaling aren’t more resources, but looking for easy optimizations:
>
> 1. Use a pre-trained base layer where possible
> 2. Use a GPU, almost always
> 3. Use early stopping
> 4. Max out GPU utilization with larger batch sizes - and learning rates
>
> Scaling to train on an entire large data set in the cloud requires some new tools, but not necessarily more GPUs at first. With careful use of Petastorm, 10x the data helped achieve 83.6% accuracy in about 10x the time on the same hardware.
>
> 1. Use Petastorm to handle large data sets efficiently during training
>
> The next step of scaling up means utilizing multiple GPUs with tools like Horovod, but doesn't necessarily mean a cluster of machines, unlike in ETL jobs where a cluster of machines is the norm. A single 4 GPU instance allowed training to finish 4x faster and achieve 84.4% accuracy. Only for the largest problems are multiple GPU instances necessary, but Horovod can help scale there further without much overhead, to improve accuracy even further.
>
> 1. Scale to multiple GPUs on one machine with Horovod
> 2. Scale ot more GPUs spread across a cluster of machines with Horovod

