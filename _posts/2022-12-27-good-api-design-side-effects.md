---
layout: post
title: "My personal history with NLP or side-effects of good API design"
author: Peter Baumgartner
date: 2022-01-16
categories: data
tags: best-practice
---

[https://www.peterbaumgartner.com/blog/personal-history-and-api-design/](https://www.peterbaumgartner.com/blog/personal-history-and-api-design/)

> The hard problem in data science isn’t training the best model, but rather a collection of difficult sub-problems:
>
> - it’s understanding what the problem is
> - having a set of tools you know how to use
> - having an organizational framework (conceptual model) that those tools can fit into
> - being able to customize your solution when necessary
>
> In my own data science adventure, discovering each of these sub-problems has been a critical part of my journey. It helps to have well-designed tools, like spaCy, to help with all four steps—whether it’s your first day as a data scientist or you’re a seasoned expert.

> There’s a key lesson I’ve learned about “what works” on most projects - what works is actually the models themselves. In most cases, the performance of any algorithm or machine learning model is not usually a reason why a project fails. There are rare exceptions when performance is worse than a random guess, but even if it’s slightly better than random, there’s almost always value in automating some decision if you can frame the problem correctly, even if this done only to understand how a model makes different decisions than a human would.
>
> Framing the problem correctly *is* where most projects stumble. There are many obstacles in the way of a correct problem framing:
>
> - The stakeholders (i.e. the client or subject matter experts) do not understand what machine learning can do
>   - In one direction, this can just be naive ignorance - it’s not their field, so they shouldn’t know it
>   - In the opposite direction, this can be insane expectations due to hype combined with misunderstanding, leading to inflated expectations about what can happen
> - There might be a set of methods that can work for your scenario, but if you don’t already know what those are you can’t apply them.
>   - Also, it’s difficult to keep up up with the insane pace of new methods and models.
> - You might know a method (or set of methods) that you think might work for a given problem, but once you actually start working with it you discover issues with it.
>
> In sum, the big problem with executing successful projects is solving this data science alignment problem—mapping the problem at hand to the the combination of methods you know.
>
> In the social sciences, the best description of this problem I’ve seen of this is this paper: [Machine Learning for Social Science: An Agnostic Approach](https://www.annualreviews.org/doi/full/10.1146/annurev-polisci-053119-015921)
>
> > By agnostic, we mean that our general view is that in many instances there is no correct or true model that we target with machine learning methods, and there is no one best method that can be used for all applications of a data set. Instead, we advocate that researchers use the method that optimizes performance for their particular research task. Unlike in many computer science applications, this task will often not be prediction but may instead be discovery, measurement, description, or causal inference. How we evaluate the quality of a model and compare models will be specific to the research question.

>  Here’s Norman with his basic definition of what makes something complex:
>
> > What makes something simple or complex? It’s not the number of dials or controls or how many features it has: It is whether the person using the device has a good conceptual model of how it operates.
>
> Norman’s point in this book is that perceived complexity arises from a mismatch between the system of the thing *as designed* or *as it exists* and the conceptual model of the person using that system. How do we reduce complexity? Norman explains (emphasis mine):
>
> > Complexity can be tamed, but it requires considerable effort to do it well. Decreasing the number of buttons and displays is not the solution. The solution is to **understand the total system, to design it in a way that allows all the pieces fit nicely together, so that initial learning as well as usage are both optimal.**
>
> The spaCy API for this task is aligned with this idea. It makes it easy to understand what you need to solve this problem: first you need a model, that model processes the text in various ways including tokenizing it and assigning a part of speech to each token. The tokens are saved with the document, so now you can do arbitrary things with them (like put them in a list if they’re nouns). This *initial learning* gets you closer to understanding the *total system* because it’s clear what objects exist and how you interact with them.

> **Tools for Doing and Thinking: Helping with the Data Science Alignment Problem**
>
> “Industrial-strength NLP” is a phrase you’ll see if you go back and look at an [archived version of spacy.io](https://web.archive.org/web/20160905151957/http://spacy.io/). When I started using it, spaCy had a ton of functionality in order to get things done—which, when I started using it was exactly what I needed to do. However, as I matured as a data scientist, I started to think more about this alignment problem rather than just getting stuff done. Fortunately, as spaCy matured it expanded from a tool to help do natural language processing to a tool to help think about *ways* I could do natural language processing.
>
> For example, if you go look at the [spaCy Usage](https://spacy.io/usage/) API docs, you’ll notice the guides are organized around NLP tasks. Organizing the *things* you can do in this way helps us with our original alignment problem: the ability to organize and “bucket” the types of tasks you can do is essential because you need to map them to the problem you’re trying to solve.
