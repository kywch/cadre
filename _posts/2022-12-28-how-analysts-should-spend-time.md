---
layout: post
title: "How should analysts spend their time"
author: Mikkel Dengsoe
date: 2022-05-29
categories: [data, teamwork]
tags: [strategy, best-practice, gitlab]
---

[https://mikkeldengsoe.substack.com/p/time-allocation](https://mikkeldengsoe.substack.com/p/time-allocation)

Gitlab data-team handbook: https://about.gitlab.com/handbook/business-technology/data-team/

> However, one common topic is that data people spend upwards 50% of their time working reactively, often dealing with data issues or trying to find or get access to data. Examples of this are:
>
> - A stakeholder mentions that a KPI in a dashboard looks different to what it did last week and you have to answer why this is
>- A data test in dbt is failing and you have to understand what’s the root cause of the issue
> - You want to use a data point for a new customer segment and there are five different definitions when you search in Looker and it’s unclear which one to use

> Here’s an alternative for how data analysts could be spending their time
>
> ## More time for analysis
>
> Analysts should do… wait for it… analysis. They should have the freedom to get an idea on the way in to work and have it answered by lunch time. This type of work often requires long stretches of focused time, having the right tools in place and an acceptance that it's okay to spend half a day on work that may go nowhere. 
>
> I’ve seen this done particularly well when data analysts work closely with other people such as user research on quickly formulating hypotheses for which A/B tests to run well knowing that not all of them will be a home run. 
>
> > *“Taking that extra time to making sure you’re doing the right work instead of doing the work right is often some of time best spent”*
>
> ## Less time spent dealing with data issues 
>
> Data teams I’ve spoken to spend upwards 20% of their day on dealing with data issues and it gets more painful as you scale. When you are a small data team you can look at a few data models to get to the root cause. As you scale you start having dozens of other data people relying on your data models, engineering systems breaking without you being notified and code changes that you had no idea about impacting your data models.
>
> ## Less time finding what data to use
>
> The difficulty of finding the right data to use increases exponentially with data team size as well. When you’re a small team you know where everything is. As you get larger it becomes increasingly difficult and you often run into issues around having multiple definitions of the same metric. As you get really large just getting access to the right data can in the worse instances take months. 

> *“I’d recommend setting aside a few minutes each week to look back at the past week and note down how you spent your time. If you do this regularly you’ll get a surprisingly good understanding of whether you spend your time right”*
>
> We need to be able to apply some of what made life easy when you were a smaller data team to larger data teams. Some ideas of how this could be done: 
>
> - Every data asset should have an owner
> - Encapsulate data assets into domains with public and private access endpoints so not all data is accessible to everyone
> - Close the loop to data producers with shared ownership so issues are caught as far upstream as possible
> - Enable everyone to debug data issues so they don’t have to be escalated to the same few “data heroes“ each time
>
> *“Instead of treating every data issue as an ad-hoc fire, invest in fundamental data quality and controls that make data issues less likely to reoccur”*
