---
layout: post
title: "Clean architecture: How to structure your ML projects to reduce technical debt"
author: Laszlo Sragner
date: 2022-06-20
categories: data
tags: [mlops, best-practice]
---

[https://laszlo.substack.com/p/slides-for-my-talk-at-pydata-london](https://laszlo.substack.com/p/slides-for-my-talk-at-pydata-london)

Youtube: https://www.youtube.com/watch?v=QXfsS-ZOeyA

> Quick summary of slides:
>
> - What do we mean by “ML products”?
> - Why does tech debt matter in ML?
> - How ML Lifecycle affects tech debt?
> - Tech Debt vs Tech Mess (This slide was received by a significant amount of laughter)
> - What is refactoring?
> - What is Experimental-Operational Symmetry (EOS)?
> - What is decoupling?
> - Inversion of Control and Dependency Injection
> - Clean Architecture in Production
> - Three Useful Design Patterns (Adapter/Factory/Strategy)
> - Workflow building a system from scratch
> - Interoperability with Jupyter notebooks

[https://laszlo.substack.com/p/you-only-need-2-design-patterns-to](https://laszlo.substack.com/p/you-only-need-2-design-patterns-to)

> ## **The Factory Pattern**
>
> In its simplest form, the Factory Pattern is about generating objects.
>
> Its primary role is to separate the objects from their creation. In Data Science, this usually means that using data is decoupled from where is this data coming from. Employing the pattern allows you a layer of abstraction in your computations where you can work with classes but don’t need to worry about their origin. Let’s refactor the above example in four quick steps:
>
> - Step 1: move loading code to a new class
> - Step 2: add loading class to the constructor
> - Step 3: refactor loading to use new loader
> - Step 4: create a loader at usage time
>
> ## **The Strategy Pattern**
>
> The second major problem is deciding on which algorithm to use in a concrete implementation. 
>
> Often you face choices that cannot be decided early on and need to be changed later. If this happens, you need to rewrite the main body of your code because algorithms are typically tightly coupled in it, leading to potentially breaking changes.
>
> To help with that, one can abstract out the algorithm with a Strategy Pattern. Just like in the Factory Pattern, this starts with an interface. Instead of calling the algorithm directly, you will wrap it with a class and call a class member function to get the output. Any input is passed to the member function, and if generic parameters are the same for all calls, you can add them to the constructor.
>
> - Step 1: move code to a new class
> - Step 2: add a new class as a member variable
> - Step 3: refactor usage
> - Step 4: create a lemmatizer at usage time
>
> ## Other useful patterns
>
> - Bridge Pattern - to join data with model
> - Adapter Pattern - to do dependency inversion
> - Builder Pattern - to build complex classes
