---
layout: post
title: "Sequential consumer choice as multi-cued retrieval"
author: Adam Hornsby, Bradley Love
date: 2022-02-25
categories: [research, cognitive]
tags: choicelogy
---

[https://www.science.org/doi/full/10.1126/sciadv.abl9754](https://www.science.org/doi/full/10.1126/sciadv.abl9754)

> Whether adding songs to a playlist or groceries during an online shop, how do we decide what to choose next? 
>
> We develop a model that predicts such open-ended, sequential choices using a process of cued retrieval from long-term memory. 
>
> **Using the past choice to cue subsequent retrievals, this model predicts the sequential purchases and response times of nearly 5 million grocery purchases made by more than 100,000 online shoppers.** 
>
> Products can be associated in different ways, such as by their episodic association or semantic overlap, and we find that consumers query multiple forms of associative knowledge when retrieving options. 
>
> Attending to certain knowledge sources, as estimated by our model, predicts important retrieval errors, such as the propensity to forget or add unwanted products. 

> First, choices and their response times were predicted by their similarity with the last choice, suggesting that choices cue the retrieval of subsequent options. Second, this behavior was best explained by **a mixture of episodic, semantic, and hierarchical knowledge**, suggesting that consumers reason about associations between products in different ways by querying different sources of knowledge. Third, how prone consumers were to different types of memory errors was predicted by their reliance on different types of memory, as assessed by model fits.

> We analyzed a dataset of sequential consumer purchases gathered from one of the United Kingdom’s largest supermarket retailers. The data contained 5,238,469 choices from 132,146 unique visitors across 42,837 unique products.
>
> ### Clickstream data
>
> Data capturing a sequence of clicks during a given shopping session are known as clickstream data. In this study, we used clickstream data collected by a large British retailer between 1 January 2015 and 31 March 2016. We used a random sample of visits resulting in a checkout during that period, each from a different customer, and only kept observations where a product was added to a shopper’s basket (more information in section S1.1). By shopping online, all customers were required to participate in the loyalty scheme of the retailer and therefore consented to having their data used for research. To preserve user privacy, we removed all customer identifiers from the data and kept only a cryptographic hash of each visit ID.
>
> ### In-store data
>
> To prevent information leaking into our analysis of online shopping behavior, we used a distinct dataset of in-store shopping behavior to develop knowledge representations. In-store grocery receipts are unordered, making it particularly useful for this study. The final dataset contained purchase information from 4,336,917 distinct baskets. We followed the same procedure of encryption as with the clickstream data to preserve the privacy of customers.
>
> ### Forgotten items
>
> Forgotten items were flagged through the use of a personalized recommender system, which prompted users about items that they may have forgotten at the end of their visit, before they checked out. The exact products shown to each customer were determined according to the recency and frequency of purchase in previous shops (online or in-store), deduplicated against products that had been purchased in the present visit. This page was displayed to users before payment.
>
> ### Removed items
>
> Shoppers could also remove products from their basket at any time during the shop. The total number of removed items was counted for each user. Further details about the method can be found in section S1.
