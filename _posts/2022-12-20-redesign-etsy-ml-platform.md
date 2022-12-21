---
layout: post
title: "Redesigning Etsy's machine learning platform"
author: Kyle Gallatin, Rob Miles
date: 2021-12-21
categories: [ml/ai/nlp, data]
tags: best-practice
---

[https://www.etsy.com/codeascraft/redesigning-etsys-machine-learning-platform/](https://www.etsy.com/codeascraft/redesigning-etsys-machine-learning-platform/)

> Above all in this iteration, we wanted to avoid building in-house tooling if possible. Our customers were already starting to experiment with open-source and managed technologies to work around the limitations of the V1 platform, and we wanted to collaborate with them. Leveraging managed solutions from [Google Cloud](https://cloud.google.com/) and industry standard tooling such as [TensorFlow](https://www.tensorflow.org/) would help new and existing ML practitioners train models quickly without having to rely on the platform team for help.
>
> Moving our platform in the direction of self-service would allow it to scale to the rapidly increasing number of ML practitioners at Etsy. Instead of burdening our customers with platform-specific abstractions, we wanted to let well-built, well-documented open source tools speak for themselves. This would both unblock our customers, and free up the ML Platform team to focus away from support and more on its core work.

> ### Training and Prototyping
>
> ML experimentation is a highly iterative process, requiring many ad hoc experiments. Practitioners need to be able to train and prototype new models quickly, in whatever language or framework seems appropriate, and deploy them reliably. Given the amount of data Etsy works with, that means our infrastructure has to be robust and scalable.
>
> Our training and prototyping platform largely relies on Google Cloud services like [Vertex AI](https://cloud.google.com/vertex-ai) and [Dataflow](https://cloud.google.com/dataflow), where customers can experiment freely with the ML framework of their choice. These services let customers easily leverage complex ML infrastructure (such as GPUs) through comfortable interfaces like [Jupyter Notebooks](https://jupyter.org/). Massive extract transform load (ETL) jobs can be run through Dataflow while complex training jobs of any form can be submitted to Vertex AI for optimization.
