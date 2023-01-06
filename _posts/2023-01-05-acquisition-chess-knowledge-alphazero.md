---
layout: post
title: "Acquisition of chess knowledge in AlphaZero"
author: Thomas McGrath, Andrei Kapishnikov, Nenad Tomasev, Valdimir Kramnik
date: 2022-11-14
categories: [research, ml/ai/nlp]
tags: multi-agent-rl
---

[https://www.pnas.org/doi/10.1073/pnas.2206625119](https://www.pnas.org/doi/10.1073/pnas.2206625119)

> We analyze the knowledge acquired by AlphaZero, a neural network engine that learns chess solely by playing against itself yet becomes capable of outperforming human chess players. 
>
> **Although the system trains without access to human games or guidance, it appears to learn concepts analogous to those used by human chess players.** We provide two lines of evidence. Linear probes applied to AlphaZero’s internal state enable us to quantify when and where such concepts are represented in the network. We also describe a behavioral analysis of opening play, including qualitative commentary by a former world chess champion.

> The success of an entirely self-taught system raises intriguing questions. 
>
> * What exactly has the system learned? 
> * Having developed without human input, will it be inevitably opaque? 
> * Can its training history shed light on human progress in chess? 
> * A human player naturally picks up basic concepts while playing: that a queen is worth more than a pawn or that a check to the king is important. Can we find qualitative or quantitative evidence of such concepts in AlphaZero’s neural network?

> Although the results are far from a complete understanding of the AlphaZero system, they show evidence for the existence of a broad set of human-understandable concepts within AlphaZero. We pair these quantitative results with qualitative analysis from a human world chess champion and compare AlphaZero’s choice of opening over its training to human progress in opening analysis. Furthermore, we observe interesting variance between concepts in terms of when they are learned during training, as well as where in the network’s reasoning chain they are learned.
