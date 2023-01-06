---
layout: post
title: "What is causal inference? An intro for data scientists"
author: Hugo Bowne-Anderson, Mike Loukides
date: 2022-01-18
categories: [data, statistics]
tags: [metrics, analytics, causal-inference]
---

[https://www.oreilly.com/radar/what-is-causal-inference/](https://www.oreilly.com/radar/what-is-causal-inference/)

> Whenever we consider the potential downstream effects of our decisions, whether consciously or otherwise, we are thinking about cause. We’re imagining what the world would be like under different sets of circumstances: what would happen if we do X? What would happen if we do Y instead? Judea Pearl, in [*The Book of Why*](https://oreil.ly/9Pn1N), goes so far as to say that reaching the top of the “ladder of causation” is “a key moment in the evolution of human consciousness” (p. 34). Human consciousness may be a stretch, but causation is about to cause a revolution in how we use data.
>
> **The ladder of causation**
>
> * ***Association*.** We, along with just about every animal, can make associations and observations about what happens in our world. Animals know that if they go to a certain place, they’re likely to find food, whether that’s a bird going to a feeder, or a hawk going to the birds that are going to the feeder. This is also the level at which statistics operates—and that includes machine learning.
> * ***Intervention*.** On this rung of the ladder, we can do experiments. We can try something and see what happens. This is the world of A/B testing. It answers the question “what happens if we change something?”
> * ***Counterfactuals*.** The third level is where we ask questions about what the world would be like if something were different. What might happen if I didn’t get a COVID vaccine? What might happen if I quit my job? Counterfactual reasoning itself emerges from developing robust causal models: once you have a causal model based on association and intervention, you can then utilize this model for counterfactual reasoning, which is qualitatively different from (1) inferring a cause from observational data alone and (2) performing an intervention.

> ## The End of Correlation, the Beginning of Cause
>
> As “data science” became a buzzword, we got lazy: we thought that, if we could just gather enough data, correlation would be good enough. We can now store all the data we could conceivably want (a petabyte costs around $20,000 retail), and correlation still hasn’t gotten us what we want: the ability to understand cause and effect. But as we’ve seen, it is possible to go further. Medical research has been using RCTs for decades; causal graphs provide new tools and techniques for thinking about the relationships between possible causes. Epidemiologists like John Snow, the doctors who made the connection between smoking and cancer, and the many scientists who have made the causal connection between human activity and climate change, have all taken this path.
>
> We have tools, and good ones, for investigating cause and weeding out the effects of confounders. It’s time to start using them.
