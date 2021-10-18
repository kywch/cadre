---
layout: post
title: "The missing piece of the modern data stack"
author: Benn Stancil
date: 2021-04-22
categories: data
tags: metrics
---
[https://benn.substack.com/p/metrics-layer](https://benn.substack.com/p/metrics-layer)

> To see the problem, consider the journey that data follows to reach that dashboard. After being written into a warehouse (e.g., Snowflake) by an ingestion tool (e.g., Fivetran), data is updated by a transformation tool (e.g., dbt) several times, passing through a couple types of aggregations along the way:
>
> - **Cleaned granular data**: The first stage creates dimension and fact tables, which maintain the same degree of granularity as raw tables while removing the irregularities and aesthetic irritations that make raw data difficult to work with. In these cleaned tables, malformed rows are excluded, columns are renamed so they’re easier to understand, fields like phone numbers are standardized, and tables for new concepts that don’t exist in raw form, such as dimension_web_sessions, are created. Data is polished at this stage, but not aggregated—if there’s a raw table that has one row per email, dimension_emails will have one row per email too.
> 
> - **Rollups**: A second stage rolls up granular data into aggregated metrics tables. For example, a rollup_active_users table might include rows for daily, weekly, rolling 7-day, and rolling 28-day active users, signups, returning users, and so on. These tables only include metrics, obscuring which records compose those aggregates. While the rollup_active_users table will tell you that 100 people were active over the seven days prior to April 10th, it won’t tell you who those 100 people were.
>
> To extract metrics from these tables, people have two options: They can pull from pre-aggregated rollups, or they can compute new metrics on the fly from granular dimension tables.

> A better architecture would do for metrics what dbt did for transformed data—make them globally accessible to every other tool in the data stack. Rather than each tool defining their own aggregations, the metrics layer is a centralized clearing house for how all metrics are calculated.

