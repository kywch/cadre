---
layout: post
title: "Predicting trends in the quality of state-of-the-art neural networks without access to training or testing data"
author: Charles H. Martin, Tongsu Peng, & Michael W. Mahoney
date: 2021-07-05
categories: [research, ml/ai/nlp]
tags: large-language-model
---

[https://www.nature.com/articles/s41467-021-24025-8](https://www.nature.com/articles/s41467-021-24025-8)

https://pypi.org/project/weightwatcher/

> In many applications, one works with neural network models trained by someone else. For such pretrained models, one may not have access to training data or test data. Moreover, one may not know details about the model, e.g., the specifics of the training data, the loss function, the hyperparameter values, etc. Given one or many pretrained models, it is a challenge to say anything about the expected performance or quality of the models. 
>
> Here, we address this challenge by providing a detailed meta-analysis of hundreds of publicly available pretrained models. We examine norm-based capacity control metrics as well as power law based metrics from the recently-developed Theory of Heavy-Tailed Self Regularization. We find that norm based metrics correlate well with reported test accuracies for well-trained models, but that they often cannot distinguish well-trained versus poorly trained models. 
>
> We also find that **power law based metrics can do much better—quantitatively better** at discriminating among series of well-trained models with a given architecture; and qualitatively better at discriminating well-trained versus poorly trained models. These methods can be used to identify when a pretrained neural network has problems that cannot be detected simply by examining training/test accuracies.
