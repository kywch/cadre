---
layout: post
title: "TextWorldExpress: Simulating Text Games at One Million Steps Per Second"
author: Peter Jansen, Marc-Alexandre Cote
date: 2022-08-01
categories: [research, ml/ai/nlp]
tags: multi-agent-rl
---

[https://ar5iv.labs.arxiv.org/html/2208.01174](https://ar5iv.labs.arxiv.org/html/2208.01174)

https://github.com/cognitiveailab/TextWorldExpress

SayCan 같이 로봇 가르치는데 이런게 필요한게 아닐까?

> Text-based games offer a challenging test bed to evaluate virtual agents at language understanding, multi-step problem-solving, and common-sense reasoning. However, **speed is a major limitation of current text-based games**, capping at 300 steps per second, mainly due to the use of legacy tooling. 
>
> In this work we present TextWorldExpress, a high-performance implementation of three common text game benchmarks that increases simulation throughput by approximately **three orders of magnitude**, reaching over one million steps per second on common desktop hardware. This significantly reduces experiment runtime, enabling billion-step-scale experiments in about one day.
>
> 1. TextWorldExpress, a highly optimized reimplementation of three text game benchmarks focusing on instruction following, commonsense reasoning, and object identification.
> 2. We empirically demonstrate that this simulator runs up to *three orders of magnitude* faster than current tooling, reaching 300k steps per second (SPS) on a single-thread, and exceeding 1M SPS on modest multi-core desktop hardware. This substantially reduces experiment times (from weeks to hours) for sample-heavy machine learning agents.

TextWorld: https://www.microsoft.com/en-us/research/project/textworld/, https://github.com/microsoft/textworld 

https://ar5iv.labs.arxiv.org/html/2203.07540

github: https://github.com/allenai/ScienceWorld

>  ## ScienceWorld: Is your Agent Smarter than a 5 Grader?
>
> This paper presents a new benchmark, ScienceWorld, to test agents’ scientific reasoning abilities in a new interactive text environment at the level of a standard elementary school science curriculum. Despite the recent transformer-based progress seen in adjacent fields such as question-answering, scientific text processing, and the wider area of natural language processing, we find that current state-of-the-art models are unable to reason about or explain learned science concepts in novel contexts. For instance, models can easily answer *what* the conductivity of a previously seen material is **but struggle when asked *how* they would conduct an experiment in a grounded, interactive environment to find the conductivity of an unknown material**. 
>
> This begs the question of whether current models are simply retrieving answers by way of seeing a large number of similar input examples or if they have learned to reason about concepts in a reusable manner. 
>
> We hypothesize that **agents need to be grounded in interactive environments to achieve such reasoning capabilities**. Our experiments provide empirical evidence supporting this hypothesis—showing that a 1.5 million parameter agent trained interactively for 100k steps outperforms a 11 billion parameter model statically trained for scientific question-answering and reasoning via millions of expert demonstrations.

