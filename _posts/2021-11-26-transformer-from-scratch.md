---
layout: post
title: "Transformer from scratch"
author: Brandon Rohrer
date: 2021-10-29
categories: ml/ai/nlp
tags: [transformer, to-dos]
---

[https://e2eml.school/transformers.html](https://e2eml.school/transformers.html)

> Transformers were introduced in this 2017 [paper](https://proceedings.neurips.cc/paper/2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf) as a tool for sequence transduction—converting one sequence of symbols to another. The most popular examples of this are translation, as in English to German. It has also been modified to perform sequence completion—given a starting prompt, carry on in the same vein and style. They have quickly become an indispensible tool for research and product development in natural language processing.
>
> Before we start, just a heads-up. We're going to be talking a lot about matrix multiplications and touching on backpropagation (the algorithm for training the model), but you don't need to know any of it beforehand. We'll add the concepts we need one at a time, with explanation.
>
> ...
>
> ### Wrap up
>
> If you're still with me, thank you. I hope it was worth it. This is the end of our journey. We started with a goal of making a speech-to-text converter for our imaginary voice-controlled computer. In the process, we started from the most basic building blocks, counting and arithmetic, and reconstructed a transformer from scratch. My hope is that the next time you read an article about the latest natural language processing conquest, you'll be able to nod contentedly, having pretty darn good mental model of what's going on under the hood.
>
> ### Resources and credits
>
> - ► The O.G. [paper](https://proceedings.neurips.cc/paper/2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf), Attention is All You Need.
> - ► A wildly helpful Python [implementation](https://nlp.seas.harvard.edu/2018/04/03/attention.html) of the transformer.
> - ► Jay Alammar's insightful transformer [walkthough](https://jalammar.github.io/illustrated-transformer/).
> - ► Lukasz Kaiser's (one of the authors) [talk](https://www.youtube.com/watch?v=rBCqOTEfxvg) explaining how transformers work.
> - ► The [illustrations](https://docs.google.com/presentation/d/1Po-GY7X-mXmPKHr8Vh29S4tFPv23TjeY-jq-yShlivM/edit?usp=sharing) in Google Slides.

