---
layout: post
title: "Unpopular opinion - Data scientists should be more end-to-end"
author: Eugene Yan
date: 2021-10-27
categories: [data, ml/ai/nlp, teamwork]
tags: [mlops, strategy]
---
[https://eugeneyan.com/writing/end-to-end-data-science/](https://eugeneyan.com/writing/end-to-end-data-science/)

> ## More context, faster iteration, greater satisfaction
>
> For most data science roles, being more end-to-end improves your ability to make meaningful impact. (Nonetheless, there are [roles](https://nvidia.wd5.myworkdayjobs.com/en-US/NVIDIAExternalCareerSite/job/US-CA-Santa-Clara/Senior-Deep-Learning-Data-Scientist--RAPIDS---AI_JR1929838) that focus on machine learning.)
>
> **Working end-to-end provides increased context.** While specialized roles can increase efficiency, it reduces context (for the data scientist) and leads to suboptimal solutions.
> > The trick to forgetting the big picture is to look at everything close-up. – Chuck Palahniuk
> > It’s hard to design a holistic solution without full context of the upstream problem. 
>
> **Communication and coordination overhead is reduced.** With multiple roles comes additional overhead. Let’s look at an example of a data engineer (DE) cleaning the data and creating features, a data scientist (DS) analysing the data and training the model, and a machine learning engineer (MLE) deploying and maintaining it.
>
> > What one programmer can do in one month, two programmers can do in two months. – Frederick P. Brooks
>
> ![img](https://eugeneyan.com/assets/sldc-specialists.jpg)
>
> **Iteration and learning rate is increased.** With greater context and lesser overhead, we can now iterate, fail (read: learn), and deliver value faster. This is especially important for developing data and algorithmic products. Unlike software engineering (a far more mature craft), we can’t do all the learning and design before we start building—our blueprints, architectures, and design patterns are not as developed. Thus, rapid iteration is essential for the design-build-learn cycle.



> ## End-to-end in Stitch Fix and Netflix
>
> Eric Colson of **Stitch Fix** was initially “lured to a function-based division of labour by the attraction of process efficiencies” (i.e., the [data science pin factory](https://multithreaded.stitchfix.com/blog/2019/03/11/FullStackDS-Generalists/)). But over trial and error, he found end-to-end data scientists to be more effective. Now, instead of organizing data teams for specialization and productivity, Stitch Fix organizes them for **learning and developing new data and algorithmic products**.
>
> > The goal of data science is not to execute. Rather, the goal is to learn and develop new business capabilities. … There are no blueprints; these are new capabilities with inherent uncertainty. … All the elements you’ll need must be learned through experimentation, trial and error, and iteration. – Eric Colson
>
> He suggests that data science roles should be made more general, with broad responsibilities agnostic to technical function and optimized for learning. Thus, his team hires and grows generalists who can conceptualize, model, implement, and measure. Of course, this is dependent on a solid data platform that abstracts away the complexities of infra setup, distributed processing, monitoring, automated failover, etc.

