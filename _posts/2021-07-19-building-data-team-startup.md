---
layout: post
title: "Building a data team at a mid-stage startup: a short story"
author: Erik Bernhardsson
date: 2021-07-07
categories: [data, teamwork]
tags: best-practice
---
[https://erikbern.com/2021/07/07/the-data-team-a-short-story.html](https://erikbern.com/2021/07/07/the-data-team-a-short-story.html)

> "The backdrop is: you have been brought in to grow a tiny data team (~4 people) at a mid-stage startup (~$10M annual revenue), although this story could take place at many different types of companies.
>
> It's a made up story based on n-th hand experiences (for n ≤ 3), and quite opinionated. It's a story about teams and organization, not the tech itself. As a minor note, I deliberately use the term “data scientist” to mean something very broad."

> **July 1**
> - Lack of data, and fragmented data
>   - The product is poorly instrumented so data often doesn't exist in the first place
>   - A fragmentation of data systems, with data spread out over many different ones
>   - Brittle business processes driven by data but with little or no automation
> - An unclear expectation of what the data team's job is supposed to be
>   - Data scientists hired to do R&D and figure out some way to deploy AI or whatever — as a result not having any clear business goal
>   - Data team complaining about it being hard to productionize ML, yet the product team doesn't really seem to care about the feature
>   - People in need of “English-to-SQL translators”
> - A product team not trained to be data driven
>   - Product managers not thinking about data as a tool for building better features
>   - A lack of alignment between what product teams want to build versus what data teams have
> - A culture that fundamentally is at odds with being data driven
>   - A culture of celebrating shipping, versus celebrating measurable progress and learnings
>   - To the extent teams actually use metrics, they are inconsistent, poorly measured, and in some cases at conflict with other teams
> - No data leadership
>   - A fractured data org with various data people reporting into other functional areas
>   - Other departments not getting the help they need, so they work around the data team and hire lots of analysts
>   - Lack of standardizations of toolchain and best practice

> **July 8**
> You're starting to lay the most basic foundation of what is most critically needed: all the important data, in the same place, easily queryable. Opening up SQL access and training other teams to use it means a lot of the “SQL translation” goes away."

> **September 1**
> These are primarily *organizational* challenges. Teams don't know how to work with the data team. You're probably a bottleneck, even though you don't realize it. Other teams will build around the data team. Lots of “simple” analyses are not getting done.
>
> What I think makes most sense to push for is a *centralization the reporting structure*, but keeping the *work management decentralized*.
>
> Why? Primarily because it creates a much tighter feedback loop between data and decisions. If every question has to go through a central bottleneck, transaction costs will be high. On the other hand, you don't want to decentralize the *management*. Strong data people want to report into a manager who understands data, not into a business person.
>
> **September 2**
> "Instead, push out the resource management to other teams. Given them a handful of data people to work with, and let them work with them. Those data people will be able to iterate much more quicker, and will also develop valuable domain skills. This reduces the need for other teams to work around the data team and hire their own resources."

> **January 3**
> The good news is that the product team is starting to experiment with A/B tests. The bad news is that it's ignoring the results and that projects seem mostly driven by milestones and artificial deadlines. The *excellent* news is the CEO is pushing for teams to use data as the truth.
>
> Once there is an organizational pressure to be more data driven, this is a time to accelerate the way the data team works with other teams. In particular, people at the highest level will start to focus more on metrics, and it's your responsibility that the data team works with them on it. One simple thing that goes a long way is to work with every team and make sure they have their own dashboard with the top set of metrics they care about.

> **April 1**
> First of all, there's a glimmer of hope for some of the cool machine learning work. It seems like the product team is finally excited about launching the recommendation system as a small test. It was previously stuck because the product engineering team couldn't estimate the work and didn't want to commit to it, but the data team didn't have the practical software skills to bring it to something where the work of productionizing it is more tangible.
> What resolved this was the data team taking it one step further and actually building a demo. Not just does it bring it close to production, it also shows the potential in a more clear way.
>
> The other thing is, note what's happening with the supply chain team. The journey is roughly:
>
> 1. That team started out with their own “business analysts” (outside the data team) but need the data team to run queries for them to get data
> 2. Those business analysts are starting to run queries themselves with the help of the data team
> 3. They start to build up “shadow tech debt” (in this case monster SQL queries) which first causes a bunch of friction with the data team
> 4. The data team starts embedding into the team and helping them get to a better place
> 5. Because of the embedding, the need for business analysts goes down and data scientists goes up

> **July 1**
> You made it. You have transformed the organization to be truly data-native. 
> - The data team works cross functionally with lots of different stakeholders. 
> - Data and insights is used for planning. 
> - Data is used to drive business value and not a standalone lab with unclear goals. 
> - The company is working in an iterative way instead of big “waterfall” style planning, with quick data-driven feedback cycles. 
> - Metrics are defined in such a way that people feel a responsibility for generating business value. 
> - The data culture is driven both from above (the CEO pushing for it) as well as from below (people in the trenches). 
> - It's OK to fail if at least you learned something from it.

