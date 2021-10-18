---
layout: post
title: "The 80/20 rule in data (and why it doesn't have to be that way)"
author: Kelly Burdine
date: 2021-04-13
categories: data
tags: best-practice
---
[https://blog.aula.education/the-80-20-rule-in-data-and-why-it-doesnt-have-to-be-that-way-7659f8456d8f](https://blog.aula.education/the-80-20-rule-in-data-and-why-it-doesnt-have-to-be-that-way-7659f8456d8f), [Kelly Burdine](https://www.linkedin.com/in/kellyburdine/)

> **In** **just 3 months, my mighty data team of one** was able to:
> - Stand up a data warehouse in Snowflake with separate databases for raw data and production data including the automation of branch schemas for testing
> - Create 50+ separate ingestion pipelines using Stitch and Fivetran
> - Implement dbt and created 600+ models, 2000+ tests, and 50+ snapshots
> - Implement Metabase using AWS ECS and Docker

> I use a combination of Fivetran and Stitch to load all of our source data into Snowflake. Although I would prefer to have one load tool, neither option came with connector options for all of our sources. With that being said, both are really easy to set up and maintain (hit me up if you ever want to discuss the differences).

> I load all of the data into “raw” databases based on the loader. Then I use dbt to clean and transform the data and dump it into a production ready database. From there we use Metabase, a very lightweight point-and-click BI tool, to visualize and analyze our data. In addition, we can easily connect to the production analytics database from a Jupyter Notebook for more advanced analytics. 

> The cost? It varies between $1500-$2000 per month (note: I don’t have petabytes of data at this point).
