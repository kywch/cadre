---
layout: post
title: "Confidence intervals for policy evaluation in adaptive experiments"
author: Vitor Hadad, Susan Athey, et al.
date: 2021-04-13
categories: [research, statistics]
tags: [adaptive, metrics]
---

[https://www.pnas.org/content/118/15/e2014602118](https://www.pnas.org/content/118/15/e2014602118)

[https://github.com/gsbDBI/adaptive-confidence-intervals/](https://github.com/gsbDBI/adaptive-confidence-intervals/)

> Adaptive experimental designs can dramatically improve efficiency in randomized trials. But with adaptively collected data, common estimators based on sample means and inverse propensity-weighted means can be biased or heavy-tailed. This poses statistical challenges, in particular when the experimenter would like to test hypotheses about parameters that were not targeted by the data-collection mechanism. 
>
> In this paper, we present a class of test statistics that can handle these challenges. Our approach is to **adaptively reweight the terms of an augmented inverse propensity-weighting estimator to control the contribution of each term to the estimator’s variance.** 
>
> This scheme reduces overall variance and yields an asymptotically normal test statistic. We validate the accuracy of the resulting estimates and their CIs in numerical experiments and show that our methods compare favorably to existing alternatives in terms of mean squared error, coverage, and CI size.
