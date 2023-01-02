---
layout: post
title: "If data is a product, what is production?"
author: Benn Stancil
date: 2022-09-07
categories: data
tags: [strategy, leadership]
---

[https://benn.substack.com/p/what-is-production](https://benn.substack.com/p/what-is-production)

> But a huge percentage of a data team’s work sits somewhere in a muddy middle. We share one-off reports to answer one-off questions. We create new dashboards for a product launch, or to fill an urgent demand from an executive. We copy existing dashboards to make new versions that tweak some calculation for a specific customer or marketing campaign. We build data apps that solve narrow problems, like reconciling revenue figures for a financial audit. We ship report after report around the business, each of them addressing something specific, none of them meant to last forever. 
>
> When I send a report like this to someone, there’s an implicit contract attached to it: It works now, for the thing I said it would work for. It is, at that moment, *in production.* But that contract has an undefined scope and an uncertain expiration date. Will it work in the future? For how long? Can the report be extended to answer related questions? People don’t usually ask these questions, and data teams don’t usually volunteer answers.

> ## Commit more, less often
>
> I’ll take a hard line here: Data teams should be explicit and comprehensive in defining what’s in production. Whenever we create something with an external edge—a dashboard, an explorable dataset, an operational pipeline with a user or system on the other end—we should make a choice: Is this a production asset? If it is, it should be marked, recorded, and supported until decided otherwise. 
>
> We actually have to support the smaller set of things that we officially designate as being in production. We have to stand behind them, just as a product team stands behind features they ship. When some data source or dbt model changes, we have to make sure these things still work. And **when we want to stop supporting something, we have to actually deprecate it**, rather than letting it drift into slow decay.
