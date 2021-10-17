---
layout: post
title: "268 billion events with snowplow analytics and snowflake at CarGurus"
author: bostada
date: 2020-07-15
categories: [product, data]
tags: [analytics, best-practice]
---
[https://www.bostata.com/268-billion-events-with-snowplow-snowflake-at-cargurus](https://www.bostata.com/268-billion-events-with-snowplow-snowflake-at-cargurus)

> Two years ago we set up [**Open-Source Snowplow**](https://github.com/snowplow/snowplow/wiki) at [**CarGurus**](https://www.cargurus.com/) to fulfill a need for self-managed client-side instrumentation. Since that time it has become incredibly impactful for the entire company and has scaled significantly beyond what was originally envisioned. The following is an overview of **why we set up the system**, **our experience with it,** **what we have learned**, and **where we see it continuing to go.**

> **The Stats At Time of Writing**
>
> - Total events collected: >268 billion
> - Data collected: > 1.5pb (uncompressed)
> - Event volume: ~ 1 billion events/day
> - Max Daily Throughput: ~ 15k events/second (sustained during peak hours)
> - Distinct events: hundreds and hundreds
> - Infrastructure upgrade duration: less than two minutes with zero downtime
> - Distinct sites with Snowplow tracking: > 180

> **We wanted to independently manage and scale data collection systems.**

> **We wanted to own all data that was generated.****

> **The world of compliance is changing rapidly and we needed the ability to audit every piece of information.**

> **We wanted to modernize event collection systems.**

> Another requirement of choosing Snowplow was its ability to quickly and effectively introduce a [**lambda architecture**](http://lambda-architecture.net/) into our analytics stack. As customer needs and demands evolved, we found that having both a real-time, low-latency (on the order of hundreds of milliseconds) component of the event pipeline as well as a batch-based, higher-latency (on the order of minutes) component gave us significant flexibility to proactively fulfill stakeholder asks before they surfaced*.*

> Our pipelines are set up in AWS with [**Kinesis**](https://aws.amazon.com/kinesis/) as transport and [**Snowflake**](https://www.snowflake.com/) as long-term data storage. As stakeholders need real-time access to enriched data, Kinesis is the go-to location. If stakeholders need access to historical event data or want to augment it with other sources in the data warehouse, Snowflake is the place to go.
