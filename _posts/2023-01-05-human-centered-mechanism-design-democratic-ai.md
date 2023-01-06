---
layout: post
title: "Human-centred mechanism design with Democratic AI"
author: Raphael Koster, Jan Balaguer, Andrea Tacchetti, Christopher Summerfield, et al.
date: 2022-07-04
categories: [research, ml/ai/nlp]
tags: [multi-agent-rl]
---

[https://www.nature.com/articles/s41562-022-01383-x](https://www.nature.com/articles/s41562-022-01383-x)

> Building artificial intelligence (AI) that aligns with human values is an unsolved problem. Here we developed a human-in-the-loop research pipeline called Democratic AI, in which reinforcement learning is used to design a social mechanism that humans prefer by majority. 
>
> A large group of humans played an online investment game that involved deciding whether to keep a monetary endowment or to share it with others for collective benefit. Shared revenue was returned to players under two different redistribution mechanisms, one designed by the AI and the other by humans. **The AI discovered a mechanism that redressed initial wealth imbalance, sanctioned free riders and successfully won the majority vote.** By optimizing for human preferences, Democratic AI offers a proof of concept for value-aligned policy innovation.

> We tested Democratic AI using a mechanism design problem based on an economic game. The game generalizes the linear public goods problem that has been extensively used to study human collective action[22](https://www.nature.com/articles/s41562-022-01383-x#ref-CR22),[23](https://www.nature.com/articles/s41562-022-01383-x#ref-CR23) (Fig. [1a](https://www.nature.com/articles/s41562-022-01383-x#Fig1)). In each of 10 rounds, each player *i* contributes an integer number *c*i of coins to a public investment fund, drawing upon an endowment *e*i, with the residual sum *e**i*−*c**i* remaining in a private account (endowments may vary across players, with one player receiving more than the others). Aggregated contributions over *k* = 4 players are scaled by a growth factor *r* = 1.6 (positive return on investment; this is equivalent to a marginal per capita return (MPCR) of 0.4). The public fund is paid back to players under a redistribution mechanism which specifies the fraction of total public investment that is returned to each player, conditional on their contribution and endowment. This game admits a continuum of mechanisms for redistribution popularly associated with opposing ends of the political spectrum[19](https://www.nature.com/articles/s41562-022-01383-x#ref-CR19), in which returns variously depend on the contributions of self and others[23](https://www.nature.com/articles/s41562-022-01383-x#ref-CR23).
>
> More generally, Exp. 1 highlights the challenge that the game poses for the mechanism designer: a redistribution scheme might be unpopular because it provokes a general collapse of contributions due to free riding, leads to unequal outcomes, or siphons funds away too aggressively from the wealthiest player, who then fails to provision the public fund. We thus asked whether an AI system could design a mechanism that humans preferred over these alternatives.

> ## Human-in-the-loop pipeline
>
> How then should the public funds be shared? The maximally popular policy could be one of these three canonical mechanisms or something else entirely. The size of the potential search space makes it hard to identify the preferred mechanism using traditional behavioural research methods. We thus developed a human-in-the-loop AI research pipeline to tackle this problem (Fig. [1d](https://www.nature.com/articles/s41562-022-01383-x#Fig1)). 
>
> First, we collected an initial sample of human data (Acquire) and used it to **train ‘virtual human players’ which were recurrent neural networks that learned to imitate human behaviour during the game and voted according to the same principles as human players** (Model; see Supplementary Fig. [1](https://www.nature.com/articles/s41562-022-01383-x#MOESM1)). This simulation step was necessary because training agents during online interaction with humans would have been prohibitively costly and time-consuming. 
>
> Third, **we optimized the mechanism design with deep RL, using policy gradient methods to maximize the votes of virtual human players (Optimize)**. Fourth, we sampled a new group of humans, and pitted the RL-designed redistribution mechanisms against rival baselines in a series of head-to-head majoritarian elections. This new human data was then used to **augment our player modelling process, which in turn improved optimization and led to potentially better mechanisms (Repeat)**. This pipeline builds on recent approaches that have used human data interactively to train artificial agents[31](https://www.nature.com/articles/s41562-022-01383-x?utm_source=pocket_reader#ref-CR31),[32](https://www.nature.com/articles/s41562-022-01383-x?utm_source=pocket_reader#ref-CR32),[33](https://www.nature.com/articles/s41562-022-01383-x#ref-CR33). We iterated this procedure to obtain a mechanism that we call the Human Centred Redistribution Mechanism or HCRM, which is the major focus of the remainder of this report.

> ## Voting
>
> we evaluated the AI-designed HCRM against the three canonical baselines introduced above. Groups of 4 human participants (n=2,508n=2,508) played successive incentive-compatible games of 10 rounds under two rival mechanisms, before voting for one that they preferred to play again (for additional payoff) in a final round.

> Our AI system designed a mechanism for redistribution that was more popular than that implemented by human players. This is especially interesting because unlike our agent, human referees could integrate information over multiple timesteps to reward or sanction players on the basis of their past behaviour. However, **on average the human-invented redistribution policy tended to reward the tail player insufficiently for making relatively large contributions (from their smaller endowment) to the public purse and was less popular than that discovered by HCRM**. Humans received lower volumes of training data than HCRM, but presumably enjoyed a lifetime of experience with social situations that involved fair and unfair distribution, so we think they represent a strong baseline, and a proof of concept for AI mechanism design.
