---
layout: post
title: "Why nvidia's AI supremacy is only temporary"
author: Pete Warden
date: 2023-09-10
categories: ml/ai/nlp
tags: strategy
---

[https://petewarden.com/2023/09/10/why-nvidias-ai-supremacy-is-only-temporary/](https://petewarden.com/2023/09/10/why-nvidias-ai-supremacy-is-only-temporary/)

> #1 – Inference will Dominate, not Training
> Somebody years ago told me “Training costs scale with the number of researchers, inference costs scale with the number of users”.

> #2 – CPUs are Competitive for Inference
> Old-timers will remember the early days of the internet when most of the cost of setting up a dot-com was millions of dollars for a bunch of high-end web server hardware from someone like Sun. This was because they were the only realistic platform that could serve web pages reliably and with low-latency. They had the fastest hardware money could buy, and that was important when entire sites needed to fit on a single machine. Sun’s market share was rapidly eaten by the introduction of software that could distribute the work across a large number of individually much less capable machines, commodity x86 boxes that were far cheaper.

> Training is currently very hard to distribute in a similar way. The workloads make it possible to split work across a few GPUs that are tightly interconnected, but the pattern of continuous updates makes reducing latency by sharding across low-end CPUs unrealistic. This is not true for inference though. The model weights are fixed and can easily be duplicated across a lot of machines at initialization time, so no communication is needed. This makes an army of commodity PCs very appealing for applications relying on ML inference.

> #4 – Application Costs Rule
> When inference dominates the overall AI budget, the hardware and workload requirements are very different. Researchers value the
ability to quickly experiment, so they need flexibility to prototype new ideas. Applications usually change their models comparatively infrequently, and may use the same fundamental architecture for years, once the researchers have come up with something that meets their needs. We may almost be heading towards a world where model authors use a specialized tool, like Matlab is for mathematical algorithms, and then hand over the results to deployment engineers who will manually convert the results into something more efficient for an application. This will make sense because any cost savings will be multiplied over a long period of time if the model architecture remains constant (even if the weights change).