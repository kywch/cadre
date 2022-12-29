---
layout: post
title: "You only need these 3 data roles in a data-driven enterprise"
author: Laszlo Sragner
date: 2021-05-24
categories: data
tags: [strategy, career]
---

[https://laszlo.substack.com/p/you-only-need-these-3-data-roles](https://laszlo.substack.com/p/you-only-need-these-3-data-roles)

> You can justify this categorisation by asking: Who is your customer? If your customer is an executive, you are doing **analytics** (DSA/BI). If you work on automated models, recommender systems, and your customers are your company’s clients, you belong to a data **product** function (DS/MLE etc.). If your customers are data roles from the previous two categories, then you belong to the **data** function (DWH/DE). 
>
> According to Self Determination Theory, you need to shape these roles so that they own the entire value chain from a stable infrastructure input down to their end customers. This allows them to solve their problems independently and measurably, leading to a high level of **autonomy**. By relying on a stable infrastructure and outsourcing rarely used functions to Engineering and DevOps, the team will be able to spend most of their time on their core skills, improving them on the job leading to **mastery**. Self-contained ownership and low friction communication with the rest of the company will lead to **relatedness**.

> ## **Data Warehouse Engineers (Data Function)**
>
> Their core function is to enter data into the company’s data domain and record it safely. 
>
> Their job is to provide a homogenous data infrastructure that the other two functions can utilise. Their focus is on **storing** the data, not processing it. This trend was validated when DWHs moved from ETL to ELT, focusing on “Load” instead of “Transform” as transform is problem-specific, while loading (i.e. storing) is more straightforward now with cheaper storage costs.
>
> ## **Data Science Analysts (Analytics Function)**
>
> Data Science Analysts are responsible for extracting meaningful information from collected data and present it to the executive aiding higher-level decision making. 
>
> They take data from DWH and transform it according to problem-specific needs. This is helped by moving to the ELT paradigm, as it allows better slicing of the Transform step between the three teams. After they transformed raw data into a consumable form, they can perform statistical analysis and modelling on it and present the results through custom visualisation. Their whole skillset is put into use for every project, and they are directly responsible for their outcome. They don’t need to wait for external teams to solve part of their value chain that might slow down or block their progress. 
>
> ## **Data Scientists (Product Function)**
>
> If you are creating features that must operate without supervision, you are part of the product team. Your clients are the company’s own clients, and you need to perform at a level of professionalism expected from software engineers.
>
> Just like DSAs, you take raw data from the DWH and transform it further. On this more consumable data, you do feature engineering and model building. Your model is deployed straight into production without a rewrite either by you or a third party. The engineering team works closely with you to prepare the containers and interfaces that let the model interoperate with the rest of their system. You are responsible for creating the model in a production-ready form from day one.

> Unfortunately, if you split or combine the role as described above, you violate at least one of the SDT principles, for example:
>
> - Make DSes work on Kubernetes (a DevOps skill): as K8S is a rarely used function, DSes will struggle to gain **mastery** in it.
> - Split Data Engineering from Data Science: Because DSes need to wait for DEs to produce the data, DSes will lose **autonomy** to reach their goals.
> - DSes making POCs siloed away from engineers: They don’t connect to the customer and the added value. They lose **relatedness** to the product team and their goals.
