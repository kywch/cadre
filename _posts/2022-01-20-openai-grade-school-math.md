---
layout: post
title: "The sobering truth about the impact of your business ideas"
author: Eric Colson, Daragh Sibley, Dave Spiegel
date: 2021-10-26
categories: [research, ml/ai/nlp, math]
tags: [math-nlp, to-dos]
---

[https://openai.com/blog/grade-school-math/](https://openai.com/blog/grade-school-math/)

[https://arxiv.org/pdf/2110.14168.pdf](https://arxiv.org/pdf/2110.14168.pdf)

[https://github.com/openai/grade-school-math](https://github.com/openai/grade-school-math)

> We’ve trained a system that solves grade school math problems with nearly twice the accuracy of a fine-tuned GPT-3 model. It solves about 90% as many problems as real kids: a small sample of 9-12 year olds scored 60% on a test from our dataset, while our system scored 55% on those same problems. This is important because today’s AI is still quite weak at commonsense multistep reasoning, which is easy even for grade school kids. We achieved these results by training our model to recognize its mistakes, so that it can try repeatedly until it finds a solution that works.

> To match human performance in complex logical domains, our models must learn to recognize their mistakes and to choose their steps carefully. To that end, we train verifiers to evaluate whether or not a proposed solution is correct. To solve a new problem, we use verifiers to select the best among many proposed solutions. We collected the new GSM8K dataset to evaluate our methods, and we are releasing this dataset to facilitate research.

> GSM8K consists of 8.5K high quality grade school math word problems. Each problem takes between 2 and 8 steps to solve, and solutions primarily involve performing a sequence of elementary calculations using basic arithmetic operations (+ − × ÷) to reach the final answer. Fine-tuned state-of-the-art language models perform poorly on this dataset, primarily due to the high diversity of problems. At the same time, GSM8K solutions depend only on elementary concepts, so achieving high test performance is a tractable goal.

> Producing correct arguments and recognizing incorrect ones are key challenges in developing more general AI. Grade school math is an ideal testbed for these capabilities. The problems in GSM8K are conceptually simple, yet one subtle mistake is enough to derail an entire solution. Identifying and avoiding such mistakes is a crucial skill for our models to develop. By training verifiers, we teach our models to separate the good solutions from the ones that didn’t quite work out. We expect these skills to become increasingly relevant as we attempt to apply our models to more logically complex domains.
