---
layout: post
title: "Atlas: Few-shot learning with retrieval augmented language models"
author: Gautier Izacard, Patrick Lewis, Maria Lomeli, et al.
date: 2022-08-05
categories: [research, ml/ai/nlp]
tags: large-language-model
---

[https://arxiv.org/abs/2208.03299](https://arxiv.org/abs/2208.03299)

https://github.com/facebookresearch/atlas

Perhaps a good approach for fact checking?

> A large language model uses its huge complement of parameters to memorize information contained in its pretraining and
> fine-tuning datasets. It wouldn’t need to memorize so much — and thus wouldn’t need so many parameters — if it had access to documents on demand.

> Large language models have shown impressive few-shot results on a wide range of tasks. However, when knowledge is key for such results, as is the case for tasks such as question answering and fact checking, massive parameter counts to store knowledge seem to be needed. Retrieval augmented models are known to excel at knowledge intensive tasks without the need for as many parameters, but it is unclear whether they work in few-shot settings. 
>
> In this work we present Atlas, a carefully designed and pre-trained retrieval augmented language model able to learn knowledge intensive tasks with very few training examples. We perform evaluations on a wide range of tasks, including
> MMLU, KILT and NaturalQuestions, and study the impact of the content of the document index, showing that it can easily be updated. Notably, Atlas reaches over 42% accuracy on Natural Questions using only 64 examples, outperforming a 540B parameters model by 3% despite having 50x fewer parameters.
