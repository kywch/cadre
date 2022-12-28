---
layout: post
title: "The end of Big Data"
author: Benn Stancil
date: 2022-04-08
categories: data
tags: [innovation, databricks, snowflake]
---

[https://benn.substack.com/p/the-end-of-big-data](https://benn.substack.com/p/the-end-of-big-data)

> I first heard about Databricks in 2014. It was Silicon Valley hype, manifest. Databricks’ founders were brilliant computer scientists turned reluctant entrepreneurs. They were reinventing big data, which itself was reinventing the entire world. Growth rates were straight up, and overloaded sales reps were leaving their phones off the hook. 
>
> When I looked it up, my first reaction was that it was built for people smarter than me. Instead of a demo or product screenshots, I found technical papers explaining something I didn’t understand. The case studies talked about real-time enterprise workloads, streaming Spark applications, and distributed, highly-scalable data science model development. 

> The pitch we heard from Snowflake was **both the dumbest and most effective sales pitch I’ve ever heard. We were told that it was the same as Redshift—and really, the same as Postgres—but big, fast, and stable**. We didn’t see any glossy slide decks filled with stock images of strikingly handsome business professionals huddled around a conspicuously unbranded computer. ... We were told to just keep doing what we’d been doing, except if we did it with Snowflake, they’d host the whole thing, back it with bottomless storage, and run our queries faster than ever before—a strictly better, [Pareto improvement](https://www.investopedia.com/terms/p/paretoimprovement.asp#:~:text=A Pareto improvement is an,make any available Pareto improvement.).
>
> The pitch (and Snowflake) worked masterfully. As they undoubtedly anticipated, we started using Snowflake the same way we used Redshift, but quickly, after becoming accustomed to its speed and scale, found new things to do with it. Rather than worrying about precisely tuning our incremental loads in dbt, we started doing more full refreshes. We stopped carefully vetting which logs we wrote into our warehouse. We found new ways [to share data with customers](https://mode.com/developer/discovery-database/introduction/). We didn’t buy—and wouldn’t have bought—Snowflake for these things, but once they were so accessible, we happily picked them up. 

> Throughout our entire evaluation, we never considered Databricks. 
>
> In hindsight, we should’ve. **Databricks is, just like Snowflake, a fast, hosted, almost infinitely scalable database.** And, unlike Snowflake, it supports a [wider range of languages](https://docs.databricks.com/languages/index.html) that could’ve opened up entire classes of new applications that, once accessible, we would’ve been excited to try. But we never connected these dots during our evaluation because the story Databricks told was buzzwords. Snowflake’s was boring, and all we wanted—at least at first—was boring.

> Erik Bernhardsson [identified a similar dynamic](https://erikbern.com/2020/12/16/giving-more-tools-to-software-engineers-the-reorganization-of-the-factory.html) in software development. People who had little corporate use for software, like a small dentist’s office, built their first websites not because they suddenly had a huge need to do so; they created them because it became cheap to do it. This initial, “there’s no reason not to”-inspired foray into software uncorked a rush of latent demand: If you have a website, why not let people use it to book appointments? Why not build a system to message patients? Why not run a few ads that direct people to the site? If people don’t need something—but recognize that it’s better if they have it—few things can catalyze a market to grow faster than making it easier for people to buy it. 
>
> By following the same path, Big Data is finally starting to live up to its potential. It’s getting there, ironically, by giving up many of its hyped promises for a **very boring one: lower costs for marginally more useful things**. With Snowflake—and hopefully, with Databricks—we don’t get flying cars or predicting the future; we just get a little less headache. But, it turns out, that’s exactly what [us boring people](https://www.businessinsider.com/boring-jobs-hobbies-profession-personal-traits-scientists-study-2022-3?r=US&IR=T) need. 
