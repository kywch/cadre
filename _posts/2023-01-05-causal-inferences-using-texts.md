---
layout: post
title: "How to make causal inferences using texts"
author: Naoki Egami, Christian Fong, Justin Grimmer, Margaret Roberts, Brandon Stewart
date: 2022-10-19
categories: [research, social, ml/ai/nlp]
tags: causal-inference
---

[https://www.science.org/doi/full/10.1126/sciadv.abg2652](https://www.science.org/doi/full/10.1126/sciadv.abg2652)

> Text as data techniques offer a great promise: the ability to inductively discover measures that are useful for testing social science theories with large collections of text. Nearly all text-based causal inferences depend on a latent representation of the text, but we show that estimating this latent representation from the data creates underacknowledged risks: we may introduce an identification problem or overfit. 
>
> To address these risks, we introduce a split-sample workflow for making rigorous causal inferences with discovered measures as treatments or outcomes. We then apply it to estimate causal effects from an experiment on immigration attitudes and a study on bureaucratic responsiveness.

> Here, we have introduced a rigorous machine learning workflow for causal inference with text, identified problems that emerge when using text data for causal inference, and then described a procedure to resolve those problems. In this conceptual framework, we have clarified the central role of *g*, the codebook function, in making the link between the high-dimensional text and our low-dimensional representation of the treatment or outcome. In doing so, we clarify two threats to causal inference: the FPCILV—an identification issue—and overfitting—an estimation issue. **We demonstrate that both the identification and estimation concerns can be addressed with a simple split of the dataset into a training set used for discovery of *g* and a test set used for estimation of the causal effect**. More broadly, we advocate for research designs that allow for sequential experiments that explicitly set aside research degrees of freedom for discovery of interesting measures, while rigorously testing relationships within experiments once these measures are defined explicitly.
